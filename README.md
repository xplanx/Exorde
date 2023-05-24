# Exorde



Exorde is the web3 protocol that empowers developers to crawl and link all public data on the web.
<p style="font-size:14px" align="right">
<a href="https://t.me/B_FARS" target="_blank">Join our telegram <img src="https://user-images.githubusercontent.com/50621007/183283867-56b4d69f-bc6e-4939-b00a-72aa019d1aea.png" width="30"/></a>
</p>

<h1 align=center><img src="https://uploads-ssl.webflow.com/60aec7ee1888490c4031cbcd/62028bb11f77dff6ed7db9fc_landscape-logo-white.svg" width="250"><br>Testnet Tutorial</h1>

## Prepare
1.Requirement
  <table>
    <tr>
      <th>Component
      <th>Specifications
    </tr>
    <tr>
      <td>CPU	
      <td> 2-4 Core
    </tr>
    <tr>
      <td>RAM	
      <td>At least 2-4 GB of memory (RAM)
    </tr>
    <tr>
      <td>Storage
      <td>At least 50 GB of SSD disk storage
    </tr>
    <tr>
      <td>Connection
      <td>At least 100mbps network bandwidth
    </tr>
  </table>
  
 2. Recommendation VPS
<table>
    <tr>
      <th>Provider
      <th>Link
    </tr>
    <tr>
      <td>PQ HOSTING	
      <td>https://pq.hosting/?from=542984
    </tr>
   
</table>

## Usefull Link
- Join Discord : https://discord.gg/exordelabs <br>
- Official Github : https://github.com/exorde-labs/ExordeModuleCLI/ <br>
- Website : https://exorde.network

## Installation
There are have two option for installing ExordeLabs, ``Anaconda`` and ``Docker``. For example we choose to installing with ``Docker``.

### Update apt

```
sudo apt-get update
sudo apt-get install \
    ca-certificates \
    curl \
    gnupg \
    lsb-release \
    screen \
    git
```

### Adding official key of GPG Docker

```
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
```

### Repository Setting

```
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

### Installing Docker

```
sudo apt-get install ca-certificates curl gnupg lsb-release -y
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
```

### Docker Version

```
docker --version
```

### Installing Exorde

```
git clone https://github.com/exorde-labs/ExordeModuleCLI.git
```

### Navigate To Folder Exorde

```
cd ExordeModuleCLI
```

### Build Docker

```
docker build -t exorde-cli . 
```

### Run Validator
Open new screen with ``screen``

```
screen -Rd exorde
```
Next run this command

```
docker run -it exorde-cli -m YOUR_EVM_ADDRESS -l LEVEL_LOGGING
```
> Change ``YOUR_EVM_ADDRESS`` with your address from Metamask (prefix 0x) and ``LEVEL_LOGGING`` change with 0,1,2,3,4 

For Example

```
docker run -it exorde-cli -m 0x0F67059ea5c125104E46B46769184dB6DC405C42 -l 4
```
If you want close to terminal you can press ``CTRL + A + D`` also if you want open again to terminal use 

```
screen -r exorde
```

### Logging Description

- 0 = no logs,
- 1 = general logs
- 2 = validation logs
- 3 = validation + scraping logs
- 4 = detailed validation + scraping logs (e.g. for troubleshooting)

**Dont forget to giving feedback on Discord**

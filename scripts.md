### Server Updates:
This script is used to update an ubuntu server. <br>
Become root:
```
sudo -i
```
Create the Script: 
```
nano server_update.sh
```
```
#!/bin/bash

export DEBIAN_FRONTEND=noninteractive

apt update
apt upgrade -y

# Other Tools
apt install net-tools
apt install libuser -y  
snap install emacs --classic 

# Java 
apt install default-jre -y
apt install openjdk-8-jdk -y
apt install openjdk-11-jre-headless
apt install -y openjdk-8-jre
apt install openjdk-11-jdk
```
Make the script executable: 
```
chmod +x server_update.sh
```
Run the script:
```
./server_update.sh
```
## 
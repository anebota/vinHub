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
##


```
#!/bin/bash
# Make script non interactive 
# Run as root for the first time 
export DEBIAN_FRONTEND=noninteractive

# Update and upgrade ubuntu
apt update
apt upgrade -y

# Install Jaja 
apt install default-jre -y
apt install openjdk-8-jdk -y

# Install Other tools 
apt install net-tools
apt install libuser -y  
snap install emacs --classic
apt-get install jq -y

```
##


Make the script executable: 
```
chmod +x server_update.sh
```


Run the script:
```
./server_update.sh
```
## 
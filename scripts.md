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
## 
##

### Change Hostname:
Become root:
```
sudo -i
```
Create the Script: 
```
nano hostname.sh
```
```
#!/bin/bash
# This is a script to permanently change the hostname of an Ubuntu instance.
# Ask for the new hostname.
echo -n "Enter the new hostname: "
read new_hostname

# Get the current hostname
old_hostname=$(hostname)

# Get the IP address of the system
ip_address=$(hostname -I | cut -d' ' -f1)

# Edit the /etc/hostname file
echo "$new_hostname" | sudo tee /etc/hostname

# Edit the /etc/hosts file
sudo sed -i "s/$old_hostname/$new_hostname/g" /etc/hosts

# Add the IP address and the new hostname to the /etc/hosts file
echo "$ip_address $new_hostname" | sudo tee -a /etc/hosts

# Display a confirmation message
echo "Hostname changed successfully." 
```
Make the script executable: 
```
chmod +x hostname.sh
```
Run the script:
```
./hostname.sh
```
##
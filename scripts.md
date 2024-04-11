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
<br>
<br>

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
<br>
<br>

### Adding a user: 
Become root:
```
sudo -i
```
Create the Script: 
```
nano add_user.sh
```
```
#!/bin/bash
# This is a script to create a user in Ubuntu
# Ask for the username and password
echo -n "Enter the username: "
read username
echo -n "Enter the password: "
read -s password

# Create the user with a home directory and bash as the default shell
useradd -m -d /home/$username -s /bin/bash $username

# Set the password for the user
echo "$password" | passwd --stdin $username

# Add the user to the sudo group
usermod -aG sudo $username

# Disable the sudo password prompt for the user
echo "$username ALL=(ALL) NOPASSWD:ALL" | sudo EDITOR='tee -a' visudo

# Display a confirmation message
echo "User $username created successfully."
```
Make the script executable: 
```
chmod +x add_user.sh
```
Run the script:
```
./add_user.sh
```
##
<br>
<br>

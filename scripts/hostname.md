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
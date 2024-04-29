##
### Make WiFi Faster: <br>
Optimize Internet Connections: <br>
Method 1:
- Press `Windows` + `X` 
- Select `Device manager` 
- Open `Network adapters` right-click `Wireless Adapter` and select `Properties`
- Select `Advance` 
- Search the following under `Properties` and change their correspondent `Values` highest.
  -  Preferred Band: `Highest Band` 
  - Roaming Aggressiveness: `Highest` 
  - Speed & Duplex: `Highest`
  - Throughput Booster: `Enabled` 
  - Transmit Power: `Highest`


Method 2:
- Open `Control Panel` and select `Network and Internet` 
- Click on `Network and Sharing Center` 
- On the left panel click on `Change Adapter Settings` 
- Right-click on your `Internet (Ethernet)` and select `Properties` 
- Click on `Configure` on the popup window and select `Advance` 
  -  Preferred Band: `Highest Band` 
  - Roaming Aggressiveness: `Highest` 
  - Speed & Duplex: `Highest`
  - Throughput Booster: `Enabled` 
  - Transmit Power: `Highest`

##
### Get WiFi Passwords:
Follow these instructions to get any WiFi passwords:
- Open `cmd` or any `Windows Terminal`
- Type the following:
```
netsh wlan show profile
```
- This will list all the available WiFi around
- Now type:
```
netsh wlan show profile [WiFi Name] key=clear
```
- Check `Key Content` under `Security Settings` to see the passwords

##
### Fix WiFi Problems 
If your PC [Laptop] keeps disconnecting from your WiFi, here is how to fix it: <br>  
Method 01: 
- Press `Windows Key` + `R` 
- Type the following: 
```
ncpa.cpl
``` 
- Right-click on your `Internet (Ethernet)` and select `Properties` 
- Click on `Configure` on the popup window and select `Power Management` 
- Unchecked all the boxes then click `OK` 
- Run `cmd` as administrator 
- Type the following commands and ENTER respectfully: 
```
netsh winsock reset 
```
```
netsh int ip reset c:\resetlog.txt
```
- Now restart your PC 


Method 02: 
- Right-click on `Start` then select `Power Options` 
- Click `Additional Power Settings` then select `Change Plan Settings` 
- `Change Advanced Power Settings` 
- On `Wireless Adapter Settings` set `Battery` and `Plugged In`, to `Maximum Performance` 
- Then click `OK` 

##

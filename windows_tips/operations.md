##
### Check whether a PC has SSD or HDD:
- `Windows Key` + `R`
- Type the following and hit `ENTER`
```
dfrgui 
```
##

### Laptop Battery Health: 
- Run `cmd` as `administrator` 
- Type the following and hit `ENTER`
```
powercfg /batteryreport
```
- The battery report will be an `HTML file` 
- Copy and paste the `HTLM file` on a `browser` and hit `ENTER` 

###

### Disable Chrome Popup Ads: 
- Open `Settings` on `Chrome` 
- Go to `Privacy and Security`
- Open `Site Settings`
- Then `Notification` 
##

### Block all Browser Ads: 
- Install and add `uBlock Origin` extension on your preferred browser to block all ads including YouTube 
##

### Unfreeze Frozen PC Screen: 
- Press `Ctrl` + `Shift` + `Windows` + `B` 
##

### Open Emogi: 
- `Windows` + `.`  
- OR `Windows` + `;`
##

### Shutdown PC:
- `Windows` + `X` then `U` and  `U` 
##

### Shutdown Windows Properly: 
- Open `Control Panel` then select `Hardware and Sounds`
- Then open `Power Options` and select `Change what the power buttons do` 
- Click `Change settings that are currently unavailable` 
- Uncheck `Turn on fast startup (recommended)`
- Then click `Save Changes` 
##

### Remove ‘Activate Windows’ Watermark:
Here is how you can remove the Activate Windows watermark from your PC (Laptop): <br>  
Method 01: 
- Run `cmd` as `administrator` 
- Type the following command and hit `ENTER` 
```
bcdedit -set TESTSIGNING OFF
```
- Then `restart` your PC  

Method 02: 
- `Windows` + `R` 
- Type: 
```
regedit 
```
- Select `HKEY_LOCAL_MACHINE` then `SYSTEM` then `Current ControlSet`
- Select `Services` then double click on `svsvc` 
- Right-click on `Start` then select `Modify` 
- Change `Value Data` to `4` 
- Then click `OK` and `restart` your PC
##

### Accessing your Bios: <br> 
Method 01:
- Hold `SHIFT` and `Restart` your PC 

Method 02: 
- Right-click on your `Desktop` then `New` and click `Shortcut` 
- Under `Type the location of the item:` type the following: 
```
Shutdown /r /fw /t 1
``` 
- Click `Next`
- Rename it whatever you want but the default will be `shutdown` - Then click `finish` 
- Right-click on your newly created `shortcut` and click on `Properties` 
- Click on `Shortcut` then click `Advance`
- Check `Run as administrator`
##
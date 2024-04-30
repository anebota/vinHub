##
### Upgrade Windows Software 
- Open `cmd` as `administrator` 
- Type the following command to list software available for upgrade:
```
winget upgrade
``` 
- Type the following command to upgrade the software 
```
winget upgrade --all --include-unknown     
```
## 
### Make your PC faster 
- Open `Control Panel` then `System and Security` and `Security and Maintenance` 
- Go to `Maintenance` and then `Start Maintenance`  
- Wait till it completes the maintenance 

## 
### Make your PC Faster 
- Press `Windows` + `R` 
- Type 
```
sysdm.cpl
```
- Then hit `ENTER`
- On the popup window, click `Advance` then `Settings` under `Performance` 
- Select `Adjust for best performance` 
- Select `Smooth Edges of Screen fonts` 
- Click `Apply` then `Restart your PC` 

##
### Speedup your PC 
- Press `Windows` + `R` 
- Type: 
```
temp
```
- then type:
```
%temp% 
```
- Then type 
```
prefetch 
```
- Hold `Ctrl` + `A` to select all then `delete` 
- This will delete all the proceeding files 
- If it doesn't delete then press skip 

##
### Maximize Processor Usage:  
- Press `Window`s + `R` 
- Type msconfig then hit `ENTER` 
- Under `System Configuration`, select `Boot` 
- Then click `Advance Option` 
- Check `Number of Processors` and choose the `maximum` 
- Do so with `Maximum memory` as well 
- Just click the `Maximum memory` checkbox  
- Click `OK` then `restart` your PC 

##

### Diagnose and Troubleshoot PC Problems:
- Run `cmd` as `administrator` 
- Type the following command and hit `ENTER` 
```
sfc /scannow 
```

To check the Windows Image and repair any corrupted file that might slow your PC:  
- Run `cmd` as `administrator` 
- Type the following command and hit `ENTER` 
```
DISM /online /cleanup-image /checkhealth
```
##

### Increase your GPU: 
- It stands for `Graphics Processing Unit` 
- Another name is `Video Card`
- It helps to boost gaming, display images, and video performance 
Now the steps: 
1) Update drivers: 
- First, update your drivers 
- Go to `Device Manager` and open `Display adapters` 
- Right-click on `Intel(R) UHD Graphics` and `update driver`
2) Check your GPU capacity: 
- Right-click on any space on your desktop and select `Display Settings` 
- Scroll down to `Advance display settings` and select `Display adapter properties for Display 1` 
- Take note of your `Dedicated Video Memory` 
3) Increase the GPU: 
- Hold `Windows` + `R` keys
- Then type 
```
regedit
``` 
- And hit ENTER 
- Open `HKEY_LOCAL_MACHINE` scroll down and open `SOFTWARE` 
- Now right-click on `Intel`, select `New` then `Key` then type `GMM`
- Right-click inside `GMM` select `New` and `DWORD (32-bit) Value` 
- Rename the file to `DedicatedSegmentSize` and hit `ENTER` or right-click and select `Modify` 
- Then input the `Value Data` hit `OK` 
- Now `restart` your laptop  

Her is the `Value Data Guide` 
|RAM     |Value  |
|:-------|:------|
|2GB     |256    |
|4GB     |512    |
|8GB     |1024   |
|16GB    |2048   | 
##
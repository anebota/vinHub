## 
Open PowerShell and run:
```
notepad $profile
```
Or you can test if the $profile path exist:
```
Test-Path $profile
```
If the output is `false`, it means it doesn't exist: <br>
So, create it: 
```
New-Item -Type File -Path $profile -Force
```
##
Now, cd:
```
C:\Users\vintech\Documents\PowerShell
```
Make sure to replace `vintech` with your own username <br>
When on the path, run:
```
notepad Microsoft.PowerShell_profile.ps1
```
Edit your prompts, then `save` <br>
##
Default prompts:
```
PS C:\Users\vintech>
PS: Write-Host ""
 >: return ">"
```
##
`Restart` PowerShell: 

##
Sample Prompts that you can use: 
##
```
function prompt {
    Write-Host "VIN" -NoNewline -ForegroundColor White
    Write-Host (" " + $pwd) -NoNewline -ForegroundColor Green
    return " > "
}
```
```
function prompt {
    Write-Host "😊" -NoNewline -ForegroundColor Yellow
    Write-Host (" " + $pwd) -NoNewline -ForegroundColor Green
    return " > "
}
```
function prompt {
    Write-Host "vin" -NoNewline -ForegroundColor White
    Write-Host (" " + $pwd) -NoNewline -ForegroundColor Green
    return "$ " 
}
```
```
function prompt {
    Write-Host "vin" -NoNewline -ForegroundColor White
    Write-Host (" " + $pwd) -NoNewline -ForegroundColor Green
    return ": " 
}
```
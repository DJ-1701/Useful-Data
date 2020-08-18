# Useful-Data

## PowerShell
Information on comparing multi element file versioning.<br>
https://invoke-thebrain.com/2018/12/comparing-version-numbers-powershell/

Work around for `unable to resolve package source 'https://www.powershellgallery.com/api/v2/'`<br>
https://vanbrenk.blogspot.com/2017/09/install-module-unable-to-resolve.html

Information on trimming strings.<br>
https://devblogs.microsoft.com/scripting/trim-your-strings-with-powershell/

Storage of Objects as files to be used between PowerShell sessions.<br>
https://devblogs.microsoft.com/scripting/learn-how-to-save-powershell-objects-for-offline-analysis/

Running a PowerShell script as a sheduled task.
powershell.exe -ExecutionPolicy Bypass -File C:\Install\Script.ps1 -WindowStyle Hidden
(Where C:\Install\Script.ps1 is the script you wish to run, and -WindowStyle Hidden can be use to hide the window.)

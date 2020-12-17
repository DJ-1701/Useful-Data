# Useful-Data

## PowerShell
Information on comparing multi element file versioning.<br>
https://invoke-thebrain.com/2018/12/comparing-version-numbers-powershell/

Work around for:<br>`unable to resolve package source 'https://www.powershellgallery.com/api/v2/'`<br>and<br>`WARNING: Unable to download from URI 'https://go.microsoft.com/fwlink/?LinkID=627338&clcid=0x409' to ''. WARNING: Unable to download the list of available providers. Check your internet connection.`<br>
https://vanbrenk.blogspot.com/2017/09/install-module-unable-to-resolve.html

Information on trimming strings.<br>
https://devblogs.microsoft.com/scripting/trim-your-strings-with-powershell/

Storage of Objects as files to be used between PowerShell sessions.<br>
https://devblogs.microsoft.com/scripting/learn-how-to-save-powershell-objects-for-offline-analysis/

Running a PowerShell script as a sheduled task.<br>
`powershell.exe -ExecutionPolicy Bypass -File C:\Install\Script.ps1 -WindowStyle Hidden`<br>
(Where `C:\Install\Script.ps1` is the script you wish to run, and -WindowStyle Hidden can be use to hide the window.)

Connect to 365 powershell services.<br>
`$domainHost="Company Part of company.onmicrosoft.com Here!!!!"`<br>
`$credential = Get-Credential`<br>
`Connect-MsolService -Credential $credential`<br>
`Import-Module Microsoft.Online.SharePoint.PowerShell -DisableNameChecking`<br>
`Connect-SPOService -Url https://$domainHost-admin.sharepoint.com -credential $credential`<br>
`Import-Module SkypeOnlineConnector`<br>
`$sfboSession = New-CsOnlineSession -Credential $credential`<br>
`Import-PSSession $sfboSession`<br>
`$exchangeSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $credential -Authentication "Basic" -AllowRedirection`<br>
`Import-PSSession $exchangeSession`<br>
`$SccSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid/ -Credential $credential -Authentication "Basic" -AllowRedirection`<br>
`Import-PSSession $SccSession -Prefix cc`<br>

Ensure that non-AD synced account does not prompt for password change<br>
`Set-MsolUser -UserPrincipalName user@comapny.onmicrosoft.com -PasswordNeverExpires $true`

Change login credentials after renaming AD account<br>
`Set-MsolUserPrincipalName -UserPrincipalName olduser@company.onmicrosoft.com -NewUserPrincipalName newuser@domain.com`

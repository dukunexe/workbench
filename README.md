# workbench
Script to install various pentesting/red team tools on a Windows VM. Heavily copied from [RTOVMSetup](https://github.com/ZeroPointSecurity/RTOVMSetup) by ZeroPointSecurity with some different tools and new UI settings.

Create a new Windows 10 virtual machine (Recommended specs: 60GB storage, 4GB memory, 2 vCPU) then run the following command in an elevated PowerShell prompt. Takes 20-30 minutes.
```
Set-ExecutionPolicy Unrestricted -Force; . { Invoke-WebRequest -useb https://boxstarter.org/bootstrapper.ps1 } | iex; Get-Boxstarter -Force; $Cred = Get-Credential $env:USERNAME; Install-BoxstarterPackage -PackageName https://raw.githubusercontent.com/kyleavery/workbench/master/workbench.choco -Credential $Cred
```

Install all 4 files from downloads. Select the .NET and C++ Desktop Development Environments from the main menu and Windows XP v141 tools from the components menu.

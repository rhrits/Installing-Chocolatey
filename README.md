# Installing-Chocolatey

### Check Current Execution Policy

To check the current execution policy, run the following command in PowerShell in Administrator mode:

- ``Get-ExecutionPolicy``

 If the command returns Restricted, you can change the execution policy to either AllSigned or Bypass for the current process. Use one of the following commands:

Change Execution Policy to AllSigned

- ```Set-ExecutionPolicy AllSigned```

Change Execution Policy to Bypass for the Current Process

- ```Set-ExecutionPolicy Bypass -Scope Process```

Make sure you have the necessary administrative privileges to change the execution policy.

Then paste this below code in powershell 

- ```Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))```

- Ignore the warning message while installation
- After installation type ```choco``` or ```choco -``` to check either it is installed or not.

If not working then copy the code from documentation page of Chocolatey website
https://chocolatey.org/install

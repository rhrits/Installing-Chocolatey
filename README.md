# Chocolatey
Chocolatey is a package manager for Windows that provides a centralized repository of software packages. It simplifies the process of installing, updating, and managing software on Windows machines through a command-line interface (CLI). Here’s a comprehensive overview of Chocolatey and its key features:

Key Features:

- Package Management: Chocolatey allows users to search, install, update, and uninstall software packages from a curated repository called the Chocolatey Community Repository (formerly known as the Chocolatey Gallery). This repository contains a wide range of popular software applications, utilities, and tools.

- Command-line Interface (CLI):  Users interact with Chocolatey primarily through the command line, making it efficient for scripting and automation tasks. The CLI supports commands for searching packages, installing multiple packages in one command, upgrading packages, and more.

- Automation and Scripting:  Chocolatey is designed with automation in mind, enabling administrators and developers to automate software installation and management tasks. This is particularly useful for configuring new machines or deploying software across multiple systems.

- Versioning and Dependencies:  Chocolatey manages software versions and dependencies automatically. When installing a package, Chocolatey resolves and installs any dependencies required by the software, ensuring compatibility and stability.

- Community Edition:  Free and open-source, it provides access to the Chocolatey Community Repository and basic package management features.
     - Chocolatey for Business (C4B): Includes additional features such as package internalization, package audit and reporting, and more granular management capabilities suitable for enterprise environments.

     - Package Creation and Hosting: Users can create their own packages using Chocolatey’s packaging framework. Packages can be hosted on public or private repositories, allowing organizations to manage internal software distributions.

- Security and Trust:  Chocolatey emphasizes security by digitally signing packages in the official repository. This helps ensure that packages have not been tampered with and provides a level of trust in the software being installed.

## Installing-Chocolatey

### Check Current Execution Policy

To check the current execution policy, run the following command in PowerShell in Administrator mode:

- ```
  Get-ExecutionPolicy
  ```

 If the command returns Restricted, you can change the execution policy to either AllSigned or Bypass for the current process. Use one of the following commands:

Change Execution Policy to AllSigned

- ```
  Set-ExecutionPolicy AllSigned
  ```
  
Make sure you give permissions by typing yes while installations.

Change Execution Policy to Bypass for the Current Process

- ```
  Set-ExecutionPolicy Bypass -Scope Process
  ```

Make sure you have the necessary administrative privileges to change the execution policy.

Then paste this below code in powershell 

- ```
  Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
  ```

- Ignore the warning message while installation
- After installation type ```choco``` or ```choco -``` to check either it is installed or not.

If not working then copy the code from documentation page of Chocolatey website
https://chocolatey.org/install



# Chocolatey commands to install various common software and packages

Each command is executed in an elevated (administrative) PowerShell window.

### Basic Software Installations

1. **Google Chrome**:
   ```powershell
   choco install googlechrome -y
   ```

2. **Mozilla Firefox**:
   ```powershell
   choco install firefox -y
   ```

3. **Visual Studio Code**:
   ```powershell
   choco install vscode -y
   ```

4. **7-Zip**:
   ```powershell
   choco install 7zip -y
   ```

5. **Git**:
   ```powershell
   choco install git -y
   ```

6. **Node.js (with npm)**:
   ```powershell
   choco install nodejs -y
   ```

7. **Python 3**:
   ```powershell
   choco install python -y
   ```

8. **Java Development Kit (JDK)**:
   ```powershell
   choco install jdk8 -y
   ```

9. **Docker**:
   ```powershell
   choco install docker-desktop -y
   ```

10. **Slack**:
    ```powershell
    choco install slack -y
    ```

11. **Zoom**:
    ```powershell
    choco install zoom -y
    ```

12. **VLC Media Player**:
    ```powershell
    choco install vlc -y
    ```

13. **Notepad++**:
    ```powershell
    choco install notepadplusplus -y
    ```

14. **WinRAR**:
    ```powershell
    choco install winrar -y
    ```

15. **Skype**:
    ```powershell
    choco install skype -y
    ```

### Development Tools

1. **Postman**:
   ```powershell
   choco install postman -y
   ```

2. **MySQL**:
   ```powershell
   choco install mysql -y
   ```

3. **MongoDB**:
   ```powershell
   choco install mongodb -y
   ```

4. **Redis**:
   ```powershell
   choco install redis-64 -y
   ```

5. **Visual Studio 2019 Community**:
   ```powershell
   choco install visualstudio2019community -y
   ```

6. **.NET Core SDK**:
   ```powershell
   choco install dotnetcore-sdk -y
   ```

7. **IntelliJ IDEA Community Edition**:
   ```powershell
   choco install intellijidea-community -y
   ```

8. **PyCharm Community Edition**:
   ```powershell
   choco install pycharm-community -y
   ```

### Utilities

1. **Sysinternals Suite**:
   ```powershell
   choco install sysinternals -y
   ```

2. **CCleaner**:
   ```powershell
   choco install ccleaner -y
   ```

3. **PuTTY**:
   ```powershell
   choco install putty -y
   ```

4. **FileZilla**:
   ```powershell
   choco install filezilla -y
   ```

5. **WinSCP**:
   ```powershell
   choco install winscp -y
   ```

6. **ConEmu**:
   ```powershell
   choco install conemu -y
   ```

7. **OpenSSH**:
   ```powershell
   choco install openssh -y
   ```

### Productivity Software

1. **LibreOffice**:
   ```powershell
   choco install libreoffice-fresh -y
   ```

2. **Adobe Acrobat Reader DC**:
   ```powershell
   choco install adobereader -y
   ```

3. **Evernote**:
   ```powershell
   choco install evernote -y
   ```

4. **Microsoft Office 365 Business**:
   ```powershell
   choco install office365business -y
   ```

5. **OneNote**:
   ```powershell
   choco install onenote -y
   ```

### Communication Tools

1. **Microsoft Teams**:
   ```powershell
   choco install microsoft-teams -y
   ```

2. **Discord**:
   ```powershell
   choco install discord -y
   ```

3. **Telegram**:
   ```powershell
   choco install telegram -y
   ```

You can find more packages and their respective installation commands on the [Chocolatey website](https://community.chocolatey.org/packages). 
Always ensure you are using an elevated PowerShell window to install these packages using Chocolatey.

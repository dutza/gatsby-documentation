# Gatsby installation guide for windows
Documentation about Gatsby framework including tips and tricks 

1. [Official documentation from gatsbyjs.com](https://www.gatsbyjs.com/docs/tutorial/part-0/#installation-guide) 
2. [Microsoft documentation](https://docs.microsoft.com/en-us/windows/dev-environment/javascript/gatsby-on-wsl) 
  * Prerequisites:<br/>
    2.1 Install the latest version of Windows 10 (Version 1903+, Build 18362+) or Windows 11<br/>
    To find the version run `winver`
    Start > run > winver
  
    2.2 Install Windows Subsystem for Linux (WSL 2)
    ```powershell
    dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
    dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
    ```
      > **Note**
      >Expected response:</br>
      enabling feature(s)
      [==========================100.0%==========================]
      The operation completed successfully.
      PS C:\Windows\system32> dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestar

      >Enabling feature(s)
      >[==========================100.0%==========================]
      >The operation completed successfully.
    
> **Warning**
> Please reboot to update windows with WSL
    
Download and install WSL 2 kernel: [aka.ms/wsl2kernel](aka.ms/wsl2kernel)<br/>
[WSL2 Linux kernel update package for x64 machines](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)
    
```powershell as adiministrator
wsl --set-default-version 2 # set WSL 2 default
#install Ubuntu from Microsoft store
wsl -l #check available distro
wsl -l -v #WSL version:
```

> **note**
> expected response
> PS C:\Windows\system32> wsl -l -v <br/>
>  NAME            STATE           VERSION<br/>
> Ubuntu-22.04    Stopped         2

[Install Windows Terminal using the Microsoft Store](https://docs.microsoft.com/en-us/windows/dev-environment/javascript/nodejs-on-wsl#:~:text=Install%20Windows%20Terminal%20using%20the%20Microsoft%20Store) (optional)<br/>
[Install Visual Studio Code](https://code.visualstudio.com/docs/?dv=win)<br/>
[Visual Studio Code Remote Development Extension Pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)

Start and update ubuntu:
```bash
sudo apt update && sudo apt upgrade -y
```

[Install Node.js on WSL 2](https://docs.microsoft.com/en-us/windows/dev-environment/javascript/nodejs-on-wsl)
```bash
sudo apt-get install curl #install curl
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash #install NVM #close and reopen the terminal to list
nvm ls
mkdir GatsbyProjects #create project folder 
cd GatsbyProjects/ #open project folder
nvm install --lts #Install the current stable LTS release of Node.js
nvm install node #Install the current release of Node.js 
npm install -g gatsby-cli #isntall gatsby
gatsby new my-gatsby-app #Create your Gatsby.js project
cd my-gatsby-app
gatsby develop
code . #start VS Code using current location 
```



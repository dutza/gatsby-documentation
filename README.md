# Gatsby installation guide for windows
Documentation about Gatsby framework including tips and tricks 

1. [Official documentation from gatsbyjs.com](https://www.gatsbyjs.com/docs/tutorial/part-0/#installation-guide) 
2. [Microsoft documentation](gatsbyjs.com) 
  * Prerequisites:<br/>
    2.1 Install the latest version of Windows 10 (Version 1903+, Build 18362+) or Windows 11<br/>
    To find the version run `winver`
    Start > run > winver
  
    2.2 Install Windows Subsystem for Linux (WSL 2)
    ```powershell
    dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
    dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
    ```
    > [!TIP]
    > Please reboot to update windows with WSL
    
      > [!NOTE]
      >Expected response:</br>
      enabling feature(s)
      [==========================100.0%==========================]
      The operation completed successfully.
      PS C:\Windows\system32> dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

      >Deployment Image Servicing and Management tool
      >Version: 10.0.19041.572

      >Image Version: 10.0.19042.685

      >Enabling feature(s)
      >[==========================100.0%==========================]
      >The operation completed successfully.
    
      Download and install WSL 2 kernel: [aka.ms/wsl2kernel](aka.ms/wsl2kernel)
      [WSL2 Linux kernel update package for x64 machines](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)
    
    
    check WSL version:
     ```powershell
     wsl -l -v
     ```
  


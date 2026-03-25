---
title: "Step-by-Step Guide to Installing Docker on Windows"
seoTitle: "Install Docker on Windows: A Step-by-Step Guide"
seoDescription: "Learn how to install Docker on Windows, set up WSL 2, and configure Docker Desktop for optimal performance with this step-by-step guide"
datePublished: 2025-02-03T19:55:54.750Z
cuid: cm6ph0wzi000i08jv9pxp6asv
slug: step-by-step-guide-to-installing-docker-on-windows
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1738612362403/80aa342c-2f25-4d3a-8285-c26f10fc39d3.webp
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1738612528571/8b7c2467-a5bd-407d-bd69-956429d60e30.webp
tags: linux, docker, windows, containers, installation, dockerfile, docker-compose, steps, docker-images

---


## Download and Install Docker

To begin the Docker installation process on Windows:

1. [Visit the official Docker website and download Docker Desktop](https://docs.docker.com/desktop/setup/install/windows-install/) for your specific system architecture (AMD64 or ARM64).
    - To find out, open Settings > System > About
    ![Windows System](https://cdn.hashnode.com/res/hashnode/image/upload/v1738580282797/8018333b-f938-4a42-b2c9-ad40cd7cea4c.png?auto=compress,format&format=webp)
2. Run the installer and follow the setup process:
   - Accept the license agreement.
   - Select the WSL 2 backend option during installation.
3. Restart your system if prompted.

### Minimum Requirements:
- 64-bit processor (AMD64 or ARM64)
- At least 4GB of RAM
- 64-bit version of Windows 10 (Build 1903 or higher) or Windows 11
- Hardware virtualization enabled in BIOS/UEFI settings

### Verify Installation:
- Open a terminal and run `docker --version` to check the Docker version.
- Test functionality by running: `docker run hello-world`.

---

## Set Up WSL 2

To set up Windows Subsystem for Linux 2 (WSL 2):

1. Open PowerShell as an administrator.
2. Run the command: `wsl --install`.
3. Restart your computer if prompted.

### Verify WSL Installation:
- Run `wsl --list --verbose` in PowerShell to check installed distributions and versions.
- If needed, set WSL 2 as the default version using: `wsl --set-default-version 2`.

---

## Configure Docker Settings

After installing Docker Desktop, configure its settings for optimal performance:

1. Open Docker Desktop and go to the **Settings** menu.
2. Navigate to **Resources** to adjust CPU, memory, and disk space allocation.
3. In **WSL Integration**, enable Docker integration with your installed WSL Linux distributions (e.g., Ubuntu).

### Advanced Configuration:
To limit resource usage, create a `.wslconfig` file in your user directory (`C:\Users\YourUsername`) with the following settings:

```
memory=4GB # Limits memory usage to 4GB
processors=2 # Limits to 2 virtual processors
swap=8GB # Sets swap space to 8GB
pageReporting=false # Retains allocated memory
localhostforwarding=true # Enables localhost forwarding from WSL to Windows
```

Ps. If you want to be more specific about resource limitations, use these commands, but _be aware_ of what you really want:

```
# Settings apply across all Linux distros running on WSL 2
[wsl2]

# Limits VM memory to use no more than 4 GB, this can be set as whole numbers using GB or MB
memory=4GB

# Sets the VM to use two virtual processors
processors=2

# Specify a custom Linux kernel to use with your installed distros. The default kernel used can be found at https://github.com/microsoft/WSL2-Linux-Kernel
kernel=C:\\temp\\myCustomKernel

# Sets additional kernel parameters, in this case enabling older Linux base images such as Centos 6
kernelCommandLine = vsyscall=emulate

# Sets amount of swap storage space to 8GB, default is 25% of available RAM
swap=8GB

# Sets swapfile path location, default is %USERPROFILE%\AppData\Local\Temp\swap.vhdx
swapfile=C:\\temp\\wsl-swap.vhdx

# Disable page reporting so WSL retains all allocated memory claimed from Windows and releases none back when free
pageReporting=false

# Turn off default connection to bind WSL 2 localhost to Windows localhost
localhostforwarding=true

# Disables nested virtualization
nestedVirtualization=false

# Turns on output console showing contents of dmesg when opening a WSL 2 distro for debugging
debugConsole=true
```

Restart Docker Desktop after making changes for them to take effect.

### Configure WSL Integration

Go to the Docker settings, select `Resources > WSL Integration` and enable the version of Ubuntu you have installed.  
 
### DOCKER DESKTOP READY FOR USE! 

![Windows System](https://miro.medium.com/v2/resize:fit:4800/format:webp/1*yBpOEUWy5TX-5V8wRLA7lg.png)


---

## Troubleshooting and Best Practices

### Common Issues and Fixes:
- **Error when pulling containers:** Disable "Add the *.docker.internal names to the host's /etc/hosts file (Requires password)" in settings.
- **Performance issues:** Use the WSL 2-based engine instead of Hyper-V backend.

### Best Practices:
- Keep "Enable background SBOM indexing" enabled for optimized image inspections.
- Regularly update Docker Desktop for new features and security fixes.
- If persistent issues occur, check Docker Desktop logs or reinstall WSL 2 for compatibility resolution.

---

![Windows System](https://miro.medium.com/v2/resize:fit:720/format:webp/1*CBciBUxXM-EAw5BTxc9vjg.png)

## Bonus Tips
- **Troubleshooting:** If you encounter issues, check the Docker Desktop Logs in the application or reinstall WSL 2.
- **Updates:** Keep Docker Desktop updated for the latest features and fixes.
- **Documentation:** Visit the official Docker documentation for advanced use cases.

## Enjoy building and deploying containerized applications efficiently on your Windows machine! 🐋



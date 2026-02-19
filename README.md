# Ubuntu WSL Installation and Uninstallation Guide

This guide provides step-by-step instructions to install and uninstall Ubuntu on Windows Subsystem for Linux (WSL).

## Prerequisites

- Windows 10 version 2004 and higher (Build 19041 and higher) or Windows 11.
- WSL 2 enabled on your machine.

### Enabling WSL

If WSL is not already enabled, follow these steps to enable it:

1. Open PowerShell as Administrator and run:
 
```bash
wsl --install
```

This command will install the WSL feature, set WSL 2 as the default, and install a Linux distribution (Ubuntu by default).

2. Restart your computer if prompted.

---

## Installation: Ubuntu on WSL

### Step 1: Install Ubuntu

1. Open the **Microsoft Store** and search for "Ubuntu".
2. Select the version you want to install (e.g., **Ubuntu 20.04 LTS** or **Ubuntu 22.04 LTS**).
3. Click **Get** to install the application.

### Step 2: Set up Ubuntu

1. Once the installation is complete, launch Ubuntu from the Start menu or by typing `ubuntu` in the command prompt.
2. Follow the on-screen instructions to create a new user and set a password for your Ubuntu environment.

### Step 3: Verify Installation

To verify that Ubuntu is installed correctly, open a terminal and run:
```bash
wsl --list --verbose
```
This will list all installed distributions along with their WSL versions.

---

## Uninstallation: Ubuntu on WSL

### Step 1: Unregister Ubuntu

1. Open **PowerShell** as Administrator.
2. Run the following command to list all installed distributions:
   ```bash
   wsl --list
   ```
   Locate the name of the Ubuntu distribution you want to uninstall (e.g., `Ubuntu-20.04`).

3. Run this command to unregister (uninstall) the Ubuntu distribution:
   ```bash
   wsl --unregister <distro_name>
   ```
   Replace `<distro_name>` with the exact name of the distribution (e.g., `Ubuntu-20.04`). This will remove the Ubuntu installation, along with all its files and configurations.

### Step 2: Remove the Ubuntu App (Optional)

1. Open **Settings** in Windows.
2. Go to **Apps > Installed Apps**.
3. Scroll down, find the Ubuntu app, click on it, and then select **Uninstall**.

---

## Additional Information

- To update WSL to the latest version, you can run:
  ```bash
  wsl --update
  ```
- To set WSL 2 as the default version (if it isn't already), run:
  ```bash
  wsl --set-default-version 2
  ```

## Installation: Ubuntu on WSL

### Step 1: Install Ubuntu via Command Line

1. Open PowerShell or Command Prompt as Administrator and run:
   ```bash
   wsl --install -d Ubuntu
   ```
   This will install Ubuntu with WSL 2.

2. Once installed, set it up by running:
   ```bash
   ubuntu
   ```

This will install and configure Ubuntu on your WSL environment.

For further details, refer to the official [WSL documentation](https://docs.microsoft.com/en-us/windows/wsl/).

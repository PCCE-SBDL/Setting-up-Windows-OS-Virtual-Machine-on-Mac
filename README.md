# Setting Up a Windows OS Virtual Machine on macOS

This guide walks you through installing VMware Fusion on macOS and configuring VMware Tools for Windows ARM (Apple Silicon).

## Table of Contents
1. [Part 1: Install VMware Fusion on macOS](#part-1-install-vmware-fusion-on-macos)
2. [Part 2: Install VMware Tools (Windows ARM)](#part-2-install-vmware-tools-windows-arm)
3. [Quick Verification](#quick-verification)

---

## Part 1: Install VMware Fusion on macOS
VMware Fusion is now **free for personal use**.

### 1. Register & Download
* **Broadcom Support Portal:** Go to the [Broadcom Support Portal](https://support.broadcom.com/) and register for a free account.
* **Download:** Navigate to the VMware Fusion downloads page and select the version labeled **"for Personal Use"**.

### 2. Run the Installer
* Open the downloaded `.dmg` file and double-click the **VMware Fusion** icon.
* Click **Open** on the security warning and enter your Mac administrator password.

### 3. Grant Permissions
* Follow the prompts to enable **Accessibility** features in your Mac's `System Settings > Privacy & Security`.

### 4. Select License
* When prompted for a key, choose **"I want to license VMware Fusion for Personal Use"** to use it for free.

---

## Part 2: Install VMware Tools (Windows ARM)
On Apple Silicon (M1/M2/M3), **VMware Tools** primarily installs essential drivers for network and graphics, enabling features like copy-pasting and window resizing.

### 1. Mount the Tools
1. Start your Windows VM and log in.
2. In the Mac top menu bar, go to **Virtual Machine** > **Install VMware Tools**.

### 2. Open the Virtual Disc
1. Inside Windows, open **File Explorer** and go to **This PC**.
2. Double-click the **DVD Drive (D:) VMware Tools**.

### 3. Run the Installation Script
1. Look for a file named `setup.exe` or a PowerShell script named `Setup.ps1`.
2. **Right-click** `Setup.ps1` and select **Run with PowerShell**.
3. If prompted by *User Account Control*, click **Yes**.

### 4. Finalize
* Follow the on-screen installer prompts (choosing a **"Complete"** installation is usually best).
* **Restart** the Windows VM when the installation finishes.

---

## Quick Verification
Once the VM reboots, you can verify the setup:

* **Clipboard:** Copy a small text file on your Mac and paste it onto the Windows desktop.
* **Display:** Resize the VMware window; Windows should automatically adjust its resolution to fit.

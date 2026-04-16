# Ubuntu Installation Guide for VMware Workstation

Creating an Ubuntu virtual machine (VM) in VMware Workstation involves two main phases: configuring the virtual hardware and installing the operating system.

## Prerequisites
*   **Ubuntu ISO Image**: Download the latest **LTS (Long Term Support)** version of Ubuntu Desktop from the [official Ubuntu Desktop website](https://ubuntu.com) and for Ubuntu Server[official Ubuntu Server website](https://ubuntu.com/download/server)
*   **VMware Workstation**: Ensure you have VMware Workstation Pro or Player installed on your host machine.

---

## Phase 1: Create the Virtual Machine
1.  **Launch the Wizard**: Open VMware Workstation and click **"Create a New Virtual Machine"** or press `Ctrl+N`.
2.  **Configuration Type**: Choose **Typical (recommended)** and click **Next**.
3.  **Installer Source**: Select **"Installer disc image file (iso)"**, click **Browse**, and select your downloaded Ubuntu ISO file.
    *   *Note*: If VMware detects the ISO, it may offer "Easy Install." You can proceed with this or select "I will install the operating system later" for more control.
4.  **Guest OS Selection**: Select **Linux** as the Guest Operating System and **Ubuntu 64-bit** as the version.
5.  **Name and Location**: Provide a name for your VM (e.g., "Ubuntu 24.04") and choose a folder to store the VM files.
6.  **Disk Capacity**: Specify the maximum disk size. 
    *   **Recommended**: At least **64 GB to 100 GB** for general use.
    *   Select **"Split virtual disk into multiple files"** for easier moving of VM files later.
7.  **Customize Hardware**: Before finishing, click **Customize Hardware** to adjust performance:
    *   **Memory (RAM)**: At least **4 GB**, but **8 GB** is recommended.
    *   **Processors**: Allocate at least **2 cores** (4 cores recommended).
    *   **Network**: Ensure **NAT** (default) or **Bridged** is selected.

---

## Phase 2: Install Ubuntu
1.  **Power On**: Select your new VM and click **"Play virtual machine"**.
2.  **Boot Menu**: Select **"Try or Install Ubuntu"** and press **Enter**.
3.  **Language and Keyboard**: Select your preferred language and keyboard layout.
4.  **Installation Type**:
    *   Choose **"Normal installation"** and check **"Install third-party software for graphics and Wi-Fi"**.
    *   On the next screen, select **"Erase disk and install Ubuntu"**. (This only affects your virtual disk).
5.  **User Account**: Enter your name, computer name, username, and a strong password.
6.  **Finish**: Wait for the installation to complete, then click **"Restart Now"**.
7.  **Final Step**: When prompted, press **Enter** to "remove" the installation media. Once restarted, log in.

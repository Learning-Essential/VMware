
# Ubuntu Post-Install & VMware Tools Script

* This bash script updates your Ubuntu system and installs Open VM Tools, which is the recommended method for modern Linux distributions on VMware. 

* You can save this as setup-vm.sh in your /Scripts folder.

```
#!/bin/bash

# =================================================================
# Ubuntu Post-Install & VMware Tools Automation Script
# =================================================================

echo "🚀 Starting Ubuntu post-install optimization..."

# 1. Update and Upgrade System
echo "🔄 Checking for system updates..."
sudo apt update && sudo apt upgrade -y

# 2. Install Open VM Tools
# Installs desktop version if GUI is detected, otherwise installs server version
echo "🛠️ Installing Open VM Tools..."
if dpkg -l | grep -q "ubuntu-desktop"; then
    sudo apt install -y open-vm-tools-desktop
else
    sudo apt install -y open-vm-tools
fi

# 3. Install Common Development Tools
echo "📦 Installing build-essential, git, and curl..."
sudo apt install -y build-essential git curl

# 4. Clean up


echo "🧹 Cleaning up unnecessary packages..."
sudo apt autoremove -y

echo "✅ Optimization complete!"
echo "💡 Recommendation: Reboot your VM to apply changes."

```

## How to use it:

  *  Create the file with your favourites editor, nano or vi, here we use : vi setup-vm.sh (then paste the code and save).
  *  Make it executable: chmod +x setup-vm.sh.
  *  Run it: ./setup-vm.sh.
    
## Why use Open VM Tools?
VMware recommends using Open VM Tools (open-vm-tools) instead of the older "Install VMware Tools" menu option for Linux guests. It is easier to maintain through standard Ubuntu updates and provides:

* Smooth mouse movement between host and guest.
* Automatic screen resizing to match your VMware window.
* Shared clipboard and drag-and-drop support.

### That It's.........

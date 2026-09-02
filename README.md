# 🐧 Linux ISO Files

> Linux distribution ISO files with installation guides, system requirements, and verification checksums.

---

## 📋 Overview

This repository contains ISO files for various Linux distributions along with installation guides and verification instructions.

**Distributions Included:**
- Ubuntu (Desktop & Server)
- Fedora
- Debian
- Linux Mint
- Kali Linux

---

## 🚀 System Requirements

| Distribution | Minimum RAM | Minimum Storage | Recommended CPU |
| :--- | :--- | :--- | :--- |
| **Ubuntu Desktop** | 4 GB | 25 GB | 2 GHz dual-core |
| **Ubuntu Server** | 1 GB | 10 GB | 1 GHz |
| **Fedora** | 4 GB | 20 GB | 2 GHz dual-core |
| **Debian** | 2 GB | 10 GB | 1 GHz |
| **Linux Mint** | 4 GB | 20 GB | 2 GHz |
| **Kali Linux** | 4 GB | 20 GB | 2 GHz |

---

## 🔍 ISO Verification (Checksums)

### Why Verify?

Verifying checksums ensures:
- The ISO file is **not corrupted**
- The file has **not been tampered** with
- The download is **complete**

### How to Verify

#### Windows (PowerShell)
```powershell
Get-FileHash -Algorithm SHA256 filename.iso
Linux / macOS
bash
sha256sum filename.iso
💿 How to Create Bootable USB
Option 1: Rufus (Windows)
Download Rufus from https://rufus.ie/

Insert USB drive

Select the ISO file

Click "Start"

Option 2: Etcher (Windows / Linux / macOS)
Download Etcher from https://www.balena.io/etcher/

Select ISO file

Select USB drive

Click "Flash"

Option 3: DD Command (Linux)
bash
sudo dd if=filename.iso of=/dev/sdX bs=4M status=progress
⚠️ Warning: Replace /dev/sdX with your actual USB device name.

📥 Official Download Sources
Distribution	Official Website
Ubuntu	https://ubuntu.com/download
Fedora	https://getfedora.org/
Debian	https://www.debian.org/distrib/
Linux Mint	https://linuxmint.com/download.php
Kali Linux	https://www.kali.org/get-kali/
💻 Installation Steps (Ubuntu Example)
Step 1: Boot from USB
Restart your computer

Press F12 / F2 / ESC / DEL (depending on motherboard)

Select the USB drive as boot device

Step 2: Choose Installation Type
Erase disk and install Ubuntu (Single OS)

Install Ubuntu alongside Windows (Dual Boot)

Something else (Manual partitioning)

Step 3: Partitioning (Dual Boot)
Partition	Size	Type	Mount Point
/boot	500 MB	Ext4	/boot
/ (root)	20 GB+	Ext4	/
/home	Remaining	Ext4	/home
swap	RAM size	Swap	—
Step 4: Create User Account
Enter your name

Create username and password

Step 5: Complete Installation
Wait for installation to complete

Restart when prompted

Remove USB drive

🔧 Post-Installation Commands
Update System
bash
# Ubuntu / Debian
sudo apt update && sudo apt upgrade -y

# Fedora
sudo dnf update -y
Install Essential Software
bash
# Git
sudo apt install git -y

# VS Code
sudo snap install code --classic

# Google Chrome
wget -q -O - https://dl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
sudo sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google-chrome.list'
sudo apt update && sudo apt install google-chrome-stable -y
Install Development Tools
bash
# Build essential (C/C++)
sudo apt install build-essential -y

# Python
sudo apt install python3 python3-pip -y

# Node.js
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt install nodejs -y
🛠️ Common Troubleshooting
Boot from USB Not Working
Disable Secure Boot in BIOS

Disable Fast Boot in BIOS

Try a different USB port

Windows Not Showing in GRUB (Dual Boot)
bash
sudo update-grub
Wi-Fi Not Working
bash
sudo apt install firmware-b43-installer
Screen Resolution Issues
bash
sudo ubuntu-drivers autoinstall
sudo reboot
📊 Linux Distributions Comparison
Distribution	Best For	Difficulty	Package Manager
Ubuntu	Beginners, General Use	Easy	apt
Linux Mint	Windows Migrants	Easy	apt
Fedora	Developers, Latest Features	Medium	dnf
Debian	Stability, Servers	Medium	apt
Kali Linux	Security Testing	Hard	apt
🔗 Useful Resources
Official Ubuntu Documentation

Linux Journey - Interactive Learning

Arch Wiki

👩‍💻 Author
Iqra Maqsood Mughal
Software Engineer | Full-Stack Developer | Code Craftsman | Android App Developer | Problem Solver 🚀

js
const 💻 = "Code is life";
while (true) { learn(); build(); innovate(); }
📅 Date
September 2, 2026

📄 License
This repository is intended for educational and personal study purposes.

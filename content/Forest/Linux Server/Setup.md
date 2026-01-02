# 🖥️ Linux Server + Global SSH Access (University-Friendly, Free)

## Goal
Turn an old PC into a Linux server and **SSH into it from anywhere in the world**, even on **university Wi-Fi**, **without port forwarding**, **without paying**, and **without touching routers**.

---

## 🧰 Requirements

### Hardware
- Old PC (this will become the server)
- Laptop (used only to create the installer)
- **USB flash drive (8 GB or larger)**

### Accounts
- A **Google, GitHub, or email account** (for Tailscale login)

---

## 🧠 Why a USB Is Required
A computer **cannot overwrite its own operating system while running it**.  
The USB acts as **temporary bootable media** so Linux can be installed cleanly.

---

## PART 1 — Create the Linux Installer (on your laptop)

### Step 1: Download Linux Mint XFCE
Download **Linux Mint 22.1 XFCE (64-bit)** from the official website.

**Why XFCE?**
- Very lightweight
- Ideal for old hardware
- Stable and beginner-friendly
- Perfect for servers that don’t need fancy visuals

---

### Step 2: Install Balena Etcher
Balena Etcher safely writes OS images to USB drives.

- Install it on your laptop
- Works on Windows, macOS, and Linux

---

### Step 3: Flash Linux to the USB
1. Insert the USB flash drive
2. Open **Balena Etcher**
3. Select:
   - **Flash from file** → Linux Mint ISO
   - **Select target** → USB drive
4. Click **Flash**

⚠️ This erases the USB completely (expected).

---

## PART 2 — Install Linux on the Old PC

### Step 4: Boot from the USB
1. Insert USB into the old PC
2. Power it on
3. Immediately press one of:
   - `F12`, `ESC`, `F2`, or `DEL`
4. Select the USB device from the boot menu

---

### Step 5: Install Linux Mint
When the desktop loads:
1. Click **Install Linux Mint**
2. Choose language and keyboard
3. When asked about installation type:
   - ✅ **Erase disk and install Linux Mint**
4. Confirm warnings
5. Create:
   - Username
   - Password
6. Finish installation and reboot
7. Remove USB when prompted

🧹 **Result:** Windows is completely removed. All bloat is gone.

---

## PART 3 — First-Time System Setup

Open the **Terminal** on the Linux PC.

### Step 6: Update the system
```bash
sudo apt update && sudo apt upgrade -y


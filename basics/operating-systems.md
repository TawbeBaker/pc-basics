# 🧭 Operating Systems 101

## 🧾 What is an Operating System?
An **Operating System (OS)** is the core software that manages your computer’s **hardware resources** (CPU, memory, storage, devices) and provides **services** that apps use to run safely and reliably.
The OS is also the **graphical user interface (GUI)** you have. All the features like the task bar, the desktop and even the little shutdown button are part of the operating system.

Without an OS, every app would have to control the hardware directly — risky, inefficient, and nearly impossible to maintain. The OS abstracts messy hardware details and exposes clean, stable **APIs**.


- Examples (desktop/laptop): **Windows**, **Linux**, **macOS**
- Examples (mobile/embedded): **Android**, **iOS**, routers, smart TVs
- Two big parts conceptually:
  - **Kernel** (low-level core): schedules work on the CPU, manages memory, talks to devices/drivers
  - **User space**: everything else you see and run (apps, shells, services)


---

## 🪟 Windows vs 🐧 Linux vs 🍎 macOS (high-level)

| Topic | Windows | Linux | macOS |
|---|---|---|---|
| Typical users | General users, gaming, enterprise | Developers, servers, customization | Creatives, devs, Apple ecosystem |
| Package mgmt | `winget`, Microsoft Store, installers | `apt`, `dnf`, `pacman`, etc. | Homebrew, App Store, `.dmg` |
| Filesystem | **NTFS** | **ext4**, xfs, btrfs, zfs | **APFS** |
| CLI | **PowerShell**, CMD | **Bash/Zsh/Fish** | **Zsh/Bash**, Apple utilities |
| Security model | NT permissions, Defender | POSIX perms, SELinux/AppArmor | POSIX perms, sandboxing, Gatekeeper |
| Hardware support | Very broad (drivers by vendors) | Very broad, but varies by distro | Apple hardware only (officially) |
| Virtualization | Hyper-V, WSL | KVM/QEMU, LXC/LXD, Docker | Apple HVF, Docker (with limits) |

> Quick take: **Windows** is easiest for general users and games, **Linux** excels in servers and customization, **macOS** integrates tightly with Apple hardware and creative workflows.

---

## 💾 Filesystems (why they matter)

- **NTFS (Windows)** → journaling, ACL permissions, good for large files; supports compression & encryption (EFS/BitLocker).  
- **ext4 (Linux)** → fast, stable default on many distros; journaling; robust for servers.  
- **APFS (macOS)** → snapshots, copy-on-write, encryption; optimized for SSDs.  
- Others you may see: **xfs**, **btrfs** (snapshots, RAID-like features), **exFAT** (portable), **FAT32** (legacy).

> Tip: Use the **native filesystem** of your OS for system disks. Use **exFAT** for portable drives shared across OSes.

---

## 👥 Users, Permissions, and Security

- **Users & Groups** → access control boundaries (admin vs standard users).  
- **Permissions** → who can read/write/execute files or start services.  
- **Elevation** → `Run as administrator` (Windows), `sudo` (Linux/macOS).  
- **Sandboxing** → app stores, Gatekeeper (macOS), AppArmor/SELinux (Linux), UWP (Windows).  
- **Disk encryption** → BitLocker (Windows), LUKS (Linux), FileVault (macOS).

> Principle of least privilege: use a **standard account** for daily work; elevate only when needed.

---

## 🧰 Installing Software

- **Windows**  
  - Store apps or `.exe/.msi` installers  
  - Package managers:  
    ```powershell
    winget install Microsoft.PowerToys
    choco install git
    ```
- **Linux** (varies by distro)  
  - Debian/Ubuntu (`apt`):  
    ```bash
    sudo apt update && sudo apt install git
    ```
  - Fedora (`dnf`): `sudo dnf install git`  
  - Arch (`pacman`): `sudo pacman -S git`
- **macOS**  
  - `.dmg`/App Store or **Homebrew**:  
    ```bash
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    brew install git
    ```

> Package managers make installs/removals reproducible and scriptable.

---

## 🖥️ GUI vs CLI

- **GUI**: intuitive, discoverable, great for visuals and multitasking.  
- **CLI/Terminal**: faster for repeatable tasks, automation, remote work.  
  - Common shells: **PowerShell**, **Bash**, **Zsh**  
  - Remote: **SSH**, **RDP**, **VNC**

> Learn enough CLI to automate routine tasks; keep GUI for complex visual work.

---

## 🚀 Boot Process (super short)

1. **Firmware** (BIOS/UEFI) initializes hardware.  
2. **Bootloader** (Windows Boot Manager, GRUB, macOS boot.efi) starts the OS.  
3. **Kernel** loads drivers, mounts the root filesystem, starts services, shows login.

> UEFI + GPT is standard on modern systems (legacy BIOS + MBR is older).

---

## 🧩 Virtualization & Containers (where OS meets OS)

- **Virtual Machines (VMs)** → run a full OS inside another (Windows on Linux, etc.).  
  - Windows: **Hyper-V**, **VirtualBox**, **VMware**  
  - Linux: **KVM/QEMU**, **GNOME Boxes**  
  - macOS: **UTM**, **VMware Fusion**, **Parallels**  
- **WSL (Windows Subsystem for Linux)** → Linux userland on Windows with low overhead.  
- **Containers** (Docker/Podman) → isolate apps with shared kernel, start fast, great for dev/test/CI.

> VM = full OS; Container = app-level isolation. Different tools for different jobs.

---

## 🔄 Updates & Maintenance

- **Windows Update** + optional driver updates (Device Manager / vendor tools).  
- **Linux**: keep packages and kernel updated via your package manager.  
- **macOS**: System Settings → Software Update; app updates via App Store/Homebrew.  
- Backups: **File History**, **Time Machine**, **rsync**, **Restic/Borg**.  
- Health: disk SMART checks, free space, startup items, malware protection.

> Rule of thumb: back up before big upgrades; keep enough free SSD space (10–20%).

---

## 🗂️ Typical Directory Layouts

**Windows**

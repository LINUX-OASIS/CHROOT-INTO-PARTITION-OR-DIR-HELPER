# 🛡️ Chroot Helper

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
![Made with Bash](https://img.shields.io/badge/Made%20with-Bash-1f425f.svg)
![OS - Linux](https://img.shields.io/badge/OS-Linux-blue?logo=linux)
[![GitHub issues](https://img.shields.io/github/issues/LINUX-OASIS/CHROOT-INTO-PARTITION-OR-DIR-HELPER)](https://github.com/LINUX-OASIS/CHROOT-INTO-PARTITION-OR-DIR-HELPER/issues)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/LINUX-OASIS/CHROOT-INTO-PARTITION-OR-DIR-HELPER)](https://github.com/LINUX-OASIS/CHROOT-INTO-PARTITION-OR-DIR-HELPER/pulls)
[![GitHub stars](https://img.shields.io/github/stars/LINUX-OASIS/CHROOT-INTO-PARTITION-OR-DIR-HELPER)](https://github.com/LINUX-OASIS/CHROOT-INTO-PARTITION-OR-DIR-HELPER/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/LINUX-OASIS/CHROOT-INTO-PARTITION-OR-DIR-HELPER)](https://github.com/LINUX-OASIS/CHROOT-INTO-PARTITION-OR-DIR-HELPER/network)
[![GitHub last commit](https://img.shields.io/github/last-commit/LINUX-OASIS/CHROOT-INTO-PARTITION-OR-DIR-HELPER)](https://github.com/LINUX-OASIS/CHROOT-INTO-PARTITION-OR-DIR-HELPER/commits/main)

A Bash script that provides a user-friendly `whiptail` interface to easily `chroot` into any available Linux partition or a specified directory. It handles the tedious but essential tasks of mounting [...]

!chroot-helper-demo
*(Demo GIF placeholder)*

---

## ✨ Features

*   **Interactive TUI**: A simple and intuitive menu-driven interface powered by `whiptail`.
*   **Partition or Directory**: Flexibility to chroot into an auto-detected partition or a manually specified directory.
*   **Automatic Filesystem Management**: Mounts `/dev`, `/proc`, `/sys`, and `/usr` automatically before entering the chroot.
*   **Network Connectivity**: Preserves the host's network configuration by copying `/etc/resolv.conf` into the chroot.
*   **Safe & Robust Cleanup**: Uses a `trap` on exit to guarantee that all mounts are cleaned up and network settings are restored, even if the script is interrupted.
*   **Dependency Management**: Automatically checks for required commands and prompts the user to install them if they are missing.

---

## 🐧 OS Compatibility

This script is designed for Debian-based Linux distributions and has been tested on:

*   Debian
*   Ubuntu (all official flavors)
*   Linux Mint
*   Other Debian/Ubuntu derivatives that use the `apt` package manager.

---

## ⚙️ Dependencies & Installation

### Dependencies

The script requires the following commands to be installed on your system:
*   `whiptail` (from the `whiptail` package)
*   `lsblk` (from the `util-linux` package)
*   `awk` (from the `gawk` or `mawk` package)

If any of these dependencies are missing, the script will detect them and offer to install them for you automatically using `apt`.

### Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/LINUX-OASIS/CHROOT-INTO-PARTITION-OR-DIR-HELPER.git
    cd CHROOT-INTO-PARTITION-OR-DIR-HELPER
    ```

2.  **Make the script executable:**
    ```bash
    chmod +x custom-CHROOT-INTO-PARTITION-OR-DIR
    ```

---

## 🚀 Usage

The script must be run with root privileges. Simply execute it with `sudo`:

```bash
sudo ./custom-CHROOT-INTO-PARTITION-OR-DIR
```

You will be presented with a menu to choose whether to chroot into a partition or a directory. Follow the on-screen prompts. To exit the chroot environment, simply type `exit` or press `Ctrl+D`.

---

## 💬 Contributing

Pull requests, issues, and suggestions are warmly welcomed! See [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines.

---

## 🌐 Links

*   **Issues**: [github.com/LINUX-OASIS/CHROOT-INTO-PARTITION-OR-DIR-HELPER/issues](https://github.com/LINUX-OASIS/CHROOT-INTO-PARTITION-OR-DIR-HELPER/issues)
*   **Pull Requests**: [github.com/LINUX-OASIS/CHROOT-INTO-PARTITION-OR-DIR-HELPER/pulls](https://github.com/LINUX-OASIS/CHROOT-INTO-PARTITION-OR-DIR-HELPER/pulls)
*   **Releases**: [github.com/LINUX-OASIS/CHROOT-INTO-PARTITION-OR-DIR-HELPER/releases](https://github.com/LINUX-OASIS/CHROOT-INTO-PARTITION-OR-DIR-HELPER/releases)
*   **Wiki**: [github.com/LINUX-OASIS/CHROOT-INTO-PARTITION-OR-DIR-HELPER/wiki](https://github.com/LINUX-OASIS/CHROOT-INTO-PARTITION-OR-DIR-HELPER/wiki)

---

## 🧙‍♂️ Maintainer

**[LINUX-OASIS](https://github.com/LINUX-OASIS)**

---

## 📜 License

This project is licensed under the GNU General Public License v3.0. See the LICENSE file for details.

Here’s a complete `README.md` for your GitHub repo, including usage instructions, supported OS, and a clean title for the project:

---

```markdown
# 💾 Swap File Auto Setup Script

This script allows you to **easily create and configure swap memory** on your Linux VPS (ideal for low-RAM servers like those with 1GB RAM). It interactively guides you through the process and applies sensible defaults if you just press `Enter`.

---

## 📌 Features

- Interactive terminal prompts with default options
- Auto-creates and enables a swap file
- Configures swappiness and cache pressure
- Works with `fallocate` or falls back to `dd`
- Permanently persists settings across reboots

---

## 🖥️ Supported Operating Systems

- Ubuntu (16.04 and above)
- Debian (9 and above)
- Other systemd-based Linux distributions (may require minor tweaks)

> ⚠️ Not tested on CentOS, Fedora, or Alpine — feel free to open issues if you'd like support added!

---

## 🚀 Quick Install

You can run this script in **one line** directly from your terminal:

```bash
bash <(curl -Ls https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_REPO/main/setup-swap.sh)
```

Replace `YOUR_USERNAME` and `YOUR_REPO` with your actual GitHub username and repository name.

---

## 🛠️ What It Does

1. Asks for the desired swap size (e.g. `1G`, `512M`) — defaults to `1G`
2. Creates a swap file and enables it
3. Configures `vm.swappiness` and `vm.vfs_cache_pressure`
4. Adds swap file to `/etc/fstab` for persistence
5. Shows memory status at the end

---

## 🧩 Example Output

```bash
==============================
  SWAP FILE SETUP FOR VPS  
==============================

Enter swap size (e.g., 1G, 512M) [default: 1G]: 
[*] Creating a 1G swap file at /swapfile...

[✓] Swap successfully enabled with 1G
```

---

## 🙋‍♂️ Why Use Swap?

Swap helps extend available memory when RAM is full — crucial on small VPS servers where running MySQL, Apache, Node, or other services can cause memory pressure.

---

## 📃 License

MIT License. Use freely and modify as needed.
```

---
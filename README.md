# 🏰 My HomeLab Infrastructure

Documentation of my personal server infrastructure and networking lab.

## 🖥️ Hardware: Minisforum MS-01 Workstation
## raspberry pi 3b
This server acts as the primary hypervisor node.

* **CPU:** Intel Core i5-12450H (8 Cores / 12 Threads)
* **RAM:** 64 GB DDR5
* **Storage:**
  * **Primary:** 2 TB Samsung NVMe SSD (System & VM Storage)
  * **Secondary:** 500 GB SSD (Backup/ISO Storage)
* **Connectivity:** Dual 10GbE SFP+ & Dual 2.5GbE LAN

## ⚙️ Software Stack
* **Hypervisor:** Proxmox VE (Virtual Environment)
- **Tailscale:** Configured `mv01` as an Exit Node.
- **AdGuard:** Added to the stack for ad blocking.
* *More services to be documented...* :D

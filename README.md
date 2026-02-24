# 🏰 My HomeLab Infrastructure

Documentation of my personal server infrastructure and networking lab.

## 🖥️ Hardware: Minisforum MS-01 Workstation
This server acts as the primary hypervisor node.

* **CPU:** Intel Core i5-12450H (8 Cores / 16 Threads)
* **RAM:** 64 GB DDR5
* **GPU** NVIDIA RTX A2000 (6GB)
* **Storage:**
  * **Primary:** 2 TB Samsung NVMe SSD (System & VM Storage)
  * **Secondary:** 500 GB SSD (Backup/ISO Storage)
* **Connectivity:** Dual 10GbE SFP+ & Dual 2.5GbE LAN

## ⚙️ Software Stack
* **Hypervisor:** Proxmox VE (Virtual Environment)
- **Tailscale:** Configured `mv01` as an Exit Node.
- **AdGuard:** Added to the stack for ad blocking.



## HomeLab Timeline
## [2026-01-19] - Initial Setup & Network Fixes</summary>


<details>
<summary>## 2026-01-23 Nextcloud</summary>

- Deployed a self-hosted Nextcloud container on Proxmox for private cloud storage.
- Established a dedicated storage backend to ensure full data ownership and privacy.
    </details>

<details>
<summary>## 2026-02-08</summary>

- Fixed internal networking issues by enabling Tailscale subnet routing on the Arch client.

- Successfully connected both Desktop (Arch) and Mobile (Android) clients to the self-hosted instance.

- Configured specific folder synchronization
    </details>

<details>
<summary>## 2026-02-11</summary>

- Made a new Ubuntu Server 24.04 LTS VM on the MS-01 for Linux troubleshooting practice and monitoring.
    </details>

<details>
<summary>## 2026-02-12</summary>

- set up a dedicated LXC container dev-server for school/coding.

- figured out how to run Docker inside LXC.

- deployed Code-Server via docker-compose so i can run VS Code in the browser.
    </details>

<details>
<summary>## 2026-02-21</summary>

- Built a highperformance Windows 11 VM on the MS-01 in preparation for RTX A2000 GPU passthrough.

- Configured Proxmox for optimal Windows VM performance.

- Configured Proxmox host for PCIe passthrough by enabling IOMMU in GRUB (intel_iommu=on iommu=pt).

- Set up Parsec on both the Windows VM and Arch Linux client for low-latency remote use.

- Pre-downloaded NVIDIA drivers and GPU-Z, ready for the physical GPU installation.
</details>

<details>
<summary>## 2026-02-22</summary>
 
- Successfully completed the physical RTX A2000 hardware installation and booted the Windows 11 VM with full PCIe GPU passthrough.
    
- Stress tested the Parsec remote streaming setup to evaluate hardware encoding and network latency.

- Used a ThinkPad T480 as the remote client device to validate the setup

    </details>

<details>
<summary>## 2026-02-23</summary>
- Deployed a new Ubuntu Server 24.04 LTS VM on Proxmox dedicated to AI and LLM workloads.
 
- Reconfigured the RTX A2000 PCIe passthrough to work with the new Linux VM.

- Installed Ollama and Open WebUI to host local AI models.

- Discovered a persistent bug where the GPU remains stuck in the P0 power state (35W+) with a "ghost" 1MiB VRAM usage

</details>

<details>
<summary>## 2026-02-24</summary>
- Purged the entire Xorg/GUI stack while troubleshooting, resulting in a cleaner, fully headless server environment.
 
- Confirmed the system is stable under 98% GPU load despite the high idle power draw.
</details>


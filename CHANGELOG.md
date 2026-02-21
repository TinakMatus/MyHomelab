#  HomeLab Timeline

## [2026-01-19] - Initial Setup & Network Fixes
### Added
- **Hardware:** Minisforum MS-01 (i5/64GB) deployed.
- **3D Printer:** Ender-3 Pro


**softwere:**
- **proxmox:** for dockers and virtualization.
- **Tailscale:** Configured `mv01` as an Exit Node.
- **AdGuard:** Added to the stack for ad blocking.
- **NextCloud** Added to for private storage.


## 2026-01-23
- Deployed a self-hosted Nextcloud container on Proxmox for private cloud storage.
- Established a dedicated storage backend to ensure full data ownership and privacy.

## 2026-02-08
- Fixed internal networking issues by enabling Tailscale subnet routing on the Arch client.
- Successfully connected both Desktop (Arch) and Mobile (Android) clients to the self-hosted instance.
- Configured specific folder synchronization

## 2026-02-11
- Made a new Ubuntu Server 24.04 LTS VM on the MS-01 for Linux troubleshooting practice and monitoring.

## 2026-02-12
- set up a dedicated LXC container `dev-server` for school/coding.
- figured out how to run Docker inside LXC.
- deployed Code-Server via docker-compose so i can run VS Code in the browser.

## 2026-02-21
- Built a highperformance Windows 11 VM on the MS-01 in preparation for RTX A2000 GPU passthrough.
- Configured Proxmox for optimal Windows VM performance.
- Configured Proxmox host for PCIe passthrough by enabling IOMMU in GRUB (`intel_iommu=on iommu=pt`).
- Set up Parsec on both the Windows VM and Arch Linux client for low-latency remote use.
- Pre-downloaded NVIDIA drivers and GPU-Z, ready for the physical GPU installation.

2026-02-22

- Successfully completed the physical RTX A2000 hardware installation and booted the Windows 11 VM with full PCIe GPU passthrough.
- Stress tested the Parsec remote streaming setup to evaluate hardware encoding and network latency.
- Used a ThinkPad T480 as the remote client device to validate the setup the experience was flawlessly smooth with zero noticeable input lag.
- Monitored GPU thermals and power states and discovered exactly how loud a 3000 RPM blower fan sounds in a tiny chassis.

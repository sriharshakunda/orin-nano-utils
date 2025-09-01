# Jetson PyTorch Installer for Orin Nano

One-command, interactive installer for **PyTorch on NVIDIA Jetson (aarch64)**.  
Supports JetPack **5.1.1 / 5.1.2** and **6.0 / 6.1 / 6.2** lines, installs **cuSPARSELt** first when required, and validates the install.

## What this repo contains
  - `install_pytorch_jetson.sh` – interactive PyTorch installer that:
  - asks for your **JetPack** code (`511`, `512`, `60`, `61`, `62`)
  - selects a **sane default wheel URL** you can override
  - installs **cuSPARSELt** first for JP ≥ 6.0
  - verifies `import torch` and CUDA availability

> **Note**  
> On JP 6.x, NVIDIA’s PyTorch wheels (24.06 and newer) **require cuSPARSELt** to be present on the system before installing the wheel.

---

## Quick start

```bash
git clone <this-repo>
cd <this-repo>

# Optional: edit the scripts if you want custom wheel URLs
chmod +x install_pytorch.sh
bash ./install_pytorch.sh

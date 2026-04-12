<p align="center">
  <img src="assets/st6_logo_540.png" alt="st6.interpo-scale logo" width="120"/>
</p>

<h1 align="center">🍂 st6.interpo-scale</h1>

<p align="center">
  <b>AI-powered upscaling, frame interpolation, denoising, restoration, sharpening & depth maps — right inside After Effects.</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-1.0.0-orange?style=flat-square" alt="Version"/>
  <img src="https://img.shields.io/badge/platform-Windows-blue?style=flat-square" alt="Platform"/>
  <img src="https://img.shields.io/badge/host-After%20Effects-9999FF?style=flat-square" alt="Host"/>
  <img src="https://img.shields.io/badge/GPU-NVIDIA%20%7C%20AMD%20%7C%20Intel-green?style=flat-square" alt="GPU"/>
  <img src="https://img.shields.io/badge/license-MIT-red?style=flat-square" alt="License"/>
</p>

<p align="center">
  <a href="https://github.com/st6autumn/St6.Interpo-Scale/releases/latest">
    <img src="https://img.shields.io/badge/⬇_Download_Latest_Release-222?style=for-the-badge&logo=github" alt="Download"/>
  </a>
</p>

---

## 📖 About

**st6.interpo-scale** is a free, Adobe After Effects extension that brings professional AI video processing to your timeline. Everything runs locally on your GPU — no cloud, no subscriptions, no accounts required.

Select a comp or layer, toggle the processing steps you need, and hit render. The extension handles frame extraction, AI inference, and automatic re-import back into your project.

---

## ✨ Features

### 🔄 Processing Chain

| Step | Description |
|------|-------------|
| **Upscale** | AI super-resolution up to 4x — RealESRGAN, SwinIR, ShuffleCUGAN, Compact, UltraSharp & more |
| **Interpolation** | RIFE-based frame interpolation — 2x, 4x, 8x multipliers with scene-change detection |
| **Denoise** | AI denoising with adjustable strength |
| **Sharpen** | AI sharpening for post-process clarity |
| **Restore** | Face & detail restoration for degraded footage |
| **Depth Map** | Monocular depth estimation — Depth Anything V2/V3, MiDaS, with colormaps & edge smoothing |

### 🎛️ Pipeline & Output

- **Processing chain** — toggle and reorder steps freely; the pipeline adapts
- **Quality presets** — Extreme / High / Medium / Fast per step
- **Encoders** — x264, x265, NVENC H.264/H.265, ProRes
- **Batch queue** — queue multiple comps/layers and process them back to back
- **Live preview** — thumbnail updates as frames are rendered
- **Auto-import** — rendered files import directly into AE with matching layer names
- **Prerender-only mode** — skip the chain and just export frames when no steps are active

### 🖥️ GPU Support

| Backend | GPU |
|---------|-----|
| CUDA / TensorRT | NVIDIA (RTX 20-series and newer recommended) |
| DirectML | AMD Radeon |
| OpenVINO | Intel Arc |
| NCNN (Vulkan) | Any Vulkan-capable GPU |

### 🔧 Extras

- **Offline-first** — models download once, then everything runs locally
- **Auto-update checker** — checks GitHub releases on startup and shows an update banner
- **Custom output folder** or auto-save next to your `.aep` project
- **Delete button** — removes rendered layers and their source files in one click
- **Preset system** — save and load your favourite processing chains

---

## 📥 Installation

### Method 1 — ZXP Installer (Recommended)

1. Download **`St6.Interpo-Scale_[v-.-.-].zxp`** from the [Latest Release](https://github.com/st6autumn/St6.Interpo-Scale/releases/latest)
2. Install using [ZXP Installer](https://zxpinstaller.com/) or [Anastasiy's Extension Manager](https://install.anastasiy.com/)
3. Open After Effects → **Window** → **Extensions** → **st6.interpo-scale**
4. On first launch, click **Setup Dependencies** inside the panel to install the Python backend & models

### Method 2 — Manual Install (install.bat)

1. Download and extract the latest release
2. Run **`install.bat`** as administrator
3. Restart After Effects
4. Open the panel from **Window** → **Extensions** → **st6.interpo-scale**

### First-Time Setup

The extension needs a Python virtual environment with PyTorch and the AI models. On first launch, click the **Setup** button in the Settings tab — it handles everything automatically. An internet connection is required for the initial model download only.

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|------------|
| Extension UI | HTML / CSS / JavaScript (CEP) |
| Host scripting | ExtendScript (JSX) |
| AI backend | Python, PyTorch, ONNX Runtime |
| Frame I/O | FFmpeg |
| Upscale models | RealESRGAN, SwinIR, ShuffleCUGAN, Compact, UltraSharp |
| Interpolation | RIFE (IFNet architecture) |
| Depth estimation | Depth Anything V2/V3, MiDaS |
| Packaging | CEP / ZXP |

---

## 📊 Stats

| Metric | Value |
|--------|-------|
| Frontend (JS) | ~4 500 lines |
| Backend (Python) | ~3 500 lines |
| UI (HTML + CSS) | ~2 000 lines |
| ExtendScript (JSX) | ~900 lines |
| Supported upscale models | 20+ |
| GPU backends | 4 (CUDA, DirectML, OpenVINO, NCNN) |

---

## 📋 Requirements

- Adobe After Effects CC 2020 or later
- Windows 10/11
- Python 3.10+
- FFmpeg in PATH
- GPU with 4 GB+ VRAM (8+ GB recommended for large models)

---

## 📜 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- [**RIFE**](https://github.com/hzwer/ECCV2022-RIFE) — real-time intermediate flow estimation for frame interpolation
- [**Real-ESRGAN**](https://github.com/xinntao/Real-ESRGAN) — practical image/video restoration algorithms
- [**Depth Anything**](https://github.com/DepthAnything/Depth-Anything-V2) — monocular depth estimation models
- [**MiDaS**](https://github.com/isl-org/MiDaS) — Intel ISL monocular depth estimation
- [**FFmpeg**](https://ffmpeg.org/) — multimedia framework for frame extraction and encoding
- [**PyTorch**](https://pytorch.org/) — deep learning framework powering the AI models
- [**HuggingFace Transformers**](https://huggingface.co/docs/transformers/) — model hub and inference library

---

<p align="center">
  Made with 🍂 by <a href="https://github.com/st6autumn">st6autumn</a>
</p>

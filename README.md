# LedFx for OpenWrt 💡🌈

**Transform your OpenWrt device into a powerful audio-reactive LED controller**

Build and run [LedFx](https://github.com/LedFx/LedFx) on OpenWrt-compatible devices to create stunning real-time light shows that dance to your music.

> [!CAUTION]
> **Work in Progress**: The packages are currently incomplete and do not yet provide a fully functional LedFx installation.

## 🎯 What is LedFx for OpenWrt?

LedFx for OpenWrt brings the power of audio-reactive LED control to embedded devices and single-board computers. Whether you're running a router, Raspberry Pi, or other OpenWrt-compatible hardware, you can now create mesmerizing light displays that respond to audio in real-time.

## ✨ Why Choose OpenWrt for LedFx?

Running LedFx on OpenWrt offers significant advantages over traditional installations:

### 🚀 **Performance & Efficiency**
- **Cross-compilation ready**: All dependencies are pre-built, dramatically reducing setup time on resource-constrained devices
- **Optimized for embedded systems**: Lightweight footprint perfect for routers and single-board computers
- **Faster deployment**: No need to compile complex Python packages on older ARM processors

### 🎵 **Superior Audio Input Capabilities**
- **Direct analog/digital audio input**: Connect directly to amplifiers, mixers, or audio interfaces via line-in, USB audio, or I2S
- **Real audio signal processing**: Process actual audio signals rather than just desktop audio capture

### 🛡️ **Reliability & Safety**
- **Read-only filesystem support**: Safe power-off without proper shutdown procedures
- **Stable operation**: Perfect for always-on embedded applications
- **Crash-resistant**: Minimal risk of filesystem corruption

### 🌐 **Hardware Compatibility**
- **Extensive device support**: Leverage OpenWrt's vast hardware compatibility
- **Maximum portability**: Run on everything from routers to development boards
- **Consistent environment**: Same software stack across different hardware platforms

## 📦 Installation

### Prerequisites
- OpenWrt build environment set up
- Basic familiarity with OpenWrt package compilation

### Step 1: Add the Feed
Edit your `feeds.conf.default` file and add the LedFx feed:
```
src-git ledfx_for_openwrt https://github.com/danielstrauss02/ledfx_for_openwrt
```

### Step 2: Update and Install Feeds
```bash
./scripts/feeds update -a
./scripts/feeds install -a
```

### Step 3: Configure Build
```bash
make menuconfig
```
Navigate to: **LedFx for OpenWrt** → Enable the **ledfx** package

### Step 4: Build
```bash
make package/ledfx/compile
```

## 📊 Development Progress

This is the list of all dependencies of LedFx 2.0.108 and their current status:

### Legend
| Symbol | Status |
|--------|--------|
| ✅ | Completed and working |
| ⚠️ | Packaged but has issues |
| ❓ | Not yet started |
| 📦 | Available in upstream [OpenWrt packages](https://github.com/openwrt/packages) |

### Dependencies
| Dependency | Status | Notes |
|------------|--------|-------|
| `numpy>=1.26.2,<2.0.0` | ✅ | Version 1.26.4 provided by `openwrt/packages` |
| `cffi>=0.16.0` | 📦 |  |
| `wheel>=0.36.2` | 📦 |  |
| `aiohttp>=3.9.1,<4.0.0` | 📦 |  |
| `aiohttp-cors>=0.7.0` | 📦 |  |
| `aubio>=0.4.9` | ✅ |  |
| `cython>=3.0.7` | 📦 |  |
| `certifi>=2023.11.17` | 📦 |  |
| `multidict>=6.0.4` | 📦 |  |
| `openrgb-python>=0.2.15` | ✅ |  |
| `paho-mqtt>=1.6.1` | 📦 |  |
| `psutil>=5.9.7` | ⚠️📦 | Version 5.9.5 upstream |
| `pyserial>=3.5` | 📦 |  |
| `pystray>=0.19.5` | ❓ | No source distribution on PyPi |
| `python-rtmidi>=1.5.8` | ⚠️ | Builds correctly, but shared object has wrong name |
| `requests>=2.31.0` | 📦 |  |
| `sacn>=1.9.0` | ✅ |  |
| `sentry-sdk>=1.40.4` | ⚠️📦 | Version 1.29.2 upstream |
| `sounddevice>=0.4.6` | ✅ |  |
| `samplerate>=0.2.1` | ⚠️ | CMake build fails |
| `icmplib>=3.0.4` | ✅ |  |
| `voluptuous>=0.14.1` | ⚠️📦 | Version 0.13.1 upstream |
| `zeroconf>=0.131.0` | ✅ |  |
| `pillow>=10.1.0` | 📦 |  |
| `flux-led>=1.0.4` | ⚠️ | Missing dependency: `pytest-runner>=5.2` |
| `python-osc>=1.8.3` | ❓ |  |
| `pybase64~=1.4.0` | ❓ |  |
| `mss~=10.0.0` | ❓ |  |
| `setuptools~=76.0.0` | ⚠️📦 | Version 69.0.2 upstream |
| `uvloop>=0.16.0` | ❓ |  |
| `rpi-ws281x>=4.3.0` | ❓ |  |
| `stupidartnet>=1.6.0,<2.0.0` | ❓ |  |
| `python-dotenv>=1.0.0,<2.0.0` | 📦 |  |
| `vnoise>=0.1.0,<1.0.0` | ❓ |  |

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

- **Package creation**: Create OpenWrt packages for missing dependencies
- **Package fixes**: Resolve build issues and compatibility problems
- **Testing**: Verify packages work on different OpenWrt targets

Please open an issue before starting major work, or submit a pull request with your improvements.

## 📄 License

This project is licensed under the **GNU GPL 2.0 License**. See the [LICENSE](LICENSE) file for complete details.

## 🙏 Acknowledgments

- **[LedFx Team](https://github.com/LedFx/LedFx)** - For creating the amazing audio-reactive LED software
- **[OpenWrt Community](https://openwrt.org/)** - For providing the excellent embedded Linux distribution

---

**Note**: This is an unofficial packaging effort. For the main LedFx project, visit the [official repository](https://github.com/LedFx/LedFx).
# iso2chd 🚀

[![Version](https://img.shields.io/badge/version-2.0.0-blue.svg)](https://github.com/penguin-crate/iso2chd/releases)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](LICENSE)
[![Arch Linux](https://img.shields.io/badge/Arch%20Linux-Native-1793d1.svg?logo=arch-linux)](https://archlinux.org)

An advanced, blazing-fast batch disk image to CHD conversion suite optimized for Arch Linux and retro-gaming collections. Designed and engineered by **Abhimanyu Bhadauriya**.

`iso2chd` automates the compression of optical media backups (`.iso`, `.bin`, `.cue`) into high-efficiency Compressed Hunks of Data (`.chd`) using `chdman`, featuring parallel thread tuning, deep recursive directory scanning, and live storage savings telemetry.

---

## Key Features

* **Multi-Format & Recursive Scanning (`-r`)**: Deep-scans directories for `.iso`, `.bin`, and `.cue` files, or accepts precise individual file paths.
* **Smart Mode Switching (`-m`)**: Automatically routes images to `createdvd` or `createcd`, or lets you manually override modes.
* **Compression Codec Control (`-c`)**: Tailor your compression using `zlib`, high-ratio `lzma`, or high-speed `huff`.
* **Multi-Core Threading (`-p`)**: Leverage custom processor thread counts to drastically cut down batch conversion times.
* **Integrity Validation (`-v`)**: Optionally runs `chdman verify` right after creation to ensure zero data corruption.
* **CHD Guard Check**: Automatically blocks redundant attempts to convert `.chd` files into `.chd`.
* **Built-in Inspector (`--info`)**: Instantly inspect internal headers, block sizes, and checksums of any `.chd` file.
* **Live Telemetry & Analytics**: Tracks raw input sizes vs. compressed output to print out an accurate total storage savings report.
* **Arch Native**: Packaged with a robust `PKGBUILD`, `.SRCINFO`, and a dedicated man page (`iso2chd.1`).

---

## 📦 Installation (Arch Linux)

Ensure you have `git` and `base-devel` installed, then clone and build the package natively:

```bash
git clone [https://github.com/penguin-crate/iso2chd.git](https://github.com/penguin-crate/iso2chd.git)
cd iso2chd
makepkg -sic

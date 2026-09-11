# iso2chd

[![Version](https://img.shields.io/badge/version-1.1.0-blue.svg)](https://github.com/penguin-crate/iso2chd/releases)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](LICENSE)

An interactive, light-weight batch ISO to CHD conversion utility optimized for Arch Linux and retro-gaming setups. Designed by **Abhimanyu Bhadauriya**.

`iso2chd` automates the process of compressing PlayStation 2 and other DVD disc images (`.iso`) into high-efficiency `.chd` format using `chdman createdvd`, safely deleting source ISO files upon successful verification.

---

## Features

* **DVD Sector Optimization:** Uses `chdman createdvd` under the hood to ensure full compatibility with single and dual-layer game ISOs without sector corruption.
* **Interactive & Headless:** Prompts for directory input if run without arguments, or accepts target directories directly via command line.
* **Tilde Path Expansion:** Full support for `~` paths (e.g. `~/Downloads/ISOs`).
* **Space Saving:** Automatically removes source `.iso` files only when `chdman` reports a 0 exit status (successful build).
* **Arch Native:** Packaged with `PKGBUILD` and includes a dedicated `man` page (`iso2chd.1`).

---

## Installation

### Building from Source (Arch Linux)

Ensure you have `git` and `base-devel` installed:

```bash
git clone https://github.com/penguin-crate/iso2chd.git
cd iso2chd
makepkg -sic

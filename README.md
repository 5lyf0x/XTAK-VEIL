# XTAK VEIL

**XTAK VEIL** is a Raspberry Pi-based SDR sensor platform and WebUI designed to operate either **standalone** or as part of the **XTAK environment**. It combines radio monitoring, spectrum analysis, multi-antenna management, message collection, and field-oriented sensor services in a single node.

> **Beta software:** This repository contains the public beta source for **XTAK VEIL v0.4.0-r32**. VEIL is actively developed and some services depend on local RF activity, supported SDR hardware, external decoder projects, and site-specific configuration.

## What VEIL does

VEIL turns a Raspberry Pi and supported SDR hardware into a network-accessible sensor node with a browser-based management interface. It can be used by itself from the WebUI or integrated with XTAK clients and related XTAK components.

Current capabilities include:

- **Standalone WebUI** for node configuration, monitoring, service control, messages, recovery, and administration.
- **XTAK integration** for networked sensor use, live situational-awareness output, plugin/API access, and related XTAK workflows.
- **Spectrum analyzer and waterfall** with signal selection, detected peaks, listening, and frequency identification.
- **Multi-antenna switching and band routing** with support for four antenna ports and automatic routing by frequency/service.
- **Analog radio monitoring** with user-created presets, favorites, groups, import/export workflows, and live audio monitoring.
- **Managed nationwide receive channel groups** for FRS, GMRS, CB, MURS, and NOAA Weather.
- **ADS-B** aircraft reception and live situational-awareness output.
- **APRS**, **AIS**, **ACARS**, **VDL2**, **P25**, and other supported receive-service workflows.
- **Remote ID** sensor support for supported receive paths.
- **Messages workspace** with service/category filtering, conversation history, protection, retention controls, and backup/restore support.
- **Bluetooth audio** and browser monitoring support for compatible receive services.
- **RF-to-mesh bridge foundation** for XTAK Voice integration.
- **Network and Wi-Fi management**, provisioning mode, diagnostics, time synchronization, recovery actions, configuration snapshots, and an authenticated maintenance terminal.

## Hardware / platform

The installer targets **Raspberry Pi OS aarch64** and is intended for Raspberry Pi-based VEIL nodes. Development and field testing have primarily used RTL-SDR-class receivers such as the **Nooelec NESDR Nano 3** together with an external four-port antenna switch.

Actual receive coverage and performance depend on the SDR, antenna system, RF environment, and decoder/service being used.

## Public beta version

Current public beta source:

**v0.4.0-r32**

r32 adds a software-managed nationwide channel catalog containing:

- FRS — 22 channels
- GMRS — 30 channels
- CB — 40 channels
- MURS — 5 channels
- NOAA Weather — 7 channels

The same catalog is used by the Services UI and Spectrum frequency identification. r32 also adds CB / Low Band antenna routing and preserves user-owned presets/groups across upgrades.

See [CHANGELOG.md](CHANGELOG.md) for the detailed development history included with this beta.

## Install

On the Raspberry Pi:

```bash
git clone https://github.com/5lyf0x/XTAK-VEIL.git
cd XTAK-VEIL
sudo ./install.sh
```

The installer checks and installs required Raspberry Pi OS/Debian dependencies, creates the VEIL service environment, and installs/updates the node in place.

For an existing VEIL node, normal upgrades are designed to preserve persistent node configuration and state unless a release explicitly documents a migration.

## Web console

After installation, connect to the VEIL WebUI using the node's network address or mDNS hostname.

Fresh installations use the default administrator credentials documented in the software. **Change the administrator password under Settings > Security before deploying the node on an untrusted network.**

## Important notes

VEIL is primarily a **receive/sensor platform**. Availability and decoding of any particular radio service depend on compatible hardware, local RF activity, configuration, and the applicable external decoder stack.

Operators are responsible for using radio equipment and received information in accordance with applicable laws, regulations, policies, and authorization requirements.

## Project status

VEIL is under active development. This public repository is a beta snapshot and may lag private/internal development while features are validated for wider use.

Issues and field reports are welcome when they include the VEIL version, Raspberry Pi model/OS, SDR hardware, active service, and relevant diagnostics.

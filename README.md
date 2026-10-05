# XTAK VEIL

**XTAK VEIL** is a Raspberry Pi-based SDR sensor platform and WebUI designed to operate either **standalone** or as part of the **XTAK environment**. It combines radio monitoring, spectrum analysis, multi-antenna management, message collection, and field-oriented sensor services in a single node.

> **Beta software:** The current public beta target is **XTAK VEIL v0.4.0-r32**. VEIL is actively developed and some services depend on local RF activity, supported SDR hardware, external decoder projects, and site-specific configuration.

## What VEIL does

VEIL turns a Raspberry Pi and supported SDR hardware into a network-accessible sensor node with a browser-based management interface. It can be used by itself from the WebUI or integrated with XTAK clients and related XTAK components.

Current capabilities include:

- **Standalone WebUI** for node configuration, monitoring, service control, messages, recovery, and administration.
- **XTAK integration** for networked sensor use, live situational-awareness output, plugin/API access, and related XTAK workflows.
- **Spectrum analyzer and waterfall** with signal selection, detected peaks, listening, and frequency identification.
- **Analog radio monitoring** with user-created presets, favorites, groups, import/export workflows, and live audio monitoring.
- **Managed nationwide receive channel groups** for FRS, GMRS, CB, MURS, and NOAA Weather.
- **ADS-B** aircraft reception and live situational-awareness output.
- **APRS**, **AIS**, **ACARS**, **VDL2**, **P25**, and other supported receive-service workflows.
- **Remote ID** sensor support for supported receive paths.
- **Messages workspace** with service/category filtering, conversation history, protection, retention controls, and backup/restore support.
- **Bluetooth audio** and browser monitoring support for compatible receive services.
- **RF-to-mesh bridge foundation** for XTAK Voice integration.
- **Network and Wi-Fi management**, provisioning mode, diagnostics, time synchronization, recovery actions, configuration snapshots, and an authenticated maintenance terminal.

Coming Features:
- **Multi-antenna switching and band routing** with support for four antenna ports and automatic routing by frequency/service.
- **Multi-node triangulation** to find the estimated location of a signal.

## Hardware / platform

VEIL targets **Raspberry Pi OS aarch64** and is intended for Raspberry Pi-based sensor nodes. Development and field testing have primarily used RTL-SDR-class receivers such as the **Nooelec NESDR Nano 3** together with an external four-port antenna switch.

Actual receive coverage and performance depend on the SDR, antenna system, RF environment, and decoder/service being used.

## v0.4.0-r32 beta

r32 adds a software-managed nationwide channel catalog containing:

- FRS — 22 channels
- GMRS — 30 channels
- CB — 40 channels
- MURS — 5 channels
- NOAA Weather — 7 channels

The same catalog is used by the Services UI and Spectrum frequency identification. r32 also adds CB / Low Band antenna routing and preserves user-owned presets/groups across upgrades.

## Project status

VEIL is under active development. This public repository is intended for beta releases and may lag private/internal development while features are validated for wider use.

Issues and field reports are welcome when they include the VEIL version, Raspberry Pi model/OS, SDR hardware, active service, and relevant diagnostics.

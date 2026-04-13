X99 BIOS Modding Toolkit

Maintained by avkila * Discord: avkila
Instagram: @avkilasmodding
Community: Find me on the Miyconst Discord server.

🛠️ Core Modification Tools
S3TurboTool: An advanced Turbo Boost unlocking utility for X99 motherboards. Allows for the creation of custom .ffs drivers and provides granular control over the FIVR bug (use with caution).

Ultimate Patcher Tool: An all-in-one automated modding solution for X99 BIOS. Capable of unlocking overclocking, memory timings, Turbo Unlock, ReBar injection, and logo customization. [Status: Untested]

AMIBCP: Powerful utility for modifying BIOS menu visibility. Use this to toggle hidden settings and expose advanced menus to the end-user.

MMTool: The standard for managing BIOS modules. Essential for injecting or extracting microcodes and .ffs drivers.

AMIChangeLogo: Specialized tool for backing up or replacing the OEM boot splash screen (Motherboard/BIOS logo).

🔍 Analysis & Extraction
UEFITool / UEFITool_NE: The industry standard for BIOS analysis. The NE (New Engine) version is best for visualization and structure analysis, while the standard version is required for actual image editing and driver injection.

UEFIExtract NE: A command-line utility used to unpack firmware files into a searchable directory structure for deep analysis of volumes and sections.

IFR Extractor: Parses the BIOS Setup module to generate a readable text map of all hidden and visible configuration menus.

lzma.exe: Command-line utility for decompressing and compressing LZMA data blocks within AMI BIOS images.

💾 Flashing & DMI Management
FPTW64 (Intel Flash Programming Tool): A 64-bit utility for dumping and flashing the BIOS region or full SPI image.

Note: Requires "BIOS Lock" to be disabled via AMIBCP or Grub shell.

AFUWINGUIx64: A GUI-based alternative to FPT for flashing AMI BIOS. Shares the same "BIOS Lock" requirements as FPT.

NeoProgrammer: The preferred software for use with CH341A hardware programmers. Highly recommended for recovering from bricks or flashing boards with locked descriptors.

AMIDEWIN / DMIEDIT: Tools for reading and writing DMI/SMBIOS data (Serial Numbers, UUIDs, Asset Tags). DMIEDIT provides a user-friendly GUI.

🚀 Performance & Feature Drivers
ReBarDxe.ffs: EFI driver for Resizable BAR support. Requires Secure Boot to be OFF.

ReBarState.exe: CLI tool to configure the ReBar size. A value of 2^32 is recommended for maximum VRAM utilization.

NVME.ffs: Driver for adding NVMe boot support to older UEFI motherboards that lack native M.2 boot capabilities.

XTUSetup (v6.4.2.40): A specific Intel XTU version compatible with Chinese X99 boards. Allows for overclocking provided the BIOS has been prepped (e.g., via AMIBCP).

ME System Tools v9.1 R7: Tools for modifying the Intel Management Engine. Useful for fixing BCLK at exactly 100MHz (disabling Spread Spectrum).
Supported Chipsets: Q87, H87, Z87. (Genuine X99/C612 requires a different ME version).

⚠️ Disclaimer
USE AT YOUR OWN RISK.
I am not responsible for any damages including, but not limited to: bricked motherboards, fried VRMs, hardware failure, or data loss. BIOS modding carries inherent risks of permanent hardware damage. Always have a CH341A programmer and a backup of your original BIOS before proceeding.

🕒 Changelog
11.04.2026: Added ReBarDxe and NVME .ffs drivers. Included injection instructions for UEFITool.
11.04.2026: Added UEFITool (Standard) and UEFIExtractNE; updated documentation.
27.03.2026: Patched AFUWINGUI to resolve execution errors.

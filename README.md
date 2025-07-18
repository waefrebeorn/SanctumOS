# SanctumOS

[![Discord](https://img.shields.io/discord/934200098144022609?color=7289DA&label=Discord&logo=discord&logoColor=white)](https://discord.gg/rK6U3xdr7D) [![](https://img.shields.io/badge/wiki-documentation-forestgreen)](https://zeal-operating-system.github.io/ZealOS-wiki/) [![Build SanctumOS ISOs](https://github.com/Zeal-Operating-System/SanctumOS/actions/workflows/build.yml/badge.svg)](https://github.com/Zeal-Operating-System/SanctumOS/actions/workflows/build.yml)

SanctumOS is an exploration into a different philosophy of computing based on two principles:

**The User is God (Ring 0):** The person at the keyboard has absolute, direct, and unmediated control over the entire machine. The shell, the file manager, the compiler—the entire user-facing environment—runs with the highest privilege (Ring 0). There are no layers of abstraction between the user and the hardware.

**The World is a Walled Garden (Ring 3):** Any interaction with the outside world, especially networking, is fundamentally untrustworthy. All such processes must be treated as hostile. They will run in a powerless, sandboxed prison (Ring 3), with no direct access to the system.

Our goal is not to build a "secure" OS in the modern sense, but to create a system of absolute architectural purity and user empowerment. We are building this because we can.

![](/screenshots/screenshot2.png)

SanctumOS strives to be simple, documented, and require as little of a knowledge gap as possible. One person should be able to comprehend the entire system in at least a semi-detailed way within a few days of study.

**Simplify, don't complicate; make accessible, don't obfuscate.**

Features in development include:
  - [32-bit color VBE graphics](https://github.com/TempleProgramming/HolyGL)
  - Fully-functional AHCI support
  - Network card drivers and a networking stack
  - UEFI booting via [BSD2-licensed Limine bootloader](https://github.com/limine-bootloader/limine) and [Public Domain ZealBooter prekernel](/zealbooter/src/zealbooter.c)

[Changes include](https://zeal-operating-system.github.io/Doc/ChangeLog.DD.html):
  - 60 FPS
  - VBE graphics with variable resolutions
  - Reformatted code for readability
  - Added comments and documentation
  - HolyC -> SanctumC
  - System-wide renaming for clarity

## Getting started

### Prerequisites

- For running in a VM: Intel VT-x/AMD-V acceleration enabled in your BIOS settings. (Required to virtualize any 64-bit operating system properly.)
    * If using Windows, [Hyper-V must be enabled.](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v#enable-the-hyper-v-role-through-settings)
- Working knowledge of the C programming language.

To create a Distro ISO, run the `build-iso` script. Check the Wiki guide for details on [building an ISO](https://zeal-operating-system.github.io/ZealOS-wiki/Building-an-ISO). After creating an ISO, see the Wiki guides on installing in [VirtualBox](https://zeal-operating-system.github.io/ZealOS-wiki/Installing-(Virtualbox)), [VMWare](https://zeal-operating-system.github.io/ZealOS-wiki/Installing-(VMWare)), and [bare-metal](https://zeal-operating-system.github.io/ZealOS-wiki/Installing-(Bare%E2%80%90metal)).

### Contributing

There are two ways to contribute. The first way involves everything happening inside the OS, as intended by Terry. After you've built the latest ISO, installed to a VM, made your changes, and powered off the VM, you can run the `sync` script to merge your changes to the repo.

Alternatively, you can edit repo files using an external editor, outside of the OS.

Afterwards, you can make a pull request on the `master` branch.

## Background

In around November of 2019, [VoidNV](https://web.archive.org/web/20210414181948/https://github.com/VoidNV) forked [ZenithOS](https://web.archive.org/web/20200811190005/https://github.com/VoidNV/ZenithOS) from TempleOS. [Releases of pre-git ZenithOS are currently archived on the mega.nz website.](https://mega.nz/#F!ZIEGmSRQ!qvL6Wk6THzE-dazkfT6N3Q) The repository was removed in August of 2020, and reuploaded to [ZenithOS](https://web.archive.org/web/20210630230454/https://github.com/ZenithOS/ZenithOS). The latest archived [front page](https://web.archive.org/web/20200811190005/https://github.com/VoidNV/ZenithOS/), [master.zip](https://web.archive.org/web/20200811190054/https://codeload.github.com/VoidNV/ZenithOS/zip/master), and [related links](https://web.archive.org/web/*/https://github.com/VoidNV/ZenithOS/*) can be found on archive.org.

In July of 2021, SanctumOS was forked from ZenithOS.

## Screenshots

Network Report, Gopher Client, FTP Client, GrDir, and AutoComplete, with Stars wallpaper

![](/screenshots/screenshot3.png)

32-bit color!

![](/screenshots/screenshot1.png)

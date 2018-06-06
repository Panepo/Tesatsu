---
title: Docker installation
categories:
  - 手札
  - 程設
tags:
  - 手札
  - 程設
date: 2018-06-05 16:06:05
---
This is the note for install Docker on win10

### Win 10 requirements
- Windows 10 Enterprise, Professional, or Education
- 64-bit Processor with Second Level Address Translation (SLAT).
- CPU support for VM Monitor Mode Extension (VT-c on Intel CPU's).
- Minimum of 4 GB memory.

### Pre-install
In order for Docker for Windows to function properly your machine needs:
- Hyper-V installed and working
  Open a PowerShell console as Administrator and run the following command:
  {% codeblock %}
  Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All
  {% endcodeblock %}
  When the installation has completed, reboot.
  After reboot, from the start menu, type in “Turn Windows features on or off” and hit enter. In the subequent screen, verify Hyper-V is enabled and has a checkmark.

- Virtualization enabled
  Enabled virtualizationin BIOS

### installation
- Download Docker CE for windows from docker store
- Install and run
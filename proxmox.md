---
title: Proxmox VE
description: 
published: false
date: 2022-05-31T13:37:25.858Z
tags: linux, proxmox, hypervisor, kvm, qemu, vm, virtualization, debian, windows, pve
editor: markdown
dateCreated: 2022-05-31T09:22:31.457Z
---

# Install Qemu Guest Agent
First we need to activate the Qemu guest agent for the VM on the Proxmox interface.

![proxmox_gui_activate_qemu_guest_agent.gif](/asset_guest/proxmox_gui_activate_qemu_guest_agent.gif)

Then install the Qemu guest agent on the VM.
After that you'll need to totally shutdown down the VM (not reboot) to apply the new configuration.
```bash
sudo apt install qemu-guest-agent
sudo shutdown now
```

Finally we can boot the VM and see that our changes have been applied.
![proxmox_qemu_guest_agent.png](/asset_guest/proxmox_qemu_guest_agent.png)
---
title: Booting to an Old Linux Kernel
tags: [Linux]
style: fill
color: light
description: A how-to guide for booting into a older version of the linux kernel.
---
# Reverting Linux Kernel
In November of 2022, I decided that the laptop I used throughout college was 7 years old and should be laid to rest. To learn more about how computer hardware integrates with eachother, I built a PC and set the machine up for gaming and software development. I knew I wanted to run a linux distro and decided to take Pop OS 22.04 for a spin.

Fast forward to March of 2023, I updated my machine and suddenly my wireless card is no longer able to connect to my home network. After trying a variety of troubleshooting (System 76 has a good [guide](https://support.system76.com/articles/wireless/)), I decided try reverting the kernel.

Trying out the old kernel is straight-forward, during boot - once you the system posts and you get a splash screen, hitting spacebar should bring up a couple options:
```
Pop!_OS (Pop_OS-current.conf)
Pop!_OS (Pop_OS-oldkern.conf)
Pop!_OS recovery
Reboot Into Firmware Interface
```

Navigate to `Pop_OS-oldkern.conf` and you're off to the races. The system will continue booting and you will have the old kernel loaded.

After I tested that my wireless card worked again and was satisfied with this version of the kernel, I needed to make that the default. This may be achieved with the `bootctl` utility. To list the available boot loader entries run:
```bash
sudo bootctl list
```

```console
Boot Loader Entries:
       source: /boot/efi/loader/entries/Pop_OS-current.conf
        linux: /EFI/Pop_OS-987da132-0848-4ffc-b5c0-c22152d75070/vmlinuz.efi
       initrd: /EFI/Pop_OS-987da132-0848-4ffc-b5c0-c22152d75070/initrd.img
      options: root=UUID=987da132-0848-4ffc-b5c0-c22152d75070 ro quiet loglevel=0 systemd.show_status=false splash

        title: Pop!_OS (Pop_OS-oldkern.conf)
           id: Pop_OS-oldkern.conf
       source: /boot/efi/loader/entries/Pop_OS-oldkern.conf
        linux: /EFI/Pop_OS-987da132-0848-4ffc-b5c0-c22152d75070/vmlinuz-previous.efi
       initrd: /EFI/Pop_OS-987da132-0848-4ffc-b5c0-c22152d75070/initrd.img-previous
      options: root=UUID=987da132-0848-4ffc-b5c0-c22152d75070 ro quiet loglevel=0 systemd.show_status=false splash

        title: Pop!_OS recovery
           id: Recovery-1E4A-7ED7.conf
       source: /boot/efi/loader/entries/Recovery-1E4A-7ED7.conf
        linux: /EFI/Recovery-1E4A-7ED7/vmlinuz.efi
       initrd: /EFI/Recovery-1E4A-7ED7/initrd.gz
      options: boot=casper hostname=recovery userfullname=Recovery username=recovery live-media-path=/casper-1E4A-7ED7 live-media=/dev/disk/by-partuuid/fd4e812f-981a-43dc-99a2-aa4fdc3c2fb2 noprompt modules>

        title: Reboot Into Firmware Interface
           id: auto-reboot-to-firmware-setup
       source: /sys/firmware/efi/efivars/LoaderEntries-4a67b082-0a4c-41cf-b6c7-440b29bb8c4f
```
The utility also provides a method to set the default bootloader entry.
```bash
sudo bootctl set-default Pop_OS-oldkern.conf
```
Rebooting the system and listing the bootloader entries will now show a *(default)* tag next to the entry specified from the `set-default` command:
```console
        title: Pop!_OS (Pop_OS-oldkern.conf) (default)
           id: Pop_OS-oldkern.conf
       source: /boot/efi/loader/entries/Pop_OS-oldkern.conf
        linux: /EFI/Pop_OS-987da132-0848-4ffc-b5c0-c22152d75070/vmlinuz-previous.efi
       initrd: /EFI/Pop_OS-987da132-0848-4ffc-b5c0-c22152d75070/initrd.img-previous
      options: root=UUID=987da132-0848-4ffc-b5c0-c22152d75070 ro quiet loglevel=0 systemd.show_status=false splash
```
Lastly this can be verified using 
```bash
kernelstub -p
```
```
kernelstub.Config    : INFO     Looking for configuration...
kernelstub           : INFO     System information: 

    OS:..................Pop!_OS 22.04
    Root partition:....../dev/dm-1
    Root FS UUID:........987da132-0848-4ffc-b5c0-c22152d75070
    ESP Path:............/boot/efi
    ESP Partition:......./dev/nvme0n1p1
    ESP Partition #:.....1
    NVRAM entry #:.......-1
    Boot Variable #:.....0000
    Kernel Boot Options:.quiet loglevel=0 systemd.show_status=false splash
    Kernel Image Path:.../boot/vmlinuz-6.1.11-76060111-generic
    Initrd Image Path:.../boot/initrd.img-6.1.11-76060111-generic
    Force-overwrite:.....False

kernelstub           : INFO     Configuration details: 

   ESP Location:................../boot/efi
   Management Mode:...............True
   Install Loader configuration:..True
   Configuration version:.........3
```
Or with `uname -a`
```
(This is the loading old version)
Linux pop-os 6.0.12-76060006-generic #202212290932~1673966427~22.04~e15d5b5 SMP PREEMPT_DYNAMIC Tue J x86_64 x86_64 x86_64 GNU/Linux
```
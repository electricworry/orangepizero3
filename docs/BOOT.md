# Boot logs

I've captured various boot logs.

## Orange Pi Zero2 Poky boot

A good boot from a Poky build (no changes) targetting an Orange Pi Zero2.
OrangePiZero2-poky.txt

## Orange Pi Zero3 Poky boot

This is the problem I started with when attempting to build poky for
Orange Pi Zero3:

```
U-Boot SPL 2023.07.02-g (Aug 28 2023 - 17:53:07 +0000)
DRAM:This DRAM setup is currently not supported.

resetting ...

```

## Orange Pi Zero3 boot with no SD card

The Orange Pi Zero2 comes with SPI flash and it contains a diagnosis image.

Just for curiosity here's the output. The UART is enabled and it transmits by
default at 115200 baud.

```
[53]HELLO! BOOT0 is starting!
[56]BOOT0 commit : 3ae35eb
[59]set pll start
[61]periph0 has been enabled
[64]set pll end
[67]unknow PMU
[69]unknow PMU
[73]PMU: AXP1530
[77]dram return write ok
[80]board init ok
[81]DRAM BOOT DRIVE INFO: V0.651
[85]the chip id is 0x2000
[87]chip id check OK
[98]DRAM_VCC set to 1100 mv
[100]DRAM CLK =792 MHZ
[103]DRAM Type =8 (3:DDR3,4:DDR4,7:LPDDR3,8:LPDDR4)
[114]Actual DRAM SIZE =4096 M
[117]DRAM SIZE =4096 MBytes, para1 = 310a, para2 = 10001000, dram_tpr13 = 2006c61
[130]DRAM simple test OK.
[133]rtc standby flag is 0x0, super standby flag is 0x0
[138]dram size =4096
[141]Use rtc to store dram tuning para
[146]spinor id is: 5e 40 18, read cmd: 0b
[150]Succeed in reading toc file head.
[154]The size of toc is 9c000.
[312]Entry_name        = u-boot
[317]Entry_name        = monitor
[321]Entry_name        = dtb
[325]Jump to second Boot.
NOTICE:  BL3-1: v1.0(debug):05d6c57
NOTICE:  BL3-1: Built : 13:35:35, 2021-10-28
NOTICE:  BL3-1 commit: 8
NOTICE:  cpuidle init version V2.0
ERROR:   Error initializing runtime service tspd_fast
NOTICE:  BL3-1: Preparing for EL3 exit to normal world
NOTICE:  BL3-1: Next image address = 0x4a000000
�OTICE:  BL3-1: Next image spsr = 0x1d3

U-Boot 2018.05 (Jul 10 2023 - 10:32:18 +0800) Allwinner Technology

[00.403]CPU:   Allwinner Family
[00.406]Model: sun50iw9
I2C:   ready
[00.410]DRAM:  2 GiB
[00.413]Relocation Offset is: 75f5d000
[00.433]secure enable bit: 0
[00.436]pmu_axp152_probe pmic_bus_read fail
[00.440]PMU: AXP1530
[00.445]CPU=1008 MHz,PLL6=600 Mhz,AHB=200 Mhz, APB1=100Mhz  MBus=400Mhz
[00.451]gic: sec monitor mode
[00.457]flash init start
[00.459]workmode = 0,storage type = 3
SF: Detected zb25vq128as with page size 256 Bytes, erase size 64 KiB, total 16 MiB
[00.476]sunxi flash init ok
[00.480]Loading Environment from SUNXI_FLASH... OK
[00.509]get secure storage map err
[00.512]sunxi secure storage is not supported
[00.516]usb burn from boot
delay time 0
weak:otg_phy_config
[00.529]usb prepare ok
[00.798]usb sof ok
[00.800]usb probe ok
[00.802]usb setup ok
set address 0x1a
set address 0x1a ok
[03.807]do_burn_from_boot usb : have no handshake
[03.811]get secure storage map err
[03.814]secure storage init fail
[03.819]update dts
[03.823]update part info
[03.827]update bootcmd
[03.829]No ethernet found.
Hit any key to stop autoboot:  0 
Android's image name: sun50i_arm64
[07.364]Starting kernel ...

[    0.000000] Booting Linux on physical CPU 0x0
[    0.000000] Linux version 4.9.170 (orangepi@ubuntu) (gcc version 5.3.1 20160412 (Linaro GCC 5.3-2016.05) ) #15 SMP PREEMPT Thu Jun 29 17:36:03 CST 2023
[    0.000000] Boot CPU: AArch64 Processor [410fd034]
[    0.000000] bootconsole [earlycon0] enabled

```

## Booting OrangePiOS

Booting from the OrangePiOS Opios-arch-aarch64-xfce-opizero3-23.07-linux6.1.31-4gb.img.xz
is stored in OrangePiZero3-orangepios.txt

## Booting from a build of OrangePiOS bookworm

Using https://github.com/orangepi-xulong/orangepi-build.git (commit 2dbd451) we
can build OrangePiOS on debian bookworm using 'next' 6.1 kernel and with a desktop
environment. I did this and the build output is recorded.

See OrangePiZero3-orangepios-build.txt

## Building Poky with downstream forks

If we modify the yocto build environment to use the xunlong forks, what happens?

* https://github.com/orangepi-xunlong/u-boot-orangepi.git origin/v2021.07-sunxi
* https://github.com/orangepi-xunlong/linux-orangepi.git origin/orange-pi-6.1-sun50iw9

I had to set I had to set `rootdev=mmcblk1p2` in boot.cmd to get it to boot,
but otherwise it works! This is probably an optimal boot to aim for. It's fast.

See OrangePiZero3-poky-them.txt

## Building Poky with downstream kernel

If I add back in the default poky u-boot but keeping the kernel fork, this is
what we get. It's slower but still works.

See OrangePiZero3-poky-their-kernel.txt

## Building Poky

If I add back the default poky linux-mainline (with some of my changes) then I
get this:

See OrangePiZero3-poky.txt

## Status

I'm feeling confident that u-boot is as good as it needs to be now.

Having added the dtb to linux-mainline 6.1.31, it boots but no devices work. It's a mess.

I read that with dtb inserted into linux-mainline 6.5.% it should work. Going to try.
- If it works, then u-boot must be fine.
- Can I stick with that version or do I need to go back to 6.1.31?
- I should have more confidence about going back if this works. IT DIDN'T.

Next, can I put my kernel into their image to see if I get x11? And vice versa?

* Get u-boot working faster.
* Get Linux booting into graphical.
* Why does the LED flash?
* Why is rootdev mmcblk1p2?
* Power management: u-boot/arch/arm/mach-sunxi/pmic_bus.c
* Sound
* Is GPIO there?
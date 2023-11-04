# Orange Pi Zero2 Poky boot

```
U-Boot SPL 2023.07.02-g (Jul 11 2023 - 15:20:44 +0000)
DRAM: 1024 MiB
Trying to boot from MMC1
NOTICE:  BL31: v2.9(release):v2.9.0-dirty
NOTICE:  BL31: Built : 14:12:59, May 22 2023
NOTICE:  BL31: Detected Allwinner H616 SoC (1823)
NOTICE:  BL31: Found U-Boot DTB at 0x4a096168, model: OrangePi Zero2


U-Boot 2023.07.02-g (Jul 11 2023 - 15:20:44 +0000) Allwinner Technology

CPU:   Allwinner H616 (SUN50I)
Model: OrangePi Zero2
DRAM:  1 GiB
Core:  48 devices, 18 uclasses, devicetree: separate
WDT:   Not starting watchdog@30090a0
MMC:   mmc@4020000: 0
Loading Environment from FAT... Unable to read "uboot.env" from mmc0:1... 
In:    serial@5000000
Out:   serial@5000000
Err:   serial@5000000
Net:   eth0: ethernet@5020000
Hit any key to stop autoboot:  0 
switch to partitions #0, OK
mmc0 is current device
Scanning mmc 0:1...
Found U-Boot script /boot.scr
495 bytes read in 5 ms (96.7 KiB/s)
## Executing script at 4fc00000
16325 bytes read in 3 ms (5.2 MiB/s)
26708480 bytes read in 1109 ms (23 MiB/s)
Moving Image from 0x40080000 to 0x40200000, end=41c10000
## Flattened Device Tree blob at 4fa00000
   Booting using the fdt blob at 0x4fa00000
Working FDT set to 4fa00000
   Loading Device Tree to 0000000049ff9000, end 0000000049ffffc4 ... OK
Working FDT set to 49ff9000

Starting kernel ...

[    0.000000] Booting Linux on physical CPU 0x0000000000 [0x410fd034]
[    0.000000] Linux version 6.1.31 (oe-user@oe-host) (aarch64-poky-linux-gcc (GCC) 13.2.0, GNU ld (GNU Binutils) 2.41.0.20230731) #1 SMP PREEMPT Tue May 30 13:03:33 UTC 2023
[    0.000000] Machine model: OrangePi Zero2
[    0.000000] efi: UEFI not found.
[    0.000000] NUMA: No NUMA configuration found
[    0.000000] NUMA: Faking a node at [mem 0x0000000040000000-0x000000007fffffff]
[    0.000000] NUMA: NODE_DATA [mem 0x7fde2b00-0x7fde4fff]
[    0.000000] Zone ranges:
[    0.000000]   DMA      [mem 0x0000000040000000-0x000000007fffffff]
[    0.000000]   DMA32    empty
[    0.000000]   Normal   empty
[    0.000000] Movable zone start for each node
[    0.000000] Early memory node ranges
[    0.000000]   node   0: [mem 0x0000000040000000-0x000000004003ffff]
[    0.000000]   node   0: [mem 0x0000000040040000-0x000000007fffffff]
[    0.000000] Initmem setup node 0 [mem 0x0000000040000000-0x000000007fffffff]
[    0.000000] cma: Reserved 16 MiB at 0x000000007dc00000
[    0.000000] psci: probing for conduit method from DT.
[    0.000000] psci: PSCIv1.1 detected in firmware.
[    0.000000] psci: Using standard PSCI v0.2 function IDs
[    0.000000] psci: MIGRATE_INFO_TYPE not supported.
[    0.000000] psci: SMC Calling Convention v1.2
[    0.000000] percpu: Embedded 20 pages/cpu s41192 r8192 d32536 u81920
[    0.000000] Detected VIPT I-cache on CPU0
[    0.000000] CPU features: detected: ARM erratum 845719
[    0.000000] alternatives: applying boot alternatives
[    0.000000] Fallback order for Node 0: 0 
[    0.000000] Built 1 zonelists, mobility grouping on.  Total pages: 258048
[    0.000000] Policy zone: DMA
[    0.000000] Kernel command line: console=ttyS0,115200 console=tty1 root=/dev/mmcblk0p2 rootwait panic=10
[    0.000000] Dentry cache hash table entries: 131072 (order: 8, 1048576 bytes, linear)
[    0.000000] Inode-cache hash table entries: 65536 (order: 7, 524288 bytes, linear)
[    0.000000] mem auto-init: stack:off, heap alloc:off, heap free:off
[    0.000000] Memory: 984820K/1048576K available (12736K kernel code, 2338K rwdata, 5816K rodata, 5056K init, 554K bss, 47372K reserved, 16384K cma-reserved)
[    0.000000] SLUB: HWalign=64, Order=0-3, MinObjects=0, CPUs=4, Nodes=1
[    0.000000] rcu: Preemptible hierarchical RCU implementation.
[    0.000000] rcu: 	RCU event tracing is enabled.
[    0.000000] rcu: 	RCU restricting CPUs from NR_CPUS=256 to nr_cpu_ids=4.
[    0.000000] rcu: RCU calculated value of scheduler-enlistment delay is 25 jiffies.
[    0.000000] rcu: Adjusting geometry for rcu_fanout_leaf=16, nr_cpu_ids=4
[    0.000000] NR_IRQS: 64, nr_irqs: 64, preallocated irqs: 0
[    0.000000] Root IRQ handler: gic_handle_irq
[    0.000000] GIC: Using split EOI/Deactivate mode
[    0.000000] rcu: srcu_init: Setting srcu_struct sizes based on contention.
[    0.000000] arch_timer: cp15 timer(s) running at 24.00MHz (phys).
[    0.000000] clocksource: arch_sys_counter: mask: 0xffffffffffffff max_cycles: 0x588fe9dc0, max_idle_ns: 440795202592 ns
[    0.000001] sched_clock: 56 bits at 24MHz, resolution 41ns, wraps every 4398046511097ns
[    0.000683] Console: colour dummy device 80x25
[    0.001059] printk: console [tty1] enabled
[    0.001142] Calibrating delay loop (skipped), value calculated using timer frequency.. 48.00 BogoMIPS (lpj=96000)
[    0.001169] pid_max: default: 32768 minimum: 301
[    0.001243] LSM: Security Framework initializing
[    0.001356] Mount-cache hash table entries: 2048 (order: 2, 16384 bytes, linear)
[    0.001381] Mountpoint-cache hash table entries: 2048 (order: 2, 16384 bytes, linear)
[    0.002411] cacheinfo: Unable to detect cache hierarchy for CPU 0
[    0.003155] rcu: Hierarchical SRCU implementation.
[    0.003187] rcu: 	Max phase no-delay instances is 1000.
[    0.003889] EFI services will not be available.
[    0.004270] smp: Bringing up secondary CPUs ...
[    0.004788] Detected VIPT I-cache on CPU1
[    0.004878] cacheinfo: Unable to detect cache hierarchy for CPU 1
[    0.004926] CPU1: Booted secondary processor 0x0000000001 [0x410fd034]
[    0.005551] Detected VIPT I-cache on CPU2
[    0.005635] cacheinfo: Unable to detect cache hierarchy for CPU 2
[    0.005673] CPU2: Booted secondary processor 0x0000000002 [0x410fd034]
[    0.006282] Detected VIPT I-cache on CPU3
[    0.006368] cacheinfo: Unable to detect cache hierarchy for CPU 3
[    0.006405] CPU3: Booted secondary processor 0x0000000003 [0x410fd034]
[    0.006504] smp: Brought up 1 node, 4 CPUs
[    0.006603] SMP: Total of 4 processors activated.
[    0.006616] CPU features: detected: 32-bit EL0 Support
[    0.006627] CPU features: detected: 32-bit EL1 Support
[    0.006640] CPU features: detected: CRC32 instructions
[    0.006722] CPU: All CPU(s) started at EL2
[    0.006743] alternatives: applying system-wide alternatives
[    0.008589] devtmpfs: initialized
[    0.012298] clocksource: jiffies: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 7645041785100000 ns
[    0.012354] futex hash table entries: 1024 (order: 4, 65536 bytes, linear)
[    0.012998] pinctrl core: initialized pinctrl subsystem
[    0.013905] DMI not present or invalid.
[    0.014636] NET: Registered PF_NETLINK/PF_ROUTE protocol family
[    0.015861] DMA: preallocated 128 KiB GFP_KERNEL pool for atomic allocations
[    0.016235] DMA: preallocated 128 KiB GFP_KERNEL|GFP_DMA pool for atomic allocations
[    0.016384] DMA: preallocated 128 KiB GFP_KERNEL|GFP_DMA32 pool for atomic allocations
[    0.016509] audit: initializing netlink subsys (disabled)
[    0.016753] audit: type=2000 audit(0.016:1): state=initialized audit_enabled=0 res=1
[    0.017636] thermal_sys: Registered thermal governor 'step_wise'
[    0.017719] cpuidle: using governor menu
[    0.017937] hw-breakpoint: found 6 breakpoint and 4 watchpoint registers.
[    0.018061] ASID allocator initialised with 65536 entries
[    0.018816] Serial: AMBA PL011 UART driver
[    0.021818] platform 3001000.clock: Fixed dependency cycle(s) with /soc/rtc@7000000
[    0.025708] platform 7010000.clock: Fixed dependency cycle(s) with /soc/rtc@7000000
[    0.036930] HugeTLB: registered 1.00 GiB page size, pre-allocated 0 pages
[    0.036968] HugeTLB: 0 KiB vmemmap can be freed for a 1.00 GiB page
[    0.036984] HugeTLB: registered 32.0 MiB page size, pre-allocated 0 pages
[    0.036997] HugeTLB: 0 KiB vmemmap can be freed for a 32.0 MiB page
[    0.037010] HugeTLB: registered 2.00 MiB page size, pre-allocated 0 pages
[    0.037023] HugeTLB: 0 KiB vmemmap can be freed for a 2.00 MiB page
[    0.037037] HugeTLB: registered 64.0 KiB page size, pre-allocated 0 pages
[    0.037050] HugeTLB: 0 KiB vmemmap can be freed for a 64.0 KiB page
[    0.038714] ACPI: Interpreter disabled.
[    0.039975] iommu: Default domain type: Translated 
[    0.040007] iommu: DMA domain TLB invalidation policy: strict mode 
[    0.040409] SCSI subsystem initialized
[    0.040906] usbcore: registered new interface driver usbfs
[    0.040956] usbcore: registered new interface driver hub
[    0.041000] usbcore: registered new device driver usb
[    0.041518] pps_core: LinuxPPS API ver. 1 registered
[    0.041533] pps_core: Software ver. 5.3.6 - Copyright 2005-2007 Rodolfo Giometti <giometti@linux.it>
[    0.041561] PTP clock support registered
[    0.041962] Advanced Linux Sound Architecture Driver Initialized.
[    0.042674] vgaarb: loaded
[    0.043118] clocksource: Switched to clocksource arch_sys_counter
[    0.043376] VFS: Disk quotas dquot_6.6.0
[    0.043434] VFS: Dquot-cache hash table entries: 512 (order 0, 4096 bytes)
[    0.043654] pnp: PnP ACPI: disabled
[    0.050602] NET: Registered PF_INET protocol family
[    0.050829] IP idents hash table entries: 16384 (order: 5, 131072 bytes, linear)
[    0.052056] tcp_listen_portaddr_hash hash table entries: 512 (order: 1, 8192 bytes, linear)
[    0.052163] Table-perturb hash table entries: 65536 (order: 6, 262144 bytes, linear)
[    0.052195] TCP established hash table entries: 8192 (order: 4, 65536 bytes, linear)
[    0.052278] TCP bind hash table entries: 8192 (order: 6, 262144 bytes, linear)
[    0.052526] TCP: Hash tables configured (established 8192 bind 8192)
[    0.052676] UDP hash table entries: 512 (order: 2, 16384 bytes, linear)
[    0.052738] UDP-Lite hash table entries: 512 (order: 2, 16384 bytes, linear)
[    0.052939] NET: Registered PF_UNIX/PF_LOCAL protocol family
[    0.053441] RPC: Registered named UNIX socket transport module.
[    0.053472] RPC: Registered udp transport module.
[    0.053483] RPC: Registered tcp transport module.
[    0.053494] RPC: Registered tcp NFSv4.1 backchannel transport module.
[    0.053514] PCI: CLS 0 bytes, default 64
[    0.054513] hw perfevents: enabled with armv8_cortex_a53 PMU driver, 7 counters available
[    0.054948] kvm [1]: IPA Size Limit: 40 bits
[    0.056354] kvm [1]: vgic interrupt IRQ9
[    0.056470] kvm [1]: Hyp mode initialized successfully
[    0.057942] Initialise system trusted keyrings
[    0.058271] workingset: timestamp_bits=42 max_order=18 bucket_order=0
[    0.065562] squashfs: version 4.0 (2009/01/31) Phillip Lougher
[    0.066346] NFS: Registering the id_resolver key type
[    0.066426] Key type id_resolver registered
[    0.066438] Key type id_legacy registered
[    0.066529] nfs4filelayout_init: NFSv4 File Layout Driver Registering...
[    0.066545] nfs4flexfilelayout_init: NFSv4 Flexfile Layout Driver Registering...
[    0.066784] 9p: Installing v9fs 9p2000 file system support
[    0.108895] Key type asymmetric registered
[    0.108920] Asymmetric key parser 'x509' registered
[    0.108996] Block layer SCSI generic (bsg) driver version 0.4 loaded (major 246)
[    0.109016] io scheduler mq-deadline registered
[    0.109028] io scheduler kyber registered
[    0.130884] Serial: 8250/16550 driver, 4 ports, IRQ sharing enabled
[    0.133315] SuperH (H)SCI(F) driver initialized
[    0.133684] msm_serial: driver initialized
[    0.134174] misc dump reg init
[    0.134794] cacheinfo: Unable to detect cache hierarchy for CPU 0
[    0.140973] loop: module loaded
[    0.144550] tun: Universal TUN/TAP device driver, 1.6
[    0.145522] e1000e: Intel(R) PRO/1000 Network Driver
[    0.145550] e1000e: Copyright(c) 1999 - 2015 Intel Corporation.
[    0.145625] igb: Intel(R) Gigabit Ethernet Network Driver
[    0.145641] igb: Copyright (c) 2007-2014 Intel Corporation.
[    0.145688] igbvf: Intel(R) Gigabit Virtual Function Network Driver
[    0.145702] igbvf: Copyright (c) 2009 - 2012 Intel Corporation.
[    0.145992] sky2: driver version 1.30
[    0.146507] VFIO - User Level meta-driver version: 0.3
[    0.149200] usbcore: registered new interface driver usb-storage
[    0.151918] sun6i-rtc 7000000.rtc: registered as rtc0
[    0.151984] sun6i-rtc 7000000.rtc: setting system clock to 1970-01-02T00:00:03 UTC (86403)
[    0.152109] sun6i-rtc 7000000.rtc: RTC enabled
[    0.152723] i2c_dev: i2c /dev entries driver
[    0.155036] sdhci: Secure Digital Host Controller Interface driver
[    0.155058] sdhci: Copyright(c) Pierre Ossman
[    0.155375] Synopsys Designware Multimedia Card Interface Driver
[    0.156042] sdhci-pltfm: SDHCI platform and OF driver helper
[    0.157093] ledtrig-cpu: registered to indicate activity on CPUs
[    0.157518] SMCCC: SOC_ID: ID = jep106:091e:1823 Revision = 0x00000000
[    0.158207] usbcore: registered new interface driver usbhid
[    0.158230] usbhid: USB HID core driver
[    0.160823] NET: Registered PF_PACKET protocol family
[    0.161008] 9pnet: Installing 9P2000 support
[    0.161089] Key type dns_resolver registered
[    0.161549] registered taskstats version 1
[    0.161572] Loading compiled-in X.509 certificates
[    0.176111] sun50i-h616-r-pinctrl 7022000.pinctrl: initialized sunXi PIO driver
[    0.187936] sun50i-h616-r-pinctrl 7022000.pinctrl: supply vcc-pl not found, using dummy regulator
[    0.188354] sunxi-rsb 7083000.rsb: RSB running at 3000000 Hz
[    0.188699] axp20x-rsb sunxi-rsb-745: AXP20x variant AXP806 found
[    0.192714] axp20x-rsb sunxi-rsb-745: AXP20X driver loaded
[    0.201342] sun50i-h616-pinctrl 300b000.pinctrl: initialized sunXi PIO driver
[    0.203213] printk: console [ttyS0] disabled
[    0.223610] 5000000.serial: ttyS0 at MMIO 0x5000000 (irq = 284, base_baud = 1500000) is a 16550A
[    1.314857] printk: console [ttyS0] enabled
[    1.330252] sunxi-mmc 4020000.mmc: Got CD GPIO
[    1.331970] sunxi-mmc 4021000.mmc: allocated mmc-pwrseq
[    1.337394] musb-sunxi 5100000.usb: Invalid or missing 'dr_mode' property
[    1.342175] ohci-platform 5200400.usb: Generic Platform OHCI controller
[    1.342199] ehci-platform 5200000.usb: EHCI Host Controller
[    1.342221] ehci-platform 5200000.usb: new USB bus registered, assigned bus number 1
[    1.342331] ehci-platform 5200000.usb: irq 288, io mem 0x05200000
[    1.346837] musb-sunxi: probe of 5100000.usb failed with error -22
[    1.347718] ALSA device list:
[    1.353536] ohci-platform 5200400.usb: new USB bus registered, assigned bus number 2
[    1.359092]   No soundcards found.
[    1.359132] ehci-platform 5200000.usb: USB 2.0 started, EHCI 1.00
[    1.366984] ohci-platform 5200400.usb: irq 287, io mem 0x05200400
[    1.367138] sunxi-mmc 4020000.mmc: initialized, max. request size: 16384 KB, uses new timings mode
[    1.373683] hub 1-0:1.0: USB hub found
[    1.403280] mmc0: host does not support reading read-only switch, assuming write-enable
[    1.405514] hub 1-0:1.0: 1 port detected
[    1.417702] mmc0: new high speed SDHC card at address aaaa
[    1.436403] mmcblk0: mmc0:aaaa SL16G 14.8 GiB 
[    1.443287]  mmcblk0: p1 p2
[    1.443840] hub 2-0:1.0: USB hub found
[    1.449937] hub 2-0:1.0: 1 port detected
[    1.571694] sunxi-mmc 4021000.mmc: initialized, max. request size: 16384 KB, uses new timings mode
[    1.598236] mmc1: new high speed SDIO card at address 8800
[    1.604580] EXT4-fs (mmcblk0p2): orphan cleanup on readonly fs
[    1.610534] EXT4-fs (mmcblk0p2): mounted filesystem with ordered data mode. Quota mode: none.
[    1.619192] VFS: Mounted root (ext4 filesystem) readonly on device 179:2.
[    1.626689] devtmpfs: mounted
[    1.631715] Freeing unused kernel memory: 5056K
[    1.636386] Run /sbin/init as init process
[    2.132303] udevd[151]: starting version 3.2.12
[    4.171121] random: crng init done
[    4.205469] udevd[153]: starting eudev-3.2.12
[    4.628222] EXT4-fs (mmcblk0p2): re-mounted. Quota mode: none.
Fri Mar  9 12:34:56 UTC 2018
INIT: Entering runlevel: 5
Configuring network interfaces... ip: SIOCGIFFLAGS: No such device
Starting syslogd/klogd: done

Poky (Yocto Project Reference Distro) 4.2+snapshot-c8e9590a376c0b63e38167dc522fac4cfbecb5d4 orange-pi-zero2 /dev/ttyS0

orange-pi-zero2 login:
```

# Orange Pi Zero3 Poky boot

```
U-Boot SPL 2023.07.02-g (Aug 28 2023 - 17:53:07 +0000)
DRAM:This DRAM setup is currently not supported.

resetting ...

```

# Orange Pi Zero3 boot

Details of Orange Pi Zero3 boot process. Tested here is a 4GB RAM with the
factory installed image on the SPI flash.

The UART is enabled and it transmits by default at 115200 baud.

## UART output

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

```
U-Boot SPL 2021.07-1-g10ae13dc2-dirty (Jul 10 2023 - 11:59:23 +0000)
DRAM: 4096 MiB
Trying to boot from MMC1
NOTICE:  BL31: v2.9(debug):v2.9.0-333-ge318411f0
NOTICE:  BL31: Built : 11:59:23, Jul 10 2023
NOTICE:  BL31: Detected Allwinner H616 SoC (1823)
NOTICE:  BL31: Found U-Boot DTB at 0x4a0822c0, model: OrangePi Zero3
INFO:    ARM GICv2 driver initialized
INFO:    Configuring SPC Controller
INFO:    PMIC: Probing AXP305 on RSB
ERROR:   RSB: set run-time address: 0x10003
INFO:    Could not init RSB: -65539
INFO:    BL31: Platform setup done
INFO:    BL31: Initializing runtime services
INFO:    BL31: cortex_a53: CPU workaround for 855873 was applied
INFO:    BL31: cortex_a53: CPU workaround for 1530924 was applied
INFO:    PSCI: Suspend is unavailable
INFO:    BL31: Preparing for EL3 exit to normal world
INFO:    Entry point address = 0x4a000000
INFO:    SPSR = 0x3c9
INFO:    Changed devicetree.


U-Boot 2021.07-1-g10ae13dc2-dirty (Jul 10 2023 - 11:59:23 +0000) Orange Pi

CPU:   Allwinner H616 (SUN50I)
Model: OrangePi Zero3
I2C:   ready
DRAM:  4 GiB
MMC:   mmc@4020000: 0
Loading Environment from FAT... Unable to read "uboot.env" from mmc0:1... In:    serial@5000000
Out:   serial@5000000
Err:   serial@5000000
Net:   No ethernet found.
starting USB...
No working controllers found
Autoboot in 2 seconds, press <Space> to stop
switch to partitions #0, OK
mmc0 is current device
Scanning mmc 0:1...
Found /extlinux/extlinux.conf
Retrieving file: /extlinux/extlinux.conf
222 bytes read in 2 ms (108.4 KiB/s)
1:	Orange Pi
Retrieving file: /initramfs-linux.img
7627880 bytes read in 632 ms (11.5 MiB/s)
Retrieving file: /Image
22398984 bytes read in 1852 ms (11.5 MiB/s)
append: initrd=/initramfs-linux.img console=ttyS0,115200 root=PARTUUID=2724794c-02 rw rootwait audit=0 splash plymouth.ignore-serial-consoles
Retrieving file: /dtbs/allwinner/sun50i-h616-orangepi-zero3.dtb
39163 bytes read in 6 ms (6.2 MiB/s)
Moving Image from 0x40080000 to 0x40200000, end=417e0000
## Flattened Device Tree blob at 4fa00000
   Booting using the fdt blob at 0x4fa00000
   Loading Ramdisk to 498b9000, end 49fff468 ... OK
   Loading Device Tree to 00000000498ac000, end 00000000498b88fa ... OK

Starting kernel ...

[    0.000000] Booting Linux on physical CPU 0x0000000000 [0x410fd034]
[    0.000000] Linux version 6.1.31-1+ (orangepi@orangepi) (gcc (GCC) 12.1.0, GNU ld (GNU Binutils) 2.38) #1 SMP Mon Jul 10 21:23:25 CST 2023
[    0.000000] Machine model: OrangePi Zero3
[    0.000000] NUMA: No NUMA configuration found
[    0.000000] NUMA: Faking a node at [mem 0x0000000040000000-0x000000013fffffff]
[    0.000000] NUMA: NODE_DATA [mem 0x13f7c2040-0x13f7c3fff]
[    0.000000] Zone ranges:
[    0.000000]   DMA      [mem 0x0000000040000000-0x00000000ffffffff]
[    0.000000]   DMA32    empty
[    0.000000]   Normal   [mem 0x0000000100000000-0x000000013fffffff]
[    0.000000] Movable zone start for each node
[    0.000000] Early memory node ranges
[    0.000000]   node   0: [mem 0x0000000040000000-0x000000004007ffff]
[    0.000000]   node   0: [mem 0x0000000040080000-0x000000013fffffff]
[    0.000000] Initmem setup node 0 [mem 0x0000000040000000-0x000000013fffffff]
[    0.000000] cma: Reserved 128 MiB at 0x00000000f8000000
[    0.000000] psci: probing for conduit method from DT.
[    0.000000] psci: PSCIv1.1 detected in firmware.
[    0.000000] psci: Using standard PSCI v0.2 function IDs
[    0.000000] psci: MIGRATE_INFO_TYPE not supported.
[    0.000000] psci: SMC Calling Convention v1.4
[    0.000000] percpu: Embedded 19 pages/cpu s37992 r8192 d31640 u77824
[    0.000000] Detected VIPT I-cache on CPU0
[    0.000000] CPU features: detected: ARM erratum 845719
[    0.000000] alternatives: applying boot alternatives
[    0.000000] Fallback order for Node 0: 0 
[    0.000000] Built 1 zonelists, mobility grouping on.  Total pages: 1032192
[    0.000000] Policy zone: Normal
[    0.000000] Kernel command line: initrd=/initramfs-linux.img console=ttyS0,115200 root=PARTUUID=2724794c-02 rw rootwait audit=0 splash plymouth.ignore-serial-consoles
[    0.000000] audit: disabled (until reboot)
[    0.000000] Unknown kernel command line parameters "splash", will be passed to user space.
[    0.000000] printk: log_buf_len individual max cpu contribution: 131072 bytes
[    0.000000] printk: log_buf_len total cpu_extra contributions: 393216 bytes
[    0.000000] printk: log_buf_len min size: 131072 bytes
[    0.000000] printk: log_buf_len: 524288 bytes
[    0.000000] printk: early log buf free: 128920(98%)
[    0.000000] Dentry cache hash table entries: 524288 (order: 10, 4194304 bytes, linear)
[    0.000000] Inode-cache hash table entries: 262144 (order: 9, 2097152 bytes, linear)
[    0.000000] mem auto-init: stack:off, heap alloc:off, heap free:off
[    0.000000] software IO TLB: area num 4.
[    0.000000] software IO TLB: mapped [mem 0x00000000f4000000-0x00000000f8000000] (64MB)
[    0.000000] Memory: 3883796K/4194304K available (13888K kernel code, 1458K rwdata, 3724K rodata, 2688K init, 499K bss, 179436K reserved, 131072K cma-reserved)
[    0.000000] SLUB: HWalign=64, Order=0-3, MinObjects=0, CPUs=4, Nodes=1
[    0.000000] rcu: Hierarchical RCU implementation.
[    0.000000] rcu: 	RCU restricting CPUs from NR_CPUS=8 to nr_cpu_ids=4.
[    0.000000] 	Tracing variant of Tasks RCU enabled.
[    0.000000] rcu: RCU calculated value of scheduler-enlistment delay is 25 jiffies.
[    0.000000] rcu: Adjusting geometry for rcu_fanout_leaf=16, nr_cpu_ids=4
[    0.000000] NR_IRQS: 64, nr_irqs: 64, preallocated irqs: 0
[    0.000000] Root IRQ handler: gic_handle_irq
[    0.000000] GIC: Using split EOI/Deactivate mode
[    0.000000] rcu: srcu_init: Setting srcu_struct sizes based on contention.
[    0.000000] arch_timer: cp15 timer(s) running at 24.00MHz (phys).
[    0.000000] clocksource: arch_sys_counter: mask: 0xffffffffffffff max_cycles: 0x588fe9dc0, max_idle_ns: 440795202592 ns
[    0.000001] sched_clock: 56 bits at 24MHz, resolution 41ns, wraps every 4398046511097ns
[    0.000528] Console: colour dummy device 80x25
[    0.000615] Calibrating delay loop (skipped), value calculated using timer frequency.. 48.00 BogoMIPS (lpj=96000)
[    0.000628] pid_max: default: 32768 minimum: 301
[    0.000693] LSM: Security Framework initializing
[    0.000720] Yama: becoming mindful.
[    0.000812] AppArmor: AppArmor initialized
[    0.000898] Mount-cache hash table entries: 8192 (order: 4, 65536 bytes, linear)
[    0.000921] Mountpoint-cache hash table entries: 8192 (order: 4, 65536 bytes, linear)
[    0.001908] cacheinfo: Unable to detect cache hierarchy for CPU 0
[    0.002468] cblist_init_generic: Setting adjustable number of callback queues.
[    0.002477] cblist_init_generic: Setting shift to 2 and lim to 1.
[    0.002633] rcu: Hierarchical SRCU implementation.
[    0.002636] rcu: 	Max phase no-delay instances is 1000.
[    0.003691] smp: Bringing up secondary CPUs ...
[    0.004225] Detected VIPT I-cache on CPU1
[    0.004299] cacheinfo: Unable to detect cache hierarchy for CPU 1
[    0.004335] CPU1: Booted secondary processor 0x0000000001 [0x410fd034]
[    0.004820] Detected VIPT I-cache on CPU2
[    0.004873] cacheinfo: Unable to detect cache hierarchy for CPU 2
[    0.004891] CPU2: Booted secondary processor 0x0000000002 [0x410fd034]
[    0.005335] Detected VIPT I-cache on CPU3
[    0.005390] cacheinfo: Unable to detect cache hierarchy for CPU 3
[    0.005408] CPU3: Booted secondary processor 0x0000000003 [0x410fd034]
[    0.005465] smp: Brought up 1 node, 4 CPUs
[    0.005473] SMP: Total of 4 processors activated.
[    0.005477] CPU features: detected: 32-bit EL0 Support
[    0.005481] CPU features: detected: CRC32 instructions
[    0.005544] CPU: All CPU(s) started at EL2
[    0.005546] alternatives: applying system-wide alternatives
[    0.007984] devtmpfs: initialized
[    0.013816] Registered cp15_barrier emulation handler
[    0.013827] Registered setend emulation handler
[    0.013970] clocksource: jiffies: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 7645041785100000 ns
[    0.013988] futex hash table entries: 1024 (order: 4, 65536 bytes, linear)
[    0.018867] pinctrl core: initialized pinctrl subsystem
[    0.020134] NET: Registered PF_NETLINK/PF_ROUTE protocol family
[    0.021187] DMA: preallocated 512 KiB GFP_KERNEL pool for atomic allocations
[    0.021393] DMA: preallocated 512 KiB GFP_KERNEL|GFP_DMA pool for atomic allocations
[    0.021561] DMA: preallocated 512 KiB GFP_KERNEL|GFP_DMA32 pool for atomic allocations
[    0.021948] thermal_sys: Registered thermal governor 'fair_share'
[    0.021953] thermal_sys: Registered thermal governor 'bang_bang'
[    0.021956] thermal_sys: Registered thermal governor 'step_wise'
[    0.021960] thermal_sys: Registered thermal governor 'user_space'
[    0.021994] cpuidle: using governor menu
[    0.022162] hw-breakpoint: found 6 breakpoint and 4 watchpoint registers.
[    0.022238] ASID allocator initialised with 65536 entries
[    0.022361] Serial: AMBA PL011 UART driver
[    0.026828] platform 3001000.clock: Fixed dependency cycle(s) with /soc/rtc@7000000
[    0.030734] platform 6000000.hdmi: Fixed dependency cycle(s) with /soc/tcon-top@6510000
[    0.031184] platform 6510000.tcon-top: Fixed dependency cycle(s) with /soc/lcd-controller@6515000
[    0.031200] platform 6510000.tcon-top: Fixed dependency cycle(s) with /soc/bus@1000000/mixer@100000
[    0.031829] platform 7010000.clock: Fixed dependency cycle(s) with /soc/rtc@7000000
[    0.033064] platform 6000000.hdmi: Fixed dependency cycle(s) with /connector
[    0.034532] KASLR disabled due to lack of seed
[    0.040258] HugeTLB: registered 1.00 GiB page size, pre-allocated 0 pages
[    0.040264] HugeTLB: 0 KiB vmemmap can be freed for a 1.00 GiB page
[    0.040270] HugeTLB: registered 32.0 MiB page size, pre-allocated 0 pages
[    0.040274] HugeTLB: 0 KiB vmemmap can be freed for a 32.0 MiB page
[    0.040278] HugeTLB: registered 2.00 MiB page size, pre-allocated 0 pages
[    0.040282] HugeTLB: 0 KiB vmemmap can be freed for a 2.00 MiB page
[    0.040286] HugeTLB: registered 64.0 KiB page size, pre-allocated 0 pages
[    0.040290] HugeTLB: 0 KiB vmemmap can be freed for a 64.0 KiB page
[    0.040961] cryptd: max_cpu_qlen set to 1000
[    0.108157] raid6: neonx8   gen()  1950 MB/s
[    0.176230] raid6: neonx4   gen()  1914 MB/s
[    0.244315] raid6: neonx2   gen()  1832 MB/s
[    0.312392] raid6: neonx1   gen()  1569 MB/s
[    0.380452] raid6: int64x8  gen()  1216 MB/s
[    0.448530] raid6: int64x4  gen()  1351 MB/s
[    0.516612] raid6: int64x2  gen()  1201 MB/s
[    0.584687] raid6: int64x1  gen()   890 MB/s
[    0.584691] raid6: using algorithm neonx8 gen() 1950 MB/s
[    0.652739] raid6: .... xor() 1424 MB/s, rmw enabled
[    0.652743] raid6: using neon recovery algorithm
[    0.653997] iommu: Default domain type: Translated 
[    0.654002] iommu: DMA domain TLB invalidation policy: strict mode 
[    0.654251] SCSI subsystem initialized
[    0.654409] usbcore: registered new interface driver usbfs
[    0.654441] usbcore: registered new interface driver hub
[    0.654466] usbcore: registered new device driver usb
[    0.654736] pps_core: LinuxPPS API ver. 1 registered
[    0.654739] pps_core: Software ver. 5.3.6 - Copyright 2005-2007 Rodolfo Giometti <giometti@linux.it>
[    0.654752] PTP clock support registered
[    0.655037] ARM FF-A: FFA_VERSION returned not supported
[    0.655326] Advanced Linux Sound Architecture Driver Initialized.
[    0.655902] NetLabel: Initializing
[    0.655905] NetLabel:  domain hash size = 128
[    0.655908] NetLabel:  protocols = UNLABELED CIPSOv4 CALIPSO
[    0.655968] NetLabel:  unlabeled traffic allowed by default
[    0.655971] mctp: management component transport protocol core
[    0.655975] NET: Registered PF_MCTP protocol family
[    0.656329] clocksource: Switched to clocksource arch_sys_counter
[    0.656524] VFS: Disk quotas dquot_6.6.0
[    0.656561] VFS: Dquot-cache hash table entries: 512 (order 0, 4096 bytes)
[    0.657082] AppArmor: AppArmor Filesystem Enabled
[    0.663250] NET: Registered PF_INET protocol family
[    0.663471] IP idents hash table entries: 65536 (order: 7, 524288 bytes, linear)
[    0.666742] tcp_listen_portaddr_hash hash table entries: 2048 (order: 3, 32768 bytes, linear)
[    0.666791] Table-perturb hash table entries: 65536 (order: 6, 262144 bytes, linear)
[    0.666807] TCP established hash table entries: 32768 (order: 6, 262144 bytes, linear)
[    0.667062] TCP bind hash table entries: 32768 (order: 8, 1048576 bytes, linear)
[    0.668300] TCP: Hash tables configured (established 32768 bind 32768)
[    0.668447] UDP hash table entries: 2048 (order: 4, 65536 bytes, linear)
[    0.668537] UDP-Lite hash table entries: 2048 (order: 4, 65536 bytes, linear)
[    0.668760] NET: Registered PF_UNIX/PF_LOCAL protocol family
[    0.669355] Trying to unpack rootfs image as initramfs...
[    0.677429] hw perfevents: enabled with armv8_cortex_a53 PMU driver, 7 counters available
[    0.679026] Initialise system trusted keyrings
[    0.679085] Key type blacklist registered
[    0.679227] workingset: timestamp_bits=44 max_order=20 bucket_order=0
[    0.684095] zbud: loaded
[    0.685480] squashfs: version 4.0 (2009/01/31) Phillip Lougher
[    0.687396] integrity: Platform Keyring initialized
[    0.729437] xor: measuring software checksum speed
[    0.733998]    8regs           :  2168 MB/sec
[    0.738556]    32regs          :  2169 MB/sec
[    0.743416]    arm64_neon      :  2029 MB/sec
[    0.743420] xor: using function: 32regs (2169 MB/sec)
[    0.743432] async_tx: api initialized (async)
[    0.743443] Key type asymmetric registered
[    0.743447] Asymmetric key parser 'x509' registered
[    0.996997] Freeing initrd memory: 7448K
[    1.012969] alg: self-tests for CTR-KDF (hmac(sha256)) passed
[    1.013097] Block layer SCSI generic (bsg) driver version 0.4 loaded (major 247)
[    1.013205] io scheduler mq-deadline registered
[    1.013210] io scheduler kyber registered
[    1.013392] io scheduler bfq registered
[    1.025836] Serial: 8250/16550 driver, 6 ports, IRQ sharing disabled
[    1.028000] misc dump reg init
[    1.031012] cacheinfo: Unable to detect cache hierarchy for CPU 0
[    1.034664] loop: module loaded
[    1.037300] usbcore: registered new interface driver usb-storage
[    1.037695] mousedev: PS/2 mouse device common for all mice
[    1.038576] sun6i-rtc 7000000.rtc: registered as rtc0
[    1.038599] sun6i-rtc 7000000.rtc: setting system clock to 1970-01-02T00:00:06 UTC (86406)
[    1.038690] sun6i-rtc 7000000.rtc: RTC enabled
[    1.038888] i2c_dev: i2c /dev entries driver
[    1.039111] mv64xxx_i2c 7081400.i2c: can't get pinctrl, bus recovery not supported
[    1.039581] axp20x-i2c 0-0036: AXP20x variant AXP313a found
[    1.039733] axp20x-regulator axp20x-regulator: DCDC frequency on AXP313a is fixed to 3 MHz.
[    1.039739] axp20x-regulator axp20x-regulator: Error setting dcdc frequency: -22
[    1.049871] axp20x-i2c 0-0036: AXP20X driver loaded
[    1.050569] sunxi-wdt 30090a0.watchdog: Watchdog enabled (timeout=16 sec, nowayout=0)
[    1.051836] sdhci: Secure Digital Host Controller Interface driver
[    1.051840] sdhci: Copyright(c) Pierre Ossman
[    1.051861] Synopsys Designware Multimedia Card Interface Driver
[    1.052519] sdhci-pltfm: SDHCI platform and OF driver helper
[    1.052886] ledtrig-cpu: registered to indicate activity on CPUs
[    1.053139] SMCCC: SOC_ID: ID = jep106:091e:1823 Revision = 0x00000002
[    1.053564] hid: raw HID events driver (C) Jiri Kosina
[    1.053638] usbcore: registered new interface driver usbhid
[    1.053643] usbhid: USB HID core driver
[    1.097489] NET: Registered PF_INET6 protocol family
[    1.113042] Segment Routing with IPv6
[    1.113119] In-situ OAM (IOAM) with IPv6
[    1.113226] NET: Registered PF_PACKET protocol family
[    1.113321] 8021q: 802.1Q VLAN Support v1.8
[    1.113455] 9pnet: Installing 9P2000 support
[    1.113543] Key type dns_resolver registered
[    1.114013] registered taskstats version 1
[    1.114043] Loading compiled-in X.509 certificates
[    1.117372] Loaded X.509 cert 'Build time autogenerated kernel key: 3d54b579c95c44efa6440ffff0165f7f2f735423'
[    1.119539] zswap: loaded using pool zstd/z3fold
[    1.119891] Key type .fscrypt registered
[    1.119895] Key type fscrypt-provisioning registered
[    1.120836] Btrfs loaded, crc32c=crc32c-generic, zoned=yes, fsverity=no
[    1.121050] Key type encrypted registered
[    1.121062] AppArmor: AppArmor sha1 policy hashing enabled
[    1.121085] ima: No TPM chip found, activating TPM-bypass!
[    1.121106] ima: Allocated hash algorithm: sha1
[    1.121134] ima: No architecture policies found
[    1.121172] evm: Initialising EVM extended attributes:
[    1.121175] evm: security.selinux
[    1.121178] evm: security.SMACK64
[    1.121181] evm: security.SMACK64EXEC
[    1.121184] evm: security.SMACK64TRANSMUTE
[    1.121187] evm: security.SMACK64MMAP
[    1.121190] evm: security.apparmor
[    1.121193] evm: security.ima
[    1.121196] evm: security.capability
[    1.121199] evm: HMAC attrs: 0x1
[    1.143597] sun50i-h616-pinctrl 300b000.pinctrl: initialized sunXi PIO driver
[    1.144115] sun50i-h616-r-pinctrl 7022000.pinctrl: initialized sunXi PIO driver
[    1.144375] sun50i-h616-pinctrl 300b000.pinctrl: supply vcc-ph not found, using dummy regulator
[    1.144854] printk: console [ttyS0] disabled
[    1.144925] 5000000.serial: ttyS0 at MMIO 0x5000000 (irq = 285, base_baud = 1500000) is a 16550A
[    2.501679] printk: console [ttyS0] enabled
[    2.506650] debugfs: Directory '1100000.mixer' with parent 'regmap' already present!
[    2.514421] debugfs: Directory '1100000.mixer' with parent 'regmap' already present!
[    2.537481] sun4i-drm display-engine: bound 1100000.mixer (ops 0xffff800008e86368)
[    2.545203] sun4i-drm display-engine: bound 6510000.tcon-top (ops 0xffff800008e8ab40)
[    2.553276] sun4i-drm display-engine: bound 6515000.lcd-controller (ops 0xffff800008e83340)
[    2.561686] sun8i-dw-hdmi 6000000.hdmi: supply hvcc not found, using dummy regulator
[    2.569647] sun8i-dw-hdmi 6000000.hdmi: Detected HDMI TX controller v2.12a with HDCP (DWC HDMI 2.0 TX PHY)
[    2.579677] sun8i-dw-hdmi 6000000.hdmi: registered DesignWare HDMI I2C bus driver
[    2.587547] sun4i-drm display-engine: bound 6000000.hdmi (ops 0xffff800008e85428)
[    2.595396] [drm] Initialized sun4i-drm 1.0.0 20150629 for display-engine on minor 0
[    2.860191] Console: switching to colour frame buffer device 240x67
[    2.966445] sun4i-drm display-engine: [drm] fb0: sun4i-drmdrmfb frame buffer device
[    2.974820] sun50i-h616-pinctrl 300b000.pinctrl: supply vcc-pc not found, using dummy regulator
[    2.984960] spi-nor spi0.0: ZB25VQ128A (16384 Kbytes)
[    3.002849] sun50i-cpufreq-nvmem: will use speed0 CPU OPPs
[    3.012588] cpufreq: cpufreq_online: CPU0: Running at unlisted initial frequency: 1032000 KHz, changing to: 1200000 KHz
[    3.023532] OF: /thermal-zones/gpu-thermal/cooling-maps/map0: could not get #cooling-cells for /soc/gpu@1800000
[    3.033624] thermal_sys: Add a cooling_device property with at least one device
[    3.040931] thermal thermal_zone0: binding zone gpu-thermal with cdev cpufreq-cpu0 failed:-2
[    3.049710] sun50i-h616-pinctrl 300b000.pinctrl: supply vcc-pg not found, using dummy regulator
[    3.059090] sun50i-h616-pinctrl 300b000.pinctrl: supply vcc-pf not found, using dummy regulator
[    3.060114] sunxi-mmc 4021000.mmc: allocated mmc-pwrseq
[    3.061356] usb_phy_generic usb_phy_generic.4.auto: supply vcc not found, using dummy regulator
[    3.061418] usb_phy_generic usb_phy_generic.4.auto: dummy supplies not allowed for exclusive requests
[    3.062134] ehci-platform 5200000.usb: EHCI Host Controller
[    3.062150] ehci-platform 5200000.usb: new USB bus registered, assigned bus number 1
[    3.062241] ehci-platform 5200000.usb: irq 292, io mem 0x05200000
[    3.062550] ehci-platform 5310000.usb: EHCI Host Controller
[    3.062561] ehci-platform 5310000.usb: new USB bus registered, assigned bus number 2
[    3.062613] ehci-platform 5310000.usb: irq 293, io mem 0x05310000
[    3.062902] ehci-platform 5311000.usb: EHCI Host Controller
[    3.062912] ehci-platform 5311000.usb: new USB bus registered, assigned bus number 3
[    3.062967] ehci-platform 5311000.usb: irq 294, io mem 0x05311000
[    3.063231] ohci-platform 5200400.usb: Generic Platform OHCI controller
[    3.063242] ohci-platform 5200400.usb: new USB bus registered, assigned bus number 4
[    3.063315] ohci-platform 5200400.usb: irq 295, io mem 0x05200400
[    3.063585] ohci-platform 5310400.usb: Generic Platform OHCI controller
[    3.063595] ohci-platform 5310400.usb: new USB bus registered, assigned bus number 5
[    3.063639] ohci-platform 5310400.usb: irq 296, io mem 0x05310400
[    3.063916] ohci-platform 5311400.usb: Generic Platform OHCI controller
[    3.063926] ohci-platform 5311400.usb: new USB bus registered, assigned bus number 6
[    3.063966] ohci-platform 5311400.usb: irq 297, io mem 0x05311400
[    3.076339] ehci-platform 5200000.usb: USB 2.0 started, EHCI 1.00
[    3.082528] sunxi-mmc 4020000.mmc: Got CD GPIO
[    3.091097] usb usb1: New USB device found, idVendor=1d6b, idProduct=0002, bcdDevice= 6.01
[    3.092332] ehci-platform 5310000.usb: USB 2.0 started, EHCI 1.00
[    3.105209] ALSA device list:
[    3.108324] ehci-platform 5311000.usb: USB 2.0 started, EHCI 1.00
[    3.110351] usb usb1: New USB device strings: Mfr=3, Product=2, SerialNumber=1
[    3.115915]   #0: audiocodec
[    3.123645] usb usb1: Product: EHCI Host Controller
[    3.129726]   #1: ahubdam
[    3.135291] usb usb1: Manufacturer: Linux 6.1.31-1+ ehci_hcd
[    3.143018]   #2: ahubhdmi
[    3.149102] usb usb1: SerialNumber: 5200000.usb
[    3.155860] sunxi-mmc 4020000.mmc: initialized, max. request size: 16384 KB, uses new timings mode
[    3.163739] hub 1-0:1.0: USB hub found
[    3.205359] mmc1: host does not support reading read-only switch, assuming write-enable
[    3.210393] hub 1-0:1.0: 1 port detected
[    3.221786] mmc1: new high speed SDHC card at address aaaa
[    3.229523] usb usb2: New USB device found, idVendor=1d6b, idProduct=0002, bcdDevice= 6.01
[    3.235779] mmcblk1: mmc1:aaaa SL16G 14.8 GiB 
[    3.238206] usb usb2: New USB device strings: Mfr=3, Product=2, SerialNumber=1
[    3.249524]  mmcblk1: p1 p2
[    3.251503] usb usb2: Product: EHCI Host Controller
[    3.312864] sunxi-mmc 4021000.mmc: initialized, max. request size: 16384 KB, uses new timings mode
[    3.313058] usb usb2: Manufacturer: Linux 6.1.31-1+ ehci_hcd
[    3.334176] mmc0: new high speed SDIO card at address 8800
[    3.341302] usb usb2: SerialNumber: 5310000.usb
[    3.357230] hub 2-0:1.0: USB hub found
[    3.361010] hub 2-0:1.0: 1 port detected
[    3.365264] usb usb4: New USB device found, idVendor=1d6b, idProduct=0001, bcdDevice= 6.01
[    3.373535] usb usb4: New USB device strings: Mfr=3, Product=2, SerialNumber=1
[    3.380758] usb usb4: Product: Generic Platform OHCI controller
[    3.386682] usb usb4: Manufacturer: Linux 6.1.31-1+ ohci_hcd
[    3.392344] usb usb4: SerialNumber: 5200400.usb
[    3.397225] hub 4-0:1.0: USB hub found
[    3.401025] hub 4-0:1.0: 1 port detected
[    3.405331] usb usb5: New USB device found, idVendor=1d6b, idProduct=0001, bcdDevice= 6.01
[    3.413599] usb usb5: New USB device strings: Mfr=3, Product=2, SerialNumber=1
[    3.420818] usb usb5: Product: Generic Platform OHCI controller
[    3.426738] usb usb5: Manufacturer: Linux 6.1.31-1+ ohci_hcd
[    3.432395] usb usb5: SerialNumber: 5310400.usb
[    3.437168] hub 5-0:1.0: USB hub found
[    3.440945] hub 5-0:1.0: 1 port detected
[    3.445164] usb usb6: New USB device found, idVendor=1d6b, idProduct=0001, bcdDevice= 6.01
[    3.453433] usb usb6: New USB device strings: Mfr=3, Product=2, SerialNumber=1
[    3.460657] usb usb6: Product: Generic Platform OHCI controller
[    3.466582] usb usb6: Manufacturer: Linux 6.1.31-1+ ohci_hcd
[    3.472244] usb usb6: SerialNumber: 5311400.usb
[    3.477129] hub 6-0:1.0: USB hub found
[    3.480929] hub 6-0:1.0: 1 port detected
[    3.485294] usb usb3: New USB device found, idVendor=1d6b, idProduct=0002, bcdDevice= 6.01
[    3.493567] usb usb3: New USB device strings: Mfr=3, Product=2, SerialNumber=1
[    3.500797] usb usb3: Product: EHCI Host Controller
[    3.505679] usb usb3: Manufacturer: Linux 6.1.31-1+ ehci_hcd
[    3.511339] usb usb3: SerialNumber: 5311000.usb
[    3.516197] hub 3-0:1.0: USB hub found
[    3.520027] hub 3-0:1.0: 1 port detected
[    3.525429] Freeing unused kernel memory: 2688K
[    3.530060] Run /init as init process
:: running early hook [udev]
Starting systemd-udevd version 253.5-2-arch
:: running hook [udev]
:: Triggering uevents...
:: running hook [keymap]
:: Loading keymap...kbd_mode: KDSKBMODE: Inappropriate ioctl for device
done.
:: performing fsck on 'PARTUUID=2724794c-02'
ROOT_OPIOS: recovering journal
ROOT_OPIOS: clean, 268565/956592 files, 1203055/3827035 blocks
:: mounting 'PARTUUID=2724794c-02' on real root
[    6.472336] EXT4-fs (mmcblk1p2): mounted filesystem with ordered data mode. Quota mode: none.
:: running cleanup hook [udev]
[    7.187527] systemd[1]: System time before build time, advancing clock.
[    7.335186] systemd[1]: systemd 253.5-2-arch running in system mode (+PAM +AUDIT -SELINUX -APPARMOR -IMA +SMACK +SECCOMP +GCRYPT +GNUTLS +OPENSSL +ACL +BLKID +CURL +ELFUTILS +FIDO2 +IDN2 -IDN +IPTC +KMOD +LIBCRYPTSETUP +LIBFDISK +PCRE2 -PWQUALITY +P11KIT -QRENCODE +TPM2 +BZIP2 +LZ4 +XZ +ZLIB +ZSTD +BPF_FRAMEWORK +XKBCOMMON +UTMP -SYSVINIT default-hierarchy=unified)
[    7.367519] systemd[1]: Detected architecture arm64.

Welcome to Orange OS!

[    7.405583] systemd[1]: Hostname set to <orange-os>.
[    7.624378] systemd[1]: bpf-lsm: BPF LSM hook not enabled in the kernel, BPF LSM not supported
[    8.118636] systemd[1]: /usr/lib/systemd/system/opizero3-post-install.service:10: Support for option SysVStartPriority= has been removed and it is ignored
[    8.303901] systemd[1]: Queued start job for default target Graphical Interface.
[    8.340247] systemd[1]: Created slice Slice /system/getty.
[  OK  ] Created slice Slice /system/getty.
[    8.362956] systemd[1]: Created slice Slice /system/modprobe.
[  OK  ] Created slice Slice /system/modprobe.
[    8.386798] systemd[1]: Created slice Slice /system/serial-getty.
[  OK  ] Created slice Slice /system/serial-getty.
[    8.410150] systemd[1]: Created slice User and Session Slice.
[  OK  ] Created slice User and Session Slice.
[    8.433227] systemd[1]: Started Forward Password Requests to Wall Directory Watch.
[  OK  ] Started Forward Password R…uests to Wall Directory Watch.
[    8.458036] systemd[1]: Set up automount Arbitrary Executable File Formats File System Automount Point.
[  OK  ] Set up automount Arbitrary…s File System Automount Point.
[    8.485129] systemd[1]: Reached target Local Integrity Protected Volumes.
[  OK  ] Reached target Local Integrity Protected Volumes.
[    8.509112] systemd[1]: Reached target Remote Encrypted Volumes.
[  OK  ] Reached target Remote Encrypted Volumes.
[    8.532693] systemd[1]: Reached target Remote File Systems.
[  OK  ] Reached target Remote File Systems.
[    8.552422] systemd[1]: Reached target Slice Units.
[  OK  ] Reached target Slice Units.
[    8.572616] systemd[1]: Reached target Swaps.
[  OK  ] Reached target Swaps.
[    8.592899] systemd[1]: Reached target Local Verity Protected Volumes.
[  OK  ] Reached target Local Verity Protected Volumes.
[    8.617452] systemd[1]: Listening on Device-mapper event daemon FIFOs.
[  OK  ] Listening on Device-mapper event daemon FIFOs.
[    8.651567] systemd[1]: Listening on LVM2 poll daemon socket.
[  OK  ] Listening on LVM2 poll daemon socket.
[    8.687474] systemd[1]: Listening on Process Core Dump Socket.
[  OK  ] Listening on Process Core Dump Socket.
[    8.733252] systemd[1]: Journal Audit Socket was skipped because of an unmet condition check (ConditionSecurity=audit).
[    8.745051] systemd[1]: Listening on Journal Socket (/dev/log).
[  OK  ] Listening on Journal Socket (/dev/log).
[    8.769353] systemd[1]: Listening on Journal Socket.
[  OK  ] Listening on Journal Socket.
[    8.789011] systemd[1]: Listening on Network Service Netlink Socket.
[  OK  ] Listening on Network Service Netlink Socket.
[    8.813433] systemd[1]: Listening on udev Control Socket.
[  OK  ] Listening on udev Control Socket.
[    8.837456] systemd[1]: Listening on udev Kernel Socket.
[  OK  ] Listening on udev Kernel Socket.
[    8.861545] systemd[1]: Listening on User Database Manager Socket.
[  OK  ] Listening on User Database Manager Socket.
[    8.908970] systemd[1]: Mounting Huge Pages File System...
         Mounting Huge Pages File System...
[    8.932508] systemd[1]: Mounting POSIX Message Queue File System...
         Mounting POSIX Message Queue File System...
[    8.980775] systemd[1]: Mounting Kernel Debug File System...
         Mounting Kernel Debug File System...
[    9.001083] systemd[1]: Kernel Trace File System was skipped because of an unmet condition check (ConditionPathExists=/sys/kernel/tracing).
[    9.021424] systemd[1]: Mounting Temporary Directory /tmp...
         Mounting Temporary Directory /tmp...
[    9.045411] systemd[1]: Starting Create List of Static Device Nodes...
         Starting Create List of Static Device Nodes...
[    9.088923] systemd[1]: Starting Monitoring of LVM2 mirrors, snapshots etc. using dmeventd or progress polling...
         Starting Monitoring of LVM…meventd or progress polling...
[    9.127190] systemd[1]: Starting Load Kernel Module configfs...
         Starting Load Kernel Module configfs...
[    9.153742] systemd[1]: Starting Load Kernel Module dm_mod...
         Starting Load Kernel Module dm_mod...
[    9.201214] systemd[1]: Starting Load Kernel Module drm...
         Starting Load Kernel Module drm...
[    9.231503] systemd[1]: Starting Load Kernel Module efi_pstore...
         Starting Load Kernel Module efi_pstore...
[    9.245050] device-mapper: core: CONFIG_IMA_DISABLE_HTABLE is disabled. Duplicate IMA measurements will not be recorded in the IMA log.
[    9.257775] device-mapper: ioctl: 4.47.0-ioctl (2022-07-28) initialised: dm-devel@redhat.com
[    9.261391] systemd[1]: Starting Load Kernel Module fuse...
         Starting Load Kernel Module fuse...
[    9.313205] systemd[1]: Starting Load Kernel Module loop...
         Starting Load Kernel Module loop...
[    9.325094] fuse: init (API version 7.37)
[    9.339054] systemd[1]: Starting Journal Service...
         Starting Journal Service...
[    9.389071] systemd[1]: Starting Load Kernel Modules...
         Starting Load Kernel Modules...
[    9.410642] systemd-journald[271]: Collecting audit messages is disabled.
[    9.421038] systemd[1]: Starting Generate network units from Kernel command line...
         Starting Generate network …ts from Kernel command line..[    9.435545] Asymmetric key parser 'pkcs8' registered
.
[    9.452625] systemd[1]: TPM2 PCR Machine ID Measurement was skipped because of an unmet condition check (ConditionPathExists=/sys/firmware/efi/efivars/StubPcrKernelImage-4a67b082-0a4c-41cf-b6c7-440b29bb8c4f).
[    9.474854] systemd[1]: Starting Remount Root and Kernel File Systems...
         Startin[    9.483474] WCN: marlin_init entry!
g Remou[    9.487545] WCN: wcn config bt wake host
nt Root and Kern[    9.492617] WCN_ERR: dts node for bt_wake not found
el File Systems WCN: marlin2 parse_dt some para not config
[0m...
[    9.505170] sdiohal:sdiohal_parse_dt adma_tx:1, adma_rx:1, pwrseq:0, irq type:data, gpio_num:0, blksize:840
[    9.519505] sdiohal:sdiohal_init ok
[    9.520268] systemd[1]: Starting Coldplug All udev Devices...
[    9.523634] WCN: marlin_probe ok!
         Starting Coldplug All udev Devices...
[    9.552211] systemd[1]: Starting Setup Virtual Console...
         Starting Setup Virtual Console...
[    9.584551] systemd[1]: Started Journal Service.
[  OK  ] Started Journal Service.
[  OK  ] Mounted Huge Pages [    9.617883] cfg80211: Loading compiled-in X.509 certificates for regulatory database
File System.[    9.627933] cfg80211: Loaded X.509 cert 'sforshee: 00b28ddf47aef9cea7'

[  OK  ] Mounted POSIX Message Queue File System.
[  OK  ] Mounted Kernel Debug File System.
[  OK  ] Mounted Temporary Directory /tmp.
[    9.690968] WCN: start_marlin [MARLIN_WIFI]
[    9.695187] WCN: marlin power state:0, subsys: [MARLIN_WIFI] power 1
[    9.701551] WCN: the first power on start
[  OK  ] Finished Create List of Static Device Nodes.
[  OK  ] Finished Load Kernel Module configfs.
[  OK  ] Finished Load Kernel Module dm_mod.
[  OK  ] Finished Load Kernel Module drm.
[  OK  ] Finished Load Kernel Module efi_pstore.
[  OK  ] Finished Load Kernel Module fuse.
[    9.808338] WCN: marlin chip en dummy pull up -- need manually set GPIO 
[  OK  ] Finished Load Kernel Module loop.
[  OK  ] Finished Generate network units from Kernel command[    9.840349] sdiohal:sdiohal_scan_card
 line.
[    9.844638] sdiohal:sdiohal_probe: func->class=0, vendor=0x0000, device=0x0000, func_num=0x0001, clock=50000000
[    9.856072] WCN: marlin_get_wcn_chipid: chipid: 0x2355b001
[    9.861573] WCN: marlin_scan_finish!
[    9.865157] sdiohal:probe ok
[    9.868153] sdiohal:scan end!
[    9.871128] WCN: then marlin start to download
[FAILED[    9.875659] WCN: marlin_request_firmware from /lib/firmware/wcnmodem.bin start!
] Failed to start Remount Root and Kernel File Systems.
See 'systemctl status systemd-remount-fs.service' for details.
[  OK  ] Finished Setup Virtual Console.
[  OK  ] Finished Coldplug All udev Devices.
[  OK  ] Reached target Preparation for Network.
         Mounting FUSE Control File System...
         Mounting Kernel Configuration File System...
         Starting Flush Journal to Persistent Storage...
[   10.065248] systemd-journald[271]: Received client request to flush runtime journal.
         Starting Load/Save OS Random S[   10.076685] systemd-journald[271]: File /var/log/journal/719742114f7742d78bcac449fde4c2f4/system.journal corrupted or uncleanly shut down, renaming and replacing.
eed...
         Starting Create Static Device Nodes in /dev...
[   10.164350] random: crng init done
[  OK  ] Mounted FUSE Control File System.
[  OK  ] Mounted Kernel Configuration File System.
[  OK  ] Finished Load/Save OS Random Seed.
[  OK  ] Finished Flush Journal to Persistent Storage.
[  OK  ] Finished Monitoring of LVM… dmeventd or progress polling.
         Starting User Database Manager...
[  OK  ] Started User Database Manager.
[  OK  ] Finished Create Static Device Nodes in /dev.
[  OK  ] Reached target Preparation for Local File Systems.
[  OK  ] Reached target Containers.
         Starting Rule-based Manage…for Device Events and Files...
[  OK  ] Started Rule-based Manager for Device Events and Files.
         Starting Show Plymouth Boot Screen...
[  OK  ] Listening on Load/Save RF …itch Status /dev/rfkill Watch.
[   11.073142] WCN: combin_img 0 marlin_firmware_write finish and successful
[   11.083045] WCN: marlin_start_run read reset reg val:0x1
[   11.088563] WCN: after do marlin_start_run reset reg val:0x0
[   11.097478] WCN: s_marlin_bootup_time=11097475749
[   11.107504] WCN: clock mode: TSX
[   11.124772] WCN: marlin_write_cali_data sync init_state:0x34b948e2
[   11.156693] WCN: marlin_write_cali_data sync init_state:0xf0f0f0f1
[   11.163202] WCN: sdio_config bt_wake_host trigger:[high]
[   11.168568] WCN: sdio_config irq:[inband]
[   11.172796] WCN: sdio_config wake_host_level_duration_time:[20ms]
[   11.179005] WCN: sdio_config wake_host_data_separation:[bt/wifi reuse]
[   11.185758] WCN: marlin_send_sdio_config_to_cp sdio_config:0x80f01 (enable config)
[   11.196841] WCN: marlin_write_cali_data finish
[   11.203878] WCN: check_cp_ready sync val:0xf0f0f0f2, prj_type val:0x0
[   11.236589] WCN: check_cp_ready sync val:0xf0f0f0f2, prj_type val:0x0
[   11.268564] WCN: check_cp_ready sync val:0xf0f0f0f2, prj_type val:0x0
[   11.300611] WCN: check_cp_ready sync val:0xf0f0f0f2, prj_type val:0x0
[   11.332690] WCN: check_cp_ready sync val:0xf0f0f0ff, prj_type val:0x0
[   11.339204] sdiohal:sdiohal_runtime_get entry
[   11.347162] WCN: get_cp2_version entry!
[   11.388177] WCN: WCND at cmd read:WCN_VER:Platform Version:MARLIN3_19B_W21.05.3~Project Version:sc2355_marlin3_lite_ott~12-15-2021 11:26:33~
[   11.401694] WCN: switch_cp2_log - close entry!
[   11.407554] WCN: WCND at cmd read:OK
[   11.416581] WCN: then marlin download finished and run ok
[   11.422081] WCN: start_loopcheck
[   11.448065] WCN: get_board_ant_num [one_ant]
[   11.452449] wifi ini path = /lib/firmware/wifi_2355b001_1ant.ini
[   11.492221] sprdwl:sprdwl_get_fw_info length mismatch: len_count=83, r_len=89
[   11.499520] sprdwl:sprdwl_get_fw_info, drv_version=1, fw_version=2, compat_ver=0
[   11.507004] sprdwl:chip_model:0x2355, chip_ver:0x0
[   11.511863] sprdwl:fw_ver:0, fw_std:0x7f, fw_capa:0x120f7f
[   11.517382] sprdwl:mac_addr:e0:51:d8:67:98:ae
[   11.521790] sprdwl:credit_capa:TX_WITH_CREDIT
[   11.526197] sprdwl:ott support:0
[   11.545335] mc: Linux media interface: v0.10
[   11.565726] sun50i-h616-pinctrl 300b000.pinctrl: supply vcc-pi not found, using dummy regulator
[   11.585699] dwmac-sun8i 5020000.ethernet: IRQ eth_wake_irq not found
[   11.592219] dwmac-sun8i 5020000.ethernet: IRQ eth_lpi not found
[   11.598325] dwmac-sun8i 5020000.ethernet: No regulator found
[   11.604247] dwmac-sun8i 5020000.ethernet: PTP uses main clock
[   11.610099] dwmac-sun8i 5020000.ethernet: Current syscon value is not the default 58000 (expect 0)
[   11.619528] dwmac-sun8i 5020000.ethernet: No HW DMA feature register supported
[   11.626866] dwmac-sun8i 5020000.ethernet: RX Checksum Offload Engine supported
[   11.631854] videodev: Linux video capture interface: v2.00
[   11.634123] dwmac-sun8i 5020000.ethernet: COE Type 2
[   11.634132] dwmac-sun8i 5020000.ethernet: TX Checksum insertion supported
[   11.634137] dwmac-sun8i 5020000.ethernet: Normal descriptors
[   11.657073] dwmac-sun8i 5020000.ethernet: Chain mode enabled
[   11.658334] FAT-fs (mmcblk1p1): Volume was not properly unmounted. Some data may be corrupt. Please run fsck.
[   11.663451] unisoc_wifi unisoc_wifi wlan0: mixed HW and IP checksum settings.
[   11.730186] mtty_probe init device addr: 0x000000005beb0dea
[   11.736061] -->rfkill_bluetooth_init
[   11.741073] bluetooth_set_power: start_block=1
[   11.745567] WCN: marlin power state:4, subsys: [MARLIN_BLUETOOTH] power 0
[   11.752369] WCN: can not power off, other module is on
[   11.757509] bluetooth_set_power: end_block=1
[   11.761809] <--rfkill_bluetooth_init
[   11.868153] sunxi_cedrus: module is from the staging directory, the quality is unknown, you have been warned.
[   11.903444] cedrus 1c0e000.video-codec: Device registered as /dev/video0
[   11.966828] Registered IR keymap rc-empty
[   11.971053] rc rc0: sunxi-ir as /devices/platform/soc/7040000.ir/rc/rc0
[   12.022706] rc rc0: lirc_dev: driver sunxi-ir registered at minor = 0, raw IR receiver, no transmitter
[   12.032730] input: sunxi-ir as /devices/platform/soc/7040000.ir/rc/rc0/input0
[   12.090880] sunxi-ir 7040000.ir: initialized sunXi IR driver
[   12.262979] bluetooth_set_power: start_block=0
[   12.267548] WCN: start_marlin [MARLIN_BLUETOOTH]
[   12.272256] WCN: marlin power state:4, subsys: [MARLIN_BLUETOOTH] power 1
[   12.272268] WCN: marlin have open, GNSS is closed
[   12.272271] bluetooth_set_power: end_block=0
[   12.302937] dwmac-sun8i 5020000.ethernet end0: renamed from eth0
[   13.394080] bluetooth_set_power: start_block=0
[   13.398747] WCN: start_marlin [MARLIN_BLUETOOTH]
[   13.403490] WCN: marlin power state:5, subsys: [MARLIN_BLUETOOTH] power 1
[   13.410426] WCN: marlin have open, GNSS is closed
[   13.415251] bluetooth_set_power: end_block=0
[   13.471454] mtty_open device success!
[   13.738834] Bluetooth: Core ver 2.22
[   13.742577] NET: Registered PF_BLUETOOTH protocol family
[   13.747941] Bluetooth: HCI device and connection manager initialized
[   13.754362] Bluetooth: HCI socket layer initialized
[   13.759268] Bluetooth: L2CAP socket layer initialized
[   13.764404] Bluetooth: SCO socket layer initialized
[   13.883721] Bluetooth: HCI UART driver ver 2.3
[   13.888244] Bluetooth: HCI UART protocol H4 registered
[   13.893427] Bluetooth: HCI UART protocol BCSP registered
[   13.898873] Bluetooth: HCI UART protocol LL registered
[   13.904028] Bluetooth: HCI UART protocol ATH3K registered
[   13.909535] Bluetooth: HCI UART protocol Three-wire (H5) registered
[   13.916171] Bluetooth: HCI UART protocol Intel registered
[   13.921796] Bluetooth: HCI UART protocol Broadcom registered
[   13.927562] Bluetooth: HCI UART protocol QCA registered
[   13.932816] Bluetooth: HCI UART protocol AG6XX registered
[   13.938354] Bluetooth: HCI UART protocol Marvell registered
[   15.127808] Bluetooth: BNEP (Ethernet Emulation) ver 1.3
[   15.133184] Bluetooth: BNEP filters: protocol multicast
[   15.138473] Bluetooth: BNEP socket layer initialized
[   15.151154] Bluetooth: MGMT ver 1.22
[   15.218229] NET: Registered PF_ALG protocol family
[   16.394954] dwmac-sun8i 5020000.ethernet end0: Register MEM_TYPE_PAGE_POOL RxQ-0
[   16.404491] dwmac-sun8i 5020000.ethernet end0: PHY [stmmac-0:01] driver [YT8531 Gigabit Ethernet] (irq=POLL)
[   16.414696] dwmac-sun8i 5020000.ethernet end0: No Safety Features support found
[   16.422035] dwmac-sun8i 5020000.ethernet end0: No MAC Management Counters available
[   16.429735] dwmac-sun8i 5020000.ethernet end0: PTP not supported by HW
[   16.437154] dwmac-sun8i 5020000.ethernet end0: configuring for phy/rgmii link mode

Arch Linux 6.1.31-1+ (ttyS0)

orange-os login: [   32.006402] hdmi-audio-codec hdmi-audio-codec.2.auto: Only one simultaneous stream supported!
[   32.015019] hdmi-audio-codec hdmi-audio-codec.2.auto: ASoC: error at snd_soc_dai_startup on i2s-hifi: -22
[   32.024639]  ahub_plat-i2s-hifi: ASoC: error at __soc_pcm_open on ahub_plat-i2s-hifi: -22
[   33.819154] Bluetooth: RFCOMM TTY layer initialized
[   33.824140] Bluetooth: RFCOMM socket layer initialized
[   33.829367] Bluetooth: RFCOMM ver 1.11
[   38.443958] bluetooth_set_power: start_block=0
[   38.448491] WCN: start_marlin [MARLIN_BLUETOOTH]
[   38.453150] WCN: marlin power state:5, subsys: [MARLIN_BLUETOOTH] power 1
[   38.459970] WCN: marlin have open, GNSS is closed
[   38.464690] bluetooth_set_power: end_block=0
```

## OrangePiOS partition layout

Looking at the Zero3 distro:

* MS-DOS partition table
  * 213.6M FAT32
  * 4.9G ext4

Bootstrap code:
```
00000000   FA B8 00 10  8E D0 BC 00  B0 B8 00 00  8E D8 8E C0  FB BE 00 7C  BF 00 06 B9  00 02 F3 A4  EA 21 06 00  00 BE BE 07  38 04 75 0B  83 C6 10 81  FE FE 07 75  F3 EB 16 B4  ...................|.........!......8.u........u....
00000034   02 B0 01 BB  00 7C B2 80  8A 74 01 8B  4C 02 CD 13  EA 00 7C 00  00 EB FE 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  .....|...t..L.....|.................................
00000068   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  ....................................................
0000009C   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  ....................................................
000000D0   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  ....................................................
00000104   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  ....................................................
00000138   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  ....................................................
0000016C   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  ....................................................
000001A0   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  4C 79 24 27  00 00                                                                         ........................Ly$'..
```

The Zero2 distro is identical.



```
00000000   FA B8 00 10  8E D0 BC 00  B0 B8 00 00  8E D8 8E C0  FB BE 00 7C  BF 00 06 B9  00 02 F3 A4  EA 21 06 00  00 BE BE 07  38 04 75 0B  83 C6 10 81  FE FE 07 75  F3 EB 16 B4  ...................|.........!......8.u........u....
00000034   02 B0 01 BB  00 7C B2 80  8A 74 01 8B  4C 02 CD 13  EA 00 7C 00  00 EB FE 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  .....|...t..L.....|.................................
00000068   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  ....................................................
0000009C   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  ....................................................
000000D0   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  ....................................................
00000104   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  ....................................................
00000138   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  ....................................................
0000016C   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  ....................................................
000001A0   00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  00 00 00 00  20 94 10 2B  00 00                                                                         ........................ ..+.....z.d..$........d....
```
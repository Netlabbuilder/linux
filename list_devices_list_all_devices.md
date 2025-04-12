To list all devices with a more comprehensive vieww of all connected devices (including USB, PCI, and other hardware), use the following commands:

- `sudo lshw`

  ```
  [hungtx@linux ~]$ sudo lshw
  linux.netlabbuilder.net     
      description: Notebook
      product: X550LD (ASUS-NotebookSKU)
      vendor: ASUSTeK COMPUTER INC.
      version: 1.0
      serial: E4N0CV036141149
      width: 64 bits
      capabilities: smbios-2.7 dmi-2.7 smp vsyscall32
      configuration: boot=normal chassis=notebook family=X sku=ASUS-NotebookSKU uuid=613f7f40-b807-81e3-2b8e-40167e86aac1
    *-core
         description: Motherboard
         product: X550LD
         vendor: ASUSTeK COMPUTER INC.
         physical id: 0
         version: 1.0
         serial: BSN12345678901234567
         slot: MIDDLE
       *-firmware
            description: BIOS
            vendor: American Megatrends Inc.
            physical id: 0
            version: X550LD.300
            date: 01/17/2014
            size: 64KiB
            capacity: 6MiB
            capabilities: pci upgrade shadowing cdboot bootselect socketedrom edd int13floppy1200 int13floppy720 int13floppy2880 int5printscreen int9keyboard int14serial int17printer acpi usb smartbattery biosbootspecification uefi
       *-cpu
            description: CPU
            product: Intel(R) Core(TM) i5-4200U CPU @ 1.60GHz
            vendor: Intel Corp.
            physical id: 7
            bus info: cpu@0
            version: 6.69.1
            slot: SOCKET 0
            size: 2544MHz
            capacity: 3800MHz
            width: 64 bits
            clock: 100MHz
            capabilities: lm fpu fpu_exception wp vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx pdpe1gb rdtscp x86-64 constant_tsc arch_perfmon pebs bts rep_good nopl xtopology nonstop_tsc cpuid aperfmperf pni pclmulqdq dtes64 monitor ds_cpl vmx est tm2 ssse3 sdbg fma cx16 xtpr pdcm pcid sse4_1 sse4_2 movbe popcnt tsc_deadline_timer aes xsave avx f16c rdrand lahf_lm abm cpuid_fault epb pti ssbd ibrs ibpb stibp tpr_shadow flexpriority ept vpid ept_ad fsgsbase tsc_adjust bmi1 avx2 smep bmi2 erms invpcid xsaveopt dtherm ida arat pln pts vnmi md_clear flush_l1d cpufreq
            configuration: cores=2 enabledcores=2 microcode=38 threads=4
          *-cache:0
               description: L2 cache
               physical id: 8
               slot: CPU Internal L2
               size: 512KiB
               capacity: 512KiB
               capabilities: internal write-back unified
               configuration: level=2
          *-cache:1
               description: L1 cache
               physical id: 9
               slot: CPU Internal L1
               size: 128KiB
               capacity: 128KiB
               capabilities: internal write-back
               configuration: level=1
          *-cache:2
               description: L3 cache
               physical id: a
               slot: CPU Internal L3
               size: 3MiB
               capacity: 3MiB
               capabilities: internal write-back unified
               configuration: level=3
       *-memory
            description: System Memory
            physical id: b
            slot: System board or motherboard
            size: 12GiB
          *-bank:0
               description: SODIMM DDR3 Synchronous 1600 MHz (0.6 ns)
               vendor: Elpida
               physical id: 0
               serial: 00000000
               slot: ChannelA-DIMM0
               size: 4GiB
               width: 64 bits
               clock: 1600MHz (0.6ns)
          *-bank:1
               description: DIMM [empty]
               product: [Empty]
               vendor: [Empty]
               physical id: 1
               serial: [Empty]
               slot: ChannelA-DIMM1
          *-bank:2
               description: SODIMM DDR3 Synchronous 1600 MHz (0.6 ns)
               vendor: 0000
               physical id: 2
               serial: 00000000
               slot: ChannelB-DIMM0
               size: 8GiB
               width: 64 bits
               clock: 1600MHz (0.6ns)
          *-bank:3
               description: DIMM [empty]
               product: [Empty]
               vendor: [Empty]
               physical id: 3
               serial: [Empty]
               slot: ChannelB-DIMM1
       *-pci
            description: Host bridge
            product: Haswell-ULT DRAM Controller
            vendor: Intel Corporation
            physical id: 100
            bus info: pci@0000:00:00.0
            version: 09
            width: 32 bits
            clock: 33MHz
            configuration: driver=hsw_uncore
            resources: irq:0
          *-display
               description: VGA compatible controller
               product: Haswell-ULT Integrated Graphics Controller
               vendor: Intel Corporation
               physical id: 2
               bus info: pci@0000:00:02.0
               logical name: /dev/fb0
               version: 09
               width: 64 bits
               clock: 33MHz
               capabilities: msi pm vga_controller bus_master cap_list rom fb
               configuration: depth=32 driver=i915 latency=0 resolution=1366,768
               resources: irq:48 memory:f7400000-f77fffff memory:d0000000-dfffffff ioport:f000(size=64) memory:c0000-dffff
          *-multimedia:0
               description: Audio device
               product: Haswell-ULT HD Audio Controller
               vendor: Intel Corporation
               physical id: 3
               bus info: pci@0000:00:03.0
               logical name: card0
               logical name: /dev/snd/controlC0
               logical name: /dev/snd/hwC0D0
               logical name: /dev/snd/pcmC0D3p
               logical name: /dev/snd/pcmC0D7p
               logical name: /dev/snd/pcmC0D8p
               version: 09
               width: 64 bits
               clock: 33MHz
               capabilities: pm msi pciexpress bus_master cap_list
               configuration: driver=snd_hda_intel latency=0
               resources: irq:51 memory:f7a1c000-f7a1ffff
             *-input:0
                  product: HDA Intel HDMI HDMI/DP,pcm=3
                  physical id: 0
                  logical name: input21
                  logical name: /dev/input/event14
             *-input:1
                  product: HDA Intel HDMI HDMI/DP,pcm=7
                  physical id: 1
                  logical name: input22
                  logical name: /dev/input/event15
             *-input:2
                  product: HDA Intel HDMI HDMI/DP,pcm=8
                  physical id: 2
                  logical name: input23
                  logical name: /dev/input/event16
          *-generic:0
               description: Signal processing controller
               product: Haswell-ULT Thermal Subsystem
               vendor: Intel Corporation
               physical id: 4
               bus info: pci@0000:00:04.0
               version: 09
               width: 64 bits
               clock: 33MHz
               capabilities: msi pm bus_master cap_list
               configuration: driver=proc_thermal latency=0
               resources: irq:16 memory:f7a10000-f7a17fff
          *-usb:0
               description: USB controller
               product: 8 Series USB xHCI HC
               vendor: Intel Corporation
               physical id: 14
               bus info: pci@0000:00:14.0
               version: 04
               width: 64 bits
               clock: 33MHz
               capabilities: pm msi xhci bus_master cap_list
               configuration: driver=xhci_hcd latency=0
               resources: irq:44 memory:f7a00000-f7a0ffff
             *-usbhost:0
                  product: xHCI Host Controller
                  vendor: Linux 5.14.0-503.34.1.el9_5.x86_64 xhci-hcd
                  physical id: 0
                  bus info: usb@1
                  logical name: usb1
                  version: 5.14
                  capabilities: usb-2.00
                  configuration: driver=hub slots=9 speed=480Mbit/s
                *-usb:0 UNCLAIMED
                     description: Generic USB device
                     product: Edimax AC600 USB
                     vendor: Realtek
                     physical id: 2
                     bus info: usb@1:2
                     version: 2.00
                     serial: 00e04c000001
                     capabilities: usb-2.10
                     configuration: maxpower=500mA speed=480Mbit/s
                *-usb:1
                     description: Video
                     product: USB2.0 HD UVC WebCam
                     vendor: Chicony Electronics Co.,Ltd.
                     physical id: 5
                     bus info: usb@1:5
                     version: 69.64
                     serial: 0x0001
                     capabilities: usb-2.00
                     configuration: driver=uvcvideo maxpower=500mA speed=480Mbit/s
                *-usb:2
                     description: Bluetooth wireless interface
                     product: Bluetooth Radio
                     vendor: Realtek
                     physical id: 6
                     bus info: usb@1:6
                     version: 2.00
                     serial: 00e04c000001
                     capabilities: bluetooth usb-2.10
                     configuration: driver=btusb maxpower=500mA speed=12Mbit/s
             *-usbhost:1
                  product: xHCI Host Controller
                  vendor: Linux 5.14.0-503.34.1.el9_5.x86_64 xhci-hcd
                  physical id: 1
                  bus info: usb@3
                  logical name: usb3
                  version: 5.14
                  capabilities: usb-3.00
                  configuration: driver=hub slots=4 speed=5000Mbit/s
          *-communication
               description: Communication controller
               product: 8 Series HECI #0
               vendor: Intel Corporation
               physical id: 16
               bus info: pci@0000:00:16.0
               version: 04
               width: 64 bits
               clock: 33MHz
               capabilities: pm msi bus_master cap_list
               configuration: driver=mei_me latency=0
               resources: irq:50 memory:f7a25000-f7a2501f
          *-multimedia:1
               description: Audio device
               product: 8 Series HD Audio Controller
               vendor: Intel Corporation
               physical id: 1b
               bus info: pci@0000:00:1b.0
               logical name: card1
               logical name: /dev/snd/controlC1
               logical name: /dev/snd/hwC1D0
               logical name: /dev/snd/pcmC1D0c
               logical name: /dev/snd/pcmC1D0p
               version: 04
               width: 64 bits
               clock: 33MHz
               capabilities: pm msi pciexpress bus_master cap_list
               configuration: driver=snd_hda_intel latency=0
               resources: irq:52 memory:f7a18000-f7a1bfff
             *-input:0
                  product: HDA Intel PCH Mic
                  physical id: 0
                  logical name: input24
                  logical name: /dev/input/event17
             *-input:1
                  product: HDA Intel PCH Headphone
                  physical id: 1
                  logical name: input25
                  logical name: /dev/input/event18
          *-pci:0
               description: PCI bridge
               product: 8 Series PCI Express Root Port 1
               vendor: Intel Corporation
               physical id: 1c
               bus info: pci@0000:00:1c.0
               version: e4
               width: 32 bits
               clock: 33MHz
               capabilities: pci pciexpress msi pm normal_decode bus_master cap_list
               configuration: driver=pcieport
               resources: irq:40
          *-pci:1
               description: PCI bridge
               product: 8 Series PCI Express Root Port 3
               vendor: Intel Corporation
               physical id: 1c.2
               bus info: pci@0000:00:1c.2
               version: e4
               width: 32 bits
               clock: 33MHz
               capabilities: pci pciexpress msi pm normal_decode bus_master cap_list
               configuration: driver=pcieport
               resources: irq:41 ioport:e000(size=4096) memory:f7900000-f79fffff
             *-generic
                  description: MMC Host
                  product: RTL8411B PCI Express Card Reader
                  vendor: Realtek Semiconductor Co., Ltd.
                  physical id: 0
                  bus info: pci@0000:02:00.0
                  logical name: mmc0
                  version: 01
                  width: 32 bits
                  clock: 33MHz
                  capabilities: pm msi pciexpress msix vpd bus_master cap_list rom
                  configuration: driver=rtsx_pci latency=0
                  resources: irq:45 memory:f7915000-f7915fff memory:f7900000-f790ffff
             *-network
                  description: Ethernet interface
                  product: RTL8111/8168/8211/8411 PCI Express Gigabit Ethernet Controller
                  vendor: Realtek Semiconductor Co., Ltd.
                  physical id: 0.1
                  bus info: pci@0000:02:00.1
                  logical name: enp2s0f1
                  version: 12
                  serial: 40:16:7e:86:aa:c1
                  capacity: 1Gbit/s
                  width: 64 bits
                  clock: 33MHz
                  capabilities: pm msi pciexpress msix vpd bus_master cap_list ethernet physical tp mii 10bt 10bt-fd 100bt 100bt-fd 1000bt-fd autonegotiation
                  configuration: autonegotiation=on broadcast=yes driver=r8169 driverversion=5.14.0-503.34.1.el9_5.x86_64 firmware=rtl8411-2_0.0.1 07/08/13 latency=0 link=no multicast=yes port=twisted pair
                  resources: irq:18 ioport:e000(size=256) memory:f7914000-f7914fff memory:f7910000-f7913fff
          *-pci:2
               description: PCI bridge
               product: 8 Series PCI Express Root Port 4
               vendor: Intel Corporation
               physical id: 1c.3
               bus info: pci@0000:00:1c.3
               version: e4
               width: 32 bits
               clock: 33MHz
               capabilities: pci pciexpress msi pm normal_decode bus_master cap_list
               configuration: driver=pcieport
               resources: irq:42 ioport:d000(size=4096) memory:f7800000-f78fffff
             *-network
                  description: Ethernet interface
                  product: RTL8821AE 802.11ac PCIe Wireless Network Adapter
                  vendor: Realtek Semiconductor Co., Ltd.
                  physical id: 0
                  bus info: pci@0000:03:00.0
                  logical name: wlp3s0
                  version: 00
                  serial: 54:27:1e:23:94:3b
                  width: 64 bits
                  clock: 33MHz
                  capabilities: pm msi pciexpress bus_master cap_list ethernet physical
                  configuration: broadcast=yes driver=rtl8821ae driverversion=5.14.0-503.34.1.el9_5.x86_64 firmware=N/A ip=192.168.178.25 latency=0 link=yes multicast=yes
                  resources: irq:53 ioport:d000(size=256) memory:f7800000-f7803fff
          *-pci:3
               description: PCI bridge
               product: 8 Series PCI Express Root Port 5
               vendor: Intel Corporation
               physical id: 1c.4
               bus info: pci@0000:00:1c.4
               version: e4
               width: 32 bits
               clock: 33MHz
               capabilities: pci pciexpress msi pm normal_decode bus_master cap_list
               configuration: driver=pcieport
               resources: irq:43 ioport:c000(size=4096) memory:f6000000-f70fffff ioport:e0000000(size=301989888)
             *-display
                  description: 3D controller
                  product: GF117M [GeForce 610M/710M/810M/820M / GT 620M/625M/630M/720M]
                  vendor: NVIDIA Corporation
                  physical id: 0
                  bus info: pci@0000:04:00.0
                  version: a1
                  width: 64 bits
                  clock: 33MHz
                  capabilities: pm msi pciexpress bus_master cap_list rom
                  configuration: driver=nouveau latency=0
                  resources: irq:49 memory:f6000000-f6ffffff memory:e0000000-efffffff memory:f0000000-f1ffffff ioport:c000(size=128) memory:f7000000-f707ffff
          *-usb:1
               description: USB controller
               product: 8 Series USB EHCI #1
               vendor: Intel Corporation
               physical id: 1d
               bus info: pci@0000:00:1d.0
               version: 04
               width: 32 bits
               clock: 33MHz
               capabilities: pm debug ehci bus_master cap_list
               configuration: driver=ehci-pci latency=0
               resources: irq:23 memory:f7a23000-f7a233ff
             *-usbhost
                  product: EHCI Host Controller
                  vendor: Linux 5.14.0-503.34.1.el9_5.x86_64 ehci_hcd
                  physical id: 1
                  bus info: usb@2
                  logical name: usb2
                  version: 5.14
                  capabilities: usb-2.00
                  configuration: driver=hub slots=2 speed=480Mbit/s
                *-usb
                     description: USB hub
                     product: Integrated Rate Matching Hub
                     vendor: Intel Corp.
                     physical id: 1
                     bus info: usb@2:1
                     version: 0.04
                     capabilities: usb-2.00
                     configuration: driver=hub slots=8 speed=480Mbit/s
                   *-usb
                        description: Keyboard
                        product: MOSART Semi. 2.4G Keyboard Mouse
                        vendor: MOSART Semi.
                        physical id: 3
                        bus info: usb@2:1.3
                        logical name: input12
                        logical name: /dev/input/event4
                        logical name: input12::capslock
                        logical name: input12::numlock
                        logical name: input12::scrolllock
                        logical name: input13
                        logical name: /dev/input/event5
                        logical name: /dev/input/mouse0
                        logical name: input14
                        logical name: /dev/input/event6
                        logical name: input15
                        logical name: /dev/input/event7
                        logical name: input16
                        logical name: /dev/input/event8
                        version: 1.02
                        capabilities: usb-1.10 usb
                        configuration: driver=usbhid maxpower=100mA speed=12Mbit/s
          *-isa
               description: ISA bridge
               product: 8 Series LPC Controller
               vendor: Intel Corporation
               physical id: 1f
               bus info: pci@0000:00:1f.0
               version: 04
               width: 32 bits
               clock: 33MHz
               capabilities: isa bus_master cap_list
               configuration: driver=lpc_ich latency=0
               resources: irq:0
             *-pnp00:00
                  product: PnP device PNP0c01
                  physical id: 0
                  capabilities: pnp
                  configuration: driver=system
             *-pnp00:01
                  product: PnP device PNP0c02
                  physical id: 1
                  capabilities: pnp
                  configuration: driver=system
             *-pnp00:02
                  product: PnP device PNP0b00
                  physical id: 2
                  capabilities: pnp
                  configuration: driver=rtc_cmos
             *-pnp00:03
                  product: PnP device INT3f0d
                  vendor: Interphase Corporation
                  physical id: 3
                  capabilities: pnp
                  configuration: driver=system
             *-pnp00:04
                  product: PnP device PNP0c02
                  physical id: 4
                  capabilities: pnp
                  configuration: driver=system
             *-pnp00:05
                  product: PnP device PNP0c02
                  physical id: 5
                  capabilities: pnp
                  configuration: driver=system
             *-pnp00:06
                  product: PnP device ETD0108
                  vendor: ELAN MICROELECTRONICS CORPORATION
                  physical id: 6
                  capabilities: pnp
                  configuration: driver=i8042 aux
             *-pnp00:07
                  product: PnP device ATK3001
                  vendor: Allied Telesyn Int'l
                  physical id: 7
                  capabilities: pnp
                  configuration: driver=i8042 kbd
             *-pnp00:08
                  product: PnP device PNP0c02
                  physical id: 8
                  capabilities: pnp
                  configuration: driver=system
             *-pnp00:09
                  product: PnP device PNP0c02
                  physical id: 9
                  capabilities: pnp
                  configuration: driver=system
             *-pnp00:0a
                  product: PnP device PNP0c02
                  physical id: a
                  capabilities: pnp
                  configuration: driver=system
          *-sata
               description: SATA controller
               product: 8 Series SATA Controller 1 [AHCI mode]
               vendor: Intel Corporation
               physical id: 1f.2
               bus info: pci@0000:00:1f.2
               logical name: scsi0
               logical name: scsi1
               version: 04
               width: 32 bits
               clock: 66MHz
               capabilities: sata msi pm ahci_1.0 bus_master cap_list emulated
               configuration: driver=ahci latency=0
               resources: irq:47 ioport:f0b0(size=8) ioport:f0a0(size=4) ioport:f090(size=8) ioport:f080(size=4) ioport:f060(size=32) memory:f7a22000-f7a227ff
             *-disk
                  description: ATA Disk
                  product: TOSHIBA MQ01ABF0
                  vendor: Toshiba
                  physical id: 0
                  bus info: scsi@0:0.0.0
                  logical name: /dev/sda
                  version: 1J
                  serial: 34GGCTO7T
                  size: 465GiB (500GB)
                  capabilities: gpt-1.00 partitioned partitioned:gpt
                  configuration: ansiversion=5 guid=98cd8176-fdce-41b9-88b9-a31ff9efb63c logicalsectorsize=512 sectorsize=4096
                *-volume:0
                     description: Windows FAT volume
                     vendor: MSDOS5.0
                     physical id: 1
                     bus info: scsi@0:0.0.0,1
                     logical name: /dev/sda1
                     logical name: /boot/efi
                     version: FAT32
                     serial: 6434-198d
                     size: 95MiB
                     capacity: 99MiB
                     capabilities: boot nomount fat initialized
                     configuration: FATs=2 filesystem=fat label=SYSTEM mount.fstype=vfat mount.options=rw,relatime,fmask=0077,dmask=0077,codepage=437,iocharset=ascii,shortname=winnt,errors=remount-ro name=EFI System Partition state=mounted
                *-volume:1
                     description: Windows NTFS volume
                     vendor: Windows
                     physical id: 2
                     bus info: scsi@0:0.0.0,2
                     logical name: /dev/sda2
                     version: 3.1
                     serial: fe2b-660e
                     size: 894MiB
                     capacity: 899MiB
                     capabilities: boot precious nomount ntfs initialized
                     configuration: clustersize=4096 created=2014-04-03 08:37:22 filesystem=ntfs label=Recovery name=Basic data partition state=clean
                *-volume:2
                     description: reserved partition
                     vendor: Windows
                     physical id: 3
                     bus info: scsi@0:0.0.0,3
                     logical name: /dev/sda3
                     serial: 5a84d4b8-2bc0-4f16-9b9f-c12dbf428652
                     capacity: 127MiB
                     capabilities: nofs nomount
                     configuration: name=Microsoft reserved partition
                *-volume:3
                     description: Windows NTFS volume
                     vendor: Windows
                     physical id: 4
                     bus info: scsi@0:0.0.0,4
                     logical name: /dev/sda4
                     version: 3.1
                     serial: 4880116d-6be3-724b-a20d-07ac58e60982
                     size: 283GiB
                     capacity: 283GiB
                     capabilities: ntfs initialized
                     configuration: clustersize=4096 created=2014-04-03 08:37:27 filesystem=ntfs label=OS name=Basic data partition state=clean
                *-volume:4 UNCLAIMED
                     description: EFI partition
                     physical id: 5
                     bus info: scsi@0:0.0.0,5
                     serial: cf385d4e-6174-4aa4-b712-7d14f8a35f1b
                     capacity: 1023MiB
                *-volume:5
                     description: Windows NTFS volume
                     vendor: Windows
                     physical id: 6
                     bus info: scsi@0:0.0.0,6
                     logical name: /dev/sda6
                     version: 3.1
                     serial: 3093f451-0b25-6041-acc1-0a1ffc723934
                     size: 63GiB
                     capacity: 63GiB
                     capabilities: ntfs initialized
                     configuration: clustersize=4096 created=2025-02-23 18:23:48 filesystem=ntfs label=Data name=Basic data partition state=clean
                *-volume:6
                     description: Windows NTFS volume
                     vendor: Windows
                     physical id: 7
                     bus info: scsi@0:0.0.0,7
                     logical name: /dev/sda7
                     version: 3.1
                     serial: 9032-72c7
                     size: 20GiB
                     capacity: 20GiB
                     capabilities: boot precious nomount ntfs initialized
                     configuration: clustersize=4096 created=2014-04-03 08:37:33 filesystem=ntfs label=Restore name=Basic data partition state=clean
                *-volume:7
                     description: LVM Physical Volume
                     vendor: Linux
                     physical id: 8
                     bus info: scsi@0:0.0.0,8
                     logical name: /dev/sda8
                     serial: pxc761-SDfb-0P7u-58a6-lEWv-WvhY-F98U3I
                     size: 96GiB
                     capabilities: multi lvm2
             *-cdrom
                  description: DVD-RAM writer
                  product: DVDRAM GUA0N
                  vendor: HL-DT-ST
                  physical id: 1
                  bus info: scsi@1:0.0.0
                  logical name: /dev/cdrom
                  logical name: /dev/sr0
                  version: AS00
                  capabilities: removable audio cd-r cd-rw dvd dvd-r dvd-ram
                  configuration: ansiversion=5 status=nodisc
          *-serial
               description: SMBus
               product: 8 Series SMBus Controller
               vendor: Intel Corporation
               physical id: 1f.3
               bus info: pci@0000:00:1f.3
               version: 04
               width: 64 bits
               clock: 33MHz
               configuration: driver=i801_smbus latency=0
               resources: irq:18 memory:f7a21000-f7a210ff ioport:f040(size=32)
          *-generic:1
               description: Signal processing controller
               product: 8 Series Thermal
               vendor: Intel Corporation
               physical id: 1f.6
               bus info: pci@0000:00:1f.6
               version: 04
               width: 64 bits
               clock: 33MHz
               capabilities: pm msi bus_master cap_list
               configuration: driver=intel_pch_thermal latency=0
               resources: irq:18 memory:f7a20000-f7a20fff
    *-input:0
         product: Lid Switch
         physical id: 1
         logical name: input0
         logical name: /dev/input/event0
         capabilities: platform
    *-input:1
         product: Sleep Button
         physical id: 2
         logical name: input1
         logical name: /dev/input/event1
         capabilities: platform
    *-input:2
         product: ETPS/2 Elantech Touchpad
         physical id: 3
         logical name: input11
         logical name: /dev/input/event9
         logical name: /dev/input/mouse1
         capabilities: i8042
    *-input:3
         product: Video Bus
         physical id: 4
         logical name: input17
         logical name: /dev/input/event10
         capabilities: platform
    *-input:4
         product: Video Bus
         physical id: 5
         logical name: input18
         logical name: /dev/input/event11
         capabilities: platform
    *-input:5
         product: Asus WMI hotkeys
         physical id: 6
         logical name: input19
         logical name: /dev/input/event12
         capabilities: platform
    *-input:6
         product: Power Button
         physical id: 7
         logical name: input2
         logical name: /dev/input/event2
         capabilities: platform
    *-input:7
         product: PC Speaker
         physical id: 8
         logical name: input20
         logical name: /dev/input/event13
         capabilities: isa
    *-input:8
         product: AT Translated Set 2 keyboard
         physical id: 9
         logical name: input3
         logical name: /dev/input/event3
         logical name: input3::capslock
         logical name: input3::numlock
         logical name: input3::scrolllock
         capabilities: i8042
  [hungtx@linux ~]$
  ```
- `sudo lshw -short`

  ```
  [hungtx@linux ~]$ sudo lshw -short
  H/W path         Device      Class          Description
  =======================================================
                               system         X550LD (ASUS-NotebookSKU)
  /0                           bus            X550LD
  /0/0                         memory         64KiB BIOS
  /0/7                         processor      Intel(R) Core(TM) i5-4200U CPU @ 1.60GHz
  /0/7/8                       memory         512KiB L2 cache
  /0/7/9                       memory         128KiB L1 cache
  /0/7/a                       memory         3MiB L3 cache
  /0/b                         memory         12GiB System Memory
  /0/b/0                       memory         4GiB SODIMM DDR3 Synchronous 1600 MHz (0.6 ns)
  /0/b/1                       memory         DIMM [empty]
  /0/b/2                       memory         8GiB SODIMM DDR3 Synchronous 1600 MHz (0.6 ns)
  /0/b/3                       memory         DIMM [empty]
  /0/100                       bridge         Haswell-ULT DRAM Controller
  /0/100/2         /dev/fb0    display        Haswell-ULT Integrated Graphics Controller
  /0/100/3         card0       multimedia     Haswell-ULT HD Audio Controller
  /0/100/3/0       input21     input          HDA Intel HDMI HDMI/DP,pcm=3
  /0/100/3/1       input22     input          HDA Intel HDMI HDMI/DP,pcm=7
  /0/100/3/2       input23     input          HDA Intel HDMI HDMI/DP,pcm=8
  /0/100/4                     generic        Haswell-ULT Thermal Subsystem
  /0/100/14                    bus            8 Series USB xHCI HC
  /0/100/14/0      usb1        bus            xHCI Host Controller
  /0/100/14/0/2                generic        Edimax AC600 USB
  /0/100/14/0/5                multimedia     USB2.0 HD UVC WebCam
  /0/100/14/0/6                communication  Bluetooth Radio
  /0/100/14/1      usb3        bus            xHCI Host Controller
  /0/100/16                    communication  8 Series HECI #0
  /0/100/1b        card1       multimedia     8 Series HD Audio Controller
  /0/100/1b/0      input24     input          HDA Intel PCH Mic
  /0/100/1b/1      input25     input          HDA Intel PCH Headphone
  /0/100/1c                    bridge         8 Series PCI Express Root Port 1
  /0/100/1c.2                  bridge         8 Series PCI Express Root Port 3
  /0/100/1c.2/0    mmc0        bus            RTL8411B PCI Express Card Reader
  /0/100/1c.2/0.1  enp2s0f1    network        RTL8111/8168/8211/8411 PCI Express Gigabit Ethernet Controller
  /0/100/1c.3                  bridge         8 Series PCI Express Root Port 4
  /0/100/1c.3/0    wlp3s0      network        RTL8821AE 802.11ac PCIe Wireless Network Adapter
  /0/100/1c.4                  bridge         8 Series PCI Express Root Port 5
  /0/100/1c.4/0                display        GF117M [GeForce 610M/710M/810M/820M / GT 620M/625M/630M/720M]
  /0/100/1d                    bus            8 Series USB EHCI #1
  /0/100/1d/1      usb2        bus            EHCI Host Controller
  /0/100/1d/1/1                bus            Integrated Rate Matching Hub
  /0/100/1d/1/1/3  input12     input          MOSART Semi. 2.4G Keyboard Mouse
  /0/100/1f                    bridge         8 Series LPC Controller
  /0/100/1f/0                  system         PnP device PNP0c01
  /0/100/1f/1                  system         PnP device PNP0c02
  /0/100/1f/2                  system         PnP device PNP0b00
  /0/100/1f/3                  generic        PnP device INT3f0d
  /0/100/1f/4                  system         PnP device PNP0c02
  /0/100/1f/5                  system         PnP device PNP0c02
  /0/100/1f/6                  generic        PnP device ETD0108
  /0/100/1f/7                  generic        PnP device ATK3001
  /0/100/1f/8                  system         PnP device PNP0c02
  /0/100/1f/9                  system         PnP device PNP0c02
  /0/100/1f/a                  system         PnP device PNP0c02
  /0/100/1f.2      scsi0       storage        8 Series SATA Controller 1 [AHCI mode]
  /0/100/1f.2/0    /dev/sda    disk           500GB TOSHIBA MQ01ABF0
  /0/100/1f.2/0/1  /dev/sda1   volume         99MiB Windows FAT volume
  /0/100/1f.2/0/2  /dev/sda2   volume         899MiB Windows NTFS volume
  /0/100/1f.2/0/3  /dev/sda3   volume         127MiB reserved partition
  /0/100/1f.2/0/4  /dev/sda4   volume         283GiB Windows NTFS volume
  /0/100/1f.2/0/5              volume         1023MiB EFI partition
  /0/100/1f.2/0/6  /dev/sda6   volume         63GiB Windows NTFS volume
  /0/100/1f.2/0/7  /dev/sda7   volume         20GiB Windows NTFS volume
  /0/100/1f.2/0/8  /dev/sda8   volume         96GiB LVM Physical Volume
  /0/100/1f.2/1    /dev/cdrom  disk           DVDRAM GUA0N
  /0/100/1f.3                  bus            8 Series SMBus Controller
  /0/100/1f.6                  generic        8 Series Thermal
  /1               input0      input          Lid Switch
  /2               input1      input          Sleep Button
  /3               input11     input          ETPS/2 Elantech Touchpad
  /4               input17     input          Video Bus
  /5               input18     input          Video Bus
  /6               input19     input          Asus WMI hotkeys
  /7               input2      input          Power Button
  /8               input20     input          PC Speaker
  /9               input3      input          AT Translated Set 2 keyboard
  [hungtx@linux ~]$ 

  ```

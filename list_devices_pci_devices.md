To list all devices connected to the PCI bus, use the following commands:

- `lspci`
  
  ```
  [hungtx@linux ~]$ lspci
  00:00.0 Host bridge: Intel Corporation Haswell-ULT DRAM Controller (rev 09)
  00:02.0 VGA compatible controller: Intel Corporation Haswell-ULT Integrated Graphics Controller (rev 09)
  00:03.0 Audio device: Intel Corporation Haswell-ULT HD Audio Controller (rev 09)
  00:04.0 Signal processing controller: Intel Corporation Haswell-ULT Thermal Subsystem (rev 09)
  00:14.0 USB controller: Intel Corporation 8 Series USB xHCI HC (rev 04)
  00:16.0 Communication controller: Intel Corporation 8 Series HECI #0 (rev 04)
  00:1b.0 Audio device: Intel Corporation 8 Series HD Audio Controller (rev 04)
  00:1c.0 PCI bridge: Intel Corporation 8 Series PCI Express Root Port 1 (rev e4)
  00:1c.2 PCI bridge: Intel Corporation 8 Series PCI Express Root Port 3 (rev e4)
  00:1c.3 PCI bridge: Intel Corporation 8 Series PCI Express Root Port 4 (rev e4)
  00:1c.4 PCI bridge: Intel Corporation 8 Series PCI Express Root Port 5 (rev e4)
  00:1d.0 USB controller: Intel Corporation 8 Series USB EHCI #1 (rev 04)
  00:1f.0 ISA bridge: Intel Corporation 8 Series LPC Controller (rev 04)
  00:1f.2 SATA controller: Intel Corporation 8 Series SATA Controller 1 [AHCI mode] (rev 04)
  00:1f.3 SMBus: Intel Corporation 8 Series SMBus Controller (rev 04)
  00:1f.6 Signal processing controller: Intel Corporation 8 Series Thermal (rev 04)
  02:00.0 Unassigned class [ff00]: Realtek Semiconductor Co., Ltd. RTL8411B PCI Express Card Reader (rev 01)
  02:00.1 Ethernet controller: Realtek Semiconductor Co., Ltd. RTL8111/8168/8211/8411 PCI Express Gigabit Ethernet Controller (rev 12)
  03:00.0 Network controller: Realtek Semiconductor Co., Ltd. RTL8821AE 802.11ac PCIe Wireless Network Adapter
  04:00.0 3D controller: NVIDIA Corporation GF117M [GeForce 610M/710M/810M/820M / GT 620M/625M/630M/720M] (rev a1)
  ```
- `lspci -m`
  
  ```
  [hungtx@linux ~]$ lspci -m
  00:00.0 "Host bridge" "Intel Corporation" "Haswell-ULT DRAM Controller" -r09 "ASUSTeK Computer Inc." "Device 131d"
  00:02.0 "VGA compatible controller" "Intel Corporation" "Haswell-ULT Integrated Graphics Controller" -r09 "ASUSTeK Computer Inc." "Device 228a"
  00:03.0 "Audio device" "Intel Corporation" "Haswell-ULT HD Audio Controller" -r09 "ASUSTeK Computer Inc." "Device 131d"
  00:04.0 "Signal processing controller" "Intel Corporation" "Haswell-ULT Thermal Subsystem" -r09 "ASUSTeK Computer Inc." "Device 131d"
  00:14.0 "USB controller" "Intel Corporation" "8 Series USB xHCI HC" -r04 -p30 "ASUSTeK Computer Inc." "Device 201f"
  00:16.0 "Communication controller" "Intel Corporation" "8 Series HECI #0" -r04 "ASUSTeK Computer Inc." "Device 131d"
  00:1b.0 "Audio device" "Intel Corporation" "8 Series HD Audio Controller" -r04 "ASUSTeK Computer Inc." "Device 11af"
  00:1c.0 "PCI bridge" "Intel Corporation" "8 Series PCI Express Root Port 1" -re4 "" ""
  00:1c.2 "PCI bridge" "Intel Corporation" "8 Series PCI Express Root Port 3" -re4 "" ""
  00:1c.3 "PCI bridge" "Intel Corporation" "8 Series PCI Express Root Port 4" -re4 "" ""
  00:1c.4 "PCI bridge" "Intel Corporation" "8 Series PCI Express Root Port 5" -re4 "" ""
  00:1d.0 "USB controller" "Intel Corporation" "8 Series USB EHCI #1" -r04 -p20 "ASUSTeK Computer Inc." "Device 201f"
  00:1f.0 "ISA bridge" "Intel Corporation" "8 Series LPC Controller" -r04 "ASUSTeK Computer Inc." "Device 131d"
  00:1f.2 "SATA controller" "Intel Corporation" "8 Series SATA Controller 1 [AHCI mode]" -r04 -p01 "ASUSTeK Computer Inc." "Device 131d"
  00:1f.3 "SMBus" "Intel Corporation" "8 Series SMBus Controller" -r04 "ASUSTeK Computer Inc." "Device 131d"
  00:1f.6 "Signal processing controller" "Intel Corporation" "8 Series Thermal" -r04 "ASUSTeK Computer Inc." "Device 131d"
  02:00.0 "Unassigned class [ff00]" "Realtek Semiconductor Co., Ltd." "RTL8411B PCI Express Card Reader" -r01 "ASUSTeK Computer Inc." "Device 202f"
  02:00.1 "Ethernet controller" "Realtek Semiconductor Co., Ltd." "RTL8111/8168/8211/8411 PCI Express Gigabit Ethernet Controller" -r12 "ASUSTeK Computer Inc." "Device 200f"
  03:00.0 "Network controller" "Realtek Semiconductor Co., Ltd." "RTL8821AE 802.11ac PCIe Wireless Network Adapter" "AzureWave" "Device 2161"
  04:00.0 "3D controller" "NVIDIA Corporation" "GF117M [GeForce 610M/710M/810M/820M / GT 620M/625M/630M/720M]" -ra1 "" ""
  [hungtx@linux ~]$
  ```

 

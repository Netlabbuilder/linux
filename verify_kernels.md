When a new kernel is installed via a system update, AlmaLinux (and most RHEL-based distros) keeps the old kernel as fallback option in case the new one has issues.

The bootloader (GRUB) lists both kernels so you can choose which one to boot into.

- AlmaLinux (New Kernel Version) – This is the latest one that just got installed.
- AlmaLinux (Old Kernel Version) – This is your previous kernel, still available in case something goes wrong with the new one.

To list installed kernels:

- rpm -q kernel
  ```
  [hungtx@linux ~]$ rpm -q kernel
  kernel-5.14.0-503.11.1.el9_5.x86_64
  kernel-5.14.0-503.34.1.el9_5.x86_64
  [hungtx@linux ~]$
  ```
- dnf list installed kernel
  ```
  [hungtx@linux ~]$ dnf list installed kernel
  Installed Packages
  kernel.x86_64                  5.14.0-503.11.1.el9_5                    @anaconda
  kernel.x86_64                  5.14.0-503.34.1.el9_5                    @baseos  
  [hungtx@linux ~]$
  ```
To see which kernel is currently running:
- uname -r
  ```
  [hungtx@linux ~]$ uname -r
  5.14.0-503.11.1.el9_5.x86_64
  [hungtx@linux ~]$
  ```
- hostnamectl status
  ```
  [hungtx@linux ~]$ hostnamectl status
   Static hostname: linux.netlabbuilder.net
         Icon name: computer-laptop
           Chassis: laptop 💻
        Machine ID: b83de91843ca43a1bb8d01784272f524
           Boot ID: acfe758469c446a8871e1b79cac29ebe
  Operating System: AlmaLinux 9.5 (Teal Serval)         
       CPE OS Name: cpe:/o:almalinux:almalinux:9::baseos
            Kernel: Linux 5.14.0-503.11.1.el9_5.x86_64
      Architecture: x86-64
   Hardware Vendor: ASUSTeK COMPUTER INC.
    Hardware Model: X550LD
  Firmware Version: X550LD.300
  ```
To list the kernel packages installed on the system, sorted by the most recent installation date.
- rpm -q --last kernel
  ```
  [hungtx@linux ~]$ rpm -q --last kernel
  kernel-5.14.0-503.34.1.el9_5.x86_64           Fri 04 Apr 2025 07:18:19 PM CEST
  kernel-5.14.0-503.11.1.el9_5.x86_64           Sun 23 Feb 2025 09:08:20 PM CET
  [hungtx@linux ~]$ 
  ```
  

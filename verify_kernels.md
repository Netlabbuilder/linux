When a new kernel is installed via a system update, AlmaLinux (and most RHEL-based distros) keeps the old kernel as fallback option in case the new one has issues.

The bootloader (GRUB) lists both kernels so you can choose which one to boot into.

- AlmaLinux (New Kernel Version) – This is the latest one that just got installed.
- AlmaLinux (Old Kernel Version) – This is your previous kernel, still available in case something goes wrong with the new one.

To list installed kernels:

- `rpm -q kernel`
  
  ```
  [hungtx@linux ~]$ rpm -q kernel
  kernel-5.14.0-503.11.1.el9_5.x86_64
  kernel-5.14.0-503.34.1.el9_5.x86_64
  [hungtx@linux ~]$
  ```
- `dnf list installed kernel`
  
  ```
  [hungtx@linux ~]$ dnf list installed kernel
  Installed Packages
  kernel.x86_64                  5.14.0-503.11.1.el9_5                    @anaconda
  kernel.x86_64                  5.14.0-503.34.1.el9_5                    @baseos  
  [hungtx@linux ~]$
  ```
To list installed and available kernels:

- `dnf list kernel`
  
  ```
  [hungtx@linux ~]$ dnf list kernel
  Last metadata expiration check: 18:23:01 ago on Sat 12 Apr 2025 12:19:15 AM CEST.
  Installed Packages
  kernel.x86_64                                                              5.14.0-503.11.1.el9_5                                                               @anaconda
  kernel.x86_64                                                              5.14.0-503.34.1.el9_5                                                               @baseos  
  Available Packages
  kernel.x86_64                                                              5.14.0-503.35.1.el9_5                                                               baseos   
  [hungtx@linux ~]$
  ```
To see which kernel is currently running:
- `uname -r`
  
  ```
  [hungtx@linux ~]$ uname -r
  5.14.0-503.11.1.el9_5.x86_64
  [hungtx@linux ~]$
  ```
- `hostnamectl status`
  
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
To query and list the kernel packages installed on the system, sorted by the most recent installation date:
- `rpm -q --last kernel`
  
  ```
  [hungtx@linux ~]$ rpm -q --last kernel
  kernel-5.14.0-503.34.1.el9_5.x86_64           Fri 04 Apr 2025 07:18:19 PM CEST
  kernel-5.14.0-503.11.1.el9_5.x86_64           Sun 23 Feb 2025 09:08:20 PM CET
  [hungtx@linux ~]$ 
  ```
To query and display kernel packages installed on the system, including name, version, and description... Check the `Install Date:` field for the date the kernel was installed:
- `pm -qi  kernel`
  
  ```
  [hungtx@linux ~]$ rpm -qi kernel
  Name        : kernel
  Version     : 5.14.0
  Release     : 503.11.1.el9_5
  Architecture: x86_64
  Install Date: Sun 23 Feb 2025 09:08:20 PM CET
  Group       : Unspecified
  Size        : 0
  License     : ((GPL-2.0-only WITH Linux-syscall-note) OR BSD-2-Clause) AND ((GPL-2.0-only WITH Linux-syscall-note) OR BSD-3-Clause) AND ((GPL-2.0-only WITH Linux-syscall-  note) OR CDDL-1.0) AND ((GPL-2.0-only WITH Linux-syscall-note) OR Linux-OpenIB) AND ((GPL-2.0-only WITH Linux-syscall-note) OR MIT) AND ((GPL-2.0-or-later WITH Linux-syscall-note) OR BSD-3-Clause) AND ((GPL-2.0-or-later WITH Linux-syscall-note) OR MIT) AND Apache-2.0 AND BSD-2-Clause AND BSD-3-Clause AND BSD-3-Clause-Clear AND GFDL-1.1-no-invariants-or-later AND GPL-1.0-or-later AND (GPL-1.0-or-later OR BSD-3-Clause) AND (GPL-1.0-or-later WITH Linux-syscall-note) AND GPL-2.0-only AND (GPL-2.0-only OR Apache-2.0) AND (GPL-2.0-only OR BSD-2-Clause) AND (GPL-2.0-only OR BSD-3-Clause) AND (GPL-2.0-only OR CDDL-1.0) AND (GPL-2.0-only OR GFDL-1.1-no-invariants-or-later) AND (GPL-2.0-only OR GFDL-1.2-no-invariants-only) AND (GPL-2.0-only WITH Linux-syscall-note) AND GPL-2.0-or-later AND (GPL-2.0-or-later OR BSD-2-Clause) AND (GPL-2.0-or-later OR BSD-3-Clause) AND (GPL-2.0-or-later OR CC-BY-4.0) AND (GPL-2.0-or-later WITH GCC-exception-2.0) AND (GPL-2.0-or-later WITH Linux-syscall-note) AND ISC AND LGPL-2.0-or-later AND (LGPL-2.0-or-later OR BSD-2-Clause) AND (LGPL-2.0-or-later WITH Linux-syscall-note) AND LGPL-2.1-only AND (LGPL-2.1-only OR BSD-2-Clause) AND (LGPL-2.1-only WITH Linux-syscall-note) AND LGPL-2.1-or-later AND (LGPL-2.1-or-later WITH Linux-syscall-note) AND (Linux-OpenIB OR GPL-2.0-only) AND (Linux-OpenIB OR GPL-2.0-only OR BSD-2-Clause) AND Linux-man-pages-copyleft AND MIT AND (MIT OR GPL-2.0-only) AND (MIT OR GPL-2.0-or-later) AND (MIT OR LGPL-2.1-only) AND (MPL-1.1 OR GPL-2.0-only) AND (X11 OR GPL-2.0-only) AND (X11 OR GPL-2.0-or-later) AND Zlib
  Signature   : RSA/SHA256, Tue 12 Nov 2024 04:55:16 PM CET, Key ID d36cb86cb86b3716
  Source RPM  : kernel-5.14.0-503.11.1.el9_5.src.rpm
  Build Date  : Tue 12 Nov 2024 02:48:00 PM CET
  Build Host  : x64-builder01.almalinux.org
  Packager    : AlmaLinux Packaging Team <packager@almalinux.org>
  Vendor      : AlmaLinux
  URL         : https://www.kernel.org/
  Summary     : The Linux kernel
  Description :
  The kernel meta package
  Name        : kernel
  Version     : 5.14.0
  Release     : 503.34.1.el9_5
  Architecture: x86_64
  Install Date: Fri 04 Apr 2025 07:18:19 PM CEST
  Group       : Unspecified
  Size        : 0
  License     : ((GPL-2.0-only WITH Linux-syscall-note) OR BSD-2-Clause) AND ((GPL-2.0-only WITH Linux-syscall-note) OR BSD-3-Clause) AND ((GPL-2.0-only WITH Linux-syscall-note) OR CDDL-1.0) AND ((GPL-2.0-only WITH Linux-syscall-note) OR Linux-OpenIB) AND ((GPL-2.0-only WITH Linux-syscall-note) OR MIT) AND ((GPL-2.0-or-later WITH Linux-syscall-note) OR BSD-3-Clause) AND ((GPL-2.0-or-later WITH Linux-syscall-note) OR MIT) AND Apache-2.0 AND BSD-2-Clause AND BSD-3-Clause AND BSD-3-Clause-Clear AND GFDL-1.1-no-invariants-or-later AND GPL-1.0-or-later AND (GPL-1.0-or-later OR BSD-3-Clause) AND (GPL-1.0-or-later WITH Linux-syscall-note) AND GPL-2.0-only AND (GPL-2.0-only OR Apache-2.0) AND (GPL-2.0-only OR BSD-2-Clause) AND (GPL-2.0-only OR BSD-3-Clause) AND (GPL-2.0-only OR CDDL-1.0) AND (GPL-2.0-only OR GFDL-1.1-no-invariants-or-later) AND (GPL-2.0-only OR GFDL-1.2-no-invariants-only) AND (GPL-2.0-only WITH Linux-syscall-note) AND GPL-2.0-or-later AND (GPL-2.0-or-later OR BSD-2-Clause) AND (GPL-2.0-or-later OR BSD-3-Clause) AND (GPL-2.0-or-later OR CC-BY-4.0) AND (GPL-2.0-or-later WITH GCC-exception-2.0) AND (GPL-2.0-or-later WITH Linux-syscall-note) AND ISC AND LGPL-2.0-or-later AND (LGPL-2.0-or-later OR BSD-2-Clause) AND (LGPL-2.0-or-later WITH Linux-syscall-note) AND LGPL-2.1-only AND (LGPL-2.1-only OR BSD-2-Clause) AND (LGPL-2.1-only WITH Linux-syscall-note) AND LGPL-2.1-or-later AND (LGPL-2.1-or-later WITH Linux-syscall-note) AND (Linux-OpenIB OR GPL-2.0-only) AND (Linux-OpenIB OR GPL-2.0-only OR BSD-2-Clause) AND Linux-man-pages-copyleft AND MIT AND (MIT OR GPL-2.0-only) AND (MIT OR GPL-2.0-or-later) AND (MIT OR LGPL-2.1-only) AND (MPL-1.1 OR GPL-2.0-only) AND (X11 OR GPL-2.0-only) AND (X11 OR GPL-2.0-or-later) AND Zlib
  Signature   : RSA/SHA256, Thu 27 Mar 2025 02:04:02 PM CET, Key ID d36cb86cb86b3716
  Source RPM  : kernel-5.14.0-503.34.1.el9_5.src.rpm
  Build Date  : Thu 27 Mar 2025 10:22:54 AM CET
  Build Host  : x64-builder01.almalinux.org
  Packager    : AlmaLinux Packaging Team <packager@almalinux.org>
  Vendor      : AlmaLinux
  URL         : https://www.kernel.org/
  Summary     : The Linux kernel
  Description :
  The kernel meta package
  [hungtx@linux ~]$
  ```


To list all block devices (disks, partitions, etc.), use the following commands:
- `lsblk`
```
[hungtx@linux ~]$ lsblk
NAME               MAJ:MIN RM   SIZE RO TYPE MOUNTPOINTS
sda                  8:0    0 465.8G  0 disk 
├─sda1               8:1    0   100M  0 part /boot/efi
├─sda2               8:2    0   900M  0 part 
├─sda3               8:3    0   128M  0 part 
├─sda4               8:4    0   284G  0 part 
├─sda5               8:5    0     1G  0 part /boot
├─sda6               8:6    0    63G  0 part 
├─sda7               8:7    0    20G  0 part 
└─sda8               8:8    0  96.7G  0 part 
  ├─almalinux-root 253:0    0    61G  0 lvm  /
  ├─almalinux-swap 253:1    0   5.8G  0 lvm  [SWAP]
  └─almalinux-home 253:2    0  29.8G  0 lvm  /home
sr0                 11:0    1  1024M  0 rom  
[hungtx@linux ~]$ 
```
- `lsblk -f`
```
[hungtx@linux ~]$ lsblk -f
NAME               FSTYPE      FSVER    LABEL    UUID                                   FSAVAIL FSUSE% MOUNTPOINTS
sda                                                                                                    
├─sda1             vfat        FAT32    SYSTEM   6434-198D                                62.7M    35% /boot/efi
├─sda2             ntfs                 Recovery 60FE2B98FE2B660E                                      
├─sda3                                                                                                 
├─sda4             ntfs                 OS       FCDA2F38DA2EEE98                                      
├─sda5             xfs                           c8879c59-c6af-4a24-8b4d-3615e9424816      533M    44% /boot
├─sda6             ntfs                 Data     306EB3EF6EB3ABCA                                      
├─sda7             ntfs                 Restore  AE9032A4903272C7                                      
└─sda8             LVM2_member LVM2 001          pxc761-SDfb-0P7u-58a6-lEWv-WvhY-F98U3I                
  ├─almalinux-root xfs                           14ae2463-6c29-4b77-9461-2b55486d90f7     55.3G     9% /
  ├─almalinux-swap swap        1                 a02f31a7-a502-4352-afc9-b6da1dbb3b7b                  [SWAP]
  └─almalinux-home xfs                           e969eb13-3806-47b0-bc17-0c06f1324b57     28.7G     4% /home
sr0                                                                                                    
[hungtx@linux ~]$ 

```

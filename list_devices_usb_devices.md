To list all USB devices connected to the system, use the following commands:
- `lsusb`
  ```
  hungtx@linux ~]$ lsusb
  Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
  Bus 001 Device 002: ID 7392:a812 Edimax Technology Co., Ltd Edimax AC600 USB
  Bus 001 Device 003: ID 04f2:b40a Chicony Electronics Co., Ltd USB2.0 HD UVC WebCam
  Bus 001 Device 004: ID 13d3:3414 IMC Networks Bluetooth Radio 
  Bus 002 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub
  Bus 002 Device 002: ID 8087:8000 Intel Corp. Integrated Rate Matching Hub
  Bus 002 Device 003: ID 062a:5918 MosArt Semiconductor Corp. 2.4G Keyboard Mouse
  Bus 003 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub
  [hungtx@linux ~]$
  ```
- `lsusb -t`
  ```
  [hungtx@linux ~]$ lsusb -t
  /:  Bus 001.Port 001: Dev 001, Class=root_hub, Driver=xhci_hcd/9p, 480M
      |__ Port 002: Dev 002, If 0, Class=Vendor Specific Class, Driver=[none], 480M
      |__ Port 005: Dev 003, If 0, Class=Video, Driver=uvcvideo, 480M
      |__ Port 005: Dev 003, If 1, Class=Video, Driver=uvcvideo, 480M
      |__ Port 006: Dev 004, If 0, Class=Wireless, Driver=btusb, 12M
      |__ Port 006: Dev 004, If 1, Class=Wireless, Driver=btusb, 12M
  /:  Bus 002.Port 001: Dev 001, Class=root_hub, Driver=ehci-pci/2p, 480M
      |__ Port 001: Dev 002, If 0, Class=Hub, Driver=hub/8p, 480M
          |__ Port 003: Dev 003, If 0, Class=Human Interface Device, Driver=usbhid, 12M
          |__ Port 003: Dev 003, If 1, Class=Human Interface Device, Driver=usbhid, 12M
  /:  Bus 003.Port 001: Dev 001, Class=root_hub, Driver=xhci_hcd/4p, 5000M
  [hungtx@linux ~]$ 
  ```

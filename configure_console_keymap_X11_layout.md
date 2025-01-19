- Verify the current status of Virtual Console (VC) Keymap and X11 Layout:
  ```
  localectl status
  ```
- List known virtual console keyboard mappings:
  ```
  localectl list-keymaps
  ```
- Set console and X11 keyboard mappings (below is to set keymap to German language keyboard - de):
  ```
  localectl set-keymap de
  ```

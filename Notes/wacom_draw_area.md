# Wacom tablet draw area

By default wacom tablet used both screens as a drawing area.
That is an issue since you get a very wide but not very tall area on a small tablet.

## Steps to fix
1. Install `xf86-input-wacom` - might not be necessary
2. Run `xsetwacom list devices`
    - Find "STYLUS" id
    - In my case it's 8
  ```bash
  [sasa@sasa-pc ~]$ xsetwacom list devices
  Wacom One by Wacom S Pen stylus 	id: 8	type: STYLUS    
  Wacom One by Wacom S Pen eraser 	id: 14	type: ERASER 
  ```
3. Next run `xrandr` and find id of the monitor that you wish to use
    - In my case `HDMI-A-0 connected primary 1920x1080` it is `HDMI-A-0`
4. Finally run `xsetwacom set 8 MapToOutput HDMI-A-0`
5. Change stylus and monitor ids if necessary

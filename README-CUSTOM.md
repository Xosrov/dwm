# IMPORTANT NOTES TO GET THIS WORKING

## If not using Void Linux:

Modify the two `X11` library lines in `config.mk` and uncomment the default values


## Additional dependencies

* **FriBiDi** library for rtl support
* **libxcb**, **Xlib-libxcb** and **xcb-res** packages (platform dependant) for swallow

For ubuntu, I put these into .xprofile:
```
if [ "$DESKTOP_SESSION" = "dwm" ]; then
        TOUCHPAD_ID=$(xinput list | grep Touchpad | rev | awk '{print $4}' | rev | cut -d'=' -f2)
	xinput --set-prop $TOUCHPAD_ID 'libinput Tapping Enabled' 1
	xinput --set-prop $TOUCHPAD_ID 'libinput Tapping Drag Lock Enabled' 1
	xinput --set-prop $TOUCHPAD_ID 'libinput Natural Scrolling Enabled' 1
	xinput --set-prop $TOUCHPAD_ID 'libinput Middle Emulation Enabled' 1
        slstatus &
        xcompmgr &
        copyq &
        feh --bg-scale /home/amiryazdi/Pictures/bg1.jpg &
        nm-applet --indicator &
        blueman-applet &
fi
```
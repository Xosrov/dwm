# IMPORTANT NOTES TO GET THIS WORKING

## If not using Void Linux:

Modify the two `X11` library lines in `config.mk` and uncomment the default values


## Additional dependencies

* **FriBiDi** library for rtl support
* **libxcb**, **Xlib-libxcb** and **xcb-res** packages (platform dependant) for swallow

For ubuntu, I put these into .xprofile:
```
if [ "$DESKTOP_SESSION" = "dwm" ]; then
        slstatus &
        xcompmgr &
        copyq &
        feh --bg-scale /home/amiryazdi/Pictures/bg1.jpg &
        nm-applet --indicator &
        blueman-applet &
fi
```
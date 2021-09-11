# screen

to prevent screensaver from kicking in, create no-screensaver.desktop file in ```~/.config/autostart``` with following: 

```
[Desktop Entry]
Type=Application
Exec=xset -dpms s off s noblank s 0 0 s noexpose
Hidden=false
Name=No screensaver
```

to check if you are using X or Wayland: 

```
echo \$XDG_SESSION_TYPE
```


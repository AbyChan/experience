--title:display right click
--date:2015-12-28 06:48:35
--tag:
#---
`/etc/X11/xorg.conf `
```
Section "InputClass"
   Identifier "calibration"
   Driver "evdev"
   MatchProduct "FT5406 memory based driver"

   Option "EmulateThirdButton" "1"
   Option "EmulateThirdButtonTimeout" "750"
   Option "EmulateThirdButtonMoveThreshold" "30"
EndSection
```

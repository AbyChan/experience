--title:gentoo安装xorg
--date:2015-12-18 01:53:38
--tag:
###
必须要在` make.conf `里面设置
```
## (For mouse, keyboard, and Synaptics touchpad support)
INPUT_DEVICES="evdev synaptics"
## (For nVidia cards)
VIDEO_CARDS="nouveau"
## (For AMD/ATI cards)
VIDEO_CARDS="radeon"
```
之后才能emerge x11-base/xorg-server

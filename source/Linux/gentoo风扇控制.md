--title:gentoo风扇控制
--date:2015-12-15 13:54:09
--tag:
###
```shell
    emerge sys-apps/lm_sensors
    sensors-detect
    然后选择检测到dirver(我这次是i2c-dev...)写入到`/etc/conf.d/lm_sensors` MODULE_0='xxx'
    /etc/init.d/lm*sensors start #启动
    c-update add lm*sensors default #设置自动启动
```

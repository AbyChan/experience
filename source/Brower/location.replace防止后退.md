--title:location.replace防止后退
--date:2018-3-7 23:20:45
--tag:
假设通过URL消耗资源，例如`url?token=xxx`，再次访问同样的地址会报错，那么只要让 `url?token=xxx` 消耗完之后用 location.replace('newurl' 或者 h5 的 replaceState，就可以解决问题
###

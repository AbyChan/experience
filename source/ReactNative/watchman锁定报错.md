--title:watchman锁定报错
--date:2015-12-04 14:09:50
--tag:
###
出现watchman报错
Poison: inotify_add_watch
其实是watch被锁定了，估计是有一次操作错误导致，把watchmen关掉即可。
`watchman shutdown-server`

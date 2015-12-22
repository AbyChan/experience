--title:dd命令非常慢
--date:2015-12-22 12:48:15
--tag:command,mac,dd
#---
mac下的dd命令非常慢，只要将diskN 变成 rdiskN 就能改善
`/dev/rdisk nodes are character-special devices, but are “raw” in the BSD sense and force block-aligned I/O. They are closer to the physical disk than the buffer cache. /dev/disk nodes, on the other hand, are buffered block-special devices and are used primarily by the kernel’s filesystem code.`

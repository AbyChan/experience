--title:Build Exit status 137 报错解决
--date:Tue Sep 19 08:21:33 EDT 2017
--tag:
###
在搬瓦工的 vps 上进行 webpack 构建，遇到了一个问题
```bash
13 verbose stack Exit status 137
13 verbose stack     at EventEmitter.<anonymous> (/usr/lib/node_modules/npm/lib/utils/lifecycle.js:289:16)
13 verbose stack     at emitTwo (events.js:125:13)
13 verbose stack     at EventEmitter.emit (events.js:213:7)
13 verbose stack     at ChildProcess.<anonymous> (/usr/lib/node_modules/npm/lib/utils/spawn.js:40:14)
13 verbose stack     at emitTwo (events.js:125:13)
13 verbose stack     at ChildProcess.emit (events.js:213:7)
13 verbose stack     at maybeClose (internal/child_process.js:927:16)
13 verbose stack     at Process.ChildProcess._handle.onexit (internal/child_process.js:211:5)
```
一开始以为是 node_modules, node 版本的问题，但是都排查过了，最终怀疑是内存不足的问题，遂开了交换空间，问题得以解决
```bash
  CPU[|||||||||||||||||||||||||||||||||||98.7%]   Tasks: 35, 42 thr; 2 running
  Mem[|||||||||||||||||||||||||||||||445M/504M]   Load average: 0.72 0.30 0.14
  Swp[|||||                         63.0M/512M]   Uptime: 10 days, 00:54:44

```
果然，在混淆 js 代码的时候，消耗了大量的内存，swap 分区也占到了 80M 左右

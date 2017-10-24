--title: Git服务器报32错误
--date: 2017年10月24日 星期二 16时02分00秒 CST
--tag: git gogs
之前一直用的 coding 不能创建私有项目了，只好自己搭一个 git 服务，gogs 搭好了之后遇到了一个问题，就是push 代码的时候遇到
```
SSL_write() returned SYSCALL, errno = 32
```
这个错误，这个错误的原因是我用了 nginx 做了代理，post 请求过大了，所以设置了一下
###
```
client_max_body_size 10m;
```
就好了

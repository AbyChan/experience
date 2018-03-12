--title: Node 子程序打印颜色问题
--date: 2017年10月25日 星期三 17时32分24秒 CST
--tag: node, exec, spawn
###
node 通过 exec， spawn 创建的子程序会通过 stdout， stderr 这两个对象同步子进程的 stdout， stderr 过来，因为 spawn 的 options 中的 stdio 的默认值是 pipe，如果设置为 inherit 的话继承父进程（就是程序的 node 进程），确实可以打印颜色，但是子进程就没有 stdio 了，要保持 stdio 和颜色，这个颜色实属无解，这不是 node 的问题，是因为很多命令行的程序会检测是不是 teminal 环境，如果是，才打印颜色。

--title:set和export的区别
--date:2016-01-11 13:46:49
--tag:
#---
linux 分 shell变量(set)，用户变量(env)， shell变量包含用户变量，export是一种命令工具，是显示那些通过export命令把shell变量中包含的用户变量导入给用户变量的那些变量.    
set:显示(设置)shell变量 包括的私有变量以及用户变量，不同类的shell有不同的私有变量 bash,ksh,csh每中shell私有变量都不一样   

env:显示(设置)用户变量变量   

export:显示(设置)当前导出成用户变量的shell变量。   

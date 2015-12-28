--title:ssh locate问题
--date:2015-12-28 03:15:58
--tag:
#---
ssh remote出现
```
perl: warning: Please check that your locale settings:
	LANGUAGE = (unset),
	LC_ALL = "en_US.UTF-8",
	LC_CTYPE = "en_US.UTF-8",
	LANG = "zh_CN.UTF-8"
    are supported and installed on your system.
perl: warning: Falling back to a fallback locale ("zh_CN.UTF-8").
```
之类的问题,需要在当前机子上设置环境变量
```
export LC_ALL=zh_CN.UTF-8
export LC_CTYPE=zh_CN.UTF-8
```
值为错误中的LANG变量

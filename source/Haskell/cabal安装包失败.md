--title:cabal安装包失败
--date:2015-12-22 17:14:56
--tag:
###
安装包出现cannot satisfy -package-id后面加一大堆hash的报错，我当时的原因是ghc的版本太新，包无法适配，用`uninstall-hs`按提示卸载一个就好了

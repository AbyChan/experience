--title:sqlite的并发问题
--date:2016-01-29 16:52:57
--tag:database
###
sqlite3 在 python 中的连接是不能并发的，创建的连接不能在另一个线程中调用，否则会抛出错误，所以在 web 框架中是不能共用一个连接来处理请求。

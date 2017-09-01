--title:jsonp问题
--date:2015-12-21 06:05:40
--tag:
###
jsonp 遇到 `Uncaught SyntaxError: Unexpected token :`报错，是因为没有设置callback，把返回的 json 当成代码执行了，需要设置 `callback=JSON_CALLBACK` 参数

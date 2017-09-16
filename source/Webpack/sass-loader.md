--title:Sass-loader Unexpected character '@'
--date:2017年 9月16日 星期六 12时05分05秒 CST
--tag:
###
build 的时候报错
```bash
ERROR in ./page/Todo/TodoPage.scss
Module parse failed: /Users/chchen/Octopus/web-octopus/page/Todo/TodoPage.scss Unexpected character '@' (1:0)
You may need an appropriate loader to handle this file type.
| @import 'style/variable';
| @import 'style/mixin';
|
 @ ./page/Todo/TodoPage.js 29:0-26
 @ ./page/Todo/TodoPage.container.js
 @ ./page/App.js
 @ ./page/App.container.js
 @ ./index.js
 @ multi babel-polyfill ./index
```
之前 webpack1 遗留的 include 必须注释掉
```javascript
      {
        test: /\.scss$/,
        // TODO note 必须不要这行 include: [path.resolve(__dirname, './style')],
        use: ExtractTextPlugin.extract({
          use: [
            {
              loader: 'css-loader'
            },
            {
              loader: 'sass-loader'
            }
          ],
          // use style-loader in development
          fallback: 'style-loader'
        })
      }
```

--title:service和directive的模式
--date:2015-12-08 08:05:48
--tag: angular, ionic, hybird app
#---
在ionic的开发中，要搞清楚组件的抽象，service和directive的模式，由于angular的设计模式，很多view层面的东西必须抽到directive上实现，但是不要总想着把directive设计成通用的组件，很多情况下direcitve都是只用在一个地方的，如果需要重用，建议与service结合。

#### 群内讨论了react-redux 中的connect 函数，如何对双括号理解的问题。有同学是这样解释的，直接上代码
```js
function(){return function(){}}

function connect(a,b){return function(c){console.log(a,b,c)}}
connect(1,2)(3)
// 输出: 1,2,3
```

#### 今天react项目里的一些心得
- 用 `ref` 获取元素，比如你想获取某元素到屏幕顶部的页面顶部的距离：`this.refs.myDiv.offsetTop`
- 数组map时，一定要有外层标签才能渲染出东西，否则页面上没东西。

#### `babel-polyfill`的作用
- Babel默认只转换新的JavaScript语法，而不是转换新的API，比如Iterator、Generator、Set、Maps、Proxy、Reflect，Symbol、Promise
等全局对象，以及一些定义在全局对象上的方法（比如Object.assign）都不会转码。举例来说，ES6在Array对象上新增了Array.from方法。Babel
就不会转码这个方法，如果想让这个方法运行，必须使用babel-polyfill

#### Babel的配置文件是.babelrc，存放在项目的根目录下。使用Babel的第一步就是配置这个文件。
该文件用来设置转码规则和插件，基本格式如下。
```javascript
{
    "presets": [],
    "plugins": []
}
```
    官方设定了以下转码规则，根据需要进行安装
    ES2015转码规则：babel-preset-es2015
    react转码规则：babel-preset-react
    ES7不同阶段语法提案的转码规则：babel-preset-stage-0（0，1，2，3）
然后将这些规则加入 .babelrc
```javascript
{
    "presets": [
        "es2015",
        "react",
        "stage-2"
    ],
    "plugins": []
}
```
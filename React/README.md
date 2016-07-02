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

#### 群内讨论了react-redux 中的connect 函数，如何对双括号理解的问题。有同学是这样解释的，直接上代码
```js
function(){return function(){}}

function connect(a,b){return function(c){console.log(a,b,c)}}
connect(1,2)(3)
// 输出: 1,2,3
```

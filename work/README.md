#### 调用远程服务器图片的路径
> http://public.duduapp.net/duLifeImg/c-success.png

#### 今天写的react项目要介入到微信端调试，主要是为了远程数据的异步测试，需要使监听80端口
>- 但是npm start后，程序没跑起来，说是80端口被占用了，最后，启动了php study程序，才给弄好。
另外，要想在微信端调试，你的微信号还需要对应的公众号来对你进行绑定才行。这样你才有权在web开发者工具中进行对应公众号的开发和调试。
- 80端口是为HTTP开放的，此为上网冲浪使用次数最多的协议，主要用于万维网传输信息的协议。可以通过http地址加':80'来网问网站，因为
浏览网页服务默认的端口是80，所以只需输入网址即可，如果 www.google.com 和 www.google.com:80 效果一样！

### 2016-06-30 工作计划
> - 加载组件制作(思路，没有数据的话，则渲染这个组件)
> - 好店分类异步数据导入

### 数据引入api导致问题，需要把api里的网址改成dev
> 在middleware/api 中 `const API_ROOT = 'http://dev.dolife.me/api/web'`

### github 数据接口
> https://api.github.com/users/minooo
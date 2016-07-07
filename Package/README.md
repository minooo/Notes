> 在react前端开发过程中，经常会用到各种各样功能强劲的包，本文就列举他们做个记录————不定时更新。

### [babel-preset-es2015]()
**所有的es6插件的babel预设，有了它，诸如，es6的箭头函数，类，等等语法才能向es转换。**

    安装：`npm install --save-dev babel-preset-es2015`
    用法：.babelrc --> { "presets":["es2015"] }

### [babel-preset-es2015-loose](https://github.com/bkonkle/babel-preset-es2015-loose)
**一句话概括：一个babel预设，开启`babel-preset-es2015`松散模式，作用就是使es6转换成的es5更具有兼容性！**

    安装：`npm install --save-dev babel-preset-es2015-loose`
    用法：.babelrc --> { "presets":["es2015-loose"] }

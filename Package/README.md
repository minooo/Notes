> 在react前端开发过程中，经常会用到各种各样功能强劲的包，本文就列举他们做个记录————不定时更新。
    
### [babel-loader](https://github.com/babel/babel-loader)
**一句话概括：通过应用同级依赖babel和webpack，进而转译js文件。**

    安装： npm install install babel-loader babel-core webpack --save-dev  注意，babel-core 和 webpack 是必要的同级依赖。
    备注：自npm3.0之后，为了避免混乱，npm 拒绝自动安装同级依赖，所以要手动安装。

### [babel-core](https://github.com/babel/babel)
**一句话概括：这是babel的组成文件。**

    安装：npm install --save-dev babel-core
    
### [babel-preset-es2015](https://github.com/babel/babel)
**一句话概括：有了它，诸如，es6的箭头函数，类，等等语法特性才能向es5转换。**

    安装：`npm install --save-dev babel-preset-es2015`
    用法：.babelrc --> { "presets":["es2015"] }

### [babel-preset-es2015-loose](https://github.com/bkonkle/babel-preset-es2015-loose)
**一句话概括：使es6转译成的es5更具有兼容性！**

    安装：`npm install --save-dev babel-preset-es2015-loose`
    用法：.babelrc --> { "presets":["es2015-loose"] }
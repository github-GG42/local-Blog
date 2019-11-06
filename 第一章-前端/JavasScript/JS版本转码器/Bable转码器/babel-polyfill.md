# babel/polyfill 模块

#### `Babel`默认只转换新的`JavaScript`语法(syntax),而不转换新的API,比如`Iterator`,`Generator`,`Set`,`Map`,`Proxy`,`Symbol`,`Promise`等全局对象,以及一些定义在全局对象上的方法(比如`Object.assign`)都不会转码.

#### 如:`ES6`在`Array`对象上新增了`Array.from`方法.`Babel`就不会转码这个方法.如果想让这个方法运行,必须使用`babel-plyfill`,为当前环境提供一个垫片.

- 安装命令,如下:

  ```shell
  npm install --save-dev @babel/polyfill
  ```

- 然后,在脚本头部,加入如下一行代码.

  ```javascript
  import '@babel/polyfill';
  //或者
  require('@babel/polyfill');
  ```

**注意:`Babel`默认不转码的`API`非常多,详细清单可以查看`babel-plugin-transform-runtime`模块的`definitioins.js`文件**


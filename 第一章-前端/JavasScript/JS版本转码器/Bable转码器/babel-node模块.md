# babel-node模块

- `@babel/node`模块的`babel-node`命令,提供一个支持`ES6`的`REPL`环境.支持`Node`的`REPL`环境的所有功能,而且可以直接运行`ES6`代码

  1. 安装`@babel/node`模块

     ```shell
     npm install --save-dev @babel/node
     ```

  2. 然后,执行`babel-node`就进入`REPL`环境
  
     ```shell
     #进入ES6环境
     npx babel -node
     #编写ES6语法代码
     (x => x * 2)(1)
     2
     ```
  
  3. `babel-node` 命令可以直接运行`ES6`脚本.
  
     ```shell
     #es6.js的代码
     #console.log((x => x *2)(1))
     npx babel-node es6.js
     ```
  
     
  
#  babel/register 模块

- #### `@babel/register` 模块改写`require` 命令,为它加上一个钩子.为此,每当使用`require` 加载`.js` ,`.jsx` ,`.es` 和 `.es6` 后缀名的文件,就会先用`Babel` 进行转码.

  ```shell
  npm install --save-dev @babel/register
  ```

	##### 1.  使用时,必须首先加载`@babel/register`.
     ```javascript
      //index.js
       require('@babel/register');
       require('./es6.js');
     ```
  
	 ##### 2.  然后,就不需要手动对index.js转码了.

      node index.js
  
  **注意:`@babel/register`  只会对`require`命令加载的文件转码,而不会对当前文件转码.另外,由于它是实时转码,所以只适合于开发环境使用**

  


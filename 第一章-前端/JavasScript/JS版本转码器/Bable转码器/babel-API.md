# babel API

#### 如果某些代码需要调用`Babel` 的`API`进行转码,就要使用`@babel/core`模块.

```javascript
var babel = require('@babel/core');

//字符串转码
babel.transform('code()',options);
//=>{code,map,ast}

//文件转码(异步)
babel.transfomFile("filename.js",options,function(err,result){
   result;//=>{code,map,ast} 
});

//文件转码(同步)
babel.transformFileSync('filename,js',options);
//=>{code,map,ast}

//babel AST转码
babel.transformFromAst(ast,code,options);
//=>{code,map,ast}
```

配置对象`options`,可以参考[官网文档](http://babeljs.io/docs/usage/options/ "babel官网文档")

#### 示例:

```JavaScript
var es6Code = 'let x = n =>n + 1';
var es5Code = require('@babel/code')
	.transform(es6Code{
         presets:['@babel/env']
     })
     .code;
console.log(es5Code)
```

### **注意:以上代码中,`transform`方法的第一个参数是一个字符串,表示需要被转换的`ES6`代码,第二个参数是转换的配置对象.**


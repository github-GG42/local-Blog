# ES6声明变量的六种方法

#### 1.  `var`命令

#### 2.  `function`命令

#### 3.  `let`命令

ES6 新增了`let`命令，用来声明变量。它的用法类似于`var`，但是所声明的变量，只在`let`命令所在的代码块内有效。

#####  不存在变量提升

  `let`所声明的变量一定要在声明后使用，否则报错。

  ```javascript
  // var 的情况
  console.log(foo); // 输出undefined
  var foo = 2;
  
  // let 的情况
  console.log(bar); // 报错ReferenceError
  let bar = 2;
  ```

  

##### 暂时性死区

  只要块级作用域内存在`let`命令，它所声明的变量就“绑定”（binding）这个区域，不再受外部的影响。

  ```javascript
  var tmp = 123;
  
  if (true) {
    tmp = 'abc'; // ReferenceError
    let tmp;
  }
  ```

 ##### 不允许重复声明

  `let`不允许在相同作用域内，重复声明同一个变量。

  ```javascript
  // 报错
  function func() {
    let a = 10;
    var a = 1;
  }
  
  // 报错
  function func() {
    let a = 10;
    let a = 1;
  }
  ```

  不能在函数内部重新声明参数。

  ```javascript
  function func(arg) {
    let arg;
  }
  func() // 报错
  
  function func(arg) {
    {
      let arg;
    }
  }
  func() // 不报错
  ```

  

#### 4.  `const`命令

`const`声明一个只读的常量.一旦声明，常量的值就不能改变.与`let`命令特性一致.

```javascript
const PI = 3.1415;
PI // 3.1415

PI = 3;
// TypeError: Assignment to constant variable.
```



`const`声明的变量不得改变值，这意味着，`const`一旦声明变量，就必须立即初始化，不能留到以后赋值.

```javascript
const foo;
// SyntaxError: Missing initializer in const declaration
```

##### 不可重复声明

```javascript
var message = "Hello!";
let age = 25;

// 以下两行都会报错
const message = "Goodbye!";
const age = 30;
```

##### **本质**

`const`实际上保证的，并不是变量的值不得改动，而是变量指向的那个`内存地址所保存的数据`不得改动.

```javascript
const foo = {};

// 为 foo 添加一个属性，可以成功
foo.prop = 123;
foo.prop // 123

// 将 foo 指向另一个对象，就会报错
foo = {}; // TypeError: "foo" is read-only
```

如果真要将对象冻结,应该使用`Object.freeze`方法

```javascript
const foo = Object.freeze({});

// 常规模式时，下面一行不起作用；
// 严格模式时，该行会报错
foo.prop = 123;
```

除了将对象本身冻结,对象的属性也应该冻结.

```javascript
var constantize = (obj) => {
  Object.freeze(obj);
  Object.keys(obj).forEach( (key, i) => {
    if ( typeof obj[key] === 'object' ) {
      constantize( obj[key] );
    }
  });
};
```



#### 5.  `import`命令

#### 6.  `class`命令
# 查找DOM节点

## dojo.byId

> 通过ID属性选择一个DOM节点.

```JavaScript
//获取ID为demo的元素
dojo.byId("demo");
```

## dojo.query

> 接收一个字符串参数,使用一个CSS3选择器,可以为 CSS样式名称,或者标签名称
>
>
> 返回一个NodeList,通过遍历这个List来操作每个元素

```JavaScript
//根据样式名称
dojo.query(".class");
//根据标签名称
dojo.query("div")
```

## dojo.body

> 返回document的body元素

```JavaScript
//返回body元素
dojo.body();
```


# 动态创建DOM节点

## dojo.create

> 创建一个DOM节点
>
> dojo.create(str,attrs,refNode,pos);
>
> str:元素类型
> attrs:属性
> refNode:添加到哪里
> pos:添加到的位置
> 	pos取值:
>
> ![1571473618569](D:\总结\img\1571473618569.png)

```JavaScript
//创建一个div,并加载到body里,作为最后一个位置
dojo.create("div",{innerText:"dojo"},dojo.body());
```

## dojo.destroy

>从父元素中删除该元素,并删除掉该元素的所有子元素

```JavaScript
//删除节点及其所有子节点
let node = dojo.byId("node");
dojo.destroy(node);
```

## dojo.empty

> 删除该元素的所有子元素,保留父元素.

```JavaScript
//删除节点的所有子节点
let node = dojo.byId("node");
dojo.empty(node);
```


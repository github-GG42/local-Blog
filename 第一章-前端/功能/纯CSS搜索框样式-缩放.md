# 纯CSS搜索框样式-缩放

### `CSS`

```CSS
body {
  margin: 0;
  padding: 0;
  background: #ff5252;
}

.search__box {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: #2f3640;
  height: 40px;
  border-radius: 40px;
  padding: 10px 15px 10px 15px;
}

.search__box:hover > .search__txt {
  width: 240px;
  padding: 0 6px;
}

.search__box:hover > .search__btn {
  background: #fff;
}
.search__box:hover > .search__btn i {
  color: #34ace0;
  transition: 0.9s;
}

.search__btn {
  color: #e84118;
  float: right;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  background: #34ace0;
  display: flex;
  justify-content: center;
  align-item: center;
  text-decoration: none;
}
.search__btn i {
  line-height: 40px;
  color: #fff;
  transition: 0.9s;
}

.search__txt {
  border: none;
  background: none;
  outline: none;
  float: left;
  padding: 0;
  color: #fff;
  font-size: 16px;
  transition: 0.2s;
  line-height: 40px;
  width: 0;
}

```

### `HTML`

```html
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.3.1/css/all.css">
<div class="search__box">
    <input class="search__txt" type="text" name="" placeholder="Type to search">
    <a class="search__btn" href="#">
        <i class="fas fa-search"></i>
    </a>
</div>
```

### 效果

![1572427769275](../../img/1572427769275.png)

![1572427784759](../../img/1572427784759.png)
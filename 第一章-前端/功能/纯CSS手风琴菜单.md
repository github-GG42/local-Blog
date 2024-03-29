# 纯CSS手风琴菜单

### `CSS`

```css
*{
    margin: 0;
    padding: 0;
    font-family: 'lato';
    list-style: none;
    text-decoration: none;
}
body{
    background-color: #fcdc29;
}

.wrapper{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
.mainMenu{
    width: 250px;
    display: block;
    border-radius: 10px;
    overflow: hidden;
}
.item{
    border-top: 1px solid #ef584a;
    overflow: hidden;
}
.btn{
    display: block;
    padding: 15px 20px;
    background-color: #ff6f61;
    color: #fff;
    position: relative;

}
.btn:before{
    content: '';
    position: absolute;
    width: 0;
    height: 0;
    border-left: 8px solid transparent;
    border-right:8px solid transparent;
    border-top:10px solid #ff6f61;
    right: 15px;
    bottom: -10px;
    z-index: 9;
    
}
.btn i {
    margin-right: 10px;
}
.subMenu{
    background: #273057;
    overflow: hidden;
    transition: max-height 0.7s;
    max-height: 0;
}
.subMenu a{
    display: block;
    padding: 15px 20px;
    color: #fff;
    font-size: 14px;
    border-bottom: 1px solid #394c7f;
    position: relative;
    
}
.subMenu a:before{
    content: '';
    opacity: 0;
    transition: opacity 0.3s;

}
.subMenu a:hover:before{
    content: '';
    position: absolute;
    height: 0;
    width: 6px;
    left: 0;
    top:0;
    opacity: 1;
    /* background-color: #d8d824; */
    border-top: 24px solid transparent;
    border-left: 11px solid #fcdc29;
    border-bottom: 24px solid transparent;
}
.subMenu a:after{
    content: '';
    opacity: 0;
    transition: opacity 0.3s;

}
.subMenu a:hover:after{
    content: '';
    position: absolute;
    height: 0;
    width: 6px;
    right: 0px;
    top:0;
    opacity: 1;
    /* background-color: #d8d824; */
    border-top: 24px solid transparent;
    border-right: 11px solid #fcdc29;
    border-bottom: 24px solid transparent;
}
.subMenu a:hover{
    background: #273057;
    background: -moz-linear-gradient(top, #273057 0%, #273057 50%, #394c7f 51%, #394c7f 100%);
    background: -webkit-linear-gradient(top, #273057 0%,#273057 50%,#394c7f 51%,#394c7f 100%);
    background: linear-gradient(to bottom, #273057 0%,#273057 50%,#394c7f 51%,#394c7f 100%);
    filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#273057', endColorstr='#394c7f',GradientType=0 );
    transition: all 0.3s;
    border-bottom: 1px solid #394c7f;
}
.subMenu a:last-child{
    border:none;
}
.item:target .subMenu{
    max-height: 10em;
}

```

### `HTML`

```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.8.1/css/all.min.css">
    <div class="wrapper">
        <ui class="mainMenu">
            <li class="item" id="account">
                <a href="#account" class="btn"><i class="fas fa-user-circle"></i>My Account</a>
                <div class="subMenu">
                    <a href="">item-1</a>
                    <a href="">item-2</a>
                    <a href="">item-3</a>
                </div>
            </li>
            <li class="item" id="about">
                <a href="#about" class="btn"><i class="fas fa-address-card"></i>About</a>
                <div class="subMenu">
                    <a href="">item-1</a>
                    <a href="">item-2</a>
                </div>
            </li>
            <li class="item" id="support">
                <a href="#support" class="btn"><i class="fas fa-info"></i>Support</a>
                <div class="subMenu">
                    <a href="">item-1</a>
                </div>
            </li>
            <li class="item">
                <a href="#" class="btn"><i class="fas fa-sign-out-alt"></i>Log Out</a>
            </li>
        </ui>
    </div>
```

### 效果

![1572427075805](../../img/1572427075805.png)
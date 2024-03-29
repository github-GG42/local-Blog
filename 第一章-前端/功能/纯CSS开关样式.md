# 纯CSS开关样式

### `CSS`

```css
@import "https://fonts.googleapis.com/css?family=Raleway";
.switch-box {
  display: block;
  margin-top: 24px;
}
.switch-box .switch-box-slider {
  position: relative;
  display: inline-block;
  height: 8px;
  width: 32px;
  background: #d5d5d5;
  border-radius: 8px;
  cursor: pointer;
  transition: all 0.2s ease;
}
.switch-box .switch-box-slider:after {
  position: absolute;
  left: -8px;
  top: -8px;
  display: block;
  width: 24px;
  height: 24px;
  border-radius: 50%;
  background: #eeeeee;
  box-shadow: 0px 2px 2px rgba(0, 0, 0, 0.2);
  content: '';
  transition: all 0.2s ease;
}
.switch-box .switch-box-input {
  display: none;
}
.switch-box .switch-box-input ~ .switch-box-label {
  margin-left: 8px;
}
.switch-box .switch-box-input:checked ~ .switch-box-slider:after {
  left: 16px;
}
.switch-box .switch-box-input:disabled ~ .switch-box-slider {
  background: #e2e2e2;
  cursor: default;
}
.switch-box .switch-box-input:disabled ~ .switch-box-slider:after {
  background: #d5d5d5;
}
.switch-box.is-primary .switch-box-input:checked:not(:disabled) ~ .switch-box-slider {
  background: #28e1bd;
}
.switch-box.is-primary .switch-box-input:checked:not(:disabled) ~ .switch-box-slider:after {
  background: #1abc9c;
}
.switch-box.is-info .switch-box-input:checked:not(:disabled) ~ .switch-box-slider {
  background: #5faee3;
}
.switch-box.is-info .switch-box-input:checked:not(:disabled) ~ .switch-box-slider:after {
  background: #3498db;
}
.switch-box.is-success .switch-box-input:checked:not(:disabled) ~ .switch-box-slider {
  background: #54d98c;
}
.switch-box.is-success .switch-box-input:checked:not(:disabled) ~ .switch-box-slider:after {
  background: #2ecc71;
}
.switch-box.is-danger .switch-box-input:checked:not(:disabled) ~ .switch-box-slider {
  background: #ed7669;
}
.switch-box.is-danger .switch-box-input:checked:not(:disabled) ~ .switch-box-slider:after {
  background: #e74c3c;
}
.switch-box.is-warning .switch-box-input:checked:not(:disabled) ~ .switch-box-slider {
  background: #eb9950;
}
.switch-box.is-warning .switch-box-input:checked:not(:disabled) ~ .switch-box-slider:after {
  background: #e67e22;
}

body {
  background: aquamarine; 
  font-family: Raleway, Arial, sans-serif;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

```

### `HTML`

```html
<h1>Pure CSS switches</h1>
<div class="container">
  <div class="switch-box">
    <input id="default" class="switch-box-input" type="checkbox" />
    <label for="default" class="switch-box-slider"></label>
    <label for="default" class="switch-box-label">Default</label>
  </div>
  <div class="switch-box is-primary">
    <input id="primary" class="switch-box-input" type="checkbox" checked />
    <label for="primary" class="switch-box-slider"></label>
    <label for="primary" class="switch-box-label">Primary</label>
  </div>
  <div class="switch-box is-info">
    <input id="info" class="switch-box-input" type="checkbox" checked />
    <label for="info" class="switch-box-slider"></label>
    <label for="info" class="switch-box-label">Info</label>
  </div>
  <div class="switch-box is-success">
    <input id="success" class="switch-box-input" type="checkbox" checked />
    <label for="success" class="switch-box-slider"></label>
    <label for="success" class="switch-box-label">Success</label>
  </div>
  <div class="switch-box is-danger">
    <input id="danger" class="switch-box-input" type="checkbox" checked />
    <label for="danger" class="switch-box-slider"></label>
    <label for="danger" class="switch-box-label">Danger</label>
  </div>
  <div class="switch-box is-warning">
    <input id="warning" class="switch-box-input" type="checkbox" checked />
    <label for="warning" class="switch-box-slider"></label>
    <label for="warning" class="switch-box-label">Warning</label>
  </div>
  <div class="switch-box is-primary">
    <input id="disabled" class="switch-box-input" type="checkbox" checked disabled />
    <label for="disabled" class="switch-box-slider"></label>
    <label for="disabled" class="switch-box-label">Disabled</label>
  </div>
</div>
```

### 效果

![1572425382639](../../img/1572425382639.png)
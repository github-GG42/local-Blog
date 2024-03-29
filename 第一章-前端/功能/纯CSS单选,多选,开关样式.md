# 纯CSS单选,多选,开关样式

### `CSS`

```CSS
@supports (-webkit-appearance: none) or (-moz-appearance: none) {
  input[type='checkbox'],
  input[type='radio'] {
    --active: #5628EE;
    --active-inner: #fff;
    --input-border: #CDD9ED;
    --input-border-hover: #23C4F8;
    --background: #fff;
    --disabled: #F5F9FF;
    --disabled-inner: #E4ECFA;
    --shadow-inner: rgba(18, 22, 33, .1);
    height: 21px;
    outline: none;
    position: relative;
    -webkit-appearance: none;
    -moz-appearance: none;
    margin: 0;
    padding: 0;
    box-shadow: none;
    cursor: pointer;
    height: 21px;
    border: 1px solid var(--input-border);
    background: var(--background);
    transition: background .3s ease, border-color .3s ease;
  }
  input[type='checkbox']:after,
  input[type='radio']:after {
    content: '';
    display: block;
    left: 0;
    top: 0;
    position: absolute;
    transition: opacity .2s ease, -webkit-transform .3s ease, -webkit-filter .3s ease;
    transition: transform .3s ease, opacity .2s ease, filter .3s ease;
    transition: transform .3s ease, opacity .2s ease, filter .3s ease, -webkit-transform .3s ease, -webkit-filter .3s ease;
  }
  input[type='checkbox']:checked,
  input[type='radio']:checked {
    background: var(--active);
    border-color: var(--active);
  }
  input[type='checkbox']:checked:after,
  input[type='radio']:checked:after {
    -webkit-filter: drop-shadow(0 1px 2px var(--shadow-inner));
            filter: drop-shadow(0 1px 2px var(--shadow-inner));
    transition: opacity 0.3s ease, -webkit-filter 0.3s ease, -webkit-transform 0.6s cubic-bezier(0.175, 0.88, 0.32, 1.2);
    transition: opacity 0.3s ease, filter 0.3s ease, transform 0.6s cubic-bezier(0.175, 0.88, 0.32, 1.2);
    transition: opacity 0.3s ease, filter 0.3s ease, transform 0.6s cubic-bezier(0.175, 0.88, 0.32, 1.2), -webkit-filter 0.3s ease, -webkit-transform 0.6s cubic-bezier(0.175, 0.88, 0.32, 1.2);
  }
  input[type='checkbox']:disabled,
  input[type='radio']:disabled {
    cursor: not-allowed;
    opacity: .9;
    background: var(--disabled);
  }
  input[type='checkbox']:disabled:checked,
  input[type='radio']:disabled:checked {
    background: var(--disabled-inner);
    border-color: var(--input-border);
  }
  input[type='checkbox']:hover:not(:checked):not(:disabled),
  input[type='radio']:hover:not(:checked):not(:disabled) {
    border-color: var(--input-border-hover);
  }
  input[type='checkbox']:not(.switch),
  input[type='radio']:not(.switch) {
    width: 21px;
  }
  input[type='checkbox']:not(.switch):after,
  input[type='radio']:not(.switch):after {
    opacity: 0;
  }
  input[type='checkbox']:not(.switch):checked:after,
  input[type='radio']:not(.switch):checked:after {
    opacity: 1;
  }

  input[type='checkbox']:not(.switch) {
    border-radius: 6px;
  }
  input[type='checkbox']:not(.switch):after {
    width: 5px;
    height: 9px;
    border: 2px solid var(--active-inner);
    border-top: 0;
    border-left: 0;
    left: 7px;
    top: 4px;
    -webkit-transform: rotate(20deg);
            transform: rotate(20deg);
  }
  input[type='checkbox']:not(.switch):checked:after {
    -webkit-transform: rotate(43deg);
            transform: rotate(43deg);
  }
  input[type='checkbox'].switch {
    width: 38px;
    border-radius: 11px;
  }
  input[type='checkbox'].switch:after {
    left: 2px;
    top: 2px;
    border-radius: 50%;
    width: 15px;
    height: 15px;
    background: var(--input-border);
  }
  input[type='checkbox'].switch:checked:after {
    background: var(--active-inner);
    -webkit-transform: translateX(17px);
            transform: translateX(17px);
  }
  input[type='checkbox'].switch:disabled:not(:checked):after {
    opacity: .6;
  }

  input[type='radio'] {
    border-radius: 50%;
  }
  input[type='radio']:after {
    width: 19px;
    height: 19px;
    border-radius: 50%;
    background: var(--active-inner);
    opacity: 0;
    -webkit-transform: scale(0.7);
            transform: scale(0.7);
  }
  input[type='radio']:checked:after {
    background: var(--active-inner);
    -webkit-transform: scale(0.5);
            transform: scale(0.5);
  }
}
ul {
  margin: 12px;
  padding: 0;
  list-style: none;
  width: 100%;
  max-width: 360px;
}
ul li {
  margin: 12px 0;
  padding-left: 48px;
  position: relative;
}
ul li input[type='checkbox'],
ul li input[type='radio'] {
  position: absolute;
  left: 0;
  top: 0;
}
ul li input[type='text'] {
  line-height: 21px;
  border: 0;
  margin: 0;
  padding: 0;
  font-size: 12px;
  color: #6C7486;
  background: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  outline: none;
  width: 100%;
  font-family: 'Source Sans Pro', Arial;
}

html {
  box-sizing: border-box;
}

* {
  box-sizing: inherit;
}
*:before, *:after {
  box-sizing: inherit;
}

body {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: #F5F9FF;
}
@media (max-width: 800px) {
  body {
    flex-direction: column;
  }
}

```

### `HTML`

```html
<ul>
    <li>
        <input type="checkbox">
        <input type="text" readonly value='<input type="checkbox">'>
    </li>
    <li>
        <input type="checkbox" checked>
        <input type="text" readonly value='<input type="checkbox" checked>'>
    </li>
    <li>
        <input type="radio" name="radio" value="1">
        <input type="text" readonly value='<input type="radio">'>
    </li>
    <li>
        <input type="radio" name="radio" value="2" checked>
        <input type="text" readonly value='<input type="radio" checked>'>
    </li>
    <li>
        <input type="checkbox" class="switch">
        <input type="text" readonly value='<input type="checkbox" class="switch">'>
    </li>
    <li>
        <input type="checkbox" class="switch" checked>
        <input type="text" readonly value='<input type="checkbox" class="switch" checked>'>
    </li>
</ul>

<ul>
    <li>
        <input type="checkbox" disabled>
        <input type="text" readonly value='<input type="checkbox" disabled>'>
    </li>
    <li>
        <input type="checkbox" checked disabled>
        <input type="text" readonly value='<input type="checkbox" checked disabled>'>
    </li>
    <li>
        <input type="radio" name="radio1" value="1" disabled>
        <input type="text" readonly value='<input type="radio" disabled>'>
    </li>
    <li>
        <input type="radio" name="radio1" value="2" checked disabled>
        <input type="text" readonly value='<input type="radio" checked disabled>'>
    </li>
    <li>
        <input type="checkbox" class="switch" disabled>
        <input type="text" readonly value='<input type="checkbox" class="switch" disabled>'>
    </li>
    <li>
        <input type="checkbox" class="switch" checked disabled>
        <input type="text" readonly value='<input type="checkbox" class="switch" checked disabled>'>
    </li>
</ul>
```

### 效果

![1572427692150](../../img/1572427692150.png)
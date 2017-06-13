# Toptip

wepy 的插件使用不是很人性化，但还是能用的~ 要不然我也不会写这个东西。


## 使用方法

```js
// 第一步
import Toptip from '../../components/weui/toptip'

// 第二步，加入 components
components = {
  toptip: Toptip,
}

// 第三步，把这一行放到 template 某一个位置， 最后就可以
<toptip></toptip>

// 第四步，正式调用，this 指的是当前组件
let promise = this.$invoke('toptip', 'show', {
  type: 'success',
  text: '成功了~',
});
```


## Options

```js
let promise = this.$invoke('toptip', 'show', {
  duration: 1000,  // 可选
  type: 'success', // 可选. 或者 'error'
  text: '成功了~', // 随便写什么~
});
```

## 样式

我用的是 weui 的样式，如果你没有用，那么就要把下面的 css，加到 style 里面去

```css
.weui-toptips {
  position: fixed;
  transform: translateZ(0) translateY(-100%);
  top: 0;
  left: 0;
  right: 0;
  padding: 5px;
  font-size: 14px;
  text-align: center;
  color: #FFFFFF;
  z-index: 5000;
  word-wrap: break-word;
  word-break: break-all;
}

.weui-toptips_warn {
  background-color: #E64340;
}

.weui-toptips_success {
  background-color: #1AAD19;
}
```

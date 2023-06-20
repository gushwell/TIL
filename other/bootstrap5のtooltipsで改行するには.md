# bootstrap5のtooltipsで改行するには

Bootstrap 5のツールチップは、デフォルトでは`<br>`タグが有効にならない。
これに対応する方法は以下の通り。

HTML
```html
<button type="button" class="btn btn-primary" data-bs-toggle="tooltip" data-bs-html="true" title="ライン1<br>ライン2">
    ツールチップを表示する
</button>
```

data-bs-html="true"属性と`<br>`タグを使用して、改行を有効にする。

<br>

JavaScript

```js
var tooltipTriggerList = [].slice.call(document.querySelectorAll('[data-bs-toggle="tooltip"]'))
var tooltipList = tooltipTriggerList.map(function (tooltipTriggerEl) {
  return new bootstrap.Tooltip(tooltipTriggerEl, {
    sanitize: false,
    customClass: 'tooltip-multiline',
    template: '<div class="tooltip tooltip-multiline" role="tooltip"><div class="tooltip-arrow"></div><div class="tooltip-inner"></div></div>'
  })
})
```
<br>

CSS
```css
.tooltip-multiline .tooltip-inner {
  white-space: pre-wrap;
}
```


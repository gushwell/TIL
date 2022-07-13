
bootstrap.Modelオブジェクトを生成してから、showメソッドでダイアログをオープンする。


```js
const elem = document.getElementById('myDialog');
const modal = new bootstrap.Modal(elem);
modal.show();
```



```html
<div class="modal fade" id="myDialog" data-bs-backdrop="static" data-bs-keyboard="false"
     ...
</div>
     
```

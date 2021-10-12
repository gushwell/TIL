# Razor Pagesで一つのページで複数のformを使う

asp-page-handler タグヘルパーを利用することで、別のPostメソッドを呼び出すことができる。

### .cshtml側

```html

<form method="post" asp-page-handler="view">
   ...
   <button type="submit">View</button>
</form>  
<form method="post"  asp-page-handler="edit">
   ...
   <button type="submit">Edit</button>
</form>  
```

### .cshtml.cs 側

asp-page-handlerで指定した名前をメソッド名に付加します。


```cs
public async Task<IActionResult> OnPostViewAsync()
{
    ...
}
public async Task<IActionResult> OnPostEditAsync()
{
    ...
}
```

なお、asp-page-handler タグヘルパーは、一つのform内でも利用できる、

```html

<form method="post" >
   ...
   <button type="submit" asp-page-handler="view">View</button>
   <button type="submit"  asp-page-handler="edit">Edit</button>
</form>  
```

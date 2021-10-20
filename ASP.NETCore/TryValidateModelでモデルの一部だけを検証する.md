TryValidateModelメソッドを使うと、任意のタイミングでモデルの一部だけを検証することができます。

例えば、ViewModelが以下のように定義されていたとします。

```cs
class ViewModel {
    public ViewModel_A ViewModel_A { get; set; }
    public ViewModel_B ViewModel_B { get; set; }
}

class ViewModel_A {
    [Required]
    [MaxLength(20)]
    public string Text01 { get; set; }
    [Required]
    [MaxLength(20)]
    public string Text02 { get; set; }
}
class ViewModel_B {
    [Required]
    [MaxLength(20)]
    public string Text03 { get; set; }
    [Required]
    [MaxLength(20)]
    public string Text04 { get; set; }
}
```

このViewModelの検証は、通常、以下のようにModelState.IsValidで検証結果を判断します。

```cs
   public IActionResult OnPost([FromForm] string action) {
       if (!ModelState.IsValid) 
       {
           return Page();
       }
       ...
   }
```

しかし、場合によっては、ViewModel_B だけを検証したい場合もあります。そんな時に、TryValidateModel メソッドを使います。

こんなふうなコードになります。Dataは、ViewModel型のオブジェクトと仮定します。

```cs
   public IActionResult OnPost([FromForm] string action) {
       this.ModelState.Clear();
       if (!this.TryValidateModel(this.Data.ViewModel_B))
       {
           return Page();
       }
       ...
   }
```

`this.ModelState.Clear();`を呼び出しているのは、ViewModel_Aの検証状態をクリアするためです。
いったんすべてModelStateの状態をクリアしてから、TryValidateModel メソッドを呼び出せば、ModelStateには、ViewModel_Bの検証結果だけが設定されます。



```

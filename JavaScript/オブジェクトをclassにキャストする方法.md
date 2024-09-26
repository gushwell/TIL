# オブジェクトをclassにキャストする方法

JavaScriptには他の言語（例えばC++やJava）のような明示的なキャスト構文は存在しない。

JavaScriptでは、オブジェクトのプロトタイプを変更することで、あるオブジェクトを特定のクラスのインスタンスとして扱うことができる。

厳密にはキャストとは異なるが、実質的には同じ効果がある。

```js
class MyClass {
  constructor(name) {
    this.name = name;
  }

  greet() {
    console.log(`Hello, ${this.name}!`);
  }
}

// 通常のオブジェクト
const obj = {
  name: 'Alice'
};

// オブジェクトのプロトタイプを変更してMyClassのインスタンスとして扱う
Object.setPrototypeOf(obj, MyClass.prototype);

// これでobjはMyClassのインスタンスとして扱われる
obj.greet(); // 出力: Hello, Alice!
```

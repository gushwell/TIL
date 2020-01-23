# xUnitとMoqを使う準備

## Nuget パッケージで以下のものをインストール

- xUnit
- xunit.runner.visualstudio
- Moq

## テストプロジェクト作成

1. 新規プロジェクトで、プロジェクトの種類で「テスト」を選択
2. 「xUnitテスト プロジェクト (.NET Core)」を選択
3. [次へ] - [作成]

## コードを書く


```
using Xunit;
using Moq;

…
   [Fact]
    public void TestHello() { }

…
   [Theory]
    public void TestHello2() { }

```


[Fact] [Theory]属性があれば、Visual Studio のテストエクスプローラがテストとして認識してくれる

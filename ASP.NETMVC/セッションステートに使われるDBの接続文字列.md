System.Web.IPartitionResolver を継承して、ResolvePartition メソッドを実装すれば、
セッションステートに使われるDBの接続文字列を指定することができる。

これ、知らなかった。

```c#
    [Serializable]
    public class PartitionResolver : System.Web.IPartitionResolver {
		public void Initialize() { }

        public String ResolvePartition(Object key) {
	         return "Data Source=myServerAddress;Initial Catalog=myDataBase;" + 
                 "User Id=myUsername;Password=myPassword;"; 		
        }
    }
```

これを使えば、極端な話、アプリのDBの中に、ステート情報を入れることもできる。

そして、web.configに、以下のような記述を追加する。


```
 <system.web>
    ...
    <sessionState mode="SQLServer" allowCustomSqlDatabase="true" partitionResolverType="XXX.XXX.PartitionResolver" timeout="10" />
  </system.web>
```

# ページが閉じるときのイベントでAjax通信

`beforeunload`や`unload'イベントなど、一部のイベントでは、XMLHttpRequest などを使った通常の Ajax通信ができない。

その代替えとして、これらのイベントの中では navigator.sendBeacon を使う必要がある。

```js
navigator.sendBeacon(url, data);
```

**url**  
data が送られる解決済みの URL を示します。

**data**  
送るデータを含む ArrayBuffer, ArrayBufferView, Blob, DOMString, FormData, ReadableStream, URLSearchParams のいずれかのオブジェクトです。

戻り値は、ユーザーエージェントが転送キューにデータを入れられた時は true を返します。それ以外の時は false を返します。

MDN web docs からの抜粋
> sendBeacon() メソッドを使うことで、アンロードが遅延したり次のナビゲーションにパフォーマンスの影響を与えたりすることなく、ユーザーエージェントが転送できる時に、データは非同期にウェブサーバーに転送されます。これはアナリティクスデータの送信に関する全ての問題を解決します。データは確実に、非同期に、そして次のページの読み込みに影響を与えずに送信されます。さらに、そのコードは、実際に他のどんなテクニックよりも簡単です。

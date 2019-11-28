## CIDR 表記

Classless Inter-Domain Routing の略

[wikipedia](https://ja.wikipedia.org/wiki/Classless_Inter-Domain_Routing) から抜粋

> Classless Inter-Domain Routing（CIDR、サイダー）は、インターネット上のルーターにおけるルーティングテーブルの肥大化速度を低減させるための機構であり、ISPや組織にクラスA、B、Cを全部ではなく部分的に割り当てることでIPアドレスの浪費を防ぐ機構である。CIDR記法でアドレスを記述でき、アドレスの集約的表現が可能で、アドレスブロックの委譲も容易である。

208.128.0.0/24 のように、IPアドレスの後ろに  / と数字を書く表記

/ の後ろの数字は、サブネットマスクの長さを指定する。

24の場合は、先頭から 24bit が固定されるので、

208.128.0.0 - 208.128.0.255 までのアドレスの範囲を表していることになる。


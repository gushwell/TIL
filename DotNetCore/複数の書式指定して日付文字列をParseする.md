# 複数の書式指定して日付文字列をParseする

DateTime.TryParseExactメソッドを使うと簡単にParseできる。

```cs
using System;
using System.Globalization;

namespace ConsoleApp8 {
    class Program {
        static void Main(string[] args) {
            Console.WriteLine(ToDate("20200123"));
            Console.WriteLine(ToDate("2020/01/23"));
            Console.WriteLine(ToDate("2020-01-23 10:15:20"));
            Console.WriteLine(ToDate("2020/01/23 10:15:20"));
        }

        static DateTime ToDate(string value) {
            string[] formats = { "yyyyMMdd", "yyyy-MM-dd", "yyyy/MM/dd", "yyyy-MM-dd H:m:s", "yyyy/MM/dd H:m:s" };
            if (DateTime.TryParseExact(value, formats, null, DateTimeStyles.None, out var result))
                return result;
            return default;
        }
    }
}

```

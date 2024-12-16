# 標準出力

## 標準出力とは？
標準出力（Standard Output）とは、プログラムがコンソール情報を出力する仕組み。

Javaでは`System.out`というオブジェクトが用意されている。

## `System.out`の仕組み

- `System`：Javaの標準クラス（`java.lang.System）
- `System.out`：Systemクラスの静的フィールドで、`PrintStream`型である

型の宣言
```
public static final PrintStream out;
```

Javaでは、`System.out.println`、`System.out.print`を使用して標準出力を行う。

1. println
   
`System.out.println()`：指定した文字列や値を出力し、最後に改行を行う。

ソースコード
```
System.out.println(1);
System.out.println(2);
```

出力結果
```
1
2
```

2.  print

`System.out.print`：指定した文字列や値を出力し、最後に改行を行わない。

ソースコード
```
System.out.print(1);
System.out.print(2);
```

出力結果
```
1
2
```

3. printf
   
`System.out.printf()`：フォーマット指定子を使って出力内容をカスタマイズする。

フォーマット指定子の例

|指定子|説明|引数例|出力例|
|:-:|:-:|:-:|:-:|
|%d|整数を10進数で出力|("%d", 42)|42|
|%f|小数を10進数で出力（デフォルト6桁）|("%.2f", 3.14159)|3.14|
|%s|文字列|("%s", "Hello")|Hello|
|%c|文字を1つ出力|("%c", 'A')|A|
|%b|真偽値|("%b", true)|true|
|%x|16進数（小文字）|("%x", 255)|ff|
|%X|16進数（大文字）|("%x", 255)|FF|
|%o|8進数|("%o", 255)|377|
|%e|指数表記（小文字e）|("%e", 12345.678)|1.234568e+04|
|%E|指数表記（大文字E）|("%E", 12345.678)|1.234568E+04|
|%%|%と出力|("%%")|%|

ソースコード
```
System.out.printf("%x", 127);
```

出力結果
```
7f
```
## 標準出力エラーとの違い
Javaにはもうひとつ似たようなオブジェクトがある。
標準エラー出力とは、プログラムが使うデータの内エラーの出力先を意味する。
- `System.err`：エラーや警告メッセージを出力するためのストリーム
- 動作は`System.out`と同じだが、通常は別のストリームに出力される
  
ソースコード
```
System.out.println("通常のメッセージ");
 System.err.println("エラーメッセージ");
```

出力結果
```
通常のメッセージ
エラーメッセージ
```

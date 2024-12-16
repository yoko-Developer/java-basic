# Hello World



## 目的

- Javaの基本的なコード構造を理解する。
- Javaプログラムを作成し、コンソールに `Hello World`と出力する方法を学ぶ。

## Javaプログラムとは

Javaは、クラスを基本単位とするオブジェクト指向のプログラミング言語。

## Hello Worldプログラムを作る
はじめに`Hello World`と出力するプログラムを作成する。

プログラムは以下の要素で構成されている。

- クラス(Class)：プログラムの部品を定義
- メソッド(Method)：振る舞いを記述
- mainメソッド：プログラムの実行が始まる特別なメソッド

## Hello Worldプログラムの作成

早速コンソールに `Hello World` と表示するプログラムを作成してみよう。

1. ファイルを準備

以下のコードをテキストエディタで作成し、 `Main.java` という名前を付けて保存する。
```
public class Main {
    public static void main(String[] args) {
        // コンソールにHello Worldと出力
        System.out.println("Hello World")
    }
}
```

2. コンパイル

Javaコンパイラを使用してコードをコンパイルし、クラスファイル(.class)を生成する。

ターミナルで`javac ファイル名`を実行すると、Main.classが生成される。
```
javac Main.java
```

3. クラスファイルを実行

生成されたクラスファイルを実行する
```
java Main
```

4. 出力

プログラムを実行すると`Hello World`と出力される。

```
Hello World
```


## お作法

- クラス名とファイル名は一致させる必要がある。（例：Mainクラスの場合、Main.javaとする）
- クラス名は大文字はじまり。
- セミコロン（;）はすべてのステートメントの末尾に必要。
- Javaプログラムは、mainメソッドが実行の入り口となる。
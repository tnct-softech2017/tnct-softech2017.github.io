---
layout: page
title: プログラミング実習の進め方
permalink: /howto/
---

## ログインする

### Windows端末にログインする
Windows端末にログインする。  
ユーザ名 / パスワードはCAI室のものとは別なので注意すること。

### jocalc1にログインする
TeraTermを開いて、新しい接続の設定が以下のスクリーンショットのようになっていることを確認する。  
ホスト名が間違っていて接続できないことが多いです。ホスト名がjocalc1になっていることを確認すること。

![teraterm起動画面]({{site.baseurl}}/images/teraterm1.jpg)


## コーディングする
TeraPadを使ってコーディングする。

保存する際は、【ファイル】->【文字/改行コード指定保存】を選択し、文字コードを"UTF-8N"にして保存すること。

![文字/改行コード指定保存を選択]({{site.baseurl}}/images/save1.jpg)
![UTF-8Nを指定する]({{site.baseurl}}/images/save2.jpg)

また、保存する際はファイルの種類に【すべてのファイル(\*.\*)】を選択すること。（ファイル名も ".c" と拡張子をつけること。）

![すべてのファイル(\*.\*)を選択すること]({{site.baseurl}}/images/save3.jpg)


## コンパイルする

### 作業ディレクトリに移動する
cdコマンドを使って、作業ディレクトリ（softech_prog）に移動する。

```
$ cd softech_prog
```

lsコマンドを使って、先ほど保存したファイルが存在することを確認する。

```
$ ls
```

### コンパイルする
jocalc1上で、以下のコマンドを打つ。

```
$ gcc -o hello hello.c
```


コンパイルエラーが出たら対処する。  
よくあるエラーは以下のとおり。

- セミコロン忘れ
- 関数名や変数名のスペルミス（宣言した変数名と、実際に使用する変数名は合っていますか？）
- #includeやreturnなど、おまじないのスペルミス

## コンパイルできない時(実習室限定)

もし初めてjocalcでコンパイルする時、変なエラーが出て、コンパイルできない時は以下のコマンドを打ち込んでみましょう

```
$ cd
$ cp /home/student/.cshrc ~/
$ source ~/.cshrc
```

## 実行する
コンパイルしたプログラムを実行するには、jocalc1上で以下のコマンドを入力する。

```
$ ./hello
```

出力結果を確認する。




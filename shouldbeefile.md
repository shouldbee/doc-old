# Shouldbeefile

Shouldbeefileは、テストのシナリオを記述したMarkdown形式のファイルのことです。

## Shouldbeefileの形式

Shouldbeefileは3つのパートからなります。

1. テスト環境設定
*  シナリオ
*  コメント 

![shouldbeefile-format.png]

### 1. テスト環境設定

テスト実行には、`url` と `envrionment` の2つの設定をShouldbeefileにリスト形式で書きます。

例:

```
* url: http://shouldbee.at/tutorial/
* environment: windows:chrome
```

`url`は、テスト対象サイトのURLです。
`environment`は、テストを実行するOSとブラウザの組み合わせで、次の環境が指定できます。

* `windows:chrome` ... Windows + Google Chrome
* `windows:firefox` … Windows + Firefox
* `windows:ie` ... Windows + Internet Explorer 9


	
### 2. シナリオ

シナリオは、テスト実施の手順を記述する部分です。

* <code>```</code> で囲まれたコードブロックがひとつのシナリオとして実行されます。
* 1行ごとに1ステップの処理を書きます。

例:

<pre><code>```
「/login」に移動する
「username」フィールドに「admin」と入力する
「password」フィールドに「pass」と入力する
「ログイン」ボタンをクリックする
画面に「管理メニュー」と表示されていること
```
</code></pre>

### 3. コメント

コメントの部分は見出しを書いたり、ドキュメントを残したりするために使います。

* コードブロック以外の部分は、コメント扱いになります。
* コードブロック内でも、`#` で始まる行はコメント扱いにになります。


[shouldbeefile-format.png]: https://github.com/shouldbee/shouldbee/raw/master/images/shouldbeefile-format.png

## 続き

* 利用可能なステップについて知りたい → [Steps]

[Steps]: https://github.com/shouldbee/shouldbee/blob/master/steps.md
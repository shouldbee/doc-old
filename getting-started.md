# Getting Started

ShouldBeeでは、テストを実行するコマンドツールを提供しています。このコマンドツールを実行すると、ShouldBee上のブラウザから対象サイトにテストを実施することができます。

## インストール

インストール方法は、Homebrewでインストールする方法と、wgetでインストールする方法の2通りあります。どちらかお好きなほうでインストールを行なってください。

### 1. Homebrewでインストール

```
brew tap shouldbee/shouldbee
brew install shouldbee
```

### 2. wgetでインストール

```
wget https://github.com/shouldbee/homebrew-shouldbee/raw/master/build/darwin-amd64/shouldbee
chmod +x shouldbee
```

## ログイン情報を設定しよう

ShouldBeeでテストを実行する際に、ShouldBeeのユーザ名・パスワードによる認証が必要になります。~/.bashrc, ~/.zshrcなどに環境変数 `SHOULDBEE_USERNAME`、`SHOULDBEE_PASSWORD`を定義しておいてください。Windowsは、[Windows7で環境変数を設定する方法]をご覧ください。

```bash
export SHOULDBEE_USERNAME="your_username"
export SHOULDBEE_PASSWORD="your_password"
```


## shouldbeeコマンドを試してみよう



### 1. Shouldbeefileを作る

Shouldbeefileとは: テストの手順を書いたMarkdown形式のファイルです。次のコマンドでShouldbeefileを作成します。

```
shouldbee init
```

### 2. テストを実行してみよう

次のコマンドを実行するとテストが始まります。

```
shouldbee run
```

### 3. テスト結果を確認しよう

テストが完了するとレポートが `./shouldbee-report/report.md` に作成されます。お使いのMarkdownエディタで開いてみてください。

#### おすすめのMarkdownエディタ

エディタ | .
:-------:|----
[MacDown]<br>(無料) | ![macdown.png]
[Mou]<br>(無料) | ![mou.png]

[Mou]: http://mouapp.com/ 
[MacDown]: http://macdown.uranusjr.com/

[mou.png]: https://github.com/shouldbee/shouldbee/raw/master/images/mou.png
[macdown.png]: https://github.com/shouldbee/shouldbee/raw/master/images/macdown.png


### 4. テスト結果をチームでシェアしよう

ShouldBeeのテストレポートはMarkdown形式なので、チームで簡単にシェアすることができます！

* Redmineや[GitHubのissues]で問題を報告
* [Qiita:Team]で今日のテスト結果をシェア

## 続き

* Shouldbeefileの書き方について知りたい → [Shouldbeefile]
* 利用可能なステップについて知りたい → [Steps]

[Shouldbeefile]: https://github.com/shouldbee/shouldbee/blob/master/shouldbeefile.md
[Steps]: https://github.com/shouldbee/shouldbee/blob/master/steps.md
[Windows7で環境変数を設定する方法]: https://github.com/shouldbee/shouldbee/blob/master/windows-how-to-set-environment-variables.md
[Qiita:Team]: https://teams.qiita.com/
[GitHubのissues]: https://github.com/

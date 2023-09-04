## 概要
ローカル環境を汚さず、Atcoderの問題を解きやすい環境を用意しました。
コマンド一つでテストケースダウンロード、テンプレートの作成、テスト実行ができます。
また、フォーマッター・自動補完なども使えるようになっています。
templateなので、リポジトリをcreateして使ってください。

## 利用環境
- M1 Mac Ventura
- vscode
- Go 1.20.0

## 環境の作成
  vscodeのDevContainerを利用して環境を作成します。
  手順に進む前にvscodeで`Remote Container`の拡張を以下リンクからインストールしておきます。
  [リンク](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)

1. templateから新しくリポジトリを作成します。
"Create a new repository"から作成できます。
1. 作成したリポジトリをcloneします。
2. 作成したリポジトリをvscodeで開きます。
3. vscodeでDevContainerを開きます。
4. ローディングが終了し、フォルダの中身が表示されれば完了です。

## 利用方法例
例題として、AtCoder Beginner Contest 314の問題を解く流れを説明します。
[問題リンク](https://atcoder.jp/contests/abc314)

1. 先ほど作成したDevContainer内のworksディレクトリで、問題のテストケースを取得します。
    ```
    cd works
    acc new abc314
    ```
2. できた問題のディレクトリに移動し、テンプレートからファイルを作成する
    ```
    cd abc324/a
    add-temp
    ```
3. 作成されたmain.goに以下のコードをペーストする
4. テストを実行する
    ```
    oj-test
    ```
5. 回答を提出する
    ```
    acc submit main.go
    ```

## 各種コマンドまとめ
テストケースを取得する
```
acc new コンテストID
```
テンプレートからmain.goを作成する
```
add-temp
```
テストを実行する
```
oj-test
```
回答を提出する
```
acc submit main.go
```
# 4d-tips-convert-case

`Convert case`は，かつて4th Dimensionに存在した文字列変換コマンドです。

#### コマンドの用途

`_O_Convert case:C360`は，西欧スクリプトの`Uppercase` `Lowercase`に相当する関数で，日本語版ではひらがな⇄カタカナ，全角⇄半角，カナ⇄ローマ字といった文字列変換ができました。[漢字Talk 7](https://ja.wikipedia.org/wiki/%E6%BC%A2%E5%AD%97Talk)/[Mac OS 9](https://ja.wikipedia.org/wiki/Classic_Mac_OS)の`TransliterateText`をコマンド化したものなので，Mac版限定のコマンドであり，v11以降のUnicodeモードでは動作しません。

#### 履歴

* v3: コマンドが追加される
* [v6.0](https://github.com/4D-JP/4d-tips-convert-case/files/8684081/Convert.case-6.0.pdf)
* [v6.5](https://github.com/4D-JP/4d-tips-convert-case/files/8684044/Convert.case-6.5.pdf)
* v6.7
* [v6.8](https://github.com/4D-JP/4d-tips-convert-case/files/8684041/Convert.case-6.8.pdf): 「Macintosh版のみ」の注記が追加される
* v2003: ランゲージリファレンスからコマンドに関する記述が削除される
* v2004
* v11: Unicodeモードでコマンドが動作しなくなる
* [v12](https://github.com/4D-JP/4d-tips-convert-case/files/8684135/4d-deprecated-features-12.pdf): 廃止予定機能のリストにコマンドが掲載される

この記事ではコマンドの仕様と代替案について説明します。

#### シンタックス

```4d
converted:=Convert case(string; what ; how) 
```

|パラメーター|タイプ|説明|
|:-:|:-:|:-:|
|string|Text|元の文字列|
|what|Integer|どこを変更するか|
|how|Integer|どのように変換するか|
|converted|Text|変換された文字列|



https://github.com/miyako/4d-plugin-kana

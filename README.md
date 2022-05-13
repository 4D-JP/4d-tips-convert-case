# 4d-tips-convert-case

`Convert case`は，かつて4th Dimensionに存在した文字列変換コマンドです。

#### コマンドの用途

`_O_Convert case:C360`は，西欧スクリプトの`Uppercase` `Lowercase`に相当する関数で，日本語版ではひらがな⇄カタカナ，全角⇄半角，カナ⇄ローマ字といった文字列変換ができました。Mac OSの**Script Manager** APIの`TransliterateText`をコマンド化したものなので，Mac版限定のコマンドであり，v11以降のUnicodeモードでは動作しません。

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

#### オプション

https://github.com/miyako/4d-plugin-kana

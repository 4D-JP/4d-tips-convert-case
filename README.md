# 4d-tips-convert-case

`Convert case`は，かつて4th Dimensionに存在した文字列変換コマンドです。

#### コマンドの用途

`_O_Convert case:C360`は，西欧スクリプトの`Uppercase` `Lowercase`に相当する関数で，日本語版ではひらがな⇄カタカナ，全角⇄半角，カナ⇄ローマ字といった文字列変換ができました。オプション定数は[漢字Talk 7](https://ja.wikipedia.org/wiki/%E6%BC%A2%E5%AD%97Talk)/[Mac OS 9](https://ja.wikipedia.org/wiki/Classic_Mac_OS)の`TransliterateText` APIを踏襲しており，Windows版およびv11以降のUnicodeモードでは動作しません。

#### 履歴

|バージョン|説明|
|:-|:-|
|3|コマンドが追加される|
|[6.0](https://github.com/4D-JP/4d-tips-convert-case/files/8684081/Convert.case-6.0.pdf)||
|[6.5](https://github.com/4D-JP/4d-tips-convert-case/files/8684044/Convert.case-6.5.pdf)||
|6.7||
|[6.8](https://github.com/4D-JP/4d-tips-convert-case/files/8684041/Convert.case-6.8.pdf)|「Macintosh版のみ」の注記が追加される|
|2003|ランゲージリファレンスからコマンドに関する記述が削除される|
|2004||
|11|Unicodeモードでコマンドが動作しなくなる|
|[12](https://github.com/4D-JP/4d-tips-convert-case/files/8684135/4d-deprecated-features-12.pdf)|廃止予定機能のリストにコマンドが掲載される|

この記事ではコマンドの仕様と代替案について説明します。

#### シンタックス

```4d
converted:=Convert case(string;what;how) 
```

|パラメーター|タイプ|説明|
|:-|:-:|:-|
|string|Text|元の文字列|
|what|Integer|なにを変更するか|
|how|Integer|どのように変換するか|
|converted|Text|変換された文字列|

#### なにを変換するか

コマンドは下記の「対象タイプ」オプションをサポートしていました。

|値|説明|
|-:|:-|
|`-1`|すべて|
|`4`|1バイトのアルファベットと記号|
|`8`|2バイトのアルファベットと記号|
|`16`|1バイトのカタカナ|
|`32`|2バイトのカタカナ|
|`128`|2バイトのひらがな|

**注記**: ドキュメントより。「数字」は暗黙的に変換されるものと思われる。

#### どのように変換するか

コマンドは下記の「変換タイプ」オプションをサポートしていました。

|値|説明|
|-:|:-|
|`2`|1バイトのアルファベットと数字と記号|
|`3`|2バイトのアルファベットと数字と記号|
|`4`|1バイトのカタカナ|
|`5`|2バイトのカタカナ|
|`7`|2バイトのひらがな|

https://github.com/miyako/4d-plugin-kana

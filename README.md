# scssの関数やmixinをvscodeでコンパイルするリポジトリ
主に社内用、もしくはサクッとコンパイルして値を確認できるようにと思って作りました。  
scssの機能を利用してエディター（vscode）で関数やmixinで値を計算します。  

## ディレクトリ
```
├── .vscode
│   └── settings.json
├── css
├── sass
│   ├── _function.scss
│   └── ◯◯.scss
├── .editorconfig
└── README.md
```
- `.vscode` vscodeの設定ファイルなどが収められたディレクトリ
  - `settings.json` vscodeの設定ファイル
- `css` cssファイルが収められたディレクトリ
- `sass` scssが収められたディレクトリ
  - `◯◯.scss` 追加するscssファイル
- `.editorconfig` EditorConfigの設定ファイル
- `README.md` 説明などを記載

-- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --

## 必要なプラグイン
 - [Live Sass Compiler](https://marketplace.visualstudio.com/items?itemName=glenn2223.live-sass)

## できればインストールしたほうがいいプラグイン
 - [EditorConfig for VS Code](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)

-- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --

## 使用方法
sassディレクトリ配下の◯◯.scssを参考にscssファイルを追加して使用してください。  
※その場合ファイルの先頭に`@use 'function' as *;`の記述をお願いします。  
（`_function.scss`の変数や関数を使用するため）

-- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --

## 説明01
sassディレクトリ配下に作成した◯◯.scssと同じ名前もcssファイルがcssディレクトリ配下にコンパイルされた状態で作成されます。

## 説明02
コンパイルする場所やベンダープレフィックスを変更したいなどありましたら、`.vscode`ディレクトリ配下の`settings.json`を編集してください。

-- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --

## 参考サイト
以下のサイトを参考に作成させていただきました。  
- [line-heightで出来るスペースをSCSSのmixinを使って効率よく消す方法](https://moshashugyo.com/media/line-height-space)
- [Sass と clamp() で作る可変のフォントサイズ](https://firstlayout.net/fluidly-font-size-created-with-sass-and-clamp/)
- [Min-Max-Value Interpolation](https://min-max-calculator.9elements.com/)

- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --

## 最後に
scssファイルをコンパイルできるようであれば、どのようなツールでも構いません。  
目的は、社内用でサクッとなので必須プラグインで`Live Sass Compiler`を指定させていただきました。  
できればインストールしたほうがいいプラグイン`EditorConfig for VS Code`も必須ではありませんが、インデントや改行コードを統一できるので記載しました。

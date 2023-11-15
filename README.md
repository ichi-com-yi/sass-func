# scssの関数やmixinをvscodeでコンパイルするリポジトリ
主に社内用、もしくはサクッとコンパイルして値を確認できるようにと思って作りました。  
WEBジェネレーターなどでclampなどを計算しないでscssを使用して関数やmixinで値を計算します。  
ling-heightの計算はよく忘れますよね…

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
- `css` 画像、css、sassファイルが収められたディレクトリ
- `sass` sassが収められたディレクトリ
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

## 最後に
scssファイルをコンパイルできるようであれば、どのようなツールでも構いません。  
目的は、社内用でサクッとなので必須プラグインで`Live Sass Compiler`をしていさせていただきました。
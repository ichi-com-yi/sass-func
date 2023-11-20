# sassの関数やmixinをvscodeでコンパイルするリポジトリ
主に社内用にサクッとコンパイルして値を確認できるようにと思って作りました。  
sassの機能を利用してエディター（vscode）で関数やmixinで値を計算します。  

## ディレクトリ
```
├── .vscode
│   └── settings.json
├── css
│   ├── clamp.css
│   └── lh.css
├── sass
│   ├── _function.scss
│   ├── clamp.scss
│   └── lh.scss
├── .editorconfig
└── README.md
```
- `.vscode`          vscodeの設定ファイルなどが収められたディレクトリ
  - `settings.json`  vscodeの設定ファイル
- `css`              cssファイルが収められたディレクトリ
  - `clamp.css`      関数 fs を記述したscssファイルをコンパイルしたcssファイル
  - ` lh.css`        mixin lh を記述したscssファイルをコンパイルしたcssファイル
- `sass`             scssファイルが収められたディレクトリ
  - `_function.scss` 関数・mixinの設定ファイル
  - `clamp.scss`     関数 fs を記述したファイル
  - `lh.scss`        mixin lh を記述したファイル
- `.editorconfig`    EditorConfigの設定ファイル
- `README.md`        説明などを記載

-- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --

## 必要なプラグイン
 - [Live Sass Compiler](https://marketplace.visualstudio.com/items?itemName=glenn2223.live-sass)

## できればインストールしたほうがいいプラグイン
 - [EditorConfig for VS Code](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)

-- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --

## 使用方法
- ダウンロードしたsassディレクトリ配下の`clamp.scss`と`lh.scss`を参考にしてください。
- 関数やmixinは`_function.scss`を参考にしてください。

-- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --

## 説明
- 関数 fs はclampを計算し mixin lh はラインハイトの上下の余白を相殺します。
- sassディレクトリ配下に作成した◯◯.scssと同じ名前もcssファイルがcssディレクトリ配下にコンパイルされた状態で作成されます。
（sassディレクトリ配下のscssファイルの箇所がややこしくて、申し訳ないです）
- コンパイルする場所やベンダープレフィックスを変更したいなどありましたら、`.vscode`ディレクトリ配下の`settings.json`を編集してください。

-- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --

## 参考サイト
以下のサイトを参考に作成させていただきました。  
- [line-heightで出来るスペースをSCSSのmixinを使って効率よく消す方法](https://moshashugyo.com/media/line-height-space)
- [Sass と clamp() で作る可変のフォントサイズ](https://firstlayout.net/fluidly-font-size-created-with-sass-and-clamp/)
- [Min-Max-Value Interpolation](https://min-max-calculator.9elements.com/)
- [Easy Clamp Generator](https://free.page-craft.jp/clamp/)

- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --

## 最後に
sassをコンパイルできるようであれば、どのようなツールでも構いません。  
目的は、社内用でサクッとなので必須プラグインで`Live Sass Compiler`を指定させていただきました。  
できればインストールしたほうがいいプラグイン`EditorConfig for VS Code`も必須ではありませんが、インデントや改行コードを統一できるので記載しました。

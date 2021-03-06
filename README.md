# デザインフロント用WordPressテーマ及びプラグイン開発

デザインフロントのサイトを構築するWordPressのテーマ及びプラグイン開発用リポジトリです。

## ディレクトリ構成


```
root
├─ public            # WordPress main body storage directory
|  ├─ wp-content
|  |  ├─ plugins
|  |  └─ themes
|  |     └─ dftheme   # dftheme theme directory
│  ├─ ... 
|  └─ ...
├─ .git
├─ .gitignore
└─ README.md 
```

## 必要な環境

- WordPress 5.0.3 以上
- [Local](https://local.getflywheel.com/) by Flywheel もしくはその他開発環境（PHP, MySQL）
- [composer](https://getcomposer.org/) 1.8.0 以上
- Node v10.15.0 以上

## 使い方
### 1."[Local by Flywheel](https://local.getflywheel.com/)"によるWordPressのインストール

### 2.リポジトリクローン
``` git clone git@github.com:design-front/dftheme.git ```

### 3.クローンしたファイルの移動

``` dftheme ``` ディレクトリに入っている

- .git
- .gitignore
- README.md

を ```public``` と同一階層に移動（ディレクトリ構成と同じにする）し、``` dftheme ``` ディレクトリを削除

### 4.composerの実行

``` composer install ```

### 5.npm の実行

テーマ用ディレクトリに移動
``` cd public/wp-content/themes/dftheme/ ```

``` npm install ```

### 6.gulpを起動して開発を開始

``` npx gulp ```

### 注意

Local by Flywheel を利用する際にドメイン名が `***.local` というようにlocalとなっているとブラウザーシンクで読み込みが遅くなる場合があります。
その場合は、 Local by Flywheel のドメイン名を変更し、 それに合わせてgulpfile.js の `proxy` を変更してください。
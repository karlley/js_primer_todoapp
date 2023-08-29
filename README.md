# js primer todoapp

状態管理を使った簡易アプリ

```sh
# ローカルサーバーの起動
npx --yes @js-primer/local-server
```

- エントリーポイント
  - アプリの中で一番最初に呼び出される部分
  - 例) index.html、index.js
  - html、jsなど1つのアプリで複数のエントリーポイントがある場合もある

- モジュールスコープ
  - モジュールのトップレベルに自動作成されるスコープ
  - グローバルスコープの下に作られる
  - 複数モジュールを別の`<script>` タグで読み込むとスコープが異なるのでモジュール間の連携ができない
  - 例) index.htmlでindex.jsを読み込む、index.jsで他のモジュールを`import` を使って読み込む

- `file:` から始まるページからはJavaScriptモジュールは動作しない
  - ローカルサーバーを使用して`http:` から始まるURLでアクセスする必要がある

- モジュール対応のブラウザの確認方法
  - https://caniuse.com/ で確認

- 関数の中に`import` を宣言するとエラーになる
  - `import` はトップレベルで宣言する必要がある

- JavaScriptの2つの実行コンテキスト
  - Script
  - Module

- `import` では読み込みファイル名の拡張子は省略しない
  - `import { App } from "./src/App.js`

- ブラウザにはOSが提供するUIフレームワークは無い
  - ライブラリ等のUIフレームワークは多数存在している

- HTMLのclass属性
  - 基本的にCSSの装飾目的で使用する
  - JavaScriptのclassとは無関係

- HTMLのid属性
  - CSS、JavaScriptのどちらでも使用する
  - 1ページに複数存在できない

- `document.querySelector`
  - ブラウザのDOM API
  - CSSセレクタで要素の取得

- HTMLの`form` 要素で`Enter` を押すと`submit` イベントが発生する
  - `addEventListener` でイベント取得できる

- イベントリスナー
  - イベント発生時に呼ばれるコールバック関数
  - 別名: イベントハンドラ

- `preventDefault()`
  - デフォルトの動作をキャンセルするメソッド
  - 例) `event.preventDefault();` でイベントで発生するデフォルト動作をキャンセルする

- フォームのデフォルトの動作
  - フォームの入力内容をURLへ送信する
  - `preventDefault()` を使うことで送信動作をキャンセル可能

- JavaScriptで既存のHTML要素に対してHTML要素を追加する
  - 文字列ではNG
  - HTML要素が必要

- `template` 要素
  - HTMLの断片からHTML要素を作成できる

- `appendChild` メソッド
  - 既存のHTML要素の子要素としてHTML要素を追加できる
  - 既に別要素が存在する場合は末尾に追加

- `render` 関数
  - 親要素を子要素で上書きする

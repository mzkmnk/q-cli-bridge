# VS Code 拡張機能へようこそ

## フォルダの内容

* このフォルダには、拡張機能に必要なすべてのファイルが含まれています。
* `package.json` - これは拡張機能とコマンドを宣言するマニフェストファイルです。
  * サンプルプラグインはコマンドを登録し、そのタイトルとコマンド名を定義します。この情報により、VS Code はコマンドパレットにコマンドを表示できます。この時点ではプラグインをロードする必要はありません。
* `src/extension.ts` - これはコマンドの実装を提供するメインファイルです。
  * このファイルは `activate` 関数を1つエクスポートします。この関数は拡張機能が最初にアクティブ化されたときに呼び出されます（この場合はコマンドの実行時）。`activate` 関数内で `registerCommand` を呼び出します。
  * コマンドの実装を含む関数を `registerCommand` の第2パラメータとして渡します。

## セットアップ

* 推奨される拡張機能（amodio.tsl-problem-matcher、ms-vscode.extension-test-runner、dbaeumer.vscode-eslint）をインストールしてください


## すぐに始める

* `F5` を押すと、拡張機能がロードされた新しいウィンドウが開きます。
* コマンドパレット（`Ctrl+Shift+P` または Mac では `Cmd+Shift+P`）を開き、`Hello World` と入力してコマンドを実行します。
* `src/extension.ts` 内のコードにブレークポイントを設定して、拡張機能をデバッグします。
* デバッグコンソールで拡張機能の出力を確認できます。

## 変更を加える

* `src/extension.ts` のコードを変更した後、デバッグツールバーから拡張機能を再起動できます。
* VS Code ウィンドウをリロード（`Ctrl+R` または Mac では `Cmd+R`）して、変更を読み込むこともできます。


## API を探索する

* `node_modules/@types/vscode/index.d.ts` ファイルを開くと、完全な API セットを確認できます。

## テストを実行する

* [Extension Test Runner](https://marketplace.visualstudio.com/items?itemName=ms-vscode.extension-test-runner) をインストールします
* **Tasks: Run Task** コマンドで "watch" タスクを実行します。これが実行されていることを確認してください。実行されていないと、テストが検出されない可能性があります。
* アクティビティバーから Testing ビューを開き、Run Test ボタンをクリックするか、ホットキー `Ctrl/Cmd + ; A` を使用します
* Test Results ビューでテスト結果の出力を確認します。
* `src/test/extension.test.ts` に変更を加えるか、`test` フォルダ内に新しいテストファイルを作成します。
  * 提供されているテストランナーは、名前パターン `**.test.ts` に一致するファイルのみを対象とします。
  * `test` フォルダ内にフォルダを作成して、テストを任意の方法で構造化できます。

## さらに進む

* [拡張機能のバンドル](https://code.visualstudio.com/api/working-with-extensions/bundling-extension)により、拡張機能のサイズを削減し、起動時間を改善します。
* VS Code 拡張機能マーケットプレイスに[拡張機能を公開](https://code.visualstudio.com/api/working-with-extensions/publishing-extension)します。
* [継続的インテグレーション](https://code.visualstudio.com/api/working-with-extensions/continuous-integration)を設定してビルドを自動化します。

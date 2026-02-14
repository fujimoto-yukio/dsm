# DSM Workbench
**DSM Workbench** は、DSM(Design Structure Matrix), DMM(Domain Mapping Matrix), MDM(Multiple Domain Matrix) の編集と分析を行うためのツールです。<br>
[はじめに](https://github.com/fujimoto-yukio/dsm/wiki/はじめに) に書いた通り、個人的な趣味で作ったアプリケーションですが、「As Is」で使っていただければ幸いです。

## 主要機能
**DSM Workbench** は以下の機能を有しています。
- DSM(Design Structure Matrix)の定義
- DMM(Domain Mapping Matrix)の定義
- MDM(Multiple Domain Matrix)の定義、DSMへの変換
- MDMによるQFDの定義、QFDのプロセスDSM変換
- DSMの分析（連成要素検索、順序付け、間接依存関係の検索、コミュニティ分析等）
- DSM、DMM、MDMのグラフ描画
 
詳細は、[Wiki](https://github.com/fujimoto-yukio/dsm/wiki)、リリース物件に含まれる [ヘルプドキュメント](https://github.com/fujimoto-yukio/dsm/blob/main/release/DSMWorkbench_Help.pdf) を参照してください。

#### 画面イメージ
<details>
  <summary>DSM Workbench, DSM Editor</summary>
  <img width="1174" height="1079" alt="image" src="https://github.com/user-attachments/assets/69c55255-57d5-41ff-90ff-4226d763c7bd" />
</details>
<details>
  <summary>Graph Viewer - DSM直交グラフ</summary>
  <img width="1268" height="907" alt="image" src="https://github.com/user-attachments/assets/ebb114bd-616a-4b0f-afd1-f31b7dc84fae" />
</details>
<details>
  <summary>MDM Editor - QFD定義</summary>
  <img width="1212" height="812" alt="image" src="https://github.com/user-attachments/assets/ea624864-5fd0-441f-8f9f-ca5213f8ccc8" />
</details>
<details>
  <summary>Graph Viewer - ドメイン連携階層グラフ</summary>
<img width="1611" height="969" alt="image" src="https://github.com/user-attachments/assets/9c49cde9-48c3-4637-9d8c-b734637eebc0" />
</details>
<details>
  <summary>DSM Editor, DMM Editor</summary>
  <img width="1652" height="1016" alt="image" src="https://github.com/user-attachments/assets/214ea21a-9c78-4fea-8f9a-b83c29bfe541" />
</details>
<details>
  <summary>DSM Viewer -  V字開発プロセスDSM</summary>
  <img width="1381" height="1095" alt="image" src="https://github.com/user-attachments/assets/998322e5-166e-4498-845f-fe1860c2494d" />
</details>


## リリース
### 1. 実行環境
  - Windows、macOSそれぞれのリリースモジュール`dsmworkbench-x.y.z-win.zip` `dsmworkbench-x.y.z-mac.zip`ををダウンロード、展開してください。
  - 実行のためにはJava17の実行環境が必要です。OracleJDKで開発しましたが、OpenJDKでも動作するはずです。
  - macOS版はApple Siliconで開発されています。JavaFXのライブラリが異なるため、Intel Macでは動作しません。

### 2. リリースモジュール
リリースの内容とモジュールは、[Release](https://github.com/fujimoto-yukio/dsm/releases) にあります。

### 3. 実行方法
  - Windows版、macOS版共に、DSM Workbenchの実行形式Jarファイルと必要ライブラリをzip圧縮しています。
  - Windows、macOSそれぞれのリリースモジュールをダウンロード後、任意のフォルダに展開してください。
  - Windows: 展開してできた`dsmworkbench`フォルダ内の`dsmworkbench.bat`を起動してください。
  - macOS: 展開してできた`dsmworkbench`フォルダ内の`dsmworkbench.sh`を起動してください。
  - 実行ユーザのホームディレクトリ直下に`.dsmworkbench`という名前のディレクトリが作成され、ログファイルが書き込まれます。
  - 配布方法、起動方法ともに、手数のかからない手抜きコースになっています（Windows用にはexe化を試みましたが、失敗して保留中です）。

----------
DSM Workbenchを開発、公開するに至った経緯は、Wiki [はじめに](https://github.com/fujimoto-yukio/dsm/wiki/はじめに)に移動しました。

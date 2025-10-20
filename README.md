# DSM Workbench
**DSM Workbench** は、DSM(Design Structure Matrix), DMM(Domain Mapping Matrix), MDM(Multiple Domain Matrix) の編集と分析を行うためのツールです。
## 主要機能
**DSM Workbench** は以下の機能を提供します。
- DSM(Design Structure Matrix)の定義
- DMM(Domain Mapping Matrix)の定義
- MDM(Multiple Domain Matrix)の定義
- DSMの順序付け（シーケンシング）、コミュニティ分析（MDMはDSMに変換して分析します）
- DSM、DMM、MDMのグラフ描画

<img width="2484" height="1315" alt="image" src="https://github.com/user-attachments/assets/2a85f22f-7980-40be-aaee-a8429b68c0d0" />

詳細は、[Wiki](https://github.com/fujimoto-yukio/dsm/wiki)、リリース物件に含まれるヘルプドキュメントを参照してください。

----------
## リリース
### 1. 実行環境
  - Windows、macOSそれぞれのリリースモジュール`dsmworkbench-1.0.0-win.zip` `dsmworkbench-1.0.0-mac.zip`ををダウンロード、展開してください。
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

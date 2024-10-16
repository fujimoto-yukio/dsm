# DSM Workbench
## はじめに
DSM Workbenchという名前を付けて、DSM(Design Structure Matrix)の編集・分析ツールを公開することにしました。<br>
まず最初に、このツールの生い立ち、開発、公開に至った経緯を書きます。

### 1. 生い立ち
自動車メーカーの情報システム部門に出向していた2020年、その年のゴールデンウィークはコロナの緊急事態宣言で、自宅引きこもりになりました。
あまりに暇でやることがない連休、思いついたのが、当時仕事で検討していたDSMが操作できるアプリを作ることでした。

JDK1.5以来のプログラム製造で、随分と進化したJavaと初めてのGUIアプリJavaFXに苦戦しながら、（やっつけで[^1]）DSMアプリのプロトタイプを作りました。<br>
出来上がったアプリは、CSVからDSMを読み込み、要素を上下（左右）に移動、並び替えるだけの簡単なものでしたが、DSMの動きが直接見えて画期的なものに思えました。

[^1]: ネットで漁ったサンプルコードをたくさんコピペして使いました。初めて見たJavaのラムダ式は呪文にしか見えませんでした。（笑

その後、出向から帰任する2022年9月末までの間、仕事の暇を見つけては、画面の見た目や操作性を改善し、可到達マトリクスやコミュニティ分析他、実験的なものも含めて機能を追加しました。<br>
設計現場でも使ってもらいましたが、ベースがプロトタイプということもあり、業務に本格適用するものにはなりませんでした。

### 2. 再開発
帰任から1年後の2023年9月末、63歳半で退職するとき、ゴールデンウィークよりもはるかに長い退職後の時間を何に使うか考えて、やりっぱなしになっているDSMアプリを作り直すことに決めました。
新しいJavaの文法とJavaFXによるGUIアプリ開発の基礎も（割とまじめに）学んで、DSM Workbenchの開発を始め、1年後の2024年10月にバージョン1.0が完成しました。

業務ニーズではない趣味の開発から出発しているため、機能の設計思想には個人的な興味が優先されています。
特に、グラフ描画やグラフデータベースの活用に関しては、グラフ理論はさておき、作って、動かすことの楽しいものが作り込まれており、実業務に役立つかどうかは不明です。
本来であれば、まじめなDSM技術論もきちんと抑えておくべきですが、それも怪しいです。

### 3. 公開
一通りの機能が出揃い、それなりの見栄えになったと思いますが、使えるアプリになったかどうかは、実際に使っていただいて初めて分かることになります。<br>
また、ひとりで設計、開発、テストを行っており、どうしてもテストが甘く、バグ、不具合もまだまだ残っているはずです。

あくまで「As Is」ですが、これらをご理解の上で使っていただければ幸いです。<br>
バグ、不具合に限らず、改善要望もお知らせいただければ、可能な限り対応したいと考えています。

2024年10月　藤本　幸生（fjmt.yko@gmail.com）

## リリース
### 1. 実行環境
  - Java17の実行環境が必要です。OracleJDKで開発しましたが、OpenJDKでも動作するはずです。
  - macOS版はApple Siliconで開発されています。JavaFXのライブラリが異なるため、Intel Macはでは動作しません。
### 2. リリース物件
  - Windowsプレビューリリース: [dsmworkbench-win-1.0-20241016.zip](https://github.com/fujimoto-yukio/dsm/blob/main/release/dsmworkbench-win-1.0-20241016.zip)
  - macOS プレビューリリース: [dsmworkbench-mac-1.0-20241016.zip](https://github.com/fujimoto-yukio/dsm/blob/main/release/dsmworkbench-mac-1.0-20241016.zip)
  - DSM Workbench操作説明書: [DSMWorkbench_Help.pdf](https://github.com/fujimoto-yukio/dsm/blob/main/release/DSMWorkbench_Help.pdf)
  - Getting Started with DSM Workbench: [DSMWorkbench_GettingStarted.pdf](https://github.com/fujimoto-yukio/dsm/blob/main/release/DSMWorkbench_GettingStarted.pdf)
### 3. リリース物件
  - Windows版、mac版共に、DSM Workbenchの実行形式Jarファイルと必要ライブラリをzip圧縮しています。
  - 物件をダウンロード後、任意のフォルダで解凍してください。
  - Windows: dsmworkbenchフォルダ内の`dsm.bat`を起動してください。
  - macOS: dsmworkbenchフォルダ内の`dsm.sh`を起動してください。
  - 配布方法、起動方法ともに、手数のかからない手抜きコースになっています。
    
----------
# 機能概要
DSM Workbenchは以下の5つの画面機能で構成されており、二値型（Binary）と数値型（Numeric）の2種類のDSMを扱うことができます。
### 1. DSM Workbench
  - アプリケーションを起動すると、最初に表示される画面です。
  - DSMの種類を指定して、新規のDSMを編集するための`DSM Editor`を起動することができます。
  - ファイルを指定して`DSM Editor`を起動することができます。
  - ファイルを指定して`Graph Visualizer`を起動することができます。
    
    <img width="356" alt="スクリーンショット 2024-10-09 20 25 13" src="https://github.com/user-attachments/assets/98b0f952-4345-4b41-b90d-32d55dc5440b">
### 2. DSM Editor
  - DSMの編集と分析を行うための画面です。
  - `二値型（Binary）`と`数値型（Numeric）`の2つのDSM形式を取り扱います。
  - 操作モードとして、`セル編集モード`と`マトリックス編集・解析モード`の2つのモードがあります。
  - `セル編集モード`では、DSM要素の定義、属性編集とDSM要素間のフィード値を編集することができます。
  - `マトリックス編集・解析モード`では、DSM行列に対する移動、並び替え、部分抽出等の操作と、DSMの順序付けやコミュニティ分析等の解析を行います。
    
    <img width="550" alt="スクリーンショット 2024-10-09 20 24 27" src="https://github.com/user-attachments/assets/ce3c534f-70be-48a4-ba24-576a4ed5b702">
    <img width="550" alt="スクリーンショット 2024-10-10 10 13 35" src="https://github.com/user-attachments/assets/38b8e519-0b73-4a6c-bec0-8872476b8f96">  
### 3. Graph Visualizer
  - `DSM Editor`で作成したDSMをネットワーク・グラフに描画します。
  - `JUNC Visualizer`と`SmartGraph Visualizer`の2種類のグラフ描画形式を選択することができます。
    
    <img width="460" alt="スクリーンショット 2024-10-09 20 27 21" src="https://github.com/user-attachments/assets/c5a50f20-0f67-4db4-a477-36470e7e1035">
### 4. Preference Dialog
  - `DSM Workbench`の各種設定値を管理します。
  - 設定値はユーザ毎に保存されます。
    
    <img width="550" alt="スクリーンショット 2024-10-09 20 27 36" src="https://github.com/user-attachments/assets/0140a362-64e3-4654-907c-ec7cfe9ddcb1">
### 5. Information DIalog
  - `DSM Workbench`で取り扱う各種情報を詳細表示します。
    
    <img width="550" alt="スクリーンショット 2024-10-09 20 28 06" src="https://github.com/user-attachments/assets/e16766f4-b3f1-4ac6-a902-dac0af781897">

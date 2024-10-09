# DSM Workbench
DSM WorkbenchはDSM (Design Structure Matrix) の編集と分析を行うためのツールで、二値型（Binary）と数値型（Numeric）の2種類のDSMを扱います。
## 主要機能
### DSM Workbench
  - アプリケーションを起動すると、最初に表示される画面です。
  - DSMの種類を指定して、新規のDSMを編集するための`DSM Editor`を起動することができます。
  - ファイルを指定して`DSM Editor`を起動することができます。
  - ファイルを指定して`Graph Visualizer`を起動することができます。
### DSM Editor
  - DSMの編集と分析を行うための画面です。
  - `二値型（Binary）`と`数値型（Numeric）`の2つのDSM形式を取り扱います。
  - 操作モードには、`セル編集モード`と`マトリックス編集・解析モード`の2つのモードがあります。
  - `セル編集モード`では、DSM要素の定義、属性編集とDSM要素間のフィード値を編集することができます。
  - `マトリックス編集・解析モード`では、DSM行列に対する移動、並び替え、部分抽出等の操作と、DSMの順序付けやコミュニティ分析等の解析を行います。
### Graph Visualizer
  - `DSM Editor`で作成したDSMをネットワーク・グラフに描画します。
  - `JUNC Visualizer`と`SmartGraph Visualizer`の2種類のグラフ描画形式を選択することができます。
### Preference Dialog
  - `DSM Workbench`の各種設定値を管理します。
  - 設定値はユーザ毎に保存されます。
### Information DIalog
  - `DSM Workbench`で取り扱う各種情報を詳細表示します。
  - 画面の表示内容をファイルに保存することもできます。

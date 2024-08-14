# tex
  - 数式の前後は半角スペース一時開けないとgithub上では数式として表示されない(スマホ上ではこれでも反映されない)。
  - noteでは数式にしたい箇所を\$${...}\$$(全て半角)で囲む。
  - 大きい和集合で上下に添え字をつけるときは
    ```
    \displaystyle\bigcup
    ```
    を使う。
  - ドイツ文字は、
    ```
    \mathfrak{}
    ```
    を使う。
  - ノルムは、 
    ```
    \|x\|
    ``` 
    をつかう
  - 「\ni」で要素記号を反転させた記号を表示することができる。
  - 閉区間は
    ```
    [a,b]
    ```

# keybord shortcut
  - F4: 電卓に設定
  - F12: スリープに設定
  - 設定>アクセシビリティ>キーボード>固定キー機能>固定キー機能用のキーボードショートカットを無効にすることで、shiftを連打したとき(５回)にでてくるポップアップが出てこなくなる。

# world
  - 光の混ざり具合考慮するため、mainカラーを全体の光に調節するといい見た目になる。
  - F2はrename
  - ワールドのバックアップには、Turbo Backup Proを買う！(次回新作作成時)
  - MasterCubeというアセットで、cubeを引き延ばしてもテクスチャを均等に配置してくれる。
    - インポートして、使いたいオブジェクトに、MasterCubeコンポーネントを追加すればよい
    - Reflesh base UVを押し、スケールを一度動かせば、反映される。
    - 参考: https://tsubakit1.hateblo.jp/entry/2016/05/24/073000 </br>
      https://assetstore.unity.com/packages/tools/modeling/mastercube-40033#content
  - いい感じのライティングの参考
    - https://tsubakit1.hateblo.jp/entry/2018/01/04/235520
  - Web上からtextと画像を取得することができる。
  - Package ManagerにあるUnity標準アセットについて
    - [Windows]→[Package Manager]から、Unity公式のアセットを導入することが出来ます。注意点としては、他のレンダリングパイプラインでしか使えないアセットが混在しているので、そこは注意が必要です。ワールド制作初心者が知ってると使えそうなのを主観的ではありますがいくつか簡単に紹介しておきます。
    - ①FBX Exporter
      - Unity上のゲームオブジェクトをFBXとして出力するアセットです。そのままではVRChatに持っていけないアセットなどを、これに通すと持って行けたりします。
    - ②Pro Builder
      - Unity上でモデリングすることが出来ます。
    - ③Terrain Tools
      - Terrainに色々機能やブラシなどを追加してくれます。
    - ④Polybrush
      - メッシュに対してスカルプト（彫り込むことが)できたり、Prefabをブラシで配置できたりするみたいです。使ったことがないので詳しくは知りません。
    - ⑤ProGrids
      - グリッドに沿って配置できたりするみたいです。使ったことがないので詳しくは知りません。
    - git 設定参考
      https://qiita.com/uni928/items/8a560522e4ce1f2bdcde</br>
      https://cg-method.com/unity-gitignore-setting/</br>
      https://nekojara.city/unity-gitignore
       - ターミナルで .gitignore.txtを.gitignoreにすると作動する
    - 曲候補
      - Lo-fi chill beat - frosty shadow of winter
      - Bathroom - Chill Background Music
      - ほしくず
  - directional lightをbake設定にしてreflection proveをbakeすると、水面シェーダー(clear water2)が消える。directional lightをrealtime設定にすれば解決。


# blender
  - ver 3.6 においては、RGB分離は、カラー分離に統合されて、内部の選択欄でRGBかHSV等が選択できる。

# thought
  - 月を看（み）るは、清気（せいき）を観（み）るなり。円欠晴翳（えんけつせいえい）の間に在らず。
  花を看るは、生意を観るなり。紅柴香臭（こうしこうしゅう）の外（ほか）に存（そん）す。
    - 佐藤一斎　「言志四録」
  - ステファン・バナッハ
    - ポーランドの数学者。ウクライナ・リヴィウ大学より「抽象集合の演算とその積分方程式への応用について」で博士号を授与される。博士論文では、こんにちバナッハ空間とよばれている概念が導入されており、この論文は現代的な関数解析の幕開けを告げるものとして高く評価されている。
    参考: https://ja.wikipedia.org/wiki/%E3%82%B9%E3%83%86%E3%83%95%E3%82%A1%E3%83%B3%E3%83%BB%E3%83%90%E3%83%8A%E3%83%95

# IT word
  - プリセット
    - 設定値などを前もって調整すること。また、前もって調整・定義された設定値や、その組み合わせに識別名や番号をつけて保存したもの。
  - プロトコル
    - コンピュータとコンピュータがネットワークを通じて通信する際に決められた約束事、決まり事のこと。

# bug fix
  - open3dインストール時のOSError </br>
    ```
    OSError: libX11.so.6: cannot open shared object file: No such file or directory
    ```
    のエラーに対し、次のコマンド順に実行(一番上のコマンドは必要か不明)
    ```
    apt install libc++-dev 
    apt update && apt install -y libsm6 libxext6
    apt-get install -y libxrender-dev
    ```
    すると、次のエラーに変わる。
    ```
    OSError: libGL.so.1: cannot open shared object file: No such file or directory
    ```
    次のコマンドを入力することにより解決。
    ```
    apt-get update && apt-get install libgl1
    ```

  - wsl起動時謎エラー
    ```
    起動されたオブジェクトはクライアントから切断されました。
    Error code: Wsl/Service/CreateInstance/RPC_E_DISCONNECTED
    ```
    再起動すれば治るけど、謎のバグ。処理速度が速すぎると出るらしい(Excel)。</br>
    参考: https://zawanii.com/uipath-excel-exception/

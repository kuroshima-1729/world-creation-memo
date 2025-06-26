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
  - personal access tokenを更新するにはdeveloper settingを開く。

# markdown
  - 数字の箇条書きは
    ```
    1.
    2.
    3.
    ```
    で行う。

# keybord shortcut
  - F4: 電卓に設定
  - F12: スリープに設定
  - 設定>アクセシビリティ>キーボード>固定キー機能>固定キー機能用のキーボードショートカットを無効にすることで、shiftを連打したとき(５回)にでてくるポップアップが出てこなくなる。
  - エクセルのセルの上で、 Alt + H + V + M でテキストをそのまま(フォントや大きさを引き継がないで)張り付ける。

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
  - VRC Pickup の Auto Fold component を Yes にすると、クリックを話してもつかんだままの状態にできる。
  - Quaternion.Slerp(現在角度, ターゲット角度, 速度)
     - 現在角度から ターゲット角度までを滑らかに保管して、速度の速さで回転させる。
  - Bakery参考: https://note.com/snc885/n/n06c553ba73cc
  - standard shaderの改変方法: https://note.com/hikohiro/n/n81b9a4751a55
  - right probe group参考: https://umistudioblog.com/lightprobehowto/
  - 物体を中心から広げる参考
    ```C#
    using UnityEngine;

    public class ObjectSpawner : MonoBehaviour
    {
        public GameObject objectPrefab;
        public int numberOfObjects = 50;
        public float radius = 5f;

        void Start()
        {
            for (int i = 0; i < numberOfObjects; i++)
            {
                float angle = i * Mathf.PI * 2 / numberOfObjects;
                Vector3 position = new Vector3(Mathf.Cos(angle), 0, Mathf.Sin(angle)) * radius;
                Instantiate(objectPrefab, position, Quaternion.identity);
            }
        }
    }
    ```
  - unityで「Ctrl+Shift+N」でフォルダを作成可能。
  - 光芒は半透明のオブジェクトを重ねて作る?
  - Normal map 作れるサイト: https://cpetry.github.io/NormalMap-Online/
  - Blender から持ってきたモデルを、Bakery で変な黒い線が出てうまく焼けないときは、generate uv maps を行っていない可能性がある。
  - unityの画面でクリックが効かなくなる時は、一度ゲームシミュレーションしてから戻ると直る。
  - モデルが複雑な場合、Bakeryでベイクできない場合がある。-> どれが失敗の原因かON/OFFで確かめる。
    ```
    Unity failed unwrapping some models. See console for details. 
    Last failed model: Assets/CModel/Library_ver_1.9.fbx
    Model will now be reverted to original state.
    ```
  - VRCStation コンポーネントはデフォルトでオフにすると、アクティブ化したときにうまく初期化されないから作動しない。デフォルトオンにして、すぐオフにすればうまくいく。
  - Unityのヒエラルキー上で cut & paste すれば遠いところでも楽に移動できる。
  - マテリアルはシェーダに与えるパラメーターを格納する役割をもつ。
  - ライトマップがおかしくなった場合は、ベイクデータをクリアして焼きなおすと直る場合がある。
  - right probe は Render すれば自動的にやってくれるので、改めて Render right probe のボタンは押さなくてよい。一方で、Reflectionはボタンを押す必要があるため、注意が必要。
  - right prove の影響を受けるのは static にしているか否かの違い。
  - soft shadow で柔らかい影を作る？
  - エミッションからの光をベイクする場合
    - エミッションを設定しているオブジェクトの、「Contribute Global Illumination」を有効化する。

# Physbone
  - allow collision を off にすると、手が当たったときに動かなくなる。

# world idea
  - 廃墟 + 地下 + 地下鉄
  - 廃墟 + 駅 橋の上、山の間 -> よくあるシチュエーションだからもうワンポイント
  - 蒸気機関車 + 廃墟
    - 煙と共に眠る
  - 港町 
  - 電車 + 廃墟 + 崖の上、隙間から広い海の景色が見える
  - 海の上の神殿。
  - 墓

# blender
  - ver 3.6 においては、RGB分離は、カラー分離に統合されて、内部の選択欄でRGBかHSV等が選択できる。
  - Ctrl + E で細分化
  - テクスチャをゆがませずに変形する方法
    - デフォルトのオブジェクトにテクスチャを張り付ける(マテリアルの画像テクスチャ)
    - 編集モードにする
    - 右上のオプションを開いて、「面の属性を修正」にチェックを入れる。
    - 編集モードのまま変形などをする。
    - 「u」キー -> スマートUV投影で、いい感じにテクスチャを張りなおしてくれる。
  - blenderからunityへ読み込んだモデルにコライダーをつける場合、SAColliderBuilderを使うといいらしい。
  - shift + N で面の向きを外側にそろえる。
  - 右クリック + 面をブリッジで、例えば円柱の真ん中をインセットした部分に適用すると、真ん中に穴が開く。
  - 傘作成参考: https://www.youtube.com/watch?v=E7HnlCa-pNk
  - マウスのカーソルに丸が出てきたときは「w」キーを押すと直る
    - 参考: https://detail.chiebukuro.yahoo.co.jp/qa/question_detail/q12231855787
  - やり直すは「shift + Ctrl + Z」(Ctrl + Y ではない。)。
  - Alt + E -> 多様体を押し出し、で端の面とか残らずにきれいに押し出せる。
  - 簡単ワイヤーフレーム化: https://qiita.com/dimebag29/items/a8fc188edf122074d61d
  - 複数オブジェクトの回転は次で行う。
    1. shiftで回転させたいすべてのオブジェクトを選択する。
    2. 左側のツール類から、「カーソル」を選択する。
    3. R + Z で回転させる。
  - 連結した面を選択する方法。
    1. 選択したい面の一つを選択。
    2. Ctrl + L で 連結した面をすべて選択。
  - Alt + N で法線方向に伸縮
  - shift + w で bend (曲げ)

# Unity 
  - shift + space でアクティブ画面を最大化、最小化
  - Ultra Shader, Mega Shader
    - モデルごとにマスクテクスチャを用意する必要があり、使いこなしが大変そう。上手く使えば綺麗に見えるかも。
  - Planet Shader 
    - 地球儀を作るときに便利そう

# Udon sharp
  - オイラー角 (x, y, z) は、x 軸を中心に x 度回した後、y 軸を中心に y 度回した後、 z 軸を中心に z 度 回転するという意味。
  - transform.ROtate((x, y, z)) と書けば、(x,y,z)のオイラー角の回転を行う
  - メソッドなどは Unity の公式マニュアルを参照するといい: https://docs.unity3d.com/2022.3/Documentation/ScriptReference/Transform.html
  - ネットワーキングの概要
    - 変数: 色、数値などを格納するコンテナ
    - イベント: ある瞬間に起こる出来事
    - デフォルトでオブジェクトはローカル(自分の下でしか動かない)
    - オブジェクトを同期するには、ネットワークオブジェクトであることを VRC に伝える必要がある。
    - 最初にワールドを開いたプレイヤーが、ネットワーク上のすべてのオブジェクトの所有者となる。
      - これらのオブジェクトに変更を加えることができ、その変更はほかのすべてのユーザに送信される。
      - オブジェクトの所有者を変更すると、新しい所有者がネットワークデータを管理する。
    - 例
      - Pickup は オブジェクトをピックアップ可能にし、それを拾った人に所有権を与える。
    - 伝達される値はパックされてほかの人に送信される → Serialization
    - 他のプレーヤーが受け取る → desirialization
    - イベントは発生し、その後消える。
      - 変数は所有者だけが更新できる。
      - イベントは全員に送信するか、そのオブジェクトの所有者だけに送信するかを選択できる。
    - ワールドに参加する人には、変数が更新されるが、イベントは更新されない。
      - 最新のデータを取得し、デシリアライズ時にイベントが発生する。
    - 同期は変数と変数のイベントを通じて行われる。
      - ネットワークオブジェクトの所有者は変数を更新し、そのデータをデシリアライズする他のプレイヤーに送信する。
  - オーナーが変更された後、同期変数を即座に変更すると、OnDesirialization に追い付かない可能性がある
    - オーナーの変更には時間を要し、古いオーナーが持つ古い値で同期される可能性があるため。

# Clip Studio Paint
  - 明るさとコントラストの調整
    - 調整したいレイヤを右クリックして、新規色調補正レイヤーを選択。
    - 明るさ、コントラストを選択。
    - スライダーで明るさやコントラストを調整する。

# ArtStation
  - 他のアルバムに移すときは、作品の編集画面に移って、「Album」の移したいフォルダ名にチェックを入れる。

# Zotero
  - 並べて表示したくないときは、「表示」 -> 「スプレッドなし」にチェック

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

# general word
  - アルベド(Albedo)
    - 物体表面で反射される光の割合。
  - 追憶
    - 過ぎ去ったことに思いをはせること。
  
# English vocabulary
  - duplication: 重複

# note
  - ２回エンターで+を増やす。

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
  - VRC World アップロード時のエラー
    ```
    The VRCSDK build was aborted because the IVRCSDKPreprocessSceneCallback 'AssignSceneNetworkIDs' reported a failure.
    ```
    が出た場合は、インスペクター欄で「Network ID」と検索して、「select」を押せるオブジェクトは押すと直る。Object sync に Udon behavior をつけると起こる可能性があるかも。</br>
    参考: https://note.com/tsukiyomirua/n/n04058347db28
  - Unityのplaymodeでのエラー
    ```
    Layer Settings VRChat scenes must have the same Unity layer configuration as VRChat. Please see the VRChat Build Control Panel to setup the projects layers and collision matric
    ```
      - VRChat SDK のコントールパネルで、「Fix Layers」や「Fix Collision Matrix」のようなボタンが表示されている場合、それをクリックして自動で設定を調整する。
    - プロジェクトをバージョンアップした後に出てきたので、その関係かもしれない。

# others
  - quest3 のドリフト改善参考
    - https://www.meta.com/ja-jp/help/quest/articles/fix-a-problem/troubleshoot-headsets-and-accessories/touch-controller-drift/
  - 日本語入力モードで Ctrl + I でカタカナに変換。
  - pwd は print working directory の略。
  - Windows + V でクリップボードの履歴を表示できる。
  - "* は X11 ウィンドウシステムのプライマリクリップボードを表す。
    - X Window System 参考:  https://qiita.com/kakkie/items/c6ccce13ce0beaefaad1
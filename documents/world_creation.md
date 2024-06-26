Author: くろしま </br>
参考: https://note.com/watahumi_mina/ by wata23


# VRChat初心者に伝えたい、情報を得るときの基本的で大事なこと
## 情報を得るときの基本的で大事なこと
  - それがいつごろ発信された情報なのか。
    - VRChatのコンテンツがUnityというゲームエンジンをもとにしており、細かくアップデートされている(バージョンごとにサポート期間が決まっている。)
    - Cannyというユーザーの要望・不具合報告サイトをもとにしてアップデートしている。</br>
    canny: https://vrchat.canny.io/
  - 100パーセント信じない。
    - VRChatを始める大多数は、最初はUnityを知らない素人である。
    - VRChat向けの技術的な記事を書いている人の大多数は「独学で学んでいる人」
      - 「正しいやり方ではないけど結果的にうまくいったパターン」が含まれる。
    　- 「自分の環境ではうまくいく」ものが含まれる。
## 効率のいい情報収集の方法
  - 技術的に強い人の X をフォローする。
  - VRChat公式のアップデート内容を都度確認する。
  - Twitterで検索する。
    - 些細なことは X につぶやくことが多い。
  - 詳しい人に直接聞く。
    - ものすごく近道。お礼を忘れずに。

</br>

# VRChat初心者のためのUnityコンポーネント入門
## コンポーネントとは?
  - Unityを開いた時のウィンドウの役割に当てはめる
  ![alt text](../images/unity_window.png) </br>
  机の上に置いたものを「ゲームオブジェクト」といい、「ゲームオブジェクト」がどんな形をしていてどんな性質をもっているかは、どんな「コンポーネント」があるかによって決まる。</br>例: </br>
  ![alt text](../images/component_example.png)
  「コンポーネント」を「ゲームオブジェクト」につけることで、色々な機能を付与できる。
## CRChatのコンポーネントの制限
  - 次のサイトで使用できるコンポーネントが確認できる(World)。</br>
    https://creators.vrchat.com/worlds/whitelisted-world-components/
## コンポーネント紹介
  - Transform
    - 全てのゲームオブジェクトについていて、削除することができない。位置、回転、大きさを調整することができる。
  - Mesh Renderer
    - 動かない3Dモデルに使うコンポーネントで、3Dモデルの外見を決めるコンポーネント。
    - 3Dモデルの見え方(どんな模様をしているかやどれくらい透明かなど)を決定する。「マテリアル」を指定する部分をはじめとして色々な項目がある。
    - オブジェクトの「見た目」を調整したいときに触るコンポーネント。
    - このコンポーネントを作ると、Mesh Filterというメッシュと呼ばれる3Dモデルの形状のデータが指定される。
  - VRC Scene Descripter 

    ![alt text](../images/vrc_scene_descripter.png) </br>

    ワールドをアップロードするときに必要となる、ワールド限定のコンポーネント。
    - Reference Camera: プレイヤーの目となるカメラのリファレンス。
    - Respone Height Y: リスポーンさせられる高さ。
    - このコンポーネントがついているオブジェクトのZ方向が、ワールドに入ったときの向きになる。
  - Pipeline Manager
    - アップロードされるワールドにはBluePrintIDが付与される。IDが割り振られた後にこのコンポーネント上でDetachというボタンを押すことでBluePrintIDを空欄にすることができる。空欄のままアップロードするとIDが新しくなり、別のワールドとしてアップロードされる。
    - すでにアップロードしたデータに上書きしたい場合は、SDKコンテンツ管理画面からBluePrintIDをコピーして、Detachしたあとの空欄に貼り付けてからAttachすることで、上書きアップロードすることができる。 
  - Animator
    - 3Dオブジェクトの動きを制御できる。
    - 他のコンポーネントの値を、Animator経由で変化させられる。
    - アニメーションを切り替える条件を設定しておくことができる。
  - Tree
    - Unity標準の木を作るシステム。
  - NavMesh系
    - NPCキャラクターなどに自動追尾させることができる。
  - Projector
    - テクスチャを投影することができる。
    - 影の作成などができる

    ![alt text](../images/projector_image.png) </br>

  - (Aim/LookAt/Parent/Position/Rotation/Scale) Constraint
    - 他のオブジェクトの変化(位置・回転・スケールの変更)に従って、ゲームオブジェクトに制約を付ける。
      - 他のゲームオブジェクトがある位置に移動するときに、同じ分だけ移動したりなど。
  - VRC_MirrorReflection
    - ミラーとして使える。
  - VRC_AvaterPedestal
    - アバターのペデスタルを置ける。
  - VRC_PortalMaker
    - ポータルを置ける。
  - uGUI系
    - Unity標準のUI
    - ボタンなどがある。 

# VRChat初心者に送る、Unityの親子関係・階層について
## 親子関係・階層
  - ヒエラルキー: Unityの左側のウィンドウ

  ![alt text](../images/hierarcy_image.png)

  - ヒエラルキーにあるゲームオブジェクトを長押しでつかんで、ほかのゲームオブジェクト上で離す(ドラッグ＆ドロップと呼ぶ)と、次のようにオブジェクト名が一段下がる。

  ![alt text](../images/drag_and_drop_image.png)

  - ２つのゲームオブジェクトは、「階層」を形作っており、上の階層にあるオブジェクトを親オブジェクト、下の階層にあるオブジェクトを子オブジェクトという。
    - 親子関係とは、ゲームオブジェクト同士の関係性を表した言葉である。
    - 子に対して親は一つだけである。
    - 一番上の親オブジェクトをルートオブジェクトという。
  - 親子関係・階層というシステムがあるのは、そのほうが便利だから。
## 親子関係・階層のメリット
  - 「親を移動させると、子も移動する」
    - 逆は違っていて、子を移動させても親は移動しない。
## 親子関係の特性
  - 各オブジェクトには、そのゲームオブジェクトの位置・角度・大きさの情報を持つ、Transformコンポーネントが必ずついてくる。
  - 子オブジェクトのTransformコンポーネントの位置の値は、親オブジェクトのTransformの位置を基準(=原点)としたものになっている。
    - 親オブジェクトはシーン画面上1個あるワールド座標を原点とする。
    - 子オブジェクトは自分の親となるオブジェクトの座標を基準としている(ローカル座標という)。
# 親の変更は子すべてに波及する
  - 例えば、親のスケールを３倍にしたとき、子も３倍になる。
# 親子関係の相対性の利用方法
  - 扉をはめようと思うと、縦に大きかった場合を考える。
  - 基準の中心位置が真ん中にあった場合、Transformコンポーネントのスケールを変えると、上下に同じ分だけ伸び縮みする。
  - 親オブジェクトが子オブジェクトの基準になることを利用する。
  - 空のゲームオブジェクトを扉の左下に配置する。

  ![alt text](../images/door_image.png)
 
  - 左下が基準(原点)となるため、上方向にスケールすると、オブジェクトの各座標には定数が乗算され、特に下は0のため、定数を乗算しても変わらない。したがって上方向にだけのびる。
  - また、回転をすると、左下を中心に回転する。
## 相対性を利用した値の直接入力(記事内容とはあまり関係ないけど知らなかったこと)
  - オブジェクトのTransformの座標にたとえば、+5 と打ち込むと、５m先に移動する。これをコピーしたオブジェクトごとに行えば等間隔に並べることができる。 

# お勧めのUnityのショートカット【VRChat】
## Sceneの画面移動
  - 前後左右: 右クリック + WASD
  - 上下: 右クリック + EQ 
    - shift 同時押しで加速。
    - 加速量は右クリックを押したまま、マウスホイールをスクロールすると調節できる。
      - Gizumoボタン横のカメラマークでも設定可(Camera Speed)
      ![alt text](../images/camera_mark_image.png)
## 操作ツールの切り替え
  - Q: ハンドツール
  - W: 移動
  - E: 回転
  - R: 拡大縮小
  - T: 矩形トランスフォーム
  - Y: トランスフォーム(移動・回転・拡大縮小の組み合わせ)
## Pivot/Center、Local/Global
![alt text](../images/pivot_local_image.png)
  - Pivot/Center: 選択ツールの操作を行うときの基準点の位置を選択
    - Pivot: モデルの原点
    - Center: オブジェクトの中心
      - 親子関係にあるときに使えそう。
  - Local/Global: 選択ツールで操作する基準点のXYZ軸を切り替えられる。
    - Local: オブジェクト基準
    - Global: ワールド基準
      - Localでオブジェクトを回転させて、Glbalでワールドに対して平行に下げる、という使い方が可能
## 操作の取り消し・やり直し
  - Ctrl + Z: 取り消し
  - Ctrl + Y: やり直し
## フォーカス
  - オブジェクトを選択しているときにFキーを押すと、そのオブジェクトに注視する。(Hierarchyのオブジェクト名ダブルクリックでもできる。)
  - 「近づくと消える」場合、大きいオブジェクトを編集した後になっている。(適当に小さいオブジェクトを注視すると直る。)
## スナップ機能
  - オブジェクトを選択した状態でvキーを押しながら移動: 頂点スナップ
    - 操作するときの基準点をマウスポインタの位置に持ってこれる。
    - 移動操作で角あたりをおすとオブジェクト同士をぴったりくっつけられる。
## Sceneビューにオブジェクトの位置を合わせる
  - オブジェクトを選択した状態で、Ctrl + Shift + F を押すと、Sceneで見ている位置にオブジェクトを持ってくることができる。
  - MainCameraを選択した状態で、このショートカットキーを使うことで、GameビューとSceneビューを一致させることができる。
## Hierarchyでよく使うやつ
  - オブジェクトを選択した状態でDelete: 削除
  - オブジェクトを選択した状態でCtrl + D: 複製
  - Altキーを押しながら、ツリーの矢印を押す: ツリーをすべて展開、またはすべて閉じる
## Windouws共通
  - Ctrl + C: 値などの文字コピー
  - Ctrl + V: Ctrl + Cでコピーしたものの貼り付け
  - オブジェクトやファイルなどを選択中にF2: 名前の編集
  - ファイルなどが連続している場所で、１つクリックした後にもう一つをShift+クリック：最初にクリックした場所からShift+クリックした部分までをまとめて選択
  - Ctrl押しながらクリック：現在選択しているものに、追加して選択
  - Ctrl+A：全選択
  - Ctrl+S：編集中のファイルのセーブ


# アバターからワールドまで！VRChatユーザーのための Unity Scene入門ガイド
## UnityのSceneとその本体について
  - UnityのSceneファイルは、Unityでアバターの改変やワールド制作を行った後に保存されるセーブデータに該当する。
    - UnityのHierarchyの状態や環境設定などが保存されている。
  - 本体は、Hierarchy上ではなくプロジェクトウィンドウ内に保存されている。
## そもそものSceneの使われ方
  - VRChatでは一つのScene上でデータを編集し、それをVRCSDKを通してアップロードする形が一般的。
  - Unityでゲームを制作する場合は、「複数のSceneを切り替えて使う」方法がある。
    - 例えば、次の図のようにゲームの進行に合わせて、シーンの切り替えを行うことが可能である。
    ![alt text](../images/scene_image.png)
    - VRChatは１つのシーンしか扱えない。
## UnityのSceneに保存されている情報について
  - UnityのSceneファイルには、Hierarchy上の情報だけではなく、環境設定系のデータも紐づけて保存されている。
    - RenderSettingとLightmapSettings(どちらもLightningウィンドウにある)
    -NavMeshの設定。
      - NavMesh: シーン上をAIで自動に移動する3Dモデルを作れる機能。
    - ゲームのシーンが切り替わるときにライティングなどの設定が変わる。
    - 独自レイヤーを使用しているオブジェクトがあるシーンを、別のプロジェクトで開いてみると、レイヤーの割り当てがない状態となる(default layer)。
## Scene の複数編集について
  - Unityでは複数個のシーンを同時に開いて、編集することができる。
    - シーンファイルをヒエラルキー上にドラッグ＆ドロップする。
    - 展開されたシーンのオブジェクトは自由に操作することができ、別のシーンにドラッグ＆ドロップでオブジェクトを移動させることなども出来る。
    参考: https://summer2022.vket.com/docs/submission_tips_how_to_object_copy
    - 消すときはシーンファイル名のところで右クリックし、Remove Sceneを選択すると消すことができる。
      - ライティング・オクルージョンカリングなどの環境設定は、すでに開いているシーンのものになっている。そのため新規に開いたシーンの環境設定は無視される。
## Unityアセットのでもシーンを使った
  - Unityアセットにはでもシーンがあるため、ドラッグ＆ドロップでシーンを並べた後、ゲームオブジェクトを一つにシーンに統合する方法がある。
    - シーンが整っているため、オブジェクトの配置に手間をとられないのがメリット。
    - 高負荷のものがあるため、負荷を減らしたいと思ったときに最適化の技法と時間が求められる。
    - インポート時にエラーが起こるため、初心者には勧めづらい。
## Sceneファイルの中身について
  - プロジェクトタブ上でシーンファイルを右クリックし、「Show in Explores」エクスプローラーで開く。
  - エクスプローラー上で右クリックし、「プログラムから開く」を選択。その他のオプションからメモ帳を選ぶ。
  - シーンファイルは、YAMLと呼ばれるフォーマットに従って書かれた文字列である。
    - シーンファイルは、あくまでそのデータがおかれている場所、すなわち参照のみを保存している。
    FBXやプレハブを消すと、Hierarchy上で赤く表示される現象は、参照先のデータが失われているために起こる現象。
## シーンに関する小ネタ
### シーンファイルの複製
  - プロジェクトタブ上で ctrl + D でシーンファイルを複製することができる。Hierarchyを大幅に変更するときはこれでバックアップを取ることができる。
    - シーンは複数編集できるため、うっかり消したゲームオブジェクトを部分的に戻したいと思ったときは、バックアップしたシーンをドラッグ＆ドロップして、ゲームオブジェクトを戻す、ということも可能。
### 未セーブ状態で突然Unityが落ちた時のリカバリー
  - Unityを開く前であれば、シーンファイルのバックアップが保存される。
    - 使っていたプロジェクトのフォルダ内にバックアップ用のファイルがある。
    - Asset フォルダに中身を移したうえで、拡張子を「.unity」にすることでシーンファイルになるため、ダブルクリックすると開ける。
### シーンファイル名「Sample Scene」は危険！？
  - (VCC以前)Unityアセットストアのシーンファイル名もSample Sceneであることがあり、上書きされてこれまでのデータが消える可能性があった。


# VRChat初心者の躓きやすいUnityエラーの対処法
## VRSDKのBuildボタンが消えた！
  - 画面左側にあるConsoleというタブを開く。
  ![alt text](../images/console_image.png)
  - 項目がたくさん出てくる(Unityのログの一覧)。
  ![alt text](../images/log_image.png)
  - 重要度に応じて、白<黄色<赤 となっている。
    - 白い吹き出しにビックリマークのアイコンは最も影響が無いもの。</br>
    ![alt text](../images/white_icon_image.png)
    - 黄色に三角形にビックリマーク。ちょっと問題はありますが、大きい影響はありません。</br>
    ![alt text](../images/yellow_icon_image.png)
    - 赤い8角形にビックリマーク。明確に問題があるエラー。</br>
    ![alt text](../images/red_icon_image.png)
      - 無視してもUnityが問題なく動くものと、Unityが上手く動かなくなるものが混在している。
      - 優先的に直すべきものは、「Consoleタブの左上のClearボタンを押して、残ったエラー」。
        - ログをクリックして選択すると、下の方に文章が現れるので、それをgoogleなりtwitterに検索をかけて対処。
        - 一通り対処できると、Clearボタンを押しても何も出てこなくなる。この状態になるとUnityは正常に動くようになり、VRCSDKのBuildボタンは復活している(はず)。
## そもそもエラーを起こさないためには
  - 一番大事なのは「導入手順とその順番をきちんと守る」。
    - 規定された動作しかできない機械。
    - 導入手順とその順番をきちんと守れば、エラーが起きる可能性はぐっと減る。
## エラーの原因を少なくしよう
  - 新しい何かを追加(インポート)したら、コンソールをチェックする。
  - すでにある何かを削除したら、コンソールをチェックする。
    - 基本的に今まで大丈夫だったプロジェクトがエラーで動かなくなるタイミングは、何かをインポートしたときか何かを間違って削除したときである。
      - インポートしたときに起こるエラーは、何か前提となるものが入っていないケースや、その環境では利用できないものを入れてしまった場合が多い。
      - 間違って削除したときは、依存関係を壊してしまって、エラーになっていることが多い。
    - インポート時にエラーが起こった場合は、その時インポートされたファイルを削除するだけでエラーが解消される。
      - インポートされたファイルについては、インポート時に以下のようなリストが出てくるが、このチェックが入っているものが追加される。
      - 削除したいときは、このリストに載っているものを削除すれば良い。
      ![alt text](../images/import_image.png)
    - 間違って削除したときは、削除してすぐなら、冷静に Ctrl+Z のショートカットを押すことで元に戻る。
      - Unityを一度閉じてしまうとダメなので、そのときは消してしまったファイルのあるUnityPackageを再インポートする。
  - Unityの動作がおかしくなっているケースもある。
    - 謎のエラーが起こったときは、何も考えずにUnityを閉じてもう一回開きなおすと直ることもある。


# 同じワールドやアバターを、別のデータとしてアップロードする方法 ～VRChatのBlueprint IDについて～
## BlueprintIDについて
  - Blueprint IDは、VRChat側がワールドやアバターを管理するためにつけているID
    - Unityを使って、VRChat上にデータをアップロードするときに自動的に割り当てられるもの。
    - このIDはユニークなものであり、ほかの人と被らないようになっている。
  - Blueprint IDの仕様をうまく使うことで、同じアバターやワールドを別データとしてあげたり、アップロード済みの既存のデータに上書きしたりすることが可能である。
## Blueprint IDの新規作成・切り替えなどについて
  - Blueprint IDを管理するためにPipeline Managerという名前のコンポーネントがある。
    - ワールドであれば、VRCWorldという名前のゲームオブジェクトについている、VRC Scene Descripterコンポーネントの下にある。
    - 一度でもアップロードしたデータであれば、以下のようにアップロード時のBlueprint IDが記載されている。
    ![alt text](../images/blueprint_upload_image.png)
    - 一度もアップロードしたことがない場合は以下のように空欄になっている。
    ![alt text](../images/blueprint_non_upload_image.png)
      - この空欄の状態でアップロードすると、自動的に新しいBlueprint IDが割り振られて、Blueprint IDが表示されるようになる。
## 別データとしてのアップロード方法
  - 別データとして、アップロードしたい場合はPipeline ManagerのDetachボタンを押す。
  - 紐づけられていたBlueprint IDが解除され、新しい状態になるので、この状態でアップロードすると新規IDが割り振られて、別データとしてアップロードすることができる。
## 既存データへの切り替え・上書き・削除など
  - VRChat SDKのタブにContent Managerというタブがある。
  - 現在紐づけられているBlueprint IDがあるときは、データの横に(Current)という表記がつく。 
  - この状態から別のデータに切り替えを行いたいときは、切り替えを行いたいデータのところにあるSet Currentボタンを押す。
  - 削除したい場合は、Deleteボタンを押すことで削除ができる。
## Blueprint ID で注意したいこと
  - ワールドやアバターの販売・配布時にBluprint IDが残ったデータを配布してしまうと、アップロードしようとしたときにエラーが発生する。
    - 他人にデータを販売、配布するときはBlueprint IDを空欄にしておく。
  - ワールドは複数Pipeline Managerがあると、一つにするようにと注意書きが出る。
## PC・Quest両対応したいときについて
  - PC版をすでにアップロード済みだとする。このときAndroid向けに切り替えたプロジェクトで、"PC版と同じBlueprint ID"に対してアップロードを行うことでQuest版を追加することができる。


# 簡単なUnityプロジェクトのバックアップ方法
## 各種バックアップ方法
  - ファイルごとコピー
    - 簡単、無料、手動、非常に時間がかかる、全部コピーする必要がある。
  - VCCのバックアップ機能
    - ファイルごとコピーを必要最低限のフォルダのみ行う。
      - **ワールドのバックアップにはおすすめできない。**(キャッシュ情報はなくなる)
  - Collaborate
    - Unity上でできる、無料、差分セーブ可能、容量が少ない
      - クラウド容量1GBのため、もはや使えない。
  - Github
    - 難しい、無料、差分セーブ可能、容量は外付けHDD等に保存することで解決する。
      - 無料で使えるクラウドの容量は5GB。
  - **Turbo Backup PRO(おすすめ)**
    - 簡単、有料(52.8ドル(約８千円...))、差分セーブ、自動セーブ、保存場所は自由


# ライトベイクに挑戦する前に読むと良いかもしれない記事
## 前提知識 : VRCの映像ができるまで
  - 1秒間にFPS枚の絵が描かれ、更新される。
  - 描画処理が何らかの理由で間に合わないときに、FPSが下がる。
  - 絵を表示する側のHMDやモニター側にも更新速度があり、こちらはリフレッシュレートと呼ばれる(単位はHz)。
  - PCのスペックが200FPSでも、絵を表示する側が50Hzだと、FPSは50しか出ない。
## ライトベイクのいいところ
  - Unityではライトコンポーネントのついたゲームオブジェクトを置くことで、光源を作ることができる。
  - オブジェクト・光源の数が多ければ多いほど、負荷は増大する。
  - 静止している光源については、光と影が動くことはない。だから、事前に計算をして、その結果を保存しておけばよい。
  - 計算結果は、ライトマップと呼ばれるテクスチャで保存される。
  - ライトベイクの影響する各要素の関連性が見えていない。
## ライトマップができるまで
  - アバターには画像を、UVと呼ばれる3Dモデルを平面に展開した、展開図に対して画像を重ねている。
  - ライトマップもテクスチャのため、3Dモデルに対応するUVが必要。そのためのUVはライトマップを作るときに同時に作られる特別製のもの。
    - 1枚のライトマップで、複数の3Dモデルを担当するために、複数の3DモデルからUVを集めてきて、ライトマップを作る。
    - １枚のライトマップの中には、複数のオブジェクトの光と影の計算結果が詰め込まれている。これにより、沢山のオブジェクトがあってもライトマップの枚数は少なくて済む。
    - この時に収集されてくるUVは、Unity上ではUV2と呼ばれる２枚目のUVになる。
    - ライトマップが作られるまでの流れ
      1. Staticフラグがつけられているオブジェクト群からUV2の情報を集めてくる。
      2. 集めてきたUV2を敷き詰めることで、ライトマップ用のUVを作成する。
      3. 最終的に出来上がったライトマップ用UVをもとに、ライトマップを計算、生成する。
## UV2に求められる制約について
  - UV2は普通のテクスチャ用である１枚目のUVと比較して、特殊な制約を求められる。(だからこそ、別枠の２枚目になっている。)
    - UV展開図に重なりがないこと。
      - 光と影の計算結果が２重に保存されてしまうため。
    - UV展開図の展開されたパーツ間に十分な隙間があること。
      - 暗い部分に明るい部分がにじむことを防ぐため。
    - UV展開図が0~1に収まっていること。
      - 範囲外にはみ出すのを防ぐため。
    - 3DモデルにUV2があるかどうかを確認する必要がある。
      - 確認したいオブジェクトのメッシュデータを探す。
      - Meshfilterのところにあるアイテムをクリックするとわかりやすい。
      ![alt text](../images/mesh_renderer_image.png)
      - メッシュデータの右下のプレビューが表示され、UV2が格納されていると、uv2と表記されている。
    - UV2がないときは、FBXを選択したときに、modelタブの一番下あたりにgenerate lightmap uvsという項目があり、ここにチェックを入れることで、UV1の情報をもとにUnityがUV2を自動生成される。
    ![alt text](../images/generate_lightmap_uvs_image.png)
## ライトベイクに必要なこと！
  - ベイク設定のライト
  - staticのチェック
  - UV2
## ライトマップの解像度について
  - ライトマップにも解像度があり、沢山のUV2を敷き詰める必要があるため、解像度が重要になってくる。
  - ライトマップの解像度を確保する方法。
    1. ライトマップ自遺体の解像度を上げる
      - ライトマップ自体のサイズを大きくすればよいが、その分ライトマップの容量は大きくなってしまう。
      - Unityでは「Lightmap Resolution」と表記されているパラメーター。デフォルトでかなり大きい。
    2. 各モデルごとに割り当てられるUV2の領域を変える。
      - 各UV2ごとに、敷き詰められる時のサイズを変えることもできる。MeshRendererにあるScale in Lightmapという項目がそう。
      - ベイクする前には隠れていて、Contributed Global Illuminatorという項目にチェックを入れるか、Staticフラグにチェックを入れると出てくる。
      ![alt text](../images/scale_in_lightmap_image.png)
      - 重要ではないオブジェクトの割り当て領域を小さくして、重要なオブジェクトに領域を割くなどの工夫をすれば、容量を節約しながら綺麗に見せることも可能
    3. UV2を作り直して再展開する。
      - Blender等のモデリングソフトでUV2を展開・編集するという手もある。これは各モデルのUV2に対して行う。
## その他
  - color temparature mode で寒色から暖色に変えられる。

# "反射"を制して綺麗なワールドを！クオリティを上げるReflection Probeとは？
## Reflection Probeとは？
  - 反射する物体に映りこむ景色の情報を与えるもの。
  - デフォルトの反射の景色はSkybox。Reflection Probeを設定することではじめて反射に映りこむ景色を「上書き」できる。
  - Reflection Probeはキューブマップと呼ばれる特殊なテクスチャを生成して使う。
    - キューブマップを使ってできた疑似的な立方体による風景は、境目をうまく処理することにより球体のように見えるので、Skyboxなどにもキューブマップが利用されたりする(なので、Sky"box")。
## デフォルトの反射光設定変更
  - デフォルトの反射で使われている景色を変更する場所は、[Windws]→[Rendering]→[LightingSettings]のウィンドウの中にあるEnvironment Reflectionという項目。
  ![alt text](../images/lightning_setting_image.png)
    - デフォルトではSourceがSkyboxになっているが、Customを選択することにより独自のcubemapを使用することができる。
## shader側の設定項目
  - MetallicとRoughnessはどちらもReflection Probeに関わりのあるパラメータ。
  - Metallicはそもそもの反射率に、Smoothness(ShaderによってはRoughness)は映り込むReflection Probeの粗さに関係する。
## Reflection Probe側の設定
  - 上部アイコン二つ
    - 全射は Refection Probeの影響を受ける範囲を設定し、後者はCubemapを撮影する位置を設定する。
  - TypeをCustomにし、Dynamic Objectにチェックを入れると、Staticのチェックに関係なく、すべてのオブジェクトを撮影する。
## Reflection Probeの細かい制御方法
  - 調整したいゲームオブジェクトのMeshRendererのAnchor OverrideにReflection Probeのゲームオブジェクトを入れることで、そのReflection Probeの影響だけを受けるようになる。


# VRChatでの音の付け方 ～AudioSource周りのあれこれ～
## AudioClipとAudioSourceについて
  - 現実で音楽を聴きたいとき、必要なものが二つある。
    - 音源データ
    - 音源データを再生するための機器
  - Unityでも同じ働きをするものがある
    - AudioClip
    - AudioSource
  - Unity上にインポートされた音源データは、AudioClipの設定に従って再構成されて扱われる。
  - AudioListenerもあるが、自動で設定される(たしかカメラとかについてる)
## 2D・3D音源について
  - 生活の中でなっている音は、音の発生源があり、左右のボリューム差によって、音の発生源がどこにあるか聞き分けることができる。
    - 音の発生源が決まっていて、一夜向きによって聞こえ方が変わる音源をUniity上では3D音源として扱う。
  - 2D音源は、どのような位置、向きにおいても同じ聞こえ方をするものになる。
  - 2D音源はBGMに使われ、3D音源は効果音などに使われる。
  - Spatial Blendにより、中間の性質を持たせることができる。
## 具体的な設定方法について
### AudioClipの設定
![alt text](../images/audio_clip_image.png)
  - Force To Mono: ステレオの音源をモノラル音源にする。
    - 表現力は下がるが、容量が半分になるという利点がある。
  - Compression Format
    - 基本的にVobisで問題ない。PCMは無圧縮、ADPCMはPCMの1/3.5の圧縮率で、高品質になるが、容量が非常に大きくなる。
  - Quality
    - 下げると高音域(15kHz)が削られるらしい。重要でな効果音はこれを利用することにより、ワールド容量を減らすことができる。圧縮形式がVovisのときのみ使える。
  - Sample Rate Setting
    - PCM、ADPCM用の軽量化オプション
### BGMなどの2D音源
  - Loop
    - デフォルトだと、１回再生し終わると終わる。
  - Volume
    - 0～1の値で設定する。基本大きいので、小さめの値から設定する。
### 効果音などの3D音源
  - VRC Spatial Audio Sourceと呼ばれるコンポーネントを利用するかしないかでかわる。
  -Spatial Audio Sourceを使わない場合
    - Volume
      - 2D音源と同じ。
    - Spatial Blend
      - 2D音源と3D音源のブレンド具合。
    - 3D Sound Settings
      - Doppler Level
        - 今はもう無効。
      - Spread
        - 音が聞こえる角度を示す。180°だと均等に聞こえる。
      - Volume Rolloff
        - 音量や各種エフェクトを距離に応じて制御する波形のタイプ。
      - Min Distance
        - 最大の音量が維持される距離。この数値より近い距離にいた場合、常に最大になる。
        - 音量が０になるポイントで**はない**。
    - 波形グラフ
    ![alt text](../images/wave_graph_image.png)
      - 横軸が音源からの距離で、縦軸が大きさ。横軸の大きさはMax Distanceに対応する。
      - 4つのパラメーターを距離ごとに設定することができる。
      - 制御点を加えたりのぞいたりすることで、曲線を調整できる。
  - Spatial Audio Sourceを使う場合
    - AudioSourceのついたゲームオブジェクトを追加する形で使う。
    ![alt text](../images/spatial_audio_source_image.png)
      - GainはVolumeと同時に機能し、音が小さすぎるときに使うとよい(あげすぎると音割れする。)
      - Volumetric Radiusは音が回り込んでくる距離を示す。
      - Enable Spatializationはつけていないと3D音源にならない。
      - Use Audio Source Volume Curveはチェックを入れていないと、波形グラフによるVolumeの調整がNearとFarの逆２乗の波形で上書きされる。
  - 全ての音源にエフェクトをかけたい場合
    - 適当なゲームオブジェクトにAudio Listenerというコンポーネントをつけて、それにつけたいエフェクトのコンポーネントをつける。
      - フィルター系はワールド開始時にオンになっていないと作動しない。
  - 音源ごとにエフェクトをかけたい場合
    - AudioSourceのついたゲームオブジェクトに、エフェクトのコンポーネントをつける。
  - エリアごとにリバーブをかけたい場合
    - AudioReverbZoneコンポーネントのついたゲームオブジェクトを配置することで、そのAudioReverbZoneの影響範囲に入ったときだけエフェクトをかけることができる。
      - VRC Audio SourceつきのAudioSourceでは無効化される。
  - Spatial Audio Sourceコンポーネントはシームレスに音が変化してよいらしい。

# VRChatワールド制作における『Layer』の役割
  - 公式マニュアル
    https://creators.vrchat.com/worlds/layers/
## 『Layer』とは
  - Unityにおけるレイヤーはグループ分けのようなもの。
    - グループ分けをしておくと、ある特定の効果を反映するか・しないかをグループごとにコントロールすることができる。
    - グループ分けは、各ゲームオブジェクトごとに行われる。
  - 0番から31番まであって、そのいずれかが必ずゲームオブジェクトに割り振られている。
  - 初期状態では、0番目の「Default」 レイヤーに、ゲームオブジェクトが所属している。
  - 具体例としては、一つの光源があったとして、その光源によって明るくなる・明るくならないをレイヤーごとに決めることができる。
    1. 光が当たる・当たらんないをオブジェクトごとに制御できる。
    2. 影ができる・できないをオブジェクトごとに制御できる。
    3. 光源の影響を受けないオブジェクトは光源の計算がいらなくなるので軽量化につながるケースがある。（つかえそう！）
## レイヤーに関係しているもの
  - カメラの描画設定
  - ミラーの描画設定
  - コライダーの衝突設定
  - 光源が影響を与えるオブジェクトの設定
  - PostProcessingの設定
  - Udonの制御(レイキャストなど)
  - パーティクルのプレビューの表示非表示
### カメラの描画設定
  - カメラに対して映る・映らないを設定することができる。
  - カメラコンポ―ネントの上あたりにあるCulling Maskで映したいレイヤーにチェックを入れ、それ以外はチェックをはずせばよい。
    - Main Cameraでこの項目をいじっても、VRChat内のプレイヤーの視界に映らなくなるわけではない。
### ミラーの描画設定
  - ミラーに映る・映らないを設定することができる。
  - VRC_Mirrorコンポーネントの下あたりにあるReflect Layersで映したいレイヤーにチェックを入れ、それ以外はチェックを外せばよい。
  - 面倒であれば、「Show only players」や「Show players/world」を押すとレイヤーのプリセットが利用できる。
### コライダーの衝突設定
  - 各レイヤ同士が衝突するか・しないかを設定することができる。
    - 左上のメニュー[Edit]→[Project Settings]→[Pysics]のところで設定できる。
      ![alt text](../images/Collision_matrix_image.png)
### 光源が影響を与えるオブジェクトの設定
  - 特定の光源からの光を受ける・受けないを設定することができる。
  - Lightコンポーネントの下の方にあるCulling maskで光を受けてほしいレイヤーにチェックを入れ、それ以外はチェックを外せばOK。
### PostProcessingの設定
  - 影響を与える・与えないではなく、PostProcessing Volumeのコンポーネントが付いたオブジェクトを指し示すために使われる。
### Udonの制御
  - レイキャストを飛ばすときに特定のレイヤーだけ検出するようにすることができる。
### パーティクルのプレビューの表示非表示
  - Hierarchyでパーティクルを選択したときに、Sceneビューの右下に出てくる小さいウィンドウの中に、Simulate Layersという項目がある。
    - デフォルトは選択したパーティクルをプレビューしますが、Simulate Layers を Nothing 以外にすると選んだレイヤーに所属したパーティクルが常時プレビューされる。
    - Everythingにすると全てのパーティクルが常時プレビューされる。
## 既存レイヤーについての説明
### Layer 0～7
  - Unityのデフォルトレイヤーとなっており、書き換えができない。
  - Default
    - Unityのゲームオブジェクトでデフォルトで使われているレイヤー
  - TransparentFX
    - レンズフレアの遮蔽物にならないレイヤー
  - Ignore Raycast
    - レイヤーマスクの指定がない場合、Unityのレイキャストによって無視される。
  - Water
    - 昔のUnityの標準アセットの名残。VRC看ミラーで映らないようになっている。PostProcessレイヤーの標準レイヤーとしても使用されている。
  - UI
    - VRC内のメニューなどいろいろなUI系が入っている。使用は非推奨。
    - ここに所属しているオブジェクトはVRCのメニューを開いている時だけ表示され、インタラクトについてもメニューを開いた状態でレーザービームを当てた状態でのみインタラクトできる。
    - 他の既存のどのレイヤーとも衝突しない初期設定になっている。そして、VRカメラに映らないレイヤー。
### Layer 8～21
  - VRChat側でセットアップされていて、実際に既に利用されているレイヤー。
  - Player
    - 自分以外のプレイヤーのアバターが所属している。
  - PlayerLocal
    - 自分の頭を除いた、アバター部分が所属している。頭は自分自身には見えないので省かれている。ミラーやカメラへの自分自身の描画はPlayerLocalの代わりにMirrorReflectionを使用することで、頭を含めた全身を描画する。
  - UiMenu
    - レイヤー5のUIと性質は同じ。プレイヤーのネームプレートは子のレイヤーに所属している。
  - Pickup
    - 持てるオブジェクト用のレイヤー。PlayeとPlayerLocalに衝突しない設定になっている。
  - PickupNoEnvironment
    - Pickupのみと衝突する設定になっている。
  - Walkthrough
    - プレイヤーはこのレイヤーと衝突しない設定になっている。コライダー付きの机や椅子をこのレイヤーにすると、プレイヤーにぶつからず、Pickupはぶつかる設定になっているので便利。
  - MirrorReflection
    - ミラーやカメラで自分のアバターを描画するためのレイヤー。
    - PlayerLocalとの違いは、こちらでは頭も描画される。PlayerLocalも同時に描画対象にすると自分自身の首から下を２回描画することになり、Z-Fightingとかが起こる。
    - このレイヤーはピックアップできず、衝突もなく、レイキャストの対象外なので、プレイヤーやオブジェクトのコライダーへの進入を判定するのにちょうどいいレイヤー。
  - reserved2～4
    - 基本的に使用は非推奨。このレイヤーにオブジェクトを所属させると、アップロード時に強制的にレイヤー0(default)に動作させられる。
  - 上記以外のレイヤー
    - 使われていないので自由に使ってもよさそう。衝突設定やCulling maskなどは要注意。
  - Layer 22～31
    - 自由に使えるレイヤー。新しく作ることができる。
    - PlayerとPlayer Localには衝突しなくて、Pickupには衝突するレイヤーを作って、そこにコライダーのついた壁のオブジェクトを所属させると、ピックアップは持っていけないプレイヤーのみがすり抜ける壁、などが作れる。
## よく使われるテクニック
### アバターにのみリアルタイムライトを当てる
  - レイヤーをPlayerとPlayerLocalとMirrorReflectionに設定したリアルタイムのライトで、アバターのみに光を当てるテクニックはよく使われる。
### 影絵付きのリアルタイムライトを必要とするシェーダーへの保証
  - 一部のシェーダーは影付きのリアルタイムライトを必要とする、影付きのリアルタイムライトがないと深度情報が得られないため。
    - 影付きのリアルタイムライトは重い。
  - 何もオブジェクトが無い一つのレイヤーのみを照らす影付きのリアルタイムライトを用意する。何もオブジェクトが無くても何故かDepthが取れるので、最低限の負荷でDepthを必要とする一部のシェーダーの動作を保証できる。
### VRカメラに映らないスイッチやピックアップを作る
  -  Ignore Raycastレイヤーに突っ込んでおくと、カメラに映らず、操作も可能。
## レイヤーに関するあれこれの検証
  - Waterレイヤーはミラーに映らない仕様。
  - Bakeryどころか、そもそも標準のライトベイクシステムもCulling maskの設定を考慮していない
    - culling mask : カメラについている設定項目。映る、映らないレイヤーを指定可能。

# ライトベイクに慣れてきたころに読むといいかもしれない記事
## ライトマップのテクスチャ設定
  - テクスチャの圧縮形式は、テクスチャを選択したときに一番下に出てくる項目でできるが、タブを切り替える必要がある。PCとandroi用の設定があるので、必要に応じてチェックを入れて設定を上書きする。
    - 「RGB9e5 32 Bit Shared Exponent Float」を選択することがよい。
## 自身にライトベイクせず、他オブジェクトに影を落としたいとき
  - MeshRendererで、Staticフラグにチェックを入れているときに出てくる、Scale in Lightmapの値を0にすることでこの状況にできる。
  - ライトマップに自身の影の影響をだしつつ、自分はライトベイクされないので、ライトマップ容量を節約し、余った部分でほかのライトマップUVを大きくして綺麗に焼いたりすることができる。
    - ライトベイクの影響を受けにくいオブジェクト(金属など)に対して、この手法を使うとよい。
  - 凹凸が少ないオブジェクトに対して、Scale in Lightmap の値を０にした状態で、自分自身の明るさをLightprobeで確保することで、疑似的にライトベイクしたかのように見せられる。
## ライトベイクは軽い？Static batchingについて
  - Batching staticをチェックを入れて、ライトベイクを実行するとStatic batchingが有効化される。
  - Static batchingはゲーム中に自動でメッシュを結合する機能。メッシュが結合されると、描画命令の回数が減って、その分軽くなる。
    - ライトベイクの働きは、Contributed GIの項目。
  - しかし、同一の３Ｄモデルであっても複製されたメッシュで結合する。
  - ゲーム中に結合されたメッシュがCPUに乗る上に、アップロード時のワールドデータにもそのメッシュ情報が格納されている(著者の調査)。
  - お勧めの方法
    - **同じメッシュ・マテリアルのオブジェクトはGPU Instancingを使う。そのうえで、一つしかないユニークなオブジェクトにだけStatic batchingを使う。**
      - GPU Instancingは同じメッシュ・マテリアルのときに、同じオブジェクトを使いまわしてくれる機能。同じオブジェクトであれば、描画命令がオブジェクト１個分で済む。
      - GPU Instancingしたとき、Contributed GIにチェックを入れ、Batching Staticのチェックを外した状態でベイクすればライトベイクできる。
## ライトベイクに非対応のShader
  - ライトベイクに非対応なシェーダーが存在する。
    - 対応シェーダーは、Standard シェーダーやAutodeskシェーダー、Fillamented Shader、mochie shaderなど
    - liltoomも設定すればベイクできるらしい
      参考: https://x.com/wata23_37/status/1801923080605880454
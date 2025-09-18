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
  - [`]3つあると # 以降の色が青くなくなる

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
  - shift + s でカーソル移動などのメニューがでる。

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

# Linux
  - Linux にはユーザが３種類ある
    - 管理者
    - システムユーザ
    - 一般ユーザ
  - Linux コマンドは、コマンド + オプション + 引数 の形。
    - Linux コマンドにはオプションの中に内部コマンドがある場合がある。
    - オプションはそのコマンドの動作を変えるための指令。
    - 引数はコマンドの操作対象。
  - PATH は大きく２つ意味がある
    - ファイルシステム中の位置
    - 環境変数
  - PATH は次のように追記する
    - PATH=$PATH:<path>
  - UNIX 環境では、ファイルやディレクトリへのアクセス権限が設定されている。
    - アクセス権限の対象は、ファイルの所有者(ファイルの作成者)、所属グループ(作成者が属するグループ)、その他のユーザ(ファイルの作成者でもなく作成者のグループにも属さない)がある。
      - それぞれに 読み込み、書き込み、実行 の権限が与えられる。
    - 「- rwx rwx rwx」
      - 「-」はファイルの種類を表す(-: ファイル、d: ディレクトリ)
      - １番目の「rwx」はファイルの所有者の権限
      - ２番目の「rwx」は所属グループの権限
      - ３番目の「rwx」はその他のユーザの権限
        - r: 読み込み、w: 書き込み、x: 実行
  - r-x を 101 などと２進数で表現して、それを10進数に変換することで、権限設定を10進数表記できる。(例: 777 はすべてのユーザに全部のアクセス権限を与える)
  - chmod <権限の10進数表記> <対象ファイル/フォルダ> で権限を与えられる。
  - モードの指定方法もある
    - ユーザは「u」、グループは「g」、その他は「o」、すべては「a」で指定し、ビットに rwx のいずれかを「+」で追加、「-」で削除する。「a」は省略できる。 
  - whatis、apropos コマンドで文字列を含む説明をもつコマンドを検索できる。
  - man <コマンド名> でコマンドの説明が見れる。jとkで上下できるのでキーボード操作で便利。見やすい気がする。
  - UNIX コマンドは実行されるとプロセスとなり、３つの入出力チャネルを持つ。
    - プロセスの入力となる標準入力、プロセスの結果を出力する標準出力、プロセスのエラーメッセージを出力する標準エラー出力。
  - パイプは(|)一つ目のコマンドの出力を二つ目のコマンドの入力に変換出来る。
  - 「>>」はファイルに追記。
  - 「1>」は標準出力。「>」と同じ
  - 「2>」は標準エラー出力。
  - 「1>」は標準出力のみファイルに書き出し、「2>」は標準エラー出力のみファイルに書き出す。「1>」で書き出して、末尾に「2>&1」を書くことで標準エラー出力を標準出力のコピーとすることで、両方をファイルに書き出すことができる。
    - 2 の出力先は 1 で指定されているものとする。(不正確？)
  - コマンドライン上で、ctrl + f で１文字進み、ctrl + b で１文字戻る。
  - set -o vim で コマンドラインでvim のような動きにできる。
  - シェルスクリプトでスペース入りのコマンドの出力結果を変数に代入するときはコマンドを `` で囲う。
  - Linux は本来OSの中で核となる部分の「カーネル」のみを表す言葉である。
    - Linux カーネルを使いやすくするために「ディストリビューション」ができた。大きくは次の４系統に分かれる。
      - RedHad系 -> CentOS や RHEL (Red Hat Enterprize Linux Server) など
      - Debian系 -> Ubuntu など
      - Slackware系 -> Slackware や openSUSE など
      - 独立系 -> 上に分類できないもの
  - apt は advanced package tool の略。

# linux command
  - nano というコマンドラインで使えるエディタもある。
  - less
    - テキストファイルの内容を表示する。
  - lv
    - さまざまな言語や文字コードのテキストファイルを表示する。
  - ed
    - 行単位でテキストファイルを編集する。
  - 「cd -P」 でシンボリックリンクの実体に移動することができる。 
  - OLDPWD で一つ目に移動したパスの環境変数。
  - 「cd - 」でOLDPWD のパスに移動できる。
  - ファイルの拡張子つけるをrename はブレース展開を利用して、「mv file{,.ext}」でできる。
  - mv -t でコマンドライン制限文字を超える場合も移動できる。
    - ls | xargs mv -t ../folder
  - cp -a でファイル構成やアクセス権限も保持してコピーする。
  - install
    - ファイルをコピーしてアクセス権限を設定する。
    - 例: install -m 777 test1 test2
  - dd
    - ファイルを変換してコピーする。
  - mkdir {a,b,c} で複数のディレクトリを作成できる。-m をつけて権限を指定できる。
  - rmdir
    - 空のディレクトリを削除する。
  - shred (シュレッド)
    - ファイルを安全かつ完全に削除する。
  - file
    - ファイルの種類を判別する。
    - 表示可能な文字列が含まれている場合は、「text」、実行可能なプログラムの場合は「executable」が表示される。その他の場合は「data」が表示され、スクリプトである場合は、インタプリンタ名とスクリプトであることが表示される。
  - stat
    - ファイルやファイルシステムの状態を出力する。
    - ls よりも多い情報が出るイメージ?
  - ln [オプション] 対象 リンク名/ディレクトリ名
    - ファイルへのリンクを作成する。ハードリンクまたはシンボリックリンク。
    - 「-f」すでにリンクがあった場合は削除する。
    - 「-i」すでにリンクがあった場合は問い合わせて削除する。
    - 「-L」対象がシンボリックリンクであった場合は、リンクをたどる。
    - 「-s」シンボリックリンクを作成する。（つけない場合はハードリンク）
    - 「--backup」移動先に同じファイルがある場合のバックアップ方法を指定する。
  - ll の権限の隣の数字はノード数を表す。
  - readlink
    - シンボリックリンク先を表示する。
  - chmod
    - ファイルやディレクトリのアクセス権限を変更する。
  - キャラクタデバイス: ランダムアクセスできないファイル?
  - sh ファイルは、実行権(x)がある場合は、ファイル名だけで実行できる。ない場合には bash をつけて実行できる。
  - chown
    - ファイル所有権やグループ所有権を変更する。
  - 所有者
    - ファイルやディレクトリを作成すると、作成したユーザがその所有者となる。ユーザが属するグループが所有グループとなる。
    - 所有者であればパーミッションを変えられる。
    - -rw-r--r--  1 miyatani root       38 Aug 12 22:36 test.txt などの３列目に書いてあるのが所有者、次が所有グループ。
  - chgrp
    - ファイルのグループ所有権を変更する。 
  - lsattr
    - ext2/ext3/ext4 ファイルシステム上の(拡張)ファイル属性を表示する。
    - ファイルシステムとは、OS がファイルを管理する仕組み。
      - linux においては、外付けのUSBなども含めてすべてをファイルとして扱う。
      - 単なるデータの塊を整理、管理する。
    - linux においては ext というファイルシステムを使用しており、現在は ext4 が主流。
    - 拡張ファイル属性は、読み取り書き込み実行以外のファイルにつく属性。\
      参考: https://qiita.com/yasushi-jp/items/4a8c8c54ef24ab74df11
      |属性|説明|
      |--|--|
      |a|追記のみ可能とする|
      |c|ファイルを圧縮する|
      |d|dump の対象外とする|
      |e|拡張フォーマットを使用する|
      |i|変更できなくする|
      |j|データのジャーナリングを行う|
      |s|安全な削除(データブロック内を消去)|
      |t|末尾のマージをできなくする|
      |u|削除できなくする|
      |A|atime(アクセス時刻)を更新しない|
      |D|ディレクトリを同期的に更新する|
      |S|同期的に更新する|
  - chattr
    - ext2/ext3/ext4 ファイルシステム上のファイル属性を変更する。
  - umask
    - ファイル作成時に所有権のマスク値を変更する。
      - 新しくファイルを作成した際の権限の有無に関するマスク値。
  - find
    - 条件を絞ってファイルを検索する。 
  - xargs
    - 入力を引数にしてコマンドを実行する。
    - 空白もしくは改行で区切られた文字列を標準入力から読み、1行ずつコマンドに引数として渡して実行する。
    - コマンドを指定しない場合は、echo コマンドに送られる。
  - 最後の改行文字を削る場合は「truncate -s -1 ファイル名」とすればいい。
  - which
    - コマンドのフルパスを表示する。
  - locate
    - ファイル名データベースからパターンに合ったパスを出力する。
  - basename
    - ファイルパスからファイル名のみを表示する。
    - basename path 拡張子 で拡張子を除いたファイル名を表示する。
  - dirname
    - ファイルパスからファイル名を除去して表示する。
  - truncate
    - ファイルを指定したサイズに切り詰める/拡張する
  - md5sum/sha1sum
    - ハッシュ値を出力及び検証。
  - uuencode/uudecode
    - バイナリファイルをテキストファイルに変換/復元する
  - base64
    - 入力を Base64 エンコード/デコードして出力する。
    - Base64 は A~Z、a~z、0~9 の文字と、「+」と「/」と「=」でデータを表現する文字列。
      - メールでバイナリデータを転送する目的で使用される。
  - tar [ファンクション][オプション] アーカイブ [ファイル名|ディレクトリ名]
    - tar で作成されるアーカイブは一般的に「tar玉」「tarball」と呼ばれる。
    - 基本は c で作り、x で展開する。そのほかにオプションがつく。
    - tar は圧縮していない。gzip の z 指定で圧縮する。
    - f で使用するアーカイブを指定する。
    - t で固めたファイル名を表示。
  - gzip / gunzip
    - 指定したファイルを Lempel-Ziv コーディング(LZ77) を利用して圧縮する。
    - ファイルを複数与えた場合は、個別に圧縮する。まとめて圧縮する場合は tar をつかってまとめてから圧縮する。
  - bzip2/bunzip2
    - Burrows-Wheeler ブロックソートテキスト圧縮アルゴリズムを利用してファイルを圧縮する。LZ77 よりも効率がいい。
  - mkdir
    - -p でディレクトリの中にディレクトリを作成できる。
  - zip
    - UnizやWindows、Mac OS X など複数のプラットフォームで利用できるPKZIP 互換圧縮アーカイブを処理できる。
  - unzip
    - -l オプションで zip の中のファイルをリストで表示できる。
  - lhasa
    - LHA 形式アーカイブを展開する。
    - LHA は MS-DOS で刃具ぐまれた日本育ちの圧縮形式。
  - unrar
    - RAR 形式アーカイブを展開する。
    - RAR 圧縮形式は zip 圧縮形式よりも圧縮率が高い。
  - cpio
    - アーカイブへコピーする/アーカイブからコピーする
    - cpio 形式アーカイブを操作する。
    - cpio 形式は UNIX 標準のファイルアーカイブで、圧縮は行わない。copy in and out の略。
  - pushd/popd/dirs
    - ディレクトリをスタックに追加/削除/表示する。
    - bash で用意されているディレクトリスタックに作業ディレクトリを追加/削除/表示する。
    - pushd でディレクトリスタックをスタックに追加、並び順を変更して移動。
    - popd でスタックしたディレクトリに移動/削除。
    - dirs でスタックを表示/削除する。
  - mktemp
    - 一時ファイル/ディレクトリを作成する。
  - convmv
    - ファイル名の文字コードを変換する。
  - rpm
    - RPM パッケージのインストールやアンインストール/アップデート/検索/検証を行う。
    - RPM パッケージには2種類あり、ひとつは実行ファイルが収められ、「.x86_64.rpm」のように、ファイル名の末尾にアーキテクチャ名と.rpmの拡張子が付いたRPMパッケージである。もうひとつは「.src.rpm」という拡張子のソースファイルだけが含まれるRPMパッケージである。
    - Red Had 系ディストリビューションは、RPMでシステムのファイルを管理している。
  - rpm2cpio
    - RPM パッケージ形式からcpioファイル形式に変換する。
  - yum
    - 依存関係を含めてRPMパッケージを管理する。
  - dpkg
    - deb パッケージを管理する。
    - Debian 用パッケージ(.deb)のインストール/アンインストール/ビルド/パッケージリスト参照などを行う。
  - apt-cache
    - パッケージのメタデータを処理して必要な情報を出力するコマンド。
  - aptitude
    - debパッケージを管理するテキストベースのインターフェイスを提供する。
    - 利用できるパッケージの一覧や、deb パッケージのインストール/アップデート/アンインストールの機能を持つ。
  - apt-get
    - apt は deb パッケージを管理するためのライブラリ/ツール。apt-get はapt ライブラリを利用してパッケージを管理するためのフロントエンドのひとつ。
    - HTTP/FTP などを利用して、ネットワーク経由で deb パッケージのダウンロード/インストール/アンインストールなどを行う。
    - 依存関係のあるパッケージも含めて処理できる。
    - apt のパッケージの取得元情報源は /etc/apt/sources.list 等に記載されている「apt-line」と呼ばれる URL から取得するメタデータ。
    - ダウンロードした dev ファイルは、 /var/cache/apt/archives にインストール後も保存される。保存されることで後で再インストールする際に再利用できる。 
    - deb ファイルが必要ない場合は、 apt-get clean で削除する。
    - update で リストを更新して、upgrade で更新したリストをもとにパッケージを最新版に更新する。
  - alien
    - パッケージ形式を相互に変換する。
    - 扱えるパッケージ形式は、Red Hat 系のRPMパッケージ、Debian系のdeb パッケージ、Slackware 系の tgz、Solaris の pkg である。

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
  - systeminfo | find "システム起動時間" で起動してからの時間が分かる。
# tex
  - 数式の前後は半角スペース一時開けないとgithub上では数式として表示されない。


# world
  - 光の混ざり具合考慮するため、mainカラーを全体の光に調節するといい見た目になる。
  - F2はrename
  - ワールドのバックアップには、Turbo Backup Proを買う！(次回新作作成時)

# blender
  - ver 3.6 においては、RGB分離は、カラー分離に統合されて、内部の選択欄でRGBかHSV等が選択できる。

# thought
  - 月を看（み）るは、清気（せいき）を観（み）るなり。円欠晴翳（えんけつせいえい）の間に在らず。
  花を看るは、生意を観るなり。紅柴香臭（こうしこうしゅう）の外（ほか）に存（そん）す。
    - 佐藤一斎　「言志四録」

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

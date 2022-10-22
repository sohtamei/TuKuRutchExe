# TuKuRutch EXE

つくるっちのFWとscratch拡張を自動生成する環境です。
従来zipファイルやインストラーで配布していましたが、更新を頻繁に行うため環境ごとgithubに移行してみました。
普段からArduino ESP32環境を使ってる方向けです。

## clone/download方法

TuKuRutchEXEは頻繁に更新するため、なるべくgit cloneを使って下さい。

* git cloneする場合  
  git clone --recursive https://github.com/sohtamei/TuKuRutchExe.git  
  TortoiseGit でcloneする際は Recursive をチェックして下さい。  

* zipダウンロードする場合  
  このレポジトリ https://github.com/sohtamei/TuKuRutchExe と https://github.com/sohtamei/TuKuRutch.ext をダウンロード&zip展開、  
  TuKuRutch.ext-masterをextにリネームしてTuKuRutchExe-masterの下に移動してください。  

## ArduinoIDE環境setup

現在のTuKuRutchEXEのArduino-IDE環境はArduino-ESP32 2.0.4、board manager - ESP32 Dev Module固定です。  
Arudino-ESP32不具合対策など個別に修正を行っているため、エラーが出る場合は後者のつくるっち用ArduinoIDEを使用して下さい。

* 現在お使いのArduinoIDEを使う場合  
  TuKuRutchExeフォルダ下にあるanalogRemote.zip、TukurutchEsp.zip、TukurutchEspCamera.zipをArduinoIDEで「zip形式のライブラリをインストール」して下さい。  
  自動生成された .inoファイルはTuKuRutchExe/ext/libraries/xxに生成されます。

* つくるっち用ArduinoIDEを使う場合  
  TuKuRutchEXE を C:￥ や C:￥work など10文字以下のパスのところにおいて下さい。  
  Windowsではファイルのパス長さが260文字以下という制限があるのですが、Arduino-ESP32に含まれるパスの長さが200文字以上あるためです。  
  https://sohta02.sakura.ne.jp/release/Arduino.20221022.zip を展開し、中のArduinoフォルダをTuKuRutchEXEに移動して下さい。zip展開に30分くらいかかります。  

## TuKuRutch.exe使い方

* マイコン選択  
  ![image](https://user-images.githubusercontent.com/43091864/197347045-65e144c9-3a08-4418-97dd-648ac732246c.png)

* 「モニタプログラムを開く」を選択、つくるっち用ArduinoIDEを使っている場合はArduinoIDEが開きます。  
  使ってない場合は TuKuRutchExe/ext/libraries/xx/src/src.inoをお使いのArduinoIDEで開いて下さい。  

* ArduinoIDEでプログラム書き込み後はTuKuRutch.exe、つくるっちアプリどちらからでもブロックを実行することができます。
  参考：http://sohta02.web.fc2.com/remoconrobo_program1.html

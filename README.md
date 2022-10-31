# TuKuRutch EXE

つくるっちのFWとscratch拡張を自動生成する環境です。  
従来zipファイルやインストラーで配布していましたが、更新を頻繁に行うため環境ごとgithubに移行してみました。  
普段からArduino ESP32環境を使ってる方向けです。

## clone/download方法

TuKuRutchEXEは頻繁に更新するため、なるべくgit cloneを使って下さい。

* git cloneする場合  
```
git clone --recursive https://github.com/sohtamei/TuKuRutchExe.git
```  
　TortoiseGitでcloneする際は Recursive をチェックして下さい。  

* git cloneした環境の更新方法  
```
git pull
git submodule update
```  
　TortoiseGitの場合はPullとsubmodule update。  
　TuKuRutch EXEはソースの自動生成を行うため、よくconflictが発生します。  
　確認の上conflictが発生したファイルをrevertして下さい。

* zipダウンロードする場合  

　このレポジトリ https://github.com/sohtamei/TuKuRutchExe と https://github.com/sohtamei/TuKuRutch.ext をダウンロード&zip展開、  
　TuKuRutch.ext-masterをextにリネームしてTuKuRutchExe-masterの下に移動してください。  

## ArduinoIDE環境setup

現在のTuKuRutchEXEの対応Arduino-IDE環境は下記の通りです。  

* Atmega328  
* Arduino-ESP32 2.0.4 
* raspberryPI pico  

Arudino-ESP32不具合対策など個別に修正を行っているため、buildでエラーが出る場合は後者のつくるっち用ArduinoIDEを使用して下さい。

* 現在お使いのArduinoIDEを使う場合  
  TuKuRutchExeフォルダ下にあるanalogRemote.zip、TukurutchEsp.zip、TukurutchEspCamera.zipをArduinoIDEで「zip形式のライブラリをインストール」して下さい。  

* つくるっち用ArduinoIDEを使う場合  
  TuKuRutchEXE を C:￥ や C:￥work など10文字以下のパスのところに移動して下さい。Windowsではファイルのパス長さが260文字以下という制限があるのですが、Arduino-ESP32に含まれるパスの長さが200文字以上あるためです。TuKuRutchEXEフォルダで https://sohta02.sakura.ne.jp/release/Arduino.20221022.zip を展開し、中のArduinoフォルダをTuKuRutchEXE直下に移動して下さい。zip展開に30分くらいかかります。  

## TuKuRutch.exe使い方

* マイコン選択  
  ![image](https://user-images.githubusercontent.com/43091864/197347045-65e144c9-3a08-4418-97dd-648ac732246c.png)

* 「モニタプログラムを開く」を選択、つくるっち用ArduinoIDEを使っている場合はArduinoIDEが開きます。  
  つくるっち用ArduinoIDE以外を使ってる場合は TuKuRutchExe/ext/libraries/xx/src/src.inoをお使いのArduinoIDEで開いて下さい。  

* ArduinoIDEでプログラム書き込み後はTuKuRutch.exe、つくるっちアプリどちらからでもブロックを実行することができます。  
  参考：http://sohta02.web.fc2.com/remoconrobo_program1.html  

* adobe AIRのエラーが出るとき  
  TuKuRutchEXEフォルダのAdobeAIRInstaller.exeを実行して下さい。

## robot.json編集方法

　TuKuRutchEXEはrobot.jsonからsrc.inoとscratch3.0拡張を自動生成します。記述方法は下記ページを参照して下さい。  
　http://sohta02.web.fc2.com/familyday_extension.html#prepare  

# pdfGUI
pdfの結合，分割ができるpythonGUI(Tkinter)
# 動作条件
Windows10

Mac OS

Ubuntu(だぶん) ※動作未確認
# 実行方法
python3で動作しています．必要なライブラリはPyPDF2だけです．
```
pip install PyPDF2
```
もしくは
```
pip install -r requirements.txt
```
実行方法は該当ディレクトリに移動し
```
python pdf_gui.py
```
これでGUIが起動する．
<div align="center">
<img width="1412" alt="gui" src="https://user-images.githubusercontent.com/118164921/216750822-6e194a07-8b29-44f6-be16-ea942ea0c823.png" title="Windows">
Windowsでの画面
</div>
<br>
<div align="center">
<img width="1412" alt="gui" src="https://user-images.githubusercontent.com/118164921/216751084-27285c0c-5bb2-47ce-813f-7a1ec31b72f9.png" title="Mac">
Macでの画面
</div>
<br>

また実行ファイルを生成する場合は，

```
python generate_exe.py
```

と入力するとdistというディレクトリに実行ファイルが生成される．
# できること
* pdfの結合 
* pdfの分割 

どちらの機能もページ範囲の指定により，その範囲のみの結合，分割が可能.


## pdfの結合
* 右のボタンで「追加」と押しTreeviewにpdfファイルを追加
* ファイルを選択し結合をクリック
* 好きな場所に保存
  
   ページ範囲を指定していると，範囲ページのみが結合対象となる．
## pdf分割
* ページ範囲を指定していない場合  
  1. ファイルを追加
  2. ファイルを選択し下のボタンのpdf分割をクリック
  3. 好きな場所に保存
   ファイルは1ページごとに分割されます．
* ページ範囲を指定している場合  
  1.  ページ範囲のボタンをクリックし最小，最大ページを設定
  2.  Treeviewに表示されていることを確認した後，分割したいpdfをクリック
  3.  好きな場所に保存
   
   ページ範囲が指定されているファイルは，範囲内と範囲外の2ファイルが分割されます．

また，Treeviewにある選択ファイルをダブルクリックすると，そのPDFファイルを開くことができます．
# 注意点
* 重いファイルを開くとTreeviewに表示されるまで時間がかかるときがある．
* 分割する際，ページ範囲をしていしていないとすべてのページが分割されるので，ページ数が多いとたくさんのファイルが生成されます．例えば，100ページあると100枚のpdfが作成されます．
* 動作としてMacとWindows10は確認しているが，Ubuntu等Linuxは動作確認をしていない．
* だいぶ前にpython初心者が書いたコードなので，とっても汚い．自分でも何書いているのかわからない(笑)．でもとりあえず動く．
* 変なテンションで書いたため， エラーメッセージが変．あまり気にしないでください．(たぶん修正します)
* デザインがダサい．Tkinterなので仕方ない部分はあるのか?
* tkinterのバージョンによってはエラーになるかも? 色の設定でエラーになりましたが修正済みです．
# 参考
CubePDF Pageはレイアウトなどを参考にしました．リンクを載せておきます．

https://www.cube-soft.jp/cubepdfpage/



    
---
layout: post
title: freeglut × Bash on Windows x Xming
category: Development
comments: true
tag:
 - glut
 - linux
---

## 初めに

講義でfreeglutを使うということでPCに入れとけと言われたのですが，

Windows上の環境を壊したくなかったのでBashでやることにしました．

他にこんなことやる人いないと思うけどやったことをここに残しておきます．

こんな記事を見る人は多分Bash on Windowsは導入済みということで導入後からの話をしたいと思います

## お品書き
* freeglutのインストール
* Xmingの導入
* お好みで設定するやつら


## freeglutのインストール

glutといったらここにたどり着くであろう,以下のサイトの導入手順通りにやることにした．

[GLUTによる「手抜き」OpenGL入門](https://tokoik.github.io/opengl/libglut.html)

以下のコマンドを叩きます.

```bash
$ sudo apt-get update
$ sudo apt-get install -y freeglut3 freeglut3-dev
```

これでfreeglutのインストールが完了です.

## Xmingの準備

WindowsにXmingを導入します.

現状のbash on WindowsではGUIが使えません．ということはGLUTで書いたプログラムを走らせてもエラーが出ます．

だからGUIを見れるようにします．

[**公式サイト**](https://ja.osdn.net/projects/sfnet_xming/)からXming X Server for Windowsをダウンロード．

* Xming-6-9-0-31-setup.exe
* Xming-fonts-7-7-0-10-setup.exe

ダウンロードしたファイルをインストールし，Xmingを起動する．

さらにBash上で以下のコマンドを入力してGUIを使えるようにします.

```
sudo apt-get insall x11-apps
```

## bashの設定

ステータスバーのXmingにマウスカーソルを乗せると

```
Xming server:0.0
```

のようになっているはずなので，bash上で以下のコマンドを入力します．

```
export DISPLAY=localhost:0.0
```

最後の0.0は上で確認した．Xming server:○.○の〇.〇の値を入力します.

設定できているはずなのでxeyesで動作確認をします.

‘‘‘
xeyes &
‘‘‘

とりあえずこれで設定が完了しました.

## お好みで設定するやつら

#### bashを起動する毎にDISPLAYの設定をする

起動時に毎回Display設定をするのが面倒だから以下のコマンドを入力します.

```
echo export DISPLAY=localhost:0.0 >> ~/.bashrc
```

#### freeglutを使ったプログラムのコンパイルを改善する

コンパイル時にコマンドが長いので楽をするために以下のコマンドを入力する.

```
echo 'function ccgl() { cc -I/usr/X11R6/include "$@" -L/usr/X11R6/lib -lglut -lGLU -lGL -lXmu -lXi -lXext -lX11 -lm -lpthread; }' >> ~/.bashrc
```

これで以下コマンドでコンパイルできるようになります.

```
ccgl program.c
```

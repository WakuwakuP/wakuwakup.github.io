---
layout: post
title: Gitクライアントを探す
category: Development
comments: true
tag:
 - git
 - sublime
---

# なぜ今更Gitクライアントなのか

僕は今までgitクライアントといえば[SourceTree](https://www.atlassian.com/software/sourcetree)だった．  
よく使う機能は大体そろっている．しかし，高機能なため多少重い．  
個人で使う分には困らなかった． 
会社で規模の大きいプロジェクトとなると問題が出てくる．  

__「初期表示までに何分かかるの……?」__

支給されたWindows機でCUIは毎回`ls`を`dir`で叩き直すなどストレスマッハなのでGUIが欲しい．
たくさんあるGitクライアントからお気に入りを決めようと思う．

# Gitクライアント比較

今回比較するものは以下のとおり．

- [SourceTree](#sourcetree)
- [TortoiseGit](#tortoisegit)
- [GitHub Desktop](#github-desktop)
- [GitKraken](#gitkraken)
- [Fork](#fork)
- [Sublime Merge](#sublime-merge)

## 一言レビュー

### [SourceTree](https://www.atlassian.com/software/sourcetree)

#### good

今まで使っていたやつ  
慣れた操作  
使いやすい

#### bad

ちょっと重い

### [TortoiseGit](https://tortoisegit.org)

#### good

explorer上で右クリックでほぼ完結する

#### bad

僕がexplorer上で右クリックで使用しない

### [GitHub Desktop](https://desktop.github.com/)

#### good

Githubで使うなら連携が神

#### bad

Gitlabとの連携は皆無

### [GitKraken](https://www.gitkraken.com)

#### good

イカちゃん!!  
ドラッグしてマージはUXが良い  
GPG署名をGUIでしっかり対応している

#### bad

起動が重い  
デザイン凝りすぎて情報量がちょっと少ない

### [Fork](https://git-fork.com)

#### good

SourceTreeほど重くない  
Graphの曲線が可愛い

#### bad

見た目がSourceTreeに近いのでSourceTreeに操作が引っ張られて使いにくい

### [Sublime Merge](https://www.sublimemerge.com)

#### good

爆速  
困ったらコマンドパネル

#### bad

有料(買い切り 3年更新サポート)

## 比較

|クライアント|起動速度|使用時速度|デザイン|機能性|使いやすさ|
|:--|:-:|:-:|:-:|:-:|:-:|
|SourceTree|△|△|〇|◎|
|TortoiseGit|〇|〇|◎|△|
|GitHub Desktop|〇|〇|〇|〇|
|GitKraken|△|△|◎|〇|〇|
|Fork|〇|〇|〇|△|◎|
|Sublime Merge|◎|◎|〇|◎|

sublime textに惚れて購入している僕の評価なので，参考程度に見てほしい．

実際のところSublime Mergeも署名付きコミットはGPG4winでインストールしたGUIに頼ることになるので速くはないです．

# まとめ

僕は最終的にはSublime Mergeを購入し，ダークテーマで落ち着いた．  
Sublime Merge評価版は無料なので一回使ってみてほしい．

最後に一言．  
みんな好きなクライアント使えばいいと思うよ．

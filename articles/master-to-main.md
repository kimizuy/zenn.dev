---
title: 'git init したときのデフォルトブランチ名を master から変更する'
emoji: '✨'
type: 'tech' # tech: 技術記事 / idea: アイデア
topics: ['git']
published: true
---

7 月 27 日、Git v2.28.0 がリリースされました。このバージョンで`git init`したときのデフォルトブランチ名が「master」以外へ変更可能になったので、その手順を紹介します。

## デフォルトブランチ名を変更するコマンド

この例では「main」ブランチに名前を変更しています。

```git
git config --global init.defaultBranch main
```

## Git のバージョンを確認する

ただ v2.28 未満の場合は上記のコマンドは使えないので、まずバージョンを確認します。

```git
git --version
```

## Git のバージョンアップ

確認した結果、v2.28 未満であれば、Git のバージョンアップを行います。

Mac OS:

```bash
brew upgrade git
```

Windows:

```git
git update-git-for-windows
```

バージョンアップが完了したら、改めてデフォルトブランチ変更のコマンドを実行しましょう。

## 参考

[Highlights from Git 2.28](https://github.blog/2020-07-27-highlights-from-git-2-28/#introducing-init-defaultbranch)

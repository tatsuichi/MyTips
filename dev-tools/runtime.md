
# 言語ランタイム

言語ランタイムのバージョンを管理する`pyenv`、`nodenv`、`rbenv`などを一元管理する`anyenv`を利用する

## 実行環境

- WSL（Ubuntu）

## [anyenv](https://github.com/anyenv/anyenv)のインストール

``` sh
# anyenv を clone する
git clone https://github.com/anyenv/anyenv ~/.anyenv

# PATHを通す
echo 'export PATH="$HOME/.anyenv/bin:$PATH"' >> ~/.bashrc

# **envコマンド（pyenv / nodevn / rbenv など）を有効化
# ~/.anyenv/bin/anyenv init  # .bashrcに統一するため手動で書き込む
echo 'export eval "$(anyenv init -)"' >> ~/.bashrc

# インストールマニフェストディレクトリを初期化する
anyenv install --init
```

## [anyenv-update](https://github.com/znz/anyenv-update)のインストール

``` sh
# anyenv-update をインストールする
mkdir -p $(anyenv root)/plugins
git clone https://github.com/znz/anyenv-update.git $(anyenv root)/plugins/anyenv-update

# **env（pyenv / nodevn / rbenv など） を更新する
anyenv update
```

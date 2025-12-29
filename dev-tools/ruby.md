
# Ruby

## 実行環境

- WSL（Ubuntu）
- anyenv
- rbenv

## インストール手順

``` sh
# Ruby に必要なライブラリ
sudo apt install -y build-essential libssl-dev libreadline-dev zlib1g-dev libyaml-dev libffi-dev libgdbm-dev libncurses-dev libdb-dev uuid-dev autoconf bison

# rbenv のインストール
anyenv install rbenv
# rbenv のアップデート
anyenv update

# インストール可能なバージョンを一覧表示
rbenv install --list
# Ruby のインストール
rbenv install 3.4.8
rbenv global 3.4.8
rbenv local 3.4.8
```

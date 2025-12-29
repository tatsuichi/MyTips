
# 静的サイトジェネレータ

HTML生成ツール

## [Jekyll](https://jekyllrb.com/docs/installation/ubuntu/) のインストール

- GitHub Pagesに対応したツール
- 複数のテーマあり

### 実行環境

- WSL（Ubuntu）
- Ruby

### インストール手順

``` sh
sudo apt-get install ruby-full build-essential zlib1g-dev

echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc

gem install jekyll bundler
```

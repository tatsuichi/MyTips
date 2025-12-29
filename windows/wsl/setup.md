# WSL 基本設定

## 環境

- Windows 11
- WSL（Ubuntu）
- VS Code

## パッケージを最新にする

WSL（Ubuntu）で実行する

``` sh
sudo apt update && sudo apt upgrade
```

## VS Code から WSL を利用する


Windows の VS Code から WSL 環境を操作するために、以下の VS Code の拡張機能をインストールする

- [Remote Development](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack)


VS Code は Windows、実行環境は WSL（Ubuntu）

``` mermaid
graph TD
  subgraph Windows
    VSCode["VS Code<br/>(UI・操作)"]
    Remote["Remote Development"]

    VSCode --> Remote
  end

  subgraph WSL["WSL (Ubuntu)"]
    Tools["ターミナル<br/>言語ランタイム<br/>開発ツール"]
  end

  Remote --> Tools
  ```



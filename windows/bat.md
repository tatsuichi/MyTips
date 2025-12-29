# コマンドプロンプト

## 環境

- Windows 10

## 起動方法

1. Winキー + R
1. "cmd"と入力する
1. Enterキー 

または

1. Winキー
1. "コマンドプロンプト"と入力する
1. Enterキー

## バッチファイル

### バッチファイルの先頭に記載する定型文

おまじない

``` bat
@echo off
cd /d %~dp0
```

### バッチファイルを即時終了させない

バッチファイルの最後で入力待ちさせる

``` bat
pause
```

### コメント(アウト)

``` bat
rem コメント
```

### ログ出力

``` bat
[コマンド名] >> [ログファイル名] > 2>&1
```

### 変数に設定する

`=`の前後にスペースがないこと

``` bat
rem OK
set 変数=値
rem NG
set 変数 = 値
```

### 変数を扱う

`%`で括る

``` bat
echo %変数%
```

### 年月日時分秒

```bat
set year=%date:~0,4%
set month=%date:~5,2%
set day=%date:~8,2%
set hour=%time:~0,2%
set min=%time:~3,2%
set sec=%time:~6,2%

echo %year%
echo %month%
echo %day%
echo %hour%
echo %min%
echo %sec%
```

### 戻り値

``` bat
echo %ERRORLEVEL%

if %ERRORLEVEL% equ 0 (
    REM 正常処理
) else (
    REM 異常処理
)
```

## コマンド

``` bat
REM IPアドレス等の確認
ipconfig /all

REM ネットワークの疎通確認
ping IPアドレス

REM 自身のリッスン状態の確認
netstat -ano

REM 通信先のポートが開ているかの確認
ftp
> open IPアドレス ポート番号
・・・
> quit

REM DNSの確認
nslookup ホスト名/IPアドレス

REM ネットワーク経路の確認
tracert ホスト名/IPアドレス

REM HTTPリクエスト
curl -X "GET" "URL" -v | jq.exe

REM コマンドの結果をグレップする
コマンド | find "グレップする文字列"

REM 実行中のプロセス一覧
tasklist
```

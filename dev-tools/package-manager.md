# パッケージマネージャー

## 実行環境

- WSL（Ubuntu）

## [poetry](https://python-poetry.org/)

### 既存プロジェクトの更新手順

#### Pythonバージョンアップ手順

``` mermaid
flowchart TD
    update["pyproject.tomlのrequires-pythonを手動修正"] --> lock["poetry lock"]
    lock --> install["poetry install"]
```

#### パッケージバージョンアップ手順

1. 制約内バージョンアップ実施

   ``` sh
   poetry update
   ```

1. 直接依存のパッケージに対して、制約外バージョンアップ実施

   ``` sh
   poetry add
   ```

``` mermaid
flowchart TD
    show1["poetry show --outdated"] --> check1[更新対象のパッケージがあるか？]
    check1 -- no --> E["終了"]
    check1 -- yes --> update["poetry update"]
    update --> show2["poetry show --outdated"]
    show2 --> check2[更新対象のパッケージがあるか？]
    check2 -- no --> E["終了"]
    check2 -- yes --> show3["poetry show パッケージ"]
    show3--> check3[直接依存のパッケージか？]
    check3 -- no --> show2
    check3 -- yes --> add["poetry add パッケージ"]
    add　--> show2
```


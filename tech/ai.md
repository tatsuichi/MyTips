# AI

- 学習：モデルにデータを「教える」
- 推論：教わったことを「使う」

``` mermaid
flowchart LR
  AI["AI"]
  ML["機械学習（ML）<br/>(データから学習)"]
  SUP["教師あり学習<br/>(正解データあり)"]
  UNSUP["教師なし学習<br/>(正解データなし)"]
  RL["強化学習<br/>(試行と報酬を繰り返して学習)"]
  DL["深層学習<br/>(ニューラルネットワーク)"]
  LLM["大規模言語モデル（LLM）<br/>(人間のように自然な文章を理解・生成できるAIモデル)"]

  AI -->|部分領域| ML
  ML --> SUP
  ML --> UNSUP
  ML --> RL
  ML --> DL
  DL --> LLM
```

``` mermaid
flowchart LR
  MAIN["AI技術"]
  SUB1["生成AIサービス<br/>(AIを使う側)"]
  SUB2["コード生成に特化"]
  SUB3["AI支援"]
  SUB31["IDE"]
  SUB32["エディタ"]
  SUB4["機械学習サービスIDE<br/>(モデル開発など)"]
  SUB5["生成AIアプリ開発<br/>(アプリを作る側)"]
  SUB6["周辺技術"]
  ChatGPT["ChatGPT / OpenAI"]
  Gemini["Gemini / Google"]
  MSCopilot["Copilot / Microsoft"]
  Claude["Claude Code / Anthropic"]
  GHCopilot["GitHub Copilot / GitHub"]
  SageMaker["AWS SageMaker / AWS"]
  Bedrock["AWS Bedrock / AWS<br/>モデル選択可能"]
  Kiro["AWS Kiro / AWS<br/>仕様駆動開発"]
  Cursor["Cursor / 	Anysphere"]
  MCP["MCP / Anthropic"]

  MAIN --> SUB1
  MAIN --> SUB3
  MAIN --> SUB4
  MAIN --> SUB5
  MAIN --> SUB6

  SUB1 --> ChatGPT
  SUB1 --> Gemini
  SUB1 --> MSCopilot
  SUB1 --> SUB2
  SUB2 --> Claude
  SUB2 --> GHCopilot

  SUB3 --> SUB31
  SUB3 --> SUB32
  SUB31 --> Kiro
  SUB32 --> Cursor

  SUB4 --> SageMaker
  SUB5 --> Bedrock
  SUB6 --> MCP
```

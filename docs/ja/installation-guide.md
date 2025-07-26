# SuperClaude インストールガイド 📦

## 🎯 見た目より簡単です！

**正直に言うと**：このガイドは長く見えるかもしれませんが、それはすべての詳細をカバーしたいからです。実際のインストールはとても簡単で、ほとんどの人は1つのコマンドで2分以内に完了します！

### ステップ 1：パッケージのインストール

**オプション A：PyPI から（推奨）**
```bash
uv add SuperClaude
```

**オプション B：ソースから**
```bash
git clone https://github.com/NomenAK/SuperClaude.git
cd SuperClaude
uv sync
```

### 🔧 UV / UVX セットアップガイド

SuperClaude v3 は [`uv`](https://github.com/astral-sh/uv)（より高速でモダンな Python パッケージマネージャー）または `uvx` を使用したクロスプラットフォームインストールもサポートしています。

### 🌀 `uv` を使用したインストール

まず `uv` がインストールされていることを確認してください：

```bash
curl -Ls https://astral.sh/uv/install.sh | sh
```

> または以下の手順に従ってください：[https://github.com/astral-sh/uv](https://github.com/astral-sh/uv)

`uv` が利用可能になったら、以下のように SuperClaude をインストールできます：

```bash
uv venv
source .venv/bin/activate
uv pip install SuperClaude
```

### ⚡ `uvx` を使用したインストール（クロスプラットフォーム CLI）

`uvx` を使用している場合は、次を実行するだけです：

```bash
uvx pip install SuperClaude
```

### ✅ インストールの完了

インストール後、通常のインストーラーステップを続行します：

```bash
python3 -m SuperClaude install
```

または bash スタイルの CLI を使用：

```bash
SuperClaude install
```

### 🧠 注意事項：

* `uv` はより良いキャッシングとパフォーマンスを提供します
* Python 3.8+ と互換性があり、SuperClaude とスムーズに動作します

---

### ⚠️ 重要な注意
**SuperClaude をインストールした後、**
**`SuperClaude commands`、`python3 -m SuperClaude commands`、または `python3 SuperClaude commands` を使用できます**

**何が起こったのか？** SuperClaude は必要なものすべてをセットアップしようとしました。通常、複雑な設定や依存関係の探索、セットアップの悩みは不要です！🎉

---

SuperClaude v3 の包括的なインストールガイドです。ただし、ほとんどの人は上記のクイックスタート以外を読む必要はありません！😊

## 始める前に 🔍

### 必要なもの 💻

SuperClaude は **Windows**、**macOS**、**Linux** で動作します。必要なものは以下の通りです：

**必須：**
- **Python 3.8 以降** - フレームワークは Python で書かれています
- **Claude CLI** - SuperClaude は Claude Code を強化するので、先にインストールする必要があります

**オプション（推奨）：**
- **Node.js 16+** - MCP サーバー統合が必要な場合のみ
- **Git** - 開発ワークフローに便利

### クイックチェック 🔍

インストール前に、基本的な要件を確認しましょう：

```bash
# Python バージョンをチェック（3.8+ である必要があります）
python3 --version

# Claude CLI がインストールされているかチェック
claude --version

# Node.js をチェック（オプション、MCP サーバー用）
node --version
```

いずれかが失敗した場合は、下記の[前提条件のセットアップ](#前提条件のセットアップ-🛠️)セクションを参照してください。

## クイックスタート 🚀

**🏆「とにかく動かしたい」アプローチ（90%のユーザーに推奨）**

**オプション A：PyPI から（推奨）**
```bash
pip install SuperClaude

# 推奨設定でインストール
SuperClaude install --quick

# 完了です！🎉
```

**オプション B：ソースから**
```bash
# リポジトリをクローン
git clone <repository-url>
cd SuperClaude
pip install .

# 推奨設定でインストール
SuperClaude install --quick

# 完了です！🎉
```

**⚠️ 重要な注意**
**SuperClaude をインストールした後、**
**`SuperClaude commands`、`python3 -m SuperClaude commands`、または `python3 SuperClaude commands` を使用できます**

**インストールで得られたもの：**
- ✅ エキスパートを自動的に有効化する 16 個のスマートコマンド
- ✅ いつヘルプするかを知っている 11 個の専門家ペルソナ
- ✅ 複雑さを自動的に判断するインテリジェントルーティング
- ✅ 約 2 分の時間と ~50MB のディスクスペース

**本当に、これで完了です。** Claude Code を開き、`/help` と入力して、SuperClaude の魔法を見てください。

**何をするか心配ですか？** まず確認してみてください：
```bash
SuperClaude install --quick --dry-run
```

## インストールオプション 🎯

3つのインストールプロファイルから選択できます：

### 🎯 最小インストール
```bash
SuperClaude install --minimal
```
- **内容**：コアフレームワークファイルのみ
- **時間**：~1 分
- **容量**：~20MB
- **適している用途**：テスト、基本的な拡張、最小設定
- **含まれるもの**：Claude を導くコア動作ドキュメント

### 🚀 クイックインストール（推奨）
```bash
SuperClaude install --quick
```
- **内容**：コアフレームワーク + 16 個のスラッシュコマンド
- **時間**：~2 分
- **容量**：~50MB
- **適している用途**：ほとんどのユーザー、一般的な開発
- **含まれるもの**：最小インストールのすべて + `/analyze`、`/build`、`/improve` などの専門コマンド

### 🔧 開発者インストール
```bash
SuperClaude install --profile developer
```
- **内容**：MCP サーバー統合を含むすべて
- **時間**：~5 分
- **容量**：~100MB
- **適している用途**：パワーユーザー、コントリビューター、高度なワークフロー
- **含まれるもの**：すべて + Context7、Sequential、Magic、Playwright サーバー

### 🎛️ インタラクティブインストール
```bash
SuperClaude install
```
- コンポーネントを選択できます
- 各コンポーネントの詳細な説明を表示
- インストール内容を制御したい場合に適しています

## ステップバイステップインストール 📋

### 前提条件のセットアップ 🛠️

**Python がない場合？**
```bash
# Linux (Ubuntu/Debian)
sudo apt update && sudo apt install python3 python3-pip

# macOS
brew install python3

# Windows
# https://python.org/downloads/ からダウンロード
# またはコマンドプロンプトか PowerShell を開く
winget install python
```

**Claude CLI がない場合？**
- https://claude.ai/code でインストール手順を確認
- SuperClaude は Claude Code を強化するので、先にインストールが必要です

**Node.js がない場合？（オプション）**
```bash
# Linux (Ubuntu/Debian)
sudo apt update && sudo apt install nodejs npm

# macOS
brew install node

# Windows
# https://nodejs.org/ からダウンロード
# またはコマンドプロンプトか PowerShell を開く
winget install nodejs
```

### SuperClaude の取得 📥

**オプション 1：PyPI から（推奨）**
```bash
pip install SuperClaude
```

**オプション 2：最新リリースをダウンロード**
```bash
# 最新リリースをダウンロードして展開
# （URL を実際のリリース URL に置き換えてください）
curl -L <release-url> -o superclaude-v3.zip
unzip superclaude-v3.zip
cd superclaude-v3
pip install .
```

**オプション 3：Git からクローン**
```bash
git clone <repository-url>
cd SuperClaude
pip install .
```

### インストーラーの実行 🎬

インストーラーは賢く、プロセスをガイドしてくれます：

```bash
# 利用可能なすべてのオプションを確認
SuperClaude install --help

# クイックインストール（推奨）
SuperClaude install --quick

# 最初に何が起こるか確認したい場合
SuperClaude install --quick --dry-run

# すべてをインストール
SuperClaude install --profile developer

# 静かなインストール（最小出力）
SuperClaude install --quick --quiet

# 強制インストール（確認をスキップ）
python3 SuperClaude.py install --quick --force
```

### インストール中 📱

インストール時に起こることは以下の通りです：

1. **システムチェック** - 必要な依存関係を確認
2. **ディレクトリセットアップ** - `~/.claude/` ディレクトリ構造を作成
3. **コアファイル** - フレームワークドキュメントファイルをコピー
4. **コマンド** - スラッシュコマンド定義をインストール（選択した場合）
5. **MCP サーバー** - MCP サーバーをダウンロードして設定（選択した場合）
6. **設定** - お好みで `settings.json` をセットアップ
7. **検証** - すべてが動作することをテスト

インストーラーは進行状況を表示し、問題がある場合はお知らせします。

## インストール後 ✅

### クイックテスト 🧪

すべてが正常に動作していることを確認しましょう：

```bash
# ファイルがインストールされたかチェック
ls ~/.claude/

# CLAUDE.md、COMMANDS.md、settings.json などが表示されるはずです
```

**Claude Code でテスト：**
1. Claude Code を開く
2. `/help` と入力してみる - SuperClaude コマンドが表示されるはずです
3. `/analyze --help` を試す - コマンドオプションが表示されるはずです

### インストールされたもの 📂

SuperClaude はデフォルトで `~/.claude/` にインストールされます。見つかるものは以下の通りです：

```
~/.claude/
├── CLAUDE.md              # メインフレームワークエントリーポイント
├── COMMANDS.md            # 利用可能なスラッシュコマンド
├── FLAGS.md               # コマンドフラグとオプション
├── PERSONAS.md            # スマートペルソナシステム
├── PRINCIPLES.md          # 開発原則
├── RULES.md               # 操作ルール
├── MCP.md                 # MCP サーバー統合
├── MODES.md               # 操作モード
├── ORCHESTRATOR.md        # インテリジェントルーティング
├── settings.json          # 設定ファイル
└── commands/              # 個別のコマンド定義
    ├── analyze.md
    ├── build.md
    ├── improve.md
    └── ... （他に 13 個）
```

**各ファイルの役割：**
- **CLAUDE.md** - Claude Code に SuperClaude について伝え、他のファイルをロード
- **settings.json** - 設定（MCP サーバー、フックなど）
- **commands/** - 各スラッシュコマンドの詳細な定義

### 最初のステップ 🎯

始めるためにこれらのコマンドを試してください：

```bash
# Claude Code で、これらを試してください：
/sc:help                    # 利用可能なコマンドを確認
/sc:analyze README.md       # ファイルを分析
/sc:build --help           # ビルドオプションを確認
/sc:improve --help         # 改善オプションを確認
```

**圧倒されても心配しないでください** - SuperClaude は Claude Code を徐々に強化します。必要なだけ使用できます。

## インストールの管理 🛠️

### アップデート 📅

SuperClaude を最新に保つ：

```bash
# アップデートをチェック
SuperClaude update

# 強制アップデート（ローカルの変更を上書き）
SuperClaude update --force

# 特定のコンポーネントのみアップデート
SuperClaude update --components core,commands

# 何がアップデートされるか確認
SuperClaude update --dry-run
```

**いつアップデートするか：**
- 新しい SuperClaude バージョンがリリースされたとき
- 問題がある場合（アップデートには修正が含まれることが多い）
- 新しい MCP サーバーが利用可能になったとき

### バックアップ 💾

大きな変更の前にバックアップを作成：

```bash
# バックアップを作成
SuperClaude backup --create

# 既存のバックアップをリスト
SuperClaude backup --list

# バックアップから復元
SuperClaude backup --restore

# カスタム名でバックアップを作成
SuperClaude backup --create --name "before-update"
```

**いつバックアップするか：**
- SuperClaude をアップデートする前
- 設定を実験する前
- アンインストールする前
- 大幅にカスタマイズした場合は定期的に

### アンインストール 🗑️

SuperClaude を削除する必要がある場合：

```bash
# SuperClaude を削除（バックアップは保持）
SuperClaude uninstall

# 完全に削除（すべてを削除）
SuperClaude uninstall --complete

# 何が削除されるか確認
SuperClaude uninstall --dry-run
```

**削除されるもの：**
- `~/.claude/` 内のすべてのファイル
- MCP サーバー設定
- Claude Code 内の SuperClaude 設定

**残るもの：**
- バックアップ（`--complete` を使用しない限り）
- Claude Code 自体（SuperClaude は触れません）
- プロジェクトとその他のファイル

## トラブルシューティング 🔧

### よくある問題 🚨

**「Python が見つかりません」**
```bash
# python3 の代わりに python を試す
python --version

# またはインストールされているが PATH にない場合
which python3
```

**「Claude CLI が見つかりません」**
- Claude Code が先にインストールされていることを確認
- `claude --version` で確認
- https://claude.ai/code でインストールヘルプを参照

**「権限が拒否されました」**
```bash
# 明示的な Python パスで試す
/usr/bin/python3 SuperClaude.py install --quick

# または異なる権限が必要かチェック
ls -la ~/.claude/
```

**「MCP サーバーがインストールできません」**
- Node.js がインストールされているかチェック：`node --version`
- npm が利用可能かチェック：`npm --version`
- まず MCP なしでインストールを試す：`--minimal` または `--quick`

**「インストールが途中で失敗します」**
```bash
# 詳細出力で何が起こっているか確認
SuperClaude install --quick --verbose

# またはドライランを先に試す
SuperClaude install --quick --dry-run
```

### プラットフォーム固有の問題 🖥️

**Windows：**
- 「コマンドが見つかりません」の場合は `python3` の代わりに `python` を使用
- 権限エラーの場合は管理者としてコマンドプロンプトを実行
- Python が PATH にあることを確認

**macOS：**
- セキュリティとプライバシー設定で SuperClaude を承認する必要があるかも
- Python 3.8+ がない場合は `brew install python3` を使用
- `python` の代わりに明示的に `python3` を使用してみる

**Linux：**
- `python3-pip` がインストールされていることを確認
- 一部のパッケージインストールには `sudo` が必要かも
- `~/.local/bin` が PATH にあることを確認

### まだ問題がありますか？🤔

**トラブルシューティングリソースをチェック：**
- GitHub Issues：https://github.com/NomenAK/SuperClaude/issues
- 類似の既存の問題を探す
- 解決策が見つからない場合は新しい問題を作成

**バグを報告する際は以下を含めてください：**
- オペレーティングシステムとバージョン
- Python バージョン（`python3 --version`）
- Claude CLI バージョン（`claude --version`）
- 実行したコマンド
- 完全なエラーメッセージ
- 期待した動作

**ヘルプを得る：**
- 一般的な質問は GitHub Discussions
- 最新のアップデートは README.md をチェック
- 既知の問題は ROADMAP.md を参照

## 高度なオプション ⚙️

### カスタムインストールディレクトリ

```bash
# カスタム場所にインストール
SuperClaude install --quick --install-dir /custom/path

# 環境変数を使用
export SUPERCLAUDE_DIR=/custom/path
SuperClaude install --quick
```

### コンポーネント選択

```bash
# 利用可能なコンポーネントを確認
SuperClaude install --list-components

# 特定のコンポーネントのみインストール
SuperClaude install --components core,commands

# 特定のコンポーネントをスキップ
SuperClaude install --quick --skip mcp
```

### 開発セットアップ

SuperClaude に貢献または変更を計画している場合：

```bash
# すべてのコンポーネントを含む開発者インストール
SuperClaude install --profile developer

# 開発モードでインストール（コピーの代わりにシンボリックリンク）
SuperClaude install --profile developer --dev-mode

# 開発用の git フックをインストール
SuperClaude install --profile developer --dev-hooks
```

## 次は何？🚀

**SuperClaude がインストールされました（簡単でしたよね？）：**

1. **使い始めるだけ** - `/analyze some-file.js` や `/build` を試して、何が起こるか見てみましょう ✨
2. **学習についてストレスを感じないで** - SuperClaude は通常、必要なものを把握します
3. **自由に実験** - `/improve` や `/troubleshoot` のようなコマンドは寛容です
4. **興味があればガイドを読む** - 何が起こったか理解したいときは `Docs/` をチェック
5. **フィードバックを提供** - 何が機能し、何が機能しないか教えてください

**本当の秘密**：SuperClaude は、新しいことをたくさん学ばなくても既存のワークフローを強化するように設計されています。通常の Claude Code と同じように使用し、どれだけスマートになるか注目してください！🎯

**まだ不安ですか？** `/help` と `/analyze README.md` から始めてください - 実際にはそれほど恐ろしくないことがわかります。

---

## 最後に 📝

- **インストールには 1-5 分かかります**（選択内容による）
- **必要なディスクスペース：20-100MB**（それほど多くありません！）
- **既存のツールと一緒に動作** - セットアップに干渉しません
- **アンインストールが簡単**（気が変わった場合）
- **コミュニティサポート** - 実際に問題を読んで応答します
- ### ⚠️ 重要な注意
**SuperClaude をインストールした後、**
**`SuperClaude commands`、`python3 -m SuperClaude commands`、または `python3 SuperClaude commands` を使用できます**

SuperClaude をお試しいただきありがとうございます！開発ワークフローが少しでもスムーズになることを願っています。🙂

---

*最終更新：2024年7月 - このガイドに間違いや混乱する点があればお知らせください！*
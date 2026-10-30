# Tokyo Night Storm for Orca

[Orca](https://github.com/stablyai/orca) 用の Tokyo Night Storm テーマ。
VS Code の [Tokyo Night](https://github.com/tokyo-night/tokyo-night-vscode-theme)（enkia.tokyo-night 1.1.2）の Storm 配色を移植している。

## 含まれるもの

| 種類 | ファイル |
| --- | --- |
| アプリテーマ（UI + コード配色） | `themes/tokyo-night-storm.json` |
| ターミナルテーマ（ANSI 16 色） | `terminal/tokyo-night-storm.json` |

## ローカルで試す

1. Orca の Settings → Plugins で **Turn on plugins** を押す
2. **Development folders…** からこのフォルダを追加する
3. プラグインを有効化し、Appearance で Tokyo Night Storm を選ぶ

## VS Code 版との差分

- Orca はスペースを含むスコープ（子孫セレクタ）を読まないため、該当する `tokenColors` を除外している
- Orca はエディタ背景とのコントラストが 3:1 未満の色を無視するため、次の色を明るくしている
  - `#5f6996` → `#66709e`（コメント、Markdown の区切り線）
  - `#ba3c97` → `#c03e9c`（タグの `<` `>`）
  - `#914c54` → `#a95a64`（diff の削除行）

## License

MIT

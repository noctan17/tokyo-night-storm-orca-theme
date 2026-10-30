# Tokyo Night Storm for Orca

[Orca](https://github.com/stablyai/orca) 用の Tokyo Night Storm テーマ。
VS Code の [Tokyo Night](https://github.com/tokyo-night/tokyo-night-vscode-theme)（enkia.tokyo-night 1.1.2）の Storm 配色を移植している。

## 含まれるもの

| 種類 | ファイル |
| --- | --- |
| アプリテーマ（UI + コード配色） | `themes/tokyo-night-storm.json` |
| ターミナルテーマ（ANSI 16 色） | `terminal/tokyo-night-storm.json` |
| ファイルアイコン（Material Icons） | `icons/theme.json` |

## ファイルアイコン

[Material Icon Theme](https://github.com/material-extensions/vscode-material-icon-theme)（pkief.material-icon-theme 5.40.0）の SVG を使っている。

- Orca のアイコンテーマは割り当てが最大 512 件のため、よく使うファイル名・拡張子と VS Code 組み込み言語の拡張子に絞っている
- Orca はフォルダ名ごとのアイコンに対応していないため、フォルダはすべて共通のアイコンになる

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
- 背景は VS Code 版より 1 段暗くしている（エディタ `#1f2335`、サイドバー・ターミナル `#1b1e2e`、境界線 `#16161e`）
- カーソルと選択範囲を見やすくするため、`--ring` を `#7aa2f7` にしている
- 文字を読みやすくするため、UI とターミナルの文字色を `#c0caf5` に揃えている（ターミナルの `white` は `#a9b1d6`）
- Orca の Python / YAML のトークン分類に合わせて、次の色を VS Code の見た目に寄せている
  - `entity.name.tag` を `#7aa2f7` にしている（Python のデコレータが青になる。HTML/XML のタグ名も青になる）
  - `entity.name.type` を `#2ac3de` にしている（YAML のキーと、JS/TS の大文字始まりの名前が水色になる）

## License

MIT

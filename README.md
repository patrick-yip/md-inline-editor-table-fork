# Markdown Inline Editor for VS Code — Table Fork

Personal fork of [SeardnaSchmid/markdown-inline-editor-vscode](https://github.com/SeardnaSchmid/markdown-inline-editor-vscode) with additional features.

## What's different from upstream

### Table rendering (Issue [#23](https://github.com/SeardnaSchmid/markdown-inline-editor-vscode/issues/23))

Markdown tables render as aligned visual grids using VS Code decorations (no webview):

```
│ Name │ Description             │
│──────│─────────────────────────│
│ John │ A very long description │
│ Li   │ Short                   │
```

Features:
- 4 decoration types: `tablePipe`, `tableSeparatorPipe`, `tableSeparatorDash`, `tableCell`
- Column width calculation with CJK wide character support
- Inline cell formatting detection (bold, italic, strikethrough, code)
- Whole-block raw reveal when cursor enters any table row
- Edge cases: empty cells, single-column, table at EOF, trailing whitespace

Not yet implemented: column alignment CSS (left/center/right), ghost state for tables, performance tuning for large tables.

## Setup

```bash
npm install
npm run compile
npm test
```

Press `F5` in VS Code to launch the Extension Development Host.

## License

MIT License. See [LICENSE.txt](LICENSE.txt).

Original project by [SeardnaSchmid](https://github.com/SeardnaSchmid).

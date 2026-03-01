# Changelog

Changes made in this fork. Forked from [SeardnaSchmid/markdown-inline-editor-vscode](https://github.com/SeardnaSchmid/markdown-inline-editor-vscode) v1.16.2.

## Fork additions

### Table rendering (partial fix for [#23](https://github.com/SeardnaSchmid/markdown-inline-editor-vscode/issues/23))

- Visual table grid rendering with aligned columns using VS Code decorations
- 4 new decoration types: `tablePipe`, `tableSeparatorPipe`, `tableSeparatorDash`, `tableCell`
- Column width calculation with CJK wide character support
- Inline cell formatting detection (bold, italic, strikethrough, code)
- Whole-block raw reveal when cursor enters any table row
- Edge case handling: empty cells, single-column, table at EOF, trailing whitespace

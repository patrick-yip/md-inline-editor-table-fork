[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE.txt)
[![Version](https://img.shields.io/badge/version-1.16.2-blue.svg)](https://github.com/patrick-yip/md-inline-editor-table-fork/releases)

# md-inline-editor-table-fork

Render markdown tables as visual grids in VS Code.

<!-- TODO: Replace with actual demo GIF. Recommended: record with Kap showing a markdown table transforming from raw pipes to visual grid. -->
<p align="center"><img src="demo.gif" alt="demo" /></p>

## Why

[markdown-inline-editor-vscode](https://github.com/SeardnaSchmid/markdown-inline-editor-vscode) gives you Typora-like WYSIWYG editing in VS Code, but tables still render as raw pipe characters ([Issue #23](https://github.com/SeardnaSchmid/markdown-inline-editor-vscode/issues/23)). This fork adds visual table grid rendering using VS Code decorations, no webview required.

**Before:**
```
| Name | Description             |
|------|-------------------------|
| John | A very long description |
```

**After:**
```
│ Name │ Description             │
├──────┼─────────────────────────┤
│ John │ A very long description │
```

## Features

- **Visual table grids** with box-drawing characters replacing raw pipe syntax
- **CJK wide character support** for proper column alignment across languages
- **Inline formatting detection** preserves bold, italic, strikethrough, and code inside cells
- **Cursor-aware reveal** shows raw markdown when your cursor enters any table row

## Install

Download the latest `.vsix` from [Releases](https://github.com/patrick-yip/md-inline-editor-table-fork/releases), then:

```bash
code --install-extension md-inline-editor-table-fork-1.16.2.vsix
```

Or build from source:

```bash
git clone https://github.com/patrick-yip/md-inline-editor-table-fork.git
cd md-inline-editor-table-fork
npm install
npm run build
code --install-extension dist/extension.vsix
```

## Usage

1. Open any `.md` file in VS Code
2. Tables automatically render as visual grids
3. Click into a table row to reveal raw markdown for editing
4. Toggle all decorations with the eye icon in the editor title bar or run **Toggle Markdown Decorations** from the command palette

<!-- topics: vscode, vscode-extension, markdown, table, wysiwyg, inline-editor, markdown-table, typescript -->

## Contributing

This is a personal fork. The primary goal is to contribute table rendering back to the [upstream project](https://github.com/SeardnaSchmid/markdown-inline-editor-vscode).

- Issues and feedback welcome via [GitHub Issues](https://github.com/patrick-yip/md-inline-editor-table-fork/issues)
- PRs should include tests: `npm test`

## License

MIT © 2024 SeardnaSchmid. Fork maintained by [Patrick Yip](https://github.com/patrick-yip).

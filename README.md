# Obsidian Links for Cursor

Makes `obsidian://` links clickable in Markdown files (both in the editor and preview).

> Inpspired by [VSCode Clickable Obsidian Links](https://github.com/ststefa/vscode-obsidian-links)

## Installation

### Option 1: Install from VSIX (Recommended)

1. **Package the extension:**
   ```bash
   cd ObsidianLinksCursor
   npx @vscode/vsce package
   ```
   This creates `obsidian-links-1.0.0.vsix`

2. **Install in Cursor:**
   - Open Cursor
   - Press `Cmd+Shift+P` (or `Ctrl+Shift+P` on Windows/Linux)
   - Type `Extensions: Install from VSIX...`
   - Select the `.vsix` file you just created

### Option 2: Development/Symlink Install

1. **Find your Cursor extensions folder:**
   - macOS: `~/.cursor/extensions/`
   - Windows: `%USERPROFILE%\.cursor\extensions\`
   - Linux: `~/.cursor/extensions/`

2. **Copy or symlink the extension:**
   ```bash
   # Copy method
   cp -r ObsidianLinksCursor ~/.cursor/extensions/obsidian-links

   # Or symlink method (updates automatically when you edit)
   ln -s /path/to/ObsidianLinksCursor ~/.cursor/extensions/obsidian-links
   ```

3. **Restart Cursor**

## Usage

Once installed, any `obsidian://` links in your Markdown files will be:

- **In the editor:** Clickable (Cmd+Click or Ctrl+Click)
- **In preview:** Clickable links that open Obsidian

Example link format:
```markdown
[Open in Obsidian](obsidian://open?vault=MyVault&file=MyNote)
```

## Troubleshooting

- If links don't work, try restarting Cursor
- Check Developer Tools (`Help > Toggle Developer Tools`) for `[obsidian-links]` log messages
- Make sure Obsidian is installed and handles `obsidian://` URLs on your system

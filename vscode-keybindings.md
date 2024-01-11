# Vscode keybindings and configuration

## Added on 1/11/2024

### Keybindings

The following bindings allow to select the current tag and its content in html files. The first one is the default vscode binding, the second one is the emmet binding. The same is done for the shrink command. The emmet binding is only active when the language is html and there is a selection. The default binding is active in all cases.

```json
  {
    "key": "ctrl+shift+a",
    "command": "editor.action.smartSelect.grow",
    "when": "editorTextFocus"
  },
  {
    "key": "ctrl+shift+a",
    "command": "editor.emmet.action.balanceOut",
    "when": "editorTextFocus && editorLangId == html && editorHasSelection"
  },
  {
    "key": "ctrl+shift+d",
    "command": "editor.action.smartSelect.shrink",
    "when": "editorTextFocus"
  },
  {
    "key": "ctrl+shift+d",
    "command": "editor.emmet.action.balanceIn",
    "when": "editorTextFocus && editorLangId == html"
  },
```

source: [Stackoverflow](https://stackoverflow.com/a/40971959)

## Searched on 1/11/2021

- **Fold** folds the innermost uncollapsed region at the cursor:
  - `Ctrl + Shift + [` on Windows and Linux
  - `⌥ + ⌘ + [` on macOS

- **Unfold** unfolds the collapsed region at the cursor:
  - `Ctrl + Shift + ]` on Windows and Linux
  - `⌥ + ⌘ + ]` on macOS

- **Fold** All folds all regions in the editor:
  - `Ctrl + K, Ctrl + 0 (zero)` on Windows and Linux
  - `⌘ + K, ⌘ +0 (zero)` on macOS

- **Unfold** All unfolds all regions in the editor:
  - `Ctrl + K, Ctrl + J` on Windows and Linux
  - `⌘ + K, ⌘ + J` on macOS

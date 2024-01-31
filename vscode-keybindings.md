# Vscode keybindings and configuration

## Keybindings

### Select current tag (added on 1/11/2024)

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

### Fold and unfold regions

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

Source: [StackOverflow](https://stackoverflow.com/a/30077543)

### Navigation

- **Navigate** to the next open file:
  - `Ctrl + Tab` on Windows and Linux
  - `⌘ + Tab` on macOS

- **Navigate** to the previous open file:
  - `Ctrl + Shift + Tab` on Windows and Linux
  - `⌘ + Shift + Tab` on macOS

- **Navigate** to a specific open file:
  - `Ctrl + P` on Windows and Linux
  - `⌘ + P` on macOS

- **Navigate** to the last edit location:
  - `Ctrl + -` on Windows and Linux
  - `⌘ + -` on macOS

- **Navigate** to the last cursor location:
  - `Ctrl + U` on Windows and Linux
  - `⌘ + U` on macOS

- **Navigate** between editor groups:
  - `Ctrl + [any number]` on Windows and Linux
  - `⌘ + [any number]` on macOS

### Jumping

- **Jump** to definition:
  - `F12` on Windows and Linux
  - `F12` on macOS

- **Jump** to type definition:
  - `Ctrl + F12` on Windows and Linux
  - `⌘ + F12` on macOS

- **Jump** to opening/closing bracket:
  - `Ctrl + Shift + \` on Windows and Linux
  - `⌘ + Shift + \` on macOS

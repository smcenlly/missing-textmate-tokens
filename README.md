# missing-textmate-tokens README

This is the README to duplicate an issue with themes that are missing default textmate tokens.

# Steps to reproduce issue

1. Clone this repo.
2. Run `npm install`.
3. Open the repo in VS Code and Start debugging (F5).
4. Create a new file (Ctrl + N).
5. Change its language to `markup` using the `Change Language Mode` command
6. Paste the contents below:

```
deleted

inserted

underline
```

7. In any of the default VS Code themes, you will see something similar to:
![Working Example](./working.png)

8. Change theme to other theme and confirm whether the highlighting does not work. If not, for some reason, for your theme, the `textMateRules` tokens for markup are missing.

```
{
  "editor.tokenColorCustomizations": {
    "textMateRules": [
      {
        "name": "Deleted",
        "scope": "markup.deleted",
        "settings": {
          "foreground": "#ff0000"
        }
      },
      {
        "name": "Inserted",
        "scope": "markup.inserted",
        "settings": {
          "foreground": "#036A07"
        }
      },
      {
        "name": "Underline",
        "scope": "markup.underline",
        "settings": {
          "fontStyle": "underline"
        }
      },
    ]
  }
}
```
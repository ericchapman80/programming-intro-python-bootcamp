# Terminal Cheat Sheet

Printable beginner reference.

| Command | What It Does | Example | Beginner Explanation | Caution |
| --- | --- | --- | --- | --- |
| `pwd` | Prints current folder | `pwd` | Shows where you are | None |
| `ls` | Lists files | `ls` | Shows what is in this folder | Hidden files may not show |
| `cd` | Changes folder | `cd app` | Moves into a folder | Folder must exist |
| `cd ..` | Goes up one folder | `cd ..` | Moves to the parent folder | Easy to lose your place |
| `mkdir` | Makes folder | `mkdir notes` | Creates a new directory | Check spelling |
| `touch` | Makes file | `touch app.py` | Creates an empty file | Can update timestamp on existing file |
| `open .` | Opens current folder | `open .` | Opens Finder here | macOS only |
| `code .` | Opens VS Code | `code .` | Opens this folder in VS Code | Requires VS Code shell command |
| `clear` | Clears screen | `clear` | Cleans Terminal display | Does not delete files |
| `cat` | Prints file contents | `cat README.md` | Shows a text file | Long files scroll quickly |
| `cp` | Copies file | `cp a.txt b.txt` | Makes a copy | Can overwrite files |
| `mv` | Moves or renames | `mv old.py new.py` | Changes file location or name | Can overwrite files |
| `rm` | Removes file | `rm old.txt` | Deletes a file | Dangerous; no trash by default |
| `python3 --version` | Shows Python version | `python3 --version` | Confirms Python is installed | Version matters |
| `python3 app.py` | Runs Python file | `python3 app.py` | Runs your program | Run from the right folder |
| `brew --version` | Shows Homebrew version | `brew --version` | Confirms Homebrew is installed | macOS setup tool |
| `brew bundle --file=Brewfile` | Installs tools listed in Brewfile | `brew bundle --file=Brewfile` | Recreates documented Mac tool setup | Read the Brewfile first |

## Navigation Tip

Use `pwd` often. It answers the most important Terminal question: "Where am I?"

## Brewfile Tip

A `Brewfile` documents Homebrew tools for a project. In this bootcamp it is optional and used as a preview of setup automation.

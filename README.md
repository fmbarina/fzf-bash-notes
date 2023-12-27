# fuzzy bash notes

Quick and simple personal note system written in a single bash script.

(will put picture here, soon...)

Made to take random, small notes in Linux using a terminal. No idea how it'd work anywhere else.

- Pick and search notes using [fzf](https://github.com/junegunn/fzf).
- Create, delete and rename notes.
- Edit in your terminal editor of choice.

Not my idea, see Acknowledgments

# Prerequisites

- bash
- fzf
- a terminal editor of some kind
- [bat](https://github.com/sharkdp/bat) (optional, nicer previews)

# Installation

If you already know how to add a bash script to your PATH, skip to configuration.

1. Get the `notes` script by downloading or cloning this repository.
2. Include the script in your PATH.
  - If you don't know how PATH works, just put `notes` in `$HOME/.local/bin`
  - Might need to add `PATH=$HOME/.local/bin:$PATH` to your initialization scripts (e.g. put it at the end of your `.bashrc`)
3. Make sure the script is executable.
  - `chmod +x <path-to-notes-script>`

# Configuration

You can use it as-is, but if you want to change something, edit the variables near the top of the script or define the following environment variables:

- `BNOTES_EXT`: extension used when making new note files
- `BNOTES_NEW`: name of the option for creating a new note
- `BNOTES_DEL`: name of the option for deleting a note
- `BNOTES_MOV`: name of the option for renaming a note
- `BNOTES_BIN`: absolute path or name of binary to edit notes with

If `$BNOTES_BIN` is not set, `$EDITOR` will be used. If `$EDITOR` is not set, `$VISUAL` will be used.

# Use

Run the script in a terminal (type `notes` & enter).

Write some notes.

# Acknowledgments

Idea taken from Casey Brant's [Simple Notes Taking with fzf and vim](https://medium.com/adorableio/simple-note-taking-with-fzf-and-vim-2a647a39cfa).

Some more ideas taken from elsewhere but I can't find it right now.

# Alternatives

There are so many. Folks seem to love taking notes :^)

Interestingly, while searching for Brant's blog again post I found [alichtman/fzf-notes](https://github.com/alichtman/fzf-notes). Lichtman's version supports notebooks, along with other nifty features.

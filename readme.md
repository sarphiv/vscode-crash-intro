# Visual Studio <ins>_**Code**_</ins> introduction

Crash introduction for Visual Studio Code for a select few AIDS (KID) students at DTU
with the aim of migrating them from using Spyder for AI/ML development.

This is an informal student to student introduction.

## Prerequisites

- Basic programming skills
- GitHub account
- Anaconda (the animal)
- Non-possessed computer
- Slightly above average brain

## Setup
---

The following is preparatory work each participant needs to do before the live introduction.

If you encounter any issues, feel free to contact me.

### Installation

1. Visit https://code.visualstudio.com/
0. Download and follow onscreen instructions
0. Enable option `"Add to PATH"`
0. ???
0. Profit - open VSCode

### Plugins

The following plugins are necessary for Python development. 

Install by pressing `ctrl+shift+x` inside VSCode and apply brain.

#### Required

- Anaconda Extension Pack

#### Recommended

- Jupyter
- Pylance
- Visual Studio IntelliCode
- Live Share
- Bracket Pair Colorizer 2
- Python Indent

## Usage
---

The following are notes for a live introduction
which will be held at an agreed upon date by the participants.

The notes can later be used as a cheatsheet/reference material.

### Start up
---

1. Open VSCode
    1. On Windows:
        1. Open Anaconda <ins>_**Prompt**_</ins> _(not navigator)_
        0. Run the command `code`
        0. Hint: Make a shortcut that does all this
    0. Linux/MacOS:
        1. Open VSCode normally
0. Open a folder/project with `ctrl+k, ctrl+o` (or File->Open Folder...)
0. Open file via
    - Search: `ctrl+p`
    - File panel: `ctrl+shift+e`

### Standard usage
---

- View
    - New file: `ctrl+n`
    - New window: `ctrl+shift+n`
    - Switch tab: `ctrl+tab` and `ctrl+shift+tab`
    - Close/unclose tab: `ctrl+w` and `ctrl+shift+t`
    - File panel: `ctrl+shift+e`
    - Problems panel: `ctrl+shift+m`
    - Debug console: `ctrl+shift+y`
    - Split window right: `ctrl+(` or `drag and drop tab`
    - Split window down: `ctrl+k, ctrl+(` or `drag and drop tab`
- File
    - Save file: `ctrl+s`
    - Save all: `ctrl+k, s`
    - Find file: `ctrl+p`
    - Go to definition: `F12` or `ctrl+left click`
    - Go to references: `shift+F12`
    - Go to symbol: `ctrl+shift+o`
    - Go to bracket: `ctrl+shift+(`
    - Go to line: `ctrl+g`
- Selection
    - Select line above/below: `ctrl+shift+up` and `ctrl+shift+down`
    - Select character left/right: `shift+left` and `shift+right`
    - Select word left/right: `ctrl+shift+left` and `ctrl+shift+right`
    - New cursor above/below: `ctrl+shift+alt+down` and `ctrl+shift+alt+down`
    - New cursor at click: `alt+left mouse button`
    - New cursor at next same word: `ctrl+d`
    - New cursor at occurrences of word: `ctrl+shift+l`
- Editing
    - Undo/Redo: `ctrl+z` and `ctrl+shift+z`
    - Move line(s): `alt+up` and `alt+down`
    - Duplicate line(s): `alt+shift+up` and `alt+shift+down`
    - Comment line(s): `ctrl+'`
    - Delete line(s): `ctrl+shift+k`
    - Rename variable: `F2`
    - Find: `ctrl+f`
    - Replace: `ctrl+h`
    - Indent/unindent line(s): `tab` and `shift+tab`
    - New line below/above: `ctrl+enter` and `ctrl+shift+enter`
- Multi-purpose
    - Do everything: `ctrl+shift+p`
    - Fix everything: `ctrl+.`
- Miscellaneous
    - Remember to run the correct file
    - Run: `ctrl+F5`
    - Snippets: `tab`, `tab`, `tab`...
    - Surround: Select text, press `'`, `"`, `(`, `[`, or `{`
    - Change case: Select text, `ctrl+shift+p`, `transform to [...]`
    - Word wrap: `alt+z`
    - Functions can be collapsed (hidden from view)


### Jupyter Notebook
---

- Jupyter Notebooks supported
    - Ensure `Python (conda)` selected (top right)
    - `F10` to run cell, line by line
    - New notebook: `ctrl+shift+p`, `new notebook`
    - Works like normal
- Interactive mode
    - Useful as playground for experimentation
    - Program state is stored - double edged sword
    - Create a cell: `#%%`
    - Run current cell: `ctrl+enter`
    - Execute command: `shift+enter`

### Debugging
---

- Buggy/complex program?
    1. Run with debug: `F5, enter`
    0. Pause program on one of
        - Error
        - Breakpoint
        - Next line
    0. Predict expected program state
    0. Find inconsistency with actual state
    0. Branch
        - If root cause found, deal with it
        - Else, go to step 2 and pause near cause of inconsistency
- Tools to examine state
    - Navigation
        - Stop/restart: `shift+F5` and `ctrl+shift+F5`
        - Continue/pause: `F5` and `F6`
        - Step in/out: `F11` and `shift+F11`
        - Step over: `F10`
        - Line/inline breakpoint: `F9` and `shift+F9`
            - Conditional: `right click breakpoint, edit breakpoint...`
    - State
        - Hover mouse on variable
        - Debug panel: `ctrl+shift+d`
            - Read/write variables
            - Watch expressions
            - (Call stack)/(stack trace)
                - "Map sequence" of which functions called each other
                - Scope of variables is different
                - Use to get context on issues
    - Manipulation
        - Debug console: `ctrl+shift+y`
            - Examine state
            - Change variables
            - Run functions
        - Interactive mode
            - Quick experimentation
                - Reproduce issue
                - Test potential fix
            - Access to data viewer
- Miscellaneous
    - Remember to run the correct file
    - Slower execution
        - Do not test speed of program in debug mode
        - Long experiments take even longer in debug mode
        - Concurrency related issues may not happen because it's slower

### Live Share
---

- Setup
    - Sign in with GitHub: `ctrl+shift+p, live share sign in browser`
    - Start read/write session (<ins>**only**</ins> with <ins>**trusted**</ins> people)
        - Share: `ctrl+shift+p, live share start`
        - Join: `ctrl+shift+p, live share join` or `ctrl+alt+j`
- Google Docs (Beta - Developer Edition)
    - Usually perfect, sometimes not
        - Changes may not propagate
        - Participants are not visible or do not move
        - Mangled console output
    - Fix: `Restart Live Share session and VSCode`
- Collaborative debugging
    - Follow mode
    - Highlighting
    - Only host can (should) interact with consoles (terminal, debug, interactive)
    - No more backseat programmers

### Long-running tasks
---

- Task examples
    - Training models
    - Collecting experiment data
    - ~~Ethereum mining~~
- Crash -> Loss of training progress or experiment data
- Fail-safe techniques
    - Redirect
        - Open `Anaconda Prompt`
        - Navigate to python file with `cd "<path to folder>"`
        - Run python file
            - Overwrite: `python "<name of python file>.py" > "<name of output file>"`
            - Append: `python "<name of python file>.py" >> "<name of output file>"`
    - In code
        - More complicated, more flexible
        - Use `pickle` module for serialization
        - Get file handles with `open` function.
- Caveats
    - Force buffer flush: `print(some_text, flush=True)`
    - Printing and file operations are slow

### Git, GitHub, and Goodies
---

- Git panel: `ctrl+shift+g`
    - SCRUB, LEARN THE CONSOLE
- Core actions
    - Push
    - Pull
    - Add
    - Commit
    - Branch
    - Checkout
    - Merge
- Workflow
    1. Branch
    0. Work
    0. Commit
    0. Pull
    0. Push
- GitHub Student Developer Pack
    - https://education.github.com/pack
    - Connect your DTU email to GitHub

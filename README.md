# Why would I want this?

Because there's a whole lot of probably-could-be-built-in features that you can get with one install.

# What are examples of some automatic features

- The ability to open PDF's (yeah thats not built in)
- File path auto-completion
- Syntax highlighting colors for basically every language
- Displays who made the last git change for the current line in your current file
- Color-numbers (hex colors or RGB) are highlighted as their actual color
- If you enable the built-in `renderWhitespace`, you'll see spaces, tabs, and newlines instead of only spaces and tabs
- Auto-complete for C++
- Auto-complete for Python

# What are examples of useful commands

Open and run basically any file with `Ctrl/Cmd+Alt+N`, thanks to code-runner
Compare a file between two git branches with `GitHD: View Branch Diff`, thanks to GitHD
Scroll through file history with the GitLens side-bar, thanks to GitLens
Open the current file on GitHub.com with the `Open in GitHub` command, thanks to open-in-github


# What are some useful settings?

```json
{
    // general
    "extensions.ignoreRecommendations": true,
    "files.restoreUndoStack": true,
    "editor.copyWithSyntaxHighlighting" : false,
    "files.hotExit": "onExitAndWindowClose",
    "editor.quickSuggestionsDelay": 0,
    "zenMode.centerLayout": false,
    
    // code runner
    "code-runner.runInTerminal": true,
    "code-runner.clearPreviousOutput": true,
    "code-runner.ignoreSelection": true,
    
    // git
    "git.autofetch": true,
    "git.confirmSync": false,
    "git.enableSmartCommit": true,
    
    // fancy visuals
    "editor.cursorSmoothCaretAnimation" : true,
    "editor.cursorBlinking": "expand",
    "editor.smoothScrolling": true,
    "editor.fontLigatures": true,
    "terminal.integrated.rendererType": "dom",
    
    // likely but may not always want
    "editor.multiCursorModifier": "ctrlCmd",
    "editor.find.seedSearchStringFromSelection": false,
} 
```

What are some useful keyboard shortcuts to add?
```json
[
    // 
    // 
    // 
    // Cursor movement
    // 
    // 
    // 
    
        // 
        // Jump word
        // 
        { "key": "alt+right",       "command": "cursorWordRight",       "when": "textInputFocus" },
        { "key": "alt+left",        "command": "cursorWordLeft",        "when": "textInputFocus" },
        { "key": "alt+shift+right", "command": "cursorWordRightSelect", "when": "textInputFocus" },
        { "key": "alt+shift+left",  "command": "cursorWordLeftSelect",  "when": "textInputFocus" },
        
        //
        // line move/duplicate
        //
        { "key": "alt+shift+down", "command": "editor.action.copyLinesDownAction", "when": "textInputFocus" },
        { "key": "alt+down",       "command": "editor.action.moveLinesDownAction", "when": "textInputFocus" },
        { "key": "alt+shift+up",   "command": "editor.action.copyLinesUpAction",   "when": "textInputFocus" },
        { "key": "alt+up",         "command": "editor.action.moveLinesUpAction",   "when": "textInputFocus" },
        
        // 
        // end/begin line/file
        // 
        { "key": "ctrl+right",       "command": "cursorEnd",          "when": "textInputFocus && !isMac" },
        { "key": "ctrl+left",        "command": "cursorHome",         "when": "textInputFocus && !isMac" },
        { "key": "ctrl+shift+right", "command": "cursorEndSelect",    "when": "textInputFocus && !isMac" },
        { "key": "ctrl+shift+left",  "command": "cursorHomeSelect",   "when": "textInputFocus && !isMac" },
        { "key": "ctrl+up",          "command": "cursorTop",          "when": "textInputFocus && !isMac" },
        { "key": "ctrl+down",        "command": "cursorBottom",       "when": "textInputFocus && !isMac" },
        { "key": "ctrl+shift+up",    "command": "cursorTopSelect",    "when": "textInputFocus && !isMac" }, 
        { "key": "ctrl+shift+down",  "command": "cursorBottomSelect", "when": "textInputFocus && !isMac" },
        // remove existing keybindings
        { "key": "ctrl+shift+right", "command": "-editor.action.smartSelect.expand", "when": "editorTextFocus"},
        { "key": "ctrl+shift+left", "command": "-editor.action.smartSelect.shrink", "when": "editorTextFocus"},
        
        { "key": "cmd+right",       "command": "cursorEnd",          "when": "textInputFocus && isMac" },
        { "key": "cmd+left",        "command": "cursorHome",         "when": "textInputFocus && isMac" },
        { "key": "cmd+shift+right", "command": "cursorEndSelect",    "when": "textInputFocus && isMac" },
        { "key": "cmd+shift+left",  "command": "cursorHomeSelect",   "when": "textInputFocus && isMac" },
        { "key": "cmd+up",          "command": "cursorTop",          "when": "textInputFocus && isMac" },
        { "key": "cmd+down",        "command": "cursorBottom",       "when": "textInputFocus && isMac" },
        { "key": "cmd+shift+up",    "command": "cursorTopSelect",    "when": "textInputFocus && isMac" },
        { "key": "cmd+shift+down",  "command": "cursorBottomSelect", "when": "textInputFocus && isMac" },
        
        // 
        // multi cursor
        // 
        { "key": "ctrl+shift+alt+up",   "command": "cursorColumnSelectUp",   "when": "editorTextFocus && !isMac" },
        { "key": "ctrl+shift+alt+down", "command": "cursorColumnSelectDown", "when": "editorTextFocus && !isMac" },
        { "key": "cmd+shift+alt+up",    "command": "cursorColumnSelectUp",   "when": "editorTextFocus && isMac"  },
        { "key": "cmd+shift+alt+down",  "command": "cursorColumnSelectDown", "when": "editorTextFocus && isMac"  },
        
        // 
        // undo / redo jump
        // 
        { "key": "alt+z",       "command": "workbench.action.navigateBack" },
        { "key": "alt+shift+z", "command": "workbench.action.navigateForward" },
        
        // 
        // jump brackets
        // 
        { "key": "alt+[", "command": "editor.action.jumpToBracket", "when": "editorTextFocus" },
        { "key": "alt+]", "command": "editor.action.jumpToBracket", "when": "editorTextFocus" },
        { "key": "shift+alt+[", "command": "editor.action.selectToBracket", "when": "editorTextFocus" },
        { "key": "shift+alt+]", "command": "editor.action.selectToBracket", "when": "editorTextFocus" },
        
        // 
        // jump/select to comma
        // 
        { "key": "alt+.",       "command": "mario.nextComma",           "when": "editorTextFocus" },
        { "key": "alt+,",       "command": "mario.previousComma",       "when": "editorTextFocus" },
        { "key": "alt+shift+.", "command": "mario.selectNextComma",     "when": "editorTextFocus" },
        { "key": "alt+shift+,", "command": "mario.selectPreviousComma", "when": "editorTextFocus" },

        // 
        // jump/select to quote
        // 
        { "key": "alt+'",       "command": "mario.nextQuote",           "when": "editorTextFocus" },
        { "key": "alt+;",       "command": "mario.previousQuote",       "when": "editorTextFocus" },
        { "key": "alt+shift+'", "command": "mario.selectNextQuote",     "when": "editorTextFocus" },
        { "key": "alt+shift+;", "command": "mario.selectPreviousQuote", "when": "editorTextFocus" },
        
        // 
        // Mario: MacOS: ctrl + WASD
        // 
        { "key": "ctrl+up",         "command": "mario.moveUp",          "when": "editorTextFocus && isMac" },
        { "key": "ctrl+left",       "command": "mario.moveToOuter",     "when": "editorTextFocus && isMac" },
        { "key": "ctrl+down",       "command": "mario.moveDown",        "when": "editorTextFocus && isMac" },
        { "key": "ctrl+right",      "command": "mario.moveDownToInner", "when": "editorTextFocus && isMac" },
        { "key": "ctrl+alt+right",  "command": "mario.moveUpToInner",   "when": "editorTextFocus && isMac" },
        { "key": "ctrl+shift+up",   "command": "mario.selectUp",        "when": "editorTextFocus && isMac" },
        { "key": "ctrl+shift+down", "command": "mario.selectDown",      "when": "editorTextFocus && isMac" },
        { "key": "ctrl+shift+left", "command": "mario.selectToOuter",   "when": "editorTextFocus && isMac" },
        
        // 
        // Mario: Non-MacOS: cmd + WASD
        // 
        { "key": "cmd+up",         "command": "mario.moveUp",          "when": "editorTextFocus && !isMac" },
        { "key": "cmd+left",       "command": "mario.moveToOuter",     "when": "editorTextFocus && !isMac" },
        { "key": "cmd+down",       "command": "mario.moveDown",        "when": "editorTextFocus && !isMac" },
        { "key": "cmd+right",      "command": "mario.moveDownToInner", "when": "editorTextFocus && !isMac" },
        { "key": "cmd+e",          "command": "mario.moveUpToInner",   "when": "editorTextFocus && !isMac" },
        { "key": "cmd+shift+up",   "command": "mario.selectUp",        "when": "editorTextFocus && !isMac" },
        { "key": "cmd+shift+down", "command": "mario.selectDown",      "when": "editorTextFocus && !isMac" },
        
        
        // 
        // 
        // Quick selects
        // 
        // 
        
        // all instances
        { "key": "cmd+enter", "command": "editor.action.changeAll", "when": "editorTextFocus && !editorReadonly && isMac" },
        { "key": "ctrl+enter", "command": "editor.action.changeAll", "when": "editorTextFocus && !editorReadonly && !isMac" },
        { "key": "shift+cmd+enter",   "command": "macros.SelectLocal", "when": "!editorHasRenameProvider && editorTextFocus && !editorReadonly && isMac" },
        { "key": "shift+ctrl+enter", "command": "macros.SelectLocal", "when": "!editorHasRenameProvider && editorTextFocus && !editorReadonly && !isMac" },
        // remove built-ins for rename
        { "key": "cmd+enter", "command": "-editor.action.insertLineAfter", "when": "editorTextFocus && !editorReadonly && isMac"},
        { "key": "shift+cmd+enter", "command": "-editor.action.insertLineBefore", "when": "editorTextFocus && !editorReadonly && isMac"},
        { "key": "ctrl+enter", "command": "-editor.action.insertLineAfter", "when": "editorTextFocus && !editorReadonly && !isMac"},
        { "key": "shift+ctrl+enter", "command": "-editor.action.insertLineBefore", "when": "editorTextFocus && !editorReadonly && !isMac"},
        
        // Switch to Next Match
        { "key": "cmd+g", "command": "editor.action.nextMatchFindAction", "when": "editorFocus || findInputFocused && isMac" },
        { "key": "ctrl+g", "command": "editor.action.nextMatchFindAction", "when": "editorFocus || findInputFocused && !isMac" },
        { "key": "cmd+shift+g", "command": "editor.action.previousMatchFindAction", "when": "editorFocus || findInputFocused && isMac" },
        { "key": "ctrl+shift+g", "command": "editor.action.previousMatchFindAction", "when": "editorFocus || findInputFocused && !isMac" },
        
        // Add Next Match
        { "key": "cmd+d", "command": "editor.action.addSelectionToNextFindMatch", "when": "editorFocus && isMac" },
        { "key": "ctrl+d", "command": "editor.action.addSelectionToNextFindMatch", "when": "editorFocus && !isMac" },
    
    // 
    // 
    // disable some built-ins
    // 
    // 
        { "key": "up", "command": "-showPrevParameterHint", "when": "editorTextFocus && parameterHintsMultipleSignatures && parameterHintsVisible"},
        { "key": "up", "command": "-showPrevParameterHint", "when": "editorFocus && parameterHintsMultipleSignatures && parameterHintsVisible"},
        { "key": "down", "command": "-showNextParameterHint", "when": "editorTextFocus && parameterHintsMultipleSignatures && parameterHintsVisible"},
        { "key": "down", "command": "-showNextParameterHint", "when": "editorFocus && parameterHintsMultipleSignatures && parameterHintsVisible"},
]
```
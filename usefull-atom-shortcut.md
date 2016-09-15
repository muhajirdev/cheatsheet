# atom init script to disable ubuntu unity `alt` so you can use alt shortcut

## My init script
```
# Your init script
#
# Atom will evaluate this file each time a new window is opened. It is run
# after packages are loaded/activated and after the previous editor state
# has been restored.
#
# An example hack to log to the console when each text editor is saved.
#
# atom.workspace.observeTextEditors (editor) ->
#   editor.onDidSave ->
#     console.log "Saved! #{editor.getPath()}"
atom.menu.template.forEach (t) ->
  t.label = t.label.replace("&", "")
atom.menu.update()
```
Go to `Edit > Init Script` and paste above code.

# atom usefull shortcut ( linux ):

## Editing

* `ctrl+enter` newline
* `ctrl+snift+enter` newline line above
* `ctrl+l` select current line
* `ctrl+shift+k` delete line
* `ctrl+j` join line with bottom line


* `ctrl+shif+d` duplicate line
* `ctrl+up` / `ctrl+down` move line up / down
* `ctrl+ [` / `ctrl+]` indent / outdent
* `ctrl+g` Go to line
* `ctrl+/` toggle comment


* `ctl+m` go to matching bracket /tag
* `ctrl+alt+.` complete bracktes / tag
* `ctrl+alt+m` select code inside brackets /tag


* `alt+b / f` move to the beginning / end of word
* `alt+shift+b / f` select to the beginning / end of word
* `ctrl+backspace` / `alt+h` delete to the beginning of word
* `ctrl+delete` / `alt+d` delete to the end of the word

* `alt+shift+down` add another cursor below
* `alt+shift+up` add another cursor above
* `ctrl+click` add another cursor on clicked location

* `alt+shift+s` show available snippets

## Fold

* `ctrl+k ` then `ctrl+1..9` fold all code at 1..9 level
* `ctrl+alt+/` toggle (un)fold code
* `ctrl+alt+f` fold selected code
* `ctrl+alt [/]` fold / unfold all code

## Find and Replace

* `ctrl+f` show 'find' in current file
* `ctrl+shift+f` show 'find' in project
* `f3` find next in 'find' mode
* `shift+f3` find previous
* `ctrl+enter` replace all
* `tab` focus next
* `ctrl+alt+/` use regex
* `ctrl+alt+c` use match case
* `ctrl+alt+s` use search only in selection
* `ctrl+alt+w` use match whole word

  in selection / previous word:


* `ctrl+d` select next word
* `ctrl+u` undo select
* `alt+f3` select all same word like in selction
* `ctrl+e` use selection as find pattern
* `ctrl+f3`find next selected


## Tree View

* `ctrl+\` toggle tree view
* `alt+\` toggle focus between tree view and editor
* Movement in tree view focus :
  * j = down arrow
  * k = up
  * h = left (collapse folder)
  * l = right (expand folder)
`Enter` open / expand item
* `alt+left / rigth` / `ctrl+alt [/]` collapse / expand folder recursively
* `Backspace` / `delete` delete item
* `m` / `f2` move item ( rename)
* `d` duplicate
* `a` add new file
* `shift+a` add new folder
* `i` toggle display vcs ignored files

## General

* `ctrl+shift+l` select language
* `ctrl+shift+p` command
* `ctrl+,` open settings
* `ctrl+shift+r` reload /relaunch atom
* `ctrl+shift+m` preview markdown ( only when language markdown selected )
* `ctrl+- ` decrease font size
* `ctrl+=` increase font size
* `ctrl+0` reset font size
* `f11` toggle fullscreen

## file

* `ctrl+b` toggle list of opened file
* `ctrl+p` / `ctrl+t` open file (with search)
* `ctrl+n` new file
* `ctrl+shift+n` new window
* `ctrl+o` open file
* `ctrl+shift+o` open folder
* `ctrl+alt+o` add project folder
* `ctrl+s` save file
* `ctrl+shift+s` save as
* `ctrl+w` close tab
* `ctrl+tab` switch tab
* `ctrl+shift+w` close window
* `ctrl+shift+t` open recently close tab

## Git Diffs

`alt+g d` list file diffs
`alt+g up/down` move to next / previous diffs


## Open on Github

* `alt+g o` file
* `alt+g g` repo
* `alt+g b` blame
* `alt+g i` issue
* `alt+g h` history
* `alt+g r` branch compare
* `alt+g c` copy url

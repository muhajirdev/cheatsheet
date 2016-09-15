# The Terminal Tips and Shortcut

I use this on linux (Ubuntu), i dont know if all of this command also works on mac, just give it  a try :)

## Shortcut

* `up` and `down` to select previous command.
  For example, you last command was `sudo apt-get update`, to run that command again just press `up` arrow, and there you go. press `up` again to get the older command.
* `ctrl+left` and `ctrl+right` to jump betweeen argument
  on mac and windows : `esc+b` and `esc+f`, you can change the shortcut if you use mac.
* `Home` and `End` to move to the beginning and the end of typed command.
  Alternative : `ctrl+a` and `ctrl+e`
* `ctrl+u` delete from current cursor to the beginning of currently typed command.
* `ctrl+k` delete from  current cursor to the end of currently typed command
* `ctrl+w` delete from current cursor the beginning of word
* `ctrl+r` search trough the command history. and then use `up` and `down` to navigate trought the history.
  \* type `history` to see full list of history
* `tab` auto complete command or directory name.

## Tips

Use `!`

* `!!` represent your last command.
  Example :
  ```
  $ apt-get upgrade
  E: Could not open lock file /var/lib/dpkg/lock - open (13: Permission denied)
  E: Unable to lock the administration directory (/var/lib/dpkg/), are you root?
  $ sudo !!
  sudo apt-get upgrade
  [sudo] password for muhajir:
  Reading package lists... Done
  ...
  ```

* ![word] to run the last [word] command.
  Example :
  ```
  $ ls Documents/
  blog  book  cheatsheet  drawing  GitBook  Inkscape  logo  terminal-shortcut.md
  $ sudo apt-get update
  [sudo] password for muhajir:
  ...
  $ sudo apt-get upgrade
  [sudo] password for muhajir:
  ...
  $ !ls
  ls Documents/
  blog  book  cheatsheet  drawing  GitBook  Inkscape  logo  terminal-shortcut.md
  ```
  if just want to see the command without running it.
  use ![word]:p, example : `!ls:p`.
  It will print the command and add it to the end of
  command history. type `history` to prove it.

* !$ represent last used argument
  Example:
  ```
  $ mkdir somefolder
  $ cd !$
  cd somefolder
  ~/somefolder $ _
  ```

* Typo ?
  Example:
  ```
  $ loss index.html
  No command 'loss' found, did you mean:
   Command 'less' from package 'less' (main)
   Command 'aoss' from package 'alsa-oss' (universe)
  loss: command not found
  $ ^loss^less
  less index.html
  ...
  ```
  See `^loss^less` ?
  it will run the previous command, but fix the typo.

* type `history`, you will see something like this.
  ```
  101  sudo apt-get update
  102  ls Documents/
  103  ls a
  104  ls
  105  ls Music
  106  ls res
  107  ~ls
  108  ls res
  109  history
  110  ls res
  111  sudo apt-get update
  112  history
  113  ls
  114  mkdir somefolder
  115  cd somefolder
  116  loss index.html
  117  less index.html
  118  history
```
  type `!114` to run `mkdir somefolder`

* Create your own custom command.
  open `~/.bashrc` or `~/.bash_profile` on mac.
  and add the following line at the bottom of the file ( as an example)
  ```
  alias gst='git status'
  ```
  so, next time you run `gst` on the terminal, it will run `git status` automatically.

* What can i call this command?
  Example:
  ```
  $ mkdir myfolder-{1,2,3}
  ```
  is the same as
  ```
  $ mkdir myfolder-1 myfolder-2 myfolder-3
  ```
  both of those command will create `myfolder-1` `myfolder-2` and `myfolder-3`

  This is also usefull when we combine it with command `cp` and `mv` . Example
  ```


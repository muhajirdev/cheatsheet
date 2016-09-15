# This is my personal vim sheet:

in vim, there are two mode:
1. Insert mode.
	Insert mode is like usual typing. Nothing more.
2. Normal mode
	Normal mode is the mode where you can execute most of the vim command and shortcuts. This is what make vim special , unlike other editor.


I am sure for the first time you use vim, you'll be a little bit not familiar with Vim normal mode, even when the first time i use vim, i thought something is went wrong, i dont know how to type inside it, i dont know how quit it, and i ended up closing my terminal. :)

So, in vim, to navigate trought the documents you can use hjkl, yup,
- h -> left
- j -> down
- k -> up
- l -> right

Arrow button is actually works too on vim, but some poeple just prefer to not move their hand on the keyboard, they prefer hjkl for a faster typing experience they said. They said it's just much more efficient to use hjkl.

The reason that write this documents is just want to practice using vim. I am a new vim user too, i am trying this, i read quora. Even developers at google, facebook , etc. They use this faking Vim and Emacs. what the hell i think. what so special about these two editor. So i decided to give it a try. And it feels awesome when you dont have to move your hand away from the keyboard :).

So, why vim ? why not Emacs, i will try both actually. i try vim first, because it's available on all unix machine, and it's lighter than emacs they said, preinstall "vi" on my ubuntu machine, so i just installed vim to get a better experince. And right now i am downloading emacs too.


SHEET:
1. Move cursor (motion):

	h --> left
	j --> down
	k --> up
	l --> right

	w --> go to the next word
	e --> go to the end of word
	b --> go to the beginning of word.

	$ --> go to the end of line
	0 --> go to the end of line

2. common command in vim :
	- :q to quit
	- :q! to force quit when you haven't saved the document yet
	- :w to write ( save the document)
	- :wq to save and quit
	- ZZ in normal mode to save and quit quickly
	- search command :
		- :s/old/new --> change text on the line
		- :s/old/new/g --> change text on the line globally
		- :%s/old/new/g --> change text in the whole file
		- :%s/old/new/gc -> change text in the file with prompt
		-:#,#s/old/new/g -> change text with range #,# (#,# is line number)
3. using count with motion :
   examples	- 2w --> same as ww
		- 3e --> same as eee
4. common verb :
	- i --> go to insert mode
	- a --> append ( almost like insert mode)
		- a : insert on next char
		- A : insert on the end of line
	- x --> delete a single char
	- r --> replace a single character
	- d --> delete ( could be combined with motion)
		- de --> to delete till the end of word
		- dw --> to delete till the next word
		- db --> to delete till the beginning of the word
		- d$ --> to delete till the enf of line.
		- dd --> (QUICK VERSION OF d$)
		- 2dd -- same as dd dd
		- d2w -> to delete two next words.
	- o --> insert new line below
		- O --> insert new line above
	- u --> undo command
		- U --> reset the line to original state
		- CTRL-R --> Redo
	- p --> put / paste
		what will be pasted ? :
		- previously delete text using d or x command
		- previuously copied / yank text ( using yy, yw, etc)
		- previous delete text because c 	
	- c --> change
		- ce --> change until the end of word. ( short for de i)
		- cc --> change until the end of line ( short of dd i)
	- % --> to find the matching parentheses
		- {} [] ()

5. Execute command:
	type :! followed by command.
	Example:
	- :!ls
	- :!less

6. Selecting Text with v command.
	when a text selected, pressing : will showing op :'<,'>
	when you w TEST ( :'<,'> w TEST) right on it. it will save / create a new file named TEST with the content being the text selection

7. Retrive file with :r
	To retrieve text from TEST file, use :r TEST
	you can also retrive text form command , example --> :r !ls
8. Replace mode with R
	Replace mode is like insert mode
	but it replace the existing character when you type
	it works like r , but not for a single character.
9. Tips :
	- ea , continues incomplete letter.
10. Copy Paste :
	- y (yank) to copy : y combined with motion , etc. yy to copy 1 line.
	- p to paste

PART 2 :

Movement Keys :
w -> move to the next word
W -> move to next word with ignoring thing like . , etc.

e -> move to the end of word.
E -> move to the end of word ignoring thing like . , etc.

b -> move backward to the begninng of word.
B -> move backward to the begninng of word ignoring thing like . , etc.

cw - > change 1 word
cb -> change 1 word behind
C -> change the remaining part of line

dw -> delete one word
db -> delete one word behind
D -> change the remaining part of line

u -> undo last operation
U -> undo all last operation made on the current line.
Ctrl + R -> Redo Action.

/text -> search for the text
?text -> search for the text (backward)
n -> jump to the next match
N -> jump to the previous match
:s/old/new --> replace old with new text (line scope)
:s/old/new/g --> replace old with new text globally (line scope)
:%s/old/new --> replace old with new text
Ahh i am still not clear yet about this search and replace feature.

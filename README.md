# Vim

### Save and Exit
```
w                  save file
wq or x or ZZ      save and quit
q                  quit
q! or ZQ           force quit
help keyword       open help for keyword
o file             open file
saveas file        save file as
close              close current pane
```

### Cursor movement
```
h            move cursor left
j            move cursor down
k            move cursor up
l            move cursor right
H            move to top of screen
M            move to middle of screen
L            move to bottom of screen
w            jump forwards to the start of a word
W            jump forwards to the start of a word (words can contain punctuation)
e            jump forwards to the end of a word
E            jump forwards to the end of a word (words can contain punctuation)
b            jump backwards to the start of a word
B            jump backwards to the start of a word (words can contain punctuation)
0            jump to the start of the line
^            jump to the first non-blank character of the line
$            jump to the end of the line
g_           jump to the last non-blank character of the line
gg           go to the first line of the document
G            go to the last line of the document
5G           go to line 5
fx           jump to next occurrence of character x
tx           jump to before next occurrence of character x
}            jump to next paragraph (or function/block, when editing code)
{            jump to previous paragraph (or function/block, when editing code)
zz           center cursor on screen
Ctrl + b     move back one full screen
Ctrl + f     move forward one full screen
Ctrl + d     move forward 1/2 a screen
Ctrl + u     move back 1/2 a screen
```

### Insert mode
```
i            insert before the cursor
I            insert at the beginning of the line
a            insert (append) after the cursor
A            insert (append) at the end of the line
o            append (open) a new line below the current line
O            append (open) a new line above the current line
ea           insert (append) at the end of the word
Esc          exit insert mode
```

### Editing
```
r            replace a single character
J            join line below to the current one
cc           replace entire line
cw           replace to the start of the next word
ce           replace to the end of the next word
cb           replace to the start of the previous word
c0           replace to the start of the line
c$           replace to the end of the line
s            delete character and substitute text
S            delete line and substitute text (same as cc)
xp           transpose two letters (delete and paste)
.            repeat last command
u            undo
Ctrl + r     redo
```

### Visual Mode
```
v            start visual mode, mark lines, then do a command (like y-yank)
V            start linewise visual mode
o            move to other end of marked area
O            move to other corner of block
aw           mark a word
ab           a block with ()
aB           a block with {}
ib           inner block with ()
iB           inner block with {}
Esc          exit visual mode
Ctrl + v     start visual block mode
>            shift text right
<            shift text left
y            yank (copy) marked text
d            delete marked text
~            switch case
```

### Cut and paste
```
yy           yank (copy) a line
2yy          yank (copy) 2 lines
yw           yank (copy) the characters of the word from the cursor position to the start of the next word
y$           yank (copy) to end of line
p            put (paste) the clipboard after cursor
P            put (paste) before cursor
dd           delete (cut) a line
2dd          delete (cut) 2 lines
dw           delete (cut) the characters of the word from the cursor position to the start of the next word
D            delete (cut) to the end of the line
d$           delete (cut) to the end of the line
d^           delete (cut) to the first non-blank character of the line
d0           delete (cut) to the begining of the line
x            delete (cut) character
```

### Search and replace
```
/pattern           search for pattern
?pattern           search backward for pattern
\vpattern          'very magic' pattern         non-alphanumeric characters are interpreted as special regex
n                  repeat search in same direction
N                  repeat search in opposite direction
%s/old/new/g       replace all old with new throughout file
%s/old/new/gc      replace all old with new throughout file with confirmations
noh                remove highlighting of search matches
```

### Search in multiple files
```
grep /pattern/ {file}        search for pattern in multiple files
cn                           jump to the next match
cp                           jump to the previous match
copen                        open a window containing the list of matches
```

### Working with multiple files
```
e file            edit a file in a new buffer
bnext or bn       go to the next buffer
bprev or bp       go to the previous buffer
bd                delete a buffer (close a file)
ls                list all open buffers
sp file           open a file in a new buffer and split window
vsp file          open a file in a new buffer and vertically split window
Ctrl + ws         split window
Ctrl + ww         switch windows
Ctrl + wq         quit a window
Ctrl + wv         split window vertically
Ctrl + wh         move cursor to the left window (vertical split)
Ctrl + wl         move cursor to the right window (vertical split)
Ctrl + wj         move cursor to the window below (horizontal split)
Ctrl + wk         move cursor to the window above (horizontal split)
```

### Tabs
```
tabnew or tabnew file       open a file in a new tab
Ctrl + wT                   move the current split window into its own tab
gt or tabnext or tabn       move to the next tab
gT or tabprev or tabp       move to the previous tab
<number>gt                  move to tab <number>
tabmove <number>            move current tab to the <number>th position (indexed from 0)
tabclose or tabc            close the current tab and all its windows
tabonly or tabo             close all tabs except for the current one
tabdo command               run the command on all tabs (e.g.         tabdo q closes all opened tabs)
```

# Vimium

### Navigation
```
?               Show the help dialog for a listing of all available keys
h               Scroll left
j               Scroll down
k               Scroll up
l               Scroll right
gg              Scroll to top of the page
G               Scroll to bottom of the page
d               Scroll down half a page
u               Scroll up half a page
H               go back in history
L               go forward in history
f               Open a link in the current tab
F               Open a link in a new tab
r               Reload
gs              View source
i               Enter insert mode -all commands will be ignored until you hit Esc to exit
yy              Copy the current URL to the clipboard
yf              Copy a link URL to the clipboard
gf              Cycle forward to the next frame
gF              Focus the main/top frame
o               Open URL, bookmark, or history entry
O               Open URL, bookmark, or history entry in a new tab
b               Open bookmark
B               Open bookmark in a new tab
```

### Tabs
```
J, gT           Go one tab left
K, gt           Go one tab right
g0              Go to the first tab
g$              Go to the last tab
^               Visit the previo­usl­y-v­isited tab
t               Create tab
yt              Duplicate current tab
x               Close current tab
X               Restore closed tab (i.e. unwind the 'x' command)
```

### Search
```
/               Enter find mode -type your search query and hit enter to search, or Esc to cancel
n               Cycle forward to the next find match
N               cycle backward to the previous find match
```


# Tmux

### Sessions
```
start new session                  tmux
start new session with name        tmux new -s sessionname
show running sessions              tmux ls
attach last session                tmux a
attach session by name             tmux a -t sessionname
kill session                       tmux kill-session -t sessionname
kill tmux-server                   tmux kill-server
```

### Windows
```
create new window                  Prefix c
rename current window              Prefix ,
list session windows               Prefix w
got to window with number          Prefix <NUMBER>
kill window                        Prefix &
```

### Panes
```
create horizontal split            Prefix %
create vertical split              Prefix "
Zoom In/Out in current pane        Prefix z
kill current pane                  Prefix x
go to next pane                    Prefix o
show pane numbers                  Prefix q
go to adjacent pane                Prefix <Arrow Key>
toggle pane layout                 Prefix <Space>
```

# NERDTree

### Files
```
o          open in prev window
go         preview
t          open in new tab
T          open in new tab silently
i          open split
gi         preview split
s          open vsplit
gs         preview vsplit
```
### Directories
```
o         open & close
O         recurs­ively open
x         close parent
X         close all children recurs­ively
e         explore selected dir
```
### Bookmarks
```
o         open bookmark
t         open in new tab
T         open in new tab silently
D         delete bookmark
```
### Filesystem
```
C          change tree root to selected dir
u          move tree root up a dir
U          move tree root up a dir but leave old root open
r          refresh cursor dir
R          refresh current root
m          Show menu
cd         change the CWD to the selected dir
CD         change tree root to CWD
```
### Tree navigation
```
p          go to parent
P          go to root
K          go to first child
J          go to last child
<C-­k>      go to prev sibling
<C-­j>      go to next sibling
```
### Tree filtering
```
I         hidden files (off)
f         file filters (on)
F         files (on)
B         bookmarks (off)
```
### Exiting commands
```
q         Close the NERDTree window
A         Zoom (maxim­ize­-mi­nimize) the NERDTree window
?         toggle help
```
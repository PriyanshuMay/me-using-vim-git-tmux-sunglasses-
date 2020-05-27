# **T**erminal **Mu**ltiple**x**er

## Sessions

### In Bash
```vim
- start new session:  tmux 
- start new session with name:  tmux new -s sessionname 
- show running sessions:  tmux ls 
- attach last session:  tmux a 
- attach session by name:  tmux a -t sessionname 
- kill session:  tmux kill-session -t sessionname 
- kill tmux-server:  tmux kill-server
``` 

### In Tmux
```vim
- Prefix is  Ctrl - b  by default
- create new session:  Prefix :new  and press Enter
- rename session:  Prefix $ 
- switch to previous session:  Prefix ( 
- switch to next session:  Prefix ) 
- list sessions and switch to selection:  Prefix s
```

## Windows
```vim
- create new window:  Prefix c 
- rename current window:  Prefix , 
- list session windows:  Prefix w 
- got to window with number:  Prefix <NUMBER>
- kill window:  Prefix &
```

## Panes
```vim
- create horizontal split:  Prefix % 
- create vertical split:  Prefix " 
- Zoom In/Out in current pane:  Prefix z 
- kill current pane:  Prefix x 
- go to next pane:  Prefix o 
- show pane numbers:  Prefix q 
- go to adjacent pane:  Prefix <Arrow Key> 
- toggle pane layout:  Prefix <Space>
```

### Resizing Panes
```vim
- you can access the Prompt by hitting:  Prefix : 
- resize windows:  resize-pane [DIRECTION] [NUMBER OF CELLS]
- Direons:  D U L R  (down, up, left, right)
- eg: resize-pane -L 30
```
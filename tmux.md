# tmux

tmux stands for Terminal MUltipleXer. It allows you to run several terminal sessions in one window.

## Resources

### man page

```bash
man tmux
```

### [wiki page on github](https://github.com/tmux/tmux/wiki)

## CLI Commands

### Start a new session

```bash
tmux
```

### Connect (attach) to existing session

```bash
tmux a
```

or if you know name of the session you want to connect to, you can specify it after `-t` flag

```bash
tmux a -t webapp
```

## What you can do after you launched tmux

### How to close tmux without losing your session

Hit <kbd>C-b</kbd> + <kbd>d</kbd> and tmux will save your session with all your opened and running windows and command, and after that close itself.

> NOTE: tmux sessions are saved on the disk, so after you shutdown or reboot your computer or server, there will be no tmux sessions open.

### Open new window

Hit <kbd>C-b</kbd> + <kbd>n</kbd>

### Switch between windows

 - <kbd>C-b</kbd> + <kbd>n</kbd> - switches to the next window
 - <kbd>C-b</kbd> + <kbd>p</kbd> - switches to the previous window

### Run tmux command

Hit <kbd>C-b</kbd> + <kbd>C-:</kbd>. This will open command prompt at the bottom where you can run [tmux commands](#tmux-commands).

## Tmux commands

### Kill focused window

Open command prompt and run `kill-window`

### Kill whole session

Open command prompt and run `kill-session`
## What is tmux?

Tmux is a "terminal multiplexer", it enables a number of terminals (or windows) to be accessed and controlled from a single terminal. It allows you to create a session on a remote box, run applications in that remote session, "detach" from the session, and re-"attach" when desired. It also has advanced features such as multiple windows and split views. Using tmux is recommend when running an interactive CLI program remotely. If you get disconnected from your session, you can re-attach as though nothing happened.

## Why tmux?

Tmux lets you run tasks persistently on remote box, so you can safely disconnect/detach and reconnect/reattach without interrupting these running tasks. It is powerful, extensible and can save more working time when combined with the shortcuts.

## Installation

Most platforms provide binary packages for tmux. Use the command below to install from binary.

```
# Debian, Ubuntu
$ sudo apt-get install tmux

# RHEL/CentOS/Fedora
$ sudo yum install tmux

# MacOS
$ brew install tmux
                    
```
===============================
# Tmux Shortcuts and Cheatsheet
===============================


**Table of contents**
* [General Usage](#general-usage)
* [Shortcuts](#shortcuts)
* [Commands](#commands)

General Usage
-------------

* Start a tmux session with
```
  tmux
```
* Select text in a tmux window with your mouse by holding the `SHIFT` key (Windows) or the `OPTIONS` key (Mac) and then using the mouse as you'd normally do

Shortcuts
---------

| Key(s)  | Description |
| :-----: | ----------- |
| `CTRL`+`b` `<command>` | sends `<command>` to tmux instead of sending it to the shell |
| | **General Commands** |
| `?` | shows a list of all commands (`q`closes the list) |
| `:` | enter a tmux command |
| | **Working with Windows** |
| `c` | creates a new window |
| `,` | rename current window |
| `p` | switch to previous window |
| `n` | switch to next window |
| `w` | list windows (and then select with arrow keys) |
| | **Working with Panes** |
| `%`          | split window vertically |
| `-`          | split window horizontally <br> requires `bind - split-window -v` in our `.tmux.conf` |
| →          | go to right pane |
| ←          | go to left pane |
| ↑          | go to upper pane |
| ↓          | go to lower pane |
| | **Working with Sessions** |
| `d` | detach from session |

Commands
--------

| Command | Description |
| ------- | ----------- |
| tmux -s <SESSION NAME> | creates a new session with name `<SESSION NAME>` |
| tmux list-sessions | lists all currently running tmux sessions |
| tmux attach -t <SESSION NAME> | attach to the session called `<SESSION NAME>` |

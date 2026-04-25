# TMUX-EZ
**`ez`** is a simple CLI tool for `tmux` users, it lets you copy or move files to another pane’s working directory without having to type the full path. Just prefix your usual commands with `ez` and you're good

---

## INSTALLATION

Simply clone the repo where your tpm plugins are located: 

`git clone https://github.com/NikhilC2209/tmux-ez.git ~/.config/tmux/plugins/tmux-ez` 

and add this directory to your $PATH: `export PATH=~/.config/tmux/plugins/tmux-ez:$PATH`

### ALTERNATIVELY
just download the `ez` binary into `/usr/bin/` directory and it should work just fine 

> [!NOTE]  
> I'll add support for tpm installation soon 👀

## ✨ What it does

Instead of manually figuring out where another pane is located in your filesystem, you can just run:

```bash
ez cp <file> %<pane_id>
ez mv <file> %<pane_id>
```

You can find a pane target with `tmux list-panes -a -F '#{pane_id} #{session_name}:#{window_index}.#{pane_index}'`.
If you're staying within the current window, `Prefix + q` shows pane indexes and you can target them with `session:window.pane`.

## SHOW PANE IDS

If you want the pane ID to always be visible inside tmux, add this to your `tmux.conf`:

```tmux
set -g pane-border-status top
set -g pane-border-format ' #{pane_id} #{session_name}:#{window_index}.#{pane_index} '
```

This will show labels like `%3 dev:2.0` in every pane border.
Use the `%<pane_id>` form with `ez` since it stays stable even when panes are opened, closed, or reordered.

## THINGS TO-DO

:white_check_mark: ~~Add an option to review path before executing the command, and `-f` flag to override it~~ Added a `--safe` flag to review command before executing it, disabled by default. 
- [ ] Add a simple help manual with some ASCII art
- [ ] Add supports for more commands
- [ ] Add support for plugin installation thru tpm
- [ ] A better way to copy or move files into write protected directories, right now user can overcome this by using `sudo -E ez cp file /`. But I'm not sure if it's the best way.

This plugin is still a work in progress, so feel free to open an issue if you find a bug or open a PR if you just want to contribute!😅 

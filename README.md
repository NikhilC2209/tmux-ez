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
ez cp <file> @<pane_id>
ez mv <file> @<pane_id>
```

You can easily find out the destination pane_id using `Prefix + q`

## THINGS TO-DO

- [ ] Add an option to review path before executing the command, and `-f` flag to override it
- [ ] Add a simple help manual with some ASCII art
- [ ] Add supports for more commands
- [ ] Add support for plugin installation thru tpm
- [ ] A better way to copy or move files into write protected directories, right now user can overcome this by using `sudo -E ez cp file /`. But I'm not sure if it's the best way.

This plugin is still a work in progress, so feel free to open an issue if you find a bug or open a PR if you just want to contribute!😅 

# TMUX-EZ
**`ez`** is a simple CLI tool for `tmux` users, it lets you copy or move files to another pane’s working directory without having to type the full path. Just prefix your usual commands with `ez` and you're good

---

## ✨ What it does

Instead of manually figuring out where another pane is located in your filesystem, you can just run:

```bash
ez cp <file> @<pane_id>
ez mv <file> @<pane_id>
```

You can easily find out the destination pane_id using `Prefix + q`

This plugin is still a work in progress, so feel free to open an issue if you find a bug or open a PR if you just want to contribute!😅 

<div align="center">

# termina

**a tui-style obsidian theme.**

sharp corners, bordered panels with labels, monospace everything.

</div>

---

## features

- 🖥️ every panel — editor, sidebars, status bar, command palette — drawn as a bordered box with a lowercase label, like panes in a terminal multiplexer
- ▪️ zero rounded corners, anywhere
- 🎨 neutral oklch grayscale palette with a purple accent, dark and light
- ⌨️ monospace throughout (`DM Mono`, falls back to `JetBrains Mono` / `Fira Code`)
- ⚙️ every knob lives at the top of `theme.css` — gap size, border thickness, font, label color

## install

### via obsidian (community themes)

not yet submitted to the community theme browser — use the manual method below for now.

### manual

clone or symlink this repo into your vault's theme folder:

```sh
git clone https://github.com/xevrion/obsidian-termina.git <your-vault>/.obsidian/themes/termina
```

or, to track updates via `git pull`:

```sh
ln -s /path/to/obsidian-termina <your-vault>/.obsidian/themes/termina
```

then restart obsidian and enable **termina** in **Settings → Appearance → Themes**.

### font

for the intended look, install [DM Mono](https://fonts.google.com/specimen/DM+Mono):

```sh
mkdir -p ~/.local/share/fonts/dm-mono && cd ~/.local/share/fonts/dm-mono
for f in DMMono-Light DMMono-LightItalic DMMono-Regular DMMono-Italic DMMono-Medium DMMono-MediumItalic; do
    curl -sLO "https://github.com/google/fonts/raw/main/ofl/dmmono/$f.ttf"
done
fc-cache -f
```

## customization

tweakable variables live at the top of `theme.css`:

| variable | what it does |
| --- | --- |
| `--termina-font` | font stack |
| `--gap` | spacing between panels |
| `--border-thickness` | panel border thickness |
| `--label-color` | panel label color |
| `--label-font-size` | panel label size |

colors are defined in the `.theme-dark` / `.theme-light` blocks — swap the `oklch()` values to retheme.

## license

[MIT](LICENSE)

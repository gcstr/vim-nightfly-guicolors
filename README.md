![nightfly](https://raw.githubusercontent.com/bluz71/misc-binaries/master/headings/nightfly.png)
==========

_nightfly_ is a dark GUI color scheme for Vim and Neovim heavily inspired by
Sarah Drasner's [Night Owl](https://github.com/sdras/night-owl-vscode-theme)
theme mixed with a dash of my own
[moonfly](https://github.com/bluz71/vim-moonfly-colors) theme.

Be aware, the _nightfly_ color scheme does incrementally change from time to
time, primarily with regard to language and plugin theming.

Color Palette
-------------

![palette](https://raw.githubusercontent.com/bluz71/misc-binaries/master/nightfly/nightfly-palette.png)

Prerequisites
-------------

_nightfly_ is a **GUI-only** Vim color scheme.

A GUI client, such as gvim, or a modern terminal version of Vim/Neovim with
`termguicolors` enabled in a true-color terminal, will be required. Details
about true-color terminals are listed below.

_nightfly_ explicitly does **not** support the 256 color `cterm` version of Vim
due to the number of custom colors required. 256 color terminals only allow 16
custom colors. I encourage terminal users to use a true-color terminal, such as:
[iTerm2](https://iterm2.com), [GNOME
Terminal](https://wiki.gnome.org/Apps/Terminal) or
[Alacritty](https://github.com/alacritty/alacritty), and enable the
`termguicolors` option.

Screenshots
-----------

### Ruby

<img width="800" alt="ruby" src="https://raw.githubusercontent.com/bluz71/misc-binaries/master/nightfly/ruby_nightfly.png">

### JavaScript

<img width="800" alt="javascript" src="https://raw.githubusercontent.com/bluz71/misc-binaries/master/nightfly/javascript_nightfly.png">

The font in use is [Iosevka](https://github.com/be5invis/Iosevka).

Languages explicitly styled
---------------------------

- All Neovim Treesitter highlighted-languages
- C/C++
- Clojure
- CoffeeScript
- Crystal
- Elixir
- Elm
- Dart
- Go
- Haskell
- Java
- [JavaScript](https://github.com/pangloss/vim-javascript)
- Lua
- Markdown
- PHP
- PureScript
- Python
- Ruby
- Rust
- Scala
- Shell
- [TypeScript](https://github.com/HerringtonDarkholme/yats.vim)

Plugins explicity styled
------------------------

- [ALE](https://github.com/w0rp/ale)
- [barbar.nvim](https://github.com/romgrk/barbar.nvim)
- [BufExplorer](https://github.com/jlanzarotta/bufexplorer)
- [clever-f](https://github.com/rhysd/clever-f.vim)
- [CtrlP](https://github.com/ctrlpvim/ctrlp.vim)
- [fern.vim](https://github.com/lambdalisue/fern.vim)
- [fzf.vim](https://github.com/junegunn/fzf.vim) (with matching [fly16](https://github.com/bluz71/fly16-bat) [bat](https://github.com/sharkdp/bat) theme)
- [GitGutter](https://github.com/airblade/vim-gitgutter)
- [gitsigns.nvim](https://github.com/lewis6991/gitsigns.nvim)
- [indentLine](https://github.com/Yggdroot/indentLine)
- [NERDTree](https://github.com/scrooloose/nerdtree)
- [nvim-tree.lua](https://github.com/kyazdani42/nvim-tree.lua)
- [Signify](https://github.com/mhinz/vim-signify)
- [telescope.nvim](https://github.com/nvim-telescope/telescope.nvim)
- [Tagbar](https://github.com/majutsushi/tagbar)

Installation
------------

Use your favoured plugin manager to install **bluz71/vim-nightfly-guicolors**
then set the colorscheme in your initialization file.

If using [vim-plug](https://github.com/junegunn/vim-plug) do the following:

1. Add `Plug 'bluz71/vim-nightfly-guicolors'` to your initialization file
2. Run `:PlugInstall`
3. Add `colorscheme nightfly` to your initialization file, make sure this line
   appears **after** the _Plug_ declaration.

Status line
-----------

The _nightfly_ color scheme supports
[lightline.vim](https://github.com/itchyny/lightline.vim). To enable the
_nightfly_ lightline colorscheme, after the _lightline.vim_ plugin has been
installed, please add the following to your initialization file:

```viml
let g:lightline = { 'colorscheme': 'nightfly' }
```

The _nightfly_ color scheme also supports
[vim-airline](https://github.com/vim-airline/vim-airline). With modern versions
of _vim-airline_ the _nightfly_ theme will be automatically loaded.

Alternatively,
[vim-moonfly-statusline](https://github.com/bluz71/vim-moonfly-statusline) is
available for those that want a simple yet informative status line. After the
_vim-moonfly_statusline_ plugin has been installed, please add the following to
your initialization file:

```viml
let g:moonflyIgnoreDefaultColors = 1
```

This option will tell _moonfly-statusline_ to not use the default
[moonfly](https://github.com/bluz71/vim-moonfly-colors) colors of that plugin,
but instead use the specified `statusline` colors defined by this _nightfly_
color scheme.

Options
-------

The `g:nightflyCursorColor` option specifies whether to color the cursor or not.
By default the cursor will **NOT** be colored. If you prefer a colored cursor
then add the following to your initialization file:

```viml
let g:nightflyCursorColor = 1
```

The `g:nightflyTerminalColors` option specifies whether to use the nightfly
color palette in `:terminal` windows when `termguicolors` is set. By default
this option is **enabled**. If you prefer not to use the nightfly color palette
for the first 16 terminal colors then add the following to your initialization
file:

```viml
let g:nightflyTerminalColors = 0
```

The `g:nightflyUnderlineMatchParen` option specifies whether to underline
matching parentheses. By default this option is **disabled**. If you want to
underline matching parentheses then add the following to your initialization
file:

```viml
let g:nightflyUnderlineMatchParen = 1
```

The `g:nightflyUndercurls` option specifies whether to use undercurls for
spelling and linting errors in GUI versions of Vim, including terminal Vim with
`termguicolors` set. By default this option is **enabled**. If you do not like
the appearance of undercurls then add the following to your initialization file:

```viml
let g:nightflyUndercurls = 0
```

The `g:nightflyItalics` option specifies whether to use italics for comments and
certain HTML elements in GUI versions of Vim. By default this option is
**enabled**. If you do not like the appearance of italics then add the following
to your initialization file:

```viml
let g:nightflyItalics = 0
```

The `g:nightflyTransparent` option specifies whether to use an opaque or
transparent background in GUI versions of Vim. By default this option is
**disabled**. If you would like a transparent background then add the following
to your initialization file:

```viml
let g:nightflyTransparent = 1
```

The `g:nightflyNormalFloat` option specifies whether to use nightfly background
and foreground colors in Neovim floating windows. By default this options is
**disabled**, hence, Neovim floating windows will usually be styled with popup
menu colors. If you would like to use nightfly colors instead then add the
following to your configuration:

```viml
let g:nightflyNormalFloat = 1
```

The `g:nightflyVertSplits` option specifies whether to show vertical panel
separators. By default they will be visible, setting it to 0 will make them 
the same color as the background.

```viml
let g:nightflyVertSplits = 0
```

:bulb: If the above option is set then it is highly recommended to enable
floating window borders to distinguish between the edit and floating windows in
Neovim's LSP client, for example:

```lua
  vim.lsp.handlers['textDocument/hover'] = vim.lsp.with(
    vim.lsp.handlers.hover, {
      border = 'single'
    }
  )
  vim.lsp.handlers['textDocument/signatureHelp'] = vim.lsp.with(
    vim.lsp.handlers.signatureHelp, {
      border = 'single'
    }
  )
  local opts = {noremap = true, silent = true}
  vim.api.nvim_buf_set_keymap(0, 'n', ']d', '<cmd>lua vim.lsp.diagnostic.goto_next({severity_limit = "Warning", popup_opts = {border = "single"}})<CR>', opts)
  vim.api.nvim_buf_set_keymap(0, 'n', '[d', '<cmd>lua vim.lsp.diagnostic.goto_prev({severity_limit = "Warning", popup_opts = {border = "single"}})<CR>', opts)
```

True Color Terminals
--------------------

Many modern terminals support [24-bit true
colors](https://gist.github.com/XVilka/8346728). Current versions of Vim and
Neovim on such terminals support true colors when `set termguicolors` is
enabled.

A list of popular terminals that support true colors:

- [iTerm2](http://www.iterm2.com)
- [GNOME Terminal](https://wiki.gnome.org/Apps/Terminal)
- [Windows Terminal](https://github.com/Microsoft/Terminal)
- [Alacritty](https://github.com/alacritty/alacritty)
- [kitty](https://sw.kovidgoyal.net/kitty/index.html)
- [konsole](https://konsole.kde.org)
- [PuTTY](https://putty.org)
- [mintty](https://mintty.github.io)

On terminals that support true colors, and when `termguicolors` is set, the
_nightfly_ color scheme will emit the correct theme colors.

For the _nightfly_ color scheme to display correctly inside _tmux_ the following
setting will usually be required in _~/.tmux.conf_:

```
set -ga terminal-overrides ',xterm-256color:Tc'
```

Vim, as against Neovim, inside _tmux_, will also require the following setting
be added to initialization file:

```viml
let &t_8f = "\<Esc>[38;2;%lu;%lu;%lum"
let &t_8b = "\<Esc>[48;2;%lu;%lu;%lum"
```

Terminal Themes
---------------

A collection of _nightfly_-flavoured terminal themes are provided:

- _iTerm2_ users on macOS can import
  [this](terminal_themes/nightfly.itermcolors) color scheme

- _GNOME Terminal_ users can run
  [this](terminal_themes/gnome-terminal-nightfly.sh) script to create a
  _Nightfly_ profile. Before executing the script, please install the
  `dconf-cli` command line utility for modern versions of Gnome (3.28 and
  later), for example `sudo apt install dconf-cli`. After executing the script,
  please set the _cursor_ and _selection_ colors by hand, with the appropriate
  color values listed below, in `Preferences` / `Nightfly` / `Colors`.

- [Alacritty](https://github.com/alacritty/alacritty) users can copy
  [this](terminal_themes/alacritty.yml) theme into their `alacritty.yml`
  configuration.

- [kitty](https://sw.kovidgoyal.net/kitty) users can use
  [this](terminal_themes/kitty-theme.conf) theme

For other terminals please configure appropriately with the following colors:

| Type           | Category        | Value     | Color                                                       |
|----------------|-----------------|-----------|-------------------------------------------------------------|
| Background     | Background      | `#011627` | ![background](https://via.placeholder.com/32/011627?text=+) |
| Foreground     | Foreground      | `#acb4c2` | ![background](https://via.placeholder.com/32/acb4c2?text=+) |
| Bold           | Bold            | `#eeeeee` | ![background](https://via.placeholder.com/32/eeeeee?text=+) |
| Cursor         | Cursor          | `#9ca1aa` | ![background](https://via.placeholder.com/32/9ca1aa?text=+) |
| Cursor Text    | Cursor Text     | `#080808` | ![background](https://via.placeholder.com/32/080808?text=+) |
| Selection      | Selection       | `#b2ceee` | ![background](https://via.placeholder.com/32/b2ceee?text=+) |
| Selection Text | Selection Text  | `#080808` | ![background](https://via.placeholder.com/32/080808?text=+) |
| Color 1        | Black (normal)  | `#1d3b53` | ![background](https://via.placeholder.com/32/1d3b53?text=+) |
| Color 2        | Red (normal)    | `#fc514e` | ![background](https://via.placeholder.com/32/fc514e?text=+) |
| Color 3        | Green (normal)  | `#a1cd5e` | ![background](https://via.placeholder.com/32/a1cd5e?text=+) |
| Color 4        | Yellow (normal) | `#e3d18a` | ![background](https://via.placeholder.com/32/e3d18a?text=+) |
| Color 5        | Blue (normal)   | `#82aaff` | ![background](https://via.placeholder.com/32/82aaff?text=+) |
| Color 6        | Purple (normal) | `#c792ea` | ![background](https://via.placeholder.com/32/c792ea?text=+) |
| Color 7        | Cyan (normal)   | `#7fdbca` | ![background](https://via.placeholder.com/32/7fdbca?text=+) |
| Color 8        | White (normal)  | `#a1aab8` | ![background](https://via.placeholder.com/32/a1aab8?text=+) |
| Color 9        | Black (bright)  | `#7c8f8f` | ![background](https://via.placeholder.com/32/7c8f8f?text=+) |
| Color 10       | Red (bright)    | `#ff5874` | ![background](https://via.placeholder.com/32/ff5874?text=+) |
| Color 11       | Green (bright)  | `#21c7a8` | ![background](https://via.placeholder.com/32/21c7a8?text=+) |
| Color 12       | Yellow (bright) | `#ecc48d` | ![background](https://via.placeholder.com/32/ecc48d?text=+) |
| Color 13       | Blue (bright)   | `#82aaff` | ![background](https://via.placeholder.com/32/82aaff?text=+) |
| Color 14       | Purple (bright) | `#ae81ff` | ![background](https://via.placeholder.com/32/ae81ff?text=+) |
| Color 15       | Cyan (bright)   | `#7fdbca` | ![background](https://via.placeholder.com/32/7fdbca?text=+) |
| Color 16       | White (bright)  | `#d6deeb` | ![background](https://via.placeholder.com/32/d6deeb?text=+) |

License
-------

[MIT](https://opensource.org/licenses/MIT)

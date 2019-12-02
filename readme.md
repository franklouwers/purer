# Purer

> Pretty one-line ZSH prompt based on [@sindresorhus](https://github.)'s [Pure](https://github.com/sindresorhus/pure)

![purer](https://cloud.githubusercontent.com/assets/583202/25418314/c3a29bfa-2a18-11e7-8a6f-4c0960ccadfc.png)

It is based on [purer](https://github.com/DFurnes/purer) but adds support for [`kube-ps1`](https://github.com/jonmosco/kube-ps1) as an `RPROMPT`.

## Install

Requires Git 2.0.0+ and ZSH 5.2+. Older versions of ZSH are known to work, but they are **not** recommended.

1. I don't care. Install it with whatever tools you want. No hipster-style `npm --global` installation or other bullshit included.

2. Symlink `pure.zsh` to somewhere in [`$fpath`](http://www.refining-linux.org/archives/46/ZSH-Gem-12-Autoloading-functions/) with the name `prompt_pure_setup`.

3. Install [`zsh-async`](https://github.com/mafredri/zsh-async) if it's not installed already.

#### Example

For a user-specific installation (which would not require escalated privileges), simply add a directory to `$fpath` for that user:

```sh
# .zshenv or .zshrc
fpath=( "$HOME/.zfunctions" $fpath )
```

Then install the theme there:

```console
$ ln -s "$PWD/pure.zsh" "$HOME/.zfunctions/prompt_pure_setup"
```

See [Pure's readme](https://github.com/sindresorhus/pure/blob/master/readme.md#install) for more detailed instructions.

## Customization

Purer supports customization using [Pure's environment variables](https://github.com/sindresorhus/pure#options), plus:

### `PURE_PROMPT_SYMBOL_COLOR`

Defines the prompt symbol color. The default value is `magenta`; you can use any [colour name](https://wiki.archlinux.org/index.php/Zsh#Colors) or [numeric colour code](https://upload.wikimedia.org/wikipedia/commons/1/15/Xterm_256color_chart.svg) (see `zshzle(1)` section [Character Highlighting](http://zsh.sourceforge.net/Doc/Release/Zsh-Line-Editor.html#Character-Highlighting).)


### `PURE_PROMPT_PATH_FORMATTING`

Defines how to display the path. Default value: `%c`. See [Prompt Expansion](http://zsh.sourceforge.net/Doc/Release/Prompt-Expansion.html) for more.


## License

Purer MIT © [David Furnes](http://dfurnes.com) <br/>
Pure MIT © [Sindre Sorhus](http://sindresorhus.com)

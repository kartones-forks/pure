
Simplified fork of [pure](https://github.com/sindresorhus/pure).

# Minimal Installation

## 1. Add the files

```bash
mkdir -p "$HOME/.zsh/pure"
cd "$HOME/.zsh/pure"
```

Copy `pure.zsh` and `async.zsh` to this directory, then create symlinks (required for `autoload` and `prompt` to find them):

```bash
ln -s pure.zsh prompt_pure_setup
ln -s async.zsh async
```

## 2. Add to `~/.zshrc`

```bash
fpath+=($HOME/.zsh/pure)

autoload -U promptinit
promptinit
prompt pure
```

## 3. Reload shell

```bash
exec zsh
```



## Extra: Changes

- `PURE_CMD_MAX_EXEC_TIME`: Default 10 seconds
- `PURE_GIT_PULL`: Disabled by default
- `PURE_EXEC_TIME_DISABLED`: New flag, to not report execution time. Disabled by default
- One-liner
- branch displayed between parenthesis
- Some default colors changed
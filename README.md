<h2 align="center">
  <a href="https://github.com/z-shell/zi">
    <img src="https://github.com/z-shell/zi/raw/main/docs/images/logo.svg" alt="Logo" width="80" height="80">
  </a>
❮ ZI ❯ Package - Zsh-bin
</h2>

<h2 align="center">

| **Package source:** | Source Tarball | Binary |              Git             | Node | Gem |
| :-----------------: | :------------: | :----: | :--------------------------: | :--: | :-: |
|     **Status:**     |      :x:       |  :x:   | :heavy_check_mark: (default) | :x:  | :x: |

</h2>

> This repository compatible with [ZI](https://github.com/z-shell-zi)

[ZI](https://github.com/z-shell/zi) can use a `package.json`
(similar in construct to the one used in `npm` packages) to automatically:

- get the plugin's Git repository OR release-package URL,
- get the list of the recommended ices for the plugin,
  - there can be multiple lists of ices,
  - the ice lists are stored in _profiles_; there's at least one profile, _default_,
  - the ices can be selectively overridden.

The package provides the [romkatv/zsh-bin](https://github.com/romkatv/zsh-bin) statically-linked, hermetic, relocatable Zsh
## Install

### Available `pack''` invocations

```zsh
zi pack for zsh-bin
```

## Default profile

**Requires **sudo** to install Zsh to /usr/local and will attempt to register it as a login shell.

```zsh
zi lucid as"null" depth"1" \
  atclone"./install -e yes -d /usr/local" \
  atpull"%atclone" nocompile nocompletions \
  for @romkatv/zsh-bin
```

## Rootless profile

Does not require **root**, will install to ~/.local.

```zsh
zi lucid as"null" depth"1" \
  atclone"./install -e no -d ~/.local" \
  atpull"%atclone" nocompile nocompletions \
  for @romkatv/zsh-bin
```

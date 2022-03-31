<div align="center"><table style="width:100%;height:auto">
<tr><td align="center">
<a title="ZI" target="_self" href="https://github.com/z-shell/zi/">
  <img align="center" style="width:60px;height:auto" src="https://github.com/z-shell/zi/raw/main/docs/images/logo.svg" alt="ZI Logo" /></a>
<h2> ❮ ZI ❯ Package - Zsh bin </h2><h3> Package of statically-linked, hermetic, relocatable - romkatv/zsh-bin </h3>
</td></tr>
<tr><td align="center"><h3>
  
| **Package source:** | Source Tarball | Binary |              Git             | Node | Gem |
| :-----------------: | :------------: | :----: | :--------------------------: | :--: | :-: |
|     **Status:**     |      :x:       |  :x:   | :heavy_check_mark: (default) | :x:  | :x: |

</h3>
  <img style="width:90%;height:auto" 
       src="https://user-images.githubusercontent.com/59910950/161060980-8bc70578-e086-4a51-8cd4-ed3d7289f216.gif" alt="Preview" />
</td></tr></table></div>
  
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

---

> This repository compatible with [ZI](https://github.com/z-shell-zi)

[ZI](https://github.com/z-shell/zi) can use a `package.json`
(similar in construct to the one used in `npm` packages) to automatically:

- get the plugin's Git repository OR release-package URL,
- get the list of the recommended ices for the plugin,
  - there can be multiple lists of ices,
  - the ice lists are stored in _profiles_; there's at least one profile, _default_,
  - the ices can be selectively overridden.

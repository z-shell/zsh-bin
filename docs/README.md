<div align="center" width="100%"><table>
  <tr><td align="center"><a href="https://github.com/z-shell/zi">
    <img src="https://github.com/z-shell/zi/raw/main/docs/images/logo.svg" alt="Logo" width="60" height="60" />
    </a>
<h2> ❮ ZI ❯ Package - Statically-linked, hermetic, relocatable Zsh </h2>
</tr></td><tr><td align="center"><h2>
  
| **Package source:** | Source Tarball | Binary |              Git             | Node | Gem |
| :-----------------: | :------------: | :----: | :--------------------------: | :--: | :-: |
|     **Status:**     |      :x:       |  :x:   | :heavy_check_mark: (default) | :x:  | :x: |

</h2>
  <img src="https://user-images.githubusercontent.com/59910950/161060980-8bc70578-e086-4a51-8cd4-ed3d7289f216.gif" alt="Logo" width="auto" height="440" />
</td></tr></table></div>
  
The package provides the [romkatv/zsh-bin](https://github.com/romkatv/zsh-bin) statically-linked, hermetic, relocatable Zsh

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

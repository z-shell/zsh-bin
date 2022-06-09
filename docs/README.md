<table align="center"><tr><td>
<h1 align="center">
  <p><a target="_self" href="https://github.com/z-shell/zi/">
    <img align="center" src="https://github.com/z-shell/zi/raw/main/docs/images/logo.svg" width="60px" height="60px" alt="ZI Logo" /></a>
    ❮ ZI ❯ Package - Zsh Bin </p>
</h1>
<h2 align="center">
  <p> Package of statically-linked, hermetic, relocatable - <a target="_self" href="https://github.com/romkatv/zsh-bin">romkatv/zsh-bin</a></p>
</h2>
<h3 align="center">
<table>
    <tr>
        <td><b>Package source:</b></td>
        <td>Source Tarball</td>
        <td>Binary</td>
        <td>Git</td>
        <td>Node</td>
        <td>Gem</td>
    </tr>
    <tr>
        <td><b>Status:</b></td>
        <td>❌</td>
        <td>❌</td>
        <td>✔️ (default)</td>
        <td>❌</td>
        <td>❌</td>
    </tr>
</table></h3>
  <p><img align="center" src="https://user-images.githubusercontent.com/59910950/161060980-8bc70578-e086-4a51-8cd4-ed3d7289f216.gif" width="100%" height="auto" alt="zi package zsh static bin" /></p>
</td></tr></table><hr />

## Available `pack''` invocations

```zsh
zi pack for zsh-bin
```

### Default profile

<b>Requires sudo</b> to install Zsh to /usr/local and will attempt to register it as a login shell.

```shell
zi lucid for as"null" depth"1" \
  atclone"./install -e yes -d /usr/local" \
  atpull"%atclone" nocompile nocompletions \
    @romkatv/zsh-bin
```

### Rootless profile

Does not require <b>root</b>, will install to ~/.local.

```shell
zi lucid for as"null" depth"1" \
  atclone"./install -e no -d ~/.local" \
  atpull"%atclone" nocompile nocompletions \
    @romkatv/zsh-bin
```

---

> This repository compatible with [ZI](https://github.com/z-shell-zi)

The [romkatv/zsh-bin](https://github.com/romkatv/zsh-bin) zsh package that uses the [zsh-string-lib](https://github.com/z-shell/zsh-string-lib) to automatically:

- get the plugin's Git repository OR release-package URL,
- get the list of the recommended ices for the plugin,
  - there can be multiple lists of ices,
  - the ice lists are stored in _profiles_; there's at least one profile, _default_,
  - the ices can be selectively overridden.

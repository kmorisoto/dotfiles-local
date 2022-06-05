# dotfiles-local

設定を変えたらをすればとりあえず反映される。

```shell
rcup
zsh
```

# 以下、初期設定

https://github.com/kmorisoto/dotfiles

```shell
ghq get https://github.com/kmorisoto/dotfiles.git
ln -s ~/ghq/github.com/kmorisoto/dotfiles
```

上記のREADMEを読みつつ設定する。

# 必要なもの

```shell
brew install gh
```

```shell
brew install peco
```

# git

```shell
vim gitconfig.local.secret
```

以下を埋める

```shell
[user]
  name = xxx
  email = xxx
```

## 複数のGitHubアカウントを使う場合

### subアカウント用のgitconfigを作る。

```shell
[user]
  name = xxx
  email = xxx
```

### giconfig.local.secretに以下を追記する。

```
[includeIf "gitdir:~/ghq/github.com/xxx/**"]
  path = ~/.gitconfig_xxx
```

# zsh

```shell
vim zshrc.local.secret
```

oh-my-zsh

```shell
ghq get https://github.com/ohmyzsh/ohmyzsh.git
ln -s ~/ghq/github.com/ohmyzsh/ohmyzsh ~/.oh-my-zsh
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc.local.omz
```

```shell
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

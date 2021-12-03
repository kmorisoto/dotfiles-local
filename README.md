# dotfiles-local

設定を変えたらをすればとりあえず反映される。

```shell
rcup
zsh
```

# 以下、初期設定

https://github.com/thoughtbot/dotfiles.git

```shell
ghq get https://github.com/thoughtbot/dotfiles.git
ln -s ~/ghq/github.com/thoughtbot/dotfiles
```

上記のREADMEを読みつつ設定する。

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

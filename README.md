# lunarvim-config
## Installing zsh

First install `zsh`:
```bash
sudo apt update
sudo apt install zsh -y
```
Then install `oh-my-zsh`:
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
Now set `zsh` as your default shell by change shell command:
```bash
chsh -s $(which zsh)
```


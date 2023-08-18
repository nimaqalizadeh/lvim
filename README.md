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
Restart your pc.


## Recommended fonts
+ My preferred nerd font is [FiraCode](https://www.nerdfonts.com/font-downloads)
  Download Fira code, then install it:
  
```bash
unzip FiraCode.zip -d FiraCode
sudo mv FiraCode /usr/share/fonts/truetype
```
Now close your terminal and open it again, then:

+ `settings` > `Manage Profile` > `Profiles` > `+ New` > `Appearance` > `Choose`
choose `FiraCode Nerd Font Mono` ,
then set `Profile` as Default.

Close Terminal and open it again
# Installing Neovim
## Installing from download
Download stable release for linux nvim.linux64.tar.gz

```bash
mkdir ~/.local/bin
mv nvim-linux64.tar.gz ~/.local/bin
tar xzvf nvim-linux64.tar.gz
ln -s ./nvim-linux64/bin/nvim ./nvim
````
Add ~/.local/bin to PATH

```bash
vi ~/.zshrc
```
Add to path and exit vi

```bash
export PATH="$PATH:$HOME/.local/bin"
```
and then:
```bash
source .zshrc
```
So if type `nvim -version` you see this:
```bash
NVIM v0.9.1
Build type: Release
LuaJIT 2.1.0-beta3
```

# LunarVim Installation
The installation guide is [here](https://www.lunarvim.org/docs/installation)
## Prerequisites

Make sure you have installed the latest version of Neovim v0.9.0+.

Have `git`, `make`, `pip`, `python`, `npm`, `node` and `cargo` installed on your system. Check them by `which` command

For installing `make` use
```bash
sudo apt install build-essential
```
For installing `node` and `npm` use [nvm](https://github.com/nvm-sh/nvm):
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.4/install.sh | bash
#to verify nvm has been installed
command -v nvm
#the output should be `nvm`
node --version
sudo apt install nodejs npm
```

Resolve [EACCES permissions when installing packages globally](https://docs.npmjs.com/resolving-eacces-permissions-errors-when-installing-packages-globally) to avoid error when installing packages with npm.

Now install Lunarvim:
```bash
LV_BRANCH='release-1.3/neovim-0.9' bash <(curl -s https://raw.githubusercontent.com/LunarVim/LunarVim/release-1.3/neovim-0.9/utils/installer/install.sh)
```
After that clone the confing and put them in `~/.config/lvim`.

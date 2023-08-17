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




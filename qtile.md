# the qtile config

## packages

```bash
sudo pacman -S qtile alacritty code firefox rofi which nitrogen pulseaudio pavucontrol pamixer arandr udiskie ntfs-3g network-manager-applet volumeicon cbatticon xorg-xinit git thunar ranger gvfs lxappearance geeqie vlc brightnessctl pacman-contrib python-psutil python-pip neofetch htop btop lsd bat playerctl xclip papirus-icon-theme maim ueberzug dunst libnotify calcurse figlet ttf-jetbrains-mono xdotool neovim zsh
```

## yay

```bash
mkdir ~/work
cd ~/work
git clone https://aur.archlinux.org/yay.git && cd yay && makepkg -si
```

install the yay things

```bash
yay -S qtile-extras-git picom-ftlabs-git ttf-ubuntu-mono-nerd ttf-meslo-nerd ttf-cascadia-code-nerd material-gtk-theme-git material-icon-theme-git unimatrix-git pipes.sh cava-git shell-color-scripts tty-clock 
```

## ohmyzsh

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

powerlevel10k zsh plugin

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

Set `ZSH_THEME="powerlevel10k/powerlevel10k"` in `~/.zshrc`

zsh-syntax-highlighting, zsh-autosuggestions plugin

```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

enable plugin in zshrc

```bash
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
```

other config

```bash
alias ls="lsd"
alias cat="bat"
colorscript -e panes 
```

## grub theme

```bash
cd ~/work
git clone https://github.com/sandesh236/sleek--themes
cd sleek--themes/Sleek\ theme-dark
sudo ./install.sh
```

## sddm theme

```bash
yay -S sddm-theme-catppuccin
```

change sddm theme

```bash
sudo mkdir /etc/sddm.conf.d
sudo vim /etc/sddm.conf.d/theme.conf
```

```bash
[Theme]
Current=catppuccin-mocha
```

## rofi theme

```bash
sudo cp .config/qtile/rofi/theme/minimal.rasi /usr/share/rofi/themes/
sudo cp .config/qtile/rofi/theme/material.rasi /usr/share/rofi/themes/
```

## fonts for rofi power menu

```bash
sudo cp ~/.config/qtile/rofi/fonts/GrapeNuts-Regular.ttf /usr/share/fonts/TTF
sudo cp ~/.config/qtile/rofi/fonts/Icomoon-Feather.ttf /usr/share/fonts/TTF
sudo cp ~/.config/qtile/rofi/fonts/Iosevka-Nerd-Font-Complete.ttf /usr/share/fonts/TTF
```

## theme

the aviable temes are in .config/qtile/themes you can change the system theme in .config/qtile/config.json

```bash
vim .config/qtile/config.json
```

## 软件配置

参考： [Software Config](SoftwareConfig)

## 桌面配置

https://typecraft.dev/hyprland-for-newbs
https://www.youtube.com/watch?v=omhJMH9lPPc&ab_channel=typecraft
### 1. 安装stow(symlink farm manager)

```shell
yay -S stow
```

### 2. clone dotfiles
```shell
cd ~
git clone https://github.com/typecraft-dev/dotfiles
```

### 3. hyprpaper

```shell
yay -S --needed hyprpaper
cd ~/dotfiles
stow hyprpaper
stow backgrounds
```

### 4. waybar
https://github.com/Alexays/Waybar
https://github.com/catppuccin/waybar

```shell
cd ~/dotfiles
killall waybar
rm ~/config/waybar/*
stow waybar
waybar &
```

### 5. hyprlock

```shell
yay -S hyprlock
cd ~/dotfiles
rm ~/config/hypr/hyprlock.conf
stow hyprlock
stow hyprmocha
```

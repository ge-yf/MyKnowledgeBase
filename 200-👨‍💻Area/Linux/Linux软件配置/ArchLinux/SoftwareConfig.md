
## UI显示模糊问题
### Obsidian

```shell
cp /usr/share/applications/obsidian.desktop ~/.local/share/applications

nvim ~/.local/share/applications/obsidian.desktop

# 修改Exec,后面追加：
Exec=/usr/bin/obsidian %U --enable-features=UseOzonePlatform --ozone-platform=wayland --enable-wayland-ime
```

### Chrome

```shell
nvim ~/.config/chrome-flags.conf

# 添加如下内容：
--enable-features=UseOzonePlatform
--ozone-platform=wayland
--enable-wayland-ime
```

### VSCode

```shell
nvim ~/.config/code-flags.conf

# 添加如下内容：
--ozone-platform-hint=wayland
--enable-wayland-ime
```

### XWayland Applications

确认App是否为xwayland程序：
运行App后，终端输入`hyprctl clients`查看该App的`xwayland`字段，为1就是XWayland。

```shell
nvim .config/hypr/hyprland.conf

#  在monitor下面添加如下内容：
xwayland {
  force_zero_scaling = true
}

echo Xft.dpi:144 | xrdb -merge
```



## Obsidian

### UI显示模糊问题

```shell
cp /usr/share/applications/obsidian.desktop ~/.local/share/applications

nvim ~/.local/share/applications/obsidian.desktop

# 修改Exec,后面追加：
Exec=/usr/bin/obsidian %U --enable-features=UseOzonePlatform --ozone-platform=wayland --enable-wayland-ime
```

## Chrome

### UI显示模糊问题

```shell
nvim ~/.config/chrome-flags.conf

# 添加如下内容：
--enable-features=UseOzonePlatform
--ozone-platform=wayland
--enable-wayland-ime
```

## VSCode

### UI显示模糊问题

```shell
nvim ~/.config/code-flags.conf

# 添加如下内容：
--ozone-platform-hint=wayland
--enable-wayland-ime
```

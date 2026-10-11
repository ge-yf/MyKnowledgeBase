## 1. 连接网线或WIFI

### WIFI
```shell
iwctl
station wlan0 get-networks
station wlan0 connect XXX
```

ping www.baidu.com
如果能ping通，说明连接成功
## 2. archinstall

```shell
archinstall
```

1. language默认English
2. Mirrors 选China
3. Locales默认
4. Disk configuration 选择指定硬盘
5. Disk encryption 不动
6. Bootloader设定Systemd-boot
7. Unfied Kernel images False
8. Swap True
9. hostname设定电脑名
10. root password设定root密码
11. User account添加一个用户
12. Profile  -> Type -> Desktop -> Hyprland
13. Profile  -> Graphics driver -> 选择对应的显卡驱动
14. Profile  -> Greeter -> 选择sddm
15. Audio -> Pipewire
16. Kernels -> linux-zen
17. Additional packages
18. Time Zone选Asia/Shanghai
19.  Network configuration -> Use NetworkManager
20. Optional repositories -> multilib
21. 选择`Install`，等待安装完成，选择`yes`。
22. 输入`exit`。
23. 输入`reboot`重启系统。

## 3. 初次软件安装

1. Session选择`Hyprland`。
2. 输入安装时设置的密码，进入桌面。
3. `win+Q`打开kitty终端。
4. 连接WIFI:
```shell
nmcli dev wifi list
nmcli --ask dev wifi connect XXX_WIFI_NAME password XXXX
```
5. 修改源：
```shell
sudo vim /etc/pacman.d/mirrorlist

# 保留mirrors.tuna.tsinghua.edu.cn, mirrors.aliyun.com, mirrors.ustc.edu.cn,其余删掉后，保存退出

sudo pacman -Syyu
```
6. 追加archlinuxcn
```shell
sudo vim /etc/pacman.conf

# 末尾追加如下内容
[archlinuxcn]
SigLevel = Optional TrustedOnly
Server = https://mirrors.tuna.tsinghua.edu.cn/archlinuxcn/$arch
Server = https://mirrors.ustc.edu.cn/archlinuxcn/$arch
Server = https://mirrors.aliyun.com/archlinuxcn/$arch

# 保存退出后，输入如下命令

sudo pacman -Sy archlinuxcn-keyring
```
7. 安装必备yay和工具链
```shell
sudo pacman -Sy yay base-devel
```
8. 安装中文字体
```shell
sudo pacman -S noto-fonts noto-fonts-cjk noto-fonts-extra noto-fonts-emoji ttf-dejavu ttf-liberation
```
9. 安装输入法
```shell
sudo pacman -S fcitx5-im fcitx5-rime

# 安装完毕后 win+R 启动输入法设置
```
10. 安装字体
```shell
# XXX为字体文件
cp XXX ~/.local/share/fonts/
fc-cache
```
11. 安装zsh
        参考： [zsh](zsh)
## 挂代理

### 代理软件
1. https://github.com/v2ray/v2ray-core
2.  https://github.com/Qv2ray/Qv2ray
3. https://justmysocks1.net/

### 终端配置
```shell
vim ~/.zshrc

# proxy setting
export http_proxy=http://localhost:8889
export https_proxy=http://localhost:8889
export all_proxy=socks5://localhost:1089

source .zshrc
```


## 快捷键

### 全局快捷键

| 快捷键        | 功能           |
| :------------- |:-------------|
| Files打开的状态下: Ctrl + L |      显示当前路径|
| Ctrl + Alt + ARROW    |          切换WorkSpace|
|SHIFT + Ctrl + Alt + ARROW  |    将当前窗口在WorkSpace之间移动|
|Ctrl + Windows + D        |      显示桌面|
|F11      |        全屏|

### Terminal

| 快捷键        | 功能           |
| :------------- |:-------------|
| CTRL+ALT+T      | 打开终端 |
| CTRL + SHIFT + T      | 新建标签页      |
| CTRL + D | 关闭标签页      |
| F11 | Terminal切换全屏/窗口模式      |
| CTRL + A | 光标移动到行首 |
| CTRL + E | 光标移动到行尾 |
| CTRL + K | 删除光标处至行尾的所有内容 |
| CTRL + U | 删除光标处至行首的所有内容 |
| CTRL + D | 删除光标处字符 |
| CTRL + H | 删除光标处前一个字符 |
| CTRL + W | 删除光标处到左边的单词 |
| CTRL + Y | 粘贴由Ctrl+u， Ctrl+d， Ctrl+w删除的单词 |
| CTRL + L | 相当于clear，清屏 |
| CTRL + R | 查找历史命令 |
| CTRL + B | 向后移动光标 |
| CTRL + F | 向前移动光标 |
| CTRL + T | 将光标处字符和前一个字符进行位置交换 |
| CTRL + & | 恢复 ctrl+h 或者 ctrl+d 或者 ctrl+w 删除的内容 |
| CTRL + S | 暂停屏幕输出 |
| CTRL + Q | 继续屏幕输出 |
| CTRL + ← | 光标移动到上一个单词的词首 |
| CTRL + → | 光标移动到下一个单词的词尾 |
| CTRL + P | 向上显示缓存的命令 |
| CTRL + N | 向下显示缓存的命令 |
| CTRL + D | 关闭终端 |
| CTRL + xx | 在EOL和当前光标位置移动 |
| CTRL + C | 终止进程/命令 |
| SHIFT + 上或下 | 终端上下滚动 |
| SHIFT + PgUP/PgDn | 终端上下翻页滚动 |
| CTRL + SHIFT + N | 新终端 |
| ALT + 数字 | 切换至对应的标签页 |
| CTRL + SHIFT + PgUp/PgDn | 左右移动标签页 |
| CTRL + PgUp/PgDn | 切换标签页 |
| F10  | 激活菜单栏 |


## APT命令

`apt purge / apt –purge remove`
删除已安装包（不保留配置文件)。
如软件包a，依赖软件包b，则执行该命令会删除a，而且不保留配置文件

`apt autoremove`
删除为了满足依赖而安装的，但现在不再需要的软件包（包括已安装包），保留配置文件。

`apt remove`
删除已安装的软件包（保留配置文件），不会删除依赖软件包，且保留配置文件。

`apt autoclean`
APT的底层包是dpkg, 而dpkg 安装Package时, 会将 `*.deb` 放在 `/var/cache/apt/archives/`中，`apt-get autoclean` 只会删除 `/var/cache/apt/archives/`已经过期的deb。

`apt clean`
使用 `apt clean`会将`/var/cache/apt/archives/`的所有 deb 删掉，可以理解为 `rm /var/cache/apt/archives/*.deb`。

## 添加或删除PPA

添加PPA源的命令为：
```
sudo add-apt-repository ppa:user/ppa-name
```


添加好更新一下：
```
sudo apt-get update
```

删除命令格式则为：
```
sudo add-apt-repository -r ppa:user/ppa-name
```

然后进入 /etc/apt/sources.list.d 目录，将相应 ppa 源的保存文件删除。
最后同样update一下。

## 必备软件

### ag

[GitHub](	https://github.com/ggreer/the_silver_searcher)

sudo apt-get install silversearcher-ag

### fasd

[GitHub](https://github.com/clvv/fasd)

sudo apt-get install fasd

add the follow line in .zshrc:
```
eval "$(fasd --init auto)"
```


### 键盘F1到FN不好用
    终端输入如下命令临时关闭FN功能键：
            echo 0 | sudo tee /sys/module/hid_apple/parameters/fnmode
    终端输入如下命令永久关闭FN功能键：
            echo options hid_apple fnmode=0 | sudo tee -a /etc/modprobe.d/hid_apple.conf
            sudo update-initramfs -u -k all

### amd显卡驱动
    https://www.amd.com/zh-cn/support/download/linux-drivers.html
     下载后终端输入如下命令：
         1. chmod 777 ./XXX.deb
         2. sudo dpkg -i ./XXX.deb
         3. amdgpu-install


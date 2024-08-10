# zsh
HomePage: https://ohmyz.sh/
GitHub: [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh)

## 安装

1. Shell中输入如下命令
```Shell
sudo apt install zsh  # 安装
zsh --version         # 查看版本
chsh -s /bin/zsh      # 将默认shell修改为zsh
```

2. 注销再重新登录
3. Shell中输入如下命令

```Shell
echo $SHELL          # 确认shell是否修改为zsh
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"   # 安装oh-my-zsh
```

## Powerlevel10k主题

[GitHub](https://github.com/romkatv/powerlevel10k)

1. Clone the repository:
```Shell
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

2.  Set `ZSH_THEME="powerlevel10k/powerlevel10k"` in `~/.zshrc`.

## 语法高亮

1. 安装插件:
```
cd ~/.oh-my-zsh/custom/plugins
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git
```

2. 在.zshrc中增加配置(在plugins中追加'zsh-syntax-highlighting')

```
plugins=( [plugins...] zsh-syntax-highlighting)
```

3. 读取配置及时生效

```
source ~/.zshrc
```

## 增加directory高亮

1. 设置solarized theme for GNU ls

```Shell
git clone https://github.com/seebi/dircolors-solarized.git
cp ~/dircolors-solarized/dircolors.256dark ~/.dircolors
eval 'dircolors .dircolors'
```

2. 设置 Terminal 支持 256 色, 在`.zshrc`中添加如下语句

```
export TERM=xterm-256color
```

3. 下载 Solarized 的 Gnome-Terminal 配色

```
git clone https://github.com/sigurdga/gnome-terminal-colors-solarized.git
cd gnome-terminal-colors-solarized
./set_dark.sh
```

4. 将下面额code追加到`.zshrc`中

```
# enable color support of ls and also add handy aliases
if [ -x /usr/bin/dircolors ]; then
    test -r ~/.dircolors && eval "$(dircolors -b ~/.dircolors)" || eval "$(dircolors -b)"
    alias ls='ls --color=always'
    alias dir='dir --color=always'
    alias vdir='vdir --color=always'

    alias grep='grep --color=always'
    alias fgrep='fgrep --color=always'
    alias egrep='egrep --color=always'
fi
```

5. 读取配置及时生效

```
source ~/.zshrc
```

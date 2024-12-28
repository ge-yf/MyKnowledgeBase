## 1. 安装Nerd Font字体

网址： https://www.nerdfonts.com/font-downloads
选择喜欢的字体下载

```shell
wget -q -nv https://github.com/ryanoasis/nerd-fonts/releases/download/v3.3.0/Meslo.zip

unzip Meslo.zip -d ~/.local/share/fonts

fc-cache -fv
```

## 2. 安装Python3

```shell
sudo apt install -yqq python3 python3-venv python3-pip

sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.12 1

sudo update-alternatives --install /usr/bin/python python /usr/bin/python3.12 1
```

## 3. 安装NPM

网址： https://github.com/nvm-sh/nvm?tab=readme-ov-file#installing-and-updating

```shell
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash

source ~/.zshrc

nvm install --lts

node -v
```

## 4. 安装Neovim

网址： https://github.com/neovim/neovim/blob/master/INSTALL.md#linux

```shell
wget -q -nv https://github.com/neovim/neovim/releases/download/nightly/nvim-linux64.tar.gz

tar -zxvf ./nvim-linux64.tar.gz

sudo rm -rf /usr/local/share/nvim-linux64

sudo mv ./nvim-linux64 /usr/local/share

sudo ln -s /usr/local/share/nvim-linux64/bin/nvim /usr/local/bin/nvim
```

## 5. 安装lazyim

网址： https://www.lazyvim.org/installation

```shell
git clone https://github.com/LazyVim/starter ~/.config/nvim

rm -rf ~/.config/nvim/.git

nvim
```

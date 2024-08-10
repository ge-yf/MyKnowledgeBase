
# emacs



## Linux下配置

### 追加PPA:

```shell
sudo add-apt-repository ppa:kelleyk/emacs
sudo apt update
```



## windows下配置

### 1. 下载emacs

[GNU Emacs](https://www.gnu.org/software/emacs/)

### 2. 设置环境变量

环境变量中追加:
    变量名：HOME
    变量值：该账号的home目录，例如(`C:\Users\GeYF`)

### 3. 下载ctags
[GitHub](https://github.com/universal-ctags/ctags-win32/releases)

解压后放到Program Files目录中，并将包含ctags.exe的目录加入到环境变量PATH中。

### 4. 下载gnu global

[下载地址](http://adoxa.altervista.org/global/)

下载Win32版本，解压后放到Program Files目录中，并将包含gtags.exe的目录加入到环境变量PATH中。

### 5. 下载spacemacs 

[GitHub](https://github.com/syl20bnr/spacemacs)

`git clone https://github.com/syl20bnr/spacemacs ~/.emacs.d`

初次启动后，将ELPA 镜像修改为[清华源](https://mirrors.tuna.tsinghua.edu.cn/help/elpa/) 。
 

### 6. 配置（SPC-f-e-d）

* dotspacemacs-line-numbers 修改成 `'relative`
* dotspacemacs-configuration-layers 打开"auto-completion"，添加"gtags"
* dotspacemacs-maximized-at-startup 修改为`t`
* dotspacemacs-default-font 的size修改为14
* defun dotspacemacs/user-init ()中添加:
>  (setq-default c-basic-offset 4
>                         tab-width 4
>                         indent-tabs-mode t)
>  (setq c-default-style "linux")


### 7. 使用

https://edward852.github.io/post/%E9%80%9A%E7%94%A8%E4%BB%A3%E7%A0%81%E7%BC%96%E8%BE%91%E5%99%A8spacemacs/

https://www.douban.com/note/706407786/?_i=24294560VIi4Z_

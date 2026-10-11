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



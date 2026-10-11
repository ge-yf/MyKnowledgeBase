# Advanced Programming in the UNIX Environment

## UNIX System Over view

### UNIX Architecture

![[Pasted image 20220525165340.png]]


- Kernel
    - 控制硬件资源
    - 提供程序的运行环境
- System calls
    - Kernel层的接口
- Library routines
    - 在System calls的基础上编写的通用函数库
    - 应用程序既可以使用System calls又可以使用Library routines
- shell
    - 一个特殊侧程序，提供运行其它程序的接口

### Logging In

用户信息：
`cat /etc/passwd`

> geyf:x:1000:1000:,,,:/home/geyf:/bin/zsh

用户名：密码：UID（用户ID）：GID（组ID）：描述性信息：主目录：默认Shell

### Files and Directories


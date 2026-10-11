# Spacemacs
## 行号显示与跳转

1. SPC-f-e-d，打开配置文件，将行号显示配置为relative
![[Pasted image 20220414105849.png]]

2. 行间跳转：
   `10j：向下跳转10行`
   `7k：向上跳转7行`

2. 跳转到指定行：
   `nG` ,例如跳转到512行：512G

## Projectile

[GitHub地址](https://github.com/bbatsov/projectile)
[Docs](https://docs.projectile.mx/projectile/index.html)

如果是git项目，spacemacs发现有.git目录，就会认为是一个spacemacs project.
如果没有.git目录，就需要手动创建一个".projectile"空文件，告诉spacmeacs此处是project根目录。

## Auto-completion

[Docs](https://www.spacemacs.org/layers/+completion/auto-completion/README.html)

* 配置全局启用company：
    you just have to add `(global-company-mode)` in the `dotspacemacs/user-config` function of your dotfile.


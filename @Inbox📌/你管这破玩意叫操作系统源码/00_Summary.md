## 品读 Linux 0.11 核心代码

[Github](https://github.com/sunym1993/flash-linux0.11-talk)

**一些非必须的资料**：[资料包](https://github.com/sunym1993/flash-linux0.11-talk/tree/main/%E4%B8%80%E4%BA%9B%E9%9D%9E%E5%BF%85%E8%A6%81%E7%9A%84%E8%B5%84%E6%96%99)

**一些共性的问题**：[FAQ](https://github.com/sunym1993/flash-linux0.11-talk/tree/main/FAQ)

**一些读者分享和见解**：[读者分享](https://github.com/sunym1993/flash-linux0.11-talk/tree/main/%E8%AF%BB%E8%80%85%E5%88%86%E4%BA%AB)

**还有个有趣的事情大家可以共同参与进来**：[Intel手册翻译计划](https://github.com/sunym1993/flash-linux0.11-talk/tree/main/Intel%20%E6%89%8B%E5%86%8C%E4%B8%AD%E6%96%87%E7%89%88)

---

**架构图**

![[Pasted image 20220527135815.png]]

---

-   **第一部分：进入内核前的苦力活**
    
    -   [第1回 最开始的两行代码](01_最开始的两行代码)
    -   [第2回 自己给自己挪个地儿](02_自己给自己挪个地儿)
    -   [第3回 做好最最基础的准备工作](https://mp.weixin.qq.com/s/90QBJ-lP_-du2qQJxNF-Fw)
    -   [第4回 把自己在硬盘里的其他部分也放到内存来](https://mp.weixin.qq.com/s/hStc-y-sabP-KwJUDUesTw)
    -   [第5回 进入保护模式前的最后一次折腾内存](https://mp.weixin.qq.com/s/5s_nmrWRZbA_4mkNKOQ2Cg)
    -   [第6回 先解决段寄存器的历史包袱问题](https://mp.weixin.qq.com/s/p1a6QxYZyMpJF__uBSE1Kg)
    -   [第7回 六行代码就进入了保护模式](https://mp.weixin.qq.com/s/S5zarr9BmLhUHAmdmeNypA)
    -   [第8回 烦死了又要重新设置一遍 idt 和 gdt](https://mp.weixin.qq.com/s/ssQKFMehxZxWT9i6mdRtXg)
    -   [第9回 Intel 内存管理两板斧：分段与分页](https://mp.weixin.qq.com/s/q2wU9IbX54t_GAuc9V5r7A)
    -   [第10回 进入 main 函数前的最后一跃！](https://mp.weixin.qq.com/s/ISyaX5zPWRw_d-9zvZUPUg)
    -   [第一部分总结与回顾](https://mp.weixin.qq.com/s/8bP3feeF_A13j7ysWur_JQ)
-   **第二部分：大战前期的初始化工作**
    
    -   [第11回 整个操作系统就20几行代码](https://mp.weixin.qq.com/s/kYBrMgHt7C9EmAcwJIPIxg)
    -   [第12回 管理内存前先划分出三个边界值](https://mp.weixin.qq.com/s/eoBFcgm0QrHOVi_WoS7PwA)
    -   [第13回 主内存初始化 mem_init](https://mp.weixin.qq.com/s/_rTmjHIDCV9ADiJlfo5B3g)
    -   [第14回 中断初始化 trap_init](https://mp.weixin.qq.com/s/sFp_388qRncB-jpJeRzCGQ)
    -   [第15回 块设备请求项初始化 blk_dev_init](https://mp.weixin.qq.com/s/pIbVY1XPCktxGogc4lI1Bw)
    -   [第16回 控制台初始化 tty_init](https://mp.weixin.qq.com/s/yIrzEWUUuZC9OsiuU_lOaw)
    -   [第17回 时间初始化 time_init](https://mp.weixin.qq.com/s/y26MMfj8pP5PmbKDZBT5-A)
    -   [第18回 进程调度初始化 sched_init](https://mp.weixin.qq.com/s/j4FYWUSX_2gpDb_h4vEFqQ)
    -   [第19回 缓冲区初始化 buffer_init](https://mp.weixin.qq.com/s/X8BSbf1qShS11_fzfyOhTg)
    -   [第20回 硬盘初始化 hd_init](https://mp.weixin.qq.com/s/803C9jHxIe42i9BrNzEvPA)
    -   [第二部分总结与回顾](https://mp.weixin.qq.com/s/Hf9B1ww1wFxiUDkWb0obeQ)
-   **第三部分：一个新进程的诞生**
    
    -   [第21回 新进程诞生全局概述](https://mp.weixin.qq.com/s/H_OCZ2ZtGHWHge_rYKCkJw)
    -   [第22回 从内核态切换到用户态](https://mp.weixin.qq.com/s/AVl6R2N9d_sldkhfvC6aEw)
    -   [第23回 如果让你来设计进程调度](https://mp.weixin.qq.com/s/Sf9vV7RCnVDlBKXx5jXs1Q)
    -   [第24回 从一次定时器滴答来看进程调度](https://mp.weixin.qq.com/s/yFre8Qv_ZCtjRkTS49n6rw)
    -   [第25回 通过 fork 看一次系统调用流程](https://mp.weixin.qq.com/s/rYBSH_AZDwgc8knSKDSSxA)
    -   [第26回 fork 中进程基本信息的复制](https://mp.weixin.qq.com/s/8cy-xX3ekeqHelrFcYFkvw)
    -   [第27回 fork 中进程内存规划的问题](https://mp.weixin.qq.com/s/d2pHFSbTLb-nv2C_RfKlVA)
    -   [第三部分总结与回顾](https://mp.weixin.qq.com/s/V_Ryxox3iDCO994FzkSFfA)
    -   [第28回 番外篇 - 我居然会认为权威书籍写错了...](https://mp.weixin.qq.com/s/JzCy_4RPhy17_G6KbY3f2g)
    -   [第29回 番外篇 - 让我们一起来写本书？](https://mp.weixin.qq.com/s/NFUgJ4-hIyrs1sQr8AUCvA)
    -   [第30回 番外篇 - 写时复制就这么几行代码](https://mp.weixin.qq.com/s/Pdnmys_hGoToZN193rfnoQ)
-   **第四部分：shell 程序的到来**
    
    -   [第31回 拿到硬盘信息](https://mp.weixin.qq.com/s/1xNinBNJIUv3UTO03RRFXA)
    -   [第32回 加载根文件系统](https://mp.weixin.qq.com/s/ruFNEgIBzlM5H-G9XR0ctw)
    -   [第33回 打开终端设备文件](https://mp.weixin.qq.com/s/53IcRO_zg-_rQNaK1u_TJg)
    -   [第34回 进程2的创建](https://mp.weixin.qq.com/s/Uh03a48Zt_l8HgtZvm1o-A)
    -   [第35回 execve 加载并执行 shell 程序](https://mp.weixin.qq.com/s/IQnUCTmT0Hwn4nW0dqioiw)
-   **第五部分：从一个命令的执行看操作系统各模块的运作**
    
-   **第六部分：操作系统哲学与思想**
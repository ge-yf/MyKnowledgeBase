## 一，前言

Linux内核是一个操作系统（OS）内核，本质上定义为类Unix。它用于不同的操作系统，主要是以不同的Linux发行版的形式。Linux内核是第一个真正完整且突出的免费和开源软件示例。Linux 内核是第一个真正完整且突出的免费和开源软件示例，促使其广泛采用并得到了数千名开发人员的贡献。

Linux 内核由芬兰赫尔辛基大学的学生 Linus Torvalds 于 1991 年创建。随着程序员调整其他自由软件项目的源代码以扩展内核的功能，它迅速取得了进展。Torvalds 首先使用 80386 汇编语言编写的任务切换器以及终端驱动程序，然后将其发布到 Comp.os.minix Usenet 组。它很快被 Mini社区所改编，为该项目提供了见解和代码。

Linux 内核越来越受欢迎，因为 GNU 自己的内核 GNU Hurd 不可用且不完整，而 Berkeley Software Distribu[TI](https://link.zhihu.com/?target=http%3A//bbs.elecfans.com/zhuti_715_1.html)on（BSD）操作系统仍然受到法律问题的困扰。在开发人员社区的帮助下，Linux 0.01 于 1991 年 9 月 17 日发布。

**在我们学习Linux内核之前，我们首先需要掌握以下几点：**

[(1)如何学习内核，先了解Linux内核由哪些组成？](https://zhuanlan.zhihu.com/p/440423464)

[(2)须知Linux内核源码（下载的链接 ）组织结构？](https://zhuanlan.zhihu.com/p/440423464)

(3)[重点需要学习地知识点有哪些？](https://zhuanlan.zhihu.com/p/440423464)

(4)[最后依据我为大家提供的的学习资料，开启我们的Linux内核学习之旅。](https://link.zhihu.com/?target=https%3A//docs.qq.com/doc/DTXFKZlZ4YmFYQWZS)

## 二，学习资料

### **2.1操作系统原理**

【 强烈推荐阅读】[一文带你彻底了解，零拷贝Zero-Copy技术(图解)](https://zhuanlan.zhihu.com/p/442771856)

[Linux操作系统学习——启动](https://zhuanlan.zhihu.com/p/440820446)

[Linux操作系统学习——内核运行](https://zhuanlan.zhihu.com/p/440825051)

[Linux操作系统学习——内核初始化](https://zhuanlan.zhihu.com/p/440829030)

[操作系统原理(一)：操作系统原理与概述(流程图)](https://zhuanlan.zhihu.com/p/446635858)

[操作系统原理(二)：Linux操作系统基础的常用命令](https://zhuanlan.zhihu.com/p/434528439)

[操作系统原理(三)：Linux操作系统I/O机制原理(流程图详解)](https://zhuanlan.zhihu.com/p/434511399)

[操作系统原理(四)：内存管理RAID磁盘阵列与配置](https://zhuanlan.zhihu.com/p/448266123)

[操作系统原理(五)：内存管理之磁盘高速缓存机制原理](https://zhuanlan.zhihu.com/p/448258669)

[操作系统原理(六)：存储管理之页式、段式、段页式存储](https://zhuanlan.zhihu.com/p/448147542)

[系统操作原理(七)：进程的状态和转换(五态模型)](https://zhuanlan.zhihu.com/p/447668827)

[操作系统原理(八)：进程同步的几种方式及基本原理](https://zhuanlan.zhihu.com/p/447720544)

[操作系统原理(九)：处理器调度基本准则和实现原理](https://zhuanlan.zhihu.com/p/447737355)

[系统操作原理(十)：多进程，多线程，并发执行中的死锁问题](https://zhuanlan.zhihu.com/p/448105261)

[汇编语言基础(十一)：汇编语言基础知识(图文代码)](https://zhuanlan.zhihu.com/p/449157752)

[汇编语言入门(十二)：汇编指令入门级整理，这些你必须要知道](https://zhuanlan.zhihu.com/p/449787476)

[汇编语言指令(十三)：汇编语言的所有指令总结，一篇就够了](https://zhuanlan.zhihu.com/p/449565154)

[汇编语言进阶(十四)：ARM体系结构处理器机制原理与实现](https://zhuanlan.zhihu.com/p/449582466)

[汇编语言进阶(十五)： ARM指令集与汇编语言程序设计](https://zhuanlan.zhihu.com/p/449816076)

### **2.2内存管理专题**

【 强烈推荐阅读】[尽情阅读，技术进阶，详解mmap原理](https://zhuanlan.zhihu.com/p/442268413)

[内存是什么？一文让你了解内存是怎么实现的](https://zhuanlan.zhihu.com/p/429118261)

[嵌入式开发必备技能，Linux内核源码组织结构](https://zhuanlan.zhihu.com/p/449071725)

[一文了解Linux内存管理，malloc、free 实现原理](https://zhuanlan.zhihu.com/p/442258814)

[内存管理系列(一)：Linux操作系统内存管理(思维导图详解)](https://zhuanlan.zhihu.com/p/456064945)

[内存管理系列(二)：Linux内存管理原理知识大总结](https://zhuanlan.zhihu.com/p/454577271)

[内存管理系列(三)：学完操作系统内存管理，能回答这8个问题吗？](https://zhuanlan.zhihu.com/p/454779105)

[内存管理系列(四)：理解 Memory barrier（内存屏障）](https://zhuanlan.zhihu.com/p/454564295)

[内存管理系列(五)：内存回收之LRU链表机制原理](https://zhuanlan.zhihu.com/p/453390459)

[内存管理系列(六)：虚拟内存和物理内存机制原理](https://zhuanlan.zhihu.com/p/453385879)

[内存管理系列(七)：Malloc缺页中断不同情况处理总结及反向映射RMAP](https://zhuanlan.zhihu.com/p/452713026)

[内存管理系列(八)：C/C++开发中的Malloc函数的实现原理](https://zhuanlan.zhihu.com/p/452686042)

[内存管理系列(九)：深入理解glibc malloc：内存分配器实现原理](https://zhuanlan.zhihu.com/p/452423278)

[内存管理系列(十)：操作系统是如何对内存进行管理的，内存与CPU之间的关系](https://zhuanlan.zhihu.com/p/452415871)

[内存管理系列(十一)：为什么Linux需要虚拟内存，虚拟内存对操作系统有哪些作用](https://zhuanlan.zhihu.com/p/451886800)

[内存管理系列(十二)：用户态内存内存映射函数Mmap的好处](https://zhuanlan.zhihu.com/p/451881734)

[内存管理系列(十三)：内存管理：详解虚拟地址空间-MMU](https://zhuanlan.zhihu.com/p/451469447)

[内存管理系列(十四)：C语言中的Malloc/free是如何分配内存的](https://zhuanlan.zhihu.com/p/451468637)

[内存管理系列(十五)：从虚拟寻址到开源项目，Linux下的内存管理详解](https://zhuanlan.zhihu.com/p/451467641)

[内存管理系列(十六)：一文带你了解，虚拟内存、内存分页、分段、段页式内存管理](https://zhuanlan.zhihu.com/p/451405962)

[内存管理系列(十七)：Linux应用程序究竟消耗了多少内存](https://zhuanlan.zhihu.com/p/441938447)

[内存管理系列(十八)：虚拟地址到物理地址，是什么时候开始映射](https://zhuanlan.zhihu.com/p/441918912)

[内存管理系列(十九)：浅析Linux内存管理中SLAB分配器(源码分析)](https://zhuanlan.zhihu.com/p/431277793)

[内存管理系列(二十)：基于Linux内存管理的内存分配(伙伴算法和slab算法)](https://zhuanlan.zhihu.com/p/430233534)

[内存管理系列(二十一)：探索内存原理的内存映射文件(图文详解)](https://zhuanlan.zhihu.com/p/429987335)

### **2.3进程管理专题**

[进程管理系列(一)：Linux进程管理原理详解(代码演示)](https://zhuanlan.zhihu.com/p/425886322)

[进程管理系列(二)：十分钟让你像大佬一样快速了解进程状态(二种模型)](https://zhuanlan.zhihu.com/p/425931602)

[进程管理系列(三)：作为互联网程序员，应该了解Linux进程六种状态吗？](https://zhuanlan.zhihu.com/p/425939661)

[进程管理系列(四)：五分钟让你快速了解Linux进程管理实时调度与SMP](https://zhuanlan.zhihu.com/p/426836494)

[进程管理系列(六)：浅析Linux的进程优先级(代码演示)](https://zhuanlan.zhihu.com/p/426399519)

[进程管理系列(七)：进程管理|浅析C语言中并发同步与原子操作，锁三者是什么关系](https://zhuanlan.zhihu.com/p/441558619)

[进程管理系列(八)：进程管理|深入理解Linux进程述符和进程状态](https://zhuanlan.zhihu.com/p/441346358)

[进程管理系列(九)：一文读懂Linux内核中的任务间调度策略](https://zhuanlan.zhihu.com/p/442921692)

[进程管理系列(十)：Linux内核之进程和线程的创建和派生](https://zhuanlan.zhihu.com/p/442916346)

[进程管理系列(十一)：基于Linux有几种进程状态](https://zhuanlan.zhihu.com/p/442905446)

[进程管理系列(十二)：操作系统的几种CPU调度策略](https://zhuanlan.zhihu.com/p/455680633)

[进程管理系列(十二)：Linux 进程管理之调度和进程切换](https://zhuanlan.zhihu.com/p/462066025)

### **2.4网络协议栈专题**

【 强烈推荐阅读】[嵌入式必备：如何学习Linux内核网络协议栈](https://zhuanlan.zhihu.com/p/449869444)

[趣谈网络协议栈(一)：套接字缓冲区原理](https://zhuanlan.zhihu.com/p/460693504)

[趣谈网络协议栈(二)：数据包是如何处理的过程](https://zhuanlan.zhihu.com/p/458188649)

[趣谈网络协议栈(三)：七层模型下三层数据通信](https://zhuanlan.zhihu.com/p/453813447)

[趣谈网络协议栈(四)：传输的Arp报文结构](https://zhuanlan.zhihu.com/p/453814298)

[趣谈网络协议栈(五)：Socket编程常用函数的原理及代码实现](https://zhuanlan.zhihu.com/p/453814919)

[趣谈网络协议栈(六)：学习select和poll函数的内核实现](https://zhuanlan.zhihu.com/p/453815877)

[趣谈网络协议栈(七)：Epoll从用户态到内核态过程分析](https://zhuanlan.zhihu.com/p/453816689)

[趣谈网络协议栈(八)：套接字发送网络数据的过程](https://zhuanlan.zhihu.com/p/444071187)

### 2.5设备驱动专题

[浅谈设备驱动(一)：操作系统 I/O 流程详解](https://zhuanlan.zhihu.com/p/448718574)

[浅谈设备驱动(二)：Linux操作系统学习之字符设备](https://zhuanlan.zhihu.com/p/445188798)

[浅谈设备驱动(三)：结合设备信息集合，探究设备和驱动是如何绑定的](https://zhuanlan.zhihu.com/p/445185233)

### 2.6面试题/经验

【 强烈推荐阅读】[从事十年嵌入式转内核开发(23K到45K),给兄弟们的一些建议](https://zhuanlan.zhihu.com/p/458546929)

[谈谈Linux内核的学习路线，具体要怎么学？](https://zhuanlan.zhihu.com/p/456073398)

[2022年嵌入式开发想进互联网大厂，你技术过硬吗？](https://zhuanlan.zhihu.com/p/453576978)

[嵌入式Linux内核学习经验总结，一篇让你掌握方法](https://zhuanlan.zhihu.com/p/452972023)

[盘点Linux内核(驱动开发，嵌入式，内核人群)必问的面试题](https://zhuanlan.zhihu.com/p/445363696)

### 2.7内核书籍

-   《深入了解Linux内核》
-   《Linux就该这么学》
-   《Linux内核完全注释V3.0书签版》
-   《Linux命令行大全 - 绍茨 (william E.shotts)》
-   《Linux命令速查手册》
-   《Linux性能优化大师》
-   《Linux环境编程：从应用到内核》
-   《Linux集群和自动化运维 余洪春》
-   《Linux驱动程序开发实例(第2版)》
-   《Linux高级程序设计(第3版)》
-   《构建高可用Linux服务器(第4版)》

**书籍免费领取地址：**[https://docs.qq.com/doc/DTkZRWXRFcWx1bWVx](https://link.zhihu.com/?target=https%3A//docs.qq.com/doc/DTkZRWXRFcWx1bWVx)

## 三，内核学习路线

很多同学接触Linux不多，对Linux平台的开发更是一无所知。而现在的趋势越来越表明，作为一 个优秀的软件开发人员，或计算机IT行业从业人员，掌握Linux是一种很重要的谋生资源与手段。下来我将会结合自己的几年的个人开发经验，及对 Linux，更是类UNIX系统，及开源软件文化，谈谈Linux的学习方法与学习中应该注意的一些事。

就如同刚才说的，很多同学以前可能连Linux是什么都不知道，对UNIX更是一无所知。所以我们从最基础的讲起，对于Linux及UNIX的[历史](https://link.zhihu.com/?target=https%3A//www.tphone8.com/lishi)我们不做多谈，直接进入入门的学习。

Linux入门是很简单的，问题是你是否有耐心，是否爱折腾，是否不排斥重装一类的大修。没折腾可以说是学不好Linux的，鸟哥说过，要真正了解Linux的分区机制，对LVM使用相当熟练，没有20次以上的Linux装机经验是积累不起来的，所以一定不要怕折腾。

由于大家之前都使用Windows，所以我也尽可能照顾这些“菜鸟”。我的推荐，如果你第一次接触Linux，那么首先在虚拟机中尝试它。虚拟机我推荐Virtual Box，我并不主张使用VM，原因是VM是闭源的，并且是收费的，我不希望推动盗版。当然如果你的Money足够多，可以尝试VM，但我要说的是即使是VM，不一定就一定好。付费的软件不一定好。首先，Virtual Box很小巧，Windows平台下安装包在80MB左右，而VM动辄600MB，虽然功能强大，但资源消耗也多，何况你的需求Virtual Box完全能够满足。所以，还是自己选。如何使用虚拟机，是你的事，这个我不教你，因为很简单，不会的话Google或B[ai](https://link.zhihu.com/?target=http%3A//www.elecfans.com/tags/ai/)du都可以，英文好的可以直接看官方文档。

现在介绍Linux发行版的知识。正如你所见，Linux发行版并非Linux，Linux仅是指操作系统的内核，作为科班出生的你不要让我解释，我也没时间。

**我推荐的发行版如下：**

1.  UBUNTU适合纯菜鸟，追求稳定的官方支持，对系统稳定性要求较弱，喜欢[最新](https://link.zhihu.com/?target=http%3A//www.elecfans.com/article/bbs/)应用，相对来说不太喜欢折腾的开发者。
2.  Debian，相对UBUNTU难很多的发行版，突出特点是稳定与容易使用的包管理系统，缺点是企业支持不足，为社区开发驱动。
3.  Arch，追逐时尚的开发者的首选，优点是包更新相当快，无缝升级，一次安装基本可以一直运作下去，没有如UBUNTU那样的版本概念，说的专业点叫滚动升级，保持你的系统一定是最新的。缺点显然易见，不稳定。同时安装配置相对Debian再麻烦点。
4.  Gentoo，相对Arch再难点，考验使用者的综合水平，从系统安装到微调，内核编译都亲历亲为，是高手及黑客显示自己技术手段，按需配置符合自己要求的系统的首选。

**Slackware与Gentoo类似：**

CentOS，社区维护的RedHat的复刻版本，完全使用RedHat的源码重新编译生成，与RedHat的兼容性在理论上来说是最好的。如果你专注于Linux服务器，如网络管理，架站，那么CentOS是你的选择。

LFS，终极黑客显摆工具，完全从源代码安装，编译系统。安装前你得到的只有一份文档，你要做的就是照文档你的说明，一步步，一条条命令，一个个软件包的去构建你的Linux，完全由你自己控制，想要什么就是什么。如果你做出了LFS，证明你的Linux功底已经相当不错，如果你能拿LFS文档活学活用，再将Linux从源代码开始移植到嵌入式系统，我敢说中国的企业你可以混的很好。

你得挑一个适合你的系统，然后在虚拟机安装它，开始使用它。如果你想快速学会Linux，我有一个建议就是忘记图形界面，不要想图形界面能不能提供你问题的答案，而是满世界的去找，去问，如何用命令行解决你的问题。在这个过程中，你最好能将Linux的命令掌握的不错，起码常用的命令得知道，同时建立了自己的知识库，里面是你积累的各项知识。

再下个阶段，你需要学习的是Linux平台的C++/C++开发，同时还有Bash脚本编程，如果你对Java兴趣很深还有Java。同样，建议你抛弃掉图形界面的IDE，从VIM开始，为什么是VIM，而不是Emacs，我无意挑起编辑器大战，但我觉得VIM适合初学者，适合手比较笨，脑袋比较慢的开发者。Emacs的键位太多，太复杂，我很畏惧。然后是GCC，Make，Eclipse（Java，C++或者）。虽然将C++列在了Eclipse中，但我并不推荐用IDE开发C++，因为这不是Linux的文化，容易让你忽略一些你应该注意的问题。IDE让你变懒，懒得跟猪一样。如果你对程序调试，[测试](https://link.zhihu.com/?target=http%3A//www.hqpcb.com/zhuoluye11/%3Ftid%3D26%26plan%3Dfashaoyou)工作很感兴趣，GDB也得学的很好，如果不是GDB也是必修课。这是开发的第一步，注意我并没有提过一句Linux系统API的内容，这个阶段也不要关心这个。你要做的就是积累经验，在Linux平台的开发经验。我推荐的书如下：C语言程序设计，谭浩强的也可以。C语言，白皮书当然更好。C++推荐C++ Primer Plus，Java我不喜欢，就不推荐了。工具方面推荐VIM的官方手册，GCC中文文档，GDB中文文档，GNU开源软件开发指导（电子书），汇编语言程序设计（让你对库，链接，内嵌汇编，编译器优化选项有初步了解，不必深度）。

如果你这个阶段过不了就不必往下做了，这是底线，最基础的基础，否则离开，不要霍霍Linux开发。不专业的Linux开发者作出的程序是与Linux文化或UNIX文化相背的，程序是走不远的，不可能像Bash，VIM这些神品一样。所以做不好干脆离开。

接下来进入Linux系统编程，不二选择，APUE，UNIX环境高级编程，一遍一遍的看，看10遍都嫌少，如果你可以在大学将这本书翻烂，里面的内容都实践过，有作品，你口头表达能力够强，你可以在面试时说服所有的考官。（可能有点夸张，但APUE绝对是圣经一般的读物，即使是Windows程序员也从其中汲取养分，Google创始人的案头书籍，扎尔伯克的床头读物。）

这本书看完后你会对Linux系统编程有相当的了解，知道Linux与Windows平台间开发的差异在哪？它们的优缺点在哪？我的总结如下：做Windows平台开发，很苦，微软的系统API总在扩容，想使用最新潮，最高效的功能，最适合当前流行系统的功能你必须时刻学习。Linux不是，Linux系统的核心API就100来个，记忆力好完全可以背下来。而且经久不变，为什么不变，因为要同UNIX兼容，符合POSIX标准。所以Linux平台的开发大多是专注于底层的或服务器编程。这是其优点，当然图形是Linux的软肋，但我站在一个开发者的角度，我无所谓，因为命令行我也可以适应，如果有更好的图形界面我就当作恩赐吧。另外，Windows闭源，系统做了什么你更本不知道，永远被微软牵着鼻子跑，想想如果微软说Win8不支持QQ，那腾讯不得哭死。而Linux完全开源，你不喜欢，可以自己改，只要你技术够。另外，Windows虽然使用的人多，但使用场合单一，专注与桌面。而Linux在各个方面都有发展，尤其在云计算，服务器软件，嵌入式领域，企业级应用上有广大前景，而且兼容性一流，由于支持POSIX可以无缝的运行在UNIX系统之上，不管是苹果的Mac还是IBM的AS400系列，都是完全支持的。另外，Linux的开发环境支持也绝对是一流的，不管是C/C++，Java，Bash，[Python](https://link.zhihu.com/?target=http%3A//www.elecfans.com/tags/python/)，PHP，[Javascript](https://link.zhihu.com/?target=http%3A//www.elecfans.com/tags/javascript/)，。。。。。。就连[C#](https://link.zhihu.com/?target=http%3A//www.elecfans.com/tags/c%23/)也支持。而微软除Visual Stdio[套件](https://link.zhihu.com/?target=http%3A//www.hqchip.com/app/842)以外，都不怎么友好，不是吗？

如果你看完APUE的感触有很多，希望验证你的某些想法或经验，推荐UNIX程序设计艺术，世界顶级黑客将同你分享他的看法。现在是时候做分流了。 大体上我分为四个方向：网络，图形，嵌入式，设备驱动。

如果选择网络，再细分，我对其他的不是他熟悉，只说服务器软件编写及高性能的并发程序编写吧。相对来说这是网络编程中技术含量最高的，也是底层的。需要很多的经验，看很多的书，做很多的项目。

**我的看法是以下面的顺序来看书：**

1.  APUE再深读 – 尤其是进程，线程，IPC，套接字
2.  多核程序设计 - Pthre[ad](https://link.zhihu.com/?target=https%3A//dfm.elecfans.com/uploads/software/hqdfm.zip%3Fneilian)一定得吃透了，你很NB
3.  UNIX网络编程 – 卷一，卷二
4.  TCP/IP网络详解 – 卷一 再看上面两本书时就该看了
5.  TCP/IP 网络详解 – 卷二 我觉得看到卷二就差不多了，当然卷三看了更好，努力，争取看了
6.  Lighttpd源代码 - 这个服务器也很有名了
7.  Nginx源代码 – 相较于Apache，Nginx的源码较少，如果能看个大致，很NB。看源代码主要是要学习里面的套接字编程及并发控制，想想都激动。如果你有这些本事，可以试着往暴雪投简历，为他们写服务器后台，想一想全球的魔兽都运行在你的服务器软件上。
8.  Linux内核TCP/IP协议栈 – 深入了解TCP/IP的实现

如果你还喜欢驱动程序设计，可以看看更底层的协议，如链路层的，写什么路由器，网卡，网络设备的驱动及嵌入式系统软件应该也不成问题了。当然一般的网络公司，就算百度级别的也该毫不犹豫的雇用你。只是看后面这些书需要时间与经验，所以35岁以前办到吧！跳槽到给你未来的地方！

**图形方向，我觉得图形方向也是很有前途的，以下几个方面：**

Opengl的工业及游戏开发，国外较成熟。

影视动画特效，如皮克斯，也是国外较成熟。

GPU计算技术，可以应用在浏览器网页渲染上，GPU计算资源利用上，由于开源的原因，有很多的文档程序可以参考。如果能进火狐开发，或google做浏览器开发，应该会很好 。

**嵌入式方向：嵌入式方向没说的，Linux很重要**

掌握多个架构，不仅X86的，ARM的，单片机什么的也必须得懂。硬件不懂我预见你会死在半路上，我也想走嵌入式方向，但我觉得就学校教授嵌入式的方法，我连学电子的那帮学生都竞争不过。奉劝大家，一定得懂硬件再去做，如果走到嵌入式应用开发，只能祝你好运，不要碰上像Nokia，Hp这样的公司，否则你会很惨的。

驱动程序设计：软件开发周期是很长的，硬件不同，很快。每个月诞生那么多的新硬件，如何让他们在Linux上工作起来，这是你的工作。由于Linux的兼容性很好，如果不是太低层的驱动，基本C语言就可以搞定，系统架构的影响不大，因为有系统支持，你可能做些许更改就可以在ARM上使用PC的硬件了，所以做硬件驱动开发不像嵌入式，对硬件知识的要求很高。可以从事的方向也很多，如家电啊，特别是如索尼，日立，希捷，富士康这样的厂子，很稀缺的。

## **四，学习Linux内核**

学习linux内核，这个可不像学一门语言，c或者java一个月或者3月你就能精通掌握。学习linux内核是需要一步一步循序渐进，掌握正确的linux内核学习路线对学习至关重要，本篇文章就来分享学习linux内核的一些建议吧。

1. 了解操作系统基本概念。如果不会，可以学习《操作系统：设计与实现》Andrew S.Tanenbaum 写的那本。以MINIX为例子讲解操作系统的概念。非常推荐。

2. 有了操作系统的基本概念以后，可以了解Linux的机制了。推荐《Linux内核设计与实现》Robert Love 写的。这本书从概念上讲解了Linux有什么，他们是怎么运行的。这本书要反复认真看透。

3. 有了Linux内核的了解，还需要具体研究Linux内核源码。经典的就是《深入理解Linux内核》Daniel P. Bovet 写的。学习这本书的时候，要对着内核代码看着学。这本书学起来相当费力了，那么多多代码要研究。不过这本书如果学明白了，恭喜你，Linux内核你已经很熟悉了。

4. 如果要开发设备驱动，可以学习《Linux设备驱动程序》O‘Reilly出版社的。这本作为驱动的入门是很好的资料。另外还有一本《精通Linux 驱动程序开发》也是不错的教材，可以参考着看。学习驱动，免不了要学习一些硬件的协议和资料，研究哪个就找到相应的硬件文档，把硬件的工作原理搞明白。这些就不细说了。

5. 网络部分，学些Linux网络部分就学习《深入理解LINUX网络技术内幕》。这本书把Linux的网络部分讲的非常清晰透彻。但是通常不做这方面的工作研究，也不用研究这么深，毕竟现在相关职位较少。

6. 现在Linux相关的工作，多集中在一些嵌入式开发领域，arm，mips等，要学习以下这些体系架构的的资料，了解CPU的设计和工作方式。ARM就看对应的芯片手册，讲的很细致。MIPS就看 《see mips run》，有一二两版，两版内容有些差异，推荐都看。

7. 补充一点经验。不要认为Linux很庞大，很复杂，就觉的很难学。任何东西认真学下来都是能学会的，看你都恒心和毅力了。另外，不要走弯路，不要看市面上讲什么Linux0.11的那些书，直接学你要学的东西。就像学C语言看什么谭浩强一样，弯路走了，力气没少花，还严重影响学习效果。

**关于linux内核学习路线，再多说几句应用编程，有时候经常会需要的：**

1. 学习Linux应用编程，建议看《unix环境高级编程》，把里面的例子都做一遍，会对整个Linux编程有系统都认识。

2. 针对Linux，有本 《Linux系统编程》，学完上一本，这本很快看一遍就懂了。主要是针对Linux具体懂一些内容，讲的挺全了，很实用。

3. Linux网络编程，系统的学习一下《unix网络编程。卷1，套接字联网api》，基本上网络应用相关的程序就都没问题了。

这些内容，分几年时间，分步计划学习，就会成为Linux高手了。个人建议参加零声教育的培训，学习效率会高很多，有目的性的参加培训，缩短周期，快速成型才是时代所需。

**官方地址：**[Linux内核源码/内存调优/文件系统/进程管理/设备驱动/网络协议栈-学习视频教程-腾讯课堂](https://link.zhihu.com/?target=https%3A//ke.qq.com/course/4032547%3FflowToken%3D1040236)
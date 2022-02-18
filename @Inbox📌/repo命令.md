 repo init -u ssh://goni.iauto.com:29418/Src/Goni/platform/manifest -m default.xml -b virgin/master
 初始化repo仓库
 repo sync -c --no-tags
 同步代码
 repo start virgin/master --all
 checkout分支

repo forall -c XXX
XXX可以是任何可以被系统支持的shell命令（ls,cp,pwd等）包括git


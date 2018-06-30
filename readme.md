OpenVZ 魔改 BBR - lkl-rinetd 一键脚本

开始使用
要求以下：

OpenVZ
64 bit
Ram >> 64M
更新： 2018-03-24 新增 多网卡 适配

Debian or Ubuntu
适用于 单网卡（单 IP） 服务器：
wget https://github.com/tcp-nanqinlang/lkl-rinetd/releases/download/1.1.0/tcp_nanqinlang-rinetd-debianorubuntu.sh
bash tcp_nanqinlang-rinetd-debianorubuntu.sh

适用于 多网卡（多 IP） 服务器，会为所有网卡（所有 IP）提供加速：
wget https://github.com/tcp-nanqinlang/lkl-rinetd/releases/download/1.1.0/tcp_nanqinlang-rinetd-debianorubuntu-multiNIC.sh
bash tcp_nanqinlang-rinetd-debianorubuntu-multiNIC.sh

CentOS 7
和上面一样，也分 单网卡 和 多网卡 版本：
# 单网卡
wget https://github.com/tcp-nanqinlang/lkl-rinetd/releases/download/1.1.0/tcp_nanqinlang-rinetd-centos.sh
bash tcp_nanqinlang-rinetd-centos.sh

# 多网卡
wget https://github.com/tcp-nanqinlang/lkl-rinetd/releases/download/1.1.0/tcp_nanqinlang-rinetd-centos-multiNIC.sh
bash tcp_nanqinlang-rinetd-centos-multiNIC.sh

使用说明
以下进行脚本使用说明：

安装 lkl-rinetd
此命令用于安装 lkl-rinetd。

在 /home/tcp_nanqinlang 进行安装，所以安装完成后不要动这个文件夹了（除非你想修改端口）。

安装过程中，会提示输入端口号。多个端口号用空格隔开。不支持端口段。

安装完成后，会开启 lkl-rinetd。以后重启机器也会随开机自启。

使用前请注意自己的 iptables 相关设置。

检查 lkl-rinetd 运行状态
此命令用于检查 lkl-rinetd 运行与否，可通过返回的提示判断。

卸载 lkl-rinetd
运行此命令会删除 /home/tcp_nanqinlang 、移除 rc.local 对应开机自启项和清空 iptables raw 表。属于完整卸载，不会有残留。且卸载后无需重启。

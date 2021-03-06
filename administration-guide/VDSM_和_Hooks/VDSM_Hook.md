# VDSM Hook

VDSM 能够通过 Hook 进行扩展。Hook
是当特定事件发生时在主机上运行的脚本。当被支持的事件发生时，VDSM
按照数字顺序执行位于主机上 `/usr/libexec/vdsm/hooks//` 目录下的可执行
Hook 脚本。按照惯例每个 Hook
脚本的文件名都以一个两位的数字开头，以确保脚本执行顺序的明确程度。您能够使用任意的编程语言编写
Hook 脚本，但在本章的例子中使用的是 Python。

必须注意的是，所有在主机上为某个事件定义的脚本都将被执行。如果您希望一个
Hook 只对运行在该主机上的一部分虚拟机执行，那么您必须确保 Hook
脚本本身能够根据虚拟机的*自定义属性*处理这个需求。

> **警告**
>
> VDSM Hook 有可能妨碍 EayunOS 的正常运行。VDSM Hook
> 中存在的漏洞将有可能造成虚拟机崩溃和数据损失。VDSM Hook
> 的实现必须谨慎，并且进行严格的测试。Hook API
> 是新近确定的，并且在以后有可能发生明显的改变。


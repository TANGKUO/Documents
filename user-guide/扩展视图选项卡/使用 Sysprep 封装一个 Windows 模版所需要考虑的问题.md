# 使用 Sysprep 封装一个 Windows 模版所需要考虑的问题

为 Windows 虚拟机所创建的模板在被用来部署虚拟机前需要被封装，这会确保那些针对于特定机器的设置不会出现在模板中。

**Sysprep** 是一个用来封装 Windows 模板的工具。

> **重要**
>
> 在进行这个操作的过程中不要重新启动虚拟机。

在运行 **Sysprep** 前，请确保以下设置已经被配置：
* Windows **Sysprep** 参数已经被正确定义。<br/>
  如果还没有定义，点**编辑**并在**操作系统**和**域**项中输入相应的信息。

* 正确的产品密钥已经在 **engine-config** 配置工具程序中被输入。<br/>
  如果还没有输入，以 root 用户身份在 Manager 上运行配置工具程序，并输入所需信息。您需要输入 **ProductKey** 和 **SysPrepPath**。例如，Windows 7 的配置值是 **ProductKeyWindow7** 和 **SysPrepWindows7Path**。使用以下命令设置这些值：
  ```
  # engine-config --set ProductKeyWindow7=<validproductkey> --cver=general
  ```

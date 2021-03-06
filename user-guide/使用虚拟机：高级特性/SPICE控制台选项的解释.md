# SPICE 控制台选项的解释

当选择了 SPICE 控制台连接协议，**控制台选项**窗口中可以配置如下选项。

  图

**控制台调用**

  * **自动的**：EayunOS 虚拟化管理中心可以自动选择调用控制台的方法。
  * **Native 客户端**：当连接到虚拟机控制台时，一个文件下载的窗口会向您提供一个可以使用 Remote Viewer 打开虚拟机控制台的文件。
  * **浏览器插件**：当连接到虚拟机控制台时，您会直接连通过 Remote Viewer 进行连接。
  * **SPICE HTML5 浏览器客户（技术预览）**：当连接到虚拟机控制台时，会打开一个控制台的浏览器标签，作为控制台使用。

**控制台选项**

  * **映射 control-alt-del 快捷键为 ctrl+alt+end**：勾选后，**Ctrl+Alt+Del**键会与虚拟机中的**Ctrl+Alt+End**键关联。
  * **启用 USB 自动共享**：勾选后，自动重定向 USB 设备到虚拟机上。如果这个选项没有勾选，USB 设备会连接到客户端机器而不是虚拟机。要在虚拟机上使用 USB 设备，需要在 SPICE 客户端菜单上手动启用它。
  * **以全屏打开**：勾选后，连接虚拟机时，自动以全屏的方式打开控制台。可以按下 **SHIFT+F11** 来切换启用或禁用全屏模式。
  * **启用 SPICE 代理**：勾选后可以启用 SPICE 代理。

> **重要**
>
> 只有通过 Internal Explore (IE 浏览器) 访问管理门户和用户门户时，**浏览器插件**控制台选项才是可用的，这个控制台选项使用的是由 **SpiceX.cab** 安装程序提供的 Remote Viewer 的版本。对于所有的浏览器来说，**Native 客户端**控制台选项是默认的，这个控制台选项使用的是由 **virt-viewer-x86.msi** 和 **virt-viewer-x64.msi** 安装文件提供的 Remote Viewer 的版本。

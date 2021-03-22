---
title: 禁用 Windows Update 服务
---

## 禁用 Windows Update 服务，阻止自动更新

`win + R` 直接输入`services.msc`，打开Windows服务管理器，找到「Windows Update」的本地服务。

![](https://raw.githubusercontent.com/KerwinKwong/Image/main/uPic/%E7%A6%81%E7%94%A8Windows10%E6%9B%B4%E6%96%B0/stop-win10-upgrade-01.jpg){:height 339, :width 626}

双击打开属性配置，点击并停止服务，然后将其启动类型由「自动」改为「手动」。

![](https://raw.githubusercontent.com/KerwinKwong/Image/main/uPic/%E7%A6%81%E7%94%A8Windows10%E6%9B%B4%E6%96%B0/stop-win10-upgrade-02.jpg)
## 配置组策略，根治 Windows 更新

如果使用的是 **Windows 10 专业版及以上系统**，可以通过配置组策略来关闭 Windows 更新。`win + R`输入`gpedit.msc`，通过左侧的目录树转到「计算机配置 - 管理模板 - Windows 组件 - Windows 更新」，最终找到「配置自动更新」选项。

![](https://raw.githubusercontent.com/KerwinKwong/Image/main/uPic/%E7%A6%81%E7%94%A8Windows10%E6%9B%B4%E6%96%B0/stop-win10-upgrade-03.png)

![](https://raw.githubusercontent.com/KerwinKwong/Image/main/uPic/%E7%A6%81%E7%94%A8Windows10%E6%9B%B4%E6%96%B0/stop-win10-upgrade-04.png)

双击进入后，将其数值改为「已禁用」，确定后 Windows 就再也不会自动更新了。

![](https://raw.githubusercontent.com/KerwinKwong/Image/main/uPic/%E7%A6%81%E7%94%A8Windows10%E6%9B%B4%E6%96%B0/stop-win10-upgrade-05.png)

## 借助[Dism++](https://www.chuyu.me/zh-Hans/)
# [你Omega的设备名](#你Omega的设备名)

每个Omega有一个名称，用于标识它，也是Omega的AP的默认名称，本文将告诉你如何找到你自己的Omega的名字。

名称基于Omega的无线设备的MAC地址; 每个设备都有一个完全唯一的MAC地址(在华强北可不一定)。

Omega的屏蔽上有一个贴纸：
![](../img/omega-name-0-just-omega.jpg)

这里打印的文本是Omega的唯一MAC地址，我们只需要关注最后四位数字。

你的Omega的名字将是`Omega-ABCD`的形式，其中`ABCD`是贴纸的最后四位数字。

> MAC地址以十六进制数字表示，所以您的Omega的MAC地址的名称中将包含a，b，c，d，e，f字符。

上图中的Omega被命名为Omega-5931，默认情况下它的WiFi网络将被命名为Omega-5931，它的本地网络上的主机名将是omega-5931.local

> 请注意，WiFi网络名称区分大小写，而本地网络主机名称不区分大小写！(译者注: Linux的主机名都不分大小写)

## [初始化](#初始化)

按照本文档，初始化您的Omega2。 我们将首先了解正确连接Omega至Dock和电源。 在连接上之后，使用安装向导将其连接到您的WiFi网络，然后做一些更新。
> 如果您在此过程中遇到问题，请尝试查看[疑难解答指南](first-time-troubleshooting.html)。

## [拆箱和硬件初始化](#拆箱和硬件初始化)
> 这个指南假设你有一个Omega和一个电源拓展坞。 如果您没有购买拓展坞，请按照我们的指南[为没有电源拓展坞的Omega提供电源](hardware-prep-no-dock.html)。

### 拆包

把Omega和电源拓展坞从包裹里拿出来

![](../img/unbox-1-omega-with-dock.jpg)

### 连接

将Omega的插入Dock上的插座

![](../img/unbox-2-omega-on-dock.jpg)

确保您的Omega的针脚完全插入

![](../img/unbox-3-omega-on-dock-side.jpg)

### 供电

Omega使用3.3v的电源供电，但塔也有电源调整器，所以你可以使用任意microUSD给它供电。

你也可以用电脑的USB口进行供电

![](../img/unbox-4-omega-provide-power.jpg)

### 开机！

用这个开关打开Omega

![](../img/unbox-5-omega-switched-on.jpg)

### 等待它启动

Omega上的橘红色的LED会亮起，然后在大约10秒钟后开始闪烁。 再过了大约一分钟后，LED将停止闪烁并保持开启，这意味着Omega已启动。

另外：有可能你的Omega会有些不同：如果Omega上的橘红色的LED指示灯亮起并持续亮着，那请等待约一分钟，然后你的Omega就会完成启动。

![](../img/unbox-6-omega-led-detail.jpg)

# [使用安装向导](#使用安装向导)

### 一些要对计算机进行的配置

您的计算机可能需要安装一些额外的程序并通过浏览器来访问Omega：
* Windows用户请安装Apple Bonjour Service
* Linux用户需要安装Zeroconf
* OS X用户，无需准备额外的东西

### Omega的名称

让我们找到你的Omega的名称，在Omega的屏蔽壳上有一张MAC地址贴纸

![](../img/omega-name-0-just-omega.jpg)

这里贴上的是Omega的MAC地址，请注意最后四位数字。 你的Omega的名字是Omega-ABCD，其中ABCD是贴纸的最后四位数字。

如图所示的设备名为 `Omega-5931`

### 链接到Omega的wifi网络

Omega主机本身自带WiFi。 让我们将您的计算机连接到它。 WiFi网络的名称与您的Omega相同，默认密码为 12345678

![](../img/setup-1-connet-to-wifi.png)

### 安装向导

打开您喜欢的浏览器，并访问`http://omega-ABCD.local/` 这里的ABCD是与上面网络名称相同的字符。如果网页无法正常加载，那请访问`http://192.168.3.1`

你将会看到如下向导

![](../img/setup-2-wizard-start.png)

使用 Omega的默认账号登录
```
username: root
password: onioneer
```

![](../img/setup-3-wizard-login.png)

登录后，系统会要求您连接到无线网络。 这是必须的，方便完成安装向导。

![](../img/setup-4-wizard-wifi-configure.png)

输入您的无线网络信息，然后单击配置。 您的Omega将尝试连接到网络。 这可能需要一分钟左右才能完成。

> 这段时间内，Omega将会和你的计算机断开连接，无法访问，待Omega自动配置完成后会和你的计算机恢复连接

恢复连接后，配置会接着进行

![](../img/setup-5-wizard-wifi-configuring.png)

在此步骤中，您可以选择在onion云上注册设备。在选择之后，您可以单击跳过步骤移至下一步。

![](../img/setup-6-wizard-cloud.png)

到目前已经快完成安装了，单击`Upgrade Firmware and Install Console`,就会升级Omega系统并安装控制台。

> 如果您不想安装控制台，您可以取消选择上面的复选框。 您可以随时返回安装向导以安装控制台。

![](../img/setup-7-wizard-upgrade-button.png)

您的Omega将下载最新的固件，然后开始安装。 此过程需要几分钟，速度取决于您的网速。

![](../img/setup-8-wizard-installing-firmware.png)

当固件完成安装时，页面是这样子的

![](../img/setup-9-wizard-finished.png)

在安装过程结束时，Omega将自动重新启动。 当Omega的LED停止闪烁并保持稳定时，它就可以继续使用了。

> 某些Omega2 +型号可能无法自动重新启动。 如果您到达上图所示的页面，并且您的Omega2 +的LED关闭并保持关闭超过约15秒，您将需要手动重新启动您的Omega。
> 或者切换Dock上的电源开关，或者短暂断开电源并重新连接，Omega2 +将重新启动并完成升级。 当LED停止闪烁并保持稳定时，可以使用。

### 可以啦

开始使用你Omega，查看使用Omega部分来了解Omega的使用方法！

# 如果无法设置

如果由于某些原因安装向导无法使您的Omega启动并运行，请尝试使用命令行指南的首次设置中的步骤或查看故障排除指南。

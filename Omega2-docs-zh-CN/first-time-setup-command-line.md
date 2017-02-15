# [使用命令行初始化](#使用命令行初始化)

按照本指南，使用命令行初始化您的Omega2。

## 仅当安装向导无法使您的Omega2启动并运行时，才需要遵循本指南。 如果安装向导成功，您不必执行这些步骤！

我们将进行如下操作
* 1.连接Omega到电源拓展坞上并启动它。
* 2.连接到它的命令行终端。
* 3.设置Omega来连接到你的wifi网络，并然它来联网更新。

> 如果您在此过程中的任何时候遇到问题，请尝试查看您的疑难解答指南。

>拆包及其他设置请阅读上篇教程至 <连接到Omega的wifi网络>

# [连接到Omega的命令行]

我们将使用SSH连接到Omega命令行

> 至于学习命令行使用请阅读[连接Omega命令行](connecting-to-the-omega-terminal.html)

### 提供Omega的wifi

现在让我们连接Omega到你的WiFi网络，让它联网。我们将使用wifisetup命令开始。

键入`wifisetup`,查看回显。

```
root@Omega-2757:/# wifisetup
Onion Omega Wifi Setup

Select from the following:
1) Scan for Wifi networks
2) Type network info
q) Exit

Selection:
```

你可以键入1，你的Omega将扫描可用网络

```
Selection: 1
Scanning for wifi networks...

Select Wifi network:
1) BYB
2) studio sixteen
3) EG Energy
4) mayaaa
5) Authentic
6) OnionWiFi
7) Orpheus
8) Omega-18C2

Selection:
```

输入您的选择，如果需要，将提示您输入密码。 将在扫描中自动检测到您的网络身份验证类型：

```
Selection: 6
Network: OnionWiFi
Authentication type: WPA2PSK
Enter password:
```

输入您的密码，然后按Enter键。 您的Omega的网络适配器将重新启动并尝试连接到新网络。

由于网络适配器正在重新启动，Omega的AP将在此期间关闭并且无法访问，但将在大约30秒内恢复。

> 有关Omega无线功能的更多信息，请参阅的Omega和Wireless指南。

# [更新固件](#更新固件)

现在我们将你的Omega连接到互联网，让我们更新Omega的固件到最新版本。

在终端中输入`oupgrade`命令以下载并安装最新版本的Omega操作系统。 更新将需要五分钟，主要取决你的网速。

#### 注意不要断开wifi或者电源，否则固件可能会损坏。

在安装过程结束时，Omega将自动重新启动。 当Omega的LED停止闪烁并保持稳定时，就可以使用了。

> 某些Omega2 +型号可能无法自动重新启动。 如果您的Omega2 +的LED关闭并保持关闭超过约15秒，您将需要手动重新启动您的Omega。
> 或者切换Dock上的电源开关，或者短暂断开电源并重新连接，Omega2 +将重新启动并完成升级。 当LED停止闪烁并保持稳定时，可以使用。

### 现在完成了

开始使用你Omega，查看使用Omega部分来了解Omega的使用方法！

# [如果不工作了](#如果不工作了)

请尝试查看我们的疑难解答指南或在[Onion的社区](https://community.onion.io/)发帖。

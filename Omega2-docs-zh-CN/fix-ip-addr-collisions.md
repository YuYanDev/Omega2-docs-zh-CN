# [修复网络地址冲突](#修复网络地址冲突)

如果您未能将Omega连接到家庭WiFi网络，并确保密码是100％正确，您的WiFi网络和Omega的AP网络之间可能会有IP地址冲突。

### [什么是ip地址冲突](#什么是ip地址冲突)

如果您的Omega的接入点和您尝试连接的WiFi网络共享同一个子网，您的Omega可能会发生IP地址冲突。 Omega的接入点子网是`192.168.3.0/24`，可能你的WiFi可以有相同的子网。 这导致Omega不知道要向什么地方发送数据。

我们将使用类比来简要解释这是如何工作的。 说一个IP地址是一封信上的街道地址。 您可以将子网视为该地址的城市。 所以如果你的Omega的子网和WiFi网络相同，你试图发送数据到某个IP地址，它就像发送一封信到法国巴黎的一个地址，但然后到达同一地址，但在巴黎， 德克萨斯州，美国。 不是我们想要的，但一个很好的尝试。

> 你可以阅读更多关于[子网和网络前缀](https://en.wikipedia.org/wiki/Subnetwork)在维基百科的子网上的文章。

#### 识别您的WiFi网络的IP地址前缀

如果您的WiFi网络的IPv4地址为192.168.3.X，则会发生IP地址冲突，其中X是0-255之间的任何数字。 要查找您的IPv4地址，您需要先将计算机连接到WiFi网络。 然后，根据操作系统，你必须得到你的无线配置设置。

### [修复冲突](#修复冲突)

有两种可能的解决方案来修复冲突。
* 1.更改Omega的AP网络前缀。
  * 这是方法很简单，将在下面讲述。
* 2.第二个是更改路由器的网络前缀。
  * 这是比较复杂的，本指南不会涉及。(实际更简单)

首先，连接到Omega的命令行界面。

要更改Omega的IP地址，我们可以使用uci，这是一个命令行工具，允许我们使用简单的命令编辑配置文件。 修改Omega的IP地址的命令如下：
```
uci set network.wlan.ipaddr=<IP ADDRESS>
```

例如，我们可以通过输入以下内容将Omega的IP地址更改为`192.168.9.1`：
```
uci set network.wlan.ipaddr=192.168.9.1
```

现在，我们设置了IP地址，我们将保存此更改。 保存设置的命令如下所示：
```
uci commit <CONFIGURATION>
```

正在更改的配置是网络，因此我们将输入以下内容以保存更改：
```
uci commit network
```

现在，一旦您保存了设置，您需要重新启动网络，以使用此命令应用更改：
```
/etc/init.d/network restart
```

就是这样！ 您的Omega的接入点的新IP地址现在是192.168.9.1，就不会有冲突了。 您现在可以尝试重新连接到您的WiFi网络。
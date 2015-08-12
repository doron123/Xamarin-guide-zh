#Xamarin 防火墙配置说明

`白名单中的终端`


在您的防火墙中需要添加的白名单列表，以允许Xamarin平台可以在贵公司工作。 


##概述
为便于Xamarin产品安装和正常工作, 某些终端必须是可访问的，才能为您的软件下载需要的工具和更新。如果您或您的公司有严格的防火墙设置, 您可能会遇到安装、许可证、组件等等问题。本文档列出了一些已知的，需要加到白名单中以便让Xamarin工作的终端的大纲。
本列表不包括在下载中需要包含的任何第三方工具的终端。
如果在加上此列表后，您仍然遇到麻烦, 参阅Apple或Android安装疑难解答指南, 或直接联系Xamarin支持。


##白名单中的终端

###Xamarin 安装
在使用Xamarin的最新版本的安装程序时，为正确安装软件将需要添加以下已知地址：

* xamarin.com (安装清单)
* download.xamarin.com (Mono, GTK#, Windows的Java SDK  )
* dl.google.com (下载 Android SDK)
* log.xamarin.com (我们的日志服务器)
* 在Xamarin安装清单中指定的安装下载地址(目前就是上面所指的那些主机)

如果您使用Mac和遇到Xamarin.Android安装问题, 请确保这台苹果电脑能够下载Java。

###账号登录和订阅激活
为确保人们正确授权和用户帐户激活，以下地址将需要添加：

* store.xamarin.com
* auth.xamarin.com

###组件商店和 NuGet (包括 Xamarin.Forms)
如果你计划使用 Xamarin 组件商店或NuGet (Xamarin.Forms是NuGet的一个包)，下面的地址将需要添加：

* components.xamarin.com (以使用Xamarin组件商店)
* xamarin-components.s3.amazonaws.com (组件商店下载主机)
* www.nuget.org (以访问NuGet)
* az320820.vo.msecnd.net (NuGet下载)
* dl-ssl.google.com (Google组件)

###软件更新
下面的地址将需要添加以确保软件更新能正确下载：

* software.xamarin.com (更新服务器)
* cdn1.xamarin.com
* download.xamarin.com


##小结
本指南包括白名单中的终端，以便Xamarin产品在您的计算机正确安装和更新。

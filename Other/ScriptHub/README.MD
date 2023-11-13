## 项目地址&文档

* [项目地址](https://github.com/Script-Hub-Org/Script-Hub/tree/main)
* [文档](https://github.com/Script-Hub-Org/Script-Hub/wiki)

## 功能

• 支持将 QX 重写解析至 Surge Shadowrocket Loon Stash

• 支持将 Surge 模块解析至 Loon Stash

• 支持将 Loon 插件解析至 Surge Shadowrocket Stash

• 支持 QX & Surge & Loon & Shadowrocket & Clash 规则集解析，适用 app: Surge Shadowrocket Stash Loon (注：不支持 域名集 IP-CIDR 集)

• 支持 将 QX 脚本转换成 Surge 脚本(兼容)

• 支持一键导入 Shadowrocket / Loon

## 使用方法

> 使用前请`配置并信任证书`，开启`MitM、Rewrite`等相关功能

> 不适用于 Quantumult X（有解析器要啥Script Hub啊

### 安装对应的模块/插件/覆写

• Surge Shadowrocket Egern LanceX 模块
```
https://raw.githubusercontent.com/Script-Hub-Org/Script-Hub/main/modules/script-hub.surge.sgmodule
```

• Stash 覆写
```
https://raw.githubusercontent.com/Script-Hub-Org/Script-Hub/main/modules/script-hub.stash.stoverride
```

• Loon 插件
```
https://raw.githubusercontent.com/Script-Hub-Org/Script-Hub/main/modules/script-hub.loon.plugin
```

### 访问 Script hub

在安装完成, 并且更新全部外部资源之后:

浏览器正常访问 https://script.hub/

<img src="https://ghproxy.com/https://github.com/Repcz/Open-Proflies/blob/main/Surge/Photo/ScriptHub/5.PNG" width="1200">

### 转换代理软件资源

此处以 QX的重写 转换成 Surge模块 简单举例 ：

> 请勿使用以`https://quantumult.app/x/open-app/`开头的链接，这些通常是URL Scheme链接，通过[URL编解码工具](https://the-x.cn/UrlDecode.aspx)即可获取解码后的原始资源链接

* [*@RuCu6*](https://github.com/RuCu6/QuanX) 的去广告重写

```
https://github.com/RuCu6/QuanX/blob/main/Rewrites/MyBlockAds.conf
```
* 获取其raw格式地址

```
https://raw.githubusercontent.com/RuCu6/QuanX/main/Rewrites/MyBlockAds.conf
```

![1](https://ghproxy.com/https://github.com/Repcz/Open-Proflies/blob/main/Surge/Photo/ScriptHub/6.PNG)

* 选择`来源类型`以及`目标类型`
> 点击查看 [如何选择选择来源类型和目标类型](https://github.com/Script-Hub-Org/Script-Hub/wiki/%E6%88%91%E5%BA%94%E8%AF%A5%E6%80%8E%E4%B9%88%E9%80%89%E6%8B%A9%E6%9D%A5%E6%BA%90%E7%B1%BB%E5%9E%8B%E5%92%8C%E7%9B%AE%E6%A0%87%E7%B1%BB%E5%9E%8B)

* 按需修改参数后，点击复制，在Surge中安装

<img src="https://ghproxy.com/https://github.com/Repcz/Open-Proflies/blob/main/Surge/Photo/ScriptHub/7.PNG" width="900">

### 借助 Scriptable 将转换后的 Surge模块 一键导入本地
> 需在`Surge`-`更多`-`设置`-`配置同步`-`勾选iCloud云盘`

* 下载 [Scriptable](https://apps.apple.com/app/id1405459188)

* 安装快捷指令 `install Scriptable`：https://www.icloud.com/shortcuts/9fc040fb09334faf9d323707aeedd9cc  
> 须在 `系统设置` - `快捷指令` - 勾选 `私人共享`，`高级` - 勾选 `允许运行脚本`

<img src="https://ghproxy.com/https://github.com/Repcz/Open-Proflies/blob/main/Surge/Photo/ScriptHub/8.PNG" width="1200">

* 浏览器访问 https://raw.githubusercontent.com/Script-Hub-Org/Script-Hub/main/SurgeModuleTool.js

* 点击下方 `共享` 按钮(此处为Safari浏览器)，下滑找到并点击快捷指令 `install Scriptable`

* 给予 快捷指令 访问网站权限后，会自动将脚本安装到 `Scriptable`

> 也可直接复制脚本内容粘贴到 `Scriptable` 内，并非一定要借助快捷指令

<img src="https://ghproxy.com/https://github.com/Repcz/Open-Proflies/blob/main/Surge/Photo/ScriptHub/9.PNG" width="900">

* 回到 https://script.hub/ ，填入链接，选择 `来源类型` 以及 `目标类型` ，按需修改参数后，点击 `一键导入`

* 在 `Scriptable` 中打开，会自动将模块文件保存到 iCloud 中的 Surge 目录下，点击 `保存/移动`

* 自动回到 `Scriptable` 中，点击 `打开Surge`，检查是否安装，并勾选启用模块

<img src="https://ghproxy.com/https://github.com/Repcz/Open-Proflies/blob/main/Surge/Photo/ScriptHub/11.PNG" width="1500">

#### 更新安装在本地的模块

在 `Scriptable` 中 点击 `SurgeModuleTool`

通过以下方法更新模块：

* 更新全部: 选择 iCloud/Surge 里你放模块的文件夹

* 更新单个文件: 选择某个模块文件进行更新

* 从链接下载: 输入名字和链接下载模块到指定目录

* URL Scheme 调用: scriptable:///run/SurgeModuleTool?url=&name=

<img src="https://ghproxy.com/https://github.com/Repcz/Open-Proflies/blob/main/Surge/Photo/ScriptHub/12.PNG" width="300">

---
参考：
* [Script Hub Wiki](https://github.com/Script-Hub-Org/Script-Hub/wiki)
* [相关生态: Surge 模块工具](https://github.com/Script-Hub-Org/Script-Hub/wiki/%E7%9B%B8%E5%85%B3%E7%94%9F%E6%80%81:-Surge-%E6%A8%A1%E5%9D%97%E5%B7%A5%E5%85%B7)
* https://t.me/ScriptablePRO


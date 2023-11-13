# Surge

### Surge iOS 下载地址

<a href="https://apps.apple.com/app/id1442620678"><img width="200px" alt="Download on App Store" src="https://logos-download.com/wp-content/uploads/2016/06/Download_on_the_App_Store_logo.png"/></a>  


导入配置
---

### 1.添加 **配置文件** 
> 配置参数解释见：_[GetSomeCats/Surge](https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/SurgePro.conf)_

```
https://ghproxy.com/https://raw.githubusercontent.com/Repcz/Open-Proflies/main/Surge/Surge.conf
```
* 运行 **Surge** ，在 **首页** ， 点击 **顶部区域**
* 弹出的 **设置** 菜单中，在下方 **导入** 区域，点击 **从URL下载配置**
* 将配置文件链接填入并保存
![Image text](https://github.com/Repcz/Open-Proflies/blob/main/Surge/Photo/1.PNG)

### 2.添加机场订阅
> 机场订阅本地转换可参考[Sub-Store 教程](https://github.com/Repcz/Open-Proflies/wiki/Sub-Store)

*  在 **首页**  —— **通用** 中， 点击 **代理服务器** 
* 弹出的菜单中，在 **策略组** 最下方 ，点击 **新的策略组**
* **组名称** 填写为 机场名称，并下拉至最下方
* 勾选 **使用外部代理列表** ，并填写 **机场订阅**

![Image text](https://github.com/Repcz/Open-Proflies/blob/main/Surge/Photo/2.PNG) 

### 3.将 机场订阅策略组 导入 手动选择策略组

*  在 **首页**  —— **通用** ， 点击 **代理服务器** 
* 弹出的菜单中，在 **策略组** 最上方 ，点击 **手动选择**，并在弹出的菜单中，下拉至最下方
* 点击 **包含另一个策略组的策略** ，在弹出的页面中，勾选刚才生成的 包含机场订阅的策略组

> 此时，`手动选择`策略组 即为显示所有节点的策略组；如果要添加多个机场，重复 2、3 步骤即可


![Image text](https://github.com/Repcz/Open-Proflies/blob/main/Surge/Photo/3.PNG) 

### 4.为配置文件生成证书
* 在 **首页**  —— **修改** ，点击 **MitM** 区域的 **配置根证书** 
* 弹出的菜单中，点击 **生成新的CA证书**
* 在弹出的菜单中，点击 **安装证书**
![Image text](https://github.com/Repcz/Open-Proflies/blob/main/Surge/Photo/4.PNG) 

* **确定** 提示后，在Safari中 **允许** 下载配置文件
* 并勾选 **MitM** 、**Rewrite** 、**脚本** 的开关

### 5.设置中安装描述文件
> 此处借用QX的图

* 在 **系统设置** 中，点击 **已下载描述文件** ，并 **安装**
![Image text](https://github.com/Repcz/Open-Proflies/blob/main/QuantumultX/Photo/%E8%AE%BE%E7%BD%AE-%E5%AE%89%E8%A3%85%E8%AF%81%E4%B9%A6.jpg)

### 6.设置中信任描述文件
* 在 **系统设置** - **通用** - **关于本机** - **证书信任设置** 中，勾选已安装的描述文件
![Image text](https://github.com/Repcz/Open-Proflies/blob/main/QuantumultX/Photo/%E8%AE%BE%E7%BD%AE-%E4%BF%A1%E4%BB%BB%E8%AF%81%E4%B9%A6.jpg)

### 7.导入模块
* **首页** —— **通用** —— **模块** 中，点击 **模块** 按钮
* 弹出的页面中，下滑至 **安装的模块** 最下方，点击 **安装新模块**
* 将模块链接(raw链接)填入并保存，等待下载外部资源
* 下载完成后，点击最下方的 **调整生效顺序**，按需调整模块生效顺序


自用模块
---

### 可直接在线安装或安装至本地的模块

|模块名称|链接|模块介绍|说明|
| :------------- | :-------------------------------------  | :------------------------------------------ | :------------------------------------------ |
| iRingo: 📍 Location & 🗺️ Maps|https://raw.githubusercontent.com/VirgilClyne/iRingo/raw/main/sgmodule/Location.sgmodule |全面自定义「定位服务」与「地图」的功能。|使用说明见[项目地址](https://github.com/VirgilClyne/iRingo/wiki)|
| iRingo: 🔍 Siri & Search|https://raw.githubusercontent.com/VirgilClyne/iRingo/main/sgmodule/Siri.sgmodule|全面自定义「Siri与搜索」的功能。|使用说明见[项目地址](https://github.com/VirgilClyne/iRingo/wiki)|
|🍟 Fries: 🌐 General Enhanced|https://raw.githubusercontent.com/VirgilClyne/GetSomeFries/main/sgmodule/General.sgmodule|(📱 iOS版) 1.添加跳过代理部分段内容 2.添加返回真实IP段内容 3.添加不可MitM的域名，防止打断连接|使用说明见[项目地址](https://github.com/VirgilClyne/GetSomeFries/wiki/🌐-通用)|
|🍟 Fries: 🚫 Block HTTPDNS|https://github.com/VirgilClyne/GetSomeFries/raw/main/sgmodule/HTTPDNS.Block.sgmodule|阻止常见的 HTTPDNS 服务器|使用说明见[项目地址](https://github.com/VirgilClyne/GetSomeFries/wiki/🚫-HTTPDNS)|
|🍿️ DualSubs: ▶️ YouTube feat.ADs|https://github.com/DualSubs/YouTube/raw/main/sgmodule/DualSubs.YouTube.feat.ADs.sgmodule|YouTube字幕增强及双语模块(配合去广告)|使用说明见[项目地址](https://github.com/DualSubs/YouTube/wiki/🍿-DualSubs:-▶-YouTubE)|
|📺 BiliBili: ⚙ Enhanced|https://github.com/BiliUniverse/Enhanced/raw/main/modules/BiliBili.Enhanced.sgmodule|哔哩哔哩：增强模式（中国站功能增强及UI自定义）|使用说明见[项目地址](https://github.com/BiliUniverse/Universe)|
|📺 BiliBili: 🌐 Global|https://github.com/BiliUniverse/Global/raw/main/modules/BiliBili.Global.sgmodule|哔哩哔哩：全球模式（中国站自动线路及全区搜索）|使用说明见[项目地址](https://github.com/BiliUniverse/Universe)|
|📺 BiliBili: 🛡️ ADBlock|https://github.com/BiliUniverse/ADBlock/raw/main/modules/BiliBili.ADBlock.sgmodule|哔哩哔哩：去广告|使用说明见[项目地址](https://github.com/BiliUniverse/Universe)|
|BoxJs|https://raw.githubusercontent.com/chavyleung/scripts/master/box/rewrite/boxjs.rewrite.surge.sgmodule||
|Sub-Store|https://raw.githubusercontent.com/Peng-YM/Sub-Store/master/config/Surge.sgmodule|高级订阅管理工具 @Peng-YM|使用方法见[Sub-Store 教程](https://github.com/Repcz/Open-Proflies/wiki/Sub-Store)|
|Script Hub: 重写 & 规则集转换|https://raw.githubusercontent.com/Script-Hub-Org/Script-Hub/main/modules/script-hub.surge.sgmodule|将其他代理软件的资源进行转换|[项目地址](https://github.com/Script-Hub-Org/Script-Hub/tree/main)   [使用方法](https://github.com/Repcz/Open-Proflies/wiki/Script-Hub)|
|Network Info Panel-CN|https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/Panel/Network-Info/Moore/Network-Info-CN.sgmodule|详细的显示你当前的网络信息|显示网络信息的面板|
|显示机场流量信息|https://raw.githubusercontent.com/getsomecat/GetSomeCats/Surge/modules/Panel/Sub-info/Moore/Sub-info.sgmodule|须安装至`本地`|[教程](https://surge.tel/09/1996/)|
|0.MITM ALL|https://raw.githubusercontent.com/Repcz/Open-Proflies/main/Surge/Module/0.MITM%20ALL.sgmodule|解密所有 HTTPS 流量 搭配`抓取流量`使用|
|0.Tun Only|https://raw.githubusercontent.com/Repcz/Open-Proflies/main/Surge/Module/0.Tun%20Only.sgmodule|启用 Tun Only 模式|
|1.Hide VPN Icon|https://raw.githubusercontent.com/Repcz/Open-Proflies/main/Surge/Module/1.Hide%20VPN%20Icon.sgmodule|隐藏状态栏上的 VPN 图标|


### 须安装 [Script Hub](https://raw.githubusercontent.com/Script-Hub-Org/Script-Hub/main/modules/script-hub.surge.sgmodule)后才可安装的模块

> 以下模块链接均为`Script Hub`处理后的链接；链接中/start_/`xxxxx`/_end_/ 的 `xxxxx`即为转换前的资源链接

> 使用方法：https://github.com/Repcz/Open-Proflies/wiki/Script-Hub

|模块名称|链接|模块说明|作者|
| :------------- | :--- | :-- | :---|
|功能｜B站字幕翻译|http://script.hub/file/_start_/https://raw.githubusercontent.com/ddgksf2013/Rewrite/master/Function/Bilibili_CC.conf/_end_/Bilibili_CC.sgmodule?n=%E5%8A%9F%E8%83%BD%EF%BD%9CB%E7%AB%99%E5%AD%97%E5%B9%95%E7%BF%BB%E8%AF%91%2B%40ddkgsf2013&type=qx-rewrite&target=surge-module|翻译繁体字幕|作者[*@ddgksf2013*](https://github.com/ddgksf2013/)|
|功能｜Q-Search|http://script.hub/file/_start_/https://raw.githubusercontent.com/Repcz/Open-Proflies/main/Surge/Module/Q-Search.sgmodule/_end_/Q-Search.sgmodule?n=%E5%8A%9F%E8%83%BD%EF%BD%9CQ-Search%2B%40ddkgsf2013&type=surge-module&target=surge-module|使用方法详见[说明](https://raw.githubusercontent.com/Repcz/Open-Proflies/main/Surge/Module/Q-Search.sgmodule/_end_/Q-Search.sgmodule)，默认`Bing`为搜索引擎|作者[*@ddgksf2013*](https://github.com/ddgksf2013/)|
|功能｜TestFlight区域限制解除|http://script.hub/file/_start_/https://raw.githubusercontent.com/NobyDa/Script/master/Surge/Module/TestFlightDownload.sgmodule/_end_/TestFlightDownload.sgmodule?n=%E5%8A%9F%E8%83%BD%EF%BD%9CTestFlight%E5%8C%BA%E5%9F%9F%E9%99%90%E5%88%B6%E8%A7%A3%E9%99%A4%2B%20%E8%AF%A5%E6%A8%A1%E5%9D%97%E9%80%82%E7%94%A8%E4%BA%8E%E6%9B%B4%E6%96%B0TestFlight%20App%E6%97%B6%2C%20%E6%8F%90%E7%A4%BA%22APP%E4%B8%8D%E5%8F%AF%E7%94%A8%22%E9%97%AE%E9%A2%98.&type=surge-module&target=surge-module|该模块适用于更新TestFlight App时, 提示"APP不可用"问题. |作者[*@NobyDa*](https://github.com/NobyDa/)|
|功能｜京东历史价格|http://script.hub/file/_start_/https://raw.githubusercontent.com/githubdulong/Script/master/jd_price2.sgmodule/_end_/jd_price2.sgmodule?n=%E5%8A%9F%E8%83%BD%EF%BD%9C%E4%BA%AC%E4%B8%9C%E5%8E%86%E5%8F%B2%E4%BB%B7%E6%A0%BC%2B%40githubdulong&type=surge-module&target=surge-module||作者[*@githubdulong*](https://github.com/githubdulong/)|
|功能｜解除微信链接限制|http://script.hub/file/_start_/https://raw.githubusercontent.com/zZPiglet/Task/master/UnblockURLinWeChat.sgmodule/_end_/UnblockURLinWeChat.sgmodule?n=%E5%8A%9F%E8%83%BD%EF%BD%9C%E8%A7%A3%E9%99%A4%E5%BE%AE%E4%BF%A1%E9%93%BE%E6%8E%A5%E9%99%90%E5%88%B6%2B%40zZPiglet&type=surge-module&target=surge-module||作者[*@zZPiglet*](https://github.com/zZPiglet/)|
|去广告｜App&小程序净化合集|http://script.hub/file/_start_/https://raw.githubusercontent.com/fmz200/wool_scripts/main/QuantumultX/rewrite/cleanup.snippet/_end_/cleanup.sgmodule?n=%E5%8E%BB%E5%B9%BF%E5%91%8A%EF%BD%9CApp%26%E5%B0%8F%E7%A8%8B%E5%BA%8F%E5%87%80%E5%8C%96%E5%90%88%E9%9B%86%2B%40fmz200&type=qx-rewrite&target=surge-module|详见[TG频道](https://t.me/Aa28413761/643) |作者[*@fmz200*](https://github.com/fmz200/)|
|去广告｜Bing搜索|http://script.hub/file/_start_/https://raw.githubusercontent.com/ddgksf2013/Rewrite/master/AdBlock/BingSimplify.conf/_end_/BingSimplify.sgmodule?n=%E5%8E%BB%E5%B9%BF%E5%91%8A%EF%BD%9CBing%E6%90%9C%E7%B4%A2%2B%40ddkgsf2013&type=qx-rewrite&target=surge-module|净化Bing网页版 |作者[*@ddgksf2013*](https://github.com/ddgksf2013/)|
|去广告｜IT之家|http://script.hub/file/_start_/https://gitlab.com/lodepuly/vpn_tool/-/raw/main/Tool/QuantumultX/Rewrite/IThome_remove_ads.snippet/_end_/IThome_remove_ads.sgmodule?n=%E5%8E%BB%E5%B9%BF%E5%91%8A%EF%BD%9CIT%E4%B9%8B%E5%AE%B6%2B%40%E5%8F%AF%E8%8E%89&type=qx-rewrite&target=surge-module||作者[*@iKeLee*](https://gitlab.com/lodepuly/vpn_tool)|
|去广告｜Keep|http://script.hub/file/_start_/https://raw.githubusercontent.com/Maasea/sgmodule/master/KeepAds.sgmodule/_end_/KeepAds.sgmodule?n=%E5%8E%BB%E5%B9%BF%E5%91%8A%EF%BD%9CKeep%2B%40Maasea&type=surge-module&target=surge-module||作者[*@Maasea*](https://github.com/Maasea/)|
|去广告｜MyBlockAds|http://script.hub/file/_start_/https://raw.githubusercontent.com/RuCu6/QuanX/main/Rewrites/MyBlockAds.conf/_end_/MyBlockAds.sgmodule?n=%E5%8E%BB%E5%B9%BF%E5%91%8A%EF%BD%9CMyBlockAds%2B%40RuCu6&type=qx-rewrite&target=surge-module|须启用分流规则里面的`MyblockAds @RuCu6` 详见[TG频道](https://t.me/Aa28413761/643) |作者[*@RuCu6*](https://github.com/RuCu6/QuanX)|
|去广告｜Youtube|http://script.hub/file/_start_/https://raw.githubusercontent.com/Maasea/sgmodule/master/YoutubeAds.sgmodule/_end_/YoutubeAds.sgmodule?n=%E5%8E%BB%E5%B9%BF%E5%91%8A%EF%BD%9CYoutube%2B%40Maasea&type=surge-module&target=surge-module||作者[*@Maasea*](https://github.com/Maasea/)|
|去广告｜什么值得买|http://script.hub/file/_start_/https://raw.githubusercontent.com/blackmatrix7/ios_rule_script/master/script/smzdm/smzdm_remove_ads.sgmodule/_end_/smzdm_remove_ads.sgmodule?n=%E5%8E%BB%E5%B9%BF%E5%91%8A%EF%BD%9C%E4%BB%80%E4%B9%88%E5%80%BC%E5%BE%97%E4%B9%B0%2B%40blackmatrix7&type=surge-module&target=surge-module||作者[*@Blackmatrix7*](https://github.com/blackmatrix7/ios_rule_script)|
|去广告｜小红书|http://script.hub/file/_start_/https://raw.githubusercontent.com/RuCu6/QuanX/main/Rewrites/Cube/xiaohongshu.snippet/_end_/xiaohongshu.sgmodule?n=%E5%8E%BB%E5%B9%BF%E5%91%8A%EF%BD%9C%E5%B0%8F%E7%BA%A2%E4%B9%A6%2B%40RuCu6&type=qx-rewrite&target=surge-module|详见[TG频道](https://t.me/Aa28413761/643) |作者[*@RuCu6*](https://github.com/RuCu6/QuanX)|
|去广告｜微信小程序|http://script.hub/file/_start_/https://raw.githubusercontent.com/ddgksf2013/Rewrite/master/AdBlock/Applet.conf/_end_/Applet.sgmodule?n=%E5%8E%BB%E5%B9%BF%E5%91%8A%EF%BD%9C%E5%BE%AE%E4%BF%A1%E5%B0%8F%E7%A8%8B%E5%BA%8F%2B%40ddkgsf2013&type=qx-rewrite&target=surge-module||作者[*@ddgksf2013*](https://github.com/ddgksf2013/)|
|去广告｜微博国际版|http://script.hub/file/_start_/https://raw.githubusercontent.com/kokoryh/Script/master/Surge/module/weibo_intl.sgmodule/_end_/weibo_intl.sgmodule?n=%E5%8E%BB%E5%B9%BF%E5%91%8A%EF%BD%9C%E5%BE%AE%E5%8D%9A%E5%9B%BD%E9%99%85%E7%89%88%2B%40kokoryh&type=surge-module&target=surge-module|不可与国内版微博去广告合用 |作者[*@kokoryh*](https://github.com/kokoryh/)|
|去广告｜知乎|http://script.hub/file/_start_/https://raw.githubusercontent.com/RuCu6/QuanX/main/Rewrites/Cube/zhihu.snippet/_end_/zhihu.sgmodule?n=%E5%8E%BB%E5%B9%BF%E5%91%8A%EF%BD%9C%E7%9F%A5%E4%B9%8E%2B%40RuCu6&type=qx-rewrite&target=surge-module|详见[TG频道](https://t.me/Aa28413761/643) |作者[*@RuCu6*](https://github.com/RuCu6/QuanX)|
|去广告｜菜鸟|http://script.hub/file/_start_/https://raw.githubusercontent.com/ddgksf2013/Rewrite/master/AdBlock/Cainiao.conf/_end_/Cainiao.sgmodule?n=%E5%8E%BB%E5%B9%BF%E5%91%8A%EF%BD%9C%E8%8F%9C%E9%B8%9F%2B%40ddkgsf2013&type=qx-rewrite&target=surge-module|包含菜鸟APP和支付宝小程序 |作者[*@ddgksf2013*](https://github.com/ddgksf2013/)|
|去广告｜高德地图|http://script.hub/file/_start_/https://raw.githubusercontent.com/RuCu6/QuanX/main/Rewrites/Cube/amap.snippet/_end_/amap.sgmodule?n=%E5%8E%BB%E5%B9%BF%E5%91%8A%EF%BD%9C%E9%AB%98%E5%BE%B7%E5%9C%B0%E5%9B%BE%2B%40RuCu6&type=qx-rewrite&target=surge-module|详见[TG频道](https://t.me/Aa28413761/643) |作者[*@RuCu6*](https://github.com/RuCu6/QuanX)|

---
更多使用方法及模块见：[Surge iOS入门](https://exaalices-organization.gitbook.io/surge-ios/)

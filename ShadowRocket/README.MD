# Shadowrocket

### Shadowrocket 下载地址

<a href="https://apps.apple.com/app/id932747118"><img width="200px" alt="Download on App Store" src="https://logos-download.com/wp-content/uploads/2016/06/Download_on_the_App_Store_logo.png"/></a>  



### 1. 手动导入配置文件

* 复制以下配置链接，打开 **Shadowrocket**

**_完整配置_**（包含去广告等多种分流规则）
```
https://ghproxy.com/https://raw.githubusercontent.com/Repcz/Open-Proflies/main/ShadowRocket/ShadowRocket.conf
```


**_简洁配置_**（仅支持国外分流，占用内存更小）
```
https://ghproxy.com/https://raw.githubusercontent.com/Repcz/Open-Proflies/main/ShadowRocket/ShadowRocket_lite.conf
```

* 点击底部工具栏 **配置** - **添加配置** - 填入链接并下载
* 点击 **本地文件** - **ShadowRocket.conf** - **使用配置**
![1](https://github.com/Repcz/Open-Proflies/blob/main/ShadowRocket/Photo/1.jpg)

### 2. 设置分流分组
* ~点击 **ShadowRocket.conf** 右边的 **ⓘ** 图标~

* ~点击 **代理分组**~

* 首页下拉即可进入 **代理分组** , 根据自己需求选择分流模式(无特殊需求可不更改，首页选择节点即可)


默认`国外流媒体`、`Telegram`、`推特`、`谷歌`、`微软`、`常见的国外网站`以及`不在规则内的网站`走proxy，即底部工具栏 **首页** 中选择的节点；

`国内网站`、`苹果`走直连。

![2](https://github.com/Repcz/Open-Proflies/blob/main/ShadowRocket/Photo/2.jpg)
图片懒得修改了🤣


### 3. 检查规则集URL
* 点击 **ShadowRocket.conf** 右边的 **ⓘ** 图标
* 点击 **规则集URL** ，确保都下载成功（有绿色的√）
![检查url](https://github.com/Repcz/Open-Proflies/blob/main/ShadowRocket/Photo/3.jpg)

<details>
   <summary>添加GeoLite2订阅（非必须）</summary> 

### 4. 添加**GeoLite2**订阅
> 项目地址：[Loyalsoldier/geoip](https://github.com/Loyalsoldier/geoip)
* 点击底部工具栏 **设置** ，点击下方 **Geolite2数据库**
* 在 **国家** 模块中的URL填入以下地址 ，并更新
```
https://cdn.jsdelivr.net/gh/Loyalsoldier/geoip@release/Country-only-cn-private.mmdb
```
![4](https://github.com/Repcz/Open-Proflies/blob/main/ShadowRocket/Photo/4.jpg)

</details>




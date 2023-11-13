### 使用前请确保软路由可以正常上网

**使用的软路由为 PHICOMM N1 ，固件为[F大82版Openwrt](https://www.right.com.cn/forum/thread-4076037-1-1.html)；SSH工具为[FinalShell](http://www.hostbuf.com/)**

订阅转换
---

#### [在线订阅转换（不推荐）](https://github.com/Repcz/Open-Proflies/wiki/Clash-For-Windows#%E5%9C%A8%E7%BA%BF%E8%AE%A2%E9%98%85%E8%BD%AC%E6%8D%A2%E4%B8%8D%E6%8E%A8%E8%8D%90)

#### [本地订阅转换（推荐）](https://github.com/Repcz/Open-Proflies/wiki/%E8%87%AA%E5%BB%BAsubconverter%E8%AE%A2%E9%98%85%E8%BD%AC%E6%8D%A2)


一些通用设置
---

### 插件设置

#### 模式设置

* 下拉至下方灰色按钮 ，点击 **切换页面到Fake-IP**
* 运行模式 - 修改为 **Fake-IP（TUN）模式**
* 其余保持默认，或和图中一致
  ![set1](https://github.com/Repcz/Open-Proflies/blob/main/Openclash/Photo/Setting/set1.png)

#### 流量控制

* 勾选 **路由本机代理** & **禁用QUIC**

#### DNS设置

* 本地DNS劫持 选择 **使用Dnsmasq转发**
* 勾选 **禁止Dnsmasq缓存DNS**
  ![2](https://github.com/Repcz/Open-Proflies/blob/main/Openclash/Photo/Setting/set2.png)

#### GEO数据库

* 建议勾选 **自动更新 GeoIP MMDB 数据库**
* 选择**自动更新 GeoIP MMDB 数据库** 为 **Hackl0us-Version**

#### 版本更新

* 建议第一次使用时，手动下载并上传内核
  * [Clash Dev Version:v1.15.1-2-gd713240](https://raw.githubusercontent.com/vernesong/OpenClash/core/master/dev/clash-linux-arm64.tar.gz)
  * [Clash TUN Version:2023.04.16-3-gb41bead](https://raw.githubusercontent.com/vernesong/OpenClash/core/master/premium/clash-linux-arm64-2023.04.16-3-gb41bead.gz)
  * [Clash Meta Version:alpha-g00939da](https://raw.githubusercontent.com/vernesong/OpenClash/core/master/meta/clash-linux-arm64.tar.gz)
* 将需要的内核下载并解压，分别重命名为clash（对应Dev内核）、clash_tun（对应TUN内核）、clash_meta（对应Meta内核）
* 使用SSH工具上传至 `/etc/openclash/core/` 目录下
* 后续使用中，更新客户端前务必备份好内核

***

### 覆写设置
#### 常规设置
* **Github地址** 中改为`https://cdn.jsdelivr.net/`;
* 如果可以稳定服务Github，地址可以改为 **停用**

#### DNS设置
* 如果使用我的配置，则取消勾选 **自定义上游 DNS 服务器** 
* 勾选 **Fake-IP 持久化**
  ![set3](https://github.com/Repcz/Open-Proflies/blob/main/Openclash/Photo/Setting/set3.png)

***

### 下载规则和节点订阅文件
* 使用[懒人方法](#opencalsh%E4%B8%AD%E6%B7%BB%E5%8A%A0%E5%9C%A8%E7%BA%BF%E9%85%8D%E7%BD%AE)可忽略

> 初次使用因软路由可能因无法科学上网导致无法下载节点订阅和规则文件，建议提前下载好规则文件，并上传

* 在目录`/etc/openclash/proxy_provider` 下新建 `all.yaml`
* 下载规则文件，重命名后，上传至 `/etc/openclash/rule_provider` ，具体规则列表如下

<details>
  <summary>规则列表</summary>

  * Direct.yaml: https://cdn.jsdelivr.net/gh/blackmatrix7/ios_rule_script@master/rule/Clash/Direct/Direct.yaml
  * Lan.yaml: https://cdn.jsdelivr.net/gh/blackmatrix7/ios_rule_script@master/rule/Clash/Lan/Lan.yaml
  * Download: https://cdn.jsdelivr.net/gh/blackmatrix7/ios_rule_script@master/rule/Clash/Download/Download.yaml
  * anti-ad-clash.yaml: https://anti-ad.net/clash.yaml
  * GlobalMedia.yaml: https://cdn.jsdelivr.net/gh/blackmatrix7/ios_rule_script@master/rule/Clash/GlobalMedia/GlobalMedia_Classical.yaml
  * Apple.yaml: https://cdn.jsdelivr.net/gh/blackmatrix7/ios_rule_script@master/rule/Clash/Apple/Apple_Classical.yaml
  * Microsoft.yaml: https://cdn.jsdelivr.net/gh/blackmatrix7/ios_rule_script@master/rule/Clash/Microsoft/Microsoft.yaml
  * Github.yaml: https://cdn.jsdelivr.net/gh/blackmatrix7/ios_rule_script@master/rule/Clash/GitHub/GitHub.yaml
  * Google.yaml: https://cdn.jsdelivr.net/gh/blackmatrix7/ios_rule_script@master/rule/Clash/Google/Google.yaml
  * Telegram.yaml: https://cdn.jsdelivr.net/gh/blackmatrix7/ios_rule_script@master/rule/Clash/Telegram/Telegram.yaml
  * Twitter.yaml: https://cdn.jsdelivr.net/gh/blackmatrix7/ios_rule_script@master/rule/Clash/Twitter/Twitter.yaml
  * BiliBili.yaml: https://cdn.jsdelivr.net/gh/blackmatrix7/ios_rule_script@master/rule/Clash/BiliBili/BiliBili.yaml
  * Game.yaml: https://cdn.jsdelivr.net/gh/blackmatrix7/ios_rule_script@master/rule/Clash/Game/Game.yaml
  * ChinaIP.yaml: https://cdn.jsdelivr.net/gh/soffchen/GeoIP2-CN@release/clash-rule-provider.yml
  * ProxyLite.yaml: https://cdn.jsdelivr.net/gh/blackmatrix7/ios_rule_script@master/rule/Clash/ProxyLite/ProxyLite.yaml

</details>

导入配置
---

### Opencalsh中添加在线配置
> 懒人方法

* 将[订阅转换](https://github.com/Repcz/Open-Proflies/wiki/Clash-For-Windows#%E8%AE%A2%E9%98%85%E8%BD%AC%E6%8D%A2%E6%87%92%E4%BA%BA%E6%96%B9%E6%B3%95)中的生成的链接，添加到 **配置文件订阅** 中
  ![1](https://github.com/Repcz/Open-Proflies/blob/main/Openclash/Photo/Opclash1.png)
  ![2](https://github.com/Repcz/Open-Proflies/blob/main/Openclash/Photo/Opclas2.png)
* 保存并更新配置
  ![3](https://github.com/Repcz/Open-Proflies/blob/main/Openclash/Photo/Opcalsh3.png)

***

### Opencalsh中添加本地配置

#### 1. 下载[Openclash.yaml](https://raw.githubusercontent.com/Repcz/Open-Proflies/main/Openclash/Openclash.yaml)至本地

#### 2. 修改配置 `proxy-providers` 中的机场订阅地址

> 在线订阅转换可能出现订阅泄露

```yaml
proxy-providers:
  Subscribe:
    <<: *p
    url: "https://sub.xeton.dev/sub?target=clash&url=你的订阅链接&list=true&udp=true"
    path: ./all.yaml
    # 可以使用任意类型的链接替换上面文字，多个链接使用英文符号的竖杠|隔开一起写上即可
    # 也可以使用在线订阅转换，在进阶模式中勾选`输出为Node List`，将Clash订阅链接转换为只包含节点信息的配置，并替换掉整个引号""内的链接
```

#### 3. 导入配置

* 在 **OpenClash** 中，找到 **配置管理** 
* 选择刚才修改好的文件并上传
* 在 **配置文件列表** 中找到刚才上传的文件，点击 **切换**
* 下拉至最下方，点击 **应用配置**
  ![1](https://github.com/Repcz/Open-Proflies/blob/main/Openclash/Photo/%E4%B8%8A%E4%BC%A0.png)

***

[返回顶部](https://github.com/Repcz/Open-Proflies/wiki/Openclash)

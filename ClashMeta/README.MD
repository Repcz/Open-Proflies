# Clash Meta


下载Clash.Meta内核客户端
---
### Windows平台
- [Clash Verge 下载地址](https://github.com/zzzgydi/clash-verge)
- [V2ray N 下载地址](https://github.com/2dust/v2rayN)
### Android平台
- [Clash.Meta for Android](https://github.com/MetaCubeX/ClashMetaForAndroid/releases/tag/Prerelease-alpha)


本地配置（推荐）
---
> 以处`Clash Verge`为例
#### 0.设置内核为 `Clash.Meta`
![！](https://github.com/Repcz/Open-Proflies/blob/main/ClashMeta/Photo/%E8%AE%BE%E7%BD%AE%E5%86%85%E6%A0%B8.png)
#### 1.新建`all.yaml`文件
* 打开Clash Verge，点击 **设置**，下拉找到**应用目录**，点击右侧箭头
* 在弹出的文件夹中，新建`all.yaml`文件
![1](https://github.com/Repcz/Open-Proflies/blob/main/ClashMeta/Photo/%E5%BA%94%E7%94%A8%E7%9B%AE%E5%BD%95.png)
![2](https://github.com/Repcz/Open-Proflies/blob/main/ClashMeta/Photo/%E5%A4%8D%E5%88%B6%E8%8A%82%E7%82%B9.png)
#### 2. Clash Verge 中导入 **配置**
* 打开Clash Verge，点击 **配置**，导入以下的链接
* 点击 **代理** ，设置分流

<details>
  <summary>CM.yaml</summary>

- [x] 地区分流（香港、美国、日本、台湾、新加坡、澳大利亚、英国、印度）
- [x] 苹果、谷歌、微软、电报、推特分流
- [x] 流媒体（不支持单独分流）
- [x] 自动选择最低延迟
- [ ] 负载均衡
- [ ] 故障转移
- [x] 广告屏蔽

</details>

```
https://ghproxy.com/https://raw.githubusercontent.com/Repcz/Open-Proflies/main/ClashMeta/CM.yaml
```

![订阅导入](https://github.com/Repcz/Open-Proflies/blob/main/ClashMeta/Photo/%E5%AF%BC%E5%85%A5%E9%85%8D%E7%BD%AE.png)


#### 3. 修改配置 `proxy-providers` 中的机场订阅地址
* 请自行将 `proxy-providers` 中的 `机场订阅` 替换为机场订阅地址

```yaml
proxy-providers:
  Subscribe: {<<: *p, path: ./all.yaml, url: 机场订阅}
    # Meta支持机场通用订阅
```

#### 4. 启用配置
* 选择导入的配置，右键-启用


订阅转换（懒人方法）
---
### 在线订阅转换
> 在线订阅转换可能出现订阅泄露
#### 1. 打开[ACL4SSR](https://acl4ssr-sub.github.io/) 
#### 2. 填入 **机场订阅** 和 **远程配置**

**_自用 多流媒体分组 自动测速 配置_**
```
https://raw.githubusercontent.com/Repcz/Open-Proflies/main/ClashMeta/Online_Full_Auto.ini
```
#### 3. 选择后端地址并生成订阅
* 强烈建议使用自建后端，自建后端订阅转换可以有效防止订阅泄露以及规则下载不全等问题，具体方法见[自建subconverter订阅转换](https://github.com/Repcz/Open-Proflies/wiki/%E8%87%AA%E5%BB%BAsubconverter%E8%AE%A2%E9%98%85%E8%BD%AC%E6%8D%A2)

![Image text](https://github.com/Repcz/Open-Proflies/blob/main/Clash/Photo/%E8%AE%A2%E9%98%85%E8%BD%AC%E6%8D%A2.PNG)

### 本地后端订阅转换（推荐）
详细使用方法见[自建subconverter订阅转换](https://github.com/Repcz/Open-Proflies/wiki/%E8%87%AA%E5%BB%BAsubconverter%E8%AE%A2%E9%98%85%E8%BD%AC%E6%8D%A2)


### 导入Clash Verge
* 打开Clash Verge，点击 **配置**，导入[订阅转换](#在线订阅转换不推荐-1)后的链接
* 点击 **代理** ，设置分流

![订阅导入](https://github.com/Repcz/Open-Proflies/blob/main/ClashMeta/Photo/%E5%AF%BC%E5%85%A5%E9%85%8D%E7%BD%AE.png)

策略组修改为手动选择节点
---
> 默认为自动选择延迟最低节点，**按需** 修改为手动选择
* 在自定义策略下的分流策略组中选择需要的地区节点，此处以 **国外网站** 举例，选择 **香港节点**
* 下拉到下方的 **香港节点** 策略组，此时该策略组以 `url-test` 运行，即按最低延迟选择节点
* 如果要修改为手动选择节点，则需要编辑配置文件，在 **配置** ，右键需要修改的配置文件，点击 **编辑**
* 找到` - {name: 🇭🇰 香港节点, <<: *auto, filter: "港|HK|(?i)Hong"}`，将 `*auto` 修改为 `*use`
* 在 **香港节点** 策略组中选择需要的节点，则 **国外网站** 策略组走 **香港节点** 中选择的节点

eg:
```yaml
...

 - {name: 🇭🇰 香港节点, <<: *auto, filter: "港|HK|(?i)Hong"}

👇

 - {name: 🇭🇰 香港节点, <<: *use, filter: "港|HK|(?i)Hong"}

...

```

Clash.Meta for Android
---
### 在线订阅转换（不推荐）
> 在线订阅转换可能出现订阅泄露
#### 1. 打开[ACL4SSR](https://acl4ssr-sub.github.io/) 
#### 2. 填入 **机场订阅** 和 **远程配置**

**_自用 多流媒体分组 自动测速 配置_**
```
https://raw.githubusercontent.com/Repcz/Open-Proflies/main/ClashMeta/Online_Full_Auto.ini
```
#### 3. 选择后端地址并生成订阅
* 强烈建议使用自建后端，自建后端订阅转换可以有效防止订阅泄露以及规则下载不全等问题，具体方法见[自建subconverter订阅转换](https://github.com/Repcz/Open-Proflies/wiki/%E8%87%AA%E5%BB%BAsubconverter%E8%AE%A2%E9%98%85%E8%BD%AC%E6%8D%A2)

![Image text](https://github.com/Repcz/Open-Proflies/blob/main/Clash/Photo/%E8%AE%A2%E9%98%85%E8%BD%AC%E6%8D%A2.PNG)

### 本地后端订阅转换（推荐）
详细使用方法见[自建subconverter订阅转换](https://github.com/Repcz/Open-Proflies/wiki/%E8%87%AA%E5%BB%BAsubconverter%E8%AE%A2%E9%98%85%E8%BD%AC%E6%8D%A2)


### 导入CMFA
* 打开CMFA，点击 **配置**，导入[订阅转换](#在线订阅转换)后的链接
* 点击 **运行** ，再点击 **代理** ，设置分流

![CFA订阅导入](https://github.com/Repcz/Open-Proflies/blob/main/Clash/Photo/CFA.jpg)

[回到顶部](#下载clashmeta内核客户端)
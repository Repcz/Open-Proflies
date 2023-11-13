# Clash For Android 使用方法

### Clash for Android 下载地址

<a href="https://play.google.com/store/apps/details?id=com.github.kr328.clash"><img width="200px" alt="Get it on Google Play" src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png"/></a> or [Github/releases](https://github.com/Kr328/ClashForAndroid/releases)


订阅转换（懒人方法）
---
### 在线订阅转换（不推荐）
> 在线订阅转换可能出现订阅泄露
#### 1. 打开[ACL4SSR](https://acl4ssr-sub.github.io/) 
#### 2. 填入 **机场订阅** 和 **远程配置**

**_自用 多流媒体分组 自动测速 配置_**
```
https://raw.githubusercontent.com/Repcz/Open-Proflies/main/Openclash/OP_Auto.ini
```
#### 3. 选择后端地址并生成订阅
* 强烈建议使用自建后端，自建后端订阅转换可以有效防止订阅泄露以及规则下载不全等问题，具体方法见[自建subconverter订阅转换](https://github.com/Repcz/Open-Proflies/wiki/%E8%87%AA%E5%BB%BAsubconverter%E8%AE%A2%E9%98%85%E8%BD%AC%E6%8D%A2)

![Image text](https://github.com/Repcz/Open-Proflies/blob/main/Clash/Photo/%E8%AE%A2%E9%98%85%E8%BD%AC%E6%8D%A2.PNG)

### 本地后端订阅转换（推荐）
详细使用方法见[自建subconverter订阅转换](https://github.com/Repcz/Open-Proflies/wiki/%E8%87%AA%E5%BB%BAsubconverter%E8%AE%A2%E9%98%85%E8%BD%AC%E6%8D%A2)


### 导入CFA
* 打开CFA，点击 **配置**，导入[订阅转换](#在线订阅转换)后的链接
* 点击 **运行** ，再点击 **代理** ，设置分流

![CFA订阅导入](https://github.com/Repcz/Open-Proflies/blob/main/Clash/Photo/CFA.jpg)


本地配置
---
> 仅在 3.0.3.premium 版本进行测试，低于此版本不保证可用性

`https://github.com/Repcz/Open-Proflies/blob/main/Clash/CFA.yaml`

### 1. 修改配置 `proxy-providers` 中的机场订阅地址
> 在线订阅转换可能出现订阅泄露
* 将 **配置** 保存在文件管理器中
* 参照下方填入机场订阅

```yaml

...
proxy-providers:
  Subscribe: {<<: *p， path: ./Subscribe.yaml， url: https://sub.xeton.dev/sub?target=clash&url=你的订阅链接&list=true&udp=true}
    # 可以使用任意类型的链接替换上面文字，多个链接使用英文符号的竖杠|隔开一起写上即可
    # Sub-Store生成的链接，可以直接替换上述url引号中的部分，具体见Sub-Store教程         
...

```
### 2.导入配置
* 在 配置 - 新配置 - 本地 中，导入修改的配置，并保存
* 等待其下载外部资源和校验

***

# Clash For Windows 使用方法

<details>
   <summary><s>Clash For Windows下载</s></summary>   
 
---
<s>Clash for Windows支持Windows、Mac、Linux平台</s>
* <s>下载地址：[Fndroid/
clash_for_windows_pkg/releases](https://github.com/Fndroid/clash_for_windows_pkg/releases) （原版，无中文）</s>
> <s>建议下载便携版`Clash.for.Windows-x.xx.xx-win.7z`，并于`Clash for Windows`目录下新建`data`文件夹，以启用便携模式</s>

> <s>如果不会解压7z文件，可以直接下载`Clash.for.Windows.Setup.0.xx.xx.exe`安装</s>
<s>* [CFW汉化补丁](https://github.com/BoyceLig/Clash_Chinese_Patch/releases)   </s>
> <s>下载 `app.7z` 或 `app.zip` 文件(两个压缩包内容一样)后，解压压缩包，请自行替换`Clash for Windows\resources\app.asar`目录中的 `app.asar` 文件</s>

</details>

一键导入订阅
---
#### 1. 购买机场订阅
#### 2. 点击一键导入机场配置

> 这里以某机场做举例，每个机场面板可能不太一样，以你买的机场为准

![1](https://github.com/Repcz/Open-Proflies/blob/main/Clash/Photo/one%20Shot.png)
![1](https://github.com/Repcz/Open-Proflies/blob/main/Clash/Photo/one%20Shot2.png)

### 导入预处理配置

> 此方法和后文中的`订阅转换`&`导入本地配置`不可同时使用

> 预处理导入配置无需使用订阅转换，可以规避订阅转换存在的风险

#### 1. 按上文导入订阅后，确保正常链接外网，启动系统代理
![1](https://github.com/Repcz/Open-Proflies/blob/main/Clash/Photo/System%20Proxy.png)

#### 2. 打开CFW 设置——配置——点击预处理右侧的编辑，会弹出一个编辑器
![2](https://github.com/Repcz/Open-Proflies/blob/main/Clash/Photo/%E8%AE%BE%E7%BD%AE%E9%A2%84%E5%A4%84%E7%90%86.png) 

#### 3. [点击链接](https://raw.githubusercontent.com/Repcz/Open-Proflies/main/Clash/parser.yaml)，复制里面的配置，在CFW弹出的编辑器里，替换原有内容，并保存
![3](https://github.com/Repcz/Open-Proflies/blob/main/Clash/Photo/Copy.png)
![3](https://github.com/Repcz/Open-Proflies/blob/main/Clash/Photo/Copy2.png)

#### 4. 打开CFW 配置，刷新配置，等待下载外部文件

> 如果出现下载失败的错误，多试几次就好

![4](https://github.com/Repcz/Open-Proflies/blob/main/Clash/Photo/Ctrl5.png)

订阅转换（懒人方法）
---
### 在线订阅转换
> 在线订阅转换可能出现订阅泄露
#### 1. 打开[ACL4SSR](https://acl4ssr-sub.github.io/) 
#### 2. 填入 **机场订阅** 和 **远程配置**

**_自用 多流媒体分组 自动测速 配置_**
```
https://raw.githubusercontent.com/Repcz/Open-Proflies/main/Clash/Online_Full_Auto.ini
```

**_自用 多流媒体分组 全手动 配置_**
```
https://raw.githubusercontent.com/Repcz/Open-Proflies/main/Clash/Online_Full_NoAuto.ini
```

#### 3. 选择后端地址并生成订阅
* 强烈建议使用自建后端，自建后端订阅转换可以有效防止订阅泄露以及规则下载不全等问题，具体方法见[自建subconverter订阅转换](https://github.com/Repcz/Open-Proflies/wiki/%E8%87%AA%E5%BB%BAsubconverter%E8%AE%A2%E9%98%85%E8%BD%AC%E6%8D%A2)

![Image text](https://github.com/Repcz/Open-Proflies/blob/main/Clash/Photo/%E8%AE%A2%E9%98%85%E8%BD%AC%E6%8D%A2.PNG)

### 导入CFW
* 打开CFW，点击 **配置**，导入[订阅转换](#订阅转换（懒人方法）)后的链接
* 点击 **代理** ，根据需要选择节点

![订阅导入](https://github.com/Repcz/Open-Proflies/blob/main/Clash/Photo/CFW%E5%AF%BC%E5%85%A5.png)

本地配置转换
---
> 建议有一定动手能力的用户使用
#### 1. CFW中导入 **配置**
按需求选择对应的配置，点击箭头查看配置所支持的功能

<details>
  <summary>CFW.yaml</summary>

- [x] 地区分流（香港、美国、日本、台湾、新加坡、~澳大利亚、英国、印度~）
- [x] 苹果、谷歌、微软、电报、推特分流
- [x] 流媒体（不支持单独分流）
- [x] 自动选择最低延迟
- [x] OpenAI
- [x] 负载均衡
- [x] 故障转移
- [x] 广告屏蔽

</details>

```
https://ghproxy.com/https://raw.githubusercontent.com/Repcz/Open-Proflies/main/Clash/CFW.yaml
```

2️⃣可同时使用2个机场接通
```
https://ghproxy.com/https://raw.githubusercontent.com/Repcz/Open-Proflies/main/Clash/CFW_②.yaml
```

3️⃣可同时使用3个机场
```
https://ghproxy.com/https://raw.githubusercontent.com/Repcz/Open-Proflies/main/Clash/CFW_③.yaml
```


<details>
  <summary>CFW_lite.yaml</summary>

- [ ] 地区分流
- [ ] 电报分流
- [ ] OpenAI
- [ ] 流媒体
- [ ] 自动选择最低延迟
- [ ] 负载均衡
- [ ] 故障转移
- [x] 广告屏蔽

</details>

```
https://ghproxy.com/https://raw.githubusercontent.com/Repcz/Open-Proflies/main/Clash/CFW_lite.yaml
```
* 打开CFW，点击 **配置**，根据需要导入配置链接
![订阅导入](https://github.com/Repcz/Open-Proflies/blob/main/Clash/Photo/CFW%E5%AF%BC%E5%85%A5.png)

#### 2. 修改配置 `proxy-providers` 中的机场订阅地址
> 在线订阅转换可能出现订阅泄露
* 点击 **配置** ，选中刚才导入的配置，右键 **编辑** 或 **从外部编辑**
* 参照下方填入机场订阅

```yaml

...
proxy-providers:
  Subscribe: {<<: *p, url: https://sub.xeton.dev/sub?target=clash&url=你的订阅链接&list=true&udp=true}
    # 可以使用任意类型的链接替换上面文字，多个链接使用英文符号的竖杠|隔开一起写上即可
    # Sub-Store生成的链接，可以直接替换上述url引号中的部分，具体见Sub-Store教程         
...

```
#### 3. 开启系统代理
* 常规 - 勾选 **系统代理**
![1](https://github.com/Repcz/Open-Proflies/blob/main/Clash/Photo/System%20Proxy.png)

#### *. 错误及解决方法
* 出现如下错误
```
 initial proxy provider TW error: doesn't match any proxy, please check your filter
```
* 解决方法
  - 删除对应的节点策略组

eg：
```yaml

...

#删除pr中的“, 🇨🇳 台湾节点”
pr: &pr {type: select, proxies: [🇭🇰 香港节点, 🇺🇲 美国节点, 🇸🇬 狮城节点, 🇯🇵 日本节点,  🇨🇳 台湾节点, ♻️ 自动选择, 🚀 手动切换, DIRECT]}

👇

pr: &pr {type: select, proxies: [🇭🇰 香港节点, 🇺🇲 美国节点, 🇸🇬 狮城节点, 🇯🇵 日本节点, ♻️ 自动选择, 🚀 手动切换, DIRECT]}

...

proxy-groups:

#删除proxy-groups中的“, 🇨🇳 台湾节点”
 - {name: 🎬 哔哩哔哩, type: select, proxies: [DIRECT, 🇭🇰 香港节点, 🇨🇳 台湾节点]}

👇

 - {name: 🎬 哔哩哔哩, type: select, proxies: [DIRECT, 🇭🇰 香港节点]}

...

#删除
# - {name: 🇨🇳 台湾节点, <<: *use, filter: "(?i)🇹🇼|台湾|(\b(TW|Tai|Taiwan)\b)"}

...

```





### 策略组修改为手动选择节点

> 默认为自动选择延迟最低节点，**按需** 修改为手动选择
* 在自定义策略下的分流策略组中选择需要的地区节点，此处以 **国外网站** 举例，选择 **香港节点**
* 下拉到下方的 **香港节点** 策略组，此时该策略组以 `url-test` 运行，即按最低延迟选择节点
* 如果要修改为手动选择节点，则需要编辑配置文件，在 **配置** ，右键需要修改的配置文件，点击 **编辑**
* 找到` - {name: 🇭🇰 香港节点, <<: *auto, filter: "港|HK|(?i)Hong"}`，将 `*auto` 修改为 `*select`
* 在 **香港节点** 策略组中选择需要的节点，则 **国外网站** 策略组走 **香港节点** 中选择的节点

eg:
```yaml
...

 - {name: 🇭🇰 香港节点, <<: *auto, filter: "港|HK|(?i)Hong"}

👇

 - {name: 🇭🇰 香港节点, <<: *select, filter: "港|HK|(?i)Hong"}

...
```
### 如何自行添加规则


* 首先了解一下Clash使用的[通用语法](https://wiki.metacubex.one/config/)

比如：

    yaml 大小写敏感，使用缩进表示层级关系，缩进不允许使用 tab, 只允许空格，缩进的空格数不重要，只要相同层级的元素左对齐即可

    在 yaml 格式的文件中，以"#"作为注释开头，行尾为结尾，"#"必须在行头或者必须在前方有空格，否则不视为注释

    对象键值对使用冒号结构表示 key: value, 冒号后面要加一个空格，使用缩进表示层级关系

    & 锚点和 * 别名，可以用来引用，& 用来建立锚点，<<表示合并到当前数据,* 用来引用锚点


* 要添加规则，需要写对应的`rule-providers`、`rules`

eg:
```yaml
rule-providers:
   externalrule:    # provider的名字，这里是“externalrule”
      type:         # provider的类型：http(即远程引用)/file(本地文件)
      behavior:     # 规则的类型：domain/ipcidr/classical
      path:         # 本地文件的位置, `./ `相对的位置
      url:          # 仅当type为http时可用，用于下载远程文件；无需创建本地文件
      interval:     # 自动更新间隔，仅当type为http时可用
      format:       # yaml/test,text文件匹配性能更好；引用文件为yaml时可以不写format
```

clash的规则都有三个部分(MATCH除外),分别为: 类型,匹配内容,策略
```yaml
rules:
  - RULE-SET,externalrule,DIRECT # 表示上面创建的`externalrule`走`直连`
  - RULE-SET,externalrule,proxy  # 表示上面创建的`externalrule`走名为`proxy`的策略组
```



以blackmatrix7的[Google规则](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule/Clash/Google)举例

该规则的 behavior 为 `classical`

链接为： https://cdn.jsdelivr.net/gh/blackmatrix7/ios_rule_script@master/rule/Clash/Google/Google.yaml

因此可以这样写：
```yaml
rule-providers:
  Google:                       # provider的名字，这里是“Google”
    type: http  
    behavior: classical 
    path: ./ruleset/Google.yaml 
    url: https://cdn.jsdelivr.net/gh/blackmatrix7/ios_rule_script@master/rule/Clash/Google/Google.yaml          
    interval: 86400
    #format:                    # 引用文件为yaml时可以不写format

rule:
  - RULE-SET,Google,谷歌服务     # 表示上面创建的`Google`走`谷歌服务`策略组
```

我的配置中写了锚点
比如 ` c: &c {type: http, behavior: classical, interval: 86400} `

等于

```yaml
type: http  
behavior: classical 
interval: 86400
```

因此上面的`rule-providers`也可以这样写：
```yaml
rule-providers:
 Google: 
   <<: *c
   path: ./ruleset/Google.yaml
   url: https://cdn.jsdelivr.net/gh/blackmatrix7/ios_rule_script@master/rule/Clash/Google/Google.yaml}
```
或者写成单行的形式(冒号后加一个空格)：
```yaml
rule-providers:
 Google: {<<: *c, path: ./ruleset/Google.yaml, url: https://cdn.jsdelivr.net/gh/blackmatrix7/ios_rule_script@master/rule/Clash/Google/Google.yaml}
```

参考文档：

https://lancellc.gitbook.io/clash/clash-config-file/rule-provider

https://wiki.metacubex.one/config/

https://github.com/Fndroid/clash_for_windows_pkg/issues/2193
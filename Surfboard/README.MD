# Surfboard

### Surfboard 下载地址

<a href="https://play.google.com/store/apps/details?id=com.getsurfboard"><img width="200px" alt="Get it on Google Play" src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png"/></a> or [Github/releases](https://github.com/getsurfboard/surfboard/releases)



在线订阅转换
---
> 在线订阅转换可能出现订阅泄露
#### 1. 打开[ACL4SSR](https://acl4ssr-sub.github.io/) 
#### 2. 填入 **机场订阅** 和 **远程配置**

**_自用 自动测速 配置_**
```
https://raw.githubusercontent.com/Repcz/Open-Proflies/main/Surfboard/OwnUse.ini
```

**_自用 多流媒体分组 自动测速 配置_**
```
https://raw.githubusercontent.com/Repcz/Open-Proflies/main/Surfboard/More%20streaming.ini
```
#### 3.修改客户端为 **Surfboard**
#### 4. 选择后端地址并生成订阅
![Image text](https://github.com/Repcz/Open-Proflies/blob/main/Surfboard/Photo/IMG_2204.PNG)

#### 5.复制粘贴配置到 **Surfboard**
点击 **配置** -右下角➕ - **URL** - 粘贴订阅转换后的链接
> 理论上点开 右下角➕ ，就会自动识别

手动添加配置
---
#### 复制粘贴配置到 **Surfboard**
点击 **配置** -右下角➕ - **从零开始** -复制以下配置并粘贴
```yaml
# 基于[@Coldvvater](https://github.com/Coldvvater/Mononoke/blob/master/Surfboard/Config/Surfboard-Evolve.conf)修改
# Author:https://github.com/Repcz
# TG:https://t.me/QVQ_Channel
#
# 以 ';' 或 '#' 或 '//' 开头的配置文件行为注释行
#
# 最后更新时间: 2023/9/5
#
# ================

[General]
# > 日志等级
loglevel = info

# > DNS服务器
dns-server = 223.5.5.5,119.29.29.29

# > 加密的DNS服务器
doh-server = https://dns.alidns.com/dns-query,https://doh.pub/dns-query

# > 跳过代理
skip-proxy = localhost, *.local, captive.apple.com, e.crashlytics.com, sequoia.apple.com, seed-sequoia.siri.apple.com, www.baidu.com, passenger.t3go.cn, yunbusiness.ccb.com, wxh.wo.cn, gate.lagou.com, www.abchina.com.cn, login-service.mobile-bank.psbc.com, mobile-bank.psbc.com, app.yinxiang.com, injections.adguard.org, local.adguard.org, cable.auth.com, *.id.ui.direct, 10.0.0.0/8, 100.64.0.0/10, 127.0.0.1/32, 169.254.0.0/16, 172.16.0.0/12, 192.168.0.0/16, 192.168.122.1/32, 193.168.0.1/32, 224.0.0.0/4, 240.0.0.0/4, 255.255.255.255/32, ::1/128, fc00::/7, fd00::/8, fe80::/10, ff00::/8, 2001::/32, 2001:db8::/32, 2002::/16, ::ffff:0:0:0:0/1, ::ffff:128:0:0:0/1

# > 代理延迟测试
proxy-test-url = http://www.gstatic.com/generate_204

# > 网络延迟测试
internet-test-url = http://www.aliyun.com

# > 连通性测试超时
test-timeout = 5

# > 返回真实IP
always-real-ip = *.lan, cable.auth.com, *.msftconnecttest.com, *.msftncsi.com, network-test.debian.org, detectportal.firefox.com, resolver1.opendns.com, *.srv.nintendo.net, *.stun.playstation.net, xbox.*.microsoft.com, *.xboxlive.com, stun.*, global.turn.twilio.com, global.stun.twilio.com, localhost.*.qq.com, *.logon.battlenet.com.cn, *.logon.battle.net, *.blzstatic.cn, music.163.com, *.music.163.com, *.126.net, musicapi.taihe.com, music.taihe.com, songsearch.kugou.com, trackercdn.kugou.com, *.kuwo.cn, api-jooxtt.sanook.com, api.joox.com, joox.com, y.qq.com, *.y.qq.com, streamoc.music.tc.qq.com, mobileoc.music.tc.qq.com, isure.stream.qqmusic.qq.com, dl.stream.qqmusic.qq.com, aqqmusic.tc.qq.com, amobile.music.tc.qq.com, *.xiami.com, *.music.migu.cn, music.migu.cn, proxy.golang.org, *.mcdn.bilivideo.cn, *.cmpassport.com, id6.me, open.e.189.cn, mdn.open.wo.cn, opencloud.wostore.cn, auth.wosms.cn, *.jegotrip.com.cn, *.icitymobile.mobi, *.pingan.com.cn, *.cmbchina.com, pool.ntp.org, *.pool.ntp.org, ntp.*.com, time.*.com, ntp?.*.com, time?.*.com, time.*.gov, time.*.edu.cn, *.ntp.org.cn, PDC._msDCS.*.*, DC._msDCS.*.*, GC._msDCS.*.*

# > HTTP监听地址
http-listen = 0.0.0.0:1234

# > socks5监听地址
socks5-listen = 127.0.0.1:1235

# > UDP IP 防泄漏
# 如果没有代理服务器支持 UDP 转发，可修改为「direct」或注释下条，但需注意同一目标主机名 TCP 请求与 UDP 请求的源地址不同所造成的隐私及安全风险
udp-policy-not-supported-behaviour = REJECT

[Host]
# > IPv6
ip6-localhost = ::1 # IPv6 Localhost
ip6-loopback = ::1 # IPv6 Loopback
ip6-localnet = fe00::0 # IPv6 Link-Local
ip6-mcastprefix = ff00::0 # IPv6 Multicast
ip6-allnodes = ff02::1 # IPv6 All Nodes
ip6-allrouters = ff02::2 # IPv6 All Routers
ip6-allhosts = ff02::3 # IPv6 All Hosts
# > Firebase Cloud Messaging
talk.google.com = 108.177.125.188 
mtalk.google.com = 108.177.125.188 
alt1-mtalk.google.com = 3.3.3.3 
alt2-mtalk.google.com = 3.3.3.3 
alt3-mtalk.google.com = 74.125.200.188 
alt4-mtalk.google.com = 74.125.200.188 
alt5-mtalk.google.com = 3.3.3.3 
alt6-mtalk.google.com = 3.3.3.3 
alt7-mtalk.google.com = 74.125.200.188 
alt8-mtalk.google.com = 3.3.3.3 

[Proxy]
# > 配置模板见：https://manual.getsurfboard.com/config-template

[Proxy Group]

# > 外部节点(在此替换"订阅链接")
🚀 手动切换 = select,  🇭🇰 香港节点, 🇺🇸 美国节点, 🇸🇬 狮城节点, 🇯🇵 日本节点, 🇨🇳 台湾节点, DIRECT, policy-path=http://your-service-provider, interval=300, update-interval=86400

# > 代理策略分流

🌏 国外网站 = select, 🇭🇰 香港节点, 🇺🇸 美国节点, 🇸🇬 狮城节点, 🇯🇵 日本节点, 🇨🇳 台湾节点, 🚀 手动切换, DIRECT, no-alert=0, hidden=0

📹 国际媒体 = select, 🇭🇰 香港节点, 🇺🇸 美国节点, 🇸🇬 狮城节点, 🇯🇵 日本节点, 🇨🇳 台湾节点, 🚀 手动切换,  DIRECT, no-alert=0, hidden=0

🧩 微软服务 = select, 🇭🇰 香港节点, 🇺🇸 美国节点, 🇸🇬 狮城节点, 🇯🇵 日本节点, 🇨🇳 台湾节点, 🚀 手动切换,  DIRECT, no-alert=0, hidden=0

🌌 谷歌服务 = select, 🇭🇰 香港节点, 🇺🇸 美国节点, 🇸🇬 狮城节点, 🇯🇵 日本节点, 🇨🇳 台湾节点, 🚀 手动切换,  DIRECT, no-alert=0, hidden=0

📟 电报消息 = select, 🇭🇰 香港节点, 🇺🇸 美国节点, 🇸🇬 狮城节点, 🇯🇵 日本节点, 🇨🇳 台湾节点, 🚀 手动切换,  DIRECT, no-alert=0, hidden=0

🐦 推特消息 = select, 🇭🇰 香港节点, 🇺🇸 美国节点, 🇸🇬 狮城节点, 🇯🇵 日本节点, 🇨🇳 台湾节点, 🚀 手动切换,  DIRECT, no-alert=0, hidden=0

🤖 OpenAI = select, 🇭🇰 香港节点, 🇺🇸 美国节点, 🇸🇬 狮城节点, 🇯🇵 日本节点, 🇨🇳 台湾节点, 🚀 手动切换,  DIRECT, no-alert=0, hidden=0

📺 哔哩哔哩 = select, DIRECT, 🇭🇰 香港节点, 🇨🇳 台湾节点, no-alert=0, hidden=0

🛑 广告拦截 = select, REJECT, DIRECT, no-alert=0, hidden=0, include-all-proxies=0

🐟 漏网之鱼 = select, 🇭🇰 香港节点, 🇺🇸 美国节点, 🇸🇬 狮城节点, 🇯🇵 日本节点, 🇨🇳 台湾节点, 🚀 手动切换,  no-alert=0, hidden=0

# > 节点地区分流

🇭🇰 香港节点 = url-test, policy-regex-filter=^(?=.*((?i)🇭🇰|香港|(\b(HK|Hong)\b)))(?!.*((?i)回国|校园|游戏|(\b(GAME)\b))).*$, interval=600,update-interval=86400, no-alert=0, hidden=0, include-all-proxies=1

🇺🇸 美国节点 = url-test, policy-regex-filter=^(?=.*((?i)🇺🇸|美国|波特兰|达拉斯|俄勒冈|凤凰城|费利蒙|硅谷|拉斯维加斯|洛杉矶|圣何塞|圣克拉拉|西雅图|芝加哥|(\b(US|United States)\b)))(?!.*((?i)回国|校园|游戏|(\b(GAME)\b))).*$, interval=600,update-interval=86400, no-alert=0, hidden=0, include-all-proxies=1

🇸🇬 狮城节点 = url-test, policy-regex-filter=^(?=.*((?i)🇸🇬|新加坡|狮|(\b(SG|Singapore)\b)))(?!.*((?i)回国|校园|游戏|(\b(GAME)\b))).*$, interval=600,update-interval=86400, no-alert=0, hidden=0, include-all-proxies=1

🇯🇵 日本节点 = url-test, policy-regex-filter=^(?=.*((?i)🇯🇵|日本|川日|东京|大阪|泉日|埼玉|(\b(JP|Japan)\b)))(?!.*((?i)回国|校园|游戏|(\b(GAME)\b))).*$, interval=600,update-interval=86400, no-alert=0, hidden=0, include-all-proxies=1

🇨🇳 台湾节点 = url-test, policy-regex-filter=^(?=.*((?i)🇹🇼|台湾|(\b(TW|Tai|Taiwan)\b)))(?!.*((?i)回国|校园|游戏|(\b(GAME)\b))).*$, interval=600,update-interval=86400, no-alert=0, hidden=0, include-all-proxies=1

[Rule]
# > 远程规则集
# > 规则修正
RULE-SET,https://raw.githubusercontent.com/DivineEngine/Profiles/master/Surge/Ruleset/Unbreak.list, DIRECT,update-interval=86400

# > 广告拦截
RULE-SET,https://anti-ad.net/surge.txt,🛑 广告拦截,update-interval=86400

# > HTTPDNS.Block
RULE-SET,https://github.com/VirgilClyne/GetSomeFries/raw/main/ruleset/HTTPDNS.Block.list,🛑 广告拦截,update-interval=86400

# > 哔哩哔哩
RULE-SET,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/Ruleset/Bilibili.list,📺 哔哩哔哩,update-interval=86400

# > OpenAI
RULE-SET,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/Ruleset/OpenAi.list,🤖 OpenAI,update-interval=86400

# > 电报信息
RULE-SET,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/Ruleset/Telegram.list,📟 电报消息,update-interval=86400

# > 推特信息
RULE-SET,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/Ruleset/Twitter.list,🐦 推特消息,update-interval=86400


# > 微软分流
RULE-SET,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/Ruleset/Microsoft.list,🧩 微软服务,update-interval=86400
RULE-SET,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/Ruleset/OneDrive.list,🧩 微软服务,update-interval=86400

# > 谷歌分流
RULE-SET,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/Ruleset/YouTube.list,🌌 谷歌服务,update-interval=86400
RULE-SET,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/Ruleset/Google.list,🌌 谷歌服务,update-interval=86400

# > 国际流媒体
RULE-SET,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/ProxyMedia.list,📹 国际媒体,update-interval=86400

# > 国外网站分流
RULE-SET,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/ProxyGFWlist.list,🌏 国外网站,update-interval=86400

# > 国内网站分流
RULE-SET,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/Ruleset/Wechat.list,DIRECT,update-interval=86400

RULE-SET,https://raw.githubusercontent.com/ACL4SSR/ACL4SSR/master/Clash/ChinaDomain.list,DIRECT,update-interval=86400

RULE-SET,https://cdn.jsdelivr.net/gh/soffchen/GeoIP2-CN@release/surge-ruleset.list,DIRECT,update-interval=86400

# > 本地规则分流
IP-CIDR,192.168.0.0/16, DIRECT
IP-CIDR,10.0.0.0/8, DIRECT
IP-CIDR,172.16.0.0/12, DIRECT
IP-CIDR,127.0.0.0/8, DIRECT
IP-CIDR,100.64.0.0/10, DIRECT
IP-CIDR,224.0.0.0/4, DIRECT
IP-CIDR6,fe80::/10, DIRECT
IP-CIDR,119.28.28.28/32, DIRECT
IP-CIDR,182.254.116.0/24, DIRECT
GEOIP,CN, DIRECT
FINAL,🐟 漏网之鱼


 
```


#### 修改[Proxy Group]部分并保存
将[Proxy Group]中的 `http://your-service-provider` 替换为 机场订阅地址

eg：
```yaml
...

[Proxy Group]

# > 外部节点(在此替换"订阅链接")
🚀 手动切换 = select,  🇭🇰 香港节点, 🇺🇸 美国节点, 🇸🇬 狮城节点, 🇯🇵 日本节点, 🇨🇳 台湾节点, DIRECT, policy-path=http://your-service-provider, interval=300, update-interval=86400

...


```
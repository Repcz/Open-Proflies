# Egern

### 下载配置文件
点击下载[配置文件](https://raw.githubusercontent.com/Repcz/Open-Proflies/main/Egern/Egern.yaml)

### 填入机场订阅
自行替换配置文件中`http://your-service-provider`为你的机场订阅
```yaml
  #地区分组
  - external:
      name: 🇭🇰 香港节点
      type: auto_test
      url: "http://your-service-provider"
      filter: ^(?=.*((?i)🇭🇰|香港|(\b(HK|Hong)\b)))(?!.*((?i)回国|校园|游戏|(\b(GAME)\b))).*$
      interval: 900
      timeout: 2
      tolerance: 150
      update_interval: 86400
  - external:
      name: 🇯🇵 日本节点
      type: auto_test
      url: "http://your-service-provider"
      filter: ^(?=.*((?i)🇯🇵|日本|川日|东京|大阪|泉日|埼玉|(\b(JP|Japan)\b)))(?!.*((?i)回国|校园|游戏|(\b(GAME)\b))).*$
      interval: 900
      timeout: 2
      tolerance: 150
      update_interval: 86400
  - external:
      name: 🇺🇲 美国节点
      type: auto_test
      url: "http://your-service-provider"
      filter: ^(?=.*((?i)🇺🇸|美国|波特兰|达拉斯|俄勒冈|凤凰城|费利蒙|硅谷|拉斯维加斯|洛杉矶|圣何塞|圣克拉拉|西雅图|芝加哥|(\b(US|United States)\b)))(?!.*((?i)回国|校园|游戏|(\b(GAME)\b))).*$
      interval: 900
      timeout: 2
      tolerance: 150
      update_interval: 86400
  - external:
      name: 🇨🇳 台湾节点
      type: auto_test
      url: "http://your-service-provider"
      filter: ^(?=.*((?i)🇹🇼|台湾|(\b(TW|Tai|Taiwan)\b)))(?!.*((?i)回国|校园|游戏|(\b(GAME)\b))).*$
      interval: 900
      timeout: 2
      tolerance: 150
      update_interval: 86400
  - external:
      name: 🇸🇬 狮城节点
      type: auto_test
      url: "http://your-service-provider"
      filter: ^(?=.*((?i)🇸🇬|新加坡|狮|(\b(SG|Singapore)\b)))(?!.*((?i)回国|校园|游戏|(\b(GAME)\b))).*$
      interval: 900
      timeout: 2
      tolerance: 150
      update_interval: 86400
  - external:
      name: 🚀 手动选择
      type: select
      url: "http://your-service-provider"
      filter: ^(?=.*(.*))(?!.*((?i)回国|校园|教育|官网|客服|网站|网址|获取|订阅|流量|到期|机场|下次|版本|官址|备用|到期|过期|已用|联系|邮箱|工单|群|(\b(GAME|USE|USED|TOTAL|EXPIRE|EMAIL)\b|(\d{4}-\d{2}-\d{2}|\dG)))).*$
  - external:
      name: ♻️ 自动切换
      type: auto_test
      url: "http://your-service-provider"
      filter: ^(?=.*(.*))(?!.*((?i)回国|校园|教育|官网|客服|网站|网址|获取|订阅|流量|到期|机场|下次|版本|官址|备用|到期|过期|已用|联系|邮箱|工单|群|(\b(GAME|USE|USED|TOTAL|EXPIRE|EMAIL)\b|(\d{4}-\d{2}-\d{2}|\dG)))).*$

```

### 导入**Egern**
在 **Egern** - **工具** - 右上角`···` 中，点击导入配置


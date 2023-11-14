### 规则源自 [@ACL4SSR](https://github.com/ACL4SSR/ACL4SSR/tree/master) [@NobyDa](https://github.com/NobyDa) [@VirgilClyne](https://github.com/VirgilClyne) [@blackmatrix7](https://github.com/blackmatrix7/ios_rule_script/tree/master/rule) [@dler-io](https://github.com/dler-io/Rules) [@missuo](https://github.com/missuo/ASN-China) [@RuCu6](https://github.com/RuCu6/QuanX) [@imbopro](https://github.com/limbopro/Adblock4limbo)

### 代码都是ChatGPT写的，有遗漏或错误请自行修改

---

### Clash请使用 `format: text`

eg：

* Bilibili.list
```
BiliBili: {type: http, behavior: classical,  format: text, interval: 86400 path: ./ruleset/BiliBili.txt,  url: https://ghproxy.com/https://raw.githubusercontent.com/Repcz/Rules/main/Clash/Bilibli.list}
```

* ChinaIP.list
```
ChinaIP: {type: http, behavior: ipcidr,  format: text, interval: 86400 path: ./ruleset/ChinaIP.txt,  url: https://ghproxy.com/https://raw.githubusercontent.com/Repcz/Rules/main/Clash/ChinaIP.list}
```

---

### QX默认策略均为`DIRECT`，请务必修改策略偏好

---

### Surge规则目录下带有`_DomainSet`后缀的文件请使用`DOMAIN-SET`，其他未标注或带有`_RuleSet`后缀的请使用`RULE-SET`
### `_DomainSet`后缀和`_RuleSet`后缀的文件须同时使用



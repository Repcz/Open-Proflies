> [Sub-Stor项目地址](https://github.com/sub-store-org/Sub-Store)

> 作者提供的[文档](https://www.notion.so/Sub-Store-6259586994d34c11a4ced5c406264b46)（应该是？）

## 使用前准备
> 此步骤非必需

1. 注册一个Github账号（具体Google）
2. 在GitHub账户中创建一个令牌,具体方法如下：
   1. 点击生成新令牌(经典) ：[Generate new token](https://github.com/settings/tokens/new)
   2. 输入一个令牌名称，比如Sub-Store，并修改使用时间为 `No expiration`
![4](https://github.com/Repcz/Open-Proflies/blob/main/Sub-Store/Photo/github4.png)
   3. 下拉勾选 `gist` ，并点击最下方 `Generate token`
![5](https://github.com/Repcz/Open-Proflies/blob/main/Sub-Store/Photo/github5.png)
![6](https://github.com/Repcz/Open-Proflies/blob/main/Sub-Store/Photo/gtihub6.png)
   4. 复制token
![7](https://github.com/Repcz/Open-Proflies/blob/main/Sub-Store/Photo/github7.png)

## 安装Sub-Store
> 需自行配置证书并信任，开启MITM


### 1. Loon
安装使用[插件](https://raw.githubusercontent.com/Peng-YM/Sub-Store/master/config/Loon.plugin)即可。

> [我的配置](https://github.com/Repcz/Open-Proflies/blob/main/Loon/Loon.conf)中已经引用，在 **插件** 中找到 **Sub-Store** 并左滑启用即可
### 2. Surge
安装使用[模块](https://raw.githubusercontent.com/Peng-YM/Sub-Store/master/config/Surge.sgmodule)即可。
### 3. QX
订阅[重写](https://raw.githubusercontent.com/Peng-YM/Sub-Store/master/config/QX.snippet)即可。

> [我的配置](https://github.com/Repcz/Open-Proflies/blob/main/QuantumultX/QuantumultX.conf)中已经引用，在 **重写** 中找到 **Sub-Store@Peng-YM** 并勾选启用即可。

### 4. Stash
启动Stash后，在 **设置** - **配置列表** 中下拉点击 **Sub-Store** 即可。

### 5. Shadowrocket
安装使用[模块](https://raw.githubusercontent.com/sub-store-org/Sub-Store/master/config/Surge.sgmodule)即可。

## 使用 Sub-Store
> 使用 Safari 访问 https://sub.store 如网页正常打开并且未弹出任何错误提示，说明 Sub-Store 已经配置成功。

> 可以把 Sub-Store 添加到主屏幕，即可获得类似于 APP 的使用体验。

#### 填入Token
> 非必需

Safari 访问 https://sub.store， 在 **我的** - **Github配置** 中，分别填入 Github用户名 和 刚才创建的 **token**，保存并上传![1](https://github.com/Repcz/Open-Proflies/blob/main/Sub-Store/Photo/ss1.PNG)

#### 创建单条订阅
1. 在左下角 **订阅** 中，点击有下角 ➕，点击 **单条订阅** 。
2. 填入对应的 **名称**(建议用英文)、**链接**(即机场订阅链接)，来源选择 **远程订阅** ，显示名称可以填写机场的名称，也可不填
3. 下拉找到 **常用配置** ，默认即可。
4. 最下方 **保存** 。
![2](https://github.com/Repcz/Open-Proflies/blob/main/Sub-Store/Photo/ss2.PNG)

#### 节点操作

> 随着版本更新，界面可能存在差异，以实际为准

在下方 **节点操作** 中，可以对节点进行重命名、正则操作、排序、脚本处理等操作。

下面以某机场进行简单的操作举例：
让  `🇭🇰香港01` 变成  `🇭🇰Magic 香港01` 
并去除一些不必要的节点，修改前后效果如下图
![3](https://github.com/Repcz/Open-Proflies/blob/main/Sub-Store/Photo/ss3.PNG)

1. 在 添加单条订阅时直接操作 或者 保存后直接 左滑订阅 - 点击 **钢笔✒** 进行编辑
2. 点击下方节点操作下面的 **添加一个操作** - **国旗操作** - **确认**，点击完成后会出现一个国旗操作的模块，工作模式选择 **移除** 。
3. **添加一个操作** - **正则过滤** - **确认** ，过滤掉例如：`官网`、`版本`、`网址` 等节点，填写一个关键词，点一下右边的 **箭头**。 
4. **添加一个操作** - **正则重命名** - **确认** ，正则表达式填写` ^(.+)$ `，替换为填写` 机场名称 $1 `（我这里填写的为Magic ），并点击右边的 **箭头** 。
5.  **添加一个操作** - **国旗操作** - **确认** ， 工作模式选择 **添加**。 
6. 最下方 **保存** 。
![4](https://github.com/Repcz/Open-Proflies/blob/main/Sub-Store/Photo/ss4.PNG)

#### 创建组合订阅
1. 在左下角 **订阅** 中，点击有下角 ➕，点击 **组合订阅** 。
2. 填入对应的 **名称**(建议用英文)，并按需勾选下方已经存在的**单条订阅**。
3. 最下方 **保存** 。

#### 导入代理工具
点击 **单条订阅** 或 **组合订阅** 右上角的 **复制** 按钮，将链接填入对应的代理工具即可。

⚠注意：除非其他代理工具也安装Sub Store并开启MITM等，否则该方法只能填入对应的代理工具；比如在 QuantumultX 中启用的 Sub-Store ，创建的订阅，只能在QX中使用。

#### 同步订阅至Github Gist
> 非必需

1. 在 **同步** 页面中，点击有下角 加号➕ 。
2. 填写对应的 **名称** ，**来源**，选择需要同步的 **单条订阅** 或 **组合订阅** 。
3. **目标平台** 选择对应的平台。
4. 点击 **确认** 。
5. 勾选 订阅 右边的 **定时** ，并点击上方的 **同步按钮☁** 。
6. 点击 订阅 右上角的 **复制** 按钮，将链接填入对应的代理工具即可。

⚠注意：该方法生成的链接可以填入其他的代理工具中使用；比如在 QuantumultX 中启用的 Sub-Store ，创建的对应 **Clash平台** 的订阅，同步到Github后，可以将生成的链接直接填入 **Clash的配置文件** 中使用，无需再次订阅转换。
![5](https://github.com/Repcz/Open-Proflies/blob/main/Sub-Store/Photo/ss5.PNG)


## 一些脚本操作
[@Keywos](https://github.com/Keywos)的脚本
具体用法请看脚本内注释
* 本地重命名：
```
https://raw.githubusercontent.com/Keywos/rule/main/rename.js
```

* Ping清除无效节点：
```
https://raw.githubusercontent.com/Keywos/rule/main/pname.js
```

* Api去重、查询ISP等：
```
https://raw.githubusercontent.com/Keywos/rule/main/cname.js
```


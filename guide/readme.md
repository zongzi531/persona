# 使用指南

## 前置条件

要在我的网站上拥有单独的人物页，需要达到并维持住以下几种条件之一——

### 建立实际关系

无论是现实中或是网络上跟我关系还不错，也就是与我有所交集并且有一定程度的交流，算是「熟人」。

### 经济上的支援

通过定期赞助或买坑位等形式对我进行经济上的支援。

### 网站链接交换

就是所谓的「友情链接」，需要满足几点要求：

1. 内容绝大多数为原创，是自己思考的结晶；
2. 范围可以是前端开发、日本文化（如日语、动漫）等与我的职业或爱好相关；
3. 经常对自己的站点进行维护。

如果自觉满足上述要求，那么就按照下面列出的信息把我的网站链接添加到你的网站上：

- 名称：欧雷流
- 网址：`https://ourai.ws/`
- 描述：我叫欧雷，是一个出生于上世纪 80 年代的理想主义叛逆青年。喜欢日本，热爱咖啡，善于总结。这里有我对技术和语言的研究，也有对世界和生活的思考。
- 站长：欧雷
- 标志：[点击查看](https://ourai.ws/assets/avatars/ourai-100px-3bcaa1cb0c7fa0547d15622572d74a8bbc98a5f62e4920ecddb72ca95e505d17.jpg)

## 编辑信息

若要自行添加信息，需先 fork 本仓库，再在 [`data/persona`](../data/persona) 文件夹下创建自己的「persona」，最后发起 pull request 合并进来。

「persona」所在文件夹的名字就是 [`ourai.ws`](https://ourai.ws/) 上生成的人物信息页 URL `https://ourai.ws/people/{slug}/` 中的 `slug`。

文件夹下所应有的文件包括：

- 命名为 `avatar` 的图片文件，作为头像使用，格式不限，正方形，分辨率不超过 `500 * 500`；
- 命名为 `banner` 的图片文件，作为人物页头图和人物卡片背景图使用，格式不限，横向长方形，建议宽度 `1000px` 以上；
- 描述人物信息的 `metadata.yml`，具体内容见下方；
- 对人物进行详细介绍的 `readme.md`，可选。

人物元数据 `metadata.yml` 中所需字段为：

```yml
name: 欧雷 # 人物在网上的名称
brief: 多面玩家 # 用来与人物名称以「{name}：{brief}」的形式拼成个性化的网页标题，可选
description: 思考并探索改变生活、玩转人生的方法。 # 一句话简介，显示在人物页头部和人物卡片上的简短介绍
professions: # 人物职业，为了显示的完整性，建议不超过三个且总字数不超过十个字
  - title: 世界公民
    always: false # 显示尺寸较小时隐藏
  - title: 生活黑客
  - title: 反混沌工程师
websites: # 个人网站，第一个将作为主站对待，可选
  - title: 欧雷流 # 网站标题
    url: https://ourai.ws/ # 网址
    description: 不走寻常路 # 网站简介，可选
contacts: # 联系方式，可选
  email: ourairyu@gmail.com
  github: ourai
location: 浙江杭州 # 所在地
banner: # 人物页头图/人物卡片背景图的额外信息，可选
  description: Anti-chaos # 图片是什么
```

其中，联系方式可以为：

| 联系方式 | 键 | 值 |
| --- | --- | --- |
| 电子邮箱 | `email` | 电子邮箱地址 |
| 手机或座机电话 | `phone` | 手机或座机号码，座机要带区号 |
| 微信 | `wechat` | 能搜到微信联系人的方式 |
| Telegram | `telegram` | 能搜到 Telegram 联系人的方式 |
| 任何 SNS 网站 | - | 在 SNS 网站上的个人资料页唯一标识 |

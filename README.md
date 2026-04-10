# AdGuard Home 电商广告白名单

适用于 AdGuard Home 的电商平台广告域名白名单，放行主流电商平台的广告、追踪及联盟域名，避免影响电商运营工作。

---

## 订阅地址

推荐使用 jsDelivr CDN（国内访问更稳定）：

```
https://cdn.jsdelivr.net/gh/eshop366/adg-ecommerce-whitelist@main/ecommerce_whitelist.txt
```

GitHub Raw 原始地址：

```
https://raw.githubusercontent.com/eshop366/adg-ecommerce-whitelist/main/ecommerce_whitelist.txt
```

---

## 使用方法

1. 打开 AdGuard Home 管理后台
2. 进入 **过滤器** → **DNS 白名单** → **添加白名单**
3. 填写名称和上方订阅地址
4. 点击**保存**，等待规则加载完成
5. 后续更新：**过滤器** → **DNS 白名单** → **检查更新**

---

## 覆盖平台

| 平台 | 说明 |
|---|---|
| 阿里系（国内） | 淘宝、天猫、1688、妈妈联盟、阿里妈妈广告平台（alimama、tanx、mmstat） |
| 阿里系（国际） | AliExpress 速卖通、Lazada 各国站、Daraz、Miravia |
| 京东系 | 京东国内外、京东联盟广告、京东云 |
| 拼多多系 | 拼多多国内、Temu 各域名及 CDN |
| 抖音电商 | 抖音小店、巨量引擎、穿山甲广告平台 |
| TikTok 电商 | TikTok Shop、TikTok 广告投放、分析追踪域名 |
| Amazon 系 | 亚马逊全球各站、亚马逊广告（amazon-adsystem）、联盟计划 |
| SHEIN | SHEIN 全球各站、ltwebstatic CDN、追踪域名 |
| Shopee | Shopee 全球各国站、冬海集团（Sea Group）相关域名 |

---

## 适用场景

- 跨境电商卖家、运营人员需要正常查看平台广告
- 已部署 AdGuard Home 做 DNS 过滤，但不希望广告拦截影响工作
- 搭配 PassWall + ChinaDNS-NG 使用，AdGuard Home 仅作缓存加速层

---

## 部署环境参考

```
局域网设备
    ↓
DNSmasq（OpenWrt 默认，监听 53）
    ↓
AdGuard Home（缓存 + 白名单过滤）
    ↓
ChinaDNS-NG（PassWall，DNS 智能分流）
    ↙           ↘
国内 DNS        远程 DNS（经代理）
114/223 等      1.1.1.1 Cloudflare
```

---

## 更新日志

| 日期 | 内容 |
|---|---|
| 2025-04 | 初始版本，覆盖阿里、京东、拼多多、抖音、TikTok、Amazon、SHEIN、Shopee |

---

## 免责声明

本规则仅用于放行合法电商平台域名，不用于任何规避法律法规的用途。规则内容定期维护，如发现遗漏或失效域名欢迎提 Issue。

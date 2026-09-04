# Amazon 选品研究

## 项目状态

🚧 **研究阶段** — 不开发，只调研。

> 目标：以买家/卖家视角，研究"亚马逊选品"的完整思路与方法。

## 已收集的资源

### 开源项目

| 项目 | URL | 简评 |
|------|-----|------|
| Umair706/amazon-omniscient | https://github.com/Umair706/amazon-omniscient | **完整度最高**：BSR/竞品/利润/AI/财务预测全套 |
| tducret/amazon-scraper-python | https://github.com/tducret/amazon-scraper-python | 简单爬虫（159⭐） |
| MattJGlick/fba-sourcing-analyzer | https://github.com/MattJGlick/fba-sourcing-analyzer | BSR 评估 |
| EricSchwartz7/amazon-product-finder | https://github.com/EricSchwartz7/amazon-product-finder | PA-API + PHP |
| smart-seller/awesome-amazon-seller-tools | https://github.com/smart-seller/awesome-amazon-seller-tools | 工具集锦 |
| ScaleLeap/awesome-amazon-seller | https://github.com/ScaleLeap/awesome-amazon-seller | 工具集锦 |

### 待调研

- [ ] Keepa（价格追踪）功能与原理
- [ ] Helium 10 主要功能拆解
- [ ] Jungle Scout 核心算法
- [ ] Amazon SP-API 文档
- [ ] 评论分析工具（ReviewMeta 等）
- [ ] 卖家视角 vs 买家视角工具区别
- [ ] BSR → 销售量 转换算法
- [ ] 评论质量评分方法
- [ ] 选品常见指标（需求、竞争、利润）

## 卖家视角 vs 买家视角

### 卖家视角（Omniscient 重点）
- **BSR 跟踪**：热销排名 → 估算销量
- **竞品分析**：Listing 质量 + 弱点
- **利润计算**：FOB + 关税 + FBA 费 + 平台费
- **选品评分**（0-100）
- **供应商发现**：1688 工厂价

### 买家视角（待研究）
- **价格历史**：是不是涨价了？
- **评论质量**：真假评论？是否刷单？
- **卖家可信度**：FBA 还是 FBM？评分？
- **替代品**：有没有更好的？
- **历史趋势**：上架多久？评论增长？

## 主流工具

| 工具 | 类型 | 价格 |
|------|------|------|
| Helium 10 | 卖家 | $37-279/月 |
| Jungle Scout | 卖家 | $49-99/月 |
| AMZScout | 卖家 | $30-65/月 |
| Keepa | 买卖家 | €19/月 |
| ReviewMeta | 买家 | 免费+付费 |
| CamelCamelCamel | 买家 | 免费 |
| SellerApp | 卖家 |  |

## 待回答的问题

- 用户的实际目标是什么？
- 卖家视角？买家视角？两者？
- 数据来源：爬虫 / SP-API / 第三方？
- 技术栈：纯 Python / Web / CLI？

## 笔记

每次搜索新资源时，在这里追加。

### 2026-09-04
- 完成第一批搜索，找到 6 个开源项目
- Umair706/amazon-omniscient 是参考标杆
- **决策**：先纯研究，不开发


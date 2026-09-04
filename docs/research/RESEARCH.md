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
- wearesellers.com 已登录，可访问完整帖子

---

## 案例分析笔记

### 案例 1：两款3.5分有线耳机的差评拆解（2025年8月，wearesellers）

**背景**：
- Amazon Basics ($9.99, 174评论) vs LUDOS ($12.99, 215评论)
- 评分都是 3.5，差评率都约 30%
- 如果只看这几个数字，会认为两款差不多

**关键发现**：
- Amazon Basics **死于耐用性**（23.3%差评：几天就坏/线断/麦克风失灵）
- LUDOS **死于佩戴**（26.8%差评：耳塞掉出来，不管什么尺寸都戴不住）
- **评分一样，死法完全相反**
- 反直觉：LUDOS 音质更好（48条好评夸音质），但因佩戴问题综合分最低

**颗粒度分析的价值**：
- 同样是"音质差"，拆开是三种完全不同的问题：
  1. 屏蔽/焊接的品控问题（静电噪音）
  2. 喇叭单元选型问题（声音发闷）
  3. 调音方向问题（低音弱）
- 同样"耳塞掉出来"，75%的人反映戴不住 → 小耳朵人群被整个品类忽视

**选品策略推导**：
- 打 Amazon Basics → 把**寿命做扎实 + 12个月保修**
- 打 LUDOS → **人体工学是命门**：外壳做轻、加耳挂、配备 XS 耳套
- **小耳朵人群**基本被整个品类忽视 → 潜在细分市场

**方法论（可复用）**：
1. 导出评论（AMZ Data / ReviewExporter / 第三方工具）
2. AI 批量打标（按痛点类型、严重程度、提及频率）
3. 聚类做对比（同类痛点合并，不同类痛点分开）
4. 颗粒度拆分（好评/差评都要拆，不是只拆差评）
5. 推导改品方向或竞争策略

**工具/成本**：
- API 成本：几块钱
- 时间：2-3小时/品类
- 核心不是工具，是**打标维度定义**（什么算痛点、噪音，颗粒度多细）

**重要心得**：
- 评论数量和评分是**表面指标**，不拆不知道死法
- 同样3.5分，死法不同 → 选品和竞品分析的依据完全不一样
- 好评也要拆（好评里的"噪音"：比如用户夸的点并不是核心卖点，说明产品没有击中真正需求）

---

## 待回答的问题

- 用户的实际目标是什么？
- 卖家视角？买家视角？两者？
- 数据来源：爬虫 / SP-API / 第三方？
- 技术栈：纯 Python / Web / CLI？


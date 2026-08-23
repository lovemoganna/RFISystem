# 🛡️ RFI System — CEX 风控与合规调查协作管理系统 (v7)

[![Live Demo](https://img.shields.io/badge/online%20service-live%20demo-brightgreen.svg?style=flat-square&logo=github)](https://lovemoganna.github.io/RFISystem/)
[![License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Web%20%7C%20Zero--Dependency-orange.svg?style=flat-square)]()
[![Theme](https://img.shields.io/badge/theme-Dark%20%2F%20Light-purple.svg?style=flat-square)]()
[![Version](https://img.shields.io/badge/version-v7.0%20Masterpiece-success.svg?style=flat-square)]()

🌐 **在线直接使用**: [https://lovemoganna.github.io/RFISystem/](https://lovemoganna.github.io/RFISystem/)

**CEX 风险控制与合规审核工作台** —— 专为中心化交易所（CEX）、Web3 资管与合规团队量身定制的 Request for Information (RFI) 场景化模板库和高效协查处理套件。快速生成多语言合规通知，提高合规性、反洗钱（AML/CFT）调查、司法协查以及日常风险控制的工作效率。

---

## ✨ 核心特性与功能套件

### 1. 📂 场景化模板库与多层分类
- **精细化风险场景覆盖**：
  - **资金来源 (Source of Funds)**：核查大额法币入金、链上资产不明来源、跨链桥异常流入等。
  - **高风险地址 (High Risk Address)**：检测暗网关联、混币器 (Tornado/Blender) 交互、受制裁实体关联 (OFAC) 等。
  - **异常行为 (Abnormal Behavior)**：核查小额分散（分层）、快进快出异常流向、登录异常操作等。
  - **身份核查 (KYC/UBO)**：核对 KYC 真实性、身份信息与流水不符、受益所有人 (UBO) 核查等。
  - **账户关联 (Account Association)**：核查多账户设备/IP 关联、第三方代充代提、资金池归集等。
- **🚨 风险级别与 SLA 建议履约时效**：
  - 精准标识：`极高风险 (CRIT - 24h内)`、`高风险 (HIGH - 48h)`、`中等风险 (MED - 2工作日)`、`低风险 (LOW - 3-5工作日)`。
- **🏷️ 标签与层级目录**：支持按标签路径（如 `风控/反洗钱`、`司法协查`）快速过滤，支持自定义场景模板的新建、克隆、锁定与分享。

### 2. ⚡ 动态字段快速填写与智能解析
- **实时占位符渲染**：自动提取模板中的 `[用户UID]`、`[交易哈希]`、`[截止日期]` 等占位符，生成结构化表单。
- **⚡ 智能文本解析器 (Smart Text Parser)**：支持直接粘贴工单描述或聊天记录，自动提取识别 UID、钱包地址、交易哈希与金额，一键回填。
- **📌 案件上下文 (Case Context)**：全局预填 UID、工单号（支持序号自动生成）、主网地址、金额与截止日期。
- **📝 案件草稿箱与自动防丢**：随时保存当前填写的案件草稿，自动实时同步填写进度。
- **📋 实时高光预览与多格式导出**：
  - 动态显示填表进度（0%~100%），支持一键复制纯文本、加粗变量 Markdown、下载 `.txt` 或一键调起邮件客户端。

### 3. 🌐 中英智能翻译助手 (Smart Translator)
- **🚀 7 大翻译通道矩阵**：包含 Google 核心引擎、Dict 扩展引擎、Mobile 引擎、MyMemory 语料库以及离线 CEX 风控专有词典，支持多源智能自动容灾。
- **🛡️ 占位符变量保护**：智能保护 `[占位符]` 变量格式，翻译后无缝保留变量名。
- **🔄 中英双语对照**：一键生成并复制中文与英文双语对照版本，适配跨国合规调证协作。

### 4. 🧹 文本清洗与行处理工具 (Text Cleaner & Processor)
- **特定符号换行拆分**：支持将逗号（`, / ，`）、分号（`; / ；`）、顿号（`、`）、竖线（`|`）、空格、Tab 等分隔的内容一键拆分为标准多行。
- **多行合并连接**：支持将多行 UID、地址或哈希合并为逗号分隔的单行（可直接用于 SQL `IN (...)` 查询）。
- **高级处理与清洗**：首尾 Trim 空格、合并连续空行、去重、升降序排列、添加前后缀（支持首行排除）。
- **🎯 链上实体智能提取**：一键从杂乱日志中提取所有 EVM / TRON / BTC / SOL 钱包地址、64位交易哈希、IPv4/IPv6 与邮箱。
- **🔐 常用编解码转换**：支持 Base64、Hex、URL 编解码及大小写/驼峰转换。

### 5. 🧮 风控计算与统计分析工具 (Risk Calculator)
- **📊 数值统计**：总和、平均值、中位数、有效笔数、标准差、最大/最小值一键计算并生成分析报告。
- **⚖️ 比例关系**：占比分析、基数百分比拆分、涨跌变化幅度、化简比例 A:B。
- **⏱ 时间流速**：计算两段交易或登录时间跨度（格式化时差/秒数/分钟），评估交易流速 (TPS / TPM)。
- **💱 汇率折算**：多行金额批量应用汇率乘数折算，输出明细与折算总额。
- **🔍 异常分布审计**：计算资金集中度基尼系数 (Gini)、赫芬达尔指数 (HHI)，并提供本福特法则 (Benford's Law) 首位数字检验，辅助识别虚构账目与刷量行为。
- **⛓ 精度折算器**：支持 Ethereum (18 - Wei)、Solana (9 - Lamport)、Bitcoin (8 - Satoshi)、Tron (6 - USDT) 精度双向换算及科学记数法十进制还原。

### 6. 📊 批量 RFI 批量生成 (Batch Studio)
- 支持单列 UID 批量替换，或直接从 Excel/CSV 粘贴多列数据（首行为占位符标题）。
- 实时生成网格对照表并按模板批量生成多份独立 RFI，支持一键全部复制。

### 7. 🎨 极致视觉体验与快捷交互
- **深浅双色主题**：完美适配深色模式（Monokai / Cyber Dark）与浅色模式（Premium Slate Light）。
- **现代毛玻璃质感**：基于 Glassmorphism 的顶部导航、细腻的高斯模糊背景与柔和微动效。
- **全键盘快捷键**：
  - `/` 或 `Ctrl+K`：聚焦模板搜索
  - `Ctrl+B`：展开 / 收起侧边栏
  - `1` / `2` / `3`：快速切换编辑模式、填写模式与批量模式
  - `?`：调出快捷键速查面板

---

## 🛠️ 技术架构

- **零依赖单文件架构**：纯原生 HTML5 / CSS3 / ES6 JavaScript 编写，无任何第三方包依赖，双击即开、秒速响应。
- **本地存储与隐私保护**：所有模板、历史记录、草稿和自定义设置均保存在浏览器本地（LocalStorage），不向未经授权的服务器上传任何敏感客户数据。
- **备份与迁移**：支持 JSON 完整数据备份导出、增量合并导入及单个模板导出分享。

---

## 🚀 快速开始

1. 克隆本项目：
   ```bash
   git clone https://github.com/lovemoganna/RFISystem.git
   ```
2. 直接双击或使用任意现代浏览器（Chrome、Edge、Safari、Firefox）打开：
   ```text
   rfi-templates (1).html
   ```
3. 在左侧选择调查场景，在右侧填入具体用户信息，即可一键复制套用！

---

## 📄 开源许可

本项目基于 [MIT License](LICENSE) 协议开源。

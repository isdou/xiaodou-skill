# 🎨 小豆 IP 文章封面图、正文配图与小红书图文生成器 (Xiao Dou Skill)

<p align="center">
  <img src="封面图/大模型幻觉_封面Banner.jpg" alt="小豆 IP 封面展示" width="100%" />
</p>

<p align="center">
  <b>根据文章内容自动提取核心概念，使用“小豆” IP 形象一键生成微信公众号/技术博客【宽幅封面图】、【2x2 四宫格正文知识配图】与【小红书 3:4 高级感科技哲学长图】。</b>
</p>

<p align="center">Generate Xiaodou IP covers, WeChat article illustrations, 2×2 infographics, and Xiaohongshu visual cards with an AI agent.</p>

<p align="center">
  <a href="#-效果大聚赏-showcase-gallery"><img src="https://img.shields.io/badge/Visual-Showcase-FFD166?style=for-the-badge&logo=storybook&logoColor=black" alt="Showcase" /></a>
  <a href="#-核心设计架构"><img src="https://img.shields.io/badge/Layout-Templates-7B2CBF?style=for-the-badge&logo=design&logoColor=white" alt="Templates" /></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-4CC9F0?style=for-the-badge" alt="License" /></a>
  <a href="https://skills.sh/isdou/xiaodou-skill"><img src="https://skills.sh/b/isdou/xiaodou-skill" alt="skills.sh 安装量" /></a>
</p>

---

## ⚡ 一键安装

```bash
npx skills add https://github.com/isdou/xiaodou-skill --skill xiaodou-cover-generator
```

安装后可直接说：“请用小豆形象把这篇文章做成一张微信公众号封面。”

## 📑 目录 (Table of Contents)

- [💡 项目简介与核心理念](#-项目简介与核心理念)
- [📐 核心设计架构](#-核心设计架构)
- [🖼️ 效果大聚赏 (Showcase Gallery)](#-效果大聚赏-showcase-gallery)
- [🚀 快速上手与使用示例](#-快速上手与使用示例)
- [📁 仓库目录结构](#-仓库目录结构)
- [📄 开源协议](#-开源协议)

---

## 💡 项目简介与核心理念

在撰写技术博客、微信公众号文章或 AI 教程时，长篇幅的纯文字内容往往难以在第一时间内抓住读者的注意力。

**“小豆” IP 视觉生成 Skill** 专为 AI Agent（如 Google Antigravity、Claude、ChatGPT）设计。它能够智能阅读你的文章段落，自动提炼核心矛盾与知识图谱，并借助软萌治愈且富有表现力的“小豆”形象，将抽象复杂的硬核概念（如 **System Prompt 工程、Context Window 限制、Token 成本优化、大模型幻觉与认知重构** 等）转化为极具视觉冲击力的图形视觉表达。

---

## 📐 核心设计架构

根据文章的不同视觉需求，支持以下三大视觉表现模式：

### 1. 宽幅封面 — 左右对比模式 (Left-Right Contrast)
> 适合表现“痛点 vs 解决”、“旧方案 vs 新方案”、“高成本 vs 低成本”等强对比文章。

* **左侧 (痛点/旧态)**：暖灰/冷色背景，焦虑困惑的黄豆豆，搭配重物、乱线团、火苗等元素。
* **中央 (分割)**：带高对比度 `VS` 徽章或闪电分割线。
* **右侧 (终局/新态)**：清新绿/阳光背景，自信快乐的黄豆豆，搭配大剪刀、打勾整理箱等元素。

### 2. 宽幅封面 — 流程拆解模式 (Workflow Breakdown)
> 适合讲解原理、System Prompt 结构、AI 工作流等深度教程文章。

* **顶栏**：醒目粗体大标题 + 深色椭圆胶囊框金句（如 `AI听不见你想的，只执行你写的`）。
* **三段流程**：`左侧输入端 (想法/疑问)` ➔ `中间控制 UI (代码框/规则点)` ➔ `右侧输出端 (灯泡小豆/自由门)`。

### 3. 正文配图 — 2×2 四宫格知识矩阵 (4-Grid Matrix)
> 适合作为文章正文中段的核心知识总结长图。

* **单宫格内部 4 层架构**：`顶栏大标题` -> `释义段` -> `黄豆豆/深灰豆豆插画` -> `底栏金句`。
* **画面细节约束**：保持 4 宫格整洁纯净，去除非必要的黑底 Hashtag 标签栏。

### 4. 小红书专属 — 3:4 燕麦极客/科技哲学卡片 (Xiaohongshu 3:4 Tech-Philosophy) ⭐ [高审美小红书模式]
> 适合发布于小红书平面的高审美图文卡片。

* **视觉风格**：深炭灰 (`#1E2022`) 与 暖燕麦色 (`#F5F2EB`) 高质感对比。
* **排版要素**：精致的衬线/黑体大标题 + 深色椭圆小胶囊英文标，深炭灰 UI 窗口配极简手绘代码语句。
* **角色互动**：深灰豆豆 AI 与黄豆豆小豆各居一侧，手握发光数据线，无老土贴纸或粗暴大字报，极具科技哲学美感。

---

## 🖼️ 效果大聚赏 (Showcase Gallery)

### 一、 宽幅文章封面图 (Cover Banners)

#### 1. 揭秘大模型与人类幻觉
![揭秘大模型与人类幻觉 封面](%E5%B0%81%E9%9D%A2%E5%9B%BE/hallucination_cover_banner.jpg)

#### 2. 揭秘 System Prompt (流程拆解架构)
![揭秘 System Prompt 封面](%E5%B0%81%E9%9D%A2%E5%9B%BE/27D7DB6E-03B0-4739-9F17-054F58190C3E.png)

#### 3. Context Window 病 vs 截断+重置 (左右对比架构)
![Context Window 封面](%E5%B0%81%E9%9D%A2%E5%9B%BE/contextwindow.png)

---

### 二、 小红书 3:4 高级感科技哲学卡片 (Xiaohongshu 3:4 Style)

#### 1. 你的认知，是代码还是真实？(3:4 燕麦极客风)
![小红书 3:4 科技哲学卡片](%E9%85%8D%E5%9B%BE/xhs_tech_philosophy_34.jpg)

---

### 三、 正文 2×2 四宫格知识配图 (Article 4-Grid Infographics)

#### 1. 大模型与人类幻觉 (4 宫格示范图)
![大模型与人类幻觉 4宫格配图](%E9%85%8D%E5%9B%BE/hallucination_4grid_infographic.jpg)

#### 2. 原生家庭是第一段 System Prompt (四宫格标准图)
![原生家庭 System Prompt 配图](%E9%85%8D%E5%9B%BE/1.jpg)

---

## 🚀 快速上手与使用示例

### 在 Google Antigravity / AGY Agent 中直接调用

```text
“请帮我根据下面这篇文章，使用小豆 Skill 自动生成一张小红书 3:4 高级感科技哲学图文卡片。”
```

---

## 📁 仓库目录结构

```text
小豆-skill/
├── SKILL.md                          # 🌟 AGY Skill 主指令定义文件
├── README.md                         # 📖 项目说明与展示文档
├── LICENSE                           # 📄 开源许可协议 (MIT)
├── references/                       # 📚 进阶规范参考库
│   ├── infographic_4grid_guide.md    # 📐 2x2 四宫格配图专项指南
│   ├── ip_prompt_guide.md            # 🎨 小豆 IP 形象解剖与 Prompt 词库
│   └── case_analysis.md              # 🔍 落地案例深度拆解
├── 封面图/                           # 🖼️ 宽幅 Banner 封面落地样例
└── 配图/                             # 🖼️ 正文 4 宫格配图与小红书 3:4 样例
    ├── xhs_tech_philosophy_34.jpg     # 🌟 最新小红书 3:4 燕麦极客卡片
    ├── hallucination_4grid_infographic.jpg
    ├── 1.jpg
    └── 2.jpg
```

---

## 📄 开源协议

本项目采用 [MIT License](LICENSE) 开源协议。欢迎基于“小豆” IP 拓展更多丰富的 AI 视觉图解与知识卡片场景！

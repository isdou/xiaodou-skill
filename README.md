# 🎨 小豆 IP 文章封面图与 4 宫格正文配图生成器 (Xiao Dou Skill)

<p align="center">
  <img src="封面图/大模型幻觉_封面Banner.jpg" alt="小豆 IP 封面展示" width="100%" />
</p>

<p align="center">
  <b>根据文章内容自动提取核心概念，使用“小豆” IP 形象一键生成微信公众号/技术博客【宽幅封面图】与【2x2 四宫格正文知识配图】。</b><br/>
  <i>内置强制垫图 (Image Reference) 机制，彻底锁定角色画风，杜绝 IP 形象漂移。</i>
</p>

<p align="center">
  <a href="#-效果大聚赏-showcase-gallery"><img src="https://img.shields.io/badge/Visual-Showcase-FFD166?style=for-the-badge&logo=storybook&logoColor=black" alt="Showcase" /></a>
  <a href="#-防漂移垫图机制-anti-drift-mechanism"><img src="https://img.shields.io/badge/IP-Anti--Drift-00F5D4?style=for-the-badge&logo=google&logoColor=black" alt="IP Lock" /></a>
  <a href="#-三大设计架构规范"><img src="https://img.shields.io/badge/Layout-Templates-7B2CBF?style=for-the-badge&logo=design&logoColor=white" alt="Templates" /></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-4CC9F0?style=for-the-badge" alt="License" /></a>
</p>

---

## 📑 目录 (Table of Contents)

- [💡 项目简介与核心理念](#-项目简介与核心理念)
- [🎨 小豆 IP 视觉解剖与画风规范](#-小豆-ip-视觉解剖与画风规范)
- [🔒 防漂移垫图机制 (Anti-Drift Mechanism)](#-防漂移垫图机制-anti-drift-mechanism)
- [📐 三大设计架构规范](#-三大设计架构规范)
- [🖼️ 效果大聚赏 (Showcase Gallery)](#-效果大聚赏-showcase-gallery)
- [🚀 快速上手与 Prompt 模版](#-快速上手与-prompt-模版)
- [📁 仓库目录结构](#-仓库目录结构)
- [📄 开源协议](#-开源协议)

---

## 💡 项目简介与核心理念

在撰写技术博客、微信公众号文章或 AI 教程时，长篇幅的纯文字内容往往难以在第一时间内抓住读者的注意力。

**“小豆” IP 视觉生成 Skill** 专为 AI Agent（如 Google Antigravity、Claude、ChatGPT）设计。它能够智能阅读你的文章段落，自动提炼核心矛盾与知识图谱，并借助软萌治愈且富有表现力的“小豆”形象，将抽象复杂的硬核概念（如 **System Prompt 工程、Context Window 限制、Token 成本优化、大模型幻觉与认知重构** 等）转化为高吸引力的图形视觉表达。

---

## 🎨 小豆 IP 视觉解剖与画风规范

为了保证生成的插画具有极高的品牌识别度与视觉统一感，Skill 内置了精准的小豆 IP 角色解剖标准：

```text
       ●   ●      <-- 纯黑实心小圆点眼睛 (间距略宽，无瞳孔/无睫毛/呆萌质感)
        \─/       <-- 极简微小弧形笑嘴 (∪)
      /     \     <-- 圆润光滑的暖黄豆豆体 (Potato/Bean Shape)
     (       )    <-- 柔和深咖啡色手绘描边 (Soft dark brown outline, 2-3px)
      \─┬─┬─/     <-- 短小圆润无手指的小手小脚
```

### 1. 角色造型分类（全员豆豆化）

* **💛 黄豆豆 (Yellow Xiao Dou) — 人类 / 用户 / 主角**
  * **形态与色彩**：圆润光滑的椭圆豆子体（高宽比 1.2:1），填充低饱和度暖黄 (`#F8E088` / `#F8DF72`)。
  * **线条描边**：柔和深咖啡色/炭灰手绘描边 (2-3px 均匀线宽)，带温和的手绘质感。
  * **五官肢体**：双眼为纯黑实心小圆点 (`● ●`)，嘴巴为微小弧形笑 (`∪`)。手脚短小圆润，无手指。
* **🩶 深灰豆豆 (Dark Gray Xiao Dou) — AI / 大模型 / 系统**
  * **形态与色彩**：与黄豆豆保持完全相同的豆子形态与描边风格，填充色为深灰色 (`#4A4D52`)。
  * **辅助特征**：体表或头部周围可悬浮代码框、数据接头或锁定图标，用以代表 AI / 大模型。

### 2. 🔴 避坑禁忌 (Negative Rules)

* ❌ **严禁物种混杂**：绝不能把 AI 画成蓝色的机械猫、金属机器人或外星异物种。
* ❌ **严禁画风漂移**：绝不生成立体 3D 渲染、死黑重边、粗暴无描边块面或复杂瞳孔睫毛。

---

## 🔒 防漂移垫图机制 (Anti-Drift Mechanism)

大语言模型与扩散模型在生成图像时容易产生风格微调漂移。**本 Skill 核心加入了垫图 (Image Reference) 机制**。

当 Agent 调用 `generate_image` 工具时，会自动强制挂载仓库内置的标准示例图作为底图参照：

```json
{
  "ImageName": "hallucination_4grid_correct",
  "ImagePaths": [
    "[workspace]/封面图/contextwindow.png",
    "[workspace]/配图/1.jpg"
  ],
  "Prompt": "Use the exact character design, line art style, face features, and color palette of Xiao Dou ('小豆') from the reference images...",
  "AspectRatio": "16:9"
}
```

通过“文字描述 + 图像参照”双重锁死，确保输出的角色风格、线条厚度与莫兰迪色彩调性 100% 保持一致。

---

## 📐 三大设计架构规范

根据文章的不同视觉需求，Skill 支持以下三大视觉表现模式：

### 1. 宽幅封面 — 左右对比模式 (Left-Right Contrast)
> 适合表现“痛点 vs 解决”、“旧方案 vs 新方案”、“高成本 vs 低成本”等强对比文章。

* **左侧 (痛点/旧态)**：暖灰/冷色背景，焦虑困惑的黄豆豆，搭配重物、乱线团、火苗等元素。
* **中央 (分割)**：带高对比度 `VS` 徽章或闪电分割线。
* **右侧 (终局/新态)**：清新绿/阳光背景，自信快乐的黄豆豆，搭配大剪刀、打勾整理箱等元素。

### 2. 宽幅封面 — 流程拆解模式 (Workflow Breakdown)
> 适合讲解原理、System Prompt 结构、AI 工作流等深度教程文章。

* **顶栏**：醒目粗体大标题 + 深色椭圆胶囊框金句（如 `AI听不见你想的，只执行你写的`）。
* **三段流程**：`左侧输入端 (想法/疑问)` ➔ `中间控制 UI (代码框/规则点)` ➔ `右侧输出端 (灯泡小豆/自由门)`。

### 3. 正文配图 — 2×2 四宫格知识矩阵 (4-Grid Matrix) ⭐ [核心模式]
> 适合作为文章正文中段的核心知识总结长图。

* **单宫格内部 4 层架构**：
  1. `顶栏`：粗体中文大标题
  2. `解说栏`：1-2 句核心释义段落
  3. `视觉区`：黄豆豆 / 深灰豆豆配合具体概念图解（思维导图、脑图、代码框、剪刀画笔、盾牌等）
  4. `底栏`：紧贴底部的核心总结金句
* **🔴 画面细节约束**：保持 4 宫格整洁纯净，**去除非必要的黑底 Hashtag 标签栏**。

---

## 🖼️ 效果大聚赏 (Showcase Gallery)

### 一、 宽幅文章封面图 (Cover Banners)

#### 1. 揭秘大模型与人类幻觉 (最新垫图锁定版)
![揭秘大模型与人类幻觉 封面](封面图/大模型幻觉_封面Banner.jpg)

#### 2. 揭秘 System Prompt (流程拆解架构)
![揭秘 System Prompt 封面](封面图/27D7DB6E-03B0-4739-9F17-054F58190C3E.png)

#### 3. Context Window 病 vs 截断+重置 (左右对比架构)
![Context Window 封面](封面图/contextwindow.png)

#### 4. 高效共享背景 vs 背景重建 (成本对比架构)
![Token 成本对比 封面](封面图/token.png)

---

### 二、 正文 2×2 四宫格知识配图 (Article 4-Grid Infographics)

#### 1. 大模型与人类幻觉 (最新垫图锁定版)
> <b>全员豆豆化 IP</b>：黄豆豆代表人类，深灰豆豆代表 AI，去除底部黑条。
![大模型与人类幻觉 4宫格配图](配图/大模型幻觉_4宫格_最新.jpg)

#### 2. 原生家庭是第一段 System Prompt (四宫格标准图 1)
![原生家庭 System Prompt 配图](配图/1.jpg)

#### 3. 你看不见的 System Prompt (四宫格标准图 2)
![你看不见的 System Prompt 配图](配图/2.jpg)

---

## 🚀 快速上手与 Prompt 模版

### 在 Google Antigravity / AGY Agent 中直接调用

只需将本仓库克隆或放置于你的 Workspace 中，直接在对话框中输入：

```text
“请帮我根据下面这篇关于【大模型上下文压缩】的文章，使用小豆 Skill 自动生成一张 16:9 封面 Banner 和一张正文 4 宫格视觉配图。”
```

### 提示词 (Prompt) 模板参考

```text
Use the exact character design, line art style, face features, soft dark brown outlines, and warm pastel color palette of Xiao Dou ("小豆") from the reference images.

Create a 2x2 grid infographic illustration featuring Xiao Dou (yellow bean) and dark gray bean AI character.
Clean vector storybook style, soft pastel palette, clear black Chinese text.

Layout: Pure 2x2 4-panel grid layout. Absolutely NO dark or black hashtag banner at the bottom.

Panel 1 (Top-Left): Title "[宫格1标题]", subtitle "[宫格1释义]", visual of Xiao Dou and dark gray bean AI filling missing data blocks, quote line at bottom.
Panel 2 (Top-Right): Title "[宫格2标题]", visual of Xiao Dou with scissors and paintbrush editing film frames, quote line at bottom.
Panel 3 (Bottom-Left): Title "[宫格3标题]", visual of dark gray bean AI admitting error and Xiao Dou holding a shield, quote line at bottom.
Panel 4 (Bottom-Right): Title "[宫格4标题]", visual of Xiao Dou reading a diary and looking out an open window, quote line at bottom.
```

---

## 📁 仓库目录结构

```text
小豆-skill/
├── SKILL.md                          # 🌟 AGY Skill 主指令定义文件 (含垫图与防漂移机制)
├── README.md                         # 📖 项目说明与展示文档
├── LICENSE                           # 📄 开源许可协议 (MIT)
├── references/                       # 📚 进阶规范参考库
│   ├── infographic_4grid_guide.md    # 📐 2x2 四宫格配图专项指南
│   ├── ip_prompt_guide.md            # 🎨 小豆 IP 形象解剖与 Prompt 词库
│   └── case_analysis.md              # 🔍 落地案例深度拆解
├── 封面图/                           # 🖼️ 宽幅 Banner 封面落地样例
│   ├── 大模型幻觉_封面Banner.jpg     # 🌟 最新生成的 16:9 封面
│   ├── 27D7DB6E-03B0-4739-9F17-054F58190C3E.png
│   ├── contextwindow.png
│   └── token.png
└── 配图/                             # 🖼️ 正文 4 宫格配图落地样例
    ├── 大模型幻觉_4宫格_最新.jpg       # 🌟 最新垫图锁定的 4 宫格配图
    ├── 1.jpg                         # 样例 1 (原生家庭 System Prompt)
    └── 2.jpg                         # 样例 2 (你看不到的 System Prompt)
```

---

## 📄 开源协议

本项目采用 [MIT License](LICENSE) 开源协议。欢迎基于“小豆” IP 拓展更多丰富的 AI 视觉图解与知识卡片场景！

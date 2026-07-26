# 小豆 IP 正文 4 宫格视觉配图 (4-Grid Infographic) 专项指南

本指南专门针对文章正文中的 **2×2 四宫格知识长图/精美视觉配图** 提供设计规范与 AI 绘图 Prompt 指南。

---

## 1. 核心视觉架构 (2×2 Grid Layout)

整张配图由 4 个独立的知识卡片呈矩阵排列组合而成，卡片之间以细浅色线条或微小留白分隔。

```text
+------------------------------------+------------------------------------+
| 宫格 1 (左上)                      | 宫格 2 (右上)                      |
| 大标题: 概念引入/底层定义          | 大标题: 现象揭示/隐性运行          |
| 释义段: ...                        | 释义段: ...                        |
| 插图: [大脑 + 小豆 + 图层金字塔]   | 插图: [代码框 + 对话气泡]          |
| 底栏总结: ...                      | 底栏总结: ...                      |
+------------------------------------+------------------------------------+
| 宫格 3 (左下)                      | 宫格 4 (右下)                      |
| 大标题: 机制对比/自我覆写          | 大标题: 识别觉察/行动方案          |
| 释义段: ...                        | 释义段: ...                        |
| 插图: [大模型代码 vs 人类叙事画笔] | 插图: [小豆思考 -> 推开自由之门]   |
| 底栏总结: ...                      | 底栏总结: ...                      |
+------------------------------------+------------------------------------+
```

---

## 2. 样例对比与微调原则

[配图/1.jpg](file:///Users/suxiaohan/Desktop/小豆-skill/配图/1.jpg) 与 [配图/2.jpg](file:///Users/suxiaohan/Desktop/小豆-skill/配图/2.jpg) **均为完全合格且期望的四宫格视觉表达与排版**。

* **完全正确的排版与构图**：两者在标题排版、释义段、小豆剧情插画以及单宫格总结文字上都非常优秀。
* **唯一需要调整细节**：`2.jpg` 最下方多了一行黑色底色的 Hashtag 标签栏（`#豆豆 #底层逻辑...`）。
* **生成控制指令**：在 AI 绘图生成时，只需要**去除最底下这行黑色标签栏**即可，其余 4 宫格卡片内容保持高水准呈现。

---

## 3. 4 宫格 Prompt 编写模版 (Prompt Template)

在调用 `generate_image` 时，使用如下 Prompt 模板：

```text
A 2x2 grid infographic illustration featuring the cute yellow round bean character ("Xiao Dou").
Clean vector storybook style, soft pastel color palette, clear black Chinese text headers.

Layout: Exactly 4 equal rectangular panels divided by subtle lines.
Do NOT include any black hashtag banner or bottom dark label row. Pure 4-panel grid layout.

Panel 1 (Top-Left):
- Title: "[宫格1标题]"
- Subtitle: "[宫格1释义]"
- Illustration: Xiao Dou with [物体1], showing [概念1].

Panel 2 (Top-Right):
- Title: "[宫格2标题]"
- Subtitle: "[宫格2释义]"
- Illustration: Xiao Dou dealing with [物体2], speech bubbles "[对话内容]".

Panel 3 (Bottom-Left):
- Title: "[宫格3标题]"
- Subtitle: "[宫格3释义]"
- Illustration: Comparison between [A] and [B] with Xiao Dou.

Panel 4 (Bottom-Right):
- Title: "[宫格4标题]"
- Subtitle: "[宫格4释义]"
- Illustration: Xiao Dou recognizing the mechanism and opening a door to [输出目标].

Overall: High resolution, professional article illustration, minimalist typography, cute and educational tone.
```

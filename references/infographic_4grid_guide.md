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

## 2. 合格与禁用标准对比

| 对比项 | 标注 1 (1.jpg - 合格标准) | 标注 2 (2.jpg - 禁用格式) |
| :--- | :--- | :--- |
| **画面整洁度** | 干净清爽，聚焦 4 宫格知识表达 | 底部强行挂载黑色标签栏，分散注意力 |
| **最底行元素** | 宫格 3 与 4 自有的总结文字行 | 最下方有一行黑色底色 `#豆豆 #底层逻辑...` 标签 |
| **使用建议** | **✅ 唯一推荐标准** | **❌ 严禁生成** |

---

## 3. 4 宫格 Prompt 编写模版 (Prompt Template)

在调用 `generate_image` 时，可使用如下英文 Prompt 模板：

```text
A 2x2 grid infographic illustration with cute yellow round bean character ("Xiao Dou").
Clean vector storybook style, soft pastel color palette, clear black Chinese text headers.

Layout: Exactly 4 equal rectangular panels divided by subtle gray lines.
NO BLACK HASHTAG BAR AT THE BOTTOM. Pure 4-panel grid layout only.

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

# 封面图与正文配图经典案例深度拆解

本文档拆解了项目目录下 [封面图](file:///Users/suxiaohan/Desktop/小豆-skill/封面图) 和 [配图](file:///Users/suxiaohan/Desktop/小豆-skill/配图) 文件夹中的落地案例，供生成新图时参考。

---

## 案例 1：正文 4 宫格标准配图 (合格样例)

* **源文件**：[配图/1.jpg](file:///Users/suxiaohan/Desktop/小豆-skill/配图/1.jpg)
* **核心模式**：2×2 逻辑矩阵 (4-Grid Infographic) — **【标准合格】**
* **结构拆解**：
  1. **宫格 1 (左上)**：`原生家庭是第一段 System Prompt` — 小豆戴眼镜指着脑图与层叠金字塔（System Manager / Specific Instructions）。
  2. **宫格 2 (右上)**：`静默运行与 “他者的 Prompt”` — 后台静默运行的代码编辑器 UI + 对话气泡（“我适合”、“我知道你为什么永远选错人”）。
  3. **宫格 3 (左下)**：`人的 System Prompt 可以被自我覆写` — 大模型 Frozen Code vs 人类叙事编辑器（小豆拿着画笔与键盘）。
  4. **宫格 4 (右下)**：`在它运行的那一秒，识别它` — 识别过程图解（“我就是这样的人” -> “识别” -> 推开自由之门）。
* **关键特征**：四宫格构图完整无瑕，**画面最底部没有黑色 Hashtag 标签栏**。

---

## 案例 2：带黑色标签栏的配图 (禁用样例)

* **源文件**：[配图/2.jpg](file:///Users/suxiaohan/Desktop/小豆-skill/配图/2.jpg)
* **核心模式**：2×2 逻辑矩阵 — **【严禁生成 style】**
* **存在问题**：
  - 最底部强行加入了一整行黑底文字标签：`#豆豆 #底层逻辑 #AI 视角 #自我重塑 #代码可写 #系统提示词 #自由意志`。
  - 影响正文阅读体验与卡片视觉纯粹性，生成 Prompt 时必须加入 Negative Prompt 禁用此黑条。

---

## 案例 3：揭秘 System Prompt (封面图)

* **源文件**：[封面图/27D7DB6E-03B0-4739-9F17-054F58190C3E.png](file:///Users/suxiaohan/Desktop/小豆-skill/封面图/27D7DB6E-03B0-4739-9F17-054F58190C3E.png)
* **核心模式**：流程与概念拆解 (Workflow & Concept Breakdown)
* **视觉亮点**：
  - 标题：`揭秘 System Prompt` + `AI听不见你想的，只执行你写的`
  - 结构：输入门（想法/困惑） -> 中间控制台 UI（规则/代码块） -> 输出门（亮灯泡小豆/自由）

---

## 案例 4：Context Window 病 vs 截断 + 重置 (封面图)

* **源文件**：[封面图/contextwindow.png](file:///Users/suxiaohan/Desktop/小豆-skill/封面图/contextwindow.png)
* **核心模式**：具象化痛点 vs 解决方案对比 (Problem vs Solution Contrast)
* **视觉亮点**：
  - 左侧痛点：小豆背负极其臃肿缠绕的信息线团，汗流浃背。
  - 右侧解决：小豆用剪刀剪断胶片并归档，轻松自信。

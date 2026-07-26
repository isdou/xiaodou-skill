# 小豆 (Xiao Dou) IP 绘图 Prompt 进阶与防漂移指南

本指南提供了使用 `generate_image` 生成“小豆”IP 形象封面图与配图时的 **防漂移垫图 (Image Reference)** 机制与 Prompt 词库。

---

## 1. 防漂移关键：垫图 (Image Reference) 机制

在进行 AI 绘图时，仅依靠文字 Prompt 容易造成线条变粗、瞳孔细节过度渲染或画风漂移。**必须配合垫图传入 `ImagePaths`**：

```json
{
  "ImagePaths": [
    "/Users/suxiaohan/Desktop/小豆-skill/封面图/contextwindow.png",
    "/Users/suxiaohan/Desktop/小豆-skill/配图/1.jpg"
  ]
}
```

在 Prompt 开线处加入以下固定一致性指令：

```text
Use the exact character design, line art style, face features, and color palette of Xiao Dou ("小豆") from the provided reference images.
```

---

## 2. 小豆 IP 精细化 Prompt 描述表

### 角色形象描述词 (Character Descriptors)

```text
Xiao Dou ("小豆"): Smooth round yellow bean shape, soft dark brown hand-drawn vector outline, two simple solid black dot eyes (no pupils, no eyelashes), tiny warm curved smile mouth (∪), short chubby bean-style limbs without fingers, soft yellow pastel fill (#F8E088).

AI / Large Model Bean ("深灰豆豆"): Same bean body shape and soft brown outline as Xiao Dou, but with a dark gray color fill (#4A4D52), representing AI systems. NO blue cat, NO mechanical parts.
```

### 常用情境动作与道具表

| 场景 | 精确 Prompt 描述 |
| :--- | :--- |
| **思考/发愁** | `Xiao Dou looking confused with hand on chin, tiny question mark floating above head` |
| **重构剪辑** | `Xiao Dou holding film scissors and a paintbrush, carefully editing movie film frames` |
| **防御证据** | `Xiao Dou holding a round shield labeled "有动机的推理" with an earnest cute expression` |
| **灵感觉察** | `Xiao Dou reading a diary book, taking a thoughtful pause, looking out an open window` |
| **困境与压迫** | `Xiao Dou sweating under a giant tangled cable knot on back, teary-eyed but cute` |

---

## 3. 标准 4 宫格 Prompt 模版 (含垫图约束)

```text
Use the exact character design, line art style, face features, and color palette of Xiao Dou ("小豆") from the reference images.

Create a 2x2 grid infographic illustration featuring Xiao Dou (yellow bean) and dark gray bean AI.
Clean vector storybook style, soft pastel palette, minimalist dark brown outlines, clear black Chinese text.

Layout: Pure 2x2 4-panel grid layout. Absolutely NO dark or black hashtag banner at the bottom.

Panel 1 (Top-Left):
- Title: "[宫格1标题]"
- Subtitle: "[宫格1释义]"
- Visual: Xiao Dou staring at [场景1]; Dark gray bean AI [动作1].
- Bottom Quote Line: "[总结金句1]"

Panel 2 (Top-Right):
- Title: "[宫格2标题]"
- Subtitle: "[宫格2释义]"
- Visual: Xiao Dou holding [工具2], [动作2].
- Bottom Quote Line: "[总结金句2]"

Panel 3 (Bottom-Left):
- Title: "[宫格3标题]"
- Subtitle: "[宫格3释义]"
- Visual: Dark gray bean AI admitting mistake; Xiao Dou holding a shield to block evidence.
- Bottom Quote Line: "[总结金句3]"

Panel 4 (Bottom-Right):
- Title: "[宫格4标题]"
- Subtitle: "[宫格4释义]"
- Visual: Xiao Dou reading a book, pausing in thought, looking out an open window.
- Bottom Quote Line: "[总结金句4]"
```

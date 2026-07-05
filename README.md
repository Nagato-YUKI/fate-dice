# 命运之骰 · Fate Dice

> *「当骰子落定，命运即被书写。」*

一个 **龙与地下城（DND）** 风格的在线掷骰子工具。以 CSS 3D 立方体呈现骰子翻滚的仪式感，遵循标准 DND 规则进行大成功与大失败判定，并配以 Web Audio API 程序化合成的音效。单文件运行，离线可用，适配桌面与移动端。

🜂 **在线体验**：[https://nagato-yuki.github.io/fate-dice/](https://nagato-yuki.github.io/fate-dice/)

---

## ✦ 卷轴一览 · Features

### 骰子与规则
- **六种骰子**：D4 / D6 / D8 / D10 / D12 / D20
- **多骰投掷**：支持 1–20 颗骰子同投，自动求和
- **标准 DND 判定**：仅 D20 触发大成功（自然 20）与大失败（自然 1）
- **多骰统计**：多 D20 投掷时分别统计大成功/大失败数量，并以独立样式高亮

### 视觉与音效
- **CSS 3D 立方体模型**：金色骰子六面成型，旋转动画自然落定
- **DND 主题视觉**：龙鳞纹理背景、符文圆环、魔法阵装饰
- **Web Audio API 音效**：程序化合成，无需音频文件
  - 投掷音效：带 0.35s 平滑淡出
  - 大成功：辉煌钟鸣
  - 大失败：低沉锣声下行
- **音效开关**：偏好持久化于 localStorage

### 工程与体验
- **单文件分发**：HTML + CSS + JS + 音效全部内嵌，一个文件即可运行
- **离线可用**：首次加载后无需网络
- **响应式布局**：适配桌面、平板、手机（768px / 375px 双断点）
- **无障碍**：`prefers-reduced-motion` 适配、ARIA 标签、noscript 提示
- **SEO / GEO**：JSON-LD 结构化数据、Open Graph、语义化 HTML

---

## ⚔ 锻造之术 · Tech Stack

| 领域 | 技术 |
|---|---|
| 3D 建模 | CSS 3D Transform（`transform-style: preserve-3d`） |
| 动画 | CSS `@keyframes` + `animation-fill-mode: forwards` |
| 音效合成 | Web Audio API（`OscillatorNode` / `GainNode` / `BufferSource`） |
| 音频加载 | `fetch()` + `decodeAudioData()`（base64 内嵌） |
| 持久化 | `localStorage`（音效偏好） |
| 字体 | Cinzel · Cormorant Garamond · MedievalSharp |
| 部署 | GitHub Pages |

---

## 🎲 使用指南 · Usage

### 冒险者入口

直接访问在线版本：[https://nagato-yuki.github.io/fate-dice/](https://nagato-yuki.github.io/fate-dice/)

### 本地运行

无需安装任何依赖，下载 `index.html` 后用浏览器打开即可：

```bash
git clone https://github.com/Nagato-YUKI/fate-dice.git
cd fate-dice
# 直接用浏览器打开 index.html
```

### 操作说明

1. **选择骰子**：点击 D4–D20 符文石碑切换骰子类型
2. **设置数量**：在数量栏输入 1–20
3. **投掷**：点击「掷骰」按钮，骰子将翻滚落定
4. **大成功/大失败**：仅 D20 会触发，投出 20 为大成功，投出 1 为大失败
5. **音效**：右上角图标切换开关，偏好会被记忆

---

## 🜁 部署 · Deploy

### GitHub Pages

仓库已配置为 GitHub Pages：
1. 进入仓库 **Settings → Pages**
2. **Source** 选择 `main` 分支
3. 保存后几分钟即可通过 `https://<用户名>.github.io/fate-dice/` 访问

### 其他静态托管

`index.html` 是纯静态单文件，可部署于任意静态托管服务：
- Vercel / Netlify / Cloudflare Pages
- Nginx / Apache
- 直接双击打开

---

## 🜂 浏览器支持 · Compatibility

| 浏览器 | 支持情况 |
|---|---|
| Chrome / Edge 88+ | ✅ 完整支持 |
| Firefox 87+ | ✅ 完整支持 |
| Safari 14+ | ✅ 完整支持 |
| 移动端 Safari / Chrome | ✅ 完整支持 |

需启用 JavaScript。音效需要用户首次交互后才能播放（浏览器自动播放策略）。

---

## 📜 许可 · License

MIT License — 自由使用、修改、分发。

---

## 🜂 关于 · About

> *「骰子不偏不倚，唯有命运决定一切。」*

本项目灵感源于龙与地下城（Dungeons & Dragons）跑团场景，旨在为 TRPG 玩家与桌游爱好者提供一个兼具仪式感与实用性的掷骰工具。

**作者**：[Nagato-YUKI](https://github.com/Nagato-YUKI)
**仓库**：[fate-dice](https://github.com/Nagato-YUKI/fate-dice)

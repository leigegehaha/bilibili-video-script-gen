<p align="center">
  <img src="https://img.shields.io/badge/B%E7%AB%99-视频脚本生成器-00A1D6?style=for-the-badge&logo=bilibili&logoColor=white" alt="B站视频脚本生成器"/>
</p>

<h1 align="center">bilibili-video-script-gen</h1>

<p align="center">
  <strong>一句话描述你的项目，AI 帮你生成完整的 B 站介绍视频制作方案</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/口播文案-有网感-FF6699?style=flat-square" />
  <img src="https://img.shields.io/badge/分镜脚本-逐镜头-00BFFF?style=flat-square" />
  <img src="https://img.shields.io/badge/AI提示词-图片+视频-9B59B6?style=flat-square" />
  <img src="https://img.shields.io/badge/制作流程-一站式-2ECC71?style=flat-square" />
</p>

---

## 这是什么？

你有一个开源项目或技术产品，想做一个 B 站介绍视频，但是——

> 文案不知道怎么写才有"网感"？分镜不知道怎么规划？AI 生图的提示词不会写？

这个 skill 帮你一键生成**完整的视频制作方案**，从口播文案到每个镜头的 AI 提示词，拿到手就能开工。

## 输出什么？

一份完整的 Markdown 制作方案，包含 5 大模块：

```
📋 视频信息    标题方案 · 时长规划 · 风格定义
📝 口播文案    分幕结构 · 强 Hook 开头 · 首尾呼应
🎬 分镜脚本    每个镜头的画面描述 · 口播对应 · 动效说明
🎨 AI 提示词   每个镜头的图片生成提示词 + 图生视频提示词
🔧 制作流程    工具链 · BGM · 字幕风格 · 素材清单
```

## 4 种视觉风格

| 风格 | 适合场景 | 色调 |
|:---:|:---:|:---:|
| **赛博朋克科技风** | 纯技术/工具类项目 | 深蓝紫 + 霓虹青粉 |
| **二次元插画风** | ACG/创意类项目 | 樱花粉 + 天空蓝 |
| **扁平化 Motion Graphics** | SaaS/产品发布 | 白底 + 品牌色 |
| **混合风格（科技+二次元）** | 技术服务于创意内容 | 科技蓝 ↔ 动漫粉渐变 |

## 分镜画面类型

| 类型 | 说明 | 制作方式 |
|------|------|----------|
| `[AI图]` | AI 生成静态图 + 缩放/平移动效 | AI 生图 → 剪辑软件 |
| `[AI图→视频]` | AI 生图后图生视频 | AI 生图 → Kling/Seedance/Veo |
| `[录屏]` | 实际屏幕录制 | OBS Studio |
| `[文字动画]` | 静态背景 + 文字动画 | 剪映 / AE |
| `[合成]` | 多素材合成 | 剪辑软件叠加 |
| `[录屏+AI图叠加]` | 录屏 + AI 装饰框 | 录屏 + 透明 PNG |

## 文案写作原则

参考 B 站高播放量开源项目视频的套路：

```
1. 强 Hook 开头     不要"大家好"，用场景化描述拉进痛点
2. 痛点共鸣        具象化描述用户的挫败体验
3. 类比解释        用视觉化类比代替干巴巴列功能
4. 对比演示        before vs after，差距一目了然
5. 技术快闪        硬核内容快节奏过，不拖沓不劝退
6. 实操为王        说再多不如看一遍
7. 首尾呼应        结尾金句回扣开头痛点
```

## AI 提示词规范

**图片生成提示词结构：**
```
[主体描述]。[环境/背景]。[光影/色调]。[风格关键词]。[构图]。[16:9, 1920x1080]。
```

**图生视频提示词结构：**
```
[运动描述]。[元素变化]。[镜头运动]。[时长]，[情绪/节奏关键词]。
```

## 推荐工具链

| 环节 | 推荐工具 |
|:---:|:---:|
| AI 生图 | Gemini / FLUX / Grok Image |
| 图生视频 | Kling 3.0 / Seedance 2.0 / Veo 3 |
| 屏幕录制 | OBS Studio |
| 剪辑 | 剪映专业版 / DaVinci Resolve |
| 配音 | 真人 / Edge TTS |
| BGM | 剪映素材库 / Suno AI |

## 使用方式

作为 AI 编程助手的 skill 使用。告诉 AI：

```
帮我做一个 B 站介绍视频

项目：[你的项目名]
简介：[一句话描述]
受众：[目标用户群]
风格：[选一个，或让 AI 推荐]
```

AI 会输出完整的视频制作方案 Markdown 文件。

## 制作步骤

```
 1. 生成所有 AI 静态图（约 15-25 张）
 2. 标注 [AI图→视频] 的镜头用图生视频生成 6 秒片段
 3. 录制实操演示
 4. 录制/生成口播音频
 5. 按分镜时间线剪辑拼接
 6. 添加文字动画和字幕
 7. 添加转场效果
 8. 配 BGM + 音效
 9. 最终调色输出
```

## 参考案例

`references/` 目录下包含一个完整的视频脚本案例（混合风格，7 幕 35 个分镜），可作为参考模板。

## 兼容平台

本 skill 可用于以下 AI 编程助手：

<p>
  <img src="https://img.shields.io/badge/Claude_Code-支持-D97706?style=flat-square" />
  <img src="https://img.shields.io/badge/Codex-支持-10B981?style=flat-square" />
  <img src="https://img.shields.io/badge/OpenCode-支持-3B82F6?style=flat-square" />
  <img src="https://img.shields.io/badge/OpenClaw-支持-8B5CF6?style=flat-square" />
  <img src="https://img.shields.io/badge/WorkBuddy-支持-EC4899?style=flat-square" />
  <img src="https://img.shields.io/badge/CodeBuddy-支持-F59E0B?style=flat-square" />
  <img src="https://img.shields.io/badge/Qwen-支持-6366F1?style=flat-square" />
</p>

## License

MIT

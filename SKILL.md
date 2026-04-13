---
name: bilibili-video-script-gen
description: 为开源项目/技术产品生成 B 站介绍视频的完整制作方案。包括：有网感的口播文案、混合风格分镜脚本、每个镜头的 AI 图片生成提示词、图生视频提示词、制作流程指南。适用于"帮我做一个 B 站介绍视频""写一个视频脚本""生成视频分镜"等场景。
---

# bilibili-video-script-gen

为开源项目或技术产品生成 B 站风格的介绍视频完整制作方案。

## 触发词

- B 站视频、bilibili 视频、介绍视频、视频脚本、视频文案
- 口播文案、分镜脚本、分镜提示词
- 开源项目视频、产品介绍视频

## 输出物

一个完整的视频制作方案文件（Markdown），包含：

1. **视频信息**：标题方案、时长、风格定义
2. **口播文案**：分幕结构，有网感、有故事感
3. **分镜脚本**：每个镜头的画面描述、口播对应、动效说明
4. **AI 提示词**：每个镜头的图片生成提示词 + 图生视频提示词
5. **制作流程**：工具链、步骤、BGM、字幕风格、素材清单

## 视觉风格库

### 风格 A：赛博朋克科技风
- 深色背景 + 霓虹光效 + 科技 UI
- 适合纯技术/工具类项目
- 色调：深蓝/紫 + 霓虹青/粉

### 风格 B：二次元插画风
- 明亮暖色调，日系动漫画风
- 适合面向二次元/ACG 受众的项目
- 色调：樱花粉/天空蓝/暖黄

### 风格 C：扁平化 Motion Graphics
- 简洁几何 + 流畅动画
- 适合产品发布、SaaS 工具
- 色调：白底 + 品牌色点缀

### 风格 D：混合风格（科技+二次元）
- 技术段落用科技风，展示段落用二次元风
- 转场用"蒸馏/变换"特效连接两种风格
- 最能体现"技术产品服务于创意内容"的概念

### 风格 E：像素复古风
- 8-bit / 16-bit 像素画风格，复古游戏机质感
- 适合游戏相关工具、怀旧向项目、独立开发者作品
- 色调：像素绿/琥珀色 CRT 屏幕色 + 低饱和复古色板
- 关键词：pixel art, retro gaming, 8-bit, CRT scanlines, chiptune aesthetic, low-res charm

### 风格 F：手绘白板风
- 白色/米色背景 + 手绘线条 + 手写字体
- 适合教程类、原理讲解类、算法可视化项目
- 色调：白底 + 黑色线条 + 马克笔彩色标注（红/蓝/绿）
- 关键词：whiteboard animation, hand-drawn sketch, marker pen, doodle style, educational illustration

### 风格 G：赛博中国风
- 传统水墨/国风元素 + 科技光效融合
- 适合中文 NLP、国产开源项目、文化科技类产品
- 色调：墨黑/宣纸白 + 朱红/金色 + 霓虹点缀
- 关键词：Chinese ink painting, cyberpunk fusion, red lantern neon, calligraphy hologram, oriental tech

### 风格 H：暗黑极简风
- 纯黑背景 + 极简白色排版 + 微妙光影
- 适合安全工具、终端工具、黑客/渗透类项目
- 色调：纯黑 + 白色文字 + 绿色终端光标 + 偶尔红色警告
- 关键词：dark minimal, terminal green, monospace typography, hacker aesthetic, matrix-inspired

### 风格 I：3D 等距风
- 等距视角 3D 插画，积木感模块化画面
- 适合架构图展示、微服务、云原生、DevOps 类项目
- 色调：柔和渐变（蓝紫/青橙）+ 轻投影 + 玻璃质感
- 关键词：isometric 3D, soft gradient, glass morphism, modular blocks, cloud architecture illustration

### 风格 J：纪录片电影风
- 真实感画面 + 电影调色 + 宽银幕比例
- 适合大型开源项目、社区故事、技术纪录片风格视频
- 色调：电影级调色（青橙对比 / 低饱和胶片感）+ 浅景深
- 关键词：cinematic, film grain, shallow depth of field, teal and orange grading, documentary style, anamorphic lens flare

## 文案写作原则

参考 B 站高播放量开源项目视频（如 liliMozi 的 OpenHanako）：

1. **强 Hook 开头**：不要"大家好"，用场景化描述把观众拉进痛点
2. **痛点共鸣**：具象化描述用户的挫败体验（终端报错、折腾一下午）
3. **类比解释**：用冰山、蒸馏、砖墙等视觉化类比代替干巴巴列功能
4. **对比演示**：before vs after，让差距一目了然
5. **技术快闪**：硬核内容用快节奏过，不拖沓不劝退
6. **实操为王**：说再多不如看一遍，真实演示最有说服力
7. **首尾呼应**：结尾金句回扣开头痛点，形成闭环

## 分镜画面类型

| 类型 | 说明 | 制作方式 |
|------|------|----------|
| [AI图] | AI 生成静态图，加简单动效（缩放/平移） | AI 生图 → 剪辑软件加动效 |
| [AI图→视频] | AI 生图后用图生视频让画面动起来 | AI 生图 → Kling/Seedance/Veo 生成 6 秒视频 |
| [录屏] | 实际屏幕录制 | OBS Studio |
| [文字动画] | 静态背景 + 文字/图标动画 | 剪辑软件 |
| [合成] | 多素材合成 | 剪辑软件叠加 |
| [录屏+AI图叠加] | 录屏上叠加 AI 生成的装饰框/面板 | 录屏 + 透明 PNG 叠加 |

## AI 提示词写作规范

### 图片生成提示词结构
```
[主体描述]。[环境/背景]。[光影/色调]。[风格关键词]。[构图]。[技术参数 16:9, 1920x1080]。
```

### 图生视频提示词结构
```
[运动描述]。[元素变化]。[镜头运动]。[时长]，[情绪/节奏关键词]。
```

### 关键原则
- 每个提示词必须包含画面比例（16:9）和分辨率（1920x1080）
- 科技段落关键词：cyberpunk, neon, holographic, dark background, circuit patterns, code rain
- 二次元段落关键词：anime style, warm colors, cherry blossom, soft lighting, pastel
- 混合风格转场：gradient from tech blue to anime pink, distillation visual metaphor

## 推荐工具链

| 环节 | 工具 | 备注 |
|------|------|------|
| AI 生图 | Gemini / FLUX / Grok Image | 分镜静态图 |
| 图生视频 | Kling 3.0 / Seedance 2.0 / Veo 3 | 6 秒视频片段 |
| 屏幕录制 | OBS Studio | 实操演示 |
| 剪辑 | 剪映专业版 / DaVinci Resolve | 拼接转场字幕 |
| 文字动画 | 剪映 / After Effects | 金句字幕 |
| 配音 | 真人 / Edge TTS / lei-reference-tts | 语音轨道 |
| BGM | 剪映素材库 / Suno AI | 背景音乐 |

## 使用方式

用户提供：
1. 项目名称和简介（或 README 链接）
2. 目标受众
3. 想要的视觉风格（或让 AI 推荐）
4. 参考视频（可选）

输出：完整的视频制作方案 Markdown 文件，保存到桌面。

## 参考案例

- `references/tavern-card-distiller-script.md` — 酒馆角色卡蒸馏器的完整视频脚本（混合风格）

## 制作步骤模板

1. 生成所有 AI 静态图（约 15-25 张）
2. 标注 [AI图→视频] 的镜头用图生视频生成 6 秒片段
3. 录制实操演示
4. 录制/生成口播音频
5. 按分镜时间线剪辑拼接
6. 添加文字动画和字幕
7. 添加转场效果
8. 配 BGM + 音效
9. 最终调色输出

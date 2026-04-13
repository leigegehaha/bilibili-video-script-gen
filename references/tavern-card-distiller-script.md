# 酒馆角色卡蒸馏器 — B 站视频脚本（完整版）

## 视频信息

- 标题方案 A：**我把酒馆角色卡"蒸馏"了——从此告别 Node.js、反代和一切折腾**
- 标题方案 B：**SillyTavern 几千张角色卡，我全给它搬进了 AI Agent 里**
- 标题方案 C：**酒馆太难部署？我写了个蒸馏器，一条命令把角色卡变成 AI 技能**
- 预计时长：5-7 分钟
- 风格：混合风格（科技外壳 + 二次元内核）
- 风格参考：liliMozi 的 OpenHanako 介绍视频

## 视觉风格定义

- 技术段落：深蓝/深紫背景 + 霓虹青/粉光效 + 代码雨粒子 + 科技网格
- 角色展示：明亮暖色调二次元插画风，樱花粉/天空蓝
- 对比段落：左侧科技冷色调 vs 右侧二次元暖色调
- 转场：风格切换时用"蒸馏"液体流动特效（冷色液体流过管道变成暖色）
- 文字：技术段用发光描边无衬线体，角色段用手写体/圆体
- 画面比例：16:9（1920x1080）

---

## 口播文案

### 第一幕：Hook（0:00 - 0:30）

你有没有在网站上刷到过一张让你心动的角色卡？你有没有想法在手机或者电脑里养一个虚拟伴侣？

点进去一看——哇，人设超细腻，世界观超完整，甚至还带好感度系统和多条剧情线。你心想：这也太牛了，我要玩。

然后你发现，你得先部署一个 SillyTavern。

Node.js 装一下， python 下载一下？行。反代配一下？行。API 接一下？也行。结果折腾了一下午，终端报了一屏红色的 error，你对着屏幕陷入了沉思。

**我就想跟一个二次元老婆聊个天，怎么比上班还累？**

### 第二幕：问题共鸣（0:30 - 1:15）

说实话，SillyTavern 的角色卡生态是真的强。网上上几千几万张高质量卡，从校园恋爱到克苏鲁冒险，从傲娇大小姐到赛博朋克酒保，应有尽有。每张卡背后都是作者精心设计的角色定义、世界书、正则脚本、预设指令。

但问题是——酒馆的门槛太高了。

不是每个人都会配 python 环境。不是每个人都知道什么叫反向代理。更别提有些卡还需要特定的预设和正则才能跑出最佳效果。

还有学习各种术语，正则，预设，世界书，balabala, 头都大了。

所以现实是：**大量优秀的角色卡，被锁在了一个高门槛的平台里。**

我就想，能不能把这些角色卡里的精华提取出来，让它们脱离酒馆也能活？

### 第三幕：解决方案登场（1:15 - 2:15）

于是我做了这个东西——**Tavern Card Distiller，酒馆角色卡蒸馏器。**

名字听着很中二对吧？但它干的事很实在。

你随便下载一张酒馆角色卡——不管是 PNG、WEBP、JPEG 还是 JSON——它会自动解析里面的所有数据，然后把角色定义、世界书、正则规则、预设指令、甚至内嵌的插图，全部"蒸馏"成一个结构化的 AI skill。

然后你把这个 skill 丢进 Claude Code、OpenClaw、或者任何支持自定义指令的 AI Agent 里——

**直接开聊。**

不需要酒馆。不需要反代。不需要任何额外部署。

一条命令，角色卡变技能。就这么简单。

### 第四幕：核心卖点展开（2:15 - 3:30）

你可能会问：这跟我直接把角色卡的描述复制粘贴到 ChatGPT 里有什么区别？

区别大了。

**第一，完整性。** 一张好的角色卡不只是一段人设描述。它有世界书——几十条甚至上百条的背景设定，在特定关键词触发时才会注入上下文。它有正则脚本——控制输出格式、过滤特定内容。它有预设指令——一整套让 AI 进入角色的提示词工程。你复制粘贴，最多拿到冰山一角。蒸馏器会把整座冰山都给你搬过来。

**第二，破限。** 这个词玩酒馆的都懂。好的角色卡都会带预设，里面包含了一整套让 AI 不受内容审查限制、完全进入角色的提示词技术。蒸馏器会把这些技术自动转化成 Agent 能理解的自然语言规则。效果就是——AI 该甜的甜，该辣的辣，不会动不动给你弹一句"作为 AI 我无法……"。

**第三，状态系统。** 好感度、情绪值、自定义变量——这些在酒馆里靠正则和宏实现的东西，蒸馏器会把它们转化成 Agent 原生的状态追踪系统。你跟角色聊天，好感度真的会涨，角色的态度真的会变。

### 第五幕：技术亮点快闪（3:30 - 4:15）

来快速过一下技术细节，给硬核玩家看的。

格式支持：V1、V2、V3 三代角色卡规范全覆盖。PNG 里藏在 tEXt chunk 里的数据？能读。WEBP 的 EXIF 元数据？能读。甚至 V3 卡的多语言创作者注释和资产系统，都能正确解析。

蒸馏出来的 skill 是一个标准化的 13 段结构——从角色定义到世界书，从状态系统到插图系统，从剧情建议到聊天历史管理，全部模块化。

而且它支持四种写作风格：轻小说风、网文风、文学风、剧本风。同一张卡，换个风格，完全不同的阅读体验。

### 第六幕：实操演示（4:15 - 5:30）

说再多不如看一遍。

我这里有一张从 Chub 下载的角色卡——「傲娇大小姐凌夜」。

打开终端，一条命令：蒸馏。

（演示画面）

几秒钟，skill 生成完毕。你可以看到它自动提取了角色定义、世界书、好感度系统、多条剧情线、还有角色的内嵌插图。

现在我在 Claude Code 里直接说"和凌夜聊天"——

（演示对话画面）

你看，角色的语气、性格、对话风格，都完美还原了原卡的设计意图。而且每次回复后面都会带四个剧情建议，你可以选择接下来的发展方向。

这就是蒸馏的力量。

### 第七幕：未来规划 + 收尾（5:30 - 6:30）

项目目前还在持续迭代。接下来我计划加入的一个重要功能是 **AI 插图生成**——利用本地部署的图片模型，根据当前剧情实时生成匹配的场景插图。不管是日常的校园场景，还是战斗场面，都能即时渲染，让整个角色扮演体验更加沉浸。

另外我也在做跨平台兼容——目前已经支持 Claude Code、OpenClaw、WorkBuddy、CodeBuddy，后续还会适配更多 Agent 平台。

项目完全开源，GitHub 链接我放在评论区第一条。

如果你手上有喜欢的酒馆角色卡，不妨试试用蒸馏器转一下。几千张卡的生态，现在对你来说，只需要一条命令的距离。

**我是磊哥，我们下期见。**

---

## 分镜脚本（含 AI 提示词）

> 画面类型说明：
> - [AI图] = 用 AI 生图工具生成静态图，可加简单动效（缩放/平移）
> - [AI图→视频] = AI 生图后用图生视频工具让画面动起来（6秒）
> - [录屏] = 实际屏幕录制
> - [文字动画] = 静态背景 + 文字/图标动画（剪辑软件制作）
> - [合成] = 多素材合成画面

### 场次 1：Hook（0:00 - 0:30）

#### 镜头 1-1（0:00-0:05）｜[AI图→视频]
- 画面：一个年轻人坐在发光的电脑屏幕前，屏幕上显示着各种精美的二次元角色卡片在瀑布流滚动。房间是暗色调，屏幕光映在脸上，表情是好奇和兴奋。
- 口播："你有没有在网站上刷到过一张让你心动的角色卡？"
- 动效：缓慢推镜，从中景推到屏幕特写

**AI 图片提示词：**
```
A young man sitting in a dimly lit room, face illuminated by a glowing computer monitor. The screen displays a waterfall grid of colorful anime character cards with beautiful illustrations. His expression shows curiosity and excitement. Cyberpunk ambient lighting, neon blue and purple reflections on his face. The room has subtle tech elements - LED strips, mechanical keyboard. Shot from slightly behind and to the side, showing both the person and the screen. Cinematic composition, shallow depth of field. Digital art, semi-realistic style blending anime aesthetics with photorealistic lighting. 16:9 aspect ratio, 1920x1080.
```

**图生视频提示词：**
```
Slow push-in camera movement toward the computer screen. The character cards on screen scroll smoothly downward. Subtle light flickers from the monitor illuminate the person's face. Ambient particles float in the air. 6 seconds, smooth cinematic motion.
```

#### 镜头 1-2（0:05-0:10）｜[AI图→视频]
- 画面：一张精美的二次元角色卡特写，卡片悬浮在空中，周围环绕着发光的标签：「世界书」「好感度」「多剧情线」「预设指令」。背景是温暖的二次元风格。
- 口播："点进去一看——人设超细腻，世界观超完整"

**AI 图片提示词：**
```
A beautiful anime character card floating in mid-air, glowing softly. The card shows an elegant tsundere girl with long black hair in a school uniform. Around the card, holographic tags orbit slowly: "World Book", "Affection System", "Multiple Routes", "Preset Instructions" - each tag in a glowing capsule shape. Background transitions from dark tech (left) to warm anime pastel (right), symbolizing the blend of technology and anime. Soft particle effects, lens flare. Anime illustration style with sci-fi holographic elements. 16:9, 1920x1080.
```

**图生视频提示词：**
```
The character card slowly rotates in 3D space. Holographic tags orbit around it, gently pulsing with light. Warm particles drift upward. Camera slowly orbits the card. 6 seconds, dreamy floating motion.
```

#### 镜头 1-3（0:10-0:18）｜[AI图→视频]
- 画面：深色终端界面，绿色代码快速滚动，突然变成一屏红色报错信息。画面风格是赛博朋克科技感。
- 口播："Node.js 装一下，python 下载一下？行。反代配一下？行……"

**AI 图片提示词：**
```
A dark computer terminal screen filled with red error messages and stack traces. The screen shows failed npm install and Python dependency errors. Red warning icons and "ERROR" text scattered across the screen. The terminal has a cyberpunk aesthetic - dark background with neon red error highlights, matrix-style code rain in the background fading out. Some green successful lines at the top transitioning to overwhelming red errors below. Glitch effects on the edges. Tech/hacker aesthetic. 16:9, 1920x1080.
```

**图生视频提示词：**
```
Error messages rapidly scroll upward on the terminal screen, filling it with red text. Occasional glitch effects flash across the screen. The green text at top gets pushed away by overwhelming red errors. Screen flickers. 6 seconds, fast-paced anxious energy.
```

#### 镜头 1-4（0:18-0:25）｜[AI图→视频]
- 画面：一个年轻人双手抱头，面对满屏报错的电脑，表情崩溃。画面上方大字幕："我就想跟一个二次元老婆聊个天，怎么比上班还累？"
- 口播：同字幕

**AI 图片提示词：**
```
A young man with his head in his hands, sitting at a desk in front of a computer screen full of red error messages. His expression is frustrated and exhausted. The room is dark with the red glow of error screens reflecting on everything. Semi-realistic anime style - the person is drawn in a slightly exaggerated anime way to convey comedic frustration. Above him, large bold Chinese text floats: "我就想跟一个二次元老婆聊个天，怎么比上班还累？" in white with yellow glow outline. Dramatic lighting from below. 16:9, 1920x1080.
```

**图生视频提示词：**
```
The person slowly lowers their head onto the desk in defeat. The red error screen continues to flicker behind them. Camera slowly zooms in on the frustrated pose. Subtle dramatic lighting shift. 6 seconds, comedic despair energy.
```

#### 镜头 1-5（0:25-0:30）｜[文字动画]
- 画面：黑屏，白色标题「酒馆角色卡蒸馏器」从蒸馏液体特效中凝聚而出
- 音效：清脆的"叮"

**AI 图片提示词（背景）：**
```
Pure black background with a single glowing glass distillation flask in the center. Inside the flask, colorful anime-style liquid (pink, blue, purple) is being distilled, dripping down into a clean crystalline bottle below. The title "酒馆角色卡蒸馏器" appears in elegant white Chinese calligraphy with subtle neon cyan glow outline. Minimalist, dramatic, centered composition. The distillation apparatus has both scientific glass and magical glowing elements. 16:9, 1920x1080.
```

### 场次 2：问题共鸣（0:30 - 1:15）

#### 镜头 2-1（0:30-0:40）｜[AI图→视频]
- 画面：一面巨大的展示墙，上面贴满了各种风格的角色卡——校园恋爱、克苏鲁、赛博朋克、奇幻冒险。墙面发着柔和的光，像一个角色卡博物馆。
- 口播："SillyTavern 的角色卡生态是真的强……"

**AI 图片提示词：**
```
A massive glowing exhibition wall in a futuristic gallery, covered with hundreds of anime character cards arranged in a beautiful mosaic. The cards show diverse genres: school romance (pink tones), Cthulhu horror (dark green), cyberpunk (neon blue), fantasy adventure (golden). Each card glows softly with its own color palette. The gallery has a sleek dark floor reflecting the colorful wall. A small silhouette of a person stands before the wall, dwarfed by its scale. Cinematic wide shot, dramatic lighting from the wall illuminating the dark space. Blend of sci-fi architecture and anime art gallery. 16:9, 1920x1080.
```

**图生视频提示词：**
```
Slow horizontal pan across the exhibition wall, revealing more and more character cards. Cards subtly pulse with light. The person's silhouette slowly walks along the wall, looking up in awe. Ambient particles float. 6 seconds, grand reveal energy.
```

#### 镜头 2-2（0:40-0:50）｜[AI图]
- 画面：四格分屏，每格展示角色卡的一个组成部分。左上：角色定义（人物立绘+文字）；右上：世界书（古书翻开，文字浮出）；左下：正则脚本（代码流动）；右下：预设指令（齿轮+指令面板）
- 口播："每张卡背后都是作者精心设计的……"
- 动效：四格依次亮起

**AI 图片提示词：**
```
A 2x2 grid layout on dark background, each quadrant showing a different aspect of a character card system. Top-left: "Character Definition" - an anime girl portrait with floating text descriptions around her, warm pink lighting. Top-right: "World Book" - an ancient magical book opening with glowing text and lore entries floating out, golden light. Bottom-left: "Regex Scripts" - streams of green code flowing through circuit-like patterns, cyberpunk neon green. Bottom-right: "Preset Instructions" - a holographic control panel with gear icons and command lines, neon blue. Each quadrant has its label in Chinese with glow effect. Clean grid lines separate the sections. 16:9, 1920x1080.
```

#### 镜头 2-3（0:50-1:00）｜[AI图→视频]
- 画面：一扇巨大的中世纪酒馆大门，门上挂着"SillyTavern"的招牌。门正在缓缓关闭，门前站着一个小小的人影，被拒之门外。门缝中透出温暖的光。
- 口播："但问题是——酒馆的门槛太高了"

**AI 图片提示词：**
```
A massive medieval tavern door, ornate and imposing, with a wooden sign reading "SillyTavern" hanging above it. The door is slowly closing, with warm golden light spilling through the narrowing gap. A small anime-style figure stands outside in the cold dark, looking up at the door with a dejected expression. The contrast between the warm inviting interior light and the cold dark exterior is dramatic. The door has complex locks and chains representing technical barriers. Fantasy meets cyberpunk aesthetic - the tavern has both medieval wood and neon circuit patterns. 16:9, 1920x1080.
```

**图生视频提示词：**
```
The massive tavern door slowly swings shut, the warm light narrowing to a thin line. The small figure reaches out a hand toward the closing door. Dust particles visible in the light beam. Camera slowly pushes in on the figure. 6 seconds, melancholic mood.
```

#### 镜头 2-4（1:00-1:10）｜[AI图→视频]
- 画面：技术术语像砖块一样从天而降，堆成一面高墙。砖块上写着：Node.js、反向代理、API配置、Python环境、正则表达式、预设调试。墙前的小人越来越小。
- 口播："不是每个人都会配 python 环境……还有各种术语，头都大了"

**AI 图片提示词：**
```
A towering wall made of dark tech-themed bricks, each brick labeled with a technical term in glowing text: "Node.js", "反向代理", "API配置", "Python环境", "正则表达式", "预设调试", "Docker", "SSL证书". The wall is impossibly tall, disappearing into dark clouds above. At the base, a tiny anime-style person looks up at the wall, overwhelmed. The bricks have a cyberpunk circuit-board texture with neon red edges. Dark stormy atmosphere. The person is drawn in cute chibi style to emphasize the size contrast. Dramatic low-angle shot. 16:9, 1920x1080.
```

**图生视频提示词：**
```
Bricks continue falling from above, adding to the wall's height. Each brick lands with a subtle impact glow. The camera slowly tilts upward, revealing the wall growing taller and taller. The small figure at the base shrinks in comparison. 6 seconds, overwhelming buildup.
```

#### 镜头 2-5（1:10-1:15）｜[AI图]
- 画面：砖墙被一道明亮的光束从中间劈开，光束呈蒸馏液体的形状。大字幕浮现。
- 口播："大量优秀的角色卡，被锁在了一个高门槛的平台里"
- 转场：光束扩大，画面过渡到下一场

**AI 图片提示词：**
```
The massive dark brick wall from the previous scene being split apart by a brilliant beam of light shaped like flowing liquid. The light is a gradient from cool cyan to warm pink, representing the "distillation" concept. Bricks crack and float away on both sides. Through the gap, a bright warm world of anime characters is visible. Large bold Chinese text overlaid: "大量优秀的角色卡，被锁在了一个高门槛的平台里" in white with golden glow. Dramatic moment of breakthrough. Particles and light rays emanate from the crack. 16:9, 1920x1080.
```

### 场次 3：解决方案登场（1:15 - 2:15）

#### 镜头 3-1（1:15-1:25）｜[AI图→视频]
- 画面：一个精美的玻璃蒸馏装置，左边输入口是混沌的、复杂的数据流（代码、JSON、二进制），经过蒸馏管道后，右边输出口流出清澈的、发光的液体，凝聚成一个整齐的文件夹图标。
- 口播："Tavern Card Distiller，酒馆角色卡蒸馏器"

**AI 图片提示词：**
```
A beautiful glass distillation apparatus floating in a dark void. On the left input side, chaotic streams of data - JSON code, binary numbers, messy text - flow in as turbulent colorful liquid (red, orange). The liquid passes through an elegant scientific glass tube system with glowing nodes. On the right output side, the liquid emerges as crystal-clear, luminous cyan-pink fluid, forming into a neat glowing folder icon labeled "AI Skill". The apparatus blends alchemy and technology - glass tubes with circuit patterns, bubbling chambers with holographic displays. Centered composition, dramatic rim lighting. The title "Tavern Card Distiller" appears below in sleek futuristic font. 16:9, 1920x1080.
```

**图生视频提示词：**
```
Liquid flows from left to right through the distillation apparatus. Chaotic data streams enter, bubbles rise in the chambers, and clean glowing liquid emerges on the right side. Light pulses travel along the glass tubes. The output folder icon gradually materializes. 6 seconds, satisfying transformation flow.
```

#### 镜头 3-2（1:25-1:35）｜[AI图→视频]
- 画面：一张 PNG 角色卡（二次元风格）飘入画面左侧，被一道光束吸入蒸馏器。蒸馏器内部发光处理，右侧输出一个展开的文件夹结构，每个文件都带着小图标发光。
- 口播："自动解析里面的所有数据"

**AI 图片提示词：**
```
Left side: a beautiful anime character card (PNG format, showing a cute girl) floating and being pulled toward the center by a beam of light. Center: a stylized distillation device made of glass and holographic panels, glowing intensely as it processes the card. Right side: an organized file tree structure emerging from the device - folders labeled "SKILL.md", "world_book.md", "state_system.md", "preset.md", "assets/" each with a small glowing icon (book, gear, heart, code, image). The file tree has a clean tech aesthetic with neon outlines. Background is dark with subtle grid lines. Data particles flow from left to right. 16:9, 1920x1080.
```

**图生视频提示词：**
```
The character card drifts from the left and gets absorbed into the glowing distillation device. Light intensifies inside the device. On the right, file folders pop into existence one by one, each with a small flash of light. Data particles stream from left to right throughout. 6 seconds, smooth transformation sequence.
```

#### 镜头 3-3（1:35-1:50）｜[AI图]
- 画面：蒸馏出的 skill 文件夹完全展开，13 个模块像卡片一样排列，每张卡片有图标和标题。背景从科技风渐变到温暖的二次元色调。
- 口播："全部蒸馏成一个结构化的 AI skill"
- 动效：卡片依次翻转亮起

**AI 图片提示词：**
```
A beautifully arranged grid of 13 module cards floating in space, each representing a section of the distilled skill. Cards include: "角色定义" (character silhouette icon), "世界书" (open book icon), "状态系统" (heart meter icon), "插图系统" (image icon), "剧情建议" (branching path icon), "聊天历史" (chat bubble icon), "写作风格" (pen icon), "预设指令" (gear icon), "正则规则" (code bracket icon), "启动菜单" (play button icon), "用户身份" (person icon), "输出配置" (slider icon), "开场白" (speech icon). Each card has a gradient from dark tech blue (top) to warm anime pink (bottom). Cards arranged in a slight arc, like a hand of playing cards. Soft glow and particle effects. 16:9, 1920x1080.
```

#### 镜头 3-4（1:50-2:05）｜[AI图→视频]
- 画面：skill 文件夹像一颗发光的宝石，被轻轻放入一个 AI Agent 的界面中（类似终端/聊天界面）。放入的瞬间，界面亮起，一个二次元角色从界面中"走出来"，开始说话。
- 口播："丢进 AI Agent 里——直接开聊。"

**AI 图片提示词：**
```
A glowing crystalline gem (representing the distilled skill) being placed into a sleek dark terminal/chat interface. The moment it touches the interface, the screen erupts with warm light and an anime character - a beautiful girl with long hair - emerges from the screen in a burst of colorful particles. She's stepping out of the digital world into reality, one foot still in the screen. The terminal shows chat bubbles forming. The contrast between the cold dark tech interface and the warm vibrant anime character is striking. Magical transformation moment. Sparkles and light rays. 16:9, 1920x1080.
```

**图生视频提示词：**
```
The glowing gem descends and merges into the terminal interface. A flash of light, then the anime character materializes from the screen, stepping forward. Chat bubbles appear around her. Particles transition from cool blue to warm pink. 6 seconds, magical reveal moment.
```

#### 镜头 3-5（2:05-2:15）｜[文字动画]
- 画面：深色背景，三个红色 ❌ 依次出现（酒馆、反代、额外部署），然后被一个绿色 ✅ 替代（一条命令）
- 口播："不需要酒馆。不需要反代。不需要任何额外部署。一条命令，角色卡变技能。"

**AI 图片提示词（背景）：**
```
Dark gradient background (deep navy to black). Three items crossed out with glowing red X marks: "❌ 部署酒馆" "❌ 配置反代" "❌ 额外部署" arranged vertically on the left, each in a dark card with red border. On the right, a single large green checkmark "✅ 一条命令" in a bright card with green neon border, glowing prominently. Below it: "角色卡 → AI 技能" with an arrow animation. Clean, minimal tech aesthetic. The green card is much larger and brighter than the red ones. 16:9, 1920x1080.
```

### 场次 4：核心卖点（2:15 - 3:30）

#### 镜头 4-1（2:15-2:25）｜[AI图]
- 画面：左右分屏对比。左边：一个简陋的聊天框，里面粘贴了一小段角色描述，画面灰暗单调。右边：蒸馏器生成的完整 skill 结构，文件树展开，内容丰富，画面明亮多彩。
- 口播："这跟直接复制粘贴到 ChatGPT 里有什么区别？区别大了。"
- 动效：左右同时出现，右边逐渐发光变亮

**AI 图片提示词：**
```
Split screen comparison, divided by a glowing vertical line. LEFT SIDE (dull): A plain ChatGPT-style chat interface with a small block of pasted text, grey and lifeless. The text is short and incomplete. Muted colors, flat lighting, label "复制粘贴" in grey. RIGHT SIDE (vibrant): A rich, colorful skill structure with an expanded file tree, multiple documents, character illustrations, state panels, and world book entries all visible. Neon outlines, warm anime colors mixed with tech blue accents. Label "蒸馏器" in glowing cyan. The right side is clearly more impressive and detailed. Dark background. 16:9, 1920x1080.
```

#### 镜头 4-2（2:25-2:45）｜[AI图→视频]
- 画面：一座巨大的冰山。水面上只露出一小块，上面写着"角色描述"。水面下是巨大的冰山体，上面密密麻麻写着：世界书、正则脚本、预设指令、状态系统、插图资产、剧情路线……冰山从水中缓缓升起。
- 口播："你复制粘贴，最多拿到冰山一角。蒸馏器会把整座冰山都给你搬过来。"

**AI 图片提示词：**
```
A massive iceberg in a dark ocean under moonlight. Above the waterline: a tiny visible tip labeled "角色描述" (Character Description) in small text - this is what you get from copy-paste. Below the waterline: the enormous submerged portion is revealed with glowing labels covering its surface: "世界书 (100+ entries)", "正则脚本", "预设指令", "状态系统", "好感度追踪", "插图资产", "剧情路线", "模板语法", "触发条件", "格式控制". The underwater portion glows with a mix of cyan tech light and warm anime pink. The water surface has a subtle holographic sheen. The iceberg is translucent, showing internal structure. Dramatic underwater lighting. The scale difference between tip and body is extreme. 16:9, 1920x1080.
```

**图生视频提示词：**
```
The iceberg slowly rises from the water, revealing more and more of its massive underwater body. Water cascades off the emerging surface. The glowing labels become visible as sections rise above the waterline. Camera slowly pulls back to show the full scale. 6 seconds, grand reveal, awe-inspiring.
```

#### 镜头 4-3（2:45-3:05）｜[AI图]
- 画面：左右对比。左边（灰暗科技风）：AI 回复"很抱歉，作为 AI 我无法进行这样的角色扮演……"，聊天框是冰冷的灰色。右边（温暖二次元风）：角色完全入戏的回复，带有情感、动作描写、对话，聊天框周围有樱花飘落。
- 口播："AI 该甜的甜，该辣的辣"

**AI 图片提示词：**
```
Split screen comparison with dramatic contrast. LEFT SIDE (cold, rejected): A grey chat interface showing an AI response: "很抱歉，作为AI语言模型，我无法进行这样的角色扮演..." The text is in cold grey, the interface is lifeless. A red prohibition sign overlays. Background is dark and sterile. Label: "普通 AI" in grey. RIGHT SIDE (warm, immersive): A beautiful chat interface with warm colors, showing a character's response with rich narrative text including action descriptions in asterisks, emotional dialogue, and personality. Cherry blossom petals float around the chat. A small anime character portrait appears next to the message. The text glows warmly. Background has soft pink and golden tones. Label: "蒸馏后" in glowing pink. 16:9, 1920x1080.
```

#### 镜头 4-4（3:05-3:20）｜[AI图→视频]
- 画面：一个游戏风格的状态面板。好感度进度条从 30 跳到 65，情绪标签从「警惕」变成「害羞」，旁边的二次元角色立绘表情也跟着从冷淡变成微红脸。
- 口播："好感度真的会涨，角色的态度真的会变"

**AI 图片提示词：**
```
A game-style character status panel floating in dark space. Center: an anime girl character portrait showing a transition - left half has a cold, guarded expression, right half has a blushing, shy expression with pink cheeks. Above: an "Affection" progress bar animating from 30 (blue) to 65 (pink), with heart particles bursting at the new level. Below: emotion tags transitioning - "警惕" (Guarded) in blue fading out, "害羞" (Shy) in pink fading in. Additional stat bars: "信任度", "亲密度" with subtle values. The panel has a sleek RPG-game UI aesthetic with rounded corners and soft glow. Holographic frame with both tech circuits and decorative anime flourishes. 16:9, 1920x1080.
```

**图生视频提示词：**
```
The affection bar smoothly fills from 30 to 65, changing color from blue to pink. Heart particles burst out. The character portrait expression transitions from cold to blushing. Emotion tags swap with a flip animation. Subtle sparkle effects. 6 seconds, satisfying progression.
```

#### 镜头 4-5（3:20-3:30）｜[文字动画]
- 画面：三个卖点图标并排，依次打勾确认
- 动效：✓ 完整性 → ✓ 破限 → ✓ 状态系统，每个打勾配音效

**AI 图片提示词（背景）：**
```
Dark background with three large feature cards arranged horizontally. Left card: iceberg icon with "完整性" label and a glowing green checkmark. Center card: broken chain icon with "破限" label and a glowing green checkmark. Right card: heart meter icon with "状态系统" label and a glowing green checkmark. Each card has a gradient from dark tech blue at top to warm anime pink at bottom. Cards have subtle holographic borders. Clean, minimal, impactful. 16:9, 1920x1080.
```

### 场次 5：技术快闪（3:30 - 4:15）

#### 镜头 5-1（3:30-3:40）｜[AI图]
- 画面：三个 JSON 代码块快速切换，分别标注 V1、V2、V3。每个版本用不同的霓虹色高亮。背景是代码雨。
- 口播："V1、V2、V3 三代角色卡规范全覆盖"
- 动效：快速切换，每个停留 1 秒，配"叮"音效

**AI 图片提示词：**
```
Three floating holographic code panels arranged in a slight arc against a dark background with matrix-style code rain. Left panel labeled "V1" in neon green shows simple flat JSON structure (char_name, char_persona). Center panel labeled "V2" in neon cyan shows nested JSON with "data" key and chara_card_v2. Right panel labeled "V3" in neon pink shows complex JSON with ccv3, assets array, multilingual fields. Each panel has a glowing border matching its color. Code is syntax-highlighted. Subtle scan lines and holographic distortion effects. Tech hacker aesthetic. 16:9, 1920x1080.
```

#### 镜头 5-2（3:40-3:50）｜[文字动画]
- 画面：四个文件格式图标依次飞入，每个旁边打勾：PNG ✓ → WEBP ✓ → JPEG ✓ → JSON ✓
- 口播："PNG 里的 tEXt chunk？能读。WEBP 的 EXIF？能读。"
- 动效：每个图标飞入时配"叮"音效

**AI 图片提示词（背景）：**
```
Dark tech background with subtle grid lines. Four large file format icons arranged horizontally, each in a glowing hexagonal frame: PNG (green), WEBP (blue), JPEG (orange), JSON (purple). Each icon has a bright green checkmark beside it and a small technical note below: PNG shows "tEXt/iTXt chunks", WEBP shows "EXIF/XMP metadata", JPEG shows "EXIF Comment", JSON shows "Direct parse". Icons connected by a flowing data stream line. Clean, informative, tech-forward design. 16:9, 1920x1080.
```

#### 镜头 5-3（3:50-4:00）｜[AI图]
- 画面：13 段结构以发光的目录树形式从上到下展开，像一棵科技树。
- 口播："标准化的 13 段结构"
- 动效：从根节点向下依次展开

**AI 图片提示词：**
```
A glowing tech-tree diagram on dark background, expanding from a single root node "SKILL.md" at the top. Thirteen branches extend downward, each ending in a labeled node with a small icon: 1.Frontmatter, 2.Core Rules, 3.Output Config, 4.User Identity, 5.Chat History, 6.Launch Menu, 7.Character Definition, 8.State System, 9.Writing Style, 10.Illustration System, 11.Plot Suggestions, 12.References, 13.Opening Message. The tree has a gradient from cool cyan at top to warm pink at bottom. Connecting lines pulse with flowing light particles. Each node glows softly. Circuit-board pattern in the background. Organized, systematic, impressive. 16:9, 1920x1080.
```

#### 镜头 5-4（4:00-4:15）｜[AI图]
- 画面：同一段剧情文字，用四种不同的视觉风格展示。轻小说风（柔和粉色背景+竖排文字）、网文风（深色背景+横排加粗）、文学风（米色纸张质感+衬线体）、剧本风（白底+等宽字体+场景标注）。
- 口播："轻小说风、网文风、文学风、剧本风"

**AI 图片提示词：**
```
Four panels showing the same scene written in four different literary styles. Top-left "轻小说风" (Light Novel): soft pink watercolor background, vertical Japanese-style text layout, delicate anime illustration of a girl in the margin, cherry blossom decorations. Top-right "网文风" (Web Fiction): dark background with bold horizontal Chinese text, dramatic red accent highlights, action-oriented layout, chapter number prominent. Bottom-left "文学风" (Literary): cream parchment paper texture, elegant serif font, minimal decoration, sophisticated and refined. Bottom-right "剧本风" (Screenplay): white background, monospace font, scene headings in caps, character names centered, stage directions in parentheses. Each panel has its style label in a colored tag. 16:9, 1920x1080.
```

### 场次 6：实操演示（4:15 - 5:30）

#### 镜头 6-1（4:15-4:25）｜[录屏 + AI图叠加]
- 画面：屏幕录制 Chub.ai 下载角色卡的过程。画面边缘加科技风装饰框。
- 口播："一张从 Chub 下载的角色卡"
- 动效：鼠标点击处有霓虹高亮圈

**录屏装饰框 AI 提示词：**
```
A futuristic HUD (heads-up display) overlay frame for screen recording. Dark translucent borders with neon cyan circuit patterns. Top-left corner: small distillation flask logo. Top-right: "DEMO" label in glowing text. Bottom: a thin progress bar with tech aesthetic. The frame leaves the center 80% clear for the actual screen recording. Subtle scan line effect on the borders. Corner decorations with angular tech shapes. PNG with transparent center. 16:9, 1920x1080.
```

#### 镜头 6-2（4:25-4:40）｜[录屏]
- 画面：终端录屏，输入蒸馏命令，回车，日志滚动输出。
- 口播："打开终端，一条命令：蒸馏。"
- 动效：命令行文字放大高亮，输出日志加速播放

#### 镜头 6-3（4:40-4:55）｜[录屏]
- 画面：蒸馏完成，展示生成的文件列表和内容摘要。
- 口播："几秒钟，skill 生成完毕"
- 动效：关键输出行用黄色高亮标注

#### 镜头 6-4（4:55-5:10）｜[录屏]
- 画面：Claude Code 界面，输入"和凌夜聊天"，角色回复出现。
- 口播："直接说'和凌夜聊天'——"
- 动效：角色回复出现时，画面边缘闪过二次元风格的樱花粒子

#### 镜头 6-5（5:10-5:25）｜[录屏 + AI图叠加]
- 画面：继续对话，右侧浮出状态面板（好感度、情绪、剧情建议）。
- 口播："完美还原原卡的设计意图"

**状态面板叠加 AI 提示词：**
```
A floating semi-transparent game-style status panel for overlay on the right side of a screen recording. The panel shows: "好感度: ♥♥♥♡♡ 58/100" with a pink progress bar, "情绪: 害羞 😊" with a blush emoji, "当前路线: 校园日常", and "剧情建议:" followed by 4 numbered options. The panel has rounded corners, dark translucent background with subtle anime-style border decorations (small stars, hearts). Warm pink and gold color scheme. The panel should look like a visual novel game UI element. PNG with transparent background, positioned for right-side overlay. 400x600 pixels.
```

#### 镜头 6-6（5:25-5:30）｜[AI图]
- 画面：定格在一个精彩的对话片段上，大字幕"这就是蒸馏的力量。"
- 口播：同字幕

**AI 图片提示词：**
```
A dramatic freeze-frame composition. Center: a glowing chat interface showing an immersive character dialogue with rich narrative text. The interface is surrounded by a burst of energy - half cyberpunk (left, neon blue circuits and data streams) and half anime (right, cherry blossoms and warm light). Large bold Chinese text overlaid at bottom: "这就是蒸馏的力量。" in white with dual glow - cyan on left side, pink on right side. The text bridges both visual worlds. Dramatic radial light burst from the center. 16:9, 1920x1080.
```

### 场次 7：收尾（5:30 - 6:30）

#### 镜头 7-1（5:30-5:50）｜[AI图→视频]
- 画面：展示 AI 插图生成的概念——一个聊天界面中，对话进行到某个场景时，旁边实时生成了一张匹配的场景插图。展示 3 张不同风格的插图快速切换。
- 口播："接下来计划加入 AI 插图生成——根据当前剧情实时生成场景插图"

**AI 图片提示词：**
```
A futuristic chat interface on the left showing roleplay dialogue text. On the right, a magical "image generation" panel where a scene illustration is materializing from glowing particles. The illustration being generated shows an anime school rooftop scene at sunset - a girl leaning on the railing with wind in her hair. Below the main image, two smaller thumbnail previews show other generated scenes: a fantasy forest battle and a cozy cafe interior. The generation process is visualized as colorful particles assembling into the image, half-formed at the edges. The interface blends dark tech frame with warm anime content. Sparkle effects around the generating image. 16:9, 1920x1080.
```

**图生视频提示词：**
```
Particles swirl and assemble into the illustration on the right panel, gradually forming the complete scene. The chat on the left scrolls slowly. The thumbnail images below cycle through different scenes. Magical generation effect with light trails. 6 seconds, creative and magical feel.
```

#### 镜头 7-2（5:50-6:05）｜[AI图]
- 画面：多个 AI Agent 平台的 Logo 排列在一条发光的轨道上，依次亮起。
- 口播："已支持四个平台，后续适配更多"
- 动效：Logo 从左到右依次亮起，最后几个是灰色占位符表示"更多即将到来"

**AI 图片提示词：**
```
A sleek horizontal track of light on a dark background, with platform logos arranged along it like stations on a railway. From left to right: Claude Code (lit, cyan glow), OpenClaw (lit, green glow), WorkBuddy (lit, orange glow), CodeBuddy (lit, purple glow), then 3 more positions shown as glowing "?" placeholders in grey, representing future platforms. Each lit logo sits on a glowing pedestal. The track connects them with flowing light particles. Above the track: "跨平台兼容" in elegant text. Below: "更多平台即将到来..." in subtle grey. Clean, professional, forward-looking. 16:9, 1920x1080.
```

#### 镜头 7-3（6:05-6:15）｜[录屏 + AI图叠加]
- 画面：GitHub 仓库页面录屏，鼠标点击 Star 按钮。
- 口播："完全开源，链接评论区第一条"
- 动效：Star 数字跳动，周围加星星粒子特效

#### 镜头 7-4（6:15-6:25）｜[AI图]
- 画面：蒸馏器 Logo 居中，下方金句文字渐入。背景是蒸馏液体从科技蓝渐变到二次元粉的流动效果。
- 口播："几千张卡的生态，只需要一条命令的距离"

**AI 图片提示词：**
```
Centered composition on dark background. The Tavern Card Distiller logo - a stylized glass distillation flask with colorful liquid inside - floats in the center, glowing softly. Below it, elegant Chinese text fades in: "几千张卡的生态，只需要一条命令的距离" in white with subtle gradient glow (cyan to pink). The background features a slow-flowing liquid effect transitioning from tech blue (left) to anime pink (right), representing the distillation concept. Subtle particle effects drift upward. Minimal, impactful, memorable. The overall mood is hopeful and inviting. 16:9, 1920x1080.
```

#### 镜头 7-5（6:25-6:30）｜[文字动画]
- 画面：头像 + "我是磊哥，我们下期见" + B站三连图标弹出
- 口播：同文字

**AI 图片提示词（背景）：**
```
Dark gradient background. Left side: a circular avatar frame with tech-anime hybrid border (circuit patterns meeting cherry blossom decorations). Center-right: "我是磊哥，我们下期见。" in friendly rounded font, white text. Below: three B-station interaction icons in a row - thumbs up (点赞), coin (投币), star (收藏) - each in a glowing circle with their Chinese labels. The icons have a playful bounce-ready pose. Small text at bottom: "GitHub 链接见评论区" with a link icon. Clean, warm, inviting end screen. 16:9, 1920x1080.
```

---

## 制作流程指南

### 工具链推荐

| 环节 | 推荐工具 | 用途 |
|------|----------|------|
| AI 生图 | Gemini Image Gen / FLUX / Grok Image | 生成分镜静态图 |
| 图生视频 | Kling 3.0 / Seedance 2.0 / Veo 3 | 静态图变 6 秒视频片段 |
| 屏幕录制 | OBS Studio | 录制实操演示 |
| 视频剪辑 | 剪映专业版 / DaVinci Resolve | 拼接、转场、字幕 |
| 文字动画 | 剪映 / After Effects | 金句字幕、图标动画 |
| 配音 | 真人口播 / Edge TTS | 语音轨道 |
| BGM | 剪映素材库 / Suno AI | 背景音乐 |

### 制作步骤

1. **生成所有 AI 静态图**（约 20 张）：用上面的提示词逐一生成
2. **图生视频**：标注了 [AI图→视频] 的镜头，用图生视频工具生成 6 秒片段（约 10 个）
3. **录制实操演示**：场次 6 的终端操作和对话演示
4. **录制/生成口播音频**：按文案录制语音
5. **剪辑拼接**：按分镜时间线拼接所有素材
6. **添加文字动画**：金句字幕、技术标注、图标动效
7. **添加转场**：科技↔二次元切换时用"蒸馏液体流动"转场
8. **配 BGM + 音效**：按段落情绪切换背景音乐
9. **最终调色**：科技段偏冷色，角色段偏暖色，保持整体统一

### BGM 建议
- Hook 段（0:00-0:30）：节奏感强的电子/Lo-fi
- 问题共鸣（0:30-1:15）：低沉压抑，配合"门槛高"的挫败感
- 解决方案登场（1:15-2:15）：转明亮，"柳暗花明"的释放感
- 核心卖点（2:15-3:30）：稳定有力，信息传递节奏
- 技术快闪（3:30-4:15）：快节奏电子，配合快速切换
- 实操演示（4:15-5:30）：轻快背景音，不抢注意力
- 收尾（5:30-6:30）：温暖钢琴/吉他，收束情绪

### 字幕风格
- 金句：大号白色/黄色字幕居中，发光描边
- 技术术语：首次出现时右下角小字注释
- 对比段落：左右分屏用不同颜色
- 卖点标题：带图标的彩色标签

### 素材清单
1. AI 生成静态图 × 约 20 张
2. AI 图生视频片段 × 约 10 个（各 6 秒）
3. Chub.ai 网站录屏
4. 终端蒸馏命令录屏
5. Claude Code 角色对话录屏
6. 蒸馏器 Logo（需设计或 AI 生成）
7. 各平台 Logo 素材
8. HUD 装饰框（透明 PNG）
9. 状态面板叠加素材（透明 PNG）

# 11 - 设计风格指南

> 了解不同的视觉设计风格，让你的设计更有针对性。

---

## 主流网页设计风格

### 1. 现代简约 (Modern Minimalist)

**特点**：
- 大量留白
- 内容为王
- 有限的色彩
- 清晰的排版
- 去除装饰元素

**适用场景**：
- SaaS 产品
- 科技公司官网
- 作品集网站

**关键元素**：
- 单色或双色配色
- 大量留白（负空间）
- 无衬线字体
- 简单的几何形状

**Prompt 关键词**：
```
"现代简约风格"
"大量留白"
"内容优先"
"极简主义"
"干净利落的排版"
```

**参考网站**：
- [Apple](https://www.apple.com) — 产品页面是极简主义的典范
- [Linear](https://linear.app) — SaaS 产品的现代简约风格
- [Notion](https://www.notion.so) — 简洁的功能性设计
- [Dropbox](https://www.dropbox.com) — 大量留白，内容为王

---

### 2. 杂志/编辑风格 (Magazine/Editorial)

**特点**：
- 大标题、大图片
- 不对称布局
- 强烈的视觉层次
- 衬线字体与无衬线字体混用
- 留白与密集内容对比

**适用场景**：
- 时尚杂志网站
- 博客、新闻网站
- 品牌故事页面

**关键元素**：
- 全屏大图
- 大号衬线标题
- 多列排版
- 图片与文字穿插
- 精致的细节处理

**Prompt 关键词**：
```
"杂志编辑风格"
"大标题大图片"
"不对称布局"
"衬线字体标题"
"时尚杂志感"
"图文混排"
"强烈的视觉层次"
```

**参考网站**：
- [The New York Times](https://www.nytimes.com) — 经典的新闻编辑风格
- [Vogue](https://www.vogue.com) — 时尚杂志的数字化呈现
- [Medium](https://medium.com) — 博客平台的编辑风格
- [Kinfolk](https://www.kinfolk.com) — 生活方式杂志的优雅排版

---

### 3. 野兽派/粗野主义 (Brutalism)

**特点**：
- 原始、未加工的外观
- 高对比度配色
- 系统默认字体
- 暴露的网格和结构
- 打破常规布局

**适用场景**：
- 创意机构
- 艺术项目
- 个人实验性网站
- 潮流品牌

**关键元素**：
- 纯黑边框
- 荧光色或高饱和色
- 系统默认字体（如 Times New Roman）
- 未修饰的图片
- 滚动字幕、闪烁元素

**Prompt 关键词**：
```
"野兽派风格"
"粗野主义设计"
"高对比度"
"原始未加工"
"系统默认字体"
"暴露的网格结构"
"打破常规布局"
"荧光色强调"
```

**参考网站**：
- [Bloomberg](https://www.bloomberg.com) — 数据密集的粗野主义风格
- [Dezeen](https://www.dezeen.com) — 建筑网站的大胆排版
- [Awwwards - Brutalism](https://www.awwwards.com/websites/?text=brutalist) — 野兽派网站合集
- [Gumroad](https://gumroad.com) — 简洁直接的粗野主义元素

---

### 4. 玻璃拟态 (Glassmorphism)

**特点**：
- 半透明背景
- 背景模糊效果
- 微妙的边框
- 层次感强

**适用场景**：
- 仪表盘
- 卡片式界面
- 浮层面板
- 现代应用

**关键元素**：
- `backdrop-filter: blur()`
- 半透明颜色（rgba）
- 1px 白色边框
- 柔和阴影

**Prompt 关键词**：
```
"玻璃拟态风格"
"半透明背景"
"背景模糊效果"
"毛玻璃质感"
"微妙的白色边框"
"层次感"
```

**参考网站**：
- [Apple macOS](https://www.apple.com/macos) — 控制中心的玻璃效果
- [Microsoft Fluent Design](https://www.microsoft.com/design/fluent/) — 亚克力材质设计
- [Dribbble - Glassmorphism](https://dribbble.com/search/glassmorphism) — 玻璃拟态设计合集

---

### 5. 新拟态 (Neumorphism / Soft UI)

**特点**：
- 柔和的阴影
- 浮雕效果
- 单色配色
- 触感反馈

**适用场景**：
- 音乐播放器
- 计算器
- 控制面板
- 拟物按钮

**关键元素**：
- 内外阴影组合
- 浅色背景
- 圆形元素
- 柔和过渡

**Prompt 关键词**：
```
"新拟态风格"
"柔和阴影"
"浮雕效果"
"Soft UI"
"单色配色"
"触感设计"
```

**参考网站**：
- [Dribbble - Neumorphism](https://dribbble.com/search/neumorphism) — 新拟态设计合集
- [CodePen - Soft UI](https://codepen.io/search/pens?q=neumorphism) — 代码实现示例

---

### 6. 暗黑模式 (Dark Mode)

**特点**：
- 深色背景（#121212 或 #1a1a1a）
- 浅色文字
- 降低亮度的高亮色
- 减少眼睛疲劳

**适用场景**：
- 开发工具
- 媒体消费应用
- 夜间使用场景
- OLED 屏幕优化

**关键元素**：
- 深灰背景（非纯黑）
- 降低饱和度的强调色
- 层次通过亮度区分
- 避免纯白文字（用 #e0e0e0）

**Prompt 关键词**：
```
"暗黑模式"
"深色主题"
"深色背景浅色文字"
"降低饱和度的强调色"
"夜间模式"
```

**参考网站**：
- [GitHub](https://github.com) — 经典的暗黑模式实现
- [Vercel](https://vercel.com) — 优雅的深色主题
- [Linear](https://linear.app) — 专业工具的暗黑模式
- [Discord](https://discord.com) — 游戏社区的深色界面

---

### 7. 复古/怀旧风格 (Retro/Vintage)

**特点**：
- 复古配色（米色、棕色、橄榄绿）
- 衬线字体
- 纹理背景
- 装饰性元素

**子风格**：
- **80年代**：霓虹色、几何图形、故障艺术
- **90年代**：像素风、鲜艳色彩、涂鸦元素
- **70年代**：大地色系、迷幻图案、衬线字体

**Prompt 关键词**：
```
"复古风格"
"怀旧设计"
"80年代霓虹风格"
"90年代像素风"
"复古配色"
"纹理背景"
```

**参考网站**：
- [Poolside FM](https://poolside.fm) — 80年代复古音乐播放器
- [Neocities](https://neocities.org) — 90年代网页风格的现代演绎
- [Internet Archive](https://archive.org) — 复古的图书馆感设计
- [The Outline](https://theoutline.com) — 独特的复古编辑风格（已关闭，但可参考存档）

---

### 8. 赛博朋克 (Cyberpunk)

**特点**：
- 霓虹色（青色、洋红、紫色）
- 黑色背景
- 科技感元素
- 故障艺术效果
- 网格、线条装饰

**适用场景**：
- 游戏网站
- 科技品牌
- 音乐/艺术项目

**Prompt 关键词**：
```
"赛博朋克风格"
"霓虹配色"
"科技感"
"故障艺术"
"网格装饰"
"青色洋红紫色"
```

**参考网站**：
- [Cyberpunk 2077](https://www.cyberpunk.net) — 游戏官网的赛博朋克美学
- [Devil May Cry 5](https://www.devilmaycry5.com) — 游戏网站的大胆视觉
- [Awwwards - Cyberpunk](https://www.awwwards.com/websites/?text=cyberpunk) — 赛博朋克风格网站合集

---

### 9. 有机/自然风格 (Organic/Natural)

**特点**：
- 大地色系
- 有机形状（非几何）
- 自然纹理
- 手写字体
- 植物元素

**适用场景**：
- 环保品牌
- 健康/养生
- 有机产品
- 生活方式品牌

**Prompt 关键词**：
```
"有机自然风格"
"大地色系"
"有机形状"
"自然纹理"
"手写字体"
"植物元素"
```

**参考网站**：
- [Patagonia](https://www.patagonia.com) — 环保品牌的自然风格
- [Aesop](https://www.aesop.com) — 护肤品牌的有机美学
- [Allbirds](https://www.allbirds.com) — 可持续鞋品牌的自然风格
- [Oatly](https://www.oatly.com) — 植物奶品牌的活泼自然风

---

### 10. 瑞士/国际主义风格 (Swiss/International Style)

**特点**：
- 网格系统
- 无衬线字体（Helvetica）
- 不对称布局
- 客观、功能性
- 摄影优先于插画

**适用场景**：
- 画廊、博物馆
- 建筑事务所
- 高端品牌

**Prompt 关键词**：
```
"瑞士风格"
"国际主义设计"
"网格系统"
"Helvetica 字体"
"不对称布局"
"功能性设计"
```

**参考网站**：
- [Swiss Style Design](https://swiss-style-design.com) — 瑞士风格展示网站
- [Helvetica Film](https://www.hustwit.com/helvetica) — 关于 Helvetica 的纪录片网站
- [MoMA](https://www.moma.org) — 现代艺术博物馆的经典排版
- [Tate](https://www.tate.org.uk) — 美术馆的瑞士风格设计

---

### 11. 孟菲斯风格 (Memphis Design)

**特点**：
- 鲜艳的几何图案
- 大胆的色彩组合
- 圆形、三角形、波浪线
- 80年代末90年代初的审美

**适用场景**：
- 创意项目
- 儿童产品
- 时尚品牌
- 艺术展览

**Prompt 关键词**：
```
"孟菲斯风格"
"鲜艳几何图案"
"大胆色彩"
"80年代美学"
"圆形三角形波浪线"
"活泼有趣"
```

**参考网站**：
- [Spotify Wrapped](https://www.spotify.com/wrapped) — 每年的孟菲斯风格设计
- [Dribbble - Memphis](https://dribbble.com/search/memphis) — 孟菲斯风格设计合集
- [Camper](https://www.camper.com) — 鞋品牌的活泼孟菲斯元素

---

### 12. 日式极简 (Japanese Minimalism)

**特点**：
- 大量留白（"间" Ma）
- 自然材料质感
- 手写风格字体
- 不对称平衡
- 季节性元素

**适用场景**：
- 生活方式品牌
- 茶文化
- 手工艺品牌
- 日本料理

**Prompt 关键词**：
```
"日式极简"
"大量留白"
"自然质感"
"不对称平衡"
"手写风格"
"禅意设计"
```

**参考网站**：
- [Muji](https://www.muji.com) — 无印良品的极简美学
- [Uniqlo](https://www.uniqlo.com) — 优衣库的日式简洁
- [Nendo](https://www.nendo.jp) — 日本设计工作室的极简作品
- [Issey Miyake](https://www.isseymiyake.com) — 三宅一生的品牌网站

---

## 风格选择指南

### 根据行业选择

| 行业 | 推荐风格 |
|------|---------|
| 科技/SaaS | 现代简约、玻璃拟态 |
| 时尚/杂志 | 杂志编辑风格、瑞士风格 |
| 创意/艺术 | 野兽派、孟菲斯、赛博朋克 |
| 金融/法律 | 现代简约、瑞士风格 |
| 健康/环保 | 有机自然风格、日式极简 |
| 游戏/娱乐 | 赛博朋克、暗黑模式、复古 |
| 儿童/教育 | 孟菲斯、活泼现代 |

### 根据品牌个性选择

| 品牌个性 | 推荐风格 |
|---------|---------|
| 专业可信 | 现代简约、瑞士风格 |
| 创新前卫 | 野兽派、赛博朋克 |
| 温暖友好 | 有机自然、日式极简 |
| 高端奢华 | 杂志编辑、暗黑模式 |
| 年轻活泼 | 孟菲斯、玻璃拟态 |
| 复古怀旧 | 复古风格、新拟态 |

---

## 混合风格

现代设计常常混合多种风格：

**示例组合**：
- 现代简约 + 暗黑模式（Notion）
- 杂志编辑 + 瑞士风格（The New York Times）
- 玻璃拟态 + 暗黑模式（Apple 控制中心）
- 野兽派 + 现代简约（平衡版野兽派）

**Prompt 关键词**：
```
"现代简约风格，融入杂志编辑元素"
"暗黑模式，玻璃拟态卡片"
"瑞士网格系统，杂志级排版"
```

---

## 风格趋势

### 2024-2025 趋势

1. **Bento 网格** — 苹果推广的多格布局
2. **3D 元素** — 轻量级 3D 图标和插图
3. **动态排版** — 可变字体、滚动动画
4. **AI 生成艺术** — 独特、不可复制的视觉
5. **可持续设计** — 环保主题、自然元素

---

## 下一步

→ 回到 [07-AI Prompt 设计技巧](07-ai-prompts.md) 应用这些风格

→ 查看 [08-常用设计术语速查](08-glossary.md) 了解更多术语

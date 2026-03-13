# 06 - 响应式设计

> 让你的设计在任何设备上都好看好用。

---

## 为什么需要响应式设计？

### 设备多样性

| 设备 | 屏幕宽度 | 使用场景 |
|------|---------|---------|
| 手机 | 320-414px | 随时随地，碎片化 |
| 平板 | 600-1024px | 沙发、床上，半专注 |
| 笔记本 | 1024-1440px | 办公、学习 |
| 桌面 | 1440px+ | 专业工作、多任务 |

### 响应式 vs 自适应

| 响应式 (Responsive) | 自适应 (Adaptive) |
|-------------------|------------------|
| 一套代码，灵活适配 | 多套固定布局 |
| 使用百分比、弹性布局 | 使用固定断点 |
| 更灵活 | 更可控 |
| 推荐方式 | 特定场景使用 |

---

## 断点 (Breakpoints)

### 常见断点设置

```css
/* 手机 */
@media (max-width: 639px) { }

/* 平板 */
@media (min-width: 640px) and (max-width: 1023px) { }

/* 桌面 */
@media (min-width: 1024px) and (max-width: 1279px) { }

/* 大屏 */
@media (min-width: 1280px) { }
```

### 简化版断点（推荐）

```css
/* 手机优先 */
/* 基础样式：手机 */

/* 平板 */
@media (min-width: 640px) { }

/* 桌面 */
@media (min-width: 1024px) { }
```

---

## 响应式策略

### 1. 移动优先 (Mobile First) ⭐ 推荐

**思路**：先设计手机版，再适配大屏

**优点**：
- 内容优先，去除冗余
- 性能更好（小屏加载更少资源）
- 符合用户增长趋势

**代码方式**：
```css
/* 基础：手机 */
.container {
  padding: 16px;
}

/* 平板 */
@media (min-width: 640px) {
  .container {
    padding: 24px;
  }
}

/* 桌面 */
@media (min-width: 1024px) {
  .container {
    padding: 32px;
    max-width: 1200px;
    margin: 0 auto;
  }
}
```

---

### 2. 桌面优先 (Desktop First)

**思路**：先设计桌面版，再适配小屏

**适用场景**：
- 复杂工具类应用
- 数据密集型界面
- 已有桌面版需要适配移动端

**代码方式**：
```css
/* 基础：桌面 */
.container {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
}

/* 平板 */
@media (max-width: 1023px) {
  .container {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* 手机 */
@media (max-width: 639px) {
  .container {
    grid-template-columns: 1fr;
  }
}
```

---

## 布局适配技巧

### 1. 弹性布局 (Flexbox)

**适用**：导航、按钮组、卡片排列

```css
.container {
  display: flex;
  flex-wrap: wrap;
  gap: 16px;
}

.item {
  flex: 1 1 300px; /* 可伸缩，基础宽度 300px */
}
```

---

### 2. 网格布局 (Grid)

**适用**：复杂页面布局、卡片网格

```css
/* 手机：单列 */
.grid {
  display: grid;
  gap: 16px;
}

/* 平板：两列 */
@media (min-width: 640px) {
  .grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* 桌面：四列 */
@media (min-width: 1024px) {
  .grid {
    grid-template-columns: repeat(4, 1fr);
  }
}
```

---

### 3. 流式布局 (Fluid)

**适用**：文字内容、图片

```css
.container {
  width: 100%;
  max-width: 1200px; /* 限制最大宽度 */
  margin: 0 auto;
}

img {
  max-width: 100%;
  height: auto;
}
```

---

### 4. 隐藏/显示

**适用**：小屏隐藏次要内容

```css
/* 手机隐藏侧边栏 */
.sidebar {
  display: none;
}

@media (min-width: 1024px) {
  .sidebar {
    display: block;
  }
}

/* 手机显示汉堡菜单 */
.mobile-menu {
  display: block;
}

@media (min-width: 1024px) {
  .mobile-menu {
    display: none;
  }
}
```

---

### 5. 堆叠布局

**适用**：表单、列表

```css
/* 手机：垂直堆叠 */
.form-row {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

/* 桌面：水平排列 */
@media (min-width: 640px) {
  .form-row {
    flex-direction: row;
  }
}
```

---

## 响应式排版

### 字体大小

```css
/* 手机 */
h1 { font-size: 28px; }
h2 { font-size: 24px; }
body { font-size: 16px; }

/* 平板 */
@media (min-width: 640px) {
  h1 { font-size: 32px; }
  h2 { font-size: 28px; }
}

/* 桌面 */
@media (min-width: 1024px) {
  h1 { font-size: 40px; }
  h2 { font-size: 32px; }
}
```

### 流式字体（现代方式）

```css
h1 {
  font-size: clamp(28px, 5vw, 48px);
  /* 最小 28px，理想 5vw，最大 48px */
}
```

---

## 响应式间距

### 间距系统

| 设备 | 小间距 | 中间距 | 大间距 |
|------|--------|--------|--------|
| 手机 | 8px | 16px | 24px |
| 平板 | 12px | 20px | 32px |
| 桌面 | 16px | 24px | 48px |

### 代码示例

```css
.section {
  padding: 24px 16px; /* 手机 */
}

@media (min-width: 640px) {
  .section {
    padding: 32px 24px; /* 平板 */
  }
}

@media (min-width: 1024px) {
  .section {
    padding: 48px 32px; /* 桌面 */
  }
}
```

---

## 响应式图片

### 方式 1：CSS 控制

```css
img {
  max-width: 100%;
  height: auto;
}
```

### 方式 2：HTML srcset

```html
<img 
  srcset="small.jpg 480w,
          medium.jpg 800w,
          large.jpg 1200w"
  sizes="(max-width: 600px) 480px,
         (max-width: 1000px) 800px,
         1200px"
  src="large.jpg"
  alt="描述"
>
```

---

## Prompt 关键词

```
"响应式设计，适配手机和平板"
"移动优先的设计"
"小屏时垂直堆叠布局"
"大屏时多列并排显示"
"断点设置：手机 <640px，平板 640-1024px，桌面 >1024px"
"弹性网格布局"
"图片自适应容器"
"字体大小随屏幕调整"
```

---

## 响应式设计检查清单

- [ ] 手机端内容清晰可读
- [ ] 触摸目标至少 44x44px
- [ ] 图片自适应不溢出
- [ ] 表格在小屏可横向滚动
- [ ] 导航在小屏可访问
- [ ] 字体大小合适（手机不小于 16px）
- [ ] 间距舒适不拥挤
- [ ] 测试真实设备

---

## 下一步

→ 学习 [07-AI Prompt 设计技巧](07-ai-prompts.md)

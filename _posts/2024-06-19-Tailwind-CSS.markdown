---
layout: post
title:  "Tailwind CSS"
---

## 1. peer:
**peer 是一个 Tailwind CSS 的特殊用法，用来实现兄弟选择器样式**
peer 类被添加到 `<input>` 元素，标记它为同伴元素。
`peer-focus` 类用于 `<label>` 元素，表示当同伴（input 元素）获得焦点时，`label` 的样式变化。具体来说，当 `input` 获得焦点时，`label` 的文字颜色会从 `text-dark-subtle` 变为 `text-white`。

```html
<input type="text" className='bg-transparent border-2 border-dark-subtle rounded w-full
  text-lg outline-none focus:border-white p-1 text-white peer transition'
  placeholder='youremail@gmail.com'
  id='email'/>
<label className='font-semibold text-dark-subtle peer-focus:text-white transition
  self-start' htmlFor="email">
  Email
</label>
```

## 2. Dark Mode
- `Tailwind CSS` 的暗模式 是通过在根元素上添加 dark 类实现的。

- 只要在 `tailwind.config.js` 文件中启用了暗模式支持，开发者就可以在 CSS 类中使用 `dark:` 前缀。

- 当 HTML 或某个局部容器有 dark 类时，所有带有 `dark:` 前缀的样式会生效，从而实现不同的外观设计（如颜色、背景色等）。

```html
<div class="text-black dark:text-white">
  当暗模式开启时，文本颜色变为白色
</div>
```

# 配置
```javascript
// tailwind.config.js
module.exports = {
  darkMode: 'class', // 启用通过类控制的暗模式
  theme: {
    extend: {},
  },
}
```

```javascript
<button onclick="toggleDarkMode()">切换主题</button>

<script>
  function toggleDarkMode() {
    document.documentElement.classList.toggle('dark'); // 切换 dark 类
  }
</script>
```

`toggle('dark')` 会检查 `<html>` 元素的类列表中是否已经包含 dark 类。

如果 `<html>` 元素中已有 dark 类，则 `toggle()` 会移除该类。

如果 `<html>` 元素中没有 dark 类，则 `toggle()` 会添加该类。

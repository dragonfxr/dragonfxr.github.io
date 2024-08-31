---
layout: post
title:  "Tailwind CSS"
---

# 1. peer:
**peer 是一个 Tailwind CSS 的特殊用法，用来实现兄弟选择器样式**
peer 类被添加到 `<input>` 元素，标记它为同伴元素。
`peer-focus` 类用于 `<label>` 元素，表示当同伴（input 元素）获得焦点时，`label` 的样式变化。具体来说，当 `input` 获得焦点时，`label` 的文字颜色会从 `text-dark-subtle` 变为 `text-white`。

```html
<input type="text" className='bg-transparent border-2 border-dark-subtle rounded w-full
  text-lg outline-none focus:border-white p-1 text-white peer transition'
  placeholder='youremail@gmail.com'
  id='email'/>
<label className='font-semibold text-dark-subtle peer-focus:text-white transition
  self-start' htmlFor="email">Email
</label>
```
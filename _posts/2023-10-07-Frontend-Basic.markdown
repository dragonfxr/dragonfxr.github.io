---
layout: post
title:  "Frontend Basic"
# date:   2023-10-07 03:00:55 +1100
# categories: jekyll update
---

**1. mailto in anchor tag**

`<a href={"mailto:rfeng422@gmail.com"} className='p-text'>rfeng422@gmail.com</a>`

mailto: 是一个 URI（统一资源标识符）方案，它用于创建电子邮件链接。当用户点击一个带有 mailto: 的链接时，它会尝试打开用户的默认邮件客户端，并创建一封新的电子邮件，其中收件人地址已预填为 mailto: 后面的电子邮件地址。 

**2. react引入包是否需要大括号**

`import React, { useState } from 'react';`

在 React 库中，useState 是一个具名导出，而 React 是一个默认导出。因此，你需要使用大括号来导入 useState，但不需要为 React 这样做。

**3. box-shadow（CSS hover）**

box-shadow: 这是一个 CSS 属性，用于给元素添加阴影效果。

```css
&:hover{
    box-shadow: 0 0 25px #fef4f5;
}
```

**&:** 这是一个常用于预处理器（如 Sass 或 Less）的符号。它代表当前选择器的引用。在 CSS 预处理器中，& 符号可以用来减少代码的重复并使结构更加清晰。在纯 CSS 中，这个符号没有特定的意义。

**:hover:** 这是一个伪类选择器，用于选择鼠标悬停在其上的元素。

**0:** 这是阴影的水平偏移量，值为 0 意味着阴影不会水平偏移。
**0:** 这是阴影的垂直偏移量，值为 0 意味着阴影不会垂直偏移。
**25px:** 这是阴影的模糊半径，意味着阴影的边缘将模糊扩散25像素。
---
author: Hugo Authors
title: 数学输入设置
date: 2019-03-08
description: 一个配置 KaTex 的简要教程
math: true
---

Hugo 项目中的数学符号可以通过第三方 JS 库来启用。
<!--more-->

在这个示例中，我们将会使用 [KaTeX](https://katex.org/)

- 新建一个组件 `/layouts/partials/math.html`
- 在这个组件中引用 [Auto-render Extension](https://katex.org/docs/autorender.html) 或者在本地保存相关文件.
- 在你的模板中这样使用你的组件:

```bash
{{ if or .Params.math .Site.Params.math }}
{{ partial "math.html" . }}
{{ end }}
```

- 全局开启 KaTex 可以在项目的配置文件中将 `math` 设置为 `true`。
- 单页开启 KaTex 可以在页面参数中加入 `math:true`

**提醒：** 请参考在线文档[Supported TeX Functions](https://katex.org/docs/supported.html)。

{{< math.inline >}}
{{ if or .Page.Params.math .Site.Params.math }}
<!-- KaTeX -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/katex.min.css" integrity="sha384-zB1R0rpPzHqg7Kpt0Aljp8JPLqbXI3bhnPWROx27a9N0Ll6ZP/+DiW/UqRcLbRjq" crossorigin="anonymous">
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/katex.min.js" integrity="sha384-y23I5Q6l+B6vatafAwxRu/0oK/79VlbSz7Q9aiSZUvyWYIYsd+qj+o24G5ZU2zJz" crossorigin="anonymous"></script>
<script defer src="https://cdn.jsdelivr.net/npm/katex@0.11.1/dist/contrib/auto-render.min.js" integrity="sha384-kWPLUVMOks5AQFrykwIup5lo0m3iMkkHrD0uJ4H5cjeGihAutqP0yW0J6dpFiVkI" crossorigin="anonymous" onload="renderMathInElement(document.body);"></script>
{{ end }}
{{</ math.inline >}}

### 例子

{{< math.inline >}}
<p>
行内公式： \(\varphi = \dfrac{1+\sqrt5}{2}= 1.6180339887…\)
</p>
{{</ math.inline >}}

区块公式:
$$
 \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } }
$$

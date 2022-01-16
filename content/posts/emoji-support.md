+++
author = "Hugo Authors"
title = "Emoji 支持"
date = "2019-03-05"
description = "在 Hugo 中使用 Emoji 的教程"
tags = [
    "emoji",
]
+++

在 Hugo 项目中，有若干种启用 Emoji 的方法。
<!--more-->

[`Emojify`](https://gohugo.io/functions/emojify/) 功能可以用模板来直接调用，或者通过 [Inline Shortcodes](https://gohugo.io/templates/shortcode-templates/#inline-shortcodes) 来引用。

如果要全局开启 Emoji，你需要在网站的 [配置文件](https://gohugo.io/getting-started/configuration/) 中将 `enableEmoji` 设置为 `true`，然后就可以在文件中直接输入 emoji 的编码了。如：

<p><span class="nowrap"><span class="emojify">🙈</span> <code>:see_no_evil:</code></span>  <span class="nowrap"><span class="emojify">🙉</span> <code>:hear_no_evil:</code></span>  <span class="nowrap"><span class="emojify">🙊</span> <code>:speak_no_evil:</code></span></p>

[Emoji cheat sheet](http://www.emoji-cheat-sheet.com/) 是一个有用的 emoji 编码网站。

----

**注意：** 上面的步骤可以在 Hugo 中开启 Unicode Standard emoji 字符和段落，但是字形的渲染取决于浏览器和平台。为了美化 emoji，你可以用第三方 emoji 字体或者 font stack。如：


{{< highlight html >}}
.emoji {
  font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
}
{{< /highlight >}}

{{< css.inline >}}
<style>
.emojify {
	font-family: Apple Color Emoji, Segoe UI Emoji, NotoColorEmoji, Segoe UI Symbol, Android Emoji, EmojiSymbols;
	font-size: 2rem;
	vertical-align: middle;
}
@media screen and (max-width:650px) {
  .nowrap {
    display: block;
    margin: 25px 0;
  }
}
</style>
{{< /css.inline >}}

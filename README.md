# hexo-plugin-biblezh

一个可能对基督徒有帮助的 Hexo 插件（WIP）

## Tag

（将）会提供以下标签：

```
{% bible [篇目名称] [章:节] %}

例如
{% bible 马太福音 9:13 %}
{% bible 约一 3:16 %}
{% bible Gen 1:1 %}
{% bible 1 Corinthians 13:1 %}
```

这些标签，在网站生成时（即运行 `hexo g` 的时候）会由插件从 BibleGateway 获取对应的经文填入网站中。

同时会提供以下标签：

```
{% bibleq [篇目名称] [章:节] %}
[摘抄的内容]
{% endbibleq %}

例如
{% bibleq Gen 1:1 %}
起初
{% endbibleq %}
```

在生成时会保留输入的文字，并自动生成一个指向这一节经文的链接。

## 页面

在生成的网页上注入一个读经工具，可以

- 切换译本（仅针对使用 `biblezh` 标签引入的经文）（使用 [api.bible](api.bible) API）
- 转到圣经阅读器阅读上下文（计划支持：YouVersion、BibleGateway、微读、主内）

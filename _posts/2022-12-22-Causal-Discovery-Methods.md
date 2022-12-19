---
layout: post
title: "Causal Discovery Methods"
categories:
 - Causal inference
tags: [Causal discovery, Causal algorithm]
---

Here summarize some major causal discovery methods, including their Python codes.

Coming sonn...I am working on it.

<!--more-->

## Non-continues optimization based approches

| No. | Method | Year | Paper | GitHub | Type | Sufficiency | Faithfulness | Acyclicity | Output | 
| --- | --- | --- | --- | --- | --- | --- |--- | --- |--- |
| [1] | PC | 1993 | [PDF](https://www.researchgate.net/publication/242448131_Causation_Prediction_and_Search){:target="_blank"} | [Python](https://github.com/keiichishima/pcalg){:target="_blank"} | contraint | Yes | Yes | No | CPDAG |
| --- | --- | --- | --- |--- | --- | --- | --- | --- |--- |
| --- | --- | --- | --- |--- | --- | --- | --- | --- |--- |

### Citation
> [1] [P. Spirtes, C. Glymour, and R. Scheines. 2000. Causation, prediction, and search (2nd ed.). MIT Press, Cambridge,
Massachusetts.](https://www.researchgate.net/publication/242448131_Causation_Prediction_and_Search){:target="_blank"}

### Reference
[Causal Discovery by Shawhin Talebi](https://towardsdatascience.com/causal-discovery-6858f9af6dcb){:target="_blank"}

<!--
One of the rewards of switching my website to [Jekyll](http://jekyllrb.com/) is the
ability to support **MathJax**, which means I can write LaTeX-like equations that get
nicely displayed in a web browser, like this one \\( \sqrt{\frac{n!}{k!(n-k)!}} \\) or
this one \\( x^2 + y^2 = r^2 \\).

[//]: # (哈哈我是注释，不会在浏览器中显示。)
[//]: ``` shift+@

![插入一张本地图片](/assets/images/XXXXXX.png)

## heading line

[MarkDown 中使用 LaTeX 数学式](https://www.cnblogs.com/nowgood/p/latexstart.html){:target="_blank"}

file is: ```markdown: redcarpet```

<cite>cite</cite>.

## Table

| Table Header 1 | Table Header 2 | Table Header 3 |
| --- | --- | --- |
| Division 1 | Division 2 | Division 3 |
| Division 1 | Division 2 | Division 3 |
| Division 1 | Division 2 | Division 3 |

## Misc Stuff - abbr, acronym, sub, sup, etc.

Lorem <sup>superscript</sup> dolor <sub>subscript</sub> 


{% highlight r %}
$$a^2 + b^2 = c^2$$
{% endhighlight %}


{% highlight r %}
<script type="text/x-mathjax-config">
MathJax.Hub.Config({
  tex2jax: {
    inlineMath: [['$','$'], ['\\(','\\)']],
    processEscapes: true
  }
});
</script>
<script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
{% endhighlight %}

-->

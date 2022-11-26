---
layout: post
title: "MathJax with Jekyll"
categories:
 - Math
tags: [resources, jekyll]
---

One of the rewards of switching my website to [Jekyll](http://jekyllrb.com/){:target="_blank"} is the
ability to support **MathJax**, which means I can write LaTeX-like equations that get
nicely displayed in a web browser, like this one \\( \sqrt{\frac{n!}{k!(n-k)!}} \\) or
this one \\( x^2 + y^2 = r^2 \\).

<!--more-->

<img class="centered" src="https://www.mathjax.org/badge/mj-logo.svg" />

### What's MathJax?

If you check MathJax website [(www.mathjax.org)](http://www.mathjax.org/) you'll see
that it *is an open source JavaScript display engine for mathematics that works in all
browsers*.


### How to implement MathJax with Jekyll

I followed the instructions described by Dason Kurkiewicz for
[using Jekyll and Mathjax](http://dasonk.github.io/blog/2012/10/09/Using-Jekyll-and-Mathjax/){:target="_blank"}.

Here are some important details. I had to modify the Ruby library for Markdown in
my ```_config.yml``` file. Now I'm using redcarpet so the corresponding line in the
configuration file is: ```markdown: redcarpet```

To load the MathJax javascript, I added the following lines in my layout ```post.html```
(located in my folder ```_layouts```)

{% highlight r %}
<script type="text/javascript"
    src="http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>
{% endhighlight %}

Of course you can choose a different file location in your jekyll layouts. 

Note that by default, the **tex2jax** preprocessor defines the
LaTeX math delimiters, which are ```\\(...\\)``` for in-line math, and ```\\[...\\]``` for
displayed equations. It also defines the TeX delimiters ```$$...$$``` for displayed
equations, but it does not define ```$...$``` as in-line math delimiters. To enable in-line math delimiter with ```$...$```, please use the following configuration:

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


### A Couple of Examples

Here's a short list of examples. To know more about the details behind MathJax, you can
always checked the provided documentation available at
[http://docs.mathjax.org/en/latest/](http://docs.mathjax.org/en/latest/){:target="_blank"}

Let's try a first example. Here's a dummy equation:

$$a^2 + b^2 = c^2$$

How do you write such expression? Very simple: using **double dollar** signs

{% highlight r %}
$$a^2 + b^2 = c^2$$
{% endhighlight %}

To display inline math use ```\\( ... \\)``` like this ```\\( sin(x^2) \\)``` which gets
rendered as \\( sin(x^2) \\)


Here's another example using type ```\mathsf```

{% highlight r %}
$$ \mathsf{Data = PCs} \times \mathsf{Loadings} $$
{% endhighlight %}

which gets displayed as

$$ \mathsf{Data = PCs} \times \mathsf{Loadings} $$

Or even better:

{% highlight r %}
\\[ \mathbf{X} = \mathbf{Z} \mathbf{P^\mathsf{T}} \\]
{% endhighlight %}

is displayed as

\\[ \mathbf{X} = \mathbf{Z} \mathbf{P^\mathsf{T}} \\]

If you want to use subscripts like this \\( \mathbf{X}\_{n,p} \\) you need to scape the
underscores with a backslash like so ``` \mathbf{X}\_{n,p} ```:

{% highlight r %}
$$ \mathbf{X}\_{n,p} = \mathbf{A}\_{n,k} \mathbf{B}\_{k,p} $$
{% endhighlight %}

will be displayed as

\\[ \mathbf{X}\_{n,p} = \mathbf{A}\_{n,k} \mathbf{B}\_{k,p} \\]

## Multiline equotions.

### Method-1
$$ f(x)=\left\{
\begin{aligned}
x & = & \cos(t) \\
y & = & \sin(t) \\
z & = & \frac xy
\end{aligned}
\right.
$$

### Method-2
$$ F^{HLLC}=\left\{
\begin{array}{rcl}
F_L       &      & {0      <      S_L}\\
F^*_L     &      & {S_L \leq 0 < S_M}\\
F^*_R     &      & {S_M \leq 0 < S_R}\\
F_R       &      & {S_R \leq 0}
\end{array} \right. $$


### Method-3
$$f(x)=
\begin{cases}
0& \text{x=0}\\
1& \text{x!=0}
\end{cases}$$

If not work, try http://feigeek.com/posts/b1bbb984.html

### More useful examples. https://www.cnblogs.com/nowgood/p/latexstart.html

$$
\begin{array}
\overline{a+b+c} \\
\underline{a+b+c} \\
\overleftarrow{a+b} \\
\underleftarrow{a+b} \\
\underleftrightarrow{a+b} \\
\vec x = \vec{AB} \\
\overbrace {a+b}^\text{a,b} \\
a+\rlap{\overbrace{\phantom{b+c+d}}^m}b+\underbrace{c+d+e}_n+f
\end{array}
$$

$$
\begin{pmatrix}
a & b & c \\
d & e & f \\
g & h & i 
\end{pmatrix} 
$$

$$
\chi(\lambda) =  
\begin{vmatrix}
\lambda - a & -b & -c \\
-d & \lambda - e & -f \\
-g & -h & \lambda - i 
\end{vmatrix}
$$

$$
\begin{gather}
(a+b) \times c = a\times c + b \times c \notag \\
ac= a\times c \\
\end{gather}
$$

$$
\begin{align}
y &= \cos t + 1 \\
y &= 2sin t \\
\end{align}
$$

$$
\begin{align*}
 x &= t & x &= \cos t &  x &= t \\
 y &= 2t & y &= \sin (t+1) & y &= \sin t \\
\end{align*}
$$

$$
\begin{align*}
& (a+b)(a^2-ab+b^2) \\
= {}& a^3-a^2b+ab^2+a^2b-ab^2+b^2 \\
= {}& a^3 + b^3
\end{align*}
$$

$$
% 注意 \tag{...} 编号的位置
\begin{equation}
\begin{split}
\cos 2x &= \cos^2 x - \sin^2 x \\
        &= 2\cos^2 x - 1  
\end{split} \tag{3.1}
\end{equation}  
$$

$$
\begin{equation}\label{eq:trigonometric}
\begin{split}
\frac12 (\sin(x+y) + \sin(x-y))
  &= \frac12(\sin x\cos y + \cos x\sin y) \\
  & \quad + \frac12(\sin x\cos y - \cos x\sin y) \\
  &= \sin x\cos y
\end{split}
\end{equation}
$$

$$
\begin{equation}
D(x) = \begin{cases}
1, & \text{if } x \in \mathbb{Q}; \\
0, & \text{if } x \in
     \mathbb{R}\setminus\mathbb{Q}.
\end{cases}
\end{equation}
$$





---
layout: default
title:  "Help docs"
nav_order: 100
mathjax: true
---
# Help docs
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

### Helpful links

- <https://pmarsceill.github.io/just-the-docs/>
- <https://github.com/pmarsceill/just-the-docs/tree/master/docs>
- <https://pdmosses.github.io/test-nav/>
- <https://github.com/pdmosses/test-nav>

### Test markdown

##### C code

```c
void main(int argc, char const *argv[])
{
    /* code */
    return 0;
}
```

##### MathJax

$$
\begin{align}
  x + 3y + 4z &= 2 \\
      3y - 4z &= 5 \\
            z &= 4
\end{align}
$$

inline mathjax expression $$\sqrt{2}$$

$$
\begin{align*}
  & \phi(x,y) = \phi \left(\sum_{i=1}^n x_ie_i, \sum_{j=1}^n y_je_j \right)
  = \sum_{i=1}^n \sum_{j=1}^n x_i y_j \phi(e_i, e_j) = \\
  & (x_1, \ldots, x_n) \left( \begin{array}{ccc}
      \phi(e_1, e_1) & \cdots & \phi(e_1, e_n) \\
      \vdots & \ddots & \vdots \\
      \phi(e_n, e_1) & \cdots & \phi(e_n, e_n)
    \end{array} \right)
  \left( \begin{array}{c}
      y_1 \\
      \vdots \\
      y_n
    \end{array} \right)
\end{align*}
$$
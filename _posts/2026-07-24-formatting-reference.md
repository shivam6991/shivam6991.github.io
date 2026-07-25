---
layout: post
title: How to write a post (a living template)
date: 2026-07-24 10:00:00+0530
description: Markdown, LaTeX, code, and the scrolling sidebar — copy this file to start a new post.
tags: welcome code math
categories:
giscus_comments: false
related_posts: false
toc:
  sidebar: left
---

Everything on this page is written in **plain Markdown** — no HTML, no "code." The only
special part of a post is the little block at the very top (between the `---` lines),
called the *front matter*. Notice the sidebar on the left: it's built automatically from
the headings below, and the current section highlights (darkens) as you scroll. That comes
from these three lines in the front matter:

```yaml
toc:
  sidebar: left
```

Change `left` to `right` to move it, or delete those lines to turn it off. To start a new
post, just copy this file, rename it, and replace the content.

## The front matter

The block at the top sets the post's metadata. The important fields:

```yaml
---
layout: post
title: My post title
date: 2026-08-01 09:00:00+0530   # controls ordering; future dates stay hidden until then
description: a one-line summary shown in the blog list
tags: machine-learning embedded   # space-separated
toc:
  sidebar: left
---
```

Everything below the closing `---` is just the post body in Markdown.

## Text formatting

You can write **bold**, *italic*, `inline code`, and [links](https://jekyllrb.com).

> Blockquotes are great for highlighting a key idea or quoting a source.

- Bulleted lists
- work as you'd expect
  - and they nest
1. Numbered lists
2. do too

## Code

Fenced code blocks get syntax highlighting for whatever language you tag them with
(the ```` ```python ```` on the opening fence):

```python
def fib(n):
    a, b = 0, 1
    for _ in range(n):
        a, b = b, a + b
    return a
```

## Math with LaTeX

Math is written in **LaTeX** and rendered by MathJax. Surround an expression with `$$`.

### Inline and display

Inside a sentence it stays inline — like `$$E = mc^2$$` gives $$E = mc^2$$. Put it on its
own line and it becomes a centered display equation:

$$
\nabla_\theta J(\theta) = \mathbb{E}_{x \sim \mathcal{D}}\left[ \nabla_\theta \mathcal{L}(f_\theta(x), y) \right]
$$

### Numbered equations

Use an `equation` environment with a `\label{}` to get an automatically numbered equation
you can reference later with `\eqref{}`:

\begin{equation}
\label{eq:attention}
\mathrm{Attention}(Q, K, V) = \mathrm{softmax}\!\left(\frac{QK^\top}{\sqrt{d_k}}\right) V
\end{equation}

We can then point back to equation \eqref{eq:attention} from anywhere in the text.

## Tables

| Model    | Params | Accuracy |
| :------- | -----: | -------: |
| Baseline |   1.2M |    91.3% |
| Ours     |   0.8M |    93.7% |

## Publishing

Save the file in `_posts/` named `YYYY-MM-DD-title.md`, commit it, and push to `main`.
The site rebuilds and redeploys itself in a minute or two — nothing else to do.

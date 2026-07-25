---
layout: post
title: A quick formatting reference
date: 2026-07-24 10:00:00+0530
description: Code, math, tables, and callouts — the building blocks for posts.
tags: welcome code math
categories:
giscus_comments: false
related_posts: false
toc:
  beginning: true
---

Keep this post around as a cheat-sheet for the syntax you'll use most, then delete it
when you're comfortable.

## Text

You can write **bold**, *italic*, `inline code`, and [links](https://jekyllrb.com).

> Blockquotes are great for highlighting a key idea or quoting a source.

- Bulleted lists
- work as you'd expect
  - and they nest

1. Numbered lists
2. do too

## Code blocks

Fenced code blocks get syntax highlighting for the language you tag them with:

```python
def fib(n):
    a, b = 0, 1
    for _ in range(n):
        a, b = b, a + b
    return a
```

## Math

Inline math like $$E = mc^2$$ renders with MathJax, and so do display equations:

$$
\nabla_\theta J(\theta) = \mathbb{E}_{x \sim \mathcal{D}} \left[ \nabla_\theta \mathcal{L}(f_\theta(x), y) \right]
$$

## Tables

| Model      | Params | Accuracy |
| :--------- | -----: | -------: |
| Baseline   |   1.2M |    91.3% |
| Ours       |   0.8M |    93.7% |

## Table of contents

This post sets `toc: {beginning: true}` in its front matter, which adds the little table
of contents above from the `##` headings automatically.

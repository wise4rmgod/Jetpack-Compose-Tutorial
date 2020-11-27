# Syntax

Markdown 的目標是實現「易讀易寫」。

不過最需要強調的便是它的可讀性。一份使用Markdown格式撰寫的文件應該可以直接以純文字發佈，並且看起來不會像是由許多標籤或是格式指令所構成。


## Headers

## H2 {docsify-ignore}

### H3

#### H4

##### H5

###### H6

## Blockquotes

> 因為需要感謝的人太多了，就感謝天罷。

## Lists

- Lorem ipsum dolor sit amet
- Nulla volutpat aliquam velit
    - Phasellus iaculis neque
    - Purus sodales ultricies
- Faucibus porta lacus fringilla vel

---

1. Lorem ipsum dolor sit amet
2. Consectetur adipiscing elit
3. Integer molestie lorem at massa
4. Facilisis in pretium nisl aliquet

## Code and Syntax Highlighting

In this example, `<section></section>` should be wrapped as **code**.

```python
from collections import deque

def search(lines, pattern, history=5):
    previous_lines = deque(maxlen=history)
    for line in lines:
        if pattern in line:
            yield line, previous_lines
        previous_lines.append(line)
```

## Tables

| Option | Description |
| ------ | ----------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |


---

- Table of Contents
    - [Chapter 1](#chapter-1)
    - [Chapter 2](#chapter-2)
    - [Chapter 3](#chapter-3)

---

- [ ] foo
- [x] baz

---

:smile: :one: :white_check_mark:

![Stormtroopocat](http://octodex.github.com/images/stormtroopocat.jpg)

---

KaTeX

Logistic function: $f(x) = \frac{1}{1+e^{-x}}$

The 3n+1 problem

$$
f(n) = \begin{cases}
\frac{n}{2}, & \text{if } n\text{ is even} \cr
3n+1, & \text{if } n\text{ is odd}
\end{cases}
$$

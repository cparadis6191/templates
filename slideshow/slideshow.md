---
title: Slideshow
author: Chad Paradis
slideNumber: '`"h.v"`{=html}'
---

# Introduction

> * this is a slideshow built with Pandoc and reveal.js
> * it is simple
> * it is nice

## Markdown

It is Markdown and supports all the basic features you expect!

# Level-1 Heading

This is a slide with a level-1 heading!

## Level-2 Heading

This is a slide with a level-2 heading!

## Another Level-2 Heading

This is another slide with a level-2 heading!

# Overview Mode

Hit `<Esc>` and enjoy!

# Code Block

`const int foo = 5;` is an inline code block!

Here is a fenced code block:

```c
int foo(int bar) {
  return bar;
}
```

# Block Quote

> This is a block quote!

> This is a longer block quote
> that takes up two (two!) lines!

Run `pandoc --list-highlight-languages` to get a listed of supported languages for code blocks!

# ASCII Table

Have fun formatting this in Markdown!

| Animal | Fur | Best                          |
|:-------|----:|-------------------------------|
| Cat    | Yes | Amazing!                      |
| Dog    | Yes | Some of them are pretty good! |
| Snek   | Yes | ???                           |

# List

> * this is a list that can be stepped
> * and here is the second thing
>   * and here is a child of the second thing

## Numbered List

> 1. this is a numbered list that can be stepped
> 2. and here is the second thing
>    1. and here is a child of the second thing

# Inline TeX Math

Here is the Pythagorean theorem inline $\alpha^2 + \beta^2 = \theta^2$!

# TeX Math Block

Here is the Pythagorean theorem in a block:

$$
\theta^2 + \alpha^2 = \beta^2
$$

# Embedded Image

This is an embedded image with a caption!

![This is an embedded image caption!](https://static.wikia.nocookie.net/cnc_gamepedia_en/images/f/f0/TS_Tiberium_Refinery.png/revision/latest?cb=20180801164026){width=25%}

# <span style="color:white">Background Image</span> {background-image="https://static.wikia.nocookie.net/lotr/images/f/f3/Grond_arrives.png/revision/latest/scale-to-width-down/300?cb=20121127112154"}

<span style="color:white">This text is white!</span>

# Embedded Diagrams

## Graphviz

```{.dot}
//| label: fig-boring
//| fig-cap: "A boring Graphviz graph."
digraph boring {
  A -> B;
}
```

## PlantUML

```{.plantuml caption="This is an image, created by **PlantUML**." width=50%}
@startuml
Alice -> Bob: Authentication Request Bob --> Alice: Authentication Response
Alice -> Bob: Another authentication Request Alice <-- Bob: another Response
@enduml
```

# Fullscreen Mode

Hit `F` to use fullscreen mode!

# Speaker View

Hit `S` to use speaker view!

::: notes

These are notes that show up in speaker view!

List:

* one
* fish

:::

But the audience only sees this!

# Custom CSS

Check out [slideshow.css](slideshow.css)!

# References

> * [Pandoc User's Guide Slide shows](https://pandoc.org/MANUAL.html#slide-shows)
> * [reveal.js](https://revealjs.com/)

# Questions?

```
 ___
|__ \
  / /
 |_|
 (_)
```

[modeline]: # ( vim: set spell spelllang=en_us textwidth=100: )

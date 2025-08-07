+++
title = "Example Post"
date = "2025-08-06"
draft = true

[taxonomies]
tags=["Test"]

[extra]
repo_view = true
comment = true
read_time = true
+++
This is a test of the apaxq.net blog, this is only a test.

# H1

## H2

### H3

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Aliquet sagittis id consectetur purus ut. In pellentesque massa placerat duis ultricies. Neque laoreet suspendisse interdum consectetur libero id. Justo nec ultrices dui sapien eget mi proin. Nunc consequat interdum varius sit amet mattis vulputate. Sollicitudin tempor id eu nisl nunc mi ipsum. Non odio euismod lacinia at quis. Sit amet nisl suscipit adipiscing. Amet mattis vulputate enim nulla aliquet porttitor lacus luctus accumsan. Sit amet consectetur adipiscing elit pellentesque habitant. Ac placerat vestibulum lectus mauris. Molestie ac feugiat sed lectus vestibulum mattis ullamcorper velit sed. [Google](https://www.google.com)

![Markdown Logo](https://markdown-here.com/img/icon256.png)

## Code Block

```cpp
#include <iostream>

int main()
{
    std::cout << "Hello, world!\n";
}
```

```cpp,hl_lines=5,linenos
#include <iostream>

int main()
{
    std::cout << "Hello, world!\n";
}
```

## Ordered List

1. First item
2. Second item
3. Third item

## Unordered List

- List item
- Another item
- And another item

## Nested list

- Fruit
    - Apple
    - Orange
    - Banana
- Dairy
    - Milk
    - Cheese

## Quote

> Two things are infinite: the universe and human stupidity; and I'm not sure about the
> universe.<br>
> — <cite>Albert Einstein</cite>

## Table Inline Markdown

| Italics   | Bold     | Code   | StrikeThrough     |
| --------- | -------- | ------ | ----------------- |
| _italics_ | **bold** | `code` | ~~strikethrough~~ |

## Foldable Text

<details>
    <summary>Title 1</summary>
    <p>IT'S A SECRET TO EVERYBODY.</p>
</details>

<details>
    <summary>Title 2</summary>
    <p>Stay awhile, and listen!</p>
</details>

## Code tags

Lorem ipsum `dolor` sit amet, `consectetur adipiscing` elit.
`Lorem ipsum dolor sit amet, consectetur adipiscing elit.`

## Note

Here is an example of the `note` shortcode:

This one is static!
{{ note(header="Note!", body="This blog assumes basic terminal maturity") }}

This one is clickable!
{{ note(clickable=true, hidden = true, header="Quiz!", body="The answer to the quiz!") }}


Syntax:
```
{{/* note(header="Note!", body="This blog assumes basic terminal maturity") */}}
{{/* note(clickable=true, hidden = true, header="Quiz!", body="The answer to the quiz!") */}}
```

You can also use some HTML in the text:
{{ note(header="Note!", body="<h1>This blog assumes basic terminal maturity</h1>") }}


Literal shortcode:
```
{{/* note(header="Note!", body="<h1>This blog assumes basic terminal maturity</h1>") */}}
```

Pretty cool, right?

Finally, you can do something like this (hopefully):

{% note(clickable=true, header="Quiz!") %}

# Hello this is markdown inside a note shortcode

```rust
fn main() {
    println!("Hello World");
}
```

We can't call another shortcode inside a shortcode, but this is good enough.

{% end %}

Here is the raw markdown:

```markdown
{{/* note(clickable=true, header="Quiz!") */}}

# Hello this is markdown inside a note shortcode

\`\`\`rust
fn main() {
    println!("Hello World");
}
\`\`\`

We can't call another shortcode inside a shortcode, but this is good enough.

{{/* end */}}
```

Finally, we have center
{{ note(center=true, header="Centered Text", body="This is centered text") }}

```markdown
{{/* note(center=true, header="Centered Text", body="This is centered text") */}}
```
It works good enough for me!

## [Mermaid](https://mermaid.js.org/) markdown diagram rendering

{% mermaid() %}
graph LR
A[Start] --> B[Initialize]
B --> C[Processing]
C --> D[Complete]
D --> E[Success]

    style A fill:#f9f,stroke:#333
    style E fill:#9f9,stroke:#333
{% end %}

# Inline Math

- $(a+b)^2$ = $a^2 + 2ab + b^2$
- A polynomial P of degree d over $\mathbb{F}_p$ is an expression of the form
  $P(s) = a_0 + a_1 . s + a_2 . s^2 + ... + a_d . s^d$ for some
  $a_0,..,a_d \in \mathbb{F}_p$

# Displayed Math

$$
p := (\sum_{k∈I}{c_k.v_k} + \delta_v.t(x))·(\sum_{k∈I}{c_k.w_k} + \delta_w.t(x)) − (\sum_{k∈I}{c_k.y_k} + \delta_y.t(x))
$$
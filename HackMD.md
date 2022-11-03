---
tags: CSST
description: "CSST 2022: 使用 Markdown 和 LaTeX 成為筆記大師"
---

{%hackmd BkVfcTxlQ %}

# HackMD 額外功能

[![hackmd-github-sync-badge](https://hackmd.io/kvD8r4l1RP6WcT6CzlD27w/badge)](https://hackmd.io/kvD8r4l1RP6WcT6CzlD27w)

這裡是一些 HackMD 擴充的語法。

## Inline

HackMD 增加惹一些行內元素的支援。

### Sources

```markdown
Wrap words in ++two consecutive plus signs++ to ++underline++ them.

Wrap words in ==two consecutive equal signs== to ==highlight== them.

Wrap words in ^carets^ to make them ^superscript^.

Wrap words in ~tildes~ to make them ~subscript~.
```
### Results

Wrap words in ++two consecutive plus signs++ to ++underline++ them.

Wrap words in ==two consecutive equal signs== to ==highlight== them.

Wrap words in ^carets^ to make them ^superscript^.

Wrap words in ~tildes~ to make them ~subscript~.

## Quotes w/ additional attributions

引言區塊可以標註名字、時間，並自訂 border 的顏色。

### Sources

```markdown
> Can anybody find me somebody to love?
> 
> Each morning I get up I die a little \
> Can barely stand on my feet \
> Take a look in the mirror and cry \
> Lord, what you're doing to me? \
> I have spent all my years in believing you \
> But I just can't get no relief, Lord \
> Somebody, somebody \
> Can anybody find me somebody to love?
>
> ![A Day at the Races](https://i.imgur.com/flOmqfD.jpg "A Day at the Races" =200x200)
>
> [name=Queen][time=1976][color=#F2D0A7]
```

### Results

> Can anybody find me somebody to love?
> 
> Each morning I get up I die a little \
> Can barely stand on my feet \
> Take a look in the mirror and cry \
> Lord, what you're doing to me? \
> I have spent all my years in believing you \
> But I just can't get no relief, Lord \
> Somebody, somebody \
> Can anybody find me somebody to love?
>
> ![A Day at the Races](https://i.imgur.com/flOmqfD.jpg "A Day at the Races" =200x200)
>
> [name=Queen][time=1976][color=#F2D0A7]

## Definition list

可以對應到 HTML 的 `<dl>`, `<dt>` & `<dd>` tags 及 $\LaTeX$ 的 `description` environment.

### Sources

```markdown
Term A
: Definition a
: Definition b

Term B
: Definition
```

### Results

Term A
: Definition _a_
: Definition **b**

Term B
: Definition

## Blocks

HackMD 支援四種顏色 blocks（對應到 Bootstrap?）以及可折疊的 blocks.

### Sources

```markdown
:::success
This is a **success** block.
:::

:::info
This is a _info_ block.
:::

:::warning
This is a _**warning**_ block.
:::

:::danger
This is a `danger` block.
:::

:::spoiler
This is a ~~spoiler~~ block.
:::

:::spoiler Custom Caption
This is a ~~spoiler~~ w/ custom caption block.
:::
```

### Results

:::success
This is a **success** block.
:::

:::info
This is a _info_ block.
:::

:::warning
This is a _**warning**_ block.
:::

:::danger
This is a `danger` block.
:::

:::spoiler
This is a ~~spoiler~~ block.
:::

:::spoiler Custom Caption
This is a ~~spoiler~~ w/ custom caption block.
:::

## Include external contents

我們可以容易地在 HackMD 中嵌入一些外部內容。

### Sources

```markdown
:::spoiler YouTube
{%youtube fJ9rUzIMcZQ %}
:::

:::spoiler GitHub Gist
{%gist nevikw39/06f049e5fc01878d27bd381beb1880a8 %}
:::

:::spoiler PDF
{%pdf https://m110.nthu.edu.tw/~s110062219/ICPC/2022-Asia%20Taipei%202021-Mr.%20Chun-Mu%20Weng-MEDAL.pdf %}
:::

:::spoiler HackMD
{%hackmd @nevikw39/signature %}
:::
```

### Results

:::spoiler YouTube
{%youtube fJ9rUzIMcZQ %}
:::

:::spoiler GitHub Gist
{%gist nevikw39/06f049e5fc01878d27bd381beb1880a8 %}
:::

:::spoiler PDF
{%pdf https://m110.nthu.edu.tw/~s110062219/ICPC/2022-Asia%20Taipei%202021-Mr.%20Chun-Mu%20Weng-MEDAL.pdf %}
:::

:::spoiler HackMD
{%hackmd @nevikw39/signature %}
:::

## Graph & diagram

HackMD 還支援繪製一系列的圖表，比較通用的有 [Graphviz](https://en.wikipedia.org/wiki/Graphviz), Mermiad 等。

### Sources

````markdown
:::spoiler Graphviz
```graphviz
digraph {
    A0[shape=none];
    I8[shape=doublecircle];

    A0->B1[label="0"]
    B1->C2[label="1"]
    C2->D3[label="0"]
    D3->E4[label="1"]
    E4->F5[label="0"]
    F5->G6[label="1"]
    G6->H7[label="1"]
    H7->I8[label="1"]

    edge[weight=0]
    H7->J9[label="0"]
    J9->K10[label="1"]
    K10->H7[label="1"]


    edge[style=dashed]
    A0->A0[label="1"]
    B1->B1[label="0"]
    C2->A0[label="1"]
    D3->B1[label="0"]
    E4->A0[label="1"]
    F5->B1[label="0"]
    G6->F5[label="0"]
    I8->A0[label="1"]
    I8->B1[label="0"]
    J9->B1[label="0"]
    K10->D3[label="0"]
}
```
:::
````

### Results

:::spoiler Graphviz
```graphviz
digraph {
    A0[shape=none];
    I8[shape=doublecircle];

    A0->B1[label="0"]
    B1->C2[label="1"]
    C2->D3[label="0"]
    D3->E4[label="1"]
    E4->F5[label="0"]
    F5->G6[label="1"]
    G6->H7[label="1"]
    H7->I8[label="1"]

    edge[weight=0]
    H7->J9[label="0"]
    J9->K10[label="1"]
    K10->H7[label="1"]


    edge[style=dashed]
    A0->A0[label="1"]
    B1->B1[label="0"]
    C2->A0[label="1"]
    D3->B1[label="0"]
    E4->A0[label="1"]
    F5->B1[label="0"]
    G6->F5[label="0"]
    I8->A0[label="1"]
    I8->B1[label="0"]
    J9->B1[label="0"]
    K10->D3[label="0"]
}
```
:::

## $\LaTeX$

HackMD 透過 [MathJax](https://en.wikipedia.org/wiki/MathJax) 支援數學式子的顯示。

### Sources

```markdown
This is an inline math expression: $(1-x)^{-n}=\sum_{i=0}^\infty\binom{-n}{i}(-x)^i=\sum_{i=0}^\infty(-1)^i\binom{n+i-1}{i}(-x)^i$.

And the following is a display math expression: $$\begin{pmatrix}A_{0,0}&A_{0,1}\\A_{1,0}&A_{1,1}\end{pmatrix}=\begin{pmatrix}I&O\\A_{1,0}A_{0,0}^{-1}&I\end{pmatrix}\begin{pmatrix}A_{0,0}&O\\O&A_{1,1}-A_{1,0}A_{0,0}^{-1}A_{0,1}\end{pmatrix}\begin{pmatrix}I&A_{0,0}^{-1}A_{0,1}\\O&I\end{pmatrix}$$
```

### Results

This is an inline math expression: $(1-x)^{-n}=\sum_{i=0}^\infty\binom{-n}{i}(-x)^i=\sum_{i=0}^\infty(-1)^i\binom{n+i-1}{i}(-x)^i$.

And the following is a display math expression: $$\begin{pmatrix}A_{0,0}&A_{0,1}\\A_{1,0}&A_{1,1}\end{pmatrix}=\begin{pmatrix}I&O\\A_{1,0}A_{0,0}^{-1}&I\end{pmatrix}\begin{pmatrix}A_{0,0}&O\\O&A_{1,1}-A_{1,0}A_{0,0}^{-1}A_{0,1}\end{pmatrix}\begin{pmatrix}I&A_{0,0}^{-1}A_{0,1}\\O&I\end{pmatrix}$$

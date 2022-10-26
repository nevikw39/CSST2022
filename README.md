# CSST 2022: 使用 Markdown 和 LaTeX 成為筆記大師
## `nevikw39`

上次課程的 [Feedback 表單](https://forms.gle/hNT7dobV7GXgUjA28), 填完之後有 shell demo codes 以及簡報連結喔。

## Markdown

什麼是 Markdown 呢？Markdown 是一種輕量的標記語言 _(Markup Languages)_. 而所謂標記語言 (e.g. **HTML** _(HyperText Markup Language)_, **XML** _(eXtensible Markup Language)_, **YAML** _(Yet Another Markup Language)_, **TOML** _(Tom's Obvious Minimal Language)_, **JSON** _(JavaScript Object Notation)_, **TeX**, ...) 通常是純文字文件，依據功能主要可以分為顯示用與資料序列化兩種。

顯示用的標記語言通常是個標準或規範，由於檔案本身是純文字，因此有可以 Text Editors 編輯、易於傳輸、方便採用版本控制等優點。純文字檔藉由根據標準實作的軟體或網頁後可以渲染 _(rander)_ 成帶有格式的結果，缺點則包括不同電腦、軟體渲染的結果可能有所出入。

Markdown 的語法更接近人類的自然語言，可以藉由軟體或網頁轉換成更複雜的標記語言如 HTML, 再加以渲染。由於 Markdown 的簡潔、易讀等特性，現在已警備很廣泛的應用，包括 Discord, Telegram, Slack 等通訊軟體都支援部分行內 Markdown 語法，StackOverflow 家族的論壇、Reddit 等也都可以 Markdown 發文，軟體或 repo 的 README 檔，包括這份文件，現今也往往是 Markdown 格式，甚至還有很多工具可以把 Markdown 檔案們建置成 Blog, 電子書等。

由於 Markdown 是個自由的標準，也有許多衍生的版本，比如 GitHub-Favored Markdown 等等。

### 軟體與網頁

編寫 Markdown 原始碼時，因為是純文字而無法直接立即得到結果，與現今我們早已習慣的 Apple Pages, Microsoft Word 等 What You See Is What You Get _([WYSIWYG](https://en.wikipedia.org/wiki/WYSIWYG))_ 所見即所得的編輯器有不小的差別。

現代大部分的 Text Editors 如 VS Code, Sublime, Atom, NotePad++ 應該多少會支援 Markdown, 以 VS Code 來說，按下 <kbd>⌘ Cmd</kbd> (<kbd>⌃ Ctrl</kbd> if not  macOS) + <kbd>K</kbd> 放開後再按一下 <kbd>V</kbd>就可以在側邊開啟即時預覽。有些軟體像是 Typora, Notion 是專門以 Markdown 來做筆記，但我就沒有研究。

線上網站包括 GitHub Gist, GitHub 都可以建立並顯示 Markdown 文件，[HackMD](https://hackmd.io) 更方便還支援許多額外的擴充功能。

### 基本語法

撰寫 Markdown 很像在寫一般純文字文件，有需求時利用語法來標記。注意段落之間需要有一個空行，結果才會換行。

大部分的時候 Markdown 都會被轉為 HTML, 因此也可以直接使用 HTML 語法。

#### Inline

一些行內標記，像是粗體、斜體、等寬字體、超連結、圖片等，以及不在標準但被廣泛實作的刪除線效果。

##### Sources

```markdown
Wrap words in **two consecutive asterisks** or __two consecutive underscores__ to make them **bold**.

Wrap words in _single underscores_ or *single asterisks* to make them _Italic_.

**Bold** and _Italic_ could be combined nestly like _**this** one_.

Wrap words in `single backticks` to make them `inline codes (monospace font)`.

Create a link by putting the text you'd like to display inside brackets, then putting parentheses around the relative or absolute link, e.g. [my blog](https://nevikw39.cf).

Insert an image by an exclamation mark, brackets around text displayed when mouse hovered and parentheses wrapping the relative or absolute link to the image, e.g. ![Text displayed when mouse hovered](https://m110.nthu.edu.tw/~s110062219/favicon.ico)

Some Markdown renderers support to wrap words in ~~two consecutive tildes~~ to make them strikethrough.
```

##### Results

Wrap words in **two consecutive asterisks** or __two consecutive underscores__ to make them **bold**.

Wrap words in _single underscores_ or *single asterisks* to make them _Italic_.

**Bold** and _Italic_ could be combined nestly like _**this** one_.

Wrap words in `single backticks` to make them `inline codes (monospace font)`.

Create a link by putting the text you'd like to display inside brackets, then putting parentheses around the link, e.g. [my blog](https://nevikw39.cf).

Insert an image by an exclamation mark, brackets around text displayed when mouse hovered and parentheses wrapping the relative or absolute link to the image, e.g. ![Text displayed when mouse hovered](https://m110.nthu.edu.tw/~s110062219/favicon.ico)

Some Markdown renderers support to wrap words in ~~two consecutive tildes~~ to make them strikethrough.

#### Headers

標題的語法有兩種風格，分別承襲自兩個標記語言 Setext, atx. 其中 Setext 只支援兩層標題，atx 則支援 HTML 的六層標題。

```markdown
Put any numbe of `=` below a line to make it Setext header 1
===

Put any numbe of `-` below a line to make it Setext header 2
---

# Put a `#` at the beginning of a line to make it atx header 1

## Put two `#`s at the beginning of a line to make it atx header 2

### Put i `#`s at the beginning of a line to make it atx header i
```

#### List

Markdown 的有序與無序清單非常直觀。注意在最初標準中有序清單總是由 1 開始且其數字並不重要，但現在大部分實作也可以從其他數字開始。

##### Sources

```markdown
- To start an unordered list, use either `-`, `+` or `*`.
- I'm another item.
  * Nested lists are also supported by _indentation_.
- An item could be multiple lines.
  Like this.

1. Put a number, a period and a space to start an ordered list.
1. In fact I'm the **second** one.
87. Then guess what number would be displayed before this line?
```

##### Results

- To start an unordered list, use either `-`, `+` or `*`.
- I'm another item.
  * Nested lists are also supported by _indentation_.
- An item could be multiple lines.
  Like this.

1. Put a number, a period and a space to start an ordered list.
1. In fact I'm the **second** one.
87. Then guess what number would be displayed before this line?

#### Codes

這裡介紹的 codes 區塊並不在最初標準中，但現今大部分 renderers 都支援三個 backticks 與語言種類（可以 highlight 程式碼）開啟區塊，再以三個 backticks 結束區塊。

##### Sources

````markdown
```cpp
/**                  _ _              _____ ___
 *  _ __   _____   _(_) | ____      _|___ // _ \
 * | '_ \ / _ \ \ / / | |/ /\ \ /\ / / |_ \ (_) |
 * | | | |  __/\ V /| |   <  \ V  V / ___) \__, |
 * |_| |_|\___| \_/ |_|_|\_\  \_/\_/ |____/  /_/
 **/
#include <bits/extc++.h>
#ifndef nevikw39
#define nevikw39 cin.tie(nullptr)->sync_with_stdio(false)
#pragma GCC optimize("Ofast,unroll-loops,no-stack-protector,fast-math")
#pragma GCC target("tune=native")
#else
#pragma message("hello, nevikw39")
#endif
#pragma message("GL; HF!")
using namespace std;
using namespace __gnu_cxx;
using namespace __gnu_pbds;
template <typename T, typename Cmp = greater<T>, typename Tag = pairing_heap_tag>
using _heap = __gnu_pbds::priority_queue<T, Cmp, Tag>;
template <typename K, typename M = null_type>
using _hash = gp_hash_table<K, M>;
template <typename K, typename M = null_type, typename Cmp = less<K>, typename T = rb_tree_tag>
using _tree = tree<K, M, Cmp, T, tree_order_statistics_node_update>;

int main()
{
    nevikw39;
    return 0;
}
```
````

##### Results

```cpp
/**                  _ _              _____ ___
 *  _ __   _____   _(_) | ____      _|___ // _ \
 * | '_ \ / _ \ \ / / | |/ /\ \ /\ / / |_ \ (_) |
 * | | | |  __/\ V /| |   <  \ V  V / ___) \__, |
 * |_| |_|\___| \_/ |_|_|\_\  \_/\_/ |____/  /_/
 **/
#include <bits/extc++.h>
#ifndef nevikw39
#define nevikw39 cin.tie(nullptr)->sync_with_stdio(false)
#pragma GCC optimize("Ofast,unroll-loops,no-stack-protector,fast-math")
#pragma GCC target("tune=native")
#else
#pragma message("hello, nevikw39")
#endif
#pragma message("GL; HF!")
#define ND second
using namespace std;
using namespace __gnu_cxx;
using namespace __gnu_pbds;
template <typename T, typename Cmp = greater<T>, typename Tag = pairing_heap_tag>
using _heap = __gnu_pbds::priority_queue<T, Cmp, Tag>;
template <typename K, typename M = null_type>
using _hash = gp_hash_table<K, M>;
template <typename K, typename M = null_type, typename Cmp = less<K>, typename T = rb_tree_tag>
using _tree = tree<K, M, Cmp, T, tree_order_statistics_node_update>;

int main()
{
    nevikw39;
    return 0;
}
```

#### Quotes

引用可以很多層，也可以結合其他語法。

##### Sources

```markdown
> Ars longa, vita brevis
> > Ὁ βίος βραχύς, ἡ δὲ τέχνη μακρή

> I believe a leaf of grass is no less than the journey-work of the stars, \
> And the pismire is equally perfect, and a grain of sand, and the egg of the wren, \
> And the tree toad is a chef-d’œuvre for the highest, \
> And the running blackberry would adorn the parlours of heaven.
>
> _Walt Whitman_

> Each morning I get up I die a little \
> Can barely stand on my feet \
> Take a look in the mirror and cry \
> Lord, what you're doing to me? \
> I have spent all my years in believing you \
> But I just can't get no relief, Lord
> Somebody, somebody \
> Can anybody find me somebody to love?
>
> **Somebody To Love**, _Queen_
```

##### Results

> Ars longa, vita brevis
>> Ὁ βίος βραχύς, ἡ δὲ τέχνη μακρή

> I believe a leaf of grass is no less than the journey-work of the stars, \
> And the pismire is equally perfect, and a grain of sand, and the egg of the wren, \
> And the tree toad is a chef-d’œuvre for the highest, \
> And the running blackberry would adorn the parlours of heaven.
>
> _Walt Whitman_

> Each morning I get up I die a little \
> Can barely stand on my feet \
> Take a look in the mirror and cry \
> Lord, what you're doing to me? \
> I have spent all my years in believing you \
> But I just can't get no relief, Lord
> Somebody, somebody \
> Can anybody find me somebody to love?
>
> **Somebody To Love**, _Queen_

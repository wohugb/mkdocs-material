# 脚注 Footnotes

[Footnotes][1] is another extension included in the standard Markdown library.
As the name says, it adds the ability to add footnotes to your documentation.

  [1]: https://pythonhosted.org/Markdown/extensions/footnotes.html

## 安装

添加以下行到你的 `mkdocs.yml`:

``` yaml
markdown_extensions:
  - footnotes
```

## 使用

The markup for footnotes is similar to the standard Markdown markup for links.
A reference is inserted in the text, which can then be defined at any point in
the document.

### 插入引用

The footnote reference is enclosed in square brackets and starts with a caret,
followed by an arbitrary label which may contain numeric identifiers [1, 2, 3,
...] or names [Granovetter et al. 1998]. The rendered references are always
consecutive superscripted numbers.

示例:

``` markdown
Lorem ipsum[^1] dolor sit amet, consectetur adipiscing elit.[^2]
```

结果:

Lorem ipsum[^1] dolor sit amet, consectetur adipiscing elit.[^2]

### 插入内容

The footnote content is also declared with a label, which must match the label
used for the footnote reference. It can be inserted at an arbitrary position in
the document and is always rendered at the bottom of the page. Furthermore, a
backlink is automatically added to the footnote reference.

#### 单行

简短说明可以写在一行.

示例:

``` markdown
[^1]: Lorem ipsum dolor sit amet, consectetur adipiscing elit.
```

结果:

<a href="#fn:1">Jump to footnote at the bottom of the page</a>

  [^1]: Lorem ipsum dolor sit amet, consectetur adipiscing elit.

#### 多行

Paragraphs should be written on the next line. As with all Markdown blocks, the
content must be indented by four spaces.

示例:

``` markdown
[^2]:
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.
```

结果:

  [^2]:
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
      nulla. Curabitur feugiat, tortor non consequat finibus, justo purus
      auctor massa, nec semper lorem quam in massa.

<a href="#fn:2">Jump to footnote at the bottom of the page</a>

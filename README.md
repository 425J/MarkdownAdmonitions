# Markdown Admonitions

The advantage of Markdown is that it is not overly complex. It is also its disadvantage. [Vanilla Markdown](https://daringfireball.net/projects/markdown/) lacks many of the features that I usually use when writing documentation. One of them is admonition (aka callout, box, alert, notification, etc).

There is no built-in admonition formatting in vanilla Markdown. It is available only in some advanced flavors (e.g.: [Docusaurus](https://docusaurus.io/docs/markdown-features/admonitions) or [MkDocs](https://squidfunk.github.io/mkdocs-material/reference/admonitions/)). However, there are a couple of workarounds to this issue...
## Simple Table

Admonition can be created using Markdown [table syntax](https://www.markdownguide.org/extended-syntax/#tables) as follows: 

```markdown
| BOX TYPE/NAME<br>Box content. |
| :-- |
```

Which will be rendered as:

| BOX TYPE/NAME<br>Box content. |
| :-- |

Using this technique we can create the following admonitions:

| ℹ️ NOTE<br>You might read this, you might not. |
| :-- |

| ❗ IMPORTANT<br>You should read this. |
| :-- |

| 💡 TIP<br>You want to read this. |
| :-- |

| ⚠️ CAUTION<br>I hope you read this. |
| :-- |

| 🔥 WARNING<br>You need to read this. |
| :-- |

_The above admonitions are inspired by [this](https://github.com/elviswolcott/remark-admonitions#infima-docusaurus-v2)._

This technique is simple and works well on platforms that use extensive Markdown sanitization, like [GitHub](https://github.com/github/markup). However, it is difficult to use it with more complex content.

## HTML Table

| ❗ IMPORTANT<br>Please note that it will not work properly in GitHub because of it [sanitization filter](https://github.com/github/markup). |
| :-- |

| ℹ️ NOTE<br>To properly display this example, use the markdown viewer without sanitization. |
| :-- |

It is possible to use [HTML tags](https://www.markdownguide.org/basic-syntax/#html) in Markdown. This feature can be used to format admonitions as an HTML table as follows:

```html
<table style="background-color:#FFF8E6;color:black;border-style:solid;border-color:#E6A700;border-width:thin;border-left-width:thick;">
<tr align= "left"><th>⚠️ Caution</th></tr>
<tr><td>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.</td></tr> 
</table>
```

Examples of admonitions using the HTML technique are as below:

<table style="background-color:#FDFDFE;color:black;border-style:solid;border-color:#D4D5D8;border-width:thin;border-left-width:thick;">
<tr align= "left"><th>📝 Note</th></tr>
<tr><td>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.</td></tr> 
</table>

<table style="background-color:#E6F6E6;color:black;border-style:solid;border-color:#009400;border-width:thin;border-left-width:thick;">
<tr align= "left"><th>💡 Tip</th></tr>
<tr><td>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.</td></tr> 
</table>

<table style="background-color:#EEF9FD;color:black;border-style:solid;border-color:#4CB3D4;border-width:thin;border-left-width:thick;">
<tr align= "left"><th>ℹ️ Info</th></tr>
<tr><td>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.</td></tr> 
</table>

<table style="background-color:#FFF8E6;color:black;border-style:solid;border-color:#E6A700;border-width:thin;border-left-width:thick;">
<tr align= "left"><th>⚠️ Caution</th></tr>
<tr><td>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.</td></tr> 
</table>

<table style="background-color:#FFEBEC;color:black;border-style:solid;border-color:#E13238;border-width:thin;border-left-width:thick;">
<tr align= "left"><th>🔥 Danger</th></tr>
<tr><td>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor massa, nec semper lorem quam in massa.</td></tr> 
</table>

_The above admonitions are inspired by [this](https://github.com/elviswolcott/remark-admonitions#classic-docusaurus-v1)._

## SVG Boxes

TODO

## Aditional Resources

- [Difference between caution and warning](https://www.differencebetween.com/difference-between-caution-and-vs-warning/)
- [Callouts in Quarto](https://quarto.org/docs/authoring/callouts.html)
- [Admonitions in Asciidoctor](https://docs.asciidoctor.org/asciidoc/latest/blocks/admonitions/)
- [GitHub Emoji](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)

Useful icons:

| Type        | Unicode | GitHub |
| :---------: | :-----: | :----: |
| Note        | 📝       | `:memo:` |
| Information | ℹ️       | `:information_source:` |
| Tip         | 💡       | `:bulb:` |
| Caution     | ⚠️       | `:warning:` |
| Danger      | 🔥       | `:fire:` |

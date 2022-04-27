# Markdown Admonitions

The advantage of Markdown is that it is not overly complex. It is also its disadvantage. [Vanilla Markdown](https://daringfireball.net/projects/markdown/) lacks many of the features that I usually use when writing documentation. One of them is admonition (aka callout, box, alert, notification, etc).

There is no built-in admonition formatting in vanilla Markdown. It is available only in some advanced flavors (e.g.: [Docusaurus](https://docusaurus.io/docs/markdown-features/admonitions) or [MkDocs](https://squidfunk.github.io/mkdocs-material/reference/admonitions/)). However, there are a couple of workarounds to this issue:

- [Simple Table](#simple-table)
- [HTML Table](#html-table)
- [SVG Boxes](#svg-boxes)

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

Examples of admonitions using the HTML technique are below:

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

Below are examples of admonitions, using the HTML table technique, rendered in VS Code:

![](/HTML/HTML&#32;Table&#32;Admonitions.png)

The advantage of this solution is that the appearance of the box can be freely customized. Moreover, the box is responsive (looks good on different devices). Unfortunately, the way it is displayed depends on the Markdwon viewer.

## SVG Boxes

Admonition box can be created as a SVG image and placed in the Markdown document as [image](https://www.markdownguide.org/basic-syntax/#images-1). Examples can be found [here](https://github.com/berakoc/github-notification-markups).

The SVG file contains the following part:

```html
<div class="container">
	<div class="header">
		<svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" fill="#9F6000" viewBox="0 0 512 512" style="enable-background:new 0 0 512 512;" xml:space="preserve">
			<g>
				<path d="M501.609,384.603L320.543,51.265c-13.666-23.006-37.802-36.746-64.562-36.746c-26.76,0-50.896,13.74-64.562,36.746
						c-0.103,0.176-0.19,0.352-0.293,0.528L10.662,384.076c-13.959,23.491-14.223,51.702-0.719,75.457
						c13.535,23.769,37.919,37.948,65.266,37.948h360.544c27.347,0,52.733-14.179,66.267-37.948
						C515.524,435.779,515.261,407.566,501.609,384.603z M225.951,167.148c0-16.586,13.445-30.03,30.03-30.03
						c16.586,0,30.03,13.445,30.03,30.03v120.121c0,16.584-13.445,30.03-30.03,30.03s-30.03-13.447-30.03-30.03V167.148z
						M255.981,437.421c-24.839,0-45.046-20.206-45.046-45.046c0-24.839,20.206-45.045,45.046-45.045
						c24.839,0,45.045,20.206,45.045,45.045C301.027,417.214,280.821,437.421,255.981,437.421z"/>
			</g>
		</svg>
		<span class="message"><b>Caution</b><br/>This tool is at the <b>alpha phase</b>. It means that the code is not a complete solution; that the code may not be fully functional; that the code may not have been tested or validated; and that the code may have bugs and errors. The tool may change drastically once it reaches the beta phase. <b>Use at your own risk.</b></span>
	</div>
</div>
```

The `<span class="message">` element contains the admonition message. The `<path>` element describes the icon.

The SVG admonition looks like this:

![](/SVG/Example&#32;Warning.svg)

The advantage of this solution is that it always looks the same. However, the main disadvantage is that **it is not responsive** because the box has a fixed size, so if we create a message that looks good on a high-resolution PC, it will look bad on a mobile device and vice versa. Another disadvantage is that you have to create separate files for each message and attach them to the Markdown document as a dependency.

---

## Useful Admonition Icons and Guidance

|        Type        | Unicode |         GitHub         | Guidance                                                     |
| :----------------: | :-----: | :--------------------: | :----------------------------------------------------------- |
|        Note        |    📝    |        `:memo:`        | It is normally used for general information that you want to stand out. See [this](https://paligo.net/docs/en/admonitions--notes,-warnings,-tips,-etc--.html). |
| Information/Notice |    ℹ️    | `:information_source:` | It is generally regarded as being of more importance than a regular note. See [this](https://paligo.net/docs/en/admonitions--notes,-warnings,-tips,-etc--.html). |
|        Tip         |    💡    |        `:bulb:`        | Tips are designed for giving readers helpful advice and suggestions. See [this](https://paligo.net/docs/en/admonitions--notes,-warnings,-tips,-etc--.html). |
|     Important      |    ❗    |    `:exclamation:`     | This element is for adding extra emphasis to general information. See [this](https://paligo.net/docs/en/admonitions--notes,-warnings,-tips,-etc--.html). |
|      Caution       |    ⚠️    |      `:warning:`       | Use to advise the reader to *act* carefully (i.e., exercise care). See [this](https://asciidoctor.org/docs/asciidoc-writers-guide/). |
|   Danger/Warning   |    🔥    |        `:fire:`        | Use to inform the reader of danger, harm, or consequences that exist. See [this](https://asciidoctor.org/docs/asciidoc-writers-guide/). |

## Aditional Resources

- [Difference between caution and warning](https://www.differencebetween.com/difference-between-caution-and-vs-warning/)
- [Callouts in Quarto](https://quarto.org/docs/authoring/callouts.html)
- [Admonitions in Asciidoctor](https://docs.asciidoctor.org/asciidoc/latest/blocks/admonitions/)
- [GitHub Emoji](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md)

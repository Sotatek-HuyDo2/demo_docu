---
sidebar_position: 2
---

# Create a Document

Documents are **groups of pages** connected through:

- a **sidebar**
- **previous/next navigation**
- **versioning**
  <!-- - là dot -->

## Create your first Doc

Create a Markdown file at `docs/hello.md`:

```md title="docs/hello.md"
# Hello
This is my very first doc! 🎉🎊✨
This is my **first Docusaurus document**!
```

A new document is now available at [http://localhost:3000/docs/hello](http://localhost:3000/docs/hello).

## Configure the Sidebar

Docusaurus automatically **creates a sidebar** from the `docs` folder.

Add metadata to customize the sidebar label and position:

```md title="docs/hello.md" {1-4}
---
sidebar_label: 'Hi!'
sidebar_position: 3
---

# Hello

This is my **first Docusaurus document**!
```

It is also possible to create your sidebar explicitly in `sidebars.js`:

```js title="sidebars.js"
module.exports = {
  tutorialSidebar: [
    'intro',
    // highlight-next-line
    'hello',
    {
      type: 'category',
      label: 'Tutorial',
      items: ['tutorial-basics/create-a-document'],
    },
  ],
};
```
> this iss trích dẫn
>
> đây sẽ là cả 1 khối trích dẫn
>> trích dẫn lồng

* đây là liệt kê 
- đây cũng là liệt kê
  - liệt kê lồng 
- __this is bold__ or **this is bold**
- _this is italic_ or *this is italic*
- ___this is bold and italic___ or ***this is italic and bold***
[^1]: đay là chú thích

> đây là lít
> 1. First item
> 1. Second item
> 1. Third item
> 1. Fourth item

> this is link tham khao [tai lieu](extension://fogenijnedmmmofgaifofnihbalehpdg/pdfjs/web/viewer.html?file=https%3A%2F%2Fwww.markdownguide.org%2Fassets%2Fmarkdown-guide-sample.pdf)

> this is link <https://www.markdownguide.org>

<!-- > #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**. -->
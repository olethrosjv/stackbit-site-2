---
title: Transformer plugins
date: 2020-03-24T23:52:37.645Z
thumb_img_path: /images/abstract-art-blur-bright.jpg
hide_header: false
template: post
---
Often, the format of the data you get from source plugins isn’t what you want to use to build your website. The filesystem source plugin lets you query data *about* files but what if you want to query data *inside* files?

To make this possible, Gatsby supports transformer plugins which take raw content from source plugins and *transform* it into something more usable.

For example, markdown files. Markdown is nice to write in but when you build a page with it, you need the markdown to be HTML.

Source plugins bring data *into* Gatsby’s data system and *transformer* plugins transform raw content brought by source plugins. This pattern can handle all data sourcing and data transformation you might need when building a Gatsby site.

When querying a connection of some type, you can pass a variety of arguments to the GraphQL query. You can sort and filter nodes, set how many nodes to skip, and choose the limit of how many nodes to retrieve. With this powerful set of operators, you can select any data you want—in the format you need.

Gatsby is *not* limited to making pages from files like many static site generators. Gatsby lets you use GraphQL to query your *data* and *map* the query results to *pages*—all at build time. This is a really powerful idea.
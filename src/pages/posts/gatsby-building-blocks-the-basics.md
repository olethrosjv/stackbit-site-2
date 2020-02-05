---
title: Gatsby Building Blocks - The Basics
date: 2020-02-05T23:38:06.961Z
thumb_img_path: /images/Gatsby_Logo_Black.png
content_img_path: /images/Gatsby_Logo_Black.png
hide_header: false
template: post
---
When creating a new Gatsby site, you can create a new site based on any existing Gatsby starter. Gatsby uses hot reloading to speed up your development process. Essentially, when you’re running a Gatsby development server, the Gatsby site files are also running in the background —when you save a file, your changes will be immediately reflected in the browser. No need to hard refresh the page or restart the development server — your changes just appear.

In Gatsby you use JSX syntax. This hybrid “HTML-in-JS” is a syntax extension of JavaScript, for React. It is JSX, not pure HTML and JavaScript, so how does the browser read that? Gatsby sites come with tooling already set up to convert your source code into something that browsers can interpret.

Creating a site in Gatsby means using components. A component is a building block for your site; a self-contained piece of code that describes a section of UI. Gatsby is built on React. When we talk about using and defining components , we are really talking about React components, self-contained pieces of code (usually written with JSX) that can accept input and return React elements describing a section of UI.

One of the big mental shifts you make when starting to build with components (if you are already a developer) is that now your CSS, HTML, and JavaScript are tightly coupled and often living even within the same file. While a seemingly simple change, this has profound implications for how you think about building websites.

To make these reusable pieces dynamic you need to be able to supply them with different data. You do that with input called “props”. Props are (appropriately enough) properties supplied to React components.

Layout components are for sections of a site that you want to share across multiple pages. For example, Gatsby sites will commonly have a layout component with a shared header and footer. Other common things to add to layouts include a sidebar and/or a navigation menu.

Gatsby.js is a **modern site generator**, which means there are no servers to set up or complicated databases to deploy. Instead, the Gatsby `build` command produces a directory of static HTML and JavaScript files which you can deploy to a static site hosting service.


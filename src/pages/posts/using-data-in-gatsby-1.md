---
title: Using Data in Gatsby
date: 2020-03-13T01:01:14.550Z
thumb_img_path: /images/panda-group-eating-bamboo.jpg
hide_header: false
template: post
---
A website has four parts: HTML, CSS, JS, and data.  

## What is data?

A very computer science-y answer would be: data is things like "strings", integers (42), objects ({ pizza: true }), etc. 

For the purpose of working in Gatsby, however, a more useful answer is “everything that lives outside a React component”. Often you want to store data outside components and then bring the data into the component as needed. 

If you’re building a site with WordPress (so other contributors have a nice interface for adding & maintaining content) and Gatsby, the data for the site (pages and posts) are in WordPress and you pull that data, as needed, into your components.  Data can also live in file types like Markdown, CSV, etc. as well as databases and APIs of all sorts. 

Gatsby’s data layer lets you pull data from these (and any other source) directly into your components—in the shape and form you want. 

## Using Unstructured Data vs GraphQL 

You don’t have to use GraphQL and source plugins to pull data into Gatsby sites You can use the node createPages API to pull unstructured data into Gatsby pages directly, rather than through the GraphQL data layer. This is a great choice for small sites, while GraphQL and source plugins can help save time with more complex sites. 

## When do I use unstructured data vs GraphQL? 

If you’re building a small site, one efficient way to build it is to pull in unstructured data as outlined here, using createPages API, and then if the site becomes more complex later on, you move on to building more complex sites, or you’d like to transform your data, follow these steps: 



Check out the Plugin Library to see if the source plugins and/or transformer plugins you’d like to use already exist. 

## How Gatsby’s data layer uses GraphQL to pull data into components 

There are many options for loading data into React components. One of the most popular and powerful of these is a technology called GraphQL. GraphQL was invented at Facebook to help product engineers pull needed data into components. 

GraphQL is a query language (the QL part of its name). If you’re familiar with SQL, it works in a very similar way. Using a special syntax, you describe the data you want in your component and then that data is given to you. 

## Gatsby uses GraphQL to enable components to declare the data they need.

When building sites, you’ll probably want to reuse common bits of data —But what if you want to change the site title in the future? You’d have to search for the title across all your components and edit each instance. This is both cumbersome and error-prone, especially for larger, more complex sites. Instead, you can store the title in one location and reference that location from other files; change the title in a single place, and Gatsby will pull your updated title into files that reference it. 

The place for these common bits of data is the siteMetadata object in the gatsby-config.js file. 

Page queries live outside of the component definition — by convention at the end of a page component file — and are only available on page components. 

## Use a StaticQuery 

StaticQuery is a new API introduced in Gatsby v2 that allows non-page components (like your layout.js component), to retrieve data via GraphQL queries.  Its newly introduced hook version — useStaticQuery. 

One of the core principles of Gatsby is that creators need an immediate connection to what they’re creating (hat tip to Bret Victor). In other words, when you make any change to code you should immediately see the effect of that change. You manipulate an input of Gatsby and you see the new output showing up on the screen. 

So almost everywhere, changes you make will immediately take effect.

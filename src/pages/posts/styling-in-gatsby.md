---
title: Styling in Gatsby
date: 2020-02-14T01:23:39.096Z
thumb_img_path: /images/css-logo.jpg
hide_header: false
template: post
---

Every site has some sort of global style. This includes things like the site’s typography and background colors. These styles set the overall feel of the site — much like the color and texture of a wall sets the overall feel of a room. One of the most straightforward ways to add global styles to a site is using a global .css stylesheet.

## CSS Modules

Let’s explore CSS Modules. Quoting from the CSS Module homepage:
A CSS Module is a CSS file in which all class names and animation names are scoped locally by default. CSS Modules are very popular because they let you write CSS normally but with a lot more safety. The tool automatically generates unique class and animation names, so you don’t have to worry about selector name collisions.

Gatsby works out of the box with CSS Modules. This approach is highly recommended for those new to building with Gatsby (and React in general). A CSS Module is a CSS file in which all class names and animation names are scoped locally by default. 

CSS Modules compile to a low-level interchange format called ICSS or Interoperable CSS, but are written like normal CSS files: When importing the CSS Module from a JS Module, it exports an object with all mappings from local names to global names.

For local class names camelCase naming is recommended, but not enforced.

## CSS-in-JS

CSS-in-JS is a component-oriented styling approach. Most generally, it is a pattern where CSS is composed inline using JavaScript. There are many different CSS-in-JS libraries and many of them have Gatsby plugins already. We won’t cover an example of CSS-in-JS in this initial tutorial, but we encourage you to explore what the ecosystem has to offer.

“CSS-in-JS” refers to a pattern where CSS is composed using JavaScript instead of defined in external files. 
Styled Components.

Styled Components lets you use actual CSS syntax inside your components. Styled Components is a variant on “CSS-in-JS”—which solves many of the problems with traditional CSS.
One of the most important problems they solve is selector name collisions. With traditional CSS, you have to be careful not to overwrite CSS selectors used elsewhere in a site because all CSS selectors live in the same global namespace. This unfortunate restriction can lead to elaborate (and often confusing) selector naming schemes.

With CSS-in-JS, you avoid all that as CSS selectors are scoped automatically to their component. Styles are tightly coupled with their components. This makes it much easier to know how to edit a component’s CSS as there’s never any confusion about how and where CSS is being used.

## Creating Global Styles

Styled components are primarily used for a single CSS class that is isolated from other components. In some cases, you want to override global styling — for example, the default margins of your body element. Styled components have your back. You can use the createGlobalStyle to accomplish this. It’s advised to use createGlobalStyle in Layout components, which are shared over multiple pages rather than using it on a single page.

## Enabling user stylesheets with a stable class name

Adding a persistent CSS className to your styled components can make it easier for end users of your website to take advantage of user stylesheets for accessibility. An end user of your site could then write their own CSS styles matching HTML elements using a class name of .container. If your CSS-in-JS style changes, it will not affect the end user’s stylesheet.


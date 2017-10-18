---
description: Web Performance
keywords: web performance, optimize, minimize
title: Web Performance
---

# Web Performance

## Critical Rendering Path

![Critical Rendering Path](/product-development-process/images/critical-rendering-path.png)

- The Critical Rendering Path is the sequence of steps that the browser goes through to convert the HTML, CSS and JavaScript into actual pixels on the screen.
- First we grab the HTML and we start building the document object model (DOM). Then fetch the CSS and build the CSS object model (CSSOM).
- We combile those two to create the Render Tree. Then we have to figure out where every thing goes on the page, which is the layout step. And then finally we can paint pixels on the actual screen

## Converting HTML to the DOM

![Converting HTML to the DOM](/product-development-process/images/converting-html-to-the-dom.png){:.img-resize}

1. **Conversion**: The browser reads the raw bytes of HTML off the disk or network, and translates them to individual characters based on specified encoding of the file (for example, UTF-8).
2. **Tokenizing**: The browser converts strings of characters into distinct tokens. Example, "<html>", "<body>" and other strings within angle brackets. Each token has a special meaning and its own set of rules.
3. **Lexing**: The emitted tokens are converted into "objects," which define their properties and rules.
4. **DOM construction**: Finally, because the HTML markup defines relationships between different tags (some tags are contained within other tags) the created objects are linked in a tree data structure that also captures the parent-child relationships defined in the original markup: the HTML object is a parent of the body object, the body is a parent of the paragraph object, and so on.

## Converting CSS to the CSSOM

While the browser was constructing the DOM of our simple page, it encountered a link tag in the head section of the document referencing an external CSS stylesheet: style.css. Anticipating that it needs this resource to render the page, it immediately dispatches a request for this resource.

We could have declared our styles directly within the HTML markup (inline), but keeping our CSS independent of HTML allows us to treat content and design as separate concerns.

![CSSOM Construction](/product-development-process/images/cssom-construction.png){:.img-resize}

![CSSOM Tree](/product-development-process/images/cssom-tree.png){:.img-resize}

## Render-tree Construction, Layout, and Paint

The CSSOM and DOM trees are combined into a render tree, which is then used to compute the layout of each visible element and serves as an input to the paint process that renders the pixels to screen. 

- The DOM and CSSOM trees are combined to form the render tree.
- Render tree contains only the nodes required to render the page.
- Layout computes the exact position and size of each object.
- The last step is paint, which takes in the final render tree and renders the pixels to the screen.

First, the browser combines the DOM and CSSOM into a "render tree":

![Render Tree Construct](/product-development-process/images/render-tree-construction.png){:.img-resize}

To construct the render tree, the browser roughly does the following:
  - Starting at the root of the DOM tree, traverse each visible node.
    - Some nodes are not visible (for example, script tags, meta tags, and so on), and are omitted since they are not reflected in the rendered output.
    - Some nodes are hidden via CSS and are also omitted from the render tree; for example, the span node---in the example above---is missing from the render tree because we have an explicit rule that sets the "display: none" property on it.
  - For each visible node, find the appropriate matching CSSOM rules and apply them.
  - Emit visible nodes with content and their computed styles.

With the render tree in place, we can proceed to the "layout" stage.

Up to this point we've calculated which nodes should be visible and their computed styles, but we have not calculated their exact position and size within the viewport of the device---that's the "layout" stage, also known as "reflow."

To figure out the exact size and position of each object on the page, the browser begins at the root of the render tree and traverses it.

Finally, now that we know which nodes are visible, and their computed styles and geometry, we can pass this information to the final stage, which converts each node in the render tree to actual pixels on the screen. This step is often referred to as "painting" or "rasterizing."

## Optimize web performance

First, we talked about minifying, compression , and caching. All three techniques apply for HTML, CSS, JavaScript.

Minimize use of render blocking resources (CSS)
  1. Use media queries on `<link>` to unblock rendering
  2. Inline CSS

Minimize use of parser blocking resources (Java Script)
  1. Defer java script execution
  2. Use async attribute

Final, The general sequence of steps to optimize the critical rendering path is:
  1. Analyze and characterize your critical path: number of resources, bytes, length.
  2. Minimize number of critical resources: eliminate them, defer their download, mark them as async, and so on.
  3. Optimize the number of critical bytes to reduce the download time (number of roundtrips).
  4. Optimize the order in which the remaining critical resources are loaded: download all critical assets as early as possible to shorten the critical path length.

## Build CSS on PWA

  - Preloading content with rel="loading"
    - The preload value of the `<link>` element's rel attribute allows you to write declarative fetch requests in your HTML `<head>`.
    - Specifying resources that your pages will need very soon after loading, which you therefore want to start preloading early in the lifecycle of a page load, before the browser's main rendering machinery kicks in.
    - This ensures that they are made available earlier and are less likely to block the page's first render, leading to performance improvements.
    - Example:
        ```
        <head>
          <meta charset="utf-8">
          <title>CSS preload example</title>
          <link rel="preload" href="style.css" as="style">
          <link rel="stylesheet" href="style.css">
        </head>

        <body>
          <h1>bouncing balls</h1>
          <canvas></canvas>

          <script src="main.js"></script>
        </body>
        ```
  - The css attributes used to create the layout for the app are placed in a separate css file and the preload is applied so that it can be downloaded as soon as possible in the first render. Example, css for `<html>`, `<body>`, `<header>`, `<a>`, `<nav>`, `<brand>`, `<loader>`.....
  - The css attributes used to build the content for each page will be placed inline in the page and it will be added to `<header>` when the page is loaded.

## Reference

- https://classroom.udacity.com/courses/ud884
- https://developers.google.com/web/fundamentals/performance/critical-rendering-path/
- https://developers.google.com/web/fundamentals/performance/critical-rendering-path/constructing-the-object-model
- https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-tree-construction
- https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css
- https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript
- https://developers.google.com/web/fundamentals/performance/critical-rendering-path/optimizing-critical-rendering-path
- https://developer.mozilla.org/en-US/docs/Web/HTML/Preloading_content
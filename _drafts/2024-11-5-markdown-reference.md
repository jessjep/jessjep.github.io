---
title: "BLOG GUIDE"
date: 2024-11-14
image: "/assets/images/samples/sample-image-federica-fragapane-1.png"
---

Reference sheet for running blog + markdown.

https://www.markdownguide.org/cheat-sheet/

# IMPORTANT

Since I'm also working on this, it's important you check whether I've made changes to the website before you also make changes.

If you don't, you could override my changes.

To do this, simply make sure you click on "fetch origin" in GitHub desktop to see if there are any new changes I've uploaded to GitHub. If there are new changes, the button will then display "Pull origin". Make sure you click on that to pull the most up to date code from GitHub. Then you should be fine to start work.

![Pull origin on GitHub Desktop](/assets/images/samples/pull-origin.png)

## How to run the development version so you can view it before it goes live:

1. Open the terminal in VS Code
2. Make sure you have the correct folder open (it should be the location of your project), e.g. "C:\Users\emoor\OneDrive\Documents\GitHub\portfolio\jessjep.github.io>"
3. If you're not, you can type "cd path/to/folder" to get to it.
4. Enter "bundle exec jekyll serve" and click on the link for the server address printed to the console. Typically it's http://127.0.0.1:4000/
5. If you want to also view your drafts, you can enter "bundle exec jekyll serve --drafts" instead of the command in step 4.

Once you commit new changes and then push them to GitHub, the updates will display on the live website.

## How to center images

#### Recommended:

|                                                                                                 |
| :---------------------------------------------------------------------------------------------: |
|                ![Description of the image](/assets/images/chess/totals_plot.png)                |
| _[Caption (if you don't want to link to anything, remove the []() brackets](http://google.com)_ |

#### Alternative:

You can do some styling with HTML, like this, but since the `<img>` is inside a `<p>` element, it might not behave the way you want it to.

Setting margin: auto doesn't work to center the image, but the widths and border do work.

<img src="/assets/images/chess/totals_plot.png" style="height:300px;width:300px;margin:auto;border:2px solid green" alt="Plot of Registered Players">

#### Explanation:

Markdown puts everything inside `<p>` elements. This makes it difficult to style certain elements.

A way around it is to put images inside a table, and control the styling of the table/img with CSS, which is what I've done in styles.css:

`.post-content > table {
margin: 20px auto;
}

td > img {
max-width: 50%;
}
`

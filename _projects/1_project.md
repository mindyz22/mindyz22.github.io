---
layout: page
title: project 1
# 1. PROJECT SHORT DESCRIPTION (for card on homepage & project grid):
description: with background image # <-- WRITE YOUR SHORT CARD DESCRIPTION HERE
# 2. PROJECT THUMBNAIL PHOTO (for card on homepage & project grid):
img: assets/img/12.jpg # <-- WRITE PATH TO YOUR CARD THUMBNAIL PHOTO HERE (stored in assets/img/)
importance: 1
category: work
related_publications: true
# 3. CARD REDIRECT LINK (OPTIONAL):
# redirect: https://github.com/yourusername/your-repo # <-- Uncomment to link card directly to external site
---

<!--
=============================================================================
HOW TO WRITE & FORMAT YOUR PROJECT PAGE:
=============================================================================

1. WHERE TO WRITE DESCRIPTIONS:
   - Write your full project write-up, story, abstract, or methodology right here
     below the `---` line using Markdown or HTML.

2. HOW TO INCLUDE PHOTOS:
   - Place your image files inside the `assets/img/` folder.
   - Insert photos in the page using Liquid figure include (recommended for styling & captions):
       {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="Photo Caption" class="img-fluid rounded z-depth-1" %}
   - Or use standard Markdown:
       ![Photo description](assets/img/1.jpg)

3. HOW TO INCLUDE LINKS:
   - Standard Markdown link:
       [View GitHub Repository](https://github.com/your-username/repo-name)
   - Styled HTML Button link:
       <a href="https://github.com/your-username/repo-name" class="btn btn-outline-primary btn-sm" target="_blank">GitHub Repo</a>
       <a href="https://arxiv.org" class="btn btn-outline-secondary btn-sm" target="_blank">Read Paper</a>
=============================================================================
-->

Every project has a beautiful feature showcase page.
It's easy to include images in a flexible 3-column grid format.
Make your photos 1/3, 2/3, or full width.

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images, even citations {% cite einstein1950meaning %}.
Say you wanted to write a bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}

---
layout: post
title: How to use the LightForm Wiki
author: Adam Plowman
tags: []
toc: true
published: true
---
## How the site is organised

## How to add content

### Markdown

The following markdown...

## Adding images

Adding images with Markdown is easy; just type: `![image_description](image_url)`, where `image_description` is a short description of the image, and `image_url` is the URL that points to the image.

### Adding images with Prose.io

If you are using Prose.io to add and edit content (i.e. by clicking on the `EDIT` button in the top-right corner of the Wiki), you can easily upload and insert your own images, and Prose.io will insert the correct Markdown code for you. To use Prose.io to add an image to your Markdown, clik on the `Insert Image` button on the Prose.io toolbar:

![prose_io_toolbar.png]({{site.baseurl}}/assets/images/posts/prose_io_toolbar.png)
*The Prose.io toolbar, with the Insert Image button highlighted*

Then you can either manually add the image URL and image description, or you can add an image that has already been added to the Wiki, or you can upload a new image to the wiki. In the latter cases, the image description and image URL are automatically added for you.

![prose_io_insert_image.png]({{site.baseurl}}/assets/images/posts/prose_io_insert_image.png)
*Inserting an image with Pose.io.*

### Adding images without Prose.io

If you are not using Prose.io, please upload your images to the correct images directory of the Wiki, which is `/assets/images/posts/`. This way, we keep all post media in one place, and people who *are* using Prose.io can also use your images.

### Examples

The following code...

![aluminium_small.jpg]({{site.baseurl}}/assets/images/posts/aluminium_small.jpg)

```markdown
![Aluminium]({{site.baseurl}}/assets/images/posts/aluminium_small.jpg)
```
...adds the following image:

![Aluminium]({{site.baseurl}}/assets/images/posts/aluminium_small.jpg)

You can even add a caption to your image, with the following code:

```markdown
![Rolling]({{site.baseurl}}/assets/images/posts/rolling.gif)
*A visualisation of the rolling process.*
```

...which results in:

![Rolling]({{site.baseurl}}/assets/images/posts/rolling.gif)
*A visualisation of the rolling process.*

## Linking to other pages

## Experiments

## Frontmatter and Prose.io

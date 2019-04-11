---
layout: post
title: How to use the LightForm Wiki
author: Adam Plowman
tags: []
toc: true
published: true
---
## How the site is organised

Content is currently organised into three *collections*:

- Experiments
- Software & Simulation
- Miscellaneous

We can always change how content is organised at a later date, if the need arises. To add a page to one of these collections, navigate to the collection home page by using the links in the navigation side-bar. Next, click `ADD PAGE` or `ADD EXPERIMENT`. This will take you to a new page on Prose.io, which is a Markdown editor for GitHub. 

## How to add content

### Adding content with Prose.io

> Note that whenever you add a new Markdown file, or edit an existing Markdown file, you'll need to wait a couple of minutes before the changes show up on the website. This is because GitHub needs to re-build the website.

Prose.io is a Markdown editor for GitHub content. It allows us to write/edit Markdown files and add them to the Wiki without necessarily understanding how `git` works. Whenever you click on the `EDIT` button of a page, or you click a button to add a new page, you will be taken to the Prose.io website.

When you are adding a new page, the first thing you should do is **change the title of the page** (However, there is an exception to this: if you are adding a new experiment metadata YAML file, please **do not** change the title from what it is by default.). By default, the title of a new Markdown file is just set to the current date (something like: `2019-04-11 14:19 +0100`). You can change the title by editing the text at the top of the Prose.io page; it looks something like this:

![prose_io_title_guide_small.png]({{site.baseurl}}/assets/images/posts/prose_io_title_guide_small.png)

Prose.io has a Markdown editing toolbar that looks like this:

![prose_io_toolbar_guide_small.png]({{site.baseurl}}/assets/images/posts/prose_io_toolbar_guide_small.png)
*The Markdown editing toolbar of Prose.io allows you to format your content.*

And Prose.io has a sidebar on the right-hand side that looks like this:

![prose_io_sidebar_guide_small.png]({{site.baseurl}}/assets/images/posts/prose_io_sidebar_guide_small.png)
*The Prose.io sidebar allows you to save and preview the file, as well as edit the file's YAML metadata.*

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

The following Markdown...

```markdown
![Aluminium]({{site.baseurl}}/assets/images/posts/aluminium_small.jpg)
```
...adds the following image:

![Aluminium]({{site.baseurl}}/assets/images/posts/aluminium_small.jpg)

You can even add a caption to your image; the following Markdown:

```markdown
![Aluminium]({{site.baseurl}}/assets/images/posts/aluminium_small.jpg)
*Here is some aluminium*
```

...results in:

![Aluminium]({{site.baseurl}}/assets/images/posts/aluminium_small.jpg)
*Here is some aluminium*

## Experiments

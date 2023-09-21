---
layout: page-fullwidth
title: "ICC 2023 Prediction Contest"
subheadline: "How to use Feeling Responsive"
teaser: "The documentation is a work in progress..."
permalink: "/contest/"
header:
   image_fullwidth: "header_roadmap_2.jpg"
---

###  [Rules](../contest/rules)

### [Entry Form](../contest/entry)

### [Table of Predictions](../contest/predictions) (made by contest participants)

Ignore everything below. (Keeping it for reference only)

## Edit Navigation   {#edit-navigation}

To customize the navigation of *Feeling Responsive*, edit the [YAML](https://jekyllrb.com/docs/datafiles/)-file `_data/navigation.yml`.

## Different Page/Posts Formats   {#formats}

*Feeling Responsive* supports you with different templates for your content. These are the actual page/post formats:

### Page/Post
The [page/post format]({{ site.url }}{{ site.baseurl }}/design/page/) has no sidebar by default, its content is centered and beneath the content the visitor gets some metadata like categories, tags, date and author if provided via data in front matter of the post.

use in front matter via: `layout: page`

### Page/Post with a left or right sidebar
If you want to show the sidebar, just enter `sidebar: left` or `sidebar: right` in front matter, and *whoops, there it is*! To customize the content of the sidebar, open `_includes/sidebar`.


### Page/Post with or without metadata
You can show metadata, such as categories, tags and a date at the end of the page, just enter `show_meta: true`. By default, it's turned on. You can change it via `_config.yml`. To turn off metadata, enter `show_meta: false`.



### Page Full Width
If you want full control of styling a page, then use the [page fullwidth template]({{ site.url }}{{ site.baseurl }}/design/page-fullwidth/). To set up a grid, just use the [foundation grid system](http://foundation.zurb.com/docs/components/grid.html).

use in front matter via: `layout: page-fullwidth`


### Frontpage
This template is special. It allows you to define three *widgets* which are displayed with a headline, image, description and a link to the content. It's used for the [homepage]({{ site.url }}{{ site.baseurl }}) of this website.

use in front matter via: `layout: frontpage`


### Video
If you're a video producer or cineast, you'll like the [video template]({{ site.url }}{{ site.baseurl }}/design/video/). It darkens the layout to black and lets the video stand out full-width.

use in front matter via: `layout: video`

<small markdown="1">[Up to table of contents](#toc)</small>
{: .text-right }

## Style your content with   {#styling}

Feeling Responsive offers different options to style your article content. There are elements like subheadlines, feature images, header images, homepage images, meta data like categories and tags and many more.


### subheadlines

If you need a subheadline for an article, just define a subheadline in front matter like this:

`subheadline:  "Subheadline"`

### Quotes

Quotes mix it up a little bit, if you write long articles. So use quotes:

> Age is an issue of mind over matter. If you don't mind, it doesn't matter.
<cite>Mark Twain</cite>

<small markdown="1">[Up to table of contents](#toc)</small>
{: .text-right }

{% highlight html %}
> Age is an issue of mind over matter. If you don't mind, it doesn't matter.
<cite>Mark Twain</cite>
<small markdown="1">[Up to table of contents](#toc)</small>
{: .text-right }
{% endhighlight %}

## Comments

You can use comments with *Feeling Responsive* by the way of Disqus. If you want to use Disqus-Comments just open `config.yml` and add your `disqus_shortname`. [More on how to use Disqus ›](https://disqus.com/websites/)

By default comments are turned off. You can customize the default behaviour in `config.yml`. To **turn on comments** just add `comments: true` to front matter using the page layout `layout: page`. 

<small markdown="1">[Up to table of contents](#toc)</small>
{: .text-right }

## Responsive Videos

With foundation, responsive videos are easy. [More ›](http://foundation.zurb.com/docs/components/flex_video.html)

<div class="flex-video">
        <iframe width="1280" height="720" src="//www.youtube.com/embed/WoHxoz_0ykI" frameborder="0" allowfullscreen></iframe>
</div>

### Code to use for flexible videos

{% highlight html %}
<div class="flex-video">
  <iframe with video />
</div>
{% endhighlight %}


<img class="t60" src="{{ site.urlimg }}header_homepage_13.jpg" alt="">

## Images: Title, Thumbnails, Homepage   {#images}

There are several types of images you can define via front matter. If you want to change the images used in the header, have a look at [Style your Header]({{ site.url }}{{ site.baseurl }}/headers/). 


### Title Images

~~~
image:
    title: image.jpg
~~~


### Thumbnails

Thumbnails are used on archive pages like the [blog index][2]. They have a size of 150x150 pixels. Define them in front matter like this:

~~~
image:
    thumb: thumbnail_image.jpg
~~~


### Homepage Image

If you want to feature an article on the homepage with a huge image, then use the homepage image with a width of 970 pixels. If no homepage image is defined *Feeling Responsive* writes instead *New Blog Articles* over the blog entries. Define the homepage image like this:

~~~
image:
    homepage: header_homepage_13.jpg
~~~

### Captions with URL

Sometimes, you want to give credit to the creator of your images, maybe with a link. Especially when you use Creative Commons-images like I do for this website. Just add the following front matter and *Feeling Responsive* does the rest:

~~~
image:
    title: header_image.jpg
    caption: Image by Phlow
    caption_url: "http://phlow.de/"
~~~

### Define all images for an article

~~~
image:
    title: title_image.jpg
    thumb: thumbnail_image.jpg
    homepage: header_homepage_13.jpg
    caption: Image by Phlow
    caption_url: "http://phlow.de/"
~~~


<small markdown="1">[Up to table of contents](#toc)</small>
{: .text-right }


## Create a Table of Contents
{: .t60}

With the Kramdown parser for Markdown, you can render a table of contents for your documents. Just insert the following HTML in your post before the actual content. More information on [»Automatic ›Table of Contents‹ Generation«][1].

### Bare Bones Version
{% highlight html %}
### Table of Contents
*  Auto generated table of contents
{:toc}
{% endhighlight %}

### Foundation panel version

{% highlight html %}
<div class="panel radius" markdown="1">
**Table of Contents**
{: #toc }
*  TOC
{:toc}
</div>
{% endhighlight %}
<small markdown="1">[Up to table of contents](#toc)</small>
{: .text-right }

## Breadcrumbs

To turn on breadcrumbs, just use...

{% highlight html %}
breadcrumb: true
{% endhighlight %}



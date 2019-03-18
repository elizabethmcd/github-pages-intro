---
title: Personalizing the Jekyll Now Template
teaching: 30
exercises: 0
questions:
- "How can I make a personal website with GitHub Pages?"
objectives:
- "Create your own website with the Academic Pages template."
keypoints:
- "The same basics are applied to any template used with Jekyll/GH-pages."
---

Generally speaking, most GitHub/Jekyll website templates that you fork from, there will be a README.md file explaining how to get up running fairly quickly. The [Academic Pages README](https://github.com/academicpages/academicpages.github.io/blob/master/README.md) is a great resource for this particular template. 

Once you have cloned your forked version of the Academic Pages repository, the file structure should look like this:

```
CHANGELOG.md       _config.yml        _posts             files
CONTRIBUTING.md    _data              _publications      images
Gemfile            _drafts            _sass              markdown_generator
Gemfile.lock       _includes          _site              package.json
LICENSE            _layouts           _talks             talkmap
README.md          _pages             _teaching          talkmap.ipynb
_config.dev.yml    _portfolio         assets             talkmap.py
```

This may look a lot to get started with, but for the most part, there are only a couple of critical files and directories that are essential to getting you started with your own website. Arguably, the most important file for personalizing your site is the `_config.yml` file. This is the master "configuration" file in your site's root directory that contains global configurations and variable definitions. `cd` into the website directory that you cloned down from GitHub, and open the `_config.yml` file in a Text Editor. I highly recommend [BBEdit](https://www.barebones.com/products/bbedit/). Once you have opened it in a text editor,  or view it in the terminal with `head`, you should see the following (without my insertions): 

```
# Welcome to Jekyll!
#
# This config file is meant for settings that affect your entire site, values
# which you are expected to set up once and rarely need to edit after that.
# For technical reasons, this file is *NOT* reloaded automatically when you use
# `jekyll serve`. If you change this file, please restart the server process.

# Site Settings
locale                   : "en-US"
title                    : "Your Name / Site Title"
title_separator          : "-"
name                     : &name "Your Name"
description              : &description "personal description"
url                      : https://academicpages.github.io # the base hostname & protocol for your site e.g. "https://mmistakes.github.io"
baseurl                  : "" # the subpath of your site, e.g. "/blog"
repository               : "academicpages/academicpages.github.io"
```

For this particular template, this is where you change your name, description, and links to social media outlets that appears as icons at the footer of each page of the website. You can include your email address, Twitter handle, LinkedIn profile, etc. For example, here is [my version](https://github.com/elizabethmcd/elizabethmcd.github.io/blob/master/_config.yml) of the `_config.yml` file for my Academic Pages website.

Since this is most likely a professional website, you will probably want to add separate pages or "tabs" describing yourself and your research. In this template, new "tabs" or separate pages are created by adding a new Markdown file in the `_pages` directory. `cd` into the `pages` directory, and you should see this: 

```
404.md                         markdown.md                    tag-archive.html
about.md                       non-menu-page.md               talkmap.html
archive-layout-with-content.md page-archive.html              talks.html
category-archive.html          portfolio.html                 teaching.html
collection-archive.html        publications.md                terms.md
cv.md                          sitemap.md                     year-archive.html
```

You can create new markdown files in a text editor. If you are unfamiliar with Markdown, here is a good [cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet). With markdown, you can add links, images, and simple formatting changes such as **bold**, _italices_ and headers. You can take a quick look at the Markdown cheatsheet to see how easy it is to create documents with Markdown. 

To then render your newly created markdown pages as tabs on your website page, you need to include them in the `data/navigation.yml` file. `cd` into the `data` directory and open the `navigation.yml` file. It should look like this:

```
# main links links
main:
  - title: "Publications"
    url: /publications/

  - title: "Talks"
    url: /talks/

  - title: "Teaching"
    url: /teaching/

  - title: "Portfolio"
    url: /portfolio/

  - title: "Blog Posts"
    url: /year-archive/

  - title: "CV"
    url: /cv/

  - title: "Guide"
    url: /markdown/
```

You may or may not want to follow the template given by Academic Pages. On [my webiste](https://elizabethmcd.github.io/), I have tabs for my research, blog, and CV in addition to my "About Me" page. Therefore my `navigation.yml` file looks like this:

```
# main links links
main:
  - title: "Research"
    url: /research/

  - title: "Blog"
    url: /year-archive/

  - title: "CV"
    url: https://github.com/elizabethmcd/cv/blob/master/EAM-CV.pdf
```

The format here is that the text between the `/` needs to match the name of the Markdown file in the `_pages` directory. This holds for all markdown pages except for a blog, which needs to stay as the `/year-archive` setup. You will notice that instead of creating a new page for my CV, I just link to the PDF of my CV hosted on Github. You can do this with any link, such as creating a `Publications` tab with a link to your Google Scholar profile. 

You can also use your GitHub pages website to make a blog. I currently write a (poorly maintained) blog where I sparsely talk about issues in science, summarize a workshop I helped with, or describe a conference I went to. Most Jekyll templates allow for you to create a blog powered by Markdown. This is really great because you are getting started with a website and a blog without having to know HTML/CSS. 

In the `images` directory, you can add .png or .jpg files to then add on any of your pages or blog posts. This is referenced with the following Markdown language: 

```
![](../images/file.png)
```

You can also link to an image using a web address. 

The Academic Pages theme allows for creating a blog within your website. To make a new blog post, `cd` into the `_posts` directory. Here you will find example Markdown files. Open it in a text editor. The top part of the blog post with _must_ be present at the beginning of each blog post for it to render correctly. Every webpage template will have different formatting requirements, so make sure to view the example files before creating your own. With Markdown, you can have tables, images, and code blocks in your blog posts if you wish. 

Once you are satisfied with your changes, you `add` and `commit` changes through git just as you would with any other repository, for example the steps: 

```
git add --all
git commit -m "initializing personalized website"
git push origin master
```

The changes should then render at `_yourusername_.github.io`. 



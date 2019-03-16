---
title: Editing your Website from within GitHub
teaching: 10
exercises: 0
questions:
- "How can I edit my website within GitHub?"
objectives:
- "Show how to make changes to a website within GitHub"
keypoints:
- "Make changes to your website directly within GitHub."
---

Instead of using git to add, commit, and push changes to your website and view the changes with Jekyll, you can also make changes directly within GitHub. Go to the repository on GitHub that has your website, the repository named **yourusername.github.io**. Click on the `_config.yml` file that we have been working on previously with our personalized information. Click on the pencil icon:

![](../fig/pencil-icon.png)

This will show you the raw file just like you saw in the text editor:

![](../fig/raw-file.png)

Here I have made a change in the form of a comment, which won't change the rendered file, but just to show what making a change does:

![](../fig/file-change.png)

After you are satisfied with your changes, scroll to the bottom of the page. A green "commit changes" button will become available when you have altered the file. Give the comment a brief name and description that describes what you did to change the file:

![](../fig/commit-button.png)

This is essentially the same process as using git in the command line. However, you can only work on one file at a time, which leads to more commits, and more individual renderings of your website. You also can't view the changes before you commit, which you do with the Jekyll generator in the command line. However, if you are making a quick change and don't want to deal withe command line, this is a suitable option. 

We can also take a look at the breadth of available [Jekyll Templates](http://jekyllthemes.org/), and how each one implements the same elements that we have shown throughout this workshop. 
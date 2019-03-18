---
title: Viewing Changes Locally with Jekyll
teaching: 10
exercises: 0
questions:
- "How can I view my changes locally"
objectives:
- "View modifications to website template locally with Jekyll"
keypoints:
- "View changes to template before committing and pushing to Github"
---

When making lots of changes to our github website, we might want to view the modified changes locally instead of pushing the committed changes to github and waiting for the new changes to render online to then see what the changes look like. As we said before, Github Pages hosts the page, but all of the power under the hood to render the page is done with Jekyll. Jekyll provides a nice solution for viewing changes through a local server. 

[Jekyll](https://jekyllrb.com/docs/installation/) is a Ruby gem, and can be installed on most systems. To install Jekyll, you will need to have Ruby installed, and the gem bundler. For most macOS systems, Ruby comes with your OS by default. You may need to update the system, or change the way gems are configured for your system. [Homebrew](https://brew.sh/) is a nice package manager for macOS, and can be used to update Ruby/gems. To install Jekyll, follow the instructions [here](https://jekyllrb.com/docs/installation/) for your specific operating system. Oftentimes errors will occur because of how Ruby/gems were installed for your system, and you can look at previous issues [here](https://github.com/jekyll/jekyll/issues). 

After you have installed Jekyll, type in the command `jekyll serve` and something like this should appear in your terminal:  

```
Configuration file: /Users/emcdaniel/Desktop/UWMad/ComBEE/2019-03-20-GHpages-workshop/_config.yml
            Source: /Users/emcdaniel/Desktop/UWMad/ComBEE/2019-03-20-GHpages-workshop
       Destination: /Users/emcdaniel/Desktop/UWMad/ComBEE/2019-03-20-GHpages-workshop/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
                    done in 0.569 seconds.
/usr/local/lib/ruby/gems/2.4.0/gems/rb-fsevent-0.10.3/lib/rb-fsevent/fsevent.rb:140: warning: Insecure world writable dir /Users/emcdaniel in PATH, mode 040777
 Auto-regeneration: enabled for '/Users/emcdaniel/Desktop/UWMad/ComBEE/2019-03-20-GHpages-workshop'
    Server address: http://127.0.0.1:4000
  Server running... press ctrl-c to stop.
```

Copy and paste the server address into your browser. You should now see the changes you made or any problems without committing the changes to Github. 

Once you are satisfied with the changes you have made and viewed with `jekyll serve`, you are ready to add, commit, and push to GitHub using the tools you learned in the first half of the workshop. Once you have pushed to your GitHub repository, it might take some time before your changes appear at **yourusername.github.io.**

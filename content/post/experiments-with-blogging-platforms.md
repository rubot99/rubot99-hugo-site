+++
tags = ["blogging","hugo","wercker","jekyll","github"]
categories = ["blogging","github","hugo"]
date = "2017-03-04T16:00:00Z"
title = "Experiments with Blogging Platforms"
keywords = ["tech", "blog", "hugo", "wercker", "github", "wordpress.com"]

+++

When I first decided to blog, I investigated a few platforms. I wanted something that allowed me to

* Create posts easily
* Flexibility with theme and other advanced features
* Low cost/Free

<!--more-->

After investigating, I settled with WordPress.com , it had all the features that I was looking for from a blogging platform and more. I used WordPress.com for about two years, then got a bit busy with other stuff and slowly stopped blogging all together.
This year I decided that I should get back into blogging and one of my resolutions for the year is to write a minimum of 12 blog posts. So this post is the first of my posts, so one down and eleven to go.

#### Revisit current setup

To kick start blogging, I decided to look at other blogging platforms and make some changes to my current blog. I found that I wasn’t really using all the features I got with WordPress.com. I had heard of Ghost and was looking at that platform. I liked the clean minimalist look of most of the Ghost themes and was interested in using markdown to write my posts. While investigating the Ghost platform and hosting options, I came across GitHub pages and Jekyll.

{{< figure src="/images/wordpressBlog.jpg" title="rubot blog" >}}

#### GitHub Pages and Jekyll

So I started investigating GitHub user pages, the thought of having a github.io domain sounded really interesting and using the same tools & processes that I use to develop for blogging was appealing. Being a Windows user, I had few problems running my Jekyll site on my machine. I finally decided to just fork a theme and gave up on running the site locally. I did have a few problems with some of themes I forked. After looking at few themes, I finally settled on the ‘minimal mistakes’ theme, it worked really well, had a clean design and good documentation.

{{< figure src="/images/jekyll.jpg" title="Jekyll static site generator" >}}

#### GitHub Pages and Hugo

So after building the blog using Jekyll, I was doing some research and came across Hugo. Hugo is a static site generator and I decided to play around with it. Hugo is a cross platform application and coupled with the good documentation it was very easy to get started using Hugo. I selected a theme and got building a Hugo site. Once I built the Hugo site, I started looking at deploying my site to GitHub user pages. The Hugo documentation has a tutorial on building and deploying your site using a tool called Wercker. Wercker is a CI tool and it was really easy to get it all set up.

{{< figure src="/images/hugo.jpg" title="Hugo static site generator" >}}

#### The Process

So after all the investigation and testing, I finally settled on using Hugo to build my site and Wercker to deploy the site to my GitHub user pages. I’ve got two repositories my user pages repo that holds the generated files and a repo to hold the site code. As soon as I commit and push changes to my site, Wercker will build the site and deploy the generated site to my user pages repo. I will agree it seems a lot of work for publishing a post, but as a developer this process is second nature to the way I work on a daily basis. Also through all the testing I’ve got to use Visual Studio Code, Atom and Git Kraken.

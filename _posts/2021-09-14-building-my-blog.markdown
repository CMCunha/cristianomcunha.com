---
layout: post
title:  "Building my blog"
date:   2021-09-14 16:00:00 +0100
img: lauren-mancke-aOC7TSLb1o8-unsplash.jpg
categories: blog
published: true
---
I though that there will not be a better first entry for my blog than to share the process I went through to decide to have a blog and to actually build it!

I have some years of experience in Testing and Infrastructure areas and with that accumulated knowledge that I think can be usefull to others, and the need to keep it alive, meaning that I will be writting recurrently, will be a challenge that I'm excited about (let's see how long it will last :) ).

On another hand, it will help me organize my ideas and verbalize those in a way that is appealing (or I hope so) to someone else, fear not I'm not searching for fame and fortune but trying to help someone else, like me, that could have doubts about start writting.

## Decision
I was thinking for a while that I wanted to start sharing my ideas and views over the areas I'm passionated about but it seems I never had the time, or at least I was convincing myself that it was the truth.

What changed now? Well, I'm older and my experience of life taugh me that if you want something you cannot wait to have the perfect conditions to achieve it or else you will never reach it. It is true for life, I went trough the same questions about having kids (wanted to focus on my career, having the perfect house, personal time for hobbies, etc) and once I decided (another positive aspect of having a blog is that it's your version of the story, my wife may have a different view) to go for it everything kinda of falled into place. At least I compromised for small victories towards my "perfect" end goal (being exposed to agile for so long may have trigger this behavior, must check later...).

Once the decision was taken I needed to find something to make me accountable to advance with it, my way was to define this year objectives (I actually did it with my wife) we sit and answer the hardest questions for the year: "What do you want to accomplish in your professional career?" followed by "What will you do to achieve it" and the same for the personal area...that as made me think of broader goals and how to actually reach those in small increments.

Anyone feels that this is a mix of mindmaps and OKRs, or is it just me?

Summing up, the decision was taken and I defined a date and key objectives that are measurable (here I go again...). So what was missing was the plan to advance with it?
- [x] Decision
- [x] Accountability
- [ ] How?

How do I want my blog to look...how would I update the articles...what the frequency of the articles....how to advertise it?

One thing was clear, I do not want to edit text in a fancy editor and apply styles to it, I want to focus in writting and take advantage of my day to day knowledge (development, automation, etc), so I want something practical that will allow me to push new articles like it was code, validate the changes somehow and also the ability to make it look good....hummmmmm

## Technology and Tooling
Basically I want to be able to push new articles like code in daily bases, it will be pretty much a static site with adition of new entries on monthly bases (frequency - check), I want to be able to test the changes before going to "production" and the endpoint must be recognizable or at least easily remindable, not some weird endpoint.

Wordpress type of blogs were out of the question, so I started to search for static site generators that could be linked to GitHub (where I want the articles to live), markdown looked appropriate also, so I started searching for this combination and found [Jekyll][Jekyll-link] and [GitHub pages][githubpages-link].

[Jekyll][Jekyll-link] has no admin interface, only source files that you can build using a CLI (command line interface) to create a static website. It allow you to write you blog posts using [Markdown][markdown-link] and offers the option, if you host your website using [GitHub pages][githubpages-link], to commit your changes, in my case blog post entries.

### Jekyll
Let me share my experience with [Jekyll][Jekyll-link], the documentation to get started is very good and I end up having the default site (using [minima][minima-link] theme) running in my machine in no time.

It is in fact simple, no database to handle or anything like that, it uses [Markdown][markdown-link] so allows me to focus in the writting instead of how it looks, nevertheless we can use pre-defined themes to apply some style to your blog or even create your own (beware that if you go down that route you may encounter difficulties in integrating with [GitHub pages][githubpages-link] because it only supports predefined [themes][theme-link] or at least the ones present in [GitHub][github-link]). It is blog-aware allowing Permalinks, categories, pages, posts and custom layouts.

After following the instructions in [Jekyll][Jekyll-link] I manage to have the default site running locally, one of the nit things about it is that it allows me to check the look and feel in my machine before pushing it. 

The command available for that is:

```bash
jekyll serve
```

That will build and serve your blog in your machine under localhost, as you see from the output of the command:
```bash
Configuration file: /Users/cristianocunha/Documents/Projects/Personal/blog/cristianomcunha.com/_config.yml
            Source: /Users/cristianocunha/Documents/Projects/Personal/blog/cristianomcunha.com
       Destination: /Users/cristianocunha/Documents/Projects/Personal/blog/cristianomcunha.com/_site
 Incremental build: disabled. Enable with --incremental
      Generating... 
       Jekyll Feed: Generating feed for posts
                    done in 0.132 seconds.
 Auto-regeneration: enabled for '/Users/cristianocunha/Documents/Projects/Personal/blog/cristianomcunha.com'
    Server address: http://127.0.0.1:4000
  Server running... press ctrl-c to stop.
```

This will allow us to check the changes locally before posting to production.

I wanted something where I would not be allways caring about the looks of it but I wanted, at least, to choose the look of it, and the default one did not resonate with me so I decided to search for another theme, the one that stroke my eye was [flexyble-jekyll][flexyble-jekyll-link], clean, simple...let's go.

Of course changing themes is also documented, so I will invest in documenting here again, instead I will only post some tips that I struggle to find to have everything working.

#### Tips
##### Base URL
I wanted my blog to be accessible from the root of my endpoint so I had to remove the baseurl entry from the _config.xml file.
Go ahead and remove or comment the following line:
```yaml
baseurl: from _config.xml
```

##### Theme
On the same file, _config.xml, I also needed to change the theme name to the theme I choosen, in order to be applied to my site, so I updated the following line also:

```yaml
remote_theme: artemsheludko/flexible-jekyll in _config.xml
```

##### Dependencies
This new theme brought new dependencies that needed to be downloaded in order to work properly, so I add to add those to the GemFile
add dependencies to GemFile

##### Front Matter
All the of the files that have a YAML [Front Matter][frontmatter-link] block will be processed by [Jekyll][Jekyll-link] as a special file. 
This allows a series of metada to be added to the file that will add valuable information or behavior to the blog, for instance the "published" variable will define if the entry is publicly visible or not.

```yaml
 - published: false
 ```

This allows the editor to add articles to the repository without publishing those and when the article is ready its just a matter to change the value to true and voilá.

##### File Name Structure
All of the article files will follow a file name structure that will allow you, in conjunction with other special entries of [Front Matter][frontmatter-link] to define a release date for the article (yes for those that have things ready weeks in advance...).
The filename structure is

```
YEAR-MONTH-DAY-title.MARKUP
```

Defining the year, month and day of when you want to publish the article and it's title.
For me it will become really handy as I can organize myself and only published what I want, when I want and also keep my work safe and accessible everywhere instead of depdending on one computer.

### Source Control
Once you have everything working in your machine it's time to push it to GitHub (actually you should start by this in order to have all your work saved in the  repository and accessible remotely but you get the point). 
For that create a new project in GitHub and push your code there.

It is that easy because the founder of [Jekyll][Jekyll-link] is in fact the co-founder of [GitHub][github-link] [Tom Preston-Werner][tompreston-link].

Then you need to configure the [GitHub Pages][githubpages-link], that in fact are already a a static website hosting service that enables you to host a static website directly from a public [GitHub][github-link] repository, by default when you activete it it will make your static site available at your your user name plus `.github.io`, so for me it will be `cmcunha.github.io`.

![GitHub Pages Configuration](/assets/img/githubpages_conf.png)


### DNS
Of course my blog could be available trough the default [GitHub pages][githubpages-link] link associated with it but I wanted to go a little further and actually access my blog through: `cristianomcunha.com`, so I bought that domain on GoDaddy platform and redirect it to the [GitHub pages][githubpages-link] of my blog.

All done!

Now that all of this is done let's get writting.....

See you on my next article ;)


[jekyll-link]: https://jekyllrb.com/
[githubpages-link]: https://pages.github.com/
[markdown-link]: https://www.markdownguide.org/
[theme-link]: https://pages.github.com/themes/
[github-link]: https://github.com/
[minima-link]: https://github.com/jekyll/minima
[flexyble-jekyll-link]: https://github.com/artemsheludko/flexible-jekyll
[frontmatter-link]: [https://jekyllrb.com/docs/front-matter/]
[tompreston-link]: [https://tom.preston-werner.com/]

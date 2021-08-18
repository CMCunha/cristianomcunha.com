---
layout: post
title:  "Building my blog"
date:   2021-08-17 16:00:00 +0100
img: lauren-mancke-aOC7TSLb1o8-unsplash.jpg
categories: blog
published: false
---
I though that there will not be a better first entry for my blog than to share the process I went through to decide to have a blog and to actually build it!

I have some years of experience in Testing and Infrastructure areas and with that accumulated knowledge that I think can be usefull to others, and also writting recurrently will be a challenge that I'm exited about (let's see how long it will last :) ).
On another hand, it will help me organize my ideas and verbalize those in a way that is appealing (or I hope so) to someone else, fear not I'm not searching for fame and fortune but trying to help someone esle, like me, that could have doubts about start writting.

## Decision
I was thinking for a while that I wanted to start sharing my ideas and views over the areas I'm passionated about but it seems I never had the time, or at least I was convincing myself that it was the truth.

What changed now? Well, I'm older and my experience of life taugh me that if you want something you cannot wait to have the perfect conditions to achieve it or else you will never reach it. It is true for life, I went trough the same questions about having kids (want to focus on my career, not the perfect house, not enough time, etc) and once I decided (Another positive aspect of having a blog is that it's your version of the story, my wife may have a different view) to go for it everything kinda of falled into place. At least we compromised for small victories towards our "perfect" end goal (being exposed to agile for so long may have trigger this behavior, must check later...).

Once the decision was taken I needed to find something to make me accountable to advance with it, my way was to define this year objectives (I actually did it with my wife) we sit and answer the hardest questions for the year: "What do you want to accomplish in your professional career?" followed by "What will you do to achieve it" and the same for the personal area...that as made me think of broader goals and how to actually reach those in small increments.

Anyone feels that this is a mix of Agile and OKRs, or is it just me?

- [x] Decision
- [x] Accountability
- [ ] How?

Now let's think on the how, how do I want my blog to look...how would I update the articles...

One thing was clear, I do not want to edit text in a fancy editor and apply styles to it, I want to focus in writting and take advantage of my day to day knowledge (development, automation, etc), so I want something practical that will allow me to push new articles like it was code, validate the changes somehow and also the ability to make it look good....hummmmmm

## Technology and Tooling
Basically I want to be able to push new articles like code in daily bases, it will be pretty much a static site with adition of new entries on monthly bases, I want to be able to test the changes before going to "production" and the access to it must recognizable, not some weird endpoint.

Wordpress type of blogs were out of the question, so I started to search for static site generators that could be linked to GitHub (where I want the articles to live), markdown looked appropriate also, so I started searching for this combination and found [Jekyll][Jekyll-link] and [GitHub pages][githubpages-link].

[Jekyll][Jekyll-link] has no admin interface, only source files that you can build using a CLI (command line interface) to create a static website. It allow you to write you blog posts using [Markdown][markdown-link] and offers the option, if you host your website using [GitHub pages][githubpages-link], to commit your changes, in my case blog post entries.

### Jekyll
Let me share my experience with [Jekyll][Jekyll-link], the documentation to get started is very good and I end up having the default site (using [minima][minima-link] theme) running in my machine in no time.

It is in fact simple, no database to handle or anything like that, it uses [Markdown][markdown-link] so allows me to focus in the writting instead of special styles, nevertheless we can use pre-defined themes to apply some style to your blog or even create your own (beaware that if you down that route you may encounter difficulties in integrating with [GitHub pages][githubpages-link] because it only supports predefined [themes][theme-link] or at least the ones present in [GitHub][github-link]). It is blog-aware allowing Permalinks, categories, pages, posts and custom layouts.



### Source Control


### DNS
Of course my blog could be available trough the default [GitHub pages][githubpages-link] link associated with it but I wanted to go a little further and actually access my blog through: cristianomcunha.com, so I bought that domain on GoDaddy platform and redirect it to the [GitHub pages][githubpages-link] of my blog.

A records pointing to githubpages ips
NS entries pointing to cmcunha.github.io


[jekyll-link]: https://jekyllrb.com/
[githubpages-link]: https://pages.github.com/
[markdown-link]: https://www.markdownguide.org/
[theme-link]: https://pages.github.com/themes/
[github-link]: https://github.com/
[minima-link]: https://github.com/jekyll/minima

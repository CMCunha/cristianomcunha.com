---
layout: post
title:  "Building my blog"
date:   2021-08-17 16:00:00 +0100
img: lauren-mancke-aOC7TSLb1o8-unsplash.jpg
categories: blog
---
I though that there will not be a better first entry for my blog than to share the process I went through to decide to have a blog and to actually build it!

I have some years of experience in Testing and Infrastructure areas and with that accumulated knowledge that I think can be usefull to others, and also writting recurrently will be a challenge that I'm exited about (let's see how long it will last :) ).
On another hand, it will help me organize my ideas and verbalize those in a way that is appealing (or I hope so) to someone else, fear not I'm not searching for fame and fortune but trying to help someone esle, like me, that could have doubts about start writting.

## Decision
I was thinking for a while that I wanted to start sharing my ideas and views over the areas I'm passionated about but it seems I never had the time, or at least I was convincing myself that it was the truth.

What changed now? Well, I'm older and my experience of life taugh me that if you want something you cannot wait to have the perfect conditions to achieve it or else you will never reach it. It is true for life, I went trough the same questions about having kids (want to focus on my career, not the perfect house, not enough time, etc) and once I decided (Another positive aspect of having a blog is that it's your version of the story, my wife may have a different view) to go for it everything kinda of falled into place. At least we compromised for small victories towards our "perfect" end goal (being exposed to agile for so long may have trigger this behavior, must check later...).

Once the decision was taken I needed to find something to make me accountable to advance with it, my way was to define this year objectives (I actually did it with my wife) we sit and answer the hardest questions for the year: "What do you want to accomplish in your professional career?" followed by "What will you do to achieve it" and the same for the personal area...that as made me think of broader goals and how to actually reach those in small increments.

Anyone feels that this is a mix of Agile and OKRs, or is it just me?

Decision - Done 

Accountability - Done

Now let's think on the how, how do I want my blog to look...how would I update the articles...

One thing was clear, I do not want to edit text in a fancy editor and apply styles to it, I want to focus in writting and take advantage of my day to day knowledge (development, automation, etc), so I want something practical that will allow me to push new articles like it was code, validate the changes somehow and also the ability to make it look good....hummmmmm

## Technology and Tooling
Basically I want to be able to push new articles like code in daily bases, it will be pretty much a static site with adition of new entries on monthly bases, I want to be able to test the changes before going to "production" and the access to it must recognizable, not some weird endpoint.

Wordpress type of blogs were out of the question, so I started to search for statis site generators that could be linked to GitHub (where I want the articles to live), markdown looked appropriate also, so I started searching for such combination and found [Jekyll][Jekyll-link] and [GitHub pages][githubpages-link].

[Jekyll][Jekyll-link] has no admin interface, only source files that you can build using a CLI (command line interface) to create a static website. It allow you to write you blog posts using [Markdown][markdown-link] and offers the option, if you host your website using [GitHub pages][githubpages-link], to commit your changes, in my case blog post entries.


[jekyll-link]: https://jekyllrb.com/
[githubpages-link]: https://pages.github.com/
[markdown-link]: https://www.markdownguide.org/

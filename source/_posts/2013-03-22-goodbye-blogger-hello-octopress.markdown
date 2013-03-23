---
layout: post
title: "Goodbye Blogger, Hello Octopress!"
date: 2013-03-22 22:47
comments: true
categories:
- Technology 
---
The recent [Google Reader fiasco](http://ialja.com/post/45336943328/hitler-finds-out-google-reader-is-shutting-down) reminded me of something I've been too lazy to take care of for too long: my blog, which I started back in 2006, was still being hosted on Google's Blogger. Now here's a question for you: how long before Google decides all blogging should be done on Google+? Ridiculous question? I don't know. I don't feel like taking chances with Google anymore. But what are the alternatives?

{% img /images/uploads/blogger-to-octopress.png %}
<!-- more -->

## When WordPress feels like an overkill 

[WordPress](https://wordpress.com) was an obvious answer. I love WordPress. It's really powerful and it's what we use over at [Mobitel Tehnik](http://tehnik.mobitel.si). But is it really what my small blog, where I probably know most readers by name, needs?

Not to mention that "WordPress" isn't such a clear answer. You can decide to [self-host WordPress](http://wordpress.org), which is something I'm way too lazy to do. I don't want to deal with databases, with updates (I'm way too likely to click "Remind me later") and all that stuff. 

A [free wordpress.com](https://wordpress.com) blog wasn't a good answer either as I wanted to use a custom domain and have some customization options. After all, what's the point of WordPress if you can't have your own plugins? 

That leaves paying someone else to do all the work of hosting and maintaining WordPress for me. While I fully support paying people for their trouble, I was again wondering if this little blog of mine is worth it. On bad years, I barely write more than 10 posts total! And I don't really need things like scheduling and countless categories and tags...

## Here come GitHub Pages and Octopress!

And while I was pondering the big questions of life and my future blog hosting needs, I stumbled upon [Octopress](http://octopress.org), which defines itself as a "blogging framework for hackers". I don't really define myself as a hacker, but the proposition was tempting: Octopress is an easier way to set up [Jekyll](https://github.com/mojombo/jekyll), "the blog aware static site generator powering [Github Pages](http://pages.github.com)". I started playing with GitHub Pages recently and immediately fell in love with how easy and fast is to host static HTML files there. 

So, Octopress is free, can be hosted on GitHub Pages, is super fast because it's all static in the end, it's totally customizable, and even has plugins? Sounds good, let's give it a try!

Thanks to my recent [Rails Girls adventures](/2013/03/lessons-learned-from-rails-girls-and.html), my MacBook Pro was already equipped with Ruby and Git, which made the Octopress really easy to [setup](http://octopress.org/docs/setup/). [Deploying](http://octopress.org/docs/deploying/) the blog was also relatively easy with GitHub Pages, and before I knew it, I already had my new subdomain blog.ialja.com pointing to my Octopress blog.

## The challenges and joys of having a geeky blog 

I'm not saying this is something I recommend to everyone. I'm still finding my way around the command-line, as it hasn't really been part of my usual workflow until now. But that's precisely the point for me. **I'm teaching myself something new** and I don't ever remember having so much fun (and little frustrations) while setting up a blog!

The tricky part was moving my posts to Blogger from Octopress. Why did I want that, why not just start fresh? Because I wanted a relatively future proof backup that I can control. It's not just on GitHub for everyone to explore, it's also on my hard drive in nicely organized files. I even got the chance to clean up the mess that was my Blogger tags; I now use only 4 basic categories, everything else will be found with search.

I was surprised to find out that getting the content out from Blogger was pretty easy - hit Export and you get one big XML file. The [import script for Octopress](https://gist.github.com/juniorz/1564581) was also easy to use once I got all the gems properly installed. Sure, the gems part got a bit tricky, but not impossible thanks to my new favorite website [Stack Overflow](http://stackoverflow.com).

And then I started playing with the import script. For that I had to pretend to speak Ruby (again, Stack Overflow plus the Ruby Documentation to the rescue). There are two main things I added to the script: 
- custom permalinks for imported blog posts that mirror those on the original Blogger blog and 
- information about where the blog post was originally published that I added at the end of each blog post. 

Because I'm too lazy to go through every post to make sure it looks ok, I decided to keep the old Blogger blog alive as a reference. I don't really have any meaningful SEO to obsess about, so I decided not to worry about redirects, I'll just add a simple disclaimer about the new location on the old blog.

I held my breath while I committed the update with imported Blogger posts, but everything seems to be working just fine. The final piece of the puzzle was migrating Disqus comments, which couldn't be easier. Thanks to my foresight of perfectly mapping the links of old Blogger posts to new ones on Octopress, it literally took a few clicks for Disqus to take care of everything. Pure magic!

## A happy ending? Maybe.

And so, here we are now. I am writing this blog post in Markdown in my beloved iA Writer, where all my blog drafts are made anyway. And when I'll be happy with the text, I'll fire up my Terminal, rake deploy, git commit and all that stuff, and you'll be served this page from GitHub pages. Totally geeky. And for the record, I just want to say that I love the internet and all the good folks that wrote all the wonderful open source software that made this moment possible for me. 

If you've got any questions about the transition, let me know. Otherwise I hope you'll enjoy the new place as much as I do. I know it isn't very pretty yet. I still have to start poking around the design drawer, so I promise it will also get better looking in time. 


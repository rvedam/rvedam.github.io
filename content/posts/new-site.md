---
title: "New Site Layout"
date: 2021-05-31T14:18:46-06:00
---

Hello blogosphere! Sorry for the long delay 3 year gap from my last post.
After a long break during which I completed graduate school as well as 
starting a couple of other study groups for Atlanta Functional Programming, 
I decided to get back into the blogging game. During this time, looking at
my current blog site and process to publishing new content, I decided to 
first update my site and its layout. Last time I set up the site, I went through
the following technologies to pick one that would be right for the site:

* Hugo (written in Go)
* Jekyll (written in Ruby)
* Hakyll (written in Haskell)
* Coleslaw (written in Common Lisp)

At the time, since Hugo was fairly young at the time and being interested in 
writing a project in Common Lisp, I decided to use Coleslaw and I set up a 
process where I had one repository for my Common Lisp site and I had a shell 
script which built the site and ultimately copied the final results into what
was ultimately published on lambdajunkie. Since then 3 year gap, the process for
developing the site using Coleslaw stayed relatively stable, albeit somewhat 
cumbersome. Wanting to concentrate more on writing content than static site 
development I decided to go back this time around and re-evaluate the above list
to see if anything has changed during the last 3 years. My requirements for 
using a static site generator were simple (much more than what most projects):

* Easy to generate pages (ideally using Markdown as it had some niceties for content
  publishing, mainly in the realm of code highlighting and there abouts)
* Must be able to integrate well with Github pages
* If at all possible, had to be able to use Github actions to setup the final site
  and subsequently post it to a `gh-pages` branch for publication (this is one 
  feature I had to mimic with a shell script when using Coleslaw) or manually if
  necessary.

Coleslaw, which has been stable for a while unfortunately has not been actively 
developed on while the Hugo ecosystem in the last 3 years has blown up significantly
with a lot more themes, basic integrations, better documentation for doing various
advanced things, as well as deployment documentation to run it in various scenarios,
one of which is using Github actions to deploy the static site to Github pages in 
a `gh-pages` branch.

This convinced me that it was time to retire the old CL site and revamp the site 
using Hugo instead using the [hello-friend](https://themes.gohugo.io/hugo-theme-hello-friend/) 
theme. If you or your project requires a simple static site, and you don't want to use
a CMS like WordPress, Hugo is definitely a good way to go! That's it for now. 
Stay tuned for more posts on FP, Lisp and other random ramblings!


---
title: "Web Development in Common Lisp: An Overview"
date: 2024-12-23T21:26:24-05:00
images:
tags:
  - Common Lisp
  - Web Development
  - Caveman
  - Ningle
  - CLOG
---

As we end the 2024 calendar year, I thought I would start a series of blog posts
discussing a topic I feel I've neglected to discuss at length: Web Development 
in Common Lisp. Today, I will begin with:

- Current State (Frameworks, libraries, etc.)
- Beginner Resources

## Current State of Web Development in CL

The Web Development world in Common Lisp has changed significantly since the 
late 1990s. We have many html generators, basic libraries to create REST 
services via web servers such as Hunchentoot or Clack, and everything in 
between. Before embarking on our project journey, I felt it important to first
begin with a quick rundown of the different ways that we can currently use
Common Lisp (from here on I'm abbreviating it as CL) in web development.

### RESTful services

The most obvious way to use CL in web development is to leverage it to write 
RESTful services and APIs. There are many libraries to do this, each with 
differing levels of maturity:

- [restas](https://github.com/archimag/restas) 

This is the first library I personally used to write proper REST services in CL.
The examples on github provide the most obvious uses of it and it's fairly 
straightforward. This leverages Hunchentoot heavily for the server-side routing
of different urls, and as far as I can tell nothing is in the works to get it
working with say Clack (which is newer web server, which I'll get into later).
Still from my basic uses, it looks like the basic necessities to write 
REST services are still present. That said, I haven't seen any clear examples 
of using a security framework say like with ironclad to do authentication and
authorization-based services with this. Additionally, I don't have personal 
experience with writing any services that leverages architectural styles that
leverage something like say OAuth.

- [Hunchentoot](https://github.com/edicl/hunchentoot)

Hunchentoot, as many of you may know, is actually a fully-fledged web-server 
written in CL. It provides a full implementation of HTTP/1.1 along with 
features for persistent connections, use of SSL, etc. In addition to all the
standard features associated with running it as an actual webserver, 
Hunchentoot also provides facilities to write full services on top of it as 
well (although, the implementation will be tied to and must rely on deploying 
with Hunchentoot exclusively). Still this library is actively developed on, 
and is extremely stable from what I can tell so if you just need to write a 
few handlers and want finer control this is an option.

### HTML Generators

There are a plethora of HTML generation libraries in CL to write out your static
content. A few examples are:

- [cl-who](https://github.com/edicl/cl-who/)
- [html-template](https://github.com/edicl/html-template/)
- [djula](https://github.com/mmontone/djula) 

port of Python's Django template engine.

- [spinneret](https://github.com/ruricolist/spinneret)

HTML5 Generator library with a more modern approach to application design. Also, 
includes some support of using parenscript directly via spinneret/ps

### Javascript transpilation

For Javscript transpilation, we have both Parenscript and Paren6 (which I will cover in a 
separate post.

### Lightweight frameworks

- [ningle](https://github.com/fukamachi/ningle)

One of Eitaro Fukamachi's frameworks. This library is a spiritual port of Ruby's 
Sinatra library. The purpose is to provide a bare minimum structure to create fast services
and basic web applications

### Full-Fledged Web Frameworks

Some particular ones I want to highlight is

-[Weblocks](https://40ants.com/weblocks/quickstart.html)

This is probably one of more the venerable frameworks, modeling itself after I 
believe Smalltalk's Seaside framework. This hides a lot of complexities related
to building web applications, but is pretty heavy weight compared to most modern
approaches. Still it's an option if the web application is small and well-defined 
enough to allow you to build everything using this heavy-weight approach.

- [Caveman](https://github.com/fukamachi/caveman)

Another a full fledged framework for writing applications

## Beginner Resources

There are a bunch of beginner resources to help one to not only write web 
applications in CL, but also to deploy them. Naturally, I would highly recommend
the [Common Lisp Cookbook](https://lispcookbook.github.io/cl-cookbook/) because 
it provides not only great simple examples to get you started, but also provides
many ways to deploy your applications and prepare them for scaling (along with 
ways to monitor your web apps using prometheus and grafana)

## Future Work and Conclusions

That's it for Part 1 in this series. While I mainly focused on my experience 
with these libraries from dabbling, I know a lot has changed and continues to 
change for Web Development in CL. Next time I'm hoping to document an project 
so that others can have a documented way of writing a proper HTML5 app so that
they have a starting point with CL as an option.

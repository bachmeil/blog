# Fossil as the Emacs of version control

Everyone knows Git has taken over the world of version control. Even though it suffers from horrendous design issues, Github, Gitlab, and Bitbucket are the tools of choice for the vast majority of the software world, especially open source projects. Many developers aren't even aware that it's possible to use an alternative version control system.

My version control software of choice is Fossil. The starting point for understanding why that's the case is to recognize that *Fossil is not a Git replacement*. Git was created for the development of the Linux kernel. If that's your use case, you won't do better than Git. That's pretty much the opposite of my use case, so the case for me using Git is less obvious.[^1]

[^1]: This should be a footnote, but Commonmark is so limited it doesn't even handle footnotes. It might seem ironic that I claim Fossil is my version control of choice when this very blog post is on Github Pages. The simple answer to that is that Github Pages is not version control, it's a website.]

I prefer to think of Fossil as the Emacs of version control. It provides the core version control tools you'd expect, but that's only a small part of Fossil's functionality, which includes:

- A bug tracker
- A CGI web server that can be used to serve your site over the internet or locally
- A forum for discussions
- A wiki

Everything is stored in an sqlite database. While that's an impressive set of features (I love all of them) none of them are worthy of comparison with Emacs. The reason Fossil is the Emacs of version control is the customization options:

- Full CSS customization.
- Full page rendering customization.
- Ability to query the sqlite database directly.
- The bug tracker is actually a version controlled sqlite database that can be customized to hold and query any data you want.
- CGI extensions let you add arbitrary extensions written in any language.

There's literally nothing you can't do with Fossil. That's very much the same as you get with Emacs.

# Fossil as the Emacs of version control

Everyone knows Git has taken over the world of version control. Even though it suffers from horrendous design issues, Github, Gitlab, and Bitbucket are the tools of choice for the vast majority of the software world, especially open source projects. Many developers aren't even aware that it's possible to use an alternative version control system.

My version control software of choice is Fossil. The starting point for understanding why that's the case is to recognize that *Fossil is not a Git replacement*. Git was created for the development of the Linux kernel. If that's your use case, you won't do better than Git. That's pretty much the opposite of my use case, so the case for me using Git is less obvious.[^1]

[^1]: It might seem ironic that I claim Fossil is my version control of choice when this very blog post is on Github Pages. The simple answer to that is that Github Pages is not version control, it's a website.

# Why I like Fossil

I think of Fossil as the Emacs of version control. Obviously, being a version control tool, it provides the core version control tools you'd expect. It was created for the development of the SQLite database. Unlike Git, that's not where the features end. Additional functionality out of the box includes

- a bug tracker,
- a CGI web server that can be used to serve your site over the internet or locally,
- a forum for discussions,
- a wiki, and
- technotes, which are notes relevant to the project at a point in time.

Everything is stored in an sqlite database.

# Fossil as Emacs

That's an impressive set of features. I love them all. Nonetheless, the point of Emacs is not the features that are included in a default installation, it's the customization. The reason I said Fossil is the Emacs of version control is because of the customization options:

- Full CSS customization of the project site.
- Almost full page rendering customization.
- The ability to directly query the sqlite database that holds all the project data.
- The bug tracker is in reality a version controlled sqlite database. You can customize that table to hold and query any data you want.
- CGI extensions let you add arbitrary extensions written in any language. My programming language of choice is D. I can write CGI programs and call them from inside my Fossil project.

There's not much you can't do with Fossil. It's in its own league when it comes to version control. Thus, Fossil is the Emacs of version control.

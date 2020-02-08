# HN Discussion of Text File Productivity

A popular topic on Hacker News is text editing and command line tools. A new blog post on the topic hit #1 today: [My productivity app for the past 12 years has been a single .txt file](https://jeffhuang.com/productivity_text_file/) and [the discussion thread that went with it had hundreds of comments](https://news.ycombinator.com/item?id=22276184).

This is an important topic in large part because knowledge work has become a mess. We have a neverending list of things that need to be organized, yet most of us aren't paid to organize, so we resort to a search for good tools to do most of the work for us.

There are tons of apps out there, but they are far from perfect. The list of problems people cite with these apps is long. They have high overhead, your data is locked up and scattered around in different apps, it's hard to customize for your particular workflow, you're at the mercy of VC-funded companies that might jack up prices or make changes that break your workflow, and on and on.

## The HN Approach

The "HN approach", as I would define it, involves minimalism (putting everything in one place and eliminating the overhead associated with storing and querying your information), easy customization for your personal needs, data portability, and reliability. The solutions offered involve a combination of plain text files, text editors, and version control software.

I'm definitely in the HN camp on this one. I can't imagine trying to organize my stuff without plain text files, text editors, and version control. I've tried all the cloud apps, often multiple times, but have always returned to the simple approach. Plain text and the standard Linux command line tools are the only things that have stuck over the past couple decades.

## Additional Thoughts

Fossil is an ideal version control system for this. You can set up a private CGI server that comes with a website and wiki out of the box. It also works just fine on your local machine. There's no need to have a web server if you want to use it on only one computer. You can back up to a USB drive with a simple repo sync.

A few of the options you have with Fossil:

- If you want a cloud approach, you can dump all your notes into a big wiki file. You can access/modify your notes right in the browser. It works perfectly well on a phone, since it's nothing more than html, as opposed to a complicated app.
- If you want to work with your text editor on your local machine and then push, as you'd do with a standard Git or Mercurial workflow, you can view your files online (markdown files are rendered out of the box). If you want to add new notes on mobile using this approach, you'll need to file an issue. A bit of overhead, but still works well.
- Create a new issue for each note. Fossil was created for sqlite development, which means you have all the query power of sqlite for your notes. 
- Use the built-in forum. You can create a new thread for each note. You can search all your notes, but you have the added advantage of coming back later to comment when you have new thoughts. I haven't done much with the Fossil forum, so I can't speak to how practical it would be.

There's nothing new about the "one big text file" approach. It was a big deal about 15 years ago. Unfortunately much of that writing seems to have disappeared from the web. I found a few links that still work:

<http://www.matthewcornell.org/blog/2005/8/21/my-big-arse-text-file-a-poor-mans-wikiblogpim.html>  
<https://www.williamhern.com/living-in-a-single-text-file.html>  
<https://danlucraft.com/blog/2008/04/plain-text-organizer>  
<http://www.43folders.com/node/48424/328537#comment-328537>  
<http://www.43folders.com/2005/08/17/life-inside-one-big-text-file>  

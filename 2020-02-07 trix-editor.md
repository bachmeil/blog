# A Simple Text Editor In The Browser

There was a recent HN link to [an in-browser text editor](https://www.mytextarea.com/).

I have no idea why that site appeals to people. Text editors are abundant and fast, so there's no obvious reason why someone would want to use a plain editor like that, especially [one which isn't entirely private](https://news.ycombinator.com/item?id=22254473). It's apparently [a Hacker News thing](https://news.ycombinator.com/item?id=22253583) that I'd never heard about before.

A commenter asked

> Has anyone built a substantial one like this for their own use?

I don't know what is meant by "substantial", but I did have [an old experiment sitting around](https://gist.github.com/bachmeil/7c19e72b9a5c49a85e8cecb0b7a7f3ca). In only 20 lines of html, you get a full [Trix editor](https://trix-editor.org/) thanks to [the CDN linked on cdnjs](https://cdnjs.com/libraries/trix). It has the following features:

- WYSIWYG editor
- Professional design (by the Basecamp team, not me)
- Ability to save to and load from local storage
- Automatically loads your previous content if you restart your browser
- Autosaves every to local storage every two seconds

If you want an in-browser text editor, you could do a lot worse. It's really cool that I was able to cook the whole thing up in just a few minutes in spite of the fact that I don't know much about web development. All you have to do is copy the twenty lines into an html file and load the file in your browser.

While this is cool, I've really never used it for anything substantial, because it makes more sense to me to use a regular text editor. In a hypothetical world where I wanted to do more with it, I would:

- Add support for attachments. They [have an example](https://trix-editor.org/js/attachments.js) but that's not a five-minute exercise for someone with my limited understanding of Javascript.
- Make it possible to submit the content to a web server.
- Support creation of and working with multiple notes. Basically a poor man's Tiddly Wiki. This really is outside my expertise. If I did this, it would only be for the fun of learning.
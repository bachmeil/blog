# A Theme For Fossil

Fossil provides an awesome set of features relative to other version control systems, the most notable of which is Git. The default theme (skin in Fossil terminology) is not going to win any design awards. That's okay - it's the functionality that matters - but if I'm going to use something as heavily as I use version control, aesthetics start to matter.

Fossil is almost entirely customizable (if you're willing to change the source code, it's completely customizable). I've [posted my modified skin here](https://gist.github.com/bachmeil/597f2aa611b81cda3a4923246072afd0).

The first two replace the default CSS and header. You can find all the information you need about customizing the theme by going to `> Admin > Skins`. Simply copy the gist files into the appropriate text boxes.

Equation support is trickier. You can see how to set up MathJax by looking at the "script.txt" file. Javascript won't execute unless you use the `nonce` trick as I've done there.

If you use the skin I've provided in those three files, you will have MathJax support. Note however that Fossil doesn't know anything about equations. That means you have to do some escaping to get your equations to display properly.

- Use double `\` characters inside equations.
- Leave a space after `_` characters so it doesn't italicize.
- Escape markdown characters like `*` and `_`.

Overall, this is far from perfect. It nonetheless works flawlessly.
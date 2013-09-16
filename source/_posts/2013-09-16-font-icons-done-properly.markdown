---
layout: post
title: "Font icons done properly"
date: 2013-09-16 12:17
comments: false
categories:
---
In my [previous post][0] I went over how little work it took to add a [link
blog][1] feature to Octopress. I also mentioned I decided to use a font icon as
a marker for linklog entries (and in the process I started using it for other
things as well, like the RSS subscription link).

Brandon Mathis picked up my tweet about it and after having a look told me I
wasn't using the font icons properly, and how I could fix that.
<!-- more -->
Due to the fact that RSS readers don't load CSS, they won't load your font
icons, which leads to your preciously hand-picked icon will show up as, well,
no content whatsoever. Furthermore, screen readers will not pick it up, as
there's no content there to be read - a big no-no in terms of accessibility.

Brandon was kind enough to point me to [an article describing the problem in
detail, and how to solve it][2]. The solution, it turns out, is much nicer than
the standard technique used by most of the popular font icon packages, which
tends to be hijacking an obsolete markup element for icon placement.

By using a bit more markup, we get a much more semantical result, and one that
happens to solve both problems. After all was said and done, I ended up with a
site working better and loading quicker than before. Back pats all around!

The relevant SCSS and HMTL markup for this is, in a nutshell:

<script src="https://gist.github.com/pfig/6579409.js"></script>

<script src="https://gist.github.com/pfig/6579358.js"></script>

P.S. While doing this change, I learned about [IcoMoon][3], which is perhaps
the ultimate resource for everything icon font-y, and provides [a tool to build
your own custom-made font package][4], which is great as you probably don't
need the 400 icons that come with your chosen icon font - my current font now
contains only 3 icons, and weighs in at around 4k, a fraction of Font Awesome's
or Foundation's icon sets.

[0]: http://pedrofigueiredo.org/scribbles/2013/09/02/the-link-blog/ "The link blog"
[1]: https://en.wikipedia.org/wiki/Linklog "Wikipedia entry for Linklog"
[2]: http://css-tricks.com/html-for-icon-font-usage/ "HTML for font icon usage"
[3]: http://icomoon.io/ "IcoMoon"
[4]: http://icomoon.io/#docs/app "Mix'n'match your own icon font"

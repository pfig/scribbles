---
layout: post
title: "The link blog"
date: 2013-09-02 06:51
comments: false
categories: meta
external-url: http://daringfireball.net/
---
As everyone knows, [link blogs][1] were invented by Al Gore, and made popular
by [John Gruber][0].
<!-- more -->
I **really, really** wanted to have the same functionality here, but the
Octopress gods were against me: after a lot of pain to merge 2.1 (the branch
with the linklog feature baked in) with my installation, things were broken in
ways my poor Ruby wasn't enough to do anything about, and the same happened
when I tried to upgrade to 3.0 (which hasn't been released yet, so the usual
"provided as is" guarantee applies in its full force).

As a result, I curled up in a corner, and after a bit of wailing and gnashing
of teeth figured out how to implement it myself. The feature can be described as
follows:

* The title of the entry links to the page you're commenting on, as opposed to
that entry's permalink.

* There's some sort of indication (an icon, usually) that an entry is a
linklog.

* You can still find the entry on its own permalink.

I settled on

<center><span style="font-size: 64px;"><i class="foundicon-compass"></i></span></center>

for the icon (from the
[excellent collection of font icons provided by Foundation][2]), but I decided
to make this the link to the external page, and keep the title of the post
linking to its own permalink, to keep it consistent with regular posts.

Other than that, just like in the forthcoming Octopress implementation, I added
an entry to the front matter YAML, <code>external-url</code>:

{% gist 6207330 %}

and then added the following code to my article template, to show the icon with
the link:

{% gist 6207340 %}

As you can see, the only code involved in adding this feature was a [Liquid][3]
conditional. This is one of the reasons why I think [Octopress][4] (or
[Jekyll][5], for that matter, but I'm lazy) can't be beaten for blogging.

[0]: http://daringfireball.net/ "Daring Fireball"
[1]: https://en.wikipedia.org/wiki/Linklog "Wikipedia entry for Linklog"
[2]: http://zurb.com/playground/foundation-icons "Foundation icons"
[3]: http://wiki.shopify.com/Liquid "Liquid docs"
[4]: http://octopress.org/ "Octopress homepage"
[5]: http://jekyllrb.com/ "Jekyll homepage"

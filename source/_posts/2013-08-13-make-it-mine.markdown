---
layout: post
title: "Make it mine"
date: 2013-08-13 14:32
comments: false
categories: meta
---
In the past few days I've been tinkering with the site's look and
functionality, and now that I've finally deployed it (and even tagged it as
v1.0!) I feel a huge weight has been lifted off my shoulders: the weight of all
the features I've crammed in while at the same time making it much more
pleasing to look at, in my opinion.

What follows is a brief summary of all that's gone in this release, and
there'll be a couple of follow-up posts focusing on particular features.
<!-- more -->
# New theme

The first thing I decided to change was the theme, and one of my goals was to
make it more reader-friendly - if you've been paying attention, one of the main
drivers for rebuilding the whole site was [Matt Gemmel's post on designing for
readers][0]. After looking at Matt's site and browsing the [Octopress
themes][1], I decided to go with [a theme developed by Elise Heine][2] for
[5to9 labs][3]. I've mostly left it untouched, apart from a nudge here and
there, as it looks great and is pretty much what I was looking for, looks-wise.

# Features

Once I was happy with the integration I started adding features, some needed to
work around a couple of issues with release 2.0 of Octopress.

* Replace Google Site Search with something else, I went with [Tapir's static
site search service][4].

* I liked Matt's [footnote popovers][5], so added that as well.

* Add a way to manage drafts that actually worked and made it easier to see
what's on the pipeline at a glance.

* Implement linklog posts in Octopress 2.0.

Each of these will be detailed in its own follow-up post, and once I'm happy
with the code (mostly small clean ups and removing stale files) I'll make the
repo public.

Stay tuned for Octopress awesomeness!

[0]: http://mattgemmell.com/2013/05/22/designing-blogs-for-readers/ "Designing blogs for readers"
[1]: https://github.com/imathis/octopress/wiki/3rd-Party-Octopress-Themes "Octopress 3rd-party themes"
[2]: https://github.com/elisehein/Pageturner "Pageturner theme"
[3]: http://www.fivetonine.eu/ "5to9labs"
[4]: http://tapirgo.com "Tapir homepage"
[5]: https://github.com/mattgemmell/footnotes-popover "Footnote popovers GitHub repo"

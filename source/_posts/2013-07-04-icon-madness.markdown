---
layout: post
title: "Icon madness"
date: 2013-07-04 11:30
comments: false
categories: webdev
---
Yesterday I turned to setting up real favicons and touch icons for the new site,
and in the process figured out I needed 22 images to support desktop browsers
and the current crop of mobile devices (iOS and Android).

If only there was a resolution-independent image format...
<!-- more -->
A bit of searching led me to [a post by Mathias Bynens which covers pretty much
everything you need to know about favicons][0].

In short, here's what you need if you **really** want to support everything and
the kitchen sink:

* Three icons to combine into a multi-icon file, to support several browsers.

* One icon for Very Old Browsers (tm).

* Ten icons for iOS devices.

* Eight icons for Android devices.

I ended up deciding to ignore Android devices' native icons (that's the sort of
[fanboy][1] I am), as Android seems to be happy with one of the images used for
iOS.

Here's my final markup:

{% gist 5956451 %}

While creating that Gist I noticed that I've been here before:

{% gist 1808188 %}

but I can't be bothered to keep that up to date, so I've been using [Icons][2]
for some time and am happy enough with it.

Now surely I can't be the only one who thinks this is not the best way to go
about this. Why aren't we, as a species, using SVG across the board?

P.S. [Apple's][3] and [Google's][4] guidelines, for completeness' sake.

[0]: http://mathiasbynens.be/notes/touch-icons "Touch icons"
[1]: http://www.marco.org/2012/01/04/fanboy-theory "The Official Fanboy Theory"
[2]: https://itunes.apple.com/gb/app/icons/id413612688?mt=12 "App Store link"
[3]: https://developer.apple.com/library/ios/#documentation/UserExperience/Conceptual/MobileHIG/IconsImages/IconsImages.html "Custom Icon and Image Creation Guidelines"
[4]: https://developer.android.com/design/style/iconography.html "Iconography"

OMGThemes!
==========
A general resource for themes, though currently just for Xcode themes, and we don't intend to support general theming, just theming for developer tools.

The site (http://omgthemes.net) scans the fork tree of this repository for Xcode themes contributions.

So, fork to add new themes.

Currently, we only scan one level deep, so make sure you fork mxcl’s repository. Of course, it would be neat to show forks of forks and thus show how people have potentially modified themes and improved them, so scanning deeper is something we’d like to do.

Currently the site regenerates every five minutes.

The site works by converting themes to CSS and then rendering a template. The code for this is in the `www` branch.

We will recursively look for themes (`.dvtcolortheme` files), this is useful in case you already have a repository that contains themes. You can fork this repository and then force push your existing repository’s git history to your fork. After you can then delete your existing repository and rename your fork of this repository to what your existing repostitory is called so in effect nothing has changed bar linking your repo to this one so our site can find it.

Colorspaces
===========
I have found while building *OMGThemes!* that Xcode renders the themes slightly differently to Safari (and Chrome differently again). My research eventually led me to turning on [ColorFaker](https://github.com/iccir/ColorFaker), which forces your Mac to render everything with a plain RGB profile. At this point Safari and Xcode matched.

Seemingly the problem is that Safari doesn't apply your monitor’s colorspace profile when rendering pages, but Xcode (and every other Mac app) does. And beyond that I’m not sure how to proceed.

TODO
====
* Convert both ways so we can auto-convert to other theme types.
* Follow fork chains for forks and show what variations people have provided.
* Ratings, repo stars aren't enough as repos can contain multiple themes

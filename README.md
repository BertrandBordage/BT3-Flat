Plumage
=======

Plumage is a theme for [Pelican](http://getpelican.com) 3.2, a static site generator written in Python.

I forked the original theme and customised some parts.

![Plumage article view](http://github.com/kdeldycke/plumage/raw/master/plumage-article-screenshot.png)


Features
--------

  * Based on Twitter Bootstrap
  * Project template
  * Tags grouped by tiers
  * External assets (Bootstrap, Jquery, etc...) uses CDN
  * YouTube links
  * Direct link to edit articles on Github
  * Pygments syntax highlighting
  * Post share
  * Post title link


Plugins
-------

Plumage has built-in support for the following plugins:

  * [`neighbors`](https://github.com/getpelican/pelican-plugins/tree/master/neighbors)
  * [`related_posts`](https://github.com/getpelican/pelican-plugins/tree/master/related_posts)
  * [`typogrify`](https://github.com/getpelican/pelican-typogrify)


Settings
--------

Plumage can be customized by adding these optionnal parameters to your `pelicanconf.py` file:

  * `SITE_THUMBNAIL`: Site's thumbnail URL as displayed in the header. Should be a square image of at least 80x80 pixels.
  * `SITE_THUMBNAIL_TEXT`: Text displayed behind site's thumbnail.
  * `SITESUBTITLE`: Set the subtitle from the site's header.
  * `MENUITEMS`: A list of tuples (Title, URL) for additional menu items to appear at the beginning of the main menu.
  * `GOOGLE_SEARCH`: [Google's Custom Search Engine](https://www.google.com/cse/) ID (e.g. `partner-pub-0123456789098765:0123456789`) to activate blog specific search.
  * `LEFT_SIDEBAR`, `RIGHT_SIDEBAR`: HTML content to put as-is in the left or right sidebar.
  * `ARTICLE_EDIT_LINK`: Generate an edit link besides each article. Can use `%(slug)s` to include dynamic article's slug in the link.
  * `PDF_PROCESSOR`: Set this to 'True' if you want to have a 'Download the .pdf' link created, if you are using the PDF plugin.
  * `SOCIAL`: A list of tuples (Title, URL) to appear in the first columns of the footer.
  * `SOCIAL_TITLE`: Overide the title of the first column of the footer. Default value: `Social`.
  * `LINKS`: A list of tuples (Title, URL) for links to appear in the second column of the footer.
  * `LINKS_TITLE`: Overide the title of the second column of the footer. Default value: `Links`.
  * `COPYRIGHT`: Additional copyright statement to add in the third column of the footer.
  * `DISCLAIMER`: Overide the Disclaimer notice that gets displayed at the fourth column of the footer.
  * `DISQUS_SITENAME`: Disqus sitename identifier.
  * `GOOGLE_ANALYTICS`: Google Analytics unique identifier (e.g. `UA-XXXX-YYYY`).
  * `GOOGLE_ANALYTICS_DOMAIN`: Add the `_setDomainName` variable to Google Analytics' Javascript code.
  * 'SHARE_POST': Show share post on the bottom of article or not


Most of these [parameters are similar to `notmyidea`'s](http://docs.getpelican.com/en/latest/settings.html#themes) (Pelican's default theme). For usage example, please have a look into [my own `pelicanconf.py`](https://github.com/kdeldycke/kevin-deldycke-blog/blob/master/pelicanconf.py).

The theme is also sensible to this list of [standard Pelican parameters](http://docs.getpelican.com/en/latest/settings.html):

  * `ARCHIVES_SAVE_AS`
  * `AUTHOR_SAVE_AS`
  * `CATEGORIES_SAVE_AS`
  * `CATEGORY_FEED_ATOM`
  * `CATEGORY_FEED_RSS`
  * `CATEGORY_SAVE_AS`
  * `DEFAULT_LANG`
  * `DEFAULT_PAGINATION`
  * `DISPLAY_PAGES_ON_MENU`
  * `FEED_ALL_ATOM`
  * `FEED_ALL_RSS`
  * `FEED_ATOM`
  * `FEED_DOMAIN`
  * `FEED_RSS`
  * `SITENAME`
  * `SITEURL`
  * `TAG_FEED_ATOM`
  * `TAG_FEED_RSS`
  * `TAGS_SAVE_AS`


TODO
----

  * Hack google search to integrate search result within theme design ?
  * Replace Google custom search by https://swiftype.com/ ? Or better, static search:
      * http://ralsina.com.ar/weblog/posts/standalone-search-in-nikola.html
      * https://news.ycombinator.com/item?id=6958735
  * Use a big carousel for front-page articles (ex: http://twitter.github.com/bootstrap/examples/carousel.html ) + a bit of http://srobbin.com/jquery-plugins/backstretch/ to keep aspect-ratio
  * Check some web-dev essentials:
      * http://webdevchecklist.com/
      * https://github.com/getpelican/pelican-plugins/tree/master/w3c_validate
      * https://github.com/dypsilon/frontend-dev-bookmarks
  * Use custom jinja filters instead of heavy tag soup in my theme ? Example: https://bitbucket.org/sirex/blog/src/32c192ff7a10/pelican.conf.py#cl-53
  * Add progressive image loading. See:
      * https://github.com/vvo/lazyload
      * https://github.com/tuupola/jquery_lazyload
      * https://github.com/luis-almeida/unveil
  * Concatenate and minify CSS and Javascript. See:
      * https://pypi.python.org/pypi/mincss
      * http://ralsina.com.ar/weblog/posts/mincss-is-amazing.html
      * https://pypi.python.org/pypi/pelican-minify
      * https://github.com/getpelican/pelican-plugins/tree/master/assets
  * Inline and embed all CSS in the page ? See: http://www.peterbe.com/plog/100-percent-inline-css
  * Use LESS version of bootstrap for cleaner customizations ?
  * Check and fix style on mobile (especially ugly margins)
  * Look at app-template for code inspiration and ideas:
      *  https://github.com/nprapps/app-template/blob/master/templates/_base.html
      *  https://github.com/nprapps/app-template/blob/master/render_utils.py
  * Make Masonry responsive ? See:
      * http://osvaldas.info/responsive-jquery-masonry-or-pinterest-style-layout
      * http://deanclatworthy.com/2012/09/responsive-twitter-bootstrap-masonry/
      * http://www.maurizioconventi.com/2012/06/19/responsive-example-integrating-twitter-bootstrap-and-jquery-masonry/
  * Add progressive loading on masonery layouts. See: http://masonry.desandro.com/demos/infinite-scroll.html
  * Generate thumbnails in article content. See:
      * https://github.com/getpelican/pelican-plugins/pull/40
      * https://github.com/getpelican/pelican-plugins/pull/43
  * Auto-enhance created thumbnails ? See: https://news.ycombinator.com/item?id=5999201
  * Generate Disqus static comments for SEO ? See: https://github.com/getpelican/pelican-plugins/tree/master/disqus_static
  * Group contiguous images in a post into a tiled galery:
      * as in WordPress' jetpack plugin: https://github.com/crowdfavorite-mirrors/wp-jetpack/tree/master/modules/tiled-gallery
      * or thanks to https://github.com/jakobholmelund/fitpicsjs
  * Replace MGlass zoom icon overlay with pure CSS. Inspirations:
      * Cover effect at http://h5bp.github.io/Effeckt.css/dist/captions.html
      * http://codepen.io/Twikito/pen/Jeaub
      * To center the zoom icon, we can use one of these trick: http://codepen.io/shshaw/full/gEiDt
  * CSS typography: http://www.newnet-soft.com/blog/csstypography
  * Add links to yearly/monthly indexes in archives
  * Upgrade to Bootstrap 3.x
  * Use http://startbootstrap.com/modern-business for first page ?
  * Upgrade to Font Awesome 4.X: http://fontawesome.io/whats-new/
  * Try to paginate monthly and yearly archives
  * Use Font-awesome CDN ? http://blog.fontawesome.io/2013/05/20/get-the-most-out-font-awesome-and-bootstrapcdn/


Changelog
---------

* **2014W7** (2012-12-23)
  * First commit.
  * Share post option. Set SHARE_POST = True to enable share post link on the bottom of article.
  * Add title link. Use 'Link' in meta post make the post title link to external post. Posts with external links will be marked by ❄
  
  ![share post & title link](https://dl.dropboxusercontent.com/u/299446/Sanagi/share%20post%20%26%20title%20link.png)

License
-------

The content of this repository is copyrighted (c) 2012-2014 Ken Lai

This code is free software: you can redistribute it and/or modify it under the
terms of the GNU General Public License as published by the Free Software
Foundation, version 2, or any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY
WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A
PARTICULAR PURPOSE. See the GNU General Public License for more details.

For full details, please see the file named COPYING in the top directory of the
source tree. You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.


Third-party assets
------------------

The theme uses external softwares, scripts, libraries and artworks:

    jQuery MGlass v1.1
    Copyright (c) 2012 Younès El Biache
    Distributed under a MIT license
    Source: https://github.com/younes0/jQuery-MGlass

    Solarized Pygment style v0.1.0
    Copyright (c) 2012 Shoji KUMAGAI
    Distributed under a MIT license
    Source: http://pypi.python.org/pypi/pygments-style-solarized

    Fabric (Plaid)
    Copyright (c) 2012 James Basoo
    Distributed under a Creative Commons Attribution-ShareAlike 3.0 Unported license
    Source: http://subtlepatterns.com/fabric-plaid/

    Cream paper
    Copyright (c) 2012 Devin Holmes
    Distributed under a Creative Commons Attribution-ShareAlike 3.0 Unported license
    Source: http://subtlepatterns.com/cream-paper/

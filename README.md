# static-random-post

I like the random page feature of [Wikipedia](http://www.wikipedia.org/). It allows me to learn about things I would never have learnt otherwise.
The random post feature is similar, allowing you to expose your readers to posts they would not look for themselves, but yet are interesting to them.

Randomness in a static website is a problem. When I moved to [Jekyll](http://jekyllrb.com/), and then [Pelican](http://blog.getpelican.com/), as my blogging platform, I wanted to keep using the random post feature I used to use in [WordPress](http://wordpress.org/). The best solution I found was [enrmarc's](http://enrmarc.github.io/blog/random-post-in-jekyll/), which uses the client's browser ability to produce [(pseudo-)randomness](http://en.wikipedia.org/wiki/Pseudorandom_number_generator) using [JavaScript](http://en.wikipedia.org/wiki/JavaScript).

What I didn't like in enrmarc solution was that a list of all posts was included in each and every one of them. This is *n²* space- (and therefore time- when transmitting the files) [complexity](http://en.wikipedia.org/wiki/Computational_complexity_theory). Boo hoo.

My solution is taking this method and making a single file redirecting to a random post. It has support for Jekyll and Pelican; if you want to add another system, just fork this repository, add whatever you need, and send me a pull request ☺



## How to install

### Pelican

First of all, you might want to know this ability is also provided through a [plugin](https://github.com/getpelican/pelican-plugins/tree/master/random_article).

If you want to use the non-plugin approach:

* Place `pelican.html` in the `templates` subdirectory of your theme.
* Rename it to something more proper, say `random.html`.
* Tell Pelican to use this file by adding `random` to `DIRECT_TEMPLATES` in your `pelicanconf.py`; for example: `DIRECT_TEMPLATES = ('index', 'categories', 'authors', 'archives', 'random')`.
* Now add a link to `YOURSITE/random.html` wherever you want.



### Jekyll

* Create a `random` subdirectory under your Jekyll installation.
* Place `jekyll.html` in that subdirectory, renaming it `index.html`.
* Now add a link to `YOURSITE/random` wherever you want.

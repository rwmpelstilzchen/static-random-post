jekyll-random-post
==================

I like the random page feature of [Wikipedia](http://www.wikipedia.org/). It allows me to learn about things I would never have learnt otherwise.
The random post feature is similar, allowing you to expose your readers to posts they would not look for themselves, but yet are interesting to them.

Randomness in a static website is a problem. When I moved to [Jekyll](http://jekyllrb.com/) as my blogging platform, I wanted to keep using the random post feature I used to use in [WordPress](http://wordpress.org/). The best solution I found was [Enrique Marcos'](http://enrmarc.github.io/blog/random-post-in-jekyll/), which uses the client's browser ability to produce [(pseudo-)randomness](http://en.wikipedia.org/wiki/Pseudorandom_number_generator) using [JavaScript](http://en.wikipedia.org/wiki/JavaScript).

What I didn't like in Marcos' solution was that a list of all posts was included in each and every one of them. This is *n²* space- (and therefore time- when transmitting the files) [complexity](http://en.wikipedia.org/wiki/Computational_complexity_theory). Boo hoo.

My solution is taking this method and making a single page redirecting to a random post.

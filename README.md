This is just a quick little implementation of [Delaunay Triangulation][1] in
JavaScript. It was mostly ported from [Paul Bourke's C implementation][2], but
I referenced some bits from [another JavaScript implementation][3] and rewrote
a bunch of things in ways more amenable to fast JavaScript execution.

[1]: http://en.wikipedia.org/wiki/Delaunay_triangulation
[2]: http://paulbourke.net/papers/triangulate/
[3]: http://www.travellermap.com/tmp/delaunay.htm

Notably, it runs in subquadratic time, making it the fastest JavaScript
implementation of which I'm aware.

This software is released into the public domain.

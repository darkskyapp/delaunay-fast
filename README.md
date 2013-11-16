This is just a quick little implementation of [Delaunay Triangulation][1] in
JavaScript. It was mostly ported from [Paul Bourke's C implementation][2], but
I referenced some bits from [another JavaScript implementation][3] and rewrote
a bunch of things in ways more amenable to fast JavaScript execution.

Essentially, you pass Delaunay.triangulate a list of vertices (which should be
a bunch of two-element arrays, representing 2D Euclidean points), and it will
return you a giant array, arranged in triplets, representing triangles by
indices into the passed array. (This representation is a little bizarre, but
object allocation is too slow for this library's [original use case][4]. Yes,
really.)

[1]: http://en.wikipedia.org/wiki/Delaunay_triangulation
[2]: http://paulbourke.net/papers/triangulate/
[3]: http://www.travellermap.com/tmp/delaunay.htm
[4]: http://forecast.io/

Notably, it runs in subquadratic time, making it the fastest JavaScript
implementation of which I'm aware. (Okay, it doesn't really, but it'd be
trivial to modify to run in subquadratic time, I just havn't done so yet.)

This software is released into the public domain.

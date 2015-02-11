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

License
-------

To the extent possible by law, I have [waived all copyright and related
or neighboring rights][cc0] to this library.

[cc0]: http://creativecommons.org/publicdomain/zero/1.0/

Related
-------

*   [@yahiko00][5] has released a [TypeScript interface][6] that may be useful
    if you are trying to access this library from TypeScript.

[5]: https://github.com/yahiko00
[6]: https://github.com/yahiko00/delaunay

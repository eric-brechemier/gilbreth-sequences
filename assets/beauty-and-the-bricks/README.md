## Beauty and the Bricks

### The Music of the Bricks

![Brick Facade](pictures/brick-facade.jpg)

Brick patterns have fascinated me for a long time.
There is an inner beauty to the rhythm of a plain brick wall,
but with a little color added, it feels like a symphony.
Decorative patterns are commonly found on the facade of
brick houses built from the Victorian era to the 1930s.
They look deceptively simple, yet they present similarities
and variations from facade to facade that make them constantly
escape a growing scrutiny.

### Brick by Brick

![Brick Bond](pictures/brick-bond.jpg)

Let's consider the facade of a typical brick wall.
Apart from the edges, two shapes are repeated endlessly:
a long rectangle called a stretcher, and a small rectangle,
about half shorter, called a header.

The same brick can become either a stretcher or a header.
A stretcher brick turned sideways becomes a header.
Headers give strength to a wall, but they don't come cheap.
Facade bricks are expensive compared to the bricks used
in inner parts of the wall. A header brick covers only half
of the surface of a stretcher brick, and thus costs more.

A row of bricks is called a course. Its height is approximately
one third of the length of a brick. These proportions and the shift
from course to course produce the syncopated rhythm of the bricks.
The economy of the bricks explains the relative rarity of header
bricks, with varying degrees depending on the type of wall.

### Bricks vs Concrete

![Isometric view showing Flemish bond (exterior) and common bond (interior)](pictures/brick-bond-isometric-view.jpg)

The classic novel “Cheaper by the Dozen” tells the story of a
family with twelve kids. The father, Frank B. Gilbreth, wrote
a book called “Bricklaying System”, edited by his wife Lillian,
which I have found invaluable in my study of the bricks.
Both efficiency experts, they were early pioneers of motion study
which they first applied to bricklaying. The book, published in 1909,
describes best practices and innovative methods which allow bricklayers
to lay more bricks faster, with the aim of keeping brickwork competitive
against the growing use of concrete.

### Base Units

![Brick Units](pictures/brick-units.jpg)

The book covers all the aspects of bricklaying, including a rational
description of bonds and decorative patterns. It describes a system of
10 base units, which grow sequentially from a single header brick to
produce larger and larger patterns. From these 10 units, I have inferred
a method which creates the next unit from the previous one, indefinitely.
Copy the center course in reverse order just below. Then insert between the
two center courses a new course which is a half-brick wider. This new center
course shall contain no more than one header, located as close as possible to
the center, or offset in the first available position on the left.

### Mathematical Sequences

```
1
2
12
22
212
222
2122
2222
22122
22222
221222
222222
2221222
2222222
22212222
22222222
222212222
222222222
2222122222
2222222222
```

Writing a header as 1 and a stretcher as 2,
the sequence of center rows of the first 20 units is:
`1, 2, 12, 22, 212,
222, 2122, 2222, 22122, 22222,
221222,222222,2221222,2222222,22212222,
22222222,222212222,222222222,2222122222,2222222222.`
I found it to be related to the sequence [A094626](https://oeis.org/A094626)
in the On-line Encyclopedia of Integer Sequences.
In both, the sum of the digits in term n sums to n.
The difference lies in the position of the digit 1 in each term.
It is in the leftmost position in A094626,
which would not look as beautiful.

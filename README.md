# Gilbreth Sequences
Supporting material for the definition of Gilbreth Sequences  
in the [On-Line Encyclopedia of Integer Sequences (OEIS)][OEIS].

[OEIS]: https://oeis.org/

## Rationale

I have been [fascinated with brick patterns for a long time][BEAUTY_N_BRICKS].
This led me to study the 1909 book [Bricklaying System][BRICKLAYING_SYSTEM]
by Frank B. Gilbreth. [Bond Chart No 25][BOND_CHART_25] on page 265 of the book
shows 10 successive units of a basic module used in decorative brick patterns.

I have identified the [underlying algorithm][BRICK_UNIT_ALGORITHM] which
allows to recreate the 10 first units shown on Bond Chart No 25 and to
continue the sequence indefinitely based on the same logic.

> Each successive one is a half brick wider and two courses higher
> than the one that precedes it.

*A course of bricks is a sequence of bricks on the same row.*

## Definition of Top-Down and Bottom-Up Gilbreth Sequences

This infinite sequence of Gilbreth Brick Units can be described as the
conjunction of two separate sequences:

* a **top-down sequence** which generates the upper part of the unit,
  from the uppermost course with a single header brick
  down to the course in the middle of the unit, included.

* a **bottom-up sequence** which generates the lower part of the unit,
  from the lowermost course with a single header brick
  up to the course in the middle of the unit, excluded.

*A header brick is a brick seen from the short side, as a half brick;
it is heading towards us. A stretcher brick is a brick seen from the long
side, as a whole brick; it is stretching along its whole length in the facade.*

I have devised a numerical transcription of bricks and brick courses
which forms the basis for the mathematical definition of the top-down
and the bottom-up sequences for their inclusion in the OEIS database.

* a *header brick* is represented as digit `1` (half length)
* a *stretcher brick* is represented as digit `2` (full length)
* a *course of bricks* is represented as a number in which successive digits,
  from left to right, represent the corresponding bricks found in the course
  in the same left to right order.

The first ten terms of the top-down sequence can be transcribed from the
visual descriptions of the ten units in Bond Chart 25 by creating term #i
from a transcription of the middle course in unit #i:

1.  `1`
2.  `2`
3.  `12`
4.  `22`
5.  `212`
6.  `222`
7.  `2122`
8.  `2222`
9.  `22122`
10. `22222`

The first nine terms of the bottom-up sequence can be transcribed similarly
by creating term #i as a transcription of course just below the middle course
in unit #i+1:

1.  `1`
2.  `2`
3.  `21`
4.  `22`
5.  `212`
6.  `222`
7.  `2212`
8.  `2222`
9.  `22122`

Each term in the bottom-up sequence is a mirror of the corresponding term
in the top-down sequence, with the same digits in reversed order.

## Related Sequence in the OEIS

Sequence [A094626][] in the OEIS is related to the two Gilbreth sequences:

1.  `1`
2.  `2`
3.  `12`
4.  `22`
5.  `122`
6.  `222`
7.  `1222`
8.  `2222`
9.  `12222`
10. `22222`

Starting with term #1, each term in sequence A094626 has the same digits
as the corresponding terms in the Top-Down and Bottom-Up Gilbreth sequences,
except that the digit `1` is found in the first position in A094626 rather
than in the middle position, rounded left in the Top-Down Gilbreth sequence
or rounded right in the Bottom-Up Gilbreth sequence:

| Term |   A094626 |  Top-Down | Bottom-Up |
| ---: | --------: | --------: | --------: |
|    1 |         1 |         1 |         1 |
|    2 |         2 |         2 |         2 |
|    3 |    **1**2 |    **1**2 |    **2**1 |
|    4 |        22 |        22 |        22 |
|    5 |   **1**22 |   2**1**2 |   2**1**2 |
|    6 |       222 |       222 |       222 |
|    7 |  **1**222 |  2**1**22 |  22**1**2 |
|    8 |      2222 |      2222 |      2222 |
|    9 | **1**2222 | 22**1**22 | 22**1**22 |

[A094626]: https://oeis.org/A094626

[BEAUTY_N_BRICKS]: https://raw.githubusercontent.com/eric-brechemier/gilbreth-sequences/main/beauty-and-the-bricks.pdf
[BRICKLAYING_SYSTEM]: https://raw.githubusercontent.com/eric-brechemier/gilbreth-sequences/main/assets/bricklaying-system-by-frank-b-gilbreth.pdf
[BOND_CHART_25]: https://raw.githubusercontent.com/eric-brechemier/gilbreth-sequences/main/assets/bricklaying-system-by-frank-b-gilbreth.pdf#page=281
[BRICK_UNIT_ALGORITHM]: https://raw.githubusercontent.com/eric-brechemier/gilbreth-sequences/main/beauty-and-the-bricks.pdf#page=2

## References

### Bricklaying System

#### Internet Archive

* [Bricklaying System (copy from Cornell University)](https://archive.org/details/cu31924003883562)
* [Bricklaying System (copy from Getty Research Institute)](https://archive.org/details/bricklayingsyste00gilb)
* [Bricklaying System (copy from University of California)](https://archive.org/details/bricklayingsyste00gilbrich)

### Frank and Lillian Gilbreth

#### New England Historical Society

* [Lillian Gilbreth, Genius in the Art of Living](https://www.newenglandhistoricalsociety.com/lillian-gilbreth-genius-art-living/)

#### Wikipedia

* [Frank Bunker Gilbreth](https://en.wikipedia.org/wiki/Frank_Bunker_Gilbreth)
* [Lillian Moller Gilbreth](https://en.wikipedia.org/wiki/Lillian_Moller_Gilbreth)

## License

[CC-BY][] [Eric Bréchemier][ATTRIBUTION]

[CC-BY]: https://creativecommons.org/licenses/by/4.0/
[ATTRIBUTION]: https://github.com/eric-brechemier/eb-monogram

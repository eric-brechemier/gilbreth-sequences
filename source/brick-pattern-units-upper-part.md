# Upper Part of Frank and Lillian Gilbreth Brick Pattern Units

## NAME

Upper Part of Frank and Lillian Gilbreth Brick Pattern Units

Also:
Middle Course in Frank and Lillian Gilbreth Brick Pattern Units

## DATA

1,2,12,22,212,222,2122,2222,22122,22222

## OFFSET

1

## COMMENTS

Each number in the sequence represents a course of bricks
from the top to the middle of brick pattern units.

The digits of each number represent two types of bricks,
headers and stretchers, by their relative lengths in the courses:
1 for header bricks (seen as half bricks), 2 for stretcher bricks.

The first 10 units were described on page 265 of the book Bricklaying System
by Frank B. Gilbreth and Lillian E. Moller Gilbreth (uncredited),
published in 1909:

        “Bond Chart No. 25 shows ten units. Each successive one
  is a half brick wider and two courses higher than the one that
  precedes it.”

The chart gives a visual description of the ten units. They are growing
by a half brick per course from top to middle and shrinking by the same
amount from middle to bottom. The 10 units can be transcribed numerically
as follows, course per course, from top to bottom, with 1s for headers and
2s for stretchers:

* Unit  #1: 1
* Unit  #2: 1,2,1
* Unit  #3: 1,2,12,2,1
* Unit  #4: 1,2,12,22,21,2,1
* Unit  #5: 1,2,12,22,212,22,21,2,1
* Unit  #6: 1,2,12,22,212,222,212,22,21,2,1
* Unit  #7: 1,2,12,22,212,222,2122,222,212,22,21,2,1
* Unit  #8: 1,2,12,22,212,222,2122,2222,2212,222,212,22,21,2,1
* Unit  #9: 1,2,12,22,212,222,2122,2222,22122,2222,2212,222,212,22,21,2,1
* Unit #10: 1,2,12,22,212,222,2122,2222,22122,22222,22122,2222,2212,222,212,22,21,2,1

An equivalent transcription can be obtained by describing courses in each unit
from bottom to top instead. This is the most natural order for bricklayers,
who are laying brick courses from the ground up:

* Unit  #1: 1
* Unit  #2: 1,2,1
* Unit  #3: 1,2,12,2,1
* Unit  #4: 1,2,21,22,12,2,1
* Unit  #5: 1,2,21,22,212,22,12,2,1
* Unit  #6: 1,2,21,22,212,222,212,22,12,2,1
* Unit  #7: 1,2,21,22,212,222,2122,222,212,22,12,2,1
* Unit  #8: 1,2,21,22,212,222,2212,2222,2122,222,212,22,12,2,1
* Unit  #9: 1,2,21,22,212,222,2212,2222,22122,2222,2122,222,212,22,12,2,1
* Unit #10: 1,2,21,22,212,222,2212,2222,22122,22222,22122,2222,2122,222,212,22,12,2,1

The first unit is made of a single course with a single header brick.
Each following unit can be deducted from the previous one by:

- copying the upper part, from top to middle course included
- inserting a new middle course, a half brick wider (more details below)
- copying the middle course in reversed order
- copying the bottom part, middle course excluded to bottom

There are two ways to obtain the new course, a half brick wider, depending
on whether the middle course of the previous unit contained a header or
was made entirely of stretchers:

* when the previous middle course contained a header, the new middle course
  is obtained by replacing that header with a stretcher (half width longer)

* when the previous middle course contained only stretchers, a header is
  added to obtain the new middle course. When the number of stretchers
  was even, the header is added right in the middle of the new course.
  When the number of stretchers was odd, the header is positioned as close
  as possible to the middle of the course, with one less stretcher on the
  left than on the right.

Larger and larger units can be constructed indefinitely.

This sequence, Upper Part of Frank and Lillian Gilbreth Brick Pattern Units,
describes courses of bricks in the top half of the units, from top to middle
course included. The n-th term of the sequence, starting at offset 1,
describes the middle course of Unit #n.

The first n terms of this sequence describe the courses of bricks in the
upper part of Unit #n, from top to middle course included.

The bottom half of the units, from bottom to middle course excluded,
is described in an associated sequence:

  Lower Part of Frank and Lillian Gilbreth Brick Pattern Units.

## REFERENCES

Frank B. Gilbreth, Bricklaying System, Myron C. Clark Publishing, 1909, page 265.

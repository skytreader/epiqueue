# EPiQueue
A collection of instances of textbook data structures encoded in JSON format.

These structures are nonlinear, hence the need to serialize them in a format
almost every programming language can easily parse.

## Why?
Real world makes you rusty. You'd need to refresh yourself on algorithms every
now and then. Maybe it's an interview, or you're practicing for Code Jam/Hacker
Cup/etc., or maybe you just plain want to.

The thing is, algorithms usually work on data structures. And building data
structures for practice can be cumbersome. You want to focus on practicing and
not on the boring clerical job of encoding data structures right?

Worry not. This is precisely the why of EPiQueue.

## Why the name?
A lot of reasons. _e_ is generally known as [Euler's number](http://www.wolframalpha.com/input/?i=euler+number),
an irrational and a transcendental value roughly equal to 2.7182818284. _pi_ is
another irrational and transcendental value roughly equal to
3.141592653589793238462643383279502884197169. (Note: As of this writing, I know
_pi_ to that many decimal places).

Of course, _queue_ is one of the basic data structures that still proves useful
in a lot of applications. Shame it would not be represented here.

Lastly, E.P.Q. is the initials of a particular professor from my undergrad days
who is well-known for teaching CS32, the data structures course.

# Notes on structures
**General:** Each structure will contain a field `_comment` somewhere. This field
describes the structure contained in the file and should be ignored.

## Binary Trees
Each node is represented with the following fields: `node_data`, `left_son`, and
`right_son`. Terminal nodes have the value `null` for `left_son` and `right_son`.

The root node, and only the root node, will contain the field `_comment`.

## Graphs
Graphs are represented as either an adjacency matrix or adjacency lists. The
graph representation is nested in the JSON structure in the field `representation`.
Aside from the `_comment` field, there is also another field, `_is_matrix`,
containing a boolean value that will distinguish between representations.

The representation field of an adjacency matrix representation will contain an
array of arrays, one inner array for each node. The square structure will
feature ones and zeroes, one signifying adjacency and non-adjacency,
respectively.

An adjacency list representation will feature a map of strings to a list. The
key will be the node's name while the corresponding list will contain the keys
of the adjacent nodes.

## Day 17

[Part1](part1.py) was easy. Second puzzle was small enough to solve it manually. I think, solving part 2 as described in the problem for general case is very difficult. I wonder if a general case solution will be posted by someone on advent of code subreddit. All existing solutions assume at least one of the two things:

 - Path is already known.
 - Instruction cannot be split, for example let's say path is `R4, L4, R4`, they assume that A, B cannot be `R4 L2`, `2 R4`. Although all solutions probably would be like that puzzle description doesn't explicitly say so.

My input was as follows:

```
..................................#####....
..................................#...#....
..................................#...#....
..................................#...#....
..............................#########....
..............................#...#........
..............................#...#........
..............................#...#........
..............................#...#........
..............................#...#........
..............................#...#........
..............................#...#........
..........................#########........
..........................#...#............
..........................#...#############
..........................#...............#
..........................#############...#
......................................#...#
..................................#########
..................................#...#....
#####...........###########.......#...#....
#...#...........#.........#.......#...#....
#...#...........#.........#.......#...#....
#...#...........#.........#.......#...#....
#############...#.........#.......#...#....
....#.......#...#.........#.......#...#....
....#.......#...#.........#...^########....
....#.......#...#.........#.......#........
....###########.#.........#########........
............#.#.#..........................
............#.#.#..........................
............#.#.#..........................
............#####..........................
..............#............................
..........#########........................
..........#...#...#........................
......#########...#........................
......#...#.......#........................
......#...#.......#........................
......#...#.......#........................
......#...#.......#........................
......#...#.......#........................
......#...#.......#############............
......#...#...................#............
..#########...................#............
..#...#.......................#............
..#...#...................#####............
..#...#....................................
..#####....................................
```

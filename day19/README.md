## Day 19

### Part 1

Compared to previous day, today's puzzle was very easy. [Part 1](part1.py) was solved by aggregating outputs of intcode. My beam input looks like this:

```
10000000000000000000000000000000000000000000000000
00000000000000000000000000000000000000000000000000
00010000000000000000000000000000000000000000000000
00000000000000000000000000000000000000000000000000
00000010000000000000000000000000000000000000000000
00000001100000000000000000000000000000000000000000
00000000010000000000000000000000000000000000000000
00000000001100000000000000000000000000000000000000
00000000000011000000000000000000000000000000000000
00000000000001100000000000000000000000000000000000
00000000000000111000000000000000000000000000000000
00000000000000001110000000000000000000000000000000
00000000000000000111000000000000000000000000000000
00000000000000000011110000000000000000000000000000
00000000000000000000111100000000000000000000000000
00000000000000000000011110000000000000000000000000
00000000000000000000000111100000000000000000000000
00000000000000000000000011111000000000000000000000
00000000000000000000000001111100000000000000000000
00000000000000000000000000011111000000000000000000
00000000000000000000000000001111110000000000000000
00000000000000000000000000000111111000000000000000
00000000000000000000000000000001111110000000000000
00000000000000000000000000000000111111000000000000
00000000000000000000000000000000001111110000000000
00000000000000000000000000000000000111111100000000
00000000000000000000000000000000000011111110000000
00000000000000000000000000000000000000111111100000
00000000000000000000000000000000000000011111111000
00000000000000000000000000000000000000001111111100
00000000000000000000000000000000000000000011111111
00000000000000000000000000000000000000000001111111
00000000000000000000000000000000000000000000011111
00000000000000000000000000000000000000000000001111
00000000000000000000000000000000000000000000000111
00000000000000000000000000000000000000000000000001
00000000000000000000000000000000000000000000000000
00000000000000000000000000000000000000000000000000
00000000000000000000000000000000000000000000000000
00000000000000000000000000000000000000000000000000
00000000000000000000000000000000000000000000000000
00000000000000000000000000000000000000000000000000
00000000000000000000000000000000000000000000000000
00000000000000000000000000000000000000000000000000
00000000000000000000000000000000000000000000000000
00000000000000000000000000000000000000000000000000
00000000000000000000000000000000000000000000000000
00000000000000000000000000000000000000000000000000
00000000000000000000000000000000000000000000000000
00000000000000000000000000000000000000000000000000
```

### Part 2

Let's call `x` be the x coordinate of top-left corner of 100x100 square. After finding angles, I calculated a rough estimate on `x` value. After that, just tried `x-50` and `x+50` range to find the answer. What suprises me is that if x=k satisfy the constraint and x=k-1 doesn't satisfy it, the assumption that the answer is x=k is wrong. Because beam doesn't spread on a real valued plane, there can be a value less than k-1 and still satisfy the 100x100 constraint. In my case,

 - `x=1331` DO satisfy.
 - `x=1330` DO NOT satisfy.
 - `x=1329` DO NOT satisfy.
 - `x=1328` DO satisfy.

First, i found `1331` and though that was the answer. However the minimum value satifying the condition is `1328` despite the fact that the values between them are not suitable for 100x100 square. The source code in [part2.py](part2.py)
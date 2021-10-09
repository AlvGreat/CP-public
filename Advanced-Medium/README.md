# Advanced Group Questions


## Question 1: 
### High Scoring Sublist (may be difficult; 2 pts)
You are given a list of scores, with the scores ranging from -1000 to 1000. Return the largest sum of the scores given that you can choose any consecutive section of the list to add up (any sublist starting from one index and ending at another). 

### Example 1:
```
Input:
[-2, 3, 3, -1, 7, 8, -10]

Output/returned value:
20
```

Explanation:
We choose [3, 3, -1, 7, 8] as our section from the list, which is from the 2nd element to 6th element (Note that it must be in order). This gives us the largest sum possible: `3 + 3 + -1 + 7 + 8 = 20`

### Example 2:
```
Input:
[1, 2, 3]

Output/returned value:
6
```

Explanation:
We just add up the entire list, giving us `1 + 2 + 3 = 6`

### Assumptions:
The length of the list will be less than `10,000`




## Question 2: 
### The Social Distancer (3 pts)
A student is visiting the movie theater during COVID-19 with the goal of sitting far away from everyone. You will be given a list representing the seats in a certain row: a 0 indicates an empty seat and 1 indicates an occupied seat. 

The student can sit in any empty seat. Help them find a spot such that the distance between him and the closest person to him is maximized. As a programmer, you will return this distance (in seats). 

### Example 1:
```
Input:
[1, 0, 0, 0, 1, 0, 1]

Output/returned value:
2
```

Explanation:
The student would want to sit in the 3rd seat, so that the closest people will be in the 1st seat and 5th seat. This results in the maximum distance, which would be 2.

### Example 2:
```
Input:
[1, 0, 0, 0]

Output/returned value:
3
```

Explanation:
The student would want to sit in last seat (3 seats away).

### Example 3:
```
Input:
[0, 1]

Output/returned value:
1
```

Explanation:
The student has no option but to sit in the 1st seat, which is only 1 away :(

### Assumptions:
The number of seats will be `>= 2` and `<= 2000`

Each element of the list will be `'0'` or `'1'`

At least 1 seat is occupied and at least 1 seat is empty




## Question 3: 
### Player Scoring (4 pts)
As the judge of a game, you have a list of integers `nums`, consisting of the number of points each player has. Return a list of zero-indexed rankings for each person. If two players have the same amount of points, they would be tied for a certain place (have the same rank).

### Example:
```
Input:
nums = [5, 3, 5, 9, 2]

Output/returned value:
[1, 2, 1, 0, 3]
```
Explanation:
The person with 9 points would be in 1st place, so their corresponding ranking is `0`. The people with 5 points are tied for 2nd place, so their corresponding ranking is `1`.

### Assumptions:
The input list size will be `<= 100,000`




## Question 4: 
### Days Until a Better One (6 pts)
In this problem, you will be given an array of numbers, `scores`, which represent the score of how good a day is. The score will range from 30 - 100 (not 0 because we're trying to be optimistic). 

You will return an array, `answers`, such that `answers[i]` is the number of days that you have to wait after day `i` to get a better day (a day with a strictly higher score). `answers[i]` should be 0 if there is no better day after `i`. 

### Example 1:
```
Input:
[30, 40, 50, 60]

Output/returned value:
[1, 1, 1, 0]
```

Explanation:
* For score 30, we wait 1 day to get a score of 40
* For score 40, we wait 1 day to get a score of 50
* For score 50, we wait 1 day to get a score 60
* Notice how there is no day after the last where we can get a higher score

### Example 2:
```
Input:
[65, 68, 37, 34, 72, 100]

Output/returned value:
[1, 3, 2, 1, 1, 0]
```

Explanation:
Repeat a similar process as the above example to find out why the output is correct.

### Assumptions: 
The list of scores will have `<= 10000` scores. 




## Question 5: 
### Maximum Profits (6 pts)
A magical genie lays out a bunch of items in a row, each worth a certain amount of money. As a programmer, you'll receive a list of the items' values in the form of an array, `nums`. 

Your goal get items that add up to as much money as possible, with one catch: you cannot pick two adjacent items.

### Example 1:
```
Input:
[1, 2, 3, 1]

Output/returned value:
4
```

Explanation:
Take the 1st and 3rd items (1 + 3 = 4)

### Example 2:
```
Input:
[2, 7, 9, 3, 1]

Output/returned value:
12
```

Explanation:
Take the 1st, 3rd, and 5th items (2 + 9 + 1 = 12)

### Example 3:
```
Input:
[2, 1, 1, 2]

Output/returned value:
4
```

Explanation:
Take the 1st and 4th item, skipping the 2nd and 3rd

### Assumptions: 
The list of items, `nums`, will have length `>= 1` and `<= 100`. 

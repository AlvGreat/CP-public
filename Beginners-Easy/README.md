# Beginner Group Questions


## Question 1: 
### Integer Digit Sum (3 pts)
Given a positive integer, `n`, return the sum of its digits.

### Example:
```
Input:
n = 123

Output/returned value:
6
```

Explanation:
1 + 2 + 3 = 6

### Assumptions: 
You'll receive a valid positive integer, `0 <= n < 2^31`




## Question 2: 
### Sequence Generator (4 pts)
A math professor has come up with a formula to generate a sequence of numbers given a starting point. You as a programmer are now tasked with writing a function to find out how long the sequence will be. 

The next number in the sequence after n can be calculated as follows: 
* `n_next = n / 2` if n is even
* `n_next = 3 * n + 1` if n is odd
* The sequence ends if `n = 1`

### Example:
```
Input:
n = 11

Output/returned value:
15
```

Explanation:
The sequence would go something like this: `11, 34, 17, 52, 26, 13, 40, 20, 10, 5, 16, 8, 4, 2, 1`, which has a length of 15.

### Assumptions:
There will be a finite sequence length for all test inputs.




## Question 3: 
### ACM Attendance Tracker (5 pts)
You are given a string of random length that consists of three letters ("A", "L", or "P") that records whether a member showed up to an ACM event. 
* "A" means absent
* "L" means late
* "P" means present

As an example, "AAPP" means that the member was absent to the first 2 events and present for the last 2.

The member will be featured on our website if they meet the following criteria:
* Absent for less than 2 events total (< 2 absences are accepted)
* Never late for 3 or more consecutive events (cannot be >= 3)

Return `true` if the member will be featured on our website and `false` otherwise.

### Example 1:
```
Input: 
"PPALLL"

Output/returned value:
false
```

Explanation:
The student was late to 3 consecutive events, so they will not be featured.

### Example 2:
```
Input: 
"PPALLP"

Output/returned value:
true
```

Explanation:
Both conditions are met so the student will be featured on our website.

### Assumptions:
The length of the string will be `>= 1` and `<= 1000`




## Question 4: 
### High Scoring Sublist (Challenge question; 3 pts)
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




## Question 5: 
### The Social Distancer (6 pts)
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

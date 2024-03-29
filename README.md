# Proportional-STAR-Voting-with-Runoffs
I made a Proportional STAR Voting Python Program, except it has one on one runoffs after every round. Instead of the highest scored candidate in a round winning a round, the top 2 candidates in a round face off in a runoff. A ballot's weighted runoff vote goes to the candidate it gave more points to.
I thought it was weird regular Proportional STAR Voting didn't have automatic one on one runoffs, since "Automatic Runoff" is half the acronym. I thought it would be good to make sure a majority of the people in a proportion preferred the winning candidate. I think I'll call it Allocated STAR Voting to differentiate it from Allocated Score Voting / Proportional "STAR" Voting.

Use: Just copy and paste the code into a Python Interpreter, run, and the program will ask you how many candidates are running, what their names are, how many seats can be won, and what the ballot scores are. You can paste the code and run it here: https://www.programiz.com/python-programming/online-compiler/

Random Ballot Creator Use: You can simulate a Proportional STAR Election with random votes. Just copy and paste the code into a Python Interpreter, run it, enter the amount of voters you want and how many candidates you want, and it will spit out a set of ballots with random scores on it from 0 through 5. You can then copy and paste the result as scores when the STAR-PR program asks you.

Output: The program will output the scores of the candidates each round, how many runoff votes they got, and who the winners are.

Credits: I used the algorithm used for regular Proportional STAR / Allocated Score from https://electowiki.org/wiki/Allocated_Score for the regular allocated score part. I then added an algorithm to count runoff votes.


 
Tennessee Example https://en.wikipedia.org/wiki/STAR_voting#Example

Pretend that instead of voting for a capital they are voting for representatives from these cities.
       
        |            |   City Choice |              |              |               |             |         |
        |------------|---------------|--------------|--------------|---------------|-------------|---------|
        | Voter from |               | Memphis      | Nashville    | Chattanooga   | Knoxville   |  Total  |
        |------------|---------------|--------------|--------------|---------------|-------------|---------|
        |            |   Memphis     | 210 (42 × 5) | 0 (26 × 0)   | 0 (15 × 0)    | 0 (17 × 0)  |  210    | 
        |------------|---------------|--------------|--------------|---------------|-------------|---------|
        |            |   Nashville   | 84 (42 × 2)  | 130 (26 × 5) | 45 (15 × 3)   | 34 (17 × 2) |  293    |
        |------------|---------------|--------------|--------------|---------------|-------------|---------|
        |            |   Chattanooga | 42 (42 × 1)  | 52 (26 × 2)  | 75 (15 × 5)   | 68 (17 × 4) |  237    |
        |------------|---------------|--------------|--------------|---------------|-------------|---------|
        |            |   Knoxville   | 0 (42 × 0)   | 26 (26 × 1)  | 45 (15 × 3)   | 85 (17 × 5) |  156    |





Demo with Droop Quota:

Enter the number of candidates: 4

Enter the name of candidate 1: Memphis

Enter the name of candidate 2: Nashville

Enter the name of candidate 3: Chattanooga

Enter the name of candidate 4: Knoxville

Enter the number of seats: 3

Enter all the ballots separated by space with no space within each ballot e.g. 231 215 421: 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 5210 0521 0521 0521 0521 0521 0521 0521 0521 0521 0521 0521 0521 0521 0521 0521 0521 0521 0521 0521 0521 0521 0521 0521 0521 0521 0521 0353 0353 0353 0353 0353 0353 0353 0353 0353 0353 0353 0353 0353 0353 0353 0245 0245 0245 0245 0245 0245 0245 0245 0245 0245 0245 0245 0245 0245 0245 0245 0245

There are  100  voters.

Round 1:

Scores:
Nashville: 293
Chattanooga: 237
Memphis: 210
Knoxville: 156

Runoff votes:
Nashville: 68
Chattanooga: 32
No preference: 0

Round 2:

Scores:
Memphis: 210
Chattanooga: 185
Knoxville: 130

Runoff votes:
Memphis: 42
Chattanooga: 32
No preference: 0

Round 3:

Scores:
Chattanooga: 159
Knoxville: 130

Runoff votes:
Chattanooga: 31
Knoxville: 17
No preference: 0

Winners: ['Nashville', 'Memphis', 'Chattanooga']
> 

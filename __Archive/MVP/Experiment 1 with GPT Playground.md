---
Date Created: 2024-02-29
---
## Probability 10th Standard

The first experiment is just to see how GPT 3.5 and 4 respond directly with the most obvious of prompts. This would be the ideal we strive for where we can simply plug in the questions as it is that a teacher might give their children. We include some pointers on how we want GPT to respond. We will attempt this set up with two different question sets. 

#### Sytem Prompt 1

You are a student that the user is trying to teach. The user will give you an explanation of probability using which you will answer the below questions. 
1. A single throw of a dice, find the probability of getting a number greater than 2  
2. A single throw of a dice, find the probability of getting a number less than or equal to 2  
3. From a well-shuffled deck of 52 cards, one card is drawn. Find the probability that the card drawn will be a face card  
4. In a single throw of a dice, find the probability of getting 7  
5. A card is drawn from a pack of 100 cards numbered 1 to 100. Find the probability of drawing a number which is a perfect square.
6. A bag contains 5 red balls and some blue balls. If the probability of drawing a blue ball from the bag is thrice that of a red ball, find the number of blue balls in the bag.

- Pretend like you know nothing about probability and how to solve these problems. 
- Attempt the questions based on the explanation given and return answers. 
- Remember the aim is to help the student understand the gaps in their knowledge so try to be as true to the explanation as possible. 
- Don't try to teach the student or ask any questions. Simply answer the questions based on the student's prompt. 
- Try to get as detailed an explanation as possible. 

#### User Prompt 1
Probability is the branch of mathematics concerning events and numerical descriptions of how likely they are to occur. The probability of an event is a number between 0 and 1; the larger the probability, the more likely an event is to occur. The higher the probability of an event, the more likely it is that the event will occur. A simple example is the tossing of a fair (unbiased) coin. Since the coin is fair, the two outcomes ("heads" and "tails") are both equally probable; the probability of "heads" equals the probability of "tails"; and since no other outcomes are possible, the probability of either "heads" or "tails" is 1/2 (which could also be written as 0.5 or 50%)
##### Result: 
This prompt copied from Wikipedia didn't work and GPT asked for more explanations in cases where the outcomes are not equally probable. This was a good result. 

#### User Prompt 2
Probability of an outcome is defined as the number of favourable outcomes divided by the total number of outcomes. 

##### Result: 
This prompt worked too well. Just with this simple definition GPT was able to solve all the questions correctly




#### Sytem Prompt 2

You are a student that the user is trying to teach. The user will give you an explanation of probability using which you will answer the below questions. 
1. Ashley's class is doing experiments with probability. They have a box with 3 green balls, 2 blue balls, and  5 red balls. Ashley takes a ball from the box, keeps the ball, and passes the box to Manuel. What is the probability that Ashley gets a blue ball and Manual gets a green ball?
2. Two dice, one red and one yellow, are rolled simultaneously. What is the probability of getting equal numbers on both?
3. The total events to throw three dice simultaneously is ____
4. Three dice are rolled together. What is the probability as getting at least one '4'?
5. There is a room full of 50 people. What is the probability that at least two people have the same birthday?

- Pretend like you know nothing about probability and how to solve these problems. 
- Attempt the questions based on the explanation given and return answers. 
- Remember the aim is to help the student understand the gaps in their knowledge so try to be as true to the explanation as possible. 
- Don't try to teach the student or ask any questions. Simply answer the questions based on the student's prompt. 
- Try to get as detailed an explanation as possible. 

#### User Prompt 1
Probability of an outcome is defined as the number of favourable outcomes divided by the total number of outcomes. 
##### Result: 
This prompt worked too well. Just with this simple definition GPT was able to solve all the questions barring the last one. I think it cannot solve the last one without serious effort so I don't think that question counts at all. It was a bit frustrating that it just decided that it had to multiply independent events without that being prompted by the user. 



## Notes 
- GPT 3.5 doesn't work well at all. We need GPT 4 for this to work. 
- It's not easy to create a situation of debugging. Perhaps we need to include harder questions where mistakes are happening.
- I'm pleasantly surprised by the results though. It definitely seems doable and not too far off with the right prompts and inputs. 
- It's really important to understand what it is that we want the user to explain. Having an understanding of this might help structure the prompts together. Perhaps for each question we can try to explain to GPT what it needs to look for in the explanation. 
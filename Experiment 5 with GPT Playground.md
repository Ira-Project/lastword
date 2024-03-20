---
Date Created: 2024-03-20
---
### Probability 10th Standard

So far with pure prompt engineering we are able to solve for the case where the user does not provide enough information. Though it uses a brute force methodology it has yielded fairly reasonable results. Where this approach is failing is where the user provides all the information but gives incorrect information. Here GPT tends to either correct the user or ends up working out the problem correctly based on what it already knows. We attempted a fine tuning with a small data set to solve for this. 

### Notes
- Though it was a very small data set and it possibly can be improved with a larger set we did not get good results. Given we are only able to fine tune GPT 3.5 and not GPT 4 it feels like we're taking one step forward and two steps back. 
- Fine tuning helped solve our formatting issue however and every answer was correctly formatted. Surprisingly the responses also came back in LaTeX format. 

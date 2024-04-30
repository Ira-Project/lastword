---
Date Created: 2024-03-20
---
### Periodic Table 10th Standard

To a reasonable degree we've got success with a mathematics topic. We're now trying to see how well this approach works with a topic in Chemistry. We will take a similar approach as we have taken in Experiment 3 with the topic of Periodic Table. We have looked at a 10th grade textbook in India and started with half a lesson.  

##### Elements in the lesson based on the textbook
- Periodic table has eighteen vertical columns called groups arranged from left to right. There are seven horizontal rows known as periods.
- The number of shells present in an atom determines its period. 
- The group number is typically determined by how many electrons are present in the outermost shell. 
- Electronic configuration refers to how many electrons are in each shell of an atom. Each shell in an atom can contain only a fixed number of electrons. The first can hold 2, the second and third can hold 8, fourth and fifth can hold 18 and the 6th and seventh hold 32. 
- It's important to note that in the second and third period the groups 3-12 are not present. 
- For an element with atomic number 11, the electronic configuration is 2, 8, 1. This means it is in the 3rd period and the in the 1st group.
- For an element with atomic number 9, the electronic configuration is 2, 7. This means it is in the 2nd period and the in the 17th group.
- Certain properties are similar with elements in the same period - this is because their electronic configuration is similar and is referred to as periodicity. 
- In general all atoms prefer to have complete shells than incomplete shells. Valency is the combining capacity of an atom or an element. It is equal to the number of electrons an atom can donate or accept or share. For example Sodium with atomic number 11 has an electronic configuration of 2, 8, 1 and can donate one electron and have only complete shells.  It's valency is 1. Chlorine with an atomic number of 17 has a configuration of 2, 8, 7. It can receive one electron to complete it's final shell and also has a valency of 1. 

#### Sytem Prompt 1

You are a student that the user is trying to teach. The user will give you an explanation of the periodic table using which you will answer the question. To help you the elements of a good explanation is provided. For each of these instruction is also given on what to return if it is not present. 

Question :
What is the electronic configuration of Chlorine with the atomic number 17?

Elements of a Good Explanation : 
1. The user must explain what electronic configuration i.e. the number of electrons in each shell of an atom.

What to Return if Missing -
- Answer: 0
- Working:  Sorry I'm not able to understand what electronic configuration is.

2. The user must explain how each shell in an atom can contain only a fixed number of electrons.

What to Return if Missing -
- Answer: 17
- Working:  I'm sorry I don't understand how to calculate electronic configuration based on the information you have given me. 

3. The user must indicate the correct number of electrons in each shell. 

What to Return if Missing -
- Answer: 10, 7
- Working:  Thank you for your explanation. I understand that each shell contains only a fixed number of electrons. I have assumed that we can put 10 electrons in the first shell and the remaining 7 in the second. I have calculated electronic configuration as 10, 7

If all of the above details are present compute the electronic configuration based on the information the user provided about electrons in each shell. 

#### Sytem Prompt 2

You are a student that the user is trying to teach. The user will give you an explanation of the periodic table using which you will answer the question. To help you the elements of a good explanation is provided. For each of these instruction is also given on what to return if it is not present. 

Question :
What period would the element with atomic number 16 be in?

Elements of a Good Explanation : 
1. The user must explain that the period determined by the number of shells/orbits in the atom.

What to Return if Missing -
- Answer: 0
- Working:  Sorry I'm not able to understand how to find out what period an element would be.

2. The user must explain how each shell in an atom can contain only a fixed number of electrons and that we can use this to compute the number of shells in an atom. 

What to Return if Missing -
- Answer: 1
- Working:  I understand that we need to figure out the number of shells to determine period but I am unsure how we might achieve that. 

3. The user must indicate the number of electrons in each shell to enable calculations.

What to Return if Missing -
- Answer: 2
- Working:  Thank you for your explanation. I have assumed that we can put 10 electrons in the first shell and the remaining 6 in the second. Given there are two shells I assume this element is in period 2. 

If all of the above details are present compute the electronic configuration based on the information the user provided about electrons in each shell. 

### Notes
- GPT 4 is very good at understanding when elements of a text are present and absent. What it's not good at is computing the answer based on the information the user provides. For example if the user gives wrong information on the number of electrons in each shell, GPT Is unable to compute based on their inputs.
- We're getting slightly hit or miss responses. I think GPT is confused whether to use it's own understanding and what the user might have typed. We'll have to make things more clear and improve the prompt.
- The main positive here is that GPT is able to figure out chemistry problems as well and this approach overall has merits. There's still work to be done to make it work well but it definitely seems possible to execute. 
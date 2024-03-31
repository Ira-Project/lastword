---
Date Created: 2024-03-20
---
So far we've taking a very unstructured approach to the prompt and given it as text. While this has yielded some results it can also be tedious and is not very easy to replicate in the long run. We have also observed that the assistant has a lot more capabilities with respect to the playground chat. With this experiment we hope to organise the information so GPT might process it better and we may overcome the challenges with incorrect responses. Here is an explanation for how we've structured it. 

- The Assistant is given a persona and clear instructions on how to respond. This is the identity of the assistant and here we attempt to ensure GPT doesn't use any past knowledge and plays the role of a student. The assistant is also informed of the file structure of the supporting questions so it may respond appropriately.
- A JSON file is attached with a list of questions. Each question has an answer, a list of the concepts that a good explanation would contain as well as a few sample incorrect answers a user might submit. The concepts and incorrect examples contain what a good response to the user might look like. 

----
### Assistant Prompt






-----
### Notes

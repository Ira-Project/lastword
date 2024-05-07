---
Date Created: 2024-05-07
---
The process of designing an AI that can learn a concept from a user has been a useful exercise in understanding how knowledge is constructed in the human mind. Recent research has suggested that encoding knowledge into graphs of concepts or ideas can help design intelligent systems. For the v2 of our product we've decided to follow this approach. Given below is an outline of the process and how the AI works to respond to the user :-

### Concept Maps

The first step in our process was to build a concept graph for every topic that we're creating assignments in. The concept graph breaks down the concept into smaller parts and contains information of the relationships between ideas. While the encoding is a graph and not a tree there are still some parent and child relationships between ideas where some ideas build on one another. 

For each question we can then further create a sub graph of the concepts necessary for that particular question. We used GPT-4 for this process and manually verified the outputs. 

### Explanation Classification

Having performed some user testing we had a set of 50 responses to questions that were provided by actual users. We identified that often responses were very procedural and catered to a single question. We also saw that explanations contained incorrect information and were very often incomplete. We classified explanations into four categories - Partial and Correct, Partial and Incorrect, Complete and Correct, Complete and Incorrect. In addition we flagged explanations that were only catering to a particular question and explanations that were complete gibberish.

### Checking for Completeness Using RAG

One of the insights from our previous AI versions was that it was helpful to create separate agents to test for completeness and correctness. While our previous approach used two different GPT-4 agents, the costs and time taken for computation was extremely high. Further for completeness in particular there was a lot of noise and responses were not consistent. To address this we decided to use RAG to check for completeness. Given that we have a concept map we are able to compare the explanations provided by the user to the concepts in the map. After experimentation we were able to arrive at a clear cosine similarity threshold that yields accurate completeness evaluation for all the user responses so far. 

### Short Circuiting for Incompleteness

There are certain incomplete responses where computation is not at all possible and for these cases we are short circuiting the process and returning results to the user. To determine whether computation should be attempted or not concepts are marked with a required for computation field in the concept map. If all the required for computation concepts are present in the explanation then the short circuiting is not performed. 

There are a few different cases here :-
- Similarity threshold not at all met - When cosine similarity between users explanation is below the threshold for all the concepts in the map. In this case we simply cannot proceed at all and tell the user that we understood nothing and could not proceed. This tends to be the case for gibberish explanations.
- Similarity threshold met for parent nodes  - In certain cases the parent concepts in the concept graph are present in the explanation but there is still not sufficient information for the computation. Here rather than pointing out what else is needed we simply note how we are unable to calculate with the information that the user has provided. 
- Similarity threshold met for child nodes - Often we also see that explanations by users contain concepts from child nodes. Typically this involves using technical terms without explaining what they are. In such cases the user is prompted to explain the parent concepts that they might have referenced. 

### Testing for Correctness










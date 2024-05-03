---
Date Created: 2024-05-02
---
Prerequisite
- Define a concept graph for the topic

During question upload
- Traverse the graph with a question and creates a sub graph for every question using GPT-4.

During explanation
- Explanation is converted to embeddings using RAG
- Traverse the sub graph for the question to check if concepts exists or not
	- Look at concept question - Any possible result of an experiment or a trial is an outcome
	- Check if embedding explanation contains the concept by checking for embedding
	Create a further sub graph that is purely from the explanation of the user
- GPT-4 agent is given the sub graph and it computes an answer and a reasoning
---
Date Created: 2024-05-14
---
### Done

User
- Email
- EmailVerified
- HashedPassword
- Avatar

Session
- UserId
- ExpiresAt

EmailVerification
- UserId
- Email
- Code
- ExpiresAt

PasswordResetTokens
- UserId
- ExpiresAt

Class
- Name
- Subject
- Description
- SubjectId

Subject
- Text

ClassMember
- ClassId
- User Id
- Code
- Type - Teacher or Student

Assignment
- Name
- Due Date
- Topic
- Max Score?
- Time Limit?
- ConceptGraphId?
- ClassId?
- isLive
- isSample
- ShowConceptHints

AssignmentTemplate
- Title
- Image Url
- AssistantId
- ConceptGraph
- Prompt (if needed)

ConceptGraph
- id

Concept
- ConceptGraphId
- formula
- calculationR

ConceptQuestion
- ConceptId
- Text

ConceptGraphEdges
- id
- fromConceptId
- toConceptId
- conceptGraphId

ConceptGraphRoot
- ConceptGraphId
- ConceptId

ConceptExplanationText
- ConceptId
- AlternateText
- Embedding Vector

Questions
- Text
- Answer
- ConceptSubGraph
- AssignmentTemplateId || AssignmentId

Explanation
- Text
- Embedding -> Can choose to not store
- UserId
- AttemptId?
- AssignmentTemplateId || AssignmentId 

CorrectConcepts
- ExplanationId
- ConceptId

----
### To Do

Attempt
- UserId
- AssignmentId
- Score
- FinalExplanationId
- SubmittedAt 

Answer
- ExplanationId 
- QuestionId 
- ComputedAnswer 
- IsCorrect -> Computed property 
- Explanation Text 

---
Date Created: 2024-05-14
---
Subjects
- List for Selection
	- Get list of all subjects 

Auth
- Login
- SignUp
- VerifyEmail
- Forgot Password
- GoogleAuth

Classes
- Class List
	- Get list of classes with userId
- Class Creation
	- Put class
- Join Class
	- Put Class-User based on class code and teacher last name
- 

Assignments
- Sample Assignments
	- Get list of assignments with sample true
- List of Assignments
	- Get list of assignments by classId
- Create assignment
	- Based on template id and teacher id and mark not live
- Take assignment live
	- Populate fields and mark isLive = True

Attempts
- Get Submissions
	- Get list of attempts with submitted at field and assignment Id
- Get submission percentage by assignmentId
	- Divide list of attempts with submitted at fields by total users that are students in the class
- Average and median Score 
	- Get list scores of all the attempts with assignmentId and submitted at and compute median and average
- Concept Scores
	- Get explanations from final explanationIds in the list of attempts with submitted at field matching assignmentId
	- Iterate through explanations and extract count of correct concept nodes
	- Get list of assignment template - concept and extract the concept texts from the concept ids along with position
	- Use the count of concept node and return the concept text along with a value dividing the count of each node in explanations by the total people in the class
- View Submission
	- Get a single submission object
	- Get a list of answers matching the explanation id from the final explanation in the subject
	- Get the concept map from the assignment template (attempt -> assignmentId -> assignmentTemplateId) and provide also the correct concept list
- Create Attempt
	- Create attempt using assignmentId and user Id
- Submit Attempt
	- Update attempt submitted at field
	- Update final explanationId by searching for the last explanation 
	- Update score by getting answers with last explanationId and checking correctness

Explanation
- Check explanation (to stream)
	- Create explanation object 
	- Compare explanation embedding to concept explanation text embeddings and based on threshold generate correct concepts
	- Update correct concepts in explanation object
	- For each question in assignment template
		- Run explanation through the AI and get a computed answer as well as explanation text
		- Create answer object. Compute isCorrect by comparing computed answer with the question's actual answer
	- Return list of answer objects and the explanation object

Class User
- List of people
	- Get all Class-User based on classId - can filter by type for screen later
- Add Student
	- Add item to Class-User
		- TO DO: Handle if user is not present


# Mappth - GCSE Revision App

**Product name:** Mappth  
**Date:** 2/01/2026  
**Owner:** Marcus Hanmer  
**Type:** EdTech

## 1. The Problem

**Pain point**  
Students who need help with GCSE maths (or any topic for that matter) may find it hard to get help, since it is difficult for the school itself to always deliver every need for the student, and outside of school the child is either left alone to teach themselves, or they get a personal tutor. The paint point with this is that the tutor will cost upwards of £30/hr if not more, and this is alot of money over time. Furthermore, each session is only on average an hour long, and is only on a particular time of day that is schedualed. There are many issues with this, and the idea for Mappth was to have a tutor in your pocket all of the time which is ready to teach anything, anytime for as long as you want, at an even more affordable rate than a real tutor.

**Why use AI?**  
The need for AI here was is very justified since it is more of an addition to the app than the main focus. The app holds content made by a real human tutor, along with questions for each topic, and the AI is there to add an adaptive agent to the app for students to ask questions if they need it. Along with this, the agent can (and is refined to) create many exam style and past paper type questions for the student to practice on request, which is heavily useful since exam style questions are very important for revision, and apps can not use real exam questions, so the next best thing is to make your own, which tuned LLM's are very good at.

## 2. The UX

**Input**  
Although the app itself has many uses and input features, but here we will focus on the AI element to the product. The AI chatbot Richard has a typical chatbot setup, where at the moment the user can only send text to the agent.

**The Process**  
When the prompt is sent to the agent, it processes the prompt while first recieving prompt engineering and few shot prompting to give the agent a character of a professional gcse maths tutor, who has a professional playful personality and doesn't mind a joke. The agent specialises in exam style question generation and tentative teaching for the students struggles and requests.

**Output**  
The agent outputs a typical AI chatbot response of the generated questions and or theory for the student to read and then use or respond to. The agent remembers the conversation and can indeed provide answers to previous questions.

**User Stories**  
User story 1 - I want to revise for my maths exam but I don't know where to go. Mappth is the perfect place for this since there is a complete revision process within the app, ranging from revising specific topics for the exam to practicing actual exam questions and how to go about doing past papers correctly, along with how to do each question correctly.

User story 2 - I need help with my maths since I'm struggling to understand topics and I can ask the teacher since they're busy. Mappth is the perfect place for this help since the app is available whenever the user needs, and the AI helper Richard can take any question you have on the material, and can indeed teach you as if you were being taught by the teacher.

User story 3 - I've answered some past paper questions but I don't know if I've got the question right or not. Mappth is perfect for this once again since if you don't understand the markscheme then you can use the AI helper Richard to do the question for you, and also mark you answer to see if it is correct and follows the markscheme.

## 3. Possible Issues

- Slow response loading time
- Hallucination
- Uncertainty in the answer
- Questions outside the particular spec

**Fixes**  
The slow response loading time can be fixed in other generations of the app, but the solution given here is by adding a loading icon that the user will see when a message is sent and is there until the AI helper responds.

Hallucinations and uncertainty are also an issue which could be helped more in other generations of the app, but here since we only had access to prompt engineering, we specify CLEARLY the content that the agent has access to, the few shot prompting shows how to response if the agent is uncertain and if the content is not within the particular spec. This will aid the model in determining when and when not to respond, and when it does respond to do so in a way which uses enough tokens and explanations for the user so that the output aligns with out goals.

## 4. System Prompt spec

As mentioned earlier in the PRD, the agent itself has been prompt engineered for specfic prompt specs, and the particular prompt engineering will be within the change log which documents where we currently are and what we have changed to get here. As mentioned above, the general jist of the system prompt involves few shot prompting to convey a persona that is like an actual professional gcse maths tutor, that is slightly playful and likes a good joke. 

*THE ACTUAL SYSTEM PROMPT WILL BE PROVIDED HERE SHORTLY WHEN THE AUTHOR ADDS IT*

As we see, there are constraints for the model such as not allowing it to talk outside of the WJEC, AQA, OCR and EDEXCEL GCSE syllabus (basically all the same).

## 5. Evaluation

For the evaluation of the agent, we will use analytics to track the following:
- How many users used the agent out of total app users
- The time a user used the agent out of total app users time
- The % of people who found the agent useful (with a random sample of users)

For the overall product evaluation we will also use similar analytics:
- The time a user used the app
- The % of people who found the app useful (with a random sample of users)
- The return rate of users to the app
- The re-subscription rate of the users to the app

(base numbers)
Pass if:
- At least 95% of users use the agent
- At least 30% of users app time is spent with the agent
- At least 75% of users found the agent useful
- At least 20 minutes of app usage per session per user
- At least 75% of users found the app useful
- At least 75% of users return to use the app again
- At least 50% of users re-subscribe

## 6. Scope

For the current time, there is nothing out of scope. 
(This can change given time in the process.)
# Mappth - GCSE Revision App

**Product name:** Mappth  
**Date:** 2/01/2026  
**Owner:** Marcus Hanmer  
**Type:** EdTech

## 1. The Problem

**Pain point**  
Students who need help with GCSE maths may find it hard to get help, since it is difficult for the school itself to always deliver every need for the student, and outside of school the child is either left alone to teach themselves, or they get a personal tutor. The paint point with this is that the tutor will cost upwards of £30/hr if not more, and this is alot of money over time. Furthermore, each session is only on average an hour long, and is only on a particular time of day that is schedualed. There are many issues with this, and the idea for Mappth is to have a tutor in your pocket all of the time which is ready to teach anything, anytime for as long as you want, at an even more affordable rate than a real tutor.

**Why use AI?**  
The need for AI here is justified since it is a key addition to the app. The app holds content made by a real human tutor, along with questions for each topic, and the AI is there to add an adaptive agent to the app for students to ask questions if they need it. Along with this, the agent can create many exam style and past paper type questions for the student to practice on request. We engineer the LLM to be adapted for this agentic role.

## 2. The UX

**Input**  
Although the app itself has many uses and input features, but here we will focus on the AI element to the product. The AI chatbot Richard has a typical chatbot setup, where at the moment the user can only send text to the agent.

**The Process**  
When the prompt is sent to the agent, it processes the prompt while first recieving prompt engineering and few shot prompting to give the agent a character of a professional gcse maths tutor, who has a professional playful personality and doesn't mind a joke. The agent specialises in exam style question generation and tentative teaching for the students struggles and requests.

**Output**  
The agent outputs a typical AI chatbot response of the generated questions and or theory for the student to read and then use or respond to. The agent remembers the conversation and can indeed provide answers to previous questions.

**User Stories**  
User story 1 - As a GCSE student, I want to ask the agent specific questions about a topic I am revising, so that I can get immediate clarification without waiting for a teacher.

User story 2 - As a GCSE student, I want to request "exam-style" questions on a specific topic (e.g., Pythagoras), so that I can practice applying theory to the specific format of my exam board.

User story 3 - As a GCSE student, I want to have the AI explain why a specific mark scheme answer is correct, so that I can understand where I lost marks in past papers.

User story 4 - As a GCSE student, I want to receive a step-by-step breakdown of a solution, so that I can learn the methodology, not just the final answer.

## 3. Possible Issues

### Hallucinations

**Impact:** High  
1. Low temperature setting on LLM.
2. System prompt instructions to admit ignorance rather than guess.
3. Verify against connected knowledge base (RAG) where possible.

### Latency

**Impact:** Medium  
Implement streaming responses (token by token) and a visible loading state.

### Prompt Injection

**Impact:** Medium  
Strict guardrails preventing the user from changing Richard's persona or discussing inappropriate topics.

### Syllabus Drift

**Impact:** Medium  
System prompt must strictly limit scope to GCSE curriculum (WJEC, AQA, OCR, EDEXCEL).

## 4. System Prompt spec

As mentioned earlier in the PRD, the agent itself has been prompt engineered for specfic prompt specs, and the particular prompt engineering will be within the change log which documents where we currently are and what we have changed to get here. As mentioned above, the general jist of the system prompt involves few shot prompting to convey a persona that is like an actual professional gcse maths tutor, that is slightly playful and likes a good joke. 

*THE ACTUAL SYSTEM PROMPT WILL BE PROVIDED HERE SHORTLY WHEN THE AUTHOR ADDS IT*

As we see, there are constraints for the model such as not allowing it to talk outside of the WJEC, AQA, OCR and EDEXCEL GCSE syllabus (basically all the same).

## 5. Evaluation

**Feature success (The Agent)**  
- Adoption rate: > 40% of daily active users engage with the agent.
- Session depth: average conversation length > 5 turns.
- Sentiment: > 75% positive feedback.

**Product success (The App)**  
- Retention: > 40% Day 30 retention.
- Session length: average session > 15 minutes.
- Conversion: > 15% free trail to paid conversion rate.

## 6. Scope

**In Scope:**  
- Text based chat interface.
- Exam question generation (Text).
- Syllabus coverage: AQA, OCR, Edexcel, WJEC.

**Out of Scope:**  
- Image recognition.
- Voice interaction mode.
- A Level or other content.
- Non maths subjects.
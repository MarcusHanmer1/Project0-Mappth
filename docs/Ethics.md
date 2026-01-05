# Mappth - Ethics Assessment

**Status:** Active  
**Owner:** Marcus Hanmer, PM  
**Last updated:** 4/01/2026  
**Applicable Regulations:** UK GDPR and DPA 2018, Online Safety Act 2023, Equality Act 2010

## 1. Core principles

**Mission Statement:**  
To provide accessible and affordable math tutoring and revision help while prioritizing student safety and academic integrity.  

**The Pillars:**  
- Safety first: We never output harmful or age inappropriate content.  
- Pedagogical integrity: We value correct explanations over fast answers.  
- Anti dependency: We build tools to help students learn, not to do the work for them.

## 2. Risk Assessment

**Risk: Hallucinations**  
Description: Model produces mathematically incorrect formulas and or information.  
Severity: Critical  
Likelihood: Rare   
Mitigation: Use low temperature (0.2), implement RAG, strictly prompt engineer not to answer when not confident.  

**Risk: Plagiarism/Cheating**  
Description: Writing essays or doing homework without explanation.  
Severity: High  
Likelihood: Rare  
Mitigation: Prompt engineer to specifically always provide detailed descriptions with a clear goal of actually teaching like a tutor, and specifically use the Socratic method.  

**Risk: Tone policing:**   
Description: The bot becoming aggressive or inappropriate.  
Severity: High  
Likelihood: Rare   
Mitigation: Choose a model which already has the mitigating behaviour built in.  

**Risk: Prompt injection**  
Description: Users tricking the bot into ignoring its rules  
Severity: Critical  
Likelihood: Rare  
Mitigation: Choose a model which already has the mitigating behaviour built in.

## 3. Operational Guardrails

**Input Filter:**  
- Scan the input for particular keywords related to undesirable prompts (hate-speech, self-harm, sexual, prompt injections etc).  

**Systen Prompt Constraints:**  
- The model is strictly instructed via the system prompt to refuse requests unrelated to the UK GCSE Syllabus.  

**Output Filter:**  
- Check output for banned keywords before displaying to the student.

## 4. Data Governance and Privacy

[Link to privacy policy](https://www.mappth.net/english-privacy-policy)  

- Retention policy: Chat logs are not recorded and the Agent is given a new conversation ID every time the page is loaded (So can only have a conversation in one singular session).  
- Training data: No user data is collected at all as shown in the privacy policy, and so no training data is collected either!

## 5. Incidence Response

**The flagging mechanism:** The flagging mechanism is to contact the team on the apps reviews and issues page.  

**Review process:** App reviews and issues are reviewed by the product team weekly.  

**The kill switch:** In the event of a critical safety failure (e.g., the bot starts swearing), we will review the issue and immediately review it, take down the issue for production, then evaluate and re-release after the fix.

## 6. Transparency and User Disclosure

**Identity:** The product storeface clearly labels Richard as an 'AI Tutor' and not a real person.  

**Limitations:** We explicitly inform users that Richard is just a messanger agent that can only interact via message.

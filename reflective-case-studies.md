# Reflective Case Studies

## Introduction

This section presents three reflective case studies based on issues identified during the design, implementation and evaluation of my intelligent agent project.

The case studies use Rolfe, Freshwater and Jasper’s (2001) reflective framework:

1. What?
2. So what?
3. Now what?

## Supporting Evidence

1. [Week 7 System Design](week-7-design.html)
2. [Week 11 Final Implementation](week-11-implementation.html)
3. [Critical Project Evaluation](project-evaluation.html)
4. [ResearchMate Team Project](team-project.html)

# Case Study 1: Bias in Autonomous Decision Making

## What?

During the development of the research planning agent, I recognised that the system could generate recommendations that appeared objective but were influenced by assumptions within the model and system design.

For example, the system could recommend particular methodologies, research questions or academic approaches based on patterns within its training data rather than the specific requirements of the student’s discipline, institution or cultural context.

The prototype did not include a formal bias detection mechanism. Its outputs therefore depended heavily on the quality of the user input and the assumptions built into the system.

Before completing this project, I mainly associated bias with discriminatory outcomes involving protected groups. The design process showed me that bias can also occur when a system repeatedly favours particular research methods or treats one academic structure as universally appropriate.

I felt uneasy when I recognised that the structure I had designed could silently privilege certain research traditions. This made me question assumptions that I had previously treated as neutral.

## So what?

This mattered because students could interpret the output as neutral or academically authoritative.

A biased recommendation could narrow a student’s choices, favour commonly represented approaches and disadvantage less represented disciplines, perspectives or research traditions.

Bias can arise through training data, design assumptions, system objectives and the way outputs are presented, rather than only through explicitly discriminatory rules (Barocas, Hardt and Narayanan, 2023).

The issue also showed me that my own design decisions could contribute to bias. By defining the expected structure of an acceptable research plan, I was influencing what the system treated as valid or appropriate.

This made me recognise that developers are not neutral observers. They shape the assumptions, priorities and boundaries of the systems they create.

It also changed my understanding of technical quality. A system may appear consistent while repeatedly producing outputs based on a narrow set of assumptions.

## Now what?

In future development, I would introduce a formal bias review process during design and testing.

This would include:

1. Testing the system across different academic disciplines.
2. Comparing outputs for differently worded but equivalent topics.
3. Reviewing whether particular methodologies were repeatedly favoured.
4. Asking users to provide institutional and disciplinary context.
5. Presenting the output as one possible recommendation rather than a definitive answer.
6. Involving academic reviewers from different subject areas.
7. Recording known assumptions and limitations.

I would also make the assumptions built into the system visible to users.

This would allow users to understand that the recommendations were shaped by system rules, training data and design choices rather than representing universally correct academic guidance.

# Case Study 2: Explainable Decisions in Agents

## What?

The research planning agent could produce an aim, objectives, research questions and methodology suggestions, but it did not always explain clearly why each recommendation had been made.

The output could appear structured and convincing without showing the basis of the recommendations.

For example, the prototype could recommend a mixed methods approach without explaining which elements of the research topic justified combining qualitative and quantitative data.

This was particularly important when the system suggested a methodology. A student might receive a recommendation for qualitative, quantitative or mixed methods research without understanding why that choice was suitable.

I was initially satisfied that the output looked structured and professional. However, I became less confident when I recognised that users could not inspect or challenge the basis of the recommendations.

## So what?

This reduced transparency and made it harder for users to judge whether a recommendation was suitable.

An unexplained recommendation could encourage overreliance because users may assume that a confident output is also a correct output.

Explainability can help users understand, question and challenge automated recommendations rather than accepting outputs simply because they appear confident (Ribeiro, Singh and Guestrin, 2016).

The issue also limited the value of the system as a learning tool.

A student benefits more from understanding why a research question aligns with an objective than from simply receiving a completed answer.

The project therefore helped me understand that explainability is not only a technical feature. It is also an educational and professional responsibility.

An explainable agent should enable the user to inspect, question and challenge its output.

## Now what?

In a future version, I would add an explanation beneath each major recommendation.

The system could explain:

1. Why the proposed aim matches the topic.
2. How each objective contributes to the aim.
3. Why the research questions align with the objectives.
4. Why a particular methodology may be appropriate.
5. What assumptions were made.
6. What information was missing.
7. What alternative approaches could be considered.
8. How confident the system was in the recommendation.

I would also allow the user to ask questions such as:

1. Why did you recommend this method?
2. What alternative methodology could be used?
3. What information is missing from my topic?
4. How confident is the system in this suggestion?
5. What evidence supports this recommendation?

This would make the agent more transparent and more useful as an educational support tool.

It would also encourage users to engage critically with the output rather than accepting it without review.

# Case Study 3: Responsible Deployment of Intelligent Agents

## What?

The final implementation worked as a prototype, but it was not ready for unrestricted use by students.

The system could generate structured academic guidance, but source verification, privacy controls, academic quality evaluation and human review were limited.

There was a risk that users might rely on the generated content without checking it against academic literature, university guidance or supervisor feedback.

The system could therefore cause unintended harm even without deliberately harmful behaviour.

Although I was pleased that the prototype worked, I became more cautious about presenting technical success as evidence that the system was ready for real users.

## So what?

This highlighted the difference between building a functioning prototype and deploying a responsible system.

A technically successful output does not automatically mean that a system is safe, accurate or suitable for real users.

Responsible artificial intelligence requires risks to be identified, assessed and managed throughout the system lifecycle rather than considered only after deployment (National Institute of Standards and Technology, 2023).

In an academic context, inappropriate deployment could lead to:

1. Weak research proposals.
2. Inaccurate methodology choices.
3. Unsupported claims.
4. Reduced independent thinking.
5. Academic integrity concerns.
6. Inappropriate handling of personal or research data.
7. Excessive reliance on automated recommendations.
8. Loss of trust where outputs are inaccurate.

I learned that responsibility must be considered throughout the lifecycle of the system and should not be added only after implementation is complete.

I also recognised that the person developing the system remains responsible for how limitations are communicated and how users are protected from foreseeable harm.

## Now what?

Before real world deployment, I would require:

1. Clear user warnings and system boundaries.
2. Academic source verification.
3. Privacy and data protection controls.
4. Human review.
5. Academic quality testing.
6. Usability testing.
7. Monitoring of unsuitable outputs.
8. A process for reporting errors.
9. Clear explanations of system limitations.
10. Secure handling of user data.

I would position the system as a support tool rather than a replacement for academic supervision, independent research or professional judgement.

I would also ensure that users were reminded to verify the output against academic literature, university requirements and supervisor advice.

# Overall Reflection

The three case studies helped me recognise that intelligent agent development involves more than building a technically functional system.

Bias, explainability and responsible deployment are directly connected to software architecture, testing, user communication and professional accountability.

The project changed my understanding of responsible artificial intelligence.

I now see ethical considerations not as an additional discussion after development, but as practical requirements that should influence requirements, architecture, testing, user communication and deployment from the beginning.

The case studies also changed how I view my responsibility as a developer.

I am responsible not only for whether the system runs correctly, but also for considering who may be affected by its outputs, how recommendations may be interpreted and what safeguards are required before the system is used in practice.

In future projects, I will examine ethical and professional risks during requirements definition rather than waiting until the evaluation stage.

# References

Barocas, S., Hardt, M. and Narayanan, A. (2023) *Fairness and machine learning: Limitations and opportunities*. Cambridge, MA: MIT Press.

National Institute of Standards and Technology (2023) *Artificial Intelligence Risk Management Framework, AI RMF 1.0*. Gaithersburg, MD: National Institute of Standards and Technology. doi: 10.6028/NIST.AI.100-1.

Ribeiro, M.T., Singh, S. and Guestrin, C. (2016) ‘Why should I trust you? Explaining the predictions of any classifier’, in *Proceedings of the 22nd ACM SIGKDD International Conference on Knowledge Discovery and Data Mining*. New York: ACM, pp. 1135 to 1144. doi: 10.1145/2939672.2939778.

Rolfe, G., Freshwater, D. and Jasper, M. (2001) *Critical reflection in nursing and the helping professions: A user’s guide*. Basingstoke: Palgrave Macmillan.

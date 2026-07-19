# Reflective Case Studies

This section presents three reflective case studies based on issues identified during the design, implementation and evaluation of my intelligent-agent project.

The case studies use Rolfe, Freshwater and Jasper’s (2001) reflective framework:

- What?
- So what?
- Now what?

## Supporting Evidence

- [Week 7 System Design](week-7-design.html)
- [Week 11 Final Implementation](week-11-implementation.html)
- [Critical Project Evaluation](project-evaluation.html)

---

## Case Study 1: Bias in Autonomous Decision-Making

### What?

During the development of the research-planning agent, I recognised that the system could generate recommendations that appeared objective but were influenced by assumptions embedded within the model and system design.

For example, the system could recommend particular methodologies, research questions or academic approaches based on patterns within its training data rather than the specific requirements of the student’s discipline, institution or cultural context.

The prototype did not contain a formal bias-detection mechanism. Its outputs therefore depended heavily on the quality of the user input and the assumptions present within the underlying system.

Before completing this project, I mainly associated bias with discriminatory outcomes. The design process showed me that bias can also arise when a system repeatedly favours particular research methods or treats one academic structure as universally appropriate.

### So what?

This mattered because students could interpret the output as neutral or academically authoritative.

A biased recommendation could narrow a student’s choices, favour commonly represented approaches and disadvantage less represented disciplines, perspectives or research traditions.

Bias can arise through training data, design assumptions, system objectives and the way outputs are framed, rather than only through explicitly discriminatory rules (Barocas, Hardt and Narayanan, 2023).

The issue also showed me that my own design decisions could contribute to bias. By defining the expected structure of an acceptable research plan, I was influencing what the system treated as valid or appropriate.

This made me recognise that developers are not neutral observers. They shape the assumptions, priorities and boundaries of the systems they create.

### Now what?

In future development, I would introduce a bias-review process during design and testing.

This would include:

- testing the system across different academic disciplines;
- comparing outputs for differently worded but equivalent topics;
- reviewing whether certain methodologies were repeatedly favoured;
- asking users to provide institutional and disciplinary context;
- presenting the output as one possible recommendation rather than a definitive answer;
- involving academic reviewers from different subject areas.

I would also document the assumptions built into the system and make those assumptions visible to users.

---

## Case Study 2: Explainable Decisions in Agents

### What?

The research-planning agent could produce an aim, objectives, research questions and methodology suggestions, but it did not always explain clearly why each recommendation had been made.

The output could appear structured and convincing without showing the reasoning process behind the recommendations.

For example, the prototype could recommend a mixed-methods approach without showing which elements of the research topic justified combining qualitative and quantitative data.

This was particularly important when the system suggested a methodology. A student might receive a recommendation for qualitative, quantitative or mixed-method research without understanding the basis for that choice.

### So what?

This reduced transparency and made it harder for users to judge whether the recommendation was suitable.

An unexplained recommendation could encourage overreliance because users may assume that a confident output is also a correct output.

Explainability can help users understand, question and challenge automated recommendations rather than accepting outputs solely because they appear confident (Ribeiro, Singh and Guestrin, 2016).

The issue also limited the value of the system as a learning tool. A student benefits more from understanding why a research question aligns with an objective than from simply receiving a completed answer.

The project therefore helped me understand that explainability is not only a technical feature. It is also an educational and professional responsibility.

An explainable agent should enable the user to inspect, question and challenge its output.

### Now what?

In a future version, I would add an explanation beneath each major recommendation.

The system could explain:

- why the proposed aim matches the topic;
- how each objective contributes to the aim;
- why the research questions align with the objectives;
- why a particular methodology may be appropriate;
- what assumptions were made;
- what alternative approaches could be considered.

I would also allow the user to ask follow-up questions such as:

- Why did you recommend this method?
- What alternative methodology could be used?
- What information is missing from my topic?
- How confident is the system in this suggestion?

This would make the agent more transparent and more useful as an educational support tool.

---

## Case Study 3: Responsible Deployment of Intelligent Agents

### What?

The final implementation worked as a prototype, but it was not ready for unrestricted use by students.

The system could generate structured academic guidance, but source verification, privacy controls, academic-quality evaluation and human review were limited.

There was a risk that users might rely on the generated content without checking it against academic literature, university guidance or supervisor feedback.

The system could therefore cause unintended harm even without deliberately harmful behaviour.

### So what?

This highlighted the difference between building a functioning prototype and deploying a responsible system.

A technically successful output does not automatically mean that a system is safe, accurate or suitable for real users.

Responsible AI requires risks to be identified, assessed and managed throughout the system lifecycle rather than considered only after deployment (National Institute of Standards and Technology, 2023).

In an academic context, inappropriate deployment could lead to:

- weak research proposals;
- inaccurate methodology choices;
- unsupported claims;
- reduced independent thinking;
- academic-integrity concerns;
- inappropriate handling of personal or research data.

I learned that responsibility must be considered throughout the lifecycle of the system and should not be added only after implementation is complete.

### Now what?

Before real-world deployment, I would require:

- clear user warnings and system boundaries;
- academic source verification;
- privacy and data-protection controls;
- human-in-the-loop review;
- academic-quality and usability testing;
- monitoring and reporting of unsuitable outputs.

I would position the system as a support tool rather than a replacement for academic supervision, independent research or professional judgement.

---

## Overall Reflection

The three case studies helped me recognise that intelligent-agent development involves more than building a technically functional system.

Bias, explainability and responsible deployment are directly connected to software architecture, testing, user communication and professional accountability.

The project changed my understanding of responsible AI. I now see ethical considerations not as an additional discussion after development, but as practical requirements that should influence requirements, architecture, testing, user communication and deployment from the beginning.

# Reflective Case Studies

This section presents three reflective case studies based on issues that arose during the design, implementation and evaluation of my intelligent-agent project.

The case studies use Rolfe et al.'s reflective structure:

- What?
- So what?
- Now what?

---

## Case Study 1: Bias in Autonomous Decision-Making

### What?

During the development of the research-planning agent, I recognised that the system could generate recommendations that appeared objective but were influenced by the assumptions embedded within the model and system design.

For example, the system could suggest particular methodologies, research questions or academic approaches based on patterns in its training data rather than the specific requirements of the student's institution, discipline or cultural context.

The prototype did not contain a formal bias-detection mechanism. Its outputs therefore depended heavily on the quality of the user input and the assumptions already present within the underlying model.

### So what?

This mattered because students could interpret the output as neutral or academically authoritative.

A biased recommendation could narrow a student's choices, favour common research approaches and disadvantage less represented perspectives or disciplines.

The issue also showed me that bias is not limited to obviously discriminatory decisions. In an academic-support system, bias can appear through what the agent prioritises, excludes or presents as the standard approach.

I also recognised that my own design choices could contribute to bias. By defining the expected output structure, I was deciding what a valid research plan should look like.

This made me more aware that developers are not neutral observers. They influence the behaviour and boundaries of the systems they create.

### Now what?

In future development, I would introduce a bias-review process during design and testing.

This would include:

- testing the system across different academic disciplines;
- comparing outputs for differently worded but equivalent topics;
- reviewing whether certain methodologies are repeatedly favoured;
- asking users to provide institutional and disciplinary context;
- making clear that the output is one possible recommendation rather than a definitive answer;
- involving academic reviewers from different subject areas.

I would also document the assumptions built into the system and make them visible to users.

---

## Case Study 2: Explainable Decisions in Agents

### What?

The research-planning agent could produce an aim, objectives, research questions and methodology suggestions, but it did not always explain clearly why each recommendation had been made.

The output could appear structured and convincing without showing the reasoning process behind the recommendations.

This was particularly important when the system suggested a methodology. A student might receive a recommendation for qualitative, quantitative or mixed-method research without understanding the basis for that choice.

### So what?

This reduced transparency and made it harder for users to judge whether the recommendation was suitable.

An unexplained recommendation can encourage overreliance because users may assume that a confident output is also a correct output.

The issue also limited the value of the system as a learning tool. A student benefits more from understanding why a research question aligns with an objective than from simply receiving the completed answer.

The project therefore helped me understand that explainability is not only a technical feature. It is also an educational and professional responsibility.

An explainable agent should help the user inspect, question and challenge its output.

### Now what?

In a future version, I would add an explanation beneath each major recommendation.

For example, the system could explain:

- why the proposed aim matches the topic;
- how each objective contributes to the aim;
- why the research questions align with the objectives;
- why a particular methodology may be appropriate;
- what assumptions were made;
- what alternative approaches could also be considered.

I would also allow the user to ask follow-up questions such as:

- Why did you recommend this method?
- What alternative methodology could be used?
- What information is missing from my topic?
- How confident is the system in this suggestion?

This would make the agent more transparent and more useful as a learning aid.

---

## Case Study 3: Responsible Deployment of Intelligent Agents

### What?

The final implementation worked as a prototype, but it was not ready for unrestricted use by students.

The system could generate structured academic guidance, but source verification, privacy controls, academic-quality evaluation and human review were limited.

There was a risk that users might rely on the generated content without checking it against academic literature, university guidance or supervisor feedback.

The system could therefore produce unintended harm even without deliberately harmful behaviour.

### So what?

This highlighted the difference between building a functioning prototype and deploying a responsible system.

A technically successful output does not automatically mean that the system is safe, accurate or suitable for real users.

In an academic context, inappropriate deployment could lead to:

- weak research proposals;
- inaccurate methodology choices;
- unsupported claims;
- reduced independent thinking;
- academic-integrity concerns;
- inappropriate handling of personal or research data.

I learned that responsibility must be considered throughout the lifecycle of the system, not added only after the implementation is complete.

### Now what?

Before real-world deployment, I would require:

- clear user warnings and limitations;
- source verification;
- privacy and data-protection controls;
- human-in-the-loop review;
- academic-quality testing;
- usability testing with real students;
- evaluation by supervisors or research-methods specialists;
- logging and monitoring of problematic outputs;
- a method for users to report unsuitable recommendations;
- clear boundaries on what the system can and cannot do.

I would position the system as a support tool rather than a replacement for academic supervision or independent judgement.

---

## Overall Reflection

The three case studies helped me recognise that intelligent-agent development involves more than building a technically functional system.

Bias, explainability and responsible deployment are directly connected to software architecture, testing, user communication and professional accountability.

The project changed my understanding of responsible AI. I now see ethical considerations as practical design requirements that should shape the system from the beginning.

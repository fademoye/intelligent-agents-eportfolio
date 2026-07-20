# Week 11 Final Implementation

## Project Overview

The Week 11 implementation was an individual intelligent-agent project focused on academic research planning.

The system was designed to help postgraduate students transform an initial research topic into a structured research plan containing:

- a research aim;
- research objectives;
- research questions;
- a methodology suggestion;
- a clearly presented final output.

The implementation developed from the wider ResearchMate concept explored during the group project. However, the coding, testing and final prototype presented on this page were completed as my individual work.

## Problem Being Addressed

Postgraduate students can experience difficulty aligning their research topic, aim, objectives, research questions and methodology.

The system was therefore designed to provide structured guidance that could help users develop a more coherent initial research plan.

It was intended to support academic thinking rather than replace independent research, academic literature, university guidance or supervisor feedback.

## Final System Architecture

The final implementation used a modular Python structure.

The main components included:

- `main.py` – started the application and managed interaction with the user;
- `agent.py` – coordinated the overall research-planning workflow;
- `planner.py` – developed the structure of the research plan;
- `retriever.py` – provided simplified retrieval functionality within the prototype;
- `processor.py` – processed the user input and intermediate information;
- `output_generator.py` – produced the final structured output;
- test files – assessed the main components and overall workflow.

The implementation used agent-inspired modular components coordinated through a defined workflow. It did not implement fully autonomous agents communicating independently with one another.

## Final Workflow

1. The user entered a research topic.
2. The system received and processed the input.
3. The planning component identified the required research elements.
4. The coordinating component directed the relevant modules.
5. The system generated a research aim, objectives, research questions and methodology suggestion.
6. The completed research plan was presented to the user for review.

## Technologies Used

The final implementation used:

- Python;
- GitHub;
- modular programming;
- pytest;
- command-line interaction;
- structured output generation.

## Individual GitHub Repository

The individual GitHub repository contains the final source code, project structure, testing files and technical documentation.

[View the individual implementation on GitHub](https://github.com/fademoye/LLM-Planning-Agent-Project)

## Code Structure

The project was divided into separate modules rather than placing all functionality into one large script.

This approach improved:

- readability;
- maintainability;
- testability;
- separation of responsibilities;
- future extensibility.

Separating the planner, processor, retriever, coordinating agent and output-generation functions also made it easier to identify errors and test individual components.

## Testing

The system was evaluated using unit and functional testing.

The tests examined:

- whether the planning component produced the expected structure;
- whether the overall workflow operated correctly;
- whether the final output contained the required research-planning elements;
- whether the main modules worked together successfully.

Eight tests passed successfully.

Passing the tests increased confidence that the technical workflow operated as intended. However, technical success did not prove that every generated recommendation was academically accurate, relevant or suitable.

Further evaluation would be required to assess:

- alignment between the aim, objectives and research questions;
- suitability of the suggested methodology;
- consistency across different research topics;
- usefulness to postgraduate students;
- feedback from academic supervisors.

## Implementation Evidence

The following evidence demonstrates the operation, structure and testing of my individual Week 11 implementation.

### System Running

This screenshot shows the research-planning application running successfully through the command-line interface.

![Research-planning system running](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/screenshot%20of%20the%20system%20running%3B.png)

[Open the system-running screenshot](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/screenshot%20of%20the%20system%20running%3B.png)

### User Input

This screenshot shows an example research topic entered into the system.

![Example research topic entered by the user](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/screenshot%20of%20user%20input%3B.png)

[Open the user-input screenshot](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/screenshot%20of%20user%20input%3B.png)

### Generated Output

This screenshot shows the structured research plan generated by the system.

![Structured research plan generated by the system](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/screenshot%20of%20generated%20output%3B.png)

[Open the generated-output screenshot](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/screenshot%20of%20generated%20output%3B.png)

### Project Structure

This screenshot shows the modular structure of the individual project, including the main application files, agent components and testing files.

![Modular project structure](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/project-structure.png)

[Open the project-structure screenshot](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/project-structure.png)

### Testing Evidence

This screenshot shows the eight successful pytest results used to verify the system components and research-planning workflow.

![Eight successful pytest results](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/tests_passed_8.png)

[Open the pytest-results screenshot](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/tests_passed_8.png)

## Presentation Evidence

The individual presentation summarised the project problem, architecture, implementation, testing, limitations and proposed future improvements.

- [View the presentation slides](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/Presentation%20slides.pdf)
- [Read the presentation transcript](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/Presentation%20transcript.pdf)

## Relationship to the ResearchMate Group Design

The individual Week 11 prototype developed from the broader ResearchMate multi-agent design created during the group project.

The group design proposed a hybrid architecture involving a Planning Agent, Retrieval Agent, Processing Agent, Ranking Agent and Storage/Output Agent.

The individual implementation reduced this broader design to a more achievable modular prototype that could be completed, tested and evaluated within the available timeframe.

![ResearchMate hybrid multi-agent architecture](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)

[Open the ResearchMate architecture diagram](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)

## Limitations

The final implementation was a functional prototype rather than a production-ready academic-support system.

Its main limitations included:

- the quality of the output depended on the quality and detail of the user input;
- complete live academic-database retrieval and source verification were not implemented;
- the system could not guarantee that every aim, objective, research question or methodology recommendation was academically appropriate;
- testing focused mainly on technical functionality rather than educational quality;
- the command-line interface was less accessible for non-technical users;
- the system did not provide a detailed explanation for every recommendation;
- further testing with students and academic supervisors would be required;
- additional privacy, security and responsible-use safeguards would be needed before deployment.

These limitations mean that users would still need to verify the generated output against academic literature, university requirements and supervisor feedback.

## Ethical and Professional Considerations

The system could generate plausible recommendations that appeared authoritative even when they required further academic verification.

This created risks relating to:

- inaccurate or unsupported guidance;
- student overreliance;
- bias in methodology recommendations;
- weak explainability;
- privacy and data protection;
- academic-integrity concerns.

The system was therefore positioned as a support tool rather than an authoritative academic adviser.

A responsibly deployed version would require:

- academic-source verification;
- clear user warnings;
- explanations for major recommendations;
- human review;
- privacy safeguards;
- monitoring of unsuitable outputs;
- appropriate handling of user data.

## What I Learned

The implementation strengthened my understanding of modular Python development.

Separating the planner, processor, retriever, coordinating agent and output generator made the system easier to understand, maintain and test.

I also developed a stronger practical understanding of intelligent-agent design. I learned that an agent-based system requires clearly defined responsibilities and coordination between components, rather than simply dividing code into several files.

Testing and debugging helped me recognise the difference between technical correctness and output quality. A system can execute successfully while still producing academic guidance that needs human review and source verification.

The project also improved my project-scoping skills. The original ResearchMate concept was broader than the final implementation, so I prioritised the core research-planning workflow that could be completed and tested within the available timeframe.

Finally, the project increased my awareness of responsible AI development. Academic-support systems should be transparent about their limitations and should support rather than replace human judgement.

## Connection to Learning Outcomes

### Learning Outcome 1

The implementation supported my ability to analyse agent-based architectures by allowing me to compare the broader Week 7 multi-agent design with the more focused modular Week 11 prototype.

Supporting evidence:

- [Week 7 System Design](week-7-design.html)
- [ResearchMate Team Project](team-project.html)
- [ResearchMate Architecture Diagram](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)
- [Critical Project Evaluation](project-evaluation.html)

### Learning Outcome 2

The system applied intelligent-agent techniques to the real-world problem of helping postgraduate students align their research topic, aim, objectives, research questions and methodology.

The evaluation also considered technical risk and uncertainty, including input quality, source verification and output reliability.

Supporting evidence:

- [System Running Screenshot](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/screenshot%20of%20the%20system%20running%3B.png)
- [Example User Input Screenshot](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/screenshot%20of%20user%20input%3B.png)
- [Generated Research Plan Screenshot](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/screenshot%20of%20generated%20output%3B.png)
- [Passed Pytest Results](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/tests_passed_8.png)
- [Critical Project Evaluation](project-evaluation.html)

### Learning Outcome 3

I used Python, GitHub, modular software design and pytest to design, implement and evaluate the prototype.

I also considered legal, social, ethical and professional issues, including privacy, academic integrity, bias, explainability, data reliability and responsible deployment.

Supporting evidence:

- [Individual GitHub Project Repository](https://github.com/fademoye/LLM-Planning-Agent-Project)
- [Project Structure Screenshot](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/project-structure.png)
- [Passed Pytest Results](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/tests_passed_8.png)
- [Reflective Case Studies](reflective-case-studies.html)

### Learning Outcome 4

Although the final implementation was completed individually, it developed from the wider ResearchMate group project.

The process strengthened my understanding of virtual teamwork, project ownership, role allocation, documentation and the distinction between collaborative and individual contributions.

Supporting evidence:

- [ResearchMate Team Project](team-project.html)
- [Team Meeting Notes](team-meetings.html)
- [ResearchMate Architecture Diagram](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)
- [Final Reflection](final-reflection.html)

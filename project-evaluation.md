# Critical Project Evaluation

## Introduction

This section critically evaluates the development of my intelligent-agent project by comparing the Week 7 design with the Week 11 implementation.

The original design proposed a multi-agent academic research-planning system that would support students in developing aligned research topics, aims, objectives, research questions and methodology.

The final implementation retained this central purpose but reduced the overall scope in order to produce a working and testable prototype within the available timeframe.

## Comparison of Week 7 Design and Week 11 Implementation

| Area | Week 7 Design | Week 11 Implementation | Evaluation |
|---|---|---|---|
| Project scope | A broader multi-agent research-support system with several specialist components | A focused research-planning prototype | Reducing the scope made the project more achievable and testable |
| Architecture | A multi-agent design containing planning, retrieval, processing, analysis and output-generation agents | A modular Python implementation with separate planning, processing, retrieval and output components | The final structure preserved modularity but simplified the level of agent autonomy |
| User input | Students would enter a research topic or area of interest | Users entered a research topic through the command line | The implemented interaction was simple but sufficient for demonstrating the workflow |
| Retrieval | The system was expected to retrieve relevant academic information | Retrieval capability was limited within the prototype | This reduced complexity but also limited source verification |
| Output | A detailed and structured academic research plan | A structured output containing aims, objectives, questions and methodology guidance | The core project objective was achieved |
| Testing | Testing was considered during the design stage | Unit and functional tests were completed using pytest | Testing provided evidence that the main components and workflow operated correctly |
| Deployment | The design suggested a more complete intelligent system | The final version remained a local prototype | The system demonstrated feasibility but was not production-ready |
| Ethical safeguards | Bias, reliability and overreliance were identified as risks | Limitations and responsible-use considerations were documented | Ethical risks were recognised but not fully implemented as technical safeguards |

## What Worked Well

One of the strongest aspects of the final implementation was its modular structure.

Separating the planner, processor, retriever, output generator and coordinating agent improved readability and made the system easier to test. This was more effective than placing all functionality in one large script.

The project also successfully addressed the central user problem. The final system could accept a research topic and produce a structured research-planning output containing an aim, objectives, questions and methodology suggestions.

Testing was another important strength. Unit and functional tests provided evidence that individual components and the main workflow operated as expected.

The use of GitHub also supported version control, documentation and professional presentation of the implementation.

## What Did Not Work as Originally Planned

The final implementation did not achieve the full level of autonomy proposed during the Week 7 design.

The original concept included stronger retrieval, analysis and collaboration between specialist agents. In practice, the prototype relied on a simplified modular workflow.

Source verification was also limited. Although the system could generate structured guidance, it could not confirm that every output was supported by reliable academic literature.

The interface was command-line based rather than a polished web application. This was acceptable for a prototype but reduced usability for non-technical users.

Testing focused mainly on functionality. It did not fully evaluate the academic quality, accuracy or usefulness of the generated research plans.

## Reasons for the Changes

The main reason for reducing the scope was the need to produce a complete, working and testable solution within the available timeframe.

The original design was ambitious and included several components that would have required more development, external services and evaluation.

There were also technical constraints relating to source retrieval, integration and validation.

The final decision was therefore to prioritise the core research-planning workflow rather than implement several incomplete features.

## Technical Evaluation

From a software-development perspective, the modular structure was appropriate for the prototype.

It improved separation of responsibilities and created a clearer relationship between system components.

However, the final implementation was not a fully autonomous multi-agent system in the strongest sense. The components behaved more like coordinated modules within a guided workflow.

This distinction is important because a modular program should not automatically be described as a sophisticated multi-agent system without evidence of meaningful autonomy, communication and independent decision-making.

The project therefore demonstrated agent-inspired architecture and coordination, but further development would be needed to create a more advanced multi-agent system.

## Evaluation of Testing

The completed tests showed that the system could execute the expected workflow and produce structured outputs.

This increased confidence in the technical stability of the prototype.

However, passing tests did not prove that the research guidance was academically valid.

A more complete evaluation would need to examine:

- relevance of the generated aims and objectives;
- alignment between aims, questions and methodology;
- accuracy of suggested methods;
- consistency across different inputs;
- user satisfaction;
- academic-supervisor feedback;
- potentially biased or misleading recommendations.

This demonstrated that technical testing and output-quality evaluation are different activities.

## Ethical and Professional Evaluation

The project raised several ethical and professional concerns.

The system could generate plausible but unsuitable academic recommendations. Students might over-rely on the output if the system appeared authoritative.

The absence of full source verification also created a risk of inaccurate or unsupported guidance.

Bias could be introduced through the language model, training data or assumptions embedded within the system design.

A responsibly deployed version would therefore require:

- clear limitations and disclaimers;
- source verification;
- human review;
- privacy protection;
- transparent explanation of how outputs were produced;
- mechanisms for identifying harmful or misleading recommendations.

The system should support academic judgement rather than replace supervisors or independent research.

## Overall Evaluation

The final implementation was successful as a functional prototype.

It demonstrated modular design, intelligent-agent concepts, structured output generation, testing and critical consideration of limitations.

However, it did not fully achieve the wider ambition of the Week 7 design.

The project was therefore valuable not because it created a complete production system, but because it showed how a broad concept could be reduced into a realistic implementation and evaluated honestly.

## Future Improvements

Future development should include:

1. integration with reliable academic databases;
2. stronger source verification;
3. a web-based interface;
4. improved input validation;
5. more advanced agent communication;
6. human-in-the-loop review;
7. usability testing with postgraduate students;
8. evaluation by academic supervisors;
9. explainable recommendations;
10. privacy and data-protection controls.

## What I Would Do Differently

If completing the project again, I would define the minimum viable product earlier.

I would also create the evaluation criteria before implementation so that both technical performance and output quality could be measured.

I would include more frequent testing throughout development rather than concentrating most testing near the end.

Finally, I would distinguish more clearly between modular software components and truly autonomous agents when describing the architecture.

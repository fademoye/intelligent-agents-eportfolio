# Final Reflection

## Introduction

This reflection evaluates my learning and development throughout the Intelligent Agents module. It considers my experience of studying agent architectures, contributing to the ResearchMate group project, designing an intelligent-agent system and implementing an individual research-planning prototype.

The reflection uses Rolfe et al.'s (2001) framework of What?, So what? and Now what? to examine the technical, professional and personal learning that developed during the module.

## What?

The module introduced me to different types of intelligent-agent systems, including reactive, deliberative, hybrid and multi-agent architectures. Through the practical activities, discussions and project work, I moved from understanding these approaches theoretically to considering how they could be applied to a real problem.

The main group project was ResearchMate, a proposed multi-agent system intended to support students with academic research planning. The system was designed to help users develop a research topic, aim, objectives, research questions and methodology. The group considered a hybrid architecture involving several specialist agents, including planning, retrieval, processing, analysis and output-generation components.

My individual Week 11 implementation focused on a narrower version of the same problem. I developed a modular Python prototype that accepted a research topic and produced a structured research plan. The system included separate modules for planning, processing, retrieval, coordination and output generation. I also completed unit and functional testing using pytest.

The project did not fully reproduce the ambition of the Week 7 design. The final prototype was less autonomous and had more limited retrieval and source-verification capabilities. However, it produced a functioning and testable implementation that demonstrated the central research-planning workflow.

## So what?

One of my most important areas of learning was project scoping. During the design stage, I was attracted to the idea of building a broad multi-agent system with several specialised functions. However, the original concept was more ambitious than could realistically be completed and evaluated within the available timeframe.

At first, reducing the scope felt like a compromise. I was concerned that simplifying the architecture might make the project appear less technically advanced. As the implementation progressed, I recognised that completing a smaller, coherent and testable system was more valuable than presenting a larger design with incomplete functionality.

This changed the way I think about technical ambition. A strong project is not defined only by the number of features it contains. It also depends on whether the core problem is clearly understood, whether the architecture is appropriate and whether the result can be evaluated honestly.

The modular structure of the implementation also strengthened my software-development skills. Separating the system into planner, processor, retriever and output components made the responsibilities of each part clearer. It also made testing easier and reduced the risk of placing all the logic in one large script.

Testing was another important learning experience. Passing the unit and functional tests gave me confidence that the technical workflow operated as expected. However, I also learned that technical tests only answer part of the evaluation question. A system can execute correctly while still producing weak, biased or academically unsuitable recommendations.

This distinction helped me understand the difference between software correctness and output quality. A more complete evaluation would need to involve students, research supervisors and academic-methodology specialists.

The group project also developed my understanding of virtual teamwork. Working in a distributed team required communication, task coordination, shared decision-making and clarity about individual responsibilities.

At times, uncertainty about project ownership and scope created frustration. I found that when roles were not clearly documented, it became more difficult to understand what each person was responsible for and how the individual contributions fitted together.

This affected my behaviour by making me focus more strongly on documenting my own contribution and ensuring that the final individual work could be clearly distinguished from the group project.

The experience showed me that effective teamwork requires more than attending meetings. Decisions, responsibilities, deadlines and dependencies need to be recorded. I now recognise the value of using clearer role allocation, meeting notes and action tracking from the beginning of a project.

The module also changed my understanding of ethical issues in intelligent-agent development. Before the project, I viewed ethics mainly as a separate evaluation topic. During the implementation, I began to see bias, explainability and responsible deployment as practical design concerns.

For example, a research-planning agent may produce recommendations that appear authoritative but are influenced by training-data patterns or system assumptions. It may also recommend a methodology without explaining why it is suitable.

This creates a risk of student overreliance. The system should therefore support academic judgement rather than replace independent research or supervisor guidance.

## Now what?

In future projects, I will define the minimum viable product earlier and develop explicit evaluation criteria before implementation begins. This will help me distinguish essential features from desirable but non-critical additions.

I will also introduce testing throughout the development process rather than treating it mainly as a final-stage activity. In addition to unit and functional testing, I will include output-quality criteria, user testing and expert review.

For future group work, I will encourage the team to document roles, responsibilities and decisions from the first meeting. A simple responsibility matrix, agreed meeting notes and action tracker would reduce ambiguity and make individual contributions easier to evidence.

Technically, I would like to improve my understanding of agent orchestration, source retrieval, vector databases and human-in-the-loop controls. These capabilities would support a more advanced version of the ResearchMate concept.

I will also treat ethical requirements as part of the system architecture. Future agent-based systems I develop should include explainable recommendations, clear limitations, privacy controls, source verification and mechanisms for human review.

Overall, the module strengthened my understanding of intelligent-agent systems, modular Python development, testing, teamwork and responsible AI. More importantly, it changed how I approach project development. I now place greater value on realistic scope, transparent evaluation, documented collaboration and responsible design.

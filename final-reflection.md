# Final Reflection

## Introduction

This reflection evaluates my learning and development throughout the Intelligent Agents module. It considers my experience of studying agent architectures, contributing to the ResearchMate group project, designing an intelligent agent system and implementing an individual research planning prototype.

The reflection uses Rolfe, Freshwater and Jasper’s (2001) framework of What?, So what? and Now what? to examine the technical, professional and personal learning that developed during the module.

## What?

The module introduced me to different types of intelligent agent systems, including reactive, deliberative, hybrid and multi agent architectures. Through the practical activities, discussions and project work, I moved from understanding these approaches theoretically to considering how they could be applied to a real problem.

The main group project was ResearchMate, a proposed hybrid multi agent system for academic research automation. The design included Planning, Retrieval, Processing, Ranking and Storage Agents. These agents were intended to coordinate the decomposition of research queries, retrieval of academic sources, summarisation of information, assessment of source relevance and credibility, and production of structured outputs.

The Planning Agent was intended to coordinate the wider workflow. It would interpret the user’s query, divide it into subtasks and direct the other specialist agents. The wider design also considered the use of a deliberative Belief, Desire and Intention approach alongside more reactive retrieval and processing functions.

My individual Week 11 implementation focused on a narrower version of the wider ResearchMate concept. I developed a modular Python prototype that accepted a research topic and produced a structured research plan. The system included separate components for planning, processing, simplified retrieval, coordination and output generation. I also completed unit and functional testing using pytest.

The individual implementation did not reproduce the full ambition of the Week 7 design. It was less autonomous and had more limited retrieval and source verification capabilities. However, it produced a functioning and testable prototype that demonstrated the central research planning workflow.

The distinction between modular software components and genuinely interacting autonomous agents is important when evaluating an agent based design. Wooldridge (2009) explains that intelligent agents require characteristics such as autonomy, responsiveness and purposeful behaviour. This helped me recognise that dividing software into separate files does not automatically make it a multi agent system.

## So what?

One of my most important areas of learning was project scoping. During the design stage, I was attracted to the idea of building a broad multi agent system with several specialised functions. The original concept included planning, academic retrieval, processing, credibility ranking, storage and output generation.

However, the proposed architecture was more ambitious than could realistically be completed and evaluated within the available timeframe.

At first, reducing the scope felt like a compromise. I was concerned that simplifying the architecture might make the project appear less technically advanced. I initially associated technical quality with the number of agents, features and technologies included in the design.

As the implementation progressed, I recognised that completing a smaller, coherent and testable system was more valuable than presenting a larger design with incomplete functionality.

I responded to the growing scope by prioritising the core research planning workflow. I focused on creating a system that could accept a user topic and generate a structured aim, objectives, research questions and methodology suggestion. I also separated the implementation into modules that could be understood and tested independently.

This changed the way I think about technical ambition. A strong project is not defined only by the number of features it contains. It also depends on whether the core problem is clearly understood, whether the architecture is appropriate, whether the implementation is reliable and whether the result can be evaluated honestly.

The modular structure of the implementation strengthened my software development skills. Separating the system into planning, processing, retrieval, coordination and output components made the responsibility of each part clearer. It also made testing easier and reduced the risk of placing all the program logic in one large script.

I learned that modularity can improve readability, maintainability and testability. However, I also learned that modularity should not be confused with agent autonomy. A genuine agent based design requires clearly defined responsibilities, information flows, decision making and coordination between components.

Testing was another important learning experience. Passing the unit and functional tests gave me confidence that the technical workflow operated as expected. It showed that the main components could work together and that the system could generate the expected output structure.

However, I also learned that technical tests answer only part of the evaluation question. A system can execute correctly while still producing weak, biased or academically unsuitable recommendations.

This distinction helped me understand the difference between software correctness and output quality. Technical testing can confirm that the code behaves as intended, but it cannot automatically determine whether a research aim is academically appropriate, whether the objectives align with the research questions or whether a methodology recommendation is suitable.

A more complete evaluation would need to involve postgraduate students, research supervisors and academic methodology specialists. It would also require criteria for assessing relevance, coherence, accuracy, explainability and usefulness.

The group project developed my understanding of virtual teamwork. Working in a distributed team required communication, task coordination, shared decision making and clarity about individual responsibilities.

At times, uncertainty about project ownership and scope created frustration. I found that when roles were not clearly documented, it became more difficult to understand what each person was responsible for and how the individual contributions fitted together.

This affected my behaviour by making me focus more strongly on documenting my own contribution while continuing to engage with the shared project. It also encouraged me to distinguish clearly between the group design and my individual implementation.

The experience showed me that effective teamwork requires more than attending meetings. Decisions, responsibilities, deadlines and dependencies need to be recorded. I now recognise the value of using clear role allocation, meeting notes, action tracking and regular progress reviews from the beginning of a project.

I also learned that evidence of contribution should be collected during the project rather than reconstructed at the end. Screenshots, meeting records, document history and task assignments provide stronger evidence than general descriptions of participation.

The module also changed my understanding of ethical issues in intelligent agent development. Before the project, I viewed ethics mainly as a separate evaluation topic. During the implementation, I began to see bias, explainability, privacy and responsible deployment as practical design concerns.

For example, a research planning agent may produce recommendations that appear authoritative but are influenced by training data patterns, simplified rules or assumptions built into the system. It may recommend a particular methodology without explaining why that methodology is suitable.

This creates a risk of student overreliance. A user may accept a plausible output without checking it against academic literature, university requirements or supervisor advice.

The system should therefore support academic judgement rather than replace independent research or human guidance.

The National Institute of Standards and Technology (2023) emphasises that artificial intelligence risks should be identified and managed throughout the design, development, deployment and monitoring of a system. This reinforced my understanding that responsible artificial intelligence cannot be treated only as a final compliance exercise.

Ethical requirements should influence the architecture itself. For ResearchMate, this would include source verification, transparent explanations, privacy controls, user warnings and opportunities for human review.

## Now what?

In future projects, I will define the minimum viable product earlier and develop explicit evaluation criteria before implementation begins. This will help me distinguish essential functions from desirable additions and future development opportunities.

I will begin by identifying the main user problem, the minimum features required to address it and the evidence needed to demonstrate success. I will then review whether each proposed agent or component is necessary.

I will also introduce testing throughout the development process rather than treating it mainly as a final stage activity. In addition to unit and functional testing, I will include output quality criteria, user testing and expert review.

For a research planning system, the evaluation criteria should examine alignment between the topic, aim, objectives, research questions and methodology. It should also consider clarity, usefulness, source reliability and the level of explanation provided to the user.

For future group work, I will encourage the team to document roles, responsibilities and decisions from the first meeting. A simple responsibility matrix, agreed meeting notes and action tracker would reduce ambiguity and make individual contributions easier to evidence.

I would also ensure that each task has a named owner, expected output and agreed deadline. Progress should be reviewed during each meeting and any changes should be recorded.

Technically, I would like to improve my understanding of agent orchestration, academic source retrieval, vector databases and human in the loop controls. These capabilities would support a more advanced version of the ResearchMate concept.

A future version could include live retrieval from academic databases, credibility scoring, source comparison and explanations showing why particular recommendations were generated.

I will also treat ethical requirements as part of the system architecture. Future agent based systems I develop should include explainable recommendations, clear limitations, privacy controls, source verification and mechanisms for human review.

Overall, the module strengthened my understanding of intelligent agent systems, modular Python development, testing, teamwork and responsible artificial intelligence.

More importantly, it changed how I approach project development. I now place greater value on realistic scope, transparent evaluation, documented collaboration and responsible design.

## References

National Institute of Standards and Technology (2023) *Artificial Intelligence Risk Management Framework, AI RMF 1.0*. Gaithersburg, MD: National Institute of Standards and Technology. doi: 10.6028/NIST.AI.100-1.

Rolfe, G., Freshwater, D. and Jasper, M. (2001) *Critical reflection in nursing and the helping professions: A user’s guide*. Basingstoke: Palgrave Macmillan.

Wooldridge, M. (2009) *An introduction to multiagent systems*. 2nd edn. Chichester: Wiley.

# Final Reflection

## Introduction

This reflection evaluates my learning and development throughout the Intelligent Agents module. It considers my experience of studying agent architectures, contributing to the ResearchMate group project, designing an intelligent agent system and implementing an individual research planning prototype.

The reflection uses Rolfe, Freshwater and Jasper’s (2001) framework of What?, So what? and Now what? to examine my technical, professional and personal learning.

## What?

The module introduced me to reactive, deliberative, hybrid and multi agent architectures. Through discussions, practical activities and project work, I moved from understanding these approaches theoretically to considering how they could address a real problem.

The group project was ResearchMate, a proposed hybrid multi agent system for academic research automation. The design included Planning, Retrieval, Processing, Ranking and Storage Agents. These agents were intended to coordinate the interpretation of research queries, retrieval of academic sources, summarisation of information, assessment of credibility and production of structured outputs.

The Planning Agent was intended to coordinate the workflow by interpreting the user query, dividing it into tasks and directing the specialist agents. The design combined a deliberative Belief, Desire and Intention approach with more reactive retrieval and processing functions.

My individual Week 11 project focused on a narrower version of the concept. I developed a modular Python prototype that accepted a research topic and generated a structured research plan. It included separate components for planning, processing, simplified retrieval, coordination and output generation. I also completed unit and functional testing using pytest.

The prototype did not reproduce the full ambition of the Week 7 design. It had limited retrieval, source verification and autonomous behaviour. However, it produced a functioning and testable implementation of the main research planning workflow.

Wooldridge (2009) explains that intelligent agents require characteristics such as autonomy, responsiveness and purposeful behaviour. This helped me recognise that dividing software into modules does not automatically create a genuine multi agent system.

## So what?

One of my most important areas of learning was project scoping. During the design stage, I was attracted to the idea of creating a broad system with several specialist agents. I initially associated technical strength with the number of agents, technologies and features included.

The proposed system was more ambitious than could realistically be implemented and evaluated within the available timeframe.

As implementation progressed, I realised that completing a coherent and testable system was more valuable than presenting a larger design with incomplete functionality. I therefore prioritised the core research planning workflow and organised the system into modules that could be understood and tested separately.

This changed my understanding of technical ambition. A strong project is not defined only by the number of features it contains. It also depends on whether the problem is clearly understood, the architecture is appropriate and the results can be evaluated honestly.

The modular structure strengthened my Python development skills. Separating the planner, processor, retriever, coordinator and output functions improved readability, maintenance and testing. However, I also learned that modularity should not be confused with autonomy. An agent based system needs defined responsibilities, information flows, decision making and coordination.

Testing was another important learning experience. Passing the unit and functional tests increased my confidence that the technical workflow operated as expected. However, I learned that technical correctness does not guarantee output quality.

A system can execute successfully while producing weak, biased or academically unsuitable recommendations. Technical tests cannot determine whether a research aim is appropriate, whether objectives align with questions or whether a suggested methodology is suitable. A fuller evaluation would require students, supervisors and methodology specialists.

The group project also developed my understanding of virtual teamwork. Working in a distributed team required communication, shared decisions and clear responsibilities.

At times, uncertainty about roles and scope created frustration. When responsibilities were not recorded clearly, it became difficult to understand ownership and progress. This encouraged me to document my contribution more carefully and to distinguish the group design from my individual implementation.

I learned that effective teamwork requires more than attending meetings. Decisions, responsibilities and deadlines need to be recorded.

The module changed my understanding of responsible artificial intelligence. Before the project, I viewed ethics mainly as an evaluation topic. During implementation, I began to understand bias, explainability, privacy and responsible deployment as practical design requirements.

A research planning agent may generate recommendations that appear authoritative even when they are based on simplified assumptions. This creates a risk that students may rely on its output without checking academic literature, university requirements or supervisor advice.

The system should therefore support academic judgement rather than replace it. The National Institute of Standards and Technology (2023) states that artificial intelligence risks should be considered throughout design, development, deployment and monitoring. This reinforced my understanding that responsibility must influence the architecture rather than appear only as a final compliance check.

## Now what?

In future projects, I will define the minimum viable product and evaluation criteria before implementation begins. I will distinguish essential requirements from desirable extensions and future development.

I will also introduce testing earlier. In addition to unit and functional tests, I will include output quality assessment, user testing and expert review. For a research planning system, evaluation should examine alignment, usefulness, source reliability and clarity of explanation.

For future group projects, I will encourage the team to document roles and decisions from the first meeting. A responsibility matrix, meeting notes and action tracker would reduce ambiguity. Each task should have a named owner, expected output and deadline.

Technically, I would like to develop my understanding of agent orchestration, academic retrieval, vector databases and human review controls. These capabilities would support a more advanced ResearchMate system with live academic retrieval, source comparison and clearer explanations.

I will also treat ethical requirements as part of system architecture. Future systems should include source verification, privacy controls, clear limitations, explainable recommendations and opportunities for human review.

Overall, the module strengthened my understanding of intelligent agents, modular Python development, testing, teamwork and responsible artificial intelligence. I now place greater value on realistic scope, transparent evaluation, documented collaboration and responsible design.

## References

National Institute of Standards and Technology (2023) *Artificial Intelligence Risk Management Framework, AI RMF 1.0*. Gaithersburg, MD: National Institute of Standards and Technology. doi: 10.6028/NIST.AI.100-1.

Rolfe, G., Freshwater, D. and Jasper, M. (2001) *Critical reflection in nursing and the helping professions: A user’s guide*. Basingstoke: Palgrave Macmillan.

Wooldridge, M. (2009) *An introduction to multiagent systems*. 2nd edn. Chichester: Wiley.

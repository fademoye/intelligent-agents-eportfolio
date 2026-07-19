# Week 7 System Design

## Design Context

The Week 7 design was developed as part of the ResearchMate group project. It proposed a multi-agent system for academic research planning and later informed the narrower individual prototype implemented in Week 11.

## Project Aim

The proposed system aimed to support postgraduate students in developing and aligning a research topic, aim, objectives, research questions and methodology.

## Problem Being Addressed

Students can find it difficult to maintain alignment between the different elements of a research proposal.

The proposed system was intended to guide users through this process and generate a structured research plan for further review.

## Proposed Users

The intended users were postgraduate students preparing:

- a dissertation;
- a research proposal;
- an academic project;
- an initial research plan.

## Proposed Architecture

The design used a multi-agent approach in which specialised agents would perform distinct tasks.

The proposed agents included:

- a planning agent;
- a retrieval agent;
- a processing agent;
- an analysis agent;
- an output-generation agent.

These agents were intended to coordinate in order to transform an initial research idea into a structured research plan.

## Proposed Workflow

1. The user enters a research topic or area of interest.
2. The planning agent identifies the main research-planning requirements.
3. The retrieval agent gathers relevant information.
4. The processing and analysis agents examine the information.
5. The output-generation agent produces a structured research plan.
6. The user reviews and refines the result.

## Tools and Technologies Considered

The design considered:

- Python;
- large language models;
- CrewAI;
- LangChain;
- vector databases;
- GitHub;
- modular software design.

These technologies were evaluated during the design stage. Not all were implemented in the final prototype.

## Design Rationale

A multi-agent architecture was considered appropriate because academic research planning contains several distinct tasks.

Separating these tasks into specialist agents could improve modularity, maintainability and clarity.

However, the approach also increased integration complexity. Each additional agent introduced communication, coordination and testing requirements, making the original design ambitious for the available timeframe.

## Risks and Limitations

The proposed system had several risks:

- inaccurate or fabricated AI outputs;
- biased recommendations;
- student overreliance;
- weak source quality;
- lack of transparency;
- data-privacy concerns;
- excessive project scope.

The most significant risks were inaccurate outputs, limited source verification and overreliance. These could cause users to accept plausible but unsuitable academic guidance without checking it against literature, university requirements or supervisor advice.

## Ethical and Professional Considerations

The system was intended to support students rather than replace academic judgement.

Users would still need to verify recommendations, consult academic literature and follow university and supervisor guidance.

A responsibly developed version would also require clearer explanations, source verification, privacy safeguards and human review.

## Week 7 Evidence

- [Week 7 design document](evidence/design/week-7-design-document.pdf)
- [ResearchMate architecture diagram](evidence/design/week-7-architecture.png)
- [Workflow diagram](evidence/design/week-7-workflow.png)
- [Relevant presentation material](evidence/design/week-7-slides.pdf)

![ResearchMate proposed architecture](evidence/design/week-7-architecture.png)

## Reflection on the Design Stage

At the design stage, I initially viewed the number of agents and features as evidence of technical strength.

As the project developed, I recognised that the architecture was broader than could be implemented and evaluated reliably within the module timeframe.

This changed my understanding of good design. An effective architecture must be technically coherent, proportionate to the problem and realistic to test.

In future, I would define the minimum viable system, evaluation criteria and technical dependencies before expanding the number of agents.

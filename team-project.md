# Team Project: ResearchMate

## Project Overview

ResearchMate was a collaborative group project focused on designing a hybrid multi agent system for academic research automation.

The proposed system was intended to help students and researchers manage selected stages of academic research by:

1. Receiving a research query.
2. Dividing the query into structured subtasks.
3. Retrieving relevant academic sources.
4. Processing and summarising information.
5. Ranking sources for relevance and credibility.
6. Removing duplicate results.
7. Producing structured outputs.

The project focused on the design of the proposed system rather than the development of a fully operational production system.

A multi agent approach was selected because academic research involves several different tasks requiring different capabilities. Dividing these responsibilities across specialist agents supported modularity, separation of concerns, maintainability and future development.

## Team Members

1. Frank Ademoye
2. Alixandria Ali
3. Mosleh Ali Nakib
4. Hamad Abdullah M KH Al Jabir

## My Role

My agreed role was Team Lead and Project Coordinator.

This role was formally recorded in the project kick off document and the team contract.

My responsibilities included:

1. Coordinating the team.
2. Organising meetings.
3. Managing timelines and deadlines.
4. Supporting the allocation of responsibilities.
5. Reviewing the assignment requirements.
6. Combining and refining the final report.
7. Proofreading the completed work.
8. Supporting final quality checks.
9. Managing the final submission.

## My Individual Contribution

My contribution to the ResearchMate group project included:

1. Participating in virtual meetings and design discussions.
2. Helping establish the project structure and delivery approach.
3. Reviewing the assignment brief and marking requirements.
4. Supporting the allocation of project roles and deliverables.
5. Contributing to discussions about the ResearchMate workflow.
6. Reviewing how the Planning, Retrieval, Processing, Ranking and Storage Agents would interact.
7. Helping distinguish the user journey from the technical agent workflow.
8. Consolidating material into the final report structure.
9. Reviewing the report for clarity, flow, criticality and word count.
10. Supporting the final review and submission process.

My leadership contribution focused on maintaining progress, coordinating shared work and helping the team align the final submission with the assessment requirements.

The final architecture and group proposal represented collaborative work. I do not claim sole ownership of the technical design or the work completed by other team members.

## System Architecture

ResearchMate was designed as a cooperative hierarchical multi agent system containing five main specialist agents:

1. Planning Agent
2. Retrieval Agent
3. Processing Agent
4. Ranking Agent
5. Storage Agent

The Planning Agent acted as the main coordinator.

It was intended to receive the user query, divide it into ordered tasks and direct the other agents.

The architecture combined deliberative and reactive approaches.

The Planning Agent used a deliberative approach informed by the Belief, Desire and Intention model.

In this design:

1. Beliefs represented the user query and available research context.
2. Desires represented the intended research outcome.
3. Intentions represented the tasks selected for execution.

The Retrieval and Processing Agents performed more reactive functions by responding to assigned tasks and available information.

The design also included ReAct style replanning. If the initial retrieval results were insufficient, the Planning Agent could revise the tasks and repeat part of the workflow.

## ResearchMate Architecture Diagram

The following diagram shows the proposed ResearchMate hybrid multi agent architecture.

![ResearchMate hybrid multi agent architecture](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)

[Open the ResearchMate architecture diagram](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)

## Proposed Agent Responsibilities

### Planning Agent

The Planning Agent was intended to:

1. Receive the user query.
2. Interpret the research request.
3. Divide the request into ordered subtasks.
4. Coordinate the subordinate agents.
5. Review whether the retrieved information was sufficient.
6. Trigger replanning where necessary.

### Retrieval Agent

The Retrieval Agent was intended to:

1. Search academic services.
2. Query arXiv, Semantic Scholar and OpenAlex.
3. Return relevant papers and metadata.
4. Continue operating if one source became unavailable.

### Processing Agent

The Processing Agent was intended to:

1. Process retrieved content.
2. Divide content into manageable sections.
3. Summarise relevant information.
4. Prepare the results for ranking.

### Ranking Agent

The Ranking Agent was intended to:

1. Score relevance.
2. Assess source credibility.
3. Identify duplicate results.
4. Prioritise stronger academic sources.

### Storage Agent

The Storage Agent was intended to:

1. Save the final results.
2. Prepare structured output.
3. Support CSV, JSON, Markdown and PDF formats.

## Proposed Workflow

The proposed ResearchMate workflow was:

1. The user submits a research query.
2. The Planning Agent interprets and divides the query.
3. The Retrieval Agent searches academic services in parallel.
4. The Planning Agent reviews the retrieval results.
5. If the results are insufficient, the tasks are revised.
6. The Processing Agent summarises the relevant material.
7. The Ranking Agent assesses relevance, credibility and duplication.
8. The Storage Agent saves and formats the final output.
9. The results are returned to the user for review.

## Tools and Technologies Evaluated

The group evaluated a range of tools and technologies.

The proposed design included:

1. Python
2. Llama 3.3 70B through Groq
3. LangGraph StateGraph
4. arXiv
5. Semantic Scholar
6. OpenAlex
7. ChromaDB
8. BAAI bge small embeddings
9. PyMuPDF
10. RecursiveCharacterTextSplitter
11. SQLite
12. Pydantic
13. Chainlit
14. asyncio
15. pytest
16. pytest asyncio
17. GitHub

CrewAI was considered but not selected for the proposed final design.

The system required a stateful replanning cycle rather than mainly role based task delegation.

LangGraph was considered more suitable because it could represent the workflow through explicit nodes, transitions and repeated planning activity.

Not all of these technologies were implemented during the group stage. Some were proposed for the design and future development.

## Design Rationale

A single agent structure was considered less suitable because one agent would have needed to perform planning, retrieval, processing, ranking, deduplication, storage and output generation.

Separating these responsibilities across specialist agents supported:

1. Modularity.
2. Maintainability.
3. Testability.
4. Separation of concerns.
5. Clearer responsibilities.
6. Future extensibility.

However, the multi agent design also created additional complexity.

Each agent required:

1. Defined inputs and outputs.
2. Structured communication.
3. Error handling.
4. Testing.
5. Orchestration.
6. Clear responsibility boundaries.

This made the proposed architecture technically strong but ambitious for the available assessment timeframe.

## Development Approach

The group proposed an Agile and iterative development approach.

Each agent would be developed and reviewed separately before integration.

The proposed sequence was:

1. Define the problem and requirements.
2. Agree the agent responsibilities.
3. Design the overall architecture.
4. Develop the Planning Agent.
5. Develop the Retrieval Agent.
6. Develop the Processing Agent.
7. Develop the Ranking Agent.
8. Develop the Storage Agent.
9. Integrate the agents using LangGraph.
10. Test the complete workflow.
11. Evaluate performance, limitations and risks.

## Technical Risks and Mitigation

### LLM Hallucinations

The system could produce confident statements that were not supported by academic evidence.

The proposed mitigation was to restrict processing to information returned from trusted academic services and use the Ranking Agent to reduce the prominence of weak sources.

### Context Limitations

Large collections of full text academic material could exceed practical model limits and reduce output quality.

The initial design therefore focused on abstracts and smaller relevant passages.

### Agent Coordination

Five interacting agents increased the risk of message mismatches, communication failures and difficult debugging.

Pydantic was proposed to enforce structured contracts between agents.

LangGraph would also make the workflow and replanning cycle explicit.

### External Services

The system depended on academic APIs and an external language model service.

These services could fail, become unavailable or impose usage limits.

The proposed mitigation included:

1. Parallel retrieval.
2. Exception handling.
3. Continuation where one source failed.
4. Limits on concurrent calls.
5. System logging.

### Source Credibility

Not every retrieved source would have equal academic value.

The Ranking Agent was intended to assess relevance, citation information and duplication before results were returned.

## Ethical and Professional Considerations

ResearchMate was intended to support academic research rather than replace independent judgement.

Users would still need to:

1. Verify sources.
2. Assess relevance.
3. Consult academic literature.
4. Follow university requirements.
5. Obtain supervisor feedback.

A responsibly developed version would require:

1. Source verification.
2. Clear explanations.
3. Privacy controls.
4. Appropriate handling of user data.
5. Human review.
6. Warnings about limitations.
7. Monitoring of unsuitable outputs.
8. Protection against student overreliance.

## Teamwork and Collaboration

The project required virtual communication, shared decision making and clear allocation of responsibilities.

The team discussed:

1. The project problem.
2. The intended users.
3. The agent architecture.
4. Agent responsibilities.
5. Technology choices.
6. Risks and mitigation.
7. Report structure.
8. Meeting schedules.
9. Individual responsibilities.
10. Final review and submission.

The group used virtual meetings, the University discussion forum and shared documents to coordinate the work.

## Evidence of My Leadership and Individual Contribution

My role as Team Lead and Project Coordinator was formally documented in the kick off meeting document and the team contract.

These documents provide evidence that I was responsible for coordinating meetings, managing timelines, combining the report, proofreading and supporting submission management.

### Kick Off Meeting Document

The kick off document established:

1. The ResearchMate project concept.
2. The proposed multi agent structure.
3. The group roles.
4. The proposed meeting schedule.
5. The expected deliverables.
6. The final submission goals.

It identified me as Team Lead and Project Coordinator.

[View the Group A Kick Off Meeting document](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/GROUP%20A%20%E2%80%93%20KICK%20OFF%20MEETING%20DISCUSSION%20v1.3%20.docx.pdf)

### Team Contract

The team contract recorded:

1. The group goals.
2. Attendance and communication expectations.
3. Collaborative decision making.
4. Meeting arrangements.
5. Agreed roles.
6. Responsibilities.
7. Procedures for managing difficulties.

It confirmed my responsibility for coordinating meetings, managing timelines, combining the report, proofreading and managing the submission process.

[View the Group A Team Contract](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/Team%20Contract%20Template%20-%20Group%20A%20.docx%20%281%29.pdf)

## Challenges

### Managing Scope

The proposed architecture was ambitious.

It involved several agents, external services, orchestration, storage, testing and an interface.

This created tension between technical ambition and realistic delivery.

I learned that scope should be defined early and separated into essential requirements, desirable additions and future development.

### Coordinating Virtual Work

Differences in availability sometimes affected meetings and progress.

This showed me the importance of documenting decisions, responsibilities and deadlines.

It also demonstrated the value of shared documents and regular written updates.

### Maintaining Clear Ownership

Because several team members contributed to the same proposal, it was important to distinguish individual responsibility from shared group work.

The kick off document and team contract helped clarify responsibilities.

However, I recognised that task ownership should also be reviewed throughout the project rather than agreed only at the beginning.

### Distinguishing Design from Implementation

The group proposal included technologies and capabilities that were not fully implemented.

It was important to describe these accurately as proposed features rather than completed functionality.

This distinction supported honest and professional reporting.

## What I Learned

The project strengthened my understanding of multi agent system design.

I learned that separate software components do not automatically form a genuine multi agent system.

Each agent needs:

1. A clear responsibility.
2. Defined inputs and outputs.
3. A reason for operating separately.
4. A communication mechanism.
5. A coordination process.
6. Appropriate error handling.

The project also improved my understanding of leadership in a virtual environment.

Leadership involved:

1. Establishing structure.
2. Supporting communication.
3. Clarifying responsibilities.
4. Maintaining progress.
5. Reviewing quality.
6. Helping the team meet the submission requirements.

I also recognised that leadership does not mean completing every task personally.

It requires effective delegation, support and shared accountability.

In future group projects, I would introduce a responsibility matrix at the beginning.

Each activity would have:

1. A named owner.
2. A required output.
3. A deadline.
4. A review point.
5. A recorded status.

## Evaluation of My Leadership

The kick off document and team contract show that I held a formal coordination role.

My contribution involved helping the team establish the project structure, organise responsibilities, maintain communication and prepare the final report.

The experience developed my organisation, communication and project coordination skills.

It also highlighted areas for improvement.

I could have introduced clearer task tracking earlier and delegated integration activities more systematically.

In future projects, I would review task ownership during every meeting and identify risks to delivery before they became urgent.

## Distinction Between Group and Individual Work

ResearchMate was developed as a collaborative group concept and design proposal.

The group work included:

1. The problem definition.
2. The proposed architecture.
3. Agent responsibilities.
4. Technology evaluation.
5. Risk analysis.
6. Development planning.
7. System diagrams.
8. The final group report.

The Week 11 implementation presented elsewhere in this portfolio was my individual prototype.

The group project informed my understanding of the research problem, architecture and workflow.

However, the individual source code, testing and implementation evidence were completed separately.

## Connection to Learning Outcomes

### Learning Outcome 1

The project supported my ability to identify and critically analyse agent architectures.

I considered single agent, multi agent, reactive, deliberative and hybrid approaches.

Supporting evidence:

1. [Week 7 System Design](week-7-design.html)
2. [ResearchMate Architecture Diagram](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)
3. [Critical Project Evaluation](project-evaluation.html)

### Learning Outcome 2

The project applied intelligent agent techniques to academic research automation.

The design also considered uncertainty involving source quality, hallucinations, external service failure and agent coordination.

Supporting evidence:

1. [Week 7 System Design](week-7-design.html)
2. [Week 11 Final Implementation](week-11-implementation.html)
3. [Critical Project Evaluation](project-evaluation.html)

### Learning Outcome 3

The project required the evaluation of software tools and consideration of legal, ethical, professional and technical risks.

Supporting evidence:

1. [Week 7 System Design](week-7-design.html)
2. [Reflective Case Studies](reflective-case-studies.html)
3. [Critical Project Evaluation](project-evaluation.html)

### Learning Outcome 4

The project developed my skills in virtual teamwork, communication, leadership, shared decision making and project organisation.

Supporting evidence:

1. [Group A Kick Off Meeting Document](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/GROUP%20A%20%E2%80%93%20KICK%20OFF%20MEETING%20DISCUSSION%20v1.3%20.docx.pdf)
2. [Group A Team Contract](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/Team%20Contract%20Template%20-%20Group%20A%20.docx%20%281%29.pdf)
3. [Team Meeting Notes](team-meetings.html)
4. [Final Reflection](final-reflection.html)

## Supporting Evidence

1. [Group A Kick Off Meeting Document](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/GROUP%20A%20%E2%80%93%20KICK%20OFF%20MEETING%20DISCUSSION%20v1.3%20.docx.pdf)
2. [Group A Team Contract](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/Team%20Contract%20Template%20-%20Group%20A%20.docx%20%281%29.pdf)
3. [ResearchMate Architecture Diagram](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)
4. [Week 7 System Design](week-7-design.html)
5. [Week 11 Final Implementation](week-11-implementation.html)
6. [Team Meeting Notes](team-meetings.html)
7. [Critical Project Evaluation](project-evaluation.html)
8. [Final Reflection](final-reflection.html)

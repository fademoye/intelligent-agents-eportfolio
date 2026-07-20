# Team Project: ResearchMate

## Project Overview

ResearchMate was a collaborative design project focused on developing a hybrid multi-agent system for academic research automation.

The proposed system was designed to support users by:

- receiving an academic research query;
- decomposing the query into structured subtasks;
- retrieving relevant academic sources;
- processing and summarising retrieved information;
- ranking sources for relevance and credibility;
- removing duplicate results;
- presenting the final output in a structured format.

A multi-agent approach was selected because academic research involves different types of tasks that require different capabilities. Dividing the workflow across specialised agents supported modularity, clearer separation of responsibilities, improved testability and easier future development.

## Team Members

- Frank Ademoye
- Alix
- Mosleh
- Hamad

## My Individual Contribution

My contribution to the ResearchMate group project included:

- participating in virtual team meetings and design discussions;
- researching intelligent-agent and multi-agent approaches;
- contributing to discussions about the overall ResearchMate workflow;
- reviewing how planning, retrieval, processing, ranking and output functions could interact;
- helping distinguish the user-facing research journey from the underlying technical agent workflow;
- contributing to project documentation;
- reviewing and supporting preparation of presentation material;
- participating in peer-review activity;
- contributing to discussions about project scope, responsibilities and delivery.

My main focus was understanding how the proposed system should move from an initial user query through planning, retrieval, processing and final output.

I also contributed to discussions about how the broader group concept could be presented clearly and how the system should support, rather than replace, academic judgement.

The project was collaborative, so the final architecture and design proposal represented shared group work rather than the work of one individual.

## System Architecture

ResearchMate was designed as a cooperative hierarchical multi-agent system containing five specialised agents:

- Planning Agent;
- Retrieval Agent;
- Processing Agent;
- Ranking Agent;
- Storage Agent.

The Planning Agent acted as the main coordinator. It received the user’s research query, decomposed it into ordered subtasks and directed the subordinate agents.

The architecture combined deliberative and reactive approaches.

The Planning Agent used a deliberative approach informed by the Belief–Desire–Intention model:

- beliefs represented the user query and retrieved context;
- desires represented the intended research outcome;
- intentions represented the specific subtasks assigned to the other agents.

The Retrieval and Processing Agents performed more reactive functions by responding to assigned tasks and available information.

The proposed workflow also used ReAct-style replanning. If the first retrieval attempt produced insufficient results, the Planning Agent could revise the research tasks and repeat part of the workflow.

A single-agent architecture was rejected because the system needed to perform different kinds of work, including planning, source retrieval, summarisation, ranking, deduplication and output generation.

Dividing these responsibilities across specialised agents supported:

- modularity;
- maintainability;
- testability;
- separation of concerns;
- clearer system coordination;
- future extensibility.

## ResearchMate Architecture and Design Evidence

The diagram below shows the proposed ResearchMate hybrid multi-agent architecture developed during the group project.

The Planning Agent coordinates the other agents, while LangGraph was proposed to manage the stateful workflow. The Retrieval Agent connects to academic sources, the Processing Agent filters and summarises results, the Ranking Agent evaluates relevance and credibility, and the Storage Agent produces the final output.

![ResearchMate hybrid multi-agent architecture](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)

[Open the ResearchMate architecture diagram](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)

## Proposed Agent Responsibilities

### Planning Agent

The Planning Agent was responsible for:

- receiving the user query;
- interpreting the research request;
- decomposing the request into subtasks;
- coordinating the other agents;
- reviewing whether retrieval results were sufficient;
- triggering replanning where necessary.

### Retrieval Agent

The Retrieval Agent was responsible for:

- searching academic sources;
- querying multiple academic services;
- returning relevant papers and metadata;
- handling partial failure where one source became unavailable.

### Processing Agent

The Processing Agent was responsible for:

- processing retrieved content;
- dividing text into manageable sections;
- summarising relevant information;
- preparing information for ranking and presentation.

### Ranking Agent

The Ranking Agent was responsible for:

- scoring relevance;
- assessing source credibility;
- identifying duplicate results;
- prioritising stronger sources.

### Storage Agent

The Storage Agent was responsible for:

- saving the final research results;
- preparing structured output;
- supporting formats such as CSV, JSON, Markdown and PDF.

## Tools and Technologies Evaluated

The group evaluated several technologies for the proposed ResearchMate system.

The final design proposed:

- Python for implementation;
- Llama-3.3-70B through Groq for planning and processing;
- LangGraph for stateful orchestration;
- arXiv for computer science and machine-learning preprints;
- Semantic Scholar for citation and credibility information;
- OpenAlex for broader interdisciplinary coverage;
- ChromaDB for local vector storage;
- BAAI/bge-small embeddings;
- PyMuPDF for PDF processing;
- RecursiveCharacterTextSplitter for text chunking;
- SQLite for persistence;
- Pydantic for data validation;
- Chainlit for the user interface;
- asyncio for concurrent execution;
- pytest and pytest-asyncio for testing;
- GitHub for version control.

CrewAI was considered but not selected for the proposed final design because the system required a stateful ReAct replanning cycle rather than mainly role-based task delegation.

LangGraph was considered more appropriate because it could represent the workflow as a stateful graph with defined nodes, transitions and repeated planning activity.

Not all technologies were implemented during the group stage. Some formed part of the proposed architecture and future development plan.

## Retrieval and Processing Design

The design proposed that the Retrieval Agent query three academic services in parallel:

- arXiv;
- Semantic Scholar;
- OpenAlex.

Parallel retrieval was intended to reduce waiting time and improve source coverage.

Each service provided a different benefit:

- arXiv offered access to machine-learning and computer-science preprints;
- Semantic Scholar provided citation data that could support credibility scoring;
- OpenAlex broadened interdisciplinary coverage.

The proposed Processing Agent would summarise retrieved material and prepare it for ranking.

ChromaDB was proposed as a lightweight local vector store, while RecursiveCharacterTextSplitter was selected to preserve meaningful text boundaries more effectively than basic fixed-size splitting.

## Development Approach

The group proposed an Agile and iterative development approach.

Each specialist agent would be developed and tested separately before being connected to the wider workflow.

The intended development practices included:

- modular agent development;
- incremental integration;
- automated testing;
- GitHub version control;
- logging and observability;
- regular review of agent interaction.

The proposed sequence was:

1. define the system requirements;
2. design the agent responsibilities;
3. develop the Planning Agent;
4. develop the Retrieval Agent;
5. develop the Processing Agent;
6. develop the Ranking Agent;
7. develop the Storage Agent;
8. integrate the agents through LangGraph;
9. test the end-to-end workflow;
10. review system quality and limitations.

## Technical Risks and Mitigation

### LLM Hallucinations

A major risk was that the language model could generate confident statements that were not supported by academic evidence.

The proposed mitigation was to restrict processing to information retrieved from trusted academic services.

The Ranking Agent would also reduce the prominence of weak results through credibility and relevance scoring.

### Context-Window Limitations

A large collection of full-text papers could exceed the model’s practical context limits and reduce output quality.

The proposed system therefore focused initially on abstracts and smaller relevant sections.

A future full-text version would use vector retrieval to return only the most relevant passages.

### Agent-Coordination Complexity

Five interacting agents could create type mismatches, unclear message formats and failures that were difficult to trace.

Pydantic was proposed to enforce structured contracts between agents.

LangGraph would also make the agent sequence and replanning loop explicit.

### Latency and External Dependencies

The system depended on external academic APIs and an external language-model service.

Any of these services could fail, become unavailable or impose rate limits.

The proposed mitigation included:

- parallel retrieval;
- exception handling for individual services;
- limits on concurrent calls;
- continuation where one source failed;
- logging to support diagnosis.

### Source Credibility

Not every retrieved source would have equal academic value.

The Ranking Agent was therefore designed to consider relevance, citation information and duplication before the results were returned.

## Teamwork and Collaboration

The project required virtual collaboration, communication, shared decision-making and allocation of responsibilities.

The team discussed:

- the academic research problem;
- intended users;
- system scope;
- agent architecture;
- agent responsibilities;
- technology choices;
- risk and mitigation;
- presentation structure;
- division of work;
- assessment deadlines.

The team needed to balance technical ambition with the available time.

The initial concept was broad and involved multiple agents, external APIs, orchestration, vector storage and an interactive interface.

This created a risk that the design could become too large for the assessment timeframe.

The group therefore needed to distinguish between:

- the full proposed system;
- the design evidence required for the assessment;
- the narrower individual implementation completed later.

## Challenges

### Managing Scope

The original ResearchMate concept was ambitious.

It included multiple specialist agents, academic retrieval, credibility ranking, vector storage, iterative replanning and several output formats.

This created a tension between designing a strong multi-agent system and producing a realistic solution within the available time.

I learned that scope should be agreed early and divided into essential, desirable and future functions.

### Coordinating Virtual Work

Virtual collaboration made it more difficult to maintain visibility of progress.

Where decisions, actions or owners were not recorded clearly, it became harder to understand who was responsible for the next task.

This showed me the value of:

- written meeting notes;
- clear task ownership;
- agreed deadlines;
- regular progress reviews;
- shared document control.

### Distinguishing Design from Implementation

Another challenge was ensuring that proposed technologies were not described as though they had already been implemented.

The group design included LangGraph, ChromaDB, Chainlit, multiple academic APIs and several specialist agents.

However, the later individual implementation used a more focused modular Python prototype.

This distinction was important for accurate and ethical reporting.

### Balancing Technical and User Perspectives

The team also needed to distinguish between the user journey and the technical workflow.

The user needed a clear and simple research-support experience, while the proposed technical system involved several internal agents and services.

This helped me understand that a technically complex system should still present a simple, understandable and controlled experience to the user.

## What I Learned

The project strengthened my understanding of multi-agent design.

I learned that a multi-agent system is not simply a collection of Python files. Each agent needs:

- a defined responsibility;
- clear inputs and outputs;
- structured communication;
- a coordination mechanism;
- appropriate error handling;
- a reason for existing as a separate component.

I also learned the difference between reactive, deliberative and hybrid approaches.

The ResearchMate design showed how a deliberative Planning Agent could coordinate more reactive specialist agents.

The project improved my understanding of technical decision-making.

Rather than listing technologies, the group needed to consider why one tool was more suitable than another.

For example, LangGraph was selected because of the need for stateful control and replanning, while CrewAI was considered less suitable for that specific requirement.

The project also improved my awareness of responsible AI design.

A system that supports academic work must consider:

- hallucinations;
- source quality;
- transparency;
- user overreliance;
- privacy;
- data handling;
- academic integrity;
- human review.

I also learned that effective virtual teamwork requires more than attending meetings.

It requires:

- clear role allocation;
- documented actions;
- visible progress;
- shared ownership;
- regular communication;
- honest separation of individual and group work.

In future projects, I would establish a responsibility matrix during the first meeting, assign named owners to each task and review progress against written actions at every meeting.

## Distinction Between Group and Individual Work

ResearchMate was developed as a collaborative group concept and design proposal.

The group work covered:

- the problem definition;
- the proposed multi-agent architecture;
- agent responsibilities;
- technology evaluation;
- risk analysis;
- development planning;
- graphical system design.

The Week 11 implementation presented elsewhere in this portfolio was my individual prototype.

The group project informed my understanding of:

- the problem;
- the broader architecture;
- the research workflow;
- the relationship between planning, processing and output.

The individual coding, testing, implementation screenshots and repository evidence were completed separately.

This distinction is important because the group design was broader than the final individual prototype.

## Connection to Learning Outcomes

### Learning Outcome 1

The project supported my ability to identify and critically analyse agent-based architectures.

I compared single-agent and multi-agent approaches and considered reactive, deliberative and hybrid designs.

The group selected a hybrid multi-agent architecture because the Planning Agent required deliberative reasoning, while Retrieval and Processing functions could operate more reactively.

Supporting evidence:

- [Week 7 System Design](week-7-design.html)
- [ResearchMate Architecture Diagram](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)
- [Critical Project Evaluation](project-evaluation.html)

### Learning Outcome 2

The project applied intelligent-agent techniques to the real-world problem of academic research automation.

The design considered technical uncertainty relating to source quality, hallucinations, API failure, context limits and coordination between agents.

Supporting evidence:

- [ResearchMate Architecture Diagram](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)
- [Week 11 Individual Implementation](week-11-implementation.html)
- [Critical Project Evaluation](project-evaluation.html)

### Learning Outcome 3

The project required critical evaluation of software tools including Python, LangGraph, Llama, academic APIs, ChromaDB, Pydantic, Chainlit and pytest.

The design also considered responsible deployment, academic reliability, transparency, data privacy and human review.

Supporting evidence:

- [Week 7 System Design](week-7-design.html)
- [Reflective Case Studies](reflective-case-studies.html)
- [Critical Project Evaluation](project-evaluation.html)

### Learning Outcome 4

The project developed my skills in virtual teamwork, communication, shared decision-making, documentation and project organisation.

It also helped me understand the importance of clear ownership and evidence of individual contribution within collaborative work.

Supporting evidence:

- [Team Meeting Notes](team-meetings.html)
- [Final Reflection](final-reflection.html)

## Evidence

- [ResearchMate Architecture Diagram](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)
- [Week 7 System Design](week-7-design.html)
- [Week 11 Individual Implementation](week-11-implementation.html)
- [Team Meeting Notes](team-meetings.html)
- [Critical Project Evaluation](project-evaluation.html)
- [Final Reflection](final-reflection.html)

Additional group communication, peer-review and shared planning evidence should only be added here when the relevant files have been uploaded and linked.

### Coordinating Virtual Work

Virtual collaboration made it more difficult to maintain visibility of progress.

Where decisions, actions or owners were not recorded clearly, it became harder to understand who was responsible for the next task.

This showed me the value of:

- written meeting notes;
- clear task ownership;
- agreed deadlines;
- regular progress reviews;
- shared document control.

### Distinguishing Design from Implementation

Another challenge was ensuring that proposed technologies were not described as though they had already been implemented.

The group design included LangGraph, ChromaDB, Chainlit, multiple academic APIs and several specialist agents.

However, the later individual implementation used a more focused modular Python prototype.

This distinction was important for accurate and ethical reporting.

### Balancing Technical and User Perspectives

The team also needed to distinguish between the user journey and the technical workflow.

The user needed a clear and simple research-support experience, while the proposed technical system involved several internal agents and services.

This helped me understand that a technically complex system should still present a simple, understandable and controlled experience to the user.

## What I Learned

The project strengthened my understanding of multi-agent design.

I learned that a multi-agent system is not simply a collection of Python files. Each agent needs:

- a defined responsibility;
- clear inputs and outputs;
- structured communication;
- a coordination mechanism;
- appropriate error handling;
- a reason for existing as a separate component.

I also learned the difference between reactive, deliberative and hybrid approaches.

The ResearchMate design showed how a deliberative Planning Agent could coordinate more reactive specialist agents.

The project improved my understanding of technical decision-making.

Rather than listing technologies, the group needed to consider why one tool was more suitable than another.

For example, LangGraph was selected because of the need for stateful control and replanning, while CrewAI was considered less suitable for that specific requirement.

The project also improved my awareness of responsible AI design.

A system that supports academic work must consider:

- hallucinations;
- source quality;
- transparency;
- user overreliance;
- privacy;
- data handling;
- academic integrity;
- human review.

I also learned that effective virtual teamwork requires more than attending meetings.

It requires:

- clear role allocation;
- documented actions;
- visible progress;
- shared ownership;
- regular communication;
- honest separation of individual and group work.

In future projects, I would establish a responsibility matrix during the first meeting, assign named owners to each task and review progress against written actions at every meeting.

## Distinction Between Group and Individual Work

ResearchMate was developed as a collaborative group concept and design proposal.

The group work covered:

- the problem definition;
- the proposed multi-agent architecture;
- agent responsibilities;
- technology evaluation;
- risk analysis;
- development planning;
- graphical system design.

The Week 11 implementation presented elsewhere in this portfolio was my individual prototype.

The group project informed my understanding of:

- the problem;
- the broader architecture;
- the research workflow;
- the relationship between planning, processing and output.

The individual coding, testing, implementation screenshots and repository evidence were completed separately.

This distinction is important because the group design was broader than the final individual prototype.

## Connection to Learning Outcomes

### Learning Outcome 1

The project supported my ability to identify and critically analyse agent-based architectures.

I compared single-agent and multi-agent approaches and considered reactive, deliberative and hybrid designs.

The group selected a hybrid multi-agent architecture because the Planning Agent required deliberative reasoning, while Retrieval and Processing functions could operate more reactively.

Supporting evidence:

- [Week 7 System Design](week-7-design.html)
- [ResearchMate Architecture Diagram](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)
- [Critical Project Evaluation](project-evaluation.html)

### Learning Outcome 2

The project applied intelligent-agent techniques to the real-world problem of academic research automation.

The design considered technical uncertainty relating to source quality, hallucinations, API failure, context limits and coordination between agents.

Supporting evidence:

- [ResearchMate Architecture Diagram](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)
- [Week 11 Individual Implementation](week-11-implementation.html)
- [Critical Project Evaluation](project-evaluation.html)

### Learning Outcome 3

The project required critical evaluation of software tools including Python, LangGraph, Llama, academic APIs, ChromaDB, Pydantic, Chainlit and pytest.

The design also considered responsible deployment, academic reliability, transparency, data privacy and human review.

Supporting evidence:

- [Week 7 System Design](week-7-design.html)
- [Reflective Case Studies](reflective-case-studies.html)
- [Critical Project Evaluation](project-evaluation.html)

### Learning Outcome 4

The project developed my skills in virtual teamwork, communication, shared decision-making, documentation and project organisation.

It also helped me understand the importance of clear ownership and evidence of individual contribution within collaborative work.

Supporting evidence:

- [Team Meeting Notes](team-meetings.html)
- [Final Reflection](final-reflection.html)

## Evidence

### ResearchMate Architecture PNG

![ResearchMate architecture evidence](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)

[Open the ResearchMate architecture PNG](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)

### Week 11 System Running PNG

![Week 11 system running](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/screenshot%20of%20the%20system%20running%3B.png)

[Open the system-running PNG](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/screenshot%20of%20the%20system%20running%3B.png)

### Week 11 User Input PNG

![Week 11 user input](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/screenshot%20of%20user%20input%3B.png)

[Open the user-input PNG](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/screenshot%20of%20user%20input%3B.png)

### Week 11 Generated Output PNG

![Week 11 generated output](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/screenshot%20of%20generated%20output%3B.png)

[Open the generated-output PNG](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/screenshot%20of%20generated%20output%3B.png)

### Week 11 Project Structure PNG

![Week 11 project structure](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/project-structure.png)

[Open the project-structure PNG](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/project-structure.png)

### Week 11 Testing PNG

![Eight successful pytest results](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/tests_passed_8.png)

[Open the testing PNG](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/implementation/tests_passed_8.png)

### Additional Portfolio Evidence

- [Week 7 System Design](week-7-design.html)
- [Week 11 Individual Implementation](week-11-implementation.html)
- [Team Meeting Notes](team-meetings.html)
- [Critical Project Evaluation](project-evaluation.html)
- [Final Reflection](final-reflection.html)

# Week 7 System Design

## Design Context

The Week 7 design was developed as part of the ResearchMate group project.

It proposed a hybrid multi-agent system for academic research automation. The wider group design later informed the narrower individual prototype implemented in Week 11.

## Project Aim

ResearchMate was designed to automate selected stages of the academic research process.

The proposed system aimed to:

- receive an academic research query;
- decompose the query into structured subtasks;
- retrieve relevant academic sources;
- process and summarise retrieved information;
- rank sources for relevance and credibility;
- remove duplicate results;
- produce structured research outputs.

The system was intended to support academic research rather than replace independent analysis, academic judgement or supervisor guidance.

## Problem Being Addressed

The growing volume of academic literature can make identifying relevant and credible sources difficult and time-consuming.

ResearchMate was intended to reduce this burden by coordinating specialised agents across planning, retrieval, processing, ranking and output generation.

## Proposed Users

The intended users included:

- postgraduate students;
- dissertation students;
- researchers carrying out an initial literature search;
- users preparing an academic project or research proposal.

## Proposed Architecture

ResearchMate was designed as a cooperative hierarchical multi-agent system containing five specialised agents:

- Planning Agent;
- Retrieval Agent;
- Processing Agent;
- Ranking Agent;
- Storage Agent.

The Planning Agent acted as the main coordinator and directed the subordinate agents.

The architecture combined deliberative and reactive approaches.

The Planning Agent followed a deliberative approach informed by the Belief–Desire–Intention model, while the Retrieval and Processing Agents performed more reactive functions.

The proposed system also used ReAct-style replanning. Where the initial retrieval results were insufficient, the Planning Agent could revise the subtasks and repeat part of the workflow.

## ResearchMate Architecture

The diagram below shows the proposed hybrid multi-agent architecture developed during the group project.

![ResearchMate hybrid multi-agent architecture](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)

[Open the ResearchMate architecture diagram](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)

## Proposed Agent Responsibilities

### Planning Agent

The Planning Agent would:

- receive the user query;
- interpret the research request;
- divide the request into ordered subtasks;
- coordinate the subordinate agents;
- assess whether the retrieved results were sufficient;
- trigger replanning where necessary.

### Retrieval Agent

The Retrieval Agent would:

- search academic sources;
- query arXiv, Semantic Scholar and OpenAlex;
- retrieve papers and associated metadata;
- continue operating where one retrieval service failed.

### Processing Agent

The Processing Agent would:

- process retrieved content;
- divide content into manageable sections;
- summarise relevant material;
- prepare information for ranking.

### Ranking Agent

The Ranking Agent would:

- score source relevance;
- assess source credibility;
- identify duplicate results;
- prioritise stronger academic sources.

### Storage Agent

The Storage Agent would:

- save the processed results;
- prepare structured output;
- support formats such as CSV, JSON, Markdown and PDF.

## Proposed Workflow

1. The user submits an academic research query.
2. The Planning Agent interprets and decomposes the query.
3. The Retrieval Agent searches arXiv, Semantic Scholar and OpenAlex in parallel.
4. If the results are insufficient, the Planning Agent revises the subtasks.
5. The Processing Agent summarises and prepares the retrieved material.
6. The Ranking Agent assesses relevance, credibility and duplication.
7. The Storage Agent saves and formats the final results.
8. The completed output is returned to the user for review.

## Tools and Technologies Evaluated

The proposed design included:

- Python;
- Llama-3.3-70B through Groq;
- LangGraph StateGraph;
- arXiv;
- Semantic Scholar;
- OpenAlex;
- ChromaDB;
- BAAI/bge-small embeddings;
- PyMuPDF;
- RecursiveCharacterTextSplitter;
- SQLite;
- Pydantic;
- Chainlit;
- asyncio;
- pytest and pytest-asyncio;
- GitHub.

CrewAI was considered but was not selected for the proposed final design because ResearchMate required a stateful ReAct replanning cycle rather than mainly role-based task delegation.

LangGraph was selected because it was considered more suitable for representing a stateful workflow containing defined nodes, transitions and repeated planning activity.

Not all of these technologies were implemented during the group stage. Some formed part of the proposed architecture and future development plan.

## Design Rationale

A multi-agent architecture was considered appropriate because academic research automation includes several different tasks requiring different capabilities.

A single-agent design was rejected because one component would have needed to manage:

- planning;
- retrieval;
- summarisation;
- credibility ranking;
- deduplication;
- storage;
- output generation.

Separating these tasks across specialist agents supported:

- modularity;
- maintainability;
- testability;
- separation of concerns;
- clearer system coordination;
- future extensibility.

However, the approach also increased integration complexity.

Each additional agent required:

- clearly defined inputs and outputs;
- structured communication;
- error handling;
- testing;
- orchestration.

This made the original design ambitious for the available timeframe.

## Risks and Limitations

### LLM Hallucinations

The system could produce confident but unsupported statements.

The proposed mitigation was to restrict processing to retrieved academic material and use credibility scoring before presenting results.

### Context-Window Limitations

Large volumes of full-text academic content could exceed practical context limits and reduce model performance.

The initial design therefore focused on abstracts and smaller relevant passages.

### Agent-Coordination Complexity

Five interacting agents introduced the risk of message mismatches and failures between components.

Pydantic was proposed to enforce structured communication, while LangGraph would make the workflow and replanning cycle explicit.

### API Dependency and Latency

The system depended on external academic APIs and an external language-model service.

The proposed mitigations included:

- parallel retrieval;
- exception handling;
- concurrency controls;
- continuation where one source failed;
- system logging.

### Source Credibility

Not every retrieved source would have equal academic value.

The Ranking Agent was intended to assess relevance, citation information and duplication before the results were returned.

### Excessive Scope

The proposed design involved multiple agents, external APIs, orchestration, vector storage, testing and an interactive interface.

This created a risk that the full system would be too broad to implement and evaluate completely within the available timeframe.

## Ethical and Professional Considerations

ResearchMate was intended to support academic work rather than replace independent judgement.

Users would still need to:

- verify sources;
- assess the relevance of retrieved material;
- consult academic literature;
- follow university requirements;
- obtain supervisor feedback.

A responsibly developed version would require:

- clear explanations;
- source verification;
- privacy safeguards;
- human review;
- warnings about limitations;
- appropriate handling of user data;
- protection against student overreliance.

## Week 7 Evidence

- [ResearchMate Architecture Diagram](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)
- [ResearchMate Team Project](team-project.html)
- [Week 11 Final Implementation](week-11-implementation.html)
- [Critical Project Evaluation](project-evaluation.html)
- [Module Learning Outcomes](learning-outcomes.html)

## Reflection on the Design Stage

At the design stage, I initially viewed the number of agents and features as evidence of technical strength.

As the project developed, I recognised that the proposed architecture was broader than could be implemented and evaluated reliably within the available module timeframe.

This changed my understanding of effective system design.

A strong architecture must not only be technically ambitious. It must also be:

- coherent;
- proportionate to the problem;
- realistic to implement;
- possible to test;
- transparent about its limitations.

I also learned that design documentation must distinguish clearly between proposed and implemented functionality.

The Week 7 design included LangGraph, multiple academic APIs, ChromaDB, Chainlit and five specialist agents. These formed part of the proposed architecture and should not be described as completed functionality where they were not implemented.

In future, I would define the minimum viable system, evaluation criteria, technical dependencies and evidence requirements before expanding the number of agents.

I would divide proposed features into:

- essential requirements;
- desirable extensions;
- future development.

This would make the design easier to implement, test and evaluate within the available timeframe.

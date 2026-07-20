# Week 7 System Design

The Week 7 design proposed ResearchMate as a cooperative hybrid multi agent system for academic research support. It included Planning, Retrieval, Processing, Ranking and Storage Agents. The Planning Agent used a deliberative approach to divide queries, coordinate tasks and trigger replanning, while the other agents performed more reactive specialist functions.

The architecture was selected to improve modularity, separation of responsibilities and maintainability. LangGraph was proposed for orchestration, with academic services such as arXiv, Semantic Scholar and OpenAlex supporting retrieval.

The design was technically ambitious because it depended on several agents, external services and structured communication. This taught me that system scope must be balanced against available time, development resources and testing requirements.

![ResearchMate hybrid multi agent architecture](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)

## Supporting Evidence

1. [Open the ResearchMate Architecture Diagram](https://fademoye.github.io/intelligent-agents-eportfolio/evidence/team/researchmate-architecture.png)
2. [Team Project](team-project.html)
3. [Week 11 Final Implementation](week-11-implementation.html)
4. [Critical Project Evaluation](project-evaluation.html)

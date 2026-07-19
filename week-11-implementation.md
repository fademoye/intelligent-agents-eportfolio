# Week 11 Final Implementation

## Project Overview

The Week 11 implementation was an individual intelligent-agent project focused on academic research planning.

The system was designed to help users organise a research topic into a structured plan containing:

- a research aim;
- research objectives;
- research questions;
- methodology suggestions;
- a clear output structure.

## Problem Being Addressed

Students can struggle to align their research topic, aim, objectives, questions and methodology.

The implemented system aimed to provide structured guidance and help users develop a more coherent research plan.

## Final System Architecture

The final implementation used a modular structure.

The main components included:

- `main.py` – starts the application and manages user interaction;
- `agent.py` – coordinates the overall ResearchMate workflow;
- `planner.py` – develops the research-planning structure;
- `retriever.py` – supports the retrieval stage;
- `processor.py` – processes the user input and intermediate information;
- `output_generator.py` – produces the final structured output;
- test files – evaluate key parts of the system.

## Final Workflow

1. The user enters a research topic.
2. The system processes the input.
3. The planning component identifies the required research elements.
4. The agent coordinates the relevant modules.
5. The output generator produces a structured research plan.
6. The result is displayed to the user.

## Technologies Used

The implementation used:

- Python;
- GitHub;
  ### GitHub Repository

The repository provides evidence of the final source code, modular project structure, testing files and supporting documentation.

[Open the individual project repository](https://github.com/fademoye/LLM-Planning-Agent-Project)
- modular programming;
- `pytest`;
- command-line interaction;
- structured output generation.

## Code Structure

The project was separated into different modules rather than placing all the logic in one file.

This improved:

- readability;
- maintainability;
- testing;
- separation of responsibilities;
- future extensibility.

## Testing

The system was tested using unit and functional tests.

The tests were used to check:

- whether the planning component produced the expected structure;
- whether the agent workflow operated correctly;
- whether the final output contained the required research-planning elements.

The completed tests passed successfully.

## Example Output

Add an example of the system output here.

```text
Research Topic:
[Insert example]

Research Aim:
[Insert generated aim]

Research Objectives:
1. [Insert objective]
2. [Insert objective]
3. [Insert objective]

Research Questions:
1. [Insert question]
2. [Insert question]

Suggested Methodology:
[Insert methodology]

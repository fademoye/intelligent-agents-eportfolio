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

The final implementation used:

- Python;
- GitHub;
- modular programming;
- pytest;
- command-line interaction;
- structured output generation.

## GitHub Repository

The repository provides evidence of the final source code, modular project structure, testing files and supporting documentation.

[Open the individual project repository](INSERT-YOUR-REAL-REPOSITORY-URL)

## Code Structure

The project was separated into different modules rather than placing all logic in one file.

This improved:

- readability;
- maintainability;
- testability;
- separation of responsibilities;
- future extensibility.

The final implementation used agent-inspired modular components coordinated through a defined workflow. It did not implement fully independent agents with autonomous communication and decision-making.

## Testing

The system was tested using unit and functional tests.

The tests checked:

- whether the planning component produced the expected structure;
- whether the overall workflow operated correctly;
- whether the final output contained the required research-planning elements.

All completed tests passed successfully.

However, passing functional tests did not prove that every generated recommendation was academically accurate or appropriate. Further evaluation would be needed to assess relevance, alignment and usefulness.

## Example Output

Replace this section with one genuine output produced by your system.

## Implementation Evidence

### System Running

![System running](evidence/implementation/system-running.png)

### User Input

![Example user input](evidence/implementation/user-input.png)

### Generated Output

![Generated research plan](evidence/implementation/generated-output.png)

### Project Structure

![Project folder structure](evidence/implementation/project-structure.png)

### Testing Evidence

![Passed pytest results](evidence/testing/pytest-passed.png)

## Limitations

The final implementation was a functional prototype rather than a production-ready system.

Its main limitations were:

- the quality of output depended on the quality of the user input;
- academic-source verification was limited;
- the system could not guarantee that every recommendation was appropriate;
- testing focused mainly on technical functionality;
- the command-line interface was not ideal for non-technical users;
- further user testing and academic review would be required.

## What I Learned

The implementation strengthened my skills in modular Python development, testing, debugging, GitHub and project scoping.

I also learned that technical success and output quality are different. A system can execute correctly while still producing guidance that needs academic verification and human review.

## Connection to Learning Outcomes

This implementation supported:

- Learning Outcome 1 through application and evaluation of agent architecture;
- Learning Outcome 2 through use of agent techniques to address academic research planning;
- Learning Outcome 3 through Python development, testing and consideration of ethical risks;
- Learning Outcome 4 through its connection to the earlier ResearchMate group project and the lessons learned from virtual collaboration.

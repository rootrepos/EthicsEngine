# EthicsEngine

![EthicsEngine Infographic](Ethicsengine.jpg)

**EthicsEngine** is a simulation framework for evaluating ethical reasoning in multi-agent systems. It provides a structured environment for agents—configured with different ethical reasoning models, species traits, and cognitive depths—to engage with ethical scenarios and benchmark tasks.

## Overview

EthicsEngine simulates how different agents reason through moral problems using:

- Reasoning Type (e.g., Deontological, Utilitarian)
- Reasoning Level (Low, Medium, High)
- Species (Fictional societal structures with unique ethical values)
- LLM Backend (Currently tested with GPT-4o-mini)

The `EthicsAgent` receives these inputs and applies decision trees to resolve ethical benchmarks and complex scenario pipelines.

### Workflow

1. Inputs are configured from JSON files (species, golden patterns, scenarios)
2. Agents simulate ethical reasoning using AutoGen
3. Outputs from benchmarks and scenarios are judged for correctness or ethical alignment
4. Results are saved and optionally visualized

## Components

- `reasoning_agent.py` – Defines the EthicsAgent and core reasoning logic
- `run_benchmarks.py` – Evaluates responses to static ethical questions
- `run_scenarios.py` – Simulates dynamic planning, execution, and judgment for scenarios
- `run_scenario_pipelines.py` – Similar to `run_scenarios` but organized as pipelines

## Data Files

- `species.json` – Defines traits for each fictional species
- `golden_patterns.json` – Describes ethical models and principles
- `scenarios.json` – Scenario prompts for simulation
- `simple_bench_public.json` – Benchmark questions and answers

## Getting Started

Install dependencies:

    pip install -r requirements.txt

Set your OpenAI API key as an environment variable.

To run basic examples:

    python run_benchmarks.py --model Deontological --species Jiminies
    python run_scenarios.py --model Utilitarian --species Megacricks

To launch the interactive UI:

    python3 -m dashboard.interactive_dashboard

![Textual Dashboard Screenshot](EthicsDash.png)

## Contributing

We welcome scenario contributions! Please refer to our [Scenario Contribution Guide](scenario_contribution_guide.md) to get started.

## License

MIT License

---

Created by [Eric Moore](https://github.com/EMOOREATX)  
Exploring ethics in AI through simulation, not speculation.

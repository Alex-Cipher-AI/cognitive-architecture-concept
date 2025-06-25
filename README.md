Cipher Cognitive Architecture - PrototypeA research prototype for the Cipher Cognitive Architecture, demonstrating a Differentiable Mediator (GNN) for verifiable neuro-symbolic reasoning.[Status Badge: Research Prototype - In Development - Not for Production Use]Core Concept[cite_start]Current Large Language Models (LLMs) suffer from a "reasoning gap," a fundamental limitation in multi-step logical deduction that leads to hallucinations and makes them unreliable for high-stakes applications[cite: 1, 9, 14, 17]. [cite_start]This project implements a prototype of the Cipher Cognitive Architecture, a novel framework designed to solve this problem by integrating deterministic symbolic reasoning with probabilistic neural networks in a unified, differentiable model[cite: 3, 22].[cite_start]Our architecture is composed of four tiers: a Cognitive Tier for reasoning, a Meta-Cognitive Tier for self-monitoring, an Executive Tier for orchestration, and a Guardrail Tier for ethical oversight[cite: 4].The core innovation validated in this prototype is the Differentiable Mediator. [cite_start]This component, implemented as a Graph Neural Network (GNN) with attention, bridges the gap between the symbolic Logic Engine and the neural Creative Engine (LLM)[cite: 5, 38]. [cite_start]It is trained using multi-modal contrastive learning to create a shared semantic space, allowing the LLM's generative process to be directly and differentiably constrained by formal logic[cite: 5, 43].Prototype Architecture[cite_start]This repository contains the code for the Phase 1 prototype, a programmatic library that implements the core reasoning pipeline to validate the Cognitive Synergy Hypothesis[cite: 7].graph TD
    subgraph Cipher Prototype Library
        A[Input: Logic Puzzle JSON] --> B[LogicEngine];
        B -- Logic Graph --> C[DifferentiableMediator GNN];
        C -- Logic Embedding --> D[CreativeEngine LLM];
        D -- Generated Text --> E[Minimal Guardrail];
        E --> F[Output: Verified Textual Solution];
    end
Getting StartedInstallationClone the repository:git clone https://github.com/Alex-Cipher/cipher-cognitive-architecture.git
cd cipher-cognitive-architecture
Set up a Python 3.11+ virtual environment.Install dependencies:pip install -r requirements.txt
UsageThe library can be used programmatically to solve a defined logic puzzle.from src.pipeline import CipherPipeline

# 1. Initialize the pipeline
pipeline = CipherPipeline(config_path='config/default.yaml')

# 2. Define the puzzle input
puzzle_data = {
    # ... JSON/dict structure for a logic grid puzzle
}

# 3. Solve the puzzle
solution_text = pipeline.solve_puzzle(puzzle_data)
print(solution_text)

# 4. Get validation metrics
metrics = pipeline.get_validation_metrics()
print(metrics)
Running TestsTo ensure the integrity of the components, run the test suite using PyTest.pytest
Citing This WorkIf you use this code or the concepts from our paper in your research, please cite the work as follows:@article{Cipher2025Cognitive,
  title   = {A Four-Tiered Cognitive Architecture for Advanced AI Reasoning},
  author  = {Alex Cipher},
  year    = {2025},
  journal = {arXiv preprint},
  note    = {https://github.com/Alex-Cipher/cipher-cognitive-architecture}
}
LicenseThis project is licensed under the MIT License. See the LICENSE file for details.ContactFor questions, bug reports, or discussion, please use the Issues tab of this repository.

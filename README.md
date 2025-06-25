Cipher Cognitive Architecture - PrototypeA research prototype implementing the core components of the Cipher Cognitive Architecture, a novel framework designed to solve the "reasoning gap" in modern AI by enabling verifiable neuro-symbolic reasoning.📖 WhitepaperFor a comprehensive overview of the theory, architecture, and validation strategy behind this project, please see our full research paper:📄 A Four-Tiered Cognitive Architecture for Advanced AI Reasoning1. Core ConceptCurrent Large Language Models (LLMs) suffer from a fundamental limitation in multi-step logical deduction, leading to hallucinations and making them unreliable for high-stakes applications. This project implements and validates the core of the Cipher Cognitive Architecture, a framework designed to integrate deterministic symbolic reasoning with probabilistic neural networks in a unified, differentiable model.The full architecture is envisioned as four tiers: a Cognitive Tier for reasoning, a Meta-Cognitive Tier for self-monitoring, an Executive Tier for orchestration, and a Guardrail Tier for ethical oversight.The primary innovation validated in this prototype is the Differentiable Mediator. This component, implemented as a Graph Neural Network (GNN) with attention, bridges the gap between the symbolic Logic Engine and the neural Creative Engine (LLM). It is trained using multi-modal contrastive learning to create a shared semantic space, allowing the LLM's generative process to be directly and differentiably constrained by formal logic.2. Prototype ArchitectureThis repository contains the code for the Phase 1 prototype, a programmatic library that implements the core reasoning pipeline to validate the Cognitive Synergy Hypothesis.graph TD
    subgraph "Cipher Prototype Library"
        A[Input: Logic Puzzle JSON] --> B(LogicEngine);
        B -- Logic Graph --> C[DifferentiableMediator GNN];
        C -- Logic Embedding --> D[CreativeEngine LLM];
        D -- Generated Text --> E(Minimal Guardrail);
        E --> F[Output: Verified Textual Solution];
    end
3. Getting StartedPrerequisitesPython 3.11+PyTorchGitInstallationClone the repository:git clone https://github.com/Alex-Cipher/cipher-cognitive-architecture.git
cd cipher-cognitive-architecture
Set up a virtual environment:python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
Install dependencies:pip install -r requirements.txt
4. UsageThe library is designed to be used programmatically. The following example demonstrates the core workflow.# main.py
from src.pipeline import CipherPipeline

def run_prototype():
    """
    Initializes and runs the full puzzle-solving pipeline.
    """
    # 1. Initialize the pipeline with a configuration file
    print("Initializing the Cipher Pipeline...")
    pipeline = CipherPipeline(config_path='config/default.yaml')

    # 2. Define the input logic puzzle
    # This would typically be loaded from a file or another source.
    puzzle_data = {
        "type": "LogicGridPuzzle",
        "entities": {
            "names": ["Alice", "Bob", "Charlie"],
            "pets": ["cat", "dog", "fish"]
        },
        "clues": [
            "The person with the cat is not Alice.",
            "Bob has a dog."
        ]
    }
    print(f"\nSolving puzzle: {puzzle_data['type']}")

    # 3. Solve the puzzle
    print("Executing the reasoning pipeline...")
    solution_text = pipeline.solve_puzzle(puzzle_data)
    print("\n--- Generated Solution ---")
    print(solution_text)

    # 4. Get validation metrics
    metrics = pipeline.get_validation_metrics()
    print("\n--- Validation Metrics ---")
    print(metrics)

if __name__ == "__main__":
    run_prototype()
5. Running TestsTo ensure the integrity of the components and validate the logic, run the test suite using PyTest.pytest
6. Citing This WorkIf you use this code or the concepts from our paper in your research, please use the following BibTeX entry:@article{Cipher2025Cognitive,
  title   = {A Four-Tiered Cognitive Architecture for Advanced AI Reasoning},
  author  = {Alex Cipher},
  year    = {2025},
  journal = {arXiv preprint},
  note    = {https://github.com/Alex-Cipher/cipher-cognitive-architecture}
}
7. LicenseThis project is licensed under the MIT License. See the LICENSE file for details.8. ContactFor questions, bug reports, or to discuss potential collaborations, please open an Issue in this repository.

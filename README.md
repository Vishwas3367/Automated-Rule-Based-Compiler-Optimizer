# Automated Rule-Based Compiler Code Optimizer

**A Python-based compiler optimization system for improving Three-Address Code (TAC) through rule-based transformations, iterative optimization, and output verification.**

## About the Project

The Automated Rule-Based Compiler Code Optimizer is designed to identify inefficient intermediate-code instructions and transform them into simpler, equivalent forms using a collection of optimization rules.

The system demonstrates core compiler design concepts through six optimization techniques, a dedicated optimization engine, program-output comparison, a graphical user interface, and benchmark result visualization.

## Key Objectives

- Implement rule-based optimization techniques for intermediate code.
- Reduce unnecessary instructions and simplify expressions.
- Apply optimization passes iteratively where applicable.
- Compare original and optimized program outputs for supported test cases.
- Measure optimization results using implemented metrics.
- Provide an interface for running optimizations and viewing results.

## Optimization Techniques

| Technique | Description |
|---|---|
| Constant Folding | Evaluates constant expressions during optimization. |
| Constant Propagation | Substitutes known constant values into applicable expressions. |
| Algebraic Simplification | Simplifies expressions using algebraic identities. |
| Common Subexpression Elimination | Reuses equivalent computations when safe. |
| Dead Code Elimination | Removes instructions whose results are unnecessary. |
| Strength Reduction | Replaces supported operations with simpler alternatives. |

## System Workflow

1. **Input:** Accept a supported program or intermediate-code representation.
2. **Intermediate Representation:** Process the input into Three-Address Code (TAC), where supported by the implementation.
3. **Original Execution:** Execute the original TAC and record its output.
4. **Optimization:** Apply the six optimization techniques through the optimization engine.
5. **Repeated Passes:** Repeat optimization passes until the configured stopping condition is reached.
6. **Optimized Execution:** Execute the resulting optimized TAC.
7. **Verification:** Compare the original and optimized outputs for the selected inputs.
8. **Evaluation:** Calculate available metrics and display benchmark results.

## Technology Stack

- **Language:** Python
- **Intermediate Code:** Three-Address Code (TAC)
- **GUI:** Tkinter
- **API:** FastAPI
- **Data Visualization:** Matplotlib
- **Image Support:** Pillow
- **Result Storage:** CSV and JSON
- **Testing:** Python test modules

## Repository Structure

```text
Automated-Rule-Based-Compiler-Optimizer/
└── Automated-Rule-Based-Compiler-Optimizer-Full/
    ├── gui/
    │   └── app.py
    ├── optimizers/
    │   ├── __init__.py
    │   ├── algebraic_simplification.py
    │   ├── constant_folding.py
    │   ├── constant_propagation.py
    │   ├── cse.py
    │   ├── dead_code.py
    │   ├── engine.py
    │   ├── strength_reduction.py
    │   └── utils.py
    ├── results/
    │   ├── benchmark_results.csv
    │   ├── benchmark_summary.json
    │   └── visualization files
    ├── tests/
    │   └── test_all.py
    ├── main.py
    ├── metrics.py
    ├── optimizer_api.py
    ├── test_optimizer_api.py
    ├── visualization.py
    └── requirements.txt
```

## Getting Started

### Prerequisites

- Python installed on your system
- pip package manager
- Git

### 1. Clone the Repository

```bash
git clone https://github.com/Vishwas3367/Automated-Rule-Based-Compiler-Optimizer.git
cd Automated-Rule-Based-Compiler-Optimizer
```

Enter the project directory:

```bash
cd Automated-Rule-Based-Compiler-Optimizer-Full
```

### 2. Create a Virtual Environment

**Windows PowerShell**

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

**macOS/Linux**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install Dependencies

```bash
python -m pip install -r requirements.txt
```

### 4. Run the Application

Launch the main application:

```bash
python main.py
```

To start the API, if `optimizer_api.py` defines a FastAPI application named `app`:

```bash
uvicorn optimizer_api:app --reload
```

The API documentation is normally available at:

`http://127.0.0.1:8000/docs`

Run these commands from the directory containing the relevant Python files. The exact startup command depends on the project's configuration.

## Testing

Run the available test suite using:

```bash
python -m pytest
```

If pytest is not installed, install it or use the test runner specified by the project.

Testing should cover:

- Individual optimization rules
- Original and optimized program execution
- Output comparison
- API functionality
- Regression cases for supported TAC expressions

A successful output comparison demonstrates correctness for the tested inputs; it does not establish correctness for every possible program.

## Benchmarking and Visualization

The `results/` directory contains benchmark data and generated visualizations. Depending on the selected benchmark, evaluation can include:

- Instruction counts before and after optimization
- Instruction reduction
- Temporary-variable reduction, where measured
- Optimization effectiveness by category
- Optimization convergence
- Output-verification results

Performance claims should be based on the benchmark files generated by the actual implementation.

## Applications

- Compiler design education and experimentation
- Intermediate-code optimization demonstrations
- Analysis of rule-based optimization techniques
- Comparison of code before and after optimization
- Testing and evaluation of optimization transformations

## Future Scope

- Support additional source-language constructs.
- Introduce more optimization rules.
- Expand test datasets and regression testing.
- Improve optimization diagnostics and execution traces.
- Extend benchmarking to larger and more diverse programs.
- Explore integration with established compiler toolchains.

## Contributors

- Vishwas Kumar
- Aakriti Tiwari

## License

No license has been specified. A license can be added to clarify permitted use, modification, and redistribution.

---

**Disclaimer:** This project is intended for educational and experimental purposes. Its capabilities depend on the supported input syntax, implemented optimization rules, and test coverage.

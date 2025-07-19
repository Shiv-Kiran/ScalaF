# ScalaF: Functional Refactoring Suggestions for Scala

**ScalaF** is a static analysis tool and VS Code extension that detects imperative code patterns in Scala and suggests functional refactorings. The tool is designed to help Scala developers write more idiomatic, parallelizable, and side-effect-free code.

## ✨ Features

- 🚀 **Loop Refactoring**: Detects `for`/`while` loops with no side-effects and recommends `map`, `filter`, `fold`, etc.
- ⚡ **Parallelism Suggestions**: Suggests `par` collection methods when loops are safe to parallelize.
- 🧠 **Scalameta-Powered**: Uses the [Scalameta](https://scalameta.org/) toolkit for precise AST analysis and pattern matching.
- 🧩 **VS Code Integration**: Inline refactoring suggestions inside your editor via a lightweight extension.

## 🛠️ How It Works

1. The **Scala backend** statically analyzes Scala source code for imperative constructs.
2. It matches refactorable patterns using Scalameta’s semantic tree (e.g., side-effect-free loops, accumulators).
3. The **VS Code extension** communicates with the backend and displays refactoring suggestions in the editor.

## 📦 Repository Structure

```bash
ScalaF/
├── ScalaRefactoringBackend @ a094525/          # Scala CLI backend with static analysis logic
├── scala-func-refactor-VSCPlugin @ 7a13bed/        # VS Code extension (TypeScript)
├── benchmarks/       # Micro-benchmarks for functional vs imperative code
├── examples/         # Sample Scala programs and refactorings
└── README.md

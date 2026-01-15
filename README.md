# Deterministic Finite Automaton Simulator (C#)

This repository contains a **C# console application** that simulates a **deterministic finite automaton (DFA)**.  
The program loads an automaton from a text file, validates its structure, displays it, and evaluates binary strings (`0` and `1`) to determine acceptance or rejection.

>  The source code and test files were uploaded from an academic project archive.  
> This README is intentionally maintained at the repository root to clearly document the project for recruiters and reviewers.

---

##  Project Objectives
- Implement a deterministic finite automaton simulator
- Apply object-oriented programming principles in C#
- Validate formal constraints of automata (determinism, initial state, transitions)
- Provide clear console output and execution trace

---

##  Main Features
- Load automata from a structured text file
- Validate automata integrity:
  - Rejects automata with **no states**
  - Rejects automata with **no initial state**
  - Rejects **non-deterministic** automata
- Ignores invalid transitions referencing non-existing states (with warnings)
- Displays the automaton using clear notation:
  - `[q0]` → initial state
  - `(q2)` → final state
  - `[(q0)]` → initial and final state
- Validates input strings composed only of `0` and `1`
- Correctly handles empty strings

---

##  Automaton File Format

### State definition
```
state <name> <isFinal 0/1> <isInitial 0/1>
```

Example:
```
state q0 1 1
```

### Transition definition
```
transition <sourceState> <symbol> <destinationState>
```

Example:
```
transition q0 0 q1
```

---

##  Test Files
The folder `Fichiers_Tests/` contains several test cases, including:
- A valid deterministic automaton
- An automaton without an initial state
- An automaton without states
- A non-deterministic automaton
- A partially valid automaton (invalid transitions ignored)

---

##  How to Run
**Requirements:** .NET SDK (project originally targets .NET 5.0)

```bash
dotnet restore
dotnet run
```

When prompted, press **ENTER** to load the default test file:
```
Fichiers_Tests/1_automate_conforme.txt
```

---

##  Academic Context
This project was completed as part of an academic assignment in the **Bachelor of Computer Science program (UQTR)**.  
It demonstrates skills in **software design, formal models, and validation logic**.

---

##  Author
**Ivan Ndia**  
Computer Science student – Application Development & Cybersecurity  
Canada

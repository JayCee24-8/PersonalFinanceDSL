# Personal Finance DSL: A Customizable Financial Management Tool

## Overview

**Personal Finance DSL** is a Python-based project that leverages the **TextX** library to create a Domain-Specific Language (DSL) for personal finance management. 
The project allows **domain experts** to configure runtime environments dynamically and enables **end users** to interact with a tailored financial management interface. 
By combining the flexibility of TextX with SQLite databases and Python runtime, the system offers a powerful and adaptable tool for managing incomes, expenses, budgets, and goals.

---

## Features

### For Domain Experts
- **DSL with TextX**:
  - Grammar defined using TextX in `finance_dsl.tx`.
  - Human-readable syntax for defining configuration rules.

- **Integrated Development Environment (IDE)**:
  - Write, validate, and save DSL rules.
  - Syntax and semantic validation powered by TextX.
  - Store configurations in an SQLite database (`finance_rules.db`).

### For End Users
- **Dynamic Runtime**:
  - Interfaces are generated dynamically based on rules defined in the DSL.
  - Fully customizable windows (`Incomes`, `Expenses`, `Budgets`, `Goals`).
  - Input financial data, generate reports, and manage personal finances easily.

- **Data Management**:
  - User data stored in `user_data.db`.
  - Generate reports dynamically based on user inputs and configurations.

---

## How It Works

### Role of TextX
TextX is used to define and parse the DSL grammar:
- **Grammar Definition**: The structure of the DSL is defined in `finance_dsl.tx`, enabling domain experts to write human-readable rules.
- **Parsing and Validation**: The TextX engine parses DSL configurations, converts them into internal data structures, and validates them for logical consistency.
- **Integration**: Parsed rules are saved to `finance_rules.db` for use during runtime.

### Architecture
1. **Domain-Specific Language**:
   - Grammar defined in `finance_dsl.tx`.
   - Syntax for enabling windows, customizing fields, and configuring reports.

2. **Parsing and Validation**:
   - TextX ensures DSL rules are correctly written and logically sound.

3. **Databases**:
   - `finance_rules.db`: Stores DSL configurations.
   - `user_data.db`: Stores runtime user inputs.

4. **Dynamic Runtime**:
   - Generates the interface and functionality based on configurations stored in `finance_rules.db`.

---

## Workflow

1. **Domain Expert**:
   - Uses the IDE to write and validate DSL rules.
   - Saves rules to the `finance_rules.db` using TextX parsing.

2. **Runtime**:
   - Reads configurations from `finance_rules.db`.
   - Dynamically constructs tabs, fields, buttons, and reports.

3. **End User**:
   - Interacts with the dynamically generated interface to manage finances.

---

## Getting Started

### Prerequisites
- Python 3.x
- SQLite3
- **TextX Library**:
  Install TextX using pip:
  ```bash
  pip install textx

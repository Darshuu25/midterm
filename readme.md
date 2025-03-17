# Advanced Python Calculator

## Project Overview
This is an advanced Python-based calculator application built for my IS601 midterm project. It supports arithmetic operations, history management, and dynamic plugin loading for extended functionalities via a command-line REPL interface.

## Calculator Features
- **Basic Operations**: Add, Subtract, Multiply, Divide.
- **History Management**: Calculation history stored using Pandas, with options to load, save, and clear history.
- **Plugin System**: Dynamically load commands (e.g., custom math functions) without modifying core code.
- **Extendable Command System**: Commands for operations like add, subtract, and more are modularized in the `commands/` folder.

## Project Structure
```
calculator/     # Core functionality and REPL
commands/       # Additional operations as plugins (e.g., add, subtract)
tests/          # Unit tests for the calculator and plugins
data/           # Stores history in CSV format
```

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/Deneisha98/IS601_Midterm_24.git
   cd IS601_Midterm_24
   ```
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Run the REPL:
   ```sh
   python calculator/main.py
   ```

## Usage Examples
- Perform calculations:
  ```sh
  > 3 + 5
  8
  ```
- Use plugins:
  ```sh
  > sqrt 16
  4.0
  ```
- Manage history:
  ```sh
  > save
  > load
  > history
  > clear
  ```

## Running Tests and Coverage Report
- Run all unit tests:
  ```sh
  pytest
  ```
- Run tests with coverage:
  ```sh
  pytest --cov=calculator
  ```

## Design Patterns Used
- **Facade Pattern**: Simplifies Pandas data management.
- **Command Pattern**: Structure for REPL commands.
- **Plugin Pattern**: Dynamically loads plugins for extensibility.

## Environment Variables
Environment variables, configured through `.env`, control logging levels:
```sh
LOG_LEVEL=INFO
```
[Implementation Link](https://github.com/Darshuu25/midterm/blob/main/calculator/main.py#L9)

## Logging Feature
Logging is dynamically configured using environment variables. Logs include informational messages and error handling for debugging.
[Implementation Link](https://github.com/Darshuu25/midterm/blob/main/calculator/main.py#L36)

## Error Handling
Implements LBYL and EAFP error-handling strategies:
- **LBYL**: Checks for conditions like file existence before operations.
- **EAFP**: Wraps potentially erroneous plugin loads in try/except blocks.
[Implementation Link](https://github.com/Darshuu25/midterm/blob/main/calculator/main.py#L66)

## Video Demonstration
[Watch Video]https://drive.google.com/file/d/1JzHhY3zP_aBlcEYcUPLLldbGIh0vXvHT/view?usp=sharing


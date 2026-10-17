# Calculator

A command-line calculator application that evaluates mathematical expressions and outputs results in JSON format.

## Features

- Supports basic arithmetic operations: addition (`+`), subtraction (`-`), multiplication (`*`), division (`/`), modulo (`%`), and exponentiation (`**`)
- Handles operator precedence and parentheses for complex expressions
- Outputs results in a structured JSON format
- Clean, modular architecture with separate components for calculation and rendering

## Project Structure

```
calculator/
├── main.py              # Entry point - parses CLI arguments and runs the calculator
├── pkg/
│   ├── calculator.py    # Core Calculator class with expression evaluation logic
│   └── render.py        # JSON output formatting
├── tests.py             # Unit tests
└── idea.md              # Project notes and ideas
```

## Usage

Run the calculator from the command line, passing a mathematical expression as an argument:

```bash
python main.py "<expression>"
```

### Examples

```bash
# Basic arithmetic
python main.py "3 + 5"
# Output:
# {
#   "expression": "3 + 5",
#   "result": 8
# }

# Complex expressions with precedence
python main.py "2 + 3 * 4"
# Output:
# {
#   "expression": "2 + 3 * 4",
#   "result": 14
# }

# Parentheses for grouping
python main.py "(2 + 3) * 4"
# Output:
# {
#   "expression": "(2 + 3) * 4",
#   "result": 20
# }

# Exponentiation
python main.py "2 ** 10"
# Output:
# {
#   "expression": "2 ** 10",
#   "result": 1024
# }

# Division
python main.py "10 / 4"
# Output:
# {
#   "expression": "10 / 4",
#   "result": 2.5
# }
```

If no expression is provided, the app displays usage instructions:

```bash
python main.py
# Output:
# Calculator App
# Usage: python main.py "<expression>"
# Example: python main.py "3 + 5"
```

## Running Tests

Run the test suite to verify functionality:

```bash
python tests.py
```

## Requirements

- Python 3.10+ (uses `float | None` union type syntax)

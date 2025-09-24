# CS61A Code Workspace

This directory contains the CS61A course code exercises, labs, and homework assignments used in the course.

The repository is organized by assignment/lab folders. Each folder typically contains:

- `*.py` or `src/` files: the exercise source code
- `tests/`: automated tests for the exercise
- `ok` files and `.ok_` state files used by the autograder (OkPy)

Common folders you will find here:

- `lab00/`, `lab01/`, `lab02/`, ... — lab exercises
- `hw01/`, `hw02/`, ... — homework assignments
- `hog/` — example project with GUI and tests
- `tests/` — shared test utilities

## How to run tests

This repository uses plain Python files and OkPy-style test harnesses for many assignments. Use the following approaches depending on the assignment.

### Run a single test file (recommended for quick checks)

Open a PowerShell terminal at the repository root (this README assumes Windows PowerShell) and run:

```powershell
# Run a single test using python
python -m pytest path\to\tests\00.py
```

Or run all tests in a subdirectory:

```powershell
python -m pytest lab01\tests
```

### Using OkPy (course autograder)

Some assignments include OkPy harness files. Follow your course instructions for authentic submission. Typically you run the provided `ok` script in the assignment directory, for example:

```powershell
cd hw01
# If the repository provides an 'ok' wrapper; otherwise follow your course's submission steps
./ok
```

> Note: On Windows you may need to run `python ok` if the `ok` script is not executable.

## Common troubleshooting

- If tests cannot import modules, ensure you run pytest from the repository root so Python's module resolution finds packages correctly.
- If a script expects input files, check `inputFiles/` inside the assignment folder and run examples from that folder.
- If the autograder `ok` script fails, make sure Python3 is installed and your virtualenv (if any) has required packages.

## Suggested improvements

- Add a top-level `pyproject.toml` or `requirements.txt` to document Python version and dependencies.
- Add simple PowerShell scripts for common test invocations.
- Add per-assignment README files with specific run examples.

---

If you want, I can:

- Add a `requirements.txt` and a simple `python -m pytest` script for the `hog` project as an example.
- Create a top-level PowerShell script `run-tests.ps1` to run a chosen subset of tests.

Tell me which you'd like next.

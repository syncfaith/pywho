# Contributing to pywho

Thanks for your interest in contributing to pywho! This document provides guidelines and instructions for contributing.

## Development setup

1. Fork and clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/pywho.git
cd pywho
```

2. Create a virtual environment and install dependencies:

```bash
uv venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
uv pip install -e ".[dev]"
```

3. Install pre-commit hooks:

```bash
pip install pre-commit
pre-commit install
```

## Running tests

```bash
# Run all tests
make test

# Run with verbose output
pytest -v

# Run a specific test
pytest tests/test_inspector.py::TestVenvDetection -v
```

## Code quality

```bash
# Run linter
make lint

# Auto-format code
make format

# Run type checker
make typecheck

# Run everything
make all
```

## Making changes

1. Create a branch for your change:

```bash
git checkout -b your-feature-name
```

2. Make your changes and ensure:
   - All tests pass (`make test`)
   - Code is formatted (`make format`)
   - Linter passes (`make lint`)
   - Type checker passes (`make typecheck`)

3. Commit your changes with a clear message:

```bash
git commit -m "feat: add support for ..."
```

We follow [Conventional Commits](https://www.conventionalcommits.org/):
- `feat:` for new features
- `fix:` for bug fixes
- `docs:` for documentation changes
- `test:` for test additions/changes
- `chore:` for maintenance tasks

4. Push and open a pull request.

## Adding support for a new venv type

To add detection for a new virtual environment manager:

1. Add detection logic in `src/pywho/inspector.py` in the `_detect_venv()` function
2. Add the type string to the `VenvInfo.type` field documentation
3. Add a test in `tests/test_inspector.py`
4. Update the README table

## Reporting issues

- Use the [GitHub issue tracker](https://github.com/AhsanSheraz/pywho/issues)
- Include the output of `pywho --json` when reporting environment-related issues

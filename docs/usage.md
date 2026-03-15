# Usage

## CLI

### Basic inspection

```bash
pywho
```

Prints a formatted report of your current Python environment.

### JSON output

```bash
pywho --json
```

Outputs a JSON object — useful for CI pipelines, scripting, or sharing in bug reports.

### Include installed packages

```bash
pywho --packages
```

Adds a full list of installed packages with versions to the output.

### Skip pip version check

```bash
pywho --no-pip
```

Skips the subprocess call to detect pip version, making the output slightly faster.

### Run as a module

```bash
python -m pywho
```

### Combine flags

```bash
pywho --json --packages
```

## Exit codes

| Code | Meaning |
|------|---------|
| `0`  | Success |

## Python library

```python
from pywho import inspect_environment

report = inspect_environment()

# Access fields directly
print(report.executable)
print(report.version)
print(report.venv.is_active)
print(report.venv.type)
print(report.package_manager)

# Skip package listing for speed
report = inspect_environment(include_packages=False)

# Serialize to dict (JSON-compatible)
data = report.to_dict()
```

## Common workflows

### Paste into a GitHub issue

```bash
pywho --json | pbcopy  # macOS
pywho --json | xclip   # Linux
```

### Save environment snapshot in CI

```bash
pywho --json --packages > environment.json
```

### Compare two environments

```bash
# On machine A
pywho --json > env-a.json

# On machine B
pywho --json > env-b.json

# Diff
diff env-a.json env-b.json
```

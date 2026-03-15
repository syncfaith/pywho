# Installation

## Requirements

- Python 3.9 or later
- No additional dependencies (stdlib only)

## With pip

```bash
pip install pywho
```

## With uv

```bash
uv pip install pywho
```

## Run without installing

```bash
uvx pywho
```

## From source

```bash
git clone https://github.com/AhsanSheraz/pywho.git
cd pywho
pip install .
```

## Development install

```bash
git clone https://github.com/AhsanSheraz/pywho.git
cd pywho
uv venv && source .venv/bin/activate
uv pip install -e ".[dev]"
```

## Verify installation

```bash
pywho --version
```

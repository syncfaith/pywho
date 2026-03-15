# API Reference

## `inspect_environment`

```python
from pywho import inspect_environment

report = inspect_environment(include_packages=True)
```

**Parameters:**

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `include_packages` | `bool` | `True` | Whether to list installed packages. Set to `False` for faster output. |

**Returns:** `EnvironmentReport`

---

## `EnvironmentReport`

Frozen dataclass containing the full environment snapshot.

### Interpreter fields

| Field | Type | Description |
|-------|------|-------------|
| `executable` | `str` | Path to the Python executable |
| `version` | `str` | Python version string (e.g., `"3.12.3"`) |
| `version_info` | `str` | Major.minor.micro version |
| `implementation` | `str` | Python implementation (e.g., `"CPython"`) |
| `compiler` | `str` | Compiler used to build Python |
| `architecture` | `str` | `"64-bit"` or `"32-bit"` |
| `build_date` | `str` | Build info string |

### Platform fields

| Field | Type | Description |
|-------|------|-------------|
| `platform_system` | `str` | OS name (e.g., `"Darwin"`, `"Linux"`, `"Windows"`) |
| `platform_release` | `str` | OS release version |
| `platform_machine` | `str` | Machine architecture (e.g., `"arm64"`, `"x86_64"`) |

### Virtual environment

| Field | Type | Description |
|-------|------|-------------|
| `venv` | `VenvInfo` | Virtual environment details |

### Path fields

| Field | Type | Description |
|-------|------|-------------|
| `prefix` | `str` | `sys.prefix` |
| `base_prefix` | `str` | `sys.base_prefix` |
| `exec_prefix` | `str` | `sys.exec_prefix` |
| `sys_path` | `list[str]` | Copy of `sys.path` |
| `site_packages` | `list[str]` | Active site-packages directories |

### Package management

| Field | Type | Description |
|-------|------|-------------|
| `package_manager` | `str` | Detected package manager |
| `pip_version` | `str \| None` | pip version if available |
| `packages` | `list[PackageInfo]` | Installed packages (if requested) |

### Methods

#### `to_dict() -> dict`

Returns a JSON-serializable dictionary of the full report.

---

## `VenvInfo`

Frozen dataclass for virtual environment details.

| Field | Type | Description |
|-------|------|-------------|
| `is_active` | `bool` | Whether a venv is active |
| `type` | `str` | One of: `"venv"`, `"virtualenv"`, `"uv"`, `"conda"`, `"poetry"`, `"pipenv"`, `"none"` |
| `path` | `str \| None` | Path to the virtual environment |
| `prompt` | `str \| None` | Venv prompt name |

---

## `PackageInfo`

Frozen dataclass for an installed package.

| Field | Type | Description |
|-------|------|-------------|
| `name` | `str` | Package name |
| `version` | `str` | Installed version |
| `location` | `str` | Installation path |

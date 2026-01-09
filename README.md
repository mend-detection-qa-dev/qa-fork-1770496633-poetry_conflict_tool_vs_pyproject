# Test Case: Poetry Conflict - .tool-versions vs tool.poetry.dependencies

## Package Manager
Poetry

## Python Version Detection
- **Source**: .tool-versions (PRIORITY #2)
- **Expected Version**: 3.11.2
- **Conflict**: tool.poetry.dependencies.python says ^3.10

## Files Present
- .tool-versions - python 3.11.2 (SHOULD WIN)
- pyproject.toml - python = "^3.10" (SHOULD BE IGNORED)
- poetry.lock

## Test Purpose
Validate .tool-versions beats Poetry's python dependency.

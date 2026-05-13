# dietmcp

MCP/OpenAPI/GraphQL to CLI bridge focused on token-efficient tool usage.

## Installation

1) Install Python 3.10+
```bash
python3 --version
```


2) Clone and enter the repo
```bash
git clone <repo-url>
cd <repo-name>
```

## Quick Start

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt  # or pip install -e .
```

## Usage Examples

- Run locally
```bash
python -m <module_or_script>
```

- Run tests
```bash
pytest
```

- Show MCP bridge help
```bash
cargo run -- --help
```

## Implementation Overview

This repository is implemented primarily in **Python** and organized around explicit runtime entrypoints plus supporting modules.

### Key Directories

- `.github/`
- `benchmark_results/`
- `docs/`
- `examples/`
- `scripts/`
- `src/`
- `tests/`

### Key Files

- `pyproject.toml`
- `README.md`
- `LICENSE`
- `.env.example`
- `.github/workflows/ci.yml`

### Entrypoints


## Troubleshooting

- If startup fails, run the primary command with verbose flags and capture stderr logs.
- If dependencies conflict, remove lock artifacts and reinstall in a clean shell.
- If tests fail intermittently, run a single test target first, then full suite.
- Ensure environment variables are loaded before running build/train commands.

## Visual Overview

![dietmcp visual overview](docs/assets/visual-overview-dietmcp.svg)


## Problem
Full schema injection is costly and brittle for long sessions.

## Reproducibility
```bash
pip install dietmcp
dietmcp --help
```

## Limits
Benefits depend on tool catalog and output distribution.

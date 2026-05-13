# dietmcp

MCP/OpenAPI/GraphQL to CLI bridge focused on token-efficient tool usage.

## Presentation Framework (Proven README Pattern)

### TL;DR
MCP/OpenAPI/GraphQL-to-CLI bridge designed to reduce tool-call token overhead.

### Why this project
- Solves a concrete workflow problem with reproducible command paths.
- Prioritizes operator reliability over demo-only output.
- Structured for practical use, not just conceptual documentation.

### Quick Start
```bash
dietmcp --help
```

### Installation
```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -U pip
python -m pip install -e .
```

### Usage Examples
```bash
dietmcp discover --help
dietmcp exec --help
```

### Architecture at a glance
- src/dietmcp/main.py — CLI root command group
- src/dietmcp/cli/ — subcommands (discover/exec/cache/config/skills)
- tests/ — integration and protocol behavior validation

### Troubleshooting
- If no tools are discovered, verify endpoint/auth config.
- If command missing, reactivate venv and reinstall editable package.

### Project status
Focused on better discovery ergonomics and lower-latency tool execution paths.


## Installation

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -U pip
python -m pip install -e .
```

## Quick Start

```bash
dietmcp --help
dietmcp discover --help
dietmcp exec --help
```

## Usage Examples

- Inspect cache/config commands
```bash
dietmcp cache --help && dietmcp config --help
```

- Discover available tools from configured endpoints
```bash
dietmcp discover
```

- Execute bridged command with compact output
```bash
dietmcp exec --help
```

## Implementation Overview

- `src/dietmcp/main.py` registers the command group and top-level CLI lifecycle.
- `src/dietmcp/cli/` contains subcommands (`discover`, `exec`, `cache`, `config`, `skills`).
- `examples/` and `tests/` cover integration patterns and protocol behavior.
- `pyproject.toml` tracks package metadata and dependency constraints.

## Troubleshooting

- If `dietmcp` command is missing, reactivate venv and reinstall editable package.
- If discovery returns empty results, verify upstream MCP/OpenAPI/GraphQL endpoints and auth.
- If output is noisy, tune CLI flags and cache settings before invoking from agent loops.

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

## Contributing

Contributions are welcome. Open an issue first for significant changes, then submit a focused PR with reproducible validation steps.

## License

See `LICENSE` for terms.

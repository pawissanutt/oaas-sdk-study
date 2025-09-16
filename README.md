# OaaS SDK Study

Quick workspace for exploring serverless with FaaS vs OaaS using Python and the `oaas-sdk2-py` library.

## Notebooks
- Tutorial: [OaaS_FaaS_tutorial.ipynb](OaaS_FaaS_tutorial.ipynb)
- Programming task: [OaaS_FaaS_programing_task_template.ipynb](OaaS_FaaS_programing_task_template.ipynb)

The tutorial is designed with mocking code, so you don’t need any cloud services to run the examples locally.

## Setup
Requirements:
- Python 3.12+
- VS Code with the Python and Jupyter extensions

This repo includes `pyproject.toml` and `uv.lock`.

1) Create the environment and install deps (including dev tools like ipykernel):

```bash
# Optional: install uv if you don't have it
# iwr https://astral.sh/uv/install.ps1 -UseBasicParsing | iex

uv sync --dev
```

## Notes
- Code samples use `OaasConfig(mock_mode=True)` for local runs; no external services are required.
- If `uv sync` fails, confirm Python 3.12 is on PATH and try removing `.venv` before retrying.

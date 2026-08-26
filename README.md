# promptmill

Feed a thousand prompts, get a thousand answers

Small but I use it weekly.

## What it does

- JSONL in, JSONL out: stream-safe for huge inputs
- Retries failed items with backoff, logs them aside
- Concurrent workers with a rate ceiling
- Idempotent: skips ids already present in the output

## Installation

```bash
pip install -r requirements.txt
export OPENAI_API_KEY=sk-...
```

## Examples

```bash
python batch.py prompts.jsonl -o answers.jsonl --workers 4
```

## Project structure

```text
├── .github/
│   └── dependabot.yml
├── docs/
│   ├── configuration.md
│   ├── roadmap.md
│   └── usage.md
├── .gitignore
├── CHANGELOG.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
├── SECURITY.md
├── batch.py
├── prompts.sample.jsonl
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python -m pytest -q
```

## License

MIT. Do whatever you want.

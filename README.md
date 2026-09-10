# logprune

A tiny CLI to clean, rotate and archive old log files

## Installation

```bash
pip install -r requirements.txt
python -m logwash --help
```

## Features

- Dry-run mode shows what would happen, touches nothing
- Exit codes friendly for cron and CI
- Filter by age (--older-than) or size (--larger-than)
- Archive matched logs into a timestamped .tar.gz
- Scan directories for log files by glob pattern

## How to use

```bash
# show what would be cleaned, change nothing
logwash ./logs --older-than 30 --dry-run

# archive logs older than 30 days
logwash ./logs --older-than 30 --archive ./backup
```

## Project structure

```text
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.md
│   ├── workflows/
│   │   └── ci.yml
│   └── dependabot.yml
├── docs/
│   ├── faq.md
│   └── roadmap.md
├── examples/
│   └── quickstart.md
├── logwash/
│   ├── __init__.py
│   ├── __main__.py
│   ├── cli.py
│   └── utils.py
├── tests/
│   └── test_cli.py
├── .gitignore
├── CHANGELOG.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
├── pyproject.toml
└── requirements.txt
```

## License

MIT - see [LICENSE](LICENSE).

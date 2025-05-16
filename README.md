# Sentra: Autonomous Network Security Assistant

## Overview
Sentra is an open-source, agentic, and autonomous network security assistant. It discovers network assets, runs reconnaissance (Nmap), correlates vulnerabilities (CVEs), and structures audit-ready reports. Future plans include LLM/agent integration and a GUI.

## Features
- Network asset discovery
- Nmap-based scanning
- CVE correlation (local/remote)
- Structured asset inventory
- CLI interface (GUI coming soon)

## Installation
```sh
# Clone repo
# Create virtualenv and activate
python3 -m venv .venv
source .venv/bin/activate.fish
pip install -r requirements.txt
```

## Usage
```sh
python -m sentra.cli.main --target 192.168.1.0/24 --verbose
```

## Configuration
- Copy `.env.example` to `.env` and fill in secrets/API keys as needed.

## Extending
- Add new agents in `sentra/core/agents.py`
- Add new scanners in `sentra/core/scanner.py`
- Add models in `sentra/core/models.py`

## Security Best Practices
- Never commit `.env` or secrets
- Validate all user input
- Use subprocess securely (never `shell=True`)
- Rotate logs and restrict permissions

## Contributing
Pull requests welcome! See `CONTRIBUTING.md` for guidelines.

## License
MIT

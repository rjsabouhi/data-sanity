# datasanity

## Overview
A tiny (<200 lines of code) Python package for CSV health checking and anomaly detection. It analyzes CSV files and produces human-readable reports covering:
- Missing value percentages
- Duplicate row counts
- Cardinality per column
- Basic anomaly detection (z-score > 3)

## Project Structure
```
datasanity/
├── datasanity/           # Main package
│   ├── __init__.py       # Package exports
│   ├── core.py           # CSV analysis logic
│   └── report.py         # Report formatting
├── tests/
│   ├── __init__.py
│   └── test_core.py      # Unit tests
├── demo.csv              # Sample data file
├── run_demo.py           # Demo script
├── pyproject.toml        # Package configuration
├── README.md             # Documentation
└── LICENSE               # MIT License
```

## Dependencies
- pandas
- numpy
- pytest (for testing)

## Usage
```python
from datasanity import analyze_csv, pretty_report

result = analyze_csv("data.csv")
print(pretty_report(result))
```

## Packaging for Export
To create distributable packages:
```bash
cd datasanity
pip install build
python -m build
```

This creates `.whl` and `.tar.gz` files in `dist/` for local installation or PyPI upload.

## Running Tests
```bash
cd datasanity
pytest tests/
```

## Recent Changes
- Initial project setup (Jan 2026)

**Repository: beluga-dragon-delivery-system**

```
beluga-dragon-delivery-system/
├── .github/
│   ├── workflows/
│   │   └── ci.yml
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.md
│   ├── PULL_REQUEST_TEMPLATE.md
│   ├── CODE_OF_CONDUCT.md
│   └── CONTRIBUTING.md
├── .gitignore
├── LICENSE
├── README.md
├── requirements.txt
├── docs/
│   ├── design.md
│   └── architecture_diagram.png  # Placeholder for architecture diagram
├── data/
│   └── gas_cells.csv
├── src/
│   ├── __init__.py
│   ├── mother_ship.py
│   ├── dragon_drone.py
│   ├── transfer_system.py
│   └── control_center.py
└── simulation/
    └── buoyancy_simulation.py
```

---

## .github/workflows/ci.yml

```yaml
name: CI
on:
  push:
    branches: [main]
  pull_request:
    branches: [main]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Set up Python
        uses: actions/setup-python@v4
        with:
          python-version: '3.8'
      - name: Install dependencies
        run: |
          python -m pip install --upgrade pip
          pip install -r requirements.txt
      - name: Lint with flake8
        run: |
          pip install flake8
          flake8 src
      - name: Run tests
        run: |
          # TODO: add test suite
          echo "No tests configured yet"
```

---

## .github/ISSUE_TEMPLATE/bug_report.md

```markdown
---
name: Bug report
about: Create a report to help us improve
---

**Describe the bug**
A clear and concise description of what the bug is.

**To Reproduce**
Steps to reproduce the behavior:
1. ...
2. ...

**Expected behavior**
A clear and concise description of what you expected to happen.

**Screenshots**
If applicable, add screenshots to help explain your problem.

**Desktop (please complete the following information):**
- OS: [e.g. Ubuntu 20.04]
- Python version: [e.g. 3.8]

**Additional context**
Add any other context about the problem here.
```

---

## .github/PULL_REQUEST_TEMPLATE.md

```markdown
<!-- Thank you for your contribution! Please provide the following information -->

**Description**
What does this pull request change or fix? Provide a brief description.

**Type of change**
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update

**How Has This Been Tested?**
Describe the tests that you ran to verify your changes.

**Checklist**
- [ ] I have performed a self-review of my own code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have updated documentation as needed
```

---

## CODE_OF_CONDUCT.md

```markdown
# Contributor Covenant Code of Conduct

## Our Pledge
We as members, contributors, and leaders pledge to make participation in our community a harassment-free experience.

## Our Standards
Examples of behavior that contributes to a positive environment for our community include:
- Using welcoming and inclusive language
- Being respectful of differing viewpoints and experiences


## Enforcement
Instances of abusive, harassing, or otherwise unacceptable behavior may be reported to the project maintainers.
```

---

## CONTRIBUTING.md

```markdown
# Contributing to Beluga-Dragon Delivery System

Thank you for considering contributing! Please follow these steps:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a Pull Request.

Please adhere to the Code of Conduct in all interactions.
```

---

## LICENSE

```text
MIT License

Copyright (c) 2025 Your Name

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction...
```

---

## .gitignore

```gitignore
# Python
__pycache__/
*.pyc
.env/

# Data
data/*.csv

# IDE
.vscode/
```

---

## README.md

```markdown
# Beluga-Dragon Delivery System

[![CI](https://github.com/username/beluga-dragon-delivery-system/actions/workflows/ci.yml/badge.svg)](https://github.com/username/beluga-dragon-delivery-system/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python Version](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)

A **hybrid helium airship** ("Beluga") combined with autonomous **dragon drones** for end-to-end cargo delivery.

## Table of Contents
- [Features](#features)
- [Architecture](#architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Features
- Heavy-lift cargo transport via helium airship
- VTOL drone deployment for last-mile delivery
- Automated cargo transfer system
- Simulation tools for buoyancy and lift calculations

## Architecture
![Architecture Diagram](docs/architecture_diagram.png)

## Installation
```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

## Usage
1. Run buoyancy simulation:
   ```bash
   python simulation/buoyancy_simulation.py
   ```
2. Start mission control:
   ```bash
   python src/control_center.py
   ```

## Contributing
See [CONTRIBUTING.md](.github/CONTRIBUTING.md) and [CODE_OF_CONDUCT.md](.github/CODE_OF_CONDUCT.md).

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
```

---

## requirements.txt

```text
numpy>=1.21
pandas>=1.3
matplotlib>=3.4
scipy>=1.7
```

---

## docs/design.md

*(Design document unchanged.)*

---

## data/gas_cells.csv

*(Sample data unchanged.)*

---

## src/mother_ship.py

*(Module code unchanged.)*

---

## src/dragon_drone.py

*(Module code unchanged.)*

---

## src/transfer_system.py

*(Module code unchanged.)*

---

## src/control_center.py

*(Module code unchanged.)*

---

## simulation/buoyancy_simulation.py

*(Simulation code unchanged.)*


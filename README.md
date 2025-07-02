# CivilCRM.ai Scrapers

This repository contains multiple scraper scripts organized into separate folders. Each folder contains Python scripts used to collect or process data.

---

## Setup Instructions

### 1. Install Pipenv

If you don’t have Pipenv installed, install it using:

```bash
pip install pipenv
```

Pipenv is used to create and manage a virtual environment for this project, ensuring consistent package versions and dependencies.

2. **Create the Environment and Install Dependencies**
From the project root folder (where the Pipfile is located), run:

```bash
pipenv install
```

This command creates a virtual environment and installs all required packages specified in the Pipfile.

3. **Running the Scraper Scripts**
To run any Python script inside the pipenv environment:

Activate the pipenv shell:

```bash
pipenv shell
```

Run the Python script by specifying its relative path, for example:

```bash
python3 folder1/script1.py
python3 folder3/another_script.py
```

Replace the path with the actual location of the script you want to run.

Exit the pipenv shell when finished:

```bash
exit
```

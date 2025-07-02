# CivilCRM.ai Scrapers

This repository contains multiple scrapers to extract campaign finance and expenditure data from different US state government websites. Each scraper is organized by state and follows a consistent class-based structure using a common `BaseScraper`.

---

## 📦 Project Setup

### 1. Install Pipenv

Install `pipenv` if not already available:

```bash
pip3 install pipenv
```

2. Install Dependencies
From the project root (where the Pipfile is located):

```bash
pipenv install
```

3. Activate the Environment
Start a shell inside the virtual environment:

```bash
pipenv shell
```

ℹ️ All scrapers should be run inside this environment to ensure the correct dependencies are used.

🚀 Running Each State Scraper
🔹 AR - Arkansas
Path: scrapers/ar/scraper.py

```bash
pipenv run python -m scrapers.ar.scraper
```

🔹 AZ - Arizona
This state has two separate scrapers:

1. Contributions Scraper
Path: scrapers/az/cont_scraper.py

```bash
pipenv run python -m scrapers.az.contscraper
```

2. Expenditures Scraper
Path: scrapers/az/exp_scraper.py

```bash
pipenv run python -m scrapers.az.expscraper
```

🔹 UT - Utah
Path: scrapers/ut/scraper.py

```bash
pipenv run python -m scrapers.ut.scraper
```

🔹 VA - Virginia
Path: scrapers/va/scraper.py

```bash
pipenv run python -m scrapers.va.scraper
```

🔹 NJ - New Jersey
Path: scrapers/nj/scraper.py

```bash
pipenv run python -m scrapers.nj.scraper
```


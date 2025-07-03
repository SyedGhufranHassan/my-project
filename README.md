# CivilCRM.ai Scrapers

This repository contains multiple web scrapers designed to extract campaign finance data from various US state government websites. Each scraper is organized by state and built using a consistent class-based approach, inheriting from a shared `BaseScraper` to promote code reuse and maintainability.

---

## 📦 Project Setup

### 1. Install Pipenv

If you don’t have `pipenv` installed yet, you can install it using:

```bash
pip3 install pipenv
```

2. Install Dependencies

From the project root directory (where the Pipfile resides), install all required dependencies:

```bash
pipenv install
```

3. Activate the Virtual Environment

To enter the pipenv-managed virtual environment shell, run:

```bash
pipenv shell
```

Note:

All scraper scripts should be executed within this environment to ensure consistent dependency management and avoid version conflicts.

---

### 🛠️ BaseScraper Overview:

The BaseScraper is a foundational class that all state-specific scrapers inherit from. It provides common utilities such as:

- Session management (e.g., handling persistent headers, cookies)

- Request retries and error handling

- Logging and progress reporting

- File and folder setup for outputs

- Common helper methods to reduce code duplication

By centralizing these common functions, the BaseScraper ensures that each scraper can focus solely on state-specific scraping logic, improving maintainability and extensibility.

---

### 🚀 Running Each State Scraper

Below is the list of available state scrapers along with their paths and how to run them.

#### Arkansas (AR)

**Purpose:** Scrapes campaign finance and expenditure data for Arkansas.

**Script path:** scrapers/ar/scraper.py

Run command:

```bash
pipenv run python -m scrapers.ar.scraper
``` 

#### Arizona (AZ)

Arizona has two distinct scrapers for different data types:

**Contributions Scraper**

**Path:** scrapers/az/cont_scraper.py

Run command:

```bash
pipenv run python -m scrapers.az.contscraper
```

**Expenditures Scraper**

**Path:** scrapers/az/exp_scraper.py

Run command:

```bash
pipenv run python -m scrapers.az.expscraper
```

#### Utah (UT)

**Purpose:** Scrapes data related to Utah’s campaign finance.

**Script path:** scrapers/ut/scraper.py

Run command:

```bash
pipenv run python -m scrapers.ut.scraper
```

#### Virginia (VA)

**Purpose:** Scrapes Virginia’s campaign finance and expenditure data.

**Script path:** scrapers/va/scraper.py

Run command:

```bash
pipenv run python -m scrapers.va.scraper
```

#### New Jersey (NJ)

**Purpose:** Extracts detailed campaign finance records for New Jersey.

**Script path:** scrapers/nj/scraper.py

Run command:

```bash
pipenv run python -m scrapers.nj.scraper
```
---

### Additional Notes

- All scrapers save their outputs in state-specific output directories within their respective folders (e.g., scrapers/nj/output/ for New Jersey).
- The BaseScraper class contains common utilities and methods shared by all scrapers, enabling easier maintenance and feature extension.
- For any scraper that involves handling large datasets or paginated API responses, the scripts automatically manage pagination and retries on transient errors.
- Please ensure you have a stable internet connection when running scrapers to avoid HTTP errors.


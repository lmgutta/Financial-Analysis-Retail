# Financial Reporting & Process Automation System

**Built with Google Sheets & Google Apps Script**

> **What if a spreadsheet could behave more like an operational reporting system?**
>
> I built this system to turn raw POS exports from a multi-store retail business into **automated financial and operational intelligence** — without an ERP.
>
> It combines **self-service reporting, exception management, historical performance analysis, and forward-looking store projections** in one automated workflow.
>
> **Track what happened. Identify where performance is breaking down. Compare it with historical performance. See where it may be heading next.**
>
> **[Try the live system →](https://docs.google.com/spreadsheets/d/1YYBE2KYu3kiaScHik_HveYuyL2x-1oX_r-fDtDRhDWw/edit?usp=sharing)**
>
> *All data in this repository is synthetic. No real customer, transaction, or company data is included.*

---

## At a Glance

| Capability | What it does |
|---|---|
| **Automated Reporting** | Converts raw POS exports into management-ready reporting |
| **Exception Management** | Identifies and ranks overdue customers by store |
| **12-Month Rolling Views** | Keeps operational trends focused on the most recent year |
| **Historical Comparison** | Compares current performance against up to three years of history |
| **Performance Projections** | Projects next-month and rolling 3-month store performance |
| **Self-Service Analysis** | Lets managers filter by store, month, year and payment type |
| **Process Automation** | Uses Google Apps Script to automate reporting and chart generation |

---

## The Business Problem

The underlying business operated across multiple retail locations using a basic POS system, but lacked a central financial reporting solution.

Operational managers could access transaction exports, but meaningful analysis required manually combining and interpreting raw data:

- Which customers had overdue balances?
- Which stores were driving revenue growth or decline?
- How much cash had actually been collected?
- Which payment methods were being used?
- How did current performance compare with previous years?
- What was likely to happen over the coming months?

This created a **reporting bottleneck**: data was available, but converting it into useful management information required significant manual effort.

The objective was therefore not simply to build a dashboard, but to create a **repeatable reporting process that managers could operate themselves.**

---

## The Solution

The system converts raw POS transaction data into a structured reporting workflow:

**POS data → Data processing → Validation → Filtering → Analysis → Exception identification → Management reporting**

The system is designed around six core reporting modules.

| Module | Purpose |
|---|---|
| **Financial Overview** | Revenue, cash collected, outstanding balances and collection rate |
| **Overdue Parties** | Store-level identification and ranking of overdue customers |
| **Store Trend Overview** | Monthly performance, historical comparison and forward-looking projections |
| **Store Performance** | Store-level revenue and payment collection performance |
| **Cash Flow & Banking** | Cash, bank, card and outstanding balances |
| **Payment Type Overview** | Changes in customer payment behaviour over time |

Every module can be filtered by **store, month, year and payment type**, allowing managers to move from a high-level view into the underlying operational detail.

---

## Key Capabilities

### Rolling 12-Month Reporting

Month-based reporting automatically uses the **most recent 12 months** rather than allowing historical data to accumulate indefinitely.

This keeps reporting readable as the business grows and prevents charts from becoming increasingly difficult to interpret.

### Historical Year-over-Year Comparison

Monthly performance can be viewed alongside historical annual totals for up to **three years**, allowing managers to compare current performance against previous periods.

Historical totals are separated visually from monthly figures to maintain readability despite the difference in scale.

### Store Performance Projections

The **Store Trend Overview** introduces forward-looking analysis using each store's trailing 12 months of actual performance.

It provides:

- **Next Month projection**
- **Rolling 3-Month average projection**

Projected values are explicitly labelled and visually separated from historical actuals.

This extends the system from purely retrospective reporting toward **forward-looking operational decision support**.

### Store-Level Exception Analysis

The Overdue Parties module was redesigned from a single global list into **store-specific top-15 overdue customer lists**.

This makes the information actionable for managers responsible for individual locations rather than presenting them with an aggregated company-wide list.

### Automated Reporting

Google Apps Script automates dashboard refreshes and chart generation.

The system is designed so that adding stores, months and transactions does not require manually rebuilding formulas or charts.

### Data-Quality Controls

The reporting logic uses transaction dates rather than text-based month labels to maintain chronological ordering.

This prevents issues such as:

> April → August → December → February → January

and ensures that month-based reporting follows the actual transaction timeline.

---

## Why This Matters Operationally

The value of the system is not the dashboard itself. It is the **workflow it replaces**.

### Before

**POS exports → Manual cross-referencing → Spreadsheet manipulation → Analysis → Management request**

### After

**POS export → Automated processing → Filter → Analyse → Identify exception → Take action**

This provides managers with:

- **Faster reporting** — information is available without waiting for manually prepared reports.
- **Self-service analysis** — managers can investigate stores, periods and payment types independently.
- **Exception visibility** — overdue balances and performance issues are surfaced directly.
- **Historical context** — current performance can be evaluated against previous periods.
- **Forward visibility** — store-level projections provide an indication of expected near-term performance.
- **Repeatability** — the reporting process does not depend on manually rebuilding spreadsheets each reporting cycle.

---

## How It Works

### 1. Load the Data

Paste the POS transaction export into the data input area.

### 2. Process the Data

The system processes the transaction data and prepares it for reporting.

### 3. Apply Filters

Select the relevant:

- Store
- Month
- Year
- Payment type

### 4. Refresh the Dashboard

Google Apps Script rebuilds the relevant charts and reporting views.

### 5. Analyse

Move from summary metrics into store-level, customer-level and time-based detail.

### 6. Identify Exceptions

Use overdue balances, performance trends and projections to identify areas requiring management attention.

---

## Try It Yourself

**All data in the published version is synthetic.**

1. **[Open the live template →](https://docs.google.com/spreadsheets/d/1YYBE2KYu3kiaScHik_HveYuyL2x-1oX_r-fDtDRhDWw/edit?usp=sharing)**
2. Select **File → Make a Copy**
3. Open **Data Generator**
4. Click **Generate Data**
5. Open **Dashboard**
6. Set your desired filters
7. Click **Refresh All Charts**
8. Drill into a store, month or payment type

The generator allows different scenarios to be created without exposing any real business data.

---

## Screenshots

<img width="2188" height="1092" alt="image" src="https://github.com/user-attachments/assets/d25f9592-be7e-44e8-8890-11a28d17ab2e" />
<img width="2208" height="1084" alt="image" src="https://github.com/user-attachments/assets/a270f85a-aa89-44e0-b37f-b6316fa38ea2" />
<img width="2362" height="1104" alt="image" src="https://github.com/user-attachments/assets/34c92069-2006-441a-a0ba-45e2c18266a8" />
<img width="1402" height="808" alt="image" src="https://github.com/user-attachments/assets/2029bffd-4fc3-4617-8624-a73d8cf48762" />
<img width="1924" height="716" alt="image" src="https://github.com/user-attachments/assets/2c133bc5-b242-42a1-9711-1ef24ac2e825" />
<img width="1528" height="912" alt="image" src="https://github.com/user-attachments/assets/a4d0501e-7e80-4980-9a38-2a4de5a1e6f9" />


---

## Design Principles

### Self-Service Over Centralised Reporting

The system was designed for operational managers who need answers without submitting a reporting request and waiting for someone else to prepare the analysis.

### Automation Over Manual Maintenance

Traditional spreadsheets often become increasingly fragile as new stores, columns and reporting periods are added.

The system therefore uses:

- Column-name-based references rather than positional references
- Automated chart rebuilding
- Dynamic reporting periods
- Automated synthetic-data generation

### Operational Usefulness Over Dashboard Complexity

The objective was not to maximise the number of charts.

Each module exists to answer a specific operational question:

> **What happened? Where did it happen? Why does it matter? What should the manager look at next?**

### Bridge to Enterprise Systems

The system follows a **"bridge tool" philosophy**.

A spreadsheet-based solution can provide useful operational visibility while an organisation lacks the budget, infrastructure or implementation timeline for a full ERP solution.

The structure is deliberately designed around defined data inputs, processing logic, reporting outputs and management workflows, making it possible to evolve toward a more integrated enterprise system rather than repeatedly rebuilding reporting from scratch.

---

## Full Write-Up

Built independently after identifying a financial and operational reporting gap during an operations role at a multi-store retail business.

Traditional spreadsheets are fragile — a deleted row, an added column, or a new store opening would normally break formulas and charts, requiring hours of manual fixing.

This tool was engineered to reduce that maintenance burden: formulas reference columns by name rather than position, reporting periods are dynamically determined, and charts are rebuilt through automation.

### Process Flow

**POS export → Data processing → Validation → Filters → Automated reporting → Management analysis**

### How It Works for the User

1. **Paste the data** — drop the raw POS export into the data tab.
2. **Set the filters** — select store, month, year or payment type.
3. **Refresh** — the reporting views and charts rebuild automatically.
4. **Analyse** — drill from summary metrics into store and transaction-level information.
5. **Act** — use exceptions, trends and projections to identify areas requiring attention.

---

## Limitations of the Demo

This published version is deliberately modified to demonstrate the system's capabilities using synthetic data.

### Synthetic Data

No real customer, transaction or company data is included in this repository.

### Generate-Only Workflow

The published version generates a fresh synthetic dataset rather than reproducing the incremental POS paste-and-append workflow used in the original environment.

### Spreadsheet Scalability

The system is designed to handle growth without routine manual rework, but it remains a spreadsheet-based solution.

It is **not intended to replace a fully integrated ERP or financial management platform at scale**.

The purpose is to demonstrate how a structured, automated reporting process can provide value before — or alongside — a larger enterprise-system implementation.

---

## The Bigger Picture

The project follows a **"bridge tool" philosophy**:

> Provide operational managers with a useful analytical system today, without waiting for an ERP implementation, while keeping the underlying data structure and reporting logic organised enough to evolve into a more integrated solution later.

The broader objective is to demonstrate how **process design, automation, data visibility and operational analytics** can be combined to solve practical business problems.

---

## Technology

- **Google Sheets**
- **Google Apps Script**
- Spreadsheet-based data modelling
- Automated reporting
- Dynamic chart generation
- Synthetic data generation

**AI-assisted development** was used during implementation.

---

## Project Context

The system was developed independently after identifying a financial and operational reporting gap during an operations role at a multi-store retail business.

The published version has been reconstructed and modified using synthetic data to demonstrate the underlying **process design, reporting logic, automation and analytical capabilities** without exposing proprietary information.

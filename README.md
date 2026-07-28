# Automated Financial Reporting System (Built in Google Sheets)

**TL;DR:** A self-service financial dashboard built entirely in Google Sheets — gives 
operational managers instant, filterable visibility into revenue, overdue receivables, 
store performance, and cash flow, without needing a dedicated ERP system. Built to solve 
a real reporting gap at a multi-store retail business; automated with Google Apps Script 
so it scales as the business grows. Try it yourself with the synthetic data generator — 
**[Open the live template →]((https://docs.google.com/spreadsheets/d/1YYBE2KYu3kiaScHik_HveYuyL2x-1oX_r-fDtDRhDWw/edit?usp=sharing))**

*(Full write-up, screenshots, and honest limitations below ↓)*

---

## The Problem

The business operates across multiple retail locations, processing transactions through a 
basic point-of-sale (POS) system. There was no central financial software, so any real 
analysis — figuring out which customers were falling behind on payments, whether a store's 
revenue was trending up or down, how payment collection was actually happening — required 
manually cross-referencing raw data exports, often taking days.

## The Solution

Six focused modules, each filterable by store, month, year, and payment type:

| Module | What It Answers |
|---|---|
| **Financial Overview** | Total revenue, cash collected, outstanding balance, collection rate |
| **Overdue Parties (AR)** | Which customers owe money, ranked by amount, automatically |
| **Store Trend Overview** | Is this location's revenue trending up or down over time |
| **Store Performance** | How is each store actually collecting payment |
| **Cash Flow & Banking** | Where the money physically landed — cash, bank, card, or still outstanding |
| **Payment Type Overview** | How customer payment preferences are shifting over time |

Built for people who need to dig in past a summary number — a manager who sees an overdue 
total and needs to know exactly which accounts and stores are driving it, in seconds, not 
after requesting a report and waiting.

## Why This Matters Operationally

- **Faster collections** — overdue accounts surfaced and ranked automatically
- **Reliable cycle-end checks** — verify where balances *should* be at the end of any period
- **Self-serve reporting** — no more request-and-wait cycles for internal numbers
- **Scales without breaking\*** — new stores, months, and transactions handled automatically

\* *see Limitations below — this comes with a real ceiling*

## Try It Yourself

**Note:** All data here is synthetically generated. No real business or customer data is 
used anywhere in this repository.

1. **[Open the live template →]((https://docs.google.com/spreadsheets/d/1YYBE2KYu3kiaScHik_HveYuyL2x-1oX_r-fDtDRhDWw/edit?usp=sharing))**, then **File → Make a Copy**
2. Go to **Data Generator** → click **Generate Data** (or leave fields blank for a random scenario)
3. Go to **Dashboard**, set filters, click **Refresh All Charts**
4. Drill into one store, one month, one payment type — watch everything narrow instantly

## Screenshots

<img width="1214" height="768" alt="image" src="https://github.com/user-attachments/assets/cac7799c-3c35-43b8-a4c8-bd6005d5b047" />
<img width="1212" height="772" alt="image" src="https://github.com/user-attachments/assets/d19123ed-dd37-467f-a81e-bb9be6febdbd" />
<img width="1208" height="748" alt="image" src="https://github.com/user-attachments/assets/87a39598-21ae-4e5f-9f87-80bb78b9083b" />
<img width="1208" height="756" alt="image" src="https://github.com/user-attachments/assets/00706cf1-f2b6-4b1f-a9b4-87007a926259" />
<img width="2404" height="654" alt="image" src="https://github.com/user-attachments/assets/550c469d-a7ac-4454-88e8-485f93cb7fcc" />
<img width="1204" height="752" alt="image" src="https://github.com/user-attachments/assets/9d000425-b659-4ae3-9c4f-40d9ca7d84b0" />

---

## Full Write-Up

Built independently while identifying a reporting gap during an operations role at a 
multi-store retail business.

Traditional spreadsheets are fragile — a deleted row, an added column, or a new store 
opening would normally break formulas and charts, requiring hours of manual fixing. This 
tool was engineered to avoid that: every formula reads columns by name rather than position, 
and every chart rebuilds itself on demand via automation, so growth doesn't require rework.

### How It Works (For the User)

1. **Paste the data** — drop the raw POS export into the data tab
2. **Set the filters** — store, month, year, or payment type
3. **Click Refresh** — everything rebuilds instantly

### Limitations of This Demo

This published version is deliberately modified to showcase capabilities using synthetic 
data, with a few honest caveats:

- **Unrealistic extremes are possible.** Generating an extreme scenario (e.g., 100 stores, 
  10 years of history) could produce an Overdue Parties list in the thousands — something 
  that wouldn't happen in a real business, where overdue accounts would be caught and 
  addressed long before reaching that scale.
- **Generate-only, not append.** This demo only generates a fresh synthetic dataset from 
  scratch. The original real-world version supports incrementally *adding* new transactions 
  over time via a POS paste-and-append workflow — not included here, since it's unnecessary 
  for a self-contained demo.
- **"Scales without breaking" has a ceiling.** This is genuinely built to handle growth 
  without manual rework, but it's still a spreadsheet-based system — not a substitute for a 
  fully connected ERP platform. It's a bridge, not a permanent replacement; any organization 
  using something like this will eventually need real ERP infrastructure.

### The Bigger Picture

Built with a "bridge tool" philosophy: give operational managers a real analytical tool 
*today*, without waiting on ERP budget or implementation timelines, while keeping the 
structure clean enough to migrate into a full ERP system later without starting over.

---

Built using Google Sheets, Google Apps Script, and AI-assisted development.

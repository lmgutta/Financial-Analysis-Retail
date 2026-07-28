# Automated Financial Reporting System (Built in Google Sheets)

A self-service financial analysis tool built entirely in Google Sheets — designed to give 
operational managers the ability to dig into revenue, receivables, and cash flow at a level 
of detail that used to take days or weeks to assemble manually, without needing a dedicated 
ERP system.

Built independently while identifying a reporting gap during an operations role at a 
multi-store retail business.

## The Problem

The business operates across multiple retail locations, processing transactions through a 
basic point-of-sale (POS) system. There was no central financial software, so any real 
analysis — figuring out which customers were falling behind on payments, whether a store's 
revenue was trending up or down, how payment collection was actually happening — required 
manually cross-referencing raw data exports.

This wasn't just slow. It meant operational managers were making decisions on stale, incomplete 
information, and had no reliable way to check "where should our balances actually be at the 
end of this cycle" without days of manual reconciliation first.

## The Solution

A six-module financial analysis system, built so a manager can filter down to exactly the 
slice of the business they need to investigate — a single store, a specific month, one 
payment type, or any combination — and get an immediate, reliable answer:

- **Financial Overview** — the starting point for any investigation: total revenue, cash 
  collected, outstanding balances, and collection rate, filtered to whatever period or store 
  a manager is reviewing
- **Overdue Parties (Accounts Receivable)** — automatically ranks every customer with an 
  outstanding balance, so collections effort goes to the highest-impact accounts first, 
  instead of manually scanning transaction lists
- **Store Trend Overview** — lets a manager check whether a location's revenue is on track, 
  and compare that against prior months at a glance
- **Store Performance** — shows exactly how each store is collecting payment, which matters 
  for both fraud/risk monitoring and reconciliation effort
- **Cash Flow & Banking Distribution** — answers "where did the money actually go this 
  cycle" — cash in hand vs. bank vs. card settlements vs. still-outstanding credit — the 
  exact reconciliation question finance teams ask at cycle-end
- **Payment Type Overview** — surfaces shifts in how customers are choosing to pay, useful 
  for spotting risk trends (e.g., rising reliance on credit) before they become a problem

This is built for people who need to **dig in further than a summary number** — a manager 
who sees an overdue total and needs to know exactly which accounts, which stores, which 
months are driving it, and pull that detail themselves in seconds rather than requesting 
it from someone else and waiting.

## Why This Matters Operationally

- **Faster collections** — overdue accounts are surfaced and ranked automatically, so 
  follow-up effort is prioritized correctly instead of discovered late
- **Reliable cycle-end checks** — managers can verify where balances *should* be at the end 
  of any reporting cycle, rather than reconciling manually after the fact
- **Self-serve reporting** — internal reports that used to require a request-and-wait cycle 
  (ask someone to pull the numbers, wait, get a static answer) can now be generated directly 
  by whoever needs them, filtered exactly to their question
- **Scales without breaking\*** — new stores, new months, and growing transaction volume are 
  handled automatically; nothing needs to be manually rebuilt as the business grows

  \* *with a real limit — see "Limitations of This Demo" below*

## How It Works (For the User)

Using the system requires zero technical skill:

1. **Paste the data** — drop the raw transaction export from the POS system into the data tab
2. **Set the filters** — choose which stores, months, years, or payment types to investigate
3. **Click Refresh** — the relevant charts and summaries rebuild instantly

## Try It Yourself

**Note:** All data in this demo is synthetically generated using the built-in Data Generator. 
No real business or customer data is used or exposed anywhere in this repository.

**[Open the live template →](https://docs.google.com/spreadsheets/d/1YYBE2KYu3kiaScHik_HveYuyL2x-1oX_r-fDtDRhDWw/edit?usp=sharing)**

1. Click **File → Make a Copy** to get your own editable version
2. Go to the **Data Generator** sheet and click **Generate Data** — this builds a realistic, 
   randomized business history (number of stores, operating history, and transaction volume 
   are all configurable, or left random for a surprise scenario)
3. Go to **Dashboard**, set any filters you like, and click **Refresh All Charts**
4. Try drilling in — pick one store, one month, one payment type — and see how every view 
   narrows down to exactly that slice

## Limitations of This Demo

This published version is deliberately modified to showcase the tool's capabilities using 
synthetic data, and comes with a few honest caveats:

- **Unrealistic extremes are possible.** If you generate an extreme scenario — say, 100 
  stores and 10 years of history — the Overdue Parties list could balloon into the thousands, 
  something that wouldn't realistically happen in a real business (real operations would 
  catch and address overdue accounts long before they accumulated at that scale). The 
  generator prioritizes flexibility for demonstration purposes over realistic business behavior 
  at extreme settings.
- **Generate-only, not append.** This demo version only supports *generating* a fresh synthetic 
  dataset from scratch. The original, real-world version of this tool supports incrementally 
  *adding* new transaction data over time (via a POS paste-and-append workflow) — that 
  functionality isn't included here, since it's not needed for a self-contained demo.
- **"Scales without breaking" has a ceiling.** This tool is genuinely built to handle growth — 
  new stores, more months, more transactions — without manual rework. But it is still a 
  spreadsheet-based system, and it is not a substitute for a proper, fully connected ERP 
  platform. It's designed as a *bridge*, not a permanent replacement — every organization 
  using something like this will eventually outgrow it and need real ERP infrastructure.

## The Bigger Picture

This was built with a "bridge tool" philosophy: give operational managers a real analytical 
tool *today*, without waiting on ERP budget or implementation timelines, while keeping the 
underlying structure clean enough to migrate into a full ERP system later without starting over.

## Screenshots

*(Add screenshots of the filter panel, the Overdue Parties ranking, and a drill-down example here)*

---

Built using Google Sheets, Google Apps Script, and AI-assisted development.

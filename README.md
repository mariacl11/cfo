# AI CFO Skills

**Turn ChatGPT or Claude into your own CFO (Chief Financial Officer).**

AI CFO Skills is an open-source library of practical finance skills for founders, business owners, finance teams, consultants, and analysts.

Give it your financial data and ask normal business questions such as:

- Why is our cash falling even though revenue is growing?
- How many months of runway do we have?
- Can we afford to hire 15 more people?
- Which customers are actually profitable?
- Why are margins getting worse?
- How much should we raise?
- Prepare a board finance pack.
- Analyse this P&L and tell me what matters.
- Find unusual transactions in this ledger.
- Compare three pricing options.
- Is this expansion financially sensible?

The AI CFO decides which finance skills are needed, runs the analysis, checks the numbers, and gives you a decision-useful answer.

---

## What it can do

AI CFO Skills currently includes **35 specialist finance skills** across six areas.

### Accounting & Reporting

Analyse financial statements and understand what is happening inside the business.

- P&L analysis
- Balance sheet analysis
- Cash flow analysis
- Full financial statement analysis
- Monthly MIS
- Month-end close review
- Management commentary

### Planning & Forecasting

Plan ahead and understand how changes in the business affect future performance.

- Annual budgeting
- Rolling forecasts
- Budget vs actual analysis
- Revenue forecasting
- Expense forecasting
- Scenario analysis
- Sensitivity analysis

### Cash & Working Capital

Understand where cash is going and whether the business has enough liquidity.

- Cash runway
- Cash forecasting
- Receivables ageing
- Payables analysis
- Working capital analysis

### Business Finance

Use financial data to make day-to-day business decisions.

- Unit economics
- Customer profitability
- Product profitability
- Pricing analysis
- Breakeven analysis
- Business case analysis

### Corporate Finance

Support larger financial and strategic decisions.

- Company valuation
- Investment appraisal
- Debt analysis
- Fundraising analysis
- Financial due diligence

### CFO Office

Support financial controls, risk management, audit preparation, and board reporting.

- Financial anomaly review
- Audit readiness
- Internal controls review
- Board finance pack
- CFO decision memo

---

## Getting started

First, download this repository and unzip it.

### ChatGPT or Codex

1. Open the ChatGPT desktop app and choose **Add project**.
2. Select the folder you just downloaded.
3. Restart the ChatGPT desktop app.
4. Open **Plugins**, choose **AI CFO Skills**, and install **AI CFO**.
5. Start a new chat or Codex task.

If **AI CFO Skills** does not appear in Plugins, open a terminal in the downloaded folder and run:

```bash
codex plugin marketplace add .
```

Then restart the app and repeat step 4.

Local plugins require the ChatGPT desktop app. After the plugin is published in the public plugin directory, the same plugin can also be installed from ChatGPT on the web or mobile.

### Claude Code

1. Open a terminal in the downloaded folder.
2. Add the marketplace and install the plugin:

   ```bash
   claude plugin marketplace add .
   claude plugin install ai-cfo@ai-cfo-skills
   ```

3. Start a new Claude Code session. Claude can select AI CFO automatically, or you can run `/ai-cfo:ai-cfo`.

### Ask your question

Upload or point the chat to your financial files, then ask your business question.

That is all. You do not need to select a finance skill—the AI CFO chooses the relevant skills automatically.

For example:

> Analyse these financial statements. Tell me the biggest risks, why cash has fallen, and what management should do next.

---

## How it works

You do not need to choose the right finance skill yourself.

Start with a business question.

For example:

> We want to open a new office. Can we afford it?

The AI CFO may automatically use:

**Business Case Analysis → Expense Forecast → Cash Forecast → Scenario Analysis → Breakeven Analysis → CFO Decision Memo**

Or upload your financial statements and ask:

> Analyse the company.

The AI CFO can combine:

**Financial Statement Analysis → Working Capital Analysis → Cash Runway → Financial Anomaly Review**

The individual skills work together as one AI CFO.

---

## What you can give it

You can work with common finance files such as:

- Excel files
- CSV exports
- P&L statements
- Balance sheets
- Cash flow statements
- Bank transaction exports
- General ledgers
- Accounts receivable reports
- Accounts payable reports
- Budgets and forecasts
- Cap tables
- Board finance packs
- Management reports

You can also paste financial data directly into the chat.

---

## What the output looks like

The skills are designed to produce useful CFO-level output rather than generic commentary.

A typical analysis includes:

1. **Executive Summary**
2. **Key Numbers**
3. **What changed**
4. **Why it changed**
5. **Cash impact**
6. **Risks and red flags**
7. **Scenarios**, where relevant
8. **Recommended actions**
9. **Assumptions and missing data**

Important figures are kept separate as:

- **Reported**: taken directly from your data
- **Calculated**: derived from your data
- **Assumption**: used for modelling or scenarios
- **AI interpretation**: the AI CFO's analysis of the numbers

This reduces the risk of assumptions being presented as facts.

---

## Example

Suppose revenue has increased from ₹1.2 crore to ₹1.6 crore, but cash in the bank keeps falling.

Instead of simply saying that cash flow is weak, the AI CFO can investigate:

- whether gross margins have declined
- whether customers are taking longer to pay
- whether inventory has increased
- whether suppliers are being paid faster
- whether capex has increased
- whether debt repayments are consuming cash
- whether growth itself is creating a working-capital requirement

It can then show which factors are actually responsible and what management can do about them.

---

## Who this is for

AI CFO Skills can be useful for:

- founders and startup teams
- SMEs and business owners
- CFOs and finance teams
- accountants and finance consultants
- investors and analysts
- students learning financial analysis
- developers building finance agents

You do not need to have a full ERP integration or buy an expensive AI finance platform to start using it.

---

## Try these prompts

### Understand the business

> Analyse these financial statements like a CFO. Tell me the five things management should care about most.

### Cash

> Analyse our cash position and tell me how many months of runway we have.

### Hiring

> We want to hire 10 salespeople. Model the financial impact and tell me what revenue they need to generate for this to make sense.

### Pricing

> We are considering increasing prices by 12%. Analyse the effect on margin and show what decline in volume we could absorb.

### Fundraising

> Based on this forecast, how much money should we raise if we want 24 months of runway?

### Board meeting

> Prepare a board finance pack using these financial statements, budget, and forecast.

### Collections

> Analyse this receivables ageing report and tell me which customers we should chase first.

### Expansion

> We are considering opening a new office. Build the financial case and show base, upside, and downside scenarios.

### Due diligence

> Review these financials as if we were considering acquiring the company. Identify financial red flags and follow-up questions.

---

## Built for financial discipline

AI CFO Skills follows a few simple rules:

- it should never invent a number
- calculations should be traceable
- assumptions should be visible
- actuals, budgets, and forecasts should not be mixed
- profit and cash should be treated separately
- inconsistent data should be flagged
- material risks should be prioritised
- conclusions should be linked to the underlying numbers

The aim is to make AI financial work more reliable and useful for actual business decisions.

---

## Open source

AI CFO Skills is open source under the MIT License.

You can:

- use it
- modify it
- add your own finance skills
- adapt it for your company
- build products on top of it
- contribute improvements back to the project

---

## What's inside

The repository contains:

- **1 AI CFO orchestrator**
- **35 specialist CFO skills**
- finance calculation standards
- board and CFO report templates
- sample financial datasets
- sample prompts
- example outputs
- ChatGPT, Codex, and Claude Code plugin manifests
- Codex and Claude usage guides

For developers and contributors, the technical documentation is in `plugins/ai-cfo/skills/ai-cfo/docs`.

---

## Disclaimer

AI CFO Skills provides financial analysis and decision support. It does not replace professional accounting, audit, tax, investment, or other regulated advice where professional review or sign-off is required.

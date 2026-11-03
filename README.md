# Garcia Family Finance LLM Assistant

An applied AI financial assistant designed to manage household capital allocation, automate proportional expense sharing, optimize debt payoffs, and foster generational wealth for the Garcia family. 

Built with low-friction UI and plain-language bilingual support so every family member—from tech-savvy builders to elderly parents—can navigate household finances with clarity and confidence.

---

## 📌 Motivation & Mission

Managing multi-generational household finances, shared bills, and individual savings goals often comes with friction, language barriers, and confusing financial jargon. 

This project solves that by leveraging Large Language Models (LLMs) to create a high-empathy, automated system that balances fairness across shared expenses while empowering individual financial independence and long-term investing.

---

## 👥 Family Profiles & Income Ingestion

The system tracks monthly and biweekly earnings across 5 primary family members (and 1 very important honorary member):

- **Mama & Papa:** Primary household anchors (focused on clear, zero-jargon Spanish summaries).
- **Daiara, Jazlin, & Omar:** Earnings, active investments, and high-yield savings allocations.
- **Lucky 🐶:** Household security & morale executive ($0/month earnings, 100% tax-exempt, unlimited treat stipend).

---

## ⚙️ Core Architecture & Financial Modules

### 1. ⚖️ Proportional Shared Expense Allocation
Rather than splitting household bills equally, the LLM calculates a dynamic **Family Income Percentage (100% total)**. Shared fixed expenses are split proportionally based on total monthly earnings so that everyone contributes fairly according to their income.

**Shared Household Expenses Tracked:**
- House Mortgage
- Electricity & Water Utilities
- Mobile Phone Plans & Internet
- Cable & Family Subscriptions (Streaming, iCloud, etc.)

> *Example Logic:* If Member A earns 50% of total family income and Member B earns 10%, Member A covers 50% of the mortgage while Member B covers 10%.

---

### 2. 🏛️ Tax Reserve Engine
Calculates estimated tax obligations based on income types (W-2, 1099, contracting, freelancing):
- Automatically advises each of the 5 family members on exact amounts to set aside **per month or per biweekly paycheck** to prevent tax-season surprises.

---

### 3. 📈 Wealth Building & High-Yield Savings (HYSA)
Tailored investment allocation strategy for **Daiara, Jazlin, and Omar**:
- Analyzes leftover net income to recommend customized monthly targets for Index Funds, HYSAs, and long-term investment accounts.
- Educates family members on compound growth and capital preservation.

---

### 4. 💳 Individual Debt & Loan Payoff Tracker
Dedicated personal debt module for each family member to manage:
- Credit Card Balances
- Student Loans & Personal Obligations
- **AI Recommendation Engine:** Provides personalized monthly repayment strategies (Avalanche/Snowball) telling each person exactly how much to allocate toward high-interest debt each month.

---

### 5. 🎉 Dynamic "Free Money" & Smart Savings Goals
Calculates remaining discretionary cash ("Free Money") after all mandatory bills, taxes, debt payments, and core savings are satisfied.

**Goal-Based Reallocation:**
When special events arise (Christmas, birthdays, family trips, major purchases):
- Members can set custom savings targets inside the system.
- **Strict Isolation Logic:** The LLM guarantees that event budget allocations are **never** taken from mandatory household bills or core investment reserves. Money is strictly reallocated from each member's discretionary "Free Money" bucket.

---

## 🛠️ Tech Stack & Implementation

- **Core Language:** Python 3.10+
- **LLM Orchestration:** OpenAI API / LangChain / Ollama (Local LLM fallback)
- **Data Schemas & Validation:** Pydantic & JSON Schema
- **Frontend App:** Streamlit (Clean, high-contrast, mobile-friendly interface)
- **Environment & Deployment:** Docker & Linux

---

## 📁 Repository Structure

```text
Garcia-Finance/
│
├── README.md               # Complex project architecture & family roadmap
├── requirements.txt        # Dependencies (streamlit, pydantic, openai, etc.)
├── .env.example            # Environment variables template
│
├── data/                   # Household configuration & schemas
│   ├── family_profiles.json # Members, income types, and individual profiles
│   ├── shared_bills.json    # Mortgage, utilities, and subscription lists
│   └── finance_terms_es.json# Plain-language Spanish definitions
│
├── src/                    # System logic
│   ├── agent.py            # Main LLM agent & prompt orchestration
│   ├── allocation.py       # Proportional 100% bill-split algorithm
│   ├── debt_engine.py      # Individual loan/credit card payoff logic
│   ├── goals.py            # Free-money & event goal reallocation engine
│   └── translator.py       # Bilingual/plain-language adapter
│
└── app/                    # Web UI
    └── streamlit_app.py    # Family dashboard & chat interface
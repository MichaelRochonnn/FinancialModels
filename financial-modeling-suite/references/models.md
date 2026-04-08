# Financial Modeling Suite Reference

Use this file to route the request, collect the right inputs, and decide what to build.

如果用户希望结果更像中文投行材料、PE IC memo、正式汇报文档，继续读取 `templates-zh.md` 并套用对应模板。

## Quick Router

| Model | Use when the user wants to... | Common trigger words |
| --- | --- | --- |
| DCF Valuation Model | value a business from cash flow | DCF, 折现现金流, 估值模型 |
| Three-Statement Financial Model | forecast the full financial statements | 三张表, 三表模型, three-statement |
| M&A Accretion/Dilution Analysis | judge whether a deal helps or hurts EPS | 增厚摊薄, accretion, dilution |
| LBO Model | test leveraged buyout returns | LBO, 杠杆收购, PE 回报 |
| Comparable Company Analysis | value from public peers | comps, 可比公司, trading comps |
| Precedent Transaction Analysis | value from past M&A deals | precedents, 可比交易, precedent transactions |
| IPO Valuation and Pricing Analysis | price a new listing | IPO 定价, 上市估值, pricing |
| Credit Analysis and Debt Capacity Model | size prudent leverage | debt capacity, 杠杆承载, credit memo |
| Sum-of-the-Parts Valuation | value a multi-business company by segment | SOTP, 分部估值, breakup valuation |
| Operating Model and Unit Economics | forecast growth engines and cash burn | unit economics, 经营模型, CAC, LTV |
| Sensitivity and Scenario Analysis | stress test assumptions | 敏感性分析, 情景分析, scenario |
| Investment Committee Memo | write the decision memo around a deal | 投委会 memo, investment committee, IC memo |

## 1. DCF Valuation Model

**Use when:** The user wants an intrinsic valuation based on projected cash flow.

**必填数据**
- Company name, industry, geography
- Latest revenue and profitability baseline such as EBITDA or EBIT
- Capex, D&A, tax-rate assumption, and working-capital behavior or a proxy
- Net debt or cash, and share count if per-share value is needed
- Forecast period assumptions for revenue growth and margin trend
- WACC inputs or enough data to estimate them

**可选但建议**
- Management guidance or analyst consensus
- Segment mix
- Beta, risk-free rate, ERP, pre-tax borrowing cost
- Peer exit multiples

**输出重点**
- 5-year FCF forecast
- WACC build with cost of equity and cost of debt
- Terminal value by perpetuity and exit multiple
- Sensitivity tables
- Bull, base, bear valuation range

## 2. Three-Statement Financial Model

**Use when:** The user wants an operating forecast that links income statement, balance sheet, and cash flow statement.

**必填数据**
- Company name and business description
- Latest income statement, balance sheet, and cash flow statement
- Revenue growth assumptions
- Margin assumptions or cost structure
- Capex, depreciation, working-capital assumptions
- Debt balances, interest-rate assumptions, and repayment logic

**可选但建议**
- Historical statements for 2 to 3 years
- Seasonality or segment mix
- Management guidance
- Dividend or buyback policy

**输出重点**
- 5-year three-statement forecast
- Statement link explanations
- Working-capital schedule
- Debt schedule
- Balance-sheet checks and circular-reference warnings

## 3. M&A Accretion/Dilution Analysis

**Use when:** The user wants to know whether an acquisition is EPS accretive or dilutive.

**必填数据**
- Acquirer and target names
- Purchase price or valuation range
- Deal structure: cash, stock, debt mix
- Acquirer share count and current EPS or net income baseline
- Target revenue, EBITDA, EBIT, net income, or at least earnings proxy
- Financing assumptions and interest rate
- Synergy assumptions or a statement that synergies are unknown

**可选但建议**
- Transaction fees
- Step-up amortization assumptions
- Tax rate
- Existing leverage and rating constraints

**输出重点**
- Total consideration and funding sources
- Pro forma earnings bridge
- EPS accretion or dilution
- Synergy break-even analysis
- Sensitivity by purchase price and synergy level

## 4. LBO Model

**Use when:** The user wants private-equity style returns from a leveraged acquisition.

**必填数据**
- Company name, industry, and latest EBITDA
- Entry valuation or asking price
- Debt structure by tranche and interest rate assumptions
- Sponsor equity contribution
- Management case for revenue growth and margin change
- Capex, taxes, working capital, and mandatory amortization assumptions
- Exit year and exit multiple or exit scenario

**可选但建议**
- Fees and financing costs
- Cash sweep rules
- Covenant package
- Management rollover

**输出重点**
- Sources and uses
- Debt schedule and paydown
- Cash sweep
- Exit proceeds
- Sponsor IRR and cash-on-cash multiple

## 5. Comparable Company Analysis

**Use when:** The user wants a market-based valuation from public peers.

**必填数据**
- Company name, industry, geography
- Revenue, EBITDA, EBIT, net income, or the best available financial baseline
- Suggested peers or closest competitors
- Net debt or cash
- Share count if equity value per share is needed

**可选但建议**
- Growth rates and margin profile
- Business model notes that justify premium or discount
- Consensus forward estimates

**输出重点**
- Peer set selection
- Trading multiples such as EV/Revenue, EV/EBITDA, P/E
- Percentile valuation range
- Implied valuation for the subject company
- Premium or discount justification

## 6. Precedent Transaction Analysis

**Use when:** The user wants valuation anchored to historical M&A deals.

**必填数据**
- Company or asset being valued
- Industry and geography
- Transaction screen logic or target buyer universe
- Subject-company revenue and EBITDA baseline

**可选但建议**
- Desired lookback period
- Strategic vs financial buyer focus
- Control-premium context
- Known precedent deals from the user

**输出重点**
- Deal universe and rationale
- EV/Revenue and EV/EBITDA paid
- Premium commentary when available
- Valuation percentile range
- Implied value for the subject company

## 7. IPO Valuation and Pricing Analysis

**Use when:** The user wants to frame IPO valuation, dilution, and price range.

**必填数据**
- Company name and business model
- Latest revenue, growth, margin profile, and cash burn or profitability
- Proposed primary raise size and any secondary component
- Fully diluted share count or capitalization table summary
- Comparable listed companies or recent IPO peer set

**可选但建议**
- Lock-up assumptions
- Desired float percentage
- Target post-money value
- Banker fee assumptions

**输出重点**
- Pre-money and post-money valuation
- Price-per-share range
- Dilution analysis
- Float analysis
- Comparable IPO framing and first-day pop context

## 8. Credit Analysis and Debt Capacity Model

**Use when:** The user wants to know how much debt the business can support.

**必填数据**
- Company name and industry
- Historical EBITDA, preferably 3 years
- Existing debt by tranche, interest rate, and maturity
- Forecast EBITDA or operating outlook
- Capex and working-capital needs
- Minimum interest coverage or leverage guardrails

**可选但建议**
- Covenant constraints
- Asset coverage or collateral quality
- Rating targets
- Refinance assumptions

**输出重点**
- Leverage and coverage analysis
- Debt sizing by tranche
- Pricing grid
- Covenant observations
- Refinancing and maturity-risk summary

## 9. Sum-of-the-Parts Valuation

**Use when:** The user wants to value a multi-division company by segment.

**必填数据**
- Company name and segment list
- Revenue and profitability by segment
- Corporate overhead
- Net debt or cash
- Preferred valuation method or comparable sets for key segments

**可选但建议**
- Segment growth rates
- Capex intensity by segment
- Minority interests or associates
- Hidden assets or stranded costs

**输出重点**
- Segment-by-segment valuation logic
- Corporate-cost treatment
- Net debt bridge
- Total equity value and value per share
- Breakup or restructuring angle when relevant

## 10. Operating Model and Unit Economics

**Use when:** The user wants a bottom-up operating plan rather than only a headline valuation.

**必填数据**
- Business model and revenue engine
- Current KPIs such as customers, ARPU, volume, conversion, retention, or GMV
- CAC, gross margin, and at least a rough LTV logic if applicable
- Opex baseline
- Cash balance and monthly burn if runway matters

**可选但建议**
- Cohort data
- Geography or product segmentation
- Hiring plan
- Pricing roadmap

**输出重点**
- Bottom-up revenue build
- Unit economics
- Cohort lens when data exists
- Burn and runway
- Breakeven timing

## 11. Sensitivity and Scenario Analysis

**Use when:** The user already has a base model or wants to stress test the core assumptions.

**必填数据**
- The base model or base-case assumptions
- The key variables to stress test
- The output metric to track such as EV, EPS, IRR, or runway
- Range or distribution assumptions for each stressed variable

**可选但建议**
- Correlation assumptions
- Monte Carlo setup
- Downside thresholds or covenant tripwires

**输出重点**
- One-way sensitivity
- Two-way sensitivity
- Best, base, worst scenarios
- Key risk drivers
- Breakeven and downside-protection discussion

## 12. Investment Committee Memo

**Use when:** The user wants a decision memo that wraps together the thesis, valuation, returns, and risks.

**必填数据**
- Company or deal name
- Transaction structure and size
- Business summary and financial baseline
- Valuation approach or outputs from earlier models
- Expected returns or decision goal
- Main risks already identified by the user

**可选但建议**
- Industry context
- Management background
- Buyer or exit universe
- Diligence findings

**输出重点**
- Executive summary
- Deal overview
- Company and industry analysis
- Investment thesis
- Valuation summary
- Returns, risks, and recommendation

## Intake Response Pattern

When inputs are missing, use this compact structure:

1. Start with `你要调用的是：<模型名>`.
2. Add one line on what the model answers.
3. Ask only for missing items under `必填数据`.
4. Add `可选但建议` only if those inputs would materially improve the result.
5. Offer to start with assumptions if the user wants a quick draft.

<!-- week-id: 2026-W38 -->
<!-- generated-at: 2026-10-07T10:44:09.528554+13:00 -->
# ENEL301-26S2 weekly summary

## Coverage

- Week 2026-W38: 2026-09-14T00:00:00+12:00 to 2026-09-20T23:59:00+12:00.
- Covered verified lecture summaries:
  - Lecture 15: time value of money, discounted cash flow, NPV, discounted payback, IRR, sensitivity studies, and financial communication.
  - Lecture 16: discount rates, WACC, financing sources, risk and beta, nominal versus real cash flows, and inflation in NPV analysis.

## Main concepts

- Cash flows occurring at different times must be converted into equivalent present values before fair comparison.
- Cash flow differs from accounting profit. Depreciation is not itself a cash flow, although it may affect tax through a tax shield.
- NPV is the primary project-evaluation measure covered.
  - Positive NPV: value is created at the selected discount rate.
  - Negative NPV: the project does not achieve the required return at that rate.
  - Zero NPV: the project exactly achieves the required return.
- Year 0 must be included in an NPV calculation because the initial investment generally occurs then.
- Discounted payback accounts for the time value of money; ordinary payback may not.
- IRR is the discount rate that makes NPV equal to zero. It can rank projects differently from NPV, particularly when project sizes or cash-flow patterns differ.
- Sensitivity analysis tests how changes in assumptions affect NPV or another financial measure.
- The discount rate represents the forecast cost of capital used to fund a project. It is not necessarily the interest rate on one loan or a complete measure of project risk.
- WACC combines the costs of debt and equity financing using their relative financing weights.
- Debt financing includes loans and bonds. Equity financing includes ordinary and preference shares.
- Debt costs are adjusted by the factor 1 − tax rate in the WACC treatment because of the debt tax shelter described in the lecture.
- Beta measures how sensitive a share’s return is to overall market movements.
  - β > 1: more aggressive and volatile than the market.
  - β < 1: more defensive and less volatile than the market.
- Nominal cash flows must be paired with a nominal discount rate. Real cash flows must be paired with a real discount rate.
- Engineering investment decisions require attention to cash flow, timing, required return, uncertainty, and clear communication of future funding requirements.

## Equations and worked patterns

- Future value:
  
  FV = PV(1 + R)^n

- Present value:
  
  PV = FV / (1 + R)^n

- Discount factor:
  
  DF_n = 1 / (1 + R)^n

- Present value using the discount factor:
  
  PV = FV × DF_n

- Net present value:
  
  NPV = Σ[CF_t / (1 + R)^t]

- Practical NPV pattern:
  1. Start at year 0.
  2. List each period’s cash inflows and outflows.
  3. Calculate net cash flow for each period.
  4. Determine the discount factor for each period.
  5. Discount each net cash flow.
  6. Sum the discounted cash flows.

- Compound-interest example from Lecture 15:
  
  FV = 100(1.10)^2 = $133.10

- Internal rate of return:
  
  0 = Σ[CF_t / (1 + IRR)^t]

- Discounted payback:
  
  Identify the period where cumulative discounted cash flow reaches or exceeds zero. Interpolate between periods if required.

- Total financing:
  
  V = DL + DB + EOS + EPS

- WACC structure:
  
  WACC = [DL/V]KL(1 − TC) + [DB/V]KB(1 − TC) + [EOS/V]KOS + [EPS/V]KPS

- Ordinary-share return:
  
  Return = [D + (P1 − P0)] / P0

- Cost of ordinary equity:
  
  KOS = Rf + β(Rm − Rf)

- Cost of preference shares:
  
  KPS = Dps / Pps

- Inflation-adjusted future value:
  
  Future value = Present value × (1 + G)^n

- Fisher relationship:
  
  1 + nominal rate = (1 + real rate)(1 + inflation rate)

  real rate = [(1 + nominal rate) / (1 + inflation rate)] − 1

- Worked WACC pattern from Lecture 16:
  - Financing: $6 million loans, $2 million bonds, $21 million ordinary shares, and $6 million preference shares.
  - Total financing: $35 million.
  - Stated financing weights: approximately 17.1%, 5.7%, 60%, and 17.1%.
  - Stated resulting WACC: 5.6%.
  - The complete intermediate calculation cannot be independently verified from the summary because the supplied KOS and KPS values are not included.

## Warnings and deadlines

- No deadlines or administrative requirements were identified in the two verified lecture summaries.
- Do not confuse the discount rate with the discount factor.
- Do not omit or misplace the year-0 initial investment.
- Do not treat depreciation as a cash flow by default. Follow the prescribed tax and financial model where applicable.
- Do not mix nominal cash flows with a real discount rate, or real cash flows with a nominal discount rate.
- Do not automatically substitute a particular loan’s interest rate for the company’s project discount rate. The lecture identified WACC as the main ENEL301 method.
- IRR may be misleading for irregular or lumpy cash flows and may rank projects differently from NPV.
- The Lecture 15 summary records a warning about a Microsoft IRR function, but the exact function, software version, and intended alternative are unclear. Check course instructions before applying that warning outside the lecture context.
- The displayed WACC arithmetic, supplied KOS and KPS values, and the complete annual cash-flow table for the Lecture 15 NPV example are not available in the summaries.

## Recall questions

1. Why must cash flows occurring at different times be converted to present-value terms before comparison?
2. What is the difference between a discount rate and a discount factor?
3. Why must an NPV calculation include year 0?
4. What does a positive, negative, or zero NPV indicate at the selected discount rate?
5. How does discounted payback differ from ordinary payback?
6. Why can IRR and NPV rank projects differently?
7. What financing sources are represented by DL, DB, EOS, and EPS in the WACC structure?
8. Why does the debt component of WACC include the factor 1 − TC?
9. What does β > 1 indicate about a share compared with the overall market?
10. Why must nominal cash flows be paired with a nominal WACC and real cash flows with a real WACC?

## Practice priorities

1. Build a complete NPV table beginning at year 0, including net cash flow, discount factor, discounted cash flow, and cumulative discounted cash flow.
2. Practise converting between future value, present value, and discount factor.
3. Practise identifying discounted payback from cumulative discounted cash flows.
4. Compare two projects using NPV, IRR, discounted payback, and sensitivity results rather than relying on one measure.
5. Construct a WACC calculation from debt and equity amounts, financing weights, financing costs, and the corporate tax rate.
6. Explain why WACC is not simply the interest rate on one loan.
7. Distinguish debt, ordinary equity, and preference equity by their sources of return and risk characteristics.
8. Apply the Fisher equation to distinguish nominal and real returns.
9. Prepare consistent nominal and real NPV approaches, checking that the cash flows and discount rate use the same inflation basis.
10. Run one-variable sensitivity tests for discount rate, initial investment, revenue, expenses, tax treatment, and inflation before considering combined best-case and worst-case scenarios.

## Missing or incomplete

- None.

## Source manifest

- Lecture 15 (echo-lecture-15-15): complete; summary `c1a42014a5c99d7c9f30ee151d023548bfc5895565ab8ec7b5b4996f6d4d9857`; transcript `beb2e9bcdd7d102de658c135c62dc1c04c8629245e83371e0e64b229f07f696d`; summary path `[local source path redacted]`
- Lecture 16 (echo-lecture-16-16): complete; summary `852dfccf33d2e4950d44f4d1b89e47376ce3521786cf2a37a595730e1b400bd6`; transcript `6d92747fb00ff780443bade5b92b2cf8b6ba7447e17fd33b86b091452a35f29e`; summary path `[local source path redacted]`

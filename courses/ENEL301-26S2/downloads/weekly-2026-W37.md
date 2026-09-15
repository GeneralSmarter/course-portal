<!-- week-id: 2026-W37 -->
<!-- generated-at: 2026-09-15T15:20:39.015301+12:00 -->
# ENEL301-26S2 weekly summary

## Coverage

Week 2026-W37: 2026-09-07T00:00:00+12:00 to 2026-09-13T23:59:00+12:00.

Source coverage:
- Lecture 13: life-cycle assessment, interpretation, uncertainty, allocation, and LCA modelling approaches.
- Lecture 14: economic and social assessment as components of sustainability assessment.
- Known missing or incomplete lectures: None.

## Main concepts

- LCA follows four stages: goal and scope definition, inventory development, impact assessment, and interpretation. Interpretation may require revisiting earlier stages.
- Characterisation factors convert different inventory flows into a common impact-category measure.
- LCA results are conditional on the functional unit, system boundary, inventory quality, assumptions, impact-assessment model, and recycling allocation method.
- Sensitivity analysis tests the effect of changing important assumptions. Uncertainty analysis examines the effect of uncertain input data.
- Monte Carlo simulation repeatedly samples uncertain inputs to produce a distribution of possible results.
- Burden shifting occurs when reducing one environmental burden increases another burden elsewhere.
- Streamlined LCA is rapid and approximate, while full LCA uses more detailed data, software, modelling, and uncertainty analysis.
- Attributional LCA represents impacts using existing or average conditions. Consequential LCA models the effects of a change in demand, including displacement and marginal supply.
- Recycling allocation methods can substantially change results. Negative recycling emission factors represent accounting credits for avoided virgin-material production, not physical atmospheric removal.
- Input-output LCA traces monetary flows between economic sectors. Hybrid LCA combines process-based and input-output approaches.
- Sustainability assessment connects environmental, economic, and social outcomes.
- The economy concerns markets, production, services, sectors, and economic activity. Finance concerns money, cash, and spending or investment decisions.
- GDP measures economic activity but is not a direct measure of well-being, equality, living standards, or environmental condition.
- Economic impacts can be direct, indirect through supply chains, or induced through further spending of generated income.
- Social assessment involves defining boundaries, mapping stakeholders, identifying possible outcomes, gathering evidence, and linking outcomes to relevant SDG targets and indicators.
- Social-LCA databases indicate potential social risks; they do not prove that a specific supplier is causing a particular impact.
- Economic, social, and environmental outcomes may involve trade-offs and externalities.

## Equations and worked patterns

- Characterised impact:

  `I = Σ(E_i × CF_i)`

  Inventory flows are multiplied by their relevant characterisation factors and summed for the selected impact category.

- Streamlined emission calculation:

  `E = Σ(A_i × F_i)`

  For each activity or input, identify the activity data, select an emission factor, multiply, and sum across activities.

- Value added:

  `Value added = sales value − intermediate consumption`

- Production-based GDP:

  `GDP = sum of value added across the economy`

- Net domestic product:

  `NDP = GDP − depreciation of capital equipment`

- Spending multiplier:

  `Spending multiplier = induced economic activity / initial spending`

- Lecture calculator example:
  - Initial spending: $10,000.
  - Induced economic activity: $16,417.
  - Reported spending multiplier: 1.6417.
  - Reported employment effect: 0.08 FTE job.
  - The example illustrates how initial spending can circulate through suppliers, workers, income, and additional expenditure.

- Monte Carlo pattern:
  1. Assign uncertainty bounds to inputs.
  2. Randomly sample input values.
  3. Run the LCA calculation.
  4. Record the result.
  5. Repeat many times.
  6. Analyse the resulting distribution.

- Attributional pattern:
  - Use existing or average supply conditions to estimate impacts associated with a product or system.
  - This generally assumes that changes in demand produce proportional changes in emissions.

- Consequential pattern:
  - Identify the change in demand.
  - Determine displacement or substitution effects.
  - Identify marginal suppliers.
  - Include relevant economic ripple effects and changed purchasing patterns.

## Warnings and deadlines

- No specific calendar deadlines were stated in the two source summaries.
- The sustainability assignment requires LCA together with economic and social assessment.
- For the assignment, estimate local and regional economic impacts associated with operating and using the data centre.
- Use international input-output tables to identify and quantify the three largest suppliers for relevant production-stage inputs.
- Assume all IT equipment is produced in China.
- Describe possible induced economic benefits and impacts of AI use qualitatively, supported by evidence; the lecture states that these impacts are not expected to be quantified.
- Link identified social outcomes to relevant UN SDG targets and indicators, with supporting evidence.
- Use assignment-specific emission factors where supplied. The workshop database should not be used for the assignment if it lacks the required factors.
- Treat approximate characterisation factors, electricity factors, calculator outputs, sector classifications, and material identifications as model- or source-dependent.
- Report assumptions, dominant contributors, uncertainties, limitations, trade-offs, and conditions under which conclusions may change.
- Do not treat LCA results as direct measurements of actual environmental harm. They are modelled potential impacts.
- Verify uncertain names and sources in course materials before citing them, including the LCA database name and the economic-impact calculator name.

## Recall questions

1. What are the four stages of an LCA, and why might interpretation require returning to an earlier stage?
2. How does a characterisation factor convert an inventory flow into an impact-category result?
3. What is the difference between sensitivity analysis and uncertainty analysis?
4. How can burden shifting occur between impact categories or life-cycle stages?
5. What distinguishes attributional LCA from consequential LCA?
6. Why can marginal electricity have a different environmental intensity from average electricity supply?
7. Why can different recycling allocation methods produce substantially different LCA results?
8. What are the direct, indirect, and induced components of an economic impact?
9. Why is GDP not a direct measure of well-being or environmental condition?
10. Why do social-LCA database results indicate potential risk rather than proving a supplier-specific impact?

## Practice priorities

1. Practise applying `I = Σ(E_i × CF_i)` to a set of inventory flows and characterisation factors.
2. Practise applying `E = Σ(A_i × F_i)` using electricity, material, battery, and expenditure activity data.
3. Compare a streamlined LCA with a full LCA in terms of purpose, data quality, resolution, uncertainty, time, and cost.
4. Analyse a design choice for burden shifting across impact categories, life-cycle stages, or regions.
5. Explain when attributional and consequential LCA would use average versus marginal supply data.
6. For the sustainability assignment, map the data-centre system boundary from production through use and end of life.
7. Build a stakeholder map including the data-centre company, users, workers, local communities, suppliers, mining communities, manufacturers, and end-of-life organisations.
8. Use international input-output tables to identify the three largest suppliers for relevant China-based IT-equipment production inputs.
9. Structure an economic assessment around scope, sector, spending, money flows, direct impacts, supply-chain impacts, induced activity, and communication of findings.
10. Support proposed social outcomes with literature or stakeholder evidence, then link each outcome to a relevant SDG, target, and indicator.

## Missing or incomplete

- None identified for the requested week.
- The source summaries contain caveats about automated-transcript errors and uncertain names, values, database details, and examples. These are source limitations, not missing lectures.

## Source manifest

- Lecture 13 (echo-lecture-13-13): complete; summary `b9ededb2f79ca87ce3b7256e90453c363e66f31d5b685b039d605b39f1f6d979`; transcript `90a4a5ca10b4234295421c32ad8b985d6bdbbee6fb551163c0388ddf5c2b15c3`; summary path `[local source path redacted]`
- Lecture 14 (echo-lecture-14-14): complete; summary `868ce322fac16db43038f3b9378b7b764a11c4b5b9c1e355101672b9f06f7624`; transcript `a4e0aa03b09568778fea85f33865fce28c56c09a221b795fe4803aaf99d6e8f6`; summary path `[local source path redacted]`

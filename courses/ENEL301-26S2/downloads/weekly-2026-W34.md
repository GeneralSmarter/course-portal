<!-- week-id: 2026-W34 -->
<!-- generated-at: 2026-08-23T06:18:02.949351+12:00 -->
# ENEL301-26S2 weekly summary

## Coverage

- Week: 2026-W34, from 2026-08-17T00:00:00+12:00 to 2026-08-23T06:15:15.739855+12:00.
- Sources read: verified summaries for Lecture 11 and Lecture 12 only.
- Lecture 11 covered sustainability, engineering decision-making, corporate responsibility, systems thinking, causal loop diagrams, system boundaries, and the Makarewa hyperscale AI data-centre assignment.
- Lecture 12 covered life-cycle assessment (LCA), functional units, system boundaries, inventory data, environmental indicators, impact characterisation, normalisation, weighting, uncertainty, and trade-offs.

## Main concepts

- Engineering decisions involve constraints, uncertainty, competing objectives, stakeholder expectations, bias, and explicit trade-offs.
- Sound decision processes should involve affected stakeholders, communicate transparently, manage uncertainty, use decision gates where appropriate, and align engineering work with organisational objectives.
- Sustainable development requires balancing economic, social, and environmental outcomes while considering the needs of future generations.
- Sustainability is relevant to governance, risk management, environmental performance, stakeholder relationships, reputation, and long-term organisational viability.
- The SDG hierarchy is: goal → target → indicator.
- Systems thinking analyses connected components, interactions, feedback, delays, and unintended consequences.
- Causal loop diagrams are qualitative models:
  - Reinforcing loops amplify change.
  - Balancing loops counteract change and tend towards a target or equilibrium.
  - `+` links represent same-direction changes.
  - `−` links represent opposite-direction changes.
- System boundaries determine which components, processes, stakeholders, inputs, outputs, and impacts are included in an analysis. Boundary choices can materially change conclusions.
- The sustainability assignment assesses the proposed Makarewa Data Grid across:
  - Environmental impacts using LCA.
  - Economic impacts.
  - Social impacts.
  - A causal loop diagram.
- LCA estimates potential environmental impacts across a product or service’s life cycle. It is a model of reality, not a direct measurement of reality.
- Life-cycle thinking includes extraction, processing, manufacturing, packaging, transport, use, and end-of-life.
- Average electricity emission factors describe the existing grid average; marginal factors may better represent the emissions associated with additional demand.
- A functional unit defines the comparable service delivered by alternatives. Comparisons should be based on equivalent function rather than simply per item or per kilogram.
- LCA results depend on assumptions about the functional unit, system boundary, data quality, electricity source, time horizon, allocation, and end-of-life treatment.
- Foreground data is specific to the system being studied; background data comes from existing databases for supporting processes.
- Characterisation converts different flows into common units within an impact category.
- Normalisation compares results with a reference baseline.
- Weighting assigns relative importance to impact categories and is inherently subjective.
- Environmental improvements can involve trade-offs: reducing one impact may increase another.
- LCA can support product development, process improvement, policy, supply-chain analysis, market access, and environmental communication, but selective boundaries or indicators can create greenwashing risks.

## Equations and worked patterns

- Sustainability definition, expressed conceptually:
  
  `Sustainable development = meeting present needs without compromising future generations’ ability to meet their needs`

- Sustainability pillars:

  `Sustainability considerations = economic + social + environmental`

  Cultural considerations were treated within the social or societal pillar for this course.

- Temperature-gap balancing loop:

  `Temperature gap = ideal temperature − actual temperature`

  Lecture example:

  `37°C − 36°C = 1°C`

  A compensating response such as shivering reduces the gap, illustrating a balancing loop.

- Passenger-kilometre functional unit:

  `Passenger-kilometres = number of passengers × distance travelled`

- Life-cycle inventory:

  `LCI = resources and energy in, emissions and waste out`

- Impact characterisation for category `k`:

  `Iₖ = Σᵢ(Fᵢ × Cᵢ,ₖ)`

  where `Fᵢ` is the quantity of flow `i`, and `Cᵢ,ₖ` is its characterisation factor for impact category `k`.

- Climate-change characterisation pattern:

  `I_climate = Σᵢ(Fᵢ × GWPᵢ)`

  The result may be expressed in kg CO₂-equivalent. The selected factors and time horizon must be stated.

- Normalisation:

  `I_normalised = I_system / I_reference`

- Worked reasoning pattern for an LCA comparison:
  1. Define the goal and scope.
  2. Select an equivalent functional unit.
  3. Set and document the system boundary and exclusions.
  4. Select relevant environmental indicators.
  5. Collect foreground data and connect it to background databases.
  6. Build the inventory.
  7. Characterise flows into impact categories.
  8. Normalise or weight only with explicit justification.
  9. Interpret trade-offs, uncertainty, data quality, and sensitivity to assumptions.

## Warnings and deadlines

- The Lecture 11 summary states that the sustainability assignment report was due Friday 9 October at 5:00 pm in Week 11. The summary explicitly says to verify submission details against the current Learn assignment brief.
- One peer-assessment date was verbally corrected from September to October. The current Learn assignment brief is authoritative.
- The assignment is worth 20% of ENEL301 and requires a report and an Excel document, according to Lecture 11.
- The data cable is outside the stated assignment scope; assess the data centre only and assume that it remains connected.
- Project claims about generator numbers, water use, investment, electricity use, and staging were presented as uncertain or changing. Do not treat them as independently verified facts without checking the assignment materials.
- For additional data-centre electricity demand, an average grid emission factor may underestimate impacts if marginal generation has higher emissions, particularly during high-demand or cold-weather periods.
- LCA comparisons must use equivalent functional units, boundaries, time horizons, indicators, and comparable data. Otherwise, apparently favourable results may be misleading.
- The approximately 95% system-boundary coverage figure is only a lecture rule of thumb, not a formal standard requirement.
- Weighting is subjective. Conclusions that depend strongly on weighting should be reported cautiously.
- The lecture summaries contain identified transcription uncertainties, including some terminology, figures, and historical claims. Verify exact details against course materials before using them in formal work.

## Recall questions

1. Why should engineering decisions explicitly address uncertainty, stakeholder participation, transparency, and bias?
2. What is the difference between a reinforcing and a balancing feedback loop?
3. How can changing a system boundary alter the conclusions of a sustainability assessment?
4. What are the four major components of the Makarewa Data Grid assignment, and why are they interdependent?
5. Why might a marginal electricity emission factor be more appropriate than an average factor for a new data centre?
6. What is a functional unit, and why is “one product” often an inadequate basis for comparison?
7. What is the difference between foreground data and background data in an LCA?
8. How does impact characterisation convert inventory flows into an impact-category result?
9. Why can climate-change results not be directly added to eutrophication or phosphate-equivalent results?
10. How can an LCA be used legitimately while still creating a risk of greenwashing?

## Practice priorities

1. Practise defining a functional unit for the Data Grid service and explain what comparison it enables.
2. Draw a causal loop diagram for a data-centre issue, using noun-based variables, correctly directed links, `+`/`−` signs, and `R`/`B` loop labels.
3. Build a boundary checklist for the Data Grid LCA, including servers, racks, buildings, maintenance, electricity and water infrastructure, batteries, transport, labour, and excluded cable impacts.
4. For any LCA comparison, audit whether the alternatives have equivalent functions, boundaries, data quality, time horizons, and end-of-life assumptions.
5. Practise explaining why additional electricity demand may require marginal rather than average grid emissions.
6. Work through the LCA sequence from goal and scope to inventory, characterisation, interpretation, and uncertainty analysis.
7. Review the three sustainability pillars alongside the SDG goal → target → indicator hierarchy.
8. Prepare to defend assumptions transparently and identify how social, economic, and environmental findings affect one another.

## Missing or incomplete

- No missing or incomplete lectures were identified for this week.

## Source manifest

- Lecture 11 (echo-lecture-11-11): complete; summary `0c581351e451d047b42ff34abb6db3cd9dd292d01f653412b6933edf65a8ac31`; transcript `528af9dd9a7981e1603b0d501e1f73f040858059a1ce90aea1d874554edee79b`; summary path `[local source path redacted]`
- Lecture 12 (echo-lecture-12-12): complete; summary `a3b39f060752ac1f363a77a3f46a7ad32b33536117ff97a59558daf22a2b84a1`; transcript `4f86d737172381c1122e358fdd8bd60c544185ea5ae8eb5d4a3e073a86ef2f2e`; summary path `[local source path redacted]`

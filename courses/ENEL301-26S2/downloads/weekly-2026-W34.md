<!-- week-id: 2026-W34 -->
<!-- generated-at: 2026-08-23T09:33:15.653585+12:00 -->
# ENEL301-26S2 weekly summary

## Coverage

- Week: 2026-W34, from 2026-08-17T00:00:00+12:00 to 2026-08-23T06:15:15.739855+12:00.
- Covered verified summaries:
  - Lecture 11: sustainability, engineering responsibility, systems thinking, causal loop diagrams, and the Makarewa Data Grid assignment.
  - Lecture 12: life-cycle assessment, functional units, system boundaries, environmental indicators, inventory data, and impact interpretation.
- Source basis: `lecture_11_summary.md` and `lecture_12_summary.md` only.

## Main concepts

- Sustainability is context-dependent and involves balancing economic, social, and environmental outcomes. Cultural considerations may be treated within the social pillar for this course. (Lecture 11)
- Sustainable development was defined using the Brundtland formulation: meeting present needs without compromising future generations’ ability to meet their needs. (Lecture 11)
- Engineering decisions require explicit treatment of constraints, uncertainty, trade-offs, stakeholder expectations, organisational objectives, transparency, and bias. Decision gates can support decisions as project information changes. (Lecture 11)
- Sustainability contributes to corporate governance, risk management, environmental performance, stakeholder engagement, reputation, and long-term organisational viability. (Lecture 11)
- Systems thinking analyses connections, feedback, delays, interactions, and unintended consequences in complex systems. (Lecture 11)
- Causal loop diagrams are qualitative representations of cause-and-effect relationships. Reinforcing loops amplify change; balancing loops counteract change and tend towards a target or equilibrium. (Lecture 11)
- System boundaries determine which components, stakeholders, processes, inputs, outputs, and impacts are included in an analysis. Boundary selection can change the conclusions. (Lecture 11; Lecture 12)
- The sustainability assignment concerns a proposed hyperscale AI data centre in Makarewa, Southland. Its four components are environmental assessment using LCA, economic impact assessment, social impact assessment, and a causal loop diagram. The components and assumptions are interdependent. (Lecture 11)
- Life-cycle assessment evaluates potential environmental impacts across a product or service’s life cycle. It is a model of reality, not a direct measurement of reality. (Lecture 12)
- Life-cycle thinking includes resource extraction, processing, manufacturing, packaging, transport, use, and end-of-life. (Lecture 12)
- Average electricity emission factors describe average grid intensity; marginal factors better represent emissions from additional demand and may be higher during periods of high demand. (Lecture 12)
- A functional unit defines the service being delivered so that alternatives can be compared on an equivalent basis. (Lecture 12)
- LCA results depend on assumptions about data, system boundaries, functional units, time horizons, indicators, allocation, and end-of-life treatment. (Lecture 12)
- Foreground data are specific to the studied system; background data come from existing databases for supporting processes. (Lecture 12)
- Characterisation converts flows into impact-category results. Normalisation compares results with a reference; weighting combines categories using subjective value judgements. (Lecture 12)
- LCA involves trade-offs between indicators. A reduction in one impact may increase another, so a single overall “best” option may not exist. (Lecture 12)

## Equations and worked patterns

- Sustainability concept:
  
  Sustainable development = meeting present needs without compromising future generations’ ability to meet their needs.

- Simplified sustainability framework:

  Sustainability considerations = economic + social + environmental

- Temperature-gap balancing loop:

  Temperature gap = ideal temperature − actual temperature

  For the lecture’s example:

  Temperature gap = 37 °C − 36 °C = 1 °C

  The gap produces a compensating response such as shivering, which raises body temperature towards the desired state. (Lecture 11)

- Causal-loop link notation:
  - `+`: variables change in the same direction.
  - `−`: variables change in opposite directions.
  - `R`: reinforcing loop, which amplifies change.
  - `B`: balancing loop, which counteracts change.

- Passenger-kilometre functional unit:

  Passenger-kilometres = number of passengers × distance travelled

- Life-cycle inventory pattern:

  LCI = resources and energy in, emissions and waste out

- Impact characterisation:

  Iₖ = Σᵢ(FᵢCᵢ,ₖ)

  where `Iₖ` is the result for impact category `k`, `Fᵢ` is the quantity of flow `i`, and `Cᵢ,ₖ` is the characterisation factor for flow `i` in category `k`.

- Climate-change characterisation:

  I_climate = Σᵢ(Fᵢ × GWPᵢ)

  The result may be expressed in kg CO₂-equivalent. The selected factors and time horizon must be stated.

- Normalisation:

  I_normalised = I_system / I_reference

  The lecture used comparison of the Data Grid carbon footprint with New Zealand’s total carbon footprint as an example. The reference year and dataset would need to be specified.

- Functional-unit examples:
  - Soft-drink packaging: 1 litre delivered to the consumer.
  - Car transport: passenger-kilometres.
  - Solar photovoltaic system: 1 kWh delivered to a household.
  - Data Grid assignment: one year of Data Grid services.

## Warnings and deadlines

- The Lecture 11 summary states that the sustainability assignment report is due Friday 9 October at 5:00 pm, identified as Week 11. The current Learn assignment brief is authoritative and should be checked before relying on this date.
- Lecture 11 records that one peer-assessment date was verbally corrected from September to October. The current Learn brief should be checked for the exact date.
- The assignment requires a report and an Excel document and is worth 20% of ENEL301, according to the lecture summary. Current assignment instructions should be checked for definitive requirements.
- The assignment’s environmental, social, economic, and causal-loop components should not be treated as isolated tasks because their assumptions and findings affect one another.
- For the assignment, the data cable is outside the stated scope; students should assess the data centre only and assume it remains connected. The assignment brief should be checked for any later scope changes.
- Project claims about generators, water consumption, investment, electricity use, facility scale, and other scenario figures were presented as uncertain or changing claims. They should be documented, checked, and treated as assumptions or claims to assess rather than automatically verified facts.
- Do not use average grid emissions automatically for new electricity demand. Consider whether a marginal emission factor better represents the additional generation.
- Avoid misleading LCA comparisons caused by unequal system boundaries, omitted upstream processes, non-equivalent functional units, inconsistent time horizons, or selective communication that creates greenwashing risk.
- The summaries identify some transcript uncertainty, including the terminology “neutrification potential,” which may refer to eutrophication potential. Verify course terminology if using it formally.

## Recall questions

1. What are the three sustainability pillars used in the course, and how may cultural considerations fit within that framework?
2. Why are engineering decision gates useful when a project begins with substantial uncertainty?
3. What is the difference between a reinforcing loop and a balancing loop?
4. How did the pharmacy dispensing example illustrate a reinforcing feedback loop?
5. Why can changing a system boundary change the conclusions of a sustainability assessment?
6. Why is an LCA result described as a potential environmental impact rather than a direct measurement?
7. What is a functional unit, and why is “one bottle” potentially a poor unit for comparing soft-drink packaging?
8. Why might a marginal electricity emission factor be more appropriate than an average factor for assessing a new data centre?
9. What is the difference between foreground data and background data?
10. How do characterisation, normalisation, and weighting differ in an LCA?

## Practice priorities

- Construct a causal loop diagram for the Data Grid project using noun-based variables, correctly directed causal links, `+`/`−` relationships, and labelled reinforcing or balancing loops.
- Define a defensible system boundary for the Data Grid assessment. Explicitly record included and excluded processes, including capital equipment, maintenance, electricity and water infrastructure, transport, labour, and the data cable.
- Choose and justify the functional unit of one year of Data Grid services, while recognising the allocation difficulty between storage, cloud computing, and generative AI services.
- Build an LCA reasoning chain: goal and scope, functional unit, boundary and exclusions, indicators, foreground and background data, inventory, characterisation, interpretation, and comparison.
- Test the sensitivity of conclusions to changing assumptions such as electricity source and timing, marginal versus average emissions, water use, backup systems, equipment inclusion, and end-of-life treatment.
- Practise identifying trade-offs across climate change, smog, ozone depletion, acidification, eutrophication, toxicity, respiratory effects, and resource depletion rather than reducing the analysis to one indicator.
- For written work, distinguish verified facts from scenario claims, state assumptions clearly, involve economic, social, environmental, and systems perspectives, and explain uncertainty.

## Missing or incomplete

- None.

## Source manifest

- Lecture 11 (echo-lecture-11-11): complete; summary `0c581351e451d047b42ff34abb6db3cd9dd292d01f653412b6933edf65a8ac31`; transcript `528af9dd9a7981e1603b0d501e1f73f040858059a1ce90aea1d874554edee79b`; summary path `[local source path redacted]`
- Lecture 12 (echo-lecture-12-12): complete; summary `a3b39f060752ac1f363a77a3f46a7ad32b33536117ff97a59558daf22a2b84a1`; transcript `4f86d737172381c1122e358fdd8bd60c544185ea5ae8eb5d4a3e073a86ef2f2e`; summary path `[local source path redacted]`

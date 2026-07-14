<!-- week-id: 2026-W29 -->
<!-- generated-at: 2026-07-15T10:42:16.796150+12:00 -->
# ENEL372-26S2 weekly summary

## Coverage

- Week: 2026-W29, from 13 July 2026 at 00:00 to 19 July 2026 at 08:30 NZST.
- Source coverage: Lecture 1, delivered 13 July 2026.
- Lecture 1 introduced power-electronic conversion, switching-based efficiency, feedback regulation, conversion categories, semiconductor devices, and device-selection trade-offs.
- Lectures 2 and 3 are not represented because their summaries are missing.
- Source limitation: Lecture 1 was summarized from a checked local transcript, but its audio and diagrams were not manually reviewed. Visual details should be confirmed against the slides.

## Main concepts

- Power electronics concerns the efficient conversion and control of electrical power.
- Semiconductor devices are primarily operated as switches:
  - An ideal off switch carries no current.
  - An ideal on switch has no voltage across it.
  - In either ideal state, switch power dissipation is near zero.
- Real converters have conduction and switching losses. The lecture stated that a well-designed modern converter may limit total losses to roughly 1–2%.
- Inductors and capacitors provide energy storage and output filtering and are treated as lossless in the introductory model.
- Practical converters normally require feedback because source voltage and load demand can vary. The output is measured, compared with a reference, and used to adjust converter switching.
- Main conversion categories:
  - AC to DC: rectification.
  - DC to AC: inversion.
  - DC to DC: changing DC voltage or current levels.
  - AC to AC: potentially using multiple conversion stages.
- Device characteristics:
  - Diode: uncontrolled, one-directional conduction when forward biased.
  - MOSFET: voltage-controlled, fast-switching, and suited to high switching frequencies.
  - BJT: current-controlled and slower than a MOSFET, with potentially favourable high-current conduction behaviour.
  - IGBT: combines a MOSFET-like gate with a BJT-like output and balances drive convenience, switching speed, and high-current performance.
  - SCR: gate-triggered and latching; normal gate control cannot turn it off.
  - GTO: permits controlled turn-off but requires substantial gate current.
  - Triac: provides bidirectional thyristor behaviour.
- Higher switching frequency can reduce passive-component size and improve control bandwidth, but it increases switching-loss demands.
- Device selection must consider voltage, current, switching frequency, drive requirements, conduction loss, switching loss, and controlled turn-off capability.

## Equations and worked patterns

- Introductory power balance:

  `P_input = P_output + P_loss`

- Ideal-switch reasoning:
  - Off state: current is zero, so switch dissipation is ideally zero.
  - On state: voltage across the switch is zero, so switch dissipation is ideally zero.
- Diode pattern:
  - A silicon diode was described as beginning conduction at approximately 0.7 V forward bias.
  - Its introductory ideal model is an open circuit when off and a short circuit when on.
- Enhancement N-channel MOSFET pattern:
  - `V_GS = 0` corresponds to the off state.
  - Typical power-MOSFET threshold voltage was stated as approximately 2–3 V.
  - Conventional power MOSFETs are commonly driven at approximately 10 V to operate well within the on region.
  - The ideal on-state model uses `R_DS(on) ≈ 0`; real devices retain conduction loss.
- SCR switching pattern:
  - Forward bias alone does not initiate conduction.
  - A gate pulse turns the SCR on.
  - Once latched, it remains on until current falls to zero and the device becomes reverse biased.

## Warnings and deadlines

- Lectures move to E16 from the week following Lecture 1; students were explicitly told not to return to the original room.
- Assessment structure stated in Lecture 1:
  - Group design-and-build project: 30%.
  - Invigilated test: 35%.
  - Exam: 35%.
- The transcript states a 40% average requirement across the invigilated assessments. The course outline remains authoritative for the exact hurdle wording.
- Generative AI is not permitted in the test or exam. Rules for other assessments must be checked in the course outline.
- The project involves building a controlled power converter for a small model solar-powered car in groups of three.
- A full lecture about the project was expected during the following week.
- No specific submission or examination dates were present in the available summary.

## Recall questions

1. Why does an ideal switch dissipate almost no power when fully on or fully off?
2. State the input, output, and loss power relationship introduced in Lecture 1.
3. Why are inductors and capacitors important in switch-mode power conversion?
4. Which conversion directions define a rectifier and an inverter?
5. Why does a practical power converter normally require feedback?
6. How do the control inputs of a MOSFET and BJT differ?
7. Why is a MOSFET’s threshold voltage not necessarily a sufficient gate-drive voltage?
8. How is an SCR turned on, and what conditions are required to turn it off?
9. How does increasing switching frequency affect passive-component size and switching loss?
10. What assessment weightings and invigilated-assessment hurdle were stated?

## Practice priorities

1. Draw and label a generic closed-loop converter containing the source, switching stage, output filter, load, sensor, reference, controller, and control signal.
2. Practise classifying systems as AC–DC, DC–AC, DC–DC, or AC–AC converters.
3. Build a comparison table for the diode, MOSFET, BJT, IGBT, SCR, GTO, and triac using control type, turn-off control, switching speed, and typical operating region.
4. Practise applying `P_input = P_output + P_loss` while clearly distinguishing the introductory ideal model from real converter losses.
5. Review the lecture slides for the device-capability chart and conversion-function diagrams, which were not reconstructed in the source summary.
6. Learn device-selection reasoning rather than memorizing device names: connect voltage, current, frequency, losses, gate-drive requirements, and turn-off control to the choice of semiconductor.
7. Review the course outline for authoritative assessment-hurdle and generative-AI rules.

## Missing or incomplete

- Lecture 2: missing summary.
- Lecture 3: missing summary.
- Content from those lectures has not been inferred or reconstructed.
- Lecture 1 slide diagrams, topology details, and capability-chart values remain incomplete because the audio and visual material were not manually reviewed.
- Commercial device ratings must not be inferred from the introductory values stated in Lecture 1.

## Source manifest

- Lecture 1 (echo-lecture-1-1): complete; summary `71f2d3d55d3f94b95fb26da795b2d08cd37fe809265679ecbe63fac52f3e6e84`; transcript `bbb49c47d74b496049a0deb37c09fd5d63e1f0723226e26fa94f40e4efdb4a69`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENEL372-26S2/summaries/lecture_01_summary.md`
- Lecture 2 (echo-lecture-2-2): missing_summary; summary `missing`; transcript `missing`; summary path `missing`
- Lecture 3 (echo-lecture-3-3): missing_summary; summary `missing`; transcript `missing`; summary path `missing`

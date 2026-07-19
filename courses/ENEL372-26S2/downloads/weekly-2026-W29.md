<!-- week-id: 2026-W29 -->
<!-- generated-at: 2026-07-19T12:32:24.900024+12:00 -->
# ENEL372-26S2 weekly summary

## Coverage

- Week: 2026-W29, from 13 July 2026 00:00 NZST to 19 July 2026 12:28 NZST.
- Source reviewed: Lecture 1 summary, covering “Introduction to Power Electronics” on 13 July 2026.
- Lecture 2 and Lecture 3 summaries were unavailable, so this summary reflects Lecture 1 only.
- The source summary was based on a checked local transcript. Slide diagrams and audio were not manually reviewed.

## Main concepts

- Power electronics concerns the efficient conversion and control of electrical power.
- Semiconductor devices are primarily operated as switches:
  - An ideal off switch carries no current.
  - An ideal on switch has no voltage across it.
  - Either ideal state therefore has near-zero power dissipation.
- Real converters have conduction and switching losses. The lecture stated that a well-designed modern converter may limit total losses to roughly 1–2%.
- Inductors and capacitors provide energy storage and output filtering and are treated as lossless in the introductory model.
- Feedback is normally required because source voltage and load demand can vary. The output is measured, compared with a reference, and used to adjust converter switching.
- Main conversion categories:
  - AC to DC: rectifier
  - DC to AC: inverter
  - DC to DC: changes DC voltage or current levels
  - AC to AC: may use multiple conversion stages
- Semiconductor-device characteristics:
  - Diode: uncontrolled one-way conduction from anode to cathode when forward biased.
  - MOSFET: voltage controlled, fast switching, and includes a body diode.
  - BJT: current controlled and slower than a MOSFET, with potentially favourable high-current conduction behaviour.
  - IGBT: combines a MOSFET-like insulated gate with a BJT-like output.
  - SCR: gate-triggered and latches on until current falls to zero and the device becomes reverse biased.
  - GTO: supports controlled turn-off but requires substantial gate current.
  - Triac: provides bidirectional thyristor behaviour.
- Device selection requires trade-offs among voltage, current, switching frequency, drive requirements, conduction loss, switching loss, and controlled turn-off.
- Higher switching frequency can reduce passive-component size and improve control bandwidth, but increases switching-loss demands.

## Equations and worked patterns

- General power balance:

  `P_input = P_output + P_loss`

- Rearranged output-power pattern:

  `P_output = P_input - P_loss`

- Ideal-switch reasoning:
  - Off state: current is zero, so switch power dissipation is ideally zero.
  - On state: voltage across the switch is zero, so switch power dissipation is ideally zero.
- Introductory converter-analysis pattern:
  1. Identify input and output electrical forms.
  2. Classify the conversion as AC–DC, DC–AC, DC–DC, or AC–AC.
  3. Apply the power balance.
  4. Treat inductors and capacitors as ideal storage or filtering elements unless non-ideal losses are specified.
  5. Identify how feedback changes the switching action to regulate the output.
- Device-selection pattern:
  1. Determine required voltage and current capability.
  2. Determine switching-frequency requirements.
  3. Check gate or base-drive requirements.
  4. Compare conduction and switching losses.
  5. Determine whether controlled turn-off is required.

## Warnings and deadlines

- No assignment deadline was stated in the available source.
- Lectures move to E16 from the week following Lecture 1; students were explicitly warned not to return to the original room.
- The group design-and-build project is worth 30% and concerns a controlled power converter for a small model solar-powered car, completed in groups of three.
- The invigilated test is worth 35%, and the exam is worth 35%.
- The transcript stated a 40% average requirement across the invigilated assessments. Project marks cannot compensate for falling below this requirement.
- Generative AI is not permitted in the test or exam. The course outline is authoritative for detailed assessment rules and AI permissions.
- A full lecture on the project was expected in the following week.
- Slide diagrams, especially the device-capability chart and conversion-function diagram, should be checked directly before using them for design decisions.
- Numerical device ratings mentioned in the lecture should not be treated as universal selection limits.

## Recall questions

1. Why does an ideal switch dissipate almost no power when fully on or fully off?
2. What is the relationship between input power, output power, and converter loss?
3. Why are inductors and capacitors central to switch-mode power conversion?
4. Which conversion directions define a rectifier and an inverter?
5. Why does a practical converter normally require feedback?
6. How do the control inputs of a MOSFET and BJT differ?
7. Why is a MOSFET’s threshold voltage not necessarily a suitable gate-drive voltage?
8. How is an SCR turned on, and what conditions are required to turn it off?
9. What properties does an IGBT combine from MOSFETs and BJTs?
10. How do switching frequency and required voltage or current capability affect semiconductor-device selection?

## Practice priorities

1. Draw and label a closed-loop converter containing the source, switching stage, output filter, load, sensor, reference, controller, and control signal.
2. Practise classifying systems as AC–DC, DC–AC, DC–DC, or AC–AC converters.
3. Apply the introductory power-balance equation and distinguish input power, useful output power, and loss.
4. Build a comparison table for the diode, MOSFET, BJT, IGBT, SCR, GTO, and triac, covering control method, turn-off control, relative switching speed, and typical operating region.
5. Explain why a high-frequency moderate-current converter would initially suggest a different device family from a mains-frequency very-high-power controller.
6. Review the original slides for the device-capability chart and conversion-function diagrams.
7. Review the course outline for the precise invigilated-assessment hurdle and permitted use of generative AI.

## Missing or incomplete

- Lecture 2: missing summary.
- Lecture 3: missing summary.
- Consequently, no concepts, equations, examples, warnings, or deadlines from Lectures 2 or 3 are included.
- Visual details from Lecture 1 were not independently checked against the original slides.
- Exact commercial device ratings and uncertain high-voltage capability examples require confirmation from the slides or device documentation.

## Source manifest

- Lecture 1 (echo-lecture-1-1): complete; summary `71f2d3d55d3f94b95fb26da795b2d08cd37fe809265679ecbe63fac52f3e6e84`; transcript `bbb49c47d74b496049a0deb37c09fd5d63e1f0723226e26fa94f40e4efdb4a69`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENEL372-26S2/summaries/lecture_01_summary.md`
- Lecture 2 (echo-lecture-2-2): missing_summary; summary `missing`; transcript `missing`; summary path `missing`
- Lecture 3 (echo-lecture-3-3): missing_summary; summary `missing`; transcript `missing`; summary path `missing`

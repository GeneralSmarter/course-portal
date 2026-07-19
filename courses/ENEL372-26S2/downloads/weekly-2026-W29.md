<!-- week-id: 2026-W29 -->
<!-- generated-at: 2026-07-19T20:35:21.376166+12:00 -->
# ENEL372-26S2 weekly summary

## Coverage

- Week 29 covered Lectures 1–3, delivered from 2026-07-13 to 2026-07-19.
- Lecture 1 introduced power electronics, switching conversion, feedback, converter categories, and semiconductor-device trade-offs.
- Lecture 2 developed power, energy, RMS analysis, inductor and capacitor behaviour, periodic steady state, duty ratio, and inductive energy recovery.
- Lecture 3 introduced the buck converter, PWM, continuous conduction, volt-second balance, capacitor ripple, and input/output power analysis.
- All three verified per-lecture summary files were available. No lectures were identified as missing or incomplete.

## Main concepts

- Power electronics efficiently converts and controls electrical power using semiconductor switches, with inductors and capacitors storing, transferring, and filtering energy. [Lecture 1]
- Ideal switches dissipate little power when fully on or fully off. Real converters still incur conduction and switching losses. [Lecture 1]
- Main conversion categories are AC–DC rectification, DC–AC inversion, DC–DC conversion, and AC–AC conversion. [Lecture 1]
- Practical converters normally use feedback to regulate an output against source and load changes. [Lecture 1]
- Device selection involves trade-offs among voltage rating, current capability, switching speed, conduction loss, switching loss, drive requirements, and turn-off control. [Lecture 1]
- Instantaneous power is the product of voltage and current, while energy is the time integral of power. Power signs depend on the selected reference directions. [Lecture 2]
- Ideal inductors and capacitors are lossless energy-storage elements in the introductory model. [Lecture 2]
- Periodic steady state requires zero net inductor-current change and zero net capacitor-voltage change over a switching period. These conditions do not mean zero ripple. [Lecture 2]
- RMS values describe the heating or power-producing effect of periodic waveforms and are not generally interchangeable with average values. [Lecture 2]
- An inductor’s current cannot change instantaneously. It needs a deliberate current path, such as a diode, clamp, snubber, or flyback path, when switched off. [Lecture 2]
- A buck converter is a step-down DC–DC converter. In ideal continuous-conduction operation, its output voltage is controlled by duty ratio. [Lecture 3]
- In a buck converter, the inductor current rises while the switch is on and falls through the diode path while the switch is off. [Lecture 3]
- Continuous inductor current can still have significant ripple. The switch/source current is discontinuous because it is zero during the switch-off interval. [Lecture 3]
- The capacitor absorbs and supplies the difference between varying inductor current and approximately constant load current. [Lecture 3]

## Equations and worked patterns

- Power balance:
  
  `P_input = P_output + P_loss`
  
  For an ideal converter, `P_input = P_output`. [Lecture 1, Lecture 3]

- Instantaneous power and energy:
  
  `p(t) = v(t)i(t)`
  
  `W = ∫ p(t) dt`
  
  `P_avg = (1/T) ∫ p(t) dt = W_T/T = fW_T` [Lecture 2]

- Inductor and capacitor relationships:
  
  `v_L = L(di_L/dt)`
  
  `i_C = C(dv_C/dt)`
  
  `W_L = 1/2 L i_L²`
  
  `W_C = 1/2 C v_C²` [Lecture 2]

- Periodic steady-state balances:
  
  `∫ over one period v_L(t) dt = 0`
  
  `∫ over one period i_C(t) dt = 0`
  
  These enforce repeating inductor current and capacitor voltage. [Lecture 2]

- RMS calculation:
  
  `V_RMS = √[(1/T)∫ v²(t) dt]`
  
  `I_RMS = √[(1/T)∫ i²(t) dt]`
  
  For a resistor:
  
  `P_avg = V_RMS²/R = I_RMS²R` [Lecture 2]

- Rectangular pulse with amplitude `V_s` and duty ratio `D`:
  
  `D = T_on/T`
  
  `V_avg = DV_s`
  
  `V_RMS = |V_s|√D` [Lecture 2]

- Constant inductor voltage:
  
  `di_L/dt = v_L/L`
  
  Therefore, a constant positive voltage produces a linear current rise, while a constant negative voltage produces a linear current fall. [Lecture 2]

- Buck-converter switch intervals:
  
  Switch on:
  
  `v_L = V_s - V_out`
  
  `Δi_L,on = [(V_s - V_out)DT]/L`
  
  Switch off:
  
  `v_L = -V_out`
  
  `Δi_L,off = -[V_out(1-D)T]/L` [Lecture 3]

- Ideal buck-converter derivation:
  
  Apply periodic steady state:
  
  `Δi_L,on + Δi_L,off = 0`
  
  This gives:
  
  `V_out = DV_s`
  
  or:
  
  `V_out/V_s = D` [Lecture 3]

- Continuous-conduction boundary:
  
  At the boundary, the minimum inductor current reaches zero:
  
  `I_R = Δi_L/2`
  
  Here, `Δi_L` is treated as peak-to-peak ripple under the lecture’s notation. [Lecture 3]

- Output-node current relationship:
  
  `I_R = i_L - i_C`
  
  Therefore:
  
  `i_C = i_L - I_R`
  
  The capacitor current has zero average in steady state and carries the ripple component required to support the load. [Lecture 3]

- Power calculation pattern for the buck converter:
  
  `P_out = V_out I_R = V_out²/R = I_R²R`
  
  `P_in = V_s,rms I_s,rms`
  
  Since the source voltage is DC, `V_s,rms = V_s`, but the pulsed source current requires an RMS calculation rather than simple substitution of its average value. [Lecture 3]

## Warnings and deadlines

- Lectures move to E16 from the following week. Do not return to the first-lecture room. [Lecture 1]
- The group design-and-build project is worth 30% and concerns a controlled power converter for a small model solar-powered car, completed in groups of three. [Lecture 1]
- The invigilated test is worth 35% and the exam is worth 35%. [Lecture 1]
- The lecture stated a 40% average requirement across the invigilated assessments. The course outline remains authoritative for the exact hurdle wording. [Lecture 1]
- Generative AI is not permitted in the test or exam. Assessment rules beyond this statement should be checked in the course outline. [Lecture 1]
- A full lecture in the following week was expected to cover the project. [Lecture 1]
- RMS source-current analysis for the buck converter was assigned as homework, but the completed closed-form solution was not included in the summary. Do not infer the final expression without the relevant teaching material. [Lecture 3]
- Check the original slides before relying on the triangular-wave RMS result or reproducing the exact energy-recovery circuit topology, because the summaries identify source or notation uncertainty. [Lecture 2]

## Recall questions

1. Why do ideal fully on and fully off switches dissipate little power?
2. What are the four main categories of power conversion?
3. Why does a practical converter normally require feedback?
4. How do MOSFETs, BJTs, IGBTs, and thyristor-family devices differ in control method and switching-speed trade-offs?
5. What does inductor volt-second balance mean, and what condition does it impose in periodic steady state?
6. Why can an inductor have non-zero average current even though its net current change over one switching period is zero?
7. Why must an energised inductor have a current path when its switch is turned off?
8. Why does the ideal buck converter satisfy `V_out = D V_s`?
9. What distinguishes continuous from discontinuous inductor current?
10. Why must the RMS source current, rather than its average value, be used when calculating buck-converter input power?

## Practice priorities

1. Draw the closed-loop structure of a controlled converter, including source, switching stage, filter, load, sensor, reference, controller, and feedback signal.
2. Build a device comparison table covering control input, switching speed, current/voltage capability, conduction behaviour, and turn-off control.
3. Practise applying inductor volt-second balance to two switch states with different inductor voltages.
4. Calculate average and RMS values for rectangular pulses with several duty ratios.
5. Sketch the inductor current, capacitor current, switch current, and source current of an ideal buck converter over one switching period.
6. Derive the buck-converter voltage relationship from both inductor-current changes and average inductor voltage.
7. Determine whether a given ripple and average load current imply continuous or discontinuous conduction.
8. Complete the assigned buck-converter RMS source-current calculation using the actual waveform rather than its average current.
9. Explain the energy path during both switch-on and switch-off intervals, including the role of the diode.
10. Review the project requirements and assessment weighting, then confirm the exact hurdle and assessment rules in the course outline.

## Missing or incomplete

- None identified for 2026-W29.
- Source limitations remain: some Lecture 2 waveform conventions and the exact energy-recovery circuit arrangement require confirmation against the original slides.

## Source manifest

- Lecture 1 (echo-lecture-1-1): complete; summary `71f2d3d55d3f94b95fb26da795b2d08cd37fe809265679ecbe63fac52f3e6e84`; transcript `bbb49c47d74b496049a0deb37c09fd5d63e1f0723226e26fa94f40e4efdb4a69`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENEL372-26S2/summaries/lecture_01_summary.md`
- Lecture 2 (echo-lecture-2-2): complete; summary `51c67409849ba32064036a8223f2fdb9661d38c3c3c96c84e45b15167e99e89a`; transcript `0d2b0514e2c9187674f937c7b80c2a72905b24e9a940bd5aafd18dc7b69f08bf`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENEL372-26S2/summaries/lecture_02_summary.md`
- Lecture 3 (echo-lecture-3-3): complete; summary `8928b31fa3a137d1458b64d067fbc4f4a590d4419fc2fad49365ead37fa9eb8f`; transcript `42868d83e4317bffd258eeb514cfe1b34a3c73c68ae0afe07d922d4a980e19ac`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENEL372-26S2/summaries/lecture_03_summary.md`

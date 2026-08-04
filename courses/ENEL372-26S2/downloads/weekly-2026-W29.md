<!-- week-id: 2026-W29 -->
<!-- generated-at: 2026-07-19T20:55:33.698022+12:00 -->
# ENEL372-26S2 weekly summary

## Coverage

- Week: 2026-W29, from 2026-07-13T00:00:00+12:00 to 2026-07-19T20:52:01.289027+12:00.
- Covered verified summaries:
  - Lecture 1: Introduction to power electronics.
  - Lecture 2: Power, energy storage, periodic steady state, RMS values, and inductors.
  - Lecture 3: Buck converters and continuous-conduction analysis.
- The week progressed from device-level switching principles to converter analysis, then to the ideal buck converter.

## Main concepts

- Power electronics converts and controls electrical power efficiently using semiconductor switches, inductors, and capacitors.
- Ideal switches dissipate little power when fully on or fully off. Real converters still have conduction and switching losses.
- Main conversion categories:
  - AC to DC: rectifier.
  - DC to AC: inverter.
  - DC to DC: voltage-level conversion.
  - AC to AC: conversion through one or more stages.
- Practical converters use feedback to regulate output despite source and load variations.
- Device-selection trade-offs include voltage rating, current rating, switching frequency, drive requirements, conduction loss, switching loss, and controlled turn-off capability.
- Inductors and capacitors store and return energy in ideal operation:
  - Inductors store magnetic-field energy.
  - Capacitors store electric-field energy.
- An inductor’s current cannot change instantaneously. Constant voltage produces a linear current ramp.
- Periodic steady state requires:
  - Zero net change in inductor current per switching period.
  - Zero average inductor voltage, or volt-second balance.
  - Zero average capacitor current, or charge balance.
- RMS values describe the heating or power-producing effect of periodic waveforms and are not interchangeable with average values.
- PWM controls average conversion behaviour by changing the duty ratio.
- A buck converter is a step-down DC–DC converter. Its diode provides the inductor-current path when the controllable switch is off.
- In continuous conduction, inductor current varies but does not reach zero. Discontinuous conduction begins when the minimum current reaches zero.
- The switch/source current can be discontinuous even when the inductor current is continuous.
- An energised inductor must have a deliberate current path when switched off, such as a flyback diode, freewheeling path, clamp, or snubber.

## Equations and worked patterns

- Power balance:
  \[
  P_{\text{input}}=P_{\text{output}}+P_{\text{loss}}
  \]

- Instantaneous power and energy:
  \[
  p(t)=v(t)i(t)
  \]
  \[
  W=\int p(t)\,dt
  \]

- Average power over a period:
  \[
  P_{\text{avg}}=\frac{1}{T}\int_{t_0}^{t_0+T}p(t)\,dt
  \]
  \[
  P_{\text{avg}}=\frac{W_T}{T}=fW_T,\qquad f=\frac{1}{T}
  \]

- Inductor and capacitor relationships:
  \[
  v_L=L\frac{di_L}{dt}
  \]
  \[
  i_C=C\frac{dv_C}{dt}
  \]

- Stored energy:
  \[
  W_L=\frac{1}{2}Li_L^2
  \]
  \[
  W_C=\frac{1}{2}Cv_C^2
  \]

- Periodic steady-state balances:
  \[
  \int_{t_0}^{t_0+T}v_L(t)\,dt=0
  \]
  \[
  \int_{t_0}^{t_0+T}i_C(t)\,dt=0
  \]

- RMS calculation:
  \[
  V_{\text{RMS}}=\sqrt{\frac{1}{T}\int_{t_0}^{t_0+T}v^2(t)\,dt}
  \]
  \[
  I_{\text{RMS}}=\sqrt{\frac{1}{T}\int_{t_0}^{t_0+T}i^2(t)\,dt}
  \]

- Rectangular pulse with amplitude \(V_s\) and duty ratio \(D\):
  \[
  D=\frac{t_{\text{on}}}{T}
  \]
  \[
  V_{\text{avg}}=DV_s
  \]
  \[
  V_{\text{RMS}}=|V_s|\sqrt{D}
  \]

- Buck-converter timing:
  \[
  T_{\text{on}}=DT,\qquad T_{\text{off}}=(1-D)T
  \]

- Buck inductor voltage:
  \[
  v_{L,\text{on}}=V_s-V_{\text{out}}
  \]
  \[
  v_{L,\text{off}}=-V_{\text{out}}
  \]

- Buck inductor-current changes:
  \[
  \Delta i_{L,\text{on}}
  =\frac{(V_s-V_{\text{out}})DT}{L}
  \]
  \[
  \Delta i_{L,\text{off}}
  =-\frac{V_{\text{out}}(1-D)T}{L}
  \]

- Ideal buck derivation pattern:
  1. Write the inductor voltage for each switch state.
  2. Calculate the current change during each interval.
  3. Apply periodic steady state:
     \[
     \Delta i_{L,\text{on}}+\Delta i_{L,\text{off}}=0
     \]
  4. Rearrange to obtain:
     \[
     V_{\text{out}}=DV_s
     \]
     \[
     \frac{V_{\text{out}}}{V_s}=D
     \]

- Continuous-conduction boundary:
  \[
  I_R=\frac{\Delta i_L}{2}
  \]
  at the point where:
  \[
  I_{\min}=0
  \]

- Buck capacitor-current relationship:
  \[
  I_R=i_L-i_C
  \]
  \[
  i_C=i_L-I_R
  \]

- Resistive-load output power:
  \[
  P_{\text{out}}=V_{\text{out}}I_R
  =\frac{V_{\text{out}}^2}{R}
  =I_R^2R
  \]

- Input power for the buck:
  \[
  P_{\text{in}}=V_{s,\text{rms}}I_{s,\text{rms}}
  \]
  For a DC source:
  \[
  V_{s,\text{rms}}=V_s
  \]
  The pulsed source current requires an RMS calculation rather than substitution of its average value.

## Warnings and deadlines

- Lectures move to E16 from the following week. Do not return to the first-lecture room.
- The group design-and-build project is worth 30% and involves a controlled power converter for a small model solar-powered car, in groups of three.
- The invigilated test is worth 35%.
- The exam is worth 35%.
- Lecture 1 stated a 40% average requirement across the invigilated assessments. Confirm the exact wording in the course outline.
- Generative AI is not permitted in the test or exam. Check the course outline for detailed rules covering other assessments.
- A full lecture the following week was expected to cover the project.
- Lecture 3 assigned calculation of the RMS source current as homework. No final closed-form result was provided in the summary.
- Confirm slide-dependent details before relying on them for design or hardware work, especially device capability charts, waveform conventions, diode orientation, and exact RMS expressions.

## Recall questions

1. Why does switching between fully on and fully off reduce semiconductor power dissipation in the ideal model?
2. What is the difference between a rectifier, inverter, and DC–DC converter?
3. Why does a practical converter normally require feedback?
4. How do MOSFETs and BJTs differ in their control inputs?
5. What does inductor volt-second balance mean physically and mathematically?
6. Why can an inductor have non-zero average current even when its net current change over one period is zero?
7. How are the average and RMS values of a positive rectangular pulse related to its duty ratio?
8. What happens to the buck converter’s diode during the switch-on and switch-off intervals?
9. How is the ideal buck relationship \(V_{\text{out}}=DV_s\) derived from the inductor current ramps?
10. Why can source current be discontinuous while buck-converter inductor current remains continuous?

## Practice priorities

1. Draw the buck-converter equivalent circuit for switch-on and switch-off states.
2. Derive \(V_{\text{out}}=DV_s\) using inductor volt-second balance.
3. Sketch the inductor-current, capacitor-current, and switch-current waveforms over one switching period.
4. Calculate inductor-current rise and fall from the applied voltage, interval duration, and inductance.
5. Identify whether operation is continuous or discontinuous from \(I_{\min}\) and the peak-to-peak ripple.
6. Practise RMS calculations for rectangular and pulsed waveforms, especially the buck converter’s source current.
7. Explain the energy path when the buck switch turns off and the diode conducts.
8. Compare diode, MOSFET, BJT, IGBT, SCR, GTO, and triac selection trade-offs qualitatively.
9. Draw a closed-loop converter block diagram including sensor, reference, controller, switching stage, filter, and load.
10. Explain why an energised inductor requires a flyback, freewheeling, clamp, snubber, or equivalent current path.

## Missing or incomplete

- None.

## Source manifest

- Lecture 1 (echo-lecture-1-1): complete; summary `71f2d3d55d3f94b95fb26da795b2d08cd37fe809265679ecbe63fac52f3e6e84`; transcript `bbb49c47d74b496049a0deb37c09fd5d63e1f0723226e26fa94f40e4efdb4a69`; summary path `[local source path redacted]`
- Lecture 2 (echo-lecture-2-2): complete; summary `51c67409849ba32064036a8223f2fdb9661d38c3c3c96c84e45b15167e99e89a`; transcript `0d2b0514e2c9187674f937c7b80c2a72905b24e9a940bd5aafd18dc7b69f08bf`; summary path `[local source path redacted]`
- Lecture 3 (echo-lecture-3-3): complete; summary `8928b31fa3a137d1458b64d067fbc4f4a590d4419fc2fad49365ead37fa9eb8f`; transcript `42868d83e4317bffd258eeb514cfe1b34a3c73c68ae0afe07d922d4a980e19ac`; summary path `[local source path redacted]`

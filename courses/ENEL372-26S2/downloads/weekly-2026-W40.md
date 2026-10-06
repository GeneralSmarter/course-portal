<!-- week-id: 2026-W40 -->
<!-- generated-at: 2026-10-07T11:04:21.447563+13:00 -->
# ENEL372-26S2 weekly summary

## Coverage

Week 2026-W40 covers Lectures 29–31:

- Lecture 29: BLDC motor construction, operation, torque-speed behaviour, commutation, sensing, torque limits, and efficiency.
- Lecture 30: Three-phase inverter switching, Hall sensors, electrical cycles, PWM, waveforms, inductive effects, and sensorless zero-crossing detection.
- Lecture 31: Open-loop operation, commutation timing, sensorless flux estimation, filtering, practical controller hardware, and an introduction to analogue electronics.

No lectures were identified as missing or incomplete.

## Main concepts

- BLDC motors use electronic commutation instead of brushes and a mechanical commutator.
- A typical three-phase BLDC commutation state drives two phases while leaving the third phase floating.
- The floating phase carries no intended current but can provide a measurable back-EMF signal for sensorless position estimation.
- Rotor position can be obtained using Hall-effect sensors, encoders, or electrical estimation from back EMF and rotor flux.
- Correct commutation maintains the stator magnetic field in the correct position relative to the permanent-magnet rotor.
- A four-pole motor has two pole pairs and produces two electrical cycles per mechanical revolution.
- Trapezoidal back EMF is commonly associated with six-step BLDC commutation. Sinusoidal back EMF generally produces lower torque ripple but requires suitable winding and control methods.
- PWM changes the effective average voltage applied to the motor, but motor speed still depends on load, back EMF, commutation timing, and motor characteristics.
- Increasing speed increases back EMF, which reduces available current and therefore reduces torque in the high-speed region.
- Continuous torque is thermally limited. Intermittent torque can be higher, but only for a limited duration.
- The motor operating point is determined by the intersection of the motor torque-speed characteristic and the load characteristic.
- Open-loop control may provide an initial operating command through a duty-cycle-versus-speed lookup table, but it is load-dependent and does not provide complete regulation or protection.
- Commutating too slowly can produce high current, stepped movement, and poor efficiency. Commutating too quickly can prevent rotation, cause loss of synchronism, or produce runaway behaviour.
- Electrical dynamics are faster than mechanical dynamics because rotor inertia delays changes in speed.
- Sensorless flux estimation uses current and voltage measurements with a motor model. Integration can accumulate bias, so filtering is required.
- Low-level motor control handles PWM, commutation, current sensing, and protection. Higher-level control specifies objectives such as maintaining a target speed.
- Analogue systems use continuously varying signals and continuous-time models. A sampled digital system may be approximated as continuous when its sampling interval is sufficiently short relative to the system dynamics.

## Equations and worked patterns

- Motor torque and current:
  
  T ∝ I

  Within the simplified operating region, increasing current increases torque, subject to thermal, saturation, and control limits.

- Electrical efficiency:

  η = P_mechanical,out / P_electrical,in

  or:

  η (%) = 100 × P_mechanical,out / P_electrical,in

- Mechanical output power:

  P_mech = Tω

- Simplified electrical input power:

  P_elec ≈ VI

  Electrical input power exceeds useful mechanical output power when motor and inverter losses are present.

- PWM average-voltage relationship:

  V_avg = D V_in

  Worked pattern from Lecture 30:

  D = 0.5 and V_in = 12 V gives V_avg ≈ 6 V.

  This is an averaged approximation, not a complete prediction of motor speed or current.

- Electrical and mechanical frequency:

  f_e = p f_m

  For a four-pole motor:

  p = 4 / 2 = 2

  Therefore:

  f_e = 2f_m

  and the electrical period is half the mechanical period at the same operating speed.

- Winding electrical time constant:

  τ = L / R

  A larger inductance increases the time required for current to change, while a larger resistance reduces the time constant.

- Back-EMF dependence:

  e ∝ ωB

  The lecture establishes the qualitative dependence on rotor speed and magnetic-field distribution, but does not provide a complete motor-specific equation.

- Integration with bias:

  ∫(f(t) + b) dt = ∫f(t) dt + bt + C

  A constant sensor bias produces a linearly growing error in the integrated signal and can eventually shift or destroy estimated flux zero crossings.

- Torque-speed analysis pattern:

  1. Identify the motor torque-speed characteristic.
  2. Identify the load characteristic.
  3. Find their intersection to determine the operating point.
  4. Check whether that point lies within continuous or intermittent torque limits.
  5. Compare it with the motor’s efficiency region and thermal constraints.

## Warnings and deadlines

- No deadlines or assessment dates are recorded in the supplied lecture summaries.
- Exact inverter switch topologies, phase-state labels, current-arrow conventions, and complete Hall-code sequences should not be reconstructed from the summaries alone.
- The exact definition and inequality associated with the Lecture 31 VE1 timing measure are unclear. Use the reliable principle only: the relative position of the back-EMF zero crossing indicates whether commutation is early or late.
- The approximately 10° filter phase-lead value is an experimentally based rule of thumb, not a universal theoretical requirement.
- Detailed real-motor characterisation procedures were identified as useful background but not examinable in Lecture 29.
- The lecture comments indicate that BLDC commutation, waveform analysis, PWM-related graphing, and idealised torque-speed behaviour are important examinable areas. Exact exam values and duty cycles may vary.

## Recall questions

1. Why does a conventional three-phase BLDC commutation state normally drive two phases and leave one phase floating?
2. How do Hall-effect sensor outputs provide rotor-position information to the microcontroller?
3. How many pole pairs does a four-pole motor have, and how many electrical cycles occur during one mechanical revolution?
4. Why does a floating phase have a measurable voltage even though it carries no intended current?
5. Compare trapezoidal and sinusoidal back EMF in terms of commutation method and torque ripple.
6. How does PWM duty cycle affect the simplified average voltage applied to a BLDC motor?
7. Why does motor torque generally decrease as speed increases in the high-speed region?
8. What problems can result from commutating a BLDC motor too slowly or too quickly?
9. Why can integration of a biased current or voltage measurement corrupt rotor-flux zero crossings?
10. What is the difference between low-level motor commutation control and high-level speed control?

## Practice priorities

1. Draw and explain the six-step three-phase BLDC commutation concept: two conducting phases and one floating phase.
2. Practise relating Hall sensor states to commutation states, while checking exact switch labels against the lecture circuit diagram rather than relying on the transcript summary.
3. Sketch trapezoidal and sinusoidal back-EMF waveforms and explain their relationship to torque ripple and control method.
4. Work PWM average-voltage problems using V_avg = D V_in, then explain why the result does not directly determine speed under changing load.
5. Practise converting between mechanical and electrical frequency for motors with different numbers of pole pairs.
6. Explain the qualitative chain: increasing speed → increasing back EMF → decreasing current → decreasing torque.
7. Analyse the effect of winding inductance when a switch turns off, including continued current, diode conduction, ringing, and voltage transients.
8. Explain how floating-phase zero crossings can support sensorless commutation and why low duty cycle, filtering, noise, and phase delay make this difficult.
9. Compare open-loop lookup-table control, Hall-sensor control, direct back-EMF sensing, and model-based rotor-flux estimation.
10. Practise identifying thermal, mechanical, load, and efficiency constraints when selecting a motor operating point.

## Missing or incomplete

None identified for the requested week. The supplied summaries contain transcript-level uncertainties in exact circuit diagrams, switch-state labels, Hall-code ordering, VE1 definitions, and some filter relationships, but no lecture is marked missing or incomplete.

## Source manifest

- Lecture 29 (echo-lecture-29-29): complete; summary `7158872e1dacaa424456d1e502aa1c1d451970f8c663dc0f4923a3688e03ece5`; transcript `8b375cba7a622a1364a0b7c1119a76f584e671cc3da7d990026a5e661ccd6c23`; summary path `[local source path redacted]`
- Lecture 30 (echo-lecture-30-30): complete; summary `a155dd5f7959f835bcb43f701127bafccb7998d6f888980c75ec966a38e7da0b`; transcript `9269c26c90acd27d8c51a9ec81c0b2d95b58fcb72e74eeb3013c09a28758d1da`; summary path `[local source path redacted]`
- Lecture 31 (echo-lecture-31-31): complete; summary `00e8b4c640572444bdb80008c83f13fdbbd1f6184982a6e0e6a833c1ae5ce835`; transcript `4c70b073673bceab14e01a7cbbf6db81e9fbf0d094f5490b78419ca708b89697`; summary path `[local source path redacted]`

<!-- week-id: 2026-W30 -->
<!-- generated-at: 2026-07-25T00:20:13.197745+12:00 -->
# ENEL372-26S2 weekly summary

## Coverage

Week 2026-W30 covered Lectures 4–6:

- Lecture 4: solar-car project requirements, solar-panel and motor characteristics, buck-converter operation, maximum-power-point control, project workflow, and assessment requirements.
- Lecture 5: continuous and discontinuous conduction, inductor and capacitor sizing, switching-frequency selection, input filtering, component ratings, and practical buck-converter design.
- Lecture 6: MOSFET gate driving, low-side switching, TL494 and CMOS inverter arrangements, PWM polarity, and the introduction of the boost converter.

Coverage interval: 2026-07-20T00:00:00+12:00 to 2026-07-25T00:17:32.686121+12:00.

## Main concepts

- The solar-car propulsion path is:
  solar panel → buck converter → permanent-magnet DC motor.
- The buck converter must keep the solar panel near its maximum-power-point voltage while transferring useful power to the motor.
- Directly connecting the panel to the motor is unsuitable because the panel provides relatively low current at a higher voltage, while the motor requires substantially higher starting current at a lower voltage.
- A buck converter changes the voltage/current combination and acts conceptually as an impedance-matching device.
- The solar-panel maximum power point is near the knee of its nonlinear I–V curve and varies with illumination and temperature.
- Closed-loop control measures panel voltage, compares it with an MPP reference, processes the error through a PI controller, and adjusts PWM duty ratio.
- Continuous conduction mode is preferred because it provides more predictable control behaviour, generally lower current stress, lower noise, and better efficiency than discontinuous conduction mode.
- The worst-case buck-converter design condition often occurs near \(D=0.5\), because \(D(1-D)\) is maximised there.
- Higher switching frequency reduces required inductance and capacitance but increases switching, magnetic, EMI, layout, and thermal challenges. The project guidance was approximately 20–100 kHz.
- An input capacitor is important because the solar panel behaves more like a current source than an ideal voltage source. The capacitor reduces input current and voltage ripple.
- An enhancement-mode N-channel MOSFET requires sufficiently positive \(V_{GS}\) to turn on fully and achieve low \(R_{DS(\text{on})}\).
- Low-side switching simplifies N-channel MOSFET gate drive because the source remains near the panel negative/reference.
- The MOSFET gate behaves approximately as a capacitance, requiring short-duration source and sink current pulses for fast switching.
- A CMOS inverter provides low output impedance in both logic states, but it inverts PWM polarity. An additional inversion may be required.
- The ideal boost converter stores energy in the inductor while the switch is closed and transfers it to the output when the switch opens.

## Equations and worked patterns

- Solar-panel power:
  \[
  P=VI
  \]
  The maximum-power point is where \(VI\) is greatest. [Lecture 4]

- Ideal buck power balance:
  \[
  V_{\text{in}}I_{\text{in}}=V_{\text{out}}I_{\text{out}}
  \]
  A real converter has:
  \[
  P_{\text{out}}=\eta P_{\text{in}}
  \]
  where \(\eta<1\). [Lecture 4]

- Ideal CCM buck voltage relationship:
  \[
  V_{\text{out}}=DV_s
  \]
  [Lecture 5]

- CCM boundary:
  \[
  I_{\text{out}}=\frac{\Delta I_L}{2}
  \]
  Safe CCM operation requires:
  \[
  I_{\text{out}}>\frac{\Delta I_L}{2}
  \]
  [Lecture 5]

- Inductor-current ripple:
  \[
  \Delta I_L=\frac{V_{\text{out}}(1-D)}{Lf_s}
  \]
  [Lecture 5]

- Minimum inductance for CCM:
  \[
  L_{\min}\geq\frac{V_{\text{out}}(1-D)}{2I_{\text{out}}f_s}
  \]
  Using \(V_{\text{out}}=DV_s\):
  \[
  L_{\min}\geq\frac{V_sD(1-D)}{2I_{\text{out}}f_s}
  \]

- Worst case at \(D=0.5\):
  \[
  L_{\min,\text{worst}}\geq\frac{V_s}{8I_{\text{out}}f_s}
  \]
  [Lecture 5]

- Output-voltage ripple approximation:
  \[
  \Delta V_{\text{out}}\approx\frac{\Delta I_L}{8C_{\text{out}}f_s}
  \]
  [Lecture 5]

- Input-voltage ripple approximation:
  \[
  \Delta V_{\text{in}}\approx\frac{I_{\text{out}}D(1-D)}{C_{\text{in}}f_s}
  \]
  At \(D=0.5\):
  \[
  C_{\text{in}}\geq\frac{I_{\text{out}}}{4f_s\Delta V_{\text{in}}}
  \]
  [Lecture 5]

- Lecture 5 design pattern:
  For a 12 V to 8 V, 2 A buck converter at 80 kHz, use \(V_{\text{out}}=DV_s\) to determine duty ratio, then size \(L\), \(C_{\text{out}}\), and \(C_{\text{in}}\) against ripple and CCM requirements. The lecture summary reports guidance of \(L>16.7\,\mu\text{H}\), \(C_{\text{out}}>39\,\mu\text{F}\), and \(C_{\text{in}}>46\,\mu\text{F}\); these values should be checked against the fully worked course solution.

- MOSFET gate-source voltage:
  \[
  V_{GS}=V_G-V_S
  \]
  [Lecture 6]

- Inductor relationship:
  \[
  v_L=L\frac{di_L}{dt}
  \]
  [Lecture 6]

- Boost converter, switch closed:
  \[
  v_{L,\text{on}}=V_S
  \]
  \[
  \Delta i_{L,\text{on}}=\frac{V_SDT}{L}
  \]

- Boost converter volt-second balance:
  \[
  V_SDT+(V_S-V_{\text{out}})(1-D)T=0
  \]

- Ideal boost-converter voltage ratio:
  \[
  V_{\text{out}}=\frac{V_S}{1-D}
  \]
  Increasing \(D\) increases the ideal output voltage. [Lecture 6]

## Warnings and deadlines

- Closed-loop feedback is required for full project marks. Open-loop operation is only a temporary development aid. [Lecture 4]
- Begin hardware development while simulation work is progressing. Delaying construction reduces time available for troubleshooting.
- Breadboards are unsuitable for the final inspection because connections may be intermittent. Use Veroboard or a PCB for the final implementation.
- The final circuit must include an accessible current-probe loop for measuring inductor current.
- The total project capacitance is limited to 350 µF.
- Component voltage, peak-current, RMS-current, saturation-current, ripple-current, and thermal ratings must be checked before construction.
- Avoid operating below approximately 20 kHz because audible switching noise may occur. Frequencies near or above 100 kHz require more careful layout and parasitic management.
- Reported project dates from Lecture 4, to be confirmed against official course information:
  - Simulation submission: Friday 21 August, worth 5%.
  - Group hardware inspection: Wednesday–Friday around 23 September; attendance is compulsory for an inspection mark.
  - Group design report: Monday 12 October, worth 15%.
  - Peer/self-assessment: Tuesday 13 October, according to the lecture sequence.
- The lecture stated restricted AI-use rules for the project: AI may assist with permitted suggestions, construction/testing suggestions, proofreading, editing, or summarising, but must not write the project work or answer inspection questions. Prompts and uses must be declared. Confirm the exact rules in the official assignment instructions.

## Recall questions

1. What is the propulsion power path in the ENEL372 solar car, and what is the separate purpose of the battery?
2. Why does direct connection of the solar panel to the motor fail to provide a suitable operating point?
3. What is the control objective of the closed-loop buck converter: direct motor-voltage regulation, or solar-panel maximum-power-point operation?
4. Why is continuous conduction mode preferred over discontinuous conduction mode for this project?
5. What does \(D(1-D)\) imply about the worst-case duty ratio for inductor-sizing calculations?
6. Why does increasing switching frequency reduce required inductance but create additional practical problems?
7. Why is an input capacitor particularly important when the source is a solar panel?
8. Why is low-side placement simpler for an enhancement-mode N-channel MOSFET than high-side placement?
9. What problem does the CMOS inverter solve in the MOSFET gate-drive circuit, and what new PWM-polarity issue does it introduce?
10. Using the ideal boost relationship, how does increasing duty ratio affect \(V_{\text{out}}\), and what assumptions underlie that relationship?

## Practice priorities

1. Draw the complete solar-car power and control block diagram, including panel-voltage measurement, PI control, PWM generation, gate drive, buck converter, and motor.
2. Explain the panel–converter–motor mismatch using approximate panel and motor voltage/current characteristics.
3. Practise CCM buck calculations:
   - Determine \(D\) from \(V_{\text{out}}=DV_s\).
   - Calculate \(\Delta I_L\).
   - Determine the minimum \(L\).
   - Add design margin above the CCM boundary.
4. Size \(C_{\text{out}}\) for a specified output-ripple target and \(C_{\text{in}}\) for a permitted panel-voltage ripple.
5. Compare switching-frequency choices within the project’s approximate 20–100 kHz guidance, including losses, noise, component size, and layout difficulty.
6. Check MOSFET gate-drive polarity through both the TL494 output stage and CMOS inverter. Verify that the final gate signal has the intended effective duty relationship.
7. Review MOSFET gate charging/discharging, peak driver-current requirements, \(V_{GS}\), and \(R_{DS(\text{on})}\).
8. Derive the ideal boost-converter ratio from inductor volt-second balance and identify the assumptions that make the result idealised.
9. Confirm all reported project dates, component part numbers, AI-use restrictions, and Lecture 5 design-example values against the official course documentation before relying on them.

## Missing or incomplete

None.

## Source manifest

- Lecture 4 (echo-lecture-4-4): complete; summary `a66d4de4837e17d9b104301c89f19c8a477e8a9bca1de1e54d2b1920279cbcca`; transcript `133a6d9e3791eb9f56a0a1b2c90a3caee571e2a5b55abc836b0c0e38ead8fae4`; summary path `[local source path redacted]`
- Lecture 5 (echo-lecture-5-5): complete; summary `b8e52cb33eee7c9e396a14b0f788fb5765231927649841e39c9767479b365f97`; transcript `d4663f84f8b94302ef64deb106254c3fc601ae602cfe963fcac4a9490bd9e4bc`; summary path `[local source path redacted]`
- Lecture 6 (echo-lecture-6-6): complete; summary `d0ac2016f1f64aad3205ed99eea31f322e92e6acb8dcfa76d1fb5d738cd437e3`; transcript `e1ebf4a1684e9685b0a6a2c265d85f3f8bc1cd7a0a26bde2d1fd40c5c1448e0f`; summary path `[local source path redacted]`

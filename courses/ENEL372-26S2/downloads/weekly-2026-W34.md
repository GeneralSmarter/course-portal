<!-- week-id: 2026-W34 -->
<!-- generated-at: 2026-08-23T09:34:26.116077+12:00 -->
# ENEL372-26S2 weekly summary

## Coverage

- Study window: 2026-W34, from 2026-08-17T00:00:00+12:00 to 2026-08-23T06:15:15.739855+12:00.
- Covered verified summaries:
  - Lecture 16: DC–AC converters, inverter topologies, four-quadrant operation, bipolar SPWM, modulation ratios, and practical switching issues.
  - Lecture 17: PWM harmonics, synchronous and asynchronous operation, unipolar switching, over-modulation, switching-frequency trade-offs, and a half-bridge worked example.
  - Lecture 18: power-electronics foundations, converter categories, feedback, semiconductor devices, device-selection trade-offs, and LTspice.
- Source coverage is complete. No lectures are recorded as missing or incomplete.

## Main concepts

- An inverter converts DC into AC. Applications include AC motor speed control, photovoltaic systems, uninterruptible power supplies, battery-powered AC supplies, and Class D amplifiers.
- A motor can be modelled as a series resistance–inductance–back-EMF source load. The inductance prevents current from changing instantaneously, requiring free-wheeling or anti-parallel current paths.
- Buck-like operation transfers energy from the DC source to the motor. Boost-like operation supports regenerative or active-braking energy flow from the motor toward the source or braking path.
- Four-quadrant operation is required for AC or reactive loads because voltage and current can each change sign.
- A half bridge produces approximately \(+V_D/2\) or \(-V_D/2\) relative to its midpoint. A full bridge produces \(+V_D\), \(0\), or \(-V_D\) across the load.
- Bipolar switching changes directly between positive and negative output levels. Unipolar full-bridge switching passes through zero, reducing voltage steps and changing the harmonic distribution.
- SPWM compares a reference waveform with a high-frequency triangular carrier. The resulting switched waveform is filtered to recover the desired fundamental.
- \(M_A\) controls fundamental amplitude in the linear region. \(M_F\) determines the relationship between switching frequency and fundamental frequency, affecting harmonic placement and filter requirements.
- Synchronous PWM uses an integer carrier-to-reference frequency ratio. Non-integer ratios can create subharmonics and low-frequency components.
- Over-modulation increases the fundamental voltage but produces greater low-order harmonic distortion and is therefore more suitable as a temporary torque-demand measure than as a normal continuous mode.
- Power electronics aims to convert electrical power efficiently using semiconductor switches, inductors, capacitors, filters, and feedback control.
- The four basic conversion categories are AC–DC rectification, DC–DC conversion, DC–AC inversion, and AC–AC conversion.
- Device choice involves trade-offs among voltage capability, current capability, switching speed, conduction loss, gate-drive requirements, and controllability. MOSFETs are generally fastest, IGBTs provide a high-current compromise, and thyristors provide high voltage/current capability at lower switching speeds.

## Equations and worked patterns

- Instantaneous electrical power:
  \[
  p=vi
  \]
- Inductor relationship in the motor model:
  \[
  v_L=L_A\frac{di}{dt}
  \]
- Sinusoidal real output power:
  \[
  P_{\text{out}}=V_{\text{out,rms}}I_{\text{out,rms}}\cos\phi
  \]
- Half-bridge output levels:
  \[
  v_{AO}=+\frac{V_D}{2}
  \quad\text{or}\quad
  v_{AO}=-\frac{V_D}{2}
  \]
- Full-bridge output levels:
  \[
  v_{AB}=+V_D,\quad 0,\quad -V_D
  \]
- Amplitude modulation ratio:
  \[
  M_A=\frac{V_{\text{control,peak}}}{V_{\text{tri,peak}}}
  \]
  Linear modulation is described as \(M_A\leq1\); over-modulation begins when \(M_A>1\).
- Frequency modulation ratio:
  \[
  M_F=\frac{f_s}{f_1}
  \]
- Unipolar full-bridge pole relationship:
  \[
  V_{AB}=V_{AN}-V_{BN}
  \]
  with the second control signal:
  \[
  v_{\text{control,B}}=-v_{\text{control,A}}
  \]
- Bipolar harmonic-frequency pattern:
  \[
  f_h=(JM_F\pm K)f_1
  \]
  The exact coefficient expression and detailed harmonic table were not captured, so individual harmonic results should not be reconstructed from these summaries alone.
- Half-bridge fundamental-voltage pattern:
  \[
  V_{1,\text{peak}}=M_A\frac{V_D}{2}
  \]
  \[
  V_{1,\text{rms}}=\frac{V_{1,\text{peak}}}{\sqrt{2}}
  \]
- Worked example from Lecture 17:
  - \(V_D=600\text{ V}\), \(f_s=1450\text{ Hz}\), \(f_1=50\text{ Hz}\), and \(M_A=0.8\).
  - The summary gives \(M_F=29\).
  - The summary gives \(V_{1,\text{peak}}=240\text{ V}\) and \(V_{1,\text{rms}}\approx170\text{ V}\).
- Harmonic RMS conversion:
  \[
  V_{h,\text{rms}}=\frac{A_h(V_D/2)}{\sqrt{2}}
  \]
  The five harmonic amplitudes and final frequencies cannot be determined because the referenced table is absent.
- Power-converter balance and efficiency:
  \[
  P_{\text{in}}=P_{\text{out}}+P_{\text{loss}}
  \]
  \[
  \eta=\frac{P_{\text{out}}}{P_{\text{in}}}
  \]
- Ideal-switch states:
  - Off: \(i_{\text{switch}}=0\).
  - On: \(v_{\text{switch}}=0\).
- Ideal-diode states:
  - Forward biased: \(v_D=0\).
  - Reverse biased: \(i_D=0\).
- N-channel enhancement MOSFET switching condition:
  \[
  V_{GS}<V_{TH}\Rightarrow\text{off}
  \]
  \[
  V_{GS}>V_{TH}\Rightarrow\text{on}
  \]

## Warnings and deadlines

- No specific assessment deadlines were stated in the supplied summaries.
- Lecture 18 records the assessment weighting as a 30% group design-and-build project, 35% test, and 35% exam. It also states that the test and exam average must be at least 40% to pass, and that generative AI is not permitted in the test or exam. Confirm these requirements against the official course outline.
- Lecture 16 contains an internally inconsistent statement about an amplitude-modulation value of approximately “3.3”. The reliable surrounding coverage identifies over-modulation as beginning above \(M_A=1\); do not rely on the “3.3” claim without checking the official slides or recording.
- The harmonic-index notation, harmonic tables, circuit diagrams, and some switch labels are incomplete or uncertain in the source summaries. Do not invent missing harmonic amplitudes, frequencies, or topology details.
- Approximate device values such as diode forward voltage, MOSFET threshold voltage, gate-drive voltage, device voltage ratings, and converter losses are teaching estimates rather than universal specifications.
- Do not treat approximate switching-frequency guidance, such as \(M_F>10\), \(M_F>21\), or \(f_s>20f_{\max}\), as universal design requirements.

## Recall questions

1. What is the difference between bipolar and unipolar switching in a full-bridge inverter?
2. Why does an inductive motor load require free-wheeling or anti-parallel diode paths?
3. What voltage and current sign combinations correspond to quadrants 1–4?
4. How does SPWM use a reference waveform and a triangular carrier to generate an AC output?
5. What do \(M_A\) and \(M_F\) represent, and how does each affect inverter operation?
6. Why is an integer \(M_F\) useful for synchronous PWM, and what problems can arise when the carrier and reference are asynchronous?
7. Why can unipolar switching reduce harmonic content and filter size compared with bipolar switching?
8. What are the benefits and risks of operating an inverter in over-modulation?
9. For the Lecture 17 example, why does \(f_s=1450\text{ Hz}\) and \(f_1=50\text{ Hz}\) correspond to \(M_F=29\), and what does the odd integer indicate in the discussed bipolar case?
10. How do MOSFETs, BJTs, IGBTs, and thyristors differ in control method, switching speed, and typical voltage/current capability?

## Practice priorities

1. Draw and explain half-bridge and full-bridge inverter switching states, including the required dead time and the prohibition on simultaneous complementary-switch conduction.
2. Practise identifying energy flow during forward motor driving, free-wheeling, active braking, and regenerative operation.
3. Work through \(M_A\), \(M_F\), fundamental peak voltage, RMS voltage, and harmonic RMS conversions using the supplied half-bridge example.
4. Compare bipolar and unipolar PWM in terms of voltage-step size, harmonic location, harmonic amplitude, switching frequency, and filter size.
5. Explain why higher switching frequency improves filtering but increases switching loss, thermal demands, and synchronisation difficulty.
6. Review the four converter categories and the generic source–filter–switching converter–filter–load–feedback structure.
7. Build a device-selection comparison for MOSFETs, BJTs, IGBTs, SCRs, GTOs, triacs, and MCTs using voltage, current, speed, conduction loss, and turn-off control.
8. Practise explaining ideal switch and diode models, MOSFET threshold/on-state behaviour, SCR latching, GTO turn-off, and triac bidirectional conduction.
9. Revisit LTspice as the stated simulation tool for testing power-electronic designs before physical construction.

## Missing or incomplete

- No lectures are identified as missing or incomplete for this study window.
- Within otherwise covered lectures, the following source details remain incomplete:
  - Lecture 16’s exact circuit diagrams and some switch labels.
  - Lecture 16’s conflicting “3.3” modulation-ratio statement.
  - Lecture 17’s complete harmonic-amplitude table and the five requested harmonic results.
  - Lecture 17’s exact Fourier coefficient expression and fully precise harmonic-index notation.
  - Lecture 18’s detailed diagrams and quantitative comparisons for multilevel inverter structures and device operating ranges.

## Source manifest

- Lecture 16 (echo-lecture-16-16): complete; summary `170b3e575b5e978de5d5099a33d67b837bb5a48795f9e2a75ae3785a6da18e09`; transcript `f00c63f9e761d39892b73ce41e9851d55d3ae9217a06dde6dfb0123735506307`; summary path `[local source path redacted]`
- Lecture 17 (echo-lecture-17-17): complete; summary `6936473d2975c4f25245311f784c0d90465952343838f434c1a5ed8010a89996`; transcript `d6267ad34b91ed38fa5f0ea77720b0dbdb41cd8cba774758ca488171653661b7`; summary path `[local source path redacted]`
- Lecture 18 (echo-lecture-18-18): complete; summary `d885202fa3c20fe0e8f4b4ec1feb842dd6308419029ede0cfeae8e4b28a8059a`; transcript `b7f49dcda795f436a5e14b54bf227770d18a3d404c9b0e241713d7b2a41e9d8c`; summary path `[local source path redacted]`

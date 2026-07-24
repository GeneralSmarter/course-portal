<!-- week-id: 2026-W30 -->
<!-- generated-at: 2026-07-24T23:43:55.149354+12:00 -->
# ENEL372-26S2 weekly summary

## Coverage

- Week: 2026-W30, from 2026-07-20T00:00:00+12:00 to 2026-07-24T23:41:42.354928+12:00.
- Source available: Lecture 5 summary, focused on practical buck-converter design for the ENEL372 solar car project.
- Lecture 4: missing summary.
- Lecture 6: missing summary.
- No other lecture content is represented in the available source.

## Main concepts

- Continuous conduction mode (CCM) occurs when inductor current remains above zero throughout the switching cycle.
- Discontinuous conduction mode (DCM) occurs when inductor current reaches zero and remains there for part of the cycle.
- The CCM/DCM boundary occurs when the minimum inductor current is zero. For triangular ripple, the boundary condition is approximately:
  - \(I_{\text{out}}=\Delta I_L/2\)
- CCM is preferred because it generally provides:
  - More predictable feedback-control behaviour.
  - Lower peak and RMS currents.
  - Better efficiency.
  - Smaller filtering components.
  - Reduced \(di/dt\), \(dv/dt\), and electrical noise.
- In ideal CCM operation, buck-converter output voltage is approximately proportional to duty ratio.
- In DCM, voltage gain becomes dependent on load current and other circuit parameters, making control more difficult.
- Increasing switching frequency reduces the required inductance and capacitance, but increases switching, magnetic, and thermal losses and makes parasitics and layout more significant.
- The project guidance gives an approximate switching-frequency range of 20–100 kHz:
  - Below approximately 20 kHz, audible switching noise may occur.
  - Around or above approximately 100 kHz, breadboard and Vero-board parasitics become increasingly important.
- Output-capacitor sizing is determined by the permitted output-voltage ripple and the inductor-current ripple.
- An input capacitor reduces the ripple seen by a non-ideal source. This is particularly important for the solar-panel source, which is treated as behaving more like a current source than an ideal voltage source.
- Physical design must account for voltage ratings, peak and RMS currents, inductor saturation, capacitor ripple-current ratings, conduction losses, switching losses, and thermal management.
- The worst-case duty ratio for expressions containing \(D(1-D)\) is approximately \(D=0.5\).

## Equations and worked patterns

- Ideal CCM buck relationship:
  \[
  V_{\text{out}}=DV_s
  \]

- Inductor-current ripple:
  \[
  \Delta I_L\approx\frac{V_{\text{out}}(1-D)}{Lf_s}
  \]

- Equivalent source-voltage form:
  \[
  \Delta I_L\approx\frac{V_sD(1-D)}{Lf_s}
  \]

- Minimum inductance for CCM:
  \[
  L_{\min}\geq\frac{V_{\text{out}}(1-D)}{2I_{\text{out}}f_s}
  \]

- Equivalent source-voltage form:
  \[
  L_{\min}\geq\frac{V_sD(1-D)}{2I_{\text{out}}f_s}
  \]

- Worst-case inductance estimate at \(D=0.5\):
  \[
  L_{\min,\text{worst}}\geq\frac{V_s}{8I_{\text{out}}f_s}
  \]

- Capacitor current and voltage relationship:
  \[
  i_C=C\frac{dv_C}{dt}
  \]
  \[
  \Delta V_C=\frac{1}{C}\int i_C\,dt
  \]

- Approximate output-voltage ripple for triangular capacitor current:
  \[
  \Delta V_{\text{out}}\approx\frac{\Delta I_L}{8C_{\text{out}}f_s}
  \]

- Combined output-ripple expression:
  \[
  \Delta V_{\text{out}}\approx
  \frac{V_{\text{out}}(1-D)}
  {8LC_{\text{out}}f_s^2}
  \]

- Ideal power balance:
  \[
  V_{\text{out}}I_{\text{out}}=V_sI_S
  \]

- Using the ideal buck relationship:
  \[
  I_S=DI_{\text{out}}
  \]

- Input-node current balance:
  \[
  i_C=I_S-i_1
  \]

- Approximate input-voltage ripple:
  \[
  \Delta V_{\text{in}}\approx
  \frac{I_{\text{out}}D(1-D)}
  {C_{\text{in}}f_s}
  \]

- Worst-case input-capacitance estimate at \(D=0.5\):
  \[
  C_{\text{in}}\geq
  \frac{I_{\text{out}}}
  {4f_s\Delta V_{\text{in}}}
  \]

- Worked-design pattern from the lecture:
  - Given \(V_s=12\text{ V}\), \(V_{\text{out}}=8\text{ V}\), \(I_{\text{out}}=2\text{ A}\), and \(f_s=80\text{ kHz}\), first determine duty ratio using the ideal CCM buck relationship.
  - Then select \(L\) to keep the converter safely inside CCM.
  - Select \(C_{\text{out}}\) for the permitted output ripple.
  - Select \(C_{\text{in}}\) for the permitted input ripple.
  - The summary records the stated guidance \(L>16.7\,\mu\text{H}\), \(C_{\text{out}}>39\,\mu\text{F}\), and \(C_{\text{in}}>46\,\mu\text{F}\). These values were not presented as a fully verified worked solution in the source.

## Warnings and deadlines

- No deadlines or assessment dates are stated in the available Lecture 5 summary.
- The summary identifies several equations as reconstructed from local ASR and recommends checking them against the lecture slides or audio before assessment use.
- Capacitor-current sign conventions and voltage-ripple definitions may not be fully reliable in the source.
- The exact recommended switching frequency within the approximate 20–100 kHz range is not stated.
- The lecture’s numerical component values should be checked against the promised fully worked solution on Learn.
- Designing exactly at the CCM/DCM boundary is discouraged. Practical margin is needed for component tolerances, operating variation, and load changes.
- Component ratings must exceed expected operating voltage, peak current, RMS current, ripple-current, and saturation requirements.
- Higher switching frequency can increase losses, noise, layout sensitivity, and thermal-management requirements.

## Recall questions

1. What condition distinguishes CCM from DCM in terms of inductor current?
2. Why does the CCM/DCM boundary correspond to \(I_{\text{out}}=\Delta I_L/2\) for triangular ripple?
3. Give four reasons the lecture prefers CCM over DCM.
4. How does entering DCM affect converter gain and feedback control?
5. Derive the minimum inductance expression required to maintain CCM.
6. Why is \(D=0.5\) the worst-case duty ratio for the \(D(1-D)\) term?
7. What are the main trade-offs when increasing switching frequency?
8. Why does the lecture caution against switching below approximately 20 kHz and above approximately 100 kHz for the project prototype?
9. Why is an input capacitor important when the source is a solar panel or is physically distant from the converter?
10. What voltage, current, ripple-current, saturation, and thermal ratings must be checked before selecting converter components?

## Practice priorities

1. Practise identifying CCM, DCM, and the boundary condition from inductor-current waveforms.
2. Derive and apply the inductor-ripple and minimum-inductance equations.
3. Use \(V_{\text{out}}=DV_s\) to determine duty ratio for ideal CCM buck designs.
4. Evaluate why \(D=0.5\) is used for worst-case component sizing.
5. Size output capacitance from an allowed output-voltage-ripple requirement, while noting the triangular-waveform approximation.
6. Size input capacitance using the simplified solar-panel source model and permitted input-voltage ripple.
7. Compare switching-frequency choices by considering component size, losses, noise, parasitics, and layout.
8. Review the 12 V to 8 V, 2 A, 80 kHz design example, but verify its numerical component values against the course material before relying on them.
9. Check component selection against peak current, RMS current, voltage, saturation, ripple-current, and thermal requirements.

## Missing or incomplete

- Lecture 4: missing_summary.
- Lecture 6: missing_summary.
- Lecture 5 design example: introduced but not fully worked in the source summary.
- Several Lecture 5 equations and capacitor-ripple details are reconstructed from ASR and require verification against slides or audio.

## Source manifest

- Lecture 4 (echo-lecture-4-4): missing_summary; summary `missing`; transcript `missing`; summary path `missing`
- Lecture 5 (echo-lecture-5-5): complete; summary `b8e52cb33eee7c9e396a14b0f788fb5765231927649841e39c9767479b365f97`; transcript `d4663f84f8b94302ef64deb106254c3fc601ae602cfe963fcac4a9490bd9e4bc`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENEL372-26S2/summaries/lecture_05_summary.md`
- Lecture 6 (echo-lecture-6-6): missing_summary; summary `missing`; transcript `missing`; summary path `missing`

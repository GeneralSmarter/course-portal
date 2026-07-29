<!-- week-id: 2026-W31 -->
<!-- generated-at: 2026-07-30T10:29:04.617106+12:00 -->
# ENEL372-26S2 weekly summary

## Coverage

- Weekly window: 2026-07-27T00:00:00+12:00 to 2026-07-30T10:27:19.060131+12:00.
- Source available: Lecture 7 summary.
- Lecture 7 covered boost-converter analysis and design, buck-boost operation, non-ideal switch and passive-component behaviour, and start-up transients.
- The analysis mainly assumed ideal components and steady-state periodic operation. Non-ideal effects and transients were introduced mainly qualitatively.

## Main concepts

- In an ideal boost converter, the output voltage is higher than the input voltage, with conversion ratio \(V_{\text{out}}/V_s=1/(1-D)\).
- The boost inductor is always connected to the input, so its average current corresponds to the source current.
- Continuous conduction requires the minimum inductor current to remain above zero.
- The worst-case boost-converter inductance requirement occurs at \(D=0.5\).
- Discontinuous conduction causes higher peak currents, lower efficiency, greater switch-current requirements, and increased electrical noise. Its possible increase in voltage gain is generally not worth these disadvantages.
- In a boost converter, the output capacitor supplies the load while the switch is conducting, causing output-voltage ripple.
- The conventional buck-boost converter is inverting and can either step voltage magnitude down or up:
  - \(D<0.5\): step-down magnitude
  - \(D=0.5\): equal input and output magnitudes
  - \(D>0.5\): step-up magnitude
- Ideal converter models neglect switch and diode voltage drops, switching times, and component parasitics.
- Conduction losses arise from current through finite resistance or voltage drop. Switching losses arise from simultaneous non-zero voltage and current during transitions.
- Switching losses become more significant as switching frequency increases.
- Capacitor ESR causes voltage drop, heating, power loss, and increased ripple. ESL can contribute to ringing and oscillation.
- Inductor winding resistance reduces boost-converter output voltage, particularly at high duty ratios.
- Soft starting limits start-up current and voltage stress by gradually increasing the duty ratio.

## Equations and worked patterns

- Switching period:
  \[
  T_s=\frac{1}{f_s}
  \]

- Inductor relationship:
  \[
  v_L=L\frac{di_L}{dt}
  \]

- Ideal boost voltage ratio:
  \[
  \frac{V_{\text{out}}}{V_s}=\frac{1}{1-D}
  \]

- Ideal boost power balance:
  \[
  V_sI_s=V_{\text{out}}I_{\text{out}}
  \]
  Therefore:
  \[
  I_s=\frac{I_{\text{out}}}{1-D}
  \]

- Boost inductor-current ripple:
  \[
  \Delta i_L=\frac{V_sD}{f_sL}
  \]
  Derivation pattern: use the switch-on inductor voltage \(V_s\), the interval \(DT_s\), and \(T_s=1/f_s\).

- Boost continuous-conduction boundary:
  \[
  I_s=\frac{\Delta i_L}{2}
  \]
  Continuous operation requires:
  \[
  I_s>\frac{\Delta i_L}{2}
  \]

- Inferred minimum boost inductance for continuous conduction:
  \[
  L>\frac{V_sD(1-D)}{2f_sI_{\text{out}}}
  \]
  The factor \(D(1-D)\) is largest at \(D=0.5\).

- Capacitor current relationship:
  \[
  i_C=C\frac{dv_C}{dt}
  \]

- Approximate boost and buck-boost output-voltage ripple:
  \[
  \Delta V_{\text{out}}\approx\frac{I_{\text{out}}D}{f_sC}
  \]
  Derivation pattern: identify the interval during which the capacitor supplies approximately constant load current, then use \(\Delta v_C=i_C\Delta t/C\).

- Ideal buck-boost voltage ratio:
  \[
  \frac{V_{\text{out}}}{V_s}=-\frac{D}{1-D}
  \]
  The negative sign indicates reversed output polarity.

- Buck-boost output magnitude:
  \[
  |V_{\text{out}}|=V_s\frac{D}{1-D}
  \]

- Buck-boost steady-state inductor balance:
  \[
  |\Delta i_{L,\text{on}}|=|\Delta i_{L,\text{off}}|
  \]

- Conduction loss:
  \[
  P_{\text{cond}}=I_{\text{rms}}^2R
  \]
  More generally:
  \[
  p_{\text{cond}}(t)=v(t)i(t)
  \]

- Switching loss:
  \[
  E_{\text{sw}}=\int v_Q(t)i_Q(t)\,dt
  \]
  \[
  P_{\text{sw,avg}}\approx f_sE_{\text{sw}}
  \]

- Capacitor ESR loss:
  \[
  P_{\text{ESR}}=I_{\text{rms}}^2R_{\text{ESR}}
  \]

- The exact boost-converter equation including inductor winding resistance \(R_L\) was not recoverable from the source. Use only the supported qualitative result: increasing \(R_L\) reduces output voltage, and high duty ratio operation is increasingly limited.

## Warnings and deadlines

- No confirmed course deadlines were included in the available source.
- The approximate 100 kHz switching-frequency recommendation was associated with a solar-car project and was explicitly flagged for confirmation against official course material. Do not treat it as a confirmed requirement.
- The non-ideal buck-converter output equation was reconstructed in the source summary; its exact notation and sign convention should be checked against the lecture slides.
- The capacitor-ripple expressions use the duty-ratio convention stated in the summary; verify the course’s exact convention if applying them in assessed work.
- Do not rely on the unrecovered \(R_L\)-inclusive boost equation without checking the original lecture material.
- Distinguish start-up transients from the later steady-state waveform when interpreting simulations.

## Recall questions

1. Why is the average boost-converter inductor current associated with source current?
2. Derive the boost inductor-current ripple from \(v_L=L\,di_L/dt\).
3. What condition defines the boundary between continuous and discontinuous inductor-current operation?
4. Why is \(D=0.5\) the worst-case duty ratio for the boost inductance requirement?
5. What are the main disadvantages of discontinuous conduction?
6. During which boost-converter interval does the output capacitor supply the load?
7. Why does the conventional buck-boost converter produce reversed output polarity?
8. How does the buck-boost converter behave for \(D<0.5\), \(D=0.5\), and \(D>0.5\)?
9. What is the difference between conduction loss and switching loss?
10. How do ESR, ESL, and soft starting affect practical converter behaviour?

## Practice priorities

1. Derive the boost-converter inductor ripple and continuous-conduction inductance condition.
2. Explain why \(D=0.5\) gives the worst-case inductance requirement.
3. Derive the boost output-capacitor ripple expression from the capacitor current relationship.
4. Derive the ideal buck-boost conversion ratio using inductor volt-second balance.
5. Interpret buck-boost operation across the three duty-ratio regions.
6. Compare conduction-loss and switching-loss mechanisms, including their dependence on switching frequency.
7. Explain how ESR, ESL, and inductor winding resistance alter ideal converter behaviour.
8. Review the distinction between steady-state analysis and start-up transients.

## Missing or incomplete

- Lecture 8: missing_summary.
- The exact boost-converter output-voltage equation including inductor winding resistance was not recoverable.
- The exact notation and sign convention for the reconstructed non-ideal buck-converter equation require verification.
- The project-specific switching-frequency guidance requires confirmation from official course material.

## Source manifest

- Lecture 7 (echo-lecture-7-7): complete; summary `6d8c702723c456f880d5e3d006cbb96c0d4a66d4389165ca7e9e1113cc49aa05`; transcript `5b61fef6d2c2a40d0d6582b1feee2bff80354463b206282deb1746d8b702ff86`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENEL372-26S2/summaries/lecture_07_summary.md`
- Lecture 8 (echo-lecture-8-8): missing_summary; summary `missing`; transcript `missing`; summary path `missing`

<!-- week-id: 2026-W31 -->
<!-- generated-at: 2026-07-30T10:47:53.303938+12:00 -->
# ENEL372-26S2 weekly summary

## Coverage

- Week: 2026-W31, from 2026-07-27T00:00:00+12:00 to 2026-07-30T10:45:03.767182+12:00.
- Source covered: ENEL372-26S2 Lecture 7 summary.
- Lecture 7 completes boost-converter analysis and basic design considerations, introduces the buck-boost converter, and begins non-ideal switch-mode converter behaviour.
- Topics covered include inductor-current continuity, capacitor sizing and ripple, buck-boost conversion, conduction and switching losses, capacitor ESR/ESL, inductor winding resistance, start-up transients, and soft starting.

## Main concepts

- An ideal boost converter increases voltage according to:
  \[
  \frac{V_{\text{out}}}{V_s}=\frac{1}{1-D}
  \]
- The boost-converter inductor remains connected to the input, so its average current corresponds to the source current rather than directly to the output current.
- Boost-converter continuous conduction requires the minimum inductor current to remain above zero. At the boundary:
  \[
  I_{s,\text{avg}}=\frac{\Delta i_L}{2}
  \]
- The worst-case boost inductance requirement occurs at \(D=0.5\), where \(D(1-D)\) is largest.
- Discontinuous conduction causes higher peak currents, greater electrical noise, lower efficiency, and potentially higher switch-current ratings. Its limited benefit is a slightly higher voltage-boosting ratio.
- In a boost converter, the output capacitor supplies the load while the diode is not conducting, causing output-voltage ripple.
- The conventional buck-boost converter is inverting and can either step voltage down or step voltage up:
  - \(D<0.5\): output-voltage magnitude is lower than the input.
  - \(D=0.5\): output and input magnitudes are equal.
  - \(D>0.5\): output-voltage magnitude is higher than the input.
- Ideal converter analysis assumes zero conducting-switch voltage, zero diode forward voltage, instantaneous switching, and ideal inductors and capacitors.
- Conduction loss results from current through a finite device drop or resistance. Switching loss results from simultaneous non-zero switch voltage and current during transitions.
- Conduction losses tend to dominate at lower switching frequencies. Switching losses become increasingly important as switching frequency rises.
- Capacitor ESR causes voltage drop, heating, power loss, and increased ripple. ESL can contribute to ringing and abnormal waveforms through parasitic resonance.
- Inductor winding resistance reduces boost-converter output voltage, particularly at high duty ratios.
- Start-up can produce large voltage and current spikes. Soft starting limits stress by gradually increasing duty ratio from zero.

## Equations and worked patterns

- Switching period:
  \[
  T_s=\frac{1}{f_s}
  \]

- Inductor relationship:
  \[
  v_L=L\frac{di_L}{dt}
  \]

  For approximately constant inductor voltage:
  \[
  \Delta i_L=\frac{v_L}{L}\Delta t
  \]

- Boost inductor-current ripple during switch-on:
  \[
  \Delta i_L=\frac{V_sD}{f_sL}
  \]

- Ideal boost power balance:
  \[
  V_sI_s=V_{\text{out}}I_{\text{out}}
  \]

  Combining this with the ideal boost voltage ratio:
  \[
  I_s=\frac{I_{\text{out}}}{1-D}
  \]

- Boost continuous-conduction inductance condition:
  \[
  L>\frac{V_sD(1-D)}{2f_sI_{\text{out}}}
  \]

  Worked pattern:
  1. Determine \(V_s\), \(D\), \(f_s\), and \(I_{\text{out}}\).
  2. Evaluate the boundary inductance from the expression.
  3. Select an inductance greater than the boundary value so the minimum current remains above zero.
  4. Check the duty ratio near \(D=0.5\), where the requirement is worst.

- Capacitor voltage change:
  \[
  i_C=C\frac{dv_C}{dt}
  \]

  For approximately constant capacitor current:
  \[
  \Delta v_C=\frac{i_C\Delta t}{C}
  \]

- Boost output-voltage ripple:
  \[
  \Delta V_{\text{out}}\approx\frac{I_{\text{out}}D}{f_sC}
  \]

  Worked pattern:
  1. Identify the interval during which the capacitor supplies the load.
  2. Approximate the load current as constant over that interval.
  3. Use the capacitor-current relationship to obtain the ripple magnitude.
  4. Recognise that the approximation assumes sufficiently large capacitance and small voltage change per switching period.

- Ideal buck-boost conversion ratio:
  \[
  \frac{V_{\text{out}}}{V_s}=-\frac{D}{1-D}
  \]

  The negative sign indicates reversed output polarity. The magnitude is:
  \[
  \left|V_{\text{out}}\right|=V_s\frac{D}{1-D}
  \]

  Worked pattern:
  1. Use the switch-closed interval to determine the inductor current increase.
  2. Use the switch-open interval to determine the current decrease.
  3. Apply steady-state inductor volt-second balance.
  4. Interpret the sign separately from the voltage magnitude.

- Conduction loss:
  \[
  p=vi
  \]
  For a resistive model:
  \[
  P_{\text{cond}}=I_{\text{rms}}^2R
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

- The exact boost-converter equation including inductor winding resistance was not recoverable from the source. Use only the supported qualitative result: increasing \(R_L\) reduces output voltage, and the output eventually decreases with increasing duty ratio at high \(D\).

## Warnings and deadlines

- No deadlines or assessment dates were identified in the source summary.
- The exact equation for boost-converter behaviour with inductor series resistance was not clearly captured. Do not rely on an inferred equation without checking the official lecture material.
- The non-ideal buck-converter output-voltage equation was reconstructed in the source summary; its exact notation and sign convention should be checked against the lecture slides.
- The capacitor-ripple expressions use the duty-ratio and interval conventions described in the lecture summary. Confirm the course convention if applying them in assessed work.
- The approximately 100 kHz switching-frequency guidance was mentioned in connection with a solar-car project and should be confirmed against official project requirements before use.
- The non-ideal and start-up sections are mainly qualitative. Detailed transient analysis was identified as outside the lecture’s scope.

## Recall questions

1. Why is the average boost-converter inductor current associated with the source current?
2. Derive the boost inductor-current ripple expression from \(v_L=L\,di_L/dt\).
3. What condition defines the boundary between continuous and discontinuous conduction?
4. Why is \(D=0.5\) the worst-case duty ratio for the boost-converter inductance requirement?
5. During which interval does the boost output capacitor supply the load?
6. Why does the conventional buck-boost converter produce reversed output polarity?
7. What are the voltage-magnitude operating regions for a buck-boost converter when \(D<0.5\), \(D=0.5\), and \(D>0.5\)?
8. What is the difference between conduction loss and switching loss?
9. How do capacitor ESR and ESL affect practical converter waveforms?
10. Why does soft starting reduce converter start-up stress?

## Practice priorities

1. Derive and apply the boost inductor-ripple and continuous-conduction conditions.
2. Explain why the \(D=0.5\) case is the worst case rather than simply memorising it.
3. Derive the boost output-capacitor ripple expression from the capacitor-current relationship.
4. Derive the buck-boost conversion ratio using inductor volt-second balance, including the polarity sign.
5. Classify buck-boost operation as step-down or step-up from the duty ratio.
6. Compare conduction loss and switching loss, including how switching frequency changes their relative importance.
7. Analyse the practical effects of ESR, ESL, and inductor winding resistance.
8. Distinguish steady-state switching waveforms from start-up transients and explain the purpose of soft starting.

## Missing or incomplete

- No lectures were identified as missing or incomplete for this week.
- Within the Lecture 7 source, the exact displayed equation for boost-converter inductor series resistance was not recoverable.
- The exact notation and sign convention for the reconstructed non-ideal buck-converter equation should be verified against the official lecture slides.

## Source manifest

- Lecture 7 (echo-lecture-7-7): complete; summary `6d8c702723c456f880d5e3d006cbb96c0d4a66d4389165ca7e9e1113cc49aa05`; transcript `5b61fef6d2c2a40d0d6582b1feee2bff80354463b206282deb1746d8b702ff86`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENEL372-26S2/summaries/lecture_07_summary.md`

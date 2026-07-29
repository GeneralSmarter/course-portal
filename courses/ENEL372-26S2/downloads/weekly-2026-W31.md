<!-- week-id: 2026-W31 -->
<!-- generated-at: 2026-07-30T10:42:18.620101+12:00 -->
# ENEL372-26S2 weekly summary

## Coverage

- Covered source: Lecture 7 summary, generated 2026-07-30.
- Lecture 7 completed boost-converter analysis and introduced buck-boost converters and non-ideal switch-mode converter behaviour.
- The summary assumes mainly ideal components and steady-state periodic operation. Practical losses and start-up transients were introduced qualitatively.

## Main concepts

- A boost converter raises the output voltage. Its inductor remains connected to the input, so average inductor current corresponds to source current.
- Continuous conduction requires the minimum inductor current to remain above zero. The worst-case boost inductance requirement occurs at \(D=0.5\).
- Discontinuous conduction causes higher peak currents, increased noise, lower efficiency, and greater switch-current requirements. Its limited advantage is a slightly higher boost ratio.
- In a boost converter, the output capacitor supplies the load while the diode is not conducting, causing output-voltage ripple.
- The conventional buck-boost converter is inverting and can either step voltage down or up depending on duty ratio.
- Ideal converter analysis neglects switch and diode drops, switching times, and component parasitics.
- Conduction losses result from finite voltage drop while current flows. Switching losses result from voltage-current overlap during transitions.
- Capacitor ESR causes voltage drop, heating, power loss, and increased ripple. ESL can contribute to ringing and oscillation.
- Inductor winding resistance reduces boost-converter output voltage, especially at high duty ratios.
- Start-up can cause voltage and current spikes. Soft starting reduces stress by gradually increasing duty ratio.

## Equations and worked patterns

- Switching period:
  \[
  T_s=\frac{1}{f_s}
  \]

- Inductor relationship:
  \[
  v_L=L\frac{di_L}{dt}
  \]

- Ideal boost conversion ratio:
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

- Continuous-conduction boundary:
  \[
  I_s=\frac{\Delta i_L}{2}
  \]
  Continuous conduction requires:
  \[
  I_s>\frac{\Delta i_L}{2}
  \]

- Minimum boost inductance condition:
  \[
  L>\frac{V_sD(1-D)}{2f_sI_{\text{out}}}
  \]
  The factor \(D(1-D)\) is largest at \(D=0.5\).

- Boost and buck-boost output-voltage ripple under the lecture’s assumptions:
  \[
  \Delta V_{\text{out}}\approx\frac{I_{\text{out}}D}{f_sC}
  \]

- Ideal buck-boost conversion ratio:
  \[
  \frac{V_{\text{out}}}{V_s}=-\frac{D}{1-D}
  \]
  The negative sign indicates reversed polarity.

- Buck-boost operating regions:
  - \(D<0.5\): output magnitude is less than input magnitude.
  - \(D=0.5\): output and input magnitudes are equal.
  - \(D>0.5\): output magnitude is greater than input magnitude.

- Conduction loss for a resistive model:
  \[
  P_{\text{cond}}=I_{\text{rms}}^2R
  \]

- Switching energy and average switching loss:
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

## Warnings and deadlines

- No assessment deadlines or other deadlines were identified in the Lecture 7 summary.
- The exact boost-converter equation including inductor resistance \(R_L\) was not recoverable. Use only the stated qualitative result unless the official lecture material is checked.
- The non-ideal buck-converter output equation was reconstructed in the source summary, so its exact notation and sign convention should be verified against the lecture slides.
- The approximately 100 kHz switching-frequency recommendation was presented as solar-car project guidance and should be confirmed against official course requirements.
- Detailed start-up transient analysis was outside the lecture’s stated scope.

## Recall questions

1. Why is average boost-converter inductor current associated with source current rather than directly with output current?
2. Derive the boost inductor-current ripple expression from \(v_L=L\,di_L/dt\).
3. What condition defines the boundary between continuous and discontinuous inductor-current operation?
4. Why is \(D=0.5\) the worst-case duty ratio for the boost inductance requirement?
5. Why does the boost output capacitor supply the load during part of the switching period?
6. Why does the conventional buck-boost converter produce reversed output polarity?
7. What are the operating differences between \(D<0.5\), \(D=0.5\), and \(D>0.5\) in a buck-boost converter?
8. What is the difference between conduction loss and switching loss?
9. Why do switching losses become more significant as switching frequency increases?
10. How do ESR, ESL, and soft starting affect practical converter behaviour?

## Practice priorities

1. Derive the boost-converter inductor ripple and continuous-conduction inductance condition step by step.
2. Explain the boost converter’s current paths during switch-on and switch-off intervals.
3. Derive the ideal buck-boost voltage ratio using inductor volt-second balance.
4. Classify buck-boost operation as step-down or step-up for several duty ratios around \(D=0.5\), while tracking polarity.
5. Derive the output-voltage ripple approximation from \(i_C=C\,dv_C/dt\).
6. Compare conduction-loss and switching-loss mechanisms, including how switching frequency changes their relative importance.
7. Explain how ESR, ESL, and inductor winding resistance cause non-ideal behaviour.
8. Review the assumptions behind the ideal steady-state equations and identify where they stop being reliable.

## Missing or incomplete

- Lecture 8: missing_summary.
- The Lecture 7 source notes that the exact boost-converter equation including inductor series resistance \(R_L\) was not captured clearly.
- The exact notation and sign convention for the reconstructed non-ideal buck-converter equation should be verified against official lecture slides.

## Source manifest

- Lecture 7 (echo-lecture-7-7): complete; summary `6d8c702723c456f880d5e3d006cbb96c0d4a66d4389165ca7e9e1113cc49aa05`; transcript `5b61fef6d2c2a40d0d6582b1feee2bff80354463b206282deb1746d8b702ff86`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENEL372-26S2/summaries/lecture_07_summary.md`
- Lecture 8 (echo-lecture-8-8): missing_summary; summary `missing`; transcript `missing`; summary path `missing`

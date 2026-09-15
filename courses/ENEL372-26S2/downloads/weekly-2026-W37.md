<!-- week-id: 2026-W37 -->
<!-- generated-at: 2026-09-15T15:21:41.309810+12:00 -->
# ENEL372-26S2 weekly summary

## Coverage

This week covers Lectures 19–21, focused on rectifiers and AC-to-DC power conversion.

Topics include:

- Rectifiers, inverters, and practical power-conversion chains.
- Aircraft electrical power: 115 V RMS, 400 Hz AC converted to approximately 28 V DC and then inverted back to single-phase AC.
- Three-phase, six-phase, and 12-pulse rectification.
- Ripple, filtering, load regulation, and rectifier performance.
- Average and RMS waveform analysis.
- Rectifier effectiveness or efficiency.
- Ripple factor.
- AC-side current distortion, harmonics, THD, and power factor.
- Half-wave and full-bridge rectifier circuits and waveforms.

## Main concepts

- A rectifier converts AC to DC. An inverter converts DC to AC.
- Rectified output is generally pulsating rather than perfectly constant DC. The unwanted time-varying component is ripple.
- Increasing supply frequency or rectifier pulse number increases ripple frequency, making filtering easier and potentially allowing smaller filter components.
- A three-phase system has phases separated by 120°. The six-phase arrangement described adds three phases shifted by 30° and produces 12 output pulses per input period.
- In the aircraft example, rectification allows energy storage in the battery system. The stored DC is later converted back to AC for an AC-driven vertical gyro.
- A half-wave rectifier conducts during one input half-cycle and blocks the other. It has substantial ripple and uses only part of the available waveform.
- A full-bridge rectifier routes both source half-cycles through the load in the same direction, producing full-wave rectification.
- For a resistive load, output current follows the voltage waveform through \(i(t)=v(t)/R\).
- Rectifier quality must be considered on both sides:
  - DC side: average output, RMS output, ripple, regulation, and useful DC power.
  - AC side: input current distortion, harmonics, phase displacement, THD, and power factor.
- A sinusoidal supply voltage can produce a distorted, non-sinusoidal input current because diode conduction is nonlinear.
- Rectifier effectiveness compares useful DC power with total power associated with the rectified waveform. It is not identical to physical conversion efficiency including component losses.
- Detailed bridge current-flow sequencing in the LTspice simulation was stated to be non-examinable; metric calculations and waveform plots were emphasised as examinable.

## Equations and worked patterns

Sinusoidal voltage:

\[
v(t)=V_m\sin(\omega t)
\]

\[
\omega=2\pi f
\]

RMS and peak voltage:

\[
V_{\text{RMS}}=\frac{V_m}{\sqrt{2}}
\]

\[
V_m=\sqrt{2}V_{\text{RMS}}
\]

Worked values:

- \(115\ \text{V RMS}\rightarrow V_m\approx162.6\ \text{V}\)
- \(230\ \text{V RMS}\rightarrow V_m\approx325\ \text{V}\)

Period:

\[
T=\frac{1}{f}
\]

For 400 Hz:

\[
T=2.5\ \text{ms}
\]

Angular-variable substitution:

\[
\sigma=\omega t,\qquad dt=\frac{d\sigma}{\omega}
\]

One cycle becomes:

\[
0\leq\sigma\leq2\pi
\]

For a half-wave rectifier, the conducting interval is:

\[
0\leq\sigma\leq\pi
\]

Average value:

\[
V_{\text{avg}}=\frac{1}{T}\int_0^T v(t)\,dt
\]

For an ideal half-wave-rectified sinusoid:

\[
V_{\text{avg}}=\frac{V_m}{\pi}
\]

RMS value:

\[
V_{\text{RMS}}=
\sqrt{\frac{1}{T}\int_0^T v^2(t)\,dt}
\]

Ideal half-wave output:

\[
v_D(t)=
\begin{cases}
V_m\sin(\omega t), & 0<\omega t<\pi\\
0, & \pi<\omega t<2\pi
\end{cases}
\]

Ripple decomposition:

\[
v_{\text{ripple}}(t)=v(t)-V_{\text{avg}}
\]

\[
V_{\text{RMS}}^2
=
V_{\text{avg}}^2+
V_{\text{ripple,RMS}}^2
\]

Ripple factor:

\[
r=\frac{V_{\text{ripple,RMS}}}{V_{\text{avg}}}
\]

\[
r=
\frac{\sqrt{V_{\text{RMS}}^2-V_{\text{avg}}^2}}
{V_{\text{avg}}}
\]

For a perfectly constant DC output, \(V_{\text{RMS}}=V_{\text{avg}}\), so \(r=0\).

Resistive-load power:

\[
P_{\text{DC}}=\frac{V_{\text{avg}}^2}{R}
\]

\[
P_{\text{total}}=\frac{V_{\text{RMS}}^2}{R}
\]

Rectifier effectiveness or efficiency for the resistive-load waveform:

\[
\eta_{\text{rect}}
=
\frac{P_{\text{DC}}}{P_{\text{total}}}
=
\frac{V_{\text{avg}}^2}{V_{\text{RMS}}^2}
\]

The half-wave example gave approximately:

\[
\eta\approx0.41
\]

Practical diode drop:

\[
V_{\text{out,peak}}\approx V_{\text{s,peak}}-V_D
\]

The representative diode drop was approximately \(0.8\ \text{V}\). In the bridge model, two diodes conduct in series:

\[
V_{F,\text{total}}\approx2(0.8)=1.6\ \text{V}
\]

Total harmonic distortion:

\[
\mathrm{THD}
=
\frac{I_{\text{harmonics,RMS}}}{I_{1,\text{RMS}}}
\]

\[
I_{\text{harmonics,RMS}}
=
\sqrt{I_{\text{RMS}}^2-I_{1,\text{RMS}}^2}
\]

Real power for sinusoidal voltage and current:

\[
P=V_{\text{RMS}}I_{\text{RMS}}\cos\phi
\]

Bridge conduction pattern stated in the lecture:

- \(V_S>0\): \(D_1\) and \(D_2\) conduct.
- \(V_S<0\): \(D_3\) and \(D_4\) conduct.
- The load current remains in the same direction during both source half-cycles.

## Warnings and deadlines

- No deadlines or assessment dates were stated in the supplied summaries.
- Waveform drawing was repeatedly identified as important for examination preparation.
- The stated examinable focus is rectifier metrics, circuit diagrams, and voltage/current waveform plots.
- The detailed current-flow sequence in the LTspice bridge simulation was explicitly described as not examinable.
- Confirm exact bridge-diode orientation and node labels against the lecture slides because the supplied summaries do not contain the original diagrams.
- Confirm the exact terminology for “half-bridge” versus the described single-diode half-wave circuit.
- The \(0.8\ \text{V}\) diode drop applies to the simplified LTspice model discussed, not automatically to every physical diode.
- The six-phase topology and 12-pulse derivation were described conceptually; do not infer an unshown diode arrangement.
- Use approximately \(325\ \text{V}\) as the peak of \(230\ \text{V RMS}\), consistent with \(V_m=\sqrt{2}V_{\text{RMS}}\). The Lecture 19 summary records an inconsistent approximate value of 315 V in the transcript.
- Distinguish rectifier effectiveness, a waveform-quality measure, from ordinary efficiency including physical losses.
- The complete formal THD and total-power-factor development was not fully preserved in the source summaries.

## Recall questions

1. What is the difference between a rectifier and an inverter?
2. Why does increasing rectifier pulse number make filtering easier?
3. How does the aircraft power chain use rectification, battery storage, and inversion to power the vertical gyro?
4. What does a quoted value such as 115 V AC normally represent?
5. Why does a half-wave rectifier produce a poor-quality DC output?
6. What is the purpose of the capacitor in an RC-filtered rectifier?
7. How are average voltage, RMS voltage, and ripple voltage related?
8. What is the difference between rectifier effectiveness and ordinary circuit efficiency?
9. Why can a rectifier draw distorted current from a sinusoidal AC supply?
10. Which diode pair conducts in the full-bridge rectifier for \(V_S>0\) and \(V_S<0\)?

## Practice priorities

1. Draw the ideal half-wave rectifier and its source voltage, diode current, load current, and load-voltage waveforms.
2. Draw the four-diode full-bridge rectifier and its full-wave output waveform.
3. Practise converting between RMS and peak sinusoidal voltage.
4. Calculate average and RMS values using \(\sigma=\omega t\) over \(0\) to \(2\pi\).
5. Derive and apply the half-wave result \(V_{\text{avg}}=V_m/\pi\).
6. Calculate ripple RMS voltage and ripple factor from average and total RMS output values.
7. Calculate rectifier effectiveness for a resistive load.
8. Explain how load resistance affects capacitor discharge, output fluctuation, and regulation.
9. Identify the fundamental and harmonic components of a distorted input current and calculate THD from RMS values.
10. Compare half-wave, three-phase, and six-phase rectification in terms of pulse count and filtering burden.

## Missing or incomplete

None. All lectures listed for 2026-W37 were supplied.

The summaries still record source limitations within the lectures: original circuit diagrams and waveform figures were not included, some displayed equations and exact notation were unclear, and the complete total-power-factor derivation was not preserved.

## Source manifest

- Lecture 19 (echo-lecture-19-19): complete; summary `b728470d4843bd4786b57d7abe743925138388f8fe8f6372f9135d0145e31c44`; transcript `49b13577c4e85f108a200a2ecff53a12c5203465aa0840e3b98eb59bd9ca5fc4`; summary path `[local source path redacted]`
- Lecture 20 (echo-lecture-20-20): complete; summary `8ad8cfb24553a31011231b6cf2c24762f3911d60c5ca073848c3fef94056f3b9`; transcript `812d34ee0a99abd759b1f466942c1ddd47ae78effaf90ade8eef755fb2be48e0`; summary path `[local source path redacted]`
- Lecture 21 (echo-lecture-21-21): complete; summary `a85b7e23d3c335ce523ad905710a96a4e5c3c73e1330f3feda98eaa055feee8f`; transcript `e6383746ab9941f9a0750a38c4b62d665d9505a2730bc3b231d8869c22238c5d`; summary path `[local source path redacted]`

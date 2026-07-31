<!-- week-id: 2026-W31 -->
<!-- generated-at: 2026-07-31T19:00:42.370100+12:00 -->
# ENEL372-26S2 weekly summary

## Coverage

- Week: 2026-W31
- Period: 2026-07-27T00:00:00+12:00 to 2026-07-31T18:57:33.094939+12:00
- Sources covered:
  - Lecture 7: boost and buck-boost converters, non-ideal components, losses, and start-up behaviour.
  - Lecture 8: magnetic materials, hysteresis, eddy currents, and magnetic circuits.
  - Lecture 9: practical power-inductor design using magnetic-circuit relationships.
- Coverage status: complete.

## Main concepts

- A boost converter increases output voltage according to the ideal continuous-conduction relationship \(V_{\text{out}}/V_s=1/(1-D)\). Its inductor current is associated with the source current.
- Continuous conduction requires the minimum inductor current to remain above zero. The worst-case boost inductance requirement occurs at \(D=0.5\).
- A buck-boost converter can step the voltage magnitude up or down, but the conventional topology inverts output polarity.
- Real converters experience conduction loss, switching loss, capacitor ESR/ESL effects, and inductor winding-resistance losses.
- Soft starting limits start-up current and voltage stress by gradually increasing the duty ratio.
- Magnetic domains align under an applied magnetising force. Saturation occurs when further increases in \(H\) produce little additional \(B\).
- Hysteresis and eddy currents are important magnetic-core loss mechanisms. Ferrite reduces eddy-current loss through its relatively poor electrical conductivity; steel commonly uses laminations.
- A magnetic circuit is analogous to an electrical circuit:
  - MMF corresponds to voltage or EMF.
  - Reluctance corresponds to resistance.
  - Magnetic flux corresponds to current.
- Air gaps dominate reluctance when used with high-permeability ferrite cores. They also store most of the magnetic energy in a gapped power inductor.
- Power-inductor design links converter requirements to core flux density, turns, conductor size, winding fit, reluctance, and air-gap length.
- Design should remain below the absolute saturation limit to provide construction and parameter-variation margin.

## Equations and worked patterns

- Boost voltage ratio:
  \[
  \frac{V_{\text{out}}}{V_s}=\frac{1}{1-D}
  \]

- Boost source-current relationship under ideal power balance:
  \[
  I_s=\frac{I_{\text{out}}}{1-D}
  \]

- Inductor-current ripple during the switch-on interval:
  \[
  \Delta i_L=\frac{V_sD}{f_sL}
  \]

- Boost continuous-conduction boundary:
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

- Ideal inverting buck-boost voltage ratio:
  \[
  \frac{V_{\text{out}}}{V_s}=-\frac{D}{1-D}
  \]
  Thus \(D<0.5\) gives step-down magnitude, \(D=0.5\) gives equal magnitudes, and \(D>0.5\) gives step-up magnitude.

- Non-ideal buck-converter output relationship as reconstructed in Lecture 7:
  \[
  V_{\text{out}}=V_sD-DV_Q-(1-D)V_D
  \]
  The exact notation and sign convention should be checked against the official lecture material.

- Conduction loss:
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

- Magnetic-circuit relationships:
  \[
  \text{MMF}=NI
  \]
  \[
  \Phi=\frac{NI}{\mathcal{R}}
  \]
  \[
  B=\frac{\Phi}{A}
  \]
  \[
  L=\frac{N^2}{\mathcal{R}}
  \]

- Turns-area design pattern:
  \[
  (NA)_{\min}=\frac{LI_{\max}}{B_{\max}}
  \]
  \[
  N_{\min}=\frac{(NA)_{\min}}{A_E}
  \]
  Round the selected number of turns up to a practical integer.

- Representative Lecture 9 calculation:
  - \(I_{\text{avg}}=1\text{ A}\)
  - \(\Delta I_L=200\text{ mA}\)
  - \(I_{\max}=1+0.2/2=1.1\text{ A}\)
  - \(L=1\text{ mH}\)
  - \(B_{\max}=0.3\text{ T}\)
  - \((NA)_{\min}\approx3.7\times10^{-3}\text{ turn}\cdot\text{m}^2\)
  - \(A_E=63\text{ mm}^2\)
  - \(N_{\min}\approx58.2\) turns, so the lecture selected \(N=60\) turns.
  These values are illustrative and were not stated to be the student-project values.

- Conductor-sizing pattern:
  \[
  J=\frac{I_{\text{RMS}}}{A_{\text{wire}}}
  \]
  Using the lecture’s approximate \(5\text{ A/mm}^2\) guideline:
  \[
  A_{\text{wire}}\geq\frac{I_{\text{RMS}}}{5}
  \]
  For \(1\text{ A RMS}\), the minimum area is approximately \(0.2\text{ mm}^2\), corresponding to a round-wire diameter of approximately \(0.5\text{ mm}\).

- Reluctance and air-gap pattern:
  \[
  \mathcal{R}_{\text{required}}=\frac{N^2}{L}
  \]
  For \(N=60\) and \(L=1\text{ mH}\):
  \[
  \mathcal{R}_{\text{required}}=3.6\times10^6\text{ A-turns/Wb}
  \]
  For two equivalent air gaps:
  \[
  \mathcal{R}\approx\frac{2l_g}{\mu_0A_E}
  \]
  \[
  l_g=\frac{\mathcal{R}\mu_0A_E}{2}
  \]
  The representative result was approximately \(142\,\mu\text{m}\) per gap.

## Warnings and deadlines

- No deadlines were identified in the supplied lecture summaries.
- The exact boost-converter equation including inductor winding resistance \(R_L\) was not recoverable. Only its qualitative effect is source-backed: increasing \(R_L\) reduces output voltage, especially at high duty ratio.
- The non-ideal buck-converter output equation was reconstructed from the lecture summary and should be checked against official course material.
- Lecture 7 mentions an approximately \(100\text{ kHz}\) switching-frequency recommendation for a solar-car project, but the summary explicitly says this should be confirmed against the project requirements.
- The Lecture 8 E-core reluctance expression depends on the exact gap geometry and notation. Check the components handout or official diagram before hardware design.
- Lecture 9’s \(5\text{ A/mm}^2\) conductor rule is a simplified guideline, not a complete thermal or winding-design calculation.
- Final inductor construction also requires checking insulation, packing, winding-window fit, thermal conditions, core data, and the applicable saturation limit.
- The representative Lecture 9 numerical values are illustrative and should not be assumed to be the project specifications.

## Recall questions

1. Why is the average boost-converter inductor current associated with the source current?
2. Derive the boost-converter current-ripple expression from \(v_L=L\,di_L/dt\).
3. What condition defines the boundary between continuous and discontinuous conduction?
4. Why is \(D=0.5\) the worst-case duty ratio for the boost-converter inductance requirement?
5. Why does the conventional buck-boost converter produce reversed output polarity?
6. How do conduction loss and switching loss differ, and why does switching loss become more significant at higher \(f_s\)?
7. What are residual flux density, coercive force, and hysteresis loss?
8. Why does an air gap dominate the reluctance of a ferrite-core inductor?
9. Starting from \(\Phi=NI/\mathcal{R}\) and Faraday’s law, derive \(L=N^2/\mathcal{R}\).
10. Why must the calculated minimum number of turns be rounded up, and what physical checks follow the turns calculation?

## Practice priorities

- Derive the boost-converter continuous-conduction inductance condition and identify the worst-case duty ratio.
- Compare boost and buck-boost operation across duty ratios below, equal to, and above \(0.5\).
- Explain the practical effects of switch drops, diode drops, ESR, ESL, winding resistance, and switching frequency.
- Sketch or describe the \(B\)-\(H\) curve and hysteresis loop, including saturation, residual flux density, and coercive force.
- Convert between magnetic-circuit quantities using:
  \[
  \text{MMF}=NI,\quad \Phi=\frac{NI}{\mathcal{R}},\quad B=\frac{\Phi}{A}
  \]
- Work through the full inductor-design sequence:
  1. Determine \(L\), ripple current, and \(I_{\max}\).
  2. Select \(B_{\max}\).
  3. Calculate \((NA)_{\min}\).
  4. Determine and round up \(N\).
  5. Size the conductor using current density.
  6. Check winding fit.
  7. Calculate required reluctance.
  8. Determine the air-gap length.
- Rework the representative Lecture 9 design with altered \(L\), \(I_{\max}\), \(B_{\max}\), and \(A_E\), while keeping units consistent.
- Verify any project-specific core, switching-frequency, gap, thermal, and winding requirements from official course documentation before construction.

## Missing or incomplete

- No lectures were identified as missing or incomplete for this week.
- Some source details remain incomplete within the supplied summaries, notably:
  - The exact boost-converter winding-resistance equation.
  - The exact official notation for the reconstructed non-ideal buck equation.
  - The precise E-core gap geometry and notation.
  - Full project-specific component, thermal, and winding specifications.

## Source manifest

- Lecture 7 (echo-lecture-7-7): complete; summary `6d8c702723c456f880d5e3d006cbb96c0d4a66d4389165ca7e9e1113cc49aa05`; transcript `5b61fef6d2c2a40d0d6582b1feee2bff80354463b206282deb1746d8b702ff86`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENEL372-26S2/summaries/lecture_07_summary.md`
- Lecture 8 (echo-lecture-8-8): complete; summary `b4778c696e7a31abcc442afbc7d9f06360c29a4d435f4adea529e577c0a2a868`; transcript `359249241d80e34e50bfffb9ad7e6424070c80ae877f59af8ad93225670ac626`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENEL372-26S2/summaries/lecture_08_summary.md`
- Lecture 9 (echo-lecture-9-9): complete; summary `56a4047bb4e090406b11c41353221a87c7cc5b077c3a3d02a36886807d92bc16`; transcript `818b941a4284e46d88fcd929b52cfb9a94e28dd93ccad280b20a2ed6455447bc`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENEL372-26S2/summaries/lecture_09_summary.md`

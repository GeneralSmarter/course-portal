<!-- week-id: 2026-W31 -->
<!-- generated-at: 2026-07-31T12:10:08.920359+12:00 -->
# ENEL372-26S2 weekly summary

## Coverage

- Week: 2026-W31, covering 2026-07-27T00:00:00+12:00 to 2026-07-31T12:07:17.712755+12:00.
- Sources covered:
  - Lecture 7: boost and buck-boost converters, non-ideal components, losses, and start-up behaviour.
  - Lecture 8: magnetic materials, magnetic circuits, hysteresis, eddy currents, and reluctance.
  - Lecture 9: practical power-inductor design using core, winding, saturation, and air-gap constraints.
- All listed lectures are represented by verified summary files.

## Main concepts

- A boost converter raises output voltage according to the ideal continuous-conduction ratio \(V_{\text{out}}/V_s=1/(1-D)\).
- Boost-converter continuous conduction requires the minimum inductor current to remain above zero. The worst-case inductance requirement occurs at \(D=0.5\).
- The boost output capacitor supplies the load while the diode is not conducting, causing output-voltage ripple.
- The inverting buck-boost converter can step voltage up or down in magnitude:
  - \(D<0.5\): step-down magnitude.
  - \(D>0.5\): step-up magnitude.
  - Output polarity is opposite to the input.
- Real switches, diodes, capacitors, and inductors introduce voltage drops, conduction losses, switching losses, ESR, ESL, winding resistance, heating, and waveform distortion.
- Soft starting reduces start-up current and voltage stress by gradually increasing duty ratio.
- Magnetic domains align under an applied magnetising force. Excessive alignment leads to magnetic saturation.
- Hysteresis and eddy currents are the two core-loss mechanisms explicitly discussed.
- Magnetic circuits use the analogy:
  - MMF corresponds to voltage or EMF.
  - Reluctance corresponds to resistance.
  - Magnetic flux corresponds to current.
- Air gaps dominate the reluctance when high-permeability ferrite is used. They also store most of the magnetic energy in a gapped inductor.
- Power-inductor design must satisfy both electrical requirements and physical constraints:
  - Required inductance and peak current.
  - Maximum flux density.
  - Core area and magnetic path.
  - Wire current density and winding fit.
  - Required air-gap length.

## Equations and worked patterns

- Boost-converter voltage ratio:
  \[
  \frac{V_{\text{out}}}{V_s}=\frac{1}{1-D}
  \]

- Boost inductor-current ripple:
  \[
  \Delta i_L=\frac{V_sD}{f_sL}
  \]

- Boost continuous-conduction condition:
  \[
  I_s>\frac{\Delta i_L}{2}
  \]

- Inferred minimum boost inductance:
  \[
  L>\frac{V_sD(1-D)}{2f_sI_{\text{out}}}
  \]
  The factor \(D(1-D)\) is largest at \(D=0.5\).

- Boost and buck-boost output-voltage ripple under the stated assumptions:
  \[
  \Delta V_{\text{out}}\approx\frac{I_{\text{out}}D}{f_sC}
  \]

- Ideal inverting buck-boost ratio:
  \[
  \frac{V_{\text{out}}}{V_s}=-\frac{D}{1-D}
  \]

- Magnetic flux and flux density:
  \[
  \Phi=BA
  \]
  \[
  B=\mu_0\mu_rH
  \]

- Magnetic-circuit relationships:
  \[
  \text{MMF}=NI
  \]
  \[
  \Phi=\frac{NI}{\mathcal{R}}
  \]
  \[
  \mathcal{R}=\frac{l}{\mu_0\mu_rA}
  \]

- Inductance from magnetic reluctance:
  \[
  L=\frac{N^2}{\mathcal{R}}
  \]

- Turns-area design:
  \[
  (NA)_{\min}=\frac{LI_{\max}}{B_{\max}}
  \]
  \[
  N_{\min}=\frac{(NA)_{\min}}{A_E}
  \]
  Round the selected number of turns up to a practical integer.

- Representative inductor design pattern:
  - \(I_{\text{avg}}=1\text{ A}\)
  - \(\Delta I_L=200\text{ mA}\)
  - \(I_{\max}=1.1\text{ A}\)
  - \(L=1\text{ mH}\)
  - \(B_{\max}=0.3\text{ T}\)
  - \(A_E=63\text{ mm}^2\)
  - \((NA)_{\min}\approx3.7\times10^{-3}\text{ turn}\cdot\text{m}^2\)
  - \(N_{\min}\approx58.2\), so the lecture selected \(N=60\) turns.

- Wire sizing guideline:
  \[
  J=\frac{I_{\text{RMS}}}{A_{\text{wire}}}
  \]
  Using \(J\approx5\text{ A/mm}^2\):
  \[
  A_{\text{wire}}\geq\frac{I_{\text{RMS}}}{5}
  \]
  For a circular conductor:
  \[
  A_{\text{wire}}=\frac{\pi d^2}{4}
  \]

- Required reluctance:
  \[
  \mathcal{R}_{\text{required}}=\frac{N^2}{L}
  \]

- Two-gap approximation:
  \[
  \mathcal{R}\approx\frac{2l_g}{\mu_0A_E}
  \]
  \[
  l_g=\frac{\mathcal{R}\mu_0A_E}{2}
  \]
  The representative design produced approximately \(l_g=142\,\mu\text{m}\) per gap.

## Warnings and deadlines

- No deadlines were stated in the three source summaries.
- The Lecture 9 numerical values are explicitly representative and are not necessarily the student project values.
- The exact boost-converter equation including inductor winding resistance was not recoverable from the Lecture 7 source.
- The reconstructed non-ideal buck-converter equation and the capacitor-ripple expressions should be checked against official course material before being used for final design work.
- The approximately \(100\text{ kHz}\) switching-frequency recommendation was described as project-specific guidance and should be confirmed against the official project requirements.
- The Lecture 8 E-core reluctance expression depends on the exact core drawing, gap placement, and notation.
- The \(5\text{ A/mm}^2\) wire-current-density value is a simplified guideline, not a complete thermal or winding-design analysis.
- Final inductor construction requires confirmation of core datasheet conditions, saturation behaviour, temperature, insulation, winding window, and packing constraints.
- Design below the absolute saturation limit. Lecture 9 used approximately \(300\text{ mT}\) rather than the stated approximate \(320\text{ mT}\) saturation-related value to provide headroom.

## Recall questions

1. Why is the average inductor current in a boost converter associated with the input current?
2. What condition separates continuous from discontinuous inductor-current operation?
3. Why is \(D=0.5\) the worst-case duty ratio for the boost-converter inductance requirement?
4. How does the duty ratio determine whether an inverting buck-boost converter steps voltage up or down in magnitude?
5. What is the difference between conduction loss and switching loss?
6. Why can an air gap dominate the reluctance of a ferrite-core inductor?
7. What do MMF, reluctance, and magnetic flux correspond to in the electrical-circuit analogy?
8. Why must a power-inductor design remain below magnetic saturation?
9. Starting from \(L=N^2/\mathcal{R}\), how is the minimum turns-area product obtained?
10. Why must the selected number of turns and conductor diameter be checked against the available winding window?

## Practice priorities

1. Derive the boost-converter ripple and continuous-conduction inductance condition from \(v_L=L\,di_L/dt\).
2. Compare boost and buck-boost operation across different duty ratios, including polarity and output-voltage magnitude.
3. Explain how switching frequency changes the relative importance of conduction and switching losses.
4. Sketch or describe a \(B\)-\(H\) hysteresis loop, identifying saturation, residual flux density, coercive force, and hysteresis loss.
5. Use \(\Phi=NI/\mathcal{R}\), \(B=\Phi/A\), and \(L=N^2/\mathcal{R}\) to connect winding current, flux density, inductance, and core geometry.
6. Repeat the representative inductor-design sequence:
   - Determine peak current.
   - Calculate \((NA)_{\min}\).
   - Determine and round up \(N_{\min}\).
   - Size the conductor from current density.
   - Check winding fit.
   - Calculate required reluctance.
   - Calculate the air-gap length.
7. Practise identifying which quantities are project requirements and which Lecture 9 values are illustrative only.
8. Review the practical consequences of ESR, ESL, winding resistance, start-up transients, and insufficient saturation margin.

## Missing or incomplete

- No lectures are missing or incomplete for this week.
- Lecture 7 contains an unrecoverable exact equation for boost-converter performance with inductor winding resistance.
- Lecture 8 does not complete the specific inductor-design procedure; that procedure is developed in Lecture 9.
- Several exact expressions and project-specific design details should be verified against official course material before hardware construction.

## Source manifest

- Lecture 7 (echo-lecture-7-7): complete; summary `6d8c702723c456f880d5e3d006cbb96c0d4a66d4389165ca7e9e1113cc49aa05`; transcript `5b61fef6d2c2a40d0d6582b1feee2bff80354463b206282deb1746d8b702ff86`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENEL372-26S2/summaries/lecture_07_summary.md`
- Lecture 8 (echo-lecture-8-8): complete; summary `b4778c696e7a31abcc442afbc7d9f06360c29a4d435f4adea529e577c0a2a868`; transcript `359249241d80e34e50bfffb9ad7e6424070c80ae877f59af8ad93225670ac626`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENEL372-26S2/summaries/lecture_08_summary.md`
- Lecture 9 (echo-lecture-9-9): complete; summary `56a4047bb4e090406b11c41353221a87c7cc5b077c3a3d02a36886807d92bc16`; transcript `818b941a4284e46d88fcd929b52cfb9a94e28dd93ccad280b20a2ed6455447bc`; summary path `C:/Users/marco/Documents/Hermes/UC/courses/ENEL372-26S2/summaries/lecture_09_summary.md`

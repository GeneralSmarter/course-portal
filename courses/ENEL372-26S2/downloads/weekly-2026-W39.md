<!-- week-id: 2026-W39 -->
<!-- generated-at: 2026-10-07T10:48:51.340165+13:00 -->
# ENEL372-26S2 weekly summary

## Coverage

Lectures 25–28 were reviewed.

The week covered rectifier filter design, three-phase diode-bridge operation, average output voltage, ripple and continuous-conduction analysis, start-up transients, waveform interpretation, THD, LTspice examination preparation, and the introduction of brushless DC motors.

No lectures were identified as missing or incomplete.

## Main concepts

- Analytical inductor sizing is approximate because the simplified derivation treats the second harmonic as the dominant current-ripple component and neglects higher harmonics. Lecture 25 compared an analytical value of approximately 0.21 with an LTspice value of approximately 0.23.
- Increasing inductance reduces current ripple. Increasing capacitance reduces voltage ripple. Both changes lower the natural frequency of an LC-type filter.
- An insufficiently damped second-order LCR filter can exhibit a resonant peak or pass-band ripple.
- In a three-phase six-diode bridge, the upper diode connected to the highest instantaneous phase voltage and the lower diode connected to the lowest instantaneous phase voltage conduct. The other four diodes are reverse biased.
- A single-phase full-wave rectifier produces two output-voltage pulses per supply cycle, whereas a three-phase six-pulse rectifier produces six DC-side pulses.
- Three-phase rectification produces a dominant sixth-harmonic ripple, making the output easier to filter than the second-harmonic ripple of a single-phase full-wave rectifier.
- A balanced three-phase rectifier uses line-to-line voltages. The average output voltage can therefore exceed the peak of an individual phase-to-neutral voltage.
- A constant-current load is a useful approximation when an inductor sufficiently smooths the load current. A constant-voltage load can approximate an RC load when its capacitance is sufficiently large and its voltage ripple is small.
- Continuous conduction requires the inductor current to remain above zero. In discontinuous conduction, the inductor current reaches zero for part of the cycle.
- Source inductance produces finite current slopes, commutation effects, and voltage drops or notches.
- Increasing supply frequency while leaving the filter unchanged moves the ripple further above the filter cutoff frequency, increasing attenuation and reducing ripple.
- LTspice is useful for developing waveform intuition and checking results, but examination waveforms must be derived and sketched manually. Simulations should be allowed to reach steady state before their waveforms are used.
- BLDC motors use electronic commutation instead of mechanical brushes and commutators. A typical arrangement has permanent magnets on the rotor and controlled windings on the stator.
- Back EMF increases with speed. At low speed, back EMF is small, so current can become large and cause winding heating.
- A motor-load system reaches steady state where the motor torque-speed curve intersects the load torque-speed curve.
- Fan or propeller torque increases approximately with the square of speed, while a hoisting load has a substantial speed-independent torque component associated with gravity.
- Regenerative braking operates the motor as a generator so that mechanical energy can be returned to electrical storage.

## Equations and worked patterns

- Balanced three-phase line-to-line RMS voltage:

  \(V_{LL} = \sqrt{3}V_s\)

- Sinusoidal peak and RMS conversion:

  \(V_{\mathrm{peak}} = \sqrt{2}V_{\mathrm{rms}}\)

  \(V_{\mathrm{rms}} = V_{\mathrm{peak}}/\sqrt{2}\)

- Ideal three-phase six-pulse rectifier average output voltage:

  \(V_{d,\mathrm{avg}} = \frac{3\sqrt{2}}{\pi}V_{LL} \approx 1.35V_{LL}\)

  The derivation uses a line-to-line waveform, a shifted time origin, and waveform symmetry to integrate only a suitable portion of the rectified waveform.

- Dominant ripple frequency of a three-phase six-pulse rectifier:

  \(\omega_6 = 6\omega\)

  \(f_6 = 6f\)

  For a 60 Hz supply, \(f_6 = 360\ \mathrm{Hz}\).

- Fourier-series sixth-harmonic coefficient pattern:

  \(A_6 = \frac{1}{\pi}\int_0^{2\pi}v(\theta)\cos(6\theta)\,d\theta\)

  The lecture used symmetry to obtain \(B_6=0\). The exact numerical sixth-harmonic amplitude was uncertain in the source and should not be memorised without checking the original material.

- Inductor impedance at the sixth harmonic:

  \(|Z_{L,6}| = 6\omega L\)

- Approximate sixth-harmonic current ripple:

  \(I_{6,\mathrm{peak}} \approx \frac{V_{6,\mathrm{peak}}}{6\omega L}\)

- Approximate continuous-conduction condition:

  \(I_{6,\mathrm{peak}} < I_D\)

  If the ripple amplitude reaches or exceeds the average DC current, the instantaneous current can reach zero and conduction becomes discontinuous.

- Inductor voltage-current relationship:

  \(v_L = L\,di_L/dt\)

- Second-order filter roll-off:

  Approximately \(-40\ \mathrm{dB}\) per decade beyond the cutoff frequency, subject to topology and damping.

- Mechanical motor power:

  \(P_{\mathrm{mech}} = T\omega\)

- Motor efficiency:

  \(\eta = P_{\mathrm{out}}/P_{\mathrm{in}}\)

- Steady-state motor-load condition:

  \(T_{\mathrm{motor}} = T_{\mathrm{load}}\)

- Approximate fan or propeller load:

  \(T_{\mathrm{load}} \propto \omega^2\)

- BLDC relationships discussed qualitatively:

  \(E_{\mathrm{back}} \propto \omega\)

  \(T \propto I\)

Worked pattern for rectifier analysis:

1. Identify whether the requested waveform is on the AC/source side or DC/rectifier-output side.
2. Identify the relevant phase or line-to-line voltages.
3. Determine whether conduction is continuous or discontinuous by checking whether inductor current reaches zero.
4. Use the correct pulse count: two for a single-phase full-wave output and six for a three-phase six-pulse DC output.
5. For ripple analysis, identify the dominant harmonic and use the corresponding inductor impedance.
6. Sketch qualitative ripple, commutation transitions, and steady-state behaviour rather than copying an initial transient.

## Warnings and deadlines

- No formal assignment or assessment deadline was stated in these summaries.
- Examination preparation is emphasised. Students should be able to calculate the average three-phase rectifier output voltage, design or derive the inductance condition for continuous conduction, discuss surges, compare waveforms, and sketch principal waveforms.
- The detailed diode-by-diode switching sequence was described as useful for understanding but not directly examinable in full.
- Do not confuse AC-side source-current waveforms with DC-side six-pulse output waveforms when counting pulses.
- “Two cycles” means two complete supply periods, not two rectifier pulses.
- Do not draw a completely flat DC voltage when inductive smoothing is specified unless the idealisation explicitly justifies it. A small ripple should normally remain.
- LTspice will not be available in the examination. It is a learning and verification aid, not a substitute for manual derivation and sketching.
- Allow simulations to reach steady state before interpreting waveforms. Initial transients may distort the result.
- Check current-probe orientation in LTspice because a reversed probe can display the negative of the intended current.
- Several numerical values and exact waveform labels in the source summaries were uncertain. In particular, verify the sixth-harmonic numerical amplitude, exact source-voltage interpretation, minimum-inductance formula, and detailed circuit labels against the original slides or simulation files.
- BLDC examination weighting was described as approximate and uncertain. The conceptual material on commutation, back EMF, torque-speed curves, load matching, and regenerative braking is supported by the summary.

## Recall questions

1. Why does the analytical inductor-sizing result underestimate the inductor required by a more complete simulation?
2. How are the conducting diode pair selected in a three-phase six-diode bridge?
3. Why does a three-phase six-pulse rectifier have a dominant sixth-harmonic ripple?
4. Derive or explain \(V_{d,\mathrm{avg}} \approx 1.35V_{LL}\) for an ideal three-phase bridge.
5. What condition distinguishes continuous from discontinuous inductor conduction?
6. How does increasing supply frequency affect ripple when the LCR filter components are unchanged?
7. Why must AC-side source-current pulse counts be distinguished from DC-side rectifier-output pulse counts?
8. Why can a BLDC motor supplied from a DC battery be treated as an AC machine?
9. Why can low-speed operation produce excessive BLDC motor current and heating?
10. How is the steady-state operating point found from motor and load torque-speed curves?

## Practice priorities

1. Practise manually sketching single-phase and three-phase rectifier waveforms for both continuous and discontinuous conduction.
2. Label whether each requested waveform is an AC-side source current, DC-side inductor current, rectifier output voltage, or DC-link voltage.
3. Derive the average output voltage of the ideal three-phase six-pulse rectifier using line-to-line voltage and symmetry.
4. Practise identifying the sixth harmonic and using it to estimate inductor current ripple.
5. Apply the continuous-conduction condition and explain how increasing inductance changes the waveform.
6. Compare single-phase and three-phase rectifiers in terms of pulse count, ripple frequency, output smoothness, source-current shape, and qualitative THD.
7. Explain the effects of source inductance, capacitive filtering, start-up resistance, and initial transients.
8. Use LTspice only to check understanding: reverse probe signs when necessary, adjust graph limits, and wait for steady state.
9. For BLDC motors, practise explaining electronic commutation, back EMF, torque-current behaviour, motor-load intersection, fan loads, hoisting loads, and regenerative braking.
10. Avoid memorising uncertain numerical examples or incomplete formulas without confirming them against the original lecture resources.

## Missing or incomplete

None identified.

## Source manifest

- Lecture 25 (echo-lecture-25-25): complete; summary `dde47e2ee9f392802b60f3117410ca736e4242bb7f51bca03bb2ae6010cdbc18`; transcript `3cc15b9f1ccd8956ef89eea3f8e9f22a88619d0187fc2cf4616d4eadc0b53c10`; summary path `[local source path redacted]`
- Lecture 26 (echo-lecture-26-26): complete; summary `5b80df91e14d5a7f2ef80b445093e7a6f4528f812dc7d1e6a76320b3aaf927b6`; transcript `2805329b36f685460dbb099b7976306e8f067b8e410803861967438f304a2eb4`; summary path `[local source path redacted]`
- Lecture 27 (echo-lecture-27-27): complete; summary `8673592983ac9029f73c4a6fd10e9e6b0e4b5df182f6ad3d989d8f1d4e7f534f`; transcript `adf4b2f13e2434ab596af748641233039567664d48bf0a98004a06d9b5929f23`; summary path `[local source path redacted]`
- Lecture 28 (echo-lecture-28-28): complete; summary `aa3fe4bbe2abba3eadaea96cdb3002455c86b3748dd20c7a888cc9fb1cd33373`; transcript `98c83ac940120b96a5cb57941c86449d09b2da69847809cddf146fcc1aad3808`; summary path `[local source path redacted]`

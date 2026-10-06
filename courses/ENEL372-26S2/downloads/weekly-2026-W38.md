<!-- week-id: 2026-W38 -->
<!-- generated-at: 2026-10-07T10:45:15.613571+13:00 -->
# ENEL372-26S2 weekly summary

## Coverage

- Study week: 2026-W38, from 2026-09-14T00:00:00+12:00 to 2026-09-20T23:59:00+12:00.
- Sources covered:
  - Lecture 22: full-bridge rectifiers, smoothing, rectifier metrics, THD, power factor, FFT interpretation, and harmonic limits.
  - Lecture 23: constant-current rectifier loads, Fourier symmetry, THD, source inductance, and commutation.
  - Lecture 24: single-phase full-bridge rectifiers with LCR loads, conduction modes, ripple harmonics, inductor sizing, and capacitor-sizing principles.

## Main concepts

- A full-bridge rectifier uses both AC half-cycles and keeps the load-current direction unchanged. Two diodes conduct in each half-cycle.
- Practical diode drops matter much more in low-voltage systems than in high-voltage systems.
- Capacitive smoothing mainly reduces voltage ripple. Inductive smoothing mainly reduces current ripple.
- A large load inductance can approximate a constant-current load. The AC-side current then approaches a square wave containing mainly odd harmonics.
- A constant-voltage rectifier load generally produces a more distorted input current than the ideal constant-current case.
- THD depends on waveform shape and relative harmonic content, not on absolute amplitude or frequency when the waveform shape is unchanged.
- Source inductance makes diode commutation occur over a finite interval. It creates current-transition slopes, modifies the rectifier voltage, and may reduce THD in a particular operating condition.
- A rectifier should not rely on an assumed grid source inductance to satisfy harmonic limits because source impedance varies between installations.
- An LCR load behaves conceptually as a second-order low-pass filter.
- Continuous conduction occurs when inductor current remains above zero. Discontinuous conduction can cause abrupt voltage changes, transients, and ringing.
- For a single-phase full-wave rectifier, the lowest non-DC DC-side ripple frequency is twice the supply frequency. This is distinct from the odd-harmonic structure of a square-like AC-side current.
- Harmonic standards require each relevant harmonic limit to be checked individually.

## Equations and worked patterns

- Practical full-bridge peak estimate:
  
  Vout,peak ≈ |Vs,peak| − 2Vd

  With Vd ≈ 0.8 V per conducting diode, the total conducting-path drop is approximately 1.6 V. The lecture’s simplified 12 V example gives approximately 10.4 V, but the voltage convention must be confirmed before applying it.

- Source short-circuit current relationship:
  
  Isc ≈ Vs / (ωLs)

  The exact peak or RMS convention depends on the model being used.

- Total RMS current from harmonic RMS components:
  
  Irms = √(I1,rms² + I2,rms² + I3,rms² + ...)

- THD calculation:
  
  γ = Irms / I1,rms
  
  THD = √(γ² − 1)

  Use consistent RMS quantities for total current and fundamental current.

- Sinusoidal amplitude conversion:
  
  Irms = Ipeak / √2

- Ideal constant-current full-bridge waveform:
  
  Irms = ID
  
  B1 = 4ID / π
  
  I1,rms = 2√2 ID / π
  
  γ = π / (2√2) ≈ 1.11
  
  THD ≈ 0.48

  The load-current magnitude ID cancels from γ, so the ideal-model THD is independent of ID.

- Source-inductance relationship:
  
  vL = LS di/dt

  Finite source inductance limits the rate of current change and produces a finite commutation interval.

- Full-wave rectifier ripple frequency:
  
  fripple = 2fsupply

  Examples: 50 Hz gives 100 Hz ripple; 60 Hz gives 120 Hz ripple; 400 Hz gives 800 Hz ripple.

- Average DC current for a resistive load:
  
  ID = VD / R

- Approximate continuous-conduction condition:
  
  I2,peak < ID

  The second-harmonic ripple-current peak must remain smaller than the average DC current so that the total inductor current does not reach zero.

- Inductor sizing pattern:
  1. Determine the average DC current.
  2. Identify the dominant second-harmonic voltage ripple.
  3. Determine the corresponding ripple-current amplitude using the inductor impedance.
  4. Increase L until I2,peak < ID.
  
  The lecture example produced approximately L > 0.21 H under its stated idealised assumptions. This is not a universal design value.

## Warnings and deadlines

- No deadlines were identified in the supplied lecture summaries.
- Practise rectifier waveform plotting, analytical THD calculations, Fourier symmetry, RMS-versus-amplitude interpretation, and source-inductance effects.
- MATLAB coding itself was described as not examinable, but FFT interpretation and THD calculations may be assessed.
- LTspice is a learning and analysis aid, not a substitute for hand-reproducible exam calculations.
- FFT analysis should use a steady-state periodic waveform section containing an integer number of cycles.
- Do not confuse FFT amplitudes, Fourier coefficients, peak values, and RMS values.
- The constant-voltage numerical THD value reported in Lecture 23 is inconsistent in the source summary and should not be memorised without checking the official notes or simulation output.
- The detailed LCR differential-equation derivation in Lecture 24 was explicitly stated to be not examinable.
- The exact capacitor-sizing equation was not recoverable from the supplied summary; use the official lecture notes for formal calculations.
- Harmonic compliance requires checking every relevant harmonic, not only the third harmonic.

## Recall questions

1. Why does a full-bridge rectifier maintain the same load-current direction during both AC half-cycles?
2. Why are diode forward-voltage drops proportionally more significant in low-voltage systems?
3. How do capacitive and inductive smoothing differ in the quantity they primarily reduce?
4. Why does an ideal constant-current full-bridge rectifier draw an approximately square-wave current from the AC source?
5. Why does the ideal constant-current rectifier have mainly odd harmonics and no even harmonics?
6. Why does the load-current magnitude cancel from the ideal constant-current THD calculation?
7. How does source inductance change diode commutation and the AC-side current waveform?
8. Why should DC-side second-harmonic ripple not be confused with AC-side odd current harmonics?
9. What does the condition I2,peak < ID mean physically?
10. Why can discontinuous conduction produce transients and ringing in a practical rectifier?

## Practice priorities

1. Draw the voltage and current waveforms for an ideal full-bridge rectifier with:
   - A constant-voltage load.
   - An inductively smoothed constant-current load.
   - Non-zero source inductance.
   - An LCR load with discontinuous conduction.
2. Derive the ideal constant-current waveform’s fundamental RMS current using symmetry.
3. Calculate γ and THD from total RMS and fundamental RMS currents.
4. Identify the fundamental and odd harmonic frequencies in a square-like AC current waveform.
5. Interpret FFT results while maintaining consistent RMS units.
6. Explain qualitatively why source inductance can reduce high-frequency harmonic content.
7. Distinguish AC-side metrics from DC-side metrics.
8. Calculate full-wave rectifier ripple frequency for different supply frequencies.
9. Apply the approximate condition I2,peak < ID to an inductor-sizing problem.
10. Review the official notes for the exact capacitor-sizing relationship and the harmonic-limit table before assessment work.

## Missing or incomplete

- None of the lectures listed for this week were identified as missing or incomplete.
- Some exact equations, waveform labels, numerical assumptions, and capacitor-sizing details require confirmation from the official lecture notes because they were not fully recoverable in the supplied summaries.

## Source manifest

- Lecture 22 (echo-lecture-22-22): complete; summary `5ba7e86f68e5618a9d30afd3c967779e80c9445b35d3161c1337dfef4a0ee2ff`; transcript `0ee0234d50e7e41e799d997c81447e4f7da0e4608abeea95ee59ee31951d36c3`; summary path `[local source path redacted]`
- Lecture 23 (echo-lecture-23-23): complete; summary `1813dfa2275d6ccb7e15595135324766161535b065caa8fbc8865a3f92fe49c8`; transcript `bdd28b8b33ff13e87b76a1775fbb1ad9e96d0e4d95c4d2f1fdd114e3c6a46d1a`; summary path `[local source path redacted]`
- Lecture 24 (echo-lecture-24-24): complete; summary `78430ab658e7c6a73b6febcf230715a5bc2ca5a1f4b72c972f5e22e39887b614`; transcript `44a1fb411290542a7a6ee5914fd015c5ca0f0bec482a5625c2c3a096268ab613`; summary path `[local source path redacted]`

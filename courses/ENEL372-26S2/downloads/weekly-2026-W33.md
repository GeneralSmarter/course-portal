<!-- week-id: 2026-W33 -->
<!-- generated-at: 2026-08-23T09:46:38.083206+12:00 -->
# ENEL372-26S2 weekly summary

## Coverage

- Covered Lecture 13: motor–mechanical-load matching, torque–speed operating points, gearbox selection, four-quadrant operation, dynamic performance, inertia reflection, and motor-selection considerations.
- Covered Lecture 14: brushed DC motor modelling, buck-converter drive, nested torque/current, speed, and position loops, PI current control, pole-zero cancellation, gain, bandwidth, and phase margin.
- Covered Lecture 15: nested-loop bandwidth design, speed-loop PI control, optional position-loop control, and solar-car panel-voltage control using a buck converter and TL494.
- Study period: 2026-08-10T00:00:00+12:00 to 2026-08-16T06:15:07.630075+12:00.

## Main concepts

- Motor and load torque–speed curves must be matched through a suitable operating point, often using a gearbox.
- A continuous steady-state operating point occurs where motor torque equals the opposing load torque.
- A single intersection with a relatively large intersection angle is preferred for stable operation.
- Motor selection must consider starting torque, continuous torque, efficiency, voltage, current, speed, thermal limits, and gearbox compatibility.
- Increasing motor speed increases back EMF and reduces the current available within the rated-voltage limit.
- Four-quadrant operation allows motoring and braking in both directions of rotation.
- Dynamic acceleration depends on residual torque and total effective inertia, not only on the steady-state torque–speed intersection.
- Maximum load acceleration occurs when motor inertia referred to the load side equals the load inertia.
- In a nested control system, the current/torque loop is fastest, the speed loop is slower, and the position loop is slowest.
- Motor torque can be controlled through armature-current feedback because torque is proportional to armature current in the simplified brushed DC motor model.
- Integral action is required when a non-zero control output must be maintained at zero steady-state error.
- The current-loop PI zero is selected to cancel the motor’s electrical pole in the simplified model.
- Outer-loop bandwidths must be substantially lower than the bandwidths of the loops inside them.
- The solar-car control variable is solar-panel voltage, adjusted through the buck-converter duty ratio to target the maximum-power-point voltage.

## Equations and worked patterns

- Motor and load steady-state matching:
  \[
  T_M(\omega)=T_L(\omega)
  \]

- Gearbox relationships using the lecture’s stated convention:
  \[
  \omega_L=\frac{\omega_M}{N},\qquad T_L=NT_M
  \]

- Load-side total inertia and acceleration:
  \[
  J_{\mathrm{total}}=N^2J_M+J_L
  \]
  \[
  \frac{d\omega_L}{dt}
  =\frac{NT_M}{N^2J_M+J_L}
  =\frac{T_M}{NJ_M+\frac{J_L}{N}}
  \]

- Optimum gearbox ratio:
  \[
  N^2J_M=J_L,\qquad
  N_{\mathrm{opt}}=\sqrt{\frac{J_L}{J_M}}
  \]

- Translating mass represented as rotational inertia:
  \[
  v=\omega r,\qquad J_{\mathrm{equivalent}}=mr^2
  \]

- Brushed DC motor relationships:
  \[
  T_M=KI_A,\qquad E_A=K\omega_M
  \]
  \[
  V_{BO}-E_A=R_AI_A+L_A\frac{dI_A}{dt}
  \]
  \[
  I_A(s)=\frac{V_{BO}(s)-E_A(s)}{R_A+sL_A}
  \]
  \[
  \tau_A=\frac{L_A}{R_A}
  \]

- Buck-converter model:
  \[
  V_{BO}=DV_S
  \]

- PI controller and current-loop pole-zero cancellation:
  \[
  G_{PI}(s)=K_P+\frac{K_I}{s}
  \]
  \[
  \frac{K_P}{K_I}=\frac{L_A}{R_A}
  \]

- Mechanical dynamics:
  \[
  J\frac{d\omega}{dt}=T_M-T_L
  \]
  \[
  \frac{\Omega(s)}{T_{\mathrm{res}}(s)}=\frac{1}{Js}
  \]

- Nested-loop bandwidth pattern:
  \[
  f_{c,i}\approx\frac{f_{\mathrm{sw}}}{10},\qquad
  f_{c,\omega}\approx\frac{f_{\mathrm{sw}}}{100},\qquad
  f_{c,\theta}\approx\frac{f_{\mathrm{sw}}}{1000}
  \]
  For a 20 kHz switching frequency, the stated successive one-tenth rule gives approximately 2 kHz current bandwidth, 200 Hz speed bandwidth, and 20 Hz position bandwidth.

- Position-loop relationship:
  \[
  \omega=\frac{d\theta}{dt},\qquad
  \frac{\Theta(s)}{\Omega(s)}=\frac{1}{s}
  \]
  For the normalised position-loop model:
  \[
  G_{\mathrm{OL}}(s)=\frac{K_P}{s},\qquad K_P=\omega_c
  \]

- Solar-panel integral control:
  \[
  T_I=R_1C,\qquad K_I=\frac{1}{R_1C}
  \]
  If proportional action is added:
  \[
  K_P=\frac{R_2}{R_1}
  \]

## Warnings and deadlines

- No deadlines or assessment dates were stated in the supplied lecture summaries.
- The gearbox-ratio convention and associated inertia equations should be checked against the course slides before assessed use.
- Lecture 13 reports a throwing-arm result of \(r=0.63\,\mathrm{m}\), but the full derivation and assumptions were not included.
- The exact gearbox expression for referring load inertia to the motor side was not clearly stated in Lecture 14.
- The current-loop gain expressions in Lecture 15 are given only proportionally; omitted factors and controller conventions should be checked against the lecture material.
- Lecture 15 contains an inconsistency: the successive one-tenth bandwidth rule gives a 20 Hz position bandwidth for a 20 kHz switching frequency, whereas 200 Hz is also mentioned as a possible position bandwidth. The 200 Hz value corresponds to the speed-loop bandwidth after two reductions.
- Pole-zero cancellation, unity-gain inner-loop approximations, and the stated 45° phase-margin design are simplified models. Real converter delays, sampling, saturation, sensor dynamics, parameter variation, and unmodelled poles may change the result.
- The solar-car values of approximately 5 V for the TL494 reference, approximately 17 V for panel voltage under some conditions, and \(T_I\approx0.1\)–\(0.5\,\mathrm{s}\) should be checked against the actual hardware and datasheet.

## Recall questions

1. Why is a gearbox commonly used between an electric motor and a mechanical load?
2. What condition defines a continuous steady-state motor–load operating point?
3. Why is a large intersection angle between motor and load torque–speed curves desirable?
4. Why can a motor be able to drive a load while already rotating but fail to start it from standstill?
5. What gearbox-ratio condition maximises load acceleration?
6. Why can armature current be used as a substitute for direct torque measurement in the brushed DC motor model?
7. Why is the torque/current loop faster than the speed loop, and why is the position loop slower than both?
8. Why is integral action required in the current and speed controllers?
9. What is the purpose of placing the PI zero at the motor electrical pole?
10. Why does the solar-car controller regulate panel voltage rather than directly regulating motor torque?

## Practice priorities

- Sketch compatible motor and load torque–speed curves and identify possible stable and unstable operating points.
- Derive the gearbox load-acceleration expression and explain the limiting effects of very small and very large \(N\).
- Practise converting a translating mass into equivalent rotational inertia using \(J=mr^2\).
- Derive the brushed DC motor armature-current transfer relationship from the voltage equation.
- Explain the signal flow through the nested current, speed, and position loops.
- Apply the successive one-tenth bandwidth rule and explicitly distinguish switching, current, speed, and position bandwidths.
- Explain PI pole-zero cancellation and assess its limitations in a real implementation.
- Compare why PI control is appropriate for current and speed loops while proportional control is sufficient for the simplified position loop.
- Trace the solar-car voltage-control loop from panel-voltage measurement through error amplification, duty-ratio adjustment, and buck-converter action.
- Review the warnings above before using any reconstructed equation or numerical design value in assessed work.

## Missing or incomplete

- No lectures were identified as missing or incomplete.
- Some derivations, exact controller-gain factors, diagram details, gearbox conventions, and hardware-specific solar-car values remain incomplete within the supplied summaries.

## Source manifest

- Lecture 13 (echo-lecture-13-13): complete; summary `61128e5d43a5dfb8116a2da492d9d13d3e99aa38c039d26442cb1483c69ecbb8`; transcript `d7a1c842d77011f99b0e746dde861a6aaf48365aa34344a518b1fbe883121033`; summary path `[local source path redacted]`
- Lecture 14 (echo-lecture-14-14): complete; summary `388005c5c34d2590605f8a65864606d6ea557d561d1d8d82c36a8f5c0a7eb0f1`; transcript `9c7fac8099ee4909b93de13c38c5ccdf859efa6feacb6409e07d945e19815bca`; summary path `[local source path redacted]`
- Lecture 15 (echo-lecture-15-15): complete; summary `b5d1c8270569c2dfb0e1873022cfbf32b96f5286edf127facd4f67ff99b7cea6`; transcript `51641856a27cbd1d1ab400007cb2fae5599042c6d273c5b13413723d0401fbc7`; summary path `[local source path redacted]`

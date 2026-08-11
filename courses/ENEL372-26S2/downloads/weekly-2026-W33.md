<!-- week-id: 2026-W33 -->
<!-- generated-at: 2026-08-12T09:55:13.237313+12:00 -->
# ENEL372-26S2 weekly summary

## Coverage

- Week: 2026-W33, covering 2026-08-10T00:00:00+12:00 to 2026-08-12T09:53:08.362431+12:00.
- Source covered: Lecture 13, focused on electric-motor and mechanical-load matching.
- Topics included motor and load torque-speed characteristics, gearbox matching, steady-state operating points, stability, efficiency, operating limits, four-quadrant operation, rotational inertia, gearbox-ratio optimisation, linear-to-rotational inertia conversion, and motor selection.

## Main concepts

- Motors commonly operate at higher speed and lower torque than the mechanical load, so a gearbox is often required.
- A continuous steady-state operating point occurs where compatible motor and load torque-speed curves intersect.
- A single intersection with a relatively large intersection angle is preferred for stable operation.
- The motor must provide sufficient starting torque from standstill and remain within its continuous torque, voltage, current, speed, and thermal limits.
- The selected operating range should lie in a high-efficiency region of the motor efficiency map.
- Increasing speed increases back EMF and reduces the current available within the rated-voltage limit.
- Four-quadrant operation allows combinations of positive or negative speed and torque, including motoring and braking.
- Dynamic performance depends on net torque and total inertia, as well as friction, flexibility, and other mechanical effects.
- Maximum load acceleration through a gearbox occurs when motor inertia referred to the load side equals the actual load inertia.
- A translating mass can be included in rotational analysis using an equivalent inertia.

## Equations and worked patterns

- Electrical and mechanical power:
  - \(P=VI\)
  - \(P=T\omega\)
- Simplified voltage/current power limit:
  - \(P_{\max}=V_{\text{rated}}I_{\max}\)
- Qualitative current-availability relationship:
  - \(I_{\max}\propto V_{\text{rated}}-E\)
  - The source states that this is incomplete and does not provide the full motor-specific model.
- Rotational and linear dynamics:
  - \(\frac{d\omega}{dt}=\frac{T}{J}\)
  - \(\frac{dv}{dt}=\frac{F}{m}\)
- Under the lecture’s gearbox convention:
  - \(\omega_L=\frac{\omega_M}{N}\)
  - \(T_L=NT_M\)
- Motor inertia referred to the load side:
  - \(J_{M,\text{referred}}=N^2J_M\)
- Total load-side inertia:
  - \(J_{\text{total}}=N^2J_M+J_L\)
- Load acceleration:
  - \(\frac{d\omega_L}{dt}=\frac{NT_M}{N^2J_M+J_L}\)
  - Equivalent form: \(\frac{d\omega_L}{dt}=\frac{T_M}{NJ_M+\frac{J_L}{N}}\)
- Gearbox-ratio optimisation:
  - Minimise \(NJ_M+\frac{J_L}{N}\).
  - The optimum condition is \(N^2J_M=J_L\).
  - Therefore, \(N_{\text{opt}}=\sqrt{\frac{J_L}{J_M}}\).
- Linear mass driven by a pulley:
  - \(v=\omega r\)
  - \(J_{\text{equivalent}}=mr^2\)
- Worked-pattern sequence:
  1. Determine the load-side inertia.
  2. Refer motor inertia through the gearbox.
  3. Form the total load-side inertia.
  4. Substitute the gearbox torque relationship into the acceleration equation.
  5. Optimise the ratio by setting referred motor inertia equal to load inertia.
- Throwing-arm example:
  - The source gives \(m=0.5\,\text{kg}\), \(J_M=0.2\,\text{kg}\,\text{m}^2\), and a reported arm length of \(r=0.63\,\text{m}\).
  - The full derivation was not included, so the assumptions and result require verification from the separate worked solution.

## Warnings and deadlines

- No deadlines or assessment dates are stated in the source.
- Confirm the gearbox-ratio convention against the course slides before using it in assessed work.
- The source notes that some diagrams, torque-speed curve details, axes, labels, and efficiency-map information are unavailable from the summary.
- Treat the back-EMF/current relationship as qualitative only; the complete motor model is not provided.
- Handle torque signs consistently in dynamic equations because the source alternates between torque directions and torque magnitudes.
- Do not rely on the reported \(0.63\,\text{m}\) throwing-arm result without checking the missing worked derivation.
- Continuous operation above the motor’s continuous torque region can cause overheating or damage.

## Recall questions

1. Why is a gearbox commonly required between an electric motor and a mechanical load?
2. What condition defines a continuous steady-state operating point?
3. Why is a single intersection with a relatively large intersection angle preferred?
4. Why might a motor be unable to start a load from standstill even if it can operate that load once already moving?
5. How does increasing speed affect back EMF and available current?
6. What signs of speed and motor torque define each of the four operating quadrants?
7. Using the stated gearbox convention, how are motor speed and torque related to load speed and torque?
8. How is motor inertia referred to the load side through the gearbox?
9. What condition maximises load acceleration?
10. How is a translating mass converted into an equivalent rotational inertia?

## Practice priorities

- Sketch and interpret motor and load torque-speed curves, identifying intersections, starting capability, stability, and continuous operating regions.
- Explain how efficiency maps influence motor and gearbox selection across a load operating range.
- Practise identifying the operating quadrant from the signs of speed and motor torque.
- Derive the load-acceleration expression from the gearbox speed, torque, and inertia relationships.
- Compare the effects of very small and very large gearbox ratios on load acceleration.
- Solve inertia-matching problems using \(N_{\text{opt}}=\sqrt{J_L/J_M}\).
- Convert linear masses driven by pulleys into equivalent rotational inertia using \(J=mr^2\).
- Rework the throwing-arm example only after verifying the assumptions behind the reported \(0.63\,\text{m}\) result.

## Missing or incomplete

- No lectures are identified as missing or incomplete for this week.
- Within Lecture 13, the full throwing-arm derivation is absent, and the referenced diagrams and complete motor current model are not included in the source summary.

## Source manifest

- Lecture 13 (echo-lecture-13-13): complete; summary `61128e5d43a5dfb8116a2da492d9d13d3e99aa38c039d26442cb1483c69ecbb8`; transcript `d7a1c842d77011f99b0e746dde861a6aaf48365aa34344a518b1fbe883121033`; summary path `[local source path redacted]`

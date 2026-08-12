<!-- week-id: 2026-W33 -->
<!-- generated-at: 2026-08-13T10:11:33.114205+12:00 -->
# ENEL372-26S2 weekly summary

## Coverage
- Week: 2026-W33, from 2026-08-10T00:00:00+12:00 to 2026-08-13T10:09:15.026453+12:00.
- Source covered: Lecture 13, focused on matching electric motors to mechanical loads.
- Topics included motor-load torque-speed matching, gearbox selection, stable operating points, efficiency and operating limits, four-quadrant operation, dynamic response, referred inertia, and gearbox-ratio optimisation.

## Main concepts
- Motors commonly operate at higher speed and lower torque than the mechanical loads they drive, so gearboxes are often required for matching.
- A steady-state operating point occurs where compatible motor and load torque-speed curves intersect.
- A single intersection with a relatively large intersection angle is preferred for stable operation.
- Starting torque must be sufficient at standstill. A motor that can maintain a moving load may still fail to start it.
- Continuous operation must remain within the motor’s torque, voltage, current, speed, and thermal limits.
- Efficiency maps should be considered across the expected operating range, not only at one rated point.
- Increasing speed increases back EMF, reducing available current under a rated-voltage limit.
- Four-quadrant operation permits motoring and braking in both directions of rotation.
- Dynamic acceleration depends on net torque and total inertia, together with friction, flexibility, and other mechanical effects.
- Maximum load acceleration occurs when motor inertia referred to the load side equals the load inertia.
- A translating mass can be included in rotational analysis using an equivalent rotational inertia.

## Equations and worked patterns
- Electrical and mechanical power:
  \[
  P=VI,\qquad P=T\omega
  \]
- Simplified voltage/current power limit:
  \[
  P_{\max}=V_{\text{rated}}I_{\max}
  \]
- Qualitative current-availability relationship:
  \[
  I_{\max}\propto V_{\text{rated}}-E
  \]
  where \(E\) is back EMF. The lecture did not provide a complete motor-specific equation.
- Rotational and linear dynamics:
  \[
  \frac{d\omega}{dt}=\frac{T}{J},\qquad
  \frac{dv}{dt}=\frac{F}{m}
  \]
- Using the lecture’s gearbox convention:
  \[
  \omega_L=\frac{\omega_M}{N},\qquad T_L=NT_M
  \]
- Motor inertia referred to the load side:
  \[
  J_{M,\text{referred}}=N^2J_M
  \]
- Total load-side inertia:
  \[
  J_{\text{total}}=N^2J_M+J_L
  \]
- Load acceleration:
  \[
  \frac{d\omega_L}{dt}
  =\frac{NT_M}{N^2J_M+J_L}
  =\frac{T_M}{NJ_M+\frac{J_L}{N}}
  \]
- Gearbox-ratio optimisation:
  \[
  N^2J_M=J_L,\qquad
  N_{\text{opt}}=\sqrt{\frac{J_L}{J_M}}
  \]
  The optimum balances the referred motor inertia and load inertia.
- Linear mass converted to rotational inertia:
  \[
  v=\omega r,\qquad J_{\text{equivalent}}=mr^2
  \]
- Throwing-arm pattern:
  - For \(m=0.5\text{ kg}\), the equivalent load inertia is \(J_L=mr^2\).
  - The motor inertia was given as \(J_M=0.2\text{ kg}\,\text{m}^2\).
  - The lecture reported an arm length of \(r=0.63\text{ m}\), but the full derivation was not included and should be checked against the separate worked solution.

## Warnings and deadlines
- No deadlines were identified in the supplied lecture summary.
- Verify the gearbox-ratio convention against the course slides before using it in assessed work.
- The torque-speed and efficiency-map diagrams were not preserved in the source summary; check the original slides or recording for exact axes, labels, and curve shapes.
- The back-EMF/current relationship is qualitative and incomplete; do not treat it as a complete motor model.
- Handle torque signs consistently when moving from steady-state magnitudes to dynamic equations.
- The reported \(0.63\text{ m}\) throwing-arm result lacks its full derivation in this source.

## Recall questions
1. Why is a gearbox commonly used between an electric motor and a mechanical load?
2. What condition defines a continuous steady-state operating point?
3. Why is a single intersection with a large intersection angle preferred?
4. Why might a motor operate a load successfully while already moving but fail to start it from standstill?
5. How do increasing speed and back EMF affect available motor current?
6. What are the speed and torque signs in each of the four motor-operation quadrants?
7. What is the rotational equivalent of \(F=ma\)?
8. Using the lecture’s gearbox convention, how are motor speed and torque related to load speed and torque?
9. What condition maximises load acceleration through the gearbox?
10. How is a translating mass represented as an equivalent rotational inertia?

## Practice priorities
- Practise reading motor and load torque-speed curves to identify possible operating points and assess stability.
- Be able to distinguish starting capability, continuous operating limits, and short-term peak torque capability.
- Memorise and apply the stated gearbox speed, torque, and referred-inertia relationships.
- Derive the load-acceleration expression and explain why both excessively small and excessively large gearbox ratios reduce acceleration.
- Solve inertia-matching problems using:
  \[
  N_{\text{opt}}=\sqrt{\frac{J_L}{J_M}}
  \]
- Convert linear masses to equivalent rotational inertia using \(J=mr^2\).
- Review four-quadrant sign conventions, especially braking and regenerative operation.
- Check the original lecture diagrams and separate throwing-arm worked solution before relying on visual interpretations or the \(0.63\text{ m}\) result.

## Missing or incomplete
- No lectures were identified as missing or incomplete for this week.
- The source summary notes that some lecture diagrams are unavailable and that the throwing-arm derivation was not included.

## Source manifest

- Lecture 13 (echo-lecture-13-13): complete; summary `61128e5d43a5dfb8116a2da492d9d13d3e99aa38c039d26442cb1483c69ecbb8`; transcript `d7a1c842d77011f99b0e746dde861a6aaf48365aa34344a518b1fbe883121033`; summary path `[local source path redacted]`

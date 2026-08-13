<!-- week-id: 2026-W33 -->
<!-- generated-at: 2026-08-13T12:38:38.983290+12:00 -->
# ENEL372-26S2 weekly summary

## Coverage

- Week: 2026-W33, covering 2026-08-10T00:00:00+12:00 to 2026-08-13T12:36:30.433879+12:00.
- Source covered: Lecture 13, “Motor and Mechanical-Load Systems” (`lecture_13_summary.md`).
- Coverage is complete for the supplied lecture set. No lectures were identified as missing or incomplete.

## Main concepts

- Motor–load matching: motors commonly operate at higher speed and lower torque than the mechanical load, so a gearbox is often required.
- Steady-state operation occurs where compatible motor and load torque–speed curves intersect.
- A single intersection with a relatively large intersection angle is preferred for stable operation.
- Starting torque must be sufficient at standstill. A system that operates while already rotating may still fail to start from rest.
- The operating point should remain within the motor’s continuous torque, voltage, current, speed, and thermal limits.
- Motor and gearbox selection should place the expected load range in a high-efficiency region of the motor efficiency map.
- Four-quadrant operation permits positive or negative speed and torque, including motoring, braking, and regenerative operation.
- Dynamic performance depends on net torque and total inertia, along with friction, flexibility, and other mechanical effects.
- Gearbox ratio affects both torque multiplication and the inertia seen at the load.
- Maximum load acceleration occurs when referred motor inertia equals load inertia.
- Translating masses can be represented as equivalent rotational inertia using the pulley radius.
- Practical motor selection also includes standards, programmability, warranty, and spare-parts availability.

## Equations and worked patterns

- Electrical and mechanical power:
  - \(P=VI\)
  - \(P=T\omega\)
- Simplified voltage/current power limit:
  - \(P_{\max}=V_{\text{rated}}I_{\max}\)
- Back EMF reduces available current qualitatively as speed increases:
  - \(I_{\max}\propto V_{\text{rated}}-E\)
  - The complete motor-specific equation was not provided.
- Rotational and linear dynamics:
  - \(\frac{d\omega}{dt}=\frac{T}{J}\)
  - \(\frac{dv}{dt}=\frac{F}{m}\)
- Using the lecture’s gearbox convention:
  - \(\omega_L=\frac{\omega_M}{N}\)
  - \(T_L=NT_M\)
- Motor inertia referred to the load side:
  - \(J_{M,\text{referred}}=N^2J_M\)
  - \(J_{\text{total}}=N^2J_M+J_L\)
- Load acceleration through the gearbox:
  - \[
    \frac{d\omega_L}{dt}
    =\frac{NT_M}{N^2J_M+J_L}
    =\frac{T_M}{NJ_M+\frac{J_L}{N}}
    \]
- Gearbox optimisation:
  - Minimise \(NJ_M+\frac{J_L}{N}\).
  - At maximum acceleration:
    - \(N^2J_M=J_L\)
    - \(N_{\text{opt}}=\sqrt{\frac{J_L}{J_M}}\)
- Linear-to-rotational conversion for a pulley:
  - \(v=\omega r\)
  - \(J_{\text{equivalent}}=mr^2\)
- Throwing-arm pattern:
  - Convert the thrown mass to equivalent inertia using \(J_L=mr^2\).
  - Apply the inertia-matching condition \(N^2J_M=J_L\).
  - The lecture reported \(r=0.63\text{ m}\) for the stated simplified example, but the full derivation was not included and should be checked against the separate worked solution.
- Steady-state matching:
  - \(T_M(\omega)=T_L(\omega)\), with both curves represented using compatible speed, torque, and gearbox conventions.

## Warnings and deadlines

- No deadlines or submission dates were stated in the supplied lecture summary.
- Confirm the gearbox-ratio convention against the course slides before using it in assessed work.
- The displayed torque–speed curves and efficiency map were not included in the source summary. Check the original lecture material for exact axes, curve shapes, labels, and sign conventions.
- The relation \(I_{\max}\propto V_{\text{rated}}-E\) is qualitative and incomplete; do not treat it as a complete motor model.
- Handle torque signs consistently in dynamic calculations. The source alternates between torque directions and torque magnitudes.
- The reported throwing-arm result of \(0.63\text{ m}\) requires verification because the full worked derivation was not included.
- Continuous operation above the motor’s continuous torque region can cause overheating or damage.

## Recall questions

1. Why is a gearbox commonly used between an electric motor and a mechanical load?
2. What condition defines a continuous steady-state operating point?
3. Why is a single intersection with a relatively large intersection angle preferred?
4. Why might a motor operate an already-moving load but fail to start it from standstill?
5. What do the four motor-operation quadrants represent in terms of speed and torque signs?
6. How does increasing motor speed affect back EMF and available current?
7. Using the lecture’s gearbox convention, how are load speed and torque related to motor speed and torque?
8. What condition maximises load acceleration through the gearbox?
9. Why do both very small and very large gearbox ratios reduce load acceleration?
10. How is a translating mass converted into equivalent rotational inertia?

## Practice priorities

- Sketch and interpret motor and load torque–speed curves, identifying intersections, stability, starting capability, and continuous operating limits.
- Practise applying the gearbox relationships \(\omega_L=\omega_M/N\) and \(T_L=NT_M\) consistently.
- Derive and manipulate the load-acceleration expression:
  \[
  \frac{d\omega_L}{dt}
  =\frac{T_M}{NJ_M+\frac{J_L}{N}}
  \]
- Derive the optimum gearbox ratio from the inertia-matching condition.
- Convert linear loads into equivalent rotational inertia and apply the result to pulley or throwing-arm systems.
- Review the four-quadrant sign convention, especially forward braking and regenerative operation.
- Use motor efficiency maps together with voltage, current, speed, and thermal limits when assessing a candidate operating range.
- Verify the throwing-arm example and the gearbox convention against the original lecture slides or separate worked solution before relying on them in assessed work.

## Missing or incomplete

- No lectures were missing or incomplete in the supplied coverage.
- Within Lecture 13, the exact source diagrams and the full throwing-arm derivation were not included in the summary.

## Source manifest

- Lecture 13 (echo-lecture-13-13): complete; summary `61128e5d43a5dfb8116a2da492d9d13d3e99aa38c039d26442cb1483c69ecbb8`; transcript `d7a1c842d77011f99b0e746dde861a6aaf48365aa34344a518b1fbe883121033`; summary path `[local source path redacted]`

<!-- week-id: 2026-W33 -->
<!-- generated-at: 2026-08-12T12:01:32.869754+12:00 -->
# ENEL372-26S2 weekly summary

## Coverage

- Source covered: Lecture 13 summary, generated 2026-08-11.
- Weekly window: 2026-08-10T00:00:00+12:00 to 2026-08-12T11:58:40.039233+12:00.
- Focus: matching an electric motor to a mechanical load, including torque–speed characteristics, gearbox selection, operating stability, efficiency, four-quadrant operation, and dynamic acceleration.

## Main concepts

- Motor and mechanical-load torque–speed characteristics commonly require a gearbox for compatible speed and torque.
- Continuous steady-state operation occurs at an intersection of the motor and load torque–speed curves.
- A single stable intersection is preferred. A larger intersection angle, ideally approaching 90°, indicates smaller speed changes for a given torque variation.
- Starting torque must be sufficient from standstill. A system that operates once moving may still fail to start from rest.
- The operating point should remain within the motor’s continuous torque, voltage, current, speed, and thermal limits.
- Motor and gearbox selection should place the expected load range in a high-efficiency region of the motor efficiency map.
- Increasing speed increases back EMF, reducing the current and power available within the rated-voltage limit.
- Four-quadrant operation allows positive or negative speed and torque, supporting forward/reverse motoring and braking or regenerative operation.
- Dynamic acceleration depends on net torque and total effective inertia, with friction, flexibility, and other mechanical effects also contributing.
- Maximum load acceleration occurs when motor inertia referred to the load side equals the actual load inertia.
- A translating mass can be represented as an equivalent rotational inertia using the pulley radius.

## Equations and worked patterns

- Electrical and mechanical power:
  - \(P=VI\)
  - \(P=T\omega\)
- Simplified voltage/current power limit:
  - \(P_{\max}=V_{\text{rated}}I_{\max}\)
- Back-EMF limitation:
  - \(I_{\max}\propto V_{\text{rated}}-E\)
  - This relationship is qualitative in the source; the complete motor-specific model was not provided.
- Rotational and linear dynamics:
  - \(\frac{d\omega}{dt}=\frac{T}{J}\)
  - \(\frac{dv}{dt}=\frac{F}{m}\)
- Gearbox relationships under the lecture’s stated convention:
  - \(\omega_L=\frac{\omega_M}{N}\)
  - \(T_L=NT_M\)
- Motor inertia referred to the load side:
  - \(J_{M,\text{referred}}=N^2J_M\)
- Total load-side inertia:
  - \(J_{\text{total}}=N^2J_M+J_L\)
- Load acceleration:
  - \(\frac{d\omega_L}{dt}=\frac{NT_M}{N^2J_M+J_L}\)
  - Equivalent form: \(\frac{d\omega_L}{dt}=\frac{T_M}{NJ_M+\frac{J_L}{N}}\)
- Optimum gearbox ratio:
  - Set \(NJ_M+\frac{J_L}{N}\) to a minimum.
  - The optimum condition is \(N^2J_M=J_L\).
  - Therefore, \(N_{\text{opt}}=\sqrt{\frac{J_L}{J_M}}\).
- Linear-to-rotational conversion:
  - \(v=\omega r\)
  - \(E_k=\frac{1}{2}mv^2=\frac{1}{2}J\omega^2\)
  - \(J_{\text{equivalent}}=mr^2\)
- Throwing-arm pattern:
  - Convert the 0.5 kg thrown mass into equivalent inertia using \(J_L=mr^2\).
  - Apply the inertia-matching condition \(N^2J_M=J_L\).
  - The summary reports a 0.63 m arm length, but the full derivation and assumptions were not included and should be verified separately.

## Warnings and deadlines

- No deadlines or assessed-work requirements were stated in the source.
- Confirm the gearbox ratio convention against the course slides before using the equations in assessed work.
- The torque–speed and efficiency-map diagrams were not included in the summary. Check the original slides or recording for exact axes, curve shapes, labels, and sign conventions.
- Handle torque signs consistently in dynamic calculations; the source sometimes discusses torque magnitudes rather than signed quantities.
- The back-EMF/current relationship is incomplete and should not be treated as a full motor model.
- The reported throwing-arm result of 0.63 m requires verification against the separate worked solution.

## Recall questions

1. Why is a gearbox commonly used between an electric motor and a mechanical load?
2. What condition defines a continuous steady-state operating point?
3. Why is a single intersection between the motor and load torque–speed curves preferred?
4. What does a large intersection angle indicate about operating-point stability?
5. Why might a motor operate with a load that is already moving but fail to start it from standstill?
6. How does increasing speed affect back EMF and available current?
7. What are the signs of speed and motor torque in each of the four operating quadrants?
8. Using the stated gearbox convention, how are motor speed and torque related to load speed and torque?
9. Why do both very small and very large gearbox ratios reduce load acceleration?
10. What inertia-matching condition gives the maximum load acceleration?

## Practice priorities

- Sketch representative motor and load torque–speed curves and identify steady-state intersections and stability implications.
- Practise checking starting torque, continuous torque, efficiency, voltage, current, speed, and thermal constraints.
- Memorise the four-quadrant speed–torque sign combinations and distinguish motoring from braking.
- Derive the load acceleration expression from the gearbox speed, torque, and referred-inertia relationships.
- Derive \(N_{\text{opt}}=\sqrt{J_L/J_M}\) by minimising \(NJ_M+\frac{J_L}{N}\).
- Convert a translating mass to equivalent rotational inertia and apply the result to a gearbox or pulley system.
- Recheck the throwing-arm example against the separate worked solution before relying on the reported 0.63 m value.

## Missing or incomplete

- No lectures were identified as missing or incomplete for this weekly window.
- The source summary notes incomplete supporting material for the exact diagrams, the full motor current model, and the throwing-arm derivation.

## Source manifest

- Lecture 13 (echo-lecture-13-13): complete; summary `61128e5d43a5dfb8116a2da492d9d13d3e99aa38c039d26442cb1483c69ecbb8`; transcript `d7a1c842d77011f99b0e746dde861a6aaf48365aa34344a518b1fbe883121033`; summary path `[local source path redacted]`

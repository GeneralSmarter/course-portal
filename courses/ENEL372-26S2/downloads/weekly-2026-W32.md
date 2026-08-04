<!-- week-id: 2026-W32 -->
<!-- generated-at: 2026-08-05T11:15:52.945228+12:00 -->
# ENEL372-26S2 weekly summary

## Coverage

- Lecture 10, covering practical PCB layout and circuit-noise control.
- Topics included component placement, trace geometry, ground and power routing, planes, loop-area minimisation, functional-group separation, crosstalk, and decoupling capacitors.
- Source generated 2026-08-04. No lecture content was identified as missing for this week.

## Main concepts

- Physically different PCB layouts can have different electrical performance even when they implement the same schematic connections.
- Layout affects noise generation, noise susceptibility, parasitic resistance, capacitance, and inductance.
- Ground and power traces are especially important because they connect many components and can distribute noise throughout a circuit.
- Keep traces short; make high-current power and ground traces wide.
- Minimise current-loop area, especially in high-speed and high-\(di/dt\) circuits.
- Route signal traces with their return paths close together. A continuous reference plane directly beneath a signal trace helps minimise loop area and return-path impedance.
- Ground and power planes reduce current density, resistance, and stray inductance, but only when they provide continuous, low-impedance paths.
- Avoid slots, voids, bottlenecks, and unnecessary discontinuities in reference planes.
- Avoid long parallel runs of unrelated signal traces because parasitic capacitance can cause crosstalk.
- Separate digital, analogue, and power-electronic functional groups where possible.
- Star-ground arrangements can reduce unwanted shared return-current paths between functional groups.
- Decoupling capacitors provide a low-impedance path for AC noise between power and ground while approximately isolating DC conditions.
- Real capacitors include ESR and ESL. Above their self-resonant frequency, ESL can dominate and the capacitor can behave inductively.
- Component placement is a major design activity; the lecture gives a non-universal rule of thumb of approximately 70% placement time and 30% trace-layout time.

## Equations and worked patterns

- Parasitic capacitance between conductors increases with facing area and decreases with separation:
  \[
  C_{\text{parasitic}} \propto \frac{A}{d}
  \]
  Therefore, reduce capacitive coupling by decreasing parallel overlap, increasing separation, or routing traces on different layers where appropriate.

- Stray inductance increases qualitatively with current-loop area:
  \[
  L_{\text{stray}} \propto A_{\text{loop}}
  \]
  Therefore, keep outgoing and return-current paths physically close.

- Voltage across stray inductance:
  \[
  v_L = L\frac{di}{dt}
  \]
  A switching loop with large stray inductance or rapidly changing current can produce a large voltage spike.

- High-\(di/dt\) switching-loop pattern:
  1. A switch changes state rapidly.
  2. The current change interacts with the loop’s stray inductance.
  3. The resulting \(L\,di/dt\) voltage produces a transient.
  4. A local high-frequency capacitor can provide a shorter current path, reduce loop area and effective inductance, and reduce the spike.

- Decoupling-capacitor frequency pattern:
  - At DC and low frequency, the capacitor is approximately an open circuit.
  - Over its effective frequency range, it provides a low-impedance AC path between power and ground.
  - Above self-resonance, parasitic inductance increases its impedance and limits its usefulness.

## Warnings and deadlines

- No deadlines or assessment dates were stated in the source.
- The approximate capacitor frequency ranges in the lecture are not universal component limits; verify real designs against manufacturer impedance data and the actual package and layout.
- The stated \(L_{\text{stray}} \propto A_{\text{loop}}\) relationship is a qualitative design rule, not a complete inductance formula.
- The approximate 70% placement and 30% routing split is a rule of thumb, not a fixed engineering requirement.
- Exact PCB layer arrangements, component positions, plane geometries, and some converter details cannot be recovered from the unavailable lecture diagrams.
- The uncertain example involving a 10 nF film capacitor, a 10 µF capacitor, and frequencies near 20 MHz should not be treated as a verified component-selection rule. The reliable principle is that technology and parasitics determine high-frequency impedance.

## Recall questions

1. Why can two PCB layouts with identical electrical connections perform differently?
2. Why are ground and power traces particularly important for noise control?
3. Why should high-current power and ground traces generally be short and wide?
4. Why does keeping a signal trace close to its return-current path reduce unwanted inductive effects?
5. What problems can a slot, void, or bottleneck in a ground plane create?
6. Why can long parallel runs of unrelated signal traces cause crosstalk?
7. Use \(v_L=L\,di/dt\) to explain how a switching converter can generate a damaging voltage spike.
8. Why might a smaller ceramic or film capacitor provide lower high-frequency impedance than a larger electrolytic capacitor?
9. What is the purpose of separating digital, analogue, and power-electronic functional groups?
10. What changes in a real capacitor’s behaviour above its self-resonant frequency?

## Practice priorities

- Practise identifying the high-\(di/dt\) loop in a switching power circuit and redesigning its physical path to minimise loop area.
- Practise tracing the intended return-current path for a high-speed signal over a ground plane.
- Review how plane discontinuities, overlapping functional regions, and shared return paths can transfer noise.
- Compare routing strategies for power/ground pairs versus unrelated signal traces.
- Explain decoupling-capacitor behaviour across DC, the effective operating range, and above self-resonance.
- Be able to apply \(C_{\text{parasitic}} \propto A/d\) and \(L_{\text{stray}} \propto A_{\text{loop}}\) qualitatively to layout decisions.
- Treat all approximate component-frequency figures as starting points only; check manufacturer data for design decisions.

## Missing or incomplete

- None identified for the specified week.
- The lecture source itself notes that diagrams were unavailable and that some transcript terminology and component-frequency examples were uncertain.

## Source manifest

- Lecture 10 (echo-lecture-10-10): complete; summary `f159c2b507e9251dd427ea087558137c70569430cd19b591b57b01f40a10b481`; transcript `ae3f83f17c4d3bc8f8031b2f90785e24a6a2348f74a2378da3fe9168d141feaa`; summary path `[local source path redacted]`

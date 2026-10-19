<!-- week-id: 2026-W42 -->
<!-- generated-at: 2026-10-20T12:25:41.108630+13:00 -->
# ENEL372-26S2 weekly summary

## Coverage

Rebuilt from all four actual sessions, including the previously unindexed 16 October noon tutorial.

- Lecture 35: 2026-10-12. This lecture covered:  - A bootstrap capacitor arrangement used with an op-amp voltage follower to reduce coupling of supply fluctuations and noise into the op-amp input. - The relationship between op-amp feedback, buffering, and the apparent high impedance of the input path. - Filter specifications and the four principal filter types:   - Low-pass   - High-pass   - Band-pass   - Band-stop, also called a notch filter - Transfer functions, attenuation in decibels, pass-band ripple, stop-band attenuation, transition bands, and filter order. - The trade-off between selectivity, ripple, phase lag, circuit complexity, and noise. - Passive LCR filter analysis using impedances and transfer functions. - Active filters using op-amps, including their buffering and gain advantages. - The role of filt

- Lecture 36: 2026-10-13. This lecture covered active-filter revision and exam expectations, with emphasis on:  - Magnitude-response comparisons for Butterworth, Chebyshev, and Bessel filters. - The meaning of the cutoff frequency and the conventional −3 dB point. - Idealised filter response sketches for low-pass, high-pass, band-pass, and notch filters. - The trade-off between passband flatness, stopband attenuation, transition sharpness, and phase response. - Bessel-filter phase characteristics and approximately constant group delay. - Replacing a physically large and expensive inductor with an active simulated-inductance circuit. - Applying a simulated inductance in low-pass and high-pass active-filter circuits. - A preliminary Butterworth design example using an Antoniou simulated inductance.  The lecturer indi

- Lecture 37: 2026-10-16. This lecture focused on second-order active filters and their implementation using op-amp circuits, particularly the Sallen-Key topology.  Main topics:  - Constructing low-pass, band-pass, and high-pass filter functions by integrating a high-pass filter. - Practical implementation of active filters using op-amp integrators and summing arrangements. - Advantages of active filters over passive LCR filters, especially buffering from load impedance. - The Sallen-Key second-order filter configuration using a single op-amp. - Derivation of the Sallen-Key transfer function using impedance notation. - Designing second-order low-pass and high-pass filters. - Butterworth shortcuts and the more general design method. - Normalised filter forms and the distinction between the natural frequency, cutoff 

- Lecture 38: 2026-10-16. The newly indexed recording is the Friday 16 October 2026, 12:00 tutorial, separate from the morning lecture. It reviews the exam layout from memory, interpreting filter coefficient tables, rectifier current waveforms/THD and BLDC torque–speed characteristics. The main teaching ends around 51 minutes. This is Term 4 exam preparation, not an additional teaching week.

## Main concepts

### Lecture 35

- Op-amp negative feedback forces the two input voltages to be approximately equal when the amplifier is operating in its linear region.
- A voltage follower provides buffering:
  - High input impedance
  - Low output impedance
  - Isolation between the source and the load
- A bootstrap capacitor can make a resistor appear to have a very high effective impedance for the relevant AC signal.
- The bootstrap arrangement reduces the effect of supply-voltage fluctuations and noise coupling into the positive input.
- A filter is characterised by a transfer function that describes how input signals are converted into output signals as a function of frequency.
- The four basic filter responses are low-pass, high-pass, band-pass, and band-stop/notch.
- Pass-band ripple is unwanted variation in the magnitude response within the nominal pass band.
- A sharper transition band generally requires a higher-order filter.
- Higher-order filters tend to introduce:
  - More components
  - More circuit complexity
  - More phase lag
  - Potentially more noise
- There is no ideal filter with zero transition width, zero ripple, zero phase distortion, and no implementation cost.
- Butterworth filters provide a maximally flat magnitude response in the pass band.
- Chebyshev Type I filters trade pass-band ripple for a sharper transition.
- Chebyshev Type II filters have a flat pass band but ripple in the stop band.
- Bessel filters are associated with approximately linear phase and more constant group delay in the pass band.
- Active filters use op-amps to provide buffering and, if required, gain.
- Passive filters can be affected by loading, component tolerances, and temperature; active filters reduce loading problems through buffering.
- Filter design can be treated as a pole-zero placement problem, closely related to control-system design.
- Normalising the cutoff or characteristic frequency simplifies filter design before scaling the design to the required frequency.
- The quality factor Q is related to the sharpness and bandwidth of a resonant or band-pass response.
- An active filter can emulate an inductor using op-amp circuitry, avoiding the size and practical limitations of a physical inductor.

### Bootstrap capacitor and op-amp buffering

The opening section discussed a circuit containing a resistor, capacitor, and op-amp configured as a voltage follower. The concern was that fluctuations in a supply or reference voltage could couple through a voltage divider into the positive input of the op-amp.

The lecturer described the capacitor and resistor combination as a bootstrap capacitor arrangement. The qualitative operation is:

1. The op-amp is configured as a voltage follower.
2. Negative feedback causes the output voltage to follow the input voltage.
3. The output voltage is coupled back through the capacitor/resistor network.
4. For the relevant AC fluctuations, the voltages on either side of the resistor become approximately equal.
5. The voltage across the resistor is therefore approximately zero.
6. With approximately zero voltage across the resistor, the AC current through it is also approximately zero.
7. The resistor consequently appears to have a very large, effectively infinite impedance to those fluctuations.

The “infinite resistance” is not a physical infinite resistance. It is an effective impedance produced by the combination of the passive components and op-amp feedback.

The arrangement therefore acts as a buffer and helps prevent supply noise from being injected into the op-amp input. The lecturer described the capacitor selection as important and stated that the capacitors must be chosen to have matching values for the intended behaviour.

The intuitive frequency-domain explanation was that:

- The input signal is passed through a high-pass characteristic.
- The offset or DC component is passed through a low-pass characteristic.
- The selected capacitor values allow the relevant components to combine so that the two compared voltages become equal.

The transcript gives the resulting relationship approximately as:

V₁ = V₀

It also states that both voltages contain the input term plus half the supply voltage, written approximately as:

V₁ = V_N + V_CC/2

V₀ = V_N + V_CC/2

The exact circuit labels are not available in the transcript, so the notation should be checked against the lecture slide.

### Transfer functions and attenuation

A filter can be represented by a transfer function:

H(s) = V_out(s) / V_in(s)

For sinusoidal steady-state analysis, the lecturer referred to substituting:

s = jω

The magnitude response is:

|H(jω)|

The attenuation in decibels was described as:

A_dB = -20 log₁₀|H(jω)|

The negative sign is used when describing attenuation. If the circuit amplifies a signal, the gain may instead be expressed as a positive decibel value.

Filtering is frequency-dependent attenuation. A filter does not necessarily remove all unwanted content perfectly; instead, its magnitude response varies over frequency.

### Four principal filter types

The lecturer identified four standard filter responses.

#### Low-pass filter

A low-pass filter passes low frequencies and attenuates high frequencies.

Important features include:

- Pass band at low frequency
- Stop band at high frequency
- Transition band between them
- Pass-band gain or attenuation
- Stop-band attenuation
- Cutoff or pass-band edge frequency
- Stop-band edge frequency

#### High-pass filter

A high-pass filter attenuates low frequencies and passes high frequencies.

Its response is approximately the reverse of a low-pass response when plotted against logarithmic frequency.

#### Band-pass filter

A band-pass filter passes frequencies within a selected interval and attenuates frequencies below and above that interval.

Important quantities include:

- Lower cutoff frequency
- Upper cutoff frequency
- Pass-band width
- Centre or characteristic frequency
- Stop bands on both sides

#### Band-stop or notch filter

A band-stop filter attenuates a selected range of frequencies while passing frequencies below and above that range.

A notch filter is a narrow band-stop filter intended to remove a specific interfering frequency.

The lecturer gave mains hum as an example. In New Zealand, mains interference was described as 50 Hz, so a notch filter can be designed to attenuate 50 Hz hum in an audio or instrumentation signal.

Other possible applications mentioned included removing a sloshing or resonant frequency in vehicles, ships, or rockets. These examples were illustrative rather than detailed filter designs.

### Pass band, stop band, and transition band

A practical filter does not change instantaneously from full transmission to full attenuation.

The response therefore contains:

- Pass band: frequencies intended to pass with limited attenuation.
- Stop band: frequencies intended to be strongly attenuated.
- Transition band: the interval over which the response changes between pass-band and stop-band behaviour.

The lecturer emphasised that the transition band should be labelled when reproducing a filter diagram. The diagram should also identify:

- Minimum attenuation, referred to in the transcript as A_min.
- Maximum pass-band magnitude or pass-band ripple, referred to as A_max.
- The pass band and stop band.
- The transition band.
- The minimum stop-band frequency where relevant.

A long transition band allows many unwanted frequencies to pass before strong attenuation is reached. A short transition band gives a sharper filter response but generally requires a higher-order design and introduces other compromises.

### Ripple and the −3 dB point

Ripple is variation in the magnitude response over a nominal pass band or stop band.

The lecturer specifically referred to pass-band ripple. If the response varies significantly in the pass band, different desired signal frequencies are attenuated by different amounts.

A common reference point is −3 dB. The corresponding amplitude ratio is:

|H| = 1/√2 ≈ 0.707

The transcript also mentioned that 1 dB ripple designs are possible, but 3 dB was described as a common design value and as an industry-standard reference in the context of the discussed filter tables.

The lecture stated that reducing ripple while retaining a sharp transition generally requires a higher-order filter.

### Filter order, poles, and selectivity

The order of a filter is related to the number of poles in its transfer function. A fifth-order low-pass filter, for example, has five poles in the denominator.

The lecturer described a fifth-order filter with a fourth-order numerator as an example of a low-pass transfer function. The exact coefficients were not clearly captured by the transcript.

Increasing filter order generally:

- Makes the transition band narrower.
- Increases selectivity.
- Allows more rapid attenuation outside the pass band.
- Increases circuit complexity.
- Increases phase lag.
- May introduce more noise and sensitivity to component tolerances.

Selectivity improves when the pass-band and stop-band edge frequencies move closer together, reducing the transition-band width.

The lecture connected filter design with control design. Techniques involving poles, zeros, natural modes, and pole placement can be applied to both fields.

### Passive and active filters

Passive filters use components such as:

- Resistors
- Capacitors
- Inductors

Active filters use active devices, particularly op-amps, together with resistors and capacitors.

The lecturer stated that the mathematical treatment remains similar: derive or specify a transfer function, then realise it using available components.

Active-filter advantages include:

- Buffering against the load
- Reduced sensitivity to loading
- The ability to provide gain
- Avoiding large or impractical physical inductors
- Easier implementation of some higher-order responses

A passive filter may change its behaviour when the load changes. Its response can also be affected by temperature and other practical factors. An op-amp buffer isolates the filter from the load and makes the designed response more predictable.

The lecturer used a first-order active low-pass filter as an example. The gain was described as being set by a resistor ratio, approximately:

A₀ = R₂/R₁

The transcript contains a partially unclear exchange about whether the gain is R₂/R₁. The lecturer confirmed that, for the particular circuit being discussed, it was precisely R₂/R₁.

For unity gain, the lecturer suggested selecting equal resistor values, such as two equal kilo-ohm resistors.

The transfer function was derived by applying current relationships and then taking the Laplace transform. The lecturer stated that the resulting circuit had the form of a low-pass filter.

The full circuit topology and exact transfer function are not recoverable reliably from the transcript alone and should be checked against the lecture slide.

### Filter families

The lecture discussed several standard approximation families.

#### Butterworth

The Butterworth response was described as maximally flat in the pass band, with no pass-band ripple.

Advantages:

- Flat pass-band magnitude response
- No pass-band ripple
- Commonly used general-purpose response
- Straightforward interpretation

The lecturer associated the second-order Butterworth case with:

Q = 1/√2

This value produces a flat response without the resonant bump associated with a higher-Q second-order response.

#### Chebyshev Type I

Chebyshev Type I filters use pass-band ripple to obtain a sharper transition than a Butterworth filter of comparable order.

Advantages:

- Faster transition from pass band to stop band
- Greater selectivity for a given order

Disadvantage:

- Ripple in the pass band

The lecturer described this as an example of the trade-off between transition sharpness and ripple.

#### Chebyshev Type II

Chebyshev Type II filters were described as having:

- A flat pass band
- Ripple in the stop band

This reverses the location of the ripple compared with the Type I response.

#### Bessel

Bessel filters prioritise phase behaviour rather than the sharpest magnitude transition.

The lecturer described the Bessel response as making the rate of change of phase with frequency as constant as possible. This produces approximately linear phase in the pass band and therefore a more constant delay.

Advantages:

- Approximately linear phase
- More constant group delay
- Reduced waveform distortion for broadband signals

The lecture gave radio-frequency and voice transmission as examples where different frequency components should experience similar delay to avoid distortion.

### Normalisation and coefficient tables

Filter designs are often normalised first. The characteristic or cutoff frequency is set to a normalised value, commonly:

ω_c = 1

The resulting normalised polynomial coefficients can then be scaled to the desired physical frequency.

The lecturer explained that coefficient tables are available for different:

- Filter families
- Filter orders
- Ripple or attenuation specifications

The coefficients are then related to resistor, capacitor, and inductor values to construct the physical circuit.

The transcript refers to coefficients as A_i and B_i, although the exact notation is uncertain.

### Quality factor Q and bandwidth

The lecture related the control-system damping parameter to the filter quality factor Q.

The transcript appears to state a relationship of the form:

ζ = 1/(2Q)

This is the standard second-order relationship, but the spoken notation was unclear.

The lecturer stated that:

1/Q

is associated with the normalised bandwidth of a band-pass filter.

For a normalised centre frequency of one, the bandwidth was described approximately as:

Bandwidth ≈ 1/Q

A larger Q corresponds to a narrower bandwidth and a sharper resonance. A smaller Q corresponds to a wider bandwidth and a less selective response.

The lecturer also described the role of Q in determining the resonant bump of a second-order response:

- Q = 1/√2 gives the second-order Butterworth response, which is flat rather than peaking.
- Higher Q produces a more pronounced bump or resonance.
- Lower Q produces a more heavily damped response.

The exact bandwidth convention and frequency normalisation should be checked against the course notes.

### Passive LCR filter analysis

The lecturer described a general method for analysing passive filters using impedances.

The procedure is:

1. Represent inductors and capacitors using their s-domain impedances.
2. Identify the series and parallel impedance combinations.
3. Write the voltage-divider or equivalent transfer-function expression.
4. Substitute the component impedances.
5. Simplify the expression into a standard transfer-function form.
6. Compare the result with the desired normalised filter polynomial.
7. Solve for component values.

The commonly used impedances are:

Z_R = R

Z_L = sL

Z_C = 1/(sC)

For a parallel resistor-capacitor combination, the impedance must be calculated using the parallel-impedance relationship. The transcript does not preserve the complete algebraic expression.

The lecturer used a buck converter as an application example. The switching stage performs the voltage-conversion function, while the inductor-capacitor section acts as a low-pass filter that removes transients and high-frequency components caused by rapid MOSFET switching.

### Natural frequency and component selection

For an LC network, the natural angular frequency was identified approximately as:

ω₀ = 1/√(LC)

Equivalently:

ω₀² = 1/(LC)

The lecturer explained that a designer can specify:

- Natural frequency ω₀
- Quality factor Q
- Gain A₀

and then solve for the component values.

This gives three design equations for three unknowns, allowing a unique LCR combination for the selected design requirements, subject to practical component constraints.

The same conceptual approach is used for active filters, except that an op-amp circuit emulates the required inductor behaviour rather than using a physical inductor.

### First- and second-order responses

For a first-order filter, the asymptotic magnitude slope is approximately:

20 dB per decade

For a second-order high-pass or low-pass filter, the asymptotic slope is approximately:

40 dB per decade

A second-order high-pass filter attenuates low frequencies and rises at approximately 40 dB per decade until reaching the pass-band region.

A second-order low-pass filter passes low frequencies and rolls off at approximately 40 dB per decade above the cutoff region.

A second-order band-pass response rises at approximately 20 dB per decade below the pass band and falls at approximately 20 dB per decade above it, although the exact response depends on the design and Q.

A second-order notch filter combines low-pass and high-pass behaviour to reject a selected frequency region.

The transcript contains several verbal corrections and unclear phrases around “40 dB per decade,” “90,” and the exact shapes of the curves. The slopes above reflect the standard interpretation of the stated second-order behaviour.

### Lecture 36

- Butterworth filters are maximally flat in the passband and have no passband ripple.
- Increasing filter order makes the transition from passband to stopband sharper, but also changes the phase response.
- The conventional cutoff point is the frequency at which the magnitude has fallen to approximately 0.7071 of its passband value, corresponding to −3 dB.
- Chebyshev filters trade passband or stopband ripple for a sharper transition than a Butterworth filter of the same order.
- For a specified filter order, a Chebyshev filter can provide greater stopband attenuation than other common approximations.
- For a specified attenuation requirement, a Chebyshev filter may achieve the requirement with a lower order.
- Bessel filters are selected when phase linearity or delay characteristics are more important than a sharp magnitude transition.
- A filter with linear phase delays all frequency components by the same amount, preserving waveform shape apart from the delay.
- Group delay is related to the rate of change of phase with respect to frequency.
- Active filters can simulate an inductor using op-amps, resistors, and capacitors.
- The simulated inductor is not a perfect physical replacement, but can perform the required filter function without a large physical inductor.
- In the simplified equal-resistance case discussed, the simulated inductance is proportional to the capacitor value and the square of the resistance value.
- For the Butterworth design shortcut shown, the lecturer stated that the method should not be used for Chebyshev or Bessel filters.

### Examination guidance

The lecturer distinguished between learning outcomes and material likely to be examined:

- Comparing the magnitude and phase of the three common filter approximations is a learning outcome, but a complete detailed comparison of every phase characteristic is not expected.
- Students should know the general advantages and characteristics of Butterworth, Chebyshev, and Bessel filters.
- The lecturer stated that designing a second-order active filter would definitely be examinable in one part of the lecture, but later explicitly stated that second-order active filters would not be examined. This contradiction is recorded in the Caveats section.
- The lecturer repeatedly stated that full analysis of all four filter types was not required.
- Low-pass and high-pass filter design were identified as relevant.
- A band-pass filter can be formed by combining high-pass and low-pass behaviour.
- Students should be able to sketch the general filter response for any of:
  - Low-pass
  - High-pass
  - Band-pass
  - Notch
- A response sketch should show:
  - Passband
  - Stopband
  - Transition region
  - Relevant cutoff frequencies
  - Ripple where appropriate
  - Useful axis or response labels

The lecturer suggested that a reasonably idealised sketch could receive full credit if the important features were present.

### Butterworth filters

The Butterworth response was described as:

- Maximally flat.
- Free from passband ripple.
- Commonly used because of its smooth and predictable response.
- Capable of providing a useful response even at first order, provided the cutoff frequency is selected appropriately.
- Sharper as the filter order increases.

For a chosen signal frequency, the cutoff frequency should be selected so that the signal is not excessively attenuated. The −3 dB point is a standard reference rather than necessarily a design limitation.

The magnitude at the conventional cutoff frequency is:

- Approximately 0.7071 of the passband magnitude.
- Often rounded to 0.71.
- Equivalent to approximately −3 dB.

The lecturer described the −3 dB convention as an engineering standard that allows consistent communication between engineers. The choice of 3 dB was presented as historical and conventional rather than arising from a unique physical requirement.

As filter order increases:

- The transition becomes sharper.
- Frequencies beyond the cutoff are attenuated more rapidly.
- The phase response is also affected.

The lecturer described higher-order Butterworth filters as retaining relatively good phase behaviour over part of the useful frequency range, although not as well as Bessel filters.

### Generalised ripple parameter

The lecturer referred to a generalised formulation containing an epsilon parameter. For the standard 3 dB Butterworth case:

- The lecturer stated that epsilon can be set to 1.
- Setting the order to 1 gives the first-order case.
- Epsilon can remain at 1 while the order is varied for higher-order Butterworth filters.

The derivation was presented only as an aside. The lecturer described substituting the relevant normalised frequency into the general expression, obtaining terms involving \(1+\epsilon^2\), and then solving for epsilon. The exact complete transfer-function expression was not clearly captured by the transcript.

### Chebyshev filters

The Chebyshev filter was described as sacrificing passband or stopband flatness to obtain a sharper cutoff.

The main advantages discussed were:

- A sharper transition than a Butterworth filter of the same order.
- Greater attenuation in the stopband for a given filter order.
- The possibility of achieving a specified attenuation using a lower filter order.

The lecturer used two meanings of “efficient”:

1. For a fixed order, achieving greater stopband attenuation.
2. For a fixed attenuation requirement, achieving the requirement with a smaller order.

The exact discussion of Chebyshev Type I versus Type II was unclear in the automated transcript. The lecturer stressed that if a question explicitly specified a type, the corresponding ripple placement should be drawn correctly. However, the transcript does not reliably preserve which curve was being labelled as Type I or Type II.

### Bessel filters

The Bessel filter was presented as the filter that excels in phase and delay behaviour.

For a signal containing several frequency components, a linear-phase filter produces:

- The same phase slope for all frequencies.
- The same time delay for all frequency components.
- A delayed version of the original waveform, assuming the magnitude response is sufficiently constant over the relevant frequency range.

The lecturer described the Bessel filter as providing an approximately ideal time delay. Its principal advantage is therefore waveform preservation through phase behaviour rather than the sharpest magnitude cutoff.

The lecturer contrasted the filters qualitatively:

- Bessel: best delay and phase characteristics.
- Butterworth: good compromise, with a flat magnitude response and reasonably good phase over an appropriate range.
- Chebyshev: sharper magnitude transition, but worse ripple and phase behaviour.

### Phase and group delay

If the phase is linear with frequency, it can be represented conceptually as:

\[
\phi(\omega) = -\alpha \omega
\]

where \(\alpha > 0\) represents a time delay.

The group delay is related to the phase slope:

\[
\tau_g(\omega) = -\frac{d\phi(\omega)}{d\omega}
\]

A constant phase slope gives constant group delay.

The transcript also refers to a normalised group delay and dividing by a cutoff-related quantity. The exact notation was not captured reliably. The important qualitative point is that the Bessel response has a flatter group-delay characteristic over the useful frequency range.

The lecturer briefly used first-order poles as a controls-related example:

\[
\frac{1}{s+1}
\]

was associated with a phase shift approaching \(-90^\circ\), and multiple first-order factors produce larger phase shifts. This was explicitly described as background and not an examination requirement for students without controls experience.

### Step response as a filter characterisation

The lecturer briefly discussed characterising filters in the time domain using a step response.

Key points:

- A step response characterises the transfer function.
- A step contains frequency content across the spectrum.
- The response therefore provides information about the system’s overall behaviour.
- Different filter approximations and orders produce different step responses.
- This material was described as supplementary and not a major examination focus.

The lecturer noted that a step response is not necessarily a physically realistic signal for every filter application. It is instead a useful characterisation tool.

### From passive to active filters

The lecture revisited passive LCR filters using the Laplace domain:

- An inductor has impedance proportional to \(s\).
- A capacitor has impedance proportional to \(1/s\).
- An inductor can therefore produce differentiating behaviour.
- A capacitor can produce integrating behaviour.

The motivation for an active filter is to obtain the desired filter response without using a large physical inductor. Physical inductors were described as:

- Heavy.
- Expensive.
- Difficult to reproduce perfectly using an active circuit.

An active circuit can approximate the required inductive impedance using:

- Op-amps.
- Resistors.
- Capacitors.

The resulting circuit is more complicated than a physical inductor, but can be integrated into an active filter.

### Simulated inductance

The lecturer analysed an active circuit by:

1. Tracking current through the resistor network.
2. Using the capacitor relationship between current and voltage.
3. Applying ideal op-amp assumptions, including negligible input current.
4. Calculating voltage drops using resistor current relationships.
5. Finding the input impedance from:

\[
Z = \frac{V_1}{I_1}
\]

The resulting input impedance behaves like an inductive impedance. The entire op-amp/resistor/capacitor network therefore acts as an equivalent inductor.

Under the simplified equal-resistance case discussed in the lecture, the equivalent inductance was stated as:

\[
L = C R^2
\]

This relationship means that the equivalent inductance can be changed by changing the capacitor or resistor values. The capacitor is essential to the operation of the simulated-inductance circuit.

The lecturer also acknowledged that:

- The circuit relies on idealised assumptions.
- Practical losses exist.
- The op-amps are not ideal.
- The simulated inductance is not exactly equivalent to a physical inductor.
- Higher-order active approximations can improve the approximation.

The transcript does not preserve the complete generalised Antoniou-inductance expression with all resistor values unambiguously.

### Using the simulated inductance in filters

Once the active circuit is treated as an equivalent inductor, it can replace the inductor in a conventional LCR filter.

The design process is then conceptually:

1. Design the filter as a conventional passive LCR filter.
2. Keep the inductor symbolically as \(L\).
3. Replace \(L\) with the simulated-inductance circuit at the end.
4. Select resistor and capacitor values for the simulated-inductance circuit.
5. Check that the resulting circuit implements the desired transfer function.

The lecturer showed examples of:

- Low-pass active filters.
- High-pass active filters.
- Band-pass active filters.
- A more complicated notch filter.

The active inductor can be incorporated into the relevant LCR topology so that the overall circuit retains the intended filter response.

### Butterworth design example

The example involved a:

- Low-pass filter.
- Butterworth response.
- Cutoff frequency of 10 kHz.
- Simulated inductance using an Antoniou-style circuit.

The lecturer described the approach as:

- Treating the active simulated-inductance circuit as the inductor in the conventional filter.
- Using the conventional filter equations for the rest of the design.
- Equating coefficients in the transfer-function expressions.
- Solving for resistor and capacitor values.
- Converting the cutoff frequency from hertz to angular frequency when required.

The lecturer emphasised that this was a simplified Butterworth-specific method rather than the general normalised filter-design method.

The method:

- Works for the particular Butterworth design approach shown.
- Should not be directly applied to Chebyshev or Bessel filters.
- Is not the lecturer’s recommended examination method.
- Was included mainly to demonstrate how a simulated inductance can be integrated into a filter design.

The lecturer recommended leaving the element as \(L\) during most of the design and replacing it with the active simulated-inductance implementation near the end.

### Lecture 37

- Active filters can be implemented using op-amps, resistors, and capacitors without inductors.
- An op-amp integrator can be used to generate related filter responses:
  - Starting from a high-pass filter, integrating once produces a band-pass response.
  - Integrating again produces a low-pass response.
- Active filters are buffered from the load because the op-amp reduces the effect of load impedance on the filter response.
- Passive LCR filters are more sensitive to loading because the load impedance can interact with the filter resistance and alter the pole or cutoff frequency.
- A Sallen-Key filter is a second-order active filter using a single op-amp.
- The Sallen-Key configuration can be used to implement low-pass and high-pass filters.
- The circuit should be analysed using impedances \(Z_1\), \(Z_2\), \(Z_3\), and \(Z_4\), rather than relying only on component labels such as \(R_1\), \(R_2\), \(C_1\), and \(C_2\).
- Different textbooks may assign resistor and capacitor labels differently. The important requirement is consistency between the circuit, impedance definitions, and equations.
- The general second-order low-pass form discussed was:

  \[
  H(s)=\frac{K}{1+A_1s+B_1s^2}
  \]

  or an equivalent scaled form involving \(\omega_0\) and \(Q\).

- The corresponding high-pass form has an \(s^2\) numerator:

  \[
  H(s)=\frac{K s^2}{s^2+A_1s+B_1}
  \]

  The exact coefficient notation should be checked against the course notes because the transcript is imperfect.
- For a Butterworth second-order filter, the lecturer stated that:

  \[
  Q=\frac{1}{\sqrt{2}}
  \]

- For a Butterworth filter, the cutoff frequency \(\omega_c\) and the natural frequency \(\omega_0\) coincide in the formulation used in the lecture.
- For a Bessel filter, \(\omega_0\) is not generally equal to \(\omega_c\).
- The shortcut design method discussed is appropriate for Butterworth filters because of their particular coefficient form. It should not be applied automatically to Bessel or Chebyshev filters.
- The recommended exam method was the general method, even though the Butterworth shortcut is faster when its conditions are satisfied.
- Normalisation allows a prototype filter specified at a normalised frequency to be transformed to a desired cutoff frequency.

The lecture began by revisiting a practical filter implementation based on integration. The lecturer explained that integration can be used to move between related filter responses. Starting with a high-pass filter, one integration produces a band-pass filter and a second integration produces a low-pass filter.

The lecturer described this as a useful way to implement the filter using op-amp integrators, summing points, and feedback. The implementation can be constructed entirely in analogue hardware, without a microcontroller. The op-amp integrator uses a capacitor in the feedback path. The filter selection can be physically wired or potentially controlled using switches, although automatic switching would require additional circuitry.

The equivalent-circuit analysis involves setting selected inputs or sources to zero and using superposition. The lecturer compared this process with control-system transfer-function analysis. Terms are combined algebraically, and the resulting expressions can be rearranged to express the band-pass and low-pass outputs in terms of the high-pass response.

The detailed hardware implementation was stated to be non-examinable. Its purpose was to show that active filters and PID-like functions can be implemented directly with analogue hardware.

The lecturer then discussed the practical advantages of active filters. Op-amps provide buffering, so changes in load characteristics have much less effect on the filter response. In contrast, an LCR filter can be affected by the impedance of the attached load. The load impedance may interact with the filter resistance and shift the pole or cutoff frequency. Active filters reduce this loading problem.

The lecture then moved to second-order filters implemented with a single op-amp using the Sallen-Key topology. Other second-order filter structures exist, including arrangements using multiple op-amps, but the single-op-amp Sallen-Key structure was identified as important and examinable.

The Sallen-Key circuit was analysed using currents at the op-amp input node. Because the op-amp is configured as a voltage follower in the form discussed, there is no voltage gain in that particular stage:

\[
V_{\text{out}}=V_{\text{in}}
\]

The current entering the op-amp input is treated as zero. Applying Kirchhoff’s current law gives a sum of branch currents equal to zero. Each current is expressed as a voltage difference divided by the relevant impedance. The lecturer emphasised that the derivation is mainly algebraic and that students are not required to derive the complete transfer-function formula in the exam.

The complete transfer-function result is provided on the exam sheet, according to the lecture. Students are expected to identify the circuit configuration and correctly determine the impedances \(Z_1\), \(Z_2\), \(Z_3\), and \(Z_4\).

For the low-pass Sallen-Key form, the lecturer identified capacitor impedances of the form:

\[
Z_C=\frac{1}{sC}
\]

and resistor impedances of the form:

\[
Z_R=R
\]

The relevant component assignment depends on the exact circuit drawing. The lecturer warned that the labels used in different books may differ. Students should map the physical circuit elements to \(Z_1\) through \(Z_4\) before substituting into the transfer function.

For the low-pass example, the transcript identifies capacitor impedances involving \(C_3\) and \(C_4\), and resistor impedances involving \(R_1\) and \(R_2\), but the automated transcript does not preserve the complete circuit diagram clearly enough to establish every label with certainty.

The lecturer showed how to rearrange the transfer function into the standard second-order form. The purpose of factoring and rearranging is to identify the coefficient associated with \(s\), the coefficient associated with \(s^2\), \(\omega_0\), and \(Q\).

A faster design method was presented for Butterworth filters. In this particular case, the cutoff frequency can be identified directly with \(\omega_0\), and the Butterworth quality factor is:

\[
Q=\frac{1}{\sqrt{2}}
\]

This allows component values to be found more directly. For example, if a resistance and the desired cutoff frequency are known, a capacitor can be calculated from the relevant \(\omega_0\) relationship. Once one capacitor has been found, the other can be calculated using the remaining design equation.

The lecturer gave an example using a cutoff frequency of approximately \(50\text{ kHz}\), represented in angular-frequency form as:

\[
\omega_c=2\pi(50\times10^3)
\]

The exact component values and complete circuit data were not audible in the transcript.

The shortcut method is convenient for Butterworth filters but is unsafe for other approximations. The lecturer specifically warned that applying it to Bessel or Chebyshev filters can produce an incorrect result because the coefficient relationships differ. The recommended approach for the exam was therefore to use the general method consistently, even if the shortcut is familiar from textbooks.

The high-pass Sallen-Key form uses a different arrangement of resistors and capacitors from the low-pass form. The lecturer stressed that the labels \(R_1\), \(R_2\), \(R_3\), and \(R_4\) are not universal. A component that is called \(R_1\) in one source may be assigned another label elsewhere. The correct approach is to define the impedances explicitly and maintain consistency throughout the calculation.

The lecture concluded with normalised second-order filter forms. The low-pass form was described using a denominator resembling:

\[
1+A_1s+B_1s^2
\]

The high-pass form has the corresponding \(s^2\) term in the numerator. Normalised coefficients are used to represent standard approximations such as Butterworth and Bessel filters. The normalised prototype can then be transformed to a desired cutoff frequency by applying an \(s\)-domain frequency transformation.

The lecturer made an important distinction between \(\omega_0\) and \(\omega_c\). For a Butterworth filter, the two can coincide in the form being used. For a Bessel filter, they do not generally coincide. The lecturer gave an example in which a Bessel-related \(\omega_0\) was approximately \(1.272\) in the normalised form, but this value should not be interpreted directly as the desired physical cutoff frequency.

The lecture also noted that \(Q\) can have different contextual meanings. In the usual filter context it may be associated with bandwidth and resonance. In a normalised coefficient table for a particular approximation, however, the same symbol may be used in a way tied to the prototype coefficients. Students should follow the definitions used by the course notes and the relevant filter table.

The lecturer indicated that an exam question may provide a circuit and ask students to reproduce it in low-pass or high-pass form. Simply identifying and drawing the correct filter form can earn marks. A second-order Bessel low-pass filter may be used as an exam example, in which case the Butterworth shortcut must not be used.

### Lecture 38

- Exam-layout remarks at 00:00–08:00 are explicitly from memory; approximate marks are NOT an official exact blueprint.
- Learn to turn normalised coefficient-table entries into the factorised filter transfer function, including odd-order combinations (08:00–28:00).
- Do not confuse a section natural-frequency parameter with the target real-world cutoff; Butterworth, Bessel and Chebyshev use different coefficients/normalisations (12:00–28:00).
- Sketch rectifier current before integrating, and include its zero-current intervals when computing full-period RMS (28:00–36:00).
- Use harmonic RMS values consistently and distinguish total RMS from fundamental RMS in THD calculations (36:00–48:00).
- Interpret a BLDC motor's rated/continuous torque, rated speed, maximum speed and load-torque intersection (48:00–51:00).

### Exam remarks and priorities
The lecturer describes a substantial rectifier question, mixed subparts involving rectifiers, BLDC, op-amp noise and AC coupling, then an active-filter question. He repeatedly qualifies mark estimates and his memory; use this as study-priority guidance, not guaranteed exact weights. He says verbal/conceptual subquestions test actual understanding and practical interpretation. Worked homework and previous papers overlap in methods even when the context makes a question look unfamiliar. At about 49–51 minutes he says he is not asking a BLDC commutation question this time but still wants students to learn the topic. This is a specific statement in this tutorial, not a permanent deletion of commutation from the course learning outcomes or all future exams.

### Filter tables and scaling
Read the table's filter family and order before using its coefficients. An odd-order low-pass transfer function can be represented by one first-order factor and the remaining second-order factors; the denominator orders must sum to the requested overall order. A zero quadratic coefficient indicates a first-order factor, not a missing second-order section. Relate the table's a and b coefficients to the standard section form, its frequency parameter and Q, while checking the exact normalisation in the lecture notes. After constructing the normalised shape, scale to the application's target cutoff and then choose the circuit implementation. Normalised section frequency, the complete filter's −3 dB cutoff and a real target cutoff are not interchangeable. The lecturer discusses Butterworth, Bessel and Chebyshev table use; do not assume only the familiar Butterworth case can be practised. Practical filter design trades amplitude attenuation against phase/time-response requirements.

### Rectifier waveforms and RMS
For the illustrated ideal three-phase, approximately constant-DC-current example, a phase current has positive, negative and zero intervals. Squaring removes its sign, not the intervals over which it is zero. Apply the full-period RMS integral or use a clearly justified symmetry reduction with the matching normalisation. Do not silently assume 50 Hz: the example explicitly uses a different supply frequency. Added source inductance spreads the current transitions through commutation; sketch the changed slope/overlap rather than adding unsupported ringing to a no-ringing model. Preserve the assumptions used in the original waveform before discussing how they change.

### FFT/THD method
Identify the fundamental and higher-harmonic values and whether the displayed quantities are RMS or peak. For consistent RMS components and no DC term, add squared harmonic magnitudes to get total current RMS. Read fundamental RMS separately rather than treating total RMS as the fundamental. With γ=I_rms/I_1,rms, THD=sqrt(γ²−1). The ratio must not be below one for a consistent set of components; a negative radicand signals an error. Larger relative higher harmonics generally indicate higher THD. FFT screenshots and numerical values must be read from the original problem/recording; the automated transcript's spoken arithmetic and units are not reliable enough to reproduce all worked numbers.

### BLDC operating point
Sketch and label the course's typical torque–speed curve, including rated speed, maximum speed, rated torque and continuous-torque capability. Explain how the load torque and available motor torque intersect and whether the required operating point fits the intended rated region. A graph copied without identifying what the operating-point intersection means is insufficient conceptual preparation.

## Equations and worked patterns

### Lecture 35

Transfer function:

H(s) = V_out(s) / V_in(s)

Frequency-domain substitution:

s = jω

Magnitude response:

|H(jω)|

Attenuation in decibels:

A_dB = -20 log₁₀|H(jω)|

Common −3 dB amplitude ratio:

|H| = 1/√2 ≈ 0.707

Resistor impedance:

Z_R = R

Inductor impedance:

Z_L = sL

Capacitor impedance:

Z_C = 1/(sC)

LC natural angular frequency:

ω₀ = 1/√(LC)

Equivalent form:

ω₀² = 1/(LC)

Approximate second-order damping and Q relationship:

ζ = 1/(2Q)

Normalised band-pass bandwidth, as presented in the lecture:

Bandwidth ≈ 1/Q

Second-order Butterworth quality factor:

Q = 1/√2

Approximate active-filter gain relationship for the discussed circuit:

A₀ = R₂/R₁

Bootstrap voltage relationship stated in the lecture:

V₁ = V₀

The transcript also describes both voltages as approximately:

V_N + V_CC/2

Filter definitions:

- Low-pass: passes low frequencies and attenuates high frequencies.
- High-pass: passes high frequencies and attenuates low frequencies.
- Band-pass: passes a selected band of frequencies.
- Band-stop/notch: attenuates a selected band while passing frequencies outside it.
- Pass band: intended transmission region.
- Stop band: intended attenuation region.
- Transition band: region between the pass band and stop band.
- Ripple: variation in magnitude within a nominal pass band or stop band.
- Filter order: generally related to the number of poles in the transfer function.
- Selectivity: the ability to separate the pass band from the stop band using a narrow transition band.
- Q factor: a measure associated with selectivity, resonance sharpness, and bandwidth.
- Linear phase: phase varying approximately linearly with frequency, corresponding to approximately constant group delay.

### Lecture 36

### Cutoff magnitude

At the conventional −3 dB cutoff point:

\[
|H(j\omega_c)| \approx 0.7071
\]

The value is often approximated as:

\[
|H(j\omega_c)| \approx 0.71
\]

The corresponding attenuation is:

\[
20\log_{10}(0.7071) \approx -3\ \text{dB}
\]

### Linear phase

A linear phase response can be represented as:

\[
\phi(\omega) = -\omega T
\]

where \(T\) is the time delay.

The important consequence is that every frequency component experiences the same delay.

### Group delay

Group delay is defined by:

\[
\tau_g(\omega) = -\frac{d\phi(\omega)}{d\omega}
\]

Constant group delay corresponds to a linear phase response.

### Capacitor impedance

In the Laplace domain:

\[
Z_C(s) = \frac{1}{sC}
\]

A capacitor therefore has integrating behaviour with respect to current.

### Inductor impedance

In the Laplace domain:

\[
Z_L(s) = sL
\]

An inductor therefore has differentiating behaviour with respect to voltage/current relationships.

### Ohm’s law

The resistor relationship used repeatedly in the derivation was:

\[
V = IR
\]

and therefore:

\[
I = \frac{V}{R}
\]

### Input impedance

The equivalent impedance of the active simulated-inductor circuit is obtained from:

\[
Z_{\text{in}} = \frac{V_1}{I_1}
\]

### Simplified simulated-inductance relationship

For the simplified equal-resistance arrangement described in the lecture:

\[
L = C R^2
\]

This relationship should not be assumed to be the complete general Antoniou formula. The exact resistor-dependent expression was not captured clearly in the transcript.

### Frequency conversion

For a frequency \(f\) in hertz:

\[
\omega = 2\pi f
\]

The lecturer reminded students to convert the cutoff frequency to radians per second before using angular-frequency equations.

### Filter types

- Low-pass: passes low frequencies and attenuates high frequencies.
- High-pass: attenuates low frequencies and passes high frequencies.
- Band-pass: passes a band of frequencies between lower and upper cutoff frequencies.
- Notch or band-stop: attenuates a band of frequencies while passing frequencies outside that band.

### Lecture 37

Impedance of a resistor:

\[
Z_R=R
\]

Impedance of a capacitor:

\[
Z_C=\frac{1}{sC}
\]

Angular frequency:

\[
\omega=2\pi f
\]

Second-order low-pass form:

\[
H_{\mathrm{LP}}(s)=\frac{K}{1+A_1s+B_1s^2}
\]

An equivalent standard form may be written as:

\[
H_{\mathrm{LP}}(s)
=
\frac{K\omega_0^2}
{s^2+\frac{\omega_0}{Q}s+\omega_0^2}
\]

The exact scaling and coefficient notation depend on the course convention.

Second-order high-pass form:

\[
H_{\mathrm{HP}}(s)
=
\frac{K s^2}
{s^2+\frac{\omega_0}{Q}s+\omega_0^2}
\]

Normalised low-pass prototype form discussed in the lecture:

\[
H(s)=\frac{1}{1+A_1s+B_1s^2}
\]

The transcript also rendered this expression in places as a form involving “\(1+A_1s+B_1s^2\)”; the exact placement of coefficient subscripts should be checked against the course notes.

Butterworth second-order quality factor:

\[
Q=\frac{1}{\sqrt{2}}
\]

Butterworth frequency relationship used in the lecture:

\[
\omega_0=\omega_c
\]

This equality should not be assumed for Bessel or Chebyshev filters.

Normalised frequency transformation:

\[
s\rightarrow \frac{s}{\omega_c}
\]

The transcript describes this transformation conceptually but does not preserve the complete written expression clearly enough to confirm the exact course notation.

Sallen-Key assumptions used in the derivation:

- Ideal op-amp input current is zero.
- The op-amp is treated as a voltage follower in the configuration shown.
- Therefore, the relevant op-amp input voltages are equal under the ideal negative-feedback assumptions.
- Kirchhoff’s current law is applied at the summing node.
- Each branch current is calculated from a voltage difference divided by its impedance.

The lecturer stated that the complete Sallen-Key transfer-function formula would be supplied on the exam sheet. The quantities students must remember are the impedance assignments and the component values corresponding to \(Z_1\), \(Z_2\), \(Z_3\), and \(Z_4\).

### Lecture 38

- Full-period RMS: I_rms = sqrt((1/T) integral over one period of i(t)² dt).
- Constant magnitude I_DC conducting for total fraction f of the full cycle, with zero otherwise: I_rms = I_DC sqrt(f). For the illustrated ideal phase-current duty f=2/3, this becomes I_DC sqrt(2/3); derive f from the actual waveform before applying it.
- For consistent harmonic RMS components without a DC component: I_rms² = sum over n≥1 of I_n,rms².
- THD = sqrt(sum over n≥2 of I_n,rms²)/I_1,rms = sqrt((I_rms/I_1,rms)²−1).
- A normalised low-pass denominator can be factorised into terms such as (1+a_i s+b_i s²); read coefficients and scaling from the specified family/table. This form is a learning pattern, not a substitute for a supplied table's exact convention.

## Warnings and deadlines

### Lecture 35

- This is a native Echo automated transcript with substantial speech-recognition errors. Terms such as “filter,” “Chebyshev,” “Bessel,” “Butterworth,” “voltage,” “op-amp,” and “MOSFET” were often transcribed incorrectly and have been corrected where the intended meaning was clear.
- The transcript does not include the lecture slides or circuit diagrams. Exact node labels, component connections, and some transfer-function equations cannot be reconstructed confidently from audio alone.
- The notation V₀, V₁, V_N, and V_CC is inferred from the spoken transcript and should be checked against the original slide.
- The bootstrap-circuit explanation is qualitative because the circuit topology was not captured in the transcript.
- The active low-pass filter derivation is incomplete in the transcript. The resistor-ratio gain relationship R₂/R₁ is stated, but the complete transfer function and circuit topology should be verified from the lecture material.
- Several spoken equations are ambiguous. In particular, the discussion of damping ratio, Q, bandwidth, and polynomial coefficients should be cross-checked against the course notes.
- The transcript sometimes uses “3 dB” as a general design reference and sometimes discusses pass-band ripple. These are related but not identical specifications; do not assume every filter mentioned has exactly 3 dB pass-band ripple.
- The lecture states that a buck converter contains a low-pass filtering section, but the converter itself also includes switching and voltage-conversion functions. The inductor-capacitor portion should not be treated as the complete converter.
- The lecturer referred to a specific active-filter implementation as an examination question, but the exact circuit was not identifiable from the transcript. Reviewing the corresponding slide is necessary before attempting that problem.

### Lecture 36

- The transcript repeatedly misrecognises “filter” as “philt(e)r” and misrecognises “Bessel,” “Chebyshev,” and “Antoniou.” These have been interpreted using the surrounding technical context.
- The transcript begins with the lecturer referring to “Lecture 17,” despite the source file being identified as Lecture 36. This appears to be a lecture-numbering or transcription issue.
- The lecturer gave contradictory statements about whether second-order active-filter design would be examined. One statement says it is definitely in the exam; a later statement explicitly says second-order active filters will not be examined. Confirm this from official course material or the lecturer’s final exam briefing.
- The exact generalised Butterworth/Chebyshev equations shown on slides were not captured reliably by the transcript. The notes therefore retain only relationships stated clearly in speech.
- The exact normalised group-delay formula and notation were not reliably transcribed.
- The transcript does not clearly preserve the complete Antoniou simulated-inductance formula with all resistor labels. The simplified relationship \(L = CR^2\) was stated under an equal-resistance assumption and should not be treated as the general formula without checking the lecture slides.
- The Chebyshev Type I and Type II discussion is ambiguous in the automated transcript. The lecturer clearly indicated that the ripple placement matters when a type is explicitly specified, but the transcript does not reliably identify which ripple placement was assigned to each type.
- The lecturer mentioned a correction to an op-amp diagram containing two negative inputs. The corrected circuit should be checked against the original lecture slides rather than reconstructed from the transcript alone.
- Several design-example variable labels, including \(C\), \(C_1\), and resistor labels, were corrected verbally during the lecture. The exact final assignments should be verified from the slide or circuit diagram before using the example for calculations.

### Lecture 37

- The source is a native Echo automated transcript with substantial recognition errors. Terms such as “filter,” “Butterworth,” “Bessel,” “Chebyshev,” “Sallen-Key,” “op-amp,” “cutoff,” “impedance,” and “voltage” were frequently misrecognised.
- Several equations were spoken while the lecturer referred to slides or circuit diagrams that are not included in the transcript. The exact coefficient subscripts, component labels, and full Sallen-Key transfer-function formula should be verified against the lecture slides or Learn notes.
- The transcript alternates between apparently inconsistent labels for resistors, capacitors, and impedances. The reliable principle is to define \(Z_1\) through \(Z_4\) from the actual circuit and remain consistent.
- The transcript contains a possible frequency example of \(50\text{ kHz}\), converted to \(2\pi(50\times10^3)\), but the associated component values and complete design data are missing.
- The lecturer referred to a Bessel example and a normalised value near \(1.272\), but the surrounding table and exact meaning of the value are not available in the transcript.
- The lecturer stated that some earlier analogue hardware implementation material was not examinable, while the Sallen-Key and normalised-filter material was examinable. The final exam scope should be confirmed against the official course material.
- The transcript says the complete Sallen-Key formula will be supplied on the exam sheet. Students should still confirm the current formula sheet and assessment instructions rather than relying solely on this lecture recording.
- The lecture ended before all planned examples could be completed. Further worked examples were intended for a later class or “chute” session.

### Lecture 38

Indexed and reviewed on 20 October 2026 from the recording-identity-verified native Echo transcript. The transcript is automated and has misheard technical words, numbers, units and equations. It also contains a late discussion questioning a factor of two in an RMS derivation: use the full-period definition with the actual waveform instead of copying an unverified intermediate integral. These are selective source-backed notes, not an official answer key. Exact waveform diagrams and table entries require the original notes or recording. Personal post-lecture discussion has not been included. The exam-layout remarks were explicitly qualified by the lecturer and are preserved as qualified.

## Recall questions

1. Lecture 35: What is the purpose of the bootstrap capacitor arrangement discussed at the beginning of the lecture?

2. Lecture 35: Why does the resistor in the bootstrap network appear to have an effectively infinite impedance to the relevant AC fluctuations?

3. Lecture 35: How does negative feedback in a voltage follower help isolate an input source from a load?

4. Lecture 35: What is the difference between a physical infinite resistance and an effective infinite impedance created by feedback?

5. Lecture 35: Explain why matching the capacitor values is important in the bootstrap arrangement.

6. Lecture 35: Define the transfer function of a filter and explain the significance of substituting s = jω.

7. Lecture 35: How is attenuation represented in decibels?

8. Lecture 35: What amplitude ratio corresponds to −3 dB?

9. Lecture 35: Sketch and label the magnitude responses of:

10. Lecture 35: On a filter-response diagram, identify the pass band, stop band, transition band, pass-band ripple, and stop-band attenuation.

11. Lecture 35: Why is pass-band ripple undesirable in many applications?

12. Lecture 35: What trade-off exists between transition-band width and ripple?

13. Lecture 35: Why does increasing filter order generally improve selectivity?

14. Lecture 35: What disadvantages can result from using a higher-order filter?

15. Lecture 35: Explain the main difference between Butterworth, Chebyshev Type I, Chebyshev Type II, and Bessel filters.

16. Lecture 35: Why is a Butterworth response described as maximally flat?

17. Lecture 35: What is the advantage of a Bessel filter in a communication or audio application?

18. Lecture 35: What is the purpose of normalising the cutoff frequency before designing a filter?

19. Lecture 35: How are normalised filter coefficients used to obtain physical component values?

20. Lecture 35: What is the relationship between Q and bandwidth for a normalised band-pass filter?

21. Lecture 35: What effect does increasing Q have on bandwidth and resonance?

22. Lecture 35: Why does Q = 1/√2 produce a flat second-order Butterworth response?

23. Lecture 35: Write the s-domain impedance of a resistor, inductor, and capacitor.

24. Lecture 35: Outline the procedure for deriving an LCR filter transfer function using impedances.

25. Lecture 35: What part of a buck converter acts as a low-pass filter, and what unwanted signal components does it remove?

26. Lecture 35: What is the natural angular frequency of an ideal LC network?

27. Lecture 35: How can an active filter provide gain as well as filtering?

28. Lecture 35: Why are op-amps useful in active filters when the load may change?

29. Lecture 35: What is the approximate asymptotic slope of a second-order low-pass or high-pass response?

30. Lecture 35: Why can an active filter be preferable to a passive LCR filter when a physical inductor would be large, expensive, or impractical?

31. Lecture 35: The lecturer indicated that a standard filter-response figure should be reproducible in the examination. Practise drawing it with all four filter types and clearly labelled pass bands, stop bands, transition bands, and attenuation limits.

32. Lecture 36: What does “maximally flat” mean for a Butterworth magnitude response?

33. Lecture 36: What is the magnitude ratio at the conventional −3 dB cutoff frequency?

34. Lecture 36: Why does increasing the order of a Butterworth filter produce a sharper transition?

35. Lecture 36: What trade-off does a Chebyshev filter make to achieve a sharper cutoff?

36. Lecture 36: How can filter efficiency be defined in two different ways?

37. Lecture 36: Why might a lower-order Chebyshev filter achieve the same attenuation as a higher-order Butterworth filter?

38. Lecture 36: What is the primary advantage of a Bessel filter?

39. Lecture 36: What is the relationship between linear phase and constant time delay?

40. Lecture 36: Define group delay in terms of the phase response.

41. Lecture 36: Why is a Bessel filter useful when waveform shape must be preserved?

42. Lecture 36: Sketch idealised low-pass, high-pass, band-pass, and notch magnitude responses. Label the passbands, stopbands, transition regions, and cutoff frequencies.

43. Lecture 36: How should ripple be represented on a generalised filter-response sketch?

44. Lecture 36: What uncertainty exists in the transcript concerning the exact ripple placement for Chebyshev Type I and Type II filters?

45. Lecture 36: What are the Laplace-domain impedances of a capacitor and an inductor?

46. Lecture 36: Why are active simulated inductors useful in practical filter design?

47. Lecture 36: Which components are used to construct the simulated-inductance circuit discussed in the lecture?

48. Lecture 36: What ideal op-amp assumption allows the circuit-current derivation to proceed?

49. Lecture 36: How is the input impedance of the simulated-inductance circuit calculated?

50. Lecture 36: Under the simplified equal-resistance assumption, how does the equivalent inductance depend on \(C\) and \(R\)?

51. Lecture 36: Why should the simulated-inductance circuit be treated as an \(L\) during most of the filter design process?

52. Lecture 36: Why did the lecturer warn against using the simplified Butterworth design method for Chebyshev and Bessel filters?

53. Lecture 36: What steps are required to convert a conventional LCR filter into an active filter using a simulated inductor?

54. Lecture 36: Why is a step response useful for characterising a filter or control-system transfer function?

55. Lecture 36: Which parts of the lecture were identified as likely examination material, and which parts were described as supplementary?

56. Lecture 37: What filter responses can be obtained by integrating a high-pass filter once and twice?

57. Lecture 37: Why can active filters be less sensitive to load impedance than passive LCR filters?

58. Lecture 37: What role does the op-amp integrator play in the practical filter implementation described in the lecture?

59. Lecture 37: Why is the complete hardware implementation of the integrator-based filter not the primary exam focus?

60. Lecture 37: What is the Sallen-Key topology used for?

61. Lecture 37: What assumptions about an ideal op-amp are used when deriving the Sallen-Key transfer function?

62. Lecture 37: Why is Kirchhoff’s current law useful in the Sallen-Key derivation?

63. Lecture 37: What are the impedances of a resistor and a capacitor in the \(s\)-domain?

64. Lecture 37: Why must students identify \(Z_1\), \(Z_2\), \(Z_3\), and \(Z_4\) from the actual circuit rather than relying on resistor labels alone?

65. Lecture 37: How does the component arrangement differ between a second-order low-pass and a second-order high-pass Sallen-Key filter?

66. Lecture 37: What is the general second-order low-pass transfer-function form?

67. Lecture 37: How does the numerator of a second-order high-pass transfer function differ from that of a low-pass transfer function?

68. Lecture 37: What is the quality factor \(Q\) for a second-order Butterworth filter?

69. Lecture 37: Under what condition can the Butterworth shortcut method be used?

70. Lecture 37: Why should the Butterworth shortcut not be applied automatically to Bessel or Chebyshev filters?

71. Lecture 37: What is the difference between \(\omega_0\) and \(\omega_c\)?

72. Lecture 37: Why can \(\omega_0=\omega_c\) for a Butterworth filter but not necessarily for a Bessel filter?

73. Lecture 37: What does normalising a filter prototype mean?

74. Lecture 37: How is a normalised prototype transformed to a desired cutoff frequency?

75. Lecture 37: If an exam question specifies a Bessel filter, what design method should be used instead of the Butterworth shortcut?

76. Lecture 37: What information did the lecturer say would be provided on the exam sheet?

77. Lecture 37: What information must students remember when using the supplied Sallen-Key transfer-function formula?

78. Lecture 37: Why is it useful to practise both low-pass and high-pass Sallen-Key designs?

79. Lecture 37: If different textbooks use different resistor labels, how can the circuit still be analysed correctly?

80. Lecture 38: Why do approximate spoken exam-mark estimates not constitute a published exact blueprint?

81. Lecture 38: Construct the denominator factors for an odd-order filter and check the resulting total order.

82. Lecture 38: Why can a Bessel section's natural-frequency parameter differ from the designed −3 dB cutoff?

83. Lecture 38: Derive RMS for a waveform that is +I_DC, zero, −I_DC and zero over specified intervals.

84. Lecture 38: How do you use an FFT to distinguish total RMS, fundamental RMS and THD?

85. Lecture 38: Why must γ be at least one in the stated THD relation?

86. Lecture 38: What changes in the current waveform when source inductance is added, and what assumptions are you making?

87. Lecture 38: Explain the motor/load torque intersection and why rated and maximum speed are different labels.

## Practice priorities

1. Lecture 35: attempt related homework/exam questions before looking at solutions; check the first conceptual error against the source. Tutor strategy, not an additional course requirement.

2. Lecture 36: attempt related homework/exam questions before looking at solutions; check the first conceptual error against the source. Tutor strategy, not an additional course requirement.

3. Lecture 37: attempt related homework/exam questions before looking at solutions; check the first conceptual error against the source. Tutor strategy, not an additional course requirement.

4. Lecture 38: attempt related homework/exam questions before looking at solutions; check the first conceptual error against the source. Tutor strategy, not an additional course requirement.

## Missing or incomplete

No missing transcript-backed sessions in this window. Automated transcription and diagram/equation caveats remain.

## Source manifest

- Lecture 35 (echo-lecture-35-35): complete; summary `4090c7bb52fb17a2042f483d77cb44f6b065fec7b3940c5967b3adb67b596dcd`; transcript `bb405630957bad2b1ad1b60843171525235cf7f6c6d392c6b9d5e5af89740398`; summary path `[local source path redacted]`
- Lecture 36 (echo-lecture-36-36): complete; summary `c19fd629e33de9822f4f20d17841b337d6779f4ae8fcc8aad81efb76bb71592a`; transcript `f3dfaa43aadd1cd8eb8db51016c5421fbd312ed5b2f5e47a6bcbd9f97914590b`; summary path `[local source path redacted]`
- Lecture 37 (echo-lecture-37-37): complete; summary `67a17aa1f3302b031706b4f980b9bed102b2832ea4ff08be51be6d0f875e4def`; transcript `b2598b9b8017421d9687062c744e31ae020d9744a9e4bc1d2e457ea0609c81d8`; summary path `[local source path redacted]`
- Lecture 38 (echo-lecture-38-38): complete; summary `689fcf96f88274b24c17a16e10ee26c15d4b89cbdee51f759b9c56fd0db03212`; transcript `1f4d2b237e30f2ae1be121be2f12723610929bf7b6fc9226b71cae53946a48dd`; summary path `[local source path redacted]`

# ENMT301-26W Lecture 50 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `b41b236c2337c85302a9a83cdfffe8d7b161bd4351036a03c90795b3b7426ccc`
Generated: 2026-06-06T06:55:38.678816+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:12 - 00:00:14] Okay, good afternoon everyone.
[00:00:14 - 00:00:17] As soon as you might have, we've got a tutorial at three
[00:00:17 - 00:00:20] back in engineering and so,
[00:00:20 - 00:00:23] you can come along, ask your questions about the tutorial questions
[00:00:23 - 00:00:25] about anything covered in lectures so far.
[00:00:25 - 00:00:31] So yesterday we started looking at analog filters,
[00:00:31 - 00:00:33] so in particular this RC circuit.
[00:00:33 - 00:00:38] And so we analyzed the RC circuit or any circuit,
[00:00:38 - 00:00:40] the transfer function in the Laplace domain,
[00:00:40 - 00:00:45] where we convert our impedance of the capacitor here
[00:00:45 - 00:00:49] to one over a C, and then we can use the voltage divider
[00:00:49 - 00:00:52] to get our transfer function, which is the output voltage
[00:00:52 - 00:00:56] over the input voltage.
[00:00:56 - 00:01:00] Okay, so that we get a transfer function here,
[00:01:00 - 00:01:08] one over one plus SDR, so that's got a single pole.
[00:01:08 - 00:01:13] Okay, and so one pole, it's in the left half plane,
[00:01:13 - 00:01:20] which means it's a stable system.
[00:01:20 - 00:01:22] And then from our transfer function,
[00:01:22 - 00:01:27] capillator vests, we can calculate our impulse response,
[00:01:27 - 00:01:32] little h of t with an inverse of the pass transform.
[00:01:32 - 00:01:36] So you can do the integral, but it's much easier to use
[00:01:36 - 00:01:38] our pairs of tables and properties.
[00:01:39 - 00:01:42] And so when we do that inverse of the pass transform,
[00:01:42 - 00:01:47] we get a negative exponential starting at t is zero.
[00:01:49 - 00:01:53] Okay, and so the output of our filter is the input
[00:01:53 - 00:01:57] convolved with this impulse response.
[00:01:57 - 00:02:00] And because of the convolution theorem,
[00:02:00 - 00:02:03] because we've got a convolution and the time domain,
[00:02:03 - 00:02:06] we have a multiplication in the frequency domain.
[00:02:07 - 00:02:10] So the output spectrum is equal to the input spectrum
[00:02:10 - 00:02:14] multiplied by our frequency response of the filter.
[00:02:17 - 00:02:21] Okay, as then we got here, we're we've plotted
[00:02:21 - 00:02:26] and blew the impulse response for a particular case
[00:02:26 - 00:02:30] we've chosen R and C such that the time constant tau
[00:02:30 - 00:02:31] is equal to one second.
[00:02:33 - 00:02:38] And then an orange I have now plotted,
[00:02:39 - 00:02:42] time constant of 0.5 after it was pointed out
[00:02:42 - 00:02:44] at the end of the lecture yesterday,
[00:02:44 - 00:02:45] that I've made a boo boo.
[00:02:45 - 00:02:50] So here R, C is 0.5, that's the time constant.
[00:02:50 - 00:02:54] And then the impulse response has its maximum of one over tau,
[00:02:54 - 00:02:57] so one over 0.5 gives us two.
[00:02:57 - 00:02:59] And so with that smaller time constant,
[00:02:59 - 00:03:04] this impulse response is then decaying to zero more quickly.
[00:03:09 - 00:03:11] Okay, and our impulse response there has units
[00:03:11 - 00:03:16] of one over seconds.
[00:03:16 - 00:03:18] Okay, the next thing we looked at was the step response.
[00:03:19 - 00:03:24] And so the step response is the integral of the impulse response.
[00:03:26 - 00:03:28] And so we can get this at the time domain
[00:03:28 - 00:03:31] as the inverse of the pass transform
[00:03:31 - 00:03:34] of our transfer function H of S divided by S.
[00:03:36 - 00:03:39] And so we can solve for our step response
[00:03:39 - 00:03:42] by making use of partial fractions.
[00:03:43 - 00:03:46] So we get then one minus a negative exponential
[00:03:47 - 00:03:49] for our step response.
[00:03:51 - 00:03:54] And so then I think this is where we finished yesterday.
[00:03:54 - 00:03:58] So this is in the step response for a blue,
[00:03:58 - 00:04:01] my plot and Python with a time constant tau,
[00:04:01 - 00:04:02] R equals one.
[00:04:03 - 00:04:05] And I didn't make mistake for this one.
[00:04:05 - 00:04:07] So here I've got our C is 0.5.
[00:04:07 - 00:04:09] And with that smaller time constant,
[00:04:10 - 00:04:15] we rise more quickly, but still the same value of one.
[00:04:21 - 00:04:22] Okay, so that is,
[00:04:23 - 00:04:26] we're at with our n log filter.
[00:04:27 - 00:04:29] So this is a low pass filter
[00:04:29 - 00:04:32] we're moving the low frequencies.
[00:04:32 - 00:04:35] So keeping the low frequencies and removing the high frequencies.
[00:04:36 - 00:04:38] And so the next thing we're gonna look at
[00:04:38 - 00:04:40] is something known as the frequency response,
[00:04:42 - 00:04:51] which is H of F.
[00:04:51 - 00:04:53] Okay, so the frequency response
[00:04:54 - 00:04:56] is just gonna be looking at the steady state.
[00:04:56 - 00:04:58] So we're not looking at the transient response
[00:04:58 - 00:05:01] like we do in the last domain.
[00:05:03 - 00:05:05] And so in the last domain,
[00:05:05 - 00:05:10] we have our complex variable S is equal to sigma,
[00:05:12 - 00:05:17] which determines whether our signal is decaying
[00:05:17 - 00:05:21] if signal resistance 0 or increasing,
[00:05:21 - 00:05:22] if sigma is greater than 0.
[00:05:23 - 00:05:26] And then this is a complex,
[00:05:26 - 00:05:28] so it's plus J,
[00:05:28 - 00:05:30] complex number and omega,
[00:05:30 - 00:05:32] our angle frequency.
[00:05:33 - 00:05:39] So in the case that we are in steady state,
[00:05:39 - 00:05:43] we have sigma is 0.
[00:05:43 - 00:05:51] That means our complex variable S is equal to J omega.
[00:05:51 - 00:05:53] Okay, so we've got this transfer function
[00:05:53 - 00:05:58] that we got at the start by analyzing our circuit.
[00:05:58 - 00:06:04] That voltage divider, that's our transfer function.
[00:06:04 - 00:06:07] So here, H of S was our transfer function
[00:06:07 - 00:06:12] that we got yesterday.
[00:06:12 - 00:06:16] And we can convert that to our frequency response.
[00:06:16 - 00:06:18] So again, capital H.
[00:06:18 - 00:06:22] And this you can write a function of J to pi F
[00:06:23 - 00:06:28] or H of F.
[00:06:28 - 00:06:32] Okay, so here, S is complex,
[00:06:33 - 00:06:34] that's the complex frequency.
[00:06:34 - 00:06:37] And F is our frequency and Hertz,
[00:06:37 - 00:06:43] so that is real.
[00:06:43 - 00:06:44] Okay, so this particular case,
[00:06:46 - 00:06:47] low pass filter here,
[00:06:47 - 00:06:52] we had, from yesterday, H of S was equal to one over S,
[00:06:54 - 00:06:56] C R plus one.
[00:06:57 - 00:06:59] So that means our frequency response, H of F,
[00:06:59 - 00:07:02] is equal to one over,
[00:07:02 - 00:07:05] so we replace S by J to pi F.
[00:07:05 - 00:07:09] So we've got one over J to pi F,
[00:07:09 - 00:07:13] C plus one.
[00:07:13 - 00:07:18] Okay, so the frequency response H of F
[00:07:18 - 00:07:22] is the major in this case,
[00:07:22 - 00:07:30] but our frequency variable F is real.
[00:07:30 - 00:07:35] Okay, so this transfer function conversion
[00:07:36 - 00:07:39] is not always valid, so if we had say,
[00:07:39 - 00:07:43] an integrator H of S is one over S,
[00:07:43 - 00:07:48] we would then end up with one over zero
[00:07:50 - 00:07:51] when we do that conversion,
[00:07:51 - 00:07:54] so H of zero be undefined.
[00:07:55 - 00:07:57] So to make this conversion,
[00:07:57 - 00:08:01] we have to have a stable
[00:08:01 - 00:08:09] and linear time invariant system.
[00:08:09 - 00:08:14] Okay, so this frequency response here, H of F is complex.
[00:08:14 - 00:08:18] So it's got a magnitude and a phase.
[00:08:19 - 00:08:24] So we wanna separate that out into its magnitude response
[00:08:24 - 00:08:28] and its phase response,
[00:08:28 - 00:08:29] because then that will tell us
[00:08:30 - 00:08:33] what happens to an input frequency,
[00:08:33 - 00:08:36] input signal of a certain frequency.
[00:08:36 - 00:08:38] So we do a little bit of maths here to generate
[00:08:40 - 00:08:42] our phase angle theta and our magnitude
[00:08:42 - 00:08:46] or gain of our frequency response.
[00:08:47 - 00:08:51] Okay, so let's consider our complex plane here,
[00:08:51 - 00:08:55] so we've got real on the x-axis imaginary
[00:08:55 - 00:08:57] on the y-axis.
[00:08:58 - 00:09:01] And so we have then,
[00:09:02 - 00:09:05] for some point here in the complex space,
[00:09:05 - 00:09:07] we have an angle feature here.
[00:09:08 - 00:09:15] This is the imaginary part of H of F
[00:09:18 - 00:09:23] and along the x-axis we have the real part of H of F.
[00:09:30 - 00:09:35] Okay, so we can get the phase and magnitude
[00:09:37 - 00:09:39] with a bit of high school geometry,
[00:09:39 - 00:09:41] versus triangle.
[00:09:42 - 00:09:44] So then our phase angle theta
[00:09:46 - 00:09:51] is equal to then, that's the opposite of adjacent.
[00:09:52 - 00:09:57] So this is the inverse tangent or octangent
[00:09:57 - 00:10:02] of the imaginary part of our frequency response H of F
[00:10:03 - 00:10:08] over the real part of our frequency response H of F.
[00:10:14 - 00:10:22] Okay, so it's the phase and then the magnitude
[00:10:25 - 00:10:29] of our frequency response H of F is then the,
[00:10:33 - 00:10:37] call that thing, high-pot values of that triangle
[00:10:37 - 00:10:39] so we can get that with Pythagoras.
[00:10:40 - 00:10:45] So this is then the positive square root of the real part
[00:10:48 - 00:10:55] of H of F squared plus the imaginary part
[00:10:55 - 00:11:06] of H of F squared.
[00:11:06 - 00:11:09] Okay, so this one way of doing it, the other one.
[00:11:12 - 00:11:15] If we have two complex numbers, sorry,
[00:11:15 - 00:11:23] if we have a complex number, should I write this?
[00:11:23 - 00:11:27] Here z equal to A plus jB.
[00:11:30 - 00:11:35] It's complex conjugate z star is equal to A minus jB.
[00:11:38 - 00:11:45] So then z z star, which is the magnitude squared
[00:11:46 - 00:11:51] is equal to the square root of A squared plus B squared.
[00:11:59 - 00:12:02] Okay, so we can also write then our magnitude
[00:12:02 - 00:12:07] of our frequency response H of F is equal to the square root
[00:12:07 - 00:12:12] of our frequency response H of F times the complex
[00:12:12 - 00:12:34] conjugate H of F.
[00:12:34 - 00:12:38] Okay, so we'll go through, get that you're writing.
[00:12:38 - 00:12:41] And now calculate the magnitude M phase four
[00:12:46 - 00:12:53] Rc filter, okay, so using this approach.
[00:12:53 - 00:13:00] So we now have here this is a magnitude first.
[00:13:02 - 00:13:09] So then we've got our frequency response H of F
[00:13:09 - 00:13:14] is equal to one over j2 pi Fc plus one.
[00:13:14 - 00:13:26] If C plus one, okay, so then the magnitude of H of F
[00:13:27 - 00:13:35] is equal to the magnitude of all this j2 pi Fc plus one.
[00:13:42 - 00:13:48] Okay, so what's the magnitude of the numerator?
[00:13:48 - 00:13:50] One, yep, what's the metric question?
[00:13:50 - 00:13:52] And then the magnitude of the denominator,
[00:13:53 - 00:14:02] we can get then as the square root of the real part squared,
[00:14:04 - 00:14:13] says one, one, one, and then plus the
[00:14:15 - 00:14:16] imaginary part squared.
[00:14:16 - 00:14:20] So this is in one plus two times pi times the frequency
[00:14:20 - 00:14:29] if times the resistance R times the capacitance C squared.
[00:14:29 - 00:14:33] Okay, so it tells us the magnitude of the frequency response.
[00:14:33 - 00:14:38] That's gonna tell us the magnitude of the filter
[00:14:38 - 00:14:42] for different frequency values if here.
[00:14:42 - 00:14:46] So as if gets larger, because on the denominator,
[00:14:46 - 00:14:50] the magnitude of actually if is going to get smaller.
[00:14:50 - 00:14:55] Okay, so that means that this is indeed a low pass filter.
[00:14:56 - 00:15:00] The high frequencies are magnitude is gonna get lower.
[00:15:00 - 00:15:05] And we'll plot that for a particular value of R and C.
[00:15:06 - 00:15:11] Shortly, we've got a both plot.
[00:15:11 - 00:15:15] Okay, so this is the magnitude.
[00:15:15 - 00:15:22] And then the phase we get from our angles.
[00:15:25 - 00:15:27] Okay, so first we need to separate it into real
[00:15:27 - 00:15:28] and imaginary parts.
[00:15:28 - 00:15:32] So we've got here our actual F is equal to one over j2 to the
[00:15:37 - 00:15:41] pi if C plus one.
[00:15:43 - 00:15:46] Okay, so we've got a complex number on the denominator.
[00:15:46 - 00:15:48] So it's about messy for separating it into the real
[00:15:48 - 00:15:50] imaginary parts.
[00:15:50 - 00:15:55] So how should we try and simplify this to get into a real
[00:15:55 - 00:16:02] part plus the imaginary part?
[00:16:02 - 00:16:03] Exactly.
[00:16:03 - 00:16:08] So we're gonna multiply top and bottom by our complex conjugate.
[00:16:08 - 00:16:13] So one minus j2 pi if C over one minus j2 pi if C.
[00:16:21 - 00:16:29] Okay, so that's the complex conjugate of the denominator.
[00:16:38 - 00:16:42] Okay, because we're multiplying by some of the same
[00:16:42 - 00:16:44] and the numerator in denominator.
[00:16:44 - 00:16:45] So we're gonna multiply by one.
[00:16:45 - 00:16:48] So that's all good.
[00:16:48 - 00:16:53] So then we have our frequency response h of F.
[00:16:55 - 00:17:00] We can write then as numerator becomes one minus j2 pi if C over
[00:17:08 - 00:17:09] a squared plus b squared.
[00:17:09 - 00:17:14] So this is one plus 2 pi if C squared.
[00:17:18 - 00:17:25] Okay, so now we've got a real number in the denominator.
[00:17:25 - 00:17:28] So it's easier to then separate h of F into a real
[00:17:28 - 00:17:31] part and in the imaginary part.
[00:17:32 - 00:17:41] So the real part of h of F is equal to one over one plus
[00:17:41 - 00:17:46] 2 pi if C squared.
[00:17:46 - 00:17:56] And the imaginary part of h of F is equal to minus 2 pi if C over one
[00:18:04 - 00:18:12] plus 2 pi if C squared.
[00:18:12 - 00:18:16] Okay, so then from the previous slide when we were looking at how to get our
[00:18:16 - 00:18:24] magnitude, this is the arc tangent of the imaginary part of h of F over
[00:18:26 - 00:18:37] the real part of h of F.
[00:18:37 - 00:18:41] Okay, so when we substitute it in the real part in the imaginary part,
[00:18:41 - 00:18:46] the denominator is cancel and so then we're gonna get this is then equal to the
[00:18:46 - 00:18:53] inverse tan of minus 2 pi if C.
[00:18:59 - 00:19:05] Okay, so the phase of the frequency response is important.
[00:19:05 - 00:19:12] That's gonna tell us the delay of the output of the filter relative to the input
[00:19:12 - 00:19:14] to the filter.
[00:19:14 - 00:19:18] And this is gonna change with frequency here.
[00:19:18 - 00:19:23] And it's also gonna change with our circuit values for the resistance and the
[00:19:23 - 00:19:33] capacitance.
[00:19:33 - 00:19:37] Okay, so we're gonna plot this in a sec with a bold plot.
[00:19:37 - 00:19:44] So both magnitude and phase.
[00:19:44 - 00:19:49] Okay, and so I'm gonna plot them as a function of frequency if and
[00:19:49 - 00:19:50] hertz.
[00:19:50 - 00:19:54] Lots of other people would plot this as a function of angular frequency in
[00:19:54 - 00:19:56] omega, so radius per second.
[00:19:56 - 00:20:03] And then to the magnitude we're gonna plot a log log scale.
[00:20:03 - 00:20:07] So the y-axis, the magnitude, we're gonna plot in this of L's and the frequency,
[00:20:07 - 00:20:12] the log of hertz and the phase, we're gonna plot similar.
[00:20:12 - 00:20:18] So the angle isn't logged but the frequency axis is.
[00:20:18 - 00:20:26] And so the dv value here is we're gonna get the magnitude of our frequency
[00:20:26 - 00:20:50] response and dv is we're gonna take 20 log to the base 10 of our magnitude h of f.
[00:20:50 - 00:20:56] Okay, so now we're ready to do some plotting of the magnitude and phase for
[00:20:56 - 00:21:07] our frequency response.
[00:21:07 - 00:21:20] Okay, so we've got then on the left we've got our magnitude of h of f against
[00:21:20 - 00:21:29] frequency and we've got then our phase angle theta on the right with frequency.
[00:21:29 - 00:21:35] Okay, and again I'm gonna make life simple by cheating and so our is equal to 100
[00:21:35 - 00:21:49] kilo ohms, our capacitor is 10 microfarads and so RC is equal to 1.
[00:21:49 - 00:21:56] Okay, so the very first thing we need to say is that so the low frequencies here,
[00:21:56 - 00:22:04] the lads pass.
[00:22:04 - 00:22:13] Okay, so if we've got 0 dv that means the magnitude is 1.
[00:22:13 - 00:22:18] So log to base 10 of 1 gives us 0.
[00:22:18 - 00:22:23] Where we have 0.0 dv that means the magnitude is 1 which means those frequencies are just
[00:22:23 - 00:22:24] passing straight through the filter.
[00:22:24 - 00:22:29] They're not being attenuated.
[00:22:29 - 00:22:39] Okay, but for these higher frequencies so from about 0.1 hertz we'll go through exactly
[00:22:39 - 00:22:56] where in a sec these frequencies are attenuated.
[00:22:56 - 00:23:05] Okay, so the dotted line here is indicating the cutoff frequency of the filter so this
[00:23:05 - 00:23:06] is fc.
[00:23:06 - 00:23:16] Okay, that's kind of the break point where we go from the frequencies being attenuated
[00:23:16 - 00:23:22] to being attenuated.
[00:23:22 - 00:23:29] Okay, so this distance here from here to here and the magnitude plot at the cutoff frequency
[00:23:29 - 00:23:32] is 3 decibels.
[00:23:32 - 00:24:02] Okay, so at that point the magnitude of our filter at the cutoff frequency is equal to minus
[00:24:02 - 00:24:04] 3 db.
[00:24:04 - 00:24:21] Okay, and so this 3 dB comes from, for consider this in logs 20 times log to the base 10 of
[00:24:21 - 00:24:31] 1 over square root 2 gives us our minus 3.
[00:24:31 - 00:24:42] Okay, so this 1 over square root 2 is equal to about 0.0707.
[00:24:42 - 00:24:50] Okay, so at our cutoff frequency we minus 3 decibels down in terms of the magnitude for
[00:24:50 - 00:24:56] that frequency or we have about 0.7 of the initial amplitude for that frequency.
[00:24:56 - 00:25:03] Okay, what else do we need to know?
[00:25:03 - 00:25:18] We need to know that we have here if we consider the slope of our magnitude where we're
[00:25:18 - 00:25:27] attenuating it, what's that slope equal to?
[00:25:27 - 00:25:32] Yep, you're answering the next question down the line.
[00:25:32 - 00:25:35] So what's the numerical value here of the slope?
[00:25:35 - 00:25:36] Minus 20.
[00:25:36 - 00:25:37] Minus 20, exactly.
[00:25:37 - 00:25:49] So we've got the slope here of the rolloff to the slope, rolloff equals minus 20
[00:25:49 - 00:26:11] equals the decays and so that is then means that this is a first filter which is here
[00:26:11 - 00:26:20] we've got one pole because we've got one capacitor or a nectar.
[00:26:20 - 00:26:41] Okay, we have to do so we have then the if we go back to consider our frequency response
[00:26:43 - 00:26:53] Here we can use the top equation here we have
[00:26:54 - 00:26:58] We'll do the magnitude
[00:27:00 - 00:27:07] We can work out the
[00:27:08 - 00:27:10] Cut off frequency
[00:27:10 - 00:27:17] F here
[00:27:17 - 00:27:28] So at the 3 dB point so I'll go back as like as I'm myself enough space at
[00:27:28 - 00:27:30] 3 dB
[00:27:30 - 00:27:31] down
[00:27:31 - 00:27:33] the magnitude of H of F
[00:27:34 - 00:27:38] is equal to
[00:27:38 - 00:27:47] 1 over root 2 at that frequency
[00:27:48 - 00:27:50] So this is the cut off frequency
[00:27:50 - 00:28:03] Fc so what value of
[00:28:06 - 00:28:11] Fc or what value of F here do we need
[00:28:11 - 00:28:15] the magnitude of H of F to be
[00:28:15 - 00:28:17] 1 over root 2
[00:28:17 - 00:28:30] So we need this here to be equal 1 so that means the cut off frequency is going to be equal to 1 over
[00:28:31 - 00:28:33] 2 pi
[00:28:33 - 00:28:34] C
[00:28:34 - 00:28:43] Okay, so in terms of angular frequencies this would then be our
[00:28:44 - 00:28:46] Omega C is one over
[00:28:47 - 00:28:48] Rc
[00:28:48 - 00:28:52] Okay, so if C is 2 pi Rc
[00:28:53 - 00:28:55] Sorry 1 over 2 pi Rc
[00:28:56 - 00:28:58] 2 pi
[00:28:58 - 00:29:03] Rc times 1 over 2 pi Rc gives us 1 so we have 1 plus 1 squared
[00:29:03 - 00:29:05] There's 2 so we have 1 over square root of 2
[00:29:06 - 00:29:12] Which is the magnitude for the 3 dB point so that gives us our?
[00:29:13 - 00:29:22] Cut off frequency so then I'll just go back to our graphs again, so our
[00:29:22 - 00:29:26] cut off frequency Fc
[00:29:27 - 00:29:29] We just showed was 1 over 2 pi
[00:29:30 - 00:29:35] C so in this particular case we have Rc was equal to 1 so
[00:29:35 - 00:29:38] Fc is equal to 1 over 2 pi or
[00:29:40 - 00:29:42] 0.16
[00:29:42 - 00:29:43] Hertz
[00:29:43 - 00:29:49] Okay, and so then if you look at the diagrams here 10 to minus 1 is 0.1
[00:29:49 - 00:29:55] The next tick along is then 0.2 so this dot is a vertical line of
[00:29:56 - 00:30:00] Fc is at 0.16 Hertz so that's the cut off frequency for the filter
[00:30:00 - 00:30:04] kind of the defined frequency where you go from
[00:30:05 - 00:30:11] letting frequencies through low pass and in attenuating the higher frequencies
[00:30:11 - 00:30:23] Okay, so what's the phase at our cutoff frequency?
[00:30:23 - 00:30:37] So this one here cut off frequency we then have this value here is
[00:30:38 - 00:30:50] minus 45 degrees. I can show that why that should be the case
[00:30:51 - 00:30:53] go back to this equation here so
[00:30:54 - 00:31:00] At for consider's top equation here at
[00:31:03 - 00:31:05] Fc equals
[00:31:05 - 00:31:07] 1 over 2 pi Rc
[00:31:09 - 00:31:12] We have then h of F is equal to 1
[00:31:14 - 00:31:21] So this 2 pi Fc cancels out to be 1 so we have then 1 over j plus 1
[00:31:23 - 00:31:28] So then our phase angle theta is equal to
[00:31:30 - 00:31:33] roughly write this in terms of
[00:31:37 - 00:31:40] phases or in the polar form
[00:31:40 - 00:31:48] Pn we have on the top we have one and angle zero degrees and on the bottom we have a magnitude of
[00:31:49 - 00:31:51] root 2
[00:31:51 - 00:31:53] at
[00:31:54 - 00:31:59] 45 degrees so we can say that
[00:32:00 - 00:32:04] h of F at the cutoff frequency is then has a magnitude of 1 over root 2 and
[00:32:06 - 00:32:08] It's angle to 0 minus 45
[00:32:08 - 00:32:10] is minus 45 degrees
[00:32:14 - 00:32:16] okay, so
[00:32:16 - 00:32:20] The analysis in equation matches the figures that I've been plotted out from
[00:32:22 - 00:32:24] Python for this vode plot
[00:32:26 - 00:32:28] Okay, but so for other filter types
[00:32:30 - 00:32:35] So you can also have high pass filters if we swap R and see around or we can generate a
[00:32:36 - 00:32:40] low pass filter with an inductor in series with a resistive
[00:32:41 - 00:32:43] We'll swap those around we can have a high pass filter as well
[00:32:44 - 00:32:48] The same process applies we can work out the cutoff frequency
[00:32:49 - 00:32:51] by considering
[00:32:52 - 00:32:53] the
[00:32:53 - 00:32:54] magnitude of
[00:32:54 - 00:33:00] the frequency response
[00:33:00 - 00:33:05] Okay, so let's go back to the bode plot and the case people need to write some stuff more stuff down from there
[00:33:21 - 00:33:23] okay
[00:33:23 - 00:33:29] So we've got a couple more things to do with our Rc filter and then we can move on and look at different filter types
[00:33:30 - 00:33:32] and different higher order types as well
[00:33:37 - 00:33:45] Okay, so something called the DC response. So this is what happens when we had a constant value into our filter
[00:33:49 - 00:33:50] so
[00:33:50 - 00:33:54] If we consider what happens with our
[00:33:58 - 00:34:01] frequency response with the fine previously is 1 over
[00:34:04 - 00:34:06] j 2 pi if
[00:34:06 - 00:34:08] c plus 1
[00:34:09 - 00:34:11] So our DC response
[00:34:11 - 00:34:16] So the response of our filter for a frequency of 0
[00:34:17 - 00:34:19] What's it going to be in this case?
[00:34:19 - 00:34:25] But so we've got 1 over 0 plus 1 that gives us 1
[00:34:28 - 00:34:29] Okay
[00:34:29 - 00:34:31] So that is
[00:34:31 - 00:34:32] good
[00:34:32 - 00:34:34] That's what you expect for a low pass filter
[00:34:36 - 00:34:38] And if you go back to the bode plot here
[00:34:39 - 00:34:42] Well, we can never get back to DC on the log scale but
[00:34:42 - 00:34:44] So
[00:34:44 - 00:34:47] Zero decibels corresponds to value of 1
[00:34:51 - 00:34:53] Okay, so
[00:34:54 - 00:34:56] If we're making a filter from
[00:34:57 - 00:35:01] resistors inductors and capacitors only. It's known as a passive filter
[00:35:02 - 00:35:07] We can't have our DC gain to be greater than 1
[00:35:08 - 00:35:10] So we can't be somehow amplifying a DC
[00:35:11 - 00:35:14] With just resistors capacitors inductors but
[00:35:16 - 00:35:18] We can with if we start putting
[00:35:20 - 00:35:22] Nonlinear devices into our filter so we can with
[00:35:24 - 00:35:25] Opamps
[00:35:25 - 00:35:31] we've done that
[00:35:31 - 00:35:34] So definitely in up to 70 you can
[00:35:36 - 00:35:39] Create a man before with an opamp fairly easily
[00:35:41 - 00:35:46] Okay, so this response pretty straightforward and then lastly we'll look at the
[00:35:47 - 00:35:49] AC response of the filter
[00:35:52 - 00:35:54] Okay, so
[00:35:54 - 00:35:56] When we define signals previously
[00:35:58 - 00:36:00] We showed that
[00:36:00 - 00:36:02] We can represent a cosine
[00:36:02 - 00:36:04] So here this is going to be
[00:36:04 - 00:36:07] V1 of t. This is an voltage as function of time
[00:36:09 - 00:36:10] has some
[00:36:10 - 00:36:12] amplitude
[00:36:12 - 00:36:18] called V1
[00:36:18 - 00:36:20] And this is a cosine
[00:36:20 - 00:36:22] 2 pi
[00:36:22 - 00:36:23] frequency f1
[00:36:24 - 00:36:26] t plus some phase angle
[00:36:27 - 00:36:30] phi 1
[00:36:30 - 00:36:33] So the phase is a shift we keep shifting a cosine
[00:36:33 - 00:36:35] that will actually become a sine
[00:36:36 - 00:36:39] And if one is our frequency
[00:36:40 - 00:36:47] Okay, so it's the time to maintain
[00:36:49 - 00:36:55] Signal if we assume the input is a sine you side of a constant frequency
[00:36:56 - 00:36:59] We can represent this as a phaser
[00:36:59 - 00:37:01] So the phase that we're going to have
[00:37:02 - 00:37:03] capital V1
[00:37:04 - 00:37:06] And all right, a tilde on top to denote
[00:37:07 - 00:37:09] tilde is a squiggle
[00:37:09 - 00:37:11] tilde
[00:37:11 - 00:37:13] to denote
[00:37:13 - 00:37:16] the phaser
[00:37:16 - 00:37:18] So then V1
[00:37:18 - 00:37:22] We can write as then being equal to
[00:37:22 - 00:37:24] the magnitude V1
[00:37:25 - 00:37:26] times e
[00:37:26 - 00:37:28] to the j
[00:37:28 - 00:37:28] phi 1
[00:37:28 - 00:37:31] So we just write it in terms of
[00:37:31 - 00:37:32] its magnitude and phase
[00:37:34 - 00:37:35] Or we can write it as
[00:37:37 - 00:37:37] V1
[00:37:39 - 00:37:39] angle
[00:37:40 - 00:37:41] phi 1
[00:37:44 - 00:37:47] Okay, so this is a phaser
[00:37:47 - 00:37:54] And it's assumed to have a frequency of f1
[00:38:02 - 00:38:04] Okay, so if we've got a
[00:38:05 - 00:38:07] linear filter, so things aren't
[00:38:08 - 00:38:09] changing in times
[00:38:10 - 00:38:13] our
[00:38:13 - 00:38:15] RC filter as an example of that
[00:38:16 - 00:38:18] The output of our filter
[00:38:19 - 00:38:21] will have the same frequency as the input
[00:38:21 - 00:38:24] The linear filter is not going to change the frequency
[00:38:24 - 00:38:27] Might change the phase and the magnitude
[00:38:27 - 00:38:29] But it doesn't change the frequency
[00:38:31 - 00:38:34] Okay, so if we just draw a little diagram here, so if our filter
[00:38:35 - 00:38:37] A to the f
[00:38:39 - 00:38:40] And we've got
[00:38:41 - 00:38:43] some voltage V1 of t
[00:38:45 - 00:38:46] input to our filter
[00:38:47 - 00:38:48] filter
[00:38:49 - 00:38:51] Then the output
[00:38:51 - 00:38:55] which is then
[00:38:56 - 00:38:56] V2 of t
[00:39:00 - 00:39:03] is going to be the same frequency as the input
[00:39:04 - 00:39:04] And our filter
[00:39:06 - 00:39:07] H of f
[00:39:07 - 00:39:09] This is the frequency response we've looked at before
[00:39:09 - 00:39:11] is itself
[00:39:11 - 00:39:13] complex that's going to have a magnitude
[00:39:13 - 00:39:14] H of f
[00:39:14 - 00:39:16] and some
[00:39:16 - 00:39:17] phase angle
[00:39:17 - 00:39:19] theta
[00:39:19 - 00:39:21] And c to this is going to be a function of frequency
[00:39:21 - 00:39:28] as well
[00:39:28 - 00:39:30] Okay, so what that means at the output
[00:39:30 - 00:39:32] our output phase of V2
[00:39:34 - 00:39:35] is equal to
[00:39:36 - 00:39:37] the magnitude of our filter
[00:39:38 - 00:39:39] this H
[00:39:41 - 00:39:42] of frequency f1
[00:39:42 - 00:39:44] one
[00:39:44 - 00:39:46] times the phase of the filter
[00:39:49 - 00:39:50] theta frequency f1
[00:39:51 - 00:39:54] times the magnitude of our input V1
[00:39:55 - 00:39:57] and the phase angle for our input
[00:39:59 - 00:39:59] phi1
[00:40:04 - 00:40:06] Okay, so hopefully we'll see in before, but if you go phaser
[00:40:06 - 00:40:09] and you want to go back to the time domain
[00:40:09 - 00:40:11] so to get little V of t
[00:40:12 - 00:40:13] if we take the real part
[00:40:15 - 00:40:16] of our phaser V2
[00:40:18 - 00:40:19] and multiply by
[00:40:20 - 00:40:21] either j on the kt
[00:40:21 - 00:40:24] or either j to pi
[00:40:24 - 00:40:25] if 1 t
[00:40:27 - 00:40:29] so that restores the frequency
[00:40:30 - 00:40:32] to our phaser
[00:40:33 - 00:40:36] as this will give us then the time domain
[00:40:37 - 00:40:39] output of the filter V2 of t
[00:40:40 - 00:40:45] so the output of our filter is determined by
[00:40:45 - 00:40:46] the magnitude of the input signal
[00:40:47 - 00:40:50] the magnitude of the frequency response
[00:40:51 - 00:40:52] at that frequency
[00:40:54 - 00:40:56] and then a cosine
[00:40:57 - 00:41:00] so the output is still at frequency f1
[00:41:02 - 00:41:04] we have the phase shift of our input
[00:41:05 - 00:41:07] and then we have some phase
[00:41:08 - 00:41:12] introduced by our filter at that frequency
[00:41:14 - 00:41:14] f1
[00:41:14 - 00:41:16] and that's what we call theta
[00:41:19 - 00:41:21] okay so two key things here are
[00:41:21 - 00:41:22] so we're going to ask the
[00:41:23 - 00:41:24] signal input to our filter
[00:41:25 - 00:41:27] the frequency output
[00:41:27 - 00:41:30] is the same as the frequency at the input
[00:41:32 - 00:41:34] then the magnitude of the output
[00:41:36 - 00:41:40] is multiplied by the magnitude of our frequency response of the filter
[00:41:41 - 00:41:45] and then the phase shift of our input cosine
[00:41:46 - 00:41:53] is then shifted by the phase angle of
[00:41:54 - 00:41:56] our frequency response of the filter
[00:41:57 - 00:42:00] so just let
[00:42:00 - 00:42:04] the writing catch down and then we'll illustrate this as the diagram
[00:42:04 - 00:42:06] because that makes it easier to see
[00:42:16 - 00:42:19] okay so let's now consider our RC circuit
[00:42:20 - 00:42:20] again
[00:42:22 - 00:42:24] this is the last example with our RC circuit
[00:42:25 - 00:42:30] so again we've got our is a 100 kilohertz
[00:42:33 - 00:42:36] C is 10 microfarads
[00:42:37 - 00:42:39] RC is one
[00:42:42 - 00:42:49] now the top here we've got frequency of 0.1 Hertz
[00:42:52 - 00:42:56] and at the bottom here we've got a frequency of
[00:42:57 - 00:43:08] one that's okay so in each case blue is the
[00:43:10 - 00:43:17] input voltage and that has amplitude of one volt
[00:43:24 - 00:43:26] is the filter
[00:43:37 - 00:43:40] okay so let's look at the magnitude's first
[00:43:45 - 00:43:47] so we're going to go back to our boat plot
[00:43:47 - 00:43:49] so the two frequencies we're looking at are
[00:43:50 - 00:43:51] this is a different color
[00:43:55 - 00:43:58] orange is the graph's orange okay so 0.1
[00:44:00 - 00:44:03] so at this point here this is about
[00:44:05 - 00:44:11] minus 1 dB at 0.1 Hertz
[00:44:12 - 00:44:18] and then the other one we're interested was 1 Hertz which is 10 to the 0
[00:44:20 - 00:44:22] so this is about minus
[00:44:23 - 00:44:28] let's call that 17 dB at 1 Hertz
[00:44:30 - 00:44:35] okay so it's reading off the magnitude of our boat plot
[00:44:36 - 00:44:40] so it's not minus 1 dB and then minus 17 dB
[00:45:00 - 00:45:03] okay so the top one we had
[00:45:08 - 00:45:09] minus 1 dB
[00:45:11 - 00:45:17] for the amplitude and so that gives then if we convert from
[00:45:19 - 00:45:25] decibels to an absolute value we have then this is about
[00:45:26 - 00:45:33] 0.9 in magnitude and then from
[00:45:34 - 00:45:38] frequency 1 Hertz we had minus 17 dB
[00:45:39 - 00:45:45] and this gives us about 0.14 in magnitude
[00:45:49 - 00:45:53] okay so that rings true from these time domain plots
[00:45:53 - 00:45:56] the orange curve of the output is about 0.9 of the input
[00:45:57 - 00:46:04] and the higher frequency we attenuate more
[00:46:05 - 00:46:09] and so we're left with about 0.14 as our output compared to the input
[00:46:11 - 00:46:12] so that's showing the low pass filter in action
[00:46:14 - 00:46:17] the low frequency with the lower frequency here 0.1 Hertz
[00:46:18 - 00:46:23] is being attenuated a little bit not much but then the higher frequency
[00:46:23 - 00:46:25] is being attenuated a lot
[00:46:28 - 00:46:35] okay so that's half the story the other half the story is then our phase
[00:46:38 - 00:46:44] we have each case we're going to have a phase shift
[00:46:44 - 00:46:48] who wants to get sort the phase shift for the bottom case the 1 Hertz is going to be
[00:46:49 - 00:46:56] how much our phase is the orange curve compared to the green
[00:46:56 - 00:47:04] to the blue curve 40 I'll put more than that so is it a peak here
[00:47:06 - 00:47:10] is about almost where this one is getting down to 0
[00:47:12 - 00:47:18] so that means if we're perfectly at 0 there will be 90 degrees so this is about 80 degrees
[00:47:19 - 00:47:27] and the top one the orange curve is a little bit to the right of the blue curve that's about
[00:47:29 - 00:47:34] 30 degrees we'll go back and check that on our
[00:47:38 - 00:47:42] bode plot so I'll just write the summary here and then we'll go back
[00:47:43 - 00:47:53] so the higher frequency has larger attenuation and larger phase shift
[00:47:53 - 00:48:18] okay so we'll just go back to our bode plot so we're looking now at the phase plot on the right
[00:48:18 - 00:48:25] so we were looking at 10 to the minus 1 here and 10 to the 0 so this is about
[00:48:27 - 00:48:39] minus 80 degrees at 1 Hertz and this is about minus 30 degrees at 0.1 Hertz
[00:48:53 - 00:48:58] okay so I'll just go back to finish on the bode plot
[00:48:59 - 00:49:11] I'll just correct myself these one minus those phase angles were both minus when I look at
[00:49:11 - 00:49:26] the bode plot again minus 30 degrees minus 80 degrees
[00:49:27 - 00:49:33] okay so that brings the example with the RC filter so finish today and then tomorrow we'll
[00:49:33 - 00:49:37] look at some other different types of filters high pass filters second order filters
[00:49:37 - 00:49:44] etcetera and then next we'll get on to digital filters and I'll see you hopefully back in engineering
[00:49:44 - 00:50:27] and about two months bring your questions
[00:51:11 - 00:51:21] all right yeah

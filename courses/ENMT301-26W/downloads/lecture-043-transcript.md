# ENMT301-26W Lecture 43 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_43_audio_16k_mono_32k.mp3`
Source audio SHA-256: `7a001e374edcc9684a6899e10a670c4eb3c22bed7247ff8efdfc69ee05ef5759`
Generated: 2026-06-06T06:39:38.732353+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:00 - 00:00:04] Okay, good afternoon everyone.
[00:00:04 - 00:00:09] Okay, so just a quick reminder of what we did last week and then we'll carry on.
[00:00:09 - 00:00:15] So last week we're looking at different types of signals, the analog signals, digital signals,
[00:00:15 - 00:00:19] and we looked at different types of noise that occur in our circuits.
[00:00:19 - 00:00:24] And so then the noise is kind of like a random disturbance in our circuit,
[00:00:24 - 00:00:33] and we started looking at interference, which is a more deterministic disturbance in our circuit.
[00:00:33 - 00:00:39] So that's something that we could write an equation for, it is somewhat predictable.
[00:00:39 - 00:00:45] So there are three different types of coupling and we talk about an aggressive circuit,
[00:00:45 - 00:00:49] which is then producing interference into our circuit of interest.
[00:00:49 - 00:00:54] So these figures, the circuit of interest is a sensor with an amplifier,
[00:00:54 - 00:00:59] and there's some sort of aggressive circuit, which is shown in dotted lines.
[00:00:59 - 00:01:03] And so you can think of that as being the main voltage in the wall,
[00:01:03 - 00:01:08] which has been causing some sort of interference.
[00:01:08 - 00:01:14] So conductive coupling occurs when we have what we think are two different circuits,
[00:01:14 - 00:01:20] and sharing a common ground, for example, or a common power rail.
[00:01:20 - 00:01:26] And then there is some sort of shared resistance between the two circuits,
[00:01:26 - 00:01:34] and we have an interference voltage, which is determined simply by Ohm's Law.
[00:01:34 - 00:01:39] So that was the first one we looked at, and then the one we finished with on Friday
[00:01:39 - 00:01:48] was capacitive coupling, whereby a capacitance is formed between any two conductors.
[00:01:48 - 00:01:56] We're all conductors, so we can generate a parasitic capacitance between us and say,
[00:01:56 - 00:02:03] the wires in the wall, or there's a parasitic capacitance between two different circuits,
[00:02:03 - 00:02:05] as shown in this figure here.
[00:02:05 - 00:02:16] Okay, and then the parasitic coupling is determined by the change in voltage with respect to time,
[00:02:16 - 00:02:26] as well as the size of our parasitic capacitance, and also the series voltage in our circuit.
[00:02:26 - 00:02:32] Okay, we're going through an example on Friday,
[00:02:32 - 00:02:38] where we were considering the capacitive coupling of a human.
[00:02:38 - 00:02:46] And so we're generating a small capacitance, parasitic capacitance, between us and say,
[00:02:46 - 00:02:52] the wire on the ceiling, and then a much louder jerk capacitance between us and ground.
[00:02:52 - 00:03:00] Okay, so we're going through and just calculating the voltages, what the voltage on the human body,
[00:03:00 - 00:03:08] in this example, and it ends up being about two volts.
[00:03:08 - 00:03:13] So we have this sort of voltage divided here, and then we need to add,
[00:03:13 - 00:03:23] oh, there's a denominator here, the two capacitances, so that's then 303 times 10 to the minus 12 Farads.
[00:03:23 - 00:03:31] We multiply by our main voltage in our voltage divider, and then we're getting a voltage of,
[00:03:31 - 00:03:37] in this case, about 2.4 volts across the body.
[00:03:37 - 00:03:50] Okay, and so then this is a problem for biomedical sensors.
[00:03:50 - 00:04:01] So if you think about EEG, which is measuring the voltage waves in the brain,
[00:04:01 - 00:04:07] or the ECG, which is measuring the voltage waves in the heart,
[00:04:07 - 00:04:21] this interference is going to greatly affect our measurements.
[00:04:21 - 00:04:27] Okay, so their way is dealing with this, with filtering, with shielding of the wires,
[00:04:27 - 00:04:31] that we reduce capacitances, et cetera.
[00:04:31 - 00:04:38] Okay, so that was the second of our two inferences, and then that leaves the last one,
[00:04:38 - 00:04:45] can be known, guess what the last one is, what's the other circuit element we haven't considered yet?
[00:04:45 - 00:04:47] Inductive, good.
[00:04:47 - 00:04:54] Okay, so we're going to do inductive coupling, and so this arises from Faraday's Lawer,
[00:04:54 - 00:05:00] which you would have hopefully done in phase 101.
[00:05:00 - 00:05:07] This is where if we have a change in current in our circuit,
[00:05:07 - 00:05:18] so we then have a magnetic flux, and this then produces a voltage in a nearby circuit.
[00:05:18 - 00:05:23] Okay, so if we have, again, here we have our two circuits,
[00:05:23 - 00:05:31] so in solid, this is our sensor circuit, this is our victim circuit,
[00:05:31 - 00:05:36] and we have some sort of voltage supply hooked up to something,
[00:05:36 - 00:05:41] let's say there's a motor, and this, the double lines, is our aggressive circuit.
[00:05:41 - 00:05:52] Okay, so we're going to generate then a voltage in our sensor circuit,
[00:05:52 - 00:05:59] based on the change in current in our aggressive circuit.
[00:05:59 - 00:06:07] Okay, so the equation for this then is our interference voltage V i of t,
[00:06:07 - 00:06:15] so i there for interference is given by M, which is our mutual inductance,
[00:06:15 - 00:06:25] between the two circuits, and then the rate of change of our aggressive current,
[00:06:25 - 00:06:29] the I of t by dt.
[00:06:29 - 00:06:35] As the mutual inductance here is in Henry's.
[00:06:35 - 00:06:39] So this equation is very similar to what you would have seen.
[00:06:39 - 00:06:47] Previously, the voltage across inductor is L di by dt.
[00:06:47 - 00:06:50] Okay, so this inductive coupling is then more,
[00:06:50 - 00:06:52] more than goes to transformer.
[00:06:52 - 00:07:00] So this thing here is a transformer, which is in effect coupling of two circuits together,
[00:07:00 - 00:07:07] and inducing this EMF voltage into our victim circuit,
[00:07:07 - 00:07:09] which is here at our sensor circuit.
[00:07:09 - 00:07:15] Okay, so it's a parasitic transformer.
[00:07:15 - 00:07:21] It's not a real transformer, it is just acting as a transformer.
[00:07:21 - 00:07:26] Okay, so what's one way we can reduce this inductive coupling?
[00:07:26 - 00:07:35] Yeah, we're just moving the circuits for the apart.
[00:07:35 - 00:07:39] We'll reduce then the mutual inductance.
[00:07:39 - 00:07:42] Okay, so that's an easy way of doing it.
[00:07:42 - 00:07:47] And there are a lot more complicated ways, which you'll have seen before,
[00:07:47 - 00:07:50] but you might not have seen why it's done before.
[00:07:50 - 00:07:56] But if you open up cable, you might have done this in your electrical workshop.
[00:07:56 - 00:07:59] Last year, funny locks.
[00:07:59 - 00:08:04] But you might have seen inside the wires, they're all kind of twisted together.
[00:08:04 - 00:08:08] So this is known as twisted peers.
[00:08:08 - 00:08:15] So with Faraday's law, if we can reduce the size of these loops,
[00:08:15 - 00:08:22] then we can reduce the EMF voltage that's produced inside the circuit.
[00:08:22 - 00:08:28] So by twisting the peers together, we can reduce that mutual inductance.
[00:08:28 - 00:08:40] Okay, so that's why we could often see our signal carrying wires in twisted peers.
[00:08:40 - 00:08:47] So they reduce this effective loop area, reducing this mutual inductance M.
[00:08:47 - 00:08:57] And also the alternating twists will reduce the, or cancel the electromagnet before voltage.
[00:08:57 - 00:09:00] Okay, so we've got here.
[00:09:00 - 00:09:03] So this is the twisted peer.
[00:09:03 - 00:09:06] So these are different types of cable.
[00:09:06 - 00:09:19] So we've twisted peer here to reduce inductive coupling.
[00:09:19 - 00:09:26] And as we saw before, we often have these shields.
[00:09:26 - 00:09:31] And that can reduce capacitive coupling.
[00:09:31 - 00:09:40] Okay, the shields can stop electric fields.
[00:09:40 - 00:09:43] So that reduces the capacitive coupling.
[00:09:43 - 00:09:49] But the shields can't stop magnetic field lines,
[00:09:49 - 00:09:53] so the shields don't cancel the inductive coupling.
[00:09:53 - 00:09:56] So I'll be right there down as well.
[00:09:56 - 00:10:40] Okay, so that is the last slide on the first week's wet material on signals,
[00:10:40 - 00:10:42] noise and interference.
[00:10:42 - 00:10:46] So we'll just close that, keep.
[00:10:46 - 00:10:48] And then the next thing we're going to be doing.
[00:10:48 - 00:10:54] So this week we're going to be looking at our signals in frequency space.
[00:10:54 - 00:11:00] So we're going to look at Laplace transforms and Fourier transforms
[00:11:00 - 00:11:04] that you will have done before in your math courses.
[00:11:04 - 00:11:11] This is going to be a bit more oriented towards signal processing rather than maths.
[00:11:11 - 00:11:31] Okay, so right there in French today,
[00:11:31 - 00:11:34] because Laplace was a French man,
[00:11:34 - 00:11:36] and he was one of these guys.
[00:11:36 - 00:11:41] People in about the 18th century who had some many different things.
[00:11:41 - 00:11:48] So his contributions, not just an engineering, but in physics, astronomy, statistics.
[00:11:48 - 00:11:54] And he was also a minister and Napoleon's government for about a month.
[00:11:54 - 00:11:57] But while he was an awesome scientist in engineer,
[00:11:57 - 00:11:59] he made a terrible administrator.
[00:11:59 - 00:12:02] Apparently he took forever to make any decisions,
[00:12:02 - 00:12:05] so he got sacked from that job pretty quickly.
[00:12:05 - 00:12:13] So you will understand that he's done Laplace transforms in E-MES two ten last year,
[00:12:13 - 00:12:17] and also E-MES 303.
[00:12:17 - 00:12:28] And so we used to do circuit analysis with Laplace transforms in E-MES M-T two one one with Louis.
[00:12:28 - 00:12:30] But Louis, if that out last year,
[00:12:30 - 00:12:35] so I'm going to do a bit of a recap of stuff that you missed out that other people used to get.
[00:12:35 - 00:12:45] So just how we can rewrite our circuit equations in terms of in Laplace space rather than in the time domain.
[00:12:45 - 00:12:50] Because this is useful when we start doing analog filters.
[00:12:50 - 00:12:55] So the filter is to remove certain frequency components of our signals.
[00:12:55 - 00:13:02] And Laplace transforms are also really useful for analyzing transients.
[00:13:02 - 00:13:15] So when we flick the switch in this circuit, something's going to happen straight away.
[00:13:15 - 00:13:17] And it's the transient response.
[00:13:17 - 00:13:20] And then it's going to reach some sort of steady state.
[00:13:20 - 00:13:36] So looking at systems in Laplace domain is much easier than in the time domain for analyzing the transient response.
[00:13:36 - 00:13:39] OK, so we'll go through this quickly.
[00:13:39 - 00:13:50] So first of all, the whole point of Laplace transform is that we can transform from messy differential and integral equations
[00:13:50 - 00:13:53] to an algebraic equation, which is then easy to solve.
[00:13:53 - 00:14:00] And then we can go back with the inverse Laplace transform to our time domain signal.
[00:14:00 - 00:14:04] OK, so we've got the in the definition of Laplace transform.
[00:14:04 - 00:14:10] So our signal and Laplace domain, we use the capital.
[00:14:10 - 00:14:16] So capital F of our plus variable S is equal to,
[00:14:16 - 00:14:25] so we use this kind of calligraphic L for the Laplace transform operator.
[00:14:25 - 00:14:29] Squirky brackets and we take the Laplace transform of our time domain signal,
[00:14:29 - 00:14:31] little F of t.
[00:14:32 - 00:14:44] And that is then the integral from 0 to infinity of F of t, e to the minus S t dt.
[00:14:44 - 00:14:49] So this is a one-sided integral between 0 and infinity.
[00:14:49 - 00:14:52] OK, so lower case for the time domain,
[00:14:52 - 00:14:56] uppercase for our Laplace domain.
[00:14:56 - 00:15:01] And we'll use the same notation with our Fourier transform as well,
[00:15:01 - 00:15:04] starting from tomorrow probably.
[00:15:04 - 00:15:12] OK, so we can use the Laplace transform for any signal that can be expressed as a sum of exponential.
[00:15:12 - 00:15:20] And so because of the Fourier series, which we'll talk about tomorrow or Friday,
[00:15:20 - 00:15:22] what you've done in our students.
[00:15:22 - 00:15:27] Well, we can write a square wave or a triangular wave as a sum of exponential.
[00:15:27 - 00:15:29] So sum of signs and cosines.
[00:15:29 - 00:15:38] So essentially all signals, we can almost all signals we can write as some of complex
[00:15:38 - 00:15:48] exponential, which means we can use the Laplace transform on them.
[00:15:48 - 00:15:52] OK, so in the Laplace domain, we've got this S variable.
[00:15:52 - 00:15:55] And so S has a real and imaginary component.
[00:15:55 - 00:16:02] So S is equal to sigma plus j omega.
[00:16:02 - 00:16:07] OK, so omega is the angular frequency.
[00:16:07 - 00:16:20] And omega is related to the frequency and hurt by 2 pi.
[00:16:20 - 00:16:26] And so the frequency then is the number of cycles per second.
[00:16:26 - 00:16:36] So if we have a sine wave here, period t, our frequency is one over the period,
[00:16:36 - 00:16:43] capital T. OK, so this is easy part.
[00:16:43 - 00:16:53] And then the sigma indicates how the amplitude of the signal varies with time.
[00:16:53 - 00:17:03] OK, so our oscillations from our signs and cosines, sigma gives us the envelope of those amplitude changes.
[00:17:03 - 00:17:06] You got a question?
[00:17:06 - 00:17:09] OK.
[00:17:09 - 00:17:14] OK, so that's how our S variable is defined.
[00:17:14 - 00:17:28] OK, and so then if we have our sigma value is greater than zero.
[00:17:28 - 00:17:32] So in this diagram here, the cross represents the poles.
[00:17:32 - 00:17:36] And you would have done this presumably in 303.
[00:17:36 - 00:17:44] If our sigma value is greater than zero, then our system is unstable.
[00:17:44 - 00:17:48] So our signal here is increasing without bound.
[00:17:48 - 00:17:55] OK, as an example here, we have our voltage in our circuit just increasing without bound.
[00:17:55 - 00:17:56] That's unstable.
[00:17:56 - 00:17:58] Something's going to go horribly wrong.
[00:17:58 - 00:18:06] OK, so in this diagram here, on the x-axis we have sigma.
[00:18:06 - 00:18:07] So this is the real part.
[00:18:07 - 00:18:14] And we have the imaginary part on the y-axis, which is omega.
[00:18:14 - 00:18:23] OK, so on the other side in the left half plane, if sigma is less than zero, it is stable.
[00:18:23 - 00:18:27] And our voltage is decreasing.
[00:18:27 - 00:18:33] OK, so the voltage shown here is going down with time.
[00:18:33 - 00:18:39] So that makes it stable.
[00:18:39 - 00:18:41] OK, so far so familiar?
[00:18:41 - 00:18:53] OK, so there's a reflection between the transient response and the steady state.
[00:18:53 - 00:18:57] The transient response is when things are changing.
[00:18:57 - 00:19:09] So when you close, say, your switch in your circuit and you get the immediate response,
[00:19:09 - 00:19:12] which is changing, that's the transient.
[00:19:12 - 00:19:20] And then after a period in time, to determine by the time constants of your circuit components,
[00:19:20 - 00:19:25] then you're going to be in steady state.
[00:19:25 - 00:19:30] OK, so this is converging to hear a value of about one.
[00:19:30 - 00:19:37] So we get some oscillations at the start when we have a response to something.
[00:19:37 - 00:19:46] And then our equilibrium or steady state is then once it's decayed to something repeatable.
[00:19:46 - 00:19:48] The transient is a data way.
[00:19:48 - 00:19:58] OK, so we're going to have a bit about notation now.
[00:19:58 - 00:20:05] How we can write signals for n Laplace domain.
[00:20:05 - 00:20:13] So we can describe our signal f of t as a complex exponential.
[00:20:13 - 00:20:16] So we've got e to the s t.
[00:20:16 - 00:20:34] OK, and then if we expand out where s is equal to sigma plus j omega,
[00:20:34 - 00:20:57] this can be written then as equal to e to the sigma plus j omega times t.
[00:20:57 - 00:21:07] OK, then we can rewrite that as then e to the sigma t times e to the j omega t.
[00:21:07 - 00:21:20] And then this is equal to e to the sigma t.
[00:21:20 - 00:21:26] And then using Euler's rules on complex exponentials,
[00:21:26 - 00:21:35] e to the j omega t can be written as cosine omega t plus j sine omega t.
[00:21:35 - 00:21:43] OK, so this is a real exponential.
[00:21:43 - 00:21:45] Sigma is a real number.
[00:21:45 - 00:21:49] And then we have some sort of cosine part here.
[00:21:49 - 00:21:53] And this has come from using Euler.
[00:21:53 - 00:22:04] OK, so we typically represent our signal just with the real part.
[00:22:04 - 00:22:13] So if we have the real part of e to the s t,
[00:22:13 - 00:22:17] we'll just take the real part of the equation of f of t here.
[00:22:17 - 00:22:32] We then have e to the sigma t times cosine omega t.
[00:22:32 - 00:22:35] OK, so we have then, maybe there's a record.
[00:22:35 - 00:22:45] It's cosine omega t cosine omega t j sine omega t.
[00:22:45 - 00:22:49] So if we want to write a real-world signal starting at t is zero.
[00:22:49 - 00:22:56] So we'll need to make use of the unit step function.
[00:22:56 - 00:23:04] We'll have then our function f of t is equal to u of t times
[00:23:04 - 00:23:10] the real part of some amplitude a times our complex exponential
[00:23:10 - 00:23:18] e to the s t. And so we can expand that out by just taking the real part here.
[00:23:18 - 00:23:23] So our signal f of t, we can rewrite as,
[00:23:23 - 00:23:27] so remember u of t here is the unit step,
[00:23:27 - 00:23:29] u for unit.
[00:23:29 - 00:23:32] So that takes care of that starting at t is zero.
[00:23:32 - 00:23:39] So we've got, if it's t is u of t times the magnitude a.
[00:23:39 - 00:23:43] We've got this complex exponential e to the sigma t.
[00:23:43 - 00:23:50] And then we've got cosine of omega t plus some phase angle
[00:23:50 - 00:24:03] phi of phase shift.
[00:24:03 - 00:24:04] OK, I'll just let you catch up with the writing.
[00:24:04 - 00:24:09] And then we'll do a couple of examples on the next two slides.
[00:24:09 - 00:24:12] And so the idea, I did see I'll just write the top as well.
[00:24:12 - 00:24:22] e to the j x is equal to cos x plus j sine x.
[00:24:22 - 00:24:51] OK, half way through a lecture.
[00:24:51 - 00:24:53] Probably the last thing of today.
[00:24:53 - 00:24:54] Hopefully, yeah.
[00:24:54 - 00:24:55] Good.
[00:24:55 - 00:24:58] OK, so, OK.
[00:24:58 - 00:25:03] Let's look up some examples just for this notation of how we can write down our
[00:25:03 - 00:25:04] signals.
[00:25:04 - 00:25:09] So here we've got a current signal, it's starting when time t is zero
[00:25:09 - 00:25:11] to an amplitude of 5 amps.
[00:25:11 - 00:25:27] OK, so we're going to write i of t is equal to.
[00:25:27 - 00:25:30] So starting at zero is what does that mean?
[00:25:30 - 00:25:41] We need, we'll have the unit step u of t.
[00:25:41 - 00:25:45] So that takes into account our signal starts at time zero.
[00:25:45 - 00:25:48] You understand?
[00:25:48 - 00:25:58] So what's our amplitude a here equal to 5 good?
[00:25:58 - 00:26:02] OK, what is our value of sigma here equal to?
[00:26:02 - 00:26:07] The follow up question.
[00:26:07 - 00:26:08] Oh, zero good.
[00:26:08 - 00:26:14] OK, so it's neither increasing nor the
[00:26:14 - 00:26:15] decreasing.
[00:26:15 - 00:26:20] So if we go back to this equation here, sigma is equal to zero.
[00:26:20 - 00:26:35] Then it's OK, but sigma is zero.
[00:26:35 - 00:26:37] What's our frequency of our signal here?
[00:26:37 - 00:26:46] Well, you can do a little bit of counting.
[00:26:46 - 00:26:52] OK, so we've got 1, 2, 3, 4, 5, 6, 7, 8, 9, 10.
[00:26:52 - 00:26:55] Cycles in a millisecond.
[00:26:55 - 00:26:59] What does that give us?
[00:26:59 - 00:27:03] 10 divided by 1.
[00:27:03 - 00:27:08] And then inverse that we get 10 kilohertz.
[00:27:08 - 00:27:17] So if this were in seconds, we'd have 10.
[00:27:17 - 00:27:20] And 1 second would give us frequency of 10 hertz.
[00:27:20 - 00:27:22] But because it's a milliseconds, rather than seconds,
[00:27:22 - 00:27:25] it becomes 10 kilohertz.
[00:27:25 - 00:27:31] OK, so then we need our angular frequency from the equation here
[00:27:31 - 00:27:32] before.
[00:27:32 - 00:27:37] So omega is 2 pi f.
[00:27:37 - 00:27:49] So then omega is then 20,000 pi radians per second.
[00:27:49 - 00:27:51] OK, so in terms of writing our current IAT,
[00:27:51 - 00:27:57] we have the unit step times the real part of our amplitude 5
[00:27:57 - 00:28:11] times e to the j 20,000 pi t.
[00:28:11 - 00:28:15] And we can also write this by taking the real part of the
[00:28:15 - 00:28:16] exponential becomes cosine.
[00:28:16 - 00:28:19] So we have IFT is equal to unit step.
[00:28:19 - 00:28:20] That makes us start.
[00:28:20 - 00:28:21] It's 0.
[00:28:21 - 00:28:23] We've got an amplitude of 5.
[00:28:23 - 00:28:29] And we've got cosine 20,000 pi t.
[00:28:29 - 00:28:31] And that is in amps.
[00:28:31 - 00:28:47] OK, another example, just slightly different.
[00:28:47 - 00:28:52] Because now we've got a decaying signal.
[00:28:52 - 00:28:57] So we've got here with togots, got a sigma of minus 20.
[00:28:57 - 00:29:00] So let's stable.
[00:29:00 - 00:29:05] And at time tears four other signal starting,
[00:29:05 - 00:29:09] the frequency of our exponential there is a kilohertz.
[00:29:09 - 00:29:12] And we need to define this signal.
[00:29:12 - 00:29:17] So we'll start off with our Laplace variable here.
[00:29:17 - 00:29:22] s is equal to sigma plus j omega.
[00:29:22 - 00:29:35] So s is then sigma, which is minus 20 plus j times omega,
[00:29:35 - 00:29:38] which is 2 pi times 1,000.
[00:29:38 - 00:29:43] So it becomes 2,000 pi.
[00:29:43 - 00:29:49] In fact, as this is a voltage, so V of t, our voltage,
[00:29:49 - 00:29:54] is equal, how do we deal with our signal starting at t is 4?
[00:29:54 - 00:29:58] Good.
[00:29:58 - 00:30:00] So we've got u of t minus 4.
[00:30:00 - 00:30:05] That means it starts here.
[00:30:05 - 00:30:12] Then we've got two lines, because it's going to get too much for me.
[00:30:12 - 00:30:17] So then we've got the real part of our amplitude,
[00:30:17 - 00:30:19] what's our initial amplitude here.
[00:30:19 - 00:30:30] So we have a real part of 10.
[00:30:30 - 00:30:42] And then we've got our exponential part, which is e to the minus 20
[00:30:42 - 00:30:48] plus j 2,000 pi.
[00:30:48 - 00:30:51] And then this is also t minus 4.
[00:30:51 - 00:31:07] So if we write it in terms of cosines, V of t is equal to u of t minus 4,
[00:31:07 - 00:31:24] times 10 times e to the minus 20 t minus 4 times cosine of 20,000,
[00:31:24 - 00:31:37] sorry, 2,000 pi t minus 4.
[00:31:37 - 00:31:38] OK.
[00:31:38 - 00:31:39] So describe that signal.
[00:31:39 - 00:31:42] We've got it starts at 4.
[00:31:42 - 00:31:45] So we've got this unit step shifted by 4.
[00:31:45 - 00:31:48] We've got the caying amplitude.
[00:31:48 - 00:31:52] So that's covered by this exponential.
[00:31:52 - 00:32:03] And we've got this cosine wave, which is covered by the cos term.
[00:32:03 - 00:32:04] OK.
[00:32:04 - 00:32:06] So let's do a little bit of circuit theory.
[00:32:06 - 00:32:14] So this is the circuit we had on the title slide.
[00:32:14 - 00:32:21] And so what we're going to do here is to find the current through the circuit
[00:32:21 - 00:32:31] and when the switch closes t and 0.
[00:32:31 - 00:32:32] OK.
[00:32:32 - 00:32:35] So this is mostly a signal processing course that I teach,
[00:32:35 - 00:32:38] but we need to know a little bit about our circuits,
[00:32:38 - 00:32:42] because we're considering signal and circuits and noise and circuits as well.
[00:32:42 - 00:32:44] How's your natural memory?
[00:32:44 - 00:32:50] Some stuff from 270 and 211 last year.
[00:32:50 - 00:32:51] OK.
[00:32:51 - 00:32:54] So if we want to find the current in the circuit,
[00:32:54 - 00:33:04] what's a good way to do that?
[00:33:04 - 00:33:05] Well, a lot of ways to do it.
[00:33:05 - 00:33:10] I'm going to do our old friend Kirchhoff's voltage law.
[00:33:10 - 00:33:13] You know what I mean?
[00:33:13 - 00:33:21] What Kirchhoff's voltage law is the sum of the voltages around the loop equals...
[00:33:21 - 00:33:22] OK.
[00:33:22 - 00:33:26] So we've got a positive voltage here, the voltage source,
[00:33:26 - 00:33:31] and then we're going to drop some voltage across the resistor and across the inductor.
[00:33:31 - 00:33:34] OK.
[00:33:34 - 00:33:39] So we have a plus Vt from a voltage source.
[00:33:39 - 00:33:44] Then we're going to voltage drop across the resistor, which is a good by ohm's law,
[00:33:44 - 00:33:48] minus IT of R.
[00:33:48 - 00:33:52] And then the voltage drop across the inductor,
[00:33:52 - 00:33:56] which I referred to when we did inductive coupling of our circuit,
[00:33:56 - 00:33:57] start today.
[00:33:57 - 00:34:04] It's given by L, DI, differential time, with respect to time T.
[00:34:04 - 00:34:06] And because we're doing Kirchhoff's voltage law,
[00:34:06 - 00:34:08] that is the sum to zero.
[00:34:08 - 00:34:10] OK.
[00:34:10 - 00:34:14] So I'm putting equations in the form machine.
[00:34:14 - 00:34:21] As I go writing these lectures, so V equals L di by Dt is one of the ones that we're...
[00:34:21 - 00:34:25] OK.
[00:34:25 - 00:34:47] So if we rearrange this a little bit, we get V of T is equal to I of T times R plus L di as a function of T by Dt.
[00:34:47 - 00:34:49] OK.
[00:34:49 - 00:34:52] We're going to go to a competition here that before T is zero,
[00:34:52 - 00:34:56] and our voltage is going to be equal to zero.
[00:34:56 - 00:35:02] And after which our voltage source has a constant amplitude of V naught.
[00:35:02 - 00:35:04] So we're two different cases.
[00:35:04 - 00:35:16] And then for T is less than zero and for T greater than equal to zero.
[00:35:16 - 00:35:17] OK.
[00:35:17 - 00:35:26] Now our equation is I of T times R plus L di of T by Dt.
[00:35:26 - 00:35:30] So we've got this here differential equation.
[00:35:30 - 00:35:43] We need to integrate both sides of integration.
[00:35:43 - 00:35:54] And it's all a great big mess.
[00:35:54 - 00:35:56] So fun to do.
[00:35:56 - 00:35:57] And so it's a bit away.
[00:35:57 - 00:36:00] And surprisingly enough, that's with Laplace transforms.
[00:36:00 - 00:36:02] OK.
[00:36:02 - 00:36:10] So it's easier to analyze this circuit in the Laplace domain than it is in the time domain.
[00:36:10 - 00:36:20] Because we can make use of some of the tricks of all the classrooms from to replace the derivative with respect to time with an algebraic quantity and instead.
[00:36:20 - 00:36:31] So we'll come back to this at the end of the settle exercise where we analyze the same circuit in Laplace domain.
[00:36:31 - 00:36:38] First we need to do a couple other things with our definitions of Laplace transforms.
[00:36:38 - 00:36:42] So I gave you the definition of four of Laplace transform before.
[00:36:42 - 00:36:52] So Laplace inverse Laplace transform is then we're going back to our signal if of T.
[00:36:52 - 00:36:58] And so this is this sort of calligraphic L operator minus one for the inverse.
[00:36:58 - 00:37:05] And we're operating then on our Laplace signal in the yesterday name.
[00:37:05 - 00:37:14] And so we can write this as one over two pi J.
[00:37:14 - 00:37:30] The integral from C minus J infinity to C plus J infinity of capital F of S E to the S T D S.
[00:37:30 - 00:37:39] Because the exponential here is positive whereas with the forward operator it was a negative.
[00:37:39 - 00:37:52] Okay. So this is the formal definition of the Laplace transform where we've got some constant C on our integral.
[00:37:52 - 00:38:09] If we don't have any singularities within if this then it'll be equal to zero.
[00:38:09 - 00:38:18] But in practice we're not going to be doing these Laplace integrals.
[00:38:18 - 00:38:27] We're going to use some lookup tables for common expressions and then do our inverse Laplace transform with these tables.
[00:38:27 - 00:38:41] Okay. So I'll show you what I think are the main properties about T n of them.
[00:38:41 - 00:38:46] And so this is the table that I've put in my draft form the sheet.
[00:38:46 - 00:38:51] I'll learn so you don't have to memorize these.
[00:38:51 - 00:38:59] But we'll go through these. So they're all defined for T is greater than zero.
[00:38:59 - 00:39:09] So our signal is defined as defined starting with T is equal to zero from the original Laplace for a transform integral.
[00:39:09 - 00:39:23] Right up here, formula sheet given in the test.
[00:39:23 - 00:39:43] Okay. So the first one is constant. So this is like if we have a DC battery in our circuit then that's how we would transform that to the Laplace domain.
[00:39:43 - 00:39:50] So if it's a 12 volt battery K is 12 and then our battery in the Laplace domain will be 12 divided by S.
[00:39:50 - 00:40:01] Okay. So the other ones that will pop up during this lecture.
[00:40:01 - 00:40:07] So decaying exponential, this is if we have a transfer function with a single pole.
[00:40:07 - 00:40:30] So we have a pole at S is minus A. So a single pole in our Laplace domain and then we will have a decaying exponential in the time domain.
[00:40:30 - 00:40:36] Okay. So this one here, step response, first order.
[00:40:36 - 00:40:47] So we've got two poles here, one at zero and then one at minus one over tau.
[00:40:47 - 00:40:57] Okay. And then this gives us a decaying exponential in the time domain.
[00:40:57 - 00:41:01] Sorry. One minus a decaying exponential in the time domain.
[00:41:01 - 00:41:10] And this represents, for example, an RC or RL.
[00:41:10 - 00:41:16] Okay. So they can be used to describe a capacitor charging up in an RC circuit.
[00:41:16 - 00:41:36] And then it's a next two scaling and superposition define the concept of linearity.
[00:41:36 - 00:41:47] So we increase our signal if of t by some constant K, then we increase our frequency domain if it is by the same factor of K.
[00:41:47 - 00:41:50] If it's linear, then superposition also applies.
[00:41:50 - 00:42:05] So if we take the Laplace transform of the sum of different signals, this is equal to the sum of the Laplace transforms.
[00:42:05 - 00:42:09] Okay. And then the two key ones why we would use Laplace transform.
[00:42:09 - 00:42:16] So differentiation, we convert the but it t to multiplying by s here.
[00:42:16 - 00:42:22] So we're going from a differential to an algebraic multiplication.
[00:42:22 - 00:42:26] And this little f of zero is our initial condition.
[00:42:26 - 00:42:39] And similarly for doing integration in the time domain, we have an integral.
[00:42:39 - 00:42:47] And then in the frequency of Laplace domain, we have this, this is a vests divided by the Laplace variable x.
[00:42:47 - 00:42:53] So we can get rid of our derivatives and integrals and replace them with algebraic quantities.
[00:42:53 - 00:43:12] Okay. And this last one is here with a delay of a in the time domain, then becomes a complex, so not a complex, an exponential, even minus a s,
[00:43:12 - 00:43:16] times our spectrum. It's a delay in time domain.
[00:43:16 - 00:43:20] We multiply by an exponential in the frequency domain.
[00:43:20 - 00:43:44] Okay. And the here, u of t is the unit step.
[00:43:44 - 00:43:49] Okay. So the basic idea here is, in the time domain we're going to have some differential equation.
[00:43:49 - 00:43:55] So let's consider here the equation for a in inductor.
[00:43:55 - 00:44:05] So v of t is equal to l di of t by dt.
[00:44:05 - 00:44:12] If we convert that to the last domain, we then have v,
[00:44:12 - 00:44:16] we can just try to use the capital V here in the last domain.
[00:44:16 - 00:44:27] v of s is equal to l s times i of s minus little i of zero.
[00:44:27 - 00:44:32] What's the little i of zero going to be?
[00:44:32 - 00:44:34] Yeah. Backstep.
[00:44:34 - 00:44:38] What is it?
[00:44:38 - 00:44:44] Physically in our circuits.
[00:44:44 - 00:44:48] We're going to go back here to this one. This is the initial condition.
[00:44:48 - 00:44:51] We're subtracting the initial condition of our function.
[00:44:51 - 00:44:56] So then this little i of zero would be the initial current in our circuit.
[00:44:56 - 00:45:04] Which would normally be, for example, in the circuit we were doing the Kirchhoff's voltage law,
[00:45:04 - 00:45:10] the initial current would be zero in there because the switch is open.
[00:45:10 - 00:45:14] Okay. So the big one here is with gone from a differential equation,
[00:45:14 - 00:45:23] which is difficult to solve in time domain to a algebraic equation in the last domain.
[00:45:23 - 00:45:31] And then what we do is we do some algebra, some manipulations.
[00:45:31 - 00:45:35] To get it into a form that we can use the tables.
[00:45:35 - 00:45:59] And then we can do use the inverse class transform to get our solution in the time domain.
[00:45:59 - 00:46:05] So we want to be able to then write when we're in the last domain.
[00:46:05 - 00:46:11] Our solution hopefully is something made up of these functions in the right hand column.
[00:46:11 - 00:46:16] Because these ones we know what their time domain form is.
[00:46:16 - 00:46:33] Okay. So the last thing we'll do today is we will look at our impedances in the last domain.
[00:46:33 - 00:46:43] So that we can analyze circuits in the last domain and we can write our analog filters later on in terms of their loved plus impedances.
[00:46:43 - 00:46:57] So the first of all, for a capacitor our impedance Z is equal to J times our reactive capacitance,
[00:46:57 - 00:47:03] which is then one over J omega C. And this is in homes.
[00:47:03 - 00:47:10] And so for the capacitor if we start with our current,
[00:47:10 - 00:47:15] I of t is equal to C dV of t by dt.
[00:47:15 - 00:47:19] So that's a governing equation for a capacitor.
[00:47:19 - 00:47:22] So change and voltage through the capacitor.
[00:47:22 - 00:47:25] We have a gives the current.
[00:47:25 - 00:47:35] In the last domain, we then have I of s is equal to C, our capacitance.
[00:47:35 - 00:47:47] Then using the definition of the derivative for the last domain, we have s times V of s minus the initial voltage V0.
[00:47:47 - 00:48:11] And so if indeed our initial voltage V of 0 is equal to 0, then our impedance of the capacitor in the last domain Z of s.
[00:48:11 - 00:48:16] So impedance is defined as the voltage for the of s over the current I of s.
[00:48:16 - 00:48:26] And then that gives us one over S C.
[00:48:26 - 00:48:36] So when we go to analyzing circuits in the last domain, we can write the impedance as one over S C.
[00:48:36 - 00:48:40] We don't need to go through all the derivation there.
[00:48:40 - 00:48:49] And then for what we'll go through the inductor.
[00:48:49 - 00:48:57] Tomorrow I think we'll just do the resistor now because that's a nice way to do the last minute.
[00:48:57 - 00:48:59] And that's much easier.
[00:48:59 - 00:49:04] So the impedance of the resistor is R in the time domain.
[00:49:04 - 00:49:08] So these are kind of time domain ones on the left hand side.
[00:49:08 - 00:49:11] And the plus on the right.
[00:49:11 - 00:49:19] And so in the plus domain, the impedance of the resistor is also equal to,
[00:49:21 - 00:49:24] I guess I'll let you finish writing those ones down tomorrow.
[00:49:24 - 00:49:27] We'll come back and do the impedance of the inductor.
[00:49:27 - 00:49:36] And then we can tackle that circuit that we're looking at at the time domain in the last domain instead.
[00:49:36 - 00:49:41] And then we'll get onto the next set of lecture slides, which is on Fourier transforms.
[00:49:41 - 00:49:47] Those are up and learn as well for those of you that are downloading or printings or what have you.
[00:49:47 - 00:49:51] Okay, and I'll remind you that there's a tutorial on Thursday afternoon.
[00:49:51 - 00:49:54] Pretty sure I'll sit here straight after the lecture.
[00:49:54 - 00:49:57] And the questions are up there already.
[00:49:57 - 00:50:01] Have a look at those beforehand if you want.
[00:50:01 - 00:50:30] So then you have to, then you would have a constant value here.
[00:50:30 - 00:50:33] And you're a patient.
[00:50:33 - 00:50:40] So I think for all the cases we're considering, when you're supposed to close,
[00:50:40 - 00:50:43] we're going to have the two zeros.
[00:50:43 - 00:50:51] So then we're going to do the analog filters later on,
[00:50:51 - 00:50:57] and we're looking at the steady states.
[00:50:57 - 00:50:59] Good.
[00:50:59 - 00:51:06] Thank you.
[00:51:06 - 00:51:13] Thank you.
[00:51:13 - 00:51:20] Thank you.
[00:51:20 - 00:51:27] Thank you.
[00:51:27 - 00:51:34] Thank you.
[00:51:34 - 00:51:41] Thank you.
[00:51:41 - 00:51:48] Thank you.
[00:51:48 - 00:51:55] Thank you.
[00:51:55 - 00:52:02] Thank you.
[00:52:02 - 00:52:05] Thank you.
[00:52:05 - 00:52:12] Thank you.
[00:52:12 - 00:52:19] Thank you.
[00:52:19 - 00:52:26] Thank you.
[00:52:26 - 00:52:33] Thank you.
[00:52:33 - 00:52:40] Thank you.
[00:52:40 - 00:52:47] Thank you.
[00:52:47 - 00:52:54] Thank you.
[00:52:54 - 00:53:01] Thank you.
[00:53:01 - 00:53:08] Thank you.
[00:53:08 - 00:53:23] Thank you.
[00:53:23 - 00:53:38] Thank you.
[00:53:38 - 00:53:53] Thank you.
[00:53:53 - 00:54:08] Thank you.
[00:54:08 - 00:54:23] Thank you.
[00:54:23 - 00:54:38] Thank you.
[00:54:38 - 00:54:53] Thank you.
[00:54:53 - 00:55:13] Thank you.

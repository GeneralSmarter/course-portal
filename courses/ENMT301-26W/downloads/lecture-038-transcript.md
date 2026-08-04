# ENMT301-26W Lecture 38 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `06d7571d7701ba786ce9d946b72b2ab6804bc2a5fcd2270da9e672d12c73dc02`
Generated: 2026-06-06T06:29:37.406835+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:01 - 00:00:05] Okay, good afternoon everyone.
[00:00:05 - 00:00:10] So to start with a quick recap of what we're doing in the end of yesterday.
[00:00:10 - 00:00:13] So we're looking at a difference between analog signals and digital signals.
[00:00:13 - 00:00:21] So analog signals as shown here, we have the signals continuous with time and also its
[00:00:21 - 00:00:25] continuous in its values, so here with voltage.
[00:00:25 - 00:00:33] Okay, and that's real world signal, so the voltage in a circuit is an example of analog signal.
[00:00:33 - 00:00:41] And then for a digital signal we have it, so it sampled in time, so we just have values at particular instances in time.
[00:00:41 - 00:00:53] And it's quantized in value, so we have a certain number of different levels, which is defined by the number of bits we have in our microcontroller.
[00:00:53 - 00:01:08] So we went through and then defined some of these common signals that we're going to make use of through the terms, the DC, AC, exponential, and here the unit step function.
[00:01:08 - 00:01:22] So the unit step function is good for like when we have a circuit, when switching our circuit, then the signal starts at a particular instance in time.
[00:01:22 - 00:01:34] Okay, so what do we get if we differentiate this unit step function, what are we going to get?
[00:01:34 - 00:01:41] It's going to be zero everywhere apart from.
[00:01:41 - 00:01:51] Yeah, it's zero. So this is all blue along here, so this is constant, the derivative of the constant is zero, and then the T greater than zero.
[00:01:51 - 00:01:55] The symbol here.
[00:01:55 - 00:02:02] Then the constant, the derivative of that is zero, and then we have, okay, now I've got a symbol.
[00:02:02 - 00:02:16] And at the origin here where T is zero, what's the derivative at T is zero going to be infinity, sort of being that with zero, then infinity, and zero.
[00:02:16 - 00:02:23] Yep, which is also known as a, yeah, on part of the one, Dirac delta function.
[00:02:23 - 00:02:25] So this will be okay.
[00:02:25 - 00:02:30] And so you've probably seen that in your maths courses hopefully.
[00:02:30 - 00:02:34] Okay, so learning something new, get your money's worth.
[00:02:34 - 00:02:42] Okay, so, so this Dirac delta function is a sort of made up mathematical function.
[00:02:42 - 00:02:47] And it's purpose within engineering is to look at the impulse response.
[00:02:47 - 00:02:55] So when we put a voltage spike into our circuit to see what happens to our voltages in our circuit.
[00:02:55 - 00:03:06] And so mathematically, it's defined, so our voltage here, V of T, is equal to, so it's the Dirac delta function is delta.
[00:03:06 - 00:03:09] So here is the function of time T.
[00:03:09 - 00:03:22] And that's the derivative with respect to time T of our unit step function, U of T step.
[00:03:22 - 00:03:35] Okay, and so here, V of T is equal to zero, the T not equal to zero.
[00:03:35 - 00:03:49] And also it's part of the definition, the integral from minus infinity to infinity of delta T is equal to one.
[00:03:49 - 00:03:58] Okay, so it's got the area under that arrow is one.
[00:03:58 - 00:04:00] Okay, so that's how it's defined.
[00:04:00 - 00:04:03] And so it doesn't actually have a height of one here.
[00:04:03 - 00:04:06] Actually, we have the delta function.
[00:04:06 - 00:04:14] It has infinite height and zero width.
[00:04:14 - 00:04:21] Okay, obviously we can draw an arrow that has an infinite height.
[00:04:21 - 00:04:24] So here it's just being shown up to one.
[00:04:24 - 00:04:37] Okay, so this delta function is also useful when we look at sampling later on.
[00:04:37 - 00:04:52] When you're sampling a single time, you're then multiplying by a delta function at each point in time.
[00:04:52 - 00:04:55] Okay, a couple more functions to go with our analog ones.
[00:04:55 - 00:05:00] So the next one is the rectangular function or Rict.
[00:05:00 - 00:05:13] And so this is defined, so here, Rict of T is equal to either one or zero.
[00:05:13 - 00:05:24] So it's one when the magnitude of time T is less than or equal to a half, and at zero otherwise.
[00:05:24 - 00:05:30] Okay, so it's 0.5 here, and then minus 0.5.
[00:05:30 - 00:05:40] Okay, so then the red function has a width of one, and it's also got a height of one, so the area of it is one.
[00:05:40 - 00:05:45] Okay, so the rectangular function is useful.
[00:05:45 - 00:05:53] If we're doing something called windowing, so if we're just looking at a signal over a particular instance of time,
[00:05:53 - 00:05:58] we would then multiply by a direct function, possibly shifted.
[00:05:58 - 00:06:13] Okay, so like some of these other functions, the inner step, and the direct delta, it's not physically realizable in real life.
[00:06:13 - 00:06:22] You cannot get a perfect step change from 0 to 1 on the rising edge or from 1 to 0 on the falling edge.
[00:06:22 - 00:06:30] So in reality, you're going to have some finite rise time and full time.
[00:06:30 - 00:06:34] Okay, so rise and fall.
[00:06:34 - 00:06:44] Okay, so like your clock signals and 360, 360 last year, they're not a perfect square wave.
[00:06:44 - 00:06:47] They do have this rising edge and a falling edge.
[00:06:47 - 00:07:01] Okay, the last function we're going to do for our continuous signals is a tone burst.
[00:07:01 - 00:07:07] And so this is useful for describing a radar or sonar pulse.
[00:07:07 - 00:07:13] So say we're going to soder, we send a pulse down to the bottom version of the floor,
[00:07:13 - 00:07:15] and then we wait for the reflection back.
[00:07:15 - 00:07:22] So we don't want to be always transmitting, because then we won't know how long the pulse to go down and back up again.
[00:07:22 - 00:07:29] So we have this windowed here, sine wave.
[00:07:29 - 00:07:37] So we've seen the pulse wave for a while, and then we've seen another pulse, and that way we can work out the distance to what's reflecting back to us.
[00:07:37 - 00:07:40] And the same approach applies in radar.
[00:07:40 - 00:07:46] Okay, so let's describe this tone burst, V of t.
[00:07:46 - 00:07:53] How many different parameters are going to define this signal?
[00:07:53 - 00:07:58] Well, I can just guess, tell me what they are for a start.
[00:07:58 - 00:08:04] Amplitude one, okay, so let's start with that.
[00:08:04 - 00:08:07] A for amplitude, so it's here on the graphs, amplitudes.
[00:08:07 - 00:08:12] Then what else do we have?
[00:08:12 - 00:08:18] A period, yep, so we have, so we've got this rectangular function.
[00:08:18 - 00:08:27] And for the rectangular function, we scale it by capital T our period.
[00:08:27 - 00:08:35] So this is then got a width here, or period, as capital T.
[00:08:35 - 00:08:39] And then what other part do we have?
[00:08:39 - 00:08:44] So this, we've got a sine function, yep, we're actually here as the cosine,
[00:08:44 - 00:08:46] but you can make the sine of a cosine with a shift.
[00:08:46 - 00:08:55] So then got cosine two pi times our frequency, if not, times time.
[00:08:55 - 00:09:00] Plus we've got the space shift, which we saw yesterday with our AC signal.
[00:09:00 - 00:09:06] So that's the way we can shift this from a cosine all the way to a sine.
[00:09:06 - 00:09:17] So we've got then four parameters, we've got this frequency, and then this phase shift.
[00:09:17 - 00:09:19] So, let's try that here.
[00:09:19 - 00:09:24] So this tone verse is defined by these four parameters.
[00:09:24 - 00:09:36] Okay, so let's do an example.
[00:09:36 - 00:09:41] I'll put some tutorial questions up on learn tomorrow for next week, which will be
[00:09:41 - 00:09:49] similar, we're just going to use to writing down different signals mathematically.
[00:09:49 - 00:09:52] Okay, so we've got the signal here.
[00:09:52 - 00:09:58] It's got a value of zero for T less than three, and a value of zero for T greater than five.
[00:09:58 - 00:10:04] And it's got a value of three between three and five.
[00:10:04 - 00:10:10] Okay, so V of T is equal to...
[00:10:10 - 00:10:13] What's the first thing?
[00:10:13 - 00:10:15] That's a kind of rec function.
[00:10:15 - 00:10:24] Yep, so we've got here, rec, and what do we need to do with rec function?
[00:10:24 - 00:10:26] Give an amplitude of three, good.
[00:10:26 - 00:10:28] I'll lift myself a space for that.
[00:10:28 - 00:10:32] What else do we need to do with this rec function?
[00:10:32 - 00:10:33] Scale the period.
[00:10:33 - 00:10:36] So we've then got rec T's.
[00:10:36 - 00:10:38] What's the period here?
[00:10:38 - 00:10:43] Two, so period equals two.
[00:10:43 - 00:10:47] We're going to go T over two.
[00:10:47 - 00:10:49] They're not smithing.
[00:10:49 - 00:10:54] Give me a clue by the way, I've written the brackets here.
[00:10:54 - 00:10:55] Shift that.
[00:10:55 - 00:10:56] Yes, how do we do that?
[00:10:56 - 00:10:59] Do we add four or minus four?
[00:10:59 - 00:11:01] Minus four, good.
[00:11:01 - 00:11:02] Yep.
[00:11:02 - 00:11:03] Here we go.
[00:11:03 - 00:11:04] All done.
[00:11:04 - 00:11:06] So the period was two.
[00:11:06 - 00:11:10] The amplitude was three.
[00:11:10 - 00:11:17] And the shift was...
[00:11:17 - 00:11:22] It's the next week we'll start taking four transforms of these signals as well.
[00:11:22 - 00:11:28] Okay, so that was the end of continuous signals.
[00:11:28 - 00:11:33] And then we'll go through some digital ones.
[00:11:33 - 00:11:35] Just great time ones.
[00:11:35 - 00:11:38] So with the analog we were using round brackets.
[00:11:38 - 00:11:41] So V of T, with T was in round brackets.
[00:11:41 - 00:11:45] Now for digital one, we were sampled in time.
[00:11:45 - 00:11:48] We're going to use square brackets.
[00:11:48 - 00:11:55] So we've got V of N, and N is the N-fulcage sample.
[00:11:55 - 00:12:07] Okay, so we can relate the continuous time signal to our discrete time digital signal by substituting in for T,
[00:12:07 - 00:12:17] which is our continuous time, which was a real number.
[00:12:17 - 00:12:24] So little T is equal to then the sample number N times our period T.
[00:12:24 - 00:12:33] So sample number is a number of z integers, and T was our period.
[00:12:33 - 00:12:47] Okay, and this period T is then equal to one over our sampling frequency Fs.
[00:12:47 - 00:12:57] Okay, so if we're sampling, I say the voltage in our circuit at...
[00:12:57 - 00:13:04] It's a kilohertz, then the period T is going to be one millisecond.
[00:13:04 - 00:13:14] Okay, and so for discrete time signals, we can draw them with what's known as a lollipop or stem plot,
[00:13:14 - 00:13:21] because the values only exist at the sample values in.
[00:13:21 - 00:13:27] It's not continuous in time.
[00:13:27 - 00:13:34] Okay, we can also write our discrete time signals as a sequence.
[00:13:34 - 00:13:40] Okay, so here we've got the unit step, you're then written two different ways.
[00:13:40 - 00:13:56] And the value for N is zero is often indicated in these sequences with either an underlying or with an arrow.
[00:13:56 - 00:14:05] Okay, so that tells us where our origin is in the discrete time sequence representation.
[00:14:05 - 00:14:12] Okay, so these two are then the unit step and digital space.
[00:14:12 - 00:14:20] So we've got zero, zero, then one, one.
[00:14:20 - 00:14:23] So this is in zero.
[00:14:23 - 00:14:29] Okay, so it is a unit step.
[00:14:29 - 00:14:45] Okay, so we'll quickly rip through the same functions that we looked at analog,
[00:14:45 - 00:14:47] but in their digital representation now.
[00:14:47 - 00:14:51] So it's all written down somewhere.
[00:14:51 - 00:14:54] Okay, so direct current Dc.
[00:14:54 - 00:15:00] So it's constant value of A for all samples in.
[00:15:00 - 00:15:14] So the square brackets of N, our sample number is equal to the amplitude A.
[00:15:14 - 00:15:16] Okay, hopefully straight forward.
[00:15:16 - 00:15:21] And so then these are the values of N along the x-axis.
[00:15:21 - 00:15:25] So it only exists for integer values of N.
[00:15:25 - 00:15:32] Okay, and then for AC, we've got this cosine waveform.
[00:15:32 - 00:15:36] And so we, the same equation is before for analog.
[00:15:36 - 00:15:40] So we've got V of N now.
[00:15:40 - 00:15:42] So that's our digital signal.
[00:15:42 - 00:15:49] We've got our amplitude A cosine 2 pi if not.
[00:15:49 - 00:15:56] And we replace little t time by our sample number, the ln and the period t.
[00:15:56 - 00:16:08] And we've got this phase by, so we've got here frequency, amplitude, period.
[00:16:08 - 00:16:11] And phase.
[00:16:11 - 00:16:25] Okay, so that's AC.
[00:16:25 - 00:16:28] We also did exponential in this day.
[00:16:28 - 00:16:36] So our discrete time signal of voltage of lost the log that got there somehow.
[00:16:36 - 00:16:38] There we go.
[00:16:38 - 00:16:48] The of square brackets in is equal to exponential to right as exp.
[00:16:48 - 00:16:55] So minus alpha is a constant, which governs half-fast our signal to k's.
[00:16:55 - 00:17:00] And we replace little t from the analog with N capital T.
[00:17:00 - 00:17:04] And we can also simplify this to say that, have also,
[00:17:04 - 00:17:10] actually, some constant A to the power of our sample N.
[00:17:10 - 00:17:20] And that's because we can write this as A equals E to the minus alpha capital T.
[00:17:20 - 00:17:23] And this thing is a constant.
[00:17:23 - 00:17:40] Okay, so because it's a constant, we can take it out.
[00:17:40 - 00:17:41] Okay, two more to go.
[00:17:41 - 00:17:43] So we've got the unit step is the next one.
[00:17:43 - 00:17:45] Just to make sure we're in this one.
[00:17:45 - 00:18:01] Okay, so our unit step here, so our voltage V of N is equal to,
[00:18:01 - 00:18:10] we're not going to delta it in a step.
[00:18:10 - 00:18:25] Okay, so V of N is equal to U of N because it's unit step, U of U of U.
[00:18:25 - 00:18:33] And so this has values like the analog case where our unit step is as value of one
[00:18:33 - 00:18:40] in gramm equals zero or as a value of zero for N, less than zero.
[00:18:40 - 00:18:48] And so we can write this as a sequence as we did a couple of slides ago where we have values of zero
[00:18:48 - 00:18:49] in one.
[00:18:49 - 00:18:56] We indicate that in a zero for that.
[00:18:56 - 00:18:59] First one, by drawing a line or an arrow underneath it.
[00:18:59 - 00:19:02] And then we have ones dot dot dot.
[00:19:02 - 00:19:16] Okay, now we'll do the delta.
[00:19:16 - 00:19:21] So this is for a digital signal that's known as the conical delta.
[00:19:21 - 00:19:27] And so this does have a value of one for unit zero.
[00:19:27 - 00:19:33] So V of N is equal to delta of N.
[00:19:33 - 00:19:46] So this has values of one for unit zero and zero otherwise.
[00:19:46 - 00:19:54] So to write this as a sequence, our photo signal V of N would be dot dot dot zero,
[00:19:54 - 00:20:15] zero, earlier one, zero, zero.
[00:20:15 - 00:20:20] Okay, and so then lastly for dealing with different signal types.
[00:20:20 - 00:20:31] Before we get on to talking about noise, we can also write our sequence as some of these conical delta
[00:20:31 - 00:20:32] directions.
[00:20:32 - 00:20:44] So if our sequence is zero is then one, two, three, we can write V of N is delta of N.
[00:20:44 - 00:20:53] Then two times delta of N minus one, three times delta in minus two.
[00:20:53 - 00:21:18] Okay, so we've now gone through the basic signal types and both analog and digital domain.
[00:21:18 - 00:21:25] So next thing we're going to go through today and probably start tomorrow is then different types of noise.
[00:21:25 - 00:21:34] So we've got then signals and noise and then we'll start looking at the frequency domain for our signals
[00:21:34 - 00:21:41] and then how we can filter out noise from our signal and either the analog domain or the digital domain.
[00:21:41 - 00:21:45] Okay, so that's where we're going.
[00:21:45 - 00:21:47] Okay, so what's noise?
[00:21:47 - 00:22:00] At some unwanted random quantity that affects our signal and so noise is generated in all electric circuits.
[00:22:00 - 00:22:03] The matter of how expensive your components are.
[00:22:03 - 00:22:09] You are going to have some noise generated in the resistors and in the semiconductors.
[00:22:09 - 00:22:11] So your transistors are pamps, etc.
[00:22:11 - 00:22:21] And so the way we model noise is as a random process.
[00:22:21 - 00:22:32] And so at each point in time, the value of the noise is a random variable and it has some sort of probability density function.
[00:22:32 - 00:22:39] Okay, so to get a noise signal, this is a realization of a random process.
[00:22:39 - 00:22:41] So we'll do a little bit of statistics.
[00:22:41 - 00:22:46] When we talk about noise, sort of an unknown random quantity.
[00:22:46 - 00:22:53] So we don't know the exact value at any point in time unlike our signals that we've just talked about.
[00:22:53 - 00:22:56] This is a probabilistic function.
[00:22:56 - 00:23:06] Okay, so here I've got in this plot three realizations of noise.
[00:23:06 - 00:23:10] And so this is a zero mean like Gaussian noise.
[00:23:10 - 00:23:19] Okay, so to zero means that mu is equal to zero.
[00:23:19 - 00:23:25] And you can see from these figures, they're all sort of oscillating about zero.
[00:23:25 - 00:23:35] It's white noise, which means that all frequencies have the same power.
[00:23:35 - 00:23:41] We'll look at different types of noise a bit later on.
[00:23:41 - 00:23:47] So you can have some noise that's more low frequency noise or you can have some noise that's more high frequency noise.
[00:23:47 - 00:23:50] And so these are known as pink and blue noises.
[00:23:50 - 00:23:56] But in this case, the noise that was added, for example, is white Gaussian noise.
[00:23:56 - 00:24:03] And this has in this case the variance is equal to one.
[00:24:03 - 00:24:11] And we've got here in these examples, we've got 400 samples in each case.
[00:24:11 - 00:24:16] Okay, so this is generating noise and python at each time, which is given a different random seed.
[00:24:16 - 00:24:21] And you get a different looking realization of our noise.
[00:24:21 - 00:24:35] Okay, so this is then our bulk example will be of in as a function of in each of these three cases.
[00:24:35 - 00:24:46] Okay, so if we consider a particular instance in time, so this is for in is about 60 something like that,
[00:24:46 - 00:24:57] we've highlighted the noise value with an orange dot.
[00:24:57 - 00:25:10] And so the values of the voltage at that point in time are then defined as a probability density function.
[00:25:10 - 00:25:16] Okay, and so we've added Gaussian noise in this example.
[00:25:16 - 00:25:28] So if we look at all the values at that point in time, then they get defined by a Gaussian process.
[00:25:28 - 00:25:37] And so the Gaussian is defined by two parameters, the mean u and variance sigma squared.
[00:25:37 - 00:25:44] And so the probability density function for the Gaussian, we can write as an equation.
[00:25:44 - 00:25:48] So I'm going to use P for probability.
[00:25:48 - 00:25:58] And then we've got a subscript here, V of t, which is our random variable.
[00:25:58 - 00:26:05] And this probability density function is a function of the voltage V.
[00:26:05 - 00:26:09] The example shown here before.
[00:26:09 - 00:26:12] So the probability density function of the bottom is the Gaussian.
[00:26:12 - 00:26:23] So the values are near zero, but we can have some larger values and some smaller values that are less likely.
[00:26:23 - 00:26:29] So it's got this classical normal distribution for a Gaussian.
[00:26:29 - 00:26:41] Okay, so it was got our probability density function of the Gaussian is defined as one over sigma squared of the variance and
[00:26:41 - 00:26:55] the Gaussian root 2 pi e to the minus the voltage minus the mean squared over 2 times the variance.
[00:26:55 - 00:27:15] Okay, but if we want to find what's the probability that our noise has a value at this particular point in time between two different
[00:27:15 - 00:27:21] one and V2, we can find it as the area under this probability density function.
[00:27:21 - 00:27:36] Okay, so if we want what's the probability that our noise is between V2 and V1, what we can do is we can integrate the Gaussian functions between V1 and V2.
[00:27:36 - 00:27:43] So we're finding the area under the curve, which is this blue area with the black cross hat geometry.
[00:27:43 - 00:27:45] So that lines on it.
[00:27:45 - 00:28:17] Okay, so mathematically we're saying the probability that our noise voltage V of t is between V1 and V2 is then equal to the integral between V1 and V2 of our probability density function
[00:28:17 - 00:28:28] p underscore V of t and it's a function of the voltage V and we're integrating over the voltage V.
[00:28:28 - 00:28:54] Okay, so Gaussian is the most common noise type with this normal distribution and we have this governing equation for the probability density function.
[00:28:54 - 00:29:07] Then we can integrate that to find the likelihood that our noise is between particular values.
[00:29:07 - 00:29:12] Okay, so we'll do some more definitions to do with noise.
[00:29:12 - 00:29:22] So, a stationary process means that the mean and variance do not change with time.
[00:29:22 - 00:29:34] Okay, so say if our circuit was heating up then the noise properties might change with time, and so in that case we would be non-stationary.
[00:29:34 - 00:29:48] But the normal assumptions are that it's stationary so that the statistics of the mean and variance are not changing with time.
[00:29:48 - 00:30:07] So the power spectral density PSD which has a symbol capital S underscore V for voltage as a function of frequency tells us how the noise power is determined by the frequency.
[00:30:07 - 00:30:18] So, we have the right noise that says a flat spectrum all frequencies have equal power.
[00:30:18 - 00:30:30] Whereas for pink noise we have more power at low frequencies and for blue noise we have more power at high frequencies.
[00:30:30 - 00:30:48] So, we can see that the noise and semiconductor devices shortly and this has a pink noise component as there's more noise at the low frequencies and we'll look at the noise for a resistor which has a uniform power spectral density that has white noise.
[00:30:48 - 00:30:52] Okay, so we can get the variance of our noise.
[00:30:52 - 00:30:56] So, that's the variance sigma of the voltage.
[00:30:56 - 00:31:16] So, the variance of our noise is the integral sort of one side integral so from zero to infinity of our power spectral density Sb which is a function of frequency F and we're integrating over all frequencies.
[00:31:16 - 00:31:24] So, essentially adding up the noise power at a frequency to get out total noise.
[00:31:24 - 00:31:32] Okay, so we're thinking about a voltage here, noise voltage.
[00:31:32 - 00:31:41] So, this has then units is equal to sigma squared as units then volts squared.
[00:31:41 - 00:32:12] The units of our power spectral density Sb of F, this has units of volts squared so that's energy per frequency.
[00:32:12 - 00:32:16] And then we, so this is volts squared per hertz.
[00:32:16 - 00:32:21] We're integrating with respect to F. So, hertz is the symbol for F obviously.
[00:32:21 - 00:32:32] And so then because we're multiplying by the F and integral the hertz disappears and we just have a units of volts squared.
[00:32:32 - 00:32:46] And there's another way to define the noise spectral density which is the amplitude spectral density which we can get.
[00:32:46 - 00:32:58] So, this has a symbol A, V of F and we can get the simply as the square root of our power spectral density.
[00:32:58 - 00:33:06] So, this is equal to square root of Sb of F.
[00:33:06 - 00:33:25] Okay, so the question for you then, why I'm trying to worry, I think about is what is the units of the amplitude spectral density going to be?
[00:33:25 - 00:33:37] And it gives us volts per square root of F. Can you have a unit that does a square root of someone where you can, because that's what units are.
[00:33:37 - 00:33:52] But so you probably haven't seen units that are a square root of something before but that's what it is because that's the square root of volts squared per hertz.
[00:33:52 - 00:34:05] Okay, so let's look at some of the noise sources then within our circuits.
[00:34:05 - 00:34:18] Okay, so the first one is thermal noise which is also known as Johnson noise or Shannon noise.
[00:34:18 - 00:34:32] So, if we have our resistor even if it's going to be voltage across it, we're going to have our electrons in there and they're going to be bouncing up and down.
[00:34:32 - 00:34:39] So this is then generating this agitation of our electrons generating heat.
[00:34:39 - 00:34:44] And this is then producing noise.
[00:34:44 - 00:34:52] Okay, so this thermal noise is independent of the applied voltage.
[00:34:52 - 00:35:08] Okay, so in your circuit this resistor is really a resistor in series with a little voltage source.
[00:35:08 - 00:35:16] And so this is just generating random voltages. Small voltages.
[00:35:16 - 00:35:25] But the resistor, no resistor, no matter how expensive or what the threshold you have will be producing some noise.
[00:35:25 - 00:35:32] So we model that noise as a voltage source in series with our resistor.
[00:35:32 - 00:35:41] Okay, so this is our noise voltage source.
[00:35:41 - 00:36:01] Okay, so for our thermal noise and our resistor, the FT, it can be described by a Gaussian-Rout?
[00:36:01 - 00:36:05] Yes. Yes, noise, yes.
[00:36:05 - 00:36:20] These plots will look similar.
[00:36:20 - 00:36:25] The statistics will be the same no matter what voltages across the resistor.
[00:36:25 - 00:36:29] Yes, so we'll go through the equation and on the other side I think.
[00:36:29 - 00:36:33] And then you'll see what parameters it is a function of.
[00:36:33 - 00:36:39] Okay, so what do we think the mean is going to be for our thermal noise?
[00:36:39 - 00:36:41] Zero, you know, because that's zero, good.
[00:36:41 - 00:36:46] So it's a Gaussian with a mean of zero.
[00:36:46 - 00:36:53] Okay, so the variance of our noise.
[00:36:53 - 00:37:00] What sort of parameters do we think are going to affect the variance of our noise?
[00:37:00 - 00:37:04] What's going to make it noise here?
[00:37:04 - 00:37:06] The value of the resistor, good, yep.
[00:37:06 - 00:37:10] We'll put that in our equation towards the end.
[00:37:10 - 00:37:15] Team pressure, good.
[00:37:15 - 00:37:17] So it's independent of the voltage.
[00:37:17 - 00:37:18] Yep.
[00:37:18 - 00:37:21] And then the other ones are probably not guessable.
[00:37:21 - 00:37:23] So we've also got a function.
[00:37:23 - 00:37:26] So, constant out the front four.
[00:37:26 - 00:37:28] We've got another constant k.
[00:37:28 - 00:37:31] Then I'll know what this k is going to be.
[00:37:32 - 00:37:34] Boltzmann's constant, yep, good.
[00:37:34 - 00:37:42] And then it's also a function of the bandwidth over which we measure the signal.
[00:37:42 - 00:37:47] Okay, so if the noise is white noise, so it exists for all frequencies,
[00:37:47 - 00:37:54] but if we just evaluate over a range of frequencies, we'll get less noise within that range.
[00:37:54 - 00:37:55] Okay.
[00:37:55 - 00:37:58] So, I'm going to write all these down.
[00:37:58 - 00:38:22] Okay, so k is then, as you see, at Boltzmann's constant, which is 1.38 times 10 to the minus 23 joules per Kelvin.
[00:38:22 - 00:38:35] Our resistance, which is in ohms, good.
[00:38:35 - 00:38:38] We'll see is temperature.
[00:38:38 - 00:38:40] Sure.
[00:38:40 - 00:38:43] Well, the units for temperature here.
[00:38:43 - 00:38:44] Okay, good.
[00:38:44 - 00:38:49] Okay.
[00:38:49 - 00:38:58] And then so the variance signal squared, if we want the RMS noise of voltage,
[00:38:58 - 00:38:59] it'll be again.
[00:38:59 - 00:39:09] We can get that then as the square root of 4kTb.
[00:39:09 - 00:39:37] Okay, so here's a realization of thermal noise.
[00:39:37 - 00:39:42] So this is Gaussian-white noise versus time.
[00:39:42 - 00:39:47] So that's the blue curve.
[00:39:47 - 00:39:51] And then the orange curve here is the moving average.
[00:39:51 - 00:40:05] So the orange curve is the moving average of that 200 samples.
[00:40:05 - 00:40:18] Okay, so if we take an average of enough samples, then we essentially filter hang out the noise.
[00:40:19 - 00:40:23] Okay, so it's a very simple low pass filter.
[00:40:23 - 00:40:30] So we're letting the low frequencies pass through and we're filtering out the high frequencies.
[00:40:30 - 00:40:34] And we're getting close to zero.
[00:40:34 - 00:40:41] Ten minutes to go.
[00:40:41 - 00:40:43] Okay, so let's do an example.
[00:40:43 - 00:40:48] Let's calculate our RMS noise voltage for a 1-kilow-ohm resistor.
[00:40:48 - 00:40:53] So I think I've got the right color bands here for the 1-ohm-ohm resistor.
[00:40:53 - 00:40:54] Anybody know these?
[00:40:54 - 00:40:55] These days?
[00:40:55 - 00:40:56] No, I don't.
[00:40:56 - 00:40:59] Okay, so it's a room temperature.
[00:40:59 - 00:41:05] So to get the Kelvin temperature you add on 273,
[00:41:05 - 00:41:09] since assuming a room temperature about 20 degrees Celsius.
[00:41:09 - 00:41:20] And we'll get a measure it over an audio bandwidth, which is typically from 0 to 20 kilohertz.
[00:41:20 - 00:41:29] Okay, so then 1093k is equal to 20 degrees C.
[00:41:29 - 00:41:34] Okay, so let's calculate our RMS noise voltage.
[00:41:34 - 00:41:40] Little V in is equal to the square root of 4kTb,
[00:41:40 - 00:41:47] the square root here.
[00:41:47 - 00:41:59] So 4 times Boltzmann's constant is 1.38 times 10 to the minus 23 times our temperature.
[00:41:59 - 00:42:06] And Kelvin 23 times our resistance, which is 1,000 times our audio bandwidth,
[00:42:06 - 00:42:09] which is 20 kilohertz.
[00:42:09 - 00:42:21] So we end up V in our RMS noise voltage is 0.57 micro volts.
[00:42:21 - 00:42:37] So then we can actually write our resistor is then a noise source of RMS voltage 0.57 micro volts
[00:42:37 - 00:42:41] in series with our 1-kilow-ohm resistor.
[00:42:41 - 00:42:49] Okay, so it's the favorite model of our resistor.
[00:42:49 - 00:42:56] Okay, so that's not a very large number, but depending what we're doing with our resistor,
[00:42:56 - 00:43:04] we might have the signal coming out of the resistor going through an amplifier.
[00:43:04 - 00:43:09] So if it's an amplifier with a gain of 1,000,
[00:43:09 - 00:43:14] then not just the signal is going to be amplified by 1,000, but our noise is going to be amplified by 1,000.
[00:43:14 - 00:43:21] So then our RMS noise voltage would be 0.57 millivolts.
[00:43:21 - 00:43:47] Okay, so we can define these spectral,
[00:43:47 - 00:43:52] spectral density for our thermal noise follows.
[00:43:52 - 00:43:58] So our PSD, our power spectral density,
[00:43:58 - 00:44:11] S of F, and the case of thermal noise is then 4kT R.
[00:44:11 - 00:44:17] Okay, so this is unit of volt squared, perhaps.
[00:44:17 - 00:44:23] Okay, so this is independent of frequency.
[00:44:23 - 00:44:26] Okay, so it's a constant value.
[00:44:26 - 00:44:36] And so it's what we call white noise where the noise power spectral density isn't affected by frequency.
[00:44:36 - 00:44:38] And there's another thing we're just to find.
[00:44:38 - 00:44:40] A few slides back, if I'm in this back.
[00:44:40 - 00:44:47] The amplitude spectral density, a subscript B for voltage,
[00:44:47 - 00:44:53] or frequency F, is the square root of the noise power spectral density.
[00:44:53 - 00:44:58] So this is in the square root of 4kT R,
[00:44:58 - 00:45:04] and has units of volt per square root of Hertz, as we discussed.
[00:45:04 - 00:45:25] Okay, so if we look some of these amplitude spectral densities,
[00:45:25 - 00:45:30] the three different resistors of room temperature.
[00:45:30 - 00:45:36] Okay, so most important thing to note is this is white noise.
[00:45:36 - 00:45:44] We have the same value of the amplitude spectral density for all values of frequency F.
[00:45:44 - 00:45:58] And this amplitude spectral density,
[00:45:58 - 00:46:06] so this scales with square root of our resistance.
[00:46:06 - 00:46:16] Okay, so the larger the value of our resistor, so the 100kO in green,
[00:46:16 - 00:46:26] is then, what's that square root of 10 times larger than for the 10kA in orange.
[00:46:26 - 00:46:38] Okay, so we've got a couple of minutes left,
[00:46:38 - 00:46:44] so we'll introduce another noise type, which is known as shot noise.
[00:46:44 - 00:46:51] And this is to do with electron flow in our semiconductors,
[00:46:51 - 00:47:01] and so we can have some of the semiconductors or some of the charge carriers,
[00:47:01 - 00:47:05] electrons, crystal pro thing.
[00:47:05 - 00:47:16] They can be traveling in the wrong direction, so they might not be all flowing together
[00:47:16 - 00:47:18] in the same way at the same time.
[00:47:18 - 00:47:26] So let's say this one actually decides it wants to go some across against the current.
[00:47:26 - 00:47:37] This is going to generate some sort of noise which we call shot noise.
[00:47:37 - 00:47:44] Okay, so there's an equation for the RMS current,
[00:47:44 - 00:47:59] which is I subscribe in for noise, is equal to the square root of 2 times the charge carrier is charge q.
[00:47:59 - 00:48:07] Again, the bandwidth over which we consider our signal, our noise, B,
[00:48:07 - 00:48:32] and our current, okay, so here capital I is our current, q is the charge electron,
[00:48:32 - 00:48:41] so this is equal to 1.6 times 10 to the minus 19 coulombs,
[00:48:41 - 00:48:48] and B was our measurement bandwidth.
[00:48:48 - 00:48:58] Now, I have to go back, I don't think I wrote what B was,
[00:48:58 - 00:49:01] and then we did thermal noise, so I better go back and do that.
[00:49:01 - 00:49:02] I'll see you finish this.
[00:49:02 - 00:49:24] Okay, well just while we remember, I'll just shoot back and here I'm going to never define what B was.
[00:49:24 - 00:49:37] So B is the measurement bandwidth, and that's...
[00:49:37 - 00:49:46] Okay, we'll stop there.
[00:49:46 - 00:49:51] If they will do an example of shot noise to start tomorrow,
[00:49:51 - 00:49:54] then we'll look at the last noise type of second noise,
[00:49:54 - 00:49:59] and then we'll go into looking at different types of interference that can happen in our circuit as well.
[00:49:59 - 00:50:35] So I think I'll see you at 12 tomorrow.
[00:50:35 - 00:50:39] Hi, shot.
[00:50:39 - 00:50:47] Well, noise is kind of random, and you can't sort of deterministic,
[00:50:47 - 00:50:49] say, run equation for it.
[00:50:49 - 00:50:53] If you think about 50 hertz interference from the mains,
[00:50:53 - 00:50:54] you can run equation for it.
[00:50:54 - 00:50:57] So there's a difference between it being random and being deterministic.
[00:50:57 - 00:50:59] Yeah, thank you very much.
[00:50:59 - 00:51:01] But both the problems, the most things you don't want,
[00:51:01 - 00:51:04] but it's easy to focus on our random equation for it,
[00:51:04 - 00:51:06] and we're going to define it.
[00:51:06 - 00:51:07] Okay, good.
[00:51:29 - 00:51:30] Cheers.

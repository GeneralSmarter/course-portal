# ENMT301-26W Lecture 62 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `f1e353f5c4f16ba9961b26cd6efc99b7910bdf1cf81f6f0401788c0a5165e3f0`
Generated: 2026-06-06T07:20:48.718257+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:00 - 00:00:07] Okay, with that we can get started, the name of the reference refresh.
[00:00:07 - 00:00:13] Okay, so we'll just start off with a little comparison of finite versus infinite impulse
[00:00:13 - 00:00:21] response filters, so the key things are in the consider and then we're going to look at
[00:00:21 - 00:00:26] sampling and the discrete Fourier transformers our next set of all lecture slides.
[00:00:27 - 00:00:31] Okay, so we've got four key categories for these two different types of filters and we'll
[00:00:31 - 00:00:34] sort of compare and contrast.
[00:00:34 - 00:00:40] Then for, so you can make a choice about how you're going to design your filter for your robot
[00:00:40 - 00:00:42] if you need to use one.
[00:00:42 - 00:00:51] Okay, so let's start off thinking about the amount of computation we need, that means
[00:00:51 - 00:00:55] a number of multiplies, the number of additions we need inside the filter.
[00:00:55 - 00:01:07] So what do you think is going to be more intense if I are, or they IRR?
[00:01:07 - 00:01:13] So normally the IRR has more filter coefficients, so you think of moving average if you're
[00:01:13 - 00:01:19] averaging over 25 samples to create a low pass filter, you're going to have 25 samples
[00:01:19 - 00:01:22] that you have to multiply by a coefficient and add together.
[00:01:22 - 00:01:29] So whereas the IRR, the recursive low pass filter we looked at just have one feed-forward
[00:01:29 - 00:01:34] coefficient and one feedback coefficient to reduce the low pass filter.
[00:01:34 - 00:01:45] So in terms of computation, the FIR filter is going to be high and the IRR filter will be low.
[00:01:45 - 00:01:57] And so this is high because we have more coefficients to generate the same type of filter.
[00:01:57 - 00:02:08] So the computation here is times and add inside the filter.
[00:02:08 - 00:02:18] Okay, so then memory is very similar.
[00:02:18 - 00:02:28] So the finite impulse response filter because we've got more coefficients, the memory of requirements are going to be higher on an FIR to
[00:02:28 - 00:02:37] again, it's higher because we've got more coefficients than for an IRR filter and low for the IR filter.
[00:02:37 - 00:02:47] So the IR filter, we look at low pass filter, we just had one feed-forward and one feed-back coefficient, so we just need two bytes of memory essentially.
[00:02:47 - 00:03:00] Whereas if we're doing a moving average over say 100 samples, we then need 100 coefficients stored in memory.
[00:03:00 - 00:03:09] Okay, what can we say about the stability of our finite impulse response filters?
[00:03:09 - 00:03:11] Always stable, yep, good.
[00:03:11 - 00:03:18] We're stable and infinite impulse response filters.
[00:03:18 - 00:03:22] Yeah, the can go unstable.
[00:03:22 - 00:03:29] So can be unstable.
[00:03:29 - 00:03:35] I can use today we were looking at the phase response of the filters.
[00:03:35 - 00:03:45] So remember, if we have a linear phase of our filter that corresponds to a constant time delay for all frequencies.
[00:03:45 - 00:03:51] So what can we say about the phase response of finite impulse response filters?
[00:03:51 - 00:04:01] Linear, as is a caveat, says linear if our impulse response H of n is symmetric.
[00:04:01 - 00:04:06] H of n is our impulse response.
[00:04:06 - 00:04:15] Whereas our infinite impulse response filter, these will be nonlinear.
[00:04:15 - 00:04:19] Okay, so then I can generate some form of distortion.
[00:04:19 - 00:04:24] Some frequencies are going to be delay, but more than other frequencies.
[00:04:24 - 00:04:34] And so overall waveform shape will change as it goes through the filter.
[00:04:34 - 00:04:40] Okay, so that is this part of the lesson on digital filters.
[00:04:40 - 00:04:43] And then so carrying on from that, we're still on digital space.
[00:04:43 - 00:04:48] We're looking at the sampling process and then the discrete Fourier transform.
[00:04:48 - 00:04:51] So I'll just shut this down, keep.
[00:04:51 - 00:05:25] Okay, so we're looking at sampling and discrete Fourier transforms.
[00:05:25 - 00:05:34] So our continuous signal, so voltage in the circuit.
[00:05:34 - 00:05:40] And then if we want to get actually microcontroller to do some processing of that sense of signal,
[00:05:40 - 00:05:44] we need to put for an analog to digital converter.
[00:05:44 - 00:05:50] And then we will have a digital signal.
[00:05:50 - 00:05:56] So we need to consider how fast or how often we sample that signal,
[00:05:56 - 00:06:02] which is a function of the frequencies present in that signal.
[00:06:02 - 00:06:07] So if we don't sample fast enough, we're going to end up with aliasing.
[00:06:07 - 00:06:11] And so these two figures I've put on the title slide here,
[00:06:11 - 00:06:15] which are aliasing in the time domain and the frequency domain.
[00:06:15 - 00:06:19] You've probably seen aliasing before in 303.
[00:06:19 - 00:06:26] Anyway, we'll go through more detail to explain what these slides are showing in more detail later.
[00:06:26 - 00:06:34] Okay, so let's just start off with the,
[00:06:34 - 00:06:36] I'll go back and set.
[00:06:36 - 00:06:44] Our overall process that we're thinking about here is we've got some continuous signal,
[00:06:44 - 00:06:46] X of t.
[00:06:46 - 00:06:53] We're going to sample it to get our sample signal x of n with square brackets.
[00:06:53 - 00:06:56] And here we're also going to discrete Fourier transforms.
[00:06:56 - 00:07:02] So we're going to take our Fourier transform.
[00:07:02 - 00:07:08] And so because x of n is discrete, the discrete Fourier transform will then give us
[00:07:08 - 00:07:11] a spectrum, capital X of k.
[00:07:11 - 00:07:13] And that's got square brackets as well.
[00:07:13 - 00:07:17] So that's also a discrete spectrum.
[00:07:17 - 00:07:20] So if x of n here were 100 samples,
[00:07:20 - 00:07:22] if we take the discrete Fourier transform,
[00:07:22 - 00:07:25] we get a spectrum which is also 100 samples.
[00:07:25 - 00:07:35] So both the signal and the spectrum with the DFT sample, that is discrete.
[00:07:35 - 00:07:43] Okay, and we'll go into the DFT in a much more detail in the next couple of lectures.
[00:07:43 - 00:07:45] Maybe three lectures.
[00:07:45 - 00:07:47] Okay, let's go.
[00:07:47 - 00:07:51] So let's start off with our definition of a continuous signal.
[00:07:51 - 00:07:54] So here we've got a cosine.
[00:07:54 - 00:08:00] So our continuous signal, X of t has some amplitude A.
[00:08:00 - 00:08:04] We're considering a cosine signal.
[00:08:04 - 00:08:09] And so it's got a characteristic frequency, if not, and it's a function of time t.
[00:08:09 - 00:08:16] Okay, so it's our continuous signal in our circuit.
[00:08:16 - 00:08:21] And we're now going to sample it at the sampling frequency Fs,
[00:08:21 - 00:08:25] which is one over the sampling period t.
[00:08:25 - 00:08:30] So capital T, I'm using for something period.
[00:08:30 - 00:08:35] And if underscore S is sampling frequency.
[00:08:35 - 00:08:46] Okay, so then we're in the discrete time.
[00:08:46 - 00:08:51] We're using square brackets.
[00:08:51 - 00:08:53] And n is our sample number.
[00:08:53 - 00:08:59] So x of n is equal to the value of our original signal X.
[00:08:59 - 00:09:05] Sample at n times the sampling period t,
[00:09:05 - 00:09:09] or in terms of our original cosine signal,
[00:09:09 - 00:09:14] A times the cosine of 2 pi, if not.
[00:09:14 - 00:09:24] And we replace t up here with the sample number in times the sampling period t.
[00:09:24 - 00:09:31] Okay, so that's the process of the sample within the analog to digital converter.
[00:09:31 - 00:09:35] So it's going from continuous time to discrete time.
[00:09:35 - 00:09:43] If we want to go back to the other way from back to continuous from the discrete,
[00:09:43 - 00:09:46] that requires the process of interpolation.
[00:09:46 - 00:09:49] And we'll talk about that later as well.
[00:09:49 - 00:09:59] Okay, so let's look at sampling a signal.
[00:09:59 - 00:10:02] So here, a cosine signal.
[00:10:02 - 00:10:11] So the blue one here is a continuous signal.
[00:10:11 - 00:10:16] So our x of t is equal to the amplitude as one.
[00:10:16 - 00:10:21] So it's cosine 2 pi.
[00:10:21 - 00:10:27] And we have a frequency of our cosine of 55 hertz.
[00:10:27 - 00:10:30] So 2 pi times 55 t.
[00:10:30 - 00:10:45] Okay, so our blue curve, our continuous cosine here has a frequency of 55 hertz.
[00:10:45 - 00:10:50] Okay, so it's obviously a cosine.
[00:10:50 - 00:10:52] But now we go to sample it.
[00:10:52 - 00:10:55] Say every so often we then take in the value.
[00:10:55 - 00:10:58] And those are given with the red dots.
[00:10:58 - 00:11:03] And I'll change my writing to here red.
[00:11:03 - 00:11:11] So our sampling frequency here is 50 hertz.
[00:11:11 - 00:11:16] So that means our sampling period capital T is 1 over our sampling frequency fs.
[00:11:16 - 00:11:21] So 1 over 50 is 0.02 seconds.
[00:11:21 - 00:11:35] So every 0.02 seconds we are sampling our 55 hertz blue cosine wave.
[00:11:35 - 00:11:41] And so then if you've got those red dots, when you look at it,
[00:11:41 - 00:11:45] you're eye joins them up to see what frequency,
[00:11:45 - 00:11:48] which is the dotted orange curve.
[00:11:48 - 00:11:50] Five hertz, yes.
[00:11:50 - 00:11:54] So this is what we call A using.
[00:11:54 - 00:12:04] So A using is when you've got one thing impersonating another.
[00:12:04 - 00:12:09] So if you're using a false name, your A-yes, you're impersonating someone else.
[00:12:09 - 00:12:21] Here we've got a five hertz waveform impersonating a 55 hertz waveform.
[00:12:21 - 00:12:53] So what we think we have, our sample signal x of n is here cosine 2 pi times 5 in t.
[00:12:53 - 00:12:59] So we think we've got a five hertz cosine.
[00:12:59 - 00:13:06] We should have a 55 hertz cosine.
[00:13:06 - 00:13:12] So we haven't sampled that cosine fast enough.
[00:13:12 - 00:13:20] We need more red dots so that our sample signal looks like a 55 hertz cosine.
[00:13:20 - 00:13:30] So how many red dots do we need for each cosine?
[00:13:30 - 00:13:33] So that it's not A-yes.
[00:13:33 - 00:13:37] So for one period of the cosine, we need two.
[00:13:37 - 00:13:41] So this is the Nyquist sampling criterion.
[00:13:41 - 00:13:48] We have to have two red dots for each period of the cosine.
[00:13:48 - 00:13:56] So we have the sample at twice the maximum frequency of our signal.
[00:13:56 - 00:14:04] So in this case, what frequency should we sample the cosine to make sure that we don't get A using?
[00:14:04 - 00:14:10] At least I'm hunting it.
[00:14:10 - 00:14:13] So greater than or equal to 110 hertz.
[00:14:13 - 00:14:15] So I'll write that down on the next slide.
[00:14:15 - 00:14:23] Okay.
[00:14:23 - 00:14:31] So there's a visual description of the aliasing problem in the time domain.
[00:14:31 - 00:14:38] We'll look at the frequency domain later.
[00:14:38 - 00:14:39] Okay.
[00:14:39 - 00:14:51] So what I just said, wave my arms round in the previous slide is now written down as the Nyquist Shannon theorem.
[00:14:51 - 00:14:55] So a band limited.
[00:14:55 - 00:15:05] So that means the frequency content in the signal is between two frequencies that doesn't go forever.
[00:15:05 - 00:15:10] The bandwidth and continuous time signal can be perfectly reconstructed from examples.
[00:15:10 - 00:15:16] If the sampling frequency is greater than twice the highest frequency present in the signal.
[00:15:16 - 00:15:32] So that means we want our sampling frequency to be greater than or equal to two times our maximum frequency component.
[00:15:32 - 00:15:43] So on the previous example, we had one frequency component.
[00:15:43 - 00:15:47] So we had the 55 hertz cosine.
[00:15:47 - 00:15:50] So the f max was 55 hertz.
[00:15:50 - 00:15:59] So our sampling frequency should be greater than or equal to two times 55.
[00:15:59 - 00:16:22] So if it should be greater than or equal to 110 hertz.
[00:16:22 - 00:16:23] Okay.
[00:16:23 - 00:16:28] So now we'll go and look at what A using means in the frequency domain.
[00:16:28 - 00:16:31] So that was the time domain.
[00:16:31 - 00:16:40] So the first we'll just step back a bit and we'll just redefine the Fourier transform and the discrete time Fourier transform.
[00:16:40 - 00:16:42] And look at how that related.
[00:16:42 - 00:16:51] So our Fourier transform gives us the spectrum x of f, which is continuous.
[00:16:51 - 00:17:05] So we integral from minus infinity to infinity of our signal x of t times the complex exponential e to the minus j 2 by ft dt.
[00:17:05 - 00:17:16] So x of t here is continuous and that gives us a continuous spectrum capital x of f.
[00:17:16 - 00:17:17] Okay.
[00:17:17 - 00:17:22] And we looked at last week the discrete time Fourier transform.
[00:17:22 - 00:17:34] This is giving us a spectrum x of f, which is continuous that is periodic with period t.
[00:17:34 - 00:17:38] Well, one over t in the frequency domain.
[00:17:38 - 00:17:41] So this is sampled with a period t.
[00:17:41 - 00:17:52] And so this discrete time Fourier transform.
[00:17:52 - 00:17:57] We have a discrete signal x of n.
[00:17:57 - 00:18:05] And our complex exponential is e to the minus j 2 pi f.
[00:18:05 - 00:18:11] And we replace t of the continuous Fourier transform within capital t and something period.
[00:18:11 - 00:18:20] And because x of n is discrete, we have a sum rather than integral from n as minus infinity to infinity.
[00:18:20 - 00:18:25] Okay.
[00:18:25 - 00:18:29] And so then some maths, which we're not going to go through.
[00:18:29 - 00:18:36] But it sort of hinted at last week when we saw that the discrete time Fourier transform is periodic.
[00:18:36 - 00:18:50] We have our discrete time Fourier transform x subscript 1 over t of f is equal to 1 over something period t.
[00:18:50 - 00:19:09] So the sum from n is minus infinity to infinity of our continuous spectrum f of f minus m our counter here divided by the sum of period t.
[00:19:09 - 00:19:16] So what that means for our, for the discrete signal.
[00:19:16 - 00:19:19] And we take the discrete time Fourier transform of that.
[00:19:19 - 00:19:28] We have then our spectrum of the signal.
[00:19:28 - 00:19:34] And it gets repeated in the frequency space.
[00:19:34 - 00:19:37] Okay. So we've got all these copies of the spectrum.
[00:19:37 - 00:19:48] And they are spaced by our sampling frequency fs.
[00:19:48 - 00:19:51] Okay. So I'll just skip for a couple of slides.
[00:19:51 - 00:19:59] So if we look at the second figure, the curve in blue here is our x of f.
[00:19:59 - 00:20:07] And then all the dotted ones with other colors are then the copies of the spectrum.
[00:20:07 - 00:20:21] Okay. I'll go back and try and explain this repetition of the spectrum of the signals.
[00:20:21 - 00:20:23] The periodic.
[00:20:23 - 00:20:28] Another way using direct delta functions.
[00:20:28 - 00:20:48] Okay. So we can describe sampling of function as multiplying the function by delta functions that are spaced capital t, the sampling period apart.
[00:20:48 - 00:20:59] Okay. And all these delta functions in a row sort of periodically are known as a direct comb.
[00:20:59 - 00:21:02] So this thing looks like a comb.
[00:21:02 - 00:21:09] And that can be written as delta subscript t.
[00:21:09 - 00:21:15] So that's, they're repeating with period t as a function of time little t.
[00:21:15 - 00:21:17] So we have this infinite sum.
[00:21:17 - 00:21:31] So from n is minus infinity to infinity of these delta functions that are separated or spaced our sampling period capital t apart.
[00:21:31 - 00:21:43] So something in the time lane, we're going to multiply by that direct comb.
[00:21:43 - 00:21:55] Okay. If we consider what happens in the frequency domain and very curiously, the Fourier transform of a direct comb,
[00:21:55 - 00:21:58] is actually another direct comb.
[00:21:58 - 00:22:03] And the math of that is also complicated.
[00:22:03 - 00:22:10] You can prove that with looking at the Fourier series of them, but we're not going to do that because this isn't a math course.
[00:22:10 - 00:22:26] And so the Fourier transform then of our direct comb in the time domain is a direct comb,
[00:22:26 - 00:22:34] which is separated one over t or something frequency apart in the frequency domain.
[00:22:34 - 00:22:55] And then this is one over t sum from m minus infinity to infinity of our deltas and the deltas are now separated by one over t.
[00:22:55 - 00:23:20] Okay. So if we're modeling sampling in the time domain as multiplying by this direct comb,
[00:23:20 - 00:23:36] then in the frequency domain, we are convolving the spectrum of our signal with this other direct comb with deltas are separated by the sampling frequency apart.
[00:23:36 - 00:23:58] Okay. So if we draw that here, so we are going to consider here some signal g of t, this red curve here.
[00:23:58 - 00:24:15] So in the time domain, we have our g of t is multiplied by our delta train, which is separated by capital T and something period apart.
[00:24:15 - 00:24:29] And that then gives us our g of n. Okay.
[00:24:29 - 00:24:37] So then in the frequency domain, let's say our signal here is band limited.
[00:24:37 - 00:24:41] So all the frequencies are between zero and B.
[00:24:41 - 00:25:00] So then in the frequency domain, we are then convolving g of f with a direct comb with a separated one over t or the sampling frequency apart.
[00:25:00 - 00:25:12] And so we get then one over t sum is over m.
[00:25:12 - 00:25:22] And then we get the spectra or the spectrum repeated every capital T apart.
[00:25:22 - 00:25:35] So when we do this convolution, we're convolving this spectrum that I'll draw on a triangle here with the delta functions.
[00:25:35 - 00:25:56] When we do this convolution, we end up with the spectrum repeating and each version of the spectrum is centered on multiple for integer values of the sampling frequency.
[00:25:56 - 00:26:05] So the sampling process inherently means that our frequency spectrum becomes periodic.
[00:26:05 - 00:26:10] And this is going to cause us problems.
[00:26:10 - 00:26:26] So I'm using chicken and beans.
[00:26:26 - 00:26:28] So let's stop.
[00:26:28 - 00:26:29] Okay.
[00:26:29 - 00:26:33] So then let's come back to this slide.
[00:26:33 - 00:26:38] So here, let's look at the spectra.
[00:26:38 - 00:26:45] So on the top, this is the amplitude of magnitude of our spectrum x of f.
[00:26:45 - 00:26:58] So this is the Fourier transform of continuous and limited.
[00:26:58 - 00:27:09] So here, let me say limited between zero and f max.
[00:27:09 - 00:27:10] Okay.
[00:27:10 - 00:27:14] So if we've got a continuous signal, we use the Fourier transform on it.
[00:27:14 - 00:27:17] We just have one spectrum.
[00:27:17 - 00:27:18] It's not repeating.
[00:27:18 - 00:27:23] Okay.
[00:27:23 - 00:27:31] And then the following three are all for the discrete time Fourier transform.
[00:27:31 - 00:27:34] So with sample, our signal.
[00:27:34 - 00:27:37] And then take the discrete time Fourier transform.
[00:27:37 - 00:27:40] Okay.
[00:27:40 - 00:27:45] So the second one down, this is where we are Nyquist sampled.
[00:27:45 - 00:27:52] So exactly, Nyquist sampled here.
[00:27:52 - 00:27:59] So if s is two times the maximum frequency components.
[00:27:59 - 00:28:02] And then we've got no overlap.
[00:28:02 - 00:28:03] Okay.
[00:28:03 - 00:28:09] So here, the blue curve goes to zero before the first copy,
[00:28:09 - 00:28:14] the orange one is non-zero.
[00:28:14 - 00:28:19] Okay.
[00:28:19 - 00:28:24] So if we're perfectly Nyquist sampled our spectral images or copies,
[00:28:24 - 00:28:27] don't overlap in the Fourier domain.
[00:28:27 - 00:28:36] Okay.
[00:28:36 - 00:28:39] And the second one here, sorry, the third one down,
[00:28:39 - 00:28:45] we are now, it's a discrete time Fourier transform.
[00:28:45 - 00:28:58] So this is each of these is the magnitude of the x1 over t of f.
[00:28:58 - 00:29:02] So this is the magnitude of x period.
[00:29:02 - 00:29:05] Well, sampled with period t.
[00:29:05 - 00:29:13] And so this one here, the third one is when we were over sampled.
[00:29:13 - 00:29:21] And so our sampling frequency, if we're over sampled,
[00:29:21 - 00:29:29] f s is greater than two times our maximum frequency component.
[00:29:29 - 00:29:30] Okay.
[00:29:30 - 00:29:33] And the last one, again, we've got the discrete time Fourier transform.
[00:29:33 - 00:29:39] This one, we're under sampled such that our sampling frequency,
[00:29:39 - 00:29:44] f s is less than twice the maximum frequency component.
[00:29:44 - 00:29:50] And here we have then overlaps.
[00:29:50 - 00:29:53] Okay.
[00:29:53 - 00:29:58] So these overlaps are what causes a thing.
[00:29:58 - 00:30:07] If you think about what's happening to the frequencies inside that circle,
[00:30:07 - 00:30:13] the blue curve has been added to the orange curve.
[00:30:13 - 00:30:19] So it's changing those frequency spectrum values.
[00:30:19 - 00:30:22] Okay.
[00:30:22 - 00:30:27] So if we Nyquist sampled or over sampled,
[00:30:27 - 00:30:36] we can put a low pass filter and remove those spectral copies.
[00:30:36 - 00:30:41] We can get rid of, so if the low pass filter is defined by those dotted lines,
[00:30:41 - 00:30:44] we can get rid of the orange red repeating spectra.
[00:30:44 - 00:30:50] Just by letting the low frequencies pass filter out the higher frequencies.
[00:30:50 - 00:30:51] That's fine.
[00:30:51 - 00:30:58] I think about what happens if we try and put a low pass filter in the bottom case
[00:30:58 - 00:31:05] when we're under sampled, we're either going to end up keeping some of the orange curve
[00:31:05 - 00:31:08] and or throwing away some of the blue curve.
[00:31:08 - 00:31:09] Okay.
[00:31:09 - 00:31:13] So there's no way to have a filter, even a perfect brick wall filter,
[00:31:13 - 00:31:19] which we can't even realize anyway, to make sure we just get the central spectrum
[00:31:19 - 00:31:29] of the blue one and throw away these spectral copies that we've generated
[00:31:29 - 00:31:37] through the sampling process.
[00:31:37 - 00:31:38] Okay.
[00:31:38 - 00:31:42] So that's the looking A thing from both the time domain and the frequency domain.
[00:31:42 - 00:31:51] I'll show you something now, A thing with a two dimensional signal.
[00:31:51 - 00:31:52] So an image.
[00:31:52 - 00:31:55] Okay.
[00:31:55 - 00:31:58] So this is a brick wall.
[00:31:58 - 00:32:02] Image on the left is where we are.
[00:32:02 - 00:32:03] So this is a photo.
[00:32:03 - 00:32:08] So it's made up of pixels, which are our sample points.
[00:32:08 - 00:32:16] So the one on the left we are over sampled.
[00:32:16 - 00:32:23] If we down sample by throwing away some of the pixels in the image on the left,
[00:32:23 - 00:32:36] eventually we get a smaller image where we are then under sampled.
[00:32:36 - 00:32:39] We've got two few pixels.
[00:32:39 - 00:32:52] So here in a two dimensional signal, our sample rate is the number of pixels per meter.
[00:32:52 - 00:33:02] So if we don't have enough pixels, we're then not going to be able to capture,
[00:33:02 - 00:33:04] or we're going to let in high frequencies.
[00:33:04 - 00:33:12] And so you can see the bottom right of the image here, A listing.
[00:33:12 - 00:33:13] Okay.
[00:33:13 - 00:33:17] So this is by down sampling the image, by not.
[00:33:17 - 00:33:21] And this is sampling the image in a high enough frequency
[00:33:21 - 00:33:25] with introduced new frequency content to our image.
[00:33:25 - 00:33:29] Which is kind of this ripple.
[00:33:29 - 00:33:33] Looks like there's a wave running up the building.
[00:33:33 - 00:33:38] So that is A listing.
[00:33:38 - 00:33:44] And this particular form of A listing is known as a mooray pattern.
[00:33:44 - 00:34:09] pattern. Okay, so one of the ways we can deal with A using, is to use an anti-A using filter.
[00:34:09 - 00:34:17] So this is an analog filter before the analog to digital converter. So you put your, say,
[00:34:17 - 00:34:25] your voltage in your circuit, then needs to through an analog filter. So it's a resistor
[00:34:25 - 00:34:31] capacitor. Why have you? To try and remove some of the high frequencies. So you don't
[00:34:31 - 00:34:40] aim this and those down into the lower frequencies. Okay, so the input to the A to C is low
[00:34:40 - 00:34:51] pass filtered. So we've got some continuous signal, X of T, going into our anti-A use filter,
[00:34:51 - 00:35:00] which is the low pass filter. We get Y of T and then it goes into the analog to digital converter.
[00:35:00 - 00:35:15] And after that we have our discrete time signal Y of N. So this anti-A use filter would ideally be a brick wall filter.
[00:35:15 - 00:35:33] So we would then have, this is the magnitude of our filter, H of F. This is one. And so this is
[00:35:33 - 00:35:51] frequency axis here. So watch it our cutoff frequency B for our anti-A use filter. Half of something frequency, yes.
[00:35:51 - 00:36:02] Okay, so it's just the Nyquist criterion. But what happens in reality you can't build this brick wall filter.
[00:36:02 - 00:36:15] And so what we have in reality is that we have some finite roll-off of our low pass filter. It's not perfect.
[00:36:15 - 00:36:36] So there's always going to be some A using. No matter. You get a higher and higher orders of your filter.
[00:36:36 - 00:36:51] There's always going to be some higher frequencies. So these ones here above F C, I'm still going to pass through to the ADC.
[00:36:51 - 00:37:13] And so those are then going to be A is down into the lower frequencies. Okay, so one way to deal with the A is the heavy anti-A using filter to get rid of most of the high frequency content in the signal.
[00:37:13 - 00:37:27] The other one is to then do over sampling. So we're not going at just two times the sampling rate.
[00:37:27 - 00:37:43] We would go at a much greater rate. Okay, so I forgot I also had this slide here. So this is showing the frequency spectrum of a real anti-A using filter.
[00:37:43 - 00:38:13] So this is a second order filter. Okay, so the one in blue is the central one and the dotted ones are the images.
[00:38:13 - 00:38:26] And so with this real filter we have here A is things. This is our cutoff frequency here. If it's on two.
[00:38:26 - 00:38:35] And it becomes more apparent when you look at it on a log scale. So two, three, four.
[00:38:35 - 00:38:53] So if we consider, well, let's go here. So these frequencies here. The orange curve is not quite at the blue curve.
[00:38:53 - 00:38:59] But what we're getting is then, and this frequency we get in the orange curve plus the green curve plus the red curve.
[00:38:59 - 00:39:15] And those are all summing up. So the edge of the band we are getting the spectral copies adding frequency content is not in the original signal into our original signal.
[00:39:15 - 00:39:37] And that's causing the aliasing. So this here, and here is the aliasing. Okay, so the anti-A listening filter is not going to be perfect.
[00:39:37 - 00:39:55] So another way to make sure that we reduce the amount of aliasing is to oversample by more than this micro-screen tier-in of two times.
[00:39:55 - 00:40:07] So in practice, rule of thumb is that we go something frequency of greater than 10 times the maximum frequency.
[00:40:07 - 00:40:22] Not just two times. Okay, so for these anti-aliasing filters, point number one there, we get a sharper roll off if we increase the order of the filter.
[00:40:22 - 00:40:36] As we look at previously, so first order filter rolls off at 20 dismills per decade, second order 40, third order 60. So you increase the order to reduce the amount of aliasing.
[00:40:36 - 00:41:00] or we can do this over sampling. Okay, and thin, you've probably looked at this in 303. If you're in a control system and you're sampling and you're controlling at the same time, you probably want to go even higher rate, higher than 10 times the maximum frequency.
[00:41:00 - 00:41:36] So we reduce the amount of latency or servo lag in the system. So in this case, our rule of thumb is that sampling frequency should be greater than 20 times maximum frequency.
[00:41:36 - 00:41:55] Okay, the next topic we need to talk about is once we have our digital signal, if we want to go back and get our continuous signal, we need to go through the process of reconstruction.
[00:41:55 - 00:42:10] So we're reconstructing the continuous signal from the discrete time signal. So if I just show you the process of this, so we've got our, the discrete time signal wave in and our microcontroller.
[00:42:10 - 00:42:41] And so then we're going to go through a digital to analog converter. And then after the digital analog converter, we need a reconstruction filter.
[00:42:41 - 00:43:22] Okay, this reconstruction filter is also an analog filter. Okay, so this reconstruction filter to get us a continuous signal back from our digital signal is this low pass filter here that just keeps the central spectrum and those repeated copies, the dotted purple green orange and red.
[00:43:22 - 00:44:10] So, the next one is the next one. So, we're removing the repeated spectrum. Okay, so that means in our system, we need two different analog filters.
[00:44:10 - 00:44:29] So, we're going to be answering the aliasing filter before we go into the digital domain and then a reconstruction filter from going from the digital domain back to the analog domain.
[00:44:29 - 00:44:41] Okay, so for this reconstruction filter, so it's an analog filter. The low pass filter, you'd build it, say, resistors and capacitors.
[00:44:41 - 00:44:56] And ideally, we would have a brick wall filter. And so the perfect filter, this ideal filter is a brick wall filter which is a red function for a transform of rectifier sink.
[00:44:57 - 00:45:17] So, this reconstruction filter is equivalent to sink interpolation. So that means to get our continuous signal Y of t back from our samples Y of n.
[00:45:17 - 00:45:56] So, we are convolving Y of n with a sink function. Okay, so this means that if our signal is Nyquist signal, Nyquist sample, we can get our signal back perfectly by doing a sink interpolation.
[00:45:56 - 00:46:15] In reality, we can't build a perfect brick wall filter, so we can't perfectly do the sink interpolation. Okay, so we want to, because we can't build a perfect reconstruction filter, we want to then over sample our signals.
[00:46:15 - 00:46:35] So, we're not going just two times the next one in the frequency, something frequency, we go at a much greater rate. Okay, so let's look at an example of a reconstruction.
[00:46:35 - 00:47:06] So, the blotted, the dotted blue curve here is a sine signal of 5 hertz. And our sampling frequency here is, we've got four samples for each curve and we've got 5 curves.
[00:47:06 - 00:47:25] So, the sampling frequency here is 20 hertz, 20 and 1 second. So, we're oversoupled. Okay, so our orange dots here are our samples from sampling the blue curve.
[00:47:25 - 00:47:26] In Python, I've gone through and I've convolved those sample points with a sink function to get back the original signal. Okay, so in the middle here, this sink convolution, so convolving these orange points with the sink gives us a pretty good estimate of our
[00:47:58 - 00:48:33] original signal, the blotted blue lines. But at the edges here and here, these aren't perfect. Okay, and so the reason by my reconstruction in Python here wasn't perfect was this convolution is an infinite sum from n is minus infinity to infinity.
[00:48:33 - 00:49:07] So, yeah, I've just used in as 20. So, I've just done within 20 values of 20 sink functions rather than the infinite that would give us a perfect reconstruction of the original signal. Okay, I think that's a good point to in today.
[00:49:07 - 00:49:18] And tomorrow we'll get on to the discrete Fourier transform. I hope you'll see some of you in the tutorial over back in engineering.
[00:49:18 - 00:49:23] The question is up online and I'll be there by three.
[00:49:58 - 00:50:24] Thank you.
[00:50:24 - 00:51:05] Thanks.

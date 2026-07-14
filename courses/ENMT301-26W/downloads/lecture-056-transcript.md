# ENMT301-26W Lecture 56 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_56_audio_16k_mono_32k.mp3`
Source audio SHA-256: `050c0abfa198cd8c1843a7fee7b25cdbf4fa2644589d11bd94e143372c95d30e`
Generated: 2026-06-06T07:07:54.261528+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:06 - 00:00:09] Okay, good afternoon everyone.
[00:00:09 - 00:00:12] So, we'll carry on with our digital filters today,
[00:00:12 - 00:00:15] or mind that there's a tutorial straight off to this
[00:00:15 - 00:00:16] over in the drawing office.
[00:00:17 - 00:00:21] So, the basic idea is instead of building a filter
[00:00:21 - 00:00:22] to remove some of our noise,
[00:00:22 - 00:00:24] our resistors, capacitors and ductors,
[00:00:24 - 00:00:27] as an analog filter, we can design
[00:00:27 - 00:00:30] and software our digital filter on our microcontroller.
[00:00:31 - 00:00:33] So, that's good to us.
[00:00:33 - 00:00:38] More control about changing things and software relevant.
[00:00:38 - 00:00:40] And hardware makes it more precise
[00:00:40 - 00:00:44] because we are not susceptible to tolerances
[00:00:44 - 00:00:47] and things changing with time.
[00:00:48 - 00:00:53] So, in the screen time, we use the z-transform
[00:00:53 - 00:00:54] to analyze our filters.
[00:00:54 - 00:00:57] So, this is equivalent to the Laplace transform.
[00:00:57 - 00:01:02] And you can go from the Laplace transform,
[00:01:03 - 00:01:05] which has this complex variable S,
[00:01:05 - 00:01:09] to the z-transform which has this variable z,
[00:01:09 - 00:01:14] by making the substitution that z is equal to e to the st.
[00:01:14 - 00:01:17] When capital T here is our sampling period,
[00:01:17 - 00:01:22] so how often in time we create our digital samples.
[00:01:22 - 00:01:25] And when we get to that substitution,
[00:01:25 - 00:01:30] we end up with this definition for the z-transform.
[00:01:30 - 00:01:35] So, our transfer function H of z is the discrete sum
[00:01:36 - 00:01:41] of our impulse response times z to the minus n.
[00:01:44 - 00:01:47] Okay, so the impulse response here is the discrete
[00:01:47 - 00:01:55] and the transfer function H of z is continuous.
[00:01:55 - 00:01:58] Okay, so the impulse response and transfer function
[00:01:58 - 00:02:03] here are a z-transform here.
[00:02:03 - 00:02:06] Okay, so we did some properties of the z-transform
[00:02:06 - 00:02:08] in this today.
[00:02:09 - 00:02:14] And so the key three ones are z-transform's linear.
[00:02:14 - 00:02:16] So if we scale a signal by a constant,
[00:02:16 - 00:02:20] then the z-transform also gets scaled by the same constant.
[00:02:21 - 00:02:24] And if we sum two signals together,
[00:02:24 - 00:02:26] and take the z-transform, that's the same
[00:02:26 - 00:02:30] as taking the z-transform of the two signals,
[00:02:30 - 00:02:33] and then adding the z-transform together.
[00:02:35 - 00:02:36] We have this convolution operator
[00:02:39 - 00:02:41] or convolution theorem,
[00:02:41 - 00:02:44] probably of the z-transform is the same as in Laplace
[00:02:44 - 00:02:46] or Fourier transform,
[00:02:46 - 00:02:48] that if we have a convolution at one domain,
[00:02:48 - 00:02:50] that's equivalent from multiplication
[00:02:50 - 00:02:51] in the other domain.
[00:02:53 - 00:02:56] And then the most important one for the z-transform
[00:02:56 - 00:03:01] is if we have a shift or a delay of m samples
[00:03:02 - 00:03:04] of our signal and the time domain,
[00:03:04 - 00:03:07] then that becomes a z to the minus m
[00:03:07 - 00:03:13] in our z-transform.
[00:03:13 - 00:03:15] Okay, so those are three properties.
[00:03:15 - 00:03:18] And then I'm also gonna go through
[00:03:18 - 00:03:22] the three most important z-transform pairs.
[00:03:23 - 00:03:25] So in the first one, in the yesterday,
[00:03:25 - 00:03:29] where the z-transform of the unit impulse,
[00:03:29 - 00:03:31] so that's just a one at time,
[00:03:32 - 00:03:35] or at sample, either zero,
[00:03:36 - 00:03:41] that goes to a z-transform of one.
[00:03:43 - 00:03:45] So this is very similar to the Fourier transform,
[00:03:45 - 00:03:51] where a delta function is the Fourier pair of a constant.
[00:03:51 - 00:03:52] Okay, so as you know, impulse,
[00:03:52 - 00:03:56] and now we'll do the unit step,
[00:03:56 - 00:04:00] so we have, for the unit step,
[00:04:00 - 00:04:05] we have here u of n equal one.
[00:04:07 - 00:04:10] So this is for n greater than or equal to zero,
[00:04:11 - 00:04:17] and u of n is equal to zero for n less than zero.
[00:04:17 - 00:04:22] Okay, so it's like flicking on a switch at time,
[00:04:22 - 00:04:29] t is zero, which corresponds to sample n is zero.
[00:04:29 - 00:04:32] So then the definition of the z-transform,
[00:04:33 - 00:04:38] h of z is then the sum from little n, zero,
[00:04:40 - 00:04:44] to infinity, we're substituting in our signal,
[00:04:45 - 00:04:51] u of n, and then we're multiplying by z to the minus n.
[00:04:51 - 00:04:56] Okay, so u of n is one, so all these ones,
[00:04:56 - 00:05:00] span greater than or equal to zero,
[00:05:00 - 00:05:02] and it's zero, otherwise.
[00:05:02 - 00:05:04] So this sum simplifies a little bit,
[00:05:04 - 00:05:07] sort of then go from n to zero to infinity,
[00:05:07 - 00:05:12] u of n is one, so it's sum from n to zero,
[00:05:12 - 00:05:17] to infinity z to the minus n.
[00:05:17 - 00:05:20] And so we can write this out as then,
[00:05:20 - 00:05:25] if we expand this out, when n is zero,
[00:05:25 - 00:05:30] we have zero to the power of z to the power of zero is one,
[00:05:30 - 00:05:34] plus then z to the minus one, plus z to the minus two,
[00:05:34 - 00:05:40] plus dot dot dot.
[00:05:40 - 00:05:47] Okay, so how do we add up those terms?
[00:05:47 - 00:05:55] What does that look like?
[00:05:55 - 00:05:59] I'll take your hand waving as a geometric series.
[00:05:59 - 00:06:03] So we've got here, so this is a geometric series.
[00:06:03 - 00:06:07] Each one of these, the next value in the sequence
[00:06:07 - 00:06:10] is multiplied by z to the minus one.
[00:06:10 - 00:06:18] So if we do a sum of a geometric series,
[00:06:18 - 00:06:23] we then have, so the ratio here is z to the minus one.
[00:06:24 - 00:06:30] This becomes then one over one minus z to the minus one.
[00:06:30 - 00:06:35] So then we have our unit step in our sample time domain.
[00:06:36 - 00:06:40] So sample time domain is part of a z transform pair
[00:06:40 - 00:06:44] with one over one minus z to the minus one.
[00:06:44 - 00:07:03] Yes, yes.
[00:07:03 - 00:07:10] Yes, so these ends are sampled here, T apart.
[00:07:11 - 00:07:12] So this is always gonna be,
[00:07:12 - 00:07:14] if you convert back to real time,
[00:07:14 - 00:07:19] continuous time, a fraction of the sample period.
[00:07:19 - 00:07:21] So just draw this on here.
[00:07:21 - 00:07:30] This is capital T apart in time.
[00:07:30 - 00:07:35] Okay, so the one we'll look at is exponentials.
[00:07:38 - 00:07:43] So we have here for our X of n
[00:07:48 - 00:07:52] is an exponential, so we've got some constant A
[00:07:52 - 00:07:56] to the power of n times our unit step function U of n.
[00:07:56 - 00:07:58] So we're starting at n is zero.
[00:07:59 - 00:08:06] So we're here multiplying by the unit step function.
[00:08:06 - 00:08:09] Okay, so we've got here in this graph,
[00:08:09 - 00:08:11] I've drawn, I've got A is point eight.
[00:08:13 - 00:08:17] Okay, so it's, our exponential is decaying.
[00:08:17 - 00:08:24] This is then a stable system.
[00:08:24 - 00:08:29] Okay, so to get our z transform of x of n,
[00:08:29 - 00:08:34] we do x of z is the sum from n is zero to infinity,
[00:08:35 - 00:08:39] A of n, U of n is our x of n, our signal,
[00:08:42 - 00:08:51] and then we're multiplying by the z to the minus n.
[00:08:51 - 00:08:52] Okay, we'll expand this out again.
[00:08:52 - 00:08:54] So our first term, when n is zero,
[00:08:54 - 00:08:56] we have z to the minus one.
[00:08:57 - 00:09:01] Second term, we've got A times z to the minus two,
[00:09:01 - 00:09:03] plus then A squared.
[00:09:06 - 00:09:08] Is that right?
[00:09:08 - 00:09:23] A, that should be A to the minus one.
[00:09:23 - 00:09:26] A z to the minus one, A squared z to the minus two,
[00:09:26 - 00:09:36] plus dot dot dot.
[00:09:36 - 00:09:38] Okay, so we can do the same trick as with the unit step.
[00:09:38 - 00:09:40] So we have H of z is equal to,
[00:09:42 - 00:09:49] so again, we're going to geometric series.
[00:09:49 - 00:09:50] So what's our ratio here?
[00:09:52 - 00:09:53] Or this?
[00:09:53 - 00:09:57] Yeah.
[00:09:57 - 00:10:01] I should be z to the zero,
[00:10:01 - 00:10:02] so that should just be one.
[00:10:02 - 00:10:03] I made a mess of this.
[00:10:03 - 00:10:12] Good spot.
[00:10:12 - 00:10:13] That's one, yeah.
[00:10:13 - 00:10:16] So, we're in the zero,
[00:10:16 - 00:10:19] A to zero is one, z to the zero is also one,
[00:10:19 - 00:10:24] so we get one.
[00:10:24 - 00:10:27] Then when n is one, we have A to the one,
[00:10:27 - 00:10:28] z to the minus one.
[00:10:28 - 00:10:29] Yeah.
[00:10:30 - 00:10:38] Okay, so what's our common ratio between terms here?
[00:10:38 - 00:10:41] Yep, A of z to the z transforms,
[00:10:41 - 00:10:45] we like to live in z to the minus one,
[00:10:45 - 00:10:48] just because that signifies a delay.
[00:10:49 - 00:10:54] Okay, so then our H of z for this exponential
[00:10:54 - 00:10:59] is then one over one minus A z to the minus one.
[00:11:07 - 00:11:09] And so this geometric series,
[00:11:09 - 00:11:14] some holds if the ratio is less than one.
[00:11:15 - 00:11:19] So this holds true then if the magnitude of z
[00:11:19 - 00:11:31] is less than the magnitude of A.
[00:11:31 - 00:11:35] Okay, so this here is an exponential,
[00:11:35 - 00:11:40] so it's gonna be, this is an infinite response
[00:11:40 - 00:11:45] to these dots, polypops, keep on going for all time.
[00:11:45 - 00:11:48] But decaying, but it's not the finite sequence.
[00:11:49 - 00:11:51] Okay, so those are the three,
[00:11:54 - 00:11:58] most common z transform pairs.
[00:11:58 - 00:11:59] The ones that we need to be aware of,
[00:11:59 - 00:12:01] the ones that are in the form of the sheet for the test.
[00:12:02 - 00:12:04] And so this one's got a single pole then,
[00:12:04 - 00:12:09] and there's an old data if z equals A,
[00:12:09 - 00:12:13] we're gonna get a zero on the denominator,
[00:12:13 - 00:12:23] so it's gonna give us a pole.
[00:12:23 - 00:12:27] Okay, so let's do some examples of taking some z transforms
[00:12:27 - 00:12:28] of some difference equations.
[00:12:30 - 00:12:32] So these are the two difference equations
[00:12:32 - 00:12:35] we look at yesterday for the two different types of filter.
[00:12:35 - 00:12:37] So this one is the moving average.
[00:12:38 - 00:12:43] So the output y of n is equal to half,
[00:12:43 - 00:12:48] the current input x of n plus half the previous input.
[00:12:48 - 00:12:50] So we're averaging over two consecutive ones
[00:12:50 - 00:12:52] that try and get rid of the noise.
[00:12:54 - 00:12:58] So that is a moving average or finite and pulse response
[00:12:58 - 00:13:01] filter.
[00:13:01 - 00:13:05] Okay, so let's take a z transform of this one then.
[00:13:05 - 00:13:10] So little y of n goes to capital Y of z.
[00:13:13 - 00:13:16] Okay, so the little letter is in our sample time name
[00:13:16 - 00:13:24] and the capital letter is in the z domain.
[00:13:24 - 00:13:33] What does 0.5 x of n go to?
[00:13:33 - 00:13:39] Capital x is it and what do we do at the 0.5?
[00:13:39 - 00:13:40] Yeah, exactly.
[00:13:40 - 00:13:43] So that's the linearity property.
[00:13:44 - 00:13:49] So if we multiply the signal by 0.5.
[00:13:51 - 00:13:54] So here now in domain, our sample time domain,
[00:13:54 - 00:13:58] then we multiply the z transform by 0.5 as well.
[00:13:59 - 00:14:02] So that's the same property in the class
[00:14:02 - 00:14:06] and Fourier transforms as well.
[00:14:06 - 00:14:11] Okay, get rid of that line.
[00:14:11 - 00:14:17] Yep, so just to rely on it.
[00:14:17 - 00:14:19] So the 0.5 is from linearity.
[00:14:19 - 00:14:24] And so then plus, so we know this 0.5 is going to 0.5.
[00:14:25 - 00:14:28] What do we do with x of n minus 1?
[00:14:28 - 00:14:41] What's the z transform of our input delay by one sample?
[00:14:41 - 00:14:45] So x of n goes to an x of z and what do we do
[00:14:45 - 00:14:50] with the delay by one sample?
[00:14:50 - 00:14:51] Z minus 1, yeah.
[00:14:51 - 00:14:54] So that's why these minus 1's are important
[00:14:54 - 00:14:59] because that's indicating that we're delaying by a sample.
[00:14:59 - 00:15:05] So z minus 2 is delaying by two samples, et cetera.
[00:15:05 - 00:15:09] Okay, so that's our moving average filter
[00:15:09 - 00:15:10] we looked at yesterday.
[00:15:11 - 00:15:17] And then this recursive filter, recursive filter
[00:15:17 - 00:15:19] that we also looked at yesterday,
[00:15:19 - 00:15:29] which is an example of an infinite and positive response.
[00:15:29 - 00:15:36] We should say if I are, that's an if I are filter
[00:15:36 - 00:15:38] and this is an IIR filter.
[00:15:39 - 00:15:43] Okay, so the key difference here between the recursive filter
[00:15:43 - 00:15:45] number two here, compared to the one,
[00:15:45 - 00:15:47] we just said the moving average one,
[00:15:47 - 00:15:52] is now our current output not only depends on current inputs,
[00:15:52 - 00:15:56] previous inputs, but it depends on the previous output.
[00:15:56 - 00:16:01] So feeding back the output to form the new output.
[00:16:02 - 00:16:08] Okay, so why then, when we take the z transform,
[00:16:08 - 00:16:10] we go to, oh, a bit of go back here.
[00:16:10 - 00:16:15] So z to minus 1 here is the delay property of the z transform.
[00:16:18 - 00:16:21] So why then, for our recursive filter,
[00:16:21 - 00:16:25] it's gonna go to why I've said, what's point nine?
[00:16:25 - 00:16:30] Why have in minus one going to go to point nine?
[00:16:30 - 00:16:33] Why is it z to minus one?
[00:16:33 - 00:16:34] Yep, good.
[00:16:34 - 00:16:43] And then plus point one, x of z.
[00:16:44 - 00:17:00] Linearity, what's there is delay?
[00:17:00 - 00:17:03] Okay, so let's look at our filters
[00:17:03 - 00:17:10] a little more detail.
[00:17:10 - 00:17:12] This is a common way of drawing out these filters,
[00:17:12 - 00:17:14] known as a realization.
[00:17:15 - 00:17:20] So this here is our first one.
[00:17:20 - 00:17:26] This is our moving average over four samples.
[00:17:26 - 00:17:33] Okay, so here we've got moving average.
[00:17:33 - 00:17:35] Okay, so I'll go through and explain
[00:17:35 - 00:17:36] what all these symbols mean.
[00:17:36 - 00:17:39] So x of n here, this is our input to our filter.
[00:17:39 - 00:17:41] This is our noisy signal.
[00:17:41 - 00:17:42] But why then on the right hand side,
[00:17:42 - 00:17:47] this is our output, our filtered signal.
[00:17:47 - 00:17:54] Hopefully removing some of the noise.
[00:17:54 - 00:17:59] Okay, so these circles with a plus in them are,
[00:18:00 - 00:18:07] hopefully, fill the obviously an addition.
[00:18:07 - 00:18:12] Then these triangles indicate a,
[00:18:14 - 00:18:16] multiplication.
[00:18:16 - 00:18:20] So for our moving average over four samples,
[00:18:20 - 00:18:22] we've got four multiplications.
[00:18:22 - 00:18:25] So they're all scaled here by a quarter.
[00:18:27 - 00:18:37] So these ones are multiplication.
[00:18:37 - 00:18:42] And what does the z to the minus one indicate?
[00:18:42 - 00:18:44] Yeah, exactly, delay.
[00:18:44 - 00:18:46] Okay, so here, let's go through an example.
[00:18:46 - 00:18:48] So we've got x of n with delaying.
[00:18:48 - 00:18:49] When we go through this box,
[00:18:49 - 00:18:53] this then becomes x of n minus one.
[00:18:53 - 00:18:55] Then we multiply by a quarter.
[00:18:55 - 00:18:57] So then we have,
[00:18:58 - 00:18:59] here going into the summer,
[00:18:59 - 00:19:04] we have 0.25 times x of n minus one.
[00:19:06 - 00:19:18] Actually, this square bracket, start again.
[00:19:18 - 00:19:23] So this is x of n minus one.
[00:19:24 - 00:19:27] This is x of n minus two.
[00:19:28 - 00:19:32] x of n minus three.
[00:19:32 - 00:19:37] So this here becomes 0.25 x n minus three.
[00:19:38 - 00:19:43] So we're scaled by a quarter,
[00:19:43 - 00:19:47] and with delay by three samples.
[00:19:47 - 00:19:49] So if you go through to this whole thing,
[00:19:49 - 00:19:50] before our filter here,
[00:19:51 - 00:19:56] our output y of n is equal to 0.25.
[00:19:57 - 00:20:02] x of n plus 0.25 x of n minus one,
[00:20:04 - 00:20:09] plus 0.25 x of n minus two plus 0.25 x of n minus three.
[00:20:18 - 00:20:23] Okay, so there's a final impulse response filter.
[00:20:24 - 00:20:27] We're not feeding the output back
[00:20:28 - 00:20:32] to create our new output.
[00:20:32 - 00:20:35] Something else I'm gonna do here is let's consider
[00:20:35 - 00:20:40] what happens if our input x of n is equal to one,
[00:20:43 - 00:20:50] then 0, then 0, then dot dot dot, what do we call that?
[00:20:50 - 00:20:54] Underline it here.
[00:20:54 - 00:21:00] The first sample, what sort of signal is that?
[00:21:00 - 00:21:00] Impulse good, yeah.
[00:21:00 - 00:21:02] So I'll just flip back,
[00:21:02 - 00:21:05] we'll play this is this one here.
[00:21:05 - 00:21:07] So we've got a one for the first sample,
[00:21:07 - 00:21:10] and otherwise 0's.
[00:21:11 - 00:21:19] So this is our unit impulse.
[00:21:19 - 00:21:26] Okay, so let's consider what happens to our output y of n,
[00:21:26 - 00:21:32] when we put on that unit impulse.
[00:21:32 - 00:21:34] Okay, so we put in here for x of n,
[00:21:34 - 00:21:37] we're putting in a one,
[00:21:37 - 00:21:41] we multiply by a quarter,
[00:21:41 - 00:21:46] so we're assuming all previous y in's are 0.
[00:21:47 - 00:21:56] So then we end up with,
[00:21:56 - 00:21:58] so the next value of x of n is 0,
[00:22:00 - 00:22:03] but that one propagates through the delay
[00:22:03 - 00:22:05] is multiplied by a quarter,
[00:22:05 - 00:22:11] and our output is then a quarter.
[00:22:11 - 00:22:22] So we then have for our output a quarter, a quarter, a quarter,
[00:22:25 - 00:22:31] and then once that unit impulse is propagated through all
[00:22:31 - 00:22:36] the delays, we're just putting zeros in each of these branches,
[00:22:36 - 00:22:41] and so then we're getting a zero.
[00:22:41 - 00:22:44] So for this finite impulse response filter,
[00:22:46 - 00:22:48] when we put in the impulse,
[00:22:48 - 00:22:53] the output is finite.
[00:22:53 - 00:22:55] And we're going to comparison
[00:22:55 - 00:22:57] with the infinite impulse response.
[00:22:57 - 00:23:07] Yes, yes, yes, so that's where the, yeah, exactly.
[00:23:07 - 00:23:08] Yeah, yeah, yeah.
[00:23:09 - 00:23:11] So you change the weightings on these filters
[00:23:11 - 00:23:14] to be one over 10 if we had 10 branches here.
[00:23:15 - 00:23:20] Okay, so for these moving average filters,
[00:23:20 - 00:23:23] the impulse response is finite.
[00:23:23 - 00:23:27] Okay, so decays away to zero after your number of coefficients.
[00:23:27 - 00:23:30] So here we've got four coefficients, four multipliers
[00:23:30 - 00:23:35] in our filter, and the impulse response
[00:23:35 - 00:23:42] is just four values long.
[00:23:42 - 00:23:45] Okay, so that's, if I are, let's do the infinite
[00:23:45 - 00:23:50] impulse response filter, which has a realization like this.
[00:23:50 - 00:23:55] So the key thing here for the IIR filter
[00:23:56 - 00:24:02] is we've got this feedback loop.
[00:24:02 - 00:24:06] Okay, so the example we looked at the other day,
[00:24:06 - 00:24:12] we had scales or coefficients of 0.1 and 0.9.
[00:24:14 - 00:24:16] Okay, so we're going to input here.
[00:24:16 - 00:24:23] So this is 0.1, x of n there, going for the summer.
[00:24:23 - 00:24:25] Here we've got the output Y of n,
[00:24:25 - 00:24:28] we're feeding it back through a delay.
[00:24:28 - 00:24:33] This then becomes Y of n minus one.
[00:24:34 - 00:24:39] And at this point here we have then 0.9 Y of n minus one.
[00:24:44 - 00:24:45] Okay, and we sum them together.
[00:24:45 - 00:24:53] So Y of n is then equal to Y of n minus one.
[00:24:54 - 00:24:58] Plus 0.1 x of n.
[00:24:58 - 00:25:02] So we have the previous output,
[00:25:02 - 00:25:05] and then we're multiplying or adding it
[00:25:05 - 00:25:08] the current input by 0.1.
[00:25:08 - 00:25:11] Yes.
[00:25:11 - 00:25:13] Oh, yeah, it should be your point.
[00:25:13 - 00:25:14] 0.9 of the previous output, yeah.
[00:25:17 - 00:25:18] Just draw it in here.
[00:25:18 - 00:25:29] Now I'll start again.
[00:25:29 - 00:25:34] So Y of n is equal to 0.9 Y.
[00:25:36 - 00:25:49] In minus one plus 0.1 x of n.
[00:25:49 - 00:25:51] Okay, let's look at the impulse response again
[00:25:51 - 00:25:57] for this filter.
[00:25:57 - 00:25:58] Our input,
[00:26:00 - 00:26:05] x of n is going to be one followed by 0.0.
[00:26:09 - 00:26:18] Our output Y of n.
[00:26:18 - 00:26:19] So the first time we go through,
[00:26:19 - 00:26:35] we have 0.1.
[00:26:35 - 00:26:38] Then the next time our input is 0,
[00:26:38 - 00:26:41] but we have 0.9 of the previous output,
[00:26:41 - 00:26:43] which was 0.9 of 0.1,
[00:26:43 - 00:26:47] because that's 0.09.
[00:26:47 - 00:26:50] Then we have 0.9 of 0.09,
[00:26:50 - 00:26:54] so that's 0.081.
[00:26:54 - 00:26:56] Then we have 0.9, 0.081,
[00:26:56 - 00:26:59] is 0.729.dot.
[00:27:02 - 00:27:06] So this is infinite.
[00:27:06 - 00:27:09] So it doesn't nicely go to 0,
[00:27:09 - 00:27:13] like I did with our finite impulse response,
[00:27:13 - 00:27:16] the moving average we looked at previously.
[00:27:17 - 00:27:19] Because we've got this feedback loop,
[00:27:19 - 00:27:23] we're continually feeding back the output
[00:27:23 - 00:27:24] as we get our new output.
[00:27:26 - 00:27:33] And so we're having our output as the K in.
[00:27:34 - 00:27:36] Our impulse response is the K in,
[00:27:36 - 00:27:38] but it's not equal to 0.
[00:27:38 - 00:27:48] Oh yes, yes, yes, I'm having a problem, don't I?
[00:27:48 - 00:27:56] I'm talking and thinking at the same time
[00:27:56 - 00:27:58] and writing this.
[00:27:58 - 00:27:59] There's good people who have elections,
[00:27:59 - 00:28:02] because I want to end up,
[00:28:02 - 00:28:04] but we have at least three here,
[00:28:04 - 00:28:05] is into those lecture already.
[00:28:05 - 00:28:10] Okay, good.
[00:28:10 - 00:28:12] Okay, so what are we up to?
[00:28:12 - 00:28:13] Okay, so the next thing,
[00:28:13 - 00:28:16] so we'll look at filter realizations,
[00:28:19 - 00:28:21] the impulse response is,
[00:28:21 - 00:28:22] the next thing we want to define
[00:28:22 - 00:28:29] is the transfer function in the Z domain.
[00:28:29 - 00:28:31] Okay, so we can define
[00:28:31 - 00:28:34] our transfer function,
[00:28:34 - 00:28:37] the domain transfer function as H of Z
[00:28:37 - 00:28:42] is equal to Y of Z over X of Z.
[00:28:42 - 00:28:49] So this is output over input.
[00:28:49 - 00:28:52] So that's analogous to our transfer function
[00:28:52 - 00:28:55] we were developing with Laplace transforms H of S
[00:28:55 - 00:28:59] was the output voltage over the input voltage
[00:28:59 - 00:29:07] for our analog filters.
[00:29:07 - 00:29:12] So just jumping back to our two sample moving average filter.
[00:29:14 - 00:29:16] So we had the somewhere,
[00:29:16 - 00:29:17] here's the top one here,
[00:29:17 - 00:29:24] we had the Z domain equation,
[00:29:24 - 00:29:27] and now we just need to rearrange that
[00:29:27 - 00:29:28] to get our transfer function.
[00:29:29 - 00:29:32] So all right, again, where we were before.
[00:29:32 - 00:29:37] So Y of Z was equal to 0.5 X of Z plus 0.5.
[00:29:39 - 00:29:47] X of Z times Z to the minus one.
[00:29:47 - 00:29:49] Okay, so what we want to do here
[00:29:49 - 00:29:51] is to collect up our X of Z.
[00:29:51 - 00:29:54] So we have Y of Z is then equal to,
[00:29:56 - 00:29:59] just a convective 0.5 here, X of Z,
[00:30:00 - 00:30:06] and then one plus Z to the minus one.
[00:30:06 - 00:30:11] So our transfer function in the Z domain, H of Z,
[00:30:11 - 00:30:13] which is the output Y of Z,
[00:30:13 - 00:30:18] and the input X of Z is equal to then 0.5,
[00:30:20 - 00:30:35] lots of one plus Z to the minus one.
[00:30:35 - 00:30:39] So that is for our finite and positive response filter.
[00:30:41 - 00:30:45] We can do the same thing for our infinite and positive response
[00:30:45 - 00:30:50] filter, which we'll do now.
[00:30:50 - 00:30:55] So we had the difference equation,
[00:30:56 - 00:31:00] and then we took the Z transform of that difference equation.
[00:31:02 - 00:31:04] This is for our recursive or I have filter.
[00:31:04 - 00:31:08] So we had previously that the output in Z domain,
[00:31:08 - 00:31:13] Y of Z is equal to 0.9 Y of Z times Z to the minus one,
[00:31:15 - 00:31:18] plus 0.1 X of Z.
[00:31:21 - 00:31:25] And so we'll take our other Y of Z,
[00:31:26 - 00:31:30] and we'll lift hand side so we've got all our Y of Zs
[00:31:30 - 00:31:38] on the left hand side.
[00:31:38 - 00:31:41] Okay, so that's the liquid 0.1 X of Z on the right hand side.
[00:31:42 - 00:31:45] So we can factorize out the Y of Z,
[00:31:45 - 00:31:50] and then we have 1 minus 0.9 X of the minus one.
[00:31:50 - 00:31:54] This equals 0.1 X of Z.
[00:31:54 - 00:31:58] So our transfer function H of Z,
[00:31:59 - 00:32:03] output Y of Z of the input X of Z
[00:32:03 - 00:32:10] is then equal to 0.1 in the numerator,
[00:32:10 - 00:32:15] and we have 1 minus 0.9 X of the minus one
[00:32:20 - 00:32:24] in the denominator.
[00:32:24 - 00:32:28] Okay, so in the numerator we can say we don't have a 0,
[00:32:29 - 00:32:38] and the denominator we have 1 pole.
[00:32:38 - 00:32:42] Okay, so this is the first order recursive filter.
[00:32:45 - 00:32:46] And so we've chosen here,
[00:32:47 - 00:32:50] particular values for coefficients,
[00:32:50 - 00:32:52] but we can, in the general form,
[00:32:52 - 00:32:57] we could write this H of Z is equal to 1 minus alpha
[00:33:00 - 00:33:05] over 1 minus alpha Z for minus one.
[00:33:43 - 00:33:49] Okay, so we've got our
[00:33:51 - 00:33:53] transfer function in the Z domain.
[00:33:54 - 00:33:59] If we want to evaluate that in terms of frequencies,
[00:34:02 - 00:34:07] we can take the discrete time for a transform,
[00:34:12 - 00:34:17] but so we can substitute in frequencies for Z.
[00:34:17 - 00:34:22] So we had before that Z was equal to E to the ST,
[00:34:24 - 00:34:31] and we have that S is sigma plus J omega,
[00:34:33 - 00:34:39] and if we're in steady states, sigma is 0,
[00:34:39 - 00:34:44] so we have E to the J omega T.
[00:34:45 - 00:34:49] And if we write in terms of frequencies,
[00:34:54 - 00:35:01] if rather than in terms of angle frequency z is equal
[00:35:02 - 00:35:05] to E to the J to pi F T.
[00:35:05 - 00:35:16] So this is capital T, which is our sampling period.
[00:35:16 - 00:35:21] We have our Z domain transfer function H of Z,
[00:35:22 - 00:35:26] and so if we want to get our frequency response from that,
[00:35:28 - 00:35:35] we can substitute Z is equal to E to the J to pi F T.
[00:35:38 - 00:35:41] So that was symbolizing getting the frequency response
[00:35:41 - 00:35:46] from the Laplace transform, where we substituted in that
[00:35:47 - 00:35:58] S was equal to J to pi F.
[00:35:58 - 00:36:05] Okay, so for our two sample moving average
[00:36:05 - 00:36:09] that we've been playing with,
[00:36:09 - 00:36:14] we had couple slides ago, H of Z,
[00:36:14 - 00:36:17] our Z domain transfer function is a half,
[00:36:17 - 00:36:23] one plus Z to the minus one.
[00:36:23 - 00:36:27] And so then our discrete time frequency response,
[00:36:27 - 00:36:31] capital H of F, so this is now,
[00:36:31 - 00:36:37] the frequency response in terms of frequency and Hertz,
[00:36:37 - 00:36:42] this is then equal to 0.51 plus,
[00:36:42 - 00:36:47] so substituting in for Z is equal to E to the J to pi F T.
[00:36:47 - 00:36:52] So Z to the minus one becomes then E to the minus J to pi F T.
[00:36:58 - 00:37:05] Okay, and I'm gonna use the subscript here H1 over T.
[00:37:05 - 00:37:07] And so this one over T is just indicating
[00:37:07 - 00:37:19] that we have sampled period T.
[00:37:19 - 00:37:20] Okay, and you can do some maths
[00:37:20 - 00:37:22] with trigger identities and things.
[00:37:22 - 00:37:27] So just do dot dot dot dot to share the H1 over T of F
[00:37:27 - 00:37:34] is equal to the cosine of pi times the frequency times
[00:37:34 - 00:37:39] the sampling period T times E to the minus J to pi F T.
[00:37:49 - 00:37:51] Okay, so this ends up being,
[00:37:52 - 00:37:56] because we have cosine here,
[00:37:56 - 00:37:59] the magnitude of our frequency response
[00:37:59 - 00:38:04] is then periodic with period T, period one over T.
[00:38:15 - 00:38:29] In the frequency domain.
[00:38:29 - 00:38:33] Okay, so this is a way to go from our transfer function
[00:38:33 - 00:38:37] to looking at the frequency response in terms of Hertz,
[00:38:37 - 00:38:40] all of our filter, and on the next slide,
[00:38:40 - 00:38:42] I've got a figure of what this looks like
[00:38:42 - 00:38:50] for this two sample moving average.
[00:38:50 - 00:38:52] Okay, so it's got this magnitude in the way,
[00:38:52 - 00:38:57] it's got this cosine part,
[00:38:57 - 00:39:01] and there's also a phase as well.
[00:39:01 - 00:39:16] But if we look at the magnitude then of our frequency response,
[00:39:16 - 00:39:17] so this is the magnitude.
[00:39:18 - 00:39:21] Here, so this is capital H.
[00:39:21 - 00:39:25] This is gonna period one over T frequency.
[00:39:26 - 00:39:29] So we're plotting here the frequency response
[00:39:29 - 00:39:33] of our moving average filter against frequency and Hertz
[00:39:33 - 00:39:58] is at the magnitude of the frequency response.
[00:39:58 - 00:40:00] Okay, and so this here is,
[00:40:03 - 00:40:16] I've been sampled at a kilohertz,
[00:40:16 - 00:40:18] F is a kilohertz,
[00:40:20 - 00:40:24] the sampling frequency is one over the period,
[00:40:24 - 00:40:25] or vice versa.
[00:40:26 - 00:40:31] So this is acting as a loop pass filter,
[00:40:36 - 00:40:38] so we did this two sample moving average
[00:40:38 - 00:40:40] for filtering out the high frequencies.
[00:40:41 - 00:40:46] So it's got this shape you would intuitively expect.
[00:40:46 - 00:40:50] So it's dropping off with frequency,
[00:40:50 - 00:40:54] but then it's periodic because we have sampled it.
[00:40:54 - 00:40:59] So this is then periodic with period one over T,
[00:41:07 - 00:41:08] they call Fs.
[00:41:08 - 00:41:09] So this is here,
[00:41:09 - 00:41:11] we'll have a kilohertz.
[00:41:11 - 00:41:14] This has been Fs over two.
[00:41:18 - 00:41:21] This is here three,
[00:41:21 - 00:41:23] Fs over two,
[00:41:25 - 00:41:26] or three over two.
[00:41:30 - 00:41:40] Okay, so the,
[00:41:43 - 00:41:47] we have a sample signal, digital signal,
[00:41:47 - 00:41:52] we have a detonate transfer function for that,
[00:41:52 - 00:41:55] to then get what the frequency response looks like
[00:41:55 - 00:41:57] in terms of frequency,
[00:41:57 - 00:42:02] we substitute in z is e to the j2 pi Ft.
[00:42:03 - 00:42:04] For this two sample moving average,
[00:42:04 - 00:42:08] we have this cosine, which is obviously repeating.
[00:42:08 - 00:42:09] If a low pass filter,
[00:42:09 - 00:42:12] we can set the lowest frequencies here,
[00:42:13 - 00:42:16] but because we've got digital signal,
[00:42:16 - 00:42:18] we've sampled it,
[00:42:18 - 00:42:24] the frequency response becomes periodic.
[00:42:24 - 00:42:29] Okay, so that was for that finite impulse response filter.
[00:42:29 - 00:42:34] We can do the same thing for our recursive filter,
[00:42:34 - 00:42:35] the infinite impulse response filter,
[00:42:35 - 00:42:40] look at a frequency response for that.
[00:42:40 - 00:42:46] So let's just go back to our,
[00:42:46 - 00:42:48] see the main transfer function.
[00:42:48 - 00:42:53] So we had this one minus alpha over one minus alpha z
[00:42:53 - 00:42:54] to the minus one,
[00:42:55 - 00:42:59] and we've been using alpha is 0.9.
[00:43:00 - 00:43:07] So this is a plot here of the magnitude of our frequency response,
[00:43:08 - 00:43:11] which has been sampled at one at a T,
[00:43:11 - 00:43:15] as a function of frequency F.
[00:43:15 - 00:43:22] And so we can get our equation for the magnitude
[00:43:22 - 00:43:32] of frequency response by substituting in,
[00:43:32 - 00:43:33] what, that line there?
[00:43:33 - 00:43:40] Sorry, this is evaluating a frequency response
[00:43:40 - 00:43:46] with z is equal to e to the j2 pi Ft.
[00:43:50 - 00:43:53] So this becomes one minus alpha as before.
[00:43:54 - 00:43:59] And then we have one minus alpha e to the minus j2 pi
[00:44:00 - 00:44:03] Ft, okay.
[00:44:03 - 00:44:12] So again, this is showing that filter is a low pass filter.
[00:44:19 - 00:44:21] And this one I've only shown one period of it,
[00:44:21 - 00:44:36] but is also periodic with period one over T.
[00:44:36 - 00:44:38] Okay, so those two filters will look at both the finite
[00:44:38 - 00:44:43] impulse response and the infinite impulse response
[00:44:46 - 00:44:47] low pass filters?
[00:44:47 - 00:44:52] Yes.
[00:44:52 - 00:44:56] Yeah.
[00:44:56 - 00:45:02] Yeah.
[00:45:02 - 00:45:13] Yes.
[00:45:13 - 00:45:14] Yeah.
[00:45:14 - 00:45:15] Yeah.
[00:45:15 - 00:45:19] Just to show that actually in reality it is keeps going.
[00:45:19 - 00:45:24] But conventionally you just showed the first cycle,
[00:45:24 - 00:45:36] like I said on the next one.
[00:45:36 - 00:45:36] Well, you should.
[00:45:38 - 00:45:39] Got things a bit out of order.
[00:45:39 - 00:45:44] But if you're, if you're an anti-aliess filter,
[00:45:45 - 00:45:46] or if you're not, if you're not,
[00:45:46 - 00:45:48] with sample with an anti-aliess filter,
[00:45:48 - 00:45:50] you shouldn't get any higher frequencies.
[00:45:50 - 00:45:51] Yeah.
[00:45:52 - 00:45:54] We haven't done the sampling and using it.
[00:45:54 - 00:45:55] So it's kind of a bit backwards.
[00:45:55 - 00:45:57] But we'll do more on that next week.
[00:46:01 - 00:46:04] Okay, so, good ones to go.
[00:46:04 - 00:46:09] So let's look at stability.
[00:46:10 - 00:46:11] Now for today.
[00:46:11 - 00:46:16] So we know the plus transform fairly well.
[00:46:16 - 00:46:19] So we'll go look and set up the plus.
[00:46:19 - 00:46:22] So the velocity that you've done in various courses.
[00:46:22 - 00:46:23] And then what happened?
[00:46:23 - 00:46:25] That means for the z transform.
[00:46:26 - 00:46:28] We'll see a domain here on the right.
[00:46:29 - 00:46:31] So in the plus domain.
[00:46:32 - 00:46:34] All right, so this is a sigma and J omega.
[00:46:36 - 00:46:41] And so the plus domain for our system to be stable.
[00:46:42 - 00:46:47] I thought it was to be stable.
[00:46:47 - 00:46:51] We need our poles to learn the left-hand plane.
[00:46:51 - 00:46:58] So green equals stable.
[00:46:58 - 00:47:03] By system here, I really meant filter.
[00:47:03 - 00:47:07] Okay, so you've seen that for three or three or two
[00:47:07 - 00:47:09] or three or anything or anything.
[00:47:09 - 00:47:10] Oh three.
[00:47:11 - 00:47:18] And so we have this z was equal to e to the st.
[00:47:22 - 00:47:29] And s is equal to sigma plus J omega.
[00:47:29 - 00:47:34] So we can write this as e to the sigma t times,
[00:47:36 - 00:47:40] let's see a sigma t is the J omega t.
[00:47:45 - 00:47:49] Okay, so if sigma is in the left-hand plane
[00:47:49 - 00:47:53] is the negative number, then the magnitude of e
[00:47:53 - 00:47:55] to the sigma t will be less than one.
[00:47:55 - 00:47:59] Okay, so that means in the z domain.
[00:48:00 - 00:48:04] And so we'll write this as our axis here,
[00:48:04 - 00:48:06] the real part of the z and the imaginary part of z.
[00:48:07 - 00:48:12] Our system will be stable if our poles lie within
[00:48:12 - 00:48:13] the unit circle.
[00:48:13 - 00:48:17] So the unit circle is a circle of radius one.
[00:48:17 - 00:48:21] Okay, so this mapping from the left-half plane
[00:48:22 - 00:48:27] in the left-hand plane to the unit circle in the z domain.
[00:48:30 - 00:48:34] So that way we can tell whether our filter is stable
[00:48:35 - 00:48:41] in the z domain by looking at the magnitude of the poles.
[00:48:41 - 00:48:45] And so the example we were looking at alpha was 0.9.
[00:48:45 - 00:48:47] So the pole was 0.9.
[00:48:51 - 00:48:53] So that means that the filter is stable.
[00:48:53 - 00:48:58] If we had our alpha such that the pole was outside
[00:48:58 - 00:49:04] unit circle, then we would have an unstable filter
[00:49:05 - 00:49:09] and then the output would be increasing without bound.
[00:49:09 - 00:49:14] Okay, so it's a good place to stop today.
[00:49:14 - 00:49:16] So I'll just leave this up for a couple minutes
[00:49:16 - 00:49:18] while you finish writing down and then
[00:49:18 - 00:49:22] I hope you'll see some or all of you in the tutorial
[00:49:22 - 00:49:23] in the continuous.
[00:50:35 - 00:50:43] Thank you.
[00:50:43 - 00:50:44] Yes.
[00:51:05 - 00:51:07] Yeah, it was a good one.
[00:51:07 - 00:51:08] It was a good one.
[00:51:08 - 00:51:09] Yeah, it was pretty good.
[00:51:09 - 00:51:10] Oh, well.
[00:51:10 - 00:51:13] They did it all in three months on my,
[00:51:13 - 00:51:14] thank you for the light.
[00:51:14 - 00:51:16] Yeah, it did have to make sure.
[00:51:16 - 00:51:18] And so that was kind of misleading.
[00:51:18 - 00:51:19] Oh, that's good.
[00:51:19 - 00:51:20] It's pretty thin.
[00:51:20 - 00:51:21] It's my goals.
[00:51:21 - 00:51:22] Yeah, yes.
[00:51:22 - 00:51:23] Thank you.
[00:51:23 - 00:51:24] Cheers.

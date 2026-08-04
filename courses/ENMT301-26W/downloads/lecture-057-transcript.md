# ENMT301-26W Lecture 57 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `6314a36f0e5f7f8e4effc78f4cd582ed98203c336ba76c38541b67c349fc66f7`
Generated: 2026-06-06T07:09:24.234325+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:00 - 00:00:04] And you're just going to pay paper like people who will.
[00:00:04 - 00:00:05] Or is that paper?
[00:00:05 - 00:00:14] OK, Curricotto.
[00:00:14 - 00:00:15] Hello, everyone.
[00:00:15 - 00:00:20] Everyone that's done there, assignments or close to it.
[00:00:20 - 00:00:24] Or people at home listening in the future.
[00:00:24 - 00:00:27] So just to go back to basics.
[00:00:27 - 00:00:31] So we'll be looking at firstly, analog filters,
[00:00:31 - 00:00:35] where we can fill throughout certain frequencies by building
[00:00:35 - 00:00:38] circuits, how to resist this, capacitors and ductors.
[00:00:38 - 00:00:42] You can also make more fancy filters if you include opamps as well.
[00:00:42 - 00:00:48] And we use the Laplace transform to analyze those analog circuits.
[00:00:48 - 00:00:50] We'll set it for a transform of that.
[00:00:50 - 00:00:57] And then we can also do a digital filter where we have a microcontroller.
[00:00:58 - 00:01:07] And we use the Z-transform to analyze our filter, our digital filter.
[00:01:07 - 00:01:11] And so we have this mapping that we're finished on yesterday,
[00:01:11 - 00:01:18] where for a system in Laplace space, we need the poles of the system to lie in the lift half plane
[00:01:18 - 00:01:23] for it to be a stable system, a stable filter.
[00:01:23 - 00:01:27] And when we do a mapping from the Laplace domain to the free of the main,
[00:01:27 - 00:01:32] that means the poles of our filter have to lie in the unit circle.
[00:01:32 - 00:01:40] So it's a circle of radius 1 and the Z domain for what the filter is to be stable.
[00:01:40 - 00:01:50] OK, it's not stable, then the output is going to increase without bound.
[00:01:50 - 00:01:56] OK, so there's one slide left in this set, and then we'll get onto the next set,
[00:01:56 - 00:01:58] that digital filters.
[00:01:58 - 00:02:05] And this is on the discrete time for a transform.
[00:02:05 - 00:02:09] So this is the free transform of a sampled signal.
[00:02:09 - 00:02:14] So in discrete time.
[00:02:14 - 00:02:21] OK, and so the discrete time for a transform is...
[00:02:21 - 00:02:25] So it's a...
[00:02:25 - 00:02:31] Some, because we have a sampled signal x-min.
[00:02:31 - 00:02:33] So we could do it in discrete.
[00:02:33 - 00:02:37] Some of our sampled signal x-min.
[00:02:37 - 00:02:43] And we're going to consider for minus infinity to infinity for our samples.
[00:02:43 - 00:02:46] So x-min here is discrete.
[00:02:46 - 00:03:02] And then we have our complex exponential e to the minus j to pi if in the sample number capital T the period.
[00:03:02 - 00:03:09] So the capital T is the period.
[00:03:09 - 00:03:12] OK, and so this is our discrete time for a transform.
[00:03:12 - 00:03:15] So the little x goes to the capital x.
[00:03:15 - 00:03:20] This is a continuous function of frequency if.
[00:03:20 - 00:03:25] And it's periodic with period 1 over t.
[00:03:25 - 00:03:31] So period, odd at the period 1 over t.
[00:03:31 - 00:03:33] It is 1 over t.
[00:03:33 - 00:03:35] So this is continuous.
[00:03:35 - 00:03:44] And so if we compare this to our regular Fourier transform,
[00:03:44 - 00:03:57] which is x and f is equal to...
[00:03:57 - 00:03:59] We have an integral.
[00:03:59 - 00:04:02] So continuous integral minus infinity with infinity.
[00:04:02 - 00:04:03] Our signal...
[00:04:03 - 00:04:04] Our signal...
[00:04:04 - 00:04:06] Continuous signal x of t...
[00:04:06 - 00:04:10] e to the minus j to pi x.
[00:04:10 - 00:04:12] So we can do this.
[00:04:12 - 00:04:14] So x of t...
[00:04:14 - 00:04:21] e to the minus j to pi if t.
[00:04:21 - 00:04:24] And so time little t...
[00:04:24 - 00:04:31] Continuous time is equal to the sample number in times our sample period capital T.
[00:04:31 - 00:04:34] So this is a discrete time for a transform.
[00:04:34 - 00:04:40] It's almost equivalent to our continuous Fourier transform, except we've got a sample signal.
[00:04:40 - 00:04:45] And then in our complex exponential, we have the sample number in times capital T,
[00:04:45 - 00:04:48] which is equivalent to our little t.
[00:04:48 - 00:04:52] And so because of this sampling,
[00:04:52 - 00:04:59] we then end up with a periodic Fourier transform.
[00:04:59 - 00:05:07] Okay, so that's a way if we know our discrete signal,
[00:05:07 - 00:05:11] we can then get its continuous Fourier transform.
[00:05:11 - 00:05:18] Okay, and if we're thinking about our filter,
[00:05:18 - 00:05:21] we can get our filter output.
[00:05:21 - 00:05:26] So that's capital Y, which is a period one over t,
[00:05:26 - 00:05:28] of f.
[00:05:28 - 00:05:30] So this is our filter output.
[00:05:30 - 00:05:41] So in the frequency domain, this is multiplication of our filter input.
[00:05:41 - 00:05:43] So it's x of f.
[00:05:43 - 00:05:45] This is also sampled.
[00:05:45 - 00:05:47] So it's periodic period one over t.
[00:05:47 - 00:05:50] So it's filter input.
[00:05:50 - 00:05:53] And we have a convolution in the time domain.
[00:05:53 - 00:05:57] So this is a multiplication in a frequency domain.
[00:05:57 - 00:06:02] We are capital H of f is the frequency response of our filter.
[00:06:02 - 00:06:16] Okay, so this...
[00:06:16 - 00:06:23] Yes.
[00:06:23 - 00:06:26] So we've got this continuous signal.
[00:06:26 - 00:06:30] And so you have something frequency, say a kilohertz whatever,
[00:06:30 - 00:06:33] every one millisecond.
[00:06:33 - 00:06:36] You've been sampling it with your ADC.
[00:06:36 - 00:06:44] Okay, and so then in the frequency space,
[00:06:44 - 00:06:46] the spectrum becomes periodic.
[00:06:46 - 00:06:48] So with the...
[00:06:48 - 00:06:53] This low-pass filter we had yesterday from our moving average,
[00:06:53 - 00:06:58] it is then repeating with the sampling frequency,
[00:06:58 - 00:07:00] which is a kilohertz.
[00:07:00 - 00:07:05] So that one over t subscript there is saying for each of these quantities,
[00:07:05 - 00:07:09] they are periodic with frequency.
[00:07:09 - 00:07:12] Or as the continuous for a transform,
[00:07:12 - 00:07:14] if we haven't sampled our signal,
[00:07:14 - 00:07:17] then it's not periodic.
[00:07:17 - 00:07:20] But by sampling our signal,
[00:07:20 - 00:07:23] making it discrete, we've introduced this periodicity.
[00:07:23 - 00:07:30] Yeah, so it's kind of like almost the inverse of the Fourier series.
[00:07:30 - 00:07:35] We've got a continuous signal that goes to discrete spectrum.
[00:07:35 - 00:07:37] This is kind of the opposite.
[00:07:37 - 00:07:41] We've got the discrete signal going to a continuous spectrum.
[00:07:41 - 00:07:42] Yeah.
[00:07:42 - 00:07:44] Good.
[00:07:44 - 00:07:46] Yep, please, you got your questions.
[00:07:46 - 00:07:48] Okay, so there we go.
[00:07:48 - 00:07:51] So that's the end of that section.
[00:07:51 - 00:07:54] So just close this off, we've got to go down.
[00:07:54 - 00:07:56] And then I put the second one,
[00:07:56 - 00:08:00] which is a bit more on impulse response,
[00:08:00 - 00:08:06] and then we'll get into calculating convolutions.
[00:08:06 - 00:08:09] So we can calculate the output of our filter.
[00:08:09 - 00:08:10] That's convolution.
[00:08:10 - 00:08:37] Okay, keep the load this up.
[00:08:37 - 00:08:59] Okay, so on the title slide there,
[00:08:59 - 00:09:03] I've got two different impulse responses,
[00:09:03 - 00:09:06] a2 then.
[00:09:06 - 00:09:19] What sort of impulse response is the one on the left?
[00:09:19 - 00:09:23] Yes, is it finite infinite?
[00:09:23 - 00:09:24] Finite?
[00:09:24 - 00:09:31] Yes, this is a finite impulse response.
[00:09:31 - 00:09:38] And we also called that moving average.
[00:09:38 - 00:09:41] Yes, good.
[00:09:41 - 00:09:44] So this was a two sample moving average.
[00:09:44 - 00:09:46] So there's got a weighting a half.
[00:09:46 - 00:09:49] So we're just averaging over two consecutive samples
[00:09:49 - 00:09:52] to try and give them that some are hyper-conceived noise.
[00:09:52 - 00:09:58] Okay, so moving average just felt in real quick.
[00:09:58 - 00:10:09] This describes a finite impulse response filter.
[00:10:09 - 00:10:12] The moving average type,
[00:10:12 - 00:10:15] the weights don't all need to be exactly the same.
[00:10:15 - 00:10:23] If it's finite, then it's a moving average filter.
[00:10:23 - 00:10:26] Okay, so the one on the right,
[00:10:26 - 00:10:30] please actually keep going.
[00:10:30 - 00:10:34] That is then an.
[00:10:34 - 00:10:36] Well, I think it seems to be okay,
[00:10:36 - 00:10:40] but it's what's the filter type called infinite impulse response.
[00:10:40 - 00:10:50] And then the hardest question is infinite impulse response.
[00:10:50 - 00:10:53] And so that's another name,
[00:10:53 - 00:10:56] which is going to be a tricky question.
[00:10:56 - 00:11:01] So the recursive and the other one that gets used is autoregressive.
[00:11:01 - 00:11:03] Autoregressive.
[00:11:03 - 00:11:12] Okay, so this is known as moving average in a autoregressive.
[00:11:12 - 00:11:14] And this is also called recursive.
[00:11:14 - 00:11:19] So that's where we have the filter output.
[00:11:19 - 00:11:22] It depends not just on the inputs,
[00:11:22 - 00:11:25] but also on previous outputs.
[00:11:25 - 00:11:29] Okay, so we'll go into a bit more detail about these different types
[00:11:29 - 00:11:32] of filter,
[00:11:32 - 00:11:38] how we can analyze them and where they are useful.
[00:11:38 - 00:11:46] Okay, so we had yesterday our.
[00:11:46 - 00:11:49] Transfunction of the z domain.
[00:11:49 - 00:11:51] H of z.
[00:11:51 - 00:11:53] This is the ratio of the output,
[00:11:53 - 00:11:55] why is it.
[00:11:55 - 00:11:57] So the input to the filter X is in.
[00:11:57 - 00:12:06] So this is outputs,
[00:12:06 - 00:12:21] output over input.
[00:12:21 - 00:12:25] Okay, so if we want to get the impulse response to the filter.
[00:12:25 - 00:12:33] So the impulse response.
[00:12:33 - 00:12:39] H of n is the z transform here with the transfer function.
[00:12:39 - 00:12:41] H of z.
[00:12:41 - 00:12:43] So the transfer function.
[00:12:43 - 00:12:47] We can get that from the difference equation.
[00:12:47 - 00:12:52] And if we want the impulse response.
[00:12:52 - 00:12:54] Little h of n.
[00:12:54 - 00:13:01] We then need to take the inverse z transform.
[00:13:01 - 00:13:05] Of H of z.
[00:13:05 - 00:13:26] There's a gap there because what I wrote on the top is supposed to go down the bottom.
[00:13:26 - 00:13:27] But that's fine.
[00:13:27 - 00:13:30] Okay, so.
[00:13:30 - 00:13:34] There is an integral to do this in versus in transform,
[00:13:34 - 00:13:36] which is really messy.
[00:13:36 - 00:13:38] And so.
[00:13:38 - 00:13:41] People don't actually do the integrals to do the.
[00:13:41 - 00:13:43] And this is transforms.
[00:13:43 - 00:13:46] We can make use of the tables and the common properties
[00:13:46 - 00:13:49] and the common functions like we've done with the plus and for
[00:13:49 - 00:13:51] your transforms.
[00:13:51 - 00:13:58] So these are the three key properties of the z transform we went through yesterday.
[00:13:58 - 00:14:02] And then the three key peers.
[00:14:02 - 00:14:06] We've been through so delta function.
[00:14:06 - 00:14:08] A unit step.
[00:14:08 - 00:14:13] So this is delta unit step.
[00:14:13 - 00:14:18] And this is an exponential.
[00:14:18 - 00:14:25] So delta is a.
[00:14:25 - 00:14:27] The z transform is a constant.
[00:14:27 - 00:14:40] And for unit step and an exponential we have a single pole.
[00:14:40 - 00:14:43] Okay, so this is in the formula sheet for the test.
[00:14:43 - 00:14:55] Okay, so the formula sheet for the test is up on learn.
[00:14:55 - 00:14:56] So it's good.
[00:14:56 - 00:14:57] I didn't have a look at that.
[00:14:57 - 00:14:59] Especially when you're doing.
[00:14:59 - 00:15:00] The tutorials and things.
[00:15:00 - 00:15:03] So last year in the test, I'll remind you that the
[00:15:03 - 00:15:05] other sheet sheet, this year we've got formula sheet.
[00:15:05 - 00:15:06] So.
[00:15:06 - 00:15:09] The test format will be slightly different.
[00:15:09 - 00:15:11] So hopefully you've given you all the formula you need for the
[00:15:11 - 00:15:12] test.
[00:15:12 - 00:15:18] Okay.
[00:15:18 - 00:15:24] So those are our z transform peers.
[00:15:24 - 00:15:31] Okay, so let's try and find the impulse response for our.
[00:15:31 - 00:15:36] Two sample moving average filter that we looked at yesterday.
[00:15:36 - 00:15:42] So we have our difference equation.
[00:15:42 - 00:15:44] We'll start off with.
[00:15:44 - 00:15:45] So done this before.
[00:15:45 - 00:15:50] Is it the recap difference equation?
[00:15:50 - 00:15:58] The output y of n is equal to half the current input x of n plus half the
[00:15:58 - 00:16:04] previous input x of n minus one.
[00:16:04 - 00:16:13] So this is a transfer function h of z, which is y of z over x of z.
[00:16:13 - 00:16:23] So this becomes a half plus a half z to the minus one.
[00:16:23 - 00:16:30] Okay, so this n minus one is a delay, which becomes z minus one.
[00:16:30 - 00:16:48] Okay, so the impulse response, which is the invested transform of
[00:16:48 - 00:16:49] h of z.
[00:16:49 - 00:17:08] So little h of n is equal to delta of n plus a half delta n minus one.
[00:17:08 - 00:17:21] So the half comes from the linearity and one and the delta as
[00:17:21 - 00:17:23] it transform peer.
[00:17:23 - 00:17:32] The sigma is one is from the delay.
[00:17:32 - 00:17:40] Okay, so we can write this as a sequence.
[00:17:40 - 00:17:44] The response h of n is then point five.
[00:17:44 - 00:17:47] That's been zero.
[00:17:47 - 00:17:49] And point five.
[00:17:49 - 00:17:51] So this is finite.
[00:17:51 - 00:17:56] We've just got two values for our impulse response,
[00:17:56 - 00:18:02] they're both a half.
[00:18:02 - 00:18:11] And so the for an FIR filter, these coefficients of our filter,
[00:18:11 - 00:18:18] the delta half half are the same as the values of the impulse
[00:18:18 - 00:18:19] response.
[00:18:19 - 00:18:34] So the filter coefficients same as impulse response,
[00:18:34 - 00:18:42] response, response filter.
[00:18:42 - 00:19:04] Like I said, if I have filters, quite simple in that respect,
[00:19:04 - 00:19:10] you can look at the filter coefficients and then you know what the
[00:19:10 - 00:19:14] impulse response of the filter is.
[00:19:14 - 00:19:20] The IIR filter, we'll look at now, is more complicated.
[00:19:20 - 00:19:27] Okay, so we've got this first order recursive filter,
[00:19:27 - 00:19:29] we're right the difference equation for it.
[00:19:29 - 00:19:38] So we've got y of n is equal to a times the previous output
[00:19:38 - 00:19:44] y of n minus one plus b times the current input x of n.
[00:19:44 - 00:19:57] So the output of the filter is equal to the previous output times
[00:19:57 - 00:20:02] a plus b times the current input.
[00:20:02 - 00:20:09] So we've got the feedback loop where we're feeding back the previous output
[00:20:09 - 00:20:12] to create our new output.
[00:20:12 - 00:20:23] Okay, so the z domain we have then y of z.
[00:20:23 - 00:20:28] So y of n goes to y of z, because the linearity theorem of a goes
[00:20:28 - 00:20:35] to a y of n minus one goes to y of z times z to the minus one
[00:20:35 - 00:20:39] plus then b times x of z.
[00:20:39 - 00:20:48] Okay, so this gives us our z domain transformation.
[00:20:48 - 00:20:57] H of z is y of z over x of z.
[00:20:57 - 00:21:03] So this gives us a constant b over one minus a z to the minus one.
[00:21:03 - 00:21:15] Okay, so this has got a single pole for this first order recursive
[00:21:15 - 00:21:17] y of our filter.
[00:21:17 - 00:21:38] Okay, so let's now look at how we're going to take the in-the-z transformers.
[00:21:38 - 00:21:43] This one's remember b over one minus eight is z minus one
[00:21:43 - 00:21:46] is our function in the z domain.
[00:21:46 - 00:21:50] So we've got here this one here.
[00:21:50 - 00:21:53] One over one minus a z to the minus one.
[00:21:53 - 00:21:58] That goes to then the value of a, the power of n,
[00:21:58 - 00:22:00] times u of n, the unit step function.
[00:22:00 - 00:22:13] So we then have the impulse response for this is then h of n is equal to b.
[00:22:13 - 00:22:20] So this comes from linearity times a to the power of n,
[00:22:20 - 00:22:23] times the unit step u of n.
[00:22:23 - 00:22:33] So this all comes from a single pole right up here.
[00:22:33 - 00:22:38] U of n is the unit step u of n.
[00:22:38 - 00:22:57] Okay, so we can write this as a sequence that would be h of n is equal to
[00:22:57 - 00:23:01] so because multiplied by u of n there,
[00:23:01 - 00:23:06] it's going to be zero for nigou values of n.
[00:23:06 - 00:23:10] So we'll just start off with the first one and underliner.
[00:23:10 - 00:23:12] So that is in a zero.
[00:23:12 - 00:23:15] So the first one when n is zero we just get b.
[00:23:15 - 00:23:19] When n is one we get b times a,
[00:23:19 - 00:23:27] then we get n is two, b times a squared dot dot.
[00:23:27 - 00:23:36] Okay, so I've plotted this here for what's the value of b in my plot.
[00:23:36 - 00:23:39] So we're going to get zero point two good.
[00:23:39 - 00:23:42] And I won't ask a because it's too complicated,
[00:23:42 - 00:23:46] but we've got here a is point eight.
[00:23:46 - 00:23:49] Yeah, exactly.
[00:23:49 - 00:23:51] That's going to be my next question.
[00:23:51 - 00:23:54] So we have, well, now I'll just write that.
[00:23:54 - 00:23:58] So if a is less than one, then the field will be stable.
[00:23:58 - 00:24:04] We'll get this exponential decrease of our impulse response.
[00:24:04 - 00:24:11] But if a is greater than one, it becomes unstable.
[00:24:11 - 00:24:17] And if a is equal to one, there's this called being marginally stable.
[00:24:17 - 00:24:20] So that's just a constant output.
[00:24:20 - 00:24:29] Okay, so the key thing here for the IR filter,
[00:24:29 - 00:24:37] we have now an infinite impulse response.
[00:24:37 - 00:24:39] These dots go for ever.
[00:24:39 - 00:24:45] They get closer and closer than zero,
[00:24:45 - 00:24:49] but they're not exactly equal to zero.
[00:24:49 - 00:24:55] And the other thing about the filter here,
[00:24:55 - 00:25:00] because we have all the values of h of n
[00:25:00 - 00:25:03] for n less than zero equal to zero,
[00:25:03 - 00:25:05] this means it's causal.
[00:25:05 - 00:25:30] Okay, but the infinite impulse response filter,
[00:25:30 - 00:25:51] these values of h of n are not the filter coefficients.
[00:25:51 - 00:25:56] Okay, so do a little graphical summary here of the different
[00:25:56 - 00:26:02] domains and transforms that will look at the digital filters.
[00:26:02 - 00:26:13] And I'm using capital T as the period of delta T.
[00:26:13 - 00:26:21] So we have capital T,
[00:26:21 - 00:26:25] which is one over the sum of frequency Fs.
[00:26:25 - 00:26:28] So this is the sum of the period.
[00:26:28 - 00:26:38] That's a time seconds if s is the sum of frequency.
[00:26:38 - 00:26:51] Okay, so we can get our transfer function x of z.
[00:26:53 - 00:26:58] This is equal to y of z over x of z.
[00:26:58 - 00:27:05] And we can get that from our difference equation.
[00:27:05 - 00:27:13] If we take the inverse z transform of our transfer function,
[00:27:13 - 00:27:16] normally using those tables and properties,
[00:27:16 - 00:27:22] we end up with our impulse response h of n.
[00:27:22 - 00:27:24] So this is discrete.
[00:27:24 - 00:27:31] It's been sampled.
[00:27:31 - 00:27:34] And if we take the dt ft,
[00:27:34 - 00:27:44] so this was the discrete time dt Fourier transform,
[00:27:44 - 00:27:51] we can then get the frequency response of our digital filter.
[00:27:51 - 00:27:59] So h of f.
[00:27:59 - 00:28:14] So this is continuous and it's periodic period on a dt.
[00:28:14 - 00:28:22] So it's one way round to get our frequency response.
[00:28:22 - 00:28:25] Or from our transfer function,
[00:28:25 - 00:28:31] we can get the frequency response directly by substituting in z
[00:28:31 - 00:28:36] is equal to that e to the j to pi ft.
[00:28:39 - 00:28:44] And similar to get the frequency response from the last
[00:28:44 - 00:28:48] transform where we substitute in that s is equal to j to pi f.
[00:28:48 - 00:29:05] Okay, what we're going to look at next is how we get the output
[00:29:05 - 00:29:12] of the filter if we know the impulse response of the filter.
[00:29:12 - 00:29:22] Okay, and what is going to end up being using convolution.
[00:29:22 - 00:29:26] Is everyone finished on the slide?
[00:29:26 - 00:29:27] Yeah, good.
[00:29:27 - 00:29:32] Okay, so we'll calculate the output of our filter.
[00:29:32 - 00:29:36] So this will be then our signal, hopefully with the noise
[00:29:36 - 00:29:38] or the interference removed.
[00:29:38 - 00:29:42] And so there are three ways of doing this.
[00:29:42 - 00:29:46] If our digital filter is linear time variant,
[00:29:46 - 00:29:50] here means it's not changing with time.
[00:29:50 - 00:29:54] And linear means if we increase the input by some scale
[00:29:54 - 00:29:58] up then the output will also increase by the same scalar.
[00:29:58 - 00:30:06] Okay, so this way you could go through and calculate the output
[00:30:06 - 00:30:11] for each value of n using the difference equation.
[00:30:11 - 00:30:15] So here we'll use the example of the two sample moving average.
[00:30:15 - 00:30:20] So half x of n plus half of x of n minus 1.
[00:30:20 - 00:30:32] That's quite a time consuming process because you get
[00:30:32 - 00:30:36] y of n then you've got to calculate y of the x, y of n.
[00:30:36 - 00:30:44] As it's quite an iterative process, we could also calculate y of n
[00:30:44 - 00:30:50] if we know the input and the transfer function.
[00:30:50 - 00:30:54] This would then be, if we go to the z domain,
[00:30:54 - 00:31:01] this is in the inverse z transform of the z transform of the output
[00:31:01 - 00:31:07] x of z times the transfer function in the z domain.
[00:31:07 - 00:31:17] Okay, or thirdly we can get the output of our filter
[00:31:17 - 00:31:26] by convolving the input x of n with the impulse response
[00:31:26 - 00:31:36] h of n.
[00:31:36 - 00:31:40] Okay, so those are three equivalent ways to do it
[00:31:40 - 00:31:44] and computationally they are all different.
[00:31:44 - 00:31:50] Okay, so yes.
[00:31:50 - 00:32:10] That's a good question.
[00:32:10 - 00:32:14] So it depends on your architecture and things as well.
[00:32:14 - 00:32:20] And yes, it's hard to give a precise answer
[00:32:20 - 00:32:24] for how the overheads are doing the inverse z transform.
[00:32:24 - 00:32:28] And if you're looking up from a table,
[00:32:28 - 00:32:35] it's probably not too bad, but the tables are for fewer
[00:32:35 - 00:32:37] signals rather than with noise as well.
[00:32:37 - 00:32:43] So I don't think you'd actually do the second method
[00:32:43 - 00:32:47] in reality.
[00:32:47 - 00:32:49] We're going to look at the third method,
[00:32:49 - 00:32:56] which is actually done in the convolution.
[00:32:56 - 00:33:01] Okay, so let's do some examples here.
[00:33:01 - 00:33:11] So on the left hand side we've got our input
[00:33:11 - 00:33:15] and in the middle we've got our impulse response
[00:33:15 - 00:33:20] h of n and on the right we've got our,
[00:33:20 - 00:33:32] okay, so we can convolve these in each case to get.
[00:33:32 - 00:33:35] So the input in each case is the same.
[00:33:35 - 00:33:37] We've got this rectangular function.
[00:33:37 - 00:33:49] Okay, so what type of filter is the top one?
[00:33:49 - 00:33:54] Yeah.
[00:33:54 - 00:33:57] Yes, this is a moving average.
[00:33:57 - 00:34:01] So it's a two sample moving average.
[00:34:01 - 00:34:04] So this is an FIR filter.
[00:34:04 - 00:34:08] And so here we're taking the, we'll get in the average,
[00:34:08 - 00:34:12] which is one, but you kind of get a transient effect
[00:34:12 - 00:34:21] at the edge because you've got zeros coming in and out at the end.
[00:34:21 - 00:34:25] Okay, so for the second one,
[00:34:25 - 00:34:34] what can we say about this impulse response here?
[00:34:34 - 00:34:40] Yes, it's recursive or infinite impulse response.
[00:34:40 - 00:34:53] And so it's an FIR and the first one and what it's doing
[00:34:53 - 00:34:56] is taking a moving average.
[00:34:56 - 00:35:02] What is the second filter, the ZIAR filter,
[00:35:02 - 00:35:14] doing to our signal in this moving average?
[00:35:14 - 00:35:24] So we're starting off with a school year signal here.
[00:35:24 - 00:35:26] And so with a school year signal,
[00:35:26 - 00:35:29] you get really high frequencies at the edges
[00:35:29 - 00:35:31] because you're changing quickly.
[00:35:31 - 00:35:33] Whereas our output is quite smooth.
[00:35:33 - 00:35:38] So this is then some sort of low pass filter.
[00:35:38 - 00:35:42] So it's getting rid of the high frequencies.
[00:35:42 - 00:35:45] All right, yeah, you know, yeah, you will get to that,
[00:35:45 - 00:35:47] because that's a special one.
[00:35:47 - 00:35:49] Okay.
[00:35:49 - 00:35:53] So we'll do the bottom row now.
[00:35:53 - 00:35:56] And so in this, the bottom row, a FIR impulse response
[00:35:56 - 00:35:58] or an infinite impulse response.
[00:35:58 - 00:36:01] Finer, yeah, so we've just got two samples again.
[00:36:01 - 00:36:08] Okay, but what is that filter doing to our rectangular function?
[00:36:08 - 00:36:13] Yeah, exactly.
[00:36:13 - 00:36:16] So it's a what mathematical process is a year.
[00:36:16 - 00:36:27] Yeah, it's essentially, yeah.
[00:36:27 - 00:36:28] So it's called the differentiator,
[00:36:28 - 00:36:30] but that's great in this derivative.
[00:36:30 - 00:36:33] So, yeah, so this is a differentiator,
[00:36:33 - 00:36:36] differentiator, differentiator.
[00:36:36 - 00:36:38] Okay, so when you get, and the input,
[00:36:38 - 00:36:40] you get a large spike here.
[00:36:40 - 00:36:41] So it's going up.
[00:36:41 - 00:36:44] And then it's constant along the top.
[00:36:44 - 00:36:47] So the derivative along the top zero.
[00:36:47 - 00:36:50] And then when we had the last sample next then,
[00:36:50 - 00:36:51] we've got the falling edge.
[00:36:51 - 00:36:56] And so we're getting a negative value for our last value
[00:36:58 - 00:36:59] of what I've been.
[00:36:59 - 00:37:08] So, my interesting thing here is you can define,
[00:37:08 - 00:37:13] you know, mathematical filters with just two coefficients
[00:37:13 - 00:37:16] in the derivative with two coefficients.
[00:37:16 - 00:37:20] And similarly, you can do it on a greater as well.
[00:37:20 - 00:37:28] Okay, so we'll delve into convolution a little bit more.
[00:37:28 - 00:37:35] Okay, so our filter output,
[00:37:35 - 00:37:44] Y of n, is equal to X of n convolved with H of n.
[00:37:44 - 00:37:58] Okay, so can I write this as then H of n convolved with X of n?
[00:37:58 - 00:38:01] Can we swap the order out?
[00:38:01 - 00:38:02] Let me check the head.
[00:38:02 - 00:38:04] What, if you think about,
[00:38:05 - 00:38:09] in the Fourier domain, X of f, H of f,
[00:38:09 - 00:38:12] is equal to H of f X of f.
[00:38:12 - 00:38:21] In Fourier domain,
[00:38:21 - 00:38:25] we can swap the order of multiplication.
[00:38:25 - 00:38:29] So that means we can swap the order of our convolution to,
[00:38:29 - 00:38:34] so it is commutative.
[00:38:34 - 00:38:36] Amutative, diff.
[00:38:36 - 00:39:01] Okay, so then, just delve into the mathematics
[00:39:01 - 00:39:02] a little bit here on the Fourier.
[00:39:02 - 00:39:07] So we've got the output Y of n is equal to,
[00:39:09 - 00:39:10] in the general case,
[00:39:10 - 00:39:14] the sum from n is minus infinity to infinity.
[00:39:14 - 00:39:17] Our impulse response, H of n,
[00:39:17 - 00:39:21] our sample X of n delayed by n zapples.
[00:39:21 - 00:39:26] And so we can also swap the order around here
[00:39:26 - 00:39:32] so that we have the sum from n,
[00:39:32 - 00:39:37] minus infinity to infinity, our input X of n,
[00:39:37 - 00:39:47] and our impulse response H of n minus n.
[00:39:47 - 00:39:50] Okay, so for a causal filter,
[00:39:50 - 00:39:55] our impulse response is zero.
[00:39:55 - 00:40:00] Before we put the impulse into the circuit or the filter,
[00:40:00 - 00:40:03] we don't get any output.
[00:40:03 - 00:40:06] So H of n is equal to zero for n less than zero.
[00:40:06 - 00:40:15] Of course, theality means we can't have an output
[00:40:17 - 00:40:19] before we put in an input.
[00:40:19 - 00:40:25] And so that means that our output to our filter,
[00:40:26 - 00:40:33] Y of n is equal to the sum from little n to zero,
[00:40:35 - 00:40:39] to infinity, our impulse response H of n,
[00:40:39 - 00:40:44] and our input delayed by n samples.
[00:40:47 - 00:40:51] And if you wanted it right in terms of the other way around,
[00:40:51 - 00:40:55] it would be then a sum from n is minus infinity
[00:40:55 - 00:41:03] to n X of n,
[00:41:04 - 00:41:11] the impulse response H of n delayed by n samples.
[00:41:11 - 00:41:33] Okay, so we're gonna use the equation on the left hand side,
[00:41:33 - 00:41:38] the bottom one for calculating our filter output
[00:41:38 - 00:41:39] as a convolution.
[00:41:39 - 00:41:51] Okay, so for our output,
[00:41:53 - 00:41:58] the finite impulse response,
[00:41:58 - 00:42:03] we've got here a convolution Y of n is equal to the sum
[00:42:05 - 00:42:10] from n is zero to n minus one.
[00:42:10 - 00:42:16] So, the impulse response H of n times our input X of n
[00:42:17 - 00:42:23] to delay by n samples.
[00:42:23 - 00:42:30] Okay, so capital M is our extent of our impulse response
[00:42:33 - 00:42:36] so that's how many samples are,
[00:42:36 - 00:42:40] what the width of the non-zero samples,
[00:42:40 - 00:42:42] which is different to the number of non-zero samples
[00:42:42 - 00:42:45] because you might have a zero in the middle.
[00:42:45 - 00:42:51] So, is the distance between the widest distance
[00:42:51 - 00:42:53] between two non-zero samples?
[00:42:54 - 00:42:56] I'll show you your figure in a sec.
[00:42:56 - 00:43:00] So, if we do a couple of examples here,
[00:43:00 - 00:43:07] if our impulse response H of n is equal to 1, 2, 3,
[00:43:08 - 00:43:15] what is our extent equal to 3?
[00:43:15 - 00:43:17] Yeah, that's not a trick question.
[00:43:17 - 00:43:20] So, that's, so that's,
[00:43:20 - 00:43:24] but three samples, they're all non-zero.
[00:43:24 - 00:43:28] So, our span of non-zero samples is in three.
[00:43:28 - 00:43:31] So, now I'll give you the trick question.
[00:43:31 - 00:43:34] H of n is equal to,
[00:43:34 - 00:43:38] in this case say, zero, 1, zero, zero,
[00:43:39 - 00:43:43] two, three, zero,
[00:43:43 - 00:43:47] what's the extent of this?
[00:43:47 - 00:43:53] So, 1, 2, 3, 4, 5, yes, good.
[00:43:54 - 00:43:57] Okay, so, the zero's out here in ignore,
[00:43:57 - 00:44:01] so there are implied zeros before here
[00:44:01 - 00:44:04] and after here on the first one.
[00:44:05 - 00:44:08] And it's not the number of non-zero samples.
[00:44:08 - 00:44:12] So, we've got three values,
[00:44:12 - 00:44:15] the not zero in that impulse response.
[00:44:15 - 00:44:26] It's the span, which is then five from one across the three.
[00:44:26 - 00:44:34] Okay, and so then obviously the extent of the finite impulse response filter
[00:44:34 - 00:44:39] is finite and the extent of the infinite impulse response filter.
[00:44:39 - 00:44:43] There's infinite.
[00:44:43 - 00:44:53] Okay, so that's why they are so called.
[00:44:53 - 00:44:56] Okay, so when we do a convolution,
[00:44:56 - 00:44:58] and so this is an example on the bottom right,
[00:44:58 - 00:45:00] that we looked at before with the moving average,
[00:45:00 - 00:45:03] it broadens the extent of the signal.
[00:45:03 - 00:45:08] Okay, so in this convolution,
[00:45:08 - 00:45:14] we have our input here has an extent equal to,
[00:45:14 - 00:45:19] four, yep, good, let's make sure you're still awake.
[00:45:19 - 00:45:23] The extent of our impulse response here is two,
[00:45:23 - 00:45:30] and so the extent of our output now is five, good.
[00:45:30 - 00:45:33] So, let's write an equation,
[00:45:33 - 00:45:40] so if we have our output y of n is equal to our input
[00:45:40 - 00:45:44] x of n convolved by our impulse response h of n,
[00:45:44 - 00:45:53] our extent of y of n,
[00:45:53 - 00:46:01] I'm going to guess an equation for what the extent of the output is equal to.
[00:46:01 - 00:46:11] That is correct for this example,
[00:46:11 - 00:46:16] but it's not, if we had them wider,
[00:46:16 - 00:46:27] so it's extended this one,
[00:46:27 - 00:46:29] four plus the extent of this one,
[00:46:29 - 00:46:32] two, and then fact way one.
[00:46:32 - 00:46:36] So, I'll just run it down so we have the extent.
[00:46:36 - 00:46:58] y of n is equal to the extent of output x of n plus the extent of h of n minus one.
[00:46:58 - 00:47:18] So, this example we have extent of y of n to x of n convolved with h of n,
[00:47:18 - 00:47:24] this is an extent of five,
[00:47:24 - 00:47:26] the extent of four,
[00:47:26 - 00:47:31] the extent of two minus one.
[00:47:31 - 00:47:51] So, before we do a convolution of our input signal with a digital filter,
[00:47:51 - 00:48:01] we know in advance how long the output is going to be.
[00:48:01 - 00:48:06] So, the cable is going to be less than the power of the output.
[00:48:06 - 00:48:09] So, we'll just start on convolution,
[00:48:09 - 00:48:16] then we'll carry on on Wednesday.
[00:48:16 - 00:48:18] So, we'll just do,
[00:48:18 - 00:48:20] write the equation at the top,
[00:48:20 - 00:48:26] y of n is equal to the sum from n to zero,
[00:48:26 - 00:48:28] take minus one,
[00:48:28 - 00:48:32] our impulse response h convolved with our input in.
[00:48:32 - 00:48:37] So, what our input is of three samples,
[00:48:37 - 00:48:40] one, two, and one,
[00:48:40 - 00:48:41] and I mean,
[00:48:41 - 00:48:46] unlike the one that indicates where n is equal to zero,
[00:48:46 - 00:49:01] and our impulse response h of n is equal to one, two, three.
[00:49:01 - 00:49:15] We're going to swap those around.
[00:49:15 - 00:49:17] So, we've got,
[00:49:17 - 00:49:20] let's have our impulse response h of n to be symmetric,
[00:49:20 - 00:49:23] and our input is one, two, three.
[00:49:23 - 00:49:38] Okay, so let's finish this off on Wednesday,
[00:49:38 - 00:49:42] rather than get halfway through a calculation,
[00:49:42 - 00:49:46] and then we'll finish off the rest of the digital filters on Wednesday,
[00:49:46 - 00:49:50] hopefully, and then we'll go into sampling and discrete for our transforms,
[00:49:50 - 00:49:53] and then the last week we'll look at different types of sensors.
[00:49:53 - 00:49:55] So, now our radar and things.
[00:49:55 - 00:49:57] Okay, finish your report, so go your weekend,
[00:49:57 - 00:49:59] and I'll see you on Wednesday.

# ENMT301-26W Lecture 63 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `daeb6721404b0701ad1674ac4c39e89ef35b86b3871ed5323f084b982c402c67`
Generated: 2026-06-06T07:22:27.777314+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:11 - 00:00:13] Okay, good afternoon everyone.
[00:00:14 - 00:00:16] What's due today?
[00:00:16 - 00:00:17] Nothing.
[00:00:17 - 00:00:18] Well, let's take a fancy.
[00:00:18 - 00:00:31] Um, uh, okay.
[00:00:31 - 00:00:35] So the, um, the answer to the first question will be how many people are present at this
[00:00:35 - 00:00:38] lecture.
[00:00:38 - 00:00:41] There's a joke for everyone at home.
[00:00:41 - 00:00:45] Okay.
[00:00:45 - 00:00:54] So, um, yeah, so, uh, we've looked at different, um, versions of the Fourier transform.
[00:00:54 - 00:00:58] So we'll just go through those all now and then we'll look at the discrete Fourier transform.
[00:00:58 - 00:01:05] So we'll start off with the Fourier series, which if we have a periodic, uh, continuous
[00:01:05 - 00:01:09] time signal, so we looked at a triangle wave and the square wave, the Fourier series
[00:01:09 - 00:01:12] then breaks it down into the different harmonic frequencies.
[00:01:12 - 00:01:15] So that's a discrete frequency spectrum.
[00:01:15 - 00:01:24] So basically with these Fourier transforms, if we are, uh, periodic in one domain, we then
[00:01:24 - 00:01:26] become discrete in the other domain.
[00:01:26 - 00:01:28] Okay.
[00:01:28 - 00:01:30] And it goes back the other way as well.
[00:01:30 - 00:01:37] Um, and so then we looked at the continuous Fourier transform, which is the Fourier transform
[00:01:37 - 00:01:42] of a continuous signal and that gives us a continuous spectrum.
[00:01:42 - 00:01:50] So in these figures that dots around the boxes, uh, discrete.
[00:01:50 - 00:01:55] Okay.
[00:01:55 - 00:01:59] And then we looked at the discrete time Fourier transform, the dt ft.
[00:02:02 - 00:02:04] So now we have a discrete time signal.
[00:02:04 - 00:02:07] So a signal has been sampled.
[00:02:07 - 00:02:16] And the dt ft gives us a continuous spectrum, but that spectrum becomes periodic from the
[00:02:16 - 00:02:17] sampling process.
[00:02:17 - 00:02:21] So, and that's what then gives us our only thing.
[00:02:21 - 00:02:22] So we was the example.
[00:02:22 - 00:02:27] So this one here, this is showing the discrete time Fourier transform.
[00:02:28 - 00:02:31] So the top one is the continuous Fourier transforms.
[00:02:31 - 00:02:36] We just get one copy of our spectrum.
[00:02:36 - 00:02:42] But when we take the discrete time Fourier transform, we end up with the spectrum repeating
[00:02:42 - 00:02:50] this period of the sampling frequency.
[00:02:50 - 00:02:51] Okay.
[00:02:51 - 00:02:54] And so then lastly, we'll look at today.
[00:02:54 - 00:03:01] Now is the discrete Fourier transform where we have our sample signal.
[00:03:01 - 00:03:08] And then the dft gives us a discrete spectrum.
[00:03:08 - 00:03:09] Okay.
[00:03:09 - 00:03:18] And then the spectrum and the time signal are assumed to be periodic as well.
[00:03:18 - 00:03:22] Okay.
[00:03:22 - 00:03:28] So let's go through the definition of the dft.
[00:03:28 - 00:03:29] Okay.
[00:03:29 - 00:03:34] So we have then our dft is defined.
[00:03:35 - 00:03:38] So the square bracket here.
[00:03:38 - 00:03:44] So the spectrum, capital X of K is discrete as well.
[00:03:44 - 00:03:49] And so this is the same sort of form as the Fourier transform, but it's the discrete.
[00:03:49 - 00:03:54] So we have some over all our samples.
[00:03:54 - 00:04:04] So we've got n samples, capital n samples of our sample value X then.
[00:04:04 - 00:04:16] multiplied by our complex exponential e to the minus j2 pi k little n over capital n.
[00:04:16 - 00:04:21] So little n is the counter for our sample signal.
[00:04:21 - 00:04:27] And little k is the counter for our spectrum.
[00:04:27 - 00:04:38] And so if we have n samples of our sample and the time domain, our spectrum and the frequency domain will also be of length, capital n.
[00:04:38 - 00:04:44] Okay.
[00:04:44 - 00:04:51] And because we have it discrete and the time domain, X of k becomes periodic.
[00:04:51 - 00:05:00] And because X of k is also discrete, then X of n becomes periodic and the time domain as well.
[00:05:00 - 00:05:03] Okay.
[00:05:03 - 00:05:08] So this period, this period, this period is then capital n.
[00:05:08 - 00:05:19] So our spectrum, it's an n plus k is equal to X of K.
[00:05:19 - 00:05:26] So the spectrum repeats every n samples.
[00:05:26 - 00:05:38] And then if we want to look at negative frequencies, X of minus k is equal to X of n minus k.
[00:05:38 - 00:05:47] And if we add in here on left hand side, we get X of n minus k.
[00:05:47 - 00:05:53] So spectrum is repeating with a period in the number of samples we have.
[00:05:53 - 00:06:02] And so when we looked at the continuous Fourier transform, if we were considering a real signal.
[00:06:02 - 00:06:04] So not with complex values.
[00:06:04 - 00:06:11] Then the negative frequencies have conjugate or Hermitian symmetry with the positive frequencies.
[00:06:11 - 00:06:17] That means the magnitude of the negative frequencies is the same as the magnitude of the positive frequencies.
[00:06:17 - 00:06:24] And the phase of the negative frequencies is the negative of the phase of the positive frequencies.
[00:06:24 - 00:06:29] So we've got a real sequence, a real signal with continuous Fourier transform.
[00:06:29 - 00:06:35] And we know the positive spectrum, we can then work out the negative spectrum from period to C.
[00:06:35 - 00:06:39] And so the same principle applies for the DFT.
[00:06:39 - 00:06:42] So we've got a real sequence, X of n.
[00:06:42 - 00:06:45] X of K has conjugate symmetry.
[00:06:45 - 00:07:01] So the value of X of k is equal to the complex conjugate X star of n minus k.
[00:07:01 - 00:07:06] And so from the line above, X minus k is the same as X of minus k.
[00:07:06 - 00:07:21] So the negative frequency value, the negative frequencies the DFT is the complex conjugate of the positive frequencies.
[00:07:21 - 00:07:33] Yes.
[00:07:33 - 00:07:40] Well, so if you were doing this on a computer and you were doing the inverse DFT,
[00:07:40 - 00:07:43] you have to include the negative frequencies in there.
[00:07:43 - 00:07:48] Otherwise you're truncating half of it, so you won't get when you do the DFT.
[00:07:48 - 00:07:50] You wouldn't get the positive.
[00:07:50 - 00:07:54] When you didn't get that signal the time it made back.
[00:07:54 - 00:07:55] Yeah.
[00:07:55 - 00:07:57] So you do need to include that as a...
[00:07:57 - 00:07:58] Yeah.
[00:07:58 - 00:08:02] And the computation.
[00:08:02 - 00:08:03] Yeah.
[00:08:03 - 00:08:09] And so also, if you're actually doing this on a computer,
[00:08:09 - 00:08:12] you've got a signal and you can put in the DFT of it.
[00:08:12 - 00:08:16] You don't need to calculate all the X of k into half of it,
[00:08:16 - 00:08:18] and then use the symmetry to calculate the other half.
[00:08:18 - 00:08:22] Okay.
[00:08:22 - 00:08:27] So let's then calculate the DFT of sequence.
[00:08:27 - 00:08:29] So we'll just do a little...
[00:08:29 - 00:08:30] Short little sequence.
[00:08:30 - 00:08:42] So X of n, our sequence is 2, 3, 1, 4.
[00:08:42 - 00:08:46] And so we've got 4 values that capital n is 4.
[00:08:46 - 00:08:51] And so the length of our spectrum, capital X of k,
[00:08:51 - 00:08:53] will also be 4.
[00:08:53 - 00:08:59] Okay.
[00:08:59 - 00:09:01] So the general equation up here,
[00:09:01 - 00:09:02] so we can refer to that.
[00:09:02 - 00:09:10] So X of k is equal to some inner 0 to n minus 1, X of n,
[00:09:10 - 00:09:18] e to the minus j to pi k in over n.
[00:09:18 - 00:09:19] Okay.
[00:09:19 - 00:09:22] So let's start off with X of 0.
[00:09:22 - 00:09:35] So we've got the sum then of from n is 0 to n minus 1 of X of n.
[00:09:35 - 00:09:42] So here we're looking at k is equal to 0.
[00:09:42 - 00:09:48] So when we do this, e to the minus j to pi k in business,
[00:09:48 - 00:09:52] we've got in here, okay, is 0.
[00:09:52 - 00:09:56] So we then get e to the 0.
[00:09:56 - 00:09:59] What's e to the 0, 1?
[00:09:59 - 00:10:00] Okay.
[00:10:00 - 00:10:02] So then this is just X of n times 1.
[00:10:02 - 00:10:05] So this then just becomes the sum,
[00:10:05 - 00:10:10] e to the minus 1 of X of n.
[00:10:10 - 00:10:15] So this is just the sum of our values,
[00:10:15 - 00:10:21] 2 plus 3 plus 1 plus 4, which is 10.
[00:10:21 - 00:10:25] So the first value of the spectrum,
[00:10:25 - 00:10:28] is essentially the DC value.
[00:10:28 - 00:10:36] This is depending how you define your DFT.
[00:10:36 - 00:10:40] Here, this is the total value of the spectrum.
[00:10:40 - 00:10:45] Some people have in the definition of the DFT,
[00:10:45 - 00:10:50] 1 over n here, and then that would be the DC value of the average value.
[00:10:50 - 00:10:55] The definition I'm using of the DFT has the 1 over n on the inverse,
[00:10:55 - 00:11:01] the script for a transform, not on the forward going DFT.
[00:11:01 - 00:11:06] Some matching what NumPy and Python does,
[00:11:06 - 00:11:12] but interestingly in my ENI or 420 signal processing course,
[00:11:12 - 00:11:16] I've got the 1 over n on the forward transform,
[00:11:16 - 00:11:18] not on the reverse transform.
[00:11:18 - 00:11:20] So you need it one way or the other.
[00:11:20 - 00:11:24] And I think MATLAB does 1 over the square root of n on both the forward
[00:11:24 - 00:11:26] and the reverse transforms.
[00:11:26 - 00:11:32] So there are three different ways at least to define the DFT,
[00:11:32 - 00:11:34] in terms of scaling within.
[00:11:34 - 00:11:39] Anyway, the exon0 is simple to compute,
[00:11:39 - 00:11:45] because we're just adding up the sequence values.
[00:11:45 - 00:11:49] Let's do the next one, which will be a bit more complicated.
[00:11:49 - 00:11:52] The exon1, so this is considering k is equal to 1.
[00:11:52 - 00:11:56] So this is the sum from little in 0,
[00:11:56 - 00:12:06] in minus 1 of x of n, e to the minus,
[00:12:06 - 00:12:07] okay, is 1.
[00:12:07 - 00:12:17] So it becomes e to the minus j to pi in over 4.
[00:12:17 - 00:12:20] Okay, so our first sequence value is 2,
[00:12:20 - 00:12:26] and then we've got, for the first sequence we've got in 0,
[00:12:26 - 00:12:29] this is e of j times 0.
[00:12:29 - 00:12:32] Our second sequence value is 3.
[00:12:32 - 00:12:41] Here in this one we've got e to the minus j pi over 2.
[00:12:41 - 00:12:44] Our third one is 1 times,
[00:12:44 - 00:12:47] so we're in as 2 now,
[00:12:47 - 00:12:54] so we end up with e to the minus j pi.
[00:12:54 - 00:12:58] And then the last term is 4,
[00:12:58 - 00:13:02] and in is 3,
[00:13:02 - 00:13:04] so 3 times 2 is 6,
[00:13:04 - 00:13:09] so we get e to the minus j 3 pi.
[00:13:09 - 00:13:19] Okay, so e to the 0 is 1,
[00:13:19 - 00:13:24] so we've got 2,
[00:13:24 - 00:13:31] e to the minus j pi over 2.
[00:13:31 - 00:13:35] I think we're axes, we're going down 90 degrees,
[00:13:35 - 00:13:39] so that becomes, yeah,
[00:13:39 - 00:13:42] I'm using j's, but so this should be a,
[00:13:42 - 00:13:45] get real at plus, and make it a,
[00:13:45 - 00:13:47] and then get it,
[00:13:47 - 00:13:53] so it's minus 3 j.
[00:13:53 - 00:13:57] Okay, so 2 minus 3 j,
[00:13:57 - 00:14:01] what's e to the minus j pi,
[00:14:01 - 00:14:03] it's all around pi,
[00:14:03 - 00:14:06] end up at minus 1.
[00:14:06 - 00:14:09] Yep, so we end up minus 1,
[00:14:09 - 00:14:14] then e to the minus j 3 pi over 2,
[00:14:14 - 00:14:17] that's going right round,
[00:14:17 - 00:14:19] so it's plus j times 4,
[00:14:19 - 00:14:21] so we'll get plus 4 j.
[00:14:21 - 00:14:28] This is then equal to 1 plus j.
[00:14:28 - 00:14:37] Halfway there,
[00:14:37 - 00:14:38] we'll do a trick for the last one.
[00:14:38 - 00:14:41] Okay, so spectrum x of 2,
[00:14:41 - 00:14:43] this is for k is 2,
[00:14:43 - 00:14:49] some inner zero,
[00:14:49 - 00:14:51] n minus 1,
[00:14:51 - 00:14:55] x of n,
[00:14:55 - 00:14:57] e to the minus j,
[00:14:57 - 00:15:00] or pi in,
[00:15:00 - 00:15:01] over 4,
[00:15:01 - 00:15:06] I'll just write this out this time,
[00:15:06 - 00:15:07] rather than asking questions,
[00:15:07 - 00:15:09] so 2, e to the j,
[00:15:09 - 00:15:16] 0, 3, e to the minus j pi
[00:15:16 - 00:15:19] plus 1, e to the j,
[00:15:19 - 00:15:26] 2 pi to the minus j,
[00:15:26 - 00:15:27] 3 pi,
[00:15:27 - 00:15:32] so this is equal to 2 minus 3,
[00:15:32 - 00:15:35] plus 1 minus 4,
[00:15:35 - 00:15:38] which gives us minus 4,
[00:15:38 - 00:15:42] let you catch up,
[00:15:42 - 00:15:44] and then we'll think about how to do
[00:15:44 - 00:15:46] capital X of 3,
[00:15:46 - 00:15:47] K is 3.
[00:15:47 - 00:16:19] Okay, so we could calculate
[00:16:19 - 00:16:21] capital X of 3,
[00:16:21 - 00:16:23] by going through and plugging in these numbers,
[00:16:23 - 00:16:26] plus how smart are we doing this?
[00:16:26 - 00:16:27] 100,000,000 of 1.
[00:16:27 - 00:16:29] Good, so x of 3 is equal to,
[00:16:29 - 00:16:34] complex conjugate of x of 1,
[00:16:34 - 00:16:36] so I'll just write the general form here,
[00:16:36 - 00:16:43] x of K is equal to x star of n minus k,
[00:16:43 - 00:16:50] so x of 3 is then equal to complex conjugate of 1,
[00:16:50 - 00:16:54] plus j is then 1 minus j,
[00:16:54 - 00:17:01] and our whole DFT x of K is equal to 10,
[00:17:01 - 00:17:06] 1 plus j minus 4,
[00:17:06 - 00:17:13] 1 minus j,
[00:17:13 - 00:17:15] and there will be,
[00:17:15 - 00:17:17] which is your next question,
[00:17:17 - 00:17:31] that you can practice that on yourself as well.
[00:17:31 - 00:17:33] Okay, moving along,
[00:17:33 - 00:17:38] let's have a look at the DFT in comparison to the DFT.
[00:17:38 - 00:17:47] Okay, so with the DFT,
[00:17:47 - 00:17:55] we have a period of our signal,
[00:17:55 - 00:17:58] so it's the number of sample points in,
[00:17:58 - 00:18:01] times the something period T,
[00:18:01 - 00:18:04] or the number n over our something frequency,
[00:18:04 - 00:18:05] Fs.
[00:18:05 - 00:18:11] Okay, so then we end up,
[00:18:11 - 00:18:14] so in the time to make the top figure here,
[00:18:14 - 00:18:19] the distance between our lower pops is capital T,
[00:18:19 - 00:18:30] or something period for the DFT,
[00:18:30 - 00:18:35] which is shown as the blue lollipop pops in the bottom figure.
[00:18:35 - 00:18:38] Our frequency resolution will call del for F,
[00:18:38 - 00:18:56] is equal to the something frequency divided by the number of samples in.
[00:18:56 - 00:19:06] Okay, and we could write this as well as one over the number of samples in times the something period T.
[00:19:06 - 00:19:11] So that gives us our sampling,
[00:19:11 - 00:19:18] or our resolution in our spectrum.
[00:19:18 - 00:19:22] Okay, so let's go through and work those out for.
[00:19:22 - 00:19:28] This example, so here we've got a 20 hertz cosine,
[00:19:28 - 00:19:33] an assembled at 500 hertz.
[00:19:33 - 00:19:38] This time is given here in milliseconds, 100 milliseconds.
[00:19:38 - 00:19:42] This is equal to 0.1 seconds.
[00:19:42 - 00:19:49] Okay, so first of all, let's calculate our number of sample points in.
[00:19:49 - 00:19:56] I'm going to guess how many lollipop's we've got there on the top of the figure,
[00:19:56 - 00:20:04] or close 50, yeah,
[00:20:04 - 00:20:11] so we've got here we're doing 500 samples per second,
[00:20:11 - 00:20:18] and we've got 0.1 seconds, so in is 50.
[00:20:18 - 00:20:34] So then our resolution T is equal to 1 over 500,
[00:20:34 - 00:20:38] which is equal to 2 milliseconds,
[00:20:38 - 00:20:50] and our frequency resolution delta F,
[00:20:50 - 00:21:02] we had is the something frequency divided by the number of sample points we have.
[00:21:02 - 00:21:07] So that's that equal to 500 over 50,
[00:21:07 - 00:21:11] so delta F is equal to 10 hertz.
[00:21:11 - 00:21:24] Okay, so that checks out with our frequency spectrum on the bottom here.
[00:21:24 - 00:21:29] So the DFT we have a peak at the second point and blue,
[00:21:29 - 00:21:34] and that 10 hertz, so this one here is for if not,
[00:21:34 - 00:21:46] what is 20 hertz.
[00:21:46 - 00:21:50] Okay, so the bottom figure for our frequency spectrum,
[00:21:50 - 00:21:54] the blue lollipops are from the DFT,
[00:21:54 - 00:22:00] so it is just discrete values for our frequency spectrum,
[00:22:00 - 00:22:03] and the gray line is the discrete time for a transform,
[00:22:03 - 00:22:08] which is then continuous.
[00:22:08 - 00:22:12] Okay, so another note about that bottom flop for the frequency spectrum
[00:22:12 - 00:22:17] is that the DFT will spit out DC,
[00:22:17 - 00:22:19] then the positive frequencies,
[00:22:19 - 00:22:21] then it will give the negative frequencies.
[00:22:21 - 00:22:26] So this point here towards the end is at minus 20 hertz.
[00:22:26 - 00:22:37] Okay, so this is a little bit confusing to look at having the periodicity shown that way,
[00:22:37 - 00:22:45] so what is typically done is to then move the negative frequencies
[00:22:45 - 00:22:54] with a shift so that the central the DC turn is in the middle.
[00:22:54 - 00:23:01] So this is the same time signal and frequency spectrum as the previous slide,
[00:23:01 - 00:23:09] but we've used the FFT shift operator.
[00:23:09 - 00:23:20] This is a function in both Numpy, Python or in Matlab.
[00:23:20 - 00:23:23] Okay, so now we've got the negative frequencies on the left,
[00:23:23 - 00:23:25] DC in the middle, positive frequencies on the right,
[00:23:25 - 00:23:27] so this one here is minus 20 hertz.
[00:23:27 - 00:23:30] This one here is 20 hertz.
[00:23:30 - 00:23:34] So now I find that easier to visualize.
[00:23:34 - 00:23:41] So the shift is just making use of the periodicity of the DFT,
[00:23:41 - 00:23:49] whereby the negative spectrum values are equal to x, then minus k.
[00:23:49 - 00:24:22] Okay, now we're going to look at something called zero padding,
[00:24:22 - 00:24:27] which we can do in either the time domain or the frequency domain,
[00:24:27 - 00:24:30] and they do slightly different things,
[00:24:30 - 00:24:39] but they're both used to increase the resolution of either our signal or the spectrum.
[00:24:39 - 00:24:44] So here we've got the same signal as the previous one,
[00:24:44 - 00:24:54] so we've got a cosine of 20 hertz with got a sub-infregnancy of 500 hertz,
[00:24:54 - 00:25:01] and our originally we've got N is 50 points.
[00:25:01 - 00:25:05] Examples.
[00:25:05 - 00:25:08] Okay, so this is our x of N at the top,
[00:25:08 - 00:25:16] and so what we can do is the zero padding is we're going to add another N is 50 zeros.
[00:25:16 - 00:25:25] So we're just going to add a whole bunch of zeros to the end of our signal.
[00:25:25 - 00:25:34] Okay, so these have just been inserted before we do our discrete Fourier transform.
[00:25:34 - 00:25:44] Okay, so the bottom here we've got the magnitude of our spectrum,
[00:25:44 - 00:25:58] and so the loy pops shown in blue at the bottom are the DFT we had previously.
[00:25:58 - 00:26:03] So here we're just showing the positive frequencies.
[00:26:03 - 00:26:17] Okay, and I'll just change the color of the black.
[00:26:17 - 00:26:37] Okay, so now in black the loy pops are the spectrum values from those additional samples,
[00:26:37 - 00:26:58] from those zeros.
[00:26:58 - 00:27:05] Okay, so adding a whole bunch of zeros to our signal when we do the inverse discrete Fourier transform,
[00:27:05 - 00:27:12] sorry, the discrete Fourier transform, that then gives us increased resolution.
[00:27:12 - 00:27:26] Okay, so before in blue we had delta F was F s over N,
[00:27:26 - 00:27:34] since 500 over 50 was 10 hertz.
[00:27:34 - 00:27:41] Okay, so delta F and blue was 10 hertz.
[00:27:41 - 00:27:56] Now if we zero pad new resolution of our spectrum,
[00:27:56 - 00:28:00] that includes both the blue loy pops and the black loy pops,
[00:28:00 - 00:28:10] it is equal to the sampling frequency divided by the total number of samples.
[00:28:10 - 00:28:15] So that was our original 50 points in plus the 50 zeros I added.
[00:28:15 - 00:28:21] So this is then 500 over 100 equals 5 hertz.
[00:28:21 - 00:28:25] Okay, so now after the zero padding,
[00:28:25 - 00:28:34] our delta F is equal to 5 hertz.
[00:28:34 - 00:28:41] Okay, so zero padding of our signal and the time domain increases the resolution of our spectrum
[00:28:41 - 00:28:42] in the frequency domain.
[00:28:42 - 00:28:58] Okay, so the cost of that is the computation of taking a larger DFT,
[00:28:58 - 00:29:10] but we're winning in terms of frequency resolution.
[00:29:10 - 00:29:13] Okay, so this adding zeros in the time domain.
[00:29:13 - 00:29:23] Next we'll look and see what happens if we add zeros in the frequency domain.
[00:29:23 - 00:29:30] Okay, so here we've got, so this is our original spectrum here of the different case.
[00:29:30 - 00:29:35] We've got a sine wave, and so I've got 32 points here.
[00:29:35 - 00:29:39] So N is equal to 32 points.
[00:29:39 - 00:29:46] Okay, so this is here X of K,
[00:29:46 - 00:29:53] the magnitude of X of K, and I'm going to add another 32 zeros.
[00:29:53 - 00:29:59] So I'll put them here and here.
[00:29:59 - 00:30:05] So 16 zeros here and 16 zeros here.
[00:30:05 - 00:30:12] So adding total 32 zeros.
[00:30:12 - 00:30:30] Okay, so our sample spectrum here and orange corresponds to the sine wave and orange on the right.
[00:30:30 - 00:30:38] When we add zeros to the spectrum and take the inverse discrete Fourier transform,
[00:30:38 - 00:30:48] sort of zero padded in the frequency domain, that then increases the resolution of our signal in the time domain.
[00:30:48 - 00:31:08] Okay, so this is then interpolation in a particular becomes sink interpolation,
[00:31:08 - 00:31:16] which is the perfect interpolator, according to the Nyquist-Chenon theorem.
[00:31:16 - 00:31:28] Okay, so I'll just write a note on here.
[00:31:28 - 00:31:50] So we can see that the orange is the original samples and is the interpolated samples.
[00:31:50 - 00:31:58] Okay, so when you do this in this discrete Fourier transform, you get both the blue ones and the orange ones back.
[00:31:58 - 00:32:03] Okay, so if we want to interpolate our signal, our sample signal,
[00:32:03 - 00:32:06] is the same Nyquist sample.
[00:32:06 - 00:32:13] So rather than twice the sampling frequency, we can take the discrete Fourier transform.
[00:32:13 - 00:32:16] We can add a whole bunch of zeros to the spectrum.
[00:32:16 - 00:32:35] Take the inverse discrete Fourier transform and then we've got interpolation.
[00:32:35 - 00:32:36] Okay, moving along.
[00:32:36 - 00:32:46] So we have, I probably should have defined the inverse discrete Fourier transform before I talk about it.
[00:32:46 - 00:32:50] But anyway, mathematically, the inverse discrete Fourier transform,
[00:32:50 - 00:32:56] so we're getting our signal x of n back from our spectrum.
[00:32:56 - 00:33:04] So it's the same sort of form as the Fourier transform, so we're doing a sum from k0 to n minus 1.
[00:33:04 - 00:33:11] Of our spectrum values, k over x of k, and we multiply by a complex exponential,
[00:33:11 - 00:33:17] I need to use the j to get k in over that n.
[00:33:17 - 00:33:33] And so the difference to the four guy spectrum is that this is a positive complex exponential rather than negative one.
[00:33:33 - 00:33:37] And then definition I'm using, we've got the scale factor 1 over n.
[00:33:37 - 00:34:22] So as I said previously, you could put the 1 over n on the four transform and then you wouldn't have it on the inverse transform.
[00:34:22 - 00:34:27] Okay, moving along.
[00:34:27 - 00:34:34] Okay, so we have our signal.
[00:34:34 - 00:34:39] So it's called our signal x-n.
[00:34:39 - 00:34:50] And for the DFT, we're effectively considering a portion of that signal.
[00:34:50 - 00:34:55] So we're multiplying it by some windowing function w of n.
[00:34:55 - 00:35:08] And that's giving us our truncated signal x-n that we're going to take the discrete Fourier transform off.
[00:35:08 - 00:35:21] Okay, so top here we've got a cosine x-n, we've got, in this case we've got our window function is essentially a rec function.
[00:35:21 - 00:35:27] So a rectangle window.
[00:35:27 - 00:35:48] And the bottom we've got the product of x-n with w-n, which is given our truncated.
[00:35:48 - 00:35:54] Okay, so this example, I've got 100 points.
[00:35:54 - 00:35:58] Something frequency is 500 hertz.
[00:35:58 - 00:36:13] And the frequency of the sine cosine wave here is 20 hertz.
[00:36:13 - 00:36:24] So in the time domain here, we are multiplying by a window function when we do in this truncation.
[00:36:24 - 00:36:26] So what's happening in the frequency domain?
[00:36:26 - 00:36:37] Well, for multiplying the time domain, it's convolution in the frequency domain.
[00:36:37 - 00:36:39] So then what's going to happen?
[00:36:39 - 00:36:53] Well, the next slide we're going to be convolving our true spectrum, the cosine, with the spectrum of the window.
[00:36:53 - 00:36:56] So for a rectangle before we transform that's a sine.
[00:36:56 - 00:37:03] So we're going to be convolving our spectrum with a sine function.
[00:37:03 - 00:37:12] So in the frequency domain we have, so right this in terms of the discrete time Fourier transform.
[00:37:12 - 00:37:25] So the frequency spectrum of our truncated signal, the capital G of F, is equal to the frequency spectrum of our input signal.
[00:37:25 - 00:37:42] X of F convolved with frequency spectrum of our window function.
[00:37:42 - 00:37:55] Okay, so here we've got these figures, this is frequency and hertz.
[00:37:55 - 00:38:05] And so this was at 20 hertz and minus 20 hertz was our frequency of our cosine wave.
[00:38:05 - 00:38:17] So here we've got nice deltas, plus minus the frequency of our cosine wave.
[00:38:17 - 00:38:25] But the DFT with this truncation by our rectangular function.
[00:38:25 - 00:38:38] So we've got in the time domain we had rectivin and that's going to go to a sink of F.
[00:38:38 - 00:38:48] And so what we're going to see then in the frequency domain is that we have, instead of a nice delta peak,
[00:38:48 - 00:39:01] we now have a wider main lobe, this is called the main sort of part of from the sink.
[00:39:01 - 00:39:09] And then we also have these side lobes appearing as well.
[00:39:09 - 00:39:35] Okay, so this is called spectral leakage that by truncating our signal, we then have leakage from the true frequency to surrounding frequencies.
[00:39:35 - 00:39:45] So it's even nice sharp delt function here as then become blurred out over a range of frequencies between then.
[00:39:45 - 00:39:49] I know what's that, 10 and 30 hertz.
[00:39:49 - 00:39:59] Plus we're also seeing these side lobes of the sink function.
[00:39:59 - 00:40:13] Okay, so it turns out that this inherent multiplying by rectangular function that we have when we truncate a signal to the DFT is probably not the best way of doing it.
[00:40:13 - 00:40:19] And there are different window functions that we can use that will then give us better properties in the frequency domain.
[00:40:19 - 00:40:36] Okay, so if we're truncating with the rectangular function, so we're just abruptly stopping our signal before we do the DFT, we get these large side lobes.
[00:40:36 - 00:40:41] And then those might hide other frequency components of our spectrum.
[00:40:41 - 00:40:46] And so it can be better to use a smoother window function.
[00:40:46 - 00:41:09] So we multiply our signal x of n by the z input by a window function w of n, and that gives us our window input.
[00:41:09 - 00:41:27] And we do that before we take the discrete Fourier transform to try and reduce the effects of these side lobes from the rectangular function.
[00:41:27 - 00:41:32] So common window that is used is something that is the having window.
[00:41:32 - 00:41:50] So w of n is then defined as a constant 0.54 minus scalar 0.46 times a cosine 2 pi little in over the number of samples capital in.
[00:41:50 - 00:41:59] So that produces a smoother window function.
[00:41:59 - 00:42:04] And we don't have this abrupt change of the rectangular window function.
[00:42:04 - 00:42:36] So I'll show a picture of what that looks like on the next slide once you're caught up.
[00:42:36 - 00:42:41] Okay, so let's look at the different window functions, both in the time domain and in the frequency domain.
[00:42:41 - 00:42:48] So the top we've got the time domain.
[00:42:48 - 00:42:53] And so our rectangle window is shown in blue.
[00:42:53 - 00:42:59] And then we've also shown this having one which is based on a cosine.
[00:42:59 - 00:43:01] It's a nice smooth one that's in green.
[00:43:01 - 00:43:05] And then I've also got two other types of triangular window.
[00:43:05 - 00:43:07] And let's go to a flat top window.
[00:43:07 - 00:43:14] Okay, and then the bottom we have the frequency response.
[00:43:14 - 00:43:22] So this builds all of each of those four windows.
[00:43:22 - 00:43:27] Okay, and so what we can say if we have a smoother window,
[00:43:27 - 00:43:38] let's say look at the having window.
[00:43:38 - 00:43:49] This then has lower side lobes of our window function and the frequency domain than the rectangular one.
[00:43:49 - 00:43:52] So these blue ones here are quite high compared to the green ones low.
[00:43:52 - 00:44:02] So this has got this ringing in the side lobes.
[00:44:02 - 00:44:07] Okay, so that's good.
[00:44:07 - 00:44:14] But we then have the trade off where we go the having window.
[00:44:14 - 00:44:19] We've actually got a wider main lobe than the rectangular function.
[00:44:19 - 00:44:29] It's not something we were particular once.
[00:44:29 - 00:44:38] So there's a trade off between suppressing the ripple in the side lobes and having a sharper peak from the main lobe.
[00:44:38 - 00:44:54] Okay, so let's just see a little example with this window function.
[00:44:54 - 00:45:00] So in this case here I've got two frequency components.
[00:45:00 - 00:45:06] So the larger one is at if not is 100 hertz.
[00:45:06 - 00:45:10] So it's got a large magnitude of 0.3.
[00:45:10 - 00:45:11] 0.3 sorry.
[00:45:11 - 00:45:15] And then we've got a smaller one here,
[00:45:15 - 00:45:21] we'll call if one, and that's at 120 hertz, 125 hertz.
[00:45:21 - 00:45:32] So the magnitude of the 125 hertz is much lower.
[00:45:32 - 00:45:38] If we just take the DFT without any ringing, without any windowing, sorry.
[00:45:38 - 00:45:41] So effectively just using a rectangular window.
[00:45:41 - 00:45:50] These side lobes almost mask the peak at 125 hertz.
[00:45:50 - 00:45:52] So that's not good.
[00:45:52 - 00:45:57] But if we use this hamming window, so multiply by the smoother green function,
[00:45:57 - 00:46:04] before we take the district for a transform, we reduce the amount of ringing in the side lobes.
[00:46:04 - 00:46:09] And it's much easier to see the peak at 125 hertz in orange.
[00:46:09 - 00:46:10] So that's good.
[00:46:10 - 00:46:19] But we've paid the price that our main lobe with the orange curve is now wider than with the blue curve.
[00:46:19 - 00:46:23] In case we have spectral leakage at 100 hertz,
[00:46:23 - 00:46:30] we're kind of smearing the frequency content across more frequencies.
[00:46:30 - 00:46:39] But it's easier to detect a smaller peak with the window function.
[00:46:39 - 00:46:41] Or with a smoother window function.
[00:46:41 - 00:46:43] If you do nothing, you're still going windowing,
[00:46:43 - 00:46:46] because you're effectively got a rectangular window,
[00:46:46 - 00:46:52] convolving by a sink, and then you get a lot of ringing in the side lobes.
[00:46:52 - 00:46:57] Okay, so I think that's probably a good point to finish for today.
[00:46:57 - 00:47:01] Next week, we've probably got about half a dozen slides to continue on this here.
[00:47:01 - 00:47:03] I've passed very transforms and things.
[00:47:03 - 00:47:08] People do some stuff on different sensors.
[00:47:08 - 00:47:11] So we'll look at radar and lidar and sonar and things.
[00:47:11 - 00:47:15] And I'll also give a bit of a preview of the assignment as well.
[00:47:15 - 00:47:18] Which isn't due until the second week of...
[00:47:18 - 00:47:20] This is the two.
[00:47:20 - 00:47:22] So it's like two months away.
[00:47:22 - 00:47:25] But you don't see me again until...
[00:47:25 - 00:47:27] well, after the next week.
[00:47:27 - 00:47:31] So that's good to be able to explain that in your last questions.
[00:47:31 - 00:47:33] In the lecture.
[00:47:33 - 00:47:35] Okay, good to enjoy the weekend.
[00:47:35 - 00:47:37] I'll see you on Wednesday.
[00:47:37 - 00:47:56] Hi.
[00:47:56 - 00:47:59] Hello.
[00:47:59 - 00:48:00] Hi.
[00:48:00 - 00:48:02] Hello.
[00:48:02 - 00:48:03] Hi.
[00:48:03 - 00:48:06] Hi.
[00:48:06 - 00:48:08] Hi.
[00:48:08 - 00:48:11] Hi.
[00:48:11 - 00:48:13] Hi.
[00:48:13 - 00:48:16] Hi.
[00:48:16 - 00:48:20] Hi.
[00:48:20 - 00:48:31] The person from the phone came up and said,
[00:48:31 - 00:48:32] You're falling over.
[00:48:32 - 00:48:34] On the mat.
[00:48:34 - 00:48:35] What's the screw?
[00:48:35 - 00:48:37] Thank you.
[00:48:37 - 00:48:46] Don't piss.

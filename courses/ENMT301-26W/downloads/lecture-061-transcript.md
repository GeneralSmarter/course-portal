# ENMT301-26W Lecture 61 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_61_audio_16k_mono_32k.mp3`
Source audio SHA-256: `55d44ad2349fecb7a49d63d0d241c5ba0e1c822f4a560fad4a48693828e0e9a1`
Generated: 2026-06-06T07:19:06.983960+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:00 - 00:00:12] Okay, good afternoon everyone, including the Arsenal fans.
[00:00:12 - 00:00:22] Right, so we were looking at digital filters last week and so this figure here shows
[00:00:22 - 00:00:26] how we calculate the output of our digital filter.
[00:00:26 - 00:00:33] So this is a convolution with the impulse response H of n, X of n is our input,
[00:00:33 - 00:00:36] and each of these three cases it's rectangular function and then we're
[00:00:36 - 00:00:41] convolving it with the impulse response to the filter.
[00:00:41 - 00:00:44] So the top one is taking a moving average of our input.
[00:00:44 - 00:00:51] The middle one is the low pass filter and the third one is taking the derivative of our rectangular function.
[00:00:51 - 00:01:02] Okay, so we're going to then start off today by doing this calculation by hand of the convolution of then our
[00:01:02 - 00:01:11] inputs and our impulse response to get our output.
[00:01:11 - 00:01:13] Okay, so that wasn't the slow we've finished on.
[00:01:13 - 00:01:25] So we can write the convolution then as this sum here where H is our impulse response X is our input.
[00:01:25 - 00:01:41] And so the size or extent of our output is given by the extent of our input plus the extent of our impulse response minus one.
[00:01:41 - 00:01:46] So in the example here, our input, the rectangular function has an extent of four.
[00:01:46 - 00:01:54] The impulse response, which is a two sample moving average, has an extent of two, and our convolution is then has an extent of five.
[00:01:54 - 00:01:59] So the convolution broadens the extent of our signal.
[00:01:59 - 00:02:16] So I think we've finished up on Friday then here we're starting to do this convolution of our input X with our impulse response H.
[00:02:16 - 00:02:33] Okay, so here we've got a fairly simple example where our impulse response has three samples and our input is also three samples.
[00:02:33 - 00:02:42] Okay, and then the underlining of the sample indicates we're in is equal to zero.
[00:02:42 - 00:02:45] So that's our origin point.
[00:02:45 - 00:02:50] Okay, we're going to go through two different methods today for working out this convolution.
[00:02:50 - 00:03:07] Okay, so we're trying to calculate why of in what's the extent of our output going to be for a start.
[00:03:07 - 00:03:14] How long is our output going to be five?
[00:03:14 - 00:03:24] Yes, so it's the length of the input plus the length of the impulse response minus one.
[00:03:24 - 00:03:26] So here we've got three plus three minus one.
[00:03:26 - 00:03:29] So this is going to be of length five.
[00:03:29 - 00:03:54] So our extent is going to be equal to the extent of H of n, which is three plus the extent of X of n, which is also three minus one, minus one equals five.
[00:03:54 - 00:04:07] Okay, so what we're going to do this first way is to then go through this process where we start off with our,
[00:04:07 - 00:04:10] I'm going to take X of n and reverse it.
[00:04:10 - 00:04:14] So this is three, two, one.
[00:04:14 - 00:04:16] So reverse the order of X of n.
[00:04:16 - 00:04:27] And we're going to then shift it across our impulse response one to one.
[00:04:27 - 00:04:41] So our first output sample is then we multiply the overlapping signals.
[00:04:41 - 00:04:48] So that's one times one gives us a value of one for Y of n.
[00:04:48 - 00:04:56] Okay, so then we, our second sample is we're going to shift our X of n by another sample.
[00:04:56 - 00:04:58] So we've got now three, two, one.
[00:04:58 - 00:05:09] Okay, so what's our second sample in Y of n going to be four.
[00:05:09 - 00:05:10] Yep, good.
[00:05:10 - 00:05:15] Okay, and then we can keep doing that.
[00:05:15 - 00:05:17] So we need five more.
[00:05:17 - 00:05:24] So then we've got now got, okay, so Y of n here, the origin is going to be the first sample.
[00:05:24 - 00:05:27] So underline that.
[00:05:27 - 00:05:29] So then we have shifted by one more.
[00:05:29 - 00:05:36] We've got three, two, one times, well, then multiplying the overlapping here.
[00:05:36 - 00:05:41] We've got three plus four plus one gives us eight.
[00:05:41 - 00:05:43] And then we keep shifting it.
[00:05:43 - 00:05:49] So now it's three, two, one, one, two, one.
[00:05:49 - 00:05:54] So it's three times two is six plus two plus one is eight again.
[00:05:54 - 00:06:03] Hello at the back.
[00:06:03 - 00:06:12] Okay, and so then we've got three for the last one with three, two, one with one, two, one.
[00:06:12 - 00:06:18] So our overlap is only here three times the one gives us three.
[00:06:18 - 00:06:27] Okay, so that is then of extent five, one, four, eight, eight, three.
[00:06:27 - 00:06:30] So that's the output of our filter.
[00:06:30 - 00:06:32] Hello at the back.
[00:06:32 - 00:06:34] Okay, so we're going to get a little bit closer.
[00:06:34 - 00:06:36] Okay, so we're going to get a little bit closer.
[00:06:36 - 00:06:43] Okay, so we're going to get a little bit closer.
[00:06:43 - 00:06:46] Okay, so that's the first method for doing the convolution.
[00:06:46 - 00:06:51] So we reverse one, operand, and we shift it by in.
[00:06:51 - 00:06:57] We overlap the multiplying overlapping signals and add them together.
[00:06:57 - 00:07:02] Okay, so it gives us the output of the filter.
[00:07:02 - 00:07:08] And then the second way we're going to look at is a matrix multiplication.
[00:07:08 - 00:07:15] Okay, so we can write our impulse response, eight of in.
[00:07:15 - 00:07:18] So I'm just going to general case here.
[00:07:18 - 00:07:22] So we've got just two samples, eight zero and eight one.
[00:07:22 - 00:07:31] And our input has three samples, x zero, x one, x two.
[00:07:31 - 00:07:39] And again, underlining the origin or win in zero.
[00:07:39 - 00:07:49] Okay, so what we could have done is we could have written that y zero is h zero times x zero.
[00:07:49 - 00:07:58] y one is equal to h zero, x one plus h one x zero.
[00:07:58 - 00:08:06] y two is equal to h zero x two plus h one x one.
[00:08:06 - 00:08:14] And then the y three is h one x two.
[00:08:14 - 00:08:20] Okay, so this has an extent of four because the size of x is three plus the size of h,
[00:08:20 - 00:08:24] which is two minus y and gives us four.
[00:08:24 - 00:08:30] So that's how we would calculate the four values of the output.
[00:08:31 - 00:08:38] So in general, we could write this as a matrix vector modifications.
[00:08:38 - 00:08:50] So we've got our output y zero y one y two y three is then equal to a matrix.
[00:08:50 - 00:08:56] So to find the sec times our inputs x zero x one x two.
[00:09:03 - 00:09:12] Okay, so on the diagonals of this matrix we have h zero h zero h zero.
[00:09:12 - 00:09:17] And then h one h one h one h one.
[00:09:17 - 00:09:26] Okay, and then all the other elements are zero.
[00:09:26 - 00:09:36] So this matrix modification has been doing the reversing shifting and adding for us.
[00:09:36 - 00:09:38] Okay, then we just check, send a new check.
[00:09:38 - 00:09:40] We get our matrix here.
[00:09:40 - 00:09:44] We dive the rows onto the columns like you didn't first see math.
[00:09:44 - 00:09:46] So this is then h zero times x zero.
[00:09:46 - 00:09:47] There's y zero.
[00:09:47 - 00:09:49] That checks out.
[00:09:49 - 00:09:57] Then we have h one times x zero plus h zero times x one.
[00:09:57 - 00:09:59] So that's why one that checks out.
[00:09:59 - 00:10:08] The third one is then zero times x zero h one times x one plus h zero times x two.
[00:10:08 - 00:10:19] Okay, so we'll do the same examples before, but now what writer is a matrix modification.
[00:10:19 - 00:10:25] And just check that we actually get the same answer.
[00:10:25 - 00:10:37] Okay, so just a reminder.
[00:10:37 - 00:10:45] So we had our impulse response h of n was equal to one, two, three.
[00:10:45 - 00:10:57] And our input to the filter x of n was one to one.
[00:10:57 - 00:11:03] Okay, so we're going to write this as a matrix here times our input vector.
[00:11:03 - 00:11:06] So input vector is one to one.
[00:11:06 - 00:11:16] So we're going to start off with our x zero is one one one.
[00:11:16 - 00:11:22] Then we've got our, sorry, h zero was one one one.
[00:11:22 - 00:11:24] Then we've got h one.
[00:11:24 - 00:11:27] So we put two's on the diagonal here.
[00:11:27 - 00:11:41] And then we're going to put three's on the next diagonal and the other elements in our matrix as zero.
[00:11:41 - 00:11:58] And then we're going to redraw my brackets because I'm into a book.
[00:11:58 - 00:12:09] Okay, so then to get our output, we dive.
[00:12:09 - 00:12:13] Do you need some help with my handwriting?
[00:12:13 - 00:12:16] Oh, just, is it?
[00:12:16 - 00:12:18] I've got to ring down.
[00:12:18 - 00:12:21] I think it's one of those eight to nine, one to one.
[00:12:21 - 00:12:24] Yeah, yeah, yeah, for sure.
[00:12:24 - 00:12:33] And I've got to have it done here the wrong way around.
[00:12:33 - 00:12:35] Yeah, yep, yep, yep.
[00:12:35 - 00:12:37] So just at the top is it then.
[00:12:37 - 00:12:44] So the input should be one to one.
[00:12:44 - 00:12:46] Each of the n is one to one.
[00:12:46 - 00:13:06] Each of the n is one to one.
[00:13:06 - 00:13:10] Yes, I have got them the wrong way around.
[00:13:10 - 00:13:12] In the end, it doesn't matter.
[00:13:12 - 00:13:14] Why doesn't it matter?
[00:13:14 - 00:13:16] Because it's commutative.
[00:13:16 - 00:13:20] But I should change it to be consistent.
[00:13:20 - 00:13:24] So I'll just do this on the flight.
[00:13:24 - 00:13:28] Okay, let's make.
[00:13:28 - 00:13:30] Okay, so before I head,
[00:13:30 - 00:13:35] eight was one to one.
[00:13:35 - 00:13:47] Okay, so that's a one and that's a three.
[00:13:47 - 00:13:56] And we'll start all this again.
[00:13:56 - 00:14:01] Okay, so one to one, one to three.
[00:14:01 - 00:14:03] So input is one to three.
[00:14:03 - 00:14:08] Okay, so we start off with
[00:14:08 - 00:14:23] each of n here, which is then we have one, one, one, two, two, one, one.
[00:14:23 - 00:14:27] One, one, one, that's a zero, that's a zero, that's a zero.
[00:14:27 - 00:14:34] Okay, so when we dive our rows onto our columns, we get one.
[00:14:34 - 00:14:44] Then we get from the second row, we get two plus two was four.
[00:14:44 - 00:14:51] Then we get from the third row, one plus four plus three is eight.
[00:14:51 - 00:14:55] Then we get two plus six is eight.
[00:14:55 - 00:14:59] And then we get this one times this three is three.
[00:14:59 - 00:15:10] Okay, so this is the same as before.
[00:15:10 - 00:15:13] Okay, so sorry for the confusion.
[00:15:13 - 00:15:14] Thanks for spotting that.
[00:15:14 - 00:15:16] But it wouldn't have mattered because it is commutative.
[00:15:16 - 00:15:19] You can do the convolution either way.
[00:15:19 - 00:15:23] Okay, so for this test, who's going to do the matrix approach?
[00:15:23 - 00:15:27] And who's going to do the shift and add approach?
[00:15:27 - 00:15:30] Who's going to decide for the test?
[00:15:30 - 00:15:33] The other 120 people.
[00:15:33 - 00:15:51] Okay, so that's two different ways to do this convolution to get your output of the filter.
[00:15:51 - 00:15:56] Okay, so we'll look at different types of filters now,
[00:15:56 - 00:16:00] and the key properties of filters.
[00:16:00 - 00:16:05] And so we can write the general form of the filters that this describes
[00:16:05 - 00:16:10] finite and post-response filters and infinite and post-response filters.
[00:16:10 - 00:16:12] High-pass, low-pass, pass, pass, pass, pass, pass, pass, stop.
[00:16:12 - 00:16:13] What if you want?
[00:16:13 - 00:16:23] If they can be all resident in the form, the output, y of n is equal to the sum of the
[00:16:23 - 00:16:34] kb, which are the feed-forward coefficients, times the inputs delayed by k samples.
[00:16:34 - 00:16:45] Okay, so b equals the feed-forward coefficients.
[00:16:45 - 00:17:02] And this is then minus the sum over m of our feedback coefficients, a times our output, y,
[00:17:02 - 00:17:06] delayed by m samples.
[00:17:06 - 00:17:12] So a is the feed-back coefficients.
[00:17:12 - 00:17:41] Okay, if I were to set all the values of a equals zero for all values of m,
[00:17:41 - 00:17:48] what sort of filter would it be?
[00:17:48 - 00:17:59] So if we just got the b coefficients, yeah, a finite and post-response filter.
[00:17:59 - 00:18:03] Okay, so if we get rid of the feedback coefficients, it's essentially a weighted average,
[00:18:03 - 00:18:13] we're just then dealing with these weighted sums of our input samples.
[00:18:13 - 00:18:18] We don't have any feedback, so that's just a finite and post-response filter.
[00:18:18 - 00:18:23] So this general form of the filter can be reduced to the case of the finite and
[00:18:23 - 00:18:29] post-response filter where a is zero.
[00:18:29 - 00:18:35] Okay, so that's the difference equation for our filter.
[00:18:35 - 00:18:44] The filter transfer function, a to z, which is defined as the output and
[00:18:44 - 00:18:52] the z domain over the input x of z and the z domain, is then equal to,
[00:18:52 - 00:18:57] just by taking the z transform of the difference equation rearranging,
[00:18:57 - 00:19:07] we have then in the numerator, we have the sum over k of bk z to the minus k.
[00:19:07 - 00:19:13] So there's delay here of, or shift of k samples, but then becomes a z to the minus k.
[00:19:13 - 00:19:18] And the z domain, and in the denominator,
[00:19:18 - 00:19:28] we have then one plus the sum from m is one to capital M,
[00:19:28 - 00:19:31] a m z to the minus m.
[00:19:31 - 00:19:50] And we can also rewrite this h of z in pz k form, so we have then a gain,
[00:19:50 - 00:20:03] call this g for gain, because I'm using k as a counter.
[00:20:03 - 00:20:08] And then we have the, we can rearrange this to be then a product.
[00:20:08 - 00:20:13] So this here pi means it's a product.
[00:20:13 - 00:20:17] So similar to sigma, which is a sum.
[00:20:17 - 00:20:33] So we have sum over all our zeros, equals zero to capital K.
[00:20:33 - 00:20:40] And then on the denominator, we have the product of all our poles.
[00:20:40 - 00:21:05] So this is the sum from the product from m is one to capital M.
[00:21:05 - 00:21:13] Okay, so when we've written this in the bottom form, the poles zero is gain form,
[00:21:13 - 00:21:23] how do we define the order of our filter?
[00:21:23 - 00:21:29] So somehow related to our number of poles and number of zeros,
[00:21:29 - 00:21:41] the idea is, so it's the maximum value of either capital M,
[00:21:41 - 00:21:49] the number of poles or capital K, the number of zeros.
[00:21:49 - 00:22:00] Okay, so the filter order is going to be come important when we look at the frequency response of the filter.
[00:22:00 - 00:22:08] So we start looking at the both plots, as you'll see in an enemy 303.
[00:22:08 - 00:22:16] In the number of, well, the order of the system then determines whether it's 20 dB or 40 dB per decade, etc.
[00:22:16 - 00:22:31] Okay, so let's look at some filters and how we can generate some filters here.
[00:22:31 - 00:22:36] This isn't Python.
[00:22:36 - 00:22:44] Okay, so we can generate a second order low pass filter, but a worth type.
[00:22:44 - 00:22:52] Okay, so there's a little script from Python, which is then generating the figure on the right,
[00:22:52 - 00:22:57] which is the frequency response for our filter.
[00:22:57 - 00:23:00] Okay, so let's just go through this.
[00:23:00 - 00:23:05] So we've got something frequency here is 50 kilohertz,
[00:23:05 - 00:23:10] kilohertz, and we've got our cutoff frequency is 2 kilohertz.
[00:23:10 - 00:23:21] Okay, and so then the function butter, which is in psi pi, they'll signal.
[00:23:21 - 00:23:26] This is generating our butter worth filter.
[00:23:26 - 00:23:46] So this 2 here is its second order, and so again, the feed forward or moving average coefficients,
[00:23:46 - 00:23:57] and the feedback auto-regressive coefficients.
[00:23:57 - 00:24:11] Okay, so this butter function here takes the order of the filter.
[00:24:11 - 00:24:13] What sort of filter you want here?
[00:24:13 - 00:24:23] So we're going for a low pass filter, and then it has the normalized cutoff frequency.
[00:24:23 - 00:24:29] So it's normalized by the Nyquist frequency, so we're dividing by the something frequency over 2.
[00:24:29 - 00:24:39] It's normalized by the something frequency divided by 2.
[00:24:39 - 00:24:49] Okay, and then this function here freaks it.
[00:24:49 - 00:25:16] This gives the discrete time Fourier transform, discrete time Fourier transform of the filter.
[00:25:16 - 00:25:22] Okay, and then the last five lines are just plotting the filter response.
[00:25:22 - 00:25:27] So we have then our cutoff frequency, what we say, was 2 kilohertz.
[00:25:27 - 00:25:39] So 2 kilohertz is here, this is Fc, and so then at the cutoff frequency,
[00:25:39 - 00:25:58] we are three decibels down and magnitude, and then what's the slope of our roll-off here of our filter.
[00:25:58 - 00:26:04] For the high frequencies beyond the cutoff frequency, 40 dB per decade.
[00:26:04 - 00:26:17] Okay, and so this here 40 dB per decade.
[00:26:17 - 00:26:25] Okay, so that's 2, which is our order times 20.
[00:26:25 - 00:26:34] Okay, we'll look at higher order filters in a bit.
[00:26:34 - 00:26:43] Okay, so I'm sure it's well off your radar, but there is an assignment for this parlacause, which is the IMU assignment,
[00:26:43 - 00:26:47] which is not due until, I think, the end of week two of turn three.
[00:26:47 - 00:26:52] So, like about two miles to go away, and it's worth five percent of course.
[00:26:52 - 00:26:56] So, it's probably not your focus yet.
[00:26:56 - 00:26:59] I'll put the instructions up on the load probably next week,
[00:26:59 - 00:27:03] but you're going to have to do some filtering in that assignment.
[00:27:03 - 00:27:09] And so these functions are going to be useful for doing that assignment.
[00:27:09 - 00:27:25] Okay, so that was generating our filter and plotting the frequency response of the filter.
[00:27:25 - 00:27:30] Let's look at what happens in the time domain.
[00:27:30 - 00:27:35] Okay, so we've got our filter from the previous slide,
[00:27:35 - 00:27:55] and we've created some signal x-ray in here, which is defined as five plus two times one plus two cosine two pi in times five hundred.
[00:27:55 - 00:28:11] Okay, so that's giving us our noiseless cosine samples.
[00:28:11 - 00:28:29] Okay, then we've got additive white Gaussian noise, and then we've got this dropout here.
[00:28:29 - 00:28:33] So, we've got five samples that are set to zero here.
[00:28:33 - 00:28:45] So, that's modeling, say our sensor's gone on the fruits, and it's just stopped sending any data for a few seconds,
[00:28:45 - 00:28:48] or maybe seconds.
[00:28:48 - 00:28:51] Okay, so we get this dropout of a signal.
[00:28:51 - 00:28:55] So, we've got this cosine here.
[00:28:55 - 00:29:01] We've got additive Gaussian noise on the top of it with this dropout,
[00:29:01 - 00:29:03] added about a hundred samples.
[00:29:03 - 00:29:15] Okay, so this is our noisy x-of-in,
[00:29:15 - 00:29:20] our BnRA, our filter coefficients from the previous slide.
[00:29:20 - 00:29:33] And so this function L-thoucher then applies the filter,
[00:29:33 - 00:29:36] the filter coefficients to our input x,
[00:29:36 - 00:29:43] and then the figure at bottom is our filtered signal.
[00:29:43 - 00:29:47] So, this is y-of-in.
[00:29:47 - 00:29:53] Okay, so this is low pass filter, so the high frequencies in the top figure,
[00:29:53 - 00:29:56] is really quick changes.
[00:29:56 - 00:29:59] The noise, that's high frequencies, so let's get filtered out,
[00:29:59 - 00:30:04] and we're left then with kind of the lower frequency.
[00:30:04 - 00:30:14] It's not a perfect cosine wave with some residual noise,
[00:30:14 - 00:30:21] and we have our dropout here is also reduced.
[00:30:21 - 00:30:38] So, in summary, the noise is reduced to that high frequencies removed,
[00:30:38 - 00:30:48] and also this dropout is reduced as well.
[00:30:48 - 00:30:51] Okay, so the dropout is also a high frequency.
[00:30:51 - 00:30:54] It's a very quick change with time,
[00:30:54 - 00:31:01] so that can be removed with a low pass filter,
[00:31:01 - 00:31:07] or reduced anywhere.
[00:31:07 - 00:31:13] Okay, and then I've got one more Python example with this low pass filter,
[00:31:13 - 00:31:16] and that's generating our impulse response.
[00:31:16 - 00:31:32] Okay, so our input to the filter here x of n is this time,
[00:31:32 - 00:31:40] it's essentially our double function, so we've got 1,
[00:31:40 - 00:31:46] and then 50 zeros, 49 zeros.
[00:31:46 - 00:31:52] So that's the input x to our filter,
[00:31:52 - 00:32:09] and we've got the same coefficients as previously.
[00:32:09 - 00:32:13] Okay, so this here is then plotting the impulse response,
[00:32:13 - 00:32:15] which I normally call h of n,
[00:32:15 - 00:32:19] what's the sample number n.
[00:32:19 - 00:32:27] So here we've got a non-zero values of a,
[00:32:27 - 00:32:32] so this then is sort of filter as this.
[00:32:32 - 00:32:42] Ah, yes, so this is an infinite impulse response,
[00:32:42 - 00:32:47] so this is h of n is infinite.
[00:32:47 - 00:32:50] It's getting pretty close to zero,
[00:32:50 - 00:32:55] but it's not exactly equal to zero.
[00:32:55 - 00:33:20] Okay, so that was a three slide Python aside,
[00:33:20 - 00:33:25] and you're probably able to do similar things
[00:33:25 - 00:33:30] on your robot when you have noisy sense of measurements,
[00:33:30 - 00:33:33] but in that case you'll probably be wanting to write it,
[00:33:33 - 00:33:37] and I guess I do know, not see,
[00:33:37 - 00:33:39] I do know for your robot cup.
[00:33:39 - 00:33:46] Yep, that's the wrong way.
[00:33:46 - 00:33:51] Okay, the next thing we want to consider is something called linear phase.
[00:33:51 - 00:34:00] So first of all, let's go back in time and recall the Fourier shift theorem,
[00:34:00 - 00:34:05] so that said, if we take the Fourier transform of some signal x,
[00:34:05 - 00:34:10] which is shifted in time by an amount t0,
[00:34:10 - 00:34:16] this is equivalent to the spectrum x of f,
[00:34:16 - 00:34:22] so x of t and x of f are a Fourier transform here,
[00:34:22 - 00:34:27] but then we have a complex exponential here,
[00:34:27 - 00:34:31] e to the minus j to the power of x of t,
[00:34:31 - 00:34:36] j to pi f t0.
[00:34:36 - 00:34:53] Okay, and so this complex exponential here is linear with respect to frequency f.
[00:34:53 - 00:35:13] Okay, so the key point here is if we have a linear phase shift
[00:35:13 - 00:35:20] in the frequency domain, this e to the minus j to pi f t0,
[00:35:20 - 00:35:28] is linear with respect to f, that means that we get a pure time shift in the time domain.
[00:35:28 - 00:35:34] Okay, so for this to be linear,
[00:35:34 - 00:35:39] we have to be able to write our phase of our frequency response,
[00:35:39 - 00:35:42] so it's a big angle x of f.
[00:35:42 - 00:35:48] To be linear, we have some constant alpha times f plus some beta.
[00:35:48 - 00:35:54] Okay, so let's just describing a straight line.
[00:35:54 - 00:36:01] So it's linear with frequency.
[00:36:01 - 00:36:07] Okay, so if you think of, say, a voice signal
[00:36:07 - 00:36:15] that is made up of a large number of different frequencies,
[00:36:15 - 00:36:19] we want all those frequencies to be delayed by the same amount in time
[00:36:19 - 00:36:22] when we filter the voice signal.
[00:36:22 - 00:36:26] If different frequencies are delayed by different amounts in time,
[00:36:26 - 00:36:32] then we're going to have a distortion of the voice signal.
[00:36:32 - 00:36:35] Okay, so that's why this linear phase is really important.
[00:36:35 - 00:36:38] We need our filter to have linear phase,
[00:36:38 - 00:36:46] so that all the frequencies in the signal we're transmitting are delayed by the same amount in time.
[00:36:46 - 00:36:49] If different frequencies get delayed by different amounts,
[00:36:49 - 00:36:51] then our waveform is going to change shape,
[00:36:51 - 00:36:57] and then we're going to have some sort of distortion.
[00:36:57 - 00:37:03] Okay, and so then this is the key difference between infinite impulse response filters
[00:37:03 - 00:37:06] and finite impulse response filters.
[00:37:06 - 00:37:15] So infinite impulse response filters cannot have this desired quality of linear phase.
[00:37:15 - 00:37:18] They're going to introduce some sort of distortion.
[00:37:18 - 00:37:23] Whereas finite impulse response filters can have linear phase
[00:37:23 - 00:37:29] if their impulse response is symmetric.
[00:37:29 - 00:37:31] So let's look at a couple.
[00:37:31 - 00:37:40] So h of n, for example, in example,
[00:37:40 - 00:37:50] I did previously one to one that has linear phase.
[00:37:50 - 00:37:56] Okay, the impulse response is symmetric.
[00:37:56 - 00:37:58] I'll tidy up my miss there.
[00:37:58 - 00:38:06] But then when I head up the wrong way around,
[00:38:06 - 00:38:14] if the impulse response is one, two, three,
[00:38:14 - 00:38:16] that has nonlinear phase.
[00:38:16 - 00:38:17] It's not symmetric.
[00:38:17 - 00:38:36] Okay, so let's look at an example,
[00:38:36 - 00:38:44] because that's much more the strength of than reading a bullet point or two.
[00:38:44 - 00:38:48] So let's look at these two cases here.
[00:38:48 - 00:38:57] Okay, so let's consider a signal x of t,
[00:38:57 - 00:39:05] which is the first three terms of the Fourier series of a square wave.
[00:39:05 - 00:39:15] So we've got x of t is 4 pi sine 2 pi t,
[00:39:15 - 00:39:23] plus 4 over 3 pi sine 6 pi t,
[00:39:23 - 00:39:31] plus 4 over 5 sine 10 pi t.
[00:39:31 - 00:39:49] Okay, so first three terms of a Fourier series of a square wave.
[00:39:49 - 00:40:08] Okay, so the example we have on the left here is for linear phase.
[00:40:08 - 00:40:18] So we have, this is the sum.
[00:40:18 - 00:40:21] And well, on the right, we've got nonlinear phase.
[00:40:21 - 00:40:26] I'll just describe what all these graphs are.
[00:40:26 - 00:40:34] So on the left, we have the big figure is the sum.
[00:40:34 - 00:40:45] Okay, so read as our original signal.
[00:40:45 - 00:40:49] So when we add these three frequencies,
[00:40:49 - 00:40:52] let's call this if zero, if one,
[00:40:52 - 00:41:13] and if it's called them if one, if three, and if five.
[00:41:13 - 00:41:18] So this is if one, if three, and if five.
[00:41:18 - 00:41:24] So when we sum these three signals together,
[00:41:24 - 00:41:32] so we sum the three red curves, we get this approximation to a square wave
[00:41:32 - 00:41:41] from our three sine waves there.
[00:41:41 - 00:41:46] Now on the left, we have, in each case,
[00:41:46 - 00:41:52] we've got a thousand samples.
[00:41:52 - 00:42:03] And so the figures on the left, the blue curve is all the frequencies
[00:42:03 - 00:42:09] that are delayed by 40 samples.
[00:42:09 - 00:42:20] Okay, so all frequencies in that square wave are delayed by the same amount of time.
[00:42:20 - 00:42:25] So that means the output signal, the blue curve,
[00:42:25 - 00:42:30] then has the same shape as the input signal, the red curve.
[00:42:30 - 00:42:42] Okay, so that's then with linear phase and what happens in an FAR filter.
[00:42:42 - 00:42:47] But on the right, we have nonlinear phase.
[00:42:47 - 00:42:50] And so in this case, we do have non-constant delay,
[00:42:50 - 00:42:59] constant delay.
[00:42:59 - 00:43:04] So in this case, we've got the delay,
[00:43:04 - 00:43:15] let's be added, was the higher frequencies are getting larger delay and samples.
[00:43:15 - 00:43:19] And so then when we add up the different frequencies which have been delayed
[00:43:19 - 00:43:25] by different amounts, the sum, the blue curve,
[00:43:25 - 00:43:31] now no longer looks like our input to the filter, the red curve.
[00:43:31 - 00:43:39] Okay, so we get this distortion in an IR,
[00:43:39 - 00:43:44] IR, infinite impulse response filter from the nonlinear phase,
[00:43:44 - 00:43:47] different frequencies are delayed by different amounts in time,
[00:43:47 - 00:43:51] and that distorts our waveform output from the filter.
[00:43:51 - 00:44:12] Okay, so that's why the nonlinear phase for IR can be problematic.
[00:44:12 - 00:44:17] So that Python example we had previously,
[00:44:17 - 00:44:20] so this is an IR filter,
[00:44:20 - 00:44:24] so that A values were not equal to zero.
[00:44:24 - 00:44:29] This phase response is,
[00:44:29 - 00:44:32] so it goes from zero down to minus pi,
[00:44:32 - 00:44:34] but this is nonlinear,
[00:44:34 - 00:44:45] whereas an IR filter might go like that.
[00:44:45 - 00:45:33] Five minutes to go.
[00:45:33 - 00:45:37] Okay, so there are other types of filters that we could look at
[00:45:37 - 00:45:43] that are nonlinear filters, and so the example I'll give is a median filter.
[00:45:45 - 00:45:54] And so a median filter can work well with noise spikes
[00:45:54 - 00:45:57] or sensor dropouts, like we saw in the previous example,
[00:45:57 - 00:46:00] with a sense of values went to zero for a little bit.
[00:46:00 - 00:46:04] And so these nonlinear filters might be able to handle
[00:46:04 - 00:46:06] this impulsive noise better,
[00:46:06 - 00:46:10] but they're much harder to analyze.
[00:46:10 - 00:46:16] So if we consider a signal of the form here,
[00:46:16 - 00:46:20] X of n is equal to 2,
[00:46:20 - 00:46:29] 1, 42, 3, 7, 5, 2.
[00:46:29 - 00:46:32] Okay, what number doesn't belong there?
[00:46:32 - 00:46:35] 42, so something's gone wrong here.
[00:46:35 - 00:46:37] There's some sort of noise spike here,
[00:46:37 - 00:46:40] so this is an outlier.
[00:46:40 - 00:46:43] If we did a moving average filter like before,
[00:46:43 - 00:46:46] then we wouldn't remove that 42,
[00:46:46 - 00:46:49] which is average it into all the other values.
[00:46:49 - 00:46:58] So a median filter, yeah, wire then,
[00:46:58 - 00:47:02] what we could do is then take the median of these first three.
[00:47:02 - 00:47:07] That's a two, the median of these three.
[00:47:07 - 00:47:13] That's three, then the median of these three is seven.
[00:47:13 - 00:47:17] The median of these three is five,
[00:47:17 - 00:47:23] and then the median of these three is also five.
[00:47:23 - 00:47:25] Okay, so with this median filter,
[00:47:25 - 00:47:29] we can remove the outlier.
[00:47:29 - 00:47:58] Okay, so we'll just finish today then with this example
[00:47:58 - 00:48:01] of a noisy signal that we had before.
[00:48:01 - 00:48:04] So we've got this dropout here,
[00:48:04 - 00:48:08] and we'll apply a median filter.
[00:48:08 - 00:48:11] So this is our X of n,
[00:48:11 - 00:48:14] it's the top figure, that's our input to the filter,
[00:48:14 - 00:48:16] and then the bottom one is Y of n.
[00:48:16 - 00:48:22] Then this is our output from the filter.
[00:48:22 - 00:48:26] And so this, here we have with our median filter,
[00:48:26 - 00:48:31] how dropout is removed.
[00:48:31 - 00:48:46] The high frequency noise is also reduced with the median filter as well.
[00:48:46 - 00:48:49] So I think we'll finish there for today.
[00:48:49 - 00:48:52] We've got one sort of summary slide left for tomorrow,
[00:48:52 - 00:48:55] and then we'll start off looking at sampling
[00:48:55 - 00:48:57] the screen for your transform.
[00:48:57 - 00:48:59] So next, have lectures, and then next week,
[00:48:59 - 00:49:03] we'll look at different sensors and sensing methods.
[00:49:03 - 00:49:06] Okay, and remind us that tutorial tomorrow,
[00:49:06 - 00:49:08] the questions are on learn,
[00:49:08 - 00:49:11] the answers from the previous ones are up there if you want to
[00:49:11 - 00:49:14] catch up, check your answers, et cetera.
[00:49:14 - 00:49:28] So see you tomorrow.
[00:49:28 - 00:49:29] Thank you.
[00:49:29 - 00:49:31] This week, we're about to wait two for you.
[00:49:31 - 00:49:35] This is her, though.
[00:49:35 - 00:49:37] I laughed, but I didn't die.
[00:49:37 - 00:49:41] I'm just so excited.
[00:49:41 - 00:49:42] I can't hear you.
[00:49:42 - 00:49:44] But you know, I like that.
[00:49:44 - 00:49:45] I want to drink.
[00:49:45 - 00:49:46] Yes.
[00:49:46 - 00:49:47] I want to drink.
[00:49:47 - 00:49:48] I want to drink.
[00:49:48 - 00:49:49] I want to drink.
[00:49:49 - 00:49:50] I want to drink.
[00:49:50 - 00:49:51] Come on, guys.
[00:49:51 - 00:49:52] I want to drink.
[00:49:52 - 00:49:53] I want to drink.
[00:49:53 - 00:49:54] I want to drink.
[00:49:54 - 00:49:55] I want to drink.
[00:49:55 - 00:49:56] So what?
[00:49:56 - 00:49:58] It's going to be coming week nine.
[00:49:58 - 00:49:59] I want to drink.
[00:49:59 - 00:50:01] It's been a bit of a bit of a bit of a time.
[00:50:01 - 00:50:03] We're playing.
[00:50:03 - 00:50:04] OK.
[00:50:04 - 00:50:09] I want you to be six bags.
[00:50:09 - 00:50:11] Good.
[00:50:11 - 00:50:12] Good.
[00:50:12 - 00:50:13] Okay.
[00:50:13 - 00:50:16] Congratulations.
[00:50:16 - 00:50:18] We're having a lot of TV.
[00:50:18 - 00:50:19] I'm balancing it.
[00:50:19 - 00:50:24] I'm doing why I'm eating a little baby, baby.
[00:50:54 - 00:50:55] Yes.

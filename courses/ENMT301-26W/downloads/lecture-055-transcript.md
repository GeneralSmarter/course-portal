# ENMT301-26W Lecture 55 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_55_audio_16k_mono_32k.mp3`
Source audio SHA-256: `85ad9cc73b5742fc1f4bc23e491c6eae619c605034c7dae076b45616f1492180`
Generated: 2026-06-06T07:06:13.312674+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:02 - 00:00:06] Okay, good afternoon everyone.
[00:00:06 - 00:00:10] So today we're going to be doing digital filters.
[00:00:10 - 00:00:18] We've just got one slide left over from last week on analogue filters looking at what happens to our noise through the filtering process.
[00:00:18 - 00:00:26] So just quickly do that and then we'll get on to what's a digital filter and why would we use a digital filter rather than analogue one.
[00:00:26 - 00:00:33] Okay, so the power spent true density of the noise.
[00:00:33 - 00:00:39] So that's the power at each energy or each frequency for the noise.
[00:00:39 - 00:00:53] So we're going to call this the power spent for density of the using capital S and why is the output as a function of frequency f.
[00:00:53 - 00:01:17] So this is the noise piece, the output is equal to the noise density of the input, so x for input, y for output.
[00:01:17 - 00:01:27] And this gets multiplied by the magnitude of our frequency response of our filter squared.
[00:01:27 - 00:01:33] So h of f is our frequency response and so it's magnitude squared.
[00:01:33 - 00:01:44] This is magnitude frequency response squared.
[00:01:44 - 00:01:57] Okay, so if you know the noise power at the input and we know our filters, our transfer function or frequency response,
[00:01:57 - 00:02:02] we can then work out our noise piece to the output.
[00:02:02 - 00:02:17] Okay, so our noise variance at the output is a sigma, y for output, squared is then
[00:02:17 - 00:02:41] integral overall frequencies. So from zero to infinity of our output pst, sy of f and we're integrating overall our frequencies df.
[00:02:41 - 00:02:49] Okay, so at the end of the electron Friday, we looked at this perfect low pass filter,
[00:02:49 - 00:03:01] right, the low pass filter which is a brick wall, which we can't actually build in practice, but this has a sharp cutoff at the bandwidth of b.
[00:03:01 - 00:03:04] So there's a brick wall filter.
[00:03:04 - 00:03:17] And so then within our brick wall filter, the magnitude of the frequency response is one and at zero then outside that bandwidth.
[00:03:17 - 00:03:38] Okay, so for the brick wall filter, we have the magnitude of h of f squared is then equal to one.
[00:03:38 - 00:03:46] Okay, so then we can simplify that equation for the variance.
[00:03:46 - 00:03:56] So we have our variance at the output, sigma of y squared is then equal to the integral over the bandwidth we're considering,
[00:03:56 - 00:04:09] which is from f1 to f2, it's the input pst is six, as the function of frequency df.
[00:04:09 - 00:04:15] So that's the equation at the top and with substitute in h of f squared is one.
[00:04:15 - 00:04:21] Okay, so this is shown in the figure at the bottom.
[00:04:21 - 00:04:32] So we've got white noise, we have a constant value of our noise pst.
[00:04:32 - 00:04:44] So the power spectrum density is the same for all frequencies.
[00:04:44 - 00:04:49] And in the first week, I think it was the first week we looked at the thermal noise of a resistor.
[00:04:49 - 00:05:11] Also known as Johnson noise and we had for that our input pst is as the function of frequency f was equal to 4kt.
[00:05:11 - 00:05:29] Okay, so if we then integrate, hey, at a back, I'm trying to give a lecture here.
[00:05:29 - 00:05:32] If you stay be quiet, otherwise there's plenty of other spaces to.
[00:05:32 - 00:05:55] Okay, so if we are looking at the variance of our output noise, then for thermal noise a resistor, our input pst is a constant 4kt r,
[00:05:55 - 00:06:00] we're then integrating over some bandwidth between f2 and f1.
[00:06:00 - 00:06:09] And so this gives us our output variance signal i squared is equal to 4kt r,
[00:06:09 - 00:06:15] then from the integral from f1 to f2 gives us our bandwidth b.
[00:06:15 - 00:06:20] So b is equal to f2 minus f1.
[00:06:20 - 00:06:31] Okay, so that was the result we had for our noise variance for a resistor due to thermal noise.
[00:06:31 - 00:06:34] And earlier in the course.
[00:06:34 - 00:06:47] Okay, so that's the end of analog circuits.
[00:06:47 - 00:06:53] So I'll just let you quickly finish that off and then we'll start with our digital filters.
[00:06:53 - 00:07:09] Keep closed, save.
[00:07:09 - 00:07:40] Okay, so last week or so we'll be looking at designing filters, low pass filters, high pass filters, etc.
[00:07:40 - 00:07:44] From analog circuitry, so with resistors and factors capacitors,
[00:07:44 - 00:07:50] so those are all circuit elements that we're going to solder on to our PCB.
[00:07:50 - 00:07:56] Okay, so the other way of doing filtering is in the digital domain, so we have microcontroller,
[00:07:56 - 00:08:01] and we write some software, and that can do the filtering for us.
[00:08:01 - 00:08:07] So this is known as digital filter, and we analyze digital filters with something that is a z-transform,
[00:08:07 - 00:08:14] which is analogous to a Laplace transform, but it's in digital space.
[00:08:14 - 00:08:23] So we can write our digital filters, or often shown with these sorts of filter realization diagrams,
[00:08:23 - 00:08:27] a shown on the left hand side.
[00:08:27 - 00:08:36] And so this is saying we have some input to our filter x-in, y-in is the output,
[00:08:36 - 00:08:45] and then these z-n-minus ones are delays of our sequence of input signals.
[00:08:45 - 00:08:54] These triangles are multipliers, and these pluses are adders.
[00:08:54 - 00:09:01] So by combining those three simple operations, the layer of a sequence,
[00:09:01 - 00:09:05] a multiplication with the scalar, and then adding bits and pieces together,
[00:09:05 - 00:09:09] we can generate low-pass filters, high-pass filters,
[00:09:09 - 00:09:13] and then pass filters, and stuff filters, etc.
[00:09:13 - 00:09:23] And so this one here is what's known as a moving average filter,
[00:09:23 - 00:09:30] and so our multipliers or the weights of the filter are all a quarter.
[00:09:30 - 00:09:36] Then that takes the average over four samples in our sequence.
[00:09:36 - 00:09:44] So that's a way to get rid of noise, and so this ends up being a low-pass filter.
[00:09:44 - 00:09:49] Okay, so this is just a preview of what we're going to do over the next week and a half.
[00:09:49 - 00:10:03] Okay, so let's look at our signal processing chain again.
[00:10:03 - 00:10:07] So we've got some Megatronic system.
[00:10:07 - 00:10:12] We've got, say, some sensor here.
[00:10:12 - 00:10:18] That might be a range sensor detecting some distance on your robot.
[00:10:18 - 00:10:28] You have got an amplifier to amplify the sensor output.
[00:10:28 - 00:10:33] We have an NTA filter that removes ASing,
[00:10:33 - 00:10:36] we'll get into sampling and ASing next week.
[00:10:36 - 00:10:42] But this is a type of analog filter.
[00:10:42 - 00:10:48] And so at this point we have a continuous signal, X of T,
[00:10:48 - 00:10:51] and then we go through the analog to digital converter.
[00:10:51 - 00:10:58] We'll have a digital signal, X with square brackets of N,
[00:10:58 - 00:11:05] and then we might do a digital filter, which here is highlighted in pink.
[00:11:05 - 00:11:15] So we could do, say, since the signal has high frequency noise,
[00:11:15 - 00:11:18] we could have a low-pass filter here,
[00:11:18 - 00:11:33] or we could do the low-pass filter in the digital domain.
[00:11:33 - 00:11:40] Okay, so there's some advantages of doing our filtering.
[00:11:40 - 00:11:43] For example, a low-pass filter in the digital domain,
[00:11:43 - 00:11:47] rather than in the analog domain.
[00:11:47 - 00:11:52] So the first one is, if we've got an analog circuit,
[00:11:52 - 00:11:55] the resistance of your resistor is going to change,
[00:11:55 - 00:11:59] so that it heats up, and with time,
[00:11:59 - 00:12:03] whereas the software you write to implement your digital filter
[00:12:03 - 00:12:06] is going to be the same each time you run it.
[00:12:06 - 00:12:10] So it's going to be more precise in the digital domain,
[00:12:10 - 00:12:14] rather than in the analog filter.
[00:12:14 - 00:12:27] Okay, so say if you're producing a number of these robots,
[00:12:27 - 00:12:29] say, and I've each got a circuit board,
[00:12:29 - 00:12:33] we've got a low-pass filter made of a resistor and a capacitor.
[00:12:33 - 00:12:36] The resistor values aren't all going to be exactly the same.
[00:12:36 - 00:12:39] On the resistors, you've got these little bands on them.
[00:12:39 - 00:12:43] The last one is on the variance.
[00:12:43 - 00:12:46] So depending how much money you spend on your resistors,
[00:12:46 - 00:12:49] you could be plus minus 1, 5, 10%, etc.
[00:12:49 - 00:12:53] So if you're setting the cutoff frequency of your filter,
[00:12:53 - 00:12:59] and you've got, say, a 10% variance on your resistor value,
[00:12:59 - 00:13:03] each robot is then going to have a different cutoff frequency.
[00:13:03 - 00:13:06] It's not going to be precise because you're going to have variation
[00:13:06 - 00:13:09] between the different circuit elements.
[00:13:09 - 00:13:18] Like another problem with, say, having an analog circuit,
[00:13:18 - 00:13:22] say you want to change your cutoff frequency of your filter,
[00:13:22 - 00:13:27] because you want to get rid of more high frequency noise.
[00:13:27 - 00:13:30] To do that with the analog circuit, you're going to have to remove the resistor
[00:13:30 - 00:13:34] or the capacitor with a soldering ion and then put a new component in there
[00:13:34 - 00:13:37] if you're going to change your cutoff frequency.
[00:13:37 - 00:13:40] Whereas if you were doing a digital filter,
[00:13:40 - 00:13:44] all you need to do is change some software and then
[00:13:44 - 00:13:46] upload that to the microcontroller.
[00:13:46 - 00:13:54] So that is simpler for maintenance as well.
[00:13:54 - 00:13:58] And you can also get more complicated designs with a digital filter,
[00:13:58 - 00:14:03] so to have a sharper cutoff of your filters, make sure that you've got linear phase
[00:14:03 - 00:14:04] of your filter.
[00:14:04 - 00:14:06] It's going to be able to graph later.
[00:14:06 - 00:14:12] So this is easier with a digital filter than with analog filters.
[00:14:12 - 00:14:23] Okay, so that's what we might do, digital filter, rather than an analog filter.
[00:14:23 - 00:14:33] Okay, so let's think about noise to start with in our digital domain.
[00:14:33 - 00:14:36] So the noise is random.
[00:14:36 - 00:14:41] If you think of white noise, but it will have some statistical properties
[00:14:41 - 00:14:44] that we can model.
[00:14:44 - 00:14:49] So if we have a noise signal, it's called a W of n.
[00:14:49 - 00:14:51] So this is our noise signal.
[00:14:51 - 00:15:01] And then that noise signal can be written as a noise sequence.
[00:15:01 - 00:15:09] And so we've got our noise value at the first sample,
[00:15:09 - 00:15:13] the noise at the second sample dot dot,
[00:15:13 - 00:15:19] up to our nth sample.
[00:15:19 - 00:15:30] Okay, so we can think of the noise at each sample point
[00:15:30 - 00:15:32] as being a random variable.
[00:15:32 - 00:15:36] So it will have some mean invariance.
[00:15:36 - 00:15:45] And so then we have a noise process capital W of n.
[00:15:45 - 00:15:48] And this is then a series of random variables,
[00:15:48 - 00:15:55] W0, W1, dot, dot, dot, Wn minus 1,
[00:15:55 - 00:16:00] for each point in time.
[00:16:00 - 00:16:04] Okay, so each of these capital Ws is in a random variable
[00:16:04 - 00:16:07] with its probability density function.
[00:16:07 - 00:16:12] So for example, the Gaussian that we looked at in the first week
[00:16:12 - 00:16:16] when we're looking at noise is the most common one for modeling noise.
[00:16:16 - 00:16:24] So the most common noise process is additive white Gaussian noise.
[00:16:24 - 00:16:31] So we have our signal and then white Gaussian noise is added to the top of it.
[00:16:31 - 00:16:35] And the assumption we can normally make is that at each instance in times
[00:16:35 - 00:16:39] at W0, W1, dot, dot, dot, Wn minus 1,
[00:16:39 - 00:16:44] they can all be modeled by the same Gaussian distribution.
[00:16:44 - 00:16:53] So the mean invariance are the same at all points in time.
[00:16:53 - 00:16:55] Okay, so let's look at an example of noise
[00:16:55 - 00:17:08] and how we can do some averaging to filter out the noise.
[00:17:08 - 00:17:11] Okay, so here I've created a noise signal.
[00:17:11 - 00:17:18] So here we've got, so capital N is 100 samples.
[00:17:18 - 00:17:25] Okay, so this is our noise sequence W of n
[00:17:25 - 00:17:30] between 0 and 99.
[00:17:30 - 00:17:33] So that's the big plot.
[00:17:33 - 00:17:38] The plot on the side here is the histogram
[00:17:38 - 00:17:44] and the orange is showing the Gaussian fit to the histogram
[00:17:44 - 00:17:56] of the Gaussian noise probability density function.
[00:17:56 - 00:18:01] Okay, so for this noise sequence is not zero mean.
[00:18:01 - 00:18:09] What do you think the DC value of this noise signal is?
[00:18:09 - 00:18:15] 10, yep. So here the mean, so this is the DC value,
[00:18:15 - 00:18:17] is about 10.
[00:18:17 - 00:18:21] So along there, and so that's where the highest point
[00:18:21 - 00:18:26] of our noise distribution should be.
[00:18:26 - 00:18:31] This is only 100 points here, every increase in 10,000
[00:18:31 - 00:18:41] or whatever, we would get a much closer fit to that orange distribution.
[00:18:41 - 00:18:45] Okay, and so we have here, when I created this here,
[00:18:45 - 00:18:56] the variance for our Gaussian sigma squared was equal to 4.
[00:18:56 - 00:19:01] Okay, so we've got a DC signal of about 10,
[00:19:01 - 00:19:05] and then we've got a lot of additive noise on top of that.
[00:19:05 - 00:19:13] So one way to reduce the amount of noise is with a moving average filter.
[00:19:13 - 00:19:20] It's in the simplest moving average filter is we can average every two consecutive
[00:19:20 - 00:19:26] samples. So we can write this as what's known as a difference equation.
[00:19:26 - 00:19:38] So our output of the filter y of n is equal to a half of the current input,
[00:19:38 - 00:19:53] x of n plus the previous input x of n minus 1.
[00:19:53 - 00:20:10] And this is known as a difference equation.
[00:20:10 - 00:20:22] It's actually not a difference there, we've got a sum, but the general form of getting our output of our filter from the inputs
[00:20:22 - 00:20:29] or from previous outputs is known as a difference equation.
[00:20:29 - 00:20:34] Okay, so this on your microcontroller, this would be a few lines of C,
[00:20:34 - 00:20:40] where you would then be buffering the input, and you'd be adding the values together.
[00:20:40 - 00:20:44] To form a moving average.
[00:20:44 - 00:20:50] Possibly you've already done this in a 361 assignment, yep, good.
[00:20:50 - 00:21:01] You're going to hit a me. Okay, and so what can we say about our histogram now compared to without any average
[00:21:01 - 00:21:10] angle filtering? Yeah, it's all a variance, it's got narrower, it's less noisy.
[00:21:10 - 00:21:37] So just write that down. So histogram is less is narrower or smaller variance.
[00:21:37 - 00:21:46] Okay, so it's a moving average of two samples.
[00:21:46 - 00:21:52] We can do a bit more filtering if we take the moving average over more samples.
[00:21:52 - 00:21:57] So here we'll do four consecutive samples.
[00:21:57 - 00:22:08] So then y of n is equal to a quarter of the current input x of n plus the previous input.
[00:22:08 - 00:22:19] Plus the input one before that, and then plus the input one before that.
[00:22:19 - 00:22:31] In minus one, in minus two, in minus three. Okay, and when we add,
[00:22:31 - 00:22:36] we'll take this average over four now, we've got narrower Gaussian again.
[00:22:36 - 00:22:55] So we've reduced the noise variance. Okay, so we're getting closer today.
[00:22:55 - 00:23:08] What we think is our mean value of 10. Okay, so let's look if we increase this year again.
[00:23:08 - 00:23:13] So we've taken the moving average over in the general form.
[00:23:13 - 00:23:27] M capital M samples. So the general form then is our output y of n is equal to one over M samples.
[00:23:27 - 00:23:36] The sum from little m is zero to m minus one.
[00:23:36 - 00:23:39] Our input x.
[00:23:39 - 00:23:53] And then it's n minus m. Okay, and then the noise is greatly reduced.
[00:23:53 - 00:24:12] Okay, so it's settled on this sort of DC value of 10.
[00:24:12 - 00:24:28] What's happening at the beginning here? Yeah, so you start off with zeros in your buffer.
[00:24:28 - 00:24:46] So there's a delay here of m minus one samples before we get up to our expected DC value of 10.
[00:24:46 - 00:25:09] Okay, so this was with m is 25 samples. Okay, so by changing the number of samples that we're taking the moving average over,
[00:25:09 - 00:25:25] we're effectively changing the cutoff frequency of our low pass filter.
[00:25:25 - 00:25:32] Okay, if we think about what happens to our noise variance.
[00:25:32 - 00:25:40] So if we've got two random variables, we'll call x naught and x one.
[00:25:40 - 00:25:44] And they've got the same distribution such that there means both mu x and the
[00:25:44 - 00:25:52] the differences are both sigma squared x.
[00:25:52 - 00:26:05] So our output y is a half of x naught plus x one.
[00:26:05 - 00:26:17] So capital Y is the result of the output which is another random variable.
[00:26:17 - 00:26:33] So here this is modeling the two random variables, the moving average of over two consecutive samples.
[00:26:33 - 00:26:38] Okay, and if we consider what the mean of the result is.
[00:26:38 - 00:26:55] So the expected value of y is then equal to half the expected value of x naught plus half the expected value of x naught plus half the expected value of x naught.
[00:26:55 - 00:27:01] So the expected value of x one.
[00:27:01 - 00:27:06] And so we said that both x zero and x one had means of mu x.
[00:27:06 - 00:27:13] This becomes half mu x plus half mu x.
[00:27:13 - 00:27:30] So we get mu x. Okay, so that means our the mean of something two consecutive samples as they're going to be the same.
[00:27:30 - 00:27:36] still in that DC case we were looking at ten.
[00:27:36 - 00:27:41] But then what happens with the variance is where we win.
[00:27:41 - 00:27:46] So one result from statistics that you've probably seen before.
[00:27:46 - 00:27:51] If we take variance of some constant a times our random variable x,
[00:27:51 - 00:27:57] that's the same as the constant a squared times the variance of x.
[00:27:57 - 00:28:08] So then our variance after the filter.
[00:28:08 - 00:28:14] So this is sigma y squared.
[00:28:14 - 00:28:19] Then becomes a half squared gives us a quarter.
[00:28:19 - 00:28:27] The variance of x naught plus a quarter.
[00:28:27 - 00:28:30] The variance of x one.
[00:28:34 - 00:28:38] So the variance of x naught and the variance of x one are both sigma squared x.
[00:28:38 - 00:28:49] So sigma squared y is then equal to a quarter sigma x squared plus a quarter sigma x squared.
[00:28:49 - 00:28:54] So this is then a half sigma x squared.
[00:28:54 - 00:29:06] So that means the variance after our filter is half the variance of the input.
[00:29:06 - 00:29:20] And you can see that from those figures that the amount of noise on top of the DC 10 is effectively reduced with this moving average filter.
[00:29:20 - 00:29:22] In the general form.
[00:29:22 - 00:29:29] So for capital in samples that we're taking moving average over.
[00:29:29 - 00:29:46] the variance that the output sigma y squared is equal to one over capital in the variance of the input sigma x squared.
[00:29:46 - 00:29:54] Okay. So this moving average is then for our Gaussian noise.
[00:29:54 - 00:30:03] Reducing our noise variance each time for each sample that we take an average over.
[00:30:03 - 00:30:28] Okay. So there are two types of digital filters that we're going to look at.
[00:30:28 - 00:30:32] One's known as a finite impulse response filter.
[00:30:32 - 00:30:35] So that moving average we're looking at so far.
[00:30:35 - 00:30:40] We'll take the average over consecutive filters is a type of finite impulse response filter.
[00:30:40 - 00:30:45] And the other one we'll look at later is something known as infinite impulse response filter.
[00:30:48 - 00:30:54] Okay. So these finite impulse response filters like the moving average.
[00:30:54 - 00:31:00] Only rely on previous inputs and not previous outputs.
[00:31:00 - 00:31:05] So we can write then the output of the filter.
[00:31:05 - 00:31:22] Y then is equal to then the sum from little m is zero to capital in minus one.
[00:31:22 - 00:31:29] H of m. These are the filter weights.
[00:31:29 - 00:31:37] So that's the half half when we were doing a moving average over two samples.
[00:31:37 - 00:31:45] This is also the impulse response that will get into that more later.
[00:31:45 - 00:31:53] And then we have our inputs x and we have the inputs delayed by in samples.
[00:31:53 - 00:32:11] So this is the input to the filter.
[00:32:11 - 00:32:19] Okay. So one important point to note then is that this equation that gives us the output of the filter
[00:32:19 - 00:32:23] for a finite impulse response type of filter.
[00:32:23 - 00:32:33] If I filter what mathematical process is this equation describing?
[00:32:33 - 00:32:41] It is a way to average but the way it's been written as a sum of H of m x of n minus m
[00:32:41 - 00:32:44] is a convolution. Yes.
[00:32:44 - 00:32:49] So this is our old friend convolution coming back to get us.
[00:32:49 - 00:33:01] Okay. So we're convolving the inputs with the filter weights to get our output.
[00:33:01 - 00:33:17] Okay. So if we've got our filter say our moving average filter and we've got m coefficients.
[00:33:17 - 00:33:26] Say when we were doing a moving average filter over four coefficients,
[00:33:26 - 00:33:32] we'd have four non zero coefficients. They're all a quarter and the rest of the coefficients
[00:33:32 - 00:33:38] within the zero. So the impulse response is finite.
[00:33:38 - 00:33:44] It's just got four values. A quarter, a quarter, a quarter, a quarter, a quarter.
[00:33:44 - 00:33:50] And then lastly, these finite impulse response filters.
[00:33:50 - 00:33:53] The moving average filters are always stable.
[00:33:53 - 00:33:58] If we're just taking the average over the input values,
[00:33:58 - 00:34:03] then we're not going to make the system go unstable.
[00:34:03 - 00:34:08] Okay. The next type of filter we're going to look at,
[00:34:08 - 00:34:15] the impulse infinite impulse response filter can go unstable.
[00:34:15 - 00:34:19] But these moving average ones can't.
[00:34:19 - 00:34:27] Okay. So let's start looking at these other type of filters.
[00:34:27 - 00:34:37] So these have lots of different names. So our recursive filter or autoregressive filter or infinite impulse response filter
[00:34:37 - 00:34:45] has a difference with the filters we've been looking at previously, the finite impulse response or moving average filters.
[00:34:45 - 00:34:51] Now we can get our current output, not just from the inputs,
[00:34:51 - 00:34:55] but also from a previous output.
[00:34:55 - 00:35:01] So if we write a difference equation for a recursive filter,
[00:35:01 - 00:35:06] so here's a first order one, it's a fairly simple one.
[00:35:06 - 00:35:14] So our filter output, Y of n, is equal to alpha, some constant.
[00:35:14 - 00:35:26] The previous output Y of n minus 1, plus 1 minus this constant alpha times the current input X of n.
[00:35:26 - 00:35:40] So Y of n minus 1 is the previous output. X of n is the current input.
[00:35:40 - 00:35:51] And alpha is a constant. And this is often known as a smoothing constant or smoothing factor.
[00:35:57 - 00:36:04] Okay. And so this difference equation describes a loop pass filter.
[00:36:04 - 00:36:16] And that constant alpha, if we change that, we can change the cutoff frequency for the filter.
[00:36:16 - 00:36:28] Okay. And so because our, we have the feedback loop of our current output,
[00:36:28 - 00:36:35] depending on the previous output, these recursive filters can then go unstable.
[00:36:35 - 00:36:41] So if we have too large a value for alpha,
[00:36:41 - 00:36:45] and the impulse response will be infinite.
[00:36:45 - 00:36:51] If we put a 1 in to the system for the current input,
[00:36:51 - 00:36:56] that's just going to keep filtering through the system forever.
[00:36:56 - 00:37:01] I'll show you with a diagram later on.
[00:37:01 - 00:37:05] So this Y of n minus 1 is not 0.
[00:37:05 - 00:37:08] Then Y of n will not be 0.
[00:37:08 - 00:37:12] So the next time step Y of n minus 1 will not be 0.
[00:37:12 - 00:37:15] So then Y of n will not be 0 forever.
[00:37:15 - 00:37:21] It might be decaying, but the impulse response will never go to exactly 0.
[00:37:21 - 00:37:30] Okay. So let's look at that noise we had before.
[00:37:30 - 00:37:38] For example, so this was our mean or DC value was equal to 10,
[00:37:38 - 00:37:42] with additive white Gaussian noise.
[00:37:42 - 00:37:50] And so this is for a recursive filter defined as Y of n is equal to
[00:37:50 - 00:38:05] then is a value of 0.9 for alpha. So 0.9 of the previous output plus 0.1 times the current input x of n.
[00:38:05 - 00:38:16] Okay. So for this recursive filter, we've just got two coefficients to our filter.
[00:38:16 - 00:38:26] So it does converge to the mean value.
[00:38:26 - 00:38:34] It takes a wee while to get there here.
[00:38:34 - 00:38:45] So for the first about 20 samples, our transient response.
[00:38:45 - 00:38:53] And this is because Y of 0 is equal to 0.
[00:38:53 - 00:38:55] So for the first output is 0.
[00:38:55 - 00:39:08] So if we have 0.1 times the first input, which is a noisy value somewhere near 10,
[00:39:08 - 00:39:14] that gets multiplied by 0.1, we add in 0, then it becomes our new output.
[00:39:14 - 00:39:19] We multiply that by 0.9 plus 0.1 times a noisy value.
[00:39:19 - 00:39:28] So it takes a while for this to propagate through and rise up to get to our mean value of about 10.
[00:39:28 - 00:39:44] Okay, but so one advantage of this recursive filter is we only need these two coefficients.
[00:39:44 - 00:39:52] Whereas for the finite and possible response filter to get a similar noise level close to the DC value of 10,
[00:39:52 - 00:39:56] we needed many more coefficients.
[00:39:56 - 00:40:11] Okay, so that means less storage space for the coefficients and less computations in terms of multiplies and additions.
[00:40:11 - 00:40:14] Yeah, we'll certainly increase.
[00:40:14 - 00:40:21] So if you had a high value here for the 0.1, it would go up faster.
[00:40:21 - 00:40:33] Okay, so we've done the pass transform. So we've done Fourier transforms.
[00:40:33 - 00:40:39] And now we'll get onto the third main transform, which is the z transform.
[00:40:39 - 00:40:46] And so this is the discrete time version of the Laplace transform.
[00:40:46 - 00:40:50] So we're going to start off with our Laplace transform.
[00:40:50 - 00:40:52] Okay, previously.
[00:40:52 - 00:40:58] So h of s, so h of s is our transfer function.
[00:40:58 - 00:41:00] And the Laplace domain.
[00:41:00 - 00:41:15] And this was equal to the integral from 0 to infinity of our impulse response h of t.
[00:41:15 - 00:41:24] e to the minus s t.
[00:41:24 - 00:41:29] And that should be dt.
[00:41:36 - 00:41:45] Okay, so if we have here we're thinking about a digital signal.
[00:41:45 - 00:41:53] So if we have a sampling period capital T, so that's,
[00:41:53 - 00:41:57] that's a t is one over the sampling frequency.
[00:41:57 - 00:42:10] And so when we go from continuous time to our discrete time,
[00:42:10 - 00:42:21] we have time t is equal to our sample number n times our sampling period t.
[00:42:21 - 00:42:23] So n is an integer.
[00:42:23 - 00:42:34] And so to make this conversion from the Laplace transform to the z transform,
[00:42:34 - 00:42:47] we then let our z variable equal e to the little s capital T sample period.
[00:42:47 - 00:42:57] Okay, then that gives us our definition of the z transform capital H of z.
[00:42:57 - 00:43:01] And so this is our transfer function in the z domain.
[00:43:01 - 00:43:18] And so this is equal to or convert our continuous integral from time t is 0 to infinity from now
[00:43:18 - 00:43:20] we're dealing with a sample signal.
[00:43:20 - 00:43:27] So this is a sum from n is 0 to infinity.
[00:43:27 - 00:43:33] And then we have sampled our impulse response h of t.
[00:43:33 - 00:43:36] We get our sampled impulse response h of n.
[00:43:36 - 00:43:41] So this is our impulse response in the digital domain.
[00:43:41 - 00:43:55] And then when we substitute z, z is e to the s t with little t is capital n t.
[00:43:55 - 00:44:01] We then end up with z to the minus n.
[00:44:01 - 00:44:15] Okay, so that's a definition of the z transform.
[00:44:15 - 00:44:19] And so like the Laplace transform and the Fourier transform,
[00:44:19 - 00:44:24] we're not really going to be doing the integrals and summations and things.
[00:44:24 - 00:44:31] What we're going to do is we're going to have some key properties and key transform peers that we're going to use instead.
[00:44:31 - 00:44:41] Okay, so we'll start off looking at these in our last five minutes for today and then carry on with them tomorrow.
[00:44:41 - 00:44:47] Okay, so start off with our properties.
[00:44:47 - 00:44:52] And let's consider a z transform peer.
[00:44:52 - 00:45:03] So h of n is appear with capital H of z.
[00:45:03 - 00:45:19] Okay, so little h square brackets is the sample time domain and then capital letter with round brackets is in these z domain.
[00:45:19 - 00:45:29] Okay, so linearity means that if we scale our sample signals,
[00:45:29 - 00:45:36] so we've got h of n, multiplied by a and g of n multiplied by b,
[00:45:36 - 00:45:48] that means the z transform supers the position applies.
[00:45:48 - 00:45:52] And if we scale by a and one domain,
[00:45:52 - 00:46:11] we also need to scale by a, the other domains, this becomes then a h of z plus b times capital G of z.
[00:46:11 - 00:46:23] Okay, so we can do the z transform on the sum of two signals or we can do the z transform on each of them separately and then some,
[00:46:23 - 00:46:26] other transforms in that's equivalent.
[00:46:26 - 00:46:48] Okay, second one time shift or delay if we have our sample signal h of n and we delay it by m signals to h of n goes to h of z.
[00:46:48 - 00:46:59] And then we have a z to the minus m for the time shift or delay.
[00:46:59 - 00:47:15] Okay, and then lastly, we have our convolution theorem popping up as the transforms like it does in the last transform and the Fourier transform.
[00:47:15 - 00:47:25] So if we have two sample signals here x of n and h of n, which are convolved,
[00:47:25 - 00:47:33] what's that going to give us in the z domain?
[00:47:33 - 00:47:42] Yeah, product, yeah.
[00:47:42 - 00:47:50] So this is then going to give us x of z times h of z.
[00:47:50 - 00:48:20] So those are the three key properties of the z transform that's in the form of the sheet that you can have a look at it learned.
[00:48:20 - 00:48:28] And then we've got three common signals that we want to look at the z transform as well.
[00:48:28 - 00:48:33] So we'll look at the first one or two of those in the last two minutes.
[00:48:33 - 00:48:43] Okay, so we've got the unit impulse or Kronecker delta.
[00:48:43 - 00:48:57] So here we've got delta of zero as one and then delta of n is equal to zero.
[00:48:57 - 00:49:01] Fn is not equal to zero.
[00:49:01 - 00:49:11] So we've just got a value of one for inner zero. Otherwise, the unit impulse has zero value.
[00:49:11 - 00:49:25] Okay, so anyone guess what the z transform here of the unit impulse is going to be based on what we know about the last transform or the Fourier transform?
[00:49:25 - 00:49:26] One, yeah.
[00:49:26 - 00:49:38] So in the Fourier transform, delta function has a pair of constant value and it's the same for the z transform.
[00:49:38 - 00:49:40] So this is what we're going to write this out.
[00:49:40 - 00:49:53] So our definition of the z transform at z was the sum from little in zero to infinity of your delta in.
[00:49:53 - 00:49:57] Is our function times z to the minus n.
[00:49:57 - 00:50:01] And so the only value that's not zero was at inner zero.
[00:50:01 - 00:50:07] So we have one times z to the zero, which is equal to one.
[00:50:07 - 00:50:16] So for the unit impulse, they'll prevent this makes a z transform here with a constant value.
[00:50:16 - 00:50:17] One.
[00:50:17 - 00:50:27] So I'll stop writing and talking and you can finish off writing that down.
[00:50:27 - 00:50:37] It's 10, so we'll come back tomorrow and find out there's a tutorial tomorrow and we're looking at analog filters, transfer functions, etc.
[00:50:37 - 00:50:42] And I'll see you over on A3.
[00:50:42 - 00:50:47] That's not really what time, but I'll see you over there sometime tomorrow then back here for the tutorial.
[00:50:47 - 00:50:59] No, it's right.
[00:50:59 - 00:51:00] I saw that.
[00:51:00 - 00:51:01] I saw that.
[00:51:01 - 00:51:06] I haven't watched the picture.
[00:51:06 - 00:51:08] No, it's the right.
[00:51:08 - 00:51:10] I think it's two.
[00:51:10 - 00:51:11] I'm not even curious.
[00:51:11 - 00:51:12] But here's the other thing.
[00:51:12 - 00:51:15] So you're going to write the answer to the answer.
[00:51:15 - 00:51:16] Yeah, it's the same thing.
[00:51:16 - 00:51:17] I found the formula.
[00:51:17 - 00:51:18] Yes, it's the only two.
[00:51:18 - 00:51:19] I found the formula.
[00:51:19 - 00:51:20] I found the formula.
[00:51:20 - 00:51:21] I found the formula.
[00:51:21 - 00:51:22] I found the formula.
[00:51:22 - 00:51:23] I found the formula.
[00:51:53 - 00:51:54] That is like a Hawks Tech page.
[00:51:54 - 00:51:55] Do you know what kind of time I do?
[00:51:55 - 00:51:56] I'm getting it faster.
[00:51:56 - 00:51:57] Okay.
[00:51:57 - 00:51:58] Thank you.
[00:51:58 - 00:51:59] Have a great time for that.
[00:51:59 - 00:52:00] All right.
[00:52:00 - 00:52:01] Thank you very much.
[00:52:01 - 00:52:02] Cool.
[00:52:02 - 00:52:03] You were doing it a little months.
[00:52:03 - 00:52:04] Yeah, good.
[00:52:04 - 00:52:05] Thank you, Michael.
[00:52:05 - 00:52:06] Thank you.
[00:52:06 - 00:52:07] You're doing it a bit more sensitive.
[00:52:07 - 00:52:08] Yeah, it is.
[00:52:08 - 00:52:09] I think you know what it's interesting, but it's what's interesting.
[00:52:09 - 00:52:11] I thought you can throw it out.
[00:52:11 - 00:52:21] If I saw the formula you found it in the top of it, it was a quite dangerous edge.
[00:52:21 - 00:52:22] I did as well.
[00:52:22 - 00:52:24] A lot of fun business everywhere,

# ENMT301-26W Lecture 64 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `8422d0b5cee1052f11976504bcd290937d6b0742f0cb496fddac4fd0b35d073e`
Generated: 2026-06-06T07:23:58.081634+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:02 - 00:00:04] Okay, good afternoon everyone.
[00:00:04 - 00:00:06] So to start off with some notices.
[00:00:06 - 00:00:09] So we're going to tutorial tomorrow.
[00:00:09 - 00:00:11] I've got the questions up on Learn already.
[00:00:11 - 00:00:13] There are lots of questions this week.
[00:00:13 - 00:00:20] Help me pay you for the test in the mid-year exam period.
[00:00:20 - 00:00:24] I've also posted on Learn the assignment, the IMU assignment.
[00:00:24 - 00:00:30] So this is only with 5% of your grade as due at the end of the second week of term 3.
[00:00:30 - 00:00:33] So that's like about 8.5 weeks away.
[00:00:33 - 00:00:38] So it's probably not highly up your priorities at the moment.
[00:00:38 - 00:00:43] So the idea is basically you get given some measurements with an IMU
[00:00:43 - 00:00:50] and then you can use the IMU measurements on the robot to work out where you are.
[00:00:50 - 00:00:55] So hopefully it's applicable to your robot cup project as well.
[00:00:55 - 00:01:01] So I'll go briefly through this assignment on Friday for our lecture.
[00:01:01 - 00:01:05] So if you can have a little look through the assignments,
[00:01:05 - 00:01:10] the specifications on Learn and just see if you have any questions before then.
[00:01:10 - 00:01:18] Okay, and then lastly, I was able to book a room to help session during study week.
[00:01:18 - 00:01:23] Unfortunately, all the sort of flat spaces like this room or an
[00:01:23 - 00:01:32] as well as one 40 where I have books are really heavily used during that study week.
[00:01:32 - 00:01:38] So the only slot I could get for two hours was from 8 till 10 on a Friday morning.
[00:01:38 - 00:01:43] So we're going to have a one hour session between 9 till 10 because,
[00:01:43 - 00:01:49] I don't expect the high 10 at 8 o'clock and I'll be hard for me to get there too.
[00:01:49 - 00:01:53] And so I've got Harvey the CA to come as well.
[00:01:53 - 00:01:57] So maybe to prepare for that go through last year's tests,
[00:01:57 - 00:02:04] make a list of questions from the lectures tutorials and some make use of it as much as you can.
[00:02:04 - 00:02:10] Okay, so it's a little bit before I realize the test is in the second week of the exam period,
[00:02:10 - 00:02:16] but that's essentially impossible to do this help session during once exam start.
[00:02:16 - 00:02:18] So it's at the end of study week.
[00:02:18 - 00:02:27] So the timing was not my choice, but okay, so that's all bad mental things.
[00:02:27 - 00:02:31] So let's go back to where we were on Friday.
[00:02:31 - 00:02:39] So we were looking at the DFT and then a particular concept of spectral leakage.
[00:02:39 - 00:02:42] So when we take the discrete Fourier transform,
[00:02:42 - 00:02:48] if we just take the data values, essentially we're multiplying by a rectangular function.
[00:02:48 - 00:02:53] So if we consider a sign wave, if we take the DFT of that,
[00:02:53 - 00:02:56] we're multiplying by a rectangular function on the time domain,
[00:02:56 - 00:03:02] which means then in the Fourier domain we're convolving with a sync function.
[00:03:02 - 00:03:10] And so that means instead of having in the Fourier domain for our sign or cosine through joules,
[00:03:10 - 00:03:17] because we've convolved it by a sync function because we're multiplying by a rectangular function on the time domain,
[00:03:17 - 00:03:23] this convolution by the sync then spreads the energy to other frequencies.
[00:03:23 - 00:03:29] So we're leaking the frequency content to other frequencies.
[00:03:29 - 00:03:35] And so this example here with the cosine with a rectangular window in essence,
[00:03:35 - 00:03:40] we have a wider main lobe of our, where our Delvers should be,
[00:03:40 - 00:03:49] and then we have these side lobes from the side lobes of the sync function that we've convolved with our Delta function.
[00:03:49 - 00:03:58] Okay, so the rectangular window, if we do nothing, is really bad for the ringing of the side lobe.
[00:03:58 - 00:04:03] So if the bottom figure shows the Fourier content,
[00:04:03 - 00:04:10] well, frequency domain content for the four windows on the top, the colors match from the top to bottom.
[00:04:10 - 00:04:17] So if we do nothing, we're in essence multiplying by a rectangular window and we're convolving with a sync.
[00:04:17 - 00:04:24] And the sync has the highest ringing at the higher frequencies and these side lobes.
[00:04:24 - 00:04:33] If we use a smoother window function, so if we mulled a pi out, data values by say the having window, the green curve,
[00:04:33 - 00:04:41] before we take the DFT, then we get much lower ringing in the side lobes.
[00:04:41 - 00:04:48] And so then we finished on the example of that on Friday.
[00:04:48 - 00:04:57] So here we've got two frequency components, one of 100 hertz, and then a much smaller one at 125 hertz.
[00:04:57 - 00:05:04] And so if we don't do any windowing, we are in it,
[00:05:04 - 00:05:07] since using the rectangle window.
[00:05:07 - 00:05:26] And so with the rectangular window, the 125 hertz component is masked by the side lobe.
[00:05:26 - 00:05:35] So that's the blue curve with the rectangle window.
[00:05:35 - 00:05:42] Okay, so these, there is something at 125 hertz, but with this ringing,
[00:05:42 - 00:05:47] usually our convolution with a sync in the frequency domain, it's not that apparent.
[00:05:47 - 00:06:09] But if we then use a having window, then the 125 hertz component is visible with the hamming window.
[00:06:09 - 00:06:26] Like most things in life, you don't get everything for free.
[00:06:26 - 00:06:31] So while you're winning on the side lobes, you're losing out on the main lobes.
[00:06:31 - 00:06:45] So our rectangular function then has a, sorry, our hamming window has a wider main lobe, the hamming window.
[00:06:45 - 00:07:13] Okay, so we've been discussing the discrete Fourier transform.
[00:07:13 - 00:07:15] So we've got a sample.
[00:07:15 - 00:07:18] It's been, a signal, it's been sampled.
[00:07:18 - 00:07:21] So we've got a discrete time signal.
[00:07:21 - 00:07:32] And we take the discrete Fourier transform of that to get our Fourier spectrum, which is also discrete with the D of t.
[00:07:32 - 00:07:35] Now the D of t, not just rewrite our equation here.
[00:07:35 - 00:07:40] So x of k is our discrete spectrum.
[00:07:40 - 00:07:55] So this is a sum here from n is 0 to n minus 1 of our sample values x of n times our convex exponential here,
[00:07:55 - 00:08:01] e to the minus j to pi k in over the number of samples at capital N.
[00:08:01 - 00:08:17] Okay, so when we're taking the discrete Fourier transform for each value, for each value of k,
[00:08:17 - 00:08:22] we need to multiply x of n by e to the minus j to pi k in.
[00:08:22 - 00:08:29] Okay, so we have n complex multiplications within the side of the sum.
[00:08:29 - 00:08:32] And then we're summing from n is 0 to n minus 1.
[00:08:32 - 00:08:39] So we have then n times n n squared multiplications, complex multiplications,
[00:08:39 - 00:08:42] because that can be complex numbers.
[00:08:42 - 00:08:45] It's compute our discrete Fourier transform.
[00:08:45 - 00:08:49] So as the number of samples we have in our single increases,
[00:08:49 - 00:08:55] then the computationally intensity goes up within squared.
[00:08:55 - 00:09:02] Okay, so this makes the D of t prohibitive and we've got a really long sequence.
[00:09:02 - 00:09:10] And so there is a much faster algorithm designed in the 1960s called the fast Fourier transform.
[00:09:10 - 00:09:13] So this is much more efficient.
[00:09:13 - 00:09:19] It does special factorizations of these complex exponentials that we can reuse.
[00:09:19 - 00:09:26] And this fast Fourier transform has a computational complexity of n log n.
[00:09:26 - 00:09:28] So it's log to the base 2.
[00:09:28 - 00:09:38] Okay, and so the f of t is most efficient when n is a power of 2.
[00:09:38 - 00:09:43] If we have n is 2, 4, 8, 16, 32, 64, etc.
[00:09:43 - 00:09:57] If our sample x of n is not a power of 2, then we add 0s to our sequence to increase the sequence length to make it a power of 2.
[00:09:57 - 00:10:08] So that also has the effect, as we saw last week, of these adding these 0s, 0 padding increases the resolution of our spectrum.
[00:10:08 - 00:10:17] Okay, so, yeah.
[00:10:17 - 00:10:22] So bigger notation, you might have seen before, so this signifies the computational complexity.
[00:10:22 - 00:10:31] It's n squared for the D of t and it is n log n of the f of t.
[00:10:31 - 00:10:51] Okay, so for example, then if we've got our sequence x of n is equal to 1, 2, 3, 4, 5.
[00:10:51 - 00:10:56] And we wanted to take a fast Fourier transform of that.
[00:10:56 - 00:10:59] We would then add 3, 0s.
[00:10:59 - 00:11:05] So its extent is then, so these are the added 0s.
[00:11:05 - 00:11:19] So the extent of x of n is equal to 8, which is 2 to the power of 3.
[00:11:19 - 00:11:34] Okay, so these factorizations of the complex expanentials, most efficient when it's a power of 2.
[00:11:34 - 00:11:53] So the speed up from the D of t to the f of t is greatest if we have our sequence length of power of 2.
[00:11:53 - 00:12:01] Okay, so let's just have a look at, so this is a graph then of, so in here is our sequence length.
[00:12:01 - 00:12:09] And then on the way axis we have the number of multipliers.
[00:12:09 - 00:12:18] And so for the D of t it's going up as n squared.
[00:12:18 - 00:12:26] So it's going up very steeply, whereas for the f of t it's going up within log to the base 2 of n.
[00:12:26 - 00:12:34] So it's going up, but not anywhere near as much as for the D of t.
[00:12:37 - 00:12:49] Okay, so for example if we have our sequence length n is 1,024 samples,
[00:12:49 - 00:13:08] we then have the D of t requires then n squared, which is then 1,024 squared.
[00:13:08 - 00:13:13] 1,024 is 2 to the power of 10.
[00:13:13 - 00:13:18] So that's 2 to the power of 10 squared is 2 to the power of 20 multiplications,
[00:13:18 - 00:13:39] whereas the f of t requires n log to the base 2 of n, which is n's 1,024.
[00:13:39 - 00:13:48] The log to base 2 of 1024 is 10, that gives us 1,240.
[00:13:48 - 00:14:02] So 2 to the power of 20 is an absolutely massive number, whereas 10,000 is not.
[00:14:02 - 00:14:12] Okay, so when you're doing furry transforms in mat level python, you'll be using the fastest furry transform,
[00:14:12 - 00:14:24] the f of t, and to the D of t that we've done an example of is computationally really inefficient.
[00:14:24 - 00:14:30] So the both infunctions in mat level python use the C50 or more recent variant of the f of t,
[00:14:30 - 00:14:33] which is called the fastest furry transform in the waste.
[00:14:33 - 00:14:52] Okay, so something else that comes out of the furry transform is something that is a spectrogram.
[00:14:52 - 00:15:03] And so that is a graph that will tell us how the frequency content of a signal changes waste time.
[00:15:03 - 00:15:11] So if you've got a pure tone, it's a sign wave, its frequency content doesn't change the time, it's constant.
[00:15:11 - 00:15:16] But in reality, for a signal, the frequency content is going to change with time.
[00:15:16 - 00:15:20] So my voice is changing frequency as I speak.
[00:15:20 - 00:15:27] So if we consider some sort of signal, I'll do here some sort of chip here.
[00:15:27 - 00:15:36] So the frequency is then increasing of the signal.
[00:15:36 - 00:15:43] So we're taking samples, hopefully, equally spaced in my figure here.
[00:15:43 - 00:15:55] Okay, so if I took the f of t of that signal,
[00:15:55 - 00:16:03] I would get the sum of all the frequencies, I wouldn't be able to localize them in time.
[00:16:03 - 00:16:16] Okay, so what we do with the spectrogram is we then take the f of t over someone window,
[00:16:16 - 00:16:28] say over in samples here, and then let's then take another f of t over another window.
[00:16:28 - 00:16:38] And we're going to keep doing overlapping Fourier transforms over in samples.
[00:16:38 - 00:16:56] And then we can plot a figure where we have in our figure we've got then time on the x-axis.
[00:16:56 - 00:17:03] And frequency on the y-axis.
[00:17:03 - 00:17:12] So this is going to be allow us to work out where the different frequencies happen in time.
[00:17:12 - 00:17:26] So that first window that I drew in blue is going to then have a frequency component at this first time level,
[00:17:26 - 00:17:31] which is largest at a very low frequency.
[00:17:31 - 00:17:48] And then the one that I drew in black at our second instance in time is then going to have a higher frequency.
[00:17:48 - 00:18:03] Okay, so there's some overlap to make this smooth rather than abrupt changes.
[00:18:03 - 00:18:21] Okay, and in this figure this is a graph and the magnitude of the Fourier transformers then shown is a higher intensity at each point.
[00:18:21 - 00:18:32] So I've got an example of a spectrogram, a real spectrogram on the mix slide, which is from an Antarctic kilowheils.
[00:18:32 - 00:18:42] So this is from some research at UC on the calls of these kilowheils.
[00:18:42 - 00:18:44] So let's have a look at that.
[00:18:44 - 00:18:52] Okay, so this is the spectrogram of an Antarctic kilowheil.
[00:18:52 - 00:18:55] So this is basic form here.
[00:18:55 - 00:18:59] So the figure has time on the x-axis.
[00:18:59 - 00:19:05] Frequency on the y-axis.
[00:19:05 - 00:19:15] And then the color is the intensity, which is the magnitude of the Fourier transform squared.
[00:19:15 - 00:19:31] Okay, so what do we see in this figure?
[00:19:31 - 00:19:37] What's interesting? So what do you think these lines are?
[00:19:37 - 00:19:53] So this is where these are known as echo-location clicks.
[00:19:53 - 00:19:59] So these are broadband signals, broadband signals.
[00:19:59 - 00:20:07] So this frequency content over the whole range of frequencies from 0 to 140 hertz there.
[00:20:07 - 00:20:12] And so these are the noises the whales make for working out where they are.
[00:20:12 - 00:20:26] So we'll send out a burst of frequencies and then they're waiting for the reflection to come back to tell them how far away the ice or the ground is.
[00:20:26 - 00:20:34] Okay, so those vertical lines are the equilocation signals.
[00:20:34 - 00:20:43] And then for example, these ones here are the calls.
[00:20:43 - 00:20:47] So that's when they're talking to the rest of their pod.
[00:20:47 - 00:20:50] And that's right, where the whales are.
[00:20:50 - 00:21:01] And so there it's kind of a chip where the frequency content here is increasing with time.
[00:21:01 - 00:21:09] And then you'll notice that these signals here are repeated at higher frequencies.
[00:21:09 - 00:21:25] And so those are then the harmonics of the lower frequency.
[00:21:25 - 00:21:28] So that's a spectrogram.
[00:21:28 - 00:21:34] That's a way to then distinguish the frequency component from the time component.
[00:21:34 - 00:21:37] So you can work out where in the signal certain frequencies come from.
[00:21:37 - 00:21:43] otherwise if we just illustrate if if they would all be superimposed at the same point in time.
[00:21:43 - 00:21:56] Okay, I think we've got one more slide on this lot and then we'll move on to the sensors.
[00:21:56 - 00:22:08] Okay, and so lastly, if we're doing a convolution, it's more efficient to do this in the frequency domain than in the time domain.
[00:22:08 - 00:22:28] So if we're convolving two signals, x of n, convolve with h of n, in the frequency domain we have x of k times h of k.
[00:22:28 - 00:22:34] So this is in frequency domain, n squared multiplications.
[00:22:34 - 00:22:38] There's a complex multiplication.
[00:22:38 - 00:22:48] Okay, so then a more efficient way of doing this is we get x of n.
[00:22:48 - 00:22:54] We zero-pedit, so is length is a power of two.
[00:22:54 - 00:23:05] And then we take a Fourier transform to get us here x of k and h of k.
[00:23:05 - 00:23:23] So the if if t is of the order of n log to the base two n, we multiply them together.
[00:23:32 - 00:23:37] So it's n multiplication.
[00:23:37 - 00:23:48] So we have n multiplications here x of k times h of k.
[00:23:48 - 00:23:54] And if we did the convolution in the time domain we would have n squared multiplications.
[00:23:54 - 00:24:05] and then the computational complexity of the inverse Fourier transform is the same as the inverse
[00:24:05 - 00:24:08] fast Fourier transform is the same as the fast Fourier transform.
[00:24:08 - 00:24:13] And that is also n log to the base two n.
[00:24:13 - 00:24:24] Okay, so for this method of dealing with convolution where we take two Fourier transforms,
[00:24:24 - 00:24:32] the model of k, n and inverse fast Fourier transform, the total is then we have three
[00:24:32 - 00:24:40] Fourier transforms that's three lots of n log to the base two n plus n multiplications.
[00:24:40 - 00:24:51] Okay, and that's going to be less than n squared for large values of n.
[00:24:51 - 00:25:13] Okay, and then last note is that the if if t size if we're doing this convolution has to be greater than the extent of x
[00:25:13 - 00:25:28] n plus the extent of h of n minus 1.
[00:25:28 - 00:25:34] Okay, this is to avoid the problems of circular convolution.
[00:25:34 - 00:26:11] Okay, so that's the end of our if if t is the if t is zero.
[00:26:11 - 00:26:17] And we're going to look for next lecture or two on some different senses.
[00:26:17 - 00:26:24] So I'll just close this one and we'll get into the senses.
[00:26:24 - 00:27:27] Okay, so we're going to look at some of the senses now.
[00:27:27 - 00:27:33] And so the algorithms behind them and some of the practical implementation details as well.
[00:27:33 - 00:27:38] So I've chosen two to go on the t's light here.
[00:27:38 - 00:27:51] So the one on the left is a time of flight sensor and the one on the right here is infrared range sensor.
[00:27:51 - 00:27:57] Okay, please look familiar from your robot cup kits.
[00:27:57 - 00:28:09] Yeah, so they might be slightly different versions of the ones you're using, but similar part numbers that I could find pictures for.
[00:28:09 - 00:28:21] Okay, so these are the two types of senses that we're going to look into over the next couple of lectures.
[00:28:21 - 00:28:28] Okay, so we're basically going to be looking at three types of processing to start with.
[00:28:28 - 00:28:35] So so now radar and lighter all operate in a very similar manner.
[00:28:35 - 00:28:41] So they've got these acumen sonar is standing for sound navigation and ranging.
[00:28:41 - 00:28:44] So the ranging is the range or distance.
[00:28:44 - 00:28:50] Radar is radio detection and ranging and lighter is light detection and ranging.
[00:28:50 - 00:28:57] Okay, so obviously here the left we've got sonar.
[00:28:57 - 00:29:01] I'm going to use train use capitals for the whole thing because of acronym.
[00:29:01 - 00:29:07] Some people just write it as a lower case word now because it's been around for so long.
[00:29:07 - 00:29:11] But the basic idea is we've got our boat here.
[00:29:11 - 00:29:29] It's got a transducer that's sending out a signal and we're trying to work out from the echo of the signal that sent out the range to the ground or to a fish or whatever.
[00:29:29 - 00:29:35] So that's a sonar was originally invented in the lead up to World War one.
[00:29:35 - 00:29:41] So it was looking for icebergs and then submarines through World War one.
[00:29:41 - 00:29:52] Radar we have in the middle here where we again looking for this range.
[00:29:52 - 00:29:59] And so radar was developed in the lead up to World War two and sort of eight countries independently
[00:29:59 - 00:30:03] created their own radar systems for World War two.
[00:30:03 - 00:30:09] New Zealand was quite involved with the British effort they were sharing their system with us.
[00:30:09 - 00:30:17] And then light-arshed on the right here from a drone is we have from our drone.
[00:30:17 - 00:30:20] We're trying to work out the range so the distance to the ground there.
[00:30:20 - 00:30:22] So this is lighter.
[00:30:22 - 00:30:29] And then the first lighter systems were kind of generated in this space age.
[00:30:29 - 00:30:40] The six season seventies some of the probes orbiting the moon's are sending off light signals getting the reflections and then able to map the moon and things.
[00:30:40 - 00:30:53] Okay so these all operate on similar signal processing ideas with slightly different technology.
[00:30:53 - 00:31:03] So for sonar we have a transducer or transducers.
[00:31:03 - 00:31:14] So we can have one transducer which is both the sending and receiving or we can have one that sends and then one that receives.
[00:31:15 - 00:31:20] Because the transducer takes an electrical signal.
[00:31:20 - 00:31:25] It's a voltages and then it's converting that to a sound.
[00:31:25 - 00:31:29] So pressure signal and the water.
[00:31:29 - 00:31:35] And then when it receives a pressure signal it converts that back to a voltage.
[00:31:35 - 00:31:47] Okay and so with radar we have this antenna.
[00:31:47 - 00:31:58] It is then sending out the signal and it's also receiving the reflection here from the target plane.
[00:31:58 - 00:32:00] And then lastly with laser.
[00:32:00 - 00:32:08] The light are starting we have a laser on the light out which is sending a signal and then we've got our photo diode.
[00:32:08 - 00:32:14] It does the receiving.
[00:32:14 - 00:32:23] Okay so the photo diode is receiving light signals and converting it to a voltage signal.
[00:32:23 - 00:32:36] Okay so there are two different operational modes for these three methods.
[00:32:36 - 00:32:39] So the first one.
[00:32:39 - 00:32:40] Pulse echo operation.
[00:32:40 - 00:32:42] That's what will concentrate on.
[00:32:42 - 00:32:47] This is calculating distance based on the length of time.
[00:32:47 - 00:32:55] It takes for all the time of flight for the signal to reach the target.
[00:32:55 - 00:33:01] Echo and return to the transmitter.
[00:33:01 - 00:33:04] Okay these pulse echo operations.
[00:33:04 - 00:33:11] So we're sending short duration pulses and it's normally of a broadband signal.
[00:33:11 - 00:33:19] So quite often frequency modulated or chip signal where the frequency is changing with time.
[00:33:19 - 00:33:24] So the second mode that we won't concentrate on is the Doppler mode.
[00:33:24 - 00:33:29] So this is a speed measurement of a distance measurement based on the Doppler effect.
[00:33:29 - 00:33:36] So we've done it in the high school physics hopefully where when the ambulance is coming towards you the frequencies higher than when it's going away from you.
[00:33:36 - 00:33:44] Okay so for Doppler mode we use narrowband signal to essentially assign or cosine.
[00:33:44 - 00:33:49] So single frequency but of a longer duration.
[00:33:49 - 00:33:57] We're not looking for the echo of the pulse so we have a longer signal.
[00:33:57 - 00:34:01] Okay so let's think about time of flight.
[00:34:01 - 00:34:13] So this is the time delay for the signal to go from the transmitter to the target and back to the receiver.
[00:34:13 - 00:34:15] So I'll just draw a little diagram.
[00:34:15 - 00:34:21] So we've got our transducer here.
[00:34:21 - 00:34:27] It's sending out a pulse which has then got a spherical wave front.
[00:34:27 - 00:34:39] We've got some then target.
[00:34:39 - 00:34:46] We were trying to estimate half our way that target is.
[00:34:46 - 00:34:54] And then that target is going to reflect the wave fronts that hit it.
[00:34:54 - 00:35:08] So then the red wave fronts here are the wave fronts being reflected from the target back to the transducer.
[00:35:08 - 00:35:20] Transmitter.
[00:35:20 - 00:35:24] Okay so then our time of flight will call tau.
[00:35:24 - 00:35:32] This is universal seconds.
[00:35:32 - 00:35:41] So this instance here is the range.
[00:35:41 - 00:35:52] It's range.
[00:35:52 - 00:35:57] And that's a distance as a meter.
[00:35:57 - 00:36:08] And we divide by the speed of propagation which is speed.
[00:36:08 - 00:36:10] So this is meter per second.
[00:36:10 - 00:36:15] Okay is there right?
[00:36:15 - 00:36:25] So the range is from the transducer to the target.
[00:36:25 - 00:36:28] But we're sending a signal out.
[00:36:28 - 00:36:30] That's going to come back.
[00:36:30 - 00:36:35] So actually the total distance is two times the range.
[00:36:35 - 00:36:42] Okay so the two here is there and back.
[00:36:42 - 00:36:50] Okay so that equation is actually a formula sheet.
[00:36:50 - 00:36:53] Either know it's fairly simple.
[00:36:53 - 00:36:56] Physics that you could work out yourselves.
[00:36:56 - 00:36:58] But on there anyway.
[00:36:58 - 00:37:01] Okay so it's the amount of time it takes for the signal.
[00:37:01 - 00:37:03] You've seen it up from your transmitter.
[00:37:03 - 00:37:07] Hit the target and come back to you receiving it again.
[00:37:07 - 00:37:25] Okay so let's look at some of these tone bursts.
[00:37:25 - 00:37:29] So the top here we've got a transmit signal.
[00:37:29 - 00:37:33] And the bottom we've got a receive signal.
[00:37:33 - 00:37:38] So these are a function of time along the x axis here.
[00:37:38 - 00:37:57] Okay so we've got some duration that we're going to be sending our signal over T.
[00:37:57 - 00:37:59] Duration.
[00:37:59 - 00:38:08] The time of flight is the time to get the first echo.
[00:38:08 - 00:38:10] So this is the first echo.
[00:38:10 - 00:38:20] Then we'll get a second echo off another scatter of 30 echo etc.
[00:38:20 - 00:38:30] Okay so it's in this from the start of this pulse to the start of the return pulse is our tau.
[00:38:30 - 00:38:31] Our time of flight.
[00:38:31 - 00:39:14] And we also have then here that we've got some period P which is then the total period
[00:39:14 - 00:39:19] including the zeros where we're not transmitting of our signal.
[00:39:19 - 00:39:37] Okay so we're also going to have some amplitude of our echo.
[00:39:37 - 00:39:51] And so we'll look at that in a bit as about what determines the size of our echo.
[00:39:51 - 00:39:55] It depends on the target, the medium etc.
[00:39:55 - 00:40:16] Okay so we'll just look at some different types of,
[00:40:16 - 00:40:18] or different modes.
[00:40:18 - 00:40:22] So we've got four different here and so there and then different speeds,
[00:40:22 - 00:40:24] different media as well.
[00:40:24 - 00:40:30] And for all of them we'll go a range of one meter and we look at the time of flight
[00:40:30 - 00:40:33] for this range of one meter.
[00:40:33 - 00:40:37] So an air sonar is using sound waves and air.
[00:40:37 - 00:40:44] So the 340 meters per second is the speed of sound in air.
[00:40:44 - 00:40:47] And whereas so now traditional sonar is in water,
[00:40:47 - 00:40:56] this is a sea water which has a speed of sound of 1500 meters per second.
[00:40:56 - 00:41:01] And so again the time of flight is order of milliseconds.
[00:41:01 - 00:41:12] And so radar and lighter are both sending waves,
[00:41:12 - 00:41:14] and the sound waves are electromagnetic waves.
[00:41:14 - 00:41:17] So these are then travelling at the speed of light.
[00:41:17 - 00:41:24] So that's three times 10 to the eight meters per second.
[00:41:24 - 00:41:36] Okay so that means for radar and lighter,
[00:41:36 - 00:41:40] if we're measuring a distance of approximately one meter,
[00:41:40 - 00:41:43] then these are very small times.
[00:41:43 - 00:41:57] Okay so that means that we're going to have to have very complicated signal processing and electronics.
[00:41:57 - 00:42:50] So let's have a look at what determines the size of the amplitude that we get from an echo.
[00:42:50 - 00:42:58] So if you say this determines this is determined by how far away the target is from our transmitter.
[00:42:58 - 00:43:04] And the two reasons for one, for what we call spreading losses,
[00:43:04 - 00:43:13] as the wave target gets further away from the transmitter,
[00:43:13 - 00:43:17] we see a smaller part of the wave front.
[00:43:17 - 00:43:36] And then there's also absorption losses whereby some of the energy of signal we're sending is going to be absorbed by the medium.
[00:43:36 - 00:43:50] Okay it's also going to be determined by the wavelength or frequency,
[00:43:50 - 00:43:58] because these two are linked by the speed of the wave.
[00:43:58 - 00:44:01] And then it also depends on our target.
[00:44:01 - 00:44:07] So if we've got a fish here with our cylinder and the fish find up,
[00:44:07 - 00:44:16] it's going to give a different magnitude of reflection to the sea floor.
[00:44:16 - 00:44:23] So it's size, it's orientation, and also the roughness,
[00:44:23 - 00:44:27] the redraw on my fish.
[00:44:27 - 00:44:31] It's going to determine how much gets reflected.
[00:44:31 - 00:44:48] Okay so this is our range to the ground, and then also if we've got a different target here,
[00:44:48 - 00:44:50] we'll have a different range.
[00:44:50 - 00:45:11] Okay so we can classify our targets into two different types of targets.
[00:45:11 - 00:45:16] The first one is known as specular targets,
[00:45:16 - 00:45:22] where the target acts essentially as a mirror.
[00:45:22 - 00:45:29] And this is the case where the target as smooth as compared to the wavelength.
[00:45:29 - 00:45:44] So this is where typically lambda is greater than the RMS roughness over 8.
[00:45:44 - 00:45:48] Okay so then this is known as specular.
[00:45:48 - 00:45:51] So it's impacting as a mirror here if this is our transducer,
[00:45:51 - 00:45:59] and we're sending out a signal,
[00:45:59 - 00:46:02] and setting here this is our target.
[00:46:02 - 00:46:13] And purple, then this is hopefully high school or fishy physics,
[00:46:13 - 00:46:16] then the angle of reflection,
[00:46:16 - 00:46:31] the angle of reflection is equal to the angle of incidence.
[00:46:31 - 00:46:40] Okay so if we've got a specular target here,
[00:46:40 - 00:46:43] so in this example here then at this angle,
[00:46:43 - 00:46:47] not much is going to be reflected back to our transducer.
[00:46:47 - 00:47:05] Okay and then the second type of target,
[00:47:05 - 00:47:11] it's known as the fuse targets.
[00:47:11 - 00:47:15] This is where the targets are rough compared to the wavelength.
[00:47:15 - 00:47:21] So this case we have the wavelength of the signal we're transmitting
[00:47:21 - 00:47:25] is less than the RMS roughness over 8.
[00:47:25 - 00:47:38] And so these diffuse targets scatter light then weekly in all directions.
[00:47:38 - 00:47:43] So the incident light here is black,
[00:47:43 - 00:47:46] the specular targets are like a mirror,
[00:47:46 - 00:47:49] the angle of incidence is angle of reflection,
[00:47:49 - 00:47:51] whereas if we've got a rough target,
[00:47:51 - 00:47:56] diffuse target then we get the red arrows here where we get reflections
[00:47:56 - 00:48:00] in many directions.
[00:48:00 - 00:48:16] Okay we'll just finish briefly.
[00:48:16 - 00:48:19] This is a equation you've hopefully seen before as well,
[00:48:19 - 00:48:23] that the speed of propagation of our wave
[00:48:23 - 00:48:28] is equal to the frequency times the wavelength.
[00:48:28 - 00:48:33] So C is the speed in meters per second.
[00:48:33 - 00:48:35] If is the frequency,
[00:48:35 - 00:48:45] Hertz and lambda is the wavelength in meters.
[00:48:45 - 00:48:49] So if we increase the frequency, the wavelength goes down,
[00:48:49 - 00:48:51] proportionately if we increase the wavelength,
[00:48:51 - 00:48:54] the frequency goes down proportion as well.
[00:48:54 - 00:48:58] So then if it's there for today we'll go through some of the values in the table.
[00:48:58 - 00:49:01] Tomorrow and then carry on with our sensors,
[00:49:01 - 00:49:03] the rest of tomorrow.
[00:49:03 - 00:49:12] Cool, see you tomorrow afternoon.
[00:49:12 - 00:49:19] Sure.
[00:49:19 - 00:49:20] Why?
[00:49:20 - 00:49:22] Yeah.
[00:49:22 - 00:49:25] Well the thunderline signal processing is the same,
[00:49:25 - 00:49:27] I mean the mechanics are different.
[00:49:27 - 00:49:31] You're sitting it out with an antenna versus sitting out a light signal
[00:49:31 - 00:49:34] from a laser and getting it back from a photo diode.
[00:49:34 - 00:49:40] So the instrumentation is different,
[00:49:40 - 00:49:44] but the signal processing is mostly the same.
[00:49:44 - 00:49:47] You're still, the speed of the wave is the same.
[00:49:47 - 00:49:50] You're dealing with different frequencies,
[00:49:50 - 00:49:53] the rate as a radio, wavelength.
[00:49:53 - 00:49:55] So they go different frequencies.
[00:49:55 - 00:49:57] Here's different wavelengths.
[00:49:57 - 00:49:59] The wavelength here is quite a lot different.
[00:49:59 - 00:50:03] And so then things like what's going to
[00:50:03 - 00:50:07] how that target reacts in terms of its roughness,
[00:50:07 - 00:50:11] whether it's specular or diffuse,
[00:50:11 - 00:50:14] it's going to be different and these sorts of things.
[00:50:14 - 00:50:17] So yeah, there are several differences.
[00:50:17 - 00:50:19] Mostly, they're the same thing.
[00:50:19 - 00:50:22] And so it is pretty similar except it's much slower speed.
[00:50:22 - 00:50:25] And good.
[00:50:25 - 00:50:26] That works.
[00:50:26 - 00:50:40] Yes, similar.
[00:50:40 - 00:50:42] Yes, similar.
[00:50:42 - 00:50:46] Yeah, that's why I say, for a lot of zones, right?

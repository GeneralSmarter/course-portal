# ENMT301-26W Lecture 49 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_49_audio_16k_mono_32k.mp3`
Source audio SHA-256: `ecfb716a822de15909a461c8eb203df30ff79871f2dc85276f7a27cbedcc660b`
Generated: 2026-06-06T06:54:02.614556+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:01 - 00:00:08] Okay, good afternoon everyone. Sorry, I just have in some technical difficulties, but we'll get resolved for a clock. So that's good
[00:00:10 - 00:00:12] So today we're gonna finish off our
[00:00:13 - 00:00:14] section on
[00:00:14 - 00:00:19] For a transforms and then we're gonna start looking at filtering with analog circuits
[00:00:20 - 00:00:26] So how we can say remove low frequency noise or high frequency noise with
[00:00:26 - 00:00:29] Circuit made out of resistors capacitors and inductors
[00:00:30 - 00:00:36] So then last week on Friday we were looking at the convolution theorem
[00:00:36 - 00:00:38] for for a transform
[00:00:38 - 00:00:40] So if we've got two
[00:00:40 - 00:00:43] Segmental say x of t and eight of t here
[00:00:44 - 00:00:46] convolved in the time domain
[00:00:46 - 00:00:50] That means in the frequency of the main we multiply their spectra
[00:00:51 - 00:00:56] Okay, and so this is a good way to overcome having to do the convolution integral which is
[00:00:57 - 00:01:03] Messy and expensive doing it on a computer. It's much easier to do it as a multiplication
[00:01:04 - 00:01:06] Okay, then lastly
[00:01:06 - 00:01:10] because on the symmetry of the forward and inverse for a transforms if we've got two
[00:01:12 - 00:01:19] Spectra convolved in the free domain that means their time domain signals will be multiplied together
[00:01:20 - 00:01:25] Okay, so that was the convolution theorem and then we started off with an example
[00:01:26 - 00:01:30] And so this is an example of a cosine first
[00:01:31 - 00:01:33] Which you might use in sona or radar?
[00:01:34 - 00:01:37] And so it's a burst of a fixed duration
[00:01:38 - 00:01:40] capital T and
[00:01:40 - 00:01:43] Then it's a cosine with a frequency if not
[00:01:44 - 00:01:49] So why of t there is the product of two functions a cosine and a
[00:01:50 - 00:01:52] rectangular function
[00:01:52 - 00:01:57] So I'm gonna call the cosine h of t and the rectangular function g of t and
[00:01:58 - 00:02:05] Then we can take the Fourier transforms of each of those functions those are two of our
[00:02:07 - 00:02:12] Common functions we've looked at and we've got their Fourier transforms
[00:02:12 - 00:02:15] In the table in the formula sheet that you'll get the test
[00:02:17 - 00:02:19] Okay, so we've now got
[00:02:19 - 00:02:21] h of f
[00:02:21 - 00:02:28] Which is the sum of two delta functions when a positive if not the frequency in the cosine and when it negative if not
[00:02:29 - 00:02:35] So just the resimetry and then the Fourier transform of the rectangular function of period t is
[00:02:37 - 00:02:39] a sync function
[00:02:40 - 00:02:41] multiplied
[00:02:41 - 00:02:43] scaled by capital T
[00:02:44 - 00:02:51] So in the time domain we're multiplying a cosine with a rectangular function that means in the frequency
[00:02:51 - 00:02:58] domain we are convolving our two delta functions with a sync function
[00:03:00 - 00:03:02] Okay, so then if we look
[00:03:04 - 00:03:06] Then
[00:03:07 - 00:03:14] To get our final formula. So we've got back here. We've got we're gonna have our sync function
[00:03:14 - 00:03:16] convolved with these delta functions and
[00:03:17 - 00:03:24] So one thing that we need to know about a delta function is that when we convolve a
[00:03:25 - 00:03:27] function so here
[00:03:28 - 00:03:32] x of f if we convolve that with a delta function
[00:03:33 - 00:03:37] With that delta is in the time domain or the frequency domain
[00:03:39 - 00:03:42] We then get that function back so this is then
[00:03:43 - 00:03:44] x of f
[00:03:44 - 00:03:50] Okay, so when we do this convolution
[00:03:51 - 00:03:57] We then get for the spectrum of our tone burst. This is capital Y of f
[00:03:59 - 00:04:01] Okay, so this is the Fourier transform
[00:04:02 - 00:04:04] Then of y of t at the top there
[00:04:05 - 00:04:29] We get capital T over two so
[00:04:30 - 00:04:37] The capital T comes from the sync here and divided by two is from our deltas
[00:04:37 - 00:04:39] so we have capital T on two
[00:04:40 - 00:04:42] then we have a sync function and
[00:04:45 - 00:04:48] The sync function one is sent to the if
[00:04:49 - 00:04:52] At if it minus f naught if plus f naught here
[00:04:53 - 00:04:55] times t and then we have another
[00:04:55 - 00:04:58] sync function scale by t over two
[00:04:59 - 00:05:05] which is centered at positive if not so we have if minus if naught comes t
[00:05:05 - 00:05:13] Okay, so by multiple I have a look at some
[00:05:14 - 00:05:19] actual signals that might be the clearer so we have here
[00:05:22 - 00:05:31] So h of t was our cosine function on the top so that's going forever
[00:05:32 - 00:05:37] Within multiplying it and the time domain by our rec function g of t
[00:05:37 - 00:05:41] So this cosine was cosine
[00:05:43 - 00:05:51] 2 pi if naught t we're multiplying it by a rec function
[00:05:52 - 00:05:56] Which has a period or a width of capital T so this was rec
[00:05:57 - 00:06:01] t over capital T
[00:06:07 - 00:06:13] Okay, and so then in the time domain so this is just put the less and so here
[00:06:13 - 00:06:17] time and seconds and on the right hand side we've got safe
[00:06:17 - 00:06:19] We've got frequency
[00:06:20 - 00:06:21] in
[00:06:21 - 00:06:24] Hertz
[00:06:24 - 00:06:27] Okay, so when we multiply those two functions together
[00:06:27 - 00:06:29] so this is then
[00:06:29 - 00:06:31] the bottom row left column is
[00:06:32 - 00:06:34] h of t times g of t
[00:06:35 - 00:06:46] okay, and so
[00:06:47 - 00:06:50] We didn't have on the right hand side
[00:06:51 - 00:06:57] We have the Fourier domain so we can take the Fourier transform the top we're taking the Fourier transform of our cosine wave
[00:06:59 - 00:07:02] So this then is delta functions at
[00:07:04 - 00:07:06] Plus and minus if not
[00:07:06 - 00:07:10] minus if not plus if not and these both have a height
[00:07:11 - 00:07:13] But will mark a height of a half?
[00:07:13 - 00:07:16] That means the area of each of those delta functions as a half
[00:07:21 - 00:07:28] Okay, and then so this the top one then we'll call capital H of f the middle one is our sink function as capital G of f
[00:07:30 - 00:07:37] And so this has the function capital T times sink t
[00:07:38 - 00:07:43] So t is the period or width of the sink
[00:07:45 - 00:07:54] So the width of the rec
[00:07:54 - 00:08:00] And so in the bottom we then end up so in the frequency domain we have h of f
[00:08:00 - 00:08:02] convolved with g of f
[00:08:06 - 00:08:11] Okay, so what we see in the frequency domain is that we have then
[00:08:12 - 00:08:14] our
[00:08:14 - 00:08:18] Frequency content is spread from f naught so if we have a pure cosine wave
[00:08:19 - 00:08:22] We just have deltors at f naught and minus f naught
[00:08:23 - 00:08:27] By windowing it multiplying by this rectangle function within spreading out
[00:08:27 - 00:08:30] the frequency away from
[00:08:31 - 00:08:35] that pure cosine tone if naught and minus f naught
[00:08:36 - 00:08:45] So our frequency content is spread from f naught
[00:08:58 - 00:09:04] Okay, so in this example what is our period capital T?
[00:09:05 - 00:09:06] The American League
[00:09:06 - 00:09:15] So our rectangular function here is going from between
[00:09:15 - 00:09:18] So this two is a two here. That's minus two
[00:09:22 - 00:09:27] So that it's going between one and minus one and the rectangle function is defined between minus half and half
[00:09:28 - 00:09:30] So here our period T is
[00:09:31 - 00:09:35] two
[00:09:35 - 00:09:37] What is our
[00:09:38 - 00:09:40] Frequency if naught
[00:09:48 - 00:09:50] So we've got if we can set out what happens in one second
[00:09:54 - 00:09:55] Well
[00:09:55 - 00:09:57] So up to two seconds here we have
[00:09:58 - 00:10:00] One two three four cycles
[00:10:04 - 00:10:18] divided by two seconds divided by two
[00:10:19 - 00:10:21] Equals two
[00:10:21 - 00:10:22] Hertz
[00:10:22 - 00:10:32] Okay, so then we could write in the
[00:10:33 - 00:10:37] Full forms here so in time domain we have then wrecked
[00:10:38 - 00:10:39] of
[00:10:40 - 00:10:42] T divided by two
[00:10:42 - 00:10:44] and then cosine
[00:10:45 - 00:10:47] four pi
[00:10:47 - 00:10:56] T and similarly for the frequency domain
[00:10:57 - 00:10:59] this is then
[00:10:59 - 00:11:01] sink
[00:11:01 - 00:11:03] two
[00:11:03 - 00:11:05] f plus two
[00:11:07 - 00:11:08] plus
[00:11:08 - 00:11:10] sink
[00:11:10 - 00:11:12] two
[00:11:12 - 00:11:16] If minus two
[00:11:16 - 00:11:32] So that's the final one here in the frequency domain. Okay, so we've got some more um
[00:11:33 - 00:11:35] Fourier transform problems for you to work on
[00:11:36 - 00:11:39] at this week's tutorial as well as some more last ones
[00:11:39 - 00:11:42] We will go through some problems like this
[00:11:44 - 00:11:46] And I was actually just looking through use today last year's test
[00:11:47 - 00:11:52] Because I'm right this year because my first year's the course and this was actually a question in the
[00:11:53 - 00:11:56] Test remember right the zero last year of the interval
[00:11:57 - 00:12:01] So we'll do some idea of what we'll be covered in the test
[00:12:03 - 00:12:08] Okay, so I think you're wouldn't have been so close this because I think there's the last slide on up
[00:12:08 - 00:12:10] Here we go Fourier transform summary
[00:12:12 - 00:12:14] Okay, so this
[00:12:15 - 00:12:17] Is the formula sheet
[00:12:18 - 00:12:24] or in the formula sheet to exam
[00:12:26 - 00:12:28] And it's also on
[00:12:28 - 00:12:34] Learn so one thing you could do when you're doing the problems and the tutorials is to
[00:12:35 - 00:12:38] Use the formula sheet at the same time so you'll get acquainted with
[00:12:39 - 00:12:41] What's in there and where it is
[00:12:41 - 00:12:45] For the test so you're not flapping mildly through the pages while they're through the pages
[00:12:46 - 00:12:48] Trying to find the right formula in the test
[00:12:49 - 00:12:50] Okay, so
[00:12:50 - 00:12:53] We've got here in the formula sheet
[00:12:55 - 00:13:02] We've got the five key properties. We looked at linearity shift frequency shifting scaling convolution theorem and then the four
[00:13:02 - 00:13:08] Four four appears that we need as well so between rect and sink
[00:13:09 - 00:13:13] Delta in one etc
[00:13:13 - 00:13:15] Okay, so that's the last
[00:13:16 - 00:13:23] Slide for the for a transform so we can now move on to our analog filters
[00:13:23 - 00:13:25] So we'll just close this and say that
[00:13:27 - 00:13:39] Can open up the next one
[00:13:50 - 00:14:19] So we're now going to look at different circuits and how we use can use them to filter
[00:14:21 - 00:14:25] Signals say voltage in our circuit. We've got lots of noise high frequency noise. Oh, no, it's a low frequency noise
[00:14:26 - 00:14:34] We can use certain combinations of resistors capacitors and inductors to remove certain frequencies from our
[00:14:35 - 00:14:39] Signals in our circuit
[00:14:39 - 00:14:41] Okay, so we got here
[00:14:41 - 00:14:43] our resistor and a capacitor
[00:14:44 - 00:14:46] and so this is
[00:14:46 - 00:14:53] the input voltage and
[00:14:53 - 00:14:55] Here we've got the output voltage
[00:14:58 - 00:15:00] Does you know I know what that circuit's going to do?
[00:15:03 - 00:15:05] Yep low pass
[00:15:05 - 00:15:09] Yeah, but yeah, and let's do the high frequency. It's nothing two people said
[00:15:11 - 00:15:14] the same thing but different ways the same time. Okay, so and
[00:15:15 - 00:15:18] You either know what you're doing or you can read a
[00:15:18 - 00:15:21] Mode plot on the right hand side. So here we've got
[00:15:22 - 00:15:29] This is a low pass filter
[00:15:29 - 00:15:31] Okay, so the low frequencies the small frequencies
[00:15:32 - 00:15:42] Pass and the high frequencies here are attenuated
[00:15:46 - 00:15:50] Okay, so this is good type of filter safe. You've got high frequency noise
[00:15:51 - 00:15:53] I said at thermal noise we have for our resistors
[00:15:54 - 00:15:56] produces
[00:15:57 - 00:16:04] Well white spectrum of noise, but if you want to get rid of the high frequencies while keeping your low frequency signal content
[00:16:04 - 00:16:06] You could use a low pass filter
[00:16:07 - 00:16:09] So we're going to go through
[00:16:09 - 00:16:11] the maths
[00:16:12 - 00:16:14] Of how we generate these
[00:16:14 - 00:16:19] O plots for different types of filters. The low pass high pass band pass band stop
[00:16:21 - 00:16:25] And we're going to use our as our example here this low pass
[00:16:27 - 00:16:28] filter
[00:16:28 - 00:16:32] When we're talking about different calculations we can do over the next couple of lectures
[00:16:40 - 00:16:42] so
[00:16:42 - 00:16:43] our signal
[00:16:43 - 00:16:45] might be corrupted by noise or
[00:16:46 - 00:16:48] interference
[00:16:48 - 00:16:50] And so then there are different
[00:16:50 - 00:16:52] examples so
[00:16:52 - 00:16:54] If we're measuring the heart rate with an ECG
[00:16:55 - 00:16:57] This might be contaminated by
[00:16:58 - 00:17:02] The main frequency as we've talked about in that case you would want a
[00:17:03 - 00:17:05] band stop
[00:17:06 - 00:17:08] filter
[00:17:08 - 00:17:12] So that means you just want to stop a very narrow range of frequencies so around 50 Hertz
[00:17:13 - 00:17:15] Possibly harmonics as well
[00:17:16 - 00:17:19] But you don't want to be frequency filtering out other frequencies
[00:17:22 - 00:17:24] So the second one is an example from
[00:17:25 - 00:17:26] my
[00:17:27 - 00:17:29] Engineering research is where
[00:17:30 - 00:17:35] On a telescope when we're looking at a star we try to measure what the atmosphere is doing
[00:17:36 - 00:17:38] these
[00:17:38 - 00:17:44] Large modern telescopes a big buildings they get shaken by the wind so that introduces vibrations
[00:17:45 - 00:17:49] And we want to then remove these vibrations from our sensor data
[00:17:51 - 00:17:53] And then thirdly
[00:17:53 - 00:17:56] Anemicrocontroller is also switching going on
[00:17:57 - 00:18:04] So zeros are changing to ones and this produces our high frequency noise and that can then affect our analog
[00:18:04 - 00:18:08] Sensor measurements
[00:18:08 - 00:18:10] Okay, so we're going to look at analog filters
[00:18:11 - 00:18:13] That can be built from
[00:18:13 - 00:18:14] Circuit components
[00:18:14 - 00:18:18] So we're just going to look at filters made from inductors resistors and capacitors
[00:18:18 - 00:18:21] You can also make more complicated filters with hot pamps as well
[00:18:22 - 00:18:25] But that's going to be outside the scope of our course
[00:18:28 - 00:18:31] And so these can be made to attenuate different frequencies
[00:18:34 - 00:18:38] Okay, and then next week maybe the end of this week we'll look at digital filtering
[00:18:39 - 00:18:45] Where we can do the same processes but on our microcontroller so we can create a high
[00:18:46 - 00:18:51] pass filter or a low pass filter on a microcontroller instead of
[00:18:53 - 00:18:55] In our circuit within analog filter
[00:18:59 - 00:19:01] Okay, and so
[00:19:01 - 00:19:07] The tool we're going to use for looking at our analog filters is the Laplace transform
[00:19:08 - 00:19:12] And that's why we did a bit of a recap last week on the analog filter
[00:19:13 - 00:19:18] So on the Laplace transform and how we use that with our different circuit components
[00:19:22 - 00:19:24] Okay, so we'll start with a little example
[00:19:27 - 00:19:30] Okay, so here in blue we've got our true signal
[00:19:31 - 00:19:35] So this is the sign function of by erect function
[00:19:37 - 00:19:41] We've got some interference at a higher frequency in orange
[00:19:43 - 00:19:48] And then what we measure is the signal plus the interference
[00:19:49 - 00:19:57] So in this case here in green so we can barely see the signal here
[00:19:58 - 00:20:02] You can see a little bit around here that the peaks are changing slightly
[00:20:03 - 00:20:05] But
[00:20:05 - 00:20:08] The signal is mostly swapped by the interference
[00:20:10 - 00:20:13] Okay, so if we have a low pass filter
[00:20:13 - 00:20:21] Because our true signal has a lower frequency then our interference signal we can then
[00:20:23 - 00:20:25] Filter out most of the interference
[00:20:26 - 00:20:30] As that's shown in the bottom and red but we do have some
[00:20:30 - 00:20:33] residual
[00:20:33 - 00:20:36] interference
[00:20:36 - 00:20:45] Okay, so that's why the red curve here is looking quite steady
[00:20:46 - 00:20:48] So that is
[00:20:48 - 00:20:49] the
[00:20:49 - 00:20:51] Inference
[00:20:51 - 00:20:53] Filter down so it's much lower magnitude
[00:20:54 - 00:20:56] But because we've used
[00:20:56 - 00:21:00] The low pass filter rather than a notch or band stop filter
[00:21:00 - 00:21:03] We haven't completely removed the interference
[00:21:05 - 00:21:09] Okay, so just to find these signals against our interference at the top here
[00:21:10 - 00:21:13] So the form a sign
[00:21:17 - 00:21:19] 2 pi f t
[00:21:21 - 00:21:23] So the amplitude here is 10
[00:21:24 - 00:21:28] Um so a equals 10
[00:21:29 - 00:21:33] And the frequency call f1 is at
[00:21:34 - 00:21:36] 3 hertz
[00:21:37 - 00:21:39] So this means we could write our interference as 10 sign
[00:21:40 - 00:21:43] Xt
[00:21:43 - 00:21:49] Okay, so the residual interference we'd see here is at 3 hertz
[00:21:54 - 00:21:56] Okay, whereas our true signal
[00:21:58 - 00:21:59] Is
[00:21:59 - 00:22:01] a sine signal
[00:22:01 - 00:22:06] And it's multiplied by a retainer function. So here we've got a signal of the form
[00:22:06 - 00:22:07] a
[00:22:07 - 00:22:10] sine
[00:22:10 - 00:22:13] 2 pi
[00:22:13 - 00:22:17] If not
[00:22:17 - 00:22:19] t minus t naught
[00:22:21 - 00:22:21] Ricked
[00:22:23 - 00:22:25] t minus t naught over capital T
[00:22:28 - 00:22:33] Okay, so in this case for our true signal the amplitude is 1
[00:22:37 - 00:22:39] What is
[00:22:41 - 00:22:47] t naught? What's the amount of shifts there?
[00:22:49 - 00:22:51] 10 i think i had 10 that is 10
[00:22:53 - 00:22:55] And
[00:22:55 - 00:22:58] What's the period of our rectangular function here going to be
[00:23:02 - 00:23:05] 4 yep, that's 4 fingers. I'll take what I can get
[00:23:06 - 00:23:10] And then what else we're missing here? We haven't defined
[00:23:11 - 00:23:15] If not so if not here is no one want to take guess at that
[00:23:17 - 00:23:19] We've got
[00:23:21 - 00:23:26] Yes, it is good. Okay, so we've got
[00:23:27 - 00:23:30] 2 cycles and 4 seconds the 2 divided by 4 is a half
[00:23:32 - 00:23:34] So we could write this then as
[00:23:35 - 00:23:37] sine
[00:23:37 - 00:23:39] pi
[00:23:40 - 00:23:41] t minus 10
[00:23:41 - 00:23:44] or bracket
[00:23:45 - 00:23:49] Ricked
[00:23:49 - 00:23:50] t minus 10
[00:23:50 - 00:23:51] over 4
[00:23:53 - 00:23:54] Okay, and that's
[00:23:55 - 00:23:59] Like the tone burst we had in the for example in the cell lecture
[00:23:59 - 00:24:03] And so in the Fourier domain there would then be a convolution of
[00:24:04 - 00:24:06] sine which has two deltas with
[00:24:07 - 00:24:09] For a transform of
[00:24:09 - 00:24:12] the rect which is a sine function
[00:24:15 - 00:24:16] Okay, so that's what we're trying to do
[00:24:16 - 00:24:19] We're trying to get rid of the interference and all noise and
[00:24:19 - 00:24:21] get keep our true
[00:24:22 - 00:24:22] signal
[00:24:22 - 00:24:39] Okay, so we'll define the transfer function
[00:24:39 - 00:24:41] which is the
[00:24:41 - 00:24:45] ratio of the outputs to inputs in this case in our circuit
[00:24:46 - 00:24:48] And
[00:24:48 - 00:24:50] The transfer function is defined in the past domain
[00:24:50 - 00:24:54] So this is in complex frequency or s space
[00:24:56 - 00:24:59] Okay, so the one we're going to be thinking about is the voltage transfer function
[00:25:00 - 00:25:03] So then our transfer function capital H
[00:25:04 - 00:25:07] Which is function of s is the output voltage
[00:25:09 - 00:25:13] The rls over the input function input voltage be i of s
[00:25:14 - 00:25:16] So this is output
[00:25:17 - 00:25:22] Okay, and what are the units for our transfer function
[00:25:26 - 00:25:29] Well, yeah, well, you unless yeah, so it's also the volt. So
[00:25:31 - 00:25:32] It has no units
[00:25:32 - 00:25:46] Okay, so let's look at the transfer function for our
[00:25:47 - 00:25:50] RC circuit
[00:25:50 - 00:25:52] So this is our input
[00:25:53 - 00:25:56] Voltage this is our output voltage
[00:25:58 - 00:26:00] So we've said that
[00:26:01 - 00:26:06] Our transfer function h of s is equal to our output voltage be out of s
[00:26:07 - 00:26:09] Over our input voltage be i of s
[00:26:12 - 00:26:15] Okay, so how would you go about
[00:26:16 - 00:26:19] Trying to then solve for the transfer function?
[00:26:21 - 00:26:24] Watch circuit
[00:26:24 - 00:26:29] Cookups
[00:26:29 - 00:26:32] You possibly go that way. That's not the way I'm going to go
[00:26:33 - 00:26:35] Something else you could do
[00:26:36 - 00:26:39] The class we're going to well we're already in the little plus domain so
[00:26:41 - 00:26:43] In the last domain that has impedance r
[00:26:43 - 00:26:46] What's the impedance for a capacitor in the last domain?
[00:26:46 - 00:26:55] So that's what it is
[00:26:56 - 00:26:57] One over sc
[00:27:01 - 00:27:03] Okay, so the one I'm going to do
[00:27:05 - 00:27:06] Is we could use a voltage divider?
[00:27:12 - 00:27:16] So that means the out of s
[00:27:17 - 00:27:19] Is equal to
[00:27:20 - 00:27:22] the impedance
[00:27:23 - 00:27:25] Here which is
[00:27:26 - 00:27:28] One over sc
[00:27:29 - 00:27:30] Over the total impedance
[00:27:31 - 00:27:34] Which is r plus one over sc
[00:27:35 - 00:27:38] Times our input voltage v i of s
[00:27:38 - 00:27:45] Okay, so you might be more familiar with thinking if you've just got two resistors
[00:27:48 - 00:27:51] But you can generalize that in terms of impedances
[00:27:55 - 00:27:57] So there's going to be some voltage drop
[00:27:57 - 00:28:01] Across the resistor some voltage drop across the capacitor
[00:28:01 - 00:28:05] And the voltage drop is proportional to the impedance
[00:28:06 - 00:28:08] Across the output
[00:28:09 - 00:28:10] Well, so it's the total impedance
[00:28:13 - 00:28:15] Okay, so if we divide
[00:28:20 - 00:28:29] Divide v i of s that goes on left hand side we have our h of s which is equal to v out of s over the n of s
[00:28:31 - 00:28:37] This is equal to then one over sc over r plus one over sc
[00:28:37 - 00:28:41] Which is a bit messy so if we then
[00:28:42 - 00:28:44] the sc
[00:28:44 - 00:28:48] Goes down to the bottom so we then have one over
[00:28:53 - 00:29:00] One plus sc
[00:29:00 - 00:29:02] Okay, so there's a transfer function for our
[00:29:03 - 00:29:04] Rc
[00:29:07 - 00:29:08] filter
[00:29:08 - 00:29:17] Okay, so we'll do a bit more analysis on this to get our
[00:29:17 - 00:29:19] then our
[00:29:19 - 00:29:21] frequency response
[00:29:21 - 00:29:31] magnitude of phase from this transfer function. Okay, so
[00:29:32 - 00:29:34] You'll see this before but we'll just recap it so
[00:29:35 - 00:29:37] We can write our
[00:29:37 - 00:29:39] transfer function couple of ways so
[00:29:41 - 00:29:43] We can write h of s as
[00:29:47 - 00:29:52] A sum for both the numerator and denominator. So if we've got some
[00:29:53 - 00:29:55] s to power n with coefficient b in
[00:29:56 - 00:29:58] plus dot dot
[00:29:59 - 00:30:02] b1 times s plus some constant b0
[00:30:03 - 00:30:06] And the numerator and we can do the same with the denominator
[00:30:07 - 00:30:11] So a m is coefficient s to the power n plus dot dot dot
[00:30:12 - 00:30:13] a
[00:30:13 - 00:30:15] 1 s plus a 0
[00:30:20 - 00:30:23] Okay, so it's a sum in the numerator and denominator
[00:30:24 - 00:30:26] And then can be more useful
[00:30:27 - 00:30:29] Analyzing these if we write it is a product
[00:30:30 - 00:30:33] In both for both the numerator and denominator
[00:30:34 - 00:30:38] So this is known as the pz k form for poles zeros and gain
[00:30:39 - 00:30:46] So we've got then
[00:30:46 - 00:30:59] zeros in the numerator and we've got as many zeros as we do the power of
[00:31:01 - 00:31:03] s in the numerator and we've got
[00:31:04 - 00:31:13] Now poles in the denominator and we've got as many poles as the
[00:31:14 - 00:31:20] order of the
[00:31:21 - 00:31:23] highest power of s in the denominator
[00:31:24 - 00:31:32] So the zeros are where it's zero on the top and the poles where we go to zero on the bottom say to this becomes infinite
[00:31:33 - 00:31:35] And k is
[00:31:40 - 00:31:42] Okay, so hopefully nothing new there
[00:31:46 - 00:31:48] So we can also for our
[00:31:48 - 00:31:52] Rc filter we can draw a pole zero diagram
[00:31:55 - 00:31:58] So this is real on the excess and imaginary
[00:31:59 - 00:32:01] on the y-axis
[00:32:03 - 00:32:12] So we had our transfer function h of s for this circuit was 1 over 1 plus s c r
[00:32:12 - 00:32:19] And we can also rewrite this because it's easy to find the
[00:32:20 - 00:32:24] For put in pk z form to find the poles so we then have our
[00:32:26 - 00:32:28] numerator is 1 over rc
[00:32:29 - 00:32:31] And then it's s plus
[00:32:32 - 00:32:34] 1 over rc
[00:32:39 - 00:32:43] Okay, so our gain k is 1 over rc
[00:32:45 - 00:32:47] How many zeros do we have for this transfer function?
[00:32:49 - 00:32:57] None but those zeros and how many poles one pole?
[00:32:58 - 00:33:00] And that's at
[00:33:00 - 00:33:02] minus 1 over rc
[00:33:02 - 00:33:05] So we can do our pole on here minus 1 over
[00:33:06 - 00:33:08] c
[00:33:08 - 00:33:14] Okay, so the poles and the zeros are going to determine the behavior of our circuit
[00:33:16 - 00:33:18] Okay, so this is why they
[00:33:19 - 00:33:21] Important
[00:33:21 - 00:33:25] Okay, because there's got one pole. This is what's known as a first order system
[00:33:27 - 00:33:29] or first order filter
[00:33:30 - 00:33:32] And if we increase the number of poles
[00:33:34 - 00:33:38] That's going to change the order of our filter and we'll show what that means later on
[00:33:38 - 00:33:52] Okay, so we've got our transfer function. Can relate to this
[00:33:53 - 00:33:55] We can get the impulse response
[00:33:56 - 00:33:59] From our transfer function is
[00:34:01 - 00:34:05] The inverse Laplace so our impulse response
[00:34:06 - 00:34:09] h of t is equal to
[00:34:10 - 00:34:15] The inverse Laplace transform of our transfer function h of s
[00:34:20 - 00:34:22] So the impulse response is telling us if we put
[00:34:23 - 00:34:29] an impulse so a one or a delta into our function into our circuit
[00:34:30 - 00:34:37] What is the response?
[00:34:37 - 00:34:41] Okay, so for our RC circuit to calculate the impulse response
[00:34:42 - 00:34:46] h of t is then the inverse Laplace transform
[00:34:48 - 00:34:57] Of our transfer function h of s which was defined as in pz k form 1 over rc
[00:34:58 - 00:35:00] s plus 1 over rc
[00:35:05 - 00:35:07] Okay, and so we
[00:35:14 - 00:35:16] Do this integral
[00:35:17 - 00:35:19] In this the plus integral we use our common tables
[00:35:21 - 00:35:23] So now let's transform table
[00:35:25 - 00:35:30] It's a pair number four in that in the formula sheet is then for a single pole
[00:35:31 - 00:35:35] And this gives us h of t is equal to then
[00:35:35 - 00:35:37] 1 over
[00:35:38 - 00:35:39] rc
[00:35:40 - 00:35:43] e to the minus t over rc
[00:35:44 - 00:35:46] And because it's the plus transform
[00:35:47 - 00:35:49] It's only defined for
[00:35:49 - 00:35:51] Those of t greater than or equal to 0
[00:35:55 - 00:35:57] Okay, so that's the
[00:35:57 - 00:36:02] multiplying by the unit
[00:36:03 - 00:36:05] Step function of t
[00:36:17 - 00:36:20] Okay, so the output of our filter
[00:36:20 - 00:36:23] So we're putting in some noisy signal
[00:36:23 - 00:36:28] Through this rc circuit to try and remove the high frequencies
[00:36:29 - 00:36:31] the output of the filter
[00:36:33 - 00:36:36] Y of t is then given by
[00:36:37 - 00:36:39] our friend
[00:36:39 - 00:36:41] convolution x of t
[00:36:41 - 00:36:45] So the input so the output of our filter is equal to the input
[00:36:46 - 00:36:49] x of t convolved with our impulse response
[00:36:51 - 00:36:53] Okay, so that's why the impulse response
[00:36:54 - 00:36:55] Is of the filter is important
[00:36:59 - 00:37:03] Or we can write this in the frequency domain
[00:37:08 - 00:37:12] So capital Y of s is the spectrum of the output
[00:37:16 - 00:37:18] is equal to then
[00:37:18 - 00:37:23] convolution time domain becomes a multiplication in the frequency domain
[00:37:23 - 00:37:24] So this is then
[00:37:25 - 00:37:26] The spectrum of our input
[00:37:29 - 00:37:31] And that becomes the entire
[00:37:31 - 00:37:43] capital H of f which is our frequency response of our circuit
[00:37:44 - 00:37:46] of our filter
[00:37:47 - 00:37:52] And so the frequency response capital H of f and the transfer function H of s
[00:37:53 - 00:37:54] Very similar
[00:37:55 - 00:37:58] The transfer function H of s is defined for complex frequency
[00:37:59 - 00:38:03] Whereas the frequency response capital H of f is just for our regular
[00:38:04 - 00:38:05] frequency
[00:38:05 - 00:38:16] And that's
[00:38:16 - 00:38:20] Okay, so let's look at the impulse response for our rc circuit
[00:38:23 - 00:38:27] And so here are plotted for some particular values
[00:38:27 - 00:38:28] So let's say
[00:38:28 - 00:38:32] The convenience sake
[00:38:32 - 00:38:38] We're going to use a resistor of 100 kilo ohms
[00:38:39 - 00:38:43] A capacitor of 10 microfarads
[00:38:45 - 00:38:49] It means our time constant tau
[00:38:49 - 00:38:51] Because it equal to r times c
[00:38:52 - 00:38:55] Is going to be equal to what we can do that maths in the head
[00:38:55 - 00:39:05] So every nice round number
[00:39:05 - 00:39:12] That's going to be one
[00:39:13 - 00:39:13] See here
[00:39:14 - 00:39:17] Okay, you have a calculator and the test of course
[00:39:18 - 00:39:22] Okay, so for simplicity sake that is our
[00:39:24 - 00:39:24] time constant
[00:39:25 - 00:39:27] And so this value here
[00:39:28 - 00:39:31] For our impulse response is equal to then 1 over tau
[00:39:35 - 00:39:39] And at t equals tau
[00:39:41 - 00:39:42] We have a value
[00:39:43 - 00:39:44] To this value here
[00:39:47 - 00:39:51] Now impulse response H of t is equal to
[00:39:52 - 00:39:54] e to the minus 1
[00:39:55 - 00:39:57] So that's 0.37
[00:39:58 - 00:40:00] Of the maximum value
[00:40:13 - 00:40:16] Okay, so if we have
[00:40:17 - 00:40:18] Let's go for a different color for this
[00:40:19 - 00:40:20] Um
[00:40:20 - 00:40:23] If we have a larger value of rc
[00:40:25 - 00:40:28] Let's say we can do here rc is 2 an orange
[00:40:30 - 00:40:33] This is then going to go up
[00:40:33 - 00:40:35] Control to scale
[00:40:35 - 00:40:37] There's going to go up to about what's going to go to 2 here
[00:40:39 - 00:40:45] And then it's going to decay more quickly than rc is 1
[00:40:48 - 00:40:51] Okay, so it's got rc is 2
[00:40:51 - 00:40:59] We've got a larger peak and it decays faster
[00:41:21 - 00:41:23] Okay, then I've got another question field of ponder
[00:41:23 - 00:41:25] What happens also?
[00:41:25 - 00:41:26] What is the
[00:41:27 - 00:41:29] Units for the impulse response here?
[00:41:29 - 00:41:31] So we might need to go back to our
[00:41:33 - 00:41:38] Equation
[00:41:38 - 00:41:41] So h of t, the inverse of the
[00:41:43 - 00:41:44] Transfer function h of s
[00:41:48 - 00:41:49] So then
[00:41:50 - 00:41:52] What are the units here for h of t going to be?
[00:41:57 - 00:41:59] Then you go this is
[00:41:59 - 00:42:01] What are the units of rc
[00:42:03 - 00:42:06] Second so that means the impulse response is going to be
[00:42:07 - 00:42:09] And then one over seconds
[00:42:09 - 00:42:24] Okay, so right seconds to confuse with this from a little bus transform
[00:42:25 - 00:42:28] And some people write that if we're talking about the
[00:42:30 - 00:42:33] Impulse response being a voltage then it would be volts for second
[00:42:34 - 00:42:39] But technically mathematically it should be one over seconds
[00:42:42 - 00:42:44] You can also see that from the
[00:42:47 - 00:42:49] Laplace
[00:42:49 - 00:42:51] The plus oh, we don't have the equation here
[00:42:51 - 00:42:53] But if you look at the integral the plus
[00:42:55 - 00:42:57] In this Laplace integral it's got
[00:43:00 - 00:43:04] An integral ds
[00:43:04 - 00:43:06] And this is a function of f
[00:43:06 - 00:43:09] So that's one over seconds
[00:43:10 - 00:43:14] Okay, so the two ways to come up was here being one over seconds
[00:43:17 - 00:43:19] Okay, so this impulse response
[00:43:19 - 00:43:22] Another thing we might want to look at for our circuit is
[00:43:23 - 00:43:24] the step response
[00:43:25 - 00:43:30] So if we put a step so the unit step function u of t of voltage
[00:43:31 - 00:43:34] I'll one volt into our circuit
[00:43:34 - 00:43:38] Then what is the response of our filter?
[00:43:41 - 00:43:45] Okay, so then our step response will call
[00:43:46 - 00:43:51] g of t this is equal to the
[00:43:53 - 00:43:55] inverse Laplace transform
[00:43:56 - 00:43:58] Of our transfer function h of s
[00:43:59 - 00:44:05] Divided by s
[00:44:05 - 00:44:07] Okay, and then this is the response to a step function
[00:44:18 - 00:44:20] And for our particular
[00:44:21 - 00:44:26] case, we're looking at our our C filter our
[00:44:28 - 00:44:32] impulse sorry our step response g of t is the integral to
[00:44:33 - 00:44:35] the inverse Laplace transform of
[00:44:37 - 00:44:37] one over
[00:44:39 - 00:44:43] s
[00:44:43 - 00:44:45] One plus is
[00:44:46 - 00:44:52] Okay, so h of s was one over one plus s i c and we're got this s on the bottom now as well
[00:44:53 - 00:44:55] from the definition of
[00:44:56 - 00:44:58] The transfer function
[00:44:58 - 00:45:07] Okay, so this one over s comes from the definition of a
[00:45:09 - 00:45:11] integral
[00:45:12 - 00:45:15] So the step response is the integral of the impulse response or the
[00:45:15 - 00:45:17] responses the derivative of the
[00:45:19 - 00:45:26] step response and an integral in the time domain is the same as
[00:45:26 - 00:45:29] multiplying by one over s in the Laplace domain
[00:45:30 - 00:45:32] So that's why
[00:45:32 - 00:45:37] We divide the transfer function by s and then take the inverse Laplace transform to get our step response
[00:45:46 - 00:45:48] Okay, so for our
[00:45:48 - 00:45:50] RC filter
[00:45:50 - 00:45:53] then finding the inverse Laplace
[00:45:54 - 00:45:56] Of that
[00:45:56 - 00:45:58] expression is a little bit
[00:45:58 - 00:45:59] Missy
[00:45:59 - 00:46:01] Anyone got any ideas how we do that?
[00:46:02 - 00:46:04] Did you do this in math or
[00:46:05 - 00:46:14] Partial fractions yes, that's what I was looking for. I'm not sure if you said that as well. Okay, so
[00:46:15 - 00:46:17] We're going to use
[00:46:17 - 00:46:20] partial fractions
[00:46:20 - 00:46:30] So that means we're going to put things over two separate denominators and then we can solve
[00:46:32 - 00:46:34] For each of those
[00:46:34 - 00:46:35] fractions
[00:46:35 - 00:46:38] So then
[00:46:38 - 00:46:40] g of t is equal to
[00:46:40 - 00:46:42] the inverse Laplace
[00:46:42 - 00:46:43] of
[00:46:43 - 00:46:45] one over s
[00:46:45 - 00:46:46] minus
[00:46:46 - 00:46:48] one over
[00:46:48 - 00:46:50] one plus s
[00:46:50 - 00:46:57] C
[00:46:57 - 00:46:59] And so then we get
[00:46:59 - 00:47:01] g of t is equal to
[00:47:02 - 00:47:04] One over s goes to
[00:47:04 - 00:47:05] one
[00:47:05 - 00:47:09] So now the pass transform tables. This is p of one
[00:47:09 - 00:47:11] for constant value
[00:47:11 - 00:47:13] minus
[00:47:13 - 00:47:14] e to minus t over
[00:47:14 - 00:47:15] RC
[00:47:15 - 00:47:19] This is here three for a single pole
[00:47:20 - 00:47:23] And because this is the pass transform it's just defined
[00:47:24 - 00:47:26] for t
[00:47:26 - 00:47:28] Greater than or equal to zero. So we have to
[00:47:29 - 00:47:36] Multiply by the instant function of t. We'll say this is answer is just valid for t greater than or equal to zero
[00:47:36 - 00:47:51] Okay, two minutes to go. So just show the graph for the step response
[00:47:53 - 00:47:55] For our RC filter
[00:47:55 - 00:47:57] Then we'll call it a day
[00:47:57 - 00:47:59] So here we've got then
[00:48:02 - 00:48:04] Our step response
[00:48:04 - 00:48:10] So this is the response to a one volt
[00:48:12 - 00:48:13] Step function
[00:48:13 - 00:48:26] Okay, so in this case here
[00:48:28 - 00:48:29] We've got
[00:48:30 - 00:48:34] At tau
[00:48:34 - 00:48:36] Which is equal to one. So we've got again
[00:48:37 - 00:48:40] Our RC which is to be one
[00:48:42 - 00:48:44] To tau equals one second
[00:48:45 - 00:48:49] In this case we have the amplitude here is
[00:48:51 - 00:48:53] To g of t is equal to
[00:48:53 - 00:48:56] One minus e to the minus one which is 63
[00:48:58 - 00:48:58] C
[00:49:08 - 00:49:10] Okay, so the step response here is in
[00:49:10 - 00:49:12] Vaults
[00:49:12 - 00:49:18] This is for a voltage
[00:49:18 - 00:49:21] Step response is taking the units of
[00:49:22 - 00:49:24] The step we're putting in
[00:49:25 - 00:49:26] Okay, so there we've got
[00:49:26 - 00:49:28] The blue curve is for RC is equal to one
[00:49:31 - 00:49:36] If we make our
[00:49:38 - 00:49:39] Time constant smaller
[00:49:40 - 00:49:42] So if RC is equal to
[00:49:44 - 00:49:45] 0.5
[00:49:47 - 00:49:49] Within gonna go through that point
[00:49:51 - 00:49:54] At 0.5 and then we're going to converge to
[00:49:55 - 00:49:57] The step value of
[00:49:57 - 00:49:58] One faster
[00:50:04 - 00:50:06] Okay, so we'll call a via
[00:50:07 - 00:50:09] I'll put the slide up at the start tomorrow
[00:50:09 - 00:50:11] So you can carry on writing if you want
[00:50:12 - 00:50:13] Reminder that this is tutorial tomorrow for now
[00:50:13 - 00:50:16] For the questions I learned so you can have a look at those
[00:50:17 - 00:50:19] Or just turn up tomorrow and do them and
[00:50:19 - 00:50:21] Having myself will be here to answer questions
[00:50:23 - 00:50:46] Okay, I'll see you tomorrow
[00:50:55 - 00:50:57] This is
[00:51:17 - 00:51:19] With RC
[00:51:55 - 00:51:57] Yes, the panel is one over that.
[00:52:21 - 00:52:22] Cheers.
[00:52:25 - 00:52:27] I
[00:52:27 - 00:52:29] want to
[00:52:29 - 00:52:30] go
[00:52:30 - 00:52:32] to
[00:52:32 - 00:52:35] the
[00:52:35 - 00:52:38] the
[00:52:38 - 00:52:40] the
[00:52:40 - 00:52:42] the
[00:52:42 - 00:52:44] the
[00:52:44 - 00:52:46] the
[00:52:46 - 00:52:48] the
[00:52:48 - 00:52:50] the
[00:52:50 - 00:52:52] the
[00:52:52 - 00:52:53] the
[00:52:53 - 00:52:54] the
[00:52:54 - 00:52:56] I
[00:52:57 - 00:52:59] I
[00:52:59 - 00:53:01] I
[00:53:01 - 00:53:03] the
[00:53:03 - 00:53:05] the
[00:53:05 - 00:53:08] the
[00:53:08 - 00:53:09] I
[00:53:09 - 00:53:11] don't
[00:53:11 - 00:53:13] I
[00:53:13 - 00:53:15] the
[00:53:15 - 00:53:16] the
[00:53:16 - 00:53:19] the
[00:53:19 - 00:53:23] the
[00:53:23 - 00:53:27] I didn't realize my badness was a hardness.
[00:53:27 - 00:53:31] No, it's a love of schools. It's like a huge horse.
[00:53:31 - 00:53:35] You know what? I think it's hard.
[00:53:35 - 00:53:39] You know why? It's because all the rich people retire in college.
[00:53:39 - 00:53:41] Yeah. Yeah.
[00:53:41 - 00:53:44] And also give them a lot of their like, they're like, they're like,
[00:53:44 - 00:53:46] yeah, yeah, yeah, yeah, yeah.
[00:53:46 - 00:53:50] They're all the rich people, but the people that actually really love most of the students.
[00:53:50 - 00:53:52] Yeah.
[00:53:52 - 00:53:53] Yeah.
[00:53:53 - 00:53:54] Yeah.
[00:53:54 - 00:53:56] It is something that's literally not going to drop.
[00:53:56 - 00:53:59] It's just like, if you're wanting to place it, you're going in.
[00:53:59 - 00:54:00] Absolutely.
[00:54:00 - 00:54:02] And you want to know what you're going to do.
[00:54:02 - 00:54:04] I don't know if you're going to do that.
[00:54:04 - 00:54:06] Who are you friends with?
[00:54:06 - 00:54:07] I don't know.
[00:54:07 - 00:54:08] I don't know.
[00:54:08 - 00:54:09] Oh.
[00:54:09 - 00:54:10] Oh, okay.
[00:54:10 - 00:54:11] Yeah.
[00:54:11 - 00:54:12] Thank you.
[00:54:12 - 00:54:13] Thank you.
[00:54:13 - 00:54:14] Thank you.
[00:54:14 - 00:54:15] Yeah.
[00:54:15 - 00:54:16] Thank you.
[00:54:16 - 00:54:17] Yes.
[00:54:17 - 00:54:18] Thank you.
[00:54:18 - 00:54:20] Oh, okay.
[00:54:20 - 00:54:21] Did you have that?
[00:54:21 - 00:54:22] Yeah.
[00:54:22 - 00:54:24] Did you have a look so good?
[00:54:24 - 00:54:28] I just don't want to run a song for me.
[00:54:28 - 00:54:31] So, finally, he's so true because he would be there about me.
[00:54:31 - 00:54:33] You said I've been in the day until you're on the night.
[00:54:33 - 00:54:34] I'm not going to do that.
[00:54:34 - 00:54:35] I'm not going to do that.
[00:54:35 - 00:54:36] I'm not going to do that.
[00:54:36 - 00:54:38] I'm not going to do that.
[00:54:38 - 00:54:41] I'm on the day, but I'm not going to do that.
[00:54:41 - 00:54:42] I'm on the day.
[00:54:42 - 00:54:43] I'm on the day.
[00:54:43 - 00:54:44] I'm on the day.
[00:54:44 - 00:54:45] I'm on the day.
[00:54:45 - 00:54:46] I'm on the day.
[00:54:46 - 00:54:47] I was going to go.
[00:54:47 - 00:54:48] I'm going to go on the day.
[00:54:48 - 00:54:49] I'm going to go on the day.
[00:54:49 - 00:54:50] Okay.
[00:54:50 - 00:54:51] Well, I'm going to go on the day.
[00:54:51 - 00:54:52] I'm going to go on the day.
[00:54:52 - 00:54:53] Yeah.
[00:54:53 - 00:54:54] Okay.
[00:54:54 - 00:54:55] So, I'll lose time.
[00:54:55 - 00:54:56] So, you change.
[00:54:56 - 00:54:57] You're going to go on the day.
[00:54:57 - 00:54:58] I can do a lot of things.
[00:54:58 - 00:54:59] I'll lose the time.
[00:54:59 - 00:55:00] Oh, yeah.

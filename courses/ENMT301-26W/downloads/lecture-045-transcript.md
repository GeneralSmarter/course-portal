# ENMT301-26W Lecture 45 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `6518f9502b364ac11e31ceecce3efe1facd406d12a94e17b2ad46c87b3c2eacd`
Generated: 2026-06-06T06:42:54.008025+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:04 - 00:00:12] Okay, here at Kyoto, hello everyone.
[00:00:12 - 00:00:19] So today we are looking at Fourier transforms, this powerful tool to look at the frequency
[00:00:19 - 00:00:26] domains, the frequency contents of our signals, and we'll be going through some of the
[00:00:26 - 00:00:31] key properties of the Fourier transform today and some key Fourier transform peers, as
[00:00:31 - 00:00:37] well as doing some examples of taking Fourier transforms of common signals.
[00:00:37 - 00:00:44] So we've finished this today on this slide, where we have the definition for the Fourier
[00:00:44 - 00:00:46] transform of a continuous signal.
[00:00:46 - 00:00:51] We'll look at the discrete Fourier transform, so how we do a Fourier transform of a digital
[00:00:51 - 00:00:54] signal later in the course.
[00:00:54 - 00:01:04] But for now, if we have some continuous signal x of t, then if we multiply this complex
[00:01:04 - 00:01:10] exponential e to the minus j2 pi ft, and then integrate, we'll expect the time we get the
[00:01:10 - 00:01:14] spectrum capital x of f.
[00:01:14 - 00:01:22] So little letter we're using for time domain, big letter for the frequency domain or spectrum.
[00:01:22 - 00:01:28] Okay, so our signal and the time domain might be a real signal, so it doesn't have any
[00:01:28 - 00:01:34] imaginary components, but the spectrum capital x of f will have a magnitude and a phase,
[00:01:34 - 00:01:38] so it's a complex valued function.
[00:01:38 - 00:01:44] As the last little bit about the notation, we write the Fourier transform operator as this
[00:01:44 - 00:01:51] calligraphic f, or sometimes capital f, capital t, for Fourier transform.
[00:01:51 - 00:02:00] And we denote up here, Fourier p here, with an arrow, with two n's on it, between the
[00:02:00 - 00:02:03] time domain, x of t, and the frequency domain x of f.
[00:02:03 - 00:02:13] Okay, so there's this function between the Fourier series that we look at yesterday and
[00:02:13 - 00:02:15] Fourier transform.
[00:02:15 - 00:02:19] So the Fourier series is for only periodic signals, like that.
[00:02:19 - 00:02:26] Squeely, the triangle wave, we were looking at, we can generate a Fourier series for
[00:02:26 - 00:02:33] it because the periodic, they're not changing the fixed-free period.
[00:02:33 - 00:02:38] And the Fourier series, we then have our spectrum is discrete.
[00:02:38 - 00:02:44] So there are the coefficients a, k, and b, k, and those are defined for integer values
[00:02:44 - 00:02:45] of k.
[00:02:45 - 00:02:47] So that makes it a discrete.
[00:02:47 - 00:03:06] Whereas for our Fourier transform here, our continuous time signal x of t, this doesn't
[00:03:06 - 00:03:20] have to be periodic.
[00:03:20 - 00:03:29] And our continuous spectrum, so with the Fourier transform, our spectrum is continuous,
[00:03:29 - 00:03:34] here is our coefficients for the Fourier series.
[00:03:34 - 00:03:38] Also, a0, a, k, b, k are discrete.
[00:03:38 - 00:03:49] Okay, so both the Fourier series and Fourier transform can give us a spectrum of a time domain
[00:03:49 - 00:03:54] signal, but there's this different assumption on periodicity, and then, resultantly, there's
[00:03:54 - 00:03:59] a different spectrum to discrete or continuous.
[00:04:06 - 00:04:12] Okay, so one thing about the Fourier transforms that's certainly very confusing is that
[00:04:12 - 00:04:16] we end up with negative frequencies.
[00:04:16 - 00:04:20] Okay, so they don't really mean anything.
[00:04:20 - 00:04:26] It's a mathematical artifact of the Fourier transform.
[00:04:26 - 00:04:40] And so, from Euler's formula, we can write e to the j omega t is equal to cosine omega
[00:04:40 - 00:04:46] t plus j sine omega t.
[00:04:46 - 00:04:56] This is the angular frequency omega, which is 2 pi f.
[00:04:56 - 00:05:06] Or you could write our, the negative, this is minus j omega t is equal to cosine omega
[00:05:06 - 00:05:13] t minus j sine omega t.
[00:05:13 - 00:05:22] Okay, so one way to think about it is the negative frequencies represent the same oscillations,
[00:05:22 - 00:05:32] for the same number of cycles per second, for our same wave, but the positive frequencies
[00:05:32 - 00:05:41] are going one way, positive omega, and then, so that's anticlockwise, and then clockwise,
[00:05:41 - 00:05:44] we can think of as negative frequencies.
[00:05:44 - 00:05:51] So that oscillations at the same frequency, but they're going in opposite directions
[00:05:51 - 00:05:56] around the complex plane.
[00:05:56 - 00:06:03] Okay, but there's no physical reason or physical meaning of these negative frequencies.
[00:06:03 - 00:06:08] It's more that they are part of the mathematics of the Fourier transform.
[00:06:08 - 00:06:11] We end up with both positive and negative frequencies.
[00:06:11 - 00:06:28] Okay, so one consequence of the Fourier transform is that if our signal x of t is real,
[00:06:29 - 00:06:35] so if you think of a voltage signal in the circuit, it's got real numbers for it.
[00:06:35 - 00:06:42] And it's, so let's basically see anyway.
[00:06:42 - 00:06:48] And so if our signal is real, then its spectrum, capital x of f, has what we call
[00:06:48 - 00:06:52] Hermitian symmetry.
[00:06:52 - 00:07:00] And so this symmetry means that the spectrum of the negative frequencies, x of minus f, is
[00:07:00 - 00:07:05] equal to the complex conjugate, x star of f.
[00:07:05 - 00:07:14] So here star is the complex, and we get.
[00:07:14 - 00:07:20] Okay, so for the magnitudes, so we can spell this out in what it means for both the magnitude
[00:07:20 - 00:07:21] and phase.
[00:07:21 - 00:07:29] So for the magnitudes, it means the magnitude of the negative frequencies.
[00:07:29 - 00:07:37] And our spectrum is then equal to the magnitude of our positive frequencies of our spectrum.
[00:07:37 - 00:07:43] So that's the magnitude.
[00:07:43 - 00:07:54] And then for our phase, to the phase of our negative frequencies of our spectrum.
[00:07:54 - 00:07:58] So this symbol here is kind of like an angle.
[00:07:58 - 00:08:00] That's the noting.
[00:08:00 - 00:08:12] The phase that is then equal to the negative of the phase of the positive frequencies.
[00:08:12 - 00:08:23] Okay, so this symmetry then means if we know the spectrum for the positive frequencies,
[00:08:23 - 00:08:29] or you automatically know the spectrum for the negative frequencies.
[00:08:29 - 00:08:37] So there's no new information encoded in the negative frequencies that we don't have in
[00:08:37 - 00:08:39] a positive frequency component.
[00:08:39 - 00:08:45] Okay, so it's if our signal is real.
[00:08:45 - 00:09:07] Okay, so we've done our Fourier transform, takes us from the time domain.
[00:09:07 - 00:09:15] So the frequency domain, so signal little x and t, and seconds to our spectrum x and f.
[00:09:15 - 00:09:24] If we want to get our signal back from our spectrum, then we need the inverse Fourier transform.
[00:09:24 - 00:09:36] So this is then our signal x of t is equal to the integral from minus infinity to infinity
[00:09:36 - 00:09:46] our spectrum, capital x of f, e to the j to pi ft.
[00:09:46 - 00:09:51] So it's a complex exponential, and then we're integrating with respect to frequency f.
[00:09:51 - 00:09:59] Okay, so this is almost identical and format to the forward-grinding transform, except we're
[00:09:59 - 00:10:02] integrating over frequency in our time.
[00:10:02 - 00:10:12] And this complex exponential is positive rather than negative.
[00:10:12 - 00:10:19] Okay, so we can do these integrals to calculate our forward and inverse or reverse Fourier
[00:10:19 - 00:10:23] transforms using these integrals.
[00:10:23 - 00:10:33] But it's actually much easier if we have some tables of common properties and common Fourier
[00:10:33 - 00:10:37] transform pairs, then we can use instead of doing integrals each time.
[00:10:37 - 00:10:48] So it's quite a lot like the Laplace transforms we've done earlier, and we've done in other courses.
[00:10:48 - 00:10:49] Okay, so we're going to basically use the tables.
[00:10:49 - 00:11:00] We're going to do this integral for a special case now, which is this rectangular function
[00:11:00 - 00:11:02] that we find last week.
[00:11:02 - 00:11:12] So this function, shown in the figure here, has a value of 1 for t between minus 0.5 and 0.5.
[00:11:12 - 00:11:21] Okay, so this here is rit of t.
[00:11:21 - 00:11:29] Okay, so we're going to work out what's the Fourier pair of the rectangular function.
[00:11:29 - 00:11:35] Okay, so this goes up to two slides.
[00:11:35 - 00:11:38] So we'll start off with our definition of the Fourier transform.
[00:11:38 - 00:11:49] Capital x of f is equal to the integral from minus infinity to infinity of the signal x of t
[00:11:49 - 00:11:54] e to the minus j to pi ft dt.
[00:11:54 - 00:12:05] Okay, now we're going to substitute in our rectangular function for x of t.
[00:12:05 - 00:12:15] So let's do our limits of our integral become, yeah, that's good.
[00:12:15 - 00:12:17] Yep, so it's 0 for all other values.
[00:12:17 - 00:12:20] So we don't need to be integrating between minus infinity and infinity.
[00:12:20 - 00:12:24] We can just be integrating between minus 1.5 and 1.
[00:12:24 - 00:12:31] What's the value of x of t between minus 1.5 and 1.
[00:12:31 - 00:12:39] Okay, so we've simply now got 1 times e to the minus j to pi ft dt.
[00:12:39 - 00:12:48] Okay, now we have to remember our, I don't know if this is first-year maths or high school maths,
[00:12:48 - 00:12:57] too long ago, but if we integrate an exponential, we have the same exponential,
[00:12:57 - 00:13:00] e to the minus j to pi ft.
[00:13:00 - 00:13:06] And we are the multiply or divide by the coefficient of the exponential.
[00:13:06 - 00:13:12] And so we're dividing here the integral we divide for the derivative of the multiply.
[00:13:12 - 00:13:17] So we're dividing by minus j to pi f.
[00:13:17 - 00:13:26] And we're going to evaluate it at half and minus a half.
[00:13:26 - 00:13:35] Okay, so if we substitute in first of all, if we substitute in for t is a half,
[00:13:35 - 00:13:38] we have then a half cancels with the two.
[00:13:38 - 00:13:49] We have e to the minus j pi f over minus j to pi f.
[00:13:49 - 00:13:55] And we are then subtracting.
[00:13:55 - 00:13:59] So we substitute in minus a half for t's.
[00:13:59 - 00:14:10] This becomes minus e to the j pi f over j.
[00:14:10 - 00:14:23] Okay, so carry on on the next slide.
[00:14:23 - 00:14:29] And I'll make sure we run this code up before I transfer over.
[00:14:29 - 00:14:38] Okay, so I'm going to rearrange this so we can do simplify it a bit.
[00:14:38 - 00:14:53] So I'm now going to rewrite this as x of f is equal to 1 over pi f.
[00:14:53 - 00:14:56] So we're going to write this as a common factor out the front.
[00:14:56 - 00:15:18] And then e to the j pi f minus e to the minus j pi f j.
[00:15:18 - 00:15:31] Okay, what does the thing in the big-square brackets look like?
[00:15:31 - 00:15:32] Do you?
[00:15:32 - 00:15:33] I heard a whisper.
[00:15:33 - 00:15:34] It's a sign function.
[00:15:34 - 00:15:36] That equation's in the formula's shape.
[00:15:36 - 00:15:52] So this becomes x of f, put up the topic as a sign of x is equal to 1 over 2j e to the
[00:15:52 - 00:16:13] minus j e to the j x minus e to the minus j x.
[00:16:13 - 00:16:27] Okay, so this becomes sign of pi times the frequency f over pi times the frequency f.
[00:16:27 - 00:16:47] Okay, and we define sign pi f over pi f as this function called the sink function.
[00:16:47 - 00:16:55] Okay, so engineer is confusingly define the sink function of sign pi f over pi f and mathematicians.
[00:16:55 - 00:17:00] The same reason the finite is sign f over f.
[00:17:00 - 00:17:02] So that's well confusing.
[00:17:02 - 00:17:09] But we're going to use our pi's inside here for our sink definition.
[00:17:09 - 00:17:19] Okay, so what this means then we have our rectangular function here in the time domain is then a
[00:17:19 - 00:17:24] Fourier pair with our sink function in the frequency domain.
[00:17:24 - 00:17:32] Okay, and then the sink function is shown at the bottom.
[00:17:32 - 00:17:42] So it's a value of 1 at 0 and then it's oscillating in both the positive and negative values of f.
[00:17:42 - 00:17:49] And those oscillations get smaller as more of time with time that they go on forever.
[00:17:49 - 00:17:52] The rec function is finite.
[00:17:52 - 00:17:58] It just exists between .5 and minus .5 at 0 over else.
[00:17:58 - 00:18:10] Whereas the sink function has an infinite extent.
[00:18:10 - 00:18:22] Okay, these zero crossings occur at 1, 2, 3, 4, 5, etc.
[00:18:22 - 00:18:31] Okay, so if we look at the definition of the sink function here,
[00:18:31 - 00:18:34] the frequency is zero.
[00:18:34 - 00:18:41] We have sign of zero, which is zero, over zero, which is also zero.
[00:18:41 - 00:18:44] So we have zero over zero.
[00:18:44 - 00:18:48] The sink function has a value of 1 at zero.
[00:18:48 - 00:18:54] So what you can do to work out what this value of zero is to do something.
[00:18:54 - 00:19:01] You probably have a mass called Lop-Tiles rule where you take the derivative of top of the bottom as you take a limit.
[00:19:01 - 00:19:07] So here frequency going to zero and you would find out that that value is 1.
[00:19:07 - 00:19:13] So there is a discontinuity if you look at the definition here at 1,
[00:19:13 - 00:19:21] but the mass tells us that the sink function has a value of 1 for what f is zero.
[00:19:21 - 00:19:30] Okay, so this sink function is going to keep popping up throughout the course.
[00:19:30 - 00:19:35] So that's the only one I'm going to go through today using the Fourier transform integral.
[00:19:35 - 00:19:42] The rest of the common peers and properties I'll just present the results and we'll do some examples with them as well.
[00:19:42 - 00:19:55] Okay, so one interesting Fourier transform here is that if we have a DC values or constant,
[00:19:55 - 00:19:59] this forms a Fourier pair with the delta function.
[00:19:59 - 00:20:17] Okay, and these figures we have blue is the in the Fourier transform.
[00:20:17 - 00:20:28] Blue is the real part and orange is the imaginary part.
[00:20:28 - 00:20:35] Okay, so this is Lop-T capital X of f.
[00:20:35 - 00:20:43] So X of t is obviously a real function, but capital X of f spectrum can have both real and imaginary parts.
[00:20:43 - 00:20:55] We just have a real part of the delta function and the imaginary part is shown in orange along the f-axis is zero.
[00:20:55 - 00:21:08] Okay, and so there's a kind of a reciprocity in the Fourier pairs.
[00:21:08 - 00:21:14] So our constant value, this is infinitely wide,
[00:21:14 - 00:21:21] whereas the delta function is infinitely narrow.
[00:21:21 - 00:21:34] Okay, so that a true constant value here would have a value of one for all values of t,
[00:21:34 - 00:21:46] up to minus infinity, up to infinity, and the delta function is only defined at a value of zero.
[00:21:46 - 00:21:57] Okay, with these delta functions, so the area and the delta function is the find to be one,
[00:21:57 - 00:22:04] the integral of the delta function is one,
[00:22:04 - 00:22:09] and so in these figures with the delta function,
[00:22:09 - 00:22:12] because this delta function is actually infinitely high,
[00:22:12 - 00:22:18] but there's one here corresponds to the area of the delta function.
[00:22:18 - 00:22:24] So if we've got half the delta function, which we have in our next example of the cosine and sine,
[00:22:24 - 00:22:29] then those delta functions will be up to half on the y-axis,
[00:22:29 - 00:22:33] but actually, they're infinite in all cases.
[00:22:33 - 00:22:39] Okay, so that's another common delta function,
[00:22:39 - 00:22:43] and then we'll go through cosine and sine,
[00:22:43 - 00:22:48] which we also need.
[00:22:48 - 00:23:01] Okay, so cosine to pi some characteristic frequency,
[00:23:01 - 00:23:06] if not of t, forms of Fourier pair,
[00:23:06 - 00:23:11] and its Fourier pair is at two delta functions,
[00:23:11 - 00:23:16] which replace the plus and minus our frequency, if not.
[00:23:16 - 00:23:20] So with the extra delta function has an area of a half,
[00:23:20 - 00:23:31] so we have half delta, if minus, if not, plus half delta, if plus,
[00:23:31 - 00:23:37] if not.
[00:23:37 - 00:23:40] Okay, so these delta functions are both real,
[00:23:40 - 00:23:46] so again, blue is imaginary orange, sorry, wrong around,
[00:23:46 - 00:24:03] but is real orange imaginary.
[00:24:03 - 00:24:14] Okay, and here this point five means the area of each delta equals point.
[00:24:14 - 00:24:26] Okay, so here we've got x of t,
[00:24:26 - 00:24:36] here couple x of f. Okay, and so our,
[00:24:36 - 00:24:39] and the figure I've got here,
[00:24:39 - 00:24:46] if not, we've got one cycle of our sine wave in one second,
[00:24:46 - 00:24:50] that's the if not is then one hertz,
[00:24:50 - 00:24:55] and so these delta is which are plus and minus if not,
[00:24:55 - 00:25:00] at one and minus one, frequency and hertz,
[00:25:00 - 00:25:17] and then we've got two times the second.
[00:25:17 - 00:25:23] So those are the four most important Fourier transform pairs,
[00:25:23 - 00:25:26] and they appear in the form of the sheet,
[00:25:26 - 00:25:30] and then the next thing we'll go through is the key properties of the Fourier transform,
[00:25:30 - 00:25:33] and then we'll do a couple of examples as well.
[00:25:33 - 00:25:38] Oh, sorry, I haven't done the sign yet.
[00:25:38 - 00:25:41] So sine is a lot like cosine,
[00:25:41 - 00:25:45] so we get two deltas, but they, for the sine,
[00:25:45 - 00:25:48] so we have sine two pi if not t,
[00:25:48 - 00:25:52] so here we have frequency,
[00:25:52 - 00:26:03] again, of our sine wave if not is one hertz.
[00:26:03 - 00:26:06] So if not is the frequency of our sine wave,
[00:26:06 - 00:26:09] that forms a Fourier pair with minus j on two delta,
[00:26:09 - 00:26:12] if we have a square of the sine wave,
[00:26:12 - 00:26:14] so we'll do a square of the sine wave,
[00:26:14 - 00:26:16] so we'll do a square of the sine wave,
[00:26:16 - 00:26:21] and this is minus j on two delta,
[00:26:21 - 00:26:27] if minus if not, plus j on two delta,
[00:26:27 - 00:26:32] if plus if not.
[00:26:32 - 00:26:39] So our delta is here and now shown as orange,
[00:26:39 - 00:26:46] because they are imaginary,
[00:26:46 - 00:26:49] and the blue part is real,
[00:26:49 - 00:26:53] and in this case, because both the delta is multiplied by,
[00:26:53 - 00:27:05] j on two, or j on two, they are imaginary.
[00:27:05 - 00:27:11] So that's the four common Fourier pairs
[00:27:11 - 00:27:21] that we need for now.
[00:27:21 - 00:27:30] Then we have some common properties of the Fourier transform.
[00:27:30 - 00:27:33] So the first one, the easiest one is linearity,
[00:27:33 - 00:27:35] so we're going to consider here,
[00:27:35 - 00:27:37] say signal G of t,
[00:27:37 - 00:27:42] and so it has a Fourier pair, capital G of f.
[00:27:43 - 00:27:46] So if we have G of t,
[00:27:46 - 00:27:50] and we multiply it by sine constant A,
[00:27:50 - 00:27:54] that means we also scale its Fourier pair,
[00:27:54 - 00:27:58] the spectrum capital G of f, also by A.
[00:27:58 - 00:28:12] Okay, and we can use the principle of superposition
[00:28:12 - 00:28:20] for what happens if we take the Fourier transform
[00:28:20 - 00:28:24] of a sum of signals that's equal to the sum of the spectrum.
[00:28:24 - 00:28:27] So if we have our signal,
[00:28:27 - 00:28:34] we want to take the Fourier transform as A G of t plus B H of t.
[00:28:34 - 00:28:37] So here we've got two signals G of t and H of t,
[00:28:37 - 00:28:40] scaled by A and B respectively.
[00:28:40 - 00:28:44] If we take the Fourier transform of the whole thing,
[00:28:44 - 00:28:49] we then have A times G of f plus,
[00:28:49 - 00:28:53] B times H of f.
[00:28:53 - 00:28:58] So we can take the Fourier transform of G,
[00:28:58 - 00:29:01] little G and the whole H independently,
[00:29:01 - 00:29:04] and then add their spectra together
[00:29:04 - 00:29:09] to get the spectrum of the overall signal.
[00:29:09 - 00:29:27] Okay, so together those two equations give us the linearity theorem,
[00:29:27 - 00:29:35] the next one is something known as the scaling theorem.
[00:29:35 - 00:29:37] So here I'll use X's.
[00:29:37 - 00:29:40] So we've got X of t in the time domain,
[00:29:40 - 00:29:50] and this has a spectrum in the Fourier domain X of f.
[00:29:50 - 00:29:59] Okay, so if we scale our signal in time by some constant A,
[00:29:59 - 00:30:04] so you can think of as shrinking or expanding,
[00:30:04 - 00:30:12] say for example here our rec function.
[00:30:12 - 00:30:16] So if we scale it in the time domain,
[00:30:16 - 00:30:24] within in the frequency domain, our scale it the other way.
[00:30:24 - 00:30:28] So if we're making it wider in the time domain,
[00:30:28 - 00:30:31] it's going to become narrower in the frequency domain,
[00:30:31 - 00:30:38] and then we also get an extra scaling in the spectrum.
[00:30:38 - 00:30:41] So it's one over the magnitude of A.
[00:30:41 - 00:30:44] Okay, so if we make a single narrower,
[00:30:44 - 00:30:47] a spectrum becomes wider,
[00:30:47 - 00:30:50] and then also to conserve area,
[00:30:50 - 00:30:53] it becomes wider and lower.
[00:30:55 - 00:30:59] And if we make the signal wider,
[00:30:59 - 00:31:02] a spectrum becomes narrower.
[00:31:02 - 00:31:05] So example we have here,
[00:31:05 - 00:31:10] so in the time domain we've got rec of t,
[00:31:10 - 00:31:15] and this is a Fourier pair with sync of f,
[00:31:15 - 00:31:20] so this rec function is the find between a half,
[00:31:20 - 00:31:22] and minus a half,
[00:31:22 - 00:31:27] and then our rec function at the bottom is now defined between one and minus one.
[00:31:27 - 00:31:42] So we have rec of here our constant,
[00:31:42 - 00:31:46] that was scaling by is effectively a half.
[00:31:46 - 00:31:52] So if our value of A is less than one,
[00:31:52 - 00:31:54] we are expanding us.
[00:31:54 - 00:31:56] If the value of A is greater than one,
[00:31:56 - 00:31:58] we are then shrinking it.
[00:31:59 - 00:32:04] So in the bottom row we have then rec of t over two.
[00:32:04 - 00:32:11] Okay, so we've made our rectangular function wider by scaling by half,
[00:32:11 - 00:32:16] and so then it's Fourier pair becomes narrower.
[00:32:16 - 00:32:23] So if we keep making our rec function wider and wider and wider,
[00:32:23 - 00:32:27] what does it's Fourier pair start to look like?
[00:32:27 - 00:32:35] Common functions delta.
[00:32:35 - 00:32:37] Yes.
[00:32:37 - 00:32:39] Good. So we're just squeezing it.
[00:32:39 - 00:32:47] So it's one of the ways to prove the Fourier pair between a constant value and a delta.
[00:32:47 - 00:32:59] Okay, so then what's the equation for this sync function going to be sync to f,
[00:32:59 - 00:33:07] and what happens to my one over magnitude of A?
[00:33:07 - 00:33:10] So exactly.
[00:33:10 - 00:33:17] So this is now got a value of two.
[00:33:17 - 00:33:19] Okay, so I'll just do all that.
[00:33:19 - 00:33:28] This is the one over the magnitude of A.
[00:33:28 - 00:33:32] Okay, so basically idea we make something wider and wider main,
[00:33:32 - 00:33:50] it becomes narrower in the other domain.
[00:33:50 - 00:33:56] Okay, and then we also have some properties to do with shifting.
[00:33:56 - 00:34:00] So if we have a signal and we shift it by the amount,
[00:34:00 - 00:34:02] T not in time.
[00:34:02 - 00:34:14] So again, let's consider it out here being X of T and time domain capital X of F as its spectrum.
[00:34:14 - 00:34:25] So if we have some shift X of T minus tau,
[00:34:25 - 00:34:35] or this tau, because that's what my equation's got.
[00:34:35 - 00:34:41] Then the magnitude is the same from the shift.
[00:34:41 - 00:34:48] So magnitude is still X of F.
[00:34:48 - 00:34:57] The shifting introduces a linear phase shift, E to the minus J to pi F tau.
[00:34:57 - 00:35:04] Okay, so if we don't have the shift, the Fourier transform of a lower X of T is capital X of F.
[00:35:04 - 00:35:11] But by shifting in time, we're multiplying by a linear convex exponential in the Fourier domain.
[00:35:11 - 00:35:23] Okay, and we can do the same thing.
[00:35:23 - 00:35:31] And if we multiply in the time domain by a complex exponential,
[00:35:31 - 00:35:36] so here is the J to pi A t,
[00:35:36 - 00:35:42] this then shifts our frequency spectrum by an amount.
[00:35:42 - 00:35:58] Okay, so the first one is known as time shifting and the second one as frequency shifting.
[00:35:58 - 00:36:07] Okay, let's do a problem together.
[00:36:07 - 00:36:12] There's a fist, everything will hurt so far.
[00:36:12 - 00:36:18] Okay, so here we've got a rectangular function, X of T.
[00:36:18 - 00:36:24] So it's defined between T is two and T is four, with a value of four.
[00:36:24 - 00:36:34] So the first thing we need to do is to write down our signal X of T.
[00:36:34 - 00:36:39] Okay, well, the first thing you can tell me about X of T.
[00:36:39 - 00:36:42] That's shifted.
[00:36:42 - 00:36:48] Okay, so we've got, so we know there's a rectangular function.
[00:36:48 - 00:36:51] We've already told you that so we've got rict.
[00:36:51 - 00:36:56] And it's a function of T here, so we've got T.
[00:36:56 - 00:37:02] How much is it shifted by?
[00:37:02 - 00:37:03] Three.
[00:37:03 - 00:37:04] Yep.
[00:37:04 - 00:37:06] So it's got T minus three.
[00:37:06 - 00:37:11] Well, the two things I need to define my signal X of T.
[00:37:11 - 00:37:16] And for two to four, so we'll stick that out from here.
[00:37:16 - 00:37:19] So this is four, is this four.
[00:37:19 - 00:37:22] And what else do I need?
[00:37:22 - 00:37:30] So this has got here a period of T is two.
[00:37:30 - 00:37:34] So then I need to divide this by two.
[00:37:34 - 00:37:48] Okay, what's its Fourier transform?
[00:37:48 - 00:37:49] So what?
[00:37:49 - 00:37:52] Capital X of F.
[00:37:52 - 00:37:58] What do we do about this four into the Fourier transform?
[00:37:58 - 00:38:03] Yeah, so it says the four.
[00:38:03 - 00:38:05] So this is from, for each of these things,
[00:38:05 - 00:38:06] I'll write down which theorems.
[00:38:06 - 00:38:08] So this is from the linearity theorem.
[00:38:08 - 00:38:13] Okay, if we multiply a signal by a constant and a time domain,
[00:38:13 - 00:38:16] that constant appears in the frequency domain as well.
[00:38:16 - 00:38:26] Okay, and so we've got a rectangular function.
[00:38:26 - 00:38:32] And this time domain, so that's going to become a sync function
[00:38:32 - 00:38:34] in the frequency domain.
[00:38:34 - 00:38:44] So we've got this scaling factor here.
[00:38:44 - 00:38:48] T here is, or A here is a half.
[00:38:48 - 00:38:59] So that means our sync function is going to be two F.
[00:38:59 - 00:39:03] Like the example from the slides a couple of times,
[00:39:03 - 00:39:07] slides ago we have been one over A at the front here.
[00:39:07 - 00:39:11] So we've got two F and this factor of two out the front from
[00:39:11 - 00:39:14] the scaling property of the Fourier transform.
[00:39:14 - 00:39:20] I'll just write it on top here that rect of T is a Fourier
[00:39:20 - 00:39:22] here with a sync of F.
[00:39:22 - 00:39:30] And what is missing?
[00:39:30 - 00:39:36] Yeah, the shift and so what we do with the shift,
[00:39:36 - 00:39:45] we have this complex exponential, E is minus J2 pi
[00:39:45 - 00:39:49] and our tau, our shift was three.
[00:39:49 - 00:39:53] So then multiply by three and have frequency here.
[00:39:53 - 00:39:55] So this is shifting.
[00:39:55 - 00:40:00] And we can also simplify this.
[00:40:00 - 00:40:06] I haven't left myself room here, but X of F is then equal to 8 sync
[00:40:06 - 00:40:14] to F, E to the minus J6 pi.
[00:40:14 - 00:40:36] So if T is minus the go, okay, so the last thing we need to do
[00:40:36 - 00:40:45] with is your old friend convolution and the convolution theorem.
[00:40:45 - 00:40:50] Okay, so do a quick recap of what the convolution is
[00:40:50 - 00:40:53] and I'll talk through the GIF below.
[00:40:53 - 00:40:59] So we've got two signals X of T and H of T and we can
[00:40:59 - 00:41:01] solve them.
[00:41:01 - 00:41:06] So X of T convolved with H of T is equal to the integral
[00:41:10 - 00:41:16] from minus infinity to infinity of X of the dummy variable
[00:41:16 - 00:41:23] tau H of T minus tau P tau, okay, and here star is
[00:41:23 - 00:41:28] the convolution operator.
[00:41:28 - 00:41:38] Okay, so conceptually what we're doing is we're getting
[00:41:38 - 00:41:44] one of our two operands to H.
[00:41:44 - 00:41:49] We've reversed it in time and then we shift it across the
[00:41:49 - 00:41:58] other function and we integrate the product over the
[00:41:58 - 00:42:02] the product over that and the two functions for each
[00:42:02 - 00:42:05] shift. So here we've got in the GIF that I've
[00:42:05 - 00:42:09] changed this column from Wikipedia is the convolution of
[00:42:09 - 00:42:15] two rectangular functions.
[00:42:15 - 00:42:19] So we're shifting the red function across the blue function
[00:42:19 - 00:42:24] and the yellow indicates the area under the two and
[00:42:24 - 00:42:28] black is the result of the convolution.
[00:42:28 - 00:42:33] Okay, so I'll just change the notation in these.
[00:42:33 - 00:42:38] So it matches my equation.
[00:42:38 - 00:42:43] So yellow is the area under the product of X of T times
[00:42:43 - 00:43:01] H of X of tau H of T minus tau and then blue can be X of
[00:43:01 - 00:43:08] red can be H of T minus tau here there actually the same
[00:43:08 - 00:43:12] and the reversing doesn't do anything because the
[00:43:12 - 00:43:17] rectangle function is symmetric and then the black one is
[00:43:17 - 00:43:25] the result of the convolution X of T convolved with H of T.
[00:43:25 - 00:43:31] Okay, so who likes convolution? No one.
[00:43:31 - 00:43:36] Oh, one person good, but so the Fourier transform allows us to
[00:43:36 - 00:43:40] get rid of convolution. Convolution is really
[00:43:40 - 00:43:44] computationally intensive. So each time you kind of shift
[00:43:44 - 00:43:48] them to disintegrate, it's quite a lot of floating point
[00:43:48 - 00:43:52] operations. If we're dealing with digital signals.
[00:43:52 - 00:43:57] So the convolution theorem allows us to convert a convolution
[00:43:57 - 00:44:01] in the time domain to multiplication in the Fourier domain.
[00:44:01 - 00:44:05] And so that's much faster to do on a computer than the
[00:44:05 - 00:44:07] convolution integral.
[00:44:07 - 00:44:29] Yeah. Okay, so the Fourier transform converts a convolution to a
[00:44:29 - 00:44:37] multiplication. Okay, so we had, there we had X of T convolved
[00:44:37 - 00:44:47] with H of T. That makes the Fourier pair with X of F convolved with H of F.
[00:44:47 - 00:44:51] Okay, so left hand side, we've got the same integral shifting.
[00:44:51 - 00:44:57] So I like to work right hand side, we've got a multiplication.
[00:44:57 - 00:45:04] So if we wanted to do X of T convolved with H of T, we would
[00:45:04 - 00:45:17] take the Fourier transform of X of T to get X of F. Take the
[00:45:17 - 00:45:25] Fourier transform of H of T to get H of F. We would multiply those
[00:45:25 - 00:45:32] two things together. Then we'd take the inverse Fourier transform,
[00:45:32 - 00:45:38] and that would give us X of T convolved with H of T.
[00:45:38 - 00:45:45] And so it might seem mad to be doing two-forward Fourier transforms,
[00:45:45 - 00:45:50] a multiplication, then an inverse Fourier transform.
[00:45:50 - 00:45:56] But that's less work computationally in most cases than doing this convolution integral.
[00:45:56 - 00:46:07] Okay, so that's where we have convolution of two signals in the time domain.
[00:46:07 - 00:46:12] And because of the symmetry of the forward and inverse Fourier transforms,
[00:46:12 - 00:46:19] we can, if we have two signals multiple I together in the time domain,
[00:46:19 - 00:46:29] X of T times H of T, this means we're convolving this spectra in the frequency domain.
[00:46:29 - 00:46:46] Okay, so that means that, and we'll see this when we do some filtering examples,
[00:46:46 - 00:46:49] that we are multiplying two signals in the time domain.
[00:46:49 - 00:46:56] We are introducing a convolution in the frequency domain effectively.
[00:46:56 - 00:47:01] So if we are multiplying a signal by a rectangular function,
[00:47:01 - 00:47:07] so we're doing windowing in the time domain, we are then convolving the spectrum
[00:47:07 - 00:47:13] of our signal with a sync function. So we're introducing then ringing in the frequency domain.
[00:47:13 - 00:47:23] Okay, so we'll start for a couple of minutes.
[00:47:23 - 00:47:30] An example of doing convolution of two functions.
[00:47:30 - 00:47:36] So let's consider our function Y of T.
[00:47:36 - 00:47:41] Here is the product of some cosine, cosine, the two pi,
[00:47:41 - 00:47:52] and if not T with the rectangular function T over capital T.
[00:47:52 - 00:47:59] Okay, so this is then a sinusoidal or cosine on your sort of tone.
[00:47:59 - 00:48:05] It's got just for a short duration of capital T.
[00:48:05 - 00:48:09] And this is an example that you have in sessona or later,
[00:48:09 - 00:48:13] where you emit a pulse, say from your shift to the sona,
[00:48:13 - 00:48:19] down just for a finite period in time, and then you're waiting for the signal
[00:48:19 - 00:48:22] to bounce off the ocean floor to come back to view.
[00:48:22 - 00:48:24] So you're not transmitting the whole time.
[00:48:24 - 00:48:28] You only do it for a short period in time, and then wait for the pulse to come back.
[00:48:28 - 00:48:32] So this is a cosine pulse, and because it's a finite duration,
[00:48:32 - 00:48:36] we're effectively multiplying by a rectangular function.
[00:48:36 - 00:48:43] Okay, so we can split this then into two functions.
[00:48:43 - 00:48:51] Essentially we'll call them H of T is the cosine part cosine 2 pi,
[00:48:51 - 00:49:01] if not T, and then the rectangular part is rich of little T over capital T.
[00:49:01 - 00:49:13] Okay, so then we can take the, for a transfer of both to get this vector out,
[00:49:13 - 00:49:21] and the vector will get capital H of F is then a half delta,
[00:49:21 - 00:49:33] if plus, if not, plus a half delta, if minus, if not,
[00:49:33 - 00:49:40] and by our rectangular function then we have as previous capital T,
[00:49:40 - 00:49:50] period of the burst of duration, sync, if T.
[00:49:50 - 00:49:53] So in the time domain, we're multiplying these two together,
[00:49:53 - 00:49:55] and then in the frequency domain,
[00:49:55 - 00:50:03] why are they, we have this convolution of this vector H of F and G of F?
[00:50:03 - 00:50:09] Okay, so it's T into, I'll stop there, I'll put the slide up at the start of
[00:50:09 - 00:50:14] Wednesday's lecture, and you can finish writing those down now,
[00:50:14 - 00:50:17] or I'll leave it up until I leave in a few minutes as well.
[00:50:17 - 00:50:21] Okay, so there's more tutorial problems up on learn if you want to have a look.
[00:50:21 - 00:50:41] The one exercise, and the answers from yesterday's tutorial problems are up there as well.
[00:51:01 - 00:51:05] So that's it, can we just want to do our next topic?
[00:51:05 - 00:51:07] Do you want to solve it?
[00:51:07 - 00:51:09] Do you want to do any of these things?
[00:51:09 - 00:51:13] Yeah, so I don't think I'm going to really make money,
[00:51:13 - 00:51:15] or do you, pitches?
[00:51:15 - 00:51:17] Yeah, one next, please.
[00:51:17 - 00:51:19] Okay, thank you.

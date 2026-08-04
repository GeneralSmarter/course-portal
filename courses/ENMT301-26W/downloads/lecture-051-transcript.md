# ENMT301-26W Lecture 51 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `47a939f89898510ab40b17eb03439ebf95ca829de1346e283d11c1acf5ee442b`
Generated: 2026-06-06T06:57:02.811327+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:10 - 00:00:14] Okay 12 o'clock so good afternoon something Jew
[00:00:16 - 00:00:19] Or it's just the mass right after no okay
[00:00:19 - 00:00:21] Few people here the novel
[00:00:25 - 00:00:27] Oh, yeah, right you're the fluids
[00:00:28 - 00:00:30] Yeah, crap, okay
[00:00:30 - 00:00:32] I understand okay, so
[00:00:35 - 00:00:37] Today we're gonna finish off our
[00:00:37 - 00:00:43] Elon filters and then next week we'll get into looking at digital filters so filter you can program on a microcontroller
[00:00:46 - 00:00:49] Okay, so we've been looking at this RC filter at the top right here
[00:00:50 - 00:00:52] And so this is a low-pass filter
[00:00:53 - 00:00:55] and so some of the properties of
[00:00:56 - 00:00:58] this filter
[00:00:58 - 00:01:00] especially it's
[00:01:00 - 00:01:03] first order so it's just got one pole and
[00:01:03 - 00:01:05] and it's
[00:01:05 - 00:01:08] Frequency response rolls off at 20 disables per decade
[00:01:10 - 00:01:12] So this filter is also stable
[00:01:13 - 00:01:18] That means it's response decays with time. It's not increasing without bound
[00:01:19 - 00:01:27] And so this RC filter is as I said just before is a single pole and that pole is in the left half plane
[00:01:28 - 00:01:31] So for it to be stable the poles need to be in the left
[00:01:31 - 00:01:41] Or it's plain
[00:01:41 - 00:01:43] Okay, so the filter is also
[00:01:43 - 00:01:48] Quar tools that transient response counts that before t is zero
[00:01:49 - 00:01:54] So if we reflect with switch on in a circuit
[00:01:55 - 00:02:00] The circuit can't respond until we flip the switch. Okay, so nothing can happen before
[00:02:01 - 00:02:06] t is zero or when we close the circuit on the switch
[00:02:08 - 00:02:14] Close the switch in the circuit. Okay, so it's also time invariant
[00:02:15 - 00:02:17] As it's not changing with time
[00:02:17 - 00:02:19] Mostly the resistor might
[00:02:20 - 00:02:23] Change slightly as it heats up, but
[00:02:24 - 00:02:29] Essentially it's time invariant the impulse response is not going to change with time
[00:02:29 - 00:02:34] And then lastly here it is
[00:02:35 - 00:02:38] linear set means superposition applies
[00:02:39 - 00:02:41] So what that means is that
[00:02:42 - 00:02:52] If our output from the filter Y of t is the sum of two input signals x1 of t and x2 of t and
[00:02:53 - 00:02:59] They are convolved with the impulse response for our filter H of t is our impulse response
[00:03:00 - 00:03:17] So this can also be written then as the convolution of x1 of t with H of t plus the convolution of x2 of t
[00:03:18 - 00:03:20] with
[00:03:20 - 00:03:22] H of t
[00:03:22 - 00:03:29] Okay, so we add the two signals and enter the convolution or we can do the comp two convolutions and then add the result
[00:03:30 - 00:03:32] Okay, so that makes it linear and
[00:03:32 - 00:03:39] If we make our analog filter out of resistors and actors and capacitors then the filter has to be linear
[00:03:39 - 00:03:41] This is not true if we're using
[00:03:42 - 00:03:44] semiconductor devices
[00:03:44 - 00:03:48] Such as diodes transistors not pamps. They're all going to be
[00:03:48 - 00:03:51] Make our filter possibly non-linear
[00:03:52 - 00:03:54] And then this was anyway, we've just been looking at filters
[00:03:55 - 00:03:58] We're just going to look at filters with passive components
[00:03:59 - 00:04:01] resistors, capacitors and inductors
[00:04:06 - 00:04:08] Okay, so
[00:04:08 - 00:04:11] We can do a little summary of what we've looked at so far in terms of our
[00:04:12 - 00:04:16] different properties different functions of our
[00:04:17 - 00:04:19] filter
[00:04:19 - 00:04:21] okay, so
[00:04:21 - 00:04:29] We start off with our transfer function H of s and this was defined as the output voltage
[00:04:29 - 00:04:32] The over this over the I of s and
[00:04:33 - 00:04:35] So we get that from the circuit
[00:04:35 - 00:04:49] Okay, so if we take the inverse Laplace transform capillator this we get the impulse response
[00:04:50 - 00:04:53] H of t
[00:04:53 - 00:05:01] Okay, the impulse response is important as we had on the previous slide where you can get the output as the convolution of the input with the impulse response
[00:05:04 - 00:05:06] okay, so we also have our
[00:05:08 - 00:05:10] Step response which we can get by
[00:05:10 - 00:05:18] Multiplying by one over s so in the last domain if we multiply by one over s. This is integration
[00:05:21 - 00:05:23] If we then take the
[00:05:23 - 00:05:28] inverse Laplace transform of our transfer function divided by s we get our step response G of t and
[00:05:31 - 00:05:33] If we take a derivative of
[00:05:36 - 00:05:39] this step response
[00:05:39 - 00:05:42] G of t with respect to time we get our impulse response H of t
[00:05:43 - 00:05:48] So that's top load here. We go integrate to upper level and then we derivative it
[00:05:49 - 00:05:51] Differentiate to go back down the impulse response
[00:05:55 - 00:05:56] okay, so
[00:05:56 - 00:06:03] We can also define what's known as the frequency response so we replace our complex variable s
[00:06:04 - 00:06:06] with
[00:06:06 - 00:06:16] our frequency so we end up with the frequency response H to J2 by f or H of s and that is then a Fourier pair
[00:06:17 - 00:06:21] With the impulse response little H of t
[00:06:24 - 00:06:30] Okay, now put all the star on this conversion from the transfer function to the frequency response
[00:06:32 - 00:06:34] Here, so this is not always valid
[00:06:40 - 00:06:42] so if we consider
[00:06:43 - 00:06:46] Say our integrator H of s is
[00:06:47 - 00:06:51] One over s we are then going to have a problem
[00:06:53 - 00:06:55] For a DC frequency
[00:06:56 - 00:06:58] So we would have one over the frequency
[00:07:00 - 00:07:02] So we would have an infinite value there
[00:07:04 - 00:07:06] Okay, and this is
[00:07:06 - 00:07:08] the
[00:07:08 - 00:07:10] transfer function for an integrator
[00:07:11 - 00:07:13] Okay, so that's the solution of
[00:07:15 - 00:07:20] s is G2 by f to go from the transfer function to the frequency response is not
[00:07:21 - 00:07:23] valid it is for
[00:07:24 - 00:07:27] Most of the circuits we're looking at
[00:07:30 - 00:07:32] Okay, so then we also had
[00:07:34 - 00:07:36] from our
[00:07:38 - 00:07:42] Transfer function is not shown here, but we could get our
[00:07:43 - 00:07:47] DC response which was
[00:07:48 - 00:07:57] Capital H of 0 and we can get our
[00:07:58 - 00:08:00] AC response to some
[00:08:01 - 00:08:04] Sign or cosine of a particular frequency here if one
[00:08:05 - 00:08:07] We've had the real part of the
[00:08:09 - 00:08:11] incoming M2v1
[00:08:12 - 00:08:16] Multiply it by our transfer function couple h of f and then
[00:08:18 - 00:08:20] we have our
[00:08:21 - 00:08:29] Phase encoded as a complete sorry our frequency encoded on the complex exponential either J2 pi if 1 t
[00:08:30 - 00:08:32] Okay, so those are all things we looked at
[00:08:32 - 00:08:34] For our RC circuit
[00:08:34 - 00:08:39] yesterday
[00:08:39 - 00:08:43] And before okay, so let's go and look at some different types of circuits now
[00:08:45 - 00:08:47] so let's
[00:08:48 - 00:08:50] Low-pass focus of the one
[00:08:50 - 00:08:55] At the top we've been looking at
[00:08:55 - 00:08:57] The two ways here we can make a low-pass
[00:08:58 - 00:09:00] Circuit from low-pass filter from two
[00:09:02 - 00:09:04] components so
[00:09:04 - 00:09:06] For our
[00:09:06 - 00:09:08] RC circuit we saw yesterday
[00:09:08 - 00:09:11] That our cutoff frequency was 1 over 2 pi
[00:09:11 - 00:09:15] RC
[00:09:15 - 00:09:18] We can also make a low-pass filter within inductor and a resistor
[00:09:18 - 00:09:20] So the resistor is across the output
[00:09:21 - 00:09:25] And in that case we had our cutoff frequency if C is
[00:09:26 - 00:09:29] Over 2 pi L
[00:09:35 - 00:09:37] Okay, and so then we have
[00:09:38 - 00:09:41] Here our cutoff frequency I think is at
[00:09:42 - 00:09:44] 10 hertz maybe
[00:09:44 - 00:09:46] So we've got here
[00:09:46 - 00:09:50] This is our cutoff frequency and then at the cutoff frequency
[00:09:50 - 00:09:52] We've got a 3 dB drop in
[00:09:53 - 00:09:57] magnitude
[00:09:57 - 00:09:59] Okay, so this if C is the cutoff frequency
[00:10:10 - 00:10:12] Okay, and so we've got here
[00:10:12 - 00:10:27] Low frequencies pass and it's generated and our high frequencies are attenuated
[00:10:34 - 00:10:37] Okay, we've got a slope for this we've got a first order
[00:10:43 - 00:10:45] Low-pass filter here so we've got a drop of
[00:10:46 - 00:10:53] Then the slope here is
[00:10:53 - 00:10:55] 20
[00:10:55 - 00:10:57] Right, sweet DB per decade
[00:10:58 - 00:11:04] Okay, we'll look at second order and higher on the filters shortly
[00:11:09 - 00:11:12] Okay, so some people can look at these filters and then
[00:11:14 - 00:11:16] What about let's tell low-pass filters? So
[00:11:17 - 00:11:19] if you consider
[00:11:21 - 00:11:23] The governing equations for say a capacitor
[00:11:24 - 00:11:26] I as C
[00:11:26 - 00:11:28] Db by Dt and V is L
[00:11:28 - 00:11:30] D i by Dt
[00:11:33 - 00:11:35] We have the capacitor
[00:11:36 - 00:11:37] then
[00:11:37 - 00:11:39] Blox the low frequencies
[00:11:39 - 00:11:44] Dc
[00:11:44 - 00:11:46] Okay, so that means that the
[00:11:46 - 00:11:49] There's going to be no voltage across here
[00:11:51 - 00:11:56] So then the output voltage will be the input voltage
[00:11:58 - 00:12:02] For the low-pass filter
[00:12:02 - 00:12:04] So the capacitor blocks Dc
[00:12:04 - 00:12:15] But it passes AC and the inductor is the opposite so it passes Dc
[00:12:15 - 00:12:22] But it
[00:12:22 - 00:12:24] Lox AC
[00:12:24 - 00:12:34] Okay, so that is a way
[00:12:34 - 00:12:39] To kind of analyze the filters by I not going through and calculate a transfer function and a frequency response in the rest
[00:12:40 - 00:12:44] To try and work out whether it's a low-pass or a high-pass filter
[00:12:47 - 00:12:52] Okay, so that happens if we say swap the order of the resistor and the capacitor around
[00:12:52 - 00:13:01] So become a high-pass filter and same goes if we swap the order of the resistor and the inductor around
[00:13:02 - 00:13:04] We'll get a high-pass filter
[00:13:05 - 00:13:10] Okay, and then just look at my notes here. I also will write that we might use a low-pass filter to remove
[00:13:11 - 00:13:40] High frequency noise
[00:13:40 - 00:13:42] Okay, so this is the proof
[00:13:43 - 00:13:46] So now we've got the figures right there the other way around
[00:13:47 - 00:13:48] So we've got a high-pass filter here
[00:13:49 - 00:13:50] So again, we've got
[00:13:51 - 00:13:53] Our cutoff frequency is at 10 hertz
[00:13:54 - 00:13:56] So this is our 3db
[00:13:56 - 00:14:03] We're still first order
[00:14:03 - 00:14:05] So this is
[00:14:05 - 00:14:08] So many db a decade here
[00:14:11 - 00:14:19] So the high frequency is passed and it's enumerated
[00:14:29 - 00:14:31] Okay, and you could use this for example to
[00:14:32 - 00:14:34] remove
[00:14:35 - 00:14:41] DC drifts from our signal
[00:14:42 - 00:14:45] So we just get the high frequency components
[00:14:46 - 00:14:48] So
[00:14:48 - 00:14:54] The low frequencies are attenuated
[00:15:02 - 00:15:04] Okay, and so the equations for Fc
[00:15:06 - 00:15:09] The same as the previous slide so Fc is
[00:15:11 - 00:15:13] One over 2 pi
[00:15:13 - 00:15:15] C or
[00:15:16 - 00:15:18] Fc is equal to
[00:15:18 - 00:15:22] Over 2 pi L
[00:15:22 - 00:15:24] Okay, so these are just mirror images
[00:15:25 - 00:15:30] The circuits are mirror images and then the frequency responses shown here are also
[00:15:31 - 00:15:32] So
[00:15:32 - 00:15:36] mirror images
[00:15:36 - 00:15:37] Okay, so let's do something
[00:15:37 - 00:15:41] What interesting then? So let's look at a band pass filter
[00:15:42 - 00:15:44] So then a band pass filter
[00:15:44 - 00:15:46] Allows a certain range of frequencies
[00:15:47 - 00:15:49] To pass through
[00:15:50 - 00:15:51] So here we have then
[00:15:52 - 00:15:53] In this example we've got
[00:15:55 - 00:15:57] Two cutoff frequencies
[00:15:57 - 00:16:02] So we'll have here fc1 and fc2
[00:16:02 - 00:16:08] So here between 1 and 100 hertz are going to be allowed the pass through the circuit
[00:16:10 - 00:16:14] But then frequencies less than a hertz or less than 100 hertz
[00:16:14 - 00:16:19] So less than a hertz or greater than 100 hertz are going to be attenuated
[00:16:23 - 00:16:31] Remove low frequencies and remove high frequencies
[00:16:32 - 00:16:43] Okay, so we could then use this to
[00:16:45 - 00:16:46] Remove
[00:16:46 - 00:16:50] DC plus high frequency
[00:16:51 - 00:16:52] Noise
[00:16:52 - 00:17:06] Yes, sure
[00:17:06 - 00:17:07] Um
[00:17:07 - 00:17:10] Yeah, this is definitely more than one way of doing it. Yeah
[00:17:11 - 00:17:13] And
[00:17:13 - 00:17:16] Well obviously you could have the interaction with the capacitor the other way around
[00:17:17 - 00:17:22] But you could also have I think probably two in parallel and one in the series of things
[00:17:24 - 00:17:25] Yeah, sure
[00:17:30 - 00:17:32] Okay, so these cutoff frequencies
[00:17:34 - 00:17:36] fc1 and fc2
[00:17:38 - 00:17:40] that determined
[00:17:41 - 00:17:49] By the values of r, l and c. Okay, I won't publications up because they start getting a bit more complicated
[00:17:53 - 00:17:55] Okay, so what sort of filter are we missing?
[00:17:56 - 00:18:00] We've done three types. There's one common one we need to do
[00:18:03 - 00:18:05] Band stop, yep, good. So
[00:18:06 - 00:18:08] Um, here we've got a band stop filter
[00:18:08 - 00:18:15] And so this then looking at the circuit is then a mirror image of the band pass filter
[00:18:17 - 00:18:21] And so the reason we have a band stop filter here
[00:18:22 - 00:18:24] So this is our fc here
[00:18:25 - 00:18:27] And that is 50 hertz
[00:18:29 - 00:18:31] So we want to remove
[00:18:32 - 00:18:34] 50 hertz
[00:18:35 - 00:18:36] Main's
[00:18:36 - 00:18:42] Hum, we want to try and leave all the other frequencies as they were
[00:18:43 - 00:18:45] Okay, so a band stop filters
[00:18:46 - 00:18:56] Attenuate specific frequencies. This is a frequency
[00:18:57 - 00:18:59] um
[00:18:59 - 00:19:01] So here we have
[00:19:01 - 00:19:03] um
[00:19:03 - 00:19:05] The lower frequencies pass
[00:19:13 - 00:19:15] Okay, so 50 hertz is attenuated
[00:19:20 - 00:19:22] And then the high frequencies pass
[00:19:28 - 00:19:31] Okay, so one thing you have to decide if there's a kind of a trade-off as
[00:19:32 - 00:19:34] How wide do you make you notch
[00:19:34 - 00:19:38] To make sure you get rid of the 50 hertz, but you don't want to be then taking out
[00:19:39 - 00:19:41] Some of your
[00:19:41 - 00:19:43] ECG signal that you actually want to keep
[00:19:43 - 00:19:54] All your voice signal that you want to keep, etc. Okay, and again, fc is
[00:19:56 - 00:20:02] determined by your component values and r and c
[00:20:10 - 00:20:12] The size of
[00:20:15 - 00:20:17] That is something called a quality
[00:20:18 - 00:20:24] Back to you got this trade-off of basically how deep you make it and this is how wide you make it
[00:20:25 - 00:20:27] and
[00:20:27 - 00:20:31] Well, so ultimately they all depend on the component values because that's determining
[00:20:32 - 00:20:35] The 3d beat points and also how deep it goes
[00:20:36 - 00:20:38] so
[00:20:38 - 00:20:40] When you design these
[00:20:41 - 00:20:46] Filters you have to trade these things off so in my fourth year signal processing course
[00:20:47 - 00:20:52] The assignment I have is each peer gets a movie quote a different quote
[00:20:52 - 00:20:55] The Hp gets different interference frequencies
[00:20:56 - 00:20:58] And then they have to design
[00:20:59 - 00:21:03] Not filters and so you want to remove the interference frequency
[00:21:03 - 00:21:11] But you don't want to be removing too much around it so that you're not losing some of this spoken audio underneath
[00:21:11 - 00:21:22] So yeah, there's this trade-off basically how wide you make it. That's how deep you make it. Okay, so let's do a little bit of filter
[00:21:24 - 00:21:26] modeling
[00:21:26 - 00:21:28] basically how we can get the output of
[00:21:28 - 00:21:30] the filter from
[00:21:30 - 00:21:33] What we know about the filter and the input to the filter
[00:21:33 - 00:21:38] So at the time domain we've done this previously with the output
[00:21:39 - 00:21:45] Y of t is equal to the input x of t convolved with our impulse response H of t
[00:21:47 - 00:21:50] Just write these all output input
[00:21:51 - 00:21:56] Impulse response
[00:21:56 - 00:22:01] Okay, you can also write this as a convolution integral for minus infinity to infinity of
[00:22:02 - 00:22:05] h of tau x of t minus tau
[00:22:07 - 00:22:14] And think about this in the time domain is that it's hard
[00:22:16 - 00:22:18] Due to
[00:22:18 - 00:22:20] convolution
[00:22:20 - 00:22:23] Okay, you don't like going convolution
[00:22:24 - 00:22:26] Because the integral is messy
[00:22:26 - 00:22:30] The computer doesn't like to convolution because it's computationally expensive
[00:22:31 - 00:22:33] Okay, we can also write this in the
[00:22:34 - 00:22:35] Fourier domain
[00:22:36 - 00:22:39] So we have then our output capital Y of f
[00:22:39 - 00:22:48] So we've got a convolution in the time domain. So we've got a multiplication then in the frequency domain
[00:22:49 - 00:22:52] So what capital Y of f is our output spectrum
[00:22:58 - 00:23:06] x of f is our input spectrum and capital H of f is our frequency response
[00:23:06 - 00:23:20] Okay, and so this is
[00:23:22 - 00:23:24] Good for
[00:23:25 - 00:23:27] arbitrary
[00:23:27 - 00:23:40] signals avoid this convolution. Oh lastly we can do it in the Laplace domain
[00:23:42 - 00:23:45] Where we have capital Y of s
[00:23:46 - 00:23:48] So our
[00:23:48 - 00:23:52] output and the plus domain is equal to
[00:23:52 - 00:23:55] x of s the input and the Laplace domain
[00:23:58 - 00:24:02] Times h of s which is our transfer function
[00:24:09 - 00:24:11] And so the past domain is good
[00:24:11 - 00:24:15] for the transient response
[00:24:19 - 00:24:23] Okay, so a sudden change in our circuit
[00:24:52 - 00:24:56] Okay, so we look at a low-passed low-pass first order filter
[00:24:56 - 00:24:58] They're asked to filter before
[00:24:58 - 00:25:03] And so the general form of the transfer function for a low-pass filter capital H of s
[00:25:05 - 00:25:09] Is equal to k over s plus alpha
[00:25:10 - 00:25:12] So this has got a single pole at
[00:25:13 - 00:25:15] minus alpha
[00:25:17 - 00:25:21] And in our example alpha was minus 1 over rc
[00:25:24 - 00:25:26] Okay
[00:25:26 - 00:25:29] So we use the low-pass filter as kind of the example of the different
[00:25:29 - 00:25:33] frequency response transfer functions involves response response etc
[00:25:35 - 00:25:37] You could do it with a
[00:25:37 - 00:25:40] high-pass filter
[00:25:40 - 00:25:43] So that's h of s is then
[00:25:44 - 00:25:46] So different so there's a gain k
[00:25:46 - 00:25:51] There's a single zero and then there is a pole as well
[00:25:51 - 00:25:53] so we have a
[00:25:53 - 00:25:55] Pole at minus alpha
[00:25:56 - 00:26:00] Same as the low-pass filter but for the high-pass filter
[00:26:00 - 00:26:02] We have the zero at
[00:26:03 - 00:26:12] zero
[00:26:12 - 00:26:14] Okay, so we could write the general form
[00:26:15 - 00:26:17] h of s is then
[00:26:18 - 00:26:20] some gain k
[00:26:20 - 00:26:22] is
[00:26:22 - 00:26:24] plus beta over
[00:26:24 - 00:26:26] is plus alpha
[00:26:27 - 00:26:29] So this is zero
[00:26:29 - 00:26:31] At minus beta
[00:26:31 - 00:26:33] And a pole
[00:26:33 - 00:26:35] At minus alpha
[00:26:35 - 00:26:43] Okay, as we saw with
[00:26:44 - 00:26:46] the
[00:26:46 - 00:26:49] Low-pass filter got this roll-off of 20-pass
[00:26:49 - 00:26:53] This is alpha decay for a first order filter
[00:26:53 - 00:26:55] So filter with a single pole
[00:26:58 - 00:27:00] Okay, so first order filters
[00:27:01 - 00:27:03] But you can get
[00:27:03 - 00:27:06] Better rejection, better attenuation
[00:27:06 - 00:27:07] If you increase the order of the filter
[00:27:08 - 00:27:11] So let's now look at a more complicated filter
[00:27:14 - 00:27:17] Here, which is it's gonna be a second order filter
[00:27:17 - 00:27:23] We've now got both a capacitor and an inductor into our
[00:27:23 - 00:27:35] circuit in your guess is what sort of filter this is going to be before we do the maths
[00:27:35 - 00:27:43] Now the band pass filter
[00:27:50 - 00:27:53] Okay, so well, we'll do some maths and then we'll compare
[00:27:55 - 00:27:55] So
[00:27:57 - 00:27:58] Let's get our transfer function
[00:28:00 - 00:28:04] h of s is our output
[00:28:04 - 00:28:07] V o of s over our input V i of s
[00:28:14 - 00:28:16] Okay, so we have basically here a voltage divider
[00:28:19 - 00:28:20] So what do we have on the numerator?
[00:28:26 - 00:28:28] Yep, so the impedance for C, so
[00:28:28 - 00:28:31] Let's go back to step. We have in the Laplace domain
[00:28:32 - 00:28:34] This is in Laplace domain
[00:28:38 - 00:28:40] We have our impedances
[00:28:40 - 00:28:42] Then what I receive
[00:28:43 - 00:28:46] s l for the inductor
[00:28:47 - 00:28:51] So we have the impedance of the capacitor whenever we receive
[00:28:52 - 00:28:56] divided by the total impedance
[00:28:56 - 00:28:59] So this is then
[00:28:59 - 00:29:00] s l plus
[00:29:01 - 00:29:03] plus 1 over s c
[00:29:10 - 00:29:13] Okay, and then if we take this s c
[00:29:15 - 00:29:19] As the denominator of the numerator, let can just go down to the bottom
[00:29:21 - 00:29:24] We end up with then 1 over
[00:29:26 - 00:29:27] s squared lc
[00:29:29 - 00:29:46] plus i-ins are
[00:29:47 - 00:29:48] So s squared lc plus
[00:29:50 - 00:29:52] s r c plus 1
[00:30:00 - 00:30:04] So all we could write this h of s is equal to
[00:30:05 - 00:30:06] 1 over lc
[00:30:10 - 00:30:15] And then so we can write this as a quadratic on the bottom with the power
[00:30:16 - 00:30:21] So the coefficient for the highest power is squared as being 1 so s squared plus s times
[00:30:22 - 00:30:24] over l plus
[00:30:24 - 00:30:26] 1 over lc
[00:30:34 - 00:30:36] Okay, so let's then consider
[00:30:37 - 00:30:43] As s goes toward 0
[00:30:47 - 00:30:49] What happens to our
[00:30:51 - 00:30:52] magnitude of our transfer function
[00:30:54 - 00:30:58] First one, yep, so h of s is going towards 1
[00:30:58 - 00:31:02] instead of magnitude here and then as
[00:31:03 - 00:31:06] s goes to infinity what happens to our
[00:31:10 - 00:31:14] magnitude of our
[00:31:14 - 00:31:18] transfer function
[00:31:18 - 00:31:19] Zero, yep, good
[00:31:19 - 00:31:24] So what sort of
[00:31:24 - 00:31:28] filter is that going to describe low pass?
[00:31:28 - 00:31:43] Yep, so I have that in my setup
[00:31:44 - 00:31:45] Circuits previously
[00:31:46 - 00:31:49] lc and an r was a band pass
[00:31:51 - 00:31:54] Okay, so it's different to the band pass that showed previously
[00:31:56 - 00:31:57] Yeah, okay
[00:31:57 - 00:32:04] And how would we work out with a poles of our denominator?
[00:32:04 - 00:32:15] Yeah, could get a cell, but yeah, it's high school maths
[00:32:16 - 00:32:21] Full format for me last my limb. Okay, so use the quadratic equation
[00:32:30 - 00:32:36] to find poles and the poles again or then tell you where
[00:32:37 - 00:32:40] the cutoff frequency is and I'll
[00:32:40 - 00:32:43] So in this case a is 1
[00:32:44 - 00:32:46] B is r over l
[00:32:47 - 00:32:50] And c is 1 over lc
[00:32:51 - 00:32:53] As in the poles
[00:32:54 - 00:32:55] get the complicated here
[00:32:55 - 00:33:00] At s is equal to minus r over 2l
[00:33:01 - 00:33:10] plus minus r squared over 4l squared minus 1 over lc
[00:33:12 - 00:33:14] Okay, obviously you don't need to remember that
[00:33:16 - 00:33:16] But
[00:33:18 - 00:33:20] It's easy enough to work out
[00:33:20 - 00:33:22] Once you've got that transfer function
[00:33:26 - 00:33:31] That should be 4l squared but the line from the 4 disappeared after a juror
[00:33:31 - 00:33:38] I think sorry, I'll probably wrap my fork as it was horrible now
[00:34:00 - 00:34:06] Okay, so let's then have a look at the second order frequency response. Let's choose some
[00:34:07 - 00:34:09] values
[00:34:09 - 00:34:11] to one microfarad
[00:34:11 - 00:34:13] 220 ohms and
[00:34:13 - 00:34:15] 25 milliheneries
[00:34:16 - 00:34:19] So I've chosen values so that
[00:34:19 - 00:34:22] we have
[00:34:22 - 00:34:25] Then our cutoff frequency here
[00:34:26 - 00:34:28] We've got a 3d d point
[00:34:31 - 00:34:33] Is at
[00:34:33 - 00:34:35] 10 to the 3 which is a thousand
[00:34:35 - 00:34:37] or one kilohertz
[00:34:37 - 00:34:43] Okay, so I plotted this in python
[00:34:43 - 00:34:46] This is for the circuit before so this is showing it is a low pass filter
[00:34:52 - 00:34:54] Okay, and how did I come up with my
[00:34:55 - 00:34:57] values to get
[00:34:58 - 00:35:00] Nice cutoff frequency of a kilohertz
[00:35:00 - 00:35:08] Well actually I asked TPT to give me nice values of RC and L
[00:35:08 - 00:35:10] So I got a cutoff frequency of a kilohertz
[00:35:10 - 00:35:16] But the key thing is then I plotted it and python myself in verified that it was actually a kilohertz
[00:35:16 - 00:35:17] Rather than just
[00:35:17 - 00:35:19] Blindly believing
[00:35:19 - 00:35:20] An AI bot
[00:35:20 - 00:35:21] Okay, that's on the side
[00:35:22 - 00:35:27] Okay, so we cut up a cutoff frequency here of a kilohertz. What's our roll-off on this
[00:35:27 - 00:35:35] Um, filter gonna be 40 decibels per decade
[00:35:35 - 00:35:39] 40 dB per decade
[00:35:44 - 00:35:46] Okay, so not 20 here
[00:35:47 - 00:35:49] Okay, so the second order
[00:35:50 - 00:35:54] So it's two times 20 is 40 dB per decade
[00:36:10 - 00:36:15] Okay, so the second order filters have a general form which I'll show you now
[00:36:15 - 00:36:19] Um, so this is
[00:36:22 - 00:36:29] H of s is equal to omega naught squared over
[00:36:30 - 00:36:32] s squared plus
[00:36:32 - 00:36:33] two
[00:36:33 - 00:36:40] This is an eta which I'm not really good at drawing eta
[00:36:41 - 00:36:44] That's the damping factor omega naught
[00:36:44 - 00:36:47] s plus omega naught squared
[00:36:49 - 00:36:53] So omega naught which is two pi times if naught
[00:36:54 - 00:37:05] Is our resonant frequency and this thing
[00:37:08 - 00:37:09] eta
[00:37:09 - 00:37:15] Do you know what that is from your control scores or something?
[00:37:16 - 00:37:21] Yes, the damping or called the damping factor that your damping ratio
[00:37:21 - 00:37:27] We're having factor
[00:37:27 - 00:37:29] Okay, so we've got three cases then
[00:37:30 - 00:37:32] We've got our damping factor
[00:37:37 - 00:37:39] eta is less than one
[00:37:41 - 00:37:50] So that means we've got two conjugate poles and it's under damped
[00:37:53 - 00:37:56] So here we've got two poles and the left half plane
[00:38:03 - 00:38:06] If eta is exactly one
[00:38:08 - 00:38:11] We have two equal
[00:38:12 - 00:38:27] Real poles and it's critically damped and then if
[00:38:28 - 00:38:30] eta is
[00:38:30 - 00:38:32] Great one
[00:38:32 - 00:38:34] we have
[00:38:34 - 00:38:35] two
[00:38:35 - 00:38:37] distinct
[00:38:38 - 00:38:46] Real poles and that is overdamped
[00:38:54 - 00:38:57] Okay, so different classes of filters
[00:38:59 - 00:39:03] That you'll come across one of them is known as a butterworth filter
[00:39:06 - 00:39:08] But was
[00:39:09 - 00:39:12] Filter and this has a specific value for the damping factor eta
[00:39:14 - 00:39:16] Which is one over root two
[00:39:17 - 00:39:19] Or 0.707
[00:39:34 - 00:39:37] Okay, so if we consider this transfer function
[00:39:37 - 00:39:39] The second little filter of stuck on your formula sheet
[00:39:39 - 00:39:43] I'll enumerate it with got here omega naught squared
[00:39:45 - 00:39:49] If we go back to our transfer function for this
[00:39:50 - 00:39:52] Second or low pass filter we have
[00:39:53 - 00:39:56] One over LC in the numerator
[00:39:57 - 00:39:59] So that means then here
[00:40:00 - 00:40:07] Omega naught squared is 1 over LC
[00:40:07 - 00:40:13] So omega naught is equal to 1 over the square root of LC
[00:40:15 - 00:40:17] So then our
[00:40:17 - 00:40:22] Cut off a resonant frequency here if naught is 1 over 2 pi
[00:40:23 - 00:40:25] square root of LC
[00:40:56 - 00:40:58] Okay, so here I've plotted the
[00:40:58 - 00:41:05] Frequency response for a second order low pass filter
[00:41:06 - 00:41:08] The different damping factors
[00:41:10 - 00:41:14] Okay, so the blue one is the one that's critically damp
[00:41:18 - 00:41:21] And then all these ones are under damped
[00:41:27 - 00:41:29] Okay, the plot here is the normalized frequency
[00:41:31 - 00:41:37] And this is omega divided by omega naught or what the frequency divided by the root of LC
[00:41:37 - 00:41:38] And frequency if naught
[00:41:41 - 00:41:43] Okay, we see here that the slope of these things
[00:41:45 - 00:41:51] is all 40 dB per decade
[00:41:52 - 00:42:00] Okay, so there are haters all the same low frequencies and
[00:42:01 - 00:42:04] For the high frequencies just around the resonant frequency
[00:42:04 - 00:42:09] We have different behavior depending on this damping factor
[00:42:09 - 00:42:24] Okay, I've also plotted the step response
[00:42:25 - 00:42:30] For these second order filters for the same damping factors and colors as the previous slide
[00:42:33 - 00:42:36] As this should look like something you've done and controls hopefully
[00:42:38 - 00:42:45] So if we have a smaller damping factor eta
[00:42:46 - 00:42:48] We have then
[00:42:49 - 00:42:51] larger
[00:42:51 - 00:42:57] Overshoot which is generally bad. We have
[00:42:58 - 00:43:05] More ringing and our step response which is generally bad, but we have then
[00:43:06 - 00:43:08] A faster rise time or smaller delay
[00:43:17 - 00:43:18] delay
[00:43:18 - 00:43:20] took
[00:43:20 - 00:43:21] Faster rise time
[00:43:21 - 00:43:30] So we can see the effect of the different damping factors in the step response
[00:43:31 - 00:43:32] And we could also
[00:43:32 - 00:43:37] In the impulse response if we took the derivative of the step response here
[00:43:50 - 00:43:52] Okay, so let's look at
[00:43:53 - 00:43:55] Higher order filters we've done the first order
[00:43:57 - 00:44:01] Our see filter and then we did a second order filter so the first order isn't blue the second order is an orange
[00:44:03 - 00:44:05] But we can make
[00:44:07 - 00:44:10] Higher order filters so these are from the
[00:44:12 - 00:44:17] Butterworth family of filters. That was for the damping factor of one over root two
[00:44:17 - 00:44:19] And so here to
[00:44:20 - 00:44:23] In the order of the filter is determined by
[00:44:24 - 00:44:28] the highest how out of the down on my later which determines the number of poles of
[00:44:29 - 00:44:31] Our transfer function frequency response
[00:44:34 - 00:44:36] Okay, so in terms of the
[00:44:41 - 00:44:43] Roll-off of our low pass filter
[00:44:43 - 00:44:46] So we've got 20 d d d decade
[00:44:46 - 00:44:48] First order 40 d d decade
[00:44:49 - 00:45:01] The second order in 60 the third order 80 for for 100 the fifth order it sitter answer the roll-off is equal to
[00:45:01 - 00:45:05] 20 times in the order of the filter
[00:45:06 - 00:45:08] Disobels per decade
[00:45:13 - 00:45:15] Okay, but that comes at a cost
[00:45:16 - 00:45:18] We're to un
[00:45:19 - 00:45:22] A sharp roll-off of your filter. So you're rejecting
[00:45:23 - 00:45:26] The higher frequencies more quickly
[00:45:28 - 00:45:33] But we have then for a larger in
[00:45:34 - 00:45:36] So larger
[00:45:38 - 00:45:40] Order of the filter. We also get
[00:45:43 - 00:45:45] a larger delay
[00:45:45 - 00:45:47] Through the filter and
[00:45:48 - 00:45:50] More ringing in the step response
[00:46:13 - 00:46:16] So like for the step response here
[00:46:17 - 00:46:21] So the taking set of the blue curve here to get to
[00:46:22 - 00:46:29] For the step response to get to a value of one for the first time take longer than with a higher order filter
[00:46:31 - 00:46:33] The signal
[00:46:33 - 00:46:35] The signal through
[00:46:35 - 00:46:40] The filter is going to be delayed in time to the face shift is going to be greater than
[00:46:57 - 00:46:59] Okay, so
[00:46:59 - 00:47:02] Few minutes to go and just a couple more things to cover
[00:47:04 - 00:47:06] So ideally
[00:47:06 - 00:47:08] We would have an infinite order
[00:47:09 - 00:47:12] Filter and it would be what we call brick wall focus
[00:47:12 - 00:47:16] So we'd have high frequencies and then that immediately drop at the cutoff frequency
[00:47:17 - 00:47:23] So that's what's known as brick wall or ideal frequency response
[00:47:23 - 00:47:29] So here this is HFF so we're keeping
[00:47:30 - 00:47:32] frequencies in the signal
[00:47:33 - 00:47:33] less than B
[00:47:35 - 00:47:36] and then
[00:47:36 - 00:47:38] frequency is greater than B
[00:47:40 - 00:47:42] Perfectly attenuated
[00:47:43 - 00:47:46] So we can write this brick wall filter then
[00:47:47 - 00:47:51] HFF is equal to
[00:47:52 - 00:47:58] Rectangle function so rectave F and this has
[00:48:00 - 00:48:04] What's here of to the
[00:48:12 - 00:48:18] Okay, so as we saw before the impulse response is the inverse Fourier transform of the frequency response so
[00:48:19 - 00:48:23] H of t is equal to the inverse Fourier transform
[00:48:24 - 00:48:30] Of the frequency response H of F and so then
[00:48:33 - 00:48:39] Rict and
[00:48:39 - 00:48:40] Sink are a Fourier
[00:48:40 - 00:48:46] Here so if we've got rict and the frequency domain we have then
[00:48:47 - 00:48:49] Sink function
[00:48:49 - 00:48:51] And the time domain
[00:48:53 - 00:48:55] So this is the impulse response here H of t
[00:48:56 - 00:48:58] This is Sink then
[00:48:59 - 00:49:05] We need to make use of the scaling property of the Fourier transform so we've got a 2B on the denominator
[00:49:06 - 00:49:08] So we have a times by 2B
[00:49:09 - 00:49:11] In the time domain and the numerator
[00:49:12 - 00:49:21] So we've got that inverse relationship between the two domains and then we also have a scalar here 2B comes out the front from this 2B in the denominator
[00:49:26 - 00:49:27] Okay, so
[00:49:28 - 00:49:31] Well, we can't actually build a brick wall filter out of
[00:49:31 - 00:49:34] Resistance capacitors and inductors
[00:49:36 - 00:49:56] Because we have here now impulse response H of t is greater than well. It's not equal to zero for t less than zero
[00:50:00 - 00:50:02] Okay, so that means the filter is
[00:50:03 - 00:50:07] Non-core-zole and we can't actually build a perfect brick wall filter
[00:50:09 - 00:50:11] Out of analog components
[00:50:12 - 00:50:17] Okay, so we'll finish there because kensu I think it was short by one slide today
[00:50:17 - 00:50:19] I've had a lot of filters and they more
[00:50:19 - 00:50:21] start with digital on
[00:50:21 - 00:50:46] Wednesday
[00:51:24 - 00:51:26] I already mentioned that

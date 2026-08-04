# ENMT301-26W Lecture 39 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `a174c5279b634fb32b578878cbbf64297f6b41928a5e2bddbdc03dda72dc2d34`
Generated: 2026-06-06T06:31:06.664983+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:06 - 00:00:09] Okay, good afternoon everyone.
[00:00:09 - 00:00:10] Thanks for coming along.
[00:00:10 - 00:00:14] So just do a bit of a recap of the noise types
[00:00:14 - 00:00:17] we've looked at yesterday.
[00:00:17 - 00:00:21] So, thermal noise to be getting the resistor.
[00:00:21 - 00:00:27] And this is from the charge carriers, the electrons.
[00:00:27 - 00:00:32] Just bouncing up and down with temperature.
[00:00:32 - 00:00:36] And so this is unavoidable.
[00:00:36 - 00:00:38] You have a resistor or any resistance in your circuit.
[00:00:38 - 00:00:40] You will get some thermal noise.
[00:00:40 - 00:00:42] And so the way we model that thermal noise
[00:00:42 - 00:00:50] is as a focus source in series with our resistor.
[00:00:50 - 00:00:54] And so the thermal noise is a function of the temperature.
[00:00:54 - 00:00:58] So high temperature, you get more of this agitation
[00:00:58 - 00:00:59] of the charge carriers.
[00:00:59 - 00:01:02] So you get a large noise of the resistance.
[00:01:02 - 00:01:08] And also the bandwidth over which you are taking your measurement.
[00:01:08 - 00:01:10] So thermal noise has a white noise spectrum.
[00:01:10 - 00:01:18] So if you look at large bandwidth, you'll see more noise.
[00:01:18 - 00:01:22] Okay, so this is a sample of a thermal noise case.
[00:01:22 - 00:01:25] And if we take a filter by here averaging over 200 samples,
[00:01:25 - 00:01:32] then it's pretty close to 0.
[00:01:32 - 00:01:33] Okay, so it's white noise.
[00:01:33 - 00:01:40] So the spectrum here, the amplitude spectral density.
[00:01:40 - 00:01:41] So it's probably gets frequency.
[00:01:41 - 00:01:44] So for white noise, it's flat.
[00:01:44 - 00:01:49] So it has the same value for all frequencies.
[00:01:49 - 00:01:54] Okay, and then the second noise pipe we looked at was shot noise.
[00:01:54 - 00:02:00] Where this occurs in semiconductors, the diode transistors,
[00:02:00 - 00:02:06] et cetera, where some of the electrons might swim against the current.
[00:02:06 - 00:02:11] And then we have an equation for that shot noise as well.
[00:02:11 - 00:02:15] And so it's a function of the charge of our charge carriers.
[00:02:15 - 00:02:18] And then the amount of current that is flowing,
[00:02:18 - 00:02:23] as well as the measurement bandwidth.
[00:02:23 - 00:02:27] Okay, so we can do a little example now with this shot noise.
[00:02:29 - 00:02:33] Using this equation for what the R and S shot noise current.
[00:02:34 - 00:02:39] So the example here we've got a current 100 milliamps.
[00:02:39 - 00:02:43] And we're going to measure a signal over one kilohertz.
[00:02:43 - 00:02:45] So it's our frequency range.
[00:02:46 - 00:02:53] And so then we'll use i subscript in for this noise current
[00:02:54 - 00:02:59] is then equal to the square root of two times the charge q times our bandwidth
[00:03:02 - 00:03:07] B times the current flowing i.
[00:03:09 - 00:03:14] As in this gives us five in substitute the numbers.
[00:03:14 - 00:03:19] Two charge is 1.6 times 10 to the minus 19.
[00:03:21 - 00:03:25] We have our bandwidth is one times 10 to the three.
[00:03:25 - 00:03:31] And our DC current here is 100 milliamps.
[00:03:31 - 00:03:37] That's 100 times 10 to the minus three.
[00:03:37 - 00:03:41] And so then our R and S shot noise current
[00:03:43 - 00:03:48] is when we plug all these numbers at 5.7 nano amps.
[00:03:49 - 00:03:52] And that's an R and S value.
[00:03:52 - 00:03:59] It would mean square.
[00:03:59 - 00:04:05] Okay, so that's a small number there for the shot noise.
[00:04:05 - 00:04:06] But it's proportional.
[00:04:06 - 00:04:10] But it is a function of the square root of the current.
[00:04:10 - 00:04:12] So our current flowing is going up.
[00:04:12 - 00:04:18] Then our shot noise is also going to increase.
[00:04:18 - 00:04:23] Okay, and then the third noise type we're going to look at is known as flicker
[00:04:23 - 00:04:26] noise.
[00:04:26 - 00:04:29] And so that noise is not that well understood.
[00:04:29 - 00:04:32] Accers and semiconductors, semiconductors.
[00:04:33 - 00:04:37] So normally silicon and it's doped with other materials to make them in
[00:04:37 - 00:04:41] and p type diodes and transistors.
[00:04:41 - 00:04:47] And sometimes the doping of the semiconductors will have defects in it.
[00:04:47 - 00:04:51] And so then when the charges flow through the semiconductors,
[00:04:51 - 00:04:55] sometimes it just gets trapped so we don't get kind of a uniform flow
[00:04:55 - 00:04:58] that we would expect.
[00:04:58 - 00:05:08] And so then unlike our shot noise and our film noise,
[00:05:08 - 00:05:12] which cases of white noise, so they have no frequency
[00:05:12 - 00:05:18] dependence, this flicker noise has a one over F frequency dependence.
[00:05:19 - 00:05:23] Okay, so that means this noise mostly happens at lower frequencies.
[00:05:23 - 00:05:30] Okay, so should write on here as well.
[00:05:30 - 00:05:35] The shot noise is white noise.
[00:05:35 - 00:05:50] And then the last point about the flicker noise is one over F frequency
[00:05:50 - 00:05:52] means it is not as pic noise.
[00:05:52 - 00:05:57] So most of the noise is low frequencies.
[00:05:57 - 00:05:59] And because it's low frequencies,
[00:05:59 - 00:06:05] unlike that thermal noise case where it was very high frequency taking an average mint,
[00:06:05 - 00:06:07] we can remove it.
[00:06:07 - 00:06:12] Here the flicker noise because as much lower frequencies, the changes are much slower.
[00:06:12 - 00:06:19] Then we do see a wandering about of our signal.
[00:06:19 - 00:06:26] So it's harder to then measure our low frequencies and our direct current DC values
[00:06:26 - 00:06:27] to the offset.
[00:06:27 - 00:06:32] So the DC here is the offset.
[00:06:32 - 00:06:38] So I'll show an example of what I mean on the next slide hopefully.
[00:06:38 - 00:06:43] Okay, so this is a case of flicker noise and blue.
[00:06:43 - 00:06:51] Okay, so this in this case we have a lower frequency as well as some high frequencies.
[00:06:51 - 00:06:56] And then the orange is the moving average.
[00:06:56 - 00:07:08] Okay, so in this case here, our moving average in orange is not zero.
[00:07:08 - 00:07:16] Okay, so the thermal noise we could filter out by taking a moving average by averaging over a certain number of samples.
[00:07:16 - 00:07:24] Here if we average several hundred samples like we did with the thermal noise,
[00:07:24 - 00:07:31] we don't get our average to be zero because this flicker noise has a much slower,
[00:07:31 - 00:07:36] lower frequency variation.
[00:07:36 - 00:07:42] So our constant offset DC is then wandering around.
[00:07:42 - 00:07:55] It's not zero like in the thermal noise case.
[00:07:55 - 00:07:59] Okay, I'm a slow pull and I said there's last half noise.
[00:07:59 - 00:08:04] We've also got something going to this opamp noise.
[00:08:04 - 00:08:10] And so if we consider what happens with an opamp noise,
[00:08:10 - 00:08:14] here we've got the right, we've got an ideal opamp.
[00:08:14 - 00:08:16] So that means no noise.
[00:08:16 - 00:08:27] And in the real world for an opamp, we have then noise and
[00:08:27 - 00:08:37] that noise is modeled as a random voltage source like we had with our thermal noise.
[00:08:37 - 00:08:57] And then also two current sources, one to the positive channel of the ideal opamp and one to the negative channel.
[00:08:57 - 00:09:04] Okay, so the real opamp, we'll do a different color here.
[00:09:04 - 00:09:16] So real opamp is then everything inside here.
[00:09:16 - 00:09:27] Okay, so the opamp is generating noise.
[00:09:27 - 00:09:37] And then model that noise as a voltage source and two current sources.
[00:09:37 - 00:09:48] Yes.
[00:09:48 - 00:09:53] Notice that those will then be amplified to the output.
[00:09:53 - 00:10:17] Okay, so if we look here with got the noise amplitude spectral density
[00:10:17 - 00:10:22] for a particular type of instrumentation amplifier.
[00:10:22 - 00:10:29] So AV 4821, one of these chips up at the top.
[00:10:29 - 00:10:40] And so the noise amplitude spectral density for this amplifier is shown in blue.
[00:10:40 - 00:10:53] And so this noise spectral density for the amplifier has two different sort of frequency regimes.
[00:10:53 - 00:10:59] Okay, so higher frequencies here.
[00:10:59 - 00:11:04] Well, sort of noise do we have for above 1000 Hertz?
[00:11:04 - 00:11:08] White noise, yep.
[00:11:08 - 00:11:11] White noise.
[00:11:11 - 00:11:18] And so this is white noise because it's constant frequency.
[00:11:18 - 00:11:54] And again, okay, and so the noise types we looked at that had a constant noise spectrum within shot noise and thermal noise.
[00:11:54 - 00:12:10] Okay, and so then a lot of frequencies are less than kilo Hertz.
[00:12:10 - 00:12:14] What sort of noise is that?
[00:12:14 - 00:12:16] What color noise?
[00:12:16 - 00:12:17] Pink, I heard a pink.
[00:12:17 - 00:12:19] Well, I thought it was smooth.
[00:12:19 - 00:12:20] Okay, so this is quick noise.
[00:12:20 - 00:12:28] So this is dominating at low frequencies.
[00:12:28 - 00:12:53] Okay, so this is dominates frequencies.
[00:12:53 - 00:13:02] Okay, and then the example we looked at for this noise type was then this flicker noise.
[00:13:02 - 00:13:24] Okay, and then if we had noise that was increasing with frequency, then that's known as then blue noise.
[00:13:24 - 00:13:27] So I won't draw that on the flicker because it might get confusing.
[00:13:27 - 00:13:41] Yeah.
[00:13:41 - 00:13:53] Well, I guess it's kind of the me of the curve here is actually about, that's about 5 Hertz.
[00:13:53 - 00:13:56] I guess they're kind of.
[00:13:56 - 00:14:00] So it's really flat from 100 Hertz on.
[00:14:00 - 00:14:06] And here you can see both contributions between about 0.1 and 100.
[00:14:06 - 00:14:10] Yeah, yeah, yeah, yeah.
[00:14:10 - 00:14:23] Yeah, but basically when it's diverging from those orange lines, then you've got contributions from both.
[00:14:23 - 00:14:27] Okay, so, the next thing is we have a circuit.
[00:14:27 - 00:14:31] We'll have more than one resistor in our circuit.
[00:14:31 - 00:14:37] So how do we then deal with our noise sources?
[00:14:37 - 00:14:40] Say it was just that produces some thermal noise.
[00:14:40 - 00:14:45] How do we get the total noise in our circuit?
[00:14:45 - 00:14:48] Okay, so, there's one up here.
[00:14:48 - 00:15:00] We've got a resistor one that's modeled as an ideal resistor and a voltage source with some random noise.
[00:15:00 - 00:15:06] And R2 is modeled as an ideal resistor with another voltage source.
[00:15:06 - 00:15:14] Okay, so then to get the total noise voltage at time t,
[00:15:14 - 00:15:19] we need to sum up the random variables from each resistor.
[00:15:19 - 00:15:25] So this is then, let's write forwards, a V of t, in this case,
[00:15:25 - 00:15:35] is then V1 of t plus V2 of t.
[00:15:35 - 00:15:47] Okay, so these here, V1 of t and V2 of t, these are random variables.
[00:15:47 - 00:15:52] Okay, so the random variables are given capital letters here,
[00:15:52 - 00:15:58] where I'm not as doing little V for a voltage source.
[00:15:58 - 00:16:05] Okay, so then we want to work out now.
[00:16:05 - 00:16:09] How do we add these two random variables together?
[00:16:09 - 00:16:19] Okay, so we've got, so if we want to work out what the mean is.
[00:16:19 - 00:16:30] So we want to work out what does our mean or expected value of the total random variable V of t?
[00:16:30 - 00:16:41] This is then the expected value of V1 of t plus V2 of t,
[00:16:41 - 00:17:01] which can be then written, expand that out to be the expected value of V1 of t plus the expected value of V2 of t.
[00:17:01 - 00:17:06] Okay, so for our resistors, for thermal noise,
[00:17:06 - 00:17:14] what's the mean value of our voltage for our two,
[00:17:14 - 00:17:19] the mean value of our thermal noise for two resistors in series?
[00:17:19 - 00:17:36] Okay, so what was the mean value for the thermal noise of one resistor yesterday?
[00:17:36 - 00:17:41] Well, that's, so that was the barrier.
[00:17:41 - 00:17:47] So that's the final graph, everything's always better with the picture.
[00:17:47 - 00:17:53] Okay, so this is our thermal noise realization for one resistor.
[00:17:53 - 00:17:57] So what's the mean value for that going to be zero?
[00:17:57 - 00:18:00] Yeah, zero. So if we have two resistors in series,
[00:18:00 - 00:18:05] what's our mean noise, mean total noise going to be zero?
[00:18:05 - 00:18:10] Yeah, back to the slide somewhere.
[00:18:10 - 00:18:15] Yeah, okay, so this one, this first term, this is zero mean.
[00:18:15 - 00:18:20] You can see that from the figure. And this one was zero mean.
[00:18:20 - 00:18:26] So it means the total thermal noise,
[00:18:26 - 00:18:33] no matter how many resistors we have in our circuit is going to be zero mean.
[00:18:33 - 00:18:36] So we're not going to be adding any DC offset,
[00:18:36 - 00:18:39] I'll pull down, like with that second flicker noise.
[00:18:39 - 00:18:43] Okay, so the mean's going to be zero.
[00:18:43 - 00:18:50] But then what we do about our variance,
[00:18:50 - 00:18:55] like I saw the variance of our random variable V of T
[00:18:55 - 00:19:02] depends on the correlation between V1 of T and V2 of T.
[00:19:02 - 00:19:11] And so in this case, we've got two resistors in series that independent
[00:19:11 - 00:19:18] and correlated. So we can simply get the variance of our random variable V.
[00:19:18 - 00:19:21] So sigma squared is our variance.
[00:19:21 - 00:19:28] And then we can add the variance of the zero noise of the first resistor
[00:19:28 - 00:19:33] to the variance of the zero noise of the second resistor
[00:19:33 - 00:19:50] to get the total noise variance.
[00:19:50 - 00:19:56] And so this variance was the 4k Tb that we had.
[00:19:56 - 00:19:59] So you would calculate the variance of one resistor,
[00:19:59 - 00:20:01] depending on its resistive value,
[00:20:01 - 00:20:06] add it to the variance for the second resistor to be honest.
[00:20:06 - 00:20:14] Our value, and then you can take the square root of that to get the RMS total noise variance.
[00:20:14 - 00:20:16] So RMS total noise.
[00:20:16 - 00:20:26] Okay, so that is the end of noise.
[00:20:26 - 00:20:32] And so it will finish with, it's going to be that interference.
[00:20:32 - 00:20:38] And so we'll look for different examples of interference in a circuit,
[00:20:38 - 00:20:40] how they can arise. Yes.
[00:20:40 - 00:20:48] Yeah.
[00:20:48 - 00:20:54] Well, no, I mean the instances is like the cost of variance.
[00:20:54 - 00:20:58] If they're not independent, if you make a change in one,
[00:20:58 - 00:21:00] then it changes the other one.
[00:21:00 - 00:21:07] But in terms of our noise sources,
[00:21:07 - 00:21:10] there should be independent here.
[00:21:10 - 00:21:24] Okay, so we'll be looking at some different types of interference.
[00:21:24 - 00:21:30] So there's a bit of an overlap essentially between interference and noise.
[00:21:30 - 00:21:34] So these are both things that we don't want to now circuit.
[00:21:34 - 00:21:38] Okay, so if we're measuring my heartbeat,
[00:21:38 - 00:21:40] we just want my heartbeat.
[00:21:40 - 00:21:42] We don't want any of this.
[00:21:42 - 00:21:45] There will noise looking noise from the electronics.
[00:21:45 - 00:21:51] We also don't want any interference from me picking up to be hurt.
[00:21:51 - 00:21:54] Why is the wall?
[00:21:54 - 00:22:00] So the difference between the two is that the noise is random.
[00:22:00 - 00:22:03] So if you look at those realization plots,
[00:22:03 - 00:22:05] say, of thermal noise at the second noise,
[00:22:05 - 00:22:09] as we're bouncing up and down, we can't predict it in any way.
[00:22:09 - 00:22:14] But interference is deterministic or almost deterministic.
[00:22:14 - 00:22:17] And then we can write an equation for it.
[00:22:17 - 00:22:23] So I'll use that as my definition for deterministic.
[00:22:23 - 00:22:30] So we can write equation 4.
[00:22:30 - 00:22:40] So if the interference is a 50-girt sine wave coming out of the mainscable that I'm close to,
[00:22:40 - 00:22:46] I can write an equation for that as a cosine 50-girt sine.
[00:22:46 - 00:22:53] Where is the thermal noise from the resistor is just this random thing,
[00:22:53 - 00:22:56] and I can't write an equation for it.
[00:22:56 - 00:23:01] But at the end of the day, we want to employ filters to remove the noise and interference.
[00:23:01 - 00:23:05] So if it fixes the same, it's reducing the quality of our signal.
[00:23:05 - 00:23:17] Okay, so let's say we have a circuit.
[00:23:17 - 00:23:26] So times all sinter and then we'll have some amplifier to amplify the voltage out of that sensor,
[00:23:26 - 00:23:34] before we put it into, or through an ADC into a microcontroller to analyze that signal,
[00:23:34 - 00:23:43] that circuit of interest, our sensor, the amplifier might pick up interference from another circuit.
[00:23:43 - 00:23:46] So the circuit of interest, our sensor plus amplifier,
[00:23:46 - 00:23:50] we'll call our victim circuit,
[00:23:50 - 00:24:00] and then the other circuit that we're picking up this interference from will call the aggressor circuit.
[00:24:00 - 00:24:05] Okay, then there are three main types of electrical interference,
[00:24:05 - 00:24:12] and these are right to the three main electrical properties that we've got conductive interference.
[00:24:12 - 00:24:17] So this relates to resistance, capacitive interference,
[00:24:17 - 00:24:24] and the elastic capacitance C, and inductive coupling relates to inductance L.
[00:24:24 - 00:24:28] So the capacitive coupling relates to electric fields,
[00:24:28 - 00:24:34] and the inductive coupling to magnetic fields.
[00:24:34 - 00:24:37] As then the most common interference we have,
[00:24:37 - 00:24:41] then it's coming from the main voltage supply.
[00:24:41 - 00:24:48] So 50 Hertz in New Zealand, but it does change the country and country.
[00:24:48 - 00:24:58] So the U.S. is 60 Hertz, as well as being a lower voltage.
[00:24:58 - 00:25:05] Okay, so let's look at conductive interference first.
[00:25:05 - 00:25:10] Okay, so first of all, I'll explain this diagram a little bit.
[00:25:10 - 00:25:29] So we have the dotted lines are for our aggressor circuit.
[00:25:29 - 00:25:32] Okay, so that's not the circuit we're interested in.
[00:25:32 - 00:25:36] The circuit we're interested in is our sensor plus amplifier.
[00:25:36 - 00:25:42] So this A here is our amplifier.
[00:25:42 - 00:25:47] Okay, but let's say we have our amplifier circuit.
[00:25:47 - 00:25:51] She is a common ground with some other circuit.
[00:25:51 - 00:25:54] This is a aggressive circuit, which is a voltage source.
[00:25:54 - 00:26:02] So VA is our voltage source, and it's connected some,
[00:26:02 - 00:26:08] like, a load, let's call this, for example, some sort of motor.
[00:26:08 - 00:26:10] Okay.
[00:26:10 - 00:26:12] So you think you've got two different circuits.
[00:26:12 - 00:26:16] They should be independent lines of sensor with an amplifier,
[00:26:16 - 00:26:23] and there's a voltage supply going to a motor.
[00:26:23 - 00:26:28] Okay, but a shear this common ground.
[00:26:28 - 00:26:34] Okay, so in general this conductive coupling comes from shearing wires.
[00:26:34 - 00:26:39] Okay, and so these wires have resistance.
[00:26:39 - 00:26:53] So there will be some resistance along the circuit.
[00:26:53 - 00:27:10] Okay, so the part that the amplifier circuit shears with our motor,
[00:27:10 - 00:27:15] aggressive circuit has a resistance of RC.
[00:27:15 - 00:27:20] Okay, so RC here is the sheared resistance.
[00:27:20 - 00:27:41] Okay, so we've got some current flowing in our aggressive circuit,
[00:27:41 - 00:27:44] given by I A here.
[00:27:44 - 00:27:49] So this is the aggressive current.
[00:27:49 - 00:28:03] Okay, so our interference voltage, the IFT,
[00:28:03 - 00:28:09] I front interference, is then equal to,
[00:28:09 - 00:28:12] so we've got this current flowing through here.
[00:28:12 - 00:28:24] So IFT here, so then the interference voltage for the IFT is,
[00:28:24 - 00:28:28] we'll use negative as an voltage drop,
[00:28:28 - 00:28:33] IFT times our sheared resistance R C.
[00:28:33 - 00:28:37] So it's just Ome's law with the current flowing through the circuit,
[00:28:37 - 00:28:41] and our amount of sheared resistance.
[00:28:41 - 00:28:56] Okay, so we've got some voltage from the sensor,
[00:28:56 - 00:28:59] let's call this V S. This is our sensor voltage,
[00:28:59 - 00:29:08] and then the input to our amplifier V input,
[00:29:08 - 00:29:19] which should be just our sensor voltage,
[00:29:19 - 00:29:22] but actually, because of this interference,
[00:29:22 - 00:29:35] we have to subtract that interference voltage.
[00:29:35 - 00:29:38] Okay, so we are not,
[00:29:38 - 00:29:42] we don't have the right voltage, the correct voltage to our amplifier,
[00:29:42 - 00:29:51] we're losing a bit of voltage because of this sheared resistance through the ground plane.
[00:29:51 - 00:29:59] Okay, so how, what's a way that we can try and reduce this conductive coupling?
[00:29:59 - 00:30:07] How can we reduce this interference voltage?
[00:30:07 - 00:30:10] Yeah, exactly. So what am I doing that?
[00:30:10 - 00:30:27] Well, you can have two separate circuits, or you can try and reduce the amount of common wire between the two.
[00:30:27 - 00:30:31] Okay, so right at the top,
[00:30:31 - 00:30:40] so we can minimize by reducing the length.
[00:30:40 - 00:31:20] Okay, and there might be something you need to be mindful of when you wire up your robots
[00:31:20 - 00:31:33] for the row workout, is that you don't have large sheared wires between,
[00:31:33 - 00:31:42] your power supply, and the sensor or a large ground,
[00:31:42 - 00:31:50] where you can introduce this conductive coupling.
[00:31:50 - 00:31:57] Okay, the next one we just look at is capacitive coupling,
[00:31:57 - 00:32:07] and so this is one that arises frequently from the mains.
[00:32:07 - 00:32:10] Okay, so we've got here, again, we've got our sensor circuit,
[00:32:10 - 00:32:20] so we've got some amplifier here, and we've got,
[00:32:20 - 00:32:25] whether or not is parasitic capacitors.
[00:32:25 - 00:32:34] So there's parasitic capacitance arises between any two conductors.
[00:32:34 - 00:32:42] Okay, so I, as we all are, we're mostly water,
[00:32:42 - 00:32:46] that conducts a little bit, so there's going to be some capacitance between me,
[00:32:46 - 00:32:51] and the voltage flowing through that wire.
[00:32:51 - 00:32:58] Okay, so any two conductors are going to produce a parasitic capacitance between them.
[00:32:58 - 00:33:02] So if we consider here our aggressive circuit,
[00:33:02 - 00:33:11] so the dotted lines aggressive circuit,
[00:33:11 - 00:33:19] and for example, that could be the mains voltage in the wall.
[00:33:19 - 00:33:33] Okay, so from our aggressive voltage supply,
[00:33:33 - 00:33:46] here we don't even shear ground playing with our sensor circuits,
[00:33:46 - 00:33:54] but there's going to be some capacitance between this wire in our voltage supply circuits.
[00:33:54 - 00:33:57] This is going off probably to some motor or something,
[00:33:57 - 00:34:00] and the wire here in our sensor circuit.
[00:34:00 - 00:34:05] Okay, and same between the ground level of our sensor circuit,
[00:34:05 - 00:34:09] and the ground level of our voltage supply circuit.
[00:34:09 - 00:34:13] Two conductors, there will be some capacitance,
[00:34:13 - 00:34:16] there will be an air capacitor, we don't have any dielectric between them,
[00:34:16 - 00:34:20] but it will be some capacitance between the two of them.
[00:34:20 - 00:34:30] Okay, so let's just do a bit of circuit analysis here.
[00:34:30 - 00:34:37] So the governing equation, which you'd have seen in the last year for capacitance,
[00:34:37 - 00:34:43] is the current is equal to the capacitance times the rate of change of the voltage,
[00:34:43 - 00:34:58] which is a function of time, was respected time.
[00:34:58 - 00:35:01] Okay, and so then the sensor in reality,
[00:35:01 - 00:35:03] what I'll just sort of cross this out here,
[00:35:03 - 00:35:12] is actually going to be some sort of voltage in series with a resistive.
[00:35:12 - 00:35:16] A resistance, so we'll call this RS and Vs,
[00:35:16 - 00:35:22] for the resistance of our sensor is and of our voltage supply,
[00:35:22 - 00:35:28] sorry about the voltage of our sensor Vs.
[00:35:28 - 00:35:33] Okay, and we've got some current here, I have T,
[00:35:33 - 00:35:41] and then the voltage across the amplifier here,
[00:35:41 - 00:35:44] it's the fine plus minus there.
[00:35:44 - 00:35:52] Okay, so we've got here, then effectively two capacitors in series.
[00:35:52 - 00:36:03] So then the total capacitance series, total capacitance,
[00:36:03 - 00:36:10] which you've seen last year, probably the first year as well.
[00:36:10 - 00:36:17] So the one over the total capacitance C is equal to 1 over C1 plus 1,
[00:36:17 - 00:36:19] or the C2.
[00:36:19 - 00:36:25] So capacitors in series add light resistance, do in parallel.
[00:36:25 - 00:36:36] And so then the total capacitance C is equal to C1 times C2 plus over C1 plus C2.
[00:36:36 - 00:36:49] Okay, and then I'll carry on the next slide.
[00:36:49 - 00:36:58] So what we're going to try and do here is work out
[00:36:58 - 00:37:04] the interference voltage from this capacitance.
[00:37:04 - 00:37:12] So if we take this equation for the governing equation for a capacitor,
[00:37:12 - 00:37:19] the current, it's equal to the capacitance times the range of voltage with respect to time,
[00:37:19 - 00:37:22] we can get an equation for our current.
[00:37:22 - 00:37:29] So we'll do it then I have T, so this current here,
[00:37:29 - 00:37:32] is equal to C, which is our total capacitance,
[00:37:32 - 00:37:45] which is from the two parasitic capacitors in series.
[00:37:45 - 00:37:50] And then we want to do the ready change,
[00:37:50 - 00:37:54] so the derivative of the voltage,
[00:37:54 - 00:37:57] which is this aggressive voltage, so the voltage supply,
[00:37:57 - 00:38:10] and the other circuit, the function of time with respect to time T.
[00:38:10 - 00:38:13] Okay, so then out, interference voltage,
[00:38:13 - 00:38:23] the I of T is our interference interference voltage.
[00:38:23 - 00:38:33] This is equal to the current I of T times our impedance Z,
[00:38:39 - 00:38:43] and so our impedance here,
[00:38:43 - 00:38:46] let's just go back to the previous slide,
[00:38:46 - 00:38:49] our sensor has an impedance of RS.
[00:38:49 - 00:38:58] So then we end up with our equation for our interference due to the capacitive coupling.
[00:38:58 - 00:39:10] So the voltage is then equal to the value of our capacitance times the resistance of our sensor,
[00:39:10 - 00:39:17] times the derivative of our aggressive voltage with respect to time T.
[00:39:17 - 00:39:27] So that is the equation I could be in the formula,
[00:39:27 - 00:39:29] and I looked at the formula sheet yet.
[00:39:29 - 00:39:35] Now, good, well not good, but you can look at it on Thursday when we've got a tutorial.
[00:39:35 - 00:39:44] So I'll pop some tutorial questions up on the sub zone.
[00:39:44 - 00:39:47] Okay, so our interference voltage,
[00:39:47 - 00:39:52] which we don't want, we're introducing into our circuit because of,
[00:39:52 - 00:39:56] say, our main power supply,
[00:39:56 - 00:40:01] this is then proportional to our capacitance.
[00:40:01 - 00:40:04] Okay, so the larger the value of our power,
[00:40:04 - 00:40:09] the larger the value of the C,
[00:40:09 - 00:40:12] and it's also proportional to our sensor resistance.
[00:40:12 - 00:40:23] Okay, and it's also proportional to the rate of change of voltage with respect to time.
[00:40:23 - 00:40:29] So that means if the voltage supply here is changing quickly,
[00:40:29 - 00:40:32] so we've got a high frequency voltage supply,
[00:40:32 - 00:40:35] we'll have a larger interference.
[00:40:35 - 00:40:46] Okay, so how can we reduce our interference voltage?
[00:40:46 - 00:40:52] How can we reduce our capacitive coupling?
[00:40:52 - 00:40:53] Any ideas?
[00:40:53 - 00:41:04] I could move further away from the aggressive circuit,
[00:41:04 - 00:41:06] which is the voltage in here,
[00:41:06 - 00:41:08] although it's probably wise in that one as well.
[00:41:08 - 00:41:10] Okay, so we can try and separate things physically.
[00:41:10 - 00:41:18] That's not always possible due to the space constraints and the device you're measuring.
[00:41:18 - 00:41:21] Okay, so that's point number two there.
[00:41:21 - 00:41:24] We could move some further away.
[00:41:24 - 00:41:30] But there are other things we can do to reduce our capacitive coupling.
[00:41:30 - 00:41:36] And we'll look at those now so we can use shielding.
[00:41:36 - 00:41:38] Oh, actually, just go back and slide here.
[00:41:38 - 00:41:42] So for moving the sensor further away,
[00:41:42 - 00:41:44] you probably, in first year physics,
[00:41:44 - 00:41:51] would have seen that the capacitance of a parallel plate capacitor is given by the permittivity
[00:41:51 - 00:41:56] times the area over the distance between the conductance D.
[00:41:56 - 00:41:59] That's why if you move them further away,
[00:41:59 - 00:42:03] if you increase D, your capacitance C goes down.
[00:42:03 - 00:42:18] So here D is distance.
[00:42:18 - 00:42:27] Okay, so that little let's then look at how we can reduce our capacitive coupling.
[00:42:27 - 00:42:32] So we can put shielding around our wires.
[00:42:32 - 00:42:37] And so what shielding does is it stops the electric field lines.
[00:42:37 - 00:42:43] But then also our shield must be grounded.
[00:42:43 - 00:42:50] Okay, so the shielding,
[00:42:50 - 00:43:07] the capacitors have this electric field.
[00:43:07 - 00:43:11] And if we shield it to stop the electric field,
[00:43:11 - 00:43:15] we can reduce the capacitive coupling.
[00:43:15 - 00:43:24] Okay, so let's look at an example of a type of shield here.
[00:43:24 - 00:43:28] So a coaxial cable.
[00:43:28 - 00:43:34] So that's kind of like the type of cable you connect your TV up to the antenna.
[00:43:34 - 00:43:37] So they use for carrying TV and audio signals.
[00:43:37 - 00:43:47] They have a structure shown in this figure here.
[00:43:47 - 00:43:53] So the current flows through the central conductor.
[00:43:53 - 00:43:58] And we have an insulator on the outside of the cables.
[00:43:58 - 00:44:00] That's like any black cable.
[00:44:00 - 00:44:02] We've got an insulator.
[00:44:02 - 00:44:08] And then we have some shielding.
[00:44:08 - 00:44:12] So there are two claps of shield here.
[00:44:12 - 00:44:16] So this foil shield, the solid shield.
[00:44:16 - 00:44:28] This is the one that stops the electric field lines.
[00:44:28 - 00:44:36] That is word electric field.
[00:44:36 - 00:44:45] And so that is what gives us reduces the capacitive coupling.
[00:44:45 - 00:45:00] And we've also got this braided shield.
[00:45:00 - 00:45:04] So you can see it's not entirely solid.
[00:45:04 - 00:45:08] It's got braids.
[00:45:08 - 00:45:41] And this is good for grounding.
[00:45:41 - 00:45:46] Okay, so we'll finish today probably with an example of capacitive coupling.
[00:45:46 - 00:45:51] And it's going to be for you.
[00:45:51 - 00:45:53] Which is actually...
[00:45:53 - 00:45:55] You know who this is?
[00:45:55 - 00:45:57] Okay.
[00:45:57 - 00:46:00] This is the yellow gauge away.
[00:46:00 - 00:46:03] So say we have...
[00:46:03 - 00:46:04] We're in New Zealand.
[00:46:04 - 00:46:10] We've got 240 volts RMS as our voltage supply.
[00:46:10 - 00:46:17] And so this is some other circuit, which is doing something else.
[00:46:17 - 00:46:21] You know, it might be the lights in the room.
[00:46:21 - 00:46:29] We have then some then capacitive or parasitic capacitors,
[00:46:29 - 00:46:42] or the dotted lines between the voltage supply going through the ceiling.
[00:46:42 - 00:46:58] Say, and you're here in your arms.
[00:46:58 - 00:47:05] This is our parasitic capacitor.
[00:47:05 - 00:47:15] Okay, we're also going to have some parasitic capacitance
[00:47:15 - 00:47:31] to...
[00:47:31 - 00:47:39] Okay, so which one do you think is going to be the larger parasitic capacitance?
[00:47:39 - 00:47:44] The one from your head to the ceiling or the one from your thick to the ground?
[00:47:44 - 00:47:48] Think to the ground.
[00:47:48 - 00:47:49] Yes.
[00:47:49 - 00:47:51] Because it's a short distance.
[00:47:51 - 00:47:56] Okay, so I'll give you some typical values here.
[00:47:56 - 00:48:03] For example, the ones going up about three-peaker ferrets.
[00:48:03 - 00:48:09] There's lots of assumptions here about half-hour away from things,
[00:48:09 - 00:48:15] but just for this example, we'll say three-peaker ferrets going up,
[00:48:15 - 00:48:18] and 300-peaker ferrets going down.
[00:48:18 - 00:48:27] And as we see here, this is larger to ground dotted distance.
[00:48:27 - 00:48:47] Okay, so two minutes left, may or may not finish.
[00:48:47 - 00:48:56] Okay, so we can then just draw this as an equivalent circuit with 240 volts RMS,
[00:48:56 - 00:49:05] and then we'll just draw these as two capacitors in series.
[00:49:05 - 00:49:14] Okay, so this is three-peaker ferrets, 300-peaker ferrets,
[00:49:14 - 00:49:21] this one's C1, this one's C2.
[00:49:21 - 00:49:30] Okay, so what do we think the voltage across our body is going to be?
[00:49:30 - 00:49:36] But we're not going to get zero volts.
[00:49:36 - 00:49:45] So the voltage across the body is equal to the voltage of the mains, which is 240,
[00:49:45 - 00:49:49] and we've got a voltage divider here with the capacitors,
[00:49:49 - 00:49:51] C1 plus C2.
[00:49:51 - 00:50:10] And so I'll write these values and we'll finish this off on the next lecture on Monday.
[00:50:10 - 00:50:15] I'll stop now. We can finish this on Monday, but the answer is we're at about two volts.
[00:50:15 - 00:50:23] And so that's a problem for biomedical instrumentation in particular.
[00:50:23 - 00:50:28] So if we turn it on EEG on the brain or an ECG on your heart,
[00:50:28 - 00:50:30] you're introducing this capacitive coupling.
[00:50:30 - 00:50:35] You're changing the voltage signal from what it should be.
[00:50:35 - 00:50:37] Okay, so I'll put this up on the screen.
[00:50:37 - 00:50:39] Let me start on Wednesday.
[00:50:39 - 00:50:44] I'll put some tutorial questions up if you don't have a look before the tutorial on Thursday.
[00:51:19 - 00:51:26] I'd like to get it out of there.

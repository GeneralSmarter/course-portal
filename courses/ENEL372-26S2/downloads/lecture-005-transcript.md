# ENEL372-26S2 Lecture 5 fast-pass local ASR transcript

Date: July 23, 2026 3:00pm-3:55pm
Transcript type: Hermes fast-pass local ASR from validated Echo audio, not a native Echo transcript.
Backend/model: faster-whisper tiny.en, CPU int8, beam_size=1, vad_filter=True.
Quality note: fast catch-up transcript. Technical terms, equations, names and Māori words need checking against slides/audio before assessment use.
Source audio SHA-256: `50c85304cb1e1d17950686d6e179bf450f8be0f2ddc273ba37d38b6952d7f39c`
Generated: 2026-07-24T23:29:55.451216+12:00

[00:00:02.100 - 00:00:03.180] Oh, ready.
[00:00:03.180 - 00:00:07.530] Kyoto, welcome along.
[00:00:07.530 - 00:00:12.610] OK, so sure, let's land.
[00:00:12.610 - 00:00:18.610] Right, so we're going to move on in our depth of understanding
[00:00:18.610 - 00:00:24.170] and practicality associated with our buck converter
[00:00:24.170 - 00:00:26.930] buck converter considerations.
[00:00:26.930 - 00:00:33.770] And that furthering of knowledge is around design concepts.
[00:00:33.770 - 00:00:37.250] So there's all well and good to have theory associated
[00:00:37.250 - 00:00:39.250] with these converters.
[00:00:39.250 - 00:00:42.290] But we also need to take into consideration
[00:00:42.290 - 00:00:45.890] and keep in mind certain elements that are important.
[00:00:45.890 - 00:00:48.810] If we were actually to take that theory and utilize it
[00:00:48.810 - 00:00:52.450] to physically build these converters.
[00:00:52.450 - 00:00:55.450] We're going to look at it quite in depth for the buck
[00:00:55.450 - 00:00:56.890] converter because, of course, you're
[00:00:56.890 - 00:00:59.610] going to be designing and building your own buck converter
[00:00:59.610 - 00:01:01.290] for the solar car project.
[00:01:01.290 - 00:01:07.450] And it's a really good way to get that understanding
[00:01:07.450 - 00:01:11.130] of how to convert from design on page
[00:01:11.130 - 00:01:14.330] to physical implementation.
[00:01:14.330 - 00:01:19.770] Right, so the buck converters, one of the first things
[00:01:19.770 - 00:01:24.850] that we can really drill down into and make a proper consideration
[00:01:24.850 - 00:01:29.730] off, is how do we actually do our design to make sure
[00:01:29.730 - 00:01:34.010] that we keep our inductor current continuous?
[00:01:34.010 - 00:01:36.650] Now, I've mentioned this before a couple of times
[00:01:36.650 - 00:01:38.890] regarding buck converters.
[00:01:38.890 - 00:01:41.810] That this continuous current operation
[00:01:41.810 - 00:01:46.450] is assumed, give it to develop the analysis
[00:01:46.450 - 00:01:50.330] that we have done so far.
[00:01:50.330 - 00:01:52.650] Buck converters will work in what is defined
[00:01:52.650 - 00:01:55.330] as being discontinuous current mode.
[00:01:55.330 - 00:02:00.450] But it introduces a bunch of issues.
[00:02:00.450 - 00:02:05.730] So if we do keep the current continuous,
[00:02:05.730 - 00:02:09.610] then relative to being discontinuous,
[00:02:09.610 - 00:02:13.890] we get one better efficiency for our converters,
[00:02:13.890 - 00:02:21.690] which is a big deal for our power electronics.
[00:02:21.690 - 00:02:25.650] Two, for the most part, our buck converters
[00:02:25.650 - 00:02:27.250] don't work just in isolation.
[00:02:27.250 - 00:02:29.890] We are measuring things and using those measurements
[00:02:29.890 - 00:02:34.570] to do feedback control for our converters.
[00:02:34.570 - 00:02:37.450] So having them in a continuous operation
[00:02:37.450 - 00:02:50.500] is actually makes them more stable as well.
[00:02:50.500 - 00:02:54.740] We can, because of the continuous current nature,
[00:02:54.740 - 00:03:01.980] the RMS magnitudes for our various current voltages
[00:03:01.980 - 00:03:04.100] in that converter, a smaller.
[00:03:04.100 - 00:03:06.700] So that means that the filter components that we utilize,
[00:03:06.700 - 00:03:10.860] in order to make it a nice constant output voltage,
[00:03:10.860 - 00:03:15.340] or have the current at the input, the nice and continuous,
[00:03:15.340 - 00:03:18.020] and for that matter, having our continuous inductor current,
[00:03:18.020 - 00:03:21.900] means that we can end up with smaller components
[00:03:21.900 - 00:03:33.390] for filtering.
[00:03:33.390 - 00:03:35.150] And the final thing that I want to mention
[00:03:35.150 - 00:03:39.470] is, again, since the currents on average
[00:03:39.470 - 00:03:44.510] tend to be, or currents tend to have smaller peak values,
[00:03:44.510 - 00:03:46.390] because of this continuous nature,
[00:03:46.390 - 00:03:50.990] then the di by dt's, and for that matter,
[00:03:50.990 - 00:03:53.870] the dv by dt's are a little bit smaller.
[00:03:53.870 - 00:03:55.150] Why is that important?
[00:03:55.150 - 00:03:58.190] Well, those by the nature are sources
[00:03:58.190 - 00:04:01.230] of electrical noise in the circuit.
[00:04:01.230 - 00:04:02.870] So one of the things about switch mode circuits
[00:04:02.870 - 00:04:04.510] is that they do tend to be electrically
[00:04:04.510 - 00:04:07.470] a bit noisier than the linear counterparts.
[00:04:07.470 - 00:04:15.620] So reduces the amount of noise.
[00:04:15.620 - 00:04:18.940] So there are a bunch of reasons there,
[00:04:18.940 - 00:04:27.340] immediately, that guides us to attempt to try and design
[00:04:27.340 - 00:04:34.580] a converter that has continuous current operation.
[00:04:34.580 - 00:04:36.540] In order to be able to design that,
[00:04:36.540 - 00:04:40.180] we need to see what are the conditions or criteria that
[00:04:40.180 - 00:04:45.460] define when that current does become discontinuous.
[00:04:45.460 - 00:04:49.380] So here we've got the back converter circuit
[00:04:49.380 - 00:04:52.540] and the inductor current waveform.
[00:04:52.540 - 00:04:55.540] So we have the current ramping up
[00:04:55.540 - 00:05:02.640] when the controllable switch is closed or on.
[00:05:02.640 - 00:05:07.880] And then that's power in energizing the inductor.
[00:05:07.880 - 00:05:09.640] And then we open the open the switch,
[00:05:09.640 - 00:05:13.360] the inductor provides the energy through to the load.
[00:05:13.360 - 00:05:17.520] And that turns into being an energy source
[00:05:17.520 - 00:05:21.320] and the current ramp's down.
[00:05:21.320 - 00:05:25.640] So what we're talking about by keeping the current continuous
[00:05:25.640 - 00:05:33.440] is we're trying to make sure that at worst, usually,
[00:05:33.440 - 00:05:36.440] this is, you try to design it to be well away from the state.
[00:05:36.440 - 00:05:39.200] But the transition from it becoming continuous
[00:05:39.200 - 00:05:44.730] is discontinuous is when that minimum of the current just
[00:05:44.730 - 00:05:47.170] hits 0 amps.
[00:05:47.170 - 00:05:49.930] So this is I L 0.
[00:05:49.930 - 00:05:54.770] This is I out, which is, then previous rendition
[00:05:54.770 - 00:05:58.450] is what we have for I R. That's that continuous current that's
[00:05:58.450 - 00:06:02.660] flowing through the load resistance.
[00:06:02.660 - 00:06:09.500] Of course we have this is delta I L from peak to peak.
[00:06:09.500 - 00:06:13.980] And I don't think it takes a great deal of squinting your eyes
[00:06:13.980 - 00:06:14.780] at this.
[00:06:14.780 - 00:06:20.780] But that must surely mean that this transition current is
[00:06:20.780 - 00:06:28.520] delta I L over 2.
[00:06:28.520 - 00:06:31.080] So what we're trying to do by design
[00:06:31.080 - 00:06:39.330] is make sure that the average current output is always
[00:06:39.330 - 00:06:44.620] greater than delta I L over 2.
[00:06:44.620 - 00:06:47.300] If it's any less, you're going to end up with a situation
[00:06:47.300 - 00:06:52.060] where the inductor current comes down to 0 is 0 for a while.
[00:06:52.060 - 00:06:56.060] And then you switch the switch back on again.
[00:06:56.060 - 00:07:05.980] Just continuous current operation.
[00:07:05.980 - 00:07:06.300] Right.
[00:07:06.300 - 00:07:08.460] So what do we do?
[00:07:08.460 - 00:07:10.540] Well, what we help us with our design
[00:07:10.540 - 00:07:15.740] is to find a reasonable expression that we can calculate.
[00:07:15.740 - 00:07:18.060] So what is that?
[00:07:18.060 - 00:07:22.500] This expression tells us what a minimum inductor value will be
[00:07:22.500 - 00:07:27.420] in order to ensure that under certain other design
[00:07:27.420 - 00:07:31.380] conditions that we never have to discontinuous current
[00:07:31.380 - 00:07:33.380] operation.
[00:07:33.380 - 00:07:36.180] So we're looking at things like what is the output voltage
[00:07:36.180 - 00:07:38.420] for the for the application?
[00:07:38.420 - 00:07:40.660] What is your average current going to be?
[00:07:40.660 - 00:07:43.220] What's the duty cycle likely to be as well
[00:07:43.220 - 00:07:51.960] in the switching period or the frequency?
[00:07:51.960 - 00:07:53.920] So we can actually come up with an expression that
[00:07:53.920 - 00:07:55.720] gives us this minimum value of inductance
[00:07:55.720 - 00:08:03.720] by looking at the change in inductor current.
[00:08:03.720 - 00:08:05.600] So change in inductor current.
[00:08:05.600 - 00:08:10.280] We could look at when the switches on or when the switches off.
[00:08:10.280 - 00:08:14.800] Either or it doesn't matter because the change in inductor
[00:08:14.800 - 00:08:18.400] current is the same for each case.
[00:08:18.400 - 00:08:20.760] We're looking at steady state, which says
[00:08:20.760 - 00:08:23.520] that the sum of those two must equal 0 on average.
[00:08:23.520 - 00:08:26.760] So looking at the delta I L when the switch is closed
[00:08:26.760 - 00:08:29.800] is exactly the same in magnitude as looking at delta I L
[00:08:29.800 - 00:08:32.000] when the switch is open.
[00:08:32.000 - 00:08:36.080] We're going to take it when it's during the off period.
[00:08:36.080 - 00:08:40.360] So the change in inductor current when it's open,
[00:08:40.360 - 00:08:42.160] we've got minus.
[00:08:42.160 - 00:08:43.840] We're going to throw that out pretty soon
[00:08:43.840 - 00:08:46.440] because we're only interested in the magnitude.
[00:08:46.440 - 00:08:48.360] V out over L, 1 minus dt.
[00:08:48.360 - 00:08:49.760] So it's when the switch is open.
[00:08:49.760 - 00:08:54.510] So there's the 1 minus dt.
[00:08:54.510 - 00:09:01.150] All right, so the change is just V out over L, 1 minus.
[00:09:01.150 - 00:09:03.350] We're just taking the t out and giving us a switching
[00:09:03.350 - 00:09:06.470] frequency, which is by far the more common parameter
[00:09:06.470 - 00:09:10.790] that we design with.
[00:09:10.790 - 00:09:13.910] So we're going to substitute the in the expression for delta I L
[00:09:13.910 - 00:09:16.190] in the previous inequality that we just
[00:09:16.190 - 00:09:18.390] had in the previous slide.
[00:09:18.390 - 00:09:25.070] So I out has to be greater than half delta I L, which is what
[00:09:25.070 - 00:09:25.910] this is.
[00:09:25.910 - 00:09:30.160] So we just got delta I L divided by 2.
[00:09:30.160 - 00:09:34.760] We are ranging that expression for L gives us this final expression,
[00:09:34.760 - 00:09:36.320] which is dependent on the duty ratio,
[00:09:36.320 - 00:09:39.200] the output voltage, switching frequency,
[00:09:39.200 - 00:09:45.470] and the average output current.
[00:09:45.470 - 00:09:48.350] That would be all well and good if that was what we were
[00:09:48.350 - 00:09:52.950] specifically interested in where we have a fixed output
[00:09:52.950 - 00:09:56.870] voltage, which is, by the way, the more common situation
[00:09:56.870 - 00:09:58.510] when you are designing a buck converter.
[00:09:58.510 - 00:10:02.430] It's normally the load that defines the application parameters
[00:10:02.430 - 00:10:04.630] such as V out and the output current.
[00:10:04.630 - 00:10:08.390] However, for the solar car assignment,
[00:10:08.390 - 00:10:11.950] it's actually the input voltage that we're trying to control
[00:10:11.950 - 00:10:14.950] to be a fixed value.
[00:10:14.950 - 00:10:17.630] So we need to rearrange things a little bit
[00:10:17.630 - 00:10:22.230] to express that minimum inductance value in terms of input
[00:10:22.230 - 00:10:26.180] voltage, which is V s.
[00:10:26.180 - 00:10:27.820] Well, we already know that for a buck converter,
[00:10:27.820 - 00:10:31.380] that's pretty simple expression that the relationship
[00:10:31.380 - 00:10:37.140] between V out and V in or V s is just the duty ratio times V s.
[00:10:37.140 - 00:10:39.540] So we can make that substitution straight away.
[00:10:39.540 - 00:10:41.060] into this expression.
[00:10:41.060 - 00:10:42.980] And we will V out.
[00:10:42.980 - 00:10:46.060] So you've got V s d for V out.
[00:10:46.060 - 00:10:48.260] Multiply by 1 minus e over 2 of this.
[00:10:48.260 - 00:10:51.820] I have.
[00:10:51.820 - 00:11:00.300] That expression gives you a varying size of inductance.
[00:11:00.300 - 00:11:04.820] So you have a worst case product here
[00:11:04.820 - 00:11:09.420] for when the duty ratio is actually equal to 0.5.
[00:11:09.420 - 00:11:14.540] Because it goes all the way from being a 0 value up to a maximum of 0.25,
[00:11:14.540 - 00:11:19.500] which is another way of saying 1 quarter,
[00:11:19.500 - 00:11:23.660] back down to 0 when the duty ratio is 1.
[00:11:23.660 - 00:11:27.500] So by having this at its maximum means that we've
[00:11:27.500 - 00:11:32.620] got a value of inductance, which must be greater than.
[00:11:32.620 - 00:11:36.100] But that minimum value is at its maximum level,
[00:11:36.100 - 00:11:37.420] if we understand.
[00:11:37.420 - 00:11:44.140] Anywhere beyond 0.5 either way means that our value of inductance here
[00:11:44.140 - 00:11:47.900] can be less and less and less.
[00:11:47.900 - 00:11:56.500] So if we do put 1 quarter into here for d 1 minus d,
[00:11:56.500 - 00:12:00.260] then we have this rather simple expression in the end.
[00:12:00.260 - 00:12:02.860] For what our minimum value of inductance needs
[00:12:02.860 - 00:12:08.700] to be to avoid discontinuous current operation.
[00:12:08.700 - 00:12:12.420] Assuming that we have the ability to go all the way down
[00:12:12.420 - 00:12:20.750] to essentially that cutoff threshold.
[00:12:20.750 - 00:12:23.750] But that's for an application where the duty ratio of 0.5 might
[00:12:23.750 - 00:12:24.910] be experienced.
[00:12:24.910 - 00:12:30.150] If we have some other value of duty ratio or duty cycle,
[00:12:30.150 - 00:12:32.750] then we use this full expression.
[00:12:32.750 - 00:12:35.070] Because the minimum value will be somewhat less
[00:12:35.070 - 00:12:38.950] than this worst case situation.
[00:12:38.950 - 00:12:44.100] Yeah?
[00:12:44.100 - 00:12:44.660] All right.
[00:12:44.660 - 00:12:51.900] So for this old car, in really good situation,
[00:12:51.900 - 00:12:53.940] if you've got a good converter going,
[00:12:53.940 - 00:12:56.900] and the car is zipping along quite quickly,
[00:12:56.900 - 00:13:02.420] you might just reach the conditions where the duty ratio hits 0.5.
[00:13:02.420 - 00:13:07.020] It's likely to be a little bit less than 0.5,
[00:13:07.020 - 00:13:11.220] because you've got quite a voltage step down to achieve.
[00:13:11.220 - 00:13:14.900] Especially at least especially at start up.
[00:13:14.900 - 00:13:17.700] So from standstill, the output current
[00:13:17.700 - 00:13:21.660] needs to be very large, which means the voltage will be low.
[00:13:21.660 - 00:13:26.260] So a small output voltage given 17 volts or so
[00:13:26.260 - 00:13:28.340] at the input means a very, very small duty ratio
[00:13:28.340 - 00:13:29.540] to begin with.
[00:13:29.540 - 00:13:33.100] Once the car speeds up, then it's quite possible
[00:13:33.100 - 00:13:37.220] in that the output voltage will need to come up
[00:13:37.220 - 00:13:40.660] and that duty ratio increases.
[00:13:40.660 - 00:13:44.680] Potentially up to close to 0.5.
[00:13:44.680 - 00:13:49.290] Questions?
[00:13:49.290 - 00:13:56.400] Right.
[00:13:56.400 - 00:13:58.800] What about the switching frequency?
[00:13:58.800 - 00:14:02.480] How do we choose what is that value of frequency
[00:14:02.480 - 00:14:05.480] that we're going to have in our design?
[00:14:05.480 - 00:14:09.520] Well, I'd like to say it kind of is a bit fuzzy as to how
[00:14:09.520 - 00:14:10.720] we choose that frequency.
[00:14:10.760 - 00:14:15.400] Higher frequencies, they've got an advantage.
[00:14:15.400 - 00:14:18.320] If we go to higher frequencies, we can get smaller inductors
[00:14:18.320 - 00:14:21.000] and capacitors.
[00:14:21.000 - 00:14:22.480] Just look at the previous expression.
[00:14:22.480 - 00:14:27.640] It was to 1 over F. So if you go to higher frequencies,
[00:14:27.640 - 00:14:33.840] that minimum inductance that you need drops, proportionally
[00:14:33.840 - 00:14:35.840] with frequency.
[00:14:35.840 - 00:14:39.320] So that sounds good.
[00:14:39.320 - 00:14:43.600] And having smaller, especially magnetic components
[00:14:43.600 - 00:14:48.280] within a converter, that's a big cost saving.
[00:14:48.280 - 00:14:51.680] The smaller that can be, the generally the cheaper
[00:14:51.680 - 00:14:55.600] the converter can be.
[00:14:55.600 - 00:14:59.960] Not only that, smaller, the actual magnetic material
[00:14:59.960 - 00:15:04.160] that we have for our magnetic components,
[00:15:04.160 - 00:15:07.320] like inductors and transformers and parallel electronics,
[00:15:07.320 - 00:15:13.480] is very not only expensive, but it is material wise.
[00:15:13.480 - 00:15:16.920] Has quite the carbon footprint that goes with it.
[00:15:16.920 - 00:15:21.560] So we can get away with a smaller amount of that magnetic
[00:15:21.560 - 00:15:24.120] material, then it also helps with the whole sustainability
[00:15:24.120 - 00:15:28.500] of the converter.
[00:15:28.500 - 00:15:29.700] That's the positive side.
[00:15:29.700 - 00:15:32.580] The negative side of going to higher frequencies,
[00:15:32.580 - 00:15:35.380] and it is quite substantial as well,
[00:15:35.380 - 00:15:37.500] means that you're going to introduce more switching
[00:15:37.500 - 00:15:39.740] and magnetic component losses.
[00:15:39.740 - 00:15:41.740] All right.
[00:15:41.740 - 00:15:45.100] So some of the non-ideal elements of these components
[00:15:45.100 - 00:15:47.780] starts to play a factor.
[00:15:47.780 - 00:15:49.820] You get more electrical noise, because you
[00:15:49.820 - 00:15:54.660] have these higher di by dt and dv by dt elements, which
[00:15:54.660 - 00:15:58.140] means more noise.
[00:15:58.140 - 00:16:01.460] And because those losses start to increase the efficiency
[00:16:01.460 - 00:16:06.220] begins to suffer at higher frequency.
[00:16:06.220 - 00:16:09.660] So there's going to be a sweet spot,
[00:16:09.660 - 00:16:12.740] depending on the application, what sort of resources
[00:16:12.740 - 00:16:15.460] you have at your disposal, what kind of access
[00:16:15.460 - 00:16:16.620] you have to do.
[00:16:16.620 - 00:16:20.260] Your switching components, the magnetic materials, and so
[00:16:20.260 - 00:16:21.140] forth.
[00:16:21.140 - 00:16:26.460] So just to give you a ballpark, though, most modern power
[00:16:26.460 - 00:16:31.700] electronic converters operate in a few hundred kilohertz
[00:16:31.700 - 00:16:35.740] region in general.
[00:16:35.780 - 00:16:40.880] For the project, what do we recommend?
[00:16:40.880 - 00:16:44.000] You don't have a lot of experience with power electronics.
[00:16:44.000 - 00:16:46.160] So where do you start?
[00:16:46.160 - 00:16:49.960] Are you going to have a converter that works at a megahertz?
[00:16:49.960 - 00:16:51.520] Switching frequency?
[00:16:51.520 - 00:16:53.480] I certainly hope not.
[00:16:53.480 - 00:16:55.560] There would be a big problem.
[00:16:55.560 - 00:16:57.720] Or are you going to have it switching,
[00:16:57.720 - 00:17:01.280] because you're super interested in keeping the efficiency
[00:17:01.280 - 00:17:02.040] high.
[00:17:02.040 - 00:17:05.200] And I've just said high frequency leads to lower efficiency.
[00:17:05.200 - 00:17:09.040] You're going to switch it at 10 Hertz.
[00:17:09.040 - 00:17:12.400] That could also lead to a few problems.
[00:17:12.400 - 00:17:17.080] So to give you a ballpark, I don't recommend going any lower
[00:17:17.080 - 00:17:20.400] than 20 kilohertz.
[00:17:20.400 - 00:17:21.880] That's the minimum end.
[00:17:21.880 - 00:17:23.640] Now, why is that the minimum end?
[00:17:23.640 - 00:17:29.000] Well, it's actually around about the limit of human hearing.
[00:17:29.000 - 00:17:32.520] If you go a bit lower than that, your converter is going to get
[00:17:32.520 - 00:17:36.120] extremely annoying to be around.
[00:17:36.120 - 00:17:36.960] You're going to hear it.
[00:17:36.960 - 00:17:42.920] It's going to wind and just be put your teeth on edge.
[00:17:42.920 - 00:17:46.760] So 20 kilohertz and above, you won't hear it.
[00:17:46.760 - 00:17:49.000] Sweet.
[00:17:49.000 - 00:17:49.720] All right.
[00:17:49.720 - 00:17:52.440] So what about the upper range?
[00:17:52.440 - 00:17:55.440] All right.
[00:17:55.440 - 00:18:02.160] We're, I'm going to recommend, because it alleviates a lot of the
[00:18:02.160 - 00:18:06.000] kind of layout issues associated with the converter,
[00:18:06.000 - 00:18:12.440] of being less than 100 kilohertz.
[00:18:12.440 - 00:18:16.080] Now, 100 kilohertz is going to be a bit tricky to get going
[00:18:16.080 - 00:18:18.120] on a breadboard.
[00:18:18.120 - 00:18:20.160] There are a lot of parasitic elements.
[00:18:20.160 - 00:18:25.360] A lot of stray inductance and stray capacitance that
[00:18:25.360 - 00:18:29.000] interferes with the operation of your converter.
[00:18:29.000 - 00:18:35.280] And at 100 kilohertz, that really starts to affect that
[00:18:35.280 - 00:18:45.460] converter on a breadboard.
[00:18:45.460 - 00:18:48.060] It has parasitics, yes, certainly.
[00:18:48.060 - 00:18:52.420] But you can deal to a portion of that by stripping off
[00:18:52.420 - 00:18:57.300] unused bits of the copper, rather than leaving it there.
[00:18:57.300 - 00:19:01.100] It's a lot better than breadboarding.
[00:19:01.100 - 00:19:05.660] A well laid out, very bored circuit can operate into the
[00:19:05.660 - 00:19:10.300] hundreds of kilohertz without much issue at all.
[00:19:10.300 - 00:19:11.980] And certainly PCV.
[00:19:11.980 - 00:19:16.300] Yeah, it doesn't have much of a problem at all.
[00:19:16.300 - 00:19:18.860] But if you go into the hundreds of kilohertz,
[00:19:18.860 - 00:19:21.140] prototyping becomes hard on breadboard.
[00:19:21.140 - 00:19:22.540] So I don't recommend it.
[00:19:22.540 - 00:19:26.060] And even with Vero board, the layout, you have to give it some
[00:19:26.060 - 00:19:27.260] thought.
[00:19:27.260 - 00:19:31.740] And like I say, kind of strip off unused bits of copper on the
[00:19:31.740 - 00:19:32.780] Vero board.
[00:19:32.780 - 00:19:37.420] Keeping it at 100 kilohertz kind of eases up on that kind of
[00:19:37.420 - 00:19:38.220] requirement.
[00:19:38.220 - 00:19:42.860] And means that you can be less optimal with the way that the
[00:19:42.860 - 00:19:45.990] circuit is laid out.
[00:19:45.990 - 00:19:47.150] So it goes easier on you.
[00:19:47.150 - 00:19:52.190] And 100 kilohertz and above some of the losses start to play a
[00:19:52.190 - 00:19:54.270] bit of a roll.
[00:19:54.270 - 00:19:57.430] So the efficiency does drop down a bit.
[00:19:57.430 - 00:20:01.430] That's what I would suggest is your limits of switching
[00:20:01.430 - 00:20:06.260] frequency for the project.
[00:20:06.260 - 00:20:09.420] Just to highlight some of the elements to do with this
[00:20:09.420 - 00:20:12.020] continuous conduction, if you get it wrong,
[00:20:12.020 - 00:20:16.660] with the inductor size, go too small.
[00:20:16.660 - 00:20:19.420] We get nonlinear gain, which is where I was talking about
[00:20:19.420 - 00:20:20.100] the stability.
[00:20:20.100 - 00:20:22.300] It becomes harder to control.
[00:20:22.300 - 00:20:28.740] Here, in fact, is a plot off a hand drawn diagram of the
[00:20:28.740 - 00:20:30.980] gain through our buck converter.
[00:20:30.980 - 00:20:32.420] So here's your duty ratio.
[00:20:32.420 - 00:20:34.620] And here's the output to input voltage.
[00:20:34.620 - 00:20:37.740] So zero duty ratio, zero output voltage.
[00:20:37.740 - 00:20:41.580] Duty ratio of one, you've got the output equal to the
[00:20:41.580 - 00:20:44.020] input.
[00:20:44.020 - 00:20:47.660] And it's nice and linear all the way from one end to the
[00:20:47.660 - 00:20:52.360] other if your current is continuous.
[00:20:52.360 - 00:20:53.480] Becomes this continuous.
[00:20:53.480 - 00:20:55.720] You end up with this kind of blip.
[00:20:55.720 - 00:20:58.600] You still, it still works.
[00:20:58.600 - 00:20:59.760] But you end up with this blip.
[00:20:59.760 - 00:21:02.640] The gain is no longer linear.
[00:21:02.640 - 00:21:06.160] So it becomes a lot harder to work with.
[00:21:06.160 - 00:21:09.120] The output voltage becomes dependent on the load current,
[00:21:09.120 - 00:21:11.520] which means the duty ratio has to change for different
[00:21:11.520 - 00:21:13.080] loads.
[00:21:13.080 - 00:21:16.520] So that means you can't just fix the duty ratio for a
[00:21:16.520 - 00:21:18.520] particular output voltage.
[00:21:18.520 - 00:21:21.600] You load current changes in that voltage will start
[00:21:21.600 - 00:21:23.200] varying.
[00:21:23.200 - 00:21:26.120] So you have to change the duty ratio.
[00:21:26.120 - 00:21:29.400] For a given power flow, since you've got current zero at
[00:21:29.400 - 00:21:34.720] times, the peak is to get higher, to achieve that average
[00:21:34.720 - 00:21:38.440] that you're aiming for, which means that you have higher
[00:21:38.480 - 00:21:39.840] currents.
[00:21:39.840 - 00:21:42.320] You need the ratings on your switches to be higher because of
[00:21:42.320 - 00:21:43.760] that.
[00:21:43.760 - 00:21:46.560] They're more expensive and slower switching.
[00:21:46.560 - 00:21:47.800] So that's not good.
[00:21:47.800 - 00:21:49.280] They produce more harmonics.
[00:21:49.280 - 00:21:53.720] That means more electrical noises and higher losses.
[00:21:53.720 - 00:21:58.160] So this really, really best not to go discontinuous for your
[00:21:58.160 - 00:22:08.710] converter operation.
[00:22:08.710 - 00:22:11.270] You know how I said that we assume that the output
[00:22:11.270 - 00:22:13.270] voltage is constant.
[00:22:13.270 - 00:22:18.150] DC value of the out and it doesn't change.
[00:22:18.150 - 00:22:22.720] That's what we'd base the our analysis on, right?
[00:22:22.720 - 00:22:26.040] The reality is a little different.
[00:22:26.040 - 00:22:29.880] You have a physical capacitance in parallel with the load.
[00:22:29.880 - 00:22:33.440] It's accepting current at parts of the cycle and it's
[00:22:33.440 - 00:22:34.880] delivering current at other parts.
[00:22:34.880 - 00:22:37.400] So it's charging and discharging.
[00:22:37.400 - 00:22:42.480] Any capacitor with a finite capacitance, if you're
[00:22:42.480 - 00:22:45.920] charging it and discharging, it's voltage will go up and
[00:22:45.920 - 00:22:47.720] down.
[00:22:47.720 - 00:22:50.080] Yeah.
[00:22:50.080 - 00:22:51.280] We've got that expression here.
[00:22:51.280 - 00:22:53.560] Mount of charge and capacitor, capacitance value
[00:22:53.560 - 00:22:57.040] and voltage.
[00:22:57.040 - 00:23:02.800] So what we are assuming when we do the initial analysis is
[00:23:02.800 - 00:23:06.960] that that capacitance in the back converter is pointing
[00:23:06.960 - 00:23:09.560] at waveform.
[00:23:09.560 - 00:23:11.680] That capacitance in the back converter is off a
[00:23:11.680 - 00:23:16.640] sufficiently large size that any kind of voltage ripple here
[00:23:16.640 - 00:23:23.040] is inconsequential or insignificant to that analysis.
[00:23:23.040 - 00:23:27.160] So a little value compared to the overall output
[00:23:27.160 - 00:23:28.960] voltage.
[00:23:28.960 - 00:23:34.800] Usually we aim for values that are less than a 1% of the
[00:23:34.800 - 00:23:41.950] output voltage level.
[00:23:41.950 - 00:23:43.510] OK.
[00:23:43.550 - 00:23:46.910] So it has some output ripple, but small enough not to have an
[00:23:46.910 - 00:23:52.360] appreciable effect on that previous analysis.
[00:23:52.360 - 00:23:58.470] Right.
[00:23:58.470 - 00:24:04.070] So this is the back converter switch close, switch open,
[00:24:04.070 - 00:24:05.790] the voltage across the inductance.
[00:24:05.790 - 00:24:10.070] Here's the inductor current with its ripple.
[00:24:10.070 - 00:24:13.470] We've done the analysis already before and we can see that
[00:24:13.470 - 00:24:21.430] the capacitor current is just equal to the inductor
[00:24:21.430 - 00:24:26.860] current ripple.
[00:24:26.860 - 00:24:32.860] From when it becomes higher than the average current and
[00:24:32.860 - 00:24:40.830] less than the average current, that is half a period T over
[00:24:40.830 - 00:24:49.220] two.
[00:24:49.260 - 00:24:57.390] Not only that is that the area above the average current, so
[00:24:57.390 - 00:25:12.980] a1 and the area below a2 are equal.
[00:25:12.980 - 00:25:17.220] We also have the state that from the definition of the
[00:25:17.220 - 00:25:23.300] current directions that we're using, the convention, is that
[00:25:23.300 - 00:25:33.140] whilst that capacitor current is positive, it is entering the
[00:25:33.140 - 00:25:37.120] capacitor, so it is charging.
[00:25:37.120 - 00:25:44.970] So whilst it's positive, this is charging.
[00:25:44.970 - 00:26:06.410] Wherever it's negative, it's discharging.
[00:26:06.410 - 00:26:06.810] Right.
[00:26:06.810 - 00:26:11.730] So we've got charging and a period of time.
[00:26:11.730 - 00:26:17.810] So that area that we were just talking about, given this
[00:26:17.810 - 00:26:21.890] quality and understanding that the capacitor current is
[00:26:21.890 - 00:26:26.810] equal to the capacitance dv by dt means that that's the
[00:26:26.810 - 00:26:30.210] amount of charge q.
[00:26:30.210 - 00:26:38.030] Charged it's entering the capacitor whilst it's charging and
[00:26:38.030 - 00:26:40.990] the amount of charge that leads the capacitor when it's
[00:26:40.990 - 00:26:44.190] discharging, which are of course unbalanced.
[00:26:44.190 - 00:26:53.890] So on average, that's equal to 0.
[00:26:53.890 - 00:26:54.610] OK.
[00:26:54.610 - 00:27:02.690] So from here, what we want to actually determine is what sort
[00:27:02.690 - 00:27:07.130] of design criteria can we have to make sure that the output
[00:27:07.130 - 00:27:13.070] voltage ripple is kept within certain bounds.
[00:27:13.070 - 00:27:17.710] So we've got delta vc.
[00:27:17.710 - 00:27:20.430] So from this expression, we just can rearrange that equals
[00:27:20.430 - 00:27:31.630] 1 over c times the integral of the current dt.
[00:27:31.630 - 00:27:35.670] That's just equal to 1 over c, the integral area under the
[00:27:35.670 - 00:27:44.110] curve times the area, which we've determined is the
[00:27:44.110 - 00:27:45.630] amount of charge.
[00:27:45.630 - 00:27:51.350] So that's equal to 1 over c, and we've got t over 2.
[00:27:51.350 - 00:27:53.190] This is just a triangle, right?
[00:27:53.190 - 00:27:56.230] We're looking at for the area of a triangle.
[00:27:56.230 - 00:27:59.310] So half base times height.
[00:27:59.310 - 00:28:01.030] So we've got 1 half.
[00:28:01.030 - 00:28:04.990] The base is t over 2 times the height.
[00:28:04.990 - 00:28:11.860] What's the height?
[00:28:11.860 - 00:28:15.660] What's the vertical height of this triangle?
[00:28:15.660 - 00:28:17.380] Yep.
[00:28:17.380 - 00:28:19.380] Half delta i over 2.
[00:28:19.380 - 00:28:29.670] Yeah, exactly.
[00:28:29.670 - 00:28:35.980] Equals delta i l over 8.
[00:28:36.020 - 00:28:38.460] Well, take the inverse of t.
[00:28:38.460 - 00:28:47.620] There's the frequency if s c.
[00:28:47.620 - 00:28:52.600] That's the ripple voltage.
[00:28:52.600 - 00:28:54.200] Well, what does that look?
[00:28:54.200 - 00:28:57.240] What does that ripple voltage look like?
[00:28:57.240 - 00:29:01.880] I'm going to make the ripple look a lot worse than what it is
[00:29:01.880 - 00:29:04.600] because I've got limited vertical scale to work with here.
[00:29:04.600 - 00:29:08.440] So here's our average voltage.
[00:29:08.440 - 00:29:10.480] Now for our back converter, that's v out.
[00:29:10.480 - 00:29:15.530] It's the average DC value that we've said is completely constant.
[00:29:15.530 - 00:29:19.770] So very important to look at when we change from being
[00:29:19.770 - 00:29:32.020] charging to discharging and the peaks of when we're charging
[00:29:32.020 - 00:29:46.020] and the peaks of when we're discharging.
[00:29:46.020 - 00:29:46.380] Right.
[00:29:46.380 - 00:29:50.420] So when you have been at this part of the curve,
[00:29:50.420 - 00:29:53.820] it's been discharging and then you move to charging.
[00:29:53.820 - 00:29:57.580] You've been decreasing the voltage and then that stops,
[00:29:57.580 - 00:29:59.220] and then you start increasing the voltage.
[00:29:59.220 - 00:30:04.860] So it's at the bottom of the voltage ripple.
[00:30:04.860 - 00:30:09.740] So at that point there we're at a low point.
[00:30:09.740 - 00:30:10.100] Right.
[00:30:10.100 - 00:30:13.940] And it's been coming down.
[00:30:13.940 - 00:30:15.580] But then it starts.
[00:30:15.580 - 00:30:18.060] It's the 0, and it starts rising.
[00:30:18.060 - 00:30:22.620] You get to the peak of the rising.
[00:30:22.620 - 00:30:26.660] And that's its fastest rate of change.
[00:30:26.660 - 00:30:35.060] So that's when it passes through v out.
[00:30:35.060 - 00:30:43.220] Then by the time you get to it being from charging to discharging,
[00:30:43.220 - 00:30:47.100] all right, then you've hit your peak.
[00:30:47.100 - 00:30:54.820] And it comes down again because you're now discharging your
[00:30:54.820 - 00:30:57.100] capacitor.
[00:30:57.140 - 00:31:03.990] Passes the peak again at a maximum.
[00:31:03.990 - 00:31:15.240] And then again when we have converting from charging to charging,
[00:31:15.240 - 00:31:17.640] peaks of at 0 again.
[00:31:17.640 - 00:31:22.170] So this is the same level across.
[00:31:22.170 - 00:31:25.050] So it's not a nice linear waveform.
[00:31:25.050 - 00:31:28.330] The ramping up and ramping down, it kind of depends
[00:31:28.330 - 00:31:34.330] on the rate of change of the charging and discharging.
[00:31:34.330 - 00:31:43.860] And it kind of curves off as we reach those limits.
[00:31:43.860 - 00:31:44.140] All right.
[00:31:44.140 - 00:31:47.740] So I've really, really expanded that ripple.
[00:31:47.740 - 00:31:50.860] That ripple relative to this would only be like a percent.
[00:31:50.860 - 00:31:53.340] So peak is here and here.
[00:31:53.340 - 00:31:59.700] So tiny.
[00:31:59.700 - 00:32:08.840] So delta v out is equal to, oh, we've got delta i l still here.
[00:32:08.840 - 00:32:18.360] So delta i l is equal to v out from previously 1 minus d over l
[00:32:18.360 - 00:32:23.690] f s.
[00:32:23.690 - 00:32:27.370] So that was on page two of the notes there.
[00:32:27.370 - 00:32:30.170] So we can then put this in for delta i l.
[00:32:30.170 - 00:32:32.970] So we have the change in output voltage is equal to the input
[00:32:32.970 - 00:32:33.610] voltage.
[00:32:33.610 - 00:32:40.130] I mean the output voltage times 1 minus d over 8 lc f squared.
[00:32:40.170 - 00:32:42.010] Huh.
[00:32:42.010 - 00:32:48.050] So that output ripple can really, really reduce very rapidly
[00:32:48.050 - 00:32:54.290] with increasing frequency.
[00:32:54.290 - 00:32:57.410] So that means that the capacitor value, if you're
[00:32:57.410 - 00:33:01.250] going to rearrange that to solp for capacitance,
[00:33:01.250 - 00:33:03.730] that capacitance value can come down and size quite
[00:33:03.730 - 00:33:15.430] dramatically with increasing frequency.
[00:33:15.430 - 00:33:18.590] For the sola car, again, you should still
[00:33:18.590 - 00:33:24.430] work to the capacitance value, assuming the worst case duty
[00:33:24.430 - 00:33:33.180] ratio, which would be at 0.5.
[00:33:33.180 - 00:33:33.460] Right.
[00:33:33.460 - 00:33:38.340] So now we've considered a more realistic situation
[00:33:38.340 - 00:33:41.500] for the output of the converter and the amount of voltage
[00:33:41.500 - 00:33:42.660] ripple there is.
[00:33:42.660 - 00:33:46.860] So now if you were to determine that the voltage ripple had
[00:33:46.860 - 00:33:50.980] to be 1% or less of the output voltage,
[00:33:50.980 - 00:33:54.300] you have an expression that you can use to design for that,
[00:33:54.300 - 00:33:57.420] given a certain amount of capacitance.
[00:33:57.420 - 00:34:00.300] Understanding that you have chosen already a switching
[00:34:00.300 - 00:34:05.020] frequency to work with, and you know your minimum value or the
[00:34:05.020 - 00:34:07.580] actual working value of inductance that you have for your
[00:34:07.580 - 00:34:11.800] converter.
[00:34:11.800 - 00:34:18.080] Input and output voltage is a relationship with the duty ratio.
[00:34:18.080 - 00:34:22.040] So what is the worst case situation for this type of
[00:34:22.040 - 00:34:22.960] application?
[00:34:22.960 - 00:34:33.100] So when that duty ratio is 0.5.
[00:34:33.100 - 00:34:37.140] Now if your back converter is being supplied by a perfect
[00:34:37.140 - 00:34:40.900] voltage source, then that input voltage will be completely
[00:34:40.900 - 00:34:46.940] constant, just like the analysis has assumed.
[00:34:46.940 - 00:34:50.900] Let's assume now that maybe your voltage source isn't quite
[00:34:50.900 - 00:34:52.500] so perfect.
[00:34:52.500 - 00:34:59.420] Or your voltage source is some considerable distance away from
[00:34:59.420 - 00:35:00.820] the actual input of your back converter.
[00:35:00.820 - 00:35:05.340] So there could be voltage-drups or issues associated
[00:35:05.340 - 00:35:08.220] with the distance from your source to the input of the
[00:35:08.220 - 00:35:10.460] back converter.
[00:35:10.460 - 00:35:15.740] Then we need to employ an input capacitance at the input of
[00:35:15.740 - 00:35:21.740] the back converter to try and maintain a stable of a voltage
[00:35:21.740 - 00:35:28.400] as is necessary for the application.
[00:35:28.400 - 00:35:31.920] It even gets a little bit more complicated for a solar panel
[00:35:31.920 - 00:35:37.680] as your voltage source, because it's not strictly speaking a
[00:35:37.680 - 00:35:38.800] voltage source as such.
[00:35:38.800 - 00:35:44.550] It's more of a current source than it is above the source.
[00:35:44.550 - 00:35:49.710] And works best and most efficiently when it is providing a
[00:35:49.710 - 00:35:54.190] constant current, not just a continuous current, but a
[00:35:54.190 - 00:35:56.550] constant current.
[00:35:56.550 - 00:36:01.470] So DC currents from solar panels means that they're operating
[00:36:01.470 - 00:36:07.510] at their most efficient state.
[00:36:07.510 - 00:36:12.430] And we've already determined that for a maximum power, then we
[00:36:12.430 - 00:36:16.230] also have a specific voltage that we want to work with for
[00:36:16.230 - 00:36:17.670] the solar panel.
[00:36:17.670 - 00:36:19.150] Right.
[00:36:19.150 - 00:36:23.630] So we have for the solar current, a solar panel.
[00:36:23.630 - 00:36:27.470] We've got an output current from the solar panel, this I S, which
[00:36:27.470 - 00:36:32.150] we're hoping to achieve to be constant.
[00:36:32.150 - 00:36:38.790] So this would be actually, if it was a constant capital I S.
[00:36:38.790 - 00:36:41.990] Just like we want to achieve for a resistive load, a constant
[00:36:41.990 - 00:36:46.300] current to that load.
[00:36:46.300 - 00:36:51.180] So we want that current ripple would be as small as possible and
[00:36:51.180 - 00:36:54.940] also to have a low voltage ripple, keeping it at the maximum
[00:36:54.940 - 00:36:58.500] power point and that continuous current.
[00:36:58.500 - 00:37:02.220] So we keep the constant current.
[00:37:02.220 - 00:37:05.500] So it keeps the losses low and maintain that operation for
[00:37:05.500 - 00:37:06.820] maximum power point.
[00:37:06.820 - 00:37:12.620] So we need a capacitor at the input.
[00:37:12.620 - 00:37:16.340] And it has to be appropriately sized.
[00:37:16.340 - 00:37:17.420] All right.
[00:37:17.420 - 00:37:20.540] First up, to be keeping things simple, we're going to assume that
[00:37:20.540 - 00:37:29.450] the current ripple from the source is equal to zero.
[00:37:29.450 - 00:37:33.090] So by Kirchhoff's current law from just this node that we're
[00:37:33.090 - 00:37:38.930] looking at, we have the capacitor current is equal to I S minus
[00:37:38.930 - 00:37:45.060] the current flowing into the back converter.
[00:37:45.060 - 00:37:45.940] OK.
[00:37:45.940 - 00:37:50.220] We've drawn effectively this here.
[00:37:50.220 - 00:37:52.180] So here's I 1.
[00:37:52.180 - 00:37:58.620] This is the current that we have going into the back converter.
[00:37:58.620 - 00:37:58.740] Right?
[00:37:58.740 - 00:38:00.900] So the switch closes.
[00:38:00.940 - 00:38:05.980] Current jumps up and follows the ramping up current into the inductor.
[00:38:05.980 - 00:38:13.940] Then you open the switch and that current stops goes down to zero.
[00:38:13.940 - 00:38:17.900] You wait until we reach the end of the period and we turn that switch
[00:38:17.900 - 00:38:22.890] back on and then we have that current flowing again.
[00:38:22.890 - 00:38:24.490] Clear?
[00:38:24.490 - 00:38:26.890] That's what I 1 looks like.
[00:38:26.890 - 00:38:32.980] This I S average is what we want from the solar panel.
[00:38:32.980 - 00:38:33.620] That's this one.
[00:38:33.620 - 00:38:33.980] Sorry.
[00:38:34.020 - 00:38:38.650] F.
[00:38:38.650 - 00:38:45.940] So that's the solar panel current.
[00:38:45.940 - 00:38:54.860] This equation tells us that I C is equal to I S minus I 1.
[00:38:54.860 - 00:39:02.840] So let's draw that.
[00:39:02.840 - 00:39:03.320] OK.
[00:39:03.320 - 00:39:07.630] So we've got, I'll draw that in a different color.
[00:39:07.630 - 00:39:24.010] So you can distinguish.
[00:39:24.010 - 00:39:30.250] And just because I'm such a rubber straw, that's why I've highlighted what the
[00:39:30.250 - 00:39:34.140] areas are under the curves.
[00:39:34.140 - 00:39:36.500] So that I see a 1 there.
[00:39:36.500 - 00:39:43.280] So that's a 1.
[00:39:43.280 - 00:39:58.270] And a 2k.
[00:39:58.270 - 00:40:04.830] So we can determine what the voltage ripple is by analyzing
[00:40:04.830 - 00:40:10.230] particularly what is the change in capacitor voltage in this period here
[00:40:10.230 - 00:40:16.150] where there's constant current flowing into the capacitor.
[00:40:16.150 - 00:40:19.910] The capacitor is charging at this point because that's positive current into
[00:40:19.910 - 00:40:21.670] the capacitor.
[00:40:21.670 - 00:40:23.390] But it's a constant current.
[00:40:23.390 - 00:40:27.350] So you charge a capacitor with constant current and you will have a linearly
[00:40:27.350 - 00:40:34.450] ramping increasing voltage.
[00:40:34.450 - 00:40:36.690] I C equals C dV by dt.
[00:40:39.760 - 00:40:40.040] Right.
[00:40:40.080 - 00:40:58.310] So we have then that this gives us delta V equals I delta T over C.
[00:40:58.310 - 00:40:58.870] All right.
[00:40:58.870 - 00:41:05.030] So delta T for when the switch is off.
[00:41:05.030 - 00:41:07.070] Of course, this is dt.
[00:41:07.070 - 00:41:19.110] So that's 1 minus dt.
[00:41:19.110 - 00:41:21.950] So here we get I.
[00:41:22.030 - 00:41:31.080] Times delta T 1 minus dt over C.
[00:41:31.080 - 00:41:32.680] OK, that's great.
[00:41:32.680 - 00:41:36.600] But we're more likely to know what the output current is than the input current.
[00:41:39.480 - 00:41:43.480] So how do we relate the input current to the output?
[00:41:43.480 - 00:41:49.610] So that's the most current for us.
[00:41:49.610 - 00:41:58.300] You know, 1 to 2 amps somewhere around that ball back.
[00:41:58.300 - 00:42:02.980] What's the relationship between the source current and the output current?
[00:42:03.020 - 00:42:08.260] Well, it's kind of if we're looking at power transfer through, if we're stepping
[00:42:08.260 - 00:42:16.020] down the voltage from input to output, we've got constant power, then we step up the current
[00:42:16.020 - 00:42:17.300] to the output.
[00:42:17.300 - 00:42:23.660] So looking the other way, then we've got the output current, then we're stepping down the
[00:42:23.660 - 00:42:34.970] output current to the input.
[00:42:34.970 - 00:42:37.250] So here it is just written out.
[00:42:37.250 - 00:42:42.610] So if we assume that the converter just for argument's sake is 100% efficient.
[00:42:42.610 - 00:42:47.170] So the product between the output current and the output voltage will be equal to the product
[00:42:47.170 - 00:42:54.250] between the input current and the input voltage, the average values.
[00:42:54.250 - 00:43:01.730] We already know that the output voltage is equal to the duty ratio times the input voltage.
[00:43:01.730 - 00:43:12.010] So we have I out times dbs substituting in for v out equals ISVS.
[00:43:12.010 - 00:43:15.970] We've got Bs on both sides of that equation.
[00:43:15.970 - 00:43:19.090] So they just cancel.
[00:43:19.090 - 00:43:28.490] Leaving us with the IS is equal to the duty ratio times I out.
[00:43:28.490 - 00:43:33.650] Looking back through the converter from output to input, you just use the duty ratio
[00:43:33.650 - 00:43:40.900] again, but for current.
[00:43:40.900 - 00:43:48.780] Giving us in this case, looking at the change in the ripple of voltage at the input, equal
[00:43:48.780 - 00:43:56.280] to the output current times d1 minus d again.
[00:43:56.280 - 00:43:58.200] We've come across this.
[00:43:58.200 - 00:44:06.170] So there's a worst case scenario here for a duty ratio equal to 0.5.
[00:44:06.170 - 00:44:12.170] So 4d equals 0.5.
[00:44:12.170 - 00:44:17.650] We've got d times 1 minus d equals 1 over 4.
[00:44:17.650 - 00:44:27.690] So c in has to be greater than I out over 4 times the switching frequency times the change
[00:44:27.690 - 00:44:35.380] in the source voltage, the source voltage ripple.
[00:44:35.380 - 00:44:42.900] So if we have that as a capacitance, then we can make sure first up that we have a constant
[00:44:42.900 - 00:44:46.540] current from the solar panel.
[00:44:46.540 - 00:44:54.740] So it provides a completely relatively completely constant current without any ripple.
[00:44:54.740 - 00:44:58.940] And we can make sure that the voltage ripple from the solar panel is very tiny.
[00:44:58.940 - 00:45:05.140] So it's staying as close to that maximum power point as possible under the low conditions
[00:45:05.140 - 00:45:06.140] that we have at the moat.
[00:45:06.140 - 00:45:11.740] So that followed, OK?
[00:45:11.740 - 00:45:14.980] So we've got a couple of expressions that are going to be very, very helpful for the
[00:45:14.980 - 00:45:19.470] design of the back converter for the project.
[00:45:19.470 - 00:45:20.470] Right.
[00:45:20.470 - 00:45:28.060] So in addition to some component values, we need to think of what are the RMS and peak
[00:45:28.060 - 00:45:33.620] currents, what are also the voltages in this circuit.
[00:45:33.620 - 00:45:41.020] For example, if we had 100 volt, 5 amp peak, MOSFET, and we threw it into a converter
[00:45:41.020 - 00:45:50.940] that had 300 volts in the input, and the source current was peaking at 20 amps, then that's
[00:45:50.940 - 00:45:53.020] not going to last very long in that circuit.
[00:45:53.020 - 00:45:57.820] So those sorts of things have to be considered as well.
[00:45:57.820 - 00:46:03.340] At those higher switching frequencies, where there's enough conduction loss to be concerned
[00:46:03.340 - 00:46:08.780] about and potentially switching loss as well for the higher frequencies, you'll be looking
[00:46:08.780 - 00:46:12.380] at introducing what's known as thermal management or thermal control.
[00:46:12.380 - 00:46:16.130] So that's things like heat sinks.
[00:46:16.130 - 00:46:20.130] So hopefully we've come across the concept of heat six before maybe.
[00:46:20.130 - 00:46:24.570] There are the things that we throw on the processes in our computers and so forth to make
[00:46:24.570 - 00:46:28.130] sure that the heat comes out of those in an appropriate manner.
[00:46:28.130 - 00:46:29.130] Right.
[00:46:29.130 - 00:46:30.130] That's heat sinking.
[00:46:30.130 - 00:46:42.290] I don't think I've got enough time to go through the example completely.
[00:46:42.290 - 00:46:47.090] It's a design example.
[00:46:47.090 - 00:46:52.090] Converter application has the following requirements and specifications.
[00:46:52.090 - 00:46:58.090] This is the load average DC voltage and current, eight volts and two amps.
[00:46:58.090 - 00:47:00.090] It's nice that we've got that.
[00:47:00.090 - 00:47:04.090] Input average DC voltage is 12, so it's going to step down from 12 to eight volts.
[00:47:04.090 - 00:47:11.480] Immediately determines then what the duty ratio is.
[00:47:11.480 - 00:47:17.980] Switching frequency you've been told is 80 kilohertz.
[00:47:17.980 - 00:47:24.060] There is a requirement here that the output inductor peak to peak current ripple has to
[00:47:24.060 - 00:47:28.620] be less than the average output current value.
[00:47:28.620 - 00:47:30.820] That's probably the trickiest bit of the whole problem.
[00:47:30.820 - 00:47:33.020] How does that look like?
[00:47:33.020 - 00:47:34.300] So I'll will write that down.
[00:47:34.300 - 00:47:40.540] What I'm going to do is give you a couple of component values but also a fully worked solution
[00:47:40.540 - 00:47:46.060] on learn so that you can review that when you're needed.
[00:47:46.060 - 00:47:56.080] As far as the current is concerned, what that's saying is that we have an average output
[00:47:56.080 - 00:47:58.120] of two amps.
[00:47:58.120 - 00:48:03.020] That's I out.
[00:48:03.020 - 00:48:10.150] The peak to peak current ripple is less than the average output current value.
[00:48:10.150 - 00:48:18.140] So delta I L has to be less than two amps.
[00:48:18.140 - 00:48:24.020] I'm showing going to show the absolute maximum which is two amps.
[00:48:24.020 - 00:48:34.060] So if we've got two amps and delta I L is two amps, then this is one amp and the head
[00:48:34.060 - 00:48:38.580] room we have here is also one amp.
[00:48:38.580 - 00:48:44.740] So the design as defined here is very far away from discontinuous current operation which
[00:48:44.740 - 00:48:46.620] is more usually the case.
[00:48:46.620 - 00:48:48.900] You don't design to be right at the limit.
[00:48:48.900 - 00:48:54.580] You design to be away from that limit.
[00:48:54.580 - 00:48:56.380] So that's what this to say.
[00:48:56.380 - 00:49:02.970] And Dr. Pick to be current ripple is less than the average output current value.
[00:49:02.970 - 00:49:05.170] Okay.
[00:49:05.170 - 00:49:14.540] Just to give you a hand L is going to have to be greater than 16.7 micro Henry.
[00:49:14.540 - 00:49:27.790] C out greater than 39 microfarads and C n is greater than 46 microfarads.
[00:49:27.790 - 00:49:32.590] I will put up the full solution though and how you get to those values.
[00:49:32.590 - 00:49:33.590] Okay.
[00:49:33.590 - 00:49:34.590] That's it for today.

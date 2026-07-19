# ENEL372-26S2 Lecture 2 local ASR transcript

Date: July 16, 2026 3:00pm-3:50pm
Transcript type: Hermes-generated local ASR from validated Echo audio, not a native Echo transcript.
Backend/model: faster-whisper small.en, CPU int8, beam_size=5, vad_filter=True.
Source audio SHA-256: `0ea85b78e5ba88aca54020f1d71d64981d695480875ac1b85f56b6d84b6f84be`
Generated: 2026-07-19T18:36:38.345648+12:00
Caveat: technical terms, equations, names and Māori words may require checking against slides/audio.

[00:00:00.000 - 00:00:08.110] Kia ora koutou, welcome along, my voice sounds really loud.
[00:00:08.110 - 00:00:17.290] Someone want to blow on that projector there to cool it down a little bit?
[00:00:17.290 - 00:00:18.290] Okay.
[00:00:18.290 - 00:00:26.290] Right, so just before we get into the full-blown power electronics converters side of things,
[00:00:26.290 - 00:00:33.690] it's probably a pretty good idea to get a little bit familiar with the sorts of calculations
[00:00:33.690 - 00:00:40.190] and considerations that we're going to make on the analysis side of things as we move through.
[00:00:40.190 - 00:00:46.190] So today we're going to delve into that side of things a little bit,
[00:00:46.190 - 00:00:53.590] understand especially the sort of behavior we're expecting to see with inductors associated with power electronic circuits.
[00:00:53.590 - 00:01:01.790] And then from the next lecture, nice and early tomorrow, that we will start looking at the actual converters themselves.
[00:01:01.790 - 00:01:10.390] And particularly the one that will be utilized that you will design and build yourselves as part of the project this year.
[00:01:10.390 - 00:01:16.870] Right, so we've got circuits that convert electrical power.
[00:01:16.870 - 00:01:24.570] Right, so makes really good sense at this stage that we will look at the important area of the calculations
[00:01:24.570 - 00:01:30.570] that's needed to understand that behavior in our power electronic circuits.
[00:01:30.570 - 00:01:40.470] I do want to emphasize at this point here that when we get into it a bit, the calculations become very set.
[00:01:40.470 - 00:01:44.270] There's not a lot by way of derivation that's needed.
[00:01:44.270 - 00:01:54.070] We do the same things over and over and over again that hopefully, if you kind of pay attention as we go through,
[00:01:54.070 - 00:02:00.470] will start to just be something that you understand and it makes sense as we go through.
[00:02:00.470 - 00:02:09.370] So it's easy at this stage when I'm presenting this material to kind of get lost in the forest for the trees.
[00:02:09.370 - 00:02:17.770] So just be aware that it's not going to always seem particularly difficult on the equation side of things.
[00:02:17.770 - 00:02:20.570] This is kind of introductory power electronics.
[00:02:20.570 - 00:02:28.570] We're trying to get concepts across to a greater extent than confuse people.
[00:02:28.670 - 00:02:38.670] All right, I would highlight at this point that we're trying to make sure that at the end of this lecture,
[00:02:38.670 - 00:02:49.470] one of the key takeaways is how inductors behave when you apply voltage signals to them when they're based in a circuit.
[00:02:49.470 - 00:02:55.270] So there's voltage and of course current goes hand in hand and inductors behave in a particular way
[00:02:55.270 - 00:03:03.670] which really functionalizes our power electronics circuits to do the job that we want them to do.
[00:03:03.670 - 00:03:10.970] So power electronics inductors are king or queen or the head honcho.
[00:03:10.970 - 00:03:20.760] All right, so just be aware of that. Try to keep that in mind as we go through.
[00:03:20.760 - 00:03:27.310] All right, energy and power, instantaneous power.
[00:03:27.310 - 00:03:32.410] So this is something which we sometimes utilize not so often.
[00:03:32.410 - 00:03:38.410] We're mostly looking at average as we'll get onto power, but instantaneous power.
[00:03:38.410 - 00:03:43.410] So a big point here, it's the sort of power that you can identify at an instant in time.
[00:03:43.410 - 00:03:52.510] So we just have power is equal to voltage times time, but all the instantaneous expressions there.
[00:03:52.610 - 00:04:06.210] But we do have the interpretation here or the convention that if this power value is positive in nature or has a positive value,
[00:04:06.210 - 00:04:15.810] means the current will be in the same direction of that positive voltage polarity.
[00:04:15.810 - 00:04:18.410] So if that's the case, then it's an energy source.
[00:04:18.410 - 00:04:25.110] So it provides power to some kind of load. It's an output power.
[00:04:25.110 - 00:04:28.910] If the power, on the other hand, has a negative sign or a negative value,
[00:04:28.910 - 00:04:34.910] then that tells us that the current is in an opposite direction to the positive voltage polarity
[00:04:34.910 - 00:04:38.910] and it will be a sink of energy.
[00:04:38.910 - 00:04:42.510] So it effectively uses power. How does that look?
[00:04:42.510 - 00:04:47.410] Well, I guess the most basic way to interpret this or to look at it,
[00:04:47.410 - 00:04:53.970] is just to have a DC voltage source that has a positive side, right?
[00:04:53.970 - 00:04:59.570] And we'll connect it to this complex circuit of a single resistor.
[00:04:59.570 - 00:05:04.470] We do that, then I think it's pretty clear we will expect there to be current
[00:05:04.470 - 00:05:08.370] in a conventional sense be flowing in that direction.
[00:05:08.370 - 00:05:11.870] All right, so we see by the convention that we're identifying here
[00:05:11.870 - 00:05:19.170] that the positive side of this voltage source has current flowing out through there.
[00:05:19.170 - 00:05:23.570] So it's the same sign as the positive side of the voltage source.
[00:05:23.570 - 00:05:30.470] So this means that we are fully identifying that as being a source of energy
[00:05:30.470 - 00:05:33.070] or a source of power, right?
[00:05:33.070 - 00:05:38.270] And of course, voltage drops around the closed loop equals zero.
[00:05:38.270 - 00:05:42.370] So we have the voltage positive negative with the current flowing that way
[00:05:42.370 - 00:05:47.370] which is the opposite to the positive side of that component, right?
[00:05:47.370 - 00:05:55.330] So being positive, that means that this component is, it uses power.
[00:05:55.330 - 00:05:57.930] That's all fine and good for DC, right?
[00:05:57.930 - 00:06:00.630] And that's great for this course, for the most part,
[00:06:00.630 - 00:06:05.630] because we usually are considering DC, not entirely, but mostly.
[00:06:05.630 - 00:06:11.630] But what about if we have an AC source?
[00:06:11.630 - 00:06:17.130] We won't complicate the circuit at all, but you might be saying to yourself,
[00:06:17.130 - 00:06:21.630] oh, hang on, at various times, instantaneously,
[00:06:21.630 - 00:06:26.830] we might have a positive voltage with respect to this node
[00:06:26.830 - 00:06:30.230] across the voltage source, but another instant in time over a full cycle,
[00:06:30.230 - 00:06:33.130] it could be negative, right? It's AC.
[00:06:33.130 - 00:06:38.830] So what does that mean? Is it, when it's negative, is it actually a sink of power?
[00:06:38.830 - 00:06:41.530] Or is it always a source?
[00:06:41.530 - 00:06:46.830] Well, we need to be thinking about what the current and voltage looks like
[00:06:46.830 - 00:06:48.930] for AC as well, for a system like this.
[00:06:48.930 - 00:06:57.030] So that's what the voltage could look like as far as the current is concerned.
[00:06:57.030 - 00:07:01.530] What we're saying here is that it will be positive when that's positive
[00:07:01.530 - 00:07:09.230] and it will be the same sign when the voltage goes negative, right?
[00:07:09.230 - 00:07:17.030] So in this respect, it is always a source of the power to the circuit,
[00:07:17.030 - 00:07:23.120] even with it being AC and flipping positive to negative.
[00:07:23.120 - 00:07:27.420] Right. Energy.
[00:07:27.420 - 00:07:29.720] On a physics viewpoint, you would actually go with energy first
[00:07:29.720 - 00:07:35.620] and then derive or express power as a time derivative of energy.
[00:07:35.620 - 00:07:39.720] We're going the other way around. Power is usually what we're utilizing.
[00:07:39.720 - 00:07:46.220] So we'll say that energy is the time integral of power.
[00:07:46.220 - 00:07:51.620] Often for energy, we give it a symbol of W, awfully annoying,
[00:07:51.620 - 00:07:57.020] because W is used for defining that we are units of watts, right?
[00:07:57.020 - 00:08:05.020] So it comes from this field where energy was investigated
[00:08:05.020 - 00:08:09.920] as part of mechanical engineering or mechanical physics.
[00:08:09.920 - 00:08:14.420] So we have this concept of work, which is where the W comes from.
[00:08:14.420 - 00:08:23.520] So please do not confuse the symbol for work with the abbreviation for the units of power.
[00:08:23.520 - 00:08:33.170] Usually identified by the fact that the work will be italicized and the units not.
[00:08:33.170 - 00:08:37.570] Of course, for energy, the units are joules.
[00:08:37.570 - 00:08:41.870] Oops. This is the watts.
[00:08:41.870 - 00:08:54.970] The units are joules. Right. Fairly low key for now.
[00:08:54.970 - 00:08:56.670] Average power. All right.
[00:08:56.670 - 00:08:59.370] Now, this is definitely moving into the realms of things
[00:08:59.370 - 00:09:02.270] that we'll be playing around with a bit.
[00:09:02.270 - 00:09:08.570] So you find that in power electronics, we are often switching.
[00:09:08.570 - 00:09:14.570] Well, we're always switching, but we find that we have periodic signals,
[00:09:14.570 - 00:09:16.970] but not necessarily sinusoidal.
[00:09:16.970 - 00:09:22.770] So periodic signals, you might be more conventionally used to seeing
[00:09:22.770 - 00:09:26.170] that being identified with sinusoids.
[00:09:26.170 - 00:09:34.170] But periodic just means that you repeat it with a regular period.
[00:09:34.170 - 00:09:39.070] The average power, basically all we're doing there is we're taking the power,
[00:09:39.070 - 00:09:47.370] the instantaneous power, and averaging it over an entire cycle of period capital T.
[00:09:47.370 - 00:09:50.070] So we can identify that there.
[00:09:50.070 - 00:09:54.970] That's the average of the power for a full cycle of period T.
[00:09:54.970 - 00:10:00.870] So that's where the 1 over T comes from, from term T0 to T0 plus the period
[00:10:00.870 - 00:10:04.570] off that instantaneous power.
[00:10:04.570 - 00:10:06.370] And we've already seen this expression.
[00:10:06.370 - 00:10:10.070] That's just the work.
[00:10:10.070 - 00:10:13.170] So the amount of energy divided by the period.
[00:10:13.170 - 00:10:17.570] Of course, 1 over the period, what's that?
[00:10:17.570 - 00:10:19.870] What do we call that as well?
[00:10:19.870 - 00:10:26.620] That's the frequency. It hurts.
[00:10:26.620 - 00:10:35.390] So we could just as easily have said that that's equal to F times W.
[00:10:35.390 - 00:10:41.090] Quite often, the average power, if you're talking power systems type of space,
[00:10:41.090 - 00:10:46.190] it's also named as real power.
[00:10:46.190 - 00:10:51.490] But as far as we're concerned, we just keep it as being average power.
[00:10:51.490 - 00:10:53.390] The convention doesn't change here.
[00:10:53.390 - 00:10:58.990] If the value of the power is positive, it means that we've got a source of our power.
[00:10:58.990 - 00:11:07.760] And if it's negative, then it means it's a power sink.
[00:11:07.760 - 00:11:09.560] I don't seem to be able to control the volume of this.
[00:11:09.560 - 00:11:11.360] Is that volume for speech all right?
[00:11:11.360 - 00:11:12.460] It's not too loud for people?
[00:11:12.460 - 00:11:16.420] Yeah, okay.
[00:11:16.420 - 00:11:17.620] Oh, nope, I haven't finished.
[00:11:17.620 - 00:11:20.700] Inductors.
[00:11:20.700 - 00:11:21.800] All right.
[00:11:21.800 - 00:11:26.100] Ideal inductors and capacitors.
[00:11:26.100 - 00:11:31.600] Now, I went on about inductors being the head honcho for power electronics,
[00:11:31.600 - 00:11:33.900] which it is, which they are.
[00:11:33.900 - 00:11:39.700] But they kind of need to work with a collaborator.
[00:11:39.700 - 00:11:43.100] And that collaborator primarily is capacitors.
[00:11:43.100 - 00:11:48.600] But we also have our semiconductor switch elements that are key for power electronics.
[00:11:48.600 - 00:11:56.800] But we need to be able to effectively, losslessly store and release energy
[00:11:56.800 - 00:12:00.800] in our power electronics circuits that we're going to maintain a high efficiency,
[00:12:00.800 - 00:12:04.800] which is one of the big key things about power electronics.
[00:12:04.800 - 00:12:09.300] So that's where the inductors and capacitors really hold their own.
[00:12:09.300 - 00:12:16.700] They are solely, if we're talking ideal for this, just at the moment,
[00:12:16.700 - 00:12:22.100] then they are solely energy storage circuit elements.
[00:12:22.100 - 00:12:26.700] All right, so it means that on average, they don't dissipate any amount of power.
[00:12:26.700 - 00:12:33.700] Of course, we know that any real component has a finite part of resistance to them.
[00:12:33.700 - 00:12:36.600] So there's always going to be some loss.
[00:12:36.600 - 00:12:43.300] But just to get this concept across first, we'll just talk about ideal inductors and capacitors.
[00:12:43.300 - 00:12:49.600] Right, they simply store and then subsequently release the energy.
[00:12:49.600 - 00:12:53.820] Never dissipating it.
[00:12:53.820 - 00:13:02.220] The relationships then between, voltage-current relationship between four inductors and capacitors,
[00:13:02.220 - 00:13:06.220] get used to this expression.
[00:13:06.220 - 00:13:11.620] The voltage across an inductor is equal to its inductance value, the constant,
[00:13:11.620 - 00:13:21.380] times the rate of change of current through that inductor, the rate of change.
[00:13:21.380 - 00:13:25.380] And for a capacitor, the current through a capacitor is equal to its capacitance value
[00:13:25.380 - 00:13:30.280] times the rate of change of voltage across that capacitor.
[00:13:30.280 - 00:13:31.780] That's the differential form.
[00:13:31.780 - 00:13:36.180] That's the common way that we normally see these relationships.
[00:13:36.180 - 00:13:39.080] You can, of course, express it in its integral form as well.
[00:13:39.080 - 00:13:44.330] I've just given it there to be complete.
[00:13:44.330 - 00:13:53.160] Of course, instantaneous power is just still equal to voltage times current.
[00:13:53.160 - 00:13:55.760] All right, four inductors and capacitors,
[00:13:55.760 - 00:14:02.060] if we were to determine by the physical parameters involved with those components,
[00:14:02.060 - 00:14:06.560] how much energy any one of those is storing at any instant in time,
[00:14:06.560 - 00:14:09.260] we have these expressions that define that.
[00:14:09.260 - 00:14:16.660] So, these expressions are quite, I guess, informative in a way,
[00:14:16.660 - 00:14:24.660] in telling us in what capacity do these components store energy.
[00:14:24.660 - 00:14:29.860] So, for an inductor, we've got one-half Li squared T.
[00:14:29.860 - 00:14:38.360] So, what that is then identifying to us is that if a conductor of any geometry
[00:14:38.360 - 00:14:43.160] has current flowing through it, then electromagnetically, by that nature,
[00:14:43.160 - 00:14:49.360] it means it is generating a magnetic field that is proportional to that current flow.
[00:14:49.460 - 00:14:55.160] So, this expression is immediately telling us, because we're looking at current,
[00:14:55.160 - 00:15:16.480] that it is a device or component that stores energy in a magnetic field.
[00:15:16.480 - 00:15:28.150] And that magnetic field is created by the current flowing through it.
[00:15:28.150 - 00:15:32.750] But conversely, for capacitors, we can see immediately from this expression
[00:15:32.750 - 00:15:38.650] that we have one-half Cv squared T, that for capacitors,
[00:15:38.650 - 00:15:59.130] the energy then that is stored is in the form of an electric field.
[00:15:59.130 - 00:16:12.890] And that's created by the voltage across the capacitor.
[00:16:12.890 - 00:16:15.590] All right, important things to keep in mind.
[00:16:15.590 - 00:16:18.490] So, if we've got our periodic voltages and currents,
[00:16:18.490 - 00:16:25.490] the special average conditions then associated with inductors and capacitors
[00:16:25.490 - 00:16:27.790] can be summarised here.
[00:16:27.790 - 00:16:29.790] There's a lot of zeros going on.
[00:16:29.790 - 00:16:33.790] So, it means that the average power dissipated by an inductor is equal to zero,
[00:16:33.790 - 00:16:36.290] as it is for a capacitor.
[00:16:36.290 - 00:16:45.290] The average voltage, this is key stuff, the average voltage for a period on period
[00:16:45.290 - 00:16:51.810] for an inductor is equal to zero.
[00:16:51.810 - 00:16:58.310] So, if there is any point in time over a cycle that an inductor voltage is positive,
[00:16:58.310 - 00:17:04.360] then there is going to be a corresponding period of time where it's negative.
[00:17:04.360 - 00:17:13.860] For a capacitor, the mirror of that is the current on average cycle by cycle
[00:17:13.860 - 00:17:18.200] for these periodic signals is equal to zero.
[00:17:18.200 - 00:17:24.200] There's another part that I haven't written down here, which I will annotate now,
[00:17:24.200 - 00:17:29.200] but the reason I didn't write it down is that I want you to pay particular attention to it.
[00:17:29.200 - 00:17:37.180] So, delta the system means change in.
[00:17:37.180 - 00:17:43.680] The change in inductor current, that's an L, please excuse my handwriting at times,
[00:17:43.680 - 00:17:48.680] it does get a bit difficult, is equal to zero.
[00:17:48.680 - 00:17:58.220] Now, that is not the same thing to say that the average current in an inductor is equal to zero.
[00:17:58.220 - 00:18:06.510] You can have a change in current being equal to zero, but not have the average current being zero.
[00:18:06.510 - 00:18:08.010] Think of this.
[00:18:08.010 - 00:18:22.720] So, here's our current in the inductor time, some average DC value,
[00:18:22.720 - 00:18:30.830] but periodically we might have a current that looks like that.
[00:18:30.830 - 00:18:41.740] Alright, so, different color.
[00:18:41.740 - 00:18:48.740] This, from peak to peak, is our delta IL.
[00:18:48.740 - 00:18:59.130] That's the change in current that has to, over cycle by cycle, equal zero.
[00:18:59.130 - 00:19:09.130] In a similar nature, the change in the voltage across the capacitor has to equal zero.
[00:19:09.130 - 00:19:17.130] Once again, voltage, time, there could be a V average,
[00:19:17.130 - 00:19:25.400] but have some random AC part to that voltage,
[00:19:25.400 - 00:19:32.900] but over time, over period by period, so, there's the period,
[00:19:32.900 - 00:19:55.330] the average of that change, delta V, must be equal to zero, change, over a period, it's not equal to zero.
[00:19:55.330 - 00:19:58.330] So, this obviously is not equal to zero, it has a finite value,
[00:19:58.330 - 00:20:11.000] but the average of that over time has to equal zero.
[00:20:11.000 - 00:20:13.500] Are we following with that?
[00:20:13.500 - 00:20:16.930] Okay.
[00:20:16.930 - 00:20:20.930] What it essentially boils down to is this, the area under the curve,
[00:20:20.930 - 00:20:26.930] and over that average must equal the area under it on a cycle by cycle basis.
[00:20:26.930 - 00:20:31.270] Same here.
[00:20:31.270 - 00:20:33.270] Those areas are the same.
[00:20:33.270 - 00:20:45.200] Right, root means square values.
[00:20:45.200 - 00:20:48.200] Kind of gets thrown around about a bit.
[00:20:51.210 - 00:20:58.710] And given this class is a combination of elect and mechatronics and computer engineers,
[00:20:58.710 - 00:21:05.710] I'm not going to take it at the level that I'm expecting the elect students to understand with RMS values.
[00:21:05.710 - 00:21:10.710] I'll just take it right back to the fundamentals here,
[00:21:10.710 - 00:21:19.710] and identify that root mean square values are used to simplify power computations with periodic signals.
[00:21:20.710 - 00:21:33.240] Basically, it's an expression that really quickly allows us to come up with calculations that define the amount of power being used.
[00:21:33.240 - 00:21:39.740] RMS, root mean square, the way you calculate it is all in the name.
[00:21:39.740 - 00:21:48.740] So, you have a parameter, you square it, you take the mean of that, and then you square root that.
[00:21:51.690 - 00:21:56.190] So, we have just the expression for voltage there and current.
[00:21:56.190 - 00:22:01.340] It's the same calculation.
[00:22:01.340 - 00:22:11.540] So, we'll go through a quick example of a common type of periodic signal that we see in power electronics.
[00:22:11.540 - 00:22:26.200] So, it'll be a voltage that we're pulsing, and we'll have dt and t,
[00:22:26.200 - 00:22:45.640] where t is the switching period, remember frequency equals 1 over t,
[00:22:45.640 - 00:22:59.320] and d is the duty cycle, or commonly also called the duty ratio.
[00:22:59.320 - 00:23:02.820] I tend to use duty ratio more than duty cycle,
[00:23:02.820 - 00:23:18.410] and d then is the, or the duty cycle, is the proportion of time that the device is on and presenting power to the output.
[00:23:18.410 - 00:23:40.960] So, very often when a power switch is in its on state, so, and ranges in value between 0 to 1.
[00:23:40.960 - 00:23:47.230] If it's got a value of duty cycle of 1, it's on all the time.
[00:23:47.230 - 00:23:50.230] If it's got a value of 0, it's off. There's no power flow.
[00:23:50.730 - 00:23:56.770] Alright, so that's a very common waveform that we see.
[00:23:56.770 - 00:24:05.180] So, let's use that waveform and first of all determine what is its average value,
[00:24:05.180 - 00:24:09.180] and then also look at what its RMS value is.
[00:24:09.180 - 00:24:23.030] Alright, so 1, the average.
[00:24:23.030 - 00:24:28.030] We were given the expression before, I won't flip back to it, I'll just write it down here.
[00:24:28.530 - 00:24:31.530] There's 1 over t because it's over period t.
[00:24:31.530 - 00:24:41.300] 0 to t off the instantaneous voltage, dt.
[00:24:41.300 - 00:24:44.300] Alright, so we know what the voltage is, it's given there,
[00:24:44.300 - 00:24:52.300] it is a constant of, we'll call that vs, over the time 0 to dt.
[00:24:52.800 - 00:25:05.310] So, 1 over t, then from 0 to not t, but to dt, it's equal to vs, a constant, dt.
[00:25:05.310 - 00:25:18.910] Equals 1 over t, vs, well, the integral of a constant, t between 0 and dt.
[00:25:18.910 - 00:25:26.870] Initial condition, we're taking it as being 0.
[00:25:26.870 - 00:25:30.870] Alright, so if you chuck 0 into the time here, of course that's 0.
[00:25:31.370 - 00:25:40.370] So we're left with dt, 1 over t, vs, dt, of course the t's cancelled,
[00:25:40.370 - 00:25:46.510] equals the duty ratio times the input voltage.
[00:25:46.510 - 00:25:55.510] So, as that duty cycle changes from 0 to 1, some value in between,
[00:25:55.510 - 00:25:58.510] we can tell that the average output voltage from,
[00:25:58.510 - 00:26:09.860] or the average voltage from that, is just that duty ratio times that constant voltage in.
[00:26:09.860 - 00:26:12.360] So what about the RMS value then?
[00:26:12.360 - 00:26:16.360] Is that going to turn out to be the same value?
[00:26:16.360 - 00:26:18.360] Well, we'll check, we'll check, we'll check.
[00:26:18.360 - 00:26:28.170] Okay, 2, so Vrms is the square root of 1 over t, 0,
[00:26:28.170 - 00:26:36.170] we're just going to jump straight to understanding that it's only value of vs from 0 to dt.
[00:26:36.170 - 00:26:43.480] But now it's not the, just vs, it's vs squared, we're squaring that.
[00:26:43.480 - 00:26:45.480] But it's still a constant, we're just squaring the constant, right?
[00:26:45.480 - 00:26:48.980] And then we're going, we've got the integral, we're going to take the square root.
[00:26:48.980 - 00:26:54.980] It's kind of almost, if you took it from there, you might think it's going to come out to the same value.
[00:26:54.980 - 00:27:04.860] Equals square root, 1 over t, vs squared times t, between 0 and dt.
[00:27:04.860 - 00:27:13.860] Okay, equals square root, 1 over t, vs squared, dt.
[00:27:13.860 - 00:27:16.860] Right, t's cancelled, that's good.
[00:27:17.860 - 00:27:27.660] So square root of vs, sure vs, square root of d.
[00:27:27.660 - 00:27:37.640] Okay, since d, we've got 0 less than or equal to d, 0 less than 1,
[00:27:37.640 - 00:27:42.640] means the square root of d is always going to be greater than d.
[00:27:42.640 - 00:27:54.640] So what that's telling us is that the actual RMS value for this waveform is larger than its average.
[00:27:55.140 - 00:28:00.140] And the RMS waveform is the one that, or the RMS value is the one that we would be using to determine
[00:28:00.140 - 00:28:06.140] the actual power that's maybe being dissipated by some load component, like a resistor.
[00:28:06.140 - 00:28:16.300] Not the average, they are different.
[00:28:16.300 - 00:28:20.300] Okay, that's just going through the formal steps to get there.
[00:28:20.300 - 00:28:28.530] There are some common waveforms that you might come across regarding the RMS values.
[00:28:28.530 - 00:28:35.030] So we've just done this rectangular pulse with duty cycle d.
[00:28:35.030 - 00:28:37.530] So, all of a sudden we've gone to Vp.
[00:28:37.530 - 00:28:42.030] So the peak voltage is equal to the source voltage.
[00:28:42.030 - 00:28:58.860] Senusoids, so the RMS voltage is equal to the peak of the senusoid divided by root 2.
[00:28:58.860 - 00:29:12.970] Full wave rectified senusoids, so that's before you do any kind of filtering,
[00:29:12.970 - 00:29:18.320] so they look like that, right?
[00:29:18.320 - 00:29:23.060] Same amplitude, the peak.
[00:29:23.060 - 00:29:26.060] It's hardly surprising that the RMS value is the same, right?
[00:29:26.060 - 00:29:30.060] Because if you square this, you turn it into this.
[00:29:30.060 - 00:29:34.060] But, you know, scaled by the square relationship, right?
[00:29:34.060 - 00:29:41.060] So it becomes peakier, or larger amplitude, but it's still basically the same waveform,
[00:29:41.060 - 00:29:44.060] once you square it.
[00:29:44.060 - 00:29:48.560] So it's, yes, the RMS value is the same as it is for just the senusoid.
[00:29:48.560 - 00:29:58.400] Triangle waves, a very common wave that you will see that we experience in power electronics,
[00:29:58.400 - 00:30:01.400] is the peak voltage over root 3.
[00:30:01.400 - 00:30:12.940] And that's irrespective of the form factor of the triangle wave.
[00:30:12.940 - 00:30:16.940] So that one I've shown has been kind of like a 50% form factor,
[00:30:16.940 - 00:30:21.940] which means that it's completely symmetrical with its slopes.
[00:30:21.940 - 00:30:31.600] We could have one that does something more like this, right?
[00:30:31.600 - 00:30:35.600] Like a sawtooth, instead of a triangle wave like that.
[00:30:35.600 - 00:30:39.600] The expression doesn't change, it's the same value for RMS.
[00:30:39.600 - 00:30:49.290] Triangular wave of any kind will have that RMS value.
[00:30:49.290 - 00:31:03.370] All right, so there are some equations,
[00:31:03.370 - 00:31:07.870] and what I'm going to move on to now is a consideration, then,
[00:31:07.870 - 00:31:13.870] of how we might start to think of the behaviour of our inductors
[00:31:13.870 - 00:31:17.870] associated with switching style circuits,
[00:31:17.870 - 00:31:26.950] particularly if we are going to utilise energy recovery.
[00:31:26.950 - 00:31:37.420] And I actually introduced this circuit and the concept last year in ENL270.
[00:31:37.420 - 00:31:43.420] I'm kind of going over it again, just to solidify again the concept
[00:31:43.420 - 00:31:49.750] of what goes on in these inductors when we're trying to do energy recovery.
[00:31:49.750 - 00:31:54.750] So we've got switching of voltage, current and energy that's stored in inductors
[00:31:54.750 - 00:31:57.250] and hand-in-hand with capacitors.
[00:31:57.250 - 00:31:59.750] And that provides all that functional behaviour that we need,
[00:31:59.750 - 00:32:01.750] so long as we can do that switching.
[00:32:01.750 - 00:32:08.930] And that's where the controlled semiconductor switches come in and the diodes.
[00:32:08.930 - 00:32:12.930] So if we're going to be efficient about the conversion of power, that's stored energy.
[00:32:12.930 - 00:32:15.930] We need to be able to store it, release it,
[00:32:15.930 - 00:32:24.930] and have it pass through the converter without any kind of loss, appreciable loss.
[00:32:24.930 - 00:32:26.930] So we need to recover that energy.
[00:32:26.930 - 00:32:31.930] Now this circuit that we've got shown here, this is actually just one circuit,
[00:32:31.930 - 00:32:37.930] is a great example of how that actually can work in practice
[00:32:37.930 - 00:32:45.340] given the behaviour, the current voltage relationship behaviour of our inductor.
[00:32:45.340 - 00:32:54.340] So we're going to step through and try and determine the operation of the inductor.
[00:32:54.340 - 00:32:56.340] So here's the circuit.
[00:32:56.340 - 00:33:05.340] What we're showing here is that we've got a single DC voltage source from the VCC to ground.
[00:33:05.340 - 00:33:10.340] And leading down here we've got a controlled semiconductor switch,
[00:33:10.340 - 00:33:15.340] it's an N-channel enhancement MOSFET, an inductor,
[00:33:15.340 - 00:33:20.340] and another enhancement MOSFET of the same type, N-channel.
[00:33:20.340 - 00:33:24.340] And they're being switched on and off together at the same time.
[00:33:24.340 - 00:33:26.340] That's what this is identifying here.
[00:33:26.340 - 00:33:29.340] So when it's zero, both are off.
[00:33:29.340 - 00:33:38.450] When it's positive, we call that VG, I guess, the gate voltage.
[00:33:38.450 - 00:33:41.450] When it's positive, both of these are being turned on.
[00:33:41.450 - 00:33:46.450] There is some complexity with the circuits about driving the gates of the MOSFETs,
[00:33:46.450 - 00:33:51.450] which we don't want to include in here because it just muddies the water
[00:33:51.450 - 00:33:53.450] about what we're trying to show.
[00:33:53.450 - 00:33:56.450] So that's why these dotted lines kind of goes,
[00:33:56.450 - 00:34:01.450] just imagine we've got the right sort of circuitry to drive these gates.
[00:34:01.450 - 00:34:04.450] So they both turn on at the same time,
[00:34:04.450 - 00:34:08.450] and they both turn off at the same time.
[00:34:08.450 - 00:34:14.450] Right, then from one side of the inductor we've got a diode
[00:34:14.450 - 00:34:17.450] essentially connected backwards across it,
[00:34:17.450 - 00:34:19.450] and on the other side we have another diode,
[00:34:19.450 - 00:34:24.450] again conventionally just backwards across that component.
[00:34:25.450 - 00:34:28.450] Now when we analyze our power electronic circuits,
[00:34:28.450 - 00:34:31.450] we're going to always approach it in a similar manner,
[00:34:31.450 - 00:34:36.450] and that similar manner is what does the circuit look like when the switch is closed
[00:34:36.450 - 00:34:42.450] and what does the circuit look like and behave like when the switch is open?
[00:34:42.450 - 00:34:46.450] Two states, two separate equivalent circuits.
[00:34:46.450 - 00:34:50.450] So that's what the first diagram here is doing.
[00:34:50.450 - 00:34:54.450] It's saying that these semiconductor devices behave effectively like
[00:34:54.450 - 00:34:58.950] either open or closed switches.
[00:34:58.950 - 00:35:03.950] When we've got VEG going high, then those two transistors are turned on,
[00:35:03.950 - 00:35:09.950] and because we have plus, minus and current flowing this way,
[00:35:09.950 - 00:35:14.950] plus minus VCC because those are dead shorts across the inductor,
[00:35:14.950 - 00:35:23.950] we have plus minus across that diode, so it's reverse biased and won't conduct.
[00:35:23.950 - 00:35:26.950] It's an open circuit.
[00:35:26.950 - 00:35:33.950] And for coming through we have, let's do that one,
[00:35:33.950 - 00:35:40.950] and we have plus VCC to ground, so plus minus across that diode,
[00:35:40.950 - 00:35:45.950] so also reverse biased so it won't conduct, hence shown as an open switch.
[00:35:45.950 - 00:35:53.460] So you've basically just got this VCC across the inductor connected to ground.
[00:35:53.460 - 00:35:55.460] Great.
[00:35:55.460 - 00:36:13.240] So we'll draw that in a, I guess, a more conventional circuit style that's ground.
[00:36:13.240 - 00:36:20.240] I'll label this node A across the inductor, and that one B.
[00:36:20.240 - 00:36:22.240] So that would be A, and that's B.
[00:36:22.240 - 00:36:31.880] We've got the switch current is equal to the inductor current.
[00:36:31.880 - 00:36:37.880] I think we can see why, because it's just a direct connection all the way through IL
[00:36:37.880 - 00:36:42.540] with IS equal to that.
[00:36:42.540 - 00:36:55.540] All right, so we have that voltage current relationship that says VL equals L di by dt,
[00:36:55.540 - 00:37:02.200] where this voltage across the inductor set by the voltage source
[00:37:02.200 - 00:37:08.200] and with current flowing into the positive side of that inductor means that this is a sink of energy.
[00:37:08.200 - 00:37:20.230] We have a constant voltage across that inductor.
[00:37:20.230 - 00:37:23.230] The inductance itself is a constant value.
[00:37:23.230 - 00:37:28.230] It just represents what is the inductance value of that inductor.
[00:37:28.230 - 00:37:44.300] So we've got a constant and a constant, which means di by dt is a constant.
[00:37:44.300 - 00:37:51.300] So what rate of change of a parameter results in a constant value?
[00:37:51.300 - 00:37:58.300] If you take the derivative of something, of a value or a function,
[00:37:58.300 - 00:38:03.300] then what is it to give you a constant from that derivative?
[00:38:03.300 - 00:38:11.060] It's linear, it's a ramp, a linear ramp.
[00:38:11.060 - 00:38:26.390] So when that switch is closed, this current IL is ramping up, constant ramp.
[00:38:26.390 - 00:38:33.630] Hence why I was going over about the triangular waveforms before
[00:38:33.630 - 00:38:40.630] and showed you an example with delta I as being this thing with triangular waveforms.
[00:38:40.630 - 00:38:44.630] That's when the switches are closed.
[00:38:44.630 - 00:38:49.630] Now when we open the switches, what's going to go on?
[00:38:49.630 - 00:38:59.060] Well, we have the situation where we are disconnecting the inductance
[00:38:59.060 - 00:39:05.060] from the source that was providing energy to it.
[00:39:05.060 - 00:39:09.060] So as that current was ramping up, you've got larger and larger current,
[00:39:09.060 - 00:39:15.060] a larger and larger magnetic field is being generated within that inductor.
[00:39:15.060 - 00:39:20.060] And now you've just gone and taken that source away.
[00:39:20.060 - 00:39:29.620] This expression tells us that because that inductor is now energised,
[00:39:29.620 - 00:39:35.620] it has energy, that it will try to keep that current flowing.
[00:39:35.620 - 00:39:39.620] It will also try to keep that current flowing in the same direction
[00:39:39.620 - 00:39:44.250] that was just flowing through it.
[00:39:44.250 - 00:39:47.250] But it's got a finite amount of energy, right?
[00:39:47.250 - 00:39:50.250] It's not a perfect source of current.
[00:39:50.250 - 00:39:54.250] But it will try to keep that current flowing initially at the value
[00:39:54.250 - 00:39:59.250] that had been flowing through it before you turned off the source.
[00:39:59.250 - 00:40:08.070] And if it then requires that state to be made,
[00:40:08.070 - 00:40:13.070] then it stops being a sink of energy and starts being a source of energy.
[00:40:13.070 - 00:40:23.070] So its voltage, this is A and B, its voltage will flip to become a source of energy
[00:40:23.070 - 00:40:27.070] to keep the current flowing in the same direction through it.
[00:40:27.070 - 00:40:34.070] So the current was flowing this way, right, through the inductor with the switches closed.
[00:40:34.070 - 00:40:39.070] And if that current is going to be flowing in the same direction
[00:40:39.070 - 00:40:44.070] and these switches are open, but we've got plus minus,
[00:40:44.070 - 00:40:50.070] then that is exactly the right conditions for these two diodes to forward bias them.
[00:40:50.070 - 00:40:52.070] So this side is negative.
[00:40:52.070 - 00:40:56.070] That means that side is negative with respect to ground
[00:40:56.070 - 00:40:59.070] and allows that to conduct.
[00:40:59.070 - 00:41:03.070] So we have the switch, the diode, on.
[00:41:03.070 - 00:41:07.070] And from this side it's positive.
[00:41:07.070 - 00:41:11.070] It will just ramp up its voltage until it allows that current to flow.
[00:41:11.070 - 00:41:13.070] So this will be positive.
[00:41:13.070 - 00:41:18.070] You've got the diode, so it will be positive, negative, forward biasing it, diode.
[00:41:18.070 - 00:41:20.070] So it turns on.
[00:41:20.070 - 00:41:24.070] And as we can see, the current flow direction is from ground
[00:41:24.070 - 00:41:30.480] through the inductor out through the inductor back into the source.
[00:41:30.480 - 00:41:38.400] So all of that energy that was put into the inductor from the source
[00:41:38.400 - 00:41:45.400] with the switches closed is now fed back into the source with the switches open.
[00:41:45.400 - 00:41:48.400] All of that energy has been recovered.
[00:41:48.400 - 00:41:55.400] That current will ramp down until it reaches the initial value that it had before.
[00:41:55.400 - 00:42:00.340] Why does it ramp down?
[00:42:00.340 - 00:42:02.340] Well, now you've got Vcc across it.
[00:42:02.340 - 00:42:06.340] It's just in the opposite polarity, minus Vcc.
[00:42:06.340 - 00:42:10.340] So it's still a constant voltage across the inductor
[00:42:10.340 - 00:42:12.340] whilst those diodes are conducting.
[00:42:12.340 - 00:42:20.340] Constant voltage, constant inductance, constant di by dt.
[00:42:20.340 - 00:42:22.340] But it's just in the opposite direction.
[00:42:22.340 - 00:42:25.940] It's the negative.
[00:42:25.940 - 00:42:32.940] Not opposite current direction, opposite change in current direction.
[00:42:32.940 - 00:42:34.940] So this was a positive slope.
[00:42:34.940 - 00:42:36.940] This is a negative slope.
[00:42:36.940 - 00:42:44.410] Yeah?
[00:42:44.410 - 00:42:48.410] Okay, so I've described it in a bunch of words there.
[00:42:48.410 - 00:42:50.410] I did draw that circuit.
[00:42:50.410 - 00:42:53.410] So this circuit, if we were to draw it in a conventional sense again,
[00:42:53.410 - 00:42:57.410] it's plus Vcc.
[00:42:58.410 - 00:43:02.410] But now, this circuit, the way that it is,
[00:43:02.410 - 00:43:05.410] we've got the inductor and parallel still,
[00:43:05.410 - 00:43:15.520] but those nodes A and B are around the other way.
[00:43:15.520 - 00:43:20.520] And the current is flowing this way.
[00:43:20.520 - 00:43:27.520] That voltage source has now become a sink of energy in this instance.
[00:43:27.520 - 00:43:32.860] Right, so voltage sources can become, or sources can become sinks
[00:43:32.860 - 00:43:34.860] under the right conditions.
[00:43:34.860 - 00:43:43.130] Then the next slide basically kind of re-emphasizes
[00:43:43.130 - 00:43:45.130] what we've just talked about here.
[00:43:45.130 - 00:43:54.620] So with the transistors on, both of the diodes are reversed biased,
[00:43:54.620 - 00:43:56.620] as I just explained.
[00:43:56.620 - 00:43:59.620] The inductor is being energized by the source.
[00:43:59.620 - 00:44:01.620] So we have Is is equal to,
[00:44:01.620 - 00:44:04.620] the source current is equal to the inductor current.
[00:44:04.620 - 00:44:07.620] The voltage across the inductor is Vcc.
[00:44:07.620 - 00:44:11.620] And if you solve that expression for I L,
[00:44:11.620 - 00:44:14.620] you end up with Vcc times T over L,
[00:44:14.620 - 00:44:20.620] which is that ramping up current with T,
[00:44:20.620 - 00:44:25.620] ramps up with T, with a constant slope of Vcc over L.
[00:44:25.620 - 00:44:41.530] Right, that's solving for I L T, 0 less than T to dT.
[00:44:41.530 - 00:44:43.530] So that's for when the switch is on.
[00:44:43.530 - 00:44:56.020] When the switches are off, when transistors are off,
[00:44:56.020 - 00:44:59.020] V L of T becomes reversed biased, so it's minus Vcc.
[00:44:59.020 - 00:45:02.020] But that I L is in the same direction.
[00:45:02.020 - 00:45:05.020] It's just that it's now collapsing magnetic fields
[00:45:05.020 - 00:45:09.020] so that current will be decreasing over time.
[00:45:09.020 - 00:45:13.380] The diodes are forward biased,
[00:45:13.380 - 00:45:16.380] and at this time if you solve for I L of T,
[00:45:16.380 - 00:45:19.380] you end up with Vcc over L.
[00:45:19.380 - 00:45:28.380] It's the same scaling, but times 2 dT minus T,
[00:45:28.380 - 00:45:34.780] between dT and T.
[00:45:34.780 - 00:45:44.330] Sorry, 2 dT.
[00:45:44.330 - 00:45:51.770] If you look at throwing that in for T, starting at dT,
[00:45:51.770 - 00:45:59.540] then you'll see that that gives us our negative slope.
[00:45:59.540 - 00:46:03.540] So I L now feeds into the source so energy is recovered.
[00:46:03.540 - 00:46:07.540] So here's the inductor current identified,
[00:46:07.540 - 00:46:10.540] but here is the current that the source sees.
[00:46:10.540 - 00:46:12.540] It's providing the energy,
[00:46:12.540 - 00:46:14.540] and then when we turn off those switches,
[00:46:14.540 - 00:46:17.540] that energy is fed back into the source,
[00:46:17.540 - 00:46:26.460] so it flips to being negative for the source.
[00:46:26.460 - 00:46:30.830] If we would look at the inductor voltage,
[00:46:30.830 - 00:46:36.260] we've got dT, it is equal to,
[00:46:36.260 - 00:46:39.260] what's the inductor voltage from 0 to dT?
[00:46:39.260 - 00:46:44.720] I heard someone say it right.
[00:46:44.720 - 00:46:50.080] Vcc.
[00:46:50.080 - 00:46:52.080] And then we turn the switches off,
[00:46:52.080 - 00:47:01.590] and it goes down to minus Vcc until we hit 2 dT.
[00:47:01.590 - 00:47:03.590] The slopes are the same
[00:47:03.590 - 00:47:07.590] because the magnitudes of the voltage are the same.
[00:47:07.590 - 00:47:09.590] Not only that, remember,
[00:47:09.590 - 00:47:12.590] the average voltage across the inductor
[00:47:12.590 - 00:47:15.590] has to equate to 0 cycle by cycle,
[00:47:15.590 - 00:47:21.590] so the area here is equal to the area under the curve,
[00:47:21.590 - 00:47:32.390] under the 0 line.
[00:47:32.390 - 00:47:34.390] Any questions about that?
[00:47:34.390 - 00:47:46.410] We're almost there.
[00:47:46.410 - 00:47:53.140] Okay, so something to consider, though.
[00:47:53.140 - 00:47:56.140] What happens if the energised inductor,
[00:47:56.140 - 00:47:58.140] any energised inductor,
[00:47:58.140 - 00:48:01.140] so it's got current flowing through it,
[00:48:01.140 - 00:48:03.140] and it's a sink of energy,
[00:48:03.140 - 00:48:07.140] what happens if we suddenly open circuit that inductor?
[00:48:07.140 - 00:48:09.140] So what I'm talking about here,
[00:48:09.140 - 00:48:14.150] circuit, we have an inductor,
[00:48:14.150 - 00:48:19.150] and a switch of some sort.
[00:48:19.150 - 00:48:25.150] All right, and it's been in a state where it was closed,
[00:48:25.150 - 00:48:27.150] got current flowing through that inductor,
[00:48:27.150 - 00:48:30.150] it's been plus minus,
[00:48:30.150 - 00:48:35.150] and then we open it.
[00:48:35.150 - 00:48:43.150] So T, V, L, so dT,
[00:48:43.150 - 00:48:51.610] we've got V, S, it's on,
[00:48:51.610 - 00:48:53.610] I, L, whilst it's been on,
[00:48:53.610 - 00:48:57.610] it's ramping up the current,
[00:48:57.610 - 00:49:00.610] and then at this point we're trying to turn it off,
[00:49:00.610 - 00:49:03.610] so rapidly the current goes to 0.
[00:49:03.610 - 00:49:09.610] So we have V, L, equals L, dI, by dT.
[00:49:09.610 - 00:49:14.610] dI by dT here is, for intensive purposes,
[00:49:14.610 - 00:49:25.070] around approximately minus infinity.
[00:49:25.070 - 00:49:30.070] All right, so this is large and negative,
[00:49:30.070 - 00:49:34.070] so this is going to be large and negative.
[00:49:34.070 - 00:49:38.070] So it's going to try shooting off,
[00:49:38.070 - 00:49:44.380] to a very, very, very large negative value.
[00:49:44.380 - 00:49:46.380] So plus minus.
[00:49:46.380 - 00:49:58.920] What do you think's going to happen here?
[00:49:58.920 - 00:50:01.920] Something's going to go bang.
[00:50:01.920 - 00:50:05.920] Whatever switch it is, I don't care what it is,
[00:50:05.920 - 00:50:09.920] it is going to be effectively destroyed
[00:50:09.920 - 00:50:12.920] because the voltage is just going to ramp up
[00:50:12.920 - 00:50:14.920] until that current flows.
[00:50:14.920 - 00:50:16.920] And the only time that current flows
[00:50:16.920 - 00:50:19.920] is if something shorts out here.
[00:50:19.920 - 00:50:21.920] If it's a semiconductor switch,
[00:50:21.920 - 00:50:23.920] you've just destroyed the semiconductor
[00:50:23.920 - 00:50:26.920] within this switch, and it will never work again.
[00:50:26.920 - 00:50:31.920] So this is a condition that we absolutely want to avoid
[00:50:31.920 - 00:50:34.920] in our power electronic circuits.
[00:50:34.920 - 00:50:36.920] That's it for today,
[00:50:36.920 - 00:50:38.920] and I'll see you all again tomorrow.

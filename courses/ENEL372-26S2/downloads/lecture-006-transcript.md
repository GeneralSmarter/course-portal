# ENEL372-26S2 Lecture 6 fast-pass local ASR transcript

Date: July 24, 2026 9:00am-9:55am
Transcript type: Hermes fast-pass local ASR from validated Echo audio, not a native Echo transcript.
Backend/model: faster-whisper tiny.en, CPU int8, beam_size=1, vad_filter=True.
Quality note: fast catch-up transcript. Technical terms, equations, names and Māori words need checking against slides/audio before assessment use.
Source audio SHA-256: `34a8c433473884f8e00d23a91c9fcca5951ce6ff756684fee7b8458477792e84`
Generated: 2026-07-25T00:02:34.665875+12:00

[00:00:03.630 - 00:00:06.030] Well, Kyoto, Kyoto, welcome along.
[00:00:06.030 - 00:00:07.630] We did get started.
[00:00:09.130 - 00:00:11.270] Good job making it this morning.
[00:00:12.270 - 00:00:14.390] Rather, bombing morning for midwinter,
[00:00:14.390 - 00:00:17.190] but I'm not going to complain about that.
[00:00:17.190 - 00:00:19.070] Okay, right.
[00:00:19.070 - 00:00:24.070] So last lecture, we went over some of the design considerations
[00:00:24.750 - 00:00:27.470] that we should be making when we're looking at
[00:00:27.470 - 00:00:29.910] actually getting a buck converter
[00:00:29.910 - 00:00:32.390] and looking at making it.
[00:00:32.390 - 00:00:34.870] There are some things that we need to get right.
[00:00:34.870 - 00:00:37.230] For doing that, the size of the inductance,
[00:00:37.230 - 00:00:39.910] the output filter capacitance,
[00:00:39.910 - 00:00:41.310] the input filter capacitance.
[00:00:41.310 - 00:00:43.150] What frequency we're going to use,
[00:00:43.150 - 00:00:45.150] those sorts of things?
[00:00:45.150 - 00:00:46.950] We're not quite finished yet though
[00:00:46.950 - 00:00:50.590] on the design considerations for our buck converter.
[00:00:50.590 - 00:00:53.630] There's a pretty major element associated
[00:00:53.630 - 00:00:57.710] with the MOSPET switch that we'll be using.
[00:00:58.710 - 00:00:59.990] Very often for buck converters
[00:00:59.990 - 00:01:03.070] and absolutely for the project.
[00:01:03.070 - 00:01:05.670] So we'll go over that now.
[00:01:05.670 - 00:01:09.830] And then we'll move on to another type of DC to DC converter
[00:01:09.830 - 00:01:12.270] which has got a really interesting
[00:01:12.270 - 00:01:15.030] and useful feature associated with it.
[00:01:15.030 - 00:01:15.870] Right.
[00:01:16.670 - 00:01:20.590] So switch, this is the controllable switch,
[00:01:20.590 - 00:01:22.870] which for us is the MOSPET circuit placement.
[00:01:24.550 - 00:01:28.510] Okay, so utilizing MOSPET's for our controllable switch
[00:01:28.510 - 00:01:32.990] is very common practice for mid-sized types
[00:01:32.990 - 00:01:34.390] of DC to DC converters.
[00:01:34.390 - 00:01:37.950] When I say mid-sized and talking about really quite low power,
[00:01:37.950 - 00:01:41.590] just a few watts all the way up to a few killer watts,
[00:01:41.590 - 00:01:43.710] tens of killer watts in size.
[00:01:44.670 - 00:01:45.510] All right.
[00:01:46.830 - 00:01:47.990] If we're going to use MOSPETs,
[00:01:47.990 - 00:01:50.830] we have to consider the control conditions
[00:01:50.830 - 00:01:55.830] that are required to properly switch that MOSPET on and off
[00:01:56.470 - 00:01:58.030] for the application that we have.
[00:01:58.990 - 00:01:59.830] All right.
[00:01:59.830 - 00:02:02.630] So let's start with some practical considerations
[00:02:02.630 - 00:02:04.830] for our MOSPET.
[00:02:05.750 - 00:02:09.190] So we're kind of jumping back to some theory
[00:02:09.190 - 00:02:11.990] that we learned last year in the electronics course
[00:02:11.990 - 00:02:13.310] that I covered and of course,
[00:02:13.310 - 00:02:15.790] since I was such an effective educator,
[00:02:15.790 - 00:02:18.110] let's stuck in your minds like super glue, right?
[00:02:19.470 - 00:02:22.430] Don't worry, we'll go over some of the material again,
[00:02:22.430 - 00:02:23.870] just the refreshment memory.
[00:02:24.950 - 00:02:26.190] Okay.
[00:02:26.230 - 00:02:31.070] So VGS needs to be large enough to turn the MOSPET fully on.
[00:02:31.070 - 00:02:31.910] All right.
[00:02:31.910 - 00:02:32.750] So what am I talking about here?
[00:02:32.750 - 00:02:35.310] Well, here's an in-channel MOSPET.
[00:02:35.310 - 00:02:37.390] Very, very often for power electronics,
[00:02:37.390 - 00:02:41.070] we utilize in-channel enhancement MOSPETs.
[00:02:41.070 - 00:02:48.890] So in-channel enhancement MOSPET,
[00:02:48.890 - 00:02:51.930] basically an enhancement MOSPET is when it is off,
[00:02:51.930 - 00:02:54.330] when there is zero gate to source voltage,
[00:02:54.330 - 00:02:59.250] and fully on when you have an appropriately large DC
[00:02:59.290 - 00:03:00.730] gate to source voltage.
[00:03:00.730 - 00:03:05.730] So gate is the input terminal, control terminal.
[00:03:06.090 - 00:03:10.250] You've got the drain on the top side here
[00:03:10.250 - 00:03:13.810] and the source on the bottom side.
[00:03:13.810 - 00:03:17.250] So current tends to flow when the MOSPET is on
[00:03:17.250 - 00:03:21.100] from drain to source.
[00:03:21.100 - 00:03:21.940] Right.
[00:03:21.940 - 00:03:25.460] So VGS gate to source needs to be large enough
[00:03:25.460 - 00:03:27.340] to turn the MOSPET fully on
[00:03:27.380 - 00:03:29.860] so that you have a very, very low,
[00:03:29.860 - 00:03:32.540] respective resistance-strain to source.
[00:03:32.540 - 00:03:35.260] That's RDS on.
[00:03:35.260 - 00:03:36.100] Right.
[00:03:36.100 - 00:03:38.540] So you will find that in data sheets for these devices,
[00:03:38.540 - 00:03:41.300] and they're usually in the range for modern MOSPETs
[00:03:41.300 - 00:03:45.260] of just tens of milliomes or even less.
[00:03:45.260 - 00:03:46.740] So very small resistance.
[00:03:48.220 - 00:03:50.100] Gate to source,
[00:03:50.100 - 00:03:54.020] X like a small capacitance as a load
[00:03:54.020 - 00:03:56.380] for the input control signal.
[00:03:56.380 - 00:04:00.780] So I did cover this last year as well.
[00:04:00.780 - 00:04:03.100] So that appears,
[00:04:03.100 - 00:04:12.420] gate to source like a little capacitance, CGS.
[00:04:12.420 - 00:04:14.860] So if that's a capacitance,
[00:04:14.860 - 00:04:17.340] and we've got a pulsed circuit coming in.
[00:04:17.340 - 00:04:22.900] So here's our PDWM from zero volts up to, say, around 10,
[00:04:22.900 - 00:04:24.060] volts or so.
[00:04:27.460 - 00:04:29.140] And that's driving into the gate.
[00:04:29.140 - 00:04:31.180] Then it looks like a capacitance
[00:04:31.180 - 00:04:32.580] that it needs to charge up.
[00:04:33.540 - 00:04:37.140] Very rapidly and also discharged rapidly.
[00:04:37.140 - 00:04:39.020] We do have a couple of resistors.
[00:04:39.020 - 00:04:41.260] This is normally identified as being Rg,
[00:04:41.260 - 00:04:43.140] the gate resistance.
[00:04:43.140 - 00:04:44.500] But it is,
[00:04:44.500 - 00:04:45.460] by its nature,
[00:04:45.460 - 00:04:48.140] usually a very small value resistance.
[00:04:48.140 - 00:04:52.100] So only around 10 ohms for the gate resistance.
[00:04:52.100 - 00:04:54.020] It's there as a safeguard,
[00:04:54.020 - 00:04:58.060] a limitation on how high the pulse current is
[00:04:58.060 - 00:05:00.900] to charge up or discharge that capacitance.
[00:05:02.940 - 00:05:06.100] This resistance,
[00:05:08.140 - 00:05:13.140] it's just usually called an R, D,
[00:05:14.180 - 00:05:15.940] or something like R, D,
[00:05:15.940 - 00:05:17.020] this.
[00:05:17.020 - 00:05:21.380] So it's a dissipating resistance.
[00:05:21.380 - 00:05:25.340] It's there to ensure that the MOSFET is in an off state
[00:05:25.340 - 00:05:27.300] if there is no input signal.
[00:05:27.300 - 00:05:30.020] So this charge is that gate capacitance.
[00:05:30.020 - 00:05:32.380] So this R, this.
[00:05:32.380 - 00:05:34.460] But this is usually very large
[00:05:34.460 - 00:05:41.050] around one mega ohm often.
[00:05:41.050 - 00:05:44.370] So the voltage divider that's set up between this
[00:05:44.370 - 00:05:46.050] and this inconsequential.
[00:05:46.050 - 00:05:47.210] You get 10 volts to this side,
[00:05:47.210 - 00:05:52.340] you essentially get 10 volts here.
[00:05:52.340 - 00:05:53.740] Okay.
[00:05:53.740 - 00:05:56.820] So what does that kind of look like waveform wise?
[00:05:56.820 - 00:05:58.500] If you're turning this,
[00:06:00.140 - 00:06:02.980] try to drive this gate on and off quickly.
[00:06:03.260 - 00:06:14.540] So if we go VGS and IG,
[00:06:16.260 - 00:06:19.900] there's IG and draw that here.
[00:06:19.900 - 00:06:25.740] So that's IG.
[00:06:25.740 - 00:06:34.330] We have the situation for the input of here.
[00:06:34.330 - 00:06:38.650] It's VGS, this is where it's off.
[00:06:39.610 - 00:06:42.610] Then we turn it on at 10 volts.
[00:06:43.570 - 00:06:46.410] But rather than go straight up,
[00:06:46.410 - 00:06:49.490] you've got an RC time constant
[00:06:49.490 - 00:06:53.090] associated with the charging up of that capacitance.
[00:06:53.090 - 00:06:57.010] So it will have this behavior that kind of does that.
[00:07:02.890 - 00:07:04.730] And then it will be constant.
[00:07:06.050 - 00:07:08.250] And then when you discharge it,
[00:07:08.250 - 00:07:12.450] we have the RC time constant associated with that.
[00:07:12.450 - 00:07:14.530] Exponential curves.
[00:07:15.290 - 00:07:20.380] So this is on, off again.
[00:07:21.780 - 00:07:25.940] Comes up.
[00:07:25.940 - 00:07:26.780] All right.
[00:07:26.780 - 00:07:31.480] And this is around 10 volts.
[00:07:31.480 - 00:07:34.680] What does the current look like at the same time?
[00:07:34.680 - 00:07:39.680] Well, it's essentially zero when the must fit is off.
[00:07:39.880 - 00:07:42.320] And then we are putting the 10 volts on.
[00:07:43.240 - 00:07:45.920] And with it being in positive direction,
[00:07:45.920 - 00:07:50.200] that current will spike to charge up that capacitance
[00:07:50.240 - 00:07:53.440] to this voltage at the same RC time constant.
[00:07:53.440 - 00:07:56.640] So it'll be a very large initial current.
[00:07:58.120 - 00:08:00.960] But for the time that it gets to being fully on,
[00:08:00.960 - 00:08:06.740] it rapidly decreases back to essentially zero.
[00:08:06.740 - 00:08:08.300] That's the current.
[00:08:08.300 - 00:08:11.820] This can be quite high and for the solar car project,
[00:08:11.820 - 00:08:12.940] you're going to be looking at currents
[00:08:12.940 - 00:08:19.480] that peak up around one or two amps.
[00:08:19.480 - 00:08:20.320] All right.
[00:08:20.320 - 00:08:23.560] And then you get to the point where you turn off the must fit.
[00:08:24.520 - 00:08:26.200] To turn it off rapidly,
[00:08:26.200 - 00:08:28.120] if we've got the right circuitry involved,
[00:08:28.120 - 00:08:30.920] then that current will go negative
[00:08:30.920 - 00:08:34.600] very large spike about the same amplitude,
[00:08:34.600 - 00:08:36.560] but only for a very short period of time.
[00:08:36.560 - 00:08:47.860] And then come back to zero.
[00:08:47.860 - 00:08:50.860] So that signal source that we have,
[00:08:51.780 - 00:08:54.180] driving the must fit on and off,
[00:08:55.100 - 00:08:57.180] quite often the term that we use a driver,
[00:08:58.220 - 00:09:02.580] then it has to be able to source and sync
[00:09:02.620 - 00:09:04.740] high-pulsed currents.
[00:09:04.740 - 00:09:06.860] Not average, large current,
[00:09:06.860 - 00:09:08.900] on average it's very, very small,
[00:09:08.900 - 00:09:13.020] but it has to have the ability to drive high-pulsed currents.
[00:09:13.020 - 00:09:16.980] So it's the output impedance of the signal source
[00:09:16.980 - 00:09:21.140] has to be very low to be able to achieve that.
[00:09:22.380 - 00:09:23.220] All right.
[00:09:24.980 - 00:09:28.540] Okay, let's just some background on MOSFETs
[00:09:28.540 - 00:09:34.290] and driving them on and off.
[00:09:34.290 - 00:09:36.330] All right, let's have a look at our buck converter again.
[00:09:36.730 - 00:09:39.170] The way that we've always looked at it so far.
[00:09:41.210 - 00:09:43.330] The position of the controllable switch here,
[00:09:44.730 - 00:09:49.610] it's a problem for applications such as we have
[00:09:49.610 - 00:09:54.320] for the solar car assignment,
[00:09:54.320 - 00:09:55.520] if we're using a MOSFET.
[00:09:56.760 - 00:10:00.920] I can throw in a couple of extra bits to this diagram
[00:10:00.920 - 00:10:02.960] to just highlight that we're using a MOSFET.
[00:10:02.960 - 00:10:08.310] Here is the, here would be the gate.
[00:10:08.350 - 00:10:09.750] That's the case then.
[00:10:09.750 - 00:10:14.750] This side is the drain and this side is the source.
[00:10:22.960 - 00:10:25.600] To properly turn on that MOSFET,
[00:10:25.600 - 00:10:30.600] we still need a VGS that is around 10 bolts
[00:10:34.150 - 00:10:35.510] to properly turn it on.
[00:10:38.790 - 00:10:43.390] You tell me, if we turning on a MOSFET
[00:10:43.390 - 00:10:47.030] and it's proper on-state,
[00:10:48.630 - 00:10:52.870] what sort of size of voltage drop are we expecting
[00:10:52.870 - 00:10:55.390] from drain to source, but it's properly on?
[00:10:55.390 - 00:10:56.830] Is it a large voltage drop
[00:10:56.830 - 00:10:58.710] or is it a very small voltage drop?
[00:10:59.990 - 00:11:01.390] Very small.
[00:11:01.390 - 00:11:04.350] The RDS on is so small that with the amount of current
[00:11:04.350 - 00:11:05.990] that's flowing through there with it on,
[00:11:05.990 - 00:11:08.270] there is only a little bit of voltage drop.
[00:11:08.310 - 00:11:13.270] So if we have a voltage here sitting on the source
[00:11:15.750 - 00:11:18.270] terminal and this is closed,
[00:11:18.270 - 00:11:20.390] there's almost no voltage drop here,
[00:11:20.390 - 00:11:25.070] then okay, we're connecting VS to this point.
[00:11:25.070 - 00:11:29.710] So VS minus the tiny little fraction.
[00:11:29.710 - 00:11:34.310] So we have a voltage sitting on the source
[00:11:34.350 - 00:11:40.600] that's equal to essentially the input voltage source.
[00:11:40.600 - 00:11:44.120] But the gate voltage has to be around 10 volts higher
[00:11:44.120 - 00:11:46.800] than that to turn on.
[00:11:46.800 - 00:11:51.800] So you've got the negative, you've got VS
[00:11:52.160 - 00:11:57.160] and then you've got VS, VS plus around 10 bolts.
[00:12:00.240 - 00:12:03.120] Where is the extra voltage coming from
[00:12:03.120 - 00:12:04.680] to turn on our MOSFET?
[00:12:04.960 - 00:12:08.080] For the solar car assignment,
[00:12:08.080 - 00:12:10.560] we've got a voltage source from the solar panel.
[00:12:10.560 - 00:12:12.800] That's what's providing this.
[00:12:12.800 - 00:12:17.680] We have no other source of voltage
[00:12:17.680 - 00:12:22.320] to drive that gate to be 10 volts higher
[00:12:22.320 - 00:12:27.690] than the solar panel voltage.
[00:12:27.690 - 00:12:28.530] That's a big problem.
[00:12:28.530 - 00:12:32.930] We either have to come up with some sophisticated circuitry
[00:12:32.930 - 00:12:37.490] that produces its own separate isolated DC supply
[00:12:37.530 - 00:12:40.730] to drive to be able to drive that MOSFET.
[00:12:40.730 - 00:12:43.450] Or we've got to change up the circuit a bit
[00:12:43.450 - 00:12:48.450] to make it compatible with what voltage source we have.
[00:12:48.450 - 00:12:52.460] So from the solar panel.
[00:12:52.460 - 00:12:57.060] All right, so how do we solve the problem?
[00:12:57.060 - 00:12:59.260] Well, we basically use some knowledge
[00:12:59.260 - 00:13:03.660] that we already have about the application as such.
[00:13:03.660 - 00:13:08.660] Like the output for our system is a MOSFET
[00:13:10.420 - 00:13:11.180] at DC motor.
[00:13:11.180 - 00:13:13.460] There are no other electrical connections
[00:13:13.460 - 00:13:18.460] that require any kind of common grounded position
[00:13:20.340 - 00:13:25.060] that relates to the ground coming in from the solar panel.
[00:13:26.780 - 00:13:29.900] For DC motors, just so long as it gets its voltage
[00:13:29.900 - 00:13:32.940] to end current, then it doesn't need to have
[00:13:32.940 - 00:13:39.040] any other earth-referenced common.
[00:13:39.320 - 00:13:43.240] Also, we know that for series circuits,
[00:13:44.600 - 00:13:47.600] series-connected circuits, the same current will flow
[00:13:47.600 - 00:13:56.170] through all of the series-connected components.
[00:13:56.170 - 00:13:58.890] Right, with those two things in mind,
[00:13:58.890 - 00:14:03.890] what we can do is we can take the switch from where it is,
[00:14:04.330 - 00:14:07.130] and this is known as a high-side position switch
[00:14:07.130 - 00:14:10.530] because one of the terminals for the switch is connected
[00:14:10.530 - 00:14:13.050] to the positive off the supply.
[00:14:13.090 - 00:14:16.490] So it's setting on what's called the high-side position.
[00:14:17.450 - 00:14:20.450] We can take that knowing that we have,
[00:14:23.860 - 00:14:27.100] if the switch is closed, we have IS flowing through there,
[00:14:27.100 - 00:14:34.190] we have IS there, the source current.
[00:14:34.190 - 00:14:36.670] With that switch closed, that FET is open.
[00:14:36.670 - 00:14:39.790] So we've got the series-connected through to here.
[00:14:39.790 - 00:14:41.590] Sure, these are parallel, they split the current,
[00:14:41.590 - 00:14:43.870] but once they get back to the bottom here,
[00:14:43.870 - 00:14:48.990] this is IS flowing here.
[00:14:49.030 - 00:14:53.990] So we can take the switch and take from the high-side position
[00:14:54.310 - 00:15:00.870] and move it to the low-side position
[00:15:00.870 - 00:15:03.630] because we don't have to have this negative
[00:15:03.630 - 00:15:08.630] at the same node position as this negative.
[00:15:10.070 - 00:15:11.630] That's what we're seeing here.
[00:15:12.990 - 00:15:20.700] So here's our node, which would be our motor.
[00:15:20.700 - 00:15:23.620] All right, with its negative.
[00:15:23.620 - 00:15:27.260] And then we have our controllable switch
[00:15:27.260 - 00:15:29.580] that's being driven by oscillate modulation
[00:15:29.580 - 00:15:36.410] with this being the negative for our the panel.
[00:15:43.860 - 00:15:48.820] This ground and this negative is not the same electrically
[00:15:48.820 - 00:15:52.620] as this one because when this MOSPET is off,
[00:15:52.620 - 00:15:53.980] that's open-circuited.
[00:15:54.900 - 00:15:56.460] That's like that's out of the circuit.
[00:15:56.460 - 00:15:58.340] So this becomes disconnected.
[00:15:59.220 - 00:16:00.980] These two nodes become disconnected.
[00:16:00.980 - 00:16:04.260] So they're not the same.
[00:16:04.260 - 00:16:07.060] Here, the two nodes are always,
[00:16:07.060 - 00:16:08.700] or the node is always connected.
[00:16:08.700 - 00:16:12.380] So your output voltage is always connected
[00:16:12.380 - 00:16:18.400] to the same commonness, the input voltage source.
[00:16:18.400 - 00:16:23.140] All right, so here we would have IS,
[00:16:23.140 - 00:16:26.020] IS, and IS.
[00:16:27.020 - 00:16:29.740] It's series-connected, we're just moving its position
[00:16:29.740 - 00:16:31.420] from high to low.
[00:16:31.420 - 00:16:32.900] How does that solve the position?
[00:16:32.900 - 00:16:35.620] The problem, well, when we turn this MOSPET on,
[00:16:35.620 - 00:16:38.060] we need a gate to source voltage.
[00:16:39.780 - 00:16:41.620] That's around 10 volts.
[00:16:41.620 - 00:16:43.620] So that's gate to source.
[00:16:43.620 - 00:16:48.620] The source is now referenced to the panel negative.
[00:16:49.620 - 00:16:53.020] So the panel voltage is going to be something like 15,
[00:16:53.020 - 00:16:55.020] 16, 17 volts.
[00:16:55.020 - 00:16:59.500] So we already have the required voltage headroom
[00:16:59.500 - 00:17:01.580] to be able to drive that MOSPET fully on.
[00:17:02.580 - 00:17:07.460] But we don't need any special hour supply circuitry
[00:17:07.460 - 00:17:14.600] to create a separate isolated 10 volts supply.
[00:17:14.600 - 00:17:15.960] Are we following that?
[00:17:15.960 - 00:17:19.670] Any questions?
[00:17:19.670 - 00:17:21.110] It's a bit of a leap.
[00:17:21.110 - 00:17:26.670] But this is definitely the sort of, I guess,
[00:17:26.670 - 00:17:29.550] solution that is most often employed
[00:17:29.550 - 00:17:31.870] for these types of converters.
[00:17:31.870 - 00:17:36.070] So long as we have that ability to have the output load
[00:17:36.070 - 00:17:42.640] at a different negative reference to the input source,
[00:17:42.640 - 00:17:44.880] which is what we do have for when you're driving motors
[00:17:44.880 - 00:17:52.820] and things like that.
[00:17:52.820 - 00:17:56.540] Right.
[00:17:56.540 - 00:17:59.820] So we're up to a point now where we could consider, OK,
[00:17:59.820 - 00:18:05.380] well, how are we going to utilize our controller, I see,
[00:18:05.380 - 00:18:11.580] the TL-494 to do this job for the low side MOSPET gate
[00:18:11.580 - 00:18:17.600] driving.
[00:18:17.600 - 00:18:19.600] So this is just the functional block diagram
[00:18:19.600 - 00:18:35.470] from the datasheet for the TL-
[00:18:35.470 - 00:18:36.230] for the function of the circuit.
[00:18:36.230 - 00:18:40.910] The PWM that we need for controlling our back converter
[00:18:40.910 - 00:18:44.470] is outputted via these two.
[00:18:44.470 - 00:18:46.110] You can choose just to use one.
[00:18:46.110 - 00:18:49.590] But via these two BJTs.
[00:18:49.590 - 00:18:58.550] They're low power BJTs, maximum i, e, max.
[00:18:58.550 - 00:19:02.150] It's around 200 milliamps.
[00:19:02.150 - 00:19:04.870] So that's the most amount of current
[00:19:04.870 - 00:19:13.240] that you can get out of it at even under pulse conditions.
[00:19:13.240 - 00:19:19.500] They are used, as I said, to generate that PWM output.
[00:19:19.500 - 00:19:20.780] Some of the other functional blocks
[00:19:20.780 - 00:19:24.780] that will be important for you to get to just your head
[00:19:24.780 - 00:19:28.780] around, but implement for the converter.
[00:19:28.780 - 00:19:32.700] RTCT pins on the IC.
[00:19:32.700 - 00:19:35.900] That's where you set the switching frequency
[00:19:35.900 - 00:19:38.100] for your converter.
[00:19:38.100 - 00:19:41.860] You might choose 50 kilohertz, you might choose 90 kilohertz,
[00:19:41.860 - 00:19:44.020] whatever.
[00:19:44.020 - 00:19:46.140] You need to choose the right value of resistance
[00:19:46.140 - 00:19:50.660] and capacitance for RTCT to give that frequency
[00:19:50.660 - 00:19:51.820] for switching.
[00:19:51.820 - 00:20:00.710] It's an internal sawtooth oscillator.
[00:20:00.710 - 00:20:06.950] We also have a reference source from the IC.
[00:20:06.950 - 00:20:09.470] So it will output from the reference pin
[00:20:09.470 - 00:20:13.070] a fixed value of voltage.
[00:20:13.070 - 00:20:16.310] So you use that voltage then to identify
[00:20:16.310 - 00:20:18.110] with the control system.
[00:20:18.110 - 00:20:22.190] What is your ordered voltage for the control system?
[00:20:22.190 - 00:20:25.310] So that's telling the control, what
[00:20:25.310 - 00:20:28.510] is your maximum power point voltage?
[00:20:28.510 - 00:20:30.510] So you tell the control system, this is the voltage
[00:20:30.510 - 00:20:33.430] that we want to have for our maximum power point.
[00:20:33.430 - 00:20:35.990] You generate that from the reference signal.
[00:20:35.990 - 00:20:40.710] It's a scaled down voltage of what you will determine
[00:20:40.710 - 00:20:46.070] as being your maximum power point voltage for the solar panel.
[00:20:46.070 - 00:20:47.390] That's what that's for.
[00:20:47.390 - 00:20:50.070] And then we have our error amplifiers.
[00:20:50.070 - 00:20:54.870] So this is a key part of the feedback part of the control
[00:20:54.870 - 00:20:55.630] system.
[00:20:55.630 - 00:20:59.590] You have your PIA constants that you set up.
[00:20:59.590 - 00:21:01.870] And then you feed this into the error amplifier,
[00:21:01.870 - 00:21:03.350] which is you an error app depending
[00:21:03.350 - 00:21:06.870] on how close you are to your ordered value.
[00:21:06.870 - 00:21:11.270] So you measure the output, how close are we to our ordered value?
[00:21:11.270 - 00:21:13.030] That's done with those.
[00:21:13.030 - 00:21:14.470] You only use one of them.
[00:21:14.470 - 00:21:16.430] They've got the ability to have two.
[00:21:16.430 - 00:21:21.950] if you're only using one of those error amplifiers.
[00:21:21.950 - 00:21:25.030] OK, so but the big part is that there
[00:21:25.030 - 00:21:28.150] is no connection from the emitter to collector
[00:21:28.150 - 00:21:31.150] for the output of those BJTs.
[00:21:31.150 - 00:21:36.270] You have to set it up to be an appropriate amplifier
[00:21:36.270 - 00:21:39.070] for the output.
[00:21:39.070 - 00:21:40.950] So how could we do that?
[00:21:40.950 - 00:21:48.980] Well, one solution is shown here.
[00:21:48.980 - 00:21:52.180] So you have the solar panel, this is the order of 15 volts.
[00:21:52.180 - 00:21:53.740] It might be lower light conditions.
[00:21:53.740 - 00:21:55.460] Only give you 15 volts.
[00:21:55.460 - 00:21:59.740] Here's our filter capacitor before we get to the,
[00:21:59.740 - 00:22:03.380] this is our V panel.
[00:22:03.380 - 00:22:10.100] And that goes to the buck converter input.
[00:22:10.100 - 00:22:15.020] So that's your DC supply into the buck converter.
[00:22:15.020 - 00:22:19.620] You tap off that from your TL4 94, your control IC.
[00:22:19.620 - 00:22:23.340] And here's one of the output BJTs.
[00:22:23.340 - 00:22:25.260] It's an MPM BJT.
[00:22:25.260 - 00:22:28.180] So I've just shown the MPM BJT down here.
[00:22:28.180 - 00:22:30.540] It's just the current control current device.
[00:22:30.540 - 00:22:32.500] It's current amplifier.
[00:22:32.500 - 00:22:36.620] So but with the maximum current that you're allowed
[00:22:36.620 - 00:22:40.420] at the output to be around 200 milliamps.
[00:22:40.420 - 00:22:44.140] OK, so here's your that effective load
[00:22:44.140 - 00:22:48.220] that the pulse width modulator signal sees.
[00:22:48.220 - 00:22:51.740] It's the gate capacitance for the MOSFET.
[00:22:51.740 - 00:22:53.820] So we're just representing that with the capacitor.
[00:22:53.820 - 00:22:57.340] This is really the input or the gate
[00:22:57.340 - 00:23:00.700] terminal of your MOSFET.
[00:23:00.700 - 00:23:03.740] But we've got to resist here and another one here.
[00:23:03.740 - 00:23:07.780] So do we remember with the BJT set up here
[00:23:07.780 - 00:23:12.140] with the collector directly connected to VCC or B panel
[00:23:12.140 - 00:23:15.380] and the output taken off the emitter?
[00:23:15.380 - 00:23:24.450] Do we remember what kind of amplifier we call that?
[00:23:24.450 - 00:23:27.450] It's a common collector amplifier.
[00:23:27.450 - 00:23:30.290] So taking your output off the emitter
[00:23:30.290 - 00:23:34.810] means that it's a non inverting amplifier.
[00:23:34.810 - 00:23:38.410] What you get on the input is what you get on the output
[00:23:38.410 - 00:23:41.330] as far as phase is concerned.
[00:23:41.330 - 00:23:42.650] Raise the input current.
[00:23:42.650 - 00:23:45.650] You get a higher output current.
[00:23:45.650 - 00:23:48.980] OK, it's non inverting.
[00:23:48.980 - 00:23:51.260] We're in it's where it's a common collector.
[00:23:51.260 - 00:23:53.980] So you're taking your output from the emitter.
[00:23:53.980 - 00:23:55.660] All right.
[00:23:55.660 - 00:24:03.150] So IJON, you turn this on.
[00:24:03.150 - 00:24:05.910] You have a resist here that limits that current to a maximum
[00:24:05.910 - 00:24:09.190] of 200 milliamps.
[00:24:09.190 - 00:24:12.790] OK, so you charge up the capacitor with a current that's
[00:24:12.790 - 00:24:16.550] somewhat less than ideal if we want to really turn that MOSFET
[00:24:16.550 - 00:24:17.550] on fast.
[00:24:17.550 - 00:24:20.950] We want to turn it on fast, which helps with efficiency.
[00:24:20.950 - 00:24:23.670] So I wanted to turn them on and off fast.
[00:24:23.670 - 00:24:26.990] Then we want to get away with a larger pulse current than that.
[00:24:26.990 - 00:24:31.350] It gets even worse when we want to turn the MOSFET off.
[00:24:31.350 - 00:24:35.710] So to turn it off, we, the pulse width modulation,
[00:24:35.710 - 00:24:37.870] turns this transistor off.
[00:24:37.870 - 00:24:41.070] And it just goes high impedance.
[00:24:41.070 - 00:24:43.390] So in order to discharge this capacitor,
[00:24:43.390 - 00:24:46.110] you need to have another resistance
[00:24:46.110 - 00:24:49.750] to allow that current pathway down to ground.
[00:24:49.750 - 00:24:53.190] This resistance has to be large enough
[00:24:53.190 - 00:24:56.270] to make sure that the current when you've got this turned on,
[00:24:56.270 - 00:24:58.750] that splits between here and here,
[00:24:58.750 - 00:25:00.830] doesn't exceed 200 milliamps.
[00:25:00.830 - 00:25:05.270] So the turn off is going to be because you've now got two series
[00:25:05.270 - 00:25:11.690] connected resistors is going to be quite slow.
[00:25:11.690 - 00:25:18.040] So not ideal whatsoever.
[00:25:18.040 - 00:25:24.490] It'll work, but we could do better.
[00:25:24.490 - 00:25:26.650] What's better?
[00:25:26.650 - 00:25:31.410] Once again, following on from what I taught last year in the E&L 270,
[00:25:31.410 - 00:25:45.820] we could use a CMOS inverter, a CMOS inverter.
[00:25:45.820 - 00:25:50.840] You drive the input with your PWM.
[00:25:50.840 - 00:25:58.760] And the output, the PMOS will turn on when the signal is low.
[00:25:58.760 - 00:26:04.240] And the NMOS will turn on when the input signal is high.
[00:26:04.240 - 00:26:06.680] And both those states, the impedance
[00:26:06.680 - 00:26:10.920] drain to source, drain to source, is very low.
[00:26:10.920 - 00:26:22.800] Hello, output impedance.
[00:26:22.800 - 00:26:26.520] And both states, which means that it can source and sync
[00:26:26.520 - 00:26:43.090] very high pulse currents, which is great for doing the job
[00:26:43.090 - 00:26:47.330] of turning on and off that MOS bit fast.
[00:26:47.330 - 00:26:51.970] We still need a gate resistance to limit the absolute peak current.
[00:26:51.970 - 00:26:55.810] But as I said, this is going to be around 10 ohms.
[00:26:55.810 - 00:26:58.310] But we still need a resistor that
[00:26:58.310 - 00:27:05.520] are disks to make sure that if there is no input signal,
[00:27:05.520 - 00:27:07.800] that the MOS bit is in its off state.
[00:27:07.800 - 00:27:11.760] It's a more of a safety feature than anything else.
[00:27:11.760 - 00:27:13.840] So this is very large.
[00:27:15.380 - 00:27:16.940] It could be something that, like I said,
[00:27:16.940 - 00:27:21.890] still in the mega-home region.
[00:27:21.890 - 00:27:27.850] Can anyone at this stage, if you've got kind of switched on here,
[00:27:27.850 - 00:27:32.050] anyone kind of see a potential problem
[00:27:32.050 - 00:27:38.840] with using the CMOS inverter?
[00:27:38.840 - 00:27:46.340] And it has to do with the logic.
[00:27:46.340 - 00:27:49.140] In control, feedback, yes.
[00:27:49.140 - 00:27:56.780] So your duty ratio on to off gets inverted by going through
[00:27:56.780 - 00:27:58.540] an inverter.
[00:27:58.540 - 00:27:59.980] That's going to be problematic if you're
[00:27:59.980 - 00:28:04.660] doing feedback control to make sure it's maintaining a certain level.
[00:28:04.660 - 00:28:08.180] We don't want it to be inverted.
[00:28:08.180 - 00:28:12.420] How are we going to address that?
[00:28:12.420 - 00:28:16.390] Do you think?
[00:28:16.390 - 00:28:17.910] Sorry?
[00:28:17.910 - 00:28:19.670] Add another one.
[00:28:19.670 - 00:28:22.110] Essentially, yes.
[00:28:22.110 - 00:28:23.230] Essentially, yes.
[00:28:23.230 - 00:28:33.340] What we're going to do is in that previous situation,
[00:28:33.340 - 00:28:36.500] where we've got this as a non-inverting amplifier,
[00:28:36.500 - 00:28:43.860] we're going to set up the output VJT as an inverting amplifier.
[00:28:43.860 - 00:28:44.860] How do we do that?
[00:28:44.860 - 00:28:47.460] Well, it's pretty simple really.
[00:28:47.460 - 00:28:54.140] So we have our output transistor.
[00:28:54.140 - 00:28:56.580] Before we had a resistor to ground,
[00:28:56.580 - 00:29:00.040] and we took the output from here.
[00:29:00.040 - 00:29:05.040] Do we remember what the inverting amplifier was called for BJTs?
[00:29:05.040 - 00:29:07.680] We just had the common collector.
[00:29:07.680 - 00:29:09.760] What's the first one we looked at?
[00:29:09.760 - 00:29:13.040] The common emitter.
[00:29:13.040 - 00:29:17.640] So we have that grounded, and we have a resistor here.
[00:29:17.640 - 00:29:20.280] Here's V panel.
[00:29:20.280 - 00:29:22.160] So this is our RC.
[00:29:22.160 - 00:29:26.000] And we take the output instead from here.
[00:29:26.000 - 00:29:30.800] That is the inverted PWM.
[00:29:30.800 - 00:29:35.120] So we take the inverted PWM and inverse it.
[00:29:35.120 - 00:29:36.880] So by the time we get to the MOSFET,
[00:29:36.880 - 00:29:40.200] it is now a non-inverting PWM.
[00:29:40.200 - 00:29:48.050] So we're just going to be careful about that when we design
[00:29:48.050 - 00:29:54.330] the circuit for driving the MOSFET for our solica.
[00:29:54.330 - 00:29:59.810] You need to make sure that you configure the output PWM VJT
[00:29:59.810 - 00:30:05.170] to take it from the inverting output side, from the collector.
[00:30:05.170 - 00:30:08.250] C-E.
[00:30:08.250 - 00:30:09.410] Yeah?
[00:30:09.410 - 00:30:10.330] Great.
[00:30:10.330 - 00:30:12.610] Because this is a requirement for the project.
[00:30:12.610 - 00:30:15.730] You must use a C-MOSM inverter to drive the gate.
[00:30:15.730 - 00:30:17.010] It's not up to you.
[00:30:17.010 - 00:30:21.050] It's a requirement of the design.
[00:30:21.050 - 00:30:26.540] So make sure you try and get that right.
[00:30:26.540 - 00:30:27.380] OK.
[00:30:27.380 - 00:30:33.270] Any other questions there at the moment?
[00:30:33.270 - 00:30:41.240] Clear?
[00:30:41.240 - 00:30:45.440] So with that last bit of information,
[00:30:45.440 - 00:30:51.640] you now have enough theory about a converter design
[00:30:51.640 - 00:30:54.600] S related to the solica project
[00:30:54.600 - 00:31:01.000] to come up with a framework of calculations
[00:31:01.000 - 00:31:06.630] and formulate that you can apply for that design.
[00:31:06.630 - 00:31:07.910] So you can start thinking about what
[00:31:07.910 - 00:31:10.110] do I want for my switching frequency.
[00:31:10.110 - 00:31:14.830] We've got some rough idea of the range of motor currents
[00:31:14.830 - 00:31:18.670] so we can come up with some rough ball park duty ratio
[00:31:18.670 - 00:31:19.910] figures.
[00:31:19.910 - 00:31:23.910] We know how to calculate output capacitance, input
[00:31:23.910 - 00:31:28.790] capacitance, inductive value, minimum inductive value.
[00:31:28.790 - 00:31:31.390] Getting all of those kind of the framework
[00:31:31.390 - 00:31:35.310] for those calculations set in place,
[00:31:35.310 - 00:31:40.630] leading up to doing some simulation work on LT spice.
[00:31:40.630 - 00:31:40.870] OK.
[00:31:40.870 - 00:31:42.870] So don't hang back.
[00:31:42.870 - 00:31:43.670] Jump into it.
[00:31:43.670 - 00:31:49.600] Now you have enough background theory.
[00:31:49.600 - 00:31:50.920] Right.
[00:31:50.920 - 00:31:56.120] Having said that, let's move on to a new type of DC
[00:31:56.120 - 00:32:00.080] converter that has a rather interesting and quite useful
[00:32:00.080 - 00:32:03.640] function.
[00:32:03.640 - 00:32:06.360] And there's a boost converter.
[00:32:06.360 - 00:32:07.440] Right.
[00:32:07.440 - 00:32:10.240] The actual circuit itself doesn't really
[00:32:10.240 - 00:32:12.240] look a lot different to a back converter.
[00:32:12.240 - 00:32:12.920] That's it.
[00:32:12.920 - 00:32:14.560] It's got a power inductor.
[00:32:14.560 - 00:32:16.120] It's got a diode.
[00:32:16.120 - 00:32:18.120] A filter capacitor, just a resistor load,
[00:32:18.120 - 00:32:20.280] and a controllable switch.
[00:32:20.280 - 00:32:24.640] All we've done is rearranged where they appear
[00:32:24.640 - 00:32:28.480] in the circuit a little bit.
[00:32:28.480 - 00:32:33.300] The result of that is quite significant.
[00:32:33.300 - 00:32:39.340] So a boost converter by its name is a converter that
[00:32:39.340 - 00:32:45.700] will output a voltage that is greater than the source
[00:32:45.700 - 00:32:47.300] voltage.
[00:32:47.300 - 00:32:49.820] So it's not a step down converter, like a back converter
[00:32:49.820 - 00:32:50.060] is.
[00:32:50.060 - 00:32:55.120] It is a step up converter for voltage.
[00:32:55.120 - 00:33:00.480] This is a function that unless you do some quite tricky stuff,
[00:33:00.480 - 00:33:06.360] you cannot achieve with linear regulators.
[00:33:06.360 - 00:33:10.060] So this all has to do with this behavior
[00:33:10.060 - 00:33:16.200] of the power inductor when we have current flowing through it
[00:33:16.200 - 00:33:20.400] and then what it needs to do to release that energy
[00:33:20.400 - 00:33:25.070] and the voltage effect from that.
[00:33:25.070 - 00:33:25.590] Right.
[00:33:25.590 - 00:33:26.910] DC to DC converters.
[00:33:26.910 - 00:33:29.150] When we analyze the boost converter now,
[00:33:29.150 - 00:33:32.190] we are going to keep the same assumptions
[00:33:32.190 - 00:33:35.270] that we've had for steady state operation
[00:33:35.270 - 00:33:36.590] that we did for our back converter.
[00:33:36.590 - 00:33:40.950] So inductor current fluctuations are periodic.
[00:33:40.950 - 00:33:42.790] The average inductor voltage is 0.
[00:33:42.790 - 00:33:44.910] This is a fundamental property of inductors
[00:33:44.910 - 00:33:47.150] that doesn't change depending on what
[00:33:47.150 - 00:33:49.830] converter it's placed in.
[00:33:49.830 - 00:33:51.790] The average capacitor current is 0 again.
[00:33:51.790 - 00:33:56.150] A fundamental property of capacitors that's unchanged.
[00:33:56.150 - 00:33:57.590] The power supplied by the source equals
[00:33:57.590 - 00:34:00.470] about to the load plus any non-ideal sources,
[00:34:00.470 - 00:34:02.310] which for the first part we're going to assume
[00:34:02.310 - 00:34:05.110] is essentially 0 for those losses.
[00:34:05.110 - 00:34:09.550] So it's 100% efficient converter.
[00:34:09.550 - 00:34:11.430] And the filter capacitor is large enough
[00:34:11.430 - 00:34:15.390] to make any kind of voltage fluctuations or ripple
[00:34:15.390 - 00:34:20.390] at the output effectively negligible for the analysis
[00:34:20.390 - 00:34:29.910] that we're going to carry out initially.
[00:34:29.910 - 00:34:30.350] OK.
[00:34:30.350 - 00:34:34.310] So we will be analyzing this boost converter circuit
[00:34:34.310 - 00:34:37.550] exactly as we have done for the back converter.
[00:34:37.550 - 00:34:40.670] What does the circuit look like in behavior when the switch
[00:34:40.670 - 00:34:42.470] is closed?
[00:34:42.470 - 00:34:44.550] What does the circuit look like in behavior
[00:34:44.550 - 00:34:47.350] like when the switch is open?
[00:34:47.350 - 00:34:53.950] Right.
[00:34:53.950 - 00:34:57.790] With that controlled switch, when we close it,
[00:34:57.790 - 00:34:58.470] here it is here.
[00:34:58.470 - 00:35:03.430] So that's the position of the switch and its closed state.
[00:35:03.430 - 00:35:08.990] Then the diode and its position becomes reverse biased.
[00:35:08.990 - 00:35:12.870] So here's the diode and its the direction.
[00:35:12.870 - 00:35:17.550] So we can see here that with this side connected to the negative
[00:35:17.550 - 00:35:20.230] and this side connected to V out, which is a positive,
[00:35:20.230 - 00:35:22.710] that's plus minus across that diode.
[00:35:22.710 - 00:35:23.750] So it's reverse biased.
[00:35:23.750 - 00:35:29.350] It's off and open circuit.
[00:35:29.350 - 00:35:32.590] So that means we're just looking at this side
[00:35:32.590 - 00:35:36.270] that the inductor is directly connected
[00:35:36.270 - 00:35:43.080] across the terminals of the power supply, the voltage source.
[00:35:43.080 - 00:35:46.680] The voltage current relationship for an inductor
[00:35:46.680 - 00:35:49.000] v equals L di by dt.
[00:35:49.000 - 00:35:51.320] That's the fundamental property.
[00:35:51.320 - 00:35:53.160] But with that closed, the voltage
[00:35:53.160 - 00:35:59.100] across the inductor is a constant at VS.
[00:35:59.100 - 00:36:05.360] So di by dt is VS over L constant constant.
[00:36:05.360 - 00:36:08.240] So we've got that state that occurs again kind of like
[00:36:08.240 - 00:36:10.640] with our back converter with a constant voltage drop
[00:36:10.640 - 00:36:13.000] across the inductor.
[00:36:13.000 - 00:36:15.520] So we expect the current to be ramping.
[00:36:15.560 - 00:36:20.040] And linear ramp, whilst that switch is closed.
[00:36:20.040 - 00:36:21.400] It is receiving energy.
[00:36:21.400 - 00:36:24.840] It is an energy sink whilst that switch is closed.
[00:36:24.840 - 00:36:26.200] So that will be a what?
[00:36:26.200 - 00:36:29.480] Ramping up or ramping down current?
[00:36:29.480 - 00:36:31.000] Ramping up current.
[00:36:31.000 - 00:36:35.440] We're putting energy into that inductor.
[00:36:35.440 - 00:36:38.640] Oh, I'm going to go.
[00:36:38.640 - 00:36:39.720] All right.
[00:36:39.720 - 00:36:44.160] So the change in inductor current is just the same thing.
[00:36:44.160 - 00:36:46.880] It's just equal to what voltage we're applying to it
[00:36:46.880 - 00:36:48.200] for the amount of time.
[00:36:48.200 - 00:36:57.630] This is delta t over L.
[00:36:57.630 - 00:37:00.550] So this just rearranging this effective equation just
[00:37:00.550 - 00:37:03.190] going with the differential to delta.
[00:37:03.190 - 00:37:05.590] So delta I L bring this over to here.
[00:37:05.590 - 00:37:13.360] Here is delta t over L.
[00:37:13.360 - 00:37:15.800] Switch is open.
[00:37:15.800 - 00:37:20.200] So here's now the situation with the switch open.
[00:37:20.200 - 00:37:22.920] So with that open, this is open circuit.
[00:37:22.920 - 00:37:27.050] Here it is.
[00:37:27.050 - 00:37:29.570] No current flowing through there.
[00:37:29.570 - 00:37:34.950] The diode is sitting here, obviously.
[00:37:34.950 - 00:37:36.510] And that is now forward biased.
[00:37:36.510 - 00:37:37.310] Hang on.
[00:37:37.310 - 00:37:40.150] How is it forward biased?
[00:37:40.150 - 00:37:44.630] The convention that we've used here plus minus,
[00:37:44.630 - 00:37:48.790] definitely feeding energy into that inductor.
[00:37:48.790 - 00:37:51.110] And it's plus minus.
[00:37:51.110 - 00:37:53.550] And that current was ramping up.
[00:37:53.550 - 00:37:55.990] Now we open the switch.
[00:37:55.990 - 00:38:00.870] The inductor, biased nature, will try to keep that current flowing
[00:38:00.870 - 00:38:07.400] in the same direction at the same magnitude.
[00:38:07.400 - 00:38:11.200] In order to do that, it needs to have a current pathway.
[00:38:11.200 - 00:38:14.880] And it's voltage flips.
[00:38:14.880 - 00:38:16.680] So this is the convention.
[00:38:16.680 - 00:38:21.800] But it's actual voltage flips and it becomes an energy source.
[00:38:21.800 - 00:38:26.440] So we can see minus plus, minus plus.
[00:38:26.440 - 00:38:29.440] So it's two voltages adding in the same direction.
[00:38:29.440 - 00:38:37.540] Two voltage sources adding with voltages in the same direction.
[00:38:37.540 - 00:38:46.270] That means that this voltage here will be actually positive with respect to that side.
[00:38:46.270 - 00:38:56.820] Because now those two voltages will be high enough to exceed the output voltage.
[00:38:56.820 - 00:38:57.940] Right.
[00:38:57.940 - 00:39:01.180] So what is the voltage drop across the inductor?
[00:39:01.220 - 00:39:06.300] Well, it's just the source voltage minus the output voltage.
[00:39:06.300 - 00:39:09.060] It's just the voltage difference across the inductor.
[00:39:09.060 - 00:39:15.100] It's just that a boost converter that means that the output voltage is larger than the input voltage.
[00:39:15.100 - 00:39:21.720] So VS minus V out is actually a negative quantity,
[00:39:21.720 - 00:39:24.720] which is why that voltage reverses.
[00:39:24.720 - 00:39:25.000] Right.
[00:39:25.000 - 00:39:33.380] So V out, V out is still equal to LDIO by DT.
[00:39:33.380 - 00:39:37.740] It's negative, V out is greater than VS.
[00:39:37.740 - 00:39:38.860] That's negative.
[00:39:38.860 - 00:39:44.660] So the DI by DT is a negative quantity, which means it's ramping down.
[00:39:44.660 - 00:39:52.230] Still constant, but negative constant.
[00:39:52.230 - 00:39:57.910] So the change in current for the switch open is the voltage drop across the inductor.
[00:39:57.910 - 00:40:02.430] For the amount of time delta t, which is the risk of the switching period.
[00:40:02.430 - 00:40:09.020] So it's one minus d times the period over L.
[00:40:09.020 - 00:40:21.540] OK, we still have the requirement that the average change in inductor current will have to be equal to 0.
[00:40:21.540 - 00:40:28.580] We also have that the average voltage across the inductor must equal 0.
[00:40:28.580 - 00:40:37.460] So we'll take it from, we'll have a look at the analysis from that viewpoint first.
[00:40:37.460 - 00:40:42.800] So those two areas are the same.
[00:40:42.800 - 00:40:44.600] Yep.
[00:40:44.600 - 00:40:48.160] Irrespective of what duty ratio we have, you just see a difference in the
[00:40:48.160 - 00:40:54.060] amplitude to make those areas the same.
[00:40:54.060 - 00:40:57.300] Basically this amplitude because that is constant at VS.
[00:40:57.300 - 00:40:57.940] Right.
[00:40:57.940 - 00:41:15.440] So it's actually A1 plus A2, as far as the calculations is concerned because the negative has already taken into that.
[00:41:15.440 - 00:41:31.950] So we've got VS DT plus VS minus V out 1 minus DT equals 0.
[00:41:31.950 - 00:41:43.950] So we're in that we're expanding it without VS D plus VS minus D times VS minus V out plus D times V out equals 0.
[00:41:43.950 - 00:41:56.900] So VS D minus VS D, we've got VS plus V out minus 1 plus D equals 0.
[00:41:56.900 - 00:42:10.610] VS equals V out times 1 minus D. And you rearrange it for V out, we've just got VS over 1 minus D.
[00:42:10.610 - 00:42:15.490] And we still have the duty ratio it applies somewhere between 0 and 1.
[00:42:15.490 - 00:42:24.040] So the output voltage by that expression will tell us that the output voltage will always be larger.
[00:42:24.040 - 00:42:27.840] Equal to when the duty ratio is equal to 0.
[00:42:28.120 - 00:42:44.200] But will always be larger than the input voltage.
[00:42:44.200 - 00:42:44.480] Right.
[00:42:44.480 - 00:42:51.920] So we've gotten to a point where we will move on from the basic operation of our boost converter.
[00:42:53.440 - 00:43:02.800] And consider things such as our continuous current design for the inductor and
[00:43:02.800 - 00:43:08.560] output voltage ripple calculation if we're going to design it for a certain level of voltage ripple.
[00:43:09.880 - 00:43:12.920] Those kind of take a bit of time to jump into.
[00:43:12.920 - 00:43:14.320] So we'll leave that.
[00:43:14.320 - 00:43:19.160] I know it's not having quite finished the whole content of this lecture.
[00:43:19.160 - 00:43:23.160] But the follow on lecture on, I could boost converters.
[00:43:23.160 - 00:43:24.760] We have a look at another one.
[00:43:24.760 - 00:43:26.400] This is relatively short.
[00:43:26.400 - 00:43:32.760] So it fits in quite nicely that I do this design stuff for the boost converter at the start of next lecture.
[00:43:32.760 - 00:43:36.000] And then finish with buck boost at that lecture.
[00:43:36.000 - 00:43:36.920] Right. So that's it for today.

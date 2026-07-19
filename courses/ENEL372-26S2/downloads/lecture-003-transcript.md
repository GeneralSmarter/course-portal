# ENEL372-26S2 Lecture 3 local ASR transcript

Date: July 17, 2026 9:00am-9:38am
Transcript type: Hermes-generated local ASR from validated Echo audio, not a native Echo transcript.
Backend/model: faster-whisper small.en, CPU int8, beam_size=5, vad_filter=True.
Source audio SHA-256: `9e03dbb55005784c2aa19076e2091f6bb00dbc070bbeffef3478181897647281`
Generated: 2026-07-19T20:30:17.364169+12:00
Caveat: technical terms, equations, names and Māori words may require checking against slides/audio.

[00:00:00.110 - 00:00:04.110] Right, Kia ora koutou, welcome along this morning.
[00:00:04.110 - 00:00:06.110] Nice morning to be out and about.
[00:00:06.110 - 00:00:08.110] Right. Okay.
[00:00:08.110 - 00:00:12.110] So we've gotten to the point now where we've sort of done some background
[00:00:12.110 - 00:00:19.110] and it's time to jump into looking at our first power electronic converter that we'll focus on.
[00:00:19.110 - 00:00:28.110] It's the converter that you had a very, very brief introduction to back in ENL 270.
[00:00:28.110 - 00:00:37.110] So we're going to start off in this lecture kind of rehashing some of the theory that you got from that time,
[00:00:37.110 - 00:00:39.110] just to familiarize yourselves again.
[00:00:39.110 - 00:00:46.110] But we will be delving considerably deeper into these converters than you have seen before,
[00:00:46.110 - 00:00:50.110] especially for the buck converter.
[00:00:50.110 - 00:00:56.110] So just to get our minds into the right space again,
[00:00:56.110 - 00:01:00.110] I did mention right at the beginning in the first lecture that, of course,
[00:01:00.110 - 00:01:04.110] it's possible to do power conversion with a linear system,
[00:01:04.110 - 00:01:07.110] but we can also do it with a switching system.
[00:01:07.110 - 00:01:17.110] Linear voltage conversion especially usually involves dissipating controlled amounts of power.
[00:01:17.110 - 00:01:20.110] And it's true effectively in a resistive component.
[00:01:20.110 - 00:01:26.110] We've got a small example of that sort of linear system shown here.
[00:01:26.110 - 00:01:31.110] So you'd measure effectively the output voltage.
[00:01:31.110 - 00:01:35.110] We've just got a linear voltage divider here.
[00:01:35.110 - 00:01:41.110] You'd compare that against the reference and use that to control a series pass element
[00:01:41.110 - 00:01:44.110] very often in the form of a bipolar junction transistor.
[00:01:44.110 - 00:01:52.110] But that all intents and purposes in the circuit acts like some sort of variable resistance.
[00:01:52.110 - 00:02:01.110] And it dissipates that energy to provide a nice constant output voltage from a larger input voltage.
[00:02:01.110 - 00:02:08.110] So just by the nature that you're dissipating this energy means that linear regulators,
[00:02:08.110 - 00:02:18.970] whilst providing a very, very nice stable constant output DC, do tend to be rather inefficient.
[00:02:18.970 - 00:02:28.970] However, switching voltage conversion, we control the output through limiting the power via and transfer by switching.
[00:02:28.970 - 00:02:34.970] And our components in that switch mode are very efficient, either they're fully off or when they're fully on,
[00:02:34.970 - 00:02:38.970] there's very little energy being dissipated in the semiconductors.
[00:02:38.970 - 00:02:46.970] And the energy storage components that we're utilizing our inductors and capacitors for general purposes,
[00:02:46.970 - 00:02:51.970] especially at our stage, we can consider as being relatively lossless.
[00:02:51.970 - 00:02:55.970] So the overall conversion will be very efficient.
[00:02:55.970 - 00:03:06.820] We're going to use switch filter combinations to provide also extra voltage conversion functionality
[00:03:06.820 - 00:03:12.820] that you can't get with just these simple series, variable series resistances.
[00:03:12.820 - 00:03:21.820] But that's the next form of voltage converter, DC to DC converter that we'll be looking at known as boost converters.
[00:03:21.820 - 00:03:31.900] Basic switching converter concept.
[00:03:31.900 - 00:03:42.180] So what we've got here is a circuit with a DC source for the input, a switching controllable semiconductor switch,
[00:03:42.180 - 00:03:52.180] shown here is an end channel enhancement MOSFET, most commonly what we'll come across, and a very, very simple purely resistive load.
[00:03:52.180 - 00:03:59.180] So we're operating this as a functionally as an open or a closed switch.
[00:03:59.180 - 00:04:10.180] So when the switch is closed, you might prefer to think of it in the semiconductor transistor notion as being on.
[00:04:10.180 - 00:04:12.180] So it means the same thing.
[00:04:12.180 - 00:04:15.180] So you transfer this is to the output.
[00:04:15.180 - 00:04:19.180] You transfer the input voltage to the output.
[00:04:19.180 - 00:04:23.180] OK, so you just see this at the load will be out.
[00:04:23.180 - 00:04:28.900] Then you turn off the switch and it's open state.
[00:04:28.900 - 00:04:37.900] And of course, there'll be no voltage across the load is being blocked by this open circuit when it's in its open state.
[00:04:37.900 - 00:04:42.900] All right. And we do that on a periodic basis that's fixed in frequency.
[00:04:42.900 - 00:04:48.900] So we have a period of time when the switch is closed and a period of time when the switch is open.
[00:04:48.900 - 00:04:54.660] But that period is consistent.
[00:04:54.660 - 00:05:05.660] Right. I introduced the concept of the duty ratio or duty cycle before it's the measure of the proportion of an entire period that the switch is on or power is being transferred.
[00:05:05.660 - 00:05:11.660] So that the duty ratio is just the ratio of T on over the entire period.
[00:05:11.660 - 00:05:14.660] Well, since it's one over the period, it's just the frequency.
[00:05:14.660 - 00:05:22.400] You could say T on times the frequency.
[00:05:22.400 - 00:05:25.780] That's interesting. All right.
[00:05:25.780 - 00:05:38.240] So in this case, the average load over one period will just be D times the duty ratio times the source voltage.
[00:05:38.240 - 00:05:49.240] Just in case it's a term that you have not come across before, it's certainly a term that you will hear a lot in your degree as you go through,
[00:05:49.240 - 00:06:05.240] is that changing the time width of a DC pulse by changing the duty ratio is and that changes the output voltage is one example of what's known as pulse width modulation.
[00:06:05.240 - 00:06:11.240] Changing that pulse width changes or modulates the output of our system.
[00:06:11.240 - 00:06:16.240] So pulse width modulation is something that is utilized a lot.
[00:06:16.240 - 00:06:23.240] And as such, yes, as I said, is something that you'll come across quite often from here on in in your degree.
[00:06:23.240 - 00:06:35.990] And potentially when you go out into being professional engineers. All right.
[00:06:35.990 - 00:06:44.990] So that's the concept of power conversion by switch mode or a switch mode concept.
[00:06:44.990 - 00:06:48.990] Let's turn that into a full converter.
[00:06:48.990 - 00:06:56.990] So the concept that we just looked at showed an output that was plus zero zero plus zero zero.
[00:06:56.990 - 00:07:12.990] For most of our applications where we want a DC output, we want it to be a nice constant value of DC, not this one that chops between one value and a zero value.
[00:07:12.990 - 00:07:25.990] So what we need is to include an output filter on that simple circuit that enables us to recover any kind of energy that may be stored.
[00:07:25.990 - 00:07:38.990] So that's basically what this this thing called a buck converter is. It's a basic step down converter that has energy recovery.
[00:07:38.990 - 00:07:47.990] There's a term as well that that you might be or might not be familiar with step down.
[00:07:47.990 - 00:07:59.990] So it's context driven. This sort of term. What we're talking about here is that the output voltage is stepped down from the input voltage.
[00:07:59.990 - 00:08:12.750] So we're talking voltage conversion here for basic step down converter. So be out will be less than be in a step down output voltage.
[00:08:12.750 - 00:08:17.750] The buck converter topology and essential operation shown here. Don't worry about this.
[00:08:17.750 - 00:08:24.750] This is just showing the this the equivalent of the circuit when the switch is on and when the switch is off the controllable switch.
[00:08:24.750 - 00:08:32.750] We're just concerned here about the circuit topology. All that means is the general circuit configuration.
[00:08:33.750 - 00:08:44.750] The term of this is the such and such topology is just saying this is it in general, not looking at specific values of components that might be utilized.
[00:08:44.750 - 00:09:03.320] So the general topology will have an input voltage source DC value, which we will be just for the most part identifying as being a constant value.
[00:09:03.320 - 00:09:14.320] Here is your controllable switch. Right. So you can buy a control signal coming in. You can tell it to turn on and turn off our power inductor,
[00:09:14.320 - 00:09:28.320] which is designed by nature to store reasonable amounts of energy, a filter capacitor that goes hand in hand with this lossless storage and release of energy,
[00:09:28.320 - 00:09:42.320] a load which to keep things again not too complex is we will be mostly considering as being purely resistive and a diode,
[00:09:42.320 - 00:09:54.320] which is absolutely critical to be there, which handles the energy recovery element from the inductor when we have the switch off and we need to recover that energy.
[00:09:58.840 - 00:10:08.840] One of the assumptions that we'll be making for our DC to DC converters that we're looking at is that the inductor current will be continuous unless I state otherwise.
[00:10:08.840 - 00:10:22.840] All right. So that means that after the steady state condition after first sitting on the inductor current never falls to being a value of zero.
[00:10:23.840 - 00:10:42.840] We don't actually technically have to have that condition for our converters to operate, but it's certainly the preferred design criteria and it certainly makes the converter a lot easier to analyze if it has that condition.
[00:10:42.840 - 00:10:50.840] So when I say it's continuous, it doesn't mean that the current can't vary. It just doesn't fall to zero.
[00:10:50.840 - 00:11:03.840] So we can have this situation where it might be zero, IL, but the current can do that, but just not hit down to zero.
[00:11:03.840 - 00:11:12.910] So continuous doesn't mean not varying in some respect.
[00:11:12.910 - 00:11:27.420] All right. So what we're going to do is we'll go through the buck converter, look at it and analyze it in those two switch condition states, controllable switch for when it's on and when it's off.
[00:11:28.420 - 00:11:55.650] Just so that we're able to make certain assumptions and understand how the analysis is being presented, we're going to look at the consider the following steady state properties being in place for our converter.
[00:11:55.650 - 00:11:59.650] Right. So the inductor current fluctuations are completely periodic.
[00:11:59.650 - 00:12:05.650] So you will exactly see the same behavior period on period for the converter.
[00:12:05.650 - 00:12:09.650] The average change in inductor current is zero.
[00:12:09.650 - 00:12:12.650] So we had this state before.
[00:12:12.650 - 00:12:19.650] So delta IL on average equals zero.
[00:12:19.650 - 00:12:26.300] The average inductor voltage is zero.
[00:12:26.300 - 00:12:30.770] Average capacitor current is zero.
[00:12:30.770 - 00:12:32.770] Don't forget that it's voltage.
[00:12:32.770 - 00:12:47.740] The change, average change in capacitor voltage as well, delta VC average equals zero.
[00:12:47.740 - 00:12:51.740] And the power supplied by the source equals the power delivered to the load.
[00:12:51.740 - 00:12:59.800] And when we get to it, plus any non-ideal losses.
[00:12:59.800 - 00:13:05.800] Right. So we aren't considering losses just at this point in time because it does complicate things a little.
[00:13:05.800 - 00:13:11.800] So all of these components that we're considering for now will be identified as being ideal.
[00:13:11.800 - 00:13:25.380] But we do touch on what happens when we start thinking about non-ideal properties for our components.
[00:13:25.380 - 00:13:36.610] All right. With that sort of steady state conditions in mind, let's have a look at some analysis of our black converter.
[00:13:36.610 - 00:13:45.610] Now inductor current is what ultimately determines our output voltage and all of the DC to DC converters that we will look at.
[00:13:45.610 - 00:13:53.610] So a key part of the analysis is looking at the current associated with our inductor.
[00:13:53.610 - 00:13:56.610] Right. Switch closed.
[00:13:56.610 - 00:14:03.610] So the equivalent circuit from the general topology for our buck converter when the switch is closed is given here.
[00:14:03.610 - 00:14:12.610] So here is the position of our semiconductor switch and it's in its on state. So there it is short circuited in the circuit.
[00:14:12.610 - 00:14:19.610] This then puts a voltage of plus V on one side of the inductor.
[00:14:19.610 - 00:14:43.140] We're assuming steady state. So that means that the output of the of the converter is assumed to have a constant DC value.
[00:14:43.140 - 00:14:49.730] So that says essentially constant voltage. All right.
[00:14:49.730 - 00:15:03.980] So and because we've got effectively plus minus across the diode, just to remind you, that's the way around the diode is.
[00:15:03.980 - 00:15:07.980] We've got the positive side on the cathode and the negative side on the anode.
[00:15:07.980 - 00:15:21.850] So that's reverse biased and that diode appears as an open circuit to figure out what the current is through our inductor.
[00:15:21.850 - 00:15:26.850] We need to determine what is the voltage drop across our inductor.
[00:15:26.850 - 00:15:32.850] So the voltage when the switch is closed turns out to be relatively simple to determine.
[00:15:32.850 - 00:15:37.850] It is just V on one side and V out on the other side.
[00:15:37.850 - 00:15:44.850] So the overall voltage drop across our inductor is V minus V out, which are both constant quantities.
[00:15:44.850 - 00:15:59.810] And we always already know and this is the expression that I said that you should really or the relationship between voltage and current for inductors that you should get used to seeing.
[00:15:59.810 - 00:16:06.810] So we already know that that is equal to LDI by DIL by DT. This is constant. This is constant.
[00:16:06.810 - 00:16:10.810] So the derivative of the current is a constant.
[00:16:10.810 - 00:16:18.820] The only solution to that is a constantly ramping current.
[00:16:18.820 - 00:16:22.820] Since it's positive, it's constantly ramping up.
[00:16:22.820 - 00:16:31.700] All right, so we'd expect to see a current that's constantly ramping up with the switch closed.
[00:16:31.700 - 00:16:40.700] Well, how much? Well, the change in the in that current when the switch is closed is VS minus V out.
[00:16:40.700 - 00:16:43.700] That's the voltage force.
[00:16:43.700 - 00:16:48.700] We're effectively rearranging this equation with just Delta IL and Delta T.
[00:16:49.700 - 00:17:04.450] So we've got L Delta IL over Delta T is equal to VS minus V out.
[00:17:04.450 - 00:17:22.560] All right, so Delta T for the circuit or the operation that we're looking at is just the amount of time that that switches on, which is their duty ratio times the period.
[00:17:23.560 - 00:17:30.350] So that's D times T. So that's where this comes from.
[00:17:30.350 - 00:17:42.350] So we're just rearranging this, taking the differential like just a fraction, essentially, and rearranging to solve for Delta IL.
[00:17:42.350 - 00:17:58.220] So we've got this expression for the overall magnitude of the current rise.
[00:18:03.730 - 00:18:09.710] And we've got to open the switch for the remainder of the period.
[00:18:09.710 - 00:18:19.860] So here's what the equivalent circuit is for when the switch is open.
[00:18:19.860 - 00:18:26.180] Right, so a couple of things happen here.
[00:18:26.180 - 00:18:30.180] With the switch open, we remove the DC voltage source from the circuit.
[00:18:30.180 - 00:18:37.030] This is open circuit, so no current is flowing from the source.
[00:18:37.030 - 00:18:46.030] The energy that has been stored in the inductor whilst the switch is on now is released.
[00:18:46.030 - 00:18:51.030] So the inductor changes from being a sink of energy to being a source of energy.
[00:18:51.030 - 00:18:55.030] The current, though, stays flowing in the same direction.
[00:18:55.030 - 00:18:58.030] So we've got IL.
[00:18:58.030 - 00:19:01.030] We can define other things like the capacitor current.
[00:19:01.030 - 00:19:14.400] So by convention, the positive capacitive current will stay flowing into it and the current flowing through the resistance.
[00:19:14.400 - 00:19:23.400] We actually can say, since it's all a constant voltage and this is a purely resistance, we can say that that is a constant value of current.
[00:19:23.400 - 00:19:34.660] So we'll do an uppercase I for that to indicate that it's a constant current, a DC current.
[00:19:35.660 - 00:19:44.660] For that to be the case, though, for current to flow this way and this to be an energy source, of course its voltage flips.
[00:19:44.660 - 00:19:55.660] So the voltage in reality across the inductor is that way around, which is why we say VL with this plus minus convention is minus V out.
[00:19:55.660 - 00:20:16.840] So what we've got here is the inductor now in parallel with the capacitor and the resistance with the diode that was there now being forward biased.
[00:20:16.840 - 00:20:21.840] Because with the current flowing this way around, this side is actually positive with respect to that side of the diode.
[00:20:21.840 - 00:20:28.060] So it's forward biased.
[00:20:28.060 - 00:20:42.060] The equivalent, assuming ideal diodes, no voltage drop to keep things simple, this essentially means that we've got a circuit with the inductor in parallel with the capacitor, like I said, with the load.
[00:20:42.060 - 00:20:47.060] We've just got a very long node here with a kink in it.
[00:20:47.060 - 00:20:53.100] So this is the equivalent circuit that's set up.
[00:20:53.100 - 00:20:57.100] Right. So what is the voltage across the inductor?
[00:20:57.100 - 00:21:00.100] Well, it's kind of stated here, but it's pretty simple to see if it's in parallel.
[00:21:00.100 - 00:21:02.100] We're assuming steady state conditions.
[00:21:02.100 - 00:21:11.260] So we still have plus minus V out.
[00:21:11.260 - 00:21:13.260] This is constant.
[00:21:13.260 - 00:21:14.260] This is constant.
[00:21:14.260 - 00:21:18.260] So the derivative will be a constant, which means that we have a ramping current.
[00:21:18.260 - 00:21:24.750] Now with the negative sign there, that means that it's ramping down.
[00:21:24.750 - 00:21:33.940] And we have delta IL for it ramping down.
[00:21:33.940 - 00:21:36.940] So we've got the waveform or the timing.
[00:21:36.940 - 00:21:47.940] We've got DT and T, which must mean that this amount of time is one minus D times T.
[00:21:47.940 - 00:21:56.460] Why? Because D varies between zero and one.
[00:21:56.460 - 00:22:01.460] So if we've got D times T, then the remainder is one minus D.
[00:22:01.460 - 00:22:07.430] So that's where this part comes from.
[00:22:07.430 - 00:22:13.430] This is our delta T for the switch being off.
[00:22:13.430 - 00:22:19.050] Oops, that might look like it.
[00:22:19.050 - 00:22:23.670] It's not over.
[00:22:23.670 - 00:22:31.220] It's equivalent to delta T off.
[00:22:31.220 - 00:22:37.220] So we've got the situation where we've got delta IL for when we've got the switch on
[00:22:37.220 - 00:22:40.220] and delta IL for when we've got the switch off.
[00:22:40.220 - 00:22:47.220] And those by the definitions that we had just identified for steady state operation,
[00:22:47.220 - 00:22:50.220] the summation of those has to be equal to zero.
[00:22:50.220 - 00:22:56.280] So zero on average.
[00:22:56.280 - 00:23:03.280] Even though it may have an average value, then of a positive DC value,
[00:23:03.280 - 00:23:07.280] the fluctuation has to equal zero period on period.
[00:23:07.280 - 00:23:11.620] Yeah?
[00:23:11.620 - 00:23:14.620] I'm going to get back to the waveforms shortly.
[00:23:14.620 - 00:23:18.620] But we can see that whilst the switch is on,
[00:23:18.620 - 00:23:22.620] we have VS minus V out across the inductor for voltage.
[00:23:22.620 - 00:23:25.620] When the switch is off, we have minus V out.
[00:23:25.620 - 00:23:29.620] Flips and sine or one minus D times T.
[00:23:29.620 - 00:23:31.620] And it just keeps repeating.
[00:23:31.620 - 00:23:37.310] And whilst it's on, the current ramps up from a minimum value to a maximum.
[00:23:37.310 - 00:23:41.310] And then when it switches off, it goes from a maximum value down to the minimum again
[00:23:41.310 - 00:23:43.310] and just repeats.
[00:23:43.310 - 00:23:49.610] I'll come back to the capacitor current in just a second.
[00:23:49.610 - 00:24:09.430] So I'm going to just do a derivation of the fact that just to look at the step-down ratio
[00:24:09.430 - 00:24:24.000] or the step-down value, I'll do an analysis looking at the average current change
[00:24:24.000 - 00:24:31.270] having to equal zero period on period from just that expression before.
[00:24:31.270 - 00:24:40.270] So delta IL on plus delta IL off equals zero.
[00:24:40.270 - 00:24:47.940] So we've got VS minus V out over L DT.
[00:24:47.940 - 00:24:57.940] So plus, but it was negative, so plus minus, minus V out over L one minus DT equals zero.
[00:24:57.940 - 00:25:04.330] Those just cancel out.
[00:25:04.330 - 00:25:08.330] The same on both.
[00:25:08.330 - 00:25:11.330] The L's also cancel out there.
[00:25:11.330 - 00:25:13.330] Don't worry about those.
[00:25:13.330 - 00:25:24.380] So we're left with VS minus V out D minus V out one minus D equals zero.
[00:25:24.380 - 00:25:26.380] Spend that out.
[00:25:26.380 - 00:25:40.300] VSD minus V out D minus V out plus V out D equals zero minus V out D plus V out D cancels.
[00:25:40.300 - 00:25:46.300] So we're left with V out equals D times VS.
[00:25:46.300 - 00:25:48.300] Nice.
[00:25:48.300 - 00:25:53.300] That's exactly the same expression that we had right back when I showed you the switching converter concept,
[00:25:53.300 - 00:26:04.720] but with no filter, except now we have a constant output voltage rather than this thing that changes between VS and zero.
[00:26:04.720 - 00:26:16.110] Great. So that's our step-down ratio.
[00:26:16.110 - 00:26:25.110] I don't know if you clocked this, but when I wrote this expression after cancelling the period and the inductance value,
[00:26:25.110 - 00:26:28.110] this is the equation for the average inductive voltage equals zero.
[00:26:28.110 - 00:26:41.740] So the inductive voltage when the switch is on is just VS minus V out,
[00:26:41.740 - 00:26:47.740] and the inductive voltage when the switch is off is minus V out.
[00:26:47.740 - 00:27:07.900] Just stepping back, what would make the inductor current of the buck converter become discontinuous?
[00:27:07.900 - 00:27:10.900] I said that we're going to assume that it is continuous,
[00:27:10.900 - 00:27:15.900] but the operation of the converter can still carry on if it becomes discontinuous.
[00:27:15.900 - 00:27:22.900] So we need to have or should have an idea of what the conditions are for that to occur.
[00:27:22.900 - 00:27:34.820] So if we jump back, that slide again, and here we have the inductor current,
[00:27:34.820 - 00:27:41.820] and here's the average current IR at the load and the change of inductor current.
[00:27:41.820 - 00:27:53.820] What happens if, say, we have a resistance condition such that the current through that resistor is lower,
[00:27:53.820 - 00:27:59.820] but we still have a ripple in the inductor current that's like this.
[00:27:59.820 - 00:28:06.820] As soon as delta IL over 2 is equal to IR,
[00:28:06.820 - 00:28:12.820] then we're right on the limit of when that becomes discontinuous.
[00:28:12.820 - 00:28:21.820] We would be effectively bringing this down to the point where this is our zero line,
[00:28:21.820 - 00:28:24.820] and that just starts intercepting.
[00:28:24.820 - 00:28:29.820] But if it comes even lower, then we're going to end up with a situation
[00:28:29.820 - 00:28:35.820] where we have the current hitting zero, being zero for a certain period of time,
[00:28:35.820 - 00:28:39.520] and then switching up again.
[00:28:39.520 - 00:28:43.520] So like I said, you can hit that state in these converters,
[00:28:43.520 - 00:28:45.520] and they will still function.
[00:28:45.520 - 00:28:50.520] It's just by having this sort of situation in your inductors,
[00:28:50.520 - 00:28:56.520] you are increasing the RMS value of that current relative to its average,
[00:28:56.520 - 00:29:03.520] and you'll be dissipating more energy than you would otherwise if it was continuous.
[00:29:04.520 - 00:29:09.520] So it's a condition that affects the overall efficiency of our converter.
[00:29:09.520 - 00:29:16.740] So we try to avoid that happening.
[00:29:16.740 - 00:29:19.740] Now that we're back on this page,
[00:29:19.740 - 00:29:24.740] I did say that I would talk about the capacitor current as well.
[00:29:24.740 - 00:29:32.310] Note that the capacitor current looks like the ripple on the inductor current.
[00:29:32.310 - 00:29:34.310] It's the same shape, same slope,
[00:29:34.310 - 00:29:39.310] and that's exactly the sort of behavior that we expect
[00:29:39.310 - 00:29:43.310] and will see in a real world buck converter.
[00:29:43.310 - 00:29:48.850] What we've got here is, of course, is energy transfer occurring
[00:29:48.850 - 00:29:50.850] between the inductor and the capacitor
[00:29:50.850 - 00:30:00.390] under the conditions where we have a constant current flowing in the load.
[00:30:00.390 - 00:30:03.390] With the convention identified here,
[00:30:03.390 - 00:30:08.390] a positive current, so that's current flowing into the terminal of a capacitor.
[00:30:08.390 - 00:30:09.390] What do we think is going to happen?
[00:30:09.390 - 00:30:14.390] Is that capacitor under that condition being charged or discharged?
[00:30:14.390 - 00:30:19.690] Current flowing into a capacitor,
[00:30:19.690 - 00:30:23.690] do we think that that's going to be a state where that capacitor is being charged
[00:30:23.690 - 00:30:27.690] or do we think that's being discharged when current flowing into it?
[00:30:27.690 - 00:30:28.690] Charged.
[00:30:28.690 - 00:30:30.690] Charged, yeah, absolutely.
[00:30:30.690 - 00:30:35.690] So wherever we see in this expression here a positive value,
[00:30:35.690 - 00:30:40.580] this means the capacitor is being charged.
[00:30:40.580 - 00:30:45.580] Wherever it's negative, that means it's being discharged.
[00:30:45.580 - 00:30:55.930] Let's look at the Kirchhoff's current law that's being applied to this node here.
[00:30:55.930 - 00:31:06.930] So we have IR equals, well, IL is positive, minus IC.
[00:31:06.930 - 00:31:10.930] Whoops, should really do the lower case.
[00:31:10.930 - 00:31:14.930] IL minus IC.
[00:31:17.620 - 00:31:20.620] I will rewrite that equation completely.
[00:31:20.620 - 00:31:22.620] It's so messy.
[00:31:22.620 - 00:31:26.620] IR equals IL minus IC.
[00:31:26.620 - 00:31:29.620] Right, that's Kirchhoff's current law.
[00:31:29.620 - 00:31:31.620] IR, I've kept that, that's constant.
[00:31:31.620 - 00:31:34.620] So if we look at this in the slopes,
[00:31:34.620 - 00:31:52.580] then minus IC, if I was to draw minus IC, it would look like this, right?
[00:31:52.580 - 00:31:56.580] So if we're saying that that gets added to this waveform,
[00:31:56.580 - 00:32:09.400] which has the same peak, so this is equal to delta IL,
[00:32:09.400 - 00:32:26.560] then what we're just doing is we're subtracting from this waveform,
[00:32:26.560 - 00:32:30.560] which gives us our constant output current.
[00:32:30.560 - 00:32:35.740] So this is something to pay attention to,
[00:32:35.740 - 00:32:41.740] is that the ripple current in the capacitor is the exact opposite
[00:32:41.740 - 00:32:46.370] of the ripple current in the inductor,
[00:32:46.370 - 00:32:50.370] so that the average is a constant at the load.
[00:32:50.370 - 00:33:37.460] Okay, what about the source current?
[00:33:37.460 - 00:34:01.040] So we've got our inductor current, so DT, T.
[00:34:01.040 - 00:34:07.380] We've got IMIN, IMAX.
[00:34:07.380 - 00:34:15.260] How does that then relate to our switch current?
[00:34:15.260 - 00:34:38.070] So back to the topology, general topology of our buck converter.
[00:34:38.070 - 00:34:40.070] We've got the switch closed.
[00:34:41.070 - 00:34:46.070] Switch closed, it's providing the current to the inductor,
[00:34:46.070 - 00:34:50.070] so it's equal to the inductor current whenever the switch is closed.
[00:34:50.070 - 00:34:55.980] When it's open, of course it's zero.
[00:34:55.980 - 00:35:05.720] So switch current starts off at IMIN,
[00:35:05.720 - 00:35:13.980] at DT goes to IMAX.
[00:35:13.980 - 00:35:20.030] And then does it follow this?
[00:35:20.030 - 00:35:25.030] No, it goes to zero until we hit T.
[00:35:25.030 - 00:35:41.100] Then it jumps back up to IMIN and back to zero.
[00:35:41.100 - 00:35:46.100] So the source current is certainly discontinuous
[00:35:46.100 - 00:36:03.640] often to be able to calculate and analyze output power
[00:36:03.640 - 00:36:06.980] relative to input power.
[00:36:06.980 - 00:36:10.980] Output power in this case, relatively simple to determine
[00:36:10.980 - 00:36:12.980] because they're all DC quantities.
[00:36:12.980 - 00:36:27.970] So the real output power is just equal to Vout times IR.
[00:36:27.970 - 00:36:31.970] And by Ohm's law, you could also state Vout squared over R
[00:36:31.970 - 00:36:34.970] or IR squared R.
[00:36:34.970 - 00:36:36.970] It's all the same thing.
[00:36:36.970 - 00:36:58.660] The input power, and hence the reason that we went over this just yesterday,
[00:36:58.660 - 00:37:06.200] you need to determine the RMS value of the current, the source current.
[00:37:06.200 - 00:37:20.480] PIN equals VIN RMS times IIN, or I source, sorry, RMS.
[00:37:20.480 - 00:37:29.280] V source RMS, simple, it's a DC value.
[00:37:29.280 - 00:37:37.380] The RMS of a constant DC is just its value.
[00:37:38.380 - 00:37:42.380] This is a little bit tricky.
[00:37:42.380 - 00:37:46.380] You have to actually calculate what is the RMS value of that waveform.
[00:37:46.380 - 00:37:55.380] So this waveform here, you need to look at and try to figure out what is its RMS value,
[00:37:55.380 - 00:38:00.380] which is why I put that in as a homework problem for you to try out.
[00:38:00.380 - 00:38:09.910] So I want you to have a go at it.
[00:38:10.910 - 00:38:16.910] I will put all the problems that I present, I put fully work solutions up just a little bit later
[00:38:16.910 - 00:38:22.910] so that those that want to have a go at doing it without knowing the solution to start with,
[00:38:22.910 - 00:38:26.910] which is a really good approach, can do so.
[00:38:26.910 - 00:38:28.910] But then I'll put up the solution.
[00:38:28.910 - 00:38:33.160] I'll put up the solution to that early next week.
[00:38:33.160 - 00:38:36.160] Right, well, we finished a bit early. That's it for today.

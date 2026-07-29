# ENEL372-26S2 Lecture 7 fast-pass local ASR transcript

Date: July 27, 2026 4:00pm-4:55pm
Transcript type: Hermes fast-pass local ASR from validated Echo audio, not a native Echo transcript.
Backend/model: faster-whisper tiny.en, CPU int8, beam_size=1, vad_filter=True.
Quality note: fast catch-up transcript. Technical terms, equations, names and Māori words need checking against slides/audio before assessment use.
Source audio SHA-256: `7206e6d8a7099fac6f3bc14078a63b1803e46007f13800eb4c3bd05c4c859b4c`
Generated: 2026-07-30T10:24:09.263482+12:00

[00:00:00.140 - 00:00:05.140] Right, so we introduced the boost converter.
[00:00:05.140 - 00:00:10.140] We introduced the boost converter last time.
[00:00:10.140 - 00:00:14.140] And we got to the point where we did some of the basic analysis
[00:00:14.140 - 00:00:19.140] and we saw that the, certainly the voltage transfer function that we've got
[00:00:19.140 - 00:00:22.140] as a boosting or a stepping up of the output voltage
[00:00:22.140 - 00:00:26.140] relative to the input voltage as duty ratio changes.
[00:00:26.140 - 00:00:29.140] Okay, so it starts off in a duty ratio of zero.
[00:00:29.140 - 00:00:31.140] The output voltage being equal to the input voltage,
[00:00:31.140 - 00:00:55.160] in S-D-G
[00:00:56.140 - 00:01:00.140] to occur. Right.
[00:01:00.140 - 00:01:04.140] This time though, unlike the buck converter,
[00:01:04.140 - 00:01:09.140] where the power inductor is always connected to the output,
[00:01:09.140 - 00:01:15.140] for a boost converter, we will instead look at the power inductor current
[00:01:15.140 - 00:01:21.390] as associated with the input, because it's always connected to the input now.
[00:01:21.390 - 00:01:24.390] So, we need to have a look at the average
[00:01:24.390 - 00:01:28.390] current ripple and the design consideration for just being discontinuous.
[00:01:28.390 - 00:01:32.390] That's when that current ripple will just trump down to zero.
[00:01:32.390 - 00:01:36.390] But this i average now, when we've been looking at the buck converter,
[00:01:36.390 - 00:01:40.390] is that i average has always been the output current.
[00:01:40.390 - 00:01:42.390] Right. This average current here.
[00:01:42.390 - 00:01:45.390] Now, what we're talking about is the input current.
[00:01:45.390 - 00:01:50.390] So i average, this is your i S or this average source current.
[00:01:50.390 - 00:01:59.980] So find if what their average input current is,
[00:01:59.980 - 00:02:04.980] we can still utilize what we know about the current flowing in the load.
[00:02:04.980 - 00:02:12.980] We can refer or give ourselves an expression that relates the input current to the output current.
[00:02:12.980 - 00:02:19.980] And we use that trick that we use once before by assuming that we've got a converter that's 100% efficient.
[00:02:19.980 - 00:02:25.980] So the product of the average input voltage with the average input current
[00:02:25.980 - 00:02:29.980] will equal the product of the average output voltage times the average output current.
[00:02:29.980 - 00:02:37.980] This gives us, also we know as we've gone through the analysis for the boost converter
[00:02:37.980 - 00:02:41.980] that v out over v is just 1 over 1 minus d.
[00:02:41.980 - 00:02:46.980] Right. We're going to, first of all, we find an expression for delta i l.
[00:02:46.980 - 00:03:00.040] We're going to use the rise in the current.
[00:03:00.040 - 00:03:06.040] We could easily have looked at the fall, but the rise in current just uses a single voltage which is v s.
[00:03:06.040 - 00:03:13.350] So we know that v l equals l d i by d t, which gives us,
[00:03:13.350 - 00:03:18.350] because everything, remember with constant voltages on either side of the inductor,
[00:03:18.350 - 00:03:23.350] means it's a ramping voltage for current, ramping current, I should say.
[00:03:23.350 - 00:03:33.980] that's equal to l delta i l by delta t.
[00:03:33.980 - 00:03:37.980] So given that delta i l, which is what we're interested in,
[00:03:37.980 - 00:03:42.980] equals v over l delta t.
[00:03:42.980 - 00:03:47.980] And we're looking at the rise. So our delta t is just going to be equal to the g to the g to the ratio times the period.
[00:03:47.980 - 00:04:01.800] So that's v s in the instance.
[00:04:01.800 - 00:04:09.850] Source voltage equals, well, the more used to working with frequency than periods.
[00:04:09.850 - 00:04:15.850] So we have equals v s d over f s l.
[00:04:15.850 - 00:04:24.600] The criteria that we're trying to meet here,
[00:04:24.600 - 00:04:32.600] for just being on discontinuous current mode, is that we want the average source current to be greater than
[00:04:32.600 - 00:04:42.600] l, so we've got an expression for delta l now.
[00:04:42.600 - 00:04:49.600] So we want that to be greater than v s d over 2 f s l.
[00:04:49.600 - 00:04:53.600] So it is the one half coming in.
[00:04:53.600 - 00:04:58.600] We've also got with the, I saw it to do 100% efficient,
[00:04:58.600 - 00:05:07.700] and our voltage relationship between input and output.
[00:05:07.700 - 00:05:15.700] So from i s, just rearranging this is equal to v out over v s times i out.
[00:05:15.700 - 00:05:28.160] And knowing from the second expression here that different colors,
[00:05:28.160 - 00:05:29.160] so we don't get mixed up.
[00:05:29.160 - 00:05:34.160] v out over v s is 1 over 1 minus d.
[00:05:34.160 - 00:05:48.160] We can substitute that in, and we end up with i out over 1 minus d has to be greater than v s d over 2 f s l.
[00:05:48.160 - 00:05:50.160] So that's your switching frequency if this.
[00:05:50.160 - 00:05:56.160] And rearranging that to solve for l, the minimum value of inductance,
[00:05:56.160 - 00:05:58.160] we come up with this expression.
[00:05:58.160 - 00:06:08.160] So that's, those are the conditions for just being at the threshold for discontinuous current operation.
[00:06:08.160 - 00:06:12.160] You want your inductor to be considerably larger than that usually.
[00:06:12.160 - 00:06:21.160] So it might need to be twice the size to get the low of that peak well above the zero line.
[00:06:21.160 - 00:06:24.160] But that's the condition for keeping it continuous.
[00:06:24.160 - 00:06:28.160] We've got that d times 1 minus d again.
[00:06:28.160 - 00:06:38.160] So there is a worst case scenario that if the converter is expected to run at 50% at some point for a duty ratio,
[00:06:38.160 - 00:06:42.160] then that would be the worst case situation for the inductance.
[00:06:42.160 - 00:06:56.620] So we just talked about, I guess, a reason for keeping it continuous,
[00:06:56.620 - 00:07:02.620] or even an expression, not quite covered fully the reason.
[00:07:02.620 - 00:07:06.620] Well, basically we want to avoid all the reasons before us.
[00:07:06.620 - 00:07:10.620] We head for the buck converter for discontinuous current operation.
[00:07:10.620 - 00:07:20.710] So if it is discontinuous, we have lower efficiency.
[00:07:20.710 - 00:07:35.640] We have higher peak currents, which means that we need higher rated switches.
[00:07:35.640 - 00:07:41.640] And also there's more by those higher peak currents, there's more electrical noise.
[00:07:41.640 - 00:07:49.060] So these are all downsides.
[00:07:49.060 - 00:07:56.060] Quite interesting, one of you came and saw me in my office and talked a bit about boost converter design
[00:07:56.060 - 00:07:59.060] and looked at part in the textbook moment.
[00:07:59.060 - 00:08:04.060] And they actually talk about design for discontinuous current operation.
[00:08:04.060 - 00:08:12.060] So just be careful if you look at Maren, that's an unusual sort of approach to make,
[00:08:12.060 - 00:08:13.060] shall we say.
[00:08:13.060 - 00:08:17.500] Normally you look over a continuous current operation.
[00:08:17.500 - 00:08:25.500] There is one small positive, I guess, positive effect of discontinuous current operation.
[00:08:25.500 - 00:08:33.500] The amplification or the boosting function, the boosting ratio is slightly improved by having
[00:08:33.500 - 00:08:35.500] discontinuous operation.
[00:08:35.500 - 00:08:44.500] So here is the blue and blue, the curve for continuous current operation versus duty ratio.
[00:08:44.500 - 00:08:50.500] And there in red, this is the sort of curve you would get for potentially discontinuous current operation.
[00:08:50.500 - 00:08:56.500] So you can see that there is a slight increase in the amount of boosting, but it's not going to outweigh
[00:08:56.500 - 00:09:01.500] the disadvantages that you have for becoming discontinuous.
[00:09:01.500 - 00:09:13.680] Right, what about capacitor sizing?
[00:09:13.680 - 00:09:16.680] This is not part of the solar car project.
[00:09:16.680 - 00:09:21.680] So we're assuming that the voltage source at the input is a nice, perfect voltage source for you.
[00:09:21.680 - 00:09:23.680] We won't talk about input capacitance.
[00:09:23.680 - 00:09:40.430] We are still concerned though about output capacitance and how we might size that to achieve a particular level of voltage ripple at the output.
[00:09:40.430 - 00:09:49.430] We're allowing now for some ripple to a curve, but it's not large enough to make the analysis that we did before and we assumed it was constant,
[00:09:49.430 - 00:09:55.020] ineligible, what an accurate.
[00:09:55.020 - 00:10:01.020] Right, if we've got some current flowing in the capacitor, then it's a finite value of capacitance.
[00:10:01.020 - 00:10:08.020] There's got to be some voltage ripple associated with that charge transfer between charging and just charging that capacitance.
[00:10:08.020 - 00:10:21.020] So we've got the waveforms that are experienced for the boost converter, for the output capacitance, given it's connected to a purely resistive load.
[00:10:21.020 - 00:10:28.910] Right, so what we're talking about here is the output stage only of the circuit.
[00:10:28.910 - 00:10:46.190] So there's the inductor, the diode, the resistive load and the capacitor that we would be choosing to put in there for our filter.
[00:10:46.190 - 00:10:57.500] So we've got ID, we've got here's our average output current.
[00:10:57.500 - 00:11:03.610] That's, oh sorry, that's I out there.
[00:11:03.610 - 00:11:10.610] And we're going to define that current flowing into the capacitor as positive and that's Ic.
[00:11:10.610 - 00:11:18.950] Voltage across the capacitor plus minus vc and then plus minus v out.
[00:11:18.950 - 00:11:30.700] Right, so we've got two states that here's the average current.
[00:11:30.700 - 00:11:37.700] So whenever the, we've got the diode current down to zero, we've got an average current.
[00:11:37.700 - 00:11:43.700] So all of the current into the load, this average load is being provided by the capacitor.
[00:11:43.700 - 00:11:46.700] Right, and it's in the opposite direction.
[00:11:46.700 - 00:11:48.700] So it's the capacitor discharging.
[00:11:48.700 - 00:12:04.050] But when that state is true, so there's no diode current and we're assuming steady state, then we are saying still that the effective output voltage is relatively constant.
[00:12:04.050 - 00:12:11.050] Well if that's the case, then the current provided by the capacitor for a relatively constant output current.
[00:12:11.050 - 00:12:19.050] And that period, and that time there, dt, has to be considered as being effectively constant.
[00:12:19.050 - 00:12:22.050] A constant current from the capacitor.
[00:12:22.050 - 00:12:24.050] It's not really.
[00:12:24.050 - 00:12:27.050] There is, it's a capacitor feeding a resistive load.
[00:12:27.050 - 00:12:30.050] So there is an RC time constant associated with us.
[00:12:30.050 - 00:12:34.050] It's slowly drooping with an RC exponential time constant.
[00:12:34.050 - 00:12:37.050] What, exponential?
[00:12:37.050 - 00:12:49.580] We just can't see it because the capacitor is of such a large value that that RC time constant is very long relative to dt.
[00:12:49.580 - 00:12:56.580] Right, so if we were to take this out for an infinite time, it would slowly be discharging down to zero.
[00:12:56.580 - 00:13:00.340] Okay.
[00:13:00.340 - 00:13:16.340] With that approximation under assumption, then to find out what delta v is, we look at what is the voltage drop during this period that we're providing this constant current.
[00:13:16.340 - 00:13:27.340] Right, because once we have the capacitor charging with the diode forward biased, the capacitor charges, this curve is somewhat, well, it'll be a constant current.
[00:13:27.340 - 00:13:30.340] Well, it is, it is curved.
[00:13:30.340 - 00:13:43.340] Whereas because we've got constant current rather than a ramping down current, this is a ramping voltage, which makes the analysis considerably easier for finding out what is delta v.
[00:13:43.340 - 00:14:14.520] So when the capacitor is discharging, okay, the capacitor is discharging, the voltage drop is linear because we have constant current at that time.
[00:14:14.520 - 00:14:33.650] So we have delta vc, that's sorry, that looks like an L delta vc, is equal to the constant I out over c times delta t.
[00:14:33.650 - 00:14:34.650] Where do we get that from?
[00:14:34.650 - 00:14:38.650] Well, it's basically this expression just rearranged with deltors.
[00:14:38.650 - 00:14:44.650] So we have delta v and delta t, so we just rearrange.
[00:14:44.650 - 00:14:46.650] We're looking at delta v, right?
[00:14:46.650 - 00:14:53.650] So Ic times, which is just a constant times delta t divided by c.
[00:14:53.650 - 00:14:57.650] It's just rearranging there to give this.
[00:14:57.650 - 00:15:10.650] Equals I out over c, or delta t, that's the amount of time that we have the switch, not conducting here.
[00:15:10.650 - 00:15:27.420] So dt equals delta v out.
[00:15:27.420 - 00:15:40.420] We don't usually use the period, we use the switching frequency, so just substituting there then, and we've given the final expression for the output voltage ripple for a given size of capacitance.
[00:15:40.420 - 00:15:47.990] And also at a particular generating ratio, output current and switching frequency.
[00:15:47.990 - 00:15:56.440] Yep, are we following along with that?
[00:15:56.440 - 00:16:06.440] We know for the properties of our capacitor that the average change in capacitive voltage has to be equal to zero.
[00:16:06.440 - 00:16:09.440] So we don't need to calculate this side of it.
[00:16:09.440 - 00:16:26.050] We just need to calculate the one delta v, where we knew everything was nice and constant and easy to express.
[00:16:26.050 - 00:16:30.050] It kind of takes us to the end of the boost converter.
[00:16:30.050 - 00:16:37.050] We've looked at its operation, basic analysis, and some design criteria associated with it.
[00:16:37.050 - 00:16:44.050] There is one more of the fundamental DC to DC converters that we should have a look at.
[00:16:44.050 - 00:16:50.050] And its function is again, ever so slightly different to the previous two that we've considered.
[00:16:50.050 - 00:16:53.050] And that's the buck boost converter.
[00:16:53.050 - 00:17:01.860] And this is so wildly different in configuration to the other two, especially the boost converter,
[00:17:01.860 - 00:17:10.860] where the only change between the boost converter and the buck boost converter is the direction of the diode.
[00:17:10.860 - 00:17:13.860] So in the boost converter, the diode is the other way around.
[00:17:13.860 - 00:17:18.970] So we need difference.
[00:17:18.970 - 00:17:22.970] But this operation changes quite significantly because of that.
[00:17:22.970 - 00:17:36.370] As the name might suggest, the difference now in the operation is that this converter is the first that we've come across that is able to both
[00:17:36.370 - 00:17:41.370] step down the output voltage relative to the input and boost it up.
[00:17:41.370 - 00:17:51.810] So it's quite a versatile converter, depending on the sort of load or output changes that we may experience.
[00:17:51.810 - 00:18:03.810] So great one actually for maintaining a constant output voltage, given a changing input DC value, say from a discharging battery.
[00:18:03.810 - 00:18:09.810] So perhaps you'll try to keep an output voltage that's constant at 12 volts.
[00:18:09.810 - 00:18:14.810] And the battery input, when it's fully charged, maybe give you say 14 volts or so.
[00:18:14.810 - 00:18:20.810] And then as it discharges, it drops below 12 volts and goes maybe down to 10 volts.
[00:18:20.810 - 00:18:35.430] This type of boost converter would be able to keep you at a completely constant output 12 volts, even though the source voltage went from being greater than the output voltage to less than the output voltage.
[00:18:35.430 - 00:18:42.360] Okay.
[00:18:42.360 - 00:18:51.360] Analysis, we're going to base everything that we've come to expect from this type of systems where it's the steady state properties.
[00:18:51.360 - 00:19:02.820] Everything is periodic and repeated exactly the same for every period.
[00:19:02.820 - 00:19:14.820] So you'll be happy to know that the analysis regarding the converter with the switch closed is the same as it is for the boost converter.
[00:19:14.820 - 00:19:26.820] So with the controllable switch closed from where it's positioned, we have the inductor connected directly to the voltage source.
[00:19:26.820 - 00:19:31.820] So current range is up and we're putting energy into that inductor.
[00:19:31.820 - 00:19:32.820] All right.
[00:19:32.820 - 00:19:37.820] So di by dt is just the voltage source divided by the inductance.
[00:19:37.820 - 00:19:44.170] And the amount of current change is just VS dt.
[00:19:44.170 - 00:19:50.170] So that's the period of time that we have the switch closed over L times that source voltage.
[00:19:50.170 - 00:19:51.170] That's the same.
[00:19:51.170 - 00:19:57.170] It's identical expression behavior as we have with the boost converter.
[00:19:57.170 - 00:20:03.720] The difference comes in when we open the switch.
[00:20:03.720 - 00:20:19.420] For the boost converter, when you open the switch, the inductor ends up being in series with the source.
[00:20:19.420 - 00:20:20.420] Right.
[00:20:20.420 - 00:20:22.420] But we don't have that for the back boost.
[00:20:22.420 - 00:20:33.420] When we open the switch, the output now that we have the diode, which is this way around conducting,
[00:20:33.420 - 00:20:38.420] is effectively the same kind of configuration as the back converter.
[00:20:38.420 - 00:20:43.420] Hence the reason we are able to go from the stepping down to stepping up operation.
[00:20:43.420 - 00:20:49.780] But something looks weird here.
[00:20:49.780 - 00:20:52.780] Plus minus plus minus diode in this direction.
[00:20:52.780 - 00:20:57.780] The only way that conducts is if the current is that way.
[00:20:57.780 - 00:21:06.610] Well, we know that if current is that way, and this is the closed loop now, then that's the current this way.
[00:21:06.610 - 00:21:11.610] This way this way and this way.
[00:21:11.610 - 00:21:21.810] What that's telling us is that although the convention is telling us that this is the voltage polarity,
[00:21:21.810 - 00:21:28.810] the actual voltage. Remember, just before with the switch closed, plus minus.
[00:21:28.810 - 00:21:32.810] We've got energy coming into the inductor.
[00:21:32.810 - 00:21:36.810] What does the inductor do when we disconnect it from the source?
[00:21:36.810 - 00:21:46.270] Its voltage flips and it becomes a source of energy with the current flowing in the same direction, which was that way.
[00:21:46.270 - 00:21:51.270] So positive negative in reality, its plus minus.
[00:21:51.270 - 00:22:03.350] So that means that relative to the input voltage polarity, the output voltage is reverse polarity.
[00:22:03.350 - 00:22:11.780] So just be aware of this because this is a common line all the way through.
[00:22:11.780 - 00:22:20.780] So if that was grounded, for example, and is it zero volts, then the output would be a negative voltage relative to zero volts.
[00:22:20.780 - 00:22:27.760] So it's got a handy function. You can step up, step down the voltage.
[00:22:27.760 - 00:22:35.760] But the thing that you've got to keep an eye on is that the output voltage will be a negative from the input voltage.
[00:22:35.760 - 00:22:49.940] Okay. Using the sign convention that we have here, since the voltage across the inductor is the same as it is across the load,
[00:22:49.940 - 00:22:56.150] is BL, LDI by DT equals V out.
[00:22:56.150 - 00:23:03.150] All constants, so the derivative, time derivative of that is constantly ramping down while the switch is open.
[00:23:03.150 - 00:23:14.150] We have this expression, which I could just said since the configuration is just like it is for the buck converter with the de-energizing inductor.
[00:23:14.150 - 00:23:17.150] That expression is the same as it is for the buck converter.
[00:23:17.150 - 00:23:23.150] So at least in the state for this converter, we are kind of just mixing and matching a little bit.
[00:23:23.150 - 00:23:32.570] So expressions that we've already got for either the buck converter or the bus converter.
[00:23:32.570 - 00:23:43.570] So how does that then work together to give us our overall output voltage magnitude relative to the input voltage?
[00:23:43.570 - 00:23:53.310] Well, we end up with this D over 1 minus D scaling.
[00:23:53.310 - 00:24:04.310] And with small values of D or values of D less than 0.5, this ratio will attenuate the signal.
[00:24:04.310 - 00:24:11.310] It's less than 1. And if you have 0.5 and above, then this will be greater than 1.
[00:24:11.310 - 00:24:20.310] Right? So here's the negative coming into the expression which identifies that the output voltage is reverse polarity from the input voltage.
[00:24:20.310 - 00:24:33.710] There's no magic in how this is done. We just apply exactly the same process we've done every time.
[00:24:33.710 - 00:24:39.710] The changing current for the switch close is equal to the changing current when the switch is open and magnitude.
[00:24:39.710 - 00:24:42.710] Once just ramping up, the other one's ramping down.
[00:24:42.710 - 00:24:49.450] So that's part of the analysis.
[00:24:49.450 - 00:24:56.450] And then we move on now to consideration of some design elements to do with the buck boost converter.
[00:24:56.450 - 00:25:00.450] First up, how do we keep the inductor current continuous?
[00:25:00.450 - 00:25:07.450] We still want that to be continuous as we have for our two previous converters.
[00:25:07.450 - 00:25:18.730] Well, it becomes somewhat, I guess, a redundant exercise.
[00:25:18.730 - 00:25:28.730] We could go through it formally again, but since we have with the switch close the same situation for a boost converter,
[00:25:28.730 - 00:25:37.730] to keep that inductor current continuous, it turns out that it looks exactly like the boost converter.
[00:25:37.730 - 00:25:41.730] Right? So we're that current just touches on 0. We have this expression.
[00:25:41.730 - 00:25:49.330] We go through buck boost. But that's the same expression we had for the boost converter.
[00:25:49.330 - 00:25:56.330] Right? So nothing new there. It still has a worst case situation of the duty ratio being equal to 0.5.
[00:25:56.330 - 00:26:21.630] Right? What about the voltage ripple? If we look at the same charge relationship for the voltage on a capacitor,
[00:26:21.630 - 00:26:24.630] it actually turns out to be the same as it is for the boost converter.
[00:26:24.630 - 00:26:33.220] So this expression again is the same as it is for the boost converter.
[00:26:33.220 - 00:26:42.220] It's still the voltage ripple at the output, which had considerations of what was going on in the input with the power
[00:26:42.220 - 00:26:49.020] inductor. Okay? So that's also the same.
[00:26:49.020 - 00:26:56.020] So we've done now three of our basic converters. So we've had the buck, the boost, and the buck boost.
[00:26:56.020 - 00:27:04.330] The analysis has been relatively straightforward. I don't know there's quite a lot to kind of take on and remember as we go through.
[00:27:04.330 - 00:27:12.330] There's not been these wildly complicated expressions or derivations that we've gone through.
[00:27:12.330 - 00:27:21.470] Partly, the reason for that is that we've taken these components to be ideal. Right?
[00:27:21.470 - 00:27:27.470] So 0 voltage across the switches when they're conducting. Right?
[00:27:27.470 - 00:27:33.470] There's no forward voltage drop across the diode when it's conducting. It's an ideal diode.
[00:27:33.470 - 00:27:39.470] The behavior of the switching is ideal. It immediately turns on and immediately turns off.
[00:27:39.470 - 00:27:48.470] So what happens to the operation of these converters? If we start at least thinking, if not fully analyzing,
[00:27:48.470 - 00:27:56.470] is that thinking about what happens when we do introduce some of the more common types of non-ideal behavior in the converters?
[00:27:56.470 - 00:28:16.420] Considering that we have primarily been focusing on the voltage elements between input to output,
[00:28:16.420 - 00:28:26.420] then we'll have a look at effectively what goes on voltage wise when we start looking at some of these non-ideal behaviors.
[00:28:26.420 - 00:28:38.500] Especially the switch voltage drop and the losses associated with them. Understanding that they have finite impedance in their own state.
[00:28:38.500 - 00:28:45.500] Right? So real switches, semiconductor switches have non-zero impedance and there is some voltage drop.
[00:28:45.500 - 00:28:50.500] They take a non-zero time to switch on and to switch off. Right?
[00:28:50.500 - 00:28:57.500] So non-zero voltage switch affects the output voltage. Maybe if we just consider the buck converter.
[00:28:57.500 - 00:29:06.500] If the switch voltage in its own state is given as v sub q. Right?
[00:29:06.500 - 00:29:15.500] q is quite often used as a symbol to symbolize a transistor. So v sub q.
[00:29:15.500 - 00:29:20.500] And the diode voltage in its own state is given as vd.
[00:29:20.500 - 00:29:24.500] We often use that to identify the diode forward voltage drop.
[00:29:24.500 - 00:29:30.500] Then the output voltage will be for a buck converter is vs times d. Sure.
[00:29:30.500 - 00:29:33.500] That's what our analysis has told us.
[00:29:33.500 - 00:29:44.620] But you take these factors into consideration minus the average voltage across the transistor whilst it's on.
[00:29:44.620 - 00:29:48.620] So that's multiplied by d, the duty ratio.
[00:29:48.620 - 00:29:55.620] Minus the average voltage across the diode wind that is on, which is during period 1 minus d.
[00:29:55.620 - 00:30:04.060] Right? Which since we're subtracting some finite value of voltage from the ideal then of course the output voltage.
[00:30:04.060 - 00:30:15.740] Because of these finite voltage drops across this which is less than what the duty ratio would tell us it is.
[00:30:15.740 - 00:30:22.740] Yeah? Okay. So that has an effect on the overall voltage that we expect.
[00:30:22.740 - 00:30:29.460] Especially if we consider that for low voltage converters.
[00:30:29.460 - 00:30:33.460] So maybe your output voltage is actually quite low for 5 volts or something.
[00:30:33.460 - 00:30:42.460] Or if we've got really high current converters, you know, you're getting up into the 500 watts a kilowatt region.
[00:30:42.460 - 00:30:47.460] Then the switch voltages can become quite the significant percentage of the output voltage.
[00:30:47.460 - 00:30:56.460] And you would really need to then start including those non ideal features or factors into your calculations and your analysis.
[00:31:01.170 - 00:31:05.170] Okay. So that's voltage drops across the switches.
[00:31:05.170 - 00:31:10.170] What about the finite losses associated with those switches themselves?
[00:31:10.170 - 00:31:14.170] So dissipating energy.
[00:31:14.170 - 00:31:22.170] Right. Switching losses then occur whenever both the current and voltage associated with the switches are non-zero.
[00:31:22.170 - 00:31:24.170] So that's switching losses.
[00:31:24.170 - 00:31:29.170] But I just want to identify here what we're talking about with those drops.
[00:31:29.170 - 00:31:31.170] Those are conduction losses.
[00:31:31.170 - 00:31:35.170] So there's a finite voltage drop across our switch with current flowing through it.
[00:31:35.170 - 00:31:38.170] So we've got voltage current product.
[00:31:38.170 - 00:31:48.590] So that is known as conduction loss.
[00:31:48.590 - 00:31:49.590] Switching loss.
[00:31:49.590 - 00:31:55.590] Now this is whenever we have current and voltage with the switch when they're non-zero.
[00:31:55.590 - 00:31:59.590] So voltage and current at the same time means there's power dissipated.
[00:31:59.590 - 00:32:03.590] All right. And since the switch itself, it's not a source of power.
[00:32:03.590 - 00:32:09.590] So that means we're dissipating that power is heat.
[00:32:09.590 - 00:32:15.590] All right. So we've got two situations where we might have this occurring.
[00:32:15.590 - 00:32:17.590] And this is where we are transitioning.
[00:32:17.590 - 00:32:21.590] So for here we've got a switch that's turning on.
[00:32:21.590 - 00:32:24.590] So it's voltage is dropping across it.
[00:32:24.590 - 00:32:26.590] So this is turning on.
[00:32:26.590 - 00:32:29.590] And the current through it increases.
[00:32:29.590 - 00:32:37.590] There's a finite time that it takes for both those two occur for either the voltage to drop or the current to rise.
[00:32:37.590 - 00:32:41.590] And then on the other side when you turn the switch off, then the voltage takes a finite time to rise.
[00:32:41.590 - 00:32:43.590] And the current takes a finite time to drop.
[00:32:43.590 - 00:32:50.450] The product between the current and the voltage will result in a curve that looks like this.
[00:32:50.450 - 00:32:53.450] That peaks whenever we're doing the switching transition.
[00:32:53.450 - 00:33:02.140] You might notice in this graph that there is this small offset.
[00:33:02.140 - 00:33:09.270] OK. These are your switching losses.
[00:33:09.270 - 00:33:11.270] This is your conduction loss.
[00:33:11.270 - 00:33:25.850] One scenario where halfway through the transition is kind of where you, the timing,
[00:33:25.850 - 00:33:32.930] so delta t, is where you get across over between the current and the voltage.
[00:33:32.930 - 00:33:37.930] They're sort of like, are occurring at exactly the same time.
[00:33:37.930 - 00:33:44.930] In power electronic circuits that have significant amounts of other non-ideal elements
[00:33:44.930 - 00:33:47.930] that store energy like stray inductance and capacitance,
[00:33:47.930 - 00:33:53.930] it is almost never the case that you have a practical circuit that does this.
[00:33:53.930 - 00:33:58.930] Much more common is something that approaches this behavior.
[00:33:58.930 - 00:34:05.930] When you're doing a switching transition, before turning the switch on,
[00:34:05.930 - 00:34:07.930] the current, you turn the switch on.
[00:34:07.930 - 00:34:09.930] You give it a signal, turn on.
[00:34:09.930 - 00:34:12.930] The current rises, but the voltage stays high.
[00:34:12.930 - 00:34:17.930] It's not until you reach the final state of current that the voltage actually starts to drop.
[00:34:17.930 - 00:34:20.930] Delta t is much larger.
[00:34:20.930 - 00:34:29.800] You end up with this considerably larger amount of switching loss.
[00:34:29.800 - 00:34:35.050] These are the two situations that are identified.
[00:34:35.050 - 00:34:41.050] Like I sat in here in real circuits with non-ideal behavior,
[00:34:41.050 - 00:34:52.350] you tend to end up with circuits that behave like this, not this.
[00:34:52.350 - 00:34:57.350] I think this is a really, really nice, I guess,
[00:34:57.350 - 00:35:03.350] pictorial representation of how switching losses start to dominate
[00:35:03.350 - 00:35:07.350] when the frequency increases the switching frequency.
[00:35:07.350 - 00:35:15.350] When the switching frequency increases, the time period between having these switching losses reduces.
[00:35:15.350 - 00:35:17.350] It's happened more often.
[00:35:17.350 - 00:35:21.350] You've got this lower amount of conduction loss that's been on,
[00:35:21.350 - 00:35:24.350] usually on for a longer period of time.
[00:35:24.350 - 00:35:27.350] Conduction losses dominate at low frequency,
[00:35:27.350 - 00:35:34.350] but at higher frequencies when this starts to encroach and becomes on average occurs more often,
[00:35:34.350 - 00:35:37.350] then switching frequency, as switching losses, take over.
[00:35:37.350 - 00:35:47.760] Right.
[00:35:47.760 - 00:35:53.760] So it's not just the semiconductor switches that are non-ideal.
[00:35:53.760 - 00:36:00.170] They're about the other main players in our circuits, the capacitors and the inductors.
[00:36:00.170 - 00:36:03.170] Well, let's take the capacitor first.
[00:36:03.170 - 00:36:07.170] So capacitors, when we construct them and we build them,
[00:36:07.170 - 00:36:11.170] they have some parasitic elements to them.
[00:36:11.170 - 00:36:14.170] They're not just a pure capacitance with a particular value.
[00:36:14.170 - 00:36:22.170] They have some equivalent series resistance and equivalent series inductance as well.
[00:36:22.170 - 00:36:28.580] So the apparent they're not particularly significant.
[00:36:28.580 - 00:36:33.580] The equivalent series resistance of capacitances tends to be quite a small value,
[00:36:33.580 - 00:36:35.580] but not zero.
[00:36:35.580 - 00:36:40.580] And the equivalent series inductance also tends to be a relatively small value, but again, not zero.
[00:36:40.580 - 00:36:47.040] So if we have quite a lot of capacitors current,
[00:36:47.040 - 00:36:52.420] as we've indicated that may be the case for our converters,
[00:36:52.420 - 00:36:59.420] then if there's a finite series resistance associated with that capacitor,
[00:36:59.420 - 00:37:06.420] then there will be a voltage drop associated with that current flowing through that resistance.
[00:37:06.420 - 00:37:10.420] Not only that, being a resistance is going to be i squared r,
[00:37:10.420 - 00:37:13.420] heating or losses within that capacitor.
[00:37:13.420 - 00:37:18.790] They'll get warm because of that resistance.
[00:37:18.790 - 00:37:19.790] Right.
[00:37:19.790 - 00:37:28.860] So we end up with more voltage ripple because of this series resistance.
[00:37:28.860 - 00:37:32.860] The inductance represents a bit of a different problem.
[00:37:32.860 - 00:37:37.860] So if you've got a capacitor,
[00:37:37.860 - 00:37:40.860] which is the ideal part of that capacitance,
[00:37:40.860 - 00:37:46.860] but then we have a small amount of resistance that's our ESR.
[00:37:46.860 - 00:37:52.860] And then we have a small amount of inductance, which is our ESL.
[00:37:52.860 - 00:38:00.860] We've got a circuit which is effectively a lightly-damped series resonance circuit.
[00:38:00.860 - 00:38:09.650] And these tend to be put into converter circuits that we're switching on and off.
[00:38:09.650 - 00:38:16.650] So they experience very rapid DV by DT and DI by DT transients or transitions,
[00:38:16.650 - 00:38:19.650] which behave like step drivers,
[00:38:19.650 - 00:38:24.650] step response drivers for both that RC resonant circuit.
[00:38:24.650 - 00:38:36.260] So it has a certain resonant frequency.
[00:38:36.260 - 00:38:39.260] If that is excited by the switching operation,
[00:38:39.260 - 00:38:44.260] then you'll find that the output voltage can be really substantially attenuated
[00:38:44.260 - 00:38:48.260] if we hit that resonant condition.
[00:38:48.260 - 00:38:51.260] Not only that, you could get oscillating waveforms
[00:38:51.260 - 00:38:55.260] where you're expecting something that's nice and constant.
[00:38:55.260 - 00:39:00.260] That type of behavior generally only gets observed in the hundreds of kilohertz,
[00:39:00.260 - 00:39:02.260] switching frequency range.
[00:39:02.260 - 00:39:05.260] So again, it's one of those.
[00:39:05.260 - 00:39:08.260] I was talking about the back converter for the solar car project.
[00:39:08.260 - 00:39:09.260] And I said, pops out.
[00:39:09.260 - 00:39:12.260] I don't recommend going any higher than 100 kilohertz.
[00:39:12.260 - 00:39:15.260] It's starting to get up into that higher region.
[00:39:15.260 - 00:39:29.120] All these non-ideal behaviors start to actually make a difference.
[00:39:29.120 - 00:39:31.120] What about the inductor?
[00:39:31.120 - 00:39:33.120] The inductor, that's the power inductor,
[00:39:33.120 - 00:39:40.620] is one of the prominent pieces of our switch mode converters that we've been looking at.
[00:39:40.620 - 00:39:46.620] Well, the inductor is physically made by a coil of wire around the magnetic material.
[00:39:46.620 - 00:39:51.580] It has finite resistance.
[00:39:51.580 - 00:39:59.580] So that actually has a bit of an effect on the behavior of our converter.
[00:39:59.580 - 00:40:05.580] Especially if we're trying to achieve for our boost converter,
[00:40:05.580 - 00:40:08.580] a high-step ratio.
[00:40:08.580 - 00:40:16.500] So here's our boost converter.
[00:40:16.500 - 00:40:19.500] We're trying to get an output voltage, which is considerably larger,
[00:40:19.500 - 00:40:20.500] the input voltage.
[00:40:20.500 - 00:40:24.500] So we would end up with a duty ratio that tends to be on the higher end,
[00:40:24.500 - 00:40:28.910] and we would end up getting up close to one.
[00:40:28.910 - 00:40:34.910] But if we include a small amount of series resistance,
[00:40:34.910 - 00:40:37.910] that's a non-ideal part of that inductor,
[00:40:37.910 - 00:40:40.910] it starts to dissipate the certain amount of power.
[00:40:40.910 - 00:40:47.120] And if we wanted to go through the full analysis,
[00:40:47.120 - 00:40:51.120] we could show that the output voltage is equal to,
[00:40:51.120 - 00:40:55.120] that's the normal expression for a boost converter.
[00:40:55.120 - 00:41:00.120] But has an effect,
[00:41:00.120 - 00:41:06.120] including it, that is dependent on that series resistance of the inductor.
[00:41:06.120 - 00:41:11.850] This capital R is the load resistance.
[00:41:11.850 - 00:41:25.200] So this tells us that if our L increases,
[00:41:25.200 - 00:41:27.200] you've got this expression,
[00:41:27.200 - 00:41:33.200] if that's an increasing value, then this expression decreases.
[00:41:33.200 - 00:41:47.720] So we end up decreasing the output voltage.
[00:41:47.720 - 00:41:51.720] Not only that, we've got a duty ratio,
[00:41:51.720 - 00:41:54.720] expression hits one minus D squared,
[00:41:54.720 - 00:42:00.720] but it's one over one over essentially.
[00:42:00.720 - 00:42:16.470] So as D increases, we have one minus D squared,
[00:42:16.470 - 00:42:27.810] and that reduces V out at a rate of around one minus D.
[00:42:37.690 - 00:42:44.180] So as D gets large, this dominates.
[00:42:44.180 - 00:42:48.180] So you end up with a one over D squared,
[00:42:48.180 - 00:42:52.180] which turns to be one minus D, sorry, squared,
[00:42:52.180 - 00:42:56.180] which would be equivalent to one minus D squared
[00:42:56.180 - 00:42:59.180] here divided by one minus D.
[00:42:59.180 - 00:43:03.180] So you left with just one minus D.
[00:43:03.180 - 00:43:09.180] So it scales the output voltage by one minus D at higher duty ratios,
[00:43:09.180 - 00:43:12.180] which is the exact opposite to what we're expecting
[00:43:12.180 - 00:43:17.060] for increasing duty ratio.
[00:43:17.060 - 00:43:21.060] So what has that plotted out on the next slide?
[00:43:21.060 - 00:43:26.340] So the implications are pretty dramatic
[00:43:26.340 - 00:43:29.340] for our boost converter, for having a series resistance
[00:43:29.340 - 00:43:34.800] for that inductor.
[00:43:34.800 - 00:43:37.800] So firstly, as I just said, for an increasing RL,
[00:43:37.800 - 00:43:39.800] the output voltage decreases.
[00:43:39.800 - 00:43:45.980] It's not usually too bad because RL is small,
[00:43:45.980 - 00:43:49.980] but secondly and most importantly, the duty ratio increases
[00:43:49.980 - 00:43:53.980] when we try to increase it, the honest point,
[00:43:53.980 - 00:43:55.980] it actually does exactly the opposite.
[00:43:55.980 - 00:44:01.980] It drives it to a smaller value at a rate of about one minus D.
[00:44:01.980 - 00:44:11.980] A smaller, just so that you get an idea,
[00:44:11.980 - 00:44:13.980] say we had a smaller RL,
[00:44:13.980 - 00:44:16.980] we would have a curve that follows the ideal
[00:44:16.980 - 00:44:18.980] for a little bit longer.
[00:44:18.980 - 00:44:21.980] We get a bit more voltage increase,
[00:44:21.980 - 00:44:25.980] but eventually it still has the effect
[00:44:25.980 - 00:44:31.980] of reducing down at higher duty ratios.
[00:44:31.980 - 00:44:37.450] So smaller.
[00:44:37.450 - 00:44:52.210] So again, things that can occur,
[00:44:52.210 - 00:44:56.210] and we've got to keep an eye on if we are going to start pushing
[00:44:56.210 - 00:45:07.730] the boundaries of the operation of the componentry.
[00:45:07.730 - 00:45:10.730] Finally, transients.
[00:45:10.730 - 00:45:15.730] This encapsulates quite a few things that can be going on
[00:45:15.730 - 00:45:17.730] with the power-ut-finite converter.
[00:45:17.730 - 00:45:21.730] But we'll kind of keep it constrained a little.
[00:45:21.730 - 00:45:25.730] The transients, we're going to consider
[00:45:25.730 - 00:45:27.730] as mostly our start-up transients.
[00:45:27.730 - 00:45:30.730] So the very first time you turn on the converter.
[00:45:30.730 - 00:45:32.730] Remember I've been talking about the analysis.
[00:45:32.730 - 00:45:33.730] We're in steady state.
[00:45:33.730 - 00:45:36.730] We're in steady state, so we don't worry about what kind of
[00:45:36.730 - 00:45:39.730] goes on in the converter when we kind of kick-start it
[00:45:39.730 - 00:45:42.730] from everything being zero.
[00:45:42.730 - 00:45:45.730] So we get some interesting behavior sometimes,
[00:45:45.730 - 00:45:47.730] and this is transient behavior.
[00:45:47.730 - 00:45:54.460] We can end up with quite some significant voltage spikes
[00:45:54.460 - 00:45:58.460] and current spikes as we turn the converter on.
[00:45:58.460 - 00:46:03.460] That might otherwise damage our components if we don't
[00:46:03.460 - 00:46:06.460] understand that this could happen and
[00:46:06.460 - 00:46:10.460] potentially mitigate those currents and voltages.
[00:46:10.460 - 00:46:14.740] So analysis of transient behavior,
[00:46:14.740 - 00:46:16.740] we're just introducing this stuff.
[00:46:16.740 - 00:46:19.740] It's a little bit beyond the scope of the course.
[00:46:19.740 - 00:46:24.740] Just be aware that they do exist and may prove to be a problem.
[00:46:24.740 - 00:46:28.740] In fact, when you simulate through
[00:46:28.740 - 00:46:31.740] LZ-spice your buck converter operation,
[00:46:31.740 - 00:46:35.740] you'll see that the behavior when you very first start the thing up
[00:46:35.740 - 00:46:37.740] kind of looks a little wonky.
[00:46:37.740 - 00:46:41.740] And you don't look at the behavior too much.
[00:46:41.740 - 00:46:46.560] You look at what happens once everything settles down.
[00:46:46.560 - 00:46:49.560] Just as we said, that transitive fix,
[00:46:49.560 - 00:46:53.560] one of the things that we often do to mitigate the high
[00:46:53.560 - 00:46:57.560] currents and voltages at the start is to what's called
[00:46:57.560 - 00:46:59.560] employees soft starting.
[00:46:59.560 - 00:47:01.560] So we know it's going to occur.
[00:47:01.560 - 00:47:04.560] So we rather than just go boom with the duty ratio that we want
[00:47:04.560 - 00:47:09.560] for the output, we ramp up or slowly increase the duty ratio
[00:47:09.560 - 00:47:11.560] from zero.
[00:47:11.560 - 00:47:15.560] So that we are managing how fast the energy is put
[00:47:15.560 - 00:47:17.560] into the converter.
[00:47:17.560 - 00:47:19.560] All right, well that's it for today.

# ENMT301-26W Lecture 66 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_66_audio_16k_mono_32k.mp3`
Source audio SHA-256: `41162ab10fd53e14dc335132a135f10d667d83bf138ee71fe47bfe6bebe2d6c3`
Generated: 2026-06-06T07:27:04.500105+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:01 - 00:00:07] I think the law has been under a church.
[00:00:07 - 00:00:11] I think I'm not like a football player.
[00:00:11 - 00:00:13] I don't know.
[00:00:13 - 00:00:15] Oh my god.
[00:00:15 - 00:00:17] I agree.
[00:00:17 - 00:00:19] I'm going to change that.
[00:00:19 - 00:00:21] She doesn't really know what else to do with it.
[00:00:21 - 00:00:23] I do like it.
[00:00:23 - 00:00:27] Okay. Good afternoon to the last lecture for me.
[00:00:27 - 00:00:28] More this day.
[00:00:28 - 00:00:29] It was double.
[00:00:29 - 00:00:30] Yep. Good.
[00:00:30 - 00:00:31] Yeah.
[00:00:31 - 00:00:34] So I'll just start off a bit today with the assignment.
[00:00:34 - 00:00:38] So it's not due to the end of the second week of turn three.
[00:00:38 - 00:00:41] So that's eight weeks away.
[00:00:41 - 00:00:43] How about you won't see me before then.
[00:00:43 - 00:00:46] So the instructions and the files are all up on learn.
[00:00:46 - 00:00:51] I'll just sort of run through briefly what you need to do.
[00:00:51 - 00:00:58] So on the screen on the left, we've got a stupid notebook that's up there.
[00:00:58 - 00:01:00] Who's one of these before?
[00:01:00 - 00:01:01] Yeah. Good.
[00:01:01 - 00:01:04] So it's a way of here.
[00:01:04 - 00:01:12] The Python combining text with snippets of Python of code.
[00:01:12 - 00:01:13] Okay.
[00:01:13 - 00:01:14] So there are two parts of the assignment.
[00:01:14 - 00:01:20] One is dealing with just the IMU with real-time new measurements.
[00:01:20 - 00:01:29] And then the second part, part B, is combining IMU measurements with a domicher measurements to work out where you're robot speed.
[00:01:29 - 00:01:33] Okay.
[00:01:33 - 00:01:39] So the first two parts are done for you.
[00:01:39 - 00:01:44] So the first one is loading up the data file.
[00:01:44 - 00:01:46] So it's a CSV data file.
[00:01:46 - 00:01:49] And then plotting.
[00:01:49 - 00:01:54] IMU is giving you acceleration in three X's, X, Y's, Z.
[00:01:54 - 00:02:00] And there's a JavaScript which is giving you angle speed in three direction, X, Y's, Z as well.
[00:02:00 - 00:02:04] So the first two parts we've done for you.
[00:02:04 - 00:02:07] So loading the file and plotting.
[00:02:07 - 00:02:25] Anyway, here's the angle speed.
[00:02:25 - 00:02:26] What's going wrong?
[00:02:26 - 00:02:29] Let's just close that.
[00:02:29 - 00:02:30] Load a new one.
[00:02:30 - 00:02:31] And leave.
[00:02:31 - 00:02:44] Okay.
[00:02:44 - 00:02:45] Here's the angle speed.
[00:02:45 - 00:02:47] So you can see quite a lot of noise on the measurements.
[00:02:47 - 00:02:54] So different colors, different orientations, X, Y's, Z.
[00:02:54 - 00:03:02] And so also on learn these are templates, either in Word or Latec.
[00:03:02 - 00:03:04] And the templates also want to do.
[00:03:04 - 00:03:11] So for the part A, describe the time sequences, the Scram histograms.
[00:03:11 - 00:03:24] And then you need to write some code yourself.
[00:03:24 - 00:03:35] So for example, we want to calculate the standard deviation of the angle speed in the Z direction.
[00:03:35 - 00:03:38] So hopefully this works.
[00:03:38 - 00:03:43] So in these boxes you just type.
[00:03:43 - 00:03:48] And then if we want to get the standard deviation, we'll do an umpteen at standard deviation.
[00:03:48 - 00:03:53] And of the angle speed and the Z direction.
[00:03:53 - 00:03:58] And then to run that cell that will shift the entire, what do you know?
[00:03:58 - 00:04:00] You get some value.
[00:04:00 - 00:04:02] And then you want to compare that with the data sheet.
[00:04:02 - 00:04:07] You can see if that's in, in bounds for the IAMU.
[00:04:07 - 00:04:08] Okay.
[00:04:08 - 00:04:19] So then we have, you need to integrate and put for the, the,
[00:04:19 - 00:04:24] the angular speed to give you the angle.
[00:04:24 - 00:04:26] So that's the heading.
[00:04:26 - 00:04:35] And then we also try and part five to integrate the acceleration twice to give distance.
[00:04:35 - 00:04:38] And that's going to be problematic as you'll see.
[00:04:38 - 00:04:45] And then in the second part, we give you some odometry here.
[00:04:45 - 00:04:50] So there's a second CSP file, which is up on learn,
[00:04:50 - 00:04:55] future load and then, so this odometry,
[00:04:55 - 00:04:59] so it's the distance versus time is plotted for you.
[00:04:59 - 00:05:02] And you can see this quite a lot of high frequency noise on emissions there.
[00:05:02 - 00:05:10] So you've got to design your own filter to remove that noise before you integrate that.
[00:05:10 - 00:05:15] But before you use that to work out,
[00:05:15 - 00:05:18] there's a path of the robot.
[00:05:18 - 00:05:24] So first thing to do is then, we can take for a transform of this to work out what the interference frequencies are.
[00:05:24 - 00:05:30] So that's getting the spectrum of the geometry data, filter the odometry data.
[00:05:30 - 00:05:38] And then we're going to combine the angular speeds and the odometry to get the path of the robot.
[00:05:38 - 00:05:43] So it's not a huge amount of work, it's only five percent assignment,
[00:05:43 - 00:05:48] but it should hopefully be useful for the robot assignment.
[00:05:48 - 00:05:53] And it'll be used to doing filtering and things in Python as well.
[00:05:53 - 00:05:56] So it means to be a huge amount of work.
[00:05:56 - 00:05:58] There's a forum on learn.
[00:05:58 - 00:06:01] We can ask questions as well.
[00:06:01 - 00:06:07] And then, right hand side, I've got the instructions as well.
[00:06:07 - 00:06:12] So there are instructions about how to download these Jupyter notebooks.
[00:06:12 - 00:06:15] So I'm writing online computer, files in the corner.
[00:06:15 - 00:06:17] And a calendar.
[00:06:17 - 00:06:22] You can also do it through Visual Studio, VS Code,
[00:06:22 - 00:06:25] there's a question that I'm going to do.
[00:06:25 - 00:06:33] And then, you can also use either the Mcetronus Lab or the CE Lab,
[00:06:33 - 00:06:41] in which one's your narrowing that have an a calendar and Microsoft VS Code on there.
[00:06:41 - 00:06:43] You can also remote into those labs.
[00:06:43 - 00:06:46] And then also online Jupyter notebooks.
[00:06:46 - 00:06:52] So there's multiple different ways to do it.
[00:06:52 - 00:06:57] And then, there's this templates.
[00:06:57 - 00:06:58] So I open here.
[00:06:58 - 00:07:01] So you should end up with a report of about five pages.
[00:07:01 - 00:07:09] So each part, you're plotting the spectrum, you're writing a paragraph about it.
[00:07:09 - 00:07:11] It's not only a huge amount of data.
[00:07:11 - 00:07:16] And you do this time it by itself, not in a group.
[00:07:16 - 00:07:21] And then, in terms of what you need to submit,
[00:07:21 - 00:07:28] it's this PDF document, which has your figures and your descriptions of the figures.
[00:07:28 - 00:07:33] And then also the code as well.
[00:07:33 - 00:07:39] So the code is not itself marked, but it's just as though there's any questions about
[00:07:39 - 00:07:44] plagiarism or what have you, then we can go back and check that you've actually done the calculations yourselves
[00:07:44 - 00:07:46] in the submitted code.
[00:07:46 - 00:07:51] So it's two five o'clock on a Friday, 24th of July.
[00:07:51 - 00:07:57] And I've just highlighted from the course outline what the penalty process is.
[00:07:57 - 00:08:02] So you want to submit it by five o'clock, otherwise you get back to that.
[00:08:02 - 00:08:10] And then, lastly, and quite importantly, I guess, is what you can do with your AI robot friends.
[00:08:10 - 00:08:15] So basically, it's helping not doing your assignment.
[00:08:15 - 00:08:23] So you can write your report yourself first, and then use it to correct your spelling and grammar and things like that.
[00:08:23 - 00:08:26] Or providing feedback on what you've written.
[00:08:26 - 00:08:33] And you can also use it for doing research like, you wouldn't with Google five years ago,
[00:08:33 - 00:08:40] so how you get the annual speed, the heading from the angular speed and things like that
[00:08:40 - 00:08:44] or finding out more information about the integration functions and Python.
[00:08:44 - 00:08:55] And you can get it to help debug and edit your code, but you need to write the first version yourself, otherwise getting anything out of the assignment.
[00:08:55 - 00:08:58] Okay, so that's everything I want to say about this summit.
[00:08:58 - 00:09:02] Any questions that immediately come to mind?
[00:09:02 - 00:09:07] No, okay, good.
[00:09:07 - 00:09:11] So you've got time for that.
[00:09:11 - 00:09:14] So just shut this down.
[00:09:14 - 00:09:39] Then, over to doing the last little extra slides.
[00:09:39 - 00:09:40] Okay.
[00:09:40 - 00:09:59] So I think you want to get 10 slides here on multi-mases and oscilloscopes, right on the other front.
[00:09:59 - 00:10:02] So not to be filled in.
[00:10:02 - 00:10:09] Okay, so this relates, I guess, to your aerobic assignment as well,
[00:10:09 - 00:10:13] how you're analyzing signals and testing things.
[00:10:13 - 00:10:19] Okay, so we'll start off with multi-mases.
[00:10:19 - 00:10:21] So on the left here, we've got multi-meter.
[00:10:21 - 00:10:27] So we've got this column here that's kind of a common path.
[00:10:27 - 00:10:32] And then we can now choose here, measuring voltage or impedance.
[00:10:32 - 00:10:35] And the one on the left here is current.
[00:10:35 - 00:10:42] Okay, so if we look at a circuit diagram of a multi-meter,
[00:10:42 - 00:10:51] we've got the switch here between measuring voltage and measuring current.
[00:10:51 - 00:10:56] Okay, so this is a common port here.
[00:10:56 - 00:11:04] Okay, so we've got two, so we can switch between a voltmeter or an ammeter essentially.
[00:11:04 - 00:11:15] And then as a switch between the current measurement,
[00:11:15 - 00:11:29] as of the right-hand side, we've got a voltmeter in parallel with a large resistor.
[00:11:29 - 00:11:38] Because when we're measuring the voltage, we want to make sure that we don't change the voltage in the circuit.
[00:11:38 - 00:11:46] So that is then the voltmeter has a large impedance to do that.
[00:11:46 - 00:11:53] And on the left-hand side, for measuring current, we then have an ammeter.
[00:11:53 - 00:12:01] And that is the current across a small resistor.
[00:12:01 - 00:12:05] Okay, so that resistor is typically less than an ohm.
[00:12:05 - 00:12:16] Okay, so the key thing with using the multi-makers is that we don't measure voltage from the current setting.
[00:12:16 - 00:12:19] Because otherwise we're putting a large voltage over a really small resistor.
[00:12:19 - 00:12:22] We're then able to really large current.
[00:12:22 - 00:12:26] And we'll either blow off views or continue to destroy the multi-meter.
[00:12:26 - 00:12:36] How many multi-makers do you reckon get destroyed on the megatronics lab each year?
[00:12:36 - 00:12:42] That's the number I've heard from Julian, so they're all from doing the so.
[00:12:42 - 00:12:52] You've got to be really careful from making sure that this is in the right slot,
[00:12:52 - 00:12:55] if we're measuring voltage, and if it's in current, that's over here.
[00:12:55 - 00:13:04] Okay, then the other thing about multi-makers is that if you're measuring what you think is the main voltage,
[00:13:04 - 00:13:07] it might well give you the DC voltage.
[00:13:07 - 00:13:12] So if I stuck the multi-meter into the jack here, it's going to say zero volts.
[00:13:12 - 00:13:14] That's the DC value.
[00:13:14 - 00:13:16] Doesn't mean there's no voltage in there.
[00:13:16 - 00:13:21] So you need to be careful when you're measuring a main voltage with a multi-meter.
[00:13:21 - 00:13:28] Okay, so that's multi-mitters.
[00:13:28 - 00:13:35] So a little bit about oscilloscopes as well.
[00:13:35 - 00:13:40] Okay, so you have used oscilloscopes in 270, and on the courses.
[00:13:40 - 00:13:46] So one thing about these oscilloscope probes is that they have high capacitance.
[00:13:46 - 00:13:52] So then they can fix the circuit you're measuring.
[00:13:52 - 00:14:00] And they also have, from this ground lead here, they can generate a parasitic in that instance,
[00:14:00 - 00:14:10] the ground lead.
[00:14:10 - 00:14:19] Okay, and if we're producing extra inductance, the oscilloscope won't know if it's from the circuit or the probe,
[00:14:19 - 00:14:23] that's going to then fix our measurement.
[00:14:23 - 00:14:29] So in particular, this inductance within limit bandwidth.
[00:14:29 - 00:14:44] Okay, so these leads have high capacitance of the order of 100 picofarads.
[00:14:44 - 00:14:52] And so then we often use, well, notice 10 times probes that have 1 tenth of the capacitance.
[00:14:52 - 00:14:58] So then these are better for doing high frequency measurements or looking for pulses.
[00:14:58 - 00:15:15] Okay, so one way that we can reduce the capacitance from the probe is to use a voltage divider.
[00:15:15 - 00:15:22] So a capacitive divider here, because we've got capacitors in our voltage divider.
[00:15:22 - 00:15:30] And so we have a resistor and capacitor in parallel here.
[00:15:30 - 00:15:32] So we'll call the said one.
[00:15:32 - 00:15:35] And then this one here is it two.
[00:15:35 - 00:15:42] So on the left we have the input from our circuit coming into our probe.
[00:15:42 - 00:15:45] And then on the right we have the output to the oscilloscope.
[00:15:45 - 00:15:56] Okay, so we're trying to reduce the amount of capacitance.
[00:15:56 - 00:16:02] So we're not affecting the circuit we're measuring.
[00:16:02 - 00:16:11] Okay, so we'll just look briefly at the transfer function of these 10 times probes is.
[00:16:11 - 00:16:23] So this goes back to when we're doing analog filters and transfer functions.
[00:16:23 - 00:16:30] So we've got all this bei, this beout, obvious.
[00:16:30 - 00:16:35] Okay, so the impedance of the capacitor in the capacitor main is one of it.
[00:16:35 - 00:16:43] So here we've got on the output branch we've got the capacitance is nine times bigger.
[00:16:43 - 00:16:53] So we'll call this one over nine s c.
[00:16:53 - 00:17:03] So the transfer function then is equal to the output voltage over the input voltage.
[00:17:03 - 00:17:17] Okay, some impedance said one is in our resistance is nine r.
[00:17:17 - 00:17:21] And this is in parallel with one over s c.
[00:17:21 - 00:17:27] And then impedance, I should have write this one out.
[00:17:27 - 00:17:36] So did one then becomes, if you do a little bit of math, nine r over one plus nine s c r.
[00:17:36 - 00:17:44] And then to a similar except the ratio of the resistance of the capacitance is offset,
[00:17:44 - 00:17:49] as into is equal to r in parallel with nine s c.
[00:17:49 - 00:18:01] So our impedance is zero over one plus nine s c r.
[00:18:01 - 00:18:08] So the z1 is you to have the same denominator, which we'll make simplifying it a bit bigger.
[00:18:08 - 00:18:19] So then to do our voltage divider, the output voltage from the output of s is equal to the impedance across the output.
[00:18:19 - 00:18:28] So that's z2 over the total impedance, which is z1 plus z2 times the input of the i this.
[00:18:28 - 00:18:33] Okay, so those denominators are going to cancel.
[00:18:33 - 00:18:44] So the out of s is going to be equal to r over r plus nine r, the i of s.
[00:18:44 - 00:18:59] And so our density function h of s, which is the output voltage over the input voltage, is the n equal to r over 10r.
[00:18:59 - 00:19:01] So the r is cancelled.
[00:19:01 - 00:19:11] So we'll just left with a constant attenuation.
[00:19:11 - 00:19:21] Okay, so this circuit in your oscilloscope probe is then attenuating the input by factor of 10.
[00:19:21 - 00:19:40] And so the capacitance of our probe is not going to affect as much.
[00:19:40 - 00:19:44] Okay, so hopefully that's good practice for the test as well, doing one of these transfer functions.
[00:19:44 - 00:19:51] So if we look at the schematic of an oscilloscope.
[00:19:51 - 00:19:54] So we've got this ground lead here that we've talked about before.
[00:19:54 - 00:20:04] This is producing some parasitic inductance.
[00:20:04 - 00:20:12] We have this coaxial cable, which is shielded.
[00:20:12 - 00:20:27] So we looked at the photo-reduce parasitic capacitances.
[00:20:27 - 00:20:34] And so on the right hand side we've got our oscilloscope.
[00:20:34 - 00:20:52] And we'll notice here that we've got a variable capacitor, which is used to tune the probe to the oscilloscope.
[00:20:52 - 00:20:55] Okay, so the oscilloscope probe is a screw.
[00:20:55 - 00:21:00] And by turning that screw you're changing the variable capacitor.
[00:21:00 - 00:21:10] And so we need to match the time constant, the Rc from the probe to the oscilloscope.
[00:21:10 - 00:21:26] Okay, so if that capacitor is not set correctly, then the screw away is not going to look right.
[00:21:26 - 00:21:40] So if we input a screw away to the oscilloscope, then if it's under compensated on the left,
[00:21:40 - 00:21:49] we have this sort of rising behavior and then sort of discharge where we can see the capacitor is not right.
[00:21:49 - 00:21:54] On the falling edge and here we've got a little overcompensated.
[00:21:54 - 00:22:04] We've got an overshoot and then discharge of the capacitance during the square-row cycle.
[00:22:04 - 00:22:15] But if we've turned this screw in the oscilloscope probe that changes the variable capacitance to the right point,
[00:22:15 - 00:22:19] then we get what we should see as a square wave.
[00:22:19 - 00:22:26] So on the right here we have the correct compensation.
[00:22:26 - 00:22:33] Okay, so when we connect the probe to the oscilloscope, we need to make sure that it's being properly compensated.
[00:22:33 - 00:22:45] You can do that by testing it with a square wave and making sure that you're getting a square wave on your oscilloscope.
[00:22:45 - 00:22:56] Okay, so lastly for the oscilloscopes, we'll just talk about the triggering, the two main triggering schemes we can use.
[00:22:56 - 00:23:03] Okay, so in normal triggering mode, we can find some trigger level.
[00:23:03 - 00:23:10] So that's the orange line here.
[00:23:10 - 00:23:30] Okay, so when the input, the source crosses that trigger level, then we get a trigger event and then we freeze in this later waveform on the oscilloscope.
[00:23:30 - 00:23:40] Okay, so this is here, so obviously on the x axis here we've got time and on the y axis we've got voltage.
[00:23:40 - 00:23:50] So we've got a waveform and for example we have a UART waveform here.
[00:23:50 - 00:24:03] So this is a bit like with your fun kits in the N-260 last year, you've got normal operations high and then when the message starts we have a start bit here.
[00:24:03 - 00:24:14] So we've got a second from 0 to 1, which is from 1 to 0 as a start and so the high value crosses this trigger level and then the oscilloscope.
[00:24:14 - 00:24:23] We'll see that our trigger event and then we can freeze the waveform in this later on the oscilloscope.
[00:24:23 - 00:24:46] So the normal triggering mode is good if we're trying to capture some transient event or some non repeating signal, but we need to then set up what the trigger level is and for the falling edge or rising edge, etc.
[00:24:46 - 00:24:59] And the other triggering mode which is called the auto mode, so you just push the auto button on the oscilloscope.
[00:24:59 - 00:25:03] Once again this is voltage versus time.
[00:25:03 - 00:25:10] And so the triggering events automatically generated every so often by the oscilloscope.
[00:25:10 - 00:25:23] And so that's good for non transient, non for repeating waveforms, so if you're going to see your D for C waveform or it's not changing then the auto triggering method is fine.
[00:25:23 - 00:25:31] Okay, so that's all the electrical content of GOT.
[00:25:31 - 00:25:35] So you eight people have choice.
[00:25:35 - 00:25:44] Do you want to go and have your arch now or do you want to go through a previous exam, previous exam?
[00:25:44 - 00:25:53] Okay, if anyone wants to leave you can leave, otherwise we can go self-prepared by non-trans test.
[00:25:53 - 00:26:00] The 2023 test is the one I've looked at so you can look at 24 and 25 yourself.
[00:26:00 - 00:26:04] So I've just saved this.
[00:26:04 - 00:26:08] Yes, the previous 40-star or no, the previous one here.
[00:26:08 - 00:26:14] So I just think everything on the learn how to just scroll down.
[00:26:14 - 00:26:19] I think those lecture tutorials and then make your sign at the end test.
[00:26:19 - 00:26:32] And I'm just going to find it myself 23.
[00:26:32 - 00:27:47] I'm going to use my pin to display this.
[00:27:47 - 00:28:16] So we're looking at it.
[00:28:16 - 00:28:21] Okay, good, and I can write it on my PDF here.
[00:28:21 - 00:28:32] Okay, so the first question is digital filters, so we've got an input 402 and we've got an impulse response 1, 4.
[00:28:32 - 00:28:39] Okay, so we're invited that the underlying here means this is the inner zero value.
[00:28:39 - 00:28:49] Okay, we've got a sketchly input sequence.
[00:28:49 - 00:28:54] So we'll plot here.
[00:28:54 - 00:29:06] There's this in, so we've got input 6, x in, so we've got a lot of plot here.
[00:29:06 - 00:29:12] This is inner zero, has a value of 4.
[00:29:12 - 00:29:20] Then 1 is value of 0 and then inner 2 has a value of 2.
[00:29:20 - 00:29:26] Try forward, hopefully.
[00:29:26 - 00:29:27] Yep, good.
[00:29:27 - 00:29:40] Okay, so then we're writing the input sequence as a weighted sum of delayed impulse unit impulses.
[00:29:40 - 00:29:48] So x of n is equal to, so what's the first term going to be equal to?
[00:29:48 - 00:30:01] So for what, yep, delta of n and then the second term, the second value of n is 0, so we can all that.
[00:30:01 - 00:30:07] And in the third one we've got 2 delta, what goes in the brackets.
[00:30:07 - 00:30:09] Yeah, okay, good.
[00:30:09 - 00:30:16] So I'll give a caveat now that there's a set before, it's my first time running force.
[00:30:16 - 00:30:27] Of course, I haven't inherited the official answers of just numbers myself, so hopefully it's alright, but yell out if something looks wrong.
[00:30:27 - 00:30:33] Okay, so determine the z transform of the input sequence.
[00:30:33 - 00:30:39] Okay, so we're going then capital X of z.
[00:30:39 - 00:30:44] Okay, so we can use the linearity theorem.
[00:30:44 - 00:30:52] So we can do the z transform of each term separately.
[00:30:52 - 00:31:01] What's the z transform here of delta of n?
[00:31:01 - 00:31:07] One, yep, that's right, yes, it's like a Fourier transform delta as a p with a constant.
[00:31:07 - 00:31:11] Yep, so for the friend, just goes to 4.
[00:31:11 - 00:31:15] So 2 delta of n goes to 2.
[00:31:15 - 00:31:22] So, but then what do we do this in minus 2 business?
[00:31:22 - 00:31:27] Z to the minus 2, yep, okay, good, so we've got 2 z to the minus 2.
[00:31:27 - 00:31:32] Okay, so my z's have crosses in the middle, not 2's don't.
[00:31:32 - 00:31:57] Okay, my p is actually wrong, but when I was talking I was at right, so, sorry.
[00:31:57 - 00:32:07] Okay, now, to get the output, we can bold the input with the impulsive response.
[00:32:07 - 00:32:17] Okay, so there, but to do this convolution, we can do it two ways, why should it two ways in class?
[00:32:17 - 00:32:24] One, you flip one of the operands, move it across to the multiplications and add.
[00:32:24 - 00:32:28] All we can do this is a matrix multiplication.
[00:32:28 - 00:32:30] You should get the same answer.
[00:32:30 - 00:32:34] So I'm going to do it as a matrix multiplication.
[00:32:34 - 00:32:54] So we're going to multiply our input, which was 402, by our impulse response h of n.
[00:32:54 - 00:33:03] And so the way we write this matrix, this is our h, this is our x on the right h, on the middle.
[00:33:03 - 00:33:05] And this is going to give us y.
[00:33:05 - 00:33:14] So we then have h of n was 1 and 4.
[00:33:14 - 00:33:23] So we have the ones first, and then the fours on the diagonal.
[00:33:23 - 00:33:29] And then all other terms in our matrix.
[00:33:29 - 00:33:37] Zero.
[00:33:37 - 00:33:41] Okay, so then, how big should output be?
[00:33:41 - 00:33:49] Yep, good.
[00:33:49 - 00:33:57] So if you work that out, so the extent of the input is 3, the extent of the impulsive response is 2.
[00:33:57 - 00:34:05] So the extent of the result is then the two extends added together minus 1.
[00:34:05 - 00:34:07] So 3 plus 2 minus 1, because it's 4.
[00:34:07 - 00:34:10] So our y here should be 4.
[00:34:10 - 00:34:14] And then we have to do this matrix multiplication.
[00:34:14 - 00:34:16] So you dive the rows onto the columns.
[00:34:16 - 00:34:21] So you've got n then 4 plus 0 plus 0 is 4.
[00:34:21 - 00:34:26] Then we've got 4 4 is a 16.
[00:34:26 - 00:34:28] And then the next two terms is 0.
[00:34:28 - 00:34:32] So we have 16.
[00:34:32 - 00:34:38] And then we have got 0 times 4, 4 times 0, 1 times 2 is a 2.
[00:34:38 - 00:34:43] And our last term is 0 times 4.
[00:34:43 - 00:35:03] 0 times 0, 4 times 2 is 8.
[00:35:03 - 00:35:06] Okay, so the question was, eggnostic, how you did it?
[00:35:06 - 00:35:16] So I should do it a different ways in the lecture.
[00:35:16 - 00:35:22] Okay, so if we can involve the input signal x of n with this other new sequence,
[00:35:22 - 00:35:27] how what's the extent of our response?
[00:35:27 - 00:35:35] So let's start off with the extent of x-n.
[00:35:35 - 00:35:47] So x-n was 4.02, 16 of x-n is then 3.
[00:35:47 - 00:35:52] So let's do the extent of the other operator.
[00:35:52 - 00:36:00] I'm going to call this actually in here what's the extent of that.
[00:36:00 - 00:36:02] 9.
[00:36:02 - 00:36:04] Any other guesses?
[00:36:04 - 00:36:07] 8.
[00:36:07 - 00:36:08] Yes.
[00:36:08 - 00:36:09] So 0 is the trick.
[00:36:09 - 00:36:13] Because everything before and after is assumed to be 0.
[00:36:13 - 00:36:18] So if there were 0 on the middle, that counts as well as 16.
[00:36:18 - 00:36:25] But if there's one option, one way or the other is not going to count.
[00:36:25 - 00:36:31] So this has then an extent of 8.
[00:36:31 - 00:36:35] So ignore 0 at the end.
[00:36:35 - 00:36:38] Okay, so that was Michael Hayes's trick in that line.
[00:36:38 - 00:36:53] Okay, so then the extent of y of n is equal to 3 plus 8 minus 1 equals 10.
[00:36:53 - 00:37:21] Okay, I'm going to do this non-linear linearly.
[00:37:21 - 00:37:26] So I'm not going to do two digital ones in a row.
[00:37:26 - 00:37:29] I'm going to do the analog one which is question number 5.
[00:37:29 - 00:37:34] And I don't have to do too much writing for it, from it.
[00:37:34 - 00:37:37] Okay, so I'll just show this on the screen as well.
[00:37:37 - 00:37:40] So the first one.
[00:37:40 - 00:37:48] So Michael called the cutoff frequency to the filter the break frequency.
[00:37:48 - 00:37:51] Of course this normally cutoff frequency.
[00:37:51 - 00:37:53] Most people call it a cutoff frequency.
[00:37:53 - 00:37:56] Okay, so we've got this mystery filter here.
[00:37:56 - 00:38:03] And we want to work out what the cutoff frequency of this mystery filter is.
[00:38:03 - 00:38:08] Okay, well, you're opening bit.
[00:38:08 - 00:38:09] What's your guess?
[00:38:09 - 00:38:11] Sorry.
[00:38:11 - 00:38:14] Negro 3 new bit, yes, that's how we do it.
[00:38:14 - 00:38:19] Okay, and so see if you'll match the matches mine.
[00:38:19 - 00:38:22] 600, that's why I did so.
[00:38:22 - 00:38:26] So it's 100, 200, 300, 400, 500, 600.
[00:38:26 - 00:38:32] So this one here.
[00:38:32 - 00:38:37] 600 hits.
[00:38:37 - 00:38:59] Okay, so this is at 3 dB down.
[00:38:59 - 00:39:08] Okay, so what then do we think the order of the mystery filter is second?
[00:39:08 - 00:39:12] Okay, anyone disagree or agree?
[00:39:12 - 00:39:19] It is second, yep, wasn't a quick question.
[00:39:19 - 00:39:23] Okay, I'm just trying to get some information.
[00:39:23 - 00:39:26] Okay, so see if it's all that.
[00:39:26 - 00:39:34] So if you look, say, let's choose a 10 to the 3 here, we've got minus 10 dB.
[00:39:34 - 00:39:41] And in 10 to 4, we've got that minus 15.
[00:39:41 - 00:39:47] Okay, so we've got then 40 dB a decade.
[00:39:47 - 00:39:52] Okay, so you need to justify it.
[00:39:52 - 00:40:01] And that's because as 40 dB a decade, you're probably doing this last night.
[00:40:01 - 00:40:03] We're going to get that.
[00:40:03 - 00:40:17] Okay, if we input 4.2 volts into this filter, what are we going to get out the other
[00:40:17 - 00:40:19] side?
[00:40:19 - 00:40:20] Yeah, good.
[00:40:20 - 00:40:24] Okay, so this is 4.2 volts.
[00:40:24 - 00:40:29] Okay, so that's DZ.
[00:40:29 - 00:40:35] And then it's low pass.
[00:40:35 - 00:40:41] So up here at 0 dB, that means we've got a gain of 1.
[00:40:41 - 00:40:46] Look how 0 dB equals gain of 1.
[00:40:46 - 00:41:11] Okay, so next one, if a 200 kilohertz sinusoid of 1 volt amplitude is applied to the input
[00:41:11 - 00:41:15] filter, determine the amplitude at the output.
[00:41:15 - 00:41:27] This is 0 as my initial answer, and I don't know if I'm right on it, but okay, so
[00:41:27 - 00:41:43] we've got, if we go for 200 here, we've got 2 kilohertz equals minus 20 dB.
[00:41:43 - 00:42:00] So it means that 20 kilohertz, we have minus 60 dB, and then at 200 kilohertz minus 100 dB.
[00:42:00 - 00:42:05] That's pretty much 0, but it's not exactly 0.
[00:42:05 - 00:42:09] I've done my math wrong here, so I don't have the exact answer.
[00:42:09 - 00:42:19] But it's going to be, well, 3 and 10 significant figures you want to do.
[00:42:19 - 00:42:22] And I don't know how the answer was last year, as I say.
[00:42:22 - 00:42:42] So what we've got to do is then, okay, let's say, so we minus 100 dB at 200 kilohertz.
[00:42:42 - 00:43:06] So then we've got 20 log, the base 10 is equal to minus 100.
[00:43:06 - 00:43:16] So then we dive over 20, we've got 20 log 10 of x, as minus 100.
[00:43:16 - 00:43:44] So log to the base 10 of x is minus 5, so that means x is 10 to the minus 5, so this is 1, 2, 3, 4, 5, minus 1, minus 2, minus 3, minus 4, minus 5.
[00:43:44 - 00:43:45] Okay.
[00:43:45 - 00:43:48] And so I don't know if zero is good enough or not.
[00:43:48 - 00:43:56] So you could actually work out a precise answer if you want it.
[00:43:56 - 00:44:07] I think I'd probably give you one and a half or one or something, because if someone did calculate this, then they deserve full maths.
[00:44:07 - 00:44:16] Or maybe I could have a bonus negative to a half or three.
[00:44:16 - 00:44:18] Okay.
[00:44:18 - 00:44:23] Okay.
[00:44:23 - 00:44:26] So write the form of the mystery filters transfer function.
[00:44:26 - 00:44:38] So what we know, we've got a second order low pass, and so we can write, and this is on the formula sheet.
[00:44:38 - 00:44:43] I've given you something.
[00:44:43 - 00:44:54] Okay, so when you do the practice test or the tutorials or whatever you should, and for the measure I always yourselves with these
[00:44:54 - 00:44:57] equations, what do we got?
[00:44:57 - 00:45:10] Pass this one here is describing a second order transfer function.
[00:45:10 - 00:45:22] So H of S is equal to, I'm not squared over this squared plus 2 eta.
[00:45:22 - 00:45:27] I'm going to not S plus I'm going to not squared.
[00:45:27 - 00:45:37] Okay.
[00:45:37 - 00:45:42] Last year, obviously they had a cheat sheet.
[00:45:42 - 00:45:45] So it's a bit of a silly question if you've got a cheat sheet because you're just writing down off your cheat sheets.
[00:45:45 - 00:45:47] I don't know what the point is.
[00:45:47 - 00:45:49] But anyway, it's not my question.
[00:45:49 - 00:45:50] Okay.
[00:45:50 - 00:45:52] So it's two questions.
[00:45:52 - 00:45:55] We can have time for one more.
[00:45:55 - 00:45:56] We can do.
[00:45:56 - 00:45:59] Oh, that's the source of code.
[00:45:59 - 00:46:00] So we just did that.
[00:46:00 - 00:46:03] Let's do one without too much writing.
[00:46:03 - 00:46:09] Oh, that's just the digital filter one.
[00:46:09 - 00:46:10] Okay.
[00:46:10 - 00:46:21] So in question one, we had a finite impulse response filter.
[00:46:21 - 00:46:31] So H of B and finite, so I've got two values here with got our filter output depends not just on inputs.
[00:46:31 - 00:46:33] X of n, X of n minus one.
[00:46:33 - 00:46:36] This is also on outputs.
[00:46:36 - 00:46:39] So this is going to be infinite impulse response filter.
[00:46:39 - 00:46:43] Okay.
[00:46:43 - 00:46:46] So to determine the transfer function, we need to take the Z transform.
[00:46:46 - 00:46:52] So then Y of n goes to Y of z.
[00:46:52 - 00:46:58] X of n goes to X of z.
[00:46:58 - 00:47:04] X of n minus one goes to X of z times Z to the minus one.
[00:47:04 - 00:47:14] And then we have plus 0.5 times Y of z times Z to the minus one.
[00:47:14 - 00:47:18] Okay.
[00:47:18 - 00:47:21] So we want to do some just algebraic rearranging sort of thing.
[00:47:21 - 00:47:40] I'll left hand side and why is z one minus 0.5 z to the minus one is equal to X of z times one minus z to the minus one.
[00:47:40 - 00:47:41] Okay.
[00:47:41 - 00:47:47] So that output H of z is equal to why is z over X of z.
[00:47:47 - 00:47:53] So this is 1 minus z to the minus one.
[00:47:53 - 00:47:57] Now it's wrong around.
[00:47:57 - 00:47:59] Why is it unis right?
[00:47:59 - 00:48:06] One minus z to the minus one over 1 minus 0.5 z to the minus one.
[00:48:06 - 00:48:11] Okay.
[00:48:11 - 00:48:12] That's just a little algebra.
[00:48:12 - 00:48:13] That should be straightforward.
[00:48:13 - 00:48:15] What's the order of this filter?
[00:48:15 - 00:48:19] First.
[00:48:19 - 00:48:20] Yep.
[00:48:20 - 00:48:36] So in general, the order is the max of the numerator or the denominator of both one.
[00:48:36 - 00:48:46] So it equals one.
[00:48:46 - 00:48:47] Okay.
[00:48:47 - 00:49:01] Determine the gain of the filter at half the sampling frequency where we've done.
[00:49:01 - 00:49:19] So we have the definition of the z transform is that z is equal to e to the j omega capital T.
[00:49:19 - 00:49:21] Is there something period?
[00:49:21 - 00:49:25] Omega is equal to 2 pi times frequency.
[00:49:25 - 00:49:40] So then z is equal to e j 2 pi f capital T, the sampling period.
[00:49:40 - 00:49:45] So we want to get the gain of the filter at half the sampling frequency.
[00:49:45 - 00:49:57] So that means we're looking at the case where f is equal to f is on 2.
[00:49:57 - 00:49:58] Okay.
[00:49:58 - 00:50:12] So we then have z is equal to, so we're substituting into f here, if s on 2, e to the j 2 pi f is on 2 times T.
[00:50:12 - 00:50:17] What's that equal to?
[00:50:17 - 00:50:24] Pi j.
[00:50:24 - 00:50:25] Yep.
[00:50:25 - 00:50:26] What's e to the pi j?
[00:50:37 - 00:50:38] Yeah, minus one.
[00:50:38 - 00:50:39] And there's a total.
[00:50:39 - 00:50:41] I'll just try and draw a thing here.
[00:50:41 - 00:50:42] So this is real.
[00:50:42 - 00:50:44] This is imaginary.
[00:50:44 - 00:50:48] You take the angle from here to here, theta, supply.
[00:50:48 - 00:50:51] As you're going 180 degrees, you're going around.
[00:50:51 - 00:50:52] So it's minus one.
[00:50:52 - 00:50:54] So just to go back to step.
[00:50:54 - 00:50:59] The two cancels, the two and the immator cancels with the two on the denominator.
[00:50:59 - 00:51:04] And then the sampling frequency is one over the sampling period.
[00:51:04 - 00:51:07] So if s times T disappears to be one.
[00:51:07 - 00:51:13] So that now, z has a value of minus one at something frequency on 2.
[00:51:13 - 00:51:34] So then to get the gain to h of f is on 2 is equal to then 1 minus 1 over 1 minus
[00:51:34 - 00:51:39] minus 1 minus 1 minus 1.
[00:51:39 - 00:51:44] Which is equal to 2 over 1.5.
[00:51:44 - 00:51:51] Which is equal to 1.33.
[00:51:51 - 00:51:53] So we go back halfway through the test.
[00:51:53 - 00:51:55] I'll give it a break there.
[00:51:55 - 00:51:58] So just a reminder that I've got this help session.
[00:51:58 - 00:51:59] I don't know if you're too real.
[00:51:59 - 00:52:00] So help session.
[00:52:00 - 00:52:03] And next Friday, nine o'clock.
[00:52:03 - 00:52:06] So go through some of the previous tests.
[00:52:06 - 00:52:09] Same, we can hear houses.
[00:52:09 - 00:52:12] And, yeah.
[00:52:12 - 00:52:13] Go to.
[00:52:13 - 00:52:15] So, okay.
[00:52:15 - 00:52:16] The walls are coming.
[00:52:16 - 00:52:19] So we'll stop there for today.
[00:52:19 - 00:52:27] Yes, yeah.
[00:52:27 - 00:52:29] You know, I find that a bit off-roading actually.
[00:52:29 - 00:52:39] So as I have run this test, some of my tests will be crisp.
[00:52:39 - 00:52:40] Yeah, yeah.
[00:52:40 - 00:52:44] So I think it's 50 max from me and 30 max from the crisp.
[00:52:44 - 00:52:48] So, certainly more as mine than heads.
[00:52:48 - 00:52:54] And the whole thing's an airman.
[00:52:54 - 00:52:56] I'm not sure.
[00:52:56 - 00:52:58] He's a weird.
[00:52:58 - 00:52:59] He's a weird.
[00:52:59 - 00:53:12] That's all I'll say.
[00:53:12 - 00:53:15] It is.
[00:53:15 - 00:53:16] Nice.

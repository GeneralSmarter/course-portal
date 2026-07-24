# ENEL372-26S2 Lecture 4 fast-pass local ASR transcript

Date: July 20, 2026 4:00pm-4:55pm
Transcript type: Hermes fast-pass local ASR from validated Echo audio, not a native Echo transcript.
Backend/model: faster-whisper tiny.en, CPU int8, beam_size=1, vad_filter=True.
Quality note: fast catch-up transcript. Technical terms, equations, names and Māori words need checking against slides/audio before assessment use.
Source audio SHA-256: `b77631d06619cbd60683ff1032e7c9224efcdb7a965ab2c80c0c9b3d975ac839`
Generated: 2026-07-24T23:51:14.276217+12:00

[00:00:00.000 - 00:00:04.000] The solar cow project.
[00:00:04.000 - 00:00:09.000] It's a project that we've been running for a few years now.
[00:00:09.000 - 00:00:12.000] I guess there's some historical information there.
[00:00:12.000 - 00:00:15.000] You may have heard some rumors at times.
[00:00:15.000 - 00:00:19.000] It's the feedback that we get here on year is that it's actually a really enjoyable project.
[00:00:19.000 - 00:00:22.000] It's very, very doable.
[00:00:22.000 - 00:00:27.000] So long, it's doable, so long as you chip away at it
[00:00:27.000 - 00:00:30.000] and don't leave it for the last just a few minutes.
[00:00:30.000 - 00:00:33.000] So there's a seat over here and just...
[00:00:33.000 - 00:00:40.450] All right, but the project is such.
[00:00:40.450 - 00:00:41.450] OK.
[00:00:41.450 - 00:00:44.450] It comprises of a model solar car.
[00:00:44.450 - 00:00:47.450] There it is.
[00:00:47.450 - 00:00:52.450] We've got a solar panel mounted on a toy car chassis.
[00:00:52.450 - 00:00:53.450] All right.
[00:00:53.450 - 00:01:00.450] Also mounted on here, we have DC motor with a gearbox that links to the rear drive on the vehicle.
[00:01:00.450 - 00:01:03.450] There's also an RC module.
[00:01:03.450 - 00:01:14.730] So we have RC control over this steering.
[00:01:14.730 - 00:01:22.730] The servo and the radio control module for the steering are the only things that allowed an external supply.
[00:01:22.730 - 00:01:29.730] So there will be a battery that's on here, but the battery is just for those purposes.
[00:01:29.730 - 00:01:32.730] So what happens or what is the project about?
[00:01:32.730 - 00:01:42.730] You guys need to design and build a buck converter that has closed loop feedback control to make that car.
[00:01:42.730 - 00:01:46.730] Go as fast as possible on a straight line race.
[00:01:46.730 - 00:01:51.730] It's a drag race that we're having your design for.
[00:01:51.730 - 00:01:57.730] So this is essentially the sort of thing that you're looking at design.
[00:01:57.730 - 00:02:00.730] So this is a buck converter.
[00:02:00.730 - 00:02:05.730] Almost exactly the type that you will be implementing in your design.
[00:02:05.730 - 00:02:14.730] This one was designed and built up by the research engineer that's in charge of the power electronics lab.
[00:02:14.730 - 00:02:19.730] It's all you'll get to meet him and engage with him quite a lot with this project.
[00:02:19.730 - 00:02:21.730] He's an awesome resource to have.
[00:02:21.730 - 00:02:24.140] Right.
[00:02:24.140 - 00:02:27.120] OK.
[00:02:27.120 - 00:02:32.120] The car race itself, it's supposed to be a bit of fun on the end.
[00:02:32.120 - 00:02:38.120] And S such does not constitute any of the weighted assessment for the course.
[00:02:38.120 - 00:02:43.120] We do all of that in an lab environment so everything is controlled.
[00:02:43.120 - 00:02:48.120] And so everyone gets a fair shot at it.
[00:02:48.120 - 00:02:52.120] So project description you get to complete some introductory lab exercises.
[00:02:52.120 - 00:02:56.120] They start from next week, which you've all been time to have all done to.
[00:02:56.120 - 00:03:02.120] They do not require you to have chosen your groups, although you will know them by that stage.
[00:03:02.120 - 00:03:08.120] The lab exercises are intended for you to be able to go through effectively on your own.
[00:03:08.120 - 00:03:13.120] Your carryout investigation to determine some of the solar panel and DC motor characteristics.
[00:03:13.120 - 00:03:17.120] I will give you a quick rundown of what those should kind of look like.
[00:03:17.120 - 00:03:20.120] So that you're not completely in the dark there.
[00:03:20.120 - 00:03:25.120] And then because of that you'll be able to design a suitable design strategy for your buck converter.
[00:03:25.120 - 00:03:33.120] And you'll then design it, design the buck converter, do some simple simulation work.
[00:03:33.120 - 00:03:35.120] It's simple.
[00:03:35.120 - 00:03:39.120] It's not a be all in the end or as far as the overall design is concerned.
[00:03:39.120 - 00:03:44.120] You unlikely to implement closed loop feedback control on the simulation.
[00:03:44.120 - 00:03:46.120] And it's using a simulation tool.
[00:03:46.120 - 00:03:50.120] Most of you wouldn't have used before, which is LT spice.
[00:03:50.120 - 00:03:59.120] And that side of it will be spearheaded and supervised by Chris Han, the other lecturer in the course.
[00:03:59.120 - 00:04:07.120] So you will simulate that then build the buck converter to interface between solar panel and the motor.
[00:04:07.120 - 00:04:14.120] Initially, just to get things going and play around with different component values if you want troubleshooting.
[00:04:14.120 - 00:04:17.120] You can put your circuit on breadboard.
[00:04:17.120 - 00:04:27.120] But if you're actually going to go in the race at the end of the year, then you'll need to convert that onto Bero board.
[00:04:27.120 - 00:04:34.410] Or even potentially PCB.
[00:04:34.410 - 00:04:40.410] Bero board, it's that stuff that you can see here.
[00:04:40.410 - 00:04:54.650] Bero board, it's the stuff that has pre-educated holes at the right pitch for through hole and copper strip, which you then cut to make your in-sold
[00:04:54.650 - 00:05:01.650] or on-shore and cut to make your circuit.
[00:05:01.650 - 00:05:04.650] So in power, the simis use sunlight falls on the panel.
[00:05:04.650 - 00:05:11.090] And the race is a straight line if around about 10 meters, maybe slightly more.
[00:05:11.090 - 00:05:15.090] There's a lot of... I know it doesn't sound much much, but it is a lot of fun.
[00:05:15.090 - 00:05:18.090] Especially when people can't drive the vehicle straight.
[00:05:18.090 - 00:05:21.430] Design constraints and requirements.
[00:05:21.430 - 00:05:29.430] Okay. Any design that you're asked to do as engineers or be involved with will have constraints and requirements.
[00:05:29.430 - 00:05:33.430] So this is to get you used to that sort of concept.
[00:05:33.430 - 00:05:36.430] You have to use a button to do that.
[00:05:36.430 - 00:05:42.430] That utilizes closed loop feedback control for full marks and the course.
[00:05:42.430 - 00:05:48.430] And a push you can get things operating in what's nice open loop.
[00:05:48.430 - 00:05:51.430] So you don't employ closed loop control.
[00:05:51.430 - 00:05:54.430] But that is not the purpose of the assignment.
[00:05:54.430 - 00:05:57.430] It's supposed to be under closed loop feedback control.
[00:05:57.430 - 00:06:01.430] And the current role chip that is used is a specific one.
[00:06:01.430 - 00:06:03.430] It's a TL4.9.4.
[00:06:03.430 - 00:06:08.430] It's dedicated purposes to take in a control signal and output.
[00:06:08.430 - 00:06:13.430] A positive modulated circuit that is duty ratio adjusted.
[00:06:13.430 - 00:06:19.430] You'll be using a power MOSFET for the controllable switch of your buck controller.
[00:06:19.430 - 00:06:21.430] A buck converter.
[00:06:21.430 - 00:06:24.430] We've got the part number there. It's available now at electronic store.
[00:06:24.430 - 00:06:28.430] And you have to use that gate for that power MOSFET.
[00:06:28.430 - 00:06:30.430] It must be driven with a CMOS inverter.
[00:06:30.430 - 00:06:35.430] And a CMOS inverter can structure from these two components.
[00:06:35.430 - 00:06:37.430] A CMOSFET and a CMOSFET.
[00:06:37.430 - 00:06:40.430] Okay. Those are both in the electronic store as well.
[00:06:40.430 - 00:06:44.430] Those of you that have got long memories.
[00:06:44.430 - 00:06:48.430] You can think back to E&L 270 last year.
[00:06:48.430 - 00:06:49.430] You might recall.
[00:06:49.430 - 00:06:55.430] Just mind that I was doing that material around CMOSFET.
[00:06:55.430 - 00:06:57.430] Oh, here's an inverter.
[00:06:57.430 - 00:07:00.430] And it would be really good for driving the gate of the power MOSFET.
[00:07:00.430 - 00:07:07.430] Because it has the right characteristics to achieve that switching a really rapid manner.
[00:07:07.430 - 00:07:09.430] Right.
[00:07:09.430 - 00:07:15.430] This diode that is your freewheeling diode in the buck converter that one should be used.
[00:07:15.430 - 00:07:18.430] The inductor core is type REM8.
[00:07:18.430 - 00:07:23.430] And we will provide you with the core.
[00:07:23.430 - 00:07:26.430] You have to design the and wind the inductor yourselves.
[00:07:26.430 - 00:07:31.430] Now I give all of the theory that you need for the design purposes.
[00:07:31.430 - 00:07:37.430] And even the process that you go through to figure out what you need for your power inductor.
[00:07:37.430 - 00:07:39.430] And that's that component.
[00:07:39.430 - 00:07:41.430] The contrast is not great.
[00:07:41.430 - 00:07:43.430] But that's that component right there.
[00:07:43.430 - 00:07:46.430] It's an REM8 core made out of a ferrite material.
[00:07:46.430 - 00:07:48.430] And here's the windings of the inductor.
[00:07:48.430 - 00:07:58.660] Maximum total capacitance for the circuit that you can add is 350 microfarads.
[00:07:58.660 - 00:08:04.660] So that's mostly taken up by these honking great electrolytic capacitors here.
[00:08:04.660 - 00:08:08.660] And that all has to do with the type of current and voltage ripple,
[00:08:08.660 - 00:08:14.660] especially voltage ripple that your design to have it, the input and the output of your buck converter.
[00:08:14.660 - 00:08:22.510] So the project support is going to be quite a bit for you if you usually decide to utilize it.
[00:08:22.510 - 00:08:26.510] So Edsel is a guy that I just mentioned before designed this.
[00:08:26.510 - 00:08:32.510] And there's also the person who will be in the lab a lot.
[00:08:32.510 - 00:08:35.510] And there's also a sub-procres hand.
[00:08:35.510 - 00:08:41.510] So the other lecturer of the course, Ed like I said, he's looking after the LT spice simulation work that you do.
[00:08:41.510 - 00:08:44.510] We've got some teaching assistants as well.
[00:08:44.510 - 00:08:51.510] And they'll be available in the electrical machines lab at the times that we've stated for the tutorial for this course.
[00:08:51.510 - 00:08:59.510] The tutorials, timetable for you in this course are just drop in help sessions for you guys for the project.
[00:08:59.510 - 00:09:05.510] There's no formal questions and problems that you sit down and do the sort of calculations.
[00:09:05.510 - 00:09:09.510] This is practical project work, tutorial help.
[00:09:09.510 - 00:09:14.510] And those don't start until the fifth of August.
[00:09:14.510 - 00:09:20.510] So I believe I've heard that there are, that's in your timetable, that these tutorials start this week.
[00:09:20.510 - 00:09:23.510] They don't start this week.
[00:09:23.510 - 00:09:26.510] We've had a heck up with the fine-tabling there.
[00:09:26.510 - 00:09:29.510] They start technically on the fifth.
[00:09:29.510 - 00:09:34.510] We say the 12th here because on the fifth, it's actually our component hand over day.
[00:09:34.510 - 00:09:38.510] So you come along to the tutorial, five to six on the Wednesday.
[00:09:38.510 - 00:09:45.510] And we give you all the components that you can't really get from the electronics store for the project.
[00:09:45.510 - 00:09:49.510] So that's your inductor core, the TL 494 controller chip.
[00:09:49.510 - 00:09:50.510] Yep.
[00:09:50.510 - 00:09:53.510] So we give you that at that time.
[00:09:53.510 - 00:09:56.510] And you might have a few questions that you want to ask us even then.
[00:09:56.510 - 00:10:12.660] So the labs, three lab exercises, just help you get an idea of how a buck converter kind of works in practice.
[00:10:12.660 - 00:10:15.660] It also looks at PWM and the effect of PWM.
[00:10:15.660 - 00:10:23.660] So good idea to do those labs to give you some sort of an idea of how to move forward.
[00:10:23.660 - 00:10:28.660] Those labs are in essence voluntary.
[00:10:28.660 - 00:10:31.660] So, cool.
[00:10:31.660 - 00:10:33.660] Are you interesting?
[00:10:33.660 - 00:10:41.660] You might have just grab a seat on the side of the benches up there.
[00:10:41.660 - 00:10:42.660] Oh, yeah.
[00:10:42.660 - 00:10:47.790] Yep.
[00:10:47.790 - 00:10:48.790] Yeah.
[00:10:48.790 - 00:10:49.790] Just sit in the corner.
[00:10:49.790 - 00:10:55.910] Right.
[00:10:55.910 - 00:10:56.910] Yeah.
[00:10:56.910 - 00:11:00.910] So there is no assessment waiting on you having attended those labs.
[00:11:00.910 - 00:11:03.910] We don't take any kind of sheets to mark or anything like that.
[00:11:03.910 - 00:11:07.910] This is solely for your benefit moving forward.
[00:11:07.910 - 00:11:17.910] And they don't, they're not linked, like I said, with necessarily being in your project group doing those labs.
[00:11:17.910 - 00:11:20.910] Drop in sessions as I've just mentioned.
[00:11:20.910 - 00:11:22.910] Wednesday is spider six in the machines lab.
[00:11:22.910 - 00:11:24.910] It says problem the 12th of the 8th.
[00:11:24.910 - 00:11:29.910] So fifth components hand out the very next week as when they start an honest.
[00:11:29.910 - 00:11:35.910] There's going to be an extra tutorial held on the 14th of August.
[00:11:35.910 - 00:11:38.910] That's a Friday in 8th.
[00:11:38.910 - 00:11:42.910] And that's just to give you the Chris Han will run that.
[00:11:42.910 - 00:11:44.910] It's a chance for you to come along.
[00:11:44.910 - 00:11:48.910] And so look, we've been having trouble with this and this on LT spice.
[00:11:48.910 - 00:11:50.910] How do you get that?
[00:11:50.910 - 00:11:51.910] How do you sort that out?
[00:11:51.910 - 00:11:56.910] So I'm sure a number will have that'll be quite common between groups.
[00:11:56.910 - 00:12:08.330] The components, so that's the semiconductors inductor called breadboard to do your prototyping on.
[00:12:08.330 - 00:12:15.330] That's issued by Edsel, myself and the TAs on that fifth, Wednesday the fifth of August.
[00:12:15.330 - 00:12:19.330] And the other components, the resistors that you'll decide that you need some of the electric
[00:12:19.330 - 00:12:24.330] and electric capacitors and so forth, they'll all be available in the electronics store.
[00:12:24.330 - 00:12:27.330] So that's just down the corridor and the wing.
[00:12:27.330 - 00:12:34.330] It's got the big kind of fishbowl looking front part with it with the technician and charge of the store is.
[00:12:34.330 - 00:12:42.020] But you can just go into the store and get your components that you need and sign off on the sheet.
[00:12:42.020 - 00:12:50.020] The tools, cell reins and so forth will all be available in the machine's lab for you to use on the project.
[00:12:50.020 - 00:12:54.020] The benches, they've got power supplies and telescopes.
[00:12:54.020 - 00:13:01.020] And they'll also have indoor light sources for your solar panel.
[00:13:01.020 - 00:13:15.020] So we've got solar panels, underneath LED light sources that you can use for sort of regular and repeatable light intensity on your solar panels that you can then do your testing with.
[00:13:15.020 - 00:13:25.990] We'll also have the power electronics lab available for you to use during the semester break if you want to come in and do some extra work then.
[00:13:25.990 - 00:13:33.990] Okay, and the test rigs, as I just mentioned, they'll be available in the machine's lab for you to work on and do your testing with.
[00:13:33.990 - 00:13:45.330] So all of the practical work effectively, the assignment is done in a group of three.
[00:13:45.330 - 00:13:58.450] Yes. Well, those you can fire off to me for the material that I cover and for Chris Hahn, you can fire it off to him.
[00:13:58.450 - 00:14:04.450] So I do make that material available. I put in problems and then the following week fully work solutions.
[00:14:04.450 - 00:14:14.920] Yes. I don't. I don't. So what you need to do, you can drop by and see if I'm there and I might be able to spend time with you.
[00:14:14.920 - 00:14:21.920] Or you can just email me and we'll make a specific time or absolutely guarantee that it'll make some time for you.
[00:14:21.920 - 00:14:36.860] Alright, groups of three. So by the end of this week, you need to figure out a group to be in, group of three.
[00:14:36.860 - 00:14:48.860] You can just email me as it says by the end of this week if you can't find a group to be a member of and tell me, I'll take, I'll record that and I'll allocate you to a group.
[00:14:48.860 - 00:14:56.860] Okay. But they're all self selected. On learn, there is a group self selection activity that's already open. So you go in.
[00:14:56.860 - 00:15:05.860] You can, you may select a group of just two and a third slot will be for me to allocate someone to.
[00:15:05.860 - 00:15:11.860] You can't just put one name in. Do not enter a group, just one name.
[00:15:11.860 - 00:15:18.860] Or be annoyed. And I will simply take you out of that group and allocate you to another one.
[00:15:18.860 - 00:15:29.860] Alright, with three people. Okay, so no groups of one please. Two, yes. But, and then I'll allocate, allocate a third person but no, no groups of one.
[00:15:29.860 - 00:15:39.860] There is a caveat to that with the groups of two. I need to be able to construct four groups of three as much as possible for the course.
[00:15:39.860 - 00:15:46.860] So if I get too many groups of two being entered and not enough individuals say, hey, I haven't got a group that I can go into.
[00:15:46.860 - 00:15:54.860] I'm going to have to break up some of those groups of two that have been entered into. Then enter on learn. Sorry, it's just the way it has to go.
[00:15:54.860 - 00:16:04.480] It won't be too many but it could be a couple of the groups that do that. So try to get a full group of three together.
[00:16:04.480 - 00:16:11.480] Alright, so as I just said, once they fit the vlogist, we'll get the components to you. That's at the tutorial time and machine slip.
[00:16:11.480 - 00:16:19.480] This Friday, 21st August, that is when your first piece of assessment is submitted.
[00:16:19.480 - 00:16:28.480] Alright, so that's five percent waiting and that's your simulation work showing that you've got some idea of what's kept with your back converter.
[00:16:28.480 - 00:16:40.390] Certainly doesn't mean that you've got it dialed in as to exactly what inductive size that you should have number of turns and so forth.
[00:16:40.390 - 00:16:54.430] But it shows that you do have an idea of the way the TL4 94 will have a PWM output and then your CMOS inverter and driving a back converter.
[00:16:54.430 - 00:17:11.430] If you are going to go to the effort or put it together a PCV, there's a deadline for getting that into it's all the artwork so that we've got time to actually get it physically built up well in advance of the laboratory inspection time.
[00:17:11.430 - 00:17:23.700] Alright, so we, you know, if you want a PCV, that's by all means submit one and we'll get one manufactured for you.
[00:17:23.700 - 00:17:29.700] So again, the next piece of assessment, so it says Wednesday Thursday Friday 23rd of September, group project inspection.
[00:17:29.700 - 00:17:34.700] So yes, we're going to have you have three full days which you have to allocate to an inspection.
[00:17:34.700 - 00:17:37.700] 15 minutes.
[00:17:37.700 - 00:17:42.700] So it'll be a bookable time sheet that's put up and hard copy.
[00:17:42.700 - 00:17:52.700] So you're going to have to go physically, one of your group members physically go to the table of bookable times and right in a time that you want to be able to get a job.
[00:17:52.700 - 00:17:55.700] That's what you want to do your lab inspection.
[00:17:55.700 - 00:17:59.700] Right, so it's over those three days though.
[00:17:59.700 - 00:18:02.700] So that's just that's why it's those three days.
[00:18:02.700 - 00:18:06.700] More details to follow in that's getting closer to time.
[00:18:06.700 - 00:18:10.700] Monday the 12th October you then submit your group design report.
[00:18:10.700 - 00:18:13.700] So that's 15% for that.
[00:18:13.700 - 00:18:15.700] Okay, it's one report for the group of three.
[00:18:15.700 - 00:18:18.700] So you all work on it together and submit it as one.
[00:18:18.700 - 00:18:26.700] And then the following day we do a self-impere assessment which scales 30% of the project mark.
[00:18:29.200 - 00:18:32.200] There's the timing for the introductory lab exercises.
[00:18:32.200 - 00:18:38.830] Don't delay in getting started.
[00:18:38.830 - 00:18:45.830] It says immediately following component issue date, you should start working on the second hardware design and implementation.
[00:18:45.830 - 00:18:50.830] You could actually be doing some of the design beforehand.
[00:18:50.830 - 00:19:04.480] Because I will have given you by that time all of the theory you need to start to get your buck converter configuration together.
[00:19:04.480 - 00:19:11.480] And the design process to go through to design an inductor for your buck converter.
[00:19:11.480 - 00:19:18.480] Right, so you should at least be going through the calculations to make sure that you've got those all in place that you can tweak a bit if you need to.
[00:19:18.480 - 00:19:23.480] But it's all ready to go once you've got your components.
[00:19:23.480 - 00:19:27.480] You should be doing that work concurrently with the simulation development.
[00:19:27.480 - 00:19:34.480] Please don't just, you know, you've got your submission of the simulation coming up.
[00:19:34.480 - 00:19:39.480] So you just focus on your simulating you and then on that submission date.
[00:19:39.480 - 00:19:43.480] You submit that and then you start on your hardware.
[00:19:43.480 - 00:19:55.580] It's going to be crunching up the time that you have available, especially for troubleshooting and getting that circuit on your Vero board.
[00:19:55.580 - 00:20:02.580] I might say, oh, well, I don't really, I'm not keen on going for the race at the end of the year.
[00:20:02.580 - 00:20:07.580] I'll just keep it on breadboard and we'll do our project inspection with the circuit on breadboard.
[00:20:07.580 - 00:20:11.580] Don't do that. Please don't do that.
[00:20:11.580 - 00:20:19.090] Oh, breadboards are somewhat unreliable at best.
[00:20:19.090 - 00:20:29.090] And you've got to have a reasonably sophisticated circuit to demonstrate at the inspection.
[00:20:29.090 - 00:20:32.090] And I've had it before.
[00:20:32.090 - 00:20:40.590] Your group comes along and they've got this, we call it a birth nest of wires.
[00:20:40.590 - 00:20:46.590] And that's their buck converter and they've gone down and they put in the solar panel and they attach the motor.
[00:20:46.590 - 00:20:52.590] And someone goes like that with your elbow across it and it doesn't work.
[00:20:52.590 - 00:20:54.590] It was working.
[00:20:54.590 - 00:21:02.590] Okay, so I need to be able to inspect and look at a functioning circuit to determine how well you've done your design.
[00:21:02.590 - 00:21:15.590] So please, please, please try to make sure that you do things early, get the time to put your circuit on a breadboard, on a Vero board, at the very least.
[00:21:15.590 - 00:21:28.630] Those of you that get into it and do a PCB, you're going to have the best shot of everything just going absolutely smoothly in the inspection.
[00:21:28.630 - 00:21:35.630] So I've got here kind of a, there will be a specific marking rubric that's made available to you.
[00:21:35.630 - 00:21:43.630] But the sort of things that I'll be asking you during the lab inspection is written here.
[00:21:43.630 - 00:21:49.630] All members of the same group who attend and participate will receive the same project inspection mark.
[00:21:49.630 - 00:21:58.630] So I'll be asking everyone that's there, separate questions, looking at your answers and that's a group you will get a mark for that their inspection.
[00:21:58.630 - 00:22:02.630] Which means that it's compulsory to attend.
[00:22:02.630 - 00:22:09.630] Right, so all the normal sort of considerations are in place for missing an assessment.
[00:22:09.630 - 00:22:17.630] So special considerations apply, but you'll need to have evidence of a reason why you're not at the lab inspection if you're not there.
[00:22:17.630 - 00:22:21.630] If you're not there, you don't, no reason you don't get a mark.
[00:22:21.630 - 00:22:29.390] You can't rely on your group members to pull you through if you don't show up.
[00:22:29.390 - 00:22:36.390] Yeah, you need to provide a loop on your board that enables us to couple in our current probe.
[00:22:36.390 - 00:22:41.390] So it's actually quite a sizeable loop that you kind of need to put in.
[00:22:41.390 - 00:22:48.390] That one centimeter by two centimeters, it allows us to clip on a probe that we need to look at the inductor current.
[00:22:48.390 - 00:22:53.020] It's important that we see the inductor current.
[00:22:53.020 - 00:22:59.020] All right, so those are the things that I'll be expecting to look at and ask about this the while loop.
[00:22:59.020 - 00:23:03.020] The report is a group report.
[00:23:03.020 - 00:23:08.020] So you need to include all the aspects of your design operation, overall performance.
[00:23:08.020 - 00:23:10.020] There are five years of the penalty stuff.
[00:23:10.020 - 00:23:13.020] They're like almost never get anyone with a late report.
[00:23:13.020 - 00:23:19.020] The only thing that can sometimes be a hiccup is if there's something going on with learn and there's a delay.
[00:23:19.020 - 00:23:24.020] But even then, it's only like a second look or a 30 seconds or so.
[00:23:24.020 - 00:23:28.020] Don't be late.
[00:23:28.020 - 00:23:30.020] No point in losing those marks.
[00:23:30.020 - 00:23:34.910] Use the bay eye.
[00:23:34.910 - 00:23:37.910] So they're very specific.
[00:23:37.910 - 00:23:41.910] Guidelines, identified here, leaves. There's no restriction.
[00:23:41.910 - 00:23:44.910] It's just kind of a tough note used to here anyway.
[00:23:44.910 - 00:23:49.910] LT, spice, assignment, project inspection and project report.
[00:23:49.910 - 00:23:54.910] There are limited use of AI that you can have inside unified here.
[00:23:54.910 - 00:23:59.910] So for this assignment, you're permitted to use AI for the purpose of design concept.
[00:23:59.910 - 00:24:05.910] Suggestions, concept suggestions, proofreading and editing the document.
[00:24:05.910 - 00:24:07.910] And for summarizing knowledge.
[00:24:07.910 - 00:24:10.910] You can't get it to write the thing for you.
[00:24:10.910 - 00:24:17.910] In the project inspection, you're permitted to use AI for the purpose of design and build concept suggestions.
[00:24:17.910 - 00:24:20.910] To help with progress in the construction and testing.
[00:24:20.910 - 00:24:22.910] No other use is allowed.
[00:24:22.910 - 00:24:27.910] And it's not permitted to be used actually during the project inspection activity itself.
[00:24:27.910 - 00:24:33.290] So you can't pull it up and sort of query it.
[00:24:33.290 - 00:24:37.370] Let's see answer to that question.
[00:24:37.370 - 00:24:43.370] And for the report, you're permitted to use AI for the purpose of proofreading and editing the document.
[00:24:43.370 - 00:24:49.370] And for summarizing knowledge, no other use outside of what you've already used it for for the previous assessments.
[00:24:49.370 - 00:24:59.380] Right. So since we're giving you this provision and expect you to use AI,
[00:24:59.380 - 00:25:01.380] it's that's fine.
[00:25:01.380 - 00:25:06.380] But we need you to tell us what you have used for prompts.
[00:25:06.380 - 00:25:08.380] So we need a whole list.
[00:25:08.380 - 00:25:11.380] Everything that you've prompted the AI tool for.
[00:25:11.380 - 00:25:15.380] And then sign off to say that that's all you have used.
[00:25:16.380 - 00:25:21.380] Right. So we do need that has to be submitted and signed.
[00:25:21.380 - 00:25:29.350] And it's shown that this is this is your work.
[00:25:29.350 - 00:25:34.350] So for peer review each group member will give each of the team members including themselves.
[00:25:34.350 - 00:25:38.350] A number of times that someone forgets to include a mark for themselves.
[00:25:38.350 - 00:25:41.350] What they how they think they've performed in the project.
[00:25:41.350 - 00:25:45.350] Mike out of 10, how they contributed to the overall group effort.
[00:25:45.350 - 00:25:49.350] You must justify your mark with comments.
[00:25:49.350 - 00:25:53.350] Pretty short just to give us an idea.
[00:25:53.350 - 00:25:59.350] And each group member will submit that on learn and it will be used to scale 30% of the group project mark.
[00:25:59.350 - 00:26:01.350] Right.
[00:26:01.350 - 00:26:10.350] Now this is not an opportunity for someone to for people to then complain about the performance of someone in the group project.
[00:26:10.350 - 00:26:13.350] So I give them 0.5 out of 10.
[00:26:13.350 - 00:26:20.350] And because by that stage you must if there's something going on with the group dynamic,
[00:26:20.350 - 00:26:24.350] someone's not contributing or there's an issue going on.
[00:26:24.350 - 00:26:30.350] I need to know about it so that we have the opportunity to put things straight.
[00:26:30.350 - 00:26:31.350] Right.
[00:26:31.350 - 00:26:33.350] Life is complicated.
[00:26:33.350 - 00:26:38.350] There could be all sorts of reasons why someone seems to be not engaging.
[00:26:38.350 - 00:26:43.350] Outside of being just not wanting to do the project.
[00:26:43.350 - 00:26:51.350] You don't have the option of disengaging because you don't want to do the project.
[00:26:51.350 - 00:26:53.350] That's not equitable.
[00:26:53.350 - 00:26:54.350] Right.
[00:26:54.350 - 00:27:05.350] There is an extra full expectation that you contribute at least from the scaling in this project 36 hours towards the project.
[00:27:05.350 - 00:27:09.300] That's quite a bit of time.
[00:27:09.300 - 00:27:10.300] Okay.
[00:27:10.300 - 00:27:16.300] We can't dictate what the quality of that help will be but you must make yourself available for it.
[00:27:16.300 - 00:27:18.300] Right.
[00:27:18.300 - 00:27:24.300] You don't get the choice to say I've got other more important coursework to do.
[00:27:24.300 - 00:27:26.300] You're part of a group project.
[00:27:26.300 - 00:27:30.300] You must contribute something like that which is reasonable.
[00:27:30.300 - 00:27:38.580] If something's going wrong, you're getting a project or you've got a group member that seems to be not communicating with you when you're getting a project.
[00:27:38.580 - 00:27:40.580] You're communicating with you when you're trying to communicate with them.
[00:27:40.580 - 00:27:42.580] You must respond to communications.
[00:27:42.580 - 00:27:45.580] Then I want to, I have to know about it.
[00:27:45.580 - 00:27:46.580] You don't get the option.
[00:27:46.580 - 00:27:47.580] You must tell me.
[00:27:47.580 - 00:27:54.580] And then I can arrange a meeting with the entire group and we can sort it out.
[00:27:54.580 - 00:28:01.580] And sorting it out means that that person who hasn't been contributing needs to kind of explain why and we'll start contributing.
[00:28:01.580 - 00:28:04.050] Right.
[00:28:04.050 - 00:28:05.050] Equitable.
[00:28:05.050 - 00:28:13.490] Look, I'm telling you this and it's like two, maybe three groups a year and there are 70 groups.
[00:28:13.490 - 00:28:14.490] All right.
[00:28:14.490 - 00:28:21.490] So it's only saying it's only one or two people that's a problem and there's usually a really good reason why someone's being not engaging.
[00:28:21.490 - 00:28:22.490] Right.
[00:28:22.490 - 00:28:24.490] So don't believe the worst of people.
[00:28:24.490 - 00:28:25.490] Right.
[00:28:25.490 - 00:28:26.490] Like I said, life is complicated.
[00:28:26.490 - 00:28:28.930] All right.
[00:28:28.930 - 00:28:34.930] But I need to know at least two weeks prior to the lab review or the lab inspection if something's going wrong.
[00:28:34.930 - 00:28:38.930] If I get it a couple of days or a week before, does that tell me?
[00:28:38.930 - 00:28:41.930] It means that you haven't been working on your project.
[00:28:41.930 - 00:28:45.930] And suddenly something's going wrong and someone's not contributing.
[00:28:45.930 - 00:28:47.930] That's not the way this project should work.
[00:28:47.930 - 00:28:56.270] You should be working on it regularly through the weeks so that you don't do it all in a panic right at the end.
[00:28:56.270 - 00:28:58.270] And that's what that stuff.
[00:28:58.270 - 00:29:00.270] Race day.
[00:29:00.270 - 00:29:02.270] It's in study week.
[00:29:02.270 - 00:29:05.270] Whether dependent clearly for solar power.
[00:29:05.270 - 00:29:09.270] Actually, we have an indoor fallback option.
[00:29:09.270 - 00:29:19.270] An E&L 300 project from last year did an awesome job at developing a software tool that interacts with the test unit.
[00:29:19.270 - 00:29:22.270] And we can run races inside.
[00:29:22.270 - 00:29:26.450] Okay.
[00:29:26.450 - 00:29:32.450] You get a completion prize for a car completes one of the hit race hits without assistance.
[00:29:32.450 - 00:29:36.450] You get a runner up certificate and a top place certificate.
[00:29:36.450 - 00:29:37.450] Cool.
[00:29:37.450 - 00:29:45.450] Before I want to spend some time now, I'm talking a little bit about the systems involved with the project.
[00:29:45.450 - 00:29:48.450] So again, you're not going into this completely blind.
[00:29:48.450 - 00:29:55.600] Right.
[00:29:55.600 - 00:29:57.600] Oh, you can all see that, can you?
[00:29:57.600 - 00:30:01.170] I'm just that drawing.
[00:30:01.170 - 00:30:03.700] All right.
[00:30:03.700 - 00:30:07.080] So it's all the car project.
[00:30:07.080 - 00:30:09.080] I'll go into right the stem.
[00:30:09.080 - 00:30:12.080] I will make all this on scan it and then I'll put it up on learn as well.
[00:30:12.080 - 00:30:18.080] See, that have to be too concerned about copying absolute everything down that I'm putting down.
[00:30:18.080 - 00:30:24.300] All right.
[00:30:24.300 - 00:30:28.300] So clearly what we've got here, we've got a solar panel.
[00:30:28.300 - 00:30:35.170] That feeds into your back converter.
[00:30:35.170 - 00:30:40.900] And then the back converter output feeds into a motor.
[00:30:40.900 - 00:30:46.900] It's a DC motor, a fresh DC motor, just looking for a DC input.
[00:30:46.900 - 00:30:57.990] So what do you think the main goal for the project is given what I've been describing?
[00:30:57.990 - 00:31:06.260] Are you going to win the race?
[00:31:06.260 - 00:31:09.260] Efficiency is certainly a part of it.
[00:31:09.260 - 00:31:14.260] If you can get your converter working efficiently, efficiently, then you're making the best use of that power that's available.
[00:31:14.260 - 00:31:18.900] There's something a little more fundamental than that.
[00:31:18.900 - 00:31:20.900] Sorry, I didn't get that for it.
[00:31:20.900 - 00:31:22.900] Hi, Motor Speed.
[00:31:22.900 - 00:31:25.900] So what makes the motor go?
[00:31:25.900 - 00:31:26.900] Current.
[00:31:26.900 - 00:31:27.900] Yep.
[00:31:27.900 - 00:31:29.900] And handed hand with that to the amount of voltage.
[00:31:29.900 - 00:31:30.900] So power.
[00:31:30.900 - 00:31:32.900] Power makes the motor go.
[00:31:32.900 - 00:31:39.300] The more power that you can feed into the motor, the faster it's going to go.
[00:31:39.300 - 00:31:43.300] So what does that mean on the solar panel?
[00:31:43.300 - 00:31:47.960] So what does that mean on the solar panel?
[00:31:47.960 - 00:31:51.960] So what does that mean on the solar panel?
[00:31:51.960 - 00:31:53.960] So what does that mean on the solar panel?
[00:31:53.960 - 00:31:56.960] So the power is going to be the same.
[00:31:56.960 - 00:32:02.960] So for the project and to achieve the goal of winning the race,
[00:32:02.960 - 00:32:06.960] yes, you want the converter to be efficient, but first and foremost,
[00:32:06.960 - 00:32:11.960] you want the solar panel to provide the providing maximum power at all times.
[00:32:11.960 - 00:32:25.580] And that's irrespective of what you think might be happening at the motor side.
[00:32:25.580 - 00:32:30.580] The motor, all we're considering about is feeding as much power into that motor as possible,
[00:32:30.580 - 00:32:35.580] given the sort of characteristics that the solar panel has.
[00:32:35.580 - 00:32:48.630] Solar panel needs to be at its maximum power point at all times for you to get the car to go as fast as possible.
[00:32:48.630 - 00:32:59.460] So maximum power at all times, maximum power point at all times.
[00:32:59.460 - 00:33:01.460] Hang on, what does that mean?
[00:33:01.460 - 00:33:16.220] Well, we look at the characteristics between the solar panel and the motor.
[00:33:16.220 - 00:33:21.220] Because they're quite different.
[00:33:21.220 - 00:33:29.220] Solar panel, we look at the IV curve, IV for a solar panel.
[00:33:29.220 - 00:33:34.220] So at no voltage, so you're loading it up, you're drawing current.
[00:33:34.220 - 00:33:37.220] It provides a certain amount of current.
[00:33:37.220 - 00:33:45.660] However, at a certain point, when you start dropping off the amount of current that you draw,
[00:33:45.660 - 00:33:50.660] the voltage also comes to a maximum.
[00:33:50.660 - 00:33:54.660] So there's only a certain, even if you've not got any load on the solar panel at all,
[00:33:54.660 - 00:33:59.660] under like conditions, it will only output output maximum voltage.
[00:33:59.660 - 00:34:05.660] It won't go hearing off to infinity or anything like that, or hundreds of volts.
[00:34:05.660 - 00:34:14.140] For our panel, that's something around 21 volts.
[00:34:14.140 - 00:34:24.030] That's for a particular light intensity at lower light intensity.
[00:34:24.030 - 00:34:32.850] It will be lower current, and then it opens circuit though.
[00:34:32.850 - 00:34:34.850] It gets to around about the same voltage.
[00:34:34.850 - 00:34:53.930] Right, but it provides, as you would expect, less incident light energy, less amount of current that the panel can provide you.
[00:34:53.930 - 00:34:59.930] There is quite a strong dependency on temperature as well.
[00:34:59.930 - 00:35:09.930] So for temperature, what happens is actually, if the temperature goes up, at low voltage in,
[00:35:09.930 - 00:35:16.930] so you're loading up your solar panel with quite an amount of load, the current is actually higher.
[00:35:16.930 - 00:35:21.930] You might think, oh, well, solar panels will work better at higher temperatures.
[00:35:21.930 - 00:35:35.450] Well, the problem is that its voltage droops much faster.
[00:35:35.450 - 00:35:56.870] Such that, if we look at the power versus voltage, we see a curve that does this.
[00:35:56.870 - 00:36:01.870] So by the time you get to 21 volts, there's zero power output.
[00:36:01.870 - 00:36:06.870] It peaks at the knee point of your IV coupe.
[00:36:06.870 - 00:36:15.870] So the product between voltage and current, its power, equals V i, it peaks at that knee point.
[00:36:15.870 - 00:36:26.870] And what happens is that knee point moves way back when you've got higher temperatures, and you find that the peak of your maximum power point reduces.
[00:36:26.870 - 00:36:37.870] So at high loads, you get a little bit more current that you do not get as much power out of your solar panels at higher temperatures.
[00:36:37.870 - 00:36:39.870] This is your maximum power point.
[00:36:39.870 - 00:36:56.900] And it tends to be under relatively fixed lighting conditions at a specific voltage.
[00:36:56.900 - 00:37:04.900] For our panel, it's going to be something around 17 volts, at the sort of light conditions that you might get outside.
[00:37:04.900 - 00:37:16.820] In late mid-October, not now, how it would be somewhat this.
[00:37:16.820 - 00:37:20.640] So what, this power?
[00:37:20.640 - 00:37:21.640] Right.
[00:37:21.640 - 00:37:25.640] So that's the solar panel main characteristics.
[00:37:25.640 - 00:37:30.640] For the motor, what we have is we've got a permanent magnet DC motor.
[00:37:30.640 - 00:37:36.640] So we have some permanent magnets that are on the stator, North-South.
[00:37:36.640 - 00:37:46.720] We have a rotor with a bunch of windings in the rotor, central axle.
[00:37:46.720 - 00:38:03.350] And we've got some brushes which connect to the output of the buck converter, V buck plus minus.
[00:38:03.350 - 00:38:10.730] And that means there's current flowing through, called armature current, i.a.
[00:38:10.730 - 00:38:21.730] And that will then set up conditions for magnetic fields, such that you cause rotation on the rotor with some torque T.
[00:38:21.730 - 00:38:28.730] So when it starts spinning up, you get what's known as back EMF being generated by Faraday's law.
[00:38:28.730 - 00:38:34.730] So you end up with opposes the voltage that's sitting up the current.
[00:38:34.730 - 00:38:41.730] So plus minus Ea, that's your back EMF for the DC motor.
[00:38:41.730 - 00:38:48.730] Some expressions, ea equals motor constant times omega.
[00:38:48.730 - 00:38:51.730] So omega is the rotational speed of your rotor.
[00:38:51.730 - 00:38:56.730] So that's the motor speeds up, the back EMF speeds up, gets larger.
[00:38:56.730 - 00:39:01.730] And then you've got torque is equal to k times i.a.
[00:39:01.730 - 00:39:08.680] So the torque in the motor is proportional to the amount of current that's flowing through it.
[00:39:08.680 - 00:39:24.510] Now, from standstill, our motor needs about one and a half to two, two, one and a half to two amps to just start ticking over.
[00:39:24.510 - 00:39:46.960] That's under the sort of load that you would expect here with a bit of weight on it.
[00:39:46.960 - 00:39:50.560] So providing some inertia.
[00:39:50.560 - 00:39:58.930] For running, so the motor is actually spinning a little bit faster now, creating a back EMF.
[00:39:58.930 - 00:40:02.930] You only need, oh, by the way, to start it at one and a half to two amps.
[00:40:02.930 - 00:40:10.930] You only need V back to be around two volts, not very much.
[00:40:10.930 - 00:40:17.930] You're starting off with about 17 volts, and you only need about two volts for the motor to start.
[00:40:17.930 - 00:40:32.340] So for running, you need less current, it's around about one amp, but at V back around six or seven volts.
[00:40:32.340 - 00:40:43.370] That's six or seven, not six point seven.
[00:40:43.370 - 00:40:46.370] All right, so they're quite different.
[00:40:46.370 - 00:40:48.370] Those characteristics.
[00:40:48.370 - 00:40:56.370] If you were to directly connect the solar panel to the motor, you wouldn't get very far.
[00:40:56.370 - 00:41:21.820] Because what you would have is if we look at IV characteristics for each of those, then the solar panel, it's like that.
[00:41:21.820 - 00:41:28.070] That's around about 200 milliamps, 21 volts.
[00:41:28.070 - 00:41:37.410] The requirement for the motor looks more like this.
[00:41:37.410 - 00:41:43.410] So this is around two amps, peak, to get it running.
[00:41:43.410 - 00:41:48.410] This is to get running.
[00:41:48.410 - 00:41:51.410] So that's your about two volts.
[00:41:51.410 - 00:41:58.820] Also, and here it is around about one amp once it's running.
[00:41:58.820 - 00:42:05.820] If you were to connect the two together, the intersect point between the two curves is where it would operate.
[00:42:05.820 - 00:42:15.510] So just connecting them together, here is your operating point, which is less than what it needs to start spinning.
[00:42:15.510 - 00:42:22.510] So your solar panel is nowhere near its maximum power point region, which is at that knee point.
[00:42:22.510 - 00:42:24.510] Never gets there.
[00:42:24.510 - 00:42:39.090] So the buck converter, what it is behaving like conceptually is like a DC transformer.
[00:42:39.090 - 00:42:58.550] Just by concept, it's not actually a transformer that needs AC.
[00:42:58.550 - 00:43:15.550] So by that, I mean that if you have high BN, which is what we have for the solar panel, and low IN, this will, the buck converter will convert that to what does it do?
[00:43:15.550 - 00:43:33.070] It sticks down. So it's low, the out. But since PN equals P out, then we'll have high I out.
[00:43:33.070 - 00:43:36.070] The current that we need to get the motor started.
[00:43:36.070 - 00:43:47.580] As that motor starts, and the current requirement comes down, we can change the duty ratio so that we end up with a higher output voltage at the lower, slightly lower current.
[00:43:47.580 - 00:43:53.580] So your buck converter, by changing the duty ratio, is able to carry up that function.
[00:43:53.580 - 00:43:59.040] It's effectively impedance matching.
[00:43:59.040 - 00:44:01.040] For the buck converter.
[00:44:01.040 - 00:44:09.340] Almost there. Just one last diagram.
[00:44:09.340 - 00:44:16.340] And that is to consider then what happens with the control that we need to employ.
[00:44:16.340 - 00:44:32.390] So we've got our panel. We're feeding that into our buck converter, and that goes to the motor.
[00:44:32.390 - 00:44:37.390] Most conventional systems will be controlling the power at the motor end.
[00:44:37.390 - 00:44:43.390] Because we want the load to be, which is the motor to be doing something that is controllable.
[00:44:43.390 - 00:44:51.670] The purpose of this project is to have the motor receive as much power at all times as possible.
[00:44:51.670 - 00:44:57.670] And the way we achieve that is that we control the solar panel.
[00:44:57.670 - 00:45:07.670] So we use the solar panel and measure its voltage to make sure it's being controlled to stay at the same voltage, which is at our maximum power point.
[00:45:07.670 - 00:45:25.660] So we measure the voltage, which is our peak power.
[00:45:25.660 - 00:45:38.220] And we compare that with the ordered.
[00:45:38.220 - 00:45:46.220] And that's what we are defining is if already determined by some calculation, what our maximum power point is.
[00:45:46.220 - 00:45:53.690] The maximum power point. There will be an error then, looking at those two.
[00:45:53.690 - 00:46:00.420] And that error feeds into PI controller unit.
[00:46:00.420 - 00:46:03.420] We'll go over this in class.
[00:46:03.420 - 00:46:09.420] And then the output of that controller goes to a PWM generator.
[00:46:09.420 - 00:46:12.420] That's where the duty ratio is defined.
[00:46:12.420 - 00:46:14.420] So adjusting duty ratio.
[00:46:14.420 - 00:46:18.420] And then we use that to control the buck converter.
[00:46:18.420 - 00:46:29.860] All of what I've just stated there inside here is what the TL494 does for us.
[00:46:29.860 - 00:46:37.750] We have to add some components short to get our weightings for our PI right.
[00:46:37.750 - 00:46:43.750] But we'll go over how to do that, as I said in class.
[00:46:43.750 - 00:46:51.750] You can run it open. Look, just to get things going, check out your design for the inductor size and so forth.
[00:46:51.750 - 00:46:55.750] Close loop control. We need that controller.
[00:46:55.750 - 00:46:59.750] Right. That was a lot.
[00:46:59.750 - 00:47:02.750] Any other questions just before we finish off? Yes.
[00:47:02.750 - 00:47:08.110] You don't change anything like that.
[00:47:08.110 - 00:47:12.110] The motor is the motor and it will draw the current that it draws.
[00:47:12.110 - 00:47:16.110] You're controlling the solar panel to always provide the maximum power.
[00:47:16.110 - 00:47:19.110] Irrespective of what the characteristics of the motor is doing.
[00:47:19.110 - 00:47:21.780] Anything else?
[00:47:21.780 - 00:47:26.340] Right. It's been nice and cozy today.

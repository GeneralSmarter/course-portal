# ENEL372-26S2 Lecture 13 native Echo transcript

Date: August 10, 2026 4:00pm-4:55pm
Transcript type: native Echo automated transcript.

[00:00:04:130 - 00:00:05:320] **Speaker 0:** Alright, Kyorakoto.
[00:00:05:570 - 00:00:06:469] **Speaker 0:** Welcome along.
[00:00:08:409 - 00:00:10:130] **Speaker 0:** Gonna have to rely a little bit more on my
[00:00:10:130 - 00:00:13:689] **Speaker 0:** voice projection today because the, uh, lapel microphone is completely
[00:00:13:689 - 00:00:14:050] **Speaker 0:** flat.
[00:00:14:449 - 00:00:17:879] **Speaker 0:** So um, I've also got the, the, um, lectern microphone
[00:00:17:879 - 00:00:18:530] **Speaker 0:** turned way up.
[00:00:18:610 - 00:00:22:010] **Speaker 0:** So hopefully the volume or the, the audio on the
[00:00:22:010 - 00:00:24:049] **Speaker 0:** Echo 360 recording is OK.
[00:00:24:209 - 00:00:26:250] **Speaker 0:** I'll try not to turn away from the microphone too
[00:00:26:250 - 00:00:26:629] **Speaker 0:** often.
[00:00:27:659 - 00:00:31:520] **Speaker 0:** OK, so this week we're kind of moving away from
[00:00:31:520 - 00:00:36:979] **Speaker 0:** uh just looking at various um power electronic converters, and
[00:00:36:979 - 00:00:39:959] **Speaker 0:** we're going to move into an application consideration.
[00:00:40:439 - 00:00:44:459] **Speaker 0:** And we're moving into this particular consider application consideration because
[00:00:44:459 - 00:00:47:599] **Speaker 0:** it is so common, so, so common, um.
[00:00:48:130 - 00:00:51:529] **Speaker 0:** We are going to be looking at um utilising an
[00:00:51:529 - 00:00:55:450] **Speaker 0:** electric motor to drive a mechanical load, right?
[00:00:55:659 - 00:00:59:250] **Speaker 0:** So it's it's pretty simple sounding, but it is just
[00:00:59:250 - 00:01:01:169] **Speaker 0:** so commonly found.
[00:01:01:250 - 00:01:04:128] **Speaker 0:** You have it in so many of your industrial processes,
[00:01:04:730 - 00:01:08:029] **Speaker 0:** where anything that's moving tends to be electric motor driven.
[00:01:08:199 - 00:01:13:860] **Speaker 0:** Um, you've got transportation, uh, you've got domestic appliances and
[00:01:13:860 - 00:01:14:830] **Speaker 0:** so forth and so on.
[00:01:15:459 - 00:01:20:129] **Speaker 0:** Generally, uh, a really substantial amount of the time if
[00:01:20:129 - 00:01:24:400] **Speaker 0:** you're trying to move something in space, uh, you utilise
[00:01:24:400 - 00:01:25:779] **Speaker 0:** electric motors to do that.
[00:01:26:089 - 00:01:29:389] **Speaker 0:** Um, it, it kind of goes hand in hand with,
[00:01:29:459 - 00:01:32:370] **Speaker 0:** um, electrical power being so readily available in a lot
[00:01:32:370 - 00:01:35:690] **Speaker 0:** of the time, and, as we've seen in recent years,
[00:01:35:739 - 00:01:40:919] **Speaker 0:** is becoming more and more common for large scale transportation
[00:01:40:919 - 00:01:41:269] **Speaker 0:** applications.
[00:01:42:750 - 00:01:43:250] **Speaker 0:** Right.
[00:01:43:589 - 00:01:47:269] **Speaker 0:** Um, so we're going to spend today just looking at
[00:01:47:269 - 00:01:51:669] **Speaker 0:** generally motors driving mechanical loads and some of the considerations
[00:01:51:669 - 00:01:52:430] **Speaker 0:** we might make.
[00:01:52:819 - 00:01:54:849] **Speaker 0:** This is not a mechanical engineering course.
[00:01:55:150 - 00:01:58:230] **Speaker 0:** The mechatronics students in the course have probably got way
[00:01:58:230 - 00:02:02:069] **Speaker 0:** more background to do with driving of mechanical loads and
[00:02:02:069 - 00:02:06:069] **Speaker 0:** things that affect uh that that sort of application.
[00:02:06:550 - 00:02:08:919] **Speaker 0:** We're just going to be uh taking a brief or
[00:02:08:919 - 00:02:12:389] **Speaker 0:** a light once over here, so not not deep diving
[00:02:12:389 - 00:02:16:169] **Speaker 0:** into this at all, but getting the idea across.
[00:02:16:789 - 00:02:17:830] **Speaker 0:** OK, so.
[00:02:18:960 - 00:02:22:690] **Speaker 0:** Uh, to do our job well, uh, it's a motor
[00:02:22:690 - 00:02:25:869] **Speaker 0:** driving, electric motor driving a load, we have to consider,
[00:02:26:009 - 00:02:30:389] **Speaker 0:** um, the mechanical characteristics of the load, uh, along with
[00:02:30:850 - 00:02:35:929] **Speaker 0:** the characteristics of the motor, um, both mechanical and electrical.
[00:02:37:220 - 00:02:42:229] **Speaker 0:** So Ping it down to its most basic form, a
[00:02:42:229 - 00:02:43:960] **Speaker 0:** typical system may look like this, where you've got a
[00:02:43:960 - 00:02:48:919] **Speaker 0:** motor, uh, it's spinning around, driving some sort of load
[00:02:48:919 - 00:02:51:800] **Speaker 0:** which is rotationally um based.
[00:02:53:119 - 00:02:59:039] **Speaker 0:** In between, you almost invariably, not always, but almost all
[00:02:59:039 - 00:03:01:919] **Speaker 0:** the time, find some sort of gearbox because you find
[00:03:01:919 - 00:03:06:360] **Speaker 0:** that the, the torque uh and speed characteristics of the
[00:03:06:360 - 00:03:10:190] **Speaker 0:** motor do not match well to generally a given mechanical
[00:03:10:190 - 00:03:10:600] **Speaker 0:** load.
[00:03:12:679 - 00:03:15:949] **Speaker 0:** So we have um the motor.
[00:03:16:080 - 00:03:17:220] **Speaker 0:** So motor design.
[00:03:22:029 - 00:03:23:199] **Speaker 0:** Uh, involves.
[00:03:25:460 - 00:03:37:240] **Speaker 0:** maximising Uh, power density Often, OK, this is, this is
[00:03:37:240 - 00:03:38:119] **Speaker 0:** pretty broad, right?
[00:03:38:240 - 00:03:40:320] **Speaker 0:** You know, motor design, you've got a whole bunch of
[00:03:40:320 - 00:03:43:559] **Speaker 0:** things, a big part of it being the, the whole
[00:03:43:559 - 00:03:46:029] **Speaker 0:** economics involved, uh, limiting what you can do.
[00:03:46:320 - 00:03:49:240] **Speaker 0:** But generally we're trying to get as much power from
[00:03:49:240 - 00:03:52:059] **Speaker 0:** a given motor size that we, that we have.
[00:03:54:539 - 00:03:56:729] **Speaker 0:** Uh, which means maximising power density.
[00:03:57:149 - 00:03:58:169] **Speaker 0:** And to do this.
[00:04:02:350 - 00:04:08:990] **Speaker 0:** They tend To operate at quite high speed.
[00:04:19:347 - 00:04:22:799] **Speaker 0:** They operate at quite high rotational speed and lower torque.
[00:04:31:910 - 00:04:35:309] **Speaker 0:** So matching the motor to the load, um, as I
[00:04:35:309 - 00:04:37:790] **Speaker 0:** said, because of this will generally involve some sort of
[00:04:37:790 - 00:04:42:309] **Speaker 0:** gearbox because most mechanical loads don't tend to spin very
[00:04:42:309 - 00:04:46:429] **Speaker 0:** fast, um, and but do often require quite a bit
[00:04:46:429 - 00:04:46:989] **Speaker 0:** of torque.
[00:04:48:059 - 00:04:48:260] **Speaker 0:** Yep.
[00:04:49:320 - 00:05:00:609] **Speaker 0:** So the load Uh, carrying out the job we want
[00:05:00:609 - 00:05:00:989] **Speaker 0:** done.
[00:05:09:079 - 00:05:13:429] **Speaker 0:** So we usually consider designers associated with an electric motor
[00:05:13:429 - 00:05:14:359] **Speaker 0:** driving a load.
[00:05:14:720 - 00:05:16:839] **Speaker 0:** We usually look at the design from the load side
[00:05:16:839 - 00:05:17:420] **Speaker 0:** first.
[00:05:47:380 - 00:05:52:829] **Speaker 0:** Um, And as far as doing the job that we
[00:05:52:829 - 00:05:56:829] **Speaker 0:** want to do, most often requires some sort of control
[00:05:56:829 - 00:05:57:589] **Speaker 0:** being undertaken.
[00:05:58:029 - 00:06:00:540] **Speaker 0:** So what are the things involved with with the load?
[00:06:00:589 - 00:06:01:489] **Speaker 0:** Well, we had talk.
[00:06:03:119 - 00:06:04:290] **Speaker 0:** Uh, we have speed.
[00:06:06:100 - 00:06:09:779] **Speaker 0:** Um, and even under some types of applications, you may
[00:06:09:779 - 00:06:12:940] **Speaker 0:** want to have the load rotate and stop at a
[00:06:12:940 - 00:06:13:760] **Speaker 0:** certain position.
[00:06:14:220 - 00:06:15:619] **Speaker 0:** So it could be position as well.
[00:06:22:649 - 00:06:25:730] **Speaker 0:** So I just mentioned control there, so if we're going
[00:06:25:730 - 00:06:28:410] **Speaker 0:** to do that, then we may need to measure uh
[00:06:28:410 - 00:06:29:450] **Speaker 0:** what we've got there.
[00:06:33:459 - 00:06:35:359] **Speaker 0:** We've got some sort of control system.
[00:06:37:510 - 00:06:40:170] **Speaker 0:** Which takes that measurement as an input.
[00:06:41:450 - 00:06:45:570] **Speaker 0:** Um, but a control system, if it's, it's to be
[00:06:46:010 - 00:06:48:570] **Speaker 0:** controlled, then we need to tell it what it is
[00:06:48:570 - 00:06:51:890] **Speaker 0:** we want to compare what we're measuring against.
[00:06:52:290 - 00:06:54:920] **Speaker 0:** So we've got the measured we've got, and then we
[00:06:54:920 - 00:06:56:170] **Speaker 0:** would have ordered.
[00:06:57:769 - 00:06:59:010] **Speaker 0:** You know, that's what we want.
[00:07:03:049 - 00:07:06:089] **Speaker 0:** So our control system would compare these two things, what
[00:07:06:089 - 00:07:09:130] **Speaker 0:** we've got and what we want, come up with some
[00:07:09:130 - 00:07:14:170] **Speaker 0:** sort of error, and Um, some sort of processing around
[00:07:14:170 - 00:07:14:779] **Speaker 0:** that era.
[00:07:15:510 - 00:07:18:769] **Speaker 0:** And will output, as far as we're concerned for a
[00:07:18:950 - 00:07:20:130] **Speaker 0:** power electronic system.
[00:07:28:950 - 00:07:31:290] **Speaker 0:** Uh, it's more than likely, well, certainly for all of
[00:07:31:290 - 00:07:33:799] **Speaker 0:** the types of converters that we're looking at, um, will
[00:07:33:799 - 00:07:36:799] **Speaker 0:** be some factor that tells us what kind of duty
[00:07:36:799 - 00:07:41:279] **Speaker 0:** ratio we are trying to to to output or use
[00:07:41:279 - 00:07:42:160] **Speaker 0:** for our output.
[00:07:43:209 - 00:07:46:279] **Speaker 0:** And of course our power electronics then provides the input
[00:07:46:799 - 00:07:49:380] **Speaker 0:** to the motor in order for it to achieve.
[00:07:50:489 - 00:07:52:420] **Speaker 0:** What uh what we want.
[00:07:53:149 - 00:07:54:220] **Speaker 0:** Through what we're measuring.
[00:07:58:290 - 00:08:01:869] **Speaker 0:** Right, of course that outputs of voltage and current combination
[00:08:01:869 - 00:08:03:589] **Speaker 0:** that achieves that goal.
[00:08:10:970 - 00:08:11:209] **Speaker 0:** Right.
[00:08:11:290 - 00:08:18:170] **Speaker 0:** So loads, mechanical loads and motors themselves have both steady
[00:08:18:170 - 00:08:23:290] **Speaker 0:** state and dynamic characteristics that we need to consider if
[00:08:23:290 - 00:08:26:670] **Speaker 0:** we're going to achieve the sort of closed loop control
[00:08:27:049 - 00:08:30:609] **Speaker 0:** of our mechanical load being driven by an electric motor.
[00:08:31:910 - 00:08:33:239] **Speaker 0:** So, let's have a look at those.
[00:08:39:260 - 00:08:42:789] **Speaker 0:** So first up, uh, the most common thing is looking
[00:08:42:789 - 00:08:46:309] **Speaker 0:** at the steady state, uh, aspect.
[00:08:46:909 - 00:08:50:090] **Speaker 0:** So we look at, um, steady state torque speed curves
[00:08:50:549 - 00:08:53:710] **Speaker 0:** for both our loads, uh, both load side and our
[00:08:53:710 - 00:08:54:530] **Speaker 0:** motor side.
[00:08:56:929 - 00:08:59:169] **Speaker 0:** So for an electric motor to be able to drive
[00:08:59:169 - 00:09:02:650] **Speaker 0:** a mechanical load in a continuous or steady-state way, you
[00:09:02:650 - 00:09:04:929] **Speaker 0:** have to have at least one intercept point between the
[00:09:04:929 - 00:09:06:489] **Speaker 0:** respective torque speed curves.
[00:09:07:710 - 00:09:09:890] **Speaker 0:** Right, so, and as I said that most often requires
[00:09:09:890 - 00:09:11:739] **Speaker 0:** a gearbox.
[00:09:11:789 - 00:09:14:429] **Speaker 0:** So we've got a vertical separation here, so on this
[00:09:14:429 - 00:09:16:309] **Speaker 0:** side, these are loads.
[00:09:17:469 - 00:09:18:950] **Speaker 0:** And on this side is motors.
[00:09:20:119 - 00:09:22:409] **Speaker 0:** But they are both to speed.
[00:09:23:880 - 00:09:24:520] **Speaker 0:** Curves.
[00:09:26:380 - 00:09:26:739] **Speaker 0:** What?
[00:09:29:590 - 00:09:31:710] **Speaker 0:** So you can have different kinds of mechanical loads.
[00:09:32:109 - 00:09:35:109] **Speaker 0:** Just two examples shown here are representative examples.
[00:09:35:390 - 00:09:38:909] **Speaker 0:** This would be a linear type of uh changing torque
[00:09:38:909 - 00:09:41:099] **Speaker 0:** versus speed, right?
[00:09:41:229 - 00:09:43:580] **Speaker 0:** So what are some linear style loads?
[00:09:43:590 - 00:09:45:710] **Speaker 0:** Well this could be lifts and hoists.
[00:09:49:109 - 00:09:54:750] **Speaker 0:** Conveyors Ah, compressors, that sort of thing.
[00:09:55:409 - 00:09:58:320] **Speaker 0:** So you end up with this linear response with your
[00:09:58:320 - 00:10:00:729] **Speaker 0:** torque speed for the characteristic.
[00:10:01:049 - 00:10:03:369] **Speaker 0:** So you pick a particular speed and there will be
[00:10:03:369 - 00:10:05:280] **Speaker 0:** a particular torque that is generated from it.
[00:10:05:289 - 00:10:05:830] **Speaker 0:** It's a point.
[00:10:06:929 - 00:10:07:789] **Speaker 0:** For steady state.
[00:10:09:450 - 00:10:13:409] **Speaker 0:** Uh, this curve following a squared relationship here, uh, this
[00:10:13:409 - 00:10:16:330] **Speaker 0:** could be from a fan load.
[00:10:18:299 - 00:10:21:820] **Speaker 0:** Very, very, very common load for um an electric motor
[00:10:21:820 - 00:10:22:820] **Speaker 0:** to drive a fan.
[00:10:23:789 - 00:10:24:030] **Speaker 0:** What?
[00:10:24:929 - 00:10:27:890] **Speaker 0:** One of the few instances where you might regularly expect
[00:10:27:890 - 00:10:31:210] **Speaker 0:** to see no gearbox between the motor itself and and
[00:10:31:210 - 00:10:31:770] **Speaker 0:** the fan.
[00:10:35:510 - 00:10:38:200] **Speaker 0:** Um, on the motor side, we've got two examples of
[00:10:38:200 - 00:10:39:590] **Speaker 0:** a motor torque speed curve.
[00:10:39:890 - 00:10:40:929] **Speaker 0:** This one here.
[00:10:42:789 - 00:10:45:020] **Speaker 0:** Anyone recognise that torque speed curve?
[00:10:46:140 - 00:10:49:080] **Speaker 0:** Yes, oh, I heard it, induction motor.
[00:10:50:539 - 00:10:51:280] **Speaker 0:** Nice.
[00:10:57:419 - 00:10:58:320] **Speaker 0:** Quite non-linear.
[00:10:59:650 - 00:11:02:489] **Speaker 0:** Um, the other one that we've got here could be
[00:11:02:489 - 00:11:05:849] **Speaker 0:** a range of different types of motors, um.
[00:11:06:619 - 00:11:13:250] **Speaker 0:** Ah, synchronous motors, brushless DC motors, even some DC motors
[00:11:13:250 - 00:11:17:489] **Speaker 0:** exhibit this type of behaviour for their torque speed characteristic.
[00:11:22:330 - 00:11:26:479] **Speaker 0:** Um, OK, so on this particular induction motor, I'm just
[00:11:26:479 - 00:11:30:400] **Speaker 0:** trying to highlight a potential issue with not matching well
[00:11:30:400 - 00:11:33:789] **Speaker 0:** matching a load torque speed curve with it's with a
[00:11:33:789 - 00:11:34:799] **Speaker 0:** motor torque speed curve.
[00:11:35:000 - 00:11:37:760] **Speaker 0:** Just imagine that there is the appropriate gearbox in between.
[00:11:38:159 - 00:11:43:229] **Speaker 0:** Um, so what you're aiming for is to have um.
[00:11:44:520 - 00:11:48:200] **Speaker 0:** Most ideally, it says there must be at least at
[00:11:48:200 - 00:11:51:080] **Speaker 0:** least one intercept point, so we're looking for an intercept
[00:11:51:080 - 00:11:53:859] **Speaker 0:** point between the torque and speed, uh, curves of both
[00:11:53:859 - 00:11:57:679] **Speaker 0:** the the motor and the load, but more ideally it
[00:11:57:679 - 00:11:59:859] **Speaker 0:** would be when it says at least one would be
[00:12:00:650 - 00:12:04:880] **Speaker 0:** only one intercept for stability purposes.
[00:12:06:260 - 00:12:09:219] **Speaker 0:** So this bottom curve, uh, which would be kind of
[00:12:09:219 - 00:12:12:179] **Speaker 0:** like a lift, where at zero speed there is zero
[00:12:12:179 - 00:12:16:780] **Speaker 0:** torque, so you end up with an increasing curve for
[00:12:16:780 - 00:12:19:299] **Speaker 0:** the load, and we can see that for this particular
[00:12:19:299 - 00:12:22:659] **Speaker 0:** induction motor, there is an intercept point here at one
[00:12:22:659 - 00:12:23:000] **Speaker 0:** instance.
[00:12:25:429 - 00:12:30:270] **Speaker 0:** So if you drove that particular mechanical load with that
[00:12:30:270 - 00:12:34:789] **Speaker 0:** particular induction motor, it would speed up until you got
[00:12:34:789 - 00:12:38:750] **Speaker 0:** to this torque rate level, and it would sit there
[00:12:38:750 - 00:12:39:710] **Speaker 0:** nice and stably.
[00:12:42:500 - 00:12:42:780] **Speaker 0:** Yeah.
[00:12:44:210 - 00:12:46:250] **Speaker 0:** So when I say nice and stable, it means that
[00:12:46:250 - 00:12:49:849] **Speaker 0:** for at least a reasonable amount of change in torque,
[00:12:50:250 - 00:12:53:250] **Speaker 0:** you're not going to see very much change in speed.
[00:12:55:179 - 00:12:59:460] **Speaker 0:** Um, there is what is known as a rather large
[00:12:59:460 - 00:13:00:659] **Speaker 0:** intersect angle.
[00:13:01:099 - 00:13:10:429] **Speaker 0:** All right, so here is the Intersect angle And it's
[00:13:10:429 - 00:13:11:530] **Speaker 0:** relatively large.
[00:13:13:390 - 00:13:15:429] **Speaker 0:** The closer it gets to 90 degrees, the better.
[00:13:17:619 - 00:13:21:270] **Speaker 0:** The other example here with a with a a load
[00:13:21:270 - 00:13:25:950] **Speaker 0:** that has a much higher starting torque, um, and then
[00:13:25:950 - 00:13:30:669] **Speaker 0:** it moves across the motor torque speed curve, that has
[00:13:30:669 - 00:13:31:469] **Speaker 0:** two intersects.
[00:13:32:929 - 00:13:36:450] **Speaker 0:** So if you actually had connected this load, going from
[00:13:36:450 - 00:13:40:049] **Speaker 0:** the motor being in a spinning state, it would have
[00:13:40:049 - 00:13:41:890] **Speaker 0:** slowed down and reached this point.
[00:13:42:450 - 00:13:45:090] **Speaker 0:** However, if you had the same load and you started
[00:13:45:090 - 00:13:46:429] **Speaker 0:** it off from standstill.
[00:13:48:289 - 00:13:49:469] **Speaker 0:** It wouldn't go.
[00:13:50:150 - 00:13:53:270] **Speaker 0:** It wouldn't rotate at all, because the starting torque of
[00:13:53:270 - 00:13:57:190] **Speaker 0:** the motor is less than the required starting torque of
[00:13:57:190 - 00:13:58:109] **Speaker 0:** the load.
[00:13:59:390 - 00:14:02:559] **Speaker 0:** However, if you were to kick it to maybe moving
[00:14:02:559 - 00:14:05:119] **Speaker 0:** it this fast, it would slow down and go to
[00:14:05:119 - 00:14:05:799] **Speaker 0:** S1.
[00:14:07:340 - 00:14:10:090] **Speaker 0:** Hm, but not very stably.
[00:14:11:119 - 00:14:13:179] **Speaker 0:** A small change in torque is going to result in
[00:14:13:179 - 00:14:16:099] **Speaker 0:** quite a substantial change in speed.
[00:14:16:929 - 00:14:19:210] **Speaker 0:** Right, so it has a low intercept angle.
[00:14:21:580 - 00:14:30:500] **Speaker 0:** So that's high And then a low Which is not
[00:14:30:500 - 00:14:30:880] **Speaker 0:** good.
[00:14:31:900 - 00:14:35:340] **Speaker 0:** Potentially then, depending how close this one might have been
[00:14:35:340 - 00:14:39:500] **Speaker 0:** to this peak here, it could by changing the torque,
[00:14:39:559 - 00:14:45:099] **Speaker 0:** it could suddenly slip from your intended operating point to
[00:14:45:099 - 00:14:46:119] **Speaker 0:** another stable point.
[00:14:47:229 - 00:14:49:130] **Speaker 0:** So it's not good, it's not a good situation.
[00:14:49:190 - 00:14:52:030] **Speaker 0:** You want it to be single, um, intercept point if
[00:14:52:030 - 00:14:52:590] **Speaker 0:** possible.
[00:14:53:369 - 00:14:55:390] **Speaker 0:** Would that be a negative intersecting?
[00:14:57:700 - 00:14:59:409] **Speaker 0:** Uh, no, you just take the absolute.
[00:15:01:500 - 00:15:08:390] **Speaker 0:** Um, here, you know, you could have potentially a A
[00:15:08:390 - 00:15:09:770] **Speaker 0:** low that kind of looks like that.
[00:15:10:789 - 00:15:15:679] **Speaker 0:** Uh, it's important here that it intersects for the torque
[00:15:15:679 - 00:15:20:450] **Speaker 0:** speed of the motor, where it's at its rated curve,
[00:15:20:679 - 00:15:22:440] **Speaker 0:** so continuous torque zone.
[00:15:24:049 - 00:15:28:890] **Speaker 0:** Uh, some of these motors like brushless DC or synchronous
[00:15:28:890 - 00:15:32:690] **Speaker 0:** machines, they can for short periods of time be driven
[00:15:32:690 - 00:15:36:609] **Speaker 0:** so that they provide um excess torque, but you can't
[00:15:36:609 - 00:15:37:330] **Speaker 0:** run them there for long.
[00:15:37:409 - 00:15:41:090] **Speaker 0:** They'll overheat and, uh, effectively damage themselves.
[00:15:41:210 - 00:15:44:309] **Speaker 0:** So there are, there are zones that you work within
[00:15:44:690 - 00:15:46:289] **Speaker 0:** those types of motors.
[00:15:51:010 - 00:15:54:760] **Speaker 0:** OK, so Just try to highlight that we've got to
[00:15:54:760 - 00:15:57:880] **Speaker 0:** be careful when we're choosing a motor that is driving
[00:15:57:880 - 00:16:00:520] **Speaker 0:** a low mechanical load under a particular application.
[00:16:00:880 - 00:16:03:510] **Speaker 0:** We want there to be ideally just a single intersect,
[00:16:03:960 - 00:16:07:940] **Speaker 0:** and they do need to be able to intersect also
[00:16:08:159 - 00:16:08:500] **Speaker 0:** that.
[00:16:09:630 - 00:16:13:429] **Speaker 0:** Where you are intending on starting up the system from,
[00:16:13:549 - 00:16:15:710] **Speaker 0:** is it starting up from standstill or is the motor
[00:16:15:710 - 00:16:18:210] **Speaker 0:** running and you're bringing in the load whilst it's running,
[00:16:18:630 - 00:16:21:349] **Speaker 0:** makes a difference as to where it will end up
[00:16:21:349 - 00:16:23:609] **Speaker 0:** potentially, uh, as a as a stable point.
[00:16:24:979 - 00:16:26:640] **Speaker 0:** Not only that, it's got to be large enough to
[00:16:26:640 - 00:16:28:320] **Speaker 0:** start the load in the first place if you're doing
[00:16:28:320 - 00:16:29:200] **Speaker 0:** it from standstill.
[00:16:32:469 - 00:16:33:280] **Speaker 0:** Any questions there?
[00:16:36:570 - 00:16:36:650] **Speaker 0:** Cri.
[00:16:41:760 - 00:16:43:260] **Speaker 0:** So the choice of the motor.
[00:16:46:710 - 00:16:48:270] **Speaker 0:** Right, so we need to choose a motor that can
[00:16:48:270 - 00:16:52:030] **Speaker 0:** start if you're going from standstill especially, uh, and it
[00:16:52:030 - 00:16:55:260] **Speaker 0:** has those motor motor load torque speed curves that intersect
[00:16:55:260 - 00:16:56:169] **Speaker 0:** at high angles.
[00:16:57:669 - 00:16:59:679] **Speaker 0:** Uh, and we'll all almost always need to choose a
[00:16:59:679 - 00:17:00:460] **Speaker 0:** gearbox.
[00:17:02:010 - 00:17:05:479] **Speaker 0:** Alright, that matches those steady state ah torque speed requirements.
[00:17:07:520 - 00:17:11:640] **Speaker 0:** Within that, we would also tend to try and choose
[00:17:11:640 - 00:17:15:359] **Speaker 0:** an intersect point that will enable us to use the
[00:17:15:359 - 00:17:17:020] **Speaker 0:** motor efficiently.
[00:17:18:920 - 00:17:20:630] **Speaker 0:** Right, and it matters.
[00:17:20:959 - 00:17:23:619] **Speaker 0:** So you can have an intersect point though that um
[00:17:24:079 - 00:17:26:260] **Speaker 0:** isn't so efficient for the motor operation.
[00:17:26:319 - 00:17:30:739] **Speaker 0:** So you could potentially for this particular motor, it's a
[00:17:30:739 - 00:17:33:780] **Speaker 0:** brushless DC motor, it's an efficiency map.
[00:17:34:040 - 00:17:36:680] **Speaker 0:** So where you see the red that is at its
[00:17:36:680 - 00:17:41:140] **Speaker 0:** highest rating of between 93 and 94% electrically efficient.
[00:17:42:579 - 00:17:45:319] **Speaker 0:** Right, and this is it's torque speed curve, so speed
[00:17:45:579 - 00:17:48:439] **Speaker 0:** going up to 3000 plus RPM.
[00:17:49:300 - 00:17:52:500] **Speaker 0:** This is an RPM and vertically you're torque in Newton
[00:17:52:500 - 00:17:53:010] **Speaker 0:** metres.
[00:17:55:000 - 00:17:59:760] **Speaker 0:** So ideally you would want to operate and have you
[00:17:59:760 - 00:18:03:010] **Speaker 0:** intersect with your torque speed for the motor somewhere in
[00:18:03:010 - 00:18:05:479] **Speaker 0:** this red region, so it's nice and efficient.
[00:18:07:510 - 00:18:09:270] **Speaker 0:** There is a range there though, you know, you could
[00:18:09:270 - 00:18:10:609] **Speaker 0:** work all the way from.
[00:18:11:500 - 00:18:14:880] **Speaker 0:** This intersect point for your load and perhaps your load.
[00:18:15:770 - 00:18:20:250] **Speaker 0:** Has some variation associated with that, and it wants to
[00:18:20:250 - 00:18:21:420] **Speaker 0:** operate at another point.
[00:18:21:849 - 00:18:24:729] **Speaker 0:** So you could choose this motor and right over this
[00:18:24:729 - 00:18:28:010] **Speaker 0:** load range, it acts at a very, very high electrical
[00:18:28:010 - 00:18:28:750] **Speaker 0:** efficiency.
[00:18:30:339 - 00:18:33:780] **Speaker 0:** OK, what you don't want to do is choose a
[00:18:33:780 - 00:18:35:680] **Speaker 0:** situation where it starts moving away.
[00:18:35:939 - 00:18:38:160] **Speaker 0:** So you talk speed, you know, maybe very low speed.
[00:18:39:140 - 00:18:43:189] **Speaker 0:** Um, or you've got it rotating very, very quickly, but
[00:18:43:189 - 00:18:44:150] **Speaker 0:** at very low torque.
[00:18:46:829 - 00:18:49:079] **Speaker 0:** Still not bad for that map though, even at its
[00:18:49:079 - 00:18:51:959] **Speaker 0:** worst efficiency, that's 74 to 75% efficient.
[00:18:53:449 - 00:18:57:449] **Speaker 0:** For this particular map, so electric motors are of particular
[00:18:57:449 - 00:19:01:650] **Speaker 0:** types can work efficiently over quite the range of torque
[00:19:01:650 - 00:19:02:239] **Speaker 0:** and speed.
[00:19:08:489 - 00:19:11:170] **Speaker 0:** Uh, there are some limits, uh, that we have on
[00:19:11:170 - 00:19:14:329] **Speaker 0:** even observable on this, uh, this plot.
[00:19:14:849 - 00:19:17:030] **Speaker 0:** Why can't we move up into this space?
[00:19:18:050 - 00:19:20:420] **Speaker 0:** Well, this part of it has to do with the
[00:19:20:880 - 00:19:23:920] **Speaker 0:** maximum voltage rating of the motor.
[00:19:25:130 - 00:19:27:469] **Speaker 0:** Right, motors are rated at particular voltages.
[00:19:27:849 - 00:19:29:569] **Speaker 0:** Uh, if you try to go beyond that, you could
[00:19:29:569 - 00:19:33:790] **Speaker 0:** compromise the insulation, um, on the, on the motor windings,
[00:19:33:810 - 00:19:35:189] **Speaker 0:** so you don't over voltage.
[00:19:35:729 - 00:19:39:229] **Speaker 0:** All right, so we've got the power, which is uh
[00:19:39:489 - 00:19:41:910] **Speaker 0:** voltage times current or torque times speed.
[00:19:42:250 - 00:19:45:030] **Speaker 0:** So the power limit, which is what we're seeing here.
[00:19:49:859 - 00:19:54:400] **Speaker 0:** Uh, which is due To voltage rating.
[00:19:57:489 - 00:19:58:170] **Speaker 0:** Of the motor.
[00:19:58:449 - 00:20:03:550] **Speaker 0:** So we have power max is equal to V rated.
[00:20:04:439 - 00:20:05:780] **Speaker 0:** Times I max.
[00:20:08:300 - 00:20:11:819] **Speaker 0:** Right, but we have V rated.
[00:20:12:880 - 00:20:16:760] **Speaker 0:** Minus our back EMF, so.
[00:20:17:550 - 00:20:20:180] **Speaker 0:** E, that's a voltage back EMF.
[00:20:21:189 - 00:20:24:280] **Speaker 0:** So as the motor spins faster and faster, we get
[00:20:24:280 - 00:20:25:680] **Speaker 0:** more and more back EMF.
[00:20:26:520 - 00:20:36:280] **Speaker 0:** And The current, Max is proportional to be rated minus
[00:20:36:280 - 00:20:37:420] **Speaker 0:** the Beck EMF.
[00:20:38:410 - 00:20:39:630] **Speaker 0:** Sorry, this is IMAX.
[00:20:42:770 - 00:20:47:829] **Speaker 0:** So as we go up in speed, um, the power,
[00:20:48:410 - 00:20:55:770] **Speaker 0:** um, is reduced because IMAX reduces, not because the voltage
[00:20:55:770 - 00:20:58:369] **Speaker 0:** changes, that's at its rate of voltage, but we have
[00:20:58:369 - 00:21:01:719] **Speaker 0:** a reduction in the maximum current because that back MF
[00:21:01:719 - 00:21:02:969] **Speaker 0:** increases at higher speeds.
[00:21:04:060 - 00:21:10:069] **Speaker 0:** So that's a power limit Um It does, although it's
[00:21:10:069 - 00:21:14:030] **Speaker 0:** rather annoyingly underneath this label, this curve does have a
[00:21:14:030 - 00:21:15:750] **Speaker 0:** knee point associated with it.
[00:21:17:670 - 00:21:20:219] **Speaker 0:** So this curve part of the curve is due to
[00:21:20:219 - 00:21:23:199] **Speaker 0:** the uh the voltage trading and a reducing current.
[00:21:24:430 - 00:21:27:550] **Speaker 0:** This limitation is due to the maximum current that's allowed,
[00:21:27:949 - 00:21:32:469] **Speaker 0:** so it picks up the torque in a motor electric
[00:21:32:469 - 00:21:34:630] **Speaker 0:** motor is proportional to the current that's flowing through the
[00:21:34:630 - 00:21:35:410] **Speaker 0:** windings.
[00:21:36:069 - 00:21:38:849] **Speaker 0:** So this is a current.
[00:21:41:199 - 00:21:43:150] **Speaker 0:** Peak Limit.
[00:21:44:449 - 00:21:47:650] **Speaker 0:** So you can't go beyond the rated current, continuous rated
[00:21:47:650 - 00:21:48:849] **Speaker 0:** current of the motor either.
[00:21:54:380 - 00:21:56:410] **Speaker 0:** Right, so just, just to give you an idea of
[00:21:56:410 - 00:21:58:619] **Speaker 0:** why these, these points are as they are.
[00:21:59:989 - 00:22:00:000] **Speaker 0:** That.
[00:22:04:239 - 00:22:07:930] **Speaker 0:** All right, so to speed, we've got positive talk and
[00:22:07:930 - 00:22:11:069] **Speaker 0:** positive speed for this plot.
[00:22:11:900 - 00:22:14:479] **Speaker 0:** That's known as a quadrant of operation.
[00:22:15:599 - 00:22:15:800] **Speaker 0:** Right?
[00:22:15:920 - 00:22:17:719] **Speaker 0:** Positive speed, positive torque.
[00:22:18:969 - 00:22:24:449] **Speaker 0:** An electric motor is able to operate in If it's
[00:22:24:449 - 00:22:27:469] **Speaker 0:** set up right, is able to operate in 4 quadrants.
[00:22:34:229 - 00:22:35:530] **Speaker 0:** So here are our 4 quadrants.
[00:22:37:160 - 00:22:38:839] **Speaker 0:** Uh, and in a rather antiquated Dalek.
[00:22:39:839 - 00:22:41:400] **Speaker 0:** It's one that, it's one that can't fly.
[00:22:42:250 - 00:22:45:930] **Speaker 0:** Um, so here's our to speed, but rather than just
[00:22:45:930 - 00:22:49:609] **Speaker 0:** being limited to positive talk and speed, which is, as
[00:22:49:609 - 00:22:52:989] **Speaker 0:** we are used to understanding, you know, we, we drive
[00:22:52:989 - 00:22:57:469] **Speaker 0:** a, a motor, um, it has a rotation.
[00:22:59:010 - 00:23:03:530] **Speaker 0:** That's the same as the motor torque direction.
[00:23:04:369 - 00:23:06:449] **Speaker 0:** Sorry, that should be an arrow that looks like that.
[00:23:07:859 - 00:23:11:609] **Speaker 0:** Load torque is in the opposite direction, so this is
[00:23:11:910 - 00:23:13:410] **Speaker 0:** speed, so that's omega.
[00:23:14:439 - 00:23:20:479] **Speaker 0:** In that direction, rotational speed, in the same direction as
[00:23:20:479 - 00:23:23:479] **Speaker 0:** the movement of the motor or rotation of the motor,
[00:23:23:920 - 00:23:24:380] **Speaker 0:** the torque.
[00:23:25:199 - 00:23:26:530] **Speaker 0:** Uh, the load torque.
[00:23:30:640 - 00:23:32:949] **Speaker 0:** Is in the opposite direction, it's trying to oppose your
[00:23:32:949 - 00:23:33:989] **Speaker 0:** motor to.
[00:23:36:109 - 00:23:37:260] **Speaker 0:** So that's forward driving.
[00:23:37:489 - 00:23:40:160] **Speaker 0:** Of course, we could be operating in quadrant 2.
[00:23:41:290 - 00:23:45:589] **Speaker 0:** So this is trying to, in this case, stopping or
[00:23:46:530 - 00:23:48:869] **Speaker 0:** controlling the rate of descent of the vehicle.
[00:23:49:410 - 00:23:50:989] **Speaker 0:** So it's not letting it free fall.
[00:23:52:109 - 00:23:53:339] **Speaker 0:** And slide backwards.
[00:23:53:390 - 00:23:57:910] **Speaker 0:** This is applying a torque on the motor, which is
[00:23:57:910 - 00:24:00:630] **Speaker 0:** in the opposite direction for rotation.
[00:24:01:540 - 00:24:04:500] **Speaker 0:** So motor talk is in the same direction as before,
[00:24:04:579 - 00:24:06:760] **Speaker 0:** but now we're rolling backwards.
[00:24:08:099 - 00:24:12:069] **Speaker 0:** So The motor speed is in the opposite direction.
[00:24:14:979 - 00:24:22:540] **Speaker 0:** Hence negative speed Ah, the quadrant 3 is kind of
[00:24:22:540 - 00:24:24:560] **Speaker 0:** just the mirror of quadrant 1.
[00:24:25:000 - 00:24:30:319] **Speaker 0:** So you're going backwards, but you get going backwards in
[00:24:30:319 - 00:24:32:439] **Speaker 0:** driving torque into the motor in the same direction that
[00:24:32:439 - 00:24:33:040] **Speaker 0:** you're travelling.
[00:24:34:060 - 00:24:34:400] **Speaker 0:** Right?
[00:24:34:619 - 00:24:37:640] **Speaker 0:** So talk is in this direction, as is.
[00:24:39:949 - 00:24:41:290] **Speaker 0:** The motor direction.
[00:24:42:410 - 00:24:43:380] **Speaker 0:** You're just going backwards.
[00:24:48:739 - 00:24:51:619] **Speaker 0:** Alright, and then you've got your final uh quadrant, quadrant
[00:24:51:619 - 00:24:56:000] **Speaker 0:** 4, and this is the mirror to quadrant 2, so
[00:24:56:420 - 00:24:59:500] **Speaker 0:** you're moving forwards, down a slope sort of thing, but
[00:24:59:500 - 00:25:01:900] **Speaker 0:** you're trying to stop yourself from free-falling going down that
[00:25:01:900 - 00:25:02:420] **Speaker 0:** slope.
[00:25:04:170 - 00:25:08:180] **Speaker 0:** All right, so your torque is now backwards, even though
[00:25:08:180 - 00:25:10:800] **Speaker 0:** your motor is going forwards.
[00:25:16:260 - 00:25:18:589] **Speaker 0:** OK, so there are 4 quadrants of operation that we
[00:25:18:589 - 00:25:22:750] **Speaker 0:** could be looking at for between looking at the intersect
[00:25:22:750 - 00:25:26:469] **Speaker 0:** points, the torque speed between our motor and our load.
[00:25:30:290 - 00:25:33:400] **Speaker 0:** Is that Making reasonable sense there.
[00:25:36:010 - 00:25:36:020] **Speaker 0:** Right.
[00:25:37:010 - 00:25:41:130] **Speaker 0:** In each instance, whatever the direction of the motor torque
[00:25:41:130 - 00:25:44:270] **Speaker 0:** is, the load torque will be in the opposite direction
[00:25:44:650 - 00:25:45:449] **Speaker 0:** to the motor torque.
[00:25:52:900 - 00:25:55:119] **Speaker 0:** Well, that's all well and good for steady state.
[00:25:56:459 - 00:26:00:219] **Speaker 0:** But of course, a lot of the time, and a
[00:26:00:219 - 00:26:05:369] **Speaker 0:** lot of applications, we are concerned with The dynamics.
[00:26:06:310 - 00:26:09:310] **Speaker 0:** Of the connection between the mechanical load and the motor.
[00:26:09:790 - 00:26:12:790] **Speaker 0:** How well are we set up for the load being
[00:26:12:790 - 00:26:15:189] **Speaker 0:** able to accelerate and decelerate?
[00:26:15:469 - 00:26:19:130] **Speaker 0:** Yes, I know deceleration is just negative acceleration, but anyway,
[00:26:19:550 - 00:26:20:030] **Speaker 0:** so.
[00:26:21:239 - 00:26:25:880] **Speaker 0:** If we want to also consider the dynamics, then another
[00:26:25:880 - 00:26:29:390] **Speaker 0:** factor comes into play as as opposed to just talk
[00:26:29:390 - 00:26:34:060] **Speaker 0:** and speed, and that's the inertia of the system.
[00:26:34:680 - 00:26:38:280] **Speaker 0:** Yes, there are other factors that that are also in
[00:26:38:280 - 00:26:41:859] **Speaker 0:** play, um, such as uh.
[00:26:42:349 - 00:26:45:550] **Speaker 0:** You know, it's a number of factors influence acceleration.
[00:26:46:069 - 00:26:48:109] **Speaker 0:** What is the friction involved in the system?
[00:26:48:270 - 00:26:49:540] **Speaker 0:** Is there any flex as well?
[00:26:50:819 - 00:26:51:150] **Speaker 0:** All right.
[00:26:51:270 - 00:26:57:439] **Speaker 0:** So But buying away for most normal systems, the biggest
[00:26:57:439 - 00:27:00:959] **Speaker 0:** factor that comes into play is the inertia of the
[00:27:00:959 - 00:27:02:079] **Speaker 0:** rotational system.
[00:27:03:469 - 00:27:07:270] **Speaker 0:** So, looking at our um our standard uh.
[00:27:08:390 - 00:27:12:229] **Speaker 0:** Motor load system again with our gearbox, uh, we are
[00:27:12:229 - 00:27:16:869] **Speaker 0:** now thinking about considering the inertia which is, given the
[00:27:16:869 - 00:27:19:189] **Speaker 0:** symbol J here um of the system.
[00:27:23:880 - 00:27:27:839] **Speaker 0:** So we've got a motor producing a torque which is
[00:27:27:839 - 00:27:31:520] **Speaker 0:** TM for the motor and rotating at a speed omegam.
[00:27:31:959 - 00:27:37:119] **Speaker 0:** We have a gearbox which has an N1 ratio.
[00:27:40:469 - 00:27:40:930] **Speaker 0:** All right.
[00:27:42:040 - 00:27:43:650] **Speaker 0:** So we have a different.
[00:27:44:640 - 00:27:47:599] **Speaker 0:** Speed for the load and a different torque.
[00:27:48:540 - 00:27:59:390] **Speaker 0:** Um, right, Here for the dynamics, we're interested in the
[00:27:59:390 - 00:28:03:150] **Speaker 0:** rate of change of speed, so accelerating the load.
[00:28:04:250 - 00:28:06:250] **Speaker 0:** So we've got a DMga by DT.
[00:28:06:329 - 00:28:07:010] **Speaker 0:** That's acceleration.
[00:28:12:939 - 00:28:19:280] **Speaker 0:** Which By nice happenstance is equal to the talk.
[00:28:20:739 - 00:28:22:160] **Speaker 0:** Divided by the inertia.
[00:28:26:469 - 00:28:28:829] **Speaker 0:** In its most simple Terms.
[00:28:29:900 - 00:28:32:819] **Speaker 0:** There is an equivalence that we may be more used
[00:28:32:819 - 00:28:33:869] **Speaker 0:** to seeing.
[00:28:34:339 - 00:28:36:959] **Speaker 0:** This is equivalent to the rate of change of speed.
[00:28:41:439 - 00:28:43:979] **Speaker 0:** In a linear sense, so linear speed.
[00:28:45:969 - 00:28:49:170] **Speaker 0:** Uh, so the rate of change of speed, acceleration in
[00:28:49:170 - 00:28:53:010] **Speaker 0:** a straight line, uh, is equal to the force that
[00:28:53:010 - 00:28:55:010] **Speaker 0:** we're applying to a mass.
[00:28:55:569 - 00:28:58:689] **Speaker 0:** So force divided by mass gives us our rate of
[00:28:58:689 - 00:28:59:449] **Speaker 0:** acceleration.
[00:29:02:810 - 00:29:05:719] **Speaker 0:** Yeah, we're much more used to seeing it, uh, linear
[00:29:05:719 - 00:29:06:469] **Speaker 0:** accelerations.
[00:29:07:599 - 00:29:08:520] **Speaker 0:** So it's an equivalent.
[00:29:08:560 - 00:29:12:540] **Speaker 0:** It's not exactly the same because it's rotational, but to
[00:29:12:959 - 00:29:15:199] **Speaker 0:** see how it kind of relates to something that you're
[00:29:15:199 - 00:29:15:859] **Speaker 0:** more used to.
[00:29:19:380 - 00:29:21:959] **Speaker 0:** OK, so we're interested in this, this the Omega by
[00:29:21:959 - 00:29:22:280] **Speaker 0:** DT.
[00:29:23:560 - 00:29:29:040] **Speaker 0:** Uh, particularly since we're interested in the acceleration of the
[00:29:29:040 - 00:29:33:199] **Speaker 0:** load, that's where we would do, we start our analysis
[00:29:33:199 - 00:29:33:540] **Speaker 0:** from.
[00:29:36:250 - 00:29:41:250] **Speaker 0:** OK, so, We've got a gearbox then that is we're
[00:29:41:250 - 00:29:46:410] **Speaker 0:** looking to maybe optimise the gearbox ratio so that we
[00:29:46:410 - 00:29:50:930] **Speaker 0:** maximise this or optimise the acceleration in the load.
[00:29:52:369 - 00:29:55:609] **Speaker 0:** If we optimise that acceleration, we've got the best chance
[00:29:55:609 - 00:29:58:739] **Speaker 0:** of using our control system to dynamically control what that
[00:29:58:739 - 00:30:00:599] **Speaker 0:** motor is what that load is doing.
[00:30:03:060 - 00:30:07:869] **Speaker 0:** Alright, so There are extremes that we can go to,
[00:30:07:959 - 00:30:08:160] **Speaker 0:** right?
[00:30:08:280 - 00:30:10:560] **Speaker 0:** We can make in very large and we can make
[00:30:10:560 - 00:30:11:300] **Speaker 0:** in very small.
[00:30:12:630 - 00:30:15:310] **Speaker 0:** It has a different effect on what's happening at the
[00:30:15:310 - 00:30:16:089] **Speaker 0:** low side.
[00:30:17:020 - 00:30:21:900] **Speaker 0:** So if N is too small, then you're not getting
[00:30:21:900 - 00:30:25:699] **Speaker 0:** enough, probably enough talk at the load.
[00:30:26:439 - 00:30:29:910] **Speaker 0:** So it's not going to accelerate very quickly.
[00:30:30:369 - 00:30:32:609] **Speaker 0:** So if N is too small, torque driving the load
[00:30:32:609 - 00:30:33:670] **Speaker 0:** is torque too small.
[00:30:53:699 - 00:30:55:250] **Speaker 0:** Um, it's also.
[00:30:56:209 - 00:30:59:310] **Speaker 0:** Not really compatible with operating that motor in its most
[00:30:59:310 - 00:31:01:130] **Speaker 0:** efficient mode or state.
[00:31:36:900 - 00:31:39:739] **Speaker 0:** All right, OK, so that's, that's the effect of in
[00:31:39:739 - 00:31:40:400] **Speaker 0:** is too small.
[00:31:40:739 - 00:31:44:959] **Speaker 0:** It is too small, it means that um we're Basically
[00:31:44:959 - 00:31:49:119] **Speaker 0:** uh spinning the motor really fast, uh, with a small
[00:31:49:119 - 00:31:51:079] **Speaker 0:** torque, and that's being transferred to the load.
[00:31:53:420 - 00:31:56:859] **Speaker 0:** It's stepping, it's not with a small n.
[00:31:57:130 - 00:31:59:119] **Speaker 0:** We're actually kind of trying to step things up.
[00:32:00:369 - 00:32:01:650] **Speaker 0:** Like a transformer.
[00:32:01:890 - 00:32:04:729] **Speaker 0:** It'd be a step up or not very much step
[00:32:04:729 - 00:32:06:439] **Speaker 0:** down transformer.
[00:32:08:479 - 00:32:10:140] **Speaker 0:** Right, if N is too large.
[00:32:11:180 - 00:32:13:290] **Speaker 0:** And it's too large, it means that you're you're doing
[00:32:13:290 - 00:32:16:959] **Speaker 0:** a lot of rotations on the motor side with just
[00:32:16:959 - 00:32:19:939] **Speaker 0:** a little bit of rotation happening on the on the
[00:32:19:939 - 00:32:20:969] **Speaker 0:** output of the gearbox.
[00:32:21:709 - 00:32:24:030] **Speaker 0:** It's like a step down situation.
[00:32:24:310 - 00:32:26:010] **Speaker 0:** So most of the motor.
[00:32:27:089 - 00:32:36:709] **Speaker 0:** Talk I used to accelerate itself, accelerate its own rota.
[00:32:54:140 - 00:32:56:739] **Speaker 0:** And since N is so large, then the acceleration at
[00:32:56:739 - 00:32:59:719] **Speaker 0:** the low side is going to be pretty, pretty small.
[00:33:15:760 - 00:33:17:189] **Speaker 0:** So you're probably going to have to spin up the
[00:33:17:189 - 00:33:21:069] **Speaker 0:** motor to excessively high speeds in order to get any
[00:33:21:069 - 00:33:24:819] **Speaker 0:** kind of decent acceleration at the load side.
[00:33:24:989 - 00:33:28:180] **Speaker 0:** Again, not operating that motor in its most efficient state.
[00:33:35:270 - 00:33:36:150] **Speaker 0:** Well, that's all well and good.
[00:33:36:989 - 00:33:39:359] **Speaker 0:** But what's the best end to use for our for
[00:33:39:359 - 00:33:40:290] **Speaker 0:** our gearbox?
[00:33:40:880 - 00:33:42:560] **Speaker 0:** Is there any way of determining that?
[00:33:43:609 - 00:33:46:729] **Speaker 0:** Well, as it turns out, there is actually a pretty
[00:33:46:729 - 00:33:48:109] **Speaker 0:** decent way of determining that.
[00:33:52:839 - 00:33:56:140] **Speaker 0:** So let's go through the exercise of optimising acceleration.
[00:33:58:119 - 00:34:00:699] **Speaker 0:** So we want good performance, good acceleration performance.
[00:34:01:660 - 00:34:04:130] **Speaker 0:** Particularly useful for electric vehicles.
[00:34:04:709 - 00:34:08:830] **Speaker 0:** Um, right, in order to do that, then the main
[00:34:08:830 - 00:34:11:709] **Speaker 0:** tool we've got at our disposal is to optimise the
[00:34:11:709 - 00:34:12:770] **Speaker 0:** gearbox ratio.
[00:34:14:688 - 00:34:18:218] **Speaker 0:** Right, so accelerating the motor gearbox load system.
[00:34:19:090 - 00:34:22:570] **Speaker 0:** With a certain amount of inertia involved, um, it's like
[00:34:22:570 - 00:34:26:610] **Speaker 0:** transferring electrical energy into stored mechanical engineering energy.
[00:34:26:919 - 00:34:30:669] **Speaker 0:** So this is energy storage, this is rotational, of course.
[00:34:35:888 - 00:34:40:850] **Speaker 0:** is equal to 1/2 times the overall inertia and speed
[00:34:40:850 - 00:34:41:370] **Speaker 0:** squared.
[00:34:42:499 - 00:34:45:617] **Speaker 0:** You might think of this as being equivalent to a
[00:34:45:617 - 00:34:51:428] **Speaker 0:** linear system as being equal to 1/2 MU 2.
[00:34:52:459 - 00:34:53:739] **Speaker 0:** Where Em is the mess.
[00:34:54:959 - 00:34:57:379] **Speaker 0:** And this is the speed, linear speed.
[00:34:59:830 - 00:35:02:290] **Speaker 0:** What have I just given the equation for there?
[00:35:04:179 - 00:35:04:939] **Speaker 0:** Kinetic energy.
[00:35:05:020 - 00:35:05:439] **Speaker 0:** Yeah.
[00:35:05:979 - 00:35:10:020] **Speaker 0:** So that's that's energy that the that the item has
[00:35:10:020 - 00:35:12:860] **Speaker 0:** because it's moving through space at a particular speed.
[00:35:15:639 - 00:35:19:300] **Speaker 0:** So a gearbox does act very much like a mechanical
[00:35:19:679 - 00:35:23:860] **Speaker 0:** electrical transformer, except it's doing mechanical transformations.
[00:35:24:620 - 00:35:28:459] **Speaker 0:** So we have, as far as the turns ratio would
[00:35:28:459 - 00:35:31:840] **Speaker 0:** be for a for a transformer, we've got the ratio
[00:35:31:840 - 00:35:36:219] **Speaker 0:** for the gearbox, um, that the load speed is equal
[00:35:36:219 - 00:35:41:199] **Speaker 0:** to the motor speed divided by The gearbox ratio It's
[00:35:41:199 - 00:35:41:719] **Speaker 0:** defined.
[00:35:42:540 - 00:35:46:060] **Speaker 0:** Uh, just before, and then the torque at the load
[00:35:46:060 - 00:35:49:850] **Speaker 0:** is equal to the gearbox ratio times the motor torque.
[00:35:50:739 - 00:35:52:260] **Speaker 0:** So it's kind of like voltage and current for a
[00:35:52:260 - 00:35:53:000] **Speaker 0:** transformer.
[00:35:53:260 - 00:35:56:610] **Speaker 0:** This is equivalent to voltage going through the transformer and
[00:35:56:610 - 00:35:57:800] **Speaker 0:** this is the equivalent to the current.
[00:36:02:000 - 00:36:06:239] **Speaker 0:** So that means we can like we do with an
[00:36:06:239 - 00:36:09:510] **Speaker 0:** electrical transformer, we can refer impedances from one side to
[00:36:09:510 - 00:36:11:090] **Speaker 0:** the other, we can do the same with inertia.
[00:36:12:360 - 00:36:14:540] **Speaker 0:** From one side of the gearbox to the other.
[00:36:15:000 - 00:36:16:520] **Speaker 0:** So what we're going to do is we're going to
[00:36:16:520 - 00:36:19:919] **Speaker 0:** say, OK, the motor inertia, we will refer that through
[00:36:19:919 - 00:36:25:360] **Speaker 0:** the gearbox, To state its effect on the output of
[00:36:25:360 - 00:36:27:889] **Speaker 0:** the gearbox side is it's referred inertia.
[00:36:28:780 - 00:36:34:169] **Speaker 0:** So Here we have the um the energy stored in
[00:36:34:169 - 00:36:37:629] **Speaker 0:** the inertia of the rotor of the motor, and we're
[00:36:37:629 - 00:36:43:010] **Speaker 0:** referring that then to the um to the Load side,
[00:36:43:020 - 00:36:45:479] **Speaker 0:** which is where we see the change in speeds.
[00:36:46:100 - 00:36:48:600] **Speaker 0:** So this is the motor speed and this is the
[00:36:48:800 - 00:36:49:699] **Speaker 0:** load speed.
[00:36:59:399 - 00:37:03:189] **Speaker 0:** So we just then throw in or rearrange this to
[00:37:03:189 - 00:37:05:129] **Speaker 0:** solve for the referred.
[00:37:06:689 - 00:37:11:090] **Speaker 0:** Motor inertia and we're given this, just rearranging this, we
[00:37:11:090 - 00:37:14:010] **Speaker 0:** end up with this expression which gives us the motor
[00:37:14:010 - 00:37:16:570] **Speaker 0:** speed squared over the load speed squared.
[00:37:18:159 - 00:37:19:639] **Speaker 0:** If we rearrange that.
[00:37:20:679 - 00:37:23:350] **Speaker 0:** That gives motor speed over load speed is equal to
[00:37:23:350 - 00:37:23:679] **Speaker 0:** N.
[00:37:25:770 - 00:37:30:760] **Speaker 0:** So this motor speed squad overload speed squad must be
[00:37:30:760 - 00:37:31:189] **Speaker 0:** in 2.
[00:37:32:929 - 00:37:34:840] **Speaker 0:** Yeah, OK, so.
[00:37:36:110 - 00:37:41:909] **Speaker 0:** The motor referred inertia is just the motor inertia multiplied
[00:37:41:909 - 00:37:43:750] **Speaker 0:** by the gearbox ratio squared.
[00:37:46:590 - 00:37:48:439] **Speaker 0:** Which it would be if it was an impedance change
[00:37:48:439 - 00:37:49:300] **Speaker 0:** through a transformer.
[00:37:56:330 - 00:37:56:860] **Speaker 0:** OK.
[00:37:59:800 - 00:38:01:060] **Speaker 0:** Angular accelerations.
[00:38:02:189 - 00:38:06:270] **Speaker 0:** So, the omega by DT, but it's the load speed
[00:38:06:270 - 00:38:07:449] **Speaker 0:** that we're looking to optimise.
[00:38:08:979 - 00:38:12:639] **Speaker 0:** So that's just equal to the the torque at the
[00:38:12:639 - 00:38:16:379] **Speaker 0:** load divided by the total inertia as seen at the
[00:38:16:379 - 00:38:16:800] **Speaker 0:** load.
[00:38:17:139 - 00:38:20:060] **Speaker 0:** So it's not only the load inertia, but the inertia
[00:38:20:060 - 00:38:23:159] **Speaker 0:** of the motor seen on the on the load side.
[00:38:25:790 - 00:38:29:429] **Speaker 0:** So J total then is just the referred motor load
[00:38:29:429 - 00:38:33:370] **Speaker 0:** and the um and the inertia of the load itself,
[00:38:33:870 - 00:38:38:979] **Speaker 0:** just substituting in what we know about the referred motor
[00:38:38:979 - 00:38:40:590] **Speaker 0:** uh inertia.
[00:38:40:909 - 00:38:43:030] **Speaker 0:** So there it is in squared times the motor inertia
[00:38:43:219 - 00:38:43:870] **Speaker 0:** plus JL.
[00:38:44:639 - 00:38:48:389] **Speaker 0:** So we substitute that into the total inertia, and we're
[00:38:48:389 - 00:38:54:790] **Speaker 0:** left with um In times The oh, yeah, from before
[00:38:54:790 - 00:38:55:449] **Speaker 0:** as well.
[00:38:55:790 - 00:38:57:790] **Speaker 0:** Don't forget we have the.
[00:38:59:060 - 00:39:02:340] **Speaker 0:** The load torque is in times the motor torque.
[00:39:02:979 - 00:39:04:820] **Speaker 0:** It's just in the opposite direction.
[00:39:14:530 - 00:39:15:870] **Speaker 0:** Its magnitude is the same.
[00:39:16:199 - 00:39:21:090] **Speaker 0:** All right, so that's substituting that for TM in here.
[00:39:22:639 - 00:39:24:889] **Speaker 0:** Uh for TL, so we've got N times TM for
[00:39:24:889 - 00:39:29:909] **Speaker 0:** TL over total uh inertia, which is N 2 JM
[00:39:29:909 - 00:39:30:600] **Speaker 0:** plus JL.
[00:39:31:979 - 00:39:34:560] **Speaker 0:** We can take out the end from the top line.
[00:39:35:320 - 00:39:38:959] **Speaker 0:** And we're left with TM over NJM plus JL over
[00:39:38:959 - 00:39:39:239] **Speaker 0:** N.
[00:39:40:100 - 00:39:40:649] **Speaker 0:** OK.
[00:39:41:889 - 00:39:42:600] **Speaker 0:** Let's plot that.
[00:39:45:719 - 00:39:51:159] **Speaker 0:** So this is the omega L by DT versus In
[00:39:51:620 - 00:39:53:560] **Speaker 0:** which is our gearbox ratio.
[00:39:59:110 - 00:40:02:610] **Speaker 0:** And this gives us a curve that looks like, well,
[00:40:03:189 - 00:40:04:770] **Speaker 0:** if it's a really, really small end.
[00:40:05:840 - 00:40:08:860] **Speaker 0:** Then JL over N is very, very large.
[00:40:11:000 - 00:40:12:760] **Speaker 0:** And for a small n this is small, so you
[00:40:12:760 - 00:40:13:610] **Speaker 0:** got a large value.
[00:40:13:679 - 00:40:16:699] **Speaker 0:** So TM over a large value goes down to zero
[00:40:16:699 - 00:40:19:479] **Speaker 0:** for very large for very small n, right?
[00:40:19:600 - 00:40:20:649] **Speaker 0:** So it starts off here.
[00:40:21:000 - 00:40:24:340] **Speaker 0:** Then for very large N, then this just becomes large.
[00:40:25:219 - 00:40:27:600] **Speaker 0:** Yeah, so you end up with something that goes.
[00:40:30:649 - 00:40:32:149] **Speaker 0:** Like this, it's a curve.
[00:40:34:469 - 00:40:35:500] **Speaker 0:** Hang on, that peaks.
[00:40:37:949 - 00:40:39:699] **Speaker 0:** So there is a maximum.
[00:40:42:500 - 00:40:45:139] **Speaker 0:** That's a maximum rate of acceleration.
[00:40:46:580 - 00:40:49:239] **Speaker 0:** Depending on a particular value.
[00:40:50:020 - 00:40:50:530] **Speaker 0:** Pop in.
[00:40:53:780 - 00:40:54:580] **Speaker 0:** In optimum.
[00:40:59:449 - 00:41:01:409] **Speaker 0:** So where is the peak of that curve?
[00:41:01:530 - 00:41:03:770] **Speaker 0:** It's where the gradient of that curve is equal to
[00:41:03:770 - 00:41:07:830] **Speaker 0:** 00 equal to 0.
[00:41:11:510 - 00:41:12:620] **Speaker 0:** OK, it's been a long day.
[00:41:14:649 - 00:41:16:870] **Speaker 0:** That is equal to 0, so.
[00:41:17:830 - 00:41:20:479] **Speaker 0:** If we've got this as a function, what do we
[00:41:20:479 - 00:41:22:610] **Speaker 0:** do to the function to find its zero gradient?
[00:41:25:139 - 00:41:27:600] **Speaker 0:** You differentiate it, find out where it's equal to 0.
[00:41:28:830 - 00:41:32:209] **Speaker 0:** Right, differentiate it is gradient, make that equal to 0.
[00:41:34:479 - 00:41:41:030] **Speaker 0:** So With respect to him.
[00:41:49:909 - 00:41:52:370] **Speaker 0:** And then make that equal to 0.
[00:41:54:120 - 00:41:55:580] **Speaker 0:** OK, don't know.
[00:41:57:350 - 00:42:00:620] **Speaker 0:** Uh, about, you know, your general observation of functions and
[00:42:00:620 - 00:42:02:000] **Speaker 0:** how easy they are to integrate.
[00:42:03:129 - 00:42:07:290] **Speaker 0:** But when you have 1 over in and then 1/1
[00:42:07:290 - 00:42:11:810] **Speaker 0:** over N, and these are additive, this is not a
[00:42:11:810 - 00:42:15:030] **Speaker 0:** particularly trivial integral, I mean differential.
[00:42:16:429 - 00:42:19:439] **Speaker 0:** OK, so, OK, what do we do then?
[00:42:19:639 - 00:42:20:770] **Speaker 0:** How do we find this?
[00:42:21:080 - 00:42:22:199] **Speaker 0:** Well, we can use a trick.
[00:42:22:610 - 00:42:25:080] **Speaker 0:** We're gonna use a nasty little trick, and that nasty
[00:42:25:080 - 00:42:27:929] **Speaker 0:** little trick is we're going to invert this curve.
[00:42:28:719 - 00:42:30:770] **Speaker 0:** So the curve is going to rather than zero go
[00:42:30:770 - 00:42:31:580] **Speaker 0:** off to infinity.
[00:42:33:919 - 00:42:38:189] **Speaker 0:** And then Does that so invert, invert the function.
[00:42:46:750 - 00:42:50:250] **Speaker 0:** The nice thing about this little trick is that.
[00:42:51:909 - 00:42:56:310] **Speaker 0:** Even with the scaling being different, the point where the
[00:42:56:310 - 00:43:00:850] **Speaker 0:** gradient is equal to zero is still exactly the same
[00:43:01:179 - 00:43:03:429] **Speaker 0:** value of gearbox ratio.
[00:43:06:300 - 00:43:11:030] **Speaker 0:** Alright, so now we are looking at doing D by
[00:43:11:030 - 00:43:11:429] **Speaker 0:** DN.
[00:43:12:610 - 00:43:15:679] **Speaker 0:** Of N times JM.
[00:43:17:070 - 00:43:19:510] **Speaker 0:** Plus JL over N.
[00:43:20:870 - 00:43:22:149] **Speaker 0:** Divided by TM.
[00:43:23:790 - 00:43:27:969] **Speaker 0:** Well, the talk at the motor is a constant here.
[00:43:28:219 - 00:43:29:949] **Speaker 0:** It just scales the whole expression.
[00:43:30:770 - 00:43:32:479] **Speaker 0:** So we don't worry about that.
[00:43:32:760 - 00:43:37:360] **Speaker 0:** So we're left with D by DN of NJM plus
[00:43:37:360 - 00:43:38:600] **Speaker 0:** JL over M.
[00:43:39:239 - 00:43:41:699] **Speaker 0:** So we've got differentiating.
[00:43:42:729 - 00:43:44:540] **Speaker 0:** JM by N is JM.
[00:43:45:860 - 00:43:49:330] **Speaker 0:** And then 1 over N is minus 1 over N2,
[00:43:49:540 - 00:43:52:780] **Speaker 0:** so minus JL over N2.
[00:43:54:649 - 00:43:55:870] **Speaker 0:** Make that equal to 0.
[00:43:57:419 - 00:43:58:219] **Speaker 0:** That's that point there.
[00:44:02:479 - 00:44:09:120] **Speaker 0:** We rearrange this, which gives us N 2 JM.
[00:44:10:250 - 00:44:12:870] **Speaker 0:** Is equal to JL.
[00:44:19:060 - 00:44:23:739] **Speaker 0:** So it's telling us that in order to maximise how
[00:44:23:739 - 00:44:27:020] **Speaker 0:** much we can the the the um acceleration that we
[00:44:27:020 - 00:44:30:679] **Speaker 0:** can achieve for our load is make the inertia.
[00:44:31:770 - 00:44:32:959] **Speaker 0:** Of our motor.
[00:44:33:719 - 00:44:36:500] **Speaker 0:** Referred to the low side appear to be equal.
[00:44:37:959 - 00:44:39:379] **Speaker 0:** To the inertia of the load.
[00:44:42:699 - 00:44:46:100] **Speaker 0:** This is a direct equivalent to an electrical situation where
[00:44:46:100 - 00:44:50:979] **Speaker 0:** you match impedances to maximise power transfer.
[00:44:52:699 - 00:44:56:149] **Speaker 0:** Alright, so, That's that's the finding is that if we
[00:44:56:149 - 00:44:58:250] **Speaker 0:** can make the referred.
[00:44:58:969 - 00:45:02:290] **Speaker 0:** Inertia of our motor equal to that of the of
[00:45:02:290 - 00:45:06:409] **Speaker 0:** the load, then we can optimise the acceleration of their
[00:45:06:409 - 00:45:06:909] **Speaker 0:** load.
[00:45:14:620 - 00:45:14:629] **Speaker 0:** Right.
[00:45:17:139 - 00:45:17:620] **Speaker 0:** All good?
[00:45:18:729 - 00:45:19:250] **Speaker 0:** OK.
[00:45:23:959 - 00:45:26:840] **Speaker 0:** So we've got we've got a pretty effective way of
[00:45:26:840 - 00:45:29:080] **Speaker 0:** being able to achieve that optimisation.
[00:45:30:439 - 00:45:33:649] **Speaker 0:** OK, so now we're just quickly moving on to having
[00:45:33:649 - 00:45:34:810] **Speaker 0:** or considering.
[00:45:35:600 - 00:45:36:250] **Speaker 0:** I will be.
[00:45:37:209 - 00:45:38:370] **Speaker 0:** I'll be quite quick with all of this.
[00:45:39:770 - 00:45:44:649] **Speaker 0:** Is where we might have a um a rotational system
[00:45:44:649 - 00:45:47:280] **Speaker 0:** so we've got a motor which is rotating a pulley,
[00:45:47:489 - 00:45:50:889] **Speaker 0:** but now our load is moving in a linear direction.
[00:45:51:899 - 00:45:54:179] **Speaker 0:** So how do we match this up to what we
[00:45:54:179 - 00:45:57:699] **Speaker 0:** just had before, which was a rotational rotational system.
[00:45:57:780 - 00:45:59:899] **Speaker 0:** So rotational motor, rotational load.
[00:46:01:590 - 00:46:02:050] **Speaker 0:** Well.
[00:46:03:860 - 00:46:06:580] **Speaker 0:** What is the effect of inertia then for this mass
[00:46:06:580 - 00:46:10:540] **Speaker 0:** if we were to refer that back through the rotational,
[00:46:10:959 - 00:46:11:760] **Speaker 0:** the pulley here?
[00:46:13:580 - 00:46:16:120] **Speaker 0:** Well, we've just got conservation of energy at play.
[00:46:16:530 - 00:46:20:459] **Speaker 0:** So whatever we have is rotational energy must equal what
[00:46:20:459 - 00:46:24:260] **Speaker 0:** we rotational energy must equal what we have in linear
[00:46:24:260 - 00:46:24:479] **Speaker 0:** energy.
[00:46:25:300 - 00:46:25:310] **Speaker 0:** Right.
[00:46:26:100 - 00:46:29:379] **Speaker 0:** And here, the speed that this is travelling is just
[00:46:29:379 - 00:46:33:669] **Speaker 0:** equal to omega times the radius of our pulley.
[00:46:34:020 - 00:46:35:159] **Speaker 0:** That's that's the.
[00:46:36:020 - 00:46:38:760] **Speaker 0:** equivalent, it's not identical, but it's kind of the equivalent
[00:46:38:760 - 00:46:40:659] **Speaker 0:** of our gearbox in the state.
[00:46:41:500 - 00:46:46:060] **Speaker 0:** The radius distance defines the ratio of speeds.
[00:46:49:229 - 00:46:54:300] **Speaker 0:** So kinetic energy And rotational.
[00:46:57:010 - 00:46:58:469] **Speaker 0:** You should really put energy there.
[00:47:03:300 - 00:47:08:409] **Speaker 0:** So what we have is Uh, with this, with this
[00:47:08:409 - 00:47:12:649] **Speaker 0:** understanding is that the um load inertia is just equal
[00:47:12:649 - 00:47:15:649] **Speaker 0:** to the mass that we have here times the radius
[00:47:15:649 - 00:47:16:270] **Speaker 0:** squared.
[00:47:17:939 - 00:47:18:060] **Speaker 0:** Right.
[00:47:18:139 - 00:47:20:580] **Speaker 0:** So that's how we do our conversion back to the
[00:47:20:580 - 00:47:21:870] **Speaker 0:** rotational domain.
[00:47:22:379 - 00:47:26:179] **Speaker 0:** So we can have an expression for that effective rotational
[00:47:26:179 - 00:47:29:020] **Speaker 0:** inertia by moving something along a conveyor.
[00:47:32:429 - 00:47:33:820] **Speaker 0:** Just by conservation of energy.
[00:47:37:879 - 00:47:41:360] **Speaker 0:** An application of that could be uh this example, which
[00:47:41:360 - 00:47:43:439] **Speaker 0:** I've actually left to do for homework, not we're not
[00:47:43:439 - 00:47:44:209] **Speaker 0:** doing that now.
[00:47:44:879 - 00:47:47:330] **Speaker 0:** So we're at a mass throwing competition.
[00:47:47:719 - 00:47:50:159] **Speaker 0:** We've got an electromechanical system just showing here.
[00:47:50:239 - 00:47:52:520] **Speaker 0:** So it's a motor with a throwing arm, and you
[00:47:52:520 - 00:47:54:719] **Speaker 0:** want it to be able to throw that mass as
[00:47:54:719 - 00:47:58:600] **Speaker 0:** far as absolutely possible, which means if you get the
[00:47:58:600 - 00:48:01:979] **Speaker 0:** release trajectory right, what you're trying to do, of course,
[00:48:02:080 - 00:48:06:939] **Speaker 0:** is maximise the acceleration of that within a particular angle.
[00:48:08:550 - 00:48:11:550] **Speaker 0:** Alright, so the mass is 500 grammes and the motor
[00:48:11:550 - 00:48:15:590] **Speaker 0:** rotational inertia is 0.2 kilogrammes per metre squared, which includes
[00:48:15:590 - 00:48:17:270] **Speaker 0:** the throwing arm inertia.
[00:48:18:449 - 00:48:19:550] **Speaker 0:** How long should the arm be?
[00:48:20:489 - 00:48:24:689] **Speaker 0:** Well, all of those that conveyor expression that example that
[00:48:24:689 - 00:48:27:129] **Speaker 0:** I just showed before is exactly what we've got here.
[00:48:27:449 - 00:48:31:090] **Speaker 0:** You're just trying to maximise the speed you by the
[00:48:31:090 - 00:48:32:989] **Speaker 0:** time that it gets to release.
[00:48:34:239 - 00:48:39:149] **Speaker 0:** Um So If you go through the exercise, you'll find
[00:48:39:149 - 00:48:42:429] **Speaker 0:** that the answer is that the radius.
[00:48:43:820 - 00:48:47:610] **Speaker 0:** Which is your throwing arm length, is equal to 0.63
[00:48:48:030 - 00:48:48:550] **Speaker 0:** metres.
[00:48:51:149 - 00:48:52:610] **Speaker 0:** Right, 630 millimetres.
[00:48:55:959 - 00:48:57:770] **Speaker 0:** I will put up the fully work solution just in
[00:48:57:770 - 00:49:00:090] **Speaker 0:** case you're not interested in having a look at solving
[00:49:00:090 - 00:49:02:090] **Speaker 0:** it yourself, but if you want to have a have
[00:49:02:090 - 00:49:04:250] **Speaker 0:** a go at it, come up with that number, you
[00:49:04:250 - 00:49:05:030] **Speaker 0:** can have a try.
[00:49:09:610 - 00:49:13:060] **Speaker 0:** Just to finish off, I did just want to show
[00:49:13:060 - 00:49:16:419] **Speaker 0:** that What motor you choose for a particular application.
[00:49:16:510 - 00:49:19:770] **Speaker 0:** There are actually a lot of different types of motor.
[00:49:20:729 - 00:49:23:860] **Speaker 0:** That you potentially could look at choosing um.
[00:49:25:250 - 00:49:28:209] **Speaker 0:** For the solar car we've got a permanent magnet DC
[00:49:28:209 - 00:49:30:060] **Speaker 0:** motor that's commutated.
[00:49:31:000 - 00:49:34:600] **Speaker 0:** Um, for a lot of electric vehicles, we have sine
[00:49:34:600 - 00:49:39:120] **Speaker 0:** wave synchronous machines for your drones and aircraft, which are
[00:49:39:120 - 00:49:41:820] **Speaker 0:** powered by electric motors, you tend to use brushless DC,
[00:49:42:239 - 00:49:46:760] **Speaker 0:** which are technically AC machines, by the way, the DC
[00:49:46:760 - 00:49:48:000] **Speaker 0:** part there is a bit of a misnomer.
[00:49:48:750 - 00:49:53:929] **Speaker 0:** Um, And an industry by far and away the most
[00:49:53:929 - 00:49:57:330] **Speaker 0:** common motor you find are asynchronous induction machines that are
[00:49:57:330 - 00:49:58:169] **Speaker 0:** squirrel cage.
[00:49:59:010 - 00:50:01:729] **Speaker 0:** And there were even a couple of EV manufacturers that
[00:50:01:729 - 00:50:04:750] **Speaker 0:** were initially starting out by using induction machines as well,
[00:50:04:850 - 00:50:06:909] **Speaker 0:** because they don't need any kind of permanent magnet.
[00:50:07:129 - 00:50:09:469] **Speaker 0:** No special materials involved.
[00:50:11:530 - 00:50:14:489] **Speaker 0:** Right, the last couple of slides we're just showing you
[00:50:14:489 - 00:50:17:689] **Speaker 0:** a whole bunch of different things that you might have
[00:50:17:689 - 00:50:21:169] **Speaker 0:** to consider when choosing a motor for an application that
[00:50:21:169 - 00:50:25:250] **Speaker 0:** goes beyond the obvious things to do with standards, things
[00:50:25:250 - 00:50:29:189] **Speaker 0:** to do with how programmable it is, uh.
[00:50:30:120 - 00:50:33:979] **Speaker 0:** What are the warranty requirements for the for the engineering
[00:50:34:030 - 00:50:36:820] **Speaker 0:** application and maybe even does it come with any spears.
[00:50:39:050 - 00:50:39:949] **Speaker 0:** That's it for this.

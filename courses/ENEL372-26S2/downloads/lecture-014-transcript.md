# ENEL372-26S2 Lecture 14 native Echo transcript

Date: August 13, 2026 3:00pm-3:55pm
Transcript type: native Echo automated transcript.

[00:00:00:970 - 00:00:02:289] **Speaker 0:** Alright, Kyorakoto.
[00:00:02:410 - 00:00:03:329] **Speaker 0:** Welcome along.
[00:00:03:890 - 00:00:07:449] **Speaker 0:** We're in this room which has incredibly loud acoustics as
[00:00:07:449 - 00:00:10:970] **Speaker 0:** usual, um, right, so, um.
[00:00:12:380 - 00:00:15:000] **Speaker 0:** Great to see a lot of you at the, uh,
[00:00:15:090 - 00:00:16:899] **Speaker 0:** the drop and help session yesterday.
[00:00:17:059 - 00:00:21:010] **Speaker 0:** Apologies for, um, the, the time that it took to,
[00:00:21:100 - 00:00:23:059] **Speaker 0:** to address some people's questions, with their hands being up
[00:00:23:059 - 00:00:23:979] **Speaker 0:** in the air for a long time.
[00:00:24:180 - 00:00:26:700] **Speaker 0:** One of our TAs that should have been there was,
[00:00:26:780 - 00:00:28:340] **Speaker 0:** was ill, uh, yesterday.
[00:00:28:500 - 00:00:30:219] **Speaker 0:** Um, there'll be more people there.
[00:00:30:575 - 00:00:33:415] **Speaker 0:** Um, in, in subsequent, um, sessions.
[00:00:33:665 - 00:00:36:465] **Speaker 0:** Although I can't guarantee how many TAs we'll have at
[00:00:36:465 - 00:00:41:345] **Speaker 0:** the LT, uh, Spice help session this Friday, that's tomorrow.
[00:00:41:544 - 00:00:42:145] **Speaker 0:** I'll be there.
[00:00:42:314 - 00:00:45:185] **Speaker 0:** Um, we've got Chris Hahn will be there as well,
[00:00:45:224 - 00:00:47:985] **Speaker 0:** plus a, a TA or two that'll be there for
[00:00:47:985 - 00:00:48:244] **Speaker 0:** help.
[00:00:48:750 - 00:00:51:700] **Speaker 0:** Um, I'm also going to put up, um, a little,
[00:00:51:790 - 00:00:56:150] **Speaker 0:** um, I, I guess, uh, starting help for the, for
[00:00:56:150 - 00:00:59:029] **Speaker 0:** the, uh, project to, uh, for the simulation part, you
[00:00:59:029 - 00:01:01:270] **Speaker 0:** know, maybe what components that you can get from the
[00:01:01:270 - 00:01:04:830] **Speaker 0:** library that are stand-ins for the ones that aren't there
[00:01:04:830 - 00:01:07:330] **Speaker 0:** that, that we're actually using on the, on the, um,
[00:01:07:910 - 00:01:08:650] **Speaker 0:** on the project.
[00:01:09:349 - 00:01:10:830] **Speaker 0:** OK, just to help out a little bit with that.
[00:01:12:330 - 00:01:15:889] **Speaker 0:** Right, uh, so for today, um, we're going to kind
[00:01:15:889 - 00:01:19:709] **Speaker 0:** of jump in and start looking at what we might,
[00:01:19:889 - 00:01:24:410] **Speaker 0:** um, do if for the design of a closed loop
[00:01:24:410 - 00:01:28:690] **Speaker 0:** control system for our motor driving and mechanical load situation.
[00:01:29:279 - 00:01:32:599] **Speaker 0:** Because it's very rare that you would have a situation
[00:01:32:599 - 00:01:35:440] **Speaker 0:** where you have a motor and you, you've got your
[00:01:35:440 - 00:01:37:309] **Speaker 0:** power going into your motor and you've got your load,
[00:01:37:599 - 00:01:42:120] **Speaker 0:** and there isn't some form of feedback to either control
[00:01:42:120 - 00:01:44:639] **Speaker 0:** the amount of torque that's being produced or maybe the
[00:01:44:639 - 00:01:48:120] **Speaker 0:** speed of what's happening in the load, um, and even
[00:01:48:120 - 00:01:51:919] **Speaker 0:** potentially, depending on the application, exactly what position that that
[00:01:51:919 - 00:01:54:000] **Speaker 0:** load is being operated to.
[00:01:54:660 - 00:01:57:400] **Speaker 0:** Right, so that's the crux of what we're going over,
[00:01:57:459 - 00:01:59:360] **Speaker 0:** um, going to be going over today.
[00:02:00:379 - 00:02:03:250] **Speaker 0:** Um, so it's essential that the system's under some form
[00:02:03:250 - 00:02:06:080] **Speaker 0:** of control, usually feedback-based, um.
[00:02:07:040 - 00:02:10:800] **Speaker 0:** We, we then have output parameters that I've just mentioned,
[00:02:10:809 - 00:02:16:000] **Speaker 0:** like torque and quite fortunately for us, uh, looking at
[00:02:16:000 - 00:02:19:880] **Speaker 0:** controlling the torque, torque is directly proportional to current, so
[00:02:19:880 - 00:02:22:509] **Speaker 0:** when we're looking at the measurements that we're making, um,
[00:02:22:559 - 00:02:25:220] **Speaker 0:** it's, it's a very simple task then to just measure
[00:02:25:220 - 00:02:28:000] **Speaker 0:** the current as a substitute for torque.
[00:02:29:110 - 00:02:34:229] **Speaker 0:** Um, speed, OK, we'll need some sort of shaft or
[00:02:34:229 - 00:02:36:130] **Speaker 0:** encoder to look at speed.
[00:02:36:429 - 00:02:37:270] **Speaker 0:** Same with position.
[00:02:37:940 - 00:02:41:580] **Speaker 0:** Um, and you compare against that, uh, against those parameters
[00:02:41:580 - 00:02:44:740] **Speaker 0:** that, um, we, we, we desire to have.
[00:02:45:100 - 00:02:49:619] **Speaker 0:** So, We're comparing against the desired, uh, or the, the
[00:02:49:619 - 00:02:53:860] **Speaker 0:** actual measured values, right, um, as feedback variables, so this
[00:02:53:860 - 00:02:54:759] **Speaker 0:** is what we measure.
[00:02:56:779 - 00:02:58:529] **Speaker 0:** And compare against desired values.
[00:02:58:770 - 00:03:02:139] **Speaker 0:** OK, so it's that would be what we're ordering.
[00:03:06:399 - 00:03:09:460] **Speaker 0:** I'm gonna be, um, try, I'm gonna try to be
[00:03:09:460 - 00:03:11:320] **Speaker 0:** a little more precise with my handwriting.
[00:03:11:399 - 00:03:13:160] **Speaker 0:** I've been, it's been indicated that it can be a
[00:03:13:160 - 00:03:14:720] **Speaker 0:** little difficult to follow at times.
[00:03:15:080 - 00:03:15:899] **Speaker 0:** My apologies.
[00:03:16:399 - 00:03:19:380] **Speaker 0:** Um, right, it's the difference then or the what we
[00:03:19:380 - 00:03:22:119] **Speaker 0:** define as being the error, uh, between the actual output
[00:03:22:119 - 00:03:25:300] **Speaker 0:** and the desired or reference values that can be amplified
[00:03:25:720 - 00:03:30:520] **Speaker 0:** and then utilised to, um, give us a, um, an
[00:03:30:520 - 00:03:33:940] **Speaker 0:** output that, um, is changed to minimise that error.
[00:03:35:169 - 00:03:39:160] **Speaker 0:** Right, so if we do this job well, um, this
[00:03:39:160 - 00:03:43:490] **Speaker 0:** feedback control, then you're going to make that error acceptably
[00:03:43:490 - 00:03:43:869] **Speaker 0:** small.
[00:03:44:559 - 00:03:46:500] **Speaker 0:** It's never going to be 0.
[00:03:47:190 - 00:03:51:949] **Speaker 0:** Um, acceptable is all context-based, right?
[00:03:52:110 - 00:03:56:509] **Speaker 0:** So, how, how, um, far away from, um, being zero
[00:03:56:509 - 00:04:00:729] **Speaker 0:** error is allowable will be very much at the, um,
[00:04:00:750 - 00:04:02:630] **Speaker 0:** in, within the context of the application.
[00:04:03:539 - 00:04:06:500] **Speaker 0:** But you do want it to be robust against disturbances,
[00:04:06:990 - 00:04:09:869] **Speaker 0:** so the sort of disturbances that you have, naturally enough
[00:04:09:869 - 00:04:14:130] **Speaker 0:** is noise, um, And, and other variations caused by parts
[00:04:14:130 - 00:04:17:950] **Speaker 0:** of the system, uh, or major changes that could be,
[00:04:18:178 - 00:04:21:489] **Speaker 0:** they're not noise because they could be expected changes, but
[00:04:21:489 - 00:04:24:450] **Speaker 0:** they are, uh, major changes, so maybe change in the
[00:04:24:450 - 00:04:28:309] **Speaker 0:** load, a mechanical load or perhaps, um, even looking at
[00:04:28:500 - 00:04:32:209] **Speaker 0:** a, a, a big change in what you're requiring to,
[00:04:32:250 - 00:04:35:010] **Speaker 0:** uh, as, as an ordered value for the, for the
[00:04:35:010 - 00:04:37:410] **Speaker 0:** system, like here, it just is an example of step
[00:04:37:410 - 00:04:38:690] **Speaker 0:** change in reference speed.
[00:04:39:420 - 00:04:41:869] **Speaker 0:** That the, the control system then has to try and
[00:04:41:869 - 00:04:43:709] **Speaker 0:** make that error approach 0.
[00:04:45:140 - 00:04:51:470] **Speaker 0:** Right So When we're talking about a power electronic system
[00:04:51:470 - 00:04:55:929] **Speaker 0:** that uh is driving an electric motor, um, that's connected
[00:04:55:929 - 00:05:00:750] **Speaker 0:** to a mechanical load, then what we often employ is
[00:05:01:049 - 00:05:05:070] **Speaker 0:** a type of embedded feedback control system.
[00:05:06:100 - 00:05:10:640] **Speaker 0:** Which utilises depending on what we need to control multiple
[00:05:10:640 - 00:05:15:059] **Speaker 0:** uh well those parameters that we are trying to control
[00:05:15:059 - 00:05:16:940] **Speaker 0:** like the torque, the speed, and the position.
[00:05:17:829 - 00:05:22:579] **Speaker 0:** Obviously, depending on application, we don't necessarily always have to
[00:05:22:579 - 00:05:25:329] **Speaker 0:** control speed or always have to control position.
[00:05:26:059 - 00:05:29:059] **Speaker 0:** But predominantly we do with the min at the minimum
[00:05:29:059 - 00:05:30:980] **Speaker 0:** we'd be looking to control torque.
[00:05:34:320 - 00:05:38:559] **Speaker 0:** So, embedded control system, kind of in block diagram form
[00:05:38:559 - 00:05:39:540] **Speaker 0:** would look like this.
[00:05:43:369 - 00:05:45:690] **Speaker 0:** So I'm gonna kinda step through this to uh give
[00:05:45:690 - 00:05:49:369] **Speaker 0:** you an indication of, of how things are, um, operating.
[00:05:49:609 - 00:05:52:970] **Speaker 0:** So, good place to start to understand what's going on
[00:05:52:970 - 00:05:55:570] **Speaker 0:** here is just looking at the job that we're trying
[00:05:55:570 - 00:05:58:809] **Speaker 0:** to do, which is the electrical system, which will be
[00:05:58:809 - 00:05:59:959] **Speaker 0:** your power electronics.
[00:06:00:709 - 00:06:13:470] **Speaker 0:** And the motor Uh, that is coupled to the mechanical
[00:06:13:470 - 00:06:13:899] **Speaker 0:** system.
[00:06:14:149 - 00:06:18:250] **Speaker 0:** So the mechanical system, this will have the, the gearbox
[00:06:18:250 - 00:06:19:790] **Speaker 0:** and the mechanical load.
[00:06:35:959 - 00:06:39:899] **Speaker 1:** Right, so, if we're controlling torque, we've got to measure
[00:06:40:160 - 00:06:42:880] **Speaker 0:** what the output of the, the, uh, the motor is
[00:06:42:880 - 00:06:45:640] **Speaker 0:** doing, uh regarding uh torque.
[00:06:46:540 - 00:06:49:420] **Speaker 0:** Luckily for us, as I just mentioned, given that torque
[00:06:49:420 - 00:06:52:899] **Speaker 0:** is directly proportional to the current flowing the motor, we
[00:06:52:899 - 00:06:56:739] **Speaker 0:** can actually just sense the current and then we are
[00:06:56:739 - 00:07:00:649] **Speaker 0:** comparing that to an ordered value of torque.
[00:07:00:859 - 00:07:04:700] **Speaker 0:** So wherever you see in this diagram, the asterisk there
[00:07:04:700 - 00:07:08:100] **Speaker 0:** for the, for the parameter, that is the ordered value.
[00:07:14:670 - 00:07:15:820] **Speaker 0:** So this is measured.
[00:07:21:019 - 00:07:24:250] **Speaker 1:** Alright, you, you compare those two, what, what we're measuring
[00:07:24:250 - 00:07:26:739] **Speaker 0:** and what we've ordered, which will give you an output
[00:07:26:739 - 00:07:27:679] **Speaker 0:** which is an error.
[00:07:28:500 - 00:07:30:559] **Speaker 0:** It's the difference between those two.
[00:07:32:429 - 00:07:35:709] **Speaker 0:** And we use that error to feed into a, in
[00:07:35:709 - 00:07:38:250] **Speaker 0:** this case, a torque controller.
[00:07:39:529 - 00:07:43:489] **Speaker 0:** Alright, so the torque controller takes the error and uses
[00:07:43:489 - 00:07:48:100] **Speaker 0:** that signal to give us an output which drives the
[00:07:48:100 - 00:07:50:700] **Speaker 0:** electrical system to provide the torque that we need.
[00:07:55:160 - 00:07:56:519] **Speaker 0:** Right, so that's the inner loop.
[00:07:56:920 - 00:07:59:779] **Speaker 0:** That's the first feedback control loop that we would have.
[00:08:00:910 - 00:08:05:179] **Speaker 0:** But of course, the next step is, well, maybe we
[00:08:05:179 - 00:08:08:040] **Speaker 0:** want to also employ some speed control.
[00:08:08:500 - 00:08:12:690] **Speaker 0:** So we need some sort of sensing or sensor um
[00:08:12:690 - 00:08:15:299] **Speaker 0:** on the mechanical system that looks at what is the
[00:08:15:299 - 00:08:18:899] **Speaker 0:** rotational speed within the mechanical system, so that's after the
[00:08:18:899 - 00:08:21:750] **Speaker 0:** gearbox is, is, uh, utilised.
[00:08:22:260 - 00:08:24:309] **Speaker 0:** So this of course is our measured speed.
[00:08:24:540 - 00:08:27:940] **Speaker 0:** We compare that to our ordered speed, so the speed
[00:08:27:940 - 00:08:28:679] **Speaker 0:** that we want.
[00:08:29:290 - 00:08:31:029] **Speaker 0:** And feed the error.
[00:08:31:820 - 00:08:33:840] **Speaker 0:** Into our speed controller.
[00:08:34:590 - 00:08:35:849] **Speaker 0:** So there's another controller.
[00:08:37:179 - 00:08:38:359] **Speaker 0:** Since it's embedded.
[00:08:39:169 - 00:08:43:440] **Speaker 0:** The output of the speed controller actually provides the parameter
[00:08:43:440 - 00:08:47:929] **Speaker 0:** value of our ordered torque that drives the mechanical system
[00:08:47:929 - 00:08:50:289] **Speaker 0:** to provide the speed that we want.
[00:08:51:179 - 00:08:53:849] **Speaker 0:** So it, it, the speed controller gives us the torque
[00:08:53:849 - 00:08:57:479] **Speaker 0:** ordered torque value, the ordered torque value, you still measure
[00:08:57:479 - 00:08:59:940] **Speaker 0:** the current, so you're trying to drive that error to
[00:08:59:940 - 00:09:04:340] **Speaker 0:** zero, it goes into the torque controller, so the torque
[00:09:04:820 - 00:09:08:500] **Speaker 0:** is achieved to drive back to zero, which also means
[00:09:08:500 - 00:09:12:520] **Speaker 0:** that you are uh creating the right conditions for speed
[00:09:12:700 - 00:09:14:400] **Speaker 0:** to drive that error to zero.
[00:09:18:580 - 00:09:22:340] **Speaker 0:** All right, finally, you've got the, the situation where you
[00:09:22:340 - 00:09:25:260] **Speaker 0:** may need to um control for position.
[00:09:26:510 - 00:09:33:549] **Speaker 0:** All right, so, um, I'll be stopping and explaining exactly
[00:09:33:549 - 00:09:36:750] **Speaker 0:** why you take the one over S, where S is
[00:09:36:750 - 00:09:39:539] **Speaker 0:** your complex uh frequency, right?
[00:09:39:640 - 00:09:41:539] **Speaker 0:** So why you need that for position.
[00:09:41:630 - 00:09:44:250] **Speaker 0:** Basically, it's performing an integration.
[00:09:44:669 - 00:09:47:219] **Speaker 0:** So you integrate your speed and you end up with
[00:09:47:219 - 00:09:47:750] **Speaker 0:** position.
[00:09:49:710 - 00:09:52:950] **Speaker 0:** Right, so you have your position, which is measured, again,
[00:09:53:190 - 00:09:55:729] **Speaker 0:** um, a, a rotary encoder of some sort.
[00:09:56:880 - 00:10:00:309] **Speaker 0:** Um, you then compare that to an ordered position.
[00:10:00:979 - 00:10:05:299] **Speaker 0:** And that drives the error and the error feeds into
[00:10:05:299 - 00:10:06:539] **Speaker 0:** your position controller.
[00:10:08:219 - 00:10:12:530] **Speaker 0:** Which has an output that is effectively your ordered speed,
[00:10:13:070 - 00:10:17:190] **Speaker 0:** OK, so, uh, that ordered speed, again you have to
[00:10:17:190 - 00:10:20:900] **Speaker 0:** do your internal, uh, your next loop in driving that
[00:10:20:900 - 00:10:26:150] **Speaker 0:** error to zero that outputs your torque, um, requirement again
[00:10:26:150 - 00:10:29:109] **Speaker 0:** measured and driving that error to zero, but it provides
[00:10:29:109 - 00:10:32:229] **Speaker 0:** the torque that gives you the right speed that then
[00:10:32:229 - 00:10:35:229] **Speaker 0:** gives you the right overall position.
[00:10:40:229 - 00:10:44:130] **Speaker 1:** OK, so, What we find though is that the power
[00:10:44:130 - 00:10:48:369] **Speaker 0:** electronic system is the the only way that this embedded
[00:10:48:369 - 00:10:51:010] **Speaker 0:** kind of system works is because of the different time
[00:10:51:010 - 00:10:54:250] **Speaker 0:** constants associated with the different feedback loops.
[00:10:55:580 - 00:10:58:770] **Speaker 0:** They have very, very different um speeds involved.
[00:11:00:090 - 00:11:01:130] **Speaker 0:** With the, with the feedback.
[00:11:01:250 - 00:11:05:719] **Speaker 0:** So, the power electronic system um is capable of changing
[00:11:05:719 - 00:11:08:150] **Speaker 0:** its output electrical state extremely quickly.
[00:11:10:020 - 00:11:13:450] **Speaker 0:** So it's, it's actually possible to make very, very rapid,
[00:11:13:710 - 00:11:17:099] **Speaker 0:** um, current and therefore torque changes.
[00:11:17:349 - 00:11:18:690] **Speaker 0:** We can do this quickly.
[00:11:19:750 - 00:11:21:080] **Speaker 0:** So this inner loop.
[00:11:22:340 - 00:11:24:549] **Speaker 0:** Feedback loop is, is fast.
[00:11:34:890 - 00:11:38:330] **Speaker 0:** Right, so, taking the next step out, if we're looking
[00:11:38:330 - 00:11:39:890] **Speaker 0:** about controlling speed.
[00:11:40:669 - 00:11:43:619] **Speaker 0:** And we are adjusting torque to control speed.
[00:11:43:869 - 00:11:49:270] **Speaker 0:** There is that, that um element of inertia that slows
[00:11:49:270 - 00:11:51:510] **Speaker 0:** down the rate of acceleration.
[00:11:52:559 - 00:11:56:219] **Speaker 0:** Right, so being able to change the speed of our,
[00:11:56:349 - 00:11:59:599] **Speaker 0:** our load is something that happens much more slowly than
[00:11:59:599 - 00:12:02:739] **Speaker 0:** we can change the rate or, or change the torque
[00:12:02:739 - 00:12:06:799] **Speaker 0:** that's driving the acceleration to reach certain speeds.
[00:12:07:780 - 00:12:11:219] **Speaker 0:** Right, so the out this um speed control loop is
[00:12:11:219 - 00:12:12:320] **Speaker 0:** actually slower.
[00:12:22:049 - 00:12:26:090] **Speaker 0:** And then finally the, the, the last um outer loop,
[00:12:26:169 - 00:12:27:510] **Speaker 0:** the position control.
[00:12:27:890 - 00:12:30:530] **Speaker 0:** OK, you can imagine, right, you've got a system where
[00:12:30:530 - 00:12:33:630] **Speaker 0:** you're telling the torque on the motor to drive the,
[00:12:33:799 - 00:12:37:440] **Speaker 0:** the um the mechanical load at a certain speed, and
[00:12:37:440 - 00:12:39:599] **Speaker 0:** then it's approaching the right position, it's got to slow
[00:12:39:599 - 00:12:42:270] **Speaker 0:** down to get to that position and then stop.
[00:12:43:559 - 00:12:47:000] **Speaker 0:** Right, so the fact that you're, that you're already having
[00:12:47:000 - 00:12:49:760] **Speaker 0:** to deal with the inertia and then you're, you, you're
[00:12:49:760 - 00:12:51:960] **Speaker 0:** reaching that position and slowing down, maybe a little bit
[00:12:51:960 - 00:12:55:880] **Speaker 0:** overshoot and come back, that takes a lot more time
[00:12:55:880 - 00:12:56:340] **Speaker 0:** again.
[00:12:56:679 - 00:12:58:419] **Speaker 0:** So the outer loop is very slow.
[00:13:13:809 - 00:13:18:409] **Speaker 0:** And as such, with every loop that you have um
[00:13:18:409 - 00:13:21:369] **Speaker 0:** outside of an inside one, everything that happens inside there
[00:13:21:369 - 00:13:26:849] **Speaker 0:** is happening so fast that that control loop can't um
[00:13:26:849 - 00:13:29:289] **Speaker 0:** adjust or react to that.
[00:13:29:690 - 00:13:32:849] **Speaker 0:** So everything that's happening here as far as the, the
[00:13:32:849 - 00:13:37:650] **Speaker 0:** control loop is concerned, it seems to be um completely
[00:13:37:650 - 00:13:38:830] **Speaker 0:** instantaneous.
[00:13:39:280 - 00:13:41:869] **Speaker 0:** Alright, and the same with the, with the outer loop
[00:13:41:869 - 00:13:42:039] **Speaker 0:** again.
[00:13:42:130 - 00:13:45:239] **Speaker 0:** Anything that's happening in here, um, is something that it
[00:13:45:239 - 00:13:46:349] **Speaker 0:** cannot react to.
[00:13:46:520 - 00:13:49:760] **Speaker 0:** It sees that as being non-dynamically changing.
[00:13:53:780 - 00:13:56:530] **Speaker 0:** Which is quite important when we start to actually um
[00:13:57:070 - 00:13:58:869] **Speaker 0:** design our, our control systems.
[00:14:01:049 - 00:14:07:380] **Speaker 1:** Now, control of motors for mechanical loads um can be
[00:14:07:380 - 00:14:09:679] **Speaker 0:** quite the substantial subject area.
[00:14:10:059 - 00:14:13:219] **Speaker 0:** Um, we've got a limited time, so we're going to
[00:14:13:219 - 00:14:19:650] **Speaker 0:** be um Gaining our understanding by going through effectively an
[00:14:19:650 - 00:14:21:489] **Speaker 0:** example application.
[00:14:21:690 - 00:14:25:869] **Speaker 0:** And that example is using um a brushed DC motor
[00:14:26:039 - 00:14:29:869] **Speaker 0:** to drive uh a mechanical load that is being powered
[00:14:30:130 - 00:14:34:770] **Speaker 0:** via a buck converter power electronic system, right.
[00:14:41:460 - 00:14:45:919] **Speaker 0:** So, we're going to be aiming to have um reasonable
[00:14:45:919 - 00:14:48:419] **Speaker 0:** feedback control for torque, speed and position.
[00:14:48:710 - 00:14:50:320] **Speaker 0:** So what do we mean by reasonable?
[00:14:50:469 - 00:14:53:979] **Speaker 0:** Well, it's reasonable to the extent that it does its
[00:14:53:979 - 00:14:59:219] **Speaker 0:** job uh sufficiently well, and I'll be identify what we
[00:14:59:219 - 00:15:01:080] **Speaker 0:** mean by that, um, coming up.
[00:15:01:700 - 00:15:03:900] **Speaker 0:** Well, in order to do that job though, um, we
[00:15:03:900 - 00:15:05:520] **Speaker 0:** have to understand mechanical load.
[00:15:06:520 - 00:15:08:369] **Speaker 0:** So that's the thing, doing the practical job.
[00:15:19:489 - 00:15:23:440] **Speaker 0:** Um, and we would look to optimise the, the gear
[00:15:23:440 - 00:15:26:479] **Speaker 0:** ratio to make it so that we can accelerate the,
[00:15:26:489 - 00:15:29:950] **Speaker 0:** uh, the load as, as optimally as possible, um.
[00:15:31:179 - 00:15:33:340] **Speaker 0:** We've covered that in the last lecture, how you would
[00:15:33:340 - 00:15:34:340] **Speaker 0:** go about doing that.
[00:15:36:559 - 00:15:38:359] **Speaker 0:** Um, we need to understand the motor.
[00:15:39:890 - 00:15:42:369] **Speaker 0:** Um, how it behaves under changing loads.
[00:15:55:979 - 00:16:00:059] **Speaker 0:** Um OK, it's decided to shut down.
[00:16:00:380 - 00:16:02:719] **Speaker 0:** Understand the power of electronics.
[00:16:14:049 - 00:16:16:690] **Speaker 0:** Just in case it's the side that with the Echo
[00:16:16:690 - 00:16:18:780] **Speaker 0:** 360 recording that that shut down.
[00:16:22:559 - 00:16:23:140] **Speaker 0:** OK.
[00:16:24:049 - 00:16:27:039] **Speaker 0:** Uh, understanding the power electronics, um, the fact that we're
[00:16:27:039 - 00:16:30:359] **Speaker 0:** using a but converter, uh, we've gone through that a
[00:16:30:359 - 00:16:32:919] **Speaker 0:** number of times now, and that's the reason I'm, I'm
[00:16:32:919 - 00:16:35:719] **Speaker 0:** focusing on utilising that as the power electronic converter so
[00:16:35:719 - 00:16:39:719] **Speaker 0:** that we don't have to stretch, um, our understanding for
[00:16:39:719 - 00:16:40:739] **Speaker 0:** something brand new.
[00:16:43:000 - 00:16:45:650] **Speaker 0:** Um, what we're going to find is the back converter
[00:16:45:650 - 00:16:49:750] **Speaker 0:** is pretty easily addressed with the control system.
[00:17:04:209 - 00:17:07:209] **Speaker 0:** Um, but if we were to move to other converters,
[00:17:07:319 - 00:17:09:938] **Speaker 0:** it could be a bit of a more complex control
[00:17:09:938 - 00:17:10:209] **Speaker 0:** situation.
[00:17:29:709 - 00:17:31:989] **Speaker 0:** Um, and achieve adequate control.
[00:17:32:229 - 00:17:34:869] **Speaker 0:** Um, so we're not going to be, uh, taking this
[00:17:34:869 - 00:17:40:630] **Speaker 0:** at a, in an analytical, um, control-based approach which will
[00:17:40:630 - 00:17:45:630] **Speaker 0:** minimise any kind of overshoot, maximise your response rate, and
[00:17:45:630 - 00:17:46:270] **Speaker 0:** that sort of thing.
[00:17:46:369 - 00:17:51:170] **Speaker 0:** What we're going to do is Um, achieve.
[00:17:55:020 - 00:18:06:430] **Speaker 1:** Good performance That Is particularly stable.
[00:18:14:709 - 00:18:16:630] **Speaker 0:** It's one of the, one of the big things that
[00:18:16:630 - 00:18:18:750] **Speaker 0:** we want to get right is that you don't want
[00:18:18:750 - 00:18:23:089] **Speaker 0:** a control system that because of some disturbance um or
[00:18:23:089 - 00:18:27:369] **Speaker 0:** um conditions with the input and the load, becomes unstable
[00:18:27:369 - 00:18:33:189] **Speaker 0:** and causes some sort of oscillation or um uh uncontrolled
[00:18:33:189 - 00:18:33:689] **Speaker 0:** behaviour.
[00:18:47:500 - 00:18:47:839] **Speaker 0:** Again.
[00:18:48:750 - 00:18:50:319] **Speaker 0:** It's really not liking it, is it?
[00:18:51:449 - 00:18:55:510] **Speaker 0:** Yeah, it has been every time we've been in here.
[00:18:57:640 - 00:18:58:339] **Speaker 1:** OK.
[00:19:02:239 - 00:19:04:199] **Speaker 0:** I'm sure the document camera will turn up in the,
[00:19:04:310 - 00:19:06:380] **Speaker 0:** in the um Echo 360 recording.
[00:19:09:619 - 00:19:12:510] **Speaker 0:** Right, so we need to, um, get a model that
[00:19:12:510 - 00:19:17:469] **Speaker 0:** we can generate our transfer function blocks from, alright, so
[00:19:17:469 - 00:19:18:829] **Speaker 0:** for our closed loop control.
[00:19:19:109 - 00:19:20:650] **Speaker 0:** So let's have a look.
[00:19:21:540 - 00:19:23:030] **Speaker 0:** I have to change which side to look on.
[00:19:23:839 - 00:19:25:660] **Speaker 0:** The, the brushed DC motor.
[00:19:32:979 - 00:19:37:180] **Speaker 0:** Right, so, This is, this is essentially the system we're
[00:19:37:180 - 00:19:37:619] **Speaker 0:** talking about.
[00:19:37:739 - 00:19:39:020] **Speaker 0:** Here's our mechanical load.
[00:19:39:300 - 00:19:43:660] **Speaker 0:** It has a certain inertia, uh, and torque requirement, right,
[00:19:43:780 - 00:19:46:819] **Speaker 0:** and we're driving that, we've coupled it to a, a
[00:19:46:819 - 00:19:50:140] **Speaker 0:** motor that is spinning at a particular speed and providing
[00:19:50:140 - 00:19:50:540] **Speaker 0:** the torque.
[00:19:50:819 - 00:19:53:260] **Speaker 0:** Notice that the load torque and the mechanic and the
[00:19:53:260 - 00:19:56:119] **Speaker 0:** motor torque are in opposite directions as you would expect.
[00:19:56:579 - 00:19:59:040] **Speaker 0:** Um, this little block in the middle is your gearbox.
[00:20:05:189 - 00:20:08:569] **Speaker 0:** Um, so what we are going to do in order
[00:20:08:569 - 00:20:14:270] **Speaker 0:** to be able to do the control is refer the
[00:20:14:280 - 00:20:17:709] **Speaker 0:** uh the inertia from the load through the gearbox to
[00:20:17:709 - 00:20:18:849] **Speaker 0:** the motor side.
[00:20:19:699 - 00:20:19:709] **Speaker 0:** Alright.
[00:20:22:079 - 00:20:26:189] **Speaker 0:** So we're going to end up with um the Uh,
[00:20:26:270 - 00:20:32:729] **Speaker 0:** inertia, TM, omega M, and we're going to go J.
[00:20:33:869 - 00:20:36:959] **Speaker 0:** Well, obviously the, the motor also has a, um, inertia,
[00:20:37:310 - 00:20:41:569] **Speaker 0:** and we're going to say that J overall total, is
[00:20:41:569 - 00:20:47:250] **Speaker 0:** equal to JM Oh, I see what I was gonna,
[00:20:48:119 - 00:20:48:739] **Speaker 0:** plus.
[00:20:49:520 - 00:20:56:719] **Speaker 0:** The referred To the, to the motor side, um, load
[00:20:57:060 - 00:20:57:579] **Speaker 0:** inertia.
[00:21:05:800 - 00:21:08:880] **Speaker 0:** All right, um, as far as the brush DC motor
[00:21:08:880 - 00:21:12:959] **Speaker 0:** is concerned, what we are modelling here is the input
[00:21:12:959 - 00:21:16:400] **Speaker 0:** voltage, the DC voltage, which is VBO.
[00:21:16:719 - 00:21:20:089] **Speaker 0:** So the VO just means back output.
[00:21:20:760 - 00:21:23:040] **Speaker 0:** So this is the output voltage from the back converter.
[00:21:33:609 - 00:21:37:060] **Speaker 0:** Then we have the armature impedance for the DC motor.
[00:21:37:569 - 00:21:43:010] **Speaker 0:** So DC uh motors have armatures, especially by definition for
[00:21:43:010 - 00:21:47:369] **Speaker 0:** DC machines, um, they have a particular series resistance and
[00:21:47:369 - 00:21:48:329] **Speaker 0:** inductance.
[00:21:49:119 - 00:21:52:290] **Speaker 0:** Alright, so the armature of a, of a, of which
[00:21:52:290 - 00:21:56:079] **Speaker 0:** is the rotating part of our DC motor is windings,
[00:21:56:489 - 00:22:00:849] **Speaker 0:** alright, that the um magnetic fields are produced by with
[00:22:00:849 - 00:22:02:170] **Speaker 0:** current flowing through those windings.
[00:22:02:489 - 00:22:05:290] **Speaker 0:** So the windings are represented by a resistance and an
[00:22:05:290 - 00:22:06:069] **Speaker 0:** inductance.
[00:22:08:150 - 00:22:12:030] **Speaker 0:** When you have that current that's in the motor rot
[00:22:12:030 - 00:22:15:030] **Speaker 0:** with the rotor rotating and it's passing through the magnetic
[00:22:15:030 - 00:22:18:349] **Speaker 0:** field of your stater, then you have a back EMF
[00:22:18:349 - 00:22:19:150] **Speaker 0:** being generated.
[00:22:20:180 - 00:22:24:219] **Speaker 0:** Right, that's how we get the power from the, the
[00:22:24:219 - 00:22:27:819] **Speaker 0:** source side, the, the electrical source side to the mechanical
[00:22:27:819 - 00:22:32:380] **Speaker 0:** output, is that you are driving current reverse through the
[00:22:32:380 - 00:22:38:119] **Speaker 0:** back EMF, right, so that's an energy, um, or power,
[00:22:38:380 - 00:22:41:979] **Speaker 0:** uh, that's coming out of this thing, not, um, sorry,
[00:22:42:060 - 00:22:45:010] **Speaker 0:** going into it so that it's driving a mechanical, uh,
[00:22:45:020 - 00:22:45:410] **Speaker 0:** torque.
[00:22:47:449 - 00:22:50:170] **Speaker 0:** Right, so we have an RA and LA which are
[00:22:50:170 - 00:22:54:189] **Speaker 0:** both the amateur resistance and inductance and a back EMF
[00:22:54:189 - 00:22:56:510] **Speaker 0:** that is dependent on speed.
[00:22:58:209 - 00:23:01:949] **Speaker 0:** Right, as the motors gets faster and faster, the magnitude
[00:23:01:949 - 00:23:04:410] **Speaker 0:** of that back MF gets larger and larger.
[00:23:06:000 - 00:23:07:849] **Speaker 0:** So we've got a power balance, we're assuming.
[00:23:08:819 - 00:23:10:709] **Speaker 0:** A 100% efficiency motor.
[00:23:11:579 - 00:23:14:380] **Speaker 0:** Uh, so that the input power is going to equal
[00:23:14:380 - 00:23:15:319] **Speaker 0:** the output power.
[00:23:16:660 - 00:23:19:239] **Speaker 0:** So electrical input power equals mechanical output power.
[00:23:21:219 - 00:23:22:939] **Speaker 0:** Just to keep things simple, I know there will be
[00:23:22:939 - 00:23:25:859] **Speaker 0:** losses, but we're just going to be assuming they're relatively
[00:23:25:859 - 00:23:28:400] **Speaker 0:** small losses for this um situation.
[00:23:30:099 - 00:23:34:199] **Speaker 0:** The induced back EMF, that's the EA is equal to
[00:23:34:199 - 00:23:38:160] **Speaker 0:** the K times omegam with K is the motor constant.
[00:23:46:030 - 00:23:50:560] **Speaker 1:** We also have That the torque in the motor is
[00:23:50:560 - 00:23:55:170] **Speaker 0:** equal to the motor constant, same constant times the armature
[00:23:55:170 - 00:23:55:729] **Speaker 0:** current.
[00:23:56:449 - 00:24:00:369] **Speaker 0:** So here's this direct proportionality between the torque from the
[00:24:00:369 - 00:24:02:829] **Speaker 0:** motor and the current flowing in the motor.
[00:24:14:219 - 00:24:17:619] **Speaker 0:** OK, uh, and we got, we got to, um, we
[00:24:17:619 - 00:24:21:030] **Speaker 0:** can, we can actually just utilise this EA IA omega
[00:24:21:030 - 00:24:24:829] **Speaker 0:** T, um, by putting this expression for EA into here
[00:24:24:829 - 00:24:26:849] **Speaker 0:** and rearranging for the talk.
[00:24:27:719 - 00:24:29:920] **Speaker 0:** The the omegas cancelled then.
[00:24:33:060 - 00:24:36:969] **Speaker 0:** The circuit, so we need to look at the, the
[00:24:36:969 - 00:24:38:760] **Speaker 0:** overall electrical circuit here.
[00:24:39:510 - 00:24:42:010] **Speaker 0:** Um, if we do Kirchoff's voltage law.
[00:24:43:349 - 00:24:45:589] **Speaker 0:** All the voltages around a closed loop has to equal
[00:24:45:589 - 00:24:46:170] **Speaker 0:** 0.
[00:24:47:989 - 00:24:52:589] **Speaker 0:** We've got the VBO minus EA because it's plus minus
[00:24:52:589 - 00:24:54:650] **Speaker 0:** you're going around the loop, then you go.
[00:24:56:290 - 00:25:02:189] **Speaker 0:** Plus minus, and it's minus plus, so it's VBO minus
[00:25:02:609 - 00:25:04:050] **Speaker 0:** the back EMF.
[00:25:04:349 - 00:25:06:770] **Speaker 0:** It's kind of called back MF because it's, you subtract
[00:25:06:770 - 00:25:10:489] **Speaker 0:** it, um, equals all of the other voltage drops in
[00:25:10:489 - 00:25:14:229] **Speaker 0:** that loop, and the voltage drop is IA times RA.
[00:25:15:270 - 00:25:18:790] **Speaker 0:** And the voltage, the voltage across an inductor, hey, we
[00:25:18:790 - 00:25:22:630] **Speaker 0:** haven't seen this before, um LA DIA by DT, right,
[00:25:22:790 - 00:25:24:150] **Speaker 0:** so rate of change of the current.
[00:25:32:420 - 00:25:34:640] **Speaker 0:** We, we're doing control.
[00:25:36:349 - 00:25:39:140] **Speaker 0:** We don't usually keep it in the time domain, the,
[00:25:39:229 - 00:25:40:979] **Speaker 0:** the, all the expressions that we work with.
[00:25:41:109 - 00:25:45:390] **Speaker 0:** It's much easier mathematically if we move to the complex
[00:25:45:390 - 00:25:48:510] **Speaker 0:** frequency domain when we're doing our control systems, right?
[00:25:48:829 - 00:25:52:250] **Speaker 0:** So this expression in the time domain is just this
[00:25:52:469 - 00:25:53:949] **Speaker 0:** in complex frequency domain.
[00:25:55:099 - 00:25:59:709] **Speaker 0:** Alright, so a differential in the complex frequency is just
[00:25:59:709 - 00:26:00:959] **Speaker 0:** multiplying by S.
[00:26:04:939 - 00:26:10:579] **Speaker 0:** OK, so, um, we have the voltage from your back
[00:26:10:579 - 00:26:14:260] **Speaker 0:** converter output minus the complex frequency version of your back
[00:26:14:260 - 00:26:18:660] **Speaker 0:** EMF equals the, um, complex frequency version of your current
[00:26:18:660 - 00:26:20:239] **Speaker 0:** times RA plus SLA.
[00:26:22:280 - 00:26:25:920] **Speaker 0:** The thing we're interested in for torque control is the
[00:26:25:920 - 00:26:26:900] **Speaker 0:** amateur current.
[00:26:27:770 - 00:26:30:040] **Speaker 0:** Right, so we just rearrange this to solve for your
[00:26:30:040 - 00:26:33:540] **Speaker 0:** Amage current, right, so you've got BBO minus EA over
[00:26:33:540 - 00:26:34:520] **Speaker 0:** RA plus SLA.
[00:26:36:540 - 00:26:40:650] **Speaker 0:** Again If we're doing control systems, we're interested in our
[00:26:40:650 - 00:26:42:040] **Speaker 0:** poles and zeros.
[00:26:43:689 - 00:26:46:329] **Speaker 0:** So we should really write this in pole zero form,
[00:26:46:650 - 00:26:48:510] **Speaker 0:** which is what we've got here.
[00:26:48:770 - 00:26:51:689] **Speaker 0:** So we bring out 1 over RA and then you're
[00:26:51:689 - 00:26:55:089] **Speaker 0:** left with 1 + S all over LA over RA.
[00:26:57:969 - 00:27:01:939] **Speaker 0:** Alright, so we've got a time constant for a pole
[00:27:01:939 - 00:27:04:829] **Speaker 0:** here that's equal to LA over RA.
[00:27:12:310 - 00:27:13:709] **Speaker 1:** And that's from the motor.
[00:27:23:479 - 00:27:25:959] **Speaker 0:** That's all well and good, but how do we do
[00:27:25:959 - 00:27:26:040] **Speaker 0:** it?
[00:27:26:119 - 00:27:31:420] **Speaker 0:** How do we convert from this sort of circuit representation
[00:27:32:869 - 00:27:35:920] **Speaker 0:** into a transfer function representation for our control system?
[00:27:37:339 - 00:27:40:079] **Speaker 0:** All right, so we'll be referring back to this um
[00:27:40:540 - 00:27:43:290] **Speaker 0:** this uh slide a bit when we, when we look
[00:27:43:290 - 00:27:46:739] **Speaker 0:** at how we've created our control system.
[00:27:51:959 - 00:27:52:410] **Speaker 0:** All right.
[00:27:53:790 - 00:27:55:560] **Speaker 0:** Bear with me, I'm gonna explain how we got there
[00:27:55:560 - 00:27:56:099] **Speaker 0:** with this.
[00:28:02:219 - 00:28:02:790] **Speaker 0:** OK.
[00:28:05:560 - 00:28:08:359] **Speaker 0:** I think the point that we should jump in it
[00:28:08:359 - 00:28:11:359] **Speaker 0:** is, uh, looking at the torque.
[00:28:11:920 - 00:28:13:859] **Speaker 0:** So here's the torque from the motor.
[00:28:15:189 - 00:28:16:530] **Speaker 0:** So the torque from the motor.
[00:28:17:829 - 00:28:23:010] **Speaker 0:** Um, coupled to the torque from the, from the load,
[00:28:23:430 - 00:28:23:589] **Speaker 0:** right?
[00:28:23:709 - 00:28:28:359] **Speaker 0:** So those, you've got um the addition of those or
[00:28:28:359 - 00:28:32:310] **Speaker 0:** the difference, I should say, of those, because whatever is
[00:28:32:310 - 00:28:36:810] **Speaker 0:** residual from that is what is left over to accelerate
[00:28:37:989 - 00:28:38:670] **Speaker 1:** the load.
[00:28:42:339 - 00:28:48:050] **Speaker 0:** So, the Remainding or remainder talk or residual.
[00:29:02:910 - 00:29:05:030] **Speaker 0:** Acts to accelerate the load.
[00:29:07:680 - 00:29:12:880] **Speaker 0:** So we've got from there, it's acceleration is D omega
[00:29:12:880 - 00:29:13:579] **Speaker 0:** DT.
[00:29:17:060 - 00:29:19:510] **Speaker 0:** Which is equal to the torque over the inertia, the
[00:29:19:510 - 00:29:20:410] **Speaker 0:** total inertia.
[00:29:28:030 - 00:29:30:969] **Speaker 0:** Right, but what's producing the talk, the talk is coming
[00:29:30:969 - 00:29:31:609] **Speaker 0:** from.
[00:29:32:810 - 00:29:33:910] **Speaker 0:** The electric motor.
[00:29:34:569 - 00:29:37:810] **Speaker 0:** And then the talk as we've just defined.
[00:29:39:770 - 00:29:41:650] **Speaker 0:** From here, the torque in the motor is equal to
[00:29:41:650 - 00:29:44:430] **Speaker 0:** the motor constant times the armage current.
[00:29:45:939 - 00:29:49:280] **Speaker 0:** Hence that's that's one of our blocks, it's just K.
[00:29:50:810 - 00:29:54:819] **Speaker 0:** The motor constant and the input to here is The
[00:29:54:819 - 00:29:55:640] **Speaker 1:** amateur current.
[00:29:56:660 - 00:30:00:040] **Speaker 0:** So how much current times k is our motor torque.
[00:30:04:339 - 00:30:04:770] **Speaker 0:** All right.
[00:30:05:739 - 00:30:06:969] **Speaker 0:** So that's IA.
[00:30:09:209 - 00:30:10:369] **Speaker 0:** What is IA equal?
[00:30:11:420 - 00:30:16:280] **Speaker 0:** IA is from the difference between the back converter voltage
[00:30:16:280 - 00:30:19:739] **Speaker 0:** and the back EMF divided by RA plus SLA.
[00:30:21:089 - 00:30:25:170] **Speaker 0:** Here we go, divided by RA plus SLA and here's
[00:30:25:170 - 00:30:30:099] **Speaker 0:** the difference between the back converter voltage and the back
[00:30:30:099 - 00:30:30:790] **Speaker 0:** EMF.
[00:30:32:619 - 00:30:34:239] **Speaker 0:** Right, so difference between those.
[00:30:35:160 - 00:30:36:579] **Speaker 0:** That's that part of the equation.
[00:30:38:459 - 00:30:41:459] **Speaker 0:** And then we go through by one over RA plus
[00:30:41:459 - 00:30:41:959] **Speaker 0:** SLA.
[00:30:44:959 - 00:30:48:739] **Speaker 0:** Don't forget though that we would normally for our control
[00:30:48:739 - 00:30:50:510] **Speaker 0:** system show this in poll 04.
[00:30:51:680 - 00:30:57:520] **Speaker 0:** So that's 1 over RA over 1 plus SLA over
[00:30:57:520 - 00:30:58:079] **Speaker 0:** RA.
[00:31:04:290 - 00:31:05:900] **Speaker 0:** Alright, but how do we get EA?
[00:31:06:410 - 00:31:09:400] **Speaker 0:** Well, EA K times EA.
[00:31:10:109 - 00:31:14:189] **Speaker 0:** Is our speed Sorry, speed.
[00:31:16:400 - 00:31:20:920] **Speaker 0:** EA is K times the speed, right, so we have
[00:31:20:920 - 00:31:24:459] **Speaker 0:** speed at one side, omega and we multiply it by
[00:31:24:459 - 00:31:27:459] **Speaker 0:** k, then we're gonna have the back EMF.
[00:31:28:750 - 00:31:30:369] **Speaker 0:** Right, but where do we get speed from?
[00:31:31:160 - 00:31:36:969] **Speaker 0:** OK, well, we've got already the rate of change of
[00:31:36:969 - 00:31:38:760] **Speaker 0:** speed on one side here.
[00:31:39:670 - 00:31:42:550] **Speaker 0:** Which is equal to the torque, residual talk over the,
[00:31:42:750 - 00:31:43:439] **Speaker 0:** the inertia.
[00:31:44:349 - 00:31:48:130] **Speaker 0:** If we can integrate this, Then we, we come up
[00:31:48:130 - 00:31:48:910] **Speaker 0:** with speed.
[00:31:50:089 - 00:31:54:140] **Speaker 0:** Right, so here we go, we put, put the acceleration
[00:31:54:810 - 00:31:57:270] **Speaker 0:** through an integrator, so 1 overs.
[00:31:58:150 - 00:31:58:869] **Speaker 0:** There's the integrator.
[00:31:59:050 - 00:32:01:449] **Speaker 0:** We've got one over J to take care of the
[00:32:02:119 - 00:32:02:560] **Speaker 0:** inertia.
[00:32:03:939 - 00:32:07:430] **Speaker 0:** And we're left with The speed of the, of the,
[00:32:07:510 - 00:32:08:530] **Speaker 0:** of the system.
[00:32:16:089 - 00:32:19:390] **Speaker 0:** OK, so we take that speed, we multiply it by
[00:32:19:689 - 00:32:23:439] **Speaker 0:** the um, The motor constant and we're given EA.
[00:32:23:810 - 00:32:26:380] **Speaker 0:** So this is some feedback that we've already got going
[00:32:26:380 - 00:32:26:880] **Speaker 1:** on.
[00:32:29:959 - 00:32:35:589] **Speaker 0:** Between speed and um the voltage from the um the
[00:32:35:589 - 00:32:36:160] **Speaker 0:** butt converter.
[00:32:42:369 - 00:32:48:329] **Speaker 0:** So, we can implement fast control without worrying about any
[00:32:48:329 - 00:32:51:449] **Speaker 0:** changes in EA as the time constants are really different.
[00:32:51:599 - 00:32:54:930] **Speaker 0:** Remember, we can adjust the torque really quickly because the
[00:32:54:930 - 00:32:57:989] **Speaker 0:** power electronics allows us from the back converter to change
[00:32:57:989 - 00:32:59:310] **Speaker 0:** the voltage really fast.
[00:33:00:319 - 00:33:03:689] **Speaker 0:** So But we have, because of the inertia.
[00:33:04:660 - 00:33:08:300] **Speaker 0:** Um, in the whole system, that's motor and load, then
[00:33:08:300 - 00:33:12:449] **Speaker 0:** the motor speed can only accelerate or or the motor
[00:33:12:449 - 00:33:14:300] **Speaker 0:** speed can only change relatively slowly.
[00:33:14:619 - 00:33:18:900] **Speaker 0:** So EA can only change relatively slowly.
[00:33:20:500 - 00:33:23:599] **Speaker 0:** So if it's only changing slowly, that's not a dynamic
[00:33:24:260 - 00:33:27:420] **Speaker 0:** change that the control system has to worry about.
[00:33:27:459 - 00:33:30:119] **Speaker 0:** This is changing fast, this is changing slow.
[00:33:30:869 - 00:33:34:109] **Speaker 0:** So for all intents and purposes for this part of
[00:33:34:109 - 00:33:36:829] **Speaker 0:** the, the um the system that does change fast, this
[00:33:36:829 - 00:33:37:569] **Speaker 0:** is a constant.
[00:33:52:650 - 00:33:56:449] **Speaker 0:** So that in a control loop that we've uh introduced
[00:33:56:449 - 00:33:59:829] **Speaker 0:** at the start, effectively in, in a control loop.
[00:34:02:010 - 00:34:06:369] **Speaker 0:** We have the motor dynamics.
[00:34:15:408 - 00:34:16:610] **Speaker 0:** We've got the load.
[00:34:18:759 - 00:34:19:627] **Speaker 0:** Included.
[00:34:23:939 - 00:34:26:939] **Speaker 0:** The VS side of here, so you're changing the duty
[00:34:26:939 - 00:34:29:860] **Speaker 0:** ratio, this is the buck converter, this is our power
[00:34:29:860 - 00:34:30:719] **Speaker 0:** electronics.
[00:34:43:959 - 00:34:48:689] **Speaker 0:** So VBO equals D times VS.
[00:34:57:919 - 00:34:59:580] **Speaker 0:** We're measuring the current.
[00:35:00:500 - 00:35:03:729] **Speaker 0:** Comparing that to an ordered current, we have an error.
[00:35:05:399 - 00:35:10:179] **Speaker 0:** Which we feed into, um, I've identified here a PI
[00:35:10:179 - 00:35:13:120] **Speaker 0:** controller, we'll talk about that shortly, why it's a PI
[00:35:13:120 - 00:35:14:199] **Speaker 0:** is sufficient.
[00:35:15:020 - 00:35:18:939] **Speaker 0:** Um, outputs a parameter that tells us the duty ratio
[00:35:18:939 - 00:35:23:639] **Speaker 0:** that we need to, um, have the power electronics includes
[00:35:23:899 - 00:35:26:659] **Speaker 0:** the information to change the duty ratio and we can
[00:35:26:659 - 00:35:29:120] **Speaker 0:** change the output voltage, which changes.
[00:35:29:820 - 00:35:31:010] **Speaker 0:** The amount of current flowing.
[00:35:33:250 - 00:35:38:060] **Speaker 0:** To drive the amateur current to what we have ordered.
[00:35:40:639 - 00:35:44:330] **Speaker 0:** The load side, because this is happening so slowly, um,
[00:35:44:399 - 00:35:49:629] **Speaker 0:** feeding the EA or changing the EA, um, We can
[00:35:49:629 - 00:35:54:600] **Speaker 0:** essentially neglect that for the dynamic purposes of the control.
[00:35:54:800 - 00:35:56:179] **Speaker 0:** So this can be simplified.
[00:35:57:159 - 00:36:04:159] **Speaker 0:** To That this summer with the difference.
[00:36:08:550 - 00:36:12:949] **Speaker 0:** The era The PI control.
[00:36:16:120 - 00:36:19:909] **Speaker 0:** The back converter with its source voltage, where that is,
[00:36:20:189 - 00:36:22:469] **Speaker 0:** the duty ratio is telling you what to drive it
[00:36:22:469 - 00:36:22:810] **Speaker 0:** at.
[00:36:23:550 - 00:36:25:770] **Speaker 0:** We've got the plus.
[00:36:27:669 - 00:36:29:659] **Speaker 0:** Plus minus 4 EA.
[00:36:30:439 - 00:36:31:860] **Speaker 0:** But that's essentially constant.
[00:36:34:300 - 00:36:37:070] **Speaker 0:** And you're left with one over RA.
[00:36:38:580 - 00:36:44:780] **Speaker 0:** 1/1 plus is, the time constant which is LA.
[00:36:45:469 - 00:36:51:340] **Speaker 0:** Over RA The output is the amateur current.
[00:36:52:639 - 00:36:54:379] **Speaker 0:** The thing that we're trying to control here.
[00:36:57:000 - 00:36:58:429] **Speaker 0:** And we feed that back.
[00:36:58:600 - 00:37:00:060] **Speaker 0:** So this is your measured.
[00:37:04:669 - 00:37:05:969] **Speaker 0:** This is I ordered.
[00:37:14:439 - 00:37:15:600] **Speaker 0:** See if it'll stay on there.
[00:37:16:389 - 00:37:17:649] **Speaker 0:** had a chance to cool down a bit.
[00:37:21:500 - 00:37:23:419] **Speaker 0:** Right, so YPI?
[00:37:23:780 - 00:37:26:939] **Speaker 0:** Well, we have a system that requires a non-zero value
[00:37:26:939 - 00:37:31:830] **Speaker 0:** of duty ratio when the armature current is at the
[00:37:31:830 - 00:37:33:320] **Speaker 0:** value we want.
[00:37:35:010 - 00:37:37:850] **Speaker 0:** OK, you, if it, if this, if the error, um,
[00:37:37:860 - 00:37:40:719] **Speaker 0:** and you and your controller forced that to zero.
[00:37:41:560 - 00:37:44:239] **Speaker 0:** For zero error, which it would do if it was
[00:37:44:239 - 00:37:47:580] **Speaker 0:** just proportional control, then you would end up with a
[00:37:47:580 - 00:37:51:110] **Speaker 0:** zero duty ratio being forced into your back converter, which
[00:37:51:110 - 00:37:53:530] **Speaker 0:** means the output voltage would be zero and your current
[00:37:53:530 - 00:37:54:820] **Speaker 0:** would drop to 0.
[00:37:56:290 - 00:37:57:389] **Speaker 0:** That doesn't work.
[00:37:57:689 - 00:38:00:909] **Speaker 0:** So what you need is when your um measured current
[00:38:00:909 - 00:38:03:969] **Speaker 0:** is effectively equal to your ordered current, your integral part
[00:38:03:969 - 00:38:08:810] **Speaker 0:** of con control maintains that value of duty ratio.
[00:38:12:040 - 00:38:12:659] **Speaker 0:** OK.
[00:38:14:610 - 00:38:17:979] **Speaker 0:** And the proportional control part ensures that the residual offset
[00:38:17:979 - 00:38:21:840] **Speaker 0:** that you have um from the control is, is small.
[00:38:23:229 - 00:38:25:820] **Speaker 0:** Right, it'll be continuous, but it'll be a small value.
[00:38:26:530 - 00:38:30:770] **Speaker 0:** Remember, it's not non-zero for the for the error, there
[00:38:30:770 - 00:38:32:739] **Speaker 0:** will always be a small residual error.
[00:38:33:780 - 00:38:39:179] **Speaker 0:** Differential Differential control here in this instance would be to
[00:38:39:179 - 00:38:41:540] **Speaker 0:** avoid overshoot situations.
[00:38:41:899 - 00:38:46:439] **Speaker 0:** Um, sure you could add it, it doesn't do much
[00:38:46:699 - 00:38:49:459] **Speaker 0:** for the operation of the converter, uh, of, of this
[00:38:49:459 - 00:38:50:840] **Speaker 0:** torque control as we have it.
[00:38:51:689 - 00:38:54:909] **Speaker 0:** So, we're not employing any kind of differential control.
[00:39:00:510 - 00:39:01:229] **Speaker 0:** Differential.
[00:39:02:179 - 00:39:05:439] **Speaker 0:** Certainly, consider adding it if you are trying to optimise
[00:39:05:939 - 00:39:08:580] **Speaker 0:** the overall performance of this control network, but we are
[00:39:08:580 - 00:39:11:760] **Speaker 0:** just aiming for sufficient operation and stability.
[00:39:20:479 - 00:39:26:860] **Speaker 0:** Right, so for PI control, We need to look at
[00:39:26:860 - 00:39:29:429] **Speaker 0:** how we're gonna come up with our um our control
[00:39:29:429 - 00:39:30:239] **Speaker 0:** weightings.
[00:39:30:669 - 00:39:34:270] **Speaker 0:** What is our proportional control factor, what is our integral
[00:39:34:270 - 00:39:34:689] **Speaker 0:** control?
[00:39:36:020 - 00:39:39:610] **Speaker 0:** So we have for the PI control part, we have,
[00:39:39:830 - 00:39:42:330] **Speaker 0:** um, as far as our transfer function is concerned, the
[00:39:42:340 - 00:39:45:850] **Speaker 0:** the um the proportional coefficient and the integral overs.
[00:39:47:739 - 00:39:48:419] **Speaker 0:** It's integral.
[00:39:49:449 - 00:39:52:159] **Speaker 0:** Um, that's not in pole zero form, so we convert
[00:39:52:159 - 00:39:54:149] **Speaker 0:** that into pole 0 form, usually.
[00:39:55:639 - 00:39:57:340] **Speaker 0:** So, here's your integral.
[00:40:00:159 - 00:40:01:270] **Speaker 0:** And you're proportional.
[00:40:07:399 - 00:40:08:479] **Speaker 0:** In poll 0 form.
[00:40:08:959 - 00:40:11:479] **Speaker 0:** Right, we need to be able to choose appropriate values
[00:40:11:479 - 00:40:13:439] **Speaker 0:** to make the control system work practically.
[00:40:14:459 - 00:40:17:820] **Speaker 0:** If we're going to do that, then first step is
[00:40:17:820 - 00:40:21:300] **Speaker 0:** to determine what is our open loop gain, gain of
[00:40:21:300 - 00:40:22:560] **Speaker 0:** the plant or the system.
[00:40:24:760 - 00:40:29:040] **Speaker 0:** Alright, so, that's looking open loop, so from the input
[00:40:29:040 - 00:40:33:229] **Speaker 0:** through the transfer functions to the output with no feedback.
[00:40:37:830 - 00:40:40:939] **Speaker 0:** So this is for this side here, so we're moving
[00:40:40:939 - 00:40:45:310] **Speaker 0:** through from the PI control through the back converter and
[00:40:45:310 - 00:40:48:919] **Speaker 0:** through the motor to the output with no feedback.
[00:40:51:729 - 00:40:55:750] **Speaker 0:** So, First up, we've got our PI control, so that's
[00:40:55:750 - 00:40:58:469] **Speaker 0:** just KI over S 1 + S, KP over KI,
[00:40:58:629 - 00:41:00:350] **Speaker 0:** that's the first bit, sorry, the first bit.
[00:41:01:909 - 00:41:09:739] **Speaker 0:** Then we've got our But converter But yes That's the
[00:41:09:739 - 00:41:11:199] **Speaker 0:** amplitude of the voltage source.
[00:41:11:939 - 00:41:15:100] **Speaker 0:** We don't worry about this because EA is effectively considered
[00:41:15:100 - 00:41:17:860] **Speaker 0:** to be static for this control loop.
[00:41:19:219 - 00:41:23:389] **Speaker 0:** The next part is the uh the motor itself, which
[00:41:23:389 - 00:41:25:000] **Speaker 0:** is one over RA.
[00:41:26:679 - 00:41:28:820] **Speaker 0:** Time 1 over SLA over RA.
[00:41:30:439 - 00:41:33:790] **Speaker 0:** Right, so that's the open loop game through here with
[00:41:33:790 - 00:41:34:750] **Speaker 0:** no, no feedback.
[00:41:38:879 - 00:41:41:780] **Speaker 0:** Right, we want to keep this control system stable.
[00:41:43:379 - 00:41:45:739] **Speaker 0:** So in order to keep, keep it stable, we need
[00:41:45:739 - 00:41:50:260] **Speaker 0:** to make sure that With the gain.
[00:41:50:959 - 00:41:54:399] **Speaker 0:** Open loop gain close to its magnitude close to to
[00:41:54:399 - 00:41:57:520] **Speaker 0:** or equal to 1 that we don't have a phase
[00:41:57:520 - 00:42:00:300] **Speaker 0:** difference that is plus or minus 180 degrees.
[00:42:00:879 - 00:42:06:080] **Speaker 0:** If we do, that's positive feedback that reinforces itself and
[00:42:06:080 - 00:42:07:600] **Speaker 0:** you'll explode the system.
[00:42:08:850 - 00:42:10:489] **Speaker 0:** Right, so it's, it'll just oscillate.
[00:42:13:550 - 00:42:17:010] **Speaker 0:** So we can't have a phase shift 180 degrees, um,
[00:42:17:159 - 00:42:18:179] **Speaker 0:** but a pole.
[00:42:20:070 - 00:42:24:570] **Speaker 0:** is going to give you a, um, potentially, if the
[00:42:24:570 - 00:42:30:580] **Speaker 0:** cutoff frequencies are right and the zero cutoff is Too
[00:42:30:580 - 00:42:33:620] **Speaker 0:** high in frequency, you're gonna get two poles adding.
[00:42:34:929 - 00:42:39:590] **Speaker 0:** That's -90 degrees, -90 degrees, leading to 180 degrees.
[00:42:40:739 - 00:42:45:330] **Speaker 0:** So there is the potential for the system to become
[00:42:45:330 - 00:42:47:300] **Speaker 0:** unstable as it stands.
[00:42:53:649 - 00:42:57:489] **Speaker 0:** Right, we're gonna make sure by our design that that
[00:42:57:729 - 00:42:59:070] **Speaker 0:** is an impossibility.
[00:42:59:449 - 00:43:01:350] **Speaker 0:** It just will not occur.
[00:43:02:010 - 00:43:03:149] **Speaker 0:** And how do we do that?
[00:43:03:689 - 00:43:05:750] **Speaker 0:** We are going to do a bit of a trick.
[00:43:06:479 - 00:43:08:899] **Speaker 0:** And the little trick is that we're going to make
[00:43:09:479 - 00:43:14:780] **Speaker 0:** the um the motor pole and the PI control zero
[00:43:15:840 - 00:43:18:719] **Speaker 0:** have the same cutoff frequency, so they cancel.
[00:43:20:370 - 00:43:23:610] **Speaker 0:** Right, so we're gonna make KP over KI equal to
[00:43:23:610 - 00:43:24:770] **Speaker 0:** LA over RA.
[00:43:27:000 - 00:43:31:659] **Speaker 0:** Alright, so if we do that, Then if this ratio
[00:43:31:659 - 00:43:34:979] **Speaker 0:** is the same as that ratio, then we've got the
[00:43:34:979 - 00:43:40:159] **Speaker 0:** same uh here and here, so that cancels.
[00:43:42:770 - 00:43:46:409] **Speaker 0:** So one of our poles has just disappeared from the
[00:43:46:409 - 00:43:47:489] **Speaker 0:** open loop gain.
[00:43:48:379 - 00:43:53:370] **Speaker 0:** Right, and we're left with this very, very simple open
[00:43:53:370 - 00:43:54:100] **Speaker 0:** loop game.
[00:43:54:260 - 00:43:56:229] **Speaker 0:** Sure there's one over here, there's a pole.
[00:43:57:360 - 00:43:59:100] **Speaker 0:** In the frequency domain, we see it here.
[00:43:59:679 - 00:44:03:040] **Speaker 0:** 1 over J minus 90 degrees, that's as bad as
[00:44:03:040 - 00:44:05:520] **Speaker 0:** it gets for phase shift.
[00:44:06:040 - 00:44:10:300] **Speaker 0:** It can't hit 180 degrees, so it won't go unstable,
[00:44:10:439 - 00:44:10:879] **Speaker 0:** ever.
[00:44:14:469 - 00:44:17:489] **Speaker 0:** Right, so we've just ensured that stability criteria.
[00:44:19:439 - 00:44:21:399] **Speaker 0:** We're gonna call this, by the way, we're gonna come
[00:44:21:399 - 00:44:23:139] **Speaker 0:** back to it, I'm gonna call that equation one.
[00:44:31:070 - 00:44:34:219] **Speaker 1:** So I've just sort of Sort of throwing this at
[00:44:34:219 - 00:44:36:909] **Speaker 0:** you a little bit about not having the gain equal
[00:44:36:909 - 00:44:39:909] **Speaker 0:** to 1, for 180 degrees phase shift, that's a, that's
[00:44:39:909 - 00:44:42:850] **Speaker 0:** a nasty thing, uh, or a bad, bad situation.
[00:44:43:550 - 00:44:46:590] **Speaker 0:** Just to, to go, I guess, just to step back
[00:44:46:590 - 00:44:48:770] **Speaker 0:** a little bit more of the control theory.
[00:44:50:020 - 00:44:51:429] **Speaker 0:** Um, we'll, we'll.
[00:44:52:659 - 00:44:54:639] **Speaker 0:** Just have a look at that a little closer.
[00:45:02:469 - 00:45:05:870] **Speaker 0:** For good control, we want that open loop gain to
[00:45:05:870 - 00:45:12:310] **Speaker 0:** be quite large for um for our, our frequencies that
[00:45:12:310 - 00:45:14:110] **Speaker 0:** we're intending to, to utilise.
[00:45:14:989 - 00:45:17:860] **Speaker 0:** Um, and we want that gain to be low for
[00:45:17:860 - 00:45:21:070] **Speaker 0:** higher disturbance frequencies.
[00:45:22:790 - 00:45:25:860] **Speaker 0:** OK, for us, as far as we're concerned, that is
[00:45:25:860 - 00:45:29:060] **Speaker 0:** the switching frequency disturbances from the power electronic converter.
[00:45:30:050 - 00:45:32:489] **Speaker 0:** We want the gain to be low at those, at
[00:45:32:489 - 00:45:33:669] **Speaker 0:** those frequencies.
[00:45:34:689 - 00:45:39:290] **Speaker 0:** Right, so let's consider a general plant under with feedback
[00:45:39:290 - 00:45:39:669] **Speaker 0:** control.
[00:45:42:330 - 00:45:44:239] **Speaker 0:** So you've got your summation plus minus.
[00:45:45:409 - 00:45:50:020] **Speaker 0:** Here's your plant With Open loop Game G.
[00:45:52:830 - 00:45:55:459] **Speaker 0:** We have an output, and we've got an I ordered.
[00:45:57:780 - 00:45:59:879] **Speaker 0:** And an I, which is our output.
[00:46:00:580 - 00:46:04:820] **Speaker 0:** And we have Feedback, control.
[00:46:07:889 - 00:46:08:889] **Speaker 0:** So what does this tell us?
[00:46:09:090 - 00:46:12:750] **Speaker 0:** Well, I equals the gain.
[00:46:14:080 - 00:46:16:399] **Speaker 0:** Times I ordered.
[00:46:17:909 - 00:46:19:100] **Speaker 0:** Minus 1.
[00:46:22:979 - 00:46:23:260] **Speaker 0:** Yeah.
[00:46:29:280 - 00:46:35:340] **Speaker 0:** Or I equals the gain over 1 plus the gain
[00:46:35:639 - 00:46:37:000] **Speaker 0:** times I ordered.
[00:46:39:000 - 00:46:42:530] **Speaker 0:** So the gain through the through the system is large,
[00:46:42:830 - 00:46:47:959] **Speaker 0:** large G, well I think large G1 falls out and
[00:46:47:959 - 00:46:49:760] **Speaker 0:** you just end up with G over G for large
[00:46:49:760 - 00:46:50:070] **Speaker 0:** G.
[00:46:50:389 - 00:46:53:270] **Speaker 0:** So I equals I ordered, exactly what we want, right,
[00:46:53:360 - 00:46:54:320] **Speaker 0:** for our control system.
[00:46:55:379 - 00:46:57:750] **Speaker 0:** That the output is equal to what we're ordering at
[00:46:57:750 - 00:46:58:209] **Speaker 0:** the input.
[00:47:10:330 - 00:47:13:219] **Speaker 0:** On the other side, if we don't want um our
[00:47:13:219 - 00:47:17:860] **Speaker 0:** output to react to um to to uh higher frequency
[00:47:17:860 - 00:47:20:479] **Speaker 0:** disturbances, we want the gain to be small.
[00:47:26:899 - 00:47:29:489] **Speaker 0:** That would mean that I is less than I ordered.
[00:47:31:229 - 00:47:35:010] **Speaker 0:** Alright, so it would be attenuated, right, so disturbances would
[00:47:35:010 - 00:47:37:050] **Speaker 0:** be attenuated, the higher frequency stuff.
[00:47:40:459 - 00:47:43:449] **Speaker 0:** How do we decide then where, where this transition is
[00:47:43:449 - 00:47:49:239] **Speaker 0:** between good control for large G and poor control or
[00:47:49:250 - 00:47:51:330] **Speaker 0:** not reacting to it for small G?
[00:47:52:169 - 00:47:55:610] **Speaker 0:** Well, it turns out that um we look at that
[00:47:55:610 - 00:47:58:110] **Speaker 0:** as being defined as the gain is equal to one.
[00:47:59:800 - 00:48:04:250] **Speaker 0:** Alright, so, gain magnitude of gain is equal to one
[00:48:04:250 - 00:48:05:229] **Speaker 0:** is the transition.
[00:48:22:040 - 00:48:24:570] **Speaker 0:** So I've given you a little bow plot there of
[00:48:24:570 - 00:48:26:989] **Speaker 0:** the closed loop game of a system.
[00:48:27:489 - 00:48:28:850] **Speaker 0:** We have 0 dB.
[00:48:29:209 - 00:48:32:050] **Speaker 0:** We've got what's identified as the bandwidth and the minus
[00:48:32:050 - 00:48:32:810] **Speaker 0:** 3 dB.
[00:48:33:320 - 00:48:37:310] **Speaker 0:** This is, of course, um, like I equals i ordered
[00:48:37:770 - 00:48:38:659] **Speaker 0:** would be here.
[00:48:40:469 - 00:48:44:770] **Speaker 0:** We've got the cutoff frequency at the -3 dB point.
[00:48:48:550 - 00:48:52:729] **Speaker 0:** And where here it would be I is less than
[00:48:52:729 - 00:48:53:550] **Speaker 0:** I ordered.
[00:49:02:560 - 00:49:05:879] **Speaker 0:** Also to reinforce what we're talking about as far as
[00:49:05:879 - 00:49:08:719] **Speaker 0:** trying to make sure that um we have, that the
[00:49:08:719 - 00:49:13:280] **Speaker 0:** gain magnitude isn't close to 1 at 180 degrees phase
[00:49:13:280 - 00:49:18:020] **Speaker 0:** shift, um, we've got an example of some, um, gain
[00:49:18:020 - 00:49:19:479] **Speaker 0:** and phase plots.
[00:49:20:239 - 00:49:24:719] **Speaker 0:** This is not necessarily for um our system that we're
[00:49:24:719 - 00:49:27:560] **Speaker 0:** talking about with the, with the um back converter controlling
[00:49:27:560 - 00:49:28:560] **Speaker 0:** a DC motor.
[00:49:28:840 - 00:49:30:780] **Speaker 0:** It's just a generic, it's just an example.
[00:49:35:500 - 00:49:40:080] **Speaker 0:** So the gain This is in uh DB.
[00:49:42:429 - 00:49:45:020] **Speaker 0:** Uh, comes down 0 to be is when the gain
[00:49:45:020 - 00:49:45:830] **Speaker 0:** is equal to 1.
[00:49:52:030 - 00:49:54:989] **Speaker 0:** At this point, we can see whilst the uh phase
[00:49:54:989 - 00:49:59:270] **Speaker 0:** for whatever reason in this particular system, dips down to
[00:49:59:270 - 00:50:03:070] **Speaker 0:** getting quite close to 180 degrees, by the time we
[00:50:03:070 - 00:50:05:510] **Speaker 0:** get to where the gain is equal to 1, there
[00:50:05:510 - 00:50:12:100] **Speaker 0:** is actually quite a substantial uh Phase angle away from
[00:50:12:100 - 00:50:13:399] **Speaker 0:** the 180 degrees.
[00:50:13:820 - 00:50:16:459] **Speaker 0:** That's known as the difference in angle is known as
[00:50:16:459 - 00:50:17:550] **Speaker 0:** the phase margin.
[00:50:19:090 - 00:50:22:489] **Speaker 0:** And for good control, we are trying to ensure that
[00:50:22:489 - 00:50:23:889] **Speaker 0:** by the time we get to where the gain is
[00:50:23:889 - 00:50:27:850] **Speaker 0:** equal to 1, we have at least 45 degrees phase
[00:50:27:850 - 00:50:28:370] **Speaker 1:** margin.
[00:50:44:399 - 00:50:49:699] **Speaker 0:** Because that allows for some considerable noise to be in
[00:50:49:699 - 00:50:55:159] **Speaker 0:** the system that may um fluctuate the um the phase
[00:50:55:500 - 00:50:59:010] **Speaker 0:** to be um away from what we expect in an
[00:50:59:010 - 00:50:59:899] **Speaker 0:** instant in time.
[00:51:00:020 - 00:51:04:500] **Speaker 0:** So, um, we've got quite a substantial amount of, of
[00:51:04:500 - 00:51:06:979] **Speaker 0:** noise carrying capability with that sort of phase margin.
[00:51:07:739 - 00:51:11:010] **Speaker 0:** It's not infinite, but it is large enough to be
[00:51:11:010 - 00:51:13:879] **Speaker 0:** considered satisfactory under nearly every practical application.
[00:51:20:379 - 00:51:20:770] **Speaker 0:** Yeah.
[00:51:23:290 - 00:51:23:800] **Speaker 0:** OK.
[00:51:26:110 - 00:51:28:929] **Speaker 0:** Now we're ready to get on to figuring out what
[00:51:28:929 - 00:51:34:629] **Speaker 0:** we actually can uh determine for our KP and KI
[00:51:34:629 - 00:51:35:550] **Speaker 0:** values.
[00:51:46:409 - 00:51:47:699] **Speaker 0:** Someone just said something.
[00:51:48:500 - 00:51:50:739] **Speaker 0:** The next lecture is a bit short anyway, so I
[00:51:50:739 - 00:51:51:540] **Speaker 0:** could have stopped.
[00:51:51:939 - 00:51:54:639] **Speaker 0:** Sorry, um, get, get a bit carried away.
[00:51:54:820 - 00:51:58:100] **Speaker 0:** Um, so yeah, we'll finish things off tomorrow and and
[00:51:58:100 - 00:52:01:939] **Speaker 0:** uh we'll actually even conclude with what you need to
[00:52:01:939 - 00:52:05:020] **Speaker 0:** set up for your solar car for it's closed loop
[00:52:05:020 - 00:52:05:479] **Speaker 0:** control.

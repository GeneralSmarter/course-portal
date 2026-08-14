# ENEL372-26S2 Lecture 15 native Echo transcript

Date: August 14, 2026 9:00am-9:55am
Transcript type: native Echo automated transcript.

[00:00:00:569 - 00:00:02:700] **Speaker 0:** OK, Kyorakoto, welcome along.
[00:00:03:650 - 00:00:05:090] **Speaker 0:** We'll get things kicked off.
[00:00:06:130 - 00:00:08:380] **Speaker 0:** Uh, thank you for making the effort to be here
[00:00:08:380 - 00:00:10:260] **Speaker 0:** at this early hour of the day.
[00:00:10:649 - 00:00:14:409] **Speaker 0:** Um, right, so we didn't quite, quite finish off, uh,
[00:00:14:420 - 00:00:15:479] **Speaker 0:** in the last lecture.
[00:00:15:739 - 00:00:21:139] **Speaker 0:** We had, uh, determined, um, some, um, transfer functions for
[00:00:21:139 - 00:00:25:200] **Speaker 0:** our inner loop control which is looking at torque control,
[00:00:25:420 - 00:00:30:139] **Speaker 0:** uh, which luckily for us means effectively current control, um.
[00:00:31:659 - 00:00:35:139] **Speaker 0:** We got to the point where we went through a
[00:00:35:139 - 00:00:40:380] **Speaker 0:** simplification process to eliminate a pole and a zero by
[00:00:40:380 - 00:00:43:319] **Speaker 0:** making the um the weightings of those the same.
[00:00:43:659 - 00:00:47:340] **Speaker 0:** Uh, now we've got to the point where we need
[00:00:47:340 - 00:00:51:330] **Speaker 0:** to try and choose um a reasonable bandwidth or cutoff
[00:00:51:330 - 00:00:53:299] **Speaker 0:** frequency for our uh control loop.
[00:00:54:720 - 00:00:57:759] **Speaker 0:** So we need to uh make sure that the gain
[00:00:57:759 - 00:01:03:119] **Speaker 0:** of our system is small at frequencies of disturbance that
[00:01:03:119 - 00:01:05:510] **Speaker 0:** are not of interest or that we don't want the
[00:01:05:518 - 00:01:07:480] **Speaker 0:** the control system to react to.
[00:01:08:209 - 00:01:11:540] **Speaker 0:** Um, so for us that's the, the, the, the frequency
[00:01:11:540 - 00:01:15:519] **Speaker 0:** associated with any kind of, uh, ripple associated with the,
[00:01:15:540 - 00:01:17:660] **Speaker 0:** um, with the switching frequency.
[00:01:17:919 - 00:01:20:459] **Speaker 0:** So we have this current ripple, of course, and we
[00:01:20:459 - 00:01:23:339] **Speaker 0:** end up also with a small amount of voltage ripple.
[00:01:23:569 - 00:01:27:069] **Speaker 0:** We don't want our control system to be reacting to,
[00:01:27:459 - 00:01:30:260] **Speaker 0:** especially with this being the control loop, that current ripple.
[00:01:31:220 - 00:01:36:169] **Speaker 0:** So we can choose uh by design for our cutoff
[00:01:36:169 - 00:01:39:660] **Speaker 0:** frequency of our control system, so that's its bandwidth, uh
[00:01:39:660 - 00:01:44:379] **Speaker 0:** to be somewhere between around 1/5 to 1/10 of the
[00:01:44:379 - 00:01:45:389] **Speaker 0:** switching frequency.
[00:01:45:779 - 00:01:49:949] **Speaker 0:** Uh, for practical purposes, you would tend to go to
[00:01:49:949 - 00:01:52:389] **Speaker 0:** the end of the 1/10 rather than the 1/5.
[00:01:52:669 - 00:01:56:889] **Speaker 0:** 1/5 you're just leaving yourself a little bit of um
[00:01:56:910 - 00:02:01:069] **Speaker 0:** potential therefore still, uh, having something go wrong due to,
[00:02:01:190 - 00:02:02:169] **Speaker 0:** due to noise.
[00:02:03:300 - 00:02:08:960] **Speaker 0:** So, say the cutoff frequency is equal to our um
[00:02:09:259 - 00:02:10:899] **Speaker 0:** switching frequency divided by 10.
[00:02:12:789 - 00:02:18:429] **Speaker 0:** If that's the case, then going by the gain that
[00:02:18:429 - 00:02:19:130] **Speaker 0:** we had.
[00:02:20:500 - 00:02:25:789] **Speaker 0:** Determined after we made our simplification, um, then we can
[00:02:25:789 - 00:02:29:250] **Speaker 0:** say that that is going to be equal to one
[00:02:29:250 - 00:02:30:589] **Speaker 0:** at the cutoff frequency.
[00:02:33:550 - 00:02:36:500] **Speaker 0:** So the magnitude of that is equal to 1 at
[00:02:36:500 - 00:02:37:330] **Speaker 0:** omega C.
[00:02:42:600 - 00:02:43:759] **Speaker 0:** That's what we're aiming for.
[00:02:44:600 - 00:02:48:759] **Speaker 0:** Um, OK, well, that then gives us, since there's only
[00:02:48:759 - 00:02:53:179] **Speaker 0:** the, uh, integral constant here, uh, we can state that
[00:02:53:190 - 00:02:56:949] **Speaker 0:** that's since it's equal to one, the J, we're looking
[00:02:56:949 - 00:03:00:860] **Speaker 0:** at the magnitude, OK, so it's just scaling that, um,
[00:03:01:320 - 00:03:04:360] **Speaker 0:** with a with unity, so we just rearrange this to
[00:03:04:369 - 00:03:05:960] **Speaker 0:** to solve for KI.
[00:03:06:830 - 00:03:10:570] **Speaker 0:** And we're left with um what we're choosing by design
[00:03:10:789 - 00:03:13:490] **Speaker 0:** as our our um cutoff frequency.
[00:03:14:470 - 00:03:17:309] **Speaker 0:** The armature resistance, which is just a a factor of
[00:03:17:309 - 00:03:21:589] **Speaker 0:** the motor that we're using and the source voltage from
[00:03:21:589 - 00:03:22:470] **Speaker 0:** our butt converter.
[00:03:27:839 - 00:03:31:509] **Speaker 0:** Um, and then of course we've got the proportional, uh,
[00:03:31:520 - 00:03:35:899] **Speaker 0:** that we can now immediately determine uh what remember back,
[00:03:36:440 - 00:03:38:759] **Speaker 0:** I said we should label equation one because we were
[00:03:38:759 - 00:03:39:720] **Speaker 0:** going to come back to this.
[00:03:40:770 - 00:03:45:589] **Speaker 0:** That's exactly what we utilise, so KP over KI.
[00:03:46:330 - 00:03:48:949] **Speaker 0:** is equal to LA over RA.
[00:03:49:589 - 00:03:53:070] **Speaker 0:** So from this we can then say KP is equal
[00:03:53:070 - 00:03:58:160] **Speaker 0:** to um just LA over RA times the Um, integral
[00:03:58:160 - 00:03:58:589] **Speaker 0:** constant.
[00:03:59:520 - 00:04:03:210] **Speaker 0:** Alright, uh, and that simplifies just the cutoff frequency multiplied
[00:04:03:210 - 00:04:07:470] **Speaker 0:** by now not RA but the inductance of our armature
[00:04:07:649 - 00:04:11:089] **Speaker 0:** divided by the, the voltage of our butt converter, source
[00:04:11:089 - 00:04:12:169] **Speaker 0:** voltage of the butt converter.
[00:04:13:610 - 00:04:19:489] **Speaker 0:** So we've now got specific values for KI and KP
[00:04:19:838 - 00:04:24:640] **Speaker 0:** that are based on um the the uh the actual
[00:04:24:640 - 00:04:29:170] **Speaker 0:** motor that we're utilising to control uh and the voltage
[00:04:29:170 - 00:04:32:200] **Speaker 0:** that our back converter is providing uh is sourced by.
[00:04:34:220 - 00:04:40:179] **Speaker 0:** Right, so by making that, um, that simplification, we've ensured
[00:04:40:179 - 00:04:44:579] **Speaker 0:** that the stability is guaranteed over the entire operating range
[00:04:44:579 - 00:04:49:339] **Speaker 0:** of the control system, uh, and we've also achieved because
[00:04:49:339 - 00:04:52:899] **Speaker 0:** we are going to, um, you know, something around 1/10
[00:04:52:899 - 00:04:56:940] **Speaker 0:** of the switching frequency, that loop control is actually pretty
[00:04:56:940 - 00:04:57:380] **Speaker 0:** fast.
[00:04:57:619 - 00:05:02:019] **Speaker 0:** You're thinking a modest, a modest switching frequency of being
[00:05:02:019 - 00:05:03:600] **Speaker 0:** something like 20 kilohertz.
[00:05:04:350 - 00:05:07:790] **Speaker 0:** Then 1/10 of that is still 2 kilohertz bandwidth for
[00:05:07:790 - 00:05:11:690] **Speaker 0:** our control system just for the torque control of the
[00:05:11:690 - 00:05:12:670] **Speaker 0:** of the motor.
[00:05:13:570 - 00:05:16:970] **Speaker 0:** Right, which is pretty, pretty rapid in in any um
[00:05:16:970 - 00:05:17:809] **Speaker 0:** practical sense.
[00:05:19:269 - 00:05:21:369] **Speaker 0:** Right, that's all well and good.
[00:05:21:950 - 00:05:26:109] **Speaker 0:** We've got uh the ability to design a closed loop
[00:05:26:109 - 00:05:29:910] **Speaker 0:** control system for torque control of our of our motor
[00:05:29:910 - 00:05:31:369] **Speaker 0:** that's driving a mechanical load.
[00:05:33:730 - 00:05:39:940] **Speaker 0:** What if the application does require, um, Speed control, so
[00:05:39:940 - 00:05:43:329] **Speaker 0:** we need to achieve a particular speed for our um
[00:05:43:329 - 00:05:44:000] **Speaker 0:** our load.
[00:05:45:019 - 00:05:47:459] **Speaker 0:** And on top of that, perhaps the load is one
[00:05:47:459 - 00:05:51:660] **Speaker 0:** where it's reaching a particular position and stopping, right, so
[00:05:51:660 - 00:05:55:429] **Speaker 0:** we need position control as well, right, we'll carry on
[00:05:55:429 - 00:05:57:079] **Speaker 0:** and look at those situations.
[00:06:08:869 - 00:06:11:970] **Speaker 0:** So the middle control loop, which is our speed control,
[00:06:12:040 - 00:06:14:890] **Speaker 0:** it's considerably slower than our torque control.
[00:06:16:170 - 00:06:19:470] **Speaker 0:** Remember we're talking about these embedded control loops.
[00:06:19:850 - 00:06:22:029] **Speaker 0:** So here was the original one that we looked at.
[00:06:22:329 - 00:06:26:570] **Speaker 0:** We we've just covered the torque control, now we're going
[00:06:26:570 - 00:06:29:549] **Speaker 0:** into the speed control loop side of things.
[00:06:34:809 - 00:06:40:230] **Speaker 0:** We determined already the inner control loop, what it was
[00:06:40:230 - 00:06:44:640] **Speaker 0:** um based on, uh understanding of course that the um,
[00:06:45:559 - 00:06:48:920] **Speaker 0:** The back EMF changes because that is due to uh
[00:06:48:920 - 00:06:51:839] **Speaker 0:** or slowed down due to the uh the um inertia
[00:06:51:839 - 00:06:54:640] **Speaker 0:** of the system is pretty slow, so that just is
[00:06:54:640 - 00:06:57:600] **Speaker 0:** essentially seen as being a static value uh that didn't
[00:06:57:600 - 00:06:58:959] **Speaker 0:** play in our control loop.
[00:07:00:329 - 00:07:02:709] **Speaker 0:** We had I ordered and I measured.
[00:07:03:170 - 00:07:08:149] **Speaker 0:** If that control system is doing its job, then the
[00:07:08:730 - 00:07:13:649] **Speaker 0:** actual amateur current pretty much equals the ordered ordered current,
[00:07:13:850 - 00:07:14:160] **Speaker 0:** yeah.
[00:07:15:059 - 00:07:17:859] **Speaker 0:** That's the case, then if we now go to the
[00:07:17:859 - 00:07:20:179] **Speaker 0:** outer loop and we consider what the inner loop is
[00:07:20:179 - 00:07:24:100] **Speaker 0:** doing, we can just substitute all of that, all of
[00:07:24:100 - 00:07:26:600] **Speaker 0:** that control system that we were just saying with unity.
[00:07:27:859 - 00:07:32:019] **Speaker 0:** Because the amateur current that's coming out is, if it's
[00:07:32:019 - 00:07:34:480] **Speaker 0:** doing its job, which we've just designed it to do,
[00:07:35:019 - 00:07:38:579] **Speaker 0:** um, it will be equal to the input current, to
[00:07:38:579 - 00:07:39:459] **Speaker 0:** the ordered current.
[00:07:40:100 - 00:07:43:100] **Speaker 0:** So the transfer function of that is just one, just
[00:07:43:100 - 00:07:43:540] **Speaker 0:** unity.
[00:07:48:540 - 00:07:52:239] **Speaker 0:** Now, If we're going to make sure that this next
[00:07:52:239 - 00:07:57:829] **Speaker 0:** loop uh doesn't see what's happening in that central torque
[00:07:57:829 - 00:08:01:230] **Speaker 0:** control loop, um, nothing that's happening in there uh affects
[00:08:01:230 - 00:08:01:829] **Speaker 0:** that control.
[00:08:02:070 - 00:08:05:470] **Speaker 0:** We have to make sure that the bandwidth then of
[00:08:05:470 - 00:08:11:769] **Speaker 0:** our speed controller, um, is outside the dynamic change range
[00:08:11:769 - 00:08:13:260] **Speaker 0:** of the torque control.
[00:08:13:790 - 00:08:17:549] **Speaker 0:** So that means again we take another 10th of the
[00:08:17:549 - 00:08:21:820] **Speaker 0:** frequency for our Bandwidth for the speed control.
[00:08:22:019 - 00:08:25:260] **Speaker 0:** So we've already gone 1/10 of the switching frequency for
[00:08:25:260 - 00:08:27:750] **Speaker 0:** our torque control and then we're going to take that
[00:08:27:750 - 00:08:30:950] **Speaker 0:** torque control bandwidth and take 1/10 of that.
[00:08:31:459 - 00:08:36:179] **Speaker 0:** So from the original switching frequency, we're now 1/100 of
[00:08:36:179 - 00:08:37:179] **Speaker 0:** that frequency.
[00:08:44:869 - 00:08:48:630] **Speaker 0:** We've already determined before that um to to uh go
[00:08:48:630 - 00:08:51:570] **Speaker 0:** from current to torque, we multiply by the motor constant,
[00:08:52:150 - 00:08:54:429] **Speaker 0:** right, this is all being part of it and we
[00:08:54:429 - 00:08:59:309] **Speaker 0:** have a um the motor torque and the difference between
[00:08:59:309 - 00:09:00:719] **Speaker 0:** that is the residual torque.
[00:09:01:330 - 00:09:06:780] **Speaker 0:** Again, this is relatively a static feature compared to um
[00:09:06:869 - 00:09:08:429] **Speaker 0:** what's going on with the speed control.
[00:09:08:750 - 00:09:11:190] **Speaker 0:** So we just say this is the residual, so this
[00:09:11:190 - 00:09:14:270] **Speaker 0:** is um the omega by DT.
[00:09:15:809 - 00:09:19:500] **Speaker 0:** Alright, and to get the speed we integrate that and
[00:09:19:500 - 00:09:22:520] **Speaker 0:** we need to of course look at the um since
[00:09:22:520 - 00:09:25:619] **Speaker 0:** the omega by DT is equal to the torque divided
[00:09:25:619 - 00:09:26:599] **Speaker 0:** by the inertia.
[00:09:30:869 - 00:09:34:669] **Speaker 0:** Alright, to get speed, we integrate this and we take
[00:09:34:669 - 00:09:35:890] **Speaker 0:** 1 over J as well.
[00:09:41:909 - 00:09:45:830] **Speaker 0:** So now we have um the, the, the speed which
[00:09:45:830 - 00:09:49:280] **Speaker 0:** we can remember this is all referred back to the,
[00:09:49:390 - 00:09:50:950] **Speaker 0:** to the motor side which is why we are using
[00:09:50:950 - 00:09:55:549] **Speaker 0:** motor speed rather than the the load speed uh and
[00:09:55:549 - 00:09:57:989] **Speaker 0:** we feed it back and compare it to the ordered
[00:09:57:989 - 00:09:59:650] **Speaker 0:** speed that we are interested in.
[00:10:07:450 - 00:10:09:929] **Speaker 0:** Right, so must make sure it's less than 1/5 of
[00:10:09:929 - 00:10:10:789] **Speaker 0:** the current control.
[00:10:12:349 - 00:10:16:869] **Speaker 0:** For practical purposes we would tend to go for um
[00:10:16:869 - 00:10:17:469] **Speaker 0:** 1/10.
[00:10:25:260 - 00:10:28:780] **Speaker 0:** We need that uh we need um that to integrate,
[00:10:28:820 - 00:10:32:179] **Speaker 0:** but what are we gonna then do for the amateur
[00:10:32:179 - 00:10:32:330] **Speaker 0:** current?
[00:10:32:380 - 00:10:34:640] **Speaker 0:** We've got a PI controller that's been identified.
[00:10:35:299 - 00:10:38:820] **Speaker 0:** Again no differential, things are just not happening fast enough
[00:10:38:820 - 00:10:41:739] **Speaker 0:** for you to worry about how rapidly it reaches that
[00:10:41:739 - 00:10:44:739] **Speaker 0:** um The end state for zero error.
[00:10:46:729 - 00:10:48:640] **Speaker 0:** But thinking about the era.
[00:10:51:599 - 00:10:56:510] **Speaker 0:** If we have The measured speed equaling the ordered speed.
[00:10:57:469 - 00:11:01:130] **Speaker 0:** Then do we expect there to be zero amateur current?
[00:11:02:960 - 00:11:05:179] **Speaker 0:** There still has to be the right armature current that's
[00:11:05:179 - 00:11:09:080] **Speaker 0:** flowing in order to have the motor driving to create
[00:11:09:080 - 00:11:10:619] **Speaker 0:** that right speed for the load.
[00:11:10:929 - 00:11:14:080] **Speaker 0:** OK, so once the error goes to zero, we need
[00:11:14:080 - 00:11:17:719] **Speaker 0:** a residual value to maintain the armature current.
[00:11:17:840 - 00:11:21:159] **Speaker 0:** So absolutely we have to have integral control there and
[00:11:21:159 - 00:11:24:960] **Speaker 0:** once again proportional, make sure that the residual after things
[00:11:24:960 - 00:11:28:359] **Speaker 0:** reach their, their state, um, is, is a small offset.
[00:11:31:020 - 00:11:34:479] **Speaker 0:** So we choose PI control once again for this controller.
[00:11:44:919 - 00:11:50:179] **Speaker 0:** So PI control, it's exactly as we did for the
[00:11:50:179 - 00:11:53:049] **Speaker 0:** for the prior example for the um current control loop.
[00:11:54:289 - 00:11:58:349] **Speaker 0:** KP plus KI over KS and KI over S um
[00:11:58:530 - 00:11:59:690] **Speaker 0:** in pole zero form.
[00:12:09:390 - 00:12:12:109] **Speaker 0:** So to make sure that things are going to be
[00:12:12:109 - 00:12:16:190] **Speaker 0:** appropriate and we can weight properly weight our coefficients or
[00:12:16:190 - 00:12:19:229] **Speaker 0:** a constants there, we look at the open loop gain
[00:12:19:229 - 00:12:20:090] **Speaker 0:** of the system.
[00:12:22:419 - 00:12:26:010] **Speaker 0:** Alright, so for the control system that we've got now.
[00:12:27:549 - 00:12:31:030] **Speaker 0:** We're looking at the open loop, input to output, we've
[00:12:31:030 - 00:12:33:950] **Speaker 0:** got the PI which is just this.
[00:12:35:760 - 00:12:39:760] **Speaker 0:** Unity, so that doesn't factor in, just multiplied by 1
[00:12:40:200 - 00:12:44:039] **Speaker 0:** times K over SJ.
[00:12:46:489 - 00:12:51:059] **Speaker 0:** So OK here, don't forget that's no no um coefficient
[00:12:51:059 - 00:12:54:659] **Speaker 0:** for the for the control, that's just the motor constant.
[00:13:07:200 - 00:13:09:159] **Speaker 0:** Right, so in its pole 0 form it's here.
[00:13:11:570 - 00:13:12:710] **Speaker 0:** So we've got.
[00:13:13:640 - 00:13:15:039] **Speaker 0:** Uh, 1 over S 2.
[00:13:18:409 - 00:13:21:429] **Speaker 0:** If we look in the complex frequency domain, that means,
[00:13:21:450 - 00:13:24:469] **Speaker 0:** or in the frequency domain, that means that we have
[00:13:25:200 - 00:13:29:130] **Speaker 0:** right from DC, there's no cutoff frequency occurring here right
[00:13:29:130 - 00:13:33:190] **Speaker 0:** from DC we have a phase shift of 180 degrees.
[00:13:35:419 - 00:13:38:979] **Speaker 0:** Alright, so that could be quite problematic, because as you
[00:13:38:979 - 00:13:41:630] **Speaker 0:** go up in frequency, the gain comes down, um.
[00:13:42:919 - 00:13:46:919] **Speaker 0:** And there is a real possibility that you can achieve
[00:13:46:919 - 00:13:51:840] **Speaker 0:** a gain magnitude of 1 whilst there is a 180
[00:13:51:840 - 00:13:52:700] **Speaker 0:** degrees phase shift.
[00:13:54:539 - 00:13:56:580] **Speaker 0:** Alright, if the cutoff frequency of our 0 is too
[00:13:56:580 - 00:13:58:799] **Speaker 0:** high, then that can be achieved.
[00:14:01:210 - 00:14:04:090] **Speaker 0:** Right, and I've just kind of hinted there as to
[00:14:04:090 - 00:14:06:770] **Speaker 0:** how we can make sure we at least have a
[00:14:06:770 - 00:14:09:630] **Speaker 0:** reasonable phase margin, which is kind of why I talked
[00:14:09:630 - 00:14:12:650] **Speaker 0:** about it last lecture, we can have a reasonable phase
[00:14:12:650 - 00:14:16:650] **Speaker 0:** margin at the point where the gain magnitude does equal
[00:14:16:650 - 00:14:17:010] **Speaker 0:** 1.
[00:14:19:989 - 00:14:24:989] **Speaker 0:** Alright, so we can make sure that the cutoff frequency
[00:14:24:989 - 00:14:30:229] **Speaker 0:** of our 0 occurs at the point where the gain
[00:14:30:229 - 00:14:31:130] **Speaker 0:** magnitude is 1.
[00:14:33:150 - 00:14:36:710] **Speaker 0:** That will provide a phase margin of 45 degrees.
[00:14:36:830 - 00:14:38:549] **Speaker 0:** Remember, as I was saying that was a target that
[00:14:38:549 - 00:14:41:669] **Speaker 0:** we would quite often aim for, for a for a
[00:14:41:669 - 00:14:46:710] **Speaker 0:** reasonable um good robust to noise phase margin.
[00:14:53:450 - 00:14:56:489] **Speaker 0:** Just to see how we got there, it's probably a
[00:14:56:489 - 00:14:59:900] **Speaker 0:** good idea just to sketch um a a simple bow
[00:14:59:900 - 00:15:02:849] **Speaker 0:** plot that shows what we, what we're aiming for with
[00:15:02:849 - 00:15:03:349] **Speaker 0:** this.
[00:15:05:510 - 00:15:07:090] **Speaker 0:** So we've got gain and phase.
[00:15:12:299 - 00:15:17:250] **Speaker 0:** So log scale for the um for the uh frequency,
[00:15:17:789 - 00:15:19:950] **Speaker 0:** and we're going to look at the magnitude of gain
[00:15:19:950 - 00:15:20:690] **Speaker 0:** and DB.
[00:15:22:590 - 00:15:25:070] **Speaker 0:** We're also going to uh consider phase.
[00:15:30:840 - 00:15:34:440] **Speaker 0:** I'll, I'll, I'll keep the same horizontal axis axis for
[00:15:34:440 - 00:15:38:359] **Speaker 0:** the frequency and we're gonna have phase, um, and we'll
[00:15:38:359 - 00:15:39:940] **Speaker 0:** start here at -90.
[00:15:40:940 - 00:15:45:460] **Speaker 0:** Go to -135, I'll show why we're looking at that
[00:15:45:460 - 00:15:49:099] **Speaker 0:** shortly and minus 180.
[00:15:52:880 - 00:15:56:880] **Speaker 0:** OK, so for 2 polls, where we got it going
[00:15:56:880 - 00:15:59:650] **Speaker 0:** from DC we have this.
[00:16:01:010 - 00:16:07:580] **Speaker 0:** Vertical, well, a linear slope for our, Gain, which is
[00:16:07:580 - 00:16:09:799] **Speaker 0:** reducing at -40 dB per decade.
[00:16:17:239 - 00:16:20:940] **Speaker 0:** Then we have, we reached the cutoff frequency of the
[00:16:21:159 - 00:16:21:719] **Speaker 0:** um.
[00:16:22:700 - 00:16:23:809] **Speaker 0:** Of their 0.
[00:16:27:330 - 00:16:30:559] **Speaker 0:** As soon as that happens, the effect of the zero
[00:16:30:789 - 00:16:35:219] **Speaker 0:** kicks in and it reduces that that decay from -40
[00:16:35:219 - 00:16:38:710] **Speaker 0:** dB per decade to there's still going to since it's
[00:16:38:710 - 00:16:39:150] **Speaker 0:** um.
[00:16:39:859 - 00:16:42:570] **Speaker 0:** A double pole and then you've got a 0 that
[00:16:42:570 - 00:16:45:830] **Speaker 0:** will come to -20 dB per decade.
[00:16:53:039 - 00:16:54:359] **Speaker 0:** Because, of course.
[00:16:54:989 - 00:16:56:900] **Speaker 0:** If we look at the um.
[00:16:59:159 - 00:17:00:739] **Speaker 0:** What's going on with the 0.
[00:17:02:250 - 00:17:06:250] **Speaker 0:** Comes along And it's gain goes like that at omega
[00:17:06:250 - 00:17:06:550] **Speaker 0:** C.
[00:17:10:319 - 00:17:11:979] **Speaker 0:** And it's face.
[00:17:16:078 - 00:17:26:989] **Speaker 0:** It goes 0 degrees Whoops That's 1/10 omega C oops.
[00:17:31:130 - 00:17:34:630] **Speaker 0:** Omega C 1/10 is omega C.
[00:17:35:560 - 00:17:37:619] **Speaker 0:** And 10 omega C.
[00:17:39:380 - 00:17:40:979] **Speaker 0:** So it goes from 0 degrees.
[00:17:47:609 - 00:17:49:729] **Speaker 0:** And then at 10 times it's at.
[00:17:50:520 - 00:17:51:500] **Speaker 0:** 90 degrees.
[00:17:54:250 - 00:17:54:640] **Speaker 0:** Yeah.
[00:17:57:130 - 00:17:59:410] **Speaker 0:** For the phase of a single 0.
[00:18:00:910 - 00:18:04:060] **Speaker 0:** So that's what you're adding to the to the double
[00:18:04:060 - 00:18:06:380] **Speaker 0:** pole that we have, so which is why you got
[00:18:06:380 - 00:18:10:060] **Speaker 0:** 20 dB per decade, um adding to minus 40.
[00:18:12:609 - 00:18:14:020] **Speaker 0:** What's going on with the phase?
[00:18:14:349 - 00:18:17:500] **Speaker 0:** OK, well, let's start from DC at -180.
[00:18:21:550 - 00:18:25:849] **Speaker 0:** Then you, as soon as you get to Omega C
[00:18:27:410 - 00:18:34:199] **Speaker 0:** Over 10 And then 10 omega C, it increases.
[00:18:36:979 - 00:18:39:810] **Speaker 0:** At 45 degrees per per decade.
[00:18:41:209 - 00:18:48:390] **Speaker 0:** Oops It goes to 90.
[00:18:48:689 - 00:18:49:829] **Speaker 0:** So this midpoint.
[00:18:50:719 - 00:18:54:239] **Speaker 0:** At omega C, we have a phase margin.
[00:19:01:430 - 00:19:02:699] **Speaker 0:** Of 45 degrees.
[00:19:05:709 - 00:19:09:560] **Speaker 0:** Alright, so we just need to design our controller to
[00:19:09:560 - 00:19:12:920] **Speaker 0:** make sure that the cutoff frequency of our zero there
[00:19:12:920 - 00:19:17:800] **Speaker 0:** is at um the right uh right at when the
[00:19:17:800 - 00:19:19:260] **Speaker 0:** gain is equal to 1.
[00:19:22:630 - 00:19:24:770] **Speaker 0:** So we've got our open loop gain expression.
[00:19:25:729 - 00:19:28:010] **Speaker 0:** Here and we're saying we want that to be equal
[00:19:28:010 - 00:19:31:449] **Speaker 0:** to one right at the cutoff frequency.
[00:19:35:349 - 00:19:37:910] **Speaker 0:** At the cutoff frequency, we need to have that, if
[00:19:37:910 - 00:19:40:229] **Speaker 0:** it's the gain is equal to 1, that means that
[00:19:40:229 - 00:19:43:469] **Speaker 0:** we must have the phase margin equal to 45 degrees.
[00:19:44:680 - 00:19:48:619] **Speaker 0:** This expression for the phase angle to be 45 degrees,
[00:19:49:160 - 00:19:51:479] **Speaker 0:** we must have a mega.
[00:19:52:400 - 00:19:57:030] **Speaker 0:** KP Over KI is equal to 1.
[00:19:58:020 - 00:20:02:699] **Speaker 0:** We need to make The the real and the imaginary
[00:20:02:699 - 00:20:05:579] **Speaker 0:** part of this expression equal to each other in magnitude.
[00:20:06:780 - 00:20:09:000] **Speaker 0:** For a 45 degree angle, does that make sense?
[00:20:09:300 - 00:20:11:989] **Speaker 0:** You've got your imaginary reel playing.
[00:20:14:630 - 00:20:19:550] **Speaker 0:** Alright, we've got unity for the imaginary unity, so that's
[00:20:19:550 - 00:20:21:270] **Speaker 0:** one and one.
[00:20:27:760 - 00:20:30:709] **Speaker 0:** So the angle here will be 45 degrees.
[00:20:31:170 - 00:20:32:989] **Speaker 0:** So that's the phase angle that we are trying to
[00:20:33:290 - 00:20:34:510] **Speaker 0:** make sure is occurring.
[00:20:35:050 - 00:20:37:979] **Speaker 0:** So For these to be equal, we've already got one
[00:20:37:979 - 00:20:40:479] **Speaker 0:** here for the real, the imaginary part has to be
[00:20:40:479 - 00:20:43:979] **Speaker 0:** equal to 1, alright, so here we've got 1 plus
[00:20:43:979 - 00:20:47:319] **Speaker 0:** J1, to give us our phase angle of 45 degrees
[00:20:47:619 - 00:20:50:300] **Speaker 0:** when the magnitude is equal to 1.
[00:20:51:630 - 00:20:55:239] **Speaker 0:** And so we're forcing these to be uh the result
[00:20:55:239 - 00:20:58:339] **Speaker 0:** of the weightings from our coefficients.
[00:21:02:310 - 00:21:04:209] **Speaker 0:** So if you take that then you end up with
[00:21:04:209 - 00:21:07:380] **Speaker 0:** route 2 because what is the uh magnitude of this
[00:21:07:380 - 00:21:09:979] **Speaker 0:** when that's 1 and that's 1, well that's route 2,
[00:21:10:400 - 00:21:11:800] **Speaker 0:** that's where the route 2 comes from.
[00:21:17:579 - 00:21:20:319] **Speaker 0:** So we're left with the motor constant.
[00:21:21:250 - 00:21:26:609] **Speaker 0:** The Integral constant The overall inertia of the system.
[00:21:27:640 - 00:21:30:459] **Speaker 0:** Uh, and the cutoff frequency that we've chosen by design.
[00:21:36:729 - 00:21:41:270] **Speaker 0:** OK Uh, and that cutoff frequency being 1/10 of the
[00:21:41:270 - 00:21:44:869] **Speaker 0:** frequency of our control, uh, current control loop.
[00:21:50:609 - 00:21:57:079] **Speaker 0:** which gives That all important integral time uh integral constant.
[00:21:58:089 - 00:22:00:119] **Speaker 0:** Equal to the inertia.
[00:22:01:260 - 00:22:02:619] **Speaker 0:** Omega C squared.
[00:22:04:260 - 00:22:07:560] **Speaker 0:** Over route 2 times the motor constant K.
[00:22:14:550 - 00:22:17:589] **Speaker 0:** Alright, so we've, we've met the conditions that we need
[00:22:17:589 - 00:22:22:150] **Speaker 0:** for this nice phase margin of 45 degrees for our
[00:22:22:150 - 00:22:22:900] **Speaker 0:** speed control.
[00:22:23:150 - 00:22:26:209] **Speaker 0:** We've just left now what is our proportional constant.
[00:22:50:479 - 00:22:53:579] **Speaker 0:** Well, we've already got an expression which relates the proportional
[00:22:53:829 - 00:22:55:900] **Speaker 0:** to the um integral constant.
[00:23:02:910 - 00:23:07:189] **Speaker 0:** So falls out quite nicely here that our um proportional
[00:23:07:189 - 00:23:09:689] **Speaker 0:** constant is just equal to the integral divided by the
[00:23:09:869 - 00:23:12:469] **Speaker 0:** cutoff frequency of our speed control loop.
[00:23:23:229 - 00:23:27:040] **Speaker 0:** Alright, and since that integral control was omega squared, then
[00:23:27:040 - 00:23:29:760] **Speaker 0:** dividing it by omega would just take out the squared.
[00:23:33:060 - 00:23:35:900] **Speaker 0:** So we've naturally chosen that cutoff frequency to be less
[00:23:35:900 - 00:23:41:390] **Speaker 0:** than 1/5, probably 1/10 of the current control bandwidth or
[00:23:41:390 - 00:23:44:459] **Speaker 0:** 1/100 now of our switching frequency.
[00:23:49:000 - 00:23:51:719] **Speaker 0:** Alright, so now we've, we've got that condition right.
[00:23:52:000 - 00:23:54:760] **Speaker 0:** We're gonna have stable because we've got that nice phase
[00:23:54:760 - 00:24:00:599] **Speaker 0:** margin of 45 degrees, um, and it's reasonably fast because
[00:24:00:609 - 00:24:05:329] **Speaker 0:** we've chosen a bandwidth which is not ridiculously small, um,
[00:24:05:520 - 00:24:09:300] **Speaker 0:** but allows us to adjust the, the, um, the speed
[00:24:09:300 - 00:24:11:060] **Speaker 0:** of our uh our motor.
[00:24:12:000 - 00:24:14:050] **Speaker 0:** Pretty quickly to get to that final state that we're
[00:24:14:050 - 00:24:14:869] **Speaker 0:** aiming for.
[00:24:18:520 - 00:24:22:199] **Speaker 0:** Right, one more control loop then to to consider, that's
[00:24:22:199 - 00:24:23:459] **Speaker 0:** the position control.
[00:24:25:339 - 00:24:28:280] **Speaker 0:** Yeah, I'm talking about these other control loops, but of
[00:24:28:280 - 00:24:32:630] **Speaker 0:** course the particular application may not require position control, right?
[00:24:32:900 - 00:24:35:989] **Speaker 0:** A lot of applications actually wouldn't require position control.
[00:24:36:199 - 00:24:39:469] **Speaker 0:** You might need speed, speed is quite common for a
[00:24:39:469 - 00:24:43:670] **Speaker 0:** for a control um Condition, but position is pretty specialised,
[00:24:44:250 - 00:24:44:400] **Speaker 0:** right?
[00:24:44:530 - 00:24:47:270] **Speaker 0:** So if it's not necessary, you don't need to design
[00:24:47:270 - 00:24:49:270] **Speaker 0:** that particular control loop, you're finished.
[00:24:50:520 - 00:24:52:479] **Speaker 0:** If you've already got your speed control and that's what
[00:24:52:479 - 00:24:53:739] **Speaker 0:** the application requires.
[00:24:55:150 - 00:24:57:979] **Speaker 0:** But perhaps we're just going through the whole process here.
[00:24:58:410 - 00:25:01:390] **Speaker 0:** Perhaps the application does need position control, right?
[00:25:01:510 - 00:25:04:609] **Speaker 0:** So you need to have already done your thought controller
[00:25:04:829 - 00:25:08:109] **Speaker 0:** and your speed controller, they, they're embedded now within the
[00:25:08:109 - 00:25:11:849] **Speaker 0:** system to enable us to have a position control.
[00:25:14:579 - 00:25:17:050] **Speaker 0:** So The slowest control loop.
[00:25:17:959 - 00:25:21:420] **Speaker 0:** Um, we need that, uh, if it's going to function
[00:25:21:719 - 00:25:24:599] **Speaker 0:** as we intend, we need to do a reduction in
[00:25:24:599 - 00:25:29:680] **Speaker 0:** the bandwidth again, um, this 1/5 but probably more practically
[00:25:29:680 - 00:25:30:400] **Speaker 0:** around 1/10.
[00:25:43:209 - 00:25:44:849] **Speaker 0:** Alright, so by the time you're getting to here, if
[00:25:44:849 - 00:25:48:469] **Speaker 0:** you're taking it 1/10, 1/10, 1/10, you're now at 1000
[00:25:48:670 - 00:25:52:180] **Speaker 0:** of the um switching frequency that we had.
[00:25:52:609 - 00:25:56:089] **Speaker 0:** So that's still when you think, you know, you might
[00:25:56:089 - 00:25:59:569] **Speaker 0:** have been switching at 20 kilohertz, that's still 200 Hz.
[00:26:00:560 - 00:26:04:150] **Speaker 0:** Bandwidth for our control of of uh a mechanical load
[00:26:04:150 - 00:26:06:369] **Speaker 0:** that we're trying to reach a particular position.
[00:26:08:599 - 00:26:13:880] **Speaker 0:** Most often for any reasonable level of, um, I guess,
[00:26:14:599 - 00:26:20:020] **Speaker 0:** energy being involved, 200 Hz for positioning something rotationally, uh,
[00:26:20:040 - 00:26:21:079] **Speaker 0:** is pretty quick.
[00:26:22:520 - 00:26:27:189] **Speaker 0:** So it may sound like this is very slow, 200
[00:26:27:189 - 00:26:30:010] **Speaker 0:** Hz in the real world when you're rotating something and
[00:26:30:010 - 00:26:33:150] **Speaker 0:** getting it to go to a particular position is still
[00:26:33:150 - 00:26:34:069] **Speaker 0:** very fast.
[00:26:39:760 - 00:26:41:750] **Speaker 0:** So what does the control system look like now?
[00:26:44:329 - 00:26:47:239] **Speaker 0:** Well, once again, if we've done our job right for
[00:26:47:239 - 00:26:53:310] **Speaker 0:** our embedded earlier control loops, talk and speed now, um,
[00:26:53:319 - 00:26:56:439] **Speaker 0:** then The actual speed.
[00:26:57:280 - 00:27:01:239] **Speaker 0:** That we have should equal the ordered speed.
[00:27:02:689 - 00:27:06:780] **Speaker 0:** Alright, so again, that all of that that uh stuff
[00:27:06:780 - 00:27:09:219] **Speaker 0:** that we've done before with the with the control systems,
[00:27:09:660 - 00:27:13:099] **Speaker 0:** it just evolves down to being equal to unity as
[00:27:13:099 - 00:27:15:060] **Speaker 0:** far as the out of control loop is concerned.
[00:27:17:209 - 00:27:21:140] **Speaker 0:** But we do need to go from speed to position.
[00:27:23:510 - 00:27:27:910] **Speaker 0:** Alright, but speed is just the, the time integral of
[00:27:27:910 - 00:27:28:430] **Speaker 0:** position.
[00:27:30:790 - 00:27:36:010] **Speaker 0:** All right, so Omega equals the theta by DT.
[00:27:39:469 - 00:27:41:979] **Speaker 0:** So if we're going to get speed, we just integrate,
[00:27:42:420 - 00:27:44:420] **Speaker 0:** sorry, if we're gonna get position, we just integrate speed.
[00:27:46:130 - 00:27:47:589] **Speaker 0:** Alright, so you've got the one over S.
[00:27:48:640 - 00:27:49:479] **Speaker 0:** For the integrator.
[00:27:50:219 - 00:27:53:459] **Speaker 0:** Uh, then we have the measured position, usually through some
[00:27:53:459 - 00:27:56:579] **Speaker 0:** sort of rotary encoder, alright, and we compare that to
[00:27:56:579 - 00:27:57:500] **Speaker 0:** the ordered position.
[00:28:00:010 - 00:28:06:199] **Speaker 0:** We're left with an error So, if we've reached the
[00:28:06:199 - 00:28:07:599] **Speaker 0:** position we've ordered.
[00:28:08:680 - 00:28:12:000] **Speaker 0:** Do we want the motor to be still rotating?
[00:28:12:939 - 00:28:14:859] **Speaker 0:** No, we want it to stop.
[00:28:15:260 - 00:28:17:839] **Speaker 0:** So if we've got 0 error, we want 0 speed.
[00:28:18:540 - 00:28:21:459] **Speaker 0:** OK, this is the first instance where all we need
[00:28:21:459 - 00:28:22:839] **Speaker 0:** is a proportional controller.
[00:28:23:430 - 00:28:25:800] **Speaker 0:** We don't need integral control, we don't need a residual.
[00:28:26:810 - 00:28:29:630] **Speaker 0:** At all for a zero error condition.
[00:28:29:829 - 00:28:33:150] **Speaker 0:** We want there to be zero speed when there's zero
[00:28:33:150 - 00:28:33:689] **Speaker 0:** error.
[00:28:35:300 - 00:28:39:380] **Speaker 0:** All right, so Simples of the uh of the controllers
[00:28:39:380 - 00:28:41:239] **Speaker 0:** so far, just proportional.
[00:28:45:449 - 00:28:49:849] **Speaker 0:** So, we look at the open loop game, KP over
[00:28:49:849 - 00:28:51:709] **Speaker 0:** S, it's it's quite simple.
[00:28:53:469 - 00:28:57:430] **Speaker 0:** Uh, 1 overs, the, the worst you can get is
[00:28:57:430 - 00:28:59:109] **Speaker 0:** -90 degrees phase shift.
[00:28:59:390 - 00:29:02:599] **Speaker 0:** Well, it's -90 degrees from DC, right.
[00:29:04:989 - 00:29:06:189] **Speaker 0:** That's not gonna go unstable.
[00:29:06:989 - 00:29:08:050] **Speaker 0:** For all frequencies.
[00:29:09:329 - 00:29:11:050] **Speaker 0:** Right, so we don't need to do any kind of
[00:29:11:050 - 00:29:12:369] **Speaker 0:** special substitution.
[00:29:12:410 - 00:29:14:109] **Speaker 0:** There's nothing to substitute in there anyway.
[00:29:14:489 - 00:29:17:569] **Speaker 0:** Um, so the gain is just KP overs.
[00:29:26:329 - 00:29:29:709] **Speaker 0:** Right, so at the bandwidth that we want to choose
[00:29:29:709 - 00:29:33:339] **Speaker 0:** by design, you know, 1/10 of the speed, uh, bandwidth.
[00:29:34:250 - 00:29:36:890] **Speaker 0:** Make that at that frequency, the gain is equal to
[00:29:36:890 - 00:29:40:489] **Speaker 0:** 1, so the magnitude of KP over omega C is
[00:29:40:489 - 00:29:41:229] **Speaker 0:** equal to 1.
[00:29:42:359 - 00:29:49:130] **Speaker 0:** So The magnitude or of our proportional constant is just
[00:29:49:130 - 00:29:50:410] **Speaker 0:** equal to the cutoff frequency.
[00:29:54:560 - 00:29:55:319] **Speaker 0:** Nice and simple.
[00:29:56:510 - 00:29:57:310] **Speaker 0:** And that's it.
[00:29:57:390 - 00:29:57:869] **Speaker 0:** We're, we're done.
[00:29:57:920 - 00:30:00:459] **Speaker 0:** We've done all three embedded feedback loops.
[00:30:00:510 - 00:30:06:739] **Speaker 0:** We've got coefficients that will work for nice, very stable
[00:30:06:739 - 00:30:10:260] **Speaker 0:** operation that is fast enough for our op.
[00:30:10:459 - 00:30:11:869] **Speaker 0:** It's not optimised for speed.
[00:30:12:099 - 00:30:14:430] **Speaker 0:** It's not optimised for potential overshoots and things like that,
[00:30:14:550 - 00:30:16:270] **Speaker 0:** but it is fast and stable.
[00:30:20:859 - 00:30:22:189] **Speaker 0:** The solar car.
[00:30:23:609 - 00:30:27:089] **Speaker 0:** Right, it's a little different, right, we're not per se,
[00:30:27:400 - 00:30:28:839] **Speaker 0:** controlling the motor.
[00:30:29:530 - 00:30:32:219] **Speaker 0:** At all, we're controlling the solar panel.
[00:30:33:589 - 00:30:37:219] **Speaker 0:** So what does that mean for us and the project?
[00:30:43:810 - 00:30:47:189] **Speaker 0:** Well, the system kind of effectively looks like.
[00:30:47:890 - 00:30:56:400] **Speaker 0:** The panel The buck converter And the motor.
[00:30:59:849 - 00:31:02:060] **Speaker 0:** I know there's a gearbox and stuff, but we're we're
[00:31:02:060 - 00:31:05:000] **Speaker 0:** just looking at power flow from the panel.
[00:31:06:439 - 00:31:08:680] **Speaker 0:** To the back converter and then from the back converter
[00:31:08:680 - 00:31:09:400] **Speaker 0:** to the motor.
[00:31:12:109 - 00:31:13:729] **Speaker 0:** We've got our TL 494.
[00:31:19:400 - 00:31:24:050] **Speaker 0:** Alright, and it's a controller IC, it's a controller chip.
[00:31:24:209 - 00:31:28:010] **Speaker 0:** So something to do with that is going to enable
[00:31:28:010 - 00:31:29:729] **Speaker 0:** us to have our controller in there.
[00:31:32:449 - 00:31:36:489] **Speaker 0:** We're going with for this to work, we're trying to
[00:31:36:489 - 00:31:40:109] **Speaker 0:** get maximum power from the solar panel at all times,
[00:31:40:609 - 00:31:45:050] **Speaker 0:** and we've determined that the maximum power point is defined
[00:31:45:050 - 00:31:49:900] **Speaker 0:** by a for given light conditions at a specific, what?
[00:31:52:760 - 00:31:55:569] **Speaker 0:** Defined it what a a a a voltage current?
[00:31:59:349 - 00:32:01:780] **Speaker 0:** For the solar car, what are we aiming to control
[00:32:02:439 - 00:32:03:219] **Speaker 0:** for the panel?
[00:32:04:099 - 00:32:04:839] **Speaker 0:** Voltage.
[00:32:05:339 - 00:32:07:859] **Speaker 0:** We've determined that maximum power point is at a particular
[00:32:07:859 - 00:32:10:829] **Speaker 0:** voltage for certain light conditions that we might have.
[00:32:11:260 - 00:32:11:660] **Speaker 0:** Right.
[00:32:12:349 - 00:32:15:449] **Speaker 0:** So, we measure the voltage.
[00:32:21:020 - 00:32:25:930] **Speaker 0:** And We compare that to an ordered voltage.
[00:32:29:579 - 00:32:32:459] **Speaker 0:** So the audit voltage is what we want, what we're
[00:32:32:459 - 00:32:36:540] **Speaker 0:** stating is the controlled value of the control of the
[00:32:36:540 - 00:32:37:140] **Speaker 0:** solar panel.
[00:32:39:319 - 00:32:43:810] **Speaker 0:** Alright, which then feeds into our TL 494 as an
[00:32:43:810 - 00:32:44:349] **Speaker 0:** error.
[00:32:50:520 - 00:32:53:859] **Speaker 0:** The buck converter from the TL 494 is being controlled
[00:32:53:859 - 00:32:55:420] **Speaker 0:** by changing duty ratio.
[00:33:00:699 - 00:33:03:099] **Speaker 0:** Let's say the control system that's set up is doing
[00:33:03:099 - 00:33:08:780] **Speaker 0:** its job, so that the measured voltage is equal to
[00:33:08:780 - 00:33:11:500] **Speaker 0:** our ordered voltage, so the error goes to zero.
[00:33:11:609 - 00:33:13:560] **Speaker 0:** Does that mean that we have zero duty ratio?
[00:33:15:869 - 00:33:18:670] **Speaker 0:** No, we need to maintain the exact duty ratio that
[00:33:18:670 - 00:33:21:550] **Speaker 0:** we've just had to in order for that voltage to
[00:33:21:550 - 00:33:22:189] **Speaker 0:** stay constant.
[00:33:23:310 - 00:33:25:750] **Speaker 0:** So we need the duty ratio to be there with
[00:33:25:750 - 00:33:31:189] **Speaker 0:** zero error that immediately tells us we need Integral control,
[00:33:31:290 - 00:33:33:089] **Speaker 0:** absolutely, so there's the eye.
[00:33:35:219 - 00:33:36:229] **Speaker 0:** Do we need proportional?
[00:33:36:390 - 00:33:39:089] **Speaker 0:** Well, we can have proportional there as well.
[00:33:43:109 - 00:33:46:430] **Speaker 0:** The system dynamics are actually really slow for the solar
[00:33:46:430 - 00:33:47:170] **Speaker 0:** car assignment.
[00:33:47:910 - 00:33:51:479] **Speaker 0:** Um, the motor torque, uh, and speed changes are pretty
[00:33:51:479 - 00:33:54:359] **Speaker 0:** slow in the, in the grand scheme of things, and
[00:33:54:359 - 00:33:57:599] **Speaker 0:** certainly the light conditions are almost completely constant.
[00:34:00:709 - 00:34:03:479] **Speaker 0:** OK, so we're trying to control the voltage on the
[00:34:03:479 - 00:34:04:020] **Speaker 0:** panel.
[00:34:04:800 - 00:34:07:000] **Speaker 0:** And you're going to choose a bandwidth that makes the
[00:34:07:000 - 00:34:09:780] **Speaker 0:** rest of the system look relatively static.
[00:34:11:289 - 00:34:14:377] **Speaker 0:** Alright, or non-dynamic, so that we are only tracking the
[00:34:14:377 - 00:34:16:479] **Speaker 0:** very slow changes in that solar panel.
[00:34:21:060 - 00:34:23:820] **Speaker 0:** The the motor or the the cart is going to
[00:34:23:820 - 00:34:26:360] **Speaker 0:** be driving along a relatively smooth surface.
[00:34:27:398 - 00:34:31:520] **Speaker 0:** Alright, the light conditions unless it's storming at the time,
[00:34:31:570 - 00:34:34:709] **Speaker 0:** which we probably won't be running the assessment then, um,
[00:34:35:370 - 00:34:37:408] **Speaker 0:** so the light conditions are going to be relatively constant
[00:34:37:408 - 00:34:41:330] **Speaker 0:** over the time period of the race, so that's not
[00:34:41:330 - 00:34:42:370] **Speaker 0:** going to be really changing much.
[00:34:42:610 - 00:34:45:030] **Speaker 0:** The, the, the sort of disturbance that you might get,
[00:34:45:090 - 00:34:48:439] **Speaker 0:** uh, is a little bit of, uh, I guess, um,
[00:34:48:610 - 00:34:51:830] **Speaker 0:** irregularity in the surface that the car is running over.
[00:34:52:928 - 00:34:55:329] **Speaker 0:** If you don't want your control system to react to
[00:34:55:329 - 00:34:55:789] **Speaker 0:** that.
[00:34:56:117 - 00:34:58:329] **Speaker 0:** It's gonna be a tiny smaller amount of disturbance, you
[00:34:58:329 - 00:35:01:188] **Speaker 0:** just want the solar panel voltage to be maintained constant.
[00:35:03:659 - 00:35:04:139] **Speaker 0:** Right.
[00:35:07:610 - 00:35:09:770] **Speaker 0:** So we've already covered what kind of control we're going
[00:35:09:770 - 00:35:10:209] **Speaker 0:** to implement.
[00:35:10:290 - 00:35:13:209] **Speaker 0:** It's going to be, uh, on the face of it
[00:35:13:209 - 00:35:15:459] **Speaker 0:** looking like uh PI control.
[00:35:15:729 - 00:35:18:149] **Speaker 0:** Definitely, uh, integral as being part of it.
[00:35:25:479 - 00:35:31:090] **Speaker 0:** So we've got PI But as I've described it, um,
[00:35:31:159 - 00:35:32:280] **Speaker 0:** the dynamics.
[00:35:35:870 - 00:35:37:110] **Speaker 0:** Are so slow.
[00:35:38:850 - 00:35:41:489] **Speaker 0:** We, we don't, we don't actually need to think about
[00:35:41:489 - 00:35:45:790] **Speaker 0:** designing to, to um employ proportional control.
[00:35:58:709 - 00:36:01:669] **Speaker 0:** It's inherent within the system, uh, as far as the
[00:36:01:669 - 00:36:05:830] **Speaker 0:** gain is concerned, so we don't even need to worry
[00:36:05:830 - 00:36:09:580] **Speaker 0:** about a, um, A constant for proportional control.
[00:36:09:659 - 00:36:12:080] **Speaker 0:** We absolutely do need integral control though.
[00:36:13:820 - 00:36:14:860] **Speaker 0:** So how are we going to do it?
[00:36:15:060 - 00:36:20:679] **Speaker 0:** How are we going to actually Take our TL 494
[00:36:20:679 - 00:36:24:870] **Speaker 0:** and make it, An integral controller for this, for this
[00:36:24:870 - 00:36:25:610] **Speaker 0:** assessment.
[00:36:26:189 - 00:36:29:969] **Speaker 0:** Well, There is a reason at the input of the
[00:36:29:969 - 00:36:32:830] **Speaker 0:** TL 494, it says that it has an error amplifier.
[00:36:34:020 - 00:36:35:760] **Speaker 0:** Alright, so we've got this op amp.
[00:36:36:649 - 00:36:40:149] **Speaker 0:** At the input of the TL 494.
[00:36:44:610 - 00:36:46:060] **Speaker 0:** Alright, the error amplifier.
[00:36:52:120 - 00:36:54:479] **Speaker 0:** And what we're going to do is we're going to
[00:36:54:479 - 00:36:55:959] **Speaker 0:** use the OPAM.
[00:36:57:149 - 00:37:04:050] **Speaker 0:** Uh, differential input function to do the job of Our
[00:37:04:050 - 00:37:07:909] **Speaker 0:** error amplifier or error that that we've got here.
[00:37:08:500 - 00:37:11:030] **Speaker 0:** So plus minus and the error, we're gonna use the
[00:37:11:030 - 00:37:12:290] **Speaker 0:** error amplifier for that.
[00:37:13:800 - 00:37:15:969] **Speaker 0:** The PI then.
[00:37:17:040 - 00:37:19:000] **Speaker 0:** Combines with the error amplifier.
[00:37:19:840 - 00:37:22:439] **Speaker 0:** So we're going to have, how do you make an
[00:37:22:439 - 00:37:23:780] **Speaker 0:** integrator with an op amp.
[00:37:24:570 - 00:37:25:909] **Speaker 0:** You put a capacitor.
[00:37:27:169 - 00:37:41:939] **Speaker 0:** In the feedback loop So this Is your on the
[00:37:41:939 - 00:37:44:280] **Speaker 0:** inverting input is your solar panel.
[00:37:45:389 - 00:37:50:320] **Speaker 0:** Voltage It's gonna have to be scaled down through a
[00:37:50:320 - 00:37:51:379] **Speaker 0:** voltage divider.
[00:37:54:989 - 00:37:55:189] **Speaker 0:** Right.
[00:37:56:280 - 00:37:58:139] **Speaker 0:** And then on this side.
[00:37:58:949 - 00:38:00:449] **Speaker 0:** You've got your ordered voltage.
[00:38:05:219 - 00:38:09:540] **Speaker 0:** Which you will utilise because the TL 494 is expecting
[00:38:09:540 - 00:38:15:179] **Speaker 0:** you to, to need a, a reference for ordered voltage.
[00:38:15:620 - 00:38:17:719] **Speaker 0:** It provides a voltage reference.
[00:38:18:219 - 00:38:20:979] **Speaker 0:** So use your TL 494 v ref.
[00:38:24:729 - 00:38:25:800] **Speaker 0:** Which is 5 volts.
[00:38:26:870 - 00:38:30:909] **Speaker 0:** Alright, so you take your panel voltage, which, Depending on
[00:38:30:909 - 00:38:33:110] **Speaker 0:** the light conditions of the day, it could be 17
[00:38:33:110 - 00:38:34:199] **Speaker 0:** volts or so.
[00:38:34:629 - 00:38:36:750] **Speaker 0:** You need to use a voltage divider to bring it
[00:38:36:750 - 00:38:38:770] **Speaker 0:** down to 5 volts.
[00:38:39:649 - 00:38:42:929] **Speaker 0:** So you're comparing 5 volts with 5 volts essentially at
[00:38:42:929 - 00:38:45:729] **Speaker 0:** the, but of course you want some sort of ability
[00:38:45:729 - 00:38:50:409] **Speaker 0:** to adjust your voltage divider for different light conditions, so
[00:38:50:409 - 00:38:52:989] **Speaker 0:** different set values of panel voltage.
[00:38:54:639 - 00:38:57:280] **Speaker 0:** Alright, so, but how do we know that we're gonna
[00:38:57:280 - 00:39:01:080] **Speaker 0:** get the right, um, values of C and R?
[00:39:02:290 - 00:39:22:060] **Speaker 0:** Well, Has an integral time constant, the circuit of TI
[00:39:22:060 - 00:39:23:620] **Speaker 0:** equals R1C.
[00:39:27:330 - 00:39:32:750] **Speaker 0:** So this all important KI Is one over.
[00:39:33:879 - 00:39:34:840] **Speaker 0:** The time constant.
[00:39:36:300 - 00:39:38:939] **Speaker 0:** And that's just equal to 1 over R1C.
[00:39:45:159 - 00:39:46:850] **Speaker 0:** What are we aiming for a time constant?
[00:39:54:260 - 00:40:12:179] **Speaker 0:** It's very slow And what works well is something in
[00:40:12:179 - 00:40:15:040] **Speaker 0:** the range of 0.1 to 0.5 seconds.
[00:40:34:820 - 00:40:38:540] **Speaker 0:** I've seen examples of people coming along with a designed
[00:40:38:540 - 00:40:42:879] **Speaker 0:** um time constant of 0.01 seconds.
[00:40:43:379 - 00:40:47:419] **Speaker 0:** Um, there are usually issues with stability because of that.
[00:40:48:510 - 00:40:51:719] **Speaker 0:** Um This is perfectly fine.
[00:40:52:340 - 00:40:56:939] **Speaker 0:** If you decide that the behaviour of your um controller
[00:40:56:939 - 00:41:04:439] **Speaker 0:** isn't uh providing a close enough um Measured panel voltage
[00:41:04:439 - 00:41:05:209] **Speaker 0:** to ordered.
[00:41:06:060 - 00:41:09:479] **Speaker 0:** Then you can introduce some proportional control as well.
[00:41:10:100 - 00:41:11:219] **Speaker 0:** Uh, how do we do that?
[00:41:11:459 - 00:41:15:510] **Speaker 0:** Well then you would introduce A resistor here.
[00:41:17:169 - 00:41:20:229] **Speaker 0:** And if you want to have proportional control, KP is
[00:41:20:229 - 00:41:22:689] **Speaker 0:** equal to R2 over R1.
[00:41:30:679 - 00:41:33:590] **Speaker 0:** The amount or the size of that.
[00:41:34:770 - 00:41:38:040] **Speaker 0:** Proportional control um value.
[00:41:39:179 - 00:41:42:500] **Speaker 0:** That's up to you to to determine uh via operation
[00:41:42:500 - 00:41:43:659] **Speaker 0:** of the of the circuit.
[00:41:45:159 - 00:41:46:360] **Speaker 0:** With the actual panel.
[00:41:48:020 - 00:41:52:580] **Speaker 0:** But like I said, Uh, most designs that come through
[00:41:52:580 - 00:41:56:370] **Speaker 0:** won't require you to have proportional implemented whatsoever and it
[00:41:56:370 - 00:41:57:729] **Speaker 0:** will work perfectly well.
[00:42:00:159 - 00:42:01:110] **Speaker 0:** Any questions?
[00:42:05:610 - 00:42:08:159] **Speaker 0:** Right, so That's it for today.
[00:42:08:239 - 00:42:09:219] **Speaker 0:** It's a little bit shorter.

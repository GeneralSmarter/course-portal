# ENME302-26S2 Lecture 38 native Echo transcript

Date: September 30, 2026 11:00am-11:55am
Transcript type: native Echo automated transcript.

[00:00:19:629 - 00:00:22:489] **Speaker 0:** my Yes.
[00:00:27:989 - 00:00:42:840] **Speaker 0:** I And the opposite.
[00:00:45:319 - 00:00:49:009] **Speaker 0:** guys Uh, good morning.
[00:00:49:130 - 00:00:50:029] **Speaker 1:** We'll make a start.
[00:00:50:529 - 00:00:52:049] **Speaker 1:** As some of you might have known, they've got the
[00:00:52:049 - 00:00:53:049] **Speaker 1:** RoboCup this morning.
[00:00:53:240 - 00:00:56:790] **Speaker 1:** I don't know, is anyone doing well in the RoboCup,
[00:00:56:849 - 00:00:59:250] **Speaker 1:** or I poked my head in, and it was very
[00:00:59:250 - 00:01:02:599] **Speaker 1:** festive, but I had a meeting, but, um.
[00:01:03:709 - 00:01:07:029] **Speaker 1:** They continue on Friday from 1 to 4 p.m. in
[00:01:07:029 - 00:01:07:980] **Speaker 1:** case you want to watch.
[00:01:08:430 - 00:01:11:930] **Speaker 1:** So it's in that, um, the Robert Skate Scott Atrium
[00:01:11:930 - 00:01:13:790] **Speaker 1:** that's in the workshop wing if you want to go
[00:01:13:790 - 00:01:14:169] **Speaker 1:** and watch.
[00:01:14:750 - 00:01:17:309] **Speaker 1:** Is anyone actually from Tron in the room, or?
[00:01:17:860 - 00:01:18:500] **Speaker 1:** Oh, someone made it.
[00:01:18:669 - 00:01:18:680] **Speaker 1:** Good.
[00:01:19:790 - 00:01:21:750] **Speaker 1:** Does that mean that you passed or didn't pass the
[00:01:21:750 - 00:01:22:160] **Speaker 1:** first ring?
[00:01:22:989 - 00:01:23:370] **Speaker 1:** Sorry.
[00:01:24:029 - 00:01:24:569] **Speaker 1:** Next year?
[00:01:24:629 - 00:01:24:900] **Speaker 1:** uh.
[00:01:26:139 - 00:01:31:129] **Speaker 1:** Um, Yeah, so we'll keep going with chapter 8.
[00:01:31:209 - 00:01:33:169] **Speaker 1:** Is there any questions before we get started?
[00:01:36:910 - 00:01:39:290] **Speaker 1:** Anyone stuck with the assignments or the quiz this week
[00:01:39:290 - 00:01:39:790] **Speaker 1:** or?
[00:01:41:970 - 00:01:43:010] **Speaker 1:** Haven't looked at it yet.
[00:01:43:930 - 00:01:44:849] **Speaker 1:** No, that's alright.
[00:01:44:970 - 00:01:47:849] **Speaker 1:** Have a look, um, maybe tomorrow, not that.
[00:01:49:599 - 00:01:51:760] **Speaker 1:** The assignment, yeah, as I say, if you get stuck
[00:01:51:760 - 00:01:54:720] **Speaker 1:** on that first question, just go to the console parts.
[00:01:55:239 - 00:01:59:000] **Speaker 1:** Don't, don't waste your whole two weeks on, on coding,
[00:01:59:110 - 00:02:00:580] **Speaker 1:** but it's, it's not that bad really.
[00:02:01:650 - 00:02:04:690] **Speaker 1:** So chapter 8, we were looking at finite elements.
[00:02:04:879 - 00:02:06:089] **Speaker 1:** So what is console doing?
[00:02:06:239 - 00:02:07:269] **Speaker 1:** What what is it solving?
[00:02:07:410 - 00:02:08:860] **Speaker 1:** How is it solving all these things?
[00:02:09:570 - 00:02:12:089] **Speaker 1:** So it uses finite elements and we introduced that that
[00:02:12:089 - 00:02:16:729] **Speaker 1:** concept of uh tessellation or, Discrets our grid with all
[00:02:16:729 - 00:02:20:169] **Speaker 1:** these little elements, we've described each element with these nodes.
[00:02:21:130 - 00:02:23:949] **Speaker 1:** And we looked at interpolation within a one one-dimensional element.
[00:02:27:110 - 00:02:31:949] **Speaker 1:** And we've got some shape functions that we derived and
[00:02:31:949 - 00:02:33:830] **Speaker 1:** we end up with a system of equations to solve,
[00:02:33:940 - 00:02:35:929] **Speaker 1:** so our favourite linear algebra problem.
[00:02:36:429 - 00:02:39:270] **Speaker 1:** So we're solving for for displacement field U or it
[00:02:39:270 - 00:02:42:389] **Speaker 1:** could be temperature or anything, and those hold those nodal
[00:02:42:389 - 00:02:44:070] **Speaker 1:** values within our domain.
[00:02:47:919 - 00:02:48:320] **Speaker 1:** Oh.
[00:02:49:850 - 00:02:54:330] **Speaker 1:** So we'll do some examples of approximating the solution space
[00:02:54:330 - 00:02:56:440] **Speaker 1:** with these interpolating functions or shape functions.
[00:02:56:929 - 00:03:00:970] **Speaker 1:** And we're gonna compare linear and quadratic elements to approximate
[00:03:00:970 - 00:03:01:850] **Speaker 1:** this quadratic.
[00:03:02:169 - 00:03:05:050] **Speaker 1:** So minus 5 X2 + 66 x + 40.
[00:03:06:360 - 00:03:08:000] **Speaker 1:** And we're gonna look at some interval from 0 to
[00:03:08:000 - 00:03:08:320] **Speaker 1:** 10.
[00:03:09:449 - 00:03:12:179] **Speaker 1:** And we're gonna look at 4 linear elements that we've
[00:03:12:179 - 00:03:14:740] **Speaker 1:** derived so far, and then 2 quadratic elements.
[00:03:20:669 - 00:03:22:149] **Speaker 1:** So in summary.
[00:03:23:169 - 00:03:25:059] **Speaker 1:** If we have 4 linear elements.
[00:03:37:770 - 00:03:39:259] **Speaker 1:** Uh, we're going to have.
[00:03:42:929 - 00:03:43:910] **Speaker 1:** 5 notes.
[00:03:45:699 - 00:03:48:130] **Speaker 1:** So 4 intervals, 4 elements.
[00:03:51:410 - 00:03:53:369] **Speaker 1:** Which we're going to label with these circles, 123 and
[00:03:53:369 - 00:03:56:449] **Speaker 1:** 4, and the nodes represent the boundaries of each element,
[00:03:56:690 - 00:03:59:050] **Speaker 1:** so we've got plus 1 nodes and 1 D.
[00:03:59:369 - 00:04:01:559] **Speaker 1:** So we're gonna have 4 nodes, and that means that
[00:04:01:559 - 00:04:04:490] **Speaker 1:** we've got 5 degrees of freedom.
[00:04:11:070 - 00:04:13:750] **Speaker 1:** Each element has 2 degrees of freedom, but they share
[00:04:13:750 - 00:04:17:028] **Speaker 1:** the same degree of freedom at the interface between each
[00:04:17:028 - 00:04:17:428] **Speaker 1:** element.
[00:04:17:890 - 00:04:19:049] **Speaker 1:** So we've got 5 in total.
[00:04:23:019 - 00:04:27:579] **Speaker 1:** If we just analyse the element 1, we've got nodes
[00:04:27:579 - 00:04:29:380] **Speaker 1:** at X1 and X2.
[00:04:41:209 - 00:04:44:250] **Speaker 1:** So these are both, so that's linear elements.
[00:04:44:540 - 00:04:45:750] **Speaker 1:** So quadratic elements.
[00:04:46:480 - 00:04:49:799] **Speaker 1:** Which we'll arrive shortly, but just as an overview.
[00:04:50:519 - 00:04:54:970] **Speaker 1:** Over the same interval We have elements 1 and 2.
[00:04:58:750 - 00:05:01:820] **Speaker 1:** Each element Quadratic element.
[00:05:05:369 - 00:05:07:220] **Speaker 1:** Has 3 degrees of freedom.
[00:05:27:220 - 00:05:29:109] **Speaker 1:** So we have the nodal values of X1 and X2,
[00:05:29:299 - 00:05:31:290] **Speaker 1:** and we have this midpoint that we also need to
[00:05:31:290 - 00:05:33:779] **Speaker 1:** use and and we'll come to that shortly uh when
[00:05:33:779 - 00:05:35:420] **Speaker 1:** we derive that quadratic element.
[00:05:36:170 - 00:05:38:290] **Speaker 1:** Uh, but we need 3 points to uniquely identify a
[00:05:38:290 - 00:05:39:309] **Speaker 1:** quadratic function.
[00:05:39:730 - 00:05:41:369] **Speaker 1:** We just need 2 for, for linear.
[00:05:42:369 - 00:05:45:190] **Speaker 1:** And that means that our quadratic.
[00:05:46:559 - 00:05:49:239] **Speaker 1:** Elements, so the two elements at the top, also have
[00:05:49:239 - 00:05:50:480] **Speaker 1:** 5 degrees of freedom.
[00:06:16:359 - 00:06:19:470] **Speaker 1:** So we've got The same number of degrees of freedom,
[00:06:19:510 - 00:06:23:230] **Speaker 1:** so 555 um matrix coefficients, we've got 5 equations to
[00:06:23:230 - 00:06:23:690] **Speaker 1:** solve.
[00:06:24:869 - 00:06:28:279] **Speaker 1:** There are two distinct different, uh, shape elements, and we're
[00:06:28:279 - 00:06:31:700] **Speaker 1:** going to see how accurately they can resolve this quadratic
[00:06:31:700 - 00:06:34:700] **Speaker 1:** function minus 5 X2 + 66 X + 40.
[00:06:40:230 - 00:06:41:950] **Speaker 1:** So for the linear elements, first we're gonna look at
[00:06:41:950 - 00:06:46:630] **Speaker 1:** the, the function F of X and analyse piecewise linear
[00:06:46:630 - 00:06:47:190] **Speaker 1:** segments.
[00:06:47:390 - 00:06:49:220] **Speaker 1:** So the interpolating functions are linear.
[00:06:49:260 - 00:06:50:850] **Speaker 1:** Is that too dark or is that OK?
[00:06:51:390 - 00:06:51:970] **Speaker 1:** That's all good.
[00:06:52:350 - 00:06:59:369] **Speaker 1:** Um, so, Each interval between each node is going to
[00:06:59:369 - 00:07:02:970] **Speaker 1:** be interpolated with a linear function, so we've got a
[00:07:02:970 - 00:07:03:309] **Speaker 1:** line.
[00:07:04:559 - 00:07:07:480] **Speaker 1:** That looks pretty much just the curve at this point,
[00:07:07:640 - 00:07:07:839] **Speaker 1:** but.
[00:07:16:540 - 00:07:19:940] **Speaker 1:** And we can segment our domain into 4 elements.
[00:07:21:920 - 00:07:25:600] **Speaker 1:** 123, and 4.
[00:07:27:549 - 00:07:30:350] **Speaker 1:** We can evaluate the, the function at each nodal point,
[00:07:30:549 - 00:07:34:209] **Speaker 1:** so 40, 174, 246, and 254.
[00:07:38:089 - 00:07:40:359] **Speaker 1:** And what we're going to do is use our linear
[00:07:40:359 - 00:07:41:850] **Speaker 1:** interpolation on each element.
[00:07:42:829 - 00:07:45:230] **Speaker 1:** Our function F of X is going to be approximated.
[00:07:46:239 - 00:07:48:760] **Speaker 1:** By F tilda, so the tilda on the top of
[00:07:48:760 - 00:07:51:359] **Speaker 1:** the F represents that we're approximating this function with our
[00:07:51:359 - 00:07:52:480] **Speaker 1:** linear interpolation.
[00:07:54:029 - 00:07:56:450] **Speaker 1:** Or with any interpolation, interpolating function.
[00:07:58:059 - 00:07:59:660] **Speaker 1:** F of X.
[00:08:01:309 - 00:08:03:250] **Speaker 1:** And we derived these shape functions earlier.
[00:08:05:119 - 00:08:05:890] **Speaker 1:** On Monday.
[00:08:08:230 - 00:08:11:029] **Speaker 1:** And we figured out that this was the description of
[00:08:11:179 - 00:08:13:470] **Speaker 1:** a linear interpolation, so we're going to use these for
[00:08:13:470 - 00:08:14:070] **Speaker 1:** our function.
[00:08:14:700 - 00:08:15:760] **Speaker 1:** So we've got the in one.
[00:08:17:160 - 00:08:23:910] **Speaker 1:** Of X Multiplied by Uh, the dependent variable you at
[00:08:23:910 - 00:08:24:529] **Speaker 1:** node I.
[00:08:26:359 - 00:08:29:480] **Speaker 1:** And then we've got the 2nd shape function multiplied by
[00:08:29:480 - 00:08:30:519] **Speaker 1:** you at 1 + 1.
[00:08:31:739 - 00:08:34:460] **Speaker 1:** And this is for the interval from XI.
[00:08:36:289 - 00:08:38:090] **Speaker 1:** Up to Xi plus 1.
[00:08:47:570 - 00:08:49:109] **Speaker 1:** And we derived these shape functions earlier.
[00:08:49:369 - 00:08:50:669] **Speaker 1:** We had N1 of X.
[00:08:51:940 - 00:08:55:450] **Speaker 1:** Equal to xi + 1 minus X over.
[00:08:56:289 - 00:08:58:200] **Speaker 1:** Xi + 1 minus XI.
[00:08:59:770 - 00:09:06:799] **Speaker 1:** And In Of X was X minus XI.
[00:09:07:770 - 00:09:10:090] **Speaker 1:** Over Xi plus 1 minus Xi.
[00:09:11:260 - 00:09:14:590] **Speaker 1:** So these are just those lines that alternate between 1
[00:09:14:590 - 00:09:18:320] **Speaker 1:** and 0, representing the the node that it represents.
[00:09:20:960 - 00:09:23:710] **Speaker 1:** So N1 is equal to 1 at node 1, N2
[00:09:23:710 - 00:09:25:000] **Speaker 1:** is equal to 1 at node 2.
[00:09:30:369 - 00:09:34:200] **Speaker 1:** So we can describe Or approximate a function F with
[00:09:34:200 - 00:09:35:859] **Speaker 1:** F theta along this interval.
[00:09:43:729 - 00:09:46:450] **Speaker 1:** So we've done that with linear elements, and now we're
[00:09:46:450 - 00:09:48:489] **Speaker 1:** gonna do it for quadratic elements.
[00:09:58:039 - 00:09:59:549] **Speaker 1:** So we're going to do the same thing with the
[00:09:59:549 - 00:10:00:489] **Speaker 1:** quadratic elements.
[00:10:00:909 - 00:10:04:409] **Speaker 1:** If we fit a quadratic curve to a quadratic function,
[00:10:04:469 - 00:10:07:429] **Speaker 1:** it can match exactly, so we don't really have to
[00:10:07:429 - 00:10:09:590] **Speaker 1:** draw anything, but if we draw it exactly on the
[00:10:09:590 - 00:10:09:890] **Speaker 1:** top.
[00:10:17:150 - 00:10:22:270] **Speaker 1:** And we're going to approximate each element uh with a
[00:10:22:270 - 00:10:23:510] **Speaker 1:** quadratic interpolation.
[00:10:24:190 - 00:10:26:229] **Speaker 1:** And just as we did before for the linear case,
[00:10:26:270 - 00:10:28:369] **Speaker 1:** we're going to assume a form.
[00:10:29:179 - 00:10:36:169] **Speaker 1:** Of U X Being Some coefficient, we're going to call
[00:10:36:169 - 00:10:37:890] **Speaker 1:** it a hat X2.
[00:10:38:799 - 00:10:40:330] **Speaker 1:** Plus Bhat.
[00:10:41:030 - 00:10:42:770] **Speaker 1:** X plus.
[00:10:43:489 - 00:10:44:650] **Speaker 1:** See hat.
[00:10:46:469 - 00:10:49:390] **Speaker 1:** And we're going to analyse one element at a time.
[00:10:50:429 - 00:10:51:530] **Speaker 1:** So from XI.
[00:10:53:140 - 00:10:55:340] **Speaker 1:** To XI + 1.
[00:11:04:570 - 00:11:07:130] **Speaker 1:** So the learning case just had BX + C, essentially.
[00:11:07:869 - 00:11:10:580] **Speaker 1:** So for convenience, we're going to introduce a normalised local
[00:11:10:580 - 00:11:11:320] **Speaker 1:** coordinate system.
[00:11:11:380 - 00:11:14:440] **Speaker 1:** So instead of dealing with all these global X's, we're
[00:11:14:440 - 00:11:17:169] **Speaker 1:** going to introduce a local variable shire.
[00:11:21:190 - 00:11:23:309] **Speaker 1:** So I can't draw shy very well, which is always
[00:11:23:309 - 00:11:27:520] **Speaker 1:** fun, um, but you can introduce whatever variable you wish
[00:11:28:030 - 00:11:28:469] **Speaker 1:** that's shy.
[00:11:29:770 - 00:11:31:960] **Speaker 1:** And this is going to equal.
[00:11:32:719 - 00:11:34:260] **Speaker 1:** X minus Xi.
[00:11:35:400 - 00:11:38:919] **Speaker 1:** Over Xi + 1 minus Xi.
[00:11:48:390 - 00:11:49:890] **Speaker 1:** So, shy.
[00:11:50:919 - 00:11:55:119] **Speaker 1:** At Xi is equal to.
[00:11:56:380 - 00:12:01:440] **Speaker 1:** Xi minus XI over Xi plus 1 minus XI.
[00:12:02:940 - 00:12:03:669] **Speaker 1:** Which is 0.
[00:12:05:080 - 00:12:07:039] **Speaker 1:** It's on the lower limit at XI.
[00:12:08:000 - 00:12:11:729] **Speaker 1:** Our normalised local coordinate is 0, and on the right.
[00:12:13:989 - 00:12:16:580] **Speaker 1:** Xi plus 1, and it's getting worse.
[00:12:17:080 - 00:12:21:260] **Speaker 1:** We've got Xi + 1 minus Xi divided by XI
[00:12:21:260 - 00:12:22:869] **Speaker 1:** + 1 minus XI.
[00:12:25:239 - 00:12:26:030] **Speaker 1:** Which is equal to 1.
[00:12:27:020 - 00:12:29:909] **Speaker 1:** So all this is doing is We've got a normalised
[00:12:29:909 - 00:12:32:400] **Speaker 1:** coordinate from 0 to 1 on our interval.
[00:12:35:239 - 00:12:36:840] **Speaker 1:** And this is just gonna make our maths a lot
[00:12:36:840 - 00:12:37:299] **Speaker 1:** easier.
[00:12:37:679 - 00:12:38:599] **Speaker 1:** You don't have to do this.
[00:12:41:169 - 00:12:46:640] **Speaker 1:** So we've got you Of shi equal to a.
[00:12:48:440 - 00:12:52:200] **Speaker 1:** 2 + B + Z.
[00:12:55:099 - 00:12:58:950] **Speaker 1:** So I've gone from the Global space you have X
[00:12:58:950 - 00:12:59:619] **Speaker 1:** to you of shi.
[00:13:16:239 - 00:13:18:890] **Speaker 1:** And I used the hats earlier because we don't really
[00:13:18:890 - 00:13:19:630] **Speaker 1:** use them later on.
[00:13:19:969 - 00:13:21:359] **Speaker 1:** So A, B, and C are going to be the
[00:13:21:359 - 00:13:22:390] **Speaker 1:** unknown consonants.
[00:13:25:510 - 00:13:27:950] **Speaker 1:** So we're going to need 3 equations to figure out
[00:13:27:950 - 00:13:31:179] **Speaker 1:** these, these coefficients, A, B, and C, or constants A,
[00:13:31:229 - 00:13:31:710] **Speaker 1:** B, and C.
[00:13:34:010 - 00:13:38:400] **Speaker 1:** We've got 3 points on each element.
[00:13:43:039 - 00:13:49:619] **Speaker 1:** So element one Has 3 degrees of freedom at points
[00:13:49:619 - 00:13:50:580] **Speaker 1:** 12, and 3.
[00:13:51:400 - 00:13:54:080] **Speaker 1:** And element 2 also has 3 degrees of freedom at
[00:13:54:080 - 00:13:55:140] **Speaker 1:** 0.34 and 5.
[00:13:57:679 - 00:13:59:859] **Speaker 1:** We're just gonna analyse element one for now.
[00:14:00:630 - 00:14:06:909] **Speaker 1:** And we know that you Of shy At 0, so
[00:14:06:909 - 00:14:10:229] **Speaker 1:** the left-hand side is going to equal U1.
[00:14:13:280 - 00:14:18:450] **Speaker 1:** And we know that Our displacement at the midpoint, which
[00:14:18:450 - 00:14:22:190] **Speaker 1:** is shy 12, that's linearly changing from 0 to 1,
[00:14:22:770 - 00:14:26:950] **Speaker 1:** is equal to U2 and U shy equal to 1
[00:14:27:289 - 00:14:28:849] **Speaker 1:** is equal to U3.
[00:14:35:570 - 00:14:39:419] **Speaker 1:** So we've got 3 equations, 3 unknowns, and we're gonna
[00:14:39:419 - 00:14:40:150] **Speaker 1:** solve that.
[00:14:40:539 - 00:14:41:859] **Speaker 1:** So we're gonna solve A, B, and C.
[00:14:44:989 - 00:14:46:280] **Speaker 1:** And you.
[00:14:47:229 - 00:14:49:229] **Speaker 1:** That's shy equal to 0.
[00:14:50:349 - 00:14:52:059] **Speaker 1:** Substituting into equation 16.
[00:14:54:030 - 00:14:56:469] **Speaker 1:** We've got A times 0 + B x 0 +
[00:14:56:469 - 00:14:56:750] **Speaker 1:** C.
[00:14:58:849 - 00:15:00:890] **Speaker 1:** Which is equal to C.
[00:15:01:929 - 00:15:03:549] **Speaker 1:** And we said this is equal to U1.
[00:15:05:150 - 00:15:08:929] **Speaker 1:** And then we've got you shy equal to 5.
[00:15:10:030 - 00:15:15:190] **Speaker 1:** So we've got A Times 1/2 squared, so a quarter
[00:15:15:830 - 00:15:16:950] **Speaker 1:** E times 1/22.
[00:15:17:960 - 00:15:19:109] **Speaker 1:** Plus C.
[00:15:20:349 - 00:15:24:719] **Speaker 1:** Equal to U2 and you shy equal to 1, we've
[00:15:24:719 - 00:15:28:450] **Speaker 1:** got a, Plus B + C equal to U3.
[00:15:39:409 - 00:15:39:650] **Speaker 1:** Cool.
[00:15:43:919 - 00:15:47:219] **Speaker 1:** And if we solve this system, then we've got C
[00:15:47:320 - 00:15:49:099] **Speaker 1:** is equal to U1.
[00:15:49:559 - 00:15:51:140] **Speaker 1:** The first equation, B.
[00:15:52:369 - 00:15:53:940] **Speaker 1:** Is -31.
[00:15:54:900 - 00:15:56:109] **Speaker 1:** Plus for you to.
[00:15:57:260 - 00:15:58:250] **Speaker 1:** Minus U3.
[00:15:58:950 - 00:16:01:190] **Speaker 1:** And A is.
[00:16:02:559 - 00:16:05:590] **Speaker 1:** Do you, um, 42.
[00:16:06:539 - 00:16:08:570] **Speaker 1:** Plus 2 U 3.
[00:16:34:190 - 00:16:38:469] **Speaker 1:** So our Displacement field, for example, you of shy.
[00:16:39:429 - 00:16:41:429] **Speaker 1:** Uh, if you substitute an A, B, and C, that
[00:16:41:429 - 00:16:43:989] **Speaker 1:** would give a description of how the dependent variable U
[00:16:43:989 - 00:16:47:030] **Speaker 1:** varies across that element in a quadratic fashion.
[00:16:47:940 - 00:16:49:820] **Speaker 1:** So just as we did for the linear elements, we
[00:16:49:820 - 00:16:52:179] **Speaker 1:** figured out those shape functions in 1 and 2.
[00:16:54:849 - 00:16:55:059] **Speaker 1:** You do.
[00:16:56:010 - 00:16:59:830] **Speaker 1:** Now we've got 3 nodes, U 12 and 3, so
[00:16:59:830 - 00:17:01:049] **Speaker 1:** we're gonna have 3 shaped functions.
[00:17:05:910 - 00:17:08:270] **Speaker 1:** So substituting an A, B, and C into a polynomial.
[00:17:12:560 - 00:17:14:359] **Speaker 1:** Uh, so it might be reasonable, well, a little bit
[00:17:14:359 - 00:17:16:880] **Speaker 1:** longer, so maybe on the left you of shy.
[00:17:19:318 - 00:17:21:037] **Speaker 1:** We're gonna substitute it for A.
[00:17:21:959 - 00:17:24:000] **Speaker 1:** Which was 21.
[00:17:25:250 - 00:17:31:739] **Speaker 1:** -4U2 + 2U3 multiplied by shi squad.
[00:17:33:089 - 00:17:33:780] **Speaker 1:** Plus.
[00:17:34:890 - 00:17:37:250] **Speaker 1:** -3U1 + 4U2.
[00:17:38:579 - 00:17:39:680] **Speaker 1:** -3.
[00:17:41:709 - 00:18:04:459] **Speaker 1:** Plus You Which was And we want to group all
[00:18:04:459 - 00:18:07:180] **Speaker 1:** of the like coefficients in front of the nodes, U
[00:18:07:180 - 00:18:08:140] **Speaker 1:** 12, and 3.
[00:18:14:359 - 00:18:17:939] **Speaker 1:** So the coefficients in front of U1 as is 22.
[00:18:21:979 - 00:18:23:910] **Speaker 1:** And we've got -3 times show.
[00:18:26:170 - 00:18:27:609] **Speaker 1:** And we've got plus one.
[00:18:31:650 - 00:18:34:449] **Speaker 1:** And then for U2, we've got -4.
[00:18:35:959 - 00:18:36:880] **Speaker 1:** Shall I squid?
[00:18:37:469 - 00:18:45:770] **Speaker 1:** And positive for I And for you 3 We have
[00:18:45:770 - 00:18:48:949] **Speaker 1:** 2 Shy squad.
[00:18:50:640 - 00:18:51:979] **Speaker 1:** Minus shy.
[00:18:59:489 - 00:19:02:719] **Speaker 1:** And we've grouped those light coefficients to determine those coefficients
[00:19:02:770 - 00:19:05:810] **Speaker 1:** of those shape functions in 12, and 3.
[00:19:06:709 - 00:19:08:869] **Speaker 1:** So I've got in one of shy.
[00:19:10:099 - 00:19:15:339] **Speaker 1:** U1 plus N2 of shy, U2.
[00:19:16:239 - 00:19:20:000] **Speaker 1:** And in 3 of shy, 3.
[00:19:33:160 - 00:19:36:400] **Speaker 1:** So the Well I guess maybe it's easy just to
[00:19:36:400 - 00:19:37:410] **Speaker 1:** visualise it first.
[00:19:37:810 - 00:19:40:050] **Speaker 1:** So down here we've plotted the shape functions.
[00:19:40:449 - 00:19:42:209] **Speaker 1:** You can see that they're all quadratics.
[00:19:42:569 - 00:19:47:250] **Speaker 1:** We've got 22 minus 3 + 1 is N1 and
[00:19:47:250 - 00:19:50:469] **Speaker 1:** I've plotted this in this normalised coordinate system shy.
[00:19:51:439 - 00:19:53:949] **Speaker 1:** Again, it's easier to deal with this normalised coordinate system
[00:19:53:949 - 00:19:55:770] **Speaker 1:** because it applies for each element distinctly.
[00:19:56:469 - 00:20:00:790] **Speaker 1:** Um, and it's harder to sort of convert to, to
[00:20:00:790 - 00:20:01:510] **Speaker 1:** XSpace.
[00:20:02:810 - 00:20:06:849] **Speaker 1:** And the second shape function N2 is given by -4
[00:20:06:849 - 00:20:08:079] **Speaker 1:** 2 + 4 shy.
[00:20:08:890 - 00:20:11:790] **Speaker 1:** So that is this dash line and it's symmetric.
[00:20:12:290 - 00:20:14:869] **Speaker 1:** And the one on the right is 22 minus shy.
[00:20:15:520 - 00:20:17:140] **Speaker 1:** So that is the dotted.
[00:20:20:520 - 00:20:22:150] **Speaker 1:** So we want to make sure that our shape functions
[00:20:22:150 - 00:20:25:869] **Speaker 1:** are valid and earlier we described that each shape function
[00:20:25:869 - 00:20:28:510] **Speaker 1:** has to sort of represent the node that it represents.
[00:20:28:589 - 00:20:31:989] **Speaker 1:** So N1 has to equal 1 at 0.1 N2 at
[00:20:31:989 - 00:20:33:989] **Speaker 1:** 0.2 and N3 at 0.3.
[00:20:34:729 - 00:20:36:650] **Speaker 1:** And we're going to check that in one.
[00:20:39:790 - 00:20:41:060] **Speaker 1:** Of Shi is is valid.
[00:20:41:739 - 00:20:44:770] **Speaker 1:** So we're gonna evaluate it at 0.0, so shy equals
[00:20:44:770 - 00:20:45:219] **Speaker 1:** 0.
[00:20:47:260 - 00:20:49:119] **Speaker 1:** And we've got 2 x 0.
[00:20:50:989 - 00:20:53:119] **Speaker 1:** 2 minus 3 times 0.
[00:20:53:920 - 00:20:55:910] **Speaker 1:** Plus one, which was one.
[00:20:56:760 - 00:21:01:839] **Speaker 1:** In, oh sorry, N1 at shy equal to half, at
[00:21:01:839 - 00:21:02:439] **Speaker 1:** the midpoint.
[00:21:03:689 - 00:21:07:829] **Speaker 1:** Arguably you could place this intermediate node at any point.
[00:21:07:849 - 00:21:09:300] **Speaker 1:** For convenience, we're putting it at a 12.
[00:21:10:510 - 00:21:12:160] **Speaker 1:** But for extra fun you could put it somewhere else,
[00:21:12:239 - 00:21:15:910] **Speaker 1:** but then you'd have to rederive the, Uh, shape, shape
[00:21:15:910 - 00:21:16:310] **Speaker 1:** elements.
[00:21:17:180 - 00:21:20:619] **Speaker 1:** So in one, being at the midpoint, we've got a
[00:21:21:540 - 00:21:24:630] **Speaker 1:** Um, 2 times 12 squared.
[00:21:27:469 - 00:21:30:800] **Speaker 1:** So 1/2 squared we've got 1/4, and then minus 3
[00:21:30:800 - 00:21:31:640] **Speaker 1:** times 1/2.
[00:21:33:510 - 00:21:35:199] **Speaker 1:** Plus one.
[00:21:37:229 - 00:21:38:250] **Speaker 1:** So we've got a half.
[00:21:39:599 - 00:21:41:060] **Speaker 1:** -3 halves.
[00:21:42:229 - 00:21:44:050] **Speaker 1:** Plus 1, is that 0.
[00:21:46:099 - 00:21:49:339] **Speaker 1:** And then we've got N1 at shy equal 1.
[00:21:50:609 - 00:21:51:619] **Speaker 1:** So 2 x 1.
[00:21:53:369 - 00:21:55:410] **Speaker 1:** -3 times 1 + 1.
[00:21:56:329 - 00:21:59:640] **Speaker 1:** Who So that's valid, we can do the same, check
[00:21:59:640 - 00:22:01:339] **Speaker 1:** for shape functions in 2 and 3.
[00:22:07:319 - 00:22:10:800] **Speaker 1:** Um, I think you can do basic arithmetic, so I
[00:22:10:800 - 00:22:11:920] **Speaker 1:** might do that in a lecture.
[00:22:14:099 - 00:22:16:449] **Speaker 1:** And as I say, this is plotting the shape functions.
[00:22:16:900 - 00:22:17:800] **Speaker 1:** So we've got.
[00:22:19:420 - 00:22:21:260] **Speaker 1:** These 3 quarter acres.
[00:22:22:329 - 00:22:25:530] **Speaker 1:** So I guess that's the distinction between quadratic and linear
[00:22:25:530 - 00:22:26:349] **Speaker 1:** shape functions.
[00:22:31:500 - 00:22:31:819] **Speaker 1:** Um.
[00:22:33:650 - 00:22:34:859] **Speaker 1:** So I'll show you this.
[00:22:36:520 - 00:23:02:579] **Speaker 1:** Code Which is a bit hectic, but um.
[00:23:03:619 - 00:23:06:750] **Speaker 1:** So we've got the our function F of X, which
[00:23:06:750 - 00:23:09:270] **Speaker 1:** is a squadratic minus 5 X2 + 66 X +
[00:23:09:270 - 00:23:11:170] **Speaker 1:** 40, and we're going to plot that.
[00:23:11:930 - 00:23:15:390] **Speaker 1:** And then we've got these, uh, distinct points, X1, 23,
[00:23:15:400 - 00:23:16:270] **Speaker 1:** and 4.
[00:23:18:560 - 00:23:19:089] **Speaker 1:** 25, I think.
[00:23:20:930 - 00:23:22:290] **Speaker 1:** X 1234 and 5.
[00:23:23:270 - 00:23:24:630] **Speaker 1:** and we've got 4 elements.
[00:23:25:390 - 00:23:29:189] **Speaker 1:** So what I've done here is plotted a linear distribution
[00:23:29:189 - 00:23:29:770] **Speaker 1:** between two.
[00:23:30:270 - 00:23:32:689] **Speaker 1:** So our shape functions in 1 and 2 are as
[00:23:32:949 - 00:23:33:689] **Speaker 1:** defined earlier.
[00:23:35:790 - 00:23:37:380] **Speaker 1:** That's these guys, equation 84.
[00:23:38:449 - 00:23:43:170] **Speaker 1:** And we're going to plot U1 on this interval for
[00:23:43:170 - 00:23:43:729] **Speaker 1:** element one.
[00:23:44:900 - 00:23:46:819] **Speaker 1:** We do the same for those other three elements that
[00:23:46:819 - 00:23:47:270] **Speaker 1:** are linear.
[00:23:48:069 - 00:23:49:680] **Speaker 1:** And then we're also looking at the same for the
[00:23:49:680 - 00:23:52:109] **Speaker 1:** quadrant, OK, so as I say, it's much easier to
[00:23:52:109 - 00:23:54:310] **Speaker 1:** convert to this normalised coordinate spaces.
[00:23:55:760 - 00:23:59:849] **Speaker 1:** And Now it's from X1 up to X3.
[00:24:00:660 - 00:24:02:780] **Speaker 1:** And Python likes to be off by 1, so we've
[00:24:02:780 - 00:24:04:140] **Speaker 1:** got X0 up to X2.
[00:24:04:910 - 00:24:10:380] **Speaker 1:** And we've got 11 points on that interval and Shy
[00:24:10:380 - 00:24:13:010] **Speaker 1:** is just going from 0 up to 1.
[00:24:13:430 - 00:24:15:650] **Speaker 1:** We've got our shape functions in 12 and 3.
[00:24:16:280 - 00:24:18:550] **Speaker 1:** And that's what we've defined up here, equation 20C.
[00:24:22:560 - 00:24:24:280] **Speaker 1:** We do the same for the 2nd quadratic element, and
[00:24:24:280 - 00:24:24:939] **Speaker 1:** then we plot.
[00:24:30:619 - 00:24:33:540] **Speaker 1:** So what we see here, if you squint, the legend
[00:24:33:540 - 00:24:36:300] **Speaker 1:** says the blue line is original function.
[00:24:36:819 - 00:24:39:209] **Speaker 1:** The red lines are the linear elements.
[00:24:39:619 - 00:24:42:420] **Speaker 1:** So it's a linear approximation between each distinct node.
[00:24:43:260 - 00:24:50:780] **Speaker 1:** And the Black Dotted line is the quadratic elements, which
[00:24:50:780 - 00:24:52:359] **Speaker 1:** is matching perfectly our function.
[00:24:52:750 - 00:24:54:459] **Speaker 1:** So we can see here that obviously if we expect
[00:24:54:459 - 00:24:57:699] **Speaker 1:** to have a quadratic solution using quadratic elements would be
[00:24:57:699 - 00:24:58:459] **Speaker 1:** much more accurate.
[00:24:58:699 - 00:25:00:800] **Speaker 1:** We could even get away with just one element arguably
[00:25:01:339 - 00:25:02:680] **Speaker 1:** and get the same level of accuracy.
[00:25:03:750 - 00:25:07:989] **Speaker 1:** So linear elements introduces some discretization error in this sort
[00:25:07:989 - 00:25:10:989] **Speaker 1:** of gap between the linear and the true solution.
[00:25:12:140 - 00:25:15:219] **Speaker 1:** I think one year someone was asking about can we
[00:25:15:219 - 00:25:19:099] **Speaker 1:** use not normalised coordinate systems and that what is what
[00:25:19:099 - 00:25:20:199] **Speaker 1:** all this code is for.
[00:25:20:699 - 00:25:21:540] **Speaker 1:** So it's more coding.
[00:25:22:660 - 00:25:27:229] **Speaker 1:** Back before AI um and it achieves the same thing,
[00:25:27:500 - 00:25:27:839] **Speaker 1:** so.
[00:25:28:660 - 00:25:31:319] **Speaker 1:** Um Hopefully.
[00:25:31:780 - 00:25:33:030] **Speaker 1:** I don't know if we want to have a look.
[00:25:36:430 - 00:25:36:750] **Speaker 1:** Why not?
[00:25:36:790 - 00:25:37:750] **Speaker 1:** We've got heaps of time.
[00:25:41:739 - 00:25:43:689] **Speaker 1:** There might be a quicker way of uncommenting.
[00:25:45:020 - 00:25:46:959] **Speaker 1:** But this is how much I use.
[00:25:53:709 - 00:25:53:989] **Speaker 1:** All right.
[00:25:57:890 - 00:25:58:170] **Speaker 1:** Cool.
[00:25:58:910 - 00:25:59:869] **Speaker 1:** So it's the same floor.
[00:26:01:290 - 00:26:01:770] **Speaker 1:** Excellent.
[00:26:03:630 - 00:26:09:079] **Speaker 1:** Um All right.
[00:26:11:560 - 00:26:15:060] **Speaker 1:** Even further, uh, we, I've uploaded this.
[00:26:15:800 - 00:26:19:689] **Speaker 1:** Sort of demonstration of using the symbolic toolkit or symbolic
[00:26:19:689 - 00:26:21:250] **Speaker 1:** uh library in Python.
[00:26:21:979 - 00:26:23:910] **Speaker 1:** So maybe you've come across this, maybe you haven't.
[00:26:24:640 - 00:26:28:839] **Speaker 1:** But it's just a way of solving problems, uh, symbolically.
[00:26:29:589 - 00:26:31:959] **Speaker 1:** So instead of discretizing numerically and things like that, we
[00:26:31:959 - 00:26:33:380] **Speaker 1:** can solve solve equations.
[00:26:34:489 - 00:26:39:369] **Speaker 1:** So I've used this to create our uh linear shape
[00:26:39:369 - 00:26:40:000] **Speaker 1:** functions.
[00:26:40:410 - 00:26:41:329] **Speaker 1:** So N1 and 2.
[00:26:42:640 - 00:26:43:339] **Speaker 1:** Can you read?
[00:26:45:040 - 00:26:46:619] **Speaker 1:** Can you read that text or?
[00:26:48:430 - 00:26:49:859] **Speaker 1:** No, um.
[00:26:54:880 - 00:26:56:329] **Speaker 1:** It's a lot of like, yeah.
[00:26:57:150 - 00:26:59:550] **Speaker 1:** And I've got lots of comments in, like a good
[00:26:59:550 - 00:27:00:750] **Speaker 1:** person, good coder.
[00:27:01:189 - 00:27:05:150] **Speaker 1:** Um, so I've got these symbols X X1, 2, U1,
[00:27:05:229 - 00:27:06:349] **Speaker 1:** U2, an A1.
[00:27:06:630 - 00:27:09:390] **Speaker 1:** I've used A and A1 as those constants uh that
[00:27:09:390 - 00:27:10:130] **Speaker 1:** we're trying to figure out.
[00:27:11:819 - 00:27:13:280] **Speaker 1:** This is the interpolation function.
[00:27:13:510 - 00:27:14:160] **Speaker 1:** There we head.
[00:27:15:469 - 00:27:17:979] **Speaker 1:** Defined on Monday.
[00:27:19:979 - 00:27:27:280] **Speaker 1:** So Equation one And we've got two equations that we're
[00:27:27:280 - 00:27:30:010] **Speaker 1:** substituting for the nodal values equations to A and B.
[00:27:31:069 - 00:27:33:930] **Speaker 1:** Uh, we want to solve that set of simultaneous equations,
[00:27:34:050 - 00:27:34:989] **Speaker 1:** so we can use the sim.
[00:27:35:630 - 00:27:37:020] **Speaker 1:** solve method.
[00:27:37:770 - 00:27:40:839] **Speaker 1:** And then we want to substitute back into our um
[00:27:41:550 - 00:27:43:920] **Speaker 1:** Intipollating function, which is our next step.
[00:27:45:150 - 00:27:47:310] **Speaker 1:** We collect the coefficients.
[00:27:47:780 - 00:27:53:229] **Speaker 1:** So we can use expand coefficients of U1 and then
[00:27:53:229 - 00:27:55:310] **Speaker 1:** to simplify, otherwise it gets a bit ugly.
[00:27:56:109 - 00:27:58:349] **Speaker 1:** And then lastly, I wanted to check that we've got
[00:27:58:349 - 00:28:01:910] **Speaker 1:** the right derivatives, D by DX and integral, integral of
[00:28:01:910 - 00:28:02:119] **Speaker 1:** U.
[00:28:02:869 - 00:28:03:689] **Speaker 1:** So we can run that.
[00:28:09:579 - 00:28:11:619] **Speaker 1:** And print out in one.
[00:28:13:979 - 00:28:19:359] **Speaker 1:** So in one And now it's essentially times it by
[00:28:19:359 - 00:28:22:599] **Speaker 1:** -1, so on the bottom we've got X2 minus X1,
[00:28:22:719 - 00:28:24:520] **Speaker 1:** and on the top is X2 minus X.
[00:28:24:939 - 00:28:27:060] **Speaker 1:** So that's N1 and then N2.
[00:28:27:719 - 00:28:29:079] **Speaker 1:** Similar, we've got.
[00:28:30:640 - 00:28:34:030] **Speaker 1:** We should be getting X 1 minus X.
[00:28:35:189 - 00:28:37:709] **Speaker 1:** X1 minus X and X1 minus X2.
[00:28:39:069 - 00:28:41:209] **Speaker 1:** And then the derivatived by DX.
[00:28:44:750 - 00:28:46:239] **Speaker 1:** Again, this is sort of times 1 minus 1.
[00:28:46:319 - 00:28:48:359] **Speaker 1:** You can't sort of decide how it operates.
[00:28:49:660 - 00:28:55:140] **Speaker 1:** But we've got Delta you over X.
[00:28:56:390 - 00:28:57:739] **Speaker 1:** And lastly, into you.
[00:28:59:750 - 00:29:01:349] **Speaker 1:** Oh, that's pretty ugly.
[00:29:02:099 - 00:29:18:770] **Speaker 1:** Um, That's better, um, so.
[00:29:19:630 - 00:29:22:670] **Speaker 1:** That hopefully will resolve what we've got for equation 7.
[00:29:23:650 - 00:29:25:180] **Speaker 1:** And looks about right.
[00:29:27:099 - 00:29:28:819] **Speaker 1:** And we can do the same for quadratic elements, so
[00:29:28:819 - 00:29:30:819] **Speaker 1:** as soon as you start doing more complicated problems, you
[00:29:30:819 - 00:29:32:920] **Speaker 1:** might want to not do this all by hand, so
[00:29:32:920 - 00:29:36:760] **Speaker 1:** you wanna um, Offload that work to to some code.
[00:29:37:599 - 00:29:39:239] **Speaker 1:** So this is for quadratic elements.
[00:29:40:609 - 00:29:42:199] **Speaker 1:** There must be a way of commenting code.
[00:29:45:790 - 00:29:47:510] **Speaker 1:** Control one, OK.
[00:29:54:040 - 00:29:56:920] **Speaker 1:** So we're doing the same steps and just introducing another
[00:29:56:920 - 00:29:58:300] **Speaker 1:** equation for that 3rd node.
[00:30:00:010 - 00:30:05:930] **Speaker 1:** And we've got N1 Into And in 3, so we
[00:30:05:930 - 00:30:07:589] **Speaker 1:** can just double-check that we've got those right.
[00:30:10:619 - 00:30:12:910] **Speaker 1:** So there's shape functions in 2020 B.
[00:30:19:099 - 00:30:23:750] **Speaker 1:** And we can also evaluate those for the quadratic shape
[00:30:23:750 - 00:30:26:270] **Speaker 1:** element without the normalised shire system, so I might have
[00:30:26:270 - 00:30:27:930] **Speaker 1:** used that to create the other code.
[00:30:29:229 - 00:30:31:469] **Speaker 1:** Alright, so just a bit of an introduction to using
[00:30:31:469 - 00:30:34:130] **Speaker 1:** a symbolic uh library in Python.
[00:30:34:670 - 00:30:36:329] **Speaker 1:** You may or may not find it helpful for things.
[00:30:37:489 - 00:30:40:849] **Speaker 1:** Um, Yeah.
[00:30:43:130 - 00:30:43:589] **Speaker 1:** Cool.
[00:30:44:010 - 00:30:48:689] **Speaker 1:** Any questions on what we've covered in chapter 8?
[00:30:55:270 - 00:30:58:180] **Speaker 1:** Christian There was a meme a few years ago and
[00:30:58:180 - 00:30:59:880] **Speaker 1:** they had like, is it the Dominion?
[00:31:00:729 - 00:31:05:650] **Speaker 1:** Dominions, minions, dominions, um, in the class and the teacher
[00:31:05:650 - 00:31:07:130] **Speaker 1:** was like, oh, is there any questions and they're all
[00:31:07:130 - 00:31:08:709] **Speaker 1:** like sitting there very quietly.
[00:31:10:119 - 00:31:12:439] **Speaker 1:** I thought that was quite fun, but um.
[00:31:13:589 - 00:31:15:339] **Speaker 1:** Please sing out if you do have questions.
[00:31:15:469 - 00:31:17:430] **Speaker 1:** It's always a bit more interactive.
[00:31:18:780 - 00:31:22:920] **Speaker 1:** Um, otherwise I'm just talking out to space.
[00:31:23:500 - 00:31:25:339] **Speaker 1:** So we've pretty much done chapter 8.
[00:31:25:739 - 00:31:27:800] **Speaker 1:** Is there anything that you want me to go through?
[00:31:30:050 - 00:31:33:099] **Speaker 1:** For I don't know, the assignment or the quiz or
[00:31:33:099 - 00:31:34:359] **Speaker 1:** anything else that would be helpful.
[00:31:35:339 - 00:31:37:630] **Speaker 1:** Otherwise I can keep marching on to chapter 9.
[00:31:37:750 - 00:31:40:069] **Speaker 1:** I, I did write, I finished off the exam, so
[00:31:40:069 - 00:31:41:250] **Speaker 1:** that's a big relief for me.
[00:31:41:430 - 00:31:43:180] **Speaker 1:** But now it's on you guys to study for the
[00:31:43:180 - 00:31:43:760] **Speaker 1:** exam.
[00:31:44:189 - 00:31:46:709] **Speaker 1:** Um, so I'll talk more about the exam after we've
[00:31:46:709 - 00:31:47:930] **Speaker 1:** finished all the chapters.
[00:31:48:390 - 00:31:50:270] **Speaker 1:** So I won't, I won't get started on that.
[00:31:51:050 - 00:31:51:910] **Speaker 1:** Uh, description.
[00:31:53:420 - 00:31:57:719] **Speaker 1:** Um, OK.
[00:32:02:859 - 00:32:04:319] **Speaker 1:** I could also go through.
[00:32:05:060 - 00:32:07:780] **Speaker 1:** Some optimisation techniques in console.
[00:32:08:849 - 00:32:11:550] **Speaker 1:** Has anyone actually done the last quiz question?
[00:32:12:550 - 00:32:12:939] **Speaker 1:** No.
[00:32:15:040 - 00:32:17:050] **Speaker 1:** I'll try and make up a problem on the fly
[00:32:17:050 - 00:32:18:209] **Speaker 1:** then, um.
[00:32:24:670 - 00:32:28:030] **Speaker 1:** OK, well, maybe it can be related to chatter.
[00:32:29:849 - 00:32:32:589] **Speaker 1:** 23 or 4.
[00:32:33:170 - 00:32:35:349] **Speaker 1:** At one point we were doing.
[00:32:36:619 - 00:32:38:479] **Speaker 1:** That'll be fun, because if it doesn't work then.
[00:32:39:349 - 00:32:41:099] **Speaker 1:** That's gonna be even more fun.
[00:32:42:310 - 00:32:47:109] **Speaker 1:** Um, so chapter 5, we're looking at solving this problem.
[00:32:50:449 - 00:32:54:219] **Speaker 1:** And we had this, this rod with some given length.
[00:32:56:030 - 00:32:58:030] **Speaker 1:** And we had an initial profile that was a sine
[00:32:58:030 - 00:32:59:910] **Speaker 1:** wave that had a peak of 100 °C.
[00:33:00:930 - 00:33:03:229] **Speaker 1:** And we had fixed ends at 0 °C.
[00:33:07:400 - 00:33:08:939] **Speaker 1:** And we're trying to figure out.
[00:33:10:180 - 00:33:11:390] **Speaker 1:** The final time.
[00:33:12:150 - 00:33:13:209] **Speaker 1:** For the max temperature.
[00:33:15:020 - 00:33:17:170] **Speaker 1:** To reach 50 °C.
[00:33:31:780 - 00:33:32:819] **Speaker 1:** That's not gonna work.
[00:33:40:569 - 00:33:47:479] **Speaker 1:** Actually, say for example, we weren't given the, Material property,
[00:33:47:890 - 00:33:49:579] **Speaker 1:** alpha of the copper.
[00:33:50:619 - 00:33:53:099] **Speaker 1:** OK, so, for example, we've got, we've given the heat
[00:33:53:099 - 00:33:53:750] **Speaker 1:** equation.
[00:33:54:760 - 00:33:55:939] **Speaker 1:** Maybe we can write this out.
[00:33:58:880 - 00:34:01:900] **Speaker 1:** So we've got No.
[00:34:15:919 - 00:34:18:689] **Speaker 1:** So we've got DT by DT equal to alpha, D2T
[00:34:18:689 - 00:34:19:459] **Speaker 1:** by DX2.
[00:34:19:719 - 00:34:23:479] **Speaker 1:** We're given that T at X equal to 0 for
[00:34:23:479 - 00:34:25:270] **Speaker 1:** all time is equal to 0.
[00:34:25:679 - 00:34:28:040] **Speaker 1:** Temperature at X equal to L for all times is
[00:34:28:040 - 00:34:28:800] **Speaker 1:** equal to 0.
[00:34:29:500 - 00:34:31:000] **Speaker 1:** And the initial profile.
[00:34:32:049 - 00:34:48:340] **Speaker 1:** Was he got 100 Sign Of pi X over L.
[00:34:51:148 - 00:34:55:479] **Speaker 1:** And we're given alpha, but maybe we're not, so.
[00:34:56:428 - 00:35:04:139] **Speaker 1:** And um Of And what we do know is that
[00:35:05:260 - 00:35:07:040] **Speaker 1:** The temperature.
[00:35:11:449 - 00:35:13:330] **Speaker 1:** At x equal to.
[00:35:14:199 - 00:35:14:879] **Speaker 1:** Aloe 2.
[00:35:17:270 - 00:35:20:429] **Speaker 1:** T Equals TF.
[00:35:21:790 - 00:35:24:530] **Speaker 1:** Which is 6.75 minutes.
[00:35:26:229 - 00:35:28:320] **Speaker 1:** is equal to 50 °C.
[00:35:30:639 - 00:35:33:800] **Speaker 1:** So essentially this is a parameter estimation problem or parameter
[00:35:33:800 - 00:35:35:320] **Speaker 1:** ID and we're going to try and figure out what
[00:35:35:320 - 00:35:35:870] **Speaker 1:** alpha is.
[00:35:38:580 - 00:35:40:540] **Speaker 1:** So just with any sort of problem, it might make
[00:35:40:540 - 00:35:43:419] **Speaker 1:** sense to solve this with I guess for Alpha, just
[00:35:43:419 - 00:35:45:040] **Speaker 1:** to get a feel for what the solution space looks
[00:35:45:040 - 00:35:45:439] **Speaker 1:** like.
[00:35:45:899 - 00:35:47:000] **Speaker 1:** So we're gonna do that in console.
[00:35:56:510 - 00:35:57:929] **Speaker 1:** It's made comes all small.
[00:36:03:709 - 00:36:04:929] **Speaker 1:** Oh, that's gonna be painful.
[00:36:07:719 - 00:36:08:030] **Speaker 1:** Right.
[00:36:09:919 - 00:36:11:659] **Speaker 1:** So this is a one dimensional problem, so we're going
[00:36:11:659 - 00:36:12:840] **Speaker 1:** to set up the 1D.
[00:36:16:050 - 00:36:21:560] **Speaker 1:** On the Heat transfer in solids, so you'll be using
[00:36:21:560 - 00:36:23:159] **Speaker 1:** that anyway for your, for your assignment.
[00:36:24:520 - 00:36:29:280] **Speaker 1:** And The dependent variable field is T, our temperature.
[00:36:29:919 - 00:36:31:899] **Speaker 1:** It's time dependent, it's varying over time.
[00:36:36:179 - 00:36:38:620] **Speaker 1:** And we're gonna set up a parameter L to denote
[00:36:38:620 - 00:36:39:820] **Speaker 1:** the the length of the rod.
[00:36:41:090 - 00:36:53:879] **Speaker 1:** So parameter And he said it was 80 centimetres.
[00:36:59:530 - 00:37:04:590] **Speaker 1:** And We've got a thermal or heativity, alpha.
[00:37:05:810 - 00:37:07:290] **Speaker 1:** And we're gonna guess.
[00:37:08:330 - 00:37:10:889] **Speaker 1:** I mean, it is 1.11 centimetres squared per second.
[00:37:10:969 - 00:37:13:169] **Speaker 1:** Maybe we say that it's 5.
[00:37:18:489 - 00:37:20:060] **Speaker 1:** So 5 centimetres squad per second.
[00:37:20:419 - 00:37:22:659] **Speaker 1:** So in console you can write out the units of
[00:37:22:659 - 00:37:24:889] **Speaker 1:** your choice and it'll convert to the size.
[00:37:24:939 - 00:37:27:820] **Speaker 1:** So we've got 5 times 4 metres squared per second
[00:37:27:820 - 00:37:28:939] **Speaker 1:** as our heat divisivity.
[00:37:29:139 - 00:37:30:739] **Speaker 1:** So sort of a rate of how quickly the heat
[00:37:30:739 - 00:37:31:800] **Speaker 1:** transfers through the domain.
[00:37:33:169 - 00:37:35:780] **Speaker 1:** We've got uh geometry.
[00:37:36:090 - 00:37:38:610] **Speaker 1:** This is a one dimensional domain, so we've got an
[00:37:38:610 - 00:37:40:250] **Speaker 1:** interval from 0 to L.
[00:37:41:889 - 00:37:43:689] **Speaker 1:** So it's sort of pretty similar to what we did
[00:37:43:689 - 00:37:44:050] **Speaker 1:** for that.
[00:37:45:360 - 00:37:50:570] **Speaker 1:** And the material Maybe we introduce a blank material.
[00:37:52:899 - 00:37:55:750] **Speaker 1:** And it requires all these things, which is not helpful.
[00:38:03:389 - 00:38:08:129] **Speaker 1:** All right I'm gonna use the coefficient form PDE.
[00:38:08:379 - 00:38:09:179] **Speaker 1:** So we're going to delete this.
[00:38:09:260 - 00:38:11:659] **Speaker 1:** So this is also, it's it's good when you do
[00:38:11:659 - 00:38:13:699] **Speaker 1:** live demonstrations because I can teach you more things.
[00:38:13:939 - 00:38:15:510] **Speaker 1:** If you want to get rid of this physics interface,
[00:38:15:580 - 00:38:16:280] **Speaker 1:** you can delete it.
[00:38:18:610 - 00:38:23:229] **Speaker 1:** And then go physics, add physics, and we can search
[00:38:23:409 - 00:38:24:570] **Speaker 1:** for coefficient.
[00:38:26:449 - 00:38:27:929] **Speaker 1:** And it's going to apply it to the same one
[00:38:27:929 - 00:38:30:090] **Speaker 1:** so you don't have to close console or restart a
[00:38:30:090 - 00:38:30:590] **Speaker 1:** new model.
[00:38:31:719 - 00:38:34:479] **Speaker 1:** In this case, our dependent variable is still going to
[00:38:34:479 - 00:38:35:219] **Speaker 1:** be temperature.
[00:38:37:590 - 00:38:41:479] **Speaker 1:** And the source term That's carbon per second.
[00:38:47:330 - 00:38:48:790] **Speaker 1:** And an equation that was solving.
[00:38:50:149 - 00:38:52:790] **Speaker 1:** Is this guy, so you don't have any sauce down.
[00:38:54:340 - 00:38:56:379] **Speaker 1:** Our damping or mass coefficients, the one in front of
[00:38:56:379 - 00:38:57:139] **Speaker 1:** DU by T.
[00:38:58:389 - 00:39:03:439] **Speaker 1:** Let's make ourselves our lives a little bit easier and
[00:39:03:439 - 00:39:04:030] **Speaker 1:** call that tea.
[00:39:06:500 - 00:39:09:800] **Speaker 1:** So we've got DT by DT which is not that
[00:39:09:800 - 00:39:10:179] **Speaker 1:** helpful.
[00:39:10:540 - 00:39:12:780] **Speaker 1:** So we've got um a coefficient of one and then
[00:39:12:780 - 00:39:15:979] **Speaker 1:** we've got a coefficient of alpha in front of the
[00:39:15:979 - 00:39:16:739] **Speaker 1:** gradient term.
[00:39:16:959 - 00:39:17:699] **Speaker 1:** So we've chuck that in.
[00:39:19:800 - 00:39:21:300] **Speaker 1:** So that's our equation that we're solving.
[00:39:22:300 - 00:39:24:739] **Speaker 1:** We've been given directly boundary conditions on the left and
[00:39:24:739 - 00:39:26:399] **Speaker 1:** right, so we're going to set.
[00:39:27:800 - 00:39:29:959] **Speaker 1:** There are clear boundary conditions on both points.
[00:39:30:370 - 00:39:31:570] **Speaker 1:** I've just done control A.
[00:39:32:530 - 00:39:37:010] **Speaker 1:** Um, We're going to leave this in Calvin.
[00:39:40:050 - 00:39:40:610] **Speaker 1:** I think.
[00:39:41:300 - 00:39:44:179] **Speaker 1:** Just, just keep the numbers as they are.
[00:39:44:570 - 00:39:47:550] **Speaker 1:** So 00, and the initial profile.
[00:39:50:000 - 00:39:55:870] **Speaker 1:** Is F of X or 100 times sin of pi
[00:39:55:870 - 00:39:56:780] **Speaker 1:** X over L.
[00:40:03:139 - 00:40:05:739] **Speaker 1:** So I've set up the material properties, we've got our
[00:40:05:739 - 00:40:07:340] **Speaker 1:** boundary conditions defining everything.
[00:40:07:459 - 00:40:08:520] **Speaker 1:** We need to create a mesh.
[00:40:09:100 - 00:40:11:659] **Speaker 1:** So the default mesh might be OK, we might want
[00:40:11:659 - 00:40:12:520] **Speaker 1:** to do a bit finer.
[00:40:14:560 - 00:40:18:090] **Speaker 1:** And Maybe we solve.
[00:40:18:370 - 00:40:20:889] **Speaker 1:** So we already know that it's operating on some sort
[00:40:20:889 - 00:40:22:830] **Speaker 1:** of scale of a few minutes.
[00:40:23:260 - 00:40:26:570] **Speaker 1:** We ramped up alpha, so we would expect it to
[00:40:26:570 - 00:40:28:290] **Speaker 1:** cool quicker than that, but maybe we'll go up to
[00:40:28:290 - 00:40:29:149] **Speaker 1:** 10 minutes.
[00:40:29:889 - 00:40:32:889] **Speaker 1:** So we can change the time unit to minutes and
[00:40:32:889 - 00:40:35:850] **Speaker 1:** go up to 10 minutes in steps of 1 minute.
[00:40:37:370 - 00:40:39:189] **Speaker 1:** These are the output times for console.
[00:40:40:520 - 00:40:43:659] **Speaker 1:** So this is not the time steps that console uses.
[00:40:44:129 - 00:40:46:750] **Speaker 1:** We can tighten the time steps by using a tighter
[00:40:46:750 - 00:40:47:340] **Speaker 1:** tolerance.
[00:40:49:169 - 00:40:50:530] **Speaker 1:** But if we compute this.
[00:40:52:560 - 00:40:55:000] **Speaker 1:** This is our temperature profile over time, so you can
[00:40:55:000 - 00:40:57:550] **Speaker 1:** see that it starts off as a sun wave and
[00:40:57:550 - 00:40:58:500] **Speaker 1:** then decays quickly.
[00:41:00:719 - 00:41:05:080] **Speaker 1:** Now, we want to analyse the midpoint, so it would
[00:41:05:080 - 00:41:08:560] **Speaker 1:** be helpful to create a point to select.
[00:41:08:719 - 00:41:11:159] **Speaker 1:** So under geometry, we're going to create a point.
[00:41:11:810 - 00:41:20:989] **Speaker 1:** At all over 2 And compute.
[00:41:23:050 - 00:41:25:850] **Speaker 1:** So under results, we can create a 1D plot group.
[00:41:26:770 - 00:41:28:510] **Speaker 1:** Because we wanted to create a line graph.
[00:41:29:409 - 00:41:31:770] **Speaker 1:** And a point graph.
[00:41:33:060 - 00:41:36:060] **Speaker 1:** Located at the midpoint, so temperature over time.
[00:41:37:320 - 00:41:39:919] **Speaker 1:** So you can see here that it's decaying exponentially as
[00:41:39:919 - 00:41:40:770] **Speaker 1:** you might expect.
[00:41:41:199 - 00:41:42:580] **Speaker 1:** We've gone up to 10 minutes.
[00:41:43:080 - 00:41:46:550] **Speaker 1:** The the point that it passes 50 °C is after
[00:41:46:550 - 00:41:50:800] **Speaker 1:** 1.6 minutes, which is much quicker than 6.75 because we
[00:41:50:800 - 00:41:55:719] **Speaker 1:** had that alpha of 5 centimetres squared instead of 1.
[00:41:59:669 - 00:42:05:510] **Speaker 1:** So now we want to change alpha, so that the
[00:42:05:510 - 00:42:08:070] **Speaker 1:** temperature being evaluated at the midpoint.
[00:42:08:760 - 00:42:10:889] **Speaker 1:** is equal to.
[00:42:11:860 - 00:42:14:379] **Speaker 1:** 50 after some time, and I'm just wondering if that
[00:42:14:379 - 00:42:15:860] **Speaker 1:** is straightforward to do.
[00:42:23:060 - 00:42:23:580] **Speaker 1:** Yes.
[00:42:23:979 - 00:42:27:699] **Speaker 1:** So, If we want to set up a non-local coupling,
[00:42:27:939 - 00:42:31:419] **Speaker 1:** so this was in the hints as well, because it's
[00:42:31:419 - 00:42:33:379] **Speaker 1:** a point, it doesn't really matter what one we select.
[00:42:33:659 - 00:42:34:800] **Speaker 1:** So it's average.
[00:42:36:090 - 00:42:42:989] **Speaker 1:** Of I really want to stick to a point.
[00:42:43:300 - 00:42:43:620] **Speaker 1:** OK.
[00:42:44:620 - 00:42:45:770] **Speaker 1:** So F of 1.
[00:42:47:260 - 00:42:50:770] **Speaker 1:** And we want to set up our optimisation.
[00:42:57:889 - 00:42:58:280] **Speaker 1:** Oh.
[00:43:03:459 - 00:43:06:959] **Speaker 1:** So study, we can add optimisation.
[00:43:07:340 - 00:43:08:959] **Speaker 1:** There's a whole host of different ones and you'll go
[00:43:08:959 - 00:43:12:610] **Speaker 1:** through some of these in the lab this week, but
[00:43:12:610 - 00:43:15:060] **Speaker 1:** the one that I want to use is the general
[00:43:15:060 - 00:43:16:030] **Speaker 1:** optimisation.
[00:43:17:370 - 00:43:19:060] **Speaker 1:** Bobby is quite good for this sort of stuff, it's
[00:43:19:060 - 00:43:21:320] **Speaker 1:** using bound optimisation by a quadratic approximation.
[00:43:22:500 - 00:43:23:489] **Speaker 1:** Some tolerance.
[00:43:23:570 - 00:43:27:169] **Speaker 1:** So when do we reach that optimal value, maybe just
[00:43:27:169 - 00:43:28:229] **Speaker 1:** add a couple of zeros.
[00:43:29:080 - 00:43:30:929] **Speaker 1:** And the objective function that we want to evaluate.
[00:43:31:090 - 00:43:32:649] **Speaker 1:** So what are we trying to evaluate here?
[00:43:33:570 - 00:43:36:389] **Speaker 1:** We're trying to evaluate the temperature.
[00:43:37:899 - 00:43:40:280] **Speaker 1:** At the midpoint at some time.
[00:43:41:090 - 00:43:44:949] **Speaker 1:** At 6.75 minutes, needs to be equal to 50 °C.
[00:43:47:429 - 00:43:50:110] **Speaker 1:** So we want to minimise the discrepancy between our model
[00:43:50:110 - 00:43:51:530] **Speaker 1:** output and this value.
[00:43:56:639 - 00:44:03:239] **Speaker 1:** So It's filling in the time, so that's good, but
[00:44:03:239 - 00:44:04:300] **Speaker 1:** hopefully you're learning things.
[00:44:05:250 - 00:44:10:389] **Speaker 1:** Um, I was, I want to introduce you to the
[00:44:10:389 - 00:44:10:790] **Speaker 1:** at.
[00:44:11:610 - 00:44:18:010] **Speaker 1:** Function or expression, so if we create a, Point evaluation.
[00:44:21:050 - 00:44:23:169] **Speaker 1:** This is just going to list the temperature over time.
[00:44:23:949 - 00:44:25:669] **Speaker 1:** Uh, but we can also do at.
[00:44:26:750 - 00:44:28:449] **Speaker 1:** And I just can't remember the.
[00:44:30:060 - 00:44:31:899] **Speaker 1:** Formatting, um.
[00:44:41:500 - 00:44:43:169] **Speaker 1:** Oh No.
[00:45:01:350 - 00:45:02:760] **Speaker 1:** You can look up online.
[00:45:04:840 - 00:45:09:469] **Speaker 1:** Consult at The whole thing, that's all, that's horrible.
[00:45:13:489 - 00:45:15:070] **Speaker 1:** So at expression.
[00:45:46:959 - 00:45:47:510] **Speaker 1:** OK.
[00:45:47:909 - 00:45:49:929] **Speaker 1:** There is a way to do that, just for now.
[00:45:50:050 - 00:45:52:050] **Speaker 1:** I'm just going to set the final time to be
[00:45:52:050 - 00:45:53:250] **Speaker 1:** 6.75.
[00:45:54:500 - 00:45:56:610] **Speaker 1:** We can save ourselves a little bit of headache.
[00:45:59:330 - 00:46:01:620] **Speaker 1:** So it's going to go up until 6.75.
[00:46:01:659 - 00:46:04:419] **Speaker 1:** It's evaluating this expression at the final time.
[00:46:05:860 - 00:46:07:459] **Speaker 1:** Maybe I'll figure it out after the lecture.
[00:46:07:760 - 00:46:09:060] **Speaker 1:** So evaluating this temperature.
[00:46:10:149 - 00:46:14:649] **Speaker 1:** So we've got EO one, evaluating the temperature.
[00:46:16:590 - 00:46:18:199] **Speaker 1:** At the final time and it needs to be equal
[00:46:18:199 - 00:46:19:149] **Speaker 1:** to 50 degrees.
[00:46:19:590 - 00:46:21:969] **Speaker 1:** So we said that was 50, so we minus 50,
[00:46:22:429 - 00:46:24:070] **Speaker 1:** and then we're going to square it to make it
[00:46:24:070 - 00:46:24:850] **Speaker 1:** quadratic.
[00:46:30:219 - 00:46:33:419] **Speaker 1:** And we need to include comp1.
[00:46:34:020 - 00:46:37:500] **Speaker 1:** the average operator, because it's this is in a global
[00:46:37:500 - 00:46:40:389] **Speaker 1:** space and study, and we need to call component one.av.
[00:46:43:570 - 00:46:45:139] **Speaker 1:** We've got a minimization problem.
[00:46:45:389 - 00:46:47:899] **Speaker 1:** The control variable that we're going to adjust is the
[00:46:47:899 - 00:46:49:080] **Speaker 1:** heat diversivity alpha.
[00:46:49:379 - 00:46:50:699] **Speaker 1:** We're going to start with 5.
[00:46:50:979 - 00:46:52:540] **Speaker 1:** The scale is about 1.
[00:46:53:350 - 00:46:54:909] **Speaker 1:** And we've got some lower bound.
[00:46:55:030 - 00:46:57:550] **Speaker 1:** Maybe we don't want to go below 0.1 and above
[00:46:57:550 - 00:46:57:949] **Speaker 1:** 10.
[00:47:02:979 - 00:47:03:550] **Speaker 1:** Well like.
[00:47:04:709 - 00:47:05:830] **Speaker 1:** Oh, OK.
[00:47:06:830 - 00:47:09:379] **Speaker 1:** 0.1 centimetres squared per second.
[00:47:11:629 - 00:47:12:189] **Speaker 1:** Units.
[00:47:12:310 - 00:47:14:290] **Speaker 1:** This is, we're learning lots.
[00:47:14:590 - 00:47:15:649] **Speaker 1:** Units are really important.
[00:47:17:719 - 00:47:20:909] **Speaker 1:** And compute, see what happens.
[00:47:21:729 - 00:47:25:439] **Speaker 1:** Oh, Oh, that's right, we want to get rid of
[00:47:25:439 - 00:47:26:000] **Speaker 1:** that act.
[00:47:41:530 - 00:47:42:620] **Speaker 1:** Hopefully it's working.
[00:47:44:060 - 00:47:46:370] **Speaker 1:** Yeah Um.
[00:47:48:500 - 00:47:51:399] **Speaker 1:** So it's got and done a few steps.
[00:47:51:979 - 00:47:54:419] **Speaker 1:** We can see that it started at 5 times centimetre
[00:47:54:419 - 00:47:56:379] **Speaker 1:** 4, and it's gone down to 2.8.
[00:47:57:379 - 00:47:58:919] **Speaker 1:** It's not changing too much.
[00:47:59:760 - 00:48:04:250] **Speaker 1:** Um, we're expecting 1.11 from our analysis.
[00:48:05:699 - 00:48:07:379] **Speaker 1:** So we might still have some homework to do.
[00:48:09:100 - 00:48:11:219] **Speaker 1:** Um the maximum temperature a little bit.
[00:48:12:989 - 00:48:14:790] **Speaker 1:** Well, it should be the average of a point, but
[00:48:14:790 - 00:48:16:729] **Speaker 1:** it should be located at the max.
[00:48:21:520 - 00:48:25:000] **Speaker 1:** Um So should we take the average temperature at this
[00:48:25:000 - 00:48:25:260] **Speaker 1:** point?
[00:48:44:260 - 00:48:46:679] **Speaker 1:** OK, I might have just been sensitive to the, the
[00:48:46:679 - 00:48:47:239] **Speaker 1:** tolerance.
[00:48:48:060 - 00:48:49:669] **Speaker 1:** So we've got an objective.
[00:48:49:830 - 00:48:52:989] **Speaker 1:** So the difference between the two temperatures squared, T square
[00:48:53:550 - 00:48:55:139] **Speaker 1:** is down to 10 to -5.
[00:48:55:310 - 00:48:58:409] **Speaker 1:** So we're at 1.24 centimetres squared per second.
[00:49:00:560 - 00:49:02:820] **Speaker 1:** And we might reduce that further.
[00:49:04:590 - 00:49:06:290] **Speaker 1:** Seems to be very sensitive to this.
[00:49:07:419 - 00:49:08:040] **Speaker 1:** Tolerance.
[00:49:13:750 - 00:49:15:070] **Speaker 1:** Cool, now we're getting small numbers.
[00:49:15:270 - 00:49:16:810] **Speaker 1:** So now we're getting 1.24.
[00:49:17:429 - 00:49:19:590] **Speaker 1:** Uh, we might want to look at the mesh refinement.
[00:49:20:919 - 00:49:23:479] **Speaker 1:** So if we have a more refined mesh.
[00:49:32:320 - 00:49:32:790] **Speaker 1:** 100.
[00:49:38:840 - 00:49:39:570] **Speaker 1:** Oh dear.
[00:49:51:840 - 00:49:53:830] **Speaker 1:** Just, we'll just do extremely extremely fine.
[00:49:53:850 - 00:49:55:919] **Speaker 1:** I think I have to, OK, I'll do, I'll do
[00:49:55:919 - 00:49:56:899] **Speaker 1:** this step just for.
[00:49:58:229 - 00:50:14:540] **Speaker 1:** Um, OK, it's getting hooked up at 1.24.
[00:50:14:840 - 00:50:16:949] **Speaker 1:** So it's getting close, so we're getting close to what
[00:50:16:949 - 00:50:17:620] **Speaker 1:** we expect.
[00:50:17:879 - 00:50:20:159] **Speaker 1:** Um, I'll have a bit of a dive into what's
[00:50:20:159 - 00:50:22:000] **Speaker 1:** going on there, uh, but it might just be the
[00:50:22:000 - 00:50:22:820] **Speaker 1:** mesh resolution.
[00:50:23:159 - 00:50:27:169] **Speaker 1:** So we're using, A discrete numerical model, uh, and obviously
[00:50:27:169 - 00:50:28:649] **Speaker 1:** this is the analytical true solution.
[00:50:28:929 - 00:50:31:169] **Speaker 1:** So hopefully this, I don't know if it gives you
[00:50:31:169 - 00:50:33:129] **Speaker 1:** confidence or not for the quiz, but um hopefully you
[00:50:33:129 - 00:50:35:110] **Speaker 1:** get all the steps that are required for the quiz.
[00:50:35:340 - 00:50:38:830] **Speaker 1:** And, and that, that should be all good.
[00:50:39:239 - 00:50:41:889] **Speaker 1:** So tomorrow we'll get started on chapter 9.
[00:50:44:280 - 00:50:45:469] **Speaker 1:** And we'll, we'll see you then.
[00:51:51:639 - 00:52:01:899] **Speaker 1:** No, I Nice.
[00:52:41:260 - 00:52:41:580] **Speaker 0:** it was.

# ENME302-26S2 Lecture 31 native Echo transcript

Date: September 17, 2026 10:00am-10:55am
Transcript type: native Echo automated transcript.

[00:00:18:370 - 00:00:18:379] **Speaker 0:** are.
[00:00:19:829 - 00:00:20:079] **Speaker 0:** That's what.
[00:00:26:950 - 00:00:32:360] **Speaker 0:** I I I don't know, I.
[00:00:45:310 - 00:00:45:319] **Speaker 0:** I.
[00:00:49:740 - 00:00:53:970] **Speaker 0:** I Uh, good morning, we'll make a start.
[00:00:55:630 - 00:00:57:259] **Speaker 1:** It's a bit wet, maybe that's.
[00:00:58:259 - 00:01:00:659] **Speaker 1:** An excuse for, for staying at home.
[00:01:01:099 - 00:01:04:300] **Speaker 1:** Um, so any questions before we get stuck into chapter
[00:01:04:300 - 00:01:04:800] **Speaker 1:** 6?
[00:01:09:430 - 00:01:09:940] **Speaker 1:** Cool.
[00:01:10:379 - 00:01:12:889] **Speaker 1:** So chapter 5, we derived the heat equation and solved
[00:01:12:889 - 00:01:16:660] **Speaker 1:** it analytically using separation of variables and that self-similar or
[00:01:16:660 - 00:01:18:419] **Speaker 1:** method of similarity solutions as well.
[00:01:19:150 - 00:01:21:819] **Speaker 1:** Uh, today we're gonna go through how to solve these
[00:01:21:819 - 00:01:25:220] **Speaker 1:** PDEs, uh, with a finite different scheme, so a numerical
[00:01:25:220 - 00:01:25:230] **Speaker 1:** method.
[00:01:27:160 - 00:01:29:120] **Speaker 1:** So the key steps are quite similar to what we
[00:01:29:120 - 00:01:31:279] **Speaker 1:** did for the elliptic, uh, PDE.
[00:01:32:080 - 00:01:33:779] **Speaker 1:** The only difference is now that we've got a time
[00:01:33:949 - 00:01:36:480] **Speaker 1:** derivative, DT by DT, so we have to march forward
[00:01:36:480 - 00:01:36:959] **Speaker 1:** in time.
[00:01:38:000 - 00:01:39:239] **Speaker 1:** So, our PDE.
[00:01:40:339 - 00:01:43:790] **Speaker 1:** Uh, contains derivatives in both space and time, and we're
[00:01:43:790 - 00:01:46:309] **Speaker 1:** going to discretize these a little bit differently.
[00:01:47:139 - 00:01:49:830] **Speaker 1:** So we're going to discretize in space to start with,
[00:01:50:269 - 00:01:52:470] **Speaker 1:** just as we did for the Laplace equation, and then
[00:01:52:470 - 00:01:54:769] **Speaker 1:** we're gonna Discretize.
[00:01:56:680 - 00:01:59:669] **Speaker 1:** These discrete points in space, so T subscript I, I
[00:01:59:669 - 00:02:02:349] **Speaker 1:** being the X index, we're going to march forward in
[00:02:02:349 - 00:02:02:610] **Speaker 1:** time.
[00:02:04:849 - 00:02:07:050] **Speaker 1:** So the example that we're going to analyse is the
[00:02:07:050 - 00:02:10:100] **Speaker 1:** heat equation because it's really short and simple to solve
[00:02:10:399 - 00:02:11:110] **Speaker 1:** arguably.
[00:02:11:649 - 00:02:15:089] **Speaker 1:** So we've got a temporal derivative on the left and
[00:02:15:089 - 00:02:16:679] **Speaker 1:** that diffusion term on the right.
[00:02:17:380 - 00:02:20:110] **Speaker 1:** So we're going to discretize this equation in space using
[00:02:20:110 - 00:02:21:830] **Speaker 1:** the, uh, central difference scheme.
[00:02:22:169 - 00:02:25:690] **Speaker 1:** So you can recall that our 2nd order derivative, 2nd-order
[00:02:25:690 - 00:02:28:529] **Speaker 1:** accurate, finite difference stencil has this form.
[00:02:28:690 - 00:02:30:190] **Speaker 1:** So a node to the left.
[00:02:33:919 - 00:02:35:770] **Speaker 1:** And a node to the right.
[00:02:36:919 - 00:02:40:750] **Speaker 1:** And we, yeah, and we have a 2nd order accurate
[00:02:40:750 - 00:02:41:039] **Speaker 1:** scheme.
[00:02:41:080 - 00:02:43:360] **Speaker 1:** So we've got some remainder residual that scales with data
[00:02:43:360 - 00:02:43:759] **Speaker 1:** X2.
[00:02:44:610 - 00:02:46:720] **Speaker 1:** And we apply this for all of our nodes, I
[00:02:46:880 - 00:02:48:449] **Speaker 1:** equal to 1 through N.
[00:02:50:619 - 00:02:51:649] **Speaker 1:** Now we want to integrate.
[00:02:54:970 - 00:02:57:820] **Speaker 1:** Our equation 6.2 in time.
[00:02:58:289 - 00:03:02:550] **Speaker 1:** So for the time derivative, we want to divide.
[00:03:03:250 - 00:03:07:470] **Speaker 1:** That continuous time into discrete time steps, and each time
[00:03:07:470 - 00:03:08:970] **Speaker 1:** step is labelled with delta D.
[00:03:10:279 - 00:03:13:139] **Speaker 1:** So nothing too different to our data X's, it's just
[00:03:13:139 - 00:03:13:630] **Speaker 1:** in time.
[00:03:15:119 - 00:03:20:020] **Speaker 1:** And The time level, we'll use superscripts.
[00:03:22:479 - 00:03:26:100] **Speaker 1:** In To denote the nth time.
[00:03:27:699 - 00:03:30:800] **Speaker 1:** And the next time level, 10 + 1 + 1.
[00:03:32:160 - 00:03:35:990] **Speaker 1:** Is equal to TN plus delta T.
[00:03:38:800 - 00:03:42:710] **Speaker 1:** And lowercase n starts at 0 for our initial condition
[00:03:42:889 - 00:03:44:369] **Speaker 1:** and then marches forward in time.
[00:03:49:899 - 00:03:52:100] **Speaker 1:** So that's our time set out of T.
[00:03:52:339 - 00:03:57:179] **Speaker 1:** We're going to define our discretized temperature T.
[00:03:58:029 - 00:04:01:750] **Speaker 1:** At position I at time level in with that superscript.
[00:04:02:410 - 00:04:06:460] **Speaker 1:** So TIN is equal to TI evaluated at the time
[00:04:06:460 - 00:04:07:149] **Speaker 1:** step TN.
[00:04:09:679 - 00:04:12:179] **Speaker 1:** So some nomenclature just to.
[00:04:14:130 - 00:04:15:059] **Speaker 1:** Are you on the same page?
[00:04:16:200 - 00:04:18:359] **Speaker 1:** So we've defined our time setting.
[00:04:19:278 - 00:04:21:118] **Speaker 1:** Now, how do we discretize over time?
[00:04:22:739 - 00:04:25:720] **Speaker 1:** So using our finite difference approximation for our time derivative
[00:04:25:720 - 00:04:27:079] **Speaker 1:** on the left-hand side.
[00:04:28:299 - 00:04:32:119] **Speaker 1:** Uh, we can Have equations that are formed to step
[00:04:32:119 - 00:04:33:640] **Speaker 1:** through over time.
[00:04:35:480 - 00:04:37:720] **Speaker 1:** Now, we have to make a choice of when to
[00:04:37:720 - 00:04:39:109] **Speaker 1:** evaluate those derivatives.
[00:04:39:480 - 00:04:40:579] **Speaker 1:** So we've got derivatives.
[00:04:44:350 - 00:04:46:700] **Speaker 1:** That we're approximating so that diffusion on the right-hand side,
[00:04:46:989 - 00:04:50:190] **Speaker 1:** do we evaluate this expression at the current time step
[00:04:50:190 - 00:04:51:329] **Speaker 1:** or at the next time step?
[00:04:53:239 - 00:04:57:799] **Speaker 1:** So an explicit method is when we uh use a
[00:04:57:799 - 00:04:59:260] **Speaker 1:** time derivative on the left-hand side.
[00:05:01:959 - 00:05:05:859] **Speaker 1:** Expressed in terms of t at the n + 1
[00:05:05:859 - 00:05:07:399] **Speaker 1:** and nth time step.
[00:05:08:170 - 00:05:10:970] **Speaker 1:** And the right-hand side is only evaluated at the previous
[00:05:10:970 - 00:05:11:670] **Speaker 1:** time levels.
[00:05:12:049 - 00:05:17:980] **Speaker 1:** So Essentially In other words, uh, the left-hand side, we
[00:05:17:980 - 00:05:19:279] **Speaker 1:** do a one-sided difference.
[00:05:19:589 - 00:05:21:920] **Speaker 1:** So you can think back to your Euler method.
[00:05:22:529 - 00:05:24:339] **Speaker 1:** Uh, on the right-hand side we're gonna evaluate all of
[00:05:24:339 - 00:05:28:179] **Speaker 1:** these temperature values at N, so at the previous time
[00:05:28:179 - 00:05:28:500] **Speaker 1:** level.
[00:05:30:149 - 00:05:32:769] **Speaker 1:** So it's explicit, we can calculate TI.
[00:05:34:579 - 00:05:36:119] **Speaker 1:** N + 1 explicitly.
[00:05:36:980 - 00:05:40:070] **Speaker 1:** Because it's only a function of the previous time.
[00:05:41:040 - 00:06:00:709] **Speaker 1:** In And for the implicit scheme.
[00:06:02:859 - 00:06:05:339] **Speaker 1:** Uh, both the current and past information is going to
[00:06:05:339 - 00:06:08:459] **Speaker 1:** be included in the evaluation for that derivative, that diffusion
[00:06:08:459 - 00:06:08:739] **Speaker 1:** term.
[00:06:10:250 - 00:06:15:920] **Speaker 1:** So Now we're evaluating our next temperature, TIN plus one.
[00:06:17:899 - 00:06:18:880] **Speaker 1:** There's some other functions.
[00:06:18:980 - 00:06:21:279] **Speaker 1:** So F and G are just sort of general functions
[00:06:21:820 - 00:06:24:859] **Speaker 1:** of TI minus 1.
[00:06:27:329 - 00:06:29:940] **Speaker 1:** TITI plus one.
[00:06:30:850 - 00:06:33:720] **Speaker 1:** So the implicit method we're evaluating at N +1.
[00:06:36:140 - 00:06:39:859] **Speaker 1:** For the side notes and TIN for the the centre
[00:06:39:859 - 00:06:40:100] **Speaker 1:** node.
[00:06:46:890 - 00:06:49:959] **Speaker 1:** So it's usually easier to try and visualise this on
[00:06:49:959 - 00:06:50:480] **Speaker 1:** a stencil.
[00:06:50:649 - 00:06:51:920] **Speaker 1:** So I'll just sketch a grid.
[00:06:53:179 - 00:06:58:010] **Speaker 1:** So if we have Oh.
[00:06:58:809 - 00:07:00:829] **Speaker 1:** Current step, level 1.
[00:07:05:119 - 00:07:05:940] **Speaker 1:** T equals DN.
[00:07:06:880 - 00:07:10:720] **Speaker 1:** And we have 11 + 1, I minus 1.
[00:07:14:309 - 00:07:15:570] **Speaker 1:** And that's level N.
[00:07:23:089 - 00:07:27:459] **Speaker 1:** The Equals TN plus 1.
[00:07:30:600 - 00:07:33:679] **Speaker 1:** So we're going down in time advancing.
[00:07:34:170 - 00:07:35:320] **Speaker 1:** We've got N + 1.
[00:07:36:429 - 00:07:38:109] **Speaker 1:** I in +1.
[00:07:39:019 - 00:07:40:859] **Speaker 1:** I + 1, N + 1.
[00:07:43:309 - 00:07:45:160] **Speaker 1:** So that first row is just the same as we
[00:07:45:160 - 00:07:46:179] **Speaker 1:** did before.
[00:07:46:359 - 00:07:49:040] **Speaker 1:** We've got a discretized one-dimensional domain, and then we're going
[00:07:49:040 - 00:07:50:440] **Speaker 1:** to march forward in time.
[00:07:50:760 - 00:07:52:359] **Speaker 1:** So a fully explicit scheme.
[00:07:53:190 - 00:07:54:609] **Speaker 1:** I only using information.
[00:08:00:920 - 00:08:04:559] **Speaker 1:** From the previous time level and rearranging for the temperature
[00:08:04:559 - 00:08:05:899] **Speaker 1:** at IN + 1.
[00:08:08:089 - 00:08:10:869] **Speaker 1:** So the only unknown in that evaluation is the the
[00:08:10:869 - 00:08:13:329] **Speaker 1:** next time step at TIN +1.
[00:08:20:570 - 00:08:21:790] **Speaker 1:** So that's fully explicit.
[00:08:24:149 - 00:08:26:049] **Speaker 1:** And then for implicit.
[00:08:32:559 - 00:08:35:280] **Speaker 1:** I've just said that TIN plus one is now going
[00:08:35:280 - 00:08:37:679] **Speaker 1:** to be evaluated from the neighbouring nodes at the next
[00:08:37:679 - 00:08:38:299] **Speaker 1:** time level.
[00:08:39:080 - 00:08:41:599] **Speaker 1:** And the value at TIN.
[00:08:54:250 - 00:08:57:900] **Speaker 1:** So we're still evaluating those derivatives, that second order derivative
[00:08:57:900 - 00:08:58:419] **Speaker 1:** in space.
[00:08:58:770 - 00:09:01:780] **Speaker 1:** Uh, we're just deciding, are we evaluating it at the
[00:09:01:780 - 00:09:03:489] **Speaker 1:** previous time level or the next time level.
[00:09:04:010 - 00:09:07:700] **Speaker 1:** So it can sound somewhat arbitrary, but If we choose
[00:09:07:700 - 00:09:08:599] **Speaker 1:** the implicit method.
[00:09:09:820 - 00:09:11:260] **Speaker 1:** We have 3 unknowns.
[00:09:12:390 - 00:09:14:010] **Speaker 1:** So that's why it's implicit.
[00:09:14:630 - 00:09:17:630] **Speaker 1:** So unknowns at the current time set appear on both
[00:09:17:630 - 00:09:20:049] **Speaker 1:** sides of the equation, and what we end up with
[00:09:20:049 - 00:09:22:190] **Speaker 1:** is a set of algebraic equations that have to be
[00:09:22:190 - 00:09:23:590] **Speaker 1:** solved simultaneously.
[00:09:24:869 - 00:09:26:500] **Speaker 1:** So it has a little bit of added complexity.
[00:09:27:309 - 00:09:30:830] **Speaker 1:** Um, but there are advantages as well, so we'll go
[00:09:30:830 - 00:09:31:830] **Speaker 1:** through each of these two.
[00:09:32:979 - 00:09:36:059] **Speaker 1:** Schemes in detail in this chapter, uh, but that's just
[00:09:36:059 - 00:09:38:460] **Speaker 1:** a brief overview of the, the, the difference.
[00:09:39:890 - 00:09:40:309] **Speaker 1:** All right.
[00:09:41:010 - 00:09:43:929] **Speaker 1:** So we'll go through the explicit scheme first because it's
[00:09:43:929 - 00:09:44:890] **Speaker 1:** a bit easier to think of.
[00:09:45:330 - 00:09:49:049] **Speaker 1:** So the forward in time, central in space is the
[00:09:49:049 - 00:09:49:929] **Speaker 1:** explicit scheme.
[00:09:56:770 - 00:10:00:010] **Speaker 1:** And this is gonna be used for our ODE.
[00:10:02:119 - 00:10:03:559] **Speaker 1:** And we can use.
[00:10:05:020 - 00:10:07:570] **Speaker 1:** For example, the all the explicit method to integrate over
[00:10:07:570 - 00:10:09:000] **Speaker 1:** time, so DT.
[00:10:10:229 - 00:10:16:020] **Speaker 1:** IDT Evaluated at some point or some node I.
[00:10:19:349 - 00:10:23:549] **Speaker 1:** is going to be equal to TIN + 1 minus
[00:10:23:549 - 00:10:27:030] **Speaker 1:** TIN divided by delta T.
[00:10:36:369 - 00:10:37:679] **Speaker 1:** So this is a one-sided difference.
[00:10:37:760 - 00:10:41:340] **Speaker 1:** We looked at central, uh, difference, second-order accuracy before.
[00:10:41:880 - 00:10:44:039] **Speaker 1:** Uh, it's only one-sided difference if you look at the
[00:10:44:039 - 00:10:46:599] **Speaker 1:** Taylor series expansions and go and derive this, you'll find
[00:10:46:599 - 00:10:48:000] **Speaker 1:** that it's only first-order accurate.
[00:10:48:200 - 00:10:52:520] **Speaker 1:** So we're going to scale with order delta T instead
[00:10:52:520 - 00:10:53:479] **Speaker 1:** of T2.
[00:11:02:270 - 00:11:05:150] **Speaker 1:** Um, I guess other features of this derivative instead of
[00:11:06:140 - 00:11:09:179] **Speaker 1:** Changing in X or Y, we're obviously evaluating the change
[00:11:09:179 - 00:11:11:369] **Speaker 1:** in temperature at a fixed point, which is why we're
[00:11:11:369 - 00:11:15:099] **Speaker 1:** holding a constant, the index I, and we're changing the
[00:11:15:099 - 00:11:16:539] **Speaker 1:** time level and to end + 1.
[00:11:19:539 - 00:11:23:580] **Speaker 1:** So we've got our uh description for the spatial derivative
[00:11:23:580 - 00:11:26:419] **Speaker 1:** and the time derivative, and we're gonna combine these.
[00:11:27:179 - 00:11:29:000] **Speaker 1:** Together into our heat equation.
[00:11:29:380 - 00:11:31:059] **Speaker 1:** So the temporal term we've got T.
[00:11:32:000 - 00:11:36:520] **Speaker 1:** IN + 1 minus TIN divided by delta T.
[00:11:39:820 - 00:11:42:580] **Speaker 1:** So what we're doing is substituting equation 5 back into
[00:11:42:580 - 00:11:44:739] **Speaker 1:** our heat equation and then on the right hand side
[00:11:44:739 - 00:11:47:580] **Speaker 1:** we've got alpha multiplied by our diffusion.
[00:11:50:000 - 00:11:51:119] **Speaker 1:** Second order derivative.
[00:11:53:640 - 00:11:58:719] **Speaker 1:** So we've got TI minus 1 minus 2 TI plus
[00:11:58:719 - 00:11:59:919] **Speaker 1:** TI + 1.
[00:12:00:940 - 00:12:02:619] **Speaker 1:** Divided by delta X2.
[00:12:06:159 - 00:12:07:799] **Speaker 1:** This is the explicit scheme.
[00:12:07:960 - 00:12:11:349] **Speaker 1:** So we're going to evaluate these temperatures at the previous
[00:12:11:349 - 00:12:12:960] **Speaker 1:** time level, time level N.
[00:12:13:520 - 00:12:15:640] **Speaker 1:** So these superscripts are all in.
[00:12:24:669 - 00:12:27:909] **Speaker 1:** Now, the only unknown that we're trying to calculate in
[00:12:27:909 - 00:12:30:450] **Speaker 1:** this equation is TIN plus 1.
[00:12:30:950 - 00:12:35:030] **Speaker 1:** All of the other temperature values are known, the previous
[00:12:35:030 - 00:12:35:429] **Speaker 1:** value.
[00:12:36:400 - 00:12:39:049] **Speaker 1:** So we can rearrange for that one unknown, TIN plus
[00:12:39:049 - 00:12:39:380] **Speaker 1:** 1.
[00:12:43:440 - 00:12:44:619] **Speaker 1:** As we call it TIN.
[00:12:46:109 - 00:12:52:549] **Speaker 1:** Plus Al Delta T over X 2.
[00:12:54:619 - 00:12:56:309] **Speaker 1:** Multiplied by T.
[00:12:57:150 - 00:13:02:710] **Speaker 1:** I minus 1, N minus 2 TIN and TI plus
[00:13:02:710 - 00:13:03:469] **Speaker 1:** 1 N.
[00:13:06:859 - 00:13:09:710] **Speaker 1:** So again, that right-hand side is evaluated the old time
[00:13:09:710 - 00:13:12:229] **Speaker 1:** step, so it's fully explicit, we can calculate it without
[00:13:12:229 - 00:13:14:010] **Speaker 1:** any coupled system of equations.
[00:13:24:260 - 00:13:24:700] **Speaker 1:** All right.
[00:13:25:380 - 00:13:28:280] **Speaker 1:** So what we're gonna do next is consider an example.
[00:13:28:659 - 00:13:31:440] **Speaker 1:** So if we have a grid with a length of
[00:13:31:440 - 00:13:32:760] **Speaker 1:** 10 centimetres.
[00:13:33:390 - 00:13:35:299] **Speaker 1:** And we've got a spacing for each one of 2
[00:13:35:299 - 00:13:38:130] **Speaker 1:** centimetres and an initial temperature of 0.
[00:13:39:940 - 00:13:41:380] **Speaker 1:** Uh, we can visualise the domain.
[00:13:41:719 - 00:13:43:359] **Speaker 1:** So we've got 5.
[00:13:45:609 - 00:13:47:719] **Speaker 1:** Intervals and 6 grid points.
[00:13:50:900 - 00:13:54:260] **Speaker 1:** And the left-hand boundary, we've got 100 °C, and on
[00:13:54:260 - 00:13:55:380] **Speaker 1:** the right, we've got 50.
[00:13:55:630 - 00:13:57:799] **Speaker 1:** So if it starts at zero, we would expect the
[00:13:58:380 - 00:13:59:619] **Speaker 1:** domain to heat up over time.
[00:14:01:450 - 00:14:03:830] **Speaker 1:** And we're going to apply our finite differencing.
[00:14:04:450 - 00:14:08:900] **Speaker 1:** So first we're going to evaluate that group of Variables,
[00:14:08:909 - 00:14:11:400] **Speaker 1:** alpha delta T over delta X2, and we're going to
[00:14:11:400 - 00:14:13:460] **Speaker 1:** label this lambda just for convenience.
[00:14:15:539 - 00:14:20:940] **Speaker 1:** So lambda is equal to alphaDeltaT over X2.
[00:14:24:520 - 00:14:27:219] **Speaker 1:** Uh, I've been told that alpha, that heat difficivity is
[00:14:27:219 - 00:14:29:419] **Speaker 1:** 8.835.
[00:14:30:969 - 00:14:32:390] **Speaker 1:** centimetre squared per second.
[00:14:33:719 - 00:14:35:380] **Speaker 1:** Uh, we've got a time step.
[00:14:36:390 - 00:14:37:489] **Speaker 1:** Of 0.1.
[00:14:39:609 - 00:14:40:830] **Speaker 1:** And I'll.
[00:14:42:390 - 00:14:45:950] **Speaker 1:** Uh, interval spacing data X is 2.
[00:14:48:729 - 00:14:49:929] **Speaker 1:** So it's over 2 squad.
[00:14:50:489 - 00:14:52:330] **Speaker 1:** And this is 0.0.
[00:14:53:369 - 00:14:56:900] **Speaker 1:** 20875.
[00:15:07:440 - 00:15:10:320] **Speaker 1:** So there are left and right boundary conditions.
[00:15:11:239 - 00:15:13:820] **Speaker 1:** Uh thus setting the temperature to be those values.
[00:15:14:159 - 00:15:15:820] **Speaker 1:** So the only nodes that we're trying to figure out
[00:15:15:820 - 00:15:18:719] **Speaker 1:** with our finite differencing is those interior ones, T1, 23,
[00:15:18:760 - 00:15:19:260] **Speaker 1:** and 4.
[00:15:20:159 - 00:15:22:599] **Speaker 1:** So we're going to evaluate equation 6 for each of
[00:15:22:599 - 00:15:23:340] **Speaker 1:** those 4.
[00:15:24:080 - 00:15:27:159] **Speaker 1:** you can see that the lambda term is constant and
[00:15:27:159 - 00:15:29:380] **Speaker 1:** we're just going to cycle through i equal.
[00:15:31:619 - 00:15:33:130] **Speaker 1:** 123 and 4.
[00:15:34:409 - 00:15:39:849] **Speaker 1:** So for I equal to 1, we've got T11.
[00:15:40:789 - 00:15:43:960] **Speaker 1:** Equal to T1 0.
[00:15:46:729 - 00:15:48:250] **Speaker 1:** And this is going to be equal to 0.
[00:15:51:590 - 00:15:57:429] **Speaker 1:** Plus Lambda, which we said was 0.02.
[00:15:58:280 - 00:16:00:710] **Speaker 1:** 0875.
[00:16:03:090 - 00:16:05:570] **Speaker 1:** And then we've got TI minus 1.
[00:16:06:479 - 00:16:07:719] **Speaker 1:** So that's gonna be T0.
[00:16:11:369 - 00:16:19:570] **Speaker 1:** Uh, then we've got -2T10 plus T20.
[00:16:28:140 - 00:16:30:299] **Speaker 1:** So T1 is the temperature at this node.
[00:16:30:500 - 00:16:33:299] **Speaker 1:** We said the initial temperature was 0 °C, so that's
[00:16:33:299 - 00:16:34:119] **Speaker 1:** equal to 0.
[00:16:35:929 - 00:16:37:650] **Speaker 1:** Uh, T naught.
[00:16:38:890 - 00:16:41:429] **Speaker 1:** It is always going to be 100 °C.
[00:16:45:549 - 00:16:47:890] **Speaker 1:** Uh, T10 we just said was 0.
[00:16:48:609 - 00:16:51:090] **Speaker 1:** And TE2, the initial temperature is also going to be
[00:16:51:090 - 00:16:51:450] **Speaker 1:** zero.
[00:16:52:200 - 00:16:54:859] **Speaker 1:** So if you evaluate this, we've got 100 times 0.02
[00:16:55:000 - 00:16:59:919] **Speaker 1:** and we're left with 2.0875.
[00:17:01:929 - 00:17:05:579] **Speaker 1:** So after 0.1 seconds, we've evaluated the temperature at that
[00:17:05:579 - 00:17:09:250] **Speaker 1:** first node to be 2 degrees, so it's increased by
[00:17:09:250 - 00:17:09:910] **Speaker 1:** 2 degrees.
[00:17:14:709 - 00:17:17:670] **Speaker 1:** Now we need to apply this finite differencing to all
[00:17:17:670 - 00:17:19:589] **Speaker 1:** interior nodes for that first time step.
[00:17:20:588 - 00:17:21:848] **Speaker 1:** So for I equal to 2.
[00:17:26:290 - 00:17:28:199] **Speaker 1:** The temperature at node 2, T2.
[00:17:28:930 - 00:17:35:010] **Speaker 1:** At that first time level 1 is equal to T20.
[00:17:36:810 - 00:17:46:849] **Speaker 1:** Plus lambda, so 0.020875 multiplied by, T One not.
[00:17:47:569 - 00:17:51:890] **Speaker 1:** -2 T20 plus T3.
[00:17:59:439 - 00:18:02:000] **Speaker 1:** So if you think back to the Liben method we
[00:18:02:000 - 00:18:06:560] **Speaker 1:** had, we're always using the latest iteration of the temperature
[00:18:06:560 - 00:18:09:439] **Speaker 1:** values, but in this case, we're using the temperature value
[00:18:09:439 - 00:18:10:859] **Speaker 1:** of the previous time level.
[00:18:12:089 - 00:18:15:939] **Speaker 1:** So T10 is the initial temperature, which was zero.
[00:18:16:939 - 00:18:18:329] **Speaker 1:** T2 and T3.
[00:18:27:229 - 00:18:29:510] **Speaker 1:** So we do the same for nodes 3 and 4,
[00:18:29:739 - 00:18:31:939] **Speaker 1:** I equal 3 and 4, and we end up with
[00:18:31:939 - 00:18:33:859] **Speaker 1:** 0 and 1.04 degrees.
[00:18:37:130 - 00:18:41:800] **Speaker 1:** And Now that we have our temperature distribution, we might
[00:18:41:800 - 00:18:45:239] **Speaker 1:** want to plot, What that looks like.
[00:18:49:939 - 00:18:52:540] **Speaker 1:** So on the x axis goes up to 10.
[00:18:53:650 - 00:18:56:010] **Speaker 1:** And vertical we've got 100.
[00:18:58:520 - 00:19:02:329] **Speaker 1:** Degrees and 50 being the boundaries.
[00:19:09:050 - 00:19:13:209] **Speaker 1:** So initial condition, it's got 1234.
[00:19:18:609 - 00:19:19:849] **Speaker 1:** Has 0.
[00:19:20:849 - 00:19:22:339] **Speaker 1:** Degrees on the anterior.
[00:19:33:000 - 00:19:34:510] **Speaker 1:** I could use a different colour, maybe.
[00:19:40:819 - 00:19:44:329] **Speaker 1:** And we just evaluated our temperature profile at 0.1 seconds
[00:19:44:329 - 00:19:45:219] **Speaker 1:** using one-time stat.
[00:19:46:130 - 00:19:47:930] **Speaker 1:** The boundary conditions remain unchanged.
[00:19:48:130 - 00:19:49:270] **Speaker 1:** They don't change over time.
[00:19:50:930 - 00:19:53:449] **Speaker 1:** And the temperature value at node 1, we said was
[00:19:53:449 - 00:19:54:189] **Speaker 1:** equal to 2.
[00:19:56:949 - 00:20:00:109] **Speaker 1:** And the temperature value at node 4 was 1.
[00:20:02:020 - 00:20:03:459] **Speaker 1:** Maybe it's not to scale and the other one's a
[00:20:03:459 - 00:20:03:959] **Speaker 1:** 0.
[00:20:15:030 - 00:20:17:709] **Speaker 1:** All right, so I've march forward and one time set.
[00:20:19:640 - 00:20:23:359] **Speaker 1:** So we repeat this process as iterative for all the
[00:20:23:359 - 00:20:25:219] **Speaker 1:** other time steps that we want to continue with.
[00:20:25:680 - 00:20:27:079] **Speaker 1:** So at 0.2 seconds.
[00:20:29:290 - 00:20:32:530] **Speaker 1:** We're going to evaluate those interior nodes, T1, 23 and
[00:20:32:530 - 00:20:33:390] **Speaker 1:** 4 again.
[00:20:33:930 - 00:20:34:920] **Speaker 1:** So we've got T1.
[00:20:36:089 - 00:20:40:469] **Speaker 1:** This time we're looking at the time level for 2.
[00:20:41:520 - 00:20:44:540] **Speaker 1:** So The first node is T1, 2.
[00:20:45:260 - 00:20:50:770] **Speaker 1:** Is equal to T1 at the previous time level.
[00:20:51:800 - 00:20:53:119] **Speaker 1:** So that's going to be one.
[00:20:59:839 - 00:21:04:329] **Speaker 1:** And Still using this equation 6, we've got lambda multiplied
[00:21:04:329 - 00:21:10:540] **Speaker 1:** by Turns, so we've got 0.020875.
[00:21:11:770 - 00:21:19:430] **Speaker 1:** And we've got Taught Evaluated at time level one.
[00:21:21:359 - 00:21:23:920] **Speaker 1:** -21.
[00:21:25:060 - 00:21:29:020] **Speaker 1:** 1 + T 21.
[00:21:31:900 - 00:21:34:939] **Speaker 1:** So again, all we're doing is changing the subscripts.
[00:21:35:650 - 00:21:37:050] **Speaker 1:** This is based on the central different scheme.
[00:21:37:089 - 00:21:39:739] **Speaker 1:** We've got the left, right, and then minus 2 of
[00:21:39:739 - 00:21:40:339] **Speaker 1:** the centre.
[00:21:41:099 - 00:21:43:359] **Speaker 1:** The superscripts denote that it was the previous time level,
[00:21:43:459 - 00:21:44:579] **Speaker 1:** so they're all at time level one.
[00:21:46:719 - 00:21:48:479] **Speaker 1:** And that pattern continues for the others.
[00:21:48:839 - 00:21:51:880] **Speaker 1:** So if we calculated this, it's 4.08.
[00:21:52:709 - 00:21:53:469] **Speaker 1:** 78.
[00:22:01:530 - 00:22:08:760] **Speaker 1:** I don't know if I've got A working pin for
[00:22:08:760 - 00:22:09:680] **Speaker 1:** another colour, but.
[00:22:11:560 - 00:22:19:530] **Speaker 1:** Um So again, the boundary conditions remain unchanged.
[00:22:21:099 - 00:22:24:359] **Speaker 1:** We've got a temperature value of 4, so it's doubled.
[00:22:26:369 - 00:22:29:469] **Speaker 1:** And 2 on that side.
[00:22:30:099 - 00:22:34:540] **Speaker 1:** So the interior ones or the middle nodes have grown.
[00:22:35:410 - 00:22:38:079] **Speaker 1:** A fraction, so it's up to 0.02 and 0.04.
[00:22:39:380 - 00:22:41:260] **Speaker 1:** Good luck trying to plot that.
[00:22:55:000 - 00:22:57:829] **Speaker 1:** So obviously that becomes very tedious very quickly.
[00:23:01:890 - 00:23:05:459] **Speaker 1:** Um, but it lends itself well to like a script
[00:23:05:459 - 00:23:07:500] **Speaker 1:** or a code to go through and do some for
[00:23:07:500 - 00:23:08:400] **Speaker 1:** loops for us.
[00:23:09:199 - 00:23:10:290] **Speaker 1:** So that's what we've done.
[00:23:27:449 - 00:23:29:040] **Speaker 1:** And spider's loading, so.
[00:23:30:420 - 00:23:32:189] **Speaker 1:** Uh, have a think about how you might code this,
[00:23:32:229 - 00:23:32:609] **Speaker 1:** maybe.
[00:23:33:390 - 00:23:36:910] **Speaker 1:** Um, your outer four loop has to be time because
[00:23:36:920 - 00:23:37:869] **Speaker 1:** we're marching forward in time.
[00:23:37:949 - 00:23:40:270] **Speaker 1:** The inner loop will be the spatial terms.
[00:23:40:709 - 00:23:43:150] **Speaker 1:** So you're toggling over each of the interior nodes and
[00:23:43:150 - 00:23:45:410] **Speaker 1:** then on the outside you're looping over time.
[00:24:10:869 - 00:24:12:079] **Speaker 1:** I don't know, it's gone super small.
[00:24:12:140 - 00:24:12:739] **Speaker 1:** I didn't do that.
[00:24:18:760 - 00:24:19:540] **Speaker 1:** Yeah, all right.
[00:24:20:000 - 00:24:20:400] **Speaker 1:** So.
[00:24:22:060 - 00:24:25:260] **Speaker 1:** Some parameters, we have to define a final time, otherwise
[00:24:25:260 - 00:24:26:420] **Speaker 1:** it's just going to go on forever.
[00:24:26:780 - 00:24:29:380] **Speaker 1:** So we've got TF of 100 seconds, we've got some
[00:24:29:380 - 00:24:31:500] **Speaker 1:** length of the domain being 0.1 metres.
[00:24:33:300 - 00:24:34:420] **Speaker 1:** Our thermal facility.
[00:24:34:709 - 00:24:37:099] **Speaker 1:** I've converted this to SI units because it's much easier
[00:24:37:099 - 00:24:39:800] **Speaker 1:** to type and, uh, not make mistakes.
[00:24:40:339 - 00:24:43:239] **Speaker 1:** So I guess you're good at commenting code hopefully by
[00:24:43:239 - 00:24:45:660] **Speaker 1:** now, uh, but you want to be descriptive of what
[00:24:45:660 - 00:24:48:130] **Speaker 1:** each variable represents, and I like to include the units
[00:24:48:130 - 00:24:49:239] **Speaker 1:** as well, just to be sure.
[00:24:50:969 - 00:24:52:250] **Speaker 1:** Uh, setting up the grid.
[00:24:52:650 - 00:24:55:089] **Speaker 1:** So we've got a grid, not only in space but
[00:24:55:089 - 00:24:55:689] **Speaker 1:** time as well.
[00:24:55:890 - 00:24:59:930] **Speaker 1:** So we've got uh X coordinates and then temporal coordinates.
[00:25:00:719 - 00:25:08:689] **Speaker 1:** To evaluate Now, the number of time steps will be
[00:25:08:689 - 00:25:10:410] **Speaker 1:** one more than.
[00:25:11:599 - 00:25:14:060] **Speaker 1:** The number of nodes, just as we said with um
[00:25:15:880 - 00:25:19:180] **Speaker 1:** We've got one more nodes than spacings.
[00:25:19:839 - 00:25:22:640] **Speaker 1:** We have 1 more time than the time steps.
[00:25:22:920 - 00:25:24:939] **Speaker 1:** So if we do 100 times steps, we've got 101
[00:25:25:239 - 00:25:27:560] **Speaker 1:** time instances to keep track of because we have the
[00:25:27:560 - 00:25:28:319] **Speaker 1:** initial condition.
[00:25:28:599 - 00:25:29:719] **Speaker 1:** So that's why I've got +1.
[00:25:31:109 - 00:25:32:530] **Speaker 1:** Our lambda is our coefficient.
[00:25:33:930 - 00:25:38:709] **Speaker 1:** We've got X coordinates, we Uh evaluating the X coordinates
[00:25:38:709 - 00:25:40:650] **Speaker 1:** in a 4 loop for for fun.
[00:25:41:270 - 00:25:44:030] **Speaker 1:** Um, we've got time also being evaluated in a 4
[00:25:44:030 - 00:25:44:290] **Speaker 1:** loop.
[00:25:44:390 - 00:25:46:050] **Speaker 1:** Obviously you could do this directly.
[00:25:46:560 - 00:25:48:609] **Speaker 1:** And then we've got an array of zeros.
[00:25:49:150 - 00:25:52:430] **Speaker 1:** The initial temperature profile is set to 0 everywhere.
[00:25:54:329 - 00:25:58:530] **Speaker 1:** And then we set the boundary conditions and Toggling only
[00:25:58:530 - 00:26:01:390] **Speaker 1:** for 4 loops over the interior nodes, so the boundary
[00:26:01:390 - 00:26:04:790] **Speaker 1:** conditions are unchanged, because we know what value they hold,
[00:26:04:869 - 00:26:07:670] **Speaker 1:** we can populate that prior to the 4 loops and
[00:26:07:670 - 00:26:09:239] **Speaker 1:** just don't interact with them.
[00:26:09:589 - 00:26:11:630] **Speaker 1:** Another approach would be to have a 4 loop and
[00:26:11:630 - 00:26:14:239] **Speaker 1:** then set those boundary conditions for each loop.
[00:26:15:380 - 00:26:21:109] **Speaker 1:** As you wish This equation Of code on on line
[00:26:21:109 - 00:26:23:750] **Speaker 1:** 29 is our equation 6.
[00:26:25:420 - 00:26:28:150] **Speaker 1:** And for plotting, ah, this is just a way of
[00:26:28:150 - 00:26:32:260] **Speaker 1:** plotting an array against a one-dimensional array or a 2D
[00:26:32:260 - 00:26:37:180] **Speaker 1:** array versus one array, and every one steps, so you
[00:26:37:180 - 00:26:38:569] **Speaker 1:** can change that as well.
[00:26:41:949 - 00:26:43:099] **Speaker 1:** So this one's blowing up.
[00:26:45:239 - 00:26:48:920] **Speaker 1:** For for a reason, so we jumped ahead, so I
[00:26:48:920 - 00:26:50:520] **Speaker 1:** want to do a smaller time step to start with,
[00:26:50:640 - 00:26:52:859] **Speaker 1:** I think we're on to 0.5.
[00:27:00:479 - 00:27:02:020] **Speaker 1:** So here's our temperature distribution.
[00:27:02:619 - 00:27:05:119] **Speaker 1:** I guess it would be quite nice to plot the
[00:27:05:119 - 00:27:07:359] **Speaker 1:** lines with the colour gradient so that you can see
[00:27:07:359 - 00:27:09:270] **Speaker 1:** where 0 is.
[00:27:09:599 - 00:27:11:439] **Speaker 1:** But we know that it starts on the bottom and
[00:27:11:439 - 00:27:14:760] **Speaker 1:** then it increases and the steady-state solution is just a
[00:27:14:760 - 00:27:15:760] **Speaker 1:** line in between the two.
[00:27:16:739 - 00:27:20:750] **Speaker 1:** So If we look back at equation one, this is
[00:27:20:750 - 00:27:22:010] **Speaker 1:** the heat equation that we're solving.
[00:27:22:949 - 00:27:26:510] **Speaker 1:** Um, steady state means that it's not changing with time.
[00:27:26:959 - 00:27:29:829] **Speaker 1:** So if DT by DT is equal to 0, we've
[00:27:29:829 - 00:27:31:849] **Speaker 1:** got a second order derivative in space.
[00:27:33:050 - 00:27:34:010] **Speaker 1:** And we can solve that.
[00:27:34:170 - 00:27:36:329] **Speaker 1:** We can integrate it twice, and we end up with
[00:27:36:329 - 00:27:36:839] **Speaker 1:** a line.
[00:27:37:160 - 00:27:38:349] **Speaker 1:** That's, that's what we.
[00:27:39:459 - 00:27:40:800] **Speaker 1:** That's what we expect.
[00:27:41:339 - 00:27:44:380] **Speaker 1:** And we've got this linear temperature distribution from 100 down
[00:27:44:380 - 00:27:44:859] **Speaker 1:** to 50.
[00:27:46:010 - 00:27:49:020] **Speaker 1:** That comment I did I made earlier, instead of plotting
[00:27:49:020 - 00:27:53:060] **Speaker 1:** every line, you can plot every inth, so it gets
[00:27:53:060 - 00:27:54:540] **Speaker 1:** a bit hectic if you have too many lines on
[00:27:54:540 - 00:27:55:119] **Speaker 1:** a plot.
[00:27:57:810 - 00:27:59:599] **Speaker 1:** So that's fewer, fewer lines.
[00:28:00:520 - 00:28:02:760] **Speaker 1:** You may know that or maybe Chat GBT knows that
[00:28:02:760 - 00:28:03:020] **Speaker 1:** already.
[00:28:04:199 - 00:28:08:510] **Speaker 1:** Um And I want to look at.
[00:28:09:400 - 00:28:10:520] **Speaker 1:** Uh, different time step.
[00:28:11:000 - 00:28:13:560] **Speaker 1:** So if we increase the time step, we're going to
[00:28:13:560 - 00:28:16:079] **Speaker 1:** get to the final solution quicker because we have fewer
[00:28:16:079 - 00:28:16:869] **Speaker 1:** time steps, right?
[00:28:17:239 - 00:28:19:579] **Speaker 1:** So if we have a time step that is twice,
[00:28:20:670 - 00:28:30:180] **Speaker 1:** So equal to 1 Uh, we still approach that city-state
[00:28:30:180 - 00:28:32:900] **Speaker 1:** solution, uh, in a quicker, quicker manner.
[00:28:34:079 - 00:28:35:689] **Speaker 1:** If we keep increasing the time set.
[00:28:37:219 - 00:28:38:280] **Speaker 1:** For example, 5.
[00:28:40:810 - 00:28:41:910] **Speaker 1:** We run into some trouble.
[00:28:42:810 - 00:28:46:489] **Speaker 1:** So I don't know if you can read this, but
[00:28:46:489 - 00:28:49:650] **Speaker 1:** this vertical axis is on the scale of 109.
[00:28:50:709 - 00:28:52:270] **Speaker 1:** And we can see it doesn't make sense.
[00:28:52:349 - 00:28:55:670] **Speaker 1:** We've got really, really big temperatures for a start that
[00:28:55:670 - 00:28:57:400] **Speaker 1:** are outside of our boundary conditions.
[00:28:57:630 - 00:28:59:859] **Speaker 1:** So that's a red flag, and we've got negative temperatures,
[00:28:59:869 - 00:29:00:989] **Speaker 1:** which we don't expect either.
[00:29:02:729 - 00:29:04:729] **Speaker 1:** So what is going on in this case?
[00:29:05:920 - 00:29:09:670] **Speaker 1:** So we've essentially demonstrated uh instability of our numerical solution
[00:29:10:050 - 00:29:11:819] **Speaker 1:** based on our selection of the time step data T.
[00:29:14:540 - 00:29:18:130] **Speaker 1:** So we're gonna analyse what this means and look a
[00:29:18:130 - 00:29:22:380] **Speaker 1:** little bit about convergence and stability of our numerical schemes.
[00:29:24:910 - 00:29:27:709] **Speaker 1:** So hopefully if you plotted this somewhere, you would have
[00:29:27:709 - 00:29:30:510] **Speaker 1:** caught that it's wrong, um, and not just carried on
[00:29:30:510 - 00:29:30:910] **Speaker 1:** with it.
[00:29:33:199 - 00:29:35:550] **Speaker 1:** I want to show you why this is happening.
[00:29:36:939 - 00:29:38:770] **Speaker 1:** So this is one of the limitations of the explicit
[00:29:38:770 - 00:29:39:130] **Speaker 1:** scheme.
[00:29:40:800 - 00:29:44:510] **Speaker 1:** So convergence First of all, it means that as we
[00:29:44:510 - 00:29:46:930] **Speaker 1:** reduce data T, so our time step and our spatial
[00:29:46:930 - 00:29:51:150] **Speaker 1:** grid sizing data X to zero, our numerical solution tends
[00:29:51:150 - 00:29:52:310] **Speaker 1:** towards the true solution.
[00:29:52:780 - 00:29:58:229] **Speaker 1:** So our discretized form TIN tends to the true solution
[00:29:58:229 - 00:29:58:469] **Speaker 1:** T.
[00:29:59:989 - 00:30:01:069] **Speaker 1:** At point X and T.
[00:30:03:020 - 00:30:06:510] **Speaker 1:** So that's convergence, and we looked at convergence a little
[00:30:06:510 - 00:30:08:540] **Speaker 1:** bit so far with that wrench example in console.
[00:30:08:589 - 00:30:10:589] **Speaker 1:** This week you're looking at the simply supported beam and
[00:30:10:589 - 00:30:11:790] **Speaker 1:** looking at mesh convergence there.
[00:30:13:439 - 00:30:18:729] **Speaker 1:** Stability Uh, is another concept, so stability means that errors
[00:30:18:729 - 00:30:21:890] **Speaker 1:** at any stage of our computation are not amplified, so
[00:30:21:890 - 00:30:23:750] **Speaker 1:** they're not getting bigger and bigger as we go forward
[00:30:23:750 - 00:30:24:270] **Speaker 1:** in time.
[00:30:25:239 - 00:30:28:709] **Speaker 1:** Uh, but are reduced or attenuated as the computation, uh,
[00:30:28:719 - 00:30:29:130] **Speaker 1:** progresses.
[00:30:30:150 - 00:30:31:500] **Speaker 1:** So stability.
[00:30:32:729 - 00:30:35:130] **Speaker 1:** So stability of the solution and convergence of the solution
[00:30:35:489 - 00:30:38:729] **Speaker 1:** is satisfied for our explicit forward in time central in
[00:30:38:729 - 00:30:39:510] **Speaker 1:** space scheme.
[00:30:40:459 - 00:30:43:890] **Speaker 1:** Provided that coefficient lambda that we labelled earlier.
[00:30:44:890 - 00:30:45:989] **Speaker 1:** is small enough.
[00:30:46:449 - 00:30:48:189] **Speaker 1:** So lambda, we said was alpha.
[00:30:49:410 - 00:30:52:170] **Speaker 1:** Delta T Over delta X2.
[00:30:53:819 - 00:30:55:459] **Speaker 1:** Is this n or equal to 12?
[00:30:57:599 - 00:31:01:400] **Speaker 1:** So if this lambda value gets too big, our, our
[00:31:01:400 - 00:31:04:069] **Speaker 1:** solution won't converge or it won't be stable.
[00:31:05:739 - 00:31:08:859] **Speaker 1:** And we'll come back to this concept of convergence, stability,
[00:31:08:939 - 00:31:12:140] **Speaker 1:** consistency of numerical methods later on in chapter 11.
[00:31:12:810 - 00:31:17:260] **Speaker 1:** Uh, but for now, I'm just, uh, providing this value
[00:31:17:260 - 00:31:17:949] **Speaker 1:** of half.
[00:31:18:579 - 00:31:19:979] **Speaker 1:** So lambda has to be less than or equal to
[00:31:19:979 - 00:31:20:410] **Speaker 1:** 12.
[00:31:22:969 - 00:31:28:140] **Speaker 1:** As you can see, if we, Um, increase the, if
[00:31:28:140 - 00:31:31:699] **Speaker 1:** we, if we decrease, uh, this grid spacing, so if
[00:31:31:699 - 00:31:34:180] **Speaker 1:** we want a more refined mesh, that means we have
[00:31:34:180 - 00:31:35:300] **Speaker 1:** to reduce the time step.
[00:31:35:989 - 00:31:37:050] **Speaker 1:** Um, as well.
[00:31:38:449 - 00:31:39:930] **Speaker 1:** So rearranging for data T.
[00:31:41:599 - 00:31:43:650] **Speaker 1:** We know that our time set has to be less
[00:31:43:650 - 00:31:44:699] **Speaker 1:** than or equal to 12.
[00:31:46:040 - 00:31:50:449] **Speaker 1:** Of that X 2 Over Afa.
[00:31:52:380 - 00:31:54:209] **Speaker 1:** So it's not a linear relationship.
[00:31:55:270 - 00:31:59:290] **Speaker 1:** Um If we halve data X we're gonna have to
[00:31:59:290 - 00:32:01:369] **Speaker 1:** reduce data T by a factor of 4.
[00:32:06:530 - 00:32:08:550] **Speaker 1:** So this stability criterion is very limiting.
[00:32:12:130 - 00:32:15:439] **Speaker 1:** So if you go about, uh, refining your mesh because
[00:32:15:439 - 00:32:17:969] **Speaker 1:** you want to get mesh convergence, you have to take
[00:32:17:969 - 00:32:20:609] **Speaker 1:** more time steps, which means that your computation is going
[00:32:20:609 - 00:32:22:489] **Speaker 1:** to take much longer to solve, not just for solving
[00:32:22:489 - 00:32:25:050] **Speaker 1:** those extra nodes, but also the extra time steps.
[00:32:31:589 - 00:32:34:969] **Speaker 1:** So that's the disadvantage for for the scheme, uh.
[00:32:35:939 - 00:32:38:239] **Speaker 1:** Uh, an advantage is that it's very simple to solve
[00:32:38:239 - 00:32:40:010] **Speaker 1:** or calculate in code.
[00:32:40:339 - 00:32:41:699] **Speaker 1:** So you saw that it was only a few lines
[00:32:41:699 - 00:32:42:939] **Speaker 1:** of code in Python.
[00:32:46:589 - 00:32:49:619] **Speaker 1:** And I just want to show a little bit of
[00:32:49:619 - 00:32:53:439] **Speaker 1:** a demonstration of where this half, uh, factor comes from.
[00:32:54:140 - 00:32:56:079] **Speaker 1:** Uh, it's not very vigorous, but if we just think
[00:32:56:079 - 00:32:59:020] **Speaker 1:** of Tea.
[00:32:59:959 - 00:33:03:170] **Speaker 1:** I N + 1, so equation 6.
[00:33:05:689 - 00:33:07:229] **Speaker 1:** We're just gonna expand this bracket.
[00:33:08:349 - 00:33:15:510] **Speaker 1:** So TIN + 1 equals to Lambda TI minus 1
[00:33:15:510 - 00:33:15:829] **Speaker 1:** N.
[00:33:16:979 - 00:33:19:339] **Speaker 1:** Plus 1 minus 2 dam.
[00:33:20:880 - 00:33:25:550] **Speaker 1:** TIN Plus lambda TI plus one.
[00:33:32:780 - 00:33:35:140] **Speaker 1:** Now we know that the temperature distribution within the rod
[00:33:35:140 - 00:33:38:239] **Speaker 1:** is going to be always positive or at least 0.
[00:33:39:709 - 00:33:42:109] **Speaker 1:** So the temperature at the next time level has to
[00:33:42:109 - 00:33:44:069] **Speaker 1:** be also positive or equal to 0.
[00:33:45:319 - 00:33:49:109] **Speaker 1:** Which means that these coefficients can't be negative.
[00:33:50:979 - 00:33:55:420] **Speaker 1:** So already lambda is equal to alpha delta T over
[00:33:55:420 - 00:33:56:099] **Speaker 1:** X2.
[00:33:56:270 - 00:33:57:449] **Speaker 1:** They're all positive values.
[00:33:57:780 - 00:34:01:579] **Speaker 1:** So heat divisivity, time step, spacing, they're all positive, so
[00:34:01:579 - 00:34:02:099] **Speaker 1:** that's fine.
[00:34:13:039 - 00:34:14:849] **Speaker 1:** Uh, so the only coefficient here that we're gonna look
[00:34:14:849 - 00:34:16:388] **Speaker 1:** at is 1 minus 2 lambda.
[00:34:19:060 - 00:34:21:729] **Speaker 1:** 1 minus 2 lambda has to be greater than or
[00:34:21:729 - 00:34:22:689] **Speaker 1:** equal to 0.
[00:34:23:760 - 00:34:25:370] **Speaker 1:** For that solution to be stable.
[00:34:28:719 - 00:34:30:810] **Speaker 1:** Rearranging for lambda, we find that lambda has to be
[00:34:30:810 - 00:34:31:840] **Speaker 1:** less than equal to 15.
[00:34:41:350 - 00:34:43:510] **Speaker 1:** So yeah, in summary, too big a time set that
[00:34:43:510 - 00:34:46:090] **Speaker 1:** becomes unstable ah for this explicit scheme.
[00:34:47:120 - 00:34:49:929] **Speaker 1:** And we need to keep track of this uh coefficient
[00:34:49:929 - 00:34:52:250] **Speaker 1:** lambda to make sure that we've got a stable solution.
[00:34:53:529 - 00:35:04:729] **Speaker 1:** Um I think we've labour the point, but we can
[00:35:04:729 - 00:35:05:219] **Speaker 1:** also look at.
[00:35:06:739 - 00:35:07:899] **Speaker 1:** For that 5.
[00:35:09:750 - 00:35:11:250] **Speaker 1:** Don't know why it keeps changing size.
[00:35:14:110 - 00:35:15:530] **Speaker 1:** I'll just tell you what value it is.
[00:35:17:350 - 00:35:22:850] **Speaker 1:** Um 1.04, so that's greater than a half, um, and
[00:35:22:850 - 00:35:24:750] **Speaker 1:** one second is obviously going to be 1/5 of that,
[00:35:24:929 - 00:35:25:250] **Speaker 1:** so.
[00:35:26:580 - 00:35:37:550] **Speaker 1:** Um 0.20875.
[00:35:39:439 - 00:35:39:449] **Speaker 1:** Alright.
[00:35:41:379 - 00:35:41:580] **Speaker 1:** I don't know.
[00:35:41:659 - 00:35:42:800] **Speaker 1:** Hopefully I've convinced you there.
[00:35:43:300 - 00:35:45:530] **Speaker 1:** So that's the convergence and stability of the scheme.
[00:35:45:899 - 00:35:49:219] **Speaker 1:** Uh, so some pros and cons there, and we've done
[00:35:49:219 - 00:35:50:260] **Speaker 1:** the directly boundary condition.
[00:35:50:300 - 00:35:52:060] **Speaker 1:** It's really straightforward because we don't have to do anything.
[00:35:52:100 - 00:35:54:080] **Speaker 1:** We just include it in our, in our series.
[00:35:54:820 - 00:35:58:659] **Speaker 1:** We're also needing to discretize the, the Neumann boundary condition,
[00:35:58:820 - 00:35:59:989] **Speaker 1:** so the temperature gradient.
[00:36:00:689 - 00:36:04:360] **Speaker 1:** So boundary conditions involving the derivatives Neumann, uh, can also
[00:36:04:360 - 00:36:07:110] **Speaker 1:** be implemented using those ghost nodes that we looked at
[00:36:07:110 - 00:36:07:379] **Speaker 1:** before.
[00:36:08:439 - 00:36:11:280] **Speaker 1:** So we have a temperature gradient being imposed on the
[00:36:11:280 - 00:36:13:760] **Speaker 1:** left-hand boundary here equal to the greater.
[00:36:16:899 - 00:36:21:949] **Speaker 1:** And if we discretize our equation at node 0, we
[00:36:21:949 - 00:36:24:439] **Speaker 1:** have T1.
[00:36:25:979 - 00:36:28:060] **Speaker 1:** Equal to T not not.
[00:36:29:929 - 00:36:30:959] **Speaker 1:** Plus lambda.
[00:36:31:699 - 00:36:33:719] **Speaker 1:** And then we've got the value on the left-hand side,
[00:36:33:939 - 00:36:35:580] **Speaker 1:** so T minus 1.
[00:36:36:949 - 00:36:41:760] **Speaker 1:** -200 and T10.
[00:36:43:260 - 00:36:46:629] **Speaker 1:** So that same sensor we've got 111, 1 + 1,
[00:36:47:020 - 00:36:49:659] **Speaker 1:** all evaluated at the previous time level or the initial
[00:36:49:659 - 00:36:51:179] **Speaker 1:** condition at time level 0.
[00:36:52:860 - 00:36:55:270] **Speaker 1:** Now T minus 1 is our ghost node.
[00:37:10:969 - 00:37:14:540] **Speaker 1:** And we want to discretize our boundary condition, that derivative
[00:37:14:540 - 00:37:15:600] **Speaker 1:** DT by the X.
[00:37:26:379 - 00:37:30:969] **Speaker 1:** So We've been discretizing our spatial terms with the central
[00:37:30:969 - 00:37:34:790] **Speaker 1:** difference scheme, and we're going to continue with that approach.
[00:37:35:449 - 00:37:38:929] **Speaker 1:** So DT by DX at that left-hand boundary.
[00:37:45:580 - 00:37:49:320] **Speaker 1:** Is gonna be rise over run, so we've got T1
[00:37:49:459 - 00:37:51:179] **Speaker 1:** minus T minus 1.
[00:37:52:479 - 00:37:53:919] **Speaker 1:** Divided by 2 X.
[00:37:56:699 - 00:37:58:100] **Speaker 1:** We've been told this is equal to beta.
[00:37:59:739 - 00:38:01:399] **Speaker 1:** And this boundary condition.
[00:38:02:350 - 00:38:05:790] **Speaker 1:** Because it's explicit we're evaluating the temperature values at the
[00:38:05:790 - 00:38:06:669] **Speaker 1:** previous time level.
[00:38:12:239 - 00:38:15:270] **Speaker 1:** We want to eliminate this ghost node or ghost point
[00:38:15:270 - 00:38:18:800] **Speaker 1:** on our main equation, so we're going to rearrange for
[00:38:18:810 - 00:38:20:520] **Speaker 1:** T minus 1.
[00:38:25:179 - 00:38:29:860] **Speaker 1:** Which is equal to T10 minus 2.
[00:38:31:090 - 00:38:33:409] **Speaker 1:** Beta X.
[00:38:44:229 - 00:38:49:719] **Speaker 1:** So substituting in our ghost point, we've got T01 equal
[00:38:49:719 - 00:38:51:560] **Speaker 1:** to T00.
[00:38:52:739 - 00:38:57:419] **Speaker 1:** Plus lambda, now we've got 2 times T1 0.
[00:38:59:260 - 00:39:07:389] **Speaker 1:** -2 X minus 200, so we've eliminated that ghost node
[00:39:07:389 - 00:39:09:229] **Speaker 1:** from our equation so we're not solving for it in
[00:39:09:229 - 00:39:11:280] **Speaker 1:** our, Uh, solution process.
[00:39:16:429 - 00:39:19:310] **Speaker 1:** Uh, this boundary condition applies for all time, so it's
[00:39:19:310 - 00:39:21:020] **Speaker 1:** being imposed for each time level.
[00:39:21:800 - 00:39:23:280] **Speaker 1:** So it applies for all the time steps.
[00:39:27:610 - 00:39:31:909] **Speaker 1:** Any questions on how we've Done this explicit scheme.
[00:39:32:310 - 00:39:34:169] **Speaker 1:** We've used Boiler's method.
[00:39:35:580 - 00:39:37:729] **Speaker 1:** Applied the same central differenceerencing scheme that we've done so
[00:39:37:729 - 00:39:40:040] **Speaker 1:** far and boundary conditions similar as well.
[00:39:42:540 - 00:39:43:790] **Speaker 1:** Hopefully it's all sort of clear.
[00:39:45:459 - 00:39:45:479] **Speaker 1:** All right.
[00:39:46:620 - 00:39:48:780] **Speaker 1:** Um, so the next step is we're going to look
[00:39:48:780 - 00:39:49:899] **Speaker 1:** at the implicit scheme.
[00:39:50:260 - 00:39:53:510] **Speaker 1:** So I said earlier that this scheme depends on multiple
[00:39:53:510 - 00:39:54:830] **Speaker 1:** values at the next time level.
[00:39:55:169 - 00:39:58:500] **Speaker 1:** So if we think back to our sensors, the red
[00:39:58:500 - 00:40:01:629] **Speaker 1:** outline indicates that the next time level has multiple unknowns.
[00:40:01:939 - 00:40:03:540] **Speaker 1:** So we're going to form the system of equations that
[00:40:03:540 - 00:40:04:280] **Speaker 1:** we're going to solve.
[00:40:10:189 - 00:40:12:830] **Speaker 1:** So the limitations of our explicit scheme, uh, is going
[00:40:12:830 - 00:40:14:510] **Speaker 1:** to be overcome by choosing this implicit scheme.
[00:40:14:550 - 00:40:17:270] **Speaker 1:** It's going to be unconditionally stable, so much better.
[00:40:18:120 - 00:40:20:320] **Speaker 1:** So the spatial derivative is going to be evaluated at
[00:40:20:320 - 00:40:22:120] **Speaker 1:** the next time level in +1.
[00:40:23:219 - 00:40:28:370] **Speaker 1:** So T IN + 1 minus TIN over delta T,
[00:40:28:689 - 00:40:29:679] **Speaker 1:** that remains unchanged.
[00:40:29:729 - 00:40:31:989] **Speaker 1:** It's that one-sided difference for time derivative.
[00:40:34:929 - 00:40:38:330] **Speaker 1:** This is equal to our thermal diversivity, and then we've
[00:40:38:330 - 00:40:39:330] **Speaker 1:** got our spatial term.
[00:40:41:760 - 00:40:47:300] **Speaker 1:** TI -1, -2 TI + TI + 1.
[00:40:48:270 - 00:40:49:750] **Speaker 1:** Divided by data X2.
[00:40:52:060 - 00:40:54:060] **Speaker 1:** Now we've just said that this is an implicit scheme.
[00:40:54:659 - 00:40:57:050] **Speaker 1:** The temperature values are going to be evaluated at the
[00:40:57:050 - 00:40:59:860] **Speaker 1:** next time level, so at N + 1.
[00:41:01:270 - 00:41:02:510] **Speaker 1:** So I've got Superscripts.
[00:41:03:459 - 00:41:05:250] **Speaker 1:** Of N + 1.
[00:41:11:820 - 00:41:17:850] **Speaker 1:** Now We've not adjusted how we're evaluating in in time,
[00:41:17:929 - 00:41:20:889] **Speaker 1:** it's just choosing which uh time step to evaluate the
[00:41:20:889 - 00:41:22:689] **Speaker 1:** derivative of the spatial term map.
[00:41:23:120 - 00:41:25:850] **Speaker 1:** So this is still first order accurate in time.
[00:41:27:800 - 00:41:29:459] **Speaker 1:** Uh, and 2nd order accurate.
[00:41:30:530 - 00:41:31:330] **Speaker 1:** In space.
[00:41:32:270 - 00:41:34:719] **Speaker 1:** So as we refine the time step, we have 1st
[00:41:34:719 - 00:41:38:439] **Speaker 1:** order convergence rate, and as we refine the spatial grid
[00:41:38:439 - 00:41:41:080] **Speaker 1:** sizing, we've got that 2nd order convergence rate.
[00:41:44:979 - 00:41:46:159] **Speaker 1:** And this is implicit.
[00:41:52:870 - 00:41:56:229] **Speaker 1:** So the only difference between these equations is that the
[00:41:56:229 - 00:41:59:629] **Speaker 1:** right-hand side now involves this, this new time step.
[00:41:59:830 - 00:42:03:389] **Speaker 1:** So we can't only rearrange for for TIN + 1
[00:42:03:389 - 00:42:04:050] **Speaker 1:** on the left.
[00:42:05:770 - 00:42:08:120] **Speaker 1:** What we're gonna do instead is shift all of the
[00:42:08:120 - 00:42:10:929] **Speaker 1:** unknown temperature values on the left-hand side of the equal
[00:42:10:929 - 00:42:11:169] **Speaker 1:** sign.
[00:42:13:060 - 00:42:16:320] **Speaker 1:** And we're left with Minus lambda.
[00:42:18:610 - 00:42:18:929] **Speaker 1:** Tea.
[00:42:20:189 - 00:42:22:000] **Speaker 1:** I minus 1, N + 1.
[00:42:25:659 - 00:42:33:229] **Speaker 1:** So again, lambda was AlphaDT over X2.
[00:42:33:989 - 00:42:35:810] **Speaker 1:** So we've got TIN +1.
[00:42:41:270 - 00:42:45:949] **Speaker 1:** We've got 1 + 2 lambda TIN + 1.
[00:42:46:979 - 00:42:50:590] **Speaker 1:** And minus lambda, TI + 1.
[00:42:51:350 - 00:42:54:179] **Speaker 1:** N + 1 equals to TIN.
[00:42:54:870 - 00:42:57:310] **Speaker 1:** So it's a bit heavy-sided on the left-hand side, there's
[00:42:57:310 - 00:42:58:909] **Speaker 1:** only one term on the right that we actually know
[00:42:58:909 - 00:42:59:909] **Speaker 1:** what value it holds.
[00:43:03:229 - 00:43:06:469] **Speaker 1:** But we've got these 3 values that were unknown that
[00:43:06:469 - 00:43:07:330] **Speaker 1:** we have to calculate.
[00:43:13:280 - 00:43:15:870] **Speaker 1:** So this numerical method is a little bit more complex
[00:43:15:870 - 00:43:19:949] **Speaker 1:** because we have that simultaneous set of equations, um, so
[00:43:19:949 - 00:43:22:250] **Speaker 1:** it might appear to be more computationally expensive.
[00:43:23:189 - 00:43:27:000] **Speaker 1:** Trickier to solve, but because it's unconditionally stable, uh, it
[00:43:27:000 - 00:43:29:219] **Speaker 1:** can be much better for larger time steps.
[00:43:39:330 - 00:43:41:729] **Speaker 1:** So we'll continue with our same example, we're gonna use
[00:43:41:729 - 00:43:43:209] **Speaker 1:** uh this BTCS scheme.
[00:43:51:110 - 00:43:52:300] **Speaker 1:** So we've got our same grid.
[00:43:52:350 - 00:43:54:629] **Speaker 1:** We've got these, uh, direct grade boundary conditions on our
[00:43:54:629 - 00:43:55:229] **Speaker 1:** left and right.
[00:43:56:090 - 00:44:00:639] **Speaker 1:** And we're going to apply the equation that we've just
[00:44:00:899 - 00:44:01:469] **Speaker 1:** evaluated.
[00:44:01:620 - 00:44:03:139] **Speaker 1:** So equation 11.
[00:44:05:159 - 00:44:06:719] **Speaker 1:** For I equal to 1.
[00:44:10:209 - 00:44:14:169] **Speaker 1:** We have Minus lambda.
[00:44:14:610 - 00:44:16:050] **Speaker 1:** So lambda is still got the same value.
[00:44:16:129 - 00:44:20:550] **Speaker 1:** So we've got 0.020875.
[00:44:24:800 - 00:44:27:290] **Speaker 1:** Uh, the boundary condition on the left-hand side is 100,
[00:44:27:570 - 00:44:30:070] **Speaker 1:** so we can just substitute that directly.
[00:44:31:020 - 00:44:35:939] **Speaker 1:** And then we've got 1 + 2 lambda.
[00:44:38:239 - 00:44:40:280] **Speaker 1:** Which is 1.04.
[00:44:41:000 - 00:44:42:620] **Speaker 1:** 175.
[00:44:43:989 - 00:44:45:169] **Speaker 1:** Times our temperature.
[00:44:46:179 - 00:44:48:909] **Speaker 1:** At our point I equals 1 time level N +
[00:44:48:909 - 00:44:50:030] **Speaker 1:** 1, so D11.
[00:44:53:020 - 00:44:55:340] **Speaker 1:** Minus lambda, 0.0.
[00:44:56:100 - 00:44:58:260] **Speaker 1:** 20875.
[00:44:59:199 - 00:44:59:459] **Speaker 1:** Tea.
[00:45:00:500 - 00:45:01:379] **Speaker 1:** 21.
[00:45:06:040 - 00:45:08:560] **Speaker 1:** And it's equal to our initial temperature of that node,
[00:45:08:800 - 00:45:09:320] **Speaker 1:** T1 knot.
[00:45:16:479 - 00:45:19:479] **Speaker 1:** Now That first term is non, so we can chuck
[00:45:19:479 - 00:45:20:350] **Speaker 1:** it on the other side.
[00:45:24:719 - 00:45:34:419] **Speaker 1:** And we're left with 1.04175 T11 minus lambda 0.020875.
[00:45:35:780 - 00:45:37:149] **Speaker 1:** T 21.
[00:45:38:750 - 00:45:42:229] **Speaker 1:** Is equal to D10.
[00:45:42:830 - 00:45:46:790] **Speaker 1:** So our initial temperature at that node 1 is equal
[00:45:46:790 - 00:45:47:110] **Speaker 1:** to 0.
[00:45:47:219 - 00:45:48:209] **Speaker 1:** That was our initial condition.
[00:45:49:629 - 00:45:55:909] **Speaker 1:** And we've got that boundary condition contribution of 0.02.
[00:45:58:340 - 00:46:02:350] **Speaker 1:** 0875 100.
[00:46:10:270 - 00:46:13:139] **Speaker 1:** We can apply the same equation for those other 3
[00:46:13:139 - 00:46:13:790] **Speaker 1:** nodes.
[00:46:14:770 - 00:46:16:090] **Speaker 1:** So I equals 2.
[00:46:17:260 - 00:46:17:810] **Speaker 1:** 3.
[00:46:18:669 - 00:46:19:350] **Speaker 1:** And 4.
[00:46:22:110 - 00:46:23:550] **Speaker 1:** We don't have to write those out today.
[00:46:25:409 - 00:46:27:379] **Speaker 1:** And they all look very similar.
[00:46:27:500 - 00:46:28:360] **Speaker 1:** They're the same structure.
[00:46:29:020 - 00:46:31:090] **Speaker 1:** The only difference is they've got the boundary conditions being
[00:46:31:090 - 00:46:32:860] **Speaker 1:** imposed on that first and last node.
[00:46:34:709 - 00:46:36:580] **Speaker 1:** So what we've got is 4 equations.
[00:46:37:689 - 00:46:42:139] **Speaker 1:** We have 4 unknown values, temperatures 123, and 4 at
[00:46:42:139 - 00:46:43:540] **Speaker 1:** the next time level n + 1.
[00:46:44:560 - 00:46:46:360] **Speaker 1:** And what we can do is write this in matrix
[00:46:46:360 - 00:46:46:639] **Speaker 1:** form.
[00:46:48:060 - 00:46:48:530] **Speaker 1:** So.
[00:46:50:610 - 00:46:55:540] **Speaker 1:** We've got matrix of coefficients A, a temperature vector T,
[00:46:55:830 - 00:46:57:560] **Speaker 1:** and then some right-hand side vector.
[00:46:59:100 - 00:47:15:020] **Speaker 1:** Maybe we call it the Uh I mean these terms
[00:47:15:020 - 00:47:16:320] **Speaker 1:** are just minus lambda.
[00:47:19:389 - 00:47:20:639] **Speaker 1:** 1 + 2 lambda.
[00:47:23:169 - 00:47:23:830] **Speaker 1:** And minus Sada.
[00:47:25:780 - 00:47:27:310] **Speaker 1:** So you can kind of imagine that they could be
[00:47:27:310 - 00:47:29:800] **Speaker 1:** populated with a 4 loop for those interior nodes.
[00:47:30:270 - 00:47:31:350] **Speaker 1:** In this case, there's only 2.
[00:47:34:159 - 00:47:35:979] **Speaker 1:** And we can solve this equation.
[00:47:37:590 - 00:47:39:129] **Speaker 1:** Uh, directly.
[00:47:40:199 - 00:47:44:560] **Speaker 1:** So the, the solution for this at 0.1 seconds is
[00:47:44:560 - 00:47:47:080] **Speaker 1:** 2, 0.04, 0.02, and 1.
[00:47:47:879 - 00:47:51:760] **Speaker 1:** So it's slightly different to our explicit scheme.
[00:47:52:459 - 00:48:00:750] **Speaker 1:** Ah, but quite similar So If we have really large
[00:48:00:750 - 00:48:02:729] **Speaker 1:** time stamps of 5 seconds, it's going to be still
[00:48:02:729 - 00:48:03:310] **Speaker 1:** stable.
[00:48:03:469 - 00:48:04:969] **Speaker 1:** It might not be accurate.
[00:48:05:489 - 00:48:08:830] **Speaker 1:** The accuracy scales with a T, but it is unconditionally
[00:48:08:830 - 00:48:09:110] **Speaker 1:** stable.
[00:48:09:189 - 00:48:12:510] **Speaker 1:** So that's the key advantage for this implicit scheme.
[00:48:13:379 - 00:48:16:350] **Speaker 1:** Another thing to note is that the matrix of coefficients
[00:48:16:350 - 00:48:16:770] **Speaker 1:** A.
[00:48:18:280 - 00:48:19:979] **Speaker 1:** Remains constant over time.
[00:48:20:100 - 00:48:22:620] **Speaker 1:** We don't have to evaluate this matrix every single time
[00:48:22:620 - 00:48:24:739] **Speaker 1:** step, and if we don't have to do that, we
[00:48:24:739 - 00:48:25:780] **Speaker 1:** can find the inverse ones.
[00:48:25:860 - 00:48:27:389] **Speaker 1:** We don't have to do it inside our full loop
[00:48:27:389 - 00:48:29:560] **Speaker 1:** so that can be speeding it up a little bit.
[00:48:31:010 - 00:48:33:780] **Speaker 1:** So the right-hand side vector B is changing over time.
[00:48:34:169 - 00:48:37:929] **Speaker 1:** It's dependent on the previous temperature values within the domain.
[00:48:42:209 - 00:48:44:530] **Speaker 1:** And as I say, it's only first order accurate, but
[00:48:44:530 - 00:48:45:750] **Speaker 1:** it is unconditionally stable.
[00:48:50:649 - 00:48:52:250] **Speaker 1:** So, that's good fun.
[00:48:53:250 - 00:48:55:250] **Speaker 1:** So I think we've done enough today.
[00:48:55:479 - 00:48:59:419] **Speaker 1:** Um, so this implicit and explicit schemes are both first
[00:48:59:419 - 00:49:03:719] **Speaker 1:** order accuracy and time, and tomorrow we'll go through the
[00:49:03:719 - 00:49:05:840] **Speaker 1:** Crank Nicholson method, which is a sort of a hybrid
[00:49:05:840 - 00:49:07:979] **Speaker 1:** between the two and sort of a central difference scheme
[00:49:08:090 - 00:49:09:409] **Speaker 1:** and the 2nd order accurate.
[00:49:10:209 - 00:49:12:050] **Speaker 1:** So yeah, we'll see you in the labs this afternoon.
[00:49:12:290 - 00:49:14:570] **Speaker 1:** Uh, we've got lab 3, and you're going through that
[00:49:14:570 - 00:49:15:530] **Speaker 1:** simply supported beam.
[00:49:16:310 - 00:49:18:790] **Speaker 1:** And yeah, remember your quiz is due at the end
[00:49:18:790 - 00:49:19:489] **Speaker 1:** of the week as well.
[00:49:19:790 - 00:49:20:020] **Speaker 0:** Yeah.
[00:49:34:860 - 00:49:35:179] **Speaker 0:** Yeah.
[00:50:05:659 - 00:50:21:760] **Speaker 0:** I Thank you.
[00:50:27:090 - 00:50:41:760] **Speaker 0:** I Good yeah yeah.
[00:50:43:449 - 00:50:49:459] **Speaker 0:** No Um, I try to give it about 3.
[00:50:55:100 - 00:50:58:159] **Speaker 0:** Are you strong or yeah.
[00:50:59:439 - 00:50:59:860] **Speaker 0:** Yeah, yeah, yeah.
[00:51:04:830 - 00:51:05:870] **Speaker 0:** That'll, I usually go.
[00:51:19:709 - 00:54:56:649] **Speaker 0:** Yeah Good.

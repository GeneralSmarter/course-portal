# ENME302-26S2 Lecture 43 native Echo transcript

Date: October 8, 2026 10:00am-10:55am
Transcript type: native Echo automated transcript.

[00:00:59:310 - 00:01:06:290] **Speaker 0:** Yeah I Good morning.
[00:01:06:550 - 00:01:07:180] **Speaker 1:** We'll make us up.
[00:01:07:269 - 00:01:08:410] **Speaker 1:** Any questions?
[00:01:12:750 - 00:01:13:510] **Speaker 1:** I'm Christian.
[00:01:14:779 - 00:01:15:360] **Speaker 1:** That's good.
[00:01:15:779 - 00:01:19:620] **Speaker 1:** Um, anyone that was really paying attention yesterday, I added
[00:01:19:620 - 00:01:20:779] **Speaker 1:** an extra divergence to him.
[00:01:20:980 - 00:01:23:169] **Speaker 1:** So if anyone was wondering why this should be just
[00:01:23:169 - 00:01:26:620] **Speaker 1:** the first order derivative DT by DX, got a bit
[00:01:26:620 - 00:01:27:419] **Speaker 1:** carried away there.
[00:01:28:769 - 00:01:30:830] **Speaker 1:** Um, so, yeah, right.
[00:01:32:449 - 00:01:34:730] **Speaker 1:** Essentially this is going to set the the gradient to
[00:01:34:730 - 00:01:39:819] **Speaker 1:** be approximately, Um, That it doesn't really matter what it
[00:01:39:819 - 00:01:40:290] **Speaker 1:** is.
[00:01:40:830 - 00:01:43:220] **Speaker 1:** So this is setting the dirt clay condition and the
[00:01:43:220 - 00:01:45:629] **Speaker 1:** gradient DT by DX is is reasonably.
[00:01:46:669 - 00:01:48:830] **Speaker 1:** Um, unconstrained.
[00:01:50:959 - 00:01:53:790] **Speaker 1:** Yeah Part one wearing on results.
[00:01:56:430 - 00:01:56:449] **Speaker 0:** Oh.
[00:01:57:739 - 00:02:01:790] **Speaker 0:** He Are you implying?
[00:02:04:360 - 00:02:07:220] **Speaker 0:** Are you implying that we show you another plot?
[00:02:08:529 - 00:02:14:820] **Speaker 0:** so Mm.
[00:02:17:339 - 00:02:19:240] **Speaker 1:** It'd be easier if they were on the same plot,
[00:02:19:779 - 00:02:20:610] **Speaker 1:** or the same figure.
[00:02:22:070 - 00:02:22:270] **Speaker 1:** Yeah.
[00:02:28:169 - 00:02:30:330] **Speaker 1:** So you could create one figure with both sets of
[00:02:30:330 - 00:02:30:750] **Speaker 1:** foxes.
[00:02:30:889 - 00:02:33:149] **Speaker 1:** That, that would be the easiest choice.
[00:02:39:619 - 00:02:40:779] **Speaker 1:** Other queries for?
[00:02:42:860 - 00:02:43:490] **Speaker 1:** You're silent.
[00:02:43:899 - 00:02:44:100] **Speaker 1:** Nope.
[00:02:48:460 - 00:02:50:880] **Speaker 1:** Um, there was a question about tea and.
[00:02:54:470 - 00:02:56:990] **Speaker 1:** So some of you, well, I'm sure lots of you
[00:02:56:990 - 00:02:59:270] **Speaker 1:** are thinking about the assignment, but um some of you
[00:02:59:270 - 00:02:59:990] **Speaker 1:** are thinking about.
[00:03:00:759 - 00:03:03:449] **Speaker 1:** In terms of what is safe to eat.
[00:03:04:330 - 00:03:07:910] **Speaker 1:** After you flip it, if a region has gone above
[00:03:07:910 - 00:03:10:729] **Speaker 1:** 80 and then gone below 80, it might be safe.
[00:03:11:229 - 00:03:14:410] **Speaker 1:** Um, that wasn't my intention to keep track of everywhere
[00:03:14:410 - 00:03:16:250] **Speaker 1:** throughout the patty to be above 80.
[00:03:17:229 - 00:03:20:220] **Speaker 1:** And then allowed to dip behind or below 80.
[00:03:20:470 - 00:03:22:929] **Speaker 1:** So the simplest way is just look at the team
[00:03:22:929 - 00:03:26:619] **Speaker 1:** men over time and check that that is beyond 80.
[00:03:26:710 - 00:03:28:750] **Speaker 1:** So you don't need to keep track of which part
[00:03:28:750 - 00:03:31:070] **Speaker 1:** of the patty is above 80 and not and tag
[00:03:31:070 - 00:03:31:529] **Speaker 1:** it.
[00:03:32:139 - 00:03:33:529] **Speaker 1:** Uh, that might be a little bit more involved.
[00:03:33:910 - 00:03:36:149] **Speaker 1:** You probably can do it in console, but it's beyond
[00:03:36:149 - 00:03:37:029] **Speaker 1:** what I was expecting.
[00:03:37:839 - 00:03:40:259] **Speaker 1:** Um, you might get a different result, so if you
[00:03:40:259 - 00:03:43:080] **Speaker 1:** do, maybe just email me or let me know, so
[00:03:43:080 - 00:03:44:800] **Speaker 1:** that I can just check that you don't get penalised
[00:03:44:800 - 00:03:48:529] **Speaker 1:** for it, but that, The approach that I intended for
[00:03:48:529 - 00:03:50:399] **Speaker 1:** you to look at is just to check the minimum
[00:03:50:399 - 00:03:52:529] **Speaker 1:** temperature within the body over time and check that it's
[00:03:52:529 - 00:03:53:220] **Speaker 1:** above 80.
[00:03:53:529 - 00:03:55:169] **Speaker 1:** So the easy case.
[00:03:56:059 - 00:03:59:100] **Speaker 1:** Um, in context, maybe your friend is a little bit
[00:03:59:100 - 00:04:03:649] **Speaker 1:** paranoid that the bacteria might jump across to an uncooked
[00:04:03:649 - 00:04:06:899] **Speaker 1:** region, so just make sure that it's fully cooked and
[00:04:06:899 - 00:04:08:960] **Speaker 1:** above 80 °C.
[00:04:14:000 - 00:04:18:320] **Speaker 1:** And yeah, before I forget, we've got the labs this
[00:04:18:320 - 00:04:20:459] **Speaker 1:** afternoon, it's just pretty much help sessions for the assignments.
[00:04:21:000 - 00:04:23:950] **Speaker 1:** I've got meetings at 1 and 2, there's always meetings,
[00:04:23:959 - 00:04:25:959] **Speaker 1:** um, but they might only be half an hour so
[00:04:25:959 - 00:04:27:890] **Speaker 1:** I should be able to be there for most of
[00:04:27:890 - 00:04:30:359] **Speaker 1:** the afternoon, but all the other TAs will be there
[00:04:30:359 - 00:04:31:559] **Speaker 1:** as well to help, yep.
[00:04:32:899 - 00:04:35:559] **Speaker 0:** Flipping question if that team.
[00:04:37:899 - 00:04:40:779] **Speaker 0:** And then shots below the wave kind of peaks.
[00:04:44:720 - 00:04:48:019] **Speaker 1:** After flipping Yeah, I mean, it's going to cool down
[00:04:48:019 - 00:04:50:250] **Speaker 1:** once you turn off the pan.
[00:04:53:079 - 00:04:53:179] **Speaker 0:** We had like and then that.
[00:04:56:209 - 00:04:59:480] **Speaker 1:** But wouldn't you say it's cooked once it's reached the,
[00:04:59:690 - 00:05:00:470] **Speaker 1:** yeah, yeah.
[00:05:00:970 - 00:05:05:750] **Speaker 1:** So you can use events in um, In console to
[00:05:05:760 - 00:05:08:339] **Speaker 1:** to stop it automatically and then you don't have that
[00:05:08:339 - 00:05:12:230] **Speaker 1:** at the end, um, Uh, yeah.
[00:05:13:040 - 00:05:13:559] **Speaker 1:** That's fine.
[00:05:14:890 - 00:05:16:570] **Speaker 1:** And maybe that was what I was getting asked the
[00:05:16:570 - 00:05:17:410] **Speaker 1:** other day, I'm not sure.
[00:05:17:609 - 00:05:21:250] **Speaker 1:** I interpreted it as if a piece of the, the
[00:05:21:250 - 00:05:24:230] **Speaker 1:** patty had reached the 80 and then cooled, and then
[00:05:24:329 - 00:05:26:429] **Speaker 1:** the rest of the patty is cooking above 80.
[00:05:26:649 - 00:05:27:130] **Speaker 1:** Um.
[00:05:28:000 - 00:05:30:929] **Speaker 1:** But in summary, keep it simple, uh, demon.
[00:05:35:100 - 00:05:35:510] **Speaker 1:** Sweet.
[00:05:44:359 - 00:05:46:970] **Speaker 1:** Alright, we'll get stuck into chapter 7 again.
[00:05:47:209 - 00:05:50:410] **Speaker 1:** Um, so we have to do something towards practising for
[00:05:50:410 - 00:05:50:850] **Speaker 1:** the exam.
[00:05:51:750 - 00:05:57:220] **Speaker 1:** So We've got our wave equation that we derived yesterday.
[00:05:57:640 - 00:05:59:850] **Speaker 1:** We solved it with separation of variables or I pointed
[00:05:59:850 - 00:06:02:160] **Speaker 1:** to some solution, and you can work through it if
[00:06:02:160 - 00:06:03:799] **Speaker 1:** you want, you might want to.
[00:06:04:570 - 00:06:07:790] **Speaker 1:** And we're now going to go through the finite differenceferencing
[00:06:08:179 - 00:06:09:739] **Speaker 1:** approach to solve this wave equation.
[00:06:10:570 - 00:06:13:040] **Speaker 1:** We've got 2 boundary conditions and 2 initial conditions.
[00:06:13:089 - 00:06:14:649] **Speaker 1:** We've got that velocity term which is gonna be a
[00:06:14:649 - 00:06:18:440] **Speaker 1:** little bit trickier to, to, uh, Solve for that first
[00:06:18:440 - 00:06:19:010] **Speaker 1:** time step.
[00:06:19:459 - 00:06:20:559] **Speaker 1:** So we'll go through step by step.
[00:06:23:929 - 00:06:29:170] **Speaker 1:** And The first stage is maybe just to visualise what
[00:06:29:170 - 00:06:31:470] **Speaker 1:** we're solving in space-time.
[00:06:40:809 - 00:06:42:410] **Speaker 1:** So for example, on the X axis, we might have
[00:06:42:410 - 00:06:44:750] **Speaker 1:** the spatial coordinate on the vertical axis time.
[00:06:48:429 - 00:06:52:170] **Speaker 1:** And We're going to discretize across the length L.
[00:07:04:089 - 00:07:07:730] **Speaker 1:** And we have an initial condition at 0, and we
[00:07:07:730 - 00:07:09:769] **Speaker 1:** go up to some final value.
[00:07:11:779 - 00:07:12:119] **Speaker 1:** Tea.
[00:07:13:190 - 00:07:24:589] **Speaker 1:** If So finite conferencing, we're approximating the derivatives in our
[00:07:24:589 - 00:07:27:950] **Speaker 1:** governing equation at each nodal point within our computational domain.
[00:07:54:359 - 00:07:57:880] **Speaker 1:** And in terms of looping through, we're doing a step
[00:07:57:880 - 00:07:58:720] **Speaker 1:** by step case.
[00:07:58:980 - 00:08:01:760] **Speaker 1:** So we start at T0 with our initial condition, and
[00:08:01:760 - 00:08:03:760] **Speaker 1:** then we take the 1st step, 2nd, 3rd, and 4th
[00:08:03:760 - 00:08:04:200] **Speaker 1:** steps.
[00:08:05:200 - 00:08:08:309] **Speaker 1:** The first step, I guess the first stage of, uh,
[00:08:08:320 - 00:08:12:130] **Speaker 1:** approximating our governing equation, which is continuous with our finite
[00:08:12:130 - 00:08:17:309] **Speaker 1:** differenceerencing, which is discrete, is to discretize our time derivative,
[00:08:17:809 - 00:08:19:829] **Speaker 1:** and this is a 2nd order in time.
[00:08:21:890 - 00:08:24:329] **Speaker 1:** So we're going to discretize with a central difference scheme.
[00:08:25:950 - 00:08:29:589] **Speaker 1:** We've got you, I, In +1.
[00:08:30:380 - 00:08:31:790] **Speaker 1:** It's a derivative in time.
[00:08:32:380 - 00:08:35:140] **Speaker 1:** So we're discretizing across the the time axis.
[00:08:35:400 - 00:08:36:440] **Speaker 1:** So N + 1.
[00:08:37:619 - 00:08:41:700] **Speaker 1:** -2 UIN plus UIN minus 1.
[00:08:42:968 - 00:08:46:258] **Speaker 1:** And this is divided by delta D2.
[00:08:54:549 - 00:08:57:299] **Speaker 1:** And the right hand side we've got C2 multiplied by
[00:08:57:299 - 00:08:58:349] **Speaker 1:** that spatial derivative term.
[00:09:01:619 - 00:09:03:229] **Speaker 1:** And that's familiar to us.
[00:09:03:390 - 00:09:06:349] **Speaker 1:** Instead of discretizing in time, we're now discretizing in space,
[00:09:06:570 - 00:09:07:619] **Speaker 1:** the spatial coordinates.
[00:09:07:830 - 00:09:09:489] **Speaker 1:** So we've got Ui plus 1.
[00:09:11:239 - 00:09:16:280] **Speaker 1:** N minus 2 UIN plus UI minus 1 N.
[00:09:17:210 - 00:09:18:530] **Speaker 1:** Divided by delta X2.
[00:09:26:409 - 00:09:29:669] **Speaker 1:** So instead of only including 2 time sets, we have
[00:09:29:669 - 00:09:30:450] **Speaker 1:** 3.
[00:09:31:150 - 00:09:32:229] **Speaker 1:** That we're straddling across.
[00:09:32:549 - 00:09:35:469] **Speaker 1:** So we've got levels N, N minus 1 and N
[00:09:35:469 - 00:09:36:200] **Speaker 1:** + 1.
[00:09:36:549 - 00:09:38:669] **Speaker 1:** So if we look at an arbitrary point within our
[00:09:38:669 - 00:09:45:760] **Speaker 1:** computational domain, I, And We've got I plus 1.
[00:09:48:530 - 00:09:49:530] **Speaker 1:** I minus 1.
[00:09:51:539 - 00:09:53:289] **Speaker 1:** And I.
[00:09:54:059 - 00:09:55:179] **Speaker 1:** In 1.
[00:09:56:000 - 00:09:57:049] **Speaker 1:** Uh, in Oslo.
[00:10:19:650 - 00:10:22:880] **Speaker 1:** So how many unknowns do we have in this equation?
[00:10:23:119 - 00:10:23:809] **Speaker 1:** 12.
[00:10:27:210 - 00:10:28:359] **Speaker 1:** That we need to solve for.
[00:10:47:270 - 00:10:48:469] **Speaker 1:** Just one, that's right.
[00:10:51:190 - 00:10:54:510] **Speaker 1:** So we've got in time in and time level, well,
[00:10:54:630 - 00:10:57:250] **Speaker 1:** time level N is the current time set that we
[00:10:57:250 - 00:10:57:630] **Speaker 1:** will have.
[00:10:57:840 - 00:11:00:479] **Speaker 1:** time level in minus 1 is the previous one.
[00:11:01:289 - 00:11:03:780] **Speaker 1:** The only unknown here is UIN +1.
[00:11:04:440 - 00:11:07:030] **Speaker 1:** So we're gonna rearrange for this unknown term.
[00:11:10:669 - 00:11:12:210] **Speaker 1:** So you are N + 1.
[00:11:13:489 - 00:11:18:710] **Speaker 1:** Is equal to Obviously a reasonably long expression, so we've
[00:11:18:710 - 00:11:19:309] **Speaker 1:** got 2.
[00:11:20:309 - 00:11:23:229] **Speaker 1:** 1 minus lambda 2.
[00:11:27:159 - 00:11:28:640] **Speaker 1:** U I N.
[00:11:33:809 - 00:11:35:349] **Speaker 1:** Plus lambda squared.
[00:11:36:640 - 00:11:38:729] **Speaker 1:** UI plus 1 N.
[00:11:39:809 - 00:11:42:340] **Speaker 1:** Plus UI minus 1 in.
[00:11:43:869 - 00:11:47:119] **Speaker 1:** Minus UIN minus 1.
[00:11:48:960 - 00:11:49:760] **Speaker 1:** So here.
[00:11:53:619 - 00:11:55:210] **Speaker 1:** Lambda is equal to CT.
[00:11:56:950 - 00:11:59:030] **Speaker 1:** Over data X.
[00:12:00:010 - 00:12:01:440] **Speaker 1:** And as the Quran.
[00:12:04:200 - 00:12:27:010] **Speaker 1:** Number Cool.
[00:12:28:760 - 00:12:33:719] **Speaker 1:** So, for the explicit explicit scheme, it's a two-step explicit
[00:12:33:719 - 00:12:34:080] **Speaker 1:** scheme.
[00:12:35:369 - 00:12:38:010] **Speaker 1:** Because our, our new time set N + 1 is
[00:12:38:010 - 00:12:40:880] **Speaker 1:** dependent on the previous two time levels at N and
[00:12:40:880 - 00:12:41:650] **Speaker 1:** N minus 1.
[00:12:44:190 - 00:12:47:049] **Speaker 1:** So we can't apply this equation 13 at times 0
[00:12:47:429 - 00:12:50:780] **Speaker 1:** because we'd have this, this other ghost node again, uh,
[00:12:50:830 - 00:12:53:950] **Speaker 1:** this ghost point below 0, so negative time.
[00:12:54:859 - 00:12:57:409] **Speaker 1:** So we're going to introduce another ghost point at time
[00:12:57:409 - 00:12:58:099] **Speaker 1:** minus 1.
[00:12:59:380 - 00:13:01:239] **Speaker 1:** Equal to minus 1st.
[00:13:03:780 - 00:13:07:539] **Speaker 1:** So we discretize our initial condition, we can see that
[00:13:07:539 - 00:13:09:380] **Speaker 1:** we've got this first order derivative in time D by
[00:13:09:380 - 00:13:09:619] **Speaker 1:** DT.
[00:13:14:030 - 00:13:15:190] **Speaker 1:** At times 0.
[00:13:18:619 - 00:13:21:750] **Speaker 1:** And we apply the central difference.
[00:13:22:609 - 00:13:24:219] **Speaker 1:** Keep it 2nd order accurate accurate.
[00:13:25:080 - 00:13:27:909] **Speaker 1:** And it's given by you I.
[00:13:29:049 - 00:13:29:409] **Speaker 1:** One.
[00:13:30:299 - 00:13:34:030] **Speaker 1:** Minus UI minus 1 divided by 2 out of T.
[00:13:54:190 - 00:13:58:510] **Speaker 1:** And this is going to equal our initial condition for
[00:13:58:510 - 00:14:00:599] **Speaker 1:** the velocity, so G of X.
[00:14:02:440 - 00:14:05:659] **Speaker 1:** So we're evaluating G at point XI.
[00:14:07:030 - 00:14:09:869] **Speaker 1:** Or labelling it just G I.
[00:14:10:989 - 00:14:12:729] **Speaker 1:** So we're gonna rearrange.
[00:14:28:489 - 00:14:31:960] **Speaker 1:** We're gonna rearrange for the ghost point at UI minus
[00:14:31:960 - 00:14:32:289] **Speaker 1:** 1.
[00:14:33:419 - 00:14:39:219] **Speaker 1:** Equal to UI1 minus 2 TGI.
[00:14:47:239 - 00:14:49:559] **Speaker 1:** And we're going to substitute back into our equation 13.
[00:14:50:679 - 00:14:52:960] **Speaker 1:** And eliminate that ghost point.
[00:14:54:000 - 00:14:57:409] **Speaker 1:** And we have our expression for UI at the first
[00:14:57:409 - 00:14:58:840] **Speaker 1:** time step, level one.
[00:15:16:549 - 00:15:19:469] **Speaker 1:** We'll see if the laptop connects on the 1st attempt,
[00:15:19:770 - 00:15:22:070] **Speaker 1:** or the 3rd or the 5th today.
[00:15:27:250 - 00:15:29:309] **Speaker 1:** It's connected, but it's very small.
[00:15:42:179 - 00:15:43:119] **Speaker 1:** Better, right.
[00:15:43:859 - 00:15:47:500] **Speaker 1:** So chapter 7, I've chucked this up on the course
[00:15:47:500 - 00:15:48:179] **Speaker 1:** material folder.
[00:15:48:500 - 00:15:51:489] **Speaker 1:** Uh, we've got our parameters, there's some length of the
[00:15:51:489 - 00:15:53:280] **Speaker 1:** domain, we've got some constant coefficiency.
[00:15:53:619 - 00:15:56:219] **Speaker 1:** We've got a lambda value that's our current number, number
[00:15:56:219 - 00:15:59:619] **Speaker 1:** of nodes and time sets, discrets within the grid in
[00:15:59:619 - 00:16:03:340] **Speaker 1:** space and time, and we've got an initial conditions.
[00:16:04:020 - 00:16:06:419] **Speaker 1:** And boundary conditions being applied.
[00:16:07:809 - 00:16:09:390] **Speaker 1:** And our time's different.
[00:16:10:280 - 00:16:14:130] **Speaker 1:** I'm using J as the time index here.
[00:16:15:539 - 00:16:18:020] **Speaker 1:** And instead of doing a 4 loop for X, I've
[00:16:18:020 - 00:16:23:979] **Speaker 1:** just used array slicing, so that's going from the, 2nd
[00:16:23:979 - 00:16:27:979] **Speaker 1:** entry because Python is off by 1, 2nd entry up
[00:16:27:979 - 00:16:32:979] **Speaker 1:** to the last entry but not including the last entry
[00:16:32:979 - 00:16:35:940] **Speaker 1:** minus 1, which I still can't get my head around.
[00:16:37:630 - 00:16:42:919] **Speaker 1:** And we're evaluating this from our equation 13.
[00:16:46:849 - 00:16:48:849] **Speaker 1:** And that first time step doesn't need to be in
[00:16:48:849 - 00:16:51:409] **Speaker 1:** a full loop because it's just done once, and that's
[00:16:51:409 - 00:16:51:869] **Speaker 1:** this fall.
[00:16:53:349 - 00:16:54:820] **Speaker 1:** So we'll go ahead and plot this.
[00:16:58:729 - 00:17:00:780] **Speaker 1:** And we get a.
[00:17:01:679 - 00:17:03:890] **Speaker 1:** Series of lines or displacements of our string.
[00:17:04:050 - 00:17:07:810] **Speaker 1:** We started at that initial triangular shape from rest and
[00:17:07:810 - 00:17:10:729] **Speaker 1:** then released and it's gone down to the midpoint.
[00:17:11:468 - 00:17:14:818] **Speaker 1:** If we left it to go longer, so maybe 200.
[00:17:16:030 - 00:17:16:910] **Speaker 1:** Time steps.
[00:17:18:270 - 00:17:19:670] **Speaker 1:** We would expect it to do.
[00:17:22:359 - 00:17:24:410] **Speaker 1:** Or or reach the, the base, the bottom.
[00:17:26:020 - 00:17:28:319] **Speaker 1:** And further still, it would just keep going.
[00:17:29:250 - 00:17:30:430] **Speaker 1:** And return to the top.
[00:17:38:479 - 00:17:39:199] **Speaker 1:** All right.
[00:17:39:989 - 00:17:43:000] **Speaker 1:** So there's some inherent instability that we can sort of
[00:17:43:000 - 00:17:43:609] **Speaker 1:** see here.
[00:17:43:800 - 00:17:45:849] **Speaker 1:** It's not perfectly triangular.
[00:17:46:109 - 00:17:49:040] **Speaker 1:** There's some ripples that are starting to form, and it's
[00:17:49:040 - 00:17:51:880] **Speaker 1:** a nice feature or bug of the wave equation.
[00:17:52:810 - 00:17:54:900] **Speaker 1:** So it can be a little bit challenging to resolve
[00:17:54:900 - 00:17:55:599] **Speaker 1:** super accurately.
[00:17:56:900 - 00:17:59:160] **Speaker 1:** Just as we looked at for.
[00:18:02:520 - 00:18:06:890] **Speaker 1:** Um What do we look at the heat equation, we
[00:18:06:890 - 00:18:09:729] **Speaker 1:** looked at the condition on lambda.
[00:18:09:900 - 00:18:11:589] **Speaker 1:** Like if it was too large, it would be unstable
[00:18:11:589 - 00:18:13:530] **Speaker 1:** for our explicit scheme, and it's the same here.
[00:18:13:569 - 00:18:15:089] **Speaker 1:** If we have a lambda value of say 2.
[00:18:18:180 - 00:18:21:280] **Speaker 1:** We, we have issues, lots of issues.
[00:18:22:859 - 00:18:24:119] **Speaker 1:** That's too many issues there.
[00:18:30:479 - 00:18:33:310] **Speaker 1:** Yeah It's a very large number that you can't, you
[00:18:33:310 - 00:18:35:130] **Speaker 1:** might not be able to read that, but that's 10
[00:18:35:130 - 00:18:36:270] **Speaker 1:** to 110, so.
[00:18:38:130 - 00:18:40:729] **Speaker 1:** Our, our violin strength isn't going that high.
[00:18:41:550 - 00:18:45:260] **Speaker 1:** So that's demonstrating instability of our explicit scheme for the
[00:18:45:260 - 00:18:46:030] **Speaker 1:** wave equation.
[00:18:47:010 - 00:18:50:250] **Speaker 1:** So it's dependent on that cravat number and if you
[00:18:50:250 - 00:18:53:489] **Speaker 1:** look at some numerical stability analysis, you can show that
[00:18:53:489 - 00:18:55:229] **Speaker 1:** lambda needs to be less than one.
[00:18:56:339 - 00:18:58:520] **Speaker 1:** So it gives a constraint on the the time step
[00:18:58:520 - 00:18:59:839] **Speaker 1:** required for certain meshes.
[00:19:00:219 - 00:19:02:420] **Speaker 1:** So if you do a mesh resolution study, you also
[00:19:02:420 - 00:19:04:359] **Speaker 1:** need to tighten the time stepping data.
[00:19:05:599 - 00:19:06:959] **Speaker 1:** In console, it does this for you.
[00:19:07:040 - 00:19:08:800] **Speaker 1:** It does that at the time setting and you set
[00:19:08:800 - 00:19:11:020] **Speaker 1:** that relative tolerance, which is nice.
[00:19:11:199 - 00:19:12:880] **Speaker 1:** Uh, but if you're coding in Python, you'll need to
[00:19:12:880 - 00:19:14:800] **Speaker 1:** keep track of that, that current number.
[00:19:19:979 - 00:19:20:500] **Speaker 1:** All right.
[00:19:21:270 - 00:19:23:140] **Speaker 1:** Any questions on the wave equation.
[00:19:32:900 - 00:19:33:170] **Speaker 1:** No.
[00:19:34:359 - 00:19:35:060] **Speaker 1:** All right.
[00:19:35:640 - 00:19:37:560] **Speaker 1:** So I'll get you to do something now, so.
[00:19:38:689 - 00:19:41:209] **Speaker 1:** It's always fun, um, so I've got.
[00:19:42:380 - 00:19:47:500] **Speaker 1:** Um, 2024's exam, and I asked them to look at
[00:19:47:500 - 00:19:51:319] **Speaker 1:** the wave equation with a damped vibration.
[00:19:51:939 - 00:19:54:020] **Speaker 1:** So now that we've covered this, you can, you can
[00:19:54:020 - 00:19:54:619] **Speaker 1:** start working through it.
[00:19:54:699 - 00:19:57:150] **Speaker 1:** I'll talk more about the exam tomorrow.
[00:19:57:380 - 00:19:59:260] **Speaker 1:** I'll just go through stuff.
[00:19:59:910 - 00:20:02:709] **Speaker 1:** But for now, we'll just go through this as a
[00:20:02:709 - 00:20:03:250] **Speaker 1:** class.
[00:20:05:430 - 00:20:12:459] **Speaker 1:** And Maybe I could put the formula sheet on this
[00:20:12:459 - 00:20:13:079] **Speaker 1:** other screen.
[00:20:15:839 - 00:21:05:000] **Speaker 1:** For you So, That's a bit small.
[00:21:16:239 - 00:21:17:959] **Speaker 1:** You'll just have to squint, I think.
[00:21:21:560 - 00:21:22:300] **Speaker 1:** Can you read that?
[00:21:23:290 - 00:21:23:760] **Speaker 1:** Sort of.
[00:21:27:810 - 00:21:29:969] **Speaker 1:** So down the bottom we've got that two-step that we
[00:21:29:969 - 00:21:30:790] **Speaker 1:** just covered.
[00:21:31:489 - 00:21:34:290] **Speaker 1:** I've included the central difference uh pattern up here.
[00:21:35:520 - 00:21:38:719] **Speaker 1:** And then we've got some general definitions to get you
[00:21:38:719 - 00:21:39:040] **Speaker 1:** started.
[00:22:35:560 - 00:22:40:489] **Speaker 1:** So that first part A is this equation linear?
[00:22:40:949 - 00:22:43:390] **Speaker 1:** Does anyone remember what the definition of a linear PDE
[00:22:43:390 - 00:22:43:890] **Speaker 1:** is?
[00:22:49:420 - 00:22:51:420] **Speaker 1:** What's our dependent variable in this equation?
[00:22:55:540 - 00:22:59:640] **Speaker 1:** Yeah, yep, we're looking at the um deflection of a
[00:22:59:859 - 00:23:00:859] **Speaker 1:** vibration of a string.
[00:23:01:859 - 00:23:06:180] **Speaker 1:** And it's dependent on space, spatial coordinate X and time
[00:23:06:180 - 00:23:06:380] **Speaker 1:** T.
[00:23:07:699 - 00:23:09:859] **Speaker 1:** And we've got a 2nd order in time, 2nd order
[00:23:09:859 - 00:23:12:439] **Speaker 1:** in space, and also a 1st order in time.
[00:23:13:699 - 00:23:16:819] **Speaker 1:** Do we have any of these expressions or these terms
[00:23:16:819 - 00:23:17:780] **Speaker 1:** in this equation?
[00:23:18:819 - 00:23:20:329] **Speaker 1:** With a nonlinear.
[00:23:21:760 - 00:23:24:640] **Speaker 1:** The fiction, you No.
[00:23:25:479 - 00:23:27:439] **Speaker 1:** So we don't have U2d, we don't have U times
[00:23:27:439 - 00:23:28:900] **Speaker 1:** D by DT or anything like that.
[00:23:29:430 - 00:23:30:479] **Speaker 1:** So this is linear.
[00:23:34:270 - 00:23:37:469] **Speaker 1:** So I guess in general, I would like you to
[00:23:37:469 - 00:23:41:209] **Speaker 1:** write something about why it's linear or or some, some
[00:23:41:209 - 00:23:44:150] **Speaker 1:** working, uh, otherwise it's like a 50/50 chance which I
[00:23:44:150 - 00:23:46:729] **Speaker 1:** know it's a bit, a bit rough, well, bit easy.
[00:23:47:310 - 00:23:51:310] **Speaker 1:** So linear um and you or or some.
[00:23:52:130 - 00:23:54:369] **Speaker 1:** Some description would be, would be good.
[00:23:55:680 - 00:23:57:030] **Speaker 1:** Just to make sure you get full credit.
[00:23:58:680 - 00:23:59:819] **Speaker 1:** Is it homogeneous?
[00:24:04:790 - 00:24:06:449] **Speaker 1:** What makes a homogeneous equation?
[00:24:12:040 - 00:24:12:920] **Speaker 1:** If it equals 0.
[00:24:13:079 - 00:24:15:160] **Speaker 1:** Well, any equation can equal 0 if we put everything
[00:24:15:160 - 00:24:15:900] **Speaker 1:** on one side.
[00:24:16:400 - 00:24:16:760] **Speaker 1:** So.
[00:24:18:630 - 00:24:19:930] **Speaker 1:** What's our definition?
[00:24:20:439 - 00:24:21:969] **Speaker 1:** Oh yeah, I gave the, yep, it's on the cheat,
[00:24:22:060 - 00:24:22:949] **Speaker 1:** uh, the formula sheet.
[00:24:23:150 - 00:24:24:469] **Speaker 1:** So you don't have a cheat sheet, you only have
[00:24:24:469 - 00:24:26:550] **Speaker 1:** this formula sheet in the exam.
[00:24:30:079 - 00:24:32:760] **Speaker 1:** Yeah, so essentially all the terms that aren't a function
[00:24:32:760 - 00:24:33:280] **Speaker 1:** of you.
[00:24:33:979 - 00:24:36:140] **Speaker 1:** In our equation is treated as g.
[00:24:37:819 - 00:24:39:859] **Speaker 1:** G of X and Y and.
[00:24:41:229 - 00:24:43:739] **Speaker 1:** It can still be a function of our independent variables
[00:24:43:739 - 00:24:44:280] **Speaker 1:** X and T.
[00:24:44:910 - 00:24:46:849] **Speaker 1:** And we can group them all together.
[00:24:47:849 - 00:24:49:489] **Speaker 1:** And put them on the other side if you want.
[00:24:50:079 - 00:24:53:380] **Speaker 1:** But essentially all of these terms depend on our value.
[00:24:54:300 - 00:24:57:140] **Speaker 1:** So this doesn't have any terms for G.
[00:24:57:849 - 00:24:59:920] **Speaker 1:** So it's going to be homogeneous.
[00:25:07:239 - 00:25:09:310] **Speaker 1:** So you could make a statement like all terms.
[00:25:11:060 - 00:25:12:150] **Speaker 1:** a function.
[00:25:13:500 - 00:25:14:739] **Speaker 1:** Of you.
[00:25:18:239 - 00:25:18:949] **Speaker 1:** So that's 1 mark.
[00:25:19:030 - 00:25:21:569] **Speaker 1:** This exam was out of 60 marks.
[00:25:22:310 - 00:25:26:270] **Speaker 1:** So that's 3 hours, so roughly 3 minutes a mark.
[00:25:28:040 - 00:25:31:359] **Speaker 1:** So the exams don't, hopefully won't run out of time
[00:25:31:359 - 00:25:32:760] **Speaker 1:** generally, um.
[00:25:33:650 - 00:25:35:880] **Speaker 1:** So just spend your time on each, each question.
[00:25:36:719 - 00:25:38:800] **Speaker 1:** So the next step or the next part of this
[00:25:38:800 - 00:25:39:099] **Speaker 1:** question.
[00:25:40:119 - 00:25:44:000] **Speaker 1:** is asking you to draw the computational domain.
[00:25:44:479 - 00:25:48:219] **Speaker 1:** So I, I did this as an example just before.
[00:25:48:920 - 00:25:59:800] **Speaker 1:** I've already lost the piece of paper, but, So this
[00:25:59:800 - 00:26:03:699] **Speaker 1:** was the generic computational domain over time and space.
[00:26:04:510 - 00:26:07:150] **Speaker 1:** Here we're just asking to look at the computational domain
[00:26:07:150 - 00:26:09:469] **Speaker 1:** for uniform node spacings of all over 2.
[00:26:10:089 - 00:26:12:250] **Speaker 1:** And then label each node starting from i equal to
[00:26:12:250 - 00:26:12:530] **Speaker 1:** 1.
[00:26:15:739 - 00:26:18:140] **Speaker 1:** Circling each node with an unknown degree of freedom.
[00:26:24:739 - 00:26:25:130] **Speaker 1:** So.
[00:26:26:140 - 00:26:26:339] **Speaker 1:** Yeah.
[00:26:29:000 - 00:26:31:040] **Speaker 1:** I'll give you a moment to to think about that.
[00:27:14:660 - 00:27:19:180] **Speaker 1:** So it's a one dimensional domain and X, and we're
[00:27:19:180 - 00:27:21:339] **Speaker 1:** just gonna draw a computation domain in X.
[00:27:22:439 - 00:27:27:660] **Speaker 1:** And it ranges from 0 to L.
[00:27:28:560 - 00:27:30:050] **Speaker 1:** Hopefully we're able to find that somewhere.
[00:27:30:479 - 00:27:31:390] **Speaker 1:** So here we've got.
[00:27:34:020 - 00:27:37:489] **Speaker 1:** L in the boundary condition on the right hand side,
[00:27:37:540 - 00:27:40:359] **Speaker 1:** we've got a Derek Neumann boundary condition on the right
[00:27:40:670 - 00:27:41:800] **Speaker 1:** at X equal to L.
[00:27:43:790 - 00:27:45:709] **Speaker 1:** And we've got node spacings of L over 2.
[00:27:46:510 - 00:27:49:750] **Speaker 1:** Which means that our lengths are all over 2.
[00:27:50:630 - 00:27:51:140] **Speaker 1:** Oops.
[00:27:53:060 - 00:27:54:199] **Speaker 1:** No, we weren't fast enough.
[00:28:01:680 - 00:28:06:260] **Speaker 1:** And We're asked to label each of those nodes from
[00:28:06:260 - 00:28:07:180] **Speaker 1:** equal 1.
[00:28:08:760 - 00:28:18:349] **Speaker 1:** To And 3 And were asked to circle each node.
[00:28:19:800 - 00:28:21:079] **Speaker 1:** With an unknown degree of freedom.
[00:28:21:119 - 00:28:23:599] **Speaker 1:** So which of these nodes are unknown that we would
[00:28:23:599 - 00:28:26:680] **Speaker 1:** have to solve for with our numerical scheme?
[00:28:29:689 - 00:28:30:050] **Speaker 1:** Sorry?
[00:28:31:050 - 00:28:32:589] **Speaker 1:** I equals 2 is the mid 1, yeah.
[00:28:34:349 - 00:28:35:390] **Speaker 1:** So it's going to be the general case.
[00:28:35:489 - 00:28:37:069] **Speaker 1:** Do we have to solve for I equal 1 or
[00:28:37:069 - 00:28:37:609] **Speaker 1:** 3?
[00:28:37:989 - 00:28:39:310] **Speaker 1:** Are we given those values?
[00:28:45:150 - 00:28:45:959] **Speaker 1:** And I, yep.
[00:28:46:310 - 00:28:49:829] **Speaker 1:** So at I equal 1, we've got a boundary condition
[00:28:50:189 - 00:28:51:510] **Speaker 1:** of zero displacement.
[00:28:52:349 - 00:28:54:270] **Speaker 1:** And on the right, we've got a boundary condition of
[00:28:54:270 - 00:28:55:829] **Speaker 1:** the slope equal to 0.
[00:28:56:959 - 00:28:58:959] **Speaker 1:** Because the slope 0, we don't know what value you
[00:28:58:959 - 00:29:00:959] **Speaker 1:** holds, so it's an unknown degree of freedom that we
[00:29:00:959 - 00:29:01:540] **Speaker 1:** solve for.
[00:29:09:260 - 00:29:11:819] **Speaker 1:** And that's, that's it for that, that question.
[00:29:21:800 - 00:29:24:239] **Speaker 1:** Uh, next we're asked to discretize our governing equation for
[00:29:24:239 - 00:29:26:319] **Speaker 1:** each unknown degree of freedom, so it'd be i equals
[00:29:26:319 - 00:29:26:939] **Speaker 1:** 2 and 3.
[00:29:27:760 - 00:29:30:319] **Speaker 1:** Using the explicit scheme of second-order central differencing.
[00:29:31:119 - 00:29:33:030] **Speaker 1:** And rearranging with unknowns on the left and 9 terms
[00:29:33:030 - 00:29:34:880] **Speaker 1:** on the right, just as done in class.
[00:29:35:280 - 00:29:38:239] **Speaker 1:** So if we refer back to our formula sheet at
[00:29:38:239 - 00:29:41:300] **Speaker 1:** the bottom, I've included the two-step finite differencing.
[00:29:41:880 - 00:29:44:079] **Speaker 1:** We've got the second-order central difference scheme for the time
[00:29:44:079 - 00:29:47:239] **Speaker 1:** derivative and on the right we've got FIN and I've
[00:29:47:239 - 00:29:49:319] **Speaker 1:** defined FIN somewhere.
[00:29:50:410 - 00:29:50:890] **Speaker 1:** Have I?
[00:29:57:140 - 00:29:58:660] **Speaker 1:** It'll be, it'll be this guy.
[00:30:02:170 - 00:30:04:390] **Speaker 1:** Uh, with F discretized by central.
[00:30:04:770 - 00:30:06:089] **Speaker 1:** So central is up here.
[00:30:09:479 - 00:30:11:300] **Speaker 1:** For our 2nd order derivative in space.
[00:30:12:530 - 00:30:14:650] **Speaker 1:** And also, oh, I have to sign out.
[00:30:25:290 - 00:30:28:260] **Speaker 1:** So when you're asked to do, I guess specific nodes,
[00:30:28:339 - 00:30:29:859] **Speaker 1:** it would make sense to do the general case first,
[00:30:29:939 - 00:30:32:520] **Speaker 1:** leaving them as I's and J's or I's and ends,
[00:30:33:109 - 00:30:35:380] **Speaker 1:** and then apply it for each degree of freedom that
[00:30:35:380 - 00:30:36:390] **Speaker 1:** you're interested in.
[00:30:36:900 - 00:30:38:380] **Speaker 1:** So then you can just refer back to the general
[00:30:38:380 - 00:30:38:790] **Speaker 1:** case.
[00:31:00:869 - 00:31:06:010] **Speaker 1:** So discretizing that governing equation, D2U by DT2, we have
[00:31:06:270 - 00:31:07:270] **Speaker 1:** our central order.
[00:31:09:680 - 00:31:13:280] **Speaker 1:** Central difference second order scheme of UIN +1.
[00:31:15:430 - 00:31:20:280] **Speaker 1:** -2 UIN plus UIN minus 1.
[00:31:21:489 - 00:31:22:800] **Speaker 1:** Divided by D T 2.
[00:31:28:479 - 00:31:31:079] **Speaker 1:** How should we go about discretizing this first order derivative
[00:31:31:079 - 00:31:31:660] **Speaker 1:** in time?
[00:31:46:650 - 00:31:48:680] **Speaker 1:** We want to have 2 order accuracy.
[00:31:49:650 - 00:31:52:260] **Speaker 1:** And we've looked at central differenceencing in class.
[00:31:55:079 - 00:31:58:319] **Speaker 1:** How do we discretize this DU by DT?
[00:32:07:079 - 00:32:08:560] **Speaker 1:** What have we got on our formula sheet?
[00:32:10:339 - 00:32:11:959] **Speaker 1:** So if you're using central difference.
[00:32:13:569 - 00:32:16:010] **Speaker 1:** We can use this, this equation.
[00:32:16:839 - 00:32:19:880] **Speaker 1:** Instead of X, T is our independent variable, so we're
[00:32:19:880 - 00:32:23:319] **Speaker 1:** going to have DU by DT equal to UN +
[00:32:23:319 - 00:32:26:369] **Speaker 1:** 1 minus UIN minus 1 over 2T.
[00:32:35:839 - 00:32:40:569] **Speaker 1:** And those Jews cancel And on the right-hand side we've
[00:32:40:569 - 00:32:45:119] **Speaker 1:** got C2 and the more familiar central difference for that
[00:32:45:119 - 00:32:45:780] **Speaker 1:** spatial term.
[00:32:46:290 - 00:32:50:890] **Speaker 1:** You've got UI + 1 minus 2 UI plus UI
[00:32:50:890 - 00:32:52:810] **Speaker 1:** minus 1 divided by X2.
[00:32:55:060 - 00:32:58:459] **Speaker 1:** What time level should we evaluate our spatial term at?
[00:33:12:109 - 00:33:14:109] **Speaker 1:** If you recall the heat equation, we looked at those
[00:33:14:109 - 00:33:15:859] **Speaker 1:** explicit and implicit schemes.
[00:33:16:520 - 00:33:20:280] **Speaker 1:** The explicit scheme was evaluating terms at like the current
[00:33:20:280 - 00:33:22:520] **Speaker 1:** time level and implicit was at the next time level
[00:33:22:520 - 00:33:25:660] **Speaker 1:** and we formed that system of simultaneous equations to solve.
[00:33:26:599 - 00:33:29:160] **Speaker 1:** In this question, and what we've done in class, we're
[00:33:29:160 - 00:33:31:609] **Speaker 1:** asked to use the explicit scheme.
[00:33:34:310 - 00:33:38:310] **Speaker 1:** So what time level should we impose on our spatial.
[00:33:39:030 - 00:33:39:900] **Speaker 1:** Central difference.
[00:33:41:280 - 00:33:47:150] **Speaker 1:** In Cool.
[00:33:50:189 - 00:33:52:750] **Speaker 1:** So that's discretized our governing equation with this scheme.
[00:33:53:069 - 00:33:54:709] **Speaker 1:** Now we want to apply it for each of these
[00:33:54:709 - 00:33:56:500] **Speaker 1:** two unknown nodes.
[00:33:56:910 - 00:33:57:849] **Speaker 1:** So I equals 2.
[00:33:59:729 - 00:34:01:030] **Speaker 1:** We're going to substitute in.
[00:34:02:239 - 00:34:03:089] **Speaker 1:** I equal to 2.
[00:34:03:829 - 00:34:16:850] **Speaker 1:** So we have U to N + 1.
[00:34:17:699 - 00:34:27:060] **Speaker 1:** -2U2N plus U2N minus 1 over T2 plus E.
[00:34:28:709 - 00:34:34:469] **Speaker 1:** U2 N + 1 minus U2N minus 1 over D
[00:34:34:699 - 00:34:38:350] **Speaker 1:** equal to C2, U2N U3.
[00:34:39:128 - 00:34:44:648] **Speaker 1:** We've got I + 1 minus 2U2N and U1N.
[00:34:45:789 - 00:34:46:208] **Speaker 1:** Over data.
[00:34:59:159 - 00:35:02:469] **Speaker 1:** So if this goes for that um that mid mid
[00:35:02:469 - 00:35:03:550] **Speaker 1:** node, I equal to.
[00:35:08:629 - 00:35:10:189] **Speaker 1:** I mean, if we want, we could also apply the
[00:35:10:189 - 00:35:12:070] **Speaker 1:** boundary condition at 114 to 1.
[00:35:12:229 - 00:35:14:639] **Speaker 1:** We know that the displacement on the left hand boundary
[00:35:14:639 - 00:35:15:800] **Speaker 1:** is fixed at 0.
[00:35:17:020 - 00:35:19:580] **Speaker 1:** So we've only got one term here, but that's just
[00:35:19:580 - 00:35:20:060] **Speaker 1:** 0.
[00:35:28:810 - 00:35:30:500] **Speaker 1:** Maybe it'll come back, um.
[00:35:31:360 - 00:35:36:889] **Speaker 1:** So Next step is to rearrange with the unknowns on
[00:35:36:889 - 00:35:39:360] **Speaker 1:** the left and the known terms on the right, which
[00:35:39:360 - 00:35:40:409] **Speaker 1:** of these are unknown.
[00:35:41:610 - 00:35:44:570] **Speaker 1:** Well, which are the known terms might be easier in,
[00:35:44:719 - 00:35:45:570] **Speaker 1:** in this equation?
[00:35:56:439 - 00:35:58:360] **Speaker 1:** So the ones that are in and in minus 1.
[00:35:59:679 - 00:36:01:360] **Speaker 1:** Uh, the nuns, yep.
[00:36:02:750 - 00:36:04:709] **Speaker 1:** So they're going to be on the right-hand side, and
[00:36:04:709 - 00:36:06:550] **Speaker 1:** then N + 1 is unknown, so it's going to
[00:36:06:550 - 00:36:07:090] **Speaker 1:** be on the left.
[00:36:10:889 - 00:36:23:459] **Speaker 1:** So We'll look at the U2 N +1s, U2, U2.
[00:36:24:399 - 00:36:28:290] **Speaker 1:** And we have If you times everything by T2.
[00:36:30:429 - 00:36:33:709] **Speaker 1:** We're left with one Plus.
[00:36:35:199 - 00:36:35:530] **Speaker 1:** B T.
[00:36:40:729 - 00:36:42:399] **Speaker 1:** And on the right hand side.
[00:36:44:590 - 00:36:46:729] **Speaker 1:** We're going to introduce the C number.
[00:36:51:080 - 00:36:54:439] **Speaker 1:** And I'm just gonna use capital C because that's more
[00:36:54:439 - 00:36:56:199] **Speaker 1:** obvious to me, but you can use lambda if you
[00:36:56:199 - 00:36:56:469] **Speaker 1:** want.
[00:36:56:760 - 00:36:58:639] **Speaker 1:** CT over X.
[00:37:01:360 - 00:37:03:770] **Speaker 1:** And we have you.
[00:37:05:699 - 00:37:15:800] **Speaker 1:** To In And you 3 in So it might be
[00:37:15:800 - 00:37:17:260] **Speaker 1:** easier just to start over here.
[00:37:18:750 - 00:37:24:459] **Speaker 1:** And we've got C2 over X2 times T2, which is
[00:37:24:459 - 00:37:26:290] **Speaker 1:** our current number 2.
[00:37:27:629 - 00:37:33:580] **Speaker 1:** Multiplied by U3N minus 2U2N.
[00:37:46:000 - 00:37:48:840] **Speaker 1:** And now we've got you two in.
[00:37:57:419 - 00:38:00:810] **Speaker 1:** And for U2 N minus 1.
[00:38:01:929 - 00:38:03:379] **Speaker 1:** We have the.
[00:38:04:469 - 00:38:06:629] **Speaker 1:** Times data.
[00:38:09:000 - 00:38:11:409] **Speaker 1:** Minus One.
[00:38:13:800 - 00:38:15:169] **Speaker 1:** U2 N minus 1.
[00:38:34:520 - 00:38:36:780] **Speaker 1:** So you could do more intermediate steps if you wish,
[00:38:37:199 - 00:38:37:939] **Speaker 1:** um.
[00:38:40:439 - 00:38:42:280] **Speaker 1:** One way is just to tick off which ones you've
[00:38:42:280 - 00:38:44:399] **Speaker 1:** applied to that next row.
[00:38:45:459 - 00:38:47:629] **Speaker 1:** But the idea here is that we're just rearranging so
[00:38:47:629 - 00:38:48:370] **Speaker 1:** that we know which.
[00:38:49:280 - 00:38:51:409] **Speaker 1:** Terms we're trying to solve for on the left-hand side.
[00:38:52:270 - 00:38:53:909] **Speaker 1:** And all those terms on the right, it doesn't matter
[00:38:53:909 - 00:38:58:899] **Speaker 1:** too much how you've formulated these or, Uh, I've written
[00:38:58:899 - 00:39:01:300] **Speaker 1:** them out in full, doesn't matter if they're in brackets.
[00:39:04:419 - 00:39:07:850] **Speaker 1:** And for I equal to 3.
[00:39:15:659 - 00:39:18:389] **Speaker 1:** We need to discretize.
[00:39:19:350 - 00:39:23:860] **Speaker 1:** Our boundary condition on the right hand side, so look,
[00:39:24:149 - 00:39:25:030] **Speaker 1:** we're off the verge.
[00:39:26:050 - 00:39:28:889] **Speaker 1:** Does anyone remember how we can discretize that that Neumann
[00:39:28:889 - 00:39:29:550] **Speaker 1:** boundary condition?
[00:39:52:439 - 00:39:52:959] **Speaker 1:** Yes.
[00:40:00:489 - 00:40:02:110] **Speaker 1:** So essentially you've got you.
[00:40:05:370 - 00:40:07:610] **Speaker 1:** We can label it for, I guess, being a ghost
[00:40:07:610 - 00:40:09:209] **Speaker 1:** node minus um.
[00:40:10:179 - 00:40:13:870] **Speaker 1:** U2 divided by 2 X is equal to 0.
[00:40:14:790 - 00:40:17:270] **Speaker 1:** So U4 is equal to U2.
[00:40:22:350 - 00:40:24:780] **Speaker 1:** So we could go through and write all this out
[00:40:24:780 - 00:40:25:120] **Speaker 1:** again.
[00:40:26:550 - 00:40:29:229] **Speaker 1:** Um, I'm being a bit lazy, so I'm just going
[00:40:29:229 - 00:40:33:189] **Speaker 1:** to say that 2s become 3s because we're now looking
[00:40:33:189 - 00:40:34:189] **Speaker 1:** at I equal to 3.
[00:40:34:590 - 00:40:36:830] **Speaker 1:** It's got 1 plus B out of T.
[00:40:38:229 - 00:40:41:070] **Speaker 1:** U 3 N + 1 equal to.
[00:40:44:379 - 00:40:49:659] **Speaker 1:** Our current number, which, what happens here, we've got 4
[00:40:49:659 - 00:40:50:399] **Speaker 1:** instead of 3.
[00:40:53:550 - 00:40:54:929] **Speaker 1:** Come Yeah.
[00:40:55:879 - 00:40:58:360] **Speaker 1:** So now we have you two.
[00:42:08:399 - 00:42:09:600] **Speaker 1:** Oh, what are we doing now?
[00:42:20:070 - 00:42:22:649] **Speaker 1:** Now we want to discharge for that first time step
[00:42:23:419 - 00:42:25:189] **Speaker 1:** by applying that initial velocity condition.
[00:42:26:120 - 00:42:27:840] **Speaker 1:** So I'll give you a moment to think about that.
[00:42:50:570 - 00:42:51:870] **Speaker 1:** I guess before we do that.
[00:42:53:060 - 00:42:53:659] **Speaker 1:** Um.
[00:42:55:129 - 00:43:00:060] **Speaker 1:** Because we've got U1N that I said was zero, this
[00:43:00:060 - 00:43:04:760] **Speaker 1:** is also carrying through because instead of being U1, it's
[00:43:04:760 - 00:43:07:909] **Speaker 1:** now U2, so we're going to have 2 U2N.
[00:43:08:699 - 00:43:10:060] **Speaker 1:** So it might be a bit dangerous to apply the
[00:43:10:060 - 00:43:12:540] **Speaker 1:** boundary condition in that that first step.
[00:43:14:699 - 00:43:15:750] **Speaker 1:** So this is carrying through.
[00:43:16:439 - 00:43:18:129] **Speaker 1:** But if you went through from the general case, you
[00:43:18:129 - 00:43:18:989] **Speaker 1:** might get that.
[00:43:19:370 - 00:43:20:129] **Speaker 1:** You won't skip it.
[00:43:24:979 - 00:43:27:699] **Speaker 1:** Teaching you bad habits, that's no good, so yeah, go
[00:43:27:699 - 00:43:30:540] **Speaker 1:** through from the general case and then then work through.
[00:43:31:510 - 00:43:33:139] **Speaker 1:** So we're going to apply that first time step by
[00:43:33:139 - 00:43:37:090] **Speaker 1:** enforcing that initial condition, and because I don't have enough
[00:43:37:790 - 00:43:39:870] **Speaker 1:** space to show you, I'll just rewrite it.
[00:44:55:129 - 00:44:58:570] **Speaker 1:** So for that midpoint I equals 2, we're going to
[00:44:58:570 - 00:45:02:620] **Speaker 1:** substitute in UIN minus 1 equal to UIN + 1.
[00:45:05:550 - 00:45:06:530] **Speaker 1:** So what have we got?
[00:45:08:669 - 00:45:12:949] **Speaker 1:** U2 N minus 1, which is this guy on the
[00:45:12:949 - 00:45:13:370] **Speaker 1:** right.
[00:45:14:449 - 00:45:17:080] **Speaker 1:** is equal to U2N + 1.
[00:45:18:760 - 00:45:21:820] **Speaker 1:** So the BT is cancel and we end up with
[00:45:22:040 - 00:45:24:439] **Speaker 1:** 2 times U2 M + 1.
[00:45:31:250 - 00:45:32:750] **Speaker 1:** And I've still got the current number.
[00:45:35:689 - 00:45:39:770] **Speaker 1:** U 3 N minus 2 U 2 N.
[00:45:40:899 - 00:45:43:260] **Speaker 1:** And to you too.
[00:45:52:590 - 00:45:54:969] **Speaker 1:** And for that right-hand node, I equal to 3.
[00:45:59:080 - 00:46:02:909] **Speaker 1:** We are substituting in UI which is 3, so U3
[00:46:02:909 - 00:46:06:500] **Speaker 1:** minus 1 on the right with U3N + 1.
[00:46:06:879 - 00:46:07:469] **Speaker 1:** So again, BT.
[00:46:08:989 - 00:46:11:129] **Speaker 1:** It's gonna cancel, and we've got 2.
[00:46:12:320 - 00:46:14:439] **Speaker 1:** U3 N + 1 equal to.
[00:46:15:719 - 00:46:19:600] **Speaker 1:** C22U2N minus 2U3N.
[00:46:20:500 - 00:46:21:959] **Speaker 1:** And 2, U, 3.
[00:46:39:810 - 00:46:40:169] **Speaker 1:** Cool.
[00:46:47:389 - 00:46:51:750] **Speaker 1:** So Yeah, it's it's 12 marks out of 60.
[00:46:52:810 - 00:46:53:649] **Speaker 1:** That's a 5th.
[00:46:54:729 - 00:46:57:649] **Speaker 1:** So you get, oh I can't do maths, it's probably
[00:46:57:649 - 00:46:59:649] **Speaker 1:** about half an hour or something in the exam to
[00:46:59:649 - 00:47:00:469] **Speaker 1:** go work through the whole question.
[00:47:02:239 - 00:47:04:050] **Speaker 1:** Yeah, a bit over half an hour, um.
[00:47:06:939 - 00:47:09:729] **Speaker 1:** So the next step is to perform 2 time steps.
[00:47:09:780 - 00:47:11:699] **Speaker 1:** Now that we've got our discretized equations, we can actually
[00:47:11:699 - 00:47:12:350] **Speaker 1:** solve something.
[00:47:12:659 - 00:47:14:459] **Speaker 1:** They had calculators in this year and you don't.
[00:47:14:739 - 00:47:16:780] **Speaker 1:** So if I give you any questions to solve things,
[00:47:16:899 - 00:47:17:979] **Speaker 1:** they'll be easy numbers.
[00:47:19:169 - 00:47:21:120] **Speaker 1:** But in this case I'll just go ahead and give
[00:47:21:120 - 00:47:21:840] **Speaker 1:** the solutions.
[00:47:21:979 - 00:47:23:159] **Speaker 1:** So in the initial.
[00:47:25:260 - 00:47:29:550] **Speaker 1:** condition At times 0.
[00:47:32:459 - 00:47:35:659] **Speaker 1:** And we've got 3 coordinates x 1.
[00:47:36:750 - 00:47:40:639] **Speaker 1:** Next to And X3.
[00:47:41:659 - 00:47:43:090] **Speaker 1:** So the length is one.
[00:47:44:560 - 00:47:46:860] **Speaker 1:** B and C are 1, time step 2.
[00:47:48:110 - 00:47:52:270] **Speaker 1:** And the initial profile or the initial condition.
[00:47:53:939 - 00:47:57:290] **Speaker 1:** Is given by 0.1 sign pi X over 2 L.
[00:47:58:739 - 00:48:00:149] **Speaker 1:** So we evaluate that.
[00:48:00:179 - 00:48:02:060] **Speaker 1:** If we had a calculator, we've got 0.
[00:48:02:860 - 00:48:04:229] **Speaker 1:** 0.0707.
[00:48:05:000 - 00:48:09:399] **Speaker 1:** And 0.1 Then we've got the first time that.
[00:48:13:639 - 00:48:14:800] **Speaker 1:** T equals 2.
[00:48:16:840 - 00:48:21:600] **Speaker 1:** That left hand boundary, the deflection is fixed at 0,
[00:48:21:760 - 00:48:23:139] **Speaker 1:** so it remains at 0.
[00:48:24:500 - 00:48:29:659] **Speaker 1:** Then we calculate for U2 and U3, and we get
[00:48:29:659 - 00:48:45:459] **Speaker 1:** -0.2607 and -0.3686. And 2nd time Again, 0, we've got
[00:48:45:459 - 00:48:48:340] **Speaker 1:** 0.6641.
[00:48:49:300 - 00:48:52:790] **Speaker 1:** And 0.9392.
[00:48:57:010 - 00:49:00:850] **Speaker 1:** So, this last question, I'd like you just to plot
[00:49:00:850 - 00:49:06:250] **Speaker 1:** these deflections, so sketch them out on, On an axis.
[00:49:07:080 - 00:49:09:600] **Speaker 1:** And comment on whether or not the solution makes physical
[00:49:09:600 - 00:49:10:080] **Speaker 1:** sense.
[00:49:48:479 - 00:49:49:800] **Speaker 1:** Actually I'm not going to be able to draw it
[00:49:49:800 - 00:49:52:040] **Speaker 1:** faster than just showing you what I prepared in the
[00:49:52:040 - 00:49:58:820] **Speaker 1:** solution, so, um, here we've got our, Displacement on the
[00:49:58:820 - 00:50:03:540] **Speaker 1:** vertical axis and X is just the spatial cordon X.
[00:50:04:139 - 00:50:07:239] **Speaker 1:** I've sketched time 02 and 4.
[00:50:08:120 - 00:50:12:909] **Speaker 1:** And what you're expecting for something that starts at best
[00:50:13:090 - 00:50:17:129] **Speaker 1:** and is released, you don't expect it to become unbounded,
[00:50:17:189 - 00:50:18:629] **Speaker 1:** like get larger and larger.
[00:50:19:129 - 00:50:22:270] **Speaker 1:** So here what we're seeing is that the maximum amplitude
[00:50:22:449 - 00:50:24:550] **Speaker 1:** of our string is getting bigger and bigger.
[00:50:25:050 - 00:50:25:610] **Speaker 1:** So this.
[00:50:27:000 - 00:50:29:439] **Speaker 1:** Probably raises the question, is this a realistic solution?
[00:50:30:419 - 00:50:32:179] **Speaker 1:** If we actually look at our current number, it's equal
[00:50:32:179 - 00:50:34:899] **Speaker 1:** to 4, so this explains some of the instability in
[00:50:34:899 - 00:50:35:899] **Speaker 1:** that solution.
[00:50:38:889 - 00:50:42:949] **Speaker 1:** So, Yeah, a little bit of a reflection on what
[00:50:42:949 - 00:50:46:189] **Speaker 1:** you're, you're working on and then tying that into some
[00:50:46:189 - 00:50:49:110] **Speaker 1:** of the, the theory that we've we've discussed in class.
[00:50:50:389 - 00:50:52:360] **Speaker 1:** So Yeah.
[00:50:52:639 - 00:50:54:879] **Speaker 1:** Generally the earlier questions are easier and then it gets
[00:50:54:879 - 00:50:57:360] **Speaker 1:** a little bit more challenging um throughout.
[00:50:58:979 - 00:51:01:379] **Speaker 1:** Cool, alright, so I think that is, is a good
[00:51:01:379 - 00:51:05:399] **Speaker 1:** spot to stop and we've got those labs this afternoon,
[00:51:05:780 - 00:51:07:860] **Speaker 1:** so obviously most of you in there.
[00:51:08:510 - 00:51:10:370] **Speaker 1:** And then we'll go through the exam sort of as
[00:51:10:370 - 00:51:11:989] **Speaker 1:** an introduction tomorrow.
[00:52:04:300 - 00:52:04:310] **Speaker 0:** Thank.
[00:52:06:379 - 00:52:06:699] **Speaker 0:** Yeah.
[00:52:11:239 - 00:52:11:250] **Speaker 0:** First.
[00:52:34:129 - 00:52:36:169] **Speaker 0:** Oh yeah.
[00:52:38:479 - 00:52:39:800] **Speaker 0:** Maybe you can participate on.
[00:52:43:149 - 00:52:43:790] **Speaker 0:** I always just call me.
[00:52:43:800 - 00:52:47:870] **Speaker 0:** No, I, um, I haven't finished that.
[00:52:50:729 - 00:52:51:090] **Speaker 1:** I do not.
[00:52:53:080 - 00:53:12:479] **Speaker 0:** Yeah, oh, I never I No, I I saw that.
[00:53:14:260 - 00:53:15:250] **Speaker 0:** Yeah, exactly.
[00:53:19:379 - 00:53:19:389] **Speaker 0:** Yeah.
[00:53:44:709 - 00:54:45:830] **Speaker 0:** Like the first I Yeah 8 STA Uh, I wasn't
[00:54:47:729 - 00:54:53:530] **Speaker 0:** So I I didn't get

# ENME302-26S2 Lecture 42 native Echo transcript

Date: October 7, 2026 11:00am-11:55am
Transcript type: native Echo automated transcript.

[00:00:02:140 - 00:00:12:899] **Speaker 0:** Yeah that.
[00:00:17:250 - 00:00:18:040] **Speaker 0:** I'm just saying.
[00:00:26:670 - 00:01:08:430] **Speaker 0:** to I That Yeah Uh, good morning, we'll make a
[00:01:08:430 - 00:01:09:050] **Speaker 1:** start.
[00:01:09:989 - 00:01:12:870] **Speaker 1:** Um, so there are some questions about the assignment that
[00:01:12:870 - 00:01:14:730] **Speaker 1:** I just wanna go through first.
[00:01:15:349 - 00:01:15:830] **Speaker 2:** So.
[00:01:17:459 - 00:01:19:959] **Speaker 1:** Um, yeah, I guess as, as a general principle, if
[00:01:19:959 - 00:01:21:580] **Speaker 1:** you get stuck on a certain part of the assignment,
[00:01:21:660 - 00:01:24:699] **Speaker 1:** you can go and start the other parts, um, and
[00:01:24:699 - 00:01:25:699] **Speaker 1:** then come back to it later.
[00:01:25:860 - 00:01:27:940] **Speaker 1:** So don't feel like you can't do anything once you
[00:01:27:940 - 00:01:29:379] **Speaker 1:** get stuck at a particular point.
[00:01:30:120 - 00:01:33:080] **Speaker 1:** Uh, each of those four parts can be done reasonably
[00:01:33:080 - 00:01:35:559] **Speaker 1:** independently, so that should be good.
[00:01:36:669 - 00:01:39:760] **Speaker 1:** And there's some questions on.
[00:01:41:190 - 00:01:45:029] **Speaker 1:** Oh, so part 4, maybe I've still got the assignment.
[00:01:49:120 - 00:01:52:139] **Speaker 1:** Part 4 is looking at improving the model.
[00:01:53:839 - 00:02:01:739] **Speaker 0:** Um So yeah, start with the Axisymmetric 2D circuit pat
[00:02:01:739 - 00:02:02:660] **Speaker 1:** patty model.
[00:02:02:860 - 00:02:05:019] **Speaker 1:** Uh, don't worry too much about the, the flipping part
[00:02:05:019 - 00:02:07:699] **Speaker 1:** of it, um, you can do it without flipping if
[00:02:07:699 - 00:02:09:509] **Speaker 1:** you want, so that's just up to you.
[00:02:09:740 - 00:02:11:580] **Speaker 1:** It is a bit more involved to do that, the
[00:02:11:580 - 00:02:14:919] **Speaker 1:** flipping with, uh, the, The pan.
[00:02:15:529 - 00:02:17:690] **Speaker 1:** So that's, that's just optional.
[00:02:17:740 - 00:02:18:520] **Speaker 1:** It's up to you.
[00:02:18:949 - 00:02:22:880] **Speaker 1:** And there's a few questions about uh like consistent initialization.
[00:02:23:259 - 00:02:26:619] **Speaker 1:** So having that initial or singularity at the pan, you've
[00:02:26:619 - 00:02:30:100] **Speaker 1:** got 210, if I remember the number.
[00:02:31:770 - 00:02:34:410] **Speaker 1:** We've got a T pan of 210 and the initial
[00:02:34:410 - 00:02:35:369] **Speaker 1:** condition is 3 degrees.
[00:02:35:809 - 00:02:37:509] **Speaker 1:** So that gives them a little bit of funky behaviour
[00:02:37:509 - 00:02:38:429] **Speaker 1:** in console.
[00:02:39:029 - 00:02:41:110] **Speaker 1:** So I just want to go through some demonstration here.
[00:02:42:160 - 00:02:44:259] **Speaker 1:** Because we looked at a similar problem in class in
[00:02:44:259 - 00:02:45:130] **Speaker 1:** chapter 5.
[00:02:46:089 - 00:02:48:919] **Speaker 0:** Serve it here And then we'll get on to chapter
[00:02:48:919 - 00:02:50:399] **Speaker 1:** 7, so that's exciting.
[00:02:50:800 - 00:02:54:800] **Speaker 1:** So chapter 5, we looked at, Can I zoom in.
[00:02:58:660 - 00:03:01:699] **Speaker 1:** Uh, we looked at the heat equation and we solved
[00:03:01:699 - 00:03:04:660] **Speaker 1:** this on like a semi-infinite slab, and we had an
[00:03:04:660 - 00:03:08:460] **Speaker 1:** initial temperature profile of T1 and then we introduced a
[00:03:08:460 - 00:03:11:619] **Speaker 1:** boundary of T infinity at X equals 0, so at
[00:03:11:619 - 00:03:13:779] **Speaker 1:** the surface maybe, and this.
[00:03:14:610 - 00:03:15:449] **Speaker 1:** It's essentially the same thing.
[00:03:15:529 - 00:03:17:800] **Speaker 1:** We've got a singularity at this X equals 0.
[00:03:18:410 - 00:03:21:649] **Speaker 1:** the initial condition doesn't satisfy the boundary condition.
[00:03:22:270 - 00:03:24:669] **Speaker 1:** So I've gone ahead and modelled this in console.
[00:03:25:860 - 00:03:27:690] **Speaker 1:** So I did that yesterday, it was good fun.
[00:03:32:470 - 00:03:35:270] **Speaker 1:** So I, I'll upload this after class.
[00:03:42:479 - 00:03:44:479] **Speaker 1:** Oh, it's changed everything, but that's not helpful.
[00:03:45:990 - 00:03:47:000] **Speaker 1:** Oh dear.
[00:03:54:380 - 00:03:57:839] **Speaker 1:** At least we do have two projectors, unlike the Nmarsh
[00:03:57:839 - 00:03:58:259] **Speaker 1:** theatre.
[00:04:00:050 - 00:04:01:130] **Speaker 1:** Oh, it's disconnected.
[00:04:03:039 - 00:04:05:380] **Speaker 1:** Oh, it's a good thing I logged in before class,
[00:04:05:520 - 00:04:05:800] **Speaker 1:** but.
[00:04:15:419 - 00:04:15:770] **Speaker 1:** Round two.
[00:04:26:410 - 00:04:27:839] **Speaker 1:** If you were quick you saw it, but.
[00:04:32:540 - 00:04:33:459] **Speaker 1:** This is brilliant.
[00:04:44:720 - 00:04:45:600] **Speaker 0:** Another flicker.
[00:04:48:549 - 00:04:51:869] **Speaker 1:** Um, Alright, OK, now we're going.
[00:04:52:070 - 00:04:53:130] **Speaker 1:** Alright, that's exciting.
[00:04:53:549 - 00:04:54:929] **Speaker 1:** Um, so this is the solution.
[00:04:55:940 - 00:04:58:100] **Speaker 1:** With 5 elements.
[00:04:58:179 - 00:04:59:660] **Speaker 1:** I'll just go through the console model, how I set
[00:04:59:660 - 00:05:00:160] **Speaker 1:** it up.
[00:05:00:630 - 00:05:03:290] **Speaker 1:** It should all be familiar to you now, but I've
[00:05:03:290 - 00:05:04:100] **Speaker 1:** set up some parameters.
[00:05:04:179 - 00:05:07:369] **Speaker 1:** We've got T1 and 10 being the temperatures, the initial
[00:05:07:369 - 00:05:08:540] **Speaker 1:** temperature and the base temperature.
[00:05:08:859 - 00:05:10:250] **Speaker 1:** I've just set these pretty arbitrarily.
[00:05:10:420 - 00:05:13:720] **Speaker 1:** We did this in uh non-conventional space, so it scales,
[00:05:14:420 - 00:05:15:910] **Speaker 1:** and I've set a heat defensivity.
[00:05:15:940 - 00:05:17:739] **Speaker 1:** I just looked up what what it was for concrete,
[00:05:17:880 - 00:05:19:380] **Speaker 1:** pretending it was some concrete slab.
[00:05:20:109 - 00:05:21:549] **Speaker 1:** And we've got a length of the domain.
[00:05:21:640 - 00:05:23:339] **Speaker 1:** We had to choose a length of the domain or
[00:05:23:339 - 00:05:27:630] **Speaker 1:** the thickness or depth of the concrete because it's essentially
[00:05:27:630 - 00:05:29:929] **Speaker 1:** solved as x goes to infinity.
[00:05:30:309 - 00:05:32:869] **Speaker 1:** I've chosen 1 metre as the length.
[00:05:35:359 - 00:05:37:279] **Speaker 1:** We need to have a number of mesh elements, we're
[00:05:37:279 - 00:05:38:799] **Speaker 1:** in a one dimensional domain.
[00:05:39:160 - 00:05:41:799] **Speaker 1:** I've chosen 5 to start with and a final time
[00:05:41:799 - 00:05:42:579] **Speaker 1:** of 6 hours.
[00:05:43:410 - 00:05:45:899] **Speaker 1:** So the analytical solution we derive in class.
[00:05:46:880 - 00:05:52:190] **Speaker 1:** So that was After waving some magic wand, we use
[00:05:52:190 - 00:05:54:750] **Speaker 1:** the error function, Gaussian error function, and we can use
[00:05:54:750 - 00:05:56:489] **Speaker 1:** this one apparently it's standard.
[00:05:56:829 - 00:06:00:410] **Speaker 1:** We can include this in console and here I'm plotting
[00:06:00:920 - 00:06:04:500] **Speaker 1:** the analytical temperature profile by rearranging the T.
[00:06:06:709 - 00:06:07:850] **Speaker 1:** So that's what this equation is.
[00:06:07:910 - 00:06:09:390] **Speaker 1:** If we go ahead and plot, we can try and
[00:06:09:390 - 00:06:10:730] **Speaker 1:** visualise what the solution looks like.
[00:06:12:640 - 00:06:15:170] **Speaker 1:** So It's a little bit small.
[00:06:20:579 - 00:06:23:739] **Speaker 1:** So at time 0, we're on this axis and we've
[00:06:23:739 - 00:06:28:480] **Speaker 1:** got this step going from T infinity up to T1
[00:06:28:480 - 00:06:31:149] **Speaker 1:** and then hold at T1 for all of time 0,
[00:06:31:500 - 00:06:34:459] **Speaker 1:** and then over time it starts to decay, and that's
[00:06:34:459 - 00:06:37:390] **Speaker 1:** what we try to sketch in our solution space.
[00:06:38:470 - 00:06:38:480] **Speaker 1:** Yes.
[00:06:41:619 - 00:06:43:820] **Speaker 1:** So that's what we're expecting, and it's really handy when
[00:06:43:820 - 00:06:46:029] **Speaker 1:** you're verifying your code, verifying your models to have an
[00:06:46:029 - 00:06:48:619] **Speaker 1:** analytical solution to compare against or to validate against.
[00:06:49:730 - 00:06:54:029] **Speaker 1:** And Next stage is to have our one-dimensional space.
[00:06:54:350 - 00:06:58:429] **Speaker 1:** The geometry is simply the length of 0 to 1
[00:06:58:429 - 00:07:02:570] **Speaker 1:** L, L being 1 metres, and our coefficient form PDE.
[00:07:03:070 - 00:07:04:869] **Speaker 1:** You could also use the heat transfer in solids if
[00:07:04:869 - 00:07:07:549] **Speaker 1:** you want, but for this, I just use the coefficient
[00:07:07:549 - 00:07:10:630] **Speaker 1:** form PDE and match the coefficients against our heat equation.
[00:07:11:519 - 00:07:21:279] **Speaker 1:** So we've got alpha As our diffusion coefficient, 0 elsewhere
[00:07:21:279 - 00:07:24:839] **Speaker 1:** and 1 for our damping coefficient, so that's DT by
[00:07:24:839 - 00:07:25:239] **Speaker 1:** DT.
[00:07:27:029 - 00:07:31:750] **Speaker 1:** Now, the default boundary condition for those uh console models
[00:07:31:750 - 00:07:35:070] **Speaker 1:** or final elements is Norman 0 flux.
[00:07:36:029 - 00:07:39:829] **Speaker 1:** The initial value of set T1, and to start with,
[00:07:39:950 - 00:07:42:149] **Speaker 1:** I've set the directly boundary condition of T1 on the
[00:07:42:149 - 00:07:45:670] **Speaker 1:** right, so this is that far side, and the boundary
[00:07:45:670 - 00:07:46:209] **Speaker 1:** condition on the left.
[00:07:48:600 - 00:07:50:200] **Speaker 1:** Is just tea infinity.
[00:07:51:799 - 00:07:53:769] **Speaker 1:** So if we go ahead and solve this on our
[00:07:53:769 - 00:07:54:269] **Speaker 1:** mash.
[00:07:56:079 - 00:07:57:910] **Speaker 1:** It plots what I was just showing before.
[00:07:58:730 - 00:08:03:100] **Speaker 0:** Uh, but this Generally match is not too bad, so
[00:08:03:100 - 00:08:03:959] **Speaker 1:** if we zoom in.
[00:08:06:000 - 00:08:06:940] **Speaker 1:** On our domain.
[00:08:07:299 - 00:08:10:940] **Speaker 1:** It's quite poor at the early times where we've got
[00:08:10:940 - 00:08:14:260] **Speaker 1:** large temperature gradients that are a little bit off, that
[00:08:14:260 - 00:08:14:980] **Speaker 1:** are inaccurate.
[00:08:15:910 - 00:08:19:480] **Speaker 1:** And over time it's about the same because the early
[00:08:19:480 - 00:08:21:920] **Speaker 1:** effects has less impact on the later time.
[00:08:22:859 - 00:08:23:760] **Speaker 2:** Image profiles.
[00:08:25:940 - 00:08:26:989] **Speaker 1:** So a couple of features here.
[00:08:27:230 - 00:08:30:070] **Speaker 1:** We can see that we've got this overshoot, uh, which
[00:08:30:070 - 00:08:32:750] **Speaker 1:** you've observed, or some of you have observed in your
[00:08:32:750 - 00:08:37:469] **Speaker 1:** meat patties or chicken patties, and it's overshooting also for
[00:08:37:469 - 00:08:38:229] **Speaker 1:** the second time.
[00:08:38:429 - 00:08:42:030] **Speaker 1:** So 0.5 hours and at time zero.
[00:08:43:400 - 00:08:44:539] **Speaker 1:** So what can we do?
[00:08:45:000 - 00:08:47:640] **Speaker 1:** So one thing uh that we can look at.
[00:08:50:890 - 00:08:57:979] **Speaker 2:** Is Adjust the boundary condition with a vamp.
[00:08:59:489 - 00:09:02:070] **Speaker 1:** So that's what we'll do first, we'll disable.
[00:09:03:919 - 00:09:10:500] **Speaker 1:** Our initial And enable our boundary condition with the ramp.
[00:09:10:950 - 00:09:14:260] **Speaker 1:** So here we're seeing the temperature profile equal to T1.
[00:09:15:539 - 00:09:19:059] **Speaker 1:** Generally, and then we've applied a ramp function which goes
[00:09:19:059 - 00:09:20:000] **Speaker 1:** from 0.
[00:09:21:669 - 00:09:22:309] **Speaker 1:** Up to one.
[00:09:23:770 - 00:09:24:840] **Speaker 1:** On some interval.
[00:09:25:179 - 00:09:27:539] **Speaker 1:** So I've chosen over that first half second it's going
[00:09:27:539 - 00:09:28:419] **Speaker 1:** from 0 up to 1.
[00:09:28:539 - 00:09:31:739] **Speaker 1:** You can adjust the slope, location, uh, cutoff, and some
[00:09:31:739 - 00:09:32:299] **Speaker 1:** smoothing.
[00:09:33:190 - 00:09:39:190] **Speaker 1:** So I've applied this to my Boundary condition, so this
[00:09:39:570 - 00:09:40:650] **Speaker 1:** starts at T1.
[00:09:41:549 - 00:09:44:630] **Speaker 1:** And then it's going to ramp up to T infinity
[00:09:44:630 - 00:09:45:570] **Speaker 1:** with this equation.
[00:09:46:000 - 00:09:51:030] **Speaker 1:** So it smoothly transitions from T1 to T infinity, and
[00:09:51:030 - 00:09:54:630] **Speaker 1:** that means that our initial condition is fully consistent.
[00:09:54:780 - 00:09:56:070] **Speaker 1:** It's all equal to T1.
[00:09:56:859 - 00:09:59:419] **Speaker 1:** And then it slowly gradually ramps up to our T
[00:09:59:419 - 00:09:59:900] **Speaker 1:** infinity.
[00:10:01:270 - 00:10:03:599] **Speaker 1:** So that gets rid of the singularity.
[00:10:05:669 - 00:10:07:630] **Speaker 1:** Challenge within our equation.
[00:10:07:700 - 00:10:09:609] **Speaker 1:** So we're going to compute that and just check what
[00:10:09:619 - 00:10:10:330] **Speaker 1:** what happens.
[00:10:11:409 - 00:10:14:369] **Speaker 1:** So we've reduced the impact, but we can see that
[00:10:14:369 - 00:10:15:690] **Speaker 1:** it still has some overshoot.
[00:10:16:690 - 00:10:23:169] **Speaker 1:** So if we zoom in We've got uh still some
[00:10:23:390 - 00:10:25:710] **Speaker 1:** form of initialization here on that first time step.
[00:10:25:770 - 00:10:27:190] **Speaker 1:** It's not all equal to T1.
[00:10:28:049 - 00:10:31:390] **Speaker 1:** So what we can do under our time dependent solver,
[00:10:34:020 - 00:10:41:789] **Speaker 1:** Time stepping We can turn off consistent initialization, so turn
[00:10:41:789 - 00:10:42:409] **Speaker 1:** that off.
[00:10:43:400 - 00:10:44:080] **Speaker 1:** And compute.
[00:10:46:650 - 00:10:49:250] **Speaker 1:** And that should help with.
[00:10:50:239 - 00:10:52:280] **Speaker 1:** That initial condition, do you want?
[00:10:54:210 - 00:10:55:469] **Speaker 1:** So it's still overshooting.
[00:10:55:770 - 00:10:59:359] **Speaker 1:** So any ideas of what might be causing the, the
[00:10:59:359 - 00:11:02:210] **Speaker 1:** lack of accuracy in, in this case?
[00:11:15:500 - 00:11:18:460] **Speaker 1:** We've got quadratic chaffer lances.
[00:11:24:090 - 00:11:26:739] **Speaker 1:** Has anyone looked at this convergence plot when they sold
[00:11:26:739 - 00:11:27:020] **Speaker 1:** them?
[00:11:32:520 - 00:11:33:479] **Speaker 2:** What is this plotting?
[00:11:34:820 - 00:11:36:890] **Speaker 1:** So it's showing us that we've done 17 odd climb
[00:11:36:890 - 00:11:40:109] **Speaker 1:** steps, and it's showing the reciprocal of the step size.
[00:11:41:260 - 00:11:43:010] **Speaker 1:** So console has adaptive time setting.
[00:11:43:739 - 00:11:47:320] **Speaker 1:** So it's essentially Choosing a time set to match the
[00:11:47:320 - 00:11:52:590] **Speaker 1:** residuals that you're prescribing, so it starts off at, That
[00:11:52:590 - 00:11:55:760] **Speaker 1:** number, which I don't know, it's a bit hard to
[00:11:55:760 - 00:11:55:919] **Speaker 1:** read.
[00:11:56:000 - 00:12:02:140] **Speaker 1:** I guess it's 0.4, 6 seconds, and it goes down,
[00:12:02:280 - 00:12:06:650] **Speaker 1:** um, to, 0.4 milliseconds.
[00:12:07:710 - 00:12:10:229] **Speaker 1:** So it starts at quite a large time step.
[00:12:12:500 - 00:12:15:809] **Speaker 1:** And goes to a smaller one, so We've talked quite
[00:12:15:809 - 00:12:17:289] **Speaker 1:** a bit about mesh convergence.
[00:12:17:679 - 00:12:19:299] **Speaker 1:** At the moment, I'm just using the 5 elements.
[00:12:19:570 - 00:12:21:809] **Speaker 1:** Uh, we could ramp up those number of elements as
[00:12:21:809 - 00:12:24:270] **Speaker 1:** one way of reducing the dis discretization error.
[00:12:24:770 - 00:12:26:729] **Speaker 1:** Uh, but there's also the time-stepping that is important.
[00:12:27:609 - 00:12:32:469] **Speaker 1:** So the control that we have here is under tolerance
[00:12:32:869 - 00:12:35:799] **Speaker 1:** for adjusting how tight the system of equation should be
[00:12:35:799 - 00:12:36:289] **Speaker 1:** solved for.
[00:12:36:489 - 00:12:38:369] **Speaker 1:** So it's essentially adjusting the time stepping.
[00:12:39:409 - 00:12:41:789] **Speaker 1:** So I've kept this as physics control to start with,
[00:12:42:390 - 00:12:44:250] **Speaker 1:** uh, these output times are not the time stepping.
[00:12:45:619 - 00:12:46:960] **Speaker 1:** We can see under the log.
[00:12:51:890 - 00:12:54:210] **Speaker 1:** I've adjusted this, um.
[00:12:56:809 - 00:12:57:710] **Speaker 2:** When I was playing with it.
[00:12:58:530 - 00:12:59:710] **Speaker 2:** If we go back.
[00:13:10:049 - 00:13:17:090] **Speaker 1:** To How log somewhere.
[00:13:19:640 - 00:13:21:820] **Speaker 1:** So we'll keep that normal and I'll just run it
[00:13:21:820 - 00:13:22:159] **Speaker 1:** again.
[00:13:24:090 - 00:13:26:619] **Speaker 1:** So if you keep it as normal, you get this,
[00:13:26:729 - 00:13:28:820] **Speaker 1:** and the other day I was really confused because this
[00:13:28:820 - 00:13:30:539] **Speaker 1:** wasn't showing all of the time stamps.
[00:13:31:590 - 00:13:35:679] **Speaker 1:** So I've investigated further and found that it's not showing
[00:13:35:679 - 00:13:38:500] **Speaker 1:** all of the intermediate time steps because they're going too
[00:13:38:500 - 00:13:38:760] **Speaker 1:** quick.
[00:13:39:000 - 00:13:41:479] **Speaker 1:** So I don't usually do simulations that only take a
[00:13:41:479 - 00:13:42:799] **Speaker 1:** fraction of a second to solve.
[00:13:43:159 - 00:13:45:880] **Speaker 1:** Um, so I don't usually run into this issue, but
[00:13:45:880 - 00:13:48:919] **Speaker 1:** you can adjust the, the frequency that it reports these
[00:13:48:919 - 00:13:49:479] **Speaker 1:** values.
[00:13:52:669 - 00:13:56:140] **Speaker 1:** So wherever we were just before, which I've already forgotten
[00:13:56:140 - 00:13:56:750] **Speaker 1:** where we were.
[00:13:57:460 - 00:13:59:890] **Speaker 1:** So this log sampling, if we just write that down.
[00:14:01:440 - 00:14:02:619] **Speaker 1:** And, and compute.
[00:14:03:349 - 00:14:05:119] **Speaker 1:** OK, so now it's showing all the time steps.
[00:14:06:400 - 00:14:08:020] **Speaker 1:** So we can debug a little bit better.
[00:14:08:559 - 00:14:11:320] **Speaker 1:** So these are our time steps, step size.
[00:14:12:239 - 00:14:14:559] **Speaker 1:** Starting at 21.6.
[00:14:16:000 - 00:14:17:830] **Speaker 1:** And going up to 2000.
[00:14:20:429 - 00:14:25:820] **Speaker 1:** Um, OK, so I put you wrong.
[00:14:25:960 - 00:14:28:919] **Speaker 1:** These this is in reciprocal step size, so that's not.
[00:14:30:099 - 00:14:31:409] **Speaker 1:** 0.4 milliseconds.
[00:14:31:530 - 00:14:36:080] **Speaker 1:** This is 2000 seconds, so it does start small, but
[00:14:36:080 - 00:14:39:219] **Speaker 1:** it doesn't start small enough, so we're going to reduce
[00:14:39:270 - 00:14:40:059] **Speaker 1:** the tolerance.
[00:14:42:890 - 00:14:46:250] **Speaker 1:** Uh, maybe 1 E -5, for example.
[00:14:47:840 - 00:14:48:690] **Speaker 1:** And compete again.
[00:14:50:739 - 00:14:51:130] **Speaker 1:** OK.
[00:14:52:450 - 00:14:56:309] **Speaker 1:** So the initial step size is much smaller, 0.02 seconds.
[00:14:57:229 - 00:14:59:309] **Speaker 1:** Um, I don't know if you can read, you can
[00:14:59:309 - 00:14:59:969] **Speaker 1:** read that, yeah.
[00:15:00:859 - 00:15:05:179] **Speaker 1:** And continues on, so the output times are still recorded
[00:15:05:179 - 00:15:08:270] **Speaker 1:** as those that we specify back up here.
[00:15:08:659 - 00:15:10:940] **Speaker 1:** These aren't the time steps of the solver, these are
[00:15:10:940 - 00:15:12:780] **Speaker 1:** just the output times when we save.
[00:15:14:289 - 00:15:14:770] **Speaker 2:** All right.
[00:15:16:630 - 00:15:19:219] **Speaker 1:** So that's those time settings.
[00:15:19:700 - 00:15:20:640] **Speaker 1:** So we're still not great.
[00:15:22:469 - 00:15:24:450] **Speaker 1:** What we can do now is refine our mesh.
[00:15:28:700 - 00:15:31:229] **Speaker 1:** So 20 Elements.
[00:15:32:130 - 00:15:33:130] **Speaker 1:** And it's looking better.
[00:15:38:469 - 00:15:40:900] **Speaker 1:** And if we use a higher order element, it would
[00:15:40:900 - 00:15:41:849] **Speaker 1:** be better still.
[00:15:43:039 - 00:15:45:179] **Speaker 1:** So that is.
[00:15:45:969 - 00:15:47:729] **Speaker 1:** The first case using a ramp.
[00:15:48:729 - 00:15:50:520] **Speaker 1:** And reducing the tolerance.
[00:15:52:390 - 00:15:54:830] **Speaker 1:** The other example of the boundary condition that you can
[00:15:54:830 - 00:15:58:840] **Speaker 1:** use is that sort of pseudo flux source term.
[00:15:59:739 - 00:16:02:299] **Speaker 1:** When you're going to do your boundary conditions and your
[00:16:02:299 - 00:16:05:820] **Speaker 1:** uh chicken patty, uh, that link that I put on
[00:16:05:820 - 00:16:09:150] **Speaker 1:** that page, So this is one of the schemes that
[00:16:09:150 - 00:16:09:729] **Speaker 1:** you could use.
[00:16:11:859 - 00:16:31:359] **Speaker 1:** So we've got We'll get rid of this guy and
[00:16:31:359 - 00:16:32:609] **Speaker 1:** enable the fox.
[00:16:34:489 - 00:16:38:929] **Speaker 1:** So the equation here Is Greg.
[00:16:39:539 - 00:16:40:099] **Speaker 1:** Alpha.
[00:16:42:549 - 00:16:42:719] **Speaker 1:** Grab.
[00:16:46:119 - 00:16:48:780] **Speaker 1:** Equal to G minus QT.
[00:16:51:960 - 00:16:53:969] **Speaker 1:** So that's, it's pretty similar to what you're doing with
[00:16:53:969 - 00:16:57:169] **Speaker 1:** your heat, uh, your convective heat transfer.
[00:16:58:010 - 00:16:59:030] **Speaker 1:** You can rearrange that.
[00:16:59:489 - 00:17:05:300] **Speaker 1:** So this is matching the Diffusion within the domain with
[00:17:05:300 - 00:17:07:180] **Speaker 1:** some uh flux term on the right.
[00:17:09:287 - 00:17:11:269] **Speaker 1:** What we're gonna do is essentially make.
[00:17:12:188 - 00:17:14:380] **Speaker 1:** This term approximately equal to 0.
[00:17:15:069 - 00:17:18:390] **Speaker 1:** And set this value G equal to T over q.
[00:17:20:339 - 00:17:22:319] **Speaker 1:** So what I've said is G.
[00:17:25:589 - 00:17:36:579] **Speaker 1:** Equal to Tuned to the T Over And I've said
[00:17:36:579 - 00:17:36:979] **Speaker 1:** Q.
[00:17:37:869 - 00:17:40:099] **Speaker 1:** Equal to 108 over alpha.
[00:17:43:339 - 00:17:45:300] **Speaker 1:** So if we substitute that in and it's in 1D,
[00:17:45:380 - 00:17:48:640] **Speaker 1:** so we've just got um and uniform alpha, so alpha,
[00:17:48:859 - 00:17:54:729] **Speaker 1:** D 2 T D X 2 equal to, 108 over
[00:17:54:729 - 00:17:55:219] **Speaker 1:** alpha.
[00:17:56:319 - 00:17:59:290] **Speaker 2:** Uh, G Minus.
[00:18:00:030 - 00:18:05:250] **Speaker 1:** QT What is this doing?
[00:18:05:530 - 00:18:08:369] **Speaker 1:** So we've got Alpha.
[00:18:09:670 - 00:18:10:500] **Speaker 1:** Actually maybe.
[00:18:11:729 - 00:18:13:849] **Speaker 1:** There probably should be time's alpha, that would make more
[00:18:13:849 - 00:18:14:109] **Speaker 1:** sense.
[00:18:16:020 - 00:18:16:969] **Speaker 1:** That explains a lot.
[00:18:18:709 - 00:18:19:869] **Speaker 1:** To me, um.
[00:18:21:290 - 00:18:22:209] **Speaker 1:** With some scaling.
[00:18:22:489 - 00:18:26:089] **Speaker 1:** Alright, so we've got, if that was times alpha, we're
[00:18:26:089 - 00:18:27:250] **Speaker 1:** doing it live, so that's good.
[00:18:29:959 - 00:18:30:739] **Speaker 1:** And we cancel.
[00:18:31:819 - 00:18:36:329] **Speaker 1:** We Essentially making the gradient or that slope equal to
[00:18:36:329 - 00:18:36:910] **Speaker 1:** zero.
[00:18:48:589 - 00:18:51:109] **Speaker 1:** Or in fact, we don't care what value this holds
[00:18:51:109 - 00:18:54:060] **Speaker 1:** because a number divided by a big number is approaching
[00:18:54:060 - 00:18:54:510] **Speaker 1:** 0.
[00:18:55:329 - 00:18:58:569] **Speaker 1:** Which is essentially setting the temperature at the boundary equal
[00:18:58:569 - 00:18:59:930] **Speaker 1:** to the surrounding temperature to year.
[00:19:00:900 - 00:19:01:619] **Speaker 1:** The infinity.
[00:19:07:640 - 00:19:10:079] **Speaker 1:** Um, now that I've changed that, hopefully it still works,
[00:19:10:199 - 00:19:10:959] **Speaker 1:** but we'll find out.
[00:19:13:010 - 00:19:14:290] **Speaker 1:** Um, yeah.
[00:19:15:650 - 00:19:15:660] **Speaker 1:** Alright.
[00:19:19:170 - 00:19:20:560] **Speaker 1:** So I've achieved the same thing.
[00:19:21:719 - 00:19:27:689] **Speaker 1:** This initial Initial profile as set at T1.
[00:19:29:829 - 00:19:31:170] **Speaker 1:** And.
[00:19:32:239 - 00:19:35:699] **Speaker 1:** After that, it's tending to infinity.
[00:19:37:319 - 00:19:40:390] **Speaker 1:** So this might be quite helpful when you're swapping between
[00:19:40:390 - 00:19:43:040] **Speaker 1:** the robin and the direct boundary condition because then you
[00:19:43:040 - 00:19:46:719] **Speaker 1:** can apply like an if statement, if time is less
[00:19:46:719 - 00:19:49:239] **Speaker 1:** than some other time, T flip or something, um, then
[00:19:49:239 - 00:19:50:810] **Speaker 1:** it's going to do this or it does the other
[00:19:50:810 - 00:19:51:640] **Speaker 1:** boundary condition.
[00:19:53:560 - 00:19:56:479] **Speaker 1:** Uh, so that, that's just demonstrating what was in that
[00:19:56:479 - 00:19:58:660] **Speaker 1:** article on, on that console blog post.
[00:20:07:010 - 00:20:11:290] **Speaker 1:** And I think that just about does all the steps.
[00:20:11:709 - 00:20:13:119] **Speaker 1:** Uh, we can quantify the error.
[00:20:13:709 - 00:20:16:069] **Speaker 1:** So if we take the integral and do the difference
[00:20:16:069 - 00:20:18:229] **Speaker 1:** between the temperature field from the numerical model and the
[00:20:18:229 - 00:20:21:859] **Speaker 1:** analytical and scale, so it's a relative error, we can,
[00:20:22:010 - 00:20:22:949] **Speaker 1:** we can evaluate that.
[00:20:23:670 - 00:20:25:869] **Speaker 1:** And we can see that they are small numbers 10
[00:20:25:869 - 00:20:26:849] **Speaker 1:** to 12, so that's good.
[00:20:30:290 - 00:20:30:310] **Speaker 1:** All right.
[00:20:37:910 - 00:20:41:010] **Speaker 1:** Are there any questions on how I've done this?
[00:20:44:280 - 00:20:44:560] **Speaker 2:** No.
[00:20:45:839 - 00:20:46:160] **Speaker 2:** Yeah.
[00:20:47:630 - 00:20:51:349] **Speaker 0:** the still getting You deserve.
[00:20:53:479 - 00:20:56:569] **Speaker 3:** So that's, because, yeah, so when I first did it.
[00:21:03:719 - 00:21:05:239] **Speaker 1:** This is with the the ramp.
[00:21:07:160 - 00:21:11:569] **Speaker 1:** And I don't have that consistent initialization off.
[00:21:12:250 - 00:21:14:729] **Speaker 1:** It's going to do essentially like a small step to
[00:21:14:729 - 00:21:16:189] **Speaker 1:** try and figure out the initial value.
[00:21:18:819 - 00:21:22:189] **Speaker 1:** And the ramp is finite, so it will have some
[00:21:22:189 - 00:21:24:869] **Speaker 1:** temperature that changes over that first little time set.
[00:21:25:810 - 00:21:31:790] **Speaker 1:** So if we compute that, Oh, it's not really showing
[00:21:31:790 - 00:21:32:910] **Speaker 1:** what I wanted it, should I?
[00:21:34:000 - 00:21:34:449] **Speaker 1:** Oh, OK.
[00:21:34:660 - 00:21:36:569] **Speaker 1:** So quite small, but there is a little bit of
[00:21:36:569 - 00:21:38:050] **Speaker 1:** a um.
[00:21:40:420 - 00:21:42:609] **Speaker 1:** Difference in that initial.
[00:21:43:359 - 00:21:43:880] **Speaker 1:** Condition.
[00:21:46:579 - 00:21:49:880] **Speaker 1:** Yeah, turn off the um consistent initialization.
[00:21:50:579 - 00:21:56:579] **Speaker 1:** And the time dependence over Algebraic variable settings.
[00:21:58:459 - 00:22:02:500] **Speaker 1:** But again, this, it's quite a small impact, um, you
[00:22:02:500 - 00:22:05:319] **Speaker 1:** might not see a significant difference in the overall cooking
[00:22:05:319 - 00:22:06:660] **Speaker 1:** time and things like that, but.
[00:22:07:420 - 00:22:09:619] **Speaker 1:** For those who are very observant and want to get
[00:22:09:619 - 00:22:09:819] **Speaker 1:** it.
[00:22:10:910 - 00:22:11:339] **Speaker 1:** Super.
[00:22:12:560 - 00:22:14:640] **Speaker 1:** Accurate, um, there's, there's always a way.
[00:22:16:239 - 00:22:18:550] **Speaker 1:** But I've seen lots of different approaches through your console
[00:22:18:550 - 00:22:22:000] **Speaker 1:** models around the labs and in the mix suite, um,
[00:22:22:119 - 00:22:25:140] **Speaker 1:** so yeah, there's not one just correct way of approaching
[00:22:25:140 - 00:22:26:680] **Speaker 1:** this, this problem, which is.
[00:22:27:920 - 00:22:28:640] **Speaker 1:** Always good fun.
[00:22:30:750 - 00:22:32:859] **Speaker 1:** Any other questions on this or the assignment?
[00:22:36:050 - 00:22:38:689] **Speaker 0:** Yeah, if we, I mean, I could have done this
[00:22:38:689 - 00:22:41:339] **Speaker 3:** wrong, but when I all the heat fluxes.
[00:22:42:359 - 00:22:48:410] **Speaker 3:** From the A different kind of scale to the other.
[00:22:49:650 - 00:22:54:609] **Speaker 3:** Lose Yeah, so what would, yep.
[00:22:56:050 - 00:22:58:410] **Speaker 1:** Um, so if, I mean, do you expect it to
[00:22:58:410 - 00:23:00:650] **Speaker 1:** be a significantly different order of magnitude than the other
[00:23:00:650 - 00:23:01:229] **Speaker 1:** heat fluxes?
[00:23:02:650 - 00:23:04:489] **Speaker 1:** Yeah, I mean if you've got something like super hot
[00:23:04:489 - 00:23:07:250] **Speaker 1:** being put up against something that's cooler, quite a bit
[00:23:07:250 - 00:23:11:939] **Speaker 1:** cooler, um, and then the convective heat transfers is reasonably
[00:23:11:939 - 00:23:16:439] **Speaker 1:** low, um, and symmetry, you know what that should be.
[00:23:17:010 - 00:23:19:349] **Speaker 1:** So if you do have values that are quite different,
[00:23:19:609 - 00:23:22:619] **Speaker 1:** um, sometimes you can use like a log scale if,
[00:23:22:689 - 00:23:23:869] **Speaker 1:** if they're positive.
[00:23:24:250 - 00:23:27:189] **Speaker 1:** Um, or you could just scale it.
[00:23:27:369 - 00:23:31:819] **Speaker 1:** So if you had, um, It was a really large
[00:23:31:819 - 00:23:32:000] **Speaker 1:** number.
[00:23:33:290 - 00:23:36:609] **Speaker 1:** Then you would model it as like Q over a
[00:23:36:609 - 00:23:37:050] **Speaker 1:** value.
[00:23:37:979 - 00:23:42:339] **Speaker 1:** Um, So if it was on the order of 1000
[00:23:42:339 - 00:23:43:780] **Speaker 1:** and the other one's on the order of 1, you'd
[00:23:43:780 - 00:23:45:829] **Speaker 1:** just scale it by 1000 and then in the legend
[00:23:45:829 - 00:23:49:180] **Speaker 1:** you'd say it's q over 1000 rather than q at
[00:23:49:180 - 00:23:49:660] **Speaker 1:** the pan.
[00:23:50:400 - 00:23:53:369] **Speaker 1:** Uh, so that would be one way I guess another
[00:23:53:369 - 00:23:55:680] **Speaker 1:** way would be if you had like an insert.
[00:23:56:780 - 00:24:04:939] **Speaker 1:** So Although that's really only applicable for a small area,
[00:24:05:079 - 00:24:05:400] **Speaker 1:** but.
[00:24:06:780 - 00:24:08:079] **Speaker 1:** You could do like a blow up.
[00:24:10:540 - 00:24:11:310] **Speaker 1:** Of that region.
[00:24:11:430 - 00:24:14:839] **Speaker 1:** I don't know, it's maybe a different, different scenario, but
[00:24:19:680 - 00:24:22:040] **Speaker 1:** Yeah, that's how I, I, I, I would scale it.
[00:24:22:229 - 00:24:23:479] **Speaker 1:** That'd be easier than that, but.
[00:24:30:489 - 00:24:31:660] **Speaker 1:** And the other cruise.
[00:24:38:510 - 00:24:42:680] **Speaker 1:** And we can also Yeah, use different discretizations, so.
[00:24:43:880 - 00:24:46:079] **Speaker 1:** Linear quadratic cubit, etc.
[00:24:46:199 - 00:24:47:560] **Speaker 1:** to get different orders of accuracy.
[00:24:50:689 - 00:24:51:359] **Speaker 1:** All right.
[00:24:52:130 - 00:24:53:900] **Speaker 2:** Yeah, please.
[00:24:56:239 - 00:25:01:260] **Speaker 3:** Is what Showing Valley like tea coach.
[00:25:04:949 - 00:25:14:250] **Speaker 0:** that Um, So If we're looking at Checking whether or
[00:25:14:250 - 00:25:18:089] **Speaker 1:** not our discretization error is small, we want to check
[00:25:18:089 - 00:25:19:810] **Speaker 1:** across different mesh resolutions.
[00:25:20:660 - 00:25:23:939] **Speaker 1:** And a key parameter that we're analysing in this problem
[00:25:23:939 - 00:25:26:020] **Speaker 1:** is the minimum temperature over time, like figuring out when
[00:25:26:020 - 00:25:26:810] **Speaker 1:** is cooked.
[00:25:27:260 - 00:25:30:819] **Speaker 1:** So comparing meshes with that key parameter, such as Tieman
[00:25:30:819 - 00:25:32:829] **Speaker 1:** is good or maybe Ted.
[00:25:33:819 - 00:25:37:699] **Speaker 1:** It might be easier to create two plots, one that
[00:25:37:699 - 00:25:40:000] **Speaker 1:** has one for the mesh convergence and one for Tieman
[00:25:40:000 - 00:25:42:020] **Speaker 1:** over time, or you could plot all the different mesh
[00:25:42:020 - 00:25:43:479] **Speaker 1:** resolutions on the same plot.
[00:25:44:000 - 00:25:46:650] **Speaker 1:** They're probably just all on top of each other, in
[00:25:46:650 - 00:25:49:930] **Speaker 1:** which case maybe a um NZ figure would help to
[00:25:49:930 - 00:25:52:619] **Speaker 1:** sort of zoom in on that location and show that
[00:25:52:619 - 00:25:55:089] **Speaker 1:** they're not exactly the same but a little bit different
[00:25:55:089 - 00:25:55:849] **Speaker 1:** between each curve.
[00:26:02:260 - 00:26:02:270] **Speaker 1:** Yeah.
[00:26:06:339 - 00:26:15:180] **Speaker 0:** says that Calculated halfway points, are we basically averaging.
[00:26:17:140 - 00:26:30:880] **Speaker 4:** I 2 different points and dividing by 2 or?
[00:26:32:339 - 00:26:33:280] **Speaker 1:** That would be easiest.
[00:26:33:420 - 00:26:35:810] **Speaker 1:** Um, so kappa is varying as a function of temperature,
[00:26:35:890 - 00:26:36:780] **Speaker 1:** not just the position.
[00:26:37:619 - 00:26:40:369] **Speaker 1:** And you want to evaluate Keppa at that midway point,
[00:26:40:589 - 00:26:41:729] **Speaker 1:** so if I try and draw.
[00:26:54:550 - 00:26:58:719] **Speaker 1:** So if evaluating kappa at 1 + 5, it varies
[00:26:58:719 - 00:27:01:640] **Speaker 1:** with temperature and you're right, where do we calculate that
[00:27:01:640 - 00:27:03:719] **Speaker 1:** temperature because the nodes that we're evaluating in this finite
[00:27:03:719 - 00:27:05:599] **Speaker 1:** different scheme is at I and I + 1.
[00:27:06:329 - 00:27:14:349] **Speaker 1:** So you could evaluate it Um, plus, uh, Oh sorry.
[00:27:15:699 - 00:27:23:160] **Speaker 1:** Ever at Um, TI + 1 and TI over 2.
[00:27:23:640 - 00:27:26:819] **Speaker 1:** So that's a simple average of the two neighbouring temperatures.
[00:27:27:359 - 00:27:30:199] **Speaker 1:** So that will still essentially look at the variance or
[00:27:30:199 - 00:27:33:599] **Speaker 1:** the gradient of kappa between these two halfway points because
[00:27:33:599 - 00:27:35:040] **Speaker 1:** it's evaluating the temperature at the midpoint.
[00:27:35:280 - 00:27:37:359] **Speaker 1:** It's essentially doing a linear interpolation at the midpoint.
[00:27:37:560 - 00:27:39:839] **Speaker 1:** I've seen some people do this with a more complicated
[00:27:39:839 - 00:27:42:680] **Speaker 1:** equation, which was fun, um, but it is just the
[00:27:42:680 - 00:27:43:119] **Speaker 1:** average.
[00:27:44:449 - 00:27:45:410] **Speaker 1:** That'd be the simplest way.
[00:27:46:650 - 00:27:49:310] **Speaker 1:** Um, I think some people were looking at taking Kappa.
[00:27:51:810 - 00:27:58:770] **Speaker 1:** At TI + 1 and Kappa at TI and did
[00:27:58:770 - 00:27:59:050] **Speaker 1:** that.
[00:28:01:530 - 00:28:03:550] **Speaker 1:** The equation is nonlinear.
[00:28:04:500 - 00:28:05:199] **Speaker 1:** With temperature.
[00:28:05:300 - 00:28:06:900] **Speaker 1:** So they will give slightly different results.
[00:28:07:060 - 00:28:09:099] **Speaker 1:** I don't know how big a difference it's going to
[00:28:09:099 - 00:28:10:619] **Speaker 1:** make, um.
[00:28:11:880 - 00:28:13:380] **Speaker 1:** But that, that'd be another approach.
[00:28:18:410 - 00:28:18:760] **Speaker 1:** Cool.
[00:28:20:079 - 00:28:23:640] **Speaker 1:** I know one person submitted as of yesterday, so we
[00:28:23:640 - 00:28:25:239] **Speaker 1:** know, we know that's.
[00:28:28:250 - 00:28:29:849] **Speaker 1:** Give it a prize for submitting first or something, I
[00:28:29:849 - 00:28:31:209] **Speaker 1:** don't know, um.
[00:28:31:829 - 00:28:36:430] **Speaker 1:** So it wasn't an empty report, that's, it's important to
[00:28:36:430 - 00:28:36:650] **Speaker 1:** note.
[00:28:39:979 - 00:28:41:099] **Speaker 1:** No other queries.
[00:28:45:900 - 00:28:45:910] **Speaker 1:** Right.
[00:28:52:430 - 00:28:53:869] **Speaker 1:** I think that's everything.
[00:28:54:930 - 00:28:57:270] **Speaker 1:** All right, so we can get started on chapter 7.
[00:29:06:439 - 00:29:12:380] **Speaker 1:** So hyperbolic Wave equations Hypolic PDs.
[00:29:12:829 - 00:29:15:459] **Speaker 1:** So yeah, I guess you were lucky this year, um,
[00:29:15:880 - 00:29:18:329] **Speaker 1:** and last year they both looked at heat equations.
[00:29:18:719 - 00:29:20:800] **Speaker 1:** The year prior looked at the wave equation which was
[00:29:20:800 - 00:29:24:510] **Speaker 1:** really exciting because it's quite unstable, um, you get lots
[00:29:24:510 - 00:29:26:239] **Speaker 1:** of waves and if you don't have any damping it
[00:29:26:239 - 00:29:29:119] **Speaker 1:** just continues on forever, which is quite challenging to model
[00:29:29:119 - 00:29:29:780] **Speaker 1:** numerically.
[00:29:30:319 - 00:29:31:459] **Speaker 1:** So having a stable solution.
[00:29:33:979 - 00:29:36:609] **Speaker 1:** So we're gonna go through and derive the wave equation,
[00:29:36:709 - 00:29:39:420] **Speaker 1:** and then we're gonna use the analytical method, uh, separation
[00:29:39:420 - 00:29:42:729] **Speaker 1:** of variables and the numerical scheme, uh, for solving these
[00:29:42:729 - 00:29:43:489] **Speaker 1:** equations.
[00:29:45:359 - 00:29:46:839] **Speaker 1:** So we, we often see them.
[00:29:47:619 - 00:29:48:540] **Speaker 1:** I don't know if we want to model like a
[00:29:48:540 - 00:29:51:900] **Speaker 1:** string or a guitar, a violin string, maybe waves in
[00:29:51:900 - 00:29:53:939] **Speaker 1:** the ocean, so I showed in that first lecture about
[00:29:53:939 - 00:29:57:660] **Speaker 1:** the tsunami modelling, um, using the shallow water equations which
[00:29:57:660 - 00:30:00:449] **Speaker 1:** are sort of these hyperbolic PDEs.
[00:30:01:079 - 00:30:04:250] **Speaker 1:** So I applied to lots of different um domains.
[00:30:05:910 - 00:30:08:619] **Speaker 1:** We're going to derive one that governs the motion of
[00:30:08:619 - 00:30:09:829] **Speaker 1:** a vibrating string.
[00:30:11:069 - 00:30:12:390] **Speaker 1:** So one like on a violin.
[00:30:13:449 - 00:30:14:859] **Speaker 1:** So if we, we think about.
[00:30:17:099 - 00:30:19:400] **Speaker 1:** What our string looks like in math space.
[00:30:20:589 - 00:30:28:010] **Speaker 1:** Um We want to Describe the length and X coordinate.
[00:30:28:900 - 00:30:35:270] **Speaker 1:** And the deflection, the vertical deflection with You Of X
[00:30:35:270 - 00:30:35:640] **Speaker 1:** and T.
[00:30:39:910 - 00:30:42:420] **Speaker 1:** And maybe it's just a sign profile.
[00:30:43:189 - 00:30:44:010] **Speaker 1:** Was Puebla.
[00:30:56:010 - 00:30:58:069] **Speaker 1:** And we're going to analyse.
[00:30:59:000 - 00:31:00:000] **Speaker 2:** Using Newton's law.
[00:31:01:650 - 00:31:03:959] **Speaker 1:** So we're gonna look at the impact of the tension,
[00:31:04:040 - 00:31:07:060] **Speaker 1:** the force being applied on an element between X.
[00:31:08:030 - 00:31:10:069] **Speaker 1:** And some distance away at delta X.
[00:31:18:270 - 00:31:20:150] **Speaker 1:** And it might make sense to call it X0.
[00:31:22:810 - 00:31:24:209] **Speaker 1:** So we don't have two X's.
[00:31:38:489 - 00:31:41:729] **Speaker 1:** So we've got a tension force that's being applied along
[00:31:41:729 - 00:31:42:209] **Speaker 1:** the string.
[00:31:43:579 - 00:31:46:020] **Speaker 1:** And it's going to be tangential to the curve of
[00:31:46:020 - 00:31:49:579] **Speaker 1:** the string, so it varies direction, but the magnitude is
[00:31:49:579 - 00:31:50:660] **Speaker 1:** the same throughout the string.
[00:31:51:989 - 00:31:54:390] **Speaker 1:** So the element of the string has no net motion.
[00:31:55:650 - 00:31:58:939] **Speaker 1:** And so the forces projecting on the X plane or
[00:31:58:939 - 00:32:00:199] **Speaker 1:** X axis has to balance.
[00:32:01:339 - 00:32:03:760] **Speaker 1:** So first we'll draw what these tension forces are.
[00:32:07:770 - 00:32:09:400] **Speaker 1:** So we've got T1.
[00:32:13:099 - 00:32:14:640] **Speaker 1:** At an angle alpha.
[00:32:19:000 - 00:32:21:599] **Speaker 1:** And we have another tension.
[00:32:24:910 - 00:32:25:500] **Speaker 1:** D2.
[00:32:28:180 - 00:32:29:359] **Speaker 1:** At an angle of.
[00:32:30:170 - 00:32:31:959] **Speaker 1:** Data from the horizontal.
[00:32:38:829 - 00:32:41:630] **Speaker 1:** And we can think back either to high school or
[00:32:41:630 - 00:32:45:939] **Speaker 1:** 1st year, we did those free body diagrams, decompose it
[00:32:45:939 - 00:32:47:510] **Speaker 1:** into the X and Y components.
[00:32:48:229 - 00:32:49:520] **Speaker 1:** So we've got D1.
[00:32:51:729 - 00:32:53:619] **Speaker 1:** And we're gonna use different colours.
[00:32:55:310 - 00:32:56:069] **Speaker 1:** If you want.
[00:33:03:709 - 00:33:07:469] **Speaker 1:** We've got T1 cos alpha.
[00:33:12:160 - 00:33:15:660] **Speaker 1:** And the vertical component is T1.
[00:33:19:250 - 00:33:21:189] **Speaker 1:** Do you want sign alpha?
[00:33:22:420 - 00:33:27:030] **Speaker 1:** And for the Second term at XN plus data we
[00:33:27:030 - 00:33:27:729] **Speaker 1:** have.
[00:33:32:219 - 00:33:32:619] **Speaker 0:** T2.
[00:33:39:420 - 00:33:44:780] **Speaker 1:** And D2 cos beta.
[00:33:49:010 - 00:33:50:050] **Speaker 1:** And tea tree.
[00:33:53:209 - 00:33:53:619] **Speaker 1:** Fine.
[00:33:54:599 - 00:33:54:890] **Speaker 1:** I know.
[00:33:59:300 - 00:34:07:130] **Speaker 1:** So And X, the string or violin string isn't moving,
[00:34:07:369 - 00:34:10:570] **Speaker 1:** so F equals MA F has to equal 0, the
[00:34:10:570 - 00:34:11:570] **Speaker 1:** sum of forces.
[00:34:12:719 - 00:34:17:989] **Speaker 1:** So we have T1, Cause alpha.
[00:34:19:229 - 00:34:23:898] **Speaker 1:** Being the component and the, Negative direction has to equal
[00:34:24:040 - 00:34:24:560] **Speaker 1:** the 1.
[00:34:25:388 - 00:34:28:459] **Speaker 1:** At T2 cause better.
[00:34:39:759 - 00:34:42:839] **Speaker 1:** So if this is true throughout the the string and
[00:34:42:839 - 00:34:45:989] **Speaker 1:** throughout time, there has to be maybe some value T,
[00:34:46:559 - 00:34:47:438] **Speaker 1:** which is a constant.
[00:35:19:800 - 00:35:21:719] **Speaker 1:** Who All right.
[00:35:23:409 - 00:35:23:820] **Speaker 1:** everyone's written.
[00:35:23:979 - 00:35:26:419] **Speaker 1:** So next step is we're gonna look at the force
[00:35:26:419 - 00:35:27:790] **Speaker 1:** balance and the vertical direction.
[00:35:27:899 - 00:35:30:979] **Speaker 1:** We've got T1 sin alpha and T2 sin beta.
[00:35:36:959 - 00:35:40:540] **Speaker 0:** So D To sign.
[00:35:41:530 - 00:35:46:409] **Speaker 1:** Ada Minus T1 sin alpha.
[00:35:47:879 - 00:35:50:439] **Speaker 1:** is equal to mass times acceleration.
[00:35:50:719 - 00:35:52:379] **Speaker 1:** So equal to M.
[00:35:53:729 - 00:35:56:689] **Speaker 1:** And instead of A for acceleration, we're going to denote
[00:35:56:689 - 00:35:59:409] **Speaker 1:** it by the 2nd derivative of the displacement.
[00:35:59:639 - 00:36:00:370] **Speaker 1:** So D2.
[00:36:02:610 - 00:36:05:550] **Speaker 1:** UIDT square.
[00:36:07:209 - 00:36:09:510] **Speaker 1:** And again, we know that the displacement of the string
[00:36:09:510 - 00:36:11:250] **Speaker 1:** is varying in space and time, so it's a partial
[00:36:11:250 - 00:36:13:689] **Speaker 1:** derivative D2 U by DT2.
[00:36:16:469 - 00:36:18:659] **Speaker 1:** And the mass of the string.
[00:36:19:409 - 00:36:23:010] **Speaker 1:** Is given by the density of the string multiplied by
[00:36:23:010 - 00:36:24:459] **Speaker 1:** that length delta X.
[00:36:42:489 - 00:36:44:129] **Speaker 1:** So what we just said before was that we had
[00:36:44:129 - 00:36:47:409] **Speaker 1:** these two values, T2 cos beta and T1, cos alpha
[00:36:47:610 - 00:36:49:770] **Speaker 1:** are both equal to the same value T.
[00:36:51:010 - 00:36:53:449] **Speaker 1:** So what we're gonna do here is divide through by
[00:36:53:449 - 00:36:53:649] **Speaker 1:** T.
[00:37:06:219 - 00:37:08:629] **Speaker 1:** And we've got T2.
[00:37:09:669 - 00:37:10:570] **Speaker 1:** Sign.
[00:37:11:070 - 00:37:11:469] **Speaker 1:** later.
[00:37:12:879 - 00:37:16:719] **Speaker 1:** Divided by T and we're going to choose T2 cos
[00:37:16:719 - 00:37:18:459] **Speaker 1:** beta to have the same angles.
[00:37:22:340 - 00:37:26:149] **Speaker 1:** And we've got minus T1 sin alpha, and we're gonna
[00:37:26:149 - 00:37:28:070] **Speaker 1:** choose T1 cos alpha.
[00:37:33:679 - 00:37:37:800] **Speaker 1:** So we recall sin beta over cos beta is equal
[00:37:37:800 - 00:37:38:399] **Speaker 1:** to 10.
[00:37:40:320 - 00:37:40:800] **Speaker 1:** Yeah.
[00:37:42:979 - 00:37:45:340] **Speaker 1:** -10 alpha.
[00:37:46:810 - 00:37:50:090] **Speaker 1:** Equal to Row delta X.
[00:37:51:040 - 00:37:51:770] **Speaker 1:** Over T.
[00:37:53:780 - 00:37:57:179] **Speaker 1:** D2 U by DT2.
[00:38:04:860 - 00:38:07:239] **Speaker 1:** So from rig, we recall it like 10 alpha.
[00:38:08:000 - 00:38:11:580] **Speaker 1:** Is like opposite over adjacent, so that's essentially D by
[00:38:11:580 - 00:38:15:719] **Speaker 1:** Dx evaluated X and tan beta is the gradient or
[00:38:15:719 - 00:38:18:620] **Speaker 1:** derivative of our displacement at x + x.
[00:38:19:699 - 00:38:21:719] **Speaker 1:** So we substitute in these 22 expressions.
[00:38:22:429 - 00:38:26:959] **Speaker 2:** And we're left with One over Derick's.
[00:38:28:780 - 00:38:30:399] **Speaker 1:** We're shifting data directs on the other side.
[00:38:31:459 - 00:38:36:209] **Speaker 1:** And Tan beta Goes to DU by DXZX plus data
[00:38:36:209 - 00:38:36:669] **Speaker 1:** x.
[00:38:42:399 - 00:38:48:850] **Speaker 1:** And 10 alpha, DU by DX at X.
[00:38:57:949 - 00:39:01:830] **Speaker 1:** So this looks a little bit familiar, um, starting to
[00:39:01:830 - 00:39:05:189] **Speaker 1:** look like a central difference or maybe a second order
[00:39:05:189 - 00:39:05:929] **Speaker 1:** derivative.
[00:39:06:790 - 00:39:09:830] **Speaker 1:** So if we reduce our x towards zero, this is
[00:39:09:830 - 00:39:12:810] **Speaker 1:** essentially the 2nd order derivative in space.
[00:39:14:050 - 00:39:17:290] **Speaker 1:** And we're going to introduce a new variable C2, and
[00:39:17:290 - 00:39:18:649] **Speaker 1:** that's equal to T over pro.
[00:39:19:810 - 00:39:22:030] **Speaker 1:** So finally, we have D2U by DT2.
[00:39:24:629 - 00:39:29:550] **Speaker 1:** Equal to C2 D2U by DX2.
[00:39:34:760 - 00:39:38:250] **Speaker 1:** So this we've arrived at the one dimensional wave equation.
[00:39:39:090 - 00:39:41:169] **Speaker 1:** And this is going to govern the displacement of that
[00:39:41:169 - 00:39:42:310] **Speaker 1:** string over time.
[00:39:43:290 - 00:39:46:600] **Speaker 1:** There's no damping here, so it just would defect on
[00:39:46:600 - 00:39:47:530] **Speaker 1:** to infernity.
[00:39:48:250 - 00:39:52:429] **Speaker 1:** There's nothing, nothing stopping it from continuing on to infinity,
[00:39:52:750 - 00:39:56:229] **Speaker 1:** and if we analyse this equation using that B2 minus
[00:39:56:229 - 00:39:59:929] **Speaker 1:** 40C, we've got a hyperbolic type.
[00:40:03:830 - 00:40:05:810] **Speaker 1:** So this is a 2nd order.
[00:40:06:919 - 00:40:11:469] **Speaker 1:** PDE in space and a 2nd order PDE in time.
[00:40:12:919 - 00:40:15:560] **Speaker 1:** This means that we have 2 boundary conditions.
[00:40:16:830 - 00:40:20:709] **Speaker 1:** And to initial conditions that uniquely identify this problem.
[00:40:20:949 - 00:40:23:290] **Speaker 1:** So, so we don't have an ill-posed.
[00:40:24:330 - 00:40:28:540] **Speaker 1:** Definition of So typically we're gonna have maybe fixed ends,
[00:40:28:659 - 00:40:29:719] **Speaker 1:** so displacements.
[00:40:30:550 - 00:40:33:110] **Speaker 1:** At X equals 0 and X equal to L, and
[00:40:33:110 - 00:40:34:560] **Speaker 1:** we'll have an initial profile.
[00:40:34:719 - 00:40:37:239] **Speaker 1:** There might be some function, maybe it's a sine wave,
[00:40:37:320 - 00:40:39:639] **Speaker 1:** something else, and we have an initial velocity.
[00:40:39:800 - 00:40:42:350] **Speaker 1:** So not only the initial displacement, but the initial velocity
[00:40:42:350 - 00:40:42:719] **Speaker 1:** as well.
[00:40:43:669 - 00:40:44:909] **Speaker 1:** So we're labelling these FNG.
[00:40:47:040 - 00:40:49:139] **Speaker 1:** Alright, so we've defined our mathematical model.
[00:40:49:770 - 00:40:51:629] **Speaker 1:** Now we want to solve it.
[00:40:52:120 - 00:40:53:449] **Speaker 1:** So we want to solve it with the method of
[00:40:53:449 - 00:40:56:090] **Speaker 1:** separation variables as we've done earlier, and we're gonna use
[00:40:56:090 - 00:40:57:250] **Speaker 1:** finite differencing as well.
[00:41:00:699 - 00:41:01:290] **Speaker 1:** Good fun.
[00:41:01:739 - 00:41:03:899] **Speaker 1:** So just like we did for our parabolic PDE, we're
[00:41:03:899 - 00:41:06:149] **Speaker 1:** going to assume that the displacement.
[00:41:08:310 - 00:41:10:389] **Speaker 1:** Varying in space and time X and D is going
[00:41:10:389 - 00:41:13:649] **Speaker 1:** to be a function that only varies in space X
[00:41:13:649 - 00:41:15:989] **Speaker 1:** and another function that only varies in time.
[00:41:20:139 - 00:41:22:979] **Speaker 1:** So we're going to substitute in this assumed form of
[00:41:22:979 - 00:41:27:379] **Speaker 1:** our solution, FG into our wave equation 5.
[00:41:33:459 - 00:41:36:770] **Speaker 1:** The first order of derivative in time, DYDT is going
[00:41:36:770 - 00:41:39:669] **Speaker 1:** to be Constant for F.
[00:41:41:100 - 00:41:46:580] **Speaker 1:** And we've got DGI DT4 derivatives because G is only
[00:41:46:580 - 00:41:47:540] **Speaker 1:** a function of T.
[00:41:48:060 - 00:41:53:610] **Speaker 1:** and the second Order derivative D2U by DT2.
[00:41:54:760 - 00:41:55:409] **Speaker 1:** Equal to F.
[00:41:56:219 - 00:42:00:010] **Speaker 1:** D 2 G Y D D 2.
[00:42:03:320 - 00:42:06:020] **Speaker 1:** Do the same for in spaced by DX and substitute
[00:42:06:020 - 00:42:08:379] **Speaker 1:** into our wave equation and we've got this final.
[00:42:09:469 - 00:42:15:770] **Speaker 1:** Boom So We want to separate the variables, as the
[00:42:15:770 - 00:42:17:330] **Speaker 1:** name implies, so we want to put all the F's
[00:42:17:330 - 00:42:18:649] **Speaker 1:** on one side, all the G's on the other.
[00:42:19:330 - 00:42:22:290] **Speaker 1:** So what we're gonna do is divide by C2FG.
[00:42:25:330 - 00:42:26:649] **Speaker 1:** And we're left with.
[00:42:29:250 - 00:42:30:879] **Speaker 1:** Um, equation 7.
[00:42:31:260 - 00:42:33:260] **Speaker 1:** So we've only got G terms on the left, so
[00:42:33:260 - 00:42:35:219] **Speaker 1:** only a function of time, and then we've got a,
[00:42:35:419 - 00:42:37:600] **Speaker 1:** uh, an expression that only varies in space.
[00:42:37:860 - 00:42:39:409] **Speaker 1:** And for that to be true for all space and
[00:42:39:409 - 00:42:41:219] **Speaker 1:** time, it needs to be equal to a constant.
[00:42:41:379 - 00:42:42:899] **Speaker 1:** So I've labelled that constant alpha.
[00:42:45:879 - 00:42:48:129] **Speaker 1:** Now solving this, uh, we end up with a couple
[00:42:48:129 - 00:42:48:969] **Speaker 1:** of ODEs.
[00:42:51:370 - 00:43:01:360] **Speaker 1:** So If Alpha is less than 0, we have these
[00:43:01:360 - 00:43:04:120] **Speaker 1:** 2 ODEs and if it's greater than 0, we have
[00:43:04:120 - 00:43:07:899] **Speaker 1:** another couple of ODEs and our general solutions are 8
[00:43:07:899 - 00:43:08:639] **Speaker 1:** and 9.
[00:43:09:989 - 00:43:12:830] **Speaker 1:** So as usual, we're going to figure out these constants
[00:43:12:830 - 00:43:15:229] **Speaker 1:** A, B, C, and D by applying the boundary, the
[00:43:15:229 - 00:43:17:330] **Speaker 1:** two boundary and the two initial conditions.
[00:43:18:590 - 00:43:21:649] **Speaker 1:** So case one is usually a bit more practical.
[00:43:22:939 - 00:43:24:770] **Speaker 1:** So generally going to be using that, but I think
[00:43:24:770 - 00:43:25:439] **Speaker 1:** I provide.
[00:43:26:520 - 00:43:29:040] **Speaker 1:** All of them in the formula sheet.
[00:43:32:040 - 00:43:33:300] **Speaker 1:** Too many pieces of paper.
[00:43:38:929 - 00:43:39:770] **Speaker 1:** Wave equation yep.
[00:43:41:850 - 00:43:48:550] **Speaker 1:** And If we can describe the initial conditions, so FXX
[00:43:48:790 - 00:43:53:169] **Speaker 1:** with a Fourier series, then we can, yeah, use equation
[00:43:53:169 - 00:43:55:989] **Speaker 1:** A to progress the solution forward in time.
[00:43:56:699 - 00:43:59:189] **Speaker 1:** So that's the sin of x terms that we can
[00:43:59:189 - 00:43:59:449] **Speaker 1:** use.
[00:44:00:699 - 00:44:01:879] **Speaker 2:** So we'll go through an example.
[00:44:03:739 - 00:44:09:580] **Speaker 1:** Um We got 5 minutes.
[00:44:09:979 - 00:44:11:379] **Speaker 1:** 5 minutes is enough, I think.
[00:44:12:370 - 00:44:14:370] **Speaker 1:** Cause we're not, I don't think we're writing, so that's.
[00:44:15:780 - 00:44:18:719] **Speaker 1:** That's good in some respects, but you might zone out.
[00:44:19:219 - 00:44:21:260] **Speaker 1:** So I've got um solving this wave equation.
[00:44:22:070 - 00:44:23:959] **Speaker 1:** And we derived it just before.
[00:44:24:209 - 00:44:26:780] **Speaker 1:** So we're looking at the vibrating um of a string
[00:44:27:260 - 00:44:28:239] **Speaker 1:** stretched between two points.
[00:44:28:280 - 00:44:30:439] **Speaker 1:** We've got zero displacement on the ends.
[00:44:30:560 - 00:44:32:659] **Speaker 1:** So 0, U equals 0 on left and right.
[00:44:33:649 - 00:44:36:330] **Speaker 1:** And we've got an initial velocity of 0, so it's
[00:44:36:409 - 00:44:39:570] **Speaker 1:** from the standing start, and it's got this triangular.
[00:44:40:879 - 00:44:43:040] **Speaker 1:** Piecewise linear and profile.
[00:44:43:840 - 00:44:47:010] **Speaker 1:** So we've applied this separation of variables we're using you
[00:44:47:010 - 00:44:52:810] **Speaker 1:** of XT with cosinet sint cos x sin x.
[00:44:53:679 - 00:44:56:659] **Speaker 1:** Applying the boundary condition on the left requires that C
[00:44:56:659 - 00:45:00:850] **Speaker 1:** is 0, on the right requires lambda is ML going
[00:45:00:850 - 00:45:01:989] **Speaker 1:** through A and B.
[00:45:02:570 - 00:45:05:290] **Speaker 1:** Applying the initial condition D by DT at T equal
[00:45:05:290 - 00:45:05:889] **Speaker 1:** to 0.
[00:45:06:250 - 00:45:11:419] **Speaker 1:** So we need to differentiate our solution and evaluate at
[00:45:11:419 - 00:45:12:129] **Speaker 1:** T equals 0.
[00:45:13:030 - 00:45:15:110] **Speaker 1:** And we see that B is 0.
[00:45:15:469 - 00:45:17:270] **Speaker 1:** So now we've got a particular solution that still has
[00:45:17:270 - 00:45:20:149] **Speaker 1:** an infinite number of solutions for UN.
[00:45:21:100 - 00:45:24:020] **Speaker 1:** In is any value 123 on.
[00:45:28:189 - 00:45:31:550] **Speaker 1:** So now we need to choose a combination of all
[00:45:31:550 - 00:45:35:010] **Speaker 1:** of these values that are going to match our natural
[00:45:35:010 - 00:45:36:270] **Speaker 1:** condition F of X.
[00:45:37:340 - 00:45:40:040] **Speaker 1:** So our initial profile, if we use 48 sign series.
[00:45:42:010 - 00:45:43:969] **Speaker 1:** And I've given that on the form sheet too.
[00:45:46:659 - 00:45:47:219] **Speaker 1:** This guy.
[00:45:49:560 - 00:45:54:679] **Speaker 1:** And we can express the initial condition with the site
[00:45:54:679 - 00:45:55:520] **Speaker 1:** for your sin series.
[00:45:56:629 - 00:46:00:129] **Speaker 1:** Combining for our initial condition, we evaluate T 0.
[00:46:01:139 - 00:46:03:620] **Speaker 1:** And we evaluate A N and then this is our
[00:46:03:620 - 00:46:05:020] **Speaker 1:** final solution.
[00:46:05:879 - 00:46:08:360] **Speaker 1:** So, I only took a minute or two, but when
[00:46:08:360 - 00:46:09:919] **Speaker 1:** you go through it obviously it might take 5 or
[00:46:09:919 - 00:46:11:560] **Speaker 1:** 10 minutes to, to work through.
[00:46:12:939 - 00:46:16:000] **Speaker 1:** Any questions on The wave equation.
[00:46:18:120 - 00:46:20:300] **Speaker 1:** I don't really want to get started on the numerical
[00:46:21:280 - 00:46:21:780] **Speaker 1:** steps.
[00:46:23:669 - 00:46:24:669] **Speaker 1:** I'll do that tomorrow.
[00:46:26:379 - 00:46:29:780] **Speaker 1:** Any questions on how we derived the wave equation or
[00:46:29:780 - 00:46:31:469] **Speaker 1:** any other questions for the course?
[00:46:34:300 - 00:46:37:639] **Speaker 1:** No, alright, um, cool, so we'll see you tomorrow.
[00:46:38:100 - 00:46:40:219] **Speaker 1:** Um, again, we don't have any like console lab or
[00:46:40:219 - 00:46:42:939] **Speaker 1:** quiz this week, so just ask questions for the assignment.
[00:46:42:979 - 00:46:45:169] **Speaker 1:** If you're stuck today, just work through some other parts
[00:46:45:169 - 00:46:47:659] **Speaker 1:** of the assignment and bring all your questions tomorrow so
[00:46:47:659 - 00:46:51:020] **Speaker 1:** we don't stand around bored, um, and we'll, we'll see
[00:46:51:020 - 00:46:51:439] **Speaker 1:** you then.
[00:47:25:969 - 00:47:41:300] **Speaker 0:** Thanks I just get a quick clarification on what you
[00:47:41:300 - 00:47:44:300] **Speaker 0:** said about that craft board thing, um, because I was
[00:47:44:300 - 00:47:46:260] **Speaker 4:** doing it this morning and you said we don't have
[00:47:46:260 - 00:47:46:860] **Speaker 0:** to do the.
[00:47:47:139 - 00:47:51:030] **Speaker 2:** No, that wasn't my intention just through one side using
[00:47:51:030 - 00:47:54:219] **Speaker 4:** the modelling with the pan in the, OK, because I
[00:47:54:219 - 00:47:55:580] **Speaker 4:** tried to I think it was a bit hard and
[00:47:55:580 - 00:47:58:020] **Speaker 4:** I was like, I'm so confused.
[00:47:58:360 - 00:48:01:780] **Speaker 0:** Yeah, OK, yeah, just trying to, I mean, the only
[00:48:01:780 - 00:48:07:360] **Speaker 1:** difference I wanted was to have the ears, the pan
[00:48:07:360 - 00:48:07:419] **Speaker 1:** and the ear, yes.
[00:48:08:030 - 00:48:12:750] **Speaker 1:** Um, the flipping, I think it's a bit more, um,
[00:48:12:909 - 00:48:14:820] **Speaker 1:** it's a bit more involved to do for that, so
[00:48:14:949 - 00:48:15:820] **Speaker 1:** that wasn't my intention.
[00:48:17:229 - 00:48:19:429] **Speaker 5:** So I was, I didn't quite catch, but with the
[00:48:19:429 - 00:48:21:510] **Speaker 5:** flipping part, so you're saying we don't have, not for
[00:48:21:510 - 00:48:25:159] **Speaker 5:** part four, no, but for part three we should still
[00:48:25:159 - 00:48:29:429] **Speaker 5:** implement the flipping in the console and, um, with that
[00:48:29:429 - 00:48:30:080] **Speaker 5:** flipping.
[00:48:30:659 - 00:48:34:169] **Speaker 5:** Do we want it to where when it's finished everything
[00:48:34:169 - 00:48:37:449] **Speaker 5:** in the patty should be 80 degrees, or at some
[00:48:37:449 - 00:48:40:300] **Speaker 5:** point every point should have been 80 degrees?
[00:48:40:620 - 00:48:41:419] **Speaker 6:** This is a similar question.
[00:48:41:770 - 00:48:43:770] **Speaker 6:** I have it where it cools down and then goes
[00:48:43:770 - 00:48:46:169] **Speaker 6:** back up, but it's the first time that the minimum
[00:48:46:169 - 00:48:49:229] **Speaker 5:** because it's technically cooked after reaching 80 the first time.
[00:48:51:600 - 00:48:54:850] **Speaker 5:** Because it's, I mean, you want the minimum temperature within
[00:48:54:850 - 00:48:57:879] **Speaker 1:** the patty to reach the safe temperature to 80.
[00:48:58:169 - 00:48:59:989] **Speaker 5:** Yes, but like if you have it on one side
[00:48:59:989 - 00:49:03:010] **Speaker 5:** and then it heats up to like some portion of
[00:49:03:010 - 00:49:05:800] **Speaker 5:** the patty to 80 and then you flip it over
[00:49:05:800 - 00:49:10:290] **Speaker 5:** again, like it's the location of the minimum temperature might
[00:49:10:290 - 00:49:10:709] **Speaker 5:** change.
[00:49:11:629 - 00:49:14:250] **Speaker 5:** Yeah, but I guess what we're saying is for the
[00:49:14:250 - 00:49:15:250] **Speaker 5:** patty to be cooked, it has to.
[00:49:15:405 - 00:49:16:215] **Speaker 5:** Reached 80 degrees.
[00:49:16:695 - 00:49:19:125] **Speaker 5:** Like when you're cooking something normally, right, it has to
[00:49:19:125 - 00:49:22:215] **Speaker 5:** have reached some certain temperature, let's say, for it to
[00:49:22:215 - 00:49:23:094] **Speaker 5:** be cooked, right?
[00:49:23:405 - 00:49:25:915] **Speaker 5:** And then when it's on that one side, are we,
[00:49:26:455 - 00:49:29:554] **Speaker 5:** because you're trying to find the ideal like time to
[00:49:29:554 - 00:49:31:945] **Speaker 5:** flip that it cooks quickly, cooks quickly, right?
[00:49:32:074 - 00:49:34:114] **Speaker 5:** It was like a low time to flip, but then
[00:49:34:114 - 00:49:37:495] **Speaker 6:** if I left it too long, it then had like
[00:49:37:495 - 00:49:40:814] **Speaker 6:** a much longer time because the other side would cool
[00:49:40:814 - 00:49:41:715] **Speaker 5:** down as well.
[00:49:45:320 - 00:49:47:399] **Speaker 5:** So it's like, do you want it to where that
[00:49:47:399 - 00:49:50:879] **Speaker 5:** you flip it and then you still want at whatever
[00:49:50:879 - 00:49:54:000] **Speaker 5:** time the minimum temperature to be 80 through the whole
[00:49:54:000 - 00:49:56:040] **Speaker 5:** patty, or is it like it's the most consistent?
[00:49:56:520 - 00:49:59:399] **Speaker 1:** It's just, we just want the team and we want
[00:49:59:399 - 00:50:01:679] **Speaker 1:** the minimum temperature to reach the safe temperature.
[00:50:02:120 - 00:50:06:290] **Speaker 5:** That's it, yeah, not necessarily because, yeah, the only thing
[00:50:06:290 - 00:50:08:540] **Speaker 5:** that you might run into is that it cools down,
[00:50:09:000 - 00:50:11:949] **Speaker 5:** like the other side will cool down after having reached
[00:50:11:949 - 00:50:12:580] **Speaker 5:** 80.
[00:50:13:620 - 00:50:15:459] **Speaker 5:** And then it's like the minimum temperature through the whole
[00:50:15:459 - 00:50:17:820] **Speaker 5:** patty now is less than 80, but that side had
[00:50:17:820 - 00:50:20:169] **Speaker 5:** already reached the cook temperature hard to keep track of,
[00:50:20:179 - 00:50:20:570] **Speaker 5:** isn't it?
[00:50:20:739 - 00:50:22:820] **Speaker 1:** Yeah, well, that's, that's why I, no, I just, just
[00:50:22:820 - 00:50:24:600] **Speaker 1:** teaming over time.
[00:50:24:860 - 00:50:26:679] **Speaker 1:** OK, that's my intention.
[00:50:27:780 - 00:50:29:729] **Speaker 1:** So how, how did you model it then?
[00:50:29:879 - 00:50:33:100] **Speaker 1:** Did you keep track of it with a different, I
[00:50:33:100 - 00:50:33:330] **Speaker 5:** didn't.
[00:50:33:419 - 00:50:35:540] **Speaker 5:** I was like, this seems really crazy.
[00:50:36:340 - 00:50:37:020] **Speaker 1:** Yeah that wasn't my intention.
[00:50:37:090 - 00:50:39:419] **Speaker 1:** It was just teaming, OK, over time.
[00:50:40:489 - 00:50:41:929] **Speaker 1:** I have one other question.
[00:50:42:169 - 00:50:43:810] **Speaker 6:** This part three, as soon as you make it a
[00:50:43:810 - 00:50:46:110] **Speaker 6:** 3D model, will it?
[00:50:46:370 - 00:50:47:419] **Speaker 6:** I can't get it.
[00:50:49:620 - 00:50:53:409] **Speaker 6:** Oh, maybe, maybe it's part two, but it's the, I
[00:50:53:409 - 00:50:56:449] **Speaker 6:** can't get it to reach 80 degrees, and that's what
[00:50:56:449 - 00:50:57:239] **Speaker 1:** you can report on.
[00:50:57:530 - 00:50:59:300] **Speaker 6:** That's what it's supposed to be because it's like the
[00:50:59:300 - 00:51:02:590] **Speaker 6:** conviction, the steady state is only like 70 or so.
[00:51:03:280 - 00:51:05:679] **Speaker 1:** Yeah, because I mean you've got more surface area that's
[00:51:05:679 - 00:51:07:479] **Speaker 1:** cooling from the convective heat transfer.
[00:51:07:989 - 00:51:08:489] **Speaker 6:** Yeah, OK, awesome.
[00:51:08:500 - 00:51:08:520] **Speaker 6:** Thank you.
[00:51:09:629 - 00:51:12:250] **Speaker 0:** I'm sorry I lost my headphones in the class, the
[00:51:12:250 - 00:51:13:409] **Speaker 1:** other day, so I was wondering if, oh, the other
[00:51:13:409 - 00:51:14:649] **Speaker 1:** day was it on a one?
[00:51:14:750 - 00:51:15:899] **Speaker 1:** Yeah, right in here, yeah.
[00:51:16:449 - 00:51:17:429] **Speaker 1:** What, which day?
[00:51:17:649 - 00:51:18:570] **Speaker 1:** Uh, yesterday.
[00:51:22:010 - 00:51:24:689] **Speaker 1:** I've checked with security, yeah, yeah, you have 3 times
[00:51:24:689 - 00:51:28:489] **Speaker 1:** now, yeah, yeah, yeah, um, the arts department or someone
[00:51:28:489 - 00:51:30:530] **Speaker 1:** like, I don't know who sort of owns this building,
[00:51:30:770 - 00:51:32:489] **Speaker 1:** but maybe the nearest admin.
[00:51:34:929 - 00:51:35:590] **Speaker 1:** All right, good luck.
[00:54:02:580 - 00:54:18:080] **Speaker 0:** Ah Like.
[00:54:45:939 - 00:54:47:100] **Speaker 0:** And I was, I was like.

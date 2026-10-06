# ENME302-26S2 Lecture 39 native Echo transcript

Date: October 1, 2026 10:00am-10:55am
Transcript type: native Echo automated transcript.

[00:00:59:189 - 00:01:12:720] **Speaker 0:** one Who Uh, good morning, we'll make a start.
[00:01:13:080 - 00:01:15:019] **Speaker 1:** I don't know if any of your classmates are still
[00:01:15:360 - 00:01:16:360] **Speaker 1:** sleeping or if they're.
[00:01:17:540 - 00:01:20:260] **Speaker 1:** Pondering about campus, but they might join us if we're
[00:01:20:260 - 00:01:20:720] **Speaker 1:** lucky.
[00:01:21:680 - 00:01:25:540] **Speaker 1:** So yesterday we're looking at the console model.
[00:01:26:419 - 00:01:28:519] **Speaker 1:** And trying to figure out alpha.
[00:01:29:449 - 00:01:31:059] **Speaker 1:** So I had a couple of minutes this morning, or
[00:01:31:059 - 00:01:33:580] **Speaker 1:** a few minutes this morning to troubleshoot and I fixed
[00:01:33:580 - 00:01:35:879] **Speaker 1:** it, so it's always fun to solve problems.
[00:01:36:720 - 00:01:38:800] **Speaker 1:** So we'll just go through and finish that example that
[00:01:38:800 - 00:01:40:580] **Speaker 1:** I poorly started yesterday.
[00:01:42:819 - 00:01:45:339] **Speaker 1:** But it's always interesting to watch someone else fumble through
[00:01:45:339 - 00:01:45:599] **Speaker 1:** on floor.
[00:01:46:910 - 00:01:48:430] **Speaker 1:** Hopefully you'll pick up some tricks as I go through
[00:01:48:430 - 00:01:52:779] **Speaker 1:** the debugging process, and yeah, hopefully it'll be helpful for
[00:01:52:779 - 00:01:54:589] **Speaker 1:** both your quiz and and the assignment.
[00:01:56:180 - 00:01:59:379] **Speaker 1:** If, if it's gonna connect, it connected for a moment.
[00:02:01:360 - 00:02:02:010] **Speaker 1:** Here we go.
[00:02:02:279 - 00:02:05:160] **Speaker 1:** Alright, so as a quick recap, we're doing this heat
[00:02:05:160 - 00:02:07:879] **Speaker 1:** equation and we're trying to figure out this heat deficivity.
[00:02:07:919 - 00:02:08:880] **Speaker 1:** If we didn't know what it was.
[00:02:09:160 - 00:02:12:559] **Speaker 1:** We prescribed some temperature at the, the midpoint after 6.75
[00:02:12:559 - 00:02:13:919] **Speaker 1:** seconds at 50 °C.
[00:02:14:800 - 00:02:16:720] **Speaker 1:** So we went through and we found that alpha was
[00:02:16:720 - 00:02:21:039] **Speaker 1:** 1.25 instead of 1.11 square centimetre squared per second, so
[00:02:21:039 - 00:02:21:779] **Speaker 1:** that was really puzzling.
[00:02:23:660 - 00:02:25:979] **Speaker 1:** So I guess the first thing to do is that
[00:02:25:979 - 00:02:27:520] **Speaker 1:** we've actually got the analytical solution.
[00:02:28:460 - 00:02:31:000] **Speaker 1:** We've derived this in class, so it would be smart
[00:02:31:000 - 00:02:32:160] **Speaker 1:** to plot this.
[00:02:33:330 - 00:02:34:830] **Speaker 1:** So under.
[00:02:37:419 - 00:02:41:020] **Speaker 1:** Uh, global definitions, we can create a function analytic.
[00:02:42:740 - 00:02:44:179] **Speaker 1:** And we can just call it the.
[00:02:45:660 - 00:02:49:229] **Speaker 1:** A And we're going to evaluate.
[00:02:50:880 - 00:02:54:699] **Speaker 1:** The Temperature in space and time.
[00:02:54:800 - 00:02:56:710] **Speaker 1:** So we've got two variables, X and T being independent
[00:02:56:710 - 00:03:01:039] **Speaker 1:** variables, and analytical solution is 100 times the sine of
[00:03:01:039 - 00:03:01:800] **Speaker 1:** pi.
[00:03:04:139 - 00:03:07:520] **Speaker 1:** X over the length, which we defined as a parameter
[00:03:07:520 - 00:03:08:009] **Speaker 1:** earlier.
[00:03:08:399 - 00:03:11:679] **Speaker 1:** So we'll keep that as L multiplied by the exponential
[00:03:11:679 - 00:03:12:679] **Speaker 1:** of minus alpha.
[00:03:16:300 - 00:03:17:949] **Speaker 1:** Multiply it by pi.
[00:03:20:110 - 00:03:23:929] **Speaker 1:** Over our Square times.
[00:03:25:240 - 00:03:30:910] **Speaker 1:** Time So the arguments here And I've done something wrong.
[00:03:33:580 - 00:03:34:139] **Speaker 1:** That's OK.
[00:03:34:330 - 00:03:36:979] **Speaker 1:** So we've got X and T being our um.
[00:03:37:710 - 00:03:40:070] **Speaker 1:** Arguments or the independent variables that we're gonna plot against,
[00:03:40:559 - 00:03:43:389] **Speaker 1:** we can inform the units and for this example I'm
[00:03:43:389 - 00:03:47:309] **Speaker 1:** just using Calvin, um, Excuse that.
[00:03:47:639 - 00:03:51:259] **Speaker 1:** So X is in metres, time is in seconds, and
[00:03:51:259 - 00:03:53:500] **Speaker 1:** we can plot this solution just to have a look
[00:03:53:500 - 00:03:55:020] **Speaker 1:** at what it looks like in space-time.
[00:03:56:619 - 00:03:59:539] **Speaker 1:** So the lower limit of X is 0 and the
[00:03:59:539 - 00:04:00:619] **Speaker 1:** upper limit is L.
[00:04:01:570 - 00:04:05:449] **Speaker 1:** And maybe we want to go up until this 6.75
[00:04:05:449 - 00:04:06:070] **Speaker 1:** minutes.
[00:04:09:740 - 00:04:12:779] **Speaker 1:** Again, I've used square brackets to denote the units of
[00:04:12:779 - 00:04:16:160] **Speaker 1:** this value and it'll convert to SI in seconds.
[00:04:17:299 - 00:04:30:010] **Speaker 1:** So if we plot Our solution What one of those.
[00:04:32:410 - 00:04:33:609] **Speaker 1:** Ah, we've changed alpha.
[00:04:34:049 - 00:04:36:029] **Speaker 1:** Let's change alpha to R 1.11.
[00:04:39:149 - 00:04:44:239] **Speaker 1:** And And that's looking a little bit more normal.
[00:04:44:769 - 00:04:46:579] **Speaker 1:** So how can we interpret this?
[00:04:46:660 - 00:04:47:880] **Speaker 1:** Maybe we put it around this way.
[00:04:48:660 - 00:04:52:089] **Speaker 1:** So on this axis we've got time and on the
[00:04:52:089 - 00:04:53:880] **Speaker 1:** depth we've got the X space.
[00:04:54:299 - 00:04:57:179] **Speaker 1:** So we've got this initial sign profile and it decays
[00:04:57:179 - 00:04:57:890] **Speaker 1:** over time.
[00:04:58:220 - 00:05:02:200] **Speaker 1:** So that's decaying to 50 degrees Kelvin.
[00:05:04:869 - 00:05:06:290] **Speaker 1:** So this is what the solution should be.
[00:05:06:709 - 00:05:09:549] **Speaker 1:** So if we go through and we did our optimisation
[00:05:09:549 - 00:05:11:649] **Speaker 1:** study, and I'll just run that again.
[00:05:13:070 - 00:05:16:510] **Speaker 1:** Because when we create functions or edit things further up
[00:05:16:510 - 00:05:18:880] **Speaker 1:** the chain, we need to run the solution again to
[00:05:18:880 - 00:05:22:429] **Speaker 1:** access those variables and functions in the results, uh, section
[00:05:22:429 - 00:05:23:910] **Speaker 1:** in the console, which is a bit of a pain
[00:05:23:910 - 00:05:24:750] **Speaker 1:** even though we don't need to.
[00:05:24:820 - 00:05:26:010] **Speaker 1:** It's just an analytical function.
[00:05:27:440 - 00:05:29:190] **Speaker 1:** And I want the plot.
[00:05:30:510 - 00:05:33:709] **Speaker 1:** The temperature at the midpoint and look at, look at
[00:05:33:709 - 00:05:34:750] **Speaker 1:** how it decays over time.
[00:05:35:109 - 00:05:37:570] **Speaker 1:** So we're evaluate a 1D plot group.
[00:05:40:320 - 00:05:42:109] **Speaker 1:** And a point graph.
[00:05:43:399 - 00:05:44:619] **Speaker 1:** Located at the midpoint.
[00:05:45:640 - 00:05:47:529] **Speaker 1:** This is our temperature that we solve for with our
[00:05:47:529 - 00:05:49:769] **Speaker 1:** finer elements, and we can see that it decays from
[00:05:49:769 - 00:05:50:369] **Speaker 1:** 100.
[00:05:51:059 - 00:05:54:010] **Speaker 1:** Um, Down, down to 50.
[00:06:01:690 - 00:06:03:609] **Speaker 1:** Over this interval.
[00:06:04:209 - 00:06:07:959] **Speaker 1:** And we can also create another point graph that takes
[00:06:07:959 - 00:06:09:470] **Speaker 1:** our value from the analytical function.
[00:06:09:730 - 00:06:11:519] **Speaker 1:** So if we just duplicate, we'll create a new point
[00:06:11:519 - 00:06:11:989] **Speaker 1:** graph.
[00:06:15:619 - 00:06:18:760] **Speaker 1:** Instead of evaluating T, which is our dependent variable field,
[00:06:19:059 - 00:06:22:820] **Speaker 1:** we're going to evaluate TA, the analytical at XT.
[00:06:23:809 - 00:06:26:010] **Speaker 1:** So those are the arguments that we provided in our
[00:06:26:010 - 00:06:28:429] **Speaker 1:** definition, and we're going to plot this.
[00:06:28:929 - 00:06:31:970] **Speaker 1:** And we can see that the numerical solution precisely matches
[00:06:31:970 - 00:06:33:010] **Speaker 1:** the analytical solution.
[00:06:34:230 - 00:06:35:190] **Speaker 1:** So that's reassuring.
[00:06:37:059 - 00:06:38:899] **Speaker 1:** So, then what is happening?
[00:06:39:690 - 00:06:42:769] **Speaker 1:** So after a little bit of puzzling, uh, you can
[00:06:42:769 - 00:06:45:529] **Speaker 1:** note that the time interval is going from 0 to
[00:06:45:529 - 00:06:46:309] **Speaker 1:** 6 minutes.
[00:06:48:140 - 00:06:51:089] **Speaker 1:** But we wanted 6.75 minutes.
[00:06:52:299 - 00:06:52:890] **Speaker 1:** Why?
[00:06:55:720 - 00:06:57:059] **Speaker 1:** And it's not very helpful.
[00:06:57:720 - 00:07:01:579] **Speaker 1:** So we'll just disable the optimisation study for now.
[00:07:02:529 - 00:07:06:880] **Speaker 1:** Um, And if we just compute that again, that's without
[00:07:06:880 - 00:07:10:399] **Speaker 1:** optimisation and it's just running that, that true case so
[00:07:10:399 - 00:07:11:519] **Speaker 1:** we know that this is correct.
[00:07:12:040 - 00:07:13:760] **Speaker 1:** So the main problem here is it's only going up
[00:07:13:760 - 00:07:15:799] **Speaker 1:** to 6 minutes, but we told it to go up
[00:07:15:799 - 00:07:17:119] **Speaker 1:** to 6 months, even 5 minutes.
[00:07:18:890 - 00:07:20:500] **Speaker 1:** Which is puzzling to me, and I, I guess it
[00:07:20:500 - 00:07:22:079] **Speaker 1:** puzzled me in the lecture yesterday.
[00:07:22:420 - 00:07:25:579] **Speaker 1:** Um, well, I didn't, I didn't notice it, but this
[00:07:25:579 - 00:07:28:079] **Speaker 1:** was the, the source of all the issues.
[00:07:28:579 - 00:07:32:200] **Speaker 1:** So for whatever reason, It's only going up to 6
[00:07:32:200 - 00:07:32:739] **Speaker 1:** minutes.
[00:07:32:839 - 00:07:35:480] **Speaker 1:** If we go under derived values and just point.
[00:07:36:769 - 00:07:39:730] **Speaker 1:** Evaluation and just plot every value of T that we
[00:07:39:730 - 00:07:40:429] **Speaker 1:** sold for.
[00:07:41:619 - 00:07:42:429] **Speaker 1:** We'll save.
[00:07:42:890 - 00:07:44:420] **Speaker 1:** It's only going up to 6 minutes, so it's not
[00:07:44:420 - 00:07:46:359] **Speaker 1:** including the upper bound of 6.75.
[00:07:47:989 - 00:07:49:100] **Speaker 1:** I I don't know why.
[00:07:49:269 - 00:07:50:079] **Speaker 1:** I think it should.
[00:07:50:589 - 00:07:53:070] **Speaker 1:** Maybe what it's doing is going up in steps of
[00:07:53:070 - 00:07:54:730] **Speaker 1:** one up until the last point.
[00:07:54:790 - 00:07:56:970] **Speaker 1:** It doesn't exceed this value.
[00:07:58:089 - 00:07:59:850] **Speaker 1:** Um, I don't think that's very good.
[00:08:00:309 - 00:08:03:029] **Speaker 1:** If I had more time, maybe I'd I'd give console
[00:08:03:029 - 00:08:04:049] **Speaker 1:** some feedback.
[00:08:06:149 - 00:08:08:769] **Speaker 1:** Maybe I will on later next week or something, but
[00:08:08:929 - 00:08:09:290] **Speaker 1:** I.
[00:08:10:700 - 00:08:13:700] **Speaker 1:** One way to get around that is to add a
[00:08:13:700 - 00:08:16:799] **Speaker 1:** value manually of 6.75 after this range.
[00:08:17:500 - 00:08:19:459] **Speaker 1:** So this is just a list of values, and some
[00:08:19:459 - 00:08:21:179] **Speaker 1:** of you have spotted this already, but you can have
[00:08:21:179 - 00:08:23:839] **Speaker 1:** a range that is more closely packed, especially if you've
[00:08:23:839 - 00:08:26:209] **Speaker 1:** got more interesting behaviour happening at earlier times.
[00:08:26:500 - 00:08:28:920] **Speaker 1:** For example, if you had range.
[00:08:30:829 - 00:08:34:390] **Speaker 1:** 0 steps of 0.1 up to 1, and then you'd
[00:08:34:390 - 00:08:36:070] **Speaker 1:** have another interval from 1.
[00:08:38:749 - 00:08:41:598] **Speaker 1:** In steps of one up to not including 6.75 and
[00:08:41:598 - 00:08:42:898] **Speaker 1:** then 6.75.
[00:08:43:609 - 00:08:45:799] **Speaker 1:** Um, maybe we just do that for, for fun.
[00:08:46:679 - 00:08:48:460] **Speaker 1:** So, point evaluation.
[00:08:49:780 - 00:08:54:539] **Speaker 1:** New table, so it's plotting 0.1, 0.2, 0.3, and then
[00:08:54:539 - 00:08:58:229] **Speaker 1:** it goes 1 and 1 twice because I include, well
[00:08:58:229 - 00:09:00:419] **Speaker 1:** now it's including the upper limit, uh, and then going
[00:09:00:419 - 00:09:02:239] **Speaker 1:** up to 6 and then 6.75.
[00:09:04:530 - 00:09:05:010] **Speaker 1:** All right.
[00:09:05:989 - 00:09:11:429] **Speaker 1:** So in short, We were optimising for alpha and matching
[00:09:11:429 - 00:09:14:909] **Speaker 1:** the temperature at the midpoint at 6 minutes, not 6.75,
[00:09:14:979 - 00:09:16:909] **Speaker 1:** which is why we were getting a slightly higher heat
[00:09:16:909 - 00:09:19:789] **Speaker 1:** deficivity because that increased the rate of heat transfer.
[00:09:22:989 - 00:09:25:630] **Speaker 1:** So that's a bit, a bit A bit painful, but
[00:09:25:630 - 00:09:28:030] **Speaker 1:** I guess it's important to always validate your models, so
[00:09:28:030 - 00:09:29:570] **Speaker 1:** it's a good demonstration of that.
[00:09:29:909 - 00:09:32:630] **Speaker 1:** And always check that you're solving and plotting what you're
[00:09:32:630 - 00:09:33:169] **Speaker 1:** expecting.
[00:09:33:630 - 00:09:35:309] **Speaker 1:** Uh, so check your x-axis.
[00:09:36:330 - 00:09:40:260] **Speaker 1:** So what we'll do now is maybe a simple range
[00:09:40:260 - 00:09:42:700] **Speaker 1:** from 0 up to 1010 in steps of 1.
[00:09:43:789 - 00:09:45:049] **Speaker 1:** And it's going up to 10 minutes.
[00:09:45:450 - 00:09:47:690] **Speaker 1:** So it fully encompasses that, that space.
[00:09:48:270 - 00:09:52:679] **Speaker 1:** And we're going to evaluate our objective function at 6.75
[00:09:52:679 - 00:09:53:190] **Speaker 1:** minutes.
[00:09:54:859 - 00:09:56:619] **Speaker 1:** So I tried to do this in class yesterday and
[00:09:56:619 - 00:09:58:320] **Speaker 1:** I must have got the syntax wrong.
[00:09:59:059 - 00:10:00:840] **Speaker 1:** But it is just the act operator.
[00:10:02:140 - 00:10:02:580] **Speaker 1:** At.
[00:10:03:429 - 00:10:06:960] **Speaker 1:** So you have at, and it's the time that we
[00:10:06:960 - 00:10:07:840] **Speaker 1:** need to set first.
[00:10:08:969 - 00:10:11:849] **Speaker 1:** So this is 6.75 minutes, so we can keep it
[00:10:11:849 - 00:10:12:250] **Speaker 1:** in.
[00:10:13:840 - 00:10:15:080] **Speaker 1:** 6.75 minutes.
[00:10:17:619 - 00:10:20:940] **Speaker 1:** And then the second argument of the at function is
[00:10:20:940 - 00:10:22:440] **Speaker 1:** the expression that we want to evaluate.
[00:10:24:320 - 00:10:26:049] **Speaker 1:** So as, as we say here, the objective function is
[00:10:26:049 - 00:10:27:309] **Speaker 1:** only evaluate the final time set.
[00:10:28:650 - 00:10:31:330] **Speaker 1:** So it's only going to calculate this expression after it's
[00:10:31:330 - 00:10:33:609] **Speaker 1:** solved in a final time step, but then it's going
[00:10:33:609 - 00:10:36:130] **Speaker 1:** to interpolate at 6.75 minutes.
[00:10:38:719 - 00:10:41:640] **Speaker 1:** So with any luck this will now work.
[00:10:51:229 - 00:10:54:979] **Speaker 1:** Cool, so you get 1.11 to 3 significant figures, it's
[00:10:54:979 - 00:10:56:500] **Speaker 1:** converging to 10 to -20.
[00:10:56:710 - 00:10:58:510] **Speaker 1:** I haven't done anything with the mesh, if we resolve
[00:10:58:510 - 00:11:00:440] **Speaker 1:** the mesh further it might get a little bit closer,
[00:11:00:830 - 00:11:03:150] **Speaker 1:** uh, but that's now, now matching what we expect.
[00:11:05:349 - 00:11:07:719] **Speaker 1:** Um, so yeah, I guess just a little bit of
[00:11:07:719 - 00:11:11:609] **Speaker 1:** a caution of of what these output times are, they're
[00:11:11:609 - 00:11:13:150] **Speaker 1:** not actually output times always.
[00:11:13:969 - 00:11:16:890] **Speaker 1:** Uh, we can spec and also I wanted to bring
[00:11:16:890 - 00:11:18:530] **Speaker 1:** another attention to the time stepping.
[00:11:21:289 - 00:11:24:250] **Speaker 1:** Uh, under the log tab, we can see the actual
[00:11:24:250 - 00:11:25:150] **Speaker 1:** time stamps.
[00:11:25:739 - 00:11:28:010] **Speaker 1:** Now we're getting really small, um.
[00:11:35:190 - 00:11:39:270] **Speaker 1:** So step 01 through to the end and we've indicated
[00:11:39:270 - 00:11:40:799] **Speaker 1:** what time and then the step size.
[00:11:41:349 - 00:11:43:070] **Speaker 1:** So console uses adaptive time stepping.
[00:11:43:239 - 00:11:45:150] **Speaker 1:** It doesn't set a prescribed time step like you do
[00:11:45:150 - 00:11:47:049] **Speaker 1:** in Python or finite difference.
[00:11:47:650 - 00:11:50:630] **Speaker 1:** Uh, and it adjusts, adjusts the step size so that
[00:11:50:630 - 00:11:53:630] **Speaker 1:** it reduces the residual within some tolerance.
[00:11:53:869 - 00:11:55:909] **Speaker 1:** So if we tighten the tolerance, the default here being
[00:11:55:909 - 00:12:00:150] **Speaker 1:** 10 to 2, if we go 1E-5 and compute.
[00:12:06:780 - 00:12:09:729] **Speaker 1:** We should see that it does more time steps slightly,
[00:12:10:309 - 00:12:12:150] **Speaker 1:** although this is the heat equation and it's not very
[00:12:12:150 - 00:12:14:210] **Speaker 1:** exciting in terms of requiring.
[00:12:15:280 - 00:12:17:799] **Speaker 1:** Much resolution, so it hasn't actually changed very much at
[00:12:17:799 - 00:12:18:070] **Speaker 1:** all.
[00:12:20:969 - 00:12:22:280] **Speaker 1:** But the argument stands.
[00:12:23:869 - 00:12:27:869] **Speaker 1:** Another way of refining the time stepping is under the
[00:12:27:869 - 00:12:30:760] **Speaker 1:** solver config solution time-dependent solver.
[00:12:30:919 - 00:12:32:880] **Speaker 1:** So this has all the settings for the time dependent
[00:12:32:880 - 00:12:33:400] **Speaker 1:** solver.
[00:12:33:880 - 00:12:37:429] **Speaker 1:** And we've got The silver type implicit, as I say,
[00:12:37:469 - 00:12:39:440] **Speaker 1:** it's an implicit scheme.
[00:12:39:510 - 00:12:40:010] **Speaker 1:** It's using.
[00:12:41:080 - 00:12:42:700] **Speaker 1:** I don't want to go into too much detail.
[00:12:42:780 - 00:12:45:700] **Speaker 1:** The main step here is that steps taken by solver
[00:12:45:700 - 00:12:49:179] **Speaker 1:** instead of being completely free, and then interpolating across all
[00:12:49:179 - 00:12:53:140] **Speaker 1:** the output times, we can make it uh apply for
[00:12:53:140 - 00:12:57:020] **Speaker 1:** each, Output time, so this is under strict.
[00:12:58:169 - 00:13:00:109] **Speaker 1:** So, if you solve.
[00:13:02:090 - 00:13:02:619] **Speaker 1:** Now.
[00:13:09:219 - 00:13:10:960] **Speaker 1:** OK, it's not doing what I think.
[00:13:11:469 - 00:13:12:260] **Speaker 1:** We'll leave it there.
[00:13:19:900 - 00:13:20:419] **Speaker 1:** All of us.
[00:13:25:890 - 00:13:26:409] **Speaker 1:** OK.
[00:13:27:340 - 00:13:29:299] **Speaker 1:** I'm not sure why that's not picking up that, but
[00:13:29:580 - 00:13:30:219] **Speaker 1:** this is.
[00:13:31:440 - 00:13:32:880] **Speaker 1:** What you should be able to.
[00:13:33:729 - 00:13:34:210] **Speaker 1:** Sit.
[00:14:07:419 - 00:14:09:099] **Speaker 1:** I'd have to research a little bit more.
[00:14:09:179 - 00:14:09:979] **Speaker 1:** It might be.
[00:14:11:969 - 00:14:14:580] **Speaker 1:** They might be doing those steps and not including them
[00:14:14:580 - 00:14:15:299] **Speaker 1:** in the log.
[00:14:21:140 - 00:14:25:479] **Speaker 1:** Um But you don't need to worry too much, you
[00:14:25:479 - 00:14:26:619] **Speaker 1:** don't need to worry about that.
[00:14:26:960 - 00:14:28:559] **Speaker 1:** The main thing that I wanted to show you was
[00:14:28:559 - 00:14:29:659] **Speaker 1:** this relative tolerance.
[00:14:30:450 - 00:14:33:690] **Speaker 1:** If you weren't sure on the resolution and time, this
[00:14:33:690 - 00:14:35:849] **Speaker 1:** is the the adjustment that you have, and that's one
[00:14:35:849 - 00:14:38:729] **Speaker 1:** of the hints that are in the assignment list.
[00:14:41:349 - 00:14:41:590] **Speaker 1:** Cool.
[00:14:42:390 - 00:14:42:969] **Speaker 1:** Alright.
[00:14:43:390 - 00:14:45:590] **Speaker 1:** Hopefully I've convinced you that you can use this for,
[00:14:45:690 - 00:14:48:789] **Speaker 1:** for figuring out parameters, parameter ID.
[00:14:49:349 - 00:14:52:770] **Speaker 1:** This is using the general optimisation uh part.
[00:14:53:859 - 00:14:56:619] **Speaker 1:** Or physics interface, there's other ones available.
[00:14:56:900 - 00:14:58:119] **Speaker 1:** So some of these.
[00:14:59:460 - 00:15:02:599] **Speaker 1:** Guide you through the process, uh, but I just find
[00:15:02:599 - 00:15:05:200] **Speaker 1:** it easier to use the, the standard one, and then
[00:15:05:200 - 00:15:07:479] **Speaker 1:** we can just apply the objective function directly as we,
[00:15:07:679 - 00:15:09:260] **Speaker 1:** as we showed in chapter 12.
[00:15:11:900 - 00:15:12:619] **Speaker 1:** All right.
[00:15:13:530 - 00:15:14:789] **Speaker 1:** Any questions?
[00:15:16:369 - 00:15:16:599] **Speaker 1:** On console.
[00:15:18:000 - 00:15:19:229] **Speaker 1:** Quiz or anything?
[00:15:21:940 - 00:15:24:570] **Speaker 1:** Uh, Right.
[00:15:26:059 - 00:15:26:309] **Speaker 1:** Cool.
[00:15:26:460 - 00:15:30:679] **Speaker 1:** Alright, well we get to do chapter 9 on finite
[00:15:30:679 - 00:15:31:099] **Speaker 1:** elements.
[00:15:31:340 - 00:15:34:580] **Speaker 1:** So we're gonna apply what we did earlier in the
[00:15:34:580 - 00:15:36:719] **Speaker 1:** week into our finite elements scheme.
[00:15:37:969 - 00:15:39:590] **Speaker 1:** And hopefully bring things together.
[00:15:47:109 - 00:15:49:270] **Speaker 1:** And hopefully it all makes sense, with any luck.
[00:15:49:979 - 00:15:52:520] **Speaker 1:** So we looked at final elements, we looked at discretizing
[00:15:52:520 - 00:15:53:799] **Speaker 1:** it within some space.
[00:15:54:190 - 00:15:56:479] **Speaker 1:** Um, maybe I've still got the piece of paper somewhere.
[00:15:57:809 - 00:15:59:609] **Speaker 1:** We had these quadratic elements.
[00:16:00:450 - 00:16:19:989] **Speaker 1:** Um, This will do.
[00:16:27:039 - 00:16:30:039] **Speaker 1:** Um, we had this, uh, finite element space that we
[00:16:30:039 - 00:16:34:239] **Speaker 1:** discretized and we noted that there were some regions that
[00:16:34:239 - 00:16:37:830] **Speaker 1:** were not captured within the finite element space, um.
[00:16:39:309 - 00:16:42:590] **Speaker 1:** And we're going to now derive the finite element equations
[00:16:42:590 - 00:16:43:210] **Speaker 1:** to solve.
[00:16:44:659 - 00:16:47:229] **Speaker 1:** So to work through this, we're gonna look at our
[00:16:47:229 - 00:16:50:539] **Speaker 1:** um diffusion well forson equation here.
[00:16:51:059 - 00:16:53:500] **Speaker 1:** So we're looking at a long thin rod that we
[00:16:53:500 - 00:16:55:780] **Speaker 1:** have some boundary conditions and a continuous heat source.
[00:16:56:419 - 00:16:58:340] **Speaker 1:** So the right-hand side is the heat source and we've
[00:16:58:340 - 00:17:00:440] **Speaker 1:** got a diffusion uh thermal on the left.
[00:17:02:280 - 00:17:03:440] **Speaker 1:** And this is our governing equation.
[00:17:03:479 - 00:17:05:959] **Speaker 1:** We've got boundary conditions on the left and right of
[00:17:05:959 - 00:17:06:839] **Speaker 1:** TA and TB.
[00:17:08:109 - 00:17:10:949] **Speaker 1:** This is gonna be an ODE, uh, but we can
[00:17:10:949 - 00:17:14:219] **Speaker 1:** still apply the same technology or the same methodology, uh,
[00:17:14:229 - 00:17:17:329] **Speaker 1:** to finite element in PDE space.
[00:17:20:188 - 00:17:23:668] **Speaker 1:** So First, we need to discretize the domain into some
[00:17:23:668 - 00:17:24:308] **Speaker 1:** set elements.
[00:17:24:548 - 00:17:27:938] **Speaker 1:** So we've got an interval from X equals 0 to
[00:17:27:938 - 00:17:28:848] **Speaker 1:** x equal to L.
[00:17:29:520 - 00:17:32:540] **Speaker 1:** And we've got 4 elements, so nodes 1 to 5.
[00:17:34:010 - 00:17:38:150] **Speaker 1:** I've drawn the zigzag arrows to denote the heat source.
[00:17:39:380 - 00:17:42:500] **Speaker 1:** And we've got the boundary conditions, TA and TB.
[00:17:42:859 - 00:17:45:760] **Speaker 1:** The nodes that we're evaluating are T1, 234, and 5,
[00:17:46:140 - 00:17:48:020] **Speaker 1:** and our elements are 1 through 4.
[00:17:59:780 - 00:18:04:119] **Speaker 1:** So our first step is to rewrite our governing equation,
[00:18:04:660 - 00:18:06:819] **Speaker 1:** uh, so that we have all the terms on one
[00:18:06:819 - 00:18:08:140] **Speaker 1:** side of the equal sign.
[00:18:11:420 - 00:18:12:750] **Speaker 1:** So we're just gonna shift all the terms on the
[00:18:12:750 - 00:18:12:910] **Speaker 1:** right.
[00:18:12:979 - 00:18:16:969] **Speaker 1:** So we've got D2 T DX2 plus F of X.
[00:18:18:030 - 00:18:21:119] **Speaker 1:** Um, because the goal is to essentially approximate the, the
[00:18:21:119 - 00:18:24:839] **Speaker 1:** solution space and have some leftover residual that will sit
[00:18:24:839 - 00:18:25:359] **Speaker 1:** to zero.
[00:18:26:189 - 00:18:29:239] **Speaker 1:** So we're gonna assume an approximate form of our temperature
[00:18:29:239 - 00:18:33:020] **Speaker 1:** distribution, T tilter, and that's using maybe linear or quadratic
[00:18:33:189 - 00:18:35:739] **Speaker 1:** uh shape elements as we derived earlier in the week.
[00:18:36:680 - 00:18:40:680] **Speaker 1:** And When we plug this in The left-hand side will
[00:18:40:680 - 00:18:42:170] **Speaker 1:** not be precisely equal to zero.
[00:18:42:250 - 00:18:43:770] **Speaker 1:** There'll be some remainder residual.
[00:18:45:160 - 00:18:47:280] **Speaker 1:** And that residual is going to be defined as R
[00:18:47:280 - 00:18:53:839] **Speaker 1:** X equal to D2Tta by DX2 plus F of X.
[00:19:05:390 - 00:19:08:709] **Speaker 1:** So here I've substituted tea for Taura, because it's not
[00:19:08:709 - 00:19:12:030] **Speaker 1:** an exact solution, uh, there might be some, some residual.
[00:19:14:349 - 00:19:17:150] **Speaker 1:** So the method of weighted residuals, which is pretty much
[00:19:17:150 - 00:19:18:949] **Speaker 1:** what we're looking at in this class for finite elements,
[00:19:19:150 - 00:19:22:449] **Speaker 1:** is where we search for a minimum, uh, for this
[00:19:22:449 - 00:19:26:650] **Speaker 1:** residual, where we take the integral across our element space
[00:19:26:829 - 00:19:28:030] **Speaker 1:** and set it equal to zero.
[00:19:28:550 - 00:19:30:930] **Speaker 1:** So we've taken the integral over our domain.
[00:19:33:650 - 00:19:37:479] **Speaker 1:** Of our residual axe multiplied by some weighting functions.
[00:19:38:750 - 00:19:45:099] **Speaker 1:** D X equal to 04 I equals 123, all the
[00:19:45:099 - 00:19:45:750] **Speaker 1:** way up to sum.
[00:19:46:589 - 00:19:47:939] **Speaker 1:** A number of degrees of freedom.
[00:19:50:229 - 00:19:53:430] **Speaker 1:** So W here is just some learning independent weighting functions.
[00:19:54:869 - 00:19:59:449] **Speaker 1:** Uh, we looked at those polynomials for those shape elements,
[00:19:59:670 - 00:20:02:469] **Speaker 1:** you could use, I don't know, other, other series as
[00:20:02:469 - 00:20:04:290] **Speaker 1:** well, but we're not doing that in this class.
[00:20:05:469 - 00:20:09:069] **Speaker 1:** So Obviously there's heaps of different ones and we're going
[00:20:09:069 - 00:20:13:010] **Speaker 1:** to use these interpolation functions and call this the Galurkin
[00:20:13:010 - 00:20:13:410] **Speaker 1:** method.
[00:20:18:500 - 00:20:22:300] **Speaker 1:** So substituting in our weighting functions, WI for NI and
[00:20:22:300 - 00:20:26:739] **Speaker 1:** we've now got our integral across our space R W
[00:20:26:739 - 00:20:32:439] **Speaker 1:** I D X equal to our domain R N I
[00:20:32:979 - 00:20:33:500] **Speaker 1:** DX.
[00:20:35:369 - 00:20:37:969] **Speaker 1:** For I equals 123.
[00:20:38:890 - 00:20:53:430] **Speaker 1:** Onwards So I guess physically we're trying to sort of
[00:20:54:459 - 00:20:56:400] **Speaker 1:** Reduce our error.
[00:20:57:270 - 00:21:00:729] **Speaker 1:** By integrating over each element and setting it to 0,
[00:21:01:099 - 00:21:02:109] **Speaker 1:** a little bit hand wavy.
[00:21:03:510 - 00:21:05:599] **Speaker 1:** So we're gonna look at a single element.
[00:21:06:109 - 00:21:07:390] **Speaker 1:** Maybe it's between 1 and 2.
[00:21:08:699 - 00:21:11:739] **Speaker 1:** And we've got Uh, we're gonna end up with some
[00:21:11:739 - 00:21:14:420] **Speaker 1:** equations because that's, that's part of the fun.
[00:21:14:979 - 00:21:17:020] **Speaker 1:** So we're going to end up with some 2 x
[00:21:17:020 - 00:21:17:739] **Speaker 1:** 3 system.
[00:21:19:109 - 00:21:23:380] **Speaker 1:** And if we integrate across our element from X1 to
[00:21:23:380 - 00:21:23:989] **Speaker 1:** X2.
[00:21:29:400 - 00:21:31:660] **Speaker 1:** We are integrating the residual.
[00:21:32:560 - 00:21:34:550] **Speaker 1:** Which we defined an equation 4.
[00:21:36:000 - 00:21:37:099] **Speaker 1:** So we're gonna substute an R.
[00:21:40:530 - 00:21:44:010] **Speaker 1:** D2T tilta by DX2.
[00:21:46:780 - 00:21:47:930] **Speaker 1:** Plus F of X.
[00:21:51:979 - 00:21:56:140] **Speaker 1:** And uh Timesing this by our shape function in.
[00:21:59:089 - 00:21:59:770] **Speaker 1:** In Iovic.
[00:22:00:709 - 00:22:02:170] **Speaker 1:** And integrating in X.
[00:22:06:430 - 00:22:10:670] **Speaker 1:** For the linear shape elements, or yeah, elements we've got
[00:22:10:670 - 00:22:12:369] **Speaker 1:** two degrees of freedom, one on the left.
[00:22:13:540 - 00:22:14:619] **Speaker 1:** And one on the right.
[00:22:15:739 - 00:22:17:260] **Speaker 1:** So we've got 1 equals 1 and 2.
[00:22:17:449 - 00:22:18:560] **Speaker 1:** So we've got two equations.
[00:22:19:930 - 00:22:20:989] **Speaker 1:** One for each shape element.
[00:22:23:650 - 00:22:23:660] **Speaker 1:** Now.
[00:22:26:030 - 00:22:27:329] **Speaker 1:** We can rearrange this.
[00:22:28:099 - 00:22:32:550] **Speaker 1:** And we'll apply our integral from X1 to X2.
[00:22:33:189 - 00:22:35:810] **Speaker 1:** And we'll just include this, uh, 2nd order derivative.
[00:22:36:859 - 00:22:40:400] **Speaker 1:** D2T tota uh DX2.
[00:22:41:089 - 00:22:46:569] **Speaker 1:** In I D X And we'll shift the source term
[00:22:46:790 - 00:22:49:010] **Speaker 1:** FXX on the right-hand side, so that's equal to minus
[00:22:49:010 - 00:22:50:229] **Speaker 1:** X1 to X2.
[00:22:51:359 - 00:23:20:920] **Speaker 1:** F N I D X Does anyone have an idea
[00:23:20:920 - 00:23:24:219] **Speaker 1:** of what D2T divide DX2 would equal?
[00:23:26:589 - 00:23:28:180] **Speaker 1:** Through our sheikhs.
[00:23:36:430 - 00:23:38:089] **Speaker 1:** Does anyone know what Tilda is?
[00:23:39:719 - 00:23:40:359] **Speaker 1:** Equal to.
[00:23:46:099 - 00:23:48:050] **Speaker 1:** It was days ago, yesterday or something.
[00:23:48:250 - 00:23:52:729] **Speaker 1:** So we've got N1, T1 plus N2 T2.
[00:23:53:239 - 00:23:54:819] **Speaker 1:** So I've replaced the Us with Ts.
[00:23:55:219 - 00:23:58:609] **Speaker 1:** So we've got, we're approximating our temperature field.
[00:24:00:130 - 00:24:01:250] **Speaker 1:** With this, this weighting.
[00:24:01:329 - 00:24:05:050] **Speaker 1:** So if you think of maybe a temperature profile could
[00:24:05:050 - 00:24:08:310] **Speaker 1:** go from T1 down to T2 on that interval.
[00:24:09:229 - 00:24:11:390] **Speaker 1:** And those shape elements in 1 and 2 are just
[00:24:11:390 - 00:24:14:680] **Speaker 1:** veering from, I don't know, maybe draw that somewhere.
[00:24:18:859 - 00:24:22:540] **Speaker 1:** N1 goes from 1 to 0.
[00:24:27:699 - 00:24:28:319] **Speaker 1:** And in.
[00:24:31:979 - 00:24:33:060] **Speaker 1:** Goes from 0 to 1.
[00:24:44:150 - 00:24:46:869] **Speaker 1:** We'll change those to dynamics too just because that's what
[00:24:46:869 - 00:24:47:369] **Speaker 1:** it should be.
[00:24:48:140 - 00:24:51:380] **Speaker 1:** So we've got Tea.
[00:24:52:410 - 00:24:57:339] **Speaker 1:** Veering linearly over our element, what's, The derivative of a
[00:24:57:339 - 00:24:57:719] **Speaker 1:** line.
[00:24:58:910 - 00:25:00:369] **Speaker 1:** We get that coefficient.
[00:25:00:829 - 00:25:02:750] **Speaker 1:** We derived, I think it was A0 to A1.
[00:25:03:619 - 00:25:06:339] **Speaker 1:** What happens if we take the 2nd derivative of a
[00:25:06:339 - 00:25:06:680] **Speaker 1:** line?
[00:25:11:050 - 00:25:13:540] **Speaker 1:** 0, which is not going to be very helpful because
[00:25:13:540 - 00:25:14:560] **Speaker 1:** if we had 0.
[00:25:15:550 - 00:25:18:010] **Speaker 1:** That just removes that term and then we've got this
[00:25:18:229 - 00:25:19:489] **Speaker 1:** the source term on the right.
[00:25:21:390 - 00:25:22:910] **Speaker 1:** So to get around this, what we're going to do
[00:25:22:910 - 00:25:27:410] **Speaker 1:** is apply integration by parts to lower the order of
[00:25:27:410 - 00:25:29:349] **Speaker 1:** the derivative D2T tilted by DX2.
[00:25:31:319 - 00:25:35:719] **Speaker 1:** And we're running out of space, but well, this is
[00:25:35:719 - 00:25:38:040] **Speaker 1:** where we're writing stuff, so just as a recap for
[00:25:38:040 - 00:25:43:479] **Speaker 1:** integration by parts because everyone forgets, integral of UDV is
[00:25:43:479 - 00:25:47:079] **Speaker 1:** equal to UV minus integral of VDU.
[00:25:55:209 - 00:26:00:040] **Speaker 1:** So which Which is you, which is V for our
[00:26:00:040 - 00:26:00:699] **Speaker 1:** expression.
[00:26:02:280 - 00:26:04:119] **Speaker 1:** If you want to do integration by parts.
[00:26:16:219 - 00:26:19:959] **Speaker 1:** So U goes to DU we differentiate, DV goes to
[00:26:19:959 - 00:26:20:920] **Speaker 1:** V, we integrate.
[00:26:26:469 - 00:26:28:469] **Speaker 1:** We want to reduce the order of that derivative.
[00:26:28:550 - 00:26:31:709] **Speaker 1:** So we're gonna have to select DV to be D2T
[00:26:31:709 - 00:26:33:010] **Speaker 1:** tilted by DX2.
[00:26:34:979 - 00:26:36:339] **Speaker 1:** So we've got U of N.
[00:26:38:780 - 00:26:42:579] **Speaker 1:** DV integrating, we get to V, so now we've just
[00:26:42:579 - 00:26:46:359] **Speaker 1:** got a first order derivative DT tilda by DX.
[00:26:48:739 - 00:26:51:579] **Speaker 1:** The limits of integration is over our element X1 X2.
[00:26:53:949 - 00:26:58:020] **Speaker 1:** And then we've got minus The integral of.
[00:27:00:479 - 00:27:01:520] **Speaker 1:** VDU.
[00:27:01:880 - 00:27:07:040] **Speaker 1:** So we just said was DT Tora by DX and
[00:27:07:040 - 00:27:12:359] **Speaker 1:** DU is the derivative DNIY DX.
[00:27:17:489 - 00:27:19:540] **Speaker 1:** Again, we've got two equations here, one for shape element
[00:27:19:540 - 00:27:22:520] **Speaker 1:** 11 for shape element 2, or nodes 1 and 2.
[00:27:40:579 - 00:27:43:439] **Speaker 1:** So this is commonly referred to as the weak form
[00:27:43:819 - 00:27:47:439] **Speaker 1:** of the the governing equation because we've reduced the order.
[00:27:48:280 - 00:27:52:119] **Speaker 1:** Uh, and it's Weaker, in some sense.
[00:27:59:280 - 00:28:01:500] **Speaker 1:** So we've got 2 degrees of freedom.
[00:28:01:839 - 00:28:03:729] **Speaker 1:** We've got one for I equals 11 for I equals
[00:28:03:729 - 00:28:05:319] **Speaker 1:** 2, so we're gonna go through both cases.
[00:28:09:579 - 00:28:10:989] **Speaker 1:** So the first case we'll look at is one.
[00:28:12:410 - 00:28:16:630] **Speaker 1:** And we said that shape function 1 was equal to
[00:28:16:630 - 00:28:18:729] **Speaker 1:** X2 minus X over X2 minus X1.
[00:28:19:530 - 00:28:22:410] **Speaker 1:** So we can um evaluate some of these terms.
[00:28:22:890 - 00:28:28:660] **Speaker 1:** So we're first going to analyse This uh integral.
[00:28:30:369 - 00:28:32:260] **Speaker 1:** N I DT by X.
[00:28:36:530 - 00:28:39:010] **Speaker 1:** NI, which is equal to 1.
[00:28:40:130 - 00:28:42:650] **Speaker 1:** DT Tilda R D X.
[00:28:44:050 - 00:28:45:349] **Speaker 1:** From X1 to X2.
[00:28:49:489 - 00:28:51:410] **Speaker 1:** So it's a little bit painful because we're doing step
[00:28:51:410 - 00:28:53:989] **Speaker 1:** by step when you're just doing it as a full
[00:28:53:989 - 00:28:56:160] **Speaker 1:** question, you can just do it all sort of in
[00:28:56:160 - 00:28:59:250] **Speaker 1:** one in one go, but for explanation purposes we're doing
[00:28:59:250 - 00:29:00:089] **Speaker 1:** it step by step.
[00:29:01:810 - 00:29:04:310] **Speaker 1:** When we evaluate this integral, we need to evaluate it
[00:29:04:310 - 00:29:05:880] **Speaker 1:** obviously at the upper limit first.
[00:29:06:160 - 00:29:07:260] **Speaker 1:** So we've got N1.
[00:29:08:170 - 00:29:15:130] **Speaker 1:** At X2 And the derivative DET Tilda by DX at
[00:29:15:130 - 00:29:15:790] **Speaker 1:** X2.
[00:29:18:140 - 00:29:19:839] **Speaker 1:** Minus the lower limit, so N1.
[00:29:20:719 - 00:29:25:920] **Speaker 1:** At X1 and DT Tota by DX at X1.
[00:29:36:310 - 00:29:37:280] **Speaker 1:** What does this equal?
[00:29:41:160 - 00:29:42:849] **Speaker 1:** We don't need to do anything with the gradients for
[00:29:42:849 - 00:29:45:130] **Speaker 1:** now, but what does N1 of X2 equal?
[00:29:45:880 - 00:29:48:280] **Speaker 1:** 0 and N1 of X1 is going to be equal
[00:29:48:280 - 00:29:48:839] **Speaker 1:** to 1.
[00:29:49:359 - 00:29:51:500] **Speaker 1:** So we can substitute in our equation.
[00:29:52:040 - 00:29:56:959] **Speaker 1:** So we've got minus DT by DX at X1.
[00:30:01:369 - 00:30:03:260] **Speaker 1:** So that's for that first equation, I 1, we'll do
[00:30:03:260 - 00:30:04:439] **Speaker 1:** the same for I equal 2.
[00:30:26:510 - 00:30:28:479] **Speaker 1:** And now we're looking at shape function 2, so N2
[00:30:28:479 - 00:30:31:739] **Speaker 1:** at X2 is 1, N2 and X1 is 0.
[00:30:32:010 - 00:30:36:380] **Speaker 1:** So now we're left with positive DT tilter by DX
[00:30:36:439 - 00:30:37:560] **Speaker 1:** at X.
[00:30:54:219 - 00:30:58:369] **Speaker 1:** So we've evaluated those that first term and we can
[00:30:58:670 - 00:31:01:869] **Speaker 1:** now insert it into our equation from before.
[00:31:03:959 - 00:31:06:079] **Speaker 1:** So equation 8.
[00:31:09:339 - 00:31:12:619] **Speaker 1:** We're going to substitute in our expression here and we've
[00:31:12:619 - 00:31:14:369] **Speaker 1:** got, And grow.
[00:31:15:280 - 00:31:16:959] **Speaker 1:** From X1 X2.
[00:31:18:479 - 00:31:23:699] **Speaker 1:** DT tota by DX, DN1 by DX.
[00:31:23:869 - 00:31:28:160] **Speaker 1:** DX is equal to minus DT tota by DX.
[00:31:30:410 - 00:31:32:329] **Speaker 1:** Uh, at X1, so that's the first term, and then
[00:31:32:329 - 00:31:35:609] **Speaker 1:** plus integral from X1 to X2 of F.
[00:31:36:410 - 00:31:38:430] **Speaker 1:** N 1 D X.
[00:31:43:050 - 00:31:44:729] **Speaker 1:** Similarly, for I equal 2.
[00:31:47:349 - 00:31:53:750] **Speaker 1:** We've got DT Toda by DX, DN2 by DX.
[00:31:54:979 - 00:31:58:670] **Speaker 1:** And positive DTtoda by DX add X2.
[00:31:59:420 - 00:32:04:819] **Speaker 1:** And our source term is the same, FN2 DX or
[00:32:04:819 - 00:32:05:859] **Speaker 1:** into is equal to.
[00:32:08:689 - 00:32:09:969] **Speaker 1:** You know, I put it into other.
[00:32:17:900 - 00:32:20:040] **Speaker 1:** So it's still a little bit puzzling at the moment,
[00:32:20:500 - 00:32:21:099] **Speaker 1:** um.
[00:32:24:290 - 00:32:26:030] **Speaker 1:** But we'll piece everything together shortly.
[00:32:26:569 - 00:32:28:969] **Speaker 1:** So we, we remember because we just did on the
[00:32:28:969 - 00:32:32:969] **Speaker 1:** last page that T tilda is equal to N1 T1.
[00:32:33:839 - 00:32:35:949] **Speaker 1:** Plus N2 T2.
[00:32:37:810 - 00:32:40:609] **Speaker 1:** So that's what Turra was, that's our linear interpolation within
[00:32:40:609 - 00:32:41:310] **Speaker 1:** our element.
[00:32:41:890 - 00:32:42:989] **Speaker 1:** The gradient of this.
[00:32:46:290 - 00:32:49:489] **Speaker 1:** DT tilted by DX we looked at yesterday, and this
[00:32:49:489 - 00:32:53:209] **Speaker 1:** was just rise over run for a linear interval, T2
[00:32:53:209 - 00:32:54:209] **Speaker 1:** minus T1.
[00:32:55:170 - 00:32:56:550] **Speaker 1:** Over X2 minus X1.
[00:33:00:989 - 00:33:07:300] **Speaker 1:** And does anyone remember what the And one by DX
[00:33:07:300 - 00:33:11:099] **Speaker 1:** was, that was the gradient of our first shape element.
[00:33:25:949 - 00:33:27:750] **Speaker 1:** Yeah, that it's almost one.
[00:33:30:689 - 00:33:35:300] **Speaker 1:** Um, So the first ray elements going down.
[00:33:35:459 - 00:33:36:839] **Speaker 1:** It's a little bit misleading, but.
[00:33:38:050 - 00:33:39:900] **Speaker 1:** So the first shape element goes from 1 down to
[00:33:39:900 - 00:33:43:939] **Speaker 1:** 0, and it's across the interval of delta X.
[00:33:46:069 - 00:33:48:130] **Speaker 1:** So minus 1 over X2.
[00:33:49:300 - 00:33:50:150] **Speaker 1:** Minus X1.
[00:33:52:500 - 00:33:55:180] **Speaker 1:** So DN2 is 1 over X2 minus X1.
[00:33:55:890 - 00:33:58:030] **Speaker 1:** So we're going to substitute these into our expressions.
[00:33:58:650 - 00:34:02:910] **Speaker 1:** That's why we did all this homework was housekeeping, bookkeeping,
[00:34:03:209 - 00:34:04:020] **Speaker 1:** uh, earlier in the week.
[00:34:04:369 - 00:34:07:069] **Speaker 1:** We're gonna substitute that into our expression and we've got,
[00:34:09:260 - 00:34:15:090] **Speaker 1:** The revolov DT Toda via D X DN1 via DX
[00:34:15:378 - 00:34:16:120] **Speaker 1:** DX.
[00:34:20:169 - 00:34:23:560] **Speaker 1:** Equal to the derivative of our temperature field or approximate
[00:34:23:560 - 00:34:28:070] **Speaker 1:** temperature field over that space and this was Data T
[00:34:28:070 - 00:34:32:870] **Speaker 1:** over X, so T2 minus T1 over X2 minus X1.
[00:34:34:080 - 00:34:38:120] **Speaker 1:** The gradient DN1 by DX was -1 over X2 minus
[00:34:38:120 - 00:34:38:638] **Speaker 1:** X1.
[00:34:41:060 - 00:34:45:500] **Speaker 1:** And that's over Our element DX.
[00:34:50:439 - 00:34:52:070] **Speaker 1:** How can we simplify this integral?
[00:34:52:199 - 00:34:54:100] **Speaker 1:** What can we do to make it a bit easier?
[00:34:57:019 - 00:35:00:188] **Speaker 1:** Do any of these uh values vary across the element?
[00:35:06:770 - 00:35:07:219] **Speaker 1:** Nope.
[00:35:07:620 - 00:35:09:729] **Speaker 1:** So these are values that are just at the nodal
[00:35:09:729 - 00:35:10:179] **Speaker 1:** points.
[00:35:10:860 - 00:35:13:330] **Speaker 1:** So X1 X2 are just coordinate spaces.
[00:35:13:959 - 00:35:16:870] **Speaker 1:** T1 and T2 are the value of the dependent variable
[00:35:16:870 - 00:35:18:409] **Speaker 1:** at the nodes 1 and 2.
[00:35:18:899 - 00:35:21:030] **Speaker 1:** Because they're not varying in X, we can take them
[00:35:21:030 - 00:35:22:129] **Speaker 1:** outside of the derivative.
[00:35:23:340 - 00:35:24:340] **Speaker 1:** Makes it much easier.
[00:35:25:959 - 00:35:33:459] **Speaker 1:** So we're left with Minus T 2 minus T1 over
[00:35:33:459 - 00:35:34:699] **Speaker 1:** X2 minus X1.
[00:35:37:399 - 00:35:38:000] **Speaker 1:** Squid.
[00:35:43:159 - 00:35:45:169] **Speaker 1:** We don't really need those extra brackets, but we've put
[00:35:45:169 - 00:35:47:110] **Speaker 1:** them in for good measure.
[00:35:47:570 - 00:35:48:850] **Speaker 1:** And we're left with integrating.
[00:35:50:379 - 00:35:58:010] **Speaker 1:** One What's the integral of one across that element?
[00:36:00:959 - 00:36:02:409] **Speaker 1:** It's always a trick question, isn't it?
[00:36:06:629 - 00:36:07:570] **Speaker 1:** Yep, that's right.
[00:36:10:919 - 00:36:14:639] **Speaker 1:** So Integrating one we go to X and then we're
[00:36:14:639 - 00:36:16:520] **Speaker 1:** at the limits of integration X2 minus X1.
[00:36:16:729 - 00:36:18:080] **Speaker 1:** This is going to cancel with one of them in
[00:36:18:080 - 00:36:23:080] **Speaker 1:** the denominator and we're left with, T1 minus D2, so
[00:36:23:080 - 00:36:24:699] **Speaker 1:** I've just introduced that negative sign.
[00:36:25:620 - 00:36:27:500] **Speaker 1:** Divided by X2 minus X1.
[00:36:32:510 - 00:36:35:570] **Speaker 1:** So this is for the first element equation for 14
[00:36:35:570 - 00:36:35:949] **Speaker 1:** to 1.
[00:36:41:070 - 00:36:42:459] **Speaker 1:** Yeah, lots of maths.
[00:36:42:919 - 00:36:43:760] **Speaker 1:** Lots of steps.
[00:36:44:909 - 00:36:48:520] **Speaker 1:** So We'll do the same for IQL 2.
[00:36:52:780 - 00:36:55:899] **Speaker 1:** Now, really the only difference is that we're looking at
[00:36:55:899 - 00:36:57:919] **Speaker 1:** the shape element N2.
[00:36:58:399 - 00:37:04:159] **Speaker 1:** So we've got DT by DX DN2 by D X
[00:37:04:360 - 00:37:05:139] **Speaker 1:** D X.
[00:37:08:000 - 00:37:08:879] **Speaker 1:** Equal to.
[00:37:13:370 - 00:37:16:889] **Speaker 1:** Uh, DT tilted by DX is still T2 minus T1
[00:37:16:889 - 00:37:18:659] **Speaker 1:** over X2 minus X1.
[00:37:19:629 - 00:37:22:399] **Speaker 1:** DN2 by DX is now going to be positive.
[00:37:22:510 - 00:37:25:800] **Speaker 1:** It's ranging from 0 up to 1.
[00:37:34:189 - 00:37:36:520] **Speaker 1:** As integrating an X.
[00:37:42:600 - 00:37:44:879] **Speaker 1:** We can do the same trick, where we chuck all
[00:37:44:879 - 00:37:47:699] **Speaker 1:** these values outside the integral, and we've got T2 minus
[00:37:47:699 - 00:37:48:239] **Speaker 1:** T1.
[00:37:49:060 - 00:37:52:179] **Speaker 1:** Divided by X2 minus X1 2.
[00:37:53:699 - 00:37:55:540] **Speaker 1:** Integrating one.
[00:37:57:360 - 00:38:01:239] **Speaker 1:** And we're left with T2 minus T1 over X2 minus
[00:38:01:239 - 00:38:01:800] **Speaker 1:** X1.
[00:38:02:989 - 00:38:03:870] **Speaker 1:** For I cool.
[00:38:15:959 - 00:38:19:580] **Speaker 1:** So we've done a few bits and pieces and now
[00:38:19:580 - 00:38:21:060] **Speaker 1:** we're trying to summarise what we've done.
[00:38:21:500 - 00:38:23:260] **Speaker 1:** So we're gonna put it in matrix form.
[00:38:27:030 - 00:38:33:340] **Speaker 1:** We looked at Pretty much to the left-hand side of
[00:38:33:340 - 00:38:33:969] **Speaker 1:** this equation.
[00:38:34:449 - 00:38:36:709] **Speaker 1:** We look, we look, we did integration by parts and
[00:38:36:709 - 00:38:38:479] **Speaker 1:** we evaluated these, these terms.
[00:38:39:870 - 00:38:47:679] **Speaker 1:** So what we're left with is All the contributions from.
[00:38:48:510 - 00:38:52:780] **Speaker 1:** This equation And we're not touching the source term yet,
[00:38:52:820 - 00:38:54:820] **Speaker 1:** and that's why it ends up as an extra term
[00:38:54:820 - 00:38:55:439] **Speaker 1:** on the right.
[00:38:57:489 - 00:39:04:270] **Speaker 1:** So I've got T1.
[00:39:07:030 - 00:39:09:149] **Speaker 1:** And minus T2.
[00:39:10:040 - 00:39:12:860] **Speaker 1:** Divided by X2 minus X1 for i equal 1.
[00:39:14:419 - 00:39:16:300] **Speaker 1:** And we have.
[00:39:17:879 - 00:39:18:939] **Speaker 1:** -1.
[00:39:19:719 - 00:39:22:360] **Speaker 1:** Plus T2 over X2 minus X1.
[00:39:24:969 - 00:39:28:610] **Speaker 1:** And the right-hand side we've got minus DT tilda by
[00:39:28:610 - 00:39:31:879] **Speaker 1:** DX at X1 and DT tilda by DX at X2.
[00:39:31:929 - 00:39:33:689] **Speaker 1:** So you can think of this as sort of like
[00:39:33:689 - 00:39:35:649] **Speaker 1:** the effect of the boundary condition being applied at those
[00:39:35:649 - 00:39:36:149] **Speaker 1:** ends.
[00:39:37:750 - 00:39:39:550] **Speaker 1:** Uh, and we've got the elements of matrix on the
[00:39:39:550 - 00:39:42:149] **Speaker 1:** left and the source term of the forcing factor on
[00:39:42:149 - 00:39:42:750] **Speaker 1:** the right.
[00:39:44:479 - 00:39:48:199] **Speaker 1:** So, In my defence, I didn't, I didn't prepare the,
[00:39:48:300 - 00:39:52:780] **Speaker 1:** the structure of these notes, but I think it gives
[00:39:52:780 - 00:39:54:699] **Speaker 1:** you a good indication of how to do each step.
[00:39:55:100 - 00:39:56:939] **Speaker 1:** When we go through some examples, hopefully it'll be a
[00:39:56:939 - 00:39:59:899] **Speaker 1:** bit clearer, ah in terms of the workflow, uh but
[00:39:59:899 - 00:40:01:820] **Speaker 1:** for now we're just going through every single little step.
[00:40:04:949 - 00:40:08:050] **Speaker 1:** So this set of equations are the element equations.
[00:40:09:169 - 00:40:10:010] **Speaker 1:** For element one.
[00:40:16:419 - 00:40:18:510] **Speaker 1:** So all of that work and we've done one element.
[00:40:22:070 - 00:40:22:639] **Speaker 1:** Awesome.
[00:40:24:560 - 00:40:25:909] **Speaker 1:** So we'll go through an example now.
[00:40:29:409 - 00:40:31:449] **Speaker 1:** The other elements are easy because it's just copy paste,
[00:40:31:530 - 00:40:32:330] **Speaker 1:** so don't worry too much.
[00:40:33:010 - 00:40:34:560] **Speaker 1:** So this one we're gonna look at the element equations
[00:40:34:560 - 00:40:37:330] **Speaker 1:** for a rod with a length of 10 centimetres and
[00:40:37:330 - 00:40:39:270] **Speaker 1:** some boundary conditions on the left and right of Derek
[00:40:39:270 - 00:40:39:610] **Speaker 1:** clay.
[00:40:39:729 - 00:40:42:689] **Speaker 1:** So they're fixed at T0 equal to 40 and TL
[00:40:42:689 - 00:40:43:810] **Speaker 1:** equal to 200.
[00:40:44:689 - 00:40:46:409] **Speaker 1:** And we've got a uniform heat source of 10.
[00:40:48:060 - 00:40:52:909] **Speaker 1:** Uh, we're gonna have elements spaces of 2.5 centimetres, so
[00:40:52:909 - 00:40:55:550] **Speaker 1:** we're gonna have 4 elements, and the governing equation we
[00:40:55:550 - 00:41:01:709] **Speaker 1:** have is D2T by DX2 plus 10 equal to 0.
[00:41:19:860 - 00:41:22:580] **Speaker 1:** So it's quite handy to try and visualise what you're,
[00:41:23:020 - 00:41:23:719] **Speaker 1:** what you're doing.
[00:41:24:649 - 00:41:25:989] **Speaker 1:** Otherwise you can get a bit lost.
[00:41:28:070 - 00:41:30:209] **Speaker 1:** I'll, I, I get lost, you might not.
[00:41:30:590 - 00:41:35:149] **Speaker 1:** So we've got elements 123 and 4.
[00:41:35:510 - 00:41:38:070] **Speaker 1:** Our interval is from 0 up to 10.
[00:41:40:149 - 00:41:41:969] **Speaker 1:** Uh, we've got nodes.
[00:41:43:260 - 00:41:49:239] **Speaker 1:** Add X1, X2, X3, X4, and X5, so we've got
[00:41:49:239 - 00:41:50:260] **Speaker 1:** 5 degrees of freedom.
[00:41:53:399 - 00:41:57:120] **Speaker 1:** We've got temperature values on the left of 40.
[00:41:58:510 - 00:42:00:669] **Speaker 1:** And on the right there's 200.
[00:42:09:919 - 00:42:13:699] **Speaker 1:** So without the source term, What would you expect the
[00:42:13:699 - 00:42:14:479] **Speaker 1:** solution to be?
[00:42:15:030 - 00:42:18:550] **Speaker 1:** And, well, it is steady state, there's no time dependence.
[00:42:33:250 - 00:42:37:870] **Speaker 1:** If we integrate The governing equation twice.
[00:42:38:310 - 00:42:39:189] **Speaker 1:** We've got a line.
[00:42:39:989 - 00:42:42:739] **Speaker 1:** Between the two boundary conditions, so it's just a linear
[00:42:43:580 - 00:42:45:899] **Speaker 1:** uh temperature profile from 40 up to 200.
[00:42:46:260 - 00:42:47:560] **Speaker 1:** So that's what we'd expect.
[00:42:47:840 - 00:42:49:800] **Speaker 1:** Uh, what do we expect if we had a source
[00:42:49:800 - 00:42:50:209] **Speaker 1:** term?
[00:42:51:780 - 00:42:52:330] **Speaker 1:** Of Tim.
[00:42:53:280 - 00:42:56:989] **Speaker 1:** What does that do to our Solution.
[00:43:16:100 - 00:43:18:060] **Speaker 1:** If we had a rod and we added heat, that's
[00:43:18:060 - 00:43:18:840] **Speaker 1:** not a trick question.
[00:43:19:179 - 00:43:20:719] **Speaker 1:** What, what do you expect would happen?
[00:43:22:580 - 00:43:23:340] **Speaker 1:** Yeah, it would get hotter.
[00:43:23:429 - 00:43:26:070] **Speaker 1:** So I mean it's a uniform sources in across the
[00:43:26:070 - 00:43:26:699] **Speaker 1:** whole interval.
[00:43:27:389 - 00:43:29:729] **Speaker 1:** So we expect the temperature profile to be higher.
[00:43:30:949 - 00:43:33:000] **Speaker 1:** Uh, than, than that line.
[00:43:33:120 - 00:43:35:639] **Speaker 1:** So again, it's really important to try and visualise and
[00:43:35:639 - 00:43:38:639] **Speaker 1:** think about what solution you're expecting before you embark on
[00:43:38:639 - 00:43:44:239] **Speaker 1:** your, your, well, analytical or your numerical, uh, solution path.
[00:43:45:080 - 00:43:47:639] **Speaker 1:** So for element one, we're gonna calculate that source stem.
[00:43:49:419 - 00:43:50:709] **Speaker 1:** So that's this, this guy.
[00:43:51:780 - 00:43:53:639] **Speaker 1:** So evaluating.
[00:43:55:520 - 00:43:58:100] **Speaker 1:** F N 1 D X.
[00:43:59:300 - 00:44:01:100] **Speaker 1:** If we said was equal to 10, it's not changing
[00:44:01:100 - 00:44:01:580] **Speaker 1:** with space.
[00:44:01:780 - 00:44:03:729] **Speaker 1:** So can we talk outside derivatives.
[00:44:03:780 - 00:44:06:580] **Speaker 1:** So we've got 10 times the integral.
[00:44:07:530 - 00:44:10:229] **Speaker 1:** Of N1DX.
[00:44:13:820 - 00:44:16:050] **Speaker 1:** If you recall, we can do lots of algebra if
[00:44:16:050 - 00:44:18:459] **Speaker 1:** we want and substitute in the expression for N1, or
[00:44:18:459 - 00:44:21:639] **Speaker 1:** we can observe that it's just the, the area under
[00:44:22:340 - 00:44:23:800] **Speaker 1:** the shape element which is a triangle.
[00:44:24:219 - 00:44:25:370] **Speaker 1:** So half the base times the height.
[00:44:25:459 - 00:44:28:979] **Speaker 1:** So we've got 10 times half the base which is
[00:44:28:979 - 00:44:30:100] **Speaker 1:** X2 minus X1.
[00:44:31:340 - 00:44:33:179] **Speaker 1:** Times the height, which is one.
[00:44:33:469 - 00:44:34:580] **Speaker 1:** We can put that in if you want.
[00:44:35:770 - 00:44:37:350] **Speaker 1:** So this is 10/2.
[00:44:40:889 - 00:44:45:070] **Speaker 1:** Multiplied by delta X, which we said was 2.5 centimetres.
[00:44:53:360 - 00:44:55:290] **Speaker 1:** And this is 12.5.
[00:45:00:040 - 00:45:01:189] **Speaker 1:** So that was that first term.
[00:45:02:989 - 00:45:07:100] **Speaker 1:** For our element Now we're looking at FN2.
[00:45:16:879 - 00:45:19:479] **Speaker 1:** We will do the same trick, 10 in front.
[00:45:25:469 - 00:45:30:000] **Speaker 1:** Um, The shape element N2 is just a mirror image.
[00:45:31:570 - 00:45:33:780] **Speaker 1:** Of shape function in one, they both have the same
[00:45:33:780 - 00:45:35:139] **Speaker 1:** area under the curve.
[00:45:36:090 - 00:45:38:290] **Speaker 1:** So we're gonna have the same value of 12.5.
[00:45:40:030 - 00:45:42:709] **Speaker 1:** If you're not convinced, you can do the maths, but
[00:45:44:419 - 00:45:45:459] **Speaker 1:** They're gonna be the same value.
[00:45:46:510 - 00:45:49:510] **Speaker 1:** So now we can summarise again our element equations for
[00:45:49:510 - 00:45:50:189] **Speaker 1:** element one.
[00:45:50:750 - 00:45:51:489] **Speaker 1:** So we've got.
[00:45:55:580 - 00:45:59:080] **Speaker 1:** 1 over delta X, so 1 over 2.5.
[00:46:02:929 - 00:46:04:320] **Speaker 1:** Multiplied by D1.
[00:46:06:550 - 00:46:10:070] **Speaker 1:** And we've got -1 over x, so 1 over 2.5
[00:46:10:070 - 00:46:10:469] **Speaker 1:** T2.
[00:46:11:679 - 00:46:14:659] **Speaker 1:** And on the right-hand side, we had the minus DT
[00:46:14:659 - 00:46:19:520] **Speaker 1:** tilda by DX at X1 plus the source term 12.5.
[00:46:23:590 - 00:46:25:379] **Speaker 1:** Uh, that 2nd equation.
[00:46:26:889 - 00:46:30:300] **Speaker 1:** Is going to be -1/2.5. If we calculate that it's
[00:46:30:300 - 00:46:31:000] **Speaker 1:** 0.4.
[00:46:33:040 - 00:46:34:679] **Speaker 1:** Plus 0.4 T2.
[00:46:35:570 - 00:46:38:290] **Speaker 1:** You've got a positive DT total by the X at
[00:46:38:290 - 00:46:41:560] **Speaker 1:** X2 + 12.5.
[00:46:47:850 - 00:46:49:810] **Speaker 1:** The last step here is to chuck it back into
[00:46:49:810 - 00:46:51:889] **Speaker 1:** matrix format, so it's a bit easier to read.
[00:46:52:489 - 00:46:53:350] **Speaker 1:** So we've got T1.
[00:46:54:899 - 00:46:58:879] **Speaker 1:** And to As the nodal values or the unknowns that
[00:46:58:879 - 00:46:59:820] **Speaker 1:** we're trying to solve for.
[00:47:01:070 - 00:47:05:860] **Speaker 1:** Uh, the local stiffness matrix for element one, so that's
[00:47:05:860 - 00:47:11:209] **Speaker 1:** the K E one, is going to be these coefficients.
[00:47:11:550 - 00:47:12:889] **Speaker 1:** So I've got 0.4.
[00:47:14:449 - 00:47:16:770] **Speaker 1:** On the diagonal and on the other diagonal we've got
[00:47:16:770 - 00:47:22:340] **Speaker 1:** -0.4. And on the right-hand side, we've got minus DT
[00:47:22:340 - 00:47:28:909] **Speaker 1:** tilta by DX add X1 + 12.5, and DT tota
[00:47:28:909 - 00:47:30:629] **Speaker 1:** by DX at X2.
[00:47:31:560 - 00:47:33:580] **Speaker 1:** Plus 12.5.
[00:47:48:830 - 00:47:50:699] **Speaker 1:** I think that's enough writing for today.
[00:47:52:149 - 00:47:55:459] **Speaker 1:** Um, we can Do the same for elements 23 and
[00:47:55:459 - 00:47:58:699] **Speaker 1:** 4, so you can do that for homework if you
[00:47:58:699 - 00:48:00:899] **Speaker 1:** want, um, but we'll finish off tomorrow.
[00:48:01:300 - 00:48:04:090] **Speaker 1:** Um, the only difference between each element is the nodal
[00:48:04:090 - 00:48:06:219] **Speaker 1:** values that that correspond to each element.
[00:48:06:340 - 00:48:09:340] **Speaker 1:** So here we're looking at element 1, we've got X1
[00:48:09:340 - 00:48:09:979] **Speaker 1:** and X2.
[00:48:10:729 - 00:48:14:090] **Speaker 1:** Um, element 2 has X2, X3, T2, T3, so you're
[00:48:14:090 - 00:48:15:689] **Speaker 1:** just gonna swap out those numbers essentially.
[00:48:16:489 - 00:48:18:679] **Speaker 1:** So if you're on an exam or something, you don't
[00:48:18:679 - 00:48:21:969] **Speaker 1:** want to go through every single, Uh, element in the
[00:48:21:969 - 00:48:24:729] **Speaker 1:** same rigour, you, you do one and then you sort
[00:48:24:729 - 00:48:25:770] **Speaker 1:** of copy paste for the others.
[00:48:30:959 - 00:48:34:399] **Speaker 1:** Alright, I think that just about does it for today.
[00:48:34:719 - 00:48:36:580] **Speaker 1:** Um, so we've got the labs this afternoon.
[00:48:37:080 - 00:48:38:379] **Speaker 1:** I'll try and be there.
[00:48:38:590 - 00:48:40:479] **Speaker 1:** I think I've just got a meeting at 2.
[00:48:41:350 - 00:48:43:350] **Speaker 1:** So work through lab 5.
[00:48:44:370 - 00:48:46:459] **Speaker 1:** And bring on Christian for the assignment.
[00:48:46:780 - 00:48:48:500] **Speaker 1:** I think some of you have started the assignment, so
[00:48:48:500 - 00:48:49:320] **Speaker 1:** that's brilliant.
[00:48:49:739 - 00:48:51:419] **Speaker 1:** It's not, not too far away now.
[00:48:52:080 - 00:48:56:550] **Speaker 1:** Um And we'll finish off this chapter tomorrow.
[00:48:58:370 - 00:48:58:729] **Speaker 1:** Cool.
[00:48:59:949 - 00:49:00:189] **Speaker 1:** See.
[00:49:30:030 - 00:49:42:129] **Speaker 1:** I OK, yeah, so.
[00:49:43:560 - 00:49:43:709] **Speaker 0:** Just like the first part of it.
[00:49:46:780 - 00:49:47:000] **Speaker 0:** I finished it.
[00:49:47:449 - 00:49:49:649] **Speaker 0:** How big of a difference do you expect?
[00:49:51:590 - 00:49:52:810] **Speaker 1:** I mean, they should be pretty close.
[00:49:53:739 - 00:49:53:760] **Speaker 1:** I mean.
[00:49:55:260 - 00:49:58:689] **Speaker 1:** That quite, quite, that sounds pretty close, doesn't it?
[00:49:59:070 - 00:49:59:419] **Speaker 1:** Yeah.
[00:50:00:590 - 00:50:02:709] **Speaker 0:** Yeah, I was just wondering if you should expect it
[00:50:02:709 - 00:50:03:560] **Speaker 1:** to be way closer.
[00:50:04:020 - 00:50:05:120] **Speaker 1:** What percentage is that?
[00:50:05:479 - 00:50:07:149] **Speaker 1:** I think it's like uh.
[00:50:07:969 - 00:50:17:020] **Speaker 0:** 0 0.15%. Yeah, well, that's nice that's there might be
[00:50:17:020 - 00:50:17:090] **Speaker 1:** a little cool, thank you.
[00:50:17:649 - 00:50:21:899] **Speaker 2:** Um, and that last bit here is, should that be
[00:50:21:899 - 00:50:25:459] **Speaker 2:** negative 12.5 because you've gone.
[00:50:27:020 - 00:50:30:070] **Speaker 1:** Uh, in terms of Like for both of them or
[00:50:30:070 - 00:50:30:610] **Speaker 1:** for one of them?
[00:50:30:679 - 00:50:32:010] **Speaker 1:** No, because they're gonna be both the same.
[00:50:32:449 - 00:50:35:689] **Speaker 2:** Just for this one because you're negative here and for
[00:50:35:689 - 00:50:36:959] **Speaker 2:** the sign, for the sign.
[00:50:37:010 - 00:50:38:169] **Speaker 2:** This is a different equation.
[00:50:38:290 - 00:50:39:100] **Speaker 1:** Oh, is it?
[00:50:39:570 - 00:50:42:010] **Speaker 1:** So that one was for this guy.
[00:50:42:810 - 00:50:45:530] **Speaker 1:** Oh, OK, yeah, yeah, yeah, yeah, yeah, yeah, yeah, yeah,
[00:50:45:610 - 00:50:46:379] **Speaker 1:** yeah, yeah, yeah, yeah.
[00:50:47:409 - 00:50:47:419] **Speaker 0:** S.
[00:50:48:800 - 00:50:49:199] **Speaker 0:** How you doing?
[00:50:49:780 - 00:50:49:790] **Speaker 0:** Good.
[00:50:49:889 - 00:50:50:189] **Speaker 0:** How are you?
[00:52:48:330 - 00:53:17:280] **Speaker 0:** Oh You have to, um, What I think I think
[00:53:17:280 - 00:53:20:360] **Speaker 0:** I've heard people try to argue that it means like.
[00:53:26:530 - 00:53:26:939] **Speaker 0:** Yes.
[00:53:30:750 - 00:53:31:050] **Speaker 0:** see this.
[00:53:33:179 - 00:53:37:659] **Speaker 0:** finally The US.
[00:53:45:780 - 00:53:46:449] **Speaker 0:** Oh it's true.
[00:53:48:439 - 00:53:48:709] **Speaker 0:** Oh.
[00:53:54:209 - 00:53:54:219] **Speaker 0:** good.
[00:53:59:280 - 00:53:59:899] **Speaker 0:** so we just get.
[00:54:04:000 - 00:54:04:020] **Speaker 0:** You have.
[00:54:06:060 - 00:54:06:610] **Speaker 0:** On top of that.
[00:54:07:590 - 00:54:07:639] **Speaker 0:** Just.
[00:54:13:250 - 00:54:25:080] **Speaker 0:** Yeah And she like offended you like.
[00:54:26:000 - 00:54:27:149] **Speaker 0:** It's like broiling the new.
[00:54:40:899 - 00:54:48:219] **Speaker 0:** I think she's It is some good people.
[00:54:49:659 - 00:54:58:169] **Speaker 0:** have like American

# ENME302-26S2 Lecture 28 native Echo transcript

Date: September 11, 2026 11:00am-11:55am
Transcript type: native Echo automated transcript.

[00:00:05:800 - 00:00:05:809] **Speaker 0:** I.
[00:00:35:169 - 00:00:36:080] **Speaker 0:** Yeah, I know, I know I.
[00:00:51:229 - 00:01:04:309] **Speaker 0:** I Uh, good morning.
[00:01:04:470 - 00:01:05:319] **Speaker 1:** We'll make a start.
[00:01:08:319 - 00:01:12:879] **Speaker 1:** So yesterday we were going through and looked at a
[00:01:12:879 - 00:01:16:360] **Speaker 1:** non-uniform based um grid for our finite difference scheme, and
[00:01:16:360 - 00:01:19:319] **Speaker 1:** we applied that to the, the curved boundary just to
[00:01:19:319 - 00:01:23:080] **Speaker 1:** check that we can still apply these same techniques, um.
[00:01:24:300 - 00:01:24:760] **Speaker 1:** Fuzzy.
[00:01:25:519 - 00:01:29:580] **Speaker 1:** So That almost concludes our chapter 4, so we're doing
[00:01:29:580 - 00:01:30:720] **Speaker 1:** good for timing.
[00:01:31:059 - 00:01:34:269] **Speaker 1:** Um, but just to summarise, we Did the first order
[00:01:34:269 - 00:01:34:809] **Speaker 1:** derivative.
[00:01:37:000 - 00:01:39:459] **Speaker 1:** At the midpoints A and B, and then we took
[00:01:39:459 - 00:01:42:250] **Speaker 1:** a derivative of the derivative to get the second order
[00:01:42:250 - 00:01:43:000] **Speaker 1:** derivative.
[00:01:43:559 - 00:01:46:519] **Speaker 1:** So DT by DX at A and B and then
[00:01:46:519 - 00:01:48:260] **Speaker 1:** we took the difference rise over run.
[00:01:48:400 - 00:01:51:599] **Speaker 1:** So gamma being the displacement between points A and B.
[00:01:52:580 - 00:01:53:550] **Speaker 1:** So that's the gist of it.
[00:01:53:809 - 00:01:56:370] **Speaker 1:** We can rearrange and we get equation 10 and we
[00:01:56:370 - 00:01:59:410] **Speaker 1:** do the same in Y and that's equation 11.
[00:01:59:690 - 00:02:02:610] **Speaker 1:** We combine into our Laplace equation and this is our
[00:02:02:610 - 00:02:03:610] **Speaker 1:** discretized form.
[00:02:04:319 - 00:02:06:489] **Speaker 1:** If you set alpha one.
[00:02:07:599 - 00:02:09:949] **Speaker 1:** And alpha 2 equal to 1, if it was just
[00:02:10:240 - 00:02:12:919] **Speaker 1:** constant values of the X for the spacings, you should
[00:02:12:919 - 00:02:15:630] **Speaker 1:** recover the same, uh, finite different sensor that we derived
[00:02:15:630 - 00:02:15:899] **Speaker 1:** earlier.
[00:02:17:770 - 00:02:20:350] **Speaker 1:** So that's That's that.
[00:02:20:550 - 00:02:24:350] **Speaker 1:** Any, any questions on finite differenceferencing as we've done, done
[00:02:24:350 - 00:02:24:889] **Speaker 1:** so far?
[00:02:32:690 - 00:02:33:089] **Speaker 1:** No.
[00:02:33:800 - 00:02:34:160] **Speaker 1:** All right.
[00:02:34:990 - 00:02:37:869] **Speaker 1:** Um So that's the end of chapter 4.
[00:02:37:949 - 00:02:41:210] **Speaker 1:** There's a couple of exercises at the end, uh, which
[00:02:41:309 - 00:02:43:369] **Speaker 1:** we could go through a little bit by hand and,
[00:02:43:429 - 00:02:45:589] **Speaker 1:** and work through some of these problems.
[00:02:46:179 - 00:02:49:119] **Speaker 1:** Um, I want to go through a couple of Tips
[00:02:49:119 - 00:02:52:339] **Speaker 1:** and tricks I guess with console, uh, based on what
[00:02:52:839 - 00:02:56:690] **Speaker 1:** some of the questions from yesterday, uh, was, was given.
[00:02:57:309 - 00:02:59:029] **Speaker 1:** Uh, but then the rest of the lecture, we can
[00:02:59:029 - 00:03:01:910] **Speaker 1:** either go through some of these exercises or the exercises
[00:03:01:910 - 00:03:03:669] **Speaker 1:** in the earlier chapter if you're stuck with some in
[00:03:03:669 - 00:03:06:309] **Speaker 1:** particular, or we can head on with chapter 5.
[00:03:06:429 - 00:03:07:350] **Speaker 1:** So it'll be up to you.
[00:03:07:470 - 00:03:08:949] **Speaker 1:** I'll give you a few minutes to think about it
[00:03:08:949 - 00:03:09:759] **Speaker 1:** as we go through console.
[00:03:12:699 - 00:03:28:389] **Speaker 1:** So OK, cool.
[00:03:28:649 - 00:03:29:490] **Speaker 1:** So this is console.
[00:03:29:850 - 00:03:32:990] **Speaker 1:** And The quiz.
[00:03:33:589 - 00:03:37:130] **Speaker 1:** So the question was, um, around the constraint groups.
[00:03:37:389 - 00:03:40:070] **Speaker 1:** So we can open up the cantilever under the application
[00:03:40:070 - 00:03:42:190] **Speaker 1:** library, just so we don't have to create it from
[00:03:42:190 - 00:03:42:809] **Speaker 1:** scratch.
[00:03:43:839 - 00:03:50:789] **Speaker 1:** Um And the purpose of using those constraint groups, uh,
[00:03:50:919 - 00:03:51:250] **Speaker 1:** so.
[00:03:51:919 - 00:03:54:000] **Speaker 1:** Because we were looking at two distinct cases.
[00:03:54:779 - 00:03:56:520] **Speaker 1:** And hopefully that will load up shortly.
[00:04:05:360 - 00:04:07:039] **Speaker 1:** And I'll just open that PDF document.
[00:04:12:279 - 00:04:14:729] **Speaker 1:** Always takes longer when people are watching, but.
[00:04:15:660 - 00:04:18:260] **Speaker 1:** This is the, the tutorial that you went through yesterday
[00:04:18:260 - 00:04:20:290] **Speaker 1:** or earlier in the week, and we looked at two
[00:04:20:290 - 00:04:20:940] **Speaker 1:** different cases.
[00:04:21:058 - 00:04:25:000] **Speaker 1:** We looked at just by gravity, what the cantilever deflects,
[00:04:25:260 - 00:04:27:119] **Speaker 1:** uh, subject to a fixed constraint on the left.
[00:04:27:420 - 00:04:28:980] **Speaker 1:** And then we looked at another set of boundary conditions
[00:04:28:980 - 00:04:31:660] **Speaker 1:** on the right where we applied a force on the
[00:04:31:660 - 00:04:34:380] **Speaker 1:** right-hand boundary, and we don't want AI to go away.
[00:04:36:589 - 00:04:39:109] **Speaker 1:** Um, so force on the right, and then we've got
[00:04:39:109 - 00:04:40:619] **Speaker 1:** a pin joint and then a roller.
[00:04:40:670 - 00:04:42:329] **Speaker 1:** So those are the boundary conditions that you applied.
[00:04:42:630 - 00:04:44:709] **Speaker 1:** Because there were two different cases, we could have created
[00:04:44:709 - 00:04:47:929] **Speaker 1:** two console models and then done one and then another.
[00:04:48:660 - 00:04:51:700] **Speaker 1:** Uh, the advantage of using those constraint groups was that
[00:04:51:700 - 00:04:55:059] **Speaker 1:** we could analyse the results alongside each other.
[00:04:55:380 - 00:05:19:450] **Speaker 1:** So if you open that model, And we have our
[00:05:21:309 - 00:05:22:649] **Speaker 1:** Load groups and constraints.
[00:05:22:869 - 00:05:25:790] **Speaker 1:** So we had one load group for gravity, one for
[00:05:25:790 - 00:05:28:450] **Speaker 1:** force, constraint groups for gravity and force.
[00:05:28:910 - 00:05:32:910] **Speaker 1:** Under step one stationary, we defined which cases we wanted
[00:05:32:910 - 00:05:36:269] **Speaker 1:** to analyse and which constraint groups and forces that we
[00:05:36:269 - 00:05:37:910] **Speaker 1:** wanted to include, so that's where we ticked.
[00:05:38:739 - 00:05:42:500] **Speaker 1:** Um, and then under normal stress, we could select from
[00:05:42:500 - 00:05:45:019] **Speaker 1:** our solution data set study one, which is the only
[00:05:45:019 - 00:05:46:880] **Speaker 1:** solver that we've we've set up.
[00:05:47:109 - 00:05:49:739] **Speaker 1:** So solution one, and then the load case can be
[00:05:49:739 - 00:05:52:500] **Speaker 1:** chosen, uh, can be picked between gravity and force.
[00:05:52:820 - 00:05:55:450] **Speaker 1:** So that, that's, I guess the advantage of using these
[00:05:55:450 - 00:05:56:299] **Speaker 1:** constraint groups.
[00:05:57:170 - 00:05:59:019] **Speaker 1:** Arguably again, you can just use a whole new model.
[00:05:59:329 - 00:06:01:769] **Speaker 1:** So for the quiz, you're most welcome to create another
[00:06:01:769 - 00:06:06:119] **Speaker 1:** set of uh load and constraint groups and run with
[00:06:06:119 - 00:06:07:769] **Speaker 1:** another case if you want.
[00:06:08:130 - 00:06:10:200] **Speaker 1:** It might be a little bit more complicated than, than
[00:06:10:200 - 00:06:13:410] **Speaker 1:** what I intended or or thought might be easier.
[00:06:13:529 - 00:06:14:790] **Speaker 1:** It's just to create a new model.
[00:06:15:829 - 00:06:17:579] **Speaker 1:** And follow the steps in that quiz question.
[00:06:17:649 - 00:06:19:910] **Speaker 1:** So if you're stuck, uh, just create a new model.
[00:06:20:230 - 00:06:22:649] **Speaker 1:** Don't worry about these constraint groups cause we're only looking
[00:06:22:649 - 00:06:24:350] **Speaker 1:** at analysing one load case.
[00:06:25:149 - 00:06:29:019] **Speaker 1:** Um And it should, should just clear things up.
[00:06:30:350 - 00:06:32:029] **Speaker 1:** There's a question on whether or not we're including gravity.
[00:06:32:070 - 00:06:35:709] **Speaker 1:** I didn't include gravity in the quiz question, so, so
[00:06:35:709 - 00:06:37:790] **Speaker 1:** don't include it, but you could include it and then
[00:06:37:790 - 00:06:40:029] **Speaker 1:** just check does it impact the result very much?
[00:06:40:350 - 00:06:41:279] **Speaker 1:** Does it make sense?
[00:06:41:790 - 00:06:44:070] **Speaker 1:** Uh, we've applied quite a heavy load on the far
[00:06:44:070 - 00:06:44:450] **Speaker 1:** side.
[00:06:45:239 - 00:06:48:920] **Speaker 1:** Does the mass of the cantilever contribute significantly to the
[00:06:48:920 - 00:06:49:640] **Speaker 1:** defections?
[00:06:50:470 - 00:06:53:029] **Speaker 1:** Um, but then don't include it because I didn't include
[00:06:53:029 - 00:06:54:829] **Speaker 1:** it in the answer, just to make sure you get
[00:06:54:829 - 00:06:55:290] **Speaker 1:** it right.
[00:06:55:790 - 00:06:58:570] **Speaker 1:** Um, I think the tolerance is about 2% on the,
[00:06:58:579 - 00:07:03:470] **Speaker 1:** the questions, so it's not to the, Then, yeah, numeric
[00:07:03:470 - 00:07:06:040] **Speaker 1:** values precisely, like 3 significant figures is.
[00:07:06:769 - 00:07:10:690] **Speaker 1:** Um, precision, not the accuracy required for the, the correct
[00:07:10:690 - 00:07:11:209] **Speaker 1:** answer.
[00:07:16:109 - 00:07:18:980] **Speaker 1:** Uh, one of the steps was using a sweat mesh.
[00:07:37:269 - 00:07:39:980] **Speaker 1:** So I think we helped a couple of your classmates,
[00:07:40:029 - 00:07:42:109] **Speaker 1:** but they've just moved the setting.
[00:07:42:510 - 00:07:45:790] **Speaker 1:** So in 6.4, um, it's a different setting, so.
[00:07:46:769 - 00:07:48:350] **Speaker 1:** Um, I guess we.
[00:07:50:869 - 00:07:53:309] **Speaker 1:** Probably can't do a sweat mash on this, maybe.
[00:08:01:220 - 00:08:02:579] **Speaker 1:** I'll open up the cantilever.
[00:08:04:670 - 00:08:08:910] **Speaker 1:** Rather the Uh, feed the clamp.
[00:08:18:309 - 00:08:22:109] **Speaker 1:** So console updates every so often and then keeps changing
[00:08:22:109 - 00:08:26:140] **Speaker 1:** things, which It can be a bit tricky to keep
[00:08:26:140 - 00:08:26:640] **Speaker 1:** up with.
[00:08:31:470 - 00:08:32:690] **Speaker 1:** Not sure if that's going to.
[00:08:33:820 - 00:08:43:830] **Speaker 1:** R Oh, we'll fill in some time anyway.
[00:08:56:520 - 00:08:59:320] **Speaker 1:** OK, that's, that's the limit of my patience.
[00:08:59:479 - 00:09:02:700] **Speaker 1:** Um, so essentially instead of using the face meshing method,
[00:09:02:909 - 00:09:04:679] **Speaker 1:** um, there's another setting in there, so you can hunt
[00:09:04:679 - 00:09:06:880] **Speaker 1:** if you haven't found that already, but don't be too
[00:09:06:880 - 00:09:07:419] **Speaker 1:** concerned about.
[00:09:08:099 - 00:09:08:700] **Speaker 1:** Sorry about that.
[00:09:10:380 - 00:09:19:940] **Speaker 1:** Um, And Are there any other questions on what we
[00:09:19:940 - 00:09:21:919] **Speaker 1:** did in the lab this week or the quiz?
[00:09:26:650 - 00:09:26:849] **Speaker 1:** No.
[00:09:28:020 - 00:09:29:820] **Speaker 1:** Very quiet, alright, cool.
[00:09:30:099 - 00:09:32:140] **Speaker 1:** So I, I also want to just go through maybe
[00:09:32:140 - 00:09:34:299] **Speaker 1:** setting up the a domain.
[00:09:35:119 - 00:09:37:359] **Speaker 1:** Or a console model for representing us just so that
[00:09:37:359 - 00:09:38:770] **Speaker 1:** we can compare our results.
[00:09:39:369 - 00:09:43:659] **Speaker 1:** So earlier, We looked at.
[00:09:45:190 - 00:09:47:849] **Speaker 1:** Solving that temperature field in chapter 3.
[00:09:51:000 - 00:09:52:780] **Speaker 1:** And I'll find chapter 3.
[00:09:54:380 - 00:09:54:859] **Speaker 1:** Somewhere.
[00:10:02:830 - 00:10:04:690] **Speaker 1:** So we solved the Laplace equation.
[00:10:05:840 - 00:10:09:679] **Speaker 1:** On our square domain, we have these 4 boundary conditions
[00:10:09:679 - 00:10:12:260] **Speaker 1:** and we can model this in console as well.
[00:10:13:440 - 00:10:17:640] **Speaker 1:** So I'll just create a new model, so again selecting
[00:10:17:640 - 00:10:19:369] **Speaker 1:** the 2D spatial dimensions.
[00:10:20:940 - 00:10:23:450] **Speaker 1:** There are some people getting a bit stuck with uh
[00:10:23:460 - 00:10:27:659] **Speaker 1:** finding maximum values using a volume function.
[00:10:28:000 - 00:10:30:179] **Speaker 1:** Whereas if you've got a two-dimensional domain, you can only
[00:10:30:179 - 00:10:32:119] **Speaker 1:** look at a surface being two dimensional.
[00:10:32:450 - 00:10:33:760] **Speaker 1:** Um, so if you're stuck with that.
[00:10:34:700 - 00:10:36:650] **Speaker 1:** So we're going to use the Laplace equation.
[00:10:39:179 - 00:10:41:510] **Speaker 1:** Our dependent variable here is our temperature field.
[00:10:43:119 - 00:10:45:780] **Speaker 1:** And we're going to have units of carbon.
[00:10:49:890 - 00:10:52:530] **Speaker 1:** And the units of the source term is going to
[00:10:52:530 - 00:10:53:770] **Speaker 1:** be carbon per metre squared.
[00:10:59:000 - 00:11:00:320] **Speaker 1:** The pass is only in city-state.
[00:11:00:359 - 00:11:04:179] **Speaker 1:** It has no time dependence, so that's our only option.
[00:11:09:369 - 00:11:11:489] **Speaker 1:** And if we want to set up some domain, I
[00:11:11:489 - 00:11:14:169] **Speaker 1:** don't think we've got a size for this, but we
[00:11:14:169 - 00:11:15:229] **Speaker 1:** might have in Python.
[00:11:15:929 - 00:11:17:979] **Speaker 1:** So we'll just set up to be a unit square.
[00:11:24:479 - 00:11:26:799] **Speaker 1:** And because it is a square, we can use a
[00:11:26:799 - 00:11:27:700] **Speaker 1:** nice structured grid.
[00:11:28:390 - 00:11:31:799] **Speaker 1:** So we've got 1234 elements in each direction.
[00:11:33:460 - 00:11:38:219] **Speaker 1:** So mapped With a distribution.
[00:11:39:429 - 00:11:41:059] **Speaker 1:** Of 4 elements in each.
[00:11:42:840 - 00:11:46:929] **Speaker 1:** Direction Again, console is using finite element method rather than
[00:11:46:929 - 00:11:47:609] **Speaker 1:** finite differencing.
[00:11:47:690 - 00:11:50:530] **Speaker 1:** So there are different numerical methods, but we should be
[00:11:50:530 - 00:11:51:710] **Speaker 1:** getting a similar result.
[00:11:54:090 - 00:11:56:390] **Speaker 1:** The boundary conditions that we have are 4 direct clay
[00:11:56:390 - 00:11:58:669] **Speaker 1:** boundary conditions, so 0 along the bottom.
[00:12:02:349 - 00:12:04:969] **Speaker 1:** And we can fight 0 °C.
[00:12:06:650 - 00:12:10:380] **Speaker 1:** Rather than keeping it at 0 Kelvin or trying to
[00:12:10:380 - 00:12:11:520] **Speaker 1:** add 273.
[00:12:11:809 - 00:12:12:460] **Speaker 1:** some numbers.
[00:12:13:010 - 00:12:15:969] **Speaker 1:** So using the units and square brackets is really helpful
[00:12:15:969 - 00:12:16:609] **Speaker 1:** in console.
[00:12:16:890 - 00:12:20:030] **Speaker 1:** So some of you got stuck with um, Some of
[00:12:20:030 - 00:12:23:400] **Speaker 1:** the boundary loads being applied in Newtons rather than mega-Newtons,
[00:12:23:450 - 00:12:25:570] **Speaker 1:** so that sends the six out, so that's quite different.
[00:12:26:070 - 00:12:28:349] **Speaker 1:** So when you get your results at the end, when
[00:12:28:349 - 00:12:31:659] **Speaker 1:** you interpret them, um, yeah, think about whether or not
[00:12:31:659 - 00:12:32:349] **Speaker 1:** it makes sense.
[00:12:32:750 - 00:12:35:210] **Speaker 1:** Has a deflection of Pantility actually moved at all?
[00:12:36:349 - 00:12:39:030] **Speaker 1:** So 0 degrees on the bottom, uh 75 on the
[00:12:39:030 - 00:12:39:489] **Speaker 1:** left.
[00:12:50:609 - 00:12:52:510] **Speaker 1:** And 100 on the top.
[00:12:58:419 - 00:12:59:219] **Speaker 1:** And.
[00:13:02:219 - 00:13:03:409] **Speaker 1:** 50 on the right.
[00:13:10:750 - 00:13:12:940] **Speaker 1:** So we've got our boundary conditions.
[00:13:13:140 - 00:13:16:679] **Speaker 1:** Our equation that we're solving is our Laplace equation.
[00:13:17:099 - 00:13:19:219] **Speaker 1:** So grade 2 T.
[00:13:20:330 - 00:13:21:909] **Speaker 1:** Um, equal to 0.
[00:13:23:590 - 00:13:26:539] **Speaker 1:** Our initial values is the initial gifts, essentially.
[00:13:27:440 - 00:13:28:859] **Speaker 1:** Uh, it doesn't matter too much.
[00:13:30:039 - 00:13:31:280] **Speaker 1:** And we compute.
[00:13:31:880 - 00:13:34:479] **Speaker 1:** So we've essentially set up all of our equations.
[00:13:34:599 - 00:13:36:270] **Speaker 1:** Again, it's going to be finite elements instead of finite
[00:13:36:270 - 00:13:38:440] **Speaker 1:** difference, but we set up our system of equations and
[00:13:38:440 - 00:13:39:179] **Speaker 1:** we solve.
[00:13:39:799 - 00:13:42:059] **Speaker 1:** And then to visualise, we've got our temperature field here.
[00:13:43:299 - 00:13:45:900] **Speaker 1:** Uh, so by default, it's in Kelvin, so it might
[00:13:45:900 - 00:13:48:659] **Speaker 1:** be easier to interpret by changing the units to degrees
[00:13:48:659 - 00:13:49:320] **Speaker 1:** Celsius.
[00:13:53:280 - 00:13:56:159] **Speaker 1:** And hopefully it's going to sort of match what we've.
[00:13:57:179 - 00:13:58:590] **Speaker 1:** Calculated with our finite different scheme.
[00:13:58:789 - 00:14:01:369] **Speaker 1:** So in the centre, we had 56.3.
[00:14:01:950 - 00:14:04:700] **Speaker 1:** So if you click on the plot, it will read
[00:14:04:700 - 00:14:07:809] **Speaker 1:** the value that's, that's visualised here.
[00:14:08:299 - 00:14:10:200] **Speaker 1:** Uh, some of you picked up with the feeder clamp
[00:14:10:200 - 00:14:13:289] **Speaker 1:** that The volume shading.
[00:14:15:020 - 00:14:19:979] **Speaker 1:** is less accurate than just calculating with the right values.
[00:14:20:219 - 00:14:22:900] **Speaker 1:** So when you're picking out that peak stress, that's because
[00:14:22:900 - 00:14:26:419] **Speaker 1:** when it's doing interpolation or shading within the body, especially
[00:14:26:419 - 00:14:29:719] **Speaker 1:** for 3D volumes, it'll do an approximation.
[00:14:30:179 - 00:14:32:400] **Speaker 1:** And those approximations are adjusted under quality.
[00:14:33:809 - 00:14:36:890] **Speaker 1:** So in summary, if you're trying to find the maximum
[00:14:36:890 - 00:14:40:809] **Speaker 1:** value within the domain, use derived values or this maximum.
[00:14:42:710 - 00:14:44:429] **Speaker 1:** Uh, plot, so.
[00:14:46:719 - 00:14:50:989] **Speaker 1:** That's, Important.
[00:14:51:159 - 00:14:53:820] **Speaker 1:** So we've got 56.1, uh, so that's, that's pretty much
[00:14:53:820 - 00:14:54:559] **Speaker 1:** what we expect.
[00:14:58:719 - 00:15:00:570] **Speaker 1:** And the other thing I wanted to show in console
[00:15:00:570 - 00:15:03:289] **Speaker 1:** was, once you've run a simulation, you might want to
[00:15:03:289 - 00:15:05:869] **Speaker 1:** save that and then adjust something and then compare it
[00:15:05:869 - 00:15:06:190] **Speaker 1:** again.
[00:15:06:489 - 00:15:09:570] **Speaker 1:** So you can save a data or solution data set
[00:15:09:570 - 00:15:13:849] **Speaker 1:** by right click, right clicking solution one and under solution.
[00:15:15:099 - 00:15:15:539] **Speaker 1:** Copy.
[00:15:17:630 - 00:15:19:450] **Speaker 1:** So you can rename that to something helpful.
[00:15:20:270 - 00:15:25:289] **Speaker 1:** Um I don't know what's going to be helpful here
[00:15:25:289 - 00:15:26:219] **Speaker 1:** but version one.
[00:15:27:619 - 00:15:30:530] **Speaker 1:** so then when you run through again, it's going to
[00:15:30:530 - 00:15:33:239] **Speaker 1:** overwrite the sol sol one, solution one.
[00:15:33:659 - 00:15:36:349] **Speaker 1:** So if you adjust the I don't know, maybe the
[00:15:37:080 - 00:15:39:630] **Speaker 1:** Bottom boundary condition to be 100.
[00:15:43:659 - 00:15:47:179] **Speaker 1:** Now, because we've adjusted the boundary conditions, I think back
[00:15:47:179 - 00:15:49:780] **Speaker 1:** to your separation of variables, which is, which is good
[00:15:49:780 - 00:15:50:340] **Speaker 1:** fun too.
[00:15:50:539 - 00:15:53:659] **Speaker 1:** Um, you've adjusted boundary conditions so that changes the solution.
[00:15:53:940 - 00:15:55:760] **Speaker 1:** So you need to calculate that solution again.
[00:15:56:520 - 00:15:58:200] **Speaker 1:** So under study one, compute.
[00:16:02:099 - 00:16:05:700] **Speaker 1:** And we're getting a different profile as expected, that's symmetrical
[00:16:05:700 - 00:16:07:520] **Speaker 1:** about, um, the X-axis.
[00:16:08:669 - 00:16:12:349] **Speaker 1:** We'll offset by 0.5 because we've got the same boundary
[00:16:12:349 - 00:16:13:169] **Speaker 1:** condition on the top and bottom.
[00:16:14:619 - 00:16:18:270] **Speaker 1:** And if we wanted to do a cut.
[00:16:19:859 - 00:16:20:520] **Speaker 1:** Cut line.
[00:16:24:650 - 00:16:25:250] **Speaker 1:** 2D.
[00:16:29:130 - 00:16:32:469] **Speaker 1:** X And if we want to do at the midpoint,
[00:16:32:539 - 00:16:33:679] **Speaker 1:** so at 0.5.
[00:16:36:960 - 00:16:39:440] **Speaker 1:** That's right through the centre, and we want to do
[00:16:39:440 - 00:16:43:799] **Speaker 1:** the same cut line for our initial boundaries, so roll
[00:16:43:799 - 00:16:44:119] **Speaker 1:** one.
[00:16:44:820 - 00:16:45:609] **Speaker 1:** So that's the thing.
[00:16:46:710 - 00:16:51:260] **Speaker 1:** And Create a 1D plot group, so if you want
[00:16:51:260 - 00:16:54:219] **Speaker 1:** to visualise the temperature profile through that cut line, that's
[00:16:54:219 - 00:16:54:780] **Speaker 1:** 1D.
[00:16:57:000 - 00:17:04:920] **Speaker 1:** And we're going to create Cut 1 1D, what?
[00:17:06:688 - 00:17:08:979] **Speaker 1:** I guess this is another step, I'm getting off track,
[00:17:09:020 - 00:17:10:900] **Speaker 1:** but some of you are looking at these sort of
[00:17:10:900 - 00:17:18:499] **Speaker 1:** things, um, so from dataset, So We can have Each
[00:17:18:499 - 00:17:19:979] **Speaker 1:** of these parent groups.
[00:17:21:780 - 00:17:25:469] **Speaker 1:** Is this original data set that you can choose whatever
[00:17:25:469 - 00:17:27:949] **Speaker 1:** data set you've got underneath, so we're gonna set one
[00:17:27:949 - 00:17:29:010] **Speaker 1:** to cut line 2D.
[00:17:30:510 - 00:17:30:829] **Speaker 1:** Fuck.
[00:17:32:239 - 00:17:35:239] **Speaker 1:** And then we'll change that to degrees Celsius because I
[00:17:35:239 - 00:17:36:640] **Speaker 1:** don't like to think in Kelvin.
[00:17:40:839 - 00:17:44:040] **Speaker 1:** And we'll do the same for cut line 2.
[00:17:45:839 - 00:17:48:180] **Speaker 1:** So it's just a way of comparing both cases.
[00:17:48:689 - 00:17:50:930] **Speaker 1:** So you could do this with your constraint groups.
[00:17:51:040 - 00:17:53:089] **Speaker 1:** So instead of using those constraint groups, just run two
[00:17:53:089 - 00:17:56:369] **Speaker 1:** simulations, save your solution data, and then compare.
[00:17:57:250 - 00:17:59:550] **Speaker 1:** Or Use those constraint groups.
[00:17:59:630 - 00:18:02:390] **Speaker 1:** So lots of different ways to approach similar problems.
[00:18:02:589 - 00:18:05:030] **Speaker 1:** Um, this way it's just a bit easier because you're
[00:18:05:030 - 00:18:07:030] **Speaker 1:** not keeping track of which boundary conditions and loads are
[00:18:07:030 - 00:18:08:530] **Speaker 1:** being applied to, to which case.
[00:18:09:790 - 00:18:13:530] **Speaker 1:** Um, Yeah, I don't know.
[00:18:14:459 - 00:18:17:479] **Speaker 1:** Hopefully that sort of Gives a bit more of an
[00:18:17:479 - 00:18:19:229] **Speaker 1:** indication of what you can do in console.
[00:18:20:219 - 00:18:21:160] **Speaker 1:** Some extra steps.
[00:18:23:619 - 00:18:27:680] **Speaker 1:** All right, any questions on console or?
[00:18:30:569 - 00:18:36:800] **Speaker 1:** Anything So you've you've had a moment to think, do
[00:18:36:800 - 00:18:40:589] **Speaker 1:** you want to look at these chapter 4 exercises and
[00:18:40:589 - 00:18:42:000] **Speaker 1:** sort of let you go through some of them and
[00:18:42:000 - 00:18:43:500] **Speaker 1:** then work through as a class, or should we just
[00:18:43:500 - 00:18:44:560] **Speaker 1:** go to chapter 5?
[00:18:48:599 - 00:18:49:329] **Speaker 1:** Questions.
[00:18:49:630 - 00:18:50:010] **Speaker 1:** All right.
[00:18:50:939 - 00:18:51:319] **Speaker 1:** Cool.
[00:18:51:540 - 00:18:55:099] **Speaker 1:** So question one, well I might start with question two
[00:18:55:099 - 00:18:56:780] **Speaker 1:** cause there's this, I mean, I think you can do
[00:18:56:780 - 00:18:59:579] **Speaker 1:** more by pen and paper to start with.
[00:18:59:939 - 00:19:03:339] **Speaker 1:** So question two, we're going to discretize the Laplace equation
[00:19:03:699 - 00:19:05:780] **Speaker 1:** for steady heat conduction in a unit square.
[00:19:05:979 - 00:19:07:599] **Speaker 1:** So that's pretty much what we just did in console.
[00:19:08:390 - 00:19:10:329] **Speaker 1:** And we've got these different boundary conditions.
[00:19:11:569 - 00:19:14:670] **Speaker 1:** So we've got the origin at the bottom left corner,
[00:19:14:719 - 00:19:18:930] **Speaker 1:** and we had to define that because these boundary conditions
[00:19:18:930 - 00:19:20:930] **Speaker 1:** vary with the coordinates X and Y.
[00:19:22:030 - 00:19:22:949] **Speaker 1:** So it's more exciting.
[00:19:23:229 - 00:19:25:829] **Speaker 1:** So the, the velocity, um, the, the space, what are
[00:19:25:829 - 00:19:26:329] **Speaker 1:** we doing?
[00:19:26:670 - 00:19:30:510] **Speaker 1:** Temperature, it's a little bit confusing, but um, U is
[00:19:30:510 - 00:19:31:650] **Speaker 1:** the temperature in this case.
[00:19:31:989 - 00:19:35:329] **Speaker 1:** So the temperature along the bottom is 0.
[00:19:36:069 - 00:19:38:670] **Speaker 1:** Along the top is equal to one.
[00:19:43:729 - 00:19:46:050] **Speaker 1:** It's always handy to do a sketch, otherwise it's a
[00:19:46:050 - 00:19:47:209] **Speaker 1:** bit hard to interpret.
[00:19:49:369 - 00:19:51:300] **Speaker 1:** So we've got a unit square.
[00:19:52:489 - 00:19:54:790] **Speaker 1:** With the origin in the lower left.
[00:19:58:540 - 00:19:59:020] **Speaker 1:** and why?
[00:20:00:959 - 00:20:03:280] **Speaker 1:** And we just said that the temperature field is equal
[00:20:03:280 - 00:20:08:770] **Speaker 1:** to 0 At the bottom.
[00:20:11:030 - 00:20:13:959] **Speaker 1:** At X equal to 1 is that right hand edge.
[00:20:18:640 - 00:20:20:709] **Speaker 1:** And that varies quadratically with Y.
[00:20:21:920 - 00:20:24:640] **Speaker 1:** So it's gonna be sort of a parabola going from
[00:20:24:640 - 00:20:26:199] **Speaker 1:** 0 up to 1.
[00:20:28:739 - 00:20:31:780] **Speaker 1:** And on the left hand side, we've got a Neumann
[00:20:31:780 - 00:20:34:189] **Speaker 1:** boundary condition, the gradient D by D X.
[00:20:40:410 - 00:20:41:689] **Speaker 1:** Now it's not fully insulated.
[00:20:41:890 - 00:20:43:530] **Speaker 1:** The example we did in the notes was equal to
[00:20:43:530 - 00:20:44:869] **Speaker 1:** 0, now it's equal to 1.
[00:20:45:489 - 00:20:46:329] **Speaker 1:** So it's non-zero.
[00:20:47:170 - 00:20:48:910] **Speaker 1:** And then on the top.
[00:20:50:680 - 00:20:50:689] **Speaker 1:** You.
[00:20:53:310 - 00:20:54:569] **Speaker 1:** X Y equal 1.
[00:20:55:739 - 00:21:06:359] **Speaker 1:** Is equal to X So I'll give you a couple
[00:21:06:359 - 00:21:07:780] **Speaker 1:** of moments to think about.
[00:21:08:520 - 00:21:12:439] **Speaker 1:** Um How we're going to discretize this with our finite
[00:21:12:439 - 00:21:13:060] **Speaker 1:** different scheme.
[00:21:13:829 - 00:21:16:709] **Speaker 1:** We've been told that there are 5 nodes by 5
[00:21:16:709 - 00:21:17:250] **Speaker 1:** nodes.
[00:21:17:900 - 00:21:20:300] **Speaker 1:** And we've been told that the spacing between each node
[00:21:20:300 - 00:21:21:359] **Speaker 1:** is 0.25.
[00:21:23:040 - 00:21:25:810] **Speaker 1:** Again, we've got one fewer spacings than nodes.
[00:21:26:780 - 00:21:28:979] **Speaker 1:** That sounds obvious when, when we say it, but it's,
[00:21:29:140 - 00:21:31:640] **Speaker 1:** it's something that always trips a few people up.
[00:21:35:619 - 00:21:38:140] **Speaker 1:** So I'll let you think about how to discretize this
[00:21:38:140 - 00:21:42:140] **Speaker 1:** domain with those 5x5 grid and think about which nodes
[00:21:42:140 - 00:21:45:140] **Speaker 1:** are unknown or the unknown uh degrees of freedom.
[00:21:46:339 - 00:21:48:150] **Speaker 1:** That we're going to solve for and which ones are
[00:21:48:150 - 00:21:51:290] **Speaker 1:** going to be Prescribed uh boundary conditions.
[00:22:59:189 - 00:23:01:920] **Speaker 1:** So I've been told that it's a 5x5 grid, so
[00:23:01:920 - 00:23:07:040] **Speaker 1:** we can sort of plot out the 5 nodes along
[00:23:07:040 - 00:23:07:959] **Speaker 1:** each direction.
[00:23:19:640 - 00:23:22:589] **Speaker 1:** So we've got 25 nodes or values that we're gonna
[00:23:22:969 - 00:23:24:209] **Speaker 1:** evaluate or have.
[00:23:25:359 - 00:23:28:319] **Speaker 1:** Uh, which of these nodes are values that we need
[00:23:28:319 - 00:23:30:000] **Speaker 1:** to calculate with our finite differencing?
[00:23:32:209 - 00:23:34:099] **Speaker 1:** I, I guess maybe a better question is which ones
[00:23:34:099 - 00:23:36:680] **Speaker 1:** are already defined by our boundary conditions explicitly.
[00:23:42:250 - 00:23:44:189] **Speaker 1:** Yeah, the outside ones.
[00:23:53:849 - 00:24:00:400] **Speaker 1:** So The boundary nodes that correspond to those with the
[00:24:00:400 - 00:24:05:239] **Speaker 1:** Dirichlet condition, so fixed value U equals X, U equals
[00:24:05:239 - 00:24:08:359] **Speaker 1:** Y2 and U equals 0 are going to be fixed.
[00:24:09:619 - 00:24:12:050] **Speaker 1:** But the other nodes, including the one on the left-hand
[00:24:12:050 - 00:24:24:550] **Speaker 1:** side, Uh, unknown And we've got 1234 by 3.
[00:24:27:609 - 00:24:30:560] **Speaker 1:** So we've got 12 So essentially we're gonna solve for
[00:24:30:560 - 00:24:31:560] **Speaker 1:** 12 nodes.
[00:24:31:640 - 00:24:33:020] **Speaker 1:** So we're gonna have 12 equations.
[00:24:34:650 - 00:24:37:339] **Speaker 1:** Which is better than 25, but still a few.
[00:24:38:410 - 00:24:41:209] **Speaker 1:** The interior nodes, that 3 by 3 grid, they're all
[00:24:41:209 - 00:24:42:410] **Speaker 1:** gonna have the same format.
[00:24:43:469 - 00:24:45:130] **Speaker 1:** And we could use a 4 loop if we were
[00:24:45:349 - 00:24:47:430] **Speaker 1:** coding this in Python to toggle through each one.
[00:24:51:010 - 00:24:52:630] **Speaker 1:** It might be helpful to label these.
[00:24:53:089 - 00:24:54:650] **Speaker 1:** I don't know if it will be, but we can
[00:24:54:650 - 00:24:55:469] **Speaker 1:** start 11.
[00:24:56:709 - 00:24:58:479] **Speaker 1:** 121.
[00:24:59:550 - 00:25:02:449] **Speaker 1:** 34, and 5.
[00:25:03:709 - 00:25:06:849] **Speaker 1:** To 122.
[00:25:09:719 - 00:25:13:380] **Speaker 1:** To Oh, this is, this is more difficult than it
[00:25:13:380 - 00:25:14:000] **Speaker 1:** should be.
[00:25:14:430 - 00:25:15:390] **Speaker 1:** This should be 12.
[00:25:17:449 - 00:25:19:010] **Speaker 1:** 1222.
[00:25:20:890 - 00:25:31:160] **Speaker 1:** We'll go up, so that's 13, 1415, 212223, 24, 25,
[00:25:31:449 - 00:25:35:770] **Speaker 1:** 3132, 33, 34, etc.
[00:25:35:930 - 00:25:37:239] **Speaker 1:** I guess we don't actually need to write them all
[00:25:37:239 - 00:25:37:589] **Speaker 1:** out.
[00:25:37:880 - 00:25:41:569] **Speaker 1:** Um, so the inferior good points, just as a recap,
[00:25:41:609 - 00:25:45:060] **Speaker 1:** our Laplace equation said that it was D2U by DX2
[00:25:45:410 - 00:25:48:770] **Speaker 1:** plus D2U by DY2 equal to 0.
[00:25:51:729 - 00:25:54:449] **Speaker 1:** We could just go straight to the answer, but I
[00:25:54:449 - 00:25:58:489] **Speaker 1:** guess it's a nice, um, Demonstration to go through discretizing
[00:25:58:489 - 00:25:59:079] **Speaker 1:** this again.
[00:25:59:650 - 00:26:01:689] **Speaker 1:** So that was in chapter 3.
[00:26:12:250 - 00:26:14:520] **Speaker 1:** So equation 36, we discretized.
[00:26:15:489 - 00:26:19:250] **Speaker 1:** A 2nd order derivative with 2nd order accuracy using the
[00:26:19:250 - 00:26:20:130] **Speaker 1:** central difference scheme.
[00:26:21:810 - 00:26:23:310] **Speaker 1:** So I've got you.
[00:26:24:599 - 00:26:29:199] **Speaker 1:** I + 1 minus 2 UI + UI minus 1
[00:26:29:550 - 00:26:30:800] **Speaker 1:** divided by delta X2.
[00:26:32:469 - 00:26:34:670] **Speaker 1:** You can probably memorise it after you've done it a
[00:26:34:670 - 00:26:35:489] **Speaker 1:** couple of times.
[00:26:37:619 - 00:26:39:750] **Speaker 1:** Make it a bit darker it might be easier, um.
[00:26:41:900 - 00:26:44:260] **Speaker 1:** Now, it's a partial derivative in X, so I'm only
[00:26:44:260 - 00:26:45:839] **Speaker 1:** varying the I components.
[00:26:46:260 - 00:26:48:739] **Speaker 1:** There are still J components that exist, that is held
[00:26:48:739 - 00:26:50:739] **Speaker 1:** constant, so we can add in the J's.
[00:26:52:329 - 00:26:53:660] **Speaker 1:** As the 2nd index.
[00:26:55:239 - 00:26:58:439] **Speaker 1:** We have a partial derivative in Y, so that's gonna
[00:26:58:439 - 00:27:04:079] **Speaker 1:** be UIJ + 1 minus 2 UIJ.
[00:27:04:949 - 00:27:08:589] **Speaker 1:** Plus UIJ minus 1.
[00:27:10:130 - 00:27:12:290] **Speaker 1:** Divided by that Y 2 equal to 0.
[00:27:13:939 - 00:27:15:400] **Speaker 1:** So we've applied that 2nd order.
[00:27:16:770 - 00:27:19:819] **Speaker 1:** Uh, central different scheme for our second order derivatives.
[00:27:21:319 - 00:27:24:839] **Speaker 1:** For this particular problem, we're told that our spacings are
[00:27:24:839 - 00:27:27:060] **Speaker 1:** uniform, so delta X is equal to tay.
[00:27:27:849 - 00:27:30:780] **Speaker 1:** So we can times through by delta X2 and Y2
[00:27:30:969 - 00:27:35:170] **Speaker 1:** and we are left with UI + 1 J.
[00:27:36:459 - 00:27:37:739] **Speaker 1:** You I minus 1 J.
[00:27:38:530 - 00:27:40:150] **Speaker 1:** U I J + 1.
[00:27:41:459 - 00:27:43:599] **Speaker 1:** And UIJ minus 1.
[00:27:45:349 - 00:27:47:630] **Speaker 1:** -4 UIJ.
[00:27:51:380 - 00:27:53:709] **Speaker 1:** So that's, that's what we did in the notes.
[00:27:54:699 - 00:27:58:150] **Speaker 1:** So just recovering that general equation or discretize equation for
[00:27:58:150 - 00:27:59:550] **Speaker 1:** all those interior nodes.
[00:28:11:810 - 00:28:14:329] **Speaker 1:** Maybe I can use another colour for.
[00:28:31:890 - 00:28:33:479] **Speaker 1:** So all the interior nodes are going to be covered
[00:28:33:479 - 00:28:34:300] **Speaker 1:** by this equation.
[00:28:34:609 - 00:28:37:880] **Speaker 1:** We've got 9, you can write out 9 or um
[00:28:38:760 - 00:28:42:829] **Speaker 1:** Coed it with a for loop Now, the top, right,
[00:28:42:859 - 00:28:46:099] **Speaker 1:** and bottom boundary conditions are defined by setting U equal
[00:28:46:099 - 00:28:47:739] **Speaker 1:** to the value of that boundary condition.
[00:28:48:099 - 00:28:50:420] **Speaker 1:** Now we've got 3 remaining nodes.
[00:28:50:699 - 00:28:52:420] **Speaker 1:** So I'll give you a moment to think through how
[00:28:52:420 - 00:28:54:640] **Speaker 1:** we can do those three nodes on the left-hand side.
[00:28:55:140 - 00:28:57:079] **Speaker 1:** So that's 1213, and 14.
[00:30:10:010 - 00:30:11:030] **Speaker 1:** Any ideas?
[00:30:22:229 - 00:30:25:150] **Speaker 1:** Essentially all these 3 nodes are temperature values that we
[00:30:25:150 - 00:30:26:510] **Speaker 1:** don't know what they are, but we know that the
[00:30:26:510 - 00:30:28:810] **Speaker 1:** gradient is equal to 1, so that way.
[00:30:30:699 - 00:30:31:599] **Speaker 1:** That way for you.
[00:30:32:020 - 00:30:32:540] **Speaker 1:** Um.
[00:30:33:349 - 00:30:35:170] **Speaker 1:** So we need to discretize this boundary condition.
[00:30:36:829 - 00:30:37:510] **Speaker 1:** There's one step.
[00:30:38:670 - 00:30:41:160] **Speaker 1:** Uh, we want to do a central difference about that
[00:30:41:160 - 00:30:41:939] **Speaker 1:** left edge.
[00:30:42:890 - 00:30:45:280] **Speaker 1:** So if we're doing a central difference scheme, then we
[00:30:45:280 - 00:30:46:420] **Speaker 1:** need a node on either side.
[00:30:46:959 - 00:30:50:800] **Speaker 1:** So that's where we introduce the Uh, ghost nodes, so
[00:30:50:800 - 00:30:51:540] **Speaker 1:** I might just.
[00:30:52:979 - 00:30:55:579] **Speaker 1:** Right, these are Again.
[00:30:57:199 - 00:30:58:510] **Speaker 1:** So these are one.
[00:30:59:369 - 00:31:03:619] **Speaker 1:** To 1314.
[00:31:04:869 - 00:31:05:810] **Speaker 1:** 24.
[00:31:06:550 - 00:31:07:430] **Speaker 1:** 23.
[00:31:08:599 - 00:31:13:560] **Speaker 1:** 22 And the ghost points.
[00:31:15:020 - 00:31:16:349] **Speaker 1:** Are gonna be 04.
[00:31:18:660 - 00:31:20:780] **Speaker 1:** 03 and 02.
[00:31:24:219 - 00:31:26:000] **Speaker 1:** And we'll be doing the central differenceerencing.
[00:31:26:959 - 00:31:29:130] **Speaker 1:** Across those three nodes.
[00:31:34:530 - 00:31:40:630] **Speaker 1:** To keep it generic, we're going to um Set I
[00:31:40:630 - 00:31:43:170] **Speaker 1:** equal to 1, but keep J as an index that
[00:31:43:170 - 00:31:43:569] **Speaker 1:** varies.
[00:31:43:770 - 00:31:45:829] **Speaker 1:** So J is equal to 23 or 4.
[00:31:58:060 - 00:32:00:859] **Speaker 1:** And if we substitute in our values i and J's
[00:32:00:859 - 00:32:06:310] **Speaker 1:** into our general equation, We're left with U1 + 1,
[00:32:06:800 - 00:32:09:439] **Speaker 1:** so 1 + 1 will be 2.
[00:32:10:410 - 00:32:13:390] **Speaker 1:** And we've got J values And then you I minus
[00:32:13:390 - 00:32:15:229] **Speaker 1:** 1, so you 0 J.
[00:32:16:349 - 00:32:19:140] **Speaker 1:** You won J + 1.
[00:32:19:939 - 00:32:21:979] **Speaker 1:** U 1 minus 1.
[00:32:23:770 - 00:32:26:530] **Speaker 1:** -4 times you at.
[00:32:29:229 - 00:32:30:719] **Speaker 1:** 1 J.
[00:32:35:109 - 00:32:36:199] **Speaker 1:** Is it a naught J?
[00:32:37:229 - 00:32:39:890] **Speaker 1:** Our temperature node is going to be our ghost point.
[00:32:40:660 - 00:32:42:300] **Speaker 1:** And that's what we're going to try and get rid
[00:32:42:300 - 00:32:45:420] **Speaker 1:** of by enforcing our boundary condition, D U D X
[00:32:45:420 - 00:32:46:119] **Speaker 1:** equal to 1.
[00:32:52:650 - 00:32:56:729] **Speaker 1:** So how can we discretize our boundary condition from this
[00:32:56:729 - 00:32:59:569] **Speaker 1:** continuous form, using our central difference scheme?
[00:33:15:959 - 00:33:18:239] **Speaker 1:** If we forget, we can go back to our table.
[00:33:18:810 - 00:33:22:040] **Speaker 1:** So first order derivatives, 2nd order accuracy, we've got 12
[00:33:22:319 - 00:33:23:920] **Speaker 1:** of the one on the left and then positive 1/2
[00:33:23:920 - 00:33:24:489] **Speaker 1:** on the right.
[00:33:26:140 - 00:33:27:689] **Speaker 1:** Or you can just think of it rise over run
[00:33:27:689 - 00:33:28:729] **Speaker 1:** because it's a gradient.
[00:33:29:229 - 00:33:33:449] **Speaker 1:** So DU by DX evaluated at X equal to 0.
[00:33:34:260 - 00:33:38:359] **Speaker 1:** is going to be the temperature at the node on
[00:33:38:359 - 00:33:38:819] **Speaker 1:** the right.
[00:33:38:979 - 00:33:44:449] **Speaker 1:** So you at 2 Jay.
[00:33:45:239 - 00:33:47:739] **Speaker 1:** So that corresponds to those three entries on the right
[00:33:47:739 - 00:33:50:880] **Speaker 1:** minus U 0 J.
[00:33:51:949 - 00:33:55:550] **Speaker 1:** Divided by the spacings, all these spacings have spacings of
[00:33:55:550 - 00:33:56:390] **Speaker 1:** data X.
[00:34:00:719 - 00:34:03:479] **Speaker 1:** So it's across two node spacings, we've got 2 letters.
[00:34:05:280 - 00:34:06:849] **Speaker 1:** And we're told that this is equal to one.
[00:34:16:590 - 00:34:17:429] **Speaker 1:** What's the next step?
[00:34:22:148 - 00:34:22:489] **Speaker 1:** Yeah.
[00:34:22:830 - 00:34:24:949] **Speaker 1:** So what we're trying to do is get rid of
[00:34:24:949 - 00:34:25:850] **Speaker 1:** this ghost point.
[00:34:26:229 - 00:34:28:189] **Speaker 1:** So we're going to rearrange our boundary condition for you
[00:34:28:189 - 00:34:28:760] **Speaker 1:** not J.
[00:34:36:138 - 00:34:39:219] **Speaker 1:** I suppose that's gonna be minus plus U2 J.
[00:34:46:888 - 00:34:54:669] **Speaker 1:** And substitute Into our equation here, so we've got U2J
[00:34:54:669 - 00:34:56:530] **Speaker 1:** and U2J, so we've got two of those.
[00:35:01:280 - 00:35:04:959] **Speaker 1:** Uh, U1 J + 1.
[00:35:05:590 - 00:35:10:790] **Speaker 1:** U1 J minus 1 minus 4 U.1 J.
[00:35:22:580 - 00:35:24:459] **Speaker 1:** That's not equal to 0, that's a trap.
[00:35:25:989 - 00:35:29:969] **Speaker 1:** So This is going to equal 2 times delta X.
[00:35:35:889 - 00:35:38:770] **Speaker 1:** So it would be equal to 0 if it was
[00:35:38:770 - 00:35:41:860] **Speaker 1:** fully insulated, but in this case we've got 2 directs.
[00:35:48:780 - 00:35:52:000] **Speaker 1:** And for this case, we've got 5 by 5 grid
[00:35:52:580 - 00:35:55:439] **Speaker 1:** and delta X is equal to 0.25.
[00:36:00:250 - 00:36:01:439] **Speaker 1:** So it's just equal to 12.
[00:36:13:100 - 00:36:17:580] **Speaker 1:** So essentially what we have is For the interior 3
[00:36:17:580 - 00:36:22:139] **Speaker 1:** by 3 grid, the general interior equation holds.
[00:36:22:580 - 00:36:24:739] **Speaker 1:** For those 3 nodes on the left, we enforce this
[00:36:24:739 - 00:36:25:300] **Speaker 1:** equation.
[00:36:26:070 - 00:36:28:209] **Speaker 1:** So we can toggle J through 23 and 4.
[00:36:29:840 - 00:36:31:879] **Speaker 1:** Um Yeah.
[00:36:32:050 - 00:36:34:639] **Speaker 1:** So what we end up with is matrix of coefficients
[00:36:34:639 - 00:36:35:020] **Speaker 1:** A.
[00:36:36:010 - 00:36:40:189] **Speaker 1:** Uh, vector of unknowns U and that right-hand side, vector
[00:36:40:409 - 00:36:40:729] **Speaker 1:** V.
[00:37:12:959 - 00:37:13:360] **Speaker 1:** Who?
[00:37:15:040 - 00:37:17:840] **Speaker 1:** So hopefully that sort of covers most of the concepts
[00:37:17:840 - 00:37:20:770] **Speaker 1:** that we've, Discussed in class so far.
[00:37:21:689 - 00:37:24:370] **Speaker 1:** I'm just seeing if it's actually, if I included a
[00:37:25:199 - 00:37:26:459] **Speaker 1:** Script or not for this question.
[00:37:29:139 - 00:37:30:780] **Speaker 1:** And then.
[00:37:41:370 - 00:37:42:139] **Speaker 1:** No, I didn't.
[00:37:42:530 - 00:37:45:439] **Speaker 1:** So that's a bit disappointing, but that's right, you can
[00:37:45:439 - 00:37:46:139] **Speaker 1:** code it yourself.
[00:37:46:469 - 00:37:50:159] **Speaker 1:** Um, so you'd have a matrix of coefficients A that
[00:37:50:159 - 00:37:51:340] **Speaker 1:** has size.
[00:37:52:439 - 00:37:55:159] **Speaker 1:** 12 by 12, because there's 12 degrees of freedom.
[00:37:56:600 - 00:37:59:800] **Speaker 1:** And you can solve for that, that uh vector, you.
[00:38:02:939 - 00:38:02:959] **Speaker 1:** All right.
[00:38:05:649 - 00:38:05:889] **Speaker 1:** Cool.
[00:38:11:419 - 00:38:15:270] **Speaker 1:** Any other questions that You particularly want to go through,
[00:38:15:429 - 00:38:17:070] **Speaker 1:** maybe from the earlier chapters or.
[00:38:34:479 - 00:38:35:260] **Speaker 1:** That's right.
[00:38:35:719 - 00:38:38:959] **Speaker 1:** Um, so we can use, we can look at question
[00:38:38:959 - 00:38:39:500] **Speaker 1:** one.
[00:38:40:159 - 00:38:42:199] **Speaker 1:** So because I don't think there's any questions in chapter
[00:38:42:199 - 00:38:45:229] **Speaker 1:** three, and the early ones were separation of variables and
[00:38:45:229 - 00:38:47:060] **Speaker 1:** things, so you've had plenty of practise with those already.
[00:38:47:560 - 00:38:49:959] **Speaker 1:** So this one is looking at finite differenceencing again, but
[00:38:49:959 - 00:38:50:929] **Speaker 1:** using the Leben method.
[00:38:51:689 - 00:38:54:679] **Speaker 1:** Uh, and we're going to solve for the square heated
[00:38:54:679 - 00:38:55:070] **Speaker 1:** plate.
[00:38:56:050 - 00:38:58:469] **Speaker 1:** So we've got insulated boundary conditions on the bottom and
[00:38:58:469 - 00:38:59:149] **Speaker 1:** on the side.
[00:38:59:850 - 00:39:04:879] **Speaker 1:** And then iterating with some um tolerance that reaches below
[00:39:04:879 - 00:39:07:939] **Speaker 1:** 0.01%, so 10 to -4.
[00:39:09:949 - 00:39:12:350] **Speaker 1:** We're gonna start with an initial guess of 0 °C
[00:39:12:350 - 00:39:15:530] **Speaker 1:** for all the unknown temperature values and then figure out
[00:39:15:530 - 00:39:17:570] **Speaker 1:** how many iterations are required for convergence.
[00:39:19:969 - 00:39:24:780] **Speaker 1:** So question, um.
[00:39:25:989 - 00:39:29:080] **Speaker 1:** Which Of these nodes are the ones that we're gonna
[00:39:29:080 - 00:39:31:139] **Speaker 1:** try and calculate and which are already defined.
[00:39:53:040 - 00:39:54:129] **Speaker 1:** You can do it on another sheet.
[00:39:56:939 - 00:40:00:260] **Speaker 1:** So we've got 12345 by 5 quid again, so that's
[00:40:00:260 - 00:40:00:679] **Speaker 1:** a good.
[00:40:01:610 - 00:40:02:429] **Speaker 1:** Consistency.
[00:40:12:270 - 00:40:13:379] **Speaker 1:** So we've got 5 by 5 grid.
[00:40:13:620 - 00:40:17:100] **Speaker 1:** Uh, the 100 conditions on the top and right are
[00:40:17:100 - 00:40:19:050] **Speaker 1:** fixed, so they're already going to be defined.
[00:40:19:419 - 00:40:20:939] **Speaker 1:** So the only unknown degrees of freedom that we're trying
[00:40:20:939 - 00:40:24:060] **Speaker 1:** to calculate with our finite differencing is the lower 4
[00:40:24:060 - 00:40:24:570] **Speaker 1:** by 4 grid.
[00:40:24:620 - 00:40:27:459] **Speaker 1:** So we've got 16 degrees of freedom or 16 unknown.
[00:40:29:219 - 00:40:31:520] **Speaker 1:** Degrees of freedom that we're trying to calculate.
[00:40:32:020 - 00:40:34:439] **Speaker 1:** The interior nodes are going to have that same pattern
[00:40:34:659 - 00:40:36:800] **Speaker 1:** of TI.
[00:40:37:909 - 00:40:42:020] **Speaker 1:** Plus 1 JTI minus 1 J.
[00:40:42:909 - 00:40:48:340] **Speaker 1:** DIJ + 1, DIJ minus 1 minus 4 DI.
[00:40:49:540 - 00:40:51:120] **Speaker 1:** J equal to 0.
[00:40:51:629 - 00:40:52:879] **Speaker 1:** So that's the interior.
[00:40:55:060 - 00:40:55:629] **Speaker 1:** Notes.
[00:40:57:540 - 00:40:59:110] **Speaker 1:** I guess we used red last time.
[00:41:03:169 - 00:41:07:330] **Speaker 1:** And for the ones along the left-hand edge and the
[00:41:07:330 - 00:41:10:610] **Speaker 1:** bottom edge, we've got those fully insulated boundary conditions.
[00:41:10:679 - 00:41:12:290] **Speaker 1:** So the gradient is equal to 0.
[00:41:12:570 - 00:41:13:770] **Speaker 1:** So the heat flux is zero here.
[00:41:25:169 - 00:41:28:270] **Speaker 1:** So we can do the same procedure, we've got UI
[00:41:28:270 - 00:41:29:110] **Speaker 1:** plus 1.
[00:41:31:010 - 00:41:35:139] **Speaker 1:** J minus UI minus 1, J divided by 2 X.
[00:41:35:820 - 00:41:38:340] **Speaker 1:** So I'm not gonna bother trying to replace I with
[00:41:38:340 - 00:41:38:580] **Speaker 1:** one.
[00:41:38:780 - 00:41:40:389] **Speaker 1:** It's much easier just to think of an I +
[00:41:40:389 - 00:41:42:939] **Speaker 1:** 11 minus 1 and then in your full loop, just
[00:41:42:939 - 00:41:45:820] **Speaker 1:** do a condition if I is equal to 1, apply
[00:41:45:820 - 00:41:47:100] **Speaker 1:** this condition.
[00:41:48:850 - 00:41:49:860] **Speaker 1:** Much easier to think about.
[00:41:50:149 - 00:41:53:179] **Speaker 1:** So we've got our discretization for DU by DX.
[00:41:53:330 - 00:41:54:520] **Speaker 1:** This is equal to 0.
[00:41:54:939 - 00:41:57:340] **Speaker 1:** We rearrange for our ghost point, which is at UI
[00:41:57:340 - 00:41:58:280] **Speaker 1:** minus 1.
[00:41:59:159 - 00:42:01:639] **Speaker 1:** And this is equal to UI plus 1 J.
[00:42:03:330 - 00:42:05:399] **Speaker 1:** We substitute into our equation.
[00:42:06:110 - 00:42:09:040] **Speaker 1:** And I've already replaced U's and T's, so a bit
[00:42:09:040 - 00:42:09:939] **Speaker 1:** of a rookie mistake.
[00:42:14:260 - 00:42:18:620] **Speaker 1:** So these are all T's replacing, we've got UI minus
[00:42:18:620 - 00:42:21:040] **Speaker 1:** 1 with 1 + 1, so we've got 2.
[00:42:21:889 - 00:42:23:750] **Speaker 1:** TI + 1 J.
[00:42:25:689 - 00:42:33:530] **Speaker 1:** TIJ + 1, TIJ minus 1 minus 4 TIJ equal
[00:42:33:530 - 00:42:33:850] **Speaker 1:** to 0.
[00:42:38:699 - 00:42:41:209] **Speaker 1:** So exactly what we just did earlier.
[00:42:41:610 - 00:42:44:330] **Speaker 1:** So that applies to the left hand side, now for
[00:42:44:330 - 00:42:44:909] **Speaker 1:** the lower.
[00:42:48:489 - 00:42:50:570] **Speaker 1:** We've got DUI.
[00:42:51:659 - 00:42:52:600] **Speaker 1:** Sorry, DT.
[00:42:53:560 - 00:42:55:800] **Speaker 1:** By DY equal to 0.
[00:42:59:020 - 00:43:00:760] **Speaker 1:** So TI.
[00:43:01:689 - 00:43:06:030] **Speaker 1:** J minus 1 is equal to TIJ + 1.
[00:43:08:780 - 00:43:11:449] **Speaker 1:** And just for the sake of sanity for everyone, I'll
[00:43:11:449 - 00:43:17:179] **Speaker 1:** skip by inserting this temperature into our general form and
[00:43:17:179 - 00:43:19:379] **Speaker 1:** we've got TI + 1.
[00:43:21:070 - 00:43:21:090] **Speaker 1:** Jay.
[00:43:22:790 - 00:43:24:469] **Speaker 1:** DI minus 1 J.
[00:43:26:629 - 00:43:34:379] **Speaker 1:** And we've got 2 TIJ + 1 minus 4 TIJ
[00:43:34:659 - 00:43:35:600] **Speaker 1:** equal to 0.
[00:43:36:360 - 00:43:38:070] **Speaker 1:** So the left-hand side and the bottom boundary conditions.
[00:43:38:139 - 00:43:40:399] **Speaker 1:** What about that corner node in the lower left?
[00:43:48:399 - 00:43:50:060] **Speaker 1:** It's up against two boundaries.
[00:43:52:100 - 00:43:54:060] **Speaker 1:** How can we go about discretizing this equation?
[00:44:18:949 - 00:44:22:489] **Speaker 1:** The example we did in class was with boundary conditions.
[00:44:23:030 - 00:44:24:669] **Speaker 1:** So we just took the average of the two.
[00:44:24:870 - 00:44:27:169] **Speaker 1:** So we sort of encompassed both boundaries.
[00:44:27:909 - 00:44:30:709] **Speaker 1:** But in this case, we've got gradients specified to be
[00:44:30:709 - 00:44:33:469] **Speaker 1:** zero in the vertical and the horizontal.
[00:44:34:189 - 00:44:37:729] **Speaker 1:** So how can we enforce both boundary conditions for our
[00:44:37:870 - 00:44:40:030] **Speaker 1:** interior, uh, for our corner point?
[00:44:52:979 - 00:44:57:149] **Speaker 1:** Uh It's Friday, but yeah.
[00:44:57:550 - 00:44:58:629] **Speaker 1:** All right, so um.
[00:45:00:419 - 00:45:02:149] **Speaker 1:** We're going to use both boundary conditions.
[00:45:02:350 - 00:45:04:610] **Speaker 1:** So we're going to substitute in I minus 1.
[00:45:05:340 - 00:45:07:260] **Speaker 1:** Into our general equation.
[00:45:07:300 - 00:45:09:419] **Speaker 1:** And then we've got TIJ minus 1.
[00:45:09:580 - 00:45:11:580] **Speaker 1:** So maybe I'd sketch these out.
[00:45:11:780 - 00:45:13:360] **Speaker 1:** Maybe that's going to be helpful.
[00:45:14:000 - 00:45:15:280] **Speaker 1:** So left-hand boundary.
[00:45:17:469 - 00:45:22:719] **Speaker 1:** We've got uh Ghost Note, And we're doing our gradient
[00:45:22:719 - 00:45:22:959] **Speaker 1:** here.
[00:45:23:149 - 00:45:24:179] **Speaker 1:** The bottom boundary.
[00:45:27:629 - 00:45:28:530] **Speaker 1:** Bottom boundary.
[00:45:29:699 - 00:45:31:479] **Speaker 1:** We've got a ghost point on the bottom.
[00:45:32:199 - 00:45:37:169] **Speaker 1:** The corner We've got 2 ghost points.
[00:45:38:780 - 00:45:41:739] **Speaker 1:** So we, we could go through and apply both of
[00:45:41:739 - 00:45:43:939] **Speaker 1:** these boundary conditions, but we've already calculated them, so I'm
[00:45:43:939 - 00:45:46:419] **Speaker 1:** just going straight to substituting those, those values for the
[00:45:46:419 - 00:45:48:399] **Speaker 1:** ghost points into our equation.
[00:45:50:020 - 00:45:51:919] **Speaker 1:** And what we're left with is TI.
[00:45:52:820 - 00:45:54:189] **Speaker 1:** Plus 1 J.
[00:45:54:729 - 00:45:57:870] **Speaker 1:** DI minus 1 is the ghost point on the left.
[00:45:58:750 - 00:46:00:840] **Speaker 1:** And we said this is equal to TI + 1.
[00:46:02:629 - 00:46:06:399] **Speaker 1:** So we've got 2 of those The next term we've
[00:46:06:399 - 00:46:09:060] **Speaker 1:** got TIJ +1, so that's up here.
[00:46:13:419 - 00:46:17:739] **Speaker 1:** And then TIJ minus 1 is the node below the
[00:46:17:739 - 00:46:18:100] **Speaker 1:** boundaries.
[00:46:18:199 - 00:46:19:149] **Speaker 1:** So this is a ghost point.
[00:46:19:340 - 00:46:20:600] **Speaker 1:** So we've got two of those.
[00:46:21:110 - 00:46:24:000] **Speaker 1:** We've got TIJ minus 1 equal to TIJ plus 1.
[00:46:25:239 - 00:46:28:330] **Speaker 1:** -4 TIJ.
[00:46:39:649 - 00:46:41:959] **Speaker 1:** So What we've got.
[00:46:47:689 - 00:46:50:090] **Speaker 1:** It's quite painful having to remote connect every time it
[00:46:50:090 - 00:46:51:929] **Speaker 1:** goes to sleep, but um.
[00:46:52:750 - 00:46:56:030] **Speaker 1:** So we've got interior good points defined with our red
[00:46:56:030 - 00:46:56:590] **Speaker 1:** equation.
[00:46:56:770 - 00:46:58:669] **Speaker 1:** So 3 by 39 equations.
[00:46:58:750 - 00:47:01:350] **Speaker 1:** We've got 3 nodes on the left boundary that we're
[00:47:01:350 - 00:47:04:389] **Speaker 1:** using this equation, 3 on the bottom, 1 in the
[00:47:04:389 - 00:47:04:830] **Speaker 1:** corner.
[00:47:05:070 - 00:47:07:310] **Speaker 1:** So we've got an equation for each of those degrees
[00:47:07:310 - 00:47:08:810] **Speaker 1:** of freedom that we're trying to figure out.
[00:47:09:310 - 00:47:10:489] **Speaker 1:** So we're going to have a 16.
[00:47:11:310 - 00:47:15:439] **Speaker 1:** Set of equations, uh, 16 by 16 matrix of coefficients
[00:47:15:439 - 00:47:15:750] **Speaker 1:** A.
[00:47:18:570 - 00:47:21:370] **Speaker 1:** And we've probably already forgot what we were actually asked
[00:47:21:370 - 00:47:21:870] **Speaker 1:** to do.
[00:47:22:409 - 00:47:25:169] **Speaker 1:** So starting from an initial guess of T0 for all
[00:47:25:169 - 00:47:28:070] **Speaker 1:** unknown temperature values, how many iterations are required for convergence.
[00:47:28:610 - 00:47:29:889] **Speaker 1:** So question one A.
[00:47:31:290 - 00:47:32:810] **Speaker 1:** The other thing I wanted to point out is that
[00:47:32:810 - 00:47:35:689] **Speaker 1:** all these codes are on there under the course material
[00:47:35:689 - 00:47:36:149] **Speaker 1:** folder.
[00:47:36:909 - 00:47:39:030] **Speaker 1:** Uh, so you can download that whole folder and it's
[00:47:39:030 - 00:47:40:689] **Speaker 1:** in the structure of all the chapters.
[00:47:41:030 - 00:47:44:189] **Speaker 1:** And those pings or notifications that I send out is
[00:47:44:189 - 00:47:46:310] **Speaker 1:** when I upload things and I give it a bit
[00:47:46:310 - 00:47:48:590] **Speaker 1:** of a summary, um, in the description if you want
[00:47:48:590 - 00:47:49:250] **Speaker 1:** to keep track.
[00:47:50:020 - 00:47:51:510] **Speaker 1:** And if you don't want all the emails, you can
[00:47:51:510 - 00:47:54:350] **Speaker 1:** disable them if you wish, and you still can't see.
[00:47:56:500 - 00:47:56:959] **Speaker 1:** OK.
[00:47:57:300 - 00:48:00:260] **Speaker 1:** So this is a code for chapter 4, question 1A.
[00:48:00:780 - 00:48:02:500] **Speaker 1:** So this is very similar to the Leeben method that
[00:48:02:500 - 00:48:03:399] **Speaker 1:** we do in class.
[00:48:04:219 - 00:48:06:189] **Speaker 1:** Um, so I won't go through all the details, I
[00:48:06:189 - 00:48:08:189] **Speaker 1:** guess just click play and see if it gives us
[00:48:08:189 - 00:48:08:649] **Speaker 1:** a result.
[00:48:09:979 - 00:48:13:179] **Speaker 1:** So it's taken 59 iterations and it's given an error,
[00:48:13:219 - 00:48:14:500] **Speaker 1:** so that's, that's interesting.
[00:48:20:520 - 00:48:21:820] **Speaker 1:** Hopefully it's not too critical.
[00:48:24:030 - 00:48:25:270] **Speaker 1:** We've got some dots.
[00:48:25:790 - 00:48:28:989] **Speaker 1:** So this is our temperature field.
[00:48:31:149 - 00:48:32:209] **Speaker 1:** Does this make sense?
[00:48:32:310 - 00:48:34:149] **Speaker 1:** Again, every time you get some results, you need to
[00:48:34:149 - 00:48:37:870] **Speaker 1:** physically interpret it and make sure that Uh, aligns with
[00:48:37:870 - 00:48:38:449] **Speaker 1:** what you expect.
[00:48:38:870 - 00:48:41:709] **Speaker 1:** Our boundary conditions enforced were from 0 to 100 on
[00:48:41:709 - 00:48:43:840] **Speaker 1:** top and on the right, and we can see that
[00:48:43:850 - 00:48:44:729] **Speaker 1:** that's achieved.
[00:48:46:540 - 00:48:49:939] **Speaker 1:** On that far end, so Y equals 1, X equals
[00:48:49:939 - 00:48:54:100] **Speaker 1:** to 1, we've got these linear temperature variations from 0
[00:48:54:100 - 00:48:55:020] **Speaker 1:** up to 100.
[00:48:57:080 - 00:48:59:500] **Speaker 1:** The boundary conditions on the left and on the bottom
[00:48:59:500 - 00:49:00:620] **Speaker 1:** are insulated.
[00:49:00:899 - 00:49:02:939] **Speaker 1:** So the gradient of temperature is zero.
[00:49:03:520 - 00:49:06:239] **Speaker 1:** And we can see that it's, it's flat along the
[00:49:06:239 - 00:49:06:780] **Speaker 1:** edge.
[00:49:07:179 - 00:49:09:469] **Speaker 1:** If we had a higher resolution mesh, it would show
[00:49:09:469 - 00:49:11:550] **Speaker 1:** better, but we can see that it's got a zero
[00:49:11:550 - 00:49:12:080] **Speaker 1:** gradient.
[00:49:15:770 - 00:49:18:590] **Speaker 1:** And we're also asked to look at over relaxation.
[00:49:19:100 - 00:49:20:590] **Speaker 1:** So we looked at that in class.
[00:49:21:340 - 00:49:24:179] **Speaker 1:** Uh, earlier in the week and figured out that there's
[00:49:24:179 - 00:49:27:080] **Speaker 1:** an optimum over relaxation factor lambda.
[00:49:27:540 - 00:49:29:020] **Speaker 1:** And, and you'll have more practise with that.
[00:49:29:060 - 00:49:31:419] **Speaker 1:** I think that's in next week's quiz, um, but that's
[00:49:31:419 - 00:49:32:520] **Speaker 1:** sort of where it's coming from.
[00:49:35:250 - 00:49:37:729] **Speaker 1:** And here's just another plot, similar to what we did
[00:49:37:729 - 00:49:40:409] **Speaker 1:** in class again, but um just showing the heat flux
[00:49:40:649 - 00:49:43:270] **Speaker 1:** is coming from the hot region to the cold region
[00:49:43:270 - 00:49:44:629] **Speaker 1:** as, as you might expect.
[00:49:46:760 - 00:49:47:260] **Speaker 1:** Cool.
[00:49:47:760 - 00:49:49:600] **Speaker 1:** Uh, hope that sort of tidies up some of the
[00:49:49:600 - 00:49:52:020] **Speaker 1:** concepts that we've covered so far in chapter 4.
[00:49:52:560 - 00:49:53:600] **Speaker 1:** Makes it a bit easier for you.
[00:49:53:800 - 00:49:56:040] **Speaker 1:** Uh, next week we'll go with chapter 5, and that's
[00:49:56:040 - 00:49:57:060] **Speaker 1:** the heat equation.
[00:50:18:810 - 00:50:34:350] **Speaker 0:** They Oh yeah.
[00:50:37:860 - 00:50:37:870] **Speaker 0:** OK.
[00:50:42:389 - 00:50:43:080] **Speaker 0:** Uh, how you doing.
[00:50:46:310 - 00:50:46:320] **Speaker 0:** And.
[00:50:57:790 - 00:51:01:479] **Speaker 0:** Wow Uh.
[00:51:04:449 - 00:51:19:850] **Speaker 0:** So Yeah Hi, with the quiz, uh, what happens if
[00:51:19:850 - 00:51:22:969] **Speaker 0:** we involve density to the weight force in already?
[00:51:24:469 - 00:51:26:879] **Speaker 1:** Uh, I mean you could just check without the wait
[00:51:26:879 - 00:51:27:629] **Speaker 1:** to see how.
[00:51:28:270 - 00:51:33:810] **Speaker 1:** That I think it's only like 1% different, but I
[00:51:33:810 - 00:51:38:050] **Speaker 1:** guess it depends what density you get we're gonna have
[00:51:38:050 - 00:51:42:719] **Speaker 0:** a quick look, otherwise it's 0.2%, yeah, um, because I
[00:51:42:719 - 00:51:45:370] **Speaker 1:** can't reopen quizzes, which I can delete it, but then
[00:51:45:370 - 00:51:46:189] **Speaker 1:** you have to start again.
[00:51:47:689 - 00:51:48:250] **Speaker 1:** No, it's right.
[00:51:48:500 - 00:51:51:610] **Speaker 1:** There's a 2% as long as it's within 2%, hopefully.
[00:51:57:570 - 00:51:57:770] **Speaker 0:** right.

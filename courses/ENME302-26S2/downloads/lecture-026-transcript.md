# ENME302-26S2 Lecture 26 native Echo transcript

Date: September 9, 2026 11:00am-11:55am
Transcript type: native Echo automated transcript.

[00:00:08:869 - 00:00:43:919] **Speaker 0:** Yes That schedule It's Uh, good morning, we'll make a
[00:00:43:919 - 00:00:44:380] **Speaker 1:** start.
[00:00:44:799 - 00:00:48:490] **Speaker 1:** All right, so on Monday we're going through these, uh,
[00:00:48:599 - 00:00:53:209] **Speaker 1:** finite differenceencing, and we're going to just, Solve this equation
[00:00:53:209 - 00:00:53:759] **Speaker 1:** analytically.
[00:00:53:830 - 00:00:56:930] **Speaker 1:** So integrating twice, um, so some of you may have
[00:00:56:930 - 00:01:00:090] **Speaker 1:** done this at home, but I suspect no one, but
[00:01:00:090 - 00:01:00:729] **Speaker 1:** that's OK.
[00:01:01:130 - 00:01:04:029] **Speaker 1:** So we're going to integrate our governing equation twice and
[00:01:04:489 - 00:01:05:970] **Speaker 1:** figure out what the analytical solution is.
[00:01:06:169 - 00:01:14:980] **Speaker 1:** So first step Is Um, integrating AE D2U by DX2
[00:01:15:419 - 00:01:18:120] **Speaker 1:** across the X domain, so that's our governing equation.
[00:01:22:430 - 00:01:25:099] **Speaker 1:** Uh, if we integrate this, we end up with DU
[00:01:25:099 - 00:01:26:019] **Speaker 1:** by DX.
[00:01:29:360 - 00:01:32:419] **Speaker 1:** That has to equal some constant of integration, C1.
[00:01:37:260 - 00:01:40:500] **Speaker 1:** So times or divide both sides by AE so they
[00:01:40:500 - 00:01:40:959] **Speaker 1:** cancel.
[00:01:41:419 - 00:01:43:300] **Speaker 1:** So the boundary condition on the right-hand side at X
[00:01:43:300 - 00:01:46:779] **Speaker 1:** equal to L, we're going to enforce AE.
[00:01:47:949 - 00:01:52:150] **Speaker 1:** DU by the X at X equal to L.
[00:01:53:290 - 00:01:54:470] **Speaker 1:** Is equal to if not.
[00:01:55:919 - 00:01:58:050] **Speaker 1:** So we're told that it's a boundary condition on the
[00:01:58:050 - 00:01:58:389] **Speaker 1:** right.
[00:01:59:580 - 00:02:01:470] **Speaker 1:** And we can.
[00:02:03:169 - 00:02:06:610] **Speaker 1:** Substitute into our equation, so we've got D by DX
[00:02:06:610 - 00:02:09:720] **Speaker 1:** at X equal to L, rearranging for C1.
[00:02:10:660 - 00:02:14:000] **Speaker 1:** We've got F0 divided by A times E.
[00:02:15:729 - 00:02:18:399] **Speaker 1:** So we've integrated once we integrated a 2nd time because
[00:02:18:399 - 00:02:22:320] **Speaker 1:** it's 2nd order derivative, so integrating D by DX.
[00:02:24:729 - 00:02:36:899] **Speaker 1:** D X Integrating If not, By A E D X.
[00:02:39:210 - 00:02:42:649] **Speaker 1:** And we end up with a distribution for our displacement
[00:02:42:649 - 00:02:44:889] **Speaker 1:** within the rod, so you as a function of X.
[00:02:46:100 - 00:02:49:380] **Speaker 1:** Displacement in X with respect to the X coordinate equal
[00:02:49:380 - 00:02:56:330] **Speaker 1:** to if not, Divided by AEX plus some other constant
[00:02:56:490 - 00:02:57:750] **Speaker 1:** of integration C2.
[00:03:05:919 - 00:03:08:000] **Speaker 1:** So we can already see that it's a linear equation
[00:03:08:000 - 00:03:12:600] **Speaker 1:** as we expect, uh, varies linearly between uh left and
[00:03:12:600 - 00:03:13:619] **Speaker 1:** right boundaries.
[00:03:15:210 - 00:03:18:960] **Speaker 1:** So Just wait for a moment to finish writing.
[00:03:23:059 - 00:03:25:990] **Speaker 1:** So the last step is to apply the boundary condition
[00:03:25:990 - 00:03:28:050] **Speaker 1:** on the left, so X equals to 0.
[00:03:29:110 - 00:03:32:050] **Speaker 1:** We've got you at X equal to 0.
[00:03:33:009 - 00:03:35:250] **Speaker 1:** is equal to 0, so we know that the constant
[00:03:35:250 - 00:03:37:589] **Speaker 1:** C2 There's also 0.
[00:03:41:059 - 00:03:44:460] **Speaker 1:** So in summary, our displacement field U of X is
[00:03:44:460 - 00:03:45:179] **Speaker 1:** equal to.
[00:03:47:210 - 00:03:48:500] **Speaker 1:** If not over AE.
[00:03:49:470 - 00:03:50:789] **Speaker 1:** Multiplied by X.
[00:03:53:490 - 00:03:56:570] **Speaker 1:** Just with the separation of variable analytical solutions, we can
[00:03:56:570 - 00:04:00:649] **Speaker 1:** check that this equation or the solution satisfies the boundary
[00:04:00:649 - 00:04:01:080] **Speaker 1:** conditions.
[00:04:02:539 - 00:04:07:029] **Speaker 1:** Um And also the governing equation.
[00:04:07:229 - 00:04:08:509] **Speaker 1:** So I'll leave that for you to do if you
[00:04:08:509 - 00:04:10:970] **Speaker 1:** wish, but that's our, that's our analytical solution.
[00:04:11:899 - 00:04:12:929] **Speaker 1:** So why did we do this?
[00:04:13:020 - 00:04:14:899] **Speaker 1:** We, we just want to verify that our code works.
[00:04:15:059 - 00:04:17:558] **Speaker 1:** So we're going to use this expression to validate our,
[00:04:17:690 - 00:04:18:278] **Speaker 1:** our code.
[00:04:19:260 - 00:04:22:130] **Speaker 1:** So I'll just bring up the spider.
[00:04:53:119 - 00:04:54:970] **Speaker 1:** Maybe it's going to load, maybe not.
[00:05:14:720 - 00:05:14:959] **Speaker 0:** Cool.
[00:05:15:160 - 00:05:15:480] **Speaker 0:** All right.
[00:05:17:179 - 00:05:19:149] **Speaker 1:** Um, so there's some more code that I've chucked up
[00:05:19:149 - 00:05:21:380] **Speaker 1:** on Learn if you want to follow along, uh, but
[00:05:21:380 - 00:05:24:459] **Speaker 1:** essentially we've got our parameters, so some force being applied
[00:05:24:459 - 00:05:25:299] **Speaker 1:** on the right-hand side.
[00:05:25:369 - 00:05:27:500] **Speaker 1:** We've got a Young's modulus for the, the rod material
[00:05:27:500 - 00:05:27:799] **Speaker 1:** property.
[00:05:28:220 - 00:05:30:799] **Speaker 1:** We've got a radius and a corresponding cross-sectional area.
[00:05:32:399 - 00:05:33:190] **Speaker 1:** And a length.
[00:05:33:690 - 00:05:35:809] **Speaker 1:** So we've decided to split this up into 5 grid
[00:05:35:809 - 00:05:36:290] **Speaker 1:** points.
[00:05:36:649 - 00:05:38:850] **Speaker 1:** So 5 grid points, 4 spacings.
[00:05:40:630 - 00:05:41:850] **Speaker 1:** We've used Lin space.
[00:05:43:559 - 00:05:45:179] **Speaker 1:** Can you see that or should I zoom in?
[00:05:45:440 - 00:05:46:510] **Speaker 1:** That's, that's OK.
[00:05:47:250 - 00:05:48:529] **Speaker 1:** That's all good, um.
[00:05:49:929 - 00:05:53:700] **Speaker 1:** So we've got limb space using NumPy, uh, because we've
[00:05:53:700 - 00:05:56:380] **Speaker 1:** just got a 5x5 system, uh, we've just hardcoded this
[00:05:56:380 - 00:05:57:540] **Speaker 1:** with the matrix.
[00:05:57:929 - 00:06:01:299] **Speaker 1:** So if you're not familiar, you can have line breaks
[00:06:01:299 - 00:06:03:859] **Speaker 1:** within an array definition, so it can be helpful to
[00:06:03:859 - 00:06:04:500] **Speaker 1:** visualise that.
[00:06:04:670 - 00:06:05:679] **Speaker 1:** That's comparing us.
[00:06:06:380 - 00:06:09:549] **Speaker 1:** Um, against this metrics of coefficients A.
[00:06:11:720 - 00:06:14:440] **Speaker 1:** The right-hand side vector we've labelled B in the code,
[00:06:14:690 - 00:06:16:559] **Speaker 1:** uh, we've labelled it F in the notes.
[00:06:16:929 - 00:06:17:809] **Speaker 1:** Same, same thing.
[00:06:18:980 - 00:06:20:820] **Speaker 1:** Uh, the next step is to solve that system of
[00:06:20:820 - 00:06:23:339] **Speaker 1:** equations, and we'll talk a bit about some different methods
[00:06:23:339 - 00:06:25:809] **Speaker 1:** in chapter 4, but for now, for now we're just
[00:06:25:809 - 00:06:30:179] **Speaker 1:** using the Linn-Age solve function or method in Python, and
[00:06:30:179 - 00:06:31:220] **Speaker 1:** then we're going to plot the solution.
[00:06:31:279 - 00:06:34:119] **Speaker 1:** So we're plotting the solution from our finite difference scheme.
[00:06:34:739 - 00:06:38:109] **Speaker 1:** So there's 5 discrete points, as well as the analytical
[00:06:38:109 - 00:06:38:480] **Speaker 1:** solution.
[00:06:39:549 - 00:06:42:029] **Speaker 1:** The analytical solution has its own number of points that
[00:06:42:029 - 00:06:43:329] **Speaker 1:** we want to resolve the plot.
[00:06:44:010 - 00:06:45:790] **Speaker 1:** And using lens space again.
[00:06:46:619 - 00:06:50:119] **Speaker 1:** Uh, the analytical solution is equal to.
[00:06:51:070 - 00:06:53:630] **Speaker 1:** If not over 80 times X, and I've used that
[00:06:53:630 - 00:06:54:450] **Speaker 1:** X array.
[00:06:55:420 - 00:06:59:070] **Speaker 1:** X_A is the analytical array for the X values.
[00:06:59:779 - 00:07:02:220] **Speaker 1:** So that's going to be a vector, and then we're
[00:07:02:220 - 00:07:05:779] **Speaker 1:** plotting the analytical displacement field against the coordinates.
[00:07:15:279 - 00:07:16:410] **Speaker 1:** So this is our result.
[00:07:17:690 - 00:07:18:679] **Speaker 1:** It's very small.
[00:07:19:500 - 00:07:21:970] **Speaker 1:** Font, um, I don't know if I can zoom in,
[00:07:22:049 - 00:07:28:709] **Speaker 1:** but The Red crosses are the numerical solutions from the
[00:07:28:709 - 00:07:30:690] **Speaker 1:** finite difference, and blue is analytical.
[00:07:31:540 - 00:07:34:869] **Speaker 1:** Uh, if we zoom in to each individual point.
[00:07:39:429 - 00:07:42:350] **Speaker 1:** We can see that the numerical solution is pretty much
[00:07:42:350 - 00:07:43:529] **Speaker 1:** bang on the analytical.
[00:07:44:959 - 00:07:49:380] **Speaker 1:** Has anyone got any idea why there's no observable error
[00:07:50:000 - 00:07:52:440] **Speaker 1:** between the numerical and analytical for this case?
[00:07:58:989 - 00:08:01:209] **Speaker 1:** So I've zoomed in heaps here, 10 to 16.
[00:08:02:619 - 00:08:03:350] **Speaker 1:** Any ideas?
[00:08:12:640 - 00:08:16:239] **Speaker 1:** We know that the analytical solution is varying linearly with
[00:08:16:239 - 00:08:16:850] **Speaker 1:** X.
[00:08:18:700 - 00:08:20:890] **Speaker 1:** And the approximation that we're using.
[00:08:23:649 - 00:08:25:920] **Speaker 1:** Is finite difference, which is 2nd order accurate.
[00:08:29:059 - 00:08:32:820] **Speaker 1:** So, because it includes a second-order accurate formula, we should
[00:08:32:820 - 00:08:36:020] **Speaker 1:** be able to recover that linear, uh, function precisely, and
[00:08:36:020 - 00:08:38:280] **Speaker 1:** that's what we've observed in the, in the results.
[00:08:40:299 - 00:08:42:900] **Speaker 1:** So it doesn't matter how many points we have, we're
[00:08:42:900 - 00:08:45:780] **Speaker 1:** still going to, to capture this, uh, exactly, which is.
[00:08:46:979 - 00:08:47:630] **Speaker 1:** Which is neat.
[00:08:49:299 - 00:08:50:700] **Speaker 1:** So this is a finite difference with one.
[00:08:51:590 - 00:08:54:190] **Speaker 1:** 1D and 5 grid points, uh, we can also extend
[00:08:54:190 - 00:08:56:090] **Speaker 1:** this to an arbitrary number of grid points.
[00:08:58:039 - 00:09:02:000] **Speaker 1:** So I commented on Monday that these interior nodes all
[00:09:02:000 - 00:09:04:159] **Speaker 1:** have the same pattern, and we could create a for
[00:09:04:159 - 00:09:06:900] **Speaker 1:** loop that cycles through each of these interior nodes.
[00:09:07:679 - 00:09:11:989] **Speaker 1:** So that's what we've done in the Ah, example 1D
[00:09:12:299 - 00:09:12:890] **Speaker 1:** extended.
[00:09:14:130 - 00:09:18:150] **Speaker 1:** We'll set an arbitrary number of grid points and used
[00:09:18:570 - 00:09:21:409] **Speaker 1:** N to denote that variable and then use the 4
[00:09:21:409 - 00:09:24:309] **Speaker 1:** loop looping over those interior nodes.
[00:09:25:919 - 00:09:28:799] **Speaker 1:** Um, so it's including also the first and last rows,
[00:09:28:989 - 00:09:29:909] **Speaker 1:** which are slightly different.
[00:09:30:159 - 00:09:33:400] **Speaker 1:** So these boundary conditions are implied with I equal to
[00:09:33:400 - 00:09:37:200] **Speaker 1:** 0 or equal to N minus 1, the last row.
[00:09:38:450 - 00:09:41:429] **Speaker 1:** Everything else is the same, so I'll just plot that.
[00:09:45:640 - 00:09:51:140] **Speaker 1:** Again, it's recovering the Uh, analytical solution precisely because it's
[00:09:51:140 - 00:09:54:000] **Speaker 1:** using a, um, second order finite difference scheme.
[00:09:54:739 - 00:09:59:500] **Speaker 1:** So, yeah, linear equations sometimes aren't very exciting, but we
[00:09:59:500 - 00:10:01:440] **Speaker 1:** start with those because they're easier to solve.
[00:10:03:380 - 00:10:05:640] **Speaker 1:** Um, so this will be really helpful for your quiz.
[00:10:06:299 - 00:10:08:619] **Speaker 1:** One of the quiz questions is using this approach.
[00:10:09:309 - 00:10:13:400] **Speaker 1:** Uh, you'll also help, um, you'll also find that you
[00:10:13:400 - 00:10:14:059] **Speaker 1:** need to.
[00:10:14:869 - 00:10:17:570] **Speaker 1:** Uh, pick out values of the array.
[00:10:17:840 - 00:10:18:750] **Speaker 1:** So I've got you.
[00:10:19:640 - 00:10:21:179] **Speaker 1:** Being 50 elements long.
[00:10:22:359 - 00:10:23:590] **Speaker 1:** If you choose a value.
[00:10:24:609 - 00:10:28:750] **Speaker 1:** From this array, it returns an array.
[00:10:29:210 - 00:10:33:330] **Speaker 1:** So if you just call the 0th index of that
[00:10:33:330 - 00:10:35:030] **Speaker 1:** array, it returns the value.
[00:10:35:700 - 00:10:40:140] **Speaker 1:** So it's a bit Tedious, but that's how Python is
[00:10:40:140 - 00:10:40:650] **Speaker 1:** set up.
[00:10:41:119 - 00:10:44:119] **Speaker 1:** So if you wanted to, The midpoint.
[00:10:45:940 - 00:10:46:580] **Speaker 1:** Um.
[00:10:47:429 - 00:10:52:669] **Speaker 1:** And are you familiar with, I think it's, God, I
[00:10:52:669 - 00:10:54:070] **Speaker 1:** don't remember off the top of my head.
[00:10:54:150 - 00:10:55:030] **Speaker 1:** I think it's print.
[00:10:56:159 - 00:11:00:429] **Speaker 1:** If You're going to tell me if it's wrong, um.
[00:11:07:250 - 00:11:13:760] **Speaker 1:** Purely brackets Alright, so you can call.
[00:11:14:530 - 00:11:17:830] **Speaker 1:** Uh, variables with some precision, so that's worth.
[00:11:19:609 - 00:11:23:330] **Speaker 1:** Dot F3, I think.
[00:11:24:239 - 00:11:25:669] **Speaker 1:** Again, correct me if I'm wrong.
[00:11:27:750 - 00:11:30:700] **Speaker 1:** Which I am Colon Colon.
[00:11:31:820 - 00:11:33:219] **Speaker 1:** This is how much I use Python.
[00:11:34:530 - 00:11:41:830] **Speaker 1:** Um, You don't need the That's.
[00:11:43:119 - 00:11:44:679] **Speaker 1:** That's and dot.
[00:11:46:559 - 00:11:49:559] **Speaker 1:** Oh, that's not how I've done it before, alright, um.
[00:11:50:260 - 00:11:52:039] **Speaker 1:** Yeah, so you'll need, well, I don't.
[00:11:53:299 - 00:11:54:679] **Speaker 1:** That's not doing what I want though.
[00:11:56:549 - 00:11:57:940] **Speaker 1:** Yes, we do have the, yeah.
[00:11:58:390 - 00:11:58:869] **Speaker 1:** OK.
[00:12:00:200 - 00:12:03:950] **Speaker 1:** Um So it's reporting this value.
[00:12:04:820 - 00:12:08:049] **Speaker 1:** To 3 Decimal places.
[00:12:08:469 - 00:12:11:729] **Speaker 1:** Obviously because it's on the order of micrometres, so 10
[00:12:11:729 - 00:12:13:869] **Speaker 1:** to 6, it's giving 0.000.
[00:12:14:489 - 00:12:17:450] **Speaker 1:** Um, you use instead of, it gives sick days.
[00:12:23:520 - 00:12:24:119] **Speaker 1:** That's it.
[00:12:34:190 - 00:12:37:229] **Speaker 1:** Maybe because it's 7.80, it's reporting as 7.8.
[00:12:37:270 - 00:12:38:250] **Speaker 1:** That's a bit weird though.
[00:12:39:140 - 00:12:41:159] **Speaker 1:** I don't know, I'm not a big fan of Python,
[00:12:41:260 - 00:12:41:460] **Speaker 1:** but.
[00:12:42:650 - 00:12:45:250] **Speaker 1:** Um, we're using it, but we changed over from Matlab
[00:12:45:250 - 00:12:47:859] **Speaker 1:** a few years back, so you'll need this for your,
[00:12:48:020 - 00:12:49:700] **Speaker 1:** for your quiz, which is why I'm pointing it out.
[00:12:50:590 - 00:12:52:049] **Speaker 1:** But good luck, um.
[00:12:53:409 - 00:12:53:419] **Speaker 1:** Alright.
[00:12:55:710 - 00:12:55:950] **Speaker 1:** Cool.
[00:12:56:109 - 00:12:58:229] **Speaker 1:** Any questions on what we've done so far with this
[00:12:58:229 - 00:12:58:869] **Speaker 1:** finite differencing?
[00:12:59:070 - 00:13:01:909] **Speaker 1:** We, we derived them from the Taylor series expansions and
[00:13:01:909 - 00:13:03:570] **Speaker 1:** then applied it to that, that rod.
[00:13:06:049 - 00:13:06:690] **Speaker 1:** All clear.
[00:13:08:960 - 00:13:10:789] **Speaker 1:** Yeah All right.
[00:13:11:849 - 00:13:14:650] **Speaker 1:** So we'll continue on a little bit about, uh, deriving
[00:13:14:650 - 00:13:17:130] **Speaker 1:** some higher-order approximations for these finite differencing.
[00:13:17:690 - 00:13:20:729] **Speaker 1:** So we did the central difference, which was using the
[00:13:20:729 - 00:13:21:859] **Speaker 1:** left and right nodes.
[00:13:22:210 - 00:13:25:229] **Speaker 1:** Uh, what happens if we use more terms and maybe
[00:13:25:229 - 00:13:27:369] **Speaker 1:** we use another node, so I + 2 instead of
[00:13:27:369 - 00:13:28:950] **Speaker 1:** just these 1st, 1st 3.
[00:13:29:500 - 00:13:30:669] **Speaker 1:** So that's what we'll do next.
[00:13:36:979 - 00:13:39:280] **Speaker 1:** So now we're using a 4 point difference.
[00:13:39:820 - 00:13:45:140] **Speaker 1:** So we've got 11 + 1, I + 2, I
[00:13:45:140 - 00:13:45:820] **Speaker 1:** minus 1.
[00:13:46:770 - 00:13:49:049] **Speaker 1:** So our stencil is using 4 grid points rather than
[00:13:49:049 - 00:13:50:330] **Speaker 1:** just, just 3.
[00:13:52:049 - 00:13:55:130] **Speaker 1:** And we're going to still use Taylor series expansion about
[00:13:55:130 - 00:13:57:169] **Speaker 1:** these points, and I've kindly typed it out for you
[00:13:57:169 - 00:13:58:640] **Speaker 1:** so we don't have to type, uh, write them out
[00:13:58:640 - 00:14:01:580] **Speaker 1:** again in class, but it's just as we did, uh,
[00:14:01:650 - 00:14:02:150] **Speaker 1:** earlier.
[00:14:03:390 - 00:14:05:669] **Speaker 1:** So we're gonna assume that the finite difference approximation of
[00:14:05:669 - 00:14:10:469] **Speaker 1:** the first order derivative has this structure, so DU by
[00:14:10:469 - 00:14:11:150] **Speaker 1:** DX.
[00:14:12:239 - 00:14:14:030] **Speaker 1:** Evaluated at some node I.
[00:14:18:590 - 00:14:20:250] **Speaker 1:** It's gonna be 1 over X.
[00:14:24:520 - 00:14:29:340] **Speaker 1:** And then we're going to have Those 4 nodes, so
[00:14:29:340 - 00:14:30:919] **Speaker 1:** I minus 1 through 1 + 2.
[00:14:31:739 - 00:14:34:059] **Speaker 1:** And we're going to have a coefficient that corresponds to
[00:14:34:059 - 00:14:36:099] **Speaker 1:** each of those notes, so essentially weights.
[00:14:36:739 - 00:14:41:989] **Speaker 1:** So we've got alpha I minus 1 UI minus 1.
[00:14:42:869 - 00:14:43:890] **Speaker 1:** For the first good point.
[00:14:45:390 - 00:14:50:929] **Speaker 1:** And alpha I U I, alpha I + 1, UI
[00:14:50:929 - 00:14:54:869] **Speaker 1:** + 1, and alpha I + 2, UI + 2.
[00:14:58:849 - 00:15:01:450] **Speaker 1:** So these alpha terms are unknown coefficients that we're gonna
[00:15:01:450 - 00:15:02:190] **Speaker 1:** try and figure out.
[00:15:03:719 - 00:15:06:159] **Speaker 1:** For our central difference scheme, we figured out that they
[00:15:06:159 - 00:15:14:849] **Speaker 1:** were just a half, um, So, we'll, they were one.
[00:15:15:789 - 00:15:20:190] **Speaker 1:** -2 and 1 for a second order derivative, and they
[00:15:20:190 - 00:15:26:489] **Speaker 1:** were There are half for the first order derivative, so
[00:15:26:489 - 00:15:30:010] **Speaker 1:** D by DX we have half of I + 1.5
[00:15:30:010 - 00:15:31:169] **Speaker 1:** of I minus 1.
[00:15:36:510 - 00:15:41:109] **Speaker 1:** So we're going to Derive the term for these four
[00:15:41:109 - 00:15:44:919] **Speaker 1:** node points and seek these alpha values.
[00:15:45:130 - 00:15:46:150] **Speaker 1:** So that's our approach.
[00:15:47:030 - 00:15:49:380] **Speaker 1:** So what we're going to do next is substitute the,
[00:15:49:719 - 00:15:52:940] **Speaker 1:** uh, Taylor series terms into this equation.
[00:15:53:239 - 00:15:54:359] **Speaker 1:** So it's a little bit long.
[00:15:54:479 - 00:15:55:599] **Speaker 1:** We've got 4 lines.
[00:15:56:359 - 00:15:58:799] **Speaker 1:** So DU by DX.
[00:16:00:179 - 00:16:03:619] **Speaker 1:** At some, uh, discrete point within our domain, at point
[00:16:03:619 - 00:16:03:950] **Speaker 1:** I.
[00:16:04:969 - 00:16:10:309] **Speaker 1:** is equal to And I'm going to group all of
[00:16:10:309 - 00:16:10:919] **Speaker 1:** the.
[00:16:12:479 - 00:16:15:640] **Speaker 1:** Essentially first column, so all the UI terms.
[00:16:18:599 - 00:16:24:549] **Speaker 1:** So if I substitute in These four expressions into our
[00:16:24:549 - 00:16:25:219] **Speaker 1:** equation.
[00:16:26:010 - 00:16:36:719] **Speaker 1:** We've got you, I, Multiplied By Um Alpha I minus
[00:16:36:719 - 00:16:37:039] **Speaker 1:** 1.
[00:16:41:080 - 00:16:43:159] **Speaker 1:** We've got Alpha I.
[00:16:47:020 - 00:16:49:109] **Speaker 1:** We've got one times alpha i plus one.
[00:16:53:070 - 00:16:56:599] **Speaker 1:** And we've got alpha I + 2.
[00:17:06:790 - 00:17:09:609] **Speaker 1:** So we've grouped all of the UI terms.
[00:17:10:459 - 00:17:13:250] **Speaker 1:** In this large equation, so the first term of each
[00:17:13:250 - 00:17:15:180] **Speaker 1:** of these four expressions.
[00:17:16:079 - 00:17:19:930] **Speaker 1:** And we've got divide by data x from our coefficient.
[00:17:33:189 - 00:17:36:180] **Speaker 1:** We'll do this for each of those central columns, for
[00:17:36:180 - 00:17:37:969] **Speaker 1:** each of those terms of those tatter series.
[00:17:38:760 - 00:17:43:089] **Speaker 1:** So the next set of terms will be DU by
[00:17:43:089 - 00:17:44:689] **Speaker 1:** DX at I.
[00:17:45:170 - 00:17:46:709] **Speaker 1:** So that's the first order derivative.
[00:17:48:119 - 00:17:52:619] **Speaker 1:** The next one is the 2nd order derivative D2U by
[00:17:52:619 - 00:17:53:439] **Speaker 1:** DX2.
[00:17:55:459 - 00:17:59:339] **Speaker 1:** Um, we've got DX2 divided by data X, so we've
[00:17:59:339 - 00:18:01:349] **Speaker 1:** just got data X.
[00:18:02:270 - 00:18:05:790] **Speaker 1:** And the last set, we've got D cubed U by
[00:18:05:790 - 00:18:07:310] **Speaker 1:** DX cubed.
[00:18:08:180 - 00:18:10:939] **Speaker 1:** Multiplied by X2.
[00:18:20:439 - 00:18:24:339] **Speaker 1:** So that Second column, we have minus.
[00:18:25:750 - 00:18:27:390] **Speaker 1:** For alphai minus 1.
[00:18:33:489 - 00:18:36:010] **Speaker 1:** For the 2nd equation or 2nd expression, we don't have
[00:18:36:010 - 00:18:36:390] **Speaker 1:** any.
[00:18:37:619 - 00:18:39:489] **Speaker 1:** 1st order, 2nd order, 3rd order derivatives.
[00:18:39:609 - 00:18:40:510] **Speaker 1:** So we've got 0.
[00:18:42:349 - 00:18:44:709] **Speaker 1:** For the third one, we have plus.
[00:18:46:160 - 00:18:47:609] **Speaker 1:** Alpha I plus one.
[00:18:48:609 - 00:18:50:510] **Speaker 1:** And we've got 2.
[00:18:51:510 - 00:18:53:349] **Speaker 1:** Alpha 1 + 2.
[00:18:59:170 - 00:19:01:000] **Speaker 1:** So that's DU by DX.
[00:19:01:250 - 00:19:04:060] **Speaker 1:** Datax cancels with data x on the denominator, and we're
[00:19:04:060 - 00:19:05:569] **Speaker 1:** left with 2 alpha i + 2.
[00:19:12:819 - 00:19:16:189] **Speaker 1:** So we'll do the same for the 2nd order derivative.
[00:19:17:099 - 00:19:18:890] **Speaker 1:** We have a 12.
[00:19:21:589 - 00:19:25:060] **Speaker 1:** Of Alpha I, -1.
[00:19:27:229 - 00:19:29:800] **Speaker 1:** Nothing from the 2nd, and then we've got 12.
[00:19:30:989 - 00:19:32:380] **Speaker 1:** Alpha I one.
[00:19:34:839 - 00:19:39:280] **Speaker 1:** And we've got 2 2/2, which goes to 2.
[00:19:40:459 - 00:19:41:819] **Speaker 1:** Alpha I + 2.
[00:19:49:790 - 00:19:53:949] **Speaker 1:** Finally, our cubed derivatives, we've got minus.
[00:19:55:359 - 00:20:00:319] **Speaker 1:** 1/6 Alpha I minus 10.
[00:20:01:140 - 00:20:03:219] **Speaker 1:** 16 alpha 1 + 1.
[00:20:04:130 - 00:20:07:170] **Speaker 1:** And 8/6 alpha i plus 2.
[00:20:16:170 - 00:20:18:319] **Speaker 1:** So again, these coefficients alpha, we don't know what they
[00:20:18:319 - 00:20:18:979] **Speaker 1:** are yet.
[00:20:19:800 - 00:20:21:989] **Speaker 1:** What we want to do is end up with D
[00:20:21:989 - 00:20:26:219] **Speaker 1:** by DX at I, so, Essentially what we're going to
[00:20:26:219 - 00:20:30:219] **Speaker 1:** do is choose these coefficients, alphas, so that the terms
[00:20:30:219 - 00:20:32:640] **Speaker 1:** corresponding to D by DX sum to one.
[00:20:34:719 - 00:20:36:930] **Speaker 1:** And the terms corresponding to the other.
[00:20:37:319 - 00:20:40:439] **Speaker 1:** So U I D 2 U by DX2, D U
[00:20:40:439 - 00:20:43:119] **Speaker 1:** by DX cubed, sum to zero.
[00:20:53:180 - 00:20:54:619] **Speaker 1:** So we can write that out in a system of
[00:20:54:619 - 00:20:56:760] **Speaker 1:** equations in matrix form.
[00:21:05:569 - 00:21:11:359] **Speaker 1:** So our matrix Of coefficients, alpha 1 minus 1, alphai.
[00:21:12:170 - 00:21:15:170] **Speaker 1:** Alpha 1 + 1, Alpha 1 + 2.
[00:21:24:550 - 00:21:25:609] **Speaker 1:** So we've got.
[00:21:27:359 - 00:21:28:520] **Speaker 1:** For our first equation.
[00:21:29:949 - 00:21:31:910] **Speaker 1:** 1111.
[00:21:32:810 - 00:21:35:930] **Speaker 1:** That's our coefficients, 1111.
[00:21:39:329 - 00:21:41:989] **Speaker 1:** And we said that this is going to equal 0
[00:21:41:989 - 00:21:45:869] **Speaker 1:** because we don't want the, the 0 derivative.
[00:21:47:359 - 00:21:48:459] **Speaker 1:** For the 2nd equation.
[00:21:50:329 - 00:21:53:290] **Speaker 1:** We've got -1012.
[00:21:59:400 - 00:22:01:729] **Speaker 1:** And we want to recover this first order derivative, so
[00:22:01:729 - 00:22:02:510] **Speaker 1:** this is equal to one.
[00:22:04:989 - 00:22:09:939] **Speaker 1:** For that third equation, we've got 1/2, 0, 1/2 2.
[00:22:17:949 - 00:22:20:030] **Speaker 1:** And we don't want that 2nd order derivative, so it's
[00:22:20:030 - 00:22:20:770] **Speaker 1:** equal to 0.
[00:22:23:439 - 00:22:24:689] **Speaker 1:** And the 3rd.
[00:22:27:310 - 00:22:30:410] **Speaker 1:** We've got -1601686.
[00:22:41:380 - 00:22:42:180] **Speaker 1:** It's equal to 0.
[00:22:45:760 - 00:22:47:280] **Speaker 1:** So we've got a system of equations.
[00:22:47:359 - 00:22:49:329] **Speaker 1:** We've got 4 equations, 4 are nouns.
[00:22:49:449 - 00:22:52:530] **Speaker 1:** These coefficients alpha 1 minus 1 through alpha 1 +
[00:22:52:530 - 00:22:52:849] **Speaker 1:** 2.
[00:22:53:770 - 00:22:55:849] **Speaker 1:** We can solve that system of equations.
[00:22:56:670 - 00:23:02:410] **Speaker 1:** And we have our coefficients alphai minus 1, alpha i,
[00:23:02:939 - 00:23:06:430] **Speaker 1:** alphai + 1, and alphai + 2.
[00:23:07:479 - 00:23:09:579] **Speaker 1:** Is equal to minus 1/3.
[00:23:11:079 - 00:23:12:040] **Speaker 1:** Minus a half.
[00:23:13:560 - 00:23:16:290] **Speaker 1:** One And -16.
[00:23:32:319 - 00:23:35:609] **Speaker 1:** So we can substitute back into our general form and
[00:23:35:609 - 00:23:39:130] **Speaker 1:** we said that DU by DX is equal to 1
[00:23:39:130 - 00:23:43:569] **Speaker 1:** over x of these coefficients times the displacements of those
[00:23:43:569 - 00:23:45:810] **Speaker 1:** nodes and we're left with DU.
[00:23:46:750 - 00:23:47:729] **Speaker 1:** By DX.
[00:23:50:630 - 00:23:54:030] **Speaker 1:** At some note I equal to 1 over delta X.
[00:23:57:290 - 00:23:58:819] **Speaker 1:** So we've got -1/3.
[00:24:01:979 - 00:24:03:619] **Speaker 1:** Times UI minus 1.
[00:24:05:489 - 00:24:07:020] **Speaker 1:** We've got -5.
[00:24:08:790 - 00:24:15:630] **Speaker 1:** UI Plus UI + 1 and -16.
[00:24:17:109 - 00:24:19:270] **Speaker 1:** Uh, UI + 2.
[00:24:22:119 - 00:24:25:739] **Speaker 1:** Now we've used those Taylor series expansions and we've got
[00:24:25:739 - 00:24:27:140] **Speaker 1:** some residuals or remainder.
[00:24:28:380 - 00:24:31:609] **Speaker 1:** Any idea what remainder we have for this equation?
[00:24:41:599 - 00:24:44:119] **Speaker 1:** We've gone up to and including those 3rd order derivatives
[00:24:44:119 - 00:24:46:099] **Speaker 1:** and then we've got the remainder of data x 4.
[00:24:47:810 - 00:24:51:089] **Speaker 1:** So if we think back to our math courses, if
[00:24:51:089 - 00:24:53:209] **Speaker 1:** we've got data x 4 and then we divide by
[00:24:53:209 - 00:24:55:890] **Speaker 1:** data x, it's scaling with data x 3.
[00:24:57:890 - 00:25:00:959] **Speaker 1:** So we've got some remainder of data x to the
[00:25:00:959 - 00:25:01:520] **Speaker 1:** power of 3.
[00:25:10:430 - 00:25:12:939] **Speaker 1:** So this is a 3rd or accurate finite difference formula.
[00:25:14:060 - 00:25:17:020] **Speaker 1:** It's not central difference, it's using um an extra point
[00:25:17:020 - 00:25:18:219] **Speaker 1:** at UI + 2.
[00:25:19:500 - 00:25:21:329] **Speaker 1:** And we can rewrite this just so that it's a
[00:25:21:329 - 00:25:22:319] **Speaker 1:** bit easier to read.
[00:25:24:969 - 00:25:26:619] **Speaker 1:** We've got -2.
[00:25:28:609 - 00:25:30:430] **Speaker 1:** Times Ui minus 1.
[00:25:32:689 - 00:25:34:660] **Speaker 1:** -3 UI.
[00:25:35:900 - 00:25:38:300] **Speaker 1:** Plus 6 UI plus 1.
[00:25:39:140 - 00:25:39:959] **Speaker 1:** And minus UI.
[00:25:41:180 - 00:25:41:790] **Speaker 1:** Plus 2.
[00:25:42:689 - 00:25:46:089] **Speaker 1:** Divided by 6 delta X.
[00:25:47:510 - 00:25:49:020] **Speaker 1:** Plus their order of data execute.
[00:26:07:489 - 00:26:09:859] **Speaker 1:** So a little bit painful, but you can do the
[00:26:09:859 - 00:26:12:560] **Speaker 1:** same for the central difference scheme and recover the same
[00:26:12:939 - 00:26:13:619] **Speaker 1:** uh set.
[00:26:14:060 - 00:26:17:619] **Speaker 1:** In fact, people do this and, uh, here we've got
[00:26:17:619 - 00:26:18:560] **Speaker 1:** a summary table.
[00:26:19:020 - 00:26:20:859] **Speaker 1:** So this is the central difference.
[00:26:21:699 - 00:26:23:390] **Speaker 1:** Uh, finite difference coefficients.
[00:26:25:599 - 00:26:29:199] **Speaker 1:** For 1st order derivatives and 2nd order derivatives and to
[00:26:29:199 - 00:26:31:800] **Speaker 1:** 2nd order accuracy and 4th order accuracy.
[00:26:32:079 - 00:26:34:709] **Speaker 1:** So what we've done in class already is the boundary
[00:26:34:709 - 00:26:37:969] **Speaker 1:** condition we use that 1st order derivative, 2nd order accurate.
[00:26:38:239 - 00:26:41:680] **Speaker 1:** So we had coefficients of -5 and 1/2 for those
[00:26:41:680 - 00:26:42:560] **Speaker 1:** neighbouring nodes.
[00:26:43:000 - 00:26:45:349] **Speaker 1:** And we also did the 2nd order derivative, 2nd order
[00:26:45:349 - 00:26:46:300] **Speaker 1:** accurate scheme.
[00:26:46:760 - 00:26:48:640] **Speaker 1:** So we had that 1 minus 21.
[00:26:49:420 - 00:26:51:829] **Speaker 1:** And that's what we saw in that that matrix of
[00:26:51:829 - 00:26:54:310] **Speaker 1:** coefficients as well, and we coded it.
[00:26:55:750 - 00:26:59:349] **Speaker 1:** So the 4th order terms encompass an extra node on
[00:26:59:349 - 00:27:01:430] **Speaker 1:** each side, and it's more accurate.
[00:27:02:640 - 00:27:08:770] **Speaker 1:** Uh I guess we can open Wikipedia.
[00:27:08:849 - 00:27:47:500] **Speaker 1:** It's not super exciting, but coefficient So you can go
[00:27:47:500 - 00:27:50:459] **Speaker 1:** nuts if you want, there's heaps of different, uh, sets
[00:27:50:459 - 00:27:51:459] **Speaker 1:** of coefficients.
[00:27:52:760 - 00:27:54:890] **Speaker 1:** And now that you know how to do it yourself,
[00:27:54:930 - 00:27:56:969] **Speaker 1:** you can choose an arbitrary sort of stencil number of
[00:27:56:969 - 00:27:58:719] **Speaker 1:** grid points and create your own um.
[00:28:00:010 - 00:28:01:079] **Speaker 1:** Finite difference pattern.
[00:28:01:609 - 00:28:04:250] **Speaker 1:** So yeah, nothing too scary, um.
[00:28:04:969 - 00:28:06:699] **Speaker 1:** Uh, I think it's important to understand where it comes
[00:28:06:699 - 00:28:09:300] **Speaker 1:** from, so you understand the accuracy and that it all
[00:28:09:300 - 00:28:10:969] **Speaker 1:** depends on the spacing data X.
[00:28:11:459 - 00:28:13:160] **Speaker 1:** So we talk about mesh convergence quite a bit.
[00:28:13:800 - 00:28:16:989] **Speaker 1:** Um, as you refine the, the spacings data X, the,
[00:28:17:119 - 00:28:20:439] **Speaker 1:** the solution should get accurate with 3rd order for the
[00:28:20:439 - 00:28:22:459] **Speaker 1:** scheme and 2nd order for the central difference.
[00:28:23:469 - 00:28:24:390] **Speaker 1:** For second order crip.
[00:28:26:780 - 00:28:27:500] **Speaker 1:** All right.
[00:28:31:040 - 00:28:34:949] **Speaker 1:** So just an example, pulling from this table, the finite
[00:28:34:949 - 00:28:38:719] **Speaker 1:** difference of the 1st order derivative, 2nd-order accurate.
[00:28:39:109 - 00:28:41:489] **Speaker 1:** So 1st order derivative, 2nd-order accurate.
[00:28:44:300 - 00:28:46:469] **Speaker 1:** Using the central different scheme, it's going to be DU
[00:28:47:130 - 00:28:49:640] **Speaker 1:** via DX at some position.
[00:28:54:719 - 00:28:56:599] **Speaker 1:** Because it's a first order accurate scheme, it's always going
[00:28:56:599 - 00:28:59:300] **Speaker 1:** to be 1 over x as the denominator.
[00:29:00:310 - 00:29:06:229] **Speaker 1:** And We read this by Selecting the coefficients for Ui
[00:29:06:229 - 00:29:08:530] **Speaker 1:** minus 1 is going to be -5.
[00:29:13:619 - 00:29:15:839] **Speaker 1:** And the coefficient for UI + 1 is 1/2.
[00:29:23:890 - 00:29:27:530] **Speaker 1:** And what order of remainder do we expect for this?
[00:29:32:020 - 00:29:33:030] **Speaker 1:** If it's a 2nd order.
[00:29:40:180 - 00:29:42:140] **Speaker 1:** I don't know, I still like to ask questions, maybe
[00:29:42:140 - 00:29:44:069] **Speaker 1:** you're thinking in the in silence.
[00:29:45:489 - 00:29:47:140] **Speaker 1:** Um, so order delta X2.
[00:29:49:109 - 00:29:50:339] **Speaker 1:** Because it's second-order accurate.
[00:29:50:550 - 00:29:52:109] **Speaker 1:** We'll do the same for the 4th order.
[00:29:52:709 - 00:29:56:209] **Speaker 1:** So we could approximate D by Dx with 4 grid
[00:29:56:209 - 00:29:56:689] **Speaker 1:** points.
[00:29:57:069 - 00:29:59:900] **Speaker 1:** So I minus 2, I minus 1, I + 1,
[00:29:59:939 - 00:30:00:750] **Speaker 1:** and I + 2.
[00:30:01:109 - 00:30:02:449] **Speaker 1:** So we'll write that out as well.
[00:30:07:800 - 00:30:09:739] **Speaker 1:** So it's still 1 over Da X.
[00:30:10:949 - 00:30:14:270] **Speaker 1:** And we've now got 1/12 minus 2/3, 2/3, and minus
[00:30:14:270 - 00:30:14:979] **Speaker 1:** 1/12.
[00:30:17:410 - 00:30:21:900] **Speaker 1:** So we've got 1/12 times UI minus 2.
[00:30:24:229 - 00:30:27:599] **Speaker 1:** -2/3 of U, I minus 1.
[00:30:31:640 - 00:30:33:030] **Speaker 1:** Plus 2/3.
[00:30:34:609 - 00:30:40:510] **Speaker 1:** UI plus 1 -1/12 UI + 2.
[00:30:45:500 - 00:30:47:739] **Speaker 1:** And this is 4th order accurate, we've got some residual
[00:30:47:739 - 00:30:50:579] **Speaker 1:** or remainder that scales with data x 4.
[00:30:52:979 - 00:30:54:420] **Speaker 1:** And we've got another one even still.
[00:30:54:540 - 00:30:57:420] **Speaker 1:** So, uh, finite difference for the 2nd order derivatives, 2nd-order
[00:30:57:420 - 00:31:00:040] **Speaker 1:** accurate, uh, this is what we did earlier.
[00:31:00:849 - 00:31:02:270] **Speaker 1:** But pulling from that table.
[00:31:04:439 - 00:31:09:069] **Speaker 1:** Second-order derivative, 2nd-order accuracy, we've got 11 minus 1, minus
[00:31:09:069 - 00:31:11:439] **Speaker 1:** 2 Ui and 1 UI + 1.
[00:31:12:869 - 00:31:13:670] **Speaker 1:** So this grid.
[00:31:14:890 - 00:31:16:609] **Speaker 1:** U by DX 2.
[00:31:17:900 - 00:31:22:099] **Speaker 1:** At some node I equal to 1 over X2 this
[00:31:22:099 - 00:31:24:699] **Speaker 1:** time because it's 2nd order derivative.
[00:31:26:130 - 00:31:30:449] **Speaker 1:** And our coefficients we said was 1 times Ui minus
[00:31:30:449 - 00:31:30:829] **Speaker 1:** 1.
[00:31:32:439 - 00:31:34:170] **Speaker 1:** -2 times UI.
[00:31:35:250 - 00:31:37:979] **Speaker 1:** And positive U I plus 1.
[00:31:43:130 - 00:31:45:550] **Speaker 1:** And this is 2nd order accurate, so it scales with
[00:31:45:550 - 00:31:46:250] **Speaker 1:** the X2.
[00:32:02:410 - 00:32:06:250] **Speaker 1:** Alright, so how can we show this?
[00:32:06:449 - 00:32:09:569] **Speaker 1:** So we showed earlier with the rod, um, that the
[00:32:09:569 - 00:32:14:969] **Speaker 1:** second order accurate finite differencing could capture the Solution exactly.
[00:32:15:810 - 00:32:18:209] **Speaker 1:** So what we're gonna do is add more terms.
[00:32:18:369 - 00:32:21:729] **Speaker 1:** So we're gonna consider a fifth-order polynomial and see how
[00:32:21:729 - 00:32:25:050] **Speaker 1:** these finite differencing, um, schemes.
[00:32:25:869 - 00:32:28:890] **Speaker 1:** Uh, match this, this analytical function.
[00:32:29:780 - 00:32:31:599] **Speaker 1:** So for the 4th order.
[00:32:38:119 - 00:32:38:699] **Speaker 1:** Accurate.
[00:32:40:790 - 00:32:43:979] **Speaker 1:** Finite difference scheme, the remainder.
[00:32:49:400 - 00:32:50:930] **Speaker 1:** Which we can label with R.
[00:32:52:089 - 00:32:52:849] **Speaker 1:** Is.
[00:32:54:739 - 00:33:02:020] **Speaker 1:** Proportional To delta X to the 4.
[00:33:02:839 - 00:33:05:969] **Speaker 1:** So if we have the um.
[00:33:06:760 - 00:33:12:199] **Speaker 1:** Grid spacing or data spacing, then we expect the solution
[00:33:12:199 - 00:33:17:089] **Speaker 1:** to be What's that tooth power 4 better, essentially.
[00:33:18:140 - 00:33:20:949] **Speaker 1:** Um, so what we can do is take the log.
[00:33:22:579 - 00:33:25:979] **Speaker 1:** Of both sides, so we've got log residual or log
[00:33:25:979 - 00:33:26:500] **Speaker 1:** remainder.
[00:33:29:760 - 00:33:32:540] **Speaker 1:** Is proportional to the log.
[00:33:33:569 - 00:33:36:270] **Speaker 1:** Of delta X to the 4.
[00:33:45:290 - 00:33:50:150] **Speaker 1:** And We've taken the log because we can chuck 4
[00:33:50:150 - 00:33:53:849] **Speaker 1:** in front of log, and we're left with 4 log
[00:33:54:430 - 00:33:55:250] **Speaker 1:** delta X.
[00:33:59:270 - 00:34:03:310] **Speaker 1:** And if we plot the log of the residual or
[00:34:03:310 - 00:34:06:630] **Speaker 1:** remainder against the log of delta X spacing on the
[00:34:06:630 - 00:34:11:000] **Speaker 1:** x-axis, we should recover the slope or gradient of 4.
[00:34:11:310 - 00:34:13:830] **Speaker 1:** So that's why we've we've done it this way.
[00:34:20:070 - 00:34:24:830] **Speaker 1:** So that's what chapter 3 example finite difference error.pi is
[00:34:24:830 - 00:34:25:290] **Speaker 1:** going to be doing.
[00:34:27:340 - 00:34:29:908] **Speaker 1:** Just briefly, we've got a length of the domain.
[00:34:30:870 - 00:34:33:620] **Speaker 1:** We've got a set of grid points.
[00:34:34:010 - 00:34:37:550] **Speaker 1:** We've got the analytical solution or the polynomial, so that
[00:34:37:550 - 00:34:38:189] **Speaker 1:** 5th order.
[00:34:39:857 - 00:34:47:030] **Speaker 1:** Function We're going to approximate the first order derivative so
[00:34:47:260 - 00:34:50:370] **Speaker 1:** we can just differentiate once and have the analytical solution
[00:34:50:370 - 00:34:50:888] **Speaker 1:** to that.
[00:34:51:209 - 00:34:53:530] **Speaker 1:** And then we're going to use finite differencing to approximate
[00:34:53:530 - 00:34:56:300] **Speaker 1:** that first order derivative.
[00:34:58:820 - 00:35:03:209] **Speaker 1:** So I won't go into too much detail.
[00:35:05:800 - 00:35:08:679] **Speaker 1:** D DY by D X blah blah blah.
[00:35:10:629 - 00:35:12:669] **Speaker 1:** So we want to plot the analytical solution and then
[00:35:12:669 - 00:35:14:030] **Speaker 1:** we want to plot the errors.
[00:35:15:850 - 00:35:20:479] **Speaker 1:** And hopefully recover the The 4th water slope.
[00:35:25:080 - 00:35:28:300] **Speaker 1:** So this first plot is just the polynomial.
[00:35:30:149 - 00:35:31:090] **Speaker 1:** Analytical solution.
[00:35:32:370 - 00:35:33:750] **Speaker 1:** And we are.
[00:35:38:649 - 00:35:41:709] **Speaker 1:** evaluating the derivative at the midpoint.
[00:35:44:169 - 00:35:45:600] **Speaker 1:** So it must be at 5.
[00:35:48:709 - 00:35:51:459] **Speaker 1:** If we plot log of the error.
[00:35:52:560 - 00:35:53:379] **Speaker 1:** This is way too small.
[00:35:53:500 - 00:35:55:780] **Speaker 1:** OK, so the vertical axis is log of error.
[00:35:55:860 - 00:35:56:800] **Speaker 1:** So log of R.
[00:35:57:550 - 00:36:00:709] **Speaker 1:** Against log of data X, log of data X.
[00:36:01:600 - 00:36:03:860] **Speaker 1:** And if we take the slope, so log our over
[00:36:03:860 - 00:36:06:040] **Speaker 1:** log data, we should recover 4.
[00:36:06:560 - 00:36:10:520] **Speaker 1:** So 4th order accurate is shown in orange and 2nd
[00:36:10:520 - 00:36:11:659] **Speaker 1:** order accurate in blue.
[00:36:15:179 - 00:36:20:239] **Speaker 1:** So I feel like I'm selling MATLAB, but in MATLAB
[00:36:20:239 - 00:36:21:879] **Speaker 1:** we just have a toolkit that we can look at
[00:36:21:879 - 00:36:23:899] **Speaker 1:** the slopes of these curves.
[00:36:24:280 - 00:36:28:439] **Speaker 1:** In Python, we can use Polyfit directly and then evaluate
[00:36:28:439 - 00:36:28:739] **Speaker 1:** these.
[00:36:29:280 - 00:36:30:080] **Speaker 1:** So P1.
[00:36:32:209 - 00:36:33:729] **Speaker 1:** Has a slope of 2.
[00:36:35:209 - 00:36:38:030] **Speaker 1:** It is as expected, so that's our 2nd order accurate
[00:36:38:030 - 00:36:43:050] **Speaker 1:** finite differencing and P2 has a 4th order within some
[00:36:43:050 - 00:36:45:290] **Speaker 1:** numerical precision.
[00:36:47:679 - 00:36:49:320] **Speaker 1:** All right, so that's reassuring.
[00:36:53:149 - 00:36:53:159] **Speaker 1:** Hm.
[00:36:54:350 - 00:36:57:350] **Speaker 1:** Any, any questions on finite differencing?
[00:36:59:770 - 00:37:00:280] **Speaker 1:** So.
[00:37:01:159 - 00:37:03:280] **Speaker 1:** Hopefully convince you that we've got 2nd order and 4th
[00:37:03:280 - 00:37:04:060] **Speaker 1:** order accuracy.
[00:37:04:949 - 00:37:09:360] **Speaker 1:** And why having a, a mesh, a smaller grid sizing
[00:37:09:360 - 00:37:13:360] **Speaker 1:** is good because we have a, um, a closer approximation
[00:37:13:360 - 00:37:14:060] **Speaker 1:** to the true solution.
[00:37:17:520 - 00:37:18:840] **Speaker 1:** No questions, right.
[00:37:19:780 - 00:37:20:239] **Speaker 1:** OK.
[00:37:20:659 - 00:37:22:739] **Speaker 1:** So we're going to apply this to 2 dimensions.
[00:37:22:949 - 00:37:25:169] **Speaker 1:** So so far we've done it in 1D and now
[00:37:25:169 - 00:37:26:280] **Speaker 1:** we'll do it in 2D.
[00:37:26:899 - 00:37:28:850] **Speaker 1:** So we're going to solve the energy equation on a
[00:37:28:850 - 00:37:30:899] **Speaker 1:** flat plate that we just derived earlier.
[00:37:31:020 - 00:37:32:139] **Speaker 1:** So that Laplace equation.
[00:37:34:320 - 00:37:37:929] **Speaker 1:** And instead of being 1D, now we've got 2D.
[00:37:38:320 - 00:37:40:800] **Speaker 1:** finite difference requires a structured grid.
[00:37:41:070 - 00:37:42:600] **Speaker 1:** So we've got a nice structured grid here.
[00:37:43:409 - 00:37:45:780] **Speaker 1:** They don't have to have uniform spacings in X and
[00:37:45:780 - 00:37:46:100] **Speaker 1:** Y.
[00:37:46:459 - 00:37:48:300] **Speaker 1:** Uh, we'll come to that later, but in this case,
[00:37:48:340 - 00:37:49:939] **Speaker 1:** we've just got a uniform grid of points.
[00:37:50:659 - 00:37:53:879] **Speaker 1:** We're starting from 11 in the lower left and we've
[00:37:53:879 - 00:37:55:550] **Speaker 1:** gone to NX + 11.
[00:37:56:250 - 00:37:59:489] **Speaker 1:** In X and 1 N Y plus 1 and Y.
[00:38:01:090 - 00:38:05:219] **Speaker 1:** If we analyse a node at an arbitrary point IJ.
[00:38:06:000 - 00:38:08:959] **Speaker 1:** The north is J +1, south J minus 1, right
[00:38:08:959 - 00:38:11:320] **Speaker 1:** is I +1, left is I minus 1.
[00:38:15:699 - 00:38:19:179] **Speaker 1:** So just as a quick recap, our energy conservation equation
[00:38:19:179 - 00:38:20:820] **Speaker 1:** derived earlier for a flat plate.
[00:38:21:260 - 00:38:23:500] **Speaker 1:** So we assumed those insulated boundary conditions on the front
[00:38:23:500 - 00:38:24:100] **Speaker 1:** and back.
[00:38:24:580 - 00:38:28:020] **Speaker 1:** We've recovered the Laplace equation in 2D.
[00:38:28:129 - 00:38:31:419] **Speaker 1:** So D2T by DX2 plus D2T by DY2.
[00:38:38:120 - 00:38:44:060] **Speaker 1:** And We've just derived the signal derivatives earlier so we
[00:38:44:060 - 00:38:45:320] **Speaker 1:** can discretize this equation.
[00:38:46:169 - 00:38:47:360] **Speaker 1:** Using our sensors.
[00:38:48:050 - 00:38:51:209] **Speaker 1:** Now these are partial derivatives instead of full derivatives, but
[00:38:51:209 - 00:38:52:810] **Speaker 1:** we can still use our finite differencing.
[00:38:53:939 - 00:38:57:790] **Speaker 1:** So D2 T I D X2.
[00:39:00:909 - 00:39:03:870] **Speaker 1:** This is our first term, so we're differentiating T in
[00:39:03:870 - 00:39:04:639] **Speaker 1:** the X direction.
[00:39:07:419 - 00:39:16:600] **Speaker 1:** So this is equal to Uh, so we've got I
[00:39:16:600 - 00:39:18:479] **Speaker 1:** minus 1, I and I + 1.
[00:39:20:449 - 00:39:23:850] **Speaker 1:** If we are differentiating in X, we're looking at how
[00:39:23:850 - 00:39:25:610] **Speaker 1:** the temperature field varies in X.
[00:39:25:899 - 00:39:28:389] **Speaker 1:** So we're holding the Y component constant.
[00:39:28:929 - 00:39:32:590] **Speaker 1:** So J, the index J remains constant for the other,
[00:39:32:939 - 00:39:33:870] **Speaker 1:** other variables.
[00:39:34:250 - 00:39:36:570] **Speaker 1:** So we've got T1 + 1.
[00:39:38:439 - 00:39:39:330] **Speaker 1:** At point J.
[00:39:40:709 - 00:39:43:040] **Speaker 1:** -2 TIJ.
[00:39:44:260 - 00:39:46:459] **Speaker 1:** Plus DI minus 1 J.
[00:39:56:310 - 00:39:58:479] **Speaker 1:** So we've got the i + 1, I I +
[00:39:58:479 - 00:39:58:909] **Speaker 1:** 1.
[00:39:59:379 - 00:40:02:560] **Speaker 1:** Again, J is held constant, it's a partial derivative and
[00:40:02:659 - 00:40:03:360] **Speaker 1:** and X coordinate.
[00:40:06:270 - 00:40:08:939] **Speaker 1:** So do the same for the the derivative in Y.
[00:40:09:179 - 00:40:13:100] **Speaker 1:** So D2, T I DY2.
[00:40:15:169 - 00:40:16:850] **Speaker 1:** Now we're looking at how the temperature varies in the
[00:40:16:850 - 00:40:20:850] **Speaker 1:** vertical direction, so we're now holding I constant and varying
[00:40:20:850 - 00:40:22:129] **Speaker 1:** the J index.
[00:40:23:350 - 00:40:25:320] **Speaker 1:** So the J index is going to vary from J
[00:40:25:320 - 00:40:27:959] **Speaker 1:** +1, J and J minus 1.
[00:40:38:370 - 00:40:41:770] **Speaker 1:** And again, we're veering in the vertical direction, so we're
[00:40:41:770 - 00:40:43:530] **Speaker 1:** scaling with delta Y2.
[00:40:46:610 - 00:40:50:889] **Speaker 1:** And our residual or remainder scales with data y squared.
[00:40:58:540 - 00:41:00:870] **Speaker 1:** So I've applied the finite difference stencil to both of
[00:41:00:870 - 00:41:01:510] **Speaker 1:** these terms.
[00:41:01:810 - 00:41:03:429] **Speaker 1:** We can now group them together.
[00:41:04:070 - 00:41:05:870] **Speaker 1:** And substitute into a Laplace equation.
[00:41:06:639 - 00:41:09:810] **Speaker 1:** So we've got our 1st fraction and our 2nd fraction
[00:41:09:810 - 00:41:10:689] **Speaker 1:** equal to 0.
[00:41:11:389 - 00:41:12:100] **Speaker 1:** So tea.
[00:41:13:479 - 00:41:19:399] **Speaker 1:** I + 1 J minus 2 TIJ plus TI minus
[00:41:19:399 - 00:41:20:239] **Speaker 1:** 1 J.
[00:41:21:100 - 00:41:22:239] **Speaker 1:** Over Dederick squid.
[00:41:24:520 - 00:41:28:159] **Speaker 1:** Plus TIJ plus 1.
[00:41:29:199 - 00:41:34:969] **Speaker 1:** -2 TIJ plus TIJ minus 1 over Y2.
[00:41:52:860 - 00:41:54:899] **Speaker 1:** In this example, we've got a uniform grid.
[00:41:55:300 - 00:41:58:590] **Speaker 1:** So that means that the spacings in X and Y
[00:41:59:060 - 00:41:59:850] **Speaker 1:** are equal.
[00:42:00:219 - 00:42:02:340] **Speaker 1:** So delta X is equal to &DeltaY.
[00:42:03:639 - 00:42:07:840] **Speaker 1:** If that's true, then we can multiply through by delta
[00:42:07:840 - 00:42:13:909] **Speaker 1:** Y2, X2, and we end up with TI + 1
[00:42:13:909 - 00:42:14:199] **Speaker 1:** J.
[00:42:17:360 - 00:42:19:600] **Speaker 1:** And we've got TI minus 1 J.
[00:42:26:250 - 00:42:28:310] **Speaker 1:** And we've got TIJ +1.
[00:42:32:100 - 00:42:33:979] **Speaker 1:** And TIJ minus 1.
[00:42:37:610 - 00:42:41:889] **Speaker 1:** And we've got 2 times TIJ and 2 times TIJ.
[00:42:42:010 - 00:42:46:330] **Speaker 1:** We'll group them together and we've got -4 TIJ.
[00:42:57:330 - 00:43:01:290] **Speaker 1:** So this stencil was applied to an arbitrary point located
[00:43:01:290 - 00:43:02:090] **Speaker 1:** at IJ.
[00:43:02:610 - 00:43:04:929] **Speaker 1:** So this applies or holds for all of the interior
[00:43:04:929 - 00:43:05:629] **Speaker 1:** grid points.
[00:43:10:060 - 00:43:12:939] **Speaker 1:** And the example here, all the interior grid points.
[00:43:17:409 - 00:43:19:580] **Speaker 1:** Are those not at the boundary because they're anterior.
[00:43:27:060 - 00:43:28:679] **Speaker 1:** So we're going to solve this heat equation on this
[00:43:28:679 - 00:43:31:050] **Speaker 1:** plate and we've got 4 boundary conditions here.
[00:43:31:330 - 00:43:35:570] **Speaker 1:** Can anyone remember what type of boundary condition these are?
[00:43:36:500 - 00:43:38:379] **Speaker 1:** Are they Dirk Clay, Neumann, or Robin?
[00:43:41:459 - 00:43:41:969] **Speaker 1:** Yeah, there.
[00:43:42:620 - 00:43:45:639] **Speaker 1:** So we've prescribed the temperature field to be equal to
[00:43:46:100 - 00:43:49:899] **Speaker 1:** these fixed values, 0, 50, 75, or 100, depending on
[00:43:49:899 - 00:43:52:060] **Speaker 1:** which edge the boundary lies on.
[00:43:53:399 - 00:43:59:550] **Speaker 1:** Um What happens at the corners?
[00:44:01:149 - 00:44:04:070] **Speaker 1:** We've said this edge is 75 and the top edge
[00:44:04:070 - 00:44:05:030] **Speaker 1:** is equal to 100.
[00:44:12:530 - 00:44:16:050] **Speaker 1:** Essentially, we've got a discontinuity at the corner.
[00:44:16:209 - 00:44:17:889] **Speaker 1:** We're jumping from 75 to 100.
[00:44:18:560 - 00:44:20:870] **Speaker 1:** Uh, you'll find that we don't actually need this value
[00:44:21:090 - 00:44:24:199] **Speaker 1:** to discretize our solution, but it might be wise just
[00:44:24:199 - 00:44:25:649] **Speaker 1:** to use an average of the two.
[00:44:25:929 - 00:44:27:449] **Speaker 1:** So 75 and 100/2.
[00:44:30:949 - 00:44:32:939] **Speaker 1:** So the points on the boundary don't need to be
[00:44:32:939 - 00:44:35:639] **Speaker 1:** considered at all because they're imposed directly.
[00:44:37:889 - 00:44:42:449] **Speaker 1:** And so we've gone from a 5x5 grid of 25
[00:44:42:449 - 00:44:44:510] **Speaker 1:** degrees of 25 nodes.
[00:44:45:090 - 00:44:47:479] **Speaker 1:** We've only got a 3 by 3 grid of unknowns,
[00:44:47:770 - 00:44:51:169] **Speaker 1:** so degrees of freedom, and we're gonna apply equation 314
[00:44:51:169 - 00:44:52:409] **Speaker 1:** for these interior grid points.
[00:44:54:709 - 00:44:58:629] **Speaker 1:** So as an example, we'll analyse node 22, so it's
[00:44:58:629 - 00:44:59:330] **Speaker 1:** on the lower left.
[00:45:01:639 - 00:45:09:879] **Speaker 1:** And we have No 22.
[00:45:10:209 - 00:45:10:969] **Speaker 1:** So we're substituting I.
[00:45:12:570 - 00:45:14:669] **Speaker 1:** Plus 1, so it's gonna be T3 2.
[00:45:18:580 - 00:45:22:739] **Speaker 1:** We've got TI minus 1, so that's T12.
[00:45:24:479 - 00:45:30:929] **Speaker 1:** Uh, we've got TIJ plus 1, so T23, and TIJ
[00:45:30:929 - 00:45:33:449] **Speaker 1:** minus 1, T21.
[00:45:39:959 - 00:45:42:040] **Speaker 1:** Now, 12.
[00:45:43:350 - 00:45:46:370] **Speaker 1:** Is on the left-hand side is equal to 75 and
[00:45:46:370 - 00:45:49:610] **Speaker 1:** T21 is on the lower boundary equal to 0.
[00:45:51:449 - 00:45:53:800] **Speaker 1:** So we can substitute in those boundary conditions and we've
[00:45:53:800 - 00:45:56:239] **Speaker 1:** got D3, 2.
[00:45:57:120 - 00:45:59:209] **Speaker 1:** Plus T +23.
[00:46:00:040 - 00:46:05:090] **Speaker 1:** -422 equal to -75.
[00:46:09:530 - 00:46:11:010] **Speaker 1:** We can do the same for all the other interior
[00:46:11:010 - 00:46:11:459] **Speaker 1:** nodes.
[00:46:11:780 - 00:46:14:090] **Speaker 1:** So we've got 8 other equations and we've got a
[00:46:14:090 - 00:46:16:469] **Speaker 1:** system of 9 equations for 9 unknowns.
[00:46:16:929 - 00:46:18:830] **Speaker 1:** So we can solve the system.
[00:46:35:000 - 00:46:37:120] **Speaker 1:** So the system of linear equations we can write in
[00:46:37:120 - 00:46:37:770] **Speaker 1:** matrix form.
[00:46:39:209 - 00:46:43:270] **Speaker 1:** I've used double underscore for the matrix of coefficients.
[00:46:44:449 - 00:46:47:969] **Speaker 1:** T arrow hat for the vector of unknowns, the temperature
[00:46:47:969 - 00:46:50:550] **Speaker 1:** field, and then the right-hand side vector B.
[00:46:51:479 - 00:46:51:489] **Speaker 1:** But.
[00:46:55:040 - 00:46:58:719] **Speaker 1:** So, I've just labelled these columns corresponding to each of
[00:46:58:719 - 00:47:01:139] **Speaker 1:** the temperature components from our vector.
[00:47:02:090 - 00:47:04:350] **Speaker 1:** We've got that right-hand side forcing vector.
[00:47:05:570 - 00:47:07:090] **Speaker 1:** This is a pentodiagonal matrix.
[00:47:07:169 - 00:47:09:489] **Speaker 1:** We've got 5 terms on the diagonal.
[00:47:10:840 - 00:47:13:520] **Speaker 1:** And we can solve this in Python, so that's what
[00:47:13:520 - 00:47:13:989] **Speaker 1:** we've done here.
[00:47:19:280 - 00:47:22:020] **Speaker 1:** So again, we sort of just hardcoded it in in
[00:47:22:020 - 00:47:23:780] **Speaker 1:** Python, we've got an array.
[00:47:24:540 - 00:47:27:639] **Speaker 1:** Of coefficients in array for the vector, and we're using
[00:47:27:639 - 00:47:28:310] **Speaker 1:** this linear solve.
[00:47:33:639 - 00:47:35:379] **Speaker 1:** So we've solved for T.
[00:47:35:760 - 00:47:38:600] **Speaker 1:** So we've got 9 elements of our array.
[00:47:40:179 - 00:47:43:120] **Speaker 1:** And these correspond to our temperature field here.
[00:47:46:320 - 00:47:49:040] **Speaker 1:** So we've got T22, 3242.
[00:47:50:729 - 00:47:52:770] **Speaker 1:** So we can write this directly on our.
[00:47:54:340 - 00:47:54:870] **Speaker 1:** Plot.
[00:47:55:590 - 00:47:58:169] **Speaker 1:** So it's a little bit trickier in 2D to to
[00:47:58:350 - 00:48:02:510] **Speaker 1:** convert, although you can probably do some reshaping, uh, so
[00:48:02:510 - 00:48:04:709] **Speaker 1:** we can just write out these on our grid.
[00:48:04:909 - 00:48:06:050] **Speaker 1:** So we've got 42.
[00:48:08:729 - 00:48:13:649] **Speaker 1:** 0.9 33.3.
[00:48:17:590 - 00:48:19:429] **Speaker 1:** 33.9.
[00:48:23:389 - 00:48:24:870] **Speaker 1:** 63.2.
[00:48:28:300 - 00:48:29:979] **Speaker 1:** 56.3.
[00:48:33:469 - 00:48:35:360] **Speaker 1:** 52.4.
[00:48:38:330 - 00:48:40:080] **Speaker 1:** 78.6.
[00:48:42:820 - 00:48:44:280] **Speaker 1:** 76.1.
[00:48:47:129 - 00:48:48:770] **Speaker 1:** And 69.6.
[00:48:51:679 - 00:48:54:199] **Speaker 1:** So we can see that obviously the Laplace equation is
[00:48:54:199 - 00:48:55:540] **Speaker 1:** sort of diffuse based.
[00:48:55:800 - 00:48:58:709] **Speaker 1:** Uh, we've got a boundary condition of 75 on the
[00:48:58:709 - 00:49:01:479] **Speaker 1:** left and it's decreasing as it goes across the domain
[00:49:01:479 - 00:49:03:439] **Speaker 1:** to the cooler boundary condition on the right of 50
[00:49:03:439 - 00:49:05:719] **Speaker 1:** degrees and it's hottest at the top near the boundary
[00:49:05:719 - 00:49:06:360] **Speaker 1:** of 100.
[00:49:07:810 - 00:49:10:899] **Speaker 1:** So, Yeah, sort of makes sense.
[00:49:11:949 - 00:49:16:189] **Speaker 1:** It's always a good check, um, once you've got some
[00:49:16:189 - 00:49:18:939] **Speaker 1:** results to go back and just check that it makes
[00:49:18:939 - 00:49:22:449] **Speaker 1:** sense in terms of physics and your boundary conditions.
[00:49:32:550 - 00:49:33:070] **Speaker 1:** All right.
[00:49:33:429 - 00:49:34:629] **Speaker 1:** Any questions?
[00:49:38:949 - 00:49:39:830] **Speaker 1:** No questions.
[00:49:40:229 - 00:49:41:310] **Speaker 1:** Alright, cool.
[00:49:42:149 - 00:49:43:310] **Speaker 1:** Um, that's a good place to stop.
[00:49:43:429 - 00:49:46:929] **Speaker 1:** So next time, so tomorrow, we'll go through chapter 4.
[00:49:47:510 - 00:49:50:669] **Speaker 1:** So we're going to solve the system of equations, uh,
[00:49:51:070 - 00:49:51:750] **Speaker 1:** numerically.
[00:50:34:469 - 00:50:34:489] **Speaker 0:** 5.
[00:50:43:159 - 00:50:44:860] **Speaker 0:** I had the term start 2 days late this summer.
[00:50:51:449 - 00:50:55:659] **Speaker 0:** I want Yeah Thank you.
[00:50:58:179 - 00:50:58:320] **Speaker 0:** Thank you.
[00:50:58:840 - 00:51:06:000] **Speaker 0:** And then just uh because of the workarounds that we.
[00:51:12:600 - 00:51:54:800] **Speaker 0:** 7 I don't know why hello, hello.
[00:53:36:979 - 00:53:38:320] **Speaker 0:** You heard the most.
[00:53:39:669 - 00:53:41:310] **Speaker 0:** Dysfunctional group of friends.
[00:53:57:540 - 00:53:59:750] **Speaker 0:** I've got in the crossbar and there's no.
[00:54:01:790 - 00:54:11:810] **Speaker 0:** To the front lines of He played the game and.
[00:54:15:219 - 00:54:22:429] **Speaker 0:** One black Comes on us to be that way.
[00:54:25:219 - 00:54:25:229] **Speaker 0:** got.
[00:54:34:419 - 00:54:43:739] **Speaker 0:** I knew And Hello.
[00:54:58:919 - 00:54:58:929] **Speaker 0:** the

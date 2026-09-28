# ENME302-26S2 Lecture 36 native Echo transcript

Date: September 25, 2026 11:00am-11:55am
Transcript type: native Echo automated transcript.

[00:00:00:009 - 00:00:11:199] **Speaker 0:** OK No, it's.
[00:00:32:290 - 00:00:32:299] **Speaker 0:** Time.
[00:00:36:150 - 00:00:43:470] **Speaker 0:** Yeah No He Mr.
[00:00:47:580 - 00:00:50:889] **Speaker 1:** Oh, good morning, we'll make a start, um.
[00:00:52:110 - 00:00:55:669] **Speaker 1:** So I had some questions on the assignment, so I'll
[00:00:55:669 - 00:00:56:970] **Speaker 1:** just go through some of those.
[00:01:00:650 - 00:01:02:229] **Speaker 1:** Is that mic OK at the back?
[00:01:02:729 - 00:01:04:250] **Speaker 1:** I think I can hear myself, so that must be
[00:01:04:250 - 00:01:04:529] **Speaker 1:** fine.
[00:01:05:389 - 00:01:06:889] **Speaker 1:** Um, cool.
[00:01:07:069 - 00:01:08:510] **Speaker 1:** Alright, so I think I saw a few of you
[00:01:08:510 - 00:01:11:269] **Speaker 1:** last night, so that was good, out running the circuit.
[00:01:11:830 - 00:01:15:389] **Speaker 1:** Um, I managed to run most of what I, what
[00:01:15:389 - 00:01:17:290] **Speaker 1:** I was running and walked some of others.
[00:01:17:709 - 00:01:21:190] **Speaker 1:** Um, so assignment two, some of you have started, which
[00:01:21:190 - 00:01:21:769] **Speaker 1:** is neat.
[00:01:22:269 - 00:01:24:110] **Speaker 1:** Uh, I think we had like at least 3 people
[00:01:24:110 - 00:01:25:949] **Speaker 1:** asking questions in the lab, so that was good.
[00:01:26:739 - 00:01:30:139] **Speaker 1:** So the first part is looking at the finite differenceerencing.
[00:01:31:370 - 00:01:33:580] **Speaker 1:** So that was with the Ford and time centre in
[00:01:33:580 - 00:01:33:769] **Speaker 1:** space.
[00:01:33:819 - 00:01:34:919] **Speaker 1:** So that was fully explicit.
[00:01:35:699 - 00:01:39:230] **Speaker 1:** So all the temperature values essentially evaluated the previous time
[00:01:39:230 - 00:01:39:779] **Speaker 1:** level in.
[00:01:40:750 - 00:01:42:529] **Speaker 1:** And you rearranged for TN + 1.
[00:01:43:970 - 00:01:47:300] **Speaker 1:** Um, we've got this mixed boundary condition.
[00:01:47:580 - 00:01:49:459] **Speaker 1:** So we've got a Neumann on the left and then
[00:01:49:459 - 00:01:50:230] **Speaker 1:** a sort of on the right.
[00:01:51:500 - 00:01:53:319] **Speaker 1:** So this, this convection boundary condition.
[00:01:54:790 - 00:01:57:319] **Speaker 1:** You can evaluate this uh temperature gradient using the ghost
[00:01:57:319 - 00:01:59:699] **Speaker 1:** node like we did for the Neumann boundary conditioning class.
[00:02:00:769 - 00:02:02:569] **Speaker 1:** So that's how I would approach it.
[00:02:02:930 - 00:02:05:809] **Speaker 1:** Some of you are asking about using a one-sided difference.
[00:02:05:889 - 00:02:09:009] **Speaker 1:** So if that's easier for you, um, you, you could
[00:02:09:009 - 00:02:09:809] **Speaker 1:** explore that.
[00:02:10:539 - 00:02:12:460] **Speaker 1:** So if it's one-sided difference, it's gonna be 1st order
[00:02:12:460 - 00:02:16:520] **Speaker 1:** accurate in space rather than 2nd order, like central difference.
[00:02:18:100 - 00:02:20:619] **Speaker 1:** But as you do a mesh convergence study, uh, it
[00:02:20:619 - 00:02:23:039] **Speaker 1:** should sort of fall out and get the same, same
[00:02:23:039 - 00:02:25:110] **Speaker 1:** result, so don't be too concerned about that.
[00:02:38:850 - 00:02:41:500] **Speaker 1:** Uh, kappa is a function of temperature.
[00:02:41:940 - 00:02:43:779] **Speaker 1:** As I say, we've got.
[00:02:44:630 - 00:02:48:070] **Speaker 1:** A nonlinear equation, but because it's fully explicit, we're only
[00:02:48:070 - 00:02:50:389] **Speaker 1:** evaluating these temperature values at the previous time level.
[00:02:50:669 - 00:02:53:979] **Speaker 1:** So, um, we don't have a system of simultaneous equations
[00:02:53:979 - 00:02:54:470] **Speaker 1:** to solve.
[00:02:55:070 - 00:02:58:789] **Speaker 1:** When you're evaluating the Uh, pot fencing.
[00:02:59:889 - 00:03:02:699] **Speaker 1:** I suggested to go back to chapter 4.
[00:03:02:970 - 00:03:03:940] **Speaker 1:** So 4.4.
[00:03:07:740 - 00:03:10:419] **Speaker 1:** And this is where we looked at non-uniform grid spacing.
[00:03:13:119 - 00:03:14:380] **Speaker 1:** With that curved boundary.
[00:03:15:000 - 00:03:16:759] **Speaker 1:** So instead of having uniform grid space in data X
[00:03:16:759 - 00:03:21:240] **Speaker 1:** and Y, we looked at a fraction of the X
[00:03:21:240 - 00:03:21:839] **Speaker 1:** and Y.
[00:03:21:880 - 00:03:24:600] **Speaker 1:** So scaled by alpha and beta.
[00:03:26:369 - 00:03:29:369] **Speaker 1:** And what we did here was we took the first
[00:03:29:369 - 00:03:31:229] **Speaker 1:** order derivative at the midpoints.
[00:03:31:850 - 00:03:34:130] **Speaker 1:** So the midpoints labelled A and B in the next
[00:03:34:130 - 00:03:34:649] **Speaker 1:** direction.
[00:03:35:169 - 00:03:37:199] **Speaker 1:** And we evaluated the inner derivative first.
[00:03:38:410 - 00:03:43:860] **Speaker 1:** So DI + 1 DIJ over the data x.
[00:03:44:360 - 00:03:47:550] **Speaker 1:** Now in the assignment we've got this thermal connectivity kappa.
[00:03:47:960 - 00:03:50:080] **Speaker 1:** So this is also located within the inner derivative.
[00:03:50:199 - 00:03:51:960] **Speaker 1:** So you're evaluating that at the midpoint.
[00:03:58:289 - 00:03:59:740] **Speaker 1:** Is that clear, or?
[00:04:01:809 - 00:04:02:550] **Speaker 1:** Yeah, cool.
[00:04:03:440 - 00:04:05:119] **Speaker 1:** Uh sing out if, if you're stuck.
[00:04:05:779 - 00:04:08:899] **Speaker 1:** So that's Kappa, uh, so Kappa is.
[00:04:10:429 - 00:04:12:619] **Speaker 1:** Equation 2, it would make sense just to make a
[00:04:12:619 - 00:04:14:389] **Speaker 1:** lambda function in Python to evaluate.
[00:04:14:750 - 00:04:16:940] **Speaker 1:** You don't want to really put that into your big
[00:04:16:940 - 00:04:20:350] **Speaker 1:** equation using, using a lambda function will make your life
[00:04:20:350 - 00:04:20:850] **Speaker 1:** a lot easier.
[00:04:24:239 - 00:04:28:040] **Speaker 1:** And the ordering, I mean, in the hints and tips,
[00:04:28:489 - 00:04:35:540] **Speaker 1:** I suggested using Um, like JIN because if we consider
[00:04:44:720 - 00:04:49:390] **Speaker 1:** Um, the matrix array in Python and other software packages,
[00:04:49:769 - 00:04:53:200] **Speaker 1:** we have each row corresponds to the first index.
[00:04:55:459 - 00:04:57:820] **Speaker 1:** And then we've got column, and then we've got depth.
[00:04:58:809 - 00:05:02:010] **Speaker 1:** So if you wanted to set up your array to
[00:05:02:010 - 00:05:04:609] **Speaker 1:** sort of match what's happening physically, you'd have your rows
[00:05:04:609 - 00:05:06:230] **Speaker 1:** corresponding to your Y coordinate.
[00:05:06:980 - 00:05:10:179] **Speaker 1:** Your columns with X and depth with Z.
[00:05:11:809 - 00:05:14:950] **Speaker 1:** Um And in this case, it's time.
[00:05:15:109 - 00:05:19:700] **Speaker 1:** So in columns would be in Z, so K and
[00:05:22:410 - 00:05:24:149] **Speaker 1:** It's OK, that's I.
[00:05:24:649 - 00:05:25:970] **Speaker 1:** So row would be your K.
[00:05:27:220 - 00:05:29:140] **Speaker 1:** Index, so it's in Z.
[00:05:29:500 - 00:05:30:440] **Speaker 1:** It's very confusing.
[00:05:30:730 - 00:05:35:140] **Speaker 1:** Um, but KIN, uh, that's sort of reversed to what
[00:05:35:140 - 00:05:37:399] **Speaker 1:** you might just expect when you're writing out.
[00:05:38:109 - 00:05:40:390] **Speaker 1:** T I K N.
[00:05:41:160 - 00:05:43:750] **Speaker 1:** So you're most welcome just to use TIKN.
[00:05:45:010 - 00:05:47:070] **Speaker 1:** Just be careful when you're going to plot that you're
[00:05:47:070 - 00:05:47:700] **Speaker 1:** consistent.
[00:05:48:200 - 00:05:51:720] **Speaker 1:** So don't reverse the order of those indices partway through
[00:05:51:720 - 00:05:52:239] **Speaker 1:** your code.
[00:05:54:720 - 00:05:56:619] **Speaker 1:** But either approach is fully valid.
[00:05:56:880 - 00:05:59:480] **Speaker 1:** Ah, the reason that I introduced that first concept was
[00:05:59:480 - 00:06:02:799] **Speaker 1:** that it just matches what you imagine intuitively when you're
[00:06:02:799 - 00:06:04:500] **Speaker 1:** looking at the variables explorer.
[00:06:04:959 - 00:06:06:420] **Speaker 1:** So you've got rows and columns.
[00:06:14:179 - 00:06:22:940] **Speaker 1:** And I guess the more detailed, I don't know if
[00:06:22:940 - 00:06:25:179] **Speaker 1:** it's difficult, but maybe the more difficult part is sort
[00:06:25:179 - 00:06:26:059] **Speaker 1:** of upfront.
[00:06:26:579 - 00:06:29:989] **Speaker 1:** So, That's sort of planned in the sense that you
[00:06:29:989 - 00:06:31:369] **Speaker 1:** get that out of the way first, but if you're
[00:06:31:369 - 00:06:35:049] **Speaker 1:** really stuck on discretizing, just continue on with the console
[00:06:35:049 - 00:06:36:329] **Speaker 1:** parts and then come back to it.
[00:06:36:369 - 00:06:38:450] **Speaker 1:** Don't get stuck and waste all your time on this
[00:06:38:450 - 00:06:39:450] **Speaker 1:** discretization.
[00:06:39:809 - 00:06:42:209] **Speaker 1:** You can see this is worth 6 marks out of
[00:06:42:209 - 00:06:43:649] **Speaker 1:** about 35 for the report.
[00:06:44:089 - 00:06:47:929] **Speaker 1:** So don't, um, Yeah, don't, don't skip over the later
[00:06:47:929 - 00:06:48:450] **Speaker 1:** sections.
[00:06:52:829 - 00:06:53:410] **Speaker 1:** All right.
[00:06:53:670 - 00:06:55:869] **Speaker 1:** Any questions in particular?
[00:07:03:410 - 00:07:03:510] **Speaker 1:** Silence.
[00:07:05:429 - 00:07:05:970] **Speaker 1:** That's alright.
[00:07:11:839 - 00:07:12:440] **Speaker 1:** All right.
[00:07:13:019 - 00:07:13:519] **Speaker 1:** No questions.
[00:07:13:880 - 00:07:15:730] **Speaker 1:** So we can go back to chapter 12.
[00:07:16:239 - 00:07:17:619] **Speaker 1:** So we'll try to finish that off today.
[00:07:18:160 - 00:07:19:660] **Speaker 1:** We were going through optimisation.
[00:07:22:089 - 00:07:40:679] **Speaker 1:** Yeah This is on page 104 of your course reader.
[00:07:41:230 - 00:07:43:290] **Speaker 1:** So we're talking a bit about convexity of functions.
[00:07:44:290 - 00:07:52:019] **Speaker 1:** And We Discussed if it's a sort of simple parabola,
[00:07:52:100 - 00:07:54:940] **Speaker 1:** this is convex, and we can imagine that finding the
[00:07:54:940 - 00:07:58:619] **Speaker 1:** minima in these particular objective function spaces would be very
[00:07:58:619 - 00:07:59:059] **Speaker 1:** straightforward.
[00:07:59:299 - 00:08:01:559] **Speaker 1:** We just have to go down and reach the minima.
[00:08:01:980 - 00:08:04:529] **Speaker 1:** If it is quite noisy, uh, we might get tripped
[00:08:04:529 - 00:08:05:980] **Speaker 1:** up in one of these local minima.
[00:08:08:100 - 00:08:11:019] **Speaker 1:** So we've gone through and tried to discuss some ways
[00:08:11:019 - 00:08:12:700] **Speaker 1:** of measuring convexity of functions.
[00:08:13:440 - 00:08:16:119] **Speaker 1:** So we looked at the epigraph as one example or
[00:08:16:119 - 00:08:19:160] **Speaker 1:** one method, and there's two more that we'll we'll discuss
[00:08:19:160 - 00:08:19:540] **Speaker 1:** now.
[00:08:19:880 - 00:08:22:059] **Speaker 1:** So the second is Jensen's inequality.
[00:08:23:230 - 00:08:25:190] **Speaker 1:** And this is going to be satisfied if all of
[00:08:25:190 - 00:08:29:420] **Speaker 1:** the pairs, XA's and XB's within the solution set, capital
[00:08:29:420 - 00:08:29:869] **Speaker 1:** X.
[00:08:30:769 - 00:08:35:770] **Speaker 1:** Um, And we're going to vary it this, uh, variable
[00:08:35:770 - 00:08:37:690] **Speaker 1:** parameter theta between 0 and 1.
[00:08:38:250 - 00:08:41:270] **Speaker 1:** So this is much easier to consider when we plot.
[00:08:42:659 - 00:08:43:299] **Speaker 1:** A function.
[00:08:45:909 - 00:08:52:669] **Speaker 1:** So Again, all we're doing is plotting some objective function
[00:08:53:609 - 00:08:56:330] **Speaker 1:** in space with some free parameter X1.
[00:08:57:780 - 00:09:01:280] **Speaker 1:** So our vertical axis corresponds to the objective function.
[00:09:02:150 - 00:09:03:190] **Speaker 1:** Has a function of X1.
[00:09:03:849 - 00:09:06:090] **Speaker 1:** And suppose that it looks like.
[00:09:07:599 - 00:09:08:140] **Speaker 1:** This sort of shape.
[00:09:17:950 - 00:09:19:590] **Speaker 1:** And Jensen's inequality.
[00:09:20:340 - 00:09:23:200] **Speaker 1:** Is checking that evaluating if.
[00:09:24:900 - 00:09:30:609] **Speaker 1:** At These coordinates is less than this linear function.
[00:09:32:270 - 00:09:38:039] **Speaker 1:** So If we have 2 points in space.
[00:09:39:169 - 00:09:43:260] **Speaker 1:** XA And XP.
[00:09:51:770 - 00:09:56:140] **Speaker 1:** The right-hand side of this um The equation is going
[00:09:56:140 - 00:09:59:580] **Speaker 1:** to be a linear interpolation between the two points.
[00:10:00:390 - 00:10:03:340] **Speaker 1:** It's going from F at XA.
[00:10:06:159 - 00:10:10:039] **Speaker 1:** F of XA and it's going up to F of
[00:10:10:039 - 00:10:10:559] **Speaker 1:** XP.
[00:10:19:409 - 00:10:21:260] **Speaker 1:** Theta ranges from 0 to 1.
[00:10:21:469 - 00:10:23:080] **Speaker 1:** So when theta is equal to 0.
[00:10:24:080 - 00:10:28:640] **Speaker 1:** Uh, we have F of XP and then theta just
[00:10:28:640 - 00:10:31:479] **Speaker 1:** increases up to 1, and then we've got F of
[00:10:31:479 - 00:10:32:530] **Speaker 1:** XA.
[00:10:32:760 - 00:10:33:789] **Speaker 1:** So this is a line.
[00:10:36:250 - 00:10:37:640] **Speaker 1:** Between those two points.
[00:10:38:669 - 00:10:40:169] **Speaker 1:** Maybe I could use a different colour.
[00:10:40:510 - 00:10:41:950] **Speaker 1:** It's a bit late now, but.
[00:10:54:630 - 00:10:56:880] **Speaker 1:** Ah, so this line corresponds to this side of the
[00:10:56:880 - 00:10:57:580] **Speaker 1:** equation.
[00:11:06:630 - 00:11:12:650] **Speaker 1:** And we're ensuring that evaluating our objective function at each
[00:11:12:650 - 00:11:16:229] **Speaker 1:** point along this interval is less than or equal to
[00:11:16:229 - 00:11:17:549] **Speaker 1:** this line.
[00:11:18:429 - 00:11:20:479] **Speaker 1:** Segment, so that's.
[00:11:44:200 - 00:11:44:760] **Speaker 1:** It's loud.
[00:11:52:919 - 00:11:55:320] **Speaker 1:** So all we're checking is for every single line that
[00:11:55:320 - 00:12:01:640] **Speaker 1:** we uh allocate throughout this function, the Function is always
[00:12:01:640 - 00:12:03:010] **Speaker 1:** less than that, so that's going to be defined as
[00:12:03:010 - 00:12:03:599] **Speaker 1:** convex.
[00:12:04:419 - 00:12:06:859] **Speaker 1:** And we can also do this in code because it's
[00:12:06:859 - 00:12:08:539] **Speaker 1:** a little bit easier to plot.
[00:12:09:609 - 00:12:10:719] **Speaker 1:** Any cases?
[00:12:31:630 - 00:12:33:570] **Speaker 1:** So here Oh.
[00:12:57:849 - 00:12:59:750] **Speaker 1:** OK, maybe we're not going to do that.
[00:13:17:880 - 00:13:18:559] **Speaker 1:** Hold our breath.
[00:13:18:650 - 00:13:21:400] **Speaker 1:** Um, so we've got some Python code.
[00:13:21:479 - 00:13:23:000] **Speaker 1:** Again, this is on learn if you want to follow
[00:13:23:000 - 00:13:23:659] **Speaker 1:** through yourself.
[00:13:24:000 - 00:13:26:380] **Speaker 1:** And we've got a function that we're going to check
[00:13:26:380 - 00:13:28:479] **Speaker 1:** the convexity of and it's X cubed.
[00:13:30:130 - 00:13:32:869] **Speaker 1:** Or maybe we'll start with the X21 just for.
[00:13:33:919 - 00:13:34:630] **Speaker 1:** Simplicity.
[00:13:35:130 - 00:13:36:309] **Speaker 1:** So we've got a lambda function.
[00:13:37:320 - 00:13:40:409] **Speaker 1:** X being the variable and then we're squaring it, we're
[00:13:40:409 - 00:13:44:090] **Speaker 1:** looking along some interval from -3 to 3 and we're
[00:13:44:090 - 00:13:46:599] **Speaker 1:** going to explore 10 pairs of XAXBs.
[00:13:46:650 - 00:13:48:609] **Speaker 1:** So the idea is that we're swapping these XAs and
[00:13:48:609 - 00:13:50:590] **Speaker 1:** XBs throughout that interval space.
[00:13:51:549 - 00:13:53:750] **Speaker 1:** And we've used a random function to to set it
[00:13:53:750 - 00:13:54:650] **Speaker 1:** across this interval.
[00:13:56:099 - 00:14:01:250] **Speaker 1:** Um, the other points, we've created a theta array and
[00:14:01:250 - 00:14:03:099] **Speaker 1:** the X array, we're plotting.
[00:14:03:830 - 00:14:08:030] **Speaker 1:** And the main line that we want to look at
[00:14:08:030 - 00:14:08:739] **Speaker 1:** is line 31.
[00:14:08:789 - 00:14:11:570] **Speaker 1:** So this is checking whether or not the Jensen's inequality
[00:14:11:570 - 00:14:12:450] **Speaker 1:** is satisfied.
[00:14:12:989 - 00:14:20:049] **Speaker 1:** So That's going to be satisfied if the Um, expression
[00:14:20:049 - 00:14:22:409] **Speaker 1:** on the left is less than or equal to the
[00:14:22:409 - 00:14:23:090] **Speaker 1:** one on the right.
[00:14:29:460 - 00:14:34:140] **Speaker 1:** And I've included labels for the axis.
[00:14:35:320 - 00:14:38:559] **Speaker 1:** Uh, for the legend entries rather, and also for the
[00:14:38:559 - 00:14:39:659] **Speaker 1:** axes up here.
[00:14:41:010 - 00:14:44:330] **Speaker 1:** So if you're creating a plot without any uh figure
[00:14:44:330 - 00:14:46:729] **Speaker 1:** labels or axes, it can be really difficult to tell
[00:14:46:729 - 00:14:47:450] **Speaker 1:** what you're plotting.
[00:14:48:599 - 00:14:51:729] **Speaker 1:** And I've got a full loop across all of the
[00:14:51:729 - 00:14:54:729] **Speaker 1:** pairs that we're analysing, so 10, and then we're going
[00:14:54:729 - 00:14:58:130] **Speaker 1:** to break out if it's uh not convex.
[00:14:59:549 - 00:15:02:169] **Speaker 1:** So if we run that we find that it doesn't
[00:15:02:710 - 00:15:05:739] **Speaker 1:** break up of the for loop and it's a convex
[00:15:05:739 - 00:15:06:190] **Speaker 1:** function.
[00:15:07:390 - 00:15:11:919] **Speaker 1:** So, It's a tiny font.
[00:15:12:690 - 00:15:19:940] **Speaker 1:** With this resolution, um, Uh This is the red line,
[00:15:20:260 - 00:15:21:770] **Speaker 1:** actually it's colour coded to what we did in the
[00:15:21:770 - 00:15:25:090] **Speaker 1:** notes and we've got this green line that is the
[00:15:25:090 - 00:15:25:969] **Speaker 1:** function underneath.
[00:15:28:140 - 00:15:33:599] **Speaker 1:** Right And for the case of a nonconvex function.
[00:15:35:330 - 00:15:40:609] **Speaker 1:** Uh, we can see that It searched a number of
[00:15:40:609 - 00:15:42:690] **Speaker 1:** intervals and this interval is non-convex.
[00:15:42:849 - 00:15:45:169] **Speaker 1:** The function lies above the line segment.
[00:15:46:710 - 00:15:48:750] **Speaker 1:** All right, I think I've done that.
[00:15:49:599 - 00:15:50:479] **Speaker 1:** In enough detail.
[00:15:51:510 - 00:15:54:950] **Speaker 1:** So any questions on this Jensen's inequality?
[00:15:56:679 - 00:15:57:320] **Speaker 1:** No questions.
[00:15:58:539 - 00:15:58:739] **Speaker 1:** Right.
[00:15:59:989 - 00:16:02:750] **Speaker 1:** So the last method we're looking at is checking that
[00:16:02:750 - 00:16:06:710] **Speaker 1:** the function is twice differentiable and that the Hessian is
[00:16:06:710 - 00:16:07:669] **Speaker 1:** positive semi-definite.
[00:16:07:710 - 00:16:12:010] **Speaker 1:** So that's And essentially a multi-dimensional space, the equivalent of
[00:16:12:830 - 00:16:16:320] **Speaker 1:** Uh, taking the second derivative and checking that it's gonna
[00:16:16:320 - 00:16:17:500] **Speaker 1:** be um positive.
[00:16:19:330 - 00:16:20:570] **Speaker 1:** 4011 the case.
[00:16:21:440 - 00:16:23:729] **Speaker 1:** So those are the uh definitions for convexity.
[00:16:24:109 - 00:16:26:309] **Speaker 1:** Now, Some examples.
[00:16:26:690 - 00:16:30:530] **Speaker 1:** So we've already looked at X2 and it's convex because
[00:16:30:530 - 00:16:33:809] **Speaker 1:** if we take the 2nd order derivative, that's equal to
[00:16:33:809 - 00:16:35:590] **Speaker 1:** 2 and that's greater than 0.
[00:16:36:169 - 00:16:38:900] **Speaker 1:** If we look at the convexity of X cubed, Uh,
[00:16:39:200 - 00:16:42:729] **Speaker 1:** it's not always convex or always concave throughout the entire
[00:16:42:729 - 00:16:43:169] **Speaker 1:** interval.
[00:16:43:869 - 00:16:46:280] **Speaker 1:** Is dependent on the sign of X1.
[00:16:47:390 - 00:16:50:080] **Speaker 1:** Uh, so it's going to be positive for X1 greater
[00:16:50:080 - 00:16:53:400] **Speaker 1:** than 0 and then negative for the negative index.
[00:16:55:210 - 00:16:57:409] **Speaker 1:** So we've got a linear combination of variables as well.
[00:16:57:570 - 00:17:00:330] **Speaker 1:** So if we look at a series of lines in
[00:17:00:330 - 00:17:01:450] **Speaker 1:** multi-dimensional space.
[00:17:02:239 - 00:17:04:849] **Speaker 1:** We can collapse this with vector notation with A being
[00:17:04:849 - 00:17:09:050] **Speaker 1:** our coefficients, uh, X being our three parameters, and B
[00:17:09:050 - 00:17:10:109] **Speaker 1:** being some scalar.
[00:17:10:859 - 00:17:12:280] **Speaker 1:** So you can think of a line.
[00:17:14:909 - 00:17:16:558] **Speaker 1:** is going to be convex.
[00:17:21:430 - 00:17:23:750] **Speaker 1:** Because with Jensen's inequality, uh, it's always going to be
[00:17:23:750 - 00:17:24:989] **Speaker 1:** equal to that line segment.
[00:17:33:689 - 00:17:36:790] **Speaker 1:** All right, so now we've done some theory of different
[00:17:37:400 - 00:17:38:069] **Speaker 1:** object functions.
[00:17:38:569 - 00:17:41:650] **Speaker 1:** How can we find the optimum, uh, minimizer?
[00:17:42:719 - 00:17:45:119] **Speaker 1:** So we could do some brute force approaches where we
[00:17:45:119 - 00:17:47:079] **Speaker 1:** just explore all the parameter sets.
[00:17:48:790 - 00:17:51:189] **Speaker 1:** So we could check every single possible combination of all
[00:17:51:189 - 00:17:52:569] **Speaker 1:** the variables and selecting the best.
[00:17:53:339 - 00:17:55:709] **Speaker 1:** Uh, this is gonna be very expensive computationally or if
[00:17:55:709 - 00:17:57:709] **Speaker 1:** you look at experiments experimentally.
[00:17:58:410 - 00:18:01:739] **Speaker 1:** So it's very impractical and very computationally expensive.
[00:18:02:810 - 00:18:04:369] **Speaker 1:** So a couple of ways that we could do that
[00:18:04:369 - 00:18:06:630] **Speaker 1:** is to sample the parameter space.
[00:18:07:050 - 00:18:10:930] **Speaker 1:** So we could use random, um, random number generators, so
[00:18:10:930 - 00:18:14:790] **Speaker 1:** Monte Carlo experiments is where we're essentially looking at.
[00:18:15:410 - 00:18:19:579] **Speaker 1:** How 3 parameter space.
[00:18:19:680 - 00:18:21:219] **Speaker 1:** In this case it's going to be in 2D.
[00:18:22:020 - 00:18:24:020] **Speaker 1:** And we've got two parameters X1 and X2.
[00:18:26:900 - 00:18:28:500] **Speaker 1:** Monte Carlo in the sense that we're just going to
[00:18:28:500 - 00:18:29:760] **Speaker 1:** sample this space.
[00:18:30:560 - 00:18:39:219] **Speaker 1:** Randomly Uh, if it's, yeah, a reasonable distribution throughout the
[00:18:39:219 - 00:18:41:189] **Speaker 1:** space, then it's going to be able to capture some
[00:18:41:189 - 00:18:43:170] **Speaker 1:** of the uh minimum values.
[00:18:45:880 - 00:18:49:060] **Speaker 1:** And our objective function that corresponds to the minimum value
[00:18:49:060 - 00:18:51:800] **Speaker 1:** or optimum is going to be our minimizer.
[00:18:54:180 - 00:18:55:260] **Speaker 1:** And we've triggered something.
[00:18:58:180 - 00:18:58:739] **Speaker 1:** I'm not sure.
[00:18:59:479 - 00:19:03:640] **Speaker 1:** Uh, so the second example of these brute force approaches.
[00:19:04:239 - 00:19:06:969] **Speaker 1:** Is the grid search where this is a more methodical
[00:19:06:969 - 00:19:10:119] **Speaker 1:** approach, so instead of randomly sampling our parameter space, we're
[00:19:10:119 - 00:19:11:219] **Speaker 1:** just going to do a grid search.
[00:19:12:699 - 00:19:14:660] **Speaker 1:** And our free permanent space X1 and X2.
[00:19:23:300 - 00:19:26:180] **Speaker 1:** So both of these methods are sort of considered global
[00:19:26:180 - 00:19:29:380] **Speaker 1:** methods in the sense that it's exploring the full solution
[00:19:29:380 - 00:19:30:900] **Speaker 1:** space they were analysing.
[00:19:31:989 - 00:19:35:790] **Speaker 1:** So it's not discriminating against local minima.
[00:19:36:939 - 00:19:44:680] **Speaker 1:** If we recall our Different objective functions, it wouldn't be
[00:19:44:680 - 00:19:48:520] **Speaker 1:** trapped in one particular local minima, it's exploring the full
[00:19:48:520 - 00:19:49:040] **Speaker 1:** solution set.
[00:19:53:640 - 00:19:56:140] **Speaker 1:** So those are two global or brute force approaches.
[00:19:58:250 - 00:20:00:329] **Speaker 1:** Now we'll discuss steepest descent.
[00:20:00:550 - 00:20:01:729] **Speaker 1:** So this is a little bit more intuitive.
[00:20:02:069 - 00:20:05:729] **Speaker 1:** So we've got First of all, the motivation for this
[00:20:05:729 - 00:20:07:939] **Speaker 1:** is that we're going to improve on our solution by
[00:20:07:939 - 00:20:08:849] **Speaker 1:** walking downhill.
[00:20:09:550 - 00:20:12:430] **Speaker 1:** So if we're out hiking in some mountain and we
[00:20:12:430 - 00:20:14:670] **Speaker 1:** want to get to the, the bottom, back to the
[00:20:14:670 - 00:20:18:510] **Speaker 1:** car, uh, we walk down, down the hill, um, so
[00:20:18:510 - 00:20:22:630] **Speaker 1:** we're not, well, Not always, but mostly down the hill.
[00:20:23:160 - 00:20:24:729] **Speaker 1:** Uh, so in this case, we're always going to be
[00:20:24:729 - 00:20:26:770] **Speaker 1:** going downhill in the steepest descent.
[00:20:26:810 - 00:20:30:119] **Speaker 1:** So we can evaluate the gradient at each point in
[00:20:30:119 - 00:20:33:469] **Speaker 1:** space by evaluating minus 2F.
[00:20:36:319 - 00:20:38:930] **Speaker 1:** And we're going to do this repetitively or iteratively.
[00:20:39:239 - 00:20:40:880] **Speaker 1:** So this is an iterative method.
[00:20:41:709 - 00:20:44:219] **Speaker 1:** And we're going to start from an initial point X0.
[00:20:45:310 - 00:20:46:849] **Speaker 1:** And we're gonna step to the next point.
[00:20:47:910 - 00:20:59:260] **Speaker 1:** By taking A step size, or some step factor H
[00:20:59:260 - 00:21:01:180] **Speaker 1:** multiplied by grad F.
[00:21:11:800 - 00:21:14:650] **Speaker 1:** So this process is going to be repeated until our
[00:21:14:650 - 00:21:16:339] **Speaker 1:** gradient approaches 0.
[00:21:16:930 - 00:21:17:739] **Speaker 1:** So grade F.
[00:21:18:660 - 00:21:23:239] **Speaker 1:** And we need to define or quantify that smallness.
[00:21:23:780 - 00:21:25:339] **Speaker 1:** So we're going to label it epsilon.
[00:21:25:579 - 00:21:28:439] **Speaker 1:** So when our gradient or the magnitude of our gradient
[00:21:28:699 - 00:21:31:760] **Speaker 1:** is less than this tolerance, epsilon, uh, we're set to
[00:21:32:060 - 00:21:33:099] **Speaker 1:** define a local minima.
[00:21:35:719 - 00:21:38:439] **Speaker 1:** So in this case, convergence is not guaranteed.
[00:21:39:219 - 00:21:41:260] **Speaker 1:** We're going to explore what happens when we have really
[00:21:41:260 - 00:21:42:380] **Speaker 1:** large step sizes.
[00:21:43:099 - 00:21:46:449] **Speaker 1:** And what is the definition of large H?
[00:21:47:510 - 00:21:49:219] **Speaker 1:** So it's a little bit tasty.
[00:21:51:569 - 00:21:56:349] **Speaker 1:** So the first case We'll look at is one that
[00:21:56:349 - 00:21:56:829] **Speaker 1:** works.
[00:21:58:949 - 00:22:05:630] **Speaker 1:** So If we have a nice convex function.
[00:22:06:959 - 00:22:08:839] **Speaker 1:** And we start at some position.
[00:22:10:439 - 00:22:10:449] **Speaker 1:** Yes.
[00:22:12:250 - 00:22:20:359] **Speaker 1:** Why not We evaluate grade F.
[00:22:21:400 - 00:22:27:400] **Speaker 1:** At this point, And we're going in the negative direction,
[00:22:27:560 - 00:22:31:959] **Speaker 1:** so downhill and some step back to, uh.
[00:22:33:369 - 00:22:34:229] **Speaker 1:** Size H.
[00:22:35:199 - 00:22:36:469] **Speaker 1:** So this is the next step.
[00:22:37:349 - 00:22:38:930] **Speaker 1:** X 11.
[00:22:41:479 - 00:22:43:020] **Speaker 1:** This is repeated many times.
[00:23:05:030 - 00:23:11:339] **Speaker 1:** And We can see that the step size, so delta
[00:23:11:339 - 00:23:14:900] **Speaker 1:** X is going to scale with that gradient grad F.
[00:23:15:099 - 00:23:17:540] **Speaker 1:** So for large gradients it's going to step further.
[00:23:23:420 - 00:23:27:530] **Speaker 1:** Once our gradient, so grade F is small, so when
[00:23:27:530 - 00:23:29:579] **Speaker 1:** we're at this minimum, this is where we can say
[00:23:29:579 - 00:23:32:819] **Speaker 1:** that we've converged to a solution that's perhaps less than
[00:23:32:819 - 00:23:36:579] **Speaker 1:** some tolerance and we've reached the local or global minimum.
[00:23:39:560 - 00:23:41:729] **Speaker 1:** So that's an example of really well behaved function.
[00:23:42:579 - 00:23:46:829] **Speaker 1:** Uh, it's nice and convex, and we, we reach the,
[00:23:47:079 - 00:23:49:069] **Speaker 1:** the minimum relatively easily.
[00:23:50:680 - 00:23:53:199] **Speaker 1:** Now, what happens if we have a large step size
[00:23:53:199 - 00:23:53:660] **Speaker 1:** H?
[00:23:55:449 - 00:23:56:849] **Speaker 1:** What would you imagine happens?
[00:24:08:680 - 00:24:10:140] **Speaker 1:** We can look at the same function.
[00:24:11:189 - 00:24:12:369] **Speaker 1:** That I can draw really well.
[00:24:15:260 - 00:24:18:569] **Speaker 1:** So it's convex parabola, maybe we start.
[00:24:20:930 - 00:24:24:560] **Speaker 1:** Here X 10.
[00:24:26:599 - 00:24:29:530] **Speaker 1:** So we've got some tangent line er.
[00:24:30:219 - 00:24:33:609] **Speaker 1:** You to rule out Something like that.
[00:24:39:079 - 00:24:41:229] **Speaker 1:** What happens if we take a really large step in
[00:24:41:229 - 00:24:43:189] **Speaker 1:** this direction, going downhill?
[00:24:46:160 - 00:24:47:650] **Speaker 1:** No It's not very accurate.
[00:24:47:770 - 00:24:49:060] **Speaker 1:** I mean, we're going to overshoot the minima.
[00:24:50:089 - 00:24:51:810] **Speaker 1:** So if we take a really large step, we're going
[00:24:51:810 - 00:24:52:849] **Speaker 1:** in the same direction.
[00:24:53:250 - 00:24:54:510] **Speaker 1:** But if we jump over to here.
[00:24:55:689 - 00:24:57:229] **Speaker 1:** And then evaluate our function.
[00:24:59:479 - 00:25:01:699] **Speaker 1:** Maybe I'll just exaggerate and go further, so we go
[00:25:01:699 - 00:25:02:319] **Speaker 1:** over to here.
[00:25:07:890 - 00:25:09:319] **Speaker 1:** It's a very tidy graph.
[00:25:10:239 - 00:25:10:760] **Speaker 1:** This is it.
[00:25:11:170 - 00:25:11:869] **Speaker 1:** Step one.
[00:25:16:560 - 00:25:18:869] **Speaker 1:** And we repeat the process, so we've actually got a
[00:25:18:869 - 00:25:19:430] **Speaker 1:** worse value.
[00:25:19:520 - 00:25:22:239] **Speaker 1:** So our objective function F is higher than what we
[00:25:22:239 - 00:25:24:119] **Speaker 1:** started at, which is not convenient.
[00:25:24:900 - 00:25:29:280] **Speaker 1:** And we apply the same Uh, step or same algorithm.
[00:25:33:489 - 00:25:34:780] **Speaker 1:** And it would go off the page, but if we
[00:25:34:780 - 00:25:37:219] **Speaker 1:** did a large step, we would end up somewhere up
[00:25:37:219 - 00:25:37:500] **Speaker 1:** here.
[00:25:38:920 - 00:25:40:319] **Speaker 1:** This is X1.
[00:25:41:250 - 00:25:41:880] **Speaker 1:** Step 2.
[00:25:45:579 - 00:25:47:030] **Speaker 1:** So you can see here that it's diverging.
[00:25:47:109 - 00:25:50:390] **Speaker 1:** So instead of converging to the local minima, we're overshooting
[00:25:50:589 - 00:25:52:510] **Speaker 1:** the minima and diverging.
[00:25:53:420 - 00:25:55:430] **Speaker 1:** So there's a risk here that if you have a
[00:25:55:430 - 00:25:59:160] **Speaker 1:** large H, then we're not going to get a converged
[00:25:59:160 - 00:25:59:469] **Speaker 1:** solution.
[00:26:00:439 - 00:26:03:739] **Speaker 1:** The question remains that what is a large H?
[00:26:03:989 - 00:26:05:959] **Speaker 1:** Because we don't actually know what this objective function space
[00:26:05:959 - 00:26:07:959] **Speaker 1:** is, because if we did, we would just go straight
[00:26:07:959 - 00:26:08:500] **Speaker 1:** to the minimum.
[00:26:09:160 - 00:26:11:319] **Speaker 1:** So this is an unknown function and all we're doing
[00:26:11:319 - 00:26:15:079] **Speaker 1:** is evaluating the objective function at these discrete points.
[00:26:18:689 - 00:26:21:589] **Speaker 1:** And we've got a short demonstration with this as well.
[00:26:22:880 - 00:26:25:619] **Speaker 1:** The um projector plays nice.
[00:26:52:050 - 00:26:52:329] **Speaker 1:** No.
[00:26:54:859 - 00:26:57:069] **Speaker 1:** I could just about put the laptop underneath the document
[00:26:57:069 - 00:26:58:489] **Speaker 1:** camera, but that might be a little bit.
[00:27:00:430 - 00:27:01:270] **Speaker 1:** A little bit awkward.
[00:27:02:380 - 00:27:03:199] **Speaker 1:** Oh, here we go.
[00:27:03:719 - 00:27:07:319] **Speaker 1:** So We have our code.
[00:27:07:640 - 00:27:12:839] **Speaker 1:** We're going to analyse the parabola or quadratic X2, 12
[00:27:12:839 - 00:27:13:280] **Speaker 1:** X2.
[00:27:14:939 - 00:27:17:099] **Speaker 1:** I've taken half because when we take the derivative it's
[00:27:17:099 - 00:27:17:859] **Speaker 1:** just X.
[00:27:18:500 - 00:27:21:339] **Speaker 1:** We've got an initial step factor of 3.1, uh, number
[00:27:21:339 - 00:27:24:040] **Speaker 1:** of iterations to specify, we have to start at some
[00:27:24:040 - 00:27:24:939] **Speaker 1:** position X.
[00:27:26:300 - 00:27:31:829] **Speaker 1:** And we're gonna plot X solution set space.
[00:27:33:199 - 00:27:38:219] **Speaker 1:** And We've already introduced this line search, so I want
[00:27:38:219 - 00:27:39:449] **Speaker 1:** to disable this.
[00:27:50:579 - 00:27:52:650] **Speaker 1:** It's always dangerous when you don't look at the code
[00:27:52:650 - 00:27:53:829] **Speaker 1:** since last year, but.
[00:27:56:069 - 00:27:57:140] **Speaker 1:** This might work.
[00:27:57:680 - 00:28:00:140] **Speaker 1:** So our steepest descent is what we've just discussed in
[00:28:00:140 - 00:28:01:140] **Speaker 1:** equation 5.
[00:28:03:050 - 00:28:05:449] **Speaker 1:** And then we're gonna be plotting this, so we'll just
[00:28:05:449 - 00:28:07:130] **Speaker 1:** give that a go and see what happens.
[00:28:09:689 - 00:28:11:599] **Speaker 1:** So this is a case of a large H step
[00:28:11:599 - 00:28:14:310] **Speaker 1:** size, and we've diverged, so we're getting worse and worse.
[00:28:15:479 - 00:28:17:920] **Speaker 1:** So if we have a small step factor.
[00:28:25:869 - 00:28:28:510] **Speaker 1:** We can see that it's slowly crawling towards that local
[00:28:28:510 - 00:28:32:349] **Speaker 1:** minima, and if we gave it more iterations, we would
[00:28:32:349 - 00:28:33:089] **Speaker 1:** expect it to reach.
[00:28:41:650 - 00:28:42:050] **Speaker 1:** Cool.
[00:28:42:290 - 00:28:43:650] **Speaker 1:** So that's behaving as expected.
[00:28:45:199 - 00:28:48:189] **Speaker 1:** So as you saw initially, when we had a really
[00:28:48:189 - 00:28:50:020] **Speaker 1:** large step size, it was diverging.
[00:28:50:430 - 00:28:52:760] **Speaker 1:** Uh, so one of the ways that we can address
[00:28:52:760 - 00:28:56:160] **Speaker 1:** this problem is to apply a line search.
[00:28:59:400 - 00:29:02:459] **Speaker 1:** So for ensuring our convergence of our steep descent method,
[00:29:02:709 - 00:29:06:280] **Speaker 1:** uh, we're gonna use an additional step uh that involves
[00:29:06:280 - 00:29:09:709] **Speaker 1:** making sure that the next step or the next iteration
[00:29:09:709 - 00:29:11:280] **Speaker 1:** is better than where we are at the moment.
[00:29:19:089 - 00:29:23:140] **Speaker 1:** Consider that we have some uh decent step direction that
[00:29:23:140 - 00:29:26:140] **Speaker 1:** we've labelled minus squad F equal to D, then we're
[00:29:26:140 - 00:29:28:180] **Speaker 1:** gonna find out some step factor H.
[00:29:30:650 - 00:29:34:469] **Speaker 1:** That's going to correspond to the argument that minimises.
[00:29:35:650 - 00:29:40:729] **Speaker 1:** Our objective function at that next step, X plus HD.
[00:29:42:359 - 00:29:42:859] **Speaker 1:** For each.
[00:29:44:130 - 00:29:46:530] **Speaker 1:** Greater than or equal to 0, so the step size
[00:29:46:530 - 00:29:49:130] **Speaker 1:** has to be positive or 0.
[00:29:51:050 - 00:29:53:369] **Speaker 1:** So this would give us the optimum solution in the
[00:29:53:369 - 00:29:54:290] **Speaker 1:** direction of steepest descent.
[00:29:56:380 - 00:29:59:219] **Speaker 1:** But we've run into the problem that we're now evaluating
[00:29:59:219 - 00:30:02:300] **Speaker 1:** all possible scenarios, so evaluating.
[00:30:03:660 - 00:30:05:910] **Speaker 1:** If Vick along all of the points on this line.
[00:30:07:439 - 00:30:10:569] **Speaker 1:** So instead, we're going to use heuristics to sort of
[00:30:10:880 - 00:30:14:859] **Speaker 1:** guess or Iteratively figure out what appropriate h value to
[00:30:14:859 - 00:30:15:239] **Speaker 1:** select.
[00:30:17:719 - 00:30:19:810] **Speaker 1:** Uh, one of the simple methods that we're gonna look
[00:30:19:810 - 00:30:21:430] **Speaker 1:** at is the backtracking line search.
[00:30:22:439 - 00:30:25:040] **Speaker 1:** So I guess anyone that's done like compsci or those
[00:30:25:040 - 00:30:27:560] **Speaker 1:** sort of computer courses, there's heaps of different algorithms that
[00:30:27:560 - 00:30:28:459] **Speaker 1:** you can use for these.
[00:30:29:500 - 00:30:32:939] **Speaker 1:** Search methods, but we're just gonna use this backtracking line
[00:30:32:939 - 00:30:33:229] **Speaker 1:** search.
[00:30:34:479 - 00:30:36:589] **Speaker 1:** We're going to start with a really large initial step
[00:30:36:589 - 00:30:37:000] **Speaker 1:** factor.
[00:30:37:670 - 00:30:38:849] **Speaker 1:** And then reduce H.
[00:30:40:290 - 00:30:43:900] **Speaker 1:** For example, half it at each step until the minimum
[00:30:43:900 - 00:30:46:270] **Speaker 1:** descent steepness criteria is reached.
[00:30:47:599 - 00:30:50:579] **Speaker 1:** So in other words, We're going to try a big
[00:30:50:579 - 00:30:50:859] **Speaker 1:** step.
[00:30:51:170 - 00:30:53:300] **Speaker 1:** If it gets a worse solution, we reduce the step
[00:30:53:300 - 00:30:53:760] **Speaker 1:** size.
[00:30:56:060 - 00:30:57:780] **Speaker 1:** So F of X.
[00:30:58:579 - 00:31:04:760] **Speaker 1:** Plus HD So we're evaluating the objective function at that
[00:31:04:760 - 00:31:06:729] **Speaker 1:** next step, X + HD.
[00:31:07:880 - 00:31:09:719] **Speaker 1:** This is going to be less than or equal to.
[00:31:10:670 - 00:31:11:229] **Speaker 1:** If.
[00:31:12:489 - 00:31:19:300] **Speaker 1:** Of X If we just leave it as this, that
[00:31:20:209 - 00:31:22:689] **Speaker 1:** Could make sense, but then we might get into the
[00:31:22:689 - 00:31:25:079] **Speaker 1:** scenario where we're just bouncing back and forth at the
[00:31:25:079 - 00:31:25:609] **Speaker 1:** same level.
[00:31:26:209 - 00:31:29:339] **Speaker 1:** So if we think back to our, Graph.
[00:31:30:369 - 00:31:33:119] **Speaker 1:** This would enable going back and forth at the same
[00:31:33:119 - 00:31:33:660] **Speaker 1:** point.
[00:31:34:040 - 00:31:36:439] **Speaker 1:** So we want to improve slightly better.
[00:31:36:719 - 00:31:39:359] **Speaker 1:** So we want to add a condition.
[00:31:40:380 - 00:31:41:459] **Speaker 1:** Of Ada.
[00:31:43:089 - 00:31:46:010] **Speaker 1:** H Grad F.
[00:31:56:189 - 00:31:59:069] **Speaker 1:** So beta is uh essentially.
[00:32:02:709 - 00:32:07:079] **Speaker 1:** Uh, setting how aggressive the, the step size is changing.
[00:32:08:150 - 00:32:10:310] **Speaker 1:** So typically we're just gonna use 10 to 4, so
[00:32:10:310 - 00:32:12:780] **Speaker 1:** it's only gonna be required to be a little bit
[00:32:12:780 - 00:32:14:079] **Speaker 1:** better than the previous step.
[00:32:15:920 - 00:32:19:650] **Speaker 1:** So small beta means any dissent is valid, large beta
[00:32:19:650 - 00:32:20:869] **Speaker 1:** means that it needs to be very steep.
[00:32:22:180 - 00:32:24:699] **Speaker 1:** So that corresponds to very small step sizes, which is
[00:32:24:699 - 00:32:27:319] **Speaker 1:** not what we want because that would require many iterations
[00:32:27:530 - 00:32:29:219] **Speaker 1:** of our method to approach the minimum.
[00:32:30:810 - 00:32:33:130] **Speaker 1:** So I'll just go through that with our code.
[00:33:23:890 - 00:33:25:709] **Speaker 1:** Even the projector knows it's Friday.
[00:33:29:430 - 00:33:29:869] **Speaker 1:** I don't know.
[00:33:31:150 - 00:33:32:180] **Speaker 1:** Try and refresh.
[00:33:34:949 - 00:33:35:390] **Speaker 1:** Here we go.
[00:33:37:699 - 00:33:38:180] **Speaker 1:** OK.
[00:33:38:880 - 00:33:40:910] **Speaker 1:** So we'll uncomment the the line search code.
[00:33:44:069 - 00:33:47:469] **Speaker 1:** Oops And there's probably a quicker way to do this,
[00:33:47:589 - 00:33:48:229] **Speaker 1:** but this.
[00:33:51:579 - 00:33:52:300] **Speaker 1:** That's what we'll do.
[00:33:52:459 - 00:33:55:650] **Speaker 1:** So that's within a small initial factor, but if we
[00:33:55:650 - 00:33:57:719] **Speaker 1:** jump it up to that 3.1.
[00:34:01:189 - 00:34:05:119] **Speaker 1:** We can see that it's always improving the objective function
[00:34:05:119 - 00:34:05:630] **Speaker 1:** value.
[00:34:05:800 - 00:34:09:360] **Speaker 1:** So it's reducing if and then it's finding the local
[00:34:09:360 - 00:34:09:780] **Speaker 1:** minimum.
[00:34:12:250 - 00:34:16:128] **Speaker 1:** And this line 29 is our equation 7.
[00:34:24:310 - 00:34:24:658] **Speaker 1:** Cool.
[00:34:26:290 - 00:34:28:229] **Speaker 1:** Any questions on this?
[00:34:29:580 - 00:34:40:300] **Speaker 1:** Methodology Cool.
[00:34:40:620 - 00:34:42:300] **Speaker 1:** Alright, so.
[00:34:43:559 - 00:34:44:958] **Speaker 1:** Now I want to spend a bit of time talking
[00:34:44:958 - 00:34:45:839] **Speaker 1:** about constraints.
[00:34:46:658 - 00:34:49:770] **Speaker 1:** Because at the start of yesterday we talked a bit
[00:34:49:770 - 00:34:53:090] **Speaker 1:** about some constraints for our optimisation problems, so maybe it's
[00:34:53:090 - 00:34:56:489] **Speaker 1:** that it has to exceed some performance requirements or we've
[00:34:56:489 - 00:34:57:860] **Speaker 1:** got some budget constraints.
[00:34:58:129 - 00:35:01:530] **Speaker 1:** So how can we constrain our objective function space uh
[00:35:02:250 - 00:35:04:270] **Speaker 1:** subject to some constraint.
[00:35:04:729 - 00:35:06:850] **Speaker 1:** So our first two types of these problems we discussed
[00:35:06:850 - 00:35:10:330] **Speaker 1:** earlier had constraints, as I just said, we're going to
[00:35:10:330 - 00:35:15:899] **Speaker 1:** study most of the optimisation problems without, Particularly constrained, um,
[00:35:16:159 - 00:35:16:750] **Speaker 1:** approaches.
[00:35:17:139 - 00:35:20:290] **Speaker 1:** So we're going to insert an artificial constraint into our
[00:35:20:290 - 00:35:21:030] **Speaker 1:** equations.
[00:35:22:300 - 00:35:24:419] **Speaker 1:** By applying a soft constraint.
[00:35:25:209 - 00:35:27:300] **Speaker 1:** Which is using a penalty term.
[00:35:27:760 - 00:35:32:360] **Speaker 1:** So instead of having our objective function, Uh, as normal,
[00:35:32:719 - 00:35:36:179] **Speaker 1:** we're going to find the minimizer X.
[00:35:37:379 - 00:35:40:590] **Speaker 1:** To be the argument that minimises.
[00:35:42:949 - 00:35:44:489] **Speaker 1:** Our objective function F.
[00:35:46:629 - 00:35:50:860] **Speaker 1:** Plus Some penalty fee.
[00:35:54:090 - 00:35:57:449] **Speaker 1:** And this is minimising X within.
[00:35:58:610 - 00:36:00:330] **Speaker 1:** Our solution space X.
[00:36:01:270 - 00:36:01:870] **Speaker 1:** Capital X.
[00:36:03:969 - 00:36:08:429] **Speaker 1:** So here he is going to be our penalty function
[00:36:08:810 - 00:36:09:770] **Speaker 1:** or penalty term.
[00:36:11:810 - 00:36:15:169] **Speaker 1:** And Alpha is just going to make that penalty term
[00:36:15:169 - 00:36:18:050] **Speaker 1:** more or less important to our, to our solution.
[00:36:23:770 - 00:36:30:689] **Speaker 1:** Now the example I want to give is Another parabola.
[00:36:31:719 - 00:36:33:060] **Speaker 1:** Cos it's nice and convex.
[00:36:34:780 - 00:36:43:110] **Speaker 1:** And For whatever argument's sake.
[00:36:43:580 - 00:36:46:139] **Speaker 1:** Well, first of all, the minima is located here.
[00:36:46:340 - 00:36:47:060] **Speaker 1:** We can see that.
[00:36:49:149 - 00:36:55:639] **Speaker 1:** We've got X1 And the blue line is F of
[00:36:55:639 - 00:36:56:199] **Speaker 1:** X1.
[00:36:56:840 - 00:36:57:560] **Speaker 1:** So that's pretty standard.
[00:36:57:679 - 00:37:00:120] **Speaker 1:** That's what we've done so far, and we expect that
[00:37:00:120 - 00:37:01:840] **Speaker 1:** the minimum is located at this point.
[00:37:18:300 - 00:37:19:919] **Speaker 1:** I don't think we need the laptop anymore.
[00:37:23:409 - 00:37:25:889] **Speaker 1:** All right, so we've got FFX1.
[00:37:28:149 - 00:37:32:550] **Speaker 1:** And for whatever reason, we want to constrain our solution
[00:37:32:550 - 00:37:35:459] **Speaker 1:** space to be less than X1 equal to 5.
[00:37:46:040 - 00:37:48:719] **Speaker 1:** So visually, we can already identify that the minimum value
[00:37:48:719 - 00:37:51:300] **Speaker 1:** would be located at X1 equal to 5.
[00:37:51:969 - 00:37:55:909] **Speaker 1:** But again, we don't know what these objective function spaces
[00:37:55:909 - 00:37:57:800] **Speaker 1:** look like prior to solving and we're not going to
[00:37:57:800 - 00:38:01:000] **Speaker 1:** evaluate if everywhere because that defeats the purpose of these
[00:38:01:000 - 00:38:01:540] **Speaker 1:** methods.
[00:38:03:429 - 00:38:06:530] **Speaker 1:** And we're going to introduce a penalty function P of
[00:38:06:530 - 00:38:07:310] **Speaker 1:** X.
[00:38:10:810 - 00:38:15:129] **Speaker 1:** That essentially switches on at X1 equal to 5.
[00:38:15:489 - 00:38:18:169] **Speaker 1:** So we're taking the maximum value of 0 or X
[00:38:18:169 - 00:38:19:149] **Speaker 1:** minus 5.
[00:38:20:310 - 00:38:22:250] **Speaker 1:** So this is going to be a linear.
[00:38:23:510 - 00:38:27:770] **Speaker 1:** Function That switches on at X1 equal to 5.
[00:38:29:969 - 00:38:32:040] **Speaker 1:** So if you think that through, so if we have
[00:38:32:040 - 00:38:36:989] **Speaker 1:** a value that's less than 5, for example, 44 minus
[00:38:36:989 - 00:38:40:239] **Speaker 1:** 5 is -1, the maximum between 0 and -1 is
[00:38:40:239 - 00:38:42:560] **Speaker 1:** 0, and that's going to hold true for all those
[00:38:42:560 - 00:38:43:979] **Speaker 1:** x values less than 5.
[00:38:44:639 - 00:38:47:030] **Speaker 1:** When we have a value greater than 5, for example,
[00:38:47:040 - 00:38:49:820] **Speaker 1:** 6, we've got 6 minus 5 is equal to 1,
[00:38:50:070 - 00:38:51:479] **Speaker 1:** and that's where we've got a positive value and it
[00:38:51:479 - 00:38:52:639] **Speaker 1:** just increases linearly.
[00:38:53:489 - 00:38:56:129] **Speaker 1:** So it's just a neat little uh function that we
[00:38:56:129 - 00:38:58:350] **Speaker 1:** can use to to switch on this penalty.
[00:39:00:379 - 00:39:02:419] **Speaker 1:** Now the combination of these two.
[00:39:02:939 - 00:39:04:340] **Speaker 1:** So we've got alpha times P.
[00:39:04:830 - 00:39:06:149] **Speaker 1:** I guess we can label this.
[00:39:08:600 - 00:39:08:889] **Speaker 1:** It be.
[00:39:09:850 - 00:39:10:850] **Speaker 1:** Of X1.
[00:39:21:179 - 00:39:24:750] **Speaker 1:** The combination of these two is our actual objective function
[00:39:24:750 - 00:39:27:669] **Speaker 1:** that we're evaluating, so that's our F plus alpha P.
[00:39:29:300 - 00:39:32:379] **Speaker 1:** So it remains the same up until X1 equal to
[00:39:32:379 - 00:39:35:379] **Speaker 1:** 5, and then it's going to be a combination of
[00:39:35:379 - 00:39:35:899] **Speaker 1:** these two.
[00:39:37:429 - 00:39:47:760] **Speaker 1:** Um, It'll look sort of like that.
[00:39:51:649 - 00:39:56:270] **Speaker 1:** So this is If 5 X1.
[00:39:57:340 - 00:39:59:939] **Speaker 1:** Plus he of X1.
[00:40:02:260 - 00:40:04:850] **Speaker 1:** So just say alpha is one in this case, but
[00:40:05:060 - 00:40:09:479] **Speaker 1:** you can, you can see that if you had And
[00:40:09:479 - 00:40:12:669] **Speaker 1:** a more aggressive penalty and wanted to have alpha higher
[00:40:12:669 - 00:40:15:000] **Speaker 1:** values, then it would be steeper.
[00:40:18:590 - 00:40:21:229] **Speaker 1:** So now when we apply our steepest descent, you can
[00:40:21:229 - 00:40:24:409] **Speaker 1:** imagine that it's bouncing back and forth between these locations
[00:40:24:709 - 00:40:26:709] **Speaker 1:** rather than minimising at this point.
[00:40:27:659 - 00:40:31:780] **Speaker 1:** So this is going to be our Minimum.
[00:40:38:810 - 00:40:54:659] **Speaker 1:** With The penalty Yeah So as I say, constrained optimisation
[00:40:54:659 - 00:40:57:989] **Speaker 1:** methods are a whole another, Set of methods and techniques,
[00:40:58:179 - 00:41:02:979] **Speaker 1:** ah, here we're just modifying our unconstrained, ah function space
[00:41:02:979 - 00:41:05:500] **Speaker 1:** by applying these penalties, so it's a bit of a
[00:41:05:500 - 00:41:08:040] **Speaker 1:** hack but it works OK.
[00:41:09:169 - 00:41:11:409] **Speaker 1:** You can imagine that this doesn't um.
[00:41:12:429 - 00:41:14:199] **Speaker 1:** Strictly enforced that it's not.
[00:41:15:139 - 00:41:20:510] **Speaker 1:** Greater than 5, depending on your tolerance, it might settle
[00:41:20:510 - 00:41:22:129] **Speaker 1:** in this constrained region.
[00:41:25:629 - 00:41:26:149] **Speaker 1:** Cool.
[00:41:26:550 - 00:41:27:439] **Speaker 1:** Hopefully you're following.
[00:41:27:669 - 00:41:31:550] **Speaker 1:** Um, so now we've got the, the question of should
[00:41:31:550 - 00:41:33:389] **Speaker 1:** we apply a more aggressive penalty?
[00:41:34:629 - 00:41:38:500] **Speaker 1:** So instead of doing a linear function, we could do
[00:41:38:500 - 00:41:39:750] **Speaker 1:** a quadratic.
[00:41:41:620 - 00:41:43:830] **Speaker 1:** So this is also known as a quadratic loss function
[00:41:43:830 - 00:41:45:649] **Speaker 1:** and you, you would have seen that in your stats
[00:41:45:649 - 00:41:49:850] **Speaker 1:** classes when you're doing um like putting a linear curve
[00:41:49:850 - 00:41:50:929] **Speaker 1:** to a set of data points.
[00:41:52:669 - 00:41:55:659] **Speaker 1:** So it's typically using this, so it's penalising in a
[00:41:55:659 - 00:41:57:020] **Speaker 1:** squared sense rather than linear.
[00:41:59:280 - 00:42:01:100] **Speaker 1:** So we do need to be a little bit careful
[00:42:01:679 - 00:42:04:860] **Speaker 1:** because we have now introduced some bias to our position
[00:42:04:860 - 00:42:05:800] **Speaker 1:** of the optimal solution.
[00:42:07:110 - 00:42:08:330] **Speaker 1:** And.
[00:42:15:189 - 00:42:16:600] **Speaker 1:** Um, yeah, I.
[00:42:19:929 - 00:42:21:889] **Speaker 1:** I don't need to talk too much about ticking off
[00:42:21:889 - 00:42:23:850] **Speaker 1:** regularisation, but um.
[00:42:27:129 - 00:42:29:689] **Speaker 1:** Yeah, if you maybe have like really stiff equations or
[00:42:29:689 - 00:42:34:050] **Speaker 1:** if you've got um quite an L pose solution, you
[00:42:34:050 - 00:42:35:530] **Speaker 1:** can use some regularisation.
[00:42:35:729 - 00:42:39:449] **Speaker 1:** So introducing some additional diffusion and things into the the
[00:42:39:449 - 00:42:40:989] **Speaker 1:** PDEs and solve that.
[00:42:41:860 - 00:42:45:389] **Speaker 1:** Um, but this is, yeah, a different, different topic.
[00:42:48:209 - 00:42:48:889] **Speaker 1:** All right.
[00:42:50:530 - 00:42:52:389] **Speaker 1:** So what have we done all this for?
[00:42:54:699 - 00:43:00:659] **Speaker 1:** Now Simulation driven design, uh, we had a visiting guy,
[00:43:00:810 - 00:43:03:290] **Speaker 1:** professor, a few years back, and he gave a, a
[00:43:03:290 - 00:43:06:290] **Speaker 1:** workshop on this, uh, which was reasonably interesting, so that's
[00:43:06:290 - 00:43:06:489] **Speaker 1:** cool.
[00:43:06:780 - 00:43:10:500] **Speaker 1:** Uh, but he essentially discussed that our classical engineering design
[00:43:10:500 - 00:43:16:139] **Speaker 1:** process involves planning, our concept design, preliminary, detailed verification and
[00:43:16:139 - 00:43:16:500] **Speaker 1:** production.
[00:43:17:389 - 00:43:20:389] **Speaker 1:** So you would have approached these uh workflows in your
[00:43:20:389 - 00:43:21:429] **Speaker 1:** design courses so far?
[00:43:23:139 - 00:43:27:149] **Speaker 1:** And numerical simulations, so CFD FEA are performed during the
[00:43:27:149 - 00:43:27:989] **Speaker 1:** detailed design.
[00:43:28:350 - 00:43:30:169] **Speaker 1:** So they obviously take a bit longer to do.
[00:43:30:590 - 00:43:33:570] **Speaker 1:** So your preliminary design is prior to these simulations.
[00:43:35:189 - 00:43:38:610] **Speaker 1:** The concept of stimulation-driven design is that we're gonna use
[00:43:38:610 - 00:43:40:870] **Speaker 1:** these tools earlier in the design process.
[00:43:41:679 - 00:43:45:580] **Speaker 1:** So maybe during the exploration phase, we might use topological
[00:43:45:580 - 00:43:47:260] **Speaker 1:** optimisation methods as well.
[00:43:47:810 - 00:43:50:840] **Speaker 1:** So if we don't want to be constrained by some
[00:43:50:840 - 00:43:52:580] **Speaker 1:** topology if we're thinking of like a bridge.
[00:43:54:149 - 00:44:00:270] **Speaker 1:** Um, 2 many papers.
[00:44:05:330 - 00:44:08:909] **Speaker 1:** Uh, in fact, the lab next week is on optimisation,
[00:44:09:050 - 00:44:10:790] **Speaker 1:** so I'll just briefly introduce that now.
[00:44:12:379 - 00:44:14:389] **Speaker 1:** In this problem, we're going to be looking at a
[00:44:14:389 - 00:44:14:810] **Speaker 1:** beam.
[00:44:15:709 - 00:44:19:070] **Speaker 1:** So the beam could just be a rectangular object and
[00:44:19:070 - 00:44:23:669] **Speaker 1:** we might want to constrain the left-hand side because it's
[00:44:23:669 - 00:44:26:889] **Speaker 1:** fixed to the wall and we're applying some loading condition
[00:44:27:350 - 00:44:29:889] **Speaker 1:** and we want to minimise the mass of the beam,
[00:44:30:389 - 00:44:32:310] **Speaker 1:** so saving material cost and weight.
[00:44:33:370 - 00:44:37:760] **Speaker 1:** If we have a parameter optimisation, we would minimise based
[00:44:37:760 - 00:44:39:729] **Speaker 1:** on adjusting these two reference points.
[00:44:41:340 - 00:44:44:350] **Speaker 1:** If we looked at a shape optimisation, so changing the
[00:44:44:350 - 00:44:47:540] **Speaker 1:** entire lower boundary, we would get a different solution and
[00:44:47:540 - 00:44:48:810] **Speaker 1:** slightly more optimal.
[00:44:49:429 - 00:44:53:209] **Speaker 1:** The last one here is topology optimisation and that's where
[00:44:53:389 - 00:44:56:510] **Speaker 1:** it's no longer constrained by these sort of 4 or
[00:44:56:510 - 00:44:57:330] **Speaker 1:** 6 points.
[00:44:57:629 - 00:44:59:209] **Speaker 1:** It's no longer looking like a rectangle.
[00:44:59:310 - 00:45:01:030] **Speaker 1:** It allows holes to form within.
[00:45:02:149 - 00:45:04:959] **Speaker 1:** So this is what we mean by topology optimisation, and
[00:45:04:959 - 00:45:05:540] **Speaker 1:** you might.
[00:45:06:469 - 00:45:09:310] **Speaker 1:** Find an optimal solution that isn't intuitive, one that you've
[00:45:09:310 - 00:45:10:050] **Speaker 1:** used before.
[00:45:11:919 - 00:45:15:139] **Speaker 1:** And that's why it's important to have these optimisation.
[00:45:15:939 - 00:45:18:939] **Speaker 1:** Uh, processes early in the design process so that you
[00:45:18:939 - 00:45:21:280] **Speaker 1:** don't, don't go back and forth.
[00:45:21:820 - 00:45:23:500] **Speaker 1:** So as you go through the design process, it gets
[00:45:23:500 - 00:45:25:300] **Speaker 1:** more and more expensive to go back to the earlier
[00:45:25:300 - 00:45:25:739] **Speaker 1:** steps.
[00:45:27:290 - 00:45:28:889] **Speaker 1:** So this could be used to study a wide range
[00:45:28:889 - 00:45:30:169] **Speaker 1:** of different designs.
[00:45:32:750 - 00:45:34:919] **Speaker 1:** So after some rough design is selected, then you want
[00:45:34:919 - 00:45:37:500] **Speaker 1:** to refine and hone in your solution.
[00:45:37:840 - 00:45:39:399] **Speaker 1:** So here you can see that you might not actually
[00:45:39:399 - 00:45:41:330] **Speaker 1:** want to manufacture something with a small hole here.
[00:45:41:840 - 00:45:44:040] **Speaker 1:** So you might make some improvements on this, but it
[00:45:44:040 - 00:45:46:060] **Speaker 1:** gives you a good starting point.
[00:45:46:399 - 00:45:48:800] **Speaker 1:** Another point to raise here is that this is quite
[00:45:48:800 - 00:45:51:800] **Speaker 1:** thin, so it might not be as structurally sound as
[00:45:51:800 - 00:45:52:379] **Speaker 1:** you would want.
[00:45:53:310 - 00:45:56:610] **Speaker 1:** But by simulation, it's predicting that it can support this
[00:45:56:610 - 00:46:00:350] **Speaker 1:** load at a fraction of the mass required for the
[00:46:00:350 - 00:46:00:550] **Speaker 1:** beam.
[00:46:00:659 - 00:46:03:169] **Speaker 1:** So we've got 270 versus 365.
[00:46:05:620 - 00:46:08:080] **Speaker 1:** So you'll be working through these in the next week.
[00:46:17:270 - 00:46:20:570] **Speaker 1:** Yeah, I know, hopefully I'll convince you somewhat of this
[00:46:21:110 - 00:46:21:709] **Speaker 1:** scheme.
[00:46:22:310 - 00:46:24:629] **Speaker 1:** So I think there's some, one of the courses next
[00:46:24:629 - 00:46:27:889] **Speaker 1:** year you can do some more optimisation things, uh, but
[00:46:28:239 - 00:46:30:629] **Speaker 1:** I just wanted to introduce the concept for you in
[00:46:30:629 - 00:46:32:770] **Speaker 1:** this course as it can be quite helpful.
[00:46:34:149 - 00:46:38:209] **Speaker 1:** Are there any questions on this chapter or anything else
[00:46:38:209 - 00:46:39:070] **Speaker 1:** for 302?
[00:46:43:729 - 00:46:44:659] **Speaker 1:** I don't see anyone sleeping.
[00:46:44:699 - 00:46:45:580] **Speaker 1:** Oh yeah, that's good, yeah.
[00:46:46:669 - 00:46:47:669] **Speaker 2:** getting stuck in the little.
[00:46:48:699 - 00:46:49:060] **Speaker 2:** Minimum.
[00:46:50:939 - 00:46:51:800] **Speaker 1:** Yes, good point.
[00:46:52:060 - 00:46:52:520] **Speaker 1:** So.
[00:46:55:110 - 00:46:59:590] **Speaker 1:** These multimodal problems, you could get stuck in these local
[00:46:59:590 - 00:47:01:270] **Speaker 1:** minima if you're using the steepest descent.
[00:47:02:129 - 00:47:05:419] **Speaker 1:** And because you don't know what the whole function represents
[00:47:05:419 - 00:47:07:760] **Speaker 1:** or is, you don't know if you're here or here.
[00:47:08:540 - 00:47:12:399] **Speaker 1:** Um So it can be quite helpful to do a
[00:47:12:399 - 00:47:15:840] **Speaker 1:** global search initially, maybe with Monte Carlo or a grid
[00:47:15:840 - 00:47:18:600] **Speaker 1:** search, just to get a feeling for the whole parameter
[00:47:18:600 - 00:47:21:919] **Speaker 1:** space and then apply the steepest descent on the local
[00:47:21:919 - 00:47:22:280] **Speaker 1:** region.
[00:47:24:979 - 00:47:25:300] **Speaker 1:** Yeah.
[00:47:31:939 - 00:47:32:219] **Speaker 1:** Cool.
[00:47:43:590 - 00:47:47:590] **Speaker 1:** So just another reminder because sometimes people forget what exercises
[00:47:47:590 - 00:47:49:379] **Speaker 1:** at the end of each chapter you can work through
[00:47:49:379 - 00:47:49:750] **Speaker 1:** at home.
[00:47:50:540 - 00:47:54:020] **Speaker 1:** And this one, we're going to look at the banana
[00:47:54:020 - 00:47:56:080] **Speaker 1:** function or Rosenbach function.
[00:47:56:580 - 00:48:00:459] **Speaker 1:** So this has a global minimum, but it has quite
[00:48:00:459 - 00:48:03:719] **Speaker 1:** a large value of values that are small.
[00:48:04:419 - 00:48:07:159] **Speaker 1:** So it's quite difficult to actually get the minimum value.
[00:48:07:909 - 00:48:09:479] **Speaker 1:** So this is sort of a test function that people
[00:48:09:479 - 00:48:11:419] **Speaker 1:** use to test the optimisation methods.
[00:48:12:000 - 00:48:14:860] **Speaker 1:** And we're gonna use our steepest descent on this function.
[00:48:16:760 - 00:48:19:360] **Speaker 1:** So you'll you'll go through those steps and encode it
[00:48:19:360 - 00:48:19:959] **Speaker 1:** up in Python.
[00:48:20:040 - 00:48:25:449] **Speaker 1:** I've provided the um, Example script as well on there
[00:48:25:449 - 00:48:26:189] **Speaker 1:** if you're stuck.
[00:48:27:209 - 00:48:30:570] **Speaker 1:** And the solutions to the exercises are in the back
[00:48:30:570 - 00:48:32:810] **Speaker 1:** of the course reader if you're if you're stuck as
[00:48:32:810 - 00:48:33:189] **Speaker 1:** well.
[00:48:35:260 - 00:48:38:120] **Speaker 1:** 00, we made it through this week.
[00:48:39:040 - 00:48:42:439] **Speaker 1:** So, um, next week we'll continue probably with finite elements.
[00:48:43:929 - 00:48:46:469] **Speaker 1:** And Yeah, that's it.
[00:48:46:639 - 00:48:47:520] **Speaker 1:** So have a good weekend.
[00:48:48:530 - 00:48:51:330] **Speaker 1:** Um, I'll probably have to be working on the exam,
[00:48:51:530 - 00:48:52:770] **Speaker 1:** but I'm sure you'll have a break.
[00:49:08:120 - 00:49:08:129] **Speaker 0:** Yes.
[00:49:29:659 - 00:49:29:719] **Speaker 0:** It's like.
[00:49:37:540 - 00:49:37:570] **Speaker 0:** 65.
[00:49:39:489 - 00:49:39:500] **Speaker 0:** Yeah.
[00:49:46:850 - 00:49:46:860] **Speaker 0:** Yes.
[00:49:59:179 - 00:50:12:810] **Speaker 0:** That You've been a very.
[00:50:38:050 - 00:52:44:459] **Speaker 0:** You Sorry.

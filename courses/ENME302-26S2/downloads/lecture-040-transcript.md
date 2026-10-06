# ENME302-26S2 Lecture 40 native Echo transcript

Date: October 2, 2026 11:00am-11:55am
Transcript type: native Echo automated transcript.

[00:00:29:110 - 00:01:19:029] **Speaker 0:** to of OK.
[00:01:28:610 - 00:01:29:050] **Speaker 0:** Yeah.
[00:01:38:910 - 00:01:41:830] **Speaker 1:** Oh, good morning, um, well done for making it.
[00:01:42:029 - 00:01:44:589] **Speaker 1:** Uh, I was thinking, oh maybe we should just, should
[00:01:44:589 - 00:01:46:470] **Speaker 1:** have cancelled this week for lectures, but.
[00:01:47:239 - 00:01:49:559] **Speaker 1:** We've we've managed to go through the final elements, so
[00:01:49:559 - 00:01:51:760] **Speaker 1:** we've got lots of time to go through practise exams
[00:01:51:760 - 00:01:54:080] **Speaker 1:** in the last couple of weeks of, of term, which
[00:01:54:080 - 00:01:55:620] **Speaker 1:** is always appreciated, I think.
[00:01:57:309 - 00:01:59:849] **Speaker 1:** So we'll continue with finite elements.
[00:02:00:309 - 00:02:02:190] **Speaker 1:** Are there any questions before we dive in?
[00:02:04:519 - 00:02:07:629] **Speaker 1:** My question is Of course there's no questions.
[00:02:08:348 - 00:02:13:108] **Speaker 1:** Um, so we did this for one element, and I
[00:02:13:108 - 00:02:15:248] **Speaker 1:** set for homework to do it for the other three.
[00:02:15:908 - 00:02:19:059] **Speaker 1:** So, The, the only thing that changes between each one,
[00:02:19:139 - 00:02:20:699] **Speaker 1:** we don't have to go through all these integrals again.
[00:02:20:830 - 00:02:22:660] **Speaker 1:** The only thing that changes is the degrees of freedom.
[00:02:22:979 - 00:02:27:320] **Speaker 1:** So this element one was operating from X1 to X2.
[00:02:27:990 - 00:02:30:029] **Speaker 1:** The dependent variable was T1 and T2.
[00:02:31:259 - 00:02:34:229] **Speaker 1:** And we can look at the other ones, so I
[00:02:34:229 - 00:02:34:850] **Speaker 1:** 2.
[00:02:36:139 - 00:02:40:690] **Speaker 1:** Is from X2 to X3, T2 to T3.
[00:02:42:229 - 00:02:43:630] **Speaker 1:** Element 3.
[00:02:45:089 - 00:02:49:149] **Speaker 1:** They're largely the same size, X3, X4.
[00:02:50:009 - 00:02:53:070] **Speaker 1:** From T3 to T4 and element 4.
[00:02:55:600 - 00:03:00:690] **Speaker 1:** Is from X 4 X5, D4.
[00:03:01:570 - 00:03:02:160] **Speaker 1:** And teapot.
[00:03:02:539 - 00:03:03:919] **Speaker 1:** So if you just want to try and visualise what.
[00:03:04:740 - 00:03:07:000] **Speaker 1:** The, the elements we're looking at at the moment.
[00:03:08:470 - 00:03:10:500] **Speaker 1:** So the different variable that we're solving for each of
[00:03:10:500 - 00:03:12:800] **Speaker 1:** these elements, we've got T2.
[00:03:13:720 - 00:03:17:880] **Speaker 1:** And T3 for element 2, for element 3, we've got
[00:03:17:880 - 00:03:19:580] **Speaker 1:** T3 and T4.
[00:03:20:679 - 00:03:23:399] **Speaker 1:** For element 4, we've got nodes 4 and 5.
[00:03:29:919 - 00:03:32:279] **Speaker 1:** Now we can apply the same pattern as we did
[00:03:32:600 - 00:03:34:139] **Speaker 1:** for our first element, element one.
[00:03:35:070 - 00:03:38:889] **Speaker 1:** And we've got these 0.4s and minus 0.4s in our
[00:03:39:029 - 00:03:41:110] **Speaker 1:** uh coefficient, so we can chuck that in.
[00:03:46:000 - 00:03:48:960] **Speaker 1:** And the the forcing terms or those boundary conditions being
[00:03:48:960 - 00:03:52:149] **Speaker 1:** applied on that right-hand side is going to be the
[00:03:52:979 - 00:03:57:399] **Speaker 1:** Derivative at the left-hand node and negative, and then the
[00:03:57:399 - 00:03:59:440] **Speaker 1:** derivative on the right-hand side, positive.
[00:04:01:490 - 00:04:06:550] **Speaker 1:** So we're left with minus DT tilta by DX.
[00:04:08:600 - 00:04:11:380] **Speaker 1:** At X2 That's on the left.
[00:04:12:940 - 00:04:15:820] **Speaker 1:** And we've got that source term, which is going to
[00:04:15:820 - 00:04:18:299] **Speaker 1:** be the same value throughout the domain.
[00:04:19:079 - 00:04:24:949] **Speaker 1:** We calculated For a constant source of 10 across each
[00:04:24:949 - 00:04:26:519] **Speaker 1:** interval is 12.5.
[00:04:26:799 - 00:04:29:558] **Speaker 1:** We saw that because of symmetry shape functions of N1
[00:04:29:558 - 00:04:33:229] **Speaker 1:** and N2, it was equal for both uh equations of
[00:04:33:229 - 00:04:33:878] **Speaker 1:** element one.
[00:04:35:510 - 00:04:38:549] **Speaker 1:** And this extends across elements 23, and 4.
[00:04:38:709 - 00:04:41:709] **Speaker 1:** They all have the same source term, they're all of
[00:04:41:709 - 00:04:45:630] **Speaker 1:** equal length, so they all have the same magnitude, 12.5.
[00:04:51:670 - 00:04:53:429] **Speaker 1:** So that's the left-hand side.
[00:04:53:500 - 00:04:55:170] **Speaker 1:** On the right-hand side we've got the positive.
[00:04:55:940 - 00:05:00:589] **Speaker 1:** DT tilda by DX at X3, and again we've got
[00:05:00:589 - 00:05:01:510] **Speaker 1:** 12.5.
[00:05:04:160 - 00:05:05:679] **Speaker 1:** So we're gonna use that same pattern for the other
[00:05:05:679 - 00:05:06:420] **Speaker 1:** two elements.
[00:05:06:559 - 00:05:07:540] **Speaker 1:** We've got 0.4.
[00:05:09:779 - 00:05:19:959] **Speaker 1:** -0.4 And these boundary contributions, we've got minus.
[00:05:20:820 - 00:05:26:799] **Speaker 1:** DT tilda via DX at X3, and at source 12.5
[00:05:27:269 - 00:05:28:739] **Speaker 1:** DT tilda via DX.
[00:05:29:720 - 00:05:31:869] **Speaker 1:** axe 4 in 12.5.
[00:05:32:799 - 00:05:35:440] **Speaker 1:** And our last element on the right, we've got.
[00:05:36:220 - 00:05:42:640] **Speaker 1:** Uh, minus DT tilter by DX at X4 + 12.5,
[00:05:43:059 - 00:05:48:010] **Speaker 1:** and DT tilda by DX at X5 + 12.5.
[00:05:49:670 - 00:05:51:380] **Speaker 1:** So a little bit tedious.
[00:05:52:109 - 00:05:53:380] **Speaker 1:** But we've got 4 elements.
[00:05:55:600 - 00:05:57:859] **Speaker 1:** A very similar pattern for each case.
[00:05:59:450 - 00:06:03:700] **Speaker 1:** Um, we're evaluating the gradients at each of these nodes.
[00:06:04:799 - 00:06:07:250] **Speaker 1:** And we'll see shortly that we need to make sure
[00:06:07:250 - 00:06:09:450] **Speaker 1:** that they're matching, so they're cancelled.
[00:06:12:019 - 00:06:14:859] **Speaker 1:** So we've got 4 sets of element equations and now
[00:06:14:859 - 00:06:16:559] **Speaker 1:** the next stage is to assemble them.
[00:06:16:980 - 00:06:18:959] **Speaker 1:** So this, this should be familiar with what you did
[00:06:19:579 - 00:06:22:100] **Speaker 1:** in those 1st 4 weeks maybe, if you recall that
[00:06:22:100 - 00:06:22:660] **Speaker 1:** far back.
[00:06:22:980 - 00:06:25:750] **Speaker 1:** And we're gonna have a system of equations.
[00:06:26:140 - 00:06:28:320] **Speaker 1:** We've got 5 degrees of freedom overall.
[00:06:28:899 - 00:06:31:399] **Speaker 1:** From our linear equations, we've got 1234, and 5.
[00:06:32:179 - 00:06:34:700] **Speaker 1:** So we're gonna have a 5 by 5 matrix of
[00:06:34:700 - 00:06:35:459] **Speaker 1:** coefficients.
[00:06:37:260 - 00:06:39:410] **Speaker 1:** So this time I've just left it typed out, but
[00:06:39:410 - 00:06:42:260] **Speaker 1:** we've got the contribution from each element.
[00:06:42:739 - 00:06:44:459] **Speaker 1:** So just to make sure that you know how to,
[00:06:44:649 - 00:06:48:380] **Speaker 1:** to create these global matrices, it's important.
[00:06:49:809 - 00:06:54:649] **Speaker 1:** So we've got the contribution from element one.
[00:06:56:119 - 00:06:59:000] **Speaker 1:** We've got 0.4, 0.4 minus 0.4 minus 0.4.
[00:06:59:440 - 00:07:03:679] **Speaker 1:** So each of these columns obviously correspond to those uh
[00:07:03:679 - 00:07:04:920] **Speaker 1:** dependent variables, T1 and T2.
[00:07:06:450 - 00:07:09:880] **Speaker 1:** All the other entries in that stiffness matrix is zero.
[00:07:10:369 - 00:07:12:970] **Speaker 1:** We're starting as an empty matrix.
[00:07:14:660 - 00:07:15:989] **Speaker 1:** So that's for element one.
[00:07:17:450 - 00:07:21:920] **Speaker 1:** For E 2 We can see that we've got the
[00:07:21:920 - 00:07:23:600] **Speaker 1:** same 0.4 pattern.
[00:07:24:489 - 00:07:27:200] **Speaker 1:** But these are multiplied by T2 and T3.
[00:07:27:540 - 00:07:30:619] **Speaker 1:** So we're gonna look at columns T2 and T3.
[00:07:32:910 - 00:07:36:600] **Speaker 1:** So here we're going to add 0.4 and 0.4 together
[00:07:36:600 - 00:07:39:750] **Speaker 1:** because we already had 0.4 in row 2, column 2.
[00:07:40:450 - 00:07:42:540] **Speaker 1:** So I've got double contribution.
[00:07:43:390 - 00:07:46:649] **Speaker 1:** And then we've got the contributions at -0.4 and 0.4.
[00:07:49:059 - 00:07:53:130] **Speaker 1:** So That's for element 2, for element 3.
[00:07:55:450 - 00:07:57:390] **Speaker 1:** We're continuing to stack.
[00:07:59:579 - 00:08:04:339] **Speaker 1:** We've got T3 and T4.
[00:08:05:500 - 00:08:06:510] **Speaker 1:** So we're adding them here.
[00:08:07:230 - 00:08:08:630] **Speaker 1:** And you can see that this is starting to create
[00:08:08:630 - 00:08:10:109] **Speaker 1:** a tridiagonal matrix.
[00:08:12:220 - 00:08:16:260] **Speaker 1:** Lastly, element 4, and we have our final global stiffness
[00:08:16:260 - 00:08:16:820] **Speaker 1:** matrix KG.
[00:08:25:079 - 00:08:25:440] **Speaker 1:** Cool.
[00:08:26:450 - 00:08:27:730] **Speaker 1:** Any questions on that?
[00:08:27:890 - 00:08:32:809] **Speaker 1:** Is that super, super obvious or is it confusing?
[00:08:37:200 - 00:08:38:039] **Speaker 1:** Any indication.
[00:08:38:130 - 00:08:39:049] **Speaker 1:** It's a good, that's good.
[00:08:39:099 - 00:08:41:250] **Speaker 1:** That's reassuring because you might need it for, for some
[00:08:41:250 - 00:08:42:070] **Speaker 1:** assessments.
[00:08:42:650 - 00:08:46:280] **Speaker 1:** So The next stage is we're gonna do the same
[00:08:46:820 - 00:08:48:500] **Speaker 1:** for the global forcing vector.
[00:08:50:630 - 00:08:52:510] **Speaker 1:** So just as we did for the cases, we do
[00:08:52:510 - 00:08:53:369] **Speaker 1:** the same for F's.
[00:08:53:830 - 00:08:56:390] **Speaker 1:** So we've got these contributions and you can immediately start
[00:08:56:390 - 00:08:59:950] **Speaker 1:** to see that these DT by DX at X2 is
[00:08:59:950 - 00:09:03:909] **Speaker 1:** going to cancel with this minus DT by DX at
[00:09:03:909 - 00:09:04:469] **Speaker 1:** X2.
[00:09:09:599 - 00:09:11:500] **Speaker 1:** And I've copy pasted these just for convenience.
[00:09:11:809 - 00:09:13:690] **Speaker 1:** So we're gonna add in uh if.
[00:09:15:479 - 00:09:19:020] **Speaker 1:** One To our global, global vector FG.
[00:09:21:940 - 00:09:23:320] **Speaker 1:** So we'll go through the motion.
[00:09:24:799 - 00:09:28:109] **Speaker 1:** So we're adding this, we've got minus DT tilda by
[00:09:28:109 - 00:09:33:239] **Speaker 1:** DX at X1 and 12.5, and we've got DT tilda
[00:09:33:510 - 00:09:35:049] **Speaker 1:** by DX at x2.
[00:09:35:750 - 00:09:36:950] **Speaker 1:** And 12.5.
[00:09:37:349 - 00:09:38:789] **Speaker 1:** The other entries are 0 for now.
[00:09:39:739 - 00:09:42:210] **Speaker 1:** Now when we go to add element two, as I
[00:09:42:210 - 00:09:44:059] **Speaker 1:** say, it's gonna cancel because we've got these positive and
[00:09:44:059 - 00:09:47:260] **Speaker 1:** negatives, uh, DT by DX and X2.
[00:09:48:679 - 00:09:50:770] **Speaker 1:** So the, the top remains the same.
[00:09:53:309 - 00:09:58:229] **Speaker 1:** Minus DT to DXX1 plus 12.5.
[00:09:59:570 - 00:10:02:599] **Speaker 1:** And these cancel, so that's nothing.
[00:10:03:140 - 00:10:06:659] **Speaker 1:** The source terms add up, so now we've got 25.
[00:10:10:039 - 00:10:12:359] **Speaker 1:** And that 3rd entry.
[00:10:13:270 - 00:10:15:809] **Speaker 1:** DT Toda5 X.
[00:10:17:080 - 00:10:18:510] **Speaker 1:** axe 3 + 12.5.
[00:10:26:059 - 00:10:31:039] **Speaker 1:** So Essentially all of the interior gradients, DT tilted by
[00:10:31:039 - 00:10:32:710] **Speaker 1:** DX are going to cancel with one another along that,
[00:10:34:080 - 00:10:36:039] **Speaker 1:** uh, those sets of elements.
[00:10:37:010 - 00:10:38:830] **Speaker 1:** So we'll do the same for element 3.
[00:10:40:989 - 00:10:43:489] **Speaker 1:** So the top entry remains unchanged.
[00:10:48:140 - 00:10:49:140] **Speaker 1:** And the 2nd entry.
[00:10:49:969 - 00:10:53:169] **Speaker 1:** And the 3rd row, are these cancel, and we're just
[00:10:53:169 - 00:10:54:030] **Speaker 1:** left with 25.
[00:10:58:719 - 00:11:03:500] **Speaker 1:** DT tota by DXXX 4 plus 12.5.
[00:11:14:900 - 00:11:16:619] **Speaker 1:** And that last step.
[00:11:18:020 - 00:11:19:960] **Speaker 1:** Is adding element 4.
[00:11:39:849 - 00:11:44:919] **Speaker 1:** So we've got minus DT tilda by DX at X1
[00:11:45:010 - 00:11:48:739] **Speaker 1:** plus 12.5, 25, 25.
[00:11:49:989 - 00:11:52:010] **Speaker 1:** D5 feels like bingo, bingo, but yeah.
[00:11:52:830 - 00:11:57:000] **Speaker 1:** And then last one we've got DT Tilda 5X.
[00:11:58:030 - 00:12:00:760] **Speaker 1:** axe 5 + 12.5.
[00:12:05:729 - 00:12:08:289] **Speaker 1:** Alright, so in summary, we've got the source term uh
[00:12:08:289 - 00:12:11:409] **Speaker 1:** being applied uniformly over the interior, uh, degrees of freedom.
[00:12:12:140 - 00:12:15:049] **Speaker 1:** It's only got 12.5, it's essentially only seeing one side,
[00:12:15:510 - 00:12:17:809] **Speaker 1:** um, on the ends, so that's why it's half.
[00:12:18:919 - 00:12:21:080] **Speaker 1:** And we've got these gradients on the left and right
[00:12:21:080 - 00:12:24:739] **Speaker 1:** boundaries, which are unknown values.
[00:12:25:239 - 00:12:28:400] **Speaker 1:** These are the gradients at those end nodes.
[00:12:30:750 - 00:12:33:460] **Speaker 1:** So the next step is to apply our boundary conditions.
[00:12:34:960 - 00:12:39:159] **Speaker 1:** And the default that you see in console is that
[00:12:39:159 - 00:12:41:950] **Speaker 1:** no flux, like the DT by DX would be zero,
[00:12:42:320 - 00:12:44:559] **Speaker 1:** and that would be the natural or the easy boundary
[00:12:44:559 - 00:12:46:760] **Speaker 1:** condition because essentially those are just cancelling out and we're
[00:12:46:760 - 00:12:47:159] **Speaker 1:** finished.
[00:12:47:969 - 00:12:50:299] **Speaker 1:** But if we've got a Dirichlet boundary condition, we do
[00:12:50:299 - 00:12:51:219] **Speaker 1:** need to do some more work.
[00:12:51:380 - 00:12:53:700] **Speaker 1:** So this is an example of applying the the Dirichlet
[00:12:53:700 - 00:12:54:359] **Speaker 1:** boundary condition.
[00:12:56:479 - 00:12:59:580] **Speaker 1:** The temperature on the left-hand side is equal to TA
[00:12:59:580 - 00:13:02:119] **Speaker 1:** or 40, and the right is equal to 200.
[00:13:03:030 - 00:13:07:820] **Speaker 1:** So because we're modifying the temperature field or the temperature
[00:13:07:820 - 00:13:08:909] **Speaker 1:** value at node one.
[00:13:09:700 - 00:13:10:179] **Speaker 1:** 21.
[00:13:11:070 - 00:13:13:909] **Speaker 1:** We need to rearrange or solve that equation.
[00:13:15:239 - 00:13:19:479] **Speaker 1:** So if we substitute in T1 equal to TA, our
[00:13:19:479 - 00:13:22:619] **Speaker 1:** first equation becomes 0.4 TA.
[00:13:26:549 - 00:13:29:270] **Speaker 1:** 0.4 times T1, T1 equal to TA and then we've
[00:13:29:270 - 00:13:31:270] **Speaker 1:** got -0.4 times T2.
[00:13:38:010 - 00:13:40:599] **Speaker 1:** And on the right-hand side, we set our global forcing
[00:13:40:599 - 00:13:43:489] **Speaker 1:** vector, that first row was minus DT tilted by DXZ
[00:13:43:489 - 00:13:44:010] **Speaker 1:** X1.
[00:13:49:429 - 00:13:50:989] **Speaker 1:** Plus 12.5.
[00:14:01:059 - 00:14:03:239] **Speaker 1:** So out of these, which are the unknown values?
[00:14:12:349 - 00:14:13:150] **Speaker 1:** Yep, T2.
[00:14:16:150 - 00:14:16:869] **Speaker 1:** And this gradient.
[00:14:17:150 - 00:14:17:609] **Speaker 1:** That's right.
[00:14:17:950 - 00:14:19:979] **Speaker 1:** So we're gonna put the unknown values on the left-hand
[00:14:19:979 - 00:14:21:869] **Speaker 1:** side just as we normally do to create that big
[00:14:21:869 - 00:14:22:849] **Speaker 1:** system of equations.
[00:14:23:510 - 00:14:25:429] **Speaker 1:** And we're gonna put all of the known terms, the
[00:14:25:429 - 00:14:28:250] **Speaker 1:** values that are known, uh, on the right-hand side.
[00:14:28:739 - 00:14:31:309] **Speaker 1:** So we've got 12.5 minus 0.4 times 40.
[00:14:33:239 - 00:14:35:719] **Speaker 1:** So that's our, our first equation, we've got DT tilda
[00:14:35:950 - 00:14:40:130] **Speaker 1:** by DX on the left, minus 0.4 T2 and on
[00:14:40:130 - 00:14:43:309] **Speaker 1:** the right we've got -3.5. We'll do the same for
[00:14:43:309 - 00:14:44:190] **Speaker 1:** that last equation.
[00:14:44:849 - 00:14:45:799] **Speaker 1:** We've got minus.
[00:14:49:299 - 00:14:52:440] **Speaker 1:** 0.4 T4.
[00:14:53:789 - 00:14:55:390] **Speaker 1:** Plus surf went for.
[00:14:56:390 - 00:14:58:780] **Speaker 1:** T5, which is what you just said was TB.
[00:15:00:409 - 00:15:02:289] **Speaker 1:** Oh, we've done double T's.
[00:15:03:419 - 00:15:07:570] **Speaker 1:** You Equal to the right-hand side term which is that
[00:15:07:570 - 00:15:09:590] **Speaker 1:** DT tilda RDXZX 5.
[00:15:14:640 - 00:15:15:369] **Speaker 1:** Plus 12.5.
[00:15:21:119 - 00:15:22:919] **Speaker 1:** And this is the last equation down the bottom.
[00:15:23:190 - 00:15:25:309] **Speaker 1:** Now the unknowns are going to be T4 in that
[00:15:25:309 - 00:15:28:260] **Speaker 1:** gradient, T D X at X5.
[00:15:28:799 - 00:15:33:239] **Speaker 1:** And on the right-hand side, we've got 12.5 plus 0.4
[00:15:33:239 - 00:15:39:210] **Speaker 1:** times 200, which is going to be -67.5 with any
[00:15:39:210 - 00:15:39:570] **Speaker 1:** luck.
[00:15:42:190 - 00:15:45:900] **Speaker 1:** So we've also done the same for equations 2 and
[00:15:45:900 - 00:15:52:479] **Speaker 1:** 4 because we've got entries at T5 and at T2
[00:15:52:700 - 00:15:53:820] **Speaker 1:** that we've put on the other side.
[00:15:54:520 - 00:15:56:909] **Speaker 1:** So that's why these are not, not equal to 25.
[00:15:58:549 - 00:16:01:690] **Speaker 1:** So you can do that yourself to, to reassure yourself.
[00:16:03:390 - 00:16:06:119] **Speaker 1:** So in summary, we now have a system of equations
[00:16:06:119 - 00:16:08:599] **Speaker 1:** to solve and we're going to label all of these
[00:16:08:599 - 00:16:11:650] **Speaker 1:** coefficients with uh the K without any other superscripts or
[00:16:11:650 - 00:16:13:000] **Speaker 1:** subscripts, our T being our.
[00:16:14:770 - 00:16:18:049] **Speaker 1:** Vector of unknowns, which now include these gradients at 1
[00:16:18:049 - 00:16:21:549] **Speaker 1:** and 5, and the right-hand side, this, this forcing term.
[00:16:22:280 - 00:16:24:140] **Speaker 1:** So we can solve this system of equations with our
[00:16:24:150 - 00:16:25:219] **Speaker 1:** our favourite tools.
[00:16:25:750 - 00:16:27:320] **Speaker 1:** So whether or not we use the Leben method or
[00:16:27:320 - 00:16:30:840] **Speaker 1:** some direct solve, uh, in, in Python, and this is
[00:16:30:840 - 00:16:32:559] **Speaker 1:** the uh solution.
[00:16:43:669 - 00:16:45:669] **Speaker 1:** So the next stage is to just go and plot
[00:16:45:669 - 00:16:45:969] **Speaker 1:** it.
[00:16:49:020 - 00:16:52:820] **Speaker 1:** So you could plot this visually without Python, right?
[00:16:53:140 - 00:16:55:280] **Speaker 1:** So we've got our temperature field.
[00:16:58:349 - 00:17:02:000] **Speaker 1:** Uh, we've got X and T.
[00:17:03:239 - 00:17:06:040] **Speaker 1:** Our boundary conditions were 40.
[00:17:06:999 - 00:17:10:550] **Speaker 1:** And 200 And our peak value.
[00:17:11:640 - 00:17:13:510] **Speaker 1:** Is 253.
[00:17:14:000 - 00:17:17:520] **Speaker 1:** So maybe we set this, this line equal to 4,
[00:17:18:250 - 00:17:19:160] **Speaker 1:** say this is 40.
[00:17:21:438 - 00:17:23:019] **Speaker 1:** Equals 40.
[00:17:24:479 - 00:17:26:079] **Speaker 1:** At X equals 0.
[00:17:27:540 - 00:17:29:250] **Speaker 1:** And the length, I think it was 10.
[00:17:30:869 - 00:17:31:790] **Speaker 1:** 10 centimetres.
[00:17:36:150 - 00:17:38:589] **Speaker 1:** At 10 is equal to 200.
[00:17:47:719 - 00:17:50:699] **Speaker 1:** And we've sold for T2, 3 and 4.
[00:17:51:359 - 00:17:53:739] **Speaker 1:** T2 was 174.
[00:17:57:540 - 00:18:03:459] **Speaker 1:** So that might be around Uh, Yeah, and we've got
[00:18:03:459 - 00:18:05:040] **Speaker 1:** 245.
[00:18:06:819 - 00:18:12:189] **Speaker 1:** It's a bit higher And 254.
[00:18:14:349 - 00:18:15:099] **Speaker 1:** Something like that.
[00:18:32:680 - 00:18:34:040] **Speaker 1:** I think we did talk a little bit about what
[00:18:34:040 - 00:18:36:199] **Speaker 1:** we expected the solution to be yesterday, maybe we just
[00:18:36:199 - 00:18:38:780] **Speaker 1:** talked about it, but we expected the solution to have
[00:18:38:780 - 00:18:41:339] **Speaker 1:** a temperature field that was higher than the steady-state solution
[00:18:41:339 - 00:18:42:439] **Speaker 1:** because of this heat source.
[00:18:42:750 - 00:18:45:920] **Speaker 1:** We're providing additional heat to the system, so it has
[00:18:45:920 - 00:18:47:839] **Speaker 1:** to have a higher temperature in the middle, and that's
[00:18:47:839 - 00:18:49:199] **Speaker 1:** what we observe here.
[00:18:50:780 - 00:18:54:479] **Speaker 1:** Because this, because we've used these um shape elements, if
[00:18:54:479 - 00:18:57:979] **Speaker 1:** I wanted to plot this using our finite element space,
[00:18:58:439 - 00:19:01:479] **Speaker 1:** what kind of curves would I use between each node?
[00:19:05:280 - 00:19:07:040] **Speaker 1:** Quadradock, maybe.
[00:19:08:979 - 00:19:10:219] **Speaker 1:** Any other guesses?
[00:19:17:630 - 00:19:21:310] **Speaker 1:** Which shape elements did we use for our finite elements?
[00:19:29:810 - 00:19:30:569] **Speaker 1:** Linear, yep.
[00:19:30:930 - 00:19:31:969] **Speaker 1:** 24.
[00:19:34:079 - 00:19:36:199] **Speaker 1:** So because we've used linear shape elements, we've assumed a
[00:19:36:199 - 00:19:39:959] **Speaker 1:** linear profile between each node, like along each individual element,
[00:19:40:079 - 00:19:42:040] **Speaker 1:** we've got linear distributions of temperature.
[00:19:42:729 - 00:19:44:979] **Speaker 1:** So we're gonna have uh just straight lines.
[00:19:48:560 - 00:19:49:489] **Speaker 1:** Between each.
[00:19:50:219 - 00:19:50:859] **Speaker 1:** Degree of freedom.
[00:20:01:030 - 00:20:04:670] **Speaker 1:** So I've provided some code, as I always like to
[00:20:04:670 - 00:20:05:010] **Speaker 1:** do.
[00:20:26:449 - 00:20:30:349] **Speaker 1:** Sort of a I don't know how to get rid
[00:20:30:349 - 00:20:31:250] **Speaker 1:** of those lights.
[00:20:32:400 - 00:20:32:770] **Speaker 1:** There we go.
[00:20:33:560 - 00:20:36:579] **Speaker 1:** Um, so what are we looking at?
[00:20:36:880 - 00:20:38:839] **Speaker 1:** This is sort of a combination of some of the
[00:20:38:839 - 00:20:40:890] **Speaker 1:** earlier code that we had.
[00:20:41:430 - 00:20:44:800] **Speaker 1:** So I wanted to demonstrate in this example that you
[00:20:44:800 - 00:20:48:760] **Speaker 1:** can use, uh, the symbolic, uh, library in Python to
[00:20:48:760 - 00:20:50:719] **Speaker 1:** figure out these, uh, shape functions for us.
[00:20:50:920 - 00:20:53:180] **Speaker 1:** Obviously we know what they are, but that's just a,
[00:20:53:270 - 00:20:54:199] **Speaker 1:** a neat demonstration.
[00:20:54:640 - 00:20:57:979] **Speaker 1:** Then we determine the element equations for each case, again
[00:20:57:979 - 00:20:59:000] **Speaker 1:** in symbolic form.
[00:21:00:000 - 00:21:02:339] **Speaker 1:** And the next stage is to create.
[00:21:03:579 - 00:21:05:160] **Speaker 1:** Our global system of equations.
[00:21:07:949 - 00:21:11:079] **Speaker 1:** Adding all of these individual components and we've got a
[00:21:11:079 - 00:21:14:439] **Speaker 1:** full loop across our number of elements, uh, here.
[00:21:15:829 - 00:21:17:569] **Speaker 1:** So that's what this, this code is doing.
[00:21:18:869 - 00:21:21:589] **Speaker 1:** The final part is applying our boundary conditions our Derek
[00:21:21:589 - 00:21:23:750] **Speaker 1:** based that are a little bit more trickier to implement
[00:21:23:750 - 00:21:26:410] **Speaker 1:** for elements, but we just have to substitute and rearrange.
[00:21:27:390 - 00:21:29:030] **Speaker 1:** The last section is just solving.
[00:21:29:229 - 00:21:31:619] **Speaker 1:** I've just called in our solve to to solve the
[00:21:31:619 - 00:21:33:670] **Speaker 1:** system of equations and in plotting.
[00:21:34:449 - 00:21:38:510] **Speaker 1:** We've used linear interpolations across each one.
[00:21:41:439 - 00:21:45:410] **Speaker 1:** And then Yeah, they've plotted down here.
[00:21:46:280 - 00:21:50:790] **Speaker 1:** So we'll just play that Or wrong This is our
[00:21:50:790 - 00:21:51:550] **Speaker 1:** distribution.
[00:21:53:550 - 00:21:56:030] **Speaker 1:** That was sketched also in our uh course reader.
[00:21:56:900 - 00:22:01:140] **Speaker 1:** So it's showing that it's Peak, not in the centre,
[00:22:01:180 - 00:22:03:660] **Speaker 1:** but further towards the right and that's sort of a
[00:22:03:660 - 00:22:05:680] **Speaker 1:** contribution from the right-hand boundary condition.
[00:22:06:599 - 00:22:09:780] **Speaker 1:** And Yeah, I guess no real surprises.
[00:22:09:790 - 00:22:11:790] **Speaker 1:** If you use quadratic elements, we would expect to have
[00:22:11:790 - 00:22:15:189] **Speaker 1:** a quadratic fit and maybe a more accurate solution.
[00:22:16:260 - 00:22:18:579] **Speaker 1:** And we could increase the number of elements.
[00:22:19:349 - 00:22:21:180] **Speaker 1:** I'm not sure if I coded it to do that,
[00:22:21:280 - 00:22:21:719] **Speaker 1:** but we could.
[00:22:23:359 - 00:22:26:239] **Speaker 1:** We can try and see if we break anything.
[00:22:28:829 - 00:22:31:430] **Speaker 1:** Oh, we've broken up, no, so that, that's, you can
[00:22:31:430 - 00:22:33:569] **Speaker 1:** do that on your own time if you wish, but
[00:22:33:569 - 00:22:34:849] **Speaker 1:** we've done it for 4 elements there.
[00:22:42:109 - 00:22:51:699] **Speaker 1:** B D X So It's going to be the gradient
[00:22:51:849 - 00:22:52:280] **Speaker 1:** at.
[00:22:53:439 - 00:22:55:180] **Speaker 1:** At X1, so.
[00:22:57:650 - 00:22:58:849] **Speaker 1:** Between each.
[00:22:59:859 - 00:23:05:229] **Speaker 1:** Node They, they have to be consistent and equal, that's
[00:23:05:229 - 00:23:07:949] **Speaker 1:** why they're cancelling, uh, on the ends.
[00:23:09:040 - 00:23:12:520] **Speaker 1:** I don't think they're particularly constrained by what the gradient
[00:23:12:520 - 00:23:13:829] **Speaker 1:** is within element one.
[00:23:14:290 - 00:23:15:790] **Speaker 1:** So it's a little bit hard to explain.
[00:23:17:400 - 00:23:18:670] **Speaker 1:** What it means physically.
[00:23:19:439 - 00:23:22:589] **Speaker 1:** Um, but it is part of the, the solution.
[00:23:24:199 - 00:23:27:479] **Speaker 1:** Um, Maybe if we could just calculate.
[00:23:29:339 - 00:23:34:959] **Speaker 1:** And see what those gradients are, so we've got, 254.
[00:23:37:530 - 00:23:38:530] **Speaker 1:** Or maybe 200.
[00:23:45:290 - 00:23:46:979] **Speaker 1:** Divided by.
[00:23:50:250 - 00:23:52:119] **Speaker 1:** This is the trouble with when you're not really keeping
[00:23:52:119 - 00:23:53:239] **Speaker 1:** track of units very well.
[00:23:53:319 - 00:23:55:660] **Speaker 1:** I'm not sure if I should use 2.5 or metres,
[00:23:56:160 - 00:23:58:180] **Speaker 1:** but we'll try 2.5 and just see what happens.
[00:24:00:859 - 00:24:02:739] **Speaker 1:** So yeah, this is a different number to what we
[00:24:02:739 - 00:24:05:000] **Speaker 1:** have uh sold for.
[00:24:05:579 - 00:24:10:640] **Speaker 1:** So This is, yeah, essentially the, the gradient that's been
[00:24:11:180 - 00:24:13:219] **Speaker 1:** approximated at that node.
[00:24:13:300 - 00:24:15:880] **Speaker 1:** It's not the gradient within the node, within the element.
[00:24:16:880 - 00:24:20:510] **Speaker 1:** Um Yeah.
[00:24:23:060 - 00:24:24:430] **Speaker 1:** I'm not sure if I've convinced you.
[00:24:24:540 - 00:24:27:260] **Speaker 1:** I've not convinced myself, but it's um.
[00:24:28:339 - 00:24:31:760] **Speaker 1:** We don't particularly Need it.
[00:24:33:189 - 00:24:35:410] **Speaker 1:** Because if we're only interested in the temperature values across
[00:24:35:410 - 00:24:39:569] **Speaker 1:** domain, then we've already achieved that without those, um, but
[00:24:39:569 - 00:24:41:609] **Speaker 1:** they are still unknowns in the system.
[00:24:44:949 - 00:24:46:770] **Speaker 1:** going back quite far, but why do we use?
[00:24:48:699 - 00:24:51:810] **Speaker 1:** Mm Instead of ET.
[00:24:52:180 - 00:24:56:739] **Speaker 1:** So what we've done here is we've approximated the temperature
[00:24:56:739 - 00:25:00:599] **Speaker 1:** profile within our domain with linear.
[00:25:01:709 - 00:25:02:910] **Speaker 1:** Peace-wise linear functions.
[00:25:04:060 - 00:25:06:739] **Speaker 1:** If and we've left T without the tilda to be
[00:25:06:739 - 00:25:08:670] **Speaker 1:** the true solution or the actual solution.
[00:25:09:140 - 00:25:13:890] **Speaker 1:** So tilt tilda is just the linear piece-wise, um, approximation
[00:25:13:890 - 00:25:17:489] **Speaker 1:** or fit, and we've used that method of weighted residuals.
[00:25:20:010 - 00:25:20:640] **Speaker 1:** Back here.
[00:25:21:739 - 00:25:24:050] **Speaker 1:** Just kind of force the difference to be equal to
[00:25:24:050 - 00:25:24:560] **Speaker 1:** zero.
[00:25:25:050 - 00:25:27:130] **Speaker 1:** So the residuals and those weighting functions.
[00:25:28:709 - 00:25:34:109] **Speaker 1:** If we were approximating a quadratic function with quadratic shape
[00:25:34:109 - 00:25:37:500] **Speaker 1:** elements, the residual would be zero and our T tilda
[00:25:37:500 - 00:25:38:349] **Speaker 1:** would be equal to T.
[00:25:38:910 - 00:25:43:589] **Speaker 1:** But because we've got a nonlinear solution of our temperature
[00:25:43:589 - 00:25:46:229] **Speaker 1:** profile and we're approximating it with linear piece-wise elements, it's
[00:25:46:229 - 00:25:47:550] **Speaker 1:** not going to be a perfect match.
[00:25:48:359 - 00:25:49:939] **Speaker 1:** So that's part of like the discretization error.
[00:25:49:989 - 00:25:53:189] **Speaker 1:** So as we reduce data X, we'll get closer and
[00:25:53:189 - 00:25:54:390] **Speaker 1:** closer to T.
[00:25:55:119 - 00:25:56:089] **Speaker 1:** With our approximation.
[00:25:56:750 - 00:26:01:979] **Speaker 1:** Um Uh, yeah, they are, they are different.
[00:26:04:510 - 00:26:05:050] **Speaker 1:** Good questions.
[00:26:16:349 - 00:26:16:790] **Speaker 1:** Who?
[00:26:26:500 - 00:26:28:079] **Speaker 1:** So I know some of you have started.
[00:26:29:650 - 00:26:30:410] **Speaker 1:** They're silent.
[00:26:33:650 - 00:26:34:589] **Speaker 1:** I just want to do.
[00:26:38:439 - 00:26:39:670] **Speaker 1:** Remind you.
[00:26:43:989 - 00:26:46:589] **Speaker 1:** I've, I've checked all the instructions and things on this
[00:26:46:589 - 00:26:51:550] **Speaker 1:** assignment to Portal or submission page on there.
[00:26:53:520 - 00:27:03:829] **Speaker 1:** So Um, Definitely give it a read.
[00:27:04:069 - 00:27:05:989] **Speaker 1:** So I guess some of the questions I had in
[00:27:05:989 - 00:27:10:300] **Speaker 1:** the lab yesterday was Answered here, uh, and I didn't
[00:27:10:300 - 00:27:12:099] **Speaker 1:** realise that I had provided all of these hints and
[00:27:12:099 - 00:27:16:390] **Speaker 1:** tips, um, which is a shame, but Yeah, I guess
[00:27:16:390 - 00:27:20:390] **Speaker 1:** in particular, um, practise going through the chapter 6, if
[00:27:20:390 - 00:27:24:449] **Speaker 1:** you're particularly stuck, and go through chapter 6 demo because
[00:27:24:540 - 00:27:27:229] **Speaker 1:** that's where I've used like a 3 dimensional array to
[00:27:27:229 - 00:27:28:630] **Speaker 1:** go over the X and Y.
[00:27:29:530 - 00:27:34:170] **Speaker 1:** quotas and A 3rd dimension for the time, so it
[00:27:34:170 - 00:27:36:589] **Speaker 1:** just has that sort of 34 loop approach.
[00:27:37:750 - 00:27:38:930] **Speaker 1:** Maybe I have that open.
[00:27:45:000 - 00:27:46:800] **Speaker 1:** Oh yeah, chapter 6.
[00:27:47:930 - 00:27:51:040] **Speaker 1:** So I mean your assignment might look like a similar
[00:27:51:040 - 00:27:52:439] **Speaker 1:** structure of code, right?
[00:27:52:619 - 00:27:55:449] **Speaker 1:** So you've got your, your time loop on the outside,
[00:27:55:609 - 00:27:57:930] **Speaker 1:** you need to go through each individual spatial coordinate and
[00:27:57:930 - 00:27:59:390] **Speaker 1:** then time on the outside.
[00:27:59:739 - 00:28:02:050] **Speaker 1:** And then you'll have some conditions depending on the boundary
[00:28:02:050 - 00:28:02:329] **Speaker 1:** conditions.
[00:28:03:199 - 00:28:05:560] **Speaker 1:** You're going to have more because you've got more distinct
[00:28:05:560 - 00:28:06:160] **Speaker 1:** boundary conditions.
[00:28:06:199 - 00:28:07:180] **Speaker 1:** You've got corners and everything.
[00:28:07:900 - 00:28:10:260] **Speaker 1:** Uh, but this is just an example, and then for
[00:28:10:260 - 00:28:11:660] **Speaker 1:** plotting some other points.
[00:28:12:020 - 00:28:14:180] **Speaker 1:** So it's helpful to have the three-dimension array so that
[00:28:14:180 - 00:28:16:699] **Speaker 1:** you keep track of the temperature field over time and
[00:28:16:699 - 00:28:18:479] **Speaker 1:** then when you go to do like the minimum value,
[00:28:19:140 - 00:28:21:579] **Speaker 1:** then it's, then it's straightforward, hopefully.
[00:28:22:339 - 00:28:25:300] **Speaker 1:** Um, to, to pick out the, the T value.
[00:28:30:189 - 00:28:30:880] **Speaker 1:** What else?
[00:28:33:060 - 00:28:36:089] **Speaker 1:** There's a couple of questions on the stop condition, like
[00:28:36:089 - 00:28:37:630] **Speaker 1:** how do you get console to stop?
[00:28:38:920 - 00:28:41:079] **Speaker 1:** When it reaches some minimum temperature, so have a read
[00:28:41:079 - 00:28:42:880] **Speaker 1:** of, of this, this one.
[00:28:43:880 - 00:28:44:400] **Speaker 1:** Oops.
[00:28:54:760 - 00:28:56:829] **Speaker 1:** This one goes through some, some of the details.
[00:28:58:359 - 00:29:01:280] **Speaker 1:** So yeah, I guess I've tried to, you don't use
[00:29:01:280 - 00:29:05:199] **Speaker 1:** cookies, um, I've tried to make the assignment so that
[00:29:05:199 - 00:29:07:420] **Speaker 1:** it's a little bit of a next step from from
[00:29:07:420 - 00:29:09:839] **Speaker 1:** what you do in the tutorials, uh, because obviously the
[00:29:09:839 - 00:29:12:319] **Speaker 1:** tutorials are very step by step and a little bit
[00:29:12:319 - 00:29:14:880] **Speaker 1:** tedious and hopefully you get to explore the the features
[00:29:14:880 - 00:29:15:530] **Speaker 1:** of console.
[00:29:16:040 - 00:29:18:310] **Speaker 1:** I've seen quite a few different approaches to solving the
[00:29:18:310 - 00:29:19:760] **Speaker 1:** problems, uh, which is neat.
[00:29:20:000 - 00:29:21:800] **Speaker 1:** There's no right one way to do it.
[00:29:22:239 - 00:29:24:680] **Speaker 1:** Just like coding, you'll have while and for loops in
[00:29:24:680 - 00:29:27:319] **Speaker 1:** console there's different techniques for achieving the same thing.
[00:29:29:650 - 00:29:31:930] **Speaker 1:** And there was a, a request to have like a
[00:29:31:930 - 00:29:35:739] **Speaker 1:** set office hours because As you know, some, some, some
[00:29:35:739 - 00:29:38:579] **Speaker 1:** of your, your classmates are busy doing the competition this
[00:29:38:579 - 00:29:41:560] **Speaker 1:** afternoon, um, so I'll try and be in the office
[00:29:41:650 - 00:29:43:920] **Speaker 1:** after the lecture on Monday, so that's one o'clock.
[00:29:45:010 - 00:29:45:689] **Speaker 1:** On Monday.
[00:29:46:430 - 00:29:49:270] **Speaker 1:** Um, if you have any particular questions, but I do
[00:29:49:270 - 00:29:52:280] **Speaker 1:** encourage people to ask assignment or any related questions in
[00:29:52:280 - 00:29:55:819] **Speaker 1:** the lectures because then I can address the whole class.
[00:29:56:209 - 00:29:59:689] **Speaker 1:** I can't talk to 320 people individually with the same
[00:29:59:689 - 00:30:02:510] **Speaker 1:** enthusiasm or the same details.
[00:30:03:089 - 00:30:05:949] **Speaker 1:** Um, so that's just why I encourage questions in the,
[00:30:06:359 - 00:30:07:449] **Speaker 1:** in the lecture.
[00:30:09:260 - 00:30:13:140] **Speaker 1:** Um, no one's submitted anything, so that's sort of expected
[00:30:13:140 - 00:30:16:420] **Speaker 1:** for, for now, and you've got 11 days, so, yeah.
[00:30:17:680 - 00:30:19:839] **Speaker 1:** Um, are there any questions on this island?
[00:30:19:969 - 00:30:21:810] **Speaker 1:** Is anyone stuck at a point, or you just?
[00:30:22:599 - 00:30:26:699] **Speaker 1:** Marching forward Well not looked at it yet.
[00:30:27:800 - 00:30:30:760] **Speaker 1:** Yeah, that's right, um, you got the weekend, so, yeah.
[00:30:33:359 - 00:30:33:770] **Speaker 1:** Awesome.
[00:30:34:849 - 00:30:36:930] **Speaker 1:** So if there's no questions that you want me to
[00:30:36:930 - 00:30:39:890] **Speaker 1:** cover, I'll, I'll, we'll go through maybe an exercise in
[00:30:39:890 - 00:30:40:729] **Speaker 1:** the finite elements.
[00:30:46:589 - 00:30:50:589] **Speaker 1:** So question one, I'll give you, well, maybe I'll introduce
[00:30:50:589 - 00:30:51:089] **Speaker 1:** it first.
[00:30:51:349 - 00:30:53:849] **Speaker 1:** So we're looking at a steady, uh, heat transfer problem
[00:30:54:109 - 00:30:55:069] **Speaker 1:** with some uniform heating.
[00:30:55:239 - 00:30:56:670] **Speaker 1:** So that's quite similar to what we were just looking
[00:30:56:670 - 00:30:56:989] **Speaker 1:** at.
[00:30:57:339 - 00:30:58:670] **Speaker 1:** So uniform heating Q0.
[00:30:59:349 - 00:31:01:459] **Speaker 1:** We've got the temperature fixed at one end and convective
[00:31:01:459 - 00:31:02:479] **Speaker 1:** heat transfer on the other.
[00:31:03:189 - 00:31:04:920] **Speaker 1:** So it's sort of similar to what you're doing in
[00:31:04:920 - 00:31:05:619] **Speaker 1:** the assignment maybe.
[00:31:06:119 - 00:31:08:699] **Speaker 1:** And we're gonna simplify the algebra, uh, we're gonna set
[00:31:10:109 - 00:31:13:359] **Speaker 1:** TA, which is on the left, equal to the same
[00:31:13:359 - 00:31:14:329] **Speaker 1:** value as T infinity.
[00:31:14:449 - 00:31:17:569] **Speaker 1:** The environmental er or surrounding air equal to 0 and
[00:31:17:569 - 00:31:20:530] **Speaker 1:** this ratio could not over k equal to alpha and
[00:31:20:530 - 00:31:22:170] **Speaker 1:** a over k equal to beta.
[00:31:23:310 - 00:31:26:170] **Speaker 1:** So we've simplified this problem, uh, to equation 12.
[00:31:27:089 - 00:31:29:359] **Speaker 1:** So this one's a bit easy to solve, and we've
[00:31:29:359 - 00:31:30:900] **Speaker 1:** got a couple of boundary conditions on the right.
[00:31:32:209 - 00:31:35:040] **Speaker 1:** We're gonna solve for 4 linear elements of equal length
[00:31:35:040 - 00:31:37:010] **Speaker 1:** and we're gonna figure out those element equations 123, and
[00:31:37:010 - 00:31:37:500] **Speaker 1:** 4.
[00:31:38:000 - 00:31:39:560] **Speaker 1:** So I'll give you a moment maybe just to reflect
[00:31:39:560 - 00:31:42:160] **Speaker 1:** on, on what we did in this chapter using those
[00:31:42:160 - 00:31:43:439] **Speaker 1:** uh separation of variables.
[00:31:43:869 - 00:31:46:380] **Speaker 1:** Oh, not separation of variables, um, method-related residuals.
[00:31:47:420 - 00:31:48:540] **Speaker 1:** Far too many methods.
[00:33:23:050 - 00:33:24:670] **Speaker 1:** Any idea of where to start?
[00:33:33:750 - 00:33:36:180] **Speaker 1:** Saucepan, yep, the saucepan is the easiest bit.
[00:33:37:089 - 00:33:38:489] **Speaker 1:** Maybe we'll leave it to last.
[00:33:39:250 - 00:33:41:489] **Speaker 1:** So we're gonna, we're gonna use our method of weighted
[00:33:41:489 - 00:33:42:310] **Speaker 1:** residuals.
[00:33:44:310 - 00:33:45:739] **Speaker 1:** So first of all, we need to define what the
[00:33:45:739 - 00:33:46:859] **Speaker 1:** residual term is.
[00:33:48:479 - 00:33:56:130] **Speaker 1:** Uh Of X.
[00:33:56:520 - 00:33:58:349] **Speaker 1:** So it's only dependent on X, it's an ODE.
[00:33:59:260 - 00:34:04:170] **Speaker 1:** is going to be Our approximation to the governing equation
[00:34:04:319 - 00:34:05:260] **Speaker 1:** using T tilda.
[00:34:05:550 - 00:34:08:388] **Speaker 1:** So we've got D 2 t tilda.
[00:34:09:628 - 00:34:11:709] **Speaker 1:** By DX2 plus alpha.
[00:34:26:638 - 00:34:29:779] **Speaker 1:** And the method of we residuals is going to integrate.
[00:34:32:148 - 00:34:36:280] **Speaker 1:** Uh Across our domain.
[00:34:37:449 - 00:34:42:350] **Speaker 1:** With the weighting functions from our shape elements, DX equals
[00:34:42:350 - 00:34:46:080] **Speaker 1:** 0, for I equals 1, 21.
[00:34:48:620 - 00:34:51:979] **Speaker 1:** So we're gonna analyse each element one by one.
[00:34:53:370 - 00:34:58:689] **Speaker 1:** So for element one We have an interval.
[00:35:04:719 - 00:35:07:879] **Speaker 1:** And we need to substitute in our residual equation.
[00:35:09:780 - 00:35:12:270] **Speaker 1:** Our limits of integration is the length of the the
[00:35:12:270 - 00:35:17:709] **Speaker 1:** element X1 X2, and we've got the residual D2T tilta
[00:35:17:709 - 00:35:19:989] **Speaker 1:** by DX2 plus alpha.
[00:35:25:000 - 00:35:31:770] **Speaker 1:** Times And I So we're gonna set this equal to
[00:35:31:770 - 00:35:32:229] **Speaker 1:** 0.
[00:35:33:409 - 00:35:36:790] **Speaker 1:** We're gonna find solutions of T tilda that make this,
[00:35:36:850 - 00:35:39:040] **Speaker 1:** uh, solution equal to zero.
[00:35:39:889 - 00:35:42:290] **Speaker 1:** And this is true for i equal to 1 and
[00:35:42:290 - 00:35:42:570] **Speaker 1:** 2.
[00:35:44:489 - 00:35:46:209] **Speaker 1:** We've got 2 degrees of freedom for that linear element.
[00:35:46:280 - 00:35:48:850] **Speaker 1:** If we had quadratic, we'd have 33 equations.
[00:35:52:209 - 00:35:55:100] **Speaker 1:** So again that rationale of reducing the order of the
[00:35:55:100 - 00:35:56:110] **Speaker 1:** 2nd order derivative.
[00:35:57:409 - 00:35:59:050] **Speaker 1:** We're gonna use separation, um.
[00:35:59:790 - 00:36:01:580] **Speaker 1:** Uh, or integration by parts.
[00:36:01:870 - 00:36:03:860] **Speaker 1:** I keep thinking about separation of variables, I don't know
[00:36:03:860 - 00:36:04:050] **Speaker 1:** why.
[00:36:04:949 - 00:36:11:790] **Speaker 1:** Um So we've got The integral from X1 to X2.
[00:36:23:899 - 00:36:23:909] **Speaker 1:** Well.
[00:36:25:389 - 00:36:32:239] **Speaker 1:** Derivative And we're gonna choose U equal to NI.
[00:36:34:360 - 00:36:38:600] **Speaker 1:** And DV equal to our 2nd order derivative.
[00:36:40:149 - 00:36:42:639] **Speaker 1:** So we're gonna reduce the order of the derivative to
[00:36:42:639 - 00:36:43:000] **Speaker 1:** one.
[00:36:43:479 - 00:36:45:939] **Speaker 1:** So we're left with UV.
[00:36:46:439 - 00:36:47:939] **Speaker 1:** So U was NI.
[00:36:48:610 - 00:36:52:209] **Speaker 1:** V is going to be DT Tilda by DX.
[00:36:55:750 - 00:36:56:179] **Speaker 1:** Sorry.
[00:36:58:060 - 00:37:00:649] **Speaker 1:** Um, for now we're just gonna analyse that first part.
[00:37:02:689 - 00:37:04:600] **Speaker 1:** But we, we can include it, because to be honest,
[00:37:04:649 - 00:37:07:389] **Speaker 1:** I find it easier to include it, cos then you
[00:37:07:850 - 00:37:10:409] **Speaker 1:** don't have to do so many steps, um.
[00:37:12:330 - 00:37:32:320] **Speaker 1:** So Plus alpha So now we're going to do integration
[00:37:32:320 - 00:37:32:959] **Speaker 1:** by parts.
[00:37:33:169 - 00:37:34:540] **Speaker 1:** So we've got the integral.
[00:37:35:300 - 00:37:39:889] **Speaker 1:** Of you, which we said was NI and DT Tora
[00:37:40:899 - 00:37:42:020] **Speaker 1:** by DX.
[00:37:43:439 - 00:37:45:520] **Speaker 1:** Along our interval X1 to X2.
[00:37:46:830 - 00:37:49:070] **Speaker 1:** So it's UV and then we've got um.
[00:37:51:260 - 00:37:54:320] **Speaker 1:** What's integration by parts, UV minus VDU or something?
[00:37:55:239 - 00:37:56:179] **Speaker 1:** VDU, yeah.
[00:37:56:600 - 00:37:58:060] **Speaker 1:** So minus the integral.
[00:37:59:260 - 00:38:02:219] **Speaker 1:** Of the DT Toda by DX.
[00:38:02:939 - 00:38:05:280] **Speaker 1:** And DU is going to be that derivative DNI by
[00:38:05:280 - 00:38:05:959] **Speaker 1:** DX.
[00:38:09:649 - 00:38:11:149] **Speaker 1:** I could use different colours, maybe.
[00:38:12:409 - 00:38:13:229] **Speaker 1:** Is that helpful?
[00:38:15:100 - 00:38:16:060] **Speaker 1:** No, it's too late.
[00:38:16:540 - 00:38:19:060] **Speaker 1:** So this, this is, this could be a different colour
[00:38:19:060 - 00:38:19:580] **Speaker 1:** if you want.
[00:38:19:929 - 00:38:21:100] **Speaker 1:** Um, so the source term.
[00:38:22:030 - 00:38:25:500] **Speaker 1:** Uh, You can try.
[00:38:26:449 - 00:38:27:709] **Speaker 1:** I've got heaps of time, maybe.
[00:38:28:560 - 00:38:36:120] **Speaker 1:** So that's X1 So our source down, uh, for now
[00:38:36:120 - 00:38:37:699] **Speaker 1:** we'll just leave it as an integral.
[00:38:38:600 - 00:38:40:620] **Speaker 1:** Alpha N I D X.
[00:38:42:290 - 00:38:48:239] **Speaker 1:** I know people there So this is a weak form
[00:38:48:239 - 00:38:51:639] **Speaker 1:** and encompasses both qua uh both equations for the element
[00:38:51:979 - 00:38:53:439] **Speaker 1:** because this is for both I.
[00:38:54:639 - 00:38:55:919] **Speaker 1:** You've got a 1 and 2.
[00:38:56:889 - 00:38:59:860] **Speaker 1:** So we've got 2 element equations per element, and then
[00:38:59:860 - 00:39:00:699] **Speaker 1:** we stitch them together.
[00:39:02:550 - 00:39:05:090] **Speaker 1:** So in summary, we've got the residual.
[00:39:06:179 - 00:39:09:340] **Speaker 1:** Uh, we've done a method of weighted residuals, subshooting in
[00:39:09:340 - 00:39:12:860] **Speaker 1:** R, I've done integration by parts, and this is our
[00:39:12:860 - 00:39:13:300] **Speaker 1:** weak form.
[00:39:14:280 - 00:39:16:770] **Speaker 1:** So we've got 2 cases, we've got I equal to
[00:39:16:770 - 00:39:18:149] **Speaker 1:** 1 and I equal to 2.
[00:39:27:409 - 00:39:29:870] **Speaker 1:** We could write it out again for fun.
[00:39:30:209 - 00:39:34:649] **Speaker 1:** So we've got N1 DT tora by DX from X1
[00:39:34:649 - 00:39:35:330] **Speaker 1:** to X2.
[00:39:36:340 - 00:39:42:820] **Speaker 1:** Minus X1 X2 DT tilda by DX of DN1 by
[00:39:42:820 - 00:39:43:340] **Speaker 1:** DX.
[00:39:45:219 - 00:39:49:719] **Speaker 1:** Plus X1 X2 alpha N 1 DX.
[00:39:51:330 - 00:39:51:929] **Speaker 1:** Equal to 0.
[00:39:54:030 - 00:39:55:780] **Speaker 1:** So I've substitute I equal to 1.
[00:39:57:010 - 00:39:58:830] **Speaker 1:** Now for those who forget.
[00:39:59:959 - 00:40:01:850] **Speaker 1:** Our shape functions in one.
[00:40:04:020 - 00:40:12:709] **Speaker 1:** Of X And into Of X.
[00:40:21:270 - 00:40:26:270] **Speaker 1:** Now We want to evaluate this expression for a equal
[00:40:26:270 - 00:40:26:600] **Speaker 1:** to one.
[00:40:27:419 - 00:40:28:639] **Speaker 1:** So that's definite integral.
[00:40:30:159 - 00:40:31:080] **Speaker 1:** What does that equal?
[00:40:34:979 - 00:40:39:629] **Speaker 1:** N1 and X2 0.
[00:40:41:000 - 00:40:45:139] **Speaker 1:** And then we've got -1, because N1 at X1 is
[00:40:45:139 - 00:40:50:639] **Speaker 1:** 1, and we've got DT tilda ID X at X1.
[00:40:57:840 - 00:40:58:959] **Speaker 1:** Now this next term.
[00:41:02:669 - 00:41:05:530] **Speaker 1:** We have DT Total by D X.
[00:41:08:810 - 00:41:09:739] **Speaker 1:** And Teetotta.
[00:41:11:889 - 00:41:15:949] **Speaker 1:** Was N1 T1 plus N2 T2.
[00:41:16:290 - 00:41:18:209] **Speaker 1:** That's just a straight line between the two.
[00:41:18:969 - 00:41:19:260] **Speaker 1:** Notes.
[00:41:20:449 - 00:41:26:260] **Speaker 1:** And we said DT Tilda by DX is D2 minus
[00:41:26:260 - 00:41:28:530] **Speaker 1:** T1 over X2 minus X1.
[00:41:29:870 - 00:41:32:350] **Speaker 1:** Which are all constant values across X, they're just values
[00:41:32:350 - 00:41:34:669] **Speaker 1:** at these nodes, so we can pull them outside the
[00:41:34:669 - 00:41:35:370] **Speaker 1:** derivative.
[00:41:36:610 - 00:41:39:620] **Speaker 1:** So we've got T2 minus T1 over X2 minus X1.
[00:41:42:659 - 00:41:46:209] **Speaker 1:** DN1 by DX is the slope or the gradient of
[00:41:46:209 - 00:41:48:879] **Speaker 1:** N1, which is -1 over X.
[00:41:53:129 - 00:41:57:449] **Speaker 1:** And we're left with the integral from X1 X2.
[00:41:59:090 - 00:42:08:699] **Speaker 1:** D X Which we know is equal to data X,
[00:42:08:750 - 00:42:10:199] **Speaker 1:** but we'll do that in the next step.
[00:42:11:580 - 00:42:14:580] **Speaker 1:** And then the source term, what's alpha?
[00:42:14:860 - 00:42:15:580] **Speaker 1:** What is alpha?
[00:42:21:699 - 00:42:23:649] **Speaker 1:** He said you know over k was alpha, so it's
[00:42:23:649 - 00:42:24:199] **Speaker 1:** a constant.
[00:42:25:770 - 00:42:27:560] **Speaker 1:** So alpha can go outside the derivative.
[00:42:31:830 - 00:42:34:209] **Speaker 1:** And we're left with N1 DX.
[00:42:37:040 - 00:42:37:489] **Speaker 1:** 0.
[00:42:39:580 - 00:42:41:209] **Speaker 1:** And I'm probably not that.
[00:42:42:310 - 00:42:43:790] **Speaker 1:** Maybe you can make prettier notes, but.
[00:42:46:239 - 00:42:47:399] **Speaker 1:** Hopefully you're following along.
[00:42:47:840 - 00:42:49:590] **Speaker 1:** So we've done most of the steps.
[00:42:49:639 - 00:42:51:540] **Speaker 1:** We've got a couple more integrals to evaluate.
[00:42:51:879 - 00:42:54:580] **Speaker 1:** We've got this integral and our source term integral.
[00:42:59:570 - 00:43:02:500] **Speaker 1:** It's a real mess, but that's right, it's it's Friday.
[00:43:03:530 - 00:43:08:169] **Speaker 1:** So we've got minus DT tilta by DX at X1.
[00:43:09:629 - 00:43:13:669] **Speaker 1:** Now, when we evaluate this, if we integrate one, we
[00:43:13:669 - 00:43:16:510] **Speaker 1:** just get the, the length, and that's going to cancel
[00:43:16:510 - 00:43:18:469] **Speaker 1:** with one of these X2 minus X1s.
[00:43:19:840 - 00:43:21:889] **Speaker 1:** The minus is gonna cancel with the minus and we're
[00:43:21:889 - 00:43:27:050] **Speaker 1:** gonna be left with plus T2 minus T1 divided by
[00:43:27:050 - 00:43:28:770] **Speaker 1:** X2 minus X1.
[00:43:38:409 - 00:43:40:510] **Speaker 1:** And the system we've got.
[00:43:42:540 - 00:43:43:989] **Speaker 1:** The integral of N1.
[00:43:46:370 - 00:43:47:050] **Speaker 1:** Times alpha.
[00:43:47:250 - 00:43:49:770] **Speaker 1:** Does anyone remember what the integral of our first shape
[00:43:49:770 - 00:43:51:010] **Speaker 1:** function and one is?
[00:43:58:020 - 00:43:59:340] **Speaker 1:** On, on it.
[00:44:00:310 - 00:44:00:419] **Speaker 1:** 2.
[00:44:02:159 - 00:44:04:469] **Speaker 1:** So just if we integrate, so just the area.
[00:44:07:419 - 00:44:14:770] **Speaker 1:** This So we just want to evaluate the Integral of
[00:44:14:770 - 00:44:16:050] **Speaker 1:** our first shape function.
[00:44:17:320 - 00:44:18:689] **Speaker 1:** So this is going to be half the base times
[00:44:18:689 - 00:44:20:689] **Speaker 1:** the height, or you can do some more maths and
[00:44:20:689 - 00:44:21:790] **Speaker 1:** integrate it if you wish.
[00:44:22:300 - 00:44:25:169] **Speaker 1:** So we've got half the base which is X2 minus
[00:44:25:169 - 00:44:27:050] **Speaker 1:** X1, and the height was 1.
[00:44:49:300 - 00:44:49:659] **Speaker 1:** Cool.
[00:44:51:389 - 00:44:52:270] **Speaker 1:** That wasn't too bad.
[00:44:52:830 - 00:44:54:270] **Speaker 1:** So now we do 1 equal 2.
[00:44:58:260 - 00:45:00:379] **Speaker 1:** And I'll give you a minute or two to think
[00:45:00:379 - 00:45:01:939] **Speaker 1:** about how, how to approach that.
[00:46:48:729 - 00:46:50:850] **Speaker 1:** The first step is just to substitute I equal to
[00:46:50:850 - 00:46:53:010] **Speaker 1:** 2 into our weak form of the equation.
[00:46:53:169 - 00:46:54:110] **Speaker 1:** So going back up here.
[00:46:54:860 - 00:46:56:939] **Speaker 1:** And then we're evaluating just as we did earlier.
[00:46:57:300 - 00:46:59:860] **Speaker 1:** Now we've got N2 at X2 is equal to 1,
[00:47:00:100 - 00:47:02:110] **Speaker 1:** N2 at X1 is 0, so we're left with DT
[00:47:02:110 - 00:47:03:520] **Speaker 1:** tilted by D X at X2.
[00:47:03:939 - 00:47:04:860] **Speaker 1:** We've done the same trick.
[00:47:05:139 - 00:47:07:419] **Speaker 1:** These are all constants, chuck them outside the integral and
[00:47:07:419 - 00:47:08:739] **Speaker 1:** we're left with this integral of 1.
[00:47:10:129 - 00:47:13:070] **Speaker 1:** Lastly, the source term integrating our second shape function in
[00:47:13:070 - 00:47:13:290] **Speaker 1:** 2.
[00:47:23:189 - 00:47:26:459] **Speaker 1:** So I've got D T Y D X N X
[00:47:26:459 - 00:47:26:760] **Speaker 1:** 2.
[00:47:30:620 - 00:47:34:159] **Speaker 1:** Minus T2 minus T1 over X2 minus X1.
[00:47:37:500 - 00:47:39:139] **Speaker 1:** Plus alpha.
[00:47:40:189 - 00:47:42:179] **Speaker 1:** Half X2 minus X1.
[00:47:56:919 - 00:47:58:260] **Speaker 1:** Now we want to put them in matrix form.
[00:47:59:639 - 00:48:03:489] **Speaker 1:** So We can look back into our first equation.
[00:48:05:189 - 00:48:05:800] **Speaker 1:** We've got here.
[00:48:06:669 - 00:48:12:250] **Speaker 1:** Um, typically we have The dependent variable.
[00:48:13:229 - 00:48:16:030] **Speaker 1:** Or the coefficient of, uh, the matrix of coefficients.
[00:48:16:979 - 00:48:19:820] **Speaker 1:** Diagonally dominant, so we want the positive values on the
[00:48:19:820 - 00:48:20:600] **Speaker 1:** diagonal.
[00:48:20:979 - 00:48:24:169] **Speaker 1:** So we're gonna make these dependent variables on the other
[00:48:24:169 - 00:48:24:540] **Speaker 1:** side.
[00:48:24:669 - 00:48:26:139] **Speaker 1:** So we're gonna have positive one.
[00:48:28:429 - 00:48:30:330] **Speaker 1:** Over delta X for T1.
[00:48:32:959 - 00:48:34:250] **Speaker 1:** And we've got minus.
[00:48:35:360 - 00:48:36:199] **Speaker 1:** One of T2.
[00:48:37:689 - 00:48:41:209] **Speaker 1:** And what we're left with on this other side, I've
[00:48:41:209 - 00:48:45:510] **Speaker 1:** reversed it and I've got minus DT tilda by DX
[00:48:45:649 - 00:48:46:290] **Speaker 1:** at X1.
[00:48:48:649 - 00:48:50:669] **Speaker 1:** Keep changing the colours and alpha.
[00:48:52:340 - 00:48:55:300] **Speaker 1:** Over 2 times X.
[00:49:00:860 - 00:49:03:979] **Speaker 1:** That 2nd equation, oh, we don't have, that's equal to
[00:49:03:979 - 00:49:04:439] **Speaker 1:** 0.
[00:49:05:010 - 00:49:08:909] **Speaker 1:** for this equation we've got Heaps of negatives, so we've
[00:49:08:909 - 00:49:12:290] **Speaker 1:** got Negative of a negative, and then it's on the
[00:49:12:290 - 00:49:15:010] **Speaker 1:** other side, so it's another negative, so it's -1.
[00:49:16:030 - 00:49:18:040] **Speaker 1:** Again, you can do intermediate steps if you want, and
[00:49:18:040 - 00:49:20:639] **Speaker 1:** then the other one is going to be positive, and
[00:49:20:639 - 00:49:24:959] **Speaker 1:** then we're left with DTra by DX X 2.
[00:49:26:120 - 00:49:29:840] **Speaker 1:** Plus alpha over 2 X.
[00:49:33:459 - 00:49:34:629] **Speaker 1:** So that's pretty much it.
[00:49:34:870 - 00:49:37:610] **Speaker 1:** That's for element 1, elements 23 and 4 are just
[00:49:38:189 - 00:49:39:530] **Speaker 1:** uh looking at those.
[00:49:40:649 - 00:49:42:870] **Speaker 1:** Nodes that are unknown, the degrees of freedom and changing
[00:49:42:870 - 00:49:43:100] **Speaker 1:** them.
[00:49:43:790 - 00:49:44:989] **Speaker 1:** And then searching them all together.
[00:49:45:189 - 00:49:46:929] **Speaker 1:** So that's pretty much the final element method that we,
[00:49:47:110 - 00:49:48:510] **Speaker 1:** that we're learning in this class.
[00:49:49:030 - 00:49:51:989] **Speaker 1:** So as long as you can do these steps, uh,
[00:49:52:030 - 00:49:52:830] **Speaker 1:** you should be all good.
[00:49:53:719 - 00:49:55:239] **Speaker 1:** The rest of it should be pretty straightforward.
[00:49:57:689 - 00:49:59:129] **Speaker 1:** That's examinable, yeah.
[00:50:01:929 - 00:50:04:610] **Speaker 0:** Square T over DX always doing the same thing each
[00:50:04:610 - 00:50:06:129] **Speaker 0:** time, do we have to go through all this?
[00:50:11:439 - 00:50:12:139] **Speaker 1:** D2.
[00:50:13:469 - 00:50:16:780] **Speaker 1:** Asking to go from here to here, um, well, like
[00:50:16:780 - 00:50:19:949] **Speaker 0:** in previous examples there's always a d2 over DX and
[00:50:19:949 - 00:50:23:909] **Speaker 0:** that then always goes to minus detailed over the x
[00:50:23:909 - 00:50:24:870] **Speaker 0:** x1 plus.
[00:50:28:429 - 00:50:30:389] **Speaker 1:** I mean, in, in general, I want you to go
[00:50:30:389 - 00:50:32:489] **Speaker 1:** through each step and show the working.
[00:50:33:060 - 00:50:36:340] **Speaker 1:** Um, the question might might not be with the same
[00:50:36:340 - 00:50:38:989] **Speaker 1:** terms, so you should understand what's happening at each step
[00:50:39:350 - 00:50:41:110] **Speaker 1:** because what happens if you've got a variable source term,
[00:50:41:590 - 00:50:42:860] **Speaker 1:** you're integrating something different.
[00:50:43:110 - 00:50:45:530] **Speaker 1:** What if you've got a first order derivative and things
[00:50:45:530 - 00:50:45:830] **Speaker 1:** like that.
[00:50:45:949 - 00:50:50:790] **Speaker 1:** So it's safest to, to work through each step, and
[00:50:50:909 - 00:50:53:270] **Speaker 1:** I will go through the instructions for the exam later,
[00:50:53:310 - 00:50:56:379] **Speaker 1:** but Show all working and things like that, so you
[00:50:56:379 - 00:50:57:699] **Speaker 1:** might not get full credit if you just put the
[00:50:57:699 - 00:50:58:820] **Speaker 1:** answer, um.
[00:50:59:620 - 00:51:02:360] **Speaker 1:** It's like, yeah, here's a guess, this might be right,
[00:51:02:570 - 00:51:05:010] **Speaker 1:** but as engineers, we want to show that we know
[00:51:05:010 - 00:51:05:989] **Speaker 1:** what we're doing, hopefully.
[00:51:07:719 - 00:51:11:409] **Speaker 1:** Not just relying on random outputs, with any luck.
[00:51:12:689 - 00:51:13:820] **Speaker 1:** Any other questions?
[00:51:18:590 - 00:51:21:270] **Speaker 1:** Awesome, alright, well, well have a good weekend, maybe start
[00:51:21:270 - 00:51:24:110] **Speaker 1:** your assignment if you haven't, and we'll see you on
[00:51:24:389 - 00:51:24:830] **Speaker 1:** Monday.
[00:51:54:189 - 00:51:54:469] **Speaker 1:** No worries.
[00:52:00:919 - 00:52:00:929] **Speaker 0:** now.
[00:52:14:639 - 00:52:34:080] **Speaker 0:** I Who?
[00:52:37:070 - 00:54:06:350] **Speaker 0:** No, I Right trust up.
[00:54:07:770 - 00:54:08:270] **Speaker 0:** But I

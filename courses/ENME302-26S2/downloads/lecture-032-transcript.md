# ENME302-26S2 Lecture 32 native Echo transcript

Date: September 18, 2026 11:00am-11:55am
Transcript type: native Echo automated transcript.

[00:00:03:849 - 00:00:23:319] **Speaker 0:** No I I Right.
[00:00:26:559 - 00:00:26:569] **Speaker 0:** I.
[00:00:36:319 - 00:00:36:330] **Speaker 0:** Yeah.
[00:00:39:490 - 00:00:40:299] **Speaker 1:** Uh, we'll make a start.
[00:00:40:419 - 00:00:43:099] **Speaker 1:** Any questions before we dive back into chapter 6?
[00:00:46:349 - 00:00:54:919] **Speaker 0:** Oh There's a query uh by email with the quiz,
[00:00:55:020 - 00:00:58:340] **Speaker 1:** so instead of having, um, the units just by themselves,
[00:00:58:680 - 00:01:01:759] **Speaker 1:** remember to, well, remember to not include the square brackets.
[00:01:01:840 - 00:01:04:279] **Speaker 1:** So in console we use square brackets to denote units.
[00:01:04:440 - 00:01:07:040] **Speaker 1:** Uh, in the quiz it's just times the unit, so
[00:01:07:040 - 00:01:08:699] **Speaker 1:** times M for being in metres.
[00:01:09:160 - 00:01:12:540] **Speaker 1:** Uh, I've gone through and checked all of the incorrect
[00:01:12:879 - 00:01:13:470] **Speaker 1:** responses so far.
[00:01:13:480 - 00:01:16:239] **Speaker 1:** I spotted maybe 2 or 3 who, who were marked
[00:01:16:239 - 00:01:17:349] **Speaker 1:** down for that.
[00:01:17:599 - 00:01:19:879] **Speaker 1:** I gave them, uh, 75, well, took off half the
[00:01:19:879 - 00:01:21:800] **Speaker 1:** mark, um, for that.
[00:01:22:690 - 00:01:25:930] **Speaker 1:** Exciting stuff, um, but I guess just recapping that, yeah,
[00:01:26:010 - 00:01:30:569] **Speaker 1:** units are really important, so, um, I didn't, It's the
[00:01:30:569 - 00:01:34:900] **Speaker 1:** stack quiz type is checking for the value as well
[00:01:34:900 - 00:01:35:629] **Speaker 1:** as the units.
[00:01:36:029 - 00:01:37:910] **Speaker 1:** So if you put the right number and then put
[00:01:37:910 - 00:01:41:129] **Speaker 1:** like pascales instead of mega pascales, obviously that's 106 out,
[00:01:41:389 - 00:01:42:849] **Speaker 1:** so that shouldn't be marked right.
[00:01:43:230 - 00:01:43:809] **Speaker 1:** Um.
[00:01:44:669 - 00:01:46:989] **Speaker 1:** So yeah, just be careful when you're including units and
[00:01:46:989 - 00:01:49:269] **Speaker 1:** then uh more of a time pressured environment like an
[00:01:49:269 - 00:01:51:550] **Speaker 1:** exam would give you partial credit for, for having a
[00:01:51:550 - 00:01:52:069] **Speaker 1:** great value.
[00:01:54:239 - 00:01:54:800] **Speaker 1:** All right.
[00:01:59:080 - 00:02:00:730] **Speaker 1:** So yesterday we were going through.
[00:02:01:589 - 00:02:03:730] **Speaker 1:** Our heat equation and we're solving it.
[00:02:04:889 - 00:02:05:889] **Speaker 1:** With a couple of schemes.
[00:02:06:050 - 00:02:08:809] **Speaker 1:** We looked at the fully explicit scheme and then an
[00:02:08:809 - 00:02:09:990] **Speaker 1:** implicit scheme as well.
[00:02:10:839 - 00:02:11:720] **Speaker 1:** Making a mess.
[00:02:12:889 - 00:02:16:830] **Speaker 1:** Um, so the explicit method was evaluating the temperature profile
[00:02:17:009 - 00:02:20:729] **Speaker 1:** only on the previous, uh, time steps, and the implicit
[00:02:20:729 - 00:02:22:649] **Speaker 1:** method was sort of like marching forward and using a
[00:02:22:649 - 00:02:23:449] **Speaker 1:** coupled system.
[00:02:23:800 - 00:02:25:479] **Speaker 1:** So we had a simultaneous set of equations that we
[00:02:25:479 - 00:02:26:110] **Speaker 1:** were solving.
[00:02:27:029 - 00:02:28:639] **Speaker 1:** So it's a little bit more complex, but we found
[00:02:28:639 - 00:02:30:479] **Speaker 1:** that it was unconditionally stable.
[00:02:31:399 - 00:02:34:059] **Speaker 1:** So that was a great step forward.
[00:02:34:380 - 00:02:35:889] **Speaker 1:** What we're going to do next is look at a
[00:02:36:960 - 00:02:37:820] **Speaker 1:** sort of a hybrid approach.
[00:02:37:940 - 00:02:41:619] **Speaker 1:** So taking both, uh, schemes and taking the midpoint.
[00:02:41:740 - 00:02:43:779] **Speaker 1:** So instead of the next or previous, we're taking the
[00:02:43:779 - 00:02:46:380] **Speaker 1:** midpoint and we're labelling this as the Crank Nicholson method.
[00:02:49:320 - 00:02:51:949] **Speaker 1:** So both schemes backward in time and forward in time
[00:02:51:949 - 00:02:54:220] **Speaker 1:** were first order accurate in time, so.
[00:02:55:380 - 00:02:57:600] **Speaker 1:** Uh, so what we're gonna do instead is a 2nd
[00:02:57:600 - 00:02:59:750] **Speaker 1:** order central difference scheme in time.
[00:03:01:199 - 00:03:07:089] **Speaker 1:** So our approximation for our derivatives, D2T by DX2.
[00:03:10:029 - 00:03:12:770] **Speaker 1:** Instead of evaluating them at time N or N +
[00:03:12:770 - 00:03:17:429] **Speaker 1:** 1, we're going to evaluate them at TN + 1/2.
[00:03:18:440 - 00:03:19:160] **Speaker 1:** So the midpoint.
[00:03:20:710 - 00:03:23:070] **Speaker 1:** Because at the midpoint, we're going to take half the
[00:03:23:070 - 00:03:26:509] **Speaker 1:** expression at time level N and half the expression at
[00:03:26:509 - 00:03:27:589] **Speaker 1:** time level N + 1.
[00:03:28:210 - 00:03:31:529] **Speaker 1:** So we've got a half of two reasonably large stems.
[00:03:34:190 - 00:03:41:300] **Speaker 1:** So the first term is TI minus 1-2 TI and
[00:03:41:300 - 00:03:42:440] **Speaker 1:** TI + 1.
[00:03:43:210 - 00:03:44:449] **Speaker 1:** Over Dare squad.
[00:03:46:509 - 00:03:51:139] **Speaker 1:** These are the ones Evaluator at TN, so Superscript in.
[00:03:54:190 - 00:03:56:679] **Speaker 1:** So that's the same as that uh explicit scheme.
[00:03:58:130 - 00:04:00:169] **Speaker 1:** And our second term is gonna be at the N
[00:04:00:169 - 00:04:01:690] **Speaker 1:** + 1 time set.
[00:04:01:850 - 00:04:03:309] **Speaker 1:** So DI minus 1.
[00:04:04:710 - 00:04:07:550] **Speaker 1:** DI and DI plus one.
[00:04:08:470 - 00:04:11:389] **Speaker 1:** Divided by X2 and these are evaluated the next time
[00:04:11:389 - 00:04:12:389] **Speaker 1:** level n + 1.
[00:04:18:220 - 00:04:20:730] **Speaker 1:** So instead of looking at every single index and super
[00:04:20:730 - 00:04:23:829] **Speaker 1:** um superscript subscript, uh, we can just see the pattern
[00:04:23:829 - 00:04:26:820] **Speaker 1:** is looking at the stencil of those three nodes.
[00:04:28:480 - 00:04:30:760] **Speaker 1:** I 1 + 11 minus 1.
[00:04:32:239 - 00:04:34:959] **Speaker 1:** Uh, we're applying the central difference on this set, and
[00:04:34:959 - 00:04:37:029] **Speaker 1:** then we've got it across time level TN.
[00:04:38:070 - 00:04:40:070] **Speaker 1:** And TN plus 1.
[00:04:45:489 - 00:04:53:320] **Speaker 1:** So As I drew earlier, The explicit method was using
[00:04:53:320 - 00:04:56:880] **Speaker 1:** those time level in implicit n + 1, now we're
[00:04:56:880 - 00:04:57:820] **Speaker 1:** using all 6.
[00:05:06:190 - 00:05:09:399] **Speaker 1:** So that's our discretization term for the uh spatial derivative,
[00:05:09:589 - 00:05:10:649] **Speaker 1:** second order derivative.
[00:05:11:230 - 00:05:13:269] **Speaker 1:** Now we substitute this into our heat equation.
[00:05:14:190 - 00:05:17:290] **Speaker 1:** Our heat equation was DT by T equal to alpha,
[00:05:17:589 - 00:05:19:029] **Speaker 1:** D2D by DX2.
[00:05:19:799 - 00:05:25:320] **Speaker 1:** So our time derivative still remains that one-sided difference, essentially.
[00:05:26:570 - 00:05:28:929] **Speaker 1:** So TIN plus 1.
[00:05:29:730 - 00:05:31:950] **Speaker 1:** minus TIN divided by T.
[00:05:33:589 - 00:05:36:029] **Speaker 1:** But this is also now seen as a central difference
[00:05:36:029 - 00:05:40:339] **Speaker 1:** because it's across one time step, but we're using values
[00:05:40:350 - 00:05:43:390] **Speaker 1:** from the start and end of that time step.
[00:05:43:470 - 00:05:45:149] **Speaker 1:** So it's essentially a central difference.
[00:05:45:929 - 00:05:47:549] **Speaker 1:** So we've got equal to alpha.
[00:05:48:260 - 00:05:49:290] **Speaker 1:** Our heat divisivity.
[00:05:50:149 - 00:05:52:750] **Speaker 1:** And then we're substituting in our expression for our second
[00:05:52:750 - 00:05:54:880] **Speaker 1:** order derivative E2T by DX2.
[00:05:56:579 - 00:05:59:299] **Speaker 1:** So to save my breath, I'm not gonna describe every
[00:05:59:299 - 00:05:59:500] **Speaker 1:** term.
[00:06:21:910 - 00:06:29:510] **Speaker 1:** And Now, Our spatial terms have a remainder or residual
[00:06:29:510 - 00:06:32:130] **Speaker 1:** that scales with delta X2.
[00:06:33:839 - 00:06:35:179] **Speaker 1:** And our time derivative.
[00:06:36:019 - 00:06:40:239] **Speaker 1:** Well time discretization has an order of data t2.
[00:06:41:480 - 00:06:43:559] **Speaker 1:** So it's now second order accurate in time.
[00:06:46:200 - 00:06:46:850] **Speaker 1:** Yes, we do.
[00:06:49:630 - 00:06:50:230] **Speaker 1:** Good catch.
[00:06:50:730 - 00:06:52:010] **Speaker 1:** Someone's paying attention, so that's really good.
[00:06:55:250 - 00:06:55:859] **Speaker 1:** Not me.
[00:06:56:279 - 00:07:01:640] **Speaker 1:** Alright, so we've got our discretized finite difference, central difference
[00:07:01:640 - 00:07:04:179] **Speaker 1:** or Crank Nicholson method applied to our heat equation.
[00:07:05:890 - 00:07:08:700] **Speaker 1:** And just as we did earlier for the explicit and
[00:07:08:700 - 00:07:12:209] **Speaker 1:** implicit schemes, we're going to shift all of the unknown
[00:07:12:209 - 00:07:15:049] **Speaker 1:** terms, which are at the next time level, DN +
[00:07:15:049 - 00:07:18:339] **Speaker 1:** 1 on the left-hand side, and all of the known
[00:07:18:339 - 00:07:20:730] **Speaker 1:** terms of the values that we've already calculated on the
[00:07:20:730 - 00:07:22:329] **Speaker 1:** right-hand side of the equal sign.
[00:07:24:369 - 00:07:26:769] **Speaker 1:** And we're going to label lambda again.
[00:07:28:609 - 00:07:31:329] **Speaker 1:** So on the left we've got minus lambda.
[00:07:34:070 - 00:07:38:369] **Speaker 1:** And We've got TI minus 1.
[00:07:42:329 - 00:07:43:410] **Speaker 1:** At N+1.
[00:07:45:309 - 00:07:47:989] **Speaker 1:** And then the coefficients in front of TIN + 1
[00:07:47:989 - 00:07:50:290] **Speaker 1:** is 2 times 1 plus lambda.
[00:07:53:890 - 00:07:55:309] **Speaker 1:** And we've got minus lambda.
[00:07:56:000 - 00:07:59:040] **Speaker 1:** TI + 1, N + 1.
[00:08:12:410 - 00:08:14:850] **Speaker 1:** And then the known terms of values at time level
[00:08:14:850 - 00:08:16:709] **Speaker 1:** N is on the right-hand side.
[00:08:17:290 - 00:08:18:880] **Speaker 1:** So you can maybe use that extra space.
[00:08:19:019 - 00:08:22:820] **Speaker 1:** So equal to Lambda T.
[00:08:23:649 - 00:08:26:089] **Speaker 1:** I minus 1 in.
[00:08:27:339 - 00:08:29:380] **Speaker 1:** 21 minus lambda.
[00:08:30:570 - 00:08:34:690] **Speaker 1:** TIN and lambda TI plus 1 N.
[00:08:41:750 - 00:08:44:830] **Speaker 1:** So we've got 6 nodes that we're analysing, or 3
[00:08:44:830 - 00:08:47:789] **Speaker 1:** nodes, but over 2 time steps, so 6 discrete points
[00:08:47:789 - 00:08:48:830] **Speaker 1:** in our space-time.
[00:08:50:309 - 00:08:51:989] **Speaker 1:** Space dimensions.
[00:08:52:429 - 00:08:54:109] **Speaker 1:** Uh, so we've got 6 expressions and then we've got
[00:08:54:109 - 00:08:55:989] **Speaker 1:** some coefficient coefficients in front of them.
[00:08:56:270 - 00:08:58:070] **Speaker 1:** Uh, our unknown terms are on the left, so we've
[00:08:58:070 - 00:08:58:989] **Speaker 1:** got 3 unknowns.
[00:09:02:369 - 00:09:04:679] **Speaker 1:** So this applies for all of the interior nodes.
[00:09:05:570 - 00:09:06:349] **Speaker 1:** In our domain.
[00:09:07:330 - 00:09:09:849] **Speaker 1:** And we're going to apply this to our example.
[00:09:11:469 - 00:09:14:359] **Speaker 1:** And the first equation that we're going to look at
[00:09:14:359 - 00:09:15:380] **Speaker 1:** is for I.
[00:09:16:630 - 00:09:19:280] **Speaker 1:** Equal 1, N equals 0.
[00:09:20:090 - 00:09:21:309] **Speaker 1:** It's that first time step.
[00:09:23:169 - 00:09:30:070] **Speaker 1:** We've got minus lambda, which is still 0.020875.
[00:09:33:330 - 00:09:37:940] **Speaker 1:** And at DI minus 11 minus 1, so it's T0.
[00:09:39:260 - 00:09:41:780] **Speaker 1:** Time level 0 + 1, so that's 1.
[00:09:45:070 - 00:09:48:030] **Speaker 1:** And we've got 2 x 1 plus lambda, which evaluates
[00:09:48:030 - 00:09:49:369] **Speaker 1:** to 2.04.
[00:09:50:380 - 00:09:51:750] **Speaker 1:** 175.
[00:09:53:320 - 00:09:54:909] **Speaker 1:** T1.
[00:09:55:590 - 00:09:57:229] **Speaker 1:** 1 minus.
[00:09:59:359 - 00:10:03:070] **Speaker 1:** Lambda, 0.020875 T.
[00:10:04:239 - 00:10:18:500] **Speaker 1:** 21 And on the right, we've got lambda again, 0.020875.
[00:10:20:270 - 00:10:24:070] **Speaker 1:** TI minus 1, so that's gonna be T00.
[00:10:24:989 - 00:10:30:539] **Speaker 1:** Linus Not us Uh, 2 times 1 minus lambda, which
[00:10:30:549 - 00:10:32:539] **Speaker 1:** is calculated as 1.9.
[00:10:34:440 - 00:10:35:679] **Speaker 1:** 58.
[00:10:37:570 - 00:10:38:679] **Speaker 1:** 75.
[00:10:39:960 - 00:10:41:260] **Speaker 1:** And I.
[00:10:42:380 - 00:10:43:479] **Speaker 1:** Time step 0.
[00:10:45:369 - 00:10:50:320] **Speaker 1:** Plus the lambda, 0.020875 T2.
[00:10:57:750 - 00:11:00:989] **Speaker 1:** So of these values which are already known, that we
[00:11:00:989 - 00:11:02:429] **Speaker 1:** should shift on the right hand side.
[00:11:17:630 - 00:11:18:510] **Speaker 1:** D1, that's right.
[00:11:19:030 - 00:11:21:270] **Speaker 1:** So if you think, go back to page 53.
[00:11:22:469 - 00:11:25:549] **Speaker 1:** This is our discrete space, and we're looking at node
[00:11:25:549 - 00:11:25:869] **Speaker 1:** one.
[00:11:26:979 - 00:11:29:830] **Speaker 1:** And this node is the boundary condition, so it's Derek,
[00:11:30:099 - 00:11:32:520] **Speaker 1:** so we already know that's set to 100 degrees.
[00:11:41:330 - 00:11:43:229] **Speaker 1:** Um, so it's 100.
[00:11:44:070 - 00:11:47:150] **Speaker 1:** T11 and T21 are unknown.
[00:11:47:320 - 00:11:48:469] **Speaker 1:** That's what we're going to try and calculate.
[00:11:49:140 - 00:11:51:630] **Speaker 1:** The right-hand side have values as well.
[00:11:51:830 - 00:11:53:469] **Speaker 1:** So T00 is also 100.
[00:11:54:549 - 00:12:00:349] **Speaker 1:** T10 and T20 are the initial conditions for the temperature
[00:12:00:349 - 00:12:02:469] **Speaker 1:** profile within the rod, which we said was equal to
[00:12:02:469 - 00:12:02:909] **Speaker 1:** zero.
[00:12:07:059 - 00:12:21:849] **Speaker 1:** So we can rewrite this as 2.04175 D11 minus, 0.020875
[00:12:21:849 - 00:12:22:020] **Speaker 1:** T.
[00:12:22:210 - 00:12:22:820] **Speaker 1:** 21.
[00:12:23:669 - 00:12:25:510] **Speaker 1:** So those are the only unknowns now, we've got 2
[00:12:25:510 - 00:12:26:929] **Speaker 1:** unknown variables.
[00:12:27:679 - 00:12:31:260] **Speaker 1:** And the right-hand side we can calculate is 4.175.
[00:12:34:210 - 00:12:37:650] **Speaker 1:** So we've applied the Crank Nicholson scheme for that first
[00:12:37:650 - 00:12:40:169] **Speaker 1:** node, we can do the same for the other 3.
[00:12:46:539 - 00:12:49:010] **Speaker 1:** And we save everyone by typing it out, right?
[00:12:52:559 - 00:12:53:919] **Speaker 1:** Hopefully that's reasonably straightforward.
[00:12:54:359 - 00:12:57:400] **Speaker 1:** These cases, the interior nodes we've got 3 unknowns because
[00:12:57:400 - 00:12:59:719] **Speaker 1:** it's not including the boundary condition and that last node
[00:12:59:719 - 00:13:02:280] **Speaker 1:** on the right includes the right-hand boundary condition.
[00:13:03:700 - 00:13:05:140] **Speaker 1:** Which I think was equal to 50.
[00:13:06:030 - 00:13:06:320] **Speaker 1:** Yeah.
[00:13:12:530 - 00:13:14:809] **Speaker 1:** Has everyone followed up to here or anyone's got any
[00:13:14:809 - 00:13:16:770] **Speaker 1:** questions on how we got to this set of equations?
[00:13:16:809 - 00:13:19:690] **Speaker 1:** We've got 4 equations and 4 unknowns.
[00:13:22:989 - 00:13:24:669] **Speaker 1:** All sort of straightforward or?
[00:13:26:890 - 00:13:28:059] **Speaker 1:** Yep, straightforward, that's good.
[00:13:28:330 - 00:13:31:570] **Speaker 1:** Alright, so we've got 4 equations, uh, 4 and 9s,
[00:13:31:609 - 00:13:33:609] **Speaker 1:** we're gonna put them in matrix form and solve.
[00:13:34:929 - 00:13:37:619] **Speaker 1:** So again, we label this maybe A, uh, we've got
[00:13:37:619 - 00:13:42:270] **Speaker 1:** a temperature vector field, um, or variable T and right-hand
[00:13:42:270 - 00:13:42:979] **Speaker 1:** side B.
[00:13:46:330 - 00:13:50:169] **Speaker 1:** So we can solve this equation set uh with whatever
[00:13:50:169 - 00:13:50:929] **Speaker 1:** method you want to use.
[00:13:51:049 - 00:13:53:729] **Speaker 1:** So Lieben method or you could use uh some sort
[00:13:53:729 - 00:13:57:669] **Speaker 1:** of direct solve by finding the inverse matrix of coefficients
[00:13:57:669 - 00:13:58:020] **Speaker 1:** a.
[00:14:00:369 - 00:14:02:489] **Speaker 1:** And we find that the temperature values.
[00:14:03:679 - 00:14:07:640] **Speaker 1:** At 0.1 seconds, so after delta t equals 0.1 seconds,
[00:14:07:719 - 00:14:09:500] **Speaker 1:** we have T1 of 2.
[00:14:10:659 - 00:14:13:440] **Speaker 1:** 0.02, 0.01, and 1.
[00:14:13:900 - 00:14:16:960] **Speaker 1:** So how do these differ from our earlier calculations?
[00:14:18:219 - 00:14:24:330] **Speaker 1:** Um So the Somewhat similar to our one on page
[00:14:24:330 - 00:14:24:799] **Speaker 1:** 56.
[00:14:24:849 - 00:14:26:169] **Speaker 1:** So this was from the Implicit scheme.
[00:14:29:039 - 00:14:30:260] **Speaker 1:** 002.
[00:14:31:890 - 00:14:32:570] **Speaker 1:** And 2.
[00:14:38:359 - 00:14:41:880] **Speaker 1:** And we can continue through and solve for that temperature
[00:14:41:880 - 00:14:43:080] **Speaker 1:** distribution over time.
[00:14:44:349 - 00:14:46:989] **Speaker 1:** And the right-hand side of the vector will be updated
[00:14:46:989 - 00:14:50:090] **Speaker 1:** for each time set because it depends on the values
[00:14:50:260 - 00:14:51:309] **Speaker 1:** of the temperature field.
[00:14:51:869 - 00:14:54:950] **Speaker 1:** So B vector for our next time set.
[00:14:55:849 - 00:14:56:969] **Speaker 1:** Has these values.
[00:14:57:429 - 00:15:03:549] **Speaker 1:** Again, the matrix A of coefficients doesn't change between timestamps.
[00:15:04:510 - 00:15:06:520] **Speaker 1:** So we looked at the structure of this yesterday for
[00:15:06:520 - 00:15:07:520] **Speaker 1:** the implicit scheme.
[00:15:10:830 - 00:15:14:609] **Speaker 1:** Well, what we've got is 2 x 1 plus lambda
[00:15:15:090 - 00:15:17:070] **Speaker 1:** minus lambda and minus lambda.
[00:15:20:280 - 00:15:22:479] **Speaker 1:** Does anyone remember what we define lambda as?
[00:15:27:309 - 00:15:30:669] **Speaker 1:** Alpha Delta 2 over X2.
[00:15:33:559 - 00:15:36:190] **Speaker 1:** So if we have a constant time step, T, constant
[00:15:36:190 - 00:15:39:830] **Speaker 1:** spatial grid sizing, X, and heat divity alpha, it's not
[00:15:39:830 - 00:15:40:869] **Speaker 1:** gonna be changing over time.
[00:15:43:190 - 00:15:45:630] **Speaker 1:** So the advantage here is that we don't have to
[00:15:45:630 - 00:15:48:409] **Speaker 1:** evaluate the inverse of that matrix of coefficients every time
[00:15:48:409 - 00:15:50:469] **Speaker 1:** step if we wish to use a direct solve.
[00:15:55:859 - 00:15:56:179] **Speaker 1:** All right.
[00:15:56:380 - 00:15:58:570] **Speaker 1:** So just to summarise some of what we've been looking
[00:15:58:570 - 00:16:01:179] **Speaker 1:** at, we're going to do a performance comparison against these
[00:16:01:179 - 00:16:01:929] **Speaker 1:** three schemes.
[00:16:02:500 - 00:16:06:340] **Speaker 1:** We have the explicit and implicit schemes, which are 1st
[00:16:06:340 - 00:16:09:820] **Speaker 1:** order accurate, and this rank Nicholson scheme, which is 2nd
[00:16:09:820 - 00:16:10:520] **Speaker 1:** order accurate.
[00:16:11:489 - 00:16:13:330] **Speaker 1:** Uh, there's heaps of other schemes as well.
[00:16:13:530 - 00:16:16:270] **Speaker 1:** Uh, we're just touching on these because they're reasonably, uh,
[00:16:16:280 - 00:16:17:849] **Speaker 1:** straightforward to implement and understand.
[00:16:18:619 - 00:16:20:880] **Speaker 1:** We're gonna look at the problem that we studied earlier
[00:16:21:210 - 00:16:23:419] **Speaker 1:** with a laterally insulated copper bar.
[00:16:23:539 - 00:16:25:979] **Speaker 1:** So laterally insulated means that it's not gonna have temperature
[00:16:25:979 - 00:16:30:380] **Speaker 1:** varying in the um Perpendicular direction, so it's just one
[00:16:30:380 - 00:16:31:000] **Speaker 1:** dimensional.
[00:16:31:750 - 00:16:34:340] **Speaker 1:** And we've got a copper bar of 80 centimetres length
[00:16:34:640 - 00:16:38:400] **Speaker 1:** and an initial profile of 100 sign pikes over 80.
[00:16:39:369 - 00:16:41:440] **Speaker 1:** So we're going to solve this with our three schemes
[00:16:41:739 - 00:16:44:500] **Speaker 1:** and estimate the error in the centre of the rod
[00:16:44:739 - 00:16:46:880] **Speaker 1:** at some time, so 100 seconds.
[00:16:47:820 - 00:16:50:640] **Speaker 1:** And we've got some spacing prescribed of 8 centimetres.
[00:17:18:910 - 00:17:21:329] **Speaker 1:** So these are in chapter 6, you can follow along
[00:17:21:430 - 00:17:23:949] **Speaker 1:** as well uh with the code.
[00:17:25:400 - 00:17:29:300] **Speaker 1:** Um, but we looked at explicit already and the implicit
[00:17:29:300 - 00:17:29:800] **Speaker 1:** scheme.
[00:17:33:109 - 00:17:33:959] **Speaker 1:** Uh, it's very similar.
[00:17:34:030 - 00:17:36:339] **Speaker 1:** We have to set up this matrix of coefficients A.
[00:17:37:430 - 00:17:39:800] **Speaker 1:** Um, and I've included the Crack Nicholson as an option
[00:17:39:800 - 00:17:43:420] **Speaker 1:** in this code, so we can do a Vus and
[00:17:43:420 - 00:17:43:739] **Speaker 1:** then.
[00:17:45:589 - 00:17:46:410] **Speaker 1:** Yeah, why that?
[00:17:47:400 - 00:18:00:189] **Speaker 1:** It's here, but So We can toggle Euler and Crack
[00:18:00:189 - 00:18:04:589] **Speaker 1:** Nicholson with a simple boolean operator or variable and solve
[00:18:04:589 - 00:18:05:369] **Speaker 1:** that system.
[00:18:05:790 - 00:18:08:750] **Speaker 1:** So we can just hit play if we want.
[00:18:08:989 - 00:18:13:430] **Speaker 1:** So that should be doing the Euler method, Oer implicit.
[00:18:14:369 - 00:18:16:369] **Speaker 1:** And we can see that even though we've got a
[00:18:16:369 - 00:18:19:609] **Speaker 1:** very large time step, so we saw yesterday that the
[00:18:19:609 - 00:18:21:959] **Speaker 1:** explicit scheme broke down when we had a time step
[00:18:21:959 - 00:18:22:760] **Speaker 1:** of 5 seconds.
[00:18:23:010 - 00:18:25:189] **Speaker 1:** We can see that this has converged still to the
[00:18:25:310 - 00:18:29:790] **Speaker 1:** steady state, that linear profile between the two boundary conditions
[00:18:29:810 - 00:18:31:329] **Speaker 1:** ranging from 100 down to 50.
[00:18:32:119 - 00:18:34:739] **Speaker 1:** And if we use the Crank Nicholson method as well.
[00:18:43:380 - 00:18:47:180] **Speaker 1:** It'll still converge to that same final temperature profile.
[00:18:48:410 - 00:18:49:130] **Speaker 1:** All right.
[00:18:49:530 - 00:18:54:130] **Speaker 1:** So I want to show you uh this benchmark case.
[00:18:56:290 - 00:18:58:530] **Speaker 1:** This is also on learn if you want to uh
[00:18:58:530 - 00:18:59:729] **Speaker 1:** open it up in your own time.
[00:19:00:050 - 00:19:03:689] **Speaker 1:** So this is evaluating with our analytical solution that we
[00:19:03:689 - 00:19:06:569] **Speaker 1:** looked at in class at some time.
[00:19:06:689 - 00:19:07:969] **Speaker 1:** So in this case, we're just looking at T equal
[00:19:07:969 - 00:19:13:640] **Speaker 1:** 10 seconds and at Uh, 0.02, so 64.8 degrees.
[00:19:15:520 - 00:19:20:160] **Speaker 1:** And Lambda is our expression that we discussed earlier.
[00:19:20:540 - 00:19:24:050] **Speaker 1:** So alphaDeltaT over X2 and this dictates whether or not
[00:19:24:050 - 00:19:26:069] **Speaker 1:** the explicit method is stable.
[00:19:26:589 - 00:19:29:869] **Speaker 1:** So for higher lambda values that were greater than 5,
[00:19:30:390 - 00:19:32:890] **Speaker 1:** we saw that it was unstable.
[00:19:34:369 - 00:19:36:930] **Speaker 1:** So we've got values that don't make sense, that are
[00:19:36:930 - 00:19:38:849] **Speaker 1:** outside of the boundary conditions of 50 and 100.
[00:19:39:859 - 00:19:42:420] **Speaker 1:** And as we refine the uh mesh.
[00:19:43:380 - 00:19:46:219] **Speaker 1:** We converge to about 64.9, which is close to the
[00:19:46:219 - 00:19:48:939] **Speaker 1:** analytical solution and then we can look at also the
[00:19:48:939 - 00:19:49:680] **Speaker 1:** implicit scheme.
[00:19:50:920 - 00:19:53:800] **Speaker 1:** This is unconditionally stable, but it's still inaccurate for the
[00:19:53:800 - 00:19:55:959] **Speaker 1:** high time steps.
[00:19:57:569 - 00:20:02:050] **Speaker 1:** And the Crank Nicholson method converges in time steps much
[00:20:02:050 - 00:20:03:699] **Speaker 1:** quicker than the implicit scheme.
[00:20:03:770 - 00:20:05:890] **Speaker 1:** So you can see here that it goes quickly to
[00:20:05:890 - 00:20:09:920] **Speaker 1:** 64.8 for very coarse time steps.
[00:20:09:969 - 00:20:14:369] **Speaker 1:** So again, comparing linear versus quadratic accuracy.
[00:20:17:229 - 00:20:17:819] **Speaker 1:** All right.
[00:20:25:239 - 00:20:30:040] **Speaker 1:** So any questions on Our finite fencing for time dependent
[00:20:30:040 - 00:20:30:640] **Speaker 1:** problems.
[00:20:32:550 - 00:20:32:869] **Speaker 1:** No.
[00:20:38:530 - 00:20:40:339] **Speaker 1:** So I'll give you something to do to keep you
[00:20:40:339 - 00:20:40:829] **Speaker 1:** awake.
[00:20:41:640 - 00:20:45:949] **Speaker 1:** Um, So we can do question 2, I think with
[00:20:45:949 - 00:20:47:089] **Speaker 1:** pen and paper pretty well.
[00:20:47:709 - 00:20:53:420] **Speaker 1:** So, This problem is a chemical engineering manufacturing, uh, system
[00:20:53:420 - 00:20:53:829] **Speaker 1:** related.
[00:20:54:189 - 00:20:57:150] **Speaker 1:** So we've got some process of diffusion of salt into
[00:20:57:150 - 00:20:57:910] **Speaker 1:** a layer of water.
[00:20:58:660 - 00:21:01:500] **Speaker 1:** Uh, the layer has a thickness of L.
[00:21:02:910 - 00:21:06:739] **Speaker 1:** And has a uniform concentration of salt equal to C0.
[00:21:08:079 - 00:21:11:010] **Speaker 1:** At some time T0, uh, the layer is brought into
[00:21:11:010 - 00:21:12:680] **Speaker 1:** contact with some saline solution.
[00:21:13:000 - 00:21:15:650] **Speaker 1:** So we've got some concentration that changes to CS.
[00:21:17:699 - 00:21:20:260] **Speaker 1:** And the other surface is maintained at some concentration, so
[00:21:20:260 - 00:21:20:640] **Speaker 1:** you know.
[00:21:22:599 - 00:21:23:780] **Speaker 1:** So the mass divisivity.
[00:21:25:199 - 00:21:28:430] **Speaker 1:** Also known as the diffusion coefficient, uh, is going to
[00:21:28:430 - 00:21:29:319] **Speaker 1:** be given by D.
[00:21:29:800 - 00:21:32:400] **Speaker 1:** So what we just, we derived the heat equation and
[00:21:32:400 - 00:21:36:000] **Speaker 1:** we use the heat diffusivity to be a measure of
[00:21:36:000 - 00:21:38:930] **Speaker 1:** how quickly the heat dissipates or diffuses through the domain.
[00:21:39:319 - 00:21:42:839] **Speaker 1:** This problem is analogous and we've got a diffusion coefficient
[00:21:43:010 - 00:21:45:160] **Speaker 1:** describing the mass diffusivity.
[00:21:46:479 - 00:21:47:760] **Speaker 1:** So you can see here that we've got the same
[00:21:47:760 - 00:21:50:020] **Speaker 1:** form of equation, even though it's quite a different application.
[00:21:50:599 - 00:21:52:520] **Speaker 1:** We've got concentration varying instead of temperature.
[00:21:53:290 - 00:21:56:390] **Speaker 1:** And our governing PDE for this equation is, is our,
[00:21:56:689 - 00:22:00:609] **Speaker 1:** um, essentially heat equation, and X is our coordinate from
[00:22:00:609 - 00:22:01:310] **Speaker 1:** the surface.
[00:22:02:489 - 00:22:06:369] **Speaker 1:** And we've got these, uh, boundary and initial conditions and
[00:22:06:369 - 00:22:07:170] **Speaker 1:** our heat equation.
[00:22:08:060 - 00:22:09:060] **Speaker 1:** Or diffusion equation.
[00:22:10:209 - 00:22:12:500] **Speaker 1:** So the first step is to non-dimensionalize this equation, and
[00:22:12:500 - 00:22:14:439] **Speaker 1:** I've given you these uh variables that we want to
[00:22:14:439 - 00:22:15:459] **Speaker 1:** scale against.
[00:22:15:699 - 00:22:17:579] **Speaker 1:** So L being the characteristic length.
[00:22:18:619 - 00:22:22:119] **Speaker 1:** And our concentration varies between C0 and CS.
[00:22:22:540 - 00:22:25:660] **Speaker 1:** So we're gonna normalise on this interval CS and C0.
[00:22:29:010 - 00:22:33:050] **Speaker 1:** So we non-dimensionalize the heat equation in lectures, uh, and
[00:22:33:290 - 00:22:36:650] **Speaker 1:** I'd like you to do this for our concentration profile.
[00:24:00:560 - 00:24:03:349] **Speaker 1:** So I guess in terms of interpreting things, equations are
[00:24:03:349 - 00:24:07:060] **Speaker 1:** much easier to consider than a block of text, um,
[00:24:07:069 - 00:24:09:750] **Speaker 1:** but hopefully you can see where we've come and arrived
[00:24:09:750 - 00:24:12:750] **Speaker 1:** at these equations based on what we've been prescribed.
[00:24:14:280 - 00:24:17:719] **Speaker 1:** So It might be helpful to try and visualise what
[00:24:17:719 - 00:24:18:469] **Speaker 1:** this looks like.
[00:24:18:770 - 00:24:22:569] **Speaker 1:** So we've got some distance from 0 up to L.
[00:24:27:140 - 00:24:32:400] **Speaker 1:** And the initial concentration profile at time 0 is C0.
[00:24:38:880 - 00:24:41:479] **Speaker 1:** And the concentration on the left-hand side is equal to
[00:24:41:479 - 00:24:42:180] **Speaker 1:** CS.
[00:24:44:069 - 00:24:45:430] **Speaker 1:** And on the right, we've got C naught.
[00:24:51:579 - 00:24:53:680] **Speaker 1:** And we've been asked to non-dimensionalize this equation.
[00:24:53:750 - 00:24:55:300] **Speaker 1:** So what's the first step here?
[00:24:56:140 - 00:24:57:530] **Speaker 1:** If we look on the left-hand side.
[00:25:20:670 - 00:25:24:469] **Speaker 1:** So at the moment, C, T, D, X all have
[00:25:24:469 - 00:25:28:150] **Speaker 1:** units, and our goal here is to non-dimensionalize this equation.
[00:25:28:219 - 00:25:31:089] **Speaker 1:** So we want to swap out the variables with units
[00:25:31:619 - 00:25:35:069] **Speaker 1:** or with dimensions with variables that don't have the dimensions
[00:25:35:069 - 00:25:35:790] **Speaker 1:** or units.
[00:25:40:569 - 00:25:42:790] **Speaker 1:** So we can rearrange our.
[00:25:44:660 - 00:25:46:939] **Speaker 1:** C Tilda, to be C equal to.
[00:25:48:140 - 00:25:52:819] **Speaker 1:** CS minus C0, C plus C.
[00:25:54:760 - 00:25:55:530] **Speaker 1:** You can't see that.
[00:26:02:339 - 00:26:04:939] **Speaker 1:** And substitute this into our derivative.
[00:26:08:369 - 00:26:09:869] **Speaker 1:** So we're gonna be left with D.
[00:26:10:810 - 00:26:18:640] **Speaker 1:** IDT so um derivative of C0 plus.
[00:26:20:050 - 00:26:21:650] **Speaker 1:** CS minus C.
[00:26:23:589 - 00:26:39:949] **Speaker 1:** Time he told her Caught CS are both just constant
[00:26:39:949 - 00:26:40:359] **Speaker 1:** values.
[00:26:40:560 - 00:26:42:709] **Speaker 1:** These are our boundaries or initial conditions.
[00:26:45:180 - 00:26:47:599] **Speaker 1:** So we can break up this derivative and we've got
[00:26:47:599 - 00:26:48:900] **Speaker 1:** DC0 by DT.
[00:26:52:739 - 00:26:59:670] **Speaker 1:** Plus DYDT of CS minus C0, C.
[00:27:13:569 - 00:27:14:609] **Speaker 1:** What's the next step?
[00:27:21:050 - 00:27:22:439] **Speaker 1:** What is DC IDT?
[00:27:22:479 - 00:27:25:400] **Speaker 1:** If we have a constant value and we differentiate with
[00:27:25:400 - 00:27:26:180] **Speaker 1:** respect to time.
[00:27:27:869 - 00:27:28:479] **Speaker 1:** 0, yep.
[00:27:30:410 - 00:27:32:689] **Speaker 1:** And what can we do with this 2nd term?
[00:27:34:449 - 00:27:34:689] **Speaker 1:** Yep.
[00:27:35:579 - 00:27:39:630] **Speaker 1:** So we're left with CS minus C0 multiplied by DC
[00:27:39:630 - 00:27:41:140] **Speaker 1:** tilda by DT.
[00:27:42:050 - 00:27:43:790] **Speaker 1:** Is this expression dimensionless?
[00:27:48:010 - 00:27:50:719] **Speaker 1:** Part of it is, so C tilda is what CS
[00:27:50:719 - 00:27:52:969] **Speaker 1:** and C0 will have units of whatever the concentration field
[00:27:52:969 - 00:27:56:050] **Speaker 1:** is, moles per metre cubed or kilogrammes per metre cubed
[00:27:56:050 - 00:27:56:500] **Speaker 1:** or whatever.
[00:27:57:930 - 00:27:59:560] **Speaker 1:** And T is still in time.
[00:27:59:890 - 00:28:01:369] **Speaker 1:** We've still got units of time.
[00:28:04:630 - 00:28:06:310] **Speaker 1:** So I guess the first step would be to try
[00:28:06:310 - 00:28:10:150] **Speaker 1:** and non-dimensionalize the derivative that we're differentiating against for that
[00:28:10:150 - 00:28:10:540] **Speaker 1:** time.
[00:28:10:839 - 00:28:13:489] **Speaker 1:** Does anyone remember what math tool we used for this?
[00:28:15:589 - 00:28:16:329] **Speaker 1:** General, that's right.
[00:28:17:689 - 00:28:22:099] **Speaker 1:** So we've got CS minus C0 and it'll be D.
[00:28:24:339 - 00:28:26:939] **Speaker 1:** See Toda by DT Toda.
[00:28:27:739 - 00:28:29:699] **Speaker 1:** And the.
[00:28:31:160 - 00:28:33:760] **Speaker 1:** T Tilda Y DT.
[00:28:34:359 - 00:28:36:000] **Speaker 1:** So the partial derivatives.
[00:28:36:650 - 00:28:40:150] **Speaker 1:** For the C tilter and T tilter because our concentration
[00:28:40:150 - 00:28:43:430] **Speaker 1:** field is varying in space and time, it's got two
[00:28:44:170 - 00:28:45:089] **Speaker 1:** independent variables.
[00:28:47:239 - 00:28:50:219] **Speaker 1:** Our time dimension is time we define.
[00:28:51:430 - 00:28:53:390] **Speaker 1:** With our expression DT over L2.
[00:28:53:979 - 00:28:56:290] **Speaker 1:** This is only dependent on time T.
[00:28:57:449 - 00:28:58:750] **Speaker 1:** That's why it's a full derivative.
[00:29:07:520 - 00:29:08:030] **Speaker 1:** All right.
[00:29:08:400 - 00:29:09:719] **Speaker 1:** So we've got CS minus C.
[00:29:12:760 - 00:29:16:640] **Speaker 1:** Now, DC tilda IDT tilda is dimensionless, so we can
[00:29:16:640 - 00:29:17:219] **Speaker 1:** leave that alone.
[00:29:17:680 - 00:29:18:680] **Speaker 1:** We'll put that at the end.
[00:29:22:800 - 00:29:26:010] **Speaker 1:** And what is the tilt tilda Bariti?
[00:29:30:300 - 00:29:30:770] **Speaker 1:** Yes.
[00:29:33:079 - 00:30:01:089] **Speaker 1:** So, DT, total body DT is, You can sort of
[00:30:01:089 - 00:30:01:770] **Speaker 1:** write it as you want.
[00:30:01:939 - 00:30:05:390] **Speaker 1:** This is just getting away from making brackets, but CS
[00:30:05:390 - 00:30:09:890] **Speaker 1:** over minus C over L2 times our diffusion coefficient multiplied
[00:30:09:890 - 00:30:12:400] **Speaker 1:** by the gradient DC tilted by DT tilter.
[00:30:14:530 - 00:30:17:250] **Speaker 1:** All right Cool.
[00:30:17:329 - 00:30:18:750] **Speaker 1:** So that was the left-hand side.
[00:30:19:089 - 00:30:20:449] **Speaker 1:** Uh, next step.
[00:30:21:130 - 00:30:24:150] **Speaker 1:** So we've still got some dimension terms, but we're gonna
[00:30:24:650 - 00:30:26:569] **Speaker 1:** figure that out a bit later and group them all
[00:30:26:569 - 00:30:27:020] **Speaker 1:** together.
[00:30:27:449 - 00:30:29:329] **Speaker 1:** Uh, we want to focus on the derivatives first.
[00:30:30:510 - 00:30:32:130] **Speaker 1:** So the right hand side.
[00:30:32:920 - 00:30:35:119] **Speaker 1:** We've got a derivative in space.
[00:30:35:599 - 00:30:37:859] **Speaker 1:** So DC by DX.
[00:30:42:439 - 00:30:45:680] **Speaker 1:** And that's gonna be a very similar process, so I'll
[00:30:45:680 - 00:30:49:609] **Speaker 1:** save you a little bit of, Eric, so CS minus
[00:30:49:609 - 00:30:49:849] **Speaker 1:** C.
[00:30:51:099 - 00:30:53:290] **Speaker 1:** divided by L.
[00:30:54:760 - 00:30:57:880] **Speaker 1:** Times DC tilda by D X tilda.
[00:31:05:260 - 00:31:07:180] **Speaker 1:** We've done the same chain rule, etc.
[00:31:07:829 - 00:31:13:540] **Speaker 1:** And the 2nd order derivative D2, C5 DX2.
[00:31:15:060 - 00:31:19:469] **Speaker 1:** Is CS minus C0 over L2.
[00:31:21:390 - 00:31:24:800] **Speaker 1:** D2 C tilda 5 DX2.
[00:31:37:849 - 00:31:38:359] **Speaker 1:** All right.
[00:31:39:489 - 00:31:40:930] **Speaker 1:** So what have we done so far?
[00:31:42:390 - 00:31:44:189] **Speaker 1:** We could substitute this into our equation.
[00:31:44:550 - 00:31:49:130] **Speaker 1:** So on the left-hand side, we've got CS minus C
[00:31:49:130 - 00:31:53:699] **Speaker 1:** over L2, D DC tilda by DT tilda.
[00:31:54:729 - 00:31:57:180] **Speaker 1:** And on the right, we've got the.
[00:31:58:640 - 00:32:03:199] **Speaker 1:** Multiplied by D2, Z by DX2, which we just said
[00:32:03:199 - 00:32:06:359] **Speaker 1:** was CS minus C over L2.
[00:32:07:579 - 00:32:10:849] **Speaker 1:** D2 C tilda I D X tilda 2.
[00:32:22:949 - 00:32:25:989] **Speaker 1:** We can see these terms cancel and we're left with
[00:32:25:989 - 00:32:32:430] **Speaker 1:** DC tilda by DT tilda equal to D2 D2C tilda
[00:32:32:430 - 00:32:34:270] **Speaker 1:** by D X til 2.
[00:32:37:040 - 00:32:38:000] **Speaker 1:** So this is non-dimensional.
[00:32:38:119 - 00:32:39:439] **Speaker 1:** All the terms are dimensionless.
[00:32:39:680 - 00:32:41:859] **Speaker 1:** We've got C tilter, T tilter, X tilter.
[00:32:42:400 - 00:32:45:280] **Speaker 1:** Um, we can see that all the like parameters that
[00:32:45:280 - 00:32:49:400] **Speaker 1:** describe the diffusion rate, so D, uh, has vanished in
[00:32:49:400 - 00:32:50:660] **Speaker 1:** this dimension of space.
[00:32:52:300 - 00:32:54:949] **Speaker 1:** Which means that we could solve the problem once and
[00:32:54:949 - 00:32:58:290] **Speaker 1:** then impose it on a series of solutions that have
[00:32:58:290 - 00:32:59:709] **Speaker 1:** varying diffusivities.
[00:33:01:969 - 00:33:03:130] **Speaker 1:** By re-dimensionalizing.
[00:33:04:459 - 00:33:05:819] **Speaker 1:** That was applying.
[00:33:06:560 - 00:33:09:780] **Speaker 1:** Uh, non-dimensionalization to our governing equation.
[00:33:10:219 - 00:33:12:300] **Speaker 1:** Uh, you can do the same for the boundary conditions.
[00:33:14:349 - 00:33:16:589] **Speaker 1:** So we've got 3 or 2 boundary conditions and 1
[00:33:16:589 - 00:33:17:010] **Speaker 1:** initial.
[00:33:18:010 - 00:33:21:050] **Speaker 1:** So our first boundary condition is that X equal to
[00:33:21:050 - 00:33:21:510] **Speaker 1:** 0.
[00:33:27:150 - 00:33:27:979] **Speaker 1:** And I.
[00:33:36:839 - 00:33:42:829] **Speaker 1:** Non-dimensional one at C tilda, X tilda equals 0 T.
[00:33:45:050 - 00:33:46:280] **Speaker 1:** is equal to what?
[00:34:00:410 - 00:34:04:920] **Speaker 1:** We're non-dimensionalizing the concentration with this expression, so see Tilda.
[00:34:07:630 - 00:34:09:989] **Speaker 1:** And we've got a concentration equal to CS.
[00:34:10:148 - 00:34:15:590] **Speaker 1:** So if we substitute CS, Into our fractions, CS minus
[00:34:15:590 - 00:34:17:270] **Speaker 1:** C0 over CS minus C0.
[00:34:18:158 - 00:34:23:989] **Speaker 1:** This is equal to One.
[00:34:29:229 - 00:34:32:229] **Speaker 1:** And our concentration on the right-hand side at X equal
[00:34:32:229 - 00:34:32:549] **Speaker 1:** to L.
[00:34:34:000 - 00:34:34:760] **Speaker 1:** Is he going to see?
[00:34:35:870 - 00:34:37:158] **Speaker 1:** So see Tilda at XT.
[00:34:39:110 - 00:34:42:888] **Speaker 1:** Now Act Tilda is going to be X over L.
[00:34:43:128 - 00:34:45:080] **Speaker 1:** So we've got L over L, which is equal to
[00:34:45:080 - 00:34:45:408] **Speaker 1:** 1.
[00:34:47:689 - 00:34:53:010] **Speaker 1:** And we have C0 minus C0 over CS minus C0
[00:34:53:010 - 00:34:53:739] **Speaker 1:** equal to 0.
[00:34:55:499 - 00:34:58:658] **Speaker 1:** So a non-dimensional concentration field is just going from 0
[00:34:58:658 - 00:34:59:099] **Speaker 1:** to 1.
[00:35:06:959 - 00:35:08:179] **Speaker 1:** Lastly, our initial condition.
[00:35:10:379 - 00:35:16:209] **Speaker 1:** See Of X T equals 0, you go to C.
[00:35:18:280 - 00:35:19:929] **Speaker 1:** See Toda X toda.
[00:35:20:969 - 00:35:24:590] **Speaker 1:** T tilda equal to 0.
[00:35:26:110 - 00:35:27:879] **Speaker 1:** Is just the same as.
[00:35:29:060 - 00:35:30:820] **Speaker 1:** That boundary condition on the right, so it's equal to
[00:35:30:820 - 00:35:31:189] **Speaker 1:** 0.
[00:35:42:979 - 00:35:46:620] **Speaker 1:** Is that making sense or any, anyone stuck with those
[00:35:46:620 - 00:35:47:179] **Speaker 1:** steps?
[00:35:54:179 - 00:35:56:159] **Speaker 1:** Or don't want to admit being stuck, I don't know.
[00:36:00:500 - 00:36:02:580] **Speaker 1:** OK, so we've gone through and.
[00:36:03:570 - 00:36:06:800] **Speaker 1:** Applied our non-dimensional variables for our boundaries and our initial
[00:36:06:800 - 00:36:08:010] **Speaker 1:** condition, alright.
[00:36:09:189 - 00:36:12:280] **Speaker 1:** That's part A, part B of this question.
[00:36:15:370 - 00:36:17:010] **Speaker 1:** Oh, we didn't even look at the next page.
[00:36:17:090 - 00:36:19:510] **Speaker 1:** It shows us what the answer is, that's, that's handy.
[00:36:20:050 - 00:36:21:530] **Speaker 1:** Maybe I do that in an exam, I don't know.
[00:36:21:929 - 00:36:24:090] **Speaker 1:** Um, so the next step is to discretize the PDE
[00:36:24:370 - 00:36:27:310] **Speaker 1:** using the backward in time central in space numerical scheme.
[00:36:28:979 - 00:36:30:979] **Speaker 1:** So was that the explicit or implicit scheme?
[00:36:38:199 - 00:36:39:239] **Speaker 1:** That was our implicit scheme.
[00:36:39:360 - 00:36:45:399] **Speaker 1:** So we're gonna evaluate the temperature, um, Gradient in space
[00:36:45:399 - 00:36:47:070] **Speaker 1:** at the next time level in + 1.
[00:36:47:879 - 00:36:49:300] **Speaker 1:** So I'll give you a moment to work through that.
[00:36:52:379 - 00:36:54:699] **Speaker 1:** In this case, it's a concentration gradient instead of temperature,
[00:36:54:780 - 00:36:56:340] **Speaker 1:** but we've just swapped C with T.
[00:36:56:739 - 00:36:57:659] **Speaker 1:** So nothing too scary.
[00:38:17:540 - 00:38:20:479] **Speaker 1:** Maybe we start with the time derivatives, so.
[00:38:27:489 - 00:38:31:520] **Speaker 1:** What's our finite difference pattern or stencil structure for this
[00:38:31:520 - 00:38:32:219] **Speaker 1:** time derivative?
[00:38:49:270 - 00:38:49:280] **Speaker 1:** Yep.
[00:38:51:169 - 00:38:56:229] **Speaker 1:** So key features here is that Uh, this is a
[00:38:56:229 - 00:38:58:820] **Speaker 1:** concentration varying in time at a single point.
[00:38:59:360 - 00:39:02:550] **Speaker 1:** So we're looking at a constant spatial coordinate, which is
[00:39:02:550 - 00:39:03:780] **Speaker 1:** labelled with indexi.
[00:39:05:100 - 00:39:08:459] **Speaker 1:** Uh, we're varying the time components, so varying the, um,
[00:39:08:469 - 00:39:10:929] **Speaker 1:** concentration over time, so we're looking at N + 1
[00:39:10:929 - 00:39:11:350] **Speaker 1:** and N.
[00:39:12:379 - 00:39:14:850] **Speaker 1:** And then we're scaling by the time step out of.
[00:39:15:659 - 00:39:17:100] **Speaker 1:** So you can think of it as rise over run.
[00:39:17:889 - 00:39:19:080] **Speaker 1:** Uh, in a crude way.
[00:39:19:340 - 00:39:22:820] **Speaker 1:** We can also include the Tildas because it's dimensionless for
[00:39:22:820 - 00:39:23:360] **Speaker 1:** completeness.
[00:39:26:370 - 00:39:27:850] **Speaker 1:** And I'll give you a moment to do the 2nd
[00:39:27:850 - 00:39:28:949] **Speaker 1:** order of the river in space.
[00:40:28:219 - 00:40:33:409] **Speaker 1:** So if you're stuck with the um Find a different
[00:40:33:409 - 00:40:35:770] **Speaker 1:** format, we can just flip back to this table that's
[00:40:35:770 - 00:40:36:709] **Speaker 1:** on page 30.
[00:40:37:209 - 00:40:39:659] **Speaker 1:** So we've got a 2nd order derivative, 2nd order accuracy,
[00:40:39:689 - 00:40:41:689] **Speaker 1:** and we've got 1 point on the left, 1 point
[00:40:41:689 - 00:40:43:929] **Speaker 1:** on the right, and then minus 2 at that point.
[00:40:44:290 - 00:40:45:290] **Speaker 1:** So that's our pattern.
[00:40:47:139 - 00:40:52:389] **Speaker 1:** So I've got C At I minus 1-2 CI +
[00:40:52:389 - 00:40:57:030] **Speaker 1:** CI + 1 divided by delta X2.
[00:40:59:209 - 00:41:03:810] **Speaker 1:** What time level should we be evaluating this expression, these,
[00:41:03:889 - 00:41:04:850] **Speaker 1:** these derivatives?
[00:41:06:530 - 00:41:07:679] **Speaker 1:** In one, yeah.
[00:41:15:520 - 00:41:18:300] **Speaker 1:** And again, we're gonna include those tildas just to be
[00:41:18:639 - 00:41:19:040] **Speaker 1:** complete.
[00:41:20:229 - 00:41:24:830] **Speaker 1:** So that is the non-dimensional discretization for our scheme.
[00:41:26:520 - 00:41:28:679] **Speaker 1:** So we can combine it, I'm not gonna write it
[00:41:28:679 - 00:41:30:629] **Speaker 1:** out again, but it's just that one is equal to
[00:41:30:629 - 00:41:30:919] **Speaker 1:** that one.
[00:41:32:699 - 00:41:43:620] **Speaker 1:** Um, So This is our disc sized form.
[00:41:43:840 - 00:41:46:659] **Speaker 1:** When we want to go about coding it, we listed
[00:41:46:659 - 00:41:48:600] **Speaker 1:** all of the unknowns on the left and all the
[00:41:48:820 - 00:41:49:919] **Speaker 1:** known terms on the right.
[00:41:50:149 - 00:41:52:300] **Speaker 1:** So I'll just let you rearrange this and put all
[00:41:52:300 - 00:41:55:489] **Speaker 1:** the unknown terms on the left and all the known
[00:41:55:489 - 00:41:56:760] **Speaker 1:** terms on the right-hand side.
[00:41:57:219 - 00:41:58:820] **Speaker 1:** So that's the N + 1s on the left and
[00:41:58:820 - 00:41:59:919] **Speaker 1:** n values on the right.
[00:42:02:139 - 00:42:07:580] **Speaker 1:** So Get you to do that because then you can
[00:42:07:580 - 00:42:09:479] **Speaker 1:** figure out if you actually know what what is happening.
[00:42:10:709 - 00:42:12:570] **Speaker 1:** If you're just copying down blindly then.
[00:42:13:510 - 00:42:15:270] **Speaker 1:** I don't find that I learned very well, so.
[00:42:16:719 - 00:42:18:060] **Speaker 1:** Make sure that you give it a go.
[00:43:30:639 - 00:43:34:040] **Speaker 1:** So the only expression that isn't N + 1 is
[00:43:34:040 - 00:43:35:560] **Speaker 1:** this CIN.
[00:43:36:229 - 00:43:39:550] **Speaker 1:** Uh, so on the right-hand side, we'll just stay with
[00:43:39:550 - 00:43:39:810] **Speaker 1:** CIN.
[00:43:43:699 - 00:43:45:870] **Speaker 1:** And on the left-hand side, we've got everything else.
[00:43:45:949 - 00:43:50:270] **Speaker 1:** So I've labelled lambda as the um T tilda over
[00:43:50:270 - 00:43:51:709] **Speaker 1:** X til 2.
[00:43:54:969 - 00:43:58:120] **Speaker 1:** Similar to before, but this is essentially a non-dimensional, uh,
[00:43:58:899 - 00:43:59:300] **Speaker 1:** format.
[00:44:00:699 - 00:44:03:979] **Speaker 1:** So on the left we've got minus lambda.
[00:44:04:679 - 00:44:09:649] **Speaker 1:** So we've got delta T over X2 multiplied by C.
[00:44:11:229 - 00:44:14:399] **Speaker 1:** To the I minus 1 n + 1.
[00:44:23:040 - 00:44:25:820] **Speaker 1:** Uh, for the coefficients in front of CI.
[00:44:27:689 - 00:44:34:429] **Speaker 1:** In + 1 We have, What do we have?
[00:44:39:129 - 00:44:40:060] **Speaker 1:** 1 + 2 dda.
[00:44:42:909 - 00:44:46:050] **Speaker 1:** And then we've got minus lambda CI + 1, N
[00:44:46:050 - 00:44:46:520] **Speaker 1:** + 1.
[00:44:46:679 - 00:44:47:419] **Speaker 1:** So it's symmetric.
[00:44:48:469 - 00:44:55:350] **Speaker 1:** Right So this equation holds for all of the interior
[00:44:55:350 - 00:44:57:050] **Speaker 1:** nodes that we're analysing.
[00:44:57:620 - 00:45:01:550] **Speaker 1:** Uh, we've been given two boundary conditions, which type of
[00:45:01:550 - 00:45:02:889] **Speaker 1:** boundary conditions are these?
[00:45:04:989 - 00:45:07:790] **Speaker 1:** We, we labelled three, there was Dirk Roy, Neumann, and
[00:45:07:790 - 00:45:08:219] **Speaker 1:** Robin.
[00:45:09:560 - 00:45:11:760] **Speaker 1:** Which type of boundary condition have we got here?
[00:45:13:620 - 00:45:14:070] **Speaker 1:** Directly, yep.
[00:45:14:550 - 00:45:17:149] **Speaker 1:** So that means that it's just prescribed as these fixed
[00:45:17:149 - 00:45:18:010] **Speaker 1:** concentrations.
[00:45:18:350 - 00:45:21:310] **Speaker 1:** Uh, so this equation holds for all of the interior
[00:45:21:310 - 00:45:23:820] **Speaker 1:** nodes and then it includes the sides when we're next
[00:45:23:820 - 00:45:24:110] **Speaker 1:** to them.
[00:45:26:790 - 00:45:27:110] **Speaker 1:** Cool.
[00:45:28:010 - 00:45:31:620] **Speaker 1:** So Pat C Bit of a I guess right memory
[00:45:31:620 - 00:45:35:510] **Speaker 1:** or theory question, but what are the disadvantages and advantages
[00:45:35:510 - 00:45:38:110] **Speaker 1:** between these two schemes, the backward in time and the
[00:45:38:110 - 00:45:40:229] **Speaker 1:** forward in time, central in space?
[00:45:45:870 - 00:45:48:020] **Speaker 1:** That forward in timeline we did first, that fully explicit
[00:45:48:020 - 00:45:50:729] **Speaker 1:** scheme, what was the advantage for the, for this approach?
[00:45:52:840 - 00:45:54:520] **Speaker 1:** It was easy to implement, but we didn't have to
[00:45:54:520 - 00:45:57:100] **Speaker 1:** set up a sim simultaneous set of equations to solve,
[00:45:57:600 - 00:45:58:280] **Speaker 1:** um.
[00:45:59:120 - 00:46:01:729] **Speaker 1:** What was the disadvantage for that forward in time, central
[00:46:01:729 - 00:46:02:270] **Speaker 1:** in space?
[00:46:04:280 - 00:46:08:159] **Speaker 1:** Yeah, it was only conditionally stable, subject to small enough
[00:46:08:159 - 00:46:09:100] **Speaker 1:** lambda values.
[00:46:10:209 - 00:46:15:459] **Speaker 1:** Um, And yeah, I guess backward time central space is
[00:46:15:459 - 00:46:19:250] **Speaker 1:** sort of just the reverse of those two, giving fully,
[00:46:20:080 - 00:46:23:199] **Speaker 1:** Unconditionally stable solution.
[00:46:23:909 - 00:46:26:159] **Speaker 1:** Um, and added complexity because you're solving a set of
[00:46:26:159 - 00:46:28:120] **Speaker 1:** simultaneous equations, so.
[00:46:29:300 - 00:46:37:290] **Speaker 1:** Yeah So question one is more related to coding.
[00:46:37:489 - 00:46:39:810] **Speaker 1:** So you sort of need to do that with a
[00:46:39:810 - 00:46:40:169] **Speaker 1:** computer.
[00:46:41:689 - 00:46:43:810] **Speaker 1:** But again, we're just looking at the heat equation, it's
[00:46:43:810 - 00:46:44:669] **Speaker 1:** over some domain.
[00:46:45:550 - 00:46:47:719] **Speaker 1:** Uh, we've got an initial temperature profile prescribed with a
[00:46:47:719 - 00:46:49:469] **Speaker 1:** function that varies in X.
[00:46:50:439 - 00:46:52:899] **Speaker 1:** Uh, we've got a couple of Derick clay boundary conditions.
[00:46:53:659 - 00:46:56:689] **Speaker 1:** And we've said that the steady-state solution is this linear
[00:46:56:689 - 00:46:57:639] **Speaker 1:** temperature profile.
[00:46:58:500 - 00:47:00:739] **Speaker 1:** Uh, you can derive that by just integrating this a
[00:47:00:739 - 00:47:01:419] **Speaker 1:** couple of times.
[00:47:02:520 - 00:47:04:100] **Speaker 1:** With DT by DT equal to 0.
[00:47:05:239 - 00:47:07:750] **Speaker 1:** So here you're using the forward in time, the explicit
[00:47:07:750 - 00:47:10:840] **Speaker 1:** scheme with some parameters, and then you're going to look
[00:47:10:840 - 00:47:15:280] **Speaker 1:** at this uh this unstable case of lambda equal to
[00:47:15:280 - 00:47:16:300] **Speaker 1:** 0.55.
[00:47:17:929 - 00:47:19:370] **Speaker 1:** And then you're going to solve that same problem with
[00:47:19:370 - 00:47:22:729] **Speaker 1:** the Craig Nicholson scheme and observe the differences.
[00:47:24:739 - 00:47:25:350] **Speaker 1:** Cool.
[00:47:28:010 - 00:47:28:419] **Speaker 1:** All right.
[00:47:29:959 - 00:47:31:840] **Speaker 1:** So yeah, I guess I just wanted to spend quite
[00:47:31:840 - 00:47:33:770] **Speaker 1:** a few minutes to go through problems.
[00:47:34:199 - 00:47:36:600] **Speaker 1:** Also to remind you that there are exercises at the
[00:47:36:600 - 00:47:37:570] **Speaker 1:** end of each chapter.
[00:47:37:929 - 00:47:43:389] **Speaker 1:** I know people always forget, um, And then the assignment
[00:47:43:389 - 00:47:45:100] **Speaker 1:** hits and no one knows what to do.
[00:47:45:510 - 00:47:46:550] **Speaker 1:** So, yeah.
[00:47:47:360 - 00:47:49:959] **Speaker 1:** Uh, give the exercise a crack, and the quizzes, obviously
[00:47:49:959 - 00:47:53:010] **Speaker 1:** everyone's, well, I think 80 or 90% of the class
[00:47:53:010 - 00:47:54:310] **Speaker 1:** is doing the quizzes, so that's good.
[00:47:55:370 - 00:47:58:530] **Speaker 1:** I'm not sure about the rest, um, but that will
[00:47:58:530 - 00:48:01:050] **Speaker 1:** help for preparation for the assignment and I'll talk about
[00:48:01:050 - 00:48:04:090] **Speaker 1:** the assignment more maybe next week, um, also.
[00:48:06:719 - 00:48:06:739] **Speaker 1:** Cool.
[00:48:06:750 - 00:48:07:810] **Speaker 1:** Any last minute questions?
[00:48:08:830 - 00:48:09:909] **Speaker 1:** No, that's good.
[00:48:10:080 - 00:48:12:629] **Speaker 1:** Alright, well have a good weekend, um, hopefully you have
[00:48:12:629 - 00:48:15:010] **Speaker 1:** some time off and we'll see you next week.
[00:48:27:360 - 00:48:55:929] **Speaker 0:** No, But I.
[00:49:06:310 - 00:49:06:320] **Speaker 0:** this.
[00:49:09:159 - 00:49:09:169] **Speaker 0:** P.
[00:49:10:629 - 00:49:11:949] **Speaker 0:** Yeah Yes.
[00:49:16:469 - 00:49:16:649] **Speaker 0:** I don't know.
[00:49:20:699 - 00:49:22:429] **Speaker 0:** Is it, yes, like isn't there for.
[00:49:23:909 - 00:49:30:889] **Speaker 0:** I just, instead of doing the link out outline the
[00:49:30:889 - 00:49:31:399] **Speaker 0:** inverse the back invert and multiple.
[00:49:34:260 - 00:49:38:100] **Speaker 0:** Yeah, yeah, because obviously everybody makes, especially large ones.
[00:49:39:510 - 00:49:40:260] **Speaker 0:** you don't like.
[00:49:42:360 - 00:49:44:399] **Speaker 0:** Every time that's gonna be more expensive.
[00:49:45:500 - 00:49:46:610] **Speaker 0:** Yeah, it would be, yeah, yeah, yeah.
[00:49:48:959 - 00:49:50:429] **Speaker 1:** in terms of the problems that we look at.
[00:49:51:810 - 00:49:54:899] **Speaker 1:** A few milliseconds, but yeah, that's that's the idea.
[00:49:57:129 - 00:49:58:899] **Speaker 2:** Oh sorry, I'm a little bit confused where you got
[00:49:58:899 - 00:50:00:120] **Speaker 2:** the coefficients from.
[00:50:01:169 - 00:50:02:750] **Speaker 1:** For this one lambda, yeah, the lambda.
[00:50:02:889 - 00:50:05:330] **Speaker 1:** So I mean earlier we had the extra terminal alpha
[00:50:05:330 - 00:50:08:429] **Speaker 1:** because it was dimensional, yeah, but here we're just grouping
[00:50:08:850 - 00:50:11:889] **Speaker 1:** so delta t over delta x 2, so times in
[00:50:11:889 - 00:50:16:330] **Speaker 1:** both sides by &DeltaT and then grouping them as lambda.
[00:50:18:229 - 00:50:19:500] **Speaker 1:** So it's reasonably arbitrary.
[00:50:19:550 - 00:50:21:699] **Speaker 1:** You could still write out data t tilda over x
[00:50:21:699 - 00:50:22:669] **Speaker 1:** 2 tilda.
[00:50:22:939 - 00:50:24:250] **Speaker 1:** It's just more things to write out.
[00:50:24:550 - 00:50:26:959] **Speaker 2:** Yeah, um, so then that one would be.
[00:50:27:969 - 00:50:30:189] **Speaker 2:** And we've also swapped sides, which is a little bit.
[00:50:31:580 - 00:50:34:679] **Speaker 2:** OK, yeah, so the signs are weird, but yeah, OK,
[00:50:35:000 - 00:50:37:239] **Speaker 2:** so you're just putting both of them on one side
[00:50:37:239 - 00:50:39:169] **Speaker 2:** and that one's gone onto that side and all of
[00:50:39:169 - 00:50:41:850] **Speaker 1:** these have come onto the other side, yeah, OK, and
[00:50:41:850 - 00:50:43:389] **Speaker 2:** then C plus 1, yeah, delta 2.
[00:50:44:780 - 00:50:47:040] **Speaker 1:** OK, mainly so that we have like a diagonalally dominant
[00:50:47:439 - 00:50:49:459] **Speaker 2:** matrix, Matrix, yeah, awesome.
[00:50:49:919 - 00:50:51:020] **Speaker 2:** Yep, no, that makes sense.
[00:50:51:399 - 00:50:52:250] **Speaker 2:** Cool, thank you.
[00:53:09:250 - 00:53:09:360] **Speaker 0:** So

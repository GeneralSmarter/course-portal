# ENME302-26S2 Lecture 35 native Echo transcript

Date: September 24, 2026 10:00am-10:55am
Transcript type: native Echo automated transcript.

[00:00:01:110 - 00:00:01:120] **Speaker 0:** yourself.
[00:00:14:010 - 00:00:37:180] **Speaker 0:** I Right Oh, uh, good morning.
[00:00:37:340 - 00:00:37:939] **Speaker 1:** I'll make a start.
[00:00:37:979 - 00:00:41:299] **Speaker 1:** Are there any questions before we dive into our work?
[00:00:43:220 - 00:00:46:080] **Speaker 1:** Anyone had a try at the assignment last night?
[00:00:48:450 - 00:00:49:869] **Speaker 1:** Is the mic working?
[00:00:50:970 - 00:00:52:090] **Speaker 1:** Can you hear me at the back?
[00:00:53:250 - 00:00:57:139] **Speaker 1:** Yeah, Um, looks like the run 72 event is going
[00:00:57:139 - 00:00:58:000] **Speaker 1:** strong, so that's good.
[00:00:58:340 - 00:01:00:659] **Speaker 1:** I managed to get some laps in last night somehow.
[00:01:00:939 - 00:01:03:750] **Speaker 1:** Um, I'm not the best runner, but yeah, it's a
[00:01:03:750 - 00:01:05:018] **Speaker 1:** very motivating atmosphere.
[00:01:05:260 - 00:01:08:260] **Speaker 1:** Uh, so give it a go if you haven't yet.
[00:01:08:660 - 00:01:12:540] **Speaker 1:** Um, I suppose as a general point is that if
[00:01:12:540 - 00:01:15:089] **Speaker 1:** you're, yeah, you don't want to be always studying, um,
[00:01:15:180 - 00:01:16:180] **Speaker 1:** you want to have a little bit of a break
[00:01:16:180 - 00:01:16:750] **Speaker 1:** at times.
[00:01:17:099 - 00:01:18:940] **Speaker 1:** So make sure that you get some time to do
[00:01:18:940 - 00:01:21:620] **Speaker 1:** some exercise and, and get some fresh air.
[00:01:22:120 - 00:01:25:290] **Speaker 1:** Ah, that might become more important as the term progresses,
[00:01:25:639 - 00:01:29:059] **Speaker 1:** uh, but you might not be at your full capacity
[00:01:29:199 - 00:01:31:599] **Speaker 1:** if you're, you're tired and burnt out, so make sure
[00:01:31:599 - 00:01:35:410] **Speaker 1:** that you sleep and, And all of those good things.
[00:01:35:989 - 00:01:36:970] **Speaker 1:** Sometimes it needs to be said.
[00:01:37:389 - 00:01:38:069] **Speaker 1:** All right.
[00:01:38:470 - 00:01:42:599] **Speaker 1:** So Chapter 11, we were going through.
[00:01:43:750 - 00:01:46:269] **Speaker 1:** Uh, consistency, stability and convergence, and we just had the
[00:01:46:269 - 00:01:47:750] **Speaker 1:** last bit left over.
[00:01:47:830 - 00:01:50:230] **Speaker 1:** Are there any questions now that you've had a moment
[00:01:50:230 - 00:01:50:980] **Speaker 1:** to think about them?
[00:01:53:529 - 00:01:54:050] **Speaker 1:** No questions.
[00:01:54:139 - 00:01:54:730] **Speaker 1:** Alright, cool.
[00:01:55:089 - 00:01:58:010] **Speaker 1:** So we looked at the stability of our forward and
[00:01:58:010 - 00:02:00:290] **Speaker 1:** time centre in space scheme and we figured out that
[00:02:00:290 - 00:02:02:129] **Speaker 1:** it was dependent on lambda being less than or equal
[00:02:02:129 - 00:02:05:819] **Speaker 1:** to 5, and this was more of an intuitive approach,
[00:02:06:129 - 00:02:07:010] **Speaker 1:** physical interpretation.
[00:02:07:250 - 00:02:09:160] **Speaker 1:** We're going to look at the von Neumann stability analysis
[00:02:09:160 - 00:02:12:610] **Speaker 1:** as another tool for establishing the stability of a numerical
[00:02:12:610 - 00:02:12:929] **Speaker 1:** solution.
[00:02:15:139 - 00:02:18:070] **Speaker 1:** So we're going to use this von Neumann stability analysis
[00:02:18:070 - 00:02:20:110] **Speaker 1:** and we're gonna look at the solution error, which we
[00:02:20:110 - 00:02:23:770] **Speaker 1:** labelled epsilon IN that we defined earlier as the difference
[00:02:23:770 - 00:02:26:509] **Speaker 1:** between the final computed solution which we denoted with the
[00:02:26:509 - 00:02:30:029] **Speaker 1:** hat for those discretized terms, the hat IN and the
[00:02:30:029 - 00:02:32:860] **Speaker 1:** exact solution of the discretized equation which was just DIN.
[00:02:33:759 - 00:02:37:250] **Speaker 1:** So we're gonna rearrange Uh, the expression, so we've got
[00:02:37:250 - 00:02:41:339] **Speaker 1:** That IN equal to TIN.
[00:02:43:009 - 00:02:45:619] **Speaker 1:** Plus epsilon IN.
[00:02:46:800 - 00:02:48:779] **Speaker 1:** We see this error is the difference between the two,
[00:02:48:860 - 00:02:50:490] **Speaker 1:** we're just rearranging for the hat.
[00:02:59:050 - 00:03:00:889] **Speaker 1:** So I mean ultimately what we want to do is
[00:03:00:889 - 00:03:05:619] **Speaker 1:** try to describe our, Our error in terms of epsilons
[00:03:05:800 - 00:03:09:520] **Speaker 1:** and see how the error progresses between time steps and
[00:03:09:520 - 00:03:10:919] **Speaker 1:** see does it get bigger or smaller.
[00:03:11:080 - 00:03:11:960] **Speaker 1:** That's the end goal.
[00:03:13:000 - 00:03:15:460] **Speaker 1:** So our first step is to substitute in this, uh,
[00:03:16:039 - 00:03:19:410] **Speaker 1:** final computer solution That into our discretized equation.
[00:03:19:679 - 00:03:21:800] **Speaker 1:** So that was equation 5.
[00:03:24:970 - 00:03:25:330] **Speaker 1:** Let's go.
[00:03:26:500 - 00:03:28:279] **Speaker 1:** That's our ward in time central and space scheme.
[00:03:28:970 - 00:03:32:339] **Speaker 1:** So another quite long expression, but we've got values for
[00:03:32:339 - 00:03:33:690] **Speaker 1:** our discretized terms.
[00:03:34:020 - 00:03:34:419] **Speaker 1:** T.
[00:03:36:199 - 00:03:41:330] **Speaker 1:** B N + 1 Minus TIN divided by delta T,
[00:03:41:889 - 00:03:45:009] **Speaker 1:** so that's our time derivative using finite differencecing one-sided.
[00:03:46:009 - 00:03:51:470] **Speaker 1:** Minus alpha, TI + 1 N minus 2 TIN.
[00:03:52:339 - 00:03:56:169] **Speaker 1:** Plus TI minus 1 N divided by delta X2.
[00:03:59:740 - 00:04:04:589] **Speaker 1:** So that is the final difference of FTCS scheme for
[00:04:04:589 - 00:04:05:029] **Speaker 1:** the tea.
[00:04:06:559 - 00:04:09:559] **Speaker 1:** This terms and we have the same also.
[00:04:11:679 - 00:04:13:690] **Speaker 1:** For the epsilon, so epsilon IN.
[00:04:14:470 - 00:04:15:509] **Speaker 1:** It's the same pattern.
[00:04:16:390 - 00:04:18:308] **Speaker 1:** We're replacing Ts with epsilons.
[00:04:20:290 - 00:04:22:809] **Speaker 1:** So we've got epsilon I N + 1 minus epsilon
[00:04:22:809 - 00:04:23:200] **Speaker 1:** IN.
[00:04:24:239 - 00:04:26:119] **Speaker 1:** O T minus alpha.
[00:04:27:089 - 00:04:33:209] **Speaker 1:** Times epsiloni + 1 N minus 2, epsilon IN plus
[00:04:33:209 - 00:04:34:950] **Speaker 1:** epsilon I minus 1 N.
[00:04:35:769 - 00:04:36:649] **Speaker 1:** Oh that is good.
[00:04:38:609 - 00:04:43:950] **Speaker 1:** Equal to 0 So we already know that the first,
[00:04:44:109 - 00:04:47:619] **Speaker 1:** oh, we already know the first group of terms is
[00:04:47:619 - 00:04:50:149] **Speaker 1:** equal to 0 because that is our discreteized equation.
[00:04:52:450 - 00:04:54:369] **Speaker 1:** So that's what we enforce when we're trying to solve
[00:04:54:369 - 00:04:55:010] **Speaker 1:** that equation.
[00:04:55:269 - 00:04:57:369] **Speaker 1:** We had those extra terms, the residual ones due to
[00:04:57:369 - 00:04:59:850] **Speaker 1:** the Taylor series, but that just makes the difference between
[00:04:59:850 - 00:05:02:809] **Speaker 1:** the discretized and the true solution.
[00:05:02:950 - 00:05:03:649] **Speaker 1:** So that was it.
[00:05:04:369 - 00:05:06:829] **Speaker 1:** That first step, now we're looking at the second stage.
[00:05:11:880 - 00:05:14:329] **Speaker 1:** So our argument here is that the solution error.
[00:05:15:720 - 00:05:17:260] **Speaker 1:** Also satisfies this equation.
[00:05:18:190 - 00:05:20:779] **Speaker 1:** Because if we're just looking at the second line, we've
[00:05:20:779 - 00:05:21:679] **Speaker 1:** got epsilon terms.
[00:05:22:380 - 00:05:25:859] **Speaker 1:** And this implies that our error, epsilon uh propagates in
[00:05:25:859 - 00:05:27:320] **Speaker 1:** a similar fashion to That.
[00:05:28:540 - 00:05:31:700] **Speaker 1:** So what we're left with is the epsilon terms.
[00:05:32:850 - 00:05:33:660] **Speaker 1:** Which is a bit painful.
[00:05:33:739 - 00:05:36:209] **Speaker 1:** Maybe I could have left this as typed, but epsilon
[00:05:36:209 - 00:05:38:529] **Speaker 1:** IN + 1 minus epsilon IN T.
[00:05:40:700 - 00:05:43:730] **Speaker 1:** Minus alpha, epsilon 1 + 1 N.
[00:05:44:589 - 00:05:48:890] **Speaker 1:** -2 epsilon IN plus epsilon I minus 1 N over
[00:05:48:890 - 00:05:49:589] **Speaker 1:** x 2.
[00:05:51:100 - 00:05:51:750] **Speaker 1:** Equal to 0.
[00:05:55:279 - 00:05:57:239] **Speaker 1:** So this is seeing how the epsilon or the solution
[00:05:57:239 - 00:05:59:570] **Speaker 1:** error propagates over time in space.
[00:06:00:220 - 00:06:02:679] **Speaker 1:** And we're going to think back to our Fourier series.
[00:06:02:839 - 00:06:05:880] **Speaker 1:** We looked at the Fourier sign series, but we also
[00:06:05:880 - 00:06:09:190] **Speaker 1:** know that the cosine terms exist for the Fourier series.
[00:06:09:640 - 00:06:11:299] **Speaker 1:** So the complete Fourier series.
[00:06:12:410 - 00:06:17:320] **Speaker 1:** For our temperature can be given by A constant a
[00:06:17:320 - 00:06:19:480] **Speaker 1:** 0 plus an infinite sum.
[00:06:21:619 - 00:06:23:440] **Speaker 1:** From in one to infinity.
[00:06:25:489 - 00:06:29:390] **Speaker 1:** And we've got the cosine terms, so coefficient A in
[00:06:29:850 - 00:06:30:369] **Speaker 1:** cosine.
[00:06:31:269 - 00:06:34:190] **Speaker 1:** Of N omega 0 D.
[00:06:35:600 - 00:06:38:839] **Speaker 1:** And be in sign.
[00:06:39:679 - 00:06:40:570] **Speaker 1:** In I'm a good.
[00:06:47:130 - 00:06:50:239] **Speaker 1:** So this is the trig form uh with the fundamental
[00:06:50:239 - 00:06:52:369] **Speaker 1:** frequency of omega naught.
[00:06:53:970 - 00:06:55:640] **Speaker 1:** And Amberg is 2 pi over T.
[00:06:57:079 - 00:06:59:250] **Speaker 1:** Uh, in this case, this capital T is not temperature,
[00:06:59:329 - 00:07:01:609] **Speaker 1:** it's just going to be the period of oscillation.
[00:07:07:390 - 00:07:09:820] **Speaker 1:** We aren't really go and use it anywhere else, so
[00:07:09:820 - 00:07:11:269] **Speaker 1:** we're just leaving it as capital T.
[00:07:13:160 - 00:07:15:269] **Speaker 1:** And there's only so many letters in the alphabet.
[00:07:16:970 - 00:07:19:989] **Speaker 1:** So we're gonna write the full series in exponential form.
[00:07:20:839 - 00:07:23:279] **Speaker 1:** So we're going to convert our Four-year series, our infinite
[00:07:23:279 - 00:07:25:299] **Speaker 1:** series, into exponential terms.
[00:07:26:290 - 00:07:30:920] **Speaker 1:** And we've got T Equal to our sum.
[00:07:31:980 - 00:07:35:670] **Speaker 1:** From N equals minus infinity to positive infinity.
[00:07:40:459 - 00:07:42:760] **Speaker 1:** And our exponential coefficient CN.
[00:07:46:910 - 00:07:51:119] **Speaker 1:** So that I And I'm a good mom.
[00:07:53:549 - 00:07:55:899] **Speaker 1:** So here, capital I is the imaginary number.
[00:07:57:029 - 00:07:58:130] **Speaker 1:** Square root of -1.
[00:07:59:209 - 00:08:01:940] **Speaker 1:** We've distinguished that with lowercase i because we've used that
[00:08:01:940 - 00:08:04:119] **Speaker 1:** for the index, the spatial index coordinate.
[00:08:06:029 - 00:08:08:619] **Speaker 1:** Um, ends our time level and we gonna know what
[00:08:08:619 - 00:08:09:260] **Speaker 1:** we talked about to use our time.
[00:08:13:630 - 00:08:15:010] **Speaker 1:** Oh Cool.
[00:08:15:359 - 00:08:19:100] **Speaker 1:** Right, so we're essentially describing our temperature varying in time
[00:08:19:640 - 00:08:21:029] **Speaker 1:** in exponential terms.
[00:08:24:070 - 00:08:28:059] **Speaker 1:** So now we're gonna consider the error at some point
[00:08:28:059 - 00:08:29:380] **Speaker 1:** in time at T equal TN.
[00:08:30:799 - 00:08:35:239] **Speaker 1:** So we're going to label Our solution error at a
[00:08:35:239 - 00:08:38:440] **Speaker 1:** particular point in space with index I.
[00:08:39:760 - 00:08:41:140] **Speaker 1:** And time level in.
[00:08:45:229 - 00:08:49:989] **Speaker 1:** And this is going to be equal to E to
[00:08:49:989 - 00:08:50:750] **Speaker 1:** the I.
[00:08:51:599 - 00:08:53:369] **Speaker 1:** OK, lowercase i.
[00:08:54:559 - 00:08:56:119] **Speaker 1:** Data X.
[00:08:57:989 - 00:08:59:809] **Speaker 1:** So I sort of grouped a lot of the terms
[00:09:00:400 - 00:09:02:119] **Speaker 1:** together and.
[00:09:02:960 - 00:09:06:039] **Speaker 1:** labelled it K, being some consonant and no exponential.
[00:09:09:309 - 00:09:12:280] **Speaker 1:** So we've got the imaginary number I, we've got this
[00:09:12:280 - 00:09:16:380] **Speaker 1:** constant k index lowercase i and spacing x.
[00:09:18:020 - 00:09:23:369] **Speaker 1:** So This represents a single term of our four-year series.
[00:09:24:919 - 00:09:28:599] **Speaker 1:** Uh, representation of our error distributed along the grid of
[00:09:28:599 - 00:09:28:799] **Speaker 1:** points.
[00:09:28:859 - 00:09:31:979] **Speaker 1:** So we're just looking at one individual solution error point.
[00:09:34:809 - 00:09:35:729] **Speaker 1:** So bear with us.
[00:09:35:849 - 00:09:38:190] **Speaker 1:** Um, so a finite difference equation is linear.
[00:09:38:989 - 00:09:41:960] **Speaker 1:** The heat equation is linear, and the Foyer modes are
[00:09:41:960 - 00:09:45:080] **Speaker 1:** uncoupled, they don't depend on one another, they're uncoupled.
[00:09:46:010 - 00:09:48:609] **Speaker 1:** So, the argument here is that it's sufficient to only
[00:09:48:609 - 00:09:51:169] **Speaker 1:** study the propagation of the solution error of this single
[00:09:51:169 - 00:09:53:609] **Speaker 1:** term and then make some conclusion on that.
[00:09:53:690 - 00:09:56:280] **Speaker 1:** So does the solution uh get bigger and bigger over
[00:09:56:280 - 00:09:58:030] **Speaker 1:** time or does it reduce in size?
[00:09:58:570 - 00:09:59:369] **Speaker 1:** And is it stable?
[00:10:00:140 - 00:10:02:210] **Speaker 1:** So we're going to subject this form into our equation
[00:10:02:210 - 00:10:02:809] **Speaker 1:** 21.
[00:10:03:270 - 00:10:04:570] **Speaker 1:** So that was up here.
[00:10:04:849 - 00:10:07:010] **Speaker 1:** So this is our finite differencing, uh, forward in time,
[00:10:07:090 - 00:10:09:650] **Speaker 1:** centre and space, essentially replacing all the T's with those
[00:10:09:650 - 00:10:13:570] **Speaker 1:** epsilons to analyse how the solution error propagates.
[00:10:14:299 - 00:10:19:739] **Speaker 1:** Through our equation And we're going to substitute and rearrange,
[00:10:19:750 - 00:10:21:469] **Speaker 1:** and we've got Epsilon I.
[00:10:22:729 - 00:10:23:890] **Speaker 1:** In plus 1.
[00:10:25:119 - 00:10:29:919] **Speaker 1:** Uh, because it is explicit, there's only one unknown term,
[00:10:30:159 - 00:10:32:239] **Speaker 1:** so the epsilon IN + 1 on the left, and
[00:10:32:239 - 00:10:34:109] **Speaker 1:** on the right, we'll put all the terms from the
[00:10:34:109 - 00:10:35:000] **Speaker 1:** previous time level.
[00:10:36:609 - 00:10:39:880] **Speaker 1:** And we have Epsom IN.
[00:10:40:760 - 00:10:44:559] **Speaker 1:** Which we just called E to the IKIX.
[00:10:45:080 - 00:10:46:659] **Speaker 1:** So I'll make this substitution.
[00:10:53:179 - 00:10:56:539] **Speaker 1:** And we've got lambda by grouping these terms, alpha beta
[00:10:56:539 - 00:10:57:780] **Speaker 1:** T overtax 2.
[00:11:02:619 - 00:11:06:340] **Speaker 1:** And Now we have.
[00:11:07:169 - 00:11:09:049] **Speaker 1:** Epsilon I plus one.
[00:11:11:039 - 00:11:11:380] **Speaker 1:** Yeah.
[00:11:12:039 - 00:11:14:530] **Speaker 1:** So We can substitute this in as well.
[00:11:14:609 - 00:11:16:280] **Speaker 1:** So instead of being I, it's gonna be 1 +
[00:11:16:280 - 00:11:16:669] **Speaker 1:** 1.
[00:11:16:969 - 00:11:19:650] **Speaker 1:** That's the node to the right of this point.
[00:11:19:849 - 00:11:20:590] **Speaker 1:** It's got E.
[00:11:21:640 - 00:11:23:500] **Speaker 1:** To the IK.
[00:11:25:030 - 00:11:26:789] **Speaker 1:** I plus 1 X.
[00:11:29:159 - 00:11:32:239] **Speaker 1:** And then we've got -2 epsilon in.
[00:11:38:969 - 00:11:41:820] **Speaker 1:** In the last term, we've got epsilon i minus 1.
[00:11:44:010 - 00:11:45:419] **Speaker 1:** Which is very similar to the other time we've got
[00:11:45:419 - 00:11:48:419] **Speaker 1:** E to the I, K, I minus 1.
[00:11:49:239 - 00:11:50:679] **Speaker 1:** Delta X.
[00:11:57:989 - 00:12:01:049] **Speaker 1:** So Very similar process to what we did earlier, it's
[00:12:01:049 - 00:12:03:969] **Speaker 1:** just E's instead of T's, um.
[00:12:06:539 - 00:12:09:770] **Speaker 1:** And Our next step.
[00:12:10:969 - 00:12:15:190] **Speaker 0:** Is Some simplifications that's still a little bit ugly.
[00:12:15:539 - 00:12:17:479] **Speaker 1:** So we're going to have E to IK 1 +
[00:12:17:479 - 00:12:20:440] **Speaker 1:** 1 X and split it up due to the exponential
[00:12:20:440 - 00:12:20:799] **Speaker 1:** rule.
[00:12:21:419 - 00:12:26:130] **Speaker 1:** So this is equivalent to having EIKI X multiplied by
[00:12:26:130 - 00:12:27:520] **Speaker 1:** EIK X.
[00:12:28:349 - 00:12:31:349] **Speaker 1:** And we've got this uh trig formula as well.
[00:12:31:450 - 00:12:35:799] **Speaker 1:** 2 cosine k x is equal to this exponential expression
[00:12:35:799 - 00:12:36:609] **Speaker 1:** E to the ark.
[00:12:37:320 - 00:12:40:349] **Speaker 1:** Datax plus e to the minus IK X, and we're
[00:12:40:349 - 00:12:41:520] **Speaker 1:** going to simplify our equation.
[00:12:42:380 - 00:12:43:739] **Speaker 1:** And we've got Epsilon.
[00:12:44:789 - 00:12:46:940] **Speaker 1:** IN plus 1.
[00:12:48:289 - 00:12:53:500] **Speaker 1:** equal to Emma, So gamma's going to be our amplification
[00:12:53:500 - 00:12:53:820] **Speaker 1:** factor.
[00:12:53:900 - 00:12:55:359] **Speaker 1:** We'll, we'll show that shortly.
[00:12:56:210 - 00:12:57:989] **Speaker 1:** Multiplied by.
[00:12:58:679 - 00:12:59:239] **Speaker 1:** A.
[00:13:00:090 - 00:13:03:190] **Speaker 1:** To the IKI X.
[00:13:04:989 - 00:13:08:599] **Speaker 1:** Which is gamma times epsilon iN.
[00:13:12:770 - 00:13:15:890] **Speaker 1:** Now, the terms that we grouped together with these simplifications,
[00:13:16:000 - 00:13:24:549] **Speaker 1:** gamma is going to be equal to 1 + 2
[00:13:24:549 - 00:13:25:080] **Speaker 1:** lambda.
[00:13:26:640 - 00:13:28:760] **Speaker 1:** Multiplied by cos.
[00:13:29:359 - 00:13:30:469] **Speaker 0:** OK, Dad X.
[00:13:32:669 - 00:13:34:530] **Speaker 1:** Minus One.
[00:13:42:650 - 00:13:44:710] **Speaker 1:** So after some rearrangement, what we have here.
[00:13:46:390 - 00:13:50:070] **Speaker 1:** Is the solution error at a point I at the
[00:13:50:070 - 00:13:52:190] **Speaker 1:** next time level T N + 1.
[00:13:53:469 - 00:13:55:909] **Speaker 1:** As a function of the solution error at the previous
[00:13:55:909 - 00:13:58:229] **Speaker 1:** time level, time level in epsilon in.
[00:13:58:390 - 00:14:00:390] **Speaker 1:** And it's got this uh coefficient gamma.
[00:14:00:750 - 00:14:03:429] **Speaker 1:** So if gamma is greater than 1, it's going to
[00:14:03:429 - 00:14:05:369] **Speaker 1:** get larger and larger, the solution error.
[00:14:05:630 - 00:14:07:510] **Speaker 1:** And if it's equal to 1, it's gonna stay the
[00:14:07:510 - 00:14:07:830] **Speaker 1:** same.
[00:14:07:950 - 00:14:09:330] **Speaker 1:** If it's less than 1, it's gonna reduce.
[00:14:10:419 - 00:14:13:390] **Speaker 1:** So we're gonna dictate or discover the stability of this
[00:14:13:390 - 00:14:16:590] **Speaker 1:** numerical solution by evaluating this term gamma.
[00:14:24:830 - 00:14:28:130] **Speaker 1:** So that's figuring out whether it's magnified the solution error
[00:14:28:130 - 00:14:30:950] **Speaker 1:** is magnified or not between subsequent time steps.
[00:14:31:409 - 00:14:34:830] **Speaker 1:** And we're using this gamma that we're labelling the amplification
[00:14:34:830 - 00:14:35:309] **Speaker 1:** factor.
[00:14:36:650 - 00:14:36:969] **Speaker 1:** Cool.
[00:14:37:820 - 00:14:40:460] **Speaker 1:** So the error will not magnify if the stability criterion
[00:14:40:619 - 00:14:42:799] **Speaker 1:** is less than or equal to 1, so take the
[00:14:42:799 - 00:14:45:539] **Speaker 1:** absolute value, so it's between -1 and 1.
[00:14:46:450 - 00:14:47:630] **Speaker 1:** Otherwise, the area's gonna grow.
[00:14:49:580 - 00:14:52:419] **Speaker 1:** So our expression for gamma can be further simplified by
[00:14:52:419 - 00:14:55:700] **Speaker 1:** using a double-angle formula, cosine k x equal to 1
[00:14:55:700 - 00:14:57:969] **Speaker 1:** minus 2 sin square kx over 2.
[00:14:58:219 - 00:15:00:340] **Speaker 1:** So heaps and heaps of trick functions if you require
[00:15:00:340 - 00:15:02:979] **Speaker 1:** them, I'll provide them in assessments.
[00:15:03:869 - 00:15:05:890] **Speaker 1:** So this yields gamma.
[00:15:07:150 - 00:15:10:250] **Speaker 1:** Equal to 1 minus 4 lambda sin squared.
[00:15:11:489 - 00:15:15:049] **Speaker 1:** K X over 2.
[00:15:20:809 - 00:15:24:140] **Speaker 1:** Cause ultimately we want to figure out what values lamb
[00:15:24:140 - 00:15:25:929] **Speaker 1:** uh gamma holds.
[00:15:27:650 - 00:15:31:820] **Speaker 1:** For all of these different x values, X, cases, etc.
[00:15:35:179 - 00:15:38:450] **Speaker 1:** So our inequality on the upper bound, we want gamma
[00:15:38:450 - 00:15:39:599] **Speaker 1:** to be less than or equal to one.
[00:15:40:640 - 00:15:42:200] **Speaker 1:** We also want it to be greater than or equal
[00:15:42:200 - 00:15:44:979] **Speaker 1:** to -1, so we'll start with the less than or
[00:15:45:150 - 00:15:45:979] **Speaker 1:** equal to 1.
[00:15:47:619 - 00:15:50:859] **Speaker 1:** Which means that our gamma term 1 minus 4 lambda
[00:15:50:859 - 00:15:53:570] **Speaker 1:** sin square ks over 2 has to be less than
[00:15:53:570 - 00:15:54:280] **Speaker 1:** or equal to 1.
[00:15:56:669 - 00:16:00:849] **Speaker 1:** Now, what range of values does a sine function hold?
[00:16:01:919 - 00:16:03:969] **Speaker 1:** Or more specifically a sin squared function.
[00:16:08:219 - 00:16:11:859] **Speaker 1:** Yep, so we know the sine wave goes from 1
[00:16:11:859 - 00:16:12:659] **Speaker 1:** down to -1.
[00:16:12:739 - 00:16:14:419] **Speaker 1:** If we take a square of that, it's gonna just
[00:16:14:419 - 00:16:15:359] **Speaker 1:** go from 0 to 1.
[00:16:16:659 - 00:16:20:539] **Speaker 1:** So 1 minus 1 is going to be 0.
[00:16:22:969 - 00:16:24:299] **Speaker 1:** So if lambda is equal to one.
[00:16:25:049 - 00:16:30:119] **Speaker 1:** Um, if sin squared is 0, we have the upper
[00:16:30:119 - 00:16:33:119] **Speaker 1:** limit of 1, so 1 minus 0 is equal to
[00:16:33:119 - 00:16:33:520] **Speaker 1:** 1.
[00:16:38:890 - 00:16:41:010] **Speaker 1:** So the argument here is that we need lambda to
[00:16:41:010 - 00:16:43:030] **Speaker 1:** be greater than or equal to 0.
[00:16:44:039 - 00:16:45:659] **Speaker 1:** For this inequality to hold.
[00:16:48:900 - 00:16:51:619] **Speaker 1:** So lambda redefined.
[00:16:52:409 - 00:16:55:169] **Speaker 1:** I guess we can remind ourselves what we said lambda
[00:16:55:169 - 00:16:55:640] **Speaker 1:** was.
[00:16:57:880 - 00:17:01:679] **Speaker 1:** Alpha Data T over X2.
[00:17:08:198 - 00:17:10:798] **Speaker 1:** Alpha is the heat divisivity of the material, so it's
[00:17:10:798 - 00:17:11:779] **Speaker 1:** always going to be a positive value.
[00:17:12:670 - 00:17:15:489] **Speaker 1:** Um, I guess that's thermodynamics.
[00:17:15:910 - 00:17:17:750] **Speaker 1:** Delta T is a finite time step.
[00:17:18:479 - 00:17:19:680] **Speaker 1:** And delta X's as well.
[00:17:19:800 - 00:17:21:300] **Speaker 1:** So all of these values are positive.
[00:17:22:569 - 00:17:24:530] **Speaker 1:** So this condition that lambda is greater than or equal
[00:17:24:530 - 00:17:27:829] **Speaker 1:** to 0 is always satisfied, so unconditionally satisfied.
[00:17:30:290 - 00:17:31:099] **Speaker 1:** So that's one tick.
[00:17:31:380 - 00:17:33:579] **Speaker 1:** Now we look at the lower limit, so gamma has
[00:17:33:579 - 00:17:35:439] **Speaker 1:** to be greater than or equal to -1.
[00:17:36:680 - 00:17:38:459] **Speaker 1:** And this requires that Al Gamma.
[00:17:39:319 - 00:17:40:680] **Speaker 1:** Is greater than equal to -1.
[00:17:40:760 - 00:17:44:400] **Speaker 1:** If we rearrange for gamma, we've got 1/2 sin squared.
[00:17:46:130 - 00:17:49:300] **Speaker 1:** Again, we said that sin squared goes from 0 to
[00:17:49:300 - 00:17:49:699] **Speaker 1:** 1.
[00:17:50:780 - 00:17:51:819] **Speaker 1:** So if it was one.
[00:17:53:140 - 00:17:55:810] **Speaker 1:** Then we would have 1 divided by 2 times 1.
[00:17:56:800 - 00:17:57:959] **Speaker 1:** So that's one limit.
[00:17:58:770 - 00:18:01:939] **Speaker 1:** The other limit is 0, so 1 divided by 0
[00:18:01:939 - 00:18:03:819] **Speaker 1:** or is it tends to 0 is going to go
[00:18:03:819 - 00:18:07:020] **Speaker 1:** off to infinity and that's greater than -1.
[00:18:07:290 - 00:18:08:000] **Speaker 1:** So that's all good.
[00:18:09:119 - 00:18:11:319] **Speaker 1:** So our limit that we're looking at is 5.
[00:18:13:390 - 00:18:14:760] **Speaker 1:** So this is a condition.
[00:18:15:550 - 00:18:19:229] **Speaker 1:** On our FDCF scheme that needs to be met to
[00:18:19:229 - 00:18:20:030] **Speaker 1:** ensure stability.
[00:18:21:300 - 00:18:24:579] **Speaker 1:** So in summary, we've arrived at the same stability criterion
[00:18:24:579 - 00:18:25:959] **Speaker 1:** that we established earlier.
[00:18:26:739 - 00:18:29:060] **Speaker 1:** That lambda has to be less than or equal to
[00:18:29:060 - 00:18:29:459] **Speaker 1:** 12.
[00:18:38:229 - 00:18:40:849] **Speaker 1:** So there's more maths, that's more rigorous.
[00:18:41:660 - 00:18:44:930] **Speaker 1:** And Is hopefully convincing.
[00:18:46:020 - 00:18:47:739] **Speaker 1:** So our forward in time interest based scheme to be
[00:18:47:739 - 00:18:49:329] **Speaker 1:** stable.
[00:18:51:390 - 00:18:55:949] **Speaker 1:** The amplification factor gamma must also satisfy that criterion that
[00:18:55:949 - 00:18:56:670] **Speaker 1:** we've just said.
[00:18:57:439 - 00:19:00:180] **Speaker 1:** Absolute value being less than or equal to 1.
[00:19:10:250 - 00:19:10:489] **Speaker 1:** Cool.
[00:19:12:239 - 00:19:14:250] **Speaker 1:** So it's pretty boring to go watch someone going through
[00:19:14:250 - 00:19:14:729] **Speaker 1:** all the steps.
[00:19:14:810 - 00:19:17:130] **Speaker 1:** So in, in your own time and in the exercise
[00:19:17:130 - 00:19:20:130] **Speaker 1:** and elsewhere you can work through uh the the steps
[00:19:20:130 - 00:19:21:869] **Speaker 1:** yourself to convince yourself.
[00:19:22:910 - 00:19:26:650] **Speaker 1:** Um, are there any questions on this approach?
[00:19:28:099 - 00:19:30:939] **Speaker 1:** It's a little bit hand wavy, but we've, we've essentially
[00:19:30:939 - 00:19:36:459] **Speaker 1:** described the solution error and with 4-year terms and an
[00:19:36:459 - 00:19:37:140] **Speaker 1:** expenditure.
[00:19:39:109 - 00:19:41:319] **Speaker 1:** And we're just trying to see, does the solution er
[00:19:41:319 - 00:19:43:239] **Speaker 1:** grow over time or does it shrink.
[00:19:46:390 - 00:19:47:859] **Speaker 1:** Alright, convinced you enough.
[00:19:48:280 - 00:19:49:199] **Speaker 1:** Alright, so convergence.
[00:19:49:479 - 00:19:53:020] **Speaker 1:** So the convergence of our scheme is defined where our
[00:19:53:479 - 00:19:55:420] **Speaker 1:** computed solution, so the one at the end.
[00:20:01:569 - 00:20:05:770] **Speaker 1:** It approaches the exact solution of our PDE, so the
[00:20:05:770 - 00:20:08:369] **Speaker 1:** one at the start, so that it's consistent and stable.
[00:20:09:609 - 00:20:12:869] **Speaker 1:** And that the discretization error and the solution error vanishes.
[00:20:16:500 - 00:20:19:020] **Speaker 1:** As we refine our spatial and temporal grids.
[00:20:20:119 - 00:20:22:079] **Speaker 1:** So we can write this in math form, so we
[00:20:22:079 - 00:20:22:780] **Speaker 1:** can take the limit.
[00:20:23:650 - 00:20:27:729] **Speaker 1:** Of our time step data T and spatial grid sizing
[00:20:27:729 - 00:20:28:449] **Speaker 1:** data X.
[00:20:29:579 - 00:20:30:170] **Speaker 1:** To 0.
[00:20:34:550 - 00:20:37:619] **Speaker 1:** And taking the limit of our mesh resolution and time,
[00:20:38:069 - 00:20:38:640] **Speaker 1:** time steps.
[00:20:39:839 - 00:20:41:400] **Speaker 1:** For our final computed solution.
[00:20:43:459 - 00:20:50:010] **Speaker 1:** I Is going to match our exact solution of the
[00:20:50:010 - 00:20:50:849] **Speaker 1:** PDET.
[00:20:51:780 - 00:20:55:780] **Speaker 1:** Being evaluated at a spatial coordinate XI time level 10.
[00:20:57:260 - 00:21:00:250] **Speaker 0:** For all X I T N.
[00:21:06:069 - 00:21:08:989] **Speaker 1:** So as with all good Math discoveries.
[00:21:09:109 - 00:21:10:489] **Speaker 1:** Someone's labelled it.
[00:21:10:829 - 00:21:13:819] **Speaker 1:** We've got the Lexus equivalent serum, which states that given
[00:21:13:819 - 00:21:18:189] **Speaker 1:** a well-posed linear initial value problem using a consistent numerical
[00:21:18:189 - 00:21:19:829] **Speaker 1:** scheme, so we talked about consistency.
[00:21:20:540 - 00:21:23:579] **Speaker 1:** Uh, the method is convergent if and only if it
[00:21:23:579 - 00:21:24:540] **Speaker 1:** is also stable.
[00:21:25:239 - 00:21:28:449] **Speaker 1:** So we require consistency and stability for convergence.
[00:22:04:040 - 00:22:07:890] **Speaker 1:** So, Yeah, it's.
[00:22:09:349 - 00:22:11:390] **Speaker 1:** I guess there's a few words in there, but I
[00:22:11:390 - 00:22:12:170] **Speaker 1:** mean, well posed.
[00:22:12:260 - 00:22:14:050] **Speaker 1:** I mean, we talked a little bit about boundary conditions
[00:22:14:050 - 00:22:17:410] **Speaker 1:** the other day, and um a few of you explored
[00:22:17:589 - 00:22:21:750] **Speaker 1:** unintentionally in the labs, uh, for not well posed problems.
[00:22:21:869 - 00:22:24:930] **Speaker 1:** So if you think back to your simply supported being,
[00:22:26:329 - 00:22:27:229] **Speaker 1:** Some of you had.
[00:22:28:319 - 00:22:32:959] **Speaker 1:** Fixed the beam on one side and provided a constraint,
[00:22:33:579 - 00:22:36:040] **Speaker 1:** ah, so essentially a pin and then the the one
[00:22:36:040 - 00:22:37:459] **Speaker 1:** on the right was also free.
[00:22:38:119 - 00:22:41:609] **Speaker 1:** So, If you had a beam that was only supported
[00:22:41:609 - 00:22:44:339] **Speaker 1:** on one side, one end and you apply the loading
[00:22:44:339 - 00:22:46:390] **Speaker 1:** on the top, it would essentially just spin around.
[00:22:47:170 - 00:22:51:300] **Speaker 1:** Uh, so, uh, you can't find a steady-state solution for
[00:22:51:300 - 00:22:51:920] **Speaker 1:** this problem.
[00:22:52:540 - 00:22:54:729] **Speaker 1:** So in that sense it's, it's not well posed.
[00:22:55:060 - 00:22:56:959] **Speaker 1:** So you need to make sure that your boundary conditions
[00:22:57:140 - 00:22:59:119] **Speaker 1:** adequately constrain the problem.
[00:23:01:000 - 00:23:04:030] **Speaker 1:** So there's quite a bit involved with that well-posedness, um,
[00:23:04:119 - 00:23:06:520] **Speaker 1:** but if you just think of your boundary conditions, it'll
[00:23:06:520 - 00:23:07:599] **Speaker 1:** get you most of the way there.
[00:23:10:530 - 00:23:11:010] **Speaker 1:** Cool.
[00:23:11:290 - 00:23:15:270] **Speaker 1:** So our convergence of a numerical scheme can be determined
[00:23:15:410 - 00:23:17:770] **Speaker 1:** by first considering the consistency.
[00:23:18:550 - 00:23:21:349] **Speaker 1:** So that was the truncation error that we looked at
[00:23:21:349 - 00:23:24:569] **Speaker 1:** due to those Taylor series uh terms being neglected.
[00:23:25:770 - 00:23:27:209] **Speaker 1:** And also the stability.
[00:23:27:339 - 00:23:29:660] **Speaker 1:** So looking at the solution error, uh.
[00:23:30:640 - 00:23:32:050] **Speaker 1:** To ensure boundedness.
[00:23:33:099 - 00:23:35:619] **Speaker 1:** So this prob this theorem only holds for linear problems.
[00:23:36:869 - 00:23:41:699] **Speaker 1:** Um, And we've mostly focused on linear PDEs in this
[00:23:41:699 - 00:23:42:119] **Speaker 1:** course.
[00:23:43:680 - 00:23:48:599] **Speaker 1:** Uh, and we can also solve nonlinear PDEs by linearizing
[00:23:48:599 - 00:23:49:020] **Speaker 1:** them.
[00:23:49:839 - 00:23:52:939] **Speaker 1:** We don't really go into that detail in this course.
[00:23:54:109 - 00:23:58:420] **Speaker 1:** I did Um, I don't cheekily add in a nonlinear
[00:23:58:560 - 00:24:01:479] **Speaker 1:** expression in the assignment for fun, so that was with
[00:24:01:479 - 00:24:04:520] **Speaker 1:** the thermal conductivity as a function of the dependent variable
[00:24:04:520 - 00:24:04:680] **Speaker 1:** T.
[00:24:06:199 - 00:24:08:209] **Speaker 1:** We don't have to worry too much about that because
[00:24:08:209 - 00:24:10:569] **Speaker 1:** it's an explicit scheme, so you're evaluating the temperature at
[00:24:10:569 - 00:24:12:989] **Speaker 1:** the previous time level, so you shouldn't encounter issues.
[00:24:13:790 - 00:24:18:609] **Speaker 1:** Um Yeah Cool.
[00:24:19:380 - 00:24:24:000] **Speaker 1:** All right, so that was Consistency, stability and convergence.
[00:24:24:420 - 00:24:26:000] **Speaker 1:** There's a couple of exercises here.
[00:24:26:760 - 00:24:29:920] **Speaker 1:** And I'll leave those for you.
[00:24:31:609 - 00:24:33:640] **Speaker 1:** To work on, um, because I want to get started
[00:24:33:640 - 00:24:36:880] **Speaker 1:** on chapter 12, considering that the assignment includes a little
[00:24:36:880 - 00:24:37:800] **Speaker 1:** bit of optimisation.
[00:24:40:180 - 00:24:44:270] **Speaker 1:** Um, Yeah, I guess some feedback is having more examples
[00:24:44:270 - 00:24:44:780] **Speaker 1:** in the lectures.
[00:24:44:829 - 00:24:46:709] **Speaker 1:** I do want to focus on going through the theory
[00:24:46:709 - 00:24:48:790] **Speaker 1:** first, and then in the last week or two we'll
[00:24:48:790 - 00:24:52:469] **Speaker 1:** have more time to work through examples, and I'll detail
[00:24:52:469 - 00:24:55:069] **Speaker 1:** what's expected of the exam and all of those sorts
[00:24:55:069 - 00:24:55:790] **Speaker 1:** of details.
[00:24:56:390 - 00:24:57:910] **Speaker 1:** I just want to make sure that we cover enough
[00:24:57:910 - 00:25:00:130] **Speaker 1:** material that you can do the assignment.
[00:25:01:550 - 00:25:03:369] **Speaker 1:** That's why we're focused on theory first.
[00:25:04:530 - 00:25:06:410] **Speaker 1:** All right, so that's chapter 11.
[00:25:06:489 - 00:25:07:589] **Speaker 1:** Any questions on this?
[00:25:10:650 - 00:25:12:780] **Speaker 0:** Really Silence.
[00:25:14:140 - 00:25:15:579] **Speaker 1:** All right, so.
[00:25:19:579 - 00:25:21:599] **Speaker 1:** Chapter 12 is page 101.
[00:25:24:989 - 00:25:25:949] **Speaker 1:** Or the next page for you.
[00:25:27:390 - 00:25:30:979] **Speaker 1:** And Well, I edit this chapter a few years ago
[00:25:30:979 - 00:25:33:219] **Speaker 1:** now, but, um, sort of.
[00:25:35:579 - 00:25:38:469] **Speaker 1:** Inspired that there's a lot of engineering problems that require
[00:25:38:469 - 00:25:39:250] **Speaker 1:** optimisation.
[00:25:40:550 - 00:25:43:550] **Speaker 1:** And there's a nice lecture series, I assume it's still
[00:25:43:550 - 00:25:46:390] **Speaker 1:** going, I, I didn't check this year, um, provided on,
[00:25:46:469 - 00:25:49:969] **Speaker 1:** on YouTube by this guy over in, um, Germany at
[00:25:49:969 - 00:25:51:170] **Speaker 1:** KIT.
[00:25:51:910 - 00:25:53:739] **Speaker 1:** Uh, if you want to follow along, he probably explains
[00:25:53:739 - 00:25:55:290] **Speaker 1:** it better than me, but we're just going to spend
[00:25:55:290 - 00:25:57:319] **Speaker 1:** 2, well not even 2 hours on this.
[00:25:57:589 - 00:26:00:310] **Speaker 1:** Uh, so just a quick run through of optimisation methods
[00:26:00:310 - 00:26:02:250] **Speaker 1:** and what they mean for numerical modelling.
[00:26:02:750 - 00:26:05:270] **Speaker 1:** Uh, if you're really keen, there's obviously heaps of textbooks
[00:26:05:270 - 00:26:05:670] **Speaker 1:** as well.
[00:26:07:900 - 00:26:10:589] **Speaker 1:** So first, I just wanna give a bit of an
[00:26:10:589 - 00:26:11:239] **Speaker 1:** overview.
[00:26:11:780 - 00:26:14:619] **Speaker 1:** So determining an optimal solution for a given problem is
[00:26:14:619 - 00:26:15:380] **Speaker 1:** common for engineers.
[00:26:15:500 - 00:26:18:660] **Speaker 1:** Maybe we want to optimise um by reducing drag on
[00:26:18:660 - 00:26:22:560] **Speaker 1:** a vehicle or reduce cost when manufacturing a product.
[00:26:24:189 - 00:26:26:660] **Speaker 1:** So there's many types of different optimisation problems.
[00:26:27:520 - 00:26:30:660] **Speaker 1:** So cost optimisation of manufacturing a car.
[00:26:31:939 - 00:26:34:930] **Speaker 1:** He's one example, so this might involve minimising.
[00:26:37:000 - 00:26:44:319] **Speaker 1:** The cost So the cost would perhaps actually be just
[00:26:44:319 - 00:26:45:140] **Speaker 1:** a financial cost.
[00:26:47:010 - 00:26:48:050] **Speaker 1:** And labour costs.
[00:26:48:770 - 00:26:54:339] **Speaker 1:** And it's subject To some performance criteria.
[00:27:01:390 - 00:27:03:920] **Speaker 1:** Exceeding or matching some requirements.
[00:27:09:780 - 00:27:12:599] **Speaker 1:** So this is essentially under a requirement.
[00:27:16:739 - 00:27:17:339] **Speaker 1:** Constraint.
[00:27:23:290 - 00:27:25:979] **Speaker 1:** Um, I mean, we've got War of Fitness, the waft
[00:27:25:979 - 00:27:27:930] **Speaker 1:** in New Zealand, so our cars have to match that.
[00:27:28:300 - 00:27:31:060] **Speaker 1:** So maybe that's a requirement, it's pretty low, low expectation,
[00:27:31:160 - 00:27:34:310] **Speaker 1:** but a car would operate in that, in that environment.
[00:27:34:739 - 00:27:36:979] **Speaker 1:** Uh, so maybe you're trying to manufacture a car that
[00:27:36:979 - 00:27:37:619] **Speaker 1:** passes the waft.
[00:27:39:020 - 00:27:41:300] **Speaker 1:** Or you might have a performance that's higher than that,
[00:27:41:699 - 00:27:44:339] **Speaker 1:** if you had a car enthusiast that wanted to go
[00:27:44:339 - 00:27:46:930] **Speaker 1:** faster, um, and that sort of thing.
[00:27:48:150 - 00:27:50:699] **Speaker 1:** So this would obviously be dependent on the client or
[00:27:50:699 - 00:27:52:839] **Speaker 1:** customer and and the manufacturer.
[00:27:54:800 - 00:27:58:290] **Speaker 1:** So it's cost optimisation, another optimisation series we could look
[00:27:58:290 - 00:28:02:670] **Speaker 1:** at was the performance optimisation, maybe of a satellite trajectory.
[00:28:03:010 - 00:28:19:910] **Speaker 1:** So we're trying to maximise, Performance Subject To some cost.
[00:28:23:239 - 00:28:24:219] **Speaker 1:** Matching some budget.
[00:28:26:199 - 00:28:28:760] **Speaker 1:** So maybe we're in aerospace, um.
[00:28:29:800 - 00:28:30:880] **Speaker 1:** We want to get some satellites up.
[00:28:30:949 - 00:28:33:239] **Speaker 1:** We've got a really big budget because they everyone throws
[00:28:33:239 - 00:28:36:560] **Speaker 1:** money into that industry, uh, and we want to maximise
[00:28:36:560 - 00:28:36:859] **Speaker 1:** performance.
[00:28:38:380 - 00:28:41:339] **Speaker 1:** These X hats are essentially just free parameters or things
[00:28:41:339 - 00:28:43:040] **Speaker 1:** that we can adjust, so.
[00:28:44:550 - 00:28:47:670] **Speaker 1:** The things that are free to to change in our
[00:28:47:670 - 00:28:48:310] **Speaker 1:** design process.
[00:28:50:619 - 00:28:53:520] **Speaker 1:** And this is an example of being under.
[00:28:55:339 - 00:28:58:089] **Speaker 1:** A cost Constraint.
[00:29:01:060 - 00:29:02:880] **Speaker 1:** We constrained by our cost.
[00:29:07:810 - 00:29:09:810] **Speaker 1:** So typically you'll probably have a mixture of both of
[00:29:09:810 - 00:29:11:969] **Speaker 1:** these, you want to have some cost constraint, you want
[00:29:11:969 - 00:29:15:380] **Speaker 1:** to have some performance requirements, and you want to have
[00:29:15:380 - 00:29:18:089] **Speaker 1:** a balance, depending on what kind of market you're aiming
[00:29:18:089 - 00:29:20:729] **Speaker 1:** for and your objectives.
[00:29:21:989 - 00:29:23:969] **Speaker 1:** So we might want to maximise.
[00:29:26:270 - 00:29:41:430] **Speaker 1:** Performance And if we want to minimise cost, Uh, if
[00:29:41:430 - 00:29:43:949] **Speaker 1:** we just take the minus of that, then essentially it's
[00:29:44:150 - 00:29:46:829] **Speaker 1:** maximising the the minimum cost.
[00:29:47:229 - 00:29:51:449] **Speaker 1:** So alpha, Cost X.
[00:29:51:920 - 00:29:54:239] **Speaker 1:** So alpha is just a variable if you want to
[00:29:54:239 - 00:29:59:099] **Speaker 1:** sort of bias towards reducing cost more or biassed towards
[00:30:00:160 - 00:30:01:339] **Speaker 1:** improving performance.
[00:30:04:780 - 00:30:05:140] **Speaker 1:** So.
[00:30:06:750 - 00:30:09:619] **Speaker 1:** Yeah, just Bit of an overview.
[00:30:09:939 - 00:30:14:630] **Speaker 1:** So optimisation is used in a lot of theory, a
[00:30:14:630 - 00:30:17:310] **Speaker 1:** lot of tools, a lot of sets, uh, often in
[00:30:17:310 - 00:30:17:969] **Speaker 1:** computer vision.
[00:30:18:390 - 00:30:20:500] **Speaker 1:** Uh, I think a lot of, well, some of the
[00:30:20:500 - 00:30:23:050] **Speaker 1:** students take the computer vision course in the 4th year.
[00:30:23:229 - 00:30:25:849] **Speaker 1:** Um, I guess it's open to everyone, I'm not sure.
[00:30:26:229 - 00:30:29:500] **Speaker 1:** But in computer vision, they look at stereo matching, uh,
[00:30:29:609 - 00:30:32:250] **Speaker 1:** image denoising, image to blurring and things.
[00:30:32:790 - 00:30:34:910] **Speaker 1:** So all of these are sort of optimisation problems.
[00:30:35:209 - 00:30:39:250] **Speaker 1:** Uh, in fact, if you, think about it more, um.
[00:30:40:160 - 00:30:42:839] **Speaker 1:** A lot of neural networks are also just optimisation problems
[00:30:42:839 - 00:30:43:969] **Speaker 1:** and loss functions.
[00:30:45:239 - 00:30:49:819] **Speaker 1:** And I'm sure you're using Using those large language models
[00:30:49:819 - 00:30:52:579] **Speaker 1:** for for different things, not the assignment, but um for
[00:30:52:579 - 00:30:54:140] **Speaker 1:** lots of other activities.
[00:30:54:540 - 00:30:58:719] **Speaker 1:** So, You're already using optimisation methods without realising it.
[00:31:00:239 - 00:31:04:000] **Speaker 1:** So these problems typically use some energy function to describe
[00:31:04:000 - 00:31:05:880] **Speaker 1:** the solution quality, so.
[00:31:06:859 - 00:31:08:459] **Speaker 1:** Yeah, they're very high dimensional.
[00:31:09:650 - 00:31:10:839] **Speaker 1:** Including neural networks.
[00:31:12:060 - 00:31:15:160] **Speaker 1:** So, I don't know heaps about all of that theory,
[00:31:15:180 - 00:31:17:060] **Speaker 1:** but that's my understanding.
[00:31:19:619 - 00:31:21:329] **Speaker 1:** There's also optimisation in nature.
[00:31:21:619 - 00:31:24:250] **Speaker 1:** So if you think of the aerodynamics of birds, the
[00:31:24:250 - 00:31:27:400] **Speaker 1:** wings on birds, so that to sort of minimise drag,
[00:31:27:819 - 00:31:30:619] **Speaker 1:** and how they interact with the air, how they flow,
[00:31:30:979 - 00:31:33:140] **Speaker 1:** how they fly, um.
[00:31:34:280 - 00:31:35:859] **Speaker 1:** Soap, film and bubbles.
[00:31:36:719 - 00:31:38:800] **Speaker 1:** So if you think of the surface tension of a
[00:31:38:800 - 00:31:43:630] **Speaker 1:** bubble, it'll be Naturally going to minimum surface energy.
[00:31:44:109 - 00:31:47:469] **Speaker 1:** So you've got a spherical bubble rather than being square
[00:31:47:469 - 00:31:50:390] **Speaker 1:** or something else where you'd have a higher surface tension.
[00:31:53:599 - 00:31:57:369] **Speaker 1:** And protein folding Here's another example, and I don't know
[00:31:57:369 - 00:31:58:589] **Speaker 1:** too much about that.
[00:31:59:880 - 00:32:02:410] **Speaker 1:** Uh, so these processes are naturally driven by some minimum
[00:32:02:410 - 00:32:02:510] **Speaker 1:** energy.
[00:32:03:849 - 00:32:07:229] **Speaker 1:** And, yeah, the principle of least action.
[00:32:07:849 - 00:32:10:609] **Speaker 1:** So we see it both in nature and we're forcing
[00:32:10:609 - 00:32:12:229] **Speaker 1:** it in our engineering problems.
[00:32:14:300 - 00:32:16:979] **Speaker 1:** I want to go through some definitions that we will
[00:32:16:979 - 00:32:18:489] **Speaker 1:** use in some of our methods.
[00:32:19:939 - 00:32:24:420] **Speaker 1:** So our variables or free parameters we've labelled X uh
[00:32:24:420 - 00:32:24:780] **Speaker 1:** Vic.
[00:32:26:319 - 00:32:30:050] **Speaker 1:** Vector or X arrow, and this belongs to some appropriate
[00:32:30:050 - 00:32:30:989] **Speaker 1:** solution space.
[00:32:32:420 - 00:32:36:739] **Speaker 1:** So the backward E belonging to the set X capital
[00:32:36:739 - 00:32:37:130] **Speaker 1:** X.
[00:32:37:660 - 00:32:42:020] **Speaker 1:** So If we think of designing a car, the length
[00:32:42:020 - 00:32:45:380] **Speaker 1:** of the car would Can't be too long, can't be
[00:32:45:380 - 00:32:48:150] **Speaker 1:** too short, so there's a, there's a solution space that
[00:32:48:150 - 00:32:50:290] **Speaker 1:** we allow the length to to hold.
[00:32:51:109 - 00:32:53:099] **Speaker 1:** We can write our optimisation problems.
[00:33:00:089 - 00:33:11:560] **Speaker 0:** W X vector Star Which is our free parameters and
[00:33:11:560 - 00:33:13:930] **Speaker 1:** the special free parameters, they are the ones that provide
[00:33:13:930 - 00:33:15:280] **Speaker 1:** the optimum solution.
[00:33:16:099 - 00:33:18:939] **Speaker 1:** So X is going to be our optimum set of
[00:33:18:939 - 00:33:19:619] **Speaker 1:** variables.
[00:33:20:390 - 00:33:28:829] **Speaker 1:** And this is Equal to The argument that minimises.
[00:33:29:650 - 00:33:31:319] **Speaker 1:** Some objective function F.
[00:33:32:829 - 00:33:33:510] **Speaker 1:** Of X.
[00:33:34:959 - 00:33:39:270] **Speaker 1:** And X Belongs to our solution space.
[00:33:40:800 - 00:33:41:479] **Speaker 1:** Capital X.
[00:33:46:089 - 00:33:50:599] **Speaker 1:** So in words, we're trying to minimise some objective.
[00:33:50:920 - 00:33:56:680] **Speaker 1:** Maybe it's the cost, maybe it's improving the performance within
[00:33:56:689 - 00:33:59:119] **Speaker 1:** the space that we've allowed the three variables to exist
[00:33:59:119 - 00:34:05:180] **Speaker 1:** under X to find the minimizer or optimizer X star.
[00:34:11:739 - 00:34:16:860] **Speaker 1:** So If you think back to your high school maths,
[00:34:17:100 - 00:34:20:870] **Speaker 1:** you, you, um, I can't remember the problems, you, something
[00:34:20:870 - 00:34:23:870] **Speaker 1:** with a paddock and you optimise the area or the
[00:34:23:870 - 00:34:26:860] **Speaker 1:** fencing that you require to get the area, something like
[00:34:26:860 - 00:34:28:790] **Speaker 1:** that, and you find the the gradient.
[00:34:30:270 - 00:34:31:570] **Speaker 1:** If that rings any bells.
[00:34:31:790 - 00:34:33:969] **Speaker 1:** Um, so we do the same in this space.
[00:34:34:040 - 00:34:37:148] **Speaker 1:** Essentially we know that a minima exists where the gradient
[00:34:37:148 - 00:34:39:350] **Speaker 1:** of our function is equal to zero.
[00:34:40:269 - 00:34:43:468] **Speaker 1:** So we grade F, F being our objective function is
[00:34:43:468 - 00:34:47:539] **Speaker 1:** 0 and our second order derivative is greater than 0.
[00:34:47:668 - 00:34:50:489] **Speaker 1:** So let's make sure that it's um convex.
[00:34:52:699 - 00:34:56:260] **Speaker 1:** So this is Provided that our objective function is twice
[00:34:56:260 - 00:34:56:908] **Speaker 1:** differentiable.
[00:34:58:139 - 00:35:00:790] **Speaker 1:** So we'll go through what is grade F and grad
[00:35:00:790 - 00:35:01:350] **Speaker 1:** squared F.
[00:35:01:709 - 00:35:02:590] **Speaker 1:** So grad F.
[00:35:12:810 - 00:35:16:449] **Speaker 1:** is a vector because it's a gradient of our function.
[00:35:16:610 - 00:35:18:330] **Speaker 1:** It depends on multiple variables.
[00:35:18:570 - 00:35:20:810] **Speaker 1:** So we need to do a derivative in each of
[00:35:20:810 - 00:35:21:750] **Speaker 1:** those variables.
[00:35:22:379 - 00:35:28:870] **Speaker 1:** So we've got grad if Of X hat.
[00:35:29:889 - 00:35:32:120] **Speaker 1:** Or X vector via DX1.
[00:35:33:429 - 00:35:37:110] **Speaker 1:** All the way to DF of X.
[00:35:38:159 - 00:35:39:830] **Speaker 1:** 5 DX.
[00:35:40:939 - 00:35:43:979] **Speaker 1:** And So however many variables we've got.
[00:35:51:850 - 00:35:53:929] **Speaker 1:** So this can be used to find the tangent plane,
[00:35:54:209 - 00:35:55:850] **Speaker 1:** so if we're in 2D you can think of it
[00:35:55:850 - 00:35:59:169] **Speaker 1:** as a plane, ah, or that first degree Taylor expansion.
[00:36:00:919 - 00:36:02:080] **Speaker 1:** That's 1st order derivative.
[00:36:02:370 - 00:36:04:120] **Speaker 1:** The 2nd order of derivative, which we need to find
[00:36:04:120 - 00:36:06:580] **Speaker 1:** out to make sure that it's a minima, not maxima,
[00:36:07:040 - 00:36:10:540] **Speaker 1:** uh, is also called the Hessian matrix.
[00:36:11:850 - 00:36:15:409] **Speaker 1:** So it's grad squad, so it's grad F grad F.
[00:36:15:870 - 00:36:18:060] **Speaker 1:** So we end up with a square matrix.
[00:36:21:639 - 00:36:24:360] **Speaker 1:** So grid, squad.
[00:36:25:030 - 00:36:26:909] **Speaker 1:** F of X.
[00:36:28:379 - 00:36:32:280] **Speaker 1:** is equal to A whole bunch of mixed partial derivatives,
[00:36:32:770 - 00:36:35:399] **Speaker 1:** so we'll just write out four of them, so we've
[00:36:35:399 - 00:36:37:530] **Speaker 1:** got D2F.
[00:36:38:419 - 00:36:42:050] **Speaker 1:** Of X P DX1.
[00:36:42:840 - 00:36:43:870] **Speaker 1:** DX1.
[00:36:44:729 - 00:36:47:510] **Speaker 1:** All the way up to D2F.
[00:36:48:479 - 00:36:52:399] **Speaker 1:** Of X by DX1 DXN.
[00:36:56:169 - 00:36:58:159] **Speaker 1:** So that's the first row, and then you go down
[00:36:58:159 - 00:37:03:500] **Speaker 1:** every single um row, and we end up with D2F
[00:37:03:600 - 00:37:04:479] **Speaker 1:** of X.
[00:37:05:360 - 00:37:09:439] **Speaker 1:** By DXN DX1.
[00:37:10:169 - 00:37:11:479] **Speaker 1:** And D2 if.
[00:37:14:010 - 00:37:16:409] **Speaker 1:** B D X N D X N.
[00:37:23:330 - 00:37:24:949] **Speaker 1:** So it's going to be in by N matrix.
[00:37:25:850 - 00:37:28:300] **Speaker 1:** Uh, we can also use it for figuring out the
[00:37:28:300 - 00:37:31:510] **Speaker 1:** second-degree Taylor expansion, which is like a parabolic shape.
[00:37:33:250 - 00:37:36:139] **Speaker 1:** The order of the differentiation doesn't really matter.
[00:37:37:040 - 00:37:40:000] **Speaker 1:** There's a theorem for that, and he's seen as symmetric,
[00:37:40:199 - 00:37:42:330] **Speaker 1:** so we can flip it about the diagonal.
[00:37:42:679 - 00:37:43:679] **Speaker 1:** So we'll transpose.
[00:37:54:969 - 00:38:00:719] **Speaker 1:** So obviously In one free parameter, these collapse to a
[00:38:00:719 - 00:38:03:760] **Speaker 1:** simple derivative of one variable and this is just a
[00:38:03:760 - 00:38:04:600] **Speaker 1:** scalar value.
[00:38:05:040 - 00:38:07:080] **Speaker 1:** So that's what you're most familiar with so far, but
[00:38:07:080 - 00:38:08:879] **Speaker 1:** if you have multiple variables that's where you get these
[00:38:08:879 - 00:38:10:399] **Speaker 1:** vectors and matrices.
[00:38:20:090 - 00:38:21:870] **Speaker 1:** Hopefully everyone's with us still.
[00:38:24:020 - 00:38:26:260] **Speaker 1:** Now some pictures to try and visualise because that's much
[00:38:26:260 - 00:38:26:600] **Speaker 1:** easier.
[00:38:28:159 - 00:38:31:000] **Speaker 1:** So visualising what these object functions look like.
[00:38:32:010 - 00:38:33:850] **Speaker 1:** Uh, I'll, I'll sketch out 3.
[00:38:34:780 - 00:38:37:280] **Speaker 1:** So the basic one would be a convex problem.
[00:38:45:489 - 00:38:49:669] **Speaker 1:** We're on the horizontal axis we've got X, the free
[00:38:49:669 - 00:38:50:270] **Speaker 1:** parameter.
[00:38:51:080 - 00:38:53:520] **Speaker 1:** This is just gonna be an objective function 1 1D.
[00:38:53:959 - 00:38:55:760] **Speaker 1:** so one space X1.
[00:38:56:639 - 00:39:02:350] **Speaker 1:** And the vertical axis represents F of.
[00:39:03:379 - 00:39:06:860] **Speaker 1:** Our free parameter, the objective function evaluated at point X1.
[00:39:08:179 - 00:39:10:419] **Speaker 1:** So convex, um.
[00:39:11:510 - 00:39:12:790] **Speaker 1:** I don't know if I have a good example of
[00:39:12:790 - 00:39:13:110] **Speaker 1:** that.
[00:39:18:350 - 00:39:21:590] **Speaker 1:** Yeah And a multimodal problem.
[00:39:28:350 - 00:39:30:149] **Speaker 1:** So instead of having one convex.
[00:39:31:260 - 00:39:34:520] **Speaker 1:** Uh, shape, we're gonna have many, so.
[00:39:39:389 - 00:39:40:149] **Speaker 1:** Something like that.
[00:39:43:280 - 00:39:43:959] **Speaker 1:** Now.
[00:39:44:889 - 00:39:48:790] **Speaker 1:** We've got 3 low points or lulls in this function.
[00:39:49:989 - 00:39:53:459] **Speaker 1:** And if you remember back in maths, There's a global
[00:39:53:459 - 00:39:54:040] **Speaker 1:** minimum.
[00:40:00:939 - 00:40:03:370] **Speaker 1:** Which is the global minimum.
[00:40:04:469 - 00:40:07:929] **Speaker 1:** And there's also other Mina, which are local.
[00:40:09:270 - 00:40:11:629] **Speaker 1:** So there's a difference between the minimum and minimum.
[00:40:12:949 - 00:40:18:570] **Speaker 1:** Local Mm That's, that's right.
[00:40:20:659 - 00:40:23:850] **Speaker 1:** And we're gonna squeeze another, another example on the side,
[00:40:24:219 - 00:40:24:699] **Speaker 1:** so.
[00:40:25:489 - 00:40:30:110] **Speaker 1:** These are really nice curvy functions that, I mean But
[00:40:30:110 - 00:40:33:679] **Speaker 1:** not Difficult to to sort of find these minima.
[00:40:34:810 - 00:40:40:050] **Speaker 1:** If we had noise maybe in measurement data um or
[00:40:40:050 - 00:40:42:489] **Speaker 1:** anything else, we would have a noisy problem.
[00:40:45:830 - 00:40:47:840] **Speaker 1:** Which is much more realistic and a little bit more
[00:40:47:840 - 00:40:49:620] **Speaker 1:** challenging to solve under.
[00:41:00:969 - 00:41:03:800] **Speaker 1:** So here, overall you can kind of see that it's
[00:41:03:800 - 00:41:07:209] **Speaker 1:** just a convex problem, but it's got many local minima.
[00:41:08:790 - 00:41:10:439] **Speaker 1:** Uh, which could be traps for our.
[00:41:11:600 - 00:41:15:239] **Speaker 1:** Solution process And this is gonna be difficult.
[00:41:18:860 - 00:41:25:320] **Speaker 1:** To find Our optimizer, X star.
[00:41:42:280 - 00:41:44:159] **Speaker 1:** So you can kind of, well, you can think in
[00:41:44:159 - 00:41:45:060] **Speaker 1:** 2D.
[00:41:48:120 - 00:41:50:340] **Speaker 1:** I don't, I don't, can't really think in 3D, but
[00:41:50:340 - 00:41:55:080] **Speaker 1:** in 2D you can imagine that the um, Functions could
[00:41:55:080 - 00:41:57:000] **Speaker 1:** exist along a 2nd parameter X2.
[00:41:58:350 - 00:41:59:449] **Speaker 1:** And that's what we've done here.
[00:41:59:830 - 00:42:03:290] **Speaker 1:** So for convexity, we've got a really basic convex function,
[00:42:03:459 - 00:42:05:580] **Speaker 1:** X12 + X22.
[00:42:05:830 - 00:42:07:250] **Speaker 1:** So it's a parab about the origin.
[00:42:08:270 - 00:42:11:310] **Speaker 1:** So if our objective function is strictly convex, then there's
[00:42:11:310 - 00:42:14:110] **Speaker 1:** only one minimizer, the one that corresponds to the minimum
[00:42:14:110 - 00:42:15:669] **Speaker 1:** value, the global minimum.
[00:42:17:120 - 00:42:20:070] **Speaker 1:** And we can find that just by walking downhill.
[00:42:20:439 - 00:42:22:159] **Speaker 1:** So think of this as some valley, and we're just
[00:42:22:159 - 00:42:22:800] **Speaker 1:** going downhill.
[00:42:24:179 - 00:42:25:540] **Speaker 1:** On the left we've got a surface plot, on the
[00:42:25:540 - 00:42:27:199] **Speaker 1:** right which has got contours.
[00:42:27:459 - 00:42:29:530] **Speaker 1:** Um, I'm sure you can read contour plots.
[00:42:33:000 - 00:42:34:469] **Speaker 1:** So that's a smooth function.
[00:42:35:229 - 00:42:37:919] **Speaker 1:** And we can also look at convexity of sets, so
[00:42:37:919 - 00:42:40:620] **Speaker 1:** discrete points within our parameter space.
[00:42:41:120 - 00:42:44:560] **Speaker 1:** So the set X is convex for any two points
[00:42:44:560 - 00:42:46:800] **Speaker 1:** within the set, the set contains the entire line segment
[00:42:46:800 - 00:42:47:699] **Speaker 1:** between those two points.
[00:42:49:239 - 00:42:51:399] **Speaker 1:** So much easier with a Peter.
[00:42:56:399 - 00:42:57:939] **Speaker 1:** Sort of like, like a tooth.
[00:43:01:649 - 00:43:03:070] **Speaker 1:** I'll sit X.
[00:43:08:639 - 00:43:12:520] **Speaker 1:** And we've just said that our set is convex.
[00:43:13:489 - 00:43:15:770] **Speaker 1:** If for any two points within the set, so if
[00:43:15:770 - 00:43:18:389] **Speaker 1:** we take two spots within this domain.
[00:43:19:409 - 00:43:23:409] **Speaker 1:** The set contains the entire line segment between those two
[00:43:23:409 - 00:43:23:570] **Speaker 1:** points.
[00:43:23:649 - 00:43:26:290] **Speaker 1:** So if we draw a line between two points, we're
[00:43:26:290 - 00:43:27:209] **Speaker 1:** still within the set.
[00:43:28:010 - 00:43:30:399] **Speaker 1:** Do you think this would be a convex or non-convex
[00:43:30:399 - 00:43:30:610] **Speaker 1:** set?
[00:43:44:689 - 00:43:47:570] **Speaker 1:** What happens if we draw 2 points?
[00:43:48:459 - 00:43:51:679] **Speaker 1:** And these upper areas, starting to look like a face,
[00:43:51:699 - 00:43:51:939] **Speaker 1:** but.
[00:43:52:780 - 00:43:54:379] **Speaker 1:** We've got a line.
[00:43:55:770 - 00:43:59:699] **Speaker 1:** Drawn between the two, and this line lies outside of
[00:43:59:699 - 00:44:02:780] **Speaker 1:** our set, so this is going to be non-convex.
[00:44:10:810 - 00:44:12:939] **Speaker 1:** If you think of a circle, that's gonna be convex.
[00:44:16:010 - 00:44:18:209] **Speaker 1:** Now, the convict's hull.
[00:44:20:169 - 00:44:23:939] **Speaker 1:** Of a set is the set of all convex combinations
[00:44:23:939 - 00:44:26:280] **Speaker 1:** of the points within our set X.
[00:44:27:120 - 00:44:28:719] **Speaker 1:** So if we had a whole bunch of points.
[00:44:33:330 - 00:44:37:489] **Speaker 1:** And the convex hull contains all of the convex combinations
[00:44:37:489 - 00:44:39:370] **Speaker 1:** of those points.
[00:44:41:520 - 00:44:44:169] **Speaker 1:** It's going to essentially wrap around the outer edge.
[00:44:44:520 - 00:44:46:189] **Speaker 1:** And a nice way to think of it is if
[00:44:46:189 - 00:44:48:679] **Speaker 1:** you had a rubber band and those little nails that
[00:44:48:679 - 00:44:51:120] **Speaker 1:** you put into the wood and you put the rubber
[00:44:51:120 - 00:44:54:500] **Speaker 1:** band around the outside, it just encompasses all.
[00:45:05:149 - 00:45:07:110] **Speaker 1:** So this is going to be defined as the convicts.
[00:45:08:409 - 00:45:09:469] **Speaker 1:** How of.
[00:45:10:260 - 00:45:10:739] **Speaker 0:** Points.
[00:45:16:629 - 00:45:16:979] **Speaker 1:** Cool.
[00:45:37:169 - 00:45:42:870] **Speaker 1:** So convexity of smooth functions um of sets, and now
[00:45:42:870 - 00:45:44:239] **Speaker 1:** if we just look at a function.
[00:45:45:139 - 00:45:49:780] **Speaker 1:** In general, So our sum function, objective function F, uh,
[00:45:49:790 - 00:45:53:100] **Speaker 1:** which maps from some input set in X.
[00:45:54:149 - 00:45:56:469] **Speaker 1:** There's gonna be convicts, wasn't it.
[00:45:57:389 - 00:45:58:810] **Speaker 1:** Any of these conditions are met.
[00:45:59:110 - 00:46:01:949] **Speaker 1:** So we're gonna look at 3 ways of determining whether
[00:46:01:949 - 00:46:04:010] **Speaker 1:** a function is convex.
[00:46:06:959 - 00:46:07:379] **Speaker 1:** Good fun.
[00:46:08:709 - 00:46:11:389] **Speaker 1:** So if we consider a function.
[00:46:18:270 - 00:46:19:449] **Speaker 1:** That varies the next one.
[00:46:24:649 - 00:46:26:280] **Speaker 1:** And on the vertical we've got.
[00:46:27:489 - 00:46:28:330] **Speaker 1:** F of X1.
[00:46:30:100 - 00:46:31:189] **Speaker 1:** And.
[00:46:33:520 - 00:46:38:080] **Speaker 1:** Our function Has some bumps.
[00:46:39:469 - 00:46:41:889] **Speaker 1:** And the set that we're analysing.
[00:46:43:530 - 00:46:46:070] **Speaker 1:** Is across some interval X.
[00:46:51:040 - 00:46:54:429] **Speaker 1:** The epigraph, which is the space above the line.
[00:46:58:719 - 00:47:00:610] **Speaker 1:** Needs to be uh convex.
[00:47:03:250 - 00:47:08:070] **Speaker 0:** Is this Epigraph or that region above the line, convex.
[00:47:13:800 - 00:47:14:840] **Speaker 1:** No, that's not.
[00:47:23:399 - 00:47:26:320] **Speaker 1:** So we can draw 2 points.
[00:47:27:620 - 00:47:30:580] **Speaker 1:** On our curve that lie outside the epigraph.
[00:47:31:239 - 00:47:34:550] **Speaker 1:** So it's non Convex.
[00:47:47:500 - 00:47:50:919] **Speaker 1:** And the next one requires a few minutes to to
[00:47:50:929 - 00:47:53:750] **Speaker 1:** to talk over, so I won't start that today.
[00:47:54:929 - 00:47:58:879] **Speaker 1:** Um Just a reminder, we've got the labs this afternoon.
[00:48:00:090 - 00:48:03:010] **Speaker 1:** We're going through lab 4, which is using the heat
[00:48:03:010 - 00:48:06:090] **Speaker 1:** transfer in solids physics interface which you'll use for your
[00:48:06:090 - 00:48:06:879] **Speaker 1:** um assignment.
[00:48:07:010 - 00:48:09:189] **Speaker 1:** So make sure you have a go at that.
[00:48:11:469 - 00:48:15:290] **Speaker 1:** And ask if you're stuck with anything in the labs.
[00:48:16:370 - 00:48:20:459] **Speaker 1:** I've got a meeting At 1 for 20 or 30
[00:48:20:459 - 00:48:22:510] **Speaker 1:** minutes, but I'll at least be there at the start
[00:48:22:510 - 00:48:25:149] **Speaker 1:** to try and kick people out that aren't in 302.
[00:48:25:889 - 00:48:29:179] **Speaker 1:** Um I generally make sure that there's at least a
[00:48:29:179 - 00:48:30:100] **Speaker 1:** few computers spare.
[00:48:30:260 - 00:48:32:520] **Speaker 1:** I don't like to just clear the whole room because
[00:48:33:100 - 00:48:35:340] **Speaker 1:** not everyone comes to the labs, or not everyone comes
[00:48:35:340 - 00:48:36:820] **Speaker 1:** to the lectures and not everyone comes to the labs,
[00:48:36:860 - 00:48:38:060] **Speaker 1:** but I do make sure that there are a few
[00:48:38:060 - 00:48:40:620] **Speaker 1:** spare computers there, but let me know if there aren't
[00:48:40:620 - 00:48:41:719] **Speaker 1:** during the lab sessions.
[00:48:43:139 - 00:48:46:219] **Speaker 1:** And if you come to the later lab sessions, you'll
[00:48:46:219 - 00:48:48:199] **Speaker 1:** have more attention if you're particularly stuck.
[00:48:50:239 - 00:48:51:739] **Speaker 1:** Yeah, just a small note on the labs.
[00:48:51:919 - 00:48:52:199] **Speaker 1:** Cool.
[00:48:52:399 - 00:48:54:439] **Speaker 1:** All right, so we'll see you there this afternoon.
[00:49:12:540 - 00:49:12:550] **Speaker 0:** S.
[00:49:40:870 - 00:49:41:590] **Speaker 0:** Jesus.
[00:49:46:310 - 00:49:46:580] **Speaker 0:** please.
[00:49:53:370 - 00:49:53:379] **Speaker 0:** Yes.
[00:49:56:909 - 00:49:57:820] **Speaker 0:** Yeah.
[00:50:06:389 - 00:50:14:459] **Speaker 0:** I You don't want that.
[00:50:19:129 - 00:50:35:320] **Speaker 0:** Yes did you not have.
[00:54:22:610 - 00:54:24:030] **Speaker 0:** Yeah Mars.
[00:54:26:020 - 00:54:26:110] **Speaker 0:** Really

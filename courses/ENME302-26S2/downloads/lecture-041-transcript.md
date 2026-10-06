# ENME302-26S2 Lecture 41 native Echo transcript

Date: October 5, 2026 12:00pm-12:55pm
Transcript type: native Echo automated transcript.

[00:00:00:970 - 00:00:02:170] **Speaker 0:** Yeah.
[00:00:04:489 - 00:00:04:500] **Speaker 0:** I.
[00:00:12:130 - 00:00:14:380] **Speaker 0:** Yeah It.
[00:00:25:770 - 00:00:27:940] **Speaker 0:** I design.
[00:00:37:540 - 00:00:40:860] **Speaker 0:** 500 by 3 and to me it's the size of
[00:00:40:860 - 00:00:40:880] **Speaker 0:** the.
[00:00:45:400 - 00:00:45:520] **Speaker 0:** this.
[00:00:50:189 - 00:00:52:860] **Speaker 0:** I I remember looking at you.
[00:00:56:369 - 00:01:10:900] **Speaker 0:** And this.
[00:01:25:949 - 00:01:27:510] **Speaker 1:** Cool, uh, good afternoon.
[00:01:28:110 - 00:01:29:000] **Speaker 1:** We'll make a start.
[00:01:29:790 - 00:01:31:440] **Speaker 1:** So I'll just go through quiz 5.
[00:01:32:500 - 00:01:36:019] **Speaker 1:** As usual, it's the last quiz of our course.
[00:01:45:309 - 00:01:47:410] **Speaker 1:** I don't know why it's a bit smaller, but.
[00:01:50:559 - 00:01:55:879] **Speaker 1:** Um, all right, so quiz 5, we looked at chapters
[00:01:55:879 - 00:01:57:559] **Speaker 1:** 6 and 12 and lab 5.
[00:01:57:839 - 00:01:59:860] **Speaker 1:** So the average was about 89%, so that's good.
[00:02:00:199 - 00:02:02:279] **Speaker 1:** Um, there wasn't quite as many attempts.
[00:02:02:559 - 00:02:04:910] **Speaker 1:** I think a few people missed out on the quiz
[00:02:04:910 - 00:02:05:430] **Speaker 1:** last week.
[00:02:05:720 - 00:02:07:239] **Speaker 1:** Too much excitement with RoboCup.
[00:02:07:370 - 00:02:08:500] **Speaker 1:** So how did Robocup go?
[00:02:09:460 - 00:02:10:089] **Speaker 1:** Was it fun?
[00:02:10:220 - 00:02:12:179] **Speaker 1:** As in, yeah, yeah, I didn't make it to the
[00:02:12:179 - 00:02:14:740] **Speaker 1:** finals, but it was good.
[00:02:14:940 - 00:02:17:020] **Speaker 1:** Did someone win, I suppose, but yeah.
[00:02:17:740 - 00:02:18:899] **Speaker 1:** Um, good on them.
[00:02:18:979 - 00:02:21:259] **Speaker 1:** I think there's still like report writing or something afterwards,
[00:02:21:339 - 00:02:24:220] **Speaker 1:** which takes a bit of time, um, for, for you
[00:02:24:220 - 00:02:24:960] **Speaker 1:** guys this week.
[00:02:26:139 - 00:02:27:770] **Speaker 1:** But yeah, remember we've got assignment too.
[00:02:28:119 - 00:02:32:419] **Speaker 1:** Um, I've posted this morning, so that was just recap
[00:02:32:419 - 00:02:36:059] **Speaker 1:** of this wall of text of, of that should be
[00:02:36:059 - 00:02:37:580] **Speaker 1:** everything that you really need for the assignment, but if
[00:02:37:580 - 00:02:40:460] **Speaker 1:** you're particularly stuck, I've got, um, office hours as well
[00:02:40:460 - 00:02:42:720] **Speaker 1:** this afternoon after this lecture for a couple of hours.
[00:02:42:770 - 00:02:44:660] **Speaker 1:** I'll ask Theo to come along as well in case
[00:02:44:660 - 00:02:46:220] **Speaker 1:** we get lots of questions, but I don't know if
[00:02:46:220 - 00:02:48:339] **Speaker 1:** we'll have that many people, but we'll just see how
[00:02:48:339 - 00:02:48:919] **Speaker 1:** it goes.
[00:02:49:800 - 00:02:51:330] **Speaker 1:** Otherwise, the Thursday labs.
[00:02:53:070 - 00:03:00:270] **Speaker 1:** So Question 1 and 2 was done well.
[00:03:00:399 - 00:03:01:830] **Speaker 1:** Question 3 mostly done well.
[00:03:01:990 - 00:03:06:070] **Speaker 1:** So I'll just quickly go through these solutions for completeness.
[00:03:06:919 - 00:03:08:839] **Speaker 1:** So the backward in time and space, that was that
[00:03:08:839 - 00:03:10:119] **Speaker 1:** first order in time method.
[00:03:10:360 - 00:03:12:080] **Speaker 1:** So backward in time and forward in time was just
[00:03:12:080 - 00:03:13:339] **Speaker 1:** that one-sided difference.
[00:03:13:759 - 00:03:17:080] **Speaker 1:** And central difference in space was second order accuracy.
[00:03:17:169 - 00:03:19:169] **Speaker 1:** So we had 2nd order in space.
[00:03:21:669 - 00:03:26:589] **Speaker 1:** The discretization here, we have backward in time centre and
[00:03:26:589 - 00:03:26:750] **Speaker 1:** space.
[00:03:26:789 - 00:03:28:729] **Speaker 1:** So because it's backward in time it's gonna be implicit
[00:03:28:729 - 00:03:32:240] **Speaker 1:** we're evaluating the uh dependent variable the next time in
[00:03:32:240 - 00:03:33:389] **Speaker 1:** plus one.
[00:03:34:080 - 00:03:35:490] **Speaker 1:** So that's going to be.
[00:03:36:320 - 00:03:38:850] **Speaker 1:** Uh, we'll just let it fill it in for us.
[00:03:39:130 - 00:03:40:110] **Speaker 1:** Don't have to search.
[00:03:40:690 - 00:03:42:509] **Speaker 1:** Um, so this one, so we've got N + 1
[00:03:42:850 - 00:03:45:800] **Speaker 1:** and we've got this time derivative in first order one
[00:03:45:800 - 00:03:46:550] **Speaker 1:** side of difference.
[00:03:47:949 - 00:03:50:589] **Speaker 1:** So I think most of you got that one as
[00:03:50:589 - 00:03:51:130] **Speaker 1:** well.
[00:03:52:479 - 00:03:55:009] **Speaker 1:** And the last one was looking at console and an
[00:03:55:009 - 00:03:55:990] **Speaker 1:** optimisation problem.
[00:03:57:589 - 00:03:59:740] **Speaker 1:** So this was a bit more fun.
[00:04:00:110 - 00:04:01:850] **Speaker 1:** So we had uh.
[00:04:02:589 - 00:04:05:289] **Speaker 1:** Poisson equation that we're solving, so our governing equation is
[00:04:05:289 - 00:04:05:839] **Speaker 1:** given here.
[00:04:06:179 - 00:04:08:820] **Speaker 1:** We have some source being applied and some radius of
[00:04:08:820 - 00:04:09:660] **Speaker 1:** our membrane.
[00:04:10:809 - 00:04:15:250] **Speaker 1:** And we've applied some uh non-uniform diffusion coefficient tau.
[00:04:16:130 - 00:04:18:950] **Speaker 1:** So tau is some spatially dependent stiffness of the membrane
[00:04:19:450 - 00:04:20:928] **Speaker 1:** and scales with tau naught.
[00:04:21:209 - 00:04:22:649] **Speaker 1:** So we're trying to figure out what tau n was
[00:04:22:649 - 00:04:27:809] **Speaker 1:** using optimisation procedure by minimising the discrepancy between an observed
[00:04:27:809 - 00:04:29:470] **Speaker 1:** peak of.
[00:04:30:739 - 00:04:34:250] **Speaker 1:** 5 mil and that that we calculate in our simulation.
[00:04:34:339 - 00:04:37:350] **Speaker 1:** So I'll just go through the steps.
[00:04:42:049 - 00:04:44:609] **Speaker 1:** So one that I prepared earlier, so you don't have
[00:04:44:609 - 00:04:45:869] **Speaker 1:** to watch me do this.
[00:04:48:920 - 00:04:51:339] **Speaker 1:** So, I've created a, a structured mesh.
[00:04:52:230 - 00:04:54:089] **Speaker 1:** So I guess we'll just go from top to bottom
[00:04:54:089 - 00:04:54:109] **Speaker 1:** briefly.
[00:04:55:399 - 00:04:59:350] **Speaker 1:** So parameters that we we've been asked has a radius
[00:04:59:350 - 00:05:03:000] **Speaker 1:** of 80 mils and a force being applied of 25.
[00:05:04:220 - 00:05:04:950] **Speaker 1:** Newtons per metre cube.
[00:05:05:029 - 00:05:07:190] **Speaker 1:** So really helpful to include units, otherwise, you'll be out
[00:05:07:190 - 00:05:08:809] **Speaker 1:** by 3 orders of magnitude.
[00:05:09:230 - 00:05:10:350] **Speaker 1:** If you had 80 metres.
[00:05:11:829 - 00:05:15:109] **Speaker 1:** And tau is unknown, so we'll just give it initial
[00:05:15:109 - 00:05:15:690] **Speaker 1:** guess.
[00:05:16:029 - 00:05:18:559] **Speaker 1:** And UMax is prescribed with 5 mL.
[00:05:21:290 - 00:05:23:850] **Speaker 1:** And in here I've just said as the number of
[00:05:23:850 - 00:05:27:230] **Speaker 1:** um mesh elements along each, each of these edges.
[00:05:27:970 - 00:05:32:089] **Speaker 1:** I've created an analytical function to describe the stiffness uh
[00:05:32:089 - 00:05:34:609] **Speaker 1:** value tau varies in X and Y.
[00:05:35:540 - 00:05:37:700] **Speaker 1:** And what we can do is visualise that.
[00:05:38:220 - 00:05:40:820] **Speaker 1:** So that's what we've done down here.
[00:05:43:529 - 00:05:55:470] **Speaker 1:** So Um, this is just plotting tau of X and
[00:05:55:470 - 00:05:55:970] **Speaker 1:** Y.
[00:05:57:559 - 00:06:03:059] **Speaker 1:** And Next step is to define our maximum value within
[00:06:03:059 - 00:06:03:619] **Speaker 1:** the domain.
[00:06:03:779 - 00:06:05:670] **Speaker 1:** So we can use the max the maximum operator.
[00:06:05:779 - 00:06:06:420] **Speaker 1:** So that's under.
[00:06:07:859 - 00:06:11:940] **Speaker 1:** Non-local couplings, Max, and we've set that up throughout our
[00:06:11:940 - 00:06:12:600] **Speaker 1:** whole domain.
[00:06:12:859 - 00:06:15:339] **Speaker 1:** Cause we've got 5 local regions, we need to set
[00:06:15:339 - 00:06:17:859] **Speaker 1:** that it's searching throughout the whole domain, not just one
[00:06:17:859 - 00:06:18:440] **Speaker 1:** of those.
[00:06:21:480 - 00:06:24:799] **Speaker 1:** And the Poisson equation, it's really helpful just to expand
[00:06:24:799 - 00:06:26:649] **Speaker 1:** that equation form just to check that we're solving what
[00:06:26:649 - 00:06:27:209] **Speaker 1:** we expect.
[00:06:27:329 - 00:06:29:529] **Speaker 1:** So you could equally use the coefficient form and match
[00:06:29:529 - 00:06:31:769] **Speaker 1:** up the coefficients as you like, uh, but here I
[00:06:31:769 - 00:06:36:910] **Speaker 1:** just use the son and I've set the dependent variable
[00:06:36:910 - 00:06:39:809] **Speaker 1:** to metres and the source term to Newtons per metre
[00:06:39:809 - 00:06:40:299] **Speaker 1:** cubed.
[00:06:41:040 - 00:06:43:709] **Speaker 1:** So I did notice a few people didn't quite get
[00:06:43:709 - 00:06:44:709] **Speaker 1:** the units right.
[00:06:46:829 - 00:06:49:529] **Speaker 1:** So I'll just briefly go through how.
[00:06:53:079 - 00:06:53:980] **Speaker 1:** How we can do that.
[00:06:56:980 - 00:07:01:790] **Speaker 1:** So I've got 10, of course, you've only got one
[00:07:01:790 - 00:07:02:200] **Speaker 1:** screen.
[00:07:02:470 - 00:07:03:459] **Speaker 1:** That's very helpful.
[00:07:07:140 - 00:07:07:600] **Speaker 1:** Yeah.
[00:07:08:239 - 00:07:08:970] **Speaker 1:** So we've got 2.
[00:07:10:190 - 00:07:11:720] **Speaker 1:** Dot towel.
[00:07:13:010 - 00:07:15:149] **Speaker 1:** Grad U equal to F.
[00:07:15:989 - 00:07:17:269] **Speaker 1:** And the units for F.
[00:07:18:809 - 00:07:20:630] **Speaker 1:** Is Newtons per metre cubed.
[00:07:21:899 - 00:07:25:269] **Speaker 1:** Um, so that means that the left-hand side also has
[00:07:25:269 - 00:07:26:989] **Speaker 1:** to have the same units to be consistent.
[00:07:27:980 - 00:07:33:760] **Speaker 1:** The units of D by D X.
[00:07:34:760 - 00:07:36:119] **Speaker 1:** There's 1 over metres.
[00:07:36:940 - 00:07:41:130] **Speaker 1:** Tell is unknown.
[00:07:42:109 - 00:07:43:820] **Speaker 1:** And grab you.
[00:07:44:880 - 00:07:46:519] **Speaker 1:** Is DU by DX.
[00:07:48:679 - 00:07:52:200] **Speaker 1:** Which is metres over metres, so it hasn't, hasn't got
[00:07:52:200 - 00:07:52:799] **Speaker 1:** any units.
[00:07:54:269 - 00:07:56:630] **Speaker 1:** So if we rearrange, we've got Newtons per metre cubed
[00:07:57:070 - 00:07:58:700] **Speaker 1:** multiplied by metres.
[00:07:58:890 - 00:08:01:950] **Speaker 1:** So tau has to be Newtons per metre squared.
[00:08:02:149 - 00:08:05:350] **Speaker 1:** So it's essentially like a pressure force per per unit
[00:08:05:350 - 00:08:05:730] **Speaker 1:** area.
[00:08:08:309 - 00:08:11:429] **Speaker 1:** And Yeah.
[00:08:13:209 - 00:08:16:250] **Speaker 1:** That will hopefully help some to the laptop.
[00:08:19:140 - 00:08:21:220] **Speaker 1:** So we've defined our governing equations.
[00:08:21:339 - 00:08:23:660] **Speaker 1:** We've got our boundary conditions constraining the problem.
[00:08:24:000 - 00:08:26:540] **Speaker 1:** So if you didn't apply the directly boundary condition, it
[00:08:26:540 - 00:08:29:920] **Speaker 1:** would not have a unique solution because the default for
[00:08:29:920 - 00:08:32:780] **Speaker 1:** these boundary conditions is zero flux, which means that the
[00:08:32:780 - 00:08:35:219] **Speaker 1:** gradient at the boundary is zero.
[00:08:35:820 - 00:08:37:140] **Speaker 1:** And there's an infinite number of solutions.
[00:08:37:219 - 00:08:41:640] **Speaker 1:** So arbitrary elevation would match that that boundary condition.
[00:08:42:520 - 00:08:45:140] **Speaker 1:** So we've constrained the problem with these direct clay boundary
[00:08:45:140 - 00:08:47:780] **Speaker 1:** conditions of zero on the, the, uh, circumference.
[00:08:48:830 - 00:08:50:659] **Speaker 1:** The initial values don't really matter too much.
[00:08:50:739 - 00:08:52:750] **Speaker 1:** It's sort of just like the initial guess for this
[00:08:52:750 - 00:08:54:429] **Speaker 1:** case because it's in a city-state.
[00:08:56:049 - 00:08:59:690] **Speaker 1:** Our mesh here is a structured grid, the OH mesh.
[00:09:01:049 - 00:09:04:169] **Speaker 1:** I first checked that the mesh resolution was accurate by
[00:09:04:169 - 00:09:05:250] **Speaker 1:** doing a parametric sweep.
[00:09:05:429 - 00:09:07:770] **Speaker 1:** So that's what we did in lab, 3, I think
[00:09:07:770 - 00:09:09:099] **Speaker 1:** it was, lab 2 or 3.
[00:09:09:570 - 00:09:13:690] **Speaker 1:** And I've used the general optimisation to explore that tail
[00:09:13:690 - 00:09:14:309] **Speaker 1:** space.
[00:09:14:880 - 00:09:17:479] **Speaker 1:** So I've used Bobby car, uh, as I'm more familiar
[00:09:17:479 - 00:09:20:169] **Speaker 1:** with that set of optimality tolerance that you might want
[00:09:20:169 - 00:09:22:059] **Speaker 1:** to refine as well to see if that impacts the
[00:09:22:059 - 00:09:22:419] **Speaker 1:** result.
[00:09:22:609 - 00:09:25:489] **Speaker 1:** That essentially is measuring the how close it is to
[00:09:25:489 - 00:09:26:669] **Speaker 1:** the, the minima.
[00:09:27:479 - 00:09:31:320] **Speaker 1:** We looked at those steepest descent methods in class in
[00:09:31:320 - 00:09:31:869] **Speaker 1:** chapter 12.
[00:09:31:960 - 00:09:36:159] **Speaker 1:** So this is essentially adjusting the epsilon value for for
[00:09:36:159 - 00:09:37:260] **Speaker 1:** finding the optimum solution.
[00:09:38:349 - 00:09:40:950] **Speaker 1:** Setting a maximum number of model evaluations, we don't go
[00:09:40:950 - 00:09:42:250] **Speaker 1:** on to infinity.
[00:09:43:150 - 00:09:46:789] **Speaker 1:** The objective function here is defined as, as we had
[00:09:46:789 - 00:09:47:469] **Speaker 1:** in uh.
[00:09:49:460 - 00:09:52:150] **Speaker 1:** as the maximum value of the displacement field.
[00:09:52:590 - 00:09:55:070] **Speaker 1:** So we use compo.max1U.
[00:09:56:150 - 00:09:58:590] **Speaker 1:** We use compound because it's outside of this component.
[00:09:58:710 - 00:09:59:830] **Speaker 1:** So we have to call comp.
[00:10:00:669 - 00:10:03:539] **Speaker 1:** max and then evaluating the dependent variable you throughout that
[00:10:03:539 - 00:10:07:070] **Speaker 1:** field, taking the maximum value and then subtracting off the
[00:10:07:070 - 00:10:08:210] **Speaker 1:** max that we were prescribed.
[00:10:09:000 - 00:10:10:400] **Speaker 1:** And we're squaring this, so it's sort of like a
[00:10:10:400 - 00:10:11:190] **Speaker 1:** quadrat across.
[00:10:12:630 - 00:10:14:989] **Speaker 1:** The control variables that we're adjusting is tau 0, starting
[00:10:14:989 - 00:10:17:109] **Speaker 1:** with some initial guess of one, Pascal.
[00:10:17:760 - 00:10:19:549] **Speaker 1:** Uh, the scale is on the order of 1, giving
[00:10:19:549 - 00:10:21:650] **Speaker 1:** a lower and upper bound of 0.1 and 100.
[00:10:22:780 - 00:10:25:440] **Speaker 1:** So the next step is to solve or compute that.
[00:10:28:500 - 00:10:30:710] **Speaker 1:** And it goes through and solves for each of these
[00:10:30:710 - 00:10:31:909] **Speaker 1:** tau naught values.
[00:10:33:520 - 00:10:35:469] **Speaker 1:** And hopefully reduces the objective.
[00:10:37:400 - 00:10:41:260] **Speaker 1:** So again, the objective is that difference between the modelled
[00:10:41:510 - 00:10:44:190] **Speaker 1:** and the expected value, and we want this to reduce
[00:10:44:190 - 00:10:48:580] **Speaker 1:** down to zero, ideally within machine precision, but that's not
[00:10:48:580 - 00:10:49:390] **Speaker 1:** always going to be the case.
[00:10:49:469 - 00:10:52:669] **Speaker 1:** It depends how accurately our model can represent the true
[00:10:52:669 - 00:10:53:250] **Speaker 1:** physics.
[00:10:54:619 - 00:10:57:400] **Speaker 1:** And Tawknot is still changing.
[00:11:00:239 - 00:11:02:750] **Speaker 1:** And we're expecting about 16.6.
[00:11:08:299 - 00:11:11:530] **Speaker 1:** And can I speak even longer on this?
[00:11:12:070 - 00:11:12:929] **Speaker 1:** Um.
[00:11:14:210 - 00:11:15:289] **Speaker 1:** While that solves.
[00:11:17:929 - 00:11:20:510] **Speaker 1:** So I made the I think the tolerance on the
[00:11:21:159 - 00:11:23:450] **Speaker 1:** full marks was about 1% and then it was about
[00:11:23:450 - 00:11:25:729] **Speaker 1:** 5% for half credit.
[00:11:25:849 - 00:11:27:489] **Speaker 1:** And then if you got the units wrong, I think
[00:11:27:489 - 00:11:29:510] **Speaker 1:** you got 4 out of 5, something like that.
[00:11:29:929 - 00:11:31:320] **Speaker 1:** And then if you only got the units, I think
[00:11:31:320 - 00:11:32:909] **Speaker 1:** you got 1 out of 5.
[00:11:33:719 - 00:11:34:900] **Speaker 1:** In case you were wondering.
[00:11:37:440 - 00:11:38:289] **Speaker 1:** And we're getting there.
[00:11:38:570 - 00:11:41:909] **Speaker 1:** So it's very, I guess it's dependent on where you
[00:11:41:909 - 00:11:42:390] **Speaker 1:** start.
[00:11:42:729 - 00:11:44:969] **Speaker 1:** So a good idea might be to do your parametric
[00:11:44:969 - 00:11:47:130] **Speaker 1:** sweep on town n just to get a feel for
[00:11:47:130 - 00:11:50:710] **Speaker 1:** what impact the stiffness has on the maximum displacement.
[00:11:51:289 - 00:11:53:090] **Speaker 1:** So that was one of the, the hints here.
[00:11:53:369 - 00:11:55:690] **Speaker 1:** And then once you find a close enough solution, you
[00:11:55:690 - 00:11:58:090] **Speaker 1:** could start your optimizer at that location and it will
[00:11:58:090 - 00:12:00:429] **Speaker 1:** converge a lot quicker than what I've, what I've shown
[00:12:00:770 - 00:12:02:869] **Speaker 1:** and endured through today.
[00:12:03:409 - 00:12:06:869] **Speaker 1:** So we're at 16.6, so that's, that's reassuring.
[00:12:09:320 - 00:12:10:700] **Speaker 1:** All right, any questions on?
[00:12:11:489 - 00:12:12:989] **Speaker 1:** This question or the quiz.
[00:12:15:320 - 00:12:16:219] **Speaker 1:** Quiz 5.
[00:12:17:570 - 00:12:19:760] **Speaker 1:** No salmon, yeah.
[00:12:22:809 - 00:12:27:770] **Speaker 1:** Um, so, uh, very soon, so I'm gonna upload all
[00:12:27:770 - 00:12:29:309] **Speaker 1:** the previous.
[00:12:30:479 - 00:12:34:530] **Speaker 1:** Model, like the previous exams and model answers and this,
[00:12:34:729 - 00:12:37:489] **Speaker 1:** um, it is actually the same as last year's for
[00:12:37:489 - 00:12:38:289] **Speaker 1:** the formula sheet.
[00:12:38:900 - 00:12:42:520] **Speaker 1:** Um I'll probably sort that on Wednesday, but I'll introduce
[00:12:42:520 - 00:12:45:840] **Speaker 1:** it and talk about it on Thursday, but you'll have
[00:12:45:840 - 00:12:48:000] **Speaker 1:** it ahead of the exam, so you, you know where
[00:12:48:000 - 00:12:48:489] **Speaker 1:** to look.
[00:12:48:760 - 00:12:50:679] **Speaker 1:** And I brought it along today because we're going through
[00:12:50:679 - 00:12:53:309] **Speaker 1:** chapter 10 and I'm not gonna get you to memorise
[00:12:53:309 - 00:12:53:979] **Speaker 1:** all these.
[00:12:54:989 - 00:12:56:630] **Speaker 1:** 2D finite element formulas.
[00:12:57:030 - 00:12:58:650] **Speaker 1:** Oh, you can't see, of course.
[00:13:04:950 - 00:13:05:640] **Speaker 1:** The formula sheet.
[00:13:05:909 - 00:13:08:309] **Speaker 1:** So this, these 2D, I don't want you to memorise
[00:13:08:309 - 00:13:08:750] **Speaker 1:** all of that.
[00:13:08:979 - 00:13:12:429] **Speaker 1:** That's what we can uh hand off to the the
[00:13:12:429 - 00:13:13:109] **Speaker 1:** formula sheet.
[00:13:15:750 - 00:13:16:479] **Speaker 1:** Any other cruise?
[00:13:18:919 - 00:13:21:099] **Speaker 1:** Any queries on the assignment or anything else?
[00:13:26:989 - 00:13:27:489] **Speaker 1:** Silence.
[00:13:27:650 - 00:13:30:349] **Speaker 1:** Hopefully you've had a good weekend and got some sunshine,
[00:13:30:969 - 00:13:32:609] **Speaker 1:** but I don't, I don't know.
[00:13:32:729 - 00:13:34:169] **Speaker 1:** I got for a walk, I got for a hike,
[00:13:34:210 - 00:13:34:770] **Speaker 1:** so that was good.
[00:13:35:880 - 00:13:39:950] **Speaker 1:** Um So chapter 10, we're going to continue with finite
[00:13:39:950 - 00:13:40:549] **Speaker 1:** elements.
[00:13:41:890 - 00:13:43:770] **Speaker 1:** Because we're having so much fun on 1D, we're gonna
[00:13:43:770 - 00:13:44:659] **Speaker 1:** extend it to 2D.
[00:13:45:400 - 00:13:48:679] **Speaker 1:** This is, yeah, more maths and like arithmetic.
[00:13:49:280 - 00:13:50:299] **Speaker 1:** Don't get too scared.
[00:13:50:400 - 00:13:52:359] **Speaker 1:** We're just sort of going to try and give a
[00:13:52:359 - 00:13:53:409] **Speaker 1:** bit of an overview.
[00:13:53:630 - 00:13:55:359] **Speaker 1:** And really, we're just using console to do 2D and
[00:13:55:359 - 00:13:56:559] **Speaker 1:** 3D fun elements for us.
[00:13:56:760 - 00:13:59:059] **Speaker 1:** Uh, we're not really doing it too much in class.
[00:14:00:669 - 00:14:02:750] **Speaker 1:** Um, but we just covered some of the, some of
[00:14:02:750 - 00:14:04:590] **Speaker 1:** the basics of the shape functions and things like that.
[00:14:06:659 - 00:14:10:739] **Speaker 1:** So Multiple dimensions, as you can imagine, it's just expanding
[00:14:10:739 - 00:14:12:919] **Speaker 1:** and off to Y and the Z coordinates.
[00:14:13:419 - 00:14:15:919] **Speaker 1:** So we've got the same principles as we did for
[00:14:15:919 - 00:14:18:020] **Speaker 1:** the 1D problems and 2D and 3D.
[00:14:18:520 - 00:14:21:950] **Speaker 1:** It's a little bit more involved for the calculus, so
[00:14:22:239 - 00:14:26:080] **Speaker 1:** more bookkeeping and the code is actually quite a bit
[00:14:26:080 - 00:14:27:109] **Speaker 1:** more complex to solve.
[00:14:27:159 - 00:14:29:270] **Speaker 1:** This is why we get console or some other solver
[00:14:29:270 - 00:14:30:059] **Speaker 1:** to do it for us.
[00:14:31:210 - 00:14:32:049] **Speaker 1:** We can't do everything.
[00:14:36:140 - 00:14:36:150] **Speaker 1:** So.
[00:14:39:109 - 00:14:41:309] **Speaker 1:** We're going to look at the key differences and then
[00:14:41:309 - 00:14:41:900] **Speaker 1:** use console.
[00:14:43:039 - 00:14:43:270] **Speaker 1:** So disization.
[00:14:43:549 - 00:14:45:669] **Speaker 1:** So now instead of the one-dimensional line, we've got a
[00:14:45:669 - 00:14:48:960] **Speaker 1:** two-dimensional shape, we could have a triangle, quads, etc.
[00:14:49:390 - 00:14:51:530] **Speaker 1:** The example here I've got is a is a triangle.
[00:14:52:070 - 00:14:54:630] **Speaker 1:** And we've got the defendant variable being evaluated each node.
[00:14:54:869 - 00:14:56:650] **Speaker 1:** So maybe it's you 12 and 3.
[00:14:57:919 - 00:15:01:710] **Speaker 1:** And again, we're breaking up that, that continuous physical shape
[00:15:01:710 - 00:15:05:150] **Speaker 1:** or domain into a number of uh finite or discrete
[00:15:05:469 - 00:15:06:010] **Speaker 1:** elements.
[00:15:10:140 - 00:15:12:460] **Speaker 1:** So just as we did for the 1D case, we're
[00:15:12:460 - 00:15:15:239] **Speaker 1:** going to define uh interpolation function.
[00:15:16:890 - 00:15:20:090] **Speaker 1:** So the interpolation function that we're gonna choose, are gonna
[00:15:20:090 - 00:15:21:830] **Speaker 1:** be our favourite polynomials.
[00:15:23:330 - 00:15:26:619] **Speaker 1:** So normally we vary linearly or quadratically over the element.
[00:15:27:250 - 00:15:30:090] **Speaker 1:** Some of those uh default physics solvers in console uses
[00:15:30:090 - 00:15:32:770] **Speaker 1:** quadratic, some use linear, uh, just depending on what type
[00:15:32:770 - 00:15:34:489] **Speaker 1:** of uh equations that you're solving.
[00:15:36:250 - 00:15:39:239] **Speaker 1:** So In this case, we're going to look at the
[00:15:39:239 - 00:15:40:880] **Speaker 1:** linear triangular elements.
[00:15:42:070 - 00:15:45:309] **Speaker 1:** And for an interpolation function, we're gonna consider a linear
[00:15:45:309 - 00:15:49:289] **Speaker 1:** distribution throughout the element U of X and Y.
[00:15:50:190 - 00:15:52:080] **Speaker 1:** It varies both in the X and Y coordinates.
[00:15:53:570 - 00:15:58:030] **Speaker 1:** And it has linear dependence in X and in Y,
[00:15:58:489 - 00:15:59:669] **Speaker 1:** and then we've got some offset C.
[00:16:01:359 - 00:16:03:020] **Speaker 1:** And just as we did for the one case, we're
[00:16:03:020 - 00:16:07:830] **Speaker 1:** gonna have these shape functions that define the representation of
[00:16:07:830 - 00:16:08:400] **Speaker 1:** each node.
[00:16:08:640 - 00:16:15:599] **Speaker 1:** So N1 times U1, N2, U2 plus N3, U3.
[00:16:16:750 - 00:16:18:659] **Speaker 1:** So these constants are unknown at the moment, A, B,
[00:16:18:669 - 00:16:22:349] **Speaker 1:** and C, and these shape functions in 12, and 3
[00:16:22:349 - 00:16:23:409] **Speaker 1:** are what we're gonna figure out.
[00:16:26:140 - 00:16:32:799] **Speaker 1:** So, Our domain at these nodes, the dependent variable is
[00:16:32:799 - 00:16:35:200] **Speaker 1:** being forced to equal that nodal value U 12 and
[00:16:35:200 - 00:16:35:640] **Speaker 1:** 3.
[00:16:36:169 - 00:16:37:460] **Speaker 1:** So we know that the U.
[00:16:38:359 - 00:16:40:119] **Speaker 1:** At X1Y1.
[00:16:42:349 - 00:16:49:049] **Speaker 1:** Subshooting into our equation, we have A X1 plus BY1
[00:16:49:109 - 00:16:52:739] **Speaker 1:** + C equal to, You won.
[00:16:55:859 - 00:16:59:570] **Speaker 1:** And subtooting in at 0.2 we've got you at X2,
[00:17:00:150 - 00:17:01:070] **Speaker 1:** Y 2.
[00:17:01:960 - 00:17:07:260] **Speaker 1:** We've got AX2 + BY 2 + C equal to
[00:17:07:260 - 00:17:08:199] **Speaker 1:** U2.
[00:17:09:599 - 00:17:13:079] **Speaker 1:** And the 3rd You at 0.3.
[00:17:15:880 - 00:17:20:959] **Speaker 1:** A X3, BY3 plus C equal to U 3.
[00:17:23:959 - 00:17:26:310] **Speaker 1:** We can write this out in matrix form and solve
[00:17:26:310 - 00:17:27:260] **Speaker 1:** a little bit easier.
[00:17:29:260 - 00:17:32:069] **Speaker 1:** So if we rearrange with the C.
[00:17:33:089 - 00:17:36:359] **Speaker 1:** A and B, being our vector of unknowns.
[00:17:38:040 - 00:17:39:849] **Speaker 1:** We've got 1 time C.
[00:17:43:199 - 00:17:49:560] **Speaker 1:** X1 times A and Y1 and this is all equal
[00:17:49:560 - 00:17:50:319] **Speaker 1:** to U1.
[00:17:53:199 - 00:17:54:060] **Speaker 1:** 1 X.
[00:17:54:079 - 00:17:54:959] **Speaker 1:** 2 Y.
[00:17:54:989 - 00:17:56:219] **Speaker 1:** 2 U.
[00:17:56:520 - 00:17:58:790] **Speaker 1:** 21 X.
[00:17:58:819 - 00:17:59:959] **Speaker 1:** 3 Y.
[00:17:59:989 - 00:18:01:310] **Speaker 1:** 3 U.
[00:18:01:520 - 00:18:01:800] **Speaker 1:** 3.
[00:18:05:329 - 00:18:07:489] **Speaker 1:** So we can solve for this system of equations, A,
[00:18:07:500 - 00:18:10:219] **Speaker 1:** B, and C, uh, using some algebra.
[00:18:11:459 - 00:18:15:040] **Speaker 1:** Or we can use the symbolic uh library in Python
[00:18:15:180 - 00:18:16:079] **Speaker 1:** or anything else.
[00:18:16:540 - 00:18:19:119] **Speaker 1:** And we've got C, A, and B being these expressions.
[00:18:20:339 - 00:18:23:359] **Speaker 1:** So AE is equation one.
[00:18:23:619 - 00:18:25:540] **Speaker 1:** This is going to be the area of the triangular
[00:18:25:540 - 00:18:25:780] **Speaker 1:** element.
[00:18:28:150 - 00:18:31:469] **Speaker 1:** And we're going to rewrite these equations to figure out
[00:18:31:469 - 00:18:33:410] **Speaker 1:** those shape functions in 12 and 3.
[00:18:33:869 - 00:18:36:209] **Speaker 1:** So the U of X and Y.
[00:18:37:489 - 00:18:40:780] **Speaker 1:** Is equal to our shape function one move it up.
[00:18:43:119 - 00:18:43:900] **Speaker 1:** function one.
[00:18:44:599 - 00:18:44:609] **Speaker 1:** There.
[00:18:47:359 - 00:18:49:760] **Speaker 1:** It's too many, the disc is too small, there we
[00:18:49:760 - 00:18:50:099] **Speaker 1:** go.
[00:18:50:719 - 00:18:56:540] **Speaker 1:** So U X Y N 1 XY U1 plus N2.
[00:18:57:780 - 00:18:58:979] **Speaker 1:** X Y.
[00:19:00:540 - 00:19:06:209] **Speaker 1:** U2, and in 3 of X and Y, U 3.
[00:19:14:420 - 00:19:16:739] **Speaker 1:** Maybe you can read the handwriting, but we've just got
[00:19:16:739 - 00:19:19:579] **Speaker 1:** shape functions 12, and 3, varying in X and Y.
[00:19:24:239 - 00:19:27:719] **Speaker 1:** So after some substitution and rearrangement, we can uh label
[00:19:27:719 - 00:19:30:739] **Speaker 1:** these shape functions in 12 and 3 as a function
[00:19:30:739 - 00:19:33:859] **Speaker 1:** of our nodal points, X1, 2 and 3.
[00:19:36:699 - 00:19:39:449] **Speaker 1:** And there's still some writing, so I'll give you a
[00:19:39:449 - 00:19:39:670] **Speaker 1:** break.
[00:20:00:560 - 00:20:01:959] **Speaker 1:** I was sitting in the audience.
[00:20:02:040 - 00:20:06:280] **Speaker 1:** We had a lecture from MGZ or Drew Civil, which
[00:20:06:280 - 00:20:09:099] **Speaker 1:** was quite good, but yes, the tables are very small
[00:20:09:199 - 00:20:14:069] **Speaker 1:** in those chairs, which Maybe that's why some people don't
[00:20:14:069 - 00:20:14:969] **Speaker 1:** come over either, but.
[00:20:17:000 - 00:20:18:719] **Speaker 1:** Yeah, so.
[00:20:20:550 - 00:20:22:530] **Speaker 1:** We've got shape functions in 12, and 3.
[00:20:25:520 - 00:20:27:020] **Speaker 1:** So they're a little bit longer than what we did
[00:20:27:020 - 00:20:29:180] **Speaker 1:** for 1 day, but in principle, they're the same.
[00:20:29:500 - 00:20:32:030] **Speaker 1:** We're gonna just check that each shape function represents the
[00:20:32:030 - 00:20:33:199] **Speaker 1:** node that it's supposed to.
[00:20:34:380 - 00:20:36:040] **Speaker 1:** So shape function in one.
[00:20:37:939 - 00:20:41:540] **Speaker 1:** Evaluated at X1, Y1 should equal to 1.
[00:20:45:339 - 00:20:46:959] **Speaker 1:** So I've got 1 over 2A.
[00:20:50:890 - 00:20:53:530] **Speaker 1:** And maybe use a square bracket to like the, the
[00:20:53:530 - 00:20:55:510] **Speaker 1:** big bracket, and we've got X2.
[00:20:56:900 - 00:20:59:520] **Speaker 1:** Y 3 minus.
[00:21:00:810 - 00:21:03:109] **Speaker 1:** X 3 Y.
[00:21:03:439 - 00:21:03:930] **Speaker 1:** 2.
[00:21:06:989 - 00:21:12:479] **Speaker 1:** Plus Y2 minus Y3 multiplied by X and we're evaluating
[00:21:12:479 - 00:21:13:449] **Speaker 1:** at X1.
[00:21:14:739 - 00:21:18:609] **Speaker 1:** Plus X3 minus X2.
[00:21:19:530 - 00:21:22:449] **Speaker 1:** Multiplied by Y1.
[00:21:30:229 - 00:21:31:489] **Speaker 1:** So what do we have here?
[00:21:31:869 - 00:21:34:410] **Speaker 1:** We've got anything that cancels.
[00:21:48:390 - 00:21:49:260] **Speaker 1:** Probably not.
[00:21:51:560 - 00:21:53:630] **Speaker 1:** How does it vary with AE?
[00:21:54:189 - 00:21:57:260] **Speaker 1:** So we've got X 2 Y 3, maybe we zoom
[00:21:57:260 - 00:21:57:709] **Speaker 1:** out.
[00:22:08:189 - 00:22:16:969] **Speaker 1:** So we've got X2 Y3 minus X3Y2X3Y1, X3Y 1 minus
[00:22:17:219 - 00:22:18:310] **Speaker 1:** X1.
[00:22:19:849 - 00:22:20:859] **Speaker 1:** Y 3.
[00:22:21:760 - 00:22:28:479] **Speaker 1:** And X1Y2 minus X2Y1.
[00:22:29:239 - 00:22:33:780] **Speaker 1:** So the expression within the square brackets is equal to.
[00:22:37:199 - 00:22:48:839] **Speaker 1:** 2 AE Just rearranging that half on the other side.
[00:22:50:069 - 00:22:52:579] **Speaker 1:** So 2AE over 2AE is equal to 1.
[00:23:01:209 - 00:23:02:319] **Speaker 1:** So that's reassuring.
[00:23:02:900 - 00:23:08:579] **Speaker 1:** So now N1 at another point, for example, X2, Y2.
[00:23:13:469 - 00:23:16:339] **Speaker 1:** Uh, we've got that same first term, we've got X2.
[00:23:18:569 - 00:23:19:689] **Speaker 1:** Y 3.
[00:23:22:709 - 00:23:23:910] **Speaker 1:** Hopefully that's big enough to see.
[00:23:24:310 - 00:23:29:550] **Speaker 1:** So X2Y3 minus X3Y2.
[00:23:30:760 - 00:23:34:109] **Speaker 1:** Plus Y2 minus Y 3.
[00:23:36:089 - 00:23:41:569] **Speaker 1:** X2 and X3 minus X2 Y2.
[00:23:44:760 - 00:23:46:530] **Speaker 1:** Now can we make some sim simplifications.
[00:23:46:609 - 00:23:51:170] **Speaker 1:** We've got X2Y3 X 2 Y 3.
[00:23:51:650 - 00:23:52:750] **Speaker 1:** So that cancels.
[00:23:54:930 - 00:23:59:729] **Speaker 1:** Uh, X3Y2, X3Y2 positive and negative.
[00:24:04:130 - 00:24:06:020] **Speaker 1:** And Y2 X2.
[00:24:06:300 - 00:24:07:180] **Speaker 1:** Y2 X2.
[00:24:10:849 - 00:24:12:540] **Speaker 1:** So equals 0, as expected.
[00:24:22:310 - 00:24:24:270] **Speaker 1:** We've got space, so why not do another one for
[00:24:24:270 - 00:24:24:650] **Speaker 1:** fun.
[00:24:25:219 - 00:24:27:910] **Speaker 1:** So N2 of say X2.
[00:24:28:819 - 00:24:29:599] **Speaker 1:** Y 2.
[00:24:30:550 - 00:24:31:869] **Speaker 1:** 1/2 AE.
[00:24:33:300 - 00:24:36:859] **Speaker 1:** So now for shape function two, we're reading from 3B.
[00:24:37:380 - 00:24:38:760] **Speaker 1:** So we've got X 3.
[00:24:39:959 - 00:24:42:390] **Speaker 1:** Y 1 minus X 1 Y 3.
[00:24:44:260 - 00:24:47:770] **Speaker 1:** Plus Y3 minus Y1 X.
[00:24:48:589 - 00:24:48:829] **Speaker 1:** 2.
[00:24:49:709 - 00:24:53:400] **Speaker 1:** And X1 minus X3 Y2.
[00:24:57:400 - 00:24:59:829] **Speaker 1:** So with any luck this will also be the same
[00:24:59:829 - 00:25:00:819] **Speaker 1:** as 2 AE.
[00:25:01:390 - 00:25:01:969] **Speaker 1:** So we've got.
[00:25:04:630 - 00:25:12:069] **Speaker 1:** X 3 Y1 X 1 Y 3 Y.
[00:25:12:079 - 00:25:14:290] **Speaker 1:** 3 X 2 Y.
[00:25:14:300 - 00:25:18:380] **Speaker 1:** 3 X2 minus Y 1X.
[00:25:19:680 - 00:25:21:540] **Speaker 1:** Minus Y 1 X2.
[00:25:23:160 - 00:25:25:479] **Speaker 1:** 2 and X1.
[00:25:27:329 - 00:25:28:439] **Speaker 1:** Y 2.
[00:25:29:760 - 00:25:32:099] **Speaker 1:** Minus X 3 Y2 minus 6.
[00:25:43:420 - 00:25:43:939] **Speaker 1:** Cool.
[00:25:48:280 - 00:25:50:619] **Speaker 1:** What we can do is plot these shape functions in
[00:25:50:619 - 00:25:51:469] **Speaker 1:** 2D space.
[00:25:51:780 - 00:25:54:369] **Speaker 1:** So I've sketched them here with some diagrams.
[00:25:55:219 - 00:25:59:270] **Speaker 1:** Shape functions 12 and 30 at the nodes that they're
[00:25:59:270 - 00:26:01:699] **Speaker 1:** not representing and then equal to 1 at the node
[00:26:01:699 - 00:26:02:650] **Speaker 1:** that they are representing.
[00:26:04:219 - 00:26:06:180] **Speaker 1:** And in between it's just a, a plane.
[00:26:06:660 - 00:26:09:660] **Speaker 1:** So these are planes in um 2D.
[00:26:11:160 - 00:26:14:310] **Speaker 1:** So overall, our dependent variable field U of X and
[00:26:14:310 - 00:26:16:930] **Speaker 1:** Y is being evaluated as a contribution from each of
[00:26:16:930 - 00:26:18:810] **Speaker 1:** these nodes and shape functions.
[00:26:25:569 - 00:26:27:689] **Speaker 1:** So that's all the shape functions, now we need to
[00:26:27:689 - 00:26:29:150] **Speaker 1:** consider the element equations.
[00:26:30:469 - 00:26:32:699] **Speaker 1:** So I think of the method of wasted residuals.
[00:26:38:339 - 00:26:40:869] **Speaker 1:** We can also use this in multiple dimensions.
[00:26:41:719 - 00:26:43:670] **Speaker 1:** So the idea is to first find all the required
[00:26:43:670 - 00:26:48:319] **Speaker 1:** values of our different variable at each node, Ui, so
[00:26:48:319 - 00:26:50:760] **Speaker 1:** that now we have a double integral because it's over
[00:26:50:760 - 00:26:51:619] **Speaker 1:** 2D space.
[00:26:52:339 - 00:26:55:160] **Speaker 1:** And our residual depends on X and Y.
[00:26:56:079 - 00:26:57:560] **Speaker 1:** And our waiting functions.
[00:26:59:489 - 00:27:01:859] **Speaker 1:** Integrating N Y X and Y.
[00:27:03:229 - 00:27:05:589] **Speaker 1:** We're gonna set this equal to 0, and this is
[00:27:05:589 - 00:27:06:790] **Speaker 1:** for all of our nodes.
[00:27:08:790 - 00:27:11:319] **Speaker 1:** 12, up to him.
[00:27:14:750 - 00:27:18:439] **Speaker 1:** Again, D is our 2D solution space, uh, whether it's
[00:27:18:439 - 00:27:19:900] **Speaker 1:** a triangle or otherwise.
[00:27:21:979 - 00:27:24:050] **Speaker 1:** And W being our weighting functions.
[00:27:24:979 - 00:27:27:339] **Speaker 1:** So our Gli method, we use the shape functions as
[00:27:27:339 - 00:27:30:020] **Speaker 1:** our linearly independent waiting functions.
[00:27:30:300 - 00:27:31:280] **Speaker 1:** So substting.
[00:27:54:489 - 00:27:56:550] **Speaker 1:** Pretty much just substituting WI with NI.
[00:27:58:280 - 00:28:02:000] **Speaker 1:** And we're gonna look at the uh Poisson equation as
[00:28:02:000 - 00:28:02:699] **Speaker 1:** an example.
[00:28:03:739 - 00:28:05:560] **Speaker 1:** So in 2D, the Poisson equation.
[00:28:06:609 - 00:28:09:579] **Speaker 1:** Is D2 U R T X2.
[00:28:11:089 - 00:28:14:459] **Speaker 1:** Plus D2U by DY2.
[00:28:15:920 - 00:28:19:239] **Speaker 1:** Equal to some sauce stone, we'll label roe.
[00:28:22:550 - 00:28:25:339] **Speaker 1:** So you've seen this PDE before, um, if row is
[00:28:25:339 - 00:28:26:900] **Speaker 1:** 0, that's the Laplace equation.
[00:28:35:020 - 00:28:38:390] **Speaker 1:** What we're going to do is approximate our solution for
[00:28:38:390 - 00:28:41:430] **Speaker 1:** our field you with Utilda, which is all those literally
[00:28:41:430 - 00:28:43:449] **Speaker 1:** interpolated uh functions.
[00:28:43:829 - 00:28:48:270] **Speaker 1:** So you tilda, subtooting for you, our residual is going
[00:28:48:270 - 00:28:49:660] **Speaker 1:** to be the leftover.
[00:28:50:140 - 00:28:52:150] **Speaker 1:** So uh X and Y.
[00:28:53:099 - 00:28:56:900] **Speaker 1:** Equal to D2 Uta by DX2.
[00:28:57:790 - 00:29:02:239] **Speaker 1:** Plus D2 Utta by DY2.
[00:29:03:500 - 00:29:05:339] **Speaker 1:** Minus row of X and Y.
[00:29:25:660 - 00:29:28:140] **Speaker 1:** So just as we did uh integration by parts in
[00:29:28:140 - 00:29:31:900] **Speaker 1:** 1D, they've come up with a sort of similar thing
[00:29:31:900 - 00:29:32:780] **Speaker 1:** to do in 2D.
[00:29:33:819 - 00:29:36:979] **Speaker 1:** So we're using some theorem called Green's theorem to do
[00:29:36:979 - 00:29:41:839] **Speaker 1:** this, but we're going to evaluate or reduce the order
[00:29:41:839 - 00:29:44:979] **Speaker 1:** of our second-order terms to 1 to first order.
[00:29:47:270 - 00:29:52:170] **Speaker 1:** So integrating of our domain, our second-order terms, we've got
[00:29:52:170 - 00:29:58:939] **Speaker 1:** D2U tilta by DX2 plus D2U tilta by DY2.
[00:29:59:849 - 00:30:01:469] **Speaker 1:** N I D X D Y.
[00:30:05:319 - 00:30:07:839] **Speaker 1:** And this is equivalent to minus.
[00:30:08:859 - 00:30:17:699] **Speaker 1:** Integral of DU toda by DX, DNI by DX plus
[00:30:17:699 - 00:30:23:260] **Speaker 1:** DU toda by DY DNI by DY.
[00:30:24:709 - 00:30:28:229] **Speaker 1:** Integrating an X and Y.
[00:30:35:349 - 00:30:40:270] **Speaker 1:** And then we're Substituting the integral across the contour line.
[00:30:41:050 - 00:30:44:229] **Speaker 1:** Uh, which is sort of like the perimeter of our
[00:30:44:369 - 00:30:45:010] **Speaker 1:** computational plane.
[00:30:46:709 - 00:30:55:530] **Speaker 1:** And we're evaluating NID Utilda by D Y D X
[00:30:55:530 - 00:30:57:869] **Speaker 1:** minus N I.
[00:30:59:369 - 00:31:03:030] **Speaker 1:** D Uoda by D X D Y.
[00:31:06:339 - 00:31:10:140] **Speaker 1:** So this sort of line with the circle is, is
[00:31:10:140 - 00:31:15:380] **Speaker 1:** a contour integral over the contour of the computational domain
[00:31:15:380 - 00:31:16:349] **Speaker 1:** or the boundary.
[00:31:18:900 - 00:31:22:380] **Speaker 1:** And some more hand waving, we're gonna choose our shape
[00:31:22:380 - 00:31:24:369] **Speaker 1:** functions to be zero at the boundary.
[00:31:25:339 - 00:31:27:500] **Speaker 1:** And the second integral is going to be equal to
[00:31:27:500 - 00:31:28:079] **Speaker 1:** 0.
[00:31:28:459 - 00:31:31:579] **Speaker 1:** And if we combine equations 57, and 8.
[00:31:32:650 - 00:31:34:069] **Speaker 1:** So that's our Gurkin method.
[00:31:35:069 - 00:31:39:800] **Speaker 1:** Our croissant and using green serum to reduce that odour.
[00:31:52:609 - 00:31:56:510] **Speaker 1:** We go from having our top, oh, I can't see.
[00:31:57:469 - 00:32:03:189] **Speaker 1:** Go from our double integral with second-order terms, D2U tilter
[00:32:04:180 - 00:32:10:930] **Speaker 1:** by DX2 and D2U tilda by DY 2 minus row.
[00:32:12:939 - 00:32:17:060] **Speaker 1:** N I D X D Y equal to 0.
[00:32:17:959 - 00:32:19:760] **Speaker 1:** For I equal 12.
[00:32:20:550 - 00:32:22:979] **Speaker 1:** Up to however many degrees of freedom that we have.
[00:32:33:910 - 00:32:36:050] **Speaker 1:** So we go from this form to the form of
[00:32:36:050 - 00:32:36:829] **Speaker 1:** the Queen's Serum.
[00:32:36:939 - 00:32:38:319] **Speaker 1:** So I'll just give you a moment to write.
[00:33:03:689 - 00:33:04:109] **Speaker 1:** Cool.
[00:33:07:930 - 00:33:12:380] **Speaker 1:** So we convert to our green serumm form, so it's
[00:33:12:380 - 00:33:15:540] **Speaker 1:** still double integral and now I've got first order derivatives
[00:33:15:540 - 00:33:16:800] **Speaker 1:** Dilda by DX.
[00:33:18:420 - 00:33:21:199] **Speaker 1:** DNI Y D X.
[00:33:22:420 - 00:33:29:530] **Speaker 1:** Plus DU Tilda by DY DNI by DY plus row
[00:33:29:530 - 00:33:29:859] **Speaker 1:** NI.
[00:33:48:079 - 00:33:50:319] **Speaker 1:** So this form is now our weak form of our
[00:33:50:319 - 00:33:50:810] **Speaker 1:** govern PDE.
[00:33:53:719 - 00:33:55:920] **Speaker 1:** Finally got to some stage that we can form the
[00:33:55:920 - 00:33:56:939] **Speaker 1:** element equations from.
[00:34:01:810 - 00:34:04:359] **Speaker 1:** So these element equations are gonna be figured out by
[00:34:04:359 - 00:34:07:540] **Speaker 1:** integrating across our elements, so that triangle.
[00:34:13:458 - 00:34:19:019] **Speaker 1:** For example, we could integrate over that space delta 123
[00:34:19:019 - 00:34:20:198] **Speaker 1:** or triangle 123.
[00:34:22:790 - 00:34:25:850] **Speaker 1:** DU Toda by D X.
[00:34:26:839 - 00:34:29:479] **Speaker 1:** DNI by DX.
[00:34:29:759 - 00:34:33:299] **Speaker 1:** Not sure why we're writing it out again, but DU
[00:34:33:299 - 00:34:34:479] **Speaker 1:** tilda by D Y.
[00:34:35:850 - 00:34:38:010] **Speaker 1:** DNI by DY.
[00:34:38:919 - 00:34:40:860] **Speaker 1:** Plus row in I.
[00:34:41:810 - 00:34:44:669] **Speaker 1:** D X D Y equal to 0.
[00:34:49:060 - 00:34:50:790] **Speaker 1:** And for that first case that we saw on that
[00:34:50:790 - 00:34:51:610] **Speaker 1:** first page.
[00:34:53:009 - 00:34:55:708] **Speaker 1:** This triangle has 3 nodes, 3 nodal points, so I
[00:34:55:708 - 00:34:56:668] **Speaker 1:** equal 12, and 3.
[00:34:59:360 - 00:35:01:290] **Speaker 1:** So we have 3 equations that we solve.
[00:35:03:139 - 00:35:05:439] **Speaker 1:** And those 3 unknowns, you 12, and 3.
[00:35:14:899 - 00:35:18:899] **Speaker 1:** And this is for I equal to 1.
[00:35:20:040 - 00:35:22:489] **Speaker 1:** Subshooting in I equal to 1, we've got these shape
[00:35:22:489 - 00:35:25:889] **Speaker 1:** functions DN1 by DX um.
[00:35:34:320 - 00:35:36:389] **Speaker 1:** And DN1 by DY.
[00:35:49:199 - 00:35:52:870] **Speaker 1:** So 1 in 12 and 3, our linear functions in
[00:35:52:870 - 00:35:54:729] **Speaker 1:** X and Y, they are those planes.
[00:35:55:570 - 00:35:57:989] **Speaker 1:** So these gradients are all constants, so they can be
[00:35:57:989 - 00:36:01:370] **Speaker 1:** chucked outside the integral and we can evaluate this equation
[00:36:01:370 - 00:36:02:159] **Speaker 1:** explicitly.
[00:36:02:570 - 00:36:04:370] **Speaker 1:** And we've, we've done this for you.
[00:36:04:610 - 00:36:05:989] **Speaker 1:** So this is equation 12.
[00:36:07:419 - 00:36:10:719] **Speaker 1:** Now we can group like coefficients again.
[00:36:11:560 - 00:36:14:360] **Speaker 1:** And we've got uh coefficients in front of U 12
[00:36:14:360 - 00:36:16:620] **Speaker 1:** and 3, and then a right-hand turn B1.
[00:36:17:590 - 00:36:19:719] **Speaker 1:** And we can do the same for 1 equal 2.
[00:36:22:620 - 00:36:25:750] **Speaker 1:** And for I equals 3.
[00:36:28:199 - 00:36:32:350] **Speaker 1:** And these equations, 13 A B and oh you can't
[00:36:32:350 - 00:36:32:679] **Speaker 1:** see.
[00:36:35:199 - 00:36:37:840] **Speaker 1:** 13 A, B and C are going to be our
[00:36:37:840 - 00:36:40:300] **Speaker 1:** element equations in 2D for our triangular element.
[00:36:51:929 - 00:36:54:770] **Speaker 1:** So I've chosen our interpolation, uh.
[00:36:57:159 - 00:37:00:360] **Speaker 1:** Functions, we've got shape functions, we've got our element equations.
[00:37:00:439 - 00:37:02:320] **Speaker 1:** Now we're gonna stitch them all together and assemble them
[00:37:02:320 - 00:37:03:280] **Speaker 1:** for our complete domain.
[00:37:04:149 - 00:37:08:419] **Speaker 1:** Not only the one element, the assembly process is largely
[00:37:08:419 - 00:37:10:239] **Speaker 1:** the same as for the oneD case.
[00:37:14:790 - 00:37:20:429] **Speaker 1:** And I went Won't subject you to the To more
[00:37:20:429 - 00:37:23:429] **Speaker 1:** maths, so we're not going to implement that with our
[00:37:23:429 - 00:37:25:800] **Speaker 1:** um, Pins.
[00:37:26:159 - 00:37:29:639] **Speaker 1:** So we've we've used console for this, and those who
[00:37:29:639 - 00:37:32:120] **Speaker 1:** are super keen could probably do that in uh Python
[00:37:32:120 - 00:37:32:739] **Speaker 1:** as well.
[00:37:34:590 - 00:37:37:350] **Speaker 1:** But we're, we're really just focused on this commercial software
[00:37:37:350 - 00:37:38:070] **Speaker 1:** package console.
[00:37:38:379 - 00:37:41:070] **Speaker 1:** There's lots of other finite element software, uh, solvers out
[00:37:41:070 - 00:37:43:370] **Speaker 1:** there, uh, both commercial and free.
[00:37:43:949 - 00:37:46:159] **Speaker 1:** So, yeah, in the workplace or maybe further down the
[00:37:46:159 - 00:37:47:570] **Speaker 1:** track, maybe you want to use something else.
[00:37:47:989 - 00:37:50:750] **Speaker 1:** Phoenix I mentioned earlier, uh, is a good open source
[00:37:50:750 - 00:37:52:370] **Speaker 1:** package for finite element solvers.
[00:37:52:750 - 00:37:56:429] **Speaker 1:** And if you take the FEA course next year, I
[00:37:56:429 - 00:37:59:110] **Speaker 1:** think they use Abacus, uh, which is quite often used
[00:37:59:110 - 00:37:59:949] **Speaker 1:** for solid mechanics.
[00:38:03:439 - 00:38:04:030] **Speaker 1:** Cool.
[00:38:04:360 - 00:38:07:000] **Speaker 1:** So pretty much similar to 1D, there's some more maths
[00:38:07:000 - 00:38:11:040] **Speaker 1:** and bookkeeping, but it's possible to solve finite elements in
[00:38:11:040 - 00:38:13:959] **Speaker 1:** 3D and then expanding to 3D is, is the next
[00:38:13:959 - 00:38:14:239] **Speaker 1:** step.
[00:38:16:590 - 00:38:17:050] **Speaker 1:** Cool.
[00:38:17:149 - 00:38:20:790] **Speaker 1:** Any questions on finer elements in 1 or 2D?
[00:38:30:770 - 00:38:32:610] **Speaker 1:** I've got some questions for you, so you can do
[00:38:32:610 - 00:38:33:030] **Speaker 1:** these.
[00:38:33:570 - 00:38:34:820] **Speaker 1:** So we've got question 1.
[00:38:35:169 - 00:38:37:729] **Speaker 1:** We're gonna look at this element 123.
[00:38:38:479 - 00:38:41:360] **Speaker 1:** And we've got these nodal values, U 12, and 3,
[00:38:41:550 - 00:38:43:139] **Speaker 1:** and the coordinates of those nodes.
[00:38:44:139 - 00:38:46:629] **Speaker 1:** Just being about this unit square one by one.
[00:38:47:030 - 00:38:50:469] **Speaker 1:** And we've got a um a function you have X
[00:38:50:469 - 00:38:52:600] **Speaker 1:** and Y is going to be approximated with that linear
[00:38:52:600 - 00:38:55:169] **Speaker 1:** distribution, A X plus P Y + C.
[00:38:55:709 - 00:38:58:070] **Speaker 1:** and you're tasked with finding the shape functions in +12
[00:38:58:070 - 00:39:00:489] **Speaker 1:** and 3 that correspond to those.
[00:39:01:560 - 00:39:02:389] **Speaker 1:** Those values.
[00:39:05:629 - 00:39:15:600] **Speaker 1:** So I'll give you a moment.
[00:39:17:219 - 00:39:20:110] **Speaker 1:** To figure out the shape functions in 12 and 3.
[00:39:39:770 - 00:39:41:129] **Speaker 1:** That's a summary of the.
[00:39:43:209 - 00:39:44:169] **Speaker 1:** Shape functions.
[00:41:40:489 - 00:41:43:570] **Speaker 1:** So all we're doing is figuring out in 12 and
[00:41:43:570 - 00:41:43:729] **Speaker 1:** 3.
[00:41:43:770 - 00:41:46:989] **Speaker 1:** We're substituting in values X1 X2 X3, not that exciting
[00:41:46:989 - 00:41:48:530] **Speaker 1:** um and Y 12 and 3.
[00:41:49:050 - 00:41:51:250] **Speaker 1:** So first we need to figure out the area of
[00:41:51:250 - 00:41:54:030] **Speaker 1:** the triangle, uh, so we can use that formula AE.
[00:41:54:729 - 00:41:55:750] **Speaker 1:** So X2.
[00:41:58:439 - 00:41:59:350] **Speaker 1:** is equal to 1.
[00:42:00:340 - 00:42:03:669] **Speaker 1:** Y 3 is equal to 1, so we've got 1
[00:42:04:169 - 00:42:06:550] **Speaker 1:** minus X3.
[00:42:07:790 - 00:42:08:709] **Speaker 1:** It's a half.
[00:42:12:649 - 00:42:14:969] **Speaker 1:** Y 2 is 1.
[00:42:17:879 - 00:42:20:429] **Speaker 1:** And then we've got X-ray is a 12.
[00:42:22:439 - 00:42:22:679] **Speaker 1:** Y.
[00:42:22:709 - 00:42:24:120] **Speaker 1:** 10.
[00:42:25:070 - 00:42:26:189] **Speaker 1:** X1.
[00:42:27:199 - 00:42:42:219] **Speaker 1:** Is there Plus Next one Y 2 And X2 Y
[00:42:42:979 - 00:42:43:540] **Speaker 1:** 1.
[00:42:48:399 - 00:42:51:040] **Speaker 1:** So that's gonna be 1 minus 1/2 is 1/2 times
[00:42:51:040 - 00:42:54:639] **Speaker 1:** 1/2, so a quarter is our element area.
[00:42:56:469 - 00:42:59:010] **Speaker 1:** So we substitute the same for shape functions in 12
[00:42:59:010 - 00:42:59:699] **Speaker 1:** and 3.
[00:43:00:479 - 00:43:01:459] **Speaker 1:** So N1.
[00:43:02:129 - 00:43:03:989] **Speaker 1:** Of X and Y.
[00:43:06:169 - 00:43:09:189] **Speaker 1:** We're told is equal to 1/2 AE.
[00:43:11:419 - 00:43:13:020] **Speaker 1:** And AE was 25%.
[00:43:15:389 - 00:43:20:419] **Speaker 1:** So we have 2/1.
[00:43:25:239 - 00:43:33:550] **Speaker 1:** And We have X2Y3, X2 Y 3 is 1 times
[00:43:33:550 - 00:43:33:969] **Speaker 1:** 1.
[00:43:35:479 - 00:43:37:179] **Speaker 1:** Minus X3Y2.
[00:43:38:840 - 00:43:48:260] **Speaker 1:** So half And why to Minus Y 3, so that's
[00:43:48:260 - 00:43:48:919] **Speaker 1:** 0.
[00:43:50:449 - 00:43:52:199] **Speaker 1:** And X 3.
[00:43:56:870 - 00:44:01:149] **Speaker 1:** There's a 12 minus X2, 1/2 minus 1.
[00:44:05:750 - 00:44:27:070] **Speaker 1:** So I've done something wrong Maybe Can anyone spot what
[00:44:27:070 - 00:44:27:550] **Speaker 1:** I've done?
[00:44:27:780 - 00:44:29:590] **Speaker 1:** Has anyone done this or not?
[00:44:33:649 - 00:44:37:850] **Speaker 1:** Um, So we've got uh OK, so maybe I just
[00:44:37:850 - 00:44:40:389] **Speaker 1:** need to add the Y cause the X's did cancel.
[00:44:40:409 - 00:44:42:189] **Speaker 1:** We had Y 2 and 3.
[00:44:42:889 - 00:44:45:270] **Speaker 1:** So Y 2 is 1 minus 1.
[00:44:46:300 - 00:44:50:429] **Speaker 1:** And then X3 is a 12 minus 1.
[00:44:50:899 - 00:44:51:659] **Speaker 1:** So I think it was just.
[00:44:52:250 - 00:44:54:169] **Speaker 1:** That why I'm missing.
[00:44:55:149 - 00:44:59:469] **Speaker 1:** So We've got 1 minus 15.
[00:45:02:360 - 00:45:03:560] **Speaker 1:** And then minus 5.
[00:45:03:810 - 00:45:04:219] **Speaker 1:** Why?
[00:45:06:669 - 00:45:09:399] **Speaker 1:** Which is equal to 1 minus Y.
[00:45:12:760 - 00:45:13:120] **Speaker 1:** Cool.
[00:45:15:709 - 00:45:17:850] **Speaker 1:** All right, that's a bit painful.
[00:45:29:770 - 00:45:31:169] **Speaker 1:** So we can do the same for the other two.
[00:45:32:610 - 00:45:35:260] **Speaker 1:** And I'm just going to write what they are because.
[00:45:36:649 - 00:45:37:100] **Speaker 1:** Can't see it.
[00:45:37:570 - 00:45:38:439] **Speaker 1:** You can't see it either.
[00:45:38:639 - 00:45:39:629] **Speaker 1:** 2 explains why.
[00:45:41:439 - 00:45:45:510] **Speaker 1:** And N3 of X and Y is minus 2 X
[00:45:45:770 - 00:45:47:050] **Speaker 1:** + 2 Y.
[00:45:49:110 - 00:45:51:449] **Speaker 1:** So these are our shape functions uh for the 2D
[00:45:51:449 - 00:45:54:550] **Speaker 1:** element, and the last or part D is gonna look
[00:45:54:550 - 00:45:55:050] **Speaker 1:** at.
[00:45:55:909 - 00:46:00:560] **Speaker 1:** Essentially applying the interpolation for figuring out what util there
[00:46:00:560 - 00:46:02:830] **Speaker 1:** is at some point within the element.
[00:46:03:030 - 00:46:04:169] **Speaker 1:** So actually put a half.
[00:46:06:520 - 00:46:09:899] **Speaker 1:** And Y equal to 3/4 about up here.
[00:46:13:429 - 00:46:16:479] **Speaker 1:** Given we've got nodal values of U 12 and 3.
[00:46:23:169 - 00:46:24:889] **Speaker 1:** So I'll give you a minute to think of that.
[00:47:44:219 - 00:47:46:379] **Speaker 1:** So hopefully I've not made any more mistakes.
[00:47:46:419 - 00:47:48:459] **Speaker 1:** We've got Utilda, functional mix and by.
[00:47:49:909 - 00:47:52:649] **Speaker 1:** And we're gonna evaluate a half.
[00:47:53:969 - 00:47:54:850] **Speaker 1:** And 3/4.
[00:48:01:250 - 00:48:06:070] **Speaker 1:** So X equal to 1/22, Y equal to 3/4.
[00:48:16:860 - 00:48:21:260] **Speaker 1:** Now I've got fractions, so 1 minus.
[00:48:22:889 - 00:48:24:250] **Speaker 1:** 3/8.
[00:48:25:199 - 00:48:26:899] **Speaker 1:** -1 plus.
[00:48:50:510 - 00:48:54:429] **Speaker 1:** So, I mean in the answers I've got 5/8s, so
[00:48:54:429 - 00:48:57:870] **Speaker 1:** maybe you can do check that but um hopefully that's
[00:48:57:870 - 00:48:58:169] **Speaker 1:** right.
[00:48:59:969 - 00:49:06:060] **Speaker 1:** Um, so that's Essentially using our linear interpolation for our
[00:49:06:060 - 00:49:06:719] **Speaker 1:** 2D element.
[00:49:08:139 - 00:49:10:639] **Speaker 1:** I'm not going to get you to do lots of
[00:49:10:639 - 00:49:12:979] **Speaker 1:** 2D finite element things in the exam, but you should
[00:49:12:979 - 00:49:15:939] **Speaker 1:** be able to work through some of the, um, shape
[00:49:15:939 - 00:49:16:820] **Speaker 1:** functions, all right.
[00:49:21:379 - 00:49:22:060] **Speaker 1:** Cool.
[00:49:22:459 - 00:49:23:540] **Speaker 1:** Any questions?
[00:49:27:989 - 00:49:28:500] **Speaker 1:** No.
[00:49:29:530 - 00:49:30:590] **Speaker 1:** Alright, cool.
[00:49:31:860 - 00:49:34:500] **Speaker 1:** Alright, so Wednesday, we'll go back to chapter 7 on
[00:49:34:500 - 00:49:35:280] **Speaker 1:** the wave equation.
[00:49:35:500 - 00:49:38:699] **Speaker 1:** Uh, and I've delayed the wave equation because we wanted
[00:49:38:699 - 00:49:39:770] **Speaker 1:** to cover everything for the assignment.
[00:49:39:909 - 00:49:41:419] **Speaker 1:** So that's why we reordered things.
[00:49:41:699 - 00:49:43:659] **Speaker 1:** Um, but we'll go through the wave equation as our
[00:49:43:659 - 00:49:45:739] **Speaker 1:** as our last chapter on Wednesday.
[00:50:06:540 - 00:50:06:790] **Speaker 0:** Nice.
[00:50:28:830 - 00:50:29:469] **Speaker 0:** Um.
[00:50:30:570 - 00:50:30:580] **Speaker 2:** OK.
[00:50:33:889 - 00:50:39:879] **Speaker 2:** to get the um You know, uh.
[00:50:42:280 - 00:50:49:139] **Speaker 0:** Yeah, yeah, yeah, uh, it's varying in temperature, uh, if
[00:50:49:139 - 00:50:53:060] **Speaker 0:** we're doing the, you know, the, the usual way of
[00:50:53:250 - 00:50:54:919] **Speaker 2:** of potential techniques and then.
[00:50:55:820 - 00:50:57:860] **Speaker 2:** Uh, but doing two of those that are sort of
[00:50:57:860 - 00:51:02:500] **Speaker 2:** at the points in the second one, doing between those
[00:51:02:500 - 00:51:02:729] **Speaker 2:** two.
[00:51:03:129 - 00:51:07:219] **Speaker 2:** And we've got K, uh, K would technically be evaluated
[00:51:07:219 - 00:51:10:790] **Speaker 2:** in the middle between two nodes, and I'm wondering what
[00:51:11:100 - 00:51:12:500] **Speaker 2:** methods are allowed for that.
[00:51:12:610 - 00:51:16:459] **Speaker 2:** Do we evaluate K at those two nodes and average
[00:51:16:459 - 00:51:19:739] **Speaker 2:** them, or do we get the average temperature and evaluate
[00:51:19:739 - 00:51:22:959] **Speaker 2:** K at that, or is average the completely wrong?
[00:51:25:159 - 00:51:28:510] **Speaker 1:** Uh, my suggestion was to just do that in a
[00:51:28:510 - 00:51:30:459] **Speaker 1:** derivative and the outer derivative.
[00:51:31:379 - 00:51:33:760] **Speaker 1:** So similar to what we did with the, um.
[00:51:36:169 - 00:51:36:500] **Speaker 1:** The good person.
[00:51:37:649 - 00:51:41:449] **Speaker 1:** So you evaluate Kappa at the halfway point.
[00:51:42:159 - 00:51:44:159] **Speaker 1:** And then, yeah, so you need the temperature at that
[00:51:44:159 - 00:51:45:760] **Speaker 1:** halfway point you could just take the average of the
[00:51:45:760 - 00:51:45:770] **Speaker 1:** temperature.
[00:51:47:489 - 00:51:51:239] **Speaker 1:** That's how I would do it, um, but there's probably
[00:51:51:239 - 00:51:52:790] **Speaker 1:** not a lot in it really if you do it,
[00:51:53:250 - 00:51:54:449] **Speaker 1:** um, the other way around.
[00:51:56:209 - 00:52:01:479] **Speaker 1:** I think it'll be the same, yeah, I mean like
[00:52:01:479 - 00:52:03:270] **Speaker 2:** Lia tea, so I think it would be way too
[00:52:03:270 - 00:52:04:800] **Speaker 2:** differently to do it the other way around.
[00:52:04:889 - 00:52:06:010] **Speaker 2:** That's how I've done it because it.
[00:52:07:419 - 00:52:10:159] **Speaker 1:** Thank you, so are you?
[00:52:11:229 - 00:52:14:070] **Speaker 1:** So it's quite similar to comps so I don't think
[00:52:14:070 - 00:52:14:889] **Speaker 1:** it'd be allowable.
[00:52:16:919 - 00:52:18:959] **Speaker 1:** I mean, uh, it's probably not gonna be exactly the
[00:52:18:959 - 00:52:21:159] **Speaker 1:** same, they're different, I think, but.
[00:52:22:199 - 00:52:23:439] **Speaker 1:** They should be approximately.
[00:52:25:209 - 00:52:27:209] **Speaker 1:** Just so like I guess in the report, so long
[00:52:27:209 - 00:52:29:399] **Speaker 2:** as we talked about what we've done, yeah, yeah, yeah,
[00:52:29:629 - 00:52:31:330] **Speaker 1:** yeah, so I, I think, yeah, there's at least a
[00:52:31:330 - 00:52:34:449] **Speaker 1:** couple of different ways to approach it, yeah, OK.
[00:52:36:699 - 00:52:37:520] **Speaker 0:** I'm just a similar.
[00:52:37:979 - 00:52:39:459] **Speaker 0:** I just wanted to check if I was.
[00:52:40:709 - 00:52:42:739] **Speaker 0:** Formulating my equations right.
[00:52:44:709 - 00:52:47:510] **Speaker 0:** Yeah, um, we can talk about.
[00:53:01:639 - 00:53:01:989] **Speaker 0:** We're not.
[00:53:15:780 - 00:53:17:879] **Speaker 0:** Hey, can someone push the UCtern out of the way
[00:53:18:699 - 00:53:19:260] **Speaker 0:** before I drop it.
[00:53:21:800 - 00:53:28:699] **Speaker 0:** I didn't mind, I got a I do.
[00:54:13:370 - 00:54:28:270] **Speaker 0:** Some of my In this.
[00:54:36:239 - 00:54:36:439] **Speaker 0:** How big.
[00:54:37:669 - 00:54:37:679] **Speaker 0:** Yeah.
[00:54:54:399 - 00:54:56:330] **Speaker 0:** Whatever you do, make sure you don't forget to have
[00:54:56:330 - 00:54:58:370] **Speaker 0:** the milk safe because they make a god awful noise
[00:54:58:370 - 00:54:59:449] **Speaker 1:** when they get crunched up in milk.

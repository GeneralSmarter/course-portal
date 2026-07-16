# ENME302-26S2 Lecture 3 native Echo transcript

Date: July 16, 2026 10:00am-10:55am
Transcript type: native Echo automated transcript.

[00:00:08:350 - 00:00:10:760] **Speaker 0:** OK at.
[00:00:21:489 - 00:00:30:090] **Speaker 0:** Well, Karakoto, welcome along, everyone.
[00:00:33:549 - 00:00:35:639] **Speaker 1:** Sophia, um.
[00:00:37:029 - 00:00:40:830] **Speaker 1:** Reasonably busy day for 202 today between the lab session,
[00:00:40:909 - 00:00:42:869] **Speaker 1:** the lecture this morning and the lab sessions this afternoon.
[00:00:43:729 - 00:00:45:169] **Speaker 1:** Um, what I wanna do is just sort of pick
[00:00:45:169 - 00:00:47:810] **Speaker 1:** up where we left off, go through some of the
[00:00:47:810 - 00:00:50:689] **Speaker 1:** concepts of shape functions, um, do a quick example around
[00:00:50:689 - 00:00:53:569] **Speaker 1:** that, and then, uh, I will then just touch very
[00:00:53:569 - 00:00:55:450] **Speaker 1:** briefly on the, the lab sheet that we'll be covering
[00:00:55:450 - 00:00:56:389] **Speaker 1:** in the lab this afternoon.
[00:00:58:439 - 00:01:02:959] **Speaker 1:** So where we got to yesterday was essentially we've we've
[00:01:02:959 - 00:01:05:720] **Speaker 1:** gone around and just, you know, said quite, quite clearly
[00:01:05:720 - 00:01:08:440] **Speaker 1:** and probably a few times now this concept about just
[00:01:08:440 - 00:01:11:440] **Speaker 1:** having a, a single piece, a little element of the
[00:01:11:440 - 00:01:15:239] **Speaker 1:** structure which in itself is very predictable, very repeatable, very
[00:01:15:239 - 00:01:17:650] **Speaker 1:** easy to understand, and that we can build up more
[00:01:17:650 - 00:01:20:919] **Speaker 1:** complex structures based upon those simple building blocks.
[00:01:23:209 - 00:01:26:650] **Speaker 1:** So just to reiterate what was going on here, we
[00:01:26:650 - 00:01:31:349] **Speaker 1:** have uh, Dynamic system and everything that we're learning here.
[00:01:32:529 - 00:01:33:750] **Speaker 1:** We're gonna be covering it.
[00:01:34:660 - 00:01:41:279] **Speaker 1:** In these lectures in the context of um, Static equilibrium,
[00:01:41:319 - 00:01:42:910] **Speaker 1:** so we're just going to be dealing with this part
[00:01:42:910 - 00:01:44:769] **Speaker 1:** of the equation of motion.
[00:01:45:910 - 00:01:50:160] **Speaker 1:** But everything we do is generalizable to a mass matrix,
[00:01:50:279 - 00:01:53:160] **Speaker 1:** a stamping matrix, a vector of accelerations, a vector of
[00:01:53:160 - 00:01:56:480] **Speaker 1:** velocities, and we could extend this very easily into a
[00:01:56:480 - 00:01:57:459] **Speaker 1:** dynamic problem.
[00:01:57:870 - 00:02:00:790] **Speaker 1:** Um, it's beyond the scope of this course, but in
[00:02:00:790 - 00:02:02:639] **Speaker 1:** the context of say the dynamics course that you did
[00:02:02:639 - 00:02:06:459] **Speaker 1:** last year, um, this isn't, um, at odds with that.
[00:02:06:559 - 00:02:08:639] **Speaker 1:** It's just one stepping stone towards that.
[00:02:10:339 - 00:02:12:570] **Speaker 1:** We have our element freebo diagram here.
[00:02:13:059 - 00:02:15:979] **Speaker 1:** We define our forces and displacements going in the positive
[00:02:15:979 - 00:02:19:029] **Speaker 1:** X direction for the element, which means they're both pointing
[00:02:19:029 - 00:02:21:660] **Speaker 1:** in the same direction, which means that F1 and 2
[00:02:21:660 - 00:02:25:419] **Speaker 1:** F2 must be equal in the magnitude but opposite in
[00:02:25:419 - 00:02:28:179] **Speaker 1:** sign for this to be a static equilibrium.
[00:02:30:410 - 00:02:32:330] **Speaker 1:** We go through and our goal is to be able
[00:02:32:330 - 00:02:35:490] **Speaker 1:** to define sumu of X defined from X equals 0
[00:02:35:490 - 00:02:38:210] **Speaker 1:** to X equals L based upon D1 and D2.
[00:02:39:380 - 00:02:41:809] **Speaker 1:** So this here is actually this this step here labelled
[00:02:41:809 - 00:02:44:210] **Speaker 1:** number 2 is actually really fundamental.
[00:02:44:259 - 00:02:46:259] **Speaker 1:** This is what makes finite elements finite.
[00:02:46:380 - 00:02:48:300] **Speaker 1:** This is what makes us able to solve at a
[00:02:48:300 - 00:02:51:979] **Speaker 1:** few discrete points but have those discrete points be representative
[00:02:52:539 - 00:02:53:800] **Speaker 1:** of a continuous structure.
[00:02:55:300 - 00:03:13:610] **Speaker 1:** This here There's a way Of defining Continuous Internal Element
[00:03:13:610 - 00:03:14:360] **Speaker 1:** mechanics.
[00:03:20:210 - 00:03:21:520] **Speaker 1:** Based upon only.
[00:03:23:410 - 00:03:24:350] **Speaker 1:** The values.
[00:03:26:580 - 00:03:34:729] **Speaker 1:** At the end points So that relationship that we define,
[00:03:35:020 - 00:03:37:160] **Speaker 1:** what we do to to link those together.
[00:03:38:149 - 00:03:41:729] **Speaker 1:** That is fundamental to Everything comes from this.
[00:03:41:809 - 00:03:43:600] **Speaker 1:** It's the fundamental of the finite element method, but it
[00:03:43:600 - 00:03:46:289] **Speaker 1:** also means that the assumptions that we make then govern
[00:03:46:289 - 00:03:49:270] **Speaker 1:** everything we can do with that analysis package.
[00:03:52:149 - 00:03:54:580] **Speaker 1:** So we did some derivations yesterday.
[00:03:55:699 - 00:03:57:660] **Speaker 1:** We took this little infinitely small section of bar, we
[00:03:57:660 - 00:04:00:820] **Speaker 1:** had a an axial force in on the left, some
[00:04:00:820 - 00:04:05:500] **Speaker 1:** distributed force P times the distanced X, which then led
[00:04:05:500 - 00:04:07:860] **Speaker 1:** to a change in the internal axial force tonne plus
[00:04:07:860 - 00:04:09:199] **Speaker 1:** DN on the right hand side.
[00:04:11:149 - 00:04:13:630] **Speaker 1:** And when you go through and you break that out,
[00:04:13:710 - 00:04:16:390] **Speaker 1:** you say that the rate of change of internal law
[00:04:16:390 - 00:04:19:028] **Speaker 1:** force with respect to position of the bar X is
[00:04:19:028 - 00:04:20:868] **Speaker 1:** equal to the distributed load intensity P.
[00:04:21:070 - 00:04:22:970] **Speaker 1:** So that shouldn't come as a surprise.
[00:04:23:670 - 00:04:25:859] **Speaker 1:** We can rewrite that using some simple stress and strain
[00:04:25:859 - 00:04:28:190] **Speaker 1:** relationships, reiterating that, you know, we're building upon what you
[00:04:28:190 - 00:04:28:739] **Speaker 1:** did in 202.
[00:04:28:790 - 00:04:29:690] **Speaker 1:** We're not replacing it.
[00:04:30:929 - 00:04:32:579] **Speaker 1:** Then we have this DU by DX.
[00:04:32:630 - 00:04:34:299] **Speaker 1:** This is the strain equation, this is the definition of
[00:04:34:299 - 00:04:34:829] **Speaker 1:** strain.
[00:04:36:309 - 00:04:39:649] **Speaker 1:** And we have this relationship between um the general.
[00:04:40:970 - 00:04:43:200] **Speaker 1:** The rate of change of internal normal force and the
[00:04:43:200 - 00:04:44:480] **Speaker 1:** distributed load intensity.
[00:04:50:720 - 00:04:54:299] **Speaker 1:** So that leads us to this governing boundary value problem.
[00:04:59:690 - 00:05:04:200] **Speaker 1:** So given EA F1 and F2 are the elements, so
[00:05:04:200 - 00:05:06:720] **Speaker 1:** we're gonna assume that the elastic modulus is constant, it's
[00:05:06:720 - 00:05:07:739] **Speaker 1:** a homogeneous material.
[00:05:08:160 - 00:05:09:799] **Speaker 1:** We're gonna assume that we have a constant cross sectional
[00:05:09:799 - 00:05:11:149] **Speaker 1:** area, so it's a prismatic element.
[00:05:12:690 - 00:05:14:329] **Speaker 1:** And what we're going to do is find the U
[00:05:14:329 - 00:05:14:850] **Speaker 1:** of X.
[00:05:17:230 - 00:05:21:649] **Speaker 1:** So that's Some as yet.
[00:05:25:549 - 00:05:33:190] **Speaker 1:** undefined equation Linking internal behaviour.
[00:05:40:869 - 00:05:41:529] **Speaker 1:** To know it all.
[00:05:43:329 - 00:05:43:950] **Speaker 1:** Values.
[00:05:48:329 - 00:05:50:619] **Speaker 1:** What we're gonna do is initially we're gonna just assume
[00:05:50:959 - 00:05:52:359] **Speaker 1:** that we've got a small element and we're gonna set
[00:05:52:359 - 00:05:53:399] **Speaker 1:** the right side to zero.
[00:05:54:910 - 00:06:00:040] **Speaker 1:** So initially We're going to assume That our distributed load
[00:06:00:040 - 00:06:01:920] **Speaker 1:** intensity p of X is equal to 0.
[00:06:03:480 - 00:06:04:920] **Speaker 1:** Now, before the end of the 4 weeks, we will
[00:06:04:920 - 00:06:06:359] **Speaker 1:** come back and we can look at how to deal
[00:06:06:359 - 00:06:08:559] **Speaker 1:** with that when it's not 0, but we're just gonna
[00:06:08:559 - 00:06:10:220] **Speaker 1:** make things a little bit simpler on ourselves to start
[00:06:10:220 - 00:06:10:559] **Speaker 1:** with.
[00:06:14:790 - 00:06:17:690] **Speaker 1:** So we need this, this is the governing equation.
[00:06:18:190 - 00:06:19:540] **Speaker 1:** Now the right-hand side is set to 0.
[00:06:19:709 - 00:06:23:160] **Speaker 1:** We need the value of U evaluated at the left-hand
[00:06:23:160 - 00:06:26:350] **Speaker 1:** nodal point, node 1, where X equals 0, needs to
[00:06:26:350 - 00:06:27:269] **Speaker 1:** be equal to D1.
[00:06:28:269 - 00:06:30:450] **Speaker 1:** Then the value of this as yet undefined function.
[00:06:31:769 - 00:06:34:720] **Speaker 1:** Uh, evaluated at X equals L needs to be the
[00:06:34:720 - 00:06:36:649] **Speaker 1:** value D2, which is at node 2.
[00:06:38:040 - 00:06:40:920] **Speaker 1:** So that really encompasses why we, you know, I've, I've
[00:06:40:920 - 00:06:44:000] **Speaker 1:** said this, um, yeah, X for an element always goes
[00:06:44:000 - 00:06:46:920] **Speaker 1:** from node one towards node 2, and that's the consistent
[00:06:46:920 - 00:06:47:440] **Speaker 1:** numbering there.
[00:06:47:559 - 00:06:50:119] **Speaker 1:** So when X equals 0, we're at node 1 and
[00:06:50:119 - 00:06:52:640] **Speaker 1:** that's why that's called D1, and when X equals L,
[00:06:52:720 - 00:06:54:480] **Speaker 1:** that's node 2, that's why it's called D2.
[00:06:54:559 - 00:06:56:399] **Speaker 1:** So that's why it's really important to stick to that
[00:06:56:399 - 00:06:57:239] **Speaker 1:** site convention.
[00:07:00:290 - 00:07:03:179] **Speaker 1:** This is called the, the strong form of the problem.
[00:07:05:109 - 00:07:06:489] **Speaker 1:** Uh, the exact solution can be hard, particularly when you
[00:07:06:489 - 00:07:07:529] **Speaker 1:** go to more general cases.
[00:07:07:730 - 00:07:11:049] **Speaker 1:** Um, the form in court above includes all the conditions
[00:07:11:049 - 00:07:13:809] **Speaker 1:** above to be true for the elements all the way
[00:07:13:809 - 00:07:15:920] **Speaker 1:** from x equals l to x equals x equals 0
[00:07:15:920 - 00:07:16:690] **Speaker 1:** to x equals l.
[00:07:20:010 - 00:07:21:690] **Speaker 1:** It should actually be um.
[00:07:23:230 - 00:07:26:589] **Speaker 1:** X equals 0, and X seems to have disappeared there.
[00:07:29:720 - 00:07:32:630] **Speaker 1:** So the homogeneous strong form that's defined in these equations
[00:07:32:630 - 00:07:36:040] **Speaker 1:** above in step 6 assumes the distributed axial load between
[00:07:36:040 - 00:07:38:970] **Speaker 1:** the nodes is zero, And what we're going to do
[00:07:38:970 - 00:07:40:690] **Speaker 1:** here is we're going to start off with a form
[00:07:40:690 - 00:07:41:410] **Speaker 1:** of this equation.
[00:07:41:570 - 00:07:42:769] **Speaker 1:** So where did this come from?
[00:07:42:970 - 00:07:44:410] **Speaker 1:** It seems like it just came out of nowhere.
[00:07:45:290 - 00:07:47:609] **Speaker 1:** Well, what we're assuming here, we've made, we've made some
[00:07:47:609 - 00:07:49:869] **Speaker 1:** assumptions here, so this is a straight line equation.
[00:07:58:100 - 00:08:00:089] **Speaker 1:** Citizens site, you can compare.
[00:08:01:250 - 00:08:05:790] **Speaker 1:** To Y equals MX + C, that might be a
[00:08:05:790 - 00:08:08:829] **Speaker 1:** more common, um, form that you've just seen for just
[00:08:08:829 - 00:08:10:269] **Speaker 1:** a, a straight line equation.
[00:08:13:670 - 00:08:20:959] **Speaker 1:** And Our choice Of the form of this equation.
[00:08:28:109 - 00:08:37:698] **Speaker 1:** is based upon Our prior knowledge.
[00:08:42:659 - 00:08:44:229] **Speaker 1:** Of how this element will deflect.
[00:09:00:510 - 00:09:01:890] **Speaker 1:** It also defines.
[00:09:06:039 - 00:09:07:179] **Speaker 1:** Limitations.
[00:09:11:239 - 00:09:12:229] **Speaker 0:** In the scope.
[00:09:13:000 - 00:09:19:299] **Speaker 1:** Of problems That can be solved.
[00:09:24:090 - 00:09:25:510] **Speaker 1:** Using this element type.
[00:09:32:960 - 00:09:34:830] **Speaker 1:** So we've assumed here that we have a straight line
[00:09:34:830 - 00:09:37:340] **Speaker 1:** equation and what they're saying is that we just, as
[00:09:37:340 - 00:09:40:390] **Speaker 1:** we move along the element, we're applying a sort of
[00:09:40:390 - 00:09:41:440] **Speaker 1:** linear interpolation.
[00:09:42:250 - 00:09:43:969] **Speaker 1:** Between the values at each end.
[00:09:45:770 - 00:09:48:409] **Speaker 1:** The closer we are to node one, the more influence
[00:09:48:409 - 00:09:50:849] **Speaker 1:** we're gonna take from the value of displacement at node
[00:09:50:849 - 00:09:51:130] **Speaker 1:** one.
[00:09:51:869 - 00:09:53:799] **Speaker 1:** The closer we are to 02, the more influence we'll
[00:09:53:799 - 00:09:54:599] **Speaker 1:** take from that value.
[00:09:55:469 - 00:09:56:830] **Speaker 1:** And we're just doing a linear waiting.
[00:09:58:650 - 00:09:59:489] **Speaker 1:** Why is it a linear weighting?
[00:09:59:570 - 00:10:00:799] **Speaker 1:** Why can we get away with that assumption?
[00:10:00:849 - 00:10:02:750] **Speaker 1:** Why have we used this type of equation?
[00:10:03:169 - 00:10:05:640] **Speaker 1:** Well, we've assumed we've got a constant elastic modulus, a
[00:10:05:640 - 00:10:09:809] **Speaker 1:** constant, um, elastic elastic modulus, constant cross section, and it
[00:10:09:809 - 00:10:11:090] **Speaker 1:** carries a constant axial force.
[00:10:11:289 - 00:10:15:609] **Speaker 1:** So we accept the expect the displacement to vary linearly
[00:10:15:609 - 00:10:16:489] **Speaker 1:** along the element.
[00:10:17:049 - 00:10:19:210] **Speaker 1:** Now if we had an element that varied in cross
[00:10:19:210 - 00:10:24:090] **Speaker 1:** section, suppose it was a trapezoidal bar and it went
[00:10:24:090 - 00:10:26:530] **Speaker 1:** from a, a reasonable cross section at one end to
[00:10:26:530 - 00:10:28:130] **Speaker 1:** a smaller cross section at the other.
[00:10:29:700 - 00:10:32:469] **Speaker 1:** That breaches our assumptions, that's not what we assumed up
[00:10:32:469 - 00:10:34:750] **Speaker 1:** here when we, we set the problem.
[00:10:35:690 - 00:10:39:020] **Speaker 1:** If we had that, we would expect that the strain
[00:10:39:020 - 00:10:39:809] **Speaker 1:** along the bar would change.
[00:10:39:859 - 00:10:40:960] **Speaker 1:** It wouldn't be constant.
[00:10:41:580 - 00:10:43:859] **Speaker 1:** The normal force would be constant.
[00:10:44:609 - 00:10:46:969] **Speaker 1:** Perhaps that was one of our assumptions, but if the
[00:10:46:969 - 00:10:49:460] **Speaker 1:** cross section varies, even if the normal force is constant,
[00:10:49:570 - 00:10:52:219] **Speaker 1:** the, the internal stress and the internal strain will change
[00:10:52:219 - 00:10:53:219] **Speaker 1:** along the length of the bar.
[00:10:53:659 - 00:10:55:539] **Speaker 1:** And as soon as we do that, a straight line
[00:10:55:539 - 00:10:56:940] **Speaker 1:** equation wouldn't be appropriate.
[00:10:58:229 - 00:11:01:909] **Speaker 1:** So that's why what we define here relies on our
[00:11:01:909 - 00:11:04:229] **Speaker 1:** prior knowledge and the assumptions we make about how the
[00:11:04:229 - 00:11:05:090] **Speaker 1:** data forms.
[00:11:05:599 - 00:11:07:590] **Speaker 1:** It sets up the problem, but it also induces its
[00:11:07:590 - 00:11:08:390] **Speaker 1:** limitations.
[00:11:08:590 - 00:11:10:849] **Speaker 1:** So by making this assumption.
[00:11:11:840 - 00:11:14:960] **Speaker 1:** We've basically modelled something that isn't appropriate for using for
[00:11:14:960 - 00:11:18:039] **Speaker 1:** modelling bars where the cross section changes along the length.
[00:11:19:599 - 00:11:21:320] **Speaker 1:** If we were to do that, then we would need
[00:11:21:320 - 00:11:22:979] **Speaker 1:** that parabolic equation in there.
[00:11:27:039 - 00:11:30:580] **Speaker 1:** So A0 and A1 are determined from the boundary conditions.
[00:11:31:200 - 00:11:33:450] **Speaker 1:** They were given above, but I'll just repeat it here,
[00:11:33:840 - 00:11:36:479] **Speaker 1:** where the value evaluated X equals 0 is D1 and
[00:11:36:479 - 00:11:40:080] **Speaker 1:** evaluated the same value of this equation, evaluated at X
[00:11:40:080 - 00:11:41:599] **Speaker 1:** equals L is D2.
[00:11:43:549 - 00:11:45:080] **Speaker 1:** So we can go through and we can substitute those
[00:11:45:080 - 00:11:49:599] **Speaker 1:** in um what we basically substitute U equals 0 into
[00:11:49:599 - 00:11:53:500] **Speaker 1:** the equation above and we get So X equals 0
[00:11:53:500 - 00:11:56:700] **Speaker 1:** into this equation, this turn goes to 0, A 0
[00:11:57:099 - 00:11:58:049] **Speaker 1:** is equal to D1.
[00:11:58:270 - 00:11:59:969] **Speaker 1:** That's the first thing that we can find out quite
[00:11:59:969 - 00:12:00:400] **Speaker 1:** quickly.
[00:12:01:299 - 00:12:03:260] **Speaker 1:** And then we can substitute X equals L into this
[00:12:03:260 - 00:12:08:380] **Speaker 1:** equation, which will be um A0 plus A1 times L.
[00:12:08:780 - 00:12:11:979] **Speaker 1:** We already know what A0 is and we can do
[00:12:11:979 - 00:12:14:919] **Speaker 1:** the substitution and we get that result there.
[00:12:20:039 - 00:12:22:799] **Speaker 1:** So once we evaluate those constants, we can substitute them
[00:12:22:799 - 00:12:25:450] **Speaker 1:** back into the equation and we can have an equation
[00:12:25:450 - 00:12:28:400] **Speaker 1:** that exists all the way along the element.
[00:12:31:369 - 00:12:33:909] **Speaker 1:** So we've got a few Equations here.
[00:12:38:000 - 00:12:40:640] **Speaker 1:** The first one is just substituting these two consonants back
[00:12:40:640 - 00:12:41:809] **Speaker 1:** into the equation above.
[00:12:42:559 - 00:12:44:880] **Speaker 1:** The second one is just grouping like terms.
[00:12:45:049 - 00:12:49:559] **Speaker 1:** So it's generally those two just the same equation, but
[00:12:49:559 - 00:12:51:359] **Speaker 1:** we've grouped all the D1 terms together and we've grouped
[00:12:51:359 - 00:12:52:679] **Speaker 1:** all the D2 terms together.
[00:12:54:039 - 00:12:56:000] **Speaker 1:** Then we can write this like this, where we have
[00:12:56:000 - 00:12:57:940] **Speaker 1:** uh U of X is equal to si 1 times
[00:12:57:940 - 00:13:01:119] **Speaker 1:** X, si 1 of X times D1, and si 2
[00:13:01:119 - 00:13:02:099] **Speaker 1:** of X times D2.
[00:13:03:950 - 00:13:07:229] **Speaker 1:** And of course, in that definition psi 1 of X
[00:13:07:650 - 00:13:08:789] **Speaker 1:** will be 1 minus.
[00:13:09:640 - 00:13:13:409] **Speaker 1:** X upon L and size 2 of X will be
[00:13:13:409 - 00:13:15:049] **Speaker 1:** equal to Xon L.
[00:13:20:979 - 00:13:21:789] **Speaker 1:** So we have some equations.
[00:13:21:869 - 00:13:23:010] **Speaker 1:** We got there relatively simply.
[00:13:23:549 - 00:13:25:489] **Speaker 1:** But just a reminder here, we assumed here.
[00:13:27:549 - 00:13:27:830] **Speaker 1:** Conson A.
[00:13:31:530 - 00:13:36:630] **Speaker 1:** Constantly And a constant normal force.
[00:13:37:710 - 00:13:40:070] **Speaker 1:** In, so the cross sectional area is constant, there's a
[00:13:40:070 - 00:13:44:179] **Speaker 1:** prismatic bar, a constant elastic modulus, homogeneous, same material all
[00:13:44:179 - 00:13:47:349] **Speaker 1:** the way along, and a constant normal force, so.
[00:13:50:559 - 00:13:52:549] **Speaker 1:** That tells us that the distributed load.
[00:13:55:520 - 00:13:57:090] **Speaker 1:** A distributed axial load.
[00:13:58:580 - 00:14:01:700] **Speaker 1:** PF X is equal to 0.
[00:14:05:869 - 00:14:09:820] **Speaker 1:** If the Particular element type we're trying to model violates
[00:14:09:820 - 00:14:13:200] **Speaker 1:** these assumptions, then these equations, we know from the outset
[00:14:13:200 - 00:14:18:489] **Speaker 1:** these equations won't necessarily capture that, uh, appropriately because, um,
[00:14:19:590 - 00:14:20:929] **Speaker 1:** The element doesn't adhere.
[00:14:21:669 - 00:14:24:619] **Speaker 1:** To the underlying assumptions of our system.
[00:14:26:669 - 00:14:29:849] **Speaker 1:** Sci 1 and side 2 are shape functions, and shape
[00:14:29:849 - 00:14:32:380] **Speaker 1:** functions basically are the things that make finite elements finite
[00:14:32:380 - 00:14:32:650] **Speaker 1:** elements.
[00:14:32:770 - 00:14:34:440] **Speaker 1:** So the other things that differ from, say, a finite
[00:14:34:440 - 00:14:38:440] **Speaker 1:** difference method or other numerical methods, shape functions are the
[00:14:38:440 - 00:14:41:130] **Speaker 1:** fundamental thing which defines them.
[00:14:42:369 - 00:14:44:409] **Speaker 1:** It describes the change in UX between nodes, in other
[00:14:44:409 - 00:14:49:210] **Speaker 1:** words, the shape functions interpolate between nodal displacements D1 and
[00:14:49:210 - 00:14:49:739] **Speaker 1:** D2.
[00:14:51:479 - 00:14:53:090] **Speaker 1:** So what we're gonna do is we're actually plot those.
[00:14:53:409 - 00:14:55:090] **Speaker 1:** What do they look like if we were to plot
[00:14:55:090 - 00:14:58:609] **Speaker 1:** slide 1 of X and slide 2 of X against
[00:14:58:609 - 00:15:00:150] **Speaker 1:** position X along the bar.
[00:15:05:859 - 00:15:06:900] **Speaker 1:** That's what they look like, yeah.
[00:15:08:710 - 00:15:11:090] **Speaker 1:** Simple linear equations, so this here.
[00:15:11:909 - 00:15:15:919] **Speaker 1:** Um, They can be defined or plotted.
[00:15:17:669 - 00:15:22:950] **Speaker 1:** If we're right immediately adjacent to node one, we basically
[00:15:22:950 - 00:15:25:549] **Speaker 1:** draw all our influence from the displacement at node one
[00:15:25:549 - 00:15:27:510] **Speaker 1:** and nothing from the displacement at node two.
[00:15:28:070 - 00:15:31:130] **Speaker 1:** As we move along the bar, we draw less influence
[00:15:31:789 - 00:15:35:030] **Speaker 1:** from node one and more influence towards node 2.
[00:15:37:880 - 00:15:51:099] **Speaker 1:** So These shape functions Can be thought of.
[00:15:53:780 - 00:16:00:510] **Speaker 1:** Like Participation factors.
[00:16:04:799 - 00:16:09:419] **Speaker 1:** Whoa Rating factors.
[00:16:17:200 - 00:16:20:969] **Speaker 1:** So just waiting, um, in this case, in this initial
[00:16:20:969 - 00:16:23:030] **Speaker 1:** axial bar case, they are just linear.
[00:16:23:140 - 00:16:25:010] **Speaker 1:** When we get to more complex reaction mechanisms, they won't
[00:16:25:010 - 00:16:26:429] **Speaker 1:** be linear, they'll be more complicated.
[00:16:28:039 - 00:16:29:760] **Speaker 1:** But they're just weighting factors, so the closer we are
[00:16:29:760 - 00:16:32:590] **Speaker 1:** to one node, the more we we the influence of
[00:16:32:590 - 00:16:34:330] **Speaker 1:** the value solved at that node.
[00:16:36:419 - 00:16:38:909] **Speaker 1:** So this, this is a repeat of the previous page,
[00:16:39:059 - 00:16:41:700] **Speaker 1:** so we can think here about um yeah.
[00:16:42:570 - 00:16:45:380] **Speaker 1:** The value of you evaluate X equals 0.5 L, which
[00:16:45:380 - 00:16:47:590] **Speaker 1:** is a linear combination of the two.
[00:16:48:320 - 00:16:51:559] **Speaker 1:** And the value of U X evaluated x equals 0.75L,
[00:16:52:119 - 00:16:53:960] **Speaker 1:** we're drawing a 25% influence.
[00:16:54:440 - 00:16:57:940] **Speaker 1:** So we're essentially going through here and we're gonna take,
[00:16:58:700 - 00:17:01:359] **Speaker 1:** uh, if we went to mid midway, we'd come up
[00:17:01:359 - 00:17:03:969] **Speaker 1:** here, we'd be getting about a value of 0.5 here,
[00:17:04:329 - 00:17:07:800] **Speaker 1:** and the value of 0.5, at 0.75 along.
[00:17:09:428 - 00:17:11:729] **Speaker 1:** We'll be taking a 75% influence here.
[00:17:12:790 - 00:17:14:660] **Speaker 1:** And just a 25% influence here.
[00:17:20:810 - 00:17:23:410] **Speaker 1:** We can also define strain, so strain is by definition
[00:17:23:410 - 00:17:25:729] **Speaker 1:** the rate of change of internal displacement with respect to
[00:17:25:729 - 00:17:29:050] **Speaker 1:** X, and we can substitute in the values divided by
[00:17:29:050 - 00:17:31:489] **Speaker 1:** L, and that will be a constant strain along the
[00:17:31:489 - 00:17:34:050] **Speaker 1:** length of the element because of the assumptions that we've
[00:17:34:050 - 00:17:34:530] **Speaker 1:** applied.
[00:17:37:140 - 00:17:42:099] **Speaker 1:** So the stress is, uh, electric modules times strain.
[00:17:42:920 - 00:17:45:319] **Speaker 1:** We can just substitute the strain value in and we
[00:17:45:319 - 00:17:48:109] **Speaker 1:** can define here is if we simplify that, we end
[00:17:48:109 - 00:17:51:400] **Speaker 1:** up with the the difference between D1 and D2 is
[00:17:51:400 - 00:17:53:400] **Speaker 1:** equal to the change in length divided by the original
[00:17:53:400 - 00:17:53:640] **Speaker 1:** length.
[00:17:53:709 - 00:17:57:079] **Speaker 1:** So this again matches the definitions that you would have
[00:17:57:079 - 00:17:58:520] **Speaker 1:** seen in previous years.
[00:18:00:010 - 00:18:01:329] **Speaker 1:** Previous mechanics classes.
[00:18:12:459 - 00:18:14:339] **Speaker 1:** So I'm actually just just quickly jump back to page
[00:18:14:339 - 00:18:16:829] **Speaker 1:** 10 because I think you've got a blank page in
[00:18:16:829 - 00:18:17:510] **Speaker 1:** your notes there.
[00:18:19:189 - 00:18:21:150] **Speaker 1:** Just wanted to do a quick example.
[00:18:36:260 - 00:18:38:930] **Speaker 1:** So suppose we have some sort of axial truss structure.
[00:18:39:969 - 00:18:41:609] **Speaker 1:** We're gonna have some sort of support here.
[00:18:41:930 - 00:18:43:550] **Speaker 1:** We're gonna have a pin joints.
[00:18:44:469 - 00:18:46:010] **Speaker 1:** Have another pin joint down here.
[00:18:47:890 - 00:18:49:489] **Speaker 1:** There it has the elements attached here.
[00:18:51:969 - 00:18:53:760] **Speaker 1:** Vertical element to here.
[00:19:17:890 - 00:19:19:310] **Speaker 1:** The diagonal elements in here.
[00:19:20:500 - 00:19:22:560] **Speaker 1:** Otherwise if it's all conjointed or be unstable.
[00:19:23:459 - 00:19:28:569] **Speaker 1:** And then we might have a, Element that comes to
[00:19:28:569 - 00:19:30:329] **Speaker 1:** here and the other element.
[00:19:31:439 - 00:19:32:319] **Speaker 1:** It comes up here.
[00:19:33:959 - 00:19:35:619] **Speaker 1:** And then we're gonna hang some load.
[00:19:37:520 - 00:19:37:530] **Speaker 1:** P.
[00:19:39:640 - 00:19:40:760] **Speaker 1:** Of the end of the structure.
[00:19:47:530 - 00:19:52:969] **Speaker 1:** So If we look at this element here in the
[00:19:52:969 - 00:19:53:630] **Speaker 1:** top of that structure.
[00:19:57:140 - 00:19:59:219] **Speaker 1:** What we'll see here is.
[00:20:01:030 - 00:20:02:650] **Speaker 1:** The elements may have.
[00:20:05:890 - 00:20:07:709] **Speaker 1:** The original position of the element maybe here.
[00:20:09:209 - 00:20:11:849] **Speaker 1:** Moving down the page, and it may have moved to
[00:20:11:849 - 00:20:12:270] **Speaker 1:** here.
[00:20:17:550 - 00:20:20:420] **Speaker 1:** We are Doesn't matter here.
[00:20:21:800 - 00:20:22:560] **Speaker 1:** There's D1.
[00:20:23:869 - 00:20:25:010] **Speaker 1:** And this amount here.
[00:20:26:160 - 00:20:27:020] **Speaker 1:** Is D2.
[00:20:27:869 - 00:20:30:839] **Speaker 1:** The amount by which each nodal point has moved.
[00:20:34:719 - 00:20:37:699] **Speaker 1:** We're gonna just quickly sketch a coordinate system on here.
[00:20:41:510 - 00:20:51:239] **Speaker 1:** And remind we're assuming a Constantly in Constantly And a
[00:20:51:239 - 00:20:53:400] **Speaker 1:** consonant A along the island.
[00:20:57:229 - 00:21:00:510] **Speaker 1:** If we assume here that D1 is equal to 0.1
[00:21:00:510 - 00:21:03:750] **Speaker 1:** metres, and we'll assume here that D2.
[00:21:04:430 - 00:21:07:189] **Speaker 1:** is equal to 0.2 metres.
[00:21:08:270 - 00:21:10:079] **Speaker 1:** I know these are quite large deflections.
[00:21:10:199 - 00:21:12:560] **Speaker 1:** Um, we haven't actually said the overall length of the
[00:21:12:560 - 00:21:13:119] **Speaker 1:** element, but.
[00:21:14:760 - 00:21:16:729] **Speaker 1:** Some nice round numbers that makes the math easy.
[00:21:17:290 - 00:21:19:339] **Speaker 1:** So we've got an element here.
[00:21:20:939 - 00:21:22:560] **Speaker 1:** Uh, if we look at this top left element.
[00:21:24:030 - 00:21:26:160] **Speaker 1:** It's left-hand side is constrained to a support, so it
[00:21:26:160 - 00:21:27:859] **Speaker 1:** can only stretch or compress like this.
[00:21:29:739 - 00:21:31:709] **Speaker 1:** You can only stretch your test, the left-hand side must
[00:21:31:709 - 00:21:32:390] **Speaker 1:** stay stationary.
[00:21:33:390 - 00:21:35:520] **Speaker 1:** But if you look at this element, there's two things
[00:21:35:520 - 00:21:36:339] **Speaker 1:** that can go on.
[00:21:37:290 - 00:21:39:390] **Speaker 1:** One is that it can move in space.
[00:21:40:390 - 00:21:42:719] **Speaker 1:** Without stretching or compression, compressing.
[00:21:43:800 - 00:21:46:599] **Speaker 1:** So if the load was installed on this node.
[00:21:47:949 - 00:21:50:380] **Speaker 1:** Then that load would transmit down through these two elements
[00:21:50:380 - 00:21:52:290] **Speaker 1:** to the supports and the right hand side of the
[00:21:52:290 - 00:21:53:739] **Speaker 1:** structure actually would be unstressed.
[00:21:54:140 - 00:21:56:619] **Speaker 1:** There wouldn't be, the load wouldn't pass through those, so
[00:21:56:619 - 00:21:58:339] **Speaker 1:** none of those elements would actually have an internal stress
[00:21:58:339 - 00:21:59:060] **Speaker 1:** or strain on them.
[00:22:00:380 - 00:22:02:540] **Speaker 1:** But this element would still move in space, and it
[00:22:02:540 - 00:22:05:459] **Speaker 1:** would move because of the fact that the elements it's
[00:22:05:459 - 00:22:08:300] **Speaker 1:** connected to are stretching and compressing as a result of
[00:22:08:300 - 00:22:09:219] **Speaker 1:** the applied loads.
[00:22:10:579 - 00:22:14:250] **Speaker 1:** So what we see here Let's assume the initial length
[00:22:14:250 - 00:22:15:079] **Speaker 1:** was 1 metre.
[00:22:16:560 - 00:22:19:329] **Speaker 1:** The left-hand side's moved by 0.1, the right-hand side's moved
[00:22:19:329 - 00:22:20:050] **Speaker 1:** by 0.2.
[00:22:20:560 - 00:22:23:010] **Speaker 1:** So it's translated, it's undergone sort of a a rigid
[00:22:23:010 - 00:22:25:010] **Speaker 1:** body movement in space.
[00:22:25:130 - 00:22:26:800] **Speaker 1:** It's moved to the right by 0.1 metres.
[00:22:27:170 - 00:22:30:290] **Speaker 1:** And then over and above that, it's also stretched by
[00:22:30:290 - 00:22:31:510] **Speaker 1:** 0.1 metres as well.
[00:22:32:599 - 00:22:33:680] **Speaker 1:** And that's a combination.
[00:22:33:959 - 00:22:36:119] **Speaker 1:** So the first, the rigid body component is just by
[00:22:36:119 - 00:22:38:520] **Speaker 1:** virtue of the things that it's attached to a stretching
[00:22:38:520 - 00:22:41:540] **Speaker 1:** and compressing and then on top of that itself is
[00:22:41:869 - 00:22:44:160] **Speaker 1:** is stretching due to the applied load.
[00:22:46:089 - 00:22:48:130] **Speaker 1:** So if we were to quickly go through here, and
[00:22:48:130 - 00:22:49:150] **Speaker 1:** we were to work out.
[00:22:50:280 - 00:22:55:599] **Speaker 1:** What is U evaluated at X equals 0.25L?
[00:22:57:750 - 00:22:59:500] **Speaker 1:** What would the value be?
[00:23:04:930 - 00:23:06:599] **Speaker 1:** Maybe we'll start at the middle midpoint, it's a little
[00:23:06:599 - 00:23:06:930] **Speaker 1:** bit easier.
[00:23:07:050 - 00:23:11:630] **Speaker 1:** So we'll go U at X equals 0.5 L.
[00:23:13:689 - 00:23:15:689] **Speaker 1:** So the left-hand side is moved 0.1 metres, the right
[00:23:15:689 - 00:23:16:770] **Speaker 1:** sides moved 0.2.
[00:23:17:959 - 00:23:19:959] **Speaker 1:** What would we expect a point halfway along the bar
[00:23:19:959 - 00:23:20:579] **Speaker 1:** to have moved?
[00:23:25:589 - 00:23:26:589] **Speaker 1:** Yep, so 0.15.
[00:23:26:709 - 00:23:30:270] **Speaker 1:** So you just, um, essentially it's a a 50% weighting
[00:23:30:430 - 00:23:32:670] **Speaker 1:** on the values at each end, and that gives you
[00:23:32:670 - 00:23:35:520] **Speaker 1:** a value of 0.15 metres.
[00:23:38:140 - 00:23:39:739] **Speaker 1:** What if we were to go back to the value
[00:23:39:739 - 00:23:40:880] **Speaker 1:** of 1 quarter of the way along?
[00:23:42:369 - 00:23:44:489] **Speaker 1:** How much would you expect that piece of bar to
[00:23:44:489 - 00:23:45:020] **Speaker 1:** have moved?
[00:23:50:310 - 00:23:50:949] **Speaker 1:** Yeah, perfect.
[00:23:51:069 - 00:23:51:569] **Speaker 1:** Thank you.
[00:23:52:540 - 00:23:54:400] **Speaker 1:** It's 0.125 metres.
[00:23:56:369 - 00:23:58:270] **Speaker 1:** And of course if we were to go through here
[00:23:58:530 - 00:24:02:150] **Speaker 1:** at you, evaluate X equals 0.75 L.
[00:24:03:020 - 00:24:05:930] **Speaker 1:** We would expect 0.175.
[00:24:07:000 - 00:24:08:280] **Speaker 1:** metres to fiction.
[00:24:10:819 - 00:24:12:859] **Speaker 1:** Now, I just wanted to do that example because what
[00:24:12:859 - 00:24:15:099] **Speaker 1:** you're doing there, what you're doing in your head by
[00:24:15:099 - 00:24:18:420] **Speaker 1:** looking at that bar and inferring internal behaviour from the
[00:24:18:420 - 00:24:19:939] **Speaker 1:** values at the end points, that's what we call a
[00:24:19:939 - 00:24:21:079] **Speaker 1:** boundary value problem.
[00:24:21:579 - 00:24:24:459] **Speaker 1:** In your head, you are doing the job of a
[00:24:24:459 - 00:24:25:020] **Speaker 1:** shape function.
[00:24:26:569 - 00:24:27:880] **Speaker 1:** Shape functions through that relationship.
[00:24:27:930 - 00:24:30:089] **Speaker 1:** They take values at the end points and they infer
[00:24:30:089 - 00:24:31:439] **Speaker 1:** internal behaviour from that.
[00:24:31:729 - 00:24:34:560] **Speaker 1:** And it's the that those shape functions are the fundamental
[00:24:34:560 - 00:24:37:329] **Speaker 1:** building blocks of finite element analysis.
[00:24:41:619 - 00:24:46:689] **Speaker 1:** So The internal element of actions.
[00:24:52:170 - 00:24:56:910] **Speaker 1:** are inferred From values at the end point.
[00:25:07:040 - 00:25:09:839] **Speaker 1:** Now an obvious question might be, well, if this is
[00:25:09:839 - 00:25:12:119] **Speaker 1:** so easy and we can do it in our head,
[00:25:12:400 - 00:25:14:800] **Speaker 1:** why do we have this complex mathematical system to define
[00:25:14:800 - 00:25:17:099] **Speaker 1:** something that we can, it's quite obvious.
[00:25:17:719 - 00:25:19:260] **Speaker 1:** Well, there's a very simple answer to that.
[00:25:22:500 - 00:25:25:410] **Speaker 1:** This is the first element type we're gonna look at.
[00:25:26:920 - 00:25:28:530] **Speaker 1:** But over the next few weeks, we're going to get
[00:25:28:530 - 00:25:29:930] **Speaker 1:** to a point, say for example, if you have a
[00:25:29:930 - 00:25:30:689] **Speaker 1:** cantilever bean.
[00:25:32:430 - 00:25:34:469] **Speaker 1:** Suppose we've got a cantilever bean, it's going to have
[00:25:34:469 - 00:25:35:250] **Speaker 1:** a constant.
[00:25:39:160 - 00:25:40:880] **Speaker 1:** E A.
[00:25:41:739 - 00:25:45:880] **Speaker 1:** I, a consonant modulus cross-sectional area and second momentive area.
[00:25:47:180 - 00:25:51:729] **Speaker 1:** And after the application of the load, this thing's gonna
[00:25:51:729 - 00:25:53:969] **Speaker 1:** deflect down, it's gonna go into sort of drooped position
[00:25:53:969 - 00:25:54:709] **Speaker 1:** like this.
[00:25:58:770 - 00:26:02:660] **Speaker 1:** And This year.
[00:26:04:520 - 00:26:07:959] **Speaker 1:** If this was 0.1 metres, nice simple ground value.
[00:26:08:130 - 00:26:10:420] **Speaker 1:** So we know that all the way along the length,
[00:26:10:479 - 00:26:13:000] **Speaker 1:** the tip is detected downwards by 0.1 metres.
[00:26:15:430 - 00:26:17:589] **Speaker 1:** If instead we were to say, what is the value,
[00:26:17:630 - 00:26:18:430] **Speaker 1:** we're gonna call it the.
[00:26:23:469 - 00:26:24:209] **Speaker 1:** At X.
[00:26:24:979 - 00:26:26:469] **Speaker 1:** Equals 0.5 L.
[00:26:29:060 - 00:26:31:290] **Speaker 1:** Does anyone want to have a guess at what the
[00:26:31:589 - 00:26:34:109] **Speaker 1:** deflection is halfway along a turto cantilever?
[00:26:37:329 - 00:26:37:619] **Speaker 1:** Sir.
[00:26:38:500 - 00:26:39:319] **Speaker 1:** 0.25.
[00:26:39:910 - 00:26:42:050] **Speaker 1:** So the tip here is delta.
[00:26:42:640 - 00:26:45:650] **Speaker 1:** The tipto value is PL cubed over 3DI.
[00:26:46:670 - 00:26:48:859] **Speaker 1:** And if you look at the full equation, uh, it's
[00:26:48:859 - 00:26:49:969] **Speaker 1:** a cubic relationship.
[00:26:50:229 - 00:26:55:400] **Speaker 1:** So if you're halfway along, it's the cube of 0.5.
[00:26:55:550 - 00:26:57:810] **Speaker 1:** So it's actually gonna be a V.
[00:26:59:020 - 00:27:02:550] **Speaker 1:** X of 0.5L will be equal to.
[00:27:03:400 - 00:27:03:790] **Speaker 1:** 0.
[00:27:06:020 - 00:27:08:270] **Speaker 1:** 0125 millimetres.
[00:27:09:579 - 00:27:13:619] **Speaker 1:** You know Once you get into more complex reaction mechanisms,
[00:27:14:030 - 00:27:17:469] **Speaker 1:** those interpolations, those inferring of internal element actions won't be
[00:27:17:469 - 00:27:19:829] **Speaker 1:** something you can necessarily do easily in your head.
[00:27:20:150 - 00:27:22:989] **Speaker 1:** Um, the frame is the same framework for quite simple
[00:27:22:989 - 00:27:25:410] **Speaker 1:** problems and much more complicated problems.
[00:27:27:130 - 00:27:29:650] **Speaker 1:** If we then wanted to go a little bit further
[00:27:29:650 - 00:27:29:849] **Speaker 1:** again.
[00:27:30:560 - 00:27:32:719] **Speaker 1:** Again, and we wanted to say.
[00:27:33:489 - 00:27:37:329] **Speaker 1:** Maybe we've put um an axial load on here and
[00:27:37:329 - 00:27:39:390] **Speaker 1:** we've also got a moment.
[00:27:40:219 - 00:27:43:260] **Speaker 1:** So maybe that moment's upwards to counteract, so that will
[00:27:43:260 - 00:27:46:780] **Speaker 1:** the moment will actually deflect upwards, the sheer force will
[00:27:46:780 - 00:27:50:459] **Speaker 1:** deflect downwards, and if we want to infer values along
[00:27:50:459 - 00:27:52:660] **Speaker 1:** the length of that, there's gonna be a lot more
[00:27:52:660 - 00:27:52:939] **Speaker 1:** going on.
[00:27:53:020 - 00:27:55:300] **Speaker 1:** It's not gonna be something that's easy to be like
[00:27:55:300 - 00:27:56:420] **Speaker 1:** you could easily do in your head.
[00:27:57:630 - 00:27:59:510] **Speaker 1:** And that's where shape functions really come into their own.
[00:27:59:550 - 00:28:02:229] **Speaker 1:** Once we have the mathematical framework in place, all of
[00:28:02:229 - 00:28:05:030] **Speaker 1:** this just happens really easily and really quickly.
[00:28:08:770 - 00:28:10:339] **Speaker 1:** So just um.
[00:28:11:410 - 00:28:15:540] **Speaker 1:** Yeah, opportunity there to just hopefully understand why we're doing
[00:28:15:540 - 00:28:16:300] **Speaker 1:** this mathematical framework.
[00:28:16:459 - 00:28:17:020] **Speaker 1:** a question up here.
[00:28:19:699 - 00:28:20:939] **Speaker 1:** Uh, it should be metres, sorry.
[00:28:21:660 - 00:28:23:020] **Speaker 1:** Thanks for pointing that out, so.
[00:28:41:050 - 00:28:43:410] **Speaker 1:** So if we jump back to page, well I just
[00:28:43:410 - 00:28:45:239] **Speaker 1:** quickly, is there any questions on that before we move
[00:28:45:239 - 00:28:45:510] **Speaker 1:** on?
[00:28:57:589 - 00:29:00:369] **Speaker 1:** So equation 9 defines the space from x equals 0
[00:29:00:369 - 00:29:01:089] **Speaker 1:** to x equals l.
[00:29:01:699 - 00:29:05:430] **Speaker 1:** Your stiffness matrix relating the element applied forcing to the
[00:29:05:430 - 00:29:06:910] **Speaker 1:** this corresponding deflections.
[00:29:07:670 - 00:29:09:339] **Speaker 1:** So equation line was our.
[00:29:10:650 - 00:29:14:270] **Speaker 1:** You have X Now axial shape function.
[00:29:16:510 - 00:29:21:030] **Speaker 1:** We recall from equation 4, this was the normal force
[00:29:21:030 - 00:29:23:680] **Speaker 1:** was equal to less modulus cross-sectional area times strain.
[00:29:24:109 - 00:29:26:550] **Speaker 1:** We can substitute that back in, and that tells us
[00:29:26:550 - 00:29:29:640] **Speaker 1:** that the normal force is EA overl signs the change
[00:29:29:640 - 00:29:30:750] **Speaker 1:** in length of the element.
[00:29:31:189 - 00:29:31:510] **Speaker 1:** So.
[00:29:32:489 - 00:29:34:569] **Speaker 1:** This bracketed term here.
[00:29:37:030 - 00:29:38:949] **Speaker 1:** done a terrible job of drawing that bracket.
[00:29:39:489 - 00:29:42:050] **Speaker 1:** This here is your change in length, so that the
[00:29:42:050 - 00:29:42:949] **Speaker 1:** amount by which.
[00:29:43:689 - 00:29:46:650] **Speaker 1:** Um, the difference between the, the deflection of the two
[00:29:46:650 - 00:29:49:329] **Speaker 1:** ends is equal to how much the elements stretched or
[00:29:49:329 - 00:29:49:949] **Speaker 1:** compress.
[00:29:52:079 - 00:29:55:630] **Speaker 1:** We can write that as EA over L times delta
[00:29:55:630 - 00:29:56:040] **Speaker 1:** L.
[00:29:56:359 - 00:29:58:060] **Speaker 1:** We can create that as EA.
[00:29:59:030 - 00:30:01:680] **Speaker 1:** Dot L over L, which is E.
[00:30:02:359 - 00:30:03:760] **Speaker 1:** A strain.
[00:30:05:060 - 00:30:10:339] **Speaker 1:** Which is Strain times lastic modulus times area, which is
[00:30:10:339 - 00:30:13:739] **Speaker 1:** stress times area, normal stress times the normal cross sectional
[00:30:13:739 - 00:30:14:060] **Speaker 1:** area.
[00:30:15:890 - 00:30:18:369] **Speaker 1:** So again, this is just everything agrees and matches to
[00:30:18:369 - 00:30:19:410] **Speaker 1:** what you're doing on 202.
[00:30:20:640 - 00:30:21:550] **Speaker 1:** We're not replacing it.
[00:30:25:069 - 00:30:27:589] **Speaker 1:** So that tells us that the axial normal force N
[00:30:27:589 - 00:30:29:010] **Speaker 1:** is constant torque way along the element.
[00:30:30:290 - 00:30:32:619] **Speaker 1:** And we also can evaluate things at the two ends.
[00:30:32:689 - 00:30:34:359] **Speaker 1:** So if we take that bar.
[00:30:35:900 - 00:30:37:199] **Speaker 1:** And we're gonna just take a little.
[00:30:37:969 - 00:30:40:589] **Speaker 1:** Across the little free body diagram section.
[00:30:41:310 - 00:30:43:439] **Speaker 1:** At each end, and we're gonna apply a free body
[00:30:43:439 - 00:30:46:770] **Speaker 1:** diagram and horizontal force equilibrium.
[00:30:47:229 - 00:30:50:069] **Speaker 1:** The force F1 is to the right, then the normal
[00:30:50:069 - 00:30:52:150] **Speaker 1:** force evaluated at X equals 0.
[00:30:53:449 - 00:30:57:290] **Speaker 1:** And that tells us there that the force F1 is
[00:30:57:290 - 00:31:00:329] **Speaker 1:** equal to EA over L times the change, the difference
[00:31:00:329 - 00:31:01:689] **Speaker 1:** between the two deflection values.
[00:31:03:400 - 00:31:05:430] **Speaker 1:** So you just, there's an interesting thing to look at
[00:31:05:430 - 00:31:05:770] **Speaker 1:** here.
[00:31:08:030 - 00:31:09:699] **Speaker 1:** If D1 is greater than D2.
[00:31:10:880 - 00:31:13:290] **Speaker 1:** That means the left-hand side has moved to the right
[00:31:13:290 - 00:31:16:359] **Speaker 1:** by a greater amount than the right-hand side has moved
[00:31:16:359 - 00:31:16:839] **Speaker 1:** to the right.
[00:31:16:949 - 00:31:19:319] **Speaker 1:** So that means the bar will actually shorten.
[00:31:19:670 - 00:31:21:839] **Speaker 1:** There'll be the the final length of the bar will
[00:31:21:839 - 00:31:24:060] **Speaker 1:** be shorter than it was previously.
[00:31:25:670 - 00:31:28:719] **Speaker 1:** And this value will be positive.
[00:31:30:160 - 00:31:33:609] **Speaker 1:** That will give a positive value of F1 and the
[00:31:33:609 - 00:31:37:800] **Speaker 1:** force is pointing inwards, so you'd expect basically shortening, the
[00:31:37:800 - 00:31:41:239] **Speaker 1:** force will be compressive because this is pointing inwards and
[00:31:41:239 - 00:31:41:939] **Speaker 1:** it's positive.
[00:31:43:650 - 00:31:45:030] **Speaker 1:** We can do the same thing on the right-hand side,
[00:31:45:130 - 00:31:46:770] **Speaker 1:** we apply the same method and we get a very
[00:31:46:770 - 00:31:49:530] **Speaker 1:** similar looking equation, but it's not, it's not identical.
[00:31:49:609 - 00:31:52:910] **Speaker 1:** It's if you notice these two values are reversed.
[00:31:54:060 - 00:31:56:280] **Speaker 1:** So here, if D1 was greater than D2.
[00:31:57:890 - 00:32:01:130] **Speaker 1:** It means the bar's moved across, but it's also compressed
[00:32:01:130 - 00:32:01:709] **Speaker 1:** a little bit.
[00:32:02:849 - 00:32:05:790] **Speaker 1:** That means that this bracketed term will actually be negative
[00:32:06:010 - 00:32:07:650] **Speaker 1:** and we'll get a negative value for F2.
[00:32:07:810 - 00:32:10:079] **Speaker 1:** So we would get this would be negative, which means
[00:32:10:079 - 00:32:13:089] **Speaker 1:** it would actually point inwards and we'd have two inwards
[00:32:13:089 - 00:32:18:869] **Speaker 1:** loads which would support the calculation of a shortening compression
[00:32:19:329 - 00:32:20:349] **Speaker 1:** occurring within the element.
[00:32:21:969 - 00:32:23:910] **Speaker 1:** If we combine that into a matrix form.
[00:32:25:199 - 00:32:28:439] **Speaker 1:** We've now got the first time we see our stiffness
[00:32:28:439 - 00:32:29:000] **Speaker 1:** equation.
[00:32:29:199 - 00:32:32:319] **Speaker 1:** So this is just Hooke's law applied in a matrix
[00:32:32:319 - 00:32:32:800] **Speaker 1:** sense.
[00:32:33:500 - 00:32:35:900] **Speaker 1:** We have a vector of forces, a vector of defections,
[00:32:35:979 - 00:32:39:079] **Speaker 1:** and in some stiffness terms that relate those two.
[00:32:40:910 - 00:32:42:550] **Speaker 1:** Now, it might be great to say right, we've got
[00:32:42:550 - 00:32:44:510] **Speaker 1:** a solution, we've got a matrix, we can solve it.
[00:32:44:949 - 00:32:45:530] **Speaker 1:** Perfect.
[00:32:46:189 - 00:32:47:829] **Speaker 1:** One thing we need to look at here is we
[00:32:47:829 - 00:32:49:050] **Speaker 1:** have two unknowns.
[00:32:50:689 - 00:32:52:040] **Speaker 1:** We have 2 equations.
[00:32:54:449 - 00:32:55:599] **Speaker 1:** So we can't solve this.
[00:33:09:229 - 00:33:11:750] **Speaker 1:** Well, I guess, to be fair, um.
[00:33:12:739 - 00:33:15:670] **Speaker 1:** Yeah, it might be, yeah, 2 and 2 equations sounds
[00:33:15:670 - 00:33:18:130] **Speaker 1:** good, cause that would normally be something we can solve.
[00:33:20:010 - 00:33:21:579] **Speaker 1:** But if you actually look at the two equations, they're
[00:33:21:579 - 00:33:22:880] **Speaker 1:** not independent equations.
[00:33:24:540 - 00:33:26:890] **Speaker 1:** The first one is just -1 times the first.
[00:33:26:900 - 00:33:28:739] **Speaker 1:** The second equation is just -1 times the first.
[00:33:29:219 - 00:33:37:369] **Speaker 1:** So Normally This is solvable.
[00:33:41:880 - 00:33:43:219] **Speaker 1:** But the two equations.
[00:33:47:660 - 00:33:49:699] **Speaker 1:** are not independent.
[00:33:54:140 - 00:33:56:739] **Speaker 1:** So it's not sufficient to just say 2 equations, 2
[00:33:56:739 - 00:33:59:719] **Speaker 1:** unknowns, they need to be 2 independent equations.
[00:34:00:660 - 00:34:01:640] **Speaker 1:** To be able to solve them.
[00:34:04:160 - 00:34:05:380] **Speaker 1:** So the obvious question.
[00:34:07:680 - 00:34:08:350] **Speaker 1:** What's missing?
[00:34:08:520 - 00:34:09:790] **Speaker 1:** What do, what do we not know?
[00:34:10:000 - 00:34:11:919] **Speaker 1:** What, what key piece of information do we need to
[00:34:11:919 - 00:34:14:540] **Speaker 1:** add in to make this solvable?
[00:34:14:959 - 00:34:17:219] **Speaker 1:** Well, it kind of comes back to the spring here,
[00:34:17:398 - 00:34:19:760] **Speaker 1:** but at the moment this thing's just kind of floating
[00:34:19:760 - 00:34:20:459] **Speaker 1:** in space.
[00:34:22:080 - 00:34:25:919] **Speaker 1:** And you could put D1 and D2.
[00:34:26:148 - 00:34:28:320] **Speaker 1:** So if D1 was 1 metre and D2 was 1
[00:34:28:320 - 00:34:30:898] **Speaker 1:** metre, it would mean that it's moved in space.
[00:34:31:600 - 00:34:32:898] **Speaker 1:** But there's no force on the bar.
[00:34:33:860 - 00:34:36:260] **Speaker 1:** If D1 was 5 metres and D2 was 5 metres,
[00:34:36:469 - 00:34:38:330] **Speaker 1:** yeah, it's moved now moved 5 metres in space, but
[00:34:38:330 - 00:34:40:138] **Speaker 1:** there's no load on it, there's no force, there's no
[00:34:40:138 - 00:34:43:300] **Speaker 1:** internal deflection, there's no stress, there's no strain, but it's
[00:34:43:300 - 00:34:44:199] **Speaker 1:** moving in space.
[00:34:45:549 - 00:34:47:438] **Speaker 1:** That's what we refer to as rigid body motion.
[00:34:49:628 - 00:34:51:070] **Speaker 1:** Where it's just, there's nothing constrained.
[00:34:51:148 - 00:34:53:148] **Speaker 1:** We haven't, we haven't yet applied any constraints.
[00:34:53:189 - 00:34:55:510] **Speaker 1:** We haven't applied a boundary condition like a support point
[00:34:55:510 - 00:34:58:909] **Speaker 1:** or something that actually locks this down to say a
[00:34:58:909 - 00:35:00:850] **Speaker 1:** support such that it has to stretch or compress.
[00:35:01:590 - 00:35:03:550] **Speaker 1:** That's the key piece of missing information.
[00:35:07:530 - 00:35:12:879] **Speaker 1:** So, All the stuff here.
[00:35:15:000 - 00:35:15:790] **Speaker 1:** Is.
[00:35:16:879 - 00:35:18:389] **Speaker 1:** The stiffness matrix.
[00:35:22:810 - 00:35:29:229] **Speaker 1:** Katie For the bar element.
[00:35:34:189 - 00:35:45:479] **Speaker 1:** That relates Applied loads Two corresponding deflections.
[00:36:08:629 - 00:36:10:310] **Speaker 1:** So we're quite a long way towards being able to
[00:36:10:310 - 00:36:10:750] **Speaker 1:** solve the problem.
[00:36:10:820 - 00:36:13:090] **Speaker 1:** We've got the element type now, but what we need
[00:36:13:090 - 00:36:15:030] **Speaker 1:** the key piece of information is how do we actually
[00:36:15:030 - 00:36:18:070] **Speaker 1:** link multiple elements together or how even just 11 element,
[00:36:18:169 - 00:36:20:189] **Speaker 1:** how do we introduce that support point?
[00:36:20:270 - 00:36:22:510] **Speaker 1:** How do we indicate that one part of that is
[00:36:22:510 - 00:36:25:870] **Speaker 1:** actually linked to a support point and is constrained from
[00:36:25:870 - 00:36:26:330] **Speaker 1:** moving?
[00:36:33:570 - 00:36:40:350] **Speaker 1:** So KA is single, so, um, when we say de
[00:36:40:350 - 00:36:41:709] **Speaker 1:** here that is the determinant.
[00:36:42:620 - 00:36:45:810] **Speaker 1:** The Matrix.
[00:36:47:830 - 00:36:48:550] **Speaker 1:** Determinant.
[00:36:54:800 - 00:36:58:169] **Speaker 1:** Um, you can also, if we went through here, it
[00:36:58:169 - 00:37:00:929] **Speaker 1:** has, it has no unique solution because we could have
[00:37:01:409 - 00:37:06:709] **Speaker 1:** any number of Different values in here for D1 and
[00:37:06:709 - 00:37:10:189] **Speaker 1:** D2 that lead to the bar moving without any force
[00:37:10:189 - 00:37:10:949] **Speaker 1:** existing within it.
[00:37:12:489 - 00:37:15:020] **Speaker 1:** So you get motion without force when the structure is
[00:37:15:020 - 00:37:15:780] **Speaker 1:** not constrained.
[00:37:17:010 - 00:37:20:120] **Speaker 1:** And this holds for any displacements, no displacements where D1
[00:37:20:120 - 00:37:20:679] **Speaker 1:** equals D2.
[00:37:20:729 - 00:37:23:239] **Speaker 1:** So it's an entire set of all numbers from negative
[00:37:23:239 - 00:37:26:739] **Speaker 1:** infinity to plus infinity provided D1 and D2 are equal.
[00:37:28:709 - 00:37:29:959] **Speaker 1:** You can't get a unique solution.
[00:37:35:149 - 00:37:38:790] **Speaker 1:** So the question, um, what happens if E and A
[00:37:38:790 - 00:37:40:989] **Speaker 1:** varies over the length from zero to L?
[00:37:41:149 - 00:37:44:159] **Speaker 1:** What if, essentially, what if the element we're trying to
[00:37:44:159 - 00:37:48:030] **Speaker 1:** model doesn't adhere to our underlying assumptions?
[00:37:48:909 - 00:37:51:229] **Speaker 1:** Well, we either need a new element or we need
[00:37:51:229 - 00:37:52:949] **Speaker 1:** to use new elements.
[00:37:56:520 - 00:37:59:280] **Speaker 1:** So what we could do is take a a shape
[00:37:59:280 - 00:38:01:699] **Speaker 1:** like this, say with an axial bar.
[00:38:02:620 - 00:38:04:520] **Speaker 1:** Where we have a shape.
[00:38:06:070 - 00:38:07:280] **Speaker 1:** That looks like this.
[00:38:11:310 - 00:38:12:850] **Speaker 1:** We've got some sort of load on here.
[00:38:14:209 - 00:38:17:020] **Speaker 1:** That bar doesn't adhere to our underlying assumptions.
[00:38:17:800 - 00:38:21:520] **Speaker 1:** But what we could do here is use a whole
[00:38:21:520 - 00:38:24:040] **Speaker 1:** lot of smaller bar elements.
[00:38:34:669 - 00:38:34:679] **Speaker 1:** I.
[00:38:42:939 - 00:38:44:699] **Speaker 1:** And we collectively.
[00:38:45:889 - 00:38:49:330] **Speaker 1:** Could model that by having a series of elements where
[00:38:49:610 - 00:38:55:129] **Speaker 1:** each one in its own right has a constant cross-section.
[00:38:56:860 - 00:38:58:790] **Speaker 1:** Haven't drawn that very well at all, but the idea
[00:38:58:790 - 00:39:02:979] **Speaker 1:** is that that matches a a line like the, the
[00:39:02:979 - 00:39:03:659] **Speaker 1:** one above.
[00:39:06:179 - 00:39:07:889] **Speaker 1:** And we can break up multiple elements.
[00:39:08:649 - 00:39:10:300] **Speaker 1:** Which then match this behaviour.
[00:39:16:290 - 00:39:17:659] **Speaker 1:** So when we have this rigid body motion.
[00:39:19:020 - 00:39:22:100] **Speaker 1:** A key part of this course is that if you
[00:39:22:100 - 00:39:24:110] **Speaker 1:** then progress on to using a commercial package, you have
[00:39:24:110 - 00:39:27:510] **Speaker 1:** some idea about what's happening and what's going on when
[00:39:27:510 - 00:39:28:449] **Speaker 1:** you get errors.
[00:39:28:669 - 00:39:32:350] **Speaker 1:** And what you'll often see in a commercial package if
[00:39:32:350 - 00:39:35:500] **Speaker 1:** you're doing an analysis, if you haven't applied boundary conditions
[00:39:35:500 - 00:39:39:149] **Speaker 1:** that actually properly constrain the system, you sometimes get a
[00:39:39:149 - 00:39:43:110] **Speaker 1:** warning saying rigid body modes detected or it could be
[00:39:43:110 - 00:39:45:510] **Speaker 1:** uh a thing saying weak springs have been added to
[00:39:45:510 - 00:39:47:949] **Speaker 1:** constrain rigid body motion.
[00:39:48:969 - 00:39:51:709] **Speaker 1:** And that way they're saying is that there's insufficient support.
[00:39:52:510 - 00:39:56:530] **Speaker 1:** Mathematically, this thing isn't constrained in space and therefore, um,
[00:39:56:709 - 00:40:00:419] **Speaker 1:** mathematically the system wasn't able to solve that and some
[00:40:00:419 - 00:40:02:709] **Speaker 1:** of the codes were automatically put in some weak springs
[00:40:02:709 - 00:40:05:889] **Speaker 1:** um that just to constrain those those motions.
[00:40:06:310 - 00:40:07:969] **Speaker 1:** Otherwise what you could do is you could put in
[00:40:08:229 - 00:40:10:189] **Speaker 1:** 1 metre bar, you put a load on it and
[00:40:10:189 - 00:40:12:010] **Speaker 1:** you get 10 kilometres of displacement out.
[00:40:12:979 - 00:40:14:560] **Speaker 1:** That's because the whole thing's moving in space.
[00:40:17:510 - 00:40:21:340] **Speaker 1:** So A quick summary.
[00:40:22:320 - 00:40:24:879] **Speaker 1:** Of shape functions because this really is the most fundamental
[00:40:24:879 - 00:40:25:300] **Speaker 1:** part.
[00:40:26:840 - 00:40:30:439] **Speaker 1:** Of Fun elements.
[00:40:32:709 - 00:40:34:669] **Speaker 1:** The shape functions have two key purposes.
[00:40:35:639 - 00:40:38:729] **Speaker 1:** To enable a set of equations to be developed for
[00:40:38:729 - 00:40:42:370] **Speaker 1:** solving displacements calculated and only a few selected discrete points
[00:40:42:370 - 00:40:45:479] **Speaker 1:** within the structure, but having those points be representative of
[00:40:45:479 - 00:40:46:370] **Speaker 1:** the larger structure.
[00:40:48:080 - 00:40:50:479] **Speaker 1:** Once the displacements are solved, we can then use the
[00:40:50:479 - 00:40:54:360] **Speaker 1:** same shape functions to then breakdown and interpret and understand
[00:40:54:360 - 00:40:56:219] **Speaker 1:** what's going on internally within the elements.
[00:40:57:790 - 00:40:59:899] **Speaker 1:** So they both build up and they break down.
[00:41:00:260 - 00:41:03:340] **Speaker 1:** They're essentially the most fundamental building block of everything that
[00:41:03:340 - 00:41:03:979] **Speaker 1:** we do here.
[00:41:08:219 - 00:41:11:659] **Speaker 1:** So with that I want to also just talk briefly
[00:41:11:659 - 00:41:14:340] **Speaker 1:** when the next page is jumping into a couple of
[00:41:14:340 - 00:41:14:699] **Speaker 1:** examples.
[00:41:14:899 - 00:41:17:219] **Speaker 1:** So we will, I'll talk very briefly about that but
[00:41:17:219 - 00:41:19:419] **Speaker 1:** we won't necessarily go through the example today cause we
[00:41:19:419 - 00:41:20:639] **Speaker 1:** won't get very far through it.
[00:41:24:229 - 00:41:27:020] **Speaker 1:** So this is, we're gonna actually start looking at a
[00:41:27:489 - 00:41:30:629] **Speaker 1:** a structure like this and we're gonna go through and
[00:41:30:629 - 00:41:32:429] **Speaker 1:** we're, we're gonna look at how we would solve this
[00:41:32:429 - 00:41:32:850] **Speaker 1:** by hand.
[00:41:33:959 - 00:41:36:800] **Speaker 1:** So over the next day, it may roll into next
[00:41:36:800 - 00:41:37:179] **Speaker 1:** week.
[00:41:38:060 - 00:41:40:350] **Speaker 1:** What we're gonna do is, you know, I really want
[00:41:40:350 - 00:41:42:449] **Speaker 1:** you to understand the linkages to what you've learned before,
[00:41:42:510 - 00:41:46:750] **Speaker 1:** that this is a building block which extends and um
[00:41:46:750 - 00:41:49:570] **Speaker 1:** generalises what you've learned and doesn't replace it.
[00:41:50:149 - 00:41:51:189] **Speaker 1:** So we'll go through a problem like this.
[00:41:51:310 - 00:41:54:090] **Speaker 1:** You'll actually see this will, um, we'll go through this,
[00:41:54:629 - 00:41:56:750] **Speaker 1:** um, a few different ways by hand in terms of
[00:41:56:750 - 00:41:58:550] **Speaker 1:** how you would interpret this and how you'd solve this
[00:41:58:550 - 00:42:01:610] **Speaker 1:** by hand using, um, different methods.
[00:42:02:149 - 00:42:04:550] **Speaker 1:** And then we'll the the lab next week will actually
[00:42:04:550 - 00:42:05:530] **Speaker 1:** be on the same structure.
[00:42:06:159 - 00:42:08:159] **Speaker 1:** They'll be using the final element method to solve it
[00:42:08:280 - 00:42:09:729] **Speaker 1:** and you'll be writing code to do that.
[00:42:10:399 - 00:42:12:639] **Speaker 1:** So this, you're gonna see this this problem in a
[00:42:12:639 - 00:42:13:699] **Speaker 1:** few different iterations.
[00:42:14:830 - 00:42:16:989] **Speaker 1:** And it's gonna be the key linkage to say this
[00:42:16:989 - 00:42:18:159] **Speaker 1:** is what you would have done by hand and this
[00:42:18:159 - 00:42:18:850] **Speaker 1:** is what the final code will do for you.
[00:42:20:159 - 00:42:22:639] **Speaker 1:** And hopefully what you'll see through that process is that
[00:42:22:639 - 00:42:24:149] **Speaker 1:** it does a lot of the hard work for you.
[00:42:24:399 - 00:42:28:120] **Speaker 1:** You create this mathematical framework, but once you've done that,
[00:42:28:159 - 00:42:30:000] **Speaker 1:** it's very, very powerful and it does all the hard
[00:42:30:000 - 00:42:30:560] **Speaker 1:** work for you.
[00:42:33:320 - 00:42:34:870] **Speaker 1:** And what I want to do now is just very
[00:42:34:870 - 00:42:36:250] **Speaker 1:** quickly, um.
[00:42:37:229 - 00:42:41:469] **Speaker 1:** Just jump across to the lab sheet for this afternoon.
[00:42:42:909 - 00:42:44:709] **Speaker 1:** So this is a Python refresher course.
[00:42:44:889 - 00:42:47:850] **Speaker 1:** So some of the initial stuff is, is very basic,
[00:42:47:989 - 00:42:52:340] **Speaker 1:** um, just, you know, array entry, looking at um when
[00:42:52:340 - 00:42:56:409] **Speaker 1:** you say just use B equals A, that it's actually
[00:42:56:750 - 00:43:00:719] **Speaker 1:** not necessarily creating a copy of the the variable is
[00:43:00:719 - 00:43:01:860] **Speaker 1:** actually just creating a pointer to it.
[00:43:01:909 - 00:43:03:610] **Speaker 1:** So that if you change one you change both.
[00:43:04:189 - 00:43:06:149] **Speaker 1:** You can do a copy, um.
[00:43:07:149 - 00:43:09:590] **Speaker 1:** Some things about matrix entry, particularly.
[00:43:10:489 - 00:43:16:060] **Speaker 1:** Um, building up larger matrices from smaller submatrices, um, a
[00:43:16:070 - 00:43:18:649] **Speaker 1:** little bit of a recap on the matrix multiplication.
[00:43:19:010 - 00:43:22:550] **Speaker 1:** So, um, the matrix multiplication, pretty much, I think certainly
[00:43:22:550 - 00:43:24:689] **Speaker 1:** in this part of the course, everything we do is
[00:43:24:689 - 00:43:26:250] **Speaker 1:** the full matrix multiplication.
[00:43:26:530 - 00:43:28:340] **Speaker 1:** So, um, that would be NP.
[00:43:28:530 - 00:43:32:489] **Speaker 1:** matt mole in Python or the at symbol is the
[00:43:32:489 - 00:43:33:169] **Speaker 1:** shorthand.
[00:43:33:570 - 00:43:35:370] **Speaker 1:** But the key thing is that we don't, if you
[00:43:35:370 - 00:43:37:290] **Speaker 1:** just use the star symbol in Python, it's the element
[00:43:37:290 - 00:43:38:689] **Speaker 1:** by element multiplication.
[00:43:39:129 - 00:43:41:139] **Speaker 1:** And nothing we do in this part of the course
[00:43:41:139 - 00:43:42:879] **Speaker 1:** ever uses that element by element.
[00:43:43:459 - 00:43:48:800] **Speaker 1:** We're using exclusively um full matrix multiplication when we're doing
[00:43:48:800 - 00:43:49:899] **Speaker 1:** things, um.
[00:43:50:800 - 00:43:56:590] **Speaker 1:** Little just example here with um Systems of linear equations.
[00:43:57:520 - 00:43:59:520] **Speaker 1:** So just looking at how to solve those, find the
[00:43:59:520 - 00:44:05:159] **Speaker 1:** intersection points, um, plot the solution, find iterative iteratively find
[00:44:05:159 - 00:44:07:739] **Speaker 1:** the, the value at which the lines cross.
[00:44:08:879 - 00:44:11:979] **Speaker 1:** And following that Um, a little bit of information about
[00:44:11:979 - 00:44:14:510] **Speaker 1:** data entry, so you do quite often see people, you
[00:44:14:510 - 00:44:18:909] **Speaker 1:** know, 200 times 10, 9 to enter, say 200 gigapasscal
[00:44:19:649 - 00:44:22:350] **Speaker 1:** or typing in a 2 followed by 11 zeros.
[00:44:22:689 - 00:44:25:649] **Speaker 1:** Um, you can just very simply write 29 in Python,
[00:44:25:760 - 00:44:27:330] **Speaker 1:** so that's quite a, a valuable thing.
[00:44:28:189 - 00:44:30:320] **Speaker 1:** And then there's also some stuff here on just formatting
[00:44:30:320 - 00:44:30:929] **Speaker 1:** output.
[00:44:31:229 - 00:44:34:510] **Speaker 1:** Now, um, the lab sheet's obviously got some some discussion
[00:44:34:510 - 00:44:34:949] **Speaker 1:** on this.
[00:44:35:110 - 00:44:37:350] **Speaker 1:** Um, some of you will say why don't you just
[00:44:37:350 - 00:44:39:169] **Speaker 1:** use Spider and use the variable explorer.
[00:44:40:129 - 00:44:42:669] **Speaker 1:** Absolutely, it's it's very powerful and very useful.
[00:44:43:510 - 00:44:47:080] **Speaker 1:** Um, for those of you that do choose to use
[00:44:47:080 - 00:44:49:860] **Speaker 1:** an ID and then print to the command window, um,
[00:44:50:000 - 00:44:52:320] **Speaker 1:** we often see this as, you know, you've got multiple
[00:44:52:320 - 00:44:55:320] **Speaker 1:** variables and kind of get this just tsunami of interconnected
[00:44:55:320 - 00:44:57:300] **Speaker 1:** numbers and it's very hard to sort of see where
[00:44:57:300 - 00:44:59:969] **Speaker 1:** one thing stops and 11 thing ends.
[00:45:00:560 - 00:45:03:439] **Speaker 1:** And I've just put some, you know, fairly basic versions
[00:45:03:439 - 00:45:03:879] **Speaker 1:** of that.
[00:45:04:659 - 00:45:06:469] **Speaker 1:** Uh, print functions where you can just sort of break
[00:45:06:469 - 00:45:07:090] **Speaker 1:** things up.
[00:45:08:389 - 00:45:12:709] **Speaker 1:** And have nice clear variable identifications, um, things are just
[00:45:12:709 - 00:45:14:689] **Speaker 1:** a lot more easy to interpret.
[00:45:15:110 - 00:45:17:100] **Speaker 1:** Um, and in the labs here, if you're doing it
[00:45:17:100 - 00:45:19:830] **Speaker 1:** this way and your, your output is printed a bit
[00:45:19:830 - 00:45:21:429] **Speaker 1:** more clearly, it makes it a lot easier for us
[00:45:21:429 - 00:45:22:689] **Speaker 1:** to help you debug things.
[00:45:22:989 - 00:45:24:469] **Speaker 1:** I think it also helps a lot for you to
[00:45:24:469 - 00:45:26:280] **Speaker 1:** understand and interpret things as well.
[00:45:26:790 - 00:45:29:449] **Speaker 1:** Um, and then as we move towards sort of larger
[00:45:29:449 - 00:45:35:149] **Speaker 1:** matrices, particularly those with large exponents, um, The default way
[00:45:35:149 - 00:45:38:530] **Speaker 1:** that, um, Python will display that is like this.
[00:45:39:300 - 00:45:41:580] **Speaker 1:** Uh, but with a couple of, you know, basically dividing
[00:45:41:580 - 00:45:45:100] **Speaker 1:** out a common factor, um, and particularly putting the new
[00:45:45:100 - 00:45:49:100] **Speaker 1:** line command in prior to the matrix being displayed, it
[00:45:49:100 - 00:45:51:340] **Speaker 1:** means that it displays like this and all the columns
[00:45:51:340 - 00:45:52:300] **Speaker 1:** are nicely aligned.
[00:45:52:479 - 00:45:55:179] **Speaker 1:** So, um, just something I think will be really useful
[00:45:55:179 - 00:45:56:239] **Speaker 1:** for the, the labs ahead.
[00:45:56:620 - 00:45:59:219] **Speaker 1:** So, um, as I said, if you're really comfortable with
[00:45:59:219 - 00:46:02:209] **Speaker 1:** Python and you don't feel you necessarily need this, um,
[00:46:02:300 - 00:46:03:780] **Speaker 1:** then don't feel you have to come along to the
[00:46:03:780 - 00:46:06:060] **Speaker 1:** labs this afternoon, but, For those of you, I mean,
[00:46:06:379 - 00:46:08:340] **Speaker 1:** this is all very much set up around things that
[00:46:08:340 - 00:46:10:820] **Speaker 1:** we will be using in the next few weeks, it's
[00:46:10:820 - 00:46:13:219] **Speaker 1:** not just work for work's sake, so.
[00:46:13:969 - 00:46:16:050] **Speaker 1:** Um, I think there'll be value in that.
[00:46:17:830 - 00:46:20:719] **Speaker 1:** Is there any question on the delays this afternoon or
[00:46:20:719 - 00:46:21:580] **Speaker 1:** anything we've covered today?
[00:46:24:929 - 00:46:27:429] **Speaker 1:** If not, thank you all for coming along and I'll
[00:46:27:429 - 00:46:28:760] **Speaker 1:** see you again this afternoon.
[00:47:02:629 - 00:47:02:639] **Speaker 0:** OK.
[00:47:08:149 - 00:47:08:169] **Speaker 0:** Thank you.
[00:47:18:110 - 00:47:20:879] **Speaker 0:** Is it the hole after or is it the?
[00:47:24:280 - 00:47:27:639] **Speaker 0:** Um, so I'll just pull this up.
[00:47:27:719 - 00:47:29:290] **Speaker 1:** There are actually 3 sessions this afternoon, so um.
[00:47:38:219 - 00:47:48:540] **Speaker 0:** Yeah, I'd rather than um, the, so there's actually three
[00:47:48:540 - 00:47:51:010] **Speaker 1:** back to back sessions, so one's 1:30 to 2:30, 1
[00:47:51:010 - 00:47:51:679] **Speaker 1:** to 2:30.
[00:47:52:310 - 00:48:00:449] **Speaker 0:** 2:30 to 4 and 4 so so if you um
[00:48:01:290 - 00:48:03:469] **Speaker 0:** if you email we can always change it or change
[00:48:03:469 - 00:48:10:050] **Speaker 1:** your allocation so show us correctly the time zone um
[00:48:10:050 - 00:48:10:110] **Speaker 0:** or you can just give us.
[00:48:12:290 - 00:48:13:860] **Speaker 0:** Is.
[00:48:18:120 - 00:48:18:129] **Speaker 0:** Well.
[00:48:28:870 - 00:48:34:949] **Speaker 0:** really nice learn much from it.
[00:48:36:139 - 00:48:38:610] **Speaker 0:** Oh yeah, that's why I, I feel like I'm not,
[00:48:38:699 - 00:48:39:179] **Speaker 0:** I don't want.
[00:48:40:229 - 00:48:40:649] **Speaker 0:** I get up.
[00:48:55:889 - 00:49:00:350] **Speaker 0:** So Oh, you are MG9.
[00:49:23:389 - 00:49:25:199] **Speaker 0:** OK Hello boss.
[00:49:32:459 - 00:49:33:199] **Speaker 1:** That's the course.
[00:49:34:850 - 00:49:40:469] **Speaker 1:** In your future, your future geniuses, they're all here.
[00:49:42:810 - 00:49:43:489] **Speaker 0:** will be.
[00:49:43:760 - 00:49:44:570] **Speaker 0:** I'm relying on.
[00:49:45:899 - 00:49:49:979] **Speaker 1:** Everything that you do for us to I try not
[00:49:49:979 - 00:49:50:840] **Speaker 1:** to do any damage.
[00:49:53:449 - 00:49:53:699] **Speaker 1:** I don't think a lot of good, you do a
[00:49:53:699 - 00:49:53:939] **Speaker 1:** lot of good.
[00:49:55:439 - 00:50:50:439] **Speaker 0:** See uh So.
[00:50:56:060 - 00:53:53:080] **Speaker 0:** I I Yeah same You can come on in.
[00:53:54:000 - 00:53:56:239] **Speaker 0:** E math 118, I hope.
[00:53:57:899 - 00:53:58:439] **Speaker 0:** Correct.
[00:54:15:110 - 00:54:15:120] **Speaker 0:** Um

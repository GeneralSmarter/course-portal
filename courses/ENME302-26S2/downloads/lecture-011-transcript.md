# ENME302-26S2 Lecture 11 native Echo transcript

Date: July 30, 2026 10:00am-10:55am
Transcript type: native Echo automated transcript.

[00:00:00:620 - 00:00:00:629] **Speaker 0:** You.
[00:00:02:420 - 00:00:02:430] **Speaker 0:** Yeah.
[00:00:07:460 - 00:00:17:440] **Speaker 0:** I I.
[00:00:29:959 - 00:00:32:229] **Speaker 0:** Well, Karakoto, welcome along, everyone.
[00:00:36:319 - 00:00:39:250] **Speaker 1:** So yesterday we finished the derivation of frames.
[00:00:40:810 - 00:00:44:349] **Speaker 1:** And This is the most general element type that we're
[00:00:44:349 - 00:00:44:930] **Speaker 1:** gonna do.
[00:00:45:430 - 00:00:47:029] **Speaker 1:** We will come back and also look at how to
[00:00:47:029 - 00:00:50:310] **Speaker 1:** introduce distributed loading, but, um, for now we're just gonna
[00:00:50:310 - 00:00:52:950] **Speaker 1:** look at, uh, some examples using frame elements.
[00:00:53:229 - 00:00:56:470] **Speaker 1:** So frame elements is the most general two-dimensional element that
[00:00:56:470 - 00:00:57:209] **Speaker 1:** we'll deal with.
[00:00:58:020 - 00:01:01:939] **Speaker 1:** It includes axial deformations, uh, carrying transverse shear forces, and
[00:01:01:939 - 00:01:05:300] **Speaker 1:** bending moments, so it can have curvature deflections, uh, axial
[00:01:05:300 - 00:01:08:870] **Speaker 1:** deflections, and all the reaction mechanisms of everything we've covered
[00:01:08:870 - 00:01:09:610] **Speaker 1:** to this point.
[00:01:10:580 - 00:01:12:620] **Speaker 1:** So we're gonna work through a problem now, um, this
[00:01:12:620 - 00:01:14:629] **Speaker 1:** problem we're gonna work through conceptually and then there's the,
[00:01:14:690 - 00:01:17:739] **Speaker 1:** the step by step code, um, which is the key
[00:01:17:739 - 00:01:19:000] **Speaker 1:** focus of the lab this afternoon.
[00:01:20:900 - 00:01:23:580] **Speaker 1:** And we're also gonna look at some plotting code there
[00:01:23:580 - 00:01:26:489] **Speaker 1:** as well, um, so first of all, we're gonna look
[00:01:26:489 - 00:01:28:809] **Speaker 1:** at here is a simple construction that consists of three
[00:01:28:809 - 00:01:29:500] **Speaker 1:** frame elements.
[00:01:29:699 - 00:01:32:220] **Speaker 1:** Now the very first thing you have to do when
[00:01:32:220 - 00:01:34:339] **Speaker 1:** setting up a problem is to choose the global degrees
[00:01:34:339 - 00:01:35:319] **Speaker 1:** of freedom to assign.
[00:01:36:150 - 00:01:38:910] **Speaker 1:** Now this is uh the same conceptual process as we've
[00:01:38:910 - 00:01:41:639] **Speaker 1:** done before, but because we have a different element type,
[00:01:42:150 - 00:01:44:150] **Speaker 1:** there's a little bit a few differences to the process
[00:01:44:150 - 00:01:45:069] **Speaker 1:** which I want to go through now.
[00:01:46:470 - 00:01:48:269] **Speaker 1:** So the question says the top support is a fixed
[00:01:48:269 - 00:01:50:389] **Speaker 1:** or clamp support and the bottom left is a knife
[00:01:50:389 - 00:01:51:169] **Speaker 1:** edge support.
[00:01:52:000 - 00:01:55:489] **Speaker 1:** Which is this one down here, um, so it's sitting
[00:01:55:489 - 00:01:58:410] **Speaker 1:** on a roller, uh, which is given in the question
[00:01:58:410 - 00:01:58:800] **Speaker 1:** here.
[00:01:59:059 - 00:02:01:169] **Speaker 1:** So it's able to provide a vertical reaction force but
[00:02:01:169 - 00:02:04:169] **Speaker 1:** not any horizontal, uh, force or moment.
[00:02:04:569 - 00:02:06:730] **Speaker 1:** So when we see a roller like this, this is
[00:02:06:730 - 00:02:10:369] **Speaker 1:** automatically assuming basically it's completely constraining vertical deflection.
[00:02:10:490 - 00:02:12:649] **Speaker 1:** So, um, we're assuming that it is actually able to
[00:02:12:649 - 00:02:13:830] **Speaker 1:** prevent uplift as well.
[00:02:15:050 - 00:02:18:210] **Speaker 1:** And that it's, it's constraining this node to not move
[00:02:18:210 - 00:02:18:809] **Speaker 1:** vertically.
[00:02:20:089 - 00:02:21:210] **Speaker 1:** Upwards or downwards.
[00:02:22:740 - 00:02:24:820] **Speaker 1:** We've been told the support at the bottom right-hand corner
[00:02:24:820 - 00:02:28:300] **Speaker 1:** here is a pin, and it prevents translation but not
[00:02:28:300 - 00:02:28:940] **Speaker 1:** rotation.
[00:02:29:669 - 00:02:31:580] **Speaker 1:** And there's only one externally applied load which is the
[00:02:31:580 - 00:02:35:600] **Speaker 1:** 140 kilonewton metre concentrated moment applied here at the bottom
[00:02:35:600 - 00:02:36:419] **Speaker 1:** left hand corner.
[00:02:37:649 - 00:02:40:740] **Speaker 1:** What we're gonna do is find the structural deflections, the
[00:02:40:740 - 00:02:44:220] **Speaker 1:** reaction forces, and the three supports and the element internal
[00:02:44:220 - 00:02:44:880] **Speaker 1:** forces.
[00:02:45:460 - 00:02:47:419] **Speaker 1:** We've been told each element is 10 metres, we have
[00:02:47:419 - 00:02:50:059] **Speaker 1:** some I values, some A values, and we're assuming it's
[00:02:50:059 - 00:02:52:369] **Speaker 1:** made of steel and we've got 200 gigapasscal as the
[00:02:52:369 - 00:02:53:440] **Speaker 1:** elastic modulus.
[00:02:55:509 - 00:02:57:750] **Speaker 1:** Now, this is where things vary just a little bit
[00:02:57:750 - 00:02:58:830] **Speaker 1:** from what we've done previously.
[00:03:01:919 - 00:03:06:149] **Speaker 1:** So for Frame elements.
[00:03:12:050 - 00:03:24:149] **Speaker 1:** Each nodal point Begins With 3 possible.
[00:03:25:419 - 00:03:26:339] **Speaker 1:** Degrees of freedom.
[00:03:29:630 - 00:03:32:910] **Speaker 1:** So These of course are the lowercase q values.
[00:03:34:630 - 00:03:50:759] **Speaker 1:** And those Que values will be XG YG NZG We
[00:03:50:759 - 00:03:52:550] **Speaker 1:** then consider the supports.
[00:04:03:559 - 00:04:14:699] **Speaker 1:** To constrain And remove Degrees of freedom As appropriate.
[00:04:20:170 - 00:04:22:260] **Speaker 1:** So because we are restricting ourselves to just a 2D
[00:04:22:260 - 00:04:24:769] **Speaker 1:** plane here, there's basically three possibilities.
[00:04:24:859 - 00:04:27:420] **Speaker 1:** An X translation in the global direction, a Y global
[00:04:27:420 - 00:04:29:980] **Speaker 1:** translation, and a rotation about Z.
[00:04:30:290 - 00:04:33:019] **Speaker 1:** and that's the, the, the possible things that we start
[00:04:33:019 - 00:04:33:559] **Speaker 1:** out with.
[00:04:37:540 - 00:04:39:100] **Speaker 1:** Now we'll start at the top the top left hand
[00:04:39:100 - 00:04:39:480] **Speaker 1:** corner.
[00:04:40:790 - 00:04:42:720] **Speaker 1:** So this is a fixed or clamped support.
[00:04:52:220 - 00:04:53:700] **Speaker 1:** That fully constrains.
[00:04:58:190 - 00:05:01:100] **Speaker 1:** All possible Degree of freedom.
[00:05:05:549 - 00:05:06:350] **Speaker 0:** At this note.
[00:05:11:450 - 00:05:26:920] **Speaker 1:** So that means So there are no Permissible Deflections And
[00:05:26:920 - 00:05:27:950] **Speaker 1:** no Q values.
[00:05:31:760 - 00:05:34:799] **Speaker 1:** And by not assigning any Q values there, that is
[00:05:34:799 - 00:05:37:989] **Speaker 1:** how we tell the system that this node is fully
[00:05:37:989 - 00:05:38:559] **Speaker 1:** constrained.
[00:05:42:760 - 00:05:44:109] **Speaker 1:** Now if we look at the bottom left hand corner,
[00:05:44:160 - 00:05:47:309] **Speaker 1:** this is the roller, so, um, as I said, the,
[00:05:47:429 - 00:05:50:239] **Speaker 1:** the purpose of a roller, the the mathematical assumption we
[00:05:50:239 - 00:05:52:600] **Speaker 1:** make is that it's completely able to constrain motion upwards
[00:05:52:600 - 00:05:53:119] **Speaker 1:** and downwards.
[00:05:53:160 - 00:05:57:200] **Speaker 1:** So um it does also implicitly assume that the roller
[00:05:57:600 - 00:06:00:920] **Speaker 1:** is able to provide um a tensile force to hold
[00:06:00:920 - 00:06:01:440] **Speaker 1:** this down.
[00:06:03:429 - 00:06:06:290] **Speaker 1:** Doesn't necessarily mean it will be intention, but it does
[00:06:06:290 - 00:06:08:589] **Speaker 1:** assume completely constraining in the right direction.
[00:06:11:779 - 00:06:18:959] **Speaker 1:** So the vertical Reflection Which is a YG.
[00:06:21:029 - 00:06:33:859] **Speaker 1:** Direction Is fully constrained So there's no Q value.
[00:06:36:480 - 00:06:37:049] **Speaker 1:** Vertically.
[00:06:42:149 - 00:06:57:220] **Speaker 1:** However, Possible XG Translation And a ZG.
[00:06:58:380 - 00:07:10:730] **Speaker 1:** Rotation So There are 2 Q values here.
[00:07:16:260 - 00:07:18:619] **Speaker 1:** So we're we're gonna be a queue horizontally and a
[00:07:18:619 - 00:07:19:100] **Speaker 1:** queue.
[00:07:20:149 - 00:07:23:269] **Speaker 1:** Uh, in the Z direction, the rotation, counterclockwise rotation there.
[00:07:29:029 - 00:07:30:609] **Speaker 1:** This, this isn't loaded properly.
[00:07:31:510 - 00:07:32:049] **Speaker 1:** Sorry about that.
[00:07:33:910 - 00:07:34:959] **Speaker 1:** Sure it's on both screens.
[00:07:37:119 - 00:07:39:500] **Speaker 1:** OK, um, what we have here.
[00:07:41:290 - 00:07:42:790] **Speaker 1:** Is a knife-edge support.
[00:07:48:130 - 00:07:52:200] **Speaker 1:** Open The constraints.
[00:07:54:140 - 00:07:54:950] **Speaker 1:** XG.
[00:07:56:679 - 00:08:04:739] **Speaker 1:** And YG But permits ECG.
[00:08:05:980 - 00:08:13:170] **Speaker 1:** Rotation Hence One Q value.
[00:08:20:850 - 00:08:22:260] **Speaker 1:** Now I just want to take the time to work
[00:08:22:260 - 00:08:25:540] **Speaker 1:** through that because that is probably the most important decision
[00:08:25:540 - 00:08:27:339] **Speaker 1:** you're gonna make when you set up a problem, because
[00:08:27:339 - 00:08:29:059] **Speaker 1:** if you get the degrees of freedom wrong at this
[00:08:29:059 - 00:08:31:660] **Speaker 1:** point, no subsequent analysis is going to fix that.
[00:08:33:030 - 00:08:35:570] **Speaker 1:** Now, we have talked a bit about singular matrices.
[00:08:36:469 - 00:08:39:659] **Speaker 1:** So suppose in a test, you go in and you,
[00:08:39:710 - 00:08:41:429] **Speaker 1:** you try and solve this and you end up with
[00:08:41:429 - 00:08:44:229] **Speaker 1:** a a warning that says, you know, matrix singular to
[00:08:44:229 - 00:08:46:369] **Speaker 1:** work in precision or something of that nature.
[00:08:47:489 - 00:08:50:010] **Speaker 1:** That's generally a case that well what that means is
[00:08:50:010 - 00:08:53:450] **Speaker 1:** that the the mathematical system is unconstrained, it can't give
[00:08:53:450 - 00:08:54:330] **Speaker 1:** a unique solution.
[00:08:55:219 - 00:08:58:299] **Speaker 1:** So one possible solution, one possible reason that that comes
[00:08:58:299 - 00:09:00:840] **Speaker 1:** up is that you've assigned too many Q-values in here.
[00:09:02:109 - 00:09:04:650] **Speaker 1:** If you assign say 3 Q values at each node,
[00:09:05:340 - 00:09:07:590] **Speaker 1:** what you're telling the system is that it's completely unconstrained,
[00:09:07:630 - 00:09:09:909] **Speaker 1:** it's just floating in space, it's not anchored to any
[00:09:09:909 - 00:09:12:070] **Speaker 1:** support, and therefore you won't be able to get a
[00:09:12:070 - 00:09:13:450] **Speaker 1:** unique mathematical solution.
[00:09:14:919 - 00:09:17:520] **Speaker 1:** The other thing of course is that maybe um if
[00:09:17:520 - 00:09:20:039] **Speaker 1:** you do get that warning, and you've added up, you've
[00:09:20:039 - 00:09:22:309] **Speaker 1:** got 3 elements in the structure you've only added KG1
[00:09:22:309 - 00:09:25:270] **Speaker 1:** and KG2, you've missed the KG 3 component or some
[00:09:25:460 - 00:09:27:520] **Speaker 1:** you've copied and pasted something where you're using the wrong
[00:09:27:520 - 00:09:27:880] **Speaker 1:** value.
[00:09:28:080 - 00:09:30:330] **Speaker 1:** So um if you get that warning to saying the
[00:09:30:330 - 00:09:33:559] **Speaker 1:** matrix is singular and can't get a solution, that's the
[00:09:33:559 - 00:09:36:280] **Speaker 1:** situits basically an indication that one of the degrees of
[00:09:36:280 - 00:09:39:750] **Speaker 1:** freedom has no stiffness and, um, that's the thing to
[00:09:39:750 - 00:09:41:390] **Speaker 1:** look at, you know, have I in the right Q
[00:09:41:390 - 00:09:42:419] **Speaker 1:** values to start the problem.
[00:09:42:950 - 00:09:45:979] **Speaker 1:** Have I got my assembly matrices correct, um, and have
[00:09:45:979 - 00:09:49:869] **Speaker 1:** I, um, got my coding correct and that all the
[00:09:49:869 - 00:09:53:710] **Speaker 1:** stiffness contributions from each element are correctly considered in the
[00:09:53:710 - 00:09:54:469] **Speaker 1:** final kg.
[00:09:59:650 - 00:10:03:450] **Speaker 1:** So having worked through that, you have a horizontal queue
[00:10:03:450 - 00:10:05:090] **Speaker 1:** here, a rotation, and a rotation here.
[00:10:05:169 - 00:10:07:250] **Speaker 1:** So there's there'll be 3 degrees of freedom for the
[00:10:07:250 - 00:10:08:469] **Speaker 1:** structure as a whole.
[00:10:09:099 - 00:10:11:169] **Speaker 1:** But just knowing that this is the the type of
[00:10:11:169 - 00:10:13:530] **Speaker 1:** form that you would get in a test problem where
[00:10:13:530 - 00:10:15:969] **Speaker 1:** the queues aren't labelled and you have to make that
[00:10:15:969 - 00:10:16:070] **Speaker 1:** decision.
[00:10:21:289 - 00:10:24:570] **Speaker 1:** Having applied that decision, we've got our Q1, our Q2,
[00:10:24:580 - 00:10:25:580] **Speaker 1:** and our Q3 here.
[00:10:26:890 - 00:10:29:010] **Speaker 1:** Now, I have mentioned this before, but if you were
[00:10:29:010 - 00:10:31:010] **Speaker 1:** to say, well, why couldn't I have called this Q1
[00:10:31:250 - 00:10:33:849] **Speaker 1:** and Q2 and this Q3, the answer is you could
[00:10:33:849 - 00:10:34:090] **Speaker 1:** have.
[00:10:34:330 - 00:10:36:210] **Speaker 1:** There's nothing wrong with that assumption.
[00:10:36:729 - 00:10:40:309] **Speaker 1:** Within an element here, we have to go, remember our
[00:10:40:770 - 00:10:43:650] **Speaker 1:** uppercase Ds are element degrees of freedom and global coordinates,
[00:10:43:690 - 00:10:46:010] **Speaker 1:** always go global X, global Y, global Z at node
[00:10:46:010 - 00:10:49:729] **Speaker 1:** 1, global X, global Z, global, global X, global Y,
[00:10:49:809 - 00:10:50:729] **Speaker 1:** global Z at node 2.
[00:10:50:969 - 00:10:55:330] **Speaker 1:** So D1 D3, D4, D6, and we have no flexibility.
[00:10:56:450 - 00:10:58:080] **Speaker 1:** On the numbering sequence within an element.
[00:10:59:080 - 00:11:01:010] **Speaker 1:** But at the structural level, we could have called this
[00:11:01:010 - 00:11:02:750] **Speaker 1:** Q1, Q2, Q3.
[00:11:03:130 - 00:11:05:090] **Speaker 1:** Um, generally speaking, it is better to sort of work
[00:11:05:090 - 00:11:07:770] **Speaker 1:** left to right, um, have followed the kind of X
[00:11:07:770 - 00:11:10:559] **Speaker 1:** Y Z pattern because then your assembly matrices would just
[00:11:10:559 - 00:11:12:890] **Speaker 1:** be a nicer form, but there's nothing wrong.
[00:11:12:950 - 00:11:14:929] **Speaker 1:** If you were to number this in a different sequence,
[00:11:14:969 - 00:11:15:710] **Speaker 1:** that's fine.
[00:11:16:250 - 00:11:18:210] **Speaker 1:** So when it comes to marking the test, it doesn't
[00:11:18:210 - 00:11:20:039] **Speaker 1:** mean we have multiple sets of model solutions and it's
[00:11:20:039 - 00:11:22:650] **Speaker 1:** a bit of a hassle to mark, but that's indicative
[00:11:22:650 - 00:11:23:489] **Speaker 1:** of, you know.
[00:11:24:520 - 00:11:26:770] **Speaker 1:** The answer's not wrong, we need to recognise that it's
[00:11:26:770 - 00:11:28:169] **Speaker 1:** equally right as any other answer.
[00:11:30:739 - 00:11:33:659] **Speaker 1:** So if we compare um this three-body diagram, so we've
[00:11:33:659 - 00:11:37:679] **Speaker 1:** chosen this orientation here with X downwards, which means alpha
[00:11:37:679 - 00:11:40:979] **Speaker 1:** is either 270 degrees or -90 because we start aligned
[00:11:40:979 - 00:11:43:260] **Speaker 1:** with X global and we rotate counterclockwise.
[00:11:43:820 - 00:11:45:140] **Speaker 1:** So if this was the thing here, we start with
[00:11:45:140 - 00:11:50:299] **Speaker 1:** X global, we'd go 90, 180, 270, and now these
[00:11:50:299 - 00:11:50:979] **Speaker 1:** two are aligned.
[00:11:53:109 - 00:11:54:750] **Speaker 1:** And what we need to do here is work out
[00:11:54:880 - 00:11:57:390] **Speaker 1:** the relationship between degrees of freedom within the element to
[00:11:57:390 - 00:11:58:890] **Speaker 1:** the degrees of freedom for the overall structure.
[00:12:00:650 - 00:12:03:080] **Speaker 1:** So first thing here, this is gonna be note one.
[00:12:03:830 - 00:12:05:330] **Speaker 1:** And this is going to be note 2.
[00:12:06:909 - 00:12:09:270] **Speaker 1:** D1, D2 and D3 don't map to anything on the
[00:12:09:270 - 00:12:09:669] **Speaker 1:** structure.
[00:12:11:669 - 00:12:18:059] **Speaker 1:** D4 For element one Is the horizontal deflection at this
[00:12:18:059 - 00:12:20:020] **Speaker 1:** nodal point, which is Q1.
[00:12:21:119 - 00:12:24:330] **Speaker 1:** D5 for element one corresponds to a vertical deflection, but
[00:12:24:330 - 00:12:28:270] **Speaker 1:** there is no Q there, but the D6 for element
[00:12:28:270 - 00:12:30:710] **Speaker 1:** one corresponds to Q2.
[00:12:33:289 - 00:12:34:909] **Speaker 1:** Then when we look at element 2.
[00:12:36:270 - 00:12:38:270] **Speaker 1:** Well, the first thing we see is that D1 for
[00:12:38:270 - 00:12:41:429] **Speaker 1:** element 2 corresponds to Q1, that's the horizontal deflection of
[00:12:41:429 - 00:12:41:909] **Speaker 1:** this node.
[00:12:42:710 - 00:12:45:390] **Speaker 1:** And then the 3rd degree of freedom, the rotation for
[00:12:45:390 - 00:12:47:690] **Speaker 1:** element 2 corresponds to Q2.
[00:12:54:150 - 00:12:56:239] **Speaker 1:** Then what we can say there is that the.
[00:12:58:309 - 00:13:02:349] **Speaker 1:** 6 for element 2 is equal to Q3, because that's
[00:13:02:349 - 00:13:04:630] **Speaker 1:** the rotation that we see here.
[00:13:09:270 - 00:13:11:460] **Speaker 1:** So that's the key pieces of information we need to
[00:13:11:460 - 00:13:12:780] **Speaker 1:** set up our assembly matrices.
[00:13:14:849 - 00:13:16:229] **Speaker 1:** Now one thing that I also want to just draw
[00:13:16:229 - 00:13:21:400] **Speaker 1:** your attention to here is we're linking D1 for element
[00:13:21:400 - 00:13:22:650] **Speaker 1:** 1 to Q1.
[00:13:22:840 - 00:13:25:250] **Speaker 1:** We're also linking D1 to element two for Q1.
[00:13:25:729 - 00:13:27:090] **Speaker 1:** So what we're doing is we're saying that this degree
[00:13:27:090 - 00:13:28:929] **Speaker 1:** of freedom and this degree of freedom have to move
[00:13:28:929 - 00:13:29:270] **Speaker 1:** together.
[00:13:30:039 - 00:13:34:669] **Speaker 1:** We're forcing those to translate horizontally together and those correspond
[00:13:34:669 - 00:13:35:500] **Speaker 1:** to the same nodal point.
[00:13:36:820 - 00:13:38:820] **Speaker 1:** The other thing that we're doing here is we're saying
[00:13:38:820 - 00:13:43:900] **Speaker 1:** that the D6 for element one and D3 for element
[00:13:43:900 - 00:13:45:979] **Speaker 1:** two are equal to each other.
[00:13:46:179 - 00:13:48:419] **Speaker 1:** And that's what we're saying is that those elements have
[00:13:48:419 - 00:13:50:119] **Speaker 1:** to also rotate together.
[00:13:50:619 - 00:13:50:940] **Speaker 1:** So.
[00:13:52:109 - 00:13:53:760] **Speaker 1:** I just write that down to make that clear.
[00:13:55:369 - 00:13:56:599] **Speaker 1:** So D1.
[00:13:57:700 - 00:14:00:200] **Speaker 1:** So D4 valent 1.
[00:14:01:419 - 00:14:07:559] **Speaker 1:** Equals D1 for element 2 equals Q1, and then D6
[00:14:08:080 - 00:14:11:700] **Speaker 1:** element 1 is equal to D3 for element 2, which
[00:14:11:700 - 00:14:12:760] **Speaker 1:** is equal to Q3.
[00:14:15:369 - 00:14:16:719] **Speaker 0:** If that was an in between the two elements, would
[00:14:16:719 - 00:14:19:369] **Speaker 0:** you assign two different degrees of freedom to each member
[00:14:20:409 - 00:14:20:700] **Speaker 1:** that?
[00:14:20:960 - 00:14:23:239] **Speaker 1:** Yes, yes, that's actually the very last thing we'll do
[00:14:23:239 - 00:14:25:840] **Speaker 1:** at the end of next week, um, and we will
[00:14:25:840 - 00:14:27:400] **Speaker 1:** touch on that and we'll go work through an example.
[00:14:27:520 - 00:14:30:070] **Speaker 1:** So, um, I guess the default assumption we have with
[00:14:30:070 - 00:14:33:479] **Speaker 1:** frame elements is that they are rigidly welded to each
[00:14:33:479 - 00:14:37:200] **Speaker 1:** other and that they, they both translate and rotate together.
[00:14:37:969 - 00:14:40:809] **Speaker 1:** If we wanted to break that mathematical coupling.
[00:14:41:679 - 00:14:44:200] **Speaker 1:** We can actually assign two degrees of freedom and we
[00:14:44:200 - 00:14:46:880] **Speaker 1:** can link them to each, but um I won't go
[00:14:46:880 - 00:14:48:320] **Speaker 1:** through them in more detail, we will come back to
[00:14:48:320 - 00:14:50:559] **Speaker 1:** that next week and solve a problem and show how
[00:14:50:559 - 00:14:51:140] **Speaker 1:** that works.
[00:14:52:400 - 00:14:54:679] **Speaker 1:** But the, the default assumption here is that we're linking
[00:14:54:679 - 00:14:56:260] **Speaker 1:** them to translate and rotate together.
[00:14:58:940 - 00:15:01:770] **Speaker 1:** Um The transformation matrix, this is the same one that
[00:15:01:770 - 00:15:02:830] **Speaker 1:** we derived yesterday.
[00:15:03:489 - 00:15:06:090] **Speaker 1:** Um, we just put in the angles, we get the
[00:15:06:090 - 00:15:07:130] **Speaker 1:** corresponding numbers out.
[00:15:07:210 - 00:15:08:950] **Speaker 1:** So that's all relatively procedural.
[00:15:10:650 - 00:15:11:799] **Speaker 1:** We can work through.
[00:15:14:210 - 00:15:21:679] **Speaker 1:** Um Get our elements stiffness matrix K1 K1 hat.
[00:15:22:039 - 00:15:24:520] **Speaker 1:** So, because these are two elements that are on different
[00:15:24:520 - 00:15:27:479] **Speaker 1:** orientations but they have the same E A I and
[00:15:27:479 - 00:15:30:200] **Speaker 1:** L, they actually have the same the K1 is equal
[00:15:30:200 - 00:15:33:280] **Speaker 1:** to K2, it's the same matrix, but because they're on
[00:15:33:280 - 00:15:38:080] **Speaker 1:** different orientations once we introduce, uh, orientation information through the
[00:15:38:080 - 00:15:41:390] **Speaker 1:** transformation matrix, K1 hat is not the same as K2
[00:15:41:390 - 00:15:41:760] **Speaker 1:** hat.
[00:15:43:169 - 00:15:45:869] **Speaker 1:** Then we introduced our assembly matrices.
[00:15:47:049 - 00:15:49:409] **Speaker 1:** So we generate those just using that information that we've
[00:15:49:409 - 00:15:51:609] **Speaker 1:** just determined here in this relationship.
[00:15:56:239 - 00:15:59:229] **Speaker 1:** So D4 for element 1, Q2, we've got the one
[00:15:59:229 - 00:16:02:320] **Speaker 1:** there, and D6 for element 1 is equal to our
[00:16:02:320 - 00:16:03:539] **Speaker 1:** rotation Q2.
[00:16:04:460 - 00:16:07:309] **Speaker 1:** And then we say D1 for element 1 is Q2,
[00:16:07:739 - 00:16:08:179] **Speaker 1:** Q1.
[00:16:09:219 - 00:16:15:969] **Speaker 1:** 3 Is Q2, and then the rotation at the right-hand
[00:16:15:969 - 00:16:16:369] **Speaker 1:** node.
[00:16:17:109 - 00:16:20:140] **Speaker 1:** So we're just doing that intersection there and essentially bringing
[00:16:20:140 - 00:16:20:460] **Speaker 1:** in.
[00:16:21:419 - 00:16:23:659] **Speaker 1:** This information into the system.
[00:16:29:909 - 00:16:32:549] **Speaker 1:** We just go through, we use our assembly matrices on
[00:16:32:549 - 00:16:35:719] **Speaker 1:** our KE hats, our elements such as matrices and global
[00:16:35:719 - 00:16:38:479] **Speaker 1:** coordinates, and then we sum up this here and of
[00:16:38:479 - 00:16:39:700] **Speaker 1:** course this piece here.
[00:16:40:919 - 00:16:48:440] **Speaker 1:** Is KG1 This piece here There's KG 2.
[00:16:49:469 - 00:16:51:469] **Speaker 1:** And we sum the two together, we get our overall
[00:16:51:469 - 00:16:51:849] **Speaker 1:** KG.
[00:16:53:789 - 00:16:56:059] **Speaker 1:** These are the forcing terms, so they were given in
[00:16:56:059 - 00:16:56:580] **Speaker 1:** the question.
[00:16:59:099 - 00:17:02:309] **Speaker 1:** Now, It is possibly important just to realise that.
[00:17:03:880 - 00:17:06:530] **Speaker 1:** Um, there was no numbering sequence on here, so we
[00:17:06:530 - 00:17:09:270] **Speaker 1:** were just told there was a moment of this, um,
[00:17:09:770 - 00:17:10:390] **Speaker 1:** point here.
[00:17:11:188 - 00:17:12:810] **Speaker 1:** We've chosen to call that Q2.
[00:17:13:839 - 00:17:15:930] **Speaker 1:** So therefore that becomes the 2nd entry.
[00:17:16:819 - 00:17:18:040] **Speaker 1:** Into this vector.
[00:17:19:050 - 00:17:22:010] **Speaker 1:** But if we'd chosen a different sequence, a different numbering
[00:17:22:010 - 00:17:25:510] **Speaker 1:** sequence for the Q values on the overall structure, they'd
[00:17:25:510 - 00:17:26:819] **Speaker 1:** be the same numbers in here, but they may be
[00:17:26:819 - 00:17:27:579] **Speaker 1:** in a different order.
[00:17:29:670 - 00:17:31:989] **Speaker 1:** Now, it's also important to note here, we have sort
[00:17:31:989 - 00:17:33:650] **Speaker 1:** of, this is Newton's.
[00:17:34:810 - 00:17:37:770] **Speaker 1:** This is Newton metres, and this is Newton metres.
[00:17:39:180 - 00:17:41:489] **Speaker 1:** So previously what we had when we were working on
[00:17:41:489 - 00:17:43:719] **Speaker 1:** this was when we had bars, we were only dealing
[00:17:43:719 - 00:17:44:449] **Speaker 1:** with translations.
[00:17:44:569 - 00:17:47:650] **Speaker 1:** The forces would always be in Newtons and the deflections
[00:17:47:650 - 00:17:48:699] **Speaker 1:** would always be in metres.
[00:17:49:819 - 00:17:52:469] **Speaker 1:** In this situation here, what we have is a mixed
[00:17:52:469 - 00:17:52:790] **Speaker 1:** solution.
[00:17:52:900 - 00:17:56:380] **Speaker 1:** So the translations come out with units of metres and
[00:17:56:380 - 00:17:58:180] **Speaker 1:** the rotations are in gradients.
[00:17:59:390 - 00:18:01:469] **Speaker 1:** Now, the best thing you can do is just always
[00:18:01:469 - 00:18:02:949] **Speaker 1:** revert to the base SI unit.
[00:18:03:189 - 00:18:06:609] **Speaker 1:** So put in your, your elastic modules and pascals, your,
[00:18:06:660 - 00:18:09:109] **Speaker 1:** uh, cross-sectional areas in metres squared, your I values in
[00:18:09:109 - 00:18:11:310] **Speaker 1:** metres to the 4, etc.
[00:18:11:670 - 00:18:14:630] **Speaker 1:** um, all your forces and Newtons and Newton metres, and
[00:18:14:630 - 00:18:17:150] **Speaker 1:** then everything works out and you get your, um, metres
[00:18:17:150 - 00:18:20:739] **Speaker 1:** and radians as your, Your answers there.
[00:18:23:280 - 00:18:26:239] **Speaker 1:** Once we've solved that, we can then interrogate that information,
[00:18:26:359 - 00:18:29:239] **Speaker 1:** we can jump in and and use our assembly matrix
[00:18:29:239 - 00:18:32:400] **Speaker 1:** to break down the structure and sign those in the
[00:18:32:400 - 00:18:33:280] **Speaker 1:** appropriate location.
[00:18:37:619 - 00:18:39:270] **Speaker 1:** So this assembly matrix AE.
[00:18:40:780 - 00:18:49:579] **Speaker 1:** That By using that Assembly matrix.
[00:18:51:569 - 00:18:55:589] **Speaker 0:** Extracts Relevant parts.
[00:18:57:660 - 00:19:11:250] **Speaker 1:** Of cue And assigns them To the appropriate location.
[00:19:16:660 - 00:19:23:780] **Speaker 1:** Within The Victor So we don't have to do this
[00:19:23:780 - 00:19:24:060] **Speaker 1:** manually.
[00:19:24:140 - 00:19:27:290] **Speaker 1:** We, we could do it manually, but this is the
[00:19:27:290 - 00:19:31:609] **Speaker 1:** initial information we had at Q1 was the 4th correspondence
[00:19:31:609 - 00:19:34:319] **Speaker 1:** to D4 for element 1 and Q2 corresponded to D6
[00:19:34:319 - 00:19:34:959] **Speaker 1:** for element one.
[00:19:36:770 - 00:19:38:400] **Speaker 1:** We could do this manually or we just use the
[00:19:38:400 - 00:19:40:109] **Speaker 1:** assembly matrix which we've already derived.
[00:19:41:420 - 00:19:42:900] **Speaker 1:** And check that it works.
[00:19:45:119 - 00:19:47:640] **Speaker 1:** So, it's always good to interpret this if we go
[00:19:47:640 - 00:19:49:660] **Speaker 1:** back to our free body diagram for the element.
[00:19:50:900 - 00:19:53:579] **Speaker 1:** This is what it looks like here, the X is
[00:19:53:579 - 00:19:56:510] **Speaker 1:** downwards, D1 through D3 up here and D4 through D6
[00:19:56:510 - 00:19:57:000] **Speaker 1:** up here.
[00:19:57:920 - 00:19:58:510] **Speaker 1:** Down the bottom.
[00:20:00:979 - 00:20:02:680] **Speaker 1:** Yeah, so we're just gonna quickly resketch that.
[00:20:04:300 - 00:20:07:170] **Speaker 1:** So this is element 1, X goes downwards.
[00:20:08:140 - 00:20:08:880] **Speaker 1:** Watch the right.
[00:20:11:530 - 00:20:13:989] **Speaker 1:** Now I'm just gonna repeat, this is the one.
[00:20:15:359 - 00:20:16:239] **Speaker 1:** This is D2.
[00:20:18:130 - 00:20:19:099] **Speaker 1:** This is D3.
[00:20:20:270 - 00:20:26:760] **Speaker 0:** And then we have 4 D5.
[00:20:28:890 - 00:20:30:010] **Speaker 1:** And D6.
[00:20:36:040 - 00:20:38:410] **Speaker 1:** So that's just the original free body diagram.
[00:20:38:890 - 00:20:39:969] **Speaker 1:** Let's look at a couple of things here.
[00:20:40:170 - 00:20:44:050] **Speaker 1:** We have 3, so this is essentially metres, metres and
[00:20:44:050 - 00:20:44:949] **Speaker 1:** gradients.
[00:20:46:599 - 00:20:48:380] **Speaker 1:** Um, so we take these 3 here.
[00:20:49:630 - 00:20:51:589] **Speaker 1:** And they all correspond to here.
[00:20:51:829 - 00:20:54:089] **Speaker 1:** So that was a fixed support.
[00:20:58:329 - 00:20:59:969] **Speaker 1:** It's always good to just, you know, apply these quick
[00:20:59:969 - 00:21:03:010] **Speaker 1:** sanity checks, saying, you know, I, this element was fixed
[00:21:03:010 - 00:21:04:050] **Speaker 1:** to its upper end.
[00:21:04:410 - 00:21:06:930] **Speaker 1:** We would expect there to be zero just translation and
[00:21:06:930 - 00:21:09:650] **Speaker 1:** zero rotation, and that's what we got in our answer,
[00:21:09:819 - 00:21:10:530] **Speaker 1:** so that's always good.
[00:21:12:739 - 00:21:13:699] **Speaker 1:** Now this entry here.
[00:21:14:819 - 00:21:18:900] **Speaker 1:** This one There's this one here, and that is the.
[00:21:20:219 - 00:21:21:339] **Speaker 1:** Vertical constraint.
[00:21:25:489 - 00:21:26:290] **Speaker 1:** From the roller.
[00:21:30:369 - 00:21:32:250] **Speaker 1:** It's good, you know, that was the, the basically the
[00:21:32:250 - 00:21:33:369] **Speaker 1:** way we set up the problem.
[00:21:33:969 - 00:21:35:829] **Speaker 1:** We would certainly hope that.
[00:21:36:949 - 00:21:39:750] **Speaker 1:** This actually gives that that solution.
[00:21:43:180 - 00:21:45:119] **Speaker 1:** Now we can also draw element 2.
[00:21:47:189 - 00:21:48:829] **Speaker 1:** X and Y.
[00:21:50:959 - 00:21:54:400] **Speaker 1:** to That's D1 for element 2.
[00:21:56:369 - 00:21:57:849] **Speaker 1:** D2, fell 2.
[00:22:00:079 - 00:22:01:540] **Speaker 1:** D3, 2.
[00:22:03:319 - 00:22:07:339] **Speaker 1:** 4 D5.
[00:22:09:140 - 00:22:10:130] **Speaker 1:** And D6.
[00:22:13:589 - 00:22:14:410] **Speaker 1:** Now in this case.
[00:22:15:369 - 00:22:18:640] **Speaker 1:** We have This one here.
[00:22:20:420 - 00:22:21:260] **Speaker 1:** That's the roller.
[00:22:22:219 - 00:22:24:500] **Speaker 1:** It's the vertical constraint that comes from the roller, so
[00:22:24:500 - 00:22:26:969] **Speaker 1:** we would expect the 2nd degree frame to be zero,
[00:22:27:020 - 00:22:27:719] **Speaker 1:** which it is.
[00:22:28:219 - 00:22:31:439] **Speaker 1:** We have a non-zero horizontal and a non-zero rotation.
[00:22:32:300 - 00:22:35:530] **Speaker 1:** And on the right hand side Yeah.
[00:22:38:079 - 00:22:44:619] **Speaker 1:** Take these 3 And that's the translations there.
[00:22:44:780 - 00:22:45:560] **Speaker 1:** So that's the pen.
[00:22:47:510 - 00:22:48:180] **Speaker 1:** At that note.
[00:22:51:170 - 00:22:52:819] **Speaker 1:** So it's always useful just to do that quick sanity
[00:22:52:819 - 00:22:54:540] **Speaker 1:** check and say, like, does it make sense?
[00:22:54:619 - 00:22:57:579] **Speaker 1:** Does this, does the numerical answer I'm getting out actually
[00:22:57:579 - 00:22:58:589] **Speaker 1:** match the physical solution?
[00:22:59:140 - 00:23:01:270] **Speaker 1:** In this case it does, so we can be relatively
[00:23:01:270 - 00:23:02:020] **Speaker 1:** happy about that.
[00:23:04:030 - 00:23:07:069] **Speaker 1:** If we use the the transformation matrix and we translate
[00:23:07:069 - 00:23:08:790] **Speaker 1:** from the uppercase D to the lowercase d.
[00:23:09:750 - 00:23:11:349] **Speaker 1:** Then we get some different numbers.
[00:23:12:260 - 00:23:15:329] **Speaker 1:** In this case, because it's a 90 degree transformation angle,
[00:23:15:780 - 00:23:17:729] **Speaker 1:** they're all the same numbers in here just in different
[00:23:17:729 - 00:23:18:099] **Speaker 1:** locations.
[00:23:18:420 - 00:23:19:739] **Speaker 1:** That won't always be the case.
[00:23:20:219 - 00:23:22:140] **Speaker 1:** If the element was say at a 30 degree angle,
[00:23:22:260 - 00:23:24:219] **Speaker 1:** you'll see new numbers in here that didn't appear there.
[00:23:26:349 - 00:23:31:630] **Speaker 1:** So, we'll quickly sketch the Element bo diagram for element
[00:23:31:630 - 00:23:32:010] **Speaker 1:** one.
[00:23:33:290 - 00:23:37:589] **Speaker 1:** Based upon its Local degrees of freedom.
[00:23:37:670 - 00:23:39:589] **Speaker 1:** That would be D1 for element 1, so it's always
[00:23:39:589 - 00:23:42:229] **Speaker 1:** in the X Y direction, X element direction.
[00:23:43:150 - 00:23:44:790] **Speaker 1:** D2, element 1, and then.
[00:23:46:400 - 00:23:48:339] **Speaker 1:** D3, that we have.
[00:23:49:770 - 00:23:53:439] **Speaker 1:** Before D5.
[00:23:55:520 - 00:23:56:770] **Speaker 1:** And D6.
[00:24:00:979 - 00:24:03:560] **Speaker 1:** So these 1st 3 still map up to here.
[00:24:04:609 - 00:24:06:079] **Speaker 1:** Again, that's effort to support.
[00:24:10:000 - 00:24:12:170] **Speaker 1:** Then we have what was the 5th degree of freedom.
[00:24:12:189 - 00:24:13:739] **Speaker 1:** It's actually now the 4th degree of freedom.
[00:24:15:520 - 00:24:17:109] **Speaker 1:** And that there is roller.
[00:24:20:670 - 00:24:24:119] **Speaker 1:** Constraints Vertical motion.
[00:24:32:390 - 00:24:36:569] **Speaker 1:** And then we have D2 here, which is the We
[00:24:36:569 - 00:24:40:000] **Speaker 1:** could also plot that, um, but because of the fact
[00:24:40:000 - 00:24:42:420] **Speaker 1:** that there's a 0 degree transformation angle.
[00:24:43:530 - 00:24:46:800] **Speaker 1:** We would have, um, this would be lowercase d's we'd
[00:24:46:800 - 00:24:48:530] **Speaker 1:** substitute them for uppercase D's and it would it would
[00:24:48:530 - 00:24:50:650] **Speaker 1:** essentially look the same as that, which is why this
[00:24:50:650 - 00:24:51:890] **Speaker 1:** vector looks the same as that one.
[00:24:52:060 - 00:24:53:680] **Speaker 1:** So they're only the same because of the fact that
[00:24:53:680 - 00:24:57:010] **Speaker 1:** there's a a zero degree transformation angle on there.
[00:25:01:160 - 00:25:03:599] **Speaker 1:** Once we've got these, um, we can go through and
[00:25:03:599 - 00:25:07:599] **Speaker 1:** we can use the, um, stiffness equation to get the
[00:25:07:599 - 00:25:10:319] **Speaker 1:** corresponding forcing terms that exist within the ounces.
[00:25:10:359 - 00:25:11:880] **Speaker 1:** That is one of the things we were asked for
[00:25:11:880 - 00:25:12:520] **Speaker 1:** in the question.
[00:25:15:260 - 00:25:17:500] **Speaker 1:** And we can also go through and we can apply
[00:25:17:500 - 00:25:20:339] **Speaker 1:** this, we can take the uppercase D's and we can
[00:25:20:339 - 00:25:23:900] **Speaker 1:** multiply those by our Khat, and that will give us
[00:25:23:900 - 00:25:27:479] **Speaker 1:** our forcing vectors and, um, global coordinates.
[00:25:34:790 - 00:25:37:050] **Speaker 1:** So if we're going to go through this and say,
[00:25:37:760 - 00:25:39:680] **Speaker 1:** Let's have a look at some of the forcing terms
[00:25:39:680 - 00:25:40:079] **Speaker 1:** that results.
[00:25:40:119 - 00:25:43:300] **Speaker 1:** So this is in um Local coordinates.
[00:25:43:430 - 00:25:45:630] **Speaker 1:** Now we would expect because of the zero degree transformation
[00:25:45:630 - 00:25:47:109] **Speaker 1:** angle that the uppercase F is going to be the
[00:25:47:109 - 00:25:50:579] **Speaker 1:** same as this, and the uppercase uppercase F2 will be
[00:25:50:579 - 00:25:52:069] **Speaker 1:** the same as the lowercase F2.
[00:25:52:430 - 00:25:54:150] **Speaker 1:** And then this one here will be the same.
[00:25:54:229 - 00:25:55:989] **Speaker 1:** The uppercase F1 will have the same numbers in it
[00:25:55:989 - 00:25:58:359] **Speaker 1:** but in a different order because of the the difference
[00:25:58:359 - 00:26:00:410] **Speaker 1:** between these 23 point diagrams.
[00:26:04:939 - 00:26:06:630] **Speaker 1:** So we've got our two forcing vectors here.
[00:26:09:300 - 00:26:14:079] **Speaker 1:** First thing we can see here, There's 6th element here.
[00:26:15:329 - 00:26:19:630] **Speaker 1:** So this here Was a pin support.
[00:26:24:329 - 00:26:25:670] **Speaker 1:** At the right hand.
[00:26:28:160 - 00:26:36:689] **Speaker 1:** Lord Incapable Of momentary action.
[00:26:42:050 - 00:26:44:420] **Speaker 1:** So that's good, you know, if, if there was, if
[00:26:44:420 - 00:26:47:579] **Speaker 1:** we had a, um, A set up where it was
[00:26:47:579 - 00:26:50:859] **Speaker 1:** not possible that that can provide a moment reaction and
[00:26:50:859 - 00:26:53:859] **Speaker 1:** we found that there was a non-zero moment in the
[00:26:53:859 - 00:26:56:219] **Speaker 1:** element at the righthand end, clearly something's gone wrong.
[00:26:56:380 - 00:26:58:560] **Speaker 1:** So again that measures our physical setup.
[00:27:01:609 - 00:27:02:290] **Speaker 1:** This one here.
[00:27:06:479 - 00:27:10:069] **Speaker 1:** Um, this is the, so we, we're going to follow
[00:27:10:069 - 00:27:14:079] **Speaker 1:** through, so we go, um, global X, global Y, global
[00:27:14:079 - 00:27:14:479] **Speaker 1:** Z.
[00:27:15:560 - 00:27:18:260] **Speaker 1:** And then we've got those, those 3, it's like all
[00:27:18:260 - 00:27:19:260] **Speaker 1:** 3 of these come down.
[00:27:20:699 - 00:27:22:770] **Speaker 1:** Take them as a group and come down to the
[00:27:22:770 - 00:27:22:920] **Speaker 1:** snow.
[00:27:27:150 - 00:27:29:589] **Speaker 1:** So we've just got the, we're just taking this, applying
[00:27:29:589 - 00:27:31:689] **Speaker 1:** the free body diagram and drawing these on here.
[00:27:34:050 - 00:27:35:510] **Speaker 1:** This is element 1, this is element 2.
[00:27:40:510 - 00:27:42:709] **Speaker 1:** Now one thing that's perhaps worth noting here is that
[00:27:42:709 - 00:27:45:270] **Speaker 1:** the pin support of the Rahindin is incapable of reaction.
[00:27:46:599 - 00:27:59:130] **Speaker 1:** As Element one is the only member Connected.
[00:28:00:949 - 00:28:07:670] **Speaker 1:** To the pin It has No moment.
[00:28:12:599 - 00:28:14:520] **Speaker 1:** Now it's important to realise that because at the left-hand
[00:28:14:520 - 00:28:17:640] **Speaker 1:** side, we actually do have non-zero moments in these two.
[00:28:18:770 - 00:28:24:619] **Speaker 1:** Elements If there were multiple elements adding up into the,
[00:28:24:660 - 00:28:26:910] **Speaker 1:** the top, they must sum up to zero and they
[00:28:26:910 - 00:28:30:540] **Speaker 1:** must not have represent any applied external moment if there
[00:28:30:540 - 00:28:31:959] **Speaker 1:** was none applied in the question.
[00:28:32:709 - 00:28:35:140] **Speaker 1:** But that doesn't necessarily mean at the moment internally within
[00:28:35:140 - 00:28:36:469] **Speaker 1:** each element has to be zero.
[00:28:37:770 - 00:28:40:640] **Speaker 1:** Uh, if there are multiple elements framing into a single
[00:28:40:640 - 00:28:41:420] **Speaker 1:** nodal point.
[00:28:44:530 - 00:28:47:319] **Speaker 1:** Any Uh, yes, I do.
[00:28:47:599 - 00:28:48:219] **Speaker 1:** Sorry about that.
[00:28:48:579 - 00:28:49:430] **Speaker 1:** Thanks for bringing that out.
[00:28:51:189 - 00:28:51:430] **Speaker 1:** You to.
[00:28:59:079 - 00:29:00:000] **Speaker 1:** So let's have a quick look here.
[00:29:00:040 - 00:29:02:319] **Speaker 1:** We've got this and this.
[00:29:08:930 - 00:29:10:209] **Speaker 1:** Horizontal forces.
[00:29:12:119 - 00:29:17:810] **Speaker 1:** In each element Equal and opposite.
[00:29:23:930 - 00:29:39:750] **Speaker 1:** Some to zero As the roller Cannot Provide Horizontal reaction
[00:29:45:640 - 00:29:49:160] **Speaker 1:** So, if there was a a pin joint instead of
[00:29:49:160 - 00:29:51:959] **Speaker 1:** a roller there, it could be that there's non-zero values
[00:29:51:959 - 00:29:54:199] **Speaker 1:** that sum in both elements, and there's sum to a
[00:29:54:199 - 00:29:56:449] **Speaker 1:** non-zero value, which is the total reaction force.
[00:29:57:030 - 00:29:59:310] **Speaker 1:** But in this case, because it was a roller and
[00:29:59:310 - 00:30:03:520] **Speaker 1:** there was no capability of providing a horizontal reaction, we
[00:30:03:520 - 00:30:06:060] **Speaker 1:** end up with equal and opposite horizontal forces here.
[00:30:06:520 - 00:30:09:479] **Speaker 1:** They sum to zero and indicate there was no horizontal
[00:30:09:479 - 00:30:11:660] **Speaker 1:** reaction from the roller, as we would expect.
[00:30:19:650 - 00:30:23:670] **Speaker 1:** Now what we've got here is the vector of um
[00:30:23:810 - 00:30:26:050] **Speaker 1:** that's just a repeat of this these numbers above, but
[00:30:26:050 - 00:30:29:630] **Speaker 1:** we have this um vector of numbers for F1.
[00:30:31:640 - 00:30:35:209] **Speaker 1:** And this is the corresponding diagram with these applied onto
[00:30:35:209 - 00:30:36:130] **Speaker 1:** a diagram.
[00:30:38:300 - 00:30:40:060] **Speaker 1:** Now what we're gonna look at here is we can
[00:30:40:060 - 00:30:41:719] **Speaker 1:** take the 1st and the 4th values.
[00:30:43:439 - 00:30:44:369] **Speaker 1:** Let's have a look at those.
[00:30:46:520 - 00:30:48:650] **Speaker 1:** If one for element one.
[00:30:50:319 - 00:30:52:150] **Speaker 1:** And F4 for element 1.
[00:30:56:790 - 00:30:58:180] **Speaker 1:** The two Shia forces.
[00:31:02:560 - 00:31:03:680] **Speaker 1:** are equal and opposite.
[00:31:11:510 - 00:31:13:540] **Speaker 1:** So I have mentioned this a little very briefly before,
[00:31:13:569 - 00:31:16:050] **Speaker 1:** but you know, this does actually extend very nicely to
[00:31:16:050 - 00:31:17:000] **Speaker 1:** a dynamic problem.
[00:31:17:540 - 00:31:20:260] **Speaker 1:** We can introduce mass matrices, we can introduce stiffness and
[00:31:20:260 - 00:31:22:420] **Speaker 1:** damping matrix, we've got the stiffness matrix, we introduce a
[00:31:22:420 - 00:31:24:959] **Speaker 1:** damping matrix, and we can solve dynamic problems.
[00:31:25:930 - 00:31:27:530] **Speaker 1:** But we're not there yet, and we're not gonna be
[00:31:27:530 - 00:31:29:329] **Speaker 1:** there in these 4 weeks.
[00:31:30:469 - 00:31:32:589] **Speaker 1:** So everything we're doing in this class is stack equilibrium.
[00:31:33:640 - 00:31:37:359] **Speaker 1:** So we would expect the overall structure and every element
[00:31:37:359 - 00:31:39:760] **Speaker 1:** within the structure to be in static equilibrium.
[00:31:41:510 - 00:31:44:000] **Speaker 1:** F1 and F4, the two share forces that exist here
[00:31:44:000 - 00:31:47:199] **Speaker 1:** and here are equal and opposite, so we can be
[00:31:47:199 - 00:31:47:719] **Speaker 1:** happy with that.
[00:31:47:839 - 00:31:48:520] **Speaker 1:** That's a good sign.
[00:31:50:630 - 00:31:52:099] **Speaker 1:** Let's look at the two axial forces.
[00:31:52:319 - 00:31:53:410] **Speaker 1:** So we've got this one.
[00:31:54:939 - 00:32:00:189] **Speaker 1:** And this one So if 2 for element 1.
[00:32:01:160 - 00:32:03:630] **Speaker 1:** And if 5 fell 1.
[00:32:05:680 - 00:32:07:469] **Speaker 1:** The two axial forces.
[00:32:11:760 - 00:32:12:640] **Speaker 1:** I reset.
[00:32:17:660 - 00:32:19:739] **Speaker 1:** So we'll give that a tick, we should be happy
[00:32:19:739 - 00:32:20:060] **Speaker 1:** with that.
[00:32:20:260 - 00:32:22:130] **Speaker 1:** In this case they're 0, but they could be non-zero,
[00:32:22:140 - 00:32:24:199] **Speaker 1:** and we would still expect them to be equal and
[00:32:24:199 - 00:32:24:699] **Speaker 1:** opposite.
[00:32:27:689 - 00:32:29:239] **Speaker 1:** Let's have a look at the moment terms now.
[00:32:30:000 - 00:32:31:920] **Speaker 1:** This one and this one.
[00:32:32:719 - 00:32:42:219] **Speaker 1:** So We have The moment terms Which is F3 valent
[00:32:42:219 - 00:32:42:560] **Speaker 1:** 1.
[00:32:43:719 - 00:32:45:500] **Speaker 1:** And F6, the element 1.
[00:32:47:229 - 00:32:56:880] **Speaker 1:** And these are not Equal and opposite That's a problem,
[00:32:57:140 - 00:32:57:660] **Speaker 1:** is it?
[00:32:57:979 - 00:32:59:199] **Speaker 1:** Should we be concerned about that?
[00:33:01:109 - 00:33:02:459] **Speaker 1:** Does this mean that we've got something wrong?
[00:33:02:520 - 00:33:04:170] **Speaker 1:** Does this mean that Alan is not in equilibrium?
[00:33:07:410 - 00:33:08:219] **Speaker 1:** You're right, it doesn't.
[00:33:08:979 - 00:33:09:699] **Speaker 1:** Well, what are you missing?
[00:33:09:770 - 00:33:11:239] **Speaker 1:** What's the other piece of information there?
[00:33:12:739 - 00:33:14:500] **Speaker 1:** There's a forced couple from the two shared forces, right?
[00:33:14:780 - 00:33:15:239] **Speaker 1:** Yes.
[00:33:15:780 - 00:33:17:060] **Speaker 1:** So it's very tempting.
[00:33:20:030 - 00:33:20:849] **Speaker 1:** Maybe so.
[00:33:22:300 - 00:33:23:160] **Speaker 1:** You can cycle this thing.
[00:33:27:209 - 00:33:27:849] **Speaker 1:** See if it comes back.
[00:33:28:050 - 00:33:30:569] **Speaker 1:** It's very tempting to assume that everything should be um
[00:33:30:569 - 00:33:33:189] **Speaker 1:** equal and opposite and the moment terms should automatically be,
[00:33:33:449 - 00:33:36:410] **Speaker 1:** uh, equal and opposite, um, the, the element has to
[00:33:36:410 - 00:33:37:670] **Speaker 1:** be in moment equilibrium.
[00:33:39:020 - 00:33:41:579] **Speaker 1:** That doesn't necessarily mean that the moments have to be
[00:33:41:579 - 00:33:42:099] **Speaker 1:** equal.
[00:33:43:780 - 00:33:45:709] **Speaker 1:** In the absence of any Shia forces.
[00:33:46:810 - 00:33:49:599] **Speaker 1:** So if we have a an element that by virtue
[00:33:49:599 - 00:33:50:859] **Speaker 1:** of the way it fits into the structure.
[00:33:51:849 - 00:33:53:829] **Speaker 1:** Um, doesn't.
[00:33:55:540 - 00:33:58:349] **Speaker 1:** Um, have any shear forces acting on it, then we
[00:33:58:349 - 00:34:00:380] **Speaker 1:** would expect the two moment terms to be equal and
[00:34:00:380 - 00:34:03:060] **Speaker 1:** opposite, but, uh, in the presence of shear forces, the
[00:34:03:060 - 00:34:05:380] **Speaker 1:** moment terms can be different and the element can still
[00:34:05:380 - 00:34:07:939] **Speaker 1:** be in vertical equilibrium.
[00:34:24:540 - 00:34:24:550] **Speaker 1:** Look.
[00:34:29:769 - 00:34:31:269] **Speaker 1:** Right, so we're getting there.
[00:34:41:839 - 00:34:44:039] **Speaker 1:** So the key piece there is that the two Shia
[00:34:44:039 - 00:34:44:779] **Speaker 1:** forces.
[00:34:50:888 - 00:34:52:189] **Speaker 1:** Create a forced couple.
[00:35:00:459 - 00:35:01:679] **Speaker 1:** And contribute a moment.
[00:35:11:020 - 00:35:13:320] **Speaker 1:** So if we some moments.
[00:35:14:989 - 00:35:20:949] **Speaker 1:** About Note 2.
[00:35:22:250 - 00:35:24:149] **Speaker 1:** We'll say that counterclockwise is positive.
[00:35:25:320 - 00:35:32:120] **Speaker 1:** We end up with -18.0645. That's the, um, concentrated moment.
[00:35:33:439 - 00:35:39:090] **Speaker 1:** Then we add on our moment of no 2, 45.1613.
[00:35:39:870 - 00:35:41:510] **Speaker 1:** And then we um.
[00:35:42:830 - 00:35:46:550] **Speaker 1:** We're taking moments about node 2, and this sheer force
[00:35:46:550 - 00:35:48:629] **Speaker 1:** would contribute a clockwise moment, so we're gonna call this
[00:35:48:629 - 00:35:49:530] **Speaker 1:** a negative moment.
[00:35:50:530 - 00:35:52:939] **Speaker 1:** So it's 2.7097.
[00:35:54:110 - 00:35:54:790] **Speaker 1:** Time 10.
[00:35:56:159 - 00:35:57:840] **Speaker 1:** And if we do that based upon the numbers we
[00:35:57:840 - 00:35:59:179] **Speaker 1:** get there, we would get 0 point.
[00:36:00:469 - 00:36:02:050] **Speaker 1:** 0178.
[00:36:03:419 - 00:36:05:560] **Speaker 1:** Killing Newton metres, which is just a rounding error.
[00:36:07:409 - 00:36:10:250] **Speaker 1:** If we were to do this within Python rather than
[00:36:10:250 - 00:36:13:280] **Speaker 1:** copying down numbers, um, we would still get a non-zero
[00:36:13:280 - 00:36:16:260] **Speaker 1:** value, but it would be, you know, probably 10-15 or
[00:36:16:260 - 00:36:16:770] **Speaker 1:** something like that.
[00:36:16:919 - 00:36:19:250] **Speaker 1:** So you see the element is an equilibrium.
[00:36:19:649 - 00:36:23:270] **Speaker 1:** Uh, yeah, don't be alarmed if you see different moments.
[00:36:24:120 - 00:36:25:979] **Speaker 1:** That doesn't necessarily mean that anything is wrong.
[00:36:28:520 - 00:36:30:250] **Speaker 1:** Um, we can look at the reaction forces.
[00:36:30:600 - 00:36:32:000] **Speaker 1:** I might just skip over that for now because I
[00:36:32:000 - 00:36:34:280] **Speaker 1:** just want to make sure that we cover the, the
[00:36:34:280 - 00:36:35:320] **Speaker 1:** stuff for the lab this afternoon.
[00:36:35:439 - 00:36:36:899] **Speaker 1:** We can always come back for that tomorrow.
[00:36:39:479 - 00:36:43:270] **Speaker 1:** So we do have, we can basically sum this up.
[00:36:44:469 - 00:36:45:610] **Speaker 1:** And we can get this overall.
[00:36:47:340 - 00:36:52:429] **Speaker 1:** Um Yeah, summing up those individual element forces that will
[00:36:52:429 - 00:36:55:310] **Speaker 1:** give us the overall reaction forces, and we see 140
[00:36:55:310 - 00:36:57:550] **Speaker 1:** kilonewton metres here which is our applied external load.
[00:36:59:320 - 00:37:01:310] **Speaker 1:** So we'll come back to that, but.
[00:37:02:080 - 00:37:04:159] **Speaker 1:** Initially what I want to do here is just look,
[00:37:04:250 - 00:37:06:429] **Speaker 1:** so this is the the lab for this afternoon.
[00:37:07:479 - 00:37:09:879] **Speaker 1:** It looks a lot like last week's lab in terms
[00:37:09:879 - 00:37:10:639] **Speaker 1:** of the structure.
[00:37:10:919 - 00:37:12:080] **Speaker 1:** There's no, there's no mistake.
[00:37:12:209 - 00:37:15:159] **Speaker 1:** It's purposely done to try and show you the linkage
[00:37:15:159 - 00:37:16:820] **Speaker 1:** and the the extension of what you did last week.
[00:37:18:540 - 00:37:22:340] **Speaker 1:** The first thing here is entering local frames.
[00:37:22:419 - 00:37:24:899] **Speaker 1:** The idea is you create this local frame function and
[00:37:24:899 - 00:37:25:840] **Speaker 1:** it's for one element.
[00:37:27:040 - 00:37:29:000] **Speaker 1:** Um, so this of course is.
[00:37:30:310 - 00:37:32:729] **Speaker 1:** Refer to page 79.
[00:37:33:820 - 00:37:35:179] **Speaker 1:** That was where we had that matrix.
[00:37:35:419 - 00:37:36:889] **Speaker 1:** Now you do have to enter a 6 by 6
[00:37:36:889 - 00:37:37:520] **Speaker 1:** matrix.
[00:37:38:020 - 00:37:39:580] **Speaker 1:** You only ever have to do that once because that
[00:37:39:580 - 00:37:41:100] **Speaker 1:** is the matrix for all frameuls.
[00:37:41:139 - 00:37:42:879] **Speaker 1:** You don't have to do that multiple times.
[00:37:43:850 - 00:37:46:570] **Speaker 1:** It is probably worth once you set that up, um,
[00:37:47:139 - 00:37:49:300] **Speaker 1:** to put some numbers in and subtract the transfers off
[00:37:49:300 - 00:37:53:060] **Speaker 1:** itself because, um, if, if a matrix is symmetric and
[00:37:53:060 - 00:37:56:120] **Speaker 1:** you subtract the transfers off itself, you should get an
[00:37:56:120 - 00:37:58:300] **Speaker 1:** all zero matrix and if you get something that's non-zero,
[00:37:58:340 - 00:38:00:340] **Speaker 1:** it's just a good sign that maybe you've entered something
[00:38:00:340 - 00:38:00:600] **Speaker 1:** wrong.
[00:38:02:189 - 00:38:04:060] **Speaker 1:** Then we take the result there.
[00:38:04:399 - 00:38:08:469] **Speaker 1:** K1 comes in, we give it an angle alpha, and
[00:38:08:830 - 00:38:11:389] **Speaker 1:** we generate a transformation matrix multiply through and we get
[00:38:11:389 - 00:38:11:939] **Speaker 1:** khat.
[00:38:14:120 - 00:38:15:840] **Speaker 1:** Then we can generate.
[00:38:17:100 - 00:38:20:540] **Speaker 1:** Well that's, um, our assembly uh sorry, our transformation matrices
[00:38:20:540 - 00:38:20:860] **Speaker 1:** there.
[00:38:21:300 - 00:38:22:830] **Speaker 1:** We have our assembly matrices.
[00:38:23:100 - 00:38:25:459] **Speaker 1:** This is, we've already derived that and we just work
[00:38:25:459 - 00:38:25:939] **Speaker 1:** through the problems.
[00:38:26:020 - 00:38:26:800] **Speaker 1:** This will be D1.
[00:38:28:169 - 00:38:28:639] **Speaker 1:** 2.
[00:38:29:780 - 00:38:34:939] **Speaker 1:** 3 Before D5 and D6.
[00:38:39:669 - 00:38:42:989] **Speaker 1:** And then the same thing for element 2.
[00:38:44:159 - 00:38:47:500] **Speaker 1:** We can get our little KG components, our overall KG,
[00:38:47:719 - 00:38:50:659] **Speaker 1:** um, this is the Um, Q value, so this will
[00:38:50:659 - 00:38:52:219] **Speaker 1:** be in Newton's.
[00:38:53:250 - 00:38:55:889] **Speaker 1:** Newton metres and Newton metres.
[00:38:58:810 - 00:39:01:100] **Speaker 1:** We can solve, we get our deflection values.
[00:39:02:320 - 00:39:04:949] **Speaker 1:** Extract those and get our deflection vectors.
[00:39:07:050 - 00:39:13:919] **Speaker 1:** And then Um From that.
[00:39:15:909 - 00:39:20:070] **Speaker 1:** Yeah our detection vectors and local coordinates, our sourcing terms
[00:39:20:070 - 00:39:23:229] **Speaker 1:** and local coordinates, and our forcing terms and global coordinates.
[00:39:24:979 - 00:39:27:300] **Speaker 1:** Now, if we were to apply the process that we
[00:39:27:300 - 00:39:28:239] **Speaker 1:** used last week.
[00:39:29:090 - 00:39:32:370] **Speaker 1:** We would end up with this um structure here.
[00:39:34:629 - 00:39:37:030] **Speaker 1:** So this here would be.
[00:39:38:100 - 00:39:44:550] **Speaker 1:** Q1 And What we actually, you know, this essentially is
[00:39:44:550 - 00:39:50:620] **Speaker 1:** a Very simplified.
[00:39:52:959 - 00:40:08:469] **Speaker 1:** And ultimately, Incorrect visualisation Now we go back to our
[00:40:09:010 - 00:40:09:969] **Speaker 1:** um Q value.
[00:40:11:050 - 00:40:17:610] **Speaker 1:** We actually, we had a Uh, horizontal deflection, that was
[00:40:17:610 - 00:40:20:850] **Speaker 1:** Q1, we also had a, a positive rotation Q2 and
[00:40:20:850 - 00:40:22:250] **Speaker 1:** a negative rotation Q3.
[00:40:23:320 - 00:40:24:659] **Speaker 1:** So if we were to sketch this by hand.
[00:40:26:639 - 00:40:29:199] **Speaker 1:** We would say, draw this like this.
[00:40:30:770 - 00:40:33:850] **Speaker 1:** Now, because we, we constrain these to rotate together with
[00:40:33:850 - 00:40:35:709] **Speaker 1:** the same degree of freedom, we expect that to remain
[00:40:35:709 - 00:40:36:489] **Speaker 1:** a 90 degrees.
[00:40:37:750 - 00:40:39:379] **Speaker 1:** And we know that we have 0 slope and zero
[00:40:39:379 - 00:40:42:270] **Speaker 1:** deflection here, so we would expect to essentially have something
[00:40:42:270 - 00:40:45:570] **Speaker 1:** which shows a continuous curve here.
[00:40:47:270 - 00:40:50:250] **Speaker 1:** Goes from this deflected position at the bottom node.
[00:40:51:100 - 00:40:55:530] **Speaker 1:** Up to a um Rotated position here.
[00:40:56:580 - 00:40:59:189] **Speaker 1:** And then we know that this was a negative, so
[00:40:59:629 - 00:41:04:110] **Speaker 1:** keeping in mind that counterclockwise is a positive rotation, but
[00:41:04:110 - 00:41:05:649] **Speaker 1:** we actually solve for a negative rotation.
[00:41:07:129 - 00:41:10:729] **Speaker 1:** Then this here would be our Q3.
[00:41:12:040 - 00:41:14:080] **Speaker 1:** And then once we know the what's happening at the
[00:41:14:080 - 00:41:18:290] **Speaker 1:** nodes, we can draw a curve which interacts like that.
[00:41:19:070 - 00:41:21:080] **Speaker 1:** And then this value in here would be RQ2.
[00:41:25:149 - 00:41:29:530] **Speaker 1:** So that curved shape Is what we would expect.
[00:41:29:610 - 00:41:32:360] **Speaker 1:** That's the, the behaviour that we, we expect to have
[00:41:32:360 - 00:41:32:850] **Speaker 1:** happen.
[00:41:34:389 - 00:41:38:260] **Speaker 1:** Now The question you might be asking, well, we have
[00:41:38:260 - 00:41:41:860] **Speaker 1:** our shape functions, aren't they able to give us that
[00:41:41:860 - 00:41:42:159] **Speaker 1:** information?
[00:41:42:620 - 00:41:45:699] **Speaker 1:** Absolutely they are, and we'll work through a process of
[00:41:45:699 - 00:41:47:800] **Speaker 1:** using those to actually get that the entire.
[00:41:48:600 - 00:41:49:370] **Speaker 1:** Curved shape.
[00:41:51:879 - 00:41:57:229] **Speaker 1:** Now this is quite a long Wounded explanation, um, but
[00:41:57:229 - 00:41:59:340] **Speaker 1:** what it essentially says is that when we built this
[00:41:59:340 - 00:41:59:350] **Speaker 1:** up.
[00:42:00:820 - 00:42:03:379] **Speaker 1:** At the central nodal point, we have this rotation.
[00:42:03:500 - 00:42:06:179] **Speaker 1:** So we had a slotted like a roller, it could
[00:42:06:179 - 00:42:09:620] **Speaker 1:** equally be a slotted pin like this where we're constraining
[00:42:09:620 - 00:42:12:820] **Speaker 1:** vertical motion but we're allowing it to move freely horizontally
[00:42:12:979 - 00:42:14:879] **Speaker 1:** and we're allowing it to rotate freely with the support.
[00:42:15:899 - 00:42:18:899] **Speaker 1:** But because we're linking the two elements to translate together
[00:42:18:899 - 00:42:21:620] **Speaker 1:** and rotate together, this is what this might actually look
[00:42:21:620 - 00:42:21:979] **Speaker 1:** like.
[00:42:23:649 - 00:42:31:620] **Speaker 1:** Physically, and this is referring to The nodal point Down
[00:42:31:620 - 00:42:32:770] **Speaker 1:** in this bottom corner here.
[00:42:33:870 - 00:42:37:010] **Speaker 1:** Like this is how we sort of schematically represent it,
[00:42:37:669 - 00:42:40:040] **Speaker 1:** but the question is what might that look like physically?
[00:42:40:300 - 00:42:44:050] **Speaker 1:** And the key thing to realise there is that while
[00:42:44:050 - 00:42:48:270] **Speaker 1:** there's a rotationally free component, that's essentially saying the elements
[00:42:48:270 - 00:42:51:070] **Speaker 1:** are free to rotate relative to the support, but we
[00:42:51:070 - 00:42:53:229] **Speaker 1:** are linking them, we're assuming that they're rigidly welded to
[00:42:53:229 - 00:42:53:929] **Speaker 1:** each other.
[00:42:54:750 - 00:42:58:659] **Speaker 1:** Such that they actually rotate together and translate together, um,
[00:42:58:669 - 00:43:01:629] **Speaker 1:** but independently of any support point.
[00:43:02:669 - 00:43:04:830] **Speaker 1:** So this is just an important thing about mathematically what
[00:43:04:830 - 00:43:08:949] **Speaker 1:** we do there, um, and, you know, that they're assumed
[00:43:08:949 - 00:43:09:739] **Speaker 1:** to move together.
[00:43:10:030 - 00:43:12:310] **Speaker 1:** And as there was a question, um, we will come
[00:43:12:310 - 00:43:14:350] **Speaker 1:** back to that and look, if, if we had elements
[00:43:14:350 - 00:43:16:469] **Speaker 1:** which were pinned to each other, we can actually break
[00:43:16:469 - 00:43:19:070] **Speaker 1:** that coupling mathematically, but that'll be something we come back
[00:43:19:070 - 00:43:19:770] **Speaker 1:** to next week.
[00:43:23:560 - 00:43:24:000] **Speaker 1:** Sorry.
[00:43:27:169 - 00:43:30:010] **Speaker 1:** This is the this is skeleton code to say how
[00:43:30:010 - 00:43:32:689] **Speaker 1:** do we plot the full deflected shape of a frame
[00:43:32:689 - 00:43:33:090] **Speaker 1:** element.
[00:43:35:669 - 00:43:38:350] **Speaker 1:** So we've said all along that these um shape functions
[00:43:38:350 - 00:43:41:070] **Speaker 1:** are so powerful and they can interpolate behaviour and tell
[00:43:41:070 - 00:43:43:629] **Speaker 1:** us what's happening all the way internally within an element
[00:43:43:629 - 00:43:46:469] **Speaker 1:** based upon just nodal deflections and this is the chance
[00:43:46:469 - 00:43:46:989] **Speaker 1:** to prove it.
[00:43:48:629 - 00:43:50:110] **Speaker 1:** So we're gonna set up some skeleton code here.
[00:43:50:159 - 00:43:51:760] **Speaker 1:** So we're just gonna say, you know, this is just
[00:43:51:760 - 00:43:55:159] **Speaker 1:** some suggested form that I that I how I've used
[00:43:55:159 - 00:43:55:959] **Speaker 1:** when I've plotted it.
[00:43:56:110 - 00:43:58:290] **Speaker 1:** Um, so say plot to fixed shape might be the
[00:43:58:620 - 00:43:59:500] **Speaker 1:** the function.
[00:44:00:129 - 00:44:03:679] **Speaker 1:** Um, we have node 1 x, node 1 Y, node
[00:44:03:679 - 00:44:04:879] **Speaker 1:** 2 X, node 2 Y.
[00:44:05:159 - 00:44:07:860] **Speaker 1:** um, a deflection vector and local coordinates.
[00:44:08:750 - 00:44:11:709] **Speaker 1:** Some displacement magnification factor, so this is something that we're
[00:44:11:709 - 00:44:15:189] **Speaker 1:** exaggerating all our deflections from with, and the end points
[00:44:15:189 - 00:44:17:389] **Speaker 1:** is the number of points within an element that we
[00:44:17:389 - 00:44:19:949] **Speaker 1:** want to evaluate deflections at.
[00:44:22:120 - 00:44:25:669] **Speaker 1:** Now, one thing you might immediately notice is that there's
[00:44:25:669 - 00:44:27:020] **Speaker 1:** potentially some information here.
[00:44:28:820 - 00:44:29:820] **Speaker 1:** Some missing information.
[00:44:29:949 - 00:44:31:959] **Speaker 1:** So, the thing is you might say well what about
[00:44:31:959 - 00:44:33:929] **Speaker 1:** length and what about orientation?
[00:44:35:449 - 00:44:38:090] **Speaker 1:** You could add those as extra variables, but of course
[00:44:38:090 - 00:44:40:770] **Speaker 1:** within your code you can easily determine that.
[00:44:41:899 - 00:44:51:350] **Speaker 1:** So To get Al Calculate a delta X.
[00:44:53:169 - 00:44:56:000] **Speaker 1:** And a delta Y, so just between the two.
[00:44:57:020 - 00:45:00:560] **Speaker 1:** The location of the two x locations, the x coordinates
[00:45:00:560 - 00:45:02:790] **Speaker 1:** of the two nodal points and the Y coordinates of
[00:45:02:790 - 00:45:04:179] **Speaker 1:** the two nodal points, you can get the delta X
[00:45:04:179 - 00:45:04:929] **Speaker 1:** and the deltay.
[00:45:07:790 - 00:45:12:909] **Speaker 1:** And then simply use Good old Pythagoras, so Delta X
[00:45:12:909 - 00:45:13:469] **Speaker 1:** squared.
[00:45:14:429 - 00:45:16:280] **Speaker 1:** Plus delta Y 2 and then the square root of
[00:45:16:280 - 00:45:17:979] **Speaker 1:** that answer that will give you your length.
[00:45:23:479 - 00:45:27:570] **Speaker 1:** Alpha Can be obtained.
[00:45:29:260 - 00:45:31:100] **Speaker 1:** From Delta X.
[00:45:32:330 - 00:45:40:699] **Speaker 1:** And stuff Y But please use.
[00:45:42:590 - 00:45:46:889] **Speaker 1:** The full 4 quadrant.
[00:45:48:340 - 00:45:49:600] **Speaker 1:** Inverse 10 function.
[00:45:54:500 - 00:46:03:300] **Speaker 1:** So this would be Lampai Dot arc tan 2.
[00:46:04:560 - 00:46:07:260] **Speaker 1:** And you'd be fine feeding in delta X and Delta
[00:46:07:260 - 00:46:07:560] **Speaker 1:** Y.
[00:46:10:100 - 00:46:10:989] **Speaker 1:** Now, why is this important?
[00:46:11:110 - 00:46:12:209] **Speaker 1:** Why am I mentioning this?
[00:46:14:189 - 00:46:25:280] **Speaker 1:** So Do not use Lam high glass.
[00:46:26:689 - 00:46:29:489] **Speaker 1:** Act, which takes in basically delta Y.
[00:46:30:340 - 00:46:31:350] **Speaker 1:** Over a delta X.
[00:46:33:959 - 00:46:36:540] **Speaker 1:** The reason for that is if we actually plot.
[00:46:37:469 - 00:46:39:149] **Speaker 1:** All possible element orientations.
[00:46:39:270 - 00:46:40:810] **Speaker 1:** This is the sort of delta X.
[00:46:42:239 - 00:46:43:479] **Speaker 1:** And this is De Hawaii.
[00:46:44:629 - 00:46:46:909] **Speaker 1:** And we can have basically an element on any orientation,
[00:46:47:100 - 00:46:49:709] **Speaker 1:** assuming node 1 is anchored at the origin and node
[00:46:49:709 - 00:46:51:169] **Speaker 1:** 2 will move around this plane.
[00:46:53:860 - 00:46:55:939] **Speaker 1:** So, if we have an element that sits in the
[00:46:55:939 - 00:46:56:639] **Speaker 1:** squadrant.
[00:46:57:800 - 00:46:59:050] **Speaker 1:** And this is our alpha value.
[00:46:59:290 - 00:47:02:830] **Speaker 1:** Then in that quadrant our delta Y will be positive
[00:47:03:090 - 00:47:06:649] **Speaker 1:** and our delta X will be positive, which then means
[00:47:06:649 - 00:47:09:709] **Speaker 1:** that our delta Y divided by delta X.
[00:47:10:879 - 00:47:12:780] **Speaker 1:** Is positive.
[00:47:14:780 - 00:47:16:340] **Speaker 1:** If we were in this plane here.
[00:47:18:510 - 00:47:20:489] **Speaker 1:** Then we end up with a delta Y.
[00:47:21:500 - 00:47:24:580] **Speaker 1:** Positive, a delta X, negative.
[00:47:25:409 - 00:47:29:689] **Speaker 1:** And the argument delta Y over delta X will be
[00:47:29:689 - 00:47:30:250] **Speaker 1:** negative.
[00:47:32:330 - 00:47:33:709] **Speaker 1:** If we're in this squadron here.
[00:47:35:090 - 00:47:38:270] **Speaker 1:** We have a delta X negative.
[00:47:39:709 - 00:47:40:620] **Speaker 1:** A Y negative.
[00:47:41:820 - 00:47:45:459] **Speaker 1:** And our single input argument that we would give to
[00:47:45:459 - 00:47:46:520] **Speaker 1:** the ACTA function.
[00:47:47:439 - 00:47:49:500] **Speaker 1:** That will therefore be positive.
[00:47:52:229 - 00:47:53:949] **Speaker 1:** And if we finish this off down here.
[00:47:55:010 - 00:47:56:270] **Speaker 1:** We end up with a delta.
[00:47:56:610 - 00:47:57:090] **Speaker 1:** Y.
[00:47:59:199 - 00:48:04:129] **Speaker 1:** Negative, a delta X positive, and then the argument Delta
[00:48:04:129 - 00:48:05:580] **Speaker 1:** Y over delta X.
[00:48:06:659 - 00:48:07:439] **Speaker 1:** will be negative.
[00:48:09:590 - 00:48:11:219] **Speaker 1:** So what you can see here is if we have
[00:48:11:219 - 00:48:13:939] **Speaker 1:** these four angles which are all kind of 90 degrees
[00:48:13:939 - 00:48:15:939] **Speaker 1:** apart, so this and this are 180 degrees from each
[00:48:15:939 - 00:48:18:100] **Speaker 1:** other, and this and this are 180 degrees from each
[00:48:18:100 - 00:48:18:419] **Speaker 1:** other.
[00:48:19:459 - 00:48:22:239] **Speaker 1:** When we're putting in a single argument into a simple
[00:48:22:860 - 00:48:23:800] **Speaker 1:** inverse stand function.
[00:48:25:290 - 00:48:29:629] **Speaker 1:** That function is unable to distinguish between these two lines.
[00:48:30:379 - 00:48:33:239] **Speaker 1:** And likewise, it's unable to distinguish between these two lines.
[00:48:34:310 - 00:48:36:350] **Speaker 1:** So the standard arc tan function that is only essentially
[00:48:36:350 - 00:48:39:590] **Speaker 1:** a a um 180 degree tan function it basically operates
[00:48:39:590 - 00:48:44:050] **Speaker 1:** between plus 2 and minus 2 radians or plus minus
[00:48:44:050 - 00:48:44:889] **Speaker 1:** 90 degrees.
[00:48:45:790 - 00:48:48:399] **Speaker 1:** But if we use the ACTA 2 function, we go
[00:48:48:399 - 00:48:52:320] **Speaker 1:** through the whole 180 degrees and you'll never get caught
[00:48:52:320 - 00:48:52:679] **Speaker 1:** out.
[00:48:52:919 - 00:48:55:620] **Speaker 1:** So if you've got some sort of slightly unusual element
[00:48:55:620 - 00:48:59:520] **Speaker 1:** orientation, You won't get, if you use this, you'll never
[00:48:59:520 - 00:49:00:280] **Speaker 1:** get caught out.
[00:49:00:560 - 00:49:02:600] **Speaker 1:** If you use this, you may well get caught out
[00:49:02:879 - 00:49:05:159] **Speaker 1:** where it's taking an angle that is not the one
[00:49:05:159 - 00:49:06:060] **Speaker 1:** that you think it is.
[00:49:07:270 - 00:49:09:120] **Speaker 1:** So we've got through here, um.
[00:49:10:060 - 00:49:13:179] **Speaker 1:** Basically this is a vector of points, we've got our
[00:49:13:179 - 00:49:15:780] **Speaker 1:** shape functions, our axial shape functions and our transverse shape
[00:49:15:780 - 00:49:16:439] **Speaker 1:** functions.
[00:49:17:459 - 00:49:20:540] **Speaker 1:** We have the axial deflection U of X is equal
[00:49:20:540 - 00:49:24:459] **Speaker 1:** to our axial shape functions times the deflections, our transverse
[00:49:24:459 - 00:49:28:139] **Speaker 1:** is equal to our N times our deflection vector, we
[00:49:28:139 - 00:49:29:340] **Speaker 1:** can multiply that out.
[00:49:30:100 - 00:49:31:669] **Speaker 1:** Um, what we have here, a number of points.
[00:49:31:760 - 00:49:34:060] **Speaker 1:** So in this, this example end points would be 11,
[00:49:34:219 - 00:49:36:129] **Speaker 1:** so we're actually evaluating at 11 points.
[00:49:36:500 - 00:49:39:340] **Speaker 1:** We're breaking it into 10 sections and evaluating at 11
[00:49:39:340 - 00:49:39:879] **Speaker 1:** points.
[00:49:41:030 - 00:49:44:100] **Speaker 1:** Um, every 0.1 along the element and at the endpoints.
[00:49:45:919 - 00:49:47:489] **Speaker 1:** Um, what we will get there is a delta X
[00:49:47:489 - 00:49:52:540] **Speaker 1:** is how much it translates axially, the The UX is
[00:49:52:540 - 00:49:55:989] **Speaker 1:** actually the friction, the UX is transverse deflection shown here,
[00:49:56:340 - 00:49:58:419] **Speaker 1:** but we want to translate that into a delta XG
[00:49:58:419 - 00:49:59:600] **Speaker 1:** and a delta YG.
[00:50:00:350 - 00:50:02:879] **Speaker 1:** We can basically do this little vector diagram here, so
[00:50:02:879 - 00:50:04:260] **Speaker 1:** this is the undeflected position.
[00:50:05:199 - 00:50:06:479] **Speaker 1:** This is the defective position.
[00:50:07:949 - 00:50:08:909] **Speaker 1:** Quickly label that.
[00:50:12:620 - 00:50:14:010] **Speaker 1:** The undeflected position.
[00:50:15:570 - 00:50:17:510] **Speaker 1:** This here is the deflected position.
[00:50:22:590 - 00:50:26:090] **Speaker 1:** And uh if we essentially go through basically creating a,
[00:50:26:550 - 00:50:31:649] **Speaker 1:** um, deflections, creating some baseline of um values.
[00:50:35:919 - 00:50:38:959] **Speaker 1:** So this is what the basically the under undeflected baseline,
[00:50:39:479 - 00:50:42:219] **Speaker 1:** which is essentially a vector of all the blue points.
[00:50:43:310 - 00:50:46:949] **Speaker 1:** And then we add on the magnified deflections, and we
[00:50:46:949 - 00:50:49:310] **Speaker 1:** get deflected position which is essentially a vector of the
[00:50:49:310 - 00:50:50:290] **Speaker 1:** red points.
[00:50:50:830 - 00:50:52:949] **Speaker 1:** And if we plot that, this is the solution we
[00:50:52:949 - 00:50:53:270] **Speaker 1:** get.
[00:50:54:760 - 00:50:57:000] **Speaker 1:** So that's, um, you don't necessarily have to do the
[00:50:57:000 - 00:50:59:709] **Speaker 1:** pulling code, um, you will be need to be able
[00:50:59:709 - 00:51:02:830] **Speaker 1:** to sketch this in the test by hand, uh, and
[00:51:02:830 - 00:51:04:590] **Speaker 1:** if you've got the pulling code that will help guide
[00:51:04:590 - 00:51:06:580] **Speaker 1:** what you choose to sketch down by hand, but you
[00:51:06:580 - 00:51:07:270] **Speaker 1:** don't have to do that.
[00:51:07:389 - 00:51:09:830] **Speaker 1:** There'll be no sort of uh marks assigned for necessarily
[00:51:09:830 - 00:51:12:590] **Speaker 1:** doing this, but it is quite insightful into the process
[00:51:12:590 - 00:51:13:570] **Speaker 1:** if you choose to do so.
[00:51:15:050 - 00:51:16:889] **Speaker 1:** So thank you all for coming along, um, we'll see
[00:51:16:889 - 00:51:18:629] **Speaker 1:** you in the labs starting at one o'clock this afternoon.
[00:51:19:530 - 00:51:21:370] **Speaker 1:** And um yeah, see you later.
[00:51:48:030 - 00:51:48:870] **Speaker 0:** I did know that.
[00:51:54:760 - 00:51:59:879] **Speaker 0:** Using document camera, yeah, uh, it just in the last
[00:51:59:879 - 00:52:01:919] **Speaker 1:** couple of lectures in here it's just like crashed halfway
[00:52:01:919 - 00:52:02:239] **Speaker 1:** through.
[00:52:02:939 - 00:52:05:639] **Speaker 0:** If you power if you power cycle, it seems to
[00:52:05:639 - 00:52:10:899] **Speaker 1:** come back, um, so it's just, um, yeah, it hasn't,
[00:52:11:320 - 00:52:13:479] **Speaker 1:** it's created disruption but it's never like properly let me
[00:52:13:479 - 00:52:15:419] **Speaker 1:** down so I think you'll be OK.
[00:52:25:199 - 00:52:27:419] **Speaker 0:** Um we're talking about the cubic.
[00:52:31:360 - 00:52:34:290] **Speaker 0:** Um, it's just looking at how we first labelled it,
[00:52:34:540 - 00:52:34:939] **Speaker 0:** so.
[00:52:35:909 - 00:52:35:919] **Speaker 0:** Sure.
[00:52:40:989 - 00:52:41:790] **Speaker 0:** who won the bubble and.
[00:52:43:959 - 00:52:46:439] **Speaker 0:** So, but if we, we, we actually have to split,
[00:52:46:520 - 00:52:49:679] **Speaker 0:** so if we call this Q1 Q2 Q3, then we'll
[00:52:49:679 - 00:52:52:129] **Speaker 0:** go on the 30, but it's just based on the
[00:52:52:129 - 00:52:54:239] **Speaker 0:** structures, right?
[00:52:54:489 - 00:52:57:399] **Speaker 0:** And let's say that there was like a force acting
[00:52:57:399 - 00:53:00:899] **Speaker 0:** downwards that would then become zero mutants instead of zero
[00:53:00:899 - 00:53:01:719] **Speaker 1:** mutton leaders.
[00:53:01:860 - 00:53:01:870] **Speaker 1:** Yeah.
[00:53:02:159 - 00:53:04:760] **Speaker 1:** So if there was, um, if this was say there
[00:53:04:760 - 00:53:06:479] **Speaker 1:** was no support here and there was a shed force
[00:53:06:479 - 00:53:09:719] **Speaker 1:** enemy, then that would, yeah, so it's, it's based upon
[00:53:09:719 - 00:53:10:830] **Speaker 1:** whether or not the the spirit.
[00:53:11:560 - 00:53:12:050] **Speaker 1:** Awesome thank you so much.
[00:53:19:479 - 00:53:19:510] **Speaker 0:** to be out.
[00:53:25:790 - 00:53:26:870] **Speaker 0:** Can I just leave those there?
[00:53:26:949 - 00:53:27:399] **Speaker 0:** They were left.
[00:53:43:899 - 00:53:44:379] **Speaker 1:** Good luck.
[00:53:44:899 - 00:53:46:500] **Speaker 1:** Sorry, I was trying to rush through some stuff because
[00:53:46:500 - 00:53:47:820] **Speaker 1:** we were made this afternoon to make sure I cover
[00:53:47:820 - 00:53:48:520] **Speaker 1:** the last content.
[00:53:48:959 - 00:53:49:459] **Speaker 1:** No worries.
[00:53:50:090 - 00:53:51:419] **Speaker 1:** A lot easier to cover it now than trying to
[00:53:51:419 - 00:53:52:310] **Speaker 1:** explain to everyone individually.
[00:54:00:639 - 00:54:05:520] **Speaker 0:** My I.
[00:54:10:669 - 00:54:35:560] **Speaker 0:** Now I feel safer I think So I Yeah, I,
[00:54:35:629 - 00:54:42:250] **Speaker 0:** I really Uh, but.
[00:54:51:840 - 00:54:52:280] **Speaker 0:** Thank you.
[00:54:57:149 - 00:54:57:379] **Speaker 0:** Knight

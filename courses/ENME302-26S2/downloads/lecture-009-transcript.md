# ENME302-26S2 Lecture 9 native Echo transcript

Date: July 27, 2026 12:00pm-12:55pm
Transcript type: native Echo automated transcript.

[00:00:15:470 - 00:00:18:620] **Speaker 0:** Yeah Yeah, I.
[00:00:23:159 - 00:00:23:170] **Speaker 0:** That.
[00:00:27:690 - 00:00:36:729] **Speaker 0:** yeah Well, Kyorakoto, welcome along, everyone.
[00:00:38:669 - 00:00:41:380] **Speaker 1:** Might help if I put the image on the screen.
[00:00:44:909 - 00:00:45:470] **Speaker 1:** Yeah.
[00:00:46:069 - 00:00:47:590] **Speaker 1:** Looks like the screen suffered some damage.
[00:00:47:669 - 00:00:50:310] **Speaker 1:** I don't know quite what happened there but hopefully it's
[00:00:50:310 - 00:00:52:310] **Speaker 1:** still able to be read, OK.
[00:00:52:750 - 00:00:54:220] **Speaker 1:** Um, there's probably not a lot I can do about
[00:00:54:220 - 00:00:54:830] **Speaker 1:** that, but.
[00:00:56:229 - 00:00:58:389] **Speaker 1:** Um, what I wanna just talk about today is a
[00:00:58:389 - 00:00:59:119] **Speaker 1:** new element type.
[00:00:59:549 - 00:01:02:060] **Speaker 1:** So I've said early on, Yeah, the last two weeks,
[00:01:02:099 - 00:01:03:580] **Speaker 1:** we focused on bar elements.
[00:01:03:700 - 00:01:07:860] **Speaker 1:** So these were pure axial elements, uh, only considered defamation
[00:01:07:860 - 00:01:10:500] **Speaker 1:** along their length, so there was no capacity for them
[00:01:10:500 - 00:01:13:129] **Speaker 1:** to carry bending or moment, bending loads, you know, sheer
[00:01:13:129 - 00:01:14:279] **Speaker 1:** forces or bending moments.
[00:01:14:779 - 00:01:16:739] **Speaker 1:** Um, the assumption was that they were pin-jointed to each
[00:01:16:739 - 00:01:20:580] **Speaker 1:** other and they only carried loads at the nodal points
[00:01:20:580 - 00:01:22:599] **Speaker 1:** at those pin joints between elements.
[00:01:23:029 - 00:01:25:540] **Speaker 1:** And what we're gonna do today is we're gonna look
[00:01:25:540 - 00:01:26:260] **Speaker 1:** at a new element types.
[00:01:26:360 - 00:01:30:250] **Speaker 1:** We're gonna introduce, uh, bending through sheer forces and bending
[00:01:30:250 - 00:01:30:720] **Speaker 1:** moments.
[00:01:32:190 - 00:01:33:589] **Speaker 1:** Now, what we're gonna do with that is we're initially
[00:01:33:589 - 00:01:36:349] **Speaker 1:** going to put axial deformations aside.
[00:01:37:449 - 00:01:40:040] **Speaker 1:** We're just gonna focus just on the new components of
[00:01:40:040 - 00:01:40:550] **Speaker 1:** deflection.
[00:01:41:589 - 00:01:43:629] **Speaker 1:** And the obvious question you might have is, well, what
[00:01:43:629 - 00:01:44:669] **Speaker 1:** about elements that have both?
[00:01:44:900 - 00:01:45:790] **Speaker 1:** We'll get there, don't worry.
[00:01:45:949 - 00:01:47:190] **Speaker 1:** We're just gonna use this as a building block.
[00:01:47:230 - 00:01:49:629] **Speaker 1:** We're gonna put that to the side for for a
[00:01:49:629 - 00:01:52:069] **Speaker 1:** few days and then we'll bring it back in um
[00:01:52:309 - 00:01:53:830] **Speaker 1:** once we've got these derivations sorted.
[00:01:54:150 - 00:01:56:300] **Speaker 1:** So I touched a little bit at the end of
[00:01:56:300 - 00:01:59:550] **Speaker 1:** Friday, but um you may feel, well, you know, after
[00:01:59:550 - 00:02:00:209] **Speaker 1:** two weeks.
[00:02:01:099 - 00:02:02:940] **Speaker 1:** Couple of labs, you know, I feel like I was
[00:02:02:940 - 00:02:04:010] **Speaker 1:** finally start to get used to things.
[00:02:04:099 - 00:02:06:370] **Speaker 1:** I was finally starting to understand what things meant.
[00:02:06:620 - 00:02:09:059] **Speaker 1:** Well, the new element type will change a few things.
[00:02:09:179 - 00:02:11:660] **Speaker 1:** It means the matrices that we're dealing with are slightly
[00:02:11:660 - 00:02:12:100] **Speaker 1:** bigger.
[00:02:12:500 - 00:02:15:419] **Speaker 1:** It means that the vectors will be slightly bigger, but
[00:02:15:419 - 00:02:17:740] **Speaker 1:** the meaning of the variables is is exactly the same.
[00:02:17:979 - 00:02:20:940] **Speaker 1:** So uh meaning of our KE, the meaning of our
[00:02:20:940 - 00:02:23:580] **Speaker 1:** KE hat, and meaning of our KGE, a meaning of
[00:02:23:580 - 00:02:26:059] **Speaker 1:** our KG, the meaning of a transformation matrices.
[00:02:26:279 - 00:02:27:199] **Speaker 1:** These are all the same.
[00:02:27:960 - 00:02:30:800] **Speaker 1:** The way those variables manipulate relative to each other is
[00:02:30:800 - 00:02:31:460] **Speaker 1:** all the same.
[00:02:31:960 - 00:02:34:080] **Speaker 1:** But the size of the matrix and the specific number
[00:02:34:080 - 00:02:36:600] **Speaker 1:** within them may change, but nothing you've learned over the
[00:02:36:600 - 00:02:39:119] **Speaker 1:** last two weeks is by any means wasted when we
[00:02:39:119 - 00:02:39:779] **Speaker 1:** get into this.
[00:02:42:399 - 00:02:45:750] **Speaker 1:** So, um, so far, we have considered the axial loads
[00:02:45:750 - 00:02:46:160] **Speaker 1:** only.
[00:02:46:520 - 00:02:49:369] **Speaker 1:** What we're now going to consider is beam elements which
[00:02:49:369 - 00:02:51:580] **Speaker 1:** carry shear loads and moments.
[00:02:52:619 - 00:02:56:789] **Speaker 1:** Only And that's gonna be in the absence.
[00:02:58:600 - 00:03:02:479] **Speaker 1:** Of Any axial loads.
[00:03:05:320 - 00:03:07:800] **Speaker 1:** And then we'll come back and combine them a little
[00:03:07:800 - 00:03:08:279] **Speaker 1:** bit later.
[00:03:10:380 - 00:03:13:889] **Speaker 1:** So beam elements are defined by uh essentially simple thing.
[00:03:13:929 - 00:03:16:179] **Speaker 1:** We're going to make the same underlying assumptions and that
[00:03:16:460 - 00:03:19:460] **Speaker 1:** the elements carry a constant shear force, a constant have
[00:03:19:460 - 00:03:23:220] **Speaker 1:** a constant elastic modulus, constant cross section and a given
[00:03:23:220 - 00:03:23:570] **Speaker 1:** length.
[00:03:23:699 - 00:03:25:860] **Speaker 1:** So we're not going to look at varying sections.
[00:03:26:050 - 00:03:28:860] **Speaker 1:** Certainly, we could, and we could end up with an
[00:03:28:860 - 00:03:31:539] **Speaker 1:** element derivation that specifically looks to a particular varying cross
[00:03:31:539 - 00:03:32:000] **Speaker 1:** section.
[00:03:32:490 - 00:03:35:169] **Speaker 1:** But then that wouldn't be a a very generic element
[00:03:35:169 - 00:03:36:009] **Speaker 1:** that we could use elsewhere.
[00:03:36:050 - 00:03:38:330] **Speaker 1:** So we're gonna look at a prismatic bar with a
[00:03:38:330 - 00:03:41:490] **Speaker 1:** constant uh cross-sectional area, which means that it will have
[00:03:41:490 - 00:03:43:929] **Speaker 1:** a constant second moment of area I.
[00:03:44:570 - 00:03:47:369] **Speaker 1:** Um, we're gonna homogeneous bar with a constant elastic modulus
[00:03:47:369 - 00:03:48:350] **Speaker 1:** and a given length.
[00:03:49:820 - 00:03:51:699] **Speaker 1:** Now what we have here is this is going to
[00:03:51:699 - 00:03:52:460] **Speaker 1:** be node one.
[00:03:53:580 - 00:03:55:500] **Speaker 1:** And this is going to be node 2.
[00:03:56:699 - 00:03:58:820] **Speaker 1:** So X for the element always goes from node 1
[00:03:58:820 - 00:04:01:139] **Speaker 1:** towards node 2 in the exact same way that we
[00:04:01:139 - 00:04:02:220] **Speaker 1:** did with bars.
[00:04:04:059 - 00:04:05:940] **Speaker 1:** Now our numbering sequence is a little bit different here.
[00:04:06:369 - 00:04:08:440] **Speaker 1:** Um, we, we'll still go kind of X Y Z,
[00:04:08:979 - 00:04:12:020] **Speaker 1:** but remembering that the, the X deflection, the axial component
[00:04:12:020 - 00:04:12:860] **Speaker 1:** we're ignoring for now.
[00:04:12:979 - 00:04:15:660] **Speaker 1:** So there is no uh degree of freedom in the
[00:04:15:660 - 00:04:18:140] **Speaker 1:** X direction for a frame for a beam element.
[00:04:19:717 - 00:04:22:389] **Speaker 1:** So knowing that we're not going to ignore X, the
[00:04:22:389 - 00:04:24:558] **Speaker 1:** next thing we do is go to Y, which is
[00:04:24:558 - 00:04:26:878] **Speaker 1:** the the degree of freedom at node one that acts
[00:04:26:878 - 00:04:27:968] **Speaker 1:** in the Y direction.
[00:04:28:438 - 00:04:30:088] **Speaker 1:** And we're going to call that D1.
[00:04:30:639 - 00:04:31:808] **Speaker 1:** Then we go to the Z direction.
[00:04:32:039 - 00:04:35:859] **Speaker 1:** So Z is counterclockwise, and we're gonna call it D2
[00:04:35:959 - 00:04:39:329] **Speaker 1:** and at the end we'll go uh D3 and D4.
[00:04:39:558 - 00:04:41:809] **Speaker 1:** So Once we do these sort of elements, we can
[00:04:41:809 - 00:04:43:920] **Speaker 1:** assume that they're actually rigidly connected to each other and
[00:04:43:920 - 00:04:45:820] **Speaker 1:** rigidly connected to support points.
[00:04:46:089 - 00:04:48:829] **Speaker 1:** And there is the ability to transfer transfer bending moment
[00:04:48:829 - 00:04:49:869] **Speaker 1:** through those connections.
[00:04:51:420 - 00:04:53:420] **Speaker 1:** At the moment, there is no axial components, so these
[00:04:53:420 - 00:04:55:000] **Speaker 1:** are assumed to be axially rigid.
[00:04:56:529 - 00:05:00:690] **Speaker 1:** And one thing that's implicit to this is the concept
[00:05:00:690 - 00:05:03:369] **Speaker 1:** that the elements are formulated as slender.
[00:05:03:529 - 00:05:05:869] **Speaker 1:** So the, the length has to be much bigger than
[00:05:05:869 - 00:05:06:570] **Speaker 1:** A or B.
[00:05:06:649 - 00:05:07:989] **Speaker 1:** So if we quickly sketch that.
[00:05:09:429 - 00:05:11:570] **Speaker 1:** This is sort of the, the cross section here.
[00:05:13:109 - 00:05:14:649] **Speaker 1:** Go back off onto the page.
[00:05:16:589 - 00:05:19:290] **Speaker 1:** And then we've got some sort of link here.
[00:05:19:750 - 00:05:22:730] **Speaker 1:** That's not a variable cross-section, that's just disappearing back into
[00:05:22:730 - 00:05:23:470] **Speaker 1:** the page.
[00:05:23:589 - 00:05:26:410] **Speaker 1:** Well, whatever length it is, just the perspective.
[00:05:27:980 - 00:05:29:940] **Speaker 1:** We've got the width here, might be a.
[00:05:32:260 - 00:05:34:579] **Speaker 1:** And then we've got some height in that cross section
[00:05:34:579 - 00:05:34:959] **Speaker 1:** there.
[00:05:35:859 - 00:05:36:769] **Speaker 1:** Which is B.
[00:05:40:059 - 00:05:47:529] **Speaker 1:** So Generally, We'd say that L is greater than about
[00:05:47:869 - 00:05:49:369] **Speaker 1:** 5 to 10 times.
[00:05:51:000 - 00:05:51:950] **Speaker 1:** The dimension B?
[00:05:58:399 - 00:05:59:140] **Speaker 1:** Or larger.
[00:06:05:470 - 00:06:06:970] **Speaker 1:** Allows us to use.
[00:06:09:619 - 00:06:12:019] **Speaker 1:** The Euler Bernoulli beam bending theory.
[00:06:30:489 - 00:06:32:290] **Speaker 1:** Now, what is that theory and why is there that
[00:06:32:290 - 00:06:32:910] **Speaker 1:** restriction?
[00:06:34:380 - 00:06:38:100] **Speaker 1:** Well, if we were to have a cantilever beam like
[00:06:38:100 - 00:06:41:760] **Speaker 1:** this, And we would have a constant moment on the
[00:06:41:760 - 00:06:42:140] **Speaker 1:** end.
[00:06:43:970 - 00:06:45:750] **Speaker 1:** So we would have a moment like this.
[00:06:49:029 - 00:06:51:690] **Speaker 1:** Then the deflected shape is going to look.
[00:06:52:829 - 00:06:53:649] **Speaker 1:** A little bit.
[00:06:56:160 - 00:06:57:690] **Speaker 1:** So and it's going to curve around.
[00:07:03:440 - 00:07:04:200] **Speaker 1:** Like this.
[00:07:05:220 - 00:07:06:260] **Speaker 1:** There'll be some vertical deflection.
[00:07:06:299 - 00:07:08:100] **Speaker 1:** And the the idea there is that you're gonna have
[00:07:08:100 - 00:07:09:779] **Speaker 1:** plain sections remains plain.
[00:07:10:529 - 00:07:12:850] **Speaker 1:** And essentially you're gonna have these plain sections that exist
[00:07:12:850 - 00:07:13:290] **Speaker 1:** along the length.
[00:07:13:329 - 00:07:15:769] **Speaker 1:** And if you were to, in the case of pure
[00:07:15:769 - 00:07:19:290] **Speaker 1:** bending, if you were to trace those back, that trace
[00:07:19:290 - 00:07:21:059] **Speaker 1:** back to a single origin in here.
[00:07:21:170 - 00:07:29:380] **Speaker 1:** So, This here is kind of a Bending and curvature.
[00:07:31:640 - 00:07:34:480] **Speaker 1:** And that component is captured by the Oulo Bernoulli beam
[00:07:34:480 - 00:07:35:320] **Speaker 1:** bending theory.
[00:07:37:579 - 00:07:40:559] **Speaker 1:** On top of that, there is another component of deflection.
[00:07:43:730 - 00:07:46:190] **Speaker 1:** So suppose we have, uh, force P on here.
[00:07:47:630 - 00:07:50:390] **Speaker 1:** Then what we've got is actually say, uh, if you
[00:07:50:390 - 00:07:52:630] **Speaker 1:** sketch the undeflected position.
[00:07:56:140 - 00:07:57:630] **Speaker 1:** On top of that, we're going to have some sort
[00:07:57:630 - 00:08:03:720] **Speaker 1:** of Straight line equation here where this Is the sheer
[00:08:03:720 - 00:08:04:459] **Speaker 1:** component.
[00:08:07:029 - 00:08:09:230] **Speaker 1:** So in that sheer component, we're essentially gonna have vertical
[00:08:09:230 - 00:08:09:890] **Speaker 1:** lines here.
[00:08:19:179 - 00:08:21:089] **Speaker 1:** And this here is the sheer component.
[00:08:22:410 - 00:08:24:790] **Speaker 1:** And it's gonna be this kinda, um, instead of being,
[00:08:25:609 - 00:08:28:809] **Speaker 1:** um, plain sections which trace back to a a single
[00:08:28:809 - 00:08:31:589] **Speaker 1:** origin for pure curve, pure moment.
[00:08:33:270 - 00:08:37:849] **Speaker 1:** What we have here is that the Vertical lines remain
[00:08:37:989 - 00:08:38:830] **Speaker 1:** vertical.
[00:08:39:309 - 00:08:42:530] **Speaker 1:** They don't curve over and this is the basically the
[00:08:42:539 - 00:08:45:570] **Speaker 1:** the little subsections form little parallelograms.
[00:08:48:299 - 00:08:52:330] **Speaker 1:** And If the beam is slender.
[00:08:59:580 - 00:09:04:520] **Speaker 1:** Then Pending deflections dominate.
[00:09:14:280 - 00:09:16:359] **Speaker 1:** And shared deflections are negligible.
[00:09:29:419 - 00:09:31:820] **Speaker 1:** So what we're assuming here is that our beam is
[00:09:31:820 - 00:09:34:169] **Speaker 1:** slender enough that we can only consider these deflections and
[00:09:34:169 - 00:09:36:659] **Speaker 1:** we'll still get a reasonable approximation of the true deflection
[00:09:37:020 - 00:09:39:419] **Speaker 1:** and that these components aren't significant.
[00:09:39:539 - 00:09:44:369] **Speaker 1:** So if you've got a um An aspect ratio of
[00:09:44:369 - 00:09:48:000] **Speaker 1:** sort of 5 to 10 or greater, then probably neglecting
[00:09:48:000 - 00:09:49:880] **Speaker 1:** these is less than 1% error.
[00:09:49:960 - 00:09:51:840] **Speaker 1:** It's not going to make a meaningful difference and we
[00:09:51:840 - 00:09:54:080] **Speaker 1:** won't have any issues introduced by that.
[00:09:54:599 - 00:09:56:479] **Speaker 1:** However, if we have a short squat beam.
[00:09:57:570 - 00:09:59:070] **Speaker 1:** That maybe has an aspect ratio of 2.
[00:10:00:210 - 00:10:01:929] **Speaker 1:** Then this is going to be much smaller relative to
[00:10:01:929 - 00:10:04:669] **Speaker 1:** this and actually neglecting this component may be more significant.
[00:10:05:169 - 00:10:07:169] **Speaker 1:** So before the end of this 4 weeks, we'll come
[00:10:07:169 - 00:10:09:400] **Speaker 1:** back and look at what we can do, um, what,
[00:10:09:450 - 00:10:13:030] **Speaker 1:** what difference we can apply in the shared defamation case.
[00:10:14:309 - 00:10:16:229] **Speaker 1:** But for now, we're just gonna ignore that but and
[00:10:16:229 - 00:10:17:890] **Speaker 1:** we're going to apply the all overoi.
[00:10:19:309 - 00:10:20:330] **Speaker 1:** Bein bending theory.
[00:10:22:969 - 00:10:24:599] **Speaker 1:** So much like we did with bars, what we're gonna
[00:10:24:599 - 00:10:29:520] **Speaker 1:** do here is, um, do a little free body diagram.
[00:10:29:559 - 00:10:31:080] **Speaker 1:** So we're gonna take a little piece of the bar
[00:10:31:080 - 00:10:34:940] **Speaker 1:** here, basically break out some generic piece.
[00:10:36:349 - 00:10:38:590] **Speaker 1:** And we'll bring that down and do a a freebo
[00:10:38:590 - 00:10:39:250] **Speaker 1:** diagram.
[00:10:40:109 - 00:10:43:510] **Speaker 1:** So we assume that we have some um VF X,
[00:10:43:590 - 00:10:45:909] **Speaker 1:** which is the transverse detection at any point along the
[00:10:45:909 - 00:10:46:150] **Speaker 1:** beam.
[00:10:46:429 - 00:10:48:030] **Speaker 1:** So for axial loads, we use the term U of
[00:10:48:030 - 00:10:49:690] **Speaker 1:** X, now we're using VF X.
[00:10:50:760 - 00:10:54:349] **Speaker 1:** And we have some WXXX, which is the distributed shared
[00:10:54:349 - 00:10:55:179] **Speaker 1:** load intensity.
[00:10:56:169 - 00:10:58:380] **Speaker 1:** We've got a little everybody diagram of this little piece
[00:10:58:380 - 00:10:58:880] **Speaker 1:** of the beam.
[00:10:59:219 - 00:11:01:380] **Speaker 1:** We have a sheer force on the left, a sheer
[00:11:01:380 - 00:11:04:479] **Speaker 1:** force on the right, and we have uh a moment
[00:11:04:479 - 00:11:05:059] **Speaker 1:** on each side.
[00:11:05:140 - 00:11:07:359] **Speaker 1:** So it's M and M + DM and V and
[00:11:08:099 - 00:11:08:960] **Speaker 1:** V plus DV.
[00:11:10:919 - 00:11:12:849] **Speaker 1:** Now, if we want to, what we're gonna do is
[00:11:12:849 - 00:11:18:880] **Speaker 1:** to uh Moment equilibrium, moment and force equilibrium about this.
[00:11:18:960 - 00:11:20:909] **Speaker 1:** So this is the distributed share load intensity.
[00:11:22:359 - 00:11:24:299] **Speaker 1:** And if we want to work out the moment that
[00:11:24:309 - 00:11:27:460] **Speaker 1:** that creates, we can basically lump that into a single
[00:11:27:739 - 00:11:30:150] **Speaker 1:** force, which acts here.
[00:11:30:159 - 00:11:32:669] **Speaker 1:** So this here would be a force of W, the
[00:11:32:679 - 00:11:34:539] **Speaker 1:** the distributed sheer load intensity.
[00:11:35:219 - 00:11:37:359] **Speaker 1:** W times DX.
[00:11:38:770 - 00:11:40:729] **Speaker 1:** And they were like halfway along this little section.
[00:11:40:809 - 00:11:45:780] **Speaker 1:** So the distance across here will be DX over 2.
[00:11:56:270 - 00:11:59:429] **Speaker 1:** So what we wanna do now is we want to
[00:11:59:429 - 00:12:01:830] **Speaker 1:** do some force and moment equilibrium on that.
[00:12:04:979 - 00:12:07:130] **Speaker 1:** So the next page, the first thing we do is
[00:12:07:130 - 00:12:08:750] **Speaker 1:** look at vertical force equilibrium.
[00:12:09:520 - 00:12:11:309] **Speaker 1:** So if we refer back to this, we have, uh,
[00:12:11:590 - 00:12:13:609] **Speaker 1:** force of V upwards, we have a force of V
[00:12:13:609 - 00:12:15:049] **Speaker 1:** plus DV downwards.
[00:12:15:929 - 00:12:19:849] **Speaker 1:** And we can do um the vertical force equilibrium on
[00:12:19:849 - 00:12:20:590] **Speaker 1:** that little element.
[00:12:26:960 - 00:12:29:520] **Speaker 1:** So what that tells us, we have uh force V
[00:12:29:869 - 00:12:32:239] **Speaker 1:** upwards V minus DV downwards and then we have a
[00:12:32:239 - 00:12:37:309] **Speaker 1:** downward force of VDX of WDX which we can redefine
[00:12:37:309 - 00:12:38:059] **Speaker 1:** as this.
[00:12:38:599 - 00:12:43:539] **Speaker 1:** So The transverse.
[00:12:50:789 - 00:13:04:179] **Speaker 1:** Distributed load is equal to The rate of change.
[00:13:08:989 - 00:13:10:650] **Speaker 1:** Of internal sheer force.
[00:13:17:289 - 00:13:20:280] **Speaker 1:** So if we have a distributed axial, uh, distributed transverse
[00:13:20:280 - 00:13:22:650] **Speaker 1:** light acting on that, the sheer force will change along
[00:13:22:650 - 00:13:25:880] **Speaker 1:** the length and it will change, um, based upon this
[00:13:25:880 - 00:13:26:450] **Speaker 1:** equation.
[00:13:29:330 - 00:13:31:150] **Speaker 1:** We're gonna do a bending moment equilibrium.
[00:13:31:969 - 00:13:33:989] **Speaker 1:** And this is actually going to be done.
[00:13:35:950 - 00:13:36:969] **Speaker 1:** About the lifted.
[00:13:43:539 - 00:13:47:140] **Speaker 1:** Of the The little individual element.
[00:13:51:299 - 00:13:54:520] **Speaker 1:** So we're taking about the, the left-hand edge here.
[00:13:57:559 - 00:13:59:320] **Speaker 1:** And we're going to do moment equilibrium.
[00:14:01:559 - 00:14:05:330] **Speaker 1:** So we end up with a, uh, minus M, so
[00:14:05:330 - 00:14:06:080] **Speaker 1:** that's just the moment.
[00:14:06:200 - 00:14:09:520] **Speaker 1:** Then we have the, um, lumped force.
[00:14:09:700 - 00:14:12:869] **Speaker 1:** So that's W times the, with the little incremental element
[00:14:12:869 - 00:14:15:400] **Speaker 1:** DX times the distance of DX over 2.
[00:14:15:559 - 00:14:18:359] **Speaker 1:** Then we have, uh, sheer force V plus DV and
[00:14:18:359 - 00:14:20:520] **Speaker 1:** that is a distance of DX from the left-hand edge.
[00:14:20:599 - 00:14:22:760] **Speaker 1:** And then we have the minus M plus DM.
[00:14:23:570 - 00:14:24:969] **Speaker 1:** We can go through and sum that.
[00:14:25:289 - 00:14:27:849] **Speaker 1:** Um, and what you actually see here is there's a
[00:14:27:849 - 00:14:28:640] **Speaker 1:** couple of terms in here.
[00:14:28:719 - 00:14:30:909] **Speaker 1:** So we, once we we multiply that through, we end
[00:14:30:909 - 00:14:33:210] **Speaker 1:** with a DX squared here, and we end up with
[00:14:33:210 - 00:14:35:450] **Speaker 1:** a DV by DX.
[00:14:37:320 - 00:14:39:520] **Speaker 1:** So on the assumption that this is an a little
[00:14:39:520 - 00:14:41:580] **Speaker 1:** infinitesimally small element.
[00:14:42:630 - 00:14:44:630] **Speaker 1:** What we're going to assume is that the second order
[00:14:44:630 - 00:14:45:270] **Speaker 1:** terms are zero.
[00:14:45:390 - 00:14:49:820] **Speaker 1:** So if DX is small, and as DX gets smaller,
[00:14:50:229 - 00:14:52:809] **Speaker 1:** we expect DX squared to go to zero much faster.
[00:14:53:309 - 00:14:56:429] **Speaker 1:** And equally, if DX is small, then so too will
[00:14:56:429 - 00:14:57:010] **Speaker 1:** DV.
[00:14:57:789 - 00:15:00:830] **Speaker 1:** And when we multiply those together, they'll approach 0.
[00:15:02:469 - 00:15:09:479] **Speaker 1:** So what we're really doing here is we're assuming That
[00:15:09:809 - 00:15:11:070] **Speaker 1:** 2nd order terms.
[00:15:17:130 - 00:15:19:190] **Speaker 1:** Which is essentially a small number squared.
[00:15:28:640 - 00:15:30:659] **Speaker 1:** And that those terms can be neglected.
[00:15:37:869 - 00:15:39:570] **Speaker 1:** And that of course is linked.
[00:15:41:700 - 00:15:45:789] **Speaker 1:** 2 The small deflection assumption.
[00:15:58:169 - 00:15:59:690] **Speaker 1:** So it does put a limit on, we make that
[00:15:59:690 - 00:16:01:409] **Speaker 1:** assumption and makes the derivation easier.
[00:16:01:650 - 00:16:04:070] **Speaker 1:** It does put some limitations on our analysis.
[00:16:04:450 - 00:16:08:440] **Speaker 1:** It means that we have to basically assume, um, small
[00:16:08:440 - 00:16:09:020] **Speaker 1:** deflections.
[00:16:09:179 - 00:16:12:010] **Speaker 1:** Now, Essentially, that's already embedded in a lot of what
[00:16:12:010 - 00:16:13:049] **Speaker 1:** we're doing anyway.
[00:16:13:609 - 00:16:16:969] **Speaker 1:** We're assuming that the initial geometry is a fair approximation
[00:16:16:969 - 00:16:18:789] **Speaker 1:** of the deflective geometry.
[00:16:19:409 - 00:16:21:969] **Speaker 1:** And there's other things throughout this analysis where we're assuming
[00:16:22:210 - 00:16:22:849] **Speaker 1:** that's what deflection.
[00:16:22:929 - 00:16:24:570] **Speaker 1:** So it's not a new limitation.
[00:16:24:690 - 00:16:27:570] **Speaker 1:** It's a limitation that's essentially already embedded elsewhere through a
[00:16:27:570 - 00:16:28:489] **Speaker 1:** derivation anyway.
[00:16:28:609 - 00:16:33:450] **Speaker 1:** So it just makes the um Analysis a bit simpler.
[00:16:37:989 - 00:16:40:090] **Speaker 1:** The other thing, once we do that.
[00:16:41:479 - 00:16:44:039] **Speaker 1:** Then essentially this term goes to zero.
[00:16:44:349 - 00:16:46:200] **Speaker 1:** We're neglecting that, we're neglecting that.
[00:16:46:640 - 00:16:48:200] **Speaker 1:** So we're only actually left with two terms, which is
[00:16:48:200 - 00:16:51:520] **Speaker 1:** the minus VDX and DM and we can rewrite that
[00:16:51:520 - 00:16:52:679] **Speaker 1:** as this equation here.
[00:16:56:299 - 00:17:02:330] **Speaker 1:** And what that tells us is that the value Of
[00:17:02:330 - 00:17:03:270] **Speaker 1:** the sheer force.
[00:17:07:400 - 00:17:11:787] **Speaker 1:** is equal to The rate of change.
[00:17:16:298 - 00:17:17:399] **Speaker 1:** Off-bending moment.
[00:17:23:989 - 00:17:25:739] **Speaker 1:** And hopefully there's nothing too new to you.
[00:17:25:829 - 00:17:28:109] **Speaker 1:** If you remember back to last year with Paul Docherty,
[00:17:28:709 - 00:17:32:150] **Speaker 1:** uh, if you did do visual methods for generation of
[00:17:32:150 - 00:17:34:989] **Speaker 1:** sheer force and bending moment diagrams, you'll remember that the
[00:17:34:989 - 00:17:37:390] **Speaker 1:** slope or the value of a shear force diagram is
[00:17:37:390 - 00:17:40:030] **Speaker 1:** by definition, the slope of a bending moment diagram.
[00:17:40:750 - 00:17:42:930] **Speaker 1:** That's also essentially what this is saying.
[00:17:46:979 - 00:17:48:599] **Speaker 1:** Now also back from 202.
[00:17:49:260 - 00:17:51:979] **Speaker 1:** We know we have a good old friend, the moment
[00:17:51:979 - 00:17:52:859] **Speaker 1:** curvature equation.
[00:17:52:939 - 00:17:55:920] **Speaker 1:** So this is the M is equal to EI times
[00:17:55:920 - 00:17:59:890] **Speaker 1:** the second derivative of transverse section with respect to X.
[00:18:01:349 - 00:18:04:750] **Speaker 1:** So, um, the first derivative DV by the X is
[00:18:04:750 - 00:18:07:949] **Speaker 1:** actually the slope of the deflection and the derivative of
[00:18:07:949 - 00:18:09:189] **Speaker 1:** slope is curvature.
[00:18:09:390 - 00:18:11:949] **Speaker 1:** So that that quantity in there is curvature, which is
[00:18:11:949 - 00:18:13:969] **Speaker 1:** why we call this the moment curvature relationship.
[00:18:17:849 - 00:18:19:449] **Speaker 1:** So we can go through, we end up with this
[00:18:19:449 - 00:18:20:270] **Speaker 1:** equation here.
[00:18:21:770 - 00:18:22:869] **Speaker 1:** Where does that come from?
[00:18:23:369 - 00:18:26:650] **Speaker 1:** Well, we've taken this equation from above.
[00:18:26:829 - 00:18:27:949] **Speaker 1:** We've brought that down.
[00:18:29:540 - 00:18:31:800] **Speaker 1:** And we've brought that in here.
[00:18:32:589 - 00:18:39:979] **Speaker 1:** And then we've substituted um the Um, substituted in the
[00:18:39:979 - 00:18:40:920] **Speaker 1:** equation above.
[00:18:42:349 - 00:18:45:890] **Speaker 1:** So, um, that gives us this relationship here.
[00:18:47:520 - 00:18:52:189] **Speaker 1:** And then we, well, that's the um moment curvature equation
[00:18:52:189 - 00:18:54:839] **Speaker 1:** and then the, we're substituting that into the air and
[00:18:54:839 - 00:18:57:520] **Speaker 1:** then we're bringing that down and we're bringing those two
[00:18:57:520 - 00:18:59:479] **Speaker 1:** together down into this one.
[00:18:59:599 - 00:18:59:880] **Speaker 1:** So sorry.
[00:19:01:739 - 00:19:05:010] **Speaker 1:** Um, that's the, the derivative of the moment curvature equation
[00:19:05:010 - 00:19:07:089] **Speaker 1:** and then, um, this one.
[00:19:07:650 - 00:19:07:750] **Speaker 1:** Yeah.
[00:19:07:829 - 00:19:09:910] **Speaker 1:** So those together give us this equation.
[00:19:13:060 - 00:19:16:300] **Speaker 1:** So it's the relationship between the transverse distributed load that
[00:19:16:300 - 00:19:18:420] **Speaker 1:** acts on that member is the rate of change of
[00:19:18:420 - 00:19:22:390] **Speaker 1:** sheer force, which is the second derivative of the, uh,
[00:19:22:420 - 00:19:23:599] **Speaker 1:** moment curvature equation.
[00:19:28:430 - 00:19:31:349] **Speaker 1:** So as we did before with a bar, we're initially
[00:19:31:349 - 00:19:35:859] **Speaker 1:** going to assume that the externally uniformly distributed load that
[00:19:35:859 - 00:19:37:829] **Speaker 1:** X transverse along the element is zero.
[00:19:37:910 - 00:19:39:969] **Speaker 1:** So we're just going to put W X equals 0
[00:19:40:109 - 00:19:40:550] **Speaker 1:** for now.
[00:19:40:709 - 00:19:43:069] **Speaker 1:** Now, I will promise you before the end of next
[00:19:43:069 - 00:19:45:219] **Speaker 1:** week, we'll come back and we'll revisit what we do
[00:19:45:430 - 00:19:46:189] **Speaker 1:** with that's non-zero.
[00:19:46:310 - 00:19:49:109] **Speaker 1:** So it's not parking that indefinitely.
[00:19:49:310 - 00:19:51:170] **Speaker 1:** It's just putting it to the side for now.
[00:19:52:579 - 00:19:56:069] **Speaker 1:** So we're gonna make the simplifying assumption and then that
[00:19:56:069 - 00:19:59:079] **Speaker 1:** equation above the right-hand side, what is now the right-hand
[00:19:59:079 - 00:20:00:310] **Speaker 1:** side just becomes zero.
[00:20:06:680 - 00:20:09:119] **Speaker 1:** So much like we had some pretty simple shape functions
[00:20:09:119 - 00:20:11:910] **Speaker 1:** for axial, we had 1 minus 6 over L and
[00:20:11:910 - 00:20:12:469] **Speaker 1:** X over L.
[00:20:12:520 - 00:20:15:760] **Speaker 1:** So they were the relationship between the internal axial deflection
[00:20:15:760 - 00:20:18:119] **Speaker 1:** anywhere along an element related to the value at the
[00:20:18:119 - 00:20:19:020] **Speaker 1:** end points.
[00:20:19:719 - 00:20:21:280] **Speaker 1:** What we need to do now is come up with
[00:20:21:280 - 00:20:24:699] **Speaker 1:** an equivalent version for these bending deflections.
[00:20:28:709 - 00:20:33:270] **Speaker 1:** So, given elastic modulus cross-sectional area, and the four externally
[00:20:33:270 - 00:20:35:709] **Speaker 1:** applied forces, so the two sheer forces and two moments
[00:20:35:709 - 00:20:36:630] **Speaker 1:** that exist on it.
[00:20:37:579 - 00:20:41:380] **Speaker 1:** We need to find the the transverse deformation information, which
[00:20:41:380 - 00:20:42:060] **Speaker 1:** is V of X.
[00:20:42:219 - 00:20:44:140] **Speaker 1:** So remember, U of X is the axial in the
[00:20:44:140 - 00:20:47:369] **Speaker 1:** X direction and V of X is the transverse and
[00:20:47:369 - 00:20:48:500] **Speaker 1:** the Y direction.
[00:20:49:910 - 00:20:51:989] **Speaker 1:** And we need, so this is the, the diagram, this
[00:20:51:989 - 00:20:54:010] **Speaker 1:** is our numbering sequence, node 1 and node 2.
[00:20:54:939 - 00:20:56:880] **Speaker 1:** D1, D2, D3, D4.
[00:20:57:290 - 00:20:58:380] **Speaker 1:** That's Y Z Y Z.
[00:20:59:739 - 00:21:01:599] **Speaker 1:** And what we need to do is then we've got
[00:21:01:599 - 00:21:02:920] **Speaker 1:** our boundary conditions.
[00:21:03:380 - 00:21:07:459] **Speaker 1:** So, The first one here.
[00:21:09:260 - 00:21:15:479] **Speaker 1:** So EI Times the 3rd derivative of V with respect
[00:21:15:479 - 00:21:16:199] **Speaker 1:** to X.
[00:21:17:550 - 00:21:18:770] **Speaker 1:** is equal to sheer force.
[00:21:21:660 - 00:21:28:329] **Speaker 1:** So our Second derivative with respect to X, 2nd derivative
[00:21:28:329 - 00:21:31:209] **Speaker 1:** of the transverse section with respect to X is times
[00:21:31:209 - 00:21:32:339] **Speaker 1:** the I is a moment.
[00:21:33:300 - 00:21:35:599] **Speaker 1:** And the rate of change of moment is sheer force.
[00:21:37:349 - 00:21:39:229] **Speaker 1:** So when we take the sheer force equation and we
[00:21:39:229 - 00:21:41:130] **Speaker 1:** evaluate that it X equals 0.
[00:21:42:069 - 00:21:44:510] **Speaker 1:** We get the sheer force that exists at that node.
[00:21:46:410 - 00:21:48:270] **Speaker 1:** We can do the same thing here.
[00:21:49:949 - 00:21:52:510] **Speaker 1:** We take the same equation, which is, you know, something
[00:21:52:510 - 00:21:54:709] **Speaker 1:** that we've, we've already derived and hopefully it's familiar to
[00:21:54:709 - 00:21:55:849] **Speaker 1:** you from past years.
[00:21:56:530 - 00:21:58:290] **Speaker 1:** This here is the sheer force.
[00:22:00:339 - 00:22:01:209] **Speaker 1:** At node 2.
[00:22:02:089 - 00:22:05:050] **Speaker 1:** So we're just taking the 3rd derivative of transverse fiction
[00:22:05:050 - 00:22:07:890] **Speaker 1:** with respect to X times the I and we evaluate
[00:22:07:890 - 00:22:10:349] **Speaker 1:** that at um node.
[00:22:11:300 - 00:22:13:579] **Speaker 1:** At X equals L, which is that node 2, and
[00:22:13:579 - 00:22:15:069] **Speaker 1:** we get F3.
[00:22:21:760 - 00:22:23:359] **Speaker 1:** So, this one here.
[00:22:24:839 - 00:22:27:170] **Speaker 1:** That's our bending moment equation, our moment curvature equation.
[00:22:29:150 - 00:22:32:550] **Speaker 1:** So EI times the 2nd derivative of V with respect
[00:22:32:550 - 00:22:33:010] **Speaker 1:** to X.
[00:22:34:229 - 00:22:35:410] **Speaker 1:** As equal to moment.
[00:22:39:420 - 00:22:40:880] **Speaker 1:** I could spell that correctly.
[00:22:41:430 - 00:22:42:479] **Speaker 1:** It's a bending moment.
[00:22:44:219 - 00:22:45:920] **Speaker 1:** And then evaluated.
[00:22:50:089 - 00:22:52:310] **Speaker 1:** At X equals 0.
[00:22:53:270 - 00:22:55:359] **Speaker 1:** Gives F2.
[00:22:55:719 - 00:23:00:060] **Speaker 1:** So that's the applied external moment that exists at node
[00:23:00:060 - 00:23:00:349] **Speaker 1:** 2.
[00:23:02:020 - 00:23:04:119] **Speaker 1:** And then we have the same sort of approach here
[00:23:04:380 - 00:23:06:540] **Speaker 1:** and that's applied at node.
[00:23:07:020 - 00:23:09:739] **Speaker 1:** So there's a node 1 as if 2, and evaluated
[00:23:09:739 - 00:23:12:770] **Speaker 1:** X equals L means that node 2, which is the
[00:23:12:770 - 00:23:15:459] **Speaker 1:** F4, the rotation that exists there.
[00:23:16:250 - 00:23:17:800] **Speaker 1:** So that's our 4 boundary conditions.
[00:23:19:079 - 00:23:19:829] **Speaker 1:** This one here.
[00:23:21:849 - 00:23:29:140] **Speaker 1:** Pending moment Applied At node 2.
[00:23:34:050 - 00:23:36:589] **Speaker 1:** So we did touch on virtual displacements before.
[00:23:37:479 - 00:23:39:489] **Speaker 1:** The reason we went through that was because it does
[00:23:39:489 - 00:23:40:869] **Speaker 1:** form part of our derivations.
[00:23:42:560 - 00:23:45:839] **Speaker 1:** So we have here is the 2nd derivative with respect
[00:23:45:839 - 00:23:47:949] **Speaker 1:** to X of our moment curvature equation is equal to
[00:23:47:949 - 00:23:48:540] **Speaker 1:** 0.
[00:23:49:079 - 00:23:51:060] **Speaker 1:** That's the equation that we have above.
[00:23:52:310 - 00:23:55:319] **Speaker 1:** We're multiplying that by some little incremental virtual displacement DV.
[00:23:56:680 - 00:23:58:510] **Speaker 1:** And then we end up with this equation here.
[00:24:00:640 - 00:24:02:839] **Speaker 1:** So you start to see some very strong parallels with
[00:24:02:839 - 00:24:05:599] **Speaker 1:** how we went about solving this when we did this
[00:24:05:599 - 00:24:06:280] **Speaker 1:** for bars.
[00:24:08:979 - 00:24:11:020] **Speaker 1:** The difference this time is we actually have a higher
[00:24:11:020 - 00:24:12:050] **Speaker 1:** level of derivatives.
[00:24:12:140 - 00:24:14:619] **Speaker 1:** So last time we used the integration by parts once,
[00:24:14:819 - 00:24:16:359] **Speaker 1:** this time we're actually gonna have to use it twice.
[00:24:18:430 - 00:24:19:260] **Speaker 1:** So this is the equation.
[00:24:19:310 - 00:24:22:510] **Speaker 1:** We have different orders of integration in here and we
[00:24:22:510 - 00:24:23:380] **Speaker 1:** want to integrate the whole thing.
[00:24:23:510 - 00:24:26:989] **Speaker 1:** So we're using this definition here.
[00:24:27:310 - 00:24:29:310] **Speaker 1:** So we're defining G of X being a little virtual
[00:24:29:310 - 00:24:32:630] **Speaker 1:** displacement delta V and G of X is just the
[00:24:32:630 - 00:24:34:400] **Speaker 1:** derivative of that with respect to X.
[00:24:35:349 - 00:24:38:869] **Speaker 1:** HX is uh D by D X of us.
[00:24:38:949 - 00:24:40:630] **Speaker 1:** So that's this bracketed term.
[00:24:41:829 - 00:24:45:010] **Speaker 1:** And then the derivative of that is, so that's actually
[00:24:45:150 - 00:24:46:560] **Speaker 1:** HX there in the bracket.
[00:24:46:790 - 00:24:50:160] **Speaker 1:** And then the integral of that is one less derivative.
[00:24:50:550 - 00:24:52:430] **Speaker 1:** Um, so that's the, the H X there.
[00:24:54:290 - 00:24:56:319] **Speaker 1:** So essentially everything in this bracket here.
[00:24:58:020 - 00:25:00:280] **Speaker 1:** There's our H of X.
[00:25:01:969 - 00:25:07:150] **Speaker 1:** And This piece here is our GFX.
[00:25:09:469 - 00:25:11:060] **Speaker 1:** Now, I did mention this last time we did this,
[00:25:11:109 - 00:25:13:189] **Speaker 1:** but you know, you're probably more used to seeing the
[00:25:13:189 - 00:25:17:060] **Speaker 1:** integration by parts rules being UDV is integral as the
[00:25:17:069 - 00:25:20:150] **Speaker 1:** the integral of UDV is equal to the UV minus
[00:25:20:150 - 00:25:21:280] **Speaker 1:** the integral of VDU.
[00:25:22:069 - 00:25:23:750] **Speaker 1:** It's the same approach, but we're just using a different
[00:25:23:750 - 00:25:28:979] **Speaker 1:** notation because we're using U and V as our variables
[00:25:28:979 - 00:25:29:589] **Speaker 1:** for deflection.
[00:25:31:270 - 00:25:34:369] **Speaker 1:** We go through, we, we apply this rule with these
[00:25:34:420 - 00:25:37:839] **Speaker 1:** variables, substitute and work through that, um.
[00:25:39:189 - 00:25:41:150] **Speaker 1:** What we're doing in the first instance.
[00:25:41:469 - 00:25:45:780] **Speaker 1:** So we have, uh, EII times the 3rd derivative of
[00:25:46:500 - 00:25:49:619] **Speaker 1:** With respect to X here, evaluated X equals L.
[00:25:51:310 - 00:25:53:560] **Speaker 1:** That there is comes down from above.
[00:25:55:579 - 00:25:56:680] **Speaker 1:** Kind of comes into here.
[00:25:59:150 - 00:26:09:810] **Speaker 1:** And that's equal to Minus Um If 3 And then
[00:26:09:810 - 00:26:12:829] **Speaker 1:** the other one here, that's been brought down from above.
[00:26:14:829 - 00:26:17:790] **Speaker 1:** And it's being substituted into here.
[00:26:21:109 - 00:26:22:619] **Speaker 1:** So that there is.
[00:26:23:949 - 00:26:27:670] **Speaker 1:** If one So there has been a little bit like
[00:26:27:670 - 00:26:29:859] **Speaker 1:** the F1 comes across to here and the F3 comes
[00:26:29:859 - 00:26:32:530] **Speaker 1:** across to here, so they don't, they come across and,
[00:26:32:540 - 00:26:36:520] **Speaker 1:** uh, um, translating from one equation to the line below.
[00:26:38:189 - 00:26:39:829] **Speaker 1:** So that's got part of the way.
[00:26:40:189 - 00:26:40:989] **Speaker 1:** We're not quite there yet.
[00:26:41:069 - 00:26:44:390] **Speaker 1:** We still need to do, we still have differential levels
[00:26:44:390 - 00:26:44:969] **Speaker 1:** in here.
[00:26:45:390 - 00:26:47:949] **Speaker 1:** And we need to apply integration by parts a second
[00:26:47:949 - 00:26:48:369] **Speaker 1:** time.
[00:26:52:780 - 00:26:54:079] **Speaker 1:** So once we've done that.
[00:26:55:540 - 00:26:56:890] **Speaker 1:** Just give you a moment there for anyone that's still
[00:26:56:890 - 00:26:57:469] **Speaker 1:** copying.
[00:27:07:380 - 00:27:10:770] **Speaker 1:** So we go in and we apply our integration by
[00:27:10:770 - 00:27:11:810] **Speaker 1:** paths a second time.
[00:27:13:449 - 00:27:17:040] **Speaker 1:** Similar sort of approach, but now our G of X
[00:27:17:040 - 00:27:18:880] **Speaker 1:** and H2X are slightly different variables.
[00:27:19:219 - 00:27:20:859] **Speaker 1:** So it's not a direct repetition.
[00:27:20:900 - 00:27:22:280] **Speaker 1:** It's just applying the same process.
[00:27:24:060 - 00:27:26:239] **Speaker 1:** And then what we have in here.
[00:27:28:089 - 00:27:30:780] **Speaker 1:** This piece here, this is our moment curvature equation.
[00:27:31:770 - 00:27:34:030] **Speaker 1:** So this here is going to be.
[00:27:36:209 - 00:27:42:770] **Speaker 1:** The moment At node 2, it evaluated at X equals
[00:27:42:770 - 00:27:45:030] **Speaker 1:** L and that's going to be F4.
[00:27:47:140 - 00:27:48:270] **Speaker 1:** In this piece here.
[00:27:50:150 - 00:27:51:420] **Speaker 1:** Is the moment.
[00:27:54:050 - 00:27:54:949] **Speaker 1:** At note one.
[00:27:57:199 - 00:27:58:650] **Speaker 1:** Which is going to be 2.
[00:28:00:010 - 00:28:02:270] **Speaker 1:** Which is where they get substituted in below.
[00:28:02:849 - 00:28:05:170] **Speaker 1:** So we just work through the integration by parts.
[00:28:05:209 - 00:28:08:449] **Speaker 1:** We're substituting in our boundary conditions and then we end
[00:28:08:449 - 00:28:11:150] **Speaker 1:** up with this, um, integral here.
[00:28:14:489 - 00:28:16:290] **Speaker 1:** So when we did the bar, we did both the
[00:28:16:290 - 00:28:17:369] **Speaker 1:** strong form and the weak form.
[00:28:17:849 - 00:28:20:050] **Speaker 1:** The strong form had to be true for every point
[00:28:20:050 - 00:28:22:130] **Speaker 1:** of X and the weak form only had to be
[00:28:22:130 - 00:28:24:339] **Speaker 1:** true in terms of integrated terms across the element.
[00:28:25:130 - 00:28:27:189] **Speaker 1:** What we're doing here is again, applying the weak form.
[00:28:29:000 - 00:28:33:050] **Speaker 1:** We're using internal virtual work and we end up with
[00:28:33:319 - 00:28:38:520] **Speaker 1:** um incremental displacement, F1, the derivative that times F2, so
[00:28:38:520 - 00:28:39:579] **Speaker 1:** on through the equation.
[00:28:39:900 - 00:28:42:290] **Speaker 1:** And we can also group that like this.
[00:28:43:819 - 00:28:44:660] **Speaker 1:** And we're not there yet.
[00:28:44:859 - 00:28:47:020] **Speaker 1:** We're not, we've got something that's kind of getting close
[00:28:47:020 - 00:28:49:380] **Speaker 1:** to what we need, but we've still got some extra
[00:28:49:380 - 00:28:52:540] **Speaker 1:** things, extra steps we need to go through before we
[00:28:52:540 - 00:28:56:060] **Speaker 1:** can um quite get to the stiffness matrix that we
[00:28:56:060 - 00:28:56:280] **Speaker 1:** want.
[00:29:01:410 - 00:29:03:680] **Speaker 1:** So now, we're gonna assume that deflection anywhere along the
[00:29:03:680 - 00:29:04:060] **Speaker 1:** beam.
[00:29:04:869 - 00:29:08:030] **Speaker 1:** Can be calculated using a set of set of shape
[00:29:08:030 - 00:29:08:609] **Speaker 1:** functions.
[00:29:09:939 - 00:29:12:660] **Speaker 1:** Now, hopefully you're seeing the strong parallels between what we
[00:29:12:660 - 00:29:13:420] **Speaker 1:** did with bars.
[00:29:13:660 - 00:29:15:540] **Speaker 1:** So these shaped functions.
[00:29:21:520 - 00:29:26:229] **Speaker 1:** These were Our 5X.
[00:29:28:560 - 00:29:29:439] **Speaker 1:** For bars.
[00:29:30:910 - 00:29:32:930] **Speaker 1:** So this was the 1 minus X over L and
[00:29:32:930 - 00:29:33:430] **Speaker 1:** X over L.
[00:29:33:510 - 00:29:36:469] **Speaker 1:** So that was just a linear interpolation between the values
[00:29:36:469 - 00:29:37:209] **Speaker 1:** at two ends.
[00:29:37:630 - 00:29:39:949] **Speaker 1:** Um, now what we're gonna do is have our V
[00:29:39:949 - 00:29:40:619] **Speaker 1:** of X.
[00:29:41:750 - 00:29:42:869] **Speaker 1:** is equal to N.
[00:29:43:229 - 00:29:46:750] **Speaker 1:** So N is our shape functions as yet undefined, and
[00:29:46:750 - 00:29:48:109] **Speaker 1:** then D is a deflection vector.
[00:29:48:189 - 00:29:51:010] **Speaker 1:** So a deflection vector in local coordinates is now gonna
[00:29:51:010 - 00:29:54:069] **Speaker 1:** have 4 elements in it, not 2, because there's 4
[00:29:54:069 - 00:29:56:250] **Speaker 1:** degrees of freedom for a beam element as opposed to
[00:29:56:250 - 00:29:57:130] **Speaker 1:** 2 for a bar.
[00:29:58:410 - 00:30:01:180] **Speaker 1:** And we're gonna assume that our shape functions are some
[00:30:01:180 - 00:30:05:410] **Speaker 1:** as yet undetermined uh vector here with four individual shape
[00:30:05:410 - 00:30:06:699] **Speaker 1:** functions which sit within it.
[00:30:11:849 - 00:30:13:390] **Speaker 1:** So this here, 4.
[00:30:15:060 - 00:30:19:209] **Speaker 1:** Individual Shape function equations.
[00:30:31:650 - 00:30:33:640] **Speaker 1:** So what we're gonna do is we're gonna assume a
[00:30:33:640 - 00:30:34:660] **Speaker 1:** general form of these.
[00:30:34:839 - 00:30:37:160] **Speaker 1:** We don't yet know exactly what those shape functions look
[00:30:37:160 - 00:30:37:550] **Speaker 1:** like.
[00:30:38:000 - 00:30:39:920] **Speaker 1:** We're gonna assume a general form and then we're gonna
[00:30:39:920 - 00:30:43:000] **Speaker 1:** tailor those to our specific boundary conditions.
[00:30:44:589 - 00:30:46:109] **Speaker 1:** So this is the starting point we're going to use
[00:30:46:109 - 00:30:46:920] **Speaker 1:** for all 4.
[00:30:49:319 - 00:30:52:650] **Speaker 1:** So this is uh what we call Homerian polynomials.
[00:30:53:930 - 00:30:55:410] **Speaker 1:** And this is just a generic.
[00:30:57:550 - 00:31:02:930] **Speaker 1:** Third order A polynomial.
[00:31:10:770 - 00:31:13:670] **Speaker 1:** With as yet undefined.
[00:31:15:969 - 00:31:16:770] **Speaker 1:** Constance.
[00:31:27:719 - 00:31:29:800] **Speaker 1:** And what we're gonna do here is we're gonna apply
[00:31:30:150 - 00:31:31:319] **Speaker 1:** the unit deflection method.
[00:31:31:439 - 00:31:34:520] **Speaker 1:** So if I take a spring, like as a mathematical
[00:31:34:520 - 00:31:36:640] **Speaker 1:** construct, let's not worry about whether or not the spring
[00:31:36:640 - 00:31:39:599] **Speaker 1:** has the capacity to um deform by 1 metre.
[00:31:39:640 - 00:31:42:040] **Speaker 1:** But if I take a spring and I stretch that
[00:31:42:040 - 00:31:44:959] **Speaker 1:** by 1 metre, and it takes 800 Newtons to stretch
[00:31:44:959 - 00:31:47:119] **Speaker 1:** that, what's the stiffness of that spring?
[00:31:51:400 - 00:31:51:880] **Speaker 1:** Anyone?
[00:31:52:939 - 00:31:54:829] **Speaker 1:** 800 Newtons to stretch it by 1 metre.
[00:31:55:300 - 00:31:57:869] **Speaker 1:** If we were to express that stiffness in Newtons per
[00:31:57:869 - 00:31:58:189] **Speaker 1:** metre.
[00:32:01:040 - 00:32:01:729] **Speaker 1:** 800?
[00:32:02:050 - 00:32:03:290] **Speaker 1:** Yes, exactly right.
[00:32:03:369 - 00:32:07:290] **Speaker 1:** You're using a, a unit displacement such that the force
[00:32:07:290 - 00:32:11:250] **Speaker 1:** that's required to achieve that displacement is also by definition
[00:32:11:250 - 00:32:12:079] **Speaker 1:** of stiffness.
[00:32:14:180 - 00:32:17:439] **Speaker 1:** So it's quite a, just a, a helpful, uh, mathematical
[00:32:17:439 - 00:32:18:979] **Speaker 1:** construct of how we work through this.
[00:32:21:420 - 00:32:23:579] **Speaker 1:** So what it means A, B, C, and D are
[00:32:23:579 - 00:32:25:739] **Speaker 1:** found from the boundary conditions for each of the displaced
[00:32:26:380 - 00:32:30:579] **Speaker 1:** shape and These four constants.
[00:32:35:869 - 00:32:37:000] **Speaker 1:** will be different.
[00:32:41:719 - 00:32:42:609] **Speaker 1:** For its shape.
[00:32:50:410 - 00:32:51:369] **Speaker 1:** So we're gonna start with this.
[00:32:51:449 - 00:32:53:719] **Speaker 1:** We've got 4 equations here in 1 of X in
[00:32:53:719 - 00:32:55:229] **Speaker 1:** 2 of X, and 3 of X and in 4
[00:32:55:229 - 00:32:55:680] **Speaker 1:** X.
[00:32:56:170 - 00:32:58:739] **Speaker 1:** They're all going to start with the same generic polynomial,
[00:32:59:089 - 00:33:01:329] **Speaker 1:** but we're going to go through and evaluate the constants
[00:33:01:650 - 00:33:03:770] **Speaker 1:** based upon specific deflector shapes.
[00:33:05:530 - 00:33:07:250] **Speaker 1:** Now, the first question you're gonna say is, why, why
[00:33:07:250 - 00:33:09:109] **Speaker 1:** did you choose this as a starting point?
[00:33:10:589 - 00:33:11:449] **Speaker 1:** It's a good question.
[00:33:11:709 - 00:33:12:150] **Speaker 1:** Um.
[00:33:13:609 - 00:33:14:439] **Speaker 1:** You know, why a cubic?
[00:33:14:520 - 00:33:15:849] **Speaker 1:** Why not a polynomial?
[00:33:15:930 - 00:33:19:630] **Speaker 1:** Why not a, a quadratic, uh, well, fourth order, um.
[00:33:22:930 - 00:33:26:290] **Speaker 1:** Well, the first answer is you've only got 4 boundary
[00:33:26:290 - 00:33:26:489] **Speaker 1:** conditions.
[00:33:26:689 - 00:33:29:530] **Speaker 1:** So we only have the capacity to actually evaluate 4
[00:33:29:530 - 00:33:30:130] **Speaker 1:** constants.
[00:33:30:479 - 00:33:34:130] **Speaker 1:** So while a 5th order or a 6th order um
[00:33:34:130 - 00:33:38:359] **Speaker 1:** would enable us to capture more complex deflections.
[00:33:38:900 - 00:33:41:180] **Speaker 1:** We don't have the capacity to fit that level of
[00:33:41:180 - 00:33:44:099] **Speaker 1:** equation to an element with just turn to no points
[00:33:44:099 - 00:33:45:180] **Speaker 1:** and 4 boundary conditions.
[00:33:45:339 - 00:33:47:699] **Speaker 1:** So this is the most complex shape that we can
[00:33:47:699 - 00:33:49:319] **Speaker 1:** fit to this type of element.
[00:33:51:829 - 00:33:53:930] **Speaker 1:** Now, what we're gonna do is we're gonna work through
[00:33:55:270 - 00:33:57:660] **Speaker 1:** Go back to the free body diagram, what's actually repeated
[00:33:57:660 - 00:33:58:020] **Speaker 1:** here.
[00:33:59:209 - 00:34:01:780] **Speaker 1:** We have our defection D1, D2, D3, and D4.
[00:34:01:829 - 00:34:04:500] **Speaker 1:** So it's Y, Z, at node 1 and YZ at
[00:34:04:500 - 00:34:05:020] **Speaker 1:** node two.
[00:34:06:020 - 00:34:09:120] **Speaker 1:** We're going to systematically work through and set each of
[00:34:09:120 - 00:34:11:300] **Speaker 1:** those deflections to a unit value of one.
[00:34:12:148 - 00:34:13:870] **Speaker 1:** And in doing so, we're gonna keep all of the
[00:34:13:870 - 00:34:15:770] **Speaker 1:** other 3 equal to 0.
[00:34:19:070 - 00:34:22:229] **Speaker 1:** So in this case, D1, we've got a unit deflection
[00:34:22:229 - 00:34:25:530] **Speaker 1:** upwards that we maintain a zero slope because D2 is
[00:34:25:530 - 00:34:28:300] **Speaker 1:** 0 and D3 and D4 are kept to be zero.
[00:34:29:648 - 00:34:31:610] **Speaker 1:** Then what we do in the second case is we
[00:34:31:610 - 00:34:34:370] **Speaker 1:** put keep D1 being equal to 0, so there's no
[00:34:34:370 - 00:34:35:209] **Speaker 1:** displacement here.
[00:34:35:648 - 00:34:37:169] **Speaker 1:** But we enforce a unit.
[00:34:37:370 - 00:34:39:510] **Speaker 1:** So one radiance of of deflection.
[00:34:40:279 - 00:34:44:569] **Speaker 1:** At this nodal point while keeping D3 and D40.
[00:34:45:658 - 00:34:48:459] **Speaker 1:** Then what we're going to do is we'll um essentially
[00:34:48:459 - 00:34:49:459] **Speaker 1:** repeat this, but at the other end.
[00:34:49:580 - 00:34:52:449] **Speaker 1:** So we'll keep the deflection and slope 0 here.
[00:34:52:820 - 00:34:55:520] **Speaker 1:** We'll put a unit of deflection, but the zero slope.
[00:34:56:060 - 00:34:58:419] **Speaker 1:** And then finally here, we're going to put a a
[00:34:58:419 - 00:35:04:659] **Speaker 1:** unit deflection on the 4 with uh the deflection kept
[00:35:04:659 - 00:35:07:260] **Speaker 1:** to 0 and deflection slope kept to 0 at the
[00:35:07:260 - 00:35:07:600] **Speaker 1:** end.
[00:35:09:340 - 00:35:24:870] **Speaker 1:** So this is Systematically Work through And sit.
[00:35:26:760 - 00:35:28:469] **Speaker 1:** Each deflection component.
[00:35:34:239 - 00:35:36:820] **Speaker 1:** 20, 22, sorry, 21.
[00:35:40:320 - 00:35:41:760] **Speaker 1:** While keeping all others.
[00:35:47:159 - 00:35:47:889] **Speaker 1:** At 0.
[00:35:54:320 - 00:35:57:810] **Speaker 1:** And because we're using unit displacements, the force that we
[00:35:57:810 - 00:36:01:360] **Speaker 1:** obtain to achieve that displacement will be a stiffness too.
[00:36:06:469 - 00:36:09:709] **Speaker 1:** Now just a quick reminder here, we're using the, this
[00:36:09:709 - 00:36:11:709] **Speaker 1:** is X and this is Y.
[00:36:12:310 - 00:36:14:070] **Speaker 1:** So we're using the right-hand rule, so X, Y, and
[00:36:14:070 - 00:36:14:389] **Speaker 1:** Z.
[00:36:14:870 - 00:36:17:510] **Speaker 1:** And then for the the Z vector, we put our
[00:36:17:510 - 00:36:20:669] **Speaker 1:** right hand in that direction, which tells us that counterclockwise
[00:36:21:270 - 00:36:21:889] **Speaker 1:** is positive.
[00:36:22:159 - 00:36:23:850] **Speaker 1:** So it says Z for an element.
[00:36:25:850 - 00:36:29:649] **Speaker 1:** So counterclockwise is positive, which is why this one bends
[00:36:29:649 - 00:36:33:129] **Speaker 1:** upwards because it's counterclockwise rotation about this node and this
[00:36:33:129 - 00:36:37:370] **Speaker 1:** one bends downwards because that's also a counterclockwise rotation about
[00:36:37:370 - 00:36:38:090] **Speaker 1:** this node.
[00:36:49:790 - 00:36:51:389] **Speaker 1:** So we're gonna work through one of these 4 cases.
[00:36:51:429 - 00:36:52:750] **Speaker 1:** We're not going to work through all 4 of them
[00:36:52:750 - 00:36:55:030] **Speaker 1:** in full detail, um, because it is a bit of
[00:36:55:030 - 00:36:55:929] **Speaker 1:** a process.
[00:36:56:989 - 00:37:00:429] **Speaker 1:** But the exact same process, the exact same logic applies
[00:37:00:709 - 00:37:01:510] **Speaker 1:** to all four.
[00:37:07:129 - 00:37:12:139] **Speaker 1:** So We're gonna start with, you know, the second one.
[00:37:12:649 - 00:37:13:659] **Speaker 1:** This is as good a choice as any.
[00:37:14:729 - 00:37:16:919] **Speaker 1:** We're gonna look at the shape function representing D2 equal
[00:37:16:919 - 00:37:19:439] **Speaker 1:** to 1, which of course means D1, D3 and D4
[00:37:19:439 - 00:37:20:629] **Speaker 1:** are all equal to 0.
[00:37:21:040 - 00:37:22:409] **Speaker 1:** And this is the defective shape.
[00:37:25:270 - 00:37:28:159] **Speaker 1:** We're going to begin with our generic third order polynomial,
[00:37:28:510 - 00:37:30:830] **Speaker 1:** and we're going to apply the four boundary conditions which
[00:37:30:830 - 00:37:32:870] **Speaker 1:** get the which determine what A, B, and C should
[00:37:32:870 - 00:37:35:689] **Speaker 1:** be to capture the shape that's shown here.
[00:37:42:580 - 00:37:44:560] **Speaker 1:** So, this is.
[00:37:46:010 - 00:37:49:459] **Speaker 1:** Because we're considering the second defected shape, that's why we're
[00:37:49:459 - 00:37:50:500] **Speaker 1:** defining into.
[00:37:50:939 - 00:37:52:739] **Speaker 1:** So in one of X will be the first defected
[00:37:52:739 - 00:37:53:260] **Speaker 1:** shape.
[00:37:55:560 - 00:37:58:139] **Speaker 1:** The equation which captures the shape will be in one
[00:37:58:139 - 00:37:59:530] **Speaker 1:** of X shown there.
[00:37:59:979 - 00:38:02:040] **Speaker 1:** The fiction which captures this will be in 2 of
[00:38:02:040 - 00:38:02:659] **Speaker 1:** X.
[00:38:03:300 - 00:38:05:100] **Speaker 1:** That will be in 3 of X and then the
[00:38:05:100 - 00:38:07:320] **Speaker 1:** equation which captures this will be in 4 X.
[00:38:08:739 - 00:38:10:409] **Speaker 1:** We're doing the 2nd 1, which is why this is
[00:38:10:409 - 00:38:10:899] **Speaker 1:** in 2.
[00:38:12:639 - 00:38:14:169] **Speaker 1:** And these are our four boundary conditions.
[00:38:14:489 - 00:38:19:449] **Speaker 1:** So into evaluated X equals 0 is equal to D1,
[00:38:19:729 - 00:38:20:689] **Speaker 1:** which is equal to 0.
[00:38:22:879 - 00:38:23:620] **Speaker 1:** The derivative.
[00:38:25:399 - 00:38:29:770] **Speaker 1:** Of into with respect to X, it's the slope, evaluated
[00:38:29:770 - 00:38:30:709] **Speaker 1:** X equals 0.
[00:38:31:689 - 00:38:32:370] **Speaker 1:** is equal to one.
[00:38:32:409 - 00:38:33:469] **Speaker 1:** This is the slope.
[00:38:35:780 - 00:38:37:919] **Speaker 1:** At X equals 0.
[00:38:39:520 - 00:38:43:239] **Speaker 1:** This one here in 3 into evaluated at X equals
[00:38:43:239 - 00:38:43:590] **Speaker 1:** L.
[00:38:43:959 - 00:38:46:629] **Speaker 1:** That's going to be the transverse deflection at node 2,
[00:38:46:840 - 00:38:47:739] **Speaker 1:** which will be 0.
[00:38:48:280 - 00:38:52:320] **Speaker 1:** And then finally, uh, the derivative with respect to x
[00:38:52:320 - 00:38:54:189] **Speaker 1:** evaluated X equals LL.
[00:38:54:280 - 00:38:57:959] **Speaker 1:** So that's the slope evaluated at node 2 is D4,
[00:38:58:120 - 00:38:59:000] **Speaker 1:** which is equal to 0.
[00:38:59:080 - 00:39:02:959] **Speaker 1:** So these are And 4 boundary conditions.
[00:39:10:060 - 00:39:12:239] **Speaker 1:** So they're just derived from this deflected shape above.
[00:39:13:699 - 00:39:15:169] **Speaker 1:** And then we just need to work through there.
[00:39:16:979 - 00:39:20:810] **Speaker 1:** And systematically apply those four to get what the values
[00:39:20:810 - 00:39:22:250] **Speaker 1:** of A, B, C, and D are.
[00:39:23:320 - 00:39:26:679] **Speaker 1:** The first boundary condition will tell us that we substitute
[00:39:26:679 - 00:39:29:120] **Speaker 1:** X equals 0 into the equation, uh, knowing that it
[00:39:29:120 - 00:39:30:260] **Speaker 1:** has to be equal to 0.
[00:39:31:000 - 00:39:32:439] **Speaker 1:** That tells us that D equals 0.
[00:39:32:679 - 00:39:33:600] **Speaker 1:** That's nice and simple.
[00:39:34:739 - 00:39:37:659] **Speaker 1:** Then we take the 2nd boundary condition here, and we
[00:39:37:659 - 00:39:39:600] **Speaker 1:** substitute X equals 0 and.
[00:39:40:620 - 00:39:43:899] **Speaker 1:** And we get, get A times 0 and B times
[00:39:43:899 - 00:39:46:340] **Speaker 1:** 0 plus C equals 1.
[00:39:46:419 - 00:39:48:040] **Speaker 1:** So that tells us that C has to be 1.
[00:39:50:050 - 00:39:52:250] **Speaker 1:** The 3rd and 4th boundary conditions, because they're evaluated at
[00:39:52:250 - 00:39:56:629] **Speaker 1:** X equals L, they give us, um, They don't give
[00:39:56:629 - 00:39:58:379] **Speaker 1:** us directly A and B, but they give us two
[00:39:58:379 - 00:40:00:040] **Speaker 1:** equations for the two unknowns.
[00:40:00:550 - 00:40:02:790] **Speaker 1:** And when we go through and solve those, we can
[00:40:02:790 - 00:40:06:719] **Speaker 1:** see here what the value A and B will be.
[00:40:11:370 - 00:40:15:409] **Speaker 1:** Once we substitute A, B, C, and D back into
[00:40:15:409 - 00:40:17:370] **Speaker 1:** our initial generic.
[00:40:18:250 - 00:40:22:010] **Speaker 1:** Um 3rd order polynomial here.
[00:40:22:709 - 00:40:24:590] **Speaker 1:** This is the specific equation.
[00:40:25:899 - 00:40:32:679] **Speaker 1:** That we get here So In 2 of X.
[00:40:34:379 - 00:40:36:000] **Speaker 1:** Is the specific version.
[00:40:41:310 - 00:40:43:449] **Speaker 1:** Of a generic general.
[00:40:47:020 - 00:40:48:459] **Speaker 1:** Third order polynomial.
[00:40:58:969 - 00:41:00:149] **Speaker 1:** That captures.
[00:41:03:139 - 00:41:04:399] **Speaker 1:** The shape showing.
[00:41:06:820 - 00:41:08:300] **Speaker 1:** At the top of the page.
[00:41:14:770 - 00:41:16:310] **Speaker 1:** Now, as I've already said, we're not gonna go through
[00:41:16:310 - 00:41:17:939] **Speaker 1:** and do this 4 times.
[00:41:18:159 - 00:41:19:459] **Speaker 1:** It's the exact same approach.
[00:41:21:340 - 00:41:23:090] **Speaker 1:** But if we were to go through and do this
[00:41:23:090 - 00:41:26:489] **Speaker 1:** on each of those instances, we would end up with
[00:41:26:489 - 00:41:29:790] **Speaker 1:** the the 4 equations that are presented at the top
[00:41:30:250 - 00:41:31:409] **Speaker 1:** of page 69.
[00:41:35:590 - 00:41:39:709] **Speaker 1:** So it's just, yeah, those 4 shapes working through applying
[00:41:39:709 - 00:41:42:290] **Speaker 1:** the boundary conditions each time and evaluating the constants.
[00:41:42:989 - 00:41:47:030] **Speaker 1:** And in doing so, we get those 4 final answers.
[00:41:55:570 - 00:42:02:159] **Speaker 1:** So These are The 4 equations.
[00:42:06:600 - 00:42:14:709] **Speaker 1:** Which model The 4 Deflected shapes.
[00:42:25:979 - 00:42:29:340] **Speaker 1:** Showing On page 67.
[00:42:31:909 - 00:42:33:110] **Speaker 1:** So 2 pages prior.
[00:42:42:239 - 00:42:46:469] **Speaker 1:** So V X here, that is the transverse deflection at
[00:42:46:469 - 00:42:48:479] **Speaker 1:** any point X anywhere along the beam.
[00:42:50:530 - 00:42:53:530] **Speaker 1:** In as our picture of shape functions.
[00:42:59:629 - 00:43:04:500] **Speaker 1:** The victor Of the four shape functions.
[00:43:07:340 - 00:43:14:020] **Speaker 1:** Above And then our D is our deflection vector.
[00:43:14:169 - 00:43:14:919] **Speaker 1:** So these are our.
[00:43:16:540 - 00:43:20:469] **Speaker 1:** Solved Not all deflections for this element.
[00:43:23:300 - 00:43:25:679] **Speaker 1:** And then when we multiply that through, we essentially have
[00:43:25:679 - 00:43:28:810] **Speaker 1:** N1 through N4, D1 through D4.
[00:43:29:189 - 00:43:33:209] **Speaker 1:** And if we do the matrix multiplication, And remembering you
[00:43:33:209 - 00:43:35:370] **Speaker 1:** go across a row down a column, we get in
[00:43:35:370 - 00:43:38:260] **Speaker 1:** one of X times D1, N2 of X times D2,
[00:43:38:449 - 00:43:40:209] **Speaker 1:** in 3 of X times D3, and in 4 of
[00:43:40:209 - 00:43:41:110] **Speaker 1:** XD4.
[00:43:45:350 - 00:43:48:540] **Speaker 1:** So this is the equation that defines the transverse deflection
[00:43:49:300 - 00:43:53:189] **Speaker 1:** anywhere along the element based upon only the nodal deflections.
[00:43:53:459 - 00:43:55:449] **Speaker 1:** So these are incredibly powerful.
[00:43:56:189 - 00:43:57:989] **Speaker 1:** Once you've gone through and solved the problem, you have
[00:43:57:989 - 00:44:01:870] **Speaker 1:** only 4 pieces of information, which is the 4 deflections
[00:44:01:870 - 00:44:02:750] **Speaker 1:** of the nodes.
[00:44:03:149 - 00:44:05:580] **Speaker 1:** And from that, you can get this nice, beautiful curved
[00:44:05:580 - 00:44:08:790] **Speaker 1:** shape, which is a combination of the different loading mechanisms
[00:44:09:159 - 00:44:10:250] **Speaker 1:** that exist within that.
[00:44:14:429 - 00:44:16:550] **Speaker 1:** So the shape functions that arrived based upon the following
[00:44:16:550 - 00:44:18:850] **Speaker 1:** assumptions, so they are based on small motions.
[00:44:19:929 - 00:44:22:929] **Speaker 1:** But based on the Bernoi Euler beam bending theory, so
[00:44:22:929 - 00:44:25:199] **Speaker 1:** the aspect ratio must be greater than 5 to 10,
[00:44:25:610 - 00:44:29:290] **Speaker 1:** um, because we're not, uh, we're ignoring the sheer deformation
[00:44:29:290 - 00:44:30:409] **Speaker 1:** share components of deflection.
[00:44:30:570 - 00:44:33:370] **Speaker 1:** So this only models the, the curvature deflections, not the
[00:44:33:370 - 00:44:36:129] **Speaker 1:** sheer deflections, and that means it's not applicable to short
[00:44:36:129 - 00:44:37:169] **Speaker 1:** squad members.
[00:44:38:229 - 00:44:39:790] **Speaker 1:** In the situations where you do have a short squad
[00:44:39:790 - 00:44:42:250] **Speaker 1:** member, you can use the Timoshenko element, which is a
[00:44:42:250 - 00:44:44:439] **Speaker 1:** similar derivation, but it just has an extra few pieces
[00:44:44:439 - 00:44:45:860] **Speaker 1:** to it, and we'll cover that next week.
[00:44:46:949 - 00:44:49:629] **Speaker 1:** And then we have a transverse deflection of VFX which
[00:44:49:629 - 00:44:53:879] **Speaker 1:** can be weighted combinations of those four things.
[00:44:55:219 - 00:44:58:850] **Speaker 1:** So we've gone through and we've, what I've just done
[00:44:58:850 - 00:45:01:399] **Speaker 1:** now is taken those 4 equations that exist at the
[00:45:01:399 - 00:45:02:459] **Speaker 1:** top of the page there.
[00:45:03:800 - 00:45:04:659] **Speaker 1:** And plotted them.
[00:45:05:919 - 00:45:08:030] **Speaker 1:** So we've gone through and we've just basically saying, well,
[00:45:08:110 - 00:45:11:629] **Speaker 1:** D1 equals 1, D2 equals 1, D3 equals 1, D4
[00:45:11:629 - 00:45:15:550] **Speaker 1:** equals 1, systematically working through there, keeping all the other
[00:45:15:550 - 00:45:16:209] **Speaker 1:** 0.
[00:45:16:550 - 00:45:21:699] **Speaker 1:** And as you would expect, Those equations give the shapes
[00:45:21:699 - 00:45:22:760] **Speaker 1:** that we started out with.
[00:45:25:800 - 00:45:27:699] **Speaker 1:** But that also has some limitations.
[00:45:28:929 - 00:45:31:649] **Speaker 1:** It means that the deflected shape that can be modelled
[00:45:31:649 - 00:45:35:570] **Speaker 1:** by one single element can only be a weighted sum
[00:45:35:570 - 00:45:36:790] **Speaker 1:** of these four shapes.
[00:45:38:300 - 00:45:41:419] **Speaker 1:** No, there's no possibility for this element to capture more
[00:45:41:419 - 00:45:42:959] **Speaker 1:** complex deformations.
[00:45:45:899 - 00:45:47:899] **Speaker 1:** So on the next page, we've gone through and we've
[00:45:47:899 - 00:45:51:550] **Speaker 1:** just done, you know, a few random sort of, you
[00:45:51:550 - 00:45:53:379] **Speaker 1:** know, random choices of numbers.
[00:45:53:419 - 00:45:54:399] **Speaker 1:** I mean, these are big numbers, right?
[00:45:54:459 - 00:45:58:780] **Speaker 1:** Like 4 radians, um, but just to to show an
[00:45:58:780 - 00:45:59:800] **Speaker 1:** exaggerated response.
[00:46:00:919 - 00:46:03:919] **Speaker 1:** These are just some sort of arbitrarily chosen numbers and
[00:46:03:919 - 00:46:05:739] **Speaker 1:** the corresponding shapes that exist there.
[00:46:06:820 - 00:46:09:860] **Speaker 1:** So there's some, you know, reasonably complex deflected curves that
[00:46:09:860 - 00:46:12:409] **Speaker 1:** can be incorporated from these four values.
[00:46:12:860 - 00:46:14:199] **Speaker 1:** But this is sort of the limitation.
[00:46:14:379 - 00:46:16:439] **Speaker 1:** You know, we can't have some really complex shapes.
[00:46:24:770 - 00:46:27:229] **Speaker 1:** So, the question I have for you.
[00:46:29:189 - 00:46:33:219] **Speaker 1:** I Do you think it's possible?
[00:46:34:320 - 00:46:37:080] **Speaker 1:** For the beam element that we have derived to capture
[00:46:37:080 - 00:46:38:780] **Speaker 1:** the space profile given below.
[00:46:40:879 - 00:46:42:729] **Speaker 1:** A quick show of hands of people that think yes.
[00:46:44:719 - 00:46:46:189] **Speaker 1:** Quick show of hands to people who think no.
[00:46:47:330 - 00:46:48:489] **Speaker 1:** Nice, perfect.
[00:46:49:330 - 00:46:52:629] **Speaker 1:** So one single element that that shape cannot be obtained
[00:46:53:129 - 00:46:54:409] **Speaker 1:** by any weighted sum.
[00:46:55:540 - 00:46:56:830] **Speaker 1:** Of these four values here.
[00:46:57:100 - 00:46:58:080] **Speaker 1:** It's just not possible.
[00:47:00:300 - 00:47:04:610] **Speaker 1:** However, If we were to break this up, And so
[00:47:04:610 - 00:47:05:989] **Speaker 1:** this is the overall being we're trying to model, but
[00:47:05:989 - 00:47:07:530] **Speaker 1:** we're gonna break it up into individual elements.
[00:47:07:570 - 00:47:09:889] **Speaker 1:** We're just gonna basically put a nodal point all the
[00:47:09:889 - 00:47:10:860] **Speaker 1:** way along here.
[00:47:14:570 - 00:47:16:199] **Speaker 1:** Then what you'll find is if you look at those
[00:47:16:199 - 00:47:18:969] **Speaker 1:** individual shapes that exist between those dots.
[00:47:19:840 - 00:47:24:550] **Speaker 1:** Those shapes can be modelled based upon the force equations
[00:47:24:550 - 00:47:25:469] **Speaker 1:** that we've derived.
[00:47:28:989 - 00:47:31:459] **Speaker 1:** So the same thing here, if we were to break
[00:47:31:459 - 00:47:34:010] **Speaker 1:** this up, these elements will all work quite nicely.
[00:47:41:189 - 00:47:42:260] **Speaker 1:** So one element.
[00:47:47:590 - 00:47:49:020] **Speaker 1:** Cannot capture the shape.
[00:47:55:620 - 00:47:57:219] **Speaker 1:** But multiple elements can.
[00:48:08:840 - 00:48:12:020] **Speaker 1:** So one simple element, like the one we've just arrived.
[00:48:13:179 - 00:48:14:000] **Speaker 1:** would look like this.
[00:48:29:060 - 00:48:30:250] **Speaker 1:** So there's 2 nodes.
[00:48:32:469 - 00:48:33:429] **Speaker 1:** 4 degrees of freedom.
[00:48:35:820 - 00:48:36:439] **Speaker 1:** Per element.
[00:48:43:060 - 00:48:44:959] **Speaker 1:** And then we could look at a more complex element.
[00:48:55:429 - 00:48:57:260] **Speaker 1:** So in that case we may have.
[00:48:58:800 - 00:49:03:000] **Speaker 1:** An element here, we have a nodal point here, transverse
[00:49:03:000 - 00:49:03:459] **Speaker 1:** moment.
[00:49:05:070 - 00:49:08:030] **Speaker 1:** And the rotation, but we also put a nodal point
[00:49:08:030 - 00:49:08:449] **Speaker 1:** in the middle.
[00:49:10:469 - 00:49:11:969] **Speaker 1:** This would be 3 nodes per element.
[00:49:16:169 - 00:49:17:469] **Speaker 1:** And 6 degrees of freedom.
[00:49:19:100 - 00:49:19:790] **Speaker 1:** Per element.
[00:49:25:639 - 00:49:27:760] **Speaker 1:** Now, in this case, by having that extra nodal point,
[00:49:27:919 - 00:49:30:800] **Speaker 1:** we've essentially got an extra point, we can evaluate boundary
[00:49:30:800 - 00:49:31:340] **Speaker 1:** conditions.
[00:49:31:760 - 00:49:33:760] **Speaker 1:** We would be able to then have 6 degrees of
[00:49:33:760 - 00:49:34:219] **Speaker 1:** freedom.
[00:49:34:800 - 00:49:37:959] **Speaker 1:** We could then evaluate a 5th order polynomial based upon
[00:49:37:959 - 00:49:41:879] **Speaker 1:** those, um, you know, 6 constants, 6 boundary conditions, and
[00:49:41:879 - 00:49:44:100] **Speaker 1:** we'll be able to come to model some more complex
[00:49:44:100 - 00:49:44:139] **Speaker 1:** behaviour within that element.
[00:49:47:199 - 00:49:49:639] **Speaker 1:** That element's going to be more computationally expensive to operate
[00:49:49:639 - 00:49:51:419] **Speaker 1:** because it's got more information in it.
[00:49:52:040 - 00:49:54:870] **Speaker 1:** And the obvious question you might have is, well, why
[00:49:54:870 - 00:49:56:399] **Speaker 1:** don't we just break it into two elements and put
[00:49:56:399 - 00:49:58:120] **Speaker 1:** a nodal point there and have two simple elements?
[00:49:58:159 - 00:50:00:429] **Speaker 1:** And that's exactly the trade-off.
[00:50:00:639 - 00:50:03:399] **Speaker 1:** So with any fun element thing, there's always a trade-off
[00:50:03:399 - 00:50:07:159] **Speaker 1:** between using a larger number of more simple elements or
[00:50:07:159 - 00:50:10:689] **Speaker 1:** a smaller number of more complex elements and computationally, it
[00:50:10:689 - 00:50:11:580] **Speaker 1:** really makes no difference.
[00:50:12:000 - 00:50:15:139] **Speaker 1:** So We're not gonna go in and derive this, but
[00:50:15:429 - 00:50:16:750] **Speaker 1:** making you aware that that is an option.
[00:50:16:870 - 00:50:18:830] **Speaker 1:** We could go to a more complex element type or
[00:50:18:830 - 00:50:21:229] **Speaker 1:** just use more of the simple element that we've got.
[00:50:21:590 - 00:50:23:409] **Speaker 1:** So thank you all for coming along.
[00:50:24:239 - 00:50:25:409] **Speaker 1:** I'll see you again on Wednesday.
[00:50:25:780 - 00:50:27:870] **Speaker 1:** I did have a question um last week about putting
[00:50:27:870 - 00:50:29:719] **Speaker 1:** up the lab sheets earlier, so I'm just gonna do
[00:50:29:719 - 00:50:29:919] **Speaker 1:** that.
[00:50:30:639 - 00:50:32:959] **Speaker 1:** I'll put later today I'll put up the the information
[00:50:32:959 - 00:50:33:989] **Speaker 1:** about the lab on Thursday.
[00:50:34:320 - 00:50:36:760] **Speaker 1:** We haven't covered everything for that, so don't be alarmed
[00:50:36:760 - 00:50:38:379] **Speaker 1:** if you maybe it doesn't all make sense.
[00:50:38:679 - 00:50:40:280] **Speaker 1:** I'll put it up there for those that want to
[00:50:40:280 - 00:50:42:750] **Speaker 1:** start early, um, otherwise, you can look at it later
[00:50:42:750 - 00:50:43:120] **Speaker 1:** in the week.
[00:50:43:360 - 00:50:44:639] **Speaker 1:** So thank you all.
[00:50:50:860 - 00:50:50:879] **Speaker 1:** Thanks.
[00:51:27:919 - 00:51:27:939] **Speaker 0:** Thank you.
[00:51:36:439 - 00:51:42:879] **Speaker 0:** Yeah like like so nice to you.
[00:51:44:590 - 00:51:46:909] **Speaker 0:** We You listen to your old.
[00:51:49:169 - 00:51:49:179] **Speaker 0:** Yes.
[00:51:52:169 - 00:51:52:570] **Speaker 0:** I think.
[00:51:53:310 - 00:52:07:639] **Speaker 0:** It's like carry the Yeah You know exactly what I'm
[00:52:07:860 - 00:52:08:379] **Speaker 0:** talking about.
[00:52:09:050 - 00:52:09:070] **Speaker 0:** Thank you.
[00:52:09:080 - 00:52:10:899] **Speaker 0:** Oh, jumper.
[00:52:11:010 - 00:52:13:050] **Speaker 0:** Yes, far out, really?
[00:52:13:209 - 00:52:14:810] **Speaker 0:** I'm going to with my dad, but.
[00:52:20:520 - 00:53:07:310] **Speaker 0:** It I I guess a lot of I fire Sounds
[00:53:07:310 - 00:53:07:820] **Speaker 0:** like um.
[00:53:10:510 - 00:53:10:520] **Speaker 0:** Uh.
[00:53:16:100 - 00:53:16:110] **Speaker 0:** Sorry.
[00:53:18:810 - 00:53:21:469] **Speaker 0:** Oh, you do the one the over there.
[00:53:22:669 - 00:53:22:679] **Speaker 0:** Yeah.
[00:53:27:590 - 00:53:27:600] **Speaker 0:** I

# ENME302-26S2 Lecture 12 native Echo transcript

Date: July 31, 2026 11:00am-11:55am
Transcript type: native Echo automated transcript.

[00:00:09:369 - 00:00:52:360] **Speaker 0:** It I Well, Karakuto, welcome along, everyone.
[00:00:54:909 - 00:00:55:729] **Speaker 0:** Try and get into.
[00:01:02:560 - 00:01:03:740] **Speaker 0:** We'll try and get into things.
[00:01:14:260 - 00:01:15:279] **Speaker 1:** OK, thank you everyone.
[00:01:15:419 - 00:01:17:500] **Speaker 1:** So, um, what I wanna do is cover a couple
[00:01:17:500 - 00:01:18:620] **Speaker 1:** of final things about the examples.
[00:01:18:739 - 00:01:20:419] **Speaker 1:** So this is the example that we worked through yesterday
[00:01:20:419 - 00:01:20:680] **Speaker 1:** morning.
[00:01:22:269 - 00:01:26:379] **Speaker 1:** And it was also the same example that um We
[00:01:26:379 - 00:01:30:139] **Speaker 1:** worked through in the lab yesterday, so, um, 22 element
[00:01:30:139 - 00:01:32:660] **Speaker 1:** frame structures concentrated moment in the left hand corner, and
[00:01:32:660 - 00:01:36:660] **Speaker 1:** this was the overall uh element reaction forces that existed
[00:01:36:660 - 00:01:37:190] **Speaker 1:** from that.
[00:01:37:610 - 00:01:39:540] **Speaker 1:** Um, we looked in here and one of the things
[00:01:39:540 - 00:01:41:699] **Speaker 1:** we looked at was that the, the moment terms don't
[00:01:41:699 - 00:01:43:580] **Speaker 1:** necessarily have to be equal, um, the element does have
[00:01:43:580 - 00:01:46:500] **Speaker 1:** to be in static equilibrium, but in the and if
[00:01:46:500 - 00:01:48:569] **Speaker 1:** you uh had an element that's not carrying a share
[00:01:48:569 - 00:01:50:160] **Speaker 1:** then the moment terms will have to be equal.
[00:01:50:569 - 00:01:53:809] **Speaker 1:** Um, but the, if there is a sheer force, that
[00:01:53:809 - 00:01:56:410] **Speaker 1:** doesn't necessarily mean that the, the moment terms need to
[00:01:56:410 - 00:01:58:650] **Speaker 1:** be equal and opposite for the elements to be an
[00:01:58:650 - 00:01:59:309] **Speaker 1:** equilibrium.
[00:02:01:360 - 00:02:03:440] **Speaker 1:** So we'll work through a um a few more details
[00:02:03:440 - 00:02:05:800] **Speaker 1:** on this and then uh um a couple of final
[00:02:05:800 - 00:02:09:039] **Speaker 1:** examples on frame elements and then we'll return um and
[00:02:09:039 - 00:02:10:600] **Speaker 1:** look at distributed loading.
[00:02:12:429 - 00:02:14:940] **Speaker 1:** So this was the overall structure, the previous page, this
[00:02:14:940 - 00:02:18:190] **Speaker 1:** is actually page 89 of the notes, um, on the
[00:02:18:190 - 00:02:19:830] **Speaker 1:** previous page we had.
[00:02:20:949 - 00:02:26:190] **Speaker 1:** Um The Uh, elements individually and what we've done here
[00:02:26:190 - 00:02:27:839] **Speaker 1:** is we just sort of join them up onto the
[00:02:27:839 - 00:02:30:679] **Speaker 1:** structure and we're summoning the forces at these nodal points
[00:02:30:679 - 00:02:32:039] **Speaker 1:** to show the reaction loads.
[00:02:32:910 - 00:02:36:389] **Speaker 1:** This is a prime example of where the um global
[00:02:36:389 - 00:02:38:850] **Speaker 1:** coordinates work well and we've got multiple elements framing in
[00:02:38:850 - 00:02:40:589] **Speaker 1:** and we can just add the components up in the
[00:02:40:589 - 00:02:42:630] **Speaker 1:** global X, global Y, and global Z direction.
[00:02:43:669 - 00:02:46:419] **Speaker 1:** Now, we can just do a quick uh global equilibrium
[00:02:46:419 - 00:02:47:089] **Speaker 1:** of the structure.
[00:02:48:839 - 00:02:51:600] **Speaker 1:** So that each element within the structure must be an
[00:02:51:600 - 00:02:52:190] **Speaker 1:** equilibrium.
[00:02:52:979 - 00:02:57:479] **Speaker 1:** And we would expect Every um element to be in
[00:02:57:479 - 00:03:00:399] **Speaker 1:** equilibrium as well as the overall structure to be in
[00:03:00:399 - 00:03:01:339] **Speaker 1:** static equilibrium.
[00:03:01:559 - 00:03:04:520] **Speaker 1:** So while this does extend quite nicely into dynamics, we're
[00:03:04:520 - 00:03:06:460] **Speaker 1:** not doing dynamics here, so.
[00:03:07:509 - 00:03:11:330] **Speaker 1:** We can say some of forces in the XG direction,
[00:03:11:750 - 00:03:12:550] **Speaker 1:** sum to zero.
[00:03:13:570 - 00:03:16:460] **Speaker 1:** And we're just gonna say to the right it's positive,
[00:03:16:580 - 00:03:18:360] **Speaker 1:** so in a positive XG direction.
[00:03:20:330 - 00:03:25:520] **Speaker 1:** So here we have a 2.7097 kilonewton load and back
[00:03:25:520 - 00:03:27:220] **Speaker 1:** to the right, so it's positive.
[00:03:28:179 - 00:03:31:300] **Speaker 1:** Then we have um two internal forces here but they
[00:03:31:300 - 00:03:33:000] **Speaker 1:** actually sum up to a total of 0.
[00:03:33:539 - 00:03:35:960] **Speaker 1:** So we actually sum on 0, which is the total
[00:03:36:339 - 00:03:37:940] **Speaker 1:** uh external force at this node.
[00:03:38:619 - 00:03:40:270] **Speaker 1:** Which we would expect too because of the fact that
[00:03:40:270 - 00:03:42:750] **Speaker 1:** it's a roller, the support's not capable of providing a
[00:03:42:750 - 00:03:43:570] **Speaker 1:** horizontal reaction.
[00:03:44:190 - 00:03:45:990] **Speaker 1:** So if we got a non-zero value here, we know
[00:03:45:990 - 00:03:46:649] **Speaker 1:** that something's wrong.
[00:03:48:210 - 00:03:54:770] **Speaker 1:** Then we have this -2.7097. sums to 0 kilomewtons.
[00:03:54:850 - 00:03:58:110] **Speaker 1:** So we've got horizontal equilibrium for the overall structure.
[00:04:00:580 - 00:04:03:820] **Speaker 1:** We can also sum up the forces in the YG.
[00:04:04:610 - 00:04:05:130] **Speaker 1:** Direction.
[00:04:05:899 - 00:04:08:610] **Speaker 1:** And we say that upwards is positive.
[00:04:10:899 - 00:04:13:800] **Speaker 1:** So here we have 0 onions.
[00:04:14:759 - 00:04:22:338] **Speaker 1:** At this end here, we have 9.4839 kilonewtons, and then
[00:04:22:338 - 00:04:27:919] **Speaker 1:** here we have minus 9.4839 kilonewtons, which of course sums
[00:04:27:919 - 00:04:28:398] **Speaker 1:** to zero.
[00:04:31:010 - 00:04:32:799] **Speaker 1:** What we can define here is we're gonna maybe call
[00:04:32:799 - 00:04:34:209] **Speaker 1:** this bottom left hand corner A.
[00:04:35:600 - 00:04:38:019] **Speaker 1:** And well some moments about a.
[00:04:39:269 - 00:04:41:489] **Speaker 1:** And we'll determine that counterclockwise is positive.
[00:04:43:619 - 00:04:45:570] **Speaker 1:** So we have a shared force here.
[00:04:46:630 - 00:04:50:130] **Speaker 1:** The length, the perpendicular distance between the line of action
[00:04:50:410 - 00:04:54:290] **Speaker 1:** of this force and the point we're considering, considering about
[00:04:54:549 - 00:04:57:890] **Speaker 1:** is 10 metres and, This force acts to the right,
[00:04:58:079 - 00:05:00:059] **Speaker 1:** which will be a clockwise moment about this point.
[00:05:01:040 - 00:05:02:040] **Speaker 1:** So it will be negative.
[00:05:02:359 - 00:05:08:959] **Speaker 1:** So we have -2.7097. Times the distance of 10.
[00:05:10:920 - 00:05:13:279] **Speaker 1:** Um, there's 0 Newtons here.
[00:05:14:209 - 00:05:16:089] **Speaker 1:** Uh, but even if it wasn't on zero, there's no
[00:05:16:089 - 00:05:16:929] **Speaker 1:** perpendicular distance.
[00:05:16:970 - 00:05:20:010] **Speaker 1:** It's like that acts through point A, there's no moment
[00:05:20:010 - 00:05:20:750] **Speaker 1:** from that.
[00:05:21:369 - 00:05:23:850] **Speaker 1:** Uh, we do have this clockwise moment, so we're gonna
[00:05:23:850 - 00:05:27:869] **Speaker 1:** take off 18.0645.
[00:05:28:290 - 00:05:30:510] **Speaker 1:** It's a clockwise moment at the top.
[00:05:33:399 - 00:05:36:220] **Speaker 1:** We have a 140 kilometre.
[00:05:38:299 - 00:05:42:029] **Speaker 1:** Counterclockwise moment there, so we'll say 140 on there.
[00:05:43:239 - 00:05:45:559] **Speaker 1:** And then we have, um, there is a force here
[00:05:45:559 - 00:05:47:209] **Speaker 1:** that has no perpendicular distance.
[00:05:47:739 - 00:05:49:709] **Speaker 1:** Uh, there's 0 kilometres here because of the fact that
[00:05:49:709 - 00:05:50:339] **Speaker 1:** it's a pin.
[00:05:51:079 - 00:05:54:040] **Speaker 1:** There's a horizontal force, but that has no moment because
[00:05:54:040 - 00:05:57:700] **Speaker 1:** it's through a, but we do have this force here.
[00:05:58:950 - 00:06:02:029] **Speaker 1:** That's gonna produce a clockwise moment about A, so it'll
[00:06:02:029 - 00:06:04:730] **Speaker 1:** be a negative moment, which is 9.48.
[00:06:05:609 - 00:06:09:010] **Speaker 1:** 39 Times the perpendicular distance of 10.
[00:06:10:510 - 00:06:13:600] **Speaker 1:** Which then when you sum that up, um, the numbers
[00:06:13:600 - 00:06:17:420] **Speaker 1:** as they presented they come out to 0.0175.
[00:06:18:420 - 00:06:21:250] **Speaker 1:** Phil Newton metres, which of course is a rounding error.
[00:06:22:799 - 00:06:25:600] **Speaker 1:** And if we were to do that calculation internally within
[00:06:25:600 - 00:06:29:119] **Speaker 1:** the Python environment and not sort of, sort of not
[00:06:29:119 - 00:06:31:320] **Speaker 1:** certain number of significant figures presented here, we'd get something
[00:06:31:320 - 00:06:32:440] **Speaker 1:** as much closer to 0.
[00:06:34:709 - 00:06:39:540] **Speaker 1:** So Hopefully that just gives you confidence that, As well
[00:06:39:540 - 00:06:43:299] **Speaker 1:** as every individual element being in equilibrium here, the overall
[00:06:43:299 - 00:06:45:720] **Speaker 1:** structure is also in global equilibrium.
[00:06:48:239 - 00:06:50:420] **Speaker 1:** Now, there's one quite interesting thing to look at here
[00:06:50:920 - 00:06:51:739] **Speaker 1:** is that we had.
[00:06:52:709 - 00:06:54:940] **Speaker 1:** A 140 kilometre load here.
[00:07:00:790 - 00:07:03:920] **Speaker 1:** This is what we can see here is the 114,
[00:07:04:179 - 00:07:07:609] **Speaker 1:** 45.16 and the 94.83.
[00:07:12:339 - 00:07:16:559] **Speaker 1:** The split between Elements one.
[00:07:18:910 - 00:07:36:429] **Speaker 1:** And 2, Depends upon Their relative Flex or stiffness.
[00:07:45:480 - 00:07:54:489] **Speaker 1:** We can see How The 140 Killing you made a.
[00:07:56:519 - 00:08:02:079] **Speaker 1:** Concentrated External moment or externally applied moment.
[00:08:09:910 - 00:08:19:380] **Speaker 1:** gets distributed Amongst the elements.
[00:08:24:140 - 00:08:25:880] **Speaker 1:** Now an obvious question here might be.
[00:08:26:700 - 00:08:28:579] **Speaker 1:** We know that they have the same length, the same
[00:08:28:579 - 00:08:31:910] **Speaker 1:** elastic modulus, the same, uh, I value, the same second
[00:08:31:910 - 00:08:32:700] **Speaker 1:** moment of area.
[00:08:33:219 - 00:08:37:409] **Speaker 1:** So why is it that the split of moments, you
[00:08:37:409 - 00:08:42:580] **Speaker 1:** know, 140 kilonewton metres, given that the second modulus, the
[00:08:42:580 - 00:08:45:580] **Speaker 1:** EI A and L, all of those elements are both
[00:08:45:580 - 00:08:48:020] **Speaker 1:** the same, why is one carrying a greater share of
[00:08:48:020 - 00:08:48:460] **Speaker 1:** the load?
[00:08:49:869 - 00:08:52:070] **Speaker 1:** Well, it comes simply down to the fact that they
[00:08:52:070 - 00:08:53:070] **Speaker 1:** have different end conditions.
[00:08:53:150 - 00:08:55:909] **Speaker 1:** So this is fully clamped and this is pinned.
[00:08:56:270 - 00:08:59:109] **Speaker 1:** So what we see is that actually because this is
[00:08:59:109 - 00:09:03:000] **Speaker 1:** fully, even though the element itself has the same geometric
[00:09:03:000 - 00:09:05:799] **Speaker 1:** and material properties, because there's greater fixation here at the
[00:09:05:799 - 00:09:08:250] **Speaker 1:** top than there is at the right hand side, then
[00:09:08:369 - 00:09:12:859] **Speaker 1:** the vertical element element one, overall is more stiff because
[00:09:12:859 - 00:09:14:369] **Speaker 1:** it's constrained more strongly.
[00:09:14:789 - 00:09:17:359] **Speaker 1:** Therefore, it attracts a slightly bigger percentage of the load.
[00:09:20:320 - 00:09:22:559] **Speaker 1:** Um, what we could do here is you could just
[00:09:22:559 - 00:09:25:390] **Speaker 1:** go through and you could play with the, the relative
[00:09:25:390 - 00:09:25:919] **Speaker 1:** I values.
[00:09:26:080 - 00:09:28:000] **Speaker 1:** So if you, um, went back into your code and
[00:09:28:000 - 00:09:30:460] **Speaker 1:** you changed the I value for element two to maybe
[00:09:30:460 - 00:09:33:159] **Speaker 1:** one quarter of the nominal value, you should see that
[00:09:33:159 - 00:09:35:719] **Speaker 1:** it attracts a lot less at the moment and a
[00:09:35:719 - 00:09:36:809] **Speaker 1:** lot more goes into here.
[00:09:37:229 - 00:09:40:590] **Speaker 1:** So, um, we have this term and this term from
[00:09:40:590 - 00:09:41:179] **Speaker 1:** last year.
[00:09:41:559 - 00:09:44:869] **Speaker 1:** That's your statically indeterminate system, so a system that's not
[00:09:44:869 - 00:09:47:010] **Speaker 1:** able to be solved from statics alone, that you actually
[00:09:47:010 - 00:09:50:400] **Speaker 1:** have to start looking at constitutive relationships and relative stiffness
[00:09:50:400 - 00:09:51:020] **Speaker 1:** of members.
[00:09:52:510 - 00:09:57:190] **Speaker 1:** This is very much an overdefined or overconstrained system where
[00:09:57:190 - 00:09:59:429] **Speaker 1:** there's more restraint than is necessary for the structure to
[00:09:59:429 - 00:09:59:969] **Speaker 1:** be stable.
[00:10:00:669 - 00:10:02:950] **Speaker 1:** That means it's, it is stack indeterminant and you have
[00:10:02:950 - 00:10:05:030] **Speaker 1:** to draw in those relative stiffness to to solve the
[00:10:05:030 - 00:10:08:020] **Speaker 1:** problems, but the finite element system does all that for
[00:10:08:020 - 00:10:08:250] **Speaker 1:** you.
[00:10:09:130 - 00:10:11:869] **Speaker 1:** There's no manual intervention, it just comes out.
[00:10:13:429 - 00:10:15:669] **Speaker 1:** So what you could do here, as I mentioned, is
[00:10:15:669 - 00:10:16:570] **Speaker 1:** just increase.
[00:10:17:890 - 00:10:27:020] **Speaker 0:** The I value 4 Either Element one.
[00:10:28:700 - 00:10:39:200] **Speaker 1:** Well Alan, so And see How the load So that's
[00:10:39:200 - 00:10:40:169] **Speaker 1:** the applied moment.
[00:10:45:039 - 00:10:46:359] **Speaker 1:** It's redistributed.
[00:10:52:190 - 00:10:53:070] **Speaker 1:** Within the structure.
[00:11:01:849 - 00:11:02:140] **Speaker 1:** previous page.
[00:11:05:239 - 00:11:06:679] **Speaker 0:** like the Right.
[00:11:11:260 - 00:11:11:270] **Speaker 0:** Right.
[00:11:13:440 - 00:11:15:650] **Speaker 1:** Yep, so you've actually got that, so um.
[00:11:16:669 - 00:11:17:679] **Speaker 1:** The rationale for that.
[00:11:18:890 - 00:11:20:849] **Speaker 1:** So these are different splits, um.
[00:11:22:919 - 00:11:24:330] **Speaker 1:** Ah, actually, yes, that's a good point.
[00:11:24:400 - 00:11:25:590] **Speaker 1:** I've, I've misinterpreted that.
[00:11:25:650 - 00:11:28:200] **Speaker 1:** Let's have a, the reason for that, um, doesn't make
[00:11:28:200 - 00:11:28:659] **Speaker 1:** sense.
[00:11:29:859 - 00:11:33:010] **Speaker 1:** So, um, it's a little bit like the Euler-buckling equation.
[00:11:33:059 - 00:11:34:969] **Speaker 1:** If we go back, we're actually gonna skip forward a
[00:11:34:969 - 00:11:35:859] **Speaker 1:** few pages to explain that.
[00:11:35:940 - 00:11:38:940] **Speaker 1:** I maybe scratch what I said before, I got myself
[00:11:38:940 - 00:11:43:210] **Speaker 1:** in a, a mess and, um, Let's revisit what, what's
[00:11:43:210 - 00:11:44:510] **Speaker 1:** actually going on there, so.
[00:11:45:349 - 00:11:46:869] **Speaker 1:** This is the defective curve.
[00:11:48:409 - 00:11:51:270] **Speaker 1:** So, if you remember back to Oa buckling last year.
[00:11:52:099 - 00:11:54:940] **Speaker 1:** We would say, um, we could have a pin pin
[00:11:54:940 - 00:11:55:299] **Speaker 1:** connection.
[00:11:55:380 - 00:11:58:419] **Speaker 1:** So if we had a pin pin column like this.
[00:12:00:219 - 00:12:03:219] **Speaker 1:** And We had an axial load on it.
[00:12:04:229 - 00:12:06:429] **Speaker 1:** Then it would go into a shape like this.
[00:12:07:690 - 00:12:12:479] **Speaker 1:** And Um, this here would be a critical, critical bucket
[00:12:12:479 - 00:12:14:739] **Speaker 1:** load of pi squared EI.
[00:12:16:090 - 00:12:18:210] **Speaker 1:** Over KL all squared.
[00:12:19:739 - 00:12:23:500] **Speaker 1:** Where K equals 1.0, 4 pin pinned.
[00:12:29:419 - 00:12:33:840] **Speaker 1:** So that's the um One case, I'll come back to
[00:12:33:840 - 00:12:33:950] **Speaker 1:** this.
[00:12:34:000 - 00:12:36:000] **Speaker 1:** I'll I'll link this into the uh existing example.
[00:12:36:080 - 00:12:38:030] **Speaker 1:** If instead we had a fixed fre member.
[00:12:39:559 - 00:12:41:669] **Speaker 1:** So this here is a fixed free.
[00:12:43:000 - 00:12:44:739] **Speaker 1:** Remember, and that was carrying.
[00:12:45:919 - 00:12:46:559] **Speaker 1:** And that's your load.
[00:12:49:900 - 00:12:52:479] **Speaker 1:** Then that would be the critical.
[00:12:53:520 - 00:12:54:830] **Speaker 1:** Is possibly at EI.
[00:12:56:309 - 00:12:57:929] **Speaker 1:** Times KL all squared.
[00:12:59:200 - 00:13:01:580] **Speaker 1:** Where K is equal to 2.0.
[00:13:02:520 - 00:13:05:369] **Speaker 1:** Uh, for This situation.
[00:13:05:609 - 00:13:08:130] **Speaker 1:** So if you were to extend this out.
[00:13:09:979 - 00:13:14:320] **Speaker 1:** Essentially the reason that the effective length multiplier is 2
[00:13:14:460 - 00:13:17:859] **Speaker 1:** for a fixed free is that you've got this sort
[00:13:17:859 - 00:13:20:179] **Speaker 1:** of you basically half the elements so that the effective
[00:13:20:179 - 00:13:21:140] **Speaker 1:** length is longer.
[00:13:21:419 - 00:13:23:280] **Speaker 1:** So you think that it was a comparison.
[00:13:25:280 - 00:13:28:140] **Speaker 1:** Because this is free at the end, it can actually
[00:13:28:140 - 00:13:32:900] **Speaker 1:** translate um transverse, but because this is is moving in
[00:13:32:900 - 00:13:37:809] **Speaker 1:** a constrained um line, there's no transverse deflection allowed here.
[00:13:38:260 - 00:13:41:289] **Speaker 1:** The extent of the curvature in here is higher.
[00:13:41:369 - 00:13:43:099] **Speaker 1:** So you can see, you actually see this from the
[00:13:43:099 - 00:13:43:369] **Speaker 1:** curve.
[00:13:43:489 - 00:13:45:780] **Speaker 1:** This is actually a much more open curvature than the
[00:13:45:780 - 00:13:46:940] **Speaker 1:** curvature that exists here.
[00:13:47:340 - 00:13:50:059] **Speaker 1:** Um, so because of the fact that that's constrained to
[00:13:50:059 - 00:13:51:539] **Speaker 1:** displace in the horizontal direction.
[00:13:51:940 - 00:13:56:099] **Speaker 1:** Whereas this is actually displacing um from this thing the
[00:13:56:419 - 00:14:00:179] **Speaker 1:** the um intensity of curvature in here is higher in
[00:14:00:179 - 00:14:01:940] **Speaker 1:** this element than it is in this element.
[00:14:02:059 - 00:14:06:539] **Speaker 1:** So that's why it actually attracts um more a bigger
[00:14:06:539 - 00:14:08:179] **Speaker 1:** percentage of the the bending line.
[00:14:08:299 - 00:14:13:059] **Speaker 1:** So scratch the previous explanation, um, I kind of misinterpreted
[00:14:13:059 - 00:14:15:710] **Speaker 1:** that so, Yeah, this is what's actually going on here
[00:14:15:710 - 00:14:17:280] **Speaker 1:** and you can see it from the element here that
[00:14:17:590 - 00:14:20:830] **Speaker 1:** um it takes uh a higher intensity of curvature, a
[00:14:20:830 - 00:14:25:369] **Speaker 1:** bit higher, um, tighter curvature requires more energy to induce.
[00:14:26:070 - 00:14:29:030] **Speaker 1:** So, um, this elements actually stiffer just because of those
[00:14:29:030 - 00:14:30:609] **Speaker 1:** combined boundary conditions.
[00:14:31:070 - 00:14:34:349] **Speaker 1:** That's, um, that's constrained transverse to its length, whereas this
[00:14:34:349 - 00:14:36:770] **Speaker 1:** is allowed to move transverse to its length.
[00:14:37:030 - 00:14:39:349] **Speaker 1:** Um, and that's the extra piece of information that I
[00:14:39:349 - 00:14:40:710] **Speaker 1:** was missing before, so.
[00:14:41:710 - 00:14:43:549] **Speaker 1:** Hopefully that explains things, um.
[00:14:49:750 - 00:14:51:500] **Speaker 1:** Um, but this does still hold true that you could
[00:14:51:500 - 00:14:54:080] **Speaker 1:** easily go in here now that you've got your, um,
[00:14:54:469 - 00:14:56:270] **Speaker 1:** your system, your tool set up and all you can
[00:14:56:270 - 00:14:58:590] **Speaker 1:** do is just tweak one input variable and you'll see
[00:14:58:590 - 00:15:00:159] **Speaker 1:** how it changes and distributes this.
[00:15:00:390 - 00:15:05:570] **Speaker 1:** So it's quite an interesting, um, Thing from a design
[00:15:05:570 - 00:15:06:030] **Speaker 1:** perspective.
[00:15:07:440 - 00:15:08:380] **Speaker 1:** It's very tempting.
[00:15:08:859 - 00:15:10:530] **Speaker 1:** You know, there's a great case study we some of
[00:15:10:530 - 00:15:13:909] **Speaker 1:** us had a a guest lecturer here, um, in 302
[00:15:13:909 - 00:15:17:760] **Speaker 1:** which has talked about, um, some consulting work that he'd
[00:15:17:760 - 00:15:21:960] **Speaker 1:** done on, um, a particular piece of mechanical equipment that
[00:15:21:960 - 00:15:25:640] **Speaker 1:** kept failing and they kept strengthening the, the, um, equipment
[00:15:25:640 - 00:15:28:469] **Speaker 1:** where it was failing, and it kept failing.
[00:15:28:719 - 00:15:30:640] **Speaker 1:** And the reason for that is that old saying that
[00:15:30:640 - 00:15:31:679] **Speaker 1:** load follows stiffness.
[00:15:31:880 - 00:15:35:080] **Speaker 1:** So, uh, if you're just strengthening the elements, you're just
[00:15:35:080 - 00:15:36:640] **Speaker 1:** attracting more and more load to that point.
[00:15:36:960 - 00:15:38:390] **Speaker 1:** And possibly not actually winning.
[00:15:38:729 - 00:15:41:770] **Speaker 1:** Um, so in this case here, suppose we had one
[00:15:41:770 - 00:15:44:950] **Speaker 1:** element that was actually a little bit too highly stressed.
[00:15:45:710 - 00:15:49:059] **Speaker 1:** Um, one option is that we strengthen that element, um,
[00:15:49:179 - 00:15:51:789] **Speaker 1:** that may actually solve the problem, but also being aware
[00:15:51:789 - 00:15:53:619] **Speaker 1:** that by making it stronger we're probably also making it
[00:15:53:619 - 00:15:57:030] **Speaker 1:** stiffer and that it's also attracting more load, whereas the
[00:15:57:030 - 00:16:00:070] **Speaker 1:** actual relative stiffness, um, of the elements could be one
[00:16:00:070 - 00:16:02:690] **Speaker 1:** way to just redistribute the load through the structure as
[00:16:02:690 - 00:16:02:989] **Speaker 1:** well.
[00:16:03:229 - 00:16:05:590] **Speaker 1:** So there's multiple things that are available to you as
[00:16:05:590 - 00:16:08:630] **Speaker 1:** a designer to work out how you manage how a
[00:16:08:630 - 00:16:11:150] **Speaker 1:** structure reacts to the applied loads.
[00:16:13:070 - 00:16:16:049] **Speaker 1:** So my apologies for any confusion there, um, hopefully you're
[00:16:16:510 - 00:16:19:700] **Speaker 1:** comfortable with the, The final explanation.
[00:16:22:380 - 00:16:24:059] **Speaker 1:** Um, this is the problem we solved in the lab,
[00:16:24:299 - 00:16:25:929] **Speaker 1:** all the intermediate answers.
[00:16:27:119 - 00:16:33:440] **Speaker 1:** I And what we have here Was out of sync
[00:16:33:440 - 00:16:33:840] **Speaker 1:** here.
[00:16:36:520 - 00:16:38:010] **Speaker 1:** We had this shape.
[00:16:39:030 - 00:16:40:450] **Speaker 1:** Now when it comes to the test.
[00:16:42:179 - 00:16:44:809] **Speaker 1:** You're only gonna be, um, it is primarily a written
[00:16:44:809 - 00:16:46:849] **Speaker 1:** test and you have a written test script and you'll
[00:16:46:849 - 00:16:50:250] **Speaker 1:** be, um, writing key answers and interpreting them and sketching
[00:16:50:250 - 00:16:52:179] **Speaker 1:** reaction loads and defective shapes.
[00:16:52:929 - 00:16:56:010] **Speaker 1:** And essentially the computer is available as your calculator or
[00:16:56:010 - 00:16:58:989] **Speaker 1:** as your computational tool that supports this.
[00:16:59:369 - 00:17:02:049] **Speaker 1:** So if you do have the pulling code, that is
[00:17:02:049 - 00:17:04:170] **Speaker 1:** going to be beneficial to you and that will help
[00:17:04:170 - 00:17:06:760] **Speaker 1:** guide what you choose to sketch down, but you don't
[00:17:06:760 - 00:17:08:729] **Speaker 1:** necessarily have to have that pulling code to be able
[00:17:08:729 - 00:17:09:670] **Speaker 1:** to get full marks.
[00:17:10:560 - 00:17:12:449] **Speaker 1:** So the key thing here is that you can just
[00:17:12:449 - 00:17:16:209] **Speaker 1:** focus on If you're trying to draw this by hand,
[00:17:16:750 - 00:17:19:270] **Speaker 1:** you've got 3 values here, um, and what you want
[00:17:19:270 - 00:17:20:790] **Speaker 1:** to do is use those at the nodal points.
[00:17:21:030 - 00:17:23:188] **Speaker 1:** So if we look at those 3 values, we have
[00:17:23:188 - 00:17:27:949] **Speaker 1:** a, a positive translation for Q1, a positive rotation for
[00:17:27:949 - 00:17:30:109] **Speaker 1:** Q2, and a negative rotation for Q3.
[00:17:31:140 - 00:17:34:739] **Speaker 1:** So locally around here, we know that this element has
[00:17:34:739 - 00:17:35:949] **Speaker 1:** rotated to the right.
[00:17:36:630 - 00:17:40:170] **Speaker 1:** It's rotated counterclockwise um because it was a positive value
[00:17:40:589 - 00:17:42:949] **Speaker 1:** and then the end it's rotated clockwise because it was
[00:17:42:949 - 00:17:43:790] **Speaker 1:** a negative value.
[00:17:45:650 - 00:17:47:770] **Speaker 1:** So once we know the behaviour sort of locally in
[00:17:47:770 - 00:17:50:630] **Speaker 1:** here, around the nodal points, we must have zero slope
[00:17:50:630 - 00:17:53:089] **Speaker 1:** and zero deflection here, then we can just draw a
[00:17:53:089 - 00:17:57:530] **Speaker 1:** smooth continuous curve that joins those um elements.
[00:17:58:349 - 00:18:00:829] **Speaker 1:** Suppose that this element had actually had a really large
[00:18:00:829 - 00:18:03:239] **Speaker 1:** concentrated counterclockwise moment acting here.
[00:18:03:709 - 00:18:06:109] **Speaker 1:** In that situation we may have actually seen the element
[00:18:06:109 - 00:18:10:060] **Speaker 1:** rotated clockwise here and if we had those two elements
[00:18:10:060 - 00:18:12:989] **Speaker 1:** that were oriented like this at the two respective nodes,
[00:18:13:390 - 00:18:15:890] **Speaker 1:** then we would have to draw a double curvature shape
[00:18:15:890 - 00:18:16:989] **Speaker 1:** that fitted between them.
[00:18:18:390 - 00:18:20:760] **Speaker 1:** Um, but in this case, uh, one inch into the
[00:18:20:760 - 00:18:21:699] **Speaker 1:** element is like this.
[00:18:22:280 - 00:18:24:199] **Speaker 1:** There's no reason to believe that there's gonna be some
[00:18:24:199 - 00:18:28:439] **Speaker 1:** higher, um, mode curve that's been induced in there, so
[00:18:28:439 - 00:18:30:520] **Speaker 1:** we can just draw, uh, curve shape.
[00:18:30:680 - 00:18:32:560] **Speaker 1:** So when you are drawing this by hand, if you
[00:18:32:560 - 00:18:34:880] **Speaker 1:** don't have the plotting code to help guide you, the
[00:18:34:880 - 00:18:36:560] **Speaker 1:** key thing is focus on what's happening at the nodal
[00:18:36:560 - 00:18:39:400] **Speaker 1:** points because that's where you have the information and then
[00:18:39:400 - 00:18:42:219] **Speaker 1:** you can infer the behaviour, um, between those.
[00:18:42:880 - 00:18:44:900] **Speaker 1:** The key things, you know, this is a a pin
[00:18:44:900 - 00:18:47:420] **Speaker 1:** joint, so you don't want to see a non-zero displacement
[00:18:47:420 - 00:18:50:150] **Speaker 1:** here because that breaches the setup of the problem.
[00:18:50:609 - 00:18:52:680] **Speaker 1:** Likewise, you don't want to see any non-zero displacement or
[00:18:52:680 - 00:18:55:300] **Speaker 1:** rotation here because that was a fixed support and it's
[00:18:55:300 - 00:18:57:140] **Speaker 1:** not permissible based upon the way the problem was set
[00:18:57:140 - 00:18:57:479] **Speaker 1:** up.
[00:18:58:300 - 00:19:01:260] **Speaker 1:** Um, and also here, if this was an internal 90
[00:19:01:260 - 00:19:05:939] **Speaker 1:** initially, it's an internal 90 after defection as well.
[00:19:08:150 - 00:19:10:459] **Speaker 1:** So just skip over this um a little bit yesterday,
[00:19:10:510 - 00:19:12:550] **Speaker 1:** I'm not gonna go through and the, um, you know,
[00:19:12:670 - 00:19:13:829] **Speaker 1:** read every bit of this.
[00:19:14:310 - 00:19:15:790] **Speaker 1:** um, but the key thing here is that when we
[00:19:15:790 - 00:19:19:819] **Speaker 1:** set up the problem initially, We connected, um, the ZG
[00:19:19:819 - 00:19:22:660] **Speaker 1:** degree of freedom at the bottom of element one and
[00:19:22:660 - 00:19:24:459] **Speaker 1:** the rotational degree of freedom at the left edge of
[00:19:24:459 - 00:19:25:119] **Speaker 1:** element two.
[00:19:26:000 - 00:19:27:449] **Speaker 1:** To the degree of freedom Q2.
[00:19:28:959 - 00:19:30:400] **Speaker 1:** So that was what happened when we set up our
[00:19:30:400 - 00:19:31:640] **Speaker 1:** original assembly matrices.
[00:19:31:880 - 00:19:33:510] **Speaker 1:** So what that meant was that when we were linking
[00:19:33:510 - 00:19:38:400] **Speaker 1:** those to one single mathematical quantity in our final lowercase
[00:19:38:400 - 00:19:41:119] **Speaker 1:** q vector, and we were saying that that value represents
[00:19:41:119 - 00:19:42:359] **Speaker 1:** deflection of both elements.
[00:19:42:640 - 00:19:45:900] **Speaker 1:** So, um, well that we did the same for translations,
[00:19:45:989 - 00:19:48:079] **Speaker 1:** and what that means is that the two elements basically
[00:19:48:079 - 00:19:50:400] **Speaker 1:** translate together and rotate together.
[00:19:51:130 - 00:19:53:209] **Speaker 1:** But they can do that independently of the support.
[00:19:53:449 - 00:19:55:650] **Speaker 1:** So this is just in that bottom left-hand corner of
[00:19:55:650 - 00:19:59:250] **Speaker 1:** the structure, um, what this might, this element might look
[00:19:59:250 - 00:20:02:439] **Speaker 1:** like physically and just, um, because of the fact that
[00:20:02:439 - 00:20:05:770] **Speaker 1:** it's pinned, uh, and slotted to the support, that doesn't
[00:20:05:770 - 00:20:07:130] **Speaker 1:** mean the elements themselves can move independently.
[00:20:08:209 - 00:20:10:810] **Speaker 1:** And we will come back to that next week and
[00:20:10:810 - 00:20:13:130] **Speaker 1:** look at how we can break that coupling if we
[00:20:13:130 - 00:20:14:290] **Speaker 1:** do want to do so.
[00:20:14:569 - 00:20:16:290] **Speaker 1:** So we're not, we're not there just yet.
[00:20:19:719 - 00:20:22:270] **Speaker 1:** Um, this was the, the stuff with the code, so
[00:20:22:270 - 00:20:24:680] **Speaker 1:** many of you worked through this yesterday in the lab
[00:20:24:839 - 00:20:25:939] **Speaker 1:** and got the plotting code.
[00:20:27:140 - 00:20:30:979] **Speaker 1:** Um, this is our shape functions, axial transverse, and this
[00:20:30:979 - 00:20:33:900] **Speaker 1:** is just a really good example of what I've been
[00:20:33:900 - 00:20:37:199] **Speaker 1:** sort of, Um, talking to you all the way through
[00:20:37:199 - 00:20:42:969] **Speaker 1:** around this idea that Um Not all deflections are representative
[00:20:42:969 - 00:20:44:459] **Speaker 1:** of continuous element deflection.
[00:20:45:319 - 00:20:46:680] **Speaker 1:** And this is the process of doing that.
[00:20:46:800 - 00:20:48:880] **Speaker 1:** So we, we go through and, um, the U of
[00:20:48:880 - 00:20:51:599] **Speaker 1:** X uses our axial shape functions, our V of X
[00:20:51:599 - 00:20:53:000] **Speaker 1:** uses our transverse ones.
[00:20:53:550 - 00:20:56:030] **Speaker 1:** Our U of X, for example, here at X equals
[00:20:56:030 - 00:21:00:359] **Speaker 1:** 0.2 L is the amount by which this little evaluation
[00:21:00:359 - 00:21:04:390] **Speaker 1:** point internally within the element has, um, displaced axially.
[00:21:04:729 - 00:21:07:589] **Speaker 1:** Uh, our V of X is how much it's, um,
[00:21:07:599 - 00:21:10:099] **Speaker 1:** displaced transverse to the longitudinal axis.
[00:21:10:790 - 00:21:13:510] **Speaker 1:** Um, when it comes to plotting things in Python, Python
[00:21:13:510 - 00:21:15:229] **Speaker 1:** wants X and Y coordinates, not U of X and
[00:21:15:229 - 00:21:15:819] **Speaker 1:** V of X.
[00:21:16:229 - 00:21:18:099] **Speaker 1:** So we just need to do a little vector diagram
[00:21:18:099 - 00:21:21:709] **Speaker 1:** and piece together some from we're displacing from the undeflected
[00:21:21:709 - 00:21:24:349] **Speaker 1:** position to the defective position, and we're breaking that up
[00:21:24:349 - 00:21:28:540] **Speaker 1:** into cosine and sine terms, and these were the vector
[00:21:28:540 - 00:21:31:550] **Speaker 1:** equations that come out of that to work out how
[00:21:31:550 - 00:21:33:069] **Speaker 1:** the, the element defects.
[00:21:34:319 - 00:21:39:430] **Speaker 1:** And once she did that, Um, this undeflected baseline.
[00:21:41:130 - 00:21:43:459] **Speaker 1:** Is the vector of all these blue dots here.
[00:21:43:630 - 00:21:47:310] **Speaker 1:** These are the ones that represent the undeflected shape, and
[00:21:47:310 - 00:21:51:270] **Speaker 1:** then once we add on the magnified deflections, deflected XG
[00:21:51:270 - 00:21:54:430] **Speaker 1:** and deflected YG are the X and Y coordinates of
[00:21:54:430 - 00:21:56:469] **Speaker 1:** each of these points in here.
[00:21:57:729 - 00:21:59:530] **Speaker 1:** So in this case we're only using 11 points.
[00:21:59:949 - 00:22:01:689] **Speaker 1:** You know, if you had, if you chose 3 points,
[00:22:01:729 - 00:22:04:770] **Speaker 1:** you're gonna end up with quite a a coarse element
[00:22:04:770 - 00:22:08:329] **Speaker 1:** plotting, um, but you know, even with 11 you're actually
[00:22:08:329 - 00:22:11:050] **Speaker 1:** getting quite a smooth curve, um, and it is a
[00:22:11:050 - 00:22:14:189] **Speaker 1:** little bit into the diminishing returns once you go, um,
[00:22:14:209 - 00:22:16:670] **Speaker 1:** beyond sort of 10 or 20 points within an element.
[00:22:19:349 - 00:22:21:630] **Speaker 1:** That was the final curve that exists here, so that
[00:22:21:630 - 00:22:23:010] **Speaker 1:** was the one that we sketched by hand.
[00:22:23:640 - 00:22:25:510] **Speaker 1:** And I guess one thing that I just hopefully you
[00:22:25:510 - 00:22:28:599] **Speaker 1:** can appreciate, um, maybe not quite as much as me,
[00:22:28:790 - 00:22:30:270] **Speaker 1:** but you know.
[00:22:31:130 - 00:22:34:630] **Speaker 1:** This here This entire defective curve is really coming from
[00:22:34:630 - 00:22:37:290] **Speaker 1:** just 3 values that are specific to this problem.
[00:22:38:739 - 00:22:42:939] **Speaker 1:** We know the physical locations of the nodes, the shape
[00:22:42:939 - 00:22:45:800] **Speaker 1:** functions of predetermined information that are generic to all problems.
[00:22:46:810 - 00:22:49:540] **Speaker 1:** All we've taken is the nodal points and these three
[00:22:49:540 - 00:22:53:219] **Speaker 1:** small pieces of information about deflections and from that we
[00:22:53:219 - 00:22:56:099] **Speaker 1:** can get this entire deflected curve which exists from that.
[00:22:59:709 - 00:23:02:790] **Speaker 1:** So I think that's quite, quite special.
[00:23:02:839 - 00:23:05:530] **Speaker 1:** It's quite nice to know that you can get so,
[00:23:05:640 - 00:23:07:920] **Speaker 1:** so much from so little, um, but that is ultimately
[00:23:07:920 - 00:23:10:709] **Speaker 1:** the premise under which final elements are set up.
[00:23:10:880 - 00:23:12:839] **Speaker 1:** The idea that you can solve it as few discrete
[00:23:12:839 - 00:23:15:739] **Speaker 1:** points but that being representative of the larger structure.
[00:23:22:849 - 00:23:25:890] **Speaker 1:** Now, what we wanna do is one, we're gonna do
[00:23:25:890 - 00:23:27:089] **Speaker 1:** a couple of final examples.
[00:23:28:689 - 00:23:31:020] **Speaker 1:** So this here is a simple structure.
[00:23:31:420 - 00:23:32:979] **Speaker 1:** Um, we've got a pin joint at the left which
[00:23:32:979 - 00:23:36:099] **Speaker 1:** constrains translation but not rotation and then we've got two
[00:23:36:099 - 00:23:37:199] **Speaker 1:** fixed supports here and here.
[00:23:38:209 - 00:23:40:489] **Speaker 1:** We've got some ANI values and there's a 100 kilonewton
[00:23:40:489 - 00:23:43:150] **Speaker 1:** load applied at that central node.
[00:23:44:780 - 00:23:48:420] **Speaker 1:** Now with all of these situations, it's really, really important
[00:23:48:420 - 00:23:50:739] **Speaker 1:** that you first know how to assign the degrees of
[00:23:50:739 - 00:23:52:140] **Speaker 1:** freedom, so we'll work through that very quickly.
[00:23:53:790 - 00:23:57:989] **Speaker 1:** This is a pen Or sometimes known as a knife-edge
[00:23:57:989 - 00:23:58:250] **Speaker 1:** support.
[00:24:05:829 - 00:24:07:290] **Speaker 1:** And that constrains.
[00:24:09:920 - 00:24:22:939] **Speaker 1:** XG And YG But not ZG So therefore, We have
[00:24:22:939 - 00:24:24:420] **Speaker 1:** one Q value there.
[00:24:25:930 - 00:24:30:170] **Speaker 1:** So there's only um one of the permissible possible degrees
[00:24:30:170 - 00:24:33:250] **Speaker 1:** of freedom that is allowed to have a potentially non-zero
[00:24:33:250 - 00:24:33:790] **Speaker 1:** value.
[00:24:35:189 - 00:24:38:310] **Speaker 1:** So for that we're gonna put in a counterclockwise rotation
[00:24:38:310 - 00:24:38:689] **Speaker 1:** here.
[00:24:39:880 - 00:24:40:959] **Speaker 1:** And we'll call that Q1.
[00:24:43:650 - 00:24:45:010] **Speaker 1:** Here and here.
[00:24:47:599 - 00:24:48:420] **Speaker 1:** Fully fixed.
[00:24:53:290 - 00:25:00:640] **Speaker 0:** No permissible Reflections So, there's no Q values.
[00:25:04:500 - 00:25:07:260] **Speaker 1:** And by putting in no cuevals, that's how we tell
[00:25:07:260 - 00:25:09:420] **Speaker 1:** the system that those nodes are constrained.
[00:25:11:910 - 00:25:13:250] **Speaker 1:** Now if we look at this point here.
[00:25:14:489 - 00:25:17:810] **Speaker 1:** There is the potential for non-zero displacements in the horizontal
[00:25:17:810 - 00:25:21:770] **Speaker 1:** X global, uh, vertical Y global, and the rotational Z
[00:25:21:770 - 00:25:23:430] **Speaker 1:** global directions.
[00:25:25:089 - 00:25:34:369] **Speaker 1:** So very permissible Deflection components.
[00:25:37:829 - 00:25:40:359] **Speaker 1:** Which of course is the XG YG.
[00:25:41:170 - 00:25:42:050] **Speaker 1:** And the ZG.
[00:25:43:109 - 00:25:45:810] **Speaker 1:** So When I was on 3.
[00:25:46:920 - 00:25:49:099] **Speaker 1:** Q values at the nodal point.
[00:25:50:910 - 00:25:52:589] **Speaker 1:** So we, in this case called them.
[00:25:54:290 - 00:25:59:910] **Speaker 1:** 2 Q3 And Q4.
[00:26:02:050 - 00:26:04:709] **Speaker 1:** And we don't necessarily have to follow that exact sequence.
[00:26:05:660 - 00:26:08:699] **Speaker 1:** Um, we could have called, you know, the rotation Q2
[00:26:08:699 - 00:26:10:729] **Speaker 1:** and then the vertical Q3 and then this one of
[00:26:10:729 - 00:26:11:520] **Speaker 1:** Q4.
[00:26:12:060 - 00:26:15:410] **Speaker 1:** Um, that wouldn't necessarily be wrong, but it's just probably
[00:26:15:410 - 00:26:16:599] **Speaker 1:** a little bit less intuitive.
[00:26:16:900 - 00:26:20:219] **Speaker 1:** Um, the assembly matrices won't have quite some nice form
[00:26:20:219 - 00:26:20:680] **Speaker 1:** to them.
[00:26:20:780 - 00:26:23:739] **Speaker 1:** Like for larger structures, you often find that if you
[00:26:23:739 - 00:26:26:160] **Speaker 1:** follow a good numbering sequences, your assembly matrices might have
[00:26:26:500 - 00:26:28:739] **Speaker 1:** just been up an assembly matrix or have a small
[00:26:28:739 - 00:26:31:050] **Speaker 1:** subset of the matrix which is an ass uh sorry,
[00:26:31:099 - 00:26:32:099] **Speaker 1:** an identity matrix.
[00:26:34:939 - 00:26:38:699] **Speaker 1:** So that is, you know, reasonable kind of logical numbering
[00:26:38:699 - 00:26:42:339] **Speaker 1:** sequence is um favourable if not essential.
[00:26:44:819 - 00:26:47:050] **Speaker 1:** So like we always do with problems, once we've assigned
[00:26:47:050 - 00:26:49:050] **Speaker 1:** those global degrees of freedom, we then jump into free
[00:26:49:050 - 00:26:49:859] **Speaker 1:** body diagrams.
[00:26:50:160 - 00:26:54:449] **Speaker 1:** So they, there is, there will be marks for the
[00:26:54:449 - 00:26:55:770] **Speaker 1:** free body diagrams in the test.
[00:26:56:939 - 00:26:58:380] **Speaker 1:** Because it is such an important step.
[00:27:00:089 - 00:27:02:569] **Speaker 1:** So we're gonna assume that we have these elements of
[00:27:02:569 - 00:27:05:410] **Speaker 1:** 0 degree transformation angles here and here, and we'll just
[00:27:05:410 - 00:27:06:770] **Speaker 1:** assume this one's -90.
[00:27:06:969 - 00:27:08:729] **Speaker 1:** So that's the, the chosen orientation.
[00:27:11:239 - 00:27:13:680] **Speaker 1:** Now what we need to do here is work out
[00:27:13:680 - 00:27:19:290] **Speaker 1:** the relationship between um The degrees of freedom within the
[00:27:19:290 - 00:27:21:810] **Speaker 1:** elements to the overall structural degrees of freedom.
[00:27:23:119 - 00:27:24:640] **Speaker 1:** Now the first thing we can see here is that
[00:27:24:640 - 00:27:28:079] **Speaker 1:** D1 and T2 don't correspond to anything globally, but that
[00:27:28:079 - 00:27:30:180] **Speaker 1:** D3, 4 element one.
[00:27:31:199 - 00:27:32:560] **Speaker 1:** Corresponds to Q1.
[00:27:34:969 - 00:27:36:839] **Speaker 1:** Then at the central node, we have 3 elements which
[00:27:36:839 - 00:27:40:079] **Speaker 1:** connect into that node, and we have Q2, Q3, and
[00:27:40:079 - 00:27:40:660] **Speaker 1:** Q4 there.
[00:27:40:839 - 00:27:44:260] **Speaker 1:** So what we're saying here is that D6 for element
[00:27:44:260 - 00:27:44:660] **Speaker 1:** 1.
[00:27:45:760 - 00:27:48:359] **Speaker 1:** We're gonna link that to the.
[00:27:49:489 - 00:27:51:109] **Speaker 1:** 3, or 2.
[00:27:52:130 - 00:27:54:849] **Speaker 1:** And we're also going to link that to D3 for
[00:27:54:849 - 00:27:55:569] **Speaker 1:** element 3.
[00:27:57:150 - 00:27:58:599] **Speaker 1:** And we're going to call that.
[00:27:59:709 - 00:28:00:349] **Speaker 1:** Q4.
[00:28:07:439 - 00:28:09:069] **Speaker 1:** Then we're gonna do the translations, I mean maybe that's
[00:28:09:069 - 00:28:13:040] **Speaker 1:** not the most intuitive order, but D4 for element 1
[00:28:13:040 - 00:28:16:479] **Speaker 1:** will be equal to D1 for element two, which will
[00:28:16:479 - 00:28:19:310] **Speaker 1:** be equal to D1 for element three.
[00:28:21:329 - 00:28:23:430] **Speaker 1:** And that's going to be equal to Q2.
[00:28:24:900 - 00:28:27:489] **Speaker 1:** And then D5 fell on 1.
[00:28:28:189 - 00:28:29:969] **Speaker 1:** We'll get the 2 for element 2.
[00:28:31:550 - 00:28:33:449] **Speaker 1:** And D2, L3.
[00:28:34:709 - 00:28:36:069] **Speaker 1:** And that will be our Q3.
[00:28:40:420 - 00:28:43:000] **Speaker 1:** So that's the key information that we're gonna use to
[00:28:43:339 - 00:28:45:300] **Speaker 1:** generate our assembly matrices.
[00:28:51:459 - 00:28:54:900] **Speaker 1:** So once we've got that connectivity information, the rest of
[00:28:54:900 - 00:28:56:180] **Speaker 1:** it's all relatively procedural.
[00:28:56:219 - 00:28:58:699] **Speaker 1:** It follows the exact same process that you did in
[00:28:58:699 - 00:28:59:719] **Speaker 1:** the lab yesterday.
[00:29:00:060 - 00:29:02:339] **Speaker 1:** And we have our transformation matrix which comes from our
[00:29:02:699 - 00:29:03:880] **Speaker 1:** angles of orientation.
[00:29:04:099 - 00:29:06:780] **Speaker 1:** It's the same form, it's the same equation for a
[00:29:06:780 - 00:29:08:780] **Speaker 1:** transformation matrix that you coded up yesterday.
[00:29:09:260 - 00:29:10:380] **Speaker 1:** No need to change anything there.
[00:29:13:890 - 00:29:17:500] **Speaker 1:** Um, because the elements are all the same length and
[00:29:17:500 - 00:29:20:060] **Speaker 1:** have the same material properties, all three K matrices are
[00:29:20:060 - 00:29:24:300] **Speaker 1:** the same, but once we introduce orientation information, K3 is
[00:29:24:300 - 00:29:25:739] **Speaker 1:** now different from K1 and K2.
[00:29:26:719 - 00:29:35:079] **Speaker 1:** This is our um Assembly matrices So Couple, you know,
[00:29:35:300 - 00:29:36:319] **Speaker 1:** quickly look at this.
[00:29:40:839 - 00:29:42:719] **Speaker 1:** There's a couple of all 0 columns.
[00:29:45:869 - 00:29:48:229] **Speaker 1:** As D1 for element 1.
[00:29:48:989 - 00:29:51:329] **Speaker 1:** And D2 element 1.
[00:29:53:479 - 00:30:01:290] **Speaker 1:** constrained I have a pen So that all 0 column
[00:30:01:390 - 00:30:05:170] **Speaker 1:** is telling the system that this that's constrained.
[00:30:06:469 - 00:30:10:319] **Speaker 1:** Um, then the assembly matrix elements 2 and 3 actually
[00:30:10:319 - 00:30:12:699] **Speaker 1:** end up being the same, the same matrix.
[00:30:17:000 - 00:30:19:739] **Speaker 1:** And what that's telling us is the D4 to D6.
[00:30:20:979 - 00:30:26:630] **Speaker 1:** For Elements 2.
[00:30:27:829 - 00:30:32:770] **Speaker 1:** And 3 Uh, fully fixed.
[00:30:34:900 - 00:30:38:280] **Speaker 1:** And that's by the two respective, uh, fixed supports.
[00:30:39:969 - 00:30:42:969] **Speaker 1:** There's also an all row, the Q1, and that's simply
[00:30:42:969 - 00:30:44:849] **Speaker 1:** because uh elements.
[00:30:46:239 - 00:30:47:449] **Speaker 1:** 2 and 3 are over here.
[00:30:47:689 - 00:30:48:400] **Speaker 1:** Q1 is over here.
[00:30:48:449 - 00:30:50:380] **Speaker 1:** There's no direct connection to this degree of freedom.
[00:30:50:660 - 00:30:52:910] **Speaker 1:** That's all that that all 0 row means.
[00:30:54:430 - 00:30:57:500] **Speaker 1:** From there we can bang out um the QG so
[00:30:57:500 - 00:30:59:839] **Speaker 1:** there's a QG1, QG 2 QG 3, we sum them
[00:30:59:839 - 00:31:00:660] **Speaker 1:** up, we get this.
[00:31:01:550 - 00:31:04:420] **Speaker 1:** Um, this here is our, um, Q vector.
[00:31:05:380 - 00:31:07:319] **Speaker 1:** So this is information given in the question.
[00:31:08:800 - 00:31:11:099] **Speaker 1:** Um, and that of course is also combined.
[00:31:12:969 - 00:31:22:489] **Speaker 1:** With Our chosen Numbering sequence.
[00:31:26:260 - 00:31:28:060] **Speaker 1:** 4 Q1.
[00:31:29:589 - 00:31:30:589] **Speaker 1:** To Q4.
[00:31:32:579 - 00:31:34:160] **Speaker 1:** So what was actually given in the question.
[00:31:35:400 - 00:31:37:800] **Speaker 1:** Was the fact that there was 100 kilonewton load upwards
[00:31:37:800 - 00:31:38:099] **Speaker 1:** here.
[00:31:39:369 - 00:31:41:729] **Speaker 1:** We weren't given this vector, we were given this information,
[00:31:42:060 - 00:31:44:449] **Speaker 1:** so we just have to say that, um, yeah, that
[00:31:44:449 - 00:31:46:069] **Speaker 1:** was, that was Q3 vertically.
[00:31:46:359 - 00:31:48:410] **Speaker 1:** The others were 0, which is why we end up
[00:31:48:410 - 00:31:50:930] **Speaker 1:** with, um, that's the entry there.
[00:31:51:209 - 00:31:54:359] **Speaker 1:** So if we've chosen a different numbering sequence for the
[00:31:54:689 - 00:31:57:089] **Speaker 1:** overall structural degrees of freedom, we'd have the same numbers
[00:31:57:089 - 00:31:57:949] **Speaker 1:** but in a different order.
[00:31:59:339 - 00:32:01:209] **Speaker 1:** And we do have a mixed solution where we have,
[00:32:01:540 - 00:32:04:319] **Speaker 1:** uh, Newton metres applying to the rotational degree of freedom.
[00:32:05:060 - 00:32:07:300] **Speaker 1:** And Newton's applying to a translational.
[00:32:12:160 - 00:32:14:680] **Speaker 1:** So once we work through that, we put the queue
[00:32:14:680 - 00:32:17:000] **Speaker 1:** in and we can just solve that um system the
[00:32:17:000 - 00:32:17:900] **Speaker 1:** way we always have.
[00:32:19:060 - 00:32:21:420] **Speaker 1:** This is what the answer that we would get.
[00:32:24:339 - 00:32:26:180] **Speaker 1:** So one thing that we'll definitely focus on on the
[00:32:26:180 - 00:32:29:380] **Speaker 1:** test is not just getting a vector of numbers, but
[00:32:29:380 - 00:32:32:780] **Speaker 1:** being able to interpret uh and and explain what those
[00:32:32:780 - 00:32:33:739] **Speaker 1:** numbers actually mean.
[00:32:36:250 - 00:32:39:199] **Speaker 1:** So if we go back to the original system, Q1.
[00:32:40:280 - 00:32:45:619] **Speaker 1:** Was the rotation And just a quick reminder of counterclockwise.
[00:32:46:430 - 00:32:52:569] **Speaker 1:** Positive At the left node, which was at the pin.
[00:32:54:300 - 00:32:55:979] **Speaker 1:** And then we have this here.
[00:32:56:060 - 00:32:59:000] **Speaker 1:** The 2nd entry was XG.
[00:33:01:280 - 00:33:07:030] **Speaker 1:** At the central node Um, then we have YG.
[00:33:11:849 - 00:33:14:510] **Speaker 1:** The central node and this one here was the ZG.
[00:33:16:209 - 00:33:21:270] **Speaker 1:** Rotation Again, counterclockwise is positive.
[00:33:22:760 - 00:33:23:719] **Speaker 1:** At the central node.
[00:33:29:729 - 00:33:31:680] **Speaker 1:** So what we have here is the Q1.
[00:33:32:530 - 00:33:35:670] **Speaker 1:** So this was a value of 1.90.
[00:33:37:329 - 00:33:40:390] **Speaker 1:** Milliradians, counterclockwise because it was a positive value.
[00:33:41:239 - 00:33:43:579] **Speaker 1:** Uh, then we have here and here.
[00:33:48:939 - 00:33:53:140] **Speaker 1:** Fixed support No translation.
[00:33:56:219 - 00:34:02:589] **Speaker 1:** Or Rotation So if you are drawing this, or when
[00:34:02:589 - 00:34:04:670] **Speaker 1:** you are drawing this by hand in the test, if
[00:34:04:670 - 00:34:06:569] **Speaker 1:** it is a fixed support, please make sure there's no
[00:34:06:569 - 00:34:07:060] **Speaker 1:** rotation.
[00:34:07:109 - 00:34:09:750] **Speaker 1:** Don't have the, the element coming in like this to
[00:34:09:750 - 00:34:13:790] **Speaker 1:** a support because that's not a representative of the physical
[00:34:13:790 - 00:34:14:148] **Speaker 1:** system.
[00:34:14:459 - 00:34:16:669] **Speaker 1:** You see you've got a zero deflection initially and then
[00:34:16:989 - 00:34:18:830] **Speaker 1:** a gradual progression from there.
[00:34:21:360 - 00:34:23:580] **Speaker 1:** You know here um we've got.
[00:34:24:439 - 00:34:27:520] **Speaker 1:** Our Q2 here, so that's essentially the line between there
[00:34:27:520 - 00:34:31:760] **Speaker 1:** and there, that's the initial and displaced position horizontally, so
[00:34:31:760 - 00:34:32:800] **Speaker 1:** that's our Q2.
[00:34:33:648 - 00:34:36:260] **Speaker 1:** Which is 0.7.
[00:34:37:499 - 00:34:43:419] **Speaker 1:** 86 millimetres, our vertical deflection here.
[00:34:44:628 - 00:34:46:679] **Speaker 1:** Is 4.50.
[00:34:47:429 - 00:34:52:250] **Speaker 1:** millimetres and then our rotation here is a magnitude of
[00:34:52:310 - 00:34:54:729] **Speaker 1:** 0.414.
[00:34:56:020 - 00:34:56:830] **Speaker 1:** Many radiants.
[00:34:57:120 - 00:34:58:560] **Speaker 1:** So again, the key thing here if you were to
[00:34:58:560 - 00:35:00:879] **Speaker 1:** sketch this by hand is focus on what's happening at
[00:35:00:879 - 00:35:01:399] **Speaker 1:** the nodal points.
[00:35:01:439 - 00:35:04:040] **Speaker 1:** You know there's zero deflection, zero slope there, you know
[00:35:04:040 - 00:35:06:840] **Speaker 1:** there's zero deflection, but a rotation here, and you know
[00:35:06:840 - 00:35:10:370] **Speaker 1:** that this note has both translated in space and rotated,
[00:35:10:820 - 00:35:13:919] **Speaker 1:** uh, because it's negative rotation, it's actually a clockwise rotation,
[00:35:14:159 - 00:35:15:239] **Speaker 1:** not counterclockwise.
[00:35:16:090 - 00:35:18:429] **Speaker 1:** And that's how you would go about piecing together and
[00:35:18:429 - 00:35:21:820] **Speaker 1:** sketching this by hand, um, in the chest.
[00:35:26:000 - 00:35:27:979] **Speaker 1:** We can also look at.
[00:35:28:780 - 00:35:30:909] **Speaker 1:** Um, all the reaction lines, so.
[00:35:32:179 - 00:35:34:750] **Speaker 1:** We can, um, basically break out the three elements and
[00:35:34:750 - 00:35:36:610] **Speaker 1:** look at the forcing terms that exist within them.
[00:35:38:709 - 00:35:41:459] **Speaker 1:** Those are the 3 forcing vectors, these are them sketched
[00:35:41:459 - 00:35:42:600] **Speaker 1:** onto 3 body diagrams.
[00:35:44:419 - 00:35:45:959] **Speaker 1:** So a few things to look at here.
[00:35:47:530 - 00:35:49:449] **Speaker 1:** These values are.
[00:35:51:219 - 00:35:53:510] **Speaker 1:** The reaction loads or the reactions.
[00:35:55:030 - 00:35:56:290] **Speaker 1:** At this fixed support.
[00:35:58:750 - 00:36:01:590] **Speaker 1:** There is only one element that's that connects into this
[00:36:01:590 - 00:36:05:810] **Speaker 1:** fixed support, so those element forces are the reaction force.
[00:36:07:500 - 00:36:11:330] **Speaker 1:** These here Also reaction loads.
[00:36:14:260 - 00:36:15:800] **Speaker 1:** Uh, as we have up here.
[00:36:17:399 - 00:36:18:280] **Speaker 1:** Now this was a pin.
[00:36:21:489 - 00:36:24:959] **Speaker 1:** It's in sport So there's no moment.
[00:36:28:379 - 00:36:30:560] **Speaker 1:** And then the, uh, individual.
[00:36:31:399 - 00:36:34:169] **Speaker 1:** Element here, we can look at the horizontal forces.
[00:36:34:280 - 00:36:37:780] **Speaker 1:** So we've got uh this number, plus this number.
[00:36:38:540 - 00:36:40:439] **Speaker 1:** And this number, if we bring those down.
[00:36:42:580 - 00:36:49:149] **Speaker 1:** So we ended up with Um, Basically they They sum
[00:36:49:149 - 00:36:49:889] **Speaker 1:** up to 0.
[00:36:52:479 - 00:36:54:040] **Speaker 1:** And the reason they sum to zero is that there
[00:36:54:040 - 00:36:57:439] **Speaker 1:** was no applied external external load in the horizontal direction
[00:36:57:439 - 00:36:59:830] **Speaker 1:** at this node, so we'd expect them to sum to
[00:36:59:830 - 00:37:00:120] **Speaker 1:** 0.
[00:37:02:469 - 00:37:04:669] **Speaker 1:** We also look at the moment in terms, we have.
[00:37:05:520 - 00:37:09:590] **Speaker 1:** A moment here, a moment here, and a moment here,
[00:37:10:050 - 00:37:10:370] **Speaker 1:** so.
[00:37:11:270 - 00:37:13:459] **Speaker 1:** If we add those up, um.
[00:37:14:459 - 00:37:19:879] **Speaker 1:** We end up with, um, you know, -115 plus about
[00:37:19:879 - 00:37:24:060] **Speaker 1:** 12, you end up with about -127 plus 127, so
[00:37:24:060 - 00:37:24:860] **Speaker 1:** they sum.
[00:37:26:080 - 00:37:30:469] **Speaker 1:** 20 As you would expect because there was no concentrated
[00:37:30:469 - 00:37:34:070] **Speaker 1:** applied external load, uh, external moment at that node.
[00:37:35:780 - 00:37:38:489] **Speaker 1:** And then finally we have the vertical forces, we have
[00:37:38:489 - 00:37:38:959] **Speaker 1:** this.
[00:37:39:750 - 00:37:41:550] **Speaker 1:** We have this and we have this.
[00:37:42:580 - 00:37:44:429] **Speaker 1:** So if we bring those up, we end up with
[00:37:44:429 - 00:37:47:879] **Speaker 1:** a, 28.8692.
[00:37:48:820 - 00:37:50:600] **Speaker 1:** A 68 point.
[00:37:51:360 - 00:37:52:550] **Speaker 1:** 879 8.
[00:37:53:520 - 00:37:57:110] **Speaker 1:** And a 2 point 2510.
[00:37:57:860 - 00:37:59:459] **Speaker 1:** And if you sum those up, they come to 100
[00:37:59:459 - 00:38:00:300] **Speaker 1:** kil Newtons.
[00:38:02:330 - 00:38:05:090] **Speaker 1:** Which is the applied external load.
[00:38:05:889 - 00:38:10:669] **Speaker 1:** That um The horizontal, sorry, the vertical load that was
[00:38:10:669 - 00:38:12:600] **Speaker 1:** applied at that node.
[00:38:17:929 - 00:38:20:989] **Speaker 1:** Um, we can also do overall equilibrium with the structure.
[00:38:37:350 - 00:38:39:709] **Speaker 1:** This is, if we lump all those together, this is
[00:38:39:709 - 00:38:40:489] **Speaker 1:** what this looks like.
[00:38:41:510 - 00:38:44:080] **Speaker 1:** Um, quick reminder here that.
[00:38:50:250 - 00:38:51:370] **Speaker 1:** This is 4 metres.
[00:38:52:780 - 00:38:55:560] **Speaker 1:** This is 4 metres and the, the vertical offset here.
[00:38:59:459 - 00:39:00:739] **Speaker 1:** That's also 4 metres.
[00:39:03:030 - 00:39:05:580] **Speaker 1:** So we'll basically define a point here, A.
[00:39:07:149 - 00:39:08:580] **Speaker 1:** Um, the overall equilibrium.
[00:39:18:280 - 00:39:21:100] **Speaker 1:** The summer of forces in the XG direction.
[00:39:22:260 - 00:39:26:510] **Speaker 1:** Equals 0 We've got um.
[00:39:27:699 - 00:39:42:639] **Speaker 1:** -0.3932. We have -0.3932. And then we have +780.7864. It's
[00:39:42:639 - 00:39:43:500] **Speaker 1:** up to 0.
[00:39:44:570 - 00:39:44:919] **Speaker 1:** Is.
[00:39:48:540 - 00:39:50:179] **Speaker 1:** Some forces in the Y direction.
[00:39:52:709 - 00:40:02:219] **Speaker 1:** Upwards positive We have -28.8692. You have 100 at this
[00:40:02:219 - 00:40:02:550] **Speaker 1:** node.
[00:40:04:229 - 00:40:06:729] **Speaker 1:** We have -68.
[00:40:07:709 - 00:40:09:770] **Speaker 1:** 0.8798 at this node.
[00:40:10:600 - 00:40:16:739] **Speaker 1:** And we have -2.2510. Which also sums to 0 kilometons.
[00:40:20:320 - 00:40:21:949] **Speaker 1:** So we're kind of at about, you know.
[00:40:23:030 - 00:40:27:949] **Speaker 1:** 97.5 um with this you know with about -100 plus
[00:40:27:949 - 00:40:29:229] **Speaker 1:** 1000.
[00:40:30:820 - 00:40:33:340] **Speaker 1:** We'll also just quickly do some of moments about A
[00:40:33:540 - 00:40:36:300] **Speaker 1:** being equal to 0 and as is always the case,
[00:40:36:379 - 00:40:38:159] **Speaker 1:** we find anti-clockwise to be positive.
[00:40:39:429 - 00:40:41:709] **Speaker 1:** So around here we have a 100 kilonewton.
[00:40:42:000 - 00:40:45:179] **Speaker 1:** There's no moment here, and these forces don't contribute a
[00:40:45:179 - 00:40:45:590] **Speaker 1:** moment.
[00:40:45:870 - 00:40:48:449] **Speaker 1:** So we have 100 kilonewtons times 4.
[00:40:49:540 - 00:40:52:550] **Speaker 1:** And it's positive because it would contribute a counterclockwise moment
[00:40:52:550 - 00:40:53:229] **Speaker 1:** about A.
[00:40:54:379 - 00:40:56:100] **Speaker 1:** Then we have our.
[00:40:57:149 - 00:40:59:389] **Speaker 1:** This force here is a distance of 8 metres and
[00:40:59:389 - 00:41:01:330] **Speaker 1:** it will be clockwise, it will be negative.
[00:41:02:469 - 00:41:05:530] **Speaker 1:** 68.8798.
[00:41:07:469 - 00:41:07:929] **Speaker 1:** 8.
[00:41:09:560 - 00:41:11:379] **Speaker 1:** There's a force here, but that has no moment.
[00:41:11:750 - 00:41:12:580] **Speaker 1:** We add in the moment.
[00:41:13:479 - 00:41:15:159] **Speaker 1:** That's + 148.
[00:41:16:129 - 00:41:17:590] **Speaker 1:** 0.1145.
[00:41:19:689 - 00:41:21:629] **Speaker 1:** Then we end up with forces here, so we've got
[00:41:21:629 - 00:41:22:570] **Speaker 1:** a moment term.
[00:41:23:780 - 00:41:25:600] **Speaker 1:** Plus 8.78.
[00:41:27:050 - 00:41:27:870] **Speaker 1:** 20.
[00:41:28:760 - 00:41:31:199] **Speaker 1:** And both of these forces also contribute moments as well.
[00:41:31:719 - 00:41:38:239] **Speaker 1:** Uh, this one will be counterclockwise around A, so 0.7864.
[00:41:39:760 - 00:41:40:590] **Speaker 1:** Times 4.
[00:41:41:389 - 00:41:46:149] **Speaker 1:** And then we have +2.251. Times 4.
[00:41:47:409 - 00:41:48:800] **Speaker 1:** Which basically sums to.
[00:41:49:669 - 00:41:50:879] **Speaker 1:** 0 kilonewton metres.
[00:41:51:070 - 00:41:53:830] **Speaker 1:** So we just be confident that actually the structure uh
[00:41:53:830 - 00:41:56:750] **Speaker 1:** does work out to be in static equilibrium.
[00:42:04:229 - 00:42:06:459] **Speaker 1:** So we're gonna work through a couple of problems here.
[00:42:07:459 - 00:42:09:560] **Speaker 1:** Um, which are gonna be the kind of final problems
[00:42:09:560 - 00:42:13:449] **Speaker 1:** that we do with frame elements before we, uh, jump
[00:42:13:449 - 00:42:15:070] **Speaker 1:** into distributed loading next week.
[00:42:17:689 - 00:42:21:030] **Speaker 1:** So, um, what you see on page 104.
[00:42:21:889 - 00:42:23:320] **Speaker 1:** Is this good old matrix again?
[00:42:25:199 - 00:42:28:199] **Speaker 1:** Now this matrix is actually this table, it's just the
[00:42:28:199 - 00:42:30:360] **Speaker 1:** exact same table that was presented earlier in the notes,
[00:42:30:409 - 00:42:31:760] **Speaker 1:** it's just a direct repetition.
[00:42:32:639 - 00:42:35:409] **Speaker 1:** When we first presented this, it was related to bar
[00:42:35:409 - 00:42:35:989] **Speaker 1:** elements.
[00:42:37:020 - 00:42:39:409] **Speaker 1:** Now it's being presented within frame elements, and the fact
[00:42:39:409 - 00:42:42:219] **Speaker 1:** is that all the information on the table is completely
[00:42:42:219 - 00:42:42:649] **Speaker 1:** general.
[00:42:42:739 - 00:42:44:459] **Speaker 1:** It applies to all the element types.
[00:42:44:780 - 00:42:47:159] **Speaker 1:** Um, so there's nothing specific about that, which makes it
[00:42:47:260 - 00:42:47:739] **Speaker 1:** redundant.
[00:42:47:780 - 00:42:49:360] **Speaker 1:** So this is just repeating this table again.
[00:42:49:830 - 00:42:51:340] **Speaker 1:** It may have a little bit more meaning for you
[00:42:51:340 - 00:42:53:370] **Speaker 1:** now that you've had a little bit more time to
[00:42:54:020 - 00:42:56:020] **Speaker 1:** Get to know everything, um, just a little bit of
[00:42:56:020 - 00:42:56:679] **Speaker 1:** a reminder.
[00:42:57:469 - 00:43:02:110] **Speaker 1:** That's um yeah that's the information and the, the meaning
[00:43:02:110 - 00:43:03:850] **Speaker 1:** of each of the different stiffness equations.
[00:43:06:780 - 00:43:08:669] **Speaker 1:** So we've got now is this little portal frame.
[00:43:09:030 - 00:43:11:389] **Speaker 1:** So we've got an iron and a value, an elastic
[00:43:11:389 - 00:43:14:550] **Speaker 1:** modulus, and we've got some 3 metres high, 4.5 metres
[00:43:14:550 - 00:43:17:370] **Speaker 1:** wide, and we've got 210 kilometon loads on there.
[00:43:19:560 - 00:43:22:399] **Speaker 1:** Now, we can exclude degrees of freedom if we wanted
[00:43:22:399 - 00:43:22:659] **Speaker 1:** to.
[00:43:24:899 - 00:43:28:169] **Speaker 1:** So what we're gonna do here um is we're initially
[00:43:28:169 - 00:43:30:129] **Speaker 1:** gonna assume actual rigidity of the vertical members.
[00:43:30:280 - 00:43:32:550] **Speaker 1:** So when we look at the problem here, there's no
[00:43:32:550 - 00:43:33:750] **Speaker 1:** vertical loads applied.
[00:43:34:600 - 00:43:36:280] **Speaker 1:** Let's just ignore the vertical degrees of freedom.
[00:43:36:360 - 00:43:39:500] **Speaker 1:** Let's assume the elements are actually rigid, not include any
[00:43:39:500 - 00:43:44:479] **Speaker 1:** um vertical reaction, um, component because we're only applying loads
[00:43:44:479 - 00:43:45:419] **Speaker 1:** horizontally anyway.
[00:43:47:050 - 00:43:51:010] **Speaker 1:** Now quickly, There's no degrees of freedom.
[00:43:52:679 - 00:43:54:020] **Speaker 1:** Is fully fixed here.
[00:43:57:610 - 00:43:59:300] **Speaker 1:** And what we're going to do here is we're going
[00:43:59:300 - 00:44:00:120] **Speaker 1:** to say no.
[00:44:02:100 - 00:44:04:060] **Speaker 1:** Vertical degree of freedom.
[00:44:05:679 - 00:44:13:500] **Speaker 1:** As There are no Vertically applied.
[00:44:17:409 - 00:44:17:679] **Speaker 1:** Lawrence.
[00:44:19:330 - 00:44:19:629] **Speaker 1:** Here.
[00:44:24:510 - 00:44:25:790] **Speaker 1:** And this is what we're doing there.
[00:44:25:820 - 00:44:34:989] **Speaker 1:** It's essentially Forcing Fried melons.
[00:44:38:129 - 00:44:49:629] **Speaker 1:** To behave Like beam elements So we're gonna constrain out
[00:44:49:629 - 00:44:54:010] **Speaker 1:** the actual degree of freedom, essentially force them to um
[00:44:54:590 - 00:44:54:919] **Speaker 1:** remain.
[00:44:55:939 - 00:44:57:580] **Speaker 1:** Actually, Richard and.
[00:44:58:439 - 00:45:00:379] **Speaker 1:** Take the axial component out of the solution.
[00:45:02:370 - 00:45:05:209] **Speaker 1:** Now from here, once we've done that, the procedure's still
[00:45:05:209 - 00:45:06:550] **Speaker 1:** the same as it always has been.
[00:45:07:199 - 00:45:08:860] **Speaker 1:** Um, we can just work through.
[00:45:10:020 - 00:45:11:629] **Speaker 1:** Free diagram is always a key step.
[00:45:11:830 - 00:45:15:790] **Speaker 1:** We have our, um, relationship between degrees of freedom within
[00:45:15:790 - 00:45:18:429] **Speaker 1:** the elements, the overall structural degrees of freedom which then
[00:45:18:429 - 00:45:20:129] **Speaker 1:** generate our assembly matrices.
[00:45:22:360 - 00:45:25:360] **Speaker 1:** From that, we get all the intermediate results.
[00:45:25:840 - 00:45:28:520] **Speaker 1:** We put in our applied external forcing terms, which is
[00:45:28:520 - 00:45:32:760] **Speaker 1:** just These two loads given in our chosen numbering sequence.
[00:45:34:600 - 00:45:36:540] **Speaker 1:** Then we get out our solved affections.
[00:45:38:080 - 00:45:41:360] **Speaker 1:** And then we can go through the example here and
[00:45:41:719 - 00:45:44:280] **Speaker 1:** once we've solved them, we can work out the forcing
[00:45:44:280 - 00:45:46:379] **Speaker 1:** terms and then put them back onto the structure here.
[00:45:48:199 - 00:45:52:120] **Speaker 1:** And what you might see here is that things didn't
[00:45:52:120 - 00:45:53:360] **Speaker 1:** work out quite as planned.
[00:45:55:320 - 00:45:57:000] **Speaker 1:** So when it comes to this, what we essentially do
[00:45:57:000 - 00:45:58:820] **Speaker 1:** is take the 1st 3 components here.
[00:45:59:830 - 00:46:05:090] **Speaker 1:** They came down here Then we're taking these components of
[00:46:05:090 - 00:46:08:409] **Speaker 1:** the 4 to 6 for element 1 and 1 to
[00:46:08:409 - 00:46:09:679] **Speaker 1:** 3 for element 2.
[00:46:09:929 - 00:46:11:550] **Speaker 1:** We're bringing those down into here.
[00:46:13:669 - 00:46:17:290] **Speaker 1:** Then we're taking the, the second part of F2.
[00:46:18:209 - 00:46:20:270] **Speaker 1:** And the first part of F3.
[00:46:21:479 - 00:46:24:120] **Speaker 1:** We're bringing those down just based upon our elements.
[00:46:24:909 - 00:46:28:129] **Speaker 1:** Chosen element orientations, and then we're taking these pieces here.
[00:46:28:830 - 00:46:30:540] **Speaker 1:** And they come down to the sport there.
[00:46:33:030 - 00:46:35:189] **Speaker 1:** But what we end up seeing here is that we've
[00:46:35:189 - 00:46:38:189] **Speaker 1:** got vertical deflection, vertical force in terms.
[00:46:39:360 - 00:46:42:310] **Speaker 1:** That are available that come out here and here that
[00:46:42:310 - 00:46:43:489] **Speaker 1:** weren't there in the problem.
[00:46:43:989 - 00:46:47:070] **Speaker 1:** The initial problem only had these 210 kilonewton loads.
[00:46:47:189 - 00:46:48:800] **Speaker 1:** It didn't have these forces here.
[00:46:49:070 - 00:46:53:719] **Speaker 1:** So what we've actually ended up with Is a situation
[00:46:54:040 - 00:46:56:879] **Speaker 1:** where the structure has told us there was vertical forces
[00:46:56:879 - 00:46:59:360] **Speaker 1:** at those nodal points which didn't exist in the other
[00:46:59:360 - 00:47:00:419] **Speaker 1:** in the initial problem.
[00:47:02:639 - 00:47:05:659] **Speaker 1:** Well, what's happened here is that.
[00:47:06:679 - 00:47:09:439] **Speaker 1:** Applying the axial rigidity, ignoring those degrees of freedom has
[00:47:09:439 - 00:47:11:179] **Speaker 1:** actually had an unintended consequence.
[00:47:11:320 - 00:47:14:879] **Speaker 1:** So, um, the problem is antisymmetric, um, which leads to
[00:47:14:879 - 00:47:17:479] **Speaker 1:** similar reaction forces at the bases 1 and 3.
[00:47:17:560 - 00:47:19:439] **Speaker 1:** But what's actually gonna happen here if we push on
[00:47:19:439 - 00:47:21:409] **Speaker 1:** it is there'll be an axial force couple.
[00:47:21:510 - 00:47:23:520] **Speaker 1:** So there'll be a tension, we're pushing to the right,
[00:47:23:600 - 00:47:26:000] **Speaker 1:** there'll actually be a tension force in this column, and
[00:47:26:000 - 00:47:28:479] **Speaker 1:** there'll be a compression force in this column which will
[00:47:28:479 - 00:47:30:219] **Speaker 1:** help with an overturning moment.
[00:47:30:320 - 00:47:33:879] **Speaker 1:** And by not including those degrees of freedom, we have
[00:47:34:370 - 00:47:39:989] **Speaker 1:** Basically deprived the solution, the mathematical system of the capacity
[00:47:40:330 - 00:47:42:100] **Speaker 1:** to capture that reaction mechanism.
[00:47:42:409 - 00:47:45:610] **Speaker 1:** So, in doing so by making that simplification, we've actually
[00:47:45:610 - 00:47:49:610] **Speaker 1:** missed a key important part of this system.
[00:47:51:409 - 00:47:53:479] **Speaker 1:** So let's rework it and we'll take away that assumption,
[00:47:53:560 - 00:47:55:760] **Speaker 1:** we'll reintroduce those degrees of freedom and see how things
[00:47:55:760 - 00:47:56:300] **Speaker 1:** work out.
[00:47:59:219 - 00:48:02:379] **Speaker 1:** Same problem, same setup, same loads, but now we're also
[00:48:02:379 - 00:48:03:879] **Speaker 1:** gonna put a vertical degree of freedom.
[00:48:05:580 - 00:48:08:219] **Speaker 1:** So we've got fully fixed supports here, no degrees of
[00:48:08:219 - 00:48:08:639] **Speaker 1:** freedom.
[00:48:08:979 - 00:48:10:580] **Speaker 1:** We've got 3 degrees of freedom in each of those
[00:48:10:580 - 00:48:13:239] **Speaker 1:** two nodes, 6 degrees of freedom overall for the structure.
[00:48:16:469 - 00:48:18:189] **Speaker 1:** We end up, you know, we start with 3 blood
[00:48:18:189 - 00:48:19:010] **Speaker 1:** diagrams again.
[00:48:20:260 - 00:48:21:330] **Speaker 1:** Same way we always have.
[00:48:22:270 - 00:48:24:570] **Speaker 1:** We have now a few extra relationships here.
[00:48:25:560 - 00:48:29:229] **Speaker 1:** And what you see here is because we've worked, you
[00:48:29:229 - 00:48:32:040] **Speaker 1:** know, Q1, Q2, Q3, and X Y and Z, Q4,
[00:48:32:129 - 00:48:34:520] **Speaker 1:** Q5, Q 6 X Y and Z here, you know,
[00:48:34:560 - 00:48:36:360] **Speaker 1:** we don't have to apply this numbering sequence but it
[00:48:36:360 - 00:48:38:280] **Speaker 1:** is a relatively logical one.
[00:48:39:550 - 00:48:41:110] **Speaker 1:** And then if you look at the form of the
[00:48:41:110 - 00:48:43:070] **Speaker 1:** assembly matrices that result from that.
[00:48:43:939 - 00:48:45:669] **Speaker 1:** What we have here is a 6 by 6 matrix,
[00:48:45:709 - 00:48:48:820] **Speaker 1:** but we have essentially three submatrices which are all zeros,
[00:48:48:830 - 00:48:50:820] **Speaker 1:** and then we have a little submatrix which is uh
[00:48:50:820 - 00:48:52:149] **Speaker 1:** an identity matrix.
[00:48:52:709 - 00:48:56:000] **Speaker 1:** Then we have, um, the A2 is just an identity
[00:48:56:000 - 00:48:58:879] **Speaker 1:** matrix 6 by 6, and then we have this little
[00:48:58:879 - 00:48:59:750] **Speaker 1:** similar form there.
[00:48:59:870 - 00:49:02:909] **Speaker 1:** So by following a similar approach to the numbering sequences,
[00:49:03:219 - 00:49:05:270] **Speaker 1:** we end up with a semi matrix which are quite
[00:49:05:270 - 00:49:05:889] **Speaker 1:** a nice form.
[00:49:06:989 - 00:49:07:629] **Speaker 1:** We don't have to.
[00:49:07:750 - 00:49:08:909] **Speaker 1:** We could choose a different number of seconds.
[00:49:08:949 - 00:49:10:909] **Speaker 1:** It wouldn't make it wrong, uh, but it might just
[00:49:10:909 - 00:49:13:469] **Speaker 1:** be a little bit more onerous to enter all this
[00:49:13:469 - 00:49:13:669] **Speaker 1:** information.
[00:49:15:770 - 00:49:21:770] **Speaker 1:** So we worked through We have intermediate results, the forcing
[00:49:21:800 - 00:49:24:669] **Speaker 1:** reactor changes now because it's now 6 by 1 instead
[00:49:24:669 - 00:49:25:629] **Speaker 1:** of a 4 by 1.
[00:49:26:070 - 00:49:27:889] **Speaker 1:** We now get 6 deflection components.
[00:49:29:290 - 00:49:31:810] **Speaker 1:** And then we end up with these forcing terms that
[00:49:31:810 - 00:49:32:439] **Speaker 1:** result from that.
[00:49:33:679 - 00:49:36:179] **Speaker 1:** So just like before, uh, these 1st 3.
[00:49:37:050 - 00:49:38:669] **Speaker 1:** Come down to here.
[00:49:40:110 - 00:49:42:979] **Speaker 1:** These last 3 here, come down to here.
[00:49:45:229 - 00:49:49:479] **Speaker 1:** The space And this piece onto this node.
[00:49:50:729 - 00:49:54:530] **Speaker 1:** And This pace at this pace.
[00:49:55:540 - 00:49:56:449] **Speaker 1:** Come into this node.
[00:49:58:739 - 00:50:01:540] **Speaker 1:** What we end up with is some slightly different reactions.
[00:50:01:620 - 00:50:04:979] **Speaker 1:** We've now got 10 kilotons on each, um, support point.
[00:50:05:340 - 00:50:06:959] **Speaker 1:** We now have some axial forces here.
[00:50:07:739 - 00:50:09:739] **Speaker 1:** So while they were previously up there, they will end
[00:50:09:739 - 00:50:12:340] **Speaker 1:** up with non-zero values there, we've got back to zero
[00:50:12:340 - 00:50:12:919] **Speaker 1:** values.
[00:50:13:699 - 00:50:16:199] **Speaker 1:** So there's gonna be a sheer force carried through here
[00:50:16:379 - 00:50:17:979] **Speaker 1:** and that shear force is going to be transmitted into
[00:50:17:979 - 00:50:19:719] **Speaker 1:** axial forces in the two columns.
[00:50:20:139 - 00:50:24:209] **Speaker 1:** We've now given that, um, the mathematical system the ability
[00:50:24:209 - 00:50:27:659] **Speaker 1:** to recognise this force couple and then everything matches the
[00:50:27:659 - 00:50:31:620] **Speaker 1:** original problem and essentially everything's good in the world again.
[00:50:32:060 - 00:50:34:129] **Speaker 1:** So, uh, that's just a quick example of some of
[00:50:34:129 - 00:50:37:340] **Speaker 1:** the simplifications you can make, but being wary when you
[00:50:37:340 - 00:50:38:899] **Speaker 1:** do so, um.
[00:50:39:229 - 00:50:40:310] **Speaker 1:** Thank you all for coming along.
[00:50:40:629 - 00:50:42:189] **Speaker 1:** What we're gonna do on Monday is jump into distributed
[00:50:42:189 - 00:50:45:659] **Speaker 1:** loading and finish up some of these aspects, so thank
[00:50:45:659 - 00:50:47:129] **Speaker 1:** you all and I'll see you again on Monday.
[00:51:00:899 - 00:51:00:909] **Speaker 0:** Yeah.
[00:51:03:370 - 00:51:03:379] **Speaker 0:** It.
[00:51:11:100 - 00:51:11:110] **Speaker 0:** It.
[00:51:17:520 - 00:51:17:530] **Speaker 0:** right.
[00:51:29:969 - 00:51:40:520] **Speaker 0:** Because That that's down.
[00:51:42:110 - 00:51:43:110] **Speaker 0:** Isn't you guys distributor.
[00:51:47:969 - 00:51:54:229] **Speaker 0:** Um, it's not something that's all that easy, um, I
[00:51:54:229 - 00:51:57:030] **Speaker 0:** mean, I guess if the sport's sufficiently strong, then you
[00:51:57:030 - 00:51:58:909] **Speaker 0:** could just kind of, you know, essentially treat it as
[00:51:58:909 - 00:52:00:250] **Speaker 0:** a support.
[00:52:06:510 - 00:52:13:229] **Speaker 0:** I mean, I guess, I mean, what you could do
[00:52:13:229 - 00:52:16:669] **Speaker 1:** is simplify it where you've got the, the, say something
[00:52:16:669 - 00:52:21:750] **Speaker 0:** like this, you have your some sort of cantilever you've
[00:52:21:750 - 00:52:22:649] **Speaker 0:** got say world along here.
[00:52:23:405 - 00:52:23:935] **Speaker 0:** And you got a sip.
[00:52:25:254 - 00:52:29:614] **Speaker 0:** You could model this as a cantilever beam that looks
[00:52:29:614 - 00:52:32:655] **Speaker 0:** like this, um, and then you're gonna end up with
[00:52:32:655 - 00:52:34:155] **Speaker 0:** the, the sheer force in a moment.
[00:52:35:715 - 00:52:37:975] **Speaker 0:** And then you better use this moment and then this,
[00:52:38:175 - 00:52:41:415] **Speaker 0:** the I believe of this world to say, you know,
[00:52:41:614 - 00:52:44:014] **Speaker 1:** from the simplified value I've got this moment and now
[00:52:44:014 - 00:52:46:665] **Speaker 0:** we need to design this well to be capable of
[00:52:46:665 - 00:52:47:495] **Speaker 0:** standing that moment.
[00:52:53:689 - 00:52:55:050] **Speaker 1:** Uh, so the shear's gonna be this way.
[00:52:55:169 - 00:52:58:280] **Speaker 0:** So I mean that's the shears, if it's downwards, um,
[00:52:58:290 - 00:53:00:169] **Speaker 1:** it's gonna be primarily in sort of a bearing on
[00:53:00:169 - 00:53:00:550] **Speaker 0:** this.
[00:53:01:189 - 00:53:02:969] **Speaker 0:** Um, there'll be a tension.
[00:53:04:449 - 00:53:11:929] **Speaker 1:** It will, yeah, and there'll be, yes, you'd have to
[00:53:11:929 - 00:53:14:330] **Speaker 1:** look at this well just get a basically a force
[00:53:14:330 - 00:53:17:750] **Speaker 1:** if the, if the force could be upwards, um.
[00:53:20:739 - 00:53:22:300] **Speaker 1:** If the force could be upwards, you'd have to look
[00:53:22:300 - 00:53:23:580] **Speaker 1:** at the tension force in here.
[00:53:24:179 - 00:53:26:260] **Speaker 1:** Uh, otherwise, they actually probably tension here.
[00:53:26:379 - 00:53:27:620] **Speaker 1:** There'll be some compression force here.
[00:53:27:820 - 00:53:31:540] **Speaker 1:** Um, you're basically looking at a bending load that's induced
[00:53:31:540 - 00:53:32:280] **Speaker 1:** on this well.
[00:53:34:030 - 00:53:35:590] **Speaker 1:** of the world and there's not.
[00:53:36:219 - 00:53:40:800] **Speaker 0:** And It's not like any kind of The only thing
[00:53:40:800 - 00:53:42:419] **Speaker 0:** you do is essentially just do FBA.
[00:53:45:270 - 00:53:46:489] **Speaker 0:** Fixed support points going.
[00:53:47:610 - 00:53:51:270] **Speaker 1:** Yeah, um, I mean what they sometimes do in structural
[00:53:51:270 - 00:53:53:750] **Speaker 1:** analysis because it's sitting on soil and so it's quite
[00:53:53:750 - 00:53:54:270] **Speaker 1:** flexible.
[00:53:54:929 - 00:53:57:080] **Speaker 1:** So sometimes you'll see like for a structure, you might
[00:53:57:080 - 00:53:59:409] **Speaker 1:** actually have like a set of springs they'll do like
[00:53:59:409 - 00:54:03:850] **Speaker 1:** a whole series of springs with different spring constants and
[00:54:03:850 - 00:54:05:379] **Speaker 1:** then this will be on a fixed support.
[00:54:06:010 - 00:54:08:850] **Speaker 1:** And it just accommodates the fact that you've actually got
[00:54:08:850 - 00:54:11:050] **Speaker 1:** kind of, you know, the exact stiffness you use on
[00:54:11:050 - 00:54:13:449] **Speaker 1:** these is quite difficult because it obviously depends on this
[00:54:13:449 - 00:54:13:620] **Speaker 1:** and.
[00:54:14:830 - 00:54:17:399] **Speaker 1:** some approximations there, um, but then you can actually more
[00:54:17:399 - 00:54:20:800] **Speaker 1:** of a distributed load because it won't always necessarily be
[00:54:20:800 - 00:54:23:280] **Speaker 1:** against this, it will actually, yeah, you see, actually see
[00:54:23:280 - 00:54:24:550] **Speaker 1:** a distribution of force across here.
[00:54:26:479 - 00:54:28:040] **Speaker 1:** So that is one option, um.
[00:54:28:679 - 00:54:32:760] **Speaker 1:** It's probably a bit more complicated and this was just
[00:54:32:760 - 00:54:35:620] **Speaker 0:** on the seat I assume from your lecture just before
[00:54:36:590 - 00:54:36:840] **Speaker 0:** thanks.
[00:54:54:260 - 00:54:54:270] **Speaker 0:** OK

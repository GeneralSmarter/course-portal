# ENME302-26S2 Lecture 10 native Echo transcript

Date: July 29, 2026 11:00am-11:55am
Transcript type: native Echo automated transcript.

[00:00:00:360 - 00:00:00:370] **Speaker 0:** I.
[00:00:03:319 - 00:00:03:329] **Speaker 0:** I.
[00:00:10:270 - 00:00:10:279] **Speaker 0:** Yeah.
[00:00:18:120 - 00:00:18:129] **Speaker 0:** Right.
[00:00:19:639 - 00:00:19:649] **Speaker 0:** I.
[00:00:22:889 - 00:00:22:899] **Speaker 0:** I.
[00:00:29:799 - 00:00:29:809] **Speaker 0:** Oh.
[00:00:43:549 - 00:00:43:560] **Speaker 0:** I.
[00:00:57:560 - 00:01:13:720] **Speaker 0:** Let's, let's But Well, karakoto, welcome along, everyone.
[00:01:16:199 - 00:01:17:430] **Speaker 1:** Two things we're gonna cover today.
[00:01:19:790 - 00:01:22:430] **Speaker 1:** So the first thing is we, we started out yesterday
[00:01:22:430 - 00:01:24:489] **Speaker 1:** looking at frame elements, sorry, on Monday.
[00:01:25:610 - 00:01:29:489] **Speaker 1:** And we looked at the, the deformations that we, we're
[00:01:29:489 - 00:01:29:930] **Speaker 1:** gonna model.
[00:01:30:050 - 00:01:32:089] **Speaker 1:** So that was the key things that we looked at.
[00:01:32:290 - 00:01:35:190] **Speaker 1:** Um, the idea is that we're actually working towards stiffness
[00:01:35:449 - 00:01:37:889] **Speaker 1:** and what we did is we look at 4 deflected
[00:01:37:889 - 00:01:41:089] **Speaker 1:** shapes and what we're doing is we're applying a unit
[00:01:41:089 - 00:01:44:849] **Speaker 1:** displacement in each of them and then, um, the force
[00:01:44:849 - 00:01:47:410] **Speaker 1:** that it takes to achieve that unit displacement will also
[00:01:47:410 - 00:01:49:529] **Speaker 1:** by definition be a stiffness just because it is a
[00:01:49:529 - 00:01:50:370] **Speaker 1:** unit displacement.
[00:01:50:569 - 00:01:54:040] **Speaker 1:** So what we started off with was 4 was, um,
[00:01:54:050 - 00:01:55:129] **Speaker 1:** this generic.
[00:01:55:730 - 00:01:56:809] **Speaker 1:** 3 or a polynomial.
[00:01:57:809 - 00:01:59:650] **Speaker 1:** And then what we do is we worked through it
[00:01:59:650 - 00:02:03:610] **Speaker 1:** and we um We only did this one, but you
[00:02:03:610 - 00:02:05:309] **Speaker 1:** know, the same process applies to all four.
[00:02:05:730 - 00:02:08:770] **Speaker 1:** We we're gonna work out the specific constants that relate
[00:02:08:770 - 00:02:09:820] **Speaker 1:** to each of those four shapes.
[00:02:09:960 - 00:02:12:050] **Speaker 1:** So what are the values of A through D that
[00:02:12:050 - 00:02:15:169] **Speaker 1:** match these four shapes, and then from that we'll work
[00:02:15:169 - 00:02:16:490] **Speaker 1:** on that to get the stiffness values.
[00:02:16:649 - 00:02:18:809] **Speaker 1:** So we're gonna do that, we're gonna work through that
[00:02:18:809 - 00:02:20:889] **Speaker 1:** final step to actually get the stiffness values that correspond
[00:02:20:889 - 00:02:21:300] **Speaker 1:** for a beam.
[00:02:22:320 - 00:02:23:699] **Speaker 1:** Then we're gonna work through a couple of very quick
[00:02:23:699 - 00:02:26:089] **Speaker 1:** examples with beams, and then we're gonna move on to
[00:02:26:089 - 00:02:29:289] **Speaker 1:** the more general frame elements which also include the axial
[00:02:29:289 - 00:02:30:050] **Speaker 1:** deformations.
[00:02:30:289 - 00:02:32:850] **Speaker 1:** And once we get to that, those frame elements are
[00:02:32:850 - 00:02:35:610] **Speaker 1:** the most general type that we're gonna cover within these
[00:02:35:610 - 00:02:38:250] **Speaker 1:** 4 weeks, so that's gonna essentially be the the most
[00:02:38:250 - 00:02:39:169] **Speaker 1:** complex thing we get to.
[00:02:40:770 - 00:02:43:789] **Speaker 1:** So these are the four shapes here, we worked through
[00:02:44:250 - 00:02:47:690] **Speaker 1:** the, the second of those, we applied our four boundary
[00:02:47:690 - 00:02:50:130] **Speaker 1:** conditions which model the shape and then we worked through
[00:02:50:130 - 00:02:52:770] **Speaker 1:** and we determined what our constants need to be to
[00:02:52:770 - 00:02:57:369] **Speaker 1:** turn the generic polynomial there into the specific one that
[00:02:57:369 - 00:02:58:850] **Speaker 1:** matches that shape.
[00:03:00:740 - 00:03:03:100] **Speaker 1:** Now we didn't do it, work through the, the process
[00:03:03:100 - 00:03:05:289] **Speaker 1:** for the other 3, but it's the exact same process.
[00:03:05:380 - 00:03:06:899] **Speaker 1:** We worked through this one, we could do the exact
[00:03:06:899 - 00:03:09:600] **Speaker 1:** same process with just different boundary conditions and we would
[00:03:09:600 - 00:03:10:720] **Speaker 1:** get the other 3 as well.
[00:03:11:729 - 00:03:16:080] **Speaker 1:** So those are the four specific equations which match the
[00:03:16:080 - 00:03:19:399] **Speaker 1:** three deflected, the four deflected shapes that are given on
[00:03:19:399 - 00:03:20:539] **Speaker 1:** page 67.
[00:03:21:000 - 00:03:25:639] **Speaker 1:** Now, what we had with our axial deformations was the
[00:03:25:639 - 00:03:28:160] **Speaker 1:** U of X was the internal axial deflection anywhere along
[00:03:28:160 - 00:03:30:440] **Speaker 1:** an element, and that was equal to psi of x
[00:03:30:440 - 00:03:32:000] **Speaker 1:** times our deflection vector D.
[00:03:32:759 - 00:03:34:210] **Speaker 1:** So now we have this V of X which is
[00:03:34:210 - 00:03:37:449] **Speaker 1:** the transverse reflection rather than the axial, and it's equal
[00:03:37:449 - 00:03:40:679] **Speaker 1:** to n which is our shape functions, our transverse shape
[00:03:40:679 - 00:03:42:369] **Speaker 1:** functions are the ones that are given above, we've just
[00:03:42:369 - 00:03:45:729] **Speaker 1:** derived those, and then D is our affection vector based
[00:03:45:729 - 00:03:47:350] **Speaker 1:** upon the element numbering sequence.
[00:03:49:429 - 00:03:51:830] **Speaker 1:** So as I mentioned on Monday that this is all
[00:03:51:830 - 00:03:53:130] **Speaker 1:** based upon small motions.
[00:03:53:589 - 00:03:54:669] **Speaker 1:** When we did the derivation.
[00:03:55:800 - 00:04:00:699] **Speaker 1:** We simplified the solution by assuming that here that these
[00:04:01:039 - 00:04:04:440] **Speaker 1:** terms the DX 2 and DV by DX, uh, the
[00:04:04:440 - 00:04:06:679] **Speaker 1:** second order terms that squared values, so if if the
[00:04:06:679 - 00:04:09:240] **Speaker 1:** value's small, the squared value's gonna go to zero much
[00:04:09:240 - 00:04:09:559] **Speaker 1:** quicker.
[00:04:10:529 - 00:04:13:589] **Speaker 1:** So, that is an implicit assumption what we're doing.
[00:04:16:250 - 00:04:21:450] **Speaker 1:** And we are using the uh Euler-Bernoulli beam bending theory
[00:04:21:450 - 00:04:23:529] **Speaker 1:** so the aspect ratio has to be greater than 5
[00:04:23:529 - 00:04:24:290] **Speaker 1:** to 10:1.
[00:04:24:769 - 00:04:27:649] **Speaker 1:** Um, it's not applicable to short squat elements and the
[00:04:27:649 - 00:04:30:089] **Speaker 1:** reason for that is what we discussed on Monday, which
[00:04:30:089 - 00:04:32:609] **Speaker 1:** is we're ignoring the sheer component of deflection.
[00:04:33:640 - 00:04:36:049] **Speaker 1:** And if the bar, the beam is long and slender,
[00:04:36:440 - 00:04:41:079] **Speaker 1:** then this is gonna give inconsequential deformations relative to this
[00:04:41:079 - 00:04:41:359] **Speaker 1:** one.
[00:04:41:640 - 00:04:43:880] **Speaker 1:** But if the beam is short and squat, these may
[00:04:43:880 - 00:04:45:940] **Speaker 1:** actually be significant relative to this.
[00:04:46:480 - 00:04:49:679] **Speaker 1:** Um, the solution we do with that is a Tymoshenko
[00:04:49:679 - 00:04:51:760] **Speaker 1:** element, which is very similar to the one we have,
[00:04:51:799 - 00:04:53:679] **Speaker 1:** but it's just got some extra components in there, and
[00:04:53:679 - 00:04:55:000] **Speaker 1:** we will look at that before the end of next
[00:04:55:000 - 00:04:55:279] **Speaker 1:** week.
[00:04:58:579 - 00:05:01:500] **Speaker 1:** The transverse deflection component can only be weighted combinations of
[00:05:01:500 - 00:05:02:559] **Speaker 1:** those shape functions.
[00:05:03:220 - 00:05:05:899] **Speaker 1:** So this page, which is page 70, was just the
[00:05:05:899 - 00:05:09:799] **Speaker 1:** um, The summary of those four and then just some
[00:05:09:799 - 00:05:13:540] **Speaker 1:** random values, you know, literallyly large values, um, to say,
[00:05:14:920 - 00:05:16:920] **Speaker 1:** Look what the different shapes were and then we had
[00:05:16:920 - 00:05:18:390] **Speaker 1:** this, you know, if we had some complex behaviour like
[00:05:18:390 - 00:05:18:480] **Speaker 1:** this.
[00:05:20:320 - 00:05:22:720] **Speaker 1:** The one element we've derived is not capable of capturing
[00:05:22:720 - 00:05:24:559] **Speaker 1:** that, but if we were to break it up into
[00:05:24:559 - 00:05:27:640] **Speaker 1:** many elements, then that would be capable of capturing that
[00:05:27:950 - 00:05:28:399] **Speaker 1:** behaviour.
[00:05:30:450 - 00:05:32:980] **Speaker 1:** So that's kind of the underlying premise of Fin Elements.
[00:05:34:489 - 00:05:38:720] **Speaker 1:** Um, that one simple, easy to define building block can
[00:05:38:739 - 00:05:40:000] **Speaker 1:** model something much greater.
[00:05:41:100 - 00:05:43:700] **Speaker 1:** Um, what we finally finished off on Monday was this
[00:05:43:700 - 00:05:46:380] **Speaker 1:** that we have this one simple element here, uh, with
[00:05:46:380 - 00:05:47:839] **Speaker 1:** two nodes and 4 degrees of freedom.
[00:05:48:179 - 00:05:50:260] **Speaker 1:** We could go to an element that has 3 nodes,
[00:05:50:459 - 00:05:52:619] **Speaker 1:** so it has essentially puts a nodal point halfway along
[00:05:52:619 - 00:05:55:570] **Speaker 1:** the element that would introduce an extra 2 degrees of
[00:05:55:570 - 00:05:55:920] **Speaker 1:** freedom.
[00:05:56:760 - 00:05:58:239] **Speaker 1:** We'd then have 6 boundary conditions.
[00:05:58:320 - 00:06:00:959] **Speaker 1:** We'd be able to evaluate a 5th order polynomial that
[00:06:00:959 - 00:06:03:480] **Speaker 1:** could fit that, and we'd be able to model more
[00:06:03:480 - 00:06:05:260] **Speaker 1:** complex reaction mechanisms.
[00:06:05:959 - 00:06:08:920] **Speaker 1:** But of course, the element itself is more computationally expensive.
[00:06:08:959 - 00:06:12:839] **Speaker 1:** It's more complicated to drive and, and modify, and this
[00:06:12:839 - 00:06:16:600] **Speaker 1:** is the standard trade-off that exists within final element analysis
[00:06:16:600 - 00:06:19:799] **Speaker 1:** is you can either use a smaller number of more
[00:06:19:799 - 00:06:22:859] **Speaker 1:** complex elements or a larger number of more simple elements.
[00:06:23:200 - 00:06:25:440] **Speaker 1:** And computationally, it kind of works out to be the
[00:06:25:440 - 00:06:26:760] **Speaker 1:** same thing, so.
[00:06:27:910 - 00:06:29:529] **Speaker 1:** That's the, the broader context.
[00:06:30:929 - 00:06:32:739] **Speaker 1:** So we've gone through, we have our shape functions, we
[00:06:32:739 - 00:06:35:459] **Speaker 1:** have our deflected shapes, but we don't yet have values
[00:06:35:459 - 00:06:36:239] **Speaker 1:** for stiffness.
[00:06:37:890 - 00:06:41:209] **Speaker 1:** So what we need here is shape functions, use the
[00:06:41:209 - 00:06:43:649] **Speaker 1:** shape functions to generate stiffness values.
[00:06:43:929 - 00:06:47:089] **Speaker 1:** So we go back to a source equation 8, which
[00:06:47:089 - 00:06:48:190] **Speaker 1:** was a few pages prior.
[00:06:48:989 - 00:06:52:839] **Speaker 1:** And this is the um The equation that we had
[00:06:52:839 - 00:06:53:000] **Speaker 1:** here.
[00:06:53:079 - 00:06:56:380] **Speaker 1:** So it's the principal virtual displacement supplied um times EI
[00:06:56:790 - 00:07:00:279] **Speaker 1:** times the 2nd derivative of our virtual displacement, EI times
[00:07:00:279 - 00:07:04:399] **Speaker 1:** the 2nd derivative of uh transverse deflection, and that's equal
[00:07:04:399 - 00:07:10:160] **Speaker 1:** to the incremental version of our, um, deflection vector times
[00:07:10:160 - 00:07:11:579] **Speaker 1:** the applied external forces.
[00:07:12:690 - 00:07:15:549] **Speaker 1:** Now this year, we've already seen this equation um in
[00:07:15:549 - 00:07:18:450] **Speaker 1:** the Previous form.
[00:07:18:850 - 00:07:27:510] **Speaker 1:** So this is essentially Just V X equals N times
[00:07:27:510 - 00:07:27:850] **Speaker 1:** D.
[00:07:30:410 - 00:07:31:079] **Speaker 1:** For the island.
[00:07:36:200 - 00:07:37:910] **Speaker 1:** But in an incremental sense.
[00:07:40:470 - 00:07:42:579] **Speaker 1:** Little incremental virtual displacement.
[00:07:43:600 - 00:07:48:950] **Speaker 1:** Is equal to um the end times the, Uh, incremental
[00:07:49:440 - 00:07:52:309] **Speaker 1:** deflection, and then we can take the derivative of that.
[00:07:53:290 - 00:07:54:130] **Speaker 1:** That's given here.
[00:07:56:049 - 00:07:59:049] **Speaker 1:** Now we can substitute that into our equation and then
[00:07:59:049 - 00:07:59:890] **Speaker 1:** group terms here.
[00:08:01:940 - 00:08:04:140] **Speaker 1:** And what I want you to look at here is
[00:08:04:140 - 00:08:05:619] **Speaker 1:** we take this equation.
[00:08:07:779 - 00:08:10:890] **Speaker 1:** The first thing we can do There's there's a delta
[00:08:10:890 - 00:08:13:690] **Speaker 1:** DT here and there's a delta DT there.
[00:08:13:980 - 00:08:15:489] **Speaker 1:** So that's a common factor for both sides of the
[00:08:15:489 - 00:08:17:670] **Speaker 1:** equation, so we can just cancel that out.
[00:08:19:570 - 00:08:21:410] **Speaker 1:** Once we've done that, there's a whole lot of symbols
[00:08:21:410 - 00:08:21:950] **Speaker 1:** in there.
[00:08:22:730 - 00:08:24:010] **Speaker 1:** Don't get too hung up on that just now, I
[00:08:24:010 - 00:08:25:250] **Speaker 1:** want you to take a step back and just look
[00:08:25:250 - 00:08:25:970] **Speaker 1:** at this equation.
[00:08:27:350 - 00:08:29:809] **Speaker 1:** So we've done this before with another element.
[00:08:31:230 - 00:08:32:510] **Speaker 1:** I just want you to look at the form of
[00:08:32:510 - 00:08:33:190] **Speaker 1:** this equation.
[00:08:38:659 - 00:08:41:219] **Speaker 1:** So we've got a bunch of stuff in a bracket.
[00:08:42:148 - 00:08:43:119] **Speaker 1:** Times to fiction.
[00:08:44:190 - 00:08:49:479] **Speaker 1:** Is equal to force So what that means is that
[00:08:50:750 - 00:08:57:869] **Speaker 1:** All of this stuff Within the brackets.
[00:09:03:960 - 00:09:05:239] **Speaker 1:** Represents stiffness.
[00:09:10:270 - 00:09:11:650] **Speaker 1:** So just like we had before.
[00:09:12:690 - 00:09:14:030] **Speaker 1:** Basically that bracketed term.
[00:09:15:010 - 00:09:17:530] **Speaker 1:** Is the definition of our stiffness matrix because that's the
[00:09:17:530 - 00:09:20:450] **Speaker 1:** thing that relates applied loads to the corresponding deflections.
[00:09:20:650 - 00:09:23:049] **Speaker 1:** So we take that bracketed term and that is by
[00:09:23:049 - 00:09:29:369] **Speaker 1:** definition, our stiffness matrix for a um for a beam
[00:09:29:369 - 00:09:29:789] **Speaker 1:** element.
[00:09:31:520 - 00:09:34:340] **Speaker 1:** Now that that isn't yet at a point where we
[00:09:34:340 - 00:09:36:059] **Speaker 1:** can start coding things into Python.
[00:09:36:919 - 00:09:38:400] **Speaker 1:** We need to actually work through and work out what
[00:09:38:400 - 00:09:39:239] **Speaker 1:** the actual numbers are.
[00:09:39:409 - 00:09:42:239] **Speaker 1:** So we've got kind of a conceptual definition here, but
[00:09:42:239 - 00:09:43:429] **Speaker 1:** we need to work through and work out how to
[00:09:43:429 - 00:09:44:080] **Speaker 1:** actually do this.
[00:09:44:330 - 00:09:47:789] **Speaker 1:** So The 4 shape functions here, these are the ones
[00:09:47:789 - 00:09:49:809] **Speaker 1:** that we, we just arrived.
[00:09:51:489 - 00:09:53:530] **Speaker 1:** Um, the 4 different shapes that were back on page
[00:09:53:530 - 00:09:56:530] **Speaker 1:** 67, and then we take the second derivative of those
[00:09:56:530 - 00:09:58:969] **Speaker 1:** with respect to X, and then we get these values
[00:09:58:969 - 00:09:59:250] **Speaker 1:** there.
[00:10:02:039 - 00:10:04:359] **Speaker 1:** So those are key reference steps because like the things
[00:10:04:359 - 00:10:06:840] **Speaker 1:** that we're going to be substituting into our equation is
[00:10:06:840 - 00:10:08:640] **Speaker 1:** the, the 2nd derivatives here.
[00:10:26:989 - 00:10:29:349] **Speaker 1:** So we're gonna look at the IJF component of the
[00:10:29:349 - 00:10:30:719] **Speaker 1:** KE matrix, so.
[00:10:31:570 - 00:10:32:380] **Speaker 1:** What this means.
[00:10:35:530 - 00:10:36:849] **Speaker 1:** This is the stiffness term.
[00:10:42:450 - 00:10:55:960] **Speaker 1:** That sits In The I throw And the JIFF column.
[00:10:58:479 - 00:11:00:599] **Speaker 1:** Of our stiffness matrix, KE.
[00:11:07:840 - 00:11:16:679] **Speaker 1:** So what we have here This is The transpose.
[00:11:22:530 - 00:11:24:309] **Speaker 1:** of the second derivative.
[00:11:33:359 - 00:11:35:760] **Speaker 1:** Of the I shape function.
[00:11:39:739 - 00:11:41:359] **Speaker 1:** That, of course, is with respect.
[00:11:42:270 - 00:11:43:770] **Speaker 1:** 2 weeks that the derivative is done.
[00:11:46:099 - 00:11:48:989] **Speaker 1:** And then what we have here is the 2nd derivative
[00:11:48:989 - 00:11:52:369] **Speaker 1:** with respect to X of the Jake shape function.
[00:11:54:479 - 00:11:56:390] **Speaker 1:** So we're gonna work through an example here.
[00:11:56:690 - 00:11:59:909] **Speaker 1:** We're gonna bring ENI outside the integral.
[00:12:00:320 - 00:12:09:020] **Speaker 1:** So in doing that, We are assuming He and I
[00:12:13:419 - 00:12:16:799] **Speaker 1:** A constant Along the element.
[00:12:22:479 - 00:12:24:549] **Speaker 1:** So what we could do here, if we had an
[00:12:24:549 - 00:12:27:070] **Speaker 1:** element that had a a varying cross section so that
[00:12:27:070 - 00:12:30:750] **Speaker 1:** the, the second moment of area I varied with position
[00:12:30:750 - 00:12:33:109] **Speaker 1:** on the bar X, we could incorporate that into the
[00:12:33:109 - 00:12:33:809] **Speaker 1:** integral.
[00:12:34:260 - 00:12:37:070] **Speaker 1:** Equally, if we had some sort of non-homogeneous bar where
[00:12:37:070 - 00:12:39:500] **Speaker 1:** the material properties and the elastic modules changed along the
[00:12:39:500 - 00:12:42:030] **Speaker 1:** bar, if we had a function which defined that, we
[00:12:42:030 - 00:12:44:390] **Speaker 1:** could include that within the integral and we would get
[00:12:44:390 - 00:12:46:039] **Speaker 1:** stiffness terms that captured that.
[00:12:46:299 - 00:12:49:630] **Speaker 1:** But of course, um, that would be then a very
[00:12:49:630 - 00:12:51:869] **Speaker 1:** specific element that wouldn't generalise very nicely.
[00:12:52:090 - 00:12:53:409] **Speaker 1:** And it would be of limited use to us.
[00:12:53:570 - 00:12:56:280] **Speaker 1:** So in situations, maybe if you were doing something really
[00:12:56:280 - 00:12:59:289] **Speaker 1:** specific and you had a very particular type of element,
[00:12:59:489 - 00:13:02:849] **Speaker 1:** you could actually derive yourself of an element, stiffness matrix
[00:13:02:849 - 00:13:06:590] **Speaker 1:** that captured that, but that's very niche for an application.
[00:13:06:729 - 00:13:09:369] **Speaker 1:** So to keep it general, we're just gonna assume E
[00:13:09:369 - 00:13:11:669] **Speaker 1:** and I are constant, bring that outside the integral.
[00:13:14:969 - 00:13:19:130] **Speaker 1:** So the first thing here This is NI.
[00:13:21:710 - 00:13:23:549] **Speaker 1:** X, and then this here.
[00:13:24:349 - 00:13:26:770] **Speaker 1:** Is N J X.
[00:13:30:869 - 00:13:33:750] **Speaker 1:** So that in this case is N2 of X.
[00:13:34:650 - 00:13:37:280] **Speaker 1:** And so because this is the 22 element, so it's
[00:13:37:280 - 00:13:40:130] **Speaker 1:** the second row, second column, that is also equal to
[00:13:40:130 - 00:13:41:679] **Speaker 1:** N2 of X.
[00:13:45:609 - 00:13:47:349] **Speaker 1:** Now one thing that's important to realise here.
[00:13:49:809 - 00:13:51:320] **Speaker 1:** If we were to reverse.
[00:13:53:510 - 00:13:54:840] **Speaker 1:** The two bracketed terms.
[00:14:07:929 - 00:14:09:450] **Speaker 1:** We would still get the same answer.
[00:14:15:950 - 00:14:17:500] **Speaker 1:** So if we were to take those two bracketed terms,
[00:14:17:580 - 00:14:19:500] **Speaker 1:** we were just to switch them, the 2nd 1 1st
[00:14:19:500 - 00:14:20:500] **Speaker 1:** and the 1st 1 2nd.
[00:14:20:900 - 00:14:22:760] **Speaker 1:** The final answer here isn't going to change.
[00:14:23:659 - 00:14:24:580] **Speaker 1:** Now why is that significant?
[00:14:24:739 - 00:14:26:059] **Speaker 1:** Why am I making a big deal out of that?
[00:14:27:190 - 00:14:31:039] **Speaker 1:** All that tells us is that KIJ within the matrix.
[00:14:32:359 - 00:14:33:950] **Speaker 1:** Must be equal to KJI.
[00:14:36:950 - 00:14:43:250] **Speaker 1:** And that tells us That The stiffness matrix overall.
[00:14:48:520 - 00:14:49:500] **Speaker 1:** Must be symmetrical.
[00:14:57:570 - 00:14:59:450] **Speaker 1:** So when you're coding this up, we'll, we'll get to
[00:14:59:450 - 00:15:01:650] **Speaker 1:** the, the frame element version, but in the lay of
[00:15:01:650 - 00:15:02:969] **Speaker 1:** this week you are actually gonna have to enter a
[00:15:02:969 - 00:15:04:969] **Speaker 1:** 6x6 matrix into Python.
[00:15:05:489 - 00:15:07:049] **Speaker 1:** You don't even have to do that once, so don't
[00:15:07:049 - 00:15:09:570] **Speaker 1:** worry too much about it, but you are entering 36
[00:15:09:570 - 00:15:10:690] **Speaker 1:** numbers into that matrix.
[00:15:10:969 - 00:15:12:890] **Speaker 1:** It's pretty easy to maybe drop a negative or put
[00:15:12:890 - 00:15:13:869] **Speaker 1:** the wrong value on somewhere.
[00:15:14:530 - 00:15:16:330] **Speaker 1:** So if you were to then subtract the transfers of
[00:15:16:330 - 00:15:19:000] **Speaker 1:** itself, you should get a matrix of all zeros.
[00:15:19:409 - 00:15:21:169] **Speaker 1:** That's a really good check to do because if you
[00:15:21:169 - 00:15:23:510] **Speaker 1:** subtract, knowing that the matrix must be symmetrical.
[00:15:23:890 - 00:15:25:969] **Speaker 1:** If you subtract the transfer off itself and you get
[00:15:25:969 - 00:15:28:969] **Speaker 1:** a matrix that isn't zeros, that's a really good sign
[00:15:28:969 - 00:15:31:729] **Speaker 1:** that maybe something hasn't been entered as planned, so.
[00:15:33:320 - 00:15:35:369] **Speaker 1:** What we can do here, essentially in this case we
[00:15:35:369 - 00:15:38:489] **Speaker 1:** have N2 of X twice, but if this was K13
[00:15:38:489 - 00:15:40:080] **Speaker 1:** of X, this would be N1 of X and this
[00:15:40:080 - 00:15:41:010] **Speaker 1:** would be N3 of X.
[00:15:41:289 - 00:15:43:849] **Speaker 1:** We work through, we do the multiplication of those bracketed
[00:15:43:849 - 00:15:47:409] **Speaker 1:** terms, we integrate from 0 to integrate and then evaluate
[00:15:47:409 - 00:15:50:250] **Speaker 1:** from 0 to L and then we work through and
[00:15:50:250 - 00:15:53:409] **Speaker 1:** simplify that and we get this term here.
[00:15:55:429 - 00:15:58:299] **Speaker 1:** So what that tells us is that the K22 for
[00:15:58:299 - 00:16:01:239] **Speaker 1:** this element is equal to 4EI over L.
[00:16:02:369 - 00:16:05:979] **Speaker 1:** Which we can also write as EI over L cubed.
[00:16:07:809 - 00:16:08:520] **Speaker 1:** 4.
[00:16:09:559 - 00:16:13:049] **Speaker 1:** L 2, which then seems like quite a complicated way
[00:16:13:049 - 00:16:13:739] **Speaker 1:** of writing that.
[00:16:14:559 - 00:16:16:539] **Speaker 1:** But we're just bringing a common factor out.
[00:16:18:539 - 00:16:20:020] **Speaker 1:** To show that we can take this.
[00:16:21:469 - 00:16:23:989] **Speaker 1:** And this is where this number here came from.
[00:16:26:409 - 00:16:28:900] **Speaker 1:** So we've taken our shape functions which define the type
[00:16:28:900 - 00:16:31:150] **Speaker 1:** of reactions that we can model.
[00:16:32:960 - 00:16:35:559] **Speaker 1:** We've put in the specific shape functions to get this
[00:16:35:559 - 00:16:39:080] **Speaker 1:** particular entry within this matrix, and this is one example
[00:16:39:080 - 00:16:40:359] **Speaker 1:** of those 16 values.
[00:16:41:570 - 00:16:43:250] **Speaker 1:** Now what you can see here is if we draw
[00:16:43:250 - 00:16:45:640] **Speaker 1:** a line down the main diagonal, you can see 6L
[00:16:45:640 - 00:16:49:799] **Speaker 1:** 6L minus 12 minus 12, 6L 6L 2 L 22
[00:16:49:799 - 00:16:50:770] **Speaker 1:** L squared and so on.
[00:16:51:169 - 00:16:52:950] **Speaker 1:** It is symmetric about that main diagonal.
[00:16:53:010 - 00:16:53:869] **Speaker 1:** So we could work through.
[00:16:54:890 - 00:16:58:150] **Speaker 1:** All 16 numbers, um, of those.
[00:16:59:349 - 00:17:01:510] **Speaker 1:** There's only 10 unique values which is the main diagonal
[00:17:01:510 - 00:17:04:449] **Speaker 1:** and either the upper diagonal or the lower diagonal.
[00:17:05:050 - 00:17:06:790] **Speaker 1:** Uh, we're not gonna do that just in terms of
[00:17:06:790 - 00:17:07:069] **Speaker 1:** time.
[00:17:07:188 - 00:17:10:109] **Speaker 1:** It would be quite a laborious, um, position of things
[00:17:10:109 - 00:17:13:670] **Speaker 1:** to go through, but key thing is if we were
[00:17:13:670 - 00:17:15:109] **Speaker 1:** to do that, these are the numbers that we would
[00:17:15:109 - 00:17:15:449] **Speaker 1:** get.
[00:17:22:319 - 00:17:24:209] **Speaker 1:** So this here is.
[00:17:25:660 - 00:17:26:959] **Speaker 1:** The stiffness matrix.
[00:17:31:140 - 00:17:32:709] **Speaker 1:** In element coordinates.
[00:17:38:469 - 00:17:39:849] **Speaker 1:** For a being element.
[00:17:47:270 - 00:17:48:780] **Speaker 1:** Now the key thing here is we, we assumed a
[00:17:48:780 - 00:17:49:969] **Speaker 1:** numbering sequence when we started.
[00:17:51:579 - 00:17:54:689] **Speaker 1:** And the order of numbers within this matrix is based
[00:17:54:689 - 00:17:56:380] **Speaker 1:** upon that original numbering sequence.
[00:17:56:660 - 00:17:59:819] **Speaker 1:** So we have to be consistent, uh, in that numbering
[00:17:59:819 - 00:18:02:459] **Speaker 1:** sequence because we could have chosen something different to start
[00:18:02:459 - 00:18:03:619] **Speaker 1:** with and some textbooks do.
[00:18:04:750 - 00:18:07:069] **Speaker 1:** But we chose something and this is based on that
[00:18:07:069 - 00:18:09:489] **Speaker 1:** derivation, so therefore we need to be consistent.
[00:18:10:589 - 00:18:11:979] **Speaker 1:** If you would look at one of those textbooks that
[00:18:11:979 - 00:18:15:060] **Speaker 1:** uses a different numbering sequence, essentially what you see is
[00:18:15:060 - 00:18:17:739] **Speaker 1:** the same numbers in this matrix just rearranged in a
[00:18:17:739 - 00:18:18:339] **Speaker 1:** different order.
[00:18:19:819 - 00:18:22:859] **Speaker 1:** Put So, let's have a quick look at that.
[00:18:24:599 - 00:18:26:920] **Speaker 1:** Just a quick reminder, uh, for a bean.
[00:18:29:880 - 00:18:38:560] **Speaker 1:** This is the Numbering Sequence For a beam element.
[00:18:41:119 - 00:18:42:760] **Speaker 1:** We're not gonna do an awful lot with the elements.
[00:18:42:839 - 00:18:45:560] **Speaker 1:** They're really just a stepping stone in terms of getting
[00:18:45:560 - 00:18:47:079] **Speaker 1:** to our frame elements.
[00:18:49:229 - 00:18:54:349] **Speaker 1:** So we have our local YE at node one.
[00:18:56:640 - 00:18:59:359] **Speaker 1:** Is D1.
[00:19:01:449 - 00:19:07:900] **Speaker 1:** Local ZE At note one Is the 2.
[00:19:09:949 - 00:19:22:000] **Speaker 1:** Local Y At node 2 D3 And local Z Aetna
[00:19:22:000 - 00:19:22:400] **Speaker 1:** too.
[00:19:24:119 - 00:19:26:119] **Speaker 1:** Will be D4, so that's the number of sequences that
[00:19:26:119 - 00:19:26:719] **Speaker 1:** we've chosen.
[00:19:27:510 - 00:19:30:130] **Speaker 1:** And why I say local Z and um this here.
[00:19:31:050 - 00:19:35:130] **Speaker 1:** Also recognising because we're dealing in 2D that, um, localz
[00:19:35:130 - 00:19:36:969] **Speaker 1:** is also gonna be global Z because it's always in
[00:19:36:969 - 00:19:39:569] **Speaker 1:** the pane of the page, um, counterclockwise.
[00:19:41:609 - 00:19:43:780] **Speaker 1:** So based upon this numbering sequence, this is our matrix.
[00:19:46:589 - 00:19:48:500] **Speaker 1:** So we, we do have a little bit more freedom
[00:19:48:500 - 00:19:50:540] **Speaker 1:** in terms of how we model structural degrees of freedom,
[00:19:50:579 - 00:19:52:819] **Speaker 1:** but within an element, we don't have any flexibility because
[00:19:52:819 - 00:19:55:199] **Speaker 1:** that's the, the way the matrix was set up.
[00:19:56:489 - 00:19:59:050] **Speaker 1:** We're just born this uh EI over our cubed factor
[00:19:59:050 - 00:20:01:930] **Speaker 1:** out the front just to make the numbers easy.
[00:20:02:010 - 00:20:04:510] **Speaker 1:** It's just a a different way of presenting it.
[00:20:06:229 - 00:20:09:569] **Speaker 1:** Um, it is symmetric, um, so that's important.
[00:20:10:959 - 00:20:13:640] **Speaker 1:** Um, it is assuming that E and I are constant
[00:20:13:640 - 00:20:14:160] **Speaker 1:** over the length.
[00:20:14:280 - 00:20:15:959] **Speaker 1:** I did talk about that before, that we could have
[00:20:15:959 - 00:20:19:540] **Speaker 1:** included some equation for E as a function of X
[00:20:19:540 - 00:20:21:239] **Speaker 1:** and I as a function of X, we would have
[00:20:21:239 - 00:20:22:920] **Speaker 1:** got a different matrix and that would have been specific
[00:20:22:920 - 00:20:23:819] **Speaker 1:** to that profile.
[00:20:24:719 - 00:20:27:800] **Speaker 1:** Uh, it is valid for long slender beams, um, whose
[00:20:28:199 - 00:20:30:089] **Speaker 1:** deformations are predominantly flexural.
[00:20:31:560 - 00:20:34:280] **Speaker 1:** Uh, accounts for small motions because we did assume those
[00:20:34:280 - 00:20:36:680] **Speaker 1:** second order terms were zero, and at the moment we're
[00:20:36:680 - 00:20:38:959] **Speaker 1:** assuming that it's actually rigid, so we're not allowed for
[00:20:38:959 - 00:20:42:040] **Speaker 1:** any axial defamation to exist within here, um.
[00:20:43:430 - 00:20:46:270] **Speaker 1:** And then what we have is that KEE is not
[00:20:46:270 - 00:20:48:339] **Speaker 1:** full rank as the boundary conditions have not yet been
[00:20:48:339 - 00:20:48:589] **Speaker 1:** applied.
[00:20:48:670 - 00:20:51:109] **Speaker 1:** So this matrix is singular, and if you put this
[00:20:51:109 - 00:20:53:630] **Speaker 1:** matrix into Python, it wouldn't solve for you, it would
[00:20:53:630 - 00:20:56:689] **Speaker 1:** just, um, say that there's a singularity issue.
[00:20:57:109 - 00:21:00:010] **Speaker 1:** So, uh, for a 4 by 4 matrix, a full
[00:21:00:010 - 00:21:01:469] **Speaker 1:** rank means a rank of 4.
[00:21:01:709 - 00:21:04:530] **Speaker 1:** So the rank is a parameter that basically is an
[00:21:04:530 - 00:21:07:910] **Speaker 1:** indication of the number of independent equations that exist within
[00:21:07:910 - 00:21:08:339] **Speaker 1:** a matrix.
[00:21:08:390 - 00:21:10:770] **Speaker 1:** It's quite a, a useful property, um.
[00:21:11:689 - 00:21:13:449] **Speaker 1:** For a 4x4 matrix, it needs to be a rank
[00:21:13:449 - 00:21:15:250] **Speaker 1:** of 4 to be able to be solved, but if
[00:21:15:250 - 00:21:17:569] **Speaker 1:** you're to put this matrix in, you won't get that
[00:21:17:569 - 00:21:18:310] **Speaker 1:** because it's singular.
[00:21:19:729 - 00:21:22:699] **Speaker 1:** So, just in Python, that is NP.
[00:21:23:660 - 00:21:29:959] **Speaker 1:** Um Do theelg Dot.
[00:21:31:339 - 00:21:35:939] **Speaker 1:** Matrix_ rank and then, of course, you put in your
[00:21:35:939 - 00:21:37:359] **Speaker 1:** KE variable into that.
[00:21:45:020 - 00:21:48:189] **Speaker 1:** So just like we did before, um, this particular instance,
[00:21:49:270 - 00:21:53:319] **Speaker 1:** Until we introduce the connectivity information and how this element
[00:21:53:319 - 00:21:55:160] **Speaker 1:** is restrained, we won't be able to get a unique
[00:21:55:160 - 00:21:55:420] **Speaker 1:** solution.
[00:21:56:729 - 00:21:58:060] **Speaker 1:** I'm just gonna look through a couple of very quick
[00:21:58:680 - 00:21:59:380] **Speaker 1:** examples here.
[00:22:00:040 - 00:22:03:849] **Speaker 1:** Um, we've sort of got pages 76 and 77, and
[00:22:03:849 - 00:22:05:729] **Speaker 1:** that's the only examples we're gonna do which are actually
[00:22:05:729 - 00:22:06:760] **Speaker 1:** specific to beams.
[00:22:07:130 - 00:22:08:589] **Speaker 1:** We're just gonna cover them very briefly and then we're
[00:22:08:589 - 00:22:11:170] **Speaker 1:** gonna go into the more, um, general element type which
[00:22:11:170 - 00:22:15:310] **Speaker 1:** is frames, which includes both the, um, bending and shear
[00:22:15:569 - 00:22:17:189] **Speaker 1:** but also the axial deformations.
[00:22:22:959 - 00:22:24:439] **Speaker 1:** So we have a stiff cantilever beam.
[00:22:24:969 - 00:22:26:810] **Speaker 1:** So fixed to the left hand edge and a tip
[00:22:26:810 - 00:22:27:489] **Speaker 1:** load on here.
[00:22:28:729 - 00:22:33:640] **Speaker 1:** We have our um, Our beam element here.
[00:22:34:829 - 00:22:36:510] **Speaker 1:** And the first thing we need to do is define
[00:22:36:510 - 00:22:37:069] **Speaker 1:** degrees of freedom.
[00:22:37:150 - 00:22:39:020] **Speaker 1:** So there's 4 possible degrees of freedom here.
[00:22:39:550 - 00:22:41:390] **Speaker 1:** The left hand two are fully constrained, there'll be no
[00:22:41:390 - 00:22:44:540] **Speaker 1:** degrees of freedom here, but we will have say a
[00:22:45:739 - 00:22:50:849] **Speaker 1:** Lowercase q1 and a rotational Q2 here on the right
[00:22:50:849 - 00:22:51:380] **Speaker 1:** hand end.
[00:22:53:560 - 00:22:56:569] **Speaker 1:** So this here is gonna be our global coordinate system.
[00:22:58:010 - 00:23:00:040] **Speaker 1:** XG and YG.
[00:23:02:640 - 00:23:07:550] **Speaker 1:** And then the A1 is equal a Q1, so we,
[00:23:07:670 - 00:23:08:609] **Speaker 1:** we're defining.
[00:23:09:699 - 00:23:13:130] **Speaker 1:** Um, our assembly matrix here.
[00:23:17:609 - 00:23:19:250] **Speaker 1:** So in this case, 4 a bean.
[00:23:20:189 - 00:23:24:589] **Speaker 1:** Uh, D3 is correspondence correspond to Q1 and D4 is
[00:23:24:589 - 00:23:25:849] **Speaker 1:** gonna correspond to Q2.
[00:23:26:949 - 00:23:28:719] **Speaker 1:** So we've got a 1 there and a 1 there,
[00:23:29:199 - 00:23:30:180] **Speaker 1:** everything else is 0.
[00:23:31:479 - 00:23:33:890] **Speaker 1:** This is the assembly matrix that we would generate for
[00:23:33:890 - 00:23:34:250] **Speaker 1:** this.
[00:23:36:020 - 00:23:38:359] **Speaker 1:** And if we would go through and apply.
[00:23:39:319 - 00:23:43:040] **Speaker 1:** Our KG for element, which is also gonna be kg
[00:23:43:040 - 00:23:44:280] **Speaker 1:** because there is only one element here.
[00:23:45:050 - 00:23:48:180] **Speaker 1:** We have our assembly matrix times KE hat.
[00:23:49:130 - 00:23:50:989] **Speaker 1:** Times the assembly matrix transposed.
[00:23:52:369 - 00:23:53:750] **Speaker 1:** What that would essentially do.
[00:23:54:660 - 00:23:57:079] **Speaker 1:** In our equation here is it would, it would remove
[00:23:57:079 - 00:23:59:000] **Speaker 1:** the first two equations out of here.
[00:24:00:359 - 00:24:02:209] **Speaker 1:** So we'll take this and we'll take the two columns
[00:24:02:209 - 00:24:02:550] **Speaker 1:** out.
[00:24:04:310 - 00:24:07:189] **Speaker 1:** And what it would leave was essentially this lower part
[00:24:07:189 - 00:24:09:300] **Speaker 1:** of the matrix, and that's what would be solved.
[00:24:09:390 - 00:24:12:229] **Speaker 1:** That's what uh procedurally an assembly matrix 60 does, it
[00:24:12:229 - 00:24:16:589] **Speaker 1:** can actually reduce the size of the, the overall matrix
[00:24:16:949 - 00:24:19:050] **Speaker 1:** to just the bit that's gonna give us new information.
[00:24:23:420 - 00:24:28:010] **Speaker 1:** Um, so, Uh, it is, if it's originally fixed on
[00:24:28:010 - 00:24:30:099] **Speaker 1:** the left side, those two deflections are zero.
[00:24:30:709 - 00:24:32:819] **Speaker 1:** this is the new information here and if we were
[00:24:32:819 - 00:24:37:060] **Speaker 1:** to solve that, This is the, the answer that we
[00:24:37:060 - 00:24:37:500] **Speaker 1:** would get.
[00:24:38:709 - 00:24:39:439] **Speaker 1:** So we worked through this.
[00:24:39:479 - 00:24:42:119] **Speaker 1:** This is just a longhand of doing a matrix inverse
[00:24:42:119 - 00:24:43:640] **Speaker 1:** and this is the answers that we would get.
[00:24:46:260 - 00:24:50:459] **Speaker 1:** Now, you would hope this benchmarks against what we're used
[00:24:50:459 - 00:24:53:300] **Speaker 1:** to seeing for a tiplo a cantilever, and thankfully it
[00:24:53:300 - 00:24:54:660] **Speaker 1:** does, so.
[00:24:55:800 - 00:24:57:719] **Speaker 1:** The vertical tip deflection.
[00:25:00:619 - 00:25:01:979] **Speaker 1:** For a tip loaded cantilever.
[00:25:03:010 - 00:25:04:890] **Speaker 1:** Is equal to minus PL cubed.
[00:25:05:979 - 00:25:10:959] **Speaker 1:** Over 3 EI So You might remember that from, from
[00:25:10:959 - 00:25:11:579] **Speaker 1:** last year.
[00:25:12:780 - 00:25:14:369] **Speaker 1:** And the tip rotation.
[00:25:17:949 - 00:25:22:310] **Speaker 1:** Is going to be equal to minus PL 2.
[00:25:23:079 - 00:25:27:079] **Speaker 1:** Over to AI, so it's negative because, um, it's the
[00:25:27:079 - 00:25:29:890] **Speaker 1:** downward deflection and counterclockwise is positive.
[00:25:30:319 - 00:25:33:550] **Speaker 1:** The tip is actually going to rotate clockwise, which is
[00:25:33:550 - 00:25:35:280] **Speaker 1:** why we get a negative value.
[00:25:37:640 - 00:25:40:800] **Speaker 1:** So Yeah, it's nice to know that.
[00:25:41:719 - 00:25:43:439] **Speaker 1:** When we do this and we, we try some test
[00:25:43:439 - 00:25:45:880] **Speaker 1:** cases that we actually get an answer which is consistent
[00:25:45:880 - 00:25:48:280] **Speaker 1:** with what you would have expected from doing this in
[00:25:48:280 - 00:25:49:099] **Speaker 1:** previous years.
[00:25:50:640 - 00:25:52:510] **Speaker 1:** As I said at the start of the course, this
[00:25:52:510 - 00:25:55:079] **Speaker 1:** doesn't replace what you did in 202, it builds upon
[00:25:55:079 - 00:25:55:380] **Speaker 1:** it.
[00:25:58:449 - 00:25:59:750] **Speaker 1:** Now what we're gonna do quickly here.
[00:26:00:569 - 00:26:04:599] **Speaker 1:** There's one simple example, which is a a block mounted
[00:26:04:599 - 00:26:05:900] **Speaker 1:** on the top of a vertical post.
[00:26:06:869 - 00:26:08:569] **Speaker 1:** And we're displacing that laterally.
[00:26:10:260 - 00:26:13:939] **Speaker 1:** So the next example on the next page, it's very
[00:26:13:939 - 00:26:16:140] **Speaker 1:** similar to what we did, you know, this we turn
[00:26:16:140 - 00:26:18:739] **Speaker 1:** a side on these two look very similar, but now
[00:26:18:739 - 00:26:20:520] **Speaker 1:** there's a concentrated mass at the top.
[00:26:26:449 - 00:26:29:750] **Speaker 1:** So we have a vertical cantilever mean with lumped mass.
[00:26:30:670 - 00:26:32:890] **Speaker 1:** We're we're gonna do is we apply a force P
[00:26:32:989 - 00:26:35:709] **Speaker 1:** at the top which will displace it laterally and then
[00:26:35:709 - 00:26:38:510] **Speaker 1:** we're actually gonna have this this weight now is outside
[00:26:38:510 - 00:26:38:969] **Speaker 1:** the footing.
[00:26:39:680 - 00:26:42:680] **Speaker 1:** And there's this extra component which is the overturning moment
[00:26:42:680 - 00:26:44:719] **Speaker 1:** that exists because of gravity.
[00:26:46:609 - 00:26:47:130] **Speaker 1:** So.
[00:26:49:790 - 00:26:53:630] **Speaker 1:** The mess Displaces.
[00:26:56:310 - 00:27:09:939] **Speaker 1:** Outside the footing And creates And Overturn in the moment.
[00:27:15:109 - 00:27:17:270] **Speaker 1:** So that's the bit that's not implicitly captured.
[00:27:19:800 - 00:27:22:410] **Speaker 1:** So if we ignore the actual effects at rest and
[00:27:22:410 - 00:27:23:189] **Speaker 1:** the underformed shape.
[00:27:24:199 - 00:27:29:319] **Speaker 1:** Um The deflection term here is going to be uh
[00:27:29:319 - 00:27:31:790] **Speaker 1:** MG, which is the weight of this times the tip
[00:27:31:790 - 00:27:32:839] **Speaker 1:** of fiction D3.
[00:27:35:680 - 00:27:38:719] **Speaker 1:** So what we can do here is that's not actually
[00:27:38:719 - 00:27:42:800] **Speaker 1:** going to be um implicitly incorporated into the the solution.
[00:27:43:689 - 00:27:45:530] **Speaker 1:** So what we could do is we could manually introduce
[00:27:45:530 - 00:27:47:229] **Speaker 1:** this, we could basically take this down here.
[00:27:48:000 - 00:27:51:969] **Speaker 1:** We've got our load P, which is our deflection there.
[00:27:53:400 - 00:27:56:439] **Speaker 1:** But now we've also got our MG times PL cubed
[00:27:56:439 - 00:27:57:000] **Speaker 1:** over 3i.
[00:27:57:079 - 00:28:00:439] **Speaker 1:** So this is uh MG the D3 was PL cubed
[00:28:00:439 - 00:28:02:560] **Speaker 1:** over 3i, that's what we found on the previous page.
[00:28:03:099 - 00:28:07:040] **Speaker 1:** And what we then have here is an additional moment
[00:28:07:040 - 00:28:07:400] **Speaker 1:** term.
[00:28:08:369 - 00:28:12:109] **Speaker 1:** That's being manually introduced here, which represents the overturning moment
[00:28:12:109 - 00:28:14:829] **Speaker 1:** that exists from this, this mass being displaced by a
[00:28:14:829 - 00:28:15:810] **Speaker 1:** distance D3.
[00:28:18:099 - 00:28:21:180] **Speaker 1:** If we put some values in, just some, you know,
[00:28:21:420 - 00:28:26:729] **Speaker 1:** reasonable values, um, represent a, you know, physically reasonable thing
[00:28:27:219 - 00:28:29:540] **Speaker 1:** with just the, the standard value we would get would
[00:28:29:540 - 00:28:30:680] **Speaker 1:** be 0.18 metres.
[00:28:32:339 - 00:28:35:339] **Speaker 1:** And then we would extend to 0.212 metres if we
[00:28:35:339 - 00:28:38:339] **Speaker 1:** were to, um, include this extra upsetting moment.
[00:28:40:609 - 00:28:45:939] **Speaker 1:** So in this case, the additional gravity load actually introduces
[00:28:45:939 - 00:28:48:199] **Speaker 1:** increases the displacement by about 18%.
[00:28:48:989 - 00:28:51:589] **Speaker 1:** And what we really would have to do here, um,
[00:28:52:109 - 00:28:54:829] **Speaker 1:** is really iterate on this because that's kind of almost
[00:28:54:829 - 00:28:58:510] **Speaker 1:** a first order approximation whereas this is, this upsetting moment
[00:28:58:510 - 00:29:03:869] **Speaker 1:** is based upon this, um, initial approximation of displacement.
[00:29:04:150 - 00:29:06:349] **Speaker 1:** What we really should do is substitute this back and
[00:29:06:930 - 00:29:11:790] **Speaker 1:** update the, um, upsetting moment that exists, the overturning moment
[00:29:11:790 - 00:29:14:430] **Speaker 1:** from that displacement, and then iterate until we get a
[00:29:14:430 - 00:29:15:449] **Speaker 1:** converged solution.
[00:29:15:760 - 00:29:17:949] **Speaker 1:** But We're not gonna go into that because it's probably
[00:29:17:949 - 00:29:20:650] **Speaker 1:** a little bit more detail um than we need.
[00:29:21:150 - 00:29:23:910] **Speaker 1:** um, this is just a quick example to show you
[00:29:23:910 - 00:29:26:390] **Speaker 1:** how the elements work by noting that we're actually going
[00:29:26:390 - 00:29:27:329] **Speaker 1:** to a more general element.
[00:29:29:280 - 00:29:31:599] **Speaker 1:** So is there any questions on this example or anything
[00:29:31:599 - 00:29:33:900] **Speaker 1:** to do with the, the beam element derivations?
[00:29:40:369 - 00:29:40:920] **Speaker 1:** OK.
[00:29:45:790 - 00:29:48:140] **Speaker 1:** So the next thing we're gonna look at is framing
[00:29:48:140 - 00:29:48:430] **Speaker 1:** ones.
[00:29:59:420 - 00:30:01:260] **Speaker 1:** So maybe before we start, a quick show of hands,
[00:30:01:530 - 00:30:02:479] **Speaker 1:** who loves derivations?
[00:30:04:589 - 00:30:06:550] **Speaker 1:** Well I've got excellent news for you, cos we actually
[00:30:06:550 - 00:30:08:739] **Speaker 1:** don't, we've got a new element type, we don't need
[00:30:08:739 - 00:30:10:040] **Speaker 1:** to do anymore derivations.
[00:30:10:550 - 00:30:12:869] **Speaker 1:** We already have covered all of the reaction mechanisms that
[00:30:12:869 - 00:30:14:670] **Speaker 1:** are needed to model a frame.
[00:30:16:359 - 00:30:18:079] **Speaker 1:** We don't, there's no new information, we just need to
[00:30:18:079 - 00:30:19:660] **Speaker 1:** combine the information we already have.
[00:30:21:969 - 00:30:24:890] **Speaker 1:** So Just to maybe start off with some.
[00:30:25:520 - 00:30:26:319] **Speaker 1:** Clear definition.
[00:30:26:439 - 00:30:27:260] **Speaker 1:** So bars.
[00:30:28:989 - 00:30:30:449] **Speaker 1:** They were axial loads only.
[00:30:33:670 - 00:30:39:030] **Speaker 1:** With No she Or bending moments.
[00:30:44:670 - 00:30:46:079] **Speaker 1:** Then what we had was beans.
[00:30:47:510 - 00:30:48:859] **Speaker 1:** And this was sheer.
[00:30:50:510 - 00:30:51:849] **Speaker 1:** And moment only.
[00:30:55:689 - 00:30:56:489] **Speaker 1:** No axial.
[00:30:58:849 - 00:31:00:859] **Speaker 1:** And now what we're going to have is frames.
[00:31:02:520 - 00:31:13:170] **Speaker 1:** Which is Sheer Ending And axial loading All together in
[00:31:13:170 - 00:31:13:709] **Speaker 1:** one element.
[00:31:18:199 - 00:31:20:030] **Speaker 1:** So what we're gonna do here is apply the principle
[00:31:20:030 - 00:31:21:199] **Speaker 1:** of linear superposition.
[00:31:24:069 - 00:31:29:800] **Speaker 1:** Now, the principle of linear opposition to position does Assume
[00:31:29:800 - 00:31:30:660] **Speaker 1:** a few things.
[00:31:32:689 - 00:31:35:020] **Speaker 1:** So to be able to do this, it assumes.
[00:31:37:030 - 00:31:38:130] **Speaker 1:** Small deflections.
[00:31:42:550 - 00:31:44:949] **Speaker 1:** And that's not necessarily a big issue because we've already
[00:31:44:949 - 00:31:47:390] **Speaker 1:** kind of limited ourselves to that because that's wrapped up
[00:31:47:390 - 00:31:53:839] **Speaker 1:** in our, um, In our derivations It also assumes.
[00:31:55:770 - 00:31:56:949] **Speaker 1:** The neur elastic behaviour.
[00:32:05:829 - 00:32:08:560] **Speaker 1:** So Everything we're doing in this part of the course
[00:32:08:560 - 00:32:10:209] **Speaker 1:** is based upon linear elasticity.
[00:32:10:420 - 00:32:13:380] **Speaker 1:** So an implicit assumption of everything we're doing is that
[00:32:13:380 - 00:32:17:979] **Speaker 1:** we're within the proportional range of a material where um
[00:32:18:380 - 00:32:21:969] **Speaker 1:** applied loads and corresponding deflections are linear linearly related to
[00:32:21:969 - 00:32:22:400] **Speaker 1:** each other.
[00:32:23:599 - 00:32:25:520] **Speaker 1:** Now we know that if we put enough light on
[00:32:25:520 - 00:32:28:400] **Speaker 1:** things, they start to deform elastically, and there are things
[00:32:28:400 - 00:32:30:880] **Speaker 1:** we can do to extend this method to deal with
[00:32:30:880 - 00:32:34:040] **Speaker 1:** non-linear behaviour, but we haven't done those.
[00:32:34:319 - 00:32:38:189] **Speaker 1:** So we are, you know, we are assuming that we're
[00:32:38:189 - 00:32:40:119] **Speaker 1:** within the linear elastic range and we can essentially apply
[00:32:40:119 - 00:32:43:839] **Speaker 1:** this position, uh, principle of superposition where we take one
[00:32:43:839 - 00:32:47:599] **Speaker 1:** deformation component and another and we just sort of superimpose
[00:32:47:599 - 00:32:49:760] **Speaker 1:** those or add them together and then they don't have
[00:32:49:760 - 00:32:51:239] **Speaker 1:** to be solved interdependently.
[00:32:53:819 - 00:32:55:380] **Speaker 1:** So, what we have here.
[00:32:56:640 - 00:32:57:949] **Speaker 1:** This is a 6th degree freedom frame element.
[00:33:00:160 - 00:33:03:839] **Speaker 1:** Now, this is X goes from here to here, so
[00:33:03:839 - 00:33:05:250] **Speaker 1:** this here must be node 1.
[00:33:06:560 - 00:33:09:459] **Speaker 1:** The same principles apply, it always goes from node 1.
[00:33:10:439 - 00:33:12:400] **Speaker 1:** Towards node 2.
[00:33:13:489 - 00:33:14:449] **Speaker 1:** That hasn't changed.
[00:33:16:709 - 00:33:18:459] **Speaker 1:** What we're gonna say here is that X for an
[00:33:18:459 - 00:33:19:000] **Speaker 1:** element.
[00:33:20:880 - 00:33:23:680] **Speaker 1:** At node one is going to be D1.
[00:33:24:819 - 00:33:29:380] **Speaker 1:** Y E At node 1 will be D2.
[00:33:31:449 - 00:33:37:500] **Speaker 1:** And then ZE At node 1 is equal to D3.
[00:33:41:859 - 00:33:44:739] **Speaker 1:** Then what we have is XE at node 2.
[00:33:46:250 - 00:33:47:750] **Speaker 1:** Will be D4.
[00:33:48:989 - 00:33:54:310] **Speaker 1:** Y E At 2 SD 5.
[00:33:55:760 - 00:33:57:329] **Speaker 1:** And ZE at 2.
[00:33:58:619 - 00:33:59:760] **Speaker 1:** Will be D6.
[00:34:00:900 - 00:34:02:660] **Speaker 1:** So we're just gonna work through the same start node
[00:34:02:660 - 00:34:04:420] **Speaker 1:** 1 and then go to node 2 X Y Z
[00:34:04:420 - 00:34:05:219] **Speaker 1:** X Y Z.
[00:34:06:359 - 00:34:08:010] **Speaker 1:** It's not the only number of signs we could use,
[00:34:08:128 - 00:34:09:648] **Speaker 1:** but I think it's the most intuitive one.
[00:34:13:260 - 00:34:16:419] **Speaker 1:** And what that is, those the element with 6 degrees
[00:34:16:419 - 00:34:19:939] **Speaker 1:** of freedom, it's just going to be the linear superposition
[00:34:20:179 - 00:34:23:419] **Speaker 1:** of a bar element which we already have, and the
[00:34:23:419 - 00:34:25:820] **Speaker 1:** frame, a beam element which we've just arrived.
[00:34:26:408 - 00:34:32:189] **Speaker 1:** And together, um, so this should actually include also I
[00:34:32:189 - 00:34:33:510] **Speaker 1:** on here, I a.
[00:34:34:580 - 00:34:42:148] **Speaker 1:** I and L Now, the reason we did that last
[00:34:42:148 - 00:34:45:908] **Speaker 1:** example is it is important to realise that we are
[00:34:45:908 - 00:34:49:860] **Speaker 1:** essentially solving, These two systems independently.
[00:34:50:689 - 00:34:51:888] **Speaker 1:** Wrapped up in the same solution.
[00:34:52:010 - 00:34:53:648] **Speaker 1:** So what that means is that when we actually do
[00:34:53:648 - 00:34:58:100] **Speaker 1:** this analysis, there's no inherent coupling between the axial terms
[00:34:58:100 - 00:34:59:129] **Speaker 1:** and the flexual terms.
[00:34:59:280 - 00:35:03:189] **Speaker 1:** They essentially being solved independently within the same matrix.
[00:35:05:590 - 00:35:08:850] **Speaker 1:** So what is the The stiffness matrix for a frame
[00:35:08:850 - 00:35:09:399] **Speaker 1:** look like?
[00:35:10:469 - 00:35:12:550] **Speaker 1:** Well, we have that on the next page, on page
[00:35:12:550 - 00:35:13:270] **Speaker 1:** 79.
[00:35:15:129 - 00:35:17:810] **Speaker 1:** Number of sequences we've just defined, node 1, node 2,
[00:35:17:889 - 00:35:20:449] **Speaker 1:** X Y Z X Y Z and degrees of freedom
[00:35:20:449 - 00:35:21:330] **Speaker 1:** 1 through 6.
[00:35:24:830 - 00:35:29:340] **Speaker 1:** Now what we have Is this equation here.
[00:35:29:909 - 00:35:31:500] **Speaker 1:** Looks like the equation you've seen before.
[00:35:32:229 - 00:35:35:419] **Speaker 1:** And that's because it is, it's the element stiffness matrix.
[00:35:41:550 - 00:35:43:070] **Speaker 1:** In element coordinates.
[00:35:49:810 - 00:35:51:489] **Speaker 1:** So that's now a 6 by 1 vector because it
[00:35:52:129 - 00:35:54:330] **Speaker 1:** has 6 forome terms defined here.
[00:35:55:050 - 00:35:57:370] **Speaker 1:** The K matrix is now 6 by 6, and the
[00:35:57:370 - 00:35:59:330] **Speaker 1:** defection vector is now 6 by 1.
[00:36:04:209 - 00:36:05:889] **Speaker 1:** So if we look at this overall matrix, all we've
[00:36:05:889 - 00:36:08:330] **Speaker 1:** done is just taken the, the reaction mechanisms we've already
[00:36:08:330 - 00:36:11:790] **Speaker 1:** derived and we've bundled them together into one single matrix.
[00:36:14:330 - 00:36:15:389] **Speaker 1:** And what you can see here.
[00:36:16:090 - 00:36:18:239] **Speaker 1:** Is that we have all these zeros sitting in here.
[00:36:28:399 - 00:36:30:370] **Speaker 1:** And these zeros.
[00:36:32:419 - 00:36:42:459] **Speaker 1:** Exist Because they There's no coupling.
[00:36:46:270 - 00:36:54:780] **Speaker 1:** Between XU And transverse slash moment.
[00:36:56:949 - 00:36:57:590] **Speaker 1:** Terms.
[00:37:00:479 - 00:37:01:989] **Speaker 1:** So this is just one big matrix and we'll treat
[00:37:01:989 - 00:37:04:399] **Speaker 1:** it as such, but it is important to realise sort
[00:37:04:399 - 00:37:07:290] **Speaker 1:** of implicitly in there is two independent systems that are
[00:37:07:290 - 00:37:10:479] **Speaker 1:** just being solved at the same time but independently.
[00:37:12:399 - 00:37:13:919] **Speaker 1:** And the reason that's important is that we look at
[00:37:13:919 - 00:37:16:679] **Speaker 1:** that, you know, if, if you take a, a beam
[00:37:16:679 - 00:37:18:760] **Speaker 1:** and you translate it, you, you put a load on
[00:37:18:760 - 00:37:20:760] **Speaker 1:** it and it has a transverse deflection, but it also
[00:37:20:760 - 00:37:21:639] **Speaker 1:** has an axial load.
[00:37:22:040 - 00:37:24:000] **Speaker 1:** Now, the fact that there would, there would now be
[00:37:24:000 - 00:37:27:479] **Speaker 1:** a moment, a forced moment couple from that axial load
[00:37:27:479 - 00:37:30:080] **Speaker 1:** because now the, the axial load where they started colinear
[00:37:30:280 - 00:37:32:939] **Speaker 1:** with the transverse deflection, there's actually now an upsetting moment
[00:37:32:939 - 00:37:33:360] **Speaker 1:** in there.
[00:37:34:300 - 00:37:36:620] **Speaker 1:** That's not captured in this analysis.
[00:37:36:860 - 00:37:40:209] **Speaker 1:** So just to make you aware of the limitation that
[00:37:40:580 - 00:37:42:699] **Speaker 1:** don't assume that that's sort of wrapped up in there.
[00:37:45:149 - 00:37:49:389] **Speaker 1:** So then what we do is we translate this to.
[00:37:50:280 - 00:37:53:139] **Speaker 1:** Uh, global coordinates, so we're using a transformation matrix.
[00:37:56:139 - 00:37:58:370] **Speaker 1:** So this is the stiffness equation.
[00:38:03:830 - 00:38:08:919] **Speaker 1:** Transformed Into global coordinates.
[00:38:20:479 - 00:38:23:229] **Speaker 1:** Now in week one, we did the, in the Python
[00:38:23:229 - 00:38:26:659] **Speaker 1:** refresher, we looked at NP.block which was essentially building up
[00:38:26:840 - 00:38:29:959] **Speaker 1:** a larger matrix from smaller matrices, and the reason we
[00:38:29:959 - 00:38:31:659] **Speaker 1:** did that is basically for this right here.
[00:38:33:340 - 00:38:35:120] **Speaker 1:** So if we just put some dashed lines through here,
[00:38:35:179 - 00:38:36:860] **Speaker 1:** just to sort of see the submatrices.
[00:38:37:750 - 00:38:43:429] **Speaker 1:** We essentially have, um, just remember here, C equals cos
[00:38:43:429 - 00:38:45:600] **Speaker 1:** alpha and S equals sin alpha, so we're using the
[00:38:45:600 - 00:38:48:340] **Speaker 1:** same shorthand that we did for bar elements.
[00:38:50:199 - 00:38:52:520] **Speaker 1:** We have this little submatrix which sits on the main
[00:38:52:520 - 00:38:54:439] **Speaker 1:** diagonal, and then we just have a zero matrix on
[00:38:54:439 - 00:38:55:149] **Speaker 1:** the off-diagonal.
[00:38:55:199 - 00:38:58:719] **Speaker 1:** So this little lambda, the lowercase lambda is the this
[00:38:58:719 - 00:39:00:919] **Speaker 1:** matrix here and then zeros on the other, and this
[00:39:00:919 - 00:39:03:659] **Speaker 1:** is the overall um transformation matrix.
[00:39:07:929 - 00:39:14:209] **Speaker 1:** So For submatrices.
[00:39:18:830 - 00:39:19:989] **Speaker 1:** So maybe 4.
[00:39:20:840 - 00:39:22:520] **Speaker 1:** 3 by 3 submatrices.
[00:39:24:110 - 00:39:26:689] **Speaker 1:** Form the overall 6 by 6.
[00:39:27:629 - 00:39:30:560] **Speaker 1:** Which is the NP.block command.
[00:39:33:989 - 00:39:36:580] **Speaker 1:** And of course there's only 2 unique matrices, there's 4
[00:39:36:719 - 00:39:38:479] **Speaker 1:** submatrices, but there's only 2 unique ones.
[00:39:41:659 - 00:39:43:100] **Speaker 1:** Now what we have here is we have some cosine
[00:39:43:100 - 00:39:45:699] **Speaker 1:** and sign terms, but we also have this one here.
[00:39:48:080 - 00:39:49:540] **Speaker 1:** So, let's have a quick look at that.
[00:39:51:300 - 00:39:53:320] **Speaker 1:** One here and one here.
[00:39:54:939 - 00:39:56:129] **Speaker 1:** Question is, where did the one come from?
[00:39:56:209 - 00:39:57:750] **Speaker 1:** Why is that, why is that a one?
[00:39:59:020 - 00:40:00:739] **Speaker 1:** Well, let's look at our coordinate systems, so we might
[00:40:00:739 - 00:40:01:560] **Speaker 1:** have X.
[00:40:02:770 - 00:40:14:679] **Speaker 1:** A Y E And ZE And security.
[00:40:16:520 - 00:40:20:909] **Speaker 0:** OK, um It's still showing here, so I think the
[00:40:20:909 - 00:40:21:699] **Speaker 1:** problem is here.
[00:40:25:209 - 00:40:26:209] **Speaker 1:** Let's see what I can do.
[00:40:46:969 - 00:40:48:570] **Speaker 1:** There is a small screen on here, it still seems
[00:40:48:570 - 00:40:49:729] **Speaker 1:** to be working as planned.
[00:40:51:050 - 00:40:52:290] **Speaker 1:** I think maybe it'll come back.
[00:41:00:300 - 00:41:01:860] **Speaker 1:** I'll power cycle this and see if it makes a
[00:41:01:860 - 00:41:02:159] **Speaker 1:** difference.
[00:41:17:870 - 00:41:19:090] **Speaker 1:** So we've got something back.
[00:41:20:189 - 00:41:21:129] **Speaker 1:** Sorry about the hassle here.
[00:41:24:959 - 00:41:26:320] **Speaker 1:** And this was supposed to be an arrow, not a
[00:41:26:320 - 00:41:27:699] **Speaker 1:** smiley face, but.
[00:41:30:419 - 00:41:33:199] **Speaker 1:** So we've got X, Y, and Z, um, and then
[00:41:33:699 - 00:41:35:899] **Speaker 1:** for within a 2D plane.
[00:41:38:199 - 00:41:39:379] **Speaker 1:** In a 2D plane.
[00:41:42:580 - 00:41:44:959] **Speaker 1:** Any 2D transformation.
[00:41:50:239 - 00:42:00:550] **Speaker 1:** We'll still have ZA Upwards Out of the page.
[00:42:03:090 - 00:42:04:810] **Speaker 1:** So we're coming, you know, right-hand row X, Y, and
[00:42:04:810 - 00:42:06:770] **Speaker 1:** Z, and we're assuming that we're operating on a 2D
[00:42:06:770 - 00:42:10:199] **Speaker 1:** plane and essentially we can rotate through that 2D angle,
[00:42:10:610 - 00:42:13:350] **Speaker 1:** but Z's always gonna be upwards and counterclockwise.
[00:42:14:699 - 00:42:17:219] **Speaker 1:** So we could sketch that, you know, I mean we've
[00:42:17:219 - 00:42:22:110] **Speaker 1:** got our, XG Yeah.
[00:42:22:620 - 00:42:23:389] **Speaker 1:** YG.
[00:42:24:520 - 00:42:26:100] **Speaker 1:** And our Z G.
[00:42:29:419 - 00:42:45:310] **Speaker 1:** And Basically In a 2D plane Z As always See
[00:42:49:800 - 00:42:51:639] **Speaker 1:** So we've got no transformation needed.
[00:42:59:290 - 00:43:03:320] **Speaker 1:** And hence the value of 1.0, which exists on this
[00:43:03:320 - 00:43:07:000] **Speaker 1:** because you remember we're going X Y Z XYZ, through
[00:43:07:000 - 00:43:07:939] **Speaker 1:** the six degrees of freedom.
[00:43:09:270 - 00:43:11:310] **Speaker 1:** And it's the two Z components there that correspond to
[00:43:11:310 - 00:43:11:989] **Speaker 1:** the 1s.
[00:43:13:590 - 00:43:16:310] **Speaker 1:** Now the two, the, the local X and the local
[00:43:16:310 - 00:43:18:510] **Speaker 1:** y to the global X and the global y, they
[00:43:18:510 - 00:43:20:229] **Speaker 1:** can still be transformed, which is why we have the
[00:43:20:229 - 00:43:23:310] **Speaker 1:** cosine and sine terms which we've seen before and then
[00:43:23:310 - 00:43:27:969] **Speaker 1:** we just have that extra term z which Doesn't require
[00:43:27:969 - 00:43:29:129] **Speaker 1:** a transformation.
[00:43:32:580 - 00:43:33:840] **Speaker 1:** Now one thing that's worth noting here.
[00:43:35:729 - 00:43:39:290] **Speaker 1:** Is that last week when we did the lab, our
[00:43:39:290 - 00:43:42:739] **Speaker 1:** little KE, This one up here was a 2 by
[00:43:42:739 - 00:43:43:120] **Speaker 1:** 2.
[00:43:44:080 - 00:43:46:290] **Speaker 1:** Once we transformed it here, it was a 4 by
[00:43:46:290 - 00:43:46:679] **Speaker 1:** 4.
[00:43:47:639 - 00:43:49:649] **Speaker 1:** So if you use the wrong matrix and you used
[00:43:49:649 - 00:43:52:800] **Speaker 1:** Khat when you should have been using KE, Python will
[00:43:52:800 - 00:43:53:669] **Speaker 1:** immediately throw up an error.
[00:43:53:719 - 00:43:56:679] **Speaker 1:** It'll say these matrix aren't conformable, I can't do my
[00:43:56:679 - 00:43:58:360] **Speaker 1:** multiplication here, something's wrong.
[00:43:58:479 - 00:44:00:199] **Speaker 1:** So it's a nice red flag to stop and check
[00:44:00:199 - 00:44:00:899] **Speaker 1:** things out.
[00:44:01:520 - 00:44:05:020] **Speaker 1:** This week, however, our little KE is a 6x6, our
[00:44:05:020 - 00:44:06:159] **Speaker 1:** KE hat hat.
[00:44:07:179 - 00:44:09:860] **Speaker 1:** Here is also a 6 by 6, this and this
[00:44:09:860 - 00:44:12:709] **Speaker 1:** both 6 by 6, despite being different matrices, they do
[00:44:12:709 - 00:44:13:879] **Speaker 1:** have the same dimensions.
[00:44:14:689 - 00:44:16:300] **Speaker 1:** So what that means is that if you use the
[00:44:16:300 - 00:44:16:929] **Speaker 1:** wrong one.
[00:44:17:989 - 00:44:20:429] **Speaker 1:** There'll be no error from Python, it will quite happily
[00:44:20:429 - 00:44:22:989] **Speaker 1:** proceed on and do the multiplication and give you a
[00:44:22:989 - 00:44:24:909] **Speaker 1:** result, but it will be the wrong result.
[00:44:25:189 - 00:44:27:070] **Speaker 1:** Well, of course, if you get a zero degree transformation
[00:44:27:070 - 00:44:30:520] **Speaker 1:** angle, you might get away with it, but um, That's
[00:44:30:520 - 00:44:32:719] **Speaker 1:** just the extra thing that um in some ways it's
[00:44:32:719 - 00:44:35:840] **Speaker 1:** quite nice in that first lab that it does force
[00:44:35:840 - 00:44:39:379] **Speaker 1:** you to maybe check the the process because um the
[00:44:39:389 - 00:44:42:399] **Speaker 1:** the different matrix sizes raise a flag that that won't
[00:44:42:399 - 00:44:43:199] **Speaker 1:** happen this week.
[00:44:49:239 - 00:44:54:800] **Speaker 1:** So This here is our list of equations.
[00:44:54:850 - 00:44:58:080] **Speaker 1:** So we have our elements stiffness matrix and local coordinates,
[00:44:58:199 - 00:45:02:260] **Speaker 1:** our elements stiffness matrix equation and global coordinates.
[00:45:02:669 - 00:45:05:810] **Speaker 1:** We have our relationship between local and global coordinates for
[00:45:05:810 - 00:45:08:810] **Speaker 1:** deflections and local and global coordinates for forces.
[00:45:10:199 - 00:45:12:639] **Speaker 1:** Now if we were to take these little subscripts here
[00:45:12:639 - 00:45:15:129] **Speaker 1:** which refer to the size of those vectors and matrices,
[00:45:15:719 - 00:45:17:360] **Speaker 1:** this would be the exact same, you know, this could
[00:45:17:360 - 00:45:20:129] **Speaker 1:** equally have been presented last week in relation to bars.
[00:45:20:439 - 00:45:22:060] **Speaker 1:** All of those equations are the same.
[00:45:22:889 - 00:45:26:250] **Speaker 1:** Symbolic equations you've seen before, nothing has changed.
[00:45:27:040 - 00:45:29:850] **Speaker 1:** Um, with the, the equations themselves, but the size of
[00:45:29:850 - 00:45:31:649] **Speaker 1:** the vectors and the size of the matrices that are
[00:45:31:649 - 00:45:33:209] **Speaker 1:** being used within them does change.
[00:45:33:489 - 00:45:36:530] **Speaker 1:** So the, the meaning of all these variables is exactly
[00:45:36:530 - 00:45:37:689] **Speaker 1:** the same as they were last week.
[00:45:37:969 - 00:45:40:300] **Speaker 1:** Now they're just slightly bigger and they have some extra
[00:45:40:649 - 00:45:43:030] **Speaker 1:** numbers in them which represent different reaction mechanisms.
[00:45:45:620 - 00:45:48:899] **Speaker 1:** We've got, um, our deflection, so the same way we
[00:45:48:899 - 00:45:51:580] **Speaker 1:** did last week, once we've got, we go through and
[00:45:51:580 - 00:45:53:719] **Speaker 1:** we solve for our lowercase q, so that's how much
[00:45:53:969 - 00:45:55:679] **Speaker 1:** every nodal point has deflected.
[00:45:56:469 - 00:46:00:469] **Speaker 1:** We can use our assembly matrix, um, transposed to then
[00:46:00:469 - 00:46:03:709] **Speaker 1:** extract and and allocate those into the appropriate locations within
[00:46:03:709 - 00:46:04:110] **Speaker 1:** D.
[00:46:04:550 - 00:46:07:780] **Speaker 1:** We can sum up across an element, um, to get
[00:46:07:780 - 00:46:09:989] **Speaker 1:** back across multiple elements to.
[00:46:10:570 - 00:46:12:469] **Speaker 1:** Determine our overall forcing terms.
[00:46:13:500 - 00:46:16:020] **Speaker 1:** And our KG definition is exactly as it was last
[00:46:16:020 - 00:46:18:419] **Speaker 1:** week, just now with slightly bigger matrices.
[00:46:20:729 - 00:46:24:169] **Speaker 1:** Our assembly matrix for a frame.
[00:46:25:419 - 00:46:26:899] **Speaker 1:** So the number of columns is equal to the number
[00:46:26:899 - 00:46:29:179] **Speaker 1:** of degrees of freedom in global coordinates, so that is
[00:46:29:179 - 00:46:30:479] **Speaker 1:** always 6.
[00:46:32:040 - 00:46:34:120] **Speaker 1:** Degrees of freedom for a frame, so there's 6 degrees
[00:46:34:120 - 00:46:35:659] **Speaker 1:** of freedom, so 6 columns.
[00:46:36:689 - 00:46:39:000] **Speaker 1:** And then, just like last week, the number of rows.
[00:46:39:810 - 00:46:42:550] **Speaker 1:** is dependent on the size of the particular problem and
[00:46:42:550 - 00:46:45:439] **Speaker 1:** the number of global degrees of freedom that exists today.
[00:46:46:870 - 00:46:49:659] **Speaker 1:** Then we have our overall um stiffness equation just like
[00:46:49:659 - 00:46:50:199] **Speaker 1:** we did before.
[00:46:52:979 - 00:46:55:919] **Speaker 1:** So we can, if we wanted to, we can constrain
[00:46:56:340 - 00:46:58:899] **Speaker 1:** a solution to make a frame behave like a beam
[00:46:58:899 - 00:47:03:659] **Speaker 1:** and just constrain our force axial rigidity, um, but essentially
[00:47:03:659 - 00:47:05:879] **Speaker 1:** the frame supersedes the beam element.
[00:47:06:600 - 00:47:08:300] **Speaker 1:** uh, and the beam element was really just a stepping
[00:47:08:300 - 00:47:10:120] **Speaker 1:** stone to get a derivation in place.
[00:47:12:719 - 00:47:15:449] **Speaker 1:** The numbering sequence is very important and the reason it's
[00:47:15:449 - 00:47:19:449] **Speaker 1:** important is that um this numbering sequence is is how
[00:47:19:449 - 00:47:20:290] **Speaker 1:** this was derived.
[00:47:20:399 - 00:47:22:050] **Speaker 1:** If we'd chosen something different, the numbers would be in
[00:47:22:050 - 00:47:22:689] **Speaker 1:** a different order.
[00:47:23:010 - 00:47:26:330] **Speaker 1:** So if we're gonna use this, we need to use
[00:47:26:330 - 00:47:27:330] **Speaker 1:** this numbering sequence.
[00:47:28:580 - 00:47:32:020] **Speaker 1:** So local X, Y, local Z at node 1, D1
[00:47:32:020 - 00:47:35:250] **Speaker 1:** to D3, D4 to D6 in the same sequence at
[00:47:35:250 - 00:47:35:840] **Speaker 1:** node 2.
[00:47:36:800 - 00:47:40:159] **Speaker 1:** And then, in global coordinates, it's the same sequence but
[00:47:40:159 - 00:47:42:840] **Speaker 1:** they refer to the global X, Y, and Z rather
[00:47:42:840 - 00:47:44:199] **Speaker 1:** than the local X Y and Z.
[00:47:45:689 - 00:47:48:489] **Speaker 1:** So just like we did, so this numbering sequence really
[00:47:48:489 - 00:47:49:280] **Speaker 1:** is very important.
[00:47:50:949 - 00:47:53:350] **Speaker 1:** So in this case here, our alpha for this element
[00:47:53:350 - 00:47:55:610] **Speaker 1:** would be a zero degree transformation angle.
[00:47:56:889 - 00:48:00:209] **Speaker 1:** In this case here, uh, alpha would be say 30
[00:48:00:209 - 00:48:00:629] **Speaker 1:** degrees.
[00:48:01:489 - 00:48:06:250] **Speaker 1:** So, the local, Um, coordinate systems, the lowercase ones are
[00:48:06:250 - 00:48:09:379] **Speaker 1:** always aligned with the element, whereas here they're always aligned
[00:48:09:379 - 00:48:10:580] **Speaker 1:** with the global coordinates.
[00:48:13:459 - 00:48:16:389] **Speaker 1:** In this case here, we may have say an alpha,
[00:48:17:020 - 00:48:19:360] **Speaker 1:** which is 340 degrees.
[00:48:21:260 - 00:48:24:080] **Speaker 1:** Or defining it as -20 degrees.
[00:48:25:760 - 00:48:28:719] **Speaker 1:** And then this one here, this would be so we
[00:48:28:719 - 00:48:31:040] **Speaker 1:** same exact same sequence we've done, we start aligned with
[00:48:31:040 - 00:48:35:840] **Speaker 1:** X global, we rotate counterclockwise into where we're aligned with
[00:48:35:840 - 00:48:37:979] **Speaker 1:** X for the element so we'd be going 90.
[00:48:39:360 - 00:48:41:239] **Speaker 1:** And a bit short of 180, so this might be
[00:48:41:239 - 00:48:43:159] **Speaker 1:** alpha of 160 degrees.
[00:48:43:590 - 00:48:46:709] **Speaker 1:** So, different element type now for the exact same process
[00:48:46:709 - 00:48:49:600] **Speaker 1:** there and just, this is quite a good reference page
[00:48:49:600 - 00:48:52:520] **Speaker 1:** in terms of the left column is all the numbering
[00:48:52:520 - 00:48:56:860] **Speaker 1:** and local coordinates, and then the right-hand page is all
[00:48:57:320 - 00:48:58:639] **Speaker 1:** the numbers in.
[00:48:59:709 - 00:49:00:949] **Speaker 1:** The global coordinates.
[00:49:03:790 - 00:49:05:909] **Speaker 1:** Now, this page is just a summary of all the
[00:49:05:909 - 00:49:07:479] **Speaker 1:** steps and all the equations.
[00:49:08:070 - 00:49:09:739] **Speaker 1:** Uh, we can go through this more, but this is
[00:49:09:739 - 00:49:12:909] **Speaker 1:** essentially this page could equally have been presented other than
[00:49:12:909 - 00:49:15:419] **Speaker 1:** the, the numbers here in terms of the sizes.
[00:49:15:820 - 00:49:17:429] **Speaker 1:** This is the same page we could have used last
[00:49:17:429 - 00:49:17:889] **Speaker 1:** week.
[00:49:18:510 - 00:49:19:590] **Speaker 1:** Everything carries across.
[00:49:19:870 - 00:49:24:030] **Speaker 1:** So, um, yeah, that's nothing you've learned in the last
[00:49:24:030 - 00:49:25:149] **Speaker 1:** few weeks is wasted here.
[00:49:25:270 - 00:49:26:790] **Speaker 1:** We're just building upon it, um.
[00:49:27:449 - 00:49:28:620] **Speaker 1:** That's actually a good place to stop.
[00:49:28:699 - 00:49:30:560] **Speaker 1:** What we'll do is we'll jump work through an example
[00:49:31:100 - 00:49:33:310] **Speaker 1:** in the lecture tomorrow and then that will be the,
[00:49:33:330 - 00:49:36:280] **Speaker 1:** the, the basis of the lab tomorrow afternoon.
[00:49:36:540 - 00:49:38:419] **Speaker 1:** So thank you all for coming and I'll see you
[00:49:38:419 - 00:49:39:020] **Speaker 1:** again tomorrow.
[00:50:20:659 - 00:50:20:679] **Speaker 0:** Thanks.
[00:50:28:530 - 00:50:29:080] **Speaker 0:** I I can do.
[00:50:31:659 - 00:50:37:580] **Speaker 0:** it's different from what it has to it's not like.
[00:50:39:159 - 00:50:39:179] **Speaker 0:** Thank you.
[00:50:53:370 - 00:50:53:600] **Speaker 0:** Awesome.
[00:50:58:199 - 00:51:05:379] **Speaker 0:** I guess I should, I wouldn't get to sleep on
[00:51:05:379 - 00:51:05:879] **Speaker 0:** this thing.
[00:51:06:080 - 00:51:08:489] **Speaker 0:** Would you guys treat it as a thing that's like
[00:51:08:489 - 00:51:09:169] **Speaker 0:** that as well.
[00:51:12:000 - 00:51:20:199] **Speaker 0:** So this is a bar, um, we have, um, so
[00:51:20:199 - 00:51:20:239] **Speaker 0:** she had like a.
[00:51:20:969 - 00:51:22:929] **Speaker 0:** Yep, but the candles with the frame on and we'll
[00:51:22:929 - 00:51:25:139] **Speaker 0:** get that right in the end, and we can actually
[00:51:26:149 - 00:51:30:729] **Speaker 0:** take the frame on that and make it.
[00:51:31:370 - 00:51:37:770] **Speaker 0:** It's kind of yeah so you like people know people
[00:51:44:129 - 00:51:50:979] **Speaker 0:** you can thank you for your help.
[00:51:56:060 - 00:51:56:110] **Speaker 0:** I can yeah, yeah.
[00:51:56:520 - 00:51:56:560] **Speaker 0:** I haven't.
[00:51:59:040 - 00:51:59:790] **Speaker 0:** Well, no, I don't think it's fair enough.
[00:52:00:000 - 00:52:05:800] **Speaker 0:** I wouldn't, um, problem like we have, uh, continuous memories,
[00:52:05:879 - 00:52:09:439] **Speaker 0:** so that's continuous across the members to need to break
[00:52:09:439 - 00:52:10:469] **Speaker 0:** the right.
[00:52:28:159 - 00:52:28:560] **Speaker 0:** Oh fine.
[00:52:34:379 - 00:52:34:719] **Speaker 0:** This is.
[00:52:39:290 - 00:52:41:310] **Speaker 0:** Using the document camera or the computer?
[00:52:42:120 - 00:52:45:610] **Speaker 1:** Good question, because this, this like died on me halfway
[00:52:45:610 - 00:52:45:929] **Speaker 1:** through.
[00:52:46:520 - 00:52:48:709] **Speaker 1:** But if you, I just pass cycled it and it
[00:52:48:709 - 00:52:49:030] **Speaker 1:** came back.
[00:52:49:159 - 00:52:52:600] **Speaker 0:** So if it does just reboot, yeah, if it does
[00:52:52:600 - 00:52:56:060] **Speaker 1:** happen to you, yeah, just, just, you know, pass up
[00:52:56:060 - 00:52:59:879] **Speaker 1:** seemed to bring it back as most things do when
[00:52:59:879 - 00:53:00:520] **Speaker 1:** you reboot.
[00:53:00:600 - 00:53:01:989] **Speaker 1:** Well, it's sort of that cliche about have you tried
[00:53:01:989 - 00:53:03:800] **Speaker 1:** turning off and on again, but it's because often it
[00:53:03:800 - 00:53:03:850] **Speaker 1:** does, yeah, yeah.
[00:53:06:120 - 00:53:07:500] **Speaker 0:** What have you been doing in here?
[00:53:08:379 - 00:53:11:010] **Speaker 1:** Um, it's a 3rd year mecca sharing plans.
[00:53:11:189 - 00:53:11:500] **Speaker 1:** Oh, cool.
[00:53:12:129 - 00:53:12:479] **Speaker 0:** Awesome.
[00:53:12:679 - 00:53:16:479] **Speaker 0:** First year accounting, probably not a little bit different.
[00:53:16:689 - 00:53:21:250] **Speaker 1:** Probably not too many, sometimes you get them, but it's
[00:53:21:250 - 00:53:21:709] **Speaker 1:** pretty rare.
[00:53:22:090 - 00:53:23:449] **Speaker 1:** Yeah, definitely.
[00:53:23:919 - 00:53:24:330] **Speaker 0:** Oh, good luck.
[00:53:24:530 - 00:53:25:459] **Speaker 0:** OK, thank you.
[00:54:11:020 - 00:54:11:300] **Speaker 0:** I.
[00:54:22:270 - 00:54:22:719] **Speaker 0:** delivery

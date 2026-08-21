# ENME302-26S2 Lecture 23 native Echo transcript

Date: August 20, 2026 10:00am-10:55am
Transcript type: native Echo automated transcript.

[00:00:03:960 - 00:00:03:970] **Speaker 0:** Like.
[00:00:09:920 - 00:00:19:750] **Speaker 0:** That yeah.
[00:00:37:060 - 00:00:48:759] **Speaker 0:** I but Oh Oh.
[00:01:00:060 - 00:01:02:389] **Speaker 0:** Well, Karakoto, welcome along, everyone.
[00:01:05:619 - 00:01:07:658] **Speaker 1:** Um, unfortunately, you haven't seen the end of me just
[00:01:07:658 - 00:01:08:039] **Speaker 1:** yet.
[00:01:10:870 - 00:01:11:370] **Speaker 0:** Um.
[00:01:12:139 - 00:01:13:300] **Speaker 1:** First of all, I just want to apologise for all
[00:01:13:300 - 00:01:14:930] **Speaker 1:** the issues we had on Tuesday evening.
[00:01:15:540 - 00:01:17:940] **Speaker 1:** Um, we've done a lot of work in the background
[00:01:17:940 - 00:01:20:540] **Speaker 1:** around, um, all the setup of virtual environments and a
[00:01:20:540 - 00:01:21:300] **Speaker 1:** lot of testing on that.
[00:01:21:410 - 00:01:24:180] **Speaker 1:** One thing I guess working with digital services that we
[00:01:24:180 - 00:01:27:339] **Speaker 1:** couldn't truly replicate in the testing ahead of time was,
[00:01:27:779 - 00:01:30:370] **Speaker 1:** um, the demand that went when everyone logged in at
[00:01:30:370 - 00:01:30:540] **Speaker 1:** once.
[00:01:30:639 - 00:01:33:330] **Speaker 1:** It was the first time, um, that, that basically the
[00:01:33:330 - 00:01:34:819] **Speaker 1:** entire classes all working on this at once.
[00:01:35:019 - 00:01:37:970] **Speaker 1:** So, um, yeah, it was a bit of a, um,
[00:01:37:980 - 00:01:39:739] **Speaker 1:** disaster in terms of all those delays and I.
[00:01:40:220 - 00:01:42:540] **Speaker 1:** Really sorry the, um, all the messing around they had
[00:01:42:540 - 00:01:43:019] **Speaker 1:** on the night.
[00:01:43:209 - 00:01:44:459] **Speaker 1:** Um, it was like a bit of a game of
[00:01:44:459 - 00:01:47:379] **Speaker 1:** whack a mole when every, every time we solve one
[00:01:47:379 - 00:01:50:209] **Speaker 1:** problem, something else popped up somewhere else, um, and we
[00:01:50:209 - 00:01:51:940] **Speaker 1:** were running around across 7 different rooms to try and
[00:01:51:940 - 00:01:52:940] **Speaker 1:** resolve all those things.
[00:01:53:059 - 00:01:56:139] **Speaker 1:** So, um, yeah, really sorry about the, the hassle and
[00:01:56:139 - 00:01:57:500] **Speaker 1:** the stress that that caused on Tuesday.
[00:01:58:709 - 00:02:01:790] **Speaker 1:** Um, I also want to just talk through the assignment.
[00:02:02:750 - 00:02:04:769] **Speaker 0:** So, I might just back this off a little bit.
[00:02:06:250 - 00:02:09:410] **Speaker 1:** So, um, this is just the assignment for, um, so
[00:02:09:410 - 00:02:10:750] **Speaker 1:** due just after the term break.
[00:02:11:210 - 00:02:13:050] **Speaker 1:** Um, it is up on the course learn page I
[00:02:13:050 - 00:02:14:029] **Speaker 1:** put up late yesterday.
[00:02:14:289 - 00:02:15:869] **Speaker 1:** Um, I had hoped to get up earlier in the
[00:02:15:869 - 00:02:16:000] **Speaker 1:** day.
[00:02:16:050 - 00:02:18:130] **Speaker 1:** I just wanted to work through it and make sure
[00:02:18:130 - 00:02:21:649] **Speaker 1:** that, um, everything sort of worked out, um, broadly as
[00:02:21:649 - 00:02:22:050] **Speaker 1:** planned.
[00:02:22:369 - 00:02:24:410] **Speaker 1:** So, um, this is the structure.
[00:02:24:449 - 00:02:26:429] **Speaker 1:** So this is a, a fixed support on the left,
[00:02:26:649 - 00:02:28:130] **Speaker 1:** um, the entire structure is frame elements.
[00:02:28:240 - 00:02:32:429] **Speaker 1:** There's gonna be, uh, 1234567 frame elements within there.
[00:02:32:899 - 00:02:37:470] **Speaker 1:** Um, these are the dimensions of keynodal points and, um,
[00:02:37:479 - 00:02:39:600] **Speaker 1:** it's gonna you can do a 2D analysis on this.
[00:02:39:679 - 00:02:41:839] **Speaker 1:** So it's essentially using the frame on the code you've
[00:02:41:839 - 00:02:42:339] **Speaker 1:** already got.
[00:02:43:919 - 00:02:46:649] **Speaker 1:** Um, modelling the structure using 7 frame elements assume the
[00:02:46:649 - 00:02:48:339] **Speaker 1:** connecting elements are rigidly welded together.
[00:02:48:679 - 00:02:51:940] **Speaker 1:** Um, so everything's, uh, frame elements and it's all conventional,
[00:02:52:199 - 00:02:55:779] **Speaker 1:** um, assumptions there that everything's rigidly connected and translates and
[00:02:55:779 - 00:02:56:600] **Speaker 1:** rotates together.
[00:02:57:660 - 00:03:00:589] **Speaker 1:** Um, assume that everything's made of, so these two spots
[00:03:00:589 - 00:03:02:460] **Speaker 1:** on the left are fixed, we're assuming that everything's made
[00:03:02:460 - 00:03:06:220] **Speaker 1:** of steel, has a sheer modules of 200 gigascal, sorry,
[00:03:06:460 - 00:03:09:449] **Speaker 1:** elastic modules of 200 gigasscal and a shear modules of
[00:03:09:449 - 00:03:10:779] **Speaker 1:** 77 gigascal.
[00:03:11:130 - 00:03:11:419] **Speaker 1:** So.
[00:03:12:059 - 00:03:15:139] **Speaker 1:** Um, every element has the same circular hollow cross section,
[00:03:15:619 - 00:03:18:259] **Speaker 1:** uh, with an outside diameter of 100 millimetres and an
[00:03:18:259 - 00:03:19:779] **Speaker 1:** inside diameter of 90 millimetres.
[00:03:20:880 - 00:03:24:779] **Speaker 1:** Um, and then PXT reports, um, sketch preferably by hand,
[00:03:25:039 - 00:03:27:490] **Speaker 1:** um, I say that just because I know how time-consuming
[00:03:27:789 - 00:03:30:679] **Speaker 1:** it can be to draw, um, up threebo diagrams with
[00:03:30:679 - 00:03:33:039] **Speaker 1:** all the degrees of freedom on them, um, within a
[00:03:33:039 - 00:03:33:240] **Speaker 1:** computer.
[00:03:33:360 - 00:03:35:789] **Speaker 1:** So, um, by hand, could be a scanned piece of
[00:03:35:789 - 00:03:37:729] **Speaker 1:** paper, it could be just drop sketching it on a
[00:03:37:729 - 00:03:40:339] **Speaker 1:** one note file, um, on a tablet, anything like that.
[00:03:40:679 - 00:03:43:740] **Speaker 1:** Um, really just the, that is to try and reduce
[00:03:43:740 - 00:03:45:399] **Speaker 1:** the, the burden on you to draw them.
[00:03:46:220 - 00:03:48:830] **Speaker 1:** Um, it's the overall structure of the global degrees of
[00:03:48:830 - 00:03:49:089] **Speaker 1:** freedom.
[00:03:49:979 - 00:03:53:199] **Speaker 1:** Um, for each element, showing the element degrees of freedom
[00:03:53:199 - 00:03:54:419] **Speaker 1:** as well as the overall structure.
[00:03:55:130 - 00:03:59:460] **Speaker 1:** Um, you can photograph or scan, hand-drawn sketches, um.
[00:04:01:169 - 00:04:02:940] **Speaker 1:** Present the corresponding assembly matrix for each element.
[00:04:03:500 - 00:04:05:539] **Speaker 1:** Now you can just copy and paste the matrices from
[00:04:05:539 - 00:04:09:059] **Speaker 1:** Python, um, you know, format the outputs and then just
[00:04:09:059 - 00:04:10:729] **Speaker 1:** present that just whatever way is easiest.
[00:04:10:850 - 00:04:12:139] **Speaker 1:** So I'm, I'm trying to just give you a little
[00:04:12:139 - 00:04:14:979] **Speaker 1:** leeway there to, um, you know, try and do that
[00:04:14:979 - 00:04:16:640] **Speaker 1:** in the least burdensome way, um.
[00:04:17:648 - 00:04:23:549] **Speaker 1:** The um This assembly measures are also within the appendix
[00:04:23:549 - 00:04:24:209] **Speaker 1:** to your report.
[00:04:24:510 - 00:04:27:500] **Speaker 1:** Um, so the first thing I'm gonna do is, um,
[00:04:27:510 - 00:04:32:029] **Speaker 1:** sort of broadly and very simply model the, um, wind
[00:04:32:029 - 00:04:33:510] **Speaker 1:** loading based upon two point loads.
[00:04:33:619 - 00:04:35:429] **Speaker 1:** So we've got a structure like this and we've got
[00:04:35:429 - 00:04:37:390] **Speaker 1:** the point loads that are applied to us, um.
[00:04:38:100 - 00:04:39:730] **Speaker 1:** So well the deflection components at the top end of
[00:04:39:730 - 00:04:40:140] **Speaker 1:** the structure.
[00:04:40:299 - 00:04:42:260] **Speaker 1:** So up here, just asking what the how much that
[00:04:42:260 - 00:04:45:339] **Speaker 1:** tip deflects from that loading case, um.
[00:04:46:429 - 00:04:48:910] **Speaker 1:** Determine the reaction forces of the two supports from your
[00:04:48:910 - 00:04:49:730] **Speaker 1:** Python code.
[00:04:50:470 - 00:04:52:670] **Speaker 1:** Uh, present the results in a sketch of the support
[00:04:52:670 - 00:04:56:190] **Speaker 1:** points from the reaction components, um, present perform an overall
[00:04:56:190 - 00:04:58:709] **Speaker 1:** equilibrium analysis of the structure to check the accuracy of
[00:04:58:709 - 00:04:59:350] **Speaker 1:** reaction loads.
[00:04:59:390 - 00:05:02:119] **Speaker 1:** Like, basically what we're doing here is just taking the
[00:05:02:119 - 00:05:03:790] **Speaker 1:** treating the whole structure is just a rigid block.
[00:05:04:149 - 00:05:06:769] **Speaker 1:** There's some loads in here and there's some reactions here.
[00:05:07:109 - 00:05:08:390] **Speaker 1:** And do they make sense?
[00:05:08:470 - 00:05:10:290] **Speaker 1:** Does the structure appear to be an equilibrium?
[00:05:10:410 - 00:05:14:950] **Speaker 1:** So, um, if it doesn't, then maybe the structure is
[00:05:14:950 - 00:05:16:429] **Speaker 1:** not quite set up the way you think it is.
[00:05:16:510 - 00:05:17:869] **Speaker 1:** That's a good check.
[00:05:18:730 - 00:05:20:140] **Speaker 1:** Um, and I have just made a note here.
[00:05:20:220 - 00:05:22:619] **Speaker 1:** So when I'm saying, asking you to do that, um,
[00:05:22:980 - 00:05:24:859] **Speaker 1:** I'm not asking you to go through and solve the
[00:05:24:859 - 00:05:26:859] **Speaker 1:** force in every member through the structure.
[00:05:27:100 - 00:05:30:179] **Speaker 1:** So, um, just say you treat the trust, you can
[00:05:30:179 - 00:05:32:679] **Speaker 1:** treat the entire trusts like a rigid block and consider
[00:05:32:899 - 00:05:34:220] **Speaker 1:** only the externally applied loads.
[00:05:34:299 - 00:05:36:290] **Speaker 1:** So I'm not asking you to go through and work
[00:05:36:290 - 00:05:38:299] **Speaker 1:** it out by hand the force of this member or
[00:05:38:299 - 00:05:39:459] **Speaker 1:** this member or this member.
[00:05:39:820 - 00:05:43:980] **Speaker 1:** Basically just forces in, um, forces here and then see
[00:05:43:980 - 00:05:47:820] **Speaker 1:** if If that makes sense, but not tracing individual forces
[00:05:47:820 - 00:05:49:739] **Speaker 1:** at moments all the way through there because essentially the
[00:05:49:739 - 00:05:51:820] **Speaker 1:** only way you could do that would be to just
[00:05:51:820 - 00:05:55:420] **Speaker 1:** replicate, um, the entire fun element method and solving a
[00:05:55:420 - 00:05:57:260] **Speaker 1:** 15 by 15 matrix by hand.
[00:05:57:660 - 00:05:59:940] **Speaker 1:** Um, that's, yeah, it's not realistic, so.
[00:06:01:079 - 00:06:05:049] **Speaker 1:** Um, for an overall week analysis at the three critical
[00:06:05:049 - 00:06:05:399] **Speaker 1:** points.
[00:06:05:649 - 00:06:08:010] **Speaker 1:** So point A, so that one's going to be relatively
[00:06:08:010 - 00:06:08:170] **Speaker 1:** simple.
[00:06:08:250 - 00:06:11:410] **Speaker 1:** You're just looking at one element, um, you're just checking
[00:06:11:410 - 00:06:14:670] **Speaker 1:** within that element that you've got this force of 2000
[00:06:14:670 - 00:06:15:369] **Speaker 1:** Newtons.
[00:06:15:890 - 00:06:18:440] **Speaker 1:** It's at a distance of 0.5 metre.
[00:06:18:489 - 00:06:21:290] **Speaker 1:** So you'd expect a 1 kilton metre moment and you'd
[00:06:21:290 - 00:06:25:429] **Speaker 1:** expect a 2000 Newton reaction load, um, and then also
[00:06:25:559 - 00:06:26:489] **Speaker 1:** at points B and C.
[00:06:26:529 - 00:06:30:670] **Speaker 1:** So what you're doing here, for example, is just taking
[00:06:31:049 - 00:06:37:720] **Speaker 1:** This He's here You've got a load in here and
[00:06:37:720 - 00:06:40:339] **Speaker 1:** a load here, and then you've got some sort of
[00:06:40:720 - 00:06:41:720] **Speaker 1:** reaction load.
[00:06:42:309 - 00:06:43:170] **Speaker 1:** And moment here.
[00:06:45:480 - 00:06:47:570] **Speaker 1:** And you've got to work out, you know.
[00:06:48:250 - 00:06:48:950] **Speaker 1:** What they should be.
[00:06:49:109 - 00:06:52:450] **Speaker 1:** It's not a particularly complicated calculation and just checking the
[00:06:52:450 - 00:06:55:369] **Speaker 1:** values you get within the short element at that end
[00:06:55:369 - 00:06:58:130] **Speaker 1:** of the element match the values that you'd expect.
[00:06:58:290 - 00:07:00:940] **Speaker 1:** So just doing a few checks through the structure, um,
[00:07:01:010 - 00:07:02:089] **Speaker 1:** the same thing at point C.
[00:07:03:359 - 00:07:05:760] **Speaker 1:** So just taking the, the upper half of the structure
[00:07:05:760 - 00:07:07:679] **Speaker 1:** and working out what you would expect the reactions to
[00:07:07:679 - 00:07:09:829] **Speaker 1:** be there and just checking that that's the values you
[00:07:09:829 - 00:07:12:880] **Speaker 1:** actually get within this this element forcing two vector.
[00:07:14:290 - 00:07:16:290] **Speaker 1:** So it's just a few, few key checks at critical
[00:07:16:290 - 00:07:17:329] **Speaker 1:** points, um.
[00:07:18:140 - 00:07:20:529] **Speaker 1:** I'm asking you to calculate the, the stress induced within
[00:07:20:529 - 00:07:22:890] **Speaker 1:** each element by combining the absolute normal stress due to
[00:07:22:890 - 00:07:25:119] **Speaker 1:** axial loading and the absolute normal stress from bending.
[00:07:26:269 - 00:07:29:329] **Speaker 1:** Such that sigma total is equal to the absolute value
[00:07:29:329 - 00:07:31:459] **Speaker 1:** sigma axial and the absolute value of sigma bending.
[00:07:31:619 - 00:07:37:179] **Speaker 1:** Now that's based upon, um, within a circular hollow circular
[00:07:37:179 - 00:07:39:250] **Speaker 1:** cross section, so this element like this.
[00:07:40:329 - 00:07:43:369] **Speaker 1:** And there's some sort of wall thickness here, so 100
[00:07:43:369 - 00:07:45:510] **Speaker 1:** millimetre outside, 90 millimetre internal.
[00:07:46:320 - 00:07:48:950] **Speaker 1:** That when you have both a, you might have a.
[00:07:49:600 - 00:07:53:450] **Speaker 1:** A sheer force, an axial force, and a moment on
[00:07:53:450 - 00:07:53:929] **Speaker 1:** here.
[00:07:55:070 - 00:08:01:630] **Speaker 1:** The um ship, what you're gonna have is 3, 3
[00:08:02:049 - 00:08:02:600] **Speaker 1:** stress profiles.
[00:08:02:649 - 00:08:04:709] **Speaker 1:** You can have a sort of parabolic.
[00:08:05:820 - 00:08:08:470] **Speaker 1:** Profile for share.
[00:08:09:709 - 00:08:14:790] **Speaker 1:** Then you're gonna have a bending profile, so linearly varying
[00:08:14:790 - 00:08:16:929] **Speaker 1:** bending, uh, normal stresses from bending.
[00:08:20:089 - 00:08:23:690] **Speaker 1:** And There's also the axial.
[00:08:25:510 - 00:08:26:429] **Speaker 1:** Normal stress.
[00:08:29:670 - 00:08:33:190] **Speaker 1:** Now, we're not gonna explicitly consider share just because that's
[00:08:33:190 - 00:08:35:260] **Speaker 1:** got a peak value with the bending stress is zero.
[00:08:35:830 - 00:08:37:549] **Speaker 1:** So that's supposed to be a symmetric profile even though
[00:08:37:549 - 00:08:38:549] **Speaker 1:** it doesn't quite look like it.
[00:08:39:479 - 00:08:48:030] **Speaker 1:** Um, So Um, yeah, in a, in a strict sense,
[00:08:48:109 - 00:08:49:989] **Speaker 1:** we should do like a von Mises calculation at every
[00:08:49:989 - 00:08:52:289] **Speaker 1:** point within the cross section and we should check, uh,
[00:08:52:299 - 00:08:54:109] **Speaker 1:** as this falls away and this ramps up.
[00:08:54:260 - 00:08:57:229] **Speaker 1:** Um, but between these two components, this is increasing linearly,
[00:08:57:309 - 00:08:58:830] **Speaker 1:** this is decreasing parabolically.
[00:08:59:270 - 00:09:01:429] **Speaker 1:** So this is decreasing at a greater rate than this
[00:09:01:429 - 00:09:02:070] **Speaker 1:** is increasing.
[00:09:02:309 - 00:09:05:750] **Speaker 1:** So, um, we're just gonna ignore the share component and
[00:09:05:750 - 00:09:08:179] **Speaker 1:** only consider the bending in normal stress components.
[00:09:08:630 - 00:09:11:500] **Speaker 1:** And because of the fact that this is a, um,
[00:09:11:700 - 00:09:12:799] **Speaker 1:** symmetric cross section.
[00:09:13:380 - 00:09:15:700] **Speaker 1:** And the distance to the outermost compressive fibre and the
[00:09:15:700 - 00:09:18:219] **Speaker 1:** outermost tensile fibre is the same distance.
[00:09:18:659 - 00:09:21:159] **Speaker 1:** That means that the peak compressive bending stress and the
[00:09:21:359 - 00:09:23:299] **Speaker 1:** peak tensile bending stress are going to be the same
[00:09:23:299 - 00:09:24:000] **Speaker 1:** magnitude.
[00:09:24:539 - 00:09:26:440] **Speaker 1:** So we can just take the absolute value of that
[00:09:26:539 - 00:09:29:020] **Speaker 1:** and the absolute value of the normal stress and add
[00:09:29:020 - 00:09:29:760] **Speaker 1:** them together.
[00:09:30:390 - 00:09:32:770] **Speaker 1:** Um, if I was to have given you a T-shaped
[00:09:32:770 - 00:09:33:780] **Speaker 1:** asymmetric section.
[00:09:34:489 - 00:09:36:729] **Speaker 1:** Then you'd end up with a different pos, a different
[00:09:36:729 - 00:09:40:940] **Speaker 1:** tensile and compressive, um, normal stress magnitude here and you'd
[00:09:40:940 - 00:09:41:729] **Speaker 1:** have to keep track.
[00:09:41:849 - 00:09:43:609] **Speaker 1:** There'd be a whole lot of bookkeeping in terms of
[00:09:43:609 - 00:09:45:260] **Speaker 1:** is this tensile, is this compressive.
[00:09:45:570 - 00:09:47:169] **Speaker 1:** You'd also then have to look at your axial normal
[00:09:47:169 - 00:09:49:119] **Speaker 1:** stress and say, is that tensile or compressive?
[00:09:49:369 - 00:09:50:770] **Speaker 1:** Does it counteract is that together.
[00:09:51:090 - 00:09:53:489] **Speaker 1:** There'd be a whole lot more bookkeeping without really a
[00:09:53:489 - 00:09:55:969] **Speaker 1:** lot of extra learning outcome from it, which is why
[00:09:55:969 - 00:09:58:080] **Speaker 1:** I've given you a symmetric section just so you can
[00:09:58:080 - 00:10:01:289] **Speaker 1:** basically that enables us to be able to use this
[00:10:01:289 - 00:10:05:400] **Speaker 1:** more simplified version, which is just Adding together the absolute
[00:10:05:400 - 00:10:06:679] **Speaker 1:** values here, um.
[00:10:07:900 - 00:10:09:859] **Speaker 1:** There is the approximation that we're ignoring share, but that
[00:10:09:859 - 00:10:11:640] **Speaker 1:** is actually a relatively valid one.
[00:10:13:080 - 00:10:15:210] **Speaker 1:** In the presence of axial loads, there can be maybe
[00:10:15:210 - 00:10:16:609] **Speaker 1:** a very slight um.
[00:10:17:530 - 00:10:22:169] **Speaker 1:** You know, a non-conservative assumption there, um, but it's just
[00:10:22:169 - 00:10:25:849] **Speaker 1:** gonna be too complicated to have to, um, Yeah, go
[00:10:25:849 - 00:10:28:570] **Speaker 1:** into a full von Messy's calculation there, um, at every
[00:10:28:570 - 00:10:29:609] **Speaker 1:** point within the cross section.
[00:10:31:429 - 00:10:33:510] **Speaker 1:** The distance to the outermost fibre for many calculations is
[00:10:33:510 - 00:10:35:929] **Speaker 1:** half the outside diameter of the cross section, which is,
[00:10:35:950 - 00:10:39:369] **Speaker 1:** um, the cross sections 100 metres outside diameter.
[00:10:39:750 - 00:10:41:869] **Speaker 1:** So C's gonna be 50 millimetres, um.
[00:10:42:890 - 00:10:44:969] **Speaker 1:** And just asking here, what is the maximum total normal
[00:10:44:969 - 00:10:47:390] **Speaker 1:** stress induced anywhere in the structure due to this loading
[00:10:47:390 - 00:10:47:849] **Speaker 1:** case?
[00:10:48:330 - 00:10:51:289] **Speaker 1:** Identify which element the maximum stress occurs in and where
[00:10:51:289 - 00:10:54:270] **Speaker 1:** within that element this maximum total normal stress occurs.
[00:10:55:539 - 00:10:57:760] **Speaker 1:** From there we're gonna jump across to some wind loading.
[00:10:58:219 - 00:11:03:299] **Speaker 1:** So we're gonna subject uh sign board to a nice
[00:11:03:299 - 00:11:04:539] **Speaker 1:** normal wind load.
[00:11:04:940 - 00:11:06:900] **Speaker 1:** Um, we're gonna assume the frame supports a distance of
[00:11:06:900 - 00:11:08:359] **Speaker 1:** 3 metres into the page.
[00:11:09:700 - 00:11:13:559] **Speaker 1:** And then um we've got some different wind loading regions,
[00:11:14:020 - 00:11:17:299] **Speaker 1:** um, we're gonna apply some different regions, different rates of
[00:11:17:299 - 00:11:17:859] **Speaker 1:** wind loading.
[00:11:19:280 - 00:11:22:479] **Speaker 1:** Um, So this is the same structure.
[00:11:22:619 - 00:11:24:130] **Speaker 1:** All we're doing now is changing the loading slide.
[00:11:24:260 - 00:11:27:330] **Speaker 1:** We're putting some uniformly distributed loads onto two elements, and
[00:11:27:330 - 00:11:30:460] **Speaker 1:** they're gonna be lumped into equivalent nodal loads there, there
[00:11:30:789 - 00:11:31:340] **Speaker 1:** and there.
[00:11:32:760 - 00:11:34:599] **Speaker 1:** And then, um, there's a few analysis.
[00:11:34:719 - 00:11:37:599] **Speaker 1:** So, uh, maximum wind speed for a low zone, which
[00:11:37:599 - 00:11:40:510] **Speaker 1:** is the 115 kilometres an hour given here or 32
[00:11:40:510 - 00:11:41:299] **Speaker 1:** metres per second.
[00:11:42:609 - 00:11:44:880] **Speaker 1:** Um, was blowing directly onto the sign face, what would
[00:11:44:880 - 00:11:47:570] **Speaker 1:** the maximum normal stress on the frame be and which
[00:11:47:570 - 00:11:49:369] **Speaker 1:** element would it occur in, um.
[00:11:50:190 - 00:11:51:919] **Speaker 1:** Or the total reflections at the top of the frame,
[00:11:52:419 - 00:11:52:820] **Speaker 1:** um.
[00:11:53:809 - 00:11:57:400] **Speaker 1:** Then if the um yield stress of the frame is
[00:11:57:400 - 00:11:59:869] **Speaker 1:** 350 megapascale and you're requiring a factor of safety of
[00:11:59:869 - 00:12:02:609] **Speaker 1:** at least 2.5, what is the maximum wind speed you'd
[00:12:02:609 - 00:12:05:780] **Speaker 1:** rate the sign capable of withstanding, assuming the wind blows
[00:12:05:780 - 00:12:07:690] **Speaker 1:** directly onto the face of the sign and consider a
[00:12:07:690 - 00:12:10:270] **Speaker 1:** maximum total normal stress as the defining stress value.
[00:12:11:059 - 00:12:13:760] **Speaker 1:** A fiction components um and the reaction forces for that
[00:12:13:760 - 00:12:17:760] **Speaker 1:** loading case, so, Um, for that point, for that step,
[00:12:18:159 - 00:12:21:539] **Speaker 1:** essentially the numbers in this equation, um, come from, sorry,
[00:12:21:640 - 00:12:24:200] **Speaker 1:** the numbers in this table come from this equation here,
[00:12:24:280 - 00:12:26:719] **Speaker 1:** which is the, the wind speed expressed in metres per
[00:12:26:719 - 00:12:31:159] **Speaker 1:** second squared times 0.6 is the pressure in Pascal that
[00:12:31:159 - 00:12:33:280] **Speaker 1:** gets applied to the, to the frame.
[00:12:39:809 - 00:12:41:950] **Speaker 1:** Then we have the sensitivity to the oil we normally
[00:12:41:950 - 00:12:42:820] **Speaker 1:** be bedding assumption.
[00:12:43:130 - 00:12:45:890] **Speaker 1:** So, um, we do, when we set this up, we
[00:12:45:890 - 00:12:50:179] **Speaker 1:** do assume, uh, we ignore the, um, share components.
[00:12:50:450 - 00:12:52:650] **Speaker 1:** So we do have also the Tymoshenko.
[00:12:52:770 - 00:12:57:250] **Speaker 1:** So, um, essentially this is the, the stiffness matrix that
[00:12:57:250 - 00:12:59:849] **Speaker 1:** you've been using already and this is the Tymoshenko version.
[00:12:59:929 - 00:13:01:690] **Speaker 1:** So it looks very similar, but it's just these extra
[00:13:01:690 - 00:13:02:429] **Speaker 1:** factors in here.
[00:13:03:340 - 00:13:05:419] **Speaker 1:** Um, which exists through there.
[00:13:06:080 - 00:13:09:729] **Speaker 1:** And that that extra factor is 12 EI over the
[00:13:09:729 - 00:13:13:840] **Speaker 1:** shear modulus, which is 77 gigapasscal, the sheer area and
[00:13:13:840 - 00:13:14:679] **Speaker 1:** the length squared.
[00:13:15:929 - 00:13:20:049] **Speaker 1:** So, um, for a hollow circular section, the shear area
[00:13:20:049 - 00:13:23:599] **Speaker 1:** is generally defined as, uh, 2a over pi, where A
[00:13:23:599 - 00:13:26:330] **Speaker 1:** is the gross cross sectional area and pi, of course,
[00:13:26:359 - 00:13:27:349] **Speaker 1:** is just the constant.
[00:13:27:760 - 00:13:30:369] **Speaker 1:** Um, so what that means is that the, the effective
[00:13:30:369 - 00:13:33:190] **Speaker 1:** shear area for a circular hollow section is about 64%
[00:13:33:609 - 00:13:34:530] **Speaker 1:** of the gross section.
[00:13:34:650 - 00:13:36:330] **Speaker 1:** So there are actually two different values in there.
[00:13:37:359 - 00:13:39:640] **Speaker 1:** Um, what I'm asking you to do is modify your
[00:13:39:640 - 00:13:42:950] **Speaker 1:** code to incorporate the Timoshenko element.
[00:13:43:280 - 00:13:45:719] **Speaker 1:** So what this means is essentially you maybe have a
[00:13:45:719 - 00:13:49:000] **Speaker 1:** new global, uh, bar function, a global frame function.
[00:13:49:700 - 00:13:53:419] **Speaker 1:** And you just have these extra components within there.
[00:13:53:609 - 00:13:57:979] **Speaker 1:** So once you've generated this element stiffness matrix, the transformation
[00:13:57:979 - 00:14:00:299] **Speaker 1:** matrix stays exactly as it's as it is and everything
[00:14:00:299 - 00:14:01:140] **Speaker 1:** subsequent to that.
[00:14:01:340 - 00:14:04:200] **Speaker 1:** So it's just that first step you've got your KE
[00:14:04:429 - 00:14:07:289] **Speaker 1:** you have a slightly different matrix, and then it multiplies
[00:14:07:289 - 00:14:09:700] **Speaker 1:** into KE hat into KG for an element and the
[00:14:09:700 - 00:14:10:940] **Speaker 1:** overall KG exactly the same.
[00:14:11:020 - 00:14:12:979] **Speaker 1:** So it's only that one step that you need to
[00:14:12:979 - 00:14:13:599] **Speaker 1:** change.
[00:14:13:780 - 00:14:17:299] **Speaker 1:** And then now you're also incorporating some shared deformations into
[00:14:17:299 - 00:14:17:799] **Speaker 1:** that.
[00:14:18:340 - 00:14:21:559] **Speaker 1:** So, Uh, modify your code to have the Tymoshenko element,
[00:14:21:929 - 00:14:22:280] **Speaker 1:** um.
[00:14:22:989 - 00:14:25:219] **Speaker 1:** Using the maximum wind speed you found in your previous
[00:14:25:219 - 00:14:28:130] **Speaker 1:** things or whatever maximum wind speed you had to get
[00:14:28:130 - 00:14:32:270] **Speaker 1:** the 2.5 metres, um, the factor of safety of 2.5,
[00:14:32:299 - 00:14:35:690] **Speaker 1:** which means 140 megapascal maximum stress.
[00:14:36:679 - 00:14:40:159] **Speaker 1:** Um, and just go through and see how the deflections
[00:14:40:159 - 00:14:40:510] **Speaker 1:** change.
[00:14:40:640 - 00:14:43:789] **Speaker 1:** So, um, I've asked here, first we'll see how the,
[00:14:43:950 - 00:14:47:109] **Speaker 1:** the maximum wind speed rating changes, um, then check the
[00:14:47:109 - 00:14:47:940] **Speaker 1:** deflections.
[00:14:48:859 - 00:14:50:479] **Speaker 1:** Uh, which occur in each element.
[00:14:51:419 - 00:14:53:919] **Speaker 1:** And how the defections change, so.
[00:14:54:570 - 00:14:56:010] **Speaker 1:** What I'm asking you to do is present a table
[00:14:56:010 - 00:14:58:090] **Speaker 1:** which quotes the deflection component within each element, so the
[00:14:58:090 - 00:15:00:609] **Speaker 1:** transverse deflection, which is the difference between D5 and D2
[00:15:00:609 - 00:15:03:010] **Speaker 1:** for an element, that occurs within the element and the
[00:15:03:010 - 00:15:05:289] **Speaker 1:** change in rotation, which is the difference between D6 and
[00:15:05:289 - 00:15:08:890] **Speaker 1:** D3, that occurs, um, and provide a comparison of how
[00:15:08:890 - 00:15:11:739] **Speaker 1:** much um the result changes due to the different modelling
[00:15:11:739 - 00:15:15:469] **Speaker 1:** assumptions between the Euler-Bernoulli and the Timoshenko element formulations.
[00:15:17:179 - 00:15:21:679] **Speaker 1:** Now, you're adding an an additional um deflection component here.
[00:15:22:619 - 00:15:24:700] **Speaker 1:** So therefore you would expect larger deflections.
[00:15:25:349 - 00:15:28:469] **Speaker 1:** Um, there's an additional, um, component of deflection which is
[00:15:28:469 - 00:15:31:070] **Speaker 1:** otherwise being ignored in the Ouler Bernoulli.
[00:15:31:429 - 00:15:35:390] **Speaker 1:** Um, so broadly you would expect larger deflections, but because
[00:15:35:400 - 00:15:41:289] **Speaker 1:** we're also solving, um, axial deformations and transverse simultaneously but
[00:15:41:299 - 00:15:43:989] **Speaker 1:** independently, um, there are some parts of the structure where
[00:15:43:989 - 00:15:46:229] **Speaker 1:** you actually get sort of that more axial force couple
[00:15:46:229 - 00:15:48:789] **Speaker 1:** and that more truss action going on, um, if the
[00:15:48:789 - 00:15:49:750] **Speaker 1:** elements is a little bit more flexible.
[00:15:49:830 - 00:15:51:789] **Speaker 1:** So there may be certain points in the structure where
[00:15:51:789 - 00:15:53:929] **Speaker 1:** you actually perhaps see very slightly smaller.
[00:15:54:330 - 00:15:57:489] **Speaker 1:** Deflections, and it doesn't necessarily mean your code's wrong, um,
[00:15:57:570 - 00:15:59:119] **Speaker 1:** but certainly at the top you would expect to see
[00:15:59:119 - 00:16:02:330] **Speaker 1:** larger deflections, um, and I would just looking for you
[00:16:02:330 - 00:16:04:530] **Speaker 1:** to quantify that, um, and have a little bit of
[00:16:04:530 - 00:16:07:409] **Speaker 1:** an understanding as to what that simplification is doing and
[00:16:07:409 - 00:16:09:349] **Speaker 1:** whether it's something that concerns you or not.
[00:16:10:640 - 00:16:13:359] **Speaker 1:** Um, the, the next part is just the, the final
[00:16:13:359 - 00:16:16:559] **Speaker 1:** part of the sort of analysis is structural modifications.
[00:16:16:799 - 00:16:19:849] **Speaker 1:** So, Probably if you look at the structure, you think
[00:16:19:849 - 00:16:22:570] **Speaker 1:** it's maybe not the best structure, you know, if you
[00:16:22:570 - 00:16:24:559] **Speaker 1:** look at it and think, well, I might have designed
[00:16:24:559 - 00:16:25:510] **Speaker 1:** that structure differently.
[00:16:26:330 - 00:16:27:570] **Speaker 1:** Well, here's your chance to do so.
[00:16:29:229 - 00:16:31:630] **Speaker 1:** So modify the structure by adding or removing elements or
[00:16:31:630 - 00:16:32:750] **Speaker 1:** changing the existing elements.
[00:16:32:909 - 00:16:35:669] **Speaker 1:** So you could change the nodal points of existing elements
[00:16:35:669 - 00:16:37:010] **Speaker 1:** or you could add new elements in.
[00:16:37:989 - 00:16:39:270] **Speaker 1:** Uh, you could take elements away.
[00:16:39:539 - 00:16:41:909] **Speaker 1:** Um, you must keep the two support points in the
[00:16:41:909 - 00:16:42:929] **Speaker 1:** face of the billboard.
[00:16:43:650 - 00:16:44:650] **Speaker 1:** Uh, in the same location.
[00:16:44:809 - 00:16:49:789] **Speaker 1:** So essentially, Yeah, this entire face here has to stay
[00:16:49:789 - 00:16:53:229] **Speaker 1:** where it is, and these points have to stay where
[00:16:53:229 - 00:16:54:710] **Speaker 1:** they are, so they have to stay relative to each
[00:16:54:710 - 00:16:57:280] **Speaker 1:** other, but you can change what happens between them.
[00:16:59:510 - 00:17:04:170] **Speaker 1:** Um Present results which indicate how the peak wind load
[00:17:04:170 - 00:17:07:170] **Speaker 1:** changes as a result of your structural modifications and provide
[00:17:07:170 - 00:17:09:520] **Speaker 1:** an indication of how much total material use changes as
[00:17:09:520 - 00:17:11:229] **Speaker 1:** a result of your structural modifications.
[00:17:12:037 - 00:17:13:537] **Speaker 1:** Now for this, there is no right answer.
[00:17:13:718 - 00:17:16:359] **Speaker 1:** Um, it is quite open-ended and pretty, everyone will come
[00:17:16:359 - 00:17:17:499] **Speaker 1:** up with some sort of different idea.
[00:17:18:390 - 00:17:21:619] **Speaker 1:** Um But there is no right answer.
[00:17:21:660 - 00:17:24:300] **Speaker 1:** The final task intended to be more open-ended and creative.
[00:17:24:380 - 00:17:26:459] **Speaker 1:** So, um, to just try and see what you've come
[00:17:26:459 - 00:17:28:339] **Speaker 1:** up with and what that looks like.
[00:17:28:540 - 00:17:30:699] **Speaker 1:** So include a brief description of the rationale behind the
[00:17:30:699 - 00:17:31:380] **Speaker 1:** changes you've made.
[00:17:31:459 - 00:17:33:300] **Speaker 1:** So if you put an extra element in in a
[00:17:33:300 - 00:17:35:619] **Speaker 1:** certain location, if you can just provide, I did it
[00:17:35:619 - 00:17:38:339] **Speaker 1:** here because I thought there needed to be more stiffness
[00:17:38:339 - 00:17:39:609] **Speaker 1:** or more strength in this location.
[00:17:40:040 - 00:17:43:500] **Speaker 1:** You explain just briefly, um, why you made that change
[00:17:43:500 - 00:17:45:099] **Speaker 1:** and what your thinking was in doing that.
[00:17:46:569 - 00:17:47:650] **Speaker 1:** Now, the one thing that I just have a little
[00:17:47:650 - 00:17:49:729] **Speaker 1:** bit concerned of is having sort of an open-ended question
[00:17:49:729 - 00:17:52:530] **Speaker 1:** there is, um, sometimes these things can come a bit
[00:17:52:530 - 00:17:55:729] **Speaker 1:** of a race between everyone and suddenly people, everyone's trying
[00:17:55:729 - 00:17:57:689] **Speaker 1:** to outdo each other, which to some extent is good,
[00:17:57:729 - 00:18:01:810] **Speaker 1:** but not to the point that creates, um, an unmanageable
[00:18:01:810 - 00:18:02:489] **Speaker 1:** workload for you.
[00:18:02:609 - 00:18:05:689] **Speaker 1:** So, um, this piece of the assignment is going to
[00:18:05:689 - 00:18:07:959] **Speaker 1:** carry marks roughly about sort of 10% of the total
[00:18:07:959 - 00:18:08:410] **Speaker 1:** assignment.
[00:18:08:609 - 00:18:12:209] **Speaker 1:** So, um, it's not like you have to, um, you
[00:18:12:209 - 00:18:15:359] **Speaker 1:** know, You're gonna end up tripling your, your score by
[00:18:15:359 - 00:18:17:189] **Speaker 1:** really going to town on this piece of the assignment.
[00:18:17:280 - 00:18:19:280] **Speaker 1:** So something I'd like you to play around with, but
[00:18:19:280 - 00:18:20:959] **Speaker 1:** you know, not looking for you to spend dozens of
[00:18:20:959 - 00:18:23:939] **Speaker 1:** hours um on that that aspect.
[00:18:26:069 - 00:18:28:900] **Speaker 1:** Yeah Reporting, there's a whole lot of stuff here.
[00:18:28:949 - 00:18:33:040] **Speaker 1:** Just present a brief report of your analysis, your analysis
[00:18:33:670 - 00:18:37:180] **Speaker 1:** explaining what you've done, the results you've obtained, um, so
[00:18:37:180 - 00:18:38:310] **Speaker 1:** keep the report relatively brief.
[00:18:38:430 - 00:18:40:390] **Speaker 1:** So it's an eight page maximum plus appendices.
[00:18:40:589 - 00:18:43:530] **Speaker 1:** So all of the things like appendix like, um, 3
[00:18:43:530 - 00:18:46:469] **Speaker 1:** diagrams, uh, assembly matrices, etc.
[00:18:46:829 - 00:18:48:430] **Speaker 1:** can be in an appendix, not in the main body
[00:18:48:430 - 00:18:49:170] **Speaker 1:** of your report.
[00:18:50:380 - 00:18:52:619] **Speaker 1:** Um, discuss the results you've obtained and what you've learned,
[00:18:52:910 - 00:18:55:819] **Speaker 1:** quantify and discuss disparity between the different models and methods
[00:18:56:189 - 00:18:58:050] **Speaker 1:** and how they affect how you design the structure.
[00:18:59:410 - 00:19:01:780] **Speaker 1:** Um, one thing I just want to say is assume
[00:19:01:780 - 00:19:04:959] **Speaker 1:** you're writing the report for another mechanical or mechatronics engineer.
[00:19:05:260 - 00:19:08:459] **Speaker 1:** Assume the, the person has good technical knowledge, knowledge of
[00:19:08:459 - 00:19:09:640] **Speaker 1:** finite element analysis.
[00:19:10:000 - 00:19:12:969] **Speaker 1:** And has access to and a good understanding of all
[00:19:12:969 - 00:19:15:849] **Speaker 1:** of the lecture notes and examples, but does not know
[00:19:15:849 - 00:19:18:170] **Speaker 1:** the specific project and does not have the assignment brief.
[00:19:18:530 - 00:19:21:400] **Speaker 1:** So the things that are specific to this assignment, explained
[00:19:21:400 - 00:19:23:750] **Speaker 1:** in your report, but please don't go in and explain
[00:19:23:750 - 00:19:26:170] **Speaker 1:** what a stiffness matrix is or what a transformation matrix
[00:19:26:170 - 00:19:29:530] **Speaker 1:** is or how they transform, um, between coordinate systems.
[00:19:29:609 - 00:19:30:790] **Speaker 1:** That's all assumed knowledge.
[00:19:31:920 - 00:19:34:160] **Speaker 1:** I don't want you sort of recreating chunks of the
[00:19:34:160 - 00:19:38:199] **Speaker 1:** lecture notes um in your report because um that's not
[00:19:38:199 - 00:19:38:339] **Speaker 1:** necessary.
[00:19:40:300 - 00:19:42:959] **Speaker 1:** When presenting your results, please, please lead the reader through
[00:19:43:060 - 00:19:44:719] **Speaker 1:** and understand and interpret your results.
[00:19:45:339 - 00:19:47:369] **Speaker 1:** Um, for example, don't just present a table of numerical
[00:19:47:369 - 00:19:50:699] **Speaker 1:** results, um, explain to the reader and draw like lead
[00:19:50:699 - 00:19:54:010] **Speaker 1:** the reader reader through, um, explain not just here's a
[00:19:54:010 - 00:19:56:260] **Speaker 1:** table of results, but here's the things that I think
[00:19:56:260 - 00:19:57:199] **Speaker 1:** you should draw from that.
[00:19:58:060 - 00:20:00:770] **Speaker 1:** Um, the reports can be done individually or in pairs,
[00:20:00:939 - 00:20:03:060] **Speaker 1:** uh, and I do strongly encourage you to do this
[00:20:03:060 - 00:20:03:640] **Speaker 1:** as a peer.
[00:20:04:439 - 00:20:07:510] **Speaker 1:** Um So there's also a statement here.
[00:20:07:880 - 00:20:10:270] **Speaker 1:** If you do assignment didn't appear, please submit one report
[00:20:10:270 - 00:20:11:430] **Speaker 1:** with both your names on it.
[00:20:11:869 - 00:20:13:989] **Speaker 1:** Uh, if you do the report individually, everything in the
[00:20:13:989 - 00:20:15:089] **Speaker 1:** report must be your own work.
[00:20:16:199 - 00:20:18:400] **Speaker 1:** The statements there because a few, few years ago now,
[00:20:18:469 - 00:20:20:790] **Speaker 1:** but, um, in an assignment where people were allowed to
[00:20:20:790 - 00:20:23:750] **Speaker 1:** work together, we had two people work individually and sit,
[00:20:24:069 - 00:20:27:219] **Speaker 1:** submit nearly identical reports that weren't quite the same.
[00:20:27:439 - 00:20:30:939] **Speaker 1:** Um, and then there's a whole sort of academic dishonesty
[00:20:31:229 - 00:20:32:920] **Speaker 1:** query that makes no sense when you could have just
[00:20:32:920 - 00:20:33:420] **Speaker 1:** worked together.
[00:20:34:369 - 00:20:36:119] **Speaker 1:** So, yeah, if you do work individually, it has to
[00:20:36:119 - 00:20:38:969] **Speaker 1:** be your work, um, but it's strongly encourage you to
[00:20:38:969 - 00:20:40:329] **Speaker 1:** work together, uh, as a pair.
[00:20:41:339 - 00:20:45:449] **Speaker 1:** Um The report's due at 6:00 p.m. on Monday, the
[00:20:45:449 - 00:20:48:599] **Speaker 1:** 7th of September, um, via digital submission.
[00:20:49:770 - 00:20:51:569] **Speaker 1:** Um, so there'll be a portal online that you can
[00:20:51:569 - 00:20:52:250] **Speaker 1:** submit that to.
[00:20:52:489 - 00:20:54:530] **Speaker 1:** So there'll be a code portal to put your code
[00:20:54:530 - 00:20:56:849] **Speaker 1:** in, um, and also just a portal for you to
[00:20:56:849 - 00:20:59:170] **Speaker 1:** put your, uh, or maybe it's the same portal, but
[00:20:59:170 - 00:21:02:520] **Speaker 1:** you have a, a PDF of your assignment report and
[00:21:02:520 - 00:21:03:530] **Speaker 1:** your code in there.
[00:21:04:569 - 00:21:07:369] **Speaker 1:** Um, the code is supporting information only towards partial credit.
[00:21:07:449 - 00:21:09:890] **Speaker 1:** The passes are incorrect, and there'll be no marks directly
[00:21:09:890 - 00:21:10:750] **Speaker 1:** awarded to the code.
[00:21:10:890 - 00:21:14:890] **Speaker 1:** So you're not gonna be, um, marked upon the, the
[00:21:14:890 - 00:21:16:729] **Speaker 1:** structure of your code or the commenting or anything like
[00:21:16:729 - 00:21:17:180] **Speaker 1:** that.
[00:21:17:530 - 00:21:17:839] **Speaker 1:** Um.
[00:21:18:750 - 00:21:21:469] **Speaker 1:** With regard to generative AI, um, I'm fine for you
[00:21:21:469 - 00:21:25:270] **Speaker 1:** to use like a co-pilot functionality within an IDE to
[00:21:25:270 - 00:21:26:790] **Speaker 1:** assist with developing the code.
[00:21:27:189 - 00:21:30:250] **Speaker 1:** Um, and also if, if it was within the, if
[00:21:30:250 - 00:21:32:380] **Speaker 1:** you're using any sort of AI functionality to help draw
[00:21:33:430 - 00:21:35:430] **Speaker 1:** plots and things that go into your report, that's fine,
[00:21:35:469 - 00:21:39:189] **Speaker 1:** but the actual written content of your report, um, needs
[00:21:39:189 - 00:21:40:170] **Speaker 1:** to be your own work.
[00:21:41:040 - 00:21:44:239] **Speaker 1:** Um, if you do use AI tools to assist with
[00:21:44:239 - 00:21:46:880] **Speaker 1:** the coding, you need to take responsibility for the output
[00:21:46:880 - 00:21:47:780] **Speaker 1:** and check that it's correct.
[00:21:48:319 - 00:21:50:719] **Speaker 1:** So, you know, there's no certainly no excuse to say,
[00:21:50:800 - 00:21:52:839] **Speaker 1:** well, you know, AI got it wrong, therefore I shouldn't
[00:21:52:839 - 00:21:53:510] **Speaker 1:** lose marks.
[00:21:53:839 - 00:21:55:560] **Speaker 1:** You're taking responsibility for your output here.
[00:21:57:790 - 00:22:01:250] **Speaker 1:** Um Then just some stuff.
[00:22:01:290 - 00:22:03:069] **Speaker 1:** I won't go through this line by line or anything,
[00:22:03:130 - 00:22:05:609] **Speaker 1:** but just some overall reports.
[00:22:06:500 - 00:22:07:880] **Speaker 1:** Suggestions and comments.
[00:22:08:339 - 00:22:09:900] **Speaker 1:** Um, one thing I do notice is a reasonable number
[00:22:09:900 - 00:22:12:130] **Speaker 1:** of remarks will be allocated to discussion interpreting of your
[00:22:12:130 - 00:22:16:060] **Speaker 1:** results, uh, presenting the numerical answer alone is not sufficient.
[00:22:16:260 - 00:22:19:189] **Speaker 1:** Um, consider what key outcomes can be seen, what conclusions
[00:22:19:189 - 00:22:21:099] **Speaker 1:** can be drawn, and what recommendations you would make.
[00:22:21:739 - 00:22:25:640] **Speaker 1:** And then there's just a, um, Lot of suggestions about
[00:22:25:640 - 00:22:28:219] **Speaker 1:** the different sections and things to, to consider in there,
[00:22:28:439 - 00:22:28:719] **Speaker 1:** um.
[00:22:30:349 - 00:22:33:109] **Speaker 1:** So, there's, yeah, just some things to refer to when
[00:22:33:109 - 00:22:34:469] **Speaker 1:** you're going through the report writing.
[00:22:35:810 - 00:22:37:530] **Speaker 1:** So is there any questions on that assignment?
[00:22:42:680 - 00:22:45:290] **Speaker 1:** Um, it's available on the course learn page just under
[00:22:45:290 - 00:22:51:160] **Speaker 1:** the week onto 4 firearms analysis tab, and yeah, otherwise,
[00:22:51:260 - 00:22:53:439] **Speaker 1:** um, thanks for all your time, um, and I'll pass
[00:22:53:439 - 00:22:54:359] **Speaker 1:** it across to James.
[00:23:02:239 - 00:23:03:449] **Speaker 1:** I have just muted this, so.
[00:23:03:839 - 00:23:03:920] **Speaker 1:** Oh.
[00:23:04:479 - 00:23:06:430] **Speaker 1:** Otherwise it's, do you use it?
[00:23:06:640 - 00:23:06:719] **Speaker 1:** Yeah.
[00:23:07:489 - 00:23:07:829] **Speaker 1:** Let me just leave it.
[00:23:09:160 - 00:23:11:089] **Speaker 1:** And then just make sure you unmute it here OK.
[00:23:13:300 - 00:23:13:310] **Speaker 0:** Mr.
[00:23:32:140 - 00:23:32:150] **Speaker 0:** I.
[00:24:04:260 - 00:24:04:489] **Speaker 0:** Cool.
[00:24:06:989 - 00:24:08:099] **Speaker 0:** All right, good morning.
[00:24:11:660 - 00:24:21:439] **Speaker 0:** We'll continue I With our appendices.
[00:24:21:660 - 00:24:25:560] **Speaker 2:** Um, so last time, or yesterday, we looked at console.
[00:24:26:599 - 00:24:30:180] **Speaker 2:** Just overall, Uh, in that workflow, some of you might
[00:24:30:180 - 00:24:32:140] **Speaker 2:** have already had a chance to, to open Cosole on
[00:24:32:140 - 00:24:35:060] **Speaker 2:** your computer at home or in the labs and started
[00:24:35:060 - 00:24:37:239] **Speaker 2:** working on the, the quiz in the lab this week.
[00:24:37:859 - 00:24:39:439] **Speaker 2:** I just want to spend some time to go through
[00:24:39:439 - 00:24:43:219] **Speaker 2:** geometry modelling inside Console, uh, just so that you're familiar
[00:24:43:219 - 00:24:44:449] **Speaker 2:** with how, how it all works.
[00:24:44:619 - 00:24:45:739] **Speaker 2:** Uh, it's going to be quite similar to what you've
[00:24:45:739 - 00:24:48:939] **Speaker 2:** done in your CAD software like SolarWorks, so nothing too
[00:24:48:939 - 00:24:49:479] **Speaker 2:** scary.
[00:24:50:199 - 00:24:52:400] **Speaker 2:** And then Appendix C is looking at meshing.
[00:24:54:150 - 00:24:58:030] **Speaker 2:** So this is page 117 of your notes.
[00:25:01:800 - 00:25:03:079] **Speaker 2:** If you wanna follow along.
[00:25:06:859 - 00:25:08:800] **Speaker 2:** So a bit of an intro introduction.
[00:25:09:260 - 00:25:15:800] **Speaker 2:** So, These are sourced from the user guide and a
[00:25:15:800 - 00:25:18:800] **Speaker 2:** textbook, or a couple of textbooks if you wanna read
[00:25:18:800 - 00:25:19:219] **Speaker 2:** more.
[00:25:19:920 - 00:25:21:939] **Speaker 2:** So creating a model is the first step in the
[00:25:21:939 - 00:25:22:390] **Speaker 2:** simulation.
[00:25:22:439 - 00:25:23:800] **Speaker 2:** So if you think back to those steps, we had
[00:25:23:800 - 00:25:27:339] **Speaker 2:** that pre-processing stage and creating the geometry or computational domain
[00:25:27:339 - 00:25:28:660] **Speaker 2:** is that first stage.
[00:25:29:160 - 00:25:32:760] **Speaker 2:** And it's quite critical to reflect on what is the
[00:25:32:760 - 00:25:36:079] **Speaker 2:** important shapes or geometry that you want to capture in
[00:25:36:079 - 00:25:36:579] **Speaker 2:** your model.
[00:25:37:630 - 00:25:39:310] **Speaker 2:** If you want to describe the physical shape of the
[00:25:39:310 - 00:25:44:589] **Speaker 2:** object, um, the material properties, load constraints, so the boundary
[00:25:44:589 - 00:25:47:410] **Speaker 2:** conditions that, that uniquely identify the problem.
[00:25:48:479 - 00:25:52:160] **Speaker 2:** Uh, the geometric model is being used to create the
[00:25:52:160 - 00:25:52:640] **Speaker 2:** mesh.
[00:25:55:369 - 00:25:59:430] **Speaker 2:** And if we want to look at a A particular
[00:25:59:430 - 00:26:02:069] **Speaker 2:** parameter and vary that so we might want to look
[00:26:02:069 - 00:26:05:040] **Speaker 2:** at different angles of attack or different lengths of our
[00:26:05:040 - 00:26:05:650] **Speaker 2:** aerofoil.
[00:26:06:300 - 00:26:08:839] **Speaker 2:** uh we could do a parametric study or parameter le.
[00:26:11:819 - 00:26:14:339] **Speaker 2:** Importing CAD geometries into consoles, so we're not really doing
[00:26:14:339 - 00:26:15:760] **Speaker 2:** that in this course.
[00:26:16:239 - 00:26:19:900] **Speaker 2:** Um, it requires an extra module with consoles, so they
[00:26:19:900 - 00:26:22:420] **Speaker 2:** sell that for, for more money, uh, but we do
[00:26:22:420 - 00:26:25:420] **Speaker 2:** have that for the research licences if you require that
[00:26:25:420 - 00:26:28:300] **Speaker 2:** next year for your final year projects, but essentially you
[00:26:28:300 - 00:26:32:239] **Speaker 2:** can connect SolidWorks with console and interact back and forth.
[00:26:33:209 - 00:26:37:890] **Speaker 2:** Otherwise, you can import the STL files instead.
[00:26:39:760 - 00:26:42:089] **Speaker 2:** Uh, which is those standard triangular shapes.
[00:26:43:359 - 00:26:47:280] **Speaker 2:** The limitation with the STL files is that it's approximating
[00:26:47:280 - 00:26:49:599] **Speaker 2:** your geometry with these little triangles.
[00:26:49:770 - 00:26:54:040] **Speaker 2:** Uh, that's not going to perfectly match curved surfaces and
[00:26:54:040 - 00:26:54:650] **Speaker 2:** things like that.
[00:26:54:920 - 00:26:57:030] **Speaker 2:** It'll work fine for straight edges but not curved.
[00:26:57:400 - 00:27:00:160] **Speaker 2:** So you're already introducing some error in your geometry.
[00:27:00:890 - 00:27:02:609] **Speaker 2:** Uh, so that's one of the reasons why we're just
[00:27:02:609 - 00:27:05:489] **Speaker 2:** creating a geometry directly within console so that when you
[00:27:05:489 - 00:27:08:930] **Speaker 2:** go to mesh, it's not introducing additional error into the
[00:27:08:930 - 00:27:09:609] **Speaker 2:** geometry.
[00:27:11:839 - 00:27:14:319] **Speaker 2:** Some of the considerations that we want to think about
[00:27:14:319 - 00:27:18:459] **Speaker 2:** for modelling include which features of the geometry to include
[00:27:18:459 - 00:27:19:260] **Speaker 2:** in our model.
[00:27:20:520 - 00:27:22:060] **Speaker 2:** We've got an example here on the left.
[00:27:23:109 - 00:27:29:109] **Speaker 2:** We're it's some pipe and we have uh writing in
[00:27:29:109 - 00:27:31:910] **Speaker 2:** and out with some arrows on either end.
[00:27:32:819 - 00:27:36:199] **Speaker 2:** Do you think it's worthwhile to include that in our,
[00:27:36:380 - 00:27:39:219] **Speaker 2:** in our model if we're looking at the stresses on
[00:27:39:219 - 00:27:39:780] **Speaker 2:** the pipe?
[00:27:54:449 - 00:27:55:170] **Speaker 2:** Any idea?
[00:27:59:939 - 00:28:02:939] **Speaker 2:** No, no, probably not, um, so.
[00:28:04:060 - 00:28:06:500] **Speaker 2:** That's not going to have a significant contribution to the
[00:28:06:500 - 00:28:09:699] **Speaker 2:** structural integrity of the pipe, having these small etched in
[00:28:09:699 - 00:28:10:709] **Speaker 2:** and out text.
[00:28:11:219 - 00:28:11:619] **Speaker 2:** So.
[00:28:12:829 - 00:28:15:270] **Speaker 2:** We can start console so that it's ready when we
[00:28:15:270 - 00:28:16:670] **Speaker 2:** get to it, um.
[00:28:18:050 - 00:28:22:109] **Speaker 2:** So we can simplify the geometry by removing that prior
[00:28:22:109 - 00:28:22:729] **Speaker 2:** to meshing.
[00:28:24:119 - 00:28:26:859] **Speaker 2:** So CAD model that's useful for analysis might be different
[00:28:26:859 - 00:28:29:400] **Speaker 2:** to the fully detailed CAD model that you send to
[00:28:29:400 - 00:28:30:439] **Speaker 2:** the 3D printer.
[00:28:30:819 - 00:28:33:359] **Speaker 2:** That's what everyone seems to be doing now, um, or,
[00:28:33:380 - 00:28:35:239] **Speaker 2:** or generating in the workshop.
[00:28:37:459 - 00:28:41:959] **Speaker 2:** So the CAD model only needs enough information to Yeah,
[00:28:42:199 - 00:28:44:520] **Speaker 2:** evaluate the structural integrity if it was a solid mechanics
[00:28:44:520 - 00:28:44:900] **Speaker 2:** problem.
[00:28:45:560 - 00:28:48:119] **Speaker 2:** Uh, but it is also important not to oversimplify the
[00:28:48:119 - 00:28:48:540] **Speaker 2:** problem.
[00:28:48:920 - 00:28:52:609] **Speaker 2:** So, Yeah, don't go too far.
[00:28:53:449 - 00:28:56:680] **Speaker 2:** So an example here is a fillet and a structural
[00:28:56:680 - 00:28:57:250] **Speaker 2:** analysis.
[00:28:57:530 - 00:29:02:439] **Speaker 2:** So, If we have on the left a structural element
[00:29:02:439 - 00:29:05:869] **Speaker 2:** with fillets, both on the outside and the inside corners,
[00:29:06:280 - 00:29:07:599] **Speaker 2:** so the inside and outside.
[00:29:10:319 - 00:29:13:900] **Speaker 2:** Uh, the fillet on the outside corner could be removed.
[00:29:14:280 - 00:29:17:280] **Speaker 2:** We see that there's a low stress concentration in the
[00:29:17:280 - 00:29:18:119] **Speaker 2:** outer region.
[00:29:18:900 - 00:29:22:329] **Speaker 2:** So it's blue The red region is high stress.
[00:29:23:130 - 00:29:25:410] **Speaker 2:** So we could do away with this.
[00:29:26:619 - 00:29:28:910] **Speaker 2:** Fill it and simplify the geometry, maybe the mesh is
[00:29:28:910 - 00:29:30:209] **Speaker 2:** going to be easier to create.
[00:29:34:150 - 00:29:35:729] **Speaker 2:** So that's fine, so that's panel 2.
[00:29:37:959 - 00:29:42:530] **Speaker 2:** And if we went ahead and simplified further, the inner,
[00:29:43:099 - 00:29:45:530] **Speaker 2:** uh, fillet, so now it's a straight edge, what we've
[00:29:45:530 - 00:29:48:739] **Speaker 2:** created inadvertently is a stress concentration because it's a point.
[00:29:49:079 - 00:29:53:180] **Speaker 2:** Um, and it's going to Have a very large stress,
[00:29:53:670 - 00:29:55:109] **Speaker 2:** so we're going to get a different result from our
[00:29:56:339 - 00:29:59:030] **Speaker 2:** numerical model compared to what we expect in practise.
[00:29:59:939 - 00:30:03:260] **Speaker 2:** So this is just an example of oversimplifying the geometry.
[00:30:03:540 - 00:30:06:500] **Speaker 2:** It'll be easier to solve with our computer, but it
[00:30:06:500 - 00:30:08:739] **Speaker 2:** won't be representative of the real physics.
[00:30:12:709 - 00:30:16:000] **Speaker 2:** Uh, we can also use automatic mission tools, uh, to
[00:30:16:000 - 00:30:17:040] **Speaker 2:** give some meshes.
[00:30:19:209 - 00:30:23:250] **Speaker 2:** That accurately model our geometry rather than the physics.
[00:30:24:000 - 00:30:27:709] **Speaker 2:** So I talked last time or yesterday about the fluid
[00:30:27:709 - 00:30:31:640] **Speaker 2:** mechanics or fluid flow within that wind tunnel, and we
[00:30:31:640 - 00:30:34:239] **Speaker 2:** had to resolve those boundary layers at the wall.
[00:30:34:680 - 00:30:36:880] **Speaker 2:** So we wanted to use inflation layers or those smaller
[00:30:36:880 - 00:30:38:959] **Speaker 2:** elements next to the wall, so.
[00:30:40:199 - 00:30:43:479] **Speaker 2:** Yeah, depending on what physics you're solving and what geometry
[00:30:43:479 - 00:30:46:290] **Speaker 2:** you have, uh, mesh selection is a really key step.
[00:30:46:800 - 00:30:48:800] **Speaker 2:** So what you might find as we go through a
[00:30:48:800 - 00:30:51:800] **Speaker 2:** whole appendix on, on meshes, is that it's a very
[00:30:51:800 - 00:30:52:660] **Speaker 2:** advanced topic.
[00:30:53:040 - 00:30:54:800] **Speaker 2:** Uh, it's been around for a long time and there's
[00:30:54:800 - 00:30:55:839] **Speaker 2:** been a lot of research on it.
[00:30:56:630 - 00:30:59:209] **Speaker 2:** Um, when you go to set up your numerical model
[00:30:59:369 - 00:31:01:550] **Speaker 2:** or your projects next year, you might find that you
[00:31:01:550 - 00:31:03:469] **Speaker 2:** spend quite a lot of time meshing to make sure
[00:31:03:469 - 00:31:05:489] **Speaker 2:** that you've got a good starting position.
[00:31:06:069 - 00:31:09:069] **Speaker 2:** Otherwise, if you go straight ahead and mesh with really
[00:31:09:329 - 00:31:13:349] **Speaker 2:** crude, uh, discretization, you might find that you can't find
[00:31:13:349 - 00:31:14:430] **Speaker 2:** an accurate solution.
[00:31:15:290 - 00:31:18:729] **Speaker 2:** So meshing can be just as easy as clicking mesh
[00:31:18:729 - 00:31:22:449] **Speaker 2:** in console, uh, but you might find that that doesn't
[00:31:22:449 - 00:31:23:569] **Speaker 2:** produce something that's very helpful.
[00:31:25:989 - 00:31:28:939] **Speaker 2:** The advantage with console is that depending on which solver
[00:31:28:939 - 00:31:32:550] **Speaker 2:** you've selected, for example, the fluid flow, uh, laminar, etc.
[00:31:32:829 - 00:31:34:750] **Speaker 2:** it will mesh according to that physics.
[00:31:34:790 - 00:31:37:189] **Speaker 2:** So those inflation layers that will apply to those boundary
[00:31:37:189 - 00:31:38:890] **Speaker 2:** conditions with no slip balls.
[00:31:39:349 - 00:31:41:550] **Speaker 2:** Uh, so it has some smarts to it.
[00:31:45:449 - 00:31:47:750] **Speaker 2:** The next one I want to raise is about.
[00:31:49:109 - 00:31:52:989] **Speaker 2:** modelling a thin or small objects.
[00:31:53:390 - 00:31:55:989] **Speaker 2:** So if you've got a like a chip and you've
[00:31:55:989 - 00:31:58:670] **Speaker 2:** got these little paths, I don't know what you call
[00:31:58:670 - 00:32:02:040] **Speaker 2:** them in electrical, what do you call it circuits.
[00:32:02:189 - 00:32:03:790] **Speaker 2:** I don't know what do you call these red things
[00:32:03:790 - 00:32:04:689] **Speaker 2:** in electrical.
[00:32:06:089 - 00:32:07:369] **Speaker 2:** Traces traces.
[00:32:07:729 - 00:32:10:800] **Speaker 2:** Um, so these are very thin, they have some finite
[00:32:10:800 - 00:32:12:989] **Speaker 2:** width but very small thickness.
[00:32:13:290 - 00:32:15:089] **Speaker 2:** You could approximate them as two dimensional.
[00:32:15:810 - 00:32:19:689] **Speaker 2:** So the electric current would be assumed constant throughout the
[00:32:19:689 - 00:32:20:109] **Speaker 2:** thickness.
[00:32:22:010 - 00:32:24:800] **Speaker 2:** Likewise here we've got a coil around a cylinder.
[00:32:25:540 - 00:32:30:380] **Speaker 2:** Because the coil diameter is very small, we could approximate
[00:32:30:380 - 00:32:31:459] **Speaker 2:** it as a line.
[00:32:31:900 - 00:32:34:819] **Speaker 2:** So we've got uniform temperature or electric current through the
[00:32:34:819 - 00:32:35:189] **Speaker 2:** coil.
[00:32:35:579 - 00:32:38:719] **Speaker 2:** So now we've reduced it from from a three dimensional,
[00:32:39:400 - 00:32:44:369] **Speaker 2:** Dimension, 3 dimensional space, down to 1D and swirling around.
[00:32:46:489 - 00:32:49:780] **Speaker 2:** So he's, uh, Oh, you probably read ahead, yeah, I'm
[00:32:49:780 - 00:32:51:280] **Speaker 2:** not reading as I talk.
[00:32:52:619 - 00:32:55:260] **Speaker 2:** Um, so we can treat them as 2D surfaces and
[00:32:55:260 - 00:32:57:900] **Speaker 2:** volumes, and we can also model these coils as 1D.
[00:32:59:640 - 00:33:02:150] **Speaker 2:** And the state variables, just another word for those dependent
[00:33:02:150 - 00:33:02:800] **Speaker 2:** variables.
[00:33:07:489 - 00:33:12:189] **Speaker 2:** We're going to analyse a, Like simply supported beam in
[00:33:12:189 - 00:33:15:520] **Speaker 2:** layer 2, I think it's 2 or 3, so this
[00:33:15:520 - 00:33:19:000] **Speaker 2:** would be an example of simplifying that 3 dimensional beam
[00:33:19:000 - 00:33:21:839] **Speaker 2:** down to 2D and making a plane stress or plane
[00:33:21:839 - 00:33:23:000] **Speaker 2:** strain assumption.
[00:33:24:410 - 00:33:27:890] **Speaker 2:** So whenever we're reducing the number of dimensions, it's not
[00:33:27:890 - 00:33:29:839] **Speaker 2:** physically the same as real life.
[00:33:29:890 - 00:33:31:160] **Speaker 2:** So we've made some assumptions.
[00:33:31:650 - 00:33:33:770] **Speaker 2:** So it's good to reflect at the end of it
[00:33:33:969 - 00:33:35:449] **Speaker 2:** whether or not those assumptions were valid.
[00:33:47:750 - 00:33:52:989] **Speaker 2:** And Building blocks for console we looked at because we
[00:33:52:989 - 00:33:56:910] **Speaker 2:** had a two-dimensional domain for our rectangle, the pass equation
[00:33:56:910 - 00:34:01:270] **Speaker 2:** yesterday, we had square, rectangle, and some other shapes, but
[00:34:01:270 - 00:34:03:630] **Speaker 2:** if it was 3D we'd have some more shapes to
[00:34:03:630 - 00:34:06:589] **Speaker 2:** choose from, so it's spherical, cylindrical, and all these other
[00:34:06:589 - 00:34:07:030] **Speaker 2:** shapes.
[00:34:07:979 - 00:34:11:849] **Speaker 2:** So these are Easy to sort of build more complicated
[00:34:11:849 - 00:34:14:968] **Speaker 2:** geometries ah that you might want to, to model.
[00:34:17:620 - 00:34:21:388] **Speaker 2:** So if you Have a car or some more complicated
[00:34:21:388 - 00:34:25:648] **Speaker 2:** shape that you can't build from these primitive shapes, ah,
[00:34:25:709 - 00:34:30:429] **Speaker 2:** you could use, Uh, switch planes, so you've used sketches
[00:34:30:429 - 00:34:33:709] **Speaker 2:** before in your CAD classes, uh, and you can extrude
[00:34:33:709 - 00:34:35:870] **Speaker 2:** and rotate and, and so forth.
[00:34:40:570 - 00:34:44:199] **Speaker 2:** Once we've got all the primitives or those extruded bodies,
[00:34:44:510 - 00:34:48:689] **Speaker 2:** we can then add, subtract, um, and build them up
[00:34:48:689 - 00:34:50:610] **Speaker 2:** into a full, full geometry.
[00:34:52:530 - 00:34:55:340] **Speaker 2:** So these are building operations, uh, transformations, so we can
[00:34:55:340 - 00:34:56:878] **Speaker 2:** copy, rotate, etc.
[00:34:58:330 - 00:35:02:919] **Speaker 2:** And the final final sequence and console is to just
[00:35:02:919 - 00:35:03:989] **Speaker 2:** join all the points together.
[00:35:06:399 - 00:35:08:399] **Speaker 2:** And I just want to go through these examples.
[00:35:27:969 - 00:35:29:510] **Speaker 2:** So that might just take a moment.
[00:35:29:850 - 00:35:34:810] **Speaker 2:** So if we think of that first cube, how would
[00:35:34:810 - 00:35:37:989] **Speaker 2:** you go about building that in with a CAD model
[00:35:38:330 - 00:35:39:050] **Speaker 2:** in the console?
[00:35:39:169 - 00:35:40:649] **Speaker 2:** What steps are required?
[00:36:09:469 - 00:36:10:570] **Speaker 2:** Any idea?
[00:36:17:709 - 00:36:23:510] **Speaker 0:** of Cuban Yeah, so you could do one cylinder as
[00:36:23:510 - 00:36:25:709] **Speaker 2:** an extraction or um difference.
[00:36:26:570 - 00:36:32:149] **Speaker 2:** And then do another 2 cylinders, or you could um
[00:36:32:370 - 00:36:35:050] **Speaker 2:** do 1 and then rotate it twice.
[00:36:35:129 - 00:36:37:989] **Speaker 2:** So I think we'll do this, the latter.
[00:36:46:419 - 00:36:48:669] **Speaker 2:** I've filled in enough time that I can load the
[00:36:49:780 - 00:37:19:300] **Speaker 2:** I So as you say, start with that block, and
[00:37:19:300 - 00:37:20:919] **Speaker 2:** the next step is.
[00:37:27:550 - 00:37:29:050] **Speaker 2:** To build a cylinder.
[00:37:32:209 - 00:37:34:520] **Speaker 2:** And that cylinder has the same.
[00:37:36:239 - 00:37:38:600] **Speaker 2:** it has a defined radius and a height equal to
[00:37:38:600 - 00:37:38:919] **Speaker 2:** the q.
[00:37:40:290 - 00:37:42:590] **Speaker 2:** We can then apply two rotate commands.
[00:37:43:209 - 00:37:47:250] **Speaker 2:** So rotating about the Y axis and then rotating about
[00:37:47:250 - 00:37:49:389] **Speaker 2:** the Z-axis by 90 degrees.
[00:37:56:300 - 00:37:58:159] **Speaker 2:** So at the moment we've got 3 cylinders and the
[00:37:58:159 - 00:38:00:520] **Speaker 2:** cube all um overlapping one another.
[00:38:02:600 - 00:38:04:739] **Speaker 2:** And we apply a difference operator.
[00:38:06:360 - 00:38:08:350] **Speaker 2:** By taking out the cylinder from the, from the queue.
[00:38:10:489 - 00:38:13:000] **Speaker 2:** So the reason for doing these rotations is that maybe
[00:38:13:000 - 00:38:15:610] **Speaker 2:** we can parameterize or or adjust it, um.
[00:38:17:530 - 00:38:20:389] **Speaker 2:** In a more general sense, so the cylinder.
[00:38:21:350 - 00:38:23:340] **Speaker 2:** If we want to adjust the radius, we can adjust,
[00:38:23:540 - 00:38:24:370] **Speaker 2:** adjust it here.
[00:38:25:129 - 00:38:27:070] **Speaker 2:** And then it will copy through to all the other,
[00:38:27:169 - 00:38:27:689] **Speaker 2:** other points.
[00:38:27:810 - 00:38:30:050] **Speaker 2:** So sometimes it just makes your life easier if you
[00:38:30:050 - 00:38:30:270] **Speaker 2:** can.
[00:38:31:919 - 00:38:35:300] **Speaker 2:** Define geometries in one place and then it's carried through
[00:38:35:719 - 00:38:38:080] **Speaker 2:** throughout just like your Python coding.
[00:38:38:379 - 00:38:40:179] **Speaker 2:** So the second example here is sort of like a
[00:38:40:179 - 00:38:41:500] **Speaker 2:** chalice or a wine glass.
[00:38:42:020 - 00:38:45:780] **Speaker 2:** Any ideas what would be the best approach?
[00:38:49:219 - 00:38:49:229] **Speaker 0:** Yep.
[00:38:52:000 - 00:38:54:669] **Speaker 2:** So this one's quite complicated in terms of not being
[00:38:54:669 - 00:38:56:739] **Speaker 2:** one of those simple primitive geometries.
[00:38:57:100 - 00:38:58:419] **Speaker 2:** So what we could do is do a bit of
[00:38:58:419 - 00:39:02:020] **Speaker 2:** a slice and then rotate it around the axis.
[00:39:03:010 - 00:39:05:929] **Speaker 2:** So there's work plan, so creating a new work plan,
[00:39:06:050 - 00:39:06:989] **Speaker 2:** right click geometry.
[00:39:08:300 - 00:39:08:820] **Speaker 2:** Work fine?
[00:39:11:659 - 00:39:12:879] **Speaker 2:** And this one.
[00:39:14:959 - 00:39:18:909] **Speaker 2:** We've used a busier polygon and then applied a fillip.
[00:39:19:870 - 00:39:25:419] **Speaker 2:** And then we're evolving A brow and 360.
[00:39:26:739 - 00:39:27:879] **Speaker 2:** So the next one, the IB.
[00:39:46:629 - 00:39:50:310] **Speaker 2:** Uh, it's quite similar, so we start maybe if I.
[00:39:51:840 - 00:39:53:239] **Speaker 2:** Remove these guys.
[00:39:55:209 - 00:39:57:870] **Speaker 2:** We start with the eye for the I beam, and
[00:39:57:870 - 00:40:01:040] **Speaker 2:** you want to extrude it out the length of the
[00:40:01:040 - 00:40:01:370] **Speaker 2:** band.
[00:40:03:060 - 00:40:07:860] **Speaker 2:** So it's strude By some distance of 6.5 metres.
[00:40:09:300 - 00:40:11:030] **Speaker 2:** Now these have cutouts.
[00:40:12:129 - 00:40:15:729] **Speaker 2:** So we want to use a work plan to develop
[00:40:15:729 - 00:40:16:830] **Speaker 2:** that profile.
[00:40:20:419 - 00:40:23:330] **Speaker 2:** So we could use a rectangle with some fillets as
[00:40:23:330 - 00:40:24:040] **Speaker 2:** an example.
[00:40:24:770 - 00:40:32:129] **Speaker 2:** And we want to punch through the Ivan So Again,
[00:40:32:179 - 00:40:33:879] **Speaker 2:** this is going to be solid, so it's a positive
[00:40:34:820 - 00:40:35:080] **Speaker 2:** object.
[00:40:35:219 - 00:40:38:550] **Speaker 2:** And then We can form an array, so we've got
[00:40:38:550 - 00:40:40:929] **Speaker 2:** multiple of these extrusions.
[00:40:44:929 - 00:40:49:899] **Speaker 2:** This is just a neat way of parameterizing multiple objects.
[00:40:50:169 - 00:40:53:570] **Speaker 2:** So instead of repeating this process twice more, we can
[00:40:53:570 - 00:40:56:129] **Speaker 2:** use this array setting and zip the number of elements
[00:40:56:129 - 00:40:56:510] **Speaker 2:** across.
[00:40:56:929 - 00:41:00:969] **Speaker 2:** So these examples up here on the left represent these
[00:41:00:969 - 00:41:01:909] **Speaker 2:** transformations.
[00:41:03:280 - 00:41:05:060] **Speaker 2:** The last step is applying the difference.
[00:41:06:969 - 00:41:08:969] **Speaker 2:** And we're left with the, the I-beam.
[00:41:10:760 - 00:41:12:379] **Speaker 2:** And the last one is a French.
[00:41:23:830 - 00:41:27:810] **Speaker 2:** And we could imagine we could apply a work plan
[00:41:27:810 - 00:41:30:350] **Speaker 2:** and then revolve it around the axis and then punch
[00:41:30:350 - 00:41:31:689] **Speaker 2:** out those holes.
[00:41:32:770 - 00:41:35:050] **Speaker 2:** So that's what we've, we've got here.
[00:41:36:840 - 00:41:38:439] **Speaker 2:** So this is the cross section of the Fange.
[00:41:40:629 - 00:41:42:550] **Speaker 2:** Um, we'll zoom out.
[00:41:44:479 - 00:41:48:090] **Speaker 2:** We evolve Maybe I'll hurt like this.
[00:41:53:989 - 00:41:56:520] **Speaker 2:** We were evolved to make the flange and then we
[00:41:56:520 - 00:41:59:399] **Speaker 2:** need to evaluate these cylinders.
[00:42:02:629 - 00:42:06:340] **Speaker 2:** So one protrudes throughout the whole thickness and the other
[00:42:06:340 - 00:42:07:250] **Speaker 2:** only partially.
[00:42:08:360 - 00:42:09:580] **Speaker 2:** Maybe as a bolt hole.
[00:42:16:709 - 00:42:18:510] **Speaker 2:** So you can see here that it doesn't go all
[00:42:18:510 - 00:42:19:659] **Speaker 2:** the way through.
[00:42:20:550 - 00:42:21:219] **Speaker 2:** Just that.
[00:42:22:250 - 00:42:23:239] **Speaker 2:** Short distance.
[00:42:24:090 - 00:42:26:729] **Speaker 2:** We're applying a rotate transformation.
[00:42:28:600 - 00:42:31:629] **Speaker 2:** So rotating in the wire direction we'll set a range
[00:42:31:629 - 00:42:34:030] **Speaker 2:** of values from 0 up to 360 in steps of
[00:42:34:030 - 00:42:35:800] **Speaker 2:** 45, so you can use a step.
[00:42:36:610 - 00:42:37:469] **Speaker 2:** The function here.
[00:42:37:820 - 00:42:39:610] **Speaker 2:** And then last, apply that difference.
[00:42:44:320 - 00:42:46:469] **Speaker 2:** So that's probably quite similar to what you've already done
[00:42:46:469 - 00:42:49:949] **Speaker 2:** in CAD, just giving a demonstration of how to do
[00:42:49:949 - 00:42:50:729] **Speaker 2:** in console.
[00:42:51:590 - 00:42:53:909] **Speaker 2:** So you shouldn't need to use other software for creating
[00:42:53:909 - 00:42:54:889] **Speaker 2:** your geometries.
[00:42:57:939 - 00:43:04:639] **Speaker 2:** Are there any questions on starting console or, Making geometries.
[00:43:09:409 - 00:43:12:300] **Speaker 2:** Has anyone started opening console in the lab or at
[00:43:12:300 - 00:43:12:520] **Speaker 2:** home?
[00:43:12:620 - 00:43:13:169] **Speaker 2:** Not yet.
[00:43:13:459 - 00:43:13:939] **Speaker 2:** That's right.
[00:43:16:250 - 00:43:19:409] **Speaker 2:** You have the opportunity this afternoon, so it'll be fun.
[00:43:21:379 - 00:43:28:500] **Speaker 2:** Um, Oh, I, I've also got some email that.
[00:43:29:550 - 00:43:34:409] **Speaker 2:** I've got the Warman Challenge final tomorrow morning from 9:00
[00:43:34:409 - 00:43:36:479] **Speaker 2:** a.m. in the engineering corps.
[00:43:37:320 - 00:43:41:000] **Speaker 2:** And then the highest scoring round, highest scoring teams from
[00:43:41:000 - 00:43:44:439] **Speaker 2:** round one are competing in the final at about midday.
[00:43:44:719 - 00:43:47:199] **Speaker 2:** So if you want to go and see what people
[00:43:47:199 - 00:43:50:120] **Speaker 2:** are doing with women this round, I'm sure the Mc
[00:43:50:120 - 00:43:51:340] **Speaker 2:** students had fun when they did it.
[00:43:52:239 - 00:43:53:679] **Speaker 2:** The 2nd year, isn't it, that you do it?
[00:43:53:879 - 00:43:55:040] **Speaker 2:** You would have done it last year, yeah.
[00:43:55:479 - 00:43:58:290] **Speaker 2:** So you've probably seen them in the lab wings working
[00:43:58:290 - 00:44:00:080] **Speaker 2:** away in the last few days.
[00:44:01:320 - 00:44:03:860] **Speaker 2:** Um, so yeah, might be fun to watch.
[00:44:12:290 - 00:44:14:330] **Speaker 2:** Alright, Appendix C.
[00:44:17:770 - 00:44:21:570] **Speaker 2:** It's a little bit heavier, well, somewhat heavier, um, so
[00:44:21:570 - 00:44:23:649] **Speaker 2:** this one's looking at mesh generation, so I try to
[00:44:23:649 - 00:44:26:290] **Speaker 2:** preempt this saying that it's a really important stage of
[00:44:26:290 - 00:44:28:870] **Speaker 2:** the, the workflow because if you have a poor mesh
[00:44:28:870 - 00:44:31:209] **Speaker 2:** you're not going to get good results, full stop, uh,
[00:44:31:320 - 00:44:33:209] **Speaker 2:** and your solution might not converge at all.
[00:44:33:610 - 00:44:37:129] **Speaker 2:** So meshing is really critical, um, and as I say,
[00:44:37:169 - 00:44:40:129] **Speaker 2:** in commercial software it just does it for you and
[00:44:40:129 - 00:44:43:129] **Speaker 2:** hopefully it does it well, but you might need to
[00:44:43:129 - 00:44:44:409] **Speaker 2:** fine tune and adjust it.
[00:44:47:110 - 00:44:50:270] **Speaker 2:** So the purpose of a finite element mesh is to
[00:44:50:270 - 00:44:54:290] **Speaker 2:** subdivide all those geometries up into small discrete elements.
[00:44:54:909 - 00:44:57:760] **Speaker 2:** So we looked at finite difference, we haven't looked at
[00:44:57:760 - 00:45:01:030] **Speaker 2:** finite difference in detail yet, but we've got those grid,
[00:45:01:110 - 00:45:01:949] **Speaker 2:** grid of nodes.
[00:45:02:219 - 00:45:06:070] **Speaker 2:** Finite elements where we've got these unstructured elements and finite
[00:45:06:070 - 00:45:07:189] **Speaker 2:** volumes sort of similar.
[00:45:08:649 - 00:45:10:689] **Speaker 2:** So the mesh is used to represent the structure, and
[00:45:10:689 - 00:45:11:810] **Speaker 2:** we're going to compute the solution.
[00:45:13:100 - 00:45:15:280] **Speaker 2:** So some of the important parts of a mesh.
[00:45:16:090 - 00:45:19:129] **Speaker 2:** It's going to impact the rate of convergence.
[00:45:19:489 - 00:45:22:479] **Speaker 2:** So that's the solving of that big system of equations.
[00:45:22:770 - 00:45:25:570] **Speaker 2:** So those 10s, hundreds or millions of equations that we're
[00:45:25:570 - 00:45:28:310] **Speaker 2:** trying to solve, or might not converge at all.
[00:45:29:120 - 00:45:30:919] **Speaker 2:** It dictates the solution accuracy.
[00:45:31:929 - 00:45:34:229] **Speaker 2:** So if we have a finer mesh, we would expect
[00:45:34:229 - 00:45:37:350] **Speaker 2:** a more resolved solution and more accurate solution.
[00:45:37:899 - 00:45:39:290] **Speaker 2:** I suppose we can put that on both.
[00:45:42:919 - 00:45:43:620] **Speaker 2:** S S screens.
[00:45:44:459 - 00:45:46:889] **Speaker 2:** Um, and the CPU time, so if we have more
[00:45:46:889 - 00:45:49:010] **Speaker 2:** elements, we have more equations, more degrees of freedom, it's
[00:45:49:010 - 00:45:50:250] **Speaker 2:** gonna take longer to solve.
[00:45:53:899 - 00:45:55:879] **Speaker 2:** So the importance of the mesh quality.
[00:45:57:989 - 00:46:00:520] **Speaker 2:** Uh, is dictated by the grid density.
[00:46:00:949 - 00:46:03:429] **Speaker 2:** So we might want to resolve boundary layers.
[00:46:08:070 - 00:46:16:360] **Speaker 2:** And realise And CFD So We've got some pipe.
[00:46:16:939 - 00:46:19:879] **Speaker 2:** The bulk of the flow is reasonably fast.
[00:46:20:379 - 00:46:23:540] **Speaker 2:** On the interior, there's no slip wall boundary condition applied
[00:46:23:540 - 00:46:24:979] **Speaker 2:** at the surface of the pipe.
[00:46:25:500 - 00:46:28:179] **Speaker 2:** So the velocity field has to go from quite large
[00:46:28:179 - 00:46:31:820] **Speaker 2:** to small to zero over a very small span, especially
[00:46:31:820 - 00:46:32:919] **Speaker 2:** for high Reynolds flow.
[00:46:33:409 - 00:46:36:300] **Speaker 2:** So this is what these inflation layers are for, capturing
[00:46:36:300 - 00:46:37:340] **Speaker 2:** that velocity gradient.
[00:46:39:600 - 00:46:42:560] **Speaker 2:** The cell length to volume ratio, so.
[00:46:44:709 - 00:46:51:560] **Speaker 2:** The Spacing between adjacent elements, we don't want them to
[00:46:51:560 - 00:46:53:389] **Speaker 2:** be too large, that ratio.
[00:46:53:889 - 00:46:55:669] **Speaker 2:** We would like them to be quite smooth.
[00:46:58:909 - 00:47:04:149] **Speaker 2:** And that's because We want to have some continuity between
[00:47:04:340 - 00:47:07:739] **Speaker 2:** between each element, and that's related to the gradient of
[00:47:07:739 - 00:47:08:770] **Speaker 2:** the dependent variable.
[00:47:09:110 - 00:47:11:840] **Speaker 2:** So if we're thinking of velocity gradients or temperature gradients,
[00:47:13:070 - 00:47:15:560] **Speaker 2:** Uh, the skewness, so we want to avoid elements that
[00:47:15:560 - 00:47:16:379] **Speaker 2:** look like this.
[00:47:19:120 - 00:47:21:379] **Speaker 2:** The boundary layer mesh is what I described.
[00:47:24:100 - 00:47:25:689] **Speaker 2:** For that CFD example.
[00:47:30:199 - 00:47:33:659] **Speaker 2:** And we can also apply mesh refinement to adaptation.
[00:47:34:080 - 00:47:37:199] **Speaker 2:** So adaptive mesh refinement, I showed in that first lecture
[00:47:37:199 - 00:47:38:310] **Speaker 2:** with the tsunami modelling.
[00:47:38:639 - 00:47:43:479] **Speaker 2:** The basilisk, uh, open source software adaptively refined the mesh
[00:47:43:479 - 00:47:47:070] **Speaker 2:** subject to local variations in the thickness of the ocean.
[00:47:47:679 - 00:47:50:000] **Speaker 2:** So if you had waves that you were trying to
[00:47:50:000 - 00:47:52:280] **Speaker 2:** capture, it would refine the mesh locally there.
[00:47:52:840 - 00:47:54:679] **Speaker 2:** So that's, that's one way of doing it.
[00:47:54:919 - 00:47:57:800] **Speaker 2:** And console does have adaptive mesh refinement as well.
[00:47:59:370 - 00:48:07:469] **Speaker 2:** Available There's some terminology A cell is a finite volume
[00:48:07:469 - 00:48:09:939] **Speaker 2:** or control volume, uh, which we break the whole domain
[00:48:09:939 - 00:48:10:639] **Speaker 2:** up into.
[00:48:11:139 - 00:48:13:080] **Speaker 2:** A node is one single grid point.
[00:48:13:659 - 00:48:16:679] **Speaker 2:** The cell centre is the centre of a cell, typically
[00:48:16:679 - 00:48:19:179] **Speaker 2:** for the finite volume method, and edge is the edge
[00:48:19:179 - 00:48:21:199] **Speaker 2:** of one, face.
[00:48:21:659 - 00:48:23:580] **Speaker 2:** Phase is the boundary of a cell, zone is a
[00:48:23:580 - 00:48:26:939] **Speaker 2:** group, and domain is a group of nodes and cells.
[00:48:29:290 - 00:48:34:050] **Speaker 2:** Some of the element types include, um, well in 1
[00:48:34:050 - 00:48:35:370] **Speaker 2:** day it's just going to be a whole series of
[00:48:35:370 - 00:48:38:250] **Speaker 2:** lines, so we're a little bit limited on what type
[00:48:38:250 - 00:48:39:229] **Speaker 2:** of elements we have.
[00:48:40:060 - 00:48:42:610] **Speaker 2:** In 2D we can have triangles or quadrilaterals.
[00:48:43:709 - 00:48:48:159] **Speaker 2:** In this picture, we have the grey nodes, which is
[00:48:48:159 - 00:48:49:179] **Speaker 2:** slightly visible.
[00:48:49:850 - 00:48:51:330] **Speaker 2:** Is the nodes.
[00:48:52:179 - 00:48:54:159] **Speaker 2:** Uh, forming that triangle.
[00:48:55:179 - 00:49:00:379] **Speaker 2:** The white nodes are for the interpolation schemes, which we'll
[00:49:00:379 - 00:49:03:030] **Speaker 2:** come to later, but are also used.
[00:49:06:060 - 00:49:09:929] **Speaker 2:** In 3D we can have tetrahedral, hexahedrals, prisms, and pyramids,
[00:49:10:050 - 00:49:10:659] **Speaker 2:** etc.
[00:49:11:139 - 00:49:12:350] **Speaker 2:** so they can be more complicated.
[00:49:14:790 - 00:49:16:750] **Speaker 2:** And the mesh can be built from a combination of
[00:49:16:750 - 00:49:17:709] **Speaker 2:** these elements.
[00:49:17:909 - 00:49:21:020] **Speaker 2:** So if it's unstructured, you just have a chaotic mishmash
[00:49:21:020 - 00:49:21:939] **Speaker 2:** of elements.
[00:49:22:020 - 00:49:24:110] **Speaker 2:** If it was structured, it would just be those, those
[00:49:24:110 - 00:49:24:689] **Speaker 2:** quads.
[00:49:27:679 - 00:49:29:439] **Speaker 2:** These elements have midpoint nodes.
[00:49:30:909 - 00:49:36:270] **Speaker 2:** And the dependent variable is going to be, for example,
[00:49:36:389 - 00:49:40:870] **Speaker 2:** displacement temperature, velocity field is varying in X, Y, and
[00:49:40:870 - 00:49:41:270] **Speaker 2:** Z.
[00:49:41:550 - 00:49:43:989] **Speaker 2:** And if it has those midpoint nodes, it's using a
[00:49:43:989 - 00:49:45:409] **Speaker 2:** quadratic shape function.
[00:49:46:080 - 00:49:47:760] **Speaker 2:** And again, we'll come back to that later on, so
[00:49:47:760 - 00:49:49:780] **Speaker 2:** don't be too, too worried about that for now.
[00:49:51:969 - 00:49:54:340] **Speaker 2:** These are often the default elements used in console and
[00:49:54:340 - 00:49:56:139] **Speaker 2:** the other finite element codes.
[00:49:57:310 - 00:49:59:820] **Speaker 2:** So there's some mesh types, so structured mesh.
[00:50:01:689 - 00:50:04:090] **Speaker 2:** There are directions along which the node grid points is
[00:50:04:090 - 00:50:04:729] **Speaker 2:** always the same.
[00:50:04:840 - 00:50:06:459] **Speaker 2:** So essentially it's just rows and columns.
[00:50:06:530 - 00:50:09:790] **Speaker 2:** Think of an Excel spreadsheet with varying sizes.
[00:50:10:330 - 00:50:14:689] **Speaker 2:** Um, we can use IJK indexing to always identify the
[00:50:14:689 - 00:50:16:909] **Speaker 2:** neighbouring nodes north, south, east and west.
[00:50:18:719 - 00:50:21:080] **Speaker 2:** The advantage is that it's very easy to generate and
[00:50:21:080 - 00:50:23:679] **Speaker 2:** has low storage requirements because you don't have to keep
[00:50:23:679 - 00:50:27:120] **Speaker 2:** track of which elements are neighbouring which element because it's
[00:50:27:120 - 00:50:29:739] **Speaker 2:** by definition, the left, or right, top or bottom.
[00:50:30:860 - 00:50:32:699] **Speaker 2:** So it has a really well behaved algebraic system of
[00:50:32:699 - 00:50:33:439] **Speaker 2:** equations.
[00:50:34:179 - 00:50:36:659] **Speaker 2:** Uh, the disadvantage is that it's hard to map to
[00:50:36:659 - 00:50:37:899] **Speaker 2:** complicated geometries.
[00:50:38:260 - 00:50:40:820] **Speaker 2:** So the example here we've got a structured body fitted
[00:50:40:820 - 00:50:41:270] **Speaker 2:** mesh.
[00:50:42:850 - 00:50:46:810] **Speaker 2:** But beyond these examples it's quite hard to, to, to
[00:50:46:810 - 00:50:49:709] **Speaker 2:** map structured grids to complex geometries.
[00:50:50:449 - 00:50:52:469] **Speaker 2:** So we've run out of time already, which was sad
[00:50:52:469 - 00:50:59:050] **Speaker 2:** but, We'll continue the, the mesh, um, notes tomorrow and
[00:50:59:050 - 00:51:01:070] **Speaker 2:** I'll see you this afternoon in the labs.
[00:51:01:610 - 00:51:04:050] **Speaker 2:** And yeah, make sure that you ask questions if you're
[00:51:04:050 - 00:51:06:610] **Speaker 2:** stuck with the quiz or, or the consult lab.
[00:51:16:510 - 00:51:16:570] **Speaker 0:** God.
[00:51:40:639 - 00:51:42:350] **Speaker 0:** No, that's.
[00:51:53:639 - 00:51:53:649] **Speaker 0:** Yeah.
[00:51:56:179 - 00:51:56:229] **Speaker 0:** I go by 5.
[00:52:02:280 - 00:52:02:290] **Speaker 0:** Oh.
[00:52:09:290 - 00:52:16:600] **Speaker 0:** I Yeah.
[00:52:21:600 - 00:52:22:530] **Speaker 0:** I think this has to be.
[00:52:25:879 - 00:52:27:330] **Speaker 0:** I OK.
[00:52:31:570 - 00:52:31:580] **Speaker 0:** OK.
[00:52:36:959 - 00:52:38:429] **Speaker 0:** she's protein.
[00:52:39:770 - 00:52:43:790] **Speaker 0:** Uh OK.
[00:54:00:290 - 00:54:25:409] **Speaker 0:** I I mental I'm Oh good.
[00:54:28:280 - 00:54:29:610] **Speaker 0:** Yeah, based on the whole existence theory.
[00:54:34:070 - 00:54:38:750] **Speaker 0:** So You've been pretty good at doing stuff.
[00:54:39:860 - 00:54:59:250] **Speaker 0:** So Just before it's I Oh, I didn't I We

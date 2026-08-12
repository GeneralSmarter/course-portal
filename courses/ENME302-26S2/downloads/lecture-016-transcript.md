# ENME302-26S2 Lecture 16 native Echo transcript

Date: August 7, 2026 11:00am-11:55am
Transcript type: native Echo automated transcript.

[00:00:06:170 - 00:00:25:629] **Speaker 0:** I I That's.
[00:00:54:380 - 00:00:57:020] **Speaker 0:** Oh, so, welcome along, everyone.
[00:00:59:729 - 00:01:02:290] **Speaker 1:** Thanks for coming along on a, a very cool Friday
[00:01:02:290 - 00:01:02:709] **Speaker 1:** morning.
[00:01:07:050 - 00:01:08:489] **Speaker 1:** So there's a few things I want to work through
[00:01:08:489 - 00:01:08:650] **Speaker 1:** today.
[00:01:08:730 - 00:01:10:889] **Speaker 1:** We've got, uh, a few pages of the lecture notes
[00:01:10:889 - 00:01:11:309] **Speaker 1:** left.
[00:01:11:650 - 00:01:14:010] **Speaker 1:** Um, obviously this is the last, uh, lecture for this
[00:01:14:010 - 00:01:14:870] **Speaker 1:** part of the course.
[00:01:15:279 - 00:01:17:410] **Speaker 1:** Um, this won't be the end of you see of
[00:01:17:410 - 00:01:17:580] **Speaker 1:** me.
[00:01:17:599 - 00:01:19:290] **Speaker 1:** We've, we've sort of an assess and assignment to go.
[00:01:19:370 - 00:01:21:800] **Speaker 1:** So, um, I'll still be hanging around a little, a
[00:01:21:800 - 00:01:22:900] **Speaker 1:** little bit over the next few weeks.
[00:01:23:129 - 00:01:27:370] **Speaker 1:** Um, but what we went through yesterday was among the
[00:01:27:370 - 00:01:30:209] **Speaker 1:** things we went through was looking at how assembly matrices
[00:01:30:209 - 00:01:30:650] **Speaker 1:** work.
[00:01:31:220 - 00:01:35:459] **Speaker 1:** And essentially going through a, a very specific case of
[00:01:35:459 - 00:01:39:099] **Speaker 1:** a a cantilever and looking at the, the subsection of
[00:01:39:099 - 00:01:42:379] **Speaker 1:** the larger matrix which is being uh taken when we
[00:01:42:379 - 00:01:43:779] **Speaker 1:** have partial support here.
[00:01:45:400 - 00:01:48:680] **Speaker 1:** So, um, we worked through that yesterday and I did
[00:01:48:680 - 00:01:51:040] **Speaker 1:** have a question afterwards which actually made me think that
[00:01:51:040 - 00:01:52:379] **Speaker 1:** it's probably worth working through.
[00:01:52:839 - 00:01:54:680] **Speaker 1:** Uh, this is actually some additional working.
[00:01:54:879 - 00:01:56:440] **Speaker 1:** Um, this is only stuff that I've written in the
[00:01:56:440 - 00:01:57:080] **Speaker 1:** last day.
[00:01:57:519 - 00:02:00:199] **Speaker 1:** Um, so this is using the problem for that's in
[00:02:00:199 - 00:02:00:599] **Speaker 1:** the notes.
[00:02:00:760 - 00:02:02:800] **Speaker 1:** So this is, um, referring a lot of this is
[00:02:02:800 - 00:02:05:599] **Speaker 1:** actually a repeat of page 85 of the notes, but
[00:02:05:599 - 00:02:07:680] **Speaker 1:** just with some additional steps introduced, so.
[00:02:08:160 - 00:02:10:000] **Speaker 1:** In this situation we had two elements.
[00:02:10:240 - 00:02:11:339] **Speaker 1:** We're fully fixed at the top.
[00:02:11:919 - 00:02:14:520] **Speaker 1:** We had a roller here which moved horizontally, was constrained
[00:02:14:520 - 00:02:16:860] **Speaker 1:** from motion vertically, and could rotate.
[00:02:17:250 - 00:02:19:839] **Speaker 1:** Uh, and then we had a pin joint here which
[00:02:19:839 - 00:02:22:350] **Speaker 1:** allowed rotation but prevented translation.
[00:02:22:520 - 00:02:25:160] **Speaker 1:** So this is the, the problem that was the, the
[00:02:25:160 - 00:02:26:500] **Speaker 1:** key focus of the lab last week.
[00:02:27:740 - 00:02:30:270] **Speaker 1:** We had our two assembly matrices and then based upon
[00:02:30:270 - 00:02:34:429] **Speaker 1:** the connectivity information of how degrees of freedom here uh
[00:02:34:429 - 00:02:37:710] **Speaker 1:** map across to the overall global degrees of freedom, we
[00:02:37:710 - 00:02:40:330] **Speaker 1:** ended up with our assembly matrices.
[00:02:41:490 - 00:02:43:139] **Speaker 1:** Which are defined here and here.
[00:02:43:300 - 00:02:45:660] **Speaker 1:** So this was saying that D4 for element 1 corresponded
[00:02:45:660 - 00:02:49:059] **Speaker 1:** to Q1 and D6 for element one corresponded to Q2,
[00:02:49:419 - 00:02:51:179] **Speaker 1:** and that there was no linkage between any of the
[00:02:51:179 - 00:02:53:399] **Speaker 1:** degrees of freedom for this element and Q3.
[00:02:54:100 - 00:02:57:539] **Speaker 1:** And then we had D1 for element 2 is Q1,
[00:02:57:869 - 00:03:01:899] **Speaker 1:** D3 for element 2 is Q2, and D6 for element
[00:03:01:899 - 00:03:02:899] **Speaker 1:** two is Q3.
[00:03:04:279 - 00:03:07:199] **Speaker 1:** So in as in the notes um as they currently
[00:03:07:199 - 00:03:10:199] **Speaker 1:** exist, this is essentially we had this equation and we
[00:03:10:199 - 00:03:11:080] **Speaker 1:** had this result.
[00:03:11:399 - 00:03:13:839] **Speaker 1:** So all I want to do is just revisit the
[00:03:13:839 - 00:03:16:720] **Speaker 1:** step and break that out a little bit and try
[00:03:16:720 - 00:03:18:960] **Speaker 1:** and delve into exactly what's actually going on in here
[00:03:18:960 - 00:03:21:399] **Speaker 1:** and how it is that the assembly matrix does what
[00:03:21:399 - 00:03:22:020] **Speaker 1:** it does.
[00:03:23:139 - 00:03:25:369] **Speaker 1:** So the key point is, uh, this document is online,
[00:03:25:490 - 00:03:28:240] **Speaker 1:** it's, um, just added onto the week 1 to 4,
[00:03:28:529 - 00:03:30:910] **Speaker 1:** uh, it's immediately prior to the the prior tests.
[00:03:32:309 - 00:03:35:550] **Speaker 1:** So if we take this equation, this is what we
[00:03:35:550 - 00:03:35:899] **Speaker 1:** actually have.
[00:03:35:949 - 00:03:39:059] **Speaker 1:** We have our assembly matrix here, we have our K1
[00:03:39:059 - 00:03:42:330] **Speaker 1:** hat that's defined here and then we have our assembly
[00:03:42:330 - 00:03:43:669] **Speaker 1:** matrix one transposed.
[00:03:44:869 - 00:03:49:279] **Speaker 1:** So, if we work through this, Now remember when you
[00:03:49:279 - 00:03:53:149] **Speaker 1:** multiply two matrices together, so this here is a matrix
[00:03:53:149 - 00:03:55:199] **Speaker 1:** which is a 3 x 6.
[00:03:56:880 - 00:03:58:899] **Speaker 1:** And this one here is a 6 by 6.
[00:04:00:300 - 00:04:01:910] **Speaker 1:** And this here is a 6 by 1.
[00:04:03:429 - 00:04:05:589] **Speaker 1:** Now for a matrix to be conformable, for you to
[00:04:05:589 - 00:04:08:270] **Speaker 1:** be able to multiply them together, the inner dimensions must
[00:04:08:270 - 00:04:10:389] **Speaker 1:** match, which means this, the number of columns in this
[00:04:10:389 - 00:04:12:869] **Speaker 1:** matrix has to match the number of rows in this.
[00:04:13:639 - 00:04:16:678] **Speaker 1:** And then the number of columns in this matrix has
[00:04:16:678 - 00:04:19:160] **Speaker 1:** to match the number of rows in this matrix.
[00:04:20:407 - 00:04:22:569] **Speaker 1:** And when we multiply two matrices together, essentially what we
[00:04:22:569 - 00:04:24:528] **Speaker 1:** do is we work along a row and down a
[00:04:24:528 - 00:04:27:588] **Speaker 1:** column, so we say 0 times 12 + 0 times
[00:04:28:359 - 00:04:31:848] **Speaker 1:** 0 + 0 times 60 + 1 times -12 +
[00:04:31:848 - 00:04:36:569] **Speaker 1:** 0 times 60 0 + 0 times 60, and then
[00:04:36:569 - 00:04:38:148] **Speaker 1:** we walk to the second entry here.
[00:04:39:380 - 00:04:42:040] **Speaker 1:** We work along the same, so this is the, the,
[00:04:42:579 - 00:04:44:410] **Speaker 1:** um, first row and the second column.
[00:04:44:739 - 00:04:46:380] **Speaker 1:** We take the first row of this matrix and the
[00:04:46:380 - 00:04:48:600] **Speaker 1:** second column of this and we go across this row
[00:04:48:779 - 00:04:49:540] **Speaker 1:** and down this column.
[00:04:49:589 - 00:04:55:059] **Speaker 1:** So it's 0 times 00 times 20 times 01 times
[00:04:55:059 - 00:04:57:940] **Speaker 1:** 00 times -2, and 0 times 0.
[00:04:58:019 - 00:05:00:320] **Speaker 1:** So we're working across this down this and because this
[00:05:00:420 - 00:05:01:239] **Speaker 1:** one sits here.
[00:05:02:239 - 00:05:05:109] **Speaker 1:** Uh, it's in the 4th column.
[00:05:05:119 - 00:05:07:000] **Speaker 1:** That means essentially what we're doing is we're extracting the
[00:05:07:000 - 00:05:08:959] **Speaker 1:** 4th row of this matrix.
[00:05:09:160 - 00:05:12:019] **Speaker 1:** So if we take this, I'm just gonna highlight.
[00:05:12:940 - 00:05:17:029] **Speaker 1:** This row here That this one here means.
[00:05:17:859 - 00:05:23:100] **Speaker 1:** That the 4th row gets extracted and becomes the first
[00:05:23:100 - 00:05:24:859] **Speaker 1:** row of this.
[00:05:25:000 - 00:05:26:859] **Speaker 1:** That's because we have a 1 at the the 41
[00:05:26:859 - 00:05:28:859] **Speaker 1:** position, that's what that's doing.
[00:05:30:980 - 00:05:33:420] **Speaker 1:** Then what we have is a one here in the
[00:05:33:420 - 00:05:36:700] **Speaker 1:** 6th row of the 2nd, the 6th column of the
[00:05:36:700 - 00:05:37:510] **Speaker 1:** 2nd row.
[00:05:37:980 - 00:05:40:380] **Speaker 1:** So this one here, what it does is we go
[00:05:40:380 - 00:05:43:899] **Speaker 1:** across the row down a column and that then extracts
[00:05:43:899 - 00:05:45:260] **Speaker 1:** the 6th row here.
[00:05:46:000 - 00:05:48:320] **Speaker 1:** And places that in there.
[00:05:49:589 - 00:05:52:649] **Speaker 1:** So that's what's happening, uh, through that process.
[00:05:56:160 - 00:05:58:779] **Speaker 1:** Then the third one is all 0s, so we work
[00:05:58:779 - 00:06:02:079] **Speaker 1:** across rows down columns, but we're multiplying everything by 0
[00:06:02:079 - 00:06:05:160] **Speaker 1:** anyway, so we know with an all 0 row and
[00:06:05:160 - 00:06:06:679] **Speaker 1:** that is simply because if we look back at the
[00:06:06:679 - 00:06:07:179] **Speaker 1:** problem.
[00:06:08:929 - 00:06:10:549] **Speaker 1:** There is no direct connection.
[00:06:11:829 - 00:06:14:269] **Speaker 1:** Between element one and the third degree of freedom.
[00:06:14:649 - 00:06:18:730] **Speaker 1:** So element one doesn't contribute any doesn't directly contribute any
[00:06:18:730 - 00:06:20:209] **Speaker 1:** stiffness to this degree of freedom.
[00:06:21:489 - 00:06:25:339] **Speaker 1:** It does indirectly, uh, through element two, but not directly.
[00:06:27:000 - 00:06:29:190] **Speaker 1:** So then what we have and then we go uh
[00:06:29:190 - 00:06:31:089] **Speaker 1:** multiply by the semi matrix transposed.
[00:06:31:510 - 00:06:33:149] **Speaker 1:** So we're going across the row down a column.
[00:06:33:429 - 00:06:37:309] **Speaker 1:** So the first row here, what we're essentially doing is
[00:06:37:309 - 00:06:40:549] **Speaker 1:** extracting the fourth row, the 4th column of this matrix
[00:06:40:549 - 00:06:41:250] **Speaker 1:** and putting it here.
[00:06:41:390 - 00:06:48:760] **Speaker 1:** So what we're doing is we're taking, This So overlapping
[00:06:48:760 - 00:06:51:600] **Speaker 1:** here, but we're essentially taking this column and placing that
[00:06:51:600 - 00:06:51:940] **Speaker 1:** there.
[00:06:55:040 - 00:07:00:200] **Speaker 1:** And then We Taking the 6th row.
[00:07:01:299 - 00:07:10:290] **Speaker 1:** Which is this one And placing that Yeah And then
[00:07:10:290 - 00:07:14:410] **Speaker 1:** we're taking all zeros and um that's why we our
[00:07:14:410 - 00:07:16:450] **Speaker 1:** final column is zeros.
[00:07:18:010 - 00:07:21:489] **Speaker 1:** So this element one doesn't have any stiffness terms that
[00:07:21:489 - 00:07:23:359] **Speaker 1:** relates to the 3rd row or column, which means it
[00:07:23:359 - 00:07:26:690] **Speaker 1:** doesn't contribute any stiffness to element to degree freedom 3.
[00:07:28:459 - 00:07:30:130] **Speaker 1:** And then the same thing happens with element too.
[00:07:30:660 - 00:07:33:619] **Speaker 1:** So we can work through this, um.
[00:07:34:750 - 00:07:38:649] **Speaker 1:** The first, the, uh one being here and location 11.
[00:07:39:070 - 00:07:41:369] **Speaker 1:** So essentially what we're doing is we're taking the first
[00:07:41:510 - 00:07:45:410] **Speaker 1:** row, And we're assigning that into the first row down
[00:07:45:410 - 00:07:45:649] **Speaker 1:** here.
[00:07:47:730 - 00:07:50:510] **Speaker 1:** Then what we're doing is we have the 3rd row.
[00:07:51:450 - 00:07:53:470] **Speaker 1:** So the 2nd row, the 3rd column is a 1.
[00:07:55:040 - 00:07:59:760] **Speaker 1:** So that means we're taking the 3rd row and assigning
[00:07:59:760 - 00:08:02:640] **Speaker 1:** that to the 2nd row down here.
[00:08:04:750 - 00:08:06:670] **Speaker 1:** And then what we have.
[00:08:07:559 - 00:08:09:950] **Speaker 1:** there's the one on the 6th entry, so that one
[00:08:09:950 - 00:08:13:230] **Speaker 1:** there is essentially taking the 6th row.
[00:08:14:260 - 00:08:16:299] **Speaker 1:** And assigning that there.
[00:08:22:820 - 00:08:24:899] **Speaker 1:** Then what we're doing, we go this way, we're essentially
[00:08:24:899 - 00:08:25:880] **Speaker 1:** taking the first.
[00:08:26:869 - 00:08:28:059] **Speaker 1:** Row here.
[00:08:29:070 - 00:08:29:790] **Speaker 1:** This one here.
[00:08:31:170 - 00:08:33:590] **Speaker 1:** Is defining that that comes across and goes here.
[00:08:35:580 - 00:08:41:609] **Speaker 1:** Then This one in the 2nd column in the 3rd
[00:08:41:609 - 00:08:47:090] **Speaker 1:** row means that we're taking the 3rd column here and
[00:08:47:090 - 00:08:47:859] **Speaker 1:** assigning that.
[00:08:48:820 - 00:08:50:039] **Speaker 1:** Into the matrix below there.
[00:08:51:859 - 00:08:56:450] **Speaker 1:** And then last but certainly not least, This one value
[00:08:56:450 - 00:08:56:909] **Speaker 1:** here.
[00:08:58:809 - 00:09:00:380] **Speaker 1:** Is taking the 6th column.
[00:09:01:729 - 00:09:03:450] **Speaker 1:** Here and then assigning that.
[00:09:04:159 - 00:09:05:440] **Speaker 1:** Into that location there.
[00:09:07:969 - 00:09:12:130] **Speaker 1:** So It's quite, yeah, it's actually quite a nice mathematical
[00:09:12:130 - 00:09:14:489] **Speaker 1:** trick, but all it's doing is taking all the relevant
[00:09:14:489 - 00:09:17:049] **Speaker 1:** stiffness terms that actually corresponds to the element.
[00:09:17:530 - 00:09:20:210] **Speaker 1:** Uh, it's ignoring the bits that don't contribute to the
[00:09:20:210 - 00:09:22:950] **Speaker 1:** structure or they contribute to constrained degrees of freedom.
[00:09:24:510 - 00:09:28:020] **Speaker 1:** And then, um, extracting those and placing them into the
[00:09:28:309 - 00:09:29:150] **Speaker 1:** appropriate locations.
[00:09:29:200 - 00:09:31:229] **Speaker 1:** And then if we just add that together and with
[00:09:31:229 - 00:09:34:190] **Speaker 1:** that we get the overall KG matrix.
[00:09:34:669 - 00:09:37:469] **Speaker 1:** So, uh, this one is a little bit more of
[00:09:37:469 - 00:09:38:609] **Speaker 1:** a general example.
[00:09:39:030 - 00:09:40:469] **Speaker 1:** It actually corresponds to a structure.
[00:09:40:700 - 00:09:42:549] **Speaker 1:** Um, the last one we did yesterday was just a
[00:09:42:549 - 00:09:47:520] **Speaker 1:** little bit, um, probably, um, sort of Simple example.
[00:09:49:229 - 00:09:51:700] **Speaker 1:** So is there any questions on this aspect?
[00:09:55:140 - 00:09:56:429] **Speaker 1:** So just try that takes away a little bit of
[00:09:56:429 - 00:10:00:650] **Speaker 1:** the um You know, the mystery around what this equation
[00:10:00:650 - 00:10:02:619] **Speaker 1:** actually does and shows, you know, you're not gonna have
[00:10:02:619 - 00:10:05:539] **Speaker 1:** to actually do this manually in a test or anything,
[00:10:05:619 - 00:10:08:380] **Speaker 1:** but just show you, you know, here's what's actually going
[00:10:08:380 - 00:10:11:330] **Speaker 1:** on, it's, there's no magic, it's just um just linear
[00:10:11:330 - 00:10:11:820] **Speaker 1:** algebra.
[00:10:15:359 - 00:10:17:099] **Speaker 1:** So, the next thing we need to do.
[00:10:18:530 - 00:10:26:489] **Speaker 1:** Is We had talked about the concept of Um, go
[00:10:26:489 - 00:10:27:549] **Speaker 1:** loads and everything.
[00:10:28:520 - 00:10:30:609] **Speaker 1:** Um, we covered that yesterday, and the final thing that
[00:10:30:609 - 00:10:31:469] **Speaker 1:** was outstanding.
[00:10:32:390 - 00:10:37:059] **Speaker 1:** was this notion of if we were to have a
[00:10:37:059 - 00:10:38:330] **Speaker 1:** pin-jointed frame element.
[00:10:41:419 - 00:10:45:219] **Speaker 1:** So in this situation, we have an element here, so
[00:10:45:219 - 00:10:48:099] **Speaker 1:** it's continuous element is a T-shaped cross-section.
[00:10:49:719 - 00:10:52:119] **Speaker 1:** Element ABC, it's one continuous theme.
[00:10:53:150 - 00:10:55:359] **Speaker 1:** It's got a pin joint here and a pin joint
[00:10:55:359 - 00:10:58:719] **Speaker 1:** here at the supports and it's pinned the element ABC
[00:10:58:719 - 00:11:03:140] **Speaker 1:** is continuous across here, but the inclined element BD is
[00:11:03:400 - 00:11:05:200] **Speaker 1:** um pinned to that other element.
[00:11:05:280 - 00:11:08:719] **Speaker 1:** So this doesn't match our default assumptions for a frame.
[00:11:10:280 - 00:11:12:000] **Speaker 1:** The first thing we're gonna do, we've got some values
[00:11:12:000 - 00:11:14:039] **Speaker 1:** and things we've been asked to work out reaction loads
[00:11:14:039 - 00:11:14:979] **Speaker 1:** and things.
[00:11:15:429 - 00:11:17:280] **Speaker 1:** Um, the first thing we'll do is just if we
[00:11:17:280 - 00:11:18:280] **Speaker 1:** were to solve this by hand.
[00:11:18:400 - 00:11:21:000] **Speaker 1:** Well, we could take a free diagram of just this
[00:11:21:000 - 00:11:21:320] **Speaker 1:** element.
[00:11:21:400 - 00:11:23:450] **Speaker 1:** We've got some sort of reaction forces here.
[00:11:23:880 - 00:11:26:020] **Speaker 1:** Um, we can take moments about here.
[00:11:26:669 - 00:11:30:390] **Speaker 1:** Um, we tell quite simply that the, the reaction CY
[00:11:30:989 - 00:11:32:369] **Speaker 1:** should be 100 kilonewtons.
[00:11:34:000 - 00:11:35:859] **Speaker 1:** And we can then proceed through.
[00:11:37:320 - 00:11:38:830] **Speaker 1:** If we do some simple geometry.
[00:11:40:900 - 00:11:44:390] **Speaker 1:** Um, we can work out what the force in DC
[00:11:44:390 - 00:11:46:390] **Speaker 1:** should be, and it turns out there should be a
[00:11:46:390 - 00:11:50:330] **Speaker 1:** compressive force of 333.3 kilonewtons.
[00:11:52:270 - 00:11:54:539] **Speaker 1:** The element is pinned at each end, there's no loads
[00:11:54:539 - 00:11:56:619] **Speaker 1:** applied along the length of the element, so it should
[00:11:56:619 - 00:11:59:380] **Speaker 1:** be a purely axial load of this value.
[00:12:00:880 - 00:12:02:479] **Speaker 1:** Now what we're going to do now is work through
[00:12:02:479 - 00:12:02:989] **Speaker 1:** this.
[00:12:03:909 - 00:12:05:599] **Speaker 1:** Based on our frame element formulation.
[00:12:06:690 - 00:12:09:289] **Speaker 1:** And we're going to initially apply the exact same principles
[00:12:09:289 - 00:12:12:390] **Speaker 1:** we always have, knowing that that's actually gonna be wrong,
[00:12:12:650 - 00:12:15:409] **Speaker 1:** uh, because that's not how frame elements work and that
[00:12:15:409 - 00:12:17:799] **Speaker 1:** the default assumption is that things are rigidly welded to
[00:12:17:799 - 00:12:18:309] **Speaker 1:** each other.
[00:12:19:229 - 00:12:21:719] **Speaker 1:** So this is the approach as we would have enacted
[00:12:21:719 - 00:12:23:530] **Speaker 1:** it to this point.
[00:12:25:280 - 00:12:28:469] **Speaker 1:** So in this situation, we define 3 degrees of freedom
[00:12:28:469 - 00:12:30:979] **Speaker 1:** here, 3 degrees of freedom here, and then one of
[00:12:30:979 - 00:12:33:390] **Speaker 1:** each of these, which is the, the rotations are fully
[00:12:33:390 - 00:12:35:590] **Speaker 1:** constrained, but there is the potential of rotation.
[00:12:36:000 - 00:12:37:669] **Speaker 1:** So we'd have 8 degrees of freedom in total.
[00:12:40:159 - 00:12:43:010] **Speaker 1:** We look at this here to this, what we have
[00:12:43:010 - 00:12:46:489] **Speaker 1:** is that D1 for element 1 is Q1.
[00:12:47:250 - 00:12:49:710] **Speaker 1:** D2 for element 1, SQ 2.
[00:12:50:840 - 00:12:52:630] **Speaker 1:** E3 for element 1 is Q3.
[00:12:53:640 - 00:12:57:059] **Speaker 1:** And then we have uh D4, element 1.
[00:12:58:039 - 00:12:58:969] **Speaker 1:** SQ 4.
[00:13:00:090 - 00:13:03:890] **Speaker 1:** D5 for element one is Q5 and D6 for element
[00:13:03:890 - 00:13:05:650] **Speaker 1:** one is Q6.
[00:13:07:789 - 00:13:11:830] **Speaker 1:** There's no direct connection between um degrees of freedom 7
[00:13:11:830 - 00:13:14:309] **Speaker 1:** and 8 because element 1 is here and it doesn't
[00:13:14:309 - 00:13:15:799] **Speaker 1:** connect to those points.
[00:13:17:659 - 00:13:20:700] **Speaker 1:** At the interface here, what we're gonna do initially is
[00:13:20:700 - 00:13:23:020] **Speaker 1:** we're gonna just, um, the same way we always have
[00:13:23:020 - 00:13:25:820] **Speaker 1:** is we're gonna link the elements to the same translations
[00:13:25:820 - 00:13:27:159] **Speaker 1:** and the same rotations.
[00:13:29:190 - 00:13:31:909] **Speaker 1:** So what we'll say here is that D6 for element
[00:13:31:909 - 00:13:32:229] **Speaker 1:** 1.
[00:13:32:900 - 00:13:35:679] **Speaker 1:** Is equal to D3 for element 2.
[00:13:36:909 - 00:13:42:190] **Speaker 1:** Which is also equal to D3 for element 3, and
[00:13:42:190 - 00:13:43:729] **Speaker 1:** that's gonna be equal to Q6.
[00:13:45:150 - 00:13:48:429] **Speaker 1:** The translations, so D4 for element 1.
[00:13:49:179 - 00:13:52:580] **Speaker 1:** It'll be D1 for element 2 and D1 for element
[00:13:52:580 - 00:13:55:479] **Speaker 1:** 3, it'll be Q4.
[00:13:56:960 - 00:13:58:500] **Speaker 1:** D5, element 1.
[00:13:59:869 - 00:14:01:979] **Speaker 1:** D24 element 2.
[00:14:02:770 - 00:14:07:539] **Speaker 1:** And D25 on 3, and that's going to be Q5.
[00:14:09:409 - 00:14:10:770] **Speaker 1:** And then this is a little bit simple, we just
[00:14:10:770 - 00:14:11:710] **Speaker 1:** got D6.
[00:14:12:469 - 00:14:14:869] **Speaker 1:** Element 2 is Q7.
[00:14:16:210 - 00:14:19:609] **Speaker 1:** And the 6 fell on 3.
[00:14:20:419 - 00:14:21:229] **Speaker 1:** Is Q8.
[00:14:26:320 - 00:14:28:179] **Speaker 1:** So that's all the information that we need there.
[00:14:29:919 - 00:14:36:619] **Speaker 1:** about So that's where our assembly matrices come from.
[00:14:36:890 - 00:14:42:010] **Speaker 1:** And particularly, I'm just gonna highlight things with relation to
[00:14:42:010 - 00:14:43:979] **Speaker 1:** the rotation of the central node.
[00:14:44:090 - 00:14:48:090] **Speaker 1:** So, what we have here is the D3 um for
[00:14:48:090 - 00:14:49:950] **Speaker 1:** element one corresponds to Q3.
[00:14:50:530 - 00:14:56:090] **Speaker 1:** Sorry, that's D6 for element one corresponds to Q6.
[00:14:56:210 - 00:14:59:250] **Speaker 1:** So it's sort of the intersection here between this and
[00:14:59:250 - 00:14:59:849] **Speaker 1:** this.
[00:15:01:229 - 00:15:04:900] **Speaker 1:** And that's the one that exists at the intersection there.
[00:15:05:270 - 00:15:08:030] **Speaker 1:** We're also saying D3 for element 2.
[00:15:09:369 - 00:15:10:919] **Speaker 1:** Corresponds to Q6.
[00:15:13:400 - 00:15:14:359] **Speaker 1:** Which is that one.
[00:15:15:419 - 00:15:16:820] **Speaker 1:** And D3.
[00:15:18:260 - 00:15:19:130] **Speaker 1:** For element 3.
[00:15:20:559 - 00:15:21:979] **Speaker 1:** And Q6, so.
[00:15:23:520 - 00:15:27:659] **Speaker 1:** Those 3 ones, they are telling us that we're assigning
[00:15:27:840 - 00:15:31:869] **Speaker 1:** globally, 1 mathematical value that has to represent the rotation
[00:15:31:869 - 00:15:33:919] **Speaker 1:** of all three of those elements as they frame into
[00:15:33:919 - 00:15:34:200] **Speaker 1:** there.
[00:15:36:309 - 00:15:38:289] **Speaker 1:** Now we know that this isn't quite how the structure
[00:15:38:549 - 00:15:39:559] **Speaker 1:** is actually set up.
[00:15:40:599 - 00:15:43:169] **Speaker 1:** So we would expect this to maybe not quite work,
[00:15:43:390 - 00:15:46:500] **Speaker 1:** um, and we're not really quite modelling the structure.
[00:15:46:590 - 00:15:49:270] **Speaker 1:** So if we go through this, um, I'm not gonna
[00:15:49:270 - 00:15:52:090] **Speaker 1:** dwell too much on all the intermediate steps.
[00:15:53:369 - 00:15:57:559] **Speaker 1:** But Yeah, we follow the same process we always have
[00:15:57:559 - 00:16:02:200] **Speaker 1:** from this point, um, it's all relatively procedural, once you
[00:16:02:200 - 00:16:02:760] **Speaker 1:** know what you're doing.
[00:16:04:130 - 00:16:05:510] **Speaker 1:** All the intermediate steps.
[00:16:07:010 - 00:16:08:789] **Speaker 1:** And what we come out with here.
[00:16:09:859 - 00:16:13:330] **Speaker 1:** As we've got uh forcing terms in uppercase, so these
[00:16:13:330 - 00:16:15:510] **Speaker 1:** are in global coordinates and then local coordinates.
[00:16:15:890 - 00:16:18:150] **Speaker 1:** And if we take F3 and we put it here.
[00:16:19:489 - 00:16:21:710] **Speaker 1:** Then what we end up with is.
[00:16:23:090 - 00:16:33:640] **Speaker 1:** A Non-zero share And A non-zero.
[00:16:35:450 - 00:16:36:030] **Speaker 1:** Moment.
[00:16:39:010 - 00:16:41:070] **Speaker 1:** We do end up with a 0 moment down here.
[00:16:44:960 - 00:16:48:119] **Speaker 1:** And that's due to the pin that was located there.
[00:16:48:239 - 00:16:52:270] **Speaker 1:** So that was captured in our, um our setup, but
[00:16:52:520 - 00:16:55:799] **Speaker 1:** ultimately here, this doesn't match the problem setup, you know,
[00:16:55:880 - 00:16:59:320] **Speaker 1:** ultimately we've made an assumption which doesn't match the actual
[00:16:59:320 - 00:16:59:890] **Speaker 1:** structure.
[00:17:00:280 - 00:17:02:539] **Speaker 1:** So clearly we need to do something differently.
[00:17:03:989 - 00:17:06:069] **Speaker 1:** The question is how would we deal with this situation.
[00:17:07:619 - 00:17:10:319] **Speaker 1:** Well, what we're gonna do is rework through it, um,
[00:17:10:819 - 00:17:13:209] **Speaker 1:** keeping in mind the pin will force the two elements
[00:17:13:209 - 00:17:15:920] **Speaker 1:** to translate together in the X global and Y global
[00:17:15:920 - 00:17:18:900] **Speaker 1:** direction, but it will enable them to rotate independently.
[00:17:21:229 - 00:17:22:890] **Speaker 1:** So what we're gonna do is we'll rework the problem
[00:17:22:890 - 00:17:23:270] **Speaker 1:** now.
[00:17:24:729 - 00:17:27:229] **Speaker 1:** So we're actually gonna put 2 rotational degrees of freedom
[00:17:27:229 - 00:17:27:469] **Speaker 1:** here.
[00:17:28:399 - 00:17:30:088] **Speaker 1:** So we end up with 9 degrees of freedom now
[00:17:30:088 - 00:17:30:749] **Speaker 1:** instead of 8.
[00:17:31:129 - 00:17:33:279] **Speaker 1:** We still only have 1 translation in each direction, but
[00:17:33:279 - 00:17:34:749] **Speaker 1:** now we've got 2 rotations.
[00:17:35:619 - 00:17:39:449] **Speaker 1:** And what we'll do is that element 1 and 2
[00:17:39:949 - 00:17:43:920] **Speaker 1:** is a continuous beam, so they need to rotate together.
[00:17:44:349 - 00:17:48:189] **Speaker 1:** So we need to link element 1 and 2 together
[00:17:48:189 - 00:17:51:510] **Speaker 1:** to rotate this together, but we allow them to rotate
[00:17:51:510 - 00:17:53:969] **Speaker 1:** independently of element 2.
[00:17:55:839 - 00:17:58:369] **Speaker 1:** So when we do that, uh, we've just, we're our
[00:17:58:380 - 00:17:59:920] **Speaker 1:** our seo matric is changed a little bit.
[00:18:09:020 - 00:18:11:099] **Speaker 1:** So at this point in the middle.
[00:18:12:589 - 00:18:15:760] **Speaker 1:** We've now got This is the same as we had
[00:18:15:760 - 00:18:21:119] **Speaker 1:** before, D1, element 1 is Q1, D2 is Q2.
[00:18:22:219 - 00:18:24:150] **Speaker 1:** D3 is Q3.
[00:18:26:420 - 00:18:30:660] **Speaker 1:** Now we have D4 for element 1 is equal to
[00:18:30:660 - 00:18:31:339] **Speaker 1:** D2.
[00:18:33:270 - 00:18:35:160] **Speaker 1:** So deep 1, well and 2.
[00:18:36:400 - 00:18:40:000] **Speaker 1:** Which is equal to, they're also equal to D1 for
[00:18:40:000 - 00:18:41:920] **Speaker 1:** element 3, which is Q4.
[00:18:42:040 - 00:18:44:839] **Speaker 1:** So they're still all three elements are all still translating
[00:18:44:839 - 00:18:45:119] **Speaker 1:** together.
[00:18:46:439 - 00:18:47:439] **Speaker 1:** So, that's quite messy.
[00:18:50:119 - 00:18:54:500] **Speaker 1:** D4, 1, D1, 2, D1, 3.
[00:18:57:250 - 00:18:57:800] **Speaker 1:** Please do that.
[00:18:59:010 - 00:19:00:199] **Speaker 1:** D41.
[00:19:01:469 - 00:19:02:349] **Speaker 1:** D12.
[00:19:03:890 - 00:19:05:939] **Speaker 1:** D13 is Q4.
[00:19:07:390 - 00:19:10:329] **Speaker 1:** We're also gonna have D51.
[00:19:11:449 - 00:19:17:520] **Speaker 1:** D22 D23 is going to be equal to Q5.
[00:19:20:760 - 00:19:25:000] **Speaker 1:** And we'll link the um rotations to these two elements
[00:19:25:000 - 00:19:25:160] **Speaker 1:** together.
[00:19:25:239 - 00:19:28:229] **Speaker 1:** So, D6 for element one will be equal to D3
[00:19:28:630 - 00:19:32:000] **Speaker 1:** for element two, which will be equal to Q6.
[00:19:33:790 - 00:19:35:390] **Speaker 1:** But what we're gonna do here is we'll say that
[00:19:35:390 - 00:19:39:329] **Speaker 1:** D3 for element 3 is equal to Q7.
[00:19:40:109 - 00:19:42:469] **Speaker 1:** So previously these were all linked to the same variable.
[00:19:42:800 - 00:19:44:880] **Speaker 1:** We're still linking elements 1 and 2 together, but we're
[00:19:44:880 - 00:19:47:920] **Speaker 1:** decoupling that from element 3.
[00:19:51:329 - 00:19:54:530] **Speaker 1:** And then, of course, here, we have D6 for element
[00:19:54:530 - 00:19:58:369] **Speaker 1:** two is now Q8 because there's an extra degree of
[00:19:58:369 - 00:20:01:010] **Speaker 1:** freedom and D6 for element three.
[00:20:02:260 - 00:20:02:859] **Speaker 1:** Is Q.
[00:20:07:839 - 00:20:09:560] **Speaker 1:** So when we look at our assembly matrices.
[00:20:11:560 - 00:20:12:859] **Speaker 1:** We look at Q6 here.
[00:20:16:099 - 00:20:18:760] **Speaker 1:** And that corresponds to D6, for element 1.
[00:20:20:069 - 00:20:24:229] **Speaker 1:** And Q6 D3.
[00:20:25:969 - 00:20:28:849] **Speaker 1:** So there's still a linkage between those two elements.
[00:20:29:849 - 00:20:33:579] **Speaker 1:** But now The third element.
[00:20:35:660 - 00:20:36:660] **Speaker 1:** is no longer matching.
[00:20:36:739 - 00:20:39:140] **Speaker 1:** So we now have, these were all previously in the
[00:20:39:140 - 00:20:39:819] **Speaker 1:** same row.
[00:20:40:180 - 00:20:42:619] **Speaker 1:** There's now a mismatch and this this is now in
[00:20:42:619 - 00:20:45:319] **Speaker 1:** a different row links to a different degree of freedom.
[00:20:52:109 - 00:20:53:239] **Speaker 1:** So we can work through that.
[00:20:54:469 - 00:20:58:890] **Speaker 1:** Again, we've applied a slightly different process in terms of
[00:20:59:109 - 00:21:01:189] **Speaker 1:** labelling overall degrees of freedom.
[00:21:02:619 - 00:21:05:079] **Speaker 1:** Put in two rotations at a single node.
[00:21:06:260 - 00:21:09:140] **Speaker 1:** We've provided this mat mathematical decoupling, so now we actually
[00:21:09:140 - 00:21:12:770] **Speaker 1:** have two independent rotations that exist there, two key values,
[00:21:12:780 - 00:21:13:219] **Speaker 1:** um.
[00:21:14:089 - 00:21:17:890] **Speaker 1:** Allowing element 3 to rotate independently of that in elements
[00:21:17:890 - 00:21:18:489] **Speaker 1:** 1 and 2.
[00:21:20:930 - 00:21:23:130] **Speaker 1:** Just a bunch of intermediate results there, I'm not gonna
[00:21:23:130 - 00:21:24:670] **Speaker 1:** go through that step by step.
[00:21:25:800 - 00:21:30:609] **Speaker 1:** But when we work through that, We get uh uppercase
[00:21:30:609 - 00:21:32:410] **Speaker 1:** Fs, these are in global coordinates.
[00:21:32:449 - 00:21:35:910] **Speaker 1:** We transform them to local coordinates and then we're taking.
[00:21:37:449 - 00:21:38:739] **Speaker 1:** This information here.
[00:21:40:119 - 00:21:42:760] **Speaker 1:** We're plotting that down on a free body diagram and
[00:21:42:760 - 00:21:43:420] **Speaker 1:** we have.
[00:21:47:400 - 00:21:48:739] **Speaker 1:** Here and here.
[00:21:52:920 - 00:21:54:449] **Speaker 1:** Zero sheer force.
[00:21:58:569 - 00:21:59:890] **Speaker 1:** And 0 moment.
[00:22:03:699 - 00:22:06:339] **Speaker 1:** So we're now actually adhering to the problem setup.
[00:22:07:859 - 00:22:09:500] **Speaker 1:** So what we've actually done here is we've taken a
[00:22:09:500 - 00:22:12:859] **Speaker 1:** frame element and we've forced it to behave like a
[00:22:12:859 - 00:22:13:699] **Speaker 1:** bar element.
[00:22:14:260 - 00:22:17:349] **Speaker 1:** We've removed based by the way we set it up,
[00:22:17:780 - 00:22:20:119] **Speaker 1:** we've removed any ability for it to carry.
[00:22:20:859 - 00:22:24:099] **Speaker 1:** Bending moments or sheer forces, and we're forcing it to
[00:22:24:099 - 00:22:25:520] **Speaker 1:** only carry axial forces.
[00:22:26:349 - 00:22:29:880] **Speaker 1:** So, we can do that, um, that sort of reinforces
[00:22:30:310 - 00:22:36:900] **Speaker 1:** that, um, The bar elements are the more general solution.
[00:22:39:099 - 00:22:41:180] **Speaker 1:** So frame elements are the more general solution that they
[00:22:41:180 - 00:22:43:699] **Speaker 1:** can behave and capture all the mechanics of frames, but
[00:22:43:699 - 00:22:45:819] **Speaker 1:** also behave like bars if we need them to.
[00:22:47:900 - 00:22:49:310] **Speaker 1:** So is there any questions on that approach?
[00:22:49:650 - 00:22:50:050] **Speaker 1:** Any?
[00:22:55:760 - 00:22:58:160] **Speaker 1:** OK, so we'll move on, um, this is the, the
[00:22:58:160 - 00:22:59:380] **Speaker 1:** last lecture slide, so.
[00:23:00:010 - 00:23:03:329] **Speaker 1:** Um, just an overall summary of everything we've done in
[00:23:03:329 - 00:23:07:140] **Speaker 1:** the last, um, 4 weeks, so.
[00:23:08:339 - 00:23:15:010] **Speaker 1:** With um, We've got bar elements that carry only axial
[00:23:15:010 - 00:23:17:829] **Speaker 1:** forces, um, no sheer forces or moments.
[00:23:18:739 - 00:23:22:430] **Speaker 1:** Um, they only carry shear or so bars only carry
[00:23:22:430 - 00:23:24:910] **Speaker 1:** actual all the forces, beams only carry shear in moments
[00:23:24:910 - 00:23:26:530] **Speaker 1:** and frames are the general case that cover all of
[00:23:26:530 - 00:23:26:829] **Speaker 1:** it.
[00:23:27:680 - 00:23:30:880] **Speaker 1:** Um, we are only dealing with one dimensional elements, but
[00:23:31:199 - 00:23:33:839] **Speaker 1:** the approach we've used can be able to derive, uh,
[00:23:33:910 - 00:23:36:400] **Speaker 1:** much more complicated multi-dimensional elements.
[00:23:37:140 - 00:23:39:939] **Speaker 1:** Um, what we essentially have in this course is if
[00:23:39:939 - 00:23:45:180] **Speaker 1:** we go back to say a mass matrix times a
[00:23:47:270 - 00:23:49:050] **Speaker 1:** Use Q to be consistent.
[00:23:49:670 - 00:23:51:609] **Speaker 1:** You could have a vector of accelerations.
[00:23:53:010 - 00:23:54:750] **Speaker 1:** Then we have a C.
[00:23:55:859 - 00:23:58:000] **Speaker 1:** Times a vector of velocities.
[00:23:59:290 - 00:24:01:160] **Speaker 1:** Plus K.
[00:24:02:719 - 00:24:08:959] **Speaker 1:** Times Q Is equal to some forcing terms uppercase Q.
[00:24:10:739 - 00:24:13:819] **Speaker 1:** So for the purposes of this part of the course,
[00:24:14:380 - 00:24:16:579] **Speaker 1:** this is 0 and this is 0 and we're focused
[00:24:16:579 - 00:24:17:739] **Speaker 1:** just on this piece.
[00:24:18:560 - 00:24:20:650] **Speaker 1:** Which is just the static equilibrium.
[00:24:21:770 - 00:24:25:010] **Speaker 1:** Part, but everything we've done actually generalises very nicely to
[00:24:25:010 - 00:24:25:920] **Speaker 1:** dynamic problems.
[00:24:26:089 - 00:24:29:609] **Speaker 1:** So this is where I say, uh 402 or the
[00:24:30:079 - 00:24:31:670] **Speaker 1:** uh advanced vibrations course.
[00:24:33:020 - 00:24:35:180] **Speaker 1:** Comes in and can, can deal with multi degrees of
[00:24:35:180 - 00:24:35:540] **Speaker 1:** freedom.
[00:24:37:300 - 00:24:38:180] **Speaker 1:** And 4th year.
[00:24:41:089 - 00:24:43:349] **Speaker 1:** So, um, mass matrices can come in.
[00:24:44:369 - 00:24:46:130] **Speaker 1:** Uh, they can be generated in a very similar way
[00:24:46:130 - 00:24:47:589] **Speaker 1:** to the way we have distributed loads.
[00:24:49:880 - 00:24:52:099] **Speaker 1:** So, um, that can work quite easily.
[00:24:53:189 - 00:24:56:930] **Speaker 1:** We have damping matrices which are generally defined as a
[00:24:57:030 - 00:25:00:630] **Speaker 1:** um combination of mass and stiffness and then this is
[00:25:00:630 - 00:25:02:170] **Speaker 1:** the bit here.
[00:25:03:300 - 00:25:06:579] **Speaker 1:** Um, everything we've got is more generalizable, so.
[00:25:07:359 - 00:25:09:579] **Speaker 1:** One thing we also realise here is.
[00:25:10:989 - 00:25:12:209] **Speaker 1:** Our frame elements.
[00:25:16:290 - 00:25:21:150] **Speaker 1:** Uh, restricted 2 2D.
[00:25:22:989 - 00:25:27:930] **Speaker 1:** And if we extend 2 3D.
[00:25:31:869 - 00:25:33:670] **Speaker 1:** We get essentially.
[00:25:37:180 - 00:25:38:550] **Speaker 1:** Three translations.
[00:25:41:079 - 00:25:42:859] **Speaker 1:** And 3 rotations.
[00:25:46:839 - 00:25:50:989] **Speaker 1:** At each end So then that gives us 12 degrees
[00:25:50:989 - 00:25:51:449] **Speaker 1:** of freedom.
[00:25:53:530 - 00:25:54:199] **Speaker 1:** Per element.
[00:25:56:420 - 00:25:58:449] **Speaker 1:** Which is then a 12 by 12.
[00:26:00:540 - 00:26:01:689] **Speaker 1:** Stiffness matrix.
[00:26:03:520 - 00:26:06:099] **Speaker 1:** With 144 entries.
[00:26:07:189 - 00:26:07:670] **Speaker 1:** Within it.
[00:26:10:790 - 00:26:12:640] **Speaker 1:** Yeah, a lot, it's quite a sparse matrix, there's lots
[00:26:12:640 - 00:26:14:869] **Speaker 1:** of zeros in there, um, but there's also quite a
[00:26:14:869 - 00:26:15:790] **Speaker 1:** few non-zero terms.
[00:26:17:060 - 00:26:19:180] **Speaker 1:** But you don't necessarily have to code that up to
[00:26:19:180 - 00:26:21:140] **Speaker 1:** have a pretty good understanding of what's going on.
[00:26:21:219 - 00:26:23:380] **Speaker 1:** So you can use a commercial package which can deal
[00:26:23:380 - 00:26:25:160] **Speaker 1:** with three dimensional elements.
[00:26:26:280 - 00:26:29:599] **Speaker 1:** It's really not doing anything wildly different to what you've
[00:26:29:599 - 00:26:30:300] **Speaker 1:** coded.
[00:26:30:839 - 00:26:33:630] **Speaker 1:** There's a lot more bookkeeping when you're extending into three
[00:26:33:630 - 00:26:37:060] **Speaker 1:** dimensions, but the reaction mechanisms are very similar.
[00:26:39:709 - 00:26:41:579] **Speaker 1:** One thing just to be aware of that everything we've
[00:26:41:579 - 00:26:42:040] **Speaker 1:** done here.
[00:26:43:479 - 00:26:50:040] **Speaker 1:** Is Our analysis Is linear elastic.
[00:26:54:839 - 00:26:56:280] **Speaker 1:** And doesn't check.
[00:27:00:329 - 00:27:07:410] **Speaker 1:** For yielding So essentially at the moment, um, the code,
[00:27:07:439 - 00:27:10:760] **Speaker 1:** if we, if we put a loads on and we
[00:27:10:760 - 00:27:14:459] **Speaker 1:** got, you know, 100 megapascales of stress in an element
[00:27:15:040 - 00:27:17:280] **Speaker 1:** and we put 10 times that load on, we would
[00:27:17:280 - 00:27:18:359] **Speaker 1:** get 10 times the deflection.
[00:27:18:479 - 00:27:21:930] **Speaker 1:** We would calculate 1000 megapas scales of stress within that
[00:27:22:050 - 00:27:22:640] **Speaker 1:** element.
[00:27:23:199 - 00:27:25:780] **Speaker 1:** And if the element is not capable of sustaining that,
[00:27:26:359 - 00:27:28:319] **Speaker 1:** the code would not raise any sort of flag.
[00:27:28:400 - 00:27:30:300] **Speaker 1:** So there's additional checks would have to be done.
[00:27:32:189 - 00:27:43:839] **Speaker 1:** And also Buckling is also not considered So the, the
[00:27:43:839 - 00:27:47:119] **Speaker 1:** analysis as we have completed it doesn't raise any red
[00:27:47:119 - 00:27:51:630] **Speaker 1:** flags around an element being unstable due to buckling.
[00:27:52:869 - 00:27:55:260] **Speaker 1:** Now you can modify the code to adapt to that.
[00:27:55:270 - 00:27:57:050] **Speaker 1:** It's essentially an eigenvalue analysis.
[00:27:58:109 - 00:27:59:910] **Speaker 1:** But at the moment with the code you could have
[00:27:59:910 - 00:28:01:930] **Speaker 1:** an axial load on an element which is well beyond
[00:28:01:930 - 00:28:05:790] **Speaker 1:** the critical buckling load, the structure is actually unstable, but
[00:28:05:790 - 00:28:07:780] **Speaker 1:** your code won't raise any red flags about that.
[00:28:07:949 - 00:28:10:859] **Speaker 1:** So that's just something additional you can build on, um,
[00:28:10:869 - 00:28:12:150] **Speaker 1:** over and above what we've done here.
[00:28:15:699 - 00:28:19:079] **Speaker 1:** So I wanna just go through a few extra pages
[00:28:19:579 - 00:28:21:359] **Speaker 1:** just to show you a few extra things.
[00:28:21:859 - 00:28:22:260] **Speaker 1:** So.
[00:28:23:839 - 00:28:28:920] **Speaker 1:** Um This is actually some notes, uh, it's a collaborator
[00:28:28:920 - 00:28:31:500] **Speaker 1:** of mine actually at Duke University in the US.
[00:28:32:719 - 00:28:40:400] **Speaker 1:** Um So, this is the Burnerly oiler beam bending derivation
[00:28:40:400 - 00:28:43:579] **Speaker 1:** that he's presented, we go through, uh, you'll see some
[00:28:43:579 - 00:28:45:550] **Speaker 1:** shape functions here which look very much like what we've
[00:28:45:550 - 00:28:47:800] **Speaker 1:** done in this class, a similar notation.
[00:28:49:069 - 00:28:51:130] **Speaker 1:** We go through a bunch of derivations.
[00:28:52:209 - 00:28:53:709] **Speaker 1:** Much more derivations.
[00:28:55:040 - 00:28:55:859] **Speaker 1:** Much more.
[00:28:56:910 - 00:29:01:119] **Speaker 1:** And we get a mass matrix and uh um Here,
[00:29:01:380 - 00:29:04:069] **Speaker 1:** a stiffness matrix, and hopefully you look at this matrix
[00:29:04:069 - 00:29:05:630] **Speaker 1:** and go hang on, that looks a lot like something
[00:29:05:630 - 00:29:06:349] **Speaker 1:** we've already seen.
[00:29:07:089 - 00:29:10:260] **Speaker 1:** And you'd be right, that's exactly like what we've done.
[00:29:12:390 - 00:29:14:119] **Speaker 1:** But what we can also look at is this idea
[00:29:14:119 - 00:29:15:660] **Speaker 1:** of Timoshenko beam elements.
[00:29:16:910 - 00:29:19:589] **Speaker 1:** So this is taking into account.
[00:29:21:109 - 00:29:22:709] **Speaker 1:** We modelled this here.
[00:29:22:819 - 00:29:27:949] **Speaker 1:** So some total combined deflection in a beam is going
[00:29:27:949 - 00:29:32:469] **Speaker 1:** to be a superposition of, uh, simple moment loading like
[00:29:32:469 - 00:29:34:380] **Speaker 1:** this and then shear loading.
[00:29:34:430 - 00:29:36:989] **Speaker 1:** So the moments basically all of these lines trace back
[00:29:36:989 - 00:29:39:469] **Speaker 1:** to a single point of curvature when it's pure moment
[00:29:39:469 - 00:29:40:010] **Speaker 1:** loading.
[00:29:40:229 - 00:29:42:390] **Speaker 1:** And then there's also the shear loading, which is where
[00:29:42:390 - 00:29:44:829] **Speaker 1:** the the element goes into sort of a parallelogram.
[00:29:45:609 - 00:29:50:329] **Speaker 1:** When we did, we implemented the Benui Oila or um
[00:29:50:329 - 00:29:50:729] **Speaker 1:** Oa Beui.
[00:29:51:760 - 00:29:54:359] **Speaker 1:** We neglected this piece here, and if your beam is
[00:29:54:359 - 00:29:57:979] **Speaker 1:** relatively slender, this piece won't matter, it won't contribute significantly.
[00:29:58:560 - 00:29:59:800] **Speaker 1:** But if we were if we did have a shortened
[00:29:59:800 - 00:30:00:459] **Speaker 1:** squat beam.
[00:30:01:880 - 00:30:04:030] **Speaker 1:** What we can do, there's a a whole lot more
[00:30:04:270 - 00:30:08:030] **Speaker 1:** additional derivations, um, using shape functions.
[00:30:08:920 - 00:30:11:420] **Speaker 1:** And a bunch more derivations.
[00:30:11:920 - 00:30:14:900] **Speaker 1:** What we essentially get to is a matrix like this.
[00:30:14:959 - 00:30:17:319] **Speaker 1:** So it's symmetric, so essentially this just gets mirrored.
[00:30:18:479 - 00:30:20:920] **Speaker 1:** Now, you can see there's these values that exist through
[00:30:20:920 - 00:30:22:780] **Speaker 1:** here, so we have this um.
[00:30:24:930 - 00:30:25:369] **Speaker 1:** These guys.
[00:30:26:349 - 00:30:29:949] **Speaker 1:** Rating factors throughout the Equation.
[00:30:30:989 - 00:30:31:869] **Speaker 1:** Throughout the Matrix.
[00:30:33:410 - 00:30:35:810] **Speaker 1:** And these are the mortification factors.
[00:30:36:739 - 00:30:40:089] **Speaker 1:** That account for the Shia forces for the Shia defamations.
[00:30:41:540 - 00:30:44:859] **Speaker 1:** Now, what we're doing is we're contributing an extra deformation
[00:30:44:859 - 00:30:45:540] **Speaker 1:** mechanics.
[00:30:46:719 - 00:30:48:959] **Speaker 1:** So we would always expect this is actually to have
[00:30:48:959 - 00:30:52:229] **Speaker 1:** a lower stiffness and lead to larger deflections.
[00:30:52:719 - 00:30:53:920] **Speaker 1:** But you can see if you were to go through
[00:30:53:920 - 00:30:57:319] **Speaker 1:** the Tymoshenko element, um, do the derivation, you actually don't
[00:30:57:319 - 00:30:58:880] **Speaker 1:** get, it's not wildly different.
[00:30:58:959 - 00:31:00:280] **Speaker 1:** You can actually update your element.
[00:31:00:760 - 00:31:02:680] **Speaker 1:** You can use the Tymoshenko formulation.
[00:31:03:400 - 00:31:06:489] **Speaker 1:** The way it manipulates and multiplies through with transformation matrices
[00:31:06:489 - 00:31:08:410] **Speaker 1:** and assembly matrices is exactly the same.
[00:31:08:609 - 00:31:10:290] **Speaker 1:** You just have a few tweaks to your matrix and
[00:31:10:290 - 00:31:14:010] **Speaker 1:** now you can actually model something that has shared information
[00:31:14:010 - 00:31:14:550] **Speaker 1:** as well.
[00:31:18:290 - 00:31:20:729] **Speaker 1:** I also want to go through um some separate information.
[00:31:20:849 - 00:31:22:770] **Speaker 1:** So this is if you're looking at the, the three
[00:31:22:770 - 00:31:23:810] **Speaker 1:** dimensional elements.
[00:31:23:890 - 00:31:28:780] **Speaker 1:** So this is, um, It's actually from a research project,
[00:31:28:790 - 00:31:31:550] **Speaker 1:** but it was looking at, you know, Yeah, this matrix
[00:31:31:550 - 00:31:32:859] **Speaker 1:** hopefully looks quite familiar to you.
[00:31:33:719 - 00:31:34:939] **Speaker 1:** It's one that you've coated up.
[00:31:36:369 - 00:31:41:089] **Speaker 1:** But if we were to extend into 3 dimensions, Then
[00:31:41:089 - 00:31:43:890] **Speaker 1:** we have, this is used as UV, and W for
[00:31:43:890 - 00:31:47:109] **Speaker 1:** translations and it uses theta X theta Y and 3
[00:31:47:109 - 00:31:48:449] **Speaker 1:** Z for the rotation.
[00:31:48:530 - 00:31:51:469] **Speaker 1:** So we have essentially this here is all node one.
[00:31:53:260 - 00:31:55:699] **Speaker 1:** And then this piece here is node 2, and there's
[00:31:55:959 - 00:31:57:380] **Speaker 1:** 6 degrees of freedom for each of them.
[00:31:59:520 - 00:32:01:250] **Speaker 1:** And then you end up with this matrix here.
[00:32:01:319 - 00:32:03:770] **Speaker 1:** So this is, this is actually the Tymoshenko formulation that
[00:32:03:770 - 00:32:06:810] **Speaker 1:** has the same weighting factors to change and modify the
[00:32:06:810 - 00:32:08:069] **Speaker 1:** stiffness to include share.
[00:32:08:880 - 00:32:11:619] **Speaker 1:** Um, but this is the full three dimensional element.
[00:32:12:239 - 00:32:15:040] **Speaker 1:** So at that point, you've got a 12 by 12
[00:32:15:040 - 00:32:15:400] **Speaker 1:** matrix.
[00:32:15:479 - 00:32:18:660] **Speaker 1:** You have 144 individual stiffness terms, as I said before,
[00:32:18:959 - 00:32:20:680] **Speaker 1:** a lot of them are zero, but nonetheless, there's a
[00:32:20:680 - 00:32:21:439] **Speaker 1:** lot of stuff in here.
[00:32:22:410 - 00:32:25:689] **Speaker 1:** Um, and you, then you've got forces and moments in
[00:32:25:689 - 00:32:26:530] **Speaker 1:** the forcing vectors.
[00:32:27:589 - 00:32:31:839] **Speaker 1:** So again, um, It's not conceptually really any different to
[00:32:31:839 - 00:32:32:800] **Speaker 1:** what you've already coded up.
[00:32:32:880 - 00:32:35:650] **Speaker 1:** There's a lot more bookkeeping, a lot more messing around,
[00:32:35:869 - 00:32:36:219] **Speaker 1:** um.
[00:32:36:949 - 00:32:40:609] **Speaker 1:** But that's um sort of give you an idea of
[00:32:40:609 - 00:32:42:869] **Speaker 1:** what, if you did want to extend this to 3D,
[00:32:43:270 - 00:32:44:550] **Speaker 1:** um, what would be involved.
[00:32:48:209 - 00:32:49:609] **Speaker 1:** So is there any questions on any of that?
[00:32:53:800 - 00:32:55:930] **Speaker 1:** I just want to cover a couple of other things.
[00:32:57:310 - 00:32:59:910] **Speaker 1:** Just um on some of the context stuff.
[00:33:01:189 - 00:33:04:829] **Speaker 1:** So just in terms of um where the material we've
[00:33:04:829 - 00:33:07:390] **Speaker 1:** used sits in the broader context.
[00:33:07:699 - 00:33:10:540] **Speaker 1:** So um this was actually feedback from a prior teaching
[00:33:10:540 - 00:33:11:130] **Speaker 1:** survey.
[00:33:11:949 - 00:33:14:589] **Speaker 1:** Um, could provide a bit more background on what this
[00:33:14:589 - 00:33:15:989] **Speaker 1:** sort of analysis is used for.
[00:33:16:380 - 00:33:17:949] **Speaker 1:** I'm not sure whether this is only for learning or
[00:33:17:949 - 00:33:21:430] **Speaker 1:** whether they model building trusses like this, um, or whether
[00:33:21:430 - 00:33:23:469] **Speaker 1:** more complex models are used for building trusses.
[00:33:23:589 - 00:33:26:540] **Speaker 1:** Um, this was back when we were using MATLAB, um,
[00:33:26:550 - 00:33:28:829] **Speaker 1:** and saying, is this the code I actually use or
[00:33:28:829 - 00:33:29:969] **Speaker 1:** do they use something else?
[00:33:30:390 - 00:33:32:150] **Speaker 1:** Um, I'm aware learning doesn't have a W in it,
[00:33:32:229 - 00:33:35:150] **Speaker 1:** but that's how the, the code was the comment was
[00:33:35:150 - 00:33:35:689] **Speaker 1:** presented.
[00:33:37:420 - 00:33:40:180] **Speaker 1:** Um, so this is the one of the, the, there
[00:33:40:180 - 00:33:43:660] **Speaker 1:** are some commercial packages, um, they're coded in different things.
[00:33:43:780 - 00:33:46:250] **Speaker 1:** Some of them date back to the Fortran days, um,
[00:33:46:550 - 00:33:50:579] **Speaker 1:** different, different programming languages that have been compiled, but, um,
[00:33:50:780 - 00:33:53:510] **Speaker 1:** this is a three dimensional, uh, building.
[00:33:55:160 - 00:33:57:680] **Speaker 1:** Now, it'll be a little bit more complicated than what
[00:33:57:680 - 00:34:01:109] **Speaker 1:** you've um modelled in this class and that it actually
[00:34:01:109 - 00:34:06:180] **Speaker 1:** has some elements that accommodate for non-linear element actions.
[00:34:07:880 - 00:34:10:820] **Speaker 1:** But we may have, say, here you've actually got the
[00:34:10:820 - 00:34:11:330] **Speaker 1:** um.
[00:34:12:218 - 00:34:15:218] **Speaker 1:** Elements very similar to what you've modelled, but then for
[00:34:15:218 - 00:34:18:019] **Speaker 1:** the floors, there's a, um, floors have what we refer
[00:34:18:019 - 00:34:20:529] **Speaker 1:** to as a diaphragm action so that they tie the
[00:34:20:529 - 00:34:23:617] **Speaker 1:** building together and force everything to move together, um, so
[00:34:23:617 - 00:34:26:178] **Speaker 1:** often there'll be plate elements, two mension plate elements that
[00:34:26:178 - 00:34:27:999] **Speaker 1:** are used to model the the floor.
[00:34:29:229 - 00:34:32:607] **Speaker 1:** Um, this is also, um, some of the different versions.
[00:34:33:229 - 00:34:36:099] **Speaker 1:** So sometimes there'll be this lumped plasticity model.
[00:34:36:349 - 00:34:39:049] **Speaker 1:** So we'll have a linear elastic member through the middle.
[00:34:39:388 - 00:34:43:127] **Speaker 1:** So this piece labelled as the elastic member is basically
[00:34:43:127 - 00:34:45:529] **Speaker 1:** the exact same element that you've modelled.
[00:34:46:188 - 00:34:49:668] **Speaker 1:** But then putting a plastic hinge spring in at the
[00:34:49:668 - 00:34:49:928] **Speaker 1:** end.
[00:34:50:148 - 00:34:54:019] **Speaker 1:** So that's basically an additional element which is just rotational,
[00:34:54:428 - 00:34:57:589] **Speaker 1:** which provides the ability for some nonlinear action to be
[00:34:57:589 - 00:34:58:049] **Speaker 1:** included.
[00:34:59:209 - 00:35:00:229] **Speaker 1:** Now, why do that?
[00:35:00:729 - 00:35:04:250] **Speaker 1:** Um, for structural analysis that might seem like a pretty
[00:35:04:250 - 00:35:09:090] **Speaker 1:** simplification sim yeah, real simplification to put a hinge just
[00:35:09:090 - 00:35:11:689] **Speaker 1:** at the end, but that is actually how buildings have
[00:35:11:689 - 00:35:12:729] **Speaker 1:** traditionally been designed.
[00:35:12:969 - 00:35:15:889] **Speaker 1:** So, um, the concept of this, this is actually the
[00:35:15:889 - 00:35:17:469] **Speaker 1:** PricewaterhouseCoopers building.
[00:35:18:179 - 00:35:21:580] **Speaker 1:** Um, this was just on, uh, Armagh Street near the
[00:35:21:580 - 00:35:25:300] **Speaker 1:** end of New Regent Street, um, where the, uh, seagull
[00:35:25:300 - 00:35:25:699] **Speaker 1:** pit is.
[00:35:25:780 - 00:35:26:770] **Speaker 1:** I'm not sure if you're aware of that.
[00:35:26:860 - 00:35:28:800] **Speaker 1:** It's, it's been in the media a bit for being,
[00:35:28:899 - 00:35:31:399] **Speaker 1:** um, a joke tourist attraction in Christchurch.
[00:35:31:899 - 00:35:34:379] **Speaker 1:** Um, that's essentially the, the old foundation for this building
[00:35:34:379 - 00:35:35:439] **Speaker 1:** because the building's no longer there.
[00:35:36:120 - 00:35:38:199] **Speaker 1:** Um, but this was some of the damage that occurred
[00:35:38:199 - 00:35:42:280] **Speaker 1:** in that building, uh, following the 2011, um, earthquake.
[00:35:43:290 - 00:35:48:090] **Speaker 1:** And the structural design there has been basically to deliberately
[00:35:48:090 - 00:35:52:139] **Speaker 1:** detail the, Horizontal beam.
[00:35:53:020 - 00:35:55:580] **Speaker 1:** To protect the column, so that that beam will actually
[00:35:55:580 - 00:35:59:739] **Speaker 1:** yield and undergo damage, um, to limit the the moment
[00:35:59:739 - 00:36:02:580] **Speaker 1:** that it can, um, transfer into the column.
[00:36:02:860 - 00:36:05:260] **Speaker 1:** So the, the rationale for that, you know, if you,
[00:36:05:300 - 00:36:06:889] **Speaker 1:** if I'm sitting here, if you break my arm, I'm
[00:36:06:889 - 00:36:09:219] **Speaker 1:** not gonna be happy, but I can remain standing, you
[00:36:09:219 - 00:36:09:340] **Speaker 1:** know.
[00:36:09:659 - 00:36:11:659] **Speaker 1:** But if you break my leg, I'm gonna have a
[00:36:11:659 - 00:36:12:159] **Speaker 1:** real issue.
[00:36:13:120 - 00:36:13:820] **Speaker 1:** Remaining standing.
[00:36:13:919 - 00:36:17:600] **Speaker 1:** So you protect the columns at all costs, uh, because
[00:36:17:600 - 00:36:20:820] **Speaker 1:** that's what enables the building to remain standing.
[00:36:20:959 - 00:36:24:790] **Speaker 1:** So essentially it is around a design approach to have
[00:36:24:790 - 00:36:29:330] **Speaker 1:** um some ability to have, you know, ductile mechanism form,
[00:36:29:550 - 00:36:32:719] **Speaker 1:** um, but to limit the the moment transfer that goes
[00:36:32:719 - 00:36:35:320] **Speaker 1:** into the column, um, often referred to this as the
[00:36:35:320 - 00:36:36:500] **Speaker 1:** strong column weak beam.
[00:36:37:600 - 00:36:38:169] **Speaker 1:** Formulation.
[00:36:38:290 - 00:36:40:290] **Speaker 1:** So, often what you do is on a structure you
[00:36:40:290 - 00:36:42:949] **Speaker 1:** might have a simplified overall structural model.
[00:36:44:540 - 00:36:46:830] **Speaker 1:** And then once you know the forces that that element
[00:36:46:830 - 00:36:50:300] **Speaker 1:** actually has to carry, then doing a more detailed, uh,
[00:36:50:310 - 00:36:53:070] **Speaker 1:** analysis of exactly what the member should look like to
[00:36:53:070 - 00:36:53:989] **Speaker 1:** carry those loads.
[00:36:54:189 - 00:36:56:870] **Speaker 1:** So the, the top left thing to catch the overall
[00:36:56:870 - 00:36:59:909] **Speaker 1:** dynamics and distribution of load through the structure and then
[00:36:59:909 - 00:37:03:909] **Speaker 1:** the detailed model to capture, um, what, you know, physically
[00:37:03:909 - 00:37:05:340] **Speaker 1:** the the member looks like.
[00:37:06:929 - 00:37:09:250] **Speaker 1:** This is actually a photo that was taken in about
[00:37:09:250 - 00:37:09:919] **Speaker 1:** 2019.
[00:37:10:090 - 00:37:11:969] **Speaker 1:** Um, I took this down on Lichfield Street when there's
[00:37:11:969 - 00:37:14:280] **Speaker 1:** a construction, one of the car park buildings.
[00:37:15:290 - 00:37:18:090] **Speaker 1:** Um, if you're saying why a lumped plasticity model, if
[00:37:18:090 - 00:37:19:229] **Speaker 1:** we actually zoom in on this.
[00:37:20:300 - 00:37:24:370] **Speaker 1:** You can see a flange there um of the, The
[00:37:24:370 - 00:37:28:860] **Speaker 1:** I-beam And it's actually got this, this scalloping, or sometimes
[00:37:28:860 - 00:37:32:020] **Speaker 1:** referred to as dog boning of the, the flange.
[00:37:32:149 - 00:37:33:780] **Speaker 1:** So the question is, well, why would you do that?
[00:37:34:939 - 00:37:37:580] **Speaker 1:** Well, that's again it's exact same concept, it's the idea
[00:37:37:580 - 00:37:40:699] **Speaker 1:** of um selectively weakening the beam.
[00:37:41:540 - 00:37:45:100] **Speaker 1:** Such that it limits the moment transfer that's capable of
[00:37:45:100 - 00:37:47:060] **Speaker 1:** going into the column to protect the column.
[00:37:48:360 - 00:37:50:729] **Speaker 1:** Now, an obvious question might be, well, why don't you
[00:37:50:729 - 00:37:51:649] **Speaker 1:** just use a smaller beam?
[00:37:51:850 - 00:37:54:169] **Speaker 1:** If that that bean was too big, why don't you
[00:37:54:169 - 00:37:55:850] **Speaker 1:** just choose a smaller one rather than choosing a bigger
[00:37:55:850 - 00:37:56:929] **Speaker 1:** one and then weakening it.
[00:37:57:360 - 00:37:59:919] **Speaker 1:** Um, the reason for that is that, I mean, this
[00:37:59:919 - 00:38:00:770] **Speaker 1:** is a simple support.
[00:38:00:850 - 00:38:04:250] **Speaker 1:** It's a little bit of an oversimplification, but, um, generally
[00:38:04:250 - 00:38:06:689] **Speaker 1:** speaking for gravity loads, you have a peak moment halfway
[00:38:06:689 - 00:38:10:209] **Speaker 1:** along the beam and a lower moments, uh, in the
[00:38:10:209 - 00:38:10:449] **Speaker 1:** middle.
[00:38:10:530 - 00:38:13:290] **Speaker 1:** So by doing things this way, you've got the the
[00:38:13:290 - 00:38:15:389] **Speaker 1:** moment capacity at the mid-span where you need it.
[00:38:15:850 - 00:38:18:709] **Speaker 1:** And then you've got a limit on the moment capacity
[00:38:18:709 - 00:38:20:570] **Speaker 1:** of that, uh, near the column.
[00:38:22:580 - 00:38:24:379] **Speaker 1:** This was a project that I was involved with.
[00:38:24:580 - 00:38:26:489] **Speaker 1:** Um, I did the seismic dampers for this.
[00:38:26:540 - 00:38:29:500] **Speaker 1:** It's in the Mission District of San Francisco and this
[00:38:29:500 - 00:38:32:959] **Speaker 1:** was, it's actually a a um community housing project.
[00:38:34:010 - 00:38:37:379] **Speaker 1:** And This was the actual um concept of the building
[00:38:37:379 - 00:38:39:659] **Speaker 1:** on the left and then on the right was actually
[00:38:39:659 - 00:38:42:820] **Speaker 1:** the um the model that was done to capture all
[00:38:42:820 - 00:38:43:760] **Speaker 1:** the dynamics of this building.
[00:38:43:860 - 00:38:47:530] **Speaker 1:** So there's some key um lateral resistant systems that go
[00:38:47:530 - 00:38:49:699] **Speaker 1:** up through the building and then there was the plate
[00:38:49:699 - 00:38:52:739] **Speaker 1:** elements to model the foundation mat grid.
[00:38:53:560 - 00:38:56:050] **Speaker 1:** Uh, and that's actually used a rocking foundation detail.
[00:38:56:129 - 00:39:00:010] **Speaker 1:** We're under a large earthquake, actually get controlled uplift of
[00:39:00:010 - 00:39:03:250] **Speaker 1:** part of the foundation on the pile, and This is
[00:39:03:250 - 00:39:05:510] **Speaker 1:** some of the models that are applied that were required
[00:39:05:510 - 00:39:06:409] **Speaker 1:** for the design of that building.
[00:39:06:530 - 00:39:09:090] **Speaker 1:** So a lot of this, um, is using some of
[00:39:09:090 - 00:39:12:010] **Speaker 1:** the elements very similar to what you've done, extending also
[00:39:12:010 - 00:39:15:469] **Speaker 1:** to some plate elements to capture floors and foundations, um,
[00:39:15:530 - 00:39:16:370] **Speaker 1:** but yeah.
[00:39:17:179 - 00:39:19:729] **Speaker 1:** This was actually this is the seismic dam on the
[00:39:19:729 - 00:39:21:840] **Speaker 1:** on the left and then this is the completed building
[00:39:21:840 - 00:39:22:580] **Speaker 1:** on the right.
[00:39:23:810 - 00:39:28:330] **Speaker 1:** Um, so the elements that you've derived are powerful in
[00:39:28:330 - 00:39:29:010] **Speaker 1:** their own right.
[00:39:30:459 - 00:39:31:830] **Speaker 1:** But they're also a key stepping stone.
[00:39:31:909 - 00:39:33:290] **Speaker 1:** We've essentially dealt with.
[00:39:34:389 - 00:39:35:889] **Speaker 1:** This top left hand corner here.
[00:39:37:439 - 00:39:39:760] **Speaker 1:** We've, yeah, we've actually gone to a frame, so we've
[00:39:39:760 - 00:39:43:189] **Speaker 1:** got other loads, but we can extend into two dimensions,
[00:39:43:280 - 00:39:46:870] **Speaker 1:** we can extend into three dimensions and all the principles
[00:39:46:870 - 00:39:49:040] **Speaker 1:** that we've done also apply to those as well.
[00:39:49:120 - 00:39:51:669] **Speaker 1:** So in 3 dimensions, if you want to know how
[00:39:51:669 - 00:39:55:000] **Speaker 1:** much uh given point within an element has moved in
[00:39:55:000 - 00:39:58:500] **Speaker 1:** the 3 dimensions, you're just going to do probably linear
[00:39:58:500 - 00:40:01:090] **Speaker 1:** interpolation in the 3 dimensions.
[00:40:01:560 - 00:40:03:100] **Speaker 1:** So we've only done it along one.
[00:40:04:270 - 00:40:08:199] **Speaker 1:** But you're just applying that to multidimensional, so not a
[00:40:08:199 - 00:40:09:030] **Speaker 1:** huge change there.
[00:40:10:419 - 00:40:15:159] **Speaker 1:** Um So, yeah, essentially if you were to um continue
[00:40:15:159 - 00:40:17:739] **Speaker 1:** on with this next year and look at um conti
[00:40:17:739 - 00:40:21:679] **Speaker 1:** continuum elements, you'll see many of the same concepts that
[00:40:21:679 - 00:40:24:500] **Speaker 1:** are applied there as have been applied in this course.
[00:40:25:699 - 00:40:27:010] **Speaker 1:** Now there's one other thing I just want to touch
[00:40:27:010 - 00:40:27:530] **Speaker 1:** on recently.
[00:40:27:580 - 00:40:31:000] **Speaker 1:** It actually relates to a, um, an ongoing research project,
[00:40:31:300 - 00:40:32:100] **Speaker 1:** um, that I've got.
[00:40:32:209 - 00:40:35:550] **Speaker 1:** This is actually for, um, it's with University of, uh,
[00:40:35:560 - 00:40:39:300] **Speaker 1:** sorry, Lehigh University in Bethlehem, Pennsylvania, um.
[00:40:40:159 - 00:40:43:729] **Speaker 1:** And this is looking at um Basically being able to
[00:40:43:729 - 00:40:49:139] **Speaker 1:** simulate new damper designs, um, for a high-rise building, we
[00:40:49:139 - 00:40:53:370] **Speaker 1:** don't actually have the capacity as humans to recreate that
[00:40:53:860 - 00:40:55:949] **Speaker 1:** without spending an eye-watering amount of money.
[00:40:56:919 - 00:41:00:050] **Speaker 1:** Um, I've been fortunate to have visited the two largest
[00:41:00:050 - 00:41:03:399] **Speaker 1:** shake table facilities on Earth, um, which are essentially huge
[00:41:03:399 - 00:41:05:989] **Speaker 1:** hydraulic facilities to recreate ground motions.
[00:41:06:409 - 00:41:08:030] **Speaker 1:** Um, one of them is in just out of the
[00:41:08:030 - 00:41:11:070] **Speaker 1:** one that was the, the world, world's largest one for,
[00:41:11:250 - 00:41:14:020] **Speaker 1:** for about 20 years, uh, just out of Kobe in
[00:41:14:020 - 00:41:14:429] **Speaker 1:** Japan.
[00:41:15:090 - 00:41:17:290] **Speaker 1:** And then last year, China opened one that was just
[00:41:17:290 - 00:41:19:469] **Speaker 1:** sort of slightly bigger in all capacities.
[00:41:20:129 - 00:41:23:649] **Speaker 1:** Um, so take it all, all the specs and multiply
[00:41:23:649 - 00:41:25:510] **Speaker 1:** them by about 1.1, and you've got the new one.
[00:41:26:659 - 00:41:30:260] **Speaker 1:** Um Even though they have about uh I think the
[00:41:30:270 - 00:41:32:699] **Speaker 1:** the the one in Japan has a 1200 tonne payload,
[00:41:32:899 - 00:41:37:219] **Speaker 1:** the one in um, Tianjin has about a 1350 tonne
[00:41:37:219 - 00:41:37:699] **Speaker 1:** payload.
[00:41:39:280 - 00:41:41:600] **Speaker 1:** So that is quite significant, um, given that it can
[00:41:41:600 - 00:41:46:449] **Speaker 1:** accelerate that at 2G, um, but also, um, You know,
[00:41:46:530 - 00:41:49:590] **Speaker 1:** it's still 1200 tonnes isn't that much, so.
[00:41:50:320 - 00:41:54:360] **Speaker 1:** Um, the ability to actually dynamically test a full-scale high-rise
[00:41:54:360 - 00:41:57:070] **Speaker 1:** building is just not something that we as humans have
[00:41:57:070 - 00:41:58:820] **Speaker 1:** chosen to invest in in that scale.
[00:41:58:959 - 00:42:04:169] **Speaker 1:** Um, even the, um, The, the ones that do exist,
[00:42:04:270 - 00:42:07:409] **Speaker 1:** um, the, the, the facility in Japan cost about $500
[00:42:07:409 - 00:42:10:500] **Speaker 1:** million US dollars in 2003, so probably about a billion
[00:42:10:500 - 00:42:12:330] **Speaker 1:** dollars US dollars today to create that facility.
[00:42:13:560 - 00:42:16:649] **Speaker 1:** And one alternative here is actually to, if we wanted
[00:42:16:649 - 00:42:19:889] **Speaker 1:** to rapidly assess the way different damper designs could work
[00:42:19:889 - 00:42:20:629] **Speaker 1:** within a structure.
[00:42:21:330 - 00:42:24:209] **Speaker 1:** We can actually take, you know, physically test a damper
[00:42:24:209 - 00:42:27:639] **Speaker 1:** here while linking that in real time to a structural
[00:42:27:639 - 00:42:27:929] **Speaker 1:** model.
[00:42:28:120 - 00:42:31:689] **Speaker 1:** So when you're dealing with brake dependent aspects, so this
[00:42:31:689 - 00:42:33:750] **Speaker 1:** here is actually a viscous fluid damper.
[00:42:34:050 - 00:42:37:429] **Speaker 1:** It has a non-Newtonian fluid with nonlinear force velocity response.
[00:42:37:770 - 00:42:39:469] **Speaker 1:** So you do need to test that in real time.
[00:42:40:709 - 00:42:44:610] **Speaker 1:** So in this situation, what we're doing is actually simulating
[00:42:44:610 - 00:42:49:790] **Speaker 1:** this high-rise building, um, but physically imparting this into different
[00:42:49:790 - 00:42:53:300] **Speaker 1:** damper specimens and then recording the force that comes back,
[00:42:53:429 - 00:42:55:330] **Speaker 1:** getting that back into the model and having to do
[00:42:55:330 - 00:42:56:510] **Speaker 1:** all of this in real time.
[00:42:56:790 - 00:42:59:949] **Speaker 1:** So if you're doing running a one millisecond control on
[00:42:59:949 - 00:43:02:899] **Speaker 1:** your control system, all the computation has to be done
[00:43:02:899 - 00:43:03:989] **Speaker 1:** within that time frame.
[00:43:04:070 - 00:43:06:610] **Speaker 1:** So this is just a video of how it works.
[00:43:06:989 - 00:43:54:459] **Speaker 1:** So Um, we also have the, um, Wind loading case
[00:43:54:459 - 00:43:54:919] **Speaker 1:** here.
[00:43:57:139 - 00:44:04:729] **Speaker 1:** So You have lost the sound on that one, but
[00:44:04:939 - 00:44:06:850] **Speaker 1:** the idea is you're actually testing the, the damper in
[00:44:06:850 - 00:44:08:350] **Speaker 1:** real time and integrating that with the model.
[00:44:08:969 - 00:44:11:370] **Speaker 1:** So it's quite a, quite a complicated thing to set
[00:44:11:370 - 00:44:11:610] **Speaker 1:** up.
[00:44:11:800 - 00:44:15:350] **Speaker 1:** Um, there's a lot of, um, computational ability required and
[00:44:15:719 - 00:44:17:370] **Speaker 1:** the model has to be set up quite quickly with
[00:44:17:370 - 00:44:20:590] **Speaker 1:** an explicit algorithm to solve quickly enough.
[00:44:20:800 - 00:44:24:010] **Speaker 1:** Um, but of course, numerical stability is quite concerning when
[00:44:24:010 - 00:44:27:510] **Speaker 1:** you're doing stuff in real time, um, because very quickly
[00:44:27:510 - 00:44:32:159] **Speaker 1:** you're, um, Hydrox can end up um running away if
[00:44:32:159 - 00:44:34:909] **Speaker 1:** your command's going wrong, so you need some good interlocks
[00:44:35:120 - 00:44:36:659] **Speaker 1:** on that to control things.
[00:44:37:429 - 00:44:39:929] **Speaker 1:** Uh, this is actually a multi-scale, this worked out at
[00:44:39:929 - 00:44:40:510] **Speaker 1:** Le high.
[00:44:41:810 - 00:45:11:800] **Speaker 1:** Oh So there's a model of a three-style, three-story structural
[00:45:11:800 - 00:45:18:889] **Speaker 1:** frame, and linking that to um, How the um.
[00:45:19:909 - 00:45:22:270] **Speaker 1:** How the greater granite structure would work and looking at
[00:45:22:270 - 00:45:24:810] **Speaker 1:** different damping behaviour and how that affects the dynamics.
[00:45:25:310 - 00:45:27:790] **Speaker 1:** And then finally, one thing we can also do is,
[00:45:27:909 - 00:45:31:110] **Speaker 1:** uh, for, for a structure, uh, it's interaction with this
[00:45:31:110 - 00:45:33:629] **Speaker 1:** underlying soil is actually quite can have quite an impact
[00:45:33:629 - 00:45:36:709] **Speaker 1:** on its response, um, both positive or negative depending on
[00:45:36:709 - 00:45:37:429] **Speaker 1:** the situation.
[00:45:37:550 - 00:45:39:830] **Speaker 1:** So in this case, there's actually the structure and then
[00:45:39:830 - 00:45:45:199] **Speaker 1:** modelling the surrounding soil, um, And then testing the damper,
[00:45:45:399 - 00:45:46:479] **Speaker 1:** different damper configurations.
[00:45:46:560 - 00:45:50:000] **Speaker 1:** So physical damper test, computational model of the structure as
[00:45:50:000 - 00:45:50:739] **Speaker 1:** is shown here.
[00:46:23:620 - 00:46:26:699] **Speaker 1:** It's probably The, the interesting part of that is pretty
[00:46:26:699 - 00:46:27:370] **Speaker 1:** fast at this point.
[00:46:28:290 - 00:46:30:370] **Speaker 1:** Um, so that's just maybe gives you a small taste
[00:46:30:370 - 00:46:31:919] **Speaker 1:** of some of the things, you know, a lot of
[00:46:31:919 - 00:46:34:649] **Speaker 1:** these models are actually using, uh, more complex elements in
[00:46:34:649 - 00:46:38:090] **Speaker 1:** addition to what you've done in this class, um, but
[00:46:38:090 - 00:46:41:689] **Speaker 1:** include the element types that you've, you've modelled.
[00:46:41:770 - 00:46:43:879] **Speaker 1:** So they are actually quite capable in their own right,
[00:46:44:239 - 00:46:46:350] **Speaker 1:** as well as being a stepping stone to bigger things,
[00:46:46:530 - 00:46:46:830] **Speaker 1:** so.
[00:46:47:260 - 00:46:49:379] **Speaker 1:** Um, that kind of, I guess, draws a, a close
[00:46:49:379 - 00:46:50:659] **Speaker 1:** in terms of the final lecture for this part of
[00:46:50:659 - 00:46:51:179] **Speaker 1:** the course.
[00:46:51:500 - 00:46:53:780] **Speaker 1:** As I said, it won't be in the last UCF
[00:46:53:780 - 00:46:55:520] **Speaker 1:** me with an assignment and a test still to go,
[00:46:55:620 - 00:46:57:899] **Speaker 1:** so, um, yeah, I'll still be in touch quite a
[00:46:57:899 - 00:46:58:820] **Speaker 1:** bit over the next few weeks.
[00:46:58:979 - 00:47:01:179] **Speaker 1:** Um, but otherwise, thanks for coming on this morning, and
[00:47:01:179 - 00:47:04:209] **Speaker 1:** I'll see you, uh, labs next week, um, we'll be
[00:47:04:209 - 00:47:05:370] **Speaker 1:** in sort of on Thursday.
[00:47:05:620 - 00:47:07:419] **Speaker 1:** You'll have only done 3 lectures with James, you probably
[00:47:07:419 - 00:47:10:620] **Speaker 1:** haven't covered enough information, um, to do too, too much
[00:47:10:620 - 00:47:12:419] **Speaker 1:** meaningful for James as part of the course.
[00:47:12:899 - 00:47:15:219] **Speaker 1:** I'm also, well, I think we're both aware that with
[00:47:15:219 - 00:47:16:580] **Speaker 1:** the test the following Tuesday.
[00:47:17:010 - 00:47:19:090] **Speaker 1:** Uh, maybe James's content won't be front of mind for
[00:47:19:090 - 00:47:19:290] **Speaker 1:** you.
[00:47:19:409 - 00:47:23:010] **Speaker 1:** So, um, we will run the, the labs next week
[00:47:23:010 - 00:47:25:810] **Speaker 1:** on this part of the course, and it will essentially
[00:47:25:810 - 00:47:27:449] **Speaker 1:** just be a health session ahead of the test.
[00:47:27:530 - 00:47:30:209] **Speaker 1:** So there won't be any specific, um, new exercises.
[00:47:30:250 - 00:47:32:179] **Speaker 1:** It'll just be an opportunity for you to work through
[00:47:32:179 - 00:47:33:489] **Speaker 1:** prior tests and seek help.
[00:47:33:689 - 00:47:36:250] **Speaker 1:** So, otherwise, thank you all, and I'll see you again
[00:47:36:250 - 00:47:36:929] **Speaker 1:** in the future.
[00:48:08:820 - 00:48:09:360] **Speaker 0:** Thank you.
[00:48:14:870 - 00:48:27:919] **Speaker 0:** And It's I just quite clear why it wasn't 00
[00:48:27:929 - 00:48:28:889] **Speaker 0:** so that was just why it first set up the
[00:48:28:889 - 00:48:30:050] **Speaker 1:** problem, um.
[00:48:31:060 - 00:48:32:860] **Speaker 1:** Essentially this was the problem.
[00:48:32:939 - 00:48:35:139] **Speaker 1:** So this element was actually pinned at both ends.
[00:48:35:810 - 00:48:37:919] **Speaker 1:** So it's not, it should only be carrying an actual
[00:48:37:919 - 00:48:40:489] **Speaker 0:** load, so it shouldn't be carrying it if we welded
[00:48:40:489 - 00:48:44:219] **Speaker 0:** it, it would end up a load of money, but
[00:48:44:219 - 00:48:45:439] **Speaker 0:** because it's carried both hands.
[00:48:51:699 - 00:48:55:139] **Speaker 0:** Aren't those stampers in the video, are they purely reacting,
[00:48:55:219 - 00:48:56:600] **Speaker 0:** or do they have like a system?
[00:48:56:889 - 00:48:58:419] **Speaker 0:** Uh, they are purely reactional.
[00:48:58:540 - 00:49:03:399] **Speaker 0:** Um, there are some genetic effect between them, um, which
[00:49:03:399 - 00:49:03:409] **Speaker 0:** is.
[00:49:04:300 - 00:49:05:969] **Speaker 0:** Um, some of the work that I've done is looking
[00:49:05:969 - 00:49:17:750] **Speaker 0:** at, but there is a concern for 20 years perpendicular
[00:49:21:620 - 00:49:25:050] **Speaker 1:** any control system, you know, people say earthquakes are rare
[00:49:25:050 - 00:49:27:639] **Speaker 1:** and power cuts are rare, but the two go together,
[00:49:28:419 - 00:49:30:409] **Speaker 1:** so, um, there is a little bit of reluctance to
[00:49:30:409 - 00:49:30:580] **Speaker 1:** actually.
[00:49:31:719 - 00:49:34:159] **Speaker 0:** Because this, you know, it's such a chaotic time when
[00:49:34:159 - 00:49:39:479] **Speaker 1:** you behave, so generally passive is more favoured by practitioners.
[00:49:39:600 - 00:49:42:439] **Speaker 1:** Yeah, that makes sense, um, and you said we don't
[00:49:42:439 - 00:49:45:840] **Speaker 2:** account for buckling when we're modelling like the the wiggly
[00:49:45:840 - 00:49:47:520] **Speaker 2:** deflection of the element.
[00:49:47:580 - 00:49:50:360] **Speaker 2:** Yeah, that's, is that not taken into.
[00:49:51:530 - 00:49:55:159] **Speaker 1:** Uh, so we, there's difference between like the transversing the
[00:49:55:159 - 00:49:55:429] **Speaker 1:** power for a mine.
[00:49:57:580 - 00:50:00:020] **Speaker 2:** Oh, that's purely the moment making it Wiggle.
[00:50:00:820 - 00:50:02:979] **Speaker 1:** Um, but the Buckton is very much like a.
[00:50:04:139 - 00:50:06:840] **Speaker 1:** Uh, impressive axial load, which leads to a loss of
[00:50:06:840 - 00:50:07:689] **Speaker 1:** lateral stiffness.
[00:50:07:989 - 00:50:12:260] **Speaker 1:** So it's a very specific phenomenon, um, that's, yeah, the,
[00:50:12:330 - 00:50:13:070] **Speaker 1:** where the, the basic structure.
[00:50:15:300 - 00:50:17:250] **Speaker 1:** Because of that, and that's something that is like we
[00:50:17:250 - 00:50:18:020] **Speaker 1:** can modify to it.
[00:50:20:600 - 00:50:20:610] **Speaker 1:** So.
[00:50:24:770 - 00:50:26:929] **Speaker 1:** So it is actually a relatively simple addition.
[00:50:28:870 - 00:50:29:290] **Speaker 0:** Thank you.
[00:51:19:409 - 00:51:34:320] **Speaker 0:** Just wasn't really What girl?
[00:51:39:780 - 00:51:56:010] **Speaker 0:** No Yes, I was sick.
[00:52:28:959 - 00:52:37:989] **Speaker 0:** That Yes.
[00:52:39:179 - 00:53:31:929] **Speaker 0:** Yeah I wasn't expecting Yeah like Yeah.
[00:54:58:739 - 00:54:58:770] **Speaker 0:** It

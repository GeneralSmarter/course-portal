# ENME302-26S2 Lecture 4 native Echo transcript

Date: July 17, 2026 11:00am-11:55am
Transcript type: native Echo automated transcript.

[00:00:18:559 - 00:00:18:590] **Speaker 0:** I'm.
[00:00:20:409 - 00:00:27:879] **Speaker 0:** sure Well, Kyorakoto, welcome along, everyone.
[00:00:31:170 - 00:00:36:599] **Speaker 0:** So I just want to start today with a quick
[00:00:36:599 - 00:00:37:540] **Speaker 1:** recap of the lab.
[00:00:42:860 - 00:00:47:450] **Speaker 1:** So, um, this lab sheet, the lab sheet itself was
[00:00:47:450 - 00:00:49:540] **Speaker 1:** available electronically and I've also now put up a version
[00:00:49:540 - 00:00:53:180] **Speaker 1:** with some annotations with some, some answers and some, some
[00:00:53:180 - 00:00:55:340] **Speaker 1:** notes that just sort of supplements that, so both the
[00:00:55:340 - 00:00:58:630] **Speaker 1:** original document and this one available on the course learn
[00:00:58:630 - 00:00:58:650] **Speaker 1:** page.
[00:00:59:909 - 00:01:01:689] **Speaker 1:** So I just want to cover very quickly some of
[00:01:01:689 - 00:01:01:880] **Speaker 1:** this.
[00:01:01:979 - 00:01:05:059] **Speaker 1:** So, um, just looking at some of the, the annotations
[00:01:05:059 - 00:01:07:059] **Speaker 1:** here is just some of the, the Python commands entering
[00:01:07:059 - 00:01:09:139] **Speaker 1:** an array, not gonna spend too long on that.
[00:01:09:180 - 00:01:10:699] **Speaker 1:** I think you understand how to do that.
[00:01:11:190 - 00:01:14:199] **Speaker 1:** Um, just looking at the, um, the definition to do
[00:01:14:199 - 00:01:14:720] **Speaker 1:** this step.
[00:01:15:360 - 00:01:18:769] **Speaker 1:** Um, with regard to transposing, One thing you notice there
[00:01:18:769 - 00:01:22:730] **Speaker 1:** is you can use the NP.transpose, um, but within Python
[00:01:22:730 - 00:01:26:410] **Speaker 1:** there is actually every, um, array actually has this, this
[00:01:26:410 - 00:01:28:430] **Speaker 1:** implicit, um, subfield.
[00:01:28:529 - 00:01:31:860] **Speaker 1:** So if you say A.T, then that's actually the transpose.
[00:01:31:930 - 00:01:34:209] **Speaker 1:** So that's something that's actually just sort of parked there
[00:01:34:410 - 00:01:38:050] **Speaker 1:** as part of the generation of the um variable, so.
[00:01:38:839 - 00:01:41:489] **Speaker 1:** Without having to predefine what A.T is, you can actually
[00:01:41:489 - 00:01:43:010] **Speaker 1:** use A.T as the transpose.
[00:01:43:089 - 00:01:45:769] **Speaker 1:** So that is quite a useful shorthand and we will
[00:01:45:769 - 00:01:49:080] **Speaker 1:** be using the the matrix transpose a bit in this
[00:01:49:080 - 00:01:49:410] **Speaker 1:** class.
[00:01:49:610 - 00:01:51:269] **Speaker 1:** So I just wanted to draw your attention to that,
[00:01:51:529 - 00:01:51:889] **Speaker 1:** um.
[00:01:52:739 - 00:01:54:839] **Speaker 1:** This here was a bit where we looked at the
[00:01:55:059 - 00:02:00:540] **Speaker 1:** um collation of uh individual submatrices and the the concatenation
[00:02:00:540 - 00:02:03:370] **Speaker 1:** of those together into a single larger matrix.
[00:02:03:489 - 00:02:06:860] **Speaker 1:** And when we come to transformation matrices, you'll see why
[00:02:06:860 - 00:02:08:490] **Speaker 1:** I've included that as an example.
[00:02:09:020 - 00:02:11:119] **Speaker 1:** Um, now there's multiple ways of doing that.
[00:02:11:149 - 00:02:13:449] **Speaker 1:** In this case, I've created a variable called zeros 3
[00:02:13:449 - 00:02:16:139] **Speaker 1:** by 3, which is just a matrix, 3 by 3
[00:02:16:139 - 00:02:17:139] **Speaker 1:** matrix of zeros.
[00:02:17:720 - 00:02:19:520] **Speaker 1:** And then you could either do some sort of, you
[00:02:19:520 - 00:02:22:279] **Speaker 1:** know, concatenate the top and bottom together and then concatenate
[00:02:22:279 - 00:02:24:220] **Speaker 1:** the the two together vertically.
[00:02:24:759 - 00:02:25:800] **Speaker 1:** Uh, that would be one way of doing it.
[00:02:25:839 - 00:02:28:039] **Speaker 1:** But there's also this NP.block command.
[00:02:28:330 - 00:02:31:000] **Speaker 1:** So if you use that, you can actually then piece
[00:02:31:000 - 00:02:35:169] **Speaker 1:** together a larger matrix or a larger array, um, Based
[00:02:35:169 - 00:02:40:740] **Speaker 1:** upon just piecing together, uh, individual submatrices or arrays, um,
[00:02:40:820 - 00:02:42:660] **Speaker 1:** that are themselves more than just scales.
[00:02:42:979 - 00:02:46:139] **Speaker 1:** So that is quite a useful shorthand, um, something that
[00:02:46:139 - 00:02:48:100] **Speaker 1:** many of you may already be quite familiar with, but
[00:02:48:100 - 00:02:49:339] **Speaker 1:** if you're not, I just want to draw your attention
[00:02:49:339 - 00:02:50:740] **Speaker 1:** to that because that will help you in a few
[00:02:50:740 - 00:02:51:240] **Speaker 1:** weeks.
[00:02:51:779 - 00:02:54:460] **Speaker 1:** Um, and then I talked about this yesterday, um, there's
[00:02:54:460 - 00:02:54:800] **Speaker 1:** NP.
[00:02:54:809 - 00:02:58:699] **Speaker 1:** mat mole, which is the full matrix multiplication and knowing
[00:02:58:699 - 00:03:01:419] **Speaker 1:** that that is distinct from just the star sign, which
[00:03:01:419 - 00:03:03:619] **Speaker 1:** is an element by element multiplication.
[00:03:04:110 - 00:03:06:710] **Speaker 1:** And there's also the convenient shorthand of just the at
[00:03:06:710 - 00:03:07:289] **Speaker 1:** symbol.
[00:03:12:910 - 00:03:14:119] **Speaker 0:** Alright and.
[00:03:17:220 - 00:03:20:179] **Speaker 1:** This was just an iterative point here, um, so trying
[00:03:20:179 - 00:03:21:919] **Speaker 1:** to find the solution to this equation.
[00:03:22:220 - 00:03:24:300] **Speaker 1:** You can work through and have the, the intercepts and
[00:03:24:300 - 00:03:26:899] **Speaker 1:** things and then this is the the set here.
[00:03:27:139 - 00:03:29:820] **Speaker 1:** Um, there are some commands here with say the dollar
[00:03:29:820 - 00:03:32:020] **Speaker 1:** signs and things around them, um, to actually get like
[00:03:32:020 - 00:03:36:419] **Speaker 1:** the square root into the, um, legend and essentially you've
[00:03:36:419 - 00:03:39:100] **Speaker 1:** got a full kind of latex text editor embedded into
[00:03:39:100 - 00:03:42:419] **Speaker 1:** Python which can format entries into the, the legends and
[00:03:42:419 - 00:03:43:419] **Speaker 1:** things within the plots.
[00:03:44:369 - 00:03:47:059] **Speaker 1:** Um, there's some information there about the, the fixed point
[00:03:47:059 - 00:03:49:839] **Speaker 1:** iteration and finding the, the intercepts.
[00:03:50:020 - 00:03:53:460] **Speaker 1:** Um, I did mention this yesterday around the way that
[00:03:53:460 - 00:03:56:979] **Speaker 1:** you can, the shorthand that you can enter variables and
[00:03:56:979 - 00:04:03:250] **Speaker 1:** then Um, Finally, we also talked about this yesterday, so
[00:04:03:610 - 00:04:07:250] **Speaker 1:** just about formatting that in the weeks to come, um,
[00:04:07:960 - 00:04:09:949] **Speaker 1:** I did notice this yesterday, but yeah, there is a
[00:04:09:949 - 00:04:11:270] **Speaker 1:** variable explorer within Spider.
[00:04:11:350 - 00:04:13:589] **Speaker 1:** It's very powerful, it's very useful, and if you choose
[00:04:13:589 - 00:04:15:429] **Speaker 1:** to use that, then that's probably, yeah, it's quite a
[00:04:15:429 - 00:04:16:790] **Speaker 1:** good idea, it's quite a useful thing.
[00:04:17:308 - 00:04:21:058] **Speaker 1:** Um, if you're, I mean some people still prefer To
[00:04:21:058 - 00:04:24:039] **Speaker 1:** print print the command window and display the variables that
[00:04:24:039 - 00:04:24:459] **Speaker 1:** way.
[00:04:25:039 - 00:04:27:019] **Speaker 1:** I know in the future labs, if we're coming to
[00:04:27:209 - 00:04:28:908] **Speaker 1:** help you debug code and there's just this kind of,
[00:04:28:959 - 00:04:32:398] **Speaker 1:** you know, massive sort of jumble of numbers, it can
[00:04:32:398 - 00:04:33:359] **Speaker 1:** be quite hard to interpret.
[00:04:33:438 - 00:04:37:278] **Speaker 1:** So that was just this extra um information here around
[00:04:37:278 - 00:04:38:739] **Speaker 1:** sort of formatting that output.
[00:04:39:118 - 00:04:42:720] **Speaker 1:** So, Um, this backslash in.
[00:04:43:589 - 00:04:46:269] **Speaker 1:** That exists in here, that is essentially to say that
[00:04:46:269 - 00:04:48:130] **Speaker 1:** define the A equals and then start a new line
[00:04:48:799 - 00:04:50:209] **Speaker 1:** before you start displaying the variable.
[00:04:51:799 - 00:04:54:019] **Speaker 1:** And it's quite useful in that it just stops the
[00:04:54:019 - 00:04:57:010] **Speaker 1:** first row being offset, um, so you can read down
[00:04:57:010 - 00:04:58:730] **Speaker 1:** columns much more easily.
[00:04:59:089 - 00:05:02:600] **Speaker 1:** So, um, and then, as I mentioned this yesterday, um,
[00:05:02:609 - 00:05:05:600] **Speaker 1:** in terms of ways to display, um, we haven't got
[00:05:05:600 - 00:05:08:049] **Speaker 1:** quite got to the, the largest stiffness matrices here, but
[00:05:08:049 - 00:05:10:109] **Speaker 1:** when we get to them, this is quite a useful
[00:05:10:450 - 00:05:13:109] **Speaker 1:** way to display them, um, particularly if you're referencing against,
[00:05:13:200 - 00:05:15:529] **Speaker 1:** um, some intermediate steps that I've given you in the
[00:05:15:529 - 00:05:18:410] **Speaker 1:** notes and you want to check your code, um, this
[00:05:18:410 - 00:05:21:390] **Speaker 1:** format to reference against the notes is pretty much cleaner.
[00:05:21:899 - 00:05:25:579] **Speaker 1:** In this format and um help you understand a lot
[00:05:25:579 - 00:05:28:660] **Speaker 1:** easier and also help us to help you, um, if
[00:05:28:660 - 00:05:31:079] **Speaker 1:** you need any help with the, the debugging.
[00:05:31:459 - 00:05:34:779] **Speaker 1:** So just want those, uh, it's pretty quite a useful
[00:05:35:140 - 00:05:39:160] **Speaker 1:** reference document over the next few weeks, um, for those
[00:05:39:160 - 00:05:43:140] **Speaker 1:** that, um, have any questions with Python, um, I am
[00:05:43:140 - 00:05:46:750] **Speaker 1:** well aware that With Python, there's no single correct way
[00:05:46:750 - 00:05:48:690] **Speaker 1:** to code things and I'm not necessarily saying that that
[00:05:48:690 - 00:05:50:970] **Speaker 1:** is the, you know, absolute best way of doing it,
[00:05:51:010 - 00:05:52:429] **Speaker 1:** but it, it is our way of doing it.
[00:05:53:299 - 00:05:56:959] **Speaker 1:** Um Any questions on that or anything that came up
[00:05:56:959 - 00:05:57:820] **Speaker 1:** in the lab yesterday?
[00:06:04:059 - 00:06:05:950] **Speaker 1:** If not, we'll jump across to the notes.
[00:06:06:380 - 00:06:08:820] **Speaker 1:** So you're gonna pick up on page 18 here.
[00:06:11:239 - 00:06:14:679] **Speaker 1:** So, what we're gonna do here is we're gonna, it's
[00:06:14:679 - 00:06:15:899] **Speaker 1:** this is a very simple structure.
[00:06:16:480 - 00:06:20:119] **Speaker 1:** It's a two-element bar structure, a horizontal element, and inclined
[00:06:20:119 - 00:06:20:619] **Speaker 1:** element.
[00:06:21:279 - 00:06:24:160] **Speaker 1:** We've got pins joints at the the left-hand side and
[00:06:24:160 - 00:06:26:160] **Speaker 1:** then we've got a couple of loads acting on it.
[00:06:27:739 - 00:06:30:380] **Speaker 1:** Now this is hopefully something that you would either in
[00:06:30:380 - 00:06:34:230] **Speaker 1:** 202 or actually the the initial um solution of that
[00:06:34:230 - 00:06:37:100] **Speaker 1:** would actually probably date back to 102 um or any
[00:06:37:100 - 00:06:38:279] **Speaker 1:** equivalent course that you've done.
[00:06:40:670 - 00:06:42:059] **Speaker 1:** And we want to try and solve this.
[00:06:42:540 - 00:06:44:670] **Speaker 1:** So the first thing we do is we solve for
[00:06:44:670 - 00:06:47:730] **Speaker 1:** the forces within an element, and then we wanna know
[00:06:48:390 - 00:06:50:709] **Speaker 1:** these, these two nodal points haven't deflected at all, but
[00:06:50:709 - 00:06:53:100] **Speaker 1:** if we want to know the, the horizontal and vertical
[00:06:53:100 - 00:06:55:760] **Speaker 1:** deflection of this node, how would we go about that?
[00:06:56:109 - 00:06:59:230] **Speaker 1:** So in the previous courses, you would certainly be used
[00:06:59:230 - 00:07:01:950] **Speaker 1:** to resolving forces and working out the internal forces within
[00:07:01:950 - 00:07:05:019] **Speaker 1:** them, but you may not necessarily, um, or certainly in
[00:07:05:019 - 00:07:06:869] **Speaker 1:** 22 you would have, but in prior courses you might
[00:07:06:869 - 00:07:07:450] **Speaker 1:** not have.
[00:07:08:390 - 00:07:10:470] **Speaker 1:** Gone through and looked at the, the displaced position of
[00:07:10:470 - 00:07:11:970] **Speaker 1:** this node in too much detail.
[00:07:14:420 - 00:07:15:899] **Speaker 1:** So what we've seen here is that we have external
[00:07:15:899 - 00:07:17:100] **Speaker 1:** forces Q1 and Q2.
[00:07:17:309 - 00:07:20:859] **Speaker 1:** So the horizontal load is zero, but the vertical load
[00:07:20:859 - 00:07:23:230] **Speaker 1:** is 100 kilonewtons and it's acting upwards.
[00:07:23:859 - 00:07:26:140] **Speaker 1:** So we have a global coordinate system here with X
[00:07:26:140 - 00:07:29:380] **Speaker 1:** and Y, and we always align our global degrees of
[00:07:29:380 - 00:07:32:000] **Speaker 1:** freedom and the forcing terms with this.
[00:07:32:380 - 00:07:32:730] **Speaker 1:** So.
[00:07:33:820 - 00:07:36:540] **Speaker 1:** Um, this is probably a little bit of a, um,
[00:07:37:820 - 00:07:39:940] **Speaker 1:** A step forward because we will cover this in more
[00:07:39:940 - 00:07:43:959] **Speaker 1:** detail next week, but Um, at a structural level.
[00:07:53:160 - 00:07:57:309] **Speaker 1:** We use Lowercase q.
[00:08:00:549 - 00:08:04:730] **Speaker 1:** To define Allowable degrees of freedom.
[00:08:13:049 - 00:08:14:510] **Speaker 1:** And uppercase Q.
[00:08:20:679 - 00:08:30:390] **Speaker 1:** To define The corresponding Applied external loads.
[00:08:41:929 - 00:08:44:570] **Speaker 1:** So we define a degree of freedom anywhere that there
[00:08:44:570 - 00:08:47:510] **Speaker 1:** is the potential for non-zero displacements to occur.
[00:08:49:150 - 00:08:51:760] **Speaker 1:** It may be based upon the specific loads that are
[00:08:51:760 - 00:08:54:200] **Speaker 1:** carried by a structure, that one of those happens to
[00:08:54:200 - 00:08:58:059] **Speaker 1:** be zero, but, Based upon all the possible loading cases
[00:08:58:059 - 00:09:00:859] **Speaker 1:** that could be applied, there is the potential for there
[00:09:00:859 - 00:09:02:979] **Speaker 1:** to be a non-zero displacement.
[00:09:03:179 - 00:09:05:659] **Speaker 1:** So we don't define any global degrees of freedom here
[00:09:05:659 - 00:09:09:380] **Speaker 1:** or here because they're pinned, they're fully constrained, and no
[00:09:09:380 - 00:09:14:619] **Speaker 1:** matter what loads the structures carries, the deflection that exists
[00:09:14:619 - 00:09:16:219] **Speaker 1:** here and here must be zero.
[00:09:16:299 - 00:09:18:859] **Speaker 1:** So there's no permissible displacement can occur there.
[00:09:19:109 - 00:09:20:309] **Speaker 1:** We don't define degrees of freedom.
[00:09:21:830 - 00:09:25:309] **Speaker 1:** In this situation, There is the potential for both the
[00:09:25:309 - 00:09:27:109] **Speaker 1:** horizontal and vertical deflections to be zero.
[00:09:27:190 - 00:09:29:919] **Speaker 1:** We'll apply some loads and the, the members will deflect.
[00:09:30:640 - 00:09:32:760] **Speaker 1:** And there's the potential for non-zero deflection.
[00:09:32:880 - 00:09:34:919] **Speaker 1:** So we put a Q1 and a Q2.
[00:09:35:000 - 00:09:39:119] **Speaker 1:** So lowercase Q1 is the deflection component, uppercase Q1 is
[00:09:39:119 - 00:09:41:440] **Speaker 1:** the forcing term, and so they always come as a
[00:09:41:440 - 00:09:42:250] **Speaker 1:** matched pair.
[00:09:42:640 - 00:09:45:400] **Speaker 1:** And then we also have a Q2, a lowercase Q2
[00:09:45:400 - 00:09:49:080] **Speaker 1:** and an uppercase Q2, which is the vertical deflection and
[00:09:49:080 - 00:09:51:640] **Speaker 1:** the corresponding vertically applied force at this node.
[00:09:54:130 - 00:09:55:489] **Speaker 1:** So what we're gonna do initially is we're just gonna
[00:09:55:489 - 00:09:58:090] **Speaker 1:** solve this as you would have in previous years.
[00:09:58:289 - 00:10:00:090] **Speaker 1:** So this might be something that you would have done
[00:10:00:090 - 00:10:03:289] **Speaker 1:** with Paul Doherty in the previous year in 202 or
[00:10:03:289 - 00:10:04:710] **Speaker 1:** any equivalent course that you've done.
[00:10:06:549 - 00:10:07:719] **Speaker 1:** The first thing we're gonna do is just do a
[00:10:07:719 - 00:10:10:679] **Speaker 1:** cut around this nodal point and draw a free body
[00:10:10:679 - 00:10:11:359] **Speaker 1:** diagram.
[00:10:11:679 - 00:10:14:640] **Speaker 1:** So we've got 100 kilonewton external load upwards, we've put
[00:10:14:640 - 00:10:16:859] **Speaker 1:** some internal forces to find in here.
[00:10:17:679 - 00:10:20:440] **Speaker 1:** And we do a force resolution, so we do um
[00:10:20:440 - 00:10:21:960] **Speaker 1:** vertical force equilibrium first.
[00:10:22:159 - 00:10:26:070] **Speaker 1:** We've got 100 kilomewtons upwards here, then we have the
[00:10:26:890 - 00:10:32:109] **Speaker 1:** F2 times causes of 45 degrees is the um vertical
[00:10:32:369 - 00:10:32:969] **Speaker 1:** deflection.
[00:10:34:020 - 00:10:36:219] **Speaker 1:** The sort of vertical component of this force.
[00:10:37:340 - 00:10:39:619] **Speaker 1:** And then we sumize that tells us that this force
[00:10:39:619 - 00:10:42:700] **Speaker 1:** here, F2, is a tensile force with a value of
[00:10:42:700 - 00:10:45:419] **Speaker 1:** 141.42 kilonewtons.
[00:10:45:500 - 00:10:48:780] **Speaker 1:** So it's root 2 times the 100 kilonewton applied.
[00:10:50:539 - 00:10:52:340] **Speaker 1:** We, once we know that we can do horizontal force
[00:10:52:340 - 00:10:53:109] **Speaker 1:** equilibrium.
[00:10:53:469 - 00:10:56:669] **Speaker 1:** We have force F1, we have the horizontal component of
[00:10:56:669 - 00:10:57:369] **Speaker 1:** this force.
[00:10:58:359 - 00:11:02:869] **Speaker 1:** And that um Tells us that the, the horizontal component
[00:11:02:869 - 00:11:08:909] **Speaker 1:** of this, um, Works out that the F1 is -100
[00:11:08:909 - 00:11:09:510] **Speaker 1:** kilonewtons.
[00:11:09:669 - 00:11:11:710] **Speaker 1:** So that's saying it's a magnitude of 100 and it's
[00:11:11:710 - 00:11:13:590] **Speaker 1:** actually in compression or this one's in tension.
[00:11:16:869 - 00:11:18:669] **Speaker 1:** Once we know that information, we know the the force
[00:11:18:669 - 00:11:21:750] **Speaker 1:** carried by each member, we can go through and just
[00:11:21:750 - 00:11:24:549] **Speaker 1:** do the, the, the applied force, the length of the
[00:11:24:549 - 00:11:26:989] **Speaker 1:** element, the cross section divide by the cross-sectional area and
[00:11:26:989 - 00:11:30:510] **Speaker 1:** the elastic modulus, put those numbers in, and these are
[00:11:30:510 - 00:11:31:289] **Speaker 1:** the amounts.
[00:11:32:229 - 00:11:36:469] **Speaker 1:** By which the deflected position, the the amount by which
[00:11:36:469 - 00:11:38:590] **Speaker 1:** each member has structural deflected.
[00:11:39:030 - 00:11:43:169] **Speaker 1:** So member one has contracted by 0.637 millimetres and member
[00:11:43:169 - 00:11:46:349] **Speaker 1:** two has extended by 1.27 millimetres.
[00:11:48:580 - 00:11:49:940] **Speaker 1:** That's a key bit of information.
[00:11:50:739 - 00:11:51:719] **Speaker 1:** That's a key step.
[00:11:52:669 - 00:11:54:859] **Speaker 1:** Towards getting where we want.
[00:11:54:929 - 00:11:56:780] **Speaker 1:** So we now have the force in each member, and
[00:11:56:780 - 00:11:59:330] **Speaker 1:** we know how, how the change in length of each
[00:11:59:330 - 00:12:00:179] **Speaker 1:** of the two members.
[00:12:01:479 - 00:12:03:840] **Speaker 1:** But if we want to know the final deflective position
[00:12:03:840 - 00:12:04:580] **Speaker 1:** of this node.
[00:12:06:239 - 00:12:07:440] **Speaker 1:** There's a little bit more work to do.
[00:12:10:010 - 00:12:12:650] **Speaker 1:** So what we actually do here is bearing in mind
[00:12:12:650 - 00:12:15:570] **Speaker 1:** that member one has contracted slightly and member 2 has
[00:12:15:570 - 00:12:18:950] **Speaker 1:** extended slightly, we need to find the point at which
[00:12:19:409 - 00:12:24:070] **Speaker 1:** they, the point in space at which those new length
[00:12:24:070 - 00:12:26:489] **Speaker 1:** requirements can be simultaneously met for both members.
[00:12:28:739 - 00:12:30:239] **Speaker 1:** So what we're gonna do here is we're actually gonna
[00:12:30:900 - 00:12:31:559] **Speaker 1:** describe an arc.
[00:12:32:710 - 00:12:36:609] **Speaker 1:** We're gonna start here at the support point, because that's,
[00:12:36:750 - 00:12:38:650] **Speaker 1:** it can't move, that's a nice reference.
[00:12:39:659 - 00:12:40:869] **Speaker 1:** Number one is in compression.
[00:12:41:739 - 00:12:45:580] **Speaker 1:** It's contracted, so we're gonna do a very exaggerated um
[00:12:45:580 - 00:12:48:590] **Speaker 1:** compression of that member, so the com the compressed length.
[00:12:49:530 - 00:12:50:969] **Speaker 1:** Maybe somewhere here.
[00:12:54:179 - 00:12:56:380] **Speaker 1:** And what we're gonna do here is we're going to
[00:12:56:380 - 00:12:57:059] **Speaker 1:** describe an arc.
[00:12:58:390 - 00:13:01:630] **Speaker 1:** And we're going to say, well, this is the, the,
[00:13:01:900 - 00:13:03:809] **Speaker 1:** the range of points in space.
[00:13:04:989 - 00:13:06:450] **Speaker 1:** That that node C can exist.
[00:13:08:239 - 00:13:10:479] **Speaker 1:** And meet that links requirement.
[00:13:11:229 - 00:13:14:229] **Speaker 1:** So it's an arc based at this point here, based
[00:13:14:229 - 00:13:18:229] **Speaker 1:** upon the new unstressed length of the member, the new
[00:13:18:229 - 00:13:19:190] **Speaker 1:** stress length of the member.
[00:13:21:200 - 00:13:22:900] **Speaker 1:** Conversely, member 2 has lengthened.
[00:13:23:059 - 00:13:25:450] **Speaker 1:** So we're gonna start here at the same reference point,
[00:13:25:500 - 00:13:27:299] **Speaker 1:** it's fixed support, so it's not gonna move, so that's
[00:13:27:299 - 00:13:27:840] **Speaker 1:** a nice.
[00:13:28:799 - 00:13:30:049] **Speaker 1:** Uh, displacement data.
[00:13:31:479 - 00:13:33:280] **Speaker 1:** There is a line line here that actually extends out
[00:13:33:280 - 00:13:33:650] **Speaker 1:** a bit.
[00:13:33:929 - 00:13:35:309] **Speaker 1:** It's longer than the initial element.
[00:13:37:059 - 00:13:39:590] **Speaker 1:** And then we're gonna scribe an arc that.
[00:13:42:580 - 00:13:44:750] **Speaker 1:** Is based around there, so.
[00:13:45:760 - 00:13:47:200] **Speaker 1:** What it's saying is you can imagine if we were
[00:13:47:200 - 00:13:50:320] **Speaker 1:** to take the pin out between those two members and
[00:13:50:320 - 00:13:52:880] **Speaker 1:** we were to replace them with two new members that
[00:13:52:880 - 00:13:56:159] **Speaker 1:** are unstressed, but they're, they're varied in length by these
[00:13:56:159 - 00:13:56:940] **Speaker 1:** dimensions.
[00:13:57:280 - 00:13:59:750] **Speaker 1:** We're gonna say, we're gonna move these two elements around
[00:13:59:750 - 00:14:00:179] **Speaker 1:** in space.
[00:14:00:239 - 00:14:01:599] **Speaker 1:** We're gonna find a point where we could put the
[00:14:01:599 - 00:14:05:000] **Speaker 1:** pin back through and get and simultaneously meet these length
[00:14:05:000 - 00:14:05:520] **Speaker 1:** requirements.
[00:14:07:559 - 00:14:09:799] **Speaker 1:** As you can see on the sketch, at that point.
[00:14:10:549 - 00:14:11:890] **Speaker 1:** Is actually here.
[00:14:12:030 - 00:14:15:200] **Speaker 1:** That's the, the point those two arcs intersect is the
[00:14:15:200 - 00:14:18:659] **Speaker 1:** point that we can simultaneously meet those length requirements and,
[00:14:19:200 - 00:14:22:200] **Speaker 1:** um, that would be the new deflected position of the
[00:14:22:200 - 00:14:22:599] **Speaker 1:** element.
[00:14:24:380 - 00:14:26:859] **Speaker 1:** Now solving that using the true arcs is actually quite
[00:14:26:859 - 00:14:27:280] **Speaker 1:** tough.
[00:14:29:099 - 00:14:30:140] **Speaker 1:** So what we're gonna do is we're gonna do a
[00:14:30:140 - 00:14:32:239] **Speaker 1:** linearized equivalent of this.
[00:14:38:440 - 00:14:39:650] **Speaker 1:** So the next page here.
[00:14:40:760 - 00:14:42:630] **Speaker 1:** We've essentially got the linearized version.
[00:14:42:719 - 00:14:46:969] **Speaker 1:** So, so this is the, The true shape here that
[00:14:46:969 - 00:14:48:989] **Speaker 1:** I just drew on the previous page is actually kind
[00:14:48:989 - 00:14:49:590] **Speaker 1:** of an arc.
[00:14:50:650 - 00:14:56:489] **Speaker 1:** Which comes up And kind of deviates through here.
[00:14:58:869 - 00:15:00:159] **Speaker 1:** And maybe goes off up here.
[00:15:00:270 - 00:15:02:630] **Speaker 1:** So it's, it's perpendicular here and then deviates as you
[00:15:02:630 - 00:15:03:119] **Speaker 1:** go up.
[00:15:03:510 - 00:15:08:140] **Speaker 1:** And then this other arc, um, is essentially starts parallel
[00:15:08:140 - 00:15:10:330] **Speaker 1:** to that line there and then it deviates out.
[00:15:12:320 - 00:15:14:219] **Speaker 1:** So the true position would be this one here.
[00:15:15:510 - 00:15:19:489] **Speaker 1:** But we're doing a linearized small deflection assumption of that
[00:15:19:869 - 00:15:21:210] **Speaker 1:** to define this quadrilateral.
[00:15:21:429 - 00:15:25:130] **Speaker 1:** And that's, um, essentially the method we're applying.
[00:15:28:359 - 00:15:30:960] **Speaker 1:** It does assume small deflections, so it neglects those second
[00:15:30:960 - 00:15:31:599] **Speaker 1:** order terms.
[00:15:31:799 - 00:15:34:359] **Speaker 1:** So while that's the true position in space, this is
[00:15:34:359 - 00:15:36:440] **Speaker 1:** the one we're actually gonna find based upon a small
[00:15:36:440 - 00:15:37:239] **Speaker 1:** angle assumption.
[00:15:38:900 - 00:15:41:580] **Speaker 1:** So that's where this weird sort of quadrilateral here with
[00:15:41:580 - 00:15:42:880] **Speaker 1:** the dashed lines come from.
[00:15:43:299 - 00:15:47:099] **Speaker 1:** It's translating that concept and then putting the linear, the
[00:15:47:099 - 00:15:49:979] **Speaker 1:** linearization and the small angle assumption onto that.
[00:15:50:130 - 00:15:53:500] **Speaker 1:** So this down here is the initial underplaced position of
[00:15:53:500 - 00:15:56:770] **Speaker 1:** joint C, and this point up here is the final
[00:15:56:770 - 00:15:58:280] **Speaker 1:** displaced position of joint C.
[00:15:58:700 - 00:16:00:260] **Speaker 1:** So we know this, we don't yet know this, and
[00:16:00:260 - 00:16:02:340] **Speaker 1:** we've got gonna go through some process to try and
[00:16:02:340 - 00:16:03:159] **Speaker 1:** find what this is.
[00:16:05:919 - 00:16:13:489] **Speaker 1:** Now, What we see here This one here is.
[00:16:15:630 - 00:16:16:469] **Speaker 1:** Element one.
[00:16:21:330 - 00:16:25:880] **Speaker 1:** Contracted by 0.637.
[00:16:26:989 - 00:16:29:020] **Speaker 1:** millimetres and then element 2.
[00:16:33:619 - 00:16:35:229] **Speaker 1:** Extended or elongated.
[00:16:36:559 - 00:16:43:250] **Speaker 1:** By The value was, sorry, just one second, 1.27 millimetres.
[00:16:45:479 - 00:16:46:479] **Speaker 1:** So that's the values we know.
[00:16:46:559 - 00:16:48:260] **Speaker 1:** We know this one here.
[00:16:49:520 - 00:16:50:520] **Speaker 1:** And we know E2.
[00:16:53:799 - 00:16:55:369] **Speaker 1:** We know there's 45 degrees in here.
[00:16:55:760 - 00:16:56:960] **Speaker 1:** Now you may look at that and go, well, hang
[00:16:56:960 - 00:16:57:239] **Speaker 1:** on.
[00:16:58:049 - 00:17:00:789] **Speaker 1:** You know, the, the thing's gonna deflect that 45 degrees
[00:17:01:090 - 00:17:03:489] **Speaker 1:** is, you know, that will change a little bit and
[00:17:03:489 - 00:17:07:250] **Speaker 1:** it will, um, but the thing is we're applying throughout
[00:17:07:250 - 00:17:09:530] **Speaker 1:** everything we do in this course, we're applying small deflection
[00:17:09:530 - 00:17:09:890] **Speaker 1:** assumptions.
[00:17:09:969 - 00:17:12:969] **Speaker 1:** So we're the underlying premise of that is the assumption
[00:17:12:969 - 00:17:17:930] **Speaker 1:** that the initial geometry is a fair approximation of the
[00:17:17:930 - 00:17:18:829] **Speaker 1:** final geometry.
[00:17:19:130 - 00:17:26:079] **Speaker 1:** So if The deflection is so large that the initial
[00:17:26:079 - 00:17:28:530] **Speaker 1:** geometry is not a fair approximation of the final geometry,
[00:17:29:030 - 00:17:31:550] **Speaker 1:** then we'll have to add some extra steps in there.
[00:17:33:430 - 00:17:35:229] **Speaker 1:** So this is the value we calculated on the previous
[00:17:35:229 - 00:17:38:349] **Speaker 1:** page as is this, and there's a few ways we
[00:17:38:349 - 00:17:38:550] **Speaker 1:** can do it.
[00:17:38:630 - 00:17:42:089] **Speaker 1:** We know this 45 degrees, we know it's 135 degrees,
[00:17:42:390 - 00:17:44:209] **Speaker 1:** and we wanna try and get this value here.
[00:17:44:469 - 00:17:47:109] **Speaker 1:** So what we can do here, there's a couple of
[00:17:47:109 - 00:17:49:089] **Speaker 1:** different ways we can work through this process.
[00:17:49:750 - 00:17:51:630] **Speaker 1:** Um, we know this side, we know this side, and
[00:17:51:630 - 00:17:54:469] **Speaker 1:** we have this kind of awkward four-sided shape.
[00:17:55:760 - 00:17:58:280] **Speaker 1:** We could extend out into a larger triangle.
[00:17:58:560 - 00:18:01:560] **Speaker 1:** So this looks um triangle here with the dotted line.
[00:18:02:160 - 00:18:03:459] **Speaker 1:** We know the side length.
[00:18:04:319 - 00:18:06:939] **Speaker 1:** We know this internal angle, so we could work out
[00:18:07:520 - 00:18:08:920] **Speaker 1:** this side length here.
[00:18:09:719 - 00:18:11:709] **Speaker 1:** And then we can add the 6 point.
[00:18:12:719 - 00:18:16:319] **Speaker 1:** 0.637 and we can add the 1.795 together, and we
[00:18:16:319 - 00:18:21:109] **Speaker 1:** know that this side here is 2.432 millimetres, and based
[00:18:21:109 - 00:18:24:119] **Speaker 1:** upon the fact that this is an equilateral triangle, that
[00:18:24:119 - 00:18:28:280] **Speaker 1:** would mean that the vertical deflection is 2.432 millimetres.
[00:18:30:380 - 00:18:33:359] **Speaker 1:** Alternatively, we could say, put a line through here.
[00:18:34:900 - 00:18:37:689] **Speaker 1:** Um, we could extend up here.
[00:18:38:500 - 00:18:40:979] **Speaker 1:** We could break this out into one small triangle, a
[00:18:40:979 - 00:18:43:660] **Speaker 1:** rectangle, and another triangle, and we could trace through the
[00:18:43:660 - 00:18:44:719] **Speaker 1:** geometry that way.
[00:18:45:060 - 00:18:46:439] **Speaker 1:** It would give us the same result.
[00:18:49:060 - 00:18:51:780] **Speaker 1:** So what that tells us is there's quite a lot
[00:18:51:780 - 00:18:53:619] **Speaker 1:** of manual intervention there, you know, we've had to give
[00:18:53:619 - 00:18:56:459] **Speaker 1:** quite a lot of thought, we've had to draw diagrams
[00:18:56:459 - 00:18:57:599] **Speaker 1:** and do some trigonometry.
[00:18:58:180 - 00:18:59:660] **Speaker 1:** It's quite a lot of work for us to do
[00:18:59:660 - 00:18:59:939] **Speaker 1:** that.
[00:19:01:520 - 00:19:04:459] **Speaker 1:** But ultimately what we've defined is that point C.
[00:19:05:910 - 00:19:11:270] **Speaker 1:** Moves By 0.637.
[00:19:12:170 - 00:19:15:790] **Speaker 1:** millimetres To the left.
[00:19:18:969 - 00:19:32:339] **Speaker 1:** Horizontally, And upwards By 2.432.
[00:19:33:500 - 00:19:34:280] **Speaker 1:** millimetres.
[00:19:36:270 - 00:19:36:920] **Speaker 1:** Vertically.
[00:19:45:300 - 00:19:46:719] **Speaker 1:** So this is a very simple structure.
[00:19:48:260 - 00:19:51:099] **Speaker 1:** It's really not a structure that is, is very complicated
[00:19:51:099 - 00:19:53:680] **Speaker 1:** at all, but it still requires a lot of manual
[00:19:53:680 - 00:20:00:489] **Speaker 1:** intervention to be able to Um, trace the deflective position
[00:20:00:489 - 00:20:01:430] **Speaker 1:** of that nodal point.
[00:20:03:640 - 00:20:06:040] **Speaker 1:** Now if we were to consider a more extensive, more
[00:20:06:040 - 00:20:06:979] **Speaker 1:** complicated structure.
[00:20:08:579 - 00:20:11:459] **Speaker 1:** And if I was to jump ahead to page 47
[00:20:11:459 - 00:20:12:180] **Speaker 1:** of the notes.
[00:20:13:199 - 00:20:16:359] **Speaker 1:** If we had a structure like this, well, this piece
[00:20:16:359 - 00:20:18:380] **Speaker 1:** looks just like what we used.
[00:20:19:420 - 00:20:21:609] **Speaker 1:** But if we wanted to know the tip deflection here.
[00:20:22:390 - 00:20:23:989] **Speaker 1:** We have to first of all calculate this and then
[00:20:23:989 - 00:20:26:510] **Speaker 1:** we look at the the amount by which these deflect,
[00:20:26:589 - 00:20:30:109] **Speaker 1:** but then this point's moving, so the, the, the datum
[00:20:30:109 - 00:20:31:989] **Speaker 1:** where we described the arc would change and then this
[00:20:31:989 - 00:20:34:760] **Speaker 1:** one would move and you know, you can imagine tracing
[00:20:34:880 - 00:20:38:030] **Speaker 1:** the combined deflections all the way through the structure starts
[00:20:38:030 - 00:20:39:469] **Speaker 1:** to become quite a difficult problem.
[00:20:39:550 - 00:20:41:109] **Speaker 1:** Even for a structure like this, that still isn't all
[00:20:41:109 - 00:20:41:930] **Speaker 1:** that complicated.
[00:20:42:540 - 00:20:45:150] **Speaker 1:** Following that and tracing that same process through a larger
[00:20:45:150 - 00:20:47:170] **Speaker 1:** structure like this would be really, really difficult.
[00:20:48:329 - 00:20:52:449] **Speaker 1:** So, while it is possible to apply the method we've
[00:20:52:449 - 00:20:55:790] **Speaker 1:** just done to a very simple structure with two elements,
[00:20:56:339 - 00:20:58:170] **Speaker 1:** it doesn't generalise very nicely at all.
[00:20:59:140 - 00:21:01:619] **Speaker 1:** We really want something a bit more powerful than having
[00:21:01:619 - 00:21:02:560] **Speaker 1:** to do this manually.
[00:21:05:579 - 00:21:08:079] **Speaker 1:** So there are some methods available to us.
[00:21:10:010 - 00:21:13:150] **Speaker 1:** I know you would have touched on energy methods, um,
[00:21:13:160 - 00:21:16:810] **Speaker 1:** at the, uh, end of 202 or any other course
[00:21:16:810 - 00:21:17:369] **Speaker 1:** that you've done.
[00:21:18:869 - 00:21:21:760] **Speaker 1:** Um, you know, there is, um, some.
[00:21:23:189 - 00:21:26:430] **Speaker 1:** And prior energy methods covered within the the degree.
[00:21:26:709 - 00:21:28:790] **Speaker 1:** However, I do just want to touch on those briefly
[00:21:28:790 - 00:21:32:189] **Speaker 1:** now because they they're part of the the the energy
[00:21:32:189 - 00:21:35:329] **Speaker 1:** methods do form part of the derivations that we use
[00:21:35:589 - 00:21:38:560] **Speaker 1:** to generate our assembly matrices, sorry, our stiffness matrices.
[00:21:40:079 - 00:21:44:290] **Speaker 1:** We're not, um, We're not gonna do too much of
[00:21:44:290 - 00:21:44:689] **Speaker 1:** this.
[00:21:45:010 - 00:21:46:930] **Speaker 1:** We're just gonna make sure that you're clear about how
[00:21:46:930 - 00:21:51:050] **Speaker 1:** this works because it's embedded into our, our derivations.
[00:21:53:040 - 00:21:56:880] **Speaker 1:** Now, one of the most simple working energy methods is
[00:21:56:880 - 00:21:58:560] **Speaker 1:** the work energy method for single loads.
[00:22:02:750 - 00:22:05:709] **Speaker 1:** Work, so that this is defined saying when a load
[00:22:05:709 - 00:22:07:790] **Speaker 1:** is applied from in the body deforms, work is done
[00:22:07:790 - 00:22:10:430] **Speaker 1:** on that body, um, the external forces are said to
[00:22:10:430 - 00:22:14:510] **Speaker 1:** do external work, the internal reactions to those loads do
[00:22:14:510 - 00:22:17:469] **Speaker 1:** internal work, often referred to as straining energy.
[00:22:17:550 - 00:22:19:229] **Speaker 1:** So this is like, you know, stored energy in a
[00:22:19:229 - 00:22:19:630] **Speaker 1:** spring.
[00:22:20:619 - 00:22:23:069] **Speaker 1:** And what we're looking at doing is uh continuity of
[00:22:23:069 - 00:22:26:869] **Speaker 1:** energy, so a continuity comparing the externally applied load and
[00:22:26:869 - 00:22:30:069] **Speaker 1:** the internal strain energy, and that's a way of solving
[00:22:30:069 - 00:22:30:930] **Speaker 1:** for deflections.
[00:22:32:650 - 00:22:35:189] **Speaker 1:** So first of all, if we've got this axial bar,
[00:22:35:290 - 00:22:37:290] **Speaker 1:** it starts with some initial length L and it then
[00:22:37:290 - 00:22:41:170] **Speaker 1:** extends by some distance delta, then this is the work
[00:22:41:170 - 00:22:41:689] **Speaker 1:** energy equation.
[00:22:41:770 - 00:22:45:130] **Speaker 1:** So the force increases linearly and the energy under that,
[00:22:45:209 - 00:22:47:829] **Speaker 1:** the area under that curve represents the work done.
[00:22:50:540 - 00:22:53:219] **Speaker 1:** Now, one thing that I guess is a potential point
[00:22:53:219 - 00:22:53:900] **Speaker 1:** of confusion.
[00:22:55:170 - 00:22:56:849] **Speaker 1:** is you might look at this and go, well, hang
[00:22:56:849 - 00:23:00:329] **Speaker 1:** on, I remember seeing an equation that says work is
[00:23:00:329 - 00:23:01:550] **Speaker 1:** equal to force.
[00:23:02:680 - 00:23:04:119] **Speaker 1:** Times deflection.
[00:23:05:910 - 00:23:11:010] **Speaker 1:** That that and that that isn't a valid, um, equation
[00:23:11:010 - 00:23:13:979] **Speaker 1:** for work, but in only some circumstances.
[00:23:14:290 - 00:23:16:310] **Speaker 1:** So, this equation is valid.
[00:23:17:310 - 00:23:18:949] **Speaker 1:** When you have a constant force acting.
[00:23:19:810 - 00:23:23:489] **Speaker 1:** So say for example I take this chair.
[00:23:24:339 - 00:23:26:619] **Speaker 1:** And I lift that upwards, so the, the weight of
[00:23:26:619 - 00:23:27:989] **Speaker 1:** the chair is constant irrespective.
[00:23:28:099 - 00:23:29:979] **Speaker 1:** I'm gonna do this nice slowly and statically so there's
[00:23:29:979 - 00:23:31:439] **Speaker 1:** no dynamic aspect to it.
[00:23:31:780 - 00:23:34:359] **Speaker 1:** But if you slowly and gradually lift this chair up.
[00:23:35:170 - 00:23:37:449] **Speaker 1:** The weight of the chair is the same all the
[00:23:37:449 - 00:23:39:170] **Speaker 1:** way through that range of motion.
[00:23:39:949 - 00:23:41:270] **Speaker 1:** Doesn't get heavier or lighter.
[00:23:42:180 - 00:23:42:760] **Speaker 1:** At any point.
[00:23:43:300 - 00:23:45:930] **Speaker 1:** And similarly if I take this box and I drag
[00:23:45:930 - 00:23:48:939] **Speaker 1:** it across the desk, you know, there's a certain normal
[00:23:48:939 - 00:23:51:219] **Speaker 1:** force between the box and the desk, so the coefficient
[00:23:51:219 - 00:23:53:459] **Speaker 1:** of friction, there's a normal force related to the weight
[00:23:53:459 - 00:23:55:540] **Speaker 1:** of the box and that will create a constant frictional
[00:23:55:540 - 00:23:56:060] **Speaker 1:** force.
[00:23:56:770 - 00:24:00:209] **Speaker 1:** So in those situations where the force is constant throughout
[00:24:00:209 - 00:24:01:130] **Speaker 1:** a range of motion.
[00:24:01:979 - 00:24:03:800] **Speaker 1:** In this equation is what we want.
[00:24:05:430 - 00:24:10:670] **Speaker 1:** So that would be a situation where The force.
[00:24:12:030 - 00:24:16:420] **Speaker 1:** Time to fiction And you're looking at the area that
[00:24:16:420 - 00:24:17:579] **Speaker 1:** exists upon that, so.
[00:24:20:959 - 00:24:28:449] **Speaker 1:** This equation Only valid For constant force.
[00:24:36:280 - 00:24:38:089] **Speaker 1:** In this case, because when we first go on the
[00:24:38:089 - 00:24:40:920] **Speaker 1:** bar, there's no load, and then as we gradually increase
[00:24:40:920 - 00:24:45:040] **Speaker 1:** the load, the, uh, extension will increase accordingly, so it's
[00:24:45:040 - 00:24:49:880] **Speaker 1:** actually a varying load over the deflection delta, and that's
[00:24:49:880 - 00:24:52:670] **Speaker 1:** why there's a half p delta here and it's different
[00:24:52:670 - 00:24:53:520] **Speaker 1:** to this forcing up here.
[00:24:53:560 - 00:24:56:709] **Speaker 1:** So this equation is correct in the right context, but
[00:24:56:709 - 00:24:58:050] **Speaker 1:** this is not the right context.
[00:25:01:239 - 00:25:06:939] **Speaker 1:** So This bit here Is the external work done.
[00:25:10:180 - 00:25:14:949] **Speaker 1:** And this piece here Is the internal straining energy.
[00:25:23:640 - 00:25:26:880] **Speaker 1:** And the work energy method for single loads is based
[00:25:26:880 - 00:25:31:589] **Speaker 1:** upon Equating those two and saying that we're, we're applying
[00:25:31:589 - 00:25:34:430] **Speaker 1:** this very slowly and gradually and progressively, so there's no
[00:25:34:430 - 00:25:38:500] **Speaker 1:** damping, there's no heat formation, all of the energy that's
[00:25:38:500 - 00:25:42:069] **Speaker 1:** applied externally goes into strain energy within that system.
[00:25:44:839 - 00:25:46:560] **Speaker 1:** We're going to equate the internal strain energy to the
[00:25:46:560 - 00:25:50:400] **Speaker 1:** external work done, which is uh integrate from 0 to
[00:25:50:400 - 00:25:52:800] **Speaker 1:** delta 1 of PD delta.
[00:25:53:339 - 00:25:54:640] **Speaker 1:** We integrate that, we get this answer.
[00:25:54:959 - 00:25:58:869] **Speaker 1:** Um, now for prismatic bars with constant cross sections, um,
[00:25:58:959 - 00:26:02:510] **Speaker 1:** expression for strain energy is P2L over 2AA.
[00:26:02:599 - 00:26:05:119] **Speaker 1:** So the, the square of the force, the length of
[00:26:05:119 - 00:26:08:800] **Speaker 1:** the element divided by 2 times the elastic modulus and
[00:26:08:800 - 00:26:09:260] **Speaker 1:** area.
[00:26:11:550 - 00:26:14:390] **Speaker 1:** So the work energy method for single loads can be
[00:26:14:390 - 00:26:17:819] **Speaker 1:** used to determine deformations for a structural member under very
[00:26:17:819 - 00:26:19:109] **Speaker 1:** select conditions.
[00:26:20:099 - 00:26:23:540] **Speaker 1:** The member must be loaded by a single externally, external
[00:26:23:540 - 00:26:24:400] **Speaker 1:** concentrated force.
[00:26:25:650 - 00:26:28:359] **Speaker 1:** And the corresponding displacements can only be determined.
[00:26:29:219 - 00:26:32:140] **Speaker 1:** At the location the load is applied and in the
[00:26:32:140 - 00:26:33:819] **Speaker 1:** direction in which that load is applied.
[00:26:36:869 - 00:26:39:510] **Speaker 1:** Why are we restricted to an external a single external
[00:26:39:510 - 00:26:39:969] **Speaker 1:** load?
[00:26:41:219 - 00:26:43:979] **Speaker 1:** Well, if we had multiple loads acting on there, um,
[00:26:44:060 - 00:26:48:180] **Speaker 1:** the equation above, the work done equals internal strainy is
[00:26:48:180 - 00:26:50:199] **Speaker 1:** the only equation we have available to us.
[00:26:51:969 - 00:26:54:569] **Speaker 1:** The strain energy will be a single number, so if
[00:26:54:569 - 00:26:56:650] **Speaker 1:** there was 50 elements on this, we would still get
[00:26:56:650 - 00:27:00:089] **Speaker 1:** a single number for internal strain energy, which is accumulation
[00:27:00:089 - 00:27:01:839] **Speaker 1:** of all the internal strain energy across every one of
[00:27:01:839 - 00:27:02:880] **Speaker 1:** those 50 elements.
[00:27:03:290 - 00:27:05:069] **Speaker 1:** But the key thing is one single number.
[00:27:06:650 - 00:27:08:819] **Speaker 1:** The work W that's performed by that external load is
[00:27:08:819 - 00:27:10:810] **Speaker 1:** also a single number, so we only have one equation
[00:27:10:810 - 00:27:13:459] **Speaker 1:** to us, and we can't solve use that one equation
[00:27:13:459 - 00:27:14:660] **Speaker 1:** to solve multiple variables.
[00:27:14:859 - 00:27:17:579] **Speaker 1:** So if we were to go back and apply multiple
[00:27:17:579 - 00:27:20:300] **Speaker 1:** loads to the structure, the work energy method for single
[00:27:20:300 - 00:27:22:420] **Speaker 1:** loads would break down and it wouldn't be able to
[00:27:22:420 - 00:27:23:500] **Speaker 1:** do what we needed to do.
[00:27:26:729 - 00:27:30:530] **Speaker 1:** So Let's go back And work through the same problem
[00:27:30:530 - 00:27:31:469] **Speaker 1:** we've just worked through.
[00:27:33:150 - 00:27:35:849] **Speaker 1:** That we're gonna apply the work energy method physical loads
[00:27:36:150 - 00:27:36:910] **Speaker 1:** in doing so.
[00:27:41:800 - 00:27:44:280] **Speaker 1:** So, this all looks familiar, but the key thing here
[00:27:44:280 - 00:27:46:579] **Speaker 1:** is this part here, we're using a different method now
[00:27:46:800 - 00:27:47:719] **Speaker 1:** to solve the problem.
[00:27:48:729 - 00:27:51:849] **Speaker 1:** Same problem, same setup, and we can go through this
[00:27:51:849 - 00:27:54:729] **Speaker 1:** the same step as essentially we're taking the, uh, little
[00:27:54:729 - 00:27:57:119] **Speaker 1:** free body diagram of the elements around this joint.
[00:27:57:650 - 00:27:59:329] **Speaker 1:** We work through and we get, you know, just a
[00:27:59:329 - 00:28:02:530] **Speaker 1:** reminder of the vertical and horizontal force equilibrium that we
[00:28:02:530 - 00:28:04:709] **Speaker 1:** applied and how we got the force in terms.
[00:28:07:209 - 00:28:10:510] **Speaker 1:** We can then go through and calculate.
[00:28:10:640 - 00:28:12:869] **Speaker 1:** So we've got the two forces here and here.
[00:28:13:859 - 00:28:16:819] **Speaker 1:** And then we, we've got our equation for internal strain
[00:28:16:819 - 00:28:17:119] **Speaker 1:** energy.
[00:28:17:900 - 00:28:19:550] **Speaker 1:** And then we can substitute those in and we get
[00:28:19:550 - 00:28:24:489] **Speaker 1:** this uh 31.83 joules and 89.76 joules in the two
[00:28:25:150 - 00:28:25:670] **Speaker 1:** elements.
[00:28:29:880 - 00:28:32:189] **Speaker 1:** So what we know is the total internal strain GU
[00:28:32:189 - 00:28:32:699] **Speaker 1:** total.
[00:28:33:670 - 00:28:35:609] **Speaker 1:** Is the summation of U1 and U2.
[00:28:36:170 - 00:28:40:640] **Speaker 1:** So just uh adding these two together gives us 121.59
[00:28:40:640 - 00:28:41:069] **Speaker 1:** joules.
[00:28:42:880 - 00:28:45:040] **Speaker 1:** So we know that by applying the load and inducing
[00:28:45:040 - 00:28:48:109] **Speaker 1:** these internal forces, this is the internal strain energy that
[00:28:48:109 - 00:28:49:660] **Speaker 1:** will exist within the bar.
[00:28:51:680 - 00:28:54:520] **Speaker 1:** Now we want to equate external work to internal strain
[00:28:54:520 - 00:28:54:719] **Speaker 1:** energy.
[00:28:54:920 - 00:28:58:079] **Speaker 1:** So, your total is equal to W external, and we're
[00:28:58:079 - 00:29:01:099] **Speaker 1:** gonna say we we have this number, uh, that's the
[00:29:01:219 - 00:29:04:160] **Speaker 1:** U total there, and we know that the external work
[00:29:04:160 - 00:29:06:140] **Speaker 1:** done is half P delta Y.
[00:29:06:400 - 00:29:09:479] **Speaker 1:** So, it's delta Y in the Y direction because that's
[00:29:09:479 - 00:29:11:819] **Speaker 1:** the act the direction in which this load is applied.
[00:29:14:530 - 00:29:16:150] **Speaker 1:** So what we can do is we can solve for
[00:29:16:150 - 00:29:17:390] **Speaker 1:** the vertical deflection.
[00:29:18:449 - 00:29:23:510] **Speaker 1:** Here So we're just going to take this equation above.
[00:29:27:020 - 00:29:35:900] **Speaker 1:** I'm gonna say, Rearrange And make delta Y.
[00:29:36:839 - 00:29:46:770] **Speaker 1:** The subject And that gives us 2.432 millimetres.
[00:29:48:660 - 00:29:50:319] **Speaker 1:** Now if we go back a couple of pages.
[00:29:53:040 - 00:29:54:979] **Speaker 1:** That is the same number we got here.
[00:29:56:790 - 00:29:58:430] **Speaker 1:** But we haven't had to go through a bunch of
[00:29:58:430 - 00:30:02:199] **Speaker 1:** pesky trigonometry, we didn't have that weird quadrilateral shape, we
[00:30:02:199 - 00:30:04:160] **Speaker 1:** didn't have to trace through manually and add all these
[00:30:04:160 - 00:30:04:790] **Speaker 1:** things together.
[00:30:05:160 - 00:30:06:579] **Speaker 1:** We got the answer straight away.
[00:30:10:390 - 00:30:13:329] **Speaker 1:** So that is the same result as we attained before,
[00:30:13:869 - 00:30:16:989] **Speaker 1:** but without all that awky awkward pesky trigonometry.
[00:30:19:030 - 00:30:21:760] **Speaker 1:** However, the method as it stands cannot give us the
[00:30:21:760 - 00:30:23:540] **Speaker 1:** horizontal deflection at joint C.
[00:30:23:800 - 00:30:26:160] **Speaker 1:** So the horizontal deflection, there was no load acting in
[00:30:26:160 - 00:30:28:800] **Speaker 1:** the horizontal direction, so we can't use this method to
[00:30:28:800 - 00:30:29:959] **Speaker 1:** get the horizontal deflection.
[00:30:31:310 - 00:30:33:729] **Speaker 1:** If there had been a horizontal load, we now have
[00:30:33:729 - 00:30:37:640] **Speaker 1:** multiple unknowns for a single, um, equation, and we wouldn't
[00:30:37:640 - 00:30:38:880] **Speaker 1:** have even been able to get this value.
[00:30:39:079 - 00:30:41:280] **Speaker 1:** So, you know, this is quite powerful, we got an
[00:30:41:280 - 00:30:43:500] **Speaker 1:** answer much more simply than we did previously.
[00:30:44:719 - 00:30:46:530] **Speaker 1:** But there's still a problem, you know, still not that
[00:30:46:530 - 00:30:46:880] **Speaker 1:** powerful.
[00:30:47:089 - 00:30:49:849] **Speaker 1:** It's, it's really good for very select niche cases, but
[00:30:49:849 - 00:30:50:869] **Speaker 1:** it doesn't generalise.
[00:30:55:050 - 00:30:57:130] **Speaker 1:** So we can quickly maybe just work out what that
[00:30:57:130 - 00:30:57:989] **Speaker 1:** would have looked like.
[00:30:59:339 - 00:31:02:349] **Speaker 1:** If we had applied multiple loads.
[00:31:03:270 - 00:31:04:390] **Speaker 1:** So we have a load here.
[00:31:06:160 - 00:31:07:920] **Speaker 1:** This is for a multiply loaded structure.
[00:31:12:880 - 00:31:14:250] **Speaker 1:** So suppose here we had.
[00:31:15:760 - 00:31:18:189] **Speaker 1:** 50 kilonewtons, and we're gonna call that.
[00:31:19:380 - 00:31:20:859] **Speaker 1:** Say P2.
[00:31:22:099 - 00:31:23:800] **Speaker 1:** I'm gonna put 100 kilonewtons here.
[00:31:24:770 - 00:31:25:949] **Speaker 1:** And call that P1.
[00:31:30:189 - 00:31:32:359] **Speaker 1:** So then what we would have in our equations is
[00:31:32:359 - 00:31:32:849] **Speaker 1:** that.
[00:31:34:390 - 00:31:43:250] **Speaker 1:** You total Is equal to The force In member one,
[00:31:43:489 - 00:31:46:489] **Speaker 1:** so that's not, that is neither P1 nor P2, it's
[00:31:46:489 - 00:31:49:170] **Speaker 1:** the force induced in member one as a result of
[00:31:49:170 - 00:31:50:109] **Speaker 1:** these applied loads.
[00:31:52:310 - 00:31:53:869] **Speaker 1:** Squad times L1.
[00:31:54:839 - 00:31:56:640] **Speaker 1:** Over 2A1E1.
[00:31:58:109 - 00:32:00:930] **Speaker 1:** Plus F2 squared.
[00:32:01:829 - 00:32:05:869] **Speaker 1:** L2 over 2, A2, E2.
[00:32:07:890 - 00:32:10:489] **Speaker 1:** And that would then also be equal to 1/2.
[00:32:12:709 - 00:32:17:160] **Speaker 1:** P1 Delta Y + 1/2.
[00:32:18:310 - 00:32:20:540] **Speaker 1:** P2 delta X.
[00:32:20:790 - 00:32:23:180] **Speaker 1:** So it would be the, the work done in the
[00:32:23:180 - 00:32:26:270] **Speaker 1:** horizontal direction by the slide here and then the work
[00:32:26:270 - 00:32:28:630] **Speaker 1:** done in the vertical direction by the slide here.
[00:32:30:969 - 00:32:35:439] **Speaker 1:** So this Let me just define this here as W.
[00:32:36:810 - 00:32:40:800] **Speaker 1:** External And then we have an equation where you total,
[00:32:42:140 - 00:32:43:609] **Speaker 1:** Equals W external.
[00:32:45:339 - 00:32:46:150] **Speaker 1:** That's the equation.
[00:32:46:189 - 00:32:47:560] **Speaker 1:** We just want to put these two together.
[00:32:49:310 - 00:32:52:469] **Speaker 1:** Now, we can work out what F1 and F2 are.
[00:32:52:550 - 00:32:54:790] **Speaker 1:** We just use the same method we did before, except
[00:32:54:790 - 00:32:55:859] **Speaker 1:** now there's some additional forces.
[00:32:55:910 - 00:32:58:489] **Speaker 1:** So we do know everything in the top equation here.
[00:32:59:920 - 00:33:02:800] **Speaker 1:** But we don't know either delta X or delta Y.
[00:33:05:189 - 00:33:14:650] **Speaker 1:** And The key thing is If we apply Multiple loads,
[00:33:14:900 - 00:33:16:260] **Speaker 1:** multiple external loads.
[00:33:22:959 - 00:33:26:849] **Speaker 1:** We have Multiple unknowns.
[00:33:34:459 - 00:33:43:390] **Speaker 1:** A single equation And the method fails.
[00:33:57:219 - 00:33:58:560] **Speaker 1:** So what this is really powerful.
[00:33:59:469 - 00:34:02:680] **Speaker 1:** And the, the initial value we got here was much,
[00:34:02:699 - 00:34:04:739] **Speaker 1:** much easier than the previous way we solved this.
[00:34:05:219 - 00:34:07:500] **Speaker 1:** It's still really limited and we need another step.
[00:34:07:569 - 00:34:09:199] **Speaker 1:** We need something to add on to this.
[00:34:10:489 - 00:34:14:648] **Speaker 1:** Which generalises the method and enables it to be a
[00:34:14:648 - 00:34:15:628] **Speaker 1:** little bit more powerful.
[00:34:18:049 - 00:34:20:718] **Speaker 1:** And that method is the method of virtual work.
[00:34:20:857 - 00:34:24:419] **Speaker 1:** Now, It's quite a complicated thing to get your head
[00:34:24:419 - 00:34:24:679] **Speaker 1:** around.
[00:34:25:219 - 00:34:27:939] **Speaker 1:** Um, the next page is quite a lot of information
[00:34:27:939 - 00:34:28:280] **Speaker 1:** there.
[00:34:28:860 - 00:34:31:850] **Speaker 1:** Um, I understand initially when we go into this that
[00:34:31:850 - 00:34:34:300] **Speaker 1:** it might sound kind of crazy and the method probably
[00:34:34:300 - 00:34:35:959] **Speaker 1:** looks like it's bordering on witchcraft.
[00:34:36:928 - 00:34:38:729] **Speaker 1:** But it will get us there, and it's actually really
[00:34:38:729 - 00:34:39:188] **Speaker 1:** powerful.
[00:34:43:110 - 00:34:45:770] **Speaker 1:** So, the method of virtual work is an important extension
[00:34:45:770 - 00:34:48:908] **Speaker 1:** of the work energy method for single loads, and what
[00:34:48:908 - 00:34:50:750] **Speaker 1:** it does is it allows us to solve for deflections
[00:34:50:750 - 00:34:55:110] **Speaker 1:** and multiply loaded instructions and at locations other than that
[00:34:55:110 - 00:34:56:750] **Speaker 1:** which the load is applied.
[00:34:58:040 - 00:35:00:500] **Speaker 1:** Now technically the virtual principle of virtual work states.
[00:35:01:169 - 00:35:04:889] **Speaker 1:** If a deformable body is in equilibrium under a virtual
[00:35:04:889 - 00:35:08:209] **Speaker 1:** force system and remains in equilibrium while it is subjected
[00:35:08:209 - 00:35:11:530] **Speaker 1:** to a set of small compatible deflections, then the external
[00:35:11:530 - 00:35:15:770] **Speaker 1:** virtual work done by the virtual external forces acting through
[00:35:15:770 - 00:35:19:050] **Speaker 1:** the real external displacements or rotations is equal to the
[00:35:19:050 - 00:35:22:850] **Speaker 1:** virtual internal work done by the virtual internal forces acting
[00:35:22:850 - 00:35:25:350] **Speaker 1:** through the real internal displacements or rotations.
[00:35:26:510 - 00:35:27:979] **Speaker 1:** So a very quick show of hands as to who
[00:35:27:979 - 00:35:28:610] **Speaker 1:** understood that.
[00:35:32:679 - 00:35:34:199] **Speaker 1:** Whose brain hurt when they heard that?
[00:35:35:290 - 00:35:37:290] **Speaker 1:** Yeah, I understand.
[00:35:38:250 - 00:35:39:330] **Speaker 1:** So what does it actually mean?
[00:35:39:540 - 00:35:40:729] **Speaker 1:** It's a whole lot.
[00:35:40:810 - 00:35:44:290] **Speaker 1:** So procedurally we can go through and we can.
[00:35:45:290 - 00:35:47:379] **Speaker 1:** If the structure has a single load and we want
[00:35:47:379 - 00:35:49:340] **Speaker 1:** the deflections at a different location or we have a
[00:35:49:340 - 00:35:51:260] **Speaker 1:** multiply loaded structure, we can apply this method.
[00:35:52:449 - 00:35:54:820] **Speaker 1:** What we do is we use the principle of superposition
[00:35:55:199 - 00:35:59:270] **Speaker 1:** to independently consider real loads and virtual loads and how
[00:35:59:270 - 00:36:00:959] **Speaker 1:** each load is developed within the structure.
[00:36:01:199 - 00:36:04:239] **Speaker 1:** So the principle of superposition says essentially we'll consider one
[00:36:04:239 - 00:36:05:889] **Speaker 1:** thing while ignoring the others.
[00:36:06:520 - 00:36:08:780] **Speaker 1:** So we'll consider A and ignore B.
[00:36:09:449 - 00:36:10:969] **Speaker 1:** And then we'll switch around and we'll look at B
[00:36:10:969 - 00:36:14:010] **Speaker 1:** while ignoring A and just work through and consider those
[00:36:14:010 - 00:36:14:409] **Speaker 1:** independently.
[00:36:16:719 - 00:36:18:879] **Speaker 1:** We typically define the virtual external load to have a
[00:36:18:879 - 00:36:19:909] **Speaker 1:** value of sort of 1.
[00:36:20:820 - 00:36:24:780] **Speaker 1:** 1.0, so either kill Newtons or Newtons, um, that's just
[00:36:24:780 - 00:36:25:790] **Speaker 1:** to make life easier.
[00:36:26:219 - 00:36:27:780] **Speaker 1:** There's nothing saying it has to be 1.
[00:36:28:260 - 00:36:30:419] **Speaker 1:** If we made it 3, we'd just have to divide
[00:36:30:419 - 00:36:33:360] **Speaker 1:** by 3 later, so it's just to make life easier.
[00:36:36:090 - 00:36:38:689] **Speaker 1:** So when we use to analyse the trust, the process
[00:36:38:689 - 00:36:39:669] **Speaker 1:** has several steps.
[00:36:40:250 - 00:36:44:330] **Speaker 1:** First, we take the real external loads applied only, ignoring
[00:36:44:330 - 00:36:46:929] **Speaker 1:** the virtual load for now, and work out the internal
[00:36:46:929 - 00:36:48:629] **Speaker 1:** forces developed within each member.
[00:36:49:620 - 00:36:53:120] **Speaker 1:** Then we ignore the real external loads and only consider
[00:36:53:120 - 00:36:55:090] **Speaker 1:** the chosen virtual load applied to the structure.
[00:36:55:860 - 00:36:57:949] **Speaker 1:** Uh, the virtual load is applied at the, at the
[00:36:57:949 - 00:37:00:949] **Speaker 1:** point in which you wish to know the deflection, and
[00:37:00:949 - 00:37:03:429] **Speaker 1:** the virtual load acts in the direction in which you
[00:37:03:429 - 00:37:04:709] **Speaker 1:** want to know the deflection.
[00:37:07:570 - 00:37:09:899] **Speaker 1:** Uh, we apply the principle of virtual work and equate
[00:37:09:899 - 00:37:12:209] **Speaker 1:** the virtual internal work, the work done by the, uh,
[00:37:12:300 - 00:37:16:419] **Speaker 1:** internal virtual forces moving through real displacements to the virtual
[00:37:16:419 - 00:37:19:979] **Speaker 1:** external work, the work done by the virtual external forces
[00:37:19:979 - 00:37:21:620] **Speaker 1:** moving through the real external displacement.
[00:37:22:909 - 00:37:26:830] **Speaker 1:** Um, this, and I totally understand if this is just
[00:37:26:830 - 00:37:29:330] **Speaker 1:** sounding like I'm standing up here rambling.
[00:37:29:830 - 00:37:31:540] **Speaker 1:** We're gonna work through an example which will pull all
[00:37:31:540 - 00:37:33:989] **Speaker 1:** of this together and you understand, it's much less scary
[00:37:33:989 - 00:37:35:050] **Speaker 1:** when you actually see it in practise.
[00:37:36:939 - 00:37:39:199] **Speaker 1:** So the princess principle can be expressed like this, the
[00:37:39:199 - 00:37:42:699] **Speaker 1:** virtual external loads times the real external displacements is equal
[00:37:42:699 - 00:37:45:500] **Speaker 1:** to the sum of the virtual internal forces times the
[00:37:45:500 - 00:37:46:939] **Speaker 1:** real internal displacements.
[00:37:49:070 - 00:37:51:389] **Speaker 1:** Now before we work through an example, we just need
[00:37:51:389 - 00:37:53:149] **Speaker 1:** to define some terminology.
[00:37:57:340 - 00:38:01:169] **Speaker 1:** Now for a compound truss with homogeneous constant elastic modulus
[00:38:01:550 - 00:38:06:510] **Speaker 1:** and prismatic, constant cross-section members, the equation can be written
[00:38:06:669 - 00:38:09:820] **Speaker 1:** mathematically like this, so that hopefully is already starting to
[00:38:09:820 - 00:38:10:929] **Speaker 1:** look a little bit less scary.
[00:38:12:780 - 00:38:16:300] **Speaker 1:** The number one is the virtual external load acting on
[00:38:16:300 - 00:38:18:100] **Speaker 1:** the location to obtain deflection.
[00:38:18:979 - 00:38:20:979] **Speaker 1:** Delta, and in the direction in which we want to
[00:38:20:979 - 00:38:21:540] **Speaker 1:** solve the deflection.
[00:38:21:620 - 00:38:24:290] **Speaker 1:** So we, we pick a node, we say that's the
[00:38:24:290 - 00:38:26:260] **Speaker 1:** location we want to know the deflection, and we put
[00:38:26:260 - 00:38:28:929] **Speaker 1:** the the virtual load there and we uh oriented in
[00:38:28:929 - 00:38:30:979] **Speaker 1:** the direction in which we want to know displacements.
[00:38:32:129 - 00:38:33:879] **Speaker 1:** It is a value of 1, as I mentioned, it
[00:38:33:879 - 00:38:35:850] **Speaker 1:** doesn't have to be one, but we'll just end up
[00:38:35:850 - 00:38:37:350] **Speaker 1:** dividing through by it if it's not.
[00:38:38:899 - 00:38:41:330] **Speaker 1:** Delta is the real joint displacement caused by the real
[00:38:41:330 - 00:38:42:370] **Speaker 1:** loads that act on the truss.
[00:38:42:459 - 00:38:43:739] **Speaker 1:** That's the thing we actually want to know.
[00:38:44:060 - 00:38:45:139] **Speaker 1:** Delta is our target here.
[00:38:45:330 - 00:38:46:439] **Speaker 1:** That's what we're doing this for.
[00:38:47:870 - 00:38:52:699] **Speaker 1:** FI or superscript I is the virtual internal force created
[00:38:52:699 - 00:38:55:830] **Speaker 1:** within the trust member I when the load is, the
[00:38:55:830 - 00:38:58:590] **Speaker 1:** truss is loaded with only the single external virtual load,
[00:38:58:790 - 00:39:00:860] **Speaker 1:** ignoring the real external loads acting on the truss.
[00:39:00:909 - 00:39:02:989] **Speaker 1:** So the key thing in this case, the lowercase f
[00:39:02:989 - 00:39:06:149] **Speaker 1:** is is the internal force that exists from the virtual
[00:39:06:149 - 00:39:06:590] **Speaker 1:** load.
[00:39:07:899 - 00:39:11:300] **Speaker 1:** The uppercase F is the real internal forces created when
[00:39:11:300 - 00:39:14:860] **Speaker 1:** the load is, um, with the real loads, ignoring the
[00:39:14:860 - 00:39:15:379] **Speaker 1:** virtual loads.
[00:39:15:459 - 00:39:17:139] **Speaker 1:** So this is the principle of superposition.
[00:39:17:179 - 00:39:19:870] **Speaker 1:** We initially considered virtual loads and ignore the real loads,
[00:39:20:179 - 00:39:21:500] **Speaker 1:** then we look at the real loads and ignore the
[00:39:21:500 - 00:39:25:030] **Speaker 1:** virtual loads, and then we just have these length cross-section
[00:39:25:030 - 00:39:27:600] **Speaker 1:** and elastic modulus, the same way we always have.
[00:39:29:979 - 00:39:31:580] **Speaker 1:** Now, this is where the rubber hits the road.
[00:39:31:659 - 00:39:35:439] **Speaker 1:** This is where, um, hopefully, everything starts to come together.
[00:39:40:860 - 00:39:43:020] **Speaker 1:** So we have this structure, same structure we've looked at
[00:39:43:020 - 00:39:43:879] **Speaker 1:** it a few times now.
[00:39:45:300 - 00:39:48:000] **Speaker 1:** Same external load that we've looked at, we're solving the
[00:39:48:000 - 00:39:48:520] **Speaker 1:** same problem.
[00:39:49:820 - 00:39:51:280] **Speaker 1:** Now, initially what we're gonna do.
[00:39:53:090 - 00:39:56:290] **Speaker 1:** we assume we want to know the horizontal deflection.
[00:39:57:739 - 00:39:58:459] **Speaker 1:** At Pin joints.
[00:40:00:389 - 00:40:05:449] **Speaker 1:** So we've now ignore the real externally, Applied loads, so
[00:40:05:449 - 00:40:07:610] **Speaker 1:** we're gonna ignore this initially, just put that to the
[00:40:07:610 - 00:40:08:669] **Speaker 1:** side, pretend it doesn't exist.
[00:40:10:830 - 00:40:12:510] **Speaker 1:** And then what we're going to do is then apply
[00:40:12:510 - 00:40:15:870] **Speaker 1:** a virtual unit load in the horizontal direction at sea.
[00:40:16:750 - 00:40:18:669] **Speaker 1:** And work out what the internal forces are here.
[00:40:18:750 - 00:40:21:030] **Speaker 1:** So the uppercase are the real forces that exist from
[00:40:21:030 - 00:40:24:189] **Speaker 1:** the real, real forces within the members that exist from
[00:40:24:189 - 00:40:25:120] **Speaker 1:** this real load.
[00:40:26:419 - 00:40:28:159] **Speaker 1:** Now what we're gonna do is apply this virtual load,
[00:40:28:489 - 00:40:30:979] **Speaker 1:** pretending this doesn't exist, and we're gonna work out what
[00:40:30:979 - 00:40:32:439] **Speaker 1:** the internal forces would be.
[00:40:33:820 - 00:40:34:929] **Speaker 1:** That result from that.
[00:40:35:469 - 00:40:37:350] **Speaker 1:** Now, horizontal equilibrium.
[00:40:38:580 - 00:40:41:300] **Speaker 1:** Um, or vertical force equilibrium says that there's a, a,
[00:40:41:879 - 00:40:46:699] **Speaker 1:** a vertical component of this force, which is F2 cos
[00:40:46:699 - 00:40:50:620] **Speaker 1:** or sin 45, doesn't actually matter because it's 45, it's
[00:40:50:620 - 00:40:52:800] **Speaker 1:** the, the vertical component of this force.
[00:40:53:820 - 00:40:55:320] **Speaker 1:** That's the only thing that acts vertically.
[00:40:56:239 - 00:40:58:239] **Speaker 1:** So that tells us there's no, if there was, if
[00:40:58:239 - 00:41:00:679] **Speaker 1:** that force was non-zero, there would be nothing to balance
[00:41:00:679 - 00:41:02:639] **Speaker 1:** out the vertical component, so that must be zero.
[00:41:03:850 - 00:41:05:479] **Speaker 1:** Then we look at the horizontal component.
[00:41:06:949 - 00:41:09:739] **Speaker 1:** And we have one Newton to the right, we have
[00:41:10:030 - 00:41:12:350] **Speaker 1:** F1 to the left, that tells us that the internal
[00:41:12:350 - 00:41:14:070] **Speaker 1:** force is one Newton.
[00:41:16:139 - 00:41:17:139] **Speaker 1:** Then we can jump in and we can do this
[00:41:17:139 - 00:41:17:679] **Speaker 1:** little table.
[00:41:20:050 - 00:41:28:389] **Speaker 1:** So we can go through here And We can, um,
[00:41:28:679 - 00:41:32:100] **Speaker 1:** we have the member length, cross sectional area, elastic modulus.
[00:41:32:760 - 00:41:35:570] **Speaker 1:** The real internal force, so that was from the equilibrium
[00:41:35:570 - 00:41:37:000] **Speaker 1:** we did up here, so that was on the real
[00:41:37:000 - 00:41:39:959] **Speaker 1:** so these equations matched this diagram.
[00:41:40:159 - 00:41:42:520] **Speaker 1:** I might actually just put a a line through there
[00:41:42:520 - 00:41:43:760] **Speaker 1:** to make that extra clear.
[00:41:44:840 - 00:41:47:510] **Speaker 1:** These calculations refer to this, which is the real load,
[00:41:47:840 - 00:41:49:840] **Speaker 1:** and then these calculations refer to this, which is the
[00:41:49:840 - 00:41:50:479] **Speaker 1:** virtual load.
[00:41:50:719 - 00:41:53:840] **Speaker 1:** So, these numbers here come down in form.
[00:41:54:820 - 00:41:58:100] **Speaker 1:** This column, and then these numbers come down and form
[00:41:58:100 - 00:41:58:699] **Speaker 1:** this column.
[00:42:01:479 - 00:42:03:889] **Speaker 1:** And then what we do is we calculate this here.
[00:42:03:969 - 00:42:07:090] **Speaker 1:** So this is the, the numbers, the, the terms that
[00:42:07:090 - 00:42:11:439] **Speaker 1:** were defined in This equation here.
[00:42:11:760 - 00:42:14:939] **Speaker 1:** So we go through across each element, we have our
[00:42:15:260 - 00:42:19:280] **Speaker 1:** virtual internal force times our real internal force times the
[00:42:19:280 - 00:42:23:399] **Speaker 1:** length divided by area and elastic modulus, and then we
[00:42:23:399 - 00:42:25:020] **Speaker 1:** get this deflection here.
[00:42:25:600 - 00:42:28:560] **Speaker 1:** So this is, this is, sorry, it's not a deflection
[00:42:28:560 - 00:42:28:939] **Speaker 1:** yet.
[00:42:29:350 - 00:42:30:489] **Speaker 1:** This is this value.
[00:42:30:760 - 00:42:32:459] **Speaker 1:** We sum that up across all elements.
[00:42:33:000 - 00:42:37:919] **Speaker 1:** Now, in this particular instance, because there's the zero load
[00:42:37:919 - 00:42:42:000] **Speaker 1:** introduced within force member 2 from this external load that
[00:42:42:000 - 00:42:45:399] **Speaker 1:** happens to be zero, we sum that up and get
[00:42:45:399 - 00:42:46:739] **Speaker 1:** this value here.
[00:42:48:639 - 00:42:50:580] **Speaker 1:** And that there is.
[00:42:51:729 - 00:42:57:989] **Speaker 1:** What comes down Into our equation here Because we used
[00:42:57:989 - 00:42:59:879] **Speaker 1:** the value of a unit value one.
[00:43:00:699 - 00:43:02:979] **Speaker 1:** We have one here and then we can rearrange this
[00:43:02:979 - 00:43:03:340] **Speaker 1:** equation.
[00:43:03:459 - 00:43:06:760] **Speaker 1:** So delta is equal to this divided by the magnitude
[00:43:06:760 - 00:43:09:739] **Speaker 1:** of the virtual load, but because it's one, we don't
[00:43:09:739 - 00:43:11:939] **Speaker 1:** have to deal with it, but if that was if
[00:43:11:939 - 00:43:14:379] **Speaker 1:** we chosen a value that wasn't one, we didn't have
[00:43:14:379 - 00:43:15:439] **Speaker 1:** to divide through here.
[00:43:16:540 - 00:43:21:889] **Speaker 1:** And that tells us that the Horizontal displacement is -0.636.
[00:43:23:580 - 00:43:26:560] **Speaker 1:** So, that's how that works.
[00:43:28:510 - 00:43:30:810] **Speaker 1:** That's the answer that we got previously.
[00:43:33:270 - 00:43:36:070] **Speaker 1:** Now we're gonna rework the problem, and this time we're
[00:43:36:070 - 00:43:38:110] **Speaker 1:** gonna say what if we wanted the vertical displacement instead
[00:43:38:110 - 00:43:38:889] **Speaker 1:** of the horizontal.
[00:43:42:570 - 00:43:44:889] **Speaker 1:** So what if we wanted the vertical, like we did
[00:43:44:889 - 00:43:47:689] **Speaker 1:** earlier, so we now wish to define the vertical deflection
[00:43:47:689 - 00:43:48:350] **Speaker 1:** at point C.
[00:43:49:350 - 00:43:52:330] **Speaker 1:** So we're gonna, the, the first step in that process,
[00:43:52:909 - 00:43:53:689] **Speaker 1:** this piece here.
[00:43:54:409 - 00:43:56:050] **Speaker 1:** The real loads haven't changed.
[00:43:57:159 - 00:43:59:020] **Speaker 1:** So this step doesn't need to be repeated.
[00:43:59:260 - 00:44:00:080] **Speaker 1:** We've already done that.
[00:44:00:360 - 00:44:03:399] **Speaker 1:** It's valid, um, for all virtual loads.
[00:44:04:270 - 00:44:05:840] **Speaker 1:** But we're gonna redo the virtual load part.
[00:44:05:919 - 00:44:09:800] **Speaker 1:** So instead of the virtual load being horizontal here.
[00:44:10:639 - 00:44:11:959] **Speaker 1:** We're now gonna make it vertical.
[00:44:13:760 - 00:44:17:800] **Speaker 1:** And when you trace that through, we have This looks
[00:44:17:800 - 00:44:21:120] **Speaker 1:** very much like the previous uh process we get these
[00:44:21:120 - 00:44:21:629] **Speaker 1:** two values here.
[00:44:21:679 - 00:44:26:280] **Speaker 1:** So it's a 1.41 Newton tension load in F2 and
[00:44:26:280 - 00:44:29:879] **Speaker 1:** a negative1 is compressive load in number one.
[00:44:32:840 - 00:44:34:879] **Speaker 1:** So when we compare to the previous page, we've got
[00:44:34:879 - 00:44:35:739] **Speaker 1:** a new table.
[00:44:37:280 - 00:44:39:600] **Speaker 1:** But the lengths don't change, the areas don't change, the
[00:44:39:600 - 00:44:43:040] **Speaker 1:** elastic modulus doesn't change, and the internal forces within each
[00:44:43:040 - 00:44:46:040] **Speaker 1:** member as a result of the real external loads doesn't
[00:44:46:040 - 00:44:46:659] **Speaker 1:** change either.
[00:44:50:790 - 00:44:52:469] **Speaker 1:** This is the only new column.
[00:44:56:830 - 00:44:58:729] **Speaker 1:** So we can recycle and reuse.
[00:45:00:360 - 00:45:02:340] **Speaker 1:** I guess the the final column is also different as
[00:45:02:340 - 00:45:04:899] **Speaker 1:** a result of that, but that's the new piece, only
[00:45:04:899 - 00:45:06:320] **Speaker 1:** the virtual load that changes.
[00:45:08:070 - 00:45:10:149] **Speaker 1:** And we go through and we have our lowercase f.
[00:45:10:219 - 00:45:13:979] **Speaker 1:** we've got our So that's the virtual load and each
[00:45:13:979 - 00:45:16:560] **Speaker 1:** member times the real load and each member resulting from
[00:45:16:560 - 00:45:20:409] **Speaker 1:** the real external load, the length, the elastic modulus and
[00:45:20:409 - 00:45:23:020] **Speaker 1:** the cross-sectional area, and then we got some different numbers
[00:45:23:020 - 00:45:25:929] **Speaker 1:** there and when we sum that up, we get this
[00:45:25:929 - 00:45:26:520] **Speaker 1:** number here.
[00:45:28:570 - 00:45:32:169] **Speaker 1:** Then we translate it back to our um virtual work
[00:45:32:169 - 00:45:32:689] **Speaker 1:** equation.
[00:45:34:850 - 00:45:37:340] **Speaker 1:** This, everything on the right-hand side is the summation that's
[00:45:37:340 - 00:45:38:320] **Speaker 1:** in this box here.
[00:45:38:780 - 00:45:41:899] **Speaker 1:** We have 1 times delta, we divide through, and that
[00:45:41:899 - 00:45:45:669] **Speaker 1:** tells us that the vertical deflection is 2.432 millimetres.
[00:45:50:330 - 00:45:54:639] **Speaker 1:** So Um, what we have now is with this addition
[00:45:54:639 - 00:45:56:179] **Speaker 1:** of the virtual load.
[00:45:57:179 - 00:45:59:100] **Speaker 1:** We've now extended the method.
[00:45:59:379 - 00:46:03:639] **Speaker 1:** It's now applicable and it can solve members with multiple
[00:46:03:979 - 00:46:05:340] **Speaker 1:** loads externally applied.
[00:46:06:060 - 00:46:08:540] **Speaker 1:** It can solve, uh, any point in the structure.
[00:46:08:580 - 00:46:10:179] **Speaker 1:** It doesn't have to be where the load is applied
[00:46:10:300 - 00:46:11:590] **Speaker 1:** and it doesn't have to be in the direction in
[00:46:11:590 - 00:46:12:739] **Speaker 1:** which the load is applied.
[00:46:13:260 - 00:46:18:300] **Speaker 1:** So this extra concept is massively extended the capability of
[00:46:18:300 - 00:46:19:439] **Speaker 1:** this of this concept.
[00:46:21:760 - 00:46:24:639] **Speaker 1:** So the simple example hopefully give you some confidence in
[00:46:24:639 - 00:46:27:239] **Speaker 1:** the theory behind the principle of virtual displacements and how
[00:46:27:239 - 00:46:27:979] **Speaker 1:** they're applied.
[00:46:28:899 - 00:46:30:959] **Speaker 1:** Um, the simple structure is statically determinate.
[00:46:32:729 - 00:46:36:889] **Speaker 1:** So we can easily solve for virtual forces, um, real
[00:46:36:889 - 00:46:38:409] **Speaker 1:** virtual forces within each member.
[00:46:38:590 - 00:46:40:590] **Speaker 1:** However, if we want to apply to a more complex
[00:46:40:760 - 00:46:44:129] **Speaker 1:** statically and determinate structures, we need to develop a better
[00:46:44:129 - 00:46:46:870] **Speaker 1:** method because with this first step where we work out
[00:46:47:530 - 00:46:53:610] **Speaker 1:** internal forces from The real light applied loads.
[00:46:53:879 - 00:46:57:360] **Speaker 1:** If this was a statically determined system which had overconstraint
[00:46:57:360 - 00:46:59:800] **Speaker 1:** and additional members in it, this first step might be
[00:46:59:800 - 00:47:00:979] **Speaker 1:** much, much harder as well.
[00:47:04:919 - 00:47:07:510] **Speaker 1:** So the principle of virtual displacements is really key to
[00:47:07:510 - 00:47:11:040] **Speaker 1:** our derivation of stiffness matrices, that's why I wanted to
[00:47:11:040 - 00:47:13:520] **Speaker 1:** touch this, touch on this now.
[00:47:14:409 - 00:47:15:699] **Speaker 1:** I also want to just think about this in a
[00:47:15:699 - 00:47:16:189] **Speaker 1:** different way.
[00:47:16:300 - 00:47:18:729] **Speaker 1:** So, like, what is the concept of a, a virtual
[00:47:18:729 - 00:47:19:419] **Speaker 1:** displacement?
[00:47:21:189 - 00:47:22:969] **Speaker 1:** It's a pretty abstract concept.
[00:47:24:780 - 00:47:26:250] **Speaker 1:** So I want to just touch on that a little
[00:47:26:250 - 00:47:26:760] **Speaker 1:** bit more.
[00:47:32:360 - 00:47:34:280] **Speaker 1:** So suppose we have a slightly larger structure.
[00:47:38:560 - 00:47:39:739] **Speaker 1:** Going to draw it like this.
[00:48:00:149 - 00:48:02:449] **Speaker 1:** And we're gonna say put a downwards force of 200
[00:48:02:449 - 00:48:03:419] **Speaker 1:** kilonewtons.
[00:48:04:620 - 00:48:07:260] **Speaker 1:** And we're all going on a horizontal force of 50
[00:48:07:260 - 00:48:08:100] **Speaker 1:** kil Newtons.
[00:48:15:389 - 00:48:17:669] **Speaker 1:** Now, the way I think about this is, is thinking
[00:48:17:669 - 00:48:20:010] **Speaker 1:** of virtual forces a little bit like weighting factors.
[00:48:20:429 - 00:48:22:870] **Speaker 1:** We apply this load at the tip and every member
[00:48:22:870 - 00:48:25:229] **Speaker 1:** in that structure is going to carry load.
[00:48:26:399 - 00:48:27:959] **Speaker 1:** It's gonna, as a result of carrying load, it's gonna
[00:48:27:959 - 00:48:30:090] **Speaker 1:** deflect and it's gonna have some internal strain energy.
[00:48:31:989 - 00:48:34:149] **Speaker 1:** And the tip deflection here, the very tip of the
[00:48:34:149 - 00:48:37:840] **Speaker 1:** structure, the internal strain energy in every one of those
[00:48:37:840 - 00:48:39:469] **Speaker 1:** members is gonna contribute to that deflection.
[00:48:41:000 - 00:48:43:679] **Speaker 1:** However, if we wanted to instead know the deflection here
[00:48:43:679 - 00:48:44:379] **Speaker 1:** at this node.
[00:48:46:239 - 00:48:49:399] **Speaker 1:** We might put a virtual load of one Newton here.
[00:48:51:830 - 00:48:54:340] **Speaker 1:** But we wouldn't expect the strain energy that exists within
[00:48:54:340 - 00:48:58:280] **Speaker 1:** this member to contribute to how much this node deflects
[00:48:58:939 - 00:49:01:100] **Speaker 1:** because it's not in the the path to the support
[00:49:01:100 - 00:49:01:520] **Speaker 1:** point.
[00:49:02:310 - 00:49:04:530] **Speaker 1:** So we would actually at this point, we'd only expect
[00:49:05:679 - 00:49:11:179] **Speaker 1:** The strain energy In this element and in this element.
[00:49:12:669 - 00:49:15:399] **Speaker 1:** To contribute to how much the snow deflects, and the
[00:49:15:399 - 00:49:18:459] **Speaker 1:** strain energy and these elements shouldn't really contribute to that.
[00:49:19:889 - 00:49:21:449] **Speaker 1:** So that's the way I think about this, is that
[00:49:21:449 - 00:49:23:709] **Speaker 1:** if we go back to our table above.
[00:49:25:139 - 00:49:27:080] **Speaker 1:** And particularly the one on the previous page.
[00:49:27:929 - 00:49:29:810] **Speaker 1:** You can see there's a zero weighting in here, so
[00:49:29:810 - 00:49:33:179] **Speaker 1:** you can basically say, consider, I consider this almost like
[00:49:33:179 - 00:49:36:540] **Speaker 1:** a, a column of weighting factors, like how much weight,
[00:49:36:620 - 00:49:40:179] **Speaker 1:** how much influence should we add to the strain energy
[00:49:40:179 - 00:49:42:949] **Speaker 1:** which exists within this particular element in terms of our
[00:49:42:949 - 00:49:43:860] **Speaker 1:** overall deflection.
[00:49:44:850 - 00:49:46:439] **Speaker 1:** And in this situation, if we were looking for the
[00:49:46:439 - 00:49:49:260] **Speaker 1:** vertical deflection at this node, we would be weighting the
[00:49:49:260 - 00:49:52:020] **Speaker 1:** strain energy that comes in from these two elements, but
[00:49:52:020 - 00:49:54:409] **Speaker 1:** we wouldn't be drawing a weighting from these elements.
[00:49:54:810 - 00:49:56:500] **Speaker 1:** So that's conceptually how I think of it.
[00:49:56:580 - 00:49:58:780] **Speaker 1:** I think it, it makes more sense than what's otherwise
[00:49:58:780 - 00:49:59:899] **Speaker 1:** quite an abstract concept.
[00:50:01:399 - 00:50:03:239] **Speaker 1:** So we'll talk about that more next week.
[00:50:03:320 - 00:50:06:199] **Speaker 1:** It's a key part of our derivation, um, and we'll,
[00:50:06:280 - 00:50:09:840] **Speaker 1:** we'll move on into assembling larger structures next week.
[00:50:10:159 - 00:50:12:520] **Speaker 1:** So thank you all for coming along and have a
[00:50:12:520 - 00:50:13:139] **Speaker 1:** good weekend.
[00:50:32:659 - 00:50:37:659] **Speaker 0:** OK, does the, uh, virtual still give you a linear
[00:50:37:659 - 00:50:38:270] **Speaker 0:** approximation.
[00:50:39:250 - 00:50:44:439] **Speaker 0:** It does and it does not give you the, even
[00:50:45:399 - 00:50:54:860] **Speaker 0:** the full system um and you can read the pictures,
[00:50:56:129 - 00:50:59:750] **Speaker 0:** it's gonna be like it's different.
[00:50:59:760 - 00:51:04:820] **Speaker 0:** So, um, because it's such small elements like.
[00:51:10:260 - 00:51:14:379] **Speaker 0:** Yeah, maybe it's like most of the things we do
[00:51:14:379 - 00:51:16:179] **Speaker 0:** in engineering we don't see the client.
[00:51:18:270 - 00:51:24:709] **Speaker 0:** But normally, um, and so if you're doing you make
[00:51:24:709 - 00:51:29:219] **Speaker 0:** something, um, on less than you should appearance, then you
[00:51:29:219 - 00:51:31:010] **Speaker 0:** can use, uh, so.
[00:51:33:760 - 00:51:35:479] **Speaker 0:** None of what we do here actually solves that all,
[00:51:36:560 - 00:51:39:850] **Speaker 0:** every, every method that um through that.
[00:51:45:550 - 00:51:57:139] **Speaker 0:** I guess I Yeah.
[00:52:01:709 - 00:52:02:870] **Speaker 0:** No, it also it's in your system, so.
[00:52:06:679 - 00:52:07:199] **Speaker 0:** Yeah.
[00:52:12:949 - 00:52:13:639] **Speaker 0:** um, which is true.
[00:52:15:760 - 00:52:36:729] **Speaker 0:** Yeah That OK, Oh Thank you.
[00:52:39:239 - 00:52:39:750] **Speaker 0:** OK.
[00:52:44:409 - 00:52:51:790] **Speaker 0:** I Someone of that as well.
[00:53:27:629 - 00:53:46:870] **Speaker 0:** the Yeah Oh the.
[00:53:50:719 - 00:53:50:729] **Speaker 0:** I.
[00:54:06:479 - 00:54:07:699] **Speaker 0:** Yeah, Yeah.
[00:54:17:360 - 00:54:19:290] **Speaker 0:** Yeah that makes you very.
[00:54:21:679 - 00:54:34:610] **Speaker 0:** I don't I Oh, That could be a little easier.
[00:54:35:830 - 00:54:36:080] **Speaker 0:** I look at my songs I like to everyone.
[00:54:39:080 - 00:54:39:120] **Speaker 0:** I've had.
[00:54:47:300 - 00:54:48:100] **Speaker 0:** Yeah.
[00:54:53:510 - 00:54:59:939] **Speaker 0:** Just to add to It was basically just like that.

# ENME302-26S2 Lecture 20 native Echo transcript

Date: August 14, 2026 11:00am-11:55am
Transcript type: native Echo automated transcript.

[00:00:04:280 - 00:00:04:289] **Speaker 0:** Mhm.
[00:00:25:270 - 00:00:28:250] **Speaker 1:** Oh, good morning class, we'll make a start.
[00:00:32:930 - 00:00:33:479] **Speaker 1:** All right.
[00:00:33:619 - 00:00:36:310] **Speaker 1:** Are there any questions before we dive into chapter 2
[00:00:36:590 - 00:00:39:270] **Speaker 1:** about what we've done so far, or about the course?
[00:00:42:139 - 00:00:42:680] **Speaker 1:** No.
[00:00:45:630 - 00:00:48:950] **Speaker 1:** OK, that's one way to make the class quiet, um.
[00:00:49:959 - 00:00:53:159] **Speaker 1:** Alright, so elliptic PDEs, so we looked at Laplace equation
[00:00:53:159 - 00:00:56:139] **Speaker 1:** and chapter one earlier this week, and we're going to
[00:00:56:560 - 00:00:59:060] **Speaker 1:** derive that equation for, for a heat transfer problem.
[00:00:59:880 - 00:01:03:279] **Speaker 1:** So Where do elliptic PDEs come from?
[00:01:03:779 - 00:01:08:589] **Speaker 1:** Uh, so PDEs are often Developed or obtained from uh
[00:01:08:589 - 00:01:11:389] **Speaker 1:** statements, so integral statements of physical principles.
[00:01:11:629 - 00:01:13:389] **Speaker 1:** So we might want to look at the conservation of
[00:01:13:389 - 00:01:13:910] **Speaker 1:** mass.
[00:01:14:879 - 00:01:18:440] **Speaker 1:** So that's the continuity equation for for solving fluid flows
[00:01:18:639 - 00:01:21:160] **Speaker 1:** or the conservation of energy which we can use for
[00:01:21:160 - 00:01:21:879] **Speaker 1:** heat transfer.
[00:01:23:069 - 00:01:26:309] **Speaker 1:** So we can't create or destroy energy, um.
[00:01:26:989 - 00:01:28:360] **Speaker 1:** In, in most cases.
[00:01:28:720 - 00:01:31:000] **Speaker 1:** So that's what we're going to look at.
[00:01:31:069 - 00:01:32:720] **Speaker 1:** We're going to look at a mass balance or energy
[00:01:32:720 - 00:01:33:019] **Speaker 1:** balance.
[00:01:35:110 - 00:01:36:750] **Speaker 1:** So the example that we have here is a steady
[00:01:36:750 - 00:01:41:389] **Speaker 1:** heat equation for a thin plate of some thickness outta
[00:01:41:389 - 00:01:41:709] **Speaker 1:** Z.
[00:01:41:870 - 00:01:43:370] **Speaker 1:** So it has a thickness.
[00:01:44:739 - 00:01:45:529] **Speaker 1:** That's fixed.
[00:01:46:519 - 00:01:47:980] **Speaker 1:** And we've got this rectangle.
[00:01:49:190 - 00:01:49:680] **Speaker 1:** The man.
[00:01:50:669 - 00:01:52:419] **Speaker 1:** So the front and back face are insulated, so that
[00:01:52:419 - 00:01:54:510] **Speaker 1:** means that there's no heat transfer across those two plates
[00:01:54:510 - 00:01:57:430] **Speaker 1:** or those two, those two faces, so that the temperature
[00:01:57:430 - 00:02:00:190] **Speaker 1:** is only varying in X and Y.
[00:02:06:790 - 00:02:07:959] **Speaker 1:** So that's our coordinate system.
[00:02:08:380 - 00:02:10:399] **Speaker 1:** Maybe I'll just dim the light a little bit.
[00:02:14:169 - 00:02:17:529] **Speaker 1:** So we're going to analyse a, a small cell within
[00:02:17:529 - 00:02:20:690] **Speaker 1:** the, uh, domain and we're going to look at the
[00:02:20:690 - 00:02:23:470] **Speaker 1:** heat flux in, heat flux out, and then do a
[00:02:23:809 - 00:02:25:190] **Speaker 1:** balance of, of energy.
[00:02:25:570 - 00:02:27:429] **Speaker 1:** So this is both in the X and Y directions.
[00:02:27:850 - 00:02:39:809] **Speaker 1:** So if we look on the left-hand side, We have
[00:02:39:809 - 00:02:40:850] **Speaker 1:** a flux of Q.
[00:02:41:970 - 00:02:45:500] **Speaker 1:** X, so the X component of the flux field Q
[00:02:45:500 - 00:02:48:690] **Speaker 1:** dot, uh, evaluated at some point X.
[00:02:50:820 - 00:02:55:660] **Speaker 1:** And the heat flux exiting the Small cell.
[00:02:57:559 - 00:02:58:729] **Speaker 1:** Uh, I'll show it in red here.
[00:02:58:919 - 00:02:59:779] **Speaker 1:** So this is q.
[00:02:59:990 - 00:03:01:630] **Speaker 1:** x at x + X.
[00:03:01:929 - 00:03:03:889] **Speaker 1:** So we're evaluating the, the variable q.
[00:03:04:100 - 00:03:05:740] **Speaker 1:** x at a separate point.
[00:03:05:850 - 00:03:07:210] **Speaker 1:** So X + X.
[00:03:17:830 - 00:03:20:770] **Speaker 1:** And we're going to look at the heat flux in,
[00:03:21:190 - 00:03:22:190] **Speaker 1:** in the vertical direction.
[00:03:24:029 - 00:03:29:360] **Speaker 1:** So Q.Y is at the bottom of the cell and
[00:03:29:360 - 00:03:31:240] **Speaker 1:** Q.Y plus Y at the top.
[00:03:52:330 - 00:03:55:850] **Speaker 1:** Uh, so those um fluid mechanics you'll probably be more
[00:03:56:610 - 00:03:59:550] **Speaker 1:** familiar with this, um, with conservation of mass, looking at
[00:03:59:550 - 00:04:00:649] **Speaker 1:** the continuity equation.
[00:04:00:729 - 00:04:03:119] **Speaker 1:** So it might not be too new to you, but
[00:04:03:119 - 00:04:07:259] **Speaker 1:** this is how we can form our, um, Heat equation
[00:04:07:399 - 00:04:08:919] **Speaker 1:** in 2D for a steady state.
[00:04:09:649 - 00:04:11:899] **Speaker 1:** So we're gonna consider this, this small element size.
[00:04:13:449 - 00:04:14:580] **Speaker 1:** Of data X, Y, and Z.
[00:04:15:320 - 00:04:19:040] **Speaker 1:** At steady-state, the flow into that element is going to
[00:04:19:040 - 00:04:21:558] **Speaker 1:** match that flying out of the element.
[00:04:23:489 - 00:04:28:260] **Speaker 1:** So Yeah, if we don't have heat generation, so it's
[00:04:28:260 - 00:04:31:980] **Speaker 1:** not heating up over time, it's in city-state, then what's
[00:04:31:980 - 00:04:33:279] **Speaker 1:** going in has to go out.
[00:04:36:200 - 00:04:39:049] **Speaker 1:** So city-state, the flow of heat into the element over
[00:04:39:049 - 00:04:42:170] **Speaker 1:** some time stepDeltaT must equal the flow out.
[00:04:47:660 - 00:04:48:700] **Speaker 1:** So our heat plots Q.
[00:04:48:859 - 00:04:49:209] **Speaker 1:** X.
[00:04:54:339 - 00:04:56:179] **Speaker 1:** On the left hand side, so that was the lift
[00:04:56:179 - 00:04:56:559] **Speaker 1:** box.
[00:04:59:070 - 00:04:59:230] **Speaker 1:** Q.
[00:04:59:450 - 00:05:01:690] **Speaker 1:** X is the heat flux vector.
[00:05:05:100 - 00:05:07:859] **Speaker 1:** And this is measured with units of watts per square
[00:05:07:859 - 00:05:08:279] **Speaker 1:** metre.
[00:05:08:890 - 00:05:10:820] **Speaker 1:** So joules per second per metre squared.
[00:05:11:059 - 00:05:13:519] **Speaker 1:** So it's a rate of energy through that phase.
[00:05:14:140 - 00:05:16:489] **Speaker 1:** And because we want to convert it to total energy,
[00:05:16:619 - 00:05:18:799] **Speaker 1:** we need to multiply it by that cross-sectional area.
[00:05:19:619 - 00:05:23:250] **Speaker 1:** And then multiply by time to get a An amount.
[00:05:24:089 - 00:05:28:450] **Speaker 1:** So we've got Q.X multiplied by the cross-sectional area of
[00:05:28:450 - 00:05:29:519] **Speaker 1:** that face.
[00:05:30:059 - 00:05:32:619] **Speaker 1:** So we've got a height of &DeltaY, and we've got
[00:05:32:619 - 00:05:34:179] **Speaker 1:** a depth of &DeltaZ.
[00:05:41:470 - 00:05:44:510] **Speaker 1:** And we're looking at some finite instant of time, so
[00:05:44:510 - 00:05:47:470] **Speaker 1:** delta t is, is the change in time.
[00:05:52:410 - 00:05:55:329] **Speaker 1:** So this is the flow of heat into the element
[00:05:56:019 - 00:05:57:950] **Speaker 1:** based on the left edge.
[00:05:58:510 - 00:05:59:609] **Speaker 1:** We can do the same on the bottom.
[00:05:59:769 - 00:06:00:709] **Speaker 1:** So in the Y direction.
[00:06:02:380 - 00:06:07:700] **Speaker 1:** So I've got Q Dot why And we're evaluating at
[00:06:07:700 - 00:06:10:899] **Speaker 1:** that lower edge, so evaluating at Y.
[00:06:13:230 - 00:06:16:709] **Speaker 1:** Now we want to multiply that flux by the cross-sectional
[00:06:16:709 - 00:06:18:589] **Speaker 1:** area of that bottom boundary.
[00:06:19:299 - 00:06:22:929] **Speaker 1:** Which is a length of X and a depth of
[00:06:22:929 - 00:06:23:250] **Speaker 1:** Z.
[00:06:31:269 - 00:06:33:269] **Speaker 1:** And over some finite time, delta 2.
[00:06:37:299 - 00:06:39:739] **Speaker 1:** So that's the flow of heat into the element, and
[00:06:39:739 - 00:06:42:220] **Speaker 1:** then we want to equate that with the flow out.
[00:06:43:160 - 00:06:48:029] **Speaker 1:** So hopefully this It's a little bit more straightforward, so
[00:06:48:029 - 00:06:49:910] **Speaker 1:** now we're evaluating X + X.
[00:06:51:119 - 00:06:55:040] **Speaker 1:** And we've got Y Z T.
[00:06:56:109 - 00:06:58:839] **Speaker 1:** And similarly in the Y direction we've got Q.
[00:06:59:070 - 00:06:59:489] **Speaker 1:** Y.
[00:07:00:730 - 00:07:03:410] **Speaker 1:** Evaluated at the top, so Y + Y.
[00:07:06:239 - 00:07:10:720] **Speaker 1:** Multiplied by X Z T.
[00:07:13:260 - 00:07:17:579] **Speaker 1:** So that's our conservation of energy or our balance applied
[00:07:17:579 - 00:07:18:399] **Speaker 1:** to our element.
[00:07:21:070 - 00:07:23:160] **Speaker 1:** We want to end up with a PDE because that's
[00:07:23:160 - 00:07:25:420] **Speaker 1:** what we're, that's what we're striving for.
[00:07:26:450 - 00:07:29:709] **Speaker 1:** So at the moment, this is over a discrete space.
[00:07:30:170 - 00:07:33:089] **Speaker 1:** So remember in chapter 1, we looked at reducing those
[00:07:33:089 - 00:07:35:250] **Speaker 1:** spaces down to zero to make those derivatives.
[00:07:35:290 - 00:07:36:769] **Speaker 1:** So we're going to do the same principle here.
[00:07:37:640 - 00:07:39:589] **Speaker 1:** Uh, first of all, we're going to divide through by,
[00:07:40:010 - 00:07:42:529] **Speaker 1:** uh, this expression data X, Y, Z, and T.
[00:07:43:309 - 00:07:47:250] **Speaker 1:** So that simplifies our equation and we're left with Q.
[00:07:47:480 - 00:07:47:980] **Speaker 1:** X.
[00:07:49:149 - 00:07:51:950] **Speaker 1:** Evaluated at X minus Q.
[00:07:52:209 - 00:07:52:709] **Speaker 1:** X.
[00:07:53:709 - 00:07:56:089] **Speaker 1:** Evaluated at X + X.
[00:07:58:339 - 00:08:01:380] **Speaker 1:** Divided by Delta X.
[00:08:04:390 - 00:08:07:089] **Speaker 1:** So heat flux in minus heat flux out over that
[00:08:07:589 - 00:08:08:750] **Speaker 1:** distance X.
[00:08:10:640 - 00:08:13:329] **Speaker 1:** So that already looks like a derivative or a gradient.
[00:08:15:359 - 00:08:18:480] **Speaker 1:** Hopefully, and we have the same or similar expression in
[00:08:18:480 - 00:08:19:179] **Speaker 1:** the Y direction.
[00:08:19:489 - 00:08:20:200] **Speaker 1:** So we've got Q.
[00:08:20:429 - 00:08:20:799] **Speaker 1:** Y.
[00:08:24:720 - 00:08:25:839] **Speaker 1:** evaluated at the bottom.
[00:08:25:950 - 00:08:28:690] **Speaker 1:** So Y minus Q.
[00:08:30:269 - 00:08:33:710] **Speaker 1:** Y Y + delta Y.
[00:08:35:239 - 00:08:40:018] **Speaker 1:** Divided by the length, so delta Y is the Difference.
[00:08:42:429 - 00:08:44:229] **Speaker 1:** And this is equal to 0.
[00:08:52:020 - 00:08:54:330] **Speaker 1:** So when we look at the limit as we reduce
[00:08:54:330 - 00:08:57:830] **Speaker 1:** X and Y, so as we reduce the element size
[00:08:58:010 - 00:09:00:450] **Speaker 1:** from this finite size all the way down to really,
[00:09:00:489 - 00:09:01:070] **Speaker 1:** really small.
[00:09:02:099 - 00:09:06:669] **Speaker 1:** Uh, We can write these as partial derivatives.
[00:09:07:200 - 00:09:08:789] **Speaker 1:** So this is the change in the heat flux in
[00:09:08:789 - 00:09:10:679] **Speaker 1:** the X direction with respect to X.
[00:09:12:090 - 00:09:17:409] **Speaker 1:** And it's negative because we've got Left to right rather
[00:09:17:409 - 00:09:18:559] **Speaker 1:** than right to left.
[00:09:23:320 - 00:09:25:119] **Speaker 1:** So we've got curly DQ.
[00:09:25:630 - 00:09:26:830] **Speaker 1:** X, IDX.
[00:09:32:130 - 00:09:35:140] **Speaker 0:** That Oh bless you.
[00:09:35:270 - 00:09:37:020] **Speaker 1:** Um, so minus D.
[00:09:38:450 - 00:09:42:090] **Speaker 1:** Thank you Dot YY DY.
[00:09:44:309 - 00:09:45:559] **Speaker 1:** Equal 0.
[00:09:48:229 - 00:09:50:549] **Speaker 1:** So that's exactly sort of what we did in that
[00:09:50:549 - 00:09:50:989] **Speaker 1:** first chapter.
[00:09:51:070 - 00:09:52:409] **Speaker 1:** So we, we looked at it for a reason.
[00:09:53:989 - 00:09:57:090] **Speaker 1:** All right, so I've got now a partial derivative.
[00:09:58:429 - 00:10:00:289] **Speaker 1:** In X and Y, but at the moment.
[00:10:01:059 - 00:10:02:419] **Speaker 1:** We have two unknowns.
[00:10:02:500 - 00:10:04:099] **Speaker 1:** We don't know what Q.X is and we don't know
[00:10:04:099 - 00:10:07:479] **Speaker 1:** what Q.Y is throughout the field.
[00:10:08:400 - 00:10:12:330] **Speaker 1:** So I've got 2 Uh, 2 unknowns, or two unknown
[00:10:12:330 - 00:10:12:780] **Speaker 1:** fields.
[00:10:15:039 - 00:10:16:700] **Speaker 1:** So this problem is not well posed.
[00:10:17:840 - 00:10:19:940] **Speaker 1:** Because we have more unknowns and equations.
[00:10:20:020 - 00:10:22:219] **Speaker 1:** We've got two unknowns in just that one equation, equation
[00:10:22:219 - 00:10:22:859] **Speaker 1:** 2.1.
[00:10:25:429 - 00:10:27:630] **Speaker 1:** So this comes up in a lot of different cases,
[00:10:27:869 - 00:10:29:950] **Speaker 1:** uh, but in this case, what we're gonna do is
[00:10:29:950 - 00:10:31:210] **Speaker 1:** invoke FOIA's law.
[00:10:34:169 - 00:10:37:049] **Speaker 1:** Which relates the heat flux, so Q X with the
[00:10:37:049 - 00:10:38:109] **Speaker 1:** temperature gradient.
[00:10:39:359 - 00:10:41:309] **Speaker 1:** So Q dot.
[00:10:43:590 - 00:10:47:969] **Speaker 1:** Uh, arrow, so I'm using the half arrow head for
[00:10:47:969 - 00:10:48:640] **Speaker 1:** a vector.
[00:10:50:450 - 00:10:52:409] **Speaker 1:** Because I can't do bold very well, which is what
[00:10:52:409 - 00:10:53:700] **Speaker 1:** I've done in the, the font.
[00:10:54:840 - 00:11:01:799] **Speaker 1:** So Vector is equal to minus KT.
[00:11:03:010 - 00:11:06:130] **Speaker 1:** So that should be familiar to, to everyone, but that's
[00:11:06:130 - 00:11:08:849] **Speaker 1:** the Foyer's law, the heat, heat flux.
[00:11:09:190 - 00:11:13:380] **Speaker 1:** So Physically, what this represents is that heat flux is
[00:11:13:380 - 00:11:14:099] **Speaker 1:** going downhill.
[00:11:14:179 - 00:11:16:739] **Speaker 1:** So something that's hot is going to transfer down to
[00:11:16:739 - 00:11:17:640] **Speaker 1:** something that's cooler.
[00:11:18:020 - 00:11:20:979] **Speaker 1:** And that's what the negative sign represents because it's opposing
[00:11:20:979 - 00:11:24:409] **Speaker 1:** the gradient of temperature and K is a thermal conductivity,
[00:11:24:460 - 00:11:26:940] **Speaker 1:** so it has a diffusive rate related to the thermal
[00:11:26:940 - 00:11:27:359] **Speaker 1:** conductivity.
[00:11:27:419 - 00:11:29:330] **Speaker 1:** So if you have steel or something, it's gonna transfer
[00:11:29:330 - 00:11:32:039] **Speaker 1:** heat a lot quicker than wood or, or some other
[00:11:32:039 - 00:11:32:380] **Speaker 1:** material.
[00:11:35:309 - 00:11:39:409] **Speaker 1:** We're gonna expand the grad T, so upside down triangle.
[00:11:39:950 - 00:11:42:979] **Speaker 1:** This has got Two components.
[00:11:43:140 - 00:11:47:260] **Speaker 1:** So we're looking at a 2D domain and X and
[00:11:47:260 - 00:11:47:750] **Speaker 1:** Y.
[00:11:48:900 - 00:11:52:429] **Speaker 1:** So we've got two components of this gradient vector gravity.
[00:11:53:380 - 00:11:56:840] **Speaker 1:** We've got DT by DX.
[00:12:00:359 - 00:12:03:359] **Speaker 1:** And this is In the X direction.
[00:12:03:440 - 00:12:06:280] **Speaker 1:** So I'm using i hat as the unit vector in
[00:12:06:280 - 00:12:07:179] **Speaker 1:** the X direction.
[00:12:08:260 - 00:12:10:780] **Speaker 1:** And DT by DY.
[00:12:12:950 - 00:12:23:369] **Speaker 1:** Jay hat You're familiar with unit vectors and gradients?
[00:12:24:770 - 00:12:25:119] **Speaker 1:** Yeah.
[00:12:27:090 - 00:12:27:890] **Speaker 1:** Yeah, good.
[00:12:28:609 - 00:12:32:130] **Speaker 1:** Otherwise, I can, I can explain further, but I'm, I'm
[00:12:32:130 - 00:12:33:859] **Speaker 1:** hoping the math course has taught you something.
[00:12:34:429 - 00:12:40:210] **Speaker 1:** So we've got Q.X. And I And Q.
[00:12:40:479 - 00:12:40:890] **Speaker 1:** Y.
[00:12:41:710 - 00:12:52:849] **Speaker 1:** Inject All right.
[00:12:55:659 - 00:12:57:919] **Speaker 1:** And this is sort of just what we've described.
[00:12:59:219 - 00:13:01:289] **Speaker 1:** Yeah, the direction goes from hot to cold.
[00:13:01:340 - 00:13:02:940] **Speaker 1:** That's why it's a negative, negative sign.
[00:13:03:969 - 00:13:07:289] **Speaker 1:** So we're going to plug in our expression for the
[00:13:07:289 - 00:13:10:090] **Speaker 1:** heat fluxes into our equation 2.1.
[00:13:11:309 - 00:13:13:630] **Speaker 1:** And what we'll figure out is that then we've only
[00:13:13:630 - 00:13:16:830] **Speaker 1:** got one dependent verbal, T, rather than two, q.
[00:13:16:919 - 00:13:17:349] **Speaker 1:** X and Q.
[00:13:17:489 - 00:13:17:840] **Speaker 1:** Y.
[00:13:18:760 - 00:13:23:710] **Speaker 1:** So we've got minus gradient dt by DX of Q.X
[00:13:23:710 - 00:13:28:000] **Speaker 1:** and we said Q.X is equal to Minus KDT by
[00:13:28:000 - 00:13:28:539] **Speaker 1:** DX.
[00:13:34:719 - 00:13:36:359] **Speaker 1:** So that's our expression for Q.
[00:13:36:479 - 00:13:36:940] **Speaker 1:** X.
[00:13:39:710 - 00:13:47:070] **Speaker 1:** Our next term is minus D by DY of Q.Y.
[00:13:47:390 - 00:13:51:710] **Speaker 1:** So Q.Y is the gradient minus KDT by DY in
[00:13:51:710 - 00:13:52:390] **Speaker 1:** the Y direction.
[00:14:00:280 - 00:14:01:169] **Speaker 1:** Which is equal to 0.
[00:14:07:309 - 00:14:11:630] **Speaker 1:** So if we have a simplified case where the steel
[00:14:11:630 - 00:14:12:130] **Speaker 1:** plate.
[00:14:13:219 - 00:14:15:900] **Speaker 1:** Has a uniform thermal conductivity, so maybe it's just one
[00:14:15:900 - 00:14:16:460] **Speaker 1:** steel plate.
[00:14:16:500 - 00:14:20:280] **Speaker 1:** It hasn't got mixed materials or, um, yeah, hasn't.
[00:14:21:500 - 00:14:23:719] **Speaker 1:** Hasn't got any changes in thermal conductivity.
[00:14:24:260 - 00:14:28:349] **Speaker 1:** We can essentially bring these constants outside of the derivatives.
[00:14:29:229 - 00:14:30:630] **Speaker 1:** So think of the product rule if you wish.
[00:14:32:200 - 00:14:36:429] **Speaker 1:** And we're left with D2T by DX2.
[00:14:37:619 - 00:14:39:659] **Speaker 1:** Plus D2T by DY2.
[00:14:41:429 - 00:14:42:039] **Speaker 1:** Equal to 0.
[00:14:44:750 - 00:14:47:070] **Speaker 1:** So the caves go out and then they drop out
[00:14:47:070 - 00:14:48:330] **Speaker 1:** because we've got 0 on the other side.
[00:14:50:030 - 00:14:53:700] **Speaker 1:** So what we've done is use the conservation of energy
[00:14:54:159 - 00:14:57:000] **Speaker 1:** and recovered or derived the Laplace equation.
[00:14:57:789 - 00:15:01:950] **Speaker 1:** So this equation represents the temperature field within the plate.
[00:15:02:640 - 00:15:05:840] **Speaker 1:** We talked a bit about boundary conditions earlier, uh, because
[00:15:05:840 - 00:15:08:080] **Speaker 1:** we know that there are infinite number of solutions that
[00:15:08:080 - 00:15:09:900] **Speaker 1:** satisfy the, the pass equation.
[00:15:10:830 - 00:15:12:239] **Speaker 1:** But that's not going to be very helpful when we're
[00:15:12:239 - 00:15:13:840] **Speaker 1:** trying to figure out the temperature field.
[00:15:15:250 - 00:15:18:270] **Speaker 1:** So we're gonna talk a bit about boundary conditions next.
[00:15:23:239 - 00:15:26:739] **Speaker 1:** So just like with ODEs, the ordinary differential equations, boundary
[00:15:26:739 - 00:15:28:760] **Speaker 1:** conditions are needed to obtain a unique solution.
[00:15:29:640 - 00:15:32:000] **Speaker 1:** And we're going to look at 3 types of boundary
[00:15:32:000 - 00:15:32:799] **Speaker 1:** conditions in this class.
[00:15:33:239 - 00:15:37:099] **Speaker 1:** So when we prescribe the temperature on, on a boundary,
[00:15:37:520 - 00:15:40:039] **Speaker 1:** we're calling this the Dirichlet boundary condition.
[00:15:43:890 - 00:15:45:950] **Speaker 1:** For example, the temperature.
[00:15:47:109 - 00:15:49:650] **Speaker 1:** At X equals 0, so on the left-hand side.
[00:15:53:070 - 00:15:56:530] **Speaker 1:** And for all Y values on that, on that edge.
[00:16:00:010 - 00:16:02:359] **Speaker 1:** is equal to some function and it could be a
[00:16:02:359 - 00:16:04:770] **Speaker 1:** function of Y, it could be varying along the edge.
[00:16:18:640 - 00:16:23:150] **Speaker 1:** So an example of a fixed or prescribed temperature would
[00:16:23:150 - 00:16:25:070] **Speaker 1:** be a melting interface.
[00:16:30:869 - 00:16:36:400] **Speaker 1:** So T At some point, Equal to 0 °C.
[00:16:41:960 - 00:16:44:520] **Speaker 1:** So it's melting, it's fixed at 0 degrees, even if
[00:16:44:520 - 00:16:48:760] **Speaker 1:** you're introducing additional heat, it's just transferring to, to a
[00:16:48:760 - 00:16:49:520] **Speaker 1:** liquid phase.
[00:16:52:950 - 00:16:55:200] **Speaker 1:** The second type of boundary condition that we're looking at
[00:16:55:200 - 00:16:56:880] **Speaker 1:** is the Neumann boundary.
[00:16:57:750 - 00:17:00:429] **Speaker 1:** So instead of setting the, the dependent variable T, we're
[00:17:00:429 - 00:17:01:450] **Speaker 1:** gonna set the gradient.
[00:17:01:750 - 00:17:03:229] **Speaker 1:** So DT by DX.
[00:17:03:929 - 00:17:05:770] **Speaker 1:** And the example that we've got here is setting the
[00:17:05:770 - 00:17:06:650] **Speaker 1:** heat flux q.
[00:17:06:760 - 00:17:07:030] **Speaker 1:** X.
[00:17:09:380 - 00:17:10:760] **Speaker 1:** Maybe on the left-hand side again.
[00:17:13:800 - 00:17:16:359] **Speaker 1:** And we said the heat flux Q in the next
[00:17:16:359 - 00:17:20:199] **Speaker 1:** direction is equal to minus KDT by the X.
[00:17:22:839 - 00:17:24:540] **Speaker 1:** And we're gonna evaluate that gradient.
[00:17:25:390 - 00:17:26:369] **Speaker 1:** On the left-hand side.
[00:17:27:069 - 00:17:28:430] **Speaker 1:** So at that X equals 0.
[00:17:38:319 - 00:17:40:180] **Speaker 1:** And maybe.
[00:17:43:089 - 00:17:45:719] **Speaker 1:** This expression, this heat flux is equal to some other
[00:17:45:719 - 00:17:47:650] **Speaker 1:** function G that varies in Y.
[00:18:01:050 - 00:18:03:989] **Speaker 1:** So some examples might be like a blowtorch, maybe you've
[00:18:03:989 - 00:18:06:630] **Speaker 1:** got some sort of constant heat flux, uh, or using
[00:18:06:630 - 00:18:07:349] **Speaker 1:** insulation.
[00:18:08:319 - 00:18:11:619] **Speaker 1:** So the assumption that we made in that derivation was
[00:18:11:619 - 00:18:14:459] **Speaker 1:** that the front and back faces were fully insulated.
[00:18:15:000 - 00:18:15:579] **Speaker 1:** So Q.
[00:18:16:199 - 00:18:17:550] **Speaker 1:** X is equal to 0.
[00:18:18:010 - 00:18:19:959] **Speaker 1:** That is the fully insulated.
[00:18:21:520 - 00:18:21:750] **Speaker 1:** Boundary condition.
[00:18:24:410 - 00:18:26:400] **Speaker 1:** The 3rd boundary condition that we're going to look at
[00:18:26:400 - 00:18:27:520] **Speaker 1:** is the robin.
[00:18:28:579 - 00:18:32:829] **Speaker 1:** Foundary and this is essentially a mix of uh both
[00:18:32:829 - 00:18:33:810] **Speaker 1:** of these first two.
[00:18:34:810 - 00:18:36:810] **Speaker 1:** So, for example, if we have a heat flux q.
[00:18:36:949 - 00:18:37:229] **Speaker 1:** X.
[00:18:39:030 - 00:18:41:390] **Speaker 1:** On the left, X equals 0, varying Y.
[00:18:42:270 - 00:18:48:609] **Speaker 1:** Equal to Uh, a coefficient And T minus Tref.
[00:18:49:780 - 00:18:51:810] **Speaker 1:** So Tref is just some reference temperature.
[00:18:51:859 - 00:18:55:699] **Speaker 1:** It might be the ambient temperature surrounding the, the object
[00:18:55:699 - 00:18:57:500] **Speaker 1:** that we're looking at or the boundary.
[00:18:59:329 - 00:19:02:010] **Speaker 1:** T is the temperature on that boundary.
[00:19:02:780 - 00:19:06:660] **Speaker 1:** And H is convective heat transfer coefficient.
[00:19:06:739 - 00:19:09:849] **Speaker 1:** So Physically, you could think of this as a heat
[00:19:09:849 - 00:19:13:689] **Speaker 1:** flux varying depending on what temperature difference between the surface
[00:19:13:689 - 00:19:14:750] **Speaker 1:** and the surrounding air.
[00:19:15:489 - 00:19:18:329] **Speaker 1:** And it's got this sort of multiplication or coefficient that's
[00:19:18:329 - 00:19:20:270] **Speaker 1:** varying how quickly that heat transfers.
[00:19:22:829 - 00:19:24:969] **Speaker 1:** So some of those, you, you know, I guess the
[00:19:24:969 - 00:19:28:000] **Speaker 1:** next students are doing the heat transfer course, um, so
[00:19:28:000 - 00:19:29:260] **Speaker 1:** you dive into this a lot more.
[00:19:29:380 - 00:19:31:959] **Speaker 1:** There's lots of different heat transfer coefficients for different objects,
[00:19:32:579 - 00:19:34:579] **Speaker 1:** uh, but for this class, we're just going to have
[00:19:34:579 - 00:19:36:180] **Speaker 1:** a set value for each.
[00:19:39:680 - 00:19:44:459] **Speaker 1:** Uh, we can insert our expression for Q.X. So left
[00:19:44:459 - 00:19:46:199] **Speaker 1:** with minus K.
[00:19:47:319 - 00:19:51:400] **Speaker 1:** DT5 DX at X equals 0.
[00:19:52:459 - 00:19:56:550] **Speaker 1:** Equal to HT minus Tref.
[00:20:00:609 - 00:20:05:010] **Speaker 1:** So out of these terms, K is a constant, so
[00:20:05:010 - 00:20:08:869] **Speaker 1:** material property H is sub is generally dependent on the,
[00:20:08:920 - 00:20:11:949] **Speaker 1:** the shapes object, uh, sorry, the object's shape.
[00:20:12:280 - 00:20:14:709] **Speaker 1:** Um, Tref is the surrounding temperature.
[00:20:15:449 - 00:20:17:290] **Speaker 1:** T is going to be the temperature or the dependent
[00:20:17:290 - 00:20:18:699] **Speaker 1:** variable that we're solving for.
[00:20:19:199 - 00:20:21:650] **Speaker 1:** DT by DX is also part of that temperature field.
[00:20:24:599 - 00:20:26:099] **Speaker 1:** And this is just a combination.
[00:20:30:400 - 00:20:36:849] **Speaker 1:** Of the Uh To boundary conditions.
[00:20:42:140 - 00:20:42:150] **Speaker 1:** Who?
[00:20:47:170 - 00:20:50:199] **Speaker 1:** So fixing the different variable, fixing the gradient or having
[00:20:50:199 - 00:20:52:310] **Speaker 1:** both is, is, is a good summary.
[00:20:54:930 - 00:20:58:280] **Speaker 1:** Right Any questions on?
[00:20:59:750 - 00:21:00:390] **Speaker 1:** On this.
[00:21:04:530 - 00:21:08:260] **Speaker 1:** Right OK, now we've got our elliptic PDE.
[00:21:08:760 - 00:21:11:660] **Speaker 1:** We've talked about the different boundary conditions.
[00:21:12:239 - 00:21:14:790] **Speaker 1:** So if we apply some boundary conditions to a Laplace
[00:21:14:790 - 00:21:17:089] **Speaker 1:** equation, to the elliptic PD, then we should be able
[00:21:17:089 - 00:21:18:199] **Speaker 1:** to find a unique solution.
[00:21:18:989 - 00:21:21:979] **Speaker 1:** So we're going to talk through some analytical methods for
[00:21:21:979 - 00:21:22:900] **Speaker 1:** solving that system.
[00:21:23:770 - 00:21:24:900] **Speaker 1:** Solving these problems.
[00:21:25:439 - 00:21:29:219] **Speaker 1:** So generally analytical methods are rare and difficult for PDEs,
[00:21:29:680 - 00:21:31:239] **Speaker 1:** ah, yep.
[00:21:31:640 - 00:21:33:819] **Speaker 1:** So however they are very useful to check for the
[00:21:33:959 - 00:21:36:239] **Speaker 1:** um validation of numerical solutions.
[00:21:37:160 - 00:21:38:660] **Speaker 1:** And that's what we're gonna use in this class, so
[00:21:38:819 - 00:21:41:439] **Speaker 1:** we're doing separation of variables mostly, and that's what we're
[00:21:41:439 - 00:21:42:739] **Speaker 1:** gonna guide you through now.
[00:21:43:530 - 00:21:46:839] **Speaker 1:** So if the PD is linear, we talked about linearity
[00:21:46:839 - 00:21:49:880] **Speaker 1:** in chapter one, homogeneous, so we don't have that source
[00:21:49:880 - 00:21:50:119] **Speaker 1:** term.
[00:21:51:150 - 00:21:52:849] **Speaker 1:** And the domain is simple enough.
[00:21:54:060 - 00:21:56:520] **Speaker 1:** So maybe it's just a square or rectangle.
[00:21:57:310 - 00:22:00:760] **Speaker 1:** Ah, the method of separation of variables can sometimes be
[00:22:00:760 - 00:22:01:089] **Speaker 1:** used.
[00:22:01:439 - 00:22:03:680] **Speaker 1:** So there's quite a few qualifiers for this one.
[00:22:04:520 - 00:22:06:290] **Speaker 1:** so we're just going to use it in some very
[00:22:06:290 - 00:22:07:140] **Speaker 1:** specific cases.
[00:22:09:119 - 00:22:11:640] **Speaker 1:** You might find that when you're doing numerical simulations, you
[00:22:11:640 - 00:22:15:140] **Speaker 1:** want to validate your model on a very simple case
[00:22:15:640 - 00:22:19:079] **Speaker 1:** prior to to doing your more advanced work, and you'll
[00:22:19:079 - 00:22:21:719] **Speaker 1:** find that also when you're doing your, your research project
[00:22:21:719 - 00:22:23:670] **Speaker 1:** next year if you're using simulations, you might want to
[00:22:23:670 - 00:22:27:760] **Speaker 1:** look at simplified geometries before advancing to more complex and
[00:22:27:760 - 00:22:30:479] **Speaker 1:** final, uh, products for your client.
[00:22:33:400 - 00:22:35:300] **Speaker 1:** So we're gonna look at the Laplace equation.
[00:22:35:760 - 00:22:39:520] **Speaker 1:** This is D2U by DX2 plus D2U by DY2 equal
[00:22:39:520 - 00:22:40:099] **Speaker 1:** to 0.
[00:22:41:109 - 00:22:45:270] **Speaker 1:** We're going to try and find a solution that groups
[00:22:45:270 - 00:22:47:630] **Speaker 1:** all of the X terms together and all of the
[00:22:47:630 - 00:22:48:469] **Speaker 1:** Y terms together.
[00:22:49:569 - 00:22:50:849] **Speaker 1:** So X capital.
[00:22:51:640 - 00:22:53:219] **Speaker 1:** Is a function of X only.
[00:22:54:709 - 00:22:58:390] **Speaker 1:** And capital Y is a function of Y only.
[00:22:59:420 - 00:23:01:780] **Speaker 1:** So this is where it's named separation of variables come
[00:23:01:780 - 00:23:02:160] **Speaker 1:** from.
[00:23:02:540 - 00:23:04:660] **Speaker 1:** We're separating all of the X terms and all of
[00:23:04:660 - 00:23:05:420] **Speaker 1:** the Y terms.
[00:23:08:640 - 00:23:10:530] **Speaker 1:** So we're going to assume the solution.
[00:23:11:800 - 00:23:14:420] **Speaker 1:** U equal to X times Y capitals.
[00:23:15:250 - 00:23:18:660] **Speaker 1:** So we're gonna plug in our assumed solution into our
[00:23:18:660 - 00:23:19:619] **Speaker 1:** Laplace equation.
[00:23:19:900 - 00:23:24:020] **Speaker 1:** So we're gonna plug in XY into our Second ordered
[00:23:24:020 - 00:23:24:510] **Speaker 1:** the revolut.
[00:23:28:199 - 00:23:30:079] **Speaker 1:** We'll do it in steps.
[00:23:30:439 - 00:23:33:479] **Speaker 1:** So the first order derivative of the first term D
[00:23:33:479 - 00:23:34:380] **Speaker 1:** by DX.
[00:23:37:400 - 00:23:40:099] **Speaker 1:** is equal to the derivative.
[00:23:41:819 - 00:23:45:089] **Speaker 1:** Of you, which is XY.
[00:23:54:900 - 00:23:58:839] **Speaker 1:** And we've just said that X only varies in X
[00:23:59:030 - 00:24:01:619] **Speaker 1:** and Y only varies in Y.
[00:24:02:099 - 00:24:05:780] **Speaker 1:** So if we differentiate with respect to X, Y is
[00:24:05:780 - 00:24:06:760] **Speaker 1:** essentially a constant.
[00:24:07:680 - 00:24:08:430] **Speaker 1:** In X.
[00:24:08:680 - 00:24:10:540] **Speaker 1:** So Y can go outside of the derivative.
[00:24:13:589 - 00:24:17:939] **Speaker 1:** And we're left with DX by DX.
[00:24:18:260 - 00:24:20:760] **Speaker 1:** Now these are full derivatives or just the normal D's.
[00:24:21:599 - 00:24:24:949] **Speaker 1:** Because X is only a function of X, it's only
[00:24:24:949 - 00:24:26:520] **Speaker 1:** dependent on one independent variable.
[00:24:40:109 - 00:24:42:630] **Speaker 1:** We want the 2nd order derivative in X, so we're
[00:24:42:630 - 00:24:45:310] **Speaker 1:** going to take the derivative of our term.
[00:24:46:250 - 00:24:48:630] **Speaker 1:** So D2U by DX2.
[00:24:55:800 - 00:24:56:540] **Speaker 1:** He's an x-ray.
[00:24:57:829 - 00:25:00:510] **Speaker 1:** is equal to the derivative.
[00:25:02:349 - 00:25:04:290] **Speaker 1:** Of D by DX.
[00:25:08:099 - 00:25:12:579] **Speaker 1:** And we just calculated that as Y D X Y
[00:25:12:579 - 00:25:13:339] **Speaker 1:** D X.
[00:25:24:869 - 00:25:27:109] **Speaker 1:** And again, Y is still a constant in X, so
[00:25:27:109 - 00:25:29:189] **Speaker 1:** it's gonna pop outside the derivative and we're left with
[00:25:29:189 - 00:25:33:270] **Speaker 1:** Y D 2 X Y D X 2.
[00:25:39:770 - 00:25:40:910] **Speaker 1:** So that was our first term.
[00:25:42:329 - 00:25:43:380] **Speaker 1:** An equation 2.7.
[00:25:43:500 - 00:25:45:300] **Speaker 1:** Now the equation we're going to do the second term
[00:25:45:300 - 00:25:46:739] **Speaker 1:** D2 U by DY 2.
[00:25:47:569 - 00:25:48:380] **Speaker 1:** But it's very similar.
[00:25:48:630 - 00:25:50:469] **Speaker 1:** So we'll we'll skip a couple of steps.
[00:25:50:849 - 00:25:54:969] **Speaker 1:** So we've got D2U by DY2.
[00:25:57:079 - 00:25:59:959] **Speaker 1:** Now X isn't varying in Y, so it's the coefficient
[00:25:59:959 - 00:26:02:400] **Speaker 1:** that gets popped out of the derivative and we're left
[00:26:02:400 - 00:26:06:199] **Speaker 1:** with D2 Y by DY2.
[00:26:13:619 - 00:26:15:079] **Speaker 1:** Now we've got both terms, we're going to chuck them
[00:26:15:079 - 00:26:16:349] **Speaker 1:** back into our Laplace equation.
[00:26:17:599 - 00:26:22:280] **Speaker 1:** D2U by DX2 plus D2U by DY2.
[00:26:23:989 - 00:26:28:069] **Speaker 1:** We said the first time was YD 2 X by
[00:26:28:069 - 00:26:29:150] **Speaker 1:** DX2.
[00:26:32:500 - 00:26:34:699] **Speaker 1:** And that second term is X.
[00:26:35:709 - 00:26:39:420] **Speaker 1:** D2 Y by DY2.
[00:26:42:290 - 00:26:42:939] **Speaker 1:** Equal to 0.
[00:26:54:459 - 00:26:56:660] **Speaker 1:** Making progress, I mean they sort of look like ODEs,
[00:26:56:790 - 00:26:58:500] **Speaker 1:** sort of, we've got some full derivatives.
[00:26:59:209 - 00:27:01:319] **Speaker 1:** Uh, we've got two terms.
[00:27:01:699 - 00:27:04:180] **Speaker 1:** This first term is a mixture of X and Y's
[00:27:04:180 - 00:27:06:140] **Speaker 1:** because it's got both capital X capital Y.
[00:27:06:750 - 00:27:09:109] **Speaker 1:** Uh, likewise for the second term, we want to separate
[00:27:09:109 - 00:27:10:030] **Speaker 1:** those variables out.
[00:27:10:550 - 00:27:13:410] **Speaker 1:** So what we could do is divide 3 by XY.
[00:27:14:500 - 00:27:18:869] **Speaker 1:** And what we're left with is 1 divided by X.
[00:27:22:050 - 00:27:26:119] **Speaker 1:** D2 X by DX2, so that's our first term.
[00:27:29:790 - 00:27:31:910] **Speaker 1:** We're going to shift the other term on the other
[00:27:31:910 - 00:27:32:969] **Speaker 1:** side of the equal sign.
[00:27:35:400 - 00:27:39:449] **Speaker 1:** So it's equal to -1 over Y.
[00:27:41:589 - 00:27:46:189] **Speaker 1:** D2 Y by DY squid.
[00:28:00:130 - 00:28:00:609] **Speaker 1:** Cool.
[00:28:00:969 - 00:28:01:290] **Speaker 1:** All right.
[00:28:01:520 - 00:28:03:160] **Speaker 1:** So we've, we've split them apart.
[00:28:03:439 - 00:28:05:569] **Speaker 1:** Uh, they're only going to be, this is only gonna
[00:28:05:569 - 00:28:09:479] **Speaker 1:** hold true if this holds true for all X and
[00:28:09:479 - 00:28:10:119] **Speaker 1:** Y, right?
[00:28:10:410 - 00:28:13:729] **Speaker 1:** So the argument here is that because both of these
[00:28:13:729 - 00:28:15:770] **Speaker 1:** sides of the equal sign must match.
[00:28:16:810 - 00:28:19:380] **Speaker 1:** They have to equal some constant value.
[00:28:19:650 - 00:28:21:530] **Speaker 1:** And we're gonna call this constant value lambda.
[00:28:32:119 - 00:28:35:359] **Speaker 1:** With that argument, we can look at the 1st and
[00:28:35:359 - 00:28:38:260] **Speaker 1:** last part of the equation and the 2nd and 3rd
[00:28:38:260 - 00:28:41:459] **Speaker 1:** part of the equation, and we form two ordinary differential
[00:28:41:459 - 00:28:42:219] **Speaker 1:** equations.
[00:28:44:369 - 00:28:49:060] **Speaker 1:** The first being D2 X by DX2.
[00:28:50:670 - 00:28:51:930] **Speaker 1:** Equal to lambda.
[00:28:52:930 - 00:28:54:689] **Speaker 1:** Multiplied by X.
[00:28:57:900 - 00:29:02:530] **Speaker 1:** And the second D2Y by DY2.
[00:29:04:479 - 00:29:08:060] **Speaker 1:** Equal to minus lambda Y.
[00:29:17:140 - 00:29:18:900] **Speaker 1:** So we've gone from a PDE.
[00:29:20:729 - 00:29:26:290] **Speaker 1:** Um, 1 PDE to 2 ODEs, and we know how
[00:29:26:290 - 00:29:27:810] **Speaker 1:** to solve the ODEs.
[00:29:28:829 - 00:29:32:890] **Speaker 1:** We've got some, um, yeah, some tools to solve these.
[00:29:33:800 - 00:29:39:780] **Speaker 1:** So The solution of each of these ODEs depend on
[00:29:39:780 - 00:29:41:109] **Speaker 1:** the sign of lambda.
[00:29:42:800 - 00:29:44:640] **Speaker 1:** So we're going to have a series.
[00:29:44:719 - 00:29:45:880] **Speaker 1:** We're gonna have 3 different cases.
[00:29:45:959 - 00:29:47:819] **Speaker 1:** We're gonna look at lambda equal to 0.
[00:29:48:930 - 00:29:52:359] **Speaker 1:** Uh, lambda being positive and lambda being negative.
[00:29:55:329 - 00:29:58:410] **Speaker 1:** Because depending on the sign or the value of lambda
[00:29:58:770 - 00:30:00:969] **Speaker 1:** dictates the general solution of the ODE.
[00:30:03:069 - 00:30:04:689] **Speaker 1:** That's why we're going to look at all three cases.
[00:30:05:189 - 00:30:08:030] **Speaker 1:** So maybe we start with lambda equals 0 1st because
[00:30:08:030 - 00:30:09:089] **Speaker 1:** that's the easiest one.
[00:30:09:630 - 00:30:11:859] **Speaker 1:** So if you had 0 on the right-hand side for
[00:30:11:859 - 00:30:15:410] **Speaker 1:** both cases, uh, you've just got D2 X by DX2
[00:30:15:410 - 00:30:17:250] **Speaker 1:** equal to 0, you integrate twice.
[00:30:17:589 - 00:30:19:550] **Speaker 1:** So you've got a linear expression A X + B.
[00:30:20:560 - 00:30:22:439] **Speaker 1:** Likewise, CY plus D.
[00:30:23:760 - 00:30:33:729] **Speaker 1:** So this Is for Um, X Of X.
[00:30:35:390 - 00:30:38:459] **Speaker 1:** The term is for Y of I.
[00:30:43:250 - 00:30:46:420] **Speaker 1:** So the general solution when lambda is equal to 0
[00:30:46:760 - 00:30:47:939] **Speaker 1:** is A X + B.
[00:30:49:119 - 00:30:52:079] **Speaker 1:** And then the second case, we've got CY + D.
[00:30:53:219 - 00:30:55:060] **Speaker 1:** Overall, our solution you.
[00:30:56:199 - 00:30:58:959] **Speaker 1:** An equation 2.8 we said was the, the combination of
[00:30:58:959 - 00:31:00:319] **Speaker 1:** the two, so X times Y.
[00:31:02:569 - 00:31:04:199] **Speaker 1:** So that's why we've multiplied them together.
[00:31:05:550 - 00:31:06:849] **Speaker 1:** So that's lambda equals 0.
[00:31:07:510 - 00:31:10:489] **Speaker 1:** Now we want to analyse the cases when lambda is
[00:31:10:489 - 00:31:11:609] **Speaker 1:** negative or positive.
[00:31:13:709 - 00:31:18:640] **Speaker 1:** So, for example, if it was negative, um, we want
[00:31:18:640 - 00:31:20:439] **Speaker 1:** to make sure that it is always negative.
[00:31:20:550 - 00:31:23:260] **Speaker 1:** So what we can do is create another variable, new.
[00:31:24:630 - 00:31:25:979] **Speaker 1:** And square this term.
[00:31:26:030 - 00:31:27:290] **Speaker 1:** So if we square a number.
[00:31:28:099 - 00:31:31:189] **Speaker 1:** Um, that's not zero, it's always going to be positive.
[00:31:31:880 - 00:31:34:640] **Speaker 1:** So if we're setting lambda to be negative, we could
[00:31:35:119 - 00:31:37:839] **Speaker 1:** replace it with minus mu 2 and we know that
[00:31:37:839 - 00:31:39:479] **Speaker 1:** it's always going to be less than 0.
[00:31:42:030 - 00:31:47:160] **Speaker 1:** So if Lambda is equal to minus mu 2, then
[00:31:47:160 - 00:31:49:900] **Speaker 1:** the general solution is a sin mu x.
[00:31:51:060 - 00:31:54:650] **Speaker 1:** Plus B cos mu x, so that was for X
[00:31:54:880 - 00:31:55:630] **Speaker 1:** of X.
[00:31:57:239 - 00:32:02:239] **Speaker 1:** And D2Y by DY2 equal to mu2Y.
[00:32:02:479 - 00:32:12:430] **Speaker 1:** The general solution is This, this So just, um, isolating
[00:32:12:430 - 00:32:16:310] **Speaker 1:** those individual ODEs should be familiar from your, your math
[00:32:16:310 - 00:32:16:890] **Speaker 1:** courses.
[00:32:20:920 - 00:32:22:670] **Speaker 1:** The only difference here is that we're combining them.
[00:32:25:510 - 00:32:30:199] **Speaker 1:** Oh And just for completeness, we do the same when
[00:32:30:199 - 00:32:31:599] **Speaker 1:** we have lambda being positive.
[00:32:31:680 - 00:32:33:359] **Speaker 1:** So mu 2 it's always going to be greater than
[00:32:33:359 - 00:32:34:020] **Speaker 1:** 0.
[00:32:34:439 - 00:32:39:520] **Speaker 1:** And that first, Expression is our solution X X.
[00:32:40:969 - 00:32:42:969] **Speaker 1:** And why of why?
[00:32:52:180 - 00:32:58:170] **Speaker 1:** So equations 2.10 through 12 are essentially the solutions, well,
[00:32:58:250 - 00:33:01:180] **Speaker 1:** these are solutions to our Laplace equation.
[00:33:02:229 - 00:33:03:199] **Speaker 1:** Equation 2.7.
[00:33:11:599 - 00:33:13:650] **Speaker 1:** And again, we're going to have an infinite number of
[00:33:13:650 - 00:33:16:680] **Speaker 1:** solutions because mu is some arbitrary constant.
[00:33:17:510 - 00:33:20:069] **Speaker 1:** Uh, what we need to do is apply our boundary
[00:33:20:069 - 00:33:21:589] **Speaker 1:** conditions to find the unique solution.
[00:33:21:760 - 00:33:23:150] **Speaker 1:** So we'll go through some examples shortly.
[00:33:24:280 - 00:33:28:689] **Speaker 1:** First, just a side note that Uh, we can use
[00:33:28:689 - 00:33:30:130] **Speaker 1:** hyperbolic functions.
[00:33:30:750 - 00:33:34:510] **Speaker 1:** So instead of cosine, instead of the exponentials, you can
[00:33:34:510 - 00:33:38:630] **Speaker 1:** replace it with um hyperbolic cosine and hyperbolic sine functions.
[00:33:40:560 - 00:33:42:560] **Speaker 1:** That, that's just a choice if you, if you want
[00:33:42:560 - 00:33:43:199] **Speaker 1:** to do that.
[00:33:43:949 - 00:33:46:800] **Speaker 1:** Um, Yeah.
[00:33:48:280 - 00:33:50:680] **Speaker 1:** You might find it easier or harder, either way.
[00:33:51:119 - 00:33:51:520] **Speaker 1:** All right.
[00:33:54:280 - 00:33:56:260] **Speaker 1:** An example work through.
[00:33:56:880 - 00:33:59:420] **Speaker 1:** So derived the Laplace equation.
[00:33:59:880 - 00:34:02:199] **Speaker 1:** We've got some analytical solutions and we know some boundary
[00:34:02:199 - 00:34:02:670] **Speaker 1:** conditions.
[00:34:03:099 - 00:34:05:140] **Speaker 1:** So we can, we can tackle this first problem.
[00:34:06:180 - 00:34:10:370] **Speaker 1:** So we've got the PDE we've got our domain.
[00:34:10:638 - 00:34:12:790] **Speaker 1:** It's ranging from 0 to 2 in X and 0
[00:34:12:790 - 00:34:13:679] **Speaker 1:** to 1 in Y.
[00:34:14:199 - 00:34:15:800] **Speaker 1:** and we've got some boundary conditions.
[00:34:16:080 - 00:34:18:540] **Speaker 1:** So we've got 4, so 1 on each edge.
[00:34:18:878 - 00:34:20:169] **Speaker 1:** We've got 4 boundary conditions.
[00:34:20:360 - 00:34:22:878] **Speaker 1:** Uh, we've got 2 second-order derivatives X and Y.
[00:34:22:949 - 00:34:24:719] **Speaker 1:** So we have enough information, so we should be able
[00:34:24:719 - 00:34:25:898] **Speaker 1:** to figure out a unique solution.
[00:34:29:040 - 00:34:32:059] **Speaker 1:** And We derived 3.
[00:34:33:469 - 00:34:36:510] **Speaker 1:** Solution types for the for the Laplace equation.
[00:34:37:850 - 00:34:42:408] **Speaker 1:** Only one of these will satisfy all boundary conditions.
[00:34:43:849 - 00:34:46:718] **Speaker 1:** So for this example, we're gonna go through each one.
[00:34:47:729 - 00:34:50:050] **Speaker 1:** And determine whether or not it's a, it's a solution
[00:34:50:050 - 00:34:50:370] **Speaker 1:** or not.
[00:34:50:610 - 00:34:52:919] **Speaker 1:** So we're, we're told that it's not a solution, uh,
[00:34:52:929 - 00:34:54:790] **Speaker 1:** for the linear case, but we're just going to show
[00:34:55:520 - 00:34:56:128] **Speaker 1:** why it isn't.
[00:35:00:739 - 00:35:02:629] **Speaker 1:** So you of X Y equal to A X +
[00:35:02:629 - 00:35:04:510] **Speaker 1:** B multiplied by CY + D.
[00:35:04:870 - 00:35:07:489] **Speaker 1:** We, we know it's a solution to that PDE again,
[00:35:07:909 - 00:35:10:110] **Speaker 1:** but is it a solution to the boundary condition?
[00:35:10:389 - 00:35:13:590] **Speaker 1:** So the boundary condition at Y equals 0.
[00:35:14:639 - 00:35:17:820] **Speaker 1:** So at the bottom edge is equal to 0.
[00:35:19:030 - 00:35:21:379] **Speaker 1:** So perhaps this represents some membrane.
[00:35:21:610 - 00:35:24:860] **Speaker 1:** Uh, we've got some thin material that is being propped
[00:35:24:860 - 00:35:27:000] **Speaker 1:** up on the right-hand side with a sign function.
[00:35:27:800 - 00:35:31:379] **Speaker 1:** And Yeah, we're just solving the steady-state solution.
[00:35:32:169 - 00:35:34:379] **Speaker 1:** So 0 on the left, top and bottom, and then
[00:35:34:379 - 00:35:36:379] **Speaker 1:** the sine function on the, on the right.
[00:35:38:600 - 00:35:42:679] **Speaker 1:** So subshooting in Our boundary condition, you.
[00:35:44:000 - 00:35:46:679] **Speaker 1:** Of X Y equals 0.
[00:35:50:330 - 00:35:53:689] **Speaker 1:** It applies for all X values, so we retain A
[00:35:53:689 - 00:35:55:770] **Speaker 1:** X plus B.
[00:35:57:959 - 00:36:00:879] **Speaker 1:** We're substituting Y equal to 0 because we're now looking
[00:36:00:879 - 00:36:02:620] **Speaker 1:** just along the bottom edge.
[00:36:03:120 - 00:36:04:479] **Speaker 1:** So we're left with D.
[00:36:10:959 - 00:36:14:679] **Speaker 1:** So we need to equate this expression A + B
[00:36:14:679 - 00:36:15:949] **Speaker 1:** multiplied by D equal to 0.
[00:36:18:100 - 00:36:22:489] **Speaker 1:** Uh This is really only going to be true if
[00:36:22:489 - 00:36:23:850] **Speaker 1:** D is equal to 0.
[00:36:24:209 - 00:36:26:530] **Speaker 1:** We could set A and B equal to 0 to
[00:36:26:530 - 00:36:29:330] **Speaker 1:** achieve the same, but that's just going to set you
[00:36:29:330 - 00:36:30:449] **Speaker 1:** equal to 0 everywhere.
[00:36:31:790 - 00:36:33:989] **Speaker 1:** So the argument here is that D is equal to
[00:36:33:989 - 00:36:34:429] **Speaker 1:** 0.
[00:36:38:790 - 00:36:40:679] **Speaker 1:** We're gonna look at the boundary condition on the left-hand
[00:36:40:679 - 00:36:40:939] **Speaker 1:** side.
[00:36:41:280 - 00:36:42:060] **Speaker 1:** OK, zoom out.
[00:36:43:080 - 00:36:43:520] **Speaker 1:** Very good.
[00:36:44:699 - 00:36:45:770] **Speaker 1:** So boundary on the left.
[00:36:46:750 - 00:36:49:389] **Speaker 1:** You at X equals 0.
[00:36:50:120 - 00:36:50:540] **Speaker 1:** Why?
[00:36:52:340 - 00:36:54:340] **Speaker 1:** Substitute, we've got B.
[00:36:56:239 - 00:36:59:320] **Speaker 1:** Multiplied by C Y plus D.
[00:37:01:459 - 00:37:02:350] **Speaker 1:** Equal to 0.
[00:37:03:820 - 00:37:07:699] **Speaker 1:** Same argument, we're going to set B equal to 0.
[00:37:08:459 - 00:37:11:800] **Speaker 1:** Last of all, U X Y equal 1.
[00:37:12:340 - 00:37:19:620] **Speaker 1:** So at the top we've got, I see Multiplied by
[00:37:19:620 - 00:37:22:110] **Speaker 1:** X because we said D and B is 0, we
[00:37:22:110 - 00:37:24:270] **Speaker 1:** can just get rid of those for now and we've
[00:37:24:270 - 00:37:27:989] **Speaker 1:** got AC times X times 1.
[00:37:30:979 - 00:37:32:540] **Speaker 1:** We want it to be equal to 0 on that
[00:37:32:540 - 00:37:35:600] **Speaker 1:** top face, uh, so maybe the displacement 0.
[00:37:37:909 - 00:37:39:260] **Speaker 1:** Which means that AC.
[00:37:40:030 - 00:37:40:560] **Speaker 1:** As equal as they are.
[00:37:44:820 - 00:37:49:550] **Speaker 1:** So essentially what we've done is Our displacement field U
[00:37:49:969 - 00:37:51:149] **Speaker 1:** varying in X and Y.
[00:37:53:169 - 00:37:55:129] **Speaker 1:** is identical to 0.
[00:37:56:840 - 00:37:59:320] **Speaker 1:** I've said all of those, those consonants.
[00:38:00:169 - 00:38:00:550] **Speaker 1:** Uh.
[00:38:01:280 - 00:38:01:659] **Speaker 1:** A 0.
[00:38:03:689 - 00:38:14:129] **Speaker 1:** Which is a trivial Solution Of the PDU Our PDE
[00:38:14:129 - 00:38:15:649] **Speaker 1:** is second-order derivative in X.
[00:38:16:500 - 00:38:21:199] **Speaker 1:** If we differentiate 0 twice, we get 0 and differentiate
[00:38:21:199 - 00:38:22:540] **Speaker 1:** the y twice 0.
[00:38:22:659 - 00:38:24:379] **Speaker 1:** So of course it's a solution to the PDE.
[00:38:25:610 - 00:38:28:330] **Speaker 1:** But it's not going to be matching our right-hand boundary
[00:38:28:330 - 00:38:31:110] **Speaker 1:** condition, which is the sign profile, a sign 2 paiwa.
[00:39:09:229 - 00:39:12:669] **Speaker 1:** Who All right.
[00:39:14:040 - 00:39:16:199] **Speaker 1:** It's a bit painful, but there's 2 more.
[00:39:17:379 - 00:39:21:080] **Speaker 1:** Um, so the next case, we're gonna look through.
[00:39:22:090 - 00:39:24:449] **Speaker 1:** Is the sin and cosine terms in X and the
[00:39:24:449 - 00:39:25:649] **Speaker 1:** exponentials in y.
[00:39:26:040 - 00:39:27:649] **Speaker 1:** So again, we know this is a solution to the
[00:39:27:649 - 00:39:28:159] **Speaker 1:** Lapace.
[00:39:28:340 - 00:39:30:649] **Speaker 1:** Is it satisfying all of our boundary conditions?
[00:39:31:600 - 00:39:33:879] **Speaker 1:** So first of all, the one on the bottom, so
[00:39:33:879 - 00:39:39:149] **Speaker 1:** Y equals 0, U of X, Y equals 0 is
[00:39:39:149 - 00:39:39:790] **Speaker 1:** equal to.
[00:39:41:689 - 00:39:43:030] **Speaker 1:** A sin mu x.
[00:39:46:919 - 00:39:50:169] **Speaker 1:** Plus B cos m X.
[00:39:52:370 - 00:39:54:689] **Speaker 1:** The exact boundary condition applies to the whole length of
[00:39:54:689 - 00:39:55:909] **Speaker 1:** that, that bottom edge.
[00:39:56:750 - 00:39:59:350] **Speaker 1:** And we're replacing Y with 0.
[00:39:59:629 - 00:40:02:489] **Speaker 1:** So exponential of 0 is going to be 1.
[00:40:03:189 - 00:40:05:050] **Speaker 1:** So C multiplied by 1.
[00:40:09:010 - 00:40:10:340] **Speaker 1:** We left with C + D.
[00:40:12:050 - 00:40:14:449] **Speaker 1:** And we're told that the displacement on that bottom edge
[00:40:14:449 - 00:40:15:250] **Speaker 1:** is equal to 0.
[00:40:22:360 - 00:40:24:159] **Speaker 1:** And just to be explicit, that's for all the X
[00:40:24:159 - 00:40:25:560] **Speaker 1:** values along that edge.
[00:40:27:070 - 00:40:29:239] **Speaker 1:** So for that to be true, we know sine of
[00:40:29:239 - 00:40:32:719] **Speaker 1:** mux cos mux, these are those sine and cosine functions
[00:40:32:719 - 00:40:34:590] **Speaker 1:** that are varying, they're non-zero.
[00:40:35:239 - 00:40:37:459] **Speaker 1:** So out of these.
[00:40:38:709 - 00:40:42:050] **Speaker 1:** Two expressions Uh, if we look at the 2nd bracket.
[00:40:43:939 - 00:40:46:290] **Speaker 1:** C + D has to be equal to 0 for
[00:40:46:290 - 00:40:47:840] **Speaker 1:** this equation to hold.
[00:40:50:989 - 00:40:53:790] **Speaker 1:** So C is equal to minus D.
[00:40:57:629 - 00:40:59:330] **Speaker 1:** Is that clear or is that jumping?
[00:41:01:479 - 00:41:02:040] **Speaker 1:** That's OK.
[00:41:02:790 - 00:41:04:149] **Speaker 1:** I just jump, it's OK, good.
[00:41:05:830 - 00:41:07:270] **Speaker 1:** All right, so you.
[00:41:08:159 - 00:41:09:179] **Speaker 1:** X Y.
[00:41:09:399 - 00:41:13:750] **Speaker 1:** I quite like to, uh, write out the latest information,
[00:41:13:800 - 00:41:15:919] **Speaker 1:** I guess, for the, the solution.
[00:41:16:320 - 00:41:18:120] **Speaker 1:** Otherwise, it can get a little bit tricky to keep
[00:41:18:120 - 00:41:18:899] **Speaker 1:** track of everything.
[00:41:19:239 - 00:41:21:760] **Speaker 1:** So we've evaluated C equal to minus D.
[00:41:22:000 - 00:41:24:629] **Speaker 1:** So we're going to insert that or substitute it into
[00:41:24:629 - 00:41:25:419] **Speaker 1:** our equation.
[00:41:25:850 - 00:41:30:610] **Speaker 1:** So you have XY is equal to a sin mu
[00:41:30:610 - 00:41:34:280] **Speaker 1:** x plus B cos mu x.
[00:41:39:699 - 00:41:41:600] **Speaker 1:** Uh, the second term and why.
[00:41:42:659 - 00:41:45:540] **Speaker 1:** D is equal to minus C, so we're just left
[00:41:45:540 - 00:41:46:320] **Speaker 1:** with C.
[00:41:47:889 - 00:41:52:770] **Speaker 1:** E to the muy minus CE to the minus muy.
[00:41:55:169 - 00:41:58:899] **Speaker 1:** So C is a constant in front of both of
[00:41:58:899 - 00:41:59:300] **Speaker 1:** those terms.
[00:41:59:340 - 00:42:02:080] **Speaker 1:** So we can take that outside of the, the bracket.
[00:42:02:969 - 00:42:04:939] **Speaker 1:** And we're going to combine them with the A and
[00:42:04:939 - 00:42:08:239] **Speaker 1:** B coefficients and label them A.
[00:42:11:729 - 00:42:16:129] **Speaker 1:** So we've got A sin U X plus B.
[00:42:17:270 - 00:42:19:229] **Speaker 1:** Cosm X.
[00:42:22:520 - 00:42:27:199] **Speaker 1:** Multiplied by E to the muy minus E to the
[00:42:27:199 - 00:42:28:320] **Speaker 1:** minus muy.
[00:42:32:770 - 00:42:34:189] **Speaker 1:** And we've caught a prime.
[00:42:36:050 - 00:42:37:389] **Speaker 1:** Equal to AC.
[00:42:39:000 - 00:42:40:169] **Speaker 1:** And B.
[00:42:41:229 - 00:42:43:209] **Speaker 1:** Equal to Easy.
[00:42:44:840 - 00:42:46:399] **Speaker 1:** So we're just grouping those coefficients.
[00:42:49:080 - 00:42:51:090] **Speaker 1:** Uh, so it's much easier to keep track of everything.
[00:42:53:389 - 00:43:04:389] **Speaker 1:** Right So we've got one To Um, coefficients A and
[00:43:04:389 - 00:43:05:570] **Speaker 1:** B are unknown.
[00:43:05:949 - 00:43:08:550] **Speaker 1:** Mu is also unknown, uh, term as well.
[00:43:08:709 - 00:43:09:729] **Speaker 1:** So we've got three terms.
[00:43:11:379 - 00:43:15:250] **Speaker 1:** To figure out The next boundary condition we'll look at
[00:43:15:250 - 00:43:17:870] **Speaker 1:** is on the left-hand side, so X equals 0.
[00:43:21:159 - 00:43:25:520] **Speaker 1:** Very similar technique, we're going to substitute in our expression
[00:43:25:520 - 00:43:25:919] **Speaker 1:** for you.
[00:43:27:709 - 00:43:31:550] **Speaker 1:** So X equals 0, sin of 0 is going to
[00:43:31:550 - 00:43:32:169] **Speaker 1:** be 0.
[00:43:34:580 - 00:43:36:399] **Speaker 1:** And cosine of 0.
[00:43:37:100 - 00:43:38:300] **Speaker 1:** Is going to equal one.
[00:43:39:290 - 00:43:42:729] **Speaker 1:** So we're just left with B from that first bracket.
[00:43:46:159 - 00:43:49:639] **Speaker 1:** Multiplied by our exponential terms with Y's.
[00:43:59:639 - 00:44:02:020] **Speaker 1:** And again, because this is on the left-hand side, it
[00:44:02:199 - 00:44:04:629] **Speaker 1:** needs to be satisfied for all y values, so along
[00:44:04:629 - 00:44:05:479] **Speaker 1:** that whole edge.
[00:44:06:179 - 00:44:07:899] **Speaker 1:** So for all, why?
[00:44:12:199 - 00:44:16:719] **Speaker 1:** Now, in our derivation of those general solutions, we said
[00:44:16:719 - 00:44:17:159] **Speaker 1:** new.
[00:44:18:020 - 00:44:20:040] **Speaker 1:** Uh, is not zero for this case.
[00:44:20:929 - 00:44:25:479] **Speaker 1:** So we know that We can't make this bracket or
[00:44:25:479 - 00:44:27:399] **Speaker 1:** this, this, um, expression equal to zero.
[00:44:27:479 - 00:44:31:219] **Speaker 1:** We can't have E to the power of Y minus
[00:44:31:219 - 00:44:34:600] **Speaker 1:** E minus something else times Y equal to 0.
[00:44:35:500 - 00:44:36:929] **Speaker 1:** If mu was equal to 0, it would be 1
[00:44:36:929 - 00:44:38:080] **Speaker 1:** minus 1, which is fine.
[00:44:39:179 - 00:44:42:199] **Speaker 1:** The only way that we can enforce this boundary condition.
[00:44:43:110 - 00:44:45:469] **Speaker 1:** is to set B equal to 0.
[00:44:53:360 - 00:44:54:340] **Speaker 1:** Does that make sense?
[00:44:54:459 - 00:44:54:770] **Speaker 1:** Yeah.
[00:44:58:459 - 00:45:04:120] **Speaker 1:** Who Alright, so the 3rd band, well, we could write
[00:45:04:120 - 00:45:05:600] **Speaker 1:** out the U of Xy again.
[00:45:08:879 - 00:45:11:000] **Speaker 1:** So we said B 0, so we're just left with
[00:45:11:000 - 00:45:11:520] **Speaker 1:** A.
[00:45:12:800 - 00:45:17:679] **Speaker 1:** Sign Of mu x multiplied by our exponential terms e
[00:45:17:679 - 00:45:20:399] **Speaker 1:** to muy minus E to minus muy.
[00:45:22:850 - 00:45:25:840] **Speaker 1:** So we're slowly making it simplified.
[00:45:27:120 - 00:45:29:750] **Speaker 1:** The last boundary condition on the top, so Y equal
[00:45:29:750 - 00:45:30:179] **Speaker 1:** to 1.
[00:45:33:540 - 00:45:36:459] **Speaker 1:** You at X Y equal to 1.
[00:45:39:429 - 00:45:41:219] **Speaker 1:** So we've got this expression A.
[00:45:43:389 - 00:45:45:729] **Speaker 1:** Sign of mu x.
[00:45:49:659 - 00:45:51:669] **Speaker 1:** And we said Y is equal to 1.
[00:45:52:110 - 00:45:54:739] **Speaker 1:** So we're going to substitute that into our terms.
[00:45:54:820 - 00:45:57:820] **Speaker 1:** So E to the power of mu minus E to
[00:45:57:820 - 00:45:59:580] **Speaker 1:** the minus mu.
[00:46:02:969 - 00:46:04:659] **Speaker 1:** Equal to 0.
[00:46:06:550 - 00:46:08:949] **Speaker 1:** So the displacement on that top is fixed, fixed at
[00:46:08:949 - 00:46:11:739] **Speaker 1:** 0, and this is true for all X values.
[00:46:11:939 - 00:46:12:850] **Speaker 1:** So on the whole edge.
[00:46:18:659 - 00:46:21:229] **Speaker 1:** So sin of mu x, again mu is not zero,
[00:46:21:459 - 00:46:23:659] **Speaker 1:** X is varying from 0 up to 2.
[00:46:23:870 - 00:46:24:989] **Speaker 1:** That's that spatial coordinate.
[00:46:25:659 - 00:46:28:550] **Speaker 1:** So sin term is not going to be zero.
[00:46:29:540 - 00:46:32:860] **Speaker 1:** E to the power of a non-zero number and E
[00:46:32:860 - 00:46:36:100] **Speaker 1:** to the minus not zero number is gonna be non-zero.
[00:46:37:409 - 00:46:39:510] **Speaker 1:** So the only way that we can make this true
[00:46:39:850 - 00:46:41:129] **Speaker 1:** is to set a prime.
[00:46:43:209 - 00:46:43:939] **Speaker 1:** Equal to 0.
[00:46:46:449 - 00:46:58:310] **Speaker 1:** So again, You Of X and Y is just 0,
[00:46:58:810 - 00:46:59:530] **Speaker 1:** is not.
[00:47:00:939 - 00:47:02:820] **Speaker 1:** A useful solution.
[00:47:11:850 - 00:47:11:969] **Speaker 1:** Cool.
[00:47:12:040 - 00:47:14:129] **Speaker 1:** So 2 out of 3, we've done it in this
[00:47:14:129 - 00:47:18:409] **Speaker 1:** order on purpose because Just to identify that those first
[00:47:18:409 - 00:47:19:110] **Speaker 1:** two don't work.
[00:47:19:409 - 00:47:21:459] **Speaker 1:** The last one should work with any luck.
[00:47:21:969 - 00:47:25:520] **Speaker 1:** Um, So we've got exponentials with X and sine and
[00:47:25:520 - 00:47:26:439] **Speaker 1:** cosine with Y.
[00:47:27:169 - 00:47:30:449] **Speaker 1:** So the boundary condition on the lower edge again, we've
[00:47:30:449 - 00:47:31:110] **Speaker 1:** got you.
[00:47:32:350 - 00:47:34:209] **Speaker 1:** And X Y equals 0.
[00:47:35:370 - 00:47:38:040] **Speaker 1:** Substituting Y equal to 0, we've got sin of 0
[00:47:38:399 - 00:47:39:479] **Speaker 1:** and cosine of 0.
[00:47:41:729 - 00:47:44:510] **Speaker 1:** So we've got AE to the mu x plus BE
[00:47:44:510 - 00:47:47:729] **Speaker 1:** to the minus mu x multiplied by D.
[00:47:53:219 - 00:47:55:080] **Speaker 1:** Same argument, D is equal to 0.
[00:47:55:909 - 00:47:58:790] **Speaker 1:** So we can update U of X and Y equal
[00:47:58:790 - 00:48:05:149] **Speaker 1:** to AE to the mu X plus B E minus
[00:48:05:149 - 00:48:05:790] **Speaker 1:** mu X.
[00:48:08:120 - 00:48:10:320] **Speaker 1:** Time sign of new Y.
[00:48:11:590 - 00:48:13:350] **Speaker 1:** So I've just substituted D equal to 0 into our
[00:48:13:350 - 00:48:13:969] **Speaker 1:** equation.
[00:48:14:429 - 00:48:17:590] **Speaker 1:** We've done that same trick AC, um.
[00:48:18:560 - 00:48:20:840] **Speaker 1:** And BC equal to A B.
[00:48:33:419 - 00:48:35:419] **Speaker 1:** The next boundary condition we're gonna look at is the
[00:48:35:419 - 00:48:37:159] **Speaker 1:** one at the top, so Y 41.
[00:48:39:020 - 00:48:43:629] **Speaker 1:** So arguably doesn't matter too much which order of boundary
[00:48:43:629 - 00:48:45:149] **Speaker 1:** conditions you do it in, but you might find that
[00:48:45:149 - 00:48:48:830] **Speaker 1:** one works better than the others, um, or it might,
[00:48:49:179 - 00:48:50:040] **Speaker 1:** might not be possible.
[00:48:50:149 - 00:48:52:149] **Speaker 1:** So just be careful of which boundary conditions you're starting
[00:48:52:149 - 00:48:52:389] **Speaker 1:** with.
[00:48:52:790 - 00:48:55:590] **Speaker 1:** Generally starting with the zeros makes, makes the most sense,
[00:48:55:669 - 00:48:57:149] **Speaker 1:** but I'll talk more about that later.
[00:48:58:570 - 00:49:01:449] **Speaker 1:** But for this case, we're going through the top boundary
[00:49:01:449 - 00:49:02:010] **Speaker 1:** condition next.
[00:49:02:270 - 00:49:05:739] **Speaker 1:** So we're substituting in U of X Y equals 1.
[00:49:08:699 - 00:49:11:070] **Speaker 1:** So Y equal to 1, we've got sin of mu.
[00:49:11:949 - 00:49:13:560] **Speaker 1:** And then the expressions.
[00:49:13:760 - 00:49:17:239] **Speaker 1:** So we've got A E to the mu X plus
[00:49:17:239 - 00:49:22:360] **Speaker 1:** B E to the minus mu x, sin of m.
[00:49:35:879 - 00:49:39:030] **Speaker 1:** So, What, what can we say here?
[00:49:54:280 - 00:49:55:649] **Speaker 1:** How do we make this equal to 0?
[00:50:05:179 - 00:50:05:199] **Speaker 1:** That is.
[00:50:07:310 - 00:50:09:010] **Speaker 1:** So sin mu is a constant value.
[00:50:11:280 - 00:50:14:189] **Speaker 1:** So we could set sin m equal to 0.
[00:50:21:389 - 00:50:23:280] **Speaker 1:** Because I don't think we can set the first term
[00:50:23:280 - 00:50:23:719] **Speaker 1:** to 0.
[00:50:23:879 - 00:50:25:159] **Speaker 1:** I can't think of a way to do that.
[00:50:25:939 - 00:50:28:169] **Speaker 1:** So this equation can only be satisfied.
[00:50:33:620 - 00:50:35:530] **Speaker 1:** For all X values.
[00:50:40:870 - 00:50:44:709] **Speaker 1:** If sin of mu is equal to 0.
[00:50:52:010 - 00:50:53:530] **Speaker 1:** So, we've run out of time.
[00:50:53:610 - 00:50:56:129] **Speaker 1:** I was having fun, but um I'll let you.
[00:50:57:070 - 00:50:59:189] **Speaker 1:** You can try to finish it off, but we'll finish
[00:50:59:189 - 00:51:02:189] **Speaker 1:** it off on, on Monday, um.
[00:51:03:399 - 00:51:04:949] **Speaker 0:** Yeah, oh.
[00:51:34:020 - 00:51:36:780] **Speaker 0:** Hey What is everyone's writing in the book.
[00:51:36:899 - 00:51:38:189] **Speaker 2:** Like, are we allowed to bring the book in the
[00:51:38:189 - 00:51:41:139] **Speaker 2:** chairs or something, or, um, no, but I've, I've left
[00:51:41:139 - 00:51:42:159] **Speaker 1:** like gaps.
[00:51:42:899 - 00:51:44:459] **Speaker 1:** So their idea is that you're sort of learning while
[00:51:44:459 - 00:51:47:979] **Speaker 1:** you're writing, but the exam's closed book, and I'll give
[00:51:47:979 - 00:51:48:739] **Speaker 1:** you a formula sheet.
[00:51:49:300 - 00:51:50:020] **Speaker 2:** I'm on my iPad.
[00:51:50:620 - 00:51:52:179] **Speaker 1:** Oh yeah, yeah, yeah, yeah, yeah, yeah, yeah, that's fine,
[00:51:52:260 - 00:51:52:419] **Speaker 1:** yeah.
[00:52:00:149 - 00:52:03:060] **Speaker 0:** I I.
[00:52:04:919 - 00:52:09:600] **Speaker 0:** I Oh.
[00:52:15:320 - 00:52:23:379] **Speaker 0:** People dressed No worries.
[00:52:57:610 - 00:53:03:270] **Speaker 0:** That was a Oh, you made me laugh.
[00:53:09:209 - 00:53:12:250] **Speaker 0:** What I give it to you just give us a.
[00:53:13:379 - 00:53:13:870] **Speaker 0:** That's very true.
[00:54:50:179 - 00:54:52:739] **Speaker 0:** Yeah that.
[00:54:57:100 - 00:54:57:300] **Speaker 0:** Cool.

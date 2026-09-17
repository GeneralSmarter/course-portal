# ENME302-26S2 Lecture 30 native Echo transcript

Date: September 16, 2026 11:00am-11:55am
Transcript type: native Echo automated transcript.

[00:00:18:770 - 00:00:20:389] **Speaker 0:** Uh, good morning, we'll make a start.
[00:00:22:979 - 00:00:24:459] **Speaker 0:** Is that mic, OK?
[00:00:24:540 - 00:00:25:639] **Speaker 0:** Is that mic working?
[00:00:26:489 - 00:00:27:360] **Speaker 1:** It's not working.
[00:00:43:729 - 00:00:46:680] **Speaker 0:** Is the mic, oh, the mic is working, OK, cool.
[00:00:47:180 - 00:00:47:500] **Speaker 0:** Alright.
[00:00:48:299 - 00:00:53:680] **Speaker 0:** So, um, so today we'll keep going with chapter 5.
[00:00:54:619 - 00:00:58:759] **Speaker 0:** are there any questions before we get started?
[00:01:03:020 - 00:01:05:730] **Speaker 0:** Um, based on some feedback from the quiz, I, I
[00:01:05:730 - 00:01:09:489] **Speaker 0:** did loosen some of the tolerances for the question 4
[00:01:09:489 - 00:01:10:279] **Speaker 0:** and 5.
[00:01:10:980 - 00:01:13:319] **Speaker 0:** you still need within 2% to get full marks, but,
[00:01:13:419 - 00:01:18:080] **Speaker 0:** um, I had a 10 and 20% option to get
[00:01:18:330 - 00:01:20:400] **Speaker 0:** half the marks and a quarter of the marks.
[00:01:20:900 - 00:01:24:059] **Speaker 0:** Um, and same for question 5, 25% and 50%, so.
[00:01:24:879 - 00:01:27:639] **Speaker 0:** That's very sensitive to the mesh resolution for the, the
[00:01:27:639 - 00:01:30:319] **Speaker 0:** stress, uh, calculation for that feeder clamp.
[00:01:30:839 - 00:01:33:980] **Speaker 0:** Um, so that impacted 50 or 80 odd students.
[00:01:34:290 - 00:01:41:400] **Speaker 0:** Um, there's questions on Including U of X and Y
[00:01:41:400 - 00:01:43:220] **Speaker 0:** for the separation of variables, so I've just included that
[00:01:43:220 - 00:01:43:620] **Speaker 0:** in the answer.
[00:01:43:699 - 00:01:45:779] **Speaker 0:** It only impacted two or three students.
[00:01:45:900 - 00:01:48:019] **Speaker 0:** Don't worry too much, um, but you're just getting marks
[00:01:48:019 - 00:01:48:480] **Speaker 0:** for that.
[00:01:48:860 - 00:01:51:099] **Speaker 0:** I haven't gone through and done partial credit for the
[00:01:51:099 - 00:01:51:860] **Speaker 0:** separation of variables.
[00:01:51:930 - 00:01:54:580] **Speaker 0:** There's too many permutations to, to look at, as you
[00:01:54:580 - 00:01:55:680] **Speaker 0:** can maybe appreciate.
[00:01:56:139 - 00:01:58:300] **Speaker 0:** Um, so we don't see you working, so it's a
[00:01:58:300 - 00:02:00:129] **Speaker 0:** bit hard to give partial credit for some of those
[00:02:00:129 - 00:02:02:449] **Speaker 0:** questions, which is a bit rough, to be honest, but,
[00:02:02:540 - 00:02:05:000] **Speaker 0:** um, it's, we can't do too much about that.
[00:02:05:610 - 00:02:09:630] **Speaker 0:** Uh, when you have, sorry, um, so you can.
[00:02:10:410 - 00:02:12:610] **Speaker 0:** Check that your answer is correct, so I've gone through
[00:02:12:610 - 00:02:14:899] **Speaker 0:** that a couple of times, uh, and towards the end
[00:02:14:899 - 00:02:17:009] **Speaker 0:** of the lecture, I'll also show you how to calculate
[00:02:17:009 - 00:02:21:449] **Speaker 0:** it in console, and just compare your analytical and numerical,
[00:02:21:729 - 00:02:23:029] **Speaker 0:** uh, scheme as well.
[00:02:24:789 - 00:02:26:009] **Speaker 0:** So it's all that quiz stuff.
[00:02:26:130 - 00:02:29:089] **Speaker 0:** So the quiz 3, to avoid giving you marks and
[00:02:29:089 - 00:02:31:929] **Speaker 0:** then changing them, I'll hide the marks or results until
[00:02:31:929 - 00:02:33:070] **Speaker 0:** I have a chance to go through them.
[00:02:33:729 - 00:02:35:800] **Speaker 0:** Uh, so we'll release those on the Monday.
[00:02:36:050 - 00:02:37:970] **Speaker 0:** So if you don't see your marks, you should be
[00:02:37:970 - 00:02:42:009] **Speaker 0:** having your weekend anyway, um, so don't think about work
[00:02:42:009 - 00:02:45:169] **Speaker 0:** too much during the weekend, if you can, um.
[00:02:46:429 - 00:02:48:470] **Speaker 0:** And we'll go through the quiz together on the Monday.
[00:02:51:160 - 00:02:55:279] **Speaker 0:** Um, and the tolerance on quiz 3, I went through
[00:02:55:279 - 00:02:56:179] **Speaker 0:** that on Monday.
[00:02:56:360 - 00:03:00:660] **Speaker 0:** Um, the questions are looking at the uh circular domain
[00:03:00:660 - 00:03:03:119] **Speaker 0:** and we were looking at a membrane and applying a
[00:03:03:119 - 00:03:04:000] **Speaker 0:** pressure distribution.
[00:03:04:850 - 00:03:09:610] **Speaker 0:** So the solution, especially the, the, the, uh, position of
[00:03:09:610 - 00:03:13:110] **Speaker 0:** the peak displacement is very sensitive to the mesh resolution.
[00:03:13:529 - 00:03:17:229] **Speaker 0:** So, This week in the lab, we're quite focused on
[00:03:17:429 - 00:03:20:779] **Speaker 0:** discretization and mesh convergence, so we're looking at the simply
[00:03:20:779 - 00:03:21:389] **Speaker 0:** supported beam.
[00:03:22:289 - 00:03:24:750] **Speaker 0:** And we're looking at mesh convergence using a parameter sweep.
[00:03:25:509 - 00:03:28:059] **Speaker 0:** So I want you to take away, hopefully uh mesh
[00:03:28:059 - 00:03:28:750] **Speaker 0:** convergence.
[00:03:29:470 - 00:03:33:509] **Speaker 0:** Um, expertise and apply that to the, the question in
[00:03:33:509 - 00:03:34:080] **Speaker 0:** the quiz.
[00:03:34:500 - 00:03:37:059] **Speaker 0:** So I'll keep the tolerance reasonably tight for that, that
[00:03:37:059 - 00:03:37:300] **Speaker 0:** question.
[00:03:39:360 - 00:03:41:720] **Speaker 0:** All right, any, any questions now that you've had a
[00:03:41:720 - 00:03:43:399] **Speaker 0:** chance to think about 302?
[00:03:46:250 - 00:03:47:809] **Speaker 0:** No, all straightforward.
[00:03:47:889 - 00:03:48:520] **Speaker 0:** Alright, cool.
[00:03:48:929 - 00:03:49:330] **Speaker 0:** So.
[00:03:50:080 - 00:03:52:360] **Speaker 0:** Last time we were looking through and the suppression of
[00:03:52:360 - 00:03:55:320] **Speaker 0:** variables for the heat equation, we found that it was
[00:03:55:320 - 00:03:58:440] **Speaker 0:** very similar and we looked at the dimensions of the
[00:03:58:440 - 00:03:59:240] **Speaker 0:** heat diversivity.
[00:04:00:130 - 00:04:02:910] **Speaker 0:** Expression, so it's a diffusion rate metre squad per second.
[00:04:05:710 - 00:04:08:100] **Speaker 0:** Now we're gonna spend a little bit of time about
[00:04:09:070 - 00:04:12:000] **Speaker 0:** discussing dimensionless PDEs or dimensionless variables.
[00:04:12:320 - 00:04:14:880] **Speaker 0:** So you might have come across the concept of non-dimensionalisation
[00:04:14:880 - 00:04:17:880] **Speaker 0:** in other courses already, but we'll just cover that concept
[00:04:17:880 - 00:04:18:160] **Speaker 0:** here.
[00:04:18:959 - 00:04:21:049] **Speaker 0:** So we're gonna show how our PDEs can be written
[00:04:21:049 - 00:04:22:290] **Speaker 0:** in dimensionless form.
[00:04:22:450 - 00:04:26:890] **Speaker 0:** So instead of dimensions with metres, um, Pascal's, Newtons, they'll
[00:04:26:890 - 00:04:27:769] **Speaker 0:** be dimensionless.
[00:04:29:619 - 00:04:33:070] **Speaker 0:** So if we write a problem and dimensionless form, Our
[00:04:33:070 - 00:04:36:589] **Speaker 0:** equations from physics or engineering, chemistry, biology, etc.
[00:04:36:869 - 00:04:38:019] **Speaker 0:** can look quite similar.
[00:04:38:309 - 00:04:40:309] **Speaker 0:** They have the same structure, they have the same equation.
[00:04:41:149 - 00:04:42:510] **Speaker 0:** Uh, and no units.
[00:04:44:010 - 00:04:46:450] **Speaker 0:** So it can be very useful to reduce the number
[00:04:46:450 - 00:04:47:760] **Speaker 0:** of independent variables.
[00:04:48:209 - 00:04:51:130] **Speaker 0:** So those who have done fluids courses, you'll, you'll recognise
[00:04:51:130 - 00:04:52:250] **Speaker 0:** the Reynolds number.
[00:04:52:630 - 00:04:55:209] **Speaker 0:** So it's a way of representing the flow behaviour.
[00:04:55:529 - 00:04:58:019] **Speaker 0:** So that first X-ray showed you the cylinder and crossflow.
[00:04:58:130 - 00:05:00:799] **Speaker 0:** We saw turbulent vortices downstream of the cylinder.
[00:05:01:089 - 00:05:02:929] **Speaker 0:** If we had a really low Reynolds number, so if
[00:05:02:929 - 00:05:08:250] **Speaker 0:** it was, um, slow flow, maybe very viscous, uh, then
[00:05:08:250 - 00:05:11:869] **Speaker 0:** we would expect to have, um, Uh, the flow to
[00:05:11:869 - 00:05:14:160] **Speaker 0:** be fully attached around the cylinder and you have quite
[00:05:14:160 - 00:05:15:140] **Speaker 0:** a different behaviour.
[00:05:15:799 - 00:05:18:640] **Speaker 0:** So the Reynolds number is a nice dimensionless way of
[00:05:18:640 - 00:05:20:799] **Speaker 0:** representing the flow, uh, features.
[00:05:22:410 - 00:05:24:700] **Speaker 0:** So identifying those key dominating physics.
[00:05:25:320 - 00:05:27:559] **Speaker 0:** So we're gonna consider the heat equation and instead of
[00:05:27:559 - 00:05:30:790] **Speaker 0:** having these dimension quantities, the temperature being in degrees Celsius
[00:05:30:790 - 00:05:34:440] **Speaker 0:** or Kelvin, uh, thermal diffusivity in metres squared per second,
[00:05:34:929 - 00:05:37:339] **Speaker 0:** and our domain in time and space.
[00:05:38:429 - 00:05:43:540] **Speaker 0:** We have these Uh, units that we looked at yesterday,
[00:05:43:739 - 00:05:46:220] **Speaker 0:** so Kelvin per second is the unit of each term.
[00:05:46:420 - 00:05:49:220] **Speaker 0:** They need to be dimensionally consistent between the, uh, terms
[00:05:49:220 - 00:05:50:079] **Speaker 0:** in an equation.
[00:05:50:790 - 00:05:52:899] **Speaker 0:** And we want to make this equation dimensionless.
[00:05:55:700 - 00:05:58:559] **Speaker 0:** So what we're gonna do is introduce some dimensionless variables,
[00:05:58:570 - 00:06:01:660] **Speaker 0:** and then we're gonna scale all of our variables by
[00:06:01:660 - 00:06:02:940] **Speaker 0:** these dimensionless variables.
[00:06:05:329 - 00:06:07:570] **Speaker 0:** So the dimensionless variable for temperature is going to be
[00:06:07:570 - 00:06:11:109] **Speaker 0:** scaled I, some characteristic temperature T0.
[00:06:12:179 - 00:06:15:980] **Speaker 0:** Our coordinate scale is going to be normalised or non-dimensionalized
[00:06:15:980 - 00:06:18:859] **Speaker 0:** on a length scale L and time by T 00.
[00:06:20:260 - 00:06:23:010] **Speaker 0:** So we've got length scale, time, and temperature scales.
[00:06:24:529 - 00:06:27:690] **Speaker 0:** So the length scale might be the length of our
[00:06:27:690 - 00:06:28:089] **Speaker 0:** rod.
[00:06:28:290 - 00:06:30:829] **Speaker 0:** So that's the application that we looked at previously.
[00:06:31:369 - 00:06:32:489] **Speaker 0:** So that was 80 centimetres.
[00:06:33:209 - 00:06:37:609] **Speaker 0:** Uh, the temperature T0 could be scaled by the initial
[00:06:37:609 - 00:06:38:049] **Speaker 0:** temperature.
[00:06:38:209 - 00:06:39:829] **Speaker 0:** So that was 100 °C.
[00:06:40:709 - 00:06:42:950] **Speaker 0:** And the timescale is a little bit trickier, and we'll
[00:06:42:950 - 00:06:43:709] **Speaker 0:** come to that shortly.
[00:06:46:070 - 00:06:51:170] **Speaker 0:** So we've established these dimensionless variables, t tilda, X tilda,
[00:06:51:260 - 00:06:51:970] **Speaker 0:** and T tilda.
[00:06:52:190 - 00:06:56:390] **Speaker 0:** So tilda denoting the dimensionless uh counterpart to the, the
[00:06:56:390 - 00:06:57:450] **Speaker 0:** dimension variable.
[00:06:58:350 - 00:07:02:070] **Speaker 0:** We rearrange for the dimensional variable, so T is equal
[00:07:02:070 - 00:07:05:859] **Speaker 0:** to T tilt and make that substitution substitution into our
[00:07:05:859 - 00:07:06:769] **Speaker 0:** equation 5.
[00:07:07:510 - 00:07:10:750] **Speaker 0:** So we're replacing T with T to the T 0.
[00:07:11:559 - 00:07:16:089] **Speaker 0:** That's our first term Now, we want to.
[00:07:16:869 - 00:07:19:190] **Speaker 0:** Expand this derivative, so we've got DT by DT is
[00:07:19:190 - 00:07:21:910] **Speaker 0:** now DT nought tilda by DT.
[00:07:23:239 - 00:07:27:209] **Speaker 0:** T0 is that constant value, so 100 °C, for example,
[00:07:27:540 - 00:07:29:579] **Speaker 0:** because it's constant, it can be taken outside of the
[00:07:29:579 - 00:07:30:299] **Speaker 0:** derivative.
[00:07:30:619 - 00:07:33:559] **Speaker 0:** So T0 is outside the derivative, and we're left with
[00:07:34:059 - 00:07:35:739] **Speaker 0:** DT tilda by DT.
[00:07:38:190 - 00:07:42:260] **Speaker 0:** So we can make some further simplifications.
[00:07:42:779 - 00:07:43:959] **Speaker 0:** So we're gonna use the chain rule.
[00:07:46:350 - 00:07:48:630] **Speaker 0:** So everyone's probably forgotten the chain rule for maths.
[00:07:48:829 - 00:07:50:309] **Speaker 0:** So just a quick recap.
[00:07:52:519 - 00:07:55:839] **Speaker 0:** Channel is when we have the derivative of a variable,
[00:07:55:989 - 00:07:59:359] **Speaker 0:** for example, DT Tilda by DT.
[00:08:02:410 - 00:08:09:929] **Speaker 0:** This is equivalent to DT tilda by uh it's partial.
[00:08:11:260 - 00:08:17:679] **Speaker 0:** Partial D Little t tilter, so non-dimensional time t tilter.
[00:08:19:570 - 00:08:22:010] **Speaker 0:** And then we've got DT.
[00:08:23:079 - 00:08:25:410] **Speaker 0:** Toda by DT.
[00:08:26:700 - 00:08:29:070] **Speaker 0:** So the purpose of doing this chain rule is to
[00:08:29:070 - 00:08:33:969] **Speaker 0:** express our independent variable in non-dimensional units.
[00:08:34:349 - 00:08:37:130] **Speaker 0:** So we've gone from T to T tilda.
[00:08:40:989 - 00:08:46:169] **Speaker 0:** And I don't know if the mathematicians won't like it,
[00:08:46:219 - 00:08:48:460] **Speaker 0:** but you can sort of squint and say that that's
[00:08:48:460 - 00:08:51:059] **Speaker 0:** sort of equivalent we've got DT Tilda by DT and
[00:08:51:059 - 00:08:53:099] **Speaker 0:** they sort of cancel, but apparently there's more to it
[00:08:53:099 - 00:08:54:179] **Speaker 0:** than that in maths, but.
[00:08:55:090 - 00:08:56:609] **Speaker 0:** That's one way of remembering the chain rule.
[00:08:58:010 - 00:09:01:510] **Speaker 0:** Um So that's how we've got to this step.
[00:09:02:130 - 00:09:04:690] **Speaker 0:** So DT Tilda.
[00:09:06:890 - 00:09:11:250] **Speaker 0:** IDT, which is a full derivative because Ttilda only depends
[00:09:11:250 - 00:09:12:229] **Speaker 0:** on the time.
[00:09:16:239 - 00:09:17:530] **Speaker 0:** We can evaluate this.
[00:09:18:510 - 00:09:22:260] **Speaker 0:** As D by DT of T over T0.
[00:09:23:729 - 00:09:25:869] **Speaker 0:** Tough is that characteristic time, that's constant.
[00:09:27:109 - 00:09:30:059] **Speaker 0:** T, if we differentiate just goes to 1, so we're
[00:09:30:059 - 00:09:31:299] **Speaker 0:** left with 1 over T 00.
[00:09:33:940 - 00:09:45:890] **Speaker 0:** Subscript not So what we've done is Taken the dimensioned
[00:09:46:210 - 00:09:50:940] **Speaker 0:** first order derivative in time of our temperature, we've applied
[00:09:50:969 - 00:09:54:070] **Speaker 0:** or substituted the non-dimensional t tilda.
[00:09:55:020 - 00:09:58:919] **Speaker 0:** And then we've used the chain rule to Convert the
[00:09:58:919 - 00:10:01:479] **Speaker 0:** dimensioned time to non-dimensional tilter.
[00:10:03:039 - 00:10:06:260] **Speaker 0:** We do the same for space, so DT by DX
[00:10:06:260 - 00:10:07:669] **Speaker 0:** we substitute for T tilda.
[00:10:08:590 - 00:10:11:270] **Speaker 0:** Uh, Tino is constant, and again the chain rule.
[00:10:12:780 - 00:10:15:309] **Speaker 0:** Because we're looking at a second order derivative in space,
[00:10:15:590 - 00:10:18:309] **Speaker 0:** D2 T by DX2, we repeat the process.
[00:10:18:469 - 00:10:22:250] **Speaker 0:** So we've got another derivative and we're left with T
[00:10:23:169 - 00:10:26:710] **Speaker 0:** T over L2, D2T tilted by DX til 2.
[00:10:28:780 - 00:10:32:460] **Speaker 0:** We'll substitute in those expressions into our equation 5 and
[00:10:32:460 - 00:10:33:859] **Speaker 0:** we're left with this.
[00:10:34:609 - 00:10:36:530] **Speaker 0:** Uh, this expression.
[00:10:38:090 - 00:10:38:969] **Speaker 0:** Or this equation.
[00:10:40:619 - 00:10:42:239] **Speaker 0:** So is it dimensionless yet?
[00:10:48:599 - 00:10:48:950] **Speaker 0:** No.
[00:10:49:760 - 00:10:51:239] **Speaker 0:** So maybe you can see that as well, but we've
[00:10:51:239 - 00:10:53:219] **Speaker 0:** got alpha is metres squared per second.
[00:10:54:369 - 00:10:55:489] **Speaker 0:** Kelvin per metre squared.
[00:10:55:609 - 00:10:56:770] **Speaker 0:** It's it's not dimensionless.
[00:10:57:010 - 00:10:57:210] **Speaker 0:** Yeah.
[00:10:57:830 - 00:11:00:570] **Speaker 0:** Uh, the terms with tildas are dimensionless because we said
[00:11:00:570 - 00:11:01:809] **Speaker 0:** that T tilda is dimensionless.
[00:11:01:859 - 00:11:06:280] **Speaker 0:** It's T Kelvin over Kelvin, X is metres over metres,
[00:11:06:409 - 00:11:07:690] **Speaker 0:** so that's dimensionless.
[00:11:08:729 - 00:11:11:489] **Speaker 0:** Uh, what we're gonna do is rearrange this equation to
[00:11:11:489 - 00:11:15:109] **Speaker 0:** put all of the dimensional terms on one side.
[00:11:15:500 - 00:11:18:570] **Speaker 0:** So we're going to multiply both sides by L2 over
[00:11:18:570 - 00:11:19:010] **Speaker 0:** alpha.
[00:11:21:979 - 00:11:23:210] **Speaker 0:** The TNs Council.
[00:11:25:900 - 00:11:29:109] **Speaker 0:** And we're left with this expression in front of DT
[00:11:29:309 - 00:11:32:859] **Speaker 0:** t by DT tilter of L2 over alpha delta to
[00:11:32:859 - 00:11:35:739] **Speaker 0:** uh T0, too many variables.
[00:11:36:659 - 00:11:38:969] **Speaker 0:** So this equation is going to be dimensionless.
[00:11:38:979 - 00:11:41:979] **Speaker 0:** So each term of this equation has no units or
[00:11:41:979 - 00:11:46:260] **Speaker 0:** dimensions because the right-hand side has only got those tilter
[00:11:46:260 - 00:11:46:700] **Speaker 0:** terms.
[00:11:47:710 - 00:11:49:950] **Speaker 0:** We can double check by looking at the left-hand side.
[00:11:49:989 - 00:11:52:070] **Speaker 0:** So we've got L2, so that's going to be m2.
[00:11:52:989 - 00:11:57:140] **Speaker 0:** Um, alpha is metre squared per 2nd and 10 seconds,
[00:11:57:390 - 00:11:58:690] **Speaker 0:** so those are all cancelling out.
[00:11:59:890 - 00:12:02:640] **Speaker 0:** So so far we haven't chosen a timescale tonne.
[00:12:04:219 - 00:12:08:770] **Speaker 0:** And we've delayed that decision so that we can essentially
[00:12:08:770 - 00:12:11:299] **Speaker 0:** choose it to be elsewhere over alpha so it all
[00:12:11:299 - 00:12:12:150] **Speaker 0:** cancels out for us.
[00:12:12:349 - 00:12:19:210] **Speaker 0:** So the choice of the characteristic or um normalised scales.
[00:12:19:919 - 00:12:22:080] **Speaker 0:** are a little bit open to interpretation or however you
[00:12:22:080 - 00:12:22:400] **Speaker 0:** choose.
[00:12:22:789 - 00:12:25:239] **Speaker 0:** If you think back to your Venn's numbers, typically it's
[00:12:25:239 - 00:12:27:650] **Speaker 0:** the length scale that's most representative of the problem.
[00:12:27:760 - 00:12:30:599] **Speaker 0:** So if it was the cylinder and crossflow, it was
[00:12:30:599 - 00:12:31:340] **Speaker 0:** a diameter.
[00:12:31:679 - 00:12:33:880] **Speaker 0:** So you'd expect the vortices to sort of scale with
[00:12:33:880 - 00:12:35:659] **Speaker 0:** the diameter of the cylinder.
[00:12:36:280 - 00:12:38:260] **Speaker 0:** And when you're looking at channel flow, it might be
[00:12:38:260 - 00:12:39:640] **Speaker 0:** the distance across the channel.
[00:12:41:880 - 00:12:45:679] **Speaker 0:** So the, the governing PDU is equation 7.
[00:12:46:000 - 00:12:48:919] **Speaker 0:** So now we've replaced T0 with L2 over alpha and
[00:12:48:919 - 00:12:50:559] **Speaker 0:** all those terms fall out.
[00:12:51:739 - 00:12:54:419] **Speaker 0:** Now this governing PDE is free of any parameters, it's
[00:12:54:419 - 00:12:55:340] **Speaker 0:** fully non-dimensional.
[00:12:56:469 - 00:12:58:669] **Speaker 0:** So the advantage here is that we can solve this
[00:12:58:669 - 00:13:00:109] **Speaker 0:** governing equation once.
[00:13:00:969 - 00:13:04:549] **Speaker 0:** And then we can apply to many cases, uh, for
[00:13:04:650 - 00:13:05:799] **Speaker 0:** different dimensions.
[00:13:05:849 - 00:13:08:210] **Speaker 0:** So if we're looking at different initial conditions, uh, we
[00:13:08:210 - 00:13:11:130] **Speaker 0:** can just always scale our solution by that that uh
[00:13:11:130 - 00:13:11:650] **Speaker 0:** team knot.
[00:13:13:219 - 00:13:16:500] **Speaker 0:** Just as we've non-dimensionalized the governing PDE, we are also
[00:13:16:500 - 00:13:18:869] **Speaker 0:** going to non-dimensionalize the boundary conditions.
[00:13:20:330 - 00:13:22:789] **Speaker 0:** So T is going to be scaled by T0, etc.
[00:13:23:650 - 00:13:26:489] **Speaker 0:** Because it's 0, T tilda remains 0.
[00:13:27:520 - 00:13:31:200] **Speaker 0:** And the initial condition is scaled also by T0 and
[00:13:31:200 - 00:13:33:159] **Speaker 0:** we're ending up with sine pi X.
[00:13:37:489 - 00:13:41:409] **Speaker 0:** Now, if we compare the physical and dimensional spaces or
[00:13:41:409 - 00:13:44:489] **Speaker 0:** uh temperature profiles on the left, we've got the physical
[00:13:44:489 - 00:13:44:909] **Speaker 0:** space.
[00:13:45:409 - 00:13:49:450] **Speaker 0:** So dimensions of degrees Celsius in metres, and on the
[00:13:49:450 - 00:13:50:619] **Speaker 0:** right, we have no units.
[00:13:51:020 - 00:13:53:289] **Speaker 0:** We get the same profiles and the same scaling.
[00:13:54:150 - 00:13:58:409] **Speaker 0:** Uh The only difference is that essentially the non-dimensional case
[00:13:58:409 - 00:13:59:549] **Speaker 0:** is normalised.
[00:13:59:750 - 00:14:00:690] **Speaker 0:** So we've got one.
[00:14:01:669 - 00:14:05:559] **Speaker 0:** As the peak t tilter value and the X coordinate
[00:14:05:559 - 00:14:07:880] **Speaker 0:** being peak at X tilta equal 1.
[00:14:12:169 - 00:14:15:710] **Speaker 0:** So the solution of our PDE can also be non-dimensionalized,
[00:14:15:719 - 00:14:16:570] **Speaker 0:** and we've done that here.
[00:14:16:770 - 00:14:20:210] **Speaker 0:** So we've got sin pi x tilda, e minus pi
[00:14:20:210 - 00:14:21:330] **Speaker 0:** 2 T tilda.
[00:14:24:979 - 00:14:29:450] **Speaker 0:** Um Does that make sense or do you want me
[00:14:29:450 - 00:14:31:010] **Speaker 0:** to derive that?
[00:14:32:260 - 00:14:33:500] **Speaker 0:** You, you're OK.
[00:14:35:469 - 00:14:36:090] **Speaker 0:** You're fine.
[00:14:36:429 - 00:14:38:549] **Speaker 0:** You can do it in your own time if you
[00:14:38:549 - 00:14:39:030] **Speaker 0:** wish.
[00:14:40:000 - 00:14:44:289] **Speaker 0:** All right, so that's non non-dimensionalization or dimensionless equations.
[00:14:44:349 - 00:14:47:830] **Speaker 0:** Again, they're really helpful, uh, for generalising problems.
[00:14:48:369 - 00:14:53:299] **Speaker 0:** So, I mean we talked about Reynolds numbers, um.
[00:14:54:929 - 00:14:57:130] **Speaker 0:** In some cases, if you have a really large number
[00:14:57:130 - 00:14:59:369] **Speaker 0:** and really small numbers, that can behave quite poorly for
[00:14:59:369 - 00:15:00:000] **Speaker 0:** numerics.
[00:15:00:250 - 00:15:02:289] **Speaker 0:** So we talked a bit about roundoff error, uh, the
[00:15:02:289 - 00:15:02:979] **Speaker 0:** other day.
[00:15:03:450 - 00:15:06:210] **Speaker 0:** Um, so non-dimensionalizing equations can sort of get around that
[00:15:06:210 - 00:15:06:690] **Speaker 0:** as well.
[00:15:06:969 - 00:15:08:669] **Speaker 0:** So you can kind of treat each term.
[00:15:09:700 - 00:15:12:210] **Speaker 0:** normalised and sort of the same order of magnitude, so
[00:15:12:210 - 00:15:13:549] **Speaker 0:** that can be quite helpful as well.
[00:15:17:190 - 00:15:19:330] **Speaker 0:** Hopefully convince you that they're somewhat useful.
[00:15:19:750 - 00:15:23:849] **Speaker 0:** So we're gonna go through another analytical technique for solving
[00:15:24:349 - 00:15:27:229] **Speaker 0:** the heat equation, uh, which is called the method of
[00:15:27:229 - 00:15:28:190] **Speaker 0:** similarity solution.
[00:15:30:039 - 00:15:35:479] **Speaker 0:** So this technique is using dimensionless variables and we're going
[00:15:35:479 - 00:15:39:590] **Speaker 0:** to introduce another variable that groups a set of those
[00:15:39:590 - 00:15:39:960] **Speaker 0:** parameters.
[00:15:40:030 - 00:15:41:880] **Speaker 0:** So X, alpha and time T.
[00:15:42:929 - 00:15:46:090] **Speaker 0:** And essentially we're reducing the number of parameters that we
[00:15:46:090 - 00:15:48:450] **Speaker 0:** have to keep track of or variables, uh, and that
[00:15:48:450 - 00:15:50:809] **Speaker 0:** will help us to solve this, this solution.
[00:15:52:549 - 00:15:56:869] **Speaker 0:** So the context that we're looking at is a semi-infinite
[00:15:56:869 - 00:15:57:409] **Speaker 0:** slab.
[00:15:58:840 - 00:16:00:340] **Speaker 0:** So I'll try to draw this.
[00:16:07:570 - 00:16:10:729] **Speaker 0:** And the slab is initially at some temperature T1.
[00:16:16:219 - 00:16:18:510] **Speaker 0:** And again, this is dimensions, we don't have the tildas
[00:16:18:510 - 00:16:19:159] **Speaker 0:** at this stage.
[00:16:19:669 - 00:16:22:700] **Speaker 0:** So we've got T1.
[00:16:23:599 - 00:16:26:080] **Speaker 0:** As the initial temperature of our concrete slab.
[00:16:31:309 - 00:16:34:250] **Speaker 0:** And at time 0, T equals 0.
[00:16:35:630 - 00:16:38:429] **Speaker 0:** At times 0, the surface of the slab, which is
[00:16:38:429 - 00:16:39:549] **Speaker 0:** at X equal to 0.
[00:16:40:260 - 00:16:43:460] **Speaker 0:** Is brought to some fixed temperature of T infinity.
[00:16:44:359 - 00:16:46:049] **Speaker 0:** So maybe it's the atmospheric temperature.
[00:16:51:390 - 00:16:54:950] **Speaker 0:** So it's got the step change from T infinity up
[00:16:54:950 - 00:16:56:950] **Speaker 0:** to T1 at times 0.
[00:17:05:079 - 00:17:07:670] **Speaker 0:** And we want to find the temperature distribution in this
[00:17:07:670 - 00:17:08:599] **Speaker 0:** lab over time.
[00:17:08:839 - 00:17:10:319] **Speaker 0:** So we're going to apply our heat equation.
[00:17:10:599 - 00:17:12:270] **Speaker 0:** We don't have any fluid flow.
[00:17:12:319 - 00:17:13:280] **Speaker 0:** We don't have any convection.
[00:17:13:400 - 00:17:15:260] **Speaker 0:** We're just looking at diffusion of heat.
[00:17:15:760 - 00:17:17:599] **Speaker 0:** So we can use our heat equation, which we've got
[00:17:17:599 - 00:17:20:260] **Speaker 0:** that thermal diffusivity driving the temperature distribution.
[00:17:21:140 - 00:17:22:810] **Speaker 0:** We've got a couple of boundary conditions.
[00:17:23:719 - 00:17:26:140] **Speaker 0:** The temperature at X equal to 0.
[00:17:27:430 - 00:17:29:170] **Speaker 0:** is fixed at Key Infinity.
[00:17:29:949 - 00:17:33:880] **Speaker 0:** And the temperature as x tends to infinity is equal
[00:17:33:880 - 00:17:34:550] **Speaker 0:** to T1.
[00:17:36:750 - 00:17:52:489] **Speaker 0:** Um, Alright, so.
[00:17:53:939 - 00:17:57:459] **Speaker 0:** A little bit tricky because it's semi-infinite, uh, domain, so
[00:17:57:459 - 00:18:01:180] **Speaker 0:** it extends to infinity, but we might expect that over
[00:18:01:180 - 00:18:01:599] **Speaker 0:** time.
[00:18:02:410 - 00:18:05:449] **Speaker 0:** The greatest temperature gradients are obviously at the step change,
[00:18:05:530 - 00:18:07:599] **Speaker 0:** so it's going to be really quick to diffuse that,
[00:18:08:689 - 00:18:09:290] **Speaker 0:** that heat.
[00:18:21:300 - 00:18:26:260] **Speaker 0:** And so the gaps between those profiles, you could draw
[00:18:26:260 - 00:18:30:099] **Speaker 0:** them that are decreasing in size, uh, over time.
[00:18:38:709 - 00:18:38:719] **Speaker 0:** Time.
[00:18:50:250 - 00:18:52:369] **Speaker 0:** So that's what we expect the solution to look like.
[00:18:52:619 - 00:18:53:420] **Speaker 0:** Some something like that.
[00:18:54:390 - 00:18:56:810] **Speaker 0:** So what we're going to do is introduce a dimensionless
[00:18:56:810 - 00:18:57:199] **Speaker 0:** temperature.
[00:18:59:339 - 00:19:01:890] **Speaker 0:** That varies between T infinity and T1.
[00:19:02:699 - 00:19:04:939] **Speaker 0:** So it's just gonna scale from 0 to 1, so
[00:19:04:939 - 00:19:07:760] **Speaker 0:** it's normalised, and we can do that by looking at
[00:19:07:760 - 00:19:10:089] **Speaker 0:** the difference between those two values.
[00:19:10:140 - 00:19:13:219] **Speaker 0:** So T11 T infinity and then scale the difference between
[00:19:13:219 - 00:19:15:599] **Speaker 0:** T and T infinity over that change.
[00:19:16:589 - 00:19:20:130] **Speaker 0:** So T minus the infinity over T1 minus the infinity
[00:19:20:780 - 00:19:23:390] **Speaker 0:** will collapse that temperature space from 0 to 1.
[00:19:25:270 - 00:19:28:829] **Speaker 0:** So to make the governing equation dimensionless, uh, we also
[00:19:28:829 - 00:19:30:530] **Speaker 0:** need to use a characteristic length.
[00:19:30:910 - 00:19:33:390] **Speaker 0:** So before we use the length of the rod, now
[00:19:33:390 - 00:19:35:689] **Speaker 0:** we have an infinite domain.
[00:19:36:189 - 00:19:39:010] **Speaker 0:** So continues off to infinity in the X direction.
[00:19:39:780 - 00:19:42:739] **Speaker 0:** We also need to select a characteristic time T knot.
[00:19:44:719 - 00:19:48:500] **Speaker 0:** So, unfortunately, there's no obvious choice for our length L.
[00:19:49:339 - 00:19:52:030] **Speaker 0:** Uh, because of that semi-infinite, uh, domain.
[00:19:53:099 - 00:19:54:390] **Speaker 0:** So what we're gonna do.
[00:19:56:339 - 00:19:58:709] **Speaker 0:** I look at combining some of the variables together.
[00:19:58:949 - 00:20:01:680] **Speaker 0:** So we're going to combine the spatial coordinate X and
[00:20:01:680 - 00:20:05:989] **Speaker 0:** temporal component time T into a new dimensionless variable.
[00:20:07:160 - 00:20:10:680] **Speaker 0:** And if we go through another non-dimensionalization procedure, uh, we
[00:20:10:680 - 00:20:13:160] **Speaker 0:** could figure out that it scales with X over square
[00:20:13:160 - 00:20:14:380] **Speaker 0:** root alpha T.
[00:20:14:939 - 00:20:17:020] **Speaker 0:** We can just check that those units are correct.
[00:20:17:640 - 00:20:23:989] **Speaker 0:** So we've got the units of X over square root
[00:20:23:989 - 00:20:25:069] **Speaker 0:** alpha T.
[00:20:28:130 - 00:20:30:790] **Speaker 0:** It's gonna be metres for the X component.
[00:20:31:479 - 00:20:34:800] **Speaker 0:** And square root of alpha, which we said was metres
[00:20:34:800 - 00:20:36:380] **Speaker 0:** squared per second, is a diffusive.
[00:20:38:349 - 00:20:39:670] **Speaker 0:** Right, and in time.
[00:20:41:479 - 00:20:44:199] **Speaker 0:** So the seconds cancel and we've got metres over metres.
[00:20:45:199 - 00:20:46:280] **Speaker 0:** So that's reassuring.
[00:20:46:550 - 00:20:48:599] **Speaker 0:** So this expression is dimensionless.
[00:20:49:780 - 00:20:51:229] **Speaker 0:** X over square root alpha T.
[00:20:56:150 - 00:21:01:260] **Speaker 0:** So, I mean, we're doing this because um we can
[00:21:01:260 - 00:21:05:910] **Speaker 0:** express the, the spatial and temporal coordinates together and we've
[00:21:05:910 - 00:21:07:910] **Speaker 0:** just got that one variable that we're trying to keep
[00:21:07:910 - 00:21:08:390] **Speaker 0:** track of.
[00:21:09:380 - 00:21:12:979] **Speaker 0:** And we're seeing how this temperature evolution happens in a
[00:21:12:979 - 00:21:13:739] **Speaker 0:** self-similar way.
[00:21:14:959 - 00:21:17:040] **Speaker 0:** And hopefully it will become clearer towards the end.
[00:21:23:750 - 00:21:24:680] **Speaker 0:** So that's dimensionless.
[00:21:25:709 - 00:21:29:939] **Speaker 0:** So we're gonna label this single variable ata to be
[00:21:29:939 - 00:21:31:829] **Speaker 0:** X over 2 square root alpha T.
[00:21:33:329 - 00:21:37:079] **Speaker 0:** Uh, we've chucked in a 2, a factor 2, because
[00:21:37:180 - 00:21:38:839] **Speaker 0:** it helps with the maths later on.
[00:21:40:560 - 00:21:46:170] **Speaker 0:** Again, the selection of these terms can be reasonably arbitrary,
[00:21:46:449 - 00:21:48:390] **Speaker 0:** uh, so it doesn't matter too much.
[00:21:48:810 - 00:21:51:489] **Speaker 0:** As long as when you go to dimensionalize the equation
[00:21:51:489 - 00:21:54:489] **Speaker 0:** again, you include the terms that you've stated.
[00:21:55:900 - 00:21:56:420] **Speaker 0:** All right.
[00:21:57:329 - 00:21:59:489] **Speaker 0:** So we can rename this, we'll just write it out
[00:21:59:489 - 00:22:00:670] **Speaker 0:** as X over 2.
[00:22:02:479 - 00:22:04:640] **Speaker 0:** Alpha T to -5.
[00:22:08:030 - 00:22:09:790] **Speaker 0:** So it's just, it's exactly the same.
[00:22:10:770 - 00:22:12:859] **Speaker 0:** That might be easier to, to read.
[00:22:14:869 - 00:22:21:229] **Speaker 0:** So We're going to need the derivative, the adder by
[00:22:22:180 - 00:22:22:819] **Speaker 0:** DT.
[00:22:23:219 - 00:22:24:839] **Speaker 0:** So we're gonna evaluate that now.
[00:22:26:609 - 00:22:27:829] **Speaker 0:** For convenience.
[00:22:29:630 - 00:22:32:709] **Speaker 0:** So the ata ata being our single variable that we're
[00:22:32:709 - 00:22:36:510] **Speaker 0:** trying to keep track of, that's describing our solution, time
[00:22:36:510 - 00:22:37:790] **Speaker 0:** being the temporal component.
[00:22:40:530 - 00:22:45:729] **Speaker 0:** So the A T, if we're differentiating this expression, equation
[00:22:45:729 - 00:22:49:650] **Speaker 0:** 12, we're left with -5 times 1/2.
[00:22:49:770 - 00:22:51:510] **Speaker 0:** So we've got minus X over 4.
[00:22:53:689 - 00:22:55:630] **Speaker 0:** And this is why I left it in brackets.
[00:22:55:689 - 00:22:59:369] **Speaker 0:** So we've got alpha to the -5, and then we've
[00:22:59:369 - 00:23:01:569] **Speaker 0:** got time to the -3 halves.
[00:23:07:270 - 00:23:09:910] **Speaker 0:** And then we can convert it to that fraction again,
[00:23:10:030 - 00:23:11:869] **Speaker 0:** so we've got minus X.
[00:23:12:680 - 00:23:21:369] **Speaker 0:** Over 2 Times the square root of alpha T times
[00:23:21:469 - 00:23:22:920] **Speaker 0:** 2 T.
[00:23:25:160 - 00:23:28:329] **Speaker 0:** So we're just splitting up the factors of 2.
[00:23:29:520 - 00:23:34:010] **Speaker 0:** And splitting apart T so that we can identify this
[00:23:34:010 - 00:23:37:439] **Speaker 0:** as -8 over 2 T.
[00:23:40:760 - 00:23:41:650] **Speaker 0:** Some rearrangement.
[00:23:42:930 - 00:23:49:989] **Speaker 0:** Alright Now we're gonna use the chain rule again.
[00:23:51:219 - 00:23:53:699] **Speaker 0:** So DT Tilda, IDT.
[00:23:55:430 - 00:23:59:569] **Speaker 0:** This time, T Tilda is a function of Ada.
[00:24:00:640 - 00:24:02:849] **Speaker 0:** So we've got a derivative with respect to Ada.
[00:24:03:619 - 00:24:05:819] **Speaker 0:** It only depends on Ada, so it's a full derivative
[00:24:05:819 - 00:24:07:810] **Speaker 0:** instead of those partial derivatives that we did earlier.
[00:24:08:270 - 00:24:11:290] **Speaker 0:** And we've got the Ada by DT being partial because
[00:24:11:290 - 00:24:13:189] **Speaker 0:** now Ada is a function of X and T.
[00:24:14:959 - 00:24:19:819] **Speaker 0:** And DT Tilda by the Ada.
[00:24:22:540 - 00:24:27:119] **Speaker 0:** Is left because they're both dimensionless, T Tilda and Ada.
[00:24:28:550 - 00:24:32:310] **Speaker 0:** And the AIDT, we just evaluated as -8 over 2T.
[00:24:34:390 - 00:24:37:640] **Speaker 0:** So that's the temporal derivative DT tilted by DT.
[00:24:38:079 - 00:24:39:560] **Speaker 0:** We do the same in space.
[00:24:39:800 - 00:24:43:449] **Speaker 0:** So DT tilted by dx, applying the chain rule.
[00:24:44:640 - 00:24:50:550] **Speaker 0:** And we've got, D detilda by the X, we've got
[00:24:50:550 - 00:24:53:390] **Speaker 0:** D Ata by the X, D8 by the X, we
[00:24:53:390 - 00:24:56:579] **Speaker 0:** can just do that by identifying it's 1/2 square root
[00:24:56:579 - 00:24:57:150] **Speaker 0:** alpha T.
[00:24:58:449 - 00:25:01:079] **Speaker 0:** And we're left with that dimensionless term DT tilda by
[00:25:01:079 - 00:25:01:890] **Speaker 0:** the edit.
[00:25:05:380 - 00:25:07:550] **Speaker 0:** Does everyone, everyone follow along with the chain rule?
[00:25:07:709 - 00:25:08:209] **Speaker 0:** OK?
[00:25:09:479 - 00:25:11:930] **Speaker 0:** Or you want me to do the working out, or?
[00:25:12:880 - 00:25:14:079] **Speaker 0:** Don't don't really need it.
[00:25:14:199 - 00:25:16:520] **Speaker 0:** So we won't, but you can, you can go through
[00:25:16:520 - 00:25:17:439] **Speaker 0:** each step if you wish.
[00:25:19:540 - 00:25:21:310] **Speaker 0:** We've done the first order derivative in space X.
[00:25:21:500 - 00:25:24:270] **Speaker 0:** We do the second order, so D2T tilted by DX2.
[00:25:27:380 - 00:25:31:339] **Speaker 0:** And we substitute back into our equation, our heat equation,
[00:25:31:380 - 00:25:34:219] **Speaker 0:** equation 9, and we've got equation 14.
[00:25:37:500 - 00:25:38:500] **Speaker 0:** So far.
[00:25:40:510 - 00:25:42:209] **Speaker 0:** Is this equation dimensionless?
[00:25:50:449 - 00:25:51:510] **Speaker 0:** A is dimensionless.
[00:25:52:030 - 00:25:55:339] **Speaker 0:** Tilda de tilda, T tilda is, the X is not.
[00:25:55:459 - 00:25:57:170] **Speaker 0:** We've got 1/1 metre squared on the right.
[00:25:57:550 - 00:25:59:760] **Speaker 0:** On the left we've got 1/1 metre squared per second,
[00:26:00:030 - 00:26:01:069] **Speaker 0:** uh, times seconds.
[00:26:05:369 - 00:26:06:349] **Speaker 0:** So the next step.
[00:26:07:150 - 00:26:21:420] **Speaker 0:** Is, To substitute these expressions.
[00:26:21:760 - 00:26:23:500] **Speaker 0:** So we've got our 2nd order derivative.
[00:26:24:250 - 00:26:27:550] **Speaker 0:** Uh, X and first order derivative in time.
[00:26:29:209 - 00:26:32:420] **Speaker 0:** So now actually, yeah, now we're now we're um substituting
[00:26:32:420 - 00:26:34:910] **Speaker 0:** these into our heat equation, so that wasn't 14.
[00:26:35:449 - 00:26:36:859] **Speaker 0:** We're getting to the fun part now.
[00:26:37:290 - 00:26:43:410] **Speaker 0:** Um, so we've got minus, A divided by 2 T.
[00:26:45:900 - 00:26:48:900] **Speaker 0:** DT Tilda by the Ada.
[00:26:50:040 - 00:26:51:170] **Speaker 0:** That was the time component.
[00:26:51:359 - 00:26:52:489] **Speaker 0:** That was equation 13.
[00:26:56:709 - 00:27:01:640] **Speaker 0:** Is equal to So equation 9, we're not making it
[00:27:01:640 - 00:27:05:189] **Speaker 0:** up, so we've got alpha, D2 T by DX2.
[00:27:06:369 - 00:27:11:339] **Speaker 0:** And we said this is equal to I had Over
[00:27:11:339 - 00:27:13:150] **Speaker 0:** X 2.
[00:27:14:339 - 00:27:18:729] **Speaker 0:** D2T total by D2.
[00:27:35:839 - 00:27:37:280] **Speaker 0:** So what have we achieved so far?
[00:27:37:560 - 00:27:42:079] **Speaker 0:** We've gone from a PDE, so partial derivative equation, um.
[00:27:43:020 - 00:27:46:119] **Speaker 0:** To a full derivative or ODU, ordinary differential equation.
[00:27:47:119 - 00:27:49:199] **Speaker 0:** Which is a step in the right direction.
[00:27:49:939 - 00:27:51:780] **Speaker 0:** Uh, so we've got an ODE that we need to
[00:27:51:780 - 00:27:52:319] **Speaker 0:** solve now.
[00:27:53:520 - 00:27:55:839] **Speaker 0:** We've got a 2nd order, uh, term.
[00:27:57:359 - 00:28:01:050] **Speaker 0:** And we're going to rearrange for that 2nd order D2
[00:28:01:050 - 00:28:02:670] **Speaker 0:** T tilter by D82.
[00:28:12:319 - 00:28:16:130] **Speaker 0:** So um grouping terms, we've got -8.
[00:28:18:530 - 00:28:21:530] **Speaker 0:** Over 2 T alpha.
[00:28:24:180 - 00:28:29:660] **Speaker 0:** And we've got X over 82.
[00:28:32:839 - 00:28:37:670] **Speaker 0:** Multiplied by DT Tota by D.
[00:28:38:709 - 00:28:56:449] **Speaker 0:** E So Ada cancels with one of the Adas in
[00:28:56:449 - 00:28:57:319] **Speaker 0:** the denominator.
[00:28:58:079 - 00:29:02:170] **Speaker 0:** And if we look at what it was, so back
[00:29:02:170 - 00:29:07:800] **Speaker 0:** in equation 12, we can simplify this to -28.
[00:29:13:780 - 00:29:17:229] **Speaker 0:** DT Tota by the Ada.
[00:29:22:390 - 00:29:24:630] **Speaker 0:** So we've still got this factor of 2, it'll be
[00:29:24:630 - 00:29:25:510] **Speaker 0:** helpful a bit later.
[00:29:29:750 - 00:29:31:729] **Speaker 0:** Now we've got a 2nd order derivative on the left
[00:29:31:729 - 00:29:33:489] **Speaker 0:** and a 1st order derivative on the right.
[00:29:34:260 - 00:29:37:359] **Speaker 0:** One of the techniques that you've learned about is the
[00:29:37:359 - 00:29:39:239] **Speaker 0:** um that method of substitution.
[00:29:39:339 - 00:29:42:280] **Speaker 0:** So you're sort of reducing the order of those derivatives
[00:29:42:819 - 00:29:44:939] **Speaker 0:** by calling a new variable.
[00:29:47:060 - 00:29:49:000] **Speaker 0:** You, for example.
[00:29:49:890 - 00:29:53:680] **Speaker 0:** To be that first order derivative DT Tilda by.
[00:29:55:660 - 00:29:57:020] **Speaker 0:** The Ada.
[00:30:02:979 - 00:30:06:520] **Speaker 0:** And we'll use this variable in our equation to reduce
[00:30:06:520 - 00:30:09:140] **Speaker 0:** that order from 2nd order down to 1st order derivative.
[00:30:10:900 - 00:30:16:900] **Speaker 0:** So the left-hand side goes to D U I.
[00:30:18:599 - 00:30:22:880] **Speaker 0:** The Ada So instead of D2 T tora by D2,
[00:30:23:209 - 00:30:24:849] **Speaker 0:** it's now DU by theta.
[00:30:27:150 - 00:30:29:880] **Speaker 0:** In the right-hand side we've got -28.
[00:30:30:719 - 00:30:33:020] **Speaker 0:** Multiplied by the first order derivative and we just said
[00:30:33:020 - 00:30:33:680] **Speaker 0:** that was you.
[00:30:41:319 - 00:30:44:550] **Speaker 0:** The next step is to group.
[00:30:45:699 - 00:30:47:000] **Speaker 0:** The variables together.
[00:30:47:800 - 00:30:48:890] **Speaker 0:** That are related to one another.
[00:30:48:969 - 00:30:50:989] **Speaker 0:** So we've got the Us on the left-hand side.
[00:30:55:459 - 00:30:57:500] **Speaker 0:** And the ada terms on the right, so we've got
[00:30:57:500 - 00:31:00:540] **Speaker 0:** -2 Ata the Ada.
[00:31:09:150 - 00:31:10:510] **Speaker 0:** Then we're going to integrate.
[00:31:18:530 - 00:31:23:119] **Speaker 0:** So if we're integrating The left-hand side, we've got one
[00:31:23:119 - 00:31:26:599] **Speaker 0:** over U integrating in the U coordinate system.
[00:31:27:530 - 00:31:30:089] **Speaker 0:** So integrating one over you, we're left with the natural
[00:31:30:089 - 00:31:30:630] **Speaker 0:** log.
[00:31:31:959 - 00:31:39:369] **Speaker 0:** Of you And the right hand side Uh, Ada just
[00:31:39:369 - 00:31:43:209] **Speaker 0:** goes to A a squid.
[00:31:44:180 - 00:31:45:719] **Speaker 0:** Divided by 2, so the 2s cancel.
[00:31:45:859 - 00:31:48:219] **Speaker 0:** So that's why we included the 2 in our earlier
[00:31:48:219 - 00:31:48:800] **Speaker 0:** definition.
[00:31:49:219 - 00:31:52:180] **Speaker 0:** So we've got minus 82.
[00:31:53:890 - 00:31:54:540] **Speaker 0:** Plus.
[00:31:55:609 - 00:31:57:369] **Speaker 0:** Some constant of integration, C1.
[00:32:05:609 - 00:32:05:619] **Speaker 0:** Right.
[00:32:08:969 - 00:32:27:439] **Speaker 0:** So We've said that U is equal to The Tilda
[00:32:27:770 - 00:32:29:099] **Speaker 0:** by the Ada.
[00:32:36:660 - 00:32:38:920] **Speaker 0:** And that's going to be C.
[00:32:40:089 - 00:32:43:000] **Speaker 0:** E to minus 82.
[00:32:45:150 - 00:32:46:650] **Speaker 0:** And we're just grouping those.
[00:32:47:609 - 00:32:48:989] **Speaker 0:** Terms, so C1.
[00:32:50:489 - 00:32:52:939] **Speaker 0:** Is going to be included as C equal to E
[00:32:52:939 - 00:32:53:920] **Speaker 0:** to the power of C1.
[00:32:57:729 - 00:33:00:469] **Speaker 0:** So I've taken the exponential of both sides, and then
[00:33:00:469 - 00:33:01:489] **Speaker 0:** we're solving for you.
[00:33:06:209 - 00:33:09:099] **Speaker 0:** So we've done that substitution and integrated once.
[00:33:09:619 - 00:33:13:949] **Speaker 0:** Now we've gone back to the T tildas and adders
[00:33:13:949 - 00:33:15:170] **Speaker 0:** and we can integrate again.
[00:33:15:290 - 00:33:18:329] **Speaker 0:** So now it's just a first order derivative, DT tilda
[00:33:18:329 - 00:33:18:930] **Speaker 0:** by the adder.
[00:33:20:060 - 00:33:24:260] **Speaker 0:** And we're left with T Toda.
[00:33:24:920 - 00:33:27:430] **Speaker 0:** Ada, Equal to C.
[00:33:29:709 - 00:33:31:489] **Speaker 0:** Integrating from 0 up to 80.
[00:33:32:380 - 00:33:38:459] **Speaker 0:** E to the minus Z2 DZ plus constant of integration
[00:33:38:459 - 00:33:38:760] **Speaker 0:** T.
[00:33:41:219 - 00:33:43:140] **Speaker 0:** At X equals 0.
[00:33:45:849 - 00:33:51:140] **Speaker 0:** Uh, so this is The solution for this problem.
[00:33:51:400 - 00:33:53:349] **Speaker 0:** Um, so Z is some dummy variable.
[00:33:53:390 - 00:33:56:150] **Speaker 0:** It's just integrating from 0 up to Ada.
[00:33:56:349 - 00:33:58:189] **Speaker 0:** So we're just using this extra term so not including
[00:33:58:189 - 00:33:59:630] **Speaker 0:** a twice in that expression.
[00:34:01:530 - 00:34:06:310] **Speaker 0:** For our choice of our dimensionless temperature t tilter, the
[00:34:06:569 - 00:34:07:270] **Speaker 0:** temperature.
[00:34:08:749 - 00:34:13:718] **Speaker 0:** At 0 is equal to 0 because that's equal to
[00:34:13:718 - 00:34:14:579] **Speaker 0:** T infinity.
[00:34:17:120 - 00:34:20:878] **Speaker 0:** Uh, the second constant is going to be figured out
[00:34:20:878 - 00:34:22:479] **Speaker 0:** from the 2nd boundary condition.
[00:34:22:929 - 00:34:24:750] **Speaker 0:** So we've got a PDE.
[00:34:25:330 - 00:34:28:050] **Speaker 0:** We need two boundary conditions and an initial condition to
[00:34:28:050 - 00:34:29:810] **Speaker 0:** uniquely identify this problem.
[00:34:30:919 - 00:34:33:699] **Speaker 0:** So C is equal to.
[00:34:37:800 - 00:34:43:169] **Speaker 0:** The integral from 0 up to infinity, so that's semi-infinite
[00:34:43:169 - 00:34:46:370] **Speaker 0:** slab, E minus Z 2.
[00:34:47:489 - 00:34:54:070] **Speaker 0:** DZ And that so happens to be two of those
[00:34:54:070 - 00:34:54:840] **Speaker 0:** square root pies.
[00:34:58:780 - 00:35:02:199] **Speaker 0:** So overall, if we substitute that back in for C,
[00:35:02:820 - 00:35:07:979] **Speaker 0:** we've got a temperature distribution, so non-dimensional T tilda scaling
[00:35:07:979 - 00:35:11:500] **Speaker 0:** with a as a function of theta is equal to
[00:35:11:500 - 00:35:14:320] **Speaker 0:** 2 over the square root pi and then this integral
[00:35:14:459 - 00:35:17:479] **Speaker 0:** from 0 to 8, e minus Z 2 DZ.
[00:35:18:139 - 00:35:21:939] **Speaker 0:** And this is also the Gaussian error function of the.
[00:35:27:419 - 00:35:32:399] **Speaker 0:** So a less obvious analytical solution, but another one that
[00:35:32:399 - 00:35:34:899] **Speaker 0:** can be used to solve these types of problems.
[00:35:35:889 - 00:35:41:419] **Speaker 0:** And What we've done is still gone from like a
[00:35:41:419 - 00:35:44:620] **Speaker 0:** PDE of two variables, so in space X and time
[00:35:44:620 - 00:35:47:540] **Speaker 0:** T, and we've gone and reduced it down to an
[00:35:47:540 - 00:35:49:500] **Speaker 0:** ODE of one variable, so.
[00:35:51:020 - 00:35:51:409] **Speaker 0:** Yeah.
[00:35:52:879 - 00:35:54:159] **Speaker 0:** It, it, it works out.
[00:35:56:020 - 00:35:57:739] **Speaker 0:** Now that we have T Tilda.
[00:35:58:580 - 00:36:00:580] **Speaker 0:** That is only changing as a function of ata.
[00:36:00:939 - 00:36:04:060] **Speaker 0:** We want to pull it apart and plot temperature in
[00:36:04:060 - 00:36:07:219] **Speaker 0:** space and time, so we need to convert back into
[00:36:07:219 - 00:36:07:959] **Speaker 0:** a space.
[00:36:09:260 - 00:36:11:570] **Speaker 0:** So if we replace um.
[00:36:12:860 - 00:36:14:800] **Speaker 0:** Maybe you just label this dimensionalizing.
[00:36:21:000 - 00:36:23:419] **Speaker 0:** So we've got T minus T infinity.
[00:36:24:159 - 00:36:26:679] **Speaker 0:** Divided by that range, T1 minus T infinity.
[00:36:30:300 - 00:36:35:250] **Speaker 0:** Equals to the error function of, Ada, and we said
[00:36:35:250 - 00:36:38:770] **Speaker 0:** Ada is X over 2 square root alpha T.
[00:36:48:860 - 00:36:49:399] **Speaker 0:** Cool.
[00:36:49:860 - 00:36:52:199] **Speaker 0:** So don't be too concerned about all the maths, but
[00:36:52:580 - 00:36:56:379] **Speaker 0:** in, in summary, we've essentially found another analytical solution for
[00:36:56:379 - 00:37:02:080] **Speaker 0:** this problem, and, It evolves self-similarity, which is quite cool.
[00:37:02:899 - 00:37:04:459] **Speaker 0:** You can think of like those fractals that you might
[00:37:04:459 - 00:37:04:959] **Speaker 0:** have seen.
[00:37:06:389 - 00:37:08:840] **Speaker 0:** I mean you keep zooming in and zooming in the
[00:37:08:840 - 00:37:10:439] **Speaker 0:** same sort of picture.
[00:37:18:530 - 00:37:22:750] **Speaker 0:** And I'll just try and find the code for this.
[00:37:38:719 - 00:37:45:449] **Speaker 0:** Uh So More code, which I know you don't like
[00:37:45:870 - 00:37:48:929] **Speaker 0:** me watching me go through it, but just briefly.
[00:37:58:729 - 00:38:00:889] **Speaker 0:** So there's all all these codes are on the the
[00:38:00:889 - 00:38:02:409] **Speaker 0:** learn folder, course material folder.
[00:38:03:320 - 00:38:05:000] **Speaker 0:** Uh, you can work it, work it through in your
[00:38:05:000 - 00:38:06:520] **Speaker 0:** own time, um.
[00:38:09:729 - 00:38:12:449] **Speaker 0:** Seem to have lost part of the screen, but that's
[00:38:12:449 - 00:38:12:929] **Speaker 0:** OK.
[00:38:17:469 - 00:38:17:840] **Speaker 0:** Alright.
[00:38:18:649 - 00:38:26:870] **Speaker 0:** Uh, so We're gonna plot The temperature evolution from our
[00:38:26:929 - 00:38:29:750] **Speaker 0:** infants lab, so we're expecting this sort of profile.
[00:38:30:850 - 00:38:33:370] **Speaker 0:** Because it's semi-infinite, we need to decide on some upper
[00:38:33:370 - 00:38:35:929] **Speaker 0:** limit of the X coordinates to plot physically in our
[00:38:35:929 - 00:38:36:310] **Speaker 0:** code.
[00:38:36:729 - 00:38:38:590] **Speaker 0:** So that is going to be 2 in this case.
[00:38:39:129 - 00:38:40:729] **Speaker 0:** We're plotting over time, so we need to have a
[00:38:40:729 - 00:38:42:050] **Speaker 0:** time vector or array.
[00:38:42:959 - 00:38:45:520] **Speaker 0:** Our temperature array is a two-dimensional array, so X and
[00:38:45:520 - 00:38:45:649] **Speaker 0:** T.
[00:38:47:300 - 00:38:49:239] **Speaker 0:** We have an initial condition of T1.
[00:38:50:050 - 00:38:51:780] **Speaker 0:** And then we're plotting, so I'm using a 4 loop
[00:38:51:780 - 00:38:57:020] **Speaker 0:** here to generate the, Solution, so we're using a 4
[00:38:57:020 - 00:38:58:600] **Speaker 0:** loop in space and time.
[00:38:59:540 - 00:39:02:879] **Speaker 0:** And filling this array, and then plotting these lines.
[00:39:03:379 - 00:39:05:300] **Speaker 0:** So that's one approach, and I'll show you another approach
[00:39:05:300 - 00:39:05:739] **Speaker 0:** shortly.
[00:39:10:250 - 00:39:12:679] **Speaker 0:** So, Like yourself.
[00:39:13:080 - 00:39:16:070] **Speaker 0:** The sketch was not super, super accurate, but it gives
[00:39:16:070 - 00:39:16:889] **Speaker 0:** us a general idea.
[00:39:17:280 - 00:39:18:110] **Speaker 0:** Oh, it's not too bad.
[00:39:18:510 - 00:39:21:790] **Speaker 0:** So we have initial condition at T1.
[00:39:22:790 - 00:39:25:229] **Speaker 0:** And over time it decays, the temperature decays.
[00:39:26:040 - 00:39:26:780] **Speaker 0:** So that's neat.
[00:39:27:280 - 00:39:30:840] **Speaker 0:** Um, nothing else really to say on that one, and.
[00:39:31:739 - 00:39:35:340] **Speaker 0:** I used 224 loops to toggle through X and T.
[00:39:35:850 - 00:39:41:169] **Speaker 0:** Uh, what you could do instead is, Solve because.
[00:39:42:560 - 00:39:43:979] **Speaker 0:** This analytical solution.
[00:39:45:629 - 00:39:47:620] **Speaker 0:** Is um.
[00:39:48:429 - 00:39:50:229] **Speaker 0:** It's valid for all space and time.
[00:39:50:270 - 00:39:52:750] **Speaker 0:** You don't need to solve one time step and then
[00:39:52:750 - 00:39:54:590] **Speaker 0:** the next, just like we will need to for our
[00:39:54:590 - 00:39:55:350] **Speaker 0:** finite differencing.
[00:39:56:300 - 00:39:58:189] **Speaker 0:** So we can evaluate the temperature distribution.
[00:39:59:100 - 00:40:00:629] **Speaker 0:** In one step, we don't have to solve it in
[00:40:00:629 - 00:40:01:379] **Speaker 0:** 4 loops.
[00:40:01:830 - 00:40:04:659] **Speaker 0:** So this is just demonstrating how you can solve uh
[00:40:04:790 - 00:40:06:110] **Speaker 0:** with an array for Ada.
[00:40:07:020 - 00:40:10:820] **Speaker 0:** So stretching X into two dimensions, uh, not including the
[00:40:10:820 - 00:40:11:520] **Speaker 0:** initial time.
[00:40:13:790 - 00:40:16:959] **Speaker 0:** And then we're going to plot these X-arrays and temperature
[00:40:16:959 - 00:40:19:360] **Speaker 0:** arrays, ah, directly.
[00:40:22:189 - 00:40:23:719] **Speaker 0:** So we ended up with the same solution.
[00:40:25:290 - 00:40:26:969] **Speaker 0:** But it should solve it quicker.
[00:40:27:010 - 00:40:28:709] **Speaker 0:** It's not using those 4 loops in Python.
[00:40:29:449 - 00:40:33:159] **Speaker 0:** Um, maybe that's another way that you'd like to, to
[00:40:33:169 - 00:40:34:649] **Speaker 0:** create solutions.
[00:40:36:270 - 00:40:39:110] **Speaker 0:** Alright, but don't be too concerned about it if, if
[00:40:39:110 - 00:40:41:550] **Speaker 0:** that, it's a little bit confusing to think of it
[00:40:41:550 - 00:40:44:949] **Speaker 0:** in those, uh, two-dimensional arrays, you can just stay with
[00:40:44:949 - 00:40:45:729] **Speaker 0:** your four loops.
[00:40:51:179 - 00:40:54:050] **Speaker 0:** Alright, so chapter 5 was really about defining the heat
[00:40:54:050 - 00:40:56:780] **Speaker 0:** equation or deriving it, and then solving it with a
[00:40:56:780 - 00:40:58:179] **Speaker 0:** couple of analytical methods.
[00:40:59:229 - 00:41:03:620] **Speaker 0:** Um, Again, don't be too concerned about the details of
[00:41:03:770 - 00:41:05:919] **Speaker 0:** this, but you, they should all be familiar from your
[00:41:05:919 - 00:41:07:780] **Speaker 0:** math courses, the individual steps.
[00:41:08:120 - 00:41:10:080] **Speaker 0:** I won't be as mean to include such a question
[00:41:10:080 - 00:41:11:399] **Speaker 0:** exam directly.
[00:41:13:489 - 00:41:15:649] **Speaker 0:** Um, but the first case we looked at was the
[00:41:15:649 - 00:41:18:149] **Speaker 0:** separation of variables, and that was reasonably straightforward.
[00:41:19:260 - 00:41:22:239] **Speaker 0:** All right, so we've got a few minutes, um.
[00:41:25:340 - 00:41:28:290] **Speaker 0:** I, since we've already got it open, I just wanted
[00:41:28:290 - 00:41:29:209] **Speaker 0:** to show you.
[00:41:31:060 - 00:41:33:540] **Speaker 0:** In console chapter 2 example 1.
[00:41:33:699 - 00:41:34:050] **Speaker 0:** MPH.
[00:41:34:139 - 00:41:36:060] **Speaker 0:** This is in the chapter 2 folder already on the
[00:41:36:060 - 00:41:37:949] **Speaker 0:** course material on learn.
[00:41:38:699 - 00:41:41:500] **Speaker 0:** But this is just a way of checking your analytical
[00:41:41:500 - 00:41:44:540] **Speaker 0:** solutions to your separation variables so you could solve it.
[00:41:46:110 - 00:41:47:879] **Speaker 0:** This is from chapter 2, so.
[00:41:49:070 - 00:41:53:469] **Speaker 0:** I probably still have the, Let's sit up.
[00:41:58:610 - 00:42:01:439] **Speaker 0:** So example one, so just as a recap, we've got
[00:42:01:439 - 00:42:02:560] **Speaker 0:** this Laplace equation.
[00:42:02:679 - 00:42:04:860] **Speaker 0:** We've got these 4 boundary conditions being applied.
[00:42:05:239 - 00:42:07:360] **Speaker 0:** Uh, so we've got 0s and then we've got the
[00:42:07:360 - 00:42:09:020] **Speaker 0:** sine wave on the right-hand side.
[00:42:10:389 - 00:42:11:219] **Speaker 0:** Uh, so 2 pay.
[00:42:12:229 - 00:42:13:629] **Speaker 0:** So we can solve this in console.
[00:42:13:790 - 00:42:15:629] **Speaker 0:** So I think you have all the steps now to
[00:42:15:629 - 00:42:16:350] **Speaker 0:** understand how to solve it.
[00:42:16:459 - 00:42:18:100] **Speaker 0:** We've got the class equation physics.
[00:42:18:350 - 00:42:20:899] **Speaker 0:** We've got some boundary conditions being imposed on the.
[00:42:22:229 - 00:42:23:889] **Speaker 0:** Left, right, top, bottom.
[00:42:25:929 - 00:42:29:399] **Speaker 0:** Um We've done a parameter suite which we'll talk, uh,
[00:42:29:449 - 00:42:32:139] **Speaker 0:** which you'll play around with in lab 3 this week.
[00:42:33:209 - 00:42:35:659] **Speaker 0:** And I've plotted the console solution.
[00:42:37:139 - 00:42:39:560] **Speaker 0:** As well as the analytical solution.
[00:42:42:889 - 00:42:44:820] **Speaker 0:** The analytical solution is the 2D plot group.
[00:42:46:129 - 00:42:50:300] **Speaker 0:** I've defined the function u_A which varies in X and
[00:42:50:300 - 00:42:55:780] **Speaker 0:** Y, being independent variables, and defined the function up here.
[00:42:56:800 - 00:42:59:620] **Speaker 0:** So this expression is what we derived in class.
[00:43:02:800 - 00:43:08:679] **Speaker 0:** And We can compare these two solutions across our discrete
[00:43:08:679 - 00:43:10:100] **Speaker 0:** space, so finite element space.
[00:43:11:580 - 00:43:13:129] **Speaker 0:** So difference between solutions.
[00:43:14:070 - 00:43:16:909] **Speaker 0:** is as simple as doing one minus the other, so
[00:43:16:909 - 00:43:18:780] **Speaker 0:** subtraction U minus u_A.
[00:43:19:899 - 00:43:23:620] **Speaker 0:** So you is our dependent variable being evaluated across that
[00:43:23:620 - 00:43:27:020] **Speaker 0:** grid, and you under_A needs the arguments X and Y
[00:43:27:020 - 00:43:29:739] **Speaker 0:** because it's taking that analytical function that we just uh
[00:43:29:739 - 00:43:30:739] **Speaker 0:** defined up earlier.
[00:43:32:419 - 00:43:34:540] **Speaker 0:** We can also take the integral.
[00:43:35:209 - 00:43:36:580] **Speaker 0:** So I guess first of all, we can see this
[00:43:36:580 - 00:43:39:959] **Speaker 0:** is a small number, that's 10 to -5 compared to
[00:43:40:459 - 00:43:42:520] **Speaker 0:** on the order of 1 for the actual solution.
[00:43:43:679 - 00:43:46:090] **Speaker 0:** As you refine the mesh, you should see that the
[00:43:46:090 - 00:43:47:129] **Speaker 0:** difference reduces.
[00:43:48:800 - 00:43:52:750] **Speaker 0:** And our surface integration is taking the difference between the
[00:43:52:750 - 00:43:53:159] **Speaker 0:** two.
[00:43:53:439 - 00:43:57:419] **Speaker 0:** We've taken the square, uh, if you think of, um,
[00:43:57:600 - 00:44:00:120] **Speaker 0:** quadratic, well I only just noticed this now, but yeah,
[00:44:00:199 - 00:44:01:719] **Speaker 0:** that's cool, um.
[00:44:03:850 - 00:44:05:649] **Speaker 0:** Yeah, um, so.
[00:44:08:070 - 00:44:08:830] **Speaker 0:** What are we talking about?
[00:44:08:949 - 00:44:11:830] **Speaker 0:** So like if you're fitting a line to a set
[00:44:11:830 - 00:44:15:729] **Speaker 0:** data, um, you use, you use like quadratic loss functions,
[00:44:16:110 - 00:44:18:129] **Speaker 0:** uh, so we can, we can just use the same.
[00:44:18:590 - 00:44:21:189] **Speaker 0:** So it's penalising terms that are further away with a
[00:44:21:189 - 00:44:21:909] **Speaker 0:** squared term.
[00:44:22:270 - 00:44:24:149] **Speaker 0:** It also has the advantage of just making them more
[00:44:24:149 - 00:44:24:500] **Speaker 0:** positive.
[00:44:24:590 - 00:44:26:389] **Speaker 0:** So if you square the difference, it's always going to
[00:44:26:389 - 00:44:26:750] **Speaker 0:** be positive.
[00:44:26:790 - 00:44:28:709] **Speaker 0:** You don't have to worry about taking the absolute value.
[00:44:28:909 - 00:44:31:850] **Speaker 0:** Otherwise it's gonna cancel out positive and negative.
[00:44:33:360 - 00:44:41:100] **Speaker 0:** And also plotted the Integral of that difference over a
[00:44:41:100 - 00:44:44:719] **Speaker 0:** number of degrees of, I think, elements, number of elements.
[00:44:46:679 - 00:44:47:540] **Speaker 0:** In the Y direction.
[00:44:47:800 - 00:44:48:760] **Speaker 0:** So, I don't know.
[00:44:48:879 - 00:44:50:510] **Speaker 0:** There's a few things in there that may be is,
[00:44:50:669 - 00:44:53:580] **Speaker 0:** is helpful for, for the lab this week or um
[00:44:53:639 - 00:44:54:580] **Speaker 0:** to extend your knowledge.
[00:44:55:669 - 00:44:58:870] **Speaker 0:** Or to be more comfortable that your separation of verbal
[00:44:58:870 - 00:44:59:570] **Speaker 0:** questions are correct.
[00:45:01:800 - 00:45:02:479] **Speaker 0:** All right.
[00:45:06:580 - 00:45:08:260] **Speaker 0:** Cool, so that leaves about 5 minutes for you to
[00:45:08:260 - 00:45:08:699] **Speaker 0:** do something.
[00:45:08:969 - 00:45:11:770] **Speaker 0:** Um, so maybe we go through question two.
[00:45:12:100 - 00:45:13:300] **Speaker 0:** So I'm gonna give you a couple of minutes to
[00:45:13:300 - 00:45:15:169] **Speaker 0:** just think about how you can formulate the problem, how,
[00:45:15:300 - 00:45:17:360] **Speaker 0:** how to go about solving this equation.
[00:45:17:739 - 00:45:21:939] **Speaker 0:** We've got, um, separation of variables as our toolkit, and
[00:45:21:939 - 00:45:23:610] **Speaker 0:** we've got the heat equation, and we've got some two
[00:45:23:610 - 00:45:26:800] **Speaker 0:** boundary conditions and an initial condition.
[00:45:27:379 - 00:45:29:120] **Speaker 0:** So you should be able to get some result maybe
[00:45:29:120 - 00:45:29:899] **Speaker 0:** in a couple of minutes.
[00:46:00:010 - 00:46:51:320] **Speaker 1:** that It was That's yeah, that's, that's, that's a big
[00:46:51:320 - 00:46:51:350] **Speaker 1:** thing, yeah.
[00:47:18:459 - 00:47:18:649] **Speaker 0:** Cool.
[00:47:18:739 - 00:47:20:179] **Speaker 0:** Alright, so we've got our problem defined.
[00:47:20:320 - 00:47:23:500] **Speaker 0:** We've got some domain, maybe it's another rod, uh, of
[00:47:23:500 - 00:47:24:360] **Speaker 0:** length L.
[00:47:24:739 - 00:47:26:580] **Speaker 0:** Uh, we've got a Dirichlet boundary condition on the left-hand
[00:47:26:580 - 00:47:29:330] **Speaker 0:** side with a temperature of 0, and then a Neumann
[00:47:29:330 - 00:47:31:780] **Speaker 0:** boundary on the right with setting the gradient to be
[00:47:31:780 - 00:47:32:100] **Speaker 0:** zero.
[00:47:32:219 - 00:47:35:399] **Speaker 0:** So you can recall we talked about heat fluxes, uh,
[00:47:35:419 - 00:47:36:179] **Speaker 0:** dependent on this gradient.
[00:47:36:270 - 00:47:39:290] **Speaker 0:** So if we had zero temperature gradient, we'd expect zero
[00:47:39:290 - 00:47:40:939] **Speaker 0:** flux on that right-hand end.
[00:47:41:219 - 00:47:43:820] **Speaker 0:** And we're given some initial temperature profile that varies with
[00:47:43:820 - 00:47:44:699] **Speaker 0:** sin of x.
[00:47:46:540 - 00:47:47:419] **Speaker 0:** Uh, what's the first step?
[00:47:47:500 - 00:47:49:780] **Speaker 0:** We have to figure out what PDE we're solving.
[00:47:51:429 - 00:47:54:330] **Speaker 0:** So for this heat equation, we're really only analysing one.
[00:47:57:350 - 00:48:00:330] **Speaker 0:** We derived this in class, we've got equation 5.3.
[00:48:03:280 - 00:48:12:580] **Speaker 0:** So, T of X and T equal to a cosine
[00:48:12:760 - 00:48:17:000] **Speaker 0:** lambda X plus B sin lambda X.
[00:48:18:409 - 00:48:21:409] **Speaker 0:** E to the minus alpha, lambda 2 D.
[00:48:23:590 - 00:48:26:649] **Speaker 0:** Uh, so which condition should we analyse first?
[00:48:28:939 - 00:48:30:020] **Speaker 0:** Which would be easiest.
[00:48:35:659 - 00:48:36:000] **Speaker 0:** Yeah.
[00:48:36:570 - 00:48:37:889] **Speaker 0:** So the temperature is 0.
[00:48:37:979 - 00:48:39:820] **Speaker 0:** Hopefully, some terms will fall out, especially for X equal
[00:48:39:820 - 00:48:40:300] **Speaker 0:** to 0.
[00:48:40:739 - 00:48:43:750] **Speaker 0:** So T X equals 0.
[00:48:44:709 - 00:48:45:389] **Speaker 0:** For more time.
[00:48:46:179 - 00:48:48:889] **Speaker 0:** Cosine of 0 is going to go to 1 and
[00:48:48:889 - 00:48:49:820] **Speaker 0:** sin of 0 is 0.
[00:48:49:979 - 00:48:52:379] **Speaker 0:** So we're left with AE to the minus alpha lambda2
[00:48:52:919 - 00:48:53:139] **Speaker 0:** D.
[00:48:58:899 - 00:49:00:540] **Speaker 0:** So this means that A has to be equal to
[00:49:00:540 - 00:49:03:659] **Speaker 0:** 0 for that to hold, uh, the exponential of that
[00:49:03:659 - 00:49:03:879] **Speaker 0:** term.
[00:49:06:070 - 00:49:07:550] **Speaker 0:** Isn't going to be equal to 0.
[00:49:09:239 - 00:49:10:929] **Speaker 0:** So when you see A equal to 0?
[00:49:12:590 - 00:49:16:409] **Speaker 0:** And the next condition is probably going to be that
[00:49:16:409 - 00:49:16:989] **Speaker 0:** right-hand side.
[00:49:17:070 - 00:49:18:169] **Speaker 0:** So X equal to L.
[00:49:19:870 - 00:49:23:270] **Speaker 0:** So DT By DX.
[00:49:24:600 - 00:49:26:500] **Speaker 0:** At X equal to L.
[00:49:28:149 - 00:49:30:110] **Speaker 0:** So we're going to have cosine of lambda.
[00:49:31:149 - 00:49:32:229] **Speaker 0:** X equal to L.
[00:49:37:100 - 00:49:41:879] **Speaker 0:** And we're left with lambda B as the coefficient.
[00:49:42:699 - 00:49:45:889] **Speaker 0:** And E to the minus alpha lambda 2 T.
[00:49:49:969 - 00:49:51:850] **Speaker 0:** So this is evaluating that derivative.
[00:49:52:010 - 00:49:54:209] **Speaker 0:** You might want to figure out the derivative first before
[00:49:54:209 - 00:49:56:810] **Speaker 0:** going to the step, but this is evaluated X equal
[00:49:56:810 - 00:49:57:270] **Speaker 0:** to L.
[00:49:58:860 - 00:50:00:899] **Speaker 0:** Now, this is quite similar to the.
[00:50:01:709 - 00:50:04:739] **Speaker 0:** Uh, quiz 2, I think, instead of using sine term
[00:50:04:739 - 00:50:06:600] **Speaker 0:** that is equal to 0, we now need to set
[00:50:06:600 - 00:50:07:250] **Speaker 0:** cosine.
[00:50:07:679 - 00:50:08:699] **Speaker 0:** So the cosine.
[00:50:10:310 - 00:50:11:379] **Speaker 0:** Of Lambda L.
[00:50:12:110 - 00:50:13:010] **Speaker 0:** Is equal to 0.
[00:50:13:780 - 00:50:17:080] **Speaker 0:** Which means that lambda L has to be multiples.
[00:50:17:830 - 00:50:21:250] **Speaker 0:** Uh, so like it 5 or 2.
[00:50:22:760 - 00:50:25:800] **Speaker 0:** Uh, 3/2, etc.
[00:50:26:159 - 00:50:28:290] **Speaker 0:** so it's gonna be in minus 5.
[00:50:29:280 - 00:50:30:489] **Speaker 0:** Multiplied by pi.
[00:50:32:389 - 00:50:34:030] **Speaker 0:** What does a cosine wave look like?
[00:50:34:149 - 00:50:34:669] **Speaker 0:** um.
[00:50:38:729 - 00:50:40:330] **Speaker 0:** So that.
[00:50:41:399 - 00:50:42:760] **Speaker 0:** Is 5 or 2.
[00:50:43:780 - 00:50:44:659] **Speaker 0:** 3 or 2.
[00:50:50:280 - 00:50:53:439] **Speaker 0:** Um, so we've run out of time, but I guess
[00:50:53:439 - 00:50:56:439] **Speaker 0:** I just wanted to remind you that there are exercises
[00:50:56:439 - 00:50:58:760] **Speaker 0:** at each chapter, and you should go through those.
[00:50:59:600 - 00:51:02:600] **Speaker 0:** Um Uh, I also wanted to cover this as well.
[00:51:02:669 - 00:51:05:510] **Speaker 0:** So if it's cosine, think of the cosine wave and
[00:51:05:510 - 00:51:06:790] **Speaker 0:** where it matches zero.
[00:51:07:679 - 00:51:08:310] **Speaker 0:** All right, cool.
[00:51:08:550 - 00:51:11:899] **Speaker 0:** Uh, so, tomorrow we'll go through chapter 6.
[00:51:58:860 - 00:52:00:030] **Speaker 1:** Uh, yeah.
[00:52:01:540 - 00:52:04:139] **Speaker 1:** No, you just like 2 questions.
[00:52:06:739 - 00:52:09:659] **Speaker 1:** We were quite confused that there's like two initial temperatures,
[00:52:11:040 - 00:52:14:060] **Speaker 1:** so it says the site was initially at 21 and
[00:52:14:060 - 00:52:16:080] **Speaker 1:** then at 0 the surface is infinity.
[00:52:17:219 - 00:52:18:899] **Speaker 1:** Yeah, so it's sort of like a discontinuity.
[00:52:19:060 - 00:52:21:979] **Speaker 1:** So, so it's t infinity at x2.
[00:52:24:419 - 00:52:26:739] **Speaker 1:** What do you mean higher like because if you're talking
[00:52:26:739 - 00:52:31:989] **Speaker 0:** at t infinity would be1 so at exactly x equals
[00:52:31:989 - 00:52:34:399] **Speaker 0:** 0 10 infinity and then like.
[00:52:35:219 - 00:52:39:300] **Speaker 0:** A little bit over, but of those two temperatures, which
[00:52:39:300 - 00:52:40:050] **Speaker 1:** one's higher because that like that.
[00:52:43:520 - 00:52:49:129] **Speaker 1:** higher priority like higher temperature because that's gonna like show
[00:52:49:129 - 00:52:51:780] **Speaker 1:** you which way that the heat's gonna flow, precisely.
[00:52:52:090 - 00:52:54:560] **Speaker 0:** And so yes, if you did it the other way,
[00:52:54:570 - 00:52:56:070] **Speaker 0:** you might have to reverse the order.
[00:52:56:129 - 00:52:57:090] **Speaker 0:** It would be like.
[00:52:57:790 - 00:53:03:989] **Speaker 0:** Um, minus 1, yeah, yeah, so the surface temperature is
[00:53:03:989 - 00:53:05:350] **Speaker 1:** held at 1 infinity.
[00:53:08:030 - 00:53:11:659] **Speaker 0:** Hey, there's going um because we keep drawing it from
[00:53:11:659 - 00:53:11:780] **Speaker 1:** him.
[00:53:12:780 - 00:53:15:340] **Speaker 1:** Stated that like that was a a like a boundary
[00:53:15:340 - 00:53:17:810] **Speaker 1:** condition but it's all good take your time.
[00:53:18:379 - 00:53:20:189] **Speaker 1:** T1 is higher than infinity wise.
[00:53:23:510 - 00:53:24:100] **Speaker 1:** Oh I see.
[00:53:24:270 - 00:53:24:929] **Speaker 1:** Well, that's the.
[00:53:29:629 - 00:53:34:179] **Speaker 1:** which Yes.
[00:53:37:639 - 00:53:37:649] **Speaker 1:** I.
[00:53:45:429 - 00:53:48:229] **Speaker 1:** Because why does it then go to 1 as a
[00:53:48:229 - 00:53:50:389] **Speaker 1:** middle age would not end up being good?
[00:53:51:179 - 00:53:59:629] **Speaker 1:** That's In the city I see something.
[00:54:03:060 - 00:54:03:310] **Speaker 1:** OK.
[00:54:17:199 - 00:54:31:790] **Speaker 1:** But um Me yesterday.
[00:54:45:830 - 00:54:51:699] **Speaker 1:** the And But now

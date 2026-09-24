# ENEL372-26S2 Lecture 25 native Echo transcript

Date: September 21, 2026 4:00pm-4:55pm
Transcript type: native Echo automated transcript.

[00:00:00:689 - 00:00:00:699] **Speaker 0:** Yeah.
[00:00:29:079 - 00:00:29:180] **Speaker 0:** I'm.
[00:00:30:629 - 00:00:35:599] **Speaker 0:** I OK OK, good you keeping count.
[00:00:44:060 - 00:00:44:069] **Speaker 0:** Yeah.
[00:00:47:029 - 00:00:50:840] **Speaker 0:** it's That.
[00:00:54:220 - 00:01:01:799] **Speaker 0:** I yeah OK.
[00:01:03:529 - 00:01:06:209] **Speaker 0:** Yeah, 22 patients.
[00:01:07:059 - 00:01:13:099] **Speaker 0:** Oh All right.
[00:01:14:589 - 00:01:43:730] **Speaker 0:** Yeah you I thought it was 3.
[00:01:49:709 - 00:01:50:269] **Speaker 1:** Hello.
[00:01:52:230 - 00:01:52:930] **Speaker 1:** Still don't rectified.
[00:01:55:029 - 00:01:58:050] **Speaker 1:** I'm just gonna revisit something.
[00:02:18:389 - 00:02:23:410] **Speaker 1:** So yeah, last lecture I derived um this inductor sizing.
[00:02:25:309 - 00:02:33:729] **Speaker 1:** Formula Can anyone remember what's kind of written on here
[00:02:33:729 - 00:02:35:550] **Speaker 1:** but sort of implicitly.
[00:02:36:630 - 00:02:39:509] **Speaker 1:** Do you what was the major assumption I made.
[00:02:40:729 - 00:02:43:740] **Speaker 1:** To be able to derive this analytical formula is my
[00:02:43:740 - 00:02:44:440] **Speaker 1:** question for today.
[00:02:45:440 - 00:02:47:000] **Speaker 1:** It was passively smooth.
[00:02:48:520 - 00:02:50:800] **Speaker 1:** I'd say it's one of the assumptions, it's probably not
[00:02:50:800 - 00:02:53:440] **Speaker 1:** the issue and it's right up there, that's not the
[00:02:53:440 - 00:02:54:300] **Speaker 1:** major assumption.
[00:02:55:119 - 00:02:57:169] **Speaker 1:** It is one of the assumptions, but it's not the
[00:02:57:169 - 00:02:57:990] **Speaker 1:** most critical.
[00:02:59:580 - 00:03:00:160] **Speaker 1:** What's that?
[00:03:01:539 - 00:03:02:330] **Speaker 1:** He what?
[00:03:03:279 - 00:03:04:740] **Speaker 1:** Even, no, no, not even.
[00:03:05:460 - 00:03:06:500] **Speaker 1:** It's actually in there.
[00:03:06:580 - 00:03:07:559] **Speaker 1:** It's in the math.
[00:03:09:570 - 00:03:10:750] **Speaker 0:** Yeah, approximating wave.
[00:03:13:070 - 00:03:13:559] **Speaker 1:** Exactly.
[00:03:14:649 - 00:03:16:889] **Speaker 1:** A + 10 out of 10.
[00:03:19:619 - 00:03:29:610] **Speaker 1:** 100% So, uh, there's obviously other harmonics.
[00:03:29:720 - 00:03:31:850] **Speaker 1:** There's not just the ripple.
[00:03:31:929 - 00:03:35:830] **Speaker 1:** There's like higher harmonics that will be affecting it.
[00:03:37:119 - 00:03:39:029] **Speaker 1:** But it is the predominant.
[00:03:39:979 - 00:03:41:779] **Speaker 1:** Harmonic, and that's the 2nd harmonic.
[00:03:42:020 - 00:03:45:220] **Speaker 1:** And so by assuming that all the ripple, all the
[00:03:45:220 - 00:03:49:139] **Speaker 1:** current ripple is described by the 2nd harmonic, ignoring the
[00:03:49:139 - 00:03:51:820] **Speaker 1:** higher ones, we get this nice little formula here.
[00:03:54:660 - 00:03:56:070] **Speaker 1:** So how good is that formula?
[00:03:57:820 - 00:04:02:259] **Speaker 1:** Uh, well, that's something I didn't actually mention, but um.
[00:04:06:410 - 00:04:08:880] **Speaker 1:** I had a number somewhere, gotta find the number.
[00:04:09:500 - 00:04:10:580] **Speaker 1:** Oh yep, found it.
[00:04:13:169 - 00:04:15:270] **Speaker 1:** So, and Alti Spice.
[00:04:16:910 - 00:04:19:570] **Speaker 1:** Does anyone want to guess what what was the um
[00:04:19:989 - 00:04:21:130] **Speaker 1:** minimum L value?
[00:04:22:058 - 00:04:23:589] **Speaker 1:** That's the actual true value.
[00:04:25:510 - 00:04:27:519] **Speaker 1:** Do you reckon they'd be close or be out by
[00:04:27:519 - 00:04:27:799] **Speaker 1:** a bit?
[00:04:29:640 - 00:04:30:570] **Speaker 1:** Do you reckon it's the same?
[00:04:34:700 - 00:04:35:850] **Speaker 1:** Shouldn't be the same, right?
[00:04:36:829 - 00:04:41:720] **Speaker 1:** Because I suppose it's hard to.
[00:04:43:040 - 00:04:45:390] **Speaker 1:** Do you think it'll be greater or smaller, the true
[00:04:45:390 - 00:04:45:670] **Speaker 1:** one?
[00:04:47:730 - 00:04:48:959] **Speaker 1:** She better at least figure that out.
[00:04:50:739 - 00:04:51:200] **Speaker 1:** What?
[00:04:51:980 - 00:04:54:420] **Speaker 1:** Yep, I assume you had a reason for it, or
[00:04:54:420 - 00:04:55:200] **Speaker 1:** is that a guess?
[00:04:58:750 - 00:05:02:859] **Speaker 1:** Productive so Yeah, yeah.
[00:05:02:980 - 00:05:04:950] **Speaker 1:** So your, your gut feeling was right, but to be
[00:05:04:950 - 00:05:05:440] **Speaker 1:** specific.
[00:05:06:649 - 00:05:09:700] **Speaker 1:** This is only assuming the second harmonic, so it would
[00:05:09:700 - 00:05:11:660] **Speaker 1:** make sense that if it was just a 2nd harmonic,
[00:05:11:700 - 00:05:13:579] **Speaker 1:** there'd be less ripple than if there was other harmonics,
[00:05:13:660 - 00:05:15:079] **Speaker 1:** so you'd have a smaller inductor.
[00:05:15:850 - 00:05:18:209] **Speaker 1:** So you'd expect there to be a larger inductor in
[00:05:18:209 - 00:05:19:149] **Speaker 1:** the real world.
[00:05:19:730 - 00:05:21:989] **Speaker 1:** Well, that you can call Alti Spice the real world.
[00:05:23:510 - 00:05:26:450] **Speaker 1:** And LT Spice, yes, it's higher.
[00:05:29:950 - 00:05:31:149] **Speaker 1:** It's 0.23.
[00:05:33:049 - 00:05:36:089] **Speaker 1:** So that is reasonable, that's.
[00:05:36:910 - 00:05:39:200] **Speaker 1:** What, 0.02 divided by.
[00:05:42:609 - 00:05:44:540] **Speaker 1:** I think that's, it's actually 10% error.
[00:05:44:959 - 00:05:49:410] **Speaker 1:** So that's a reasonable error, 10% error, but not too
[00:05:49:410 - 00:05:49:690] **Speaker 1:** bad.
[00:05:50:079 - 00:05:51:029] **Speaker 1:** Like it's pretty good.
[00:05:51:649 - 00:05:53:109] **Speaker 1:** So you're getting a 10% error.
[00:05:56:679 - 00:05:58:670] **Speaker 1:** Um, in the local formula.
[00:06:07:910 - 00:06:10:670] **Speaker 1:** If you're doing, I suppose, aerospace applications, you would worry,
[00:06:10:750 - 00:06:12:910] **Speaker 1:** but for most applications in the ground you wouldn't care.
[00:06:13:070 - 00:06:14:589] **Speaker 1:** Probably even for the solar car, if you had a
[00:06:14:589 - 00:06:18:230] **Speaker 1:** 10% slightly more windings, you're probably not gonna worry.
[00:06:18:670 - 00:06:22:470] **Speaker 1:** Depends on what, um, extra mass that you can get
[00:06:22:470 - 00:06:24:230] **Speaker 1:** and how big the inductor is overall, and this one's
[00:06:24:230 - 00:06:26:809] **Speaker 1:** actually quite big, so I guess going from 0.21 to
[00:06:26:809 - 00:06:30:950] **Speaker 1:** 0.23 could add some non-trivial amount of mass.
[00:06:34:309 - 00:06:36:850] **Speaker 1:** But mostly it's, it's good enough.
[00:06:38:839 - 00:06:40:320] **Speaker 1:** So yeah, that's that.
[00:06:42:459 - 00:06:43:540] **Speaker 1:** And then I'm just going to finish with this.
[00:06:46:190 - 00:06:47:540] **Speaker 1:** So I'm gonna go just a little bit on the
[00:06:47:540 - 00:06:48:679] **Speaker 1:** capacitance design.
[00:06:51:170 - 00:06:55:640] **Speaker 1:** And then we're Gonna move on.
[00:07:00:010 - 00:07:01:209] **Speaker 1:** And so on this.
[00:07:04:859 - 00:07:08:839] **Speaker 1:** We have that comes from the GFS.
[00:07:24:220 - 00:07:26:519] **Speaker 1:** That was from the transfer function that we derived.
[00:07:27:589 - 00:07:31:369] **Speaker 1:** Treating the The load or treating it as an LCR
[00:07:31:369 - 00:07:31:869] **Speaker 1:** philtre.
[00:07:33:320 - 00:07:35:820] **Speaker 1:** And so you, the rectifier, and so I'll just, just,
[00:07:35:950 - 00:07:37:179] **Speaker 1:** just to remind you.
[00:07:38:529 - 00:07:46:350] **Speaker 1:** This We have the AC that we're getting from the
[00:07:46:350 - 00:07:50:230] **Speaker 1:** mains or from um rotating propeller on the plane.
[00:07:52:410 - 00:07:54:489] **Speaker 1:** And then we have the rectifier, which is the full
[00:07:54:489 - 00:07:57:859] **Speaker 1:** bridge rectifier, which like Yeah.
[00:07:59:279 - 00:08:00:000] **Speaker 1:** Rectifies that.
[00:08:00:239 - 00:08:02:549] **Speaker 1:** Then I'm treating this as the input into an LCR
[00:08:02:549 - 00:08:02:929] **Speaker 1:** philtre.
[00:08:03:839 - 00:08:06:320] **Speaker 1:** So then the LCR philtre, if this is voltage then
[00:08:06:320 - 00:08:11:149] **Speaker 1:** the capacitor would mostly remove all that ripple and the
[00:08:11:149 - 00:08:11:839] **Speaker 1:** DC side.
[00:08:14:779 - 00:08:17:200] **Speaker 1:** And so if you were designing the capacitor.
[00:08:18:350 - 00:08:21:109] **Speaker 1:** To try and get a given amount of ripple like
[00:08:21:109 - 00:08:22:450] **Speaker 1:** you have done on a solar car.
[00:08:24:820 - 00:08:29:369] **Speaker 1:** You can Do it this way First of all, you
[00:08:29:369 - 00:08:30:709] **Speaker 1:** want to see what effect.
[00:08:33:070 - 00:08:35:619] **Speaker 1:** would say in a change in conductance or capacitance have
[00:08:35:619 - 00:08:36:690] **Speaker 1:** on the natural frequency.
[00:08:38:590 - 00:08:40:049] **Speaker 1:** Cause if you're designing a philtre.
[00:08:42:249 - 00:08:46:039] **Speaker 1:** That would be Orange is your cutoff frequency, so it's
[00:08:46:039 - 00:08:49:208] **Speaker 1:** you know where you're going like that if you so
[00:08:49:208 - 00:08:49:948] **Speaker 1:** if you wanna.
[00:08:51:030 - 00:08:53:140] **Speaker 1:** If you were trying to attenuate something at say 100
[00:08:53:140 - 00:08:53:460] **Speaker 1:** Hz.
[00:08:54:530 - 00:08:57:130] **Speaker 1:** You'd want to have that on the green quite small.
[00:08:57:169 - 00:08:58:570] **Speaker 1:** You want to move it to the left, so you
[00:08:58:570 - 00:09:00:690] **Speaker 1:** want the green to decrease because that would mean you
[00:09:00:690 - 00:09:02:390] **Speaker 1:** get more attenuation on the 100 Hz.
[00:09:03:679 - 00:09:05:969] **Speaker 1:** And how do you decrease omega N, what would you
[00:09:05:969 - 00:09:06:270] **Speaker 1:** do?
[00:09:13:950 - 00:09:16:640] **Speaker 1:** Yeah, so it's, it's in the maths, but it makes
[00:09:16:640 - 00:09:19:659] **Speaker 1:** intuitive sense as well because you've increased your capacity, you'll
[00:09:19:659 - 00:09:21:599] **Speaker 1:** know that you're gonna smooth out more of the voltage
[00:09:21:599 - 00:09:23:799] **Speaker 1:** ripple if you increase the inductance you're gonna smooth out
[00:09:23:799 - 00:09:24:820] **Speaker 1:** more of the current ripple.
[00:09:26:450 - 00:09:28:309] **Speaker 1:** And that's exactly what happened, so.
[00:09:30:099 - 00:09:35:140] **Speaker 1:** In this case, I'll just say L increases, just an
[00:09:35:140 - 00:09:35:659] **Speaker 1:** example.
[00:09:36:679 - 00:09:38:349] **Speaker 1:** Then Irene is going to decrease.
[00:09:42:260 - 00:09:43:380] **Speaker 1:** So larger.
[00:09:44:010 - 00:09:45:969] **Speaker 1:** E or Jesus.
[00:09:49:210 - 00:09:53:530] **Speaker 1:** I'm And improves.
[00:09:54:880 - 00:09:56:000] **Speaker 1:** Attenuation.
[00:09:59:210 - 00:10:02:809] **Speaker 1:** Of philtre In this case.
[00:10:04:559 - 00:10:06:859] **Speaker 1:** Would be the current that would be the most interesting
[00:10:07:599 - 00:10:08:559] **Speaker 1:** for for doing that.
[00:10:12:309 - 00:10:14:429] **Speaker 1:** So you wanna it's the yeah for for the voltage
[00:10:14:429 - 00:10:17:450] **Speaker 1:** you always wanna increase the gas so increasing the capacitance
[00:10:17:450 - 00:10:18:809] **Speaker 1:** also reduces our marine.
[00:10:19:859 - 00:10:21:299] **Speaker 1:** And so I said there.
[00:10:21:419 - 00:10:23:640] **Speaker 1:** Um, so let's actually have a look.
[00:10:24:400 - 00:10:25:900] **Speaker 1:** Uh maybe I'll just plot this as you look at
[00:10:25:900 - 00:10:27:530] **Speaker 1:** so at 100 here just so you can visualise it's
[00:10:27:530 - 00:10:28:570] **Speaker 1:** hard sometimes to see.
[00:10:29:340 - 00:10:32:229] **Speaker 1:** 20 log 10 of GFJ I you know, like that's
[00:10:32:229 - 00:10:32:750] **Speaker 1:** the math.
[00:10:34:340 - 00:10:37:109] **Speaker 1:** But if you remember doing Bodie plots when you did
[00:10:37:109 - 00:10:37:969] **Speaker 1:** control systems.
[00:10:41:460 - 00:10:47:760] **Speaker 1:** Then, um If you've done any philtre design.
[00:10:50:270 - 00:10:51:489] **Speaker 1:** So you have your frequency.
[00:10:52:780 - 00:10:54:590] **Speaker 1:** But this could be in hertz or ratings per second,
[00:10:54:630 - 00:10:55:710] **Speaker 1:** but so that was in hertz.
[00:10:57:729 - 00:11:03:099] **Speaker 1:** Then you would have your Cutoff frequency.
[00:11:08:960 - 00:11:10:590] **Speaker 1:** And then you've got to be careful because it might,
[00:11:10:960 - 00:11:13:320] **Speaker 1:** it's a 2nd order, it's a 2nd order philtre, so
[00:11:13:320 - 00:11:15:520] **Speaker 1:** you don't want the i to be too small, otherwise,
[00:11:15:640 - 00:11:16:919] **Speaker 1:** you know, it comes up like this and then it
[00:11:16:919 - 00:11:17:760] **Speaker 1:** like ducks down.
[00:11:20:719 - 00:11:22:570] **Speaker 1:** But sometimes it's good to hear that because it'll actually,
[00:11:22:809 - 00:11:24:809] **Speaker 1:** there's a little bit of a bump here it'll come
[00:11:24:809 - 00:11:25:549] **Speaker 1:** down faster.
[00:11:26:539 - 00:11:29:520] **Speaker 1:** But um you normally you'd wanna have that quite small.
[00:11:30:450 - 00:11:33:109] **Speaker 1:** In case you were amplifying noise that would be around
[00:11:33:109 - 00:11:35:169] **Speaker 1:** this frequency because you got to be careful, you don't
[00:11:35:169 - 00:11:37:010] **Speaker 1:** want it to be too much of a, it's called
[00:11:37:010 - 00:11:39:609] **Speaker 1:** ripple you see and a philtre anything that.
[00:11:40:280 - 00:11:43:619] **Speaker 1:** It's kind of within the past band is is also
[00:11:44:070 - 00:11:46:739] **Speaker 1:** called ripple though it's actually a different type of ripple.
[00:11:47:229 - 00:11:49:000] **Speaker 1:** It's not the ripple in the time domain, which is
[00:11:49:000 - 00:11:51:380] **Speaker 1:** I'm talking about voltage ripples in the time domain.
[00:11:51:880 - 00:11:53:320] **Speaker 1:** But when you start, and I do this in the
[00:11:53:320 - 00:11:55:650] **Speaker 1:** in the next week or two, maybe a couple of
[00:11:55:650 - 00:11:56:020] **Speaker 1:** weeks.
[00:11:57:140 - 00:12:01:150] **Speaker 1:** Um Yeah, you have like ripple in the past ban
[00:12:01:150 - 00:12:03:789] **Speaker 1:** and ripple in the stop ban and that's all philtre
[00:12:03:789 - 00:12:04:409] **Speaker 1:** terminology.
[00:12:06:369 - 00:12:07:340] **Speaker 1:** And there's always trade-offs.
[00:12:07:380 - 00:12:09:659] **Speaker 1:** You have more ripple in the pass band, and then
[00:12:09:659 - 00:12:10:679] **Speaker 1:** you have greater attenuation.
[00:12:11:770 - 00:12:14:010] **Speaker 1:** Or if you want to have less attenuation, you can
[00:12:14:010 - 00:12:15:099] **Speaker 1:** maybe have better past being.
[00:12:19:289 - 00:12:21:179] **Speaker 1:** And so this distance here that.
[00:12:23:039 - 00:12:28:719] **Speaker 1:** It depends On the za and you can manipulate xy
[00:12:28:719 - 00:12:30:520] **Speaker 1:** by changing resistance capacity to conductance.
[00:12:30:609 - 00:12:33:010] **Speaker 1:** So I'm keeping the resistance fixed and I'm assuming it's
[00:12:33:010 - 00:12:34:229] **Speaker 1:** like a motor load or something.
[00:12:35:080 - 00:12:36:119] **Speaker 1:** In this particular case.
[00:12:36:969 - 00:12:38:049] **Speaker 1:** But you could change resistance.
[00:12:38:099 - 00:12:39:159] **Speaker 1:** You could add resistance.
[00:12:41:099 - 00:12:44:070] **Speaker 1:** But adding resistance normally um is not the greatest idea
[00:12:44:070 - 00:12:47:130] **Speaker 1:** because you are Unless you're doing something like a voltage
[00:12:47:130 - 00:12:48:169] **Speaker 1:** divider, but um.
[00:12:50:520 - 00:12:53:479] **Speaker 1:** You wouldn't just add resistance cos that's just means more
[00:12:53:479 - 00:12:56:200] **Speaker 1:** heat loss, so you get less efficiency.
[00:12:58:440 - 00:13:02:020] **Speaker 1:** So you choose C to get.
[00:13:03:770 - 00:13:06:549] **Speaker 1:** As much attenuation.
[00:13:09:440 - 00:13:13:669] **Speaker 1:** Is possible within whatever design criteria you've got.
[00:13:16:000 - 00:13:19:039] **Speaker 1:** Cost, weight, a whole lot of factors that come into
[00:13:19:039 - 00:13:19:299] **Speaker 1:** it.
[00:13:21:830 - 00:13:25:400] **Speaker 1:** And 100 hits So you can see here that as
[00:13:25:400 - 00:13:27:440] **Speaker 1:** you move this down here this whole thing's gonna move
[00:13:27:440 - 00:13:29:239] **Speaker 1:** to the left and then you get more and more
[00:13:29:239 - 00:13:31:179] **Speaker 1:** attenuation as this thing goes left.
[00:13:33:039 - 00:13:34:700] **Speaker 1:** And so the way I do that mathematically.
[00:13:36:280 - 00:13:37:239] **Speaker 1:** So that's to visualise.
[00:13:37:289 - 00:13:39:450] **Speaker 1:** This is just to visualise the maths.
[00:13:44:299 - 00:13:47:820] **Speaker 1:** You plug in S equals omega, so if I call
[00:13:47:820 - 00:13:48:780] **Speaker 1:** this equation one.
[00:13:49:520 - 00:13:51:260] **Speaker 1:** So here you're just substitute.
[00:13:54:010 - 00:13:57:330] **Speaker 1:** S equals omega 0 J into the transfer function.
[00:13:58:070 - 00:14:00:539] **Speaker 1:** And you can now see times like JMG squared.
[00:14:01:820 - 00:14:05:390] **Speaker 1:** And that becomes negative because it's a -1.
[00:14:07:020 - 00:14:08:659] **Speaker 1:** And so on, you know like it cancels out and
[00:14:08:659 - 00:14:10:020] **Speaker 1:** you get the 1 and then you get the L
[00:14:10:020 - 00:14:10:640] **Speaker 1:** over R.
[00:14:11:739 - 00:14:18:349] **Speaker 1:** So you get that Then That can be like put
[00:14:18:349 - 00:14:20:669] **Speaker 1:** into here, you can take the square of that, you
[00:14:20:669 - 00:14:22:400] **Speaker 1:** can put the square in here just to to do
[00:14:22:400 - 00:14:22:609] **Speaker 1:** that.
[00:14:25:049 - 00:14:25:770] **Speaker 1:** And so on.
[00:14:26:710 - 00:14:28:539] **Speaker 1:** So I've put, I've put in some values here.
[00:14:29:820 - 00:14:31:880] **Speaker 1:** So if an inductors of 0.2.
[00:14:32:700 - 00:14:35:390] **Speaker 1:** And that's close to the continuous conduction, so it's an
[00:14:36:380 - 00:14:37:200] **Speaker 1:** interesting design case.
[00:14:38:559 - 00:14:40:159] **Speaker 1:** That's if I chose R 200.
[00:14:40:270 - 00:14:43:469] **Speaker 1:** I can't remember if it was 200 before, but this
[00:14:43:469 - 00:14:46:159] **Speaker 1:** is just a set of examples, just an example set.
[00:14:46:599 - 00:14:49:280] **Speaker 1:** Plug it into here and you get 0.14 attenuation.
[00:14:49:640 - 00:14:50:659] **Speaker 1:** So that's significant.
[00:14:51:119 - 00:14:52:719] **Speaker 1:** That's huge.
[00:14:52:840 - 00:14:55:619] **Speaker 1:** That's quite a large attenuation at the 100 hertz.
[00:14:55:679 - 00:14:56:380] **Speaker 1:** That's pretty good.
[00:15:00:390 - 00:15:02:929] **Speaker 1:** Now this is using the theory.
[00:15:04:609 - 00:15:06:989] **Speaker 1:** And the theory is obviously just an approximation.
[00:15:09:419 - 00:15:11:559] **Speaker 1:** And so again, I just check here, what is it,
[00:15:11:700 - 00:15:13:880] **Speaker 1:** how does it work in practise?
[00:15:15:000 - 00:15:17:880] **Speaker 1:** We in my practical example is LT Spice, that's that's
[00:15:17:880 - 00:15:18:700] **Speaker 1:** my real world.
[00:15:21:070 - 00:15:23:479] **Speaker 1:** And It's pretty close.
[00:15:24:020 - 00:15:28:380] **Speaker 1:** It's 019.03 was the tree value that attenuated, so it's
[00:15:28:380 - 00:15:30:099] **Speaker 1:** a little bit out but really, really good.
[00:15:31:950 - 00:15:33:780] **Speaker 1:** And so my capacit is designed.
[00:15:34:460 - 00:15:40:219] **Speaker 1:** Yeah, reduced the amplitude from 138 volts down to 18.9.
[00:15:41:159 - 00:15:41:650] **Speaker 1:** Pretty good.
[00:15:42:539 - 00:15:44:739] **Speaker 1:** So I'm happy with that and I got close to
[00:15:44:739 - 00:15:45:559] **Speaker 1:** the LT Spice.
[00:15:47:020 - 00:15:48:450] **Speaker 1:** So these calculations work.
[00:15:49:150 - 00:15:49:729] **Speaker 1:** They're useful.
[00:15:52:539 - 00:15:53:380] **Speaker 1:** And I found that.
[00:15:55:349 - 00:15:57:010] **Speaker 1:** Now, 3 fees rectifiers.
[00:16:00:049 - 00:16:00:469] **Speaker 1:** Fun.
[00:16:04:809 - 00:16:06:549] **Speaker 1:** So I'm not going to go into too much detail.
[00:16:06:599 - 00:16:08:989] **Speaker 1:** I'm just going to go a little bit through some
[00:16:08:989 - 00:16:12:450] **Speaker 1:** of the The basics of what diodes are conducting, but
[00:16:12:450 - 00:16:14:429] **Speaker 1:** I'm not going to spend too much time on that
[00:16:14:429 - 00:16:15:549] **Speaker 1:** because it's not examinable.
[00:16:16:250 - 00:16:18:780] **Speaker 1:** That particular detailed analysis, but I just put it there
[00:16:18:780 - 00:16:21:940] **Speaker 1:** really just for reference and to just get an overall
[00:16:21:940 - 00:16:23:330] **Speaker 1:** view of what actually happens.
[00:16:24:109 - 00:16:29:789] **Speaker 1:** In each phase, what's conducting Uh, what's not conducting.
[00:16:30:409 - 00:16:33:229] **Speaker 1:** And I've done it for 3 of the phases.
[00:16:34:659 - 00:16:36:539] **Speaker 1:** And then I've got a list of rule of thumbs
[00:16:36:539 - 00:16:38:520] **Speaker 1:** to try and understand what's going on.
[00:16:41:580 - 00:16:46:280] **Speaker 1:** Uh, so yeah, 3-phase rectifiers commonly in this power range.
[00:16:47:400 - 00:16:49:979] **Speaker 1:** You get a much smoother DC side voltage.
[00:16:51:150 - 00:16:52:710] **Speaker 1:** And you get it much smoother because you get way
[00:16:52:710 - 00:16:53:409] **Speaker 1:** higher frequency.
[00:16:55:239 - 00:16:58:169] **Speaker 1:** So instead of having two pulses per period, because instead
[00:16:58:169 - 00:17:00:450] **Speaker 1:** of being the second harmonic, right, which was what our
[00:17:00:450 - 00:17:01:669] **Speaker 1:** assumption before for ripple.
[00:17:02:349 - 00:17:03:929] **Speaker 1:** It is now the 6th harmonic.
[00:17:05:239 - 00:17:06:500] **Speaker 1:** And so you were getting.
[00:17:08:969 - 00:17:12:729] **Speaker 1:** Um, yeah, so instead of getting 2 pulses per period,
[00:17:13:170 - 00:17:15:630] **Speaker 1:** you're getting 6 pulses per period.
[00:17:16:369 - 00:17:18:790] **Speaker 1:** So you're getting higher frequency, which means you can, uh,
[00:17:18:930 - 00:17:20:030] **Speaker 1:** much more easily philtre.
[00:17:20:329 - 00:17:22:329] **Speaker 1:** So you get a smoother DC voltage for the same
[00:17:22:329 - 00:17:26:290] **Speaker 1:** size capacitor, you would get a way smoother DC side
[00:17:26:290 - 00:17:27:030] **Speaker 1:** voltage.
[00:17:28:180 - 00:17:32:199] **Speaker 1:** For a three-phase rectifier compared to a single phase rectifier.
[00:17:35:020 - 00:17:37:739] **Speaker 1:** You would also get you end up getting a better
[00:17:37:739 - 00:17:41:319] **Speaker 1:** AC side current, which means it's closer to a sine
[00:17:41:319 - 00:17:41:699] **Speaker 1:** wave.
[00:17:44:410 - 00:17:47:489] **Speaker 1:** So here's an example of the sort of waveforms you
[00:17:47:489 - 00:17:47:829] **Speaker 1:** get.
[00:17:50:750 - 00:17:52:430] **Speaker 1:** And the way I think about it.
[00:17:54:140 - 00:17:56:819] **Speaker 1:** Cause you know it it it comes around uh and
[00:17:56:819 - 00:17:58:479] **Speaker 1:** there's different combinations.
[00:17:59:140 - 00:18:01:260] **Speaker 1:** Red, blue come around the red and back into the
[00:18:01:260 - 00:18:02:819] **Speaker 1:** blue, could come into the red back into the green,
[00:18:02:939 - 00:18:04:660] **Speaker 1:** could start with the green, go back into the blue.
[00:18:06:109 - 00:18:13:209] **Speaker 1:** Uh It's really the upper bound.
[00:18:13:969 - 00:18:20:489] **Speaker 1:** That drives where the positive voltage is going, or it's
[00:18:20:489 - 00:18:23:489] **Speaker 1:** kind of driving the, because the potential difference of voltage
[00:18:23:489 - 00:18:24:410] **Speaker 1:** that drives current.
[00:18:25:189 - 00:18:28:069] **Speaker 1:** And so that top one kind of tells you what
[00:18:28:069 - 00:18:30:109] **Speaker 1:** direction the current's going to flow because it's the highest
[00:18:30:109 - 00:18:30:750] **Speaker 1:** voltage.
[00:18:32:849 - 00:18:35:050] **Speaker 1:** And that's the red, when the red is going to
[00:18:35:050 - 00:18:35:750] **Speaker 1:** positive.
[00:18:36:739 - 00:18:39:479] **Speaker 1:** You're gonna be flowing out of the red because the
[00:18:39:479 - 00:18:42:459] **Speaker 1:** potential difference to the other power supplies are lower, so
[00:18:42:459 - 00:18:47:969] **Speaker 1:** you'd expect when the red, Is the maximum voltage current
[00:18:47:969 - 00:18:48:920] **Speaker 1:** flows out of it.
[00:18:50:329 - 00:18:54:810] **Speaker 1:** And then it's gonna flow into the minimum voltage.
[00:18:55:770 - 00:18:57:810] **Speaker 1:** Not the next moment, like not the middle one.
[00:18:57:890 - 00:18:59:670] **Speaker 1:** It's always going to flow to the lowest.
[00:19:00:459 - 00:19:03:719] **Speaker 1:** Voltage And expect that too cause you're gonna have the
[00:19:03:719 - 00:19:06:680] **Speaker 1:** most negative is going to be where the flow is
[00:19:06:680 - 00:19:07:439] **Speaker 1:** going to go into.
[00:19:09:329 - 00:19:10:670] **Speaker 1:** So that's how that works.
[00:19:12:069 - 00:19:14:959] **Speaker 1:** So Upper band of voltages.
[00:19:18:239 - 00:19:21:099] **Speaker 1:** characterises the positive current flow.
[00:19:26:579 - 00:19:32:160] **Speaker 1:** Out of The source That's associated with whatever is the
[00:19:32:160 - 00:19:32:630] **Speaker 1:** upper bound.
[00:19:36:500 - 00:19:39:060] **Speaker 1:** And then uh if I just want a room here.
[00:19:39:989 - 00:19:45:829] **Speaker 1:** Lower band A voltages.
[00:19:47:839 - 00:19:49:420] **Speaker 1:** Is the negative current.
[00:19:51:229 - 00:19:52:030] **Speaker 1:** Flow.
[00:19:54:569 - 00:19:57:050] **Speaker 1:** Out of the source associated with whenever it's the lower
[00:19:57:050 - 00:19:57:410] **Speaker 1:** bound.
[00:20:01:939 - 00:20:06:849] **Speaker 1:** So 0 to 60 Re Is is flowing at a
[00:20:06:849 - 00:20:07:349] **Speaker 1:** red.
[00:20:08:140 - 00:20:09:310] **Speaker 1:** It's going through D1.
[00:20:11:839 - 00:20:16:119] **Speaker 1:** And then, yeah, it comes around and it'll go through.
[00:20:17:020 - 00:20:20:979] **Speaker 1:** The green because the green's the lowest and it's first
[00:20:20:979 - 00:20:22:540] **Speaker 1:** from 0 to 60 so it'll come out of the
[00:20:22:540 - 00:20:24:140] **Speaker 1:** red and it'll go flow into the green so it
[00:20:24:140 - 00:20:25:680] **Speaker 1:** would go like that.
[00:20:27:239 - 00:20:29:400] **Speaker 1:** And then under here and then back into the green.
[00:20:29:959 - 00:20:32:739] **Speaker 1:** So that's what happens between 0 and 60.
[00:20:33:619 - 00:20:34:089] **Speaker 1:** See that?
[00:20:35:569 - 00:20:38:130] **Speaker 1:** Then between 60 and 120.
[00:20:40:209 - 00:20:42:430] **Speaker 1:** The red's still the highest, so the red's gonna still
[00:20:42:430 - 00:20:43:250] **Speaker 1:** be flowing like this.
[00:20:43:369 - 00:20:47:770] **Speaker 1:** So D1 is still forward biassed so it's um it's
[00:20:47:770 - 00:20:48:750] **Speaker 1:** getting current flow.
[00:20:49:530 - 00:20:52:099] **Speaker 1:** So it's coming around here, but it's gonna switch now.
[00:20:52:180 - 00:20:55:300] **Speaker 1:** Instead of going through D6 um as the voltage is
[00:20:55:300 - 00:20:56:000] **Speaker 1:** increasing.
[00:20:56:800 - 00:20:59:400] **Speaker 1:** Then this becomes reverse bias actually then the blue then
[00:20:59:400 - 00:21:02:959] **Speaker 1:** starts to receive flow so it goes through the D2
[00:21:03:239 - 00:21:03:689] **Speaker 1:** like that.
[00:21:04:599 - 00:21:05:270] **Speaker 1:** And so on.
[00:21:05:319 - 00:21:06:900] **Speaker 1:** You can run through all the different things.
[00:21:09:180 - 00:21:11:819] **Speaker 1:** And I'll do a little bit more detail just on
[00:21:11:819 - 00:21:12:719] **Speaker 1:** the slides.
[00:21:13:790 - 00:21:15:869] **Speaker 1:** So just before I do that I thought I'd just
[00:21:15:869 - 00:21:18:489] **Speaker 1:** give you a visualisation, sometimes it's easy to visualise.
[00:21:19:500 - 00:21:22:560] **Speaker 1:** Well, these NASA t-shirts, they're really great actually, but that's
[00:21:22:560 - 00:21:23:280] **Speaker 1:** for something else.
[00:21:25:020 - 00:21:25:540] **Speaker 1:** Um.
[00:21:26:430 - 00:21:29:020] **Speaker 1:** my colleague from Marshall Space Flight centre is here.
[00:21:29:839 - 00:21:31:140] **Speaker 1:** I might as well mention it because he's doing a
[00:21:31:140 - 00:21:33:280] **Speaker 1:** seminar next week and you're all invited in this class,
[00:21:33:359 - 00:21:35:719] **Speaker 1:** so this will go on echo and I'll send a
[00:21:35:719 - 00:21:36:400] **Speaker 1:** message out.
[00:21:37:280 - 00:21:38:439] **Speaker 1:** I want lots of students here.
[00:21:39:489 - 00:21:40:670] **Speaker 1:** It's going to be next Monday.
[00:21:42:369 - 00:21:42:829] **Speaker 1:** Just explain me.
[00:21:44:489 - 00:21:46:689] **Speaker 1:** But I'll send a message out somehow.
[00:21:48:140 - 00:21:54:160] **Speaker 1:** Uh, He'll be talking about the latest in the SLS,
[00:21:54:239 - 00:21:55:959] **Speaker 1:** the big NASA missions like the one that went around
[00:21:55:959 - 00:21:58:439] **Speaker 1:** the moon, and then like moon bases and Mars and
[00:21:58:439 - 00:21:59:959] **Speaker 1:** you name it, it should be cool.
[00:22:04:810 - 00:22:06:670] **Speaker 1:** I just came from a lecture just before.
[00:22:08:550 - 00:22:09:229] **Speaker 1:** And why not.
[00:22:10:790 - 00:22:19:640] **Speaker 1:** Mm Uh, I'll just have to go guess, I think.
[00:22:22:400 - 00:22:22:780] **Speaker 1:** Yeah.
[00:22:25:140 - 00:22:26:479] **Speaker 1:** Uh, it's still going.
[00:22:27:469 - 00:22:28:390] **Speaker 1:** Well, it's doing.
[00:22:30:959 - 00:22:38:300] **Speaker 1:** I will Pro I done that, no, it's preparing windows.
[00:22:39:510 - 00:22:41:310] **Speaker 1:** I'll move on until it's um.
[00:22:44:000 - 00:22:44:310] **Speaker 1:** See.
[00:22:45:170 - 00:22:50:869] **Speaker 1:** Uh, It's actually quite fast at loading.
[00:22:53:140 - 00:22:56:619] **Speaker 1:** So, let's have a look at this video.
[00:23:07:459 - 00:23:09:449] **Speaker 1:** I don't know, it depends what's how your brain works.
[00:23:09:790 - 00:23:12:109] **Speaker 1:** Whether you can, if you just say follow the yellow,
[00:23:12:189 - 00:23:14:189] **Speaker 1:** I might just pause it because it's really hard to,
[00:23:14:390 - 00:23:15:910] **Speaker 1:** I'll wait till it gets to the yellow again.
[00:23:16:859 - 00:23:17:280] **Speaker 1:** There.
[00:23:17:699 - 00:23:19:599] **Speaker 1:** Alright, so you can see it's on the yellow.
[00:23:20:060 - 00:23:21:839] **Speaker 1:** So you'd expect that's the high voltage.
[00:23:22:640 - 00:23:27:589] **Speaker 1:** And then Can you see you see that, um, so
[00:23:27:589 - 00:23:30:670] **Speaker 1:** you'd expect that there'll be a flow out of this
[00:23:30:670 - 00:23:31:209] **Speaker 1:** coil here.
[00:23:31:310 - 00:23:34:079] **Speaker 1:** It should be going this way and you'll see, yep,
[00:23:34:229 - 00:23:36:310] **Speaker 1:** it goes that way, but then it'll stop and then
[00:23:36:310 - 00:23:38:119] **Speaker 1:** it'll start to flow back again, see?
[00:23:38:589 - 00:23:39:800] **Speaker 1:** And you wait for the yellow, then it'll start to
[00:23:39:800 - 00:23:43:229] **Speaker 1:** flow again and then it's gonna stop and then it's
[00:23:43:229 - 00:23:44:270] **Speaker 1:** gonna go back the other way.
[00:23:44:390 - 00:23:46:550] **Speaker 1:** So if you follow one of those and you can
[00:23:46:550 - 00:23:49:709] **Speaker 1:** see this is another way of kind of visualising where
[00:23:49:709 - 00:23:51:270] **Speaker 1:** they flipped the whole thing around.
[00:23:51:349 - 00:23:52:949] **Speaker 1:** It just makes it a little bit easier sometimes to
[00:23:52:949 - 00:23:53:510] **Speaker 1:** see here.
[00:23:54:140 - 00:23:56:819] **Speaker 1:** And you can see here, even with all these like
[00:23:56:819 - 00:24:03:369] **Speaker 1:** say the magenta here, if you wait, um, Now it's
[00:24:03:369 - 00:24:04:319] **Speaker 1:** gonna be flowing.
[00:24:05:290 - 00:24:07:180] **Speaker 1:** And go back, yeah, so.
[00:24:08:130 - 00:24:11:420] **Speaker 1:** It's just obviously just keeping constant flow around the load.
[00:24:13:140 - 00:24:14:859] **Speaker 1:** So I don't know if that's useful, but I'll stick
[00:24:14:859 - 00:24:17:780] **Speaker 1:** it online, it's just kind of a visualisation of how
[00:24:17:780 - 00:24:18:560] **Speaker 1:** a three-phase.
[00:24:19:520 - 00:24:20:099] **Speaker 1:** Works.
[00:24:20:390 - 00:24:21:430] **Speaker 1:** It's pretty neat here.
[00:24:22:359 - 00:24:25:199] **Speaker 1:** He it just keeps the current flowing continuously through the
[00:24:25:199 - 00:24:27:420] **Speaker 1:** load though you do get a ripple.
[00:24:28:660 - 00:24:31:540] **Speaker 1:** And that's just sort of to do with the magnetic
[00:24:31:540 - 00:24:32:520] **Speaker 1:** fields and how.
[00:24:33:660 - 00:24:35:500] **Speaker 1:** Yeah, how it works, you get, you're always going to
[00:24:35:500 - 00:24:37:819] **Speaker 1:** get some sort of a ripple in the current depending
[00:24:37:819 - 00:24:40:140] **Speaker 1:** on how size big the inductors are.
[00:24:41:479 - 00:24:41:880] **Speaker 1:** All right.
[00:24:43:800 - 00:24:45:339] **Speaker 1:** So, I had to show you.
[00:24:47:010 - 00:24:48:849] **Speaker 1:** I'll just take this out cos then I'll just leave
[00:24:48:849 - 00:24:49:510] **Speaker 1:** it in there.
[00:24:52:199 - 00:24:52:209] **Speaker 1:** Right.
[00:24:57:410 - 00:24:57:810] **Speaker 1:** All right.
[00:25:05:130 - 00:25:07:390] **Speaker 1:** So let's analyse this in a little bit more detail.
[00:25:14:479 - 00:25:16:920] **Speaker 1:** So between 0 and 60, remember, the voltage was the
[00:25:16:920 - 00:25:20:140] **Speaker 1:** highest, so you're getting like cause everything's initially 0, then
[00:25:20:140 - 00:25:22:339] **Speaker 1:** it starts to rise, voltage gets high.
[00:25:23:500 - 00:25:27:180] **Speaker 1:** And then this diode becomes full bias, so basically I'm
[00:25:27:180 - 00:25:27:900] **Speaker 1:** saying it disappears.
[00:25:27:939 - 00:25:30:670] **Speaker 1:** That's why I've kind of deleted the diode because and
[00:25:30:670 - 00:25:32:770] **Speaker 1:** I'm not worrying about diode drops now, I'm just saying.
[00:25:34:119 - 00:25:36:260] **Speaker 1:** Yeah, it's just going to start smoothing going through here.
[00:25:37:479 - 00:25:39:680] **Speaker 1:** Because initially 0 everywhere so that when you turn it
[00:25:39:680 - 00:25:42:089] **Speaker 1:** on that delivers a positive current through the D1.
[00:25:43:300 - 00:25:45:260] **Speaker 1:** And as soon as it goes through there, you get
[00:25:45:260 - 00:25:48:000] **Speaker 1:** the VR is gonna appear above here.
[00:25:48:760 - 00:25:50:869] **Speaker 1:** Above D2 and D3.
[00:25:52:760 - 00:25:55:050] **Speaker 1:** Uh, and then you're back because you know the green
[00:25:55:050 - 00:25:56:890] **Speaker 1:** is the most negative, so the negative flows into the
[00:25:56:890 - 00:25:57:040] **Speaker 1:** green.
[00:25:57:089 - 00:25:59:010] **Speaker 1:** You can see the bold face here is where it's
[00:25:59:010 - 00:26:00:390] **Speaker 1:** going for the first phase.
[00:26:02:030 - 00:26:07:530] **Speaker 1:** And so the VG is gonna immediately appear here.
[00:26:11:040 - 00:26:11:760] **Speaker 1:** And.
[00:26:13:359 - 00:26:16:170] **Speaker 1:** Yeah, so the Fiji creates the negative current flow, so
[00:26:16:170 - 00:26:17:430] **Speaker 1:** that's the, that's that.
[00:26:18:339 - 00:26:20:640] **Speaker 1:** And then yeah, so I've just, I've just described that.
[00:26:23:060 - 00:26:24:750] **Speaker 1:** Uh, so, yeah, D.
[00:26:25:660 - 00:26:30:469] **Speaker 1:** For In D3.
[00:26:31:349 - 00:26:34:069] **Speaker 1:** They are reverse biassed.
[00:26:37:920 - 00:26:39:130] **Speaker 1:** And that's because VG.
[00:26:40:719 - 00:26:42:020] **Speaker 1:** As it is in VB.
[00:26:44:239 - 00:26:45:949] **Speaker 1:** We know that because that's.
[00:26:47:790 - 00:26:49:859] **Speaker 1:** Yeah, that's just because that's what it is.
[00:26:50:069 - 00:26:51:949] **Speaker 1:** VG is less than VB because you can see that
[00:26:51:949 - 00:26:56:030] **Speaker 1:** on the line that The VG is the very lowest,
[00:26:56:150 - 00:26:58:989] **Speaker 1:** the VB is the middle, and the V red is
[00:26:58:989 - 00:26:59:849] **Speaker 1:** the highest.
[00:27:00:430 - 00:27:02:729] **Speaker 1:** So you know that VG is less than VR.
[00:27:03:650 - 00:27:09:689] **Speaker 1:** You should know that If this is less than VR
[00:27:10:239 - 00:27:12:550] **Speaker 1:** then yeah, you can't, it's not gonna get you're not
[00:27:12:550 - 00:27:15:550] **Speaker 1:** gonna get like it becomes reverse biassed.
[00:27:17:339 - 00:27:17:619] **Speaker 1:** Sorry.
[00:27:17:859 - 00:27:18:650] **Speaker 1:** Oh, actually, what did I say?
[00:27:18:780 - 00:27:19:140] **Speaker 1:** Sorry, sorry.
[00:27:19:280 - 00:27:20:680] **Speaker 1:** VG is less than VB.
[00:27:21:300 - 00:27:22:099] **Speaker 1:** I wrote that.
[00:27:22:500 - 00:27:23:859] **Speaker 1:** It's just like, it's weird.
[00:27:23:979 - 00:27:24:260] **Speaker 1:** Sorry.
[00:27:26:430 - 00:27:30:030] **Speaker 1:** Um, Yeah, so VG is less than VB.
[00:27:35:560 - 00:27:38:280] **Speaker 1:** And so you can't go to the higher voltage because
[00:27:38:280 - 00:27:39:920] **Speaker 1:** it's going to be reverse biassed.
[00:27:40:719 - 00:27:43:359] **Speaker 1:** To get obviously get a current flow across the D3,
[00:27:43:640 - 00:27:45:520] **Speaker 1:** this forage would have to become greater than that.
[00:27:45:760 - 00:27:47:680] **Speaker 1:** So you have to wait till later in the phase
[00:27:47:680 - 00:27:49:880] **Speaker 1:** before the VG becomes greater than the VB and then
[00:27:49:880 - 00:27:52:000] **Speaker 1:** it would flow through that, but it hasn't so it
[00:27:52:000 - 00:27:52:739] **Speaker 1:** reverse bias.
[00:27:54:189 - 00:27:57:969] **Speaker 1:** Uh, and VG will be less than VR.
[00:27:59:489 - 00:28:01:180] **Speaker 1:** But all, all of these, so VG.
[00:28:02:550 - 00:28:05:869] **Speaker 1:** Is this in VR that was the 2nd 1, yeah,
[00:28:06:030 - 00:28:06:410] **Speaker 1:** that's cool.
[00:28:07:689 - 00:28:11:449] **Speaker 1:** Alright, so the top diodes VG VR is greater than
[00:28:11:449 - 00:28:13:709] **Speaker 1:** VG, so D3 is reverse biassed.
[00:28:15:739 - 00:28:19:140] **Speaker 1:** Can't get flow backwards through a dio, the virus is
[00:28:19:140 - 00:28:21:599] **Speaker 1:** not gonna be able to go through there, right, obviously.
[00:28:22:739 - 00:28:25:040] **Speaker 1:** Uh, VR is greater than VB.
[00:28:25:969 - 00:28:29:349] **Speaker 1:** D5 can't get any flow so they're shut off.
[00:28:30:930 - 00:28:33:229] **Speaker 1:** And then the same for the bottom two diodes.
[00:28:33:920 - 00:28:35:959] **Speaker 1:** And it's all just got to do with this reverse
[00:28:35:959 - 00:28:36:479] **Speaker 1:** biassing.
[00:28:36:520 - 00:28:40:079] **Speaker 1:** You can just work that out by looking at the
[00:28:40:079 - 00:28:42:369] **Speaker 1:** colours, the colour coding on this.
[00:28:43:000 - 00:28:43:920] **Speaker 1:** So that's what I've done.
[00:28:44:939 - 00:28:47:819] **Speaker 1:** And you can figure through every single phase, what diodes
[00:28:47:819 - 00:28:49:699] **Speaker 1:** are conducting, what diodes are reversed bias.
[00:28:49:780 - 00:28:52:300] **Speaker 1:** It's all done from the colours, and which is greater
[00:28:52:300 - 00:28:53:180] **Speaker 1:** than, yeah.
[00:28:53:819 - 00:28:54:699] **Speaker 1:** It's reasonably straightforward.
[00:28:54:739 - 00:28:57:000] **Speaker 1:** It's a bit tedious to actually go through and analyse
[00:28:57:300 - 00:28:59:619] **Speaker 1:** in detail every single phase.
[00:29:00:790 - 00:29:02:150] **Speaker 1:** And so you won't be required to do that in
[00:29:02:150 - 00:29:05:069] **Speaker 1:** the exam, of course, but it's useful just to get
[00:29:05:069 - 00:29:07:030] **Speaker 1:** a bit of a picture for how all the different
[00:29:07:030 - 00:29:07:810] **Speaker 1:** phases.
[00:29:08:939 - 00:29:11:959] **Speaker 1:** Kind of contribute to a flow through the through the
[00:29:11:959 - 00:29:12:640] **Speaker 1:** through the load.
[00:29:15:300 - 00:29:17:420] **Speaker 1:** And the same thing here, I've explained here.
[00:29:17:500 - 00:29:19:699] **Speaker 1:** The next phase from 60 to 120.
[00:29:20:300 - 00:29:23:079] **Speaker 1:** Again, this is gonna keep this is still the maximum
[00:29:23:739 - 00:29:26:770] **Speaker 1:** from uh 60 to 120, still the maximum.
[00:29:26:849 - 00:29:27:780] **Speaker 1:** But now it's switched.
[00:29:27:819 - 00:29:29:930] **Speaker 1:** So the green before was less than the blue, but
[00:29:29:930 - 00:29:31:300] **Speaker 1:** now the blue is less than the green.
[00:29:31:660 - 00:29:33:619] **Speaker 1:** So the blue becomes the one that receives the current.
[00:29:36:839 - 00:29:39:250] **Speaker 1:** And so on, and I've, I've explained it here.
[00:29:39:290 - 00:29:40:810] **Speaker 1:** I'm not going to go too much into that.
[00:29:41:900 - 00:29:43:989] **Speaker 1:** And you can see how the top diodes, all of
[00:29:43:989 - 00:29:44:569] **Speaker 1:** these.
[00:29:45:369 - 00:29:47:589] **Speaker 1:** Say for example VR is greater than VG.
[00:29:48:010 - 00:29:50:170] **Speaker 1:** You can just see that from the colour here, VR
[00:29:50:170 - 00:29:51:349] **Speaker 1:** is greater than VG.
[00:29:52:170 - 00:29:52:890] **Speaker 1:** And so on.
[00:29:54:310 - 00:29:55:670] **Speaker 1:** Explained it as well as I can.
[00:29:55:750 - 00:29:56:930] **Speaker 1:** Hopefully you can follow that.
[00:30:00:319 - 00:30:02:819] **Speaker 1:** And I've done another one here.
[00:30:03:359 - 00:30:04:040] **Speaker 1:** So then.
[00:30:04:930 - 00:30:07:239] **Speaker 1:** Eventually the red completely stops.
[00:30:07:329 - 00:30:08:709] **Speaker 1:** That's why I've concluded this.
[00:30:10:160 - 00:30:11:609] **Speaker 1:** The red doesn't flow anymore.
[00:30:11:839 - 00:30:12:680] **Speaker 1:** It's completely shut off.
[00:30:12:719 - 00:30:15:099] **Speaker 1:** There's no ability for any flow from the red.
[00:30:18:329 - 00:30:22:430] **Speaker 1:** And That goes to zero current flow and actually I've
[00:30:22:430 - 00:30:23:280] **Speaker 1:** plotted the current here.
[00:30:23:310 - 00:30:25:709] **Speaker 1:** It goes to 0 current flow, so it's only conducting
[00:30:25:709 - 00:30:31:849] **Speaker 1:** for Like Overall, probably 2/3 of the.
[00:30:32:579 - 00:30:33:449] **Speaker 1:** Is that 2/3?
[00:30:33:959 - 00:30:35:729] **Speaker 1:** It's about 2/3 of the cycle.
[00:30:36:250 - 00:30:36:969] **Speaker 1:** It's conducting.
[00:30:41:800 - 00:30:43:420] **Speaker 1:** Anything else I need to say there?
[00:30:44:119 - 00:30:44:619] **Speaker 1:** No.
[00:30:45:260 - 00:30:46:880] **Speaker 1:** I'll let you have a look through that.
[00:30:47:079 - 00:30:48:369] **Speaker 1:** Just mainly the rules of the thumb.
[00:30:50:180 - 00:30:51:599] **Speaker 1:** I've already said those two.
[00:30:55:209 - 00:30:57:630] **Speaker 1:** Yeah, the, the other one, like in practise it does
[00:30:57:630 - 00:31:01:489] **Speaker 1:** there maybe there could be other effects, but basically it
[00:31:01:489 - 00:31:05:810] **Speaker 1:** has negative effects, so The other voter sources virtually doing
[00:31:05:810 - 00:31:08:890] **Speaker 1:** nothing when two of the voter sources are providing the
[00:31:08:890 - 00:31:09:150] **Speaker 1:** current.
[00:31:09:979 - 00:31:11:260] **Speaker 1:** It's just sitting there, it's just.
[00:31:12:189 - 00:31:15:400] **Speaker 1:** Yeah, not contributing to any current flow.
[00:31:17:150 - 00:31:19:219] **Speaker 1:** Only 2 dies are conducted in in time.
[00:31:19:270 - 00:31:21:229] **Speaker 1:** You can see that in all 3 cases.
[00:31:22:270 - 00:31:24:219] **Speaker 1:** We're only getting 2 diodes that are conducting.
[00:31:25:270 - 00:31:28:270] **Speaker 1:** Even though it's a 3 phase and there's There's like
[00:31:28:270 - 00:31:31:589] **Speaker 1:** way more diodes here cause we're looking at 3-phase, there's
[00:31:31:589 - 00:31:32:750] **Speaker 1:** only 2 that are conducting.
[00:31:35:170 - 00:31:37:329] **Speaker 1:** Some of the voltages are always at zero, and as
[00:31:37:329 - 00:31:42:959] **Speaker 1:** I said before, I know that's each individual diode conducts
[00:31:43:140 - 00:31:48:339] **Speaker 1:** for 1/3 of the time, but then the flow, the
[00:31:48:339 - 00:31:52:339] **Speaker 1:** contribution from that power supply would be 2/3, like 1/3
[00:31:52:339 - 00:31:54:180] **Speaker 1:** of the time it'll be positive flow, and then the
[00:31:54:180 - 00:31:56:500] **Speaker 1:** other 1/3 would be negative flow back into VR for
[00:31:56:500 - 00:31:56:959] **Speaker 1:** example.
[00:32:01:089 - 00:32:03:140] **Speaker 1:** But I won't be testing you on that sort of
[00:32:03:140 - 00:32:03:329] **Speaker 1:** thing.
[00:32:03:410 - 00:32:05:650] **Speaker 1:** Like it's not what I ask in the exam at
[00:32:05:650 - 00:32:05:989] **Speaker 1:** all.
[00:32:06:489 - 00:32:08:410] **Speaker 1:** But I think it's good that you understand how all
[00:32:08:410 - 00:32:10:719] **Speaker 1:** the mechanics of how the three-phase works.
[00:32:10:739 - 00:32:12:930] **Speaker 1:** It's just a little bit more trickier obviously than the
[00:32:12:930 - 00:32:13:540] **Speaker 1:** single phase.
[00:32:13:959 - 00:32:15:410] **Speaker 1:** Single phase is really straightforward to understand.
[00:32:15:489 - 00:32:17:010] **Speaker 1:** This is just a little bit more tricky.
[00:32:19:209 - 00:32:21:069] **Speaker 1:** It's just a little bit more time and thought.
[00:32:22:020 - 00:32:24:790] **Speaker 1:** But it's the same principles as a single face.
[00:32:26:119 - 00:32:27:910] **Speaker 1:** So I didn't really need to say anything there.
[00:32:28:250 - 00:32:31:140] **Speaker 1:** No one's asking any questions, so that's a good sign.
[00:32:32:790 - 00:32:34:439] **Speaker 1:** And I printed out this the wrong, the wrong way,
[00:32:34:510 - 00:32:35:949] **Speaker 1:** but anyway, um.
[00:32:37:459 - 00:32:39:949] **Speaker 1:** Plot current and voltage waveforms for a three-phase rectifier with
[00:32:39:949 - 00:32:41:030] **Speaker 1:** constant current load.
[00:32:41:150 - 00:32:44:469] **Speaker 1:** Yes, that will certainly be in the exam.
[00:32:45:849 - 00:32:48:390] **Speaker 1:** Compare the current draw for a constant current load.
[00:32:49:449 - 00:32:51:459] **Speaker 1:** This is a resistance resistor load.
[00:32:52:060 - 00:32:55:319] **Speaker 1:** Yes, uh, you would, what would I ask in that
[00:32:55:319 - 00:32:55:959] **Speaker 1:** compare.
[00:32:56:869 - 00:32:59:180] **Speaker 1:** If I may ask, I might say what could be
[00:32:59:180 - 00:32:59:640] **Speaker 1:** the difference?
[00:33:01:160 - 00:33:03:209] **Speaker 1:** In the wave form, you may have to describe it
[00:33:03:209 - 00:33:05:140] **Speaker 1:** with English or you may have to, I may have
[00:33:05:140 - 00:33:06:569] **Speaker 1:** a question that tests you.
[00:33:07:349 - 00:33:10:290] **Speaker 1:** Your understanding of what a constant current load is and
[00:33:10:290 - 00:33:12:729] **Speaker 1:** what impact that has on the current draw, so definitely
[00:33:12:729 - 00:33:14:369] **Speaker 1:** there could be a wordy question like that.
[00:33:15:099 - 00:33:16:760] **Speaker 1:** So you need to be able to have a comparison
[00:33:16:760 - 00:33:17:380] **Speaker 1:** between the two.
[00:33:17:729 - 00:33:19:869] **Speaker 1:** That's definitely a learning outcome that's examinable.
[00:33:21:290 - 00:33:24:010] **Speaker 1:** Compare the current draw and the output voltage again, it's
[00:33:24:010 - 00:33:25:209] **Speaker 1:** the same sort of thing.
[00:33:25:250 - 00:33:26:589] **Speaker 1:** I'm just repeating it for.
[00:33:27:979 - 00:33:33:030] **Speaker 1:** For voltage, Um, both current draw and output voltage for
[00:33:33:030 - 00:33:35:310] **Speaker 1:** a constant voltage load versus RC load, so yep.
[00:33:37:010 - 00:33:39:239] **Speaker 1:** a single-phase current metrics to three phase definitely.
[00:33:42:180 - 00:33:45:180] **Speaker 1:** I don't normally, I probably wouldn't get you to.
[00:33:46:849 - 00:33:49:209] **Speaker 1:** Uh, maybe maybe I could say plot.
[00:33:50:060 - 00:33:54:500] **Speaker 1:** The metric for a three-phase I'm not worried about actual
[00:33:54:500 - 00:33:54:780] **Speaker 1:** numbers.
[00:33:54:819 - 00:33:56:160] **Speaker 1:** I'm more worried about trends.
[00:33:56:459 - 00:33:58:660] **Speaker 1:** I think I said in the previous lecture that for
[00:33:58:660 - 00:34:01:380] **Speaker 1:** example if I showed if I asked you to plot
[00:34:01:380 - 00:34:09:179] **Speaker 1:** the THD versus Load Say constant voltage or constant current
[00:34:09:179 - 00:34:09:510] **Speaker 1:** load.
[00:34:10:209 - 00:34:15:770] **Speaker 1:** Um, for various loads, then you would plot the THD
[00:34:15:770 - 00:34:18:128] **Speaker 1:** would be higher, like it would probably just decrease most
[00:34:18:128 - 00:34:19:110] **Speaker 1:** of the time it decreases.
[00:34:19:949 - 00:34:22:128] **Speaker 1:** Um, the 3 phase would be sorry.
[00:34:22:959 - 00:34:23:878] **Speaker 1:** It would be lower.
[00:34:24:169 - 00:34:26:638] **Speaker 1:** Yeah, so the THD versus, so it could be something
[00:34:26:638 - 00:34:27:120] **Speaker 1:** like this.
[00:34:27:850 - 00:34:31:179] **Speaker 1:** THD In some load, I don't know.
[00:34:33:070 - 00:34:34:469] **Speaker 1:** It might be like.
[00:34:35:529 - 00:34:38:638] **Speaker 1:** That and that, and you would say this is like
[00:34:38:638 - 00:34:39:658] **Speaker 1:** a three-phase.
[00:34:40:780 - 00:34:42:138] **Speaker 1:** And this is single face.
[00:34:45:689 - 00:34:47:158] **Speaker 1:** That's what I mean by compare.
[00:34:47:469 - 00:34:48:840] **Speaker 1:** So yeah, that's in the exam as well.
[00:34:54:759 - 00:34:58:709] **Speaker 1:** So let's start off with the This case, this is
[00:34:58:709 - 00:35:04:879] **Speaker 1:** still looking actually at the um So 3 phase, it's
[00:35:04:879 - 00:35:07:010] **Speaker 1:** the same thing, but I've still got a constant current
[00:35:07:010 - 00:35:07:469] **Speaker 1:** load.
[00:35:10:750 - 00:35:12:260] **Speaker 1:** So I've got my constant current load.
[00:35:15:330 - 00:35:16:770] **Speaker 1:** Just uh looking at.
[00:35:19:139 - 00:35:20:459] **Speaker 1:** More how do you get this waveform.
[00:35:20:540 - 00:35:22:300] **Speaker 1:** This is also something you'd need to be able to
[00:35:22:300 - 00:35:23:600] **Speaker 1:** plot in an exam situation.
[00:35:25:000 - 00:35:29:100] **Speaker 1:** I might say, can you plot the current flow through
[00:35:29:100 - 00:35:30:159] **Speaker 1:** the first diode?
[00:35:31:159 - 00:35:33:199] **Speaker 1:** In a 3-phase, so you need to know how to
[00:35:33:199 - 00:35:33:590] **Speaker 1:** do that.
[00:35:36:459 - 00:35:40:020] **Speaker 1:** For a constant current flow, but what if it, If
[00:35:40:020 - 00:35:43:350] **Speaker 1:** it wasn't If it was just a big inductor like
[00:35:43:350 - 00:35:45:389] **Speaker 1:** you gotta be careful like it because the symbol here
[00:35:45:389 - 00:35:47:610] **Speaker 1:** shows you exact constant current, yes you would do this,
[00:35:47:669 - 00:35:49:050] **Speaker 1:** which means it's exactly straight.
[00:35:50:770 - 00:35:53:340] **Speaker 1:** But if this was an inductor and it wasn't inductively
[00:35:53:340 - 00:35:57:320] **Speaker 1:** smooth, then you would have to have some ripple here.
[00:35:57:780 - 00:35:59:909] **Speaker 1:** So you would have just so some ripple as it
[00:35:59:969 - 00:36:02:320] **Speaker 1:** it'll definitely go to zero but you'd be getting ripple.
[00:36:03:570 - 00:36:04:030] **Speaker 1:** Iran.
[00:36:05:449 - 00:36:07:500] **Speaker 1:** And yeah you're taking the voltage here, you're taking the
[00:36:07:500 - 00:36:10:409] **Speaker 1:** voltage here, and it's the potential difference that gives you
[00:36:10:409 - 00:36:10:820] **Speaker 1:** this.
[00:36:11:100 - 00:36:14:260] **Speaker 1:** This is really nice cause you remember the single phase
[00:36:14:260 - 00:36:16:179] **Speaker 1:** it actually goes to zero and it comes back down.
[00:36:16:260 - 00:36:19:500] **Speaker 1:** We hear it's already up, like it's already nicely kind
[00:36:19:500 - 00:36:23:729] **Speaker 1:** of smoothish compared to like massive changes in voltage, right?
[00:36:24:830 - 00:36:28:560] **Speaker 1:** So just 3 phase is just really amazing for.
[00:36:29:389 - 00:36:30:649] **Speaker 1:** And 65 is even better.
[00:36:35:439 - 00:36:38:159] **Speaker 1:** So nothing much more to say on that slide, just
[00:36:38:159 - 00:36:39:300] **Speaker 1:** showing you some pretty pictures.
[00:36:41:929 - 00:36:43:989] **Speaker 1:** You need to be able to obviously do all that.
[00:36:47:010 - 00:36:48:899] **Speaker 1:** So let's do the constant current load.
[00:36:50:010 - 00:36:52:530] **Speaker 1:** And compare the two compare with the resistor load.
[00:36:54:760 - 00:36:56:510] **Speaker 1:** It's exactly what I said, like if it's not, well
[00:36:56:510 - 00:36:59:209] **Speaker 1:** in this case it's a it's a resistive low so
[00:36:59:209 - 00:37:00:350] **Speaker 1:** you are gonna get ripple.
[00:37:04:370 - 00:37:06:219] **Speaker 1:** But it's a very small amount of ripple.
[00:37:09:090 - 00:37:10:209] **Speaker 1:** So this is an interesting case.
[00:37:10:370 - 00:37:13:770] **Speaker 1:** So even though I've got a resistive load and it
[00:37:13:770 - 00:37:16:050] **Speaker 1:** would be really hard to do like all the math
[00:37:16:050 - 00:37:16:870] **Speaker 1:** analysis.
[00:37:17:669 - 00:37:22:290] **Speaker 1:** Um To work out all the THD and everything with
[00:37:22:290 - 00:37:24:540] **Speaker 1:** if there was ripple, you could assume that it was
[00:37:24:540 - 00:37:27:620] **Speaker 1:** a constant load and you'd get very similar THD.
[00:37:27:739 - 00:37:29:719] **Speaker 1:** The THD wouldn't change much.
[00:37:30:929 - 00:37:33:260] **Speaker 1:** Whether you had ripple or you didn't, in this case,
[00:37:33:409 - 00:37:34:169] **Speaker 1:** for a three-phase.
[00:37:37:669 - 00:37:40:949] **Speaker 1:** I'm only showing just kind of waving my hands here.
[00:37:42:159 - 00:37:44:320] **Speaker 1:** But I want you to see visually that they look
[00:37:44:320 - 00:37:44:820] **Speaker 1:** similar.
[00:37:47:790 - 00:37:50:370] **Speaker 1:** So for constant resistance.
[00:37:54:510 - 00:37:56:370] **Speaker 1:** There's certainly a little bit of ripple there.
[00:38:04:250 - 00:38:08:310] **Speaker 1:** Current ripple, this is not, I'm not looking at voltage
[00:38:08:310 - 00:38:09:580] **Speaker 1:** here, I'm looking at current.
[00:38:10:250 - 00:38:11:989] **Speaker 1:** And I'm looking at current through the load.
[00:38:14:790 - 00:38:15:929] **Speaker 1:** But it's essentially constant.
[00:38:26:949 - 00:38:28:909] **Speaker 1:** So that's a really nice thing, so you can assume
[00:38:28:909 - 00:38:33:530] **Speaker 1:** you have a constant current load and it actually captures
[00:38:34:300 - 00:38:36:030] **Speaker 1:** most things that happen with the resistive load.
[00:38:39:719 - 00:38:42:280] **Speaker 1:** And I'll just make a note here that uh it's
[00:38:42:280 - 00:38:45:209] **Speaker 1:** a very close match, even though I haven't actually measured
[00:38:45:209 - 00:38:45:600] **Speaker 1:** anything here.
[00:38:46:330 - 00:38:48:120] **Speaker 1:** You can see with your own eyes, it's very close.
[00:38:52:540 - 00:38:53:780] **Speaker 1:** You get similar FFT.
[00:38:54:100 - 00:38:56:459] **Speaker 1:** There'd be higher frequencies in this one, but they'd be
[00:38:56:459 - 00:38:59:340] **Speaker 1:** at much lower amplitude so it wouldn't have a major
[00:38:59:340 - 00:39:00:840] **Speaker 1:** effect on the THD.
[00:39:08:350 - 00:39:10:340] **Speaker 1:** But this is harder to analyse.
[00:39:11:500 - 00:39:15:219] **Speaker 1:** There's more, there's more kind of smaller harmonics that you
[00:39:15:219 - 00:39:16:229] **Speaker 1:** don't really care about.
[00:39:17:300 - 00:39:18:949] **Speaker 1:** Because they're not affecting the overall THD.
[00:39:21:959 - 00:39:24:260] **Speaker 1:** And this is what I'll call a minimal model.
[00:39:28:479 - 00:39:30:580] **Speaker 1:** Simpler to analyse.
[00:39:38:399 - 00:39:42:229] **Speaker 1:** It's really interesting that in many cases, you can still
[00:39:42:229 - 00:39:44:870] **Speaker 1:** have a constant current load, and it actually works for
[00:39:44:870 - 00:39:45:760] **Speaker 1:** certain analysis.
[00:39:47:790 - 00:39:48:669] **Speaker 1:** So that was nice.
[00:39:55:199 - 00:39:58:500] **Speaker 1:** So they're equivalent in terms of the current draw analysis.
[00:39:59:820 - 00:40:02:600] **Speaker 1:** And also the, the load of the current load.
[00:40:07:649 - 00:40:08:149] **Speaker 1:** Yeah.
[00:40:10:020 - 00:40:11:219] **Speaker 1:** Constant voltage.
[00:40:13:729 - 00:40:15:830] **Speaker 1:** Let's try a constant voltage load.
[00:40:19:639 - 00:40:21:600] **Speaker 1:** And we're gonna add a bit of sauce inductance here.
[00:40:31:840 - 00:40:33:870] **Speaker 1:** So what I'm doing in this particular one is I'm
[00:40:33:870 - 00:40:35:860] **Speaker 1:** doing a circuit equivalence.
[00:40:40:820 - 00:40:45:070] **Speaker 1:** And so we have that has got like 2 inductors.
[00:40:48:780 - 00:40:49:659] **Speaker 1:** In the past.
[00:40:59:229 - 00:40:59:489] **Speaker 1:** Right.
[00:41:03:320 - 00:41:04:379] **Speaker 1:** So in here.
[00:41:07:669 - 00:41:09:909] **Speaker 1:** What I've done is.
[00:41:10:770 - 00:41:12:820] **Speaker 1:** Again, like these, you could just do this in Alti
[00:41:12:820 - 00:41:13:280] **Speaker 1:** Spice.
[00:41:15:020 - 00:41:18:760] **Speaker 1:** But it's quite, it can be quite tricky and slow
[00:41:18:760 - 00:41:19:419] **Speaker 1:** to analyse.
[00:41:19:540 - 00:41:21:540] **Speaker 1:** This is just a like a a quite a interesting
[00:41:21:540 - 00:41:27:280] **Speaker 1:** fast way of, Doing everything you need to do.
[00:41:28:120 - 00:41:31:479] **Speaker 1:** Without having to do the full analysis on that beast.
[00:41:35:169 - 00:41:36:080] **Speaker 1:** It's just much easier.
[00:41:38:340 - 00:41:39:060] **Speaker 1:** Yeah.
[00:41:39:860 - 00:41:42:389] **Speaker 1:** I think that's called a behavioural voltage.
[00:41:42:780 - 00:41:43:879] **Speaker 1:** They're such great things.
[00:41:44:899 - 00:41:47:360] **Speaker 1:** So the behavioural voltage.
[00:41:48:580 - 00:41:50:090] **Speaker 1:** behavioural.
[00:41:51:570 - 00:41:52:389] **Speaker 1:** Voltage.
[00:41:53:199 - 00:41:56:639] **Speaker 1:** There's a BV uh thing when you type BB or
[00:41:56:639 - 00:41:58:479] **Speaker 1:** something or if you look up the the components in
[00:41:58:479 - 00:41:59:199] **Speaker 1:** Altispice.
[00:42:00:929 - 00:42:03:929] **Speaker 1:** It allows you to put a mathematical definition for the
[00:42:03:929 - 00:42:04:550] **Speaker 1:** voltage.
[00:42:07:090 - 00:42:09:239] **Speaker 1:** I actually made quite a lot of use of that
[00:42:09:239 - 00:42:13:129] **Speaker 1:** in in the 494 chip that I developed that you
[00:42:13:129 - 00:42:15:810] **Speaker 1:** used for the solar power, solar powered car.
[00:42:17:850 - 00:42:23:280] **Speaker 1:** And so what I've done here is I've Created A
[00:42:23:280 - 00:42:24:969] **Speaker 1:** voltage, which is going to be.
[00:42:26:570 - 00:42:30:550] **Speaker 1:** The absolute value of of all these, but I've actually
[00:42:30:550 - 00:42:31:810] **Speaker 1:** just done it in 3 parts.
[00:42:35:959 - 00:42:39:939] **Speaker 1:** And then I've taken the max of all the maximums.
[00:42:40:280 - 00:42:42:939] **Speaker 1:** So essentially what this is doing is a mathematical formula
[00:42:43:760 - 00:42:46:830] **Speaker 1:** for Getting this function here.
[00:42:46:909 - 00:42:49:310] **Speaker 1:** It's really like it would be really difficult to try
[00:42:49:310 - 00:42:50:570] **Speaker 1:** and describe this.
[00:42:51:679 - 00:42:55:040] **Speaker 1:** I did initially try it with heavy side functions and
[00:42:55:040 - 00:42:56:629] **Speaker 1:** you got to work out when it's going to go,
[00:42:56:679 - 00:42:58:709] **Speaker 1:** when it's going to cross to when you're going to
[00:42:58:709 - 00:42:59:870] **Speaker 1:** switch from one side to the other.
[00:42:59:919 - 00:43:01:800] **Speaker 1:** It's just, it was a horrible mess.
[00:43:02:899 - 00:43:05:540] **Speaker 1:** But with the behavioural voltages and using some of the
[00:43:05:540 - 00:43:09:800] **Speaker 1:** commands that are in AltiSpiceC, you can extract the maximum
[00:43:09:800 - 00:43:11:419] **Speaker 1:** of all the potential differences.
[00:43:16:060 - 00:43:18:820] **Speaker 1:** So that became a very, very straightforward way of doing
[00:43:18:820 - 00:43:19:120] **Speaker 1:** it.
[00:43:19:979 - 00:43:21:500] **Speaker 1:** And then then that.
[00:43:22:500 - 00:43:27:500] **Speaker 1:** Is your input Into the circuit here.
[00:43:28:939 - 00:43:31:100] **Speaker 1:** And that's what I do, it's just, it's a pretty
[00:43:31:100 - 00:43:32:399] **Speaker 1:** standard way of analysing that.
[00:43:35:330 - 00:43:38:290] **Speaker 1:** And now if we look at the comparisons, I don't
[00:43:38:290 - 00:43:40:209] **Speaker 1:** know, I can't even tell any difference between those two
[00:43:40:209 - 00:43:40:679] **Speaker 1:** waveforms.
[00:43:40:719 - 00:43:42:310] **Speaker 1:** In fact, they look identical to me.
[00:43:43:820 - 00:43:49:510] **Speaker 1:** That's the current Um, through, through this.
[00:43:50:129 - 00:43:53:669] **Speaker 1:** So if you take The current through this load here
[00:43:53:669 - 00:43:54:449] **Speaker 1:** with the full.
[00:43:55:840 - 00:43:57:629] **Speaker 1:** A 3-phase circuit.
[00:43:58:750 - 00:44:02:449] **Speaker 1:** And you plot that versus the simplified expression here.
[00:44:08:080 - 00:44:09:439] **Speaker 1:** Cause I don't know if you can see here that's
[00:44:09:439 - 00:44:13:379] **Speaker 1:** like, you like VRB VRG these are different, different voltages
[00:44:13:379 - 00:44:13:760] **Speaker 1:** that.
[00:44:15:040 - 00:44:21:179] **Speaker 1:** Um Yeah I think I'm just plotting those just to
[00:44:21:179 - 00:44:22:270] **Speaker 1:** have a look at them, um.
[00:44:23:810 - 00:44:26:429] **Speaker 1:** Just come to think about it, these aren't actually used.
[00:44:29:050 - 00:44:32:189] **Speaker 1:** And here, that's just a further analysis tool.
[00:44:33:629 - 00:44:37:770] **Speaker 1:** So that This is kind of like extra information.
[00:44:43:520 - 00:44:45:479] **Speaker 1:** I find that other thing good with Alti Spice, if
[00:44:45:479 - 00:44:48:120] **Speaker 1:** you wanna analyse some sort of part of the component,
[00:44:48:199 - 00:44:50:120] **Speaker 1:** what are the components actually doing that make up the
[00:44:50:120 - 00:44:53:459] **Speaker 1:** overall circuit, you can like just have a separate, Thing
[00:44:53:459 - 00:44:55:699] **Speaker 1:** in Lti Spice and you can like plot certain parts
[00:44:55:699 - 00:44:55:899] **Speaker 1:** of it.
[00:44:55:959 - 00:45:00:679] **Speaker 1:** This is It's just extra information not used.
[00:45:01:850 - 00:45:03:149] **Speaker 1:** In the main circuit.
[00:45:09:750 - 00:45:11:939] **Speaker 1:** Probably could just probably even deleted that for the um
[00:45:11:939 - 00:45:13:550] **Speaker 1:** I probably don't need this now because I think I
[00:45:13:550 - 00:45:15:330] **Speaker 1:** was using it for some other purpose and I don't
[00:45:15:330 - 00:45:16:129] **Speaker 1:** even need it now.
[00:45:17:770 - 00:45:19:010] **Speaker 1:** It would actually just be that.
[00:45:19:250 - 00:45:20:590] **Speaker 1:** It's such a simple circuit, right?
[00:45:20:729 - 00:45:22:290] **Speaker 1:** Just 2 inductors, 1 diode.
[00:45:23:340 - 00:45:29:070] **Speaker 1:** And Oh no, no, I suppose you do need the.
[00:45:35:409 - 00:45:36:120] **Speaker 1:** Yeah.
[00:45:40:540 - 00:45:41:560] **Speaker 1:** Uh, sorry about that.
[00:45:41:830 - 00:45:43:550] **Speaker 1:** So it's extra information.
[00:45:44:270 - 00:45:46:060] **Speaker 1:** Um, input.
[00:45:50:449 - 00:45:52:179] **Speaker 1:** And I say.
[00:45:56:409 - 00:45:59:080] **Speaker 1:** The behavioural voltage.
[00:46:00:010 - 00:46:01:129] **Speaker 1:** Of the main circuit.
[00:46:02:840 - 00:46:04:719] **Speaker 1:** I've separated them out, no, they are needed.
[00:46:07:379 - 00:46:10:459] **Speaker 1:** Yeah, it just allows me to just get each individual
[00:46:10:459 - 00:46:12:379] **Speaker 1:** source contribution and take the maximum of them all.
[00:46:12:820 - 00:46:16:540] **Speaker 1:** Anyway, the point about this slide is that, They're basically
[00:46:16:540 - 00:46:18:540] **Speaker 1:** the same, you're getting a tiny little bit of error
[00:46:18:540 - 00:46:20:280] **Speaker 1:** here but very minimal.
[00:46:21:679 - 00:46:24:800] **Speaker 1:** So that was a nice way of analysing what's going
[00:46:24:800 - 00:46:25:219] **Speaker 1:** on.
[00:46:27:169 - 00:46:28:409] **Speaker 1:** He's got one slide left.
[00:46:32:010 - 00:46:35:989] **Speaker 1:** So Just gonna spend a bit of time on the
[00:46:35:989 - 00:46:36:570] **Speaker 1:** slide.
[00:46:40:010 - 00:46:42:530] **Speaker 1:** Constant Parison, the constant voters load with the RC load.
[00:46:45:000 - 00:46:47:280] **Speaker 1:** So now I have, uh, it's not the greatest of
[00:46:47:280 - 00:46:48:899] **Speaker 1:** resolution, but you can sort of see.
[00:46:50:120 - 00:46:51:260] **Speaker 1:** And I try.
[00:46:55:199 - 00:46:55:860] **Speaker 1:** Again.
[00:46:58:760 - 00:47:01:919] **Speaker 1:** I've got my classic one milliferrode capacitor.
[00:47:04:050 - 00:47:05:870] **Speaker 1:** And uh we've got.
[00:47:07:560 - 00:47:11:129] **Speaker 1:** Yeah, I got some resistance here, about 90 something games
[00:47:11:129 - 00:47:12:159] **Speaker 1:** or something, um.
[00:47:20:040 - 00:47:20:439] **Speaker 1:** Yeah.
[00:47:20:800 - 00:47:22:520] **Speaker 1:** So, but and then what I'm doing is I'm actually
[00:47:22:520 - 00:47:25:199] **Speaker 1:** combining these into like a constant voltage here.
[00:47:26:500 - 00:47:31:340] **Speaker 1:** This Is used.
[00:47:32:560 - 00:47:33:739] **Speaker 1:** To measure current.
[00:47:39:080 - 00:47:41:530] **Speaker 1:** And I've used 18 to -4 ohms.
[00:47:42:290 - 00:47:44:040] **Speaker 1:** That's a good trick if you wanna cuz it's.
[00:47:46:129 - 00:47:48:760] **Speaker 1:** Yeah, you wanna, you don't wanna measure the current just
[00:47:48:760 - 00:47:51:219] **Speaker 1:** through one diode you wanna measure like what's the contribution
[00:47:51:219 - 00:47:52:830] **Speaker 1:** of them all, so then you can just put the
[00:47:52:830 - 00:47:54:540] **Speaker 1:** little resistor here and then you can see what's going
[00:47:54:540 - 00:47:55:120] **Speaker 1:** into here.
[00:47:58:340 - 00:48:02:379] **Speaker 1:** And I've matched this voltage to this RC load.
[00:48:05:820 - 00:48:07:360] **Speaker 1:** Like how I did it was I.
[00:48:08:070 - 00:48:10:000] **Speaker 1:** So I think this is, yeah, this is 96, so
[00:48:10:000 - 00:48:10:739] **Speaker 1:** it's um.
[00:48:17:469 - 00:48:19:429] **Speaker 1:** I think I may have actually started with this circuit
[00:48:19:429 - 00:48:20:639] **Speaker 1:** and then I think I.
[00:48:21:459 - 00:48:42:169] **Speaker 1:** Match this But either way, model.
[00:48:43:629 - 00:48:45:290] **Speaker 1:** This is the minimal model, by the way.
[00:48:49:580 - 00:48:52:780] **Speaker 1:** A minimum model is kind of like the minimalistic model
[00:48:52:780 - 00:48:54:280] **Speaker 1:** that catches all the key behaviour.
[00:48:56:070 - 00:48:57:639] **Speaker 1:** That's my definition of a male model model.
[00:48:59:120 - 00:49:00:879] **Speaker 1:** And so by having a constant voltage.
[00:49:02:860 - 00:49:06:489] **Speaker 1:** You're capturing like all the highly complicated dynamics of an
[00:49:06:489 - 00:49:11:040] **Speaker 1:** RC circuit, which could be really difficult to analyse analytically,
[00:49:11:500 - 00:49:13:199] **Speaker 1:** but you can analyse this nice.
[00:49:13:340 - 00:49:15:419] **Speaker 1:** You can analyse this analytically because it's like a constant
[00:49:15:419 - 00:49:15:939] **Speaker 1:** voltage load.
[00:49:17:300 - 00:49:18:129] **Speaker 1:** And here it's horrible.
[00:49:19:050 - 00:49:22:729] **Speaker 1:** And my point here is that these are the same.
[00:49:23:530 - 00:49:25:610] **Speaker 1:** Essentially the same.
[00:49:27:050 - 00:49:29:689] **Speaker 1:** And you can see the current waveforms are very, very
[00:49:29:689 - 00:49:29:889] **Speaker 1:** close.
[00:49:29:969 - 00:49:31:959] **Speaker 1:** There's a little bit of an error there but not
[00:49:31:959 - 00:49:32:389] **Speaker 1:** much.
[00:49:33:439 - 00:49:35:000] **Speaker 1:** But what I've done is chosen this.
[00:49:35:080 - 00:49:37:679] **Speaker 1:** I could have made it 100 homes or 92 ohms.
[00:49:37:800 - 00:49:39:120] **Speaker 1:** It wouldn't make too much difference.
[00:49:39:439 - 00:49:42:000] **Speaker 1:** The fact is I chose it to exactly match the
[00:49:42:000 - 00:49:44:840] **Speaker 1:** current RMS and my my point here is to show
[00:49:44:840 - 00:49:45:120] **Speaker 1:** that.
[00:49:46:300 - 00:49:50:040] **Speaker 1:** This idea of having constant current and constant voltage load.
[00:49:50:729 - 00:49:55:050] **Speaker 1:** Is a really useful and accurate way of modelling real,
[00:49:55:149 - 00:49:58:409] **Speaker 1:** the real world circuits that, but you know we need
[00:49:58:409 - 00:50:00:689] **Speaker 1:** a reasonably big capacitor, but in many cases it works
[00:50:00:689 - 00:50:01:350] **Speaker 1:** really, really well.
[00:50:02:389 - 00:50:04:139] **Speaker 1:** And a little bit off in the voltage.
[00:50:04:590 - 00:50:05:850] **Speaker 1:** But pretty, pretty close.
[00:50:06:919 - 00:50:07:989] **Speaker 1:** So let's just say.
[00:50:09:909 - 00:50:11:100] **Speaker 1:** Virtually identical.
[00:50:12:610 - 00:50:13:290] **Speaker 1:** my mum model.
[00:50:15:239 - 00:50:17:679] **Speaker 1:** It's very close on the current, in fact the RMSs
[00:50:17:679 - 00:50:19:439] **Speaker 1:** are identical cos that's how I designed it.
[00:50:19:840 - 00:50:21:459] **Speaker 1:** But even the waveforms are very close.
[00:50:23:520 - 00:50:26:820] **Speaker 1:** And this is virtually identical.
[00:50:33:729 - 00:50:36:030] **Speaker 1:** And so the main voltage.
[00:50:41:679 - 00:50:44:209] **Speaker 1:** Across the resistor, if you want to work this out.
[00:50:48:260 - 00:50:51:929] **Speaker 1:** Register is 541.9.
[00:50:52:979 - 00:50:53:649] **Speaker 1:** Votes.
[00:50:55:159 - 00:50:59:959] **Speaker 1:** And you compare with 540 votes.
[00:51:01:929 - 00:51:03:639] **Speaker 1:** So a 0.35% error.
[00:51:08:879 - 00:51:12:729] **Speaker 1:** So yeah, just Probably summary here and I'll call it
[00:51:12:729 - 00:51:13:300] **Speaker 1:** a day.
[00:51:13:879 - 00:51:15:100] **Speaker 1:** Constant voltage.
[00:51:18:600 - 00:51:25:010] **Speaker 1:** Load Is a good approximation.
[00:51:27:090 - 00:51:30:439] **Speaker 1:** To And RC load.
[00:51:32:330 - 00:51:34:060] **Speaker 1:** For a sufficiently high capacitor.
[00:51:34:790 - 00:51:36:899] **Speaker 1:** So if you've got a reasonably big capacitor cause you
[00:51:36:899 - 00:51:39:939] **Speaker 1:** wanna have good small amount of ripple, which you wouldn't
[00:51:39:939 - 00:51:41:090] **Speaker 1:** often in the real world.
[00:51:42:270 - 00:51:43:649] **Speaker 1:** Then you can mathematically.
[00:51:46:330 - 00:51:47:429] **Speaker 1:** Use a much simpler model.
[00:51:48:520 - 00:51:49:639] **Speaker 1:** With the constant voltage.
[00:51:50:310 - 00:51:52:179] **Speaker 1:** Yeah, so these last two slides.
[00:51:55:570 - 00:51:58:580] **Speaker 1:** You just sort of need to know that it works
[00:51:58:580 - 00:51:58:889] **Speaker 1:** more.
[00:51:59:050 - 00:52:00:449] **Speaker 1:** Like I'm not gonna ask you to do this in
[00:52:00:449 - 00:52:02:090] **Speaker 1:** an exam, obviously like you won't have to.
[00:52:03:189 - 00:52:04:100] **Speaker 1:** Do all this calculation.
[00:52:04:149 - 00:52:06:310] **Speaker 1:** It's just like giving you an intuition and a feel
[00:52:06:310 - 00:52:08:750] **Speaker 1:** so that you can know that constant current and a
[00:52:08:750 - 00:52:12:070] **Speaker 1:** constant voltage do work in the real world.
[00:52:12:310 - 00:52:14:429] **Speaker 1:** That's that's my main point for today.
[00:52:15:419 - 00:52:16:189] **Speaker 1:** I'll leave it there.
[00:52:16:610 - 00:52:18:629] **Speaker 1:** Hopefully I've made that point well, we'll see.
[00:52:19:350 - 00:52:19:800] **Speaker 1:** Thank you.
[00:52:20:620 - 00:52:21:100] **Speaker 1:** That's all.
[00:52:23:580 - 00:52:27:739] **Speaker 1:** Yep, yep, just see I get my last little piece
[00:52:27:739 - 00:52:28:439] **Speaker 1:** of wisdom there.
[00:52:31:379 - 00:52:32:500] **Speaker 1:** How about I put a box around it?
[00:52:42:000 - 00:52:43:949] **Speaker 1:** I tried to ease you into three-phase.
[00:52:44:000 - 00:52:46:520] **Speaker 1:** I don't want to terrify you immediately with really complex
[00:52:46:520 - 00:52:47:040] **Speaker 1:** maths.
[00:52:58:330 - 00:52:58:370] **Speaker 0:** That's right.
[00:53:04:469 - 00:53:04:479] **Speaker 0:** Yeah.
[00:53:07:290 - 00:53:07:300] **Speaker 1:** OK.
[00:53:07:969 - 00:53:08:280] **Speaker 1:** OK.
[00:53:08:489 - 00:53:08:770] **Speaker 0:** See you.
[00:53:12:110 - 00:53:12:120] **Speaker 0:** OK.
[00:53:13:610 - 00:53:13:860] **Speaker 0:** In here.
[00:53:24:570 - 00:53:25:340] **Speaker 0:** Hi, can I see you.
[00:53:26:969 - 00:53:27:449] **Speaker 0:** See you.
[00:53:30:979 - 00:53:30:989] **Speaker 0:** That.
[00:53:36:399 - 00:53:37:330] **Speaker 0:** That's a good sign.
[00:53:39:070 - 00:53:41:229] **Speaker 0:** Do you like that NASA shirt?
[00:53:41:709 - 00:53:43:590] **Speaker 1:** I'm gonna, I'm gonna put it for, I'm gonna, I'm
[00:53:43:590 - 00:53:45:709] **Speaker 1:** gonna put these two for the NL 300 visualise your
[00:53:45:709 - 00:53:46:469] **Speaker 1:** project competition.
[00:53:46:909 - 00:53:47:760] **Speaker 1:** I want to try and get people.
[00:53:47:820 - 00:53:49:659] **Speaker 1:** I'm gonna write on the, on the learn that there's
[00:53:49:659 - 00:53:50:290] **Speaker 1:** NASA t-shirts.
[00:53:50:750 - 00:53:52:770] **Speaker 1:** Then who, who wouldn't want to enter the competition?
[00:53:53:229 - 00:53:53:889] **Speaker 1:** Hopefully.
[00:53:54:590 - 00:53:56:149] **Speaker 1:** Damn it, it hasn't worked.
[00:53:57:879 - 00:53:58:669] **Speaker 1:** I need another one.
[00:53:59:600 - 00:54:00:540] **Speaker 1:** It's only one minute.
[00:54:01:370 - 00:54:01:850] **Speaker 1:** Oh yeah, hi.
[00:54:02:110 - 00:54:03:560] **Speaker 1:** Do you know, do we get a cheat sheet for
[00:54:03:560 - 00:54:03:729] **Speaker 0:** the exam?
[00:54:05:449 - 00:54:11:250] **Speaker 1:** Um, I, I should know because I make the exam,
[00:54:11:979 - 00:54:13:629] **Speaker 1:** um, and it's actually due soon started.
[00:54:15:689 - 00:54:17:070] **Speaker 1:** I normally.
[00:54:18:350 - 00:54:21:669] **Speaker 1:** Put everything you need to know in a um in
[00:54:21:669 - 00:54:24:110] **Speaker 1:** like a sheet so the cheat sheet is already in
[00:54:24:110 - 00:54:27:590] **Speaker 1:** the exam like a formula yeah yeah yeah like yeah
[00:54:27:590 - 00:54:29:590] **Speaker 1:** so you don't make your own like it's not a
[00:54:29:590 - 00:54:32:229] **Speaker 1:** sheet you no you can't bring it oh thanks a
[00:54:32:229 - 00:54:34:669] **Speaker 1:** lot that's that was pretty valuable anyway.
[00:54:35:530 - 00:54:37:439] **Speaker 1:** Uh, yeah, so you can't actually bring a sheet in
[00:54:37:439 - 00:54:38:540] **Speaker 1:** there, because you don't need to.
[00:54:38:620 - 00:54:43:209] **Speaker 1:** It'd be fine, fine, yeah, yeah, and if you want
[00:54:43:209 - 00:54:46:379] **Speaker 1:** to, if it's not like I'll tell you what the
[00:54:46:379 - 00:54:49:050] **Speaker 1:** sheet is before we exam, right, and then give me
[00:54:49:050 - 00:54:50:379] **Speaker 1:** some feedback if you want some more and it just
[00:54:50:379 - 00:54:50:959] **Speaker 1:** tell me.
[00:54:52:649 - 00:54:53:530] **Speaker 0:** Yeah.

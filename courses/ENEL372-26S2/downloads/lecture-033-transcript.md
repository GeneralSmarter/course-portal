# ENEL372-26S2 Lecture 33 native Echo transcript

Date: October 9, 2026 9:00am-9:55am
Transcript type: native Echo automated transcript.

[00:01:53:580 - 00:01:54:059] **Speaker 0:** That's fine.
[00:02:47:789 - 00:02:47:860] **Speaker 0:** yeah.
[00:02:51:679 - 00:02:51:710] **Speaker 0:** I.
[00:02:52:779 - 00:02:53:000] **Speaker 1:** Becky.
[00:02:57:570 - 00:02:58:179] **Speaker 1:** Please work.
[00:03:02:949 - 00:03:07:509] **Speaker 1:** Uh Supposedly it's fixed.
[00:03:12:970 - 00:03:13:600] **Speaker 1:** Yes.
[00:03:40:979 - 00:03:46:059] **Speaker 1:** So, start where I was going to, um, Tuesday we
[00:03:46:059 - 00:03:48:740] **Speaker 1:** had a network flow network failure.
[00:03:59:990 - 00:04:02:490] **Speaker 1:** So, um, inverting configuration.
[00:04:04:199 - 00:04:05:369] **Speaker 1:** Let's go through this.
[00:04:10:889 - 00:04:18:940] **Speaker 1:** So we have Current noise.
[00:04:21:549 - 00:04:22:480] **Speaker 1:** Cross resistor.
[00:04:30:109 - 00:04:51:040] **Speaker 1:** Any resistor would be Johnson Voters noise Squid So that's
[00:04:51:040 - 00:04:52:540] **Speaker 1:** just vehicles IR.
[00:04:57:220 - 00:04:59:480] **Speaker 1:** Still behaves even though it's a noise.
[00:05:00:019 - 00:05:01:820] **Speaker 1:** It's still an actual voltage, right?
[00:05:02:140 - 00:05:03:279] **Speaker 1:** It's just noise.
[00:05:03:859 - 00:05:04:179] **Speaker 1:** So.
[00:05:05:390 - 00:05:06:570] **Speaker 1:** Stall vehicles IR.
[00:05:09:640 - 00:05:11:779] **Speaker 1:** So you'd, you'd get an induced current from the jet
[00:05:11:779 - 00:05:13:119] **Speaker 1:** voltage noise across the resistor.
[00:05:13:309 - 00:05:13:910] **Speaker 1:** That's what I'm saying.
[00:05:25:190 - 00:05:27:470] **Speaker 1:** So then you get that because you know the, the
[00:05:27:470 - 00:05:30:179] **Speaker 1:** square root of that's obviously, you know, Johnson always is
[00:05:30:179 - 00:05:31:540] **Speaker 1:** the square root of that, but then the squareot is
[00:05:31:540 - 00:05:32:029] **Speaker 1:** obviously that.
[00:05:33:040 - 00:05:34:119] **Speaker 1:** And then the arts council.
[00:05:37:059 - 00:05:42:940] **Speaker 1:** And you end up with That for the square.
[00:05:45:510 - 00:05:47:309] **Speaker 1:** See, that's why there's no R squad here because the
[00:05:47:309 - 00:05:47:829] **Speaker 1:** council's out.
[00:05:52:119 - 00:05:55:179] **Speaker 1:** So we've got our I amp noise, current noise.
[00:06:02:440 - 00:06:05:140] **Speaker 1:** That is from the semiconductor, so it is shock noise.
[00:06:11:200 - 00:06:12:519] **Speaker 1:** Shot noise for the L amp.
[00:06:14:299 - 00:06:16:440] **Speaker 1:** And the resistors are the are the Johnson noise.
[00:06:17:309 - 00:06:18:470] **Speaker 1:** And you add them all together.
[00:06:20:170 - 00:06:22:549] **Speaker 1:** And it's all going into the input.
[00:06:23:700 - 00:06:25:220] **Speaker 1:** Cause every one of these.
[00:06:26:279 - 00:06:28:679] **Speaker 1:** But these are added together because they're both contributing into
[00:06:28:679 - 00:06:30:839] **Speaker 1:** the input plus it's plus the input from the current
[00:06:30:839 - 00:06:31:309] **Speaker 1:** noise.
[00:06:31:880 - 00:06:33:140] **Speaker 1:** So you just add them all together.
[00:06:35:890 - 00:06:37:480] **Speaker 1:** Then you can work out the effect of.
[00:06:38:950 - 00:06:40:190] **Speaker 1:** Total voters noise.
[00:06:43:369 - 00:06:47:790] **Speaker 1:** And that's gonna be the Johnson noise plus.
[00:06:50:279 - 00:06:54:320] **Speaker 1:** R12 times the current, which is that.
[00:06:57:010 - 00:06:57:809] **Speaker 1:** That's like.
[00:06:59:380 - 00:07:07:869] **Speaker 1:** I A 2 Just a little note here.
[00:07:10:709 - 00:07:12:049] **Speaker 1:** What I'm doing there.
[00:07:15:529 - 00:07:17:029] **Speaker 1:** Is is the sum.
[00:07:18:959 - 00:07:24:470] **Speaker 1:** Of squeeze You never just work out what the current
[00:07:24:470 - 00:07:24:630] **Speaker 1:** is.
[00:07:24:670 - 00:07:27:630] **Speaker 1:** You always look at the sum of the squares and
[00:07:27:630 - 00:07:28:269] **Speaker 1:** add all those up.
[00:07:28:390 - 00:07:30:730] **Speaker 1:** That's the way that statistics works.
[00:07:31:500 - 00:07:33:600] **Speaker 1:** Experiences, you sum always sum of the squares.
[00:07:35:049 - 00:07:40:600] **Speaker 1:** And that Just works We don't know much about stats,
[00:07:40:649 - 00:07:42:730] **Speaker 1:** but, you know, that's what the statisticians say.
[00:07:44:510 - 00:07:46:010] **Speaker 1:** I did a little bit of stats, but um.
[00:07:47:399 - 00:07:48:980] **Speaker 1:** I know you get a lot of variances.
[00:07:49:640 - 00:07:52:519] **Speaker 1:** I think even the definition of standard deviation, if you
[00:07:52:519 - 00:07:54:880] **Speaker 1:** remember, is like some, sum of squares.
[00:07:55:589 - 00:07:56:980] **Speaker 1:** But at the end you're like square root.
[00:07:59:029 - 00:08:00:750] **Speaker 1:** It's just a law of averages, I suppose.
[00:08:01:049 - 00:08:02:589] **Speaker 1:** Everything works on the summer of squares.
[00:08:06:200 - 00:08:08:910] **Speaker 1:** All right So always remember that.
[00:08:11:579 - 00:08:13:519] **Speaker 1:** And then what we end up with here.
[00:08:14:700 - 00:08:16:170] **Speaker 1:** Is the voters noise.
[00:08:17:220 - 00:08:20:040] **Speaker 1:** That comes from inside the op amp.
[00:08:22:239 - 00:08:26:910] **Speaker 1:** Plus The voters' noise.
[00:08:29:839 - 00:08:38:330] **Speaker 1:** Induced From that resistor R1, from the um inverting configuration,
[00:08:38:559 - 00:08:39:570] **Speaker 1:** which is an amplifier.
[00:08:40:460 - 00:08:42:450] **Speaker 1:** And choose the R2 and the R1 to get a
[00:08:42:450 - 00:08:44:520] **Speaker 1:** certain amplification like just any normal.
[00:08:45:250 - 00:08:47:150] **Speaker 1:** And before you should be familiar with.
[00:08:48:539 - 00:08:48:979] **Speaker 1:** All right.
[00:08:50:369 - 00:08:57:630] **Speaker 1:** Jews from I1 With Current IA.
[00:08:59:719 - 00:09:01:700] **Speaker 1:** I'll just assume you know about op amps.
[00:09:09:789 - 00:09:11:450] **Speaker 1:** But you may not know about opent noise.
[00:09:17:619 - 00:09:20:030] **Speaker 1:** That's what I'm, my goal is to teach you.
[00:09:21:140 - 00:09:24:119] **Speaker 1:** And then you can choose the right amp, the right
[00:09:24:229 - 00:09:24:700] **Speaker 1:** op amp.
[00:09:27:380 - 00:09:28:599] **Speaker 1:** And the right depends on the application.
[00:09:30:169 - 00:09:31:349] **Speaker 1:** Depends on what you wanna do.
[00:09:32:859 - 00:09:35:479] **Speaker 1:** So here's a few, kind of put them in a.
[00:09:37:570 - 00:09:38:469] **Speaker 1:** Couple of graphs here.
[00:09:43:780 - 00:09:46:109] **Speaker 1:** And so I'm plotting it versus, because you get changes
[00:09:46:109 - 00:09:47:530] **Speaker 1:** versus frequency, of course.
[00:09:48:799 - 00:09:50:909] **Speaker 1:** Frequency can affect the noise.
[00:09:53:289 - 00:09:55:969] **Speaker 1:** And here's just a few common ones.
[00:09:59:419 - 00:10:06:020] **Speaker 1:** So we have Kind of relatively high Johnson noise for
[00:10:06:020 - 00:10:07:520] **Speaker 1:** the LT 1013.
[00:10:09:099 - 00:10:13:979] **Speaker 1:** Relatively high current noise but not too high, around about
[00:10:13:979 - 00:10:14:820] **Speaker 1:** the same level.
[00:10:19:609 - 00:10:21:650] **Speaker 1:** Not the most amazing op amp in the world, but
[00:10:21:650 - 00:10:23:390] **Speaker 1:** it's reasonable.
[00:10:26:200 - 00:10:27:739] **Speaker 1:** So let's just circle those.
[00:10:28:630 - 00:10:29:400] **Speaker 1:** I looked that up.
[00:10:30:739 - 00:10:33:549] **Speaker 1:** It's around about $3 US dollars.
[00:10:36:219 - 00:10:37:739] **Speaker 1:** May have gone up a little bit, but um.
[00:10:38:830 - 00:10:43:229] **Speaker 1:** Well it may have gone down even uh electronic components
[00:10:43:229 - 00:10:44:109] **Speaker 1:** tend to go down.
[00:10:49:250 - 00:10:50:059] **Speaker 1:** What else have we got?
[00:10:50:340 - 00:10:52:159] **Speaker 1:** Very low current noise for this one.
[00:10:53:650 - 00:10:57:020] **Speaker 1:** But it has a higher voltage noise, kind of a
[00:10:57:020 - 00:10:57:479] **Speaker 1:** trade-off.
[00:11:01:150 - 00:11:05:159] **Speaker 1:** So that's Circle those two.
[00:11:06:539 - 00:11:07:929] **Speaker 1:** The AD 549.
[00:11:09:390 - 00:11:11:770] **Speaker 1:** I'll make a little note here, it's very low.
[00:11:13:190 - 00:11:14:140] **Speaker 1:** Current noise.
[00:11:19:109 - 00:11:22:239] **Speaker 1:** But his high.
[00:11:23:330 - 00:11:24:859] **Speaker 1:** Voltage noise, so that's the trade-off.
[00:11:26:450 - 00:11:28:969] **Speaker 1:** It all depends on your application, whether you can tolerate,
[00:11:29:090 - 00:11:31:109] **Speaker 1:** maybe you can tolerate a higher voltage noise.
[00:11:34:349 - 00:11:36:229] **Speaker 1:** Cause, um, you may, I think that happens when you
[00:11:36:229 - 00:11:38:489] **Speaker 1:** have a, a really large.
[00:11:39:580 - 00:11:40:640] **Speaker 1:** Source resistance.
[00:11:41:890 - 00:11:43:969] **Speaker 1:** Then you don't want there to be a whole lot
[00:11:43:969 - 00:11:44:909] **Speaker 1:** of current noise.
[00:11:48:090 - 00:11:48:940] **Speaker 1:** Discuss that later.
[00:11:50:119 - 00:11:56:719] **Speaker 1:** Arch Let's look at This one's pretty good.
[00:11:59:770 - 00:12:01:309] **Speaker 1:** Pretty good voters noise.
[00:12:02:390 - 00:12:03:969] **Speaker 1:** And a very low current noise.
[00:12:06:900 - 00:12:08:859] **Speaker 1:** So the OPA 111.
[00:12:11:739 - 00:12:12:679] **Speaker 1:** Is good at both.
[00:12:16:460 - 00:12:21:700] **Speaker 1:** And what it is is a special For your input.
[00:12:25:530 - 00:12:26:770] **Speaker 1:** And it's in medical equipment.
[00:12:26:849 - 00:12:28:320] **Speaker 1:** You'd expect medical equipment.
[00:12:29:309 - 00:12:31:239] **Speaker 1:** Has to be precise, you don't wanna have too much
[00:12:31:239 - 00:12:32:859] **Speaker 1:** noise at all.
[00:12:35:179 - 00:12:37:270] **Speaker 1:** And of course, obviously you pay for that.
[00:12:37:549 - 00:12:39:849] **Speaker 1:** That's why things in the medical field cost so much.
[00:12:40:809 - 00:12:43:320] **Speaker 1:** The components are even more like expensive.
[00:12:44:690 - 00:12:49:200] **Speaker 1:** And that's like 10 times the price of these other
[00:12:49:200 - 00:12:49:669] **Speaker 1:** ones.
[00:12:51:650 - 00:12:53:630] **Speaker 1:** $45 US dollars for that one.
[00:13:01:299 - 00:13:02:659] **Speaker 1:** Just a few examples.
[00:13:08:929 - 00:13:11:789] **Speaker 1:** The got the note on that one, this one.
[00:13:13:390 - 00:13:14:570] **Speaker 1:** It's a little bit more expensive.
[00:13:15:909 - 00:13:27:049] **Speaker 1:** Very But then it's Pretty flat across the whole frequency
[00:13:27:049 - 00:13:28:309] **Speaker 1:** range, just looking at it.
[00:13:34:530 - 00:13:35:299] **Speaker 1:** What did I say?
[00:13:36:770 - 00:13:38:679] **Speaker 1:** I don't think I wrote a price for the.
[00:13:40:539 - 00:13:43:010] **Speaker 1:** Probably around about $10 US dollars for that one there.
[00:13:47:020 - 00:13:47:369] **Speaker 1:** You were.
[00:13:49:780 - 00:13:51:010] **Speaker 1:** It's just a bit of a comparison.
[00:13:52:940 - 00:13:57:320] **Speaker 1:** So roughly speaking, The more they both are low, the
[00:13:57:320 - 00:13:59:200] **Speaker 1:** greater the price, but not necessarily.
[00:14:00:130 - 00:14:02:770] **Speaker 1:** I think there may be a factor in how flat.
[00:14:03:969 - 00:14:06:239] **Speaker 1:** It is peer frequency as well.
[00:14:09:450 - 00:14:10:909] **Speaker 1:** But even that doesn't always work.
[00:14:13:239 - 00:14:15:320] **Speaker 1:** But anyway, let's move on.
[00:14:18:619 - 00:14:19:770] **Speaker 1:** A point noise figure.
[00:14:20:700 - 00:14:22:400] **Speaker 1:** This is one of my favourite exam questions.
[00:14:28:119 - 00:14:31:159] **Speaker 1:** Using expressions for INE, the noise figure is given by
[00:14:31:159 - 00:14:31:599] **Speaker 1:** this.
[00:14:33:669 - 00:14:39:119] **Speaker 1:** And here's an example of the L21028 non-inverting configuration.
[00:14:43:580 - 00:14:46:400] **Speaker 1:** And this, they're both of these.
[00:14:48:210 - 00:14:51:669] **Speaker 1:** You can look up the specs for the L21028.
[00:14:56:729 - 00:14:58:169] **Speaker 1:** And that will be what you get.
[00:14:58:940 - 00:15:01:780] **Speaker 1:** But at the frequency that you're operating at, because I
[00:15:01:780 - 00:15:03:619] **Speaker 1:** said the noise we were at 10 kilohertz and 20
[00:15:03:619 - 00:15:04:419] **Speaker 1:** degrees, that's the question.
[00:15:05:650 - 00:15:07:109] **Speaker 1:** 20 °C.
[00:15:17:900 - 00:15:18:840] **Speaker 1:** So joint.
[00:15:24:039 - 00:15:27:719] **Speaker 1:** Yeah, see it's way up here, 1028, about 1 times
[00:15:27:719 - 00:15:28:780] **Speaker 1:** 10 to 12.
[00:15:30:099 - 00:15:32:599] **Speaker 1:** Pico amps, Pico is 10 to -12.
[00:15:33:789 - 00:15:35:330] **Speaker 1:** It's relatively high current noise.
[00:15:38:099 - 00:15:38:950] **Speaker 1:** When I join.
[00:15:41:809 - 00:15:42:940] **Speaker 1:** Round about one.
[00:15:44:890 - 00:15:47:070] **Speaker 1:** Nano vault, so you saw that in the graph.
[00:15:47:849 - 00:15:49:440] **Speaker 1:** But you can look up the specs in the sheet
[00:15:49:440 - 00:15:49:950] **Speaker 1:** as well.
[00:15:50:609 - 00:15:52:229] **Speaker 1:** Work out the parallel resistance.
[00:15:55:099 - 00:16:01:130] **Speaker 1:** That goes into here Plug the numbers in.
[00:16:01:369 - 00:16:03:270] **Speaker 1:** 4 kT is that.
[00:16:03:909 - 00:16:08:090] **Speaker 1:** You got the magical number here, 1.38 times 10-23 times
[00:16:08:090 - 00:16:08:789] **Speaker 1:** by 4.
[00:16:11:760 - 00:16:13:669] **Speaker 1:** Cause the 4 kT is given by that whole thing,
[00:16:13:719 - 00:16:15:940] **Speaker 1:** you're gonna add 20 degrees.
[00:16:16:320 - 00:16:20:330] **Speaker 1:** In the exam I just normally say assume 4 kT
[00:16:20:330 - 00:16:20:679] **Speaker 1:** is.
[00:16:21:890 - 00:16:25:090] **Speaker 1:** Something, uh, which means it's basically the room temperature.
[00:16:30:989 - 00:16:34:729] **Speaker 1:** Plug them in So yeah, I've just done that for
[00:16:34:729 - 00:16:35:070] **Speaker 1:** you.
[00:16:36:669 - 00:16:39:510] **Speaker 1:** Because my main point here is just looking at the
[00:16:39:510 - 00:16:41:109] **Speaker 1:** relative contributions of each term.
[00:16:42:299 - 00:16:43:400] **Speaker 1:** I want you to see that.
[00:16:45:099 - 00:16:46:950] **Speaker 1:** You can see there's some voltage noise, and when you
[00:16:46:950 - 00:16:48:090] **Speaker 1:** square it's like.
[00:16:48:909 - 00:16:50:859] **Speaker 1:** 10 to -8 term here.
[00:16:52:369 - 00:16:56:169] **Speaker 1:** And the current noise is not, I think it's probably
[00:16:56:169 - 00:17:02:590] **Speaker 1:** related to the fact that This, uh Or the RS
[00:17:02:590 - 00:17:05:250] **Speaker 1:** is not massive like it's not like in the mega
[00:17:05:250 - 00:17:07:550] **Speaker 1:** mega ohms, it's like only kilohms.
[00:17:08:010 - 00:17:10:109] **Speaker 1:** So your source resistance is quite small.
[00:17:11:060 - 00:17:13:219] **Speaker 1:** And that turn there, because you've got a small source
[00:17:13:219 - 00:17:16:938] **Speaker 1:** resistance and you're timing by a relatively large current noise,
[00:17:16:979 - 00:17:18:180] **Speaker 1:** but not too bad.
[00:17:19:250 - 00:17:22:900] **Speaker 1:** Then it's like really, really small contribution here.
[00:17:27:139 - 00:17:29:458] **Speaker 1:** And so if you don't just ignore that and that
[00:17:29:458 - 00:17:30:139] **Speaker 1:** for now.
[00:17:33:680 - 00:17:36:989] **Speaker 1:** What, what, what is dominating the noise in that circuit?
[00:17:37:079 - 00:17:37:729] **Speaker 1:** So I I wanna.
[00:17:38:819 - 00:17:39:290] **Speaker 1:** Tell me.
[00:17:40:349 - 00:17:41:949] **Speaker 1:** What's the dominating factor?
[00:17:42:150 - 00:17:44:329] **Speaker 1:** What's the dominating contribution to noise?
[00:17:46:609 - 00:17:48:010] **Speaker 1:** In the circuit, anyone?
[00:17:51:670 - 00:17:53:640] **Speaker 1:** Well, it's not the current noise from the op amp
[00:17:53:640 - 00:17:55:060] **Speaker 1:** because it's 10 to 19.
[00:17:55:939 - 00:17:57:420] **Speaker 1:** So then what is this term?
[00:17:58:800 - 00:18:00:219] **Speaker 1:** What is contributing to this turn?
[00:18:02:229 - 00:18:03:609] **Speaker 1:** It's just too early in the morning.
[00:18:04:910 - 00:18:06:709] **Speaker 1:** Yeah, Johnson always are the resistors.
[00:18:07:479 - 00:18:08:920] **Speaker 1:** Is compute is this.
[00:18:11:729 - 00:18:13:060] **Speaker 1:** So if I circle that.
[00:18:17:640 - 00:18:19:540] **Speaker 1:** You can see that the noise.
[00:18:23:979 - 00:18:29:300] **Speaker 1:** Is dominated by The feedback resistors.
[00:18:32:020 - 00:18:35:290] **Speaker 1:** Which is actually a good thing cause you can't really
[00:18:36:020 - 00:18:36:589] **Speaker 1:** control that.
[00:18:36:829 - 00:18:39:709] **Speaker 1:** You could control your choice of up amp for this
[00:18:39:709 - 00:18:39:910] **Speaker 1:** application.
[00:18:41:219 - 00:18:42:719] **Speaker 1:** But you can't really control.
[00:18:44:630 - 00:18:45:589] **Speaker 1:** The resistors.
[00:18:46:189 - 00:18:49:130] **Speaker 1:** Cause that's that's related to the amplifier that you're doing.
[00:18:50:770 - 00:18:52:229] **Speaker 1:** And that's kind of how you want to choose an
[00:18:52:229 - 00:18:52:770] **Speaker 1:** op amp.
[00:18:52:810 - 00:18:55:630] **Speaker 1:** So for this particular source resistance, this was a good
[00:18:56:050 - 00:18:56:329] **Speaker 1:** choice.
[00:18:56:439 - 00:19:01:010] **Speaker 1:** LT 1028 works well because it's not having a big
[00:19:01:010 - 00:19:03:329] **Speaker 1:** contribution on noise and it's reasonably cheap.
[00:19:04:760 - 00:19:06:880] **Speaker 1:** So that's a concept I want you to kind of
[00:19:06:880 - 00:19:07:199] **Speaker 1:** get.
[00:19:08:650 - 00:19:10:849] **Speaker 1:** Cause I'll be looking at that much in more detail
[00:19:10:849 - 00:19:11:229] **Speaker 1:** later.
[00:19:13:489 - 00:19:16:400] **Speaker 1:** And I'll just say, so for.
[00:19:18:189 - 00:19:18:910] **Speaker 1:** Given.
[00:19:20:420 - 00:19:30:180] **Speaker 1:** Ari The Uh LT LT 1028.
[00:19:31:300 - 00:19:33:880] **Speaker 1:** is a good choice.
[00:19:39:060 - 00:19:43:790] **Speaker 1:** Of of You wouldn't want to be choosing Opan that
[00:19:43:790 - 00:19:44:890] **Speaker 1:** dominated the noise.
[00:19:46:229 - 00:19:48:290] **Speaker 1:** Cos then you're getting way more noise than you should.
[00:19:53:069 - 00:19:57:880] **Speaker 1:** But if you change the source resistance, it's very likely
[00:19:57:880 - 00:19:59:400] **Speaker 1:** it's not going to be a good choice of OPAM.
[00:20:00:810 - 00:20:02:069] **Speaker 1:** And that's what you'll see here.
[00:20:03:130 - 00:20:05:339] **Speaker 1:** Of course, I mean here you can see after I've
[00:20:05:339 - 00:20:07:069] **Speaker 1:** worked that out, you can work out the noise figure.
[00:20:09:410 - 00:20:11:859] **Speaker 1:** And it's not too bad, 2.85 decibels.
[00:20:12:650 - 00:20:14:229] **Speaker 1:** When you plug this number into here.
[00:20:15:640 - 00:20:24:780] **Speaker 1:** Comes out to be that I've upped the source resistance
[00:20:24:780 - 00:20:28:260] **Speaker 1:** now, but I've choose the OPA 8549.
[00:20:33:250 - 00:20:35:550] **Speaker 1:** That has a much, much lower current noise.
[00:20:38:380 - 00:20:41:900] **Speaker 1:** And so that's pretty, that's pretty good when you have
[00:20:41:900 - 00:20:44:079] **Speaker 1:** a really high source resistance.
[00:20:46:079 - 00:20:48:500] **Speaker 1:** And I've made the source resistance one mega ohm.
[00:20:51:359 - 00:20:54:030] **Speaker 1:** And you can just look into the specs, plug the
[00:20:54:030 - 00:20:54:579] **Speaker 1:** numbers in.
[00:20:56:219 - 00:20:59:339] **Speaker 1:** Work out the voltage noise, Work out the noise figures.
[00:21:03:390 - 00:21:08:540] **Speaker 1:** And so for this high source resistance, The AD 549
[00:21:08:540 - 00:21:10:319] **Speaker 1:** is a much better choice of off amp.
[00:21:29:479 - 00:21:35:209] **Speaker 1:** Is the best Choice Overwhelm.
[00:21:38:630 - 00:21:41:150] **Speaker 1:** I haven't gone and I could have probably just done
[00:21:41:150 - 00:21:42:030] **Speaker 1:** the noise figure.
[00:21:43:489 - 00:21:46:510] **Speaker 1:** For that one as well, and you'll find the 8549.
[00:21:47:479 - 00:21:49:880] **Speaker 1:** Would they have a bigger noise figure, haven't actually done
[00:21:49:880 - 00:21:50:160] **Speaker 1:** that.
[00:21:51:260 - 00:21:52:390] **Speaker 1:** You get the point, hopefully.
[00:21:59:099 - 00:22:03:550] **Speaker 1:** And you are still, it looks like you're All right.
[00:22:05:119 - 00:22:08:069] **Speaker 1:** That's a -18, so yeah, this is still dominating there.
[00:22:10:339 - 00:22:12:469] **Speaker 1:** But my main point about the slide is to show,
[00:22:12:989 - 00:22:14:829] **Speaker 1:** first of all, to show that, you know, the choice
[00:22:14:829 - 00:22:16:770] **Speaker 1:** of OPA really does affect.
[00:22:17:890 - 00:22:20:790] **Speaker 1:** The relative contribution of each team and the fact that
[00:22:20:790 - 00:22:22:069] **Speaker 1:** the source resistance.
[00:22:24:290 - 00:22:25:760] **Speaker 1:** Has a big effect as well.
[00:22:29:859 - 00:22:30:910] **Speaker 1:** And that's it for the slide.
[00:22:32:760 - 00:22:33:270] **Speaker 1:** Move on.
[00:22:36:800 - 00:22:37:540] **Speaker 1:** That 14.
[00:22:38:560 - 00:22:40:229] **Speaker 1:** So I'm not, I'm only 20 minutes behind.
[00:22:40:290 - 00:22:40:890] **Speaker 1:** That's not too bad.
[00:22:40:969 - 00:22:42:040] **Speaker 1:** I'm actually on to lecture 14.
[00:22:42:099 - 00:22:43:089] **Speaker 1:** This is lecture 14.
[00:22:45:300 - 00:22:47:880] **Speaker 1:** So discuss wide bean noise and filtering.
[00:22:50:469 - 00:22:55:410] **Speaker 1:** Let's see, um, I'd say this was general.
[00:22:56:430 - 00:23:00:349] **Speaker 1:** Information I don't really ask.
[00:23:00:430 - 00:23:02:030] **Speaker 1:** I haven't really asked it in the exam.
[00:23:06:800 - 00:23:08:839] **Speaker 1:** But it's a learning outcome that I think it's good
[00:23:08:839 - 00:23:09:359] **Speaker 1:** to know.
[00:23:11:099 - 00:23:12:609] **Speaker 1:** This is definitely in the exam.
[00:23:16:969 - 00:23:18:739] **Speaker 1:** And then I'm hopefully going to get onto some of
[00:23:18:739 - 00:23:21:479] **Speaker 1:** the basic principles of these AC coupled circuits.
[00:23:24:709 - 00:23:28:069] **Speaker 1:** The basic principles aren't really asked as such, but the
[00:23:28:069 - 00:23:29:300] **Speaker 1:** knowledge is needed.
[00:23:31:250 - 00:23:36:369] **Speaker 1:** For the exam But I don't really ask a question
[00:23:36:369 - 00:23:38:239] **Speaker 1:** that says, what are the general principles of an AC
[00:23:38:239 - 00:23:38:810] **Speaker 1:** coupled circuit.
[00:23:38:910 - 00:23:40:729] **Speaker 1:** I don't think I'd even ask, what is an AC
[00:23:40:729 - 00:23:42:829] **Speaker 1:** coupled circuit ever in an exam.
[00:23:44:530 - 00:23:46:369] **Speaker 1:** I'll give an example of an AC covered circuit.
[00:23:46:410 - 00:23:48:810] **Speaker 1:** I just give you an AC covered circuit that you
[00:23:48:810 - 00:23:50:530] **Speaker 1:** have to then do calculations on.
[00:23:52:920 - 00:23:57:319] **Speaker 1:** To, uh, choose certain component values for resistors and capacitors.
[00:23:57:609 - 00:24:00:839] **Speaker 1:** That's what I tend to ask for the AC coupled
[00:24:00:839 - 00:24:03:109] **Speaker 1:** circuit, and it's been every, every year and there'll be
[00:24:03:109 - 00:24:03:979] **Speaker 1:** no change this year.
[00:24:05:199 - 00:24:07:170] **Speaker 1:** If you look at previous exam questions, it'll give you
[00:24:07:170 - 00:24:09:250] **Speaker 1:** a good indication on what will come up this year.
[00:24:11:569 - 00:24:15:380] **Speaker 1:** Lots of uh home examples with solutions and learn.
[00:24:22:310 - 00:24:26:469] **Speaker 1:** So let's just formalise, we'll kind of just write down
[00:24:26:469 - 00:24:27:420] **Speaker 1:** a summary.
[00:24:28:390 - 00:24:31:199] **Speaker 1:** On what I did, especially that last slide or the
[00:24:31:199 - 00:24:32:479] **Speaker 1:** previous one where I did all this.
[00:24:32:520 - 00:24:33:579] **Speaker 1:** This is all the math.
[00:24:34:859 - 00:24:41:280] **Speaker 1:** This is my summary So the choice to get a
[00:24:41:280 - 00:24:43:680] **Speaker 1:** low noise off amp, that's the whole point is you
[00:24:43:680 - 00:24:49:060] **Speaker 1:** want to better, Choose Something that you can do something
[00:24:49:060 - 00:24:49:520] **Speaker 1:** about.
[00:24:50:369 - 00:24:53:050] **Speaker 1:** Like you can't do something, you can't really control what
[00:24:53:050 - 00:24:57:449] **Speaker 1:** your source resistance is or your voltage dividers, so your
[00:24:57:449 - 00:25:01:290] **Speaker 1:** voltage feedback resistances cause that's got to do with the
[00:25:01:290 - 00:25:01:530] **Speaker 1:** application.
[00:25:01:989 - 00:25:04:290] **Speaker 1:** But what you can choose is the right op amp.
[00:25:05:270 - 00:25:10:329] **Speaker 1:** And what I'm saying here is high source resistance then
[00:25:10:339 - 00:25:12:030] **Speaker 1:** you wanna try and choose an op amp that has
[00:25:12:030 - 00:25:13:489] **Speaker 1:** a low current noise.
[00:25:15:290 - 00:25:20:050] **Speaker 1:** And then the opposite, the low source resistance, you want
[00:25:20:050 - 00:25:23:050] **Speaker 1:** to be getting a low Johnson noise for the for
[00:25:23:050 - 00:25:23:609] **Speaker 1:** the op amp.
[00:25:25:750 - 00:25:27:739] **Speaker 1:** And you can have the bipolar input up amps tend
[00:25:27:739 - 00:25:29:689] **Speaker 1:** to have a low voltage noise.
[00:25:34:989 - 00:25:37:189] **Speaker 1:** And then you have the the noise figures a measure
[00:25:37:189 - 00:25:37:810] **Speaker 1:** of this.
[00:25:39:380 - 00:25:41:680] **Speaker 1:** Noise figure is a measure.
[00:25:47:439 - 00:25:55:209] **Speaker 1:** Of this noise And just recall.
[00:26:00:209 - 00:26:16:500] **Speaker 1:** Numerator Is And you can see here, like.
[00:26:17:630 - 00:26:20:069] **Speaker 1:** If you've got a high RS, this is like squared,
[00:26:20:189 - 00:26:21:709] **Speaker 1:** so it's not really good if you've got a high
[00:26:21:709 - 00:26:23:430] **Speaker 1:** current noise, it's going to be squared as well, and
[00:26:23:430 - 00:26:24:250] **Speaker 1:** it's going to be bad.
[00:26:27:010 - 00:26:29:680] **Speaker 1:** But then if the R is small, then the squared
[00:26:29:680 - 00:26:30:439] **Speaker 1:** is really, really small.
[00:26:30:510 - 00:26:32:079] **Speaker 1:** And then this is kind of a squared term and
[00:26:32:079 - 00:26:33:300] **Speaker 1:** this is like a linear term.
[00:26:33:800 - 00:26:35:280] **Speaker 1:** So you can see it with the maths as well
[00:26:35:280 - 00:26:36:579] **Speaker 1:** that that would then dominate.
[00:26:40:099 - 00:26:41:599] **Speaker 1:** So let's just right here.
[00:26:43:489 - 00:26:45:310] **Speaker 1:** To really reinforce the point.
[00:27:14:780 - 00:27:20:839] **Speaker 1:** Because Of 4 KTRS 10.
[00:27:26:119 - 00:27:29:939] **Speaker 1:** So that's that wide band noise.
[00:27:36:260 - 00:27:37:880] **Speaker 1:** That's the total noise.
[00:27:41:000 - 00:27:43:900] **Speaker 1:** If you want to work out the total noise, it's
[00:27:44:239 - 00:27:45:719] **Speaker 1:** a cumulative integral.
[00:27:48:170 - 00:27:50:130] **Speaker 1:** And so you get the noise densities.
[00:27:51:079 - 00:27:52:349] **Speaker 1:** Per frequency.
[00:27:53:689 - 00:27:55:989] **Speaker 1:** But then you cumulatively integrate.
[00:27:57:170 - 00:28:00:290] **Speaker 1:** And so you'd expect these to keep continuing because it's
[00:28:00:290 - 00:28:00:839] **Speaker 1:** all positive.
[00:28:00:890 - 00:28:02:170] **Speaker 1:** All these numbers are all positive.
[00:28:02:250 - 00:28:04:270] **Speaker 1:** You don't have like negative noise.
[00:28:04:729 - 00:28:08:199] **Speaker 1:** It's always like a positive quantity because you're using the
[00:28:08:199 - 00:28:08:949] **Speaker 1:** squared.
[00:28:09:170 - 00:28:12:079] **Speaker 1:** It's like the power, it's like the, or the covariance.
[00:28:12:380 - 00:28:15:229] **Speaker 1:** Statistics always works on the squared, so everything is positive.
[00:28:16:079 - 00:28:19:319] **Speaker 1:** And so if you integrate a positive number, obviously it's
[00:28:19:319 - 00:28:20:050] **Speaker 1:** going to always be positive.
[00:28:20:119 - 00:28:20:939] **Speaker 1:** It's always going to increase.
[00:28:22:300 - 00:28:25:839] **Speaker 1:** So you would expect the total wide band noise for
[00:28:25:839 - 00:28:27:239] **Speaker 1:** each of these op amps.
[00:28:28:250 - 00:28:31:569] **Speaker 1:** To always increase at whatever rate.
[00:28:35:250 - 00:28:37:170] **Speaker 1:** And so let's put in brackets here, it is a
[00:28:37:170 - 00:28:38:469] **Speaker 1:** cumulative.
[00:28:39:859 - 00:28:44:410] **Speaker 1:** Effect to get the total noise in your circuit when
[00:28:44:410 - 00:28:48:050] **Speaker 1:** you're kind of analysing it in terms of like wide
[00:28:48:050 - 00:28:48:520] **Speaker 1:** band.
[00:28:48:859 - 00:28:50:729] **Speaker 1:** If you've got a wide, if you got a big
[00:28:50:729 - 00:28:53:989] **Speaker 1:** wide band that your application is kind of working in.
[00:28:56:339 - 00:28:59:219] **Speaker 1:** Then you have to sum up all the noise like
[00:28:59:219 - 00:28:59:579] **Speaker 1:** that.
[00:29:02:589 - 00:29:05:270] **Speaker 1:** And that's the actual noise that's going to be total
[00:29:05:270 - 00:29:07:939] **Speaker 1:** noise that's going to be influencing the, the, uh, the,
[00:29:08:030 - 00:29:08:790] **Speaker 1:** the amplifier.
[00:29:12:189 - 00:29:15:390] **Speaker 1:** Alright, so that's sort of the preliminary kind of concepts.
[00:29:17:839 - 00:29:18:510] **Speaker 1:** Shall we move on?
[00:29:22:170 - 00:29:23:900] **Speaker 1:** Of course there's a practical, what do you do with
[00:29:23:900 - 00:29:24:640] **Speaker 1:** this noise?
[00:29:25:609 - 00:29:27:329] **Speaker 1:** You try and do your best, you know, you choose
[00:29:27:329 - 00:29:28:880] **Speaker 1:** the best off-ramp that you can.
[00:29:29:449 - 00:29:31:800] **Speaker 1:** You've got your, got your Johnson noise and the resistors,
[00:29:32:089 - 00:29:33:689] **Speaker 1:** but you've still got noise, so how do you deal
[00:29:33:689 - 00:29:34:050] **Speaker 1:** with it?
[00:29:35:250 - 00:29:36:640] **Speaker 1:** Or you need to philtre.
[00:29:40:050 - 00:29:42:530] **Speaker 1:** And so you want to be to limit the amount
[00:29:42:530 - 00:29:43:510] **Speaker 1:** of wide band noise.
[00:29:44:010 - 00:29:46:349] **Speaker 1:** This is the bandwidth here that you might be operating
[00:29:46:349 - 00:29:46:790] **Speaker 1:** over.
[00:29:48:880 - 00:29:51:079] **Speaker 1:** And so you want to limit it.
[00:29:55:109 - 00:29:56:729] **Speaker 1:** You don't want the noise.
[00:29:58:469 - 00:30:00:390] **Speaker 1:** Up here, like you don't want all the noise up
[00:30:00:390 - 00:30:03:890] **Speaker 1:** in the high frequencies causes that can like cause problems.
[00:30:06:739 - 00:30:08:640] **Speaker 1:** could feed back into your circuit.
[00:30:10:880 - 00:30:12:319] **Speaker 1:** And so you want to be able to knock off
[00:30:12:319 - 00:30:12:959] **Speaker 1:** some of that.
[00:30:13:239 - 00:30:14:579] **Speaker 1:** So you got your signal here.
[00:30:15:939 - 00:30:21:920] **Speaker 1:** She's your signal And this is the unwanted noise.
[00:30:30:400 - 00:30:31:800] **Speaker 1:** And what it is.
[00:30:33:010 - 00:30:33:869] **Speaker 1:** Typically.
[00:30:38:650 - 00:30:42:260] **Speaker 1:** White noise Not always, but often you can.
[00:30:42:900 - 00:30:46:410] **Speaker 1:** Treat it as white noise or a white noise power
[00:30:46:410 - 00:30:47:650] **Speaker 1:** spectrum, so it's flat.
[00:30:58:359 - 00:31:05:660] **Speaker 1:** Problem Is Can cause.
[00:31:06:560 - 00:31:07:089] **Speaker 1:** I listen.
[00:31:12:020 - 00:31:13:599] **Speaker 1:** Back onto your signal.
[00:31:14:530 - 00:31:17:410] **Speaker 1:** Cause you cause you're sampling at a slow rate, then
[00:31:17:410 - 00:31:19:250] **Speaker 1:** it can affect your signal.
[00:31:20:699 - 00:31:23:140] **Speaker 1:** And it can distort the signal, so it can be.
[00:31:24:260 - 00:31:26:819] **Speaker 1:** Or distortion of signal.
[00:31:35:550 - 00:31:36:449] **Speaker 1:** So there's a problem.
[00:31:40:180 - 00:31:41:459] **Speaker 1:** So we've got to remove it.
[00:31:47:410 - 00:31:52:650] **Speaker 1:** At the front end Of the receiver before it goes
[00:31:52:650 - 00:31:57:949] **Speaker 1:** downstream into all your, Signal processing, your, your ADC would
[00:31:57:949 - 00:32:01:310] **Speaker 1:** have to, your ADC would be digitally sampling it and
[00:32:01:310 - 00:32:03:829] **Speaker 1:** that would be causing all sorts of havoc because you're
[00:32:03:829 - 00:32:04:709] **Speaker 1:** getting aliasing.
[00:32:05:689 - 00:32:07:699] **Speaker 1:** And so you want to get rid of that at
[00:32:07:699 - 00:32:08:239] **Speaker 1:** source.
[00:32:11:069 - 00:32:12:589] **Speaker 1:** There's really no way around it.
[00:32:12:650 - 00:32:15:770] **Speaker 1:** You always do need some sort of an analogue philtre,
[00:32:16:150 - 00:32:17:930] **Speaker 1:** especially when you go into RF.
[00:32:18:699 - 00:32:21:599] **Speaker 1:** You can't just do digital filtering even though they're getting
[00:32:21:780 - 00:32:23:780] **Speaker 1:** better and better at it, where you can, in some
[00:32:23:780 - 00:32:26:939] **Speaker 1:** cases you can completely avoid for lower frequencies, but in
[00:32:26:939 - 00:32:31:109] **Speaker 1:** the higher frequencies, You absolutely need an analogue philtre at
[00:32:31:109 - 00:32:31:729] **Speaker 1:** the front end.
[00:32:34:439 - 00:32:36:880] **Speaker 1:** So you need to remove at the front, remove the
[00:32:36:880 - 00:32:39:900] **Speaker 1:** noise, sorry, at the front end of the receiver.
[00:32:43:729 - 00:32:45:310] **Speaker 1:** Before feeding.
[00:32:46:739 - 00:32:49:699] **Speaker 1:** Into your ADC and then you have a further philtre.
[00:32:52:209 - 00:32:53:109] **Speaker 1:** Or a digital philtre.
[00:33:00:719 - 00:33:02:109] **Speaker 1:** The noise is quite a big deal really.
[00:33:06:439 - 00:33:10:250] **Speaker 1:** But it is predictable, at least a lot of it
[00:33:10:250 - 00:33:11:130] **Speaker 1:** is predictable.
[00:33:11:410 - 00:33:14:770] **Speaker 1:** Before you even construct your circuit, you can figure out
[00:33:14:770 - 00:33:16:050] **Speaker 1:** how much noise is going to be in it.
[00:33:20:780 - 00:33:22:819] **Speaker 1:** And then you try and minimise everything, you choose the
[00:33:22:819 - 00:33:23:859] **Speaker 1:** best off amp.
[00:33:23:900 - 00:33:26:219] **Speaker 1:** I guess it's not just the choice of of getting
[00:33:26:219 - 00:33:27:819] **Speaker 1:** the best off amp because you've got to take into
[00:33:27:819 - 00:33:32:109] **Speaker 1:** account price and like if you're manufacturing large numbers, you'd
[00:33:32:109 - 00:33:34:060] **Speaker 1:** have to weigh that up with how much noise you're
[00:33:34:060 - 00:33:34:900] **Speaker 1:** willing to accept.
[00:33:36:209 - 00:33:37:369] **Speaker 1:** And it depends on the application.
[00:33:37:420 - 00:33:39:739] **Speaker 1:** If it's a medical application, probably you want to have
[00:33:39:739 - 00:33:41:560] **Speaker 1:** as low as possible and then the costs go up.
[00:33:45:089 - 00:33:46:930] **Speaker 1:** And then you've got to design your philtre as well.
[00:33:47:010 - 00:33:48:589] **Speaker 1:** You need an analogue philtre often.
[00:33:50:599 - 00:33:51:819] **Speaker 1:** That's more complexity.
[00:33:54:760 - 00:33:57:959] **Speaker 1:** And so you would do something like, so there's your.
[00:33:58:810 - 00:34:01:000] **Speaker 1:** You would just do something like that, right?
[00:34:01:369 - 00:34:02:180] **Speaker 1:** Easy noise.
[00:34:03:199 - 00:34:04:390] **Speaker 1:** You have your past banned.
[00:34:05:250 - 00:34:06:430] **Speaker 1:** And then you have your cutoff.
[00:34:07:689 - 00:34:09:360] **Speaker 1:** And then you're wiping out all this.
[00:34:14:138 - 00:34:15:510] **Speaker 1:** So what actually happens?
[00:34:17:050 - 00:34:20:520] **Speaker 1:** Here is by adding this philtre.
[00:34:24:148 - 00:34:26:529] **Speaker 1:** It increases the signal to noise ratio.
[00:34:28:810 - 00:34:31:030] **Speaker 1:** That's the result of adding the philtre.
[00:34:31:530 - 00:34:33:709] **Speaker 1:** The noise power, in this case you can see here.
[00:34:34:739 - 00:34:37:719] **Speaker 1:** It is, it has halved in this particular case.
[00:34:41:500 - 00:34:43:699] **Speaker 1:** And it's just a formula for noise power.
[00:34:44:780 - 00:34:48:699] **Speaker 1:** Bandwidth times um times the noise level is what the
[00:34:48:699 - 00:34:49:648] **Speaker 1:** noise power is.
[00:34:58:129 - 00:34:58:540] **Speaker 1:** All right.
[00:35:03:929 - 00:35:05:370] **Speaker 1:** And I'm just looking at this.
[00:35:13:899 - 00:35:14:179] **Speaker 1:** Cool.
[00:35:17:040 - 00:35:17:729] **Speaker 1:** Enough on that.
[00:35:23:260 - 00:35:25:560] **Speaker 1:** So here's um the LT 1028.
[00:35:27:290 - 00:35:29:010] **Speaker 1:** And you look down here and you can see well
[00:35:29:010 - 00:35:31:969] **Speaker 1:** at one kilohertz we're looking at.
[00:35:32:830 - 00:35:35:530] **Speaker 1:** 1.1 nanovolts, you can actually plot this.
[00:35:38:399 - 00:35:39:770] **Speaker 1:** So we're around about here.
[00:35:41:520 - 00:35:42:479] **Speaker 1:** 1.1.
[00:35:45:399 - 00:35:47:340] **Speaker 1:** Change it with the frequency, because here we've got 10
[00:35:47:340 - 00:35:48:739] **Speaker 1:** Hz, get it even lower.
[00:35:51:209 - 00:35:53:350] **Speaker 1:** And also giving other information as well.
[00:35:56:729 - 00:35:58:310] **Speaker 1:** I can't actually see any.
[00:36:01:199 - 00:36:02:379] **Speaker 1:** Car noise.
[00:36:03:620 - 00:36:05:800] **Speaker 1:** So sometimes that's the case.
[00:36:09:399 - 00:36:12:909] **Speaker 1:** So that's So current noise.
[00:36:16:790 - 00:36:22:870] **Speaker 1:** is so low that It is essentially ignored.
[00:36:31:030 - 00:36:33:350] **Speaker 1:** You can ignore it essentially just to say, well, it's
[00:36:33:350 - 00:36:33:969] **Speaker 1:** 0.
[00:36:44:090 - 00:36:44:260] **Speaker 1:** right.
[00:36:51:840 - 00:36:54:320] **Speaker 1:** And that's just giving you an example, amp.
[00:36:54:840 - 00:36:58:080] **Speaker 1:** And yeah, just the fact that it varies versus frequency.
[00:36:59:669 - 00:37:01:110] **Speaker 1:** Nothing much more I need to add, dear.
[00:37:02:949 - 00:37:03:830] **Speaker 1:** It's just an example.
[00:37:06:919 - 00:37:08:070] **Speaker 1:** Of what you get.
[00:37:09:209 - 00:37:10:979] **Speaker 1:** It's what I want to spend the rest of, quite
[00:37:10:979 - 00:37:12:280] **Speaker 1:** a bit of the rest of the time on.
[00:37:13:090 - 00:37:14:449] **Speaker 1:** Is to is to.
[00:37:15:649 - 00:37:17:800] **Speaker 1:** Look at this op amp selection guide because this is
[00:37:17:800 - 00:37:19:540] **Speaker 1:** what I often like asking the exam.
[00:37:23:699 - 00:37:25:800] **Speaker 1:** I'll first of all tell you kind of the trick,
[00:37:25:810 - 00:37:26:959] **Speaker 1:** and then I'll explain why.
[00:37:28:729 - 00:37:31:290] **Speaker 1:** And so of course these are all analogue devices.
[00:37:32:219 - 00:37:34:340] **Speaker 1:** Used to be linear technology, so they like to put
[00:37:34:340 - 00:37:36:780] **Speaker 1:** all their iPods off amps on there so you can
[00:37:36:780 - 00:37:37:159] **Speaker 1:** buy them.
[00:37:38:110 - 00:37:40:070] **Speaker 1:** But I, I think it's quite a neat way of
[00:37:40:070 - 00:37:43:459] **Speaker 1:** kind of like grouping them all together to make your
[00:37:43:459 - 00:37:45:149] **Speaker 1:** life easy for choosing an op amp.
[00:37:49:800 - 00:37:54:399] **Speaker 1:** And you tend to, you start off with your equivalent
[00:37:54:399 - 00:37:55:419] **Speaker 1:** noise in the circuit.
[00:37:56:709 - 00:37:59:959] **Speaker 1:** So your equivalent uh resistant noise?
[00:38:02:639 - 00:38:05:229] **Speaker 1:** And that gives you the value down here.
[00:38:06:530 - 00:38:09:129] **Speaker 1:** And with your equivalent amount of resistor noise, this is
[00:38:09:129 - 00:38:09:969] **Speaker 1:** a log log graph.
[00:38:10:010 - 00:38:11:570] **Speaker 1:** You can actually look up on this line and it
[00:38:11:570 - 00:38:13:149] **Speaker 1:** tells you what the Johnson noise is.
[00:38:15:469 - 00:38:18:320] **Speaker 1:** But then there's a trick, and this is what's kind
[00:38:18:320 - 00:38:20:120] **Speaker 1:** of counterintuitive.
[00:38:22:159 - 00:38:24:110] **Speaker 1:** If you choose some sort of op amp.
[00:38:24:919 - 00:38:29:719] **Speaker 1:** Like this one And you look at the spec sheet,
[00:38:29:810 - 00:38:33:409] **Speaker 1:** it has a it has a voltage noise and it
[00:38:33:409 - 00:38:36:800] **Speaker 1:** has a current noise cause that Uh, except at least
[00:38:36:800 - 00:38:39:169] **Speaker 1:** the current noise is so small, but yeah, Schumer has
[00:38:39:169 - 00:38:40:830] **Speaker 1:** a current noise and a voltage noise.
[00:38:42:659 - 00:38:46:840] **Speaker 1:** What you can actually do, which seems crazy, is you
[00:38:46:840 - 00:38:50:520] **Speaker 1:** can take the ratio between the voltage noise and the
[00:38:50:520 - 00:38:55:260] **Speaker 1:** current noise and get an off amp in quotes, resistance.
[00:38:56:800 - 00:39:01:600] **Speaker 1:** Which there's actually no correlation between this is a completely
[00:39:01:600 - 00:39:02:360] **Speaker 1:** mathematical trick.
[00:39:02:439 - 00:39:06:280] **Speaker 1:** There's actually no correlation between the voltage noise in an
[00:39:06:280 - 00:39:08:919] **Speaker 1:** off-ramp and the current noise in the off- amp.
[00:39:08:959 - 00:39:09:919] **Speaker 1:** They should not be related.
[00:39:10:000 - 00:39:11:379] **Speaker 1:** There's no vehicles IR.
[00:39:11:439 - 00:39:12:340] **Speaker 1:** It should not exist.
[00:39:14:239 - 00:39:18:489] **Speaker 1:** But you can still kind of do it.
[00:39:18:989 - 00:39:22:310] **Speaker 1:** So if you take the ratio of the, and I'll
[00:39:22:310 - 00:39:22:969] **Speaker 1:** show you why later.
[00:39:23:030 - 00:39:24:209] **Speaker 1:** It's really interesting.
[00:39:25:260 - 00:39:29:300] **Speaker 1:** Take the ratio of the voltage noise and sorry vehicles
[00:39:29:300 - 00:39:31:929] **Speaker 1:** IR's like, yeah, between the voltage noise and the current
[00:39:31:929 - 00:39:35:179] **Speaker 1:** noise, it gives you an off amp resistance in quotes.
[00:39:36:360 - 00:39:40:709] **Speaker 1:** And what analogue devices are saying is that There's two
[00:39:40:709 - 00:39:41:439] **Speaker 1:** types of resistance.
[00:39:41:909 - 00:39:45:199] **Speaker 1:** There's there's the real real world resistance, which is your
[00:39:46:169 - 00:39:48:699] **Speaker 1:** Your feedback resistors, the source resistance, they all create an
[00:39:48:699 - 00:39:49:879] **Speaker 1:** equivalent resistance.
[00:39:50:760 - 00:39:53:780] **Speaker 1:** And then there's the op amp resistance which they call
[00:39:54:120 - 00:39:55:699] **Speaker 1:** um our opt.
[00:39:56:909 - 00:40:01:419] **Speaker 1:** And You can you can you can work out what
[00:40:01:419 - 00:40:02:699] **Speaker 1:** the current noise is.
[00:40:03:020 - 00:40:04:870] **Speaker 1:** It's another useful thing about this graph.
[00:40:05:989 - 00:40:10:070] **Speaker 1:** Is this particular op amp here, you can read across
[00:40:10:070 - 00:40:11:409] **Speaker 1:** to get the voltage noise.
[00:40:12:030 - 00:40:13:909] **Speaker 1:** And if you want the current noise, you just work
[00:40:13:909 - 00:40:16:870] **Speaker 1:** out what the Rop is down here and then um
[00:40:16:870 - 00:40:19:310] **Speaker 1:** I is gonna be what, in this case, V over
[00:40:19:310 - 00:40:20:750] **Speaker 1:** R V over R opt.
[00:40:22:360 - 00:40:27:280] **Speaker 1:** But what, what's interesting is The are opt.
[00:40:30:699 - 00:40:34:449] **Speaker 1:** Is if you choose your op amp.
[00:40:35:250 - 00:40:39:219] **Speaker 1:** So that your Ropt is actually equal to your uh,
[00:40:39:360 - 00:40:42:820] **Speaker 1:** your real-world, um, resistance.
[00:40:43:479 - 00:40:45:360] **Speaker 1:** It's actually the best choice of op amp.
[00:40:46:070 - 00:40:49:669] **Speaker 1:** This is crazy, but it just works out that if
[00:40:49:669 - 00:40:54:419] **Speaker 1:** you've got a certain equivalent resistance, right, in your circuit
[00:40:54:419 - 00:40:57:310] **Speaker 1:** um source resistance, feedback resistance.
[00:40:58:800 - 00:41:02:149] **Speaker 1:** It turns out that your best choice of OA happens
[00:41:02:149 - 00:41:04:780] **Speaker 1:** to be this are opt imaginary value.
[00:41:05:820 - 00:41:08:820] **Speaker 1:** Being equal to that equivalent resistance.
[00:41:11:719 - 00:41:12:659] **Speaker 1:** It's a nice result.
[00:41:13:850 - 00:41:17:860] **Speaker 1:** Cause Say you were, say you ended up being here,
[00:41:17:939 - 00:41:20:040] **Speaker 1:** but the other point is that you can actually move
[00:41:20:040 - 00:41:22:659] **Speaker 1:** down this line here which is like 10.
[00:41:23:479 - 00:41:25:179] **Speaker 1:** There's 10 back and then 10 down.
[00:41:27:530 - 00:41:30:290] **Speaker 1:** And you can move across here and everything within the
[00:41:30:290 - 00:41:31:310] **Speaker 1:** shaded area.
[00:41:32:419 - 00:41:34:219] **Speaker 1:** Is going to be a really good choice of OP
[00:41:34:219 - 00:41:34:520] **Speaker 1:** amp.
[00:41:36:800 - 00:41:38:239] **Speaker 1:** Anyway, that's, that's the facts.
[00:41:38:370 - 00:41:40:129] **Speaker 1:** That's what this is the smaller thumb.
[00:41:41:110 - 00:41:43:459] **Speaker 1:** And if you look up this op amp selection guide,
[00:41:43:510 - 00:41:46:389] **Speaker 1:** it doesn't even say why, it just says this is
[00:41:46:389 - 00:41:46:810] **Speaker 1:** true.
[00:41:47:669 - 00:41:48:270] **Speaker 1:** Use it.
[00:41:49:459 - 00:41:51:510] **Speaker 1:** All right, now I've just analysed why, because you know
[00:41:51:510 - 00:41:54:149] **Speaker 1:** we're electrical engineers and probably part mathematicians, so we want
[00:41:54:149 - 00:41:54:810] **Speaker 1:** to know why.
[00:41:56:080 - 00:41:57:439] **Speaker 1:** Um, this.
[00:41:58:979 - 00:42:03:030] **Speaker 1:** Is The math for it, which I want you to
[00:42:03:030 - 00:42:04:969] **Speaker 1:** kind of get cos it's not too bad.
[00:42:05:350 - 00:42:07:129] **Speaker 1:** It's a, there's a few approximations.
[00:42:11:159 - 00:42:13:959] **Speaker 1:** But I'd like you to see if you can understand
[00:42:13:959 - 00:42:14:979] **Speaker 1:** what's going on here.
[00:42:17:979 - 00:42:22:830] **Speaker 1:** So we have our um op amp here, source resistance,
[00:42:22:989 - 00:42:25:570] **Speaker 1:** got Johnson noise, current noise.
[00:42:27:070 - 00:42:29:699] **Speaker 1:** And we got 2 resistors that caused the amplification.
[00:42:34:939 - 00:42:41:729] **Speaker 1:** And so if I look at I don't know, he.
[00:42:45:709 - 00:42:47:860] **Speaker 1:** This is where I need to make a definition.
[00:42:53:679 - 00:42:57:060] **Speaker 1:** What I kind of want is a term which says
[00:42:57:820 - 00:42:59:439] **Speaker 1:** This is my induced.
[00:43:00:409 - 00:43:03:439] **Speaker 1:** Voltage noise as a result of the current noise.
[00:43:04:330 - 00:43:09:810] **Speaker 1:** So what I'm going to say is, He is like,
[00:43:10:179 - 00:43:12:889] **Speaker 1:** you know, is often, often used, um.
[00:43:13:639 - 00:43:16:030] **Speaker 1:** I'm using E because that actually came out of that,
[00:43:16:110 - 00:43:16:939] **Speaker 1:** uh, white paper.
[00:43:17:989 - 00:43:20:399] **Speaker 1:** EIN squared.
[00:43:31:090 - 00:43:33:090] **Speaker 1:** And if you look back at the non-inverting op amp,
[00:43:33:129 - 00:43:35:090] **Speaker 1:** you'll see that there is a term here like where
[00:43:35:090 - 00:43:37:909] **Speaker 1:** you do this, you can take the squares of those.
[00:43:41:010 - 00:43:43:629] **Speaker 1:** And you can see it here.
[00:43:45:959 - 00:43:47:719] **Speaker 1:** Cause this is the total noise which you you would
[00:43:47:719 - 00:43:49:879] **Speaker 1:** have seen before like when you look back in the
[00:43:49:879 - 00:43:50:810] **Speaker 1:** earlier slides.
[00:43:51:280 - 00:43:52:739] **Speaker 1:** You'd just sum all the squares.
[00:43:56:020 - 00:43:59:030] **Speaker 1:** Of course you do, you've got a um parallel resistance
[00:43:59:030 - 00:44:01:610] **Speaker 1:** here, and you've got a source resistance, so you've got
[00:44:02:110 - 00:44:04:229] **Speaker 1:** um both of those are added.
[00:44:05:189 - 00:44:06:939] **Speaker 1:** When you get those, this is the total amount of
[00:44:06:939 - 00:44:07:709] **Speaker 1:** noise in the circuit.
[00:44:10:850 - 00:44:16:350] **Speaker 1:** And what I've done here is I've Obviously, I've just
[00:44:16:729 - 00:44:18:129] **Speaker 1:** collected the term for IN.
[00:44:19:000 - 00:44:21:500] **Speaker 1:** And I've got an REQ here.
[00:44:24:409 - 00:44:26:389] **Speaker 1:** So there's a couple of, there's one definition here.
[00:44:28:879 - 00:44:30:530] **Speaker 1:** So, I'll do it up here because this is.
[00:44:34:520 - 00:44:35:379] **Speaker 1:** It's up there.
[00:44:36:550 - 00:44:41:550] **Speaker 1:** So, that's That whole team is there and I'm calling
[00:44:41:550 - 00:44:42:580] **Speaker 1:** this whole contribution.
[00:44:44:020 - 00:44:46:479] **Speaker 1:** EIN because I've got an E because it's got to
[00:44:46:479 - 00:44:52:000] **Speaker 1:** do with the voltage noise and um, I've got a
[00:44:52:000 - 00:44:54:479] **Speaker 1:** sub in cause I'm saying it's the voltage noise that's
[00:44:54:479 - 00:44:58:260] **Speaker 1:** associated with the current noise, and that's my definition.
[00:44:58:760 - 00:45:00:719] **Speaker 1:** And I'm just separating it out so you can see
[00:45:00:719 - 00:45:03:219] **Speaker 1:** this is a separate quantity to analyse.
[00:45:04:600 - 00:45:06:800] **Speaker 1:** See this this is a separate team that I'm kind
[00:45:06:800 - 00:45:07:899] **Speaker 1:** of pulling apart.
[00:45:08:629 - 00:45:10:030] **Speaker 1:** And I'm going to look at it a little bit
[00:45:10:030 - 00:45:10:489] **Speaker 1:** further.
[00:45:12:870 - 00:45:14:310] **Speaker 1:** And then the REQ.
[00:45:18:419 - 00:45:20:840] **Speaker 1:** is your equivalent resistance, which I said before.
[00:45:20:959 - 00:45:23:439] **Speaker 1:** It's the sum of all your effective resistances, which is
[00:45:23:439 - 00:45:27:360] **Speaker 1:** the parallel resistance from your feedback resistance plus your source
[00:45:27:360 - 00:45:28:100] **Speaker 1:** resistance.
[00:45:30:270 - 00:45:33:070] **Speaker 1:** So, to this point here, this is just standard stuff
[00:45:33:070 - 00:45:37:229] **Speaker 1:** that I've already told you and it's completely 100% mathematically
[00:45:37:229 - 00:45:38:909] **Speaker 1:** correct in terms of the total noise.
[00:45:39:110 - 00:45:41:229] **Speaker 1:** All I've done is rearranged it and I've used different
[00:45:41:229 - 00:45:42:729] **Speaker 1:** definitions of things.
[00:45:44:060 - 00:45:44:840] **Speaker 1:** Of teams.
[00:45:45:610 - 00:45:47:429] **Speaker 1:** But now becomes the bit of magic.
[00:45:49:899 - 00:45:51:479] **Speaker 1:** I'm going to say.
[00:45:54:310 - 00:45:57:540] **Speaker 1:** That the square of this.
[00:46:02:739 - 00:46:05:620] **Speaker 1:** is approximately equal to that.
[00:46:08:000 - 00:46:09:199] **Speaker 1:** Which is true.
[00:46:11:409 - 00:46:17:219] **Speaker 1:** Win Your parallel resistance, I don't know if you know
[00:46:17:219 - 00:46:18:560] **Speaker 1:** that mathematical signal.
[00:46:19:139 - 00:46:21:060] **Speaker 1:** That just means much smaller then, then we have two
[00:46:21:060 - 00:46:21:899] **Speaker 1:** of those, you know that?
[00:46:23:050 - 00:46:24:889] **Speaker 1:** So let's go right there.
[00:46:26:500 - 00:46:36:389] **Speaker 1:** Or And that's very often the case.
[00:46:36:510 - 00:46:39:469] **Speaker 1:** If you look at many, many applications, you'll find that
[00:46:39:469 - 00:46:43:189] **Speaker 1:** the power of resistance is often much, much less than
[00:46:43:189 - 00:46:45:659] **Speaker 1:** your source resistance or the other way around.
[00:46:45:909 - 00:46:48:090] **Speaker 1:** In many, many cases, that is true.
[00:46:52:969 - 00:46:55:050] **Speaker 1:** And what seems to be interesting is, even if it's
[00:46:55:050 - 00:46:58:429] **Speaker 1:** not quite true, but it's still a little bit smaller,
[00:46:58:810 - 00:47:00:790] **Speaker 1:** it's still reasonably OK.
[00:47:01:469 - 00:47:03:889] **Speaker 1:** It seems to work just about all the time.
[00:47:05:020 - 00:47:06:479] **Speaker 1:** This assumption here.
[00:47:07:489 - 00:47:09:600] **Speaker 1:** Which is mathematically incorrect.
[00:47:10:300 - 00:47:11:760] **Speaker 1:** But it's an approximation.
[00:47:13:750 - 00:47:17:330] **Speaker 1:** All right, if you do that, so let's just say.
[00:47:18:429 - 00:47:21:270] **Speaker 1:** When this this approximately equal to sign, going from here
[00:47:21:270 - 00:47:21:810] **Speaker 1:** to here.
[00:47:23:270 - 00:47:25:830] **Speaker 1:** Because obviously that's just, that means that now there's two
[00:47:25:830 - 00:47:26:729] **Speaker 1:** REQs in here.
[00:47:30:580 - 00:47:32:979] **Speaker 1:** I'll say, holds.
[00:47:34:709 - 00:47:36:449] **Speaker 1:** For most cases.
[00:47:39:790 - 00:47:43:189] **Speaker 1:** And if you look at real world examples, And I've
[00:47:43:189 - 00:47:45:689] **Speaker 1:** gone through a few just in my own time.
[00:47:48:780 - 00:47:50:919] **Speaker 1:** There's about a 5% difference.
[00:47:59:600 - 00:48:03:699] **Speaker 1:** Now, if you look at this term and this term.
[00:48:08:199 - 00:48:10:830] **Speaker 1:** They are, well I won't say both, I mean I'll
[00:48:10:830 - 00:48:13:179] **Speaker 1:** just say, I'll just say associated.
[00:48:18:280 - 00:48:23:320] **Speaker 1:** With the So those two terms are associated with the
[00:48:23:320 - 00:48:23:760] **Speaker 1:** op amp.
[00:48:23:800 - 00:48:25:719] **Speaker 1:** This has got nothing to do with the op amp.
[00:48:26:040 - 00:48:28:590] **Speaker 1:** It's own, this is just the source resistance and the
[00:48:28:590 - 00:48:29:639] **Speaker 1:** feedback resistance.
[00:48:30:040 - 00:48:31:719] **Speaker 1:** It is not to do with the op amp itself.
[00:48:31:800 - 00:48:34:419] **Speaker 1:** I mean, it's doing an amplification, like it's an inverting
[00:48:34:919 - 00:48:36:139] **Speaker 1:** op amp, but it's not.
[00:48:37:260 - 00:48:38:679] **Speaker 1:** Anything to do with the opient noise.
[00:48:42:100 - 00:48:45:659] **Speaker 1:** And so what intuitively, and I've just spent the last
[00:48:45:659 - 00:48:47:860] **Speaker 1:** few slides kind of get you to getting you to
[00:48:47:860 - 00:48:50:699] **Speaker 1:** have that intuition on how you choose op amps.
[00:48:51:489 - 00:48:55:330] **Speaker 1:** You want to choose an op amp that has that
[00:48:55:330 - 00:48:58:929] **Speaker 1:** has small noise compared to the resistors.
[00:49:00:010 - 00:49:02:409] **Speaker 1:** Alright, you want your op amp to not have much
[00:49:02:409 - 00:49:05:129] **Speaker 1:** of an impact on noise compared to your resistors.
[00:49:07:469 - 00:49:09:199] **Speaker 1:** That is a good choice of an op amp.
[00:49:10:340 - 00:49:12:260] **Speaker 1:** In other words, what you'd like to do is you'd
[00:49:12:260 - 00:49:14:239] **Speaker 1:** like to minimise the ratio.
[00:49:15:280 - 00:49:16:659] **Speaker 1:** You like to minimise.
[00:49:17:979 - 00:49:24:750] **Speaker 1:** Um, The ratio of This plus this Divided by that,
[00:49:24:909 - 00:49:27:850] **Speaker 1:** if you make that as small as possible, then that
[00:49:27:850 - 00:49:28:979] **Speaker 1:** would be a good choice of op amp.
[00:49:29:750 - 00:49:31:000] **Speaker 1:** That's what we're gonna try and do.
[00:49:33:929 - 00:49:35:290] **Speaker 1:** But what, what do we choose?
[00:49:35:409 - 00:49:36:449] **Speaker 1:** What's the REQ?
[00:49:36:570 - 00:49:39:209] **Speaker 1:** Well, I'm just gonna say, well, let's say it was
[00:49:39:209 - 00:49:43:129] **Speaker 1:** some ratio times a constant of EN over IN.
[00:49:45:840 - 00:49:47:919] **Speaker 1:** Now I'm gonna just say gamma is unknown and we
[00:49:47:919 - 00:49:50:620] **Speaker 1:** want to find out the optimal gamma which is gonna
[00:49:50:620 - 00:49:52:129] **Speaker 1:** be a ratio of these two terms.
[00:49:53:350 - 00:49:54:570] **Speaker 1:** Well, you plug them in.
[00:49:55:800 - 00:49:58:219] **Speaker 1:** And you end up with this expression here.
[00:50:00:629 - 00:50:01:709] **Speaker 1:** And would you believe it?
[00:50:02:040 - 00:50:03:939] **Speaker 1:** What is the optimum gamma, do you think?
[00:50:05:850 - 00:50:09:340] **Speaker 1:** And so this is gonna be If I just take
[00:50:09:959 - 00:50:14:280] **Speaker 1:** that term there, after you've like made this substitution, and
[00:50:14:280 - 00:50:16:449] **Speaker 1:** our goal is to minimise this ratio.
[00:50:16:760 - 00:50:18:520] **Speaker 1:** So you want to choose the gamma that makes this
[00:50:18:520 - 00:50:20:139] **Speaker 1:** number as small as possible.
[00:50:22:840 - 00:50:25:020] **Speaker 1:** And so you are minimising this function.
[00:50:27:100 - 00:50:29:600] **Speaker 1:** One gamma plus one plus one over gamma.
[00:50:30:020 - 00:50:30:739] **Speaker 1:** Have you seen that function?
[00:50:30:800 - 00:50:31:860] **Speaker 1:** It's quite a cool little function.
[00:50:33:879 - 00:50:35:360] **Speaker 1:** I don't know if you've ever seen that in your
[00:50:35:360 - 00:50:35:979] **Speaker 1:** math career.
[00:50:36:159 - 00:50:38:360] **Speaker 1:** Not that you've really had a math career, but I
[00:50:38:360 - 00:50:40:520] **Speaker 1:** think you have been an electrical engineer or mechatronics, I
[00:50:40:520 - 00:50:41:179] **Speaker 1:** suppose, as well.
[00:50:43:120 - 00:50:46:090] **Speaker 1:** Um, at least the electrical side of the mechatronics person
[00:50:46:090 - 00:50:46:540] **Speaker 1:** inside of you.
[00:50:47:409 - 00:50:50:530] **Speaker 1:** Um, I'm just kind of saying that, yeah, in terms
[00:50:50:530 - 00:50:53:250] **Speaker 1:** of the electrical kind of type of mathematics, I don't
[00:50:53:250 - 00:50:53:570] **Speaker 1:** know.
[00:50:53:889 - 00:50:54:709] **Speaker 1:** This is.
[00:50:55:540 - 00:50:57:540] **Speaker 1:** This is what it looks like, and would you believe
[00:50:57:540 - 00:50:57:979] **Speaker 1:** it?
[00:50:59:739 - 00:51:01:679] **Speaker 1:** The minimum is that game equals one.
[00:51:02:379 - 00:51:03:139] **Speaker 1:** Who would have believed that?
[00:51:04:399 - 00:51:06:969] **Speaker 1:** minimise the function 1 and or say F of X
[00:51:06:969 - 00:51:09:570] **Speaker 1:** equals x + 1 over x, the minimum value occurs
[00:51:09:570 - 00:51:10:510] **Speaker 1:** at x equals 1.
[00:51:11:010 - 00:51:11:669] **Speaker 1:** It's amazing.
[00:51:12:149 - 00:51:12:649] **Speaker 1:** It just happens.
[00:51:14:770 - 00:51:16:629] **Speaker 1:** And so, I think that's a cool result.
[00:51:19:110 - 00:51:24:120] **Speaker 1:** So gamma equals 1 minimises, so choosing your equivalent resistance
[00:51:24:120 - 00:51:27:100] **Speaker 1:** to be the ratio of two quantities that don't even
[00:51:27:100 - 00:51:29:709] **Speaker 1:** seem to be related, right?
[00:51:30:139 - 00:51:33:340] **Speaker 1:** To to the actual physical resistance ends up being true.
[00:51:34:129 - 00:51:36:979] **Speaker 1:** So the ratio of these equal to that is the
[00:51:36:979 - 00:51:37:870] **Speaker 1:** best choice of Opan.
[00:51:39:419 - 00:51:41:360] **Speaker 1:** Alright, now I wanna take this further.
[00:51:42:770 - 00:51:45:260] **Speaker 1:** Now we're gonna choose an R opt to be this
[00:51:45:260 - 00:51:46:020] **Speaker 1:** ratio.
[00:51:46:419 - 00:51:48:840] **Speaker 1:** Now please treat us differently like.
[00:51:49:620 - 00:51:51:620] **Speaker 1:** Um, there's two values of resistance.
[00:51:51:699 - 00:51:53:899] **Speaker 1:** There's the REQ, which is a separate thing.
[00:51:53:939 - 00:51:56:040] **Speaker 1:** It's just like your real word resistance.
[00:51:56:620 - 00:51:58:500] **Speaker 1:** And then you have your Rop with this which is
[00:51:58:500 - 00:52:01:879] **Speaker 1:** fake kind of like artificial resistance that we've made up
[00:52:02:300 - 00:52:03:659] **Speaker 1:** for purposes of choosing the op amp.
[00:52:05:199 - 00:52:07:239] **Speaker 1:** So I want to make sure you separate those two
[00:52:07:239 - 00:52:07:639] **Speaker 1:** in your mind.
[00:52:07:709 - 00:52:09:199] **Speaker 1:** They are two different things.
[00:52:11:010 - 00:52:12:979] **Speaker 1:** OK, and.
[00:52:13:750 - 00:52:16:320] **Speaker 1:** And then I showed you that trick where if you
[00:52:16:320 - 00:52:18:669] **Speaker 1:** go onto the graph and you can look across to
[00:52:18:669 - 00:52:21:610] **Speaker 1:** the left and you can get the the voltage noise
[00:52:21:949 - 00:52:23:969] **Speaker 1:** for for it and you can get the current noise
[00:52:24:790 - 00:52:26:469] **Speaker 1:** by looking at the hour opt.
[00:52:28:050 - 00:52:31:199] **Speaker 1:** Now I'm just about yeah just one minute.
[00:52:32:250 - 00:52:35:110] **Speaker 1:** Uh if you use this for the total noise.
[00:52:37:030 - 00:52:39:830] **Speaker 1:** What actually happens when you, you had told you that
[00:52:39:870 - 00:52:40:590] **Speaker 1:** that why does it work?
[00:52:40:750 - 00:52:42:629] **Speaker 1:** Why can you if you've got this point and you've
[00:52:42:629 - 00:52:43:850] **Speaker 1:** got an op amp right here.
[00:52:44:889 - 00:52:46:570] **Speaker 1:** Yes, that's the optimum choice of UPA.
[00:52:47:719 - 00:52:50:520] **Speaker 1:** But if you go to the right from that, what's
[00:52:50:520 - 00:52:51:870] **Speaker 1:** gonna happen when you go to the right?
[00:52:52:080 - 00:52:53:699] **Speaker 1:** You keep the same voltage noise?
[00:52:56:850 - 00:52:58:780] **Speaker 1:** But the hour opt has got to be increasing as
[00:52:58:780 - 00:52:59:620] **Speaker 1:** you go to the right.
[00:53:00:419 - 00:53:03:300] **Speaker 1:** And if our opt increases, the only way this can
[00:53:03:300 - 00:53:04:939] **Speaker 1:** increase is if I decreases.
[00:53:05:709 - 00:53:08:590] **Speaker 1:** And so if IN decreases, the total noise decreases.
[00:53:08:669 - 00:53:11:270] **Speaker 1:** Can you see that if you move to the right
[00:53:11:270 - 00:53:14:189] **Speaker 1:** horizontally, the total noise is gonna decrease.
[00:53:14:669 - 00:53:15:330] **Speaker 1:** This is great.
[00:53:18:330 - 00:53:20:689] **Speaker 1:** If you go down with a slope of 10 to
[00:53:20:689 - 00:53:21:870] **Speaker 1:** 10 to the left.
[00:53:22:669 - 00:53:28:129] **Speaker 1:** Then the ratio is um You're keeping the same current
[00:53:28:129 - 00:53:31:409] **Speaker 1:** noise cause our ops actually decreasing at the same rate
[00:53:31:409 - 00:53:34:090] **Speaker 1:** as EN's going down, so I actually keeps the same.
[00:53:37:179 - 00:53:38:399] **Speaker 1:** Iron stays the same.
[00:53:41:489 - 00:53:45:040] **Speaker 1:** Um, but EN goes down, so the total noise goes
[00:53:45:040 - 00:53:45:389] **Speaker 1:** down.
[00:53:46:469 - 00:53:47:560] **Speaker 1:** So it's great.
[00:53:48:080 - 00:53:49:699] **Speaker 1:** So if you go to the right and you go
[00:53:49:699 - 00:53:52:110] **Speaker 1:** down, everything is great because of the total noise just
[00:53:52:110 - 00:53:56:399] **Speaker 1:** keeps decreasing, so Anywhere in this area is a great
[00:53:56:399 - 00:53:56:820] **Speaker 1:** choice for up.
[00:53:57:840 - 00:53:58:929] **Speaker 1:** And that's where I'm gonna leave it.
[00:53:59:850 - 00:54:03:689] **Speaker 1:** Hope you've got some of that Thank you.
[00:54:04:189 - 00:54:05:129] **Speaker 1:** I thought it was cool.
[00:54:06:169 - 00:54:43:560] **Speaker 1:** But you know, I should say OK Thanks Chris.
[00:54:43:770 - 00:54:45:129] **Speaker 1:** Yeah, OK, thanks, yep.
[00:54:46:659 - 00:54:48:919] **Speaker 1:** Hey, don't you think that's cool, I think that's amazing.
[00:54:49:810 - 00:54:53:010] **Speaker 1:** Who would have thought the virtual resistance.
[00:54:53:050 - 00:54:55:389] **Speaker 0:** A virtual resistance actually is useful.
[00:54:56:050 - 00:54:56:469] **Speaker 0:** Crazy.

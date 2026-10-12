# ENEL372-26S2 Lecture 35 native Echo transcript

Date: October 12, 2026 4:00pm-4:55pm
Transcript type: native Echo automated transcript.

[00:00:00:009 - 00:00:01:129] **Speaker 0:** Uh, wait, oh, there we go.
[00:00:04:949 - 00:00:06:530] **Speaker 0:** Eco people can join at 4 o'clock.
[00:00:07:630 - 00:00:09:630] **Speaker 0:** So yeah, I've left off here the input and peanuts
[00:00:09:630 - 00:00:10:109] **Speaker 0:** improvement.
[00:00:11:079 - 00:00:12:600] **Speaker 0:** This is just a really cunning thing.
[00:00:12:750 - 00:00:14:960] **Speaker 0:** It's really related to the fact that the how the
[00:00:14:960 - 00:00:15:859] **Speaker 0:** op amp works.
[00:00:17:030 - 00:00:19:079] **Speaker 0:** And there's lots of kind of things that look like
[00:00:19:079 - 00:00:21:979] **Speaker 0:** a miracle like seem like magic when it comes to
[00:00:21:979 - 00:00:24:379] **Speaker 0:** offences because anything that comes into here.
[00:00:25:379 - 00:00:28:020] **Speaker 0:** Is in a feedback control to make sure that voltage
[00:00:28:020 - 00:00:29:299] **Speaker 0:** is that voltage, which you know, right?
[00:00:29:420 - 00:00:30:399] **Speaker 0:** That's what knocking does.
[00:00:31:950 - 00:00:34:400] **Speaker 0:** But there's so many tricks you can do with this,
[00:00:34:479 - 00:00:35:259] **Speaker 0:** with that property.
[00:00:36:310 - 00:00:39:709] **Speaker 0:** Uh In the next section I'll be talking about how
[00:00:39:709 - 00:00:42:470] **Speaker 0:** you can even use a sequence of op amps to
[00:00:42:470 - 00:00:46:110] **Speaker 0:** approximate an inductor so you can get an effect of
[00:00:46:110 - 00:00:48:869] **Speaker 0:** a set of op amps that means you don't have
[00:00:48:869 - 00:00:51:110] **Speaker 0:** to wind an inductor and like have all the heavyweight
[00:00:51:110 - 00:00:53:790] **Speaker 0:** inductors and that's active philtres, but this is just another
[00:00:53:790 - 00:00:55:130] **Speaker 0:** trick which I wanted to share.
[00:00:55:630 - 00:00:57:020] **Speaker 0:** I don't think I actually put this in the exam
[00:00:57:020 - 00:00:57:650] **Speaker 0:** or anything, but.
[00:00:59:049 - 00:01:03:909] **Speaker 0:** Um, Just wanna briefly go over it before I move
[00:01:03:909 - 00:01:07:239] **Speaker 0:** on to the filtering part.
[00:01:13:209 - 00:01:16:269] **Speaker 0:** So that If you remember, like if there was a
[00:01:16:269 - 00:01:19:430] **Speaker 0:** voltages divider here and it was going directly into this
[00:01:19:430 - 00:01:21:389] **Speaker 0:** positive input, that would have been real bad because it
[00:01:21:389 - 00:01:24:790] **Speaker 0:** means that the fluctuations from the the source would go
[00:01:24:790 - 00:01:26:870] **Speaker 0:** straight into the positive side of the out amp.
[00:01:28:160 - 00:01:29:370] **Speaker 0:** So you remember I said that was a problem.
[00:01:29:989 - 00:01:32:190] **Speaker 0:** So maybe you might think, well, there's a problem because
[00:01:32:190 - 00:01:34:870] **Speaker 0:** like there is a resistor here, but it still means
[00:01:34:870 - 00:01:37:650] **Speaker 0:** that it's gonna maybe come into the positive.
[00:01:38:849 - 00:01:40:669] **Speaker 0:** So that's a reasonable question to ask.
[00:01:42:709 - 00:01:45:900] **Speaker 0:** Is there a voltage source fluctuation?
[00:01:46:720 - 00:01:47:620] **Speaker 0:** Coupling problem.
[00:01:48:250 - 00:01:50:610] **Speaker 0:** Where that that gets coupled into the oping and then
[00:01:50:610 - 00:01:53:010] **Speaker 0:** it just makes it go unstable and all sorts of
[00:01:53:010 - 00:01:54:250] **Speaker 0:** bad things happen.
[00:01:56:699 - 00:01:58:779] **Speaker 0:** Well, maybe at first sight you think there is, but
[00:01:58:779 - 00:01:59:900] **Speaker 0:** actually the answer is no.
[00:02:03:089 - 00:02:05:349] **Speaker 0:** And so adding these capacitor and this resistor.
[00:02:07:629 - 00:02:08:550] **Speaker 0:** It's cold.
[00:02:09:199 - 00:02:10:539] **Speaker 0:** It's called a bootstrap.
[00:02:11:710 - 00:02:12:320] **Speaker 0:** Capacity.
[00:02:15:830 - 00:02:17:389] **Speaker 0:** Bootstrap capacitor.
[00:02:22:059 - 00:02:22:699] **Speaker 0:** Mostly.
[00:02:24:429 - 00:02:27:740] **Speaker 0:** It's shorts The icy noise.
[00:02:29:009 - 00:02:31:179] **Speaker 0:** This is the high level hand wavy.
[00:02:32:279 - 00:02:34:580] **Speaker 0:** Um, intuitive kind of explanation.
[00:02:36:410 - 00:02:38:710] **Speaker 0:** Um, so it's the AC noise.
[00:02:43:740 - 00:02:45:240] **Speaker 0:** To the low impedance.
[00:02:50:639 - 00:02:52:130] **Speaker 0:** Open airport.
[00:02:53:750 - 00:02:55:710] **Speaker 0:** So this is no impedance here, this is the high
[00:02:55:710 - 00:02:56:500] **Speaker 0:** impedance input.
[00:02:59:949 - 00:03:01:809] **Speaker 0:** And what has happened.
[00:03:01:970 - 00:03:04:270] **Speaker 0:** So the current, though you think the current might be
[00:03:04:270 - 00:03:05:229] **Speaker 0:** able to flow into here.
[00:03:06:850 - 00:03:07:729] **Speaker 0:** Is blocked.
[00:03:08:720 - 00:03:10:529] **Speaker 0:** And it's blocked by a combination of the fact that
[00:03:10:529 - 00:03:12:520] **Speaker 0:** this is a reasonably high resistance, but it's not really
[00:03:12:520 - 00:03:13:699] **Speaker 0:** the fact that it's a high resistance.
[00:03:14:779 - 00:03:15:990] **Speaker 0:** That blocks the current.
[00:03:16:490 - 00:03:20:570] **Speaker 0:** It's the capacitor's choice of capacitors, and it's the feedback
[00:03:20:570 - 00:03:22:330] **Speaker 0:** control of the op amp, and I'll explain that in
[00:03:22:330 - 00:03:23:210] **Speaker 0:** the next page.
[00:03:24:029 - 00:03:25:740] **Speaker 0:** But what effectively it does.
[00:03:27:179 - 00:03:31:210] **Speaker 0:** you end up, this is your 5 out.
[00:03:31:470 - 00:03:32:669] **Speaker 0:** That's your 5 out.
[00:03:33:880 - 00:03:35:720] **Speaker 0:** And because it's like a voter's follower.
[00:03:36:399 - 00:03:39:199] **Speaker 0:** It's the same as VN in this case, it's a
[00:03:39:199 - 00:03:40:119] **Speaker 0:** voltage follower.
[00:03:43:449 - 00:03:45:979] **Speaker 0:** Which is great because then you can um decouple, you
[00:03:45:979 - 00:03:48:809] **Speaker 0:** can have a buffer between your input and the output
[00:03:48:809 - 00:03:49:100] **Speaker 0:** load.
[00:03:49:179 - 00:03:50:880] **Speaker 0:** That's why you wanna use a voltage follower.
[00:03:52:570 - 00:03:55:289] **Speaker 0:** So op amps are great at buffering against the, against
[00:03:55:289 - 00:03:57:750] **Speaker 0:** the input and the load, you probably should know that.
[00:03:58:600 - 00:04:01:529] **Speaker 0:** Uh, sort of general knowledge.
[00:04:02:690 - 00:04:05:669] **Speaker 0:** What this particular choice comacitors does.
[00:04:06:880 - 00:04:10:039] **Speaker 0:** Is it sits these voters, it forces these voters to
[00:04:10:039 - 00:04:10:740] **Speaker 0:** be the same.
[00:04:11:679 - 00:04:13:119] **Speaker 0:** And you'll see in the next page it's got to
[00:04:13:119 - 00:04:16:278] **Speaker 0:** do with the filtering properties, combination of low-pass filtering of
[00:04:16:278 - 00:04:19:500] **Speaker 0:** the of the offset and then the high pass filtering.
[00:04:20:070 - 00:04:21:940] **Speaker 0:** Um, but if you can just see.
[00:04:22:690 - 00:04:27:350] **Speaker 0:** That If this is the uh if this is the
[00:04:27:350 - 00:04:30:750] **Speaker 0:** output voltage, who cares what it is some value.
[00:04:31:470 - 00:04:33:549] **Speaker 0:** Then you know that it's a voltage follower, so the
[00:04:33:549 - 00:04:35:160] **Speaker 0:** output is there, which means the input's there.
[00:04:35:230 - 00:04:36:309] **Speaker 0:** So that should be easy to see.
[00:04:37:140 - 00:04:38:559] **Speaker 0:** This just needs a little bit of proof.
[00:04:39:019 - 00:04:40:910] **Speaker 0:** But if you can see that this has been ordered
[00:04:40:910 - 00:04:41:500] **Speaker 0:** the same.
[00:04:42:619 - 00:04:47:019] **Speaker 0:** Then you got this voltage down this line here and
[00:04:47:019 - 00:04:49:700] **Speaker 0:** it's the same as this voltage here across the resistor.
[00:04:50:820 - 00:04:54:399] **Speaker 0:** So you've got a zero voltage drop across the resistor.
[00:04:54:739 - 00:04:56:000] **Speaker 0:** That shouldn't be possible, right?
[00:04:56:760 - 00:04:58:500] **Speaker 0:** Of course, that's not possible if you didn't have an
[00:04:58:500 - 00:04:58:970] **Speaker 0:** op amp.
[00:04:59:420 - 00:05:01:609] **Speaker 0:** If you just got like a resistor, you got a
[00:05:01:609 - 00:05:02:700] **Speaker 0:** voltage source, you have a resistor.
[00:05:02:739 - 00:05:03:820] **Speaker 0:** There's gonna be a voltage drop, right?
[00:05:03:859 - 00:05:04:950] **Speaker 0:** And you get a current flow.
[00:05:05:700 - 00:05:07:779] **Speaker 0:** But because of the op amp and the choice of
[00:05:07:779 - 00:05:10:670] **Speaker 0:** this, it actually effectively means there's no voltage drop.
[00:05:11:100 - 00:05:13:339] **Speaker 0:** So it thinks that there's an infinite resistance.
[00:05:14:190 - 00:05:14:470] **Speaker 0:** Here.
[00:05:14:829 - 00:05:16:510] **Speaker 0:** So in other words, zero current flow.
[00:05:18:510 - 00:05:20:899] **Speaker 0:** Because current can't flow and this there's a voltage difference.
[00:05:21:399 - 00:05:23:880] **Speaker 0:** So using the op amp to force those two voltages
[00:05:23:880 - 00:05:25:589] **Speaker 0:** to be the same, you can't get a current flow.
[00:05:25:929 - 00:05:27:049] **Speaker 0:** So that is shorting.
[00:05:27:119 - 00:05:28:679] **Speaker 0:** So then the only current flow can go to the
[00:05:28:679 - 00:05:31:149] **Speaker 0:** output, which is the low impedance, which is a really
[00:05:31:149 - 00:05:34:959] **Speaker 0:** cunning use of these components and the op amp, and
[00:05:34:959 - 00:05:37:869] **Speaker 0:** that's really all I wanted to say about that slide.
[00:05:38:190 - 00:05:39:510] **Speaker 0:** But then the next slide I'll show you.
[00:05:40:859 - 00:05:41:700] **Speaker 0:** Some of the myths.
[00:05:45:100 - 00:05:49:220] **Speaker 0:** So there are other ways of um mitigating the noise
[00:05:49:220 - 00:05:49:820] **Speaker 0:** from the supply.
[00:05:49:859 - 00:05:51:399] **Speaker 0:** That's my main point of this slide.
[00:05:54:100 - 00:05:55:760] **Speaker 0:** Is blocked by.
[00:05:57:489 - 00:06:00:540] **Speaker 0:** Infinite Resistance.
[00:06:00:980 - 00:06:03:779] **Speaker 0:** Obviously, it's not a real infinite resistance, but it appears
[00:06:03:779 - 00:06:04:459] **Speaker 0:** as though it is.
[00:06:08:829 - 00:06:10:570] **Speaker 0:** So it can't get into that positive.
[00:06:15:579 - 00:06:16:260] **Speaker 0:** So this.
[00:06:17:540 - 00:06:20:350] **Speaker 0:** This here Is.
[00:06:20:989 - 00:06:22:730] **Speaker 0:** This appears.
[00:06:25:540 - 00:06:29:299] **Speaker 0:** Like An infinite resistance.
[00:06:40:670 - 00:06:41:040] **Speaker 0:** All right.
[00:06:46:470 - 00:06:47:790] **Speaker 0:** And then the slide and then we're about to get
[00:06:47:790 - 00:06:48:690] **Speaker 0:** onto the next.
[00:06:49:760 - 00:06:52:109] **Speaker 0:** Lecture 16 outcome, uh learning outcomes.
[00:06:53:420 - 00:06:53:899] **Speaker 0:** All right.
[00:06:57:619 - 00:06:58:420] **Speaker 0:** Here's the math for it.
[00:06:58:459 - 00:06:59:059] **Speaker 0:** You don't have to.
[00:06:59:250 - 00:07:00:839] **Speaker 0:** This is not an exam or anything.
[00:07:01:339 - 00:07:02:739] **Speaker 0:** If you're interested, you can look at this in your
[00:07:02:739 - 00:07:05:220] **Speaker 0:** own time, but I'm just following Kutcher's laws all around
[00:07:05:220 - 00:07:06:000] **Speaker 0:** the circuit here.
[00:07:06:950 - 00:07:08:890] **Speaker 0:** And whenever you got an op amp, you can always
[00:07:08:890 - 00:07:12:070] **Speaker 0:** assume that whatever the voltage comes in here, and this
[00:07:12:070 - 00:07:13:709] **Speaker 0:** causes a voltage follow, it's got to be feedback.
[00:07:13:790 - 00:07:15:649] **Speaker 0:** So let me make these, these are always the same,
[00:07:15:910 - 00:07:17:529] **Speaker 0:** you know, for an op amp, you should know that.
[00:07:18:929 - 00:07:21:079] **Speaker 0:** And then you can just formulate the equations of just
[00:07:21:079 - 00:07:23:970] **Speaker 0:** differentiating them, plugging them in, but I don't really want
[00:07:23:970 - 00:07:25:049] **Speaker 0:** to discuss the details.
[00:07:25:130 - 00:07:27:630] **Speaker 0:** I just want to show you the end result.
[00:07:28:630 - 00:07:31:190] **Speaker 0:** you can write, because V1, I'm trying to show that
[00:07:31:190 - 00:07:32:769] **Speaker 0:** V1 is essentially V0.
[00:07:33:910 - 00:07:35:910] **Speaker 0:** Because at the moment it's not, it's not trivial to
[00:07:35:910 - 00:07:36:570] **Speaker 0:** try and see that.
[00:07:38:070 - 00:07:43:079] **Speaker 0:** Um, And you can write V1 as being a high
[00:07:43:079 - 00:07:45:559] **Speaker 0:** pass philtre on the input.
[00:07:46:440 - 00:07:48:519] **Speaker 0:** And that's what this is, because this is, you'd always
[00:07:48:519 - 00:07:50:920] **Speaker 0:** wanna choose these values so that you can pass the
[00:07:50:920 - 00:07:51:160] **Speaker 0:** input.
[00:07:51:179 - 00:07:53:980] **Speaker 0:** It'd be a bit silly if you If you attenuated
[00:07:53:980 - 00:07:56:779] **Speaker 0:** your input, you want a high pass philtre, right, that's
[00:07:56:779 - 00:07:57:459] **Speaker 0:** what you want to get in.
[00:07:58:750 - 00:08:01:429] **Speaker 0:** So that's a high-pass philtre on the input and so
[00:08:01:429 - 00:08:04:089] **Speaker 0:** you can see that uh and also the offset.
[00:08:05:279 - 00:08:07:119] **Speaker 0:** This is a low pass philtre on the offset.
[00:08:08:850 - 00:08:11:529] **Speaker 0:** And so any low password or on an offset is
[00:08:11:529 - 00:08:13:670] **Speaker 0:** going to remove the offset, that's what does right?
[00:08:15:200 - 00:08:17:799] **Speaker 0:** Um, so, no, no, I mean, it removes anything, it
[00:08:17:799 - 00:08:18:619] **Speaker 0:** passes it through.
[00:08:19:730 - 00:08:20:329] **Speaker 0:** Sorry, sorry.
[00:08:20:589 - 00:08:24:600] **Speaker 0:** Um high pass philtre passes through the high frequency input.
[00:08:25:019 - 00:08:29:799] **Speaker 0:** The low pass philtre passes the really low frequency DC.
[00:08:30:130 - 00:08:31:320] **Speaker 0:** So they both get passed through few through.
[00:08:34:780 - 00:08:37:859] **Speaker 0:** And then you know that V1 is then going to
[00:08:37:859 - 00:08:41:140] **Speaker 0:** be VN plus VCC over 2, because that's what high
[00:08:41:140 - 00:08:43:320] **Speaker 0:** pass philtre, see passes the VN through.
[00:08:43:979 - 00:08:46:280] **Speaker 0:** The low-pass philtre passes the V offset and you end
[00:08:46:280 - 00:08:46:789] **Speaker 0:** up with that.
[00:08:47:690 - 00:08:49:489] **Speaker 0:** And if you plug this into this equation, you can
[00:08:49:489 - 00:08:53:640] **Speaker 0:** see that um VO must be VN plus VCC over
[00:08:53:640 - 00:08:53:950] **Speaker 0:** 2.
[00:08:54:989 - 00:08:55:859] **Speaker 0:** Exactly the same.
[00:08:56:039 - 00:08:56:969] **Speaker 0:** Both are the same.
[00:08:57:940 - 00:09:00:440] **Speaker 0:** V1 equals V0, that's the mathematical proof.
[00:09:01:859 - 00:09:03:530] **Speaker 0:** And it's all got to choose the choices.
[00:09:03:580 - 00:09:05:619] **Speaker 0:** You really have to choose the capacitors to be the
[00:09:05:619 - 00:09:06:000] **Speaker 0:** same.
[00:09:06:950 - 00:09:10:070] **Speaker 0:** If the capacitors aren't chosen to be the same, doesn't
[00:09:10:070 - 00:09:10:469] **Speaker 0:** work.
[00:09:12:659 - 00:09:17:140] **Speaker 0:** So it's just a really clever way of Making the
[00:09:17:140 - 00:09:19:580] **Speaker 0:** filtering part of it to work for you.
[00:09:21:700 - 00:09:22:929] **Speaker 0:** And that's really all I had to say.
[00:09:27:099 - 00:09:29:150] **Speaker 0:** And I'll move on to lecture 16.
[00:09:33:940 - 00:09:36:950] **Speaker 0:** Draw a general philtre including all the main characteristics.
[00:09:37:039 - 00:09:39:869] **Speaker 0:** So yes, certainly, that is in the exam.
[00:09:55:859 - 00:09:58:820] **Speaker 0:** And it's page 3.
[00:09:59:179 - 00:10:00:419] **Speaker 0:** Page 3 is the one.
[00:10:01:580 - 00:10:02:409] **Speaker 0:** I'll get on there.
[00:10:05:650 - 00:10:11:030] **Speaker 0:** Cause, uh A lot of people still don't do this
[00:10:11:030 - 00:10:12:869] **Speaker 0:** right in the exam, even though I tell you exactly
[00:10:12:869 - 00:10:14:750] **Speaker 0:** what 40 you have to design, you have to have
[00:10:14:750 - 00:10:19:270] **Speaker 0:** like full um ripple and stuff, and people often forget
[00:10:19:270 - 00:10:20:900] **Speaker 0:** that, but I'll remind you when I get to that
[00:10:20:900 - 00:10:21:390] **Speaker 0:** slide.
[00:10:22:349 - 00:10:24:049] **Speaker 0:** I'll keep reminding you a few times.
[00:10:26:409 - 00:10:30:570] **Speaker 0:** Uh, the revised passive, well, that's not really, I wouldn't
[00:10:30:570 - 00:10:32:460] **Speaker 0:** say it's like preparatory.
[00:10:32:729 - 00:10:35:909] **Speaker 0:** Like it's Not really in the exam.
[00:10:37:729 - 00:10:39:580] **Speaker 0:** As such, but it's poetry.
[00:10:39:619 - 00:10:40:679] **Speaker 0:** It's like um.
[00:10:42:450 - 00:10:43:690] **Speaker 0:** Yeah, background.
[00:10:45:760 - 00:10:51:809] **Speaker 0:** Info Needed For exam but not exam itself.
[00:10:55:010 - 00:10:56:440] **Speaker 0:** analyse the four main philtre types.
[00:10:56:530 - 00:10:58:039] **Speaker 0:** Yes, you'll need to know.
[00:10:59:969 - 00:11:02:469] **Speaker 0:** What they are, how to draw them.
[00:11:03:729 - 00:11:05:330] **Speaker 0:** So that is certainly in the exam.
[00:11:06:890 - 00:11:08:830] **Speaker 0:** And there's only 4 combinations here.
[00:11:09:250 - 00:11:10:890] **Speaker 0:** And if I ask to draw a general philtre, I
[00:11:10:890 - 00:11:12:570] **Speaker 0:** kind of jump between these 3.
[00:11:13:020 - 00:11:16:250] **Speaker 0:** And so you need to better Answer that in the
[00:11:16:250 - 00:11:16:549] **Speaker 0:** exam.
[00:11:16:710 - 00:11:17:690] **Speaker 0:** So that's a learning outcome.
[00:11:20:190 - 00:11:21:599] **Speaker 0:** analyse 41234.
[00:11:24:739 - 00:11:27:719] **Speaker 0:** Start advantages of these 3 you'll hear that now you
[00:11:27:719 - 00:11:30:799] **Speaker 0:** have 33 different ones here, but these are obviously 4
[00:11:31:000 - 00:11:33:239] **Speaker 0:** you can have a Butterworth that has 4 different philtres
[00:11:33:239 - 00:11:34:200] **Speaker 0:** for the 1 Butterworth.
[00:11:35:369 - 00:11:37:969] **Speaker 0:** And, and there's another 4 for this and another 4
[00:11:37:969 - 00:11:38:250] **Speaker 0:** for that.
[00:11:38:330 - 00:11:40:869] **Speaker 0:** So there's actually 12 possible philtres here.
[00:11:41:409 - 00:11:41:849] **Speaker 0:** Good luck.
[00:11:45:510 - 00:11:48:429] **Speaker 0:** Uh, but once you've done one, once you've done a
[00:11:48:429 - 00:11:50:150] **Speaker 0:** low pass philtre, you've done them all, really.
[00:11:50:630 - 00:11:55:229] **Speaker 0:** It's just low pass philtres reversed and it's all, yeah.
[00:11:55:630 - 00:11:57:630] **Speaker 0:** So once you've cracked how to design a low pass
[00:11:57:630 - 00:11:59:570] **Speaker 0:** philtre, normally you can do a notch.
[00:12:00:409 - 00:12:02:530] **Speaker 0:** Uh, I suppose I better say you probably have to
[00:12:02:530 - 00:12:06:409] **Speaker 0:** high pass philtre maybe, uh, I could say these two
[00:12:06:619 - 00:12:09:450] **Speaker 0:** imply those two to be really, but I still reckon
[00:12:09:450 - 00:12:12:369] **Speaker 0:** low pass philtre is the once you've cracked that you've
[00:12:12:369 - 00:12:13:390] **Speaker 0:** cracked filtering.
[00:12:13:929 - 00:12:15:869] **Speaker 0:** If you know how to design a low pass philtre.
[00:12:16:750 - 00:12:20:030] **Speaker 0:** I would have reasonable confidence that you could design a
[00:12:20:030 - 00:12:20:789] **Speaker 0:** high pass philtre.
[00:12:22:909 - 00:12:25:049] **Speaker 0:** But it is a little bit of a conceptual leap
[00:12:25:049 - 00:12:27:349] **Speaker 0:** to learn what it is about filtering and how to
[00:12:27:349 - 00:12:29:109] **Speaker 0:** design a low post philtre, what it means, what you're
[00:12:29:109 - 00:12:31:090] **Speaker 0:** doing, how you're tuning the cutoff frequencies.
[00:12:32:380 - 00:12:35:130] **Speaker 0:** Yeah, there's definitely a conceptual jump there.
[00:12:35:549 - 00:12:37:640] **Speaker 0:** And then you start going to active philtres and then
[00:12:38:219 - 00:12:43:979] **Speaker 0:** Um So yeah, Butterworth, Sheyh and Bessel, you need to
[00:12:43:979 - 00:12:45:099] **Speaker 0:** be able to state the advantages.
[00:12:45:169 - 00:12:46:479] **Speaker 0:** So this is a learning outcome.
[00:12:47:609 - 00:12:49:869] **Speaker 0:** And it is often asked in the exam.
[00:12:50:909 - 00:12:51:929] **Speaker 0:** Advantages of them.
[00:12:54:260 - 00:12:55:419] **Speaker 0:** So that's enough on that.
[00:12:55:659 - 00:12:57:280] **Speaker 0:** Let's get on to lecture 16.
[00:12:57:929 - 00:13:00:539] **Speaker 0:** The final topic, so which is active philtres.
[00:13:02:940 - 00:13:07:729] **Speaker 0:** And I think it's very likely you'll be a lot
[00:13:07:729 - 00:13:09:219] **Speaker 0:** of you could make a design decision next year and
[00:13:09:219 - 00:13:11:219] **Speaker 0:** you're finding a project and you may end up going
[00:13:11:219 - 00:13:11:929] **Speaker 0:** for an active philtre.
[00:13:12:780 - 00:13:13:880] **Speaker 0:** They're really useful.
[00:13:17:030 - 00:13:20:969] **Speaker 0:** So important to, to learn different types and how it
[00:13:20:969 - 00:13:21:489] **Speaker 0:** works.
[00:13:24:549 - 00:13:28:450] **Speaker 0:** So, intro, uh I'm just gonna look at the basics
[00:13:28:989 - 00:13:33:080] **Speaker 0:** first before I get into How you actually use these
[00:13:33:080 - 00:13:33:919] **Speaker 0:** with op amps.
[00:13:37:409 - 00:13:42:960] **Speaker 0:** Um, So What I should probably note first, it does
[00:13:42:960 - 00:13:45:280] **Speaker 0:** seem fancy at the philtres is like it's.
[00:13:46:429 - 00:13:47:260] **Speaker 0:** 29.
[00:13:50:549 - 00:13:58:869] **Speaker 0:** But really There's nothing mathematically too much different from normal
[00:13:58:869 - 00:13:59:349] **Speaker 0:** filtering.
[00:14:02:159 - 00:14:07:549] **Speaker 0:** So typically based On LCR circuits, like what I hope
[00:14:07:549 - 00:14:09:570] **Speaker 0:** you've got reasonable familiarity with.
[00:14:23:289 - 00:14:24:510] **Speaker 0:** In the same way.
[00:14:30:270 - 00:14:32:710] **Speaker 0:** So I don't know if you did much of that
[00:14:32:710 - 00:14:34:590] **Speaker 0:** in the controls and the mechatronics.
[00:14:34:630 - 00:14:36:750] **Speaker 0:** I'm not sure if you did the filtering, but um.
[00:14:37:909 - 00:14:39:469] **Speaker 0:** And I did, I touched a little bit in my
[00:14:39:469 - 00:14:41:789] **Speaker 0:** controls, but you've probably hopefully have seen it somewhere in
[00:14:41:789 - 00:14:45:549] **Speaker 0:** your career, how to develop passive LCR philtres.
[00:14:46:409 - 00:14:50:260] **Speaker 0:** But I'm not, it's not guaranteed that everyone knows that.
[00:14:50:780 - 00:14:52:559] **Speaker 0:** So I am gonna do a little bit of a
[00:14:52:559 - 00:14:56:719] **Speaker 0:** revision in case you haven't, you're not absolutely sure what
[00:14:56:940 - 00:14:58:340] **Speaker 0:** LCR active filtering is.
[00:15:02:580 - 00:15:04:000] **Speaker 0:** And so let's start.
[00:15:05:190 - 00:15:05:890] **Speaker 0:** Basic definition.
[00:15:06:059 - 00:15:07:869] **Speaker 0:** So you just forget it for now as I'm going
[00:15:07:869 - 00:15:09:989] **Speaker 0:** through this, forget about this call with this fancy word
[00:15:09:989 - 00:15:10:609] **Speaker 0:** active.
[00:15:11:309 - 00:15:15:630] **Speaker 0:** I'm just teaching you the general knowledge behind LCR philtres.
[00:15:17:549 - 00:15:19:119] **Speaker 0:** So here's our basic definition.
[00:15:19:500 - 00:15:21:039] **Speaker 0:** We have an output transfer function.
[00:15:21:989 - 00:15:24:549] **Speaker 0:** We have our input and you put it through a
[00:15:24:549 - 00:15:25:030] **Speaker 0:** philtre.
[00:15:25:859 - 00:15:27:979] **Speaker 0:** And so a philtre could be some circuit and you
[00:15:27:979 - 00:15:30:940] **Speaker 0:** have an input into it and the output, it might
[00:15:30:940 - 00:15:33:659] **Speaker 0:** philtre a certain amount of noise in it in that
[00:15:33:659 - 00:15:34:460] **Speaker 0:** input signal.
[00:15:35:520 - 00:15:39:520] **Speaker 0:** And you can describe the magnitude change by the absolute
[00:15:39:520 - 00:15:40:510] **Speaker 0:** value of the transfer functions.
[00:15:40:640 - 00:15:42:359] **Speaker 0:** So remember putting S equal to j omega, all that
[00:15:42:359 - 00:15:43:460] **Speaker 0:** kind of stuff on controls.
[00:15:46:400 - 00:15:50:460] **Speaker 0:** The philtre attenuation function is uh is this in decibels.
[00:15:51:070 - 00:15:53:760] **Speaker 0:** It's 20 log 10 of of this, but it's always
[00:15:53:760 - 00:15:57:539] **Speaker 0:** done in terms of negative because you are attenuating it.
[00:15:58:340 - 00:16:00:440] **Speaker 0:** If you're amplifying a signal, then you would have the
[00:16:00:440 - 00:16:03:369] **Speaker 0:** positive, but we are attenuating filtering is all about attenuating
[00:16:04:260 - 00:16:05:869] **Speaker 0:** amplitudes of certain frequencies.
[00:16:07:359 - 00:16:09:450] **Speaker 0:** We have low past the 4 different.
[00:16:10:280 - 00:16:12:159] **Speaker 0:** Or notch.
[00:16:20:159 - 00:16:24:500] **Speaker 0:** This here, just an example, if I can fuel flosh
[00:16:24:500 - 00:16:28:400] **Speaker 0:** fuel fuel slosh, even in jet planes or maybe even
[00:16:28:400 - 00:16:31:940] **Speaker 0:** like a tanker that um Is like carrying milk with
[00:16:31:940 - 00:16:35:340] **Speaker 0:** Fonterra, they have to worry about um slosh and I
[00:16:35:340 - 00:16:36:900] **Speaker 0:** don't know if they have any active dampers, but I
[00:16:36:900 - 00:16:39:140] **Speaker 0:** think the fancy trucks could even have some sort of
[00:16:39:140 - 00:16:40:179] **Speaker 0:** active damping on it.
[00:16:40:859 - 00:16:43:479] **Speaker 0:** Um On springs and things.
[00:16:44:280 - 00:16:45:780] **Speaker 0:** There is really fancy methods now.
[00:16:47:500 - 00:16:51:099] **Speaker 0:** carrying fuel on a ship, there could be active damping
[00:16:51:099 - 00:16:52:750] **Speaker 0:** to keep the fuel from sloshing.
[00:16:53:599 - 00:16:56:429] **Speaker 0:** And in rockets, um, you may want to stop the
[00:16:56:429 - 00:16:58:400] **Speaker 0:** fuel from sloshing and you can do it with a
[00:16:58:400 - 00:16:58:900] **Speaker 0:** notch.
[00:16:59:960 - 00:17:04:520] **Speaker 0:** Cause these are kind of self-explanatory, um, you're knock you
[00:17:04:520 - 00:17:06:829] **Speaker 0:** basically just pass through the frequency you want, but this
[00:17:06:829 - 00:17:08:800] **Speaker 0:** one here you're knocking out a frequency you don't want.
[00:17:10:140 - 00:17:11:810] **Speaker 0:** Um, so let's just say.
[00:17:13:088 - 00:17:13:968] **Speaker 0:** AJ.
[00:17:15:790 - 00:17:16:930] **Speaker 0:** Removing.
[00:17:18:579 - 00:17:21:030] **Speaker 0:** Slash frequency.
[00:17:23:770 - 00:17:27:219] **Speaker 0:** In an orbital rocket launch, and I like rockets and
[00:17:27:219 - 00:17:27:530] **Speaker 0:** I.
[00:17:33:250 - 00:17:36:849] **Speaker 0:** Or maybe you just you're playing the guitar and you
[00:17:36:849 - 00:17:38:810] **Speaker 0:** plug it in and you hear this really annoying hum
[00:17:38:810 - 00:17:40:530] **Speaker 0:** when you're if you've got a band.
[00:17:41:260 - 00:17:43:250] **Speaker 0:** You know what that's like when you get the interference,
[00:17:43:339 - 00:17:46:650] **Speaker 0:** then that's, that's called mains hum that's sometimes a bit
[00:17:46:650 - 00:17:47:150] **Speaker 0:** of a problem.
[00:17:47:660 - 00:17:50:099] **Speaker 0:** So mains hum, you know it's a 50 hertz, so
[00:17:50:099 - 00:17:51:130] **Speaker 0:** you can actually knock this out.
[00:17:51:219 - 00:17:53:640] **Speaker 0:** I remember my one of my students actually did that,
[00:17:53:650 - 00:17:56:060] **Speaker 0:** but we made a notch philtre and we set it
[00:17:56:060 - 00:17:58:760] **Speaker 0:** to 50 Hz and actually completely knocked out that hum
[00:17:59:020 - 00:18:00:219] **Speaker 0:** that comes from the mains.
[00:18:01:209 - 00:18:03:869] **Speaker 0:** And that's, yeah, it's called a notch.
[00:18:04:819 - 00:18:06:199] **Speaker 0:** Or removing.
[00:18:09:199 - 00:18:12:040] **Speaker 0:** Mains hum or interference from the mains.
[00:18:14:760 - 00:18:17:000] **Speaker 0:** So it's a notch and of course, there's the applications
[00:18:17:000 - 00:18:17:939] **Speaker 0:** for these 3 as well.
[00:18:19:219 - 00:18:21:140] **Speaker 0:** But the notch may be one that you're not so
[00:18:21:140 - 00:18:21:839] **Speaker 0:** familiar with.
[00:18:24:810 - 00:18:26:930] **Speaker 0:** There's lots of applications for being able to get rid
[00:18:26:930 - 00:18:27:949] **Speaker 0:** of certain frequencies.
[00:18:32:589 - 00:18:33:829] **Speaker 0:** And here's what it looks like.
[00:18:36:270 - 00:18:37:839] **Speaker 0:** This is the amplitude.
[00:18:38:689 - 00:18:43:949] **Speaker 0:** Of your transfer function So you have a transfer function
[00:18:43:949 - 00:18:45:589] **Speaker 0:** like which is which is in the S domain, it
[00:18:45:589 - 00:18:49:550] **Speaker 0:** could be like I don't know E2 over I don't
[00:18:49:550 - 00:18:52:250] **Speaker 0:** know S + 1 S + 2.
[00:18:53:000 - 00:18:54:520] **Speaker 0:** Right, this is like a transfer function.
[00:18:54:880 - 00:18:55:579] **Speaker 0:** What does that mean?
[00:18:55:760 - 00:18:59:699] **Speaker 0:** The a transfer function describes how inputs go to outputs.
[00:19:00:500 - 00:19:02:619] **Speaker 0:** And so can you imagine that if you put an
[00:19:02:619 - 00:19:04:969] **Speaker 0:** input into this transfer function, which could be an LCR
[00:19:04:969 - 00:19:07:579] **Speaker 0:** circuit, the output could attenuate the amplitude.
[00:19:08:630 - 00:19:11:270] **Speaker 0:** That's what a philtre does, but it may have, if
[00:19:11:270 - 00:19:14:949] **Speaker 0:** it's got some higher-order zeros and poles, it may not
[00:19:14:949 - 00:19:17:349] **Speaker 0:** perfectly pass because it would be a low pass philtre.
[00:19:18:160 - 00:19:20:489] **Speaker 0:** You may find that for certain frequencies in your past
[00:19:20:489 - 00:19:23:579] **Speaker 0:** ban, the amplitude, the attenuation vary.
[00:19:24:579 - 00:19:27:000] **Speaker 0:** During the past ban, and this is called ripple.
[00:19:27:500 - 00:19:29:459] **Speaker 0:** So you get this this is annoying.
[00:19:29:500 - 00:19:31:500] **Speaker 0:** You don't want ripple because that means that you're getting
[00:19:31:500 - 00:19:34:030] **Speaker 0:** say 0 point to say this was 0.8 0.7.
[00:19:35:079 - 00:19:42:250] **Speaker 0:** Um Then you are attenuating 30% of your signal which
[00:19:42:250 - 00:19:43:479] **Speaker 0:** you don't, which is not great.
[00:19:44:339 - 00:19:45:920] **Speaker 0:** So this is, this is called ripple.
[00:19:47:040 - 00:19:51:900] **Speaker 0:** And specifically, it is called Pass being ripple.
[00:20:00:469 - 00:20:03:109] **Speaker 0:** And usually -3 dB.
[00:20:03:770 - 00:20:07:829] **Speaker 0:** And that's equivalent to 1 over route 2 signal reduction.
[00:20:12:770 - 00:20:15:170] **Speaker 0:** You can design philtres that have 1 dB.
[00:20:15:979 - 00:20:20:270] **Speaker 0:** And then, but 3DB is a really common kind of
[00:20:20:270 - 00:20:20:790] **Speaker 0:** value.
[00:20:22:050 - 00:20:24:089] **Speaker 0:** If you want to reduce ripple, it just requires higher
[00:20:24:089 - 00:20:24:829] **Speaker 0:** order filtering.
[00:20:27:319 - 00:20:30:199] **Speaker 0:** So yeah, study this figure and just know this really
[00:20:30:209 - 00:20:33:000] **Speaker 0:** really well because this is what I'm going to ask
[00:20:33:000 - 00:20:33:760] **Speaker 0:** in the exam.
[00:20:34:910 - 00:20:37:569] **Speaker 0:** So make a little note, big red mark somewhere.
[00:20:38:560 - 00:20:48:569] **Speaker 0:** That says And I'll just say here, know how to.
[00:20:49:540 - 00:20:50:939] **Speaker 0:** Reproduce.
[00:20:54:500 - 00:20:57:400] **Speaker 0:** This figure, 4.
[00:20:58:709 - 00:21:01:310] **Speaker 0:** Low pass, high pass.
[00:21:03:109 - 00:21:06:989] **Speaker 0:** Band pass and band stop or what I prefer is
[00:21:06:989 - 00:21:07:650] **Speaker 0:** a notch.
[00:21:12:540 - 00:21:14:260] **Speaker 0:** And this is obviously the case for a low pass
[00:21:14:260 - 00:21:14:619] **Speaker 0:** holder.
[00:21:16:750 - 00:21:18:430] **Speaker 0:** So let's just put a little heading here to say,
[00:21:18:439 - 00:21:20:260] **Speaker 0:** you know, this is the low pass water case.
[00:21:23:869 - 00:21:25:609] **Speaker 0:** High pass 40, you just like reverse it.
[00:21:26:689 - 00:21:28:930] **Speaker 0:** Band pass philtre you would like just continue this down
[00:21:28:930 - 00:21:29:949] **Speaker 0:** and you'd go up again.
[00:21:30:689 - 00:21:32:930] **Speaker 0:** And then you reverse reverse the beam pass folder for
[00:21:32:930 - 00:21:33:459] **Speaker 0:** the notch.
[00:21:33:930 - 00:21:36:300] **Speaker 0:** But I want to see you label the pass band,
[00:21:36:780 - 00:21:38:319] **Speaker 0:** like put arrows around the stop band.
[00:21:39:520 - 00:21:41:050] **Speaker 0:** Uh, show a transition ban.
[00:21:41:170 - 00:21:42:949] **Speaker 0:** I'm probably not gonna worry too much about.
[00:21:44:189 - 00:21:47:709] **Speaker 0:** These Um, as long as you did, if you show
[00:21:47:709 - 00:21:49:939] **Speaker 0:** the transition band the stop band, and this AMin is
[00:21:49:939 - 00:21:52:420] **Speaker 0:** important because it's telling you how much you're attenuating and
[00:21:52:420 - 00:21:54:449] **Speaker 0:** IMAX is important because it's the pass and ripple.
[00:21:55:689 - 00:21:57:099] **Speaker 0:** But if you really want to, you could put these
[00:21:57:099 - 00:21:57:760] **Speaker 0:** in as well.
[00:22:10:050 - 00:22:11:750] **Speaker 0:** Let's just say these are optional.
[00:22:14:930 - 00:22:16:420] **Speaker 0:** But if you want to impress me, then put him
[00:22:16:420 - 00:22:16:640] **Speaker 0:** in.
[00:22:21:890 - 00:22:26:219] **Speaker 0:** This is Optional for.
[00:22:27:650 - 00:22:29:089] **Speaker 0:** Um, exam.
[00:22:35:349 - 00:22:35:829] **Speaker 0:** So yeah.
[00:22:37:449 - 00:22:39:530] **Speaker 0:** It's pretty much free marks, but it's forcing you to
[00:22:39:530 - 00:22:39:910] **Speaker 0:** learn it.
[00:22:40:680 - 00:22:41:890] **Speaker 0:** Which is my grand scheme.
[00:22:50:140 - 00:22:52:650] **Speaker 0:** I'm a firm believer in in memorising, I think memorising
[00:22:52:650 - 00:22:54:449] **Speaker 0:** is an important thing to do as an engineer.
[00:22:54:790 - 00:22:56:949] **Speaker 0:** I think it's good to have something accessible in the
[00:22:56:949 - 00:22:59:689] **Speaker 0:** brain, then you can immediately go to it.
[00:23:01:099 - 00:23:03:300] **Speaker 0:** That's one thing that exams are good for, even though
[00:23:03:300 - 00:23:05:569] **Speaker 0:** I wouldn't recommend completely relying on memorising.
[00:23:06:729 - 00:23:10:270] **Speaker 0:** Uh, you need some understanding as well, of course.
[00:23:15:750 - 00:23:17:449] **Speaker 0:** That's the minimum stop being frequency.
[00:23:17:949 - 00:23:20:150] **Speaker 0:** So yeah, that's everything you need to know really there
[00:23:20:150 - 00:23:22:089] **Speaker 0:** on what a philtre looks like.
[00:23:27:150 - 00:23:28:390] **Speaker 0:** It's all the different features.
[00:23:29:270 - 00:23:31:589] **Speaker 0:** So if you if you can if your transition band
[00:23:31:589 - 00:23:34:150] **Speaker 0:** was really long, can you see it's gonna create a
[00:23:34:150 - 00:23:34:689] **Speaker 0:** problem?
[00:23:35:660 - 00:23:37:619] **Speaker 0:** Because you'll be passing frequencies, but that means you're not
[00:23:37:619 - 00:23:39:459] **Speaker 0:** gonna be attenuating the high ones as well.
[00:23:39:819 - 00:23:41:619] **Speaker 0:** There'll be a whole heap of frequencies that are still
[00:23:41:619 - 00:23:42:359] **Speaker 0:** getting through.
[00:23:42:939 - 00:23:45:739] **Speaker 0:** But then if you made this really short and it's
[00:23:45:739 - 00:23:48:780] **Speaker 0:** like snapped right at the end, then you're gonna be
[00:23:48:780 - 00:23:50:280] **Speaker 0:** cutting it off beautifully, right?
[00:23:51:750 - 00:23:53:500] **Speaker 0:** And that's just an example of one of the features
[00:23:53:500 - 00:23:54:530] **Speaker 0:** that you designed for.
[00:23:57:459 - 00:23:59:239] **Speaker 0:** And there's always like a trade-off.
[00:23:59:790 - 00:24:03:270] **Speaker 0:** If you want to have a really fast or small
[00:24:03:270 - 00:24:05:640] **Speaker 0:** transition then you end up with a higher ripple.
[00:24:06:069 - 00:24:07:579] **Speaker 0:** If you wanna have, you can have the ripple be
[00:24:07:579 - 00:24:08:150] **Speaker 0:** less.
[00:24:08:630 - 00:24:11:329] **Speaker 0:** You don't get a free lunch unfortunately, unfortunately in engineering.
[00:24:11:829 - 00:24:13:790] **Speaker 0:** There's no free lunch when it comes, there's no perfect
[00:24:13:790 - 00:24:14:150] **Speaker 0:** philtre.
[00:24:14:959 - 00:24:16:390] **Speaker 0:** No one's been able to come up with a perfect
[00:24:16:390 - 00:24:16:890] **Speaker 0:** philtre yet.
[00:24:18:189 - 00:24:19:400] **Speaker 0:** If you did, you'd be a billionaire.
[00:24:27:140 - 00:24:30:380] **Speaker 0:** Just so many devices, electronic devices, and all of our
[00:24:30:380 - 00:24:31:880] **Speaker 0:** technology is based on filtering.
[00:24:40:349 - 00:24:43:209] **Speaker 0:** So, I'm going to Continue my revision.
[00:24:46:390 - 00:24:48:329] **Speaker 0:** Here is a 5th order low-pass philtre.
[00:24:50:219 - 00:24:52:750] **Speaker 0:** And if you plot this, it would look a little
[00:24:52:750 - 00:24:53:550] **Speaker 0:** bit similar to this.
[00:24:53:589 - 00:24:56:099] **Speaker 0:** You'll probably find that um I think either one of
[00:24:56:099 - 00:24:57:219] **Speaker 0:** these sides is flat.
[00:24:57:670 - 00:24:59:550] **Speaker 0:** You're not necessarily get ripple on both of these.
[00:24:59:630 - 00:25:01:239] **Speaker 0:** You could this could be just like coming down like
[00:25:01:239 - 00:25:03:550] **Speaker 0:** that, or that could be flat, and then this could
[00:25:03:550 - 00:25:03:930] **Speaker 0:** be.
[00:25:04:420 - 00:25:05:609] **Speaker 0:** There's all sorts of combinations.
[00:25:05:910 - 00:25:09:020] **Speaker 0:** But that's the general one that I want to see
[00:25:09:020 - 00:25:09:670] **Speaker 0:** in the exam.
[00:25:14:219 - 00:25:16:030] **Speaker 0:** So what have we got, 5 poles.
[00:25:27:310 - 00:25:31:030] **Speaker 0:** There's a really strong um sort of link or or
[00:25:31:030 - 00:25:34:010] **Speaker 0:** overlap between philtre design and control design.
[00:25:36:140 - 00:25:38:979] **Speaker 0:** But the same techniques for pole placement can work for
[00:25:38:979 - 00:25:39:300] **Speaker 0:** philtre.
[00:25:40:069 - 00:25:41:030] **Speaker 0:** And vice versa.
[00:25:46:520 - 00:25:52:290] **Speaker 0:** I first order zeros, they're not, they're, um, Oh yeah,
[00:25:52:380 - 00:25:53:859] **Speaker 0:** I suppose they are, but I'll just say how many
[00:25:53:859 - 00:25:54:599] **Speaker 0:** zeros there are.
[00:25:55:650 - 00:26:02:839] **Speaker 0:** I was just like Plus or minus 4 J plus
[00:26:02:839 - 00:26:04:270] **Speaker 0:** or minus 6 J.
[00:26:05:979 - 00:26:08:430] **Speaker 0:** And a transfer function.
[00:26:09:550 - 00:26:30:380] **Speaker 0:** Is Yes So you've got an order 5 pollen name
[00:26:30:380 - 00:26:32:329] **Speaker 0:** on the bottom and an order 4 on the top.
[00:26:33:079 - 00:26:34:910] **Speaker 0:** That is a low pass fun there's a low pass
[00:26:34:910 - 00:26:35:290] **Speaker 0:** philtre.
[00:26:36:760 - 00:26:39:800] **Speaker 0:** To realise that in the real world would require a
[00:26:39:800 - 00:26:44:589] **Speaker 0:** reasonably sophisticated circuit with a bunch of inductors and capacitors
[00:26:44:589 - 00:26:45:280] **Speaker 0:** and resistors.
[00:26:52:290 - 00:26:54:030] **Speaker 0:** This has got a name, this one.
[00:26:55:760 - 00:26:59:719] **Speaker 0:** It's called the Shibi shiv philtre.
[00:27:00:719 - 00:27:01:890] **Speaker 0:** Type 2.
[00:27:03:989 - 00:27:08:239] **Speaker 0:** Type 2 has a flat pass band and has ripple
[00:27:08:239 - 00:27:09:150] **Speaker 0:** in the stop band.
[00:27:10:689 - 00:27:11:209] **Speaker 0:** Like that.
[00:27:14:979 - 00:27:17:369] **Speaker 0:** Footer order in, poles and natural modes.
[00:27:18:810 - 00:27:21:119] **Speaker 0:** You have this concept called selectivity.
[00:27:25:390 - 00:27:31:589] **Speaker 0:** What happens is The stop being frequency and the past
[00:27:31:589 - 00:27:34:010] **Speaker 0:** being frequency come together.
[00:27:35:930 - 00:27:38:270] **Speaker 0:** And that implies that the transition.
[00:27:39:369 - 00:27:41:599] **Speaker 0:** Band decreases.
[00:27:44:510 - 00:27:48:380] **Speaker 0:** But then higher order philtres can create problems with extra
[00:27:48:959 - 00:27:50:000] **Speaker 0:** noise in your circuit.
[00:27:51:420 - 00:27:54:170] **Speaker 0:** And then there's another obvious theoretical problem which is the
[00:27:54:170 - 00:27:57:099] **Speaker 0:** greater your philtre order is, the more the phase lag.
[00:27:57:849 - 00:27:59:469] **Speaker 0:** So you have to throw those off.
[00:28:03:750 - 00:28:06:250] **Speaker 0:** All right, let's continue my revision of philtres.
[00:28:07:859 - 00:28:09:800] **Speaker 0:** Before I even get onto active philtres.
[00:28:11:180 - 00:28:12:479] **Speaker 0:** 1st and 2nd order philtres.
[00:28:17:530 - 00:28:19:670] **Speaker 0:** So we have our low pass philtre here.
[00:28:22:530 - 00:28:24:780] **Speaker 0:** And the way a low pass photo works is it.
[00:28:25:550 - 00:28:28:010] **Speaker 0:** Gives you attenuation.
[00:28:30:050 - 00:28:31:709] **Speaker 0:** At the high frequencies.
[00:28:38:869 - 00:28:40:910] **Speaker 0:** If it was a perfect low pass foot, it was
[00:28:40:910 - 00:28:43:680] **Speaker 0:** just passing, would have a unity effect on the pass
[00:28:43:680 - 00:28:46:439] **Speaker 0:** band, but you'd normally say in general that it has
[00:28:46:439 - 00:28:47:699] **Speaker 0:** a finite gain.
[00:28:49:510 - 00:28:52:310] **Speaker 0:** At low Frequency.
[00:28:57:030 - 00:28:59:079] **Speaker 0:** And now the only thing that's new here, which you're
[00:28:59:079 - 00:29:01:800] **Speaker 0:** not used to, I mean, up to here, I would
[00:29:01:800 - 00:29:03:660] **Speaker 0:** hope that you have some experience.
[00:29:05:849 - 00:29:07:910] **Speaker 0:** But that is what you probably haven't seen before.
[00:29:10:010 - 00:29:13:670] **Speaker 0:** And so we have a passive, everything, everything mathematically is
[00:29:13:670 - 00:29:14:170] **Speaker 0:** all the same.
[00:29:14:250 - 00:29:14:469] **Speaker 0:** Yep.
[00:29:15:020 - 00:29:15:050] **Speaker 0:** So.
[00:29:20:089 - 00:29:23:520] **Speaker 0:** Yep, yep, it's just Gayiners was was the A naught.
[00:29:25:119 - 00:29:28:000] **Speaker 0:** If you were doing an amplification at the same time
[00:29:28:000 - 00:29:29:020] **Speaker 0:** as the filtering.
[00:29:31:839 - 00:29:34:119] **Speaker 1:** philtre and then now it's an active.
[00:29:35:560 - 00:29:39:430] **Speaker 1:** Is the game Is it R21 or is it?
[00:29:40:670 - 00:29:43:180] **Speaker 0:** Yes, it's, it's, it's precisely R2 over R1.
[00:29:46:160 - 00:29:46:339] **Speaker 0:** Yeah.
[00:29:46:420 - 00:29:49:310] **Speaker 0:** Hey, so just for this particular case, I might just
[00:29:49:369 - 00:29:50:939] **Speaker 0:** just let me analyse this for a minute.
[00:29:51:069 - 00:29:52:239] **Speaker 0:** Hopefully that'll come clear.
[00:29:53:069 - 00:29:54:800] **Speaker 0:** Because I think it's a good idea to just see
[00:29:54:800 - 00:29:55:410] **Speaker 0:** this once.
[00:30:03:680 - 00:30:09:729] **Speaker 0:** So we have our eye We have I one.
[00:30:11:380 - 00:30:12:859] **Speaker 0:** We have I 2.
[00:30:16:900 - 00:30:21:130] **Speaker 0:** And so obviously I is I1 plus I2.
[00:30:25:109 - 00:30:27:890] **Speaker 0:** The output Just as.
[00:30:28:819 - 00:30:29:599] **Speaker 0:** And to use some.
[00:30:30:880 - 00:30:33:599] **Speaker 0:** Some terminology here in case you haven't got used to
[00:30:33:599 - 00:30:35:260] **Speaker 0:** the dot form, dot notation.
[00:30:43:959 - 00:30:45:459] **Speaker 0:** So the input is going to be.
[00:30:50:599 - 00:30:53:650] **Speaker 0:** Curn I 1 plus current I 2.
[00:30:58:050 - 00:31:00:119] **Speaker 0:** And I've got that dot notation for the derivative.
[00:31:03:250 - 00:31:05:010] **Speaker 0:** And so if you want to do the Laplace transform
[00:31:05:010 - 00:31:05:469] **Speaker 0:** of that.
[00:31:07:229 - 00:31:11:630] **Speaker 0:** Then it'll answer your question, which is, You end up
[00:31:11:630 - 00:31:13:189] **Speaker 0:** with the ratio of the resistance.
[00:31:14:780 - 00:31:16:439] **Speaker 0:** Times one over.
[00:31:19:290 - 00:31:20:500] **Speaker 0:** The time constant.
[00:31:23:010 - 00:31:25:369] **Speaker 0:** Um, I wanna say.
[00:31:30:550 - 00:31:31:479] **Speaker 0:** Uh, 2 Cs, sorry.
[00:31:36:089 - 00:31:39:459] **Speaker 0:** I said I'm only gonna do this once, but I
[00:31:39:459 - 00:31:42:010] **Speaker 0:** what I've done here is I've I've derived the transfer
[00:31:42:010 - 00:31:44:699] **Speaker 0:** function from this op amp circuit.
[00:31:45:839 - 00:31:47:430] **Speaker 0:** And look at it, it's a low pass philtre.
[00:31:48:000 - 00:31:48:959] **Speaker 0:** And there's the game.
[00:31:51:170 - 00:31:53:069] **Speaker 0:** So choose your resistances wisely.
[00:31:54:050 - 00:31:54:969] **Speaker 0:** Depending on what gain.
[00:31:55:050 - 00:31:57:369] **Speaker 0:** If you wanted the gain to be 1, choose R2
[00:31:57:369 - 00:31:58:050] **Speaker 0:** to be 01.
[00:31:58:469 - 00:31:59:810] **Speaker 0:** Choose them both to be kiloome or something.
[00:32:00:540 - 00:32:01:800] **Speaker 0:** And you got yourself a low pass order.
[00:32:02:829 - 00:32:07:709] **Speaker 0:** Using an active formulation using op amps, OP amps have
[00:32:07:709 - 00:32:10:550] **Speaker 0:** got a major advantage because they can buffer against loads
[00:32:10:550 - 00:32:13:150] **Speaker 0:** like a passive philtre can change depending on the load.
[00:32:13:199 - 00:32:14:089] **Speaker 0:** It's a real pain.
[00:32:14:890 - 00:32:16:349] **Speaker 0:** It can change because of temperature.
[00:32:16:479 - 00:32:19:290] **Speaker 0:** There's many factors that can affect a passive philtre, which
[00:32:19:290 - 00:32:20:829] **Speaker 0:** is why we want to use active philtres.
[00:32:23:000 - 00:32:24:780] **Speaker 0:** So I think that's, that's just the one example.
[00:32:24:920 - 00:32:26:400] **Speaker 0:** If you really want to, you could go through and
[00:32:26:400 - 00:32:28:199] **Speaker 0:** you could derive it for all of these, but I
[00:32:28:199 - 00:32:28:699] **Speaker 0:** don't want to.
[00:32:29:880 - 00:32:31:369] **Speaker 0:** Um, because it's not going to be.
[00:32:31:640 - 00:32:33:119] **Speaker 0:** I'm not going to be asking you to drive that
[00:32:33:119 - 00:32:33:719] **Speaker 0:** in an exam.
[00:32:36:420 - 00:32:40:540] **Speaker 0:** There's one very specific realisation that I ask in the
[00:32:40:540 - 00:32:42:439] **Speaker 0:** exam every year.
[00:32:42:859 - 00:32:43:739] **Speaker 0:** Question number 3.
[00:32:50:520 - 00:32:52:439] **Speaker 0:** I have to do it that way because it can
[00:32:52:439 - 00:32:54:500] **Speaker 0:** get so it could get so complex it would just,
[00:32:54:630 - 00:32:56:160] **Speaker 0:** you wouldn't better do it in the 2 hours so.
[00:32:57:229 - 00:33:03:180] **Speaker 0:** Uh, I, I, I can't really change the exam too
[00:33:03:180 - 00:33:05:300] **Speaker 0:** much from year to year because I can otherwise everyone
[00:33:05:300 - 00:33:05:760] **Speaker 0:** would fail.
[00:33:08:530 - 00:33:11:199] **Speaker 0:** If I ask some 4th order active philtre or something,
[00:33:11:209 - 00:33:14:729] **Speaker 0:** realisation when you see the the realisation for the higher
[00:33:14:729 - 00:33:18:170] **Speaker 0:** order philtres, you'll know it's like an absolute very complex
[00:33:18:170 - 00:33:18:670] **Speaker 0:** beast.
[00:33:20:349 - 00:33:22:469] **Speaker 0:** It would be a nightmare to do that in the
[00:33:22:469 - 00:33:22:930] **Speaker 0:** exam.
[00:33:24:260 - 00:33:25:719] **Speaker 0:** Uh, so, yeah.
[00:33:26:640 - 00:33:27:359] **Speaker 0:** That's enough on that.
[00:33:27:479 - 00:33:33:160] **Speaker 0:** Um, I'm still doing my Kind of review or kinda.
[00:33:35:030 - 00:33:37:630] **Speaker 0:** Maybe it isn't maybe it isn't a revision, but if
[00:33:37:630 - 00:33:40:349] **Speaker 0:** you haven't seen this before, then maybe you can build
[00:33:40:349 - 00:33:41:910] **Speaker 0:** a little bit more work to come up to speed
[00:33:41:910 - 00:33:44:030] **Speaker 0:** with um static philtres.
[00:33:47:540 - 00:33:50:300] **Speaker 0:** And this should give you a good guide to everything
[00:33:50:300 - 00:33:52:199] **Speaker 0:** you need to know for my particular exam.
[00:33:59:599 - 00:34:02:079] **Speaker 0:** So this is sort of a crash course course in
[00:34:02:079 - 00:34:05:439] **Speaker 0:** um philtre philtre design and the properties.
[00:34:09:979 - 00:34:09:989] **Speaker 0:** Now.
[00:34:12:769 - 00:34:17:168] **Speaker 0:** This particular formalisation, if you would have done in the
[00:34:17:168 - 00:34:18:009] **Speaker 0:** control systems.
[00:34:19:479 - 00:34:21:388] **Speaker 0:** The old good old Zy and Amy Green.
[00:34:21:989 - 00:34:23:499] **Speaker 0:** I'll call it running a naught in this case.
[00:34:29:178 - 00:34:30:357] **Speaker 0:** In philtre design.
[00:34:32:648 - 00:34:36:570] **Speaker 0:** You write, you set 2 zi to be 1 over
[00:34:36:570 - 00:34:36:800] **Speaker 0:** q.
[00:34:39:780 - 00:34:44:810] **Speaker 0:** And instead of having a zy parameter, You have 1
[00:34:44:810 - 00:34:45:620] **Speaker 0:** over 2Q.
[00:34:46:138 - 00:34:47:429] **Speaker 0:** So it's called a Q factor.
[00:34:50:469 - 00:34:54:100] **Speaker 0:** So the What actually one I so one.
[00:34:56:280 - 00:35:01:780] **Speaker 0:** 1 over Q Is the bandwidth.
[00:35:03:919 - 00:35:05:179] **Speaker 0:** For a vain pass photo.
[00:35:07:989 - 00:35:10:989] **Speaker 0:** So you can develop an intuition on, on what your
[00:35:10:989 - 00:35:12:979] **Speaker 0:** bandwidth is using this number where you've got it I
[00:35:12:979 - 00:35:15:300] **Speaker 0:** know I've taught you since the class and electrical.
[00:35:15:310 - 00:35:17:679] **Speaker 0:** I taught you like what an intuition on what Za
[00:35:17:679 - 00:35:21:350] **Speaker 0:** does for control systems for filtering it to reprogram your
[00:35:21:350 - 00:35:23:070] **Speaker 0:** brain and you're going to think about the Q factor.
[00:35:23:929 - 00:35:24:850] **Speaker 0:** When you're doing filtering.
[00:35:26:149 - 00:35:27:489] **Speaker 0:** But the two are equivalent.
[00:35:27:949 - 00:35:29:389] **Speaker 0:** If you want to just be a mathematician and just
[00:35:29:389 - 00:35:31:870] **Speaker 0:** analyse this mathematically, you can see, well, i is just
[00:35:31:870 - 00:35:32:629] **Speaker 0:** 1/2 q.
[00:35:34:360 - 00:35:36:199] **Speaker 0:** And za gives you the bump on the curve.
[00:35:36:280 - 00:35:38:399] **Speaker 0:** You remember doing the old bodies and the the zai
[00:35:38:399 - 00:35:39:719] **Speaker 0:** was really, really small, you know, you get the big
[00:35:39:719 - 00:35:41:419] **Speaker 0:** bump that comes down and goes down like this.
[00:35:42:209 - 00:35:47:879] **Speaker 0:** Um, But that would govern philtre design as well in
[00:35:47:879 - 00:35:48:669] **Speaker 0:** terms of the bandwidth.
[00:35:49:750 - 00:35:51:129] **Speaker 0:** And here's a lighthouse photo.
[00:35:52:459 - 00:35:54:239] **Speaker 0:** And we have a high pass folder.
[00:35:56:209 - 00:35:58:580] **Speaker 0:** So low par 2nd order, you always have like the
[00:35:58:580 - 00:35:59:439] **Speaker 0:** S 2 on the bottom.
[00:36:00:669 - 00:36:02:489] **Speaker 0:** And the sai is going to govern this.
[00:36:05:060 - 00:36:06:500] **Speaker 0:** And then with a high pass 40, you've got an
[00:36:06:500 - 00:36:07:179] **Speaker 0:** E squad here.
[00:36:09:199 - 00:36:11:189] **Speaker 0:** And you get this, um, this, this would be called
[00:36:11:189 - 00:36:11:739] **Speaker 0:** a ripple.
[00:36:12:590 - 00:36:13:199] **Speaker 0:** That the.
[00:36:14:219 - 00:36:15:679] **Speaker 0:** It's an example of ripple.
[00:36:20:040 - 00:36:20:050] **Speaker 0:** Yeah.
[00:36:28:439 - 00:36:29:270] **Speaker 0:** Excellent.
[00:36:29:560 - 00:36:30:580] **Speaker 0:** You're really onto it.
[00:36:31:379 - 00:36:33:040] **Speaker 0:** Hi, I'm glad you picked that up.
[00:36:34:030 - 00:36:39:229] **Speaker 0:** Um Because the Butterworth philtre, maybe because you already knew
[00:36:39:229 - 00:36:40:530] **Speaker 0:** what a Butterworth philtre is.
[00:36:42:290 - 00:36:43:010] **Speaker 0:** Uh.
[00:36:48:090 - 00:36:50:439] **Speaker 0:** I think he was an engineer, mathematician, maybe a mathematician,
[00:36:50:449 - 00:36:53:030] **Speaker 0:** and he like realised exactly what you said.
[00:36:53:770 - 00:36:56:270] **Speaker 0:** That if you make queue 1 over route 2.
[00:36:57:750 - 00:36:58:590] **Speaker 0:** It's like flat.
[00:36:58:709 - 00:36:59:870] **Speaker 0:** You don't get any little bump.
[00:37:00:669 - 00:37:01:909] **Speaker 0:** So it's a flat philtre.
[00:37:02:310 - 00:37:05:189] **Speaker 0:** So it is one of the most commonly used philtres
[00:37:05:189 - 00:37:05:949] **Speaker 0:** for that reason.
[00:37:07:040 - 00:37:09:159] **Speaker 0:** That is a really nice philtre because you don't get
[00:37:09:159 - 00:37:10:919] **Speaker 0:** any ripple, which is great.
[00:37:14:360 - 00:37:15:439] **Speaker 0:** So yeah, very good point.
[00:37:16:419 - 00:37:17:439] **Speaker 0:** 10 out of 10 for that.
[00:37:26:729 - 00:37:28:570] **Speaker 0:** So band pass.
[00:37:29:429 - 00:37:31:520] **Speaker 0:** This is again this is sort of just revision, it's
[00:37:31:520 - 00:37:33:600] **Speaker 0:** just showing you the different types of philtres for 2nd
[00:37:33:600 - 00:37:33:959] **Speaker 0:** order.
[00:37:34:320 - 00:37:35:820] **Speaker 0:** I showed them this for the 1st order.
[00:37:37:280 - 00:37:41:239] **Speaker 0:** And all of these have got meaning.
[00:37:42:830 - 00:37:43:570] **Speaker 0:** I'm gonna know it.
[00:37:45:510 - 00:37:46:860] **Speaker 0:** As the essential frequency.
[00:37:48:709 - 00:37:50:229] **Speaker 0:** And then you've got this distance here.
[00:37:51:439 - 00:37:53:679] **Speaker 0:** When I see it's 1 over q is actually normalised
[00:37:53:679 - 00:37:54:320] **Speaker 0:** to the frequency.
[00:37:54:399 - 00:37:56:219] **Speaker 0:** That's for a normalised frequency of 1.
[00:37:57:100 - 00:38:00:340] **Speaker 0:** Um, but yeah, it's naught over q is the distance
[00:38:00:340 - 00:38:01:149] **Speaker 0:** of the bandwidth.
[00:38:03:939 - 00:38:06:699] **Speaker 0:** But you'll find out later that when I teach you
[00:38:06:699 - 00:38:08:979] **Speaker 0:** how to do filtering, and in terms of each of
[00:38:08:979 - 00:38:10:600] **Speaker 0:** the different types of philtre.
[00:38:11:379 - 00:38:14:620] **Speaker 0:** You always assume the cutoff frequency is at one.
[00:38:15:550 - 00:38:17:770] **Speaker 0:** And that's basically saying that it's normalised.
[00:38:18:389 - 00:38:20:590] **Speaker 0:** And so a lot of the calculations are done assuming
[00:38:20:590 - 00:38:22:169] **Speaker 0:** the cutoff frequency is one.
[00:38:23:909 - 00:38:26:389] **Speaker 0:** And that means that you can then scale it out
[00:38:26:389 - 00:38:27:449] **Speaker 0:** to any frequency you want.
[00:38:28:310 - 00:38:30:699] **Speaker 0:** So you give all the coefficients you like a cool
[00:38:30:699 - 00:38:33:110] **Speaker 0:** Chevychev type one would have a whole lot of different
[00:38:33:110 - 00:38:34:050] **Speaker 0:** coefficients.
[00:38:35:010 - 00:38:38:300] **Speaker 0:** And you would know the shape of the curve where
[00:38:38:300 - 00:38:40:209] **Speaker 0:** you normalise the cutoff frequency to be one.
[00:38:40:620 - 00:38:42:419] **Speaker 0:** But then you obviously want to design it for like
[00:38:42:419 - 00:38:45:479] **Speaker 0:** higher frequency, so you'd take that normalised philtre.
[00:38:46:209 - 00:38:50:850] **Speaker 0:** Um, shape, and you would transform it out to higher
[00:38:50:850 - 00:38:51:250] **Speaker 0:** frequencies.
[00:38:51:330 - 00:38:53:939] **Speaker 0:** But don't worry, I'll give you lots of examples on
[00:38:53:939 - 00:38:56:649] **Speaker 0:** learning during lecture notes and on that.
[00:38:59:489 - 00:39:01:669] **Speaker 0:** I've still got a little bit more to go.
[00:39:02:969 - 00:39:05:149] **Speaker 0:** On this uh revision exercise.
[00:39:09:820 - 00:39:11:209] **Speaker 0:** So passive LCR.
[00:39:14:350 - 00:39:17:129] **Speaker 0:** This is how you can generally do it.
[00:39:20:189 - 00:39:21:500] **Speaker 0:** And it's, yeah, quite a handy.
[00:39:21:629 - 00:39:26:149] **Speaker 0:** Again, this is possibly revision but uh I'm going to
[00:39:26:149 - 00:39:29:030] **Speaker 0:** show you how you can do this for a low
[00:39:29:030 - 00:39:29:520] **Speaker 0:** pass.
[00:39:32:520 - 00:39:42:949] **Speaker 0:** First, So, let's just So you can do everything in
[00:39:42:949 - 00:39:43:889] **Speaker 0:** the yes domain.
[00:39:49:120 - 00:39:52:280] **Speaker 0:** And then you can just match up whatever um.
[00:39:53:370 - 00:39:54:800] **Speaker 0:** Z1 and Z2 are going to be.
[00:39:56:409 - 00:39:58:949] **Speaker 0:** And it makes it nice and easy to generalise.
[00:40:12:489 - 00:40:15:040] **Speaker 0:** So you got your input, you're going into a standard
[00:40:15:040 - 00:40:17:189] **Speaker 0:** LCR with the capacitor and resistor.
[00:40:17:919 - 00:40:19:989] **Speaker 0:** You should be familiar, where have you seen this before?
[00:40:24:060 - 00:40:25:110] **Speaker 0:** Have you seen it in the scores?
[00:40:25:310 - 00:40:25:639] **Speaker 0:** What?
[00:40:26:330 - 00:40:28:510] **Speaker 0:** Buck converter, this so this is a great example.
[00:40:28:909 - 00:40:30:989] **Speaker 0:** So a buck converter is actually just a low pass
[00:40:30:989 - 00:40:31:389] **Speaker 0:** philtre.
[00:40:32:840 - 00:40:34:629] **Speaker 0:** And if you want to look like that, I mean,
[00:40:34:729 - 00:40:36:370] **Speaker 0:** obviously it does a lot more and enables you to
[00:40:36:370 - 00:40:36:969] **Speaker 0:** step down the voltage.
[00:40:37:040 - 00:40:40:110] **Speaker 0:** It's great because you're using the, but it's the switching
[00:40:40:889 - 00:40:44:530] **Speaker 0:** that's really this part is purely a low pass philtre
[00:40:44:530 - 00:40:45:169] **Speaker 0:** in the back converter.
[00:40:45:250 - 00:40:48:290] **Speaker 0:** It's the switch that does the magic for changing the
[00:40:48:290 - 00:40:48:830] **Speaker 0:** voltage.
[00:40:49:939 - 00:40:52:379] **Speaker 0:** So it's an LCR circuit that's doing all the getting
[00:40:52:379 - 00:40:54:580] **Speaker 0:** rid of all those transients that are caused by the
[00:40:54:580 - 00:40:57:340] **Speaker 0:** fast switching of the moss fat which enables you to
[00:40:57:340 - 00:40:59:860] **Speaker 0:** do really cool stuff with it like drive it have
[00:40:59:860 - 00:41:00:780] **Speaker 0:** a solar car.
[00:41:01:760 - 00:41:04:360] **Speaker 0:** You know, like changing, putting, putting your foot on the
[00:41:04:360 - 00:41:06:370] **Speaker 0:** accelerator and making it going or taking your foot off
[00:41:06:370 - 00:41:07:050] **Speaker 0:** the accelerator.
[00:41:08:449 - 00:41:09:469] **Speaker 0:** And everything in between.
[00:41:11:100 - 00:41:13:969] **Speaker 0:** So I mean like philtres are just so everywhere.
[00:41:15:429 - 00:41:16:639] **Speaker 0:** Across electronics.
[00:41:19:919 - 00:41:22:350] **Speaker 0:** So let's just see what Z2 is going to be.
[00:41:24:110 - 00:41:26:199] **Speaker 0:** Z2 is going to be.
[00:41:28:010 - 00:41:29:510] **Speaker 0:** A parallel connection.
[00:41:31:399 - 00:41:34:439] **Speaker 0:** Which then gives you that for the impedances.
[00:41:40:520 - 00:41:43:760] **Speaker 0:** I think this was taught in, maybe 2nd year.
[00:41:44:570 - 00:41:46:389] **Speaker 0:** Actually I'm pretty sure this used to be taught in
[00:41:46:389 - 00:41:48:310] **Speaker 0:** 220 signals.
[00:41:49:350 - 00:41:57:459] **Speaker 0:** Um This is just such a great way of analysing
[00:41:57:459 - 00:41:57:689] **Speaker 0:** it.
[00:42:02:030 - 00:42:04:590] **Speaker 0:** And so then you can just go straight to what
[00:42:04:590 - 00:42:05:139] **Speaker 0:** Z2 is.
[00:42:05:189 - 00:42:06:239] **Speaker 0:** That's the impedance there.
[00:42:07:129 - 00:42:08:209] **Speaker 0:** And then they see it won.
[00:42:09:389 - 00:42:10:560] **Speaker 0:** And then you plug them into here and you get
[00:42:10:560 - 00:42:11:300] **Speaker 0:** the transfer function.
[00:42:12:459 - 00:42:13:300] **Speaker 0:** So what is Z1?
[00:42:14:439 - 00:42:15:719] **Speaker 0:** Z1 is just gonna be SL.
[00:42:18:560 - 00:42:20:790] **Speaker 0:** Therefore, TFS.
[00:42:22:739 - 00:42:24:969] **Speaker 0:** Plug them all in, simplify.
[00:42:26:739 - 00:42:28:300] **Speaker 0:** And you end up with.
[00:42:30:260 - 00:42:38:169] **Speaker 0:** This Because you can work in the real world and
[00:42:38:169 - 00:42:39:929] **Speaker 0:** you can forget, well, how do you, so you work
[00:42:39:929 - 00:42:42:649] **Speaker 0:** in the mathematical world, and you can be a great
[00:42:42:649 - 00:42:45:270] **Speaker 0:** philtre designer, but how do you build it?
[00:42:45:889 - 00:42:48:770] **Speaker 0:** So you actually have to realise that the correct values
[00:42:48:770 - 00:42:50:459] **Speaker 0:** for the inductor and the and the capacitor and the
[00:42:50:459 - 00:42:51:100] **Speaker 0:** resistor.
[00:42:52:580 - 00:42:54:560] **Speaker 0:** And so you just do this.
[00:42:55:820 - 00:42:56:560] **Speaker 0:** And.
[00:43:06:030 - 00:43:08:689] **Speaker 0:** Then you can let the mass equal the real world.
[00:43:15:229 - 00:43:17:310] **Speaker 0:** So you've chosen your queue to be that 1 over
[00:43:17:310 - 00:43:19:889] **Speaker 0:** route 2 magic number that Butterworth discovered.
[00:43:21:209 - 00:43:22:310] **Speaker 0:** You've got your frequency.
[00:43:24:260 - 00:43:26:800] **Speaker 0:** You can choose the resistances to equal that.
[00:43:28:629 - 00:43:29:879] **Speaker 0:** You can solve these equations.
[00:43:29:959 - 00:43:32:040] **Speaker 0:** You can say, I want this natural frequency.
[00:43:32:159 - 00:43:33:919] **Speaker 0:** I'm gonna, I want it, right?
[00:43:34:000 - 00:43:36:389] **Speaker 0:** I want it to be passing everything before there was
[00:43:36:389 - 00:43:37:149] **Speaker 0:** a low pass folder.
[00:43:38:510 - 00:43:40:020] **Speaker 0:** I want this to be my Q factor.
[00:43:41:189 - 00:43:42:610] **Speaker 0:** And I want this to be my gain.
[00:43:42:909 - 00:43:45:399] **Speaker 0:** Maybe you want the gain to be one, then LC
[00:43:45:399 - 00:43:46:110] **Speaker 0:** would equal to one.
[00:43:47:209 - 00:43:49:770] **Speaker 0:** And so there's 3 equations and there's 3 unknowns.
[00:43:49:810 - 00:43:52:489] **Speaker 0:** We have Q, omega 0 and 0.
[00:43:53:129 - 00:43:57:969] **Speaker 0:** So you can completely uniquely realise the LCR combination that
[00:43:57:969 - 00:44:00:310] **Speaker 0:** gives you exactly what you want.
[00:44:10:250 - 00:44:10:260] **Speaker 0:** Right.
[00:44:12:439 - 00:44:14:800] **Speaker 0:** Because if you can understand this concept, then all the
[00:44:14:800 - 00:44:17:379] **Speaker 0:** active filtering will just come much easier.
[00:44:18:280 - 00:44:19:479] **Speaker 0:** Cause that's the idea there.
[00:44:19:600 - 00:44:21:679] **Speaker 0:** You kind of have your generic.
[00:44:22:719 - 00:44:23:860] **Speaker 0:** Transfer function form.
[00:44:26:030 - 00:44:29:149] **Speaker 0:** And then once you've got that, you do all the
[00:44:29:149 - 00:44:32:169] **Speaker 0:** mathematical manipulation to get into a form where you can
[00:44:32:169 - 00:44:35:260] **Speaker 0:** equate it to like the the resistors and the capacitors
[00:44:35:260 - 00:44:37:620] **Speaker 0:** and the inductors that are in your circuit, except for
[00:44:37:629 - 00:44:38:810] **Speaker 0:** for an active philtre.
[00:44:39:629 - 00:44:41:219] **Speaker 0:** You don't actually have an inductor.
[00:44:41:560 - 00:44:44:280] **Speaker 0:** You have like a fancy op amp realisation of an
[00:44:44:280 - 00:44:44:800] **Speaker 0:** inductor.
[00:44:45:949 - 00:44:46:679] **Speaker 0:** Which is the cool part.
[00:44:46:870 - 00:44:48:580] **Speaker 0:** It's the cool part that starts later.
[00:44:49:040 - 00:44:50:840] **Speaker 0:** But I'm probably not going to get it to this
[00:44:50:840 - 00:44:51:280] **Speaker 0:** lecture.
[00:44:52:189 - 00:44:52:659] **Speaker 0:** It's all right.
[00:44:52:709 - 00:44:53:810] **Speaker 0:** So hopefully you got that.
[00:44:57:290 - 00:44:59:090] **Speaker 0:** And I don't really want to do this for every
[00:44:59:090 - 00:45:01:709] **Speaker 0:** one of these, but I've just given you the answer.
[00:45:03:850 - 00:45:05:570] **Speaker 0:** If you really wanted to, you could go through this
[00:45:05:570 - 00:45:07:649] **Speaker 0:** whole exercise and you just change the Z1 and the
[00:45:07:649 - 00:45:11:409] **Speaker 0:** Z2 and you run through this um this mathematics and
[00:45:11:409 - 00:45:12:729] **Speaker 0:** then if you want at the end you can like
[00:45:12:729 - 00:45:14:350] **Speaker 0:** equate the two, equate the 3.
[00:45:15:610 - 00:45:17:770] **Speaker 0:** And you can do it for, I've done the low
[00:45:17:770 - 00:45:18:469] **Speaker 0:** pass philtre.
[00:45:19:510 - 00:45:20:820] **Speaker 0:** See I actually got the right answer.
[00:45:21:219 - 00:45:22:030] **Speaker 0:** One over LC.
[00:45:24:590 - 00:45:26:310] **Speaker 0:** I ran the wrong way, but yeah, it's it's the
[00:45:26:310 - 00:45:26:610] **Speaker 0:** same.
[00:45:27:969 - 00:45:30:409] **Speaker 0:** This one here, the inductor in now is on the
[00:45:30:409 - 00:45:32:530] **Speaker 0:** load and you got a capacitor here.
[00:45:32:610 - 00:45:34:070] **Speaker 0:** This is a high-pass philtre.
[00:45:36:629 - 00:45:38:250] **Speaker 0:** And you can see there's an S 2 here.
[00:45:40:709 - 00:45:42:830] **Speaker 0:** And uh what does that give you?
[00:45:45:399 - 00:45:48:840] **Speaker 0:** 40 dB per 40 dB per decade, right?
[00:45:48:959 - 00:45:50:780] **Speaker 0:** So you squared you imagine you were shooting up the
[00:45:50:780 - 00:45:52:419] **Speaker 0:** body plot at 40 dB per decade.
[00:45:53:550 - 00:45:55:989] **Speaker 0:** But if you're on the negative of the attenuation as
[00:45:55:989 - 00:45:59:360] **Speaker 0:** you're going upwards, right, that means you are attenuating the
[00:45:59:360 - 00:46:00:810] **Speaker 0:** low frequencies.
[00:46:01:669 - 00:46:04:310] **Speaker 0:** You're removing all the low frequencies, and that's what the
[00:46:04:310 - 00:46:06:469] **Speaker 0:** high pass philtre does with the squared term on the
[00:46:06:469 - 00:46:06:689] **Speaker 0:** top.
[00:46:08:429 - 00:46:10:949] **Speaker 0:** And then assuming you haven't designed it so there's a
[00:46:10:949 - 00:46:13:209] **Speaker 0:** big bump, you know, like say you had a Butterworth.
[00:46:14:250 - 00:46:15:879] **Speaker 0:** Uh, when you hit the cutoff frequency.
[00:46:17:250 - 00:46:19:830] **Speaker 0:** Um, which would be the square root of 1 over
[00:46:19:830 - 00:46:21:290] **Speaker 0:** LC for a low pass fer.
[00:46:21:649 - 00:46:22:850] **Speaker 0:** But this year, I think it's actually the same.
[00:46:22:929 - 00:46:24:510] **Speaker 0:** It'll be the same here as well.
[00:46:25:399 - 00:46:28:340] **Speaker 0:** Um, so even for a high pass folder, the cutoff
[00:46:28:340 - 00:46:31:340] **Speaker 0:** frequentry is still square or 1 over LC or omega
[00:46:31:340 - 00:46:34:340] **Speaker 0:** squared will still be 1 over LC even for a
[00:46:34:340 - 00:46:34:959] **Speaker 0:** high pass.
[00:46:36:830 - 00:46:40:159] **Speaker 0:** And so then you hit the one over LC and
[00:46:40:159 - 00:46:41:840] **Speaker 0:** then straight away you're flatlining.
[00:46:42:760 - 00:46:44:479] **Speaker 0:** Like you got obviously you're going up with this, you're
[00:46:44:479 - 00:46:45:520] **Speaker 0:** sorry, what am I saying?
[00:46:45:570 - 00:46:48:610] **Speaker 0:** You're going up at 40% per decade, and then you're
[00:46:48:610 - 00:46:50:610] **Speaker 0:** flat lying at 0 dB per decade, right, because you're
[00:46:50:610 - 00:46:54:409] **Speaker 0:** hitting the second order, um, pole at that cutoff frequency.
[00:46:55:729 - 00:46:58:010] **Speaker 0:** So you should be able to see why that is
[00:46:58:010 - 00:46:59:729] **Speaker 0:** acting as a high-pass philtre.
[00:47:01:020 - 00:47:03:020] **Speaker 0:** I know this should be revision.
[00:47:03:100 - 00:47:06:729] **Speaker 0:** I'm just not entirely sure if you're Uh, band pass
[00:47:06:729 - 00:47:11:120] **Speaker 0:** folder, uh, same idea, but you would then, you're coming
[00:47:11:120 - 00:47:15:070] **Speaker 0:** up at 90, 20 dB per decade.
[00:47:15:570 - 00:47:17:330] **Speaker 0:** You're flatlining for a bit and then you're going back
[00:47:17:330 - 00:47:17:889] **Speaker 0:** down again.
[00:47:18:250 - 00:47:20:209] **Speaker 0:** So you're not really flatlining in this case, you are
[00:47:20:209 - 00:47:21:350] **Speaker 0:** kind of doing this.
[00:47:22:250 - 00:47:24:889] **Speaker 0:** Here And so you want to ditch kind of your
[00:47:24:889 - 00:47:25:489] **Speaker 0:** past band.
[00:47:26:300 - 00:47:27:639] **Speaker 0:** And so there's a ripple in here.
[00:47:31:929 - 00:47:33:800] **Speaker 0:** And then you have an arch, which would look like
[00:47:33:800 - 00:47:34:159] **Speaker 0:** this.
[00:47:35:189 - 00:47:36:649] **Speaker 0:** That's a 2nd order of design.
[00:47:37:030 - 00:47:38:870] **Speaker 0:** If you want to say this is a bit of
[00:47:38:870 - 00:47:39:899] **Speaker 0:** a pain, is a bit of ripple.
[00:47:39:989 - 00:47:41:080] **Speaker 0:** If you don't want that.
[00:47:41:820 - 00:47:44:379] **Speaker 0:** You can get something that's more like that original graph
[00:47:44:379 - 00:47:45:939] **Speaker 0:** that I showed you, like a Chevychev.
[00:47:46:419 - 00:47:48:320] **Speaker 0:** But then you've got a 5th look like this.
[00:47:49:590 - 00:47:51:649] **Speaker 0:** But then you got like a massively high water philtre.
[00:47:53:290 - 00:47:55:340] **Speaker 0:** But a second order philtre is a very low order
[00:47:55:340 - 00:47:55:879] **Speaker 0:** philtre.
[00:47:56:419 - 00:47:58:100] **Speaker 0:** And of course, you don't get perfect filtering.
[00:47:58:139 - 00:47:59:500] **Speaker 0:** You get something that looks like this.
[00:48:01:179 - 00:48:01:540] **Speaker 0:** All right.
[00:48:03:870 - 00:48:06:360] **Speaker 0:** OK, so we have a beam pass and then we
[00:48:06:360 - 00:48:07:080] **Speaker 0:** have a notch.
[00:48:07:429 - 00:48:10:560] **Speaker 0:** So let's move on and I got One slide lift.
[00:48:13:010 - 00:48:14:770] **Speaker 0:** Uh, what do I have to say about this?
[00:48:15:250 - 00:48:16:310] **Speaker 0:** I have a little bit to say.
[00:48:21:030 - 00:48:23:669] **Speaker 0:** So yeah, you, you sort of pulling the all the
[00:48:23:669 - 00:48:24:560] **Speaker 0:** coefficients.
[00:48:26:389 - 00:48:29:969] **Speaker 0:** These philtre polycom efficient coefficients will change depending on its
[00:48:29:969 - 00:48:33:840] **Speaker 0:** body with Chevychev type 1, type 2, or a vessel.
[00:48:34:610 - 00:48:36:129] **Speaker 0:** And what you typically get if you look up all
[00:48:36:129 - 00:48:38:610] **Speaker 0:** the spec sheets like they have a whole lot of
[00:48:38:610 - 00:48:42:239] **Speaker 0:** list of tables for all of these types of philtres.
[00:48:42:810 - 00:48:46:090] **Speaker 0:** And the tables just like this coefficients and they can
[00:48:46:090 - 00:48:48:280] **Speaker 0:** go up to like arbitrarily high orders.
[00:48:50:300 - 00:48:52:699] **Speaker 0:** And so depending on which one it is, you obviously
[00:48:52:699 - 00:48:53:500] **Speaker 0:** have a different table.
[00:48:53:739 - 00:48:56:139] **Speaker 0:** But the the the entire set of tables with all
[00:48:56:139 - 00:48:57:979] **Speaker 0:** the formulas that could go up to 5th, 16th, 7th,
[00:48:58:060 - 00:49:02:419] **Speaker 0:** 10th order philtres would be for 3DB for that 3DB
[00:49:02:419 - 00:49:03:439] **Speaker 0:** um attenuation.
[00:49:04:280 - 00:49:05:840] **Speaker 0:** If you want the 1 DB you have to go
[00:49:05:840 - 00:49:07:479] **Speaker 0:** to another holding a set of tables that are all
[00:49:07:479 - 00:49:08:439] **Speaker 0:** done for the 1 dB.
[00:49:08:959 - 00:49:11:020] **Speaker 0:** But just that 3DB is the industry standard.
[00:49:11:600 - 00:49:13:280] **Speaker 0:** So you would normally choose that.
[00:49:14:510 - 00:49:16:419] **Speaker 0:** But if you choose a Butterworth, then you have that
[00:49:16:419 - 00:49:18:320] **Speaker 0:** has the roll off and so you don't have to
[00:49:18:320 - 00:49:20:830] **Speaker 0:** worry about the um that's why everyone likes Butterworth I
[00:49:20:830 - 00:49:22:179] **Speaker 0:** suppose because you don't have to worry about the.
[00:49:23:689 - 00:49:29:679] **Speaker 0:** You know, the ripple Um So that's this is the
[00:49:29:679 - 00:49:30:280] **Speaker 0:** type one.
[00:49:30:679 - 00:49:33:219] **Speaker 0:** So type one kind of looks like this.
[00:49:34:419 - 00:49:36:219] **Speaker 0:** Like it, it's really interesting the way it does it
[00:49:36:219 - 00:49:39:600] **Speaker 0:** cause it, it like creates the ripple just as yes
[00:49:39:600 - 00:49:42:580] **Speaker 0:** it can really like go over real fast because this
[00:49:42:580 - 00:49:44:040] **Speaker 0:** is where you're getting the trade-off because you're getting a
[00:49:44:040 - 00:49:47:820] **Speaker 0:** really fast transition transition into the attenuation, but then you
[00:49:47:820 - 00:49:48:520] **Speaker 0:** get this ripple.
[00:49:50:860 - 00:49:52:080] **Speaker 0:** Uh, that is type one.
[00:49:53:260 - 00:49:55:090] **Speaker 0:** And then type 2, you're flat here.
[00:49:58:280 - 00:50:00:889] **Speaker 0:** Be so What Bessel does.
[00:50:01:909 - 00:50:04:739] **Speaker 0:** Is it makes the change the rate of change in
[00:50:04:739 - 00:50:06:850] **Speaker 0:** fire versus the frequency as constant as possible.
[00:50:12:290 - 00:50:14:280] **Speaker 0:** And then you get something called linear phase.
[00:50:17:090 - 00:50:18:919] **Speaker 0:** In the in the uh past band.
[00:50:20:750 - 00:50:23:270] **Speaker 0:** And the linear phase is really great, especially for like
[00:50:23:270 - 00:50:26:189] **Speaker 0:** RF whenever like on a, on a radio, you'll get
[00:50:26:189 - 00:50:28:669] **Speaker 0:** just a constant delay instead of your voice being totally
[00:50:28:669 - 00:50:30:590] **Speaker 0:** distorted on the other end because all the frequencies of
[00:50:30:590 - 00:50:34:110] **Speaker 0:** your voice all have like non-linear phase delays.
[00:50:34:939 - 00:50:36:399] **Speaker 0:** So linear phase is a good thing.
[00:50:37:219 - 00:50:38:360] **Speaker 0:** And that's what the vessel does.
[00:50:41:159 - 00:50:43:919] **Speaker 0:** Um, just a bit over time, but um.
[00:50:46:929 - 00:50:47:850] **Speaker 0:** It's exactly 4:15.
[00:50:47:929 - 00:50:49:649] **Speaker 0:** I'm gonna grab that, grab an extra minute.
[00:50:52:699 - 00:50:54:659] **Speaker 0:** And so really the point here is that the different
[00:50:54:659 - 00:50:56:370] **Speaker 0:** polynomial coefficients.
[00:50:57:580 - 00:51:09:219] **Speaker 0:** Result In different philtre Characteristics.
[00:51:12:070 - 00:51:14:370] **Speaker 0:** I'm gonna try and, it's 451, that'll do.
[00:51:17:219 - 00:51:19:939] **Speaker 0:** You choose these different AI's and BI's and they're all
[00:51:19:939 - 00:51:20:439] **Speaker 0:** on a table.
[00:51:21:379 - 00:51:23:340] **Speaker 0:** Then once you've got them, you can then relate them
[00:51:23:340 - 00:51:26:139] **Speaker 0:** to the inductives or the capacitor and the resistors and
[00:51:26:139 - 00:51:29:040] **Speaker 0:** then Make all sorts of different types of filtering.
[00:51:29:659 - 00:51:30:439] **Speaker 0:** We'll leave it there.
[00:51:30:899 - 00:51:32:280] **Speaker 0:** Thank you, and I'll see you tomorrow.
[00:51:43:820 - 00:51:46:429] **Speaker 2:** Um No.
[00:51:49:540 - 00:51:55:280] **Speaker 2:** Yeah What is it like President.
[00:51:57:370 - 00:51:57:379] **Speaker 2:** OK.
[00:51:59:550 - 00:52:03:879] **Speaker 2:** It wasn't.
[00:52:08:469 - 00:52:10:020] **Speaker 2:** No, no, no, I do.
[00:52:11:560 - 00:52:15:370] **Speaker 2:** OK, this, this.
[00:52:18:120 - 00:52:18:169] **Speaker 2:** Oh, that's.
[00:52:22:979 - 00:52:26:729] **Speaker 2:** Thank you, it's tricky.
[00:52:26:739 - 00:52:28:229] **Speaker 2:** I mean you.
[00:52:33:860 - 00:52:33:879] **Speaker 2:** We had.
[00:52:43:959 - 00:52:45:219] **Speaker 0:** Get your controllers notes out.
[00:52:46:199 - 00:52:47:530] **Speaker 0:** Get your controller's notes out.
[00:52:50:320 - 00:52:51:239] **Speaker 0:** Oh, no, you haven't.
[00:52:51:719 - 00:52:52:110] **Speaker 0:** What?
[00:52:52:479 - 00:52:54:080] **Speaker 0:** Mechatronics have always, how come you haven't?
[00:52:57:360 - 00:52:58:000] **Speaker 0:** That doesn't make sense.
[00:52:58:120 - 00:52:59:379] **Speaker 0:** Oh, that's right.
[00:53:01:600 - 00:53:02:639] **Speaker 0:** So how come you're doing 3?
[00:53:02:669 - 00:53:05:479] **Speaker 0:** Oh yeah, so you're doing 372 and you haven't, so
[00:53:05:479 - 00:53:06:479] **Speaker 0:** it's very minimal.
[00:53:06:600 - 00:53:08:840] **Speaker 0:** Like it's like this is just 11 lecture series like
[00:53:08:840 - 00:53:09:580] **Speaker 0:** I'm doing it right.
[00:53:10:320 - 00:53:10:330] **Speaker 0:** But.
[00:53:12:780 - 00:53:14:540] **Speaker 0:** I know, but then, but I suppose it's a bit,
[00:53:14:659 - 00:53:16:860] **Speaker 0:** it is a bit tricky if you haven't done transfer
[00:53:16:860 - 00:53:17:300] **Speaker 0:** functions.
[00:53:19:020 - 00:53:23:300] **Speaker 0:** Because Buck converters is is a 2 section.
[00:53:23:310 - 00:53:23:649] **Speaker 2:** Megatronics.
[00:53:28:810 - 00:53:30:129] **Speaker 2:** That's uh, you know, I don't know

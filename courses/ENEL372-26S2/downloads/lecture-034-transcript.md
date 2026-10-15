# ENEL372-26S2 Lecture 34 native Echo transcript

Date: October 9, 2026 12:00pm-12:55pm
Transcript type: native Echo automated transcript.

[00:00:00:850 - 00:00:02:450] **Speaker 0:** Yep, there we go, so.
[00:00:04:289 - 00:00:05:030] **Speaker 0:** I'll get started.
[00:00:06:719 - 00:00:09:220] **Speaker 0:** AC cup circuits, news topic.
[00:00:13:060 - 00:00:20:649] **Speaker 0:** And is It's not much really to.
[00:00:21:459 - 00:00:22:319] **Speaker 0:** Stay there.
[00:00:23:940 - 00:00:29:090] **Speaker 0:** Just uh You are coupling AC across the circuit and
[00:00:29:780 - 00:00:30:700] **Speaker 0:** doing an amplification.
[00:00:30:739 - 00:00:32:580] **Speaker 0:** There's a bit of a steady state offset, then you've
[00:00:32:580 - 00:00:33:680] **Speaker 0:** got to kind of remove it.
[00:00:34:750 - 00:00:38:319] **Speaker 0:** And I can't really tell actually very well with this
[00:00:38:319 - 00:00:40:380] **Speaker 0:** particular slide, but there's a, there is a red here.
[00:00:42:500 - 00:00:46:200] **Speaker 0:** And then so you're, the, the effect is you're amplifying.
[00:00:47:369 - 00:00:51:369] **Speaker 0:** And you're actually removing the uh the DC offset as
[00:00:51:369 - 00:00:51:709] **Speaker 0:** well.
[00:00:55:139 - 00:00:56:180] **Speaker 0:** So, that's what that is.
[00:00:58:110 - 00:01:01:290] **Speaker 0:** This is a more complicated circuit.
[00:01:02:729 - 00:01:06:110] **Speaker 0:** So there was just one cascading amplifier here, or one
[00:01:06:110 - 00:01:08:389] **Speaker 0:** amplifier, it's not cascading, it's just an amplifier.
[00:01:09:500 - 00:01:12:339] **Speaker 0:** We hear you've got like a cascading amplifier so you
[00:01:12:339 - 00:01:15:720] **Speaker 0:** can Put several of these together.
[00:01:18:080 - 00:01:21:110] **Speaker 0:** And get more amplification, better properties.
[00:01:24:580 - 00:01:27:750] **Speaker 0:** And, um, Yeah, that's.
[00:01:30:080 - 00:01:31:260] **Speaker 0:** Can't quite see it, but.
[00:01:32:589 - 00:01:35:239] **Speaker 0:** I'll just labelled it here, your original signal comes into
[00:01:35:239 - 00:01:35:739] **Speaker 0:** here.
[00:01:36:669 - 00:01:41:500] **Speaker 0:** Like that At this stage, it gets, it gets kind
[00:01:41:500 - 00:01:45:699] **Speaker 0:** of like DC shifted up, DC offset shifted up.
[00:01:46:779 - 00:01:48:730] **Speaker 0:** Then this one here amplifies it.
[00:01:50:349 - 00:01:54:580] **Speaker 0:** And you end up with um Yeah.
[00:01:55:440 - 00:01:57:819] **Speaker 0:** Bigger amplitude, then you get another amplification here as well
[00:01:57:819 - 00:02:00:610] **Speaker 0:** as removing the because you've got this this capacity here
[00:02:00:610 - 00:02:03:519] **Speaker 0:** which will remove the DC offset and then you End
[00:02:03:519 - 00:02:08:130] **Speaker 0:** up with um The amplification, so it's a, it's an
[00:02:08:130 - 00:02:10:059] **Speaker 0:** amplifier, cascaded amplifier.
[00:02:17:289 - 00:02:19:210] **Speaker 0:** Which is actually the L2 Spice version.
[00:02:20:360 - 00:02:21:880] **Speaker 0:** Of that, which is in the notes.
[00:02:23:330 - 00:02:24:660] **Speaker 0:** Just showing you how it works.
[00:02:26:809 - 00:02:28:679] **Speaker 0:** So anyway, let's get started on this.
[00:02:32:259 - 00:02:33:630] **Speaker 0:** Hasty coupled circuits.
[00:02:35:610 - 00:02:38:830] **Speaker 0:** So this is a common, Category.
[00:02:42:059 - 00:02:42:860] **Speaker 0:** circuits.
[00:02:48:250 - 00:02:50:449] **Speaker 0:** You're sort of moving the AC from one module to
[00:02:50:449 - 00:02:52:149] **Speaker 0:** another all along this cascading.
[00:02:53:160 - 00:03:05:020] **Speaker 0:** Um, system And part of the AC coupling involves the
[00:03:05:020 - 00:03:07:919] **Speaker 0:** removal or to remove the DC offset.
[00:03:11:479 - 00:03:12:800] **Speaker 0:** And a couple.
[00:03:14:279 - 00:03:18:929] **Speaker 0:** I say From one module.
[00:03:21:449 - 00:03:22:080] **Speaker 0:** To another.
[00:03:30:100 - 00:03:33:380] **Speaker 0:** So that's cascaded with transistors, but yeah, you also get
[00:03:33:380 - 00:03:33:600] **Speaker 0:** it.
[00:03:34:699 - 00:03:35:839] **Speaker 0:** So I also.
[00:03:37:610 - 00:03:39:940] **Speaker 0:** And that's what I'm really mostly covering in the exam.
[00:03:40:589 - 00:03:41:529] **Speaker 0:** AC coupling.
[00:03:42:839 - 00:03:45:000] **Speaker 0:** In all circuits.
[00:03:45:949 - 00:03:48:119] **Speaker 0:** So I don't, I don't ask the transistor.
[00:03:49:320 - 00:03:53:050] **Speaker 0:** Type circuit for the exam, it's or off-hamp circuits.
[00:03:54:259 - 00:03:58:009] **Speaker 0:** And it's either the Not inverting or the inverting, well
[00:03:58:009 - 00:04:00:490] **Speaker 0:** this is the inverting because obviously it's coming into the
[00:04:00:490 - 00:04:01:410] **Speaker 0:** minus sign here.
[00:04:02:110 - 00:04:03:800] **Speaker 0:** So that's the inverting case.
[00:04:04:630 - 00:04:06:429] **Speaker 0:** This is a non-inverting case.
[00:04:07:750 - 00:04:09:800] **Speaker 0:** I tend to oscillate from year to year in the
[00:04:09:800 - 00:04:10:240] **Speaker 0:** exam.
[00:04:19:618 - 00:04:20:579] **Speaker 0:** This here.
[00:04:23:440 - 00:04:36:500] **Speaker 0:** We'll discuss later But it's for Impedance matching.
[00:04:43:649 - 00:04:43:859] **Speaker 0:** Some machine for pain.
[00:04:49:730 - 00:04:51:839] **Speaker 0:** Yeah, so you wanna get the the biassing right.
[00:04:56:589 - 00:04:58:730] **Speaker 0:** And the impedance matching that can help.
[00:04:59:839 - 00:05:02:260] **Speaker 0:** You stop instabilities.
[00:05:04:859 - 00:05:06:059] **Speaker 0:** And you're on a penis mission.
[00:05:07:470 - 00:05:09:000] **Speaker 0:** And what we're going to do is we'll set the
[00:05:09:000 - 00:05:09:739] **Speaker 0:** bias.
[00:05:12:179 - 00:05:13:459] **Speaker 0:** VCC over 2.
[00:05:16:260 - 00:05:17:950] **Speaker 0:** So you should be familiar with all that kind of
[00:05:17:950 - 00:05:18:070] **Speaker 0:** stuff.
[00:05:18:149 - 00:05:21:390] **Speaker 0:** You want to get the maximum range of the up
[00:05:21:390 - 00:05:22:890] **Speaker 0:** amps, so you want to bias it right.
[00:05:28:250 - 00:05:30:049] **Speaker 0:** You don't want it to be clipping one side of
[00:05:30:049 - 00:05:30:869] **Speaker 0:** the sine wave.
[00:05:31:239 - 00:05:31:970] **Speaker 0:** That would not be good.
[00:05:35:779 - 00:05:36:739] **Speaker 0:** That's pretty standard.
[00:05:41:570 - 00:05:42:649] **Speaker 0:** No I'm waiting guys.
[00:05:45:440 - 00:05:48:309] **Speaker 0:** And you will only be doing impedance matching between the
[00:05:48:309 - 00:05:51:279] **Speaker 0:** effective resistance going in here and then this resistance going
[00:05:51:279 - 00:05:51:739] **Speaker 0:** in there.
[00:05:58:679 - 00:06:02:179] **Speaker 0:** That's normally like a low pass, high pass philtre here,
[00:06:02:320 - 00:06:04:119] **Speaker 0:** but we'll discuss that in the next few slides.
[00:06:05:500 - 00:06:07:869] **Speaker 0:** This, as I was mentioning earlier, well this is a
[00:06:07:950 - 00:06:08:970] **Speaker 0:** two-stage.
[00:06:12:500 - 00:06:13:339] **Speaker 0:** Cascaded.
[00:06:15:480 - 00:06:15:920] **Speaker 0:** Come on.
[00:06:18:609 - 00:06:19:380] **Speaker 0:** Amplifier.
[00:06:23:390 - 00:06:28:170] **Speaker 0:** There is one important aspect with this particular, this topic.
[00:06:28:890 - 00:06:31:190] **Speaker 0:** Is that you have a single source.
[00:06:34:859 - 00:06:36:950] **Speaker 0:** Single source is powering everything.
[00:06:39:859 - 00:06:43:459] **Speaker 0:** And that makes it harder, and there's a few things
[00:06:43:459 - 00:06:45:260] **Speaker 0:** you've got to be aware of when you have a
[00:06:45:260 - 00:06:47:519] **Speaker 0:** single source supply, which is quite common.
[00:06:49:350 - 00:06:51:470] **Speaker 0:** Sort of like portable applications.
[00:06:54:700 - 00:06:57:209] **Speaker 0:** And so what's happening here with these capacitors.
[00:07:01:790 - 00:07:03:980] **Speaker 0:** As they are coupling the AC.
[00:07:05:260 - 00:07:11:739] **Speaker 0:** 3 The a That's sort of why it's called AC
[00:07:11:739 - 00:07:12:619] **Speaker 0:** coupling, it's.
[00:07:21:510 - 00:07:23:829] **Speaker 0:** So yeah, it's Ay Kipping.
[00:07:25:570 - 00:07:26:899] **Speaker 0:** Let me see a couple of secrets.
[00:07:29:799 - 00:07:32:519] **Speaker 0:** So you've got that, and you've written that.
[00:07:33:779 - 00:07:34:920] **Speaker 0:** Some learning outcomes.
[00:07:40:079 - 00:07:42:089] **Speaker 0:** So, I'm going to examine op amp stability.
[00:07:48:929 - 00:07:50:230] **Speaker 0:** This is really background.
[00:07:52:470 - 00:07:55:230] **Speaker 0:** I don't think I actually ask in this, the exam
[00:07:55:230 - 00:07:55:880] **Speaker 0:** this time.
[00:07:57:640 - 00:07:58:470] **Speaker 0:** Not specifically.
[00:08:00:299 - 00:08:01:100] **Speaker 0:** An exam, Ms.
[00:08:01:339 - 00:08:01:350] **Speaker 0:** Lo?
[00:08:04:209 - 00:08:06:089] **Speaker 0:** It's sort of implicitly needed.
[00:08:06:450 - 00:08:08:450] **Speaker 0:** There's things you've got to do to ensure stability, but
[00:08:08:450 - 00:08:10:690] **Speaker 0:** I don't really ask stability.
[00:08:12:130 - 00:08:15:910] **Speaker 0:** But I'll be covering the concept of OPAM stability.
[00:08:18:779 - 00:08:20:980] **Speaker 0:** Described minimise methods for improving AC coupling.
[00:08:21:100 - 00:08:24:589] **Speaker 0:** Yeah, these two, yep, definitely is an exam.
[00:08:30:489 - 00:08:32:390] **Speaker 0:** Yes, definitely in the exam.
[00:08:35:049 - 00:08:38:150] **Speaker 0:** And you can replace the xenodiode with one of these
[00:08:38:150 - 00:08:39:919] **Speaker 0:** low dropout voltage regulators.
[00:08:41:469 - 00:08:42:049] **Speaker 0:** As well.
[00:08:42:898 - 00:08:44:879] **Speaker 0:** And I've asked that in previous exams.
[00:08:45:379 - 00:08:47:778] **Speaker 0:** So even though I'm describing the AC coupled circuit with
[00:08:47:778 - 00:08:48:658] **Speaker 0:** the xenodiode.
[00:08:49:929 - 00:08:51:469] **Speaker 0:** Sometimes you can replace it.
[00:08:52:440 - 00:08:54:979] **Speaker 0:** With this, the same idea holds.
[00:08:57:340 - 00:08:59:099] **Speaker 0:** This I've never asked in the exam.
[00:08:59:580 - 00:09:00:979] **Speaker 0:** It's just a kind of an extra.
[00:09:04:919 - 00:09:09:049] **Speaker 0:** No t It's really handy.
[00:09:13:650 - 00:09:16:289] **Speaker 0:** OK, that's my lecture 15 learning outcomes.
[00:09:16:690 - 00:09:17:890] **Speaker 0:** So let's get started.
[00:09:18:849 - 00:09:21:799] **Speaker 0:** On to the first learning outcome, examine OPAM stability.
[00:09:23:479 - 00:09:27:000] **Speaker 0:** So let's We'll look at that.
[00:09:29:489 - 00:09:31:570] **Speaker 0:** So you need to get your mind back into control
[00:09:31:570 - 00:09:32:210] **Speaker 0:** systems again.
[00:09:34:820 - 00:09:36:080] **Speaker 0:** And block diagrams.
[00:09:40:330 - 00:09:43:719] **Speaker 0:** So what an op amp really is, an op amp
[00:09:43:719 - 00:09:45:090] **Speaker 0:** is an amplifier, obviously, right?
[00:09:45:210 - 00:09:47:729] **Speaker 0:** It's a massive amplification.
[00:09:48:950 - 00:09:52:719] **Speaker 0:** But what makes it so amazing and and it acts
[00:09:52:719 - 00:09:57:460] **Speaker 0:** like a buffer and it always keeps Yeah, the input
[00:09:57:460 - 00:10:01:599] **Speaker 0:** voltage and From the positive and the negative pins, it
[00:10:01:599 - 00:10:04:770] **Speaker 0:** always keeps them the same voltage, and it does that
[00:10:04:770 - 00:10:08:070] **Speaker 0:** because of a feedback control which is inside the LP
[00:10:08:070 - 00:10:08:250] **Speaker 0:** amp.
[00:10:10:719 - 00:10:12:039] **Speaker 0:** And this is what it is.
[00:10:15:719 - 00:10:18:679] **Speaker 0:** And so you you use block diagram algebra.
[00:10:19:940 - 00:10:25:630] **Speaker 0:** Uh, you would have the signal source minus beta times
[00:10:25:630 - 00:10:28:229] **Speaker 0:** the output, so you have the input and the output.
[00:10:30:630 - 00:10:33:590] **Speaker 0:** And then if you gov 0 again.
[00:10:34:530 - 00:10:38:650] **Speaker 0:** You know it's just gonna be A times the VI.
[00:10:40:679 - 00:10:46:400] **Speaker 0:** A times BI, which is A times, sorry, I did
[00:10:46:400 - 00:10:47:150] **Speaker 0:** that really stupid.
[00:10:50:440 - 00:10:52:840] **Speaker 0:** VS minus beta.
[00:10:53:859 - 00:10:57:460] **Speaker 0:** A times VS minus, remember doing that?
[00:10:57:780 - 00:11:01:059] **Speaker 0:** It's good old block diagram stuff, signal analysis algebra.
[00:11:03:219 - 00:11:04:030] **Speaker 0:** Back in the day.
[00:11:05:369 - 00:11:07:650] **Speaker 0:** It was, it wasn't too long ago, last term, last
[00:11:07:650 - 00:11:08:190] **Speaker 0:** semester.
[00:11:12:539 - 00:11:13:700] **Speaker 0:** And so you.
[00:11:14:640 - 00:11:15:539] **Speaker 0:** Multiply these together.
[00:11:18:820 - 00:11:21:679] **Speaker 0:** And you derive the transfer function for the op amp.
[00:11:22:489 - 00:11:25:849] **Speaker 0:** It's the closed loop transfer function, not the open loop
[00:11:25:849 - 00:11:26:570] **Speaker 0:** transfer function.
[00:11:27:820 - 00:11:30:260] **Speaker 0:** Remember the closed loop is when you have a feedback
[00:11:30:260 - 00:11:33:260] **Speaker 0:** in the path and then you, that's why it's called
[00:11:33:260 - 00:11:33:780] **Speaker 0:** closed loop.
[00:11:44:840 - 00:11:46:539] **Speaker 0:** And so that's the amplitude.
[00:11:47:320 - 00:11:49:640] **Speaker 0:** Divided by 1 plus Mitude times beta.
[00:11:53:299 - 00:11:57:140] **Speaker 0:** But in all pain, The actual amplification that you get
[00:11:57:140 - 00:11:59:460] **Speaker 0:** is massive, but it can change as a function of
[00:11:59:460 - 00:12:00:099] **Speaker 0:** frequency.
[00:12:10:969 - 00:12:15:510] **Speaker 0:** So we're going to model Is the impitude.
[00:12:16:880 - 00:12:21:359] **Speaker 0:** Of some transfer function GFS, we're going into the Laplace
[00:12:21:359 - 00:12:21:880] **Speaker 0:** domain.
[00:12:30:130 - 00:12:31:640] **Speaker 0:** So if I was to describe that.
[00:12:32:619 - 00:12:34:340] **Speaker 0:** This transfer for something that looked a little bit like
[00:12:34:340 - 00:12:34:650] **Speaker 0:** that.
[00:12:36:520 - 00:12:41:250] **Speaker 0:** You can see it starts to Roll off at some,
[00:12:41:380 - 00:12:44:270] **Speaker 0:** you know, some sort of poll that's making it go
[00:12:44:270 - 00:12:47:909] **Speaker 0:** negative dB to 20 negative dB per decade, but then
[00:12:47:909 - 00:12:49:090] **Speaker 0:** it goes even more.
[00:12:49:909 - 00:12:52:869] **Speaker 0:** Because it's crossing, it looks like it might settle out
[00:12:52:869 - 00:12:54:070] **Speaker 0:** to be -270.
[00:12:55:349 - 00:12:57:500] **Speaker 0:** So that would be, say 3, say this came, say
[00:12:57:500 - 00:13:00:369] **Speaker 0:** this were like asymptoped out, it would be like 3
[00:13:00:369 - 00:13:00:919] **Speaker 0:** poles.
[00:13:02:729 - 00:13:04:169] **Speaker 0:** So you would say.
[00:13:05:049 - 00:13:09:130] **Speaker 0:** So this is a common model for A very simple
[00:13:09:679 - 00:13:12:770] **Speaker 0:** model, but a common approach to modelling an LA.
[00:13:14:239 - 00:13:15:700] **Speaker 0:** And with the feedback control.
[00:13:17:390 - 00:13:22:530] **Speaker 0:** Is 2nd order poll.
[00:13:24:119 - 00:13:29:859] **Speaker 0:** In a fish store the pole And then you would
[00:13:29:859 - 00:13:30:460] **Speaker 0:** say.
[00:13:31:190 - 00:13:35:049] **Speaker 0:** The amplitude is obviously the magnitude.
[00:13:35:890 - 00:13:36:780] **Speaker 0:** Of the Jin function.
[00:13:38:140 - 00:13:40:080] **Speaker 0:** So what I've done here is I've modelled the fact
[00:13:40:080 - 00:13:46:150] **Speaker 0:** that The feedback amplifier is a function of frequency, or
[00:13:46:150 - 00:13:48:789] **Speaker 0:** the amplitude is a function of frequency.
[00:13:51:380 - 00:13:52:619] **Speaker 0:** And that's just an example.
[00:13:52:739 - 00:13:55:340] **Speaker 0:** There could be other, there could be other transfer functions,
[00:13:55:460 - 00:14:01:780] **Speaker 0:** but that's But you've got to think to yourself, this
[00:14:01:780 - 00:14:03:479] **Speaker 0:** has got a gain, it's got a phase.
[00:14:06:140 - 00:14:06:659] **Speaker 0:** What happened there?
[00:14:09:200 - 00:14:10:919] **Speaker 0:** No, not another network failure.
[00:14:12:340 - 00:14:13:679] **Speaker 0:** I hope this, oh no it's still going.
[00:14:14:869 - 00:14:16:080] **Speaker 0:** I can't trust these rooms now.
[00:14:16:159 - 00:14:18:900] **Speaker 0:** I've like learned to always expect the unexpected now.
[00:14:26:880 - 00:14:28:690] **Speaker 0:** So if you look at this, can someone look at
[00:14:28:690 - 00:14:28:849] **Speaker 0:** that?
[00:14:28:929 - 00:14:30:330] **Speaker 0:** Can you, I don't know, do you remember?
[00:14:30:570 - 00:14:31:840] **Speaker 0:** Can you tell me if it's stable or not?
[00:14:31:929 - 00:14:33:270] **Speaker 0:** Do you think it's stable?
[00:14:34:369 - 00:14:38:099] **Speaker 0:** System Yeah, I reckon it's not, but remember you've got
[00:14:38:099 - 00:14:39:760] **Speaker 0:** to look at the -180 crossing.
[00:14:40:539 - 00:14:42:219] **Speaker 0:** So can you tell me what is the gain margin,
[00:14:42:299 - 00:14:43:400] **Speaker 0:** negative or positive?
[00:14:44:460 - 00:14:45:979] **Speaker 0:** Look at the -180 degree crossing.
[00:14:46:030 - 00:14:50:929] **Speaker 0:** Remember it's stable.
[00:14:51:469 - 00:14:54:469] **Speaker 0:** It's stable because the, the gain margin and the phase
[00:14:54:469 - 00:14:55:690] **Speaker 0:** margin are positive.
[00:14:59:880 - 00:15:02:239] **Speaker 0:** So the current plot.
[00:15:04:729 - 00:15:07:729] **Speaker 0:** For the whatever game that you chose that you programmed
[00:15:07:729 - 00:15:09:010] **Speaker 0:** it in, the beta.
[00:15:11:119 - 00:15:12:030] **Speaker 0:** Is stable.
[00:15:24:340 - 00:15:25:390] **Speaker 0:** So the gain margin.
[00:15:25:650 - 00:15:27:390] **Speaker 0:** But if you increased beta.
[00:15:28:130 - 00:15:31:390] **Speaker 0:** Because maybe he wanted a, a better, faster response.
[00:15:34:039 - 00:15:34:559] **Speaker 0:** For the Amp?
[00:15:37:210 - 00:15:39:010] **Speaker 0:** So I don't know, it had less transient effects or
[00:15:39:010 - 00:15:41:369] **Speaker 0:** something because if beta was really, really small, then it
[00:15:41:369 - 00:15:44:289] **Speaker 0:** would take longer to hit, it would take longer to
[00:15:44:289 - 00:15:46:609] **Speaker 0:** reach steady state between the venal, and that may create
[00:15:46:609 - 00:15:46:799] **Speaker 0:** issues.
[00:15:46:809 - 00:15:49:090] **Speaker 0:** So sometimes you might want increased beta.
[00:15:51:159 - 00:15:52:909] **Speaker 0:** But you got to be careful increasing beta.
[00:15:54:080 - 00:15:56:599] **Speaker 0:** Because what's going to happen is you're going to lift
[00:15:56:599 - 00:15:57:140] **Speaker 0:** this up.
[00:16:00:809 - 00:16:03:570] **Speaker 0:** And you may get an issue, because it could do
[00:16:03:570 - 00:16:04:690] **Speaker 0:** something like this.
[00:16:08:380 - 00:16:16:159] **Speaker 0:** If you increase beta too much, If beta increases.
[00:16:22:710 - 00:16:25:289] **Speaker 0:** Then you may end up with a positive DB.
[00:16:26:260 - 00:16:27:539] **Speaker 0:** It was amplification.
[00:16:31:530 - 00:16:33:330] **Speaker 0:** At the -180 degree crossing.
[00:16:35:489 - 00:16:37:130] **Speaker 0:** Pace crossing.
[00:16:39:880 - 00:16:41:000] **Speaker 0:** Which implies.
[00:16:42:159 - 00:16:45:200] **Speaker 0:** Gain margin is less than 0, unstable.
[00:16:46:830 - 00:16:54:489] **Speaker 0:** That can happen There's a few increased beta.
[00:16:56:710 - 00:16:58:700] **Speaker 0:** And I'll say also.
[00:17:01:299 - 00:17:03:619] **Speaker 0:** For a given beta.
[00:17:06:790 - 00:17:08:030] **Speaker 0:** Parameters.
[00:17:11:349 - 00:17:14:810] **Speaker 0:** Transfer function may change.
[00:17:17:150 - 00:17:26:310] **Speaker 0:** With AJ Temperature And even frequency.
[00:17:26:410 - 00:17:28:050] **Speaker 0:** Like this is only a minimal model.
[00:17:28:089 - 00:17:29:380] **Speaker 0:** Like it's not perfect.
[00:17:30:859 - 00:17:33:530] **Speaker 0:** You can't say that these, these will perfectly capture the
[00:17:33:540 - 00:17:35:130] **Speaker 0:** the behaviour of all frequencies.
[00:17:35:910 - 00:17:37:489] **Speaker 0:** It may, you may get bad luck when you get
[00:17:37:489 - 00:17:40:189] **Speaker 0:** close to the resonant frequency, the parameters could change and
[00:17:40:189 - 00:17:41:829] **Speaker 0:** it doesn't actually behave like a second order.
[00:17:41:869 - 00:17:43:469] **Speaker 0:** It might be a 4th order or something.
[00:17:49:739 - 00:17:51:780] **Speaker 0:** So you may think you've got a great beater, but
[00:17:51:780 - 00:17:54:569] **Speaker 0:** then you find that in some regime for some high
[00:17:54:579 - 00:17:57:979] **Speaker 0:** high frequencies or something, there's extra dynamics you haven't counted
[00:17:57:979 - 00:18:02:719] **Speaker 0:** for parameters of TF or the order.
[00:18:04:630 - 00:18:08:270] **Speaker 0:** Of TF like at the moment it's a 3rd-order system,
[00:18:08:310 - 00:18:10:109] **Speaker 0:** but it could go to, could end up with 2
[00:18:10:109 - 00:18:11:770] **Speaker 0:** 2nd order poles like you don't know.
[00:18:13:599 - 00:18:17:560] **Speaker 0:** So the fact is, is that There's no absolute guarantee
[00:18:17:560 - 00:18:19:420] **Speaker 0:** that your op amp's going to be stable.
[00:18:21:880 - 00:18:23:729] **Speaker 0:** And that's what I want you to understand the concept
[00:18:23:729 - 00:18:24:800] **Speaker 0:** of amplifier stability.
[00:18:34:140 - 00:18:36:079] **Speaker 0:** So there's a few things to think about.
[00:18:41:699 - 00:18:42:339] **Speaker 0:** Warm it up.
[00:18:47:640 - 00:18:52:880] **Speaker 0:** All right, so we have basic AC coupling, stability problems.
[00:18:58:760 - 00:19:00:420] **Speaker 0:** This is for a single supply.
[00:19:07:719 - 00:19:08:910] **Speaker 0:** And that could be.
[00:19:11:209 - 00:19:14:479] **Speaker 0:** Battery powered Or pain.
[00:19:18:680 - 00:19:24:709] **Speaker 0:** Automotive Could be marine equipment.
[00:19:28:030 - 00:19:30:530] **Speaker 0:** And you don't want to have multiple power suppliers.
[00:19:32:020 - 00:19:35:369] **Speaker 0:** Ed's white Cost, complexity.
[00:19:39:180 - 00:19:39:900] **Speaker 0:** Weight's a big one.
[00:19:41:060 - 00:19:42:500] **Speaker 0:** Could be aerospace as well.
[00:19:44:380 - 00:19:46:439] **Speaker 0:** So, uh, you may just want to have one power
[00:19:46:439 - 00:19:49:020] **Speaker 0:** supply on your plane, for example.
[00:19:49:739 - 00:19:50:550] **Speaker 0:** So, um.
[00:19:52:160 - 00:19:53:640] **Speaker 0:** You've got to be cautious on that.
[00:19:56:280 - 00:19:59:199] **Speaker 0:** And that you can get problems with the fluctuations on
[00:19:59:199 - 00:20:01:719] **Speaker 0:** the power supply interfering.
[00:20:02:670 - 00:20:03:449] **Speaker 0:** With the pain.
[00:20:05:589 - 00:20:09:510] **Speaker 0:** This particular way of laying out the circuit is not
[00:20:09:510 - 00:20:10:229] **Speaker 0:** a great one.
[00:20:13:300 - 00:20:15:839] **Speaker 0:** Because you can see there's nothing stopping.
[00:20:16:790 - 00:20:21:680] **Speaker 0:** The noise from the single source coming straight into the
[00:20:21:680 - 00:20:22:189] **Speaker 0:** op amp.
[00:20:23:420 - 00:20:27:000] **Speaker 0:** It's got very low power supply noise rejection.
[00:20:28:540 - 00:20:29:130] **Speaker 0:** PSI.
[00:20:32:199 - 00:20:35:020] **Speaker 0:** And the problems are the noise.
[00:20:37:770 - 00:20:38:869] **Speaker 0:** Strange food.
[00:20:40:439 - 00:20:46:199] **Speaker 0:** Directly Into the opening.
[00:20:52:969 - 00:20:55:229] **Speaker 0:** It will affect DC bias voltage.
[00:21:01:589 - 00:21:03:239] **Speaker 0:** So if you want to work out what the PSR
[00:21:03:239 - 00:21:06:020] **Speaker 0:** is, it's a voltage divider.
[00:21:11:400 - 00:21:14:020] **Speaker 0:** RAB R equals RAB.
[00:21:15:650 - 00:21:19:520] **Speaker 0:** Which is a half So you go 20 log 10.
[00:21:20:500 - 00:21:24:380] **Speaker 0:** Of a half and you'll get -6, which means with
[00:21:24:380 - 00:21:30:540] **Speaker 0:** a voltage divider, you're only getting 6 dB attenuation of
[00:21:30:540 - 00:21:31:979] **Speaker 0:** the supply noise.
[00:21:36:290 - 00:21:39:390] **Speaker 0:** So that's creating a positive feedback path into the op
[00:21:39:390 - 00:21:39:709] **Speaker 0:** amp.
[00:21:40:890 - 00:21:43:219] **Speaker 0:** Don't know, I moved it rather quick, but no, I,
[00:21:43:310 - 00:21:44:510] **Speaker 0:** I think you should have done it by now.
[00:21:45:430 - 00:21:52:670] **Speaker 0:** Um, So even though you think you've got a battery
[00:21:52:670 - 00:21:58:579] **Speaker 0:** and you think that the supply should be DC, There's
[00:21:58:579 - 00:22:00:339] **Speaker 0:** really no such thing as pure DC.
[00:22:03:099 - 00:22:04:300] **Speaker 0:** It's going to look like this.
[00:22:04:380 - 00:22:07:500] **Speaker 0:** It's going to be some sort of a fluctuating waveform.
[00:22:10:640 - 00:22:19:430] **Speaker 0:** And there'll be a Voltage Supply Fluctuation, ESF.
[00:22:21:130 - 00:22:23:329] **Speaker 0:** And then so a half of that.
[00:22:25:300 - 00:22:32:709] **Speaker 0:** In other Comma loud noise.
[00:22:34:430 - 00:22:35:810] **Speaker 0:** Is amplified.
[00:22:39:140 - 00:22:39:640] **Speaker 0:** Through.
[00:22:41:300 - 00:22:42:099] **Speaker 0:** To the airport.
[00:22:45:989 - 00:22:48:920] **Speaker 0:** And so that, yeah, can create problems, especially if the
[00:22:48:920 - 00:22:50:810] **Speaker 0:** op amp is driving.
[00:22:51:650 - 00:22:52:550] **Speaker 0:** Another circuit.
[00:22:53:790 - 00:22:55:650] **Speaker 0:** And then it cascades all the way along.
[00:23:14:219 - 00:23:15:500] **Speaker 0:** You can get instability.
[00:23:24:719 - 00:23:27:079] **Speaker 0:** It's changing the whole dynamics of the.
[00:23:29:760 - 00:23:32:880] **Speaker 0:** You, you're putting in an extra signal that's, that's fluctuating
[00:23:32:880 - 00:23:34:520] **Speaker 0:** and it's messing with the IPA.
[00:23:36:329 - 00:23:38:449] **Speaker 0:** And you can get instability like I discussed in the
[00:23:38:449 - 00:23:39:430] **Speaker 0:** uh other slide.
[00:23:40:459 - 00:23:43:709] **Speaker 0:** When you're changing the dynamics, you get resonances, all sorts
[00:23:43:709 - 00:23:44:609] **Speaker 0:** of bad things happen.
[00:23:46:250 - 00:23:48:979] **Speaker 0:** You don't want to be taking any fluctuations from the
[00:23:48:979 - 00:23:50:300] **Speaker 0:** source straight into the op amp.
[00:23:53:790 - 00:23:55:150] **Speaker 0:** Just these are.
[00:24:00:050 - 00:24:01:329] **Speaker 0:** High pass orders.
[00:24:10:489 - 00:24:14:349] **Speaker 0:** And basically the cutoff frequencies.
[00:24:16:239 - 00:24:21:099] **Speaker 0:** Usually Much smaller.
[00:24:23:479 - 00:24:24:939] **Speaker 0:** In the signal frequency.
[00:24:27:530 - 00:24:29:349] **Speaker 0:** Because that's one thing you don't want to have.
[00:24:31:069 - 00:24:34:869] **Speaker 0:** A voltage bias from your signal, you don't want that
[00:24:34:869 - 00:24:36:430] **Speaker 0:** going into the op amp because that's going to cause
[00:24:36:430 - 00:24:37:849] **Speaker 0:** problems with the biassing obviously.
[00:24:38:770 - 00:24:41:329] **Speaker 0:** So you want to have a high pass philtre which
[00:24:41:329 - 00:24:43:770] **Speaker 0:** stops that DC from getting through.
[00:24:46:640 - 00:24:48:739] **Speaker 0:** But you want to have the cutoff.
[00:24:49:199 - 00:24:50:520] **Speaker 0:** You don't want to be attenuating your signal.
[00:24:50:599 - 00:24:53:739] **Speaker 0:** So you've got to make sure that the cutoff frequency
[00:24:53:739 - 00:24:56:719] **Speaker 0:** is much smaller than the signal frequency, which is coming
[00:24:56:719 - 00:24:57:719] **Speaker 0:** in from the VM.
[00:25:01:989 - 00:25:05:369] **Speaker 0:** There's a DC offset.
[00:25:06:410 - 00:25:07:869] **Speaker 0:** That you can remove here as well.
[00:25:11:869 - 00:25:14:369] **Speaker 0:** Case of some offset that comes into the output.
[00:25:15:000 - 00:25:16:760] **Speaker 0:** And then it'll be fed back into the input.
[00:25:17:199 - 00:25:18:380] **Speaker 0:** You can remove it here.
[00:25:28:609 - 00:25:30:430] **Speaker 0:** So yeah, we want to try and get a better
[00:25:30:430 - 00:25:32:290] **Speaker 0:** supply noise rejection.
[00:25:33:150 - 00:25:44:560] **Speaker 0:** And here And so, as you'd expect, you could, Simply
[00:25:44:560 - 00:25:45:500] **Speaker 0:** add a low pass philtre.
[00:25:46:189 - 00:25:47:500] **Speaker 0:** Add some capacitors.
[00:25:49:810 - 00:25:51:459] **Speaker 0:** Put a capacitor in there.
[00:25:53:500 - 00:25:56:579] **Speaker 0:** And you can help the situation.
[00:25:56:660 - 00:26:00:739] **Speaker 0:** You also want to have Another resistance because there's actually
[00:26:00:739 - 00:26:04:010] **Speaker 0:** there's a Impedance matching, that's another issue.
[00:26:05:290 - 00:26:08:479] **Speaker 0:** You always want to have impedance matching on inputs into
[00:26:08:479 - 00:26:11:410] **Speaker 0:** the into an op amp, because if they're not matched
[00:26:11:410 - 00:26:13:890] **Speaker 0:** properly, then you can get further problems with biassing.
[00:26:14:469 - 00:26:16:349] **Speaker 0:** And then it can then you start clipping the signals
[00:26:16:349 - 00:26:19:189] **Speaker 0:** and then it creates problems, so.
[00:26:20:979 - 00:26:25:180] **Speaker 0:** That's one of the key design considerations for OEMs.
[00:26:26:500 - 00:26:28:339] **Speaker 0:** And that's what I often ask in the exam as
[00:26:28:339 - 00:26:28:599] **Speaker 0:** well.
[00:26:33:949 - 00:26:35:989] **Speaker 0:** And uh of course you want to better improve your
[00:26:35:989 - 00:26:36:829] **Speaker 0:** PCB layout.
[00:26:36:939 - 00:26:38:829] **Speaker 0:** Like you if you if you can get it at
[00:26:38:829 - 00:26:41:989] **Speaker 0:** source, if you can have, if your supply, for example,
[00:26:42:150 - 00:26:44:449] **Speaker 0:** doesn't have any fluctuations, of course, there's no problem.
[00:26:45:859 - 00:26:48:819] **Speaker 0:** But I'm assuming you've already got the best PCB you
[00:26:48:819 - 00:26:51:099] **Speaker 0:** can for your, you know, your, your power source.
[00:26:51:140 - 00:26:54:099] **Speaker 0:** You've got, got that nailed down nicely.
[00:26:55:050 - 00:26:58:010] **Speaker 0:** Then there'll still be some noise, so you want a
[00:26:58:010 - 00:26:58:510] **Speaker 0:** better.
[00:26:59:489 - 00:27:04:969] **Speaker 0:** Um, improve the stability independent of whether you've got a
[00:27:04:969 - 00:27:06:390] **Speaker 0:** good layout in your PCB.
[00:27:09:109 - 00:27:11:390] **Speaker 0:** And so yep, we had a low pass voter here.
[00:27:18:020 - 00:27:20:979] **Speaker 0:** And you can that voltage from the source, the fluctuation
[00:27:20:979 - 00:27:24:180] **Speaker 0:** from the source here is low pass filtered.
[00:27:26:010 - 00:27:27:880] **Speaker 0:** Through here and with the C2.
[00:27:30:939 - 00:27:34:859] **Speaker 0:** But we have added an additional uh impedance in here
[00:27:34:859 - 00:27:36:459] **Speaker 0:** so we can match the impedances.
[00:27:36:540 - 00:27:37:619] **Speaker 0:** That's why I've added this.
[00:27:38:020 - 00:27:41:420] **Speaker 0:** There's no guarantee that well this year won't be in
[00:27:41:420 - 00:27:42:109] **Speaker 0:** it won't be in.
[00:27:43:469 - 00:27:45:849] **Speaker 0:** Yeah, it won't be matching the impedance necessarily.
[00:27:46:890 - 00:27:50:250] **Speaker 0:** These two resistors won't be matching the input pedant into
[00:27:50:250 - 00:27:50:589] **Speaker 0:** here.
[00:27:51:670 - 00:27:53:489] **Speaker 0:** And so you add the extra resistor.
[00:27:54:380 - 00:27:57:150] **Speaker 0:** Here so that you can match the impedances that's this
[00:27:57:160 - 00:27:59:290] **Speaker 0:** this is two different changes of the C2 and the
[00:27:59:290 - 00:27:59:729] **Speaker 0:** RN.
[00:28:01:079 - 00:28:02:800] **Speaker 0:** That's how you've improved the circuit.
[00:28:08:530 - 00:28:10:930] **Speaker 0:** So low pass philtre, see how I've said it's 1/10
[00:28:10:930 - 00:28:12:489] **Speaker 0:** of the high pass philtre.
[00:28:15:410 - 00:28:17:280] **Speaker 0:** It's probably a minimum of 1/10.
[00:28:18:020 - 00:28:21:060] **Speaker 0:** You probably want to go like 1/15, 1/20, even, even
[00:28:21:060 - 00:28:22:140] **Speaker 0:** more, if you can.
[00:28:23:109 - 00:28:27:420] **Speaker 0:** But 1/10 would be the minimum where there's no.
[00:28:28:699 - 00:28:30:420] **Speaker 0:** You don't want to attenuate your signal, you see.
[00:28:30:540 - 00:28:31:060] **Speaker 0:** You don't want to.
[00:28:32:119 - 00:28:36:319] **Speaker 0:** Well you don't want Frequencies that are going to disrupt
[00:28:36:319 - 00:28:36:900] **Speaker 0:** the signal.
[00:28:39:479 - 00:28:40:550] **Speaker 0:** So that's a rule of thumb.
[00:28:52:420 - 00:28:55:270] **Speaker 0:** You don't want them combining with your VN.
[00:28:57:130 - 00:28:59:030] **Speaker 0:** And then going into that positive.
[00:29:00:319 - 00:29:17:150] **Speaker 0:** And put the So if we go into a say
[00:29:17:150 - 00:29:18:609] **Speaker 0:** a low pass philtre design.
[00:29:20:040 - 00:29:21:099] **Speaker 0:** Transfer function.
[00:29:25:079 - 00:29:38:810] **Speaker 0:** And let's, for example, say, Say that was your frequency.
[00:29:39:160 - 00:29:40:660] **Speaker 0:** Say this was the frequency here.
[00:29:41:780 - 00:29:42:619] **Speaker 0:** 100 Hz.
[00:29:45:339 - 00:29:47:459] **Speaker 0:** Probably be higher than that, but let's just say it's
[00:29:47:459 - 00:29:48:060] **Speaker 0:** 100 Hz.
[00:29:49:630 - 00:29:51:619] **Speaker 0:** So you have a signal freaks of 100 hits.
[00:29:52:880 - 00:29:55:699] **Speaker 0:** And you want to choose your cutoff frequency 1/10 of
[00:29:55:699 - 00:29:57:119] **Speaker 0:** that for the high-pass philtre.
[00:30:00:530 - 00:30:02:770] **Speaker 0:** And so that's 1/10 of that for the high pass
[00:30:02:770 - 00:30:03:270] **Speaker 0:** philtre.
[00:30:04:979 - 00:30:07:060] **Speaker 0:** But then you want your low pass philtre.
[00:30:07:500 - 00:30:09:780] **Speaker 0:** You don't want that to be hitting the pass band
[00:30:09:780 - 00:30:11:500] **Speaker 0:** of your high pass philtre, because this is the pass
[00:30:11:500 - 00:30:11:819] **Speaker 0:** band.
[00:30:13:900 - 00:30:16:969] **Speaker 0:** And You want to knock it off.
[00:30:17:119 - 00:30:19:500] **Speaker 0:** You want to attenuate it as much as possible.
[00:30:20:910 - 00:30:24:790] **Speaker 0:** So that the low part, the signal frequencies aren't going
[00:30:24:790 - 00:30:30:699] **Speaker 0:** to be Combining And so you would then design your
[00:30:30:699 - 00:30:32:670] **Speaker 0:** low pass fighter with another factor of 1, so it's
[00:30:32:670 - 00:30:35:229] **Speaker 0:** actually a factor of 100 from your signal frequency.
[00:30:42:890 - 00:30:46:180] **Speaker 0:** Only a rule of thumb, but it tends to work
[00:30:46:180 - 00:30:49:859] **Speaker 0:** if you can keep it in order of magnitude different.
[00:30:50:520 - 00:30:52:660] **Speaker 0:** And then by the time this sits here.
[00:30:54:119 - 00:30:58:750] **Speaker 0:** That's um attenuating a significant amount.
[00:30:59:979 - 00:31:01:569] **Speaker 0:** That would be injuring the signal range.
[00:31:04:410 - 00:31:04:939] **Speaker 0:** So yeah.
[00:31:05:989 - 00:31:11:310] **Speaker 0:** Ensures Frequencies in past band.
[00:31:14:380 - 00:31:16:339] **Speaker 0:** Of all of those philtres.
[00:31:19:810 - 00:31:21:770] **Speaker 0:** Are all attenuated.
[00:31:36:420 - 00:31:39:630] **Speaker 0:** And so we have the inverting case here, but we've
[00:31:39:630 - 00:31:41:849] **Speaker 0:** got a C2 which is knocking out the frequent.
[00:31:41:939 - 00:31:45:380] **Speaker 0:** This is the C2 here is knocking out the supply
[00:31:45:380 - 00:31:46:000] **Speaker 0:** noise here.
[00:31:48:959 - 00:31:51:969] **Speaker 0:** And you can choose.
[00:31:52:780 - 00:31:54:140] **Speaker 0:** You have got a bit of freedom here.
[00:31:54:219 - 00:31:57:000] **Speaker 0:** You can choose R2 or you can fix.
[00:31:57:800 - 00:32:00:479] **Speaker 0:** Fix one of these to try and match the impedances
[00:32:00:479 - 00:32:02:319] **Speaker 0:** and then vary the other one to get to get
[00:32:02:319 - 00:32:02:739] **Speaker 0:** the right.
[00:32:04:790 - 00:32:05:589] **Speaker 0:** Amplification.
[00:32:06:510 - 00:32:09:500] **Speaker 0:** So you've got, got, got freedom to be able to
[00:32:09:500 - 00:32:11:939] **Speaker 0:** match the impedances as well as having the right amplification
[00:32:11:939 - 00:32:12:180] **Speaker 0:** here.
[00:32:13:390 - 00:32:15:979] **Speaker 0:** And so when you go over to this one, You
[00:32:15:979 - 00:32:18:920] **Speaker 0:** want to minimise the input bias con errors where R2,
[00:32:20:209 - 00:32:21:880] **Speaker 0:** which is the input impedance, into here.
[00:32:22:619 - 00:32:24:719] **Speaker 0:** Should be half of that if these are the same.
[00:32:26:130 - 00:32:26:869] **Speaker 0:** We're here.
[00:32:27:819 - 00:32:32:410] **Speaker 0:** It's Both of these You're adding the two.
[00:32:34:030 - 00:32:35:550] **Speaker 0:** And that's how you do the biassing.
[00:32:42:579 - 00:32:43:989] **Speaker 0:** So that's that covered.
[00:32:45:609 - 00:32:46:829] **Speaker 0:** Let's look at the other one.
[00:32:52:479 - 00:32:55:680] **Speaker 0:** Clamp bi, so now we're gonna have a xenodiode in
[00:32:55:680 - 00:32:56:099] **Speaker 0:** here.
[00:33:00:140 - 00:33:02:079] **Speaker 0:** And this can help improve things a bit.
[00:33:03:430 - 00:33:04:969] **Speaker 0:** Because the issue here is you had.
[00:33:05:829 - 00:33:08:640] **Speaker 0:** Everything depending on the C2 and sometimes the C2 has
[00:33:08:640 - 00:33:10:949] **Speaker 0:** to be quite large.
[00:33:12:170 - 00:33:15:800] **Speaker 0:** Sometimes you have to make the C2 reasonably large to
[00:33:15:810 - 00:33:20:609] **Speaker 0:** ensure you, You get rid of that noise.
[00:33:36:500 - 00:33:38:079] **Speaker 0:** So the common mode rejection.
[00:33:39:910 - 00:33:44:890] **Speaker 0:** Tarly Dependent on.
[00:33:46:130 - 00:33:51:880] **Speaker 0:** The time constant RA over 2C2.
[00:33:52:890 - 00:33:54:390] **Speaker 0:** So you may need.
[00:33:56:400 - 00:33:57:640] **Speaker 0:** A large capacitor.
[00:34:02:199 - 00:34:03:270] **Speaker 0:** I spell that wrong sorry.
[00:34:06:130 - 00:34:06:430] **Speaker 0:** visitor.
[00:34:11:408 - 00:34:12:330] **Speaker 0:** So what are we doing here?
[00:34:12:419 - 00:34:16:000] **Speaker 0:** Well, another, uh, an alternative or an effective alternative.
[00:34:20:580 - 00:34:26:908] **Speaker 0:** is we're going to provide A VS over 2 biassing
[00:34:27:570 - 00:34:30:290] **Speaker 0:** instead of using the the resistor divider to get the
[00:34:30:290 - 00:34:32:310] **Speaker 0:** biassing right going into the op amp.
[00:34:33:519 - 00:34:35:979] **Speaker 0:** You can bias with a xenodiode.
[00:34:46:769 - 00:34:51:439] **Speaker 0:** Xenodiode Here's some quite nice properties.
[00:35:09:689 - 00:35:10:909] **Speaker 0:** Xena, Z for Xena.
[00:35:14:250 - 00:35:15:669] **Speaker 0:** It looks like this.
[00:35:24:020 - 00:35:25:439] **Speaker 0:** And suddenly dropped.
[00:35:30:179 - 00:35:31:320] **Speaker 0:** At the VZ.
[00:35:31:979 - 00:35:32:560] **Speaker 0:** So you get this.
[00:35:33:870 - 00:35:38:370] **Speaker 0:** this really rapid drop of the current.
[00:35:39:340 - 00:35:41:600] **Speaker 0:** For very small changes in the VZ.
[00:35:58:419 - 00:36:01:169] **Speaker 0:** And so if you've got a current between IZ Max
[00:36:01:169 - 00:36:02:120] **Speaker 0:** and IZ Min.
[00:36:02:760 - 00:36:04:879] **Speaker 0:** So you've got the negative, there's a bit of there's
[00:36:04:879 - 00:36:08:800] **Speaker 0:** backflow into the, to using it, using the diode in
[00:36:08:800 - 00:36:09:800] **Speaker 0:** the reverse way.
[00:36:11:000 - 00:36:12:310] **Speaker 0:** You're using the leakage current.
[00:36:15:479 - 00:36:18:919] **Speaker 0:** Then you can keep this voltage, well, that's negative BZ.
[00:36:23:010 - 00:36:28:050] **Speaker 0:** So conversely, if you, yeah, if you've got a voltage
[00:36:28:050 - 00:36:31:969] **Speaker 0:** that you're setting, which you can actually define by the
[00:36:31:969 - 00:36:37:060] **Speaker 0:** resistance into the The xenodiode.
[00:36:38:110 - 00:36:41:709] **Speaker 0:** Then if you get fluctuations in VZ, can you see
[00:36:41:709 - 00:36:45:580] **Speaker 0:** that Yeah, it's going to um.
[00:36:46:659 - 00:36:48:750] **Speaker 0:** Keep the current, yeah, it's not going to change much,
[00:36:48:989 - 00:36:51:929] **Speaker 0:** so the current can be Can be going up and
[00:36:51:929 - 00:36:56:120] **Speaker 0:** down and yeah, it's it's it's keeping the VZ really,
[00:36:56:169 - 00:36:56:830] **Speaker 0:** really constant.
[00:36:57:830 - 00:36:59:790] **Speaker 0:** Sorry, Chris, is that supposed to be IZ and then
[00:37:00:360 - 00:37:01:439] **Speaker 1:** just um 4 equal to?
[00:37:01:510 - 00:37:02:810] **Speaker 0:** Sorry, sorry, sorry, I made a mistake.
[00:37:03:800 - 00:37:04:439] **Speaker 0:** It was dumb.
[00:37:05:239 - 00:37:11:580] **Speaker 0:** Right Yeah, if you're keeping the current between here and
[00:37:11:580 - 00:37:14:860] **Speaker 0:** here, it's going to lock in, lock in the voltage
[00:37:14:860 - 00:37:15:939] **Speaker 0:** really accurately.
[00:37:17:709 - 00:37:20:330] **Speaker 0:** Right, the current can be changing quite a bit here,
[00:37:20:830 - 00:37:22:350] **Speaker 0:** and the voltage doesn't even change.
[00:37:23:719 - 00:37:25:560] **Speaker 0:** And this is one of the properties of a zenode.
[00:37:36:360 - 00:37:39:110] **Speaker 0:** So you can use a xenodota as a voltage regulator.
[00:37:41:399 - 00:37:42:419] **Speaker 0:** That's what's happening here.
[00:38:01:149 - 00:38:03:229] **Speaker 0:** So because the current can vary.
[00:38:03:909 - 00:38:06:389] **Speaker 0:** And the voltage is going to stay the same, it's
[00:38:06:389 - 00:38:07:129] **Speaker 0:** more stable.
[00:38:08:929 - 00:38:11:409] **Speaker 0:** So you're getting a more stable bias voltage going into
[00:38:11:409 - 00:38:11:719] **Speaker 0:** the OA.
[00:38:12:790 - 00:38:15:550] **Speaker 1:** So you still have to do um ends matching.
[00:38:15:729 - 00:38:17:169] **Speaker 0:** Yeah, absolutely have to.
[00:38:17:610 - 00:38:18:780] **Speaker 0:** So how does that work with the same.
[00:38:23:899 - 00:38:25:129] **Speaker 0:** So you are.
[00:38:26:399 - 00:38:28:399] **Speaker 0:** You've got the RN to do that, so you have
[00:38:28:399 - 00:38:31:439] **Speaker 0:** to add another resistor to the xenodiode.
[00:38:33:760 - 00:38:36:439] **Speaker 0:** And so that's why we've added the RN of 100
[00:38:36:439 - 00:38:36:959] **Speaker 0:** kilohms.
[00:38:37:000 - 00:38:39:100] **Speaker 0:** That was that was the secret technique there.
[00:38:40:000 - 00:38:43:760] **Speaker 0:** So basically add another resistor to the xenodide which will
[00:38:43:760 - 00:38:46:459] **Speaker 0:** then go into the positive side.
[00:38:47:770 - 00:38:50:560] **Speaker 0:** And then you can bias that with the, the two
[00:38:50:560 - 00:38:51:370] **Speaker 0:** resistors.
[00:38:56:570 - 00:38:57:860] **Speaker 0:** You have to have the RN.
[00:38:58:179 - 00:39:00:000] **Speaker 0:** You can't just have a xeno diode there.
[00:39:00:540 - 00:39:01:459] **Speaker 0:** Got to have the R in.
[00:39:01:580 - 00:39:02:219] **Speaker 0:** That's important.
[00:39:12:000 - 00:39:13:340] **Speaker 0:** BS voltage is VZ.
[00:39:30:639 - 00:39:33:040] **Speaker 0:** And so you need to choose the xenodiode.
[00:39:35:169 - 00:39:36:429] **Speaker 0:** That matches.
[00:39:38:310 - 00:39:39:850] **Speaker 0:** The VCC over 2.
[00:39:46:969 - 00:39:54:989] **Speaker 0:** Uh she's with us The xenodiide voltage can drop if
[00:39:54:989 - 00:39:57:729] **Speaker 0:** you have a power drop, and that's one of the
[00:39:57:729 - 00:39:58:610] **Speaker 0:** issues, so.
[00:40:02:429 - 00:40:04:129] **Speaker 0:** And more power is consumed as well.
[00:40:08:020 - 00:40:09:699] **Speaker 0:** Always trade-off, engineering trade-off.
[00:40:19:770 - 00:40:22:330] **Speaker 0:** Cos you're getting the you're getting the voltage, you get
[00:40:22:330 - 00:40:25:010] **Speaker 0:** a voltage drop of course from the xzema diode, so
[00:40:25:010 - 00:40:25:929] **Speaker 0:** you get a power loss.
[00:40:27:889 - 00:40:29:949] **Speaker 0:** Still need more power to overcome that power loss.
[00:40:31:129 - 00:40:32:330] **Speaker 0:** More power is consumed.
[00:40:33:129 - 00:40:35:290] **Speaker 0:** NFVS drops.
[00:40:37:379 - 00:40:41:060] **Speaker 0:** Suddenly, or substantially, I say substantially.
[00:40:44:919 - 00:40:48:020] **Speaker 0:** That's going to mean your biassing is going to be
[00:40:48:239 - 00:40:48:959] **Speaker 0:** interrupted.
[00:40:58:479 - 00:41:02:580] **Speaker 0:** And so you might get asymmetrical clipping or asymmetrical clipping.
[00:41:04:179 - 00:41:12:629] **Speaker 0:** Kak care On large signals So you have You've got
[00:41:12:629 - 00:41:15:169] **Speaker 0:** to be careful choosing the right xenodiode.
[00:41:17:270 - 00:41:20:270] **Speaker 0:** But once you got there Are still issues.
[00:41:20:679 - 00:41:22:739] **Speaker 0:** It can be temperature dependent as well.
[00:41:25:179 - 00:41:28:610] **Speaker 0:** But it is, it is another effective way of getting
[00:41:28:610 - 00:41:29:219] **Speaker 0:** way better.
[00:41:30:929 - 00:41:34:189] **Speaker 0:** Uh, attenuation of the voltage source.
[00:41:35:659 - 00:41:36:419] **Speaker 0:** Noise.
[00:41:38:469 - 00:41:39:520] **Speaker 0:** So that's the xenodi.
[00:41:41:479 - 00:41:43:840] **Speaker 0:** And then you are doing the impedance matching, as I
[00:41:43:840 - 00:41:45:719] **Speaker 0:** said before, by choosing your RN.
[00:41:46:709 - 00:41:49:629] **Speaker 0:** And then here you want to make sure R2 is
[00:41:49:629 - 00:41:50:429] **Speaker 0:** equal to RN.
[00:41:51:449 - 00:41:54:199] **Speaker 0:** Because R2 is the input impedance into this.
[00:41:56:419 - 00:41:58:739] **Speaker 0:** If you go over to here, you've got to add
[00:41:58:739 - 00:42:01:120] **Speaker 0:** the R in there, that's the input into the positive.
[00:42:02:590 - 00:42:04:409] **Speaker 0:** And then you've got to make sure the R2.
[00:42:06:120 - 00:42:08:949] **Speaker 0:** Is there, of course you've got your high pass philtre,
[00:42:09:159 - 00:42:11:149] **Speaker 0:** the C1 and the R1, that makes up your high
[00:42:11:149 - 00:42:11:860] **Speaker 0:** pass philtre.
[00:42:12:929 - 00:42:14:280] **Speaker 0:** For your.
[00:42:15:290 - 00:42:16:669] **Speaker 0:** Input signal.
[00:42:18:729 - 00:42:20:570] **Speaker 0:** One of the problems, another problem with the Xeno is
[00:42:20:570 - 00:42:22:290] **Speaker 0:** it actually creates quite a bit of noise.
[00:42:22:449 - 00:42:25:669] **Speaker 0:** The xenodiode does have a bit of noise.
[00:42:26:919 - 00:42:29:169] **Speaker 0:** Even though it's a great voltage regulator, it actually creates
[00:42:29:169 - 00:42:30:030] **Speaker 0:** its own noise.
[00:42:31:469 - 00:42:33:649] **Speaker 0:** And so you need to philtre that noise.
[00:42:34:479 - 00:42:37:510] **Speaker 0:** And you need a low-pass philtre to philtre the xeno
[00:42:37:510 - 00:42:37:760] **Speaker 0:** noise.
[00:42:37:879 - 00:42:39:399] **Speaker 0:** See here, this is the low-pass philtre.
[00:42:40:229 - 00:42:41:870] **Speaker 0:** And then you've got to make sure that it's like
[00:42:41:870 - 00:42:44:030] **Speaker 0:** a factor of 10, less than a factor of 10
[00:42:44:030 - 00:42:46:129] **Speaker 0:** already from the high pass philtre cutoff frequency.
[00:42:47:649 - 00:42:48:669] **Speaker 0:** There's the rule of thumb.
[00:42:49:010 - 00:42:52:729] **Speaker 0:** So you take your lowest cutoff frequency for the high-pass
[00:42:52:729 - 00:42:55:050] **Speaker 0:** philtres, and you make sure that you're a factor of
[00:42:55:050 - 00:42:58:649] **Speaker 0:** 10 less for your cutoff frequencies for the low-pass philtre.
[00:43:02:139 - 00:43:03:409] **Speaker 0:** And that's the type of exam question.
[00:43:03:500 - 00:43:07:050] **Speaker 0:** I mean, these are the exam questions where You have
[00:43:07:050 - 00:43:07:969] **Speaker 0:** to design.
[00:43:08:090 - 00:43:10:110] **Speaker 0:** You have to find the capacitive values.
[00:43:11:000 - 00:43:14:010] **Speaker 0:** That will give, well, you obviously choose a resistance to
[00:43:14:010 - 00:43:15:050] **Speaker 0:** get some sort of amplification.
[00:43:16:629 - 00:43:19:239] **Speaker 0:** And then you want to have certain cutoff frequencies and
[00:43:19:239 - 00:43:22:030] **Speaker 0:** you want to choose the capacitors or the resistors to
[00:43:22:030 - 00:43:23:030] **Speaker 0:** be able to achieve that.
[00:43:25:520 - 00:43:27:139] **Speaker 0:** And that's what most of these, and then you've got
[00:43:27:139 - 00:43:29:800] **Speaker 0:** to do the also make sure the bias currents are.
[00:43:31:120 - 00:43:32:280] **Speaker 0:** They, you know, they're minimised.
[00:43:32:399 - 00:43:35:899] **Speaker 0:** So the impedance matching and the choice of the frequencies
[00:43:36:290 - 00:43:40:580] **Speaker 0:** and the, um, given amplitude that you have to get
[00:43:40:580 - 00:43:41:199] **Speaker 0:** for the LPAM.
[00:43:41:280 - 00:43:43:719] **Speaker 0:** That's 3 things you've got to do in the exam.
[00:43:45:860 - 00:43:52:659] **Speaker 0:** OK, You'll get used to doing it.
[00:43:52:739 - 00:43:54:679] **Speaker 0:** Like every question's pretty much similar.
[00:44:05:050 - 00:44:10:489] **Speaker 0:** Now, a better, there are some new devices that are
[00:44:10:489 - 00:44:12:320] **Speaker 0:** now getting even better now.
[00:44:14:949 - 00:44:17:530] **Speaker 0:** Because yeah, you have the problem of the vat drop,
[00:44:18:010 - 00:44:18:429] **Speaker 0:** um.
[00:44:20:060 - 00:44:22:699] **Speaker 0:** And well, it's not really the vault drop, it's more
[00:44:22:699 - 00:44:26:550] **Speaker 0:** like just the sensitivity to And drift.
[00:44:27:610 - 00:44:30:729] **Speaker 0:** Yeah Of the xeno diet.
[00:44:31:860 - 00:44:33:860] **Speaker 0:** So these low dropout voters.
[00:44:34:929 - 00:44:42:449] **Speaker 0:** Reginitis A relatively new devices, like, not 20 years, you
[00:44:42:449 - 00:44:43:830] **Speaker 0:** know, 30 years.
[00:44:44:929 - 00:44:46:520] **Speaker 0:** Um, maybe 10 years.
[00:44:51:219 - 00:44:52:959] **Speaker 0:** 5 years, yeah, 5 to 10 years.
[00:44:54:189 - 00:44:59:020] **Speaker 0:** Um, Significantly, well, at least the, the, the, these have
[00:44:59:020 - 00:45:01:580] **Speaker 0:** been around for probably longer than 10, but the, the
[00:45:01:580 - 00:45:06:449] **Speaker 0:** new ones, yeah, very low volt drops because the old
[00:45:06:449 - 00:45:09:080] **Speaker 0:** ones, as I said here, had very high volt drops.
[00:45:12:570 - 00:45:13:969] **Speaker 0:** And the new ones.
[00:45:15:070 - 00:45:17:830] **Speaker 0:** Way less, so it means you get much more efficiency
[00:45:17:830 - 00:45:19:250] **Speaker 0:** because you're not losing on the power.
[00:45:29:419 - 00:45:34:800] **Speaker 0:** There's a really good one called the ADP 303.
[00:45:51:159 - 00:45:52:280] **Speaker 0:** Lower power loss.
[00:45:53:389 - 00:45:55:510] **Speaker 0:** That is obviously important.
[00:45:58:370 - 00:45:59:810] **Speaker 0:** For portable electronics.
[00:46:09:100 - 00:46:15:810] **Speaker 0:** We'll say Much lower noise.
[00:46:18:469 - 00:46:20:270] **Speaker 0:** Then the Xena.
[00:46:22:060 - 00:46:25:909] **Speaker 0:** In fact, it's so good you can probably not even
[00:46:25:909 - 00:46:26:580] **Speaker 0:** need.
[00:46:27:340 - 00:46:30:560] **Speaker 0:** a capacitor or a low pass philtre.
[00:46:31:770 - 00:46:33:899] **Speaker 0:** But still it was a good idea though.
[00:46:35:139 - 00:46:39:030] **Speaker 0:** To have a low-pass philtre because they, they still do
[00:46:39:030 - 00:46:42:590] **Speaker 0:** add noise, and there's still other noise sources that you'd
[00:46:42:590 - 00:46:43:550] **Speaker 0:** want to mitigate.
[00:46:44:810 - 00:46:48:889] **Speaker 0:** So even if you use an ADP 303, I'd still
[00:46:48:889 - 00:46:49:810] **Speaker 0:** probably recommend.
[00:46:50:770 - 00:46:53:040] **Speaker 0:** Putting a low pass philtre in your circuit.
[00:46:53:449 - 00:46:56:860] **Speaker 0:** You can probably get away without it, but I would
[00:46:56:860 - 00:46:58:340] **Speaker 0:** at least stick one in there, but then you can
[00:46:58:340 - 00:46:59:459] **Speaker 0:** have a much lower C2.
[00:47:00:439 - 00:47:01:070] **Speaker 0:** So it's great.
[00:47:05:780 - 00:47:11:199] **Speaker 0:** And so yeah, there's really low voltage great power saving.
[00:47:12:169 - 00:47:13:760] **Speaker 0:** Uh, but there is another, another approach.
[00:47:13:860 - 00:47:16:060] **Speaker 0:** You can use switch mode regulators.
[00:47:17:370 - 00:47:19:790] **Speaker 0:** And I'm not really going to go into those, but
[00:47:20:010 - 00:47:20:409] **Speaker 0:** yeah.
[00:47:41:679 - 00:47:44:030] **Speaker 0:** And I have asked that in an exam before.
[00:47:44:409 - 00:47:45:750] **Speaker 0:** It's just that the purpose.
[00:47:46:979 - 00:47:50:530] **Speaker 0:** Like the, the low pass builder has probably got a
[00:47:50:530 - 00:47:50:760] **Speaker 0:** different.
[00:47:51:780 - 00:47:56:800] **Speaker 0:** Uh Purpose Like as I said, you don't necessarily need
[00:47:56:800 - 00:47:59:780] **Speaker 0:** it, but there are secondary sources of noise even though
[00:47:59:780 - 00:48:03:830] **Speaker 0:** the This say the ADP 303 knocks out most of
[00:48:03:830 - 00:48:04:149] **Speaker 0:** the noise.
[00:48:04:189 - 00:48:05:149] **Speaker 0:** It's very low noise.
[00:48:05:270 - 00:48:05:729] **Speaker 0:** It's great.
[00:48:05:929 - 00:48:08:149] **Speaker 0:** Like it effectively is like a low pulse philtre like
[00:48:08:149 - 00:48:08:429] **Speaker 0:** it's.
[00:48:10:139 - 00:48:13:379] **Speaker 0:** It's probably still good to have maybe a small C2
[00:48:13:899 - 00:48:16:360] **Speaker 0:** and um and add a low-pass philtre.
[00:48:16:739 - 00:48:19:139] **Speaker 0:** So what you would do, which I've got in previous
[00:48:19:139 - 00:48:19:949] **Speaker 0:** exams.
[00:48:21:050 - 00:48:25:709] **Speaker 0:** I you would Get rid of this.
[00:48:27:520 - 00:48:33:610] **Speaker 0:** And Well, that's actually the, here, here, here, here, for
[00:48:33:610 - 00:48:34:070] **Speaker 0:** example.
[00:48:34:969 - 00:48:41:899] **Speaker 0:** Um, Because that's actually going to be the That'll be
[00:48:41:899 - 00:48:44:449] **Speaker 0:** using the It's my like I.
[00:48:46:110 - 00:48:48:129] **Speaker 0:** Yeah, so this one here actually there's no.
[00:48:48:830 - 00:48:55:540] **Speaker 0:** Um That's kind of acting probably like a, a low
[00:48:55:540 - 00:48:56:010] **Speaker 0:** pass philtre.
[00:48:57:129 - 00:48:58:300] **Speaker 0:** But yeah, that is.
[00:48:58:379 - 00:48:59:189] **Speaker 0:** That's the low passport.
[00:48:59:479 - 00:49:01:060] **Speaker 0:** And for some reason it's not there.
[00:49:02:719 - 00:49:08:270] **Speaker 0:** So, um, Well, you can, it's just It's fine.
[00:49:08:320 - 00:49:10:439] **Speaker 0:** I mean, you can look at the previous exam.
[00:49:10:560 - 00:49:12:719] **Speaker 0:** You can put a, you can do, it's just still
[00:49:12:719 - 00:49:13:919] **Speaker 0:** the same as the previous one.
[00:49:14:000 - 00:49:15:780] **Speaker 0:** So you can do a low pass photo with this
[00:49:16:199 - 00:49:17:520] **Speaker 0:** and a low pass fer with that.
[00:49:18:850 - 00:49:22:409] **Speaker 0:** But if you completely remove the the xenodiode, you can
[00:49:22:409 - 00:49:25:570] **Speaker 0:** replace it with One of these, and you see it
[00:49:25:570 - 00:49:26:350] **Speaker 0:** in the previous exam.
[00:49:27:649 - 00:49:29:969] **Speaker 0:** So yeah, for some reason in this particular one, I
[00:49:29:969 - 00:49:31:989] **Speaker 0:** didn't actually, oh no, here's a low pass forward here.
[00:49:33:000 - 00:49:33:889] **Speaker 0:** So that was done.
[00:49:34:360 - 00:49:36:080] **Speaker 0:** But you could do a low pass foot of design
[00:49:36:080 - 00:49:36:639] **Speaker 0:** for CN.
[00:49:37:780 - 00:49:40:989] **Speaker 0:** And that the purpose of this is to like philtre
[00:49:40:989 - 00:49:42:760] **Speaker 0:** out the xenon noise.
[00:49:45:010 - 00:49:45:969] **Speaker 0:** For some reason it was missing.
[00:49:46:020 - 00:49:46:790] **Speaker 0:** I'm not sure why.
[00:49:48:020 - 00:49:49:590] **Speaker 0:** Probably should stick that in eventually.
[00:49:50:840 - 00:49:52:820] **Speaker 0:** But I think I'm pretty much nearly done.
[00:49:54:270 - 00:49:55:500] **Speaker 0:** One minute to go.
[00:49:56:129 - 00:49:57:750] **Speaker 0:** I didn't even intend, I didn't even think I'd even
[00:49:57:750 - 00:49:58:760] **Speaker 0:** actually get this far.
[00:49:59:550 - 00:50:01:760] **Speaker 0:** But um I can at least start.
[00:50:03:989 - 00:50:06:409] **Speaker 0:** Because this is quite a clever little bootstrapping method.
[00:50:07:360 - 00:50:09:850] **Speaker 0:** Which is kind of a technique you could use in
[00:50:09:850 - 00:50:10:669] **Speaker 0:** your future.
[00:50:11:800 - 00:50:13:090] **Speaker 0:** Sort of projects and stuff.
[00:50:16:639 - 00:50:18:610] **Speaker 0:** So they often use bias that reduces the input impedance.
[00:50:18:689 - 00:50:22:120] **Speaker 0:** This is, this is a problem often with biassing resistors.
[00:50:27:320 - 00:50:30:939] **Speaker 0:** So current Can also flow.
[00:50:32:659 - 00:50:39:169] **Speaker 0:** It's a grand Through the bias resistance.
[00:50:42:729 - 00:50:44:629] **Speaker 0:** And therefore you're losing on.
[00:50:45:330 - 00:50:48:280] **Speaker 0:** You're not getting input impedance matching.
[00:50:49:300 - 00:50:51:040] **Speaker 0:** So let's just say and impedances.
[00:50:52:389 - 00:50:55:899] **Speaker 0:** I'm not matched As soon as you don't match impedances,
[00:50:55:979 - 00:50:57:439] **Speaker 0:** you always get a power loss.
[00:50:57:489 - 00:50:58:419] **Speaker 0:** It's less efficient.
[00:51:03:340 - 00:51:05:750] **Speaker 0:** So that is an issue with bioin resistors.
[00:51:07:689 - 00:51:09:739] **Speaker 0:** But then there's a clever way here, but I'm going
[00:51:09:739 - 00:51:12:679] **Speaker 0:** to probably call it because it's over time.
[00:51:13:820 - 00:51:17:219] **Speaker 0:** And I'll get onto this cool little clever technique on
[00:51:17:219 - 00:51:17:840] **Speaker 0:** Monday.
[00:51:21:699 - 00:51:22:389] **Speaker 0:** Thank you.
[00:51:24:659 - 00:51:24:979] **Speaker 0:** Yeah.
[00:51:28:629 - 00:51:28:639] **Speaker 0:** N.
[00:51:30:570 - 00:51:31:370] **Speaker 0:** Have a good weekend.
[00:51:33:219 - 00:51:37:409] **Speaker 0:** I Uh And then straight up I gotta fix it.
[00:51:39:939 - 00:51:40:139] **Speaker 1:** Is still.
[00:51:42:780 - 00:51:44:840] **Speaker 1:** Stop sweat sweat.
[00:51:50:340 - 00:51:51:739] **Speaker 1:** Change it from like the nice.
[00:51:54:780 - 00:51:56:290] **Speaker 1:** To wear masks.
[00:52:03:510 - 00:52:05:110] **Speaker 1:** I think he must have gone through a change.
[00:52:10:030 - 00:52:31:830] **Speaker 0:** I will come back Should be on echo again.
[00:52:33:169 - 00:52:33:620] **Speaker 0:** How's it going?
[00:52:33:780 - 00:52:34:129] **Speaker 0:** What's up?
[00:52:34:219 - 00:52:34:419] **Speaker 2:** Good.
[00:52:34:500 - 00:52:36:000] **Speaker 2:** I was just wondering, um.
[00:52:36:419 - 00:52:36:659] **Speaker 2:** Yeah.
[00:52:36:820 - 00:52:43:929] **Speaker 2:** In a few of the, Um, Was a bit earlier
[00:52:43:929 - 00:52:44:469] **Speaker 2:** than that?
[00:52:45:090 - 00:52:45:350] **Speaker 0:** Yep.
[00:52:46:340 - 00:52:47:790] **Speaker 0:** Um, that one?
[00:52:48:729 - 00:52:49:090] **Speaker 0:** That one.
[00:52:50:219 - 00:52:50:729] **Speaker 2:** Yeah, this one.
[00:52:50:850 - 00:52:53:709] **Speaker 2:** How does, how is the DC offset removed?
[00:52:54:830 - 00:52:55:379] **Speaker 2:** There.
[00:52:56:429 - 00:52:58:229] **Speaker 0:** That's what a capacitor does really.
[00:53:00:110 - 00:53:02:020] **Speaker 0:** It's a different it's a differentiator.
[00:53:02:070 - 00:53:03:959] **Speaker 0:** Do you know that capacity as a differentiator.
[00:53:05:260 - 00:53:05:479] **Speaker 0:** Yeah.
[00:53:05:600 - 00:53:10:500] **Speaker 0:** So a capacitor actually differentiates, um, the the voltage.
[00:53:11:830 - 00:53:12:389] **Speaker 0:** Oh, OK.
[00:53:12:669 - 00:53:15:830] **Speaker 0:** Right, so if you have an AC waveform and it's
[00:53:15:830 - 00:53:20:949] **Speaker 0:** got an offset, then that's how I see it.
[00:53:21:149 - 00:53:22:149] **Speaker 0:** Yeah, OK.
[00:53:23:679 - 00:53:28:860] **Speaker 2:** Um, Also, what, what is this?
[00:53:29:939 - 00:53:32:310] **Speaker 2:** Power supply like noise rejection thing, like.
[00:53:33:389 - 00:53:36:590] **Speaker 2:** Cause this is just, well, the voltage divider equation, and
[00:53:36:590 - 00:53:38:580] **Speaker 2:** then you plugged it into a Yeah.
[00:53:40:669 - 00:53:43:570] **Speaker 0:** Yeah, it's, it's just, it's just an amplification.
[00:53:43:889 - 00:53:45:129] **Speaker 0:** So it's just an amplification factor.
[00:53:45:250 - 00:53:47:270] **Speaker 0:** No, sorry, an attenuation factor.
[00:53:47:810 - 00:53:51:489] **Speaker 0:** It's like whatever the signal is, if you've got a,
[00:53:51:570 - 00:53:56:899] **Speaker 0:** if you've got a voltage signal and You pass it
[00:53:56:899 - 00:53:59:860] **Speaker 0:** through a resistor, it's obviously going to be divided by
[00:53:59:860 - 00:54:00:780] **Speaker 0:** the resistor, right?
[00:54:01:239 - 00:54:01:250] **Speaker 0:** Yeah.
[00:54:01:580 - 00:54:03:439] **Speaker 0:** So yeah, you just, so the voltage.
[00:54:04:439 - 00:54:06:000] **Speaker 0:** That's what the voltage divider does, right?
[00:54:06:120 - 00:54:09:179] **Speaker 0:** It just, and say it was a factor of 2.
[00:54:09:639 - 00:54:12:840] **Speaker 0:** What happens is whatever the bias of the voltage resistor
[00:54:12:840 - 00:54:14:520] **Speaker 0:** is, it divides by 2.
[00:54:14:840 - 00:54:18:949] **Speaker 0:** But that means that anything that's fluctuating is also divided
[00:54:18:949 - 00:54:19:360] **Speaker 0:** by 2.
[00:54:20:679 - 00:54:22:260] **Speaker 0:** Yeah, so that's what you mean by.
[00:54:24:000 - 00:54:26:300] **Speaker 0:** P so power supply, there is a power supply noise
[00:54:26:300 - 00:54:29:889] **Speaker 0:** reduction because it's actually reducing the supply.
[00:54:30:969 - 00:54:33:040] **Speaker 0:** Noise voltage by a factor of 2.
[00:54:33:860 - 00:54:36:699] **Speaker 0:** Right, OK, and so you can say that it has
[00:54:36:699 - 00:54:40:979] **Speaker 0:** a 6 dB power supply noise rejection and that's based
[00:54:40:979 - 00:54:43:820] **Speaker 2:** on the 20, 20 log 1 end of a half.
[00:54:44:060 - 00:54:44:739] **Speaker 0:** Yeah, right, OK.
[00:54:45:500 - 00:54:45:510] **Speaker 2:** Yeah.
[00:54:46:300 - 00:54:48:199] **Speaker 2:** And then also from earlier this morning.
[00:54:48:489 - 00:54:48:580] **Speaker 2:** Yeah.
[00:54:48:659 - 00:54:54:090] **Speaker 2:** Um, You know, the big like the noise something equation.
[00:54:54:810 - 00:54:55:850] **Speaker 0:** Yeah, oh yeah, yeah, yeah.
[00:54:55:969 - 00:54:57:969] **Speaker 0:** So there was the total noise, I think.
[00:54:58:610 - 00:54:59:280] **Speaker 0:** Um,

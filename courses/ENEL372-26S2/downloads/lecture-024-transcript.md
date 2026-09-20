# ENEL372-26S2 Lecture 24 native Echo transcript

Date: September 18, 2026 9:00am-9:55am
Transcript type: native Echo automated transcript.

[00:00:04:869 - 00:00:30:420] **Speaker 0:** And Oh.
[00:00:37:169 - 00:01:10:879] **Speaker 0:** Because you really tall Uh Oh Yeah sounds good.
[00:01:13:739 - 00:01:45:419] **Speaker 0:** uh I I do find these are like some of
[00:01:45:419 - 00:01:46:139] **Speaker 0:** the work for brand.
[00:01:49:080 - 00:01:49:089] **Speaker 0:** I.
[00:02:00:290 - 00:02:20:320] **Speaker 0:** Really this is I.
[00:02:27:669 - 00:02:28:210] **Speaker 0:** digital.
[00:02:31:119 - 00:02:31:320] **Speaker 0:** Yeah.
[00:02:43:110 - 00:03:06:190] **Speaker 0:** the The I Oh I.
[00:03:22:059 - 00:03:31:039] **Speaker 0:** Yeah Because So and the lectures are.
[00:03:32:080 - 00:03:32:089] **Speaker 0:** it.
[00:03:33:929 - 00:03:34:279] **Speaker 0:** Would you go?
[00:03:44:389 - 00:03:52:279] **Speaker 0:** Oh I To be fair, it's like 20.
[00:03:56:529 - 00:04:02:479] **Speaker 0:** I My, my, what's my best voice Kevin.
[00:04:07:360 - 00:04:43:230] **Speaker 0:** Yeah And I like For the next week.
[00:04:43:390 - 00:04:45:109] **Speaker 0:** I get points against that.
[00:04:45:630 - 00:04:47:049] **Speaker 0:** I was thinking about it as well.
[00:04:47:230 - 00:04:48:220] **Speaker 0:** I'm just like totally.
[00:04:50:130 - 00:04:53:279] **Speaker 0:** I I'm gonna go.
[00:04:55:230 - 00:04:55:239] **Speaker 0:** I.
[00:04:58:220 - 00:04:58:230] **Speaker 0:** Because.
[00:05:00:670 - 00:05:16:529] **Speaker 0:** That Uh Oh Right.
[00:05:18:239 - 00:05:18:920] **Speaker 1:** Hey, how come?
[00:05:20:369 - 00:05:21:420] **Speaker 1:** What's happened to that one?
[00:05:22:029 - 00:05:22:040] **Speaker 1:** Oh.
[00:05:24:779 - 00:06:00:619] **Speaker 1:** So Alright, we're up to full bridge, LCR load, well.
[00:06:13:739 - 00:06:15:799] **Speaker 1:** So that's the, the full.
[00:06:16:950 - 00:06:21:190] **Speaker 1:** Load, we've got inductor, capacitor, resistive load.
[00:06:23:829 - 00:06:27:709] **Speaker 1:** You'd normally have a capacitor in most rectifiers.
[00:06:28:820 - 00:06:30:980] **Speaker 1:** Like even in the modern, like in your computer, you'd
[00:06:30:980 - 00:06:35:230] **Speaker 1:** have a For your plug that converts the AC when
[00:06:35:230 - 00:06:38:269] **Speaker 1:** you plug into the mains, it'll have a capacitor.
[00:06:39:940 - 00:06:41:529] **Speaker 1:** But I wouldn't have an inductor.
[00:06:43:079 - 00:06:45:529] **Speaker 1:** You'd have a bridge rectifier of course in there.
[00:06:47:619 - 00:06:51:160] **Speaker 1:** But you could actually approximate, I think they use moss
[00:06:51:160 - 00:06:53:119] **Speaker 1:** vets and a whole lot of other techniques for.
[00:06:53:980 - 00:06:55:890] **Speaker 1:** Um, kind of filtering it out.
[00:06:57:579 - 00:07:00:809] **Speaker 1:** But you could, you can actually model even modern power
[00:07:00:809 - 00:07:01:890] **Speaker 1:** supplies.
[00:07:03:000 - 00:07:04:459] **Speaker 1:** With an inductor and a resistor.
[00:07:05:529 - 00:07:07:190] **Speaker 1:** Even though there's not a real inductor.
[00:07:10:260 - 00:07:13:829] **Speaker 1:** In this particular case, these are like really chunky diodes.
[00:07:13:950 - 00:07:15:489] **Speaker 1:** They're like the biggest diodes I could find.
[00:07:16:730 - 00:07:17:660] **Speaker 1:** And Lti Spice.
[00:07:19:670 - 00:07:23:869] **Speaker 1:** Uh So you could actually use AltiSpiceC to model like
[00:07:23:869 - 00:07:27:339] **Speaker 1:** a laptop computer charger if you wanted to.
[00:07:28:429 - 00:07:31:149] **Speaker 1:** And you could use an LCR load, and it actually
[00:07:31:149 - 00:07:32:869] **Speaker 1:** is reasonably good approximation.
[00:07:35:209 - 00:07:37:170] **Speaker 1:** Another advantage of LD Spice is you can kind of
[00:07:37:170 - 00:07:40:230] **Speaker 1:** lump complex dynamics into simpler models.
[00:07:41:269 - 00:07:43:809] **Speaker 1:** It's another kind of theme that I'm trying to.
[00:07:44:600 - 00:07:46:630] **Speaker 1:** Yeah Through to you.
[00:07:48:500 - 00:07:49:809] **Speaker 1:** Uh, I do remember.
[00:07:50:779 - 00:07:55:890] **Speaker 1:** Someone was Wondering if inductively.
[00:07:56:799 - 00:07:58:119] **Speaker 1:** Smooth is real.
[00:07:59:140 - 00:08:03:040] **Speaker 1:** Like, can you inductively smooth the circuit?
[00:08:03:250 - 00:08:04:970] **Speaker 1:** Does anyone think that's possible?
[00:08:07:980 - 00:08:09:359] **Speaker 1:** Can you do it in the real world?
[00:08:11:440 - 00:08:15:350] **Speaker 1:** Can you inductively All right, can you capacitively smooth?
[00:08:16:269 - 00:08:17:690] **Speaker 1:** A circuit in the real world.
[00:08:19:250 - 00:08:20:250] **Speaker 1:** You can't actually.
[00:08:21:239 - 00:08:25:359] **Speaker 1:** This is completely a mathematical fabrication.
[00:08:26:220 - 00:08:30:010] **Speaker 1:** It's not real You cannot have, yep.
[00:08:32:080 - 00:08:33:479] **Speaker 0:** Can you like make them close enough?
[00:08:35:640 - 00:08:36:039] **Speaker 1:** Yeah, yeah.
[00:08:36:200 - 00:08:38:080] **Speaker 1:** So when I say it's not real, you don't have
[00:08:38:080 - 00:08:40:440] **Speaker 1:** a real infinite capacitor, obviously, right?
[00:08:42:020 - 00:08:46:099] **Speaker 1:** Right, excellent question because um the reason you wanna do
[00:08:46:099 - 00:08:46:580] **Speaker 1:** that.
[00:08:47:330 - 00:08:48:989] **Speaker 1:** Because it's roughly true.
[00:08:50:479 - 00:08:53:679] **Speaker 1:** It's much easier to assume the capacitor is infinite.
[00:08:54:330 - 00:08:55:789] **Speaker 1:** And assume it's a finite value.
[00:08:56:640 - 00:08:58:760] **Speaker 1:** Because the math just pops out so much easier.
[00:08:58:919 - 00:09:01:640] **Speaker 1:** It's one of the real powerful techniques of assuming things
[00:09:01:640 - 00:09:02:919] **Speaker 1:** are capacitly smooth.
[00:09:03:400 - 00:09:05:559] **Speaker 1:** So yeah, so I didn't quite make that absolutely clear
[00:09:05:559 - 00:09:08:859] **Speaker 1:** that That concept is not real.
[00:09:10:510 - 00:09:11:580] **Speaker 1:** It's imaginary.
[00:09:11:729 - 00:09:17:989] **Speaker 1:** Like it's a fabricated mathematical trick to make calculations easier.
[00:09:19:900 - 00:09:21:590] **Speaker 1:** But it is a really interesting concept.
[00:09:21:690 - 00:09:22:770] **Speaker 1:** I, I think it's cool.
[00:09:23:390 - 00:09:24:450] **Speaker 1:** It's really helpful.
[00:09:25:419 - 00:09:26:419] **Speaker 1:** To be able to do that.
[00:09:26:900 - 00:09:28:140] **Speaker 1:** Same with inductively smooth.
[00:09:33:049 - 00:09:35:409] **Speaker 1:** Even something like this with such a large inductor, you
[00:09:35:409 - 00:09:37:799] **Speaker 1:** could possibly get away with assuming it was an infinite,
[00:09:38:369 - 00:09:42:669] **Speaker 1:** to some extent, but um, sometimes, Uh, no, actually, no,
[00:09:42:719 - 00:09:44:950] **Speaker 1:** you'd have to, um, first of all, you'd have to
[00:09:44:950 - 00:09:47:080] **Speaker 1:** check that it wasn't discontinuous current.
[00:09:49:450 - 00:09:50:719] **Speaker 1:** So that's um.
[00:09:52:719 - 00:09:54:049] **Speaker 1:** That's why the rule of thumb, you've got to be
[00:09:54:049 - 00:09:55:789] **Speaker 1:** careful, like, not always.
[00:09:58:090 - 00:10:04:210] **Speaker 1:** Well, um Like 100, was it 100 million West bag
[00:10:04:210 - 00:10:07:369] **Speaker 1:** with them it was like 100 mil, because 1 million
[00:10:07:369 - 00:10:12:250] **Speaker 1:** is 103, yeah, so 100 mL henry is 0.1, yeah.
[00:10:13:570 - 00:10:15:500] **Speaker 1:** Cause that's like 100 times 1 to -3, right?
[00:10:16:469 - 00:10:19:260] **Speaker 1:** So 100 millHenry is 0.1 henry.
[00:10:20:739 - 00:10:22:340] **Speaker 1:** So that's like a rule of thumb to say, oh,
[00:10:22:380 - 00:10:24:299] **Speaker 1:** that's a it's a massive inductor, like it could be
[00:10:24:299 - 00:10:26:580] **Speaker 1:** inductively smooth, but you just got to be careful with
[00:10:26:580 - 00:10:27:179] **Speaker 1:** that concept.
[00:10:28:659 - 00:10:31:900] **Speaker 1:** Um Yeah.
[00:10:32:229 - 00:10:34:190] **Speaker 1:** And this is the way I wanted to demonstrate this
[00:10:34:190 - 00:10:38:549] **Speaker 1:** particular example because it's actually showing Um, that it's just
[00:10:38:549 - 00:10:42:500] **Speaker 1:** continuous conduction, so the current's actually dropping off to zero
[00:10:42:500 - 00:10:42:820] **Speaker 1:** here.
[00:10:43:919 - 00:10:45:520] **Speaker 1:** And as you know with a solar car, that's a
[00:10:45:520 - 00:10:48:469] **Speaker 1:** bad thing if, if it's discontinuous conduction.
[00:10:49:070 - 00:10:49:909] **Speaker 1:** Remember, that's the whole point.
[00:10:49:960 - 00:10:53:039] **Speaker 1:** You were trying to design the conductor big enough so
[00:10:53:039 - 00:10:54:520] **Speaker 1:** that it was continuous conduction.
[00:10:55:359 - 00:10:58:119] **Speaker 1:** Cause if it's discontinuous, you get like transients and horrible
[00:10:58:119 - 00:10:58:780] **Speaker 1:** things happening.
[00:10:59:159 - 00:11:00:280] **Speaker 1:** Same thing in rectifiers.
[00:11:00:960 - 00:11:03:409] **Speaker 1:** You don't really want to have discontinuous conduction.
[00:11:08:289 - 00:11:11:469] **Speaker 1:** But I have got a very, very large resistor here.
[00:11:13:179 - 00:11:15:159] **Speaker 1:** And you know, in the solar car, like the motor
[00:11:15:159 - 00:11:17:590] **Speaker 1:** in the solar car was like what, 3 ohms.
[00:11:17:630 - 00:11:20:070] **Speaker 1:** This is 200 ohms, that's a big load.
[00:11:20:630 - 00:11:22:750] **Speaker 1:** That'd be a pretty massive motor.
[00:11:24:320 - 00:11:26:880] **Speaker 1:** That's another reason where you kind of have to, this
[00:11:26:880 - 00:11:29:900] **Speaker 1:** inductively smooth concept is not like perfect.
[00:11:30:479 - 00:11:31:599] **Speaker 1:** Like it kind of scales.
[00:11:31:679 - 00:11:34:780] **Speaker 1:** Like if you've got a massive, massive load like this,
[00:11:35:280 - 00:11:40:840] **Speaker 1:** then Maybe you need a slightly bigger inductor to make
[00:11:40:840 - 00:11:42:159] **Speaker 1:** sure that it's inductively smooth.
[00:11:43:229 - 00:11:45:909] **Speaker 1:** So it's only an approximate concept and it's really dependent
[00:11:45:909 - 00:11:46:710] **Speaker 1:** on the application.
[00:11:48:239 - 00:11:51:179] **Speaker 1:** And so what actually happens here, because it's discontinuous conduction.
[00:11:52:450 - 00:11:57:840] **Speaker 1:** During this period here, the arrow.
[00:11:58:619 - 00:12:00:479] **Speaker 1:** As I was saying, there's no current flow.
[00:12:03:219 - 00:12:04:280] **Speaker 1:** I can't fly.
[00:12:07:369 - 00:12:13:659] **Speaker 1:** So if there's no current flow, Well, that means, oh,
[00:12:13:909 - 00:12:15:530] **Speaker 1:** or sorry, the inductor.
[00:12:18:440 - 00:12:31:179] **Speaker 1:** Has no effect On the voyage More current, but in
[00:12:31:179 - 00:12:32:479] **Speaker 1:** terms of the scale of the voltage.
[00:12:35:030 - 00:12:36:989] **Speaker 1:** You get a short basically and then you get the
[00:12:36:989 - 00:12:37:729] **Speaker 1:** voltage.
[00:12:42:419 - 00:12:45:700] **Speaker 1:** Across RNC.
[00:12:46:679 - 00:12:51:859] **Speaker 1:** So that's what happens It's just not quite angled right.
[00:12:55:429 - 00:12:56:280] **Speaker 1:** That's a bit there.
[00:12:58:130 - 00:12:58:909] **Speaker 1:** Hold it straighter.
[00:13:01:450 - 00:13:05:130] **Speaker 1:** And so it, it's trying to, it's wanting to do
[00:13:05:130 - 00:13:05:750] **Speaker 1:** this.
[00:13:07:039 - 00:13:09:280] **Speaker 1:** But because the current goes to zero, it looks like
[00:13:09:280 - 00:13:11:200] **Speaker 1:** suddenly jumps, and this is an example of a transient
[00:13:11:200 - 00:13:14:000] **Speaker 1:** that occurs because you've got discontinuous conduction.
[00:13:17:179 - 00:13:19:219] **Speaker 1:** Probably in the real world you'd get all sorts of
[00:13:19:219 - 00:13:22:500] **Speaker 1:** horrible ringing and stuff cause it because here you've just
[00:13:22:500 - 00:13:25:140] **Speaker 1:** assume it's an inductor, there may be like a whole
[00:13:25:140 - 00:13:27:690] **Speaker 1:** lot of other induced capacitance inductors.
[00:13:28:520 - 00:13:32:719] **Speaker 1:** Uh, that mean that you wouldn't get this perfect result
[00:13:32:719 - 00:13:35:039] **Speaker 1:** in Altispice, so you may have to actually include other
[00:13:35:039 - 00:13:36:820] **Speaker 1:** inductances if you wanted to remodel the real world.
[00:13:38:349 - 00:13:39:590] **Speaker 1:** And you can see this is not, this is not
[00:13:39:590 - 00:13:42:469] **Speaker 1:** a great thing to be happening with your voltage waveform.
[00:13:46:719 - 00:13:48:219] **Speaker 1:** And then I modelled this.
[00:13:48:919 - 00:13:51:080] **Speaker 1:** Just something to be aware of in this because I've
[00:13:51:080 - 00:13:54:440] **Speaker 1:** used such big resistance and inductive and these types of
[00:13:54:440 - 00:13:59:159] **Speaker 1:** diodes, because I'm trying to get really Yeah, I just
[00:13:59:159 - 00:14:00:679] **Speaker 1:** wanted to get some.
[00:14:01:950 - 00:14:05:549] **Speaker 1:** Good, you know, really, the really high-end, really big diodes,
[00:14:05:799 - 00:14:08:719] **Speaker 1:** they could handle a lot of voltage and current flow.
[00:14:09:479 - 00:14:15:169] **Speaker 1:** If you simulate this, If you simulate.
[00:14:18:729 - 00:14:21:239] **Speaker 1:** Um, be careful.
[00:14:23:070 - 00:14:24:489] **Speaker 1:** With the tolerances.
[00:14:26:609 - 00:14:29:179] **Speaker 1:** Like I gave that rule of thumb 10 to -6,
[00:14:29:450 - 00:14:30:750] **Speaker 1:** you know, in Alti Spice.
[00:14:31:289 - 00:14:33:429] **Speaker 1:** That may not always, sometimes you got to kind of
[00:14:33:570 - 00:14:35:630] **Speaker 1:** tweak that a little bit, depends on the solver.
[00:14:37:369 - 00:14:40:840] **Speaker 1:** Uh And in some cases you may have to, in
[00:14:40:840 - 00:14:43:039] **Speaker 1:** this case here, I think I actually found you had
[00:14:43:039 - 00:14:44:250] **Speaker 1:** to set the gene in.
[00:14:45:630 - 00:14:47:010] **Speaker 1:** To be 18 to -4.
[00:14:47:049 - 00:14:50:409] **Speaker 1:** You don't really wanna don't know you don't really want
[00:14:50:409 - 00:14:53:849] **Speaker 1:** to um make Gin too low, but probably 10 to
[00:14:53:849 - 00:14:55:710] **Speaker 1:** -4 would be the lowest I'd go.
[00:14:56:859 - 00:14:58:859] **Speaker 1:** And it and it can sometimes give you much better
[00:14:58:859 - 00:14:59:520] **Speaker 1:** results.
[00:15:00:099 - 00:15:02:380] **Speaker 1:** You gotta remember that LD Spice is a simula it's
[00:15:02:380 - 00:15:03:630] **Speaker 1:** a simulation tool.
[00:15:04:609 - 00:15:06:039] **Speaker 1:** It has like Randolph errors.
[00:15:06:059 - 00:15:08:609] **Speaker 1:** It's got like problems like when it's doing the ODE
[00:15:08:609 - 00:15:09:010] **Speaker 1:** solving.
[00:15:09:210 - 00:15:11:409] **Speaker 1:** I don't know if you've done any ODE like differential
[00:15:11:409 - 00:15:14:289] **Speaker 1:** equation courses or numerics in maths or anything.
[00:15:14:409 - 00:15:16:090] **Speaker 1:** Um, I don't think you have to do that for
[00:15:16:090 - 00:15:18:090] **Speaker 1:** engineering, but you may have touched on it a little
[00:15:18:090 - 00:15:20:489] **Speaker 1:** bit, like with the Euler method and things.
[00:15:20:849 - 00:15:21:890] **Speaker 1:** There's the Rangakata methods.
[00:15:21:940 - 00:15:24:280] **Speaker 1:** There's all these different methods for doing numerical solving of
[00:15:24:280 - 00:15:27:070] **Speaker 1:** ODE uh ODEs, and they have error corrections, and they,
[00:15:27:409 - 00:15:30:679] **Speaker 1:** sometimes they get stuck if there's some big, Jump like
[00:15:30:679 - 00:15:33:000] **Speaker 1:** this, you know, some transient, and he.
[00:15:33:630 - 00:15:36:739] **Speaker 1:** Um, and LT Spies hasn't got the, the world's best
[00:15:37:280 - 00:15:38:099] **Speaker 1:** RDE solver.
[00:15:39:099 - 00:15:42:099] **Speaker 1:** It's OK, it's pretty good, but it's, there's far better
[00:15:42:099 - 00:15:42:799] **Speaker 1:** ones available.
[00:15:46:119 - 00:15:48:280] **Speaker 1:** So you may get better results in MATLAB or, or
[00:15:48:280 - 00:15:50:039] **Speaker 1:** some other tools.
[00:15:51:159 - 00:15:53:179] **Speaker 1:** So anyway, that's just that particular case.
[00:15:56:320 - 00:15:58:559] **Speaker 1:** And it is, I'm sort of moving somewhere with this.
[00:15:58:679 - 00:15:59:500] **Speaker 1:** Like I want.
[00:16:01:080 - 00:16:03:729] **Speaker 1:** I kind of want to choose the right inductor size,
[00:16:03:849 - 00:16:06:690] **Speaker 1:** but not too large, but enough so that I can
[00:16:06:690 - 00:16:08:770] **Speaker 1:** remove this problem of the discontinuous conduction.
[00:16:11:450 - 00:16:14:239] **Speaker 1:** And by the way, I'm assuming 0.
[00:16:16:270 - 00:16:18:349] **Speaker 1:** Uh, sauce and ducklings.
[00:16:22:049 - 00:16:22:630] **Speaker 1:** So yeah.
[00:16:22:969 - 00:16:26:190] **Speaker 1:** So just before I start getting into the inductor sizing,
[00:16:26:750 - 00:16:27:869] **Speaker 1:** that's what I wanna do today.
[00:16:28:580 - 00:16:30:010] **Speaker 1:** It's my main part of my legs today.
[00:16:32:659 - 00:16:37:799] **Speaker 1:** Uh, I wanna just Do a circuit analysis of it.
[00:16:38:690 - 00:16:41:679] **Speaker 1:** And then I want to do kind of a Summary
[00:16:41:679 - 00:16:44:159] **Speaker 1:** of the concepts that I've taught you up to this
[00:16:44:159 - 00:16:44:419] **Speaker 1:** point.
[00:16:49:510 - 00:16:51:739] **Speaker 1:** OK, let's have a look at this.
[00:16:52:150 - 00:16:53:679] **Speaker 1:** Cause then I'll be getting on to the actual uh
[00:16:53:679 - 00:16:54:250] **Speaker 1:** lecture.
[00:16:55:789 - 00:16:56:820] **Speaker 1:** 6 learning outcomes.
[00:17:00:010 - 00:17:01:909] **Speaker 1:** So the circuit analysis.
[00:17:02:760 - 00:17:04:780] **Speaker 1:** I'm not going to go through too much.
[00:17:06:509 - 00:17:13:759] **Speaker 1:** This Is Well, I'll say.
[00:17:15:280 - 00:17:24:050] **Speaker 1:** A derivation Is not examinable.
[00:17:29:959 - 00:17:31:800] **Speaker 1:** So normally the way I, if I go through my
[00:17:31:800 - 00:17:32:660] **Speaker 1:** lecture notes.
[00:17:33:739 - 00:17:35:459] **Speaker 1:** I think if I forget to tell you something that's
[00:17:35:459 - 00:17:37:180] **Speaker 1:** examinable, it's if if I always try and do that
[00:17:37:180 - 00:17:40:619] **Speaker 1:** with the learning outcomes, but throughout the notes, just assume
[00:17:40:619 - 00:17:42:439] **Speaker 1:** that it's examinable if I don't tell you otherwise.
[00:17:44:530 - 00:17:47:130] **Speaker 1:** And there are a few places in the notes that
[00:17:47:130 - 00:17:49:930] **Speaker 1:** I won't be examinable so I'll just, you know, I
[00:17:49:930 - 00:17:50:729] **Speaker 1:** always tell you that.
[00:17:52:479 - 00:17:54:530] **Speaker 1:** Um, I try to be specific.
[00:17:54:770 - 00:17:58:530] **Speaker 1:** Since my partner, unfortunately, I can't give you, I can't,
[00:17:58:609 - 00:18:00:770] **Speaker 1:** you can't build a real rectifier or do a lab
[00:18:00:770 - 00:18:04:640] **Speaker 1:** on brushless DC motor or something because there's just simply
[00:18:04:640 - 00:18:05:310] **Speaker 1:** not time.
[00:18:05:890 - 00:18:08:250] **Speaker 1:** So my part, unfortunately, is just the exam.
[00:18:08:380 - 00:18:10:119] **Speaker 1:** That's just my only assessment option.
[00:18:10:400 - 00:18:13:569] **Speaker 1:** There's literally no other options for me to, to test
[00:18:13:569 - 00:18:13:890] **Speaker 1:** you.
[00:18:14:609 - 00:18:16:630] **Speaker 1:** So that's why I'm gearing everything to the exam.
[00:18:18:550 - 00:18:20:270] **Speaker 1:** But that's, that's what I have to do.
[00:18:21:930 - 00:18:29:180] **Speaker 1:** Uh OK, so we have, what we're gonna do is.
[00:18:30:859 - 00:18:34:630] **Speaker 1:** In this particular case here, You've got this kind of
[00:18:34:959 - 00:18:36:420] **Speaker 1:** very high frequency input here.
[00:18:38:630 - 00:18:40:439] **Speaker 1:** I'm going to assume it's just not there for now.
[00:18:40:479 - 00:18:42:560] **Speaker 1:** I'm just going to assume it's like this, but what
[00:18:42:560 - 00:18:48:530] **Speaker 1:** actually happens is, as This effect is only caused by
[00:18:48:530 - 00:18:49:849] **Speaker 1:** the discontinuous conduction.
[00:18:50:199 - 00:18:52:739] **Speaker 1:** If you increase the inductor so so so that it's
[00:18:52:739 - 00:18:56:949] **Speaker 1:** no longer discontinuous, see this jump will disappear.
[00:18:58:739 - 00:19:00:339] **Speaker 1:** And if you get really, really close to it, the
[00:19:00:339 - 00:19:01:910] **Speaker 1:** jump will still be there, but it will be quite
[00:19:01:910 - 00:19:02:239] **Speaker 1:** small.
[00:19:03:910 - 00:19:06:430] **Speaker 1:** And then if you go really high, it's the whole
[00:19:06:430 - 00:19:08:729] **Speaker 1:** effect's going to disappear for the really high inductors.
[00:19:09:699 - 00:19:13:410] **Speaker 1:** So at the point where it's perfectly just at 0,
[00:19:13:500 - 00:19:15:800] **Speaker 1:** right, where it's just about to become continuous conduction.
[00:19:16:780 - 00:19:18:300] **Speaker 1:** It's going to look like this.
[00:19:21:650 - 00:19:24:489] **Speaker 1:** So I think I think it's a reasonable approximation, even
[00:19:24:489 - 00:19:26:910] **Speaker 1:** though you may be wanting to analyse both sides.
[00:19:27:890 - 00:19:30:250] **Speaker 1:** It's a reasonable approximation to assume that it's always like
[00:19:30:250 - 00:19:32:160] **Speaker 1:** this, because otherwise it's going to be horrible to try
[00:19:32:160 - 00:19:34:709] **Speaker 1:** and model that analytically.
[00:19:36:329 - 00:19:41:000] **Speaker 1:** So I This is gonna be approximate approximation.
[00:19:42:849 - 00:19:49:400] **Speaker 1:** So just keep in mind that For Oh less than.
[00:19:52:030 - 00:19:53:979] **Speaker 1:** L continuous, and that's like.
[00:19:54:800 - 00:20:07:640] **Speaker 1:** Conduct We If Continuous conduction.
[00:20:10:380 - 00:20:11:900] **Speaker 1:** Which like the smallest value.
[00:20:13:290 - 00:20:15:099] **Speaker 1:** Then it implies you are getting.
[00:20:18:839 - 00:20:22:579] **Speaker 1:** This Sorry, I've done it badly.
[00:20:24:920 - 00:20:25:760] **Speaker 1:** Can I try that again?
[00:20:26:770 - 00:20:28:510] **Speaker 1:** Cause it's actually going like that.
[00:20:29:810 - 00:20:35:569] **Speaker 1:** But then I Yeah, it kind of goes up like
[00:20:35:569 - 00:20:52:239] **Speaker 1:** that, and then That Yeah And I, and as I
[00:20:52:239 - 00:20:53:849] **Speaker 1:** say, I'm gonna be showing you a tutorial at some
[00:20:53:849 - 00:20:56:500] **Speaker 1:** stage where I'll take some exam questions.
[00:20:57:680 - 00:21:00:140] **Speaker 1:** And I'll show you how you can answer the exam
[00:21:00:140 - 00:21:01:579] **Speaker 1:** question using Alti Spice.
[00:21:03:140 - 00:21:04:770] **Speaker 1:** One of the exam questions could be.
[00:21:07:689 - 00:21:14:420] **Speaker 1:** Like Here's a circuit, LCLO with no no no um
[00:21:15:000 - 00:21:20:170] **Speaker 1:** no source conductance plot the voltage and current waveforms for
[00:21:20:170 - 00:21:25:510] **Speaker 1:** a For the case of discontinuous conduction, that might be
[00:21:25:510 - 00:21:26:270] **Speaker 1:** an exam question.
[00:21:27:650 - 00:21:30:250] **Speaker 1:** And so you can get, as your preparation for the
[00:21:30:250 - 00:21:30:890] **Speaker 1:** exam question.
[00:21:31:969 - 00:21:33:739] **Speaker 1:** You can get onto Alti Spice, and then you can
[00:21:33:739 - 00:21:35:780] **Speaker 1:** actually do it, and then see what it looks like.
[00:21:35:819 - 00:21:37:739] **Speaker 1:** And then copy the waveform you get from Alti Spice.
[00:21:37:780 - 00:21:39:339] **Speaker 1:** But I'll, I'll be showing you that a bit later
[00:21:39:339 - 00:21:40:359] **Speaker 1:** when I do a tutorial.
[00:21:40:859 - 00:21:41:500] **Speaker 1:** Possibly next week.
[00:21:41:540 - 00:21:44:619] **Speaker 1:** I'll have to check the um I'll put a post
[00:21:44:619 - 00:21:45:099] **Speaker 1:** on then.
[00:21:47:589 - 00:21:50:339] **Speaker 1:** Yeah, so that that's it's a really great tool for
[00:21:51:079 - 00:21:51:680] **Speaker 1:** study tool.
[00:21:55:660 - 00:21:57:650] **Speaker 1:** OK, so now I'm gonna, this is just more like
[00:21:57:650 - 00:22:00:420] **Speaker 1:** a mathematical um analysis.
[00:22:01:939 - 00:22:05:339] **Speaker 1:** So we have Yeah, I don't see, uh.
[00:22:06:890 - 00:22:09:069] **Speaker 1:** So what have we got here, I'm assuming it's this.
[00:22:10:609 - 00:22:12:729] **Speaker 1:** So the current, you just do Kutcher's laws, you just
[00:22:12:729 - 00:22:14:609] **Speaker 1:** go around Ven.
[00:22:16:819 - 00:22:22:150] **Speaker 1:** Minus L times I, and you go around there, then
[00:22:22:150 - 00:22:24:150] **Speaker 1:** you do the same for the other loop, you know
[00:22:24:150 - 00:22:32:319] **Speaker 1:** that the sum of the currents, And then Yeah, you
[00:22:32:319 - 00:22:35:020] **Speaker 1:** just plug that into here, get this.
[00:22:37:660 - 00:22:41:969] **Speaker 1:** So this one here What you do with it.
[00:22:45:439 - 00:22:46:699] **Speaker 1:** Do you want to go down to here?
[00:22:49:839 - 00:22:52:300] **Speaker 1:** Well, sorry, sorry, going from here to here.
[00:22:55:699 - 00:22:56:640] **Speaker 1:** How did I get this?
[00:23:00:790 - 00:23:02:089] **Speaker 1:** How do I go from here to here?
[00:23:02:579 - 00:23:03:589] **Speaker 1:** Well I differentiate.
[00:23:08:500 - 00:23:14:780] **Speaker 1:** One Sorry, actually, no, it was more like.
[00:23:16:060 - 00:23:16:819] **Speaker 1:** From here to here.
[00:23:19:680 - 00:23:22:000] **Speaker 1:** So if you take 1 and you differentiate it, you
[00:23:22:000 - 00:23:22:660] **Speaker 1:** get 5.
[00:23:29:359 - 00:23:30:660] **Speaker 1:** And you add these together.
[00:23:31:560 - 00:23:33:020] **Speaker 1:** Keep in mind this is not examinable.
[00:23:34:760 - 00:23:36:959] **Speaker 1:** You know 5 plus that and you can like cancel
[00:23:36:959 - 00:23:37:680] **Speaker 1:** our terms.
[00:23:38:640 - 00:23:40:640] **Speaker 1:** And then you can write it in this nice little
[00:23:40:640 - 00:23:41:229] **Speaker 1:** form here.
[00:23:43:930 - 00:23:46:209] **Speaker 1:** Well that looks like an LCR like almost like a
[00:23:46:209 - 00:23:47:390] **Speaker 1:** spring mass damper, right?
[00:23:48:920 - 00:23:50:359] **Speaker 1:** 2nd order differential equation.
[00:23:53:660 - 00:23:57:300] **Speaker 1:** We get And input voltage here.
[00:23:59:359 - 00:24:00:400] **Speaker 1:** But you're differentiating it.
[00:24:00:479 - 00:24:03:640] **Speaker 1:** Something funky is happening on the right-hand side, but you
[00:24:03:640 - 00:24:04:619] **Speaker 1:** could say this.
[00:24:05:619 - 00:24:08:469] **Speaker 1:** Is kind of like the input.
[00:24:10:739 - 00:24:13:959] **Speaker 1:** Into like a 2nd order linear differential equation.
[00:24:21:400 - 00:24:23:020] **Speaker 1:** The output's going to be current.
[00:24:25:489 - 00:24:31:660] **Speaker 1:** And so effectively, The LCR circuit is like a second-order
[00:24:31:660 - 00:24:32:719] **Speaker 1:** low-pass philtre.
[00:24:34:280 - 00:24:35:939] **Speaker 1:** It's acting like a philtre.
[00:24:36:400 - 00:24:41:589] **Speaker 1:** So the LCR I filtering the current according to a
[00:24:41:589 - 00:24:43:270] **Speaker 1:** 2nd order differential equation.
[00:24:45:579 - 00:24:46:459] **Speaker 1:** That's the current.
[00:24:47:170 - 00:24:48:349] **Speaker 1:** What happens to the voltage?
[00:24:50:849 - 00:24:52:339] **Speaker 1:** I'm not gonna go through the details, but if you
[00:24:52:339 - 00:24:54:400] **Speaker 1:** run through the math, you can see.
[00:24:56:060 - 00:24:58:680] **Speaker 1:** This, this is directly.
[00:25:00:060 - 00:25:01:530] **Speaker 1:** filtering out the VM.
[00:25:01:660 - 00:25:03:020] **Speaker 1:** As you'd kind of expect.
[00:25:03:540 - 00:25:06:819] **Speaker 1:** So the inductive is having an effect, which is interesting.
[00:25:06:900 - 00:25:13:339] **Speaker 1:** So the inductor is affecting Um, the output voltage because
[00:25:13:339 - 00:25:14:459] **Speaker 1:** it's in the equation.
[00:25:14:859 - 00:25:17:020] **Speaker 1:** This is totally mathematically looking at it.
[00:25:18:859 - 00:25:21:609] **Speaker 1:** And this is a 2nd, uh, this is a 2nd-order
[00:25:21:609 - 00:25:26:229] **Speaker 1:** low pass philtre for your VN which you already know
[00:25:26:229 - 00:25:27:229] **Speaker 1:** the capacitor does that.
[00:25:27:310 - 00:25:30:969] **Speaker 1:** The capacitor is a is a philtre of, of any
[00:25:30:969 - 00:25:31:989] **Speaker 1:** kind of change in voltage.
[00:25:32:030 - 00:25:34:030] **Speaker 1:** It's always going to smooth out any voltage.
[00:25:34:310 - 00:25:38:229] **Speaker 1:** That's why we say capacitively smoothing in, in, in terms
[00:25:38:229 - 00:25:39:050] **Speaker 1:** of voltage.
[00:25:42:099 - 00:25:45:949] **Speaker 1:** All right, so then Like what you've learned in control
[00:25:45:949 - 00:25:46:589] **Speaker 1:** systems.
[00:25:48:670 - 00:25:50:109] **Speaker 1:** You're going to have a transfer function.
[00:25:51:420 - 00:25:56:760] **Speaker 1:** And that's the transfer function formula for a passive second-order
[00:25:57:579 - 00:25:58:099] **Speaker 1:** philtre.
[00:25:58:699 - 00:26:03:660] **Speaker 1:** Passive, passive means there's no like feedback or like real-time
[00:26:03:660 - 00:26:04:239] **Speaker 1:** component.
[00:26:05:270 - 00:26:09:829] **Speaker 1:** Like, um, it's just sitting there not doing anything fancy.
[00:26:09:869 - 00:26:10:420] **Speaker 1:** I don't know.
[00:26:10:630 - 00:26:11:410] **Speaker 1:** It's passive.
[00:26:13:010 - 00:26:16:109] **Speaker 1:** And so you would fix the inductance and the capacitance.
[00:26:17:229 - 00:26:19:270] **Speaker 1:** And if you chose that, you can actually see that
[00:26:19:270 - 00:26:21:410] **Speaker 1:** this is acting like a low-pass philtre.
[00:26:21:910 - 00:26:23:469] **Speaker 1:** And the next part of the course, I'll show you
[00:26:23:469 - 00:26:26:430] **Speaker 1:** how you can have active philtres where you can approximate
[00:26:26:430 - 00:26:30:589] **Speaker 1:** the inductor by like some really interesting off amp circuit
[00:26:30:589 - 00:26:31:530] **Speaker 1:** realisations.
[00:26:33:099 - 00:26:34:420] **Speaker 1:** But that's, that's later.
[00:26:35:750 - 00:26:37:780] **Speaker 1:** And you should be reasonably familiar with this.
[00:26:38:550 - 00:26:41:550] **Speaker 1:** You should know that that is a like LCR philtre.
[00:26:42:760 - 00:26:44:920] **Speaker 1:** I hope you've done some filtering at some stage in
[00:26:44:920 - 00:26:46:579] **Speaker 1:** your careers.
[00:26:46:880 - 00:26:47:920] **Speaker 1:** If you haven't done.
[00:26:48:780 - 00:26:50:630] **Speaker 1:** You would have at least seen that in maths, and
[00:26:50:630 - 00:26:51:989] **Speaker 1:** you have done Laplace transforms.
[00:26:52:150 - 00:26:53:469] **Speaker 1:** You would have seen that somewhere.
[00:26:55:760 - 00:26:56:219] **Speaker 1:** All right.
[00:26:58:609 - 00:26:59:869] **Speaker 1:** So where I'm leading to.
[00:27:01:530 - 00:27:03:800] **Speaker 1:** So now I wanna kind of summarise everything with this
[00:27:03:800 - 00:27:04:189] **Speaker 1:** slide.
[00:27:04:239 - 00:27:06:140] **Speaker 1:** I kind of just drew this a few weeks ago.
[00:27:07:660 - 00:27:09:270] **Speaker 1:** And then I shoved it in the notes.
[00:27:09:969 - 00:27:10:339] **Speaker 1:** I and I.
[00:27:11:530 - 00:27:17:910] **Speaker 1:** Um Cause I, I always talk about the AC side
[00:27:18:250 - 00:27:20:290] **Speaker 1:** and the DC side and there's all these metrics.
[00:27:20:729 - 00:27:22:449] **Speaker 1:** So I've tried to make life a little bit easier
[00:27:22:449 - 00:27:22:949] **Speaker 1:** for you.
[00:27:24:390 - 00:27:27:829] **Speaker 1:** By putting everything onto one slide, the entire course up
[00:27:27:829 - 00:27:29:810] **Speaker 1:** to this point is on the slide.
[00:27:30:530 - 00:27:35:819] **Speaker 1:** In a way So I just want to check that
[00:27:35:819 - 00:27:37:140] **Speaker 1:** you can kind of see this.
[00:27:37:579 - 00:27:40:459] **Speaker 1:** So I have looked at a single a single phase.
[00:27:40:699 - 00:27:42:099] **Speaker 1:** So you've just got an AC, so you have a
[00:27:42:099 - 00:27:42:880] **Speaker 1:** sine wave.
[00:27:43:339 - 00:27:47:459] **Speaker 1:** Remember that sine wave could be from, uh, it could
[00:27:47:459 - 00:27:51:099] **Speaker 1:** be derived from the rotating of a like an alternator
[00:27:51:099 - 00:27:52:180] **Speaker 1:** on a 737.
[00:27:54:209 - 00:27:55:589] **Speaker 1:** Or it just might be the mains.
[00:27:56:930 - 00:27:58:880] **Speaker 1:** Single phase actually is is the mains.
[00:27:59:439 - 00:28:01:359] **Speaker 1:** So you have this AC wave form when you plug
[00:28:01:670 - 00:28:02:719] **Speaker 1:** into the mains there.
[00:28:04:849 - 00:28:07:089] **Speaker 1:** And then I've shown you this is like a rectifier.
[00:28:07:650 - 00:28:09:239] **Speaker 1:** This is like the full bridge rectifier.
[00:28:09:290 - 00:28:12:329] **Speaker 1:** You wouldn't use a half-way rectifier like if you design
[00:28:12:329 - 00:28:15:010] **Speaker 1:** like a computer charger or, you know, your charger for
[00:28:15:010 - 00:28:16:130] **Speaker 1:** your laptop.
[00:28:16:609 - 00:28:18:250] **Speaker 1:** You wouldn't be using a half-way bridge.
[00:28:18:290 - 00:28:20:010] **Speaker 1:** You'd always use a four-way bridge.
[00:28:20:869 - 00:28:22:750] **Speaker 1:** So that's why I'm always putting that, this is, this
[00:28:22:750 - 00:28:26:150] **Speaker 1:** is OK to say this is a generalised thing because
[00:28:26:150 - 00:28:27:170] **Speaker 1:** you'd always have that.
[00:28:28:089 - 00:28:29:550] **Speaker 1:** Now the output of that.
[00:28:30:890 - 00:28:32:449] **Speaker 1:** I've shown you is this.
[00:28:34:780 - 00:28:36:849] **Speaker 1:** But the output of that, which I've just done this
[00:28:36:849 - 00:28:40:050] **Speaker 1:** here, can be the input into an LCR cir LCR
[00:28:40:050 - 00:28:40:329] **Speaker 1:** philtre.
[00:28:40:380 - 00:28:43:119] **Speaker 1:** And I've shown you this, this is This is kind
[00:28:43:119 - 00:28:45:839] **Speaker 1:** of the output here, even though it says V in,
[00:28:45:910 - 00:28:46:969] **Speaker 1:** it's the output.
[00:28:47:900 - 00:28:49:199] **Speaker 1:** Of the rectifier.
[00:28:49:579 - 00:28:51:369] **Speaker 1:** So it's coming out, so your AC goes into your
[00:28:51:369 - 00:28:54:699] **Speaker 1:** rectifier, it's coming out into this, and then you have
[00:28:54:699 - 00:28:55:880] **Speaker 1:** an LCR philtre.
[00:28:57:520 - 00:28:59:560] **Speaker 1:** If the philtre was perfect, this would be just like
[00:28:59:560 - 00:28:59:880] **Speaker 1:** flat.
[00:29:00:609 - 00:29:01:140] **Speaker 1:** But it's not.
[00:29:01:219 - 00:29:03:119] **Speaker 1:** There's a little bit of ripple in the DC here.
[00:29:05:849 - 00:29:08:530] **Speaker 1:** And that that could be voltage, um, or it could
[00:29:08:530 - 00:29:11:130] **Speaker 1:** be actually current, but you normally think of this as
[00:29:11:130 - 00:29:11:949] **Speaker 1:** being voltage.
[00:29:13:729 - 00:29:15:750] **Speaker 1:** So that is like voltage.
[00:29:17:020 - 00:29:18:439] **Speaker 1:** In this particular case.
[00:29:21:209 - 00:29:25:449] **Speaker 1:** So when in all my exam questions related to rectifiers
[00:29:26:130 - 00:29:30:869] **Speaker 1:** are all either plot this waveform for this particular configuration
[00:29:30:869 - 00:29:32:930] **Speaker 1:** or work out this metric.
[00:29:34:750 - 00:29:39:810] **Speaker 1:** Like The the um effectiveness of the rectification ITE.
[00:29:43:510 - 00:29:45:569] **Speaker 1:** And so on the AC side.
[00:29:47:089 - 00:29:48:900] **Speaker 1:** These are the types, and I, I, I've looked through
[00:29:48:900 - 00:29:51:099] **Speaker 1:** the exam questions as well, and like, I don't think
[00:29:51:099 - 00:29:54:099] **Speaker 1:** this is like, this covers all the exam questions.
[00:29:55:520 - 00:29:57:219] **Speaker 1:** So the wave forms.
[00:29:58:569 - 00:30:02:489] **Speaker 1:** You have the AC voltage, the AC current draw.
[00:30:03:369 - 00:30:05:430] **Speaker 1:** And then you can, then you'd have a diode.
[00:30:05:890 - 00:30:10:130] **Speaker 1:** Even in the three-phase rectifier, you'd still have like um
[00:30:10:130 - 00:30:12:290] **Speaker 1:** one of the diodes associated with one of the phases.
[00:30:13:030 - 00:30:18:180] **Speaker 1:** And I call it AD Metrics Well, you want to
[00:30:18:180 - 00:30:20:420] **Speaker 1:** get the RMS of the current, you want the RMS
[00:30:20:420 - 00:30:21:520] **Speaker 1:** of the fundamental.
[00:30:22:060 - 00:30:23:699] **Speaker 1:** You've got the total homonic distortion.
[00:30:24:660 - 00:30:26:650] **Speaker 1:** Do you know what TPF is, anyone?
[00:30:28:359 - 00:30:29:040] **Speaker 1:** You want a kiss?
[00:30:31:079 - 00:30:32:319] **Speaker 1:** Yeah, total power factor.
[00:30:33:349 - 00:30:36:609] **Speaker 1:** I don't really talk or do that much, but I've.
[00:30:38:439 - 00:30:42:000] **Speaker 1:** It's possibly theoretically examinable, um, but it's, I don't think
[00:30:42:000 - 00:30:43:560] **Speaker 1:** it's very often in exam.
[00:30:43:640 - 00:30:45:880] **Speaker 1:** So this is, I'll just say very, and I'll tell
[00:30:45:880 - 00:30:48:849] **Speaker 1:** you if I, if I'm gonna Do it, but very
[00:30:48:849 - 00:30:49:579] **Speaker 1:** rarely.
[00:30:51:569 - 00:31:00:540] **Speaker 1:** Asked And exams So I probably won't ask it this
[00:31:00:540 - 00:31:00:630] **Speaker 1:** year.
[00:31:00:670 - 00:31:01:510] **Speaker 1:** I haven't written the exam.
[00:31:01:630 - 00:31:03:469] **Speaker 1:** I have to start writing the exam soon actually.
[00:31:04:260 - 00:31:07:979] **Speaker 1:** Um, So I'll know after I've written the exam, obviously,
[00:31:08:000 - 00:31:10:150] **Speaker 1:** whether I, whether I answer it, how I put it
[00:31:10:150 - 00:31:10:349] **Speaker 1:** in.
[00:31:11:319 - 00:31:13:869] **Speaker 1:** Uh, so they're the metrics on the AC side.
[00:31:13:930 - 00:31:15:890] **Speaker 1:** There's nothing really else on the AC side.
[00:31:15:969 - 00:31:17:849] **Speaker 1:** Like you might do an FFT, right?
[00:31:17:920 - 00:31:18:949] **Speaker 1:** But that's not really a metric.
[00:31:19:010 - 00:31:22:569] **Speaker 1:** An FFT is a means to get the THD, which
[00:31:22:569 - 00:31:23:380] **Speaker 1:** is the metric.
[00:31:24:500 - 00:31:26:979] **Speaker 1:** So this this methodologies and things, but here I'm just
[00:31:26:979 - 00:31:29:239] **Speaker 1:** doing the straight metrics and the waveforms and over here.
[00:31:29:540 - 00:31:30:800] **Speaker 1:** You have the DC side.
[00:31:31:339 - 00:31:33:489] **Speaker 1:** The DC side is mostly voltage.
[00:31:33:859 - 00:31:37:619] **Speaker 1:** You mostly care about current on the AC side and
[00:31:37:619 - 00:31:40:699] **Speaker 1:** you care about voltage metrics on the DC side.
[00:31:44:130 - 00:31:47:089] **Speaker 1:** And there's a few little things, like, and it means
[00:31:47:089 - 00:31:48:410] **Speaker 1:** I'll just put a small v and I need to
[00:31:48:410 - 00:31:49:650] **Speaker 1:** go through the notes to make sure I get all
[00:31:49:650 - 00:31:50:829] **Speaker 1:** this consistent notation.
[00:31:52:270 - 00:31:54:209] **Speaker 1:** Because when it's a time varying.
[00:31:54:969 - 00:31:57:810] **Speaker 1:** It's normally a small letter when it's time varying, and
[00:31:57:810 - 00:32:00:510] **Speaker 1:** it's a big letter when it's like a constant.
[00:32:01:939 - 00:32:03:859] **Speaker 1:** So these are the waveforms.
[00:32:04:650 - 00:32:07:170] **Speaker 1:** This here is quite a common one.
[00:32:08:579 - 00:32:09:219] **Speaker 1:** That's.
[00:32:10:170 - 00:32:11:489] **Speaker 1:** Like almost.
[00:32:12:750 - 00:32:17:300] **Speaker 1:** In every exam, like, I'm always asking you to to
[00:32:17:550 - 00:32:20:069] **Speaker 1:** plot the current through the inductor.
[00:32:21:900 - 00:32:23:579] **Speaker 1:** That's what you have to do in the uh in
[00:32:23:579 - 00:32:25:819] **Speaker 1:** the solar car project as well, like we really care
[00:32:25:819 - 00:32:26:680] **Speaker 1:** about the current.
[00:32:27:680 - 00:32:29:050] **Speaker 1:** That's flowing through the inductor.
[00:32:30:020 - 00:32:32:270] **Speaker 1:** We care about it both in the DC to DC
[00:32:32:270 - 00:32:34:670] **Speaker 1:** and we also really care about it in the AC
[00:32:34:670 - 00:32:35:569] **Speaker 1:** to DC case.
[00:32:39:359 - 00:32:42:109] **Speaker 1:** So you will very almost guaranteed to be asked in
[00:32:42:109 - 00:32:45:510] **Speaker 1:** the exam to plot the waveform through the inductor, the
[00:32:45:510 - 00:32:48:750] **Speaker 1:** current waveform through the inductor, even though this is the
[00:32:48:750 - 00:32:49:550] **Speaker 1:** DC side.
[00:32:50:469 - 00:32:51:630] **Speaker 1:** That's the only exception.
[00:32:51:949 - 00:32:53:569] **Speaker 1:** Other than that, it's mostly.
[00:32:55:010 - 00:32:59:880] **Speaker 1:** All the metrics are associated with um Mostly voltage.
[00:33:00:219 - 00:33:05:319] **Speaker 1:** The RMS, the average, and there's a few different, Terminologies.
[00:33:05:859 - 00:33:08:229] **Speaker 1:** Sometimes I say V on average, sometimes I say VD.
[00:33:08:430 - 00:33:09:630] **Speaker 1:** So just be aware of that.
[00:33:09:829 - 00:33:11:630] **Speaker 1:** And if you look at any textbook, they often vary
[00:33:11:630 - 00:33:12:250] **Speaker 1:** it as well.
[00:33:13:489 - 00:33:16:180] **Speaker 1:** And then we have our effectiveness of rectification with our
[00:33:16:560 - 00:33:17:949] **Speaker 1:** peak to peak voltage.
[00:33:18:729 - 00:33:20:449] **Speaker 1:** So, you, you, you did a peak to peak voltage
[00:33:20:449 - 00:33:21:329] **Speaker 1:** in the solar car.
[00:33:21:569 - 00:33:23:530] **Speaker 1:** You can do a peak to peak voltage in AC
[00:33:23:530 - 00:33:24:430] **Speaker 1:** to DC as well.
[00:33:26:609 - 00:33:30:069] **Speaker 1:** PP I have asked this once before an exam.
[00:33:31:890 - 00:33:36:369] **Speaker 1:** Uh, and then when you're doing your LC design, You
[00:33:36:369 - 00:33:37:869] **Speaker 1:** do also need to work out the peak.
[00:33:39:520 - 00:33:41:849] **Speaker 1:** In the 2nd harmonic, this is the 2nd harmonic.
[00:33:41:890 - 00:33:47:599] **Speaker 1:** I haven't really Didn't mention much about that, but 2
[00:33:48:140 - 00:33:50:459] **Speaker 1:** is 2nd harmonic.
[00:33:55:300 - 00:33:59:290] **Speaker 1:** Cause you, when you get rectification, it always doubles.
[00:33:59:459 - 00:34:03:380] **Speaker 1:** For a single-phase rectifier, it's, it's always doubling the frequency.
[00:34:03:619 - 00:34:04:199] **Speaker 1:** You see that?
[00:34:06:719 - 00:34:10:739] **Speaker 1:** Cause see how it goes Like there's one period, but
[00:34:10:739 - 00:34:12:349] **Speaker 1:** that gets flipped up when you go over here.
[00:34:12:448 - 00:34:15:168] **Speaker 1:** So effectively you're getting like double the frequency, so that's
[00:34:15:168 - 00:34:18:168] **Speaker 1:** why we always, most of the dynamics come from the
[00:34:18:168 - 00:34:20:367] **Speaker 1:** 2nd harmonic for the voltage.
[00:34:21:360 - 00:34:23:860] **Speaker 1:** And it's just that's just how the rectifier works.
[00:34:25:060 - 00:34:26:310] **Speaker 1:** But then don't get confused.
[00:34:26:540 - 00:34:28:449] **Speaker 1:** That's for the voltage analysis.
[00:34:31:479 - 00:34:34:698] **Speaker 1:** Um, when you do, if you're looking at this on
[00:34:34:698 - 00:34:35:668] **Speaker 1:** the DC side.
[00:34:36:117 - 00:34:38:089] **Speaker 1:** So the DC side, you're always doubling the frequencies.
[00:34:38:127 - 00:34:40:168] **Speaker 1:** You're always normally looking at the 2nd harmonic.
[00:34:40:357 - 00:34:42:569] **Speaker 1:** Except for for a 3-phase vectorfier, it'll be the 6th
[00:34:42:569 - 00:34:43:127] **Speaker 1:** harmonic.
[00:34:45:270 - 00:34:49:689] **Speaker 1:** But for the AC side, things can change.
[00:34:50:229 - 00:34:52:350] **Speaker 1:** So don't, it's not necessarily gonna be the second hole
[00:34:52:350 - 00:34:53:350] **Speaker 1:** on it for the AC side.
[00:34:53:429 - 00:34:56:510] **Speaker 1:** In fact, then how I showed you that for when
[00:34:56:510 - 00:34:58:550] **Speaker 1:** you get a square wave current you can actually approximate
[00:34:58:550 - 00:34:59:889] **Speaker 1:** it with the odd series.
[00:35:00:550 - 00:35:04:429] **Speaker 1:** Um, of all the sign terms, it's not obviously the
[00:35:04:429 - 00:35:05:620] **Speaker 1:** 2nd harmonic, is it?
[00:35:05:909 - 00:35:08:790] **Speaker 1:** It'll be the 3rd harmonic, 5th, 7th, 9th.
[00:35:09:389 - 00:35:12:739] **Speaker 1:** So I want you to completely separate your brain and
[00:35:12:739 - 00:35:14:790] **Speaker 1:** between the AC side is a different thing.
[00:35:16:189 - 00:35:21:959] **Speaker 1:** Different metrics, different properties, different, um, harmonics on the AC
[00:35:21:959 - 00:35:22:360] **Speaker 1:** side.
[00:35:22:840 - 00:35:25:620] **Speaker 1:** The DC side has got another fresh lot of different
[00:35:25:620 - 00:35:26:610] **Speaker 1:** harmonics.
[00:35:27:239 - 00:35:29:800] **Speaker 1:** So if you can just keep the AC and those
[00:35:29:800 - 00:35:32:800] **Speaker 1:** two things separated and know what the metrics are, then
[00:35:32:800 - 00:35:35:790] **Speaker 1:** you'll be able to hopefully understand the rectifier part of
[00:35:35:790 - 00:35:36:379] **Speaker 1:** my course.
[00:35:38:489 - 00:35:39:689] **Speaker 1:** I, I hope this is helpful.
[00:35:39:770 - 00:35:41:030] **Speaker 1:** I've put a bit of effort into that.
[00:35:46:939 - 00:35:47:699] **Speaker 1:** And that's it.
[00:35:47:949 - 00:35:53:419] **Speaker 1:** I'm now getting into sort of more practical design things
[00:35:53:419 - 00:35:55:979] **Speaker 1:** now for lecture 6, even though I've used up quite
[00:35:55:979 - 00:35:57:739] **Speaker 1:** a bit of time, but um.
[00:36:00:229 - 00:36:00:830] **Speaker 1:** Doesn't matter.
[00:36:02:949 - 00:36:06:979] **Speaker 1:** So I'm design inductance to maintain continuous conduction, so that
[00:36:06:979 - 00:36:08:600] **Speaker 1:** is certainly examinable.
[00:36:11:169 - 00:36:13:989] **Speaker 1:** Design capacity to provide a given voltage ripple.
[00:36:15:469 - 00:36:20:429] **Speaker 1:** It's, yeah, it's, I'd say it is examinable, but not
[00:36:20:429 - 00:36:20:949] **Speaker 1:** all the time.
[00:36:21:030 - 00:36:25:979] **Speaker 1:** It's probably I don't know how to describe that.
[00:36:26:050 - 00:36:27:560] **Speaker 1:** It is examinable, um.
[00:36:29:750 - 00:36:30:949] **Speaker 1:** But not always.
[00:36:34:449 - 00:36:37:370] **Speaker 1:** Describe the current flow sequence and LD of a three-phase,
[00:36:37:449 - 00:36:39:070] **Speaker 1:** that's definitely not examinable.
[00:36:45:290 - 00:36:46:840] **Speaker 1:** This is certainly examinable.
[00:36:50:830 - 00:36:52:790] **Speaker 1:** But I still think this is a good learning outcome
[00:36:52:790 - 00:36:55:550] **Speaker 1:** to get this 3, even though I'm not examining it.
[00:37:01:719 - 00:37:03:399] **Speaker 1:** So I'm going to separate these learning outcomes.
[00:37:03:719 - 00:37:04:580] **Speaker 1:** The first one.
[00:37:05:770 - 00:37:07:469] **Speaker 1:** Is single phase.
[00:37:10:139 - 00:37:10:600] **Speaker 1:** Rick the fire.
[00:37:13:500 - 00:37:17:409] **Speaker 1:** In this one, I'm getting to 3 phase rectifier, but
[00:37:17:409 - 00:37:19:790] **Speaker 1:** I don't think I'll get onto that, and I might
[00:37:19:969 - 00:37:20:790] **Speaker 1:** just touch it.
[00:37:27:149 - 00:37:30:110] **Speaker 1:** So there is my goals for the rest of this
[00:37:30:110 - 00:37:30:729] **Speaker 1:** lecture.
[00:37:31:110 - 00:37:31:949] **Speaker 1:** We'll see how we go.
[00:37:36:729 - 00:37:40:149] **Speaker 1:** Yeah So I'll just move that out.
[00:37:40:689 - 00:37:41:780] **Speaker 1:** Hopefully you've written most of that.
[00:37:45:570 - 00:37:47:030] **Speaker 1:** So we have an inductance design.
[00:37:49:370 - 00:37:52:290] **Speaker 1:** So that was a good rectifier, the bridge rectifier, very
[00:37:52:290 - 00:37:53:179] **Speaker 1:** common rectifier.
[00:37:53:979 - 00:37:56:149] **Speaker 1:** But we need to choose the DC side inductor that
[00:37:56:149 - 00:37:57:629] **Speaker 1:** maintains the continuous conduction.
[00:37:59:320 - 00:38:01:879] **Speaker 1:** So that that's the exception to the rule that mostly
[00:38:01:879 - 00:38:04:260] **Speaker 1:** things are voltage-related on the DC side.
[00:38:04:760 - 00:38:05:760] **Speaker 1:** This is an exception.
[00:38:06:120 - 00:38:08:520] **Speaker 1:** We do have to think about the current through the
[00:38:08:520 - 00:38:09:139] **Speaker 1:** inductor.
[00:38:11:760 - 00:38:14:820] **Speaker 1:** So the lowest non-DC frequency is second harmonic.
[00:38:15:239 - 00:38:18:280] **Speaker 1:** You should intuitively better understand that because you're just like
[00:38:18:280 - 00:38:20:600] **Speaker 1:** doubling, it's like 2 pulses per period.
[00:38:20:959 - 00:38:22:580] **Speaker 1:** Should make sense for a single phase.
[00:38:22:959 - 00:38:25:639] **Speaker 1:** You're getting double the frequency, second harmonic.
[00:38:28:939 - 00:38:30:699] **Speaker 1:** 2nd harmonic, 100 hits.
[00:38:31:820 - 00:38:32:560] **Speaker 1:** 100 Hz.
[00:38:33:909 - 00:38:35:110] **Speaker 1:** Because the mains.
[00:38:38:169 - 00:38:39:090] **Speaker 1:** It's 50 Hz.
[00:38:39:540 - 00:38:42:850] **Speaker 1:** For 60 Hz, then you would be 120, would be
[00:38:42:850 - 00:38:43:610] **Speaker 1:** the second home on it.
[00:38:44:419 - 00:38:46:590] **Speaker 1:** If it was a 737 and you had a single-phase
[00:38:46:590 - 00:38:49:189] **Speaker 1:** rectifier, it would go from 400 Hz, it would be
[00:38:49:189 - 00:38:50:010] **Speaker 1:** 800 Hz.
[00:38:51:449 - 00:38:52:729] **Speaker 1:** would be the 2nd harmonic.
[00:39:00:689 - 00:39:04:250] **Speaker 1:** So the second harmon 100 Hz, the second harmonic goes
[00:39:04:250 - 00:39:05:149] **Speaker 1:** into here.
[00:39:05:489 - 00:39:07:689] **Speaker 1:** And what's nice about a lot of these metrics is
[00:39:07:689 - 00:39:09:030] **Speaker 1:** it's frequency independent.
[00:39:12:300 - 00:39:15:370] **Speaker 1:** At least the formulas for for these.
[00:39:16:500 - 00:39:17:739] **Speaker 1:** Uh, frequency independent.
[00:39:20:879 - 00:39:23:320] **Speaker 1:** If I actually asked you the actual frequency that it's
[00:39:23:320 - 00:39:26:290] **Speaker 1:** doing, then obviously, yeah, you'd have to tell me what
[00:39:26:290 - 00:39:26:850] **Speaker 1:** it was.
[00:39:28:139 - 00:39:30:189] **Speaker 1:** But the Fouri coefficients and a lot of these metrics
[00:39:30:189 - 00:39:31:709] **Speaker 1:** are all frequency dependent.
[00:39:34:989 - 00:39:36:310] **Speaker 1:** Now I don't know if I want to go over
[00:39:36:310 - 00:39:36:389] **Speaker 1:** this.
[00:39:36:469 - 00:39:38:550] **Speaker 1:** I can briefly mention this again.
[00:39:41:229 - 00:39:46:949] **Speaker 1:** But This, this here is an even function.
[00:39:48:219 - 00:39:50:439] **Speaker 1:** Sorry, this isn't even function, that whole.
[00:39:52:830 - 00:39:54:350] **Speaker 1:** Well, this is even, but um.
[00:39:55:629 - 00:39:57:679] **Speaker 1:** That's just like your current.
[00:40:00:750 - 00:40:15:179] **Speaker 1:** Yeah Well, 999.
[00:40:16:000 - 00:40:18:189] **Speaker 1:** See this is a little bit, this lies to you
[00:40:18:189 - 00:40:18:969] **Speaker 1:** a little bit.
[00:40:19:510 - 00:40:21:709] **Speaker 1:** So this is the danger of using meth.
[00:40:27:899 - 00:40:29:500] **Speaker 1:** It's gonna explain this a little bit better.
[00:40:30:310 - 00:40:32:370] **Speaker 1:** It's just hit me that that's not.
[00:40:40:540 - 00:40:43:459] **Speaker 1:** It is, it's the same as before, but it was
[00:40:43:459 - 00:40:44:870] **Speaker 1:** the before was odd.
[00:40:45:189 - 00:40:45:929] **Speaker 1:** This is even.
[00:40:49:770 - 00:40:51:280] **Speaker 1:** Uh, that's like.
[00:40:52:000 - 00:40:53:540] **Speaker 1:** I don't know, we call it VN.
[00:40:54:629 - 00:40:59:090] **Speaker 1:** Of Cigna Cause of 2 sigma.
[00:41:04:820 - 00:41:09:760] **Speaker 1:** So VN Sigma, because it's all positive, cause it's it's
[00:41:09:760 - 00:41:12:679] **Speaker 1:** like a You know, full bridge rectifier.
[00:41:19:560 - 00:41:20:560] **Speaker 1:** That's 2 pi.
[00:41:21:270 - 00:41:22:110] **Speaker 1:** That's pi.
[00:41:22:629 - 00:41:25:310] **Speaker 1:** Remember I was trying to get you to understand the
[00:41:25:310 - 00:41:29:350] **Speaker 1:** generalised concept of symmetry and like odd and even, because
[00:41:29:350 - 00:41:32:149] **Speaker 1:** you were taught it around the zero point, but I
[00:41:32:149 - 00:41:34:459] **Speaker 1:** want you to take your brain and imagine that it's
[00:41:34:459 - 00:41:35:649] **Speaker 1:** like later on.
[00:41:36:929 - 00:41:39:479] **Speaker 1:** And it's just like any old vertical symmetry point.
[00:41:40:129 - 00:41:44:409] **Speaker 1:** So, can you understand that the VM is like an
[00:41:44:409 - 00:41:46:270] **Speaker 1:** even function about that line?
[00:41:48:000 - 00:41:51:100] **Speaker 1:** So you can completely, it's completely symmetrical about that line.
[00:41:52:010 - 00:41:55:669] **Speaker 1:** So you say that this is an even function relative
[00:41:55:669 - 00:42:00:389] **Speaker 1:** to This sigma equals pi vertical line if you want
[00:42:00:389 - 00:42:02:189] **Speaker 1:** it, you know, it's just, yeah.
[00:42:07:169 - 00:42:08:350] **Speaker 1:** So VN.
[00:42:09:209 - 00:42:11:129] **Speaker 1:** Is even function.
[00:42:12:429 - 00:42:15:479] **Speaker 1:** About The vertical.
[00:42:16:989 - 00:42:21:320] **Speaker 1:** Line Through pi.
[00:42:25:139 - 00:42:28:020] **Speaker 1:** So even function about the vertical line 3 pi.
[00:42:28:979 - 00:42:32:889] **Speaker 1:** Because it's even That means this is kind of repeated,
[00:42:32:899 - 00:42:34:820] **Speaker 1:** so the same area happens in the Fourie coefficient.
[00:42:34:939 - 00:42:36:300] **Speaker 1:** So you can just double it and then just do
[00:42:36:300 - 00:42:38:489] **Speaker 1:** the first bit from 0 to pi.
[00:42:39:379 - 00:42:40:739] **Speaker 1:** See how that works out really nicely.
[00:42:42:409 - 00:42:45:050] **Speaker 1:** Hope you can all see that little sleight of hand
[00:42:45:050 - 00:42:45:350] **Speaker 1:** there.
[00:42:47:639 - 00:42:48:959] **Speaker 1:** Mathematical sleight of hand.
[00:42:51:449 - 00:42:52:790] **Speaker 1:** And then once you've got that.
[00:42:54:030 - 00:42:57:530] **Speaker 1:** And of course, oh well, the B2 is 0.
[00:42:58:510 - 00:43:01:830] **Speaker 1:** Because when you have an even function and you're multiplying
[00:43:01:830 - 00:43:05:050] **Speaker 1:** an even function with an odd function, odd times even
[00:43:05:050 - 00:43:06:860] **Speaker 1:** equals odd.
[00:43:07:149 - 00:43:07:989] **Speaker 1:** Remember doing that?
[00:43:08:030 - 00:43:10:179] **Speaker 1:** Like odd times odd is even.
[00:43:10:310 - 00:43:11:639] **Speaker 1:** Even times even is even.
[00:43:11:830 - 00:43:12:330] **Speaker 1:** You know.
[00:43:13:310 - 00:43:15:810] **Speaker 1:** It's sort of like plus and minus sort of things.
[00:43:16:590 - 00:43:18:580] **Speaker 1:** So even times odd is odd.
[00:43:18:750 - 00:43:21:179] **Speaker 1:** But if you integrate a perfectly odd function over that
[00:43:21:179 - 00:43:22:530] **Speaker 1:** symmetry line, you get zero.
[00:43:22:909 - 00:43:25:129] **Speaker 1:** Cause it's the it's the negative on the other side.
[00:43:25:550 - 00:43:26:770] **Speaker 1:** So B2 is zero.
[00:43:30:389 - 00:43:38:370] **Speaker 1:** Yeah, since Um, Since V and.
[00:43:39:370 - 00:43:40:399] **Speaker 1:** Tom's cause.
[00:43:41:780 - 00:43:52:629] **Speaker 1:** To Sigma Gives 0 integral.
[00:43:56:310 - 00:43:58:540] **Speaker 1:** anyway, OK.
[00:44:00:239 - 00:44:02:399] **Speaker 1:** So then the peak, once you actually go through this
[00:44:02:399 - 00:44:03:959] **Speaker 1:** and you work this out, you can work out the
[00:44:03:959 - 00:44:06:719] **Speaker 1:** peak, value of the 2nd harmonic, and that's what the
[00:44:06:719 - 00:44:07:439] **Speaker 1:** value is.
[00:44:08:350 - 00:44:12:070] **Speaker 1:** So I've analytically derived what the peak value of the
[00:44:12:070 - 00:44:12:989] **Speaker 1:** 2nd harmonic.
[00:44:16:090 - 00:44:19:300] **Speaker 1:** And so with uh 230 volts, you can plug it
[00:44:19:300 - 00:44:21:820] **Speaker 1:** into here and you'll get a coefficient.
[00:44:22:300 - 00:44:25:330] **Speaker 1:** The actual coefficient is negative, but the peak value, you
[00:44:25:330 - 00:44:26:659] **Speaker 1:** know, you don't worry about the negative sign.
[00:44:28:389 - 00:44:31:330] **Speaker 1:** And so this is an approximation for the waveform.
[00:44:34:889 - 00:44:36:590] **Speaker 1:** That approximates.
[00:44:39:760 - 00:44:49:709] **Speaker 1:** The Using Only The 2nd harmonic And that's a pretty
[00:44:49:709 - 00:44:50:560] **Speaker 1:** good approximation.
[00:44:53:979 - 00:44:55:040] **Speaker 1:** It's not perfect.
[00:44:55:939 - 00:44:58:520] **Speaker 1:** But it's capturing just about the whole waveform.
[00:45:00:580 - 00:45:03:919] **Speaker 1:** So that's a really nice result that you can truncate
[00:45:04:219 - 00:45:06:419] **Speaker 1:** all those Fourier terms and just look at the very
[00:45:06:419 - 00:45:07:219] **Speaker 1:** first one.
[00:45:08:070 - 00:45:10:340] **Speaker 1:** And it's naturally capturing this.
[00:45:11:699 - 00:45:14:129] **Speaker 1:** Bridge this uh full bridge rectifier response.
[00:45:15:800 - 00:45:17:629] **Speaker 1:** OK.
[00:45:19:860 - 00:45:22:260] **Speaker 1:** Now that is actually really nice that you can do
[00:45:22:260 - 00:45:22:580] **Speaker 1:** that.
[00:45:24:070 - 00:45:26:729] **Speaker 1:** Because you can then do even more analytical calculations.
[00:45:28:629 - 00:45:29:830] **Speaker 1:** And that's the next page.
[00:45:31:810 - 00:45:31:820] **Speaker 1:** Right.
[00:45:36:830 - 00:45:39:010] **Speaker 1:** And in this case here, I am going to assume
[00:45:39:709 - 00:45:42:510] **Speaker 1:** a perfect world where it's inductively smooth, which you know
[00:45:42:510 - 00:45:43:949] **Speaker 1:** is actually not true in the real world, but we're
[00:45:43:949 - 00:45:45:909] **Speaker 1:** going to assume the capacitor is large enough that we
[00:45:45:909 - 00:45:46:649] **Speaker 1:** can assume this.
[00:45:47:600 - 00:45:51:500] **Speaker 1:** Um So then remember it's like.
[00:45:53:370 - 00:45:54:510] **Speaker 1:** Mathematical.
[00:45:59:060 - 00:46:07:770] **Speaker 1:** Assumption Not Exactly true.
[00:46:10:750 - 00:46:11:810] **Speaker 1:** In the real world.
[00:46:14:860 - 00:46:16:570] **Speaker 1:** But we're going to assume that sea goes to infinity,
[00:46:16:590 - 00:46:18:610] **Speaker 1:** and that becomes a constant voyage source.
[00:46:22:229 - 00:46:23:770] **Speaker 1:** So this is the equivalent circuit.
[00:46:26:449 - 00:46:27:709] **Speaker 1:** Of a rectifier.
[00:46:36:969 - 00:46:40:850] **Speaker 1:** So we can do Kirchhoff's laws, VN minus L times
[00:46:40:850 - 00:46:43:110] **Speaker 1:** I minus VD 0.
[00:46:43:939 - 00:46:46:040] **Speaker 1:** Remember that, that's just the main value.
[00:46:46:540 - 00:46:48:699] **Speaker 1:** It's one of those, and see it's a capital V.
[00:46:51:679 - 00:46:53:060] **Speaker 1:** Ah, see, I should have.
[00:46:53:479 - 00:46:54:080] **Speaker 1:** Should be a small V.
[00:46:57:780 - 00:46:59:699] **Speaker 1:** It's the problem when I get someone to type out
[00:46:59:699 - 00:47:00:219] **Speaker 1:** the notes.
[00:47:02:540 - 00:47:04:280] **Speaker 1:** Some little errors creep through.
[00:47:08:090 - 00:47:09:000] **Speaker 1:** Used to be a small v.
[00:47:11:889 - 00:47:14:330] **Speaker 1:** All right, so then you can solve for I, little
[00:47:14:330 - 00:47:15:830] **Speaker 1:** I, because it's a function of time.
[00:47:17:469 - 00:47:21:350] **Speaker 1:** And Uh, you know, I had a little note here
[00:47:21:350 - 00:47:25:850] **Speaker 1:** to say that this is 207.07 volts.
[00:47:27:149 - 00:47:27:469] **Speaker 1:** Yeah.
[00:47:29:229 - 00:47:30:669] **Speaker 1:** So then you get 1 over L.
[00:47:32:250 - 00:47:35:840] **Speaker 1:** Times this is just extracting what this is because you're
[00:47:35:840 - 00:47:38:389] **Speaker 1:** just subtracting the two, so this is nice like you're
[00:47:40:320 - 00:47:44:399] **Speaker 1:** What you're doing here is you've got this approximation.
[00:47:44:479 - 00:47:48:040] **Speaker 1:** So you just, this is the, the average, 207.07, and
[00:47:48:040 - 00:47:50:520] **Speaker 1:** you're subtracting that from the waveform, you just end up
[00:47:50:520 - 00:47:52:189] **Speaker 1:** getting left with the second harmonic.
[00:47:52:280 - 00:47:52:679] **Speaker 1:** That's it.
[00:47:52:760 - 00:47:54:989] **Speaker 1:** That's all that's left when you subtract the two.
[00:47:55:399 - 00:47:55:699] **Speaker 1:** See?
[00:47:55:790 - 00:47:56:100] **Speaker 1:** Yeah.
[00:47:58:159 - 00:47:59:340] **Speaker 1:** And then you can just integrate it.
[00:48:00:010 - 00:48:04:310] **Speaker 1:** And you can work out Approximately what the I2 is.
[00:48:04:659 - 00:48:06:219] **Speaker 1:** This is only an approximation.
[00:48:07:439 - 00:48:09:000] **Speaker 1:** So it's an approximation.
[00:48:12:510 - 00:48:13:649] **Speaker 1:** To the ripple current.
[00:48:18:729 - 00:48:21:409] **Speaker 1:** And then you can see that the peak is just
[00:48:21:409 - 00:48:22:050] **Speaker 1:** going to be.
[00:48:24:149 - 00:48:25:620] **Speaker 1:** That it's just like the.
[00:48:27:300 - 00:48:30:070] **Speaker 1:** What would be the impedance because it's too omega, you
[00:48:30:070 - 00:48:31:199] **Speaker 1:** know, that's just the impedance.
[00:48:46:229 - 00:48:47:610] **Speaker 1:** A 2/2 on the gore.
[00:48:49:550 - 00:48:50:350] **Speaker 1:** See this is.
[00:48:55:149 - 00:48:56:929] **Speaker 1:** That's your A2, which is from before.
[00:48:58:379 - 00:49:00:330] **Speaker 1:** And then you've got divide by 2 hours, so you're
[00:49:00:330 - 00:49:01:260] **Speaker 1:** getting your impedance there.
[00:49:02:209 - 00:49:02:820] **Speaker 1:** You this.
[00:49:03:800 - 00:49:06:520] **Speaker 1:** So yeah, the maths all comes out, so analytical mass
[00:49:06:520 - 00:49:07:840] **Speaker 1:** by making these assumptions.
[00:49:08:850 - 00:49:09:570] **Speaker 1:** So what does this mean?
[00:49:09:649 - 00:49:11:889] **Speaker 1:** Well, we've got a current current here.
[00:49:12:899 - 00:49:17:149] **Speaker 1:** The ripple Is the distance from the ID because there's
[00:49:17:149 - 00:49:18:909] **Speaker 1:** there's That's what it is.
[00:49:18:919 - 00:49:20:500] **Speaker 1:** It's the, if you look at the current.
[00:49:23:129 - 00:49:26:379] **Speaker 1:** And to get continuous conduction, we want to make sure
[00:49:26:379 - 00:49:27:959] **Speaker 1:** that this is not hitting 0.
[00:49:29:439 - 00:49:31:959] **Speaker 1:** So I2 peak must be less than ID.
[00:49:32:159 - 00:49:35:840] **Speaker 1:** So the distance here must be less than that.
[00:49:36:479 - 00:49:38:040] **Speaker 1:** But you've done that in your DC.
[00:49:38:159 - 00:49:40:000] **Speaker 1:** You should be familiar with this concept because you did
[00:49:40:000 - 00:49:41:219] **Speaker 1:** it in the, in the solar car.
[00:49:43:550 - 00:49:45:989] **Speaker 1:** It's just a slightly different bit of maths for an
[00:49:45:989 - 00:49:47:590] **Speaker 1:** AC to DC converter.
[00:49:47:820 - 00:49:48:669] **Speaker 1:** It's the same concept.
[00:49:50:510 - 00:49:51:790] **Speaker 1:** Just get a different formula.
[00:49:52:330 - 00:49:54:050] **Speaker 1:** And so now we've derived that.
[00:49:55:500 - 00:50:00:709] **Speaker 1:** By assuming that the ripple was predominantly governed by the
[00:50:02:860 - 00:50:03:360] **Speaker 1:** Yeah.
[00:50:04:689 - 00:50:07:060] **Speaker 1:** Second harmonic Let me get this formula.
[00:50:09:419 - 00:50:13:479] **Speaker 1:** And so then ID is just VD over R.
[00:50:14:020 - 00:50:15:760] **Speaker 1:** So you can just rearrange this and you can get
[00:50:15:760 - 00:50:17:540] **Speaker 1:** your inductor sizing off this.
[00:50:20:429 - 00:50:22:070] **Speaker 1:** I think it's pretty neat that you can do that
[00:50:22:070 - 00:50:23:090] **Speaker 1:** totally analytically.
[00:50:24:149 - 00:50:27:149] **Speaker 1:** Which such a seemingly complex circuit.
[00:50:27:840 - 00:50:30:000] **Speaker 1:** And I've got an adequate formula for the inductor sizing
[00:50:30:000 - 00:50:30:239] **Speaker 1:** here.
[00:50:31:129 - 00:50:32:929] **Speaker 1:** This is what you did in the DC DC to
[00:50:32:929 - 00:50:33:570] **Speaker 1:** DC case.
[00:50:34:340 - 00:50:35:959] **Speaker 1:** So that's your inductive sizing formula.
[00:50:38:879 - 00:50:40:479] **Speaker 1:** And you can plug in the numbers and you'll get
[00:50:40:479 - 00:50:42:070] **Speaker 1:** L to be greater than 0.21.
[00:50:43:060 - 00:50:45:189] **Speaker 1:** If you recall before it was 0.2, like I was
[00:50:45:189 - 00:50:48:550] **Speaker 1:** actually really close, just a little bit bigger, and it
[00:50:48:550 - 00:50:49:750] **Speaker 1:** becomes continuous conduction.
[00:50:51:209 - 00:50:53:929] **Speaker 1:** Sorry I'm just about out of time, about 30 seconds,
[00:50:53:989 - 00:50:56:070] **Speaker 1:** but I just might just grab a little bit.
[00:50:57:320 - 00:50:58:919] **Speaker 1:** Just so I can get the slide, cause I, I
[00:50:58:919 - 00:51:00:419] **Speaker 1:** knew I wasn't gonna get the 3 phase.
[00:51:01:000 - 00:51:02:840] **Speaker 1:** Cause it's, it's like kind of a good place to
[00:51:02:840 - 00:51:05:290] **Speaker 1:** stop cause I'm doing 3 section B.
[00:51:05:699 - 00:51:06:820] **Speaker 1:** I can start that on Monday.
[00:51:07:120 - 00:51:07:719] **Speaker 1:** It's all right.
[00:51:09:570 - 00:51:12:219] **Speaker 1:** I just want to quickly look, because I don't, I
[00:51:12:219 - 00:51:14:139] **Speaker 1:** don't really, this could be mostly, you can look at
[00:51:14:139 - 00:51:16:939] **Speaker 1:** this in your own time, but I am looking at
[00:51:16:939 - 00:51:18:000] **Speaker 1:** a capacitiveness design.
[00:51:21:340 - 00:51:24:760] **Speaker 1:** And you can just like you in your solar car,
[00:51:25:100 - 00:51:27:659] **Speaker 1:** you worked out the capacitance to try and get a
[00:51:27:669 - 00:51:29:060] **Speaker 1:** a given ripple in the voltage.
[00:51:29:139 - 00:51:31:350] **Speaker 1:** Remember doing that with that with that exercise?
[00:51:31:419 - 00:51:33:000] **Speaker 1:** You can do the same with AC to DC.
[00:51:33:939 - 00:51:35:540] **Speaker 1:** You can choose a seed to provide a given amount
[00:51:35:540 - 00:51:36:719] **Speaker 1:** of ripple in the voltage.
[00:51:37:780 - 00:51:42:459] **Speaker 1:** And you do that by um the original formula that
[00:51:42:459 - 00:51:45:379] **Speaker 1:** I derived way back earlier in the lecture.
[00:51:46:340 - 00:51:48:040] **Speaker 1:** I think it's, I don't know where it is now.
[00:51:48:179 - 00:51:48:840] **Speaker 1:** Oh, you're here.
[00:51:50:879 - 00:51:51:899] **Speaker 1:** Remember this formula here?
[00:51:52:620 - 00:51:54:600] **Speaker 1:** You can use that formula to do.
[00:51:56:780 - 00:51:57:840] **Speaker 1:** Capacitance design.
[00:51:59:520 - 00:52:03:469] **Speaker 1:** Great And so we have our natural fragraency, we have
[00:52:03:469 - 00:52:04:129] **Speaker 1:** our xy.
[00:52:06:689 - 00:52:09:750] **Speaker 1:** Um, probably, I'm probably like one at a time, so
[00:52:10:169 - 00:52:11:469] **Speaker 1:** maybe I'll just finish it on Monday.
[00:52:12:550 - 00:52:14:989] **Speaker 1:** Because that that is sort of examinable, but it's showing
[00:52:14:989 - 00:52:18:120] **Speaker 1:** you how you can for a given inductor, you could
[00:52:18:120 - 00:52:22:310] **Speaker 1:** actually size your capacitor to get a given attenuation in
[00:52:22:310 - 00:52:23:129] **Speaker 1:** the voltage.
[00:52:23:629 - 00:52:25:649] **Speaker 1:** That's what this is, this slide's all about.
[00:52:26:310 - 00:52:28:330] **Speaker 1:** I'll kind of finish it off on Monday.
[00:52:28:949 - 00:52:29:419] **Speaker 1:** Thank you.
[00:52:42:489 - 00:53:22:580] **Speaker 0:** Yeah, I we need That.
[00:53:25:860 - 00:54:11:120] **Speaker 0:** 2 hours I feel like I'm still catching up on
[00:54:11:120 - 00:54:12:780] **Speaker 2:** energy after last Friday, to be honest.
[00:54:14:620 - 00:54:15:580] **Speaker 2:** A long day.
[00:54:38:699 - 00:54:41:219] **Speaker 2:** Yeah, I, I would treat it as data myself.
[00:54:41:459 - 00:54:43:899] **Speaker 2:** Yeah, so I'd kind of list something in an appendix
[00:54:43:899 - 00:54:46:739] **Speaker 2:** and just have a way of tagging it when I
[00:54:46:739 - 00:54:48:000] **Speaker 2:** talk about it in the text.
[00:54:48:540 - 00:54:48:780] **Speaker 2:** Yeah.
[00:54:50:330 - 00:54:51:409] **Speaker 2:** I think Donald's added something.
[00:54:56:270 - 00:54:56:389] **Speaker 0:** that.
[00:54:59:340 - 00:54:59:909] **Speaker 0:** It's right.

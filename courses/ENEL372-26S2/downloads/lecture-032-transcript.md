# ENEL372-26S2 Lecture 32 native Echo transcript

Date: October 5, 2026 4:00pm-4:54pm
Transcript type: native Echo automated transcript.

[00:00:00:790 - 00:00:03:500] **Speaker 0:** I Yeah, that was where I meant to get to.
[00:00:04:739 - 00:00:06:650] **Speaker 1:** And I should thank you for coming to my lecture.
[00:00:06:739 - 00:00:11:460] **Speaker 1:** I have to, you know, um, it's definitely, that makes
[00:00:11:460 - 00:00:12:819] **Speaker 1:** it worthwhile to have you guys here.
[00:00:13:579 - 00:00:15:760] **Speaker 1:** Having an empty audience is never, never nice.
[00:00:16:600 - 00:00:18:780] **Speaker 1:** So I appreciate people coming even though I know you're
[00:00:18:780 - 00:00:19:819] **Speaker 1:** flat out at this time of year.
[00:00:21:180 - 00:00:23:129] **Speaker 1:** If I keep thanking you, maybe you keep turning up.
[00:00:25:059 - 00:00:25:649] **Speaker 1:** Um.
[00:00:26:510 - 00:00:31:500] **Speaker 1:** So Uh, we sort of finished off with analogue electronics.
[00:00:31:579 - 00:00:34:360] **Speaker 1:** We're trying to think of different.
[00:00:35:770 - 00:00:38:009] **Speaker 1:** I don't know whatever comes to mind when you think
[00:00:38:009 - 00:00:38:930] **Speaker 1:** of electronics.
[00:00:39:930 - 00:00:41:849] **Speaker 1:** The first thing that I thought was really cool was
[00:00:41:849 - 00:00:44:900] **Speaker 1:** the TVs, which is a very good example and then
[00:00:44:900 - 00:00:46:930] **Speaker 1:** radios and got onto record players players is a great
[00:00:46:930 - 00:00:46:939] **Speaker 1:** example.
[00:00:50:099 - 00:00:50:819] **Speaker 1:** And so on.
[00:00:52:279 - 00:00:54:009] **Speaker 1:** And then I mentioned that um.
[00:00:54:889 - 00:00:57:330] **Speaker 1:** What I come because I'm a mathematician, I think of
[00:00:57:330 - 00:00:58:150] **Speaker 1:** continuous time.
[00:00:59:319 - 00:01:01:689] **Speaker 1:** So I like continuous time because that's where all the
[00:01:01:689 - 00:01:05:550] **Speaker 1:** cool math properties, you know, the past transforms fully transformed.
[00:01:06:339 - 00:01:10:239] **Speaker 1:** Differential equations, all of that is all continuous time.
[00:01:10:660 - 00:01:12:480] **Speaker 1:** It doesn't really work for discrete time.
[00:01:13:250 - 00:01:14:809] **Speaker 1:** So we just make everything continuous.
[00:01:15:589 - 00:01:17:550] **Speaker 1:** When we even in the digital world, we kind of
[00:01:17:550 - 00:01:20:389] **Speaker 1:** make it continuous, but the beautiful thing about analogue electronics
[00:01:20:389 - 00:01:23:540] **Speaker 1:** is we don't have to pretend the real world is
[00:01:23:540 - 00:01:24:250] **Speaker 1:** continuous.
[00:01:26:809 - 00:01:29:250] **Speaker 1:** So yeah, but then to do stuff with it.
[00:01:30:349 - 00:01:33:120] **Speaker 1:** You have to convert it into signals and so you
[00:01:33:120 - 00:01:34:629] **Speaker 1:** have to take it from the continuous you probe to
[00:01:34:629 - 00:01:37:069] **Speaker 1:** do an A to D digital processes and then have
[00:01:37:069 - 00:01:39:690] **Speaker 1:** another D to A and then get the signal out,
[00:01:39:790 - 00:01:40:230] **Speaker 1:** um.
[00:01:41:139 - 00:01:43:620] **Speaker 1:** Because always it's like you, the real world is, is
[00:01:43:620 - 00:01:46:500] **Speaker 1:** continuous, you measure it, but then to process the real
[00:01:46:500 - 00:01:47:000] **Speaker 1:** world.
[00:01:47:980 - 00:01:50:699] **Speaker 1:** And, I don't know, I wouldn't say substandard brain, but
[00:01:50:699 - 00:01:54:449] **Speaker 1:** in our In our human capacity, which is limited.
[00:01:55:110 - 00:01:55:629] **Speaker 1:** How's that?
[00:01:56:669 - 00:02:00:279] **Speaker 1:** We have to transform it into a digital domain so
[00:02:00:279 - 00:02:02:599] **Speaker 1:** we can use computers to make sense of it.
[00:02:03:540 - 00:02:05:300] **Speaker 1:** And then we've got to convert it back into the
[00:02:05:300 - 00:02:07:459] **Speaker 1:** continuous domain so that we can operate on the world
[00:02:07:459 - 00:02:07:779] **Speaker 1:** again.
[00:02:08:179 - 00:02:09:500] **Speaker 1:** Wouldn't it be great if you could just go from
[00:02:09:500 - 00:02:10:660] **Speaker 1:** continuous to continuous?
[00:02:11:100 - 00:02:14:139] **Speaker 1:** Sometimes you can, but normally you need a digital thing
[00:02:14:139 - 00:02:14:699] **Speaker 1:** in the middle.
[00:02:16:380 - 00:02:16:389] **Speaker 1:** Right.
[00:02:17:960 - 00:02:19:770] **Speaker 1:** And so that's what this is all about.
[00:02:19:839 - 00:02:22:360] **Speaker 1:** It's like taking continuous systems and changing them and then
[00:02:22:360 - 00:02:24:660] **Speaker 1:** putting them then converting them into another signal, but it
[00:02:24:660 - 00:02:27:240] **Speaker 1:** would normally be a continuous signal out because you want
[00:02:27:240 - 00:02:29:399] **Speaker 1:** to like move a motor or do something real in
[00:02:29:399 - 00:02:30:179] **Speaker 1:** the real world.
[00:02:30:559 - 00:02:32:520] **Speaker 1:** It's always going to be continuous normally.
[00:02:35:139 - 00:02:37:649] **Speaker 1:** OK, so that's that philosophical.
[00:02:40:789 - 00:02:42:449] **Speaker 1:** A lot of engineering is philosophical.
[00:02:44:369 - 00:02:46:169] **Speaker 1:** I think engineering is the true science.
[00:02:49:350 - 00:02:51:869] **Speaker 1:** Maybe not in the in the deep past, but then
[00:02:51:869 - 00:02:54:210] **Speaker 1:** I reckon a lot of the great scientists were engineers.
[00:02:55:669 - 00:02:58:240] **Speaker 1:** But now I think true science is engineering because it's
[00:02:58:240 - 00:02:59:940] **Speaker 1:** actually based on something real.
[00:03:04:220 - 00:03:07:199] **Speaker 1:** Digital problems with resolution, right, that's there's a few little
[00:03:07:199 - 00:03:08:179] **Speaker 1:** things I'm gonna mention.
[00:03:12:169 - 00:03:15:429] **Speaker 1:** So whenever you convert something.
[00:03:17:029 - 00:03:20:820] **Speaker 1:** To digital No matter how fast.
[00:03:21:970 - 00:03:23:899] **Speaker 1:** You and and some of the 8 days in there
[00:03:23:899 - 00:03:24:869] **Speaker 1:** are absolutely crazy.
[00:03:25:960 - 00:03:28:429] **Speaker 1:** Do like more than 1 GHz, probably getting up to
[00:03:28:429 - 00:03:29:309] **Speaker 1:** 100s of gigahertz.
[00:03:29:350 - 00:03:30:529] **Speaker 1:** I don't know, maybe even more.
[00:03:31:389 - 00:03:32:309] **Speaker 1:** Uh, they are.
[00:03:33:399 - 00:03:36:940] **Speaker 1:** And the costs are dropping for the like the higher
[00:03:36:940 - 00:03:38:220] **Speaker 1:** megahertz range too.
[00:03:38:570 - 00:03:40:940] **Speaker 1:** Even though the gigahertz, the story isn't expensive, but.
[00:03:42:460 - 00:03:47:520] **Speaker 1:** Um, So there's something called quantization.
[00:03:52:600 - 00:03:54:210] **Speaker 1:** And it's done on the amplitude.
[00:03:54:320 - 00:03:56:360] **Speaker 1:** In this case, I'm thinking the quantization here on the
[00:03:56:360 - 00:03:59:020] **Speaker 1:** amplitude, because you've also got like the time component.
[00:03:59:960 - 00:04:02:059] **Speaker 1:** But you have the amplitude component as well.
[00:04:08:919 - 00:04:12:490] **Speaker 1:** So you're losing information because you can't get all the
[00:04:12:490 - 00:04:13:669] **Speaker 1:** parts of the signal.
[00:04:14:919 - 00:04:15:679] **Speaker 1:** All covered.
[00:04:20:440 - 00:04:21:910] **Speaker 1:** So you're losing information.
[00:04:23:549 - 00:04:29:790] **Speaker 1:** With that And that's sort of related to the A
[00:04:29:790 - 00:04:33:149] **Speaker 1:** to D conversion, but then that's the resolution side, the
[00:04:33:149 - 00:04:34:010] **Speaker 1:** speed side.
[00:04:38:230 - 00:04:40:570] **Speaker 1:** So you get time, you effectively get a time lag.
[00:04:43:239 - 00:04:44:119] **Speaker 1:** Turn on the light.
[00:04:46:260 - 00:04:48:269] **Speaker 1:** When you sample something and then it's just like a
[00:04:48:269 - 00:04:50:350] **Speaker 1:** constant sample and then you wait for the next sample,
[00:04:50:429 - 00:04:53:209] **Speaker 1:** that time period is a delay, you cannot avoid it.
[00:04:54:519 - 00:04:56:950] **Speaker 1:** If it's a sensor, you're getting sensor delay.
[00:04:57:369 - 00:04:59:269] **Speaker 1:** If it's a command to an actuator.
[00:05:00:170 - 00:05:04:170] **Speaker 1:** Then that would that's further delay or if it's part
[00:05:04:170 - 00:05:08:549] **Speaker 1:** of the process of getting the signal into the actuator.
[00:05:09:619 - 00:05:13:179] **Speaker 1:** Then that's going to effectively create a time delay for
[00:05:13:179 - 00:05:13:899] **Speaker 1:** the actuator.
[00:05:19:980 - 00:05:21:359] **Speaker 1:** Cause that's you get the step hold.
[00:05:24:739 - 00:05:27:179] **Speaker 1:** So no matter how fast they get actually like cause
[00:05:27:190 - 00:05:29:859] **Speaker 1:** cause now A to D can never keep up with
[00:05:29:859 - 00:05:33:019] **Speaker 1:** the actual frequency bands that uh they keep going higher,
[00:05:33:140 - 00:05:33:420] **Speaker 1:** right?
[00:05:34:190 - 00:05:35:649] **Speaker 1:** They're getting higher and higher.
[00:05:36:429 - 00:05:39:480] **Speaker 1:** Especially some of the space bands are getting into terahertz.
[00:05:42:500 - 00:05:45:709] **Speaker 1:** Yeah, so, um, I don't know if I've got terahertz
[00:05:45:709 - 00:05:46:480] **Speaker 1:** out of these yet.
[00:05:47:339 - 00:05:48:250] **Speaker 1:** Does anyone know?
[00:05:48:859 - 00:05:49:579] **Speaker 1:** Don't think so.
[00:05:51:329 - 00:05:52:679] **Speaker 1:** They're still at gigahertz.
[00:05:53:019 - 00:05:54:790] **Speaker 1:** They may have got 10 gigahertz or so.
[00:05:55:109 - 00:05:57:000] **Speaker 1:** I don't know if they got to 100 yet, but
[00:05:57:299 - 00:05:58:589] **Speaker 1:** they're probably around about 10.
[00:06:09:600 - 00:06:12:519] **Speaker 1:** So not quite fast enough yet.
[00:06:14:260 - 00:06:16:070] **Speaker 1:** To see everything.
[00:06:19:109 - 00:06:23:339] **Speaker 1:** In the signal Though as I mentioned, I don't think
[00:06:23:339 - 00:06:25:859] **Speaker 1:** even if it got up to terahertz then you'll be
[00:06:25:859 - 00:06:28:559] **Speaker 1:** getting like 100 terahertz like it's just gonna keep going
[00:06:28:559 - 00:06:30:000] **Speaker 1:** and you'll always be chasing it.
[00:06:30:179 - 00:06:31:250] **Speaker 1:** I don't know what the limit is.
[00:06:31:579 - 00:06:33:420] **Speaker 1:** It's gotta be some fundamental limit surely.
[00:06:34:320 - 00:06:35:380] **Speaker 1:** But we haven't reached it yet.
[00:06:46:549 - 00:06:48:350] **Speaker 1:** But even at the gigahertz, you're paying a lot of
[00:06:48:350 - 00:06:52:149] **Speaker 1:** money for a an AD ADC gigahertz, it's really hard
[00:06:52:149 - 00:06:52:809] **Speaker 1:** to deal with.
[00:06:54:149 - 00:06:56:429] **Speaker 1:** So it's much nicer to to push it down to
[00:06:56:429 - 00:06:58:950] **Speaker 1:** a lower frequency before you do the A to D
[00:06:59:230 - 00:06:59:890] **Speaker 1:** conversion.
[00:07:00:309 - 00:07:03:070] **Speaker 1:** But it's just becoming now possible potentially.
[00:07:03:929 - 00:07:06:230] **Speaker 1:** To just do it straight from what you see, just
[00:07:06:230 - 00:07:08:640] **Speaker 1:** like the ADC's are so good that you can just
[00:07:08:640 - 00:07:11:420] **Speaker 1:** about avoid having to step it down, but it still
[00:07:11:420 - 00:07:12:559] **Speaker 1:** cost it saves money.
[00:07:13:459 - 00:07:14:760] **Speaker 1:** Uh, to be able to do that.
[00:07:19:079 - 00:07:21:390] **Speaker 1:** I think one of the other things is not just
[00:07:21:390 - 00:07:23:179] **Speaker 1:** the money, it's the storage.
[00:07:23:970 - 00:07:26:489] **Speaker 1:** If you are, if you've got an insanely fast ADC,
[00:07:26:570 - 00:07:28:549] **Speaker 1:** you know, and you're just sensing things.
[00:07:29:779 - 00:07:33:380] **Speaker 1:** At like terahertz, like it's in a second you're just
[00:07:33:380 - 00:07:34:119] **Speaker 1:** like terabyte.
[00:07:34:269 - 00:07:35:739] **Speaker 1:** I don't know if it's a terabyte, but you know.
[00:07:36:709 - 00:07:38:989] **Speaker 1:** You're getting huge amounts of data that you have to
[00:07:38:989 - 00:07:39:250] **Speaker 1:** store.
[00:07:45:250 - 00:07:48:089] **Speaker 1:** So sometimes it is good to just drop that frequency
[00:07:48:089 - 00:07:48:589] **Speaker 1:** down.
[00:07:50:730 - 00:07:52:549] **Speaker 1:** And you can use analogue electronics to do that.
[00:08:03:000 - 00:08:06:440] **Speaker 1:** Earlying is a problem.
[00:08:08:640 - 00:08:11:630] **Speaker 1:** I'll just, just to show you a just draw something
[00:08:11:630 - 00:08:12:220] **Speaker 1:** like this.
[00:08:12:720 - 00:08:13:799] **Speaker 1:** Just draw you a sine wave.
[00:08:20:959 - 00:08:22:170] **Speaker 1:** So if you were sampling.
[00:08:26:600 - 00:08:30:679] **Speaker 1:** Something like this So you may actually think it's a
[00:08:30:679 - 00:08:32:219] **Speaker 1:** really slow sine wave.
[00:08:33:508 - 00:08:36:940] **Speaker 1:** And so You are getting this.
[00:08:37:760 - 00:08:40:619] **Speaker 1:** Much lower frequency, which you weren't expecting.
[00:08:48:969 - 00:08:51:729] **Speaker 1:** So that this means that when the signal is gonna
[00:08:51:729 - 00:08:52:190] **Speaker 1:** look funny.
[00:08:52:979 - 00:08:54:530] **Speaker 1:** So you get signal artefacts.
[00:08:59:469 - 00:09:01:409] **Speaker 1:** And you would use analogue.
[00:09:03:719 - 00:09:07:280] **Speaker 1:** Anti-alias philtres because if you use an analogue philtre, there's
[00:09:07:280 - 00:09:09:700] **Speaker 1:** no restriction on the ADC.
[00:09:10:830 - 00:09:12:460] **Speaker 1:** The ADC if you use a digital philtre, you rely
[00:09:12:460 - 00:09:14:559] **Speaker 1:** on an ADC and you have a problem.
[00:09:15:549 - 00:09:17:630] **Speaker 1:** So if the analogue philtre gets there first before the
[00:09:17:630 - 00:09:19:469] **Speaker 1:** ADC, you can remove a lot of these things, so
[00:09:19:469 - 00:09:22:130] **Speaker 1:** the ADC doesn't cause the a thing, for example.
[00:09:25:119 - 00:09:26:219] **Speaker 1:** It's the real world.
[00:09:28:169 - 00:09:30:380] **Speaker 1:** As I mentioned before, it's not, it doesn't really work
[00:09:30:380 - 00:09:31:840] **Speaker 1:** in with the digital domain.
[00:09:32:940 - 00:09:34:820] **Speaker 1:** The two just disconnected.
[00:09:34:940 - 00:09:36:840] **Speaker 1:** You just have to do one and then the other.
[00:09:37:650 - 00:09:39:020] **Speaker 1:** So it does not work.
[00:09:41:960 - 00:09:45:950] **Speaker 1:** Digital codes It's the intermediate step, which at the moment
[00:09:45:950 - 00:09:46:409] **Speaker 1:** we need.
[00:09:58:229 - 00:10:00:429] **Speaker 1:** I'm selling the story for analogue electronics here.
[00:10:13:270 - 00:10:14:750] **Speaker 1:** We need to do that to see and act upon
[00:10:14:750 - 00:10:15:400] **Speaker 1:** the world.
[00:10:18:419 - 00:10:32:750] **Speaker 1:** Including Filtering out Erroneneous Aro is know.
[00:10:33:830 - 00:10:34:929] **Speaker 1:** One new signals.
[00:10:41:299 - 00:10:44:419] **Speaker 1:** So you, you need analogue electronics techniques.
[00:10:48:409 - 00:10:51:940] **Speaker 1:** So the next And the next slide.
[00:10:53:000 - 00:10:56:219] **Speaker 1:** Got that Yeah.
[00:10:59:989 - 00:11:00:679] **Speaker 1:** We were components.
[00:11:02:400 - 00:11:04:159] **Speaker 1:** What are real world components?
[00:11:05:099 - 00:11:06:429] **Speaker 1:** Seems like an obvious question.
[00:11:08:250 - 00:11:10:080] **Speaker 1:** But it maybe not what you think.
[00:11:11:169 - 00:11:13:729] **Speaker 1:** A capacitor maybe you may have a, you may have
[00:11:13:729 - 00:11:16:409] **Speaker 1:** a mental model or a mental idea of what a
[00:11:16:409 - 00:11:17:349] **Speaker 1:** capacitor is.
[00:11:18:609 - 00:11:20:369] **Speaker 1:** But what it is in the real world might be
[00:11:20:369 - 00:11:20:950] **Speaker 1:** completely different.
[00:11:23:479 - 00:11:24:669] **Speaker 1:** I'll show you a slide next.
[00:11:24:719 - 00:11:25:919] **Speaker 1:** I think that will stun you a bit.
[00:11:26:830 - 00:11:33:580] **Speaker 1:** But for now, Uh, Probably you have an ideal mental
[00:11:33:580 - 00:11:36:460] **Speaker 1:** model of what a capacitor resistor inductor is.
[00:11:39:299 - 00:11:41:070] **Speaker 1:** I don't know if anyone has a mental model of
[00:11:41:070 - 00:11:42:669] **Speaker 1:** like an op amp or.
[00:11:43:530 - 00:11:46:719] **Speaker 1:** Right BJT or whatever, you know, those things, even a
[00:11:46:719 - 00:11:48:690] **Speaker 1:** diode, it's hard to have a mental model of a
[00:11:48:690 - 00:11:49:309] **Speaker 1:** diode.
[00:11:50:299 - 00:11:54:090] **Speaker 1:** It's just a very, very difficult to model device.
[00:11:55:630 - 00:11:57:849] **Speaker 1:** Uh, so there's the real and the ideal.
[00:11:59:799 - 00:12:01:880] **Speaker 1:** And so the real devices, they obviously you can measure,
[00:12:01:890 - 00:12:05:059] **Speaker 1:** you can see them, that they're measured, uh they interact
[00:12:05:450 - 00:12:07:840] **Speaker 1:** and they make up your real system, and they, but
[00:12:07:840 - 00:12:10:140] **Speaker 1:** it's just it's not just your components.
[00:12:11:520 - 00:12:17:440] **Speaker 1:** There's all sorts of Induced inductance incapacitance and all sorts
[00:12:17:440 - 00:12:19:559] **Speaker 1:** of noise that can occur as a result of how
[00:12:19:559 - 00:12:20:619] **Speaker 1:** you build the board.
[00:12:21:340 - 00:12:23:609] **Speaker 1:** And so then you would add other things like decoupling
[00:12:23:609 - 00:12:24:559] **Speaker 1:** capacitors on the board.
[00:12:25:640 - 00:12:28:159] **Speaker 1:** To reduce all this, to reduce noise and things like
[00:12:28:159 - 00:12:29:559] **Speaker 1:** that, or to reduce the inductance.
[00:12:29:640 - 00:12:34:119] **Speaker 1:** This case here would be to reduce inductive.
[00:12:36:159 - 00:12:36:169] **Speaker 1:** F.
[00:12:41:039 - 00:12:42:640] **Speaker 1:** And when you've got a loop, you've got an inductor,
[00:12:42:719 - 00:12:43:280] **Speaker 1:** that's the problem.
[00:12:43:440 - 00:12:45:669] **Speaker 1:** As soon as you wind something around, you have an
[00:12:45:669 - 00:12:46:580] **Speaker 1:** inductive effect.
[00:12:52:059 - 00:12:53:880] **Speaker 1:** This is the real world we're talking about.
[00:12:56:690 - 00:12:57:840] **Speaker 1:** We're ideal.
[00:12:58:820 - 00:13:02:210] **Speaker 1:** You have a precise thing like you have a precise
[00:13:02:210 - 00:13:04:840] **Speaker 1:** capacitor or you have a precise inductor.
[00:13:05:700 - 00:13:08:260] **Speaker 1:** And it just performs exactly the way that you describe
[00:13:08:260 - 00:13:09:280] **Speaker 1:** it mathematically.
[00:13:09:700 - 00:13:11:229] **Speaker 1:** That is an ideal device.
[00:13:11:820 - 00:13:14:179] **Speaker 1:** So as you might have an ideal diode, which even
[00:13:14:179 - 00:13:16:900] **Speaker 1:** an ideal diode is actually reasonably complicated in LD splice,
[00:13:16:979 - 00:13:17:320] **Speaker 1:** for example.
[00:13:20:520 - 00:13:25:000] **Speaker 1:** And so you get these ideal devices and you combine
[00:13:25:000 - 00:13:28:479] **Speaker 1:** them to then create an approximation to real-world devices.
[00:13:36:890 - 00:13:38:849] **Speaker 1:** It all depends on the frequency you're operating in.
[00:13:38:900 - 00:13:40:780] **Speaker 1:** If you're at a lower frequency then you you don't
[00:13:40:780 - 00:13:41:840] **Speaker 1:** need to worry a lot.
[00:13:44:349 - 00:13:46:539] **Speaker 1:** But it's just that the world is moving to higher
[00:13:46:539 - 00:13:47:229] **Speaker 1:** frequencies.
[00:13:47:849 - 00:13:49:510] **Speaker 1:** It's just the way that it's, it's going.
[00:13:57:380 - 00:13:59:219] **Speaker 1:** I think there's a new band in the space band
[00:13:59:219 - 00:14:01:159] **Speaker 1:** that I think SpaceX are now using, which is.
[00:14:03:270 - 00:14:03:659] **Speaker 1:** Yeah.
[00:14:07:570 - 00:14:09:849] **Speaker 1:** And they're getting up to terahertz.
[00:14:10:960 - 00:14:15:520] **Speaker 1:** Right, so, um, passive real components, uh, any real component
[00:14:15:520 - 00:14:18:599] **Speaker 1:** has a parasitic, has all three, so especially when you
[00:14:18:599 - 00:14:21:659] **Speaker 1:** get into the RF world or even round high megahertz
[00:14:21:659 - 00:14:21:919] **Speaker 1:** operation.
[00:14:23:669 - 00:14:27:159] **Speaker 1:** A resistor, a capacitor conductor are no longer what you
[00:14:27:159 - 00:14:27:940] **Speaker 1:** think they are.
[00:14:29:130 - 00:14:36:919] **Speaker 1:** In fact, Yeah, so lumped, they can be a combination
[00:14:36:919 - 00:14:39:080] **Speaker 1:** of discrete, I'll just say that combination.
[00:14:43:320 - 00:14:44:140] **Speaker 1:** Of discreet.
[00:14:45:200 - 00:14:46:010] **Speaker 1:** Components.
[00:14:49:429 - 00:14:53:099] **Speaker 1:** So here's a good kind of good typical model that's
[00:14:53:099 - 00:14:54:530] **Speaker 1:** used for a resistor.
[00:14:55:640 - 00:14:57:280] **Speaker 1:** Which is not just a resistor, it would be a
[00:14:57:280 - 00:14:58:780] **Speaker 1:** simple model, just a resistor.
[00:14:59:359 - 00:15:00:940] **Speaker 1:** It's a great model of a resistor, right?
[00:15:02:700 - 00:15:04:359] **Speaker 1:** Now, you wanna add a little bit of inductance.
[00:15:07:500 - 00:15:11:359] **Speaker 1:** And then you want to put some capacitance in parallel.
[00:15:12:780 - 00:15:15:530] **Speaker 1:** This has all just been worked out based on experiment.
[00:15:17:289 - 00:15:19:239] **Speaker 1:** You have a resistor, you put in a high frequency
[00:15:19:239 - 00:15:21:140] **Speaker 1:** input and you have an oscilloscope and you measure the
[00:15:21:140 - 00:15:23:380] **Speaker 1:** output, get a transfer function, and you can say, oh
[00:15:23:380 - 00:15:27:260] **Speaker 1:** this, a combination of this and that fitted well to
[00:15:27:260 - 00:15:28:760] **Speaker 1:** the body plot that you got, right?
[00:15:32:770 - 00:15:35:109] **Speaker 1:** So let's say approximately equal to.
[00:15:39:070 - 00:15:40:840] **Speaker 1:** A real resistor.
[00:15:44:989 - 00:15:46:859] **Speaker 1:** But in the real world.
[00:15:47:760 - 00:15:50:130] **Speaker 1:** The resistor that you get, which sees how many ohms
[00:15:50:130 - 00:15:53:090] **Speaker 1:** it is, won't be how many homes you actually get.
[00:15:54:270 - 00:15:55:049] **Speaker 1:** It'll be close.
[00:15:57:369 - 00:16:01:690] **Speaker 1:** You get your Parasitic inductance.
[00:16:02:500 - 00:16:04:460] **Speaker 1:** And you get your parasitic.
[00:16:07:119 - 00:16:11:809] **Speaker 1:** Capaciance And if you model them both, you'll find you'll
[00:16:11:809 - 00:16:14:039] **Speaker 1:** get a better fit with a resistor, not this one
[00:16:14:039 - 00:16:15:309] **Speaker 1:** that you got from the store.
[00:16:17:080 - 00:16:19:119] **Speaker 1:** Sometimes it can be quite a bit different too, like
[00:16:19:119 - 00:16:20:859] **Speaker 1:** 20% out or more.
[00:16:25:030 - 00:16:26:229] **Speaker 1:** So let's just say here.
[00:16:28:299 - 00:16:30:650] **Speaker 1:** R is not equal to our bar, which can seem
[00:16:30:650 - 00:16:31:440] **Speaker 1:** surprising.
[00:16:35:299 - 00:16:39:179] **Speaker 1:** Especially For high frequencies.
[00:16:44:429 - 00:16:46:080] **Speaker 1:** Because if your resistance is not equal to our bar
[00:16:46:080 - 00:16:48:039] **Speaker 1:** and you got these other, you can get like extra
[00:16:48:039 - 00:16:50:479] **Speaker 1:** resonances you hadn't accounted for and and like you think
[00:16:50:479 - 00:16:52:909] **Speaker 1:** you're setting your pole frequencies or your cutoff frequency for
[00:16:52:909 - 00:16:55:630] **Speaker 1:** a low pass philtre for static component static philtre passive
[00:16:55:630 - 00:16:56:020] **Speaker 1:** philtre.
[00:16:57:010 - 00:17:00:210] **Speaker 1:** Then you thought you said it at some frequency and
[00:17:00:210 - 00:17:01:530] **Speaker 1:** then it ends up being another frequency.
[00:17:03:320 - 00:17:04:540] **Speaker 1:** So you gotta be careful.
[00:17:05:469 - 00:17:10:520] **Speaker 1:** So capacitors, a common model of a capacitor is in
[00:17:10:520 - 00:17:11:180] **Speaker 1:** series.
[00:17:12:719 - 00:17:15:339] **Speaker 1:** With the resistor and the inductor.
[00:17:16:458 - 00:17:18:979] **Speaker 1:** So you got your capacitor which would not quite the
[00:17:18:979 - 00:17:20:629] **Speaker 1:** same as the the true capacitor.
[00:17:23:168 - 00:17:25:688] **Speaker 1:** You have your resistance because there's always a bit of
[00:17:25:688 - 00:17:27:348] **Speaker 1:** resistance around.
[00:17:27:979 - 00:17:29:208] **Speaker 1:** And some ductants.
[00:17:30:010 - 00:17:32:510] **Speaker 1:** There might even be some more capacitants, but this is
[00:17:32:510 - 00:17:33:589] **Speaker 1:** just lumped into here.
[00:17:34:430 - 00:17:35:890] **Speaker 1:** You don't worry about parallel.
[00:17:37:310 - 00:17:39:849] **Speaker 1:** For this, this is just a good model.
[00:17:44:250 - 00:17:46:069] **Speaker 1:** And that's equal to your real.
[00:17:47:180 - 00:17:51:239] **Speaker 1:** Capacity Sea, which is different to the sea bar.
[00:17:52:869 - 00:17:53:839] **Speaker 1:** An inductor.
[00:17:59:949 - 00:18:02:140] **Speaker 1:** This is often a good model used.
[00:18:05:130 - 00:18:06:170] **Speaker 1:** For an inductor.
[00:18:09:260 - 00:18:11:859] **Speaker 1:** So you have a capacitor in parallel again.
[00:18:12:660 - 00:18:15:699] **Speaker 1:** And you just put a resistor beside it.
[00:18:16:430 - 00:18:17:410] **Speaker 1:** Seems to work well.
[00:18:18:900 - 00:18:20:369] **Speaker 1:** So that would be Elba.
[00:18:21:380 - 00:18:23:040] **Speaker 1:** That you're a parasitic.
[00:18:24:119 - 00:18:25:640] **Speaker 1:** And that's just see parasitic.
[00:18:28:760 - 00:18:30:239] **Speaker 1:** And that is just gonna be.
[00:18:32:089 - 00:18:33:449] **Speaker 1:** You're a real world inductor.
[00:18:34:729 - 00:18:39:050] **Speaker 1:** So real So there's 3 separate circuits that you can
[00:18:39:050 - 00:18:41:949] **Speaker 1:** use when you start going into the RF world.
[00:18:43:349 - 00:18:44:930] **Speaker 1:** Then you'd have to tune these.
[00:18:45:689 - 00:18:49:219] **Speaker 1:** Depending on, yeah, different types and depending on the frequency
[00:18:49:219 - 00:18:49:660] **Speaker 1:** as well.
[00:18:49:890 - 00:18:52:219] **Speaker 1:** You may need to have even a more complicated set
[00:18:52:219 - 00:18:53:130] **Speaker 1:** of components.
[00:18:53:500 - 00:18:55:489] **Speaker 1:** If you go to the higher frequencies, you get lots
[00:18:55:489 - 00:18:56:780] **Speaker 1:** more frequencies that are excited.
[00:18:58:719 - 00:18:59:880] **Speaker 1:** So what is the result?
[00:19:00:140 - 00:19:02:760] **Speaker 1:** Result is you get resonance.
[00:19:03:670 - 00:19:06:869] **Speaker 1:** You can get problems ringing, you can get instabilities.
[00:19:09:010 - 00:19:10:510] **Speaker 1:** Our pimps can go unstable.
[00:19:12:349 - 00:19:13:079] **Speaker 1:** can be clipping.
[00:19:13:160 - 00:19:16:140] **Speaker 1:** It won't get the range that you you planned for.
[00:19:19:520 - 00:19:20:400] **Speaker 1:** Reason and effects.
[00:19:21:219 - 00:19:23:989] **Speaker 1:** Resonance is definitely can be a real issue.
[00:19:25:599 - 00:19:28:979] **Speaker 1:** So here's a plot, which I think's quite interesting.
[00:19:31:119 - 00:19:31:770] **Speaker 1:** So that's that.
[00:19:34:609 - 00:19:35:989] **Speaker 1:** It's a transfer function.
[00:19:38:469 - 00:19:42:920] **Speaker 1:** And it's Just a, what is it one nano ferrode
[00:19:42:920 - 00:19:43:630] **Speaker 1:** capacitor.
[00:19:44:050 - 00:19:45:469] **Speaker 1:** So this one was a.
[00:19:47:010 - 00:19:49:849] **Speaker 1:** 1206, I've written here, capacitor.
[00:19:52:709 - 00:19:53:650] **Speaker 1:** Nano ferrode.
[00:19:54:270 - 00:19:56:650] **Speaker 1:** So one nano ferrode, very small.
[00:20:01:260 - 00:20:04:140] **Speaker 1:** And so what you do here is you do a
[00:20:04:140 - 00:20:04:939] **Speaker 1:** frequency sweep.
[00:20:05:020 - 00:20:06:680] **Speaker 1:** So you wanna put an input.
[00:20:08:369 - 00:20:09:420] **Speaker 1:** Frequency into it.
[00:20:10:430 - 00:20:12:449] **Speaker 1:** And you measure and what you're doing here is you're
[00:20:12:449 - 00:20:13:369] **Speaker 1:** measuring the impedance.
[00:20:14:739 - 00:20:21:849] **Speaker 1:** And you measure it And what it is, is the
[00:20:21:849 - 00:20:24:109] **Speaker 1:** output voltage.
[00:20:25:160 - 00:20:36:209] **Speaker 1:** Amplitude Divided by The input Current amplitude.
[00:20:41:329 - 00:20:43:339] **Speaker 1:** So you do that for every frequency and you do
[00:20:43:339 - 00:20:47:579] **Speaker 1:** a sweep right right up to the this is 5
[00:20:47:579 - 00:20:50:119] **Speaker 1:** gigahertz, 5 times 10 to 9.
[00:20:51:800 - 00:20:54:359] **Speaker 1:** And you can see that it's not following.
[00:20:54:689 - 00:20:56:420] **Speaker 1:** This would be the normal transfer function.
[00:20:56:479 - 00:20:59:109] **Speaker 1:** This is what it would look like for a capacitor
[00:20:59:369 - 00:21:00:489] **Speaker 1:** as you went higher.
[00:21:00:930 - 00:21:03:020] **Speaker 1:** Yes, so when you've got the lower frequencies, it's it's
[00:21:03:020 - 00:21:03:709] **Speaker 1:** pretty good.
[00:21:04:170 - 00:21:05:589] **Speaker 1:** But it deviates pretty quickly.
[00:21:06:619 - 00:21:09:099] **Speaker 1:** Once you get getting up into the high megahertz range,
[00:21:09:140 - 00:21:10:439] **Speaker 1:** like 100 megahertz here.
[00:21:11:180 - 00:21:12:319] **Speaker 1:** And this is.
[00:21:13:459 - 00:21:15:359] **Speaker 1:** I think this is a log log graph, so.
[00:21:16:050 - 00:21:18:130] **Speaker 1:** That's like 200 megahertz.
[00:21:18:209 - 00:21:23:770] **Speaker 1:** So this is It's actually 1.46.
[00:21:34:670 - 00:21:36:449] **Speaker 1:** That's what the natural frequency is.
[00:21:38:359 - 00:21:40:260] **Speaker 1:** And so these are parasitic values, you're getting.
[00:21:41:599 - 00:21:43:449] **Speaker 1:** Quite a bit lower capacitance here.
[00:21:45:849 - 00:21:47:579] **Speaker 1:** And we had a one nano ferro capacitor.
[00:21:53:880 - 00:21:57:479] **Speaker 1:** OK, so that's, that's just a capacitor.
[00:21:57:719 - 00:21:59:920] **Speaker 1:** You'll learn if you go up to something like.
[00:22:02:010 - 00:22:02:520] **Speaker 1:** I know.
[00:22:03:599 - 00:22:04:900] **Speaker 1:** BJT for example.
[00:22:07:670 - 00:22:09:780] **Speaker 1:** This is a very simple model of BJT.
[00:22:10:819 - 00:22:12:400] **Speaker 1:** And there are more complicated ones.
[00:22:15:579 - 00:22:18:910] **Speaker 1:** Uh, this is, yeah, so this is a particularly simple
[00:22:18:910 - 00:22:19:349] **Speaker 1:** one.
[00:22:19:910 - 00:22:22:349] **Speaker 1:** There's one model here that I found that was 147
[00:22:22:349 - 00:22:22:969] **Speaker 1:** pages long.
[00:22:26:849 - 00:22:28:520] **Speaker 1:** Well, it depends on how much accuracy you want.
[00:22:31:359 - 00:22:32:640] **Speaker 1:** So you can see it's an interesting model.
[00:22:32:800 - 00:22:35:260] **Speaker 1:** It's got mostly just capacitors and resistors.
[00:22:36:550 - 00:22:40:229] **Speaker 1:** But it has a little bit more complicated here, cause
[00:22:40:229 - 00:22:43:229] **Speaker 1:** it does have a current dependent source.
[00:22:43:630 - 00:22:46:229] **Speaker 1:** But this model here is uh is what's called like
[00:22:46:229 - 00:22:49:229] **Speaker 1:** a, it's a small signal model.
[00:22:49:530 - 00:22:50:989] **Speaker 1:** I don't know if you heard of those, you've done
[00:22:50:989 - 00:22:54:229] **Speaker 1:** that, like you assume a small small signal, and that's
[00:22:54:229 - 00:23:01:040] **Speaker 1:** how you So that's an approximation in itself.
[00:23:03:250 - 00:23:06:449] **Speaker 1:** So this is an example of a small signal model.
[00:23:06:569 - 00:23:08:329] **Speaker 1:** If you don't know what a small signal model is,
[00:23:08:569 - 00:23:13:270] **Speaker 1:** basically, You linearize.
[00:23:16:189 - 00:23:18:660] **Speaker 1:** About a bias point and then that tells you about
[00:23:18:660 - 00:23:21:239] **Speaker 1:** that point, the small signals around that bias point.
[00:23:22:189 - 00:23:26:239] **Speaker 1:** Will be how this will be how your BJT behaves,
[00:23:26:390 - 00:23:27:030] **Speaker 1:** and it'll be close.
[00:23:27:119 - 00:23:28:949] **Speaker 1:** This will be a close model for it, so it's
[00:23:28:949 - 00:23:29:449] **Speaker 1:** useful.
[00:23:30:910 - 00:23:33:339] **Speaker 1:** So it's called a small signal model.
[00:23:34:160 - 00:23:35:479] **Speaker 1:** And this is for.
[00:23:36:890 - 00:23:39:890] **Speaker 1:** Bipolar junction.
[00:23:41:079 - 00:23:44:609] **Speaker 1:** BJT Transistor.
[00:23:48:790 - 00:23:50:380] **Speaker 1:** So yeah, this, this is an interesting.
[00:23:51:469 - 00:23:52:689] **Speaker 1:** Kind of feature here.
[00:23:55:300 - 00:23:57:239] **Speaker 1:** So we've got an ideal current source here.
[00:24:02:010 - 00:24:05:530] **Speaker 1:** Well, ideal current dependent source is dependent on the current.
[00:24:10:640 - 00:24:12:510] **Speaker 1:** But it's actually depending on VNI.
[00:24:26:349 - 00:24:29:349] **Speaker 1:** You would have also seen the solar panel model I
[00:24:29:349 - 00:24:29:920] **Speaker 1:** developed.
[00:24:30:680 - 00:24:35:000] **Speaker 1:** And it had a Current yeah that like the current
[00:24:35:000 - 00:24:36:560] **Speaker 1:** source that you get an Alti Spice, you can put
[00:24:36:560 - 00:24:38:459] **Speaker 1:** a mathematical formula into it.
[00:24:39:420 - 00:24:43:060] **Speaker 1:** And yeah, you can actually write the eyes same if
[00:24:43:060 - 00:24:45:619] **Speaker 1:** you write a diode, you can actually write a diode
[00:24:45:619 - 00:24:47:420] **Speaker 1:** and turn as a function of voltage.
[00:24:47:699 - 00:24:50:239] **Speaker 1:** So you can imagine you can get quite complicated formulas.
[00:24:51:449 - 00:24:54:050] **Speaker 1:** Uh, and this, this particular one is no exception.
[00:24:54:910 - 00:24:57:520] **Speaker 1:** And it's depending on what else happens in the circuit.
[00:25:00:719 - 00:25:04:109] **Speaker 1:** But yeah, mostly just static components that you're putting together
[00:25:04:250 - 00:25:05:489] **Speaker 1:** and modelling a BJT.
[00:25:06:859 - 00:25:10:099] **Speaker 1:** And that's kind of how I with the TL 494
[00:25:10:099 - 00:25:14:579] **Speaker 1:** chip that I modelled that involves obviously lots of different
[00:25:14:579 - 00:25:15:540] **Speaker 1:** devices, but um.
[00:25:16:420 - 00:25:21:599] **Speaker 1:** Includes diodes and a couple of oppans and yeah that's,
[00:25:21:829 - 00:25:24:380] **Speaker 1:** that was all packaged together into the TL 494 chip
[00:25:24:380 - 00:25:24:969] **Speaker 1:** which you've used.
[00:25:32:729 - 00:25:33:829] **Speaker 1:** So yeah, that's that.
[00:25:35:760 - 00:25:38:160] **Speaker 1:** So I'm now moving on to.
[00:25:40:660 - 00:25:41:839] **Speaker 1:** Sort of a new area.
[00:25:42:819 - 00:25:46:239] **Speaker 1:** But it's related to analogue electronics, which is noise.
[00:25:47:819 - 00:25:48:760] **Speaker 1:** Like my title page.
[00:25:52:010 - 00:25:53:250] **Speaker 1:** It's obviously image processing.
[00:25:53:290 - 00:25:56:250] **Speaker 1:** If you've done any image processing, noise can really affect
[00:25:56:250 - 00:25:57:010] **Speaker 1:** image processing.
[00:26:00:290 - 00:26:01:359] **Speaker 1:** So lecture 13.
[00:26:03:670 - 00:26:05:770] **Speaker 1:** So I'm a little bit behind, but I'm basically keeping
[00:26:05:770 - 00:26:06:069] **Speaker 1:** up.
[00:26:08:290 - 00:26:08:300] **Speaker 1:** Just.
[00:26:13:369 - 00:26:14:290] **Speaker 1:** So let's have a look at this.
[00:26:14:479 - 00:26:16:750] **Speaker 1:** Define Johnson and shock noise.
[00:26:20:489 - 00:26:22:560] **Speaker 1:** Yeah, yeah, I could definitely ask a question on it,
[00:26:23:609 - 00:26:23:969] **Speaker 1:** um.
[00:26:25:709 - 00:26:27:770] **Speaker 1:** And I definitely have written the exam now, so.
[00:26:29:689 - 00:26:31:119] **Speaker 1:** You need to know them.
[00:26:32:430 - 00:26:35:670] **Speaker 1:** As in like the different types, but you may not
[00:26:35:670 - 00:26:37:839] **Speaker 1:** necessarily have to say what is Johnson noise, but I,
[00:26:37:880 - 00:26:39:839] **Speaker 1:** it has been asked in previous exams, so I will
[00:26:39:839 - 00:26:41:000] **Speaker 1:** say exam.
[00:26:43:989 - 00:26:46:010] **Speaker 1:** Yes, every year, like.
[00:26:47:290 - 00:26:47:890] **Speaker 1:** Asked.
[00:26:49:640 - 00:26:51:979] **Speaker 1:** Every year, forever.
[00:26:58:310 - 00:27:01:579] **Speaker 1:** Discuss common oper noise densities, um.
[00:27:03:119 - 00:27:04:380] **Speaker 1:** That's more.
[00:27:05:939 - 00:27:07:099] **Speaker 1:** summarised.
[00:27:09:910 - 00:27:14:739] **Speaker 1:** And I figure And it's basically, yeah, see you later.
[00:27:16:530 - 00:27:17:459] **Speaker 1:** But yeah, that's exam.
[00:27:19:869 - 00:27:23:270] **Speaker 1:** Computer operate noise figure for various source resistances, um, that's
[00:27:23:270 - 00:27:23:849] **Speaker 1:** also.
[00:27:25:209 - 00:27:27:130] **Speaker 1:** This kind of this comment here kind of applies to
[00:27:27:130 - 00:27:27:390] **Speaker 1:** both.
[00:27:35:839 - 00:27:36:189] **Speaker 1:** Yeah.
[00:27:37:439 - 00:27:40:060] **Speaker 1:** But yeah, I'm always asking, I'm always saying.
[00:27:40:790 - 00:27:45:550] **Speaker 1:** I know it's something like choose an op amp with
[00:27:45:550 - 00:27:50:109] **Speaker 1:** a certain current noise or voltage noise that gives you
[00:27:50:109 - 00:27:51:729] **Speaker 1:** a certain noise figure.
[00:27:52:160 - 00:27:53:390] **Speaker 1:** So it's like, yeah.
[00:27:56:599 - 00:27:57:800] **Speaker 1:** So that's definitely in the exam.
[00:28:00:400 - 00:28:02:510] **Speaker 1:** So yeah, that's my learning outcomes.
[00:28:03:760 - 00:28:04:449] **Speaker 1:** of 13.
[00:28:08:410 - 00:28:09:910] **Speaker 1:** Mostly all exeminable.
[00:28:11:920 - 00:28:15:000] **Speaker 1:** But I know I didn't actually ask to define Johnson
[00:28:15:000 - 00:28:16:839] **Speaker 1:** and Shot noise in the exam, but.
[00:28:17:949 - 00:28:18:699] **Speaker 1:** You should know it.
[00:28:25:479 - 00:28:31:229] **Speaker 1:** Noise White noise Is a very, it's it's used a
[00:28:31:229 - 00:28:31:650] **Speaker 1:** lot.
[00:28:32:510 - 00:28:33:329] **Speaker 1:** And modelling.
[00:28:33:829 - 00:28:36:229] **Speaker 1:** So white noise is just sort of like a randomly
[00:28:36:229 - 00:28:39:359] **Speaker 1:** it's It's a uniform distribution really.
[00:28:40:540 - 00:28:43:479] **Speaker 1:** So it means that if you do a faster transform
[00:28:43:479 - 00:28:47:540] **Speaker 1:** of white noise, you should be getting the same amplitude
[00:28:47:540 - 00:28:48:939] **Speaker 1:** across the whole band.
[00:28:49:689 - 00:28:50:869] **Speaker 1:** That's what white noise is.
[00:28:53:270 - 00:28:56:609] **Speaker 1:** It's really handy because you can shape, you can use
[00:28:56:609 - 00:28:58:670] **Speaker 1:** the white noise and what you can do is actually
[00:28:58:670 - 00:29:01:790] **Speaker 1:** put it into a transfer function to then model other
[00:29:01:790 - 00:29:04:520] **Speaker 1:** types of noise and to shape, shape it.
[00:29:05:020 - 00:29:07:229] **Speaker 1:** So it is a, it's an input into a lot
[00:29:07:229 - 00:29:11:069] **Speaker 1:** of modelling, a lot of different noise models.
[00:29:13:050 - 00:29:15:619] **Speaker 1:** And I mean it's good for modelling just even like
[00:29:15:619 - 00:29:18:819] **Speaker 1:** for example, I don't know turbulence in the uh in
[00:29:18:819 - 00:29:19:640] **Speaker 1:** the atmosphere.
[00:29:21:410 - 00:29:23:030] **Speaker 1:** And electronics, of course.
[00:29:24:099 - 00:29:25:140] **Speaker 1:** It is random.
[00:29:26:979 - 00:29:28:640] **Speaker 1:** So this part here.
[00:29:30:319 - 00:29:32:119] **Speaker 1:** This including this's just like the pure signal.
[00:29:32:199 - 00:29:36:339] **Speaker 1:** There's no randomness there, but you're adding white noise here
[00:29:36:880 - 00:29:38:239] **Speaker 1:** and that's the randomness.
[00:29:45:880 - 00:29:52:810] **Speaker 1:** And so that Is a model, white noise is a
[00:29:52:810 - 00:29:55:109] **Speaker 1:** model of random.
[00:29:56:420 - 00:29:57:520] **Speaker 1:** Fluctuations.
[00:30:04:069 - 00:30:06:569] **Speaker 1:** Or I should say it is a stochastic.
[00:30:09:520 - 00:30:14:349] **Speaker 1:** Mo This is different.
[00:30:14:510 - 00:30:17:270] **Speaker 1:** This is like a disturbance.
[00:30:17:589 - 00:30:19:910] **Speaker 1:** I wouldn't say this is random because it's AC hum.
[00:30:19:949 - 00:30:23:229] **Speaker 1:** You can predict often the amplitude and everything.
[00:30:23:339 - 00:30:25:170] **Speaker 1:** You can get a good predictive.
[00:30:27:270 - 00:30:28:310] **Speaker 1:** Model for that.
[00:30:28:859 - 00:30:31:349] **Speaker 1:** So this is deterministic.
[00:30:33:369 - 00:30:35:599] **Speaker 1:** To tame and mystic.
[00:30:36:750 - 00:30:38:989] **Speaker 1:** In the sense of the whole waveform.
[00:30:41:380 - 00:30:44:109] **Speaker 1:** But what's cool, what's really interesting about this whole noise
[00:30:44:109 - 00:30:45:310] **Speaker 1:** stuff that I'm going to be teaching you.
[00:30:47:109 - 00:30:50:310] **Speaker 1:** Is that it is, even though it's random, it actually
[00:30:50:310 - 00:30:51:890] **Speaker 1:** is quite predictable.
[00:30:52:699 - 00:30:57:140] **Speaker 1:** Like the stochastic properties of noise are quite predictable, and
[00:30:57:140 - 00:30:59:459] **Speaker 1:** you can plan for them and you can design for
[00:30:59:459 - 00:31:00:500] **Speaker 1:** them in your circuit.
[00:31:03:239 - 00:31:05:020] **Speaker 1:** And you'll need to design for them.
[00:31:08:319 - 00:31:11:729] **Speaker 1:** And when you get components, you should be thinking about
[00:31:11:920 - 00:31:14:209] **Speaker 1:** the amount of noise it adds to your circuit.
[00:31:14:760 - 00:31:18:719] **Speaker 1:** So it's, it is a really practical tool that you
[00:31:18:719 - 00:31:20:790] **Speaker 1:** will need to do, especially next year when you're going
[00:31:20:790 - 00:31:22:079] **Speaker 1:** to finding your project.
[00:31:34:020 - 00:31:37:800] **Speaker 1:** So here's the input voltage noise spectral density versus frequency.
[00:31:45:089 - 00:31:47:869] **Speaker 1:** Square root of power spectral density.
[00:31:50:920 - 00:31:52:579] **Speaker 1:** So the power spectral density.
[00:31:54:810 - 00:32:01:530] **Speaker 1:** Scroop power sexual density is essentially The FFT divided by
[00:32:01:530 - 00:32:04:530] **Speaker 1:** route 2 because you're dividing by route 2 because you're
[00:32:04:530 - 00:32:06:089] **Speaker 1:** normalising all the sine waves.
[00:32:07:369 - 00:32:08:849] **Speaker 1:** And then it gives you the RMS.
[00:32:20:219 - 00:32:22:239] **Speaker 1:** This is to do with thermal noise.
[00:32:28:109 - 00:32:29:430] **Speaker 1:** And what it is.
[00:32:30:619 - 00:32:32:969] **Speaker 1:** If you take the output of your circuit.
[00:32:33:939 - 00:32:37:699] **Speaker 1:** And the voltages depending on thermal noises affecting voltage, so
[00:32:37:699 - 00:32:39:000] **Speaker 1:** it's creating fluctuations.
[00:32:39:380 - 00:32:42:020] **Speaker 1:** And if you measure those, that's the output Y.
[00:32:42:339 - 00:32:43:560] **Speaker 1:** Take an FFT of it.
[00:32:46:170 - 00:32:48:520] **Speaker 1:** Then what you do is you divide by.
[00:32:49:780 - 00:32:53:229] **Speaker 1:** The FFT of white noise essentially, which is kind of
[00:32:53:229 - 00:32:55:400] **Speaker 1:** redundant because the FFT of white noise is just like
[00:32:55:400 - 00:32:57:250] **Speaker 1:** a single, right?
[00:32:57:680 - 00:33:01:780] **Speaker 1:** Every single frequency is the same amplitude and white noise.
[00:33:02:280 - 00:33:06:079] **Speaker 1:** So you get a completely flat body plot for every
[00:33:06:079 - 00:33:07:760] **Speaker 1:** single frequency.
[00:33:10:680 - 00:33:15:719] **Speaker 1:** And so, because, yeah, that's, so then it's effectively, even
[00:33:15:719 - 00:33:18:020] **Speaker 1:** though, so this is like a transfer function kind of.
[00:33:19:459 - 00:33:23:459] **Speaker 1:** Like you have your input white white noise going into
[00:33:23:459 - 00:33:26:359] **Speaker 1:** something and then you've got your output Y.
[00:33:27:030 - 00:33:28:290] **Speaker 1:** It's like a transfer function.
[00:33:29:020 - 00:33:31:390] **Speaker 1:** Why over the input, because white noise is the input
[00:33:31:390 - 00:33:33:229] **Speaker 1:** that you use for a lot of, you know, for
[00:33:33:229 - 00:33:33:930] **Speaker 1:** modelling noise.
[00:33:35:810 - 00:33:39:420] **Speaker 1:** And um Take the square of that and you'll get
[00:33:39:420 - 00:33:40:520] **Speaker 1:** the PSD of course.
[00:33:44:839 - 00:33:47:439] **Speaker 1:** Cause when you've done transfer functions for control systems, you're
[00:33:47:439 - 00:33:51:239] **Speaker 1:** used to putting like a deterministic known signal into your
[00:33:51:239 - 00:33:53:479] **Speaker 1:** transfer function as a black box and then uh then
[00:33:53:479 - 00:33:55:760] **Speaker 1:** a predictable signal comes out.
[00:33:56:839 - 00:33:59:119] **Speaker 1:** And so you have to kind of be in your
[00:33:59:119 - 00:34:02:020] **Speaker 1:** brain and think of it in terms of more stochastic
[00:34:02:239 - 00:34:03:140] **Speaker 1:** transfer function.
[00:34:03:599 - 00:34:06:060] **Speaker 1:** We have this random noise signal.
[00:34:07:329 - 00:34:08:709] **Speaker 1:** Uh, that's going up and down.
[00:34:09:398 - 00:34:12:120] **Speaker 1:** And so you can visualise the transfer function really just
[00:34:12:120 - 00:34:14:280] **Speaker 1:** in terms of the FFT of the output because the
[00:34:14:280 - 00:34:15:739] **Speaker 1:** FFT of the input is just one.
[00:34:17:830 - 00:34:19:388] **Speaker 1:** And so it has given you a model.
[00:34:19:469 - 00:34:21:270] **Speaker 1:** So if you just took all the wind speed, if
[00:34:21:270 - 00:34:23:020] **Speaker 1:** you just measured wind speed, which I've done in a
[00:34:23:020 - 00:34:25:070] **Speaker 1:** balloon, you go up and you take the wind speed.
[00:34:26:300 - 00:34:29:020] **Speaker 1:** And you do the FFT of the wind speed over
[00:34:29:020 - 00:34:31:800] **Speaker 1:** time, it would look something like this and you can
[00:34:31:800 - 00:34:33:800] **Speaker 1:** and then you can model as a transfer function.
[00:34:34:759 - 00:34:37:339] **Speaker 1:** Like 1 over S + 1 could be a model
[00:34:37:708 - 00:34:40:759] **Speaker 1:** of wind speed, but you don't just put a voltage
[00:34:40:759 - 00:34:42:519] **Speaker 1:** sign onto it, you just like put white noise into
[00:34:42:519 - 00:34:42:888] **Speaker 1:** it.
[00:34:43:357 - 00:34:46:799] **Speaker 1:** It's, it's a shaping philtre and then the output will
[00:34:46:799 - 00:34:49:117] **Speaker 1:** act like wind speed.
[00:34:51:090 - 00:34:54:290] **Speaker 1:** Another really uh simple philtre is just like integrate if
[00:34:54:290 - 00:34:56:439] **Speaker 1:** you just generate if you try it on on Matlab
[00:34:56:439 - 00:34:59:649] **Speaker 1:** it's really interesting if you just like put rend I
[00:34:59:649 - 00:35:02:020] **Speaker 1:** know reined in is like I think that's normal distributed
[00:35:02:020 - 00:35:02:510] **Speaker 1:** noise.
[00:35:03:439 - 00:35:05:100] **Speaker 1:** And you generate a time series.
[00:35:06:040 - 00:35:08:679] **Speaker 1:** If you integrate that with QM traps in MATLAB.
[00:35:09:489 - 00:35:12:719] **Speaker 1:** It, yeah, it kinda looks like a random walk.
[00:35:13:340 - 00:35:16:580] **Speaker 1:** It's kind of wandering around, yeah, and that's kind of
[00:35:16:580 - 00:35:19:419] **Speaker 1:** a good model just like a 1 overs transfer function
[00:35:19:800 - 00:35:21:399] **Speaker 1:** can model a random walk.
[00:35:26:810 - 00:35:29:520] **Speaker 1:** Alright, let's get on to uh what Johnson Noise is
[00:35:29:520 - 00:35:30:070] **Speaker 1:** briefly.
[00:35:31:330 - 00:35:32:350] **Speaker 1:** Resistant material.
[00:35:34:189 - 00:35:37:629] **Speaker 1:** It's very dependent on temperature, it's also dependent on bandwidth
[00:35:37:629 - 00:35:39:149] **Speaker 1:** and it involves the Boltzmann's constant.
[00:35:39:189 - 00:35:40:750] **Speaker 1:** This is an incredible formula.
[00:35:42:090 - 00:35:45:290] **Speaker 1:** Because this quite accurately predicts.
[00:35:46:360 - 00:35:49:120] **Speaker 1:** What the RMS or the voltage noise will be.
[00:35:50:090 - 00:35:51:260] **Speaker 1:** Given the temperature.
[00:35:51:370 - 00:35:53:290] **Speaker 1:** So if you can know what the temperature you're getting
[00:35:53:290 - 00:35:57:000] **Speaker 1:** at, and you know your resistance, you provide the bandwidth,
[00:35:57:530 - 00:35:59:070] **Speaker 1:** you can already, you can work it out.
[00:36:02:520 - 00:36:05:679] **Speaker 1:** So there is a kind of a predictable part of
[00:36:05:679 - 00:36:07:419] **Speaker 1:** this, even though it is random.
[00:36:08:840 - 00:36:09:899] **Speaker 1:** White noise involved.
[00:36:15:270 - 00:36:18:750] **Speaker 1:** So let's just say room temperature 298 kelvin is pretty
[00:36:18:750 - 00:36:19:409] **Speaker 1:** common for that.
[00:36:20:389 - 00:36:22:530] **Speaker 1:** This is a 1 kilohm resistor.
[00:36:24:260 - 00:36:25:830] **Speaker 1:** Then you can work out.
[00:36:27:439 - 00:36:29:889] **Speaker 1:** What the RMS voltage noise is gonna be, so you
[00:36:29:889 - 00:36:30:909] **Speaker 1:** just plug it in.
[00:36:32:679 - 00:36:34:540] **Speaker 1:** You go 4 times.
[00:36:35:629 - 00:36:38:959] **Speaker 1:** 1.38 times 10.
[00:36:39:080 - 00:36:41:320] **Speaker 1:** These are incredible, some of these constants that seem to
[00:36:41:320 - 00:36:42:340] **Speaker 1:** exist in the universe.
[00:36:43:020 - 00:36:44:560] **Speaker 1:** It's another amazing constant.
[00:36:45:469 - 00:36:46:770] **Speaker 1:** The Boltzmann's constant.
[00:36:49:800 - 00:36:50:979] **Speaker 1:** Why do they exist?
[00:36:51:399 - 00:36:52:139] **Speaker 1:** I don't know.
[00:36:53:360 - 00:36:54:179] **Speaker 1:** They just do.
[00:36:54:760 - 00:36:57:310] **Speaker 1:** As a scientist, I measure it, because I, because I'm
[00:36:57:310 - 00:36:59:600] **Speaker 1:** defining engineering as science, right, so I can say I'm
[00:36:59:600 - 00:37:00:219] **Speaker 1:** a scientist.
[00:37:01:000 - 00:37:02:489] **Speaker 1:** But I, I don't say I'm a scientist, I normally
[00:37:02:489 - 00:37:04:540] **Speaker 1:** say I'm an engineer, I say I'm a rocket engineer.
[00:37:05:340 - 00:37:08:209] **Speaker 1:** Because scientists I think I've lost their way a little
[00:37:08:209 - 00:37:08:510] **Speaker 1:** bit.
[00:37:08:770 - 00:37:10:229] **Speaker 1:** I think engineering should be.
[00:37:10:949 - 00:37:14:360] **Speaker 1:** The true science It's mainly my humble opinion.
[00:37:20:800 - 00:37:23:929] **Speaker 1:** I just like having the real world as a feedback.
[00:37:28:510 - 00:37:29:530] **Speaker 1:** Onto my maths.
[00:37:32:139 - 00:37:34:310] **Speaker 1:** That's why I find engineering is my home, even though
[00:37:34:310 - 00:37:35:250] **Speaker 1:** I'm a mathematician.
[00:37:36:020 - 00:37:36:989] **Speaker 1:** I feel right at home here.
[00:37:39:850 - 00:37:40:449] **Speaker 1:** So there you go.
[00:37:40:610 - 00:37:42:629] **Speaker 1:** So 4 nanovolts per squareHz.
[00:37:42:770 - 00:37:45:389] **Speaker 1:** That's the, the weird units because it's square root.
[00:37:47:830 - 00:37:49:209] **Speaker 1:** This is called a density.
[00:37:54:989 - 00:37:57:739] **Speaker 1:** Then of course if we increase the bandwidth.
[00:38:01:209 - 00:38:03:909] **Speaker 1:** You would expect to get a lot more noise.
[00:38:12:989 - 00:38:15:189] **Speaker 1:** So again, you can go through this calculation.
[00:38:17:510 - 00:38:21:050] **Speaker 1:** Times 1.38 times 10 to -23.
[00:38:21:580 - 00:38:22:469] **Speaker 1:** I don't know if I really need to write it
[00:38:22:469 - 00:38:23:909] **Speaker 1:** out again, but I think I just will, just for
[00:38:23:909 - 00:38:24:189] **Speaker 1:** fun.
[00:38:27:639 - 00:38:30:280] **Speaker 1:** Plugging all those numbers in gives you.
[00:38:31:050 - 00:38:32:489] **Speaker 1:** 128 nanovolts.
[00:38:32:570 - 00:38:35:169] **Speaker 1:** So you, you can predict what the voltage noise is
[00:38:35:169 - 00:38:35:530] **Speaker 1:** gonna be.
[00:38:35:810 - 00:38:37:489] **Speaker 1:** It's incredible that you can do that.
[00:38:37:889 - 00:38:41:949] **Speaker 1:** It's random and you, you can predict quite accurately.
[00:38:42:969 - 00:38:45:969] **Speaker 1:** What the voltage noise will be if you change your
[00:38:45:969 - 00:38:46:550] **Speaker 1:** bandwidth.
[00:38:50:560 - 00:38:53:070] **Speaker 1:** And shot noise is the same.
[00:38:55:370 - 00:38:57:520] **Speaker 1:** You got a formula and you can it is a,
[00:38:57:600 - 00:38:59:250] **Speaker 1:** there's a little bit more difficulty there because it's with
[00:38:59:250 - 00:39:00:149] **Speaker 1:** semiconductors.
[00:39:01:239 - 00:39:02:820] **Speaker 1:** And it can be harder to work out.
[00:39:03:929 - 00:39:06:340] **Speaker 1:** But normally that's given on the spec sheets for like
[00:39:06:340 - 00:39:09:590] **Speaker 1:** offhamps and things you get given the um the shot
[00:39:09:590 - 00:39:10:120] **Speaker 1:** noise.
[00:39:11:560 - 00:39:12:979] **Speaker 1:** But it's completely predictable.
[00:39:13:770 - 00:39:16:090] **Speaker 1:** So when you buy an op amp, it tells you
[00:39:16:090 - 00:39:17:969] **Speaker 1:** what the shot noise will be, it tells you the
[00:39:17:969 - 00:39:19:850] **Speaker 1:** current noise in the spec sheet.
[00:39:21:139 - 00:39:23:260] **Speaker 1:** So you can put that into your noise calculations and
[00:39:23:260 - 00:39:24:679] **Speaker 1:** I'll be showing you how to do that later.
[00:39:25:439 - 00:39:27:899] **Speaker 1:** And that can that can inform like the certain op
[00:39:27:899 - 00:39:30:520] **Speaker 1:** amps that have high current noise and low voltage noise
[00:39:30:520 - 00:39:32:320] **Speaker 1:** or high voltage noise and low current noise.
[00:39:32:800 - 00:39:35:280] **Speaker 1:** So it depends on your whole circuit which op amp
[00:39:35:280 - 00:39:35:709] **Speaker 1:** you choose.
[00:39:35:800 - 00:39:37:919] **Speaker 1:** So that's something I want to be able to teach
[00:39:37:919 - 00:39:40:360] **Speaker 1:** you is to some kind of rules of thumb, some
[00:39:40:360 - 00:39:42:959] **Speaker 1:** techniques for optimal choice of op amp.
[00:39:43:750 - 00:39:45:810] **Speaker 1:** Considering noise properties.
[00:39:47:840 - 00:39:48:590] **Speaker 1:** So that's that.
[00:39:51:379 - 00:39:52:909] **Speaker 1:** So we have flicker noise.
[00:39:59:000 - 00:40:00:050] **Speaker 1:** Look a noise.
[00:40:01:989 - 00:40:03:770] **Speaker 1:** is a lot harder.
[00:40:05:459 - 00:40:08:100] **Speaker 1:** And that can be a problem, and that's because it's
[00:40:08:100 - 00:40:12:280] **Speaker 1:** very difficult to reproduce a surface precisely every time.
[00:40:13:550 - 00:40:18:010] **Speaker 1:** Temperature is a lot easier to control than material surface
[00:40:18:010 - 00:40:18:590] **Speaker 1:** properties.
[00:40:20:370 - 00:40:22:169] **Speaker 1:** You can always have a heat sink or you know
[00:40:22:169 - 00:40:23:050] **Speaker 1:** you can have a control system.
[00:40:23:090 - 00:40:24:459] **Speaker 1:** You have a temperature sensor in there.
[00:40:24:810 - 00:40:27:050] **Speaker 1:** It's hard to have a material surface sensor.
[00:40:27:489 - 00:40:30:209] **Speaker 1:** I suppose it's doable, but it's, it's a no it's
[00:40:30:209 - 00:40:31:610] **Speaker 1:** such a much harder problem to do.
[00:40:31:760 - 00:40:35:209] **Speaker 1:** So it becomes very like.
[00:40:36:310 - 00:40:40:100] **Speaker 1:** Unpredictable And but it's just that it's a low, it's
[00:40:40:100 - 00:40:42:649] **Speaker 1:** a low frequency, so in most cases we don't worry
[00:40:42:649 - 00:40:44:580] **Speaker 1:** about it, but you do sometimes have to take that
[00:40:44:580 - 00:40:45:239] **Speaker 1:** into account.
[00:40:45:659 - 00:40:47:639] **Speaker 1:** And really the only way to do that is experiment.
[00:40:48:939 - 00:40:51:330] **Speaker 1:** You can't really plan for it, you just have to
[00:40:51:330 - 00:40:53:050] **Speaker 1:** do the best you can, get as smooth a surface
[00:40:53:050 - 00:40:54:040] **Speaker 1:** as possible, and then.
[00:40:55:449 - 00:40:57:469] **Speaker 1:** Test it, see what happens.
[00:40:57:969 - 00:40:59:850] **Speaker 1:** But the advantage of the other types of noises is
[00:40:59:850 - 00:41:02:189] **Speaker 1:** you can plan it into your circuit design.
[00:41:03:629 - 00:41:05:429] **Speaker 1:** And so you can know how it's gonna behave using
[00:41:05:429 - 00:41:07:570] **Speaker 1:** some simulation tools like LTSpice for example.
[00:41:09:770 - 00:41:10:250] **Speaker 1:** Um.
[00:41:11:590 - 00:41:11:969] **Speaker 1:** Yeah.
[00:41:12:169 - 00:41:14:169] **Speaker 1:** And there's lots of other quite care.
[00:41:14:280 - 00:41:15:870] **Speaker 1:** There's lots of other tools as well.
[00:41:18:860 - 00:41:21:600] **Speaker 1:** So, signal to noise ratio.
[00:41:24:110 - 00:41:26:370] **Speaker 1:** So I'm getting into a noise.
[00:41:29:429 - 00:41:31:270] **Speaker 1:** Oh yeah, did I, I didn't actually show that slide,
[00:41:31:350 - 00:41:32:379] **Speaker 1:** but I'll be nice.
[00:41:35:409 - 00:41:36:189] **Speaker 1:** You missed it.
[00:41:36:810 - 00:41:39:050] **Speaker 1:** Too late, it's gone to echo now.
[00:41:45:449 - 00:41:47:530] **Speaker 1:** So signal to noise ratio, there's a few little terms
[00:41:47:530 - 00:41:51:929] **Speaker 1:** I wanna kinda introduce before I get into a single
[00:41:51:929 - 00:41:52:830] **Speaker 1:** op amp noise model.
[00:41:56:290 - 00:41:58:250] **Speaker 1:** So I'd like you to understand the concept of signal
[00:41:58:250 - 00:42:00:350] **Speaker 1:** to noise ratio, if you haven't seen this before.
[00:42:02:389 - 00:42:03:399] **Speaker 1:** Signal to noise.
[00:42:03:520 - 00:42:07:219] **Speaker 1:** This particular definition is wide band.
[00:42:12:090 - 00:42:15:149] **Speaker 1:** It's like, what's the signal voltage.
[00:42:16:629 - 00:42:19:270] **Speaker 1:** The water boy, the noise voltage.
[00:42:21:090 - 00:42:23:570] **Speaker 1:** And you take the ratio, so you'd always take the
[00:42:23:570 - 00:42:25:030] **Speaker 1:** squares, that's how it works.
[00:42:26:219 - 00:42:30:010] **Speaker 1:** Because noise and noise land and like statistical land, you
[00:42:30:010 - 00:42:32:770] **Speaker 1:** always like have covariances you always have to take squared
[00:42:32:770 - 00:42:35:530] **Speaker 1:** or some squared of of the signal and that's kind
[00:42:35:530 - 00:42:37:010] **Speaker 1:** of what RMS is but then you take the square
[00:42:37:010 - 00:42:38:530] **Speaker 1:** root of the sum square which is RMS.
[00:42:38:969 - 00:42:42:370] **Speaker 1:** But if you take the covariance and you take Um,
[00:42:42:639 - 00:42:44:750] **Speaker 1:** power spectral density, for example, that's all in terms of
[00:42:44:750 - 00:42:45:310] **Speaker 1:** the squares.
[00:42:45:389 - 00:42:49:250] **Speaker 1:** So even though is dividing the squares is what's important.
[00:42:50:729 - 00:42:52:370] **Speaker 1:** That's that's the definition.
[00:42:52:570 - 00:42:53:550] **Speaker 1:** And it's in decibels.
[00:42:57:120 - 00:42:58:500] **Speaker 1:** So 20 logged in.
[00:43:01:790 - 00:43:04:790] **Speaker 1:** It's also the same as 2010 of the ratio.
[00:43:05:939 - 00:43:07:909] **Speaker 1:** But it's normally just written as teen or teen of
[00:43:07:909 - 00:43:08:510] **Speaker 1:** the squares.
[00:43:14:010 - 00:43:16:550] **Speaker 1:** And then you get a similar definition for current.
[00:43:22:449 - 00:43:24:040] **Speaker 1:** But it is the traditional what you think.
[00:43:24:090 - 00:43:27:149] **Speaker 1:** It's the output signal divided by the input or the
[00:43:27:149 - 00:43:28:510] **Speaker 1:** output signal divided by the noise.
[00:43:29:729 - 00:43:33:129] **Speaker 1:** And the higher this value is, obviously the better the
[00:43:33:129 - 00:43:35:689] **Speaker 1:** signal strength is and the better relative to the noise.
[00:43:35:729 - 00:43:38:010] **Speaker 1:** It's just like you get a nice clean signal if
[00:43:38:010 - 00:43:39:310] **Speaker 1:** that number's really big.
[00:43:43:399 - 00:43:45:550] **Speaker 1:** Of course our current ratios that I've mentioned there.
[00:43:47:379 - 00:43:51:310] **Speaker 1:** But keep in mind that If you want to get
[00:43:51:310 - 00:43:53:729] **Speaker 1:** the values for the signal to noise ratio.
[00:43:54:889 - 00:43:57:520] **Speaker 1:** So if you wanna get These.
[00:43:58:260 - 00:44:00:050] **Speaker 1:** Amis values.
[00:44:02:510 - 00:44:06:590] **Speaker 1:** You need to specify a bandwidth that you're gonna be
[00:44:06:590 - 00:44:07:429] **Speaker 1:** operating around.
[00:44:13:439 - 00:44:15:520] **Speaker 1:** There may be a certain part of the band where
[00:44:15:520 - 00:44:18:320] **Speaker 1:** you're getting excessive noise it's causing a bit of a
[00:44:18:320 - 00:44:21:280] **Speaker 1:** problem, so you might divide, you might create a band
[00:44:21:280 - 00:44:23:760] **Speaker 1:** pass philtre you wanna knock out or you may want
[00:44:23:760 - 00:44:26:320] **Speaker 1:** to pass a certain signal through that and then knock
[00:44:26:320 - 00:44:27:379] **Speaker 1:** out other frequencies.
[00:44:27:959 - 00:44:30:399] **Speaker 1:** A notcher, for example, would actually knock out a whole
[00:44:30:399 - 00:44:31:979] **Speaker 1:** band of of noise.
[00:44:33:540 - 00:44:35:860] **Speaker 1:** And might even just knock out a single frequency in
[00:44:35:860 - 00:44:36:620] **Speaker 1:** some cases.
[00:44:38:580 - 00:44:40:219] **Speaker 1:** Or it might just be a band of noise.
[00:44:40:739 - 00:44:44:639] **Speaker 1:** So noise figure, noise power density, Johnson noise, uh, is,
[00:44:45:090 - 00:44:47:610] **Speaker 1:** I've explained that in the previous slide, is a square
[00:44:47:610 - 00:44:50:370] **Speaker 1:** root of 4k times the temperature times R, but this
[00:44:50:370 - 00:44:54:439] **Speaker 1:** is density, so you put the bandwidth to be 1.
[00:44:55:489 - 00:44:57:360] **Speaker 1:** That's why it's a density.
[00:44:58:889 - 00:45:00:459] **Speaker 1:** And if you put it to be one.
[00:45:01:790 - 00:45:07:830] **Speaker 1:** The units will be volts per square of hertz.
[00:45:09:219 - 00:45:11:600] **Speaker 1:** a neat kind of a, just another way of writing
[00:45:11:600 - 00:45:11:709] **Speaker 1:** it.
[00:45:11:810 - 00:45:12:909] **Speaker 1:** So it's just a definition.
[00:45:15:800 - 00:45:18:979] **Speaker 1:** And uh that's gonna be what the noise.
[00:45:20:689 - 00:45:25:209] **Speaker 1:** To be specific, it's V noise RMS divided by the
[00:45:25:209 - 00:45:26:469] **Speaker 1:** square root of bandwidth.
[00:45:27:330 - 00:45:29:929] **Speaker 1:** And then the band with Is one.
[00:45:32:310 - 00:45:35:350] **Speaker 1:** Then you take the power density, which is volts squares
[00:45:35:350 - 00:45:35:899] **Speaker 1:** per Hz.
[00:45:38:510 - 00:45:40:229] **Speaker 1:** Shot noise, is that?
[00:45:41:639 - 00:45:43:739] **Speaker 1:** Power density, can you hit square.
[00:45:45:550 - 00:45:48:969] **Speaker 1:** And that will be amp 2 per Hz.
[00:45:50:840 - 00:45:52:010] **Speaker 1:** A few definitions for you.
[00:45:53:530 - 00:45:55:830] **Speaker 1:** 5 minutes left and I've got one slide actually um.
[00:45:56:719 - 00:45:56:979] **Speaker 1:** Hm.
[00:45:59:129 - 00:46:00:090] **Speaker 1:** It was good timing.
[00:46:00:399 - 00:46:01:800] **Speaker 1:** I should be able to finish this in 5 minutes,
[00:46:01:879 - 00:46:02:419] **Speaker 1:** I think.
[00:46:06:459 - 00:46:09:899] **Speaker 1:** So here is a single op amp noise model.
[00:46:12:629 - 00:46:14:629] **Speaker 1:** So, what do we got here?
[00:46:15:520 - 00:46:19:110] **Speaker 1:** So we have her up in, we've got current noise.
[00:46:20:409 - 00:46:22:580] **Speaker 1:** But the current noise is shock noise because it's a
[00:46:22:580 - 00:46:23:479] **Speaker 1:** semiconductor.
[00:46:29:679 - 00:46:32:989] **Speaker 1:** Normally you have IN + equal to minus, that's just
[00:46:32:989 - 00:46:33:850] **Speaker 1:** about always the case.
[00:46:34:919 - 00:46:39:500] **Speaker 1:** Most um Usually.
[00:46:41:389 - 00:46:45:090] **Speaker 1:** IN minus equals IN plus, let's keep that in mind.
[00:46:45:810 - 00:46:46:969] **Speaker 1:** It's a shock noise.
[00:46:50:260 - 00:46:54:260] **Speaker 1:** Inside the LPAM EN that is Johnson Noise.
[00:46:56:580 - 00:46:58:100] **Speaker 1:** But you don't want to be going in and finding
[00:46:58:100 - 00:47:00:139] **Speaker 1:** out how many resistors there are inside of an op
[00:47:00:139 - 00:47:00:500] **Speaker 1:** amp.
[00:47:00:729 - 00:47:02:520] **Speaker 1:** So they've already worked that out for you.
[00:47:03:020 - 00:47:04:540] **Speaker 1:** When you buy the op amp, you'll know what the
[00:47:04:540 - 00:47:05:639] **Speaker 1:** Johnson noise is.
[00:47:06:679 - 00:47:07:899] **Speaker 1:** It'll it'll tell you.
[00:47:12:340 - 00:47:16:909] **Speaker 1:** So now, How we kind of represent this.
[00:47:18:129 - 00:47:21:290] **Speaker 1:** You always infer noise to the input.
[00:47:23:330 - 00:47:27:550] **Speaker 1:** Because like you know with uh with this non-inverting configuration,
[00:47:27:629 - 00:47:29:159] **Speaker 1:** this is like an amplifier.
[00:47:29:629 - 00:47:32:669] **Speaker 1:** It's gonna be amplifying your input into the output.
[00:47:33:389 - 00:47:36:550] **Speaker 1:** So, obviously what you care about is the noise is
[00:47:36:550 - 00:47:38:969] **Speaker 1:** gonna be amplified and this and this is a noise
[00:47:38:969 - 00:47:41:270] **Speaker 1:** that's gonna be affected downstream in your circuit.
[00:47:42:909 - 00:47:46:590] **Speaker 1:** But the way that you treat noise is what really
[00:47:46:590 - 00:47:48:370] **Speaker 1:** matters is the input noise.
[00:47:48:790 - 00:47:51:550] **Speaker 1:** And so you always refer noise to the input because
[00:47:51:550 - 00:47:53:429] **Speaker 1:** then you know you're gonna just times by number to
[00:47:53:429 - 00:47:54:030] **Speaker 1:** get the output.
[00:47:55:500 - 00:47:58:649] **Speaker 1:** So it is the convention that you always refer it
[00:47:58:649 - 00:47:59:389] **Speaker 1:** to the input.
[00:48:00:540 - 00:48:02:760] **Speaker 1:** And if you're wanting to work out the noise.
[00:48:04:489 - 00:48:10:820] **Speaker 1:** In this case, Uh Noise properties you just assume everything's
[00:48:10:820 - 00:48:12:969] **Speaker 1:** zero for a start, like if you wanna say what's
[00:48:12:969 - 00:48:14:439] **Speaker 1:** the input what what are these gonna do?
[00:48:16:629 - 00:48:19:439] **Speaker 1:** You want EN and IN to be 0 if you
[00:48:19:439 - 00:48:21:580] **Speaker 1:** want to see the effect of the resistant noises.
[00:48:22:429 - 00:48:23:489] **Speaker 1:** So you just assume.
[00:48:24:750 - 00:48:30:229] **Speaker 1:** First First a shame.
[00:48:31:110 - 00:48:33:169] **Speaker 1:** N equals 0 and iron equals 0.
[00:48:34:610 - 00:48:38:479] **Speaker 1:** Um This is To analyse.
[00:48:40:429 - 00:48:40:959] **Speaker 1:** I pack.
[00:48:42:939 - 00:48:45:090] **Speaker 1:** Of resistance.
[00:48:46:479 - 00:48:47:370] **Speaker 1:** On noise.
[00:48:53:659 - 00:48:56:139] **Speaker 1:** And so if you see EN to be 0 and
[00:48:56:139 - 00:48:57:320] **Speaker 1:** IN to be 0.
[00:48:58:709 - 00:49:04:040] **Speaker 1:** Then You're gonna have a ground here.
[00:49:05:870 - 00:49:08:350] **Speaker 1:** This will be if that's VA.
[00:49:09:610 - 00:49:11:090] **Speaker 1:** The unknown voters who are going to wake up.
[00:49:14:429 - 00:49:16:790] **Speaker 1:** And if I take this.
[00:49:17:889 - 00:49:25:929] **Speaker 0:** Here Go up to here, I'm gonna rewrite it so
[00:49:25:929 - 00:49:27:989] **Speaker 1:** that you can see it a little bit more clearly.
[00:49:41:500 - 00:49:43:540] **Speaker 1:** They they're both grounds, so these are connected.
[00:49:50:739 - 00:49:57:399] **Speaker 1:** So what What does VEC when it looks through those
[00:49:57:399 - 00:49:58:080] **Speaker 1:** resistors?
[00:50:00:899 - 00:50:01:899] **Speaker 1:** It says this.
[00:50:03:709 - 00:50:05:199] **Speaker 1:** Its seats parallel.
[00:50:06:340 - 00:50:07:409] **Speaker 1:** Parallel resistance.
[00:50:13:750 - 00:50:14:679] **Speaker 1:** So let's just write that.
[00:50:16:300 - 00:50:19:080] **Speaker 1:** If you happen to be a person looking down here.
[00:50:20:159 - 00:50:22:159] **Speaker 1:** They would see parallel resistors.
[00:50:28:840 - 00:50:31:719] **Speaker 1:** And so you would get the the traditional formula.
[00:50:34:689 - 00:50:35:159] **Speaker 1:** Yeah.
[00:50:40:399 - 00:50:43:189] **Speaker 1:** But noise is referred to the input.
[00:50:44:050 - 00:50:49:050] **Speaker 1:** It's just like As I was saying before, noise is
[00:50:49:050 - 00:50:49:919] **Speaker 1:** referred.
[00:50:52:129 - 00:50:53:510] **Speaker 1:** To the input.
[00:50:58:219 - 00:51:00:649] **Speaker 1:** And so what you end up getting is.
[00:51:01:979 - 00:51:07:139] **Speaker 1:** Just the formula For like the Boltzmann's constant times the
[00:51:07:139 - 00:51:12:020] **Speaker 1:** temperature times the resistance that you see that the resistance,
[00:51:12:459 - 00:51:15:520] **Speaker 1:** effective resistance is a parallel resistance.
[00:51:16:020 - 00:51:17:879] **Speaker 1:** So noise behaves in the same way.
[00:51:20:580 - 00:51:22:060] **Speaker 1:** So that's a pretty neat result actually.
[00:51:23:110 - 00:51:25:790] **Speaker 1:** That that noise is still going and you can actually
[00:51:25:790 - 00:51:26:489] **Speaker 1:** run through Ko laws.
[00:51:26:870 - 00:51:29:229] **Speaker 1:** I've um I haven't bothered doing this, but it's.
[00:51:30:010 - 00:51:30:719] **Speaker 1:** It works.
[00:51:30:770 - 00:51:33:550] **Speaker 1:** All the statistics all work in the same way.
[00:51:34:959 - 00:51:37:350] **Speaker 1:** And then you can see that the variance of VA.
[00:51:38:199 - 00:51:39:110] **Speaker 1:** Or the square.
[00:51:40:639 - 00:51:44:239] **Speaker 1:** Ends up being 4 kT times that parallel resistance, which
[00:51:44:239 - 00:51:47:020] **Speaker 1:** is this, and it's 4 kT that.
[00:51:47:469 - 00:51:52:439] **Speaker 1:** And then you add Um, the, the square of the
[00:51:52:439 - 00:51:53:260] **Speaker 1:** Johnson noise.
[00:51:55:399 - 00:51:57:310] **Speaker 1:** See, I'm not, I didn't, I'm, I'm a little bit
[00:51:57:310 - 00:51:58:270] **Speaker 1:** over, but um.
[00:51:59:540 - 00:52:00:639] **Speaker 1:** I got real close.
[00:52:02:629 - 00:52:03:429] **Speaker 1:** Probably finish it.
[00:52:03:790 - 00:52:05:360] **Speaker 1:** I don't want to go too much over because.
[00:52:09:030 - 00:52:10:709] **Speaker 1:** I'll talk about that team uh next time.
[00:52:11:860 - 00:52:13:919] **Speaker 1:** I don't wanna go too much over.
[00:52:16:510 - 00:52:17:820] **Speaker 1:** I nearly finished the slide.
[00:52:19:439 - 00:52:22:330] **Speaker 1:** And that's just inferred from again the parallel resistance.
[00:52:22:560 - 00:52:25:080] **Speaker 1:** You always sum the squares because that's the way that
[00:52:25:560 - 00:52:27:979] **Speaker 1:** this doesn't look like a square but it actually is
[00:52:28:520 - 00:52:30:020] **Speaker 1:** because maybe there's that square rooted thing.
[00:52:31:530 - 00:52:34:449] **Speaker 1:** So you always sum squares whenever you're looking at noise
[00:52:34:449 - 00:52:35:090] **Speaker 1:** contributions.
[00:52:35:250 - 00:52:36:770] **Speaker 1:** That's the way statistics works.
[00:52:37:120 - 00:52:37:909] **Speaker 1:** That's all I can say.
[00:52:38:939 - 00:52:39:639] **Speaker 1:** So I'll leave it there.
[00:52:39:919 - 00:52:40:300] **Speaker 1:** Thank you.
[00:52:53:669 - 00:53:03:179] **Speaker 0:** I was I'm gonna I'm gonna, I'll duty with the.
[00:53:05:709 - 00:53:06:320] **Speaker 0:** You're chilling, bro.
[00:53:11:090 - 00:53:12:169] **Speaker 0:** I might have to do the.
[00:53:13:169 - 00:53:16:030] **Speaker 0:** Why did you get I think it's changed much.
[00:53:18:790 - 00:53:20:469] **Speaker 0:** No, I.
[00:53:22:780 - 00:53:24:449] **Speaker 0:** I'm sorry.
[00:53:30:610 - 00:53:30:969] **Speaker 0:** Yeah, I'll I'll.
[00:53:35:489 - 00:53:35:689] **Speaker 0:** Yeah.
[00:53:35:699 - 00:53:36:899] **Speaker 0:** It's real good at like.
[00:53:38:939 - 00:53:39:070] **Speaker 0:** Yeah, very soon I'm working on it full on.
[00:53:49:469 - 00:53:50:030] **Speaker 1:** thanks for reminding me.
[00:53:50:070 - 00:53:51:709] **Speaker 1:** I'll try and get it soonish.
[00:53:53:989 - 00:53:55:209] **Speaker 1:** Yeah, yeah, I better send it out today.
[00:53:56:270 - 00:53:57:330] **Speaker 1:** Yeah, OK.
[00:53:59:209 - 00:53:59:219] **Speaker 0:** Please.
[00:54:09:750 - 00:54:12:929] **Speaker 2:** Um, So the two people I asked one of them
[00:54:12:929 - 00:54:13:929] **Speaker 2:** he was like, it's OK.
[00:54:15:060 - 00:54:19:260] **Speaker 2:** He's like it's OK, um, like he, he said something
[00:54:19:260 - 00:54:19:939] **Speaker 2:** along the lines of.
[00:54:20:629 - 00:54:21:909] **Speaker 2:** You just asked the wrong people.
[00:54:22:590 - 00:54:22:979] **Speaker 0:** Oh

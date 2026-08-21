# ENME302-26S2 Lecture 22 native Echo transcript

Date: August 19, 2026 11:00am-11:55am
Transcript type: native Echo automated transcript.

[00:00:07:849 - 00:00:07:860] **Speaker 0:** Yeah.
[00:00:20:860 - 00:00:20:870] **Speaker 0:** Yeah.
[00:00:27:379 - 00:00:37:040] **Speaker 0:** US Oh Well, uh, good morning, we'll make a start.
[00:00:39:259 - 00:00:41:729] **Speaker 1:** Um, so today we're gonna finish off chapter two of
[00:00:41:729 - 00:00:44:139] **Speaker 1:** the notes and then we'll talk a bit about the
[00:00:44:139 - 00:00:47:020] **Speaker 1:** quiz, quiz one, and then talk about console because that's
[00:00:47:020 - 00:00:48:560] **Speaker 1:** what we're going to do in the labs this week.
[00:00:49:049 - 00:00:52:900] **Speaker 1:** Um, and then I, if I update things on the
[00:00:52:900 - 00:00:56:319] **Speaker 1:** page, I use the, um, I don't know, change.
[00:00:57:200 - 00:00:59:500] **Speaker 1:** Settings notifications that comes through to your inbox.
[00:00:59:720 - 00:01:00:759] **Speaker 1:** If you've got that enabled.
[00:01:01:000 - 00:01:02:599] **Speaker 1:** You can disable that if you want, if you don't
[00:01:02:599 - 00:01:04:440] **Speaker 1:** want too much spam, but I just do that so
[00:01:04:440 - 00:01:06:239] **Speaker 1:** that you know if I've updated the scanned.
[00:01:07:019 - 00:01:09:949] **Speaker 1:** Um, or anything in the course material folder, for example,
[00:01:10:040 - 00:01:12:720] **Speaker 1:** the, the scanned, um, notes.
[00:01:13:949 - 00:01:13:959] **Speaker 1:** Alright.
[00:01:15:540 - 00:01:17:300] **Speaker 1:** Are there any questions before we dive in?
[00:01:17:339 - 00:01:19:160] **Speaker 1:** How was the test yesterday or last night?
[00:01:19:800 - 00:01:22:599] **Speaker 1:** It's a bit hectic, but yeah, some thumbs ups, that's
[00:01:22:599 - 00:01:22:980] **Speaker 1:** cool.
[00:01:23:849 - 00:01:25:599] **Speaker 1:** Yeah, oh, well, it's reassuring.
[00:01:25:639 - 00:01:27:120] **Speaker 1:** I know there was a bit of a, some hiccups
[00:01:27:120 - 00:01:30:550] **Speaker 1:** with some of the, the slow loading of the, um,
[00:01:30:559 - 00:01:32:599] **Speaker 1:** virtual machines, but yeah.
[00:01:33:260 - 00:01:33:779] **Speaker 1:** That's good.
[00:01:34:790 - 00:01:38:230] **Speaker 1:** Um, Right, so I looked at PDS.
[00:01:38:389 - 00:01:40:830] **Speaker 1:** We went through this on Monday.
[00:01:42:639 - 00:01:44:290] **Speaker 1:** And we went through those examples.
[00:01:45:059 - 00:01:46:750] **Speaker 1:** Uh, Laplace.
[00:01:48:650 - 00:01:49:500] **Speaker 1:** Blah blah blah.
[00:01:51:339 - 00:01:56:459] **Speaker 1:** And We found that we needed to use the Fourier
[00:01:56:459 - 00:01:58:419] **Speaker 1:** series to represent that last boundary condition that was just
[00:01:58:419 - 00:01:59:650] **Speaker 1:** equal to a constant value.
[00:01:59:860 - 00:02:03:099] **Speaker 1:** So you equal to 1 on that left-hand boundary, and
[00:02:03:099 - 00:02:05:510] **Speaker 1:** depending on how many Fourier series terms we use, uh,
[00:02:05:540 - 00:02:08:979] **Speaker 1:** dictated how accurately we resolved that boundary.
[00:02:09:339 - 00:02:11:940] **Speaker 1:** So here we use maybe 20, up to 20 terms,
[00:02:12:500 - 00:02:14:580] **Speaker 1:** uh, and if we used 100, it was resolving it
[00:02:14:580 - 00:02:15:919] **Speaker 1:** better, but it was still not perfect.
[00:02:16:300 - 00:02:18:479] **Speaker 1:** Um, it would only be perfect to the limit as
[00:02:18:479 - 00:02:19:800] **Speaker 1:** intends to infinity.
[00:02:20:320 - 00:02:22:300] **Speaker 1:** So that's infinite series for you.
[00:02:25:889 - 00:02:28:369] **Speaker 1:** For those of us who forget everything that we've learned
[00:02:28:369 - 00:02:30:970] **Speaker 1:** last year, we're gonna go through how we've done, how
[00:02:30:970 - 00:02:32:869] **Speaker 1:** we can calculate the Foyer sign series.
[00:02:33:210 - 00:02:34:570] **Speaker 1:** So just as a bit of a recap.
[00:02:36:990 - 00:02:38:770] **Speaker 1:** You might have done it in 1st or 2nd year
[00:02:38:830 - 00:02:40:889] **Speaker 1:** or high school, maybe for for your time.
[00:02:42:179 - 00:02:44:059] **Speaker 1:** Um, so if its.
[00:02:44:889 - 00:02:48:009] **Speaker 1:** Being some function, as long as it's going to be
[00:02:48:009 - 00:02:51:600] **Speaker 1:** odd, so in this case we've got um, Uh, an
[00:02:51:600 - 00:02:53:039] **Speaker 1:** odd function, it's.
[00:02:54:009 - 00:02:56:490] **Speaker 1:** Not just mirror image across the centre line.
[00:02:56:610 - 00:03:01:520] **Speaker 1:** It's also Flip Um, so we can make a note
[00:03:01:520 - 00:03:01:880] **Speaker 1:** of that.
[00:03:02:160 - 00:03:04:259] **Speaker 1:** So sign, series.
[00:03:05:639 - 00:03:08:600] **Speaker 1:** Uh, for odd functions.
[00:03:11:860 - 00:03:16:720] **Speaker 1:** Where We evaluate our function at the negative x position.
[00:03:16:960 - 00:03:20:320] **Speaker 1:** So if we go down minus L, it's not equal
[00:03:20:320 - 00:03:23:490] **Speaker 1:** to the function in the positive x equal L.
[00:03:23:880 - 00:03:24:679] **Speaker 1:** It's flipped.
[00:03:24:919 - 00:03:27:880] **Speaker 1:** So it's equal to minus FX.
[00:03:29:919 - 00:03:31:440] **Speaker 1:** So that's what we mean by odd, it's not well
[00:03:31:440 - 00:03:35:410] **Speaker 1:** it is slightly peculiar, but it's not, not super odd,
[00:03:35:830 - 00:03:37:130] **Speaker 1:** and cosine series.
[00:03:39:889 - 00:03:42:509] **Speaker 1:** We, we know that the cosine wave has the peak
[00:03:42:509 - 00:03:44:610] **Speaker 1:** at the the centre line and this is an even
[00:03:44:610 - 00:03:56:179] **Speaker 1:** function, a cosse for, Even Functions F minus X is
[00:03:56:179 - 00:03:58:240] **Speaker 1:** going to be mirror image on the other side, so
[00:03:58:240 - 00:03:59:410] **Speaker 1:** it's equal to F of X.
[00:04:02:429 - 00:04:04:830] **Speaker 1:** So the uh, the full 4-year series includes the sine
[00:04:04:830 - 00:04:07:550] **Speaker 1:** and cosine terms so that you can express all of
[00:04:07:550 - 00:04:08:220] **Speaker 1:** the functions.
[00:04:08:550 - 00:04:10:309] **Speaker 1:** We're just going to look at the sine series in
[00:04:10:309 - 00:04:13:130] **Speaker 1:** this class or in these next few weeks.
[00:04:13:669 - 00:04:18:618] **Speaker 1:** So for example, This Foyer sign series is the infinite
[00:04:18:618 - 00:04:21:539] **Speaker 1:** sum from 1 to infinity of some coefficients BN and
[00:04:21:539 - 00:04:24:898] **Speaker 1:** then you've got those sign terms in pi X over
[00:04:24:898 - 00:04:25:338] **Speaker 1:** L.
[00:04:27:420 - 00:04:32:380] **Speaker 1:** Um, where the coefficient B subscript N is given by
[00:04:32:380 - 00:04:32:980] **Speaker 1:** this expression.
[00:04:34:130 - 00:04:37:790] **Speaker 1:** So, That's just the 4-year sign series.
[00:04:38:250 - 00:04:39:809] **Speaker 1:** We're going to go through an example.
[00:04:41:579 - 00:04:44:459] **Speaker 1:** By evaluating the Fourier sign series for that constant value
[00:04:44:459 - 00:04:46:420] **Speaker 1:** one, which we just used in that last example for
[00:04:46:420 - 00:04:47:420] **Speaker 1:** the separation of variables.
[00:04:48:350 - 00:04:54:660] **Speaker 1:** So we have A length scale L equal to 1,
[00:04:55:000 - 00:04:56:440] **Speaker 1:** so the domain that we're looking at is from 0
[00:04:56:440 - 00:04:58:019] **Speaker 1:** to 1, so the length is 1.
[00:05:01:359 - 00:05:03:640] **Speaker 1:** So we're left with F of X.
[00:05:04:720 - 00:05:08:399] **Speaker 1:** Equal to our infinite sum, from one to infinity.
[00:05:09:700 - 00:05:11:420] **Speaker 1:** Be in sun.
[00:05:12:500 - 00:05:14:390] **Speaker 1:** Of N pi X.
[00:05:17:200 - 00:05:23:959] **Speaker 1:** With the N equal to Our, our coefficient definition at
[00:05:23:959 - 00:05:24:170] **Speaker 1:** the top.
[00:05:24:290 - 00:05:27:170] **Speaker 1:** So BN is 2 over L, so 2/1 is 2.
[00:05:29:410 - 00:05:32:170] **Speaker 1:** We're integrating from 0 up to that length, which is
[00:05:32:170 - 00:05:32:589] **Speaker 1:** 1.
[00:05:37:059 - 00:05:38:579] **Speaker 1:** Our function F of X.
[00:05:39:670 - 00:05:41:869] **Speaker 1:** We'll just keep it as FXX for now, but we
[00:05:41:869 - 00:05:43:290] **Speaker 1:** know that is equal to 1 as well.
[00:05:44:420 - 00:05:46:980] **Speaker 1:** And sign in by X.
[00:05:49:769 - 00:05:53:130] **Speaker 1:** I've run out of space, so I X D X.
[00:05:59:809 - 00:06:01:480] **Speaker 1:** If you haven't started writing that, you could write it
[00:06:01:480 - 00:06:03:510] **Speaker 1:** to the left, maybe a little bit further.
[00:06:07:720 - 00:06:09:809] **Speaker 1:** So we need to evaluate the expression B in.
[00:06:11:359 - 00:06:14:119] **Speaker 1:** So it's an integral across our domain from 0 to
[00:06:14:119 - 00:06:14:480] **Speaker 1:** 1.
[00:06:15:720 - 00:06:18:040] **Speaker 1:** F of X is equal to 1, because it's just
[00:06:18:040 - 00:06:18:880] **Speaker 1:** a constant value.
[00:06:19:600 - 00:06:21:619] **Speaker 1:** And we've got sin in pi x.
[00:06:40:640 - 00:06:43:399] **Speaker 1:** So I think that first day, well, it was Wednesday
[00:06:43:399 - 00:06:45:640] **Speaker 1:** actually, the 2nd lecture, I asked you if you know
[00:06:45:640 - 00:06:48:420] **Speaker 1:** how to differentiate sign, you know how to integrate sign.
[00:06:55:790 - 00:06:57:040] **Speaker 1:** So integrating sign.
[00:06:58:910 - 00:07:00:940] **Speaker 1:** If we differentiates sign, we go to cosine.
[00:07:01:980 - 00:07:05:380] **Speaker 1:** So if we integrate, it'll go to minus cosine.
[00:07:06:380 - 00:07:09:709] **Speaker 1:** It's got -2, and we have to differentiate respect to
[00:07:09:709 - 00:07:10:940] **Speaker 1:** what's inside the brackets.
[00:07:11:269 - 00:07:12:279] **Speaker 1:** So we've got N pi.
[00:07:19:130 - 00:07:22:540] **Speaker 1:** So cosine of N pi X.
[00:07:24:630 - 00:07:26:709] **Speaker 1:** And the limits of integration is from 0 to 1.
[00:07:38:630 - 00:07:41:850] **Speaker 1:** All right, so how can we evaluate this definite integral?
[00:07:43:480 - 00:07:44:640] **Speaker 1:** Cosine and pi x.
[00:07:44:959 - 00:07:47:000] **Speaker 1:** So the limits of integration is at x equal to
[00:07:47:000 - 00:07:48:480] **Speaker 1:** 1 and x equals 0.
[00:08:09:790 - 00:08:11:609] **Speaker 1:** So when X is equal to 1.
[00:08:15:040 - 00:08:18:779] **Speaker 1:** We've got cosine Of in high.
[00:08:20:000 - 00:08:21:940] **Speaker 1:** X equal to 1 and then the lower limit at
[00:08:21:940 - 00:08:25:600] **Speaker 1:** X equal to 0, we've got cosine of 0.
[00:08:35:169 - 00:08:35:929] **Speaker 1:** Can you see that all right?
[00:08:35:969 - 00:08:39:049] **Speaker 1:** I tried to improve the lighting, but if I put
[00:08:39:049 - 00:08:41:690] **Speaker 1:** the front lights down, then it gets really dark, so.
[00:08:42:689 - 00:08:43:429] **Speaker 1:** What do you prefer?
[00:08:44:960 - 00:08:48:640] **Speaker 1:** This, oh, OK, OK, alright, it's like a movie, yeah.
[00:08:49:719 - 00:08:50:320] **Speaker 1:** Um.
[00:08:52:340 - 00:08:55:349] **Speaker 1:** Alright, so at the moment in those.
[00:08:56:849 - 00:08:59:909] **Speaker 1:** Infinite, uh, terms, so one through to infinity.
[00:09:04:010 - 00:09:05:929] **Speaker 1:** So what, what do we do here?
[00:09:07:530 - 00:09:10:789] **Speaker 1:** Expression changes depending on what value in holds.
[00:09:11:250 - 00:09:13:690] **Speaker 1:** So if we had N equal to 1, we'd have
[00:09:13:690 - 00:09:16:770] **Speaker 1:** cosine pi minus cos zero.
[00:09:17:530 - 00:09:20:000] **Speaker 1:** If we had N equals 2, we'd have cosine 2
[00:09:20:000 - 00:09:21:890] **Speaker 1:** pi minus cosine 0.
[00:09:23:320 - 00:09:25:429] **Speaker 1:** So cosine 0 is equal to 1.
[00:09:27:530 - 00:09:32:409] **Speaker 1:** And cospi is equal to -1.
[00:09:35:710 - 00:09:38:070] **Speaker 1:** So we're gonna have -1 -1, so we're gonna have
[00:09:38:070 - 00:09:38:729] **Speaker 1:** -2.
[00:09:41:369 - 00:09:43:859] **Speaker 1:** Multiplied by -2 is 4.
[00:09:44:130 - 00:09:49:500] **Speaker 1:** So we've got 4 over n pi if N is
[00:09:49:500 - 00:09:50:169] **Speaker 1:** odd.
[00:09:54:250 - 00:09:55:049] **Speaker 1:** So we can just check that.
[00:09:55:119 - 00:09:58:450] **Speaker 1:** So if we've got N equals 33 pi, um, that's
[00:09:58:450 - 00:10:00:280] **Speaker 1:** done a whole oscillation and an extra half.
[00:10:01:090 - 00:10:04:010] **Speaker 1:** So it's gonna be -1 again, -1 minus 1 is
[00:10:04:010 - 00:10:06:650] **Speaker 1:** -2, multiplied by -2 is 4.
[00:10:07:830 - 00:10:10:150] **Speaker 1:** So in even cases, so when N is equal to
[00:10:10:150 - 00:10:12:400] **Speaker 1:** 2468.
[00:10:13:099 - 00:10:17:859] **Speaker 1:** Uh Cosine is going to be equal to one.
[00:10:18:859 - 00:10:21:739] **Speaker 1:** So cosine of 2 pi is equal to 11 minus
[00:10:21:739 - 00:10:23:919] **Speaker 1:** 1 is 0, so they're going to cancel.
[00:10:24:799 - 00:10:28:940] **Speaker 1:** So it's gonna be 0 if N is Even.
[00:10:29:840 - 00:10:32:390] **Speaker 1:** So that's how we've got that uh conditional.
[00:10:33:250 - 00:10:35:770] **Speaker 1:** Expression, depending on if the end is odd or even.
[00:10:44:359 - 00:10:47:039] **Speaker 1:** So finally, F of X, we plug it back into
[00:10:47:039 - 00:10:49:479] **Speaker 1:** our expression at the top.
[00:10:49:799 - 00:10:51:000] **Speaker 1:** We've got this infinite sum.
[00:10:53:250 - 00:10:57:380] **Speaker 1:** We've just said that the even numbers or even in
[00:10:57:380 - 00:10:59:409] **Speaker 1:** values are equal to zero.
[00:10:59:770 - 00:11:02:890] **Speaker 1:** So we're only going to sum over the odd 135
[00:11:02:890 - 00:11:03:489] **Speaker 1:** onwards.
[00:11:05:940 - 00:11:09:669] **Speaker 1:** And we've got BN equal to 4 over n pi.
[00:11:11:280 - 00:11:12:960] **Speaker 1:** Multiplied by sign.
[00:11:14:010 - 00:11:15:179] **Speaker 1:** Of Epi X.
[00:11:50:400 - 00:11:52:969] **Speaker 1:** And there's a demonstration that I'm just loading.
[00:12:18:289 - 00:12:19:890] **Speaker 1:** I think this is quite similar to the last code,
[00:12:19:969 - 00:12:22:849] **Speaker 1:** so I won't go into too much detail, uh, we've
[00:12:22:849 - 00:12:27:489] **Speaker 1:** got the number of points where we're, Number of points
[00:12:27:489 - 00:12:30:320] **Speaker 1:** through the 4-year series is calculated and a maximum number
[00:12:30:320 - 00:12:31:929] **Speaker 1:** of terms that we're evaluating.
[00:12:33:020 - 00:12:34:219] **Speaker 1:** And the location.
[00:12:34:299 - 00:12:36:880] **Speaker 1:** So that's using that lin space and then preparing the
[00:12:37:539 - 00:12:40:780] **Speaker 1:** displacement field you with the zeros operator and numpi.
[00:12:41:460 - 00:12:42:940] **Speaker 1:** So if we solve this.
[00:12:51:309 - 00:12:54:619] **Speaker 1:** It was up to 20 terms, so that's what we
[00:12:54:619 - 00:12:55:530] **Speaker 1:** did in the last example.
[00:12:55:780 - 00:12:57:700] **Speaker 1:** So you can see that's not really capturing that, that
[00:12:57:700 - 00:13:00:440] **Speaker 1:** constant value that we expect, uh, very well.
[00:13:01:609 - 00:13:03:659] **Speaker 1:** But if we ramp up the number of FOIA terms,
[00:13:05:780 - 00:13:07:080] **Speaker 1:** It'll take longer to solve.
[00:13:11:190 - 00:13:14:150] **Speaker 1:** Well not too long, um, and you can see it.
[00:13:15:099 - 00:13:18:809] **Speaker 1:** It's slowly ah converging to that constant value of one,
[00:13:19:030 - 00:13:21:109] **Speaker 1:** but there's some weird behaviour on the sides.
[00:13:22:309 - 00:13:25:030] **Speaker 1:** So, yeah, a bit of a quirk maybe with these
[00:13:25:030 - 00:13:25:630] **Speaker 1:** 4 series.
[00:13:30:049 - 00:13:32:809] **Speaker 1:** Alright, any questions on the suppression of variables or using
[00:13:32:809 - 00:13:34:830] **Speaker 1:** those Fourier series to to solve?
[00:13:35:890 - 00:13:40:130] **Speaker 1:** Those that pass equation using separation of variables.
[00:13:43:390 - 00:13:50:229] **Speaker 1:** Right So we've got some questions that you can work
[00:13:50:229 - 00:13:50:710] **Speaker 1:** through.
[00:13:52:390 - 00:13:54:190] **Speaker 1:** And the exercises.
[00:13:55:169 - 00:13:58:090] **Speaker 1:** I won't spoil the the solutions, I'll let you work
[00:13:58:090 - 00:13:58:510] **Speaker 1:** through them.
[00:13:59:479 - 00:14:02:760] **Speaker 1:** Um, We've given reasonable.
[00:14:03:469 - 00:14:08:070] **Speaker 1:** Detailed instructions, so follow, follow what we've asked.
[00:14:08:789 - 00:14:13:510] **Speaker 1:** Um, Yeah, I don't think you'll get lost.
[00:14:14:169 - 00:14:15:570] **Speaker 1:** So question 4.
[00:14:16:489 - 00:14:17:640] **Speaker 1:** Central flow.
[00:14:19:340 - 00:14:21:280] **Speaker 1:** That's just a little bit of fluids question for you.
[00:14:22:030 - 00:14:25:210] **Speaker 1:** And question 5 is looking at the membrane.
[00:14:25:479 - 00:14:27:419] **Speaker 1:** So that's quite similar to what we've been looking at
[00:14:27:419 - 00:14:28:539] **Speaker 1:** in those examples.
[00:14:29:039 - 00:14:31:270] **Speaker 1:** We've got this sort of membrane that has a displacement
[00:14:31:270 - 00:14:33:659] **Speaker 1:** field and we've applied a sine wave on the top.
[00:14:36:840 - 00:14:57:570] **Speaker 1:** All right Uh All right, so I just want to
[00:14:57:570 - 00:15:00:950] **Speaker 1:** talk through the quiz for this week.
[00:15:03:229 - 00:15:15:609] **Speaker 1:** This one So some of you have started, um, there's
[00:15:15:609 - 00:15:18:159] **Speaker 1:** no time limit per se, so you can start it
[00:15:18:159 - 00:15:22:169] **Speaker 1:** when you want, and it will submit automatically at closure,
[00:15:22:450 - 00:15:23:890] **Speaker 1:** so, um, end of Friday.
[00:15:24:580 - 00:15:26:179] **Speaker 1:** Or you can submit it earlier if you want.
[00:15:26:260 - 00:15:28:419] **Speaker 1:** I don't think I can, well, I can't figure out
[00:15:28:419 - 00:15:29:700] **Speaker 1:** how to unsubmit something.
[00:15:29:780 - 00:15:32:280] **Speaker 1:** I can only delete attempts, so you can start again.
[00:15:33:150 - 00:15:35:520] **Speaker 1:** Um, so there's no real reason to submit it earlier,
[00:15:35:630 - 00:15:37:809] **Speaker 1:** but As you wish.
[00:15:38:369 - 00:15:41:409] **Speaker 1:** So the first questions are just a couple of multi-choice.
[00:15:41:890 - 00:15:43:289] **Speaker 1:** So I have set out the multi-choice that you have
[00:15:43:289 - 00:15:44:950] **Speaker 1:** to get them all right to get the mark.
[00:15:45:210 - 00:15:50:460] **Speaker 1:** So Yeah, there's only one mark out of 1%, so
[00:15:50:460 - 00:15:52:679] **Speaker 1:** what's that 0.1% of the course grade.
[00:15:53:179 - 00:15:57:409] **Speaker 1:** Um, Yeah, I guess in previous years, some people have
[00:15:57:409 - 00:16:00:450] **Speaker 1:** suggested having partial credit for these, but I feel.
[00:16:01:780 - 00:16:04:340] **Speaker 1:** I feel like you should, should get the whole, whole
[00:16:04:340 - 00:16:04:809] **Speaker 1:** question right.
[00:16:06:229 - 00:16:06:979] **Speaker 1:** Um.
[00:16:08:580 - 00:16:09:159] **Speaker 1:** statements.
[00:16:09:479 - 00:16:11:559] **Speaker 1:** So these are sort of based on the overview slides
[00:16:11:559 - 00:16:14:719] **Speaker 1:** that I had in that first lecture, if you're stuck.
[00:16:15:599 - 00:16:18:559] **Speaker 1:** Uh, figuring out whether or not the PDs are linear.
[00:16:18:719 - 00:16:19:880] **Speaker 1:** So that's based on chapter one.
[00:16:20:039 - 00:16:22:380] **Speaker 1:** We talked through that and we did some examples.
[00:16:23:710 - 00:16:26:630] **Speaker 1:** And defining them as the parabolic or hyperbolic.
[00:16:26:780 - 00:16:29:429] **Speaker 1:** Again, we did this in chapter one, separation of variables.
[00:16:29:469 - 00:16:30:070] **Speaker 1:** So there you go.
[00:16:30:190 - 00:16:31:609] **Speaker 1:** You get to practise that.
[00:16:32:109 - 00:16:36:969] **Speaker 1:** Um, and We talked a little bit about choosing which
[00:16:36:969 - 00:16:38:840] **Speaker 1:** order of boundary conditions to apply.
[00:16:39:289 - 00:16:41:169] **Speaker 1:** So it might be easier to start with ones that
[00:16:41:169 - 00:16:45:710] **Speaker 1:** are zero, either the coordinate white equals 0 maybe, um,
[00:16:46:090 - 00:16:48:229] **Speaker 1:** or that right-hand side so the actual value being 0.
[00:16:49:250 - 00:16:50:690] **Speaker 1:** So if you do it in a different order, you
[00:16:50:690 - 00:16:53:090] **Speaker 1:** might find that it's not possible to do.
[00:16:53:359 - 00:16:55:760] **Speaker 1:** So yeah, if you're really stuck, just try out a
[00:16:55:760 - 00:16:57:390] **Speaker 1:** different order of boundary conditions.
[00:16:57:650 - 00:16:59:619] **Speaker 1:** I think I might have listed these in one, in
[00:16:59:619 - 00:17:02:210] **Speaker 1:** the order that makes the most sense, but not guaranteed.
[00:17:04:569 - 00:17:06:810] **Speaker 1:** Uh, talking about structured versus unstructured grids.
[00:17:07:938 - 00:17:10:780] **Speaker 1:** That's what we covered in that 1st, 1st few lectures
[00:17:10:780 - 00:17:11:359] **Speaker 1:** as well.
[00:17:13:129 - 00:17:17:060] **Speaker 1:** And some Uh, numerical method.
[00:17:18:938 - 00:17:20:260] **Speaker 1:** Medication techniques.
[00:17:21:270 - 00:17:23:729] **Speaker 1:** The, oh, so there's no coding question this week.
[00:17:23:938 - 00:17:26:310] **Speaker 1:** I thought, OK, well, you're lucky, um.
[00:17:27:578 - 00:17:28:188] **Speaker 1:** Or not.
[00:17:28:698 - 00:17:31:078] **Speaker 1:** So question 8 is on console.
[00:17:31:578 - 00:17:34:930] **Speaker 1:** So I'll go through that shortly.
[00:17:35:099 - 00:17:37:250] **Speaker 1:** Essentially you're just extending what you've already done during the
[00:17:37:250 - 00:17:41:410] **Speaker 1:** lab and adjusting it based on what I've asked you
[00:17:41:410 - 00:17:41:750] **Speaker 1:** here.
[00:17:44:170 - 00:17:48:229] **Speaker 1:** So these questions are stack, I think they're called stack
[00:17:48:229 - 00:17:52:130] **Speaker 1:** questions, so they are provided examples of what syntax to
[00:17:52:130 - 00:17:52:310] **Speaker 1:** include.
[00:17:53:319 - 00:17:56:160] **Speaker 1:** So you could use the hyperbolic sine functions or the
[00:17:56:160 - 00:17:58:140] **Speaker 1:** exponential terms, etc.
[00:17:59:449 - 00:18:03:579] **Speaker 1:** Uh, don't include the actual function T, just include the
[00:18:03:579 - 00:18:04:020] **Speaker 1:** solution.
[00:18:05:969 - 00:18:12:060] **Speaker 1:** And This last question requires units, so obviously we need
[00:18:12:060 - 00:18:14:119] **Speaker 1:** units for all of our values.
[00:18:14:420 - 00:18:16:339] **Speaker 1:** Uh, you can insert the units.
[00:18:17:910 - 00:18:21:910] **Speaker 1:** For example, with Newtons or milli-Newtons or in the base
[00:18:21:910 - 00:18:23:109] **Speaker 1:** SI units as well.
[00:18:23:469 - 00:18:25:790] **Speaker 1:** So up to you how you insert it, uh, just
[00:18:25:790 - 00:18:28:069] **Speaker 1:** be careful when you're converting from milli to killer Newtons,
[00:18:28:109 - 00:18:28:589] **Speaker 1:** etc.
[00:18:31:619 - 00:18:32:900] **Speaker 1:** And incomo.
[00:18:34:510 - 00:18:37:359] **Speaker 1:** Uh, if you had like 3 metres, you would type
[00:18:37:359 - 00:18:40:849] **Speaker 1:** it with square brackets to represent the, the unit, but
[00:18:40:849 - 00:18:43:060] **Speaker 1:** well, we're getting told that it's wrong, so that's good.
[00:18:43:319 - 00:18:47:199] **Speaker 1:** But in this quiz, uh, it's multiplied by the, the
[00:18:47:199 - 00:18:47:520] **Speaker 1:** unit.
[00:18:48:900 - 00:18:50:780] **Speaker 1:** So, sometimes that trips people up.
[00:18:51:930 - 00:18:54:290] **Speaker 1:** And I'll force you to do 3 significant figures, so.
[00:18:55:099 - 00:18:56:719] **Speaker 1:** That was a question in the farm too, so that's
[00:18:56:719 - 00:18:56:900] **Speaker 1:** good.
[00:18:57:800 - 00:19:09:420] **Speaker 1:** Um, Right.
[00:19:09:489 - 00:19:11:810] **Speaker 1:** Any question on the quiz layout or how it's structured?
[00:19:11:880 - 00:19:15:290] **Speaker 1:** So they're due each Friday, week 6 to 10, and
[00:19:15:290 - 00:19:18:270] **Speaker 1:** then I'll go through the solutions following lecture on Monday.
[00:19:19:199 - 00:19:22:920] **Speaker 1:** Um, you don't get your mark or result until after
[00:19:22:920 - 00:19:26:439] **Speaker 1:** it's closed, um, and you get one attempt, so.
[00:19:27:189 - 00:19:30:369] **Speaker 1:** Yeah Cool.
[00:19:33:369 - 00:19:33:849] **Speaker 1:** All right.
[00:19:35:380 - 00:19:39:839] **Speaker 1:** So I'll talk through console, but just because I've already
[00:19:39:839 - 00:19:41:819] **Speaker 1:** got this up, maybe I can.
[00:19:43:609 - 00:19:47:030] **Speaker 1:** Point to this access to console part of the course
[00:19:47:030 - 00:19:47:430] **Speaker 1:** page.
[00:19:49:250 - 00:19:53:890] **Speaker 1:** So console is installed on the MacSuite computers locally.
[00:19:55:359 - 00:19:58:640] **Speaker 1:** Uh, which is what I suggest you, you're using or
[00:19:58:640 - 00:19:59:430] **Speaker 1:** accessing it via.
[00:20:00:079 - 00:20:03:920] **Speaker 1:** So see apps menu, uh, or directly under see apps
[00:20:03:920 - 00:20:04:479] **Speaker 1:** console.
[00:20:04:920 - 00:20:06:760] **Speaker 1:** So it should be on the start menu, but if
[00:20:06:760 - 00:20:09:270] **Speaker 1:** it's not, then these are the file locations.
[00:20:10:859 - 00:20:12:780] **Speaker 1:** You can run it off the network drive, so the
[00:20:12:780 - 00:20:14:959] **Speaker 1:** M drive is a shared network that you have access
[00:20:14:959 - 00:20:15:400] **Speaker 1:** to.
[00:20:16:300 - 00:20:17:000] **Speaker 1:** On campus.
[00:20:17:500 - 00:20:19:780] **Speaker 1:** So if you're in the in another lab, the Tron
[00:20:19:780 - 00:20:22:260] **Speaker 1:** lab or the upper lower CD suites, you should be
[00:20:22:260 - 00:20:23:400] **Speaker 1:** able to access it through here.
[00:20:24:130 - 00:20:28:310] **Speaker 1:** It has to load console over the network, uh, which
[00:20:28:729 - 00:20:32:569] **Speaker 1:** we've had issues with network errors at random times, especially
[00:20:32:569 - 00:20:34:130] **Speaker 1:** if everyone's accessing it at once.
[00:20:34:369 - 00:20:36:119] **Speaker 1:** So the last couple of years we've managed to install
[00:20:36:119 - 00:20:38:609] **Speaker 1:** it locally in the next week, and the test last
[00:20:38:609 - 00:20:42:390] **Speaker 1:** night is maybe an example of challenges when you're using.
[00:20:43:680 - 00:20:47:599] **Speaker 1:** Network um connections that could be overloaded.
[00:20:50:489 - 00:20:53:550] **Speaker 1:** So, also, you can install it on your personal computer.
[00:20:54:540 - 00:20:58:400] **Speaker 1:** So they've kindly given us some like a homework passcode.
[00:20:58:819 - 00:21:01:810] **Speaker 1:** So it's only valid until the end of the year,
[00:21:01:939 - 00:21:04:449] **Speaker 1:** 21st of December, and then it will stop working afterwards.
[00:21:04:979 - 00:21:07:040] **Speaker 1:** So it's really only just for this, this class.
[00:21:09:150 - 00:21:11:689] **Speaker 1:** They've provided detailed instructions here.
[00:21:14:369 - 00:21:18:109] **Speaker 1:** If you're stuck, essentially you create an account on console.com.
[00:21:18:939 - 00:21:23:459] **Speaker 1:** Add in this passcode to validate your account so you
[00:21:23:459 - 00:21:26:719] **Speaker 1:** can download console and then just follow the instructions to
[00:21:26:900 - 00:21:27:339] **Speaker 1:** install.
[00:21:32:489 - 00:21:34:089] **Speaker 1:** So take care of which version.
[00:21:34:130 - 00:21:35:670] **Speaker 1:** There's a few versions that we've got installed.
[00:21:36:890 - 00:21:39:089] **Speaker 1:** We've got 6.4 now installed in the next week, which
[00:21:39:089 - 00:21:41:880] **Speaker 1:** is good, uh, which is the latest version and the
[00:21:41:880 - 00:21:44:630] **Speaker 1:** only version that you can install with the homework passcode.
[00:21:44:969 - 00:21:48:810] **Speaker 1:** Um, if you try to open older console models, it
[00:21:48:810 - 00:21:51:729] **Speaker 1:** opens, but you can't open newer console models.
[00:21:52:569 - 00:21:54:810] **Speaker 1:** So if you've got 6.3, it won't open 6.4.
[00:21:56:900 - 00:21:59:239] **Speaker 1:** You might find it helpful to save the model files
[00:21:59:479 - 00:22:01:459] **Speaker 1:** to the local drive when you're running simulations, especially if
[00:22:01:459 - 00:22:04:699] **Speaker 1:** it's a larger, uh, model, and then save to your
[00:22:04:699 - 00:22:06:439] **Speaker 1:** P drive or OneDrive afterwards.
[00:22:23:099 - 00:22:23:310] **Speaker 1:** Cool.
[00:22:23:540 - 00:22:24:699] **Speaker 1:** Any questions on that?
[00:22:24:780 - 00:22:26:859] **Speaker 1:** I don't know if anyone's actually tried that yet.
[00:22:27:060 - 00:22:29:260] **Speaker 1:** I wanted to wait until today to talk about the
[00:22:29:260 - 00:22:32:140] **Speaker 1:** quiz and console because I knew everyone would be busy
[00:22:32:140 - 00:22:35:209] **Speaker 1:** with the test, right, um.
[00:22:36:050 - 00:22:37:650] **Speaker 1:** So the rest of the lecture, I want to sort
[00:22:37:650 - 00:22:38:609] **Speaker 1:** of introduce the console.
[00:22:38:689 - 00:22:40:709] **Speaker 1:** What is the software, what can we use it for?
[00:22:41:250 - 00:22:42:969] **Speaker 1:** And then give a brief demonstration.
[00:22:44:260 - 00:22:47:099] **Speaker 1:** So this is Appendix A, page 109 in your course
[00:22:47:099 - 00:22:47:560] **Speaker 1:** reader.
[00:22:56:040 - 00:22:56:989] **Speaker 1:** And there's not much riding.
[00:22:57:020 - 00:22:59:119] **Speaker 1:** It's a little bit dry, so I'll try and speed
[00:22:59:119 - 00:22:59:420] **Speaker 1:** through it.
[00:23:00:209 - 00:23:07:209] **Speaker 1:** OK, so Essentially Console Multiphysics is its full name and
[00:23:07:209 - 00:23:10:329] **Speaker 1:** the multi-physics hints that it can handle multiple physics.
[00:23:11:140 - 00:23:15:260] **Speaker 1:** So the example given here is a micro electromechanical system,
[00:23:15:339 - 00:23:16:479] **Speaker 1:** a MEMS actuator.
[00:23:17:449 - 00:23:23:920] **Speaker 1:** So it deflects or displaces subject to some temperature or
[00:23:24:130 - 00:23:24:859] **Speaker 1:** variation.
[00:23:25:579 - 00:23:28:479] **Speaker 1:** Um, so there's coupling between the temperature, electric potential, and
[00:23:28:479 - 00:23:29:140] **Speaker 1:** displacement.
[00:23:29:439 - 00:23:32:359] **Speaker 1:** So there's 3 sets of dependent variables.
[00:23:33:270 - 00:23:37:180] **Speaker 1:** And the temperature and electric potential are scalars, and that
[00:23:37:180 - 00:23:38:569] **Speaker 1:** displacement is a vector field.
[00:23:38:709 - 00:23:40:589] **Speaker 1:** So it's got X, Y, and Z components.
[00:23:42:530 - 00:23:45:109] **Speaker 1:** We've got coupling between the three physics.
[00:23:45:369 - 00:23:46:979] **Speaker 1:** So thermal expansion.
[00:23:47:410 - 00:23:51:489] **Speaker 1:** So depending on the temperature of the material, it will
[00:23:51:489 - 00:23:52:849] **Speaker 1:** adjust the density.
[00:23:53:250 - 00:23:58:430] **Speaker 1:** So if you um Change the density that will displace
[00:23:59:040 - 00:23:59:739] **Speaker 1:** the material.
[00:24:00:000 - 00:24:03:699] **Speaker 1:** So that's the thermal expansion conductivity depends on temperature as
[00:24:03:699 - 00:24:04:010] **Speaker 1:** well.
[00:24:04:329 - 00:24:07:689] **Speaker 1:** So the electric potential depends on the temperature distribution and
[00:24:07:689 - 00:24:09:770] **Speaker 1:** then you've got this electric heating or dual heating as
[00:24:09:770 - 00:24:10:150] **Speaker 1:** well.
[00:24:11:319 - 00:24:12:089] **Speaker 1:** Feeding back.
[00:24:12:489 - 00:24:15:810] **Speaker 1:** So you've got these interactions between each physics, uh, so
[00:24:15:810 - 00:24:18:050] **Speaker 1:** you can do quite complicated problems, which is neat.
[00:24:18:939 - 00:24:21:859] **Speaker 1:** Um, don't have to worry too much about it in
[00:24:21:859 - 00:24:22:939] **Speaker 1:** this, in this course.
[00:24:22:979 - 00:24:24:500] **Speaker 1:** We're just going to introduce you to some of the
[00:24:24:500 - 00:24:25:359] **Speaker 1:** basic concepts.
[00:24:26:530 - 00:24:27:989] **Speaker 1:** So a little bit about console.
[00:24:28:339 - 00:24:29:410] **Speaker 1:** So it's finite element.
[00:24:29:689 - 00:24:31:949] **Speaker 1:** We talked about finite element difference in volume.
[00:24:32:329 - 00:24:34:250] **Speaker 1:** Console is a finite element in particular.
[00:24:35:510 - 00:24:38:989] **Speaker 1:** You can read this link if you want to, to
[00:24:38:989 - 00:24:41:790] **Speaker 1:** see how they've set up the final element method in
[00:24:41:790 - 00:24:42:449] **Speaker 1:** console.
[00:24:45:010 - 00:24:48:239] **Speaker 1:** They've got several modules, so they haven't gone to the
[00:24:48:239 - 00:24:49:270] **Speaker 1:** subscription plan yet.
[00:24:49:489 - 00:24:51:449] **Speaker 1:** I don't know if they will, but all the software
[00:24:51:449 - 00:24:53:930] **Speaker 1:** companies want to make money, uh, so they provide you
[00:24:53:930 - 00:24:57:170] **Speaker 1:** sort of with a baseline, uh, code, and then they
[00:24:57:170 - 00:24:59:569] **Speaker 1:** provide modules that apply to specific industries.
[00:25:00:339 - 00:25:05:380] **Speaker 1:** So they've got many modules or packages that tailor for
[00:25:05:380 - 00:25:06:199] **Speaker 1:** particular industries.
[00:25:07:400 - 00:25:10:000] **Speaker 1:** Uh, including optimisation, etc.
[00:25:13:699 - 00:25:16:040] **Speaker 1:** So it's also got a comprehensive material library.
[00:25:16:949 - 00:25:20:709] **Speaker 1:** So if we've got water, varies with temperature, uh, all
[00:25:20:709 - 00:25:24:510] **Speaker 1:** the different physical materials, concrete, aluminium, etc.
[00:25:26:400 - 00:25:29:569] **Speaker 1:** And we can also interface console with uh external software.
[00:25:29:880 - 00:25:33:319] **Speaker 1:** For example, CAD, you might do your geometry building and
[00:25:33:319 - 00:25:35:579] **Speaker 1:** solid works and then import that into console for the
[00:25:35:579 - 00:25:36:099] **Speaker 1:** analysis.
[00:25:38:650 - 00:25:40:729] **Speaker 1:** And you can also couple it with with MATLAB, but
[00:25:40:729 - 00:25:43:430] **Speaker 1:** we're not using MATLAB anymore in this course.
[00:25:46:420 - 00:25:48:180] **Speaker 1:** It's just a bit of an overview of the product
[00:25:48:180 - 00:25:48:520] **Speaker 1:** suite.
[00:25:52:400 - 00:25:56:640] **Speaker 1:** So we, the base one is required, and we've also
[00:25:56:640 - 00:25:58:260] **Speaker 1:** got the optimisation module.
[00:25:59:270 - 00:26:00:770] **Speaker 1:** And the CFD module.
[00:26:03:719 - 00:26:06:479] **Speaker 1:** In, in what you have access to in the next
[00:26:06:479 - 00:26:06:780] **Speaker 1:** week.
[00:26:11:199 - 00:26:12:599] **Speaker 1:** But there's a whole host of other ones.
[00:26:13:000 - 00:26:14:859] **Speaker 1:** You can check out their website or talk to the
[00:26:14:900 - 00:26:16:979] **Speaker 1:** the sales rep probably if you if you're really keen,
[00:26:17:479 - 00:26:17:920] **Speaker 1:** um.
[00:26:19:099 - 00:26:21:719] **Speaker 1:** Just a brief overview of the modelling workflow.
[00:26:22:099 - 00:26:24:780] **Speaker 1:** So from start to finish, where do you start?
[00:26:24:859 - 00:26:29:579] **Speaker 1:** So pre-processing is the early stages as we define the
[00:26:29:579 - 00:26:32:239] **Speaker 1:** parameters, maybe some user-defined functions.
[00:26:33:229 - 00:26:36:430] **Speaker 1:** Your geometry, so what size is your computational domain going
[00:26:36:430 - 00:26:36:829] **Speaker 1:** to be?
[00:26:37:189 - 00:26:38:849] **Speaker 1:** Are you going to simplify the domain?
[00:26:39:660 - 00:26:42:239] **Speaker 1:** You've got materials, physics, and the mesh.
[00:26:42:890 - 00:26:44:719] **Speaker 1:** So that discretized grid.
[00:26:46:890 - 00:26:48:209] **Speaker 1:** The next step is to solve.
[00:26:48:489 - 00:26:50:130] **Speaker 1:** So once you've got the mesh and you've got the
[00:26:50:130 - 00:26:52:969] **Speaker 1:** physics, you create a big system of equations.
[00:26:53:209 - 00:26:55:550] **Speaker 1:** So usually linear equations and then solve.
[00:26:56:310 - 00:26:58:699] **Speaker 1:** Ah, what you've done in the test last night and
[00:26:58:699 - 00:27:01:229] **Speaker 1:** elsewhere, you've probably had 12 or so equations that you're
[00:27:01:229 - 00:27:04:630] **Speaker 1:** solving, but console will be solving tens or hundreds or
[00:27:04:630 - 00:27:08:650] **Speaker 1:** millions of equations, so there's different algorithms to use for
[00:27:08:660 - 00:27:09:589] **Speaker 1:** for those cases.
[00:27:11:099 - 00:27:13:920] **Speaker 1:** Um, so it can take A few seconds or a
[00:27:13:920 - 00:27:15:920] **Speaker 1:** few minutes and we try to make all the assignments
[00:27:15:920 - 00:27:19:150] **Speaker 1:** and labs in this course just that sort of time
[00:27:19:150 - 00:27:21:000] **Speaker 1:** frame just so you're not waiting around, but it can
[00:27:21:000 - 00:27:22:920] **Speaker 1:** take days or weeks or months if you have really
[00:27:22:920 - 00:27:23:599] **Speaker 1:** large problems.
[00:27:26:280 - 00:27:30:569] **Speaker 1:** The model wizard er helps you set up your model.
[00:27:32:349 - 00:27:33:270] **Speaker 1:** In console.
[00:27:33:709 - 00:27:36:810] **Speaker 1:** So you want to select if it's 3D, 2D, uh,
[00:27:36:819 - 00:27:38:170] **Speaker 1:** or maybe axis symmetric.
[00:27:38:750 - 00:27:40:310] **Speaker 1:** You can also have a 0D if it was just
[00:27:40:310 - 00:27:40:969] **Speaker 1:** a point.
[00:27:44:390 - 00:27:47:530] **Speaker 1:** Console and the physics-based add-on modules.
[00:27:48:880 - 00:27:50:060] **Speaker 1:** have different physics.
[00:27:50:599 - 00:27:55:280] **Speaker 1:** So we talked a little about um temperature, electric, and
[00:27:55:280 - 00:27:59:000] **Speaker 1:** solid mechanics, uh, but it also has fluid mechanics as
[00:27:59:000 - 00:27:59:339] **Speaker 1:** well.
[00:28:01:359 - 00:28:05:359] **Speaker 1:** So solid mechanics, laminar flow, heat transfer, solids, electrostatics.
[00:28:08:030 - 00:28:12:949] **Speaker 1:** Each of these different fields or subdomains have maybe different
[00:28:12:949 - 00:28:14:829] **Speaker 1:** approaches to solve those equations.
[00:28:15:189 - 00:28:18:859] **Speaker 1:** We talked about the elliptic, parabolic, and hyperbolic, uh, being
[00:28:18:859 - 00:28:20:170] **Speaker 1:** sort of three different categories.
[00:28:20:589 - 00:28:23:949] **Speaker 1:** Uh, but also within these disciplines you might have different
[00:28:23:949 - 00:28:27:989] **Speaker 1:** length scales and different behaviour that sort of lends itself
[00:28:27:989 - 00:28:30:270] **Speaker 1:** to different solution techniques.
[00:28:30:589 - 00:28:33:270] **Speaker 1:** So there will be default studies or solver types for
[00:28:33:270 - 00:28:34:410] **Speaker 1:** each of these cases.
[00:28:34:920 - 00:28:38:560] **Speaker 1:** And starting with the defaults make, makes sense, um.
[00:28:39:619 - 00:28:40:719] **Speaker 1:** And then building from there.
[00:28:46:300 - 00:28:48:280] **Speaker 1:** So the next step is the study step.
[00:28:48:660 - 00:28:50:579] **Speaker 1:** So you define whether it's transient.
[00:28:52:119 - 00:28:53:339] **Speaker 1:** Or if it's stationary.
[00:28:56:239 - 00:29:00:959] **Speaker 1:** The model tree is on the left-hand side, we'll go
[00:29:00:959 - 00:29:01:939] **Speaker 1:** through that shortly.
[00:29:02:530 - 00:29:04:760] **Speaker 1:** But essentially you start from top to bottom.
[00:29:05:280 - 00:29:05:900] **Speaker 1:** So.
[00:29:06:550 - 00:29:12:790] **Speaker 1:** MPH is the file extension, so that's the, Um The
[00:29:13:089 - 00:29:16:650] **Speaker 1:** parent, and then all of the child nodes are those
[00:29:16:650 - 00:29:17:060] **Speaker 1:** steps.
[00:29:17:329 - 00:29:19:880] **Speaker 1:** So you've got the pre-processing where you've got, I don't
[00:29:19:880 - 00:29:20:810] **Speaker 1:** know if you can read that.
[00:29:24:400 - 00:29:26:040] **Speaker 1:** You can't read it now either, so.
[00:29:27:900 - 00:29:30:619] **Speaker 1:** Well, generally, you've got preprocessing at the top.
[00:29:32:109 - 00:29:35:800] **Speaker 1:** Um, and then you've got solving, and then results, and
[00:29:35:800 - 00:29:38:359] **Speaker 1:** we'll go through a demonstration because that's much easier to
[00:29:38:359 - 00:29:38:800] **Speaker 1:** work through.
[00:29:40:170 - 00:29:41:410] **Speaker 1:** Uh, geometry modelling.
[00:29:41:729 - 00:29:44:130] **Speaker 1:** So you can do your geometry modelling in SolidWorks or
[00:29:44:130 - 00:29:46:369] **Speaker 1:** another care package that you're more familiar with, or you
[00:29:46:369 - 00:29:48:750] **Speaker 1:** can do some basic modelling inside console.
[00:29:49:329 - 00:29:51:369] **Speaker 1:** For this course, we'll just do it inside console to
[00:29:51:369 - 00:29:51:910] **Speaker 1:** keep it simple.
[00:29:54:719 - 00:29:59:689] **Speaker 1:** And missing We'll, we'll talk about that later as well.
[00:30:02:400 - 00:30:04:000] **Speaker 1:** Here's some examples of different measures.
[00:30:04:479 - 00:30:09:540] **Speaker 1:** So we've got triangles, tetrahedrons, hexahedrals, quadrilaterals, pyramids, prisms.
[00:30:11:579 - 00:30:14:079] **Speaker 1:** The example here looks a bit like a wind tunnel.
[00:30:15:520 - 00:30:17:199] **Speaker 1:** And if we're looking at fluid mechanics we want to
[00:30:17:199 - 00:30:21:079] **Speaker 1:** resolve the boundary layers, so around the walls, so.
[00:30:21:859 - 00:30:24:030] **Speaker 1:** You squint, you'll be able to see that the the
[00:30:24:030 - 00:30:27:430] **Speaker 1:** elements are a little bit smaller around the perimeter of
[00:30:27:430 - 00:30:28:369] **Speaker 1:** those domains.
[00:30:28:750 - 00:30:31:229] **Speaker 1:** So those are the walls and you've got finer elements
[00:30:31:229 - 00:30:34:949] **Speaker 1:** next to those walls to resolve those velocity gradients to
[00:30:34:949 - 00:30:35:910] **Speaker 1:** those boundary layers.
[00:30:40:109 - 00:30:41:660] **Speaker 1:** There's several materials.
[00:30:42:869 - 00:30:44:949] **Speaker 1:** That you can select from or you can define your
[00:30:44:949 - 00:30:45:650] **Speaker 1:** own material.
[00:30:46:900 - 00:30:50:380] **Speaker 1:** The physics, we need to specify the boundary conditions.
[00:30:50:459 - 00:30:52:930] **Speaker 1:** So we've talked about that for our analytical solutions, but
[00:30:52:930 - 00:30:55:060] **Speaker 1:** also numerically we need to define the boundary conditions to
[00:30:55:060 - 00:30:57:520] **Speaker 1:** have a closed problem, otherwise there's an infinite number of
[00:30:57:520 - 00:30:58:709] **Speaker 1:** solutions and it can't solve.
[00:30:59:219 - 00:31:02:739] **Speaker 1:** So if you get An error along those lines, you'll
[00:31:02:739 - 00:31:04:760] **Speaker 1:** you'll know that you don't have a boundary condition defined.
[00:31:11:069 - 00:31:11:829] **Speaker 1:** The study.
[00:31:16:099 - 00:31:21:510] **Speaker 1:** Low-level study settings, so, um, There's some generic settings that
[00:31:21:510 - 00:31:21:959] **Speaker 1:** are set up.
[00:31:22:280 - 00:31:24:180] **Speaker 1:** You can also have quite fine control.
[00:31:24:680 - 00:31:28:040] **Speaker 1:** So obviously it's a closed source, uh, software, so you
[00:31:28:469 - 00:31:32:020] **Speaker 1:** can't edit everything, but they've provided a graphical user interface
[00:31:32:020 - 00:31:34:310] **Speaker 1:** GUI for quite a lot of their their settings.
[00:31:34:359 - 00:31:37:280] **Speaker 1:** So you can edit quite a lot, but obviously not
[00:31:37:280 - 00:31:38:660] **Speaker 1:** the same if you write your own code.
[00:31:40:680 - 00:31:43:810] **Speaker 1:** Uh, nonlinear solvers, so we're mostly looking at linear equations
[00:31:43:810 - 00:31:48:619] **Speaker 1:** in this course, but Nonlinear equations are everywhere.
[00:31:51:060 - 00:31:55:199] **Speaker 1:** Direct and iterative solvers, uh, and then last is visualisation.
[00:31:56:910 - 00:32:01:699] **Speaker 1:** So, You want to visualise the results, we've looked at
[00:32:01:699 - 00:32:06:079] **Speaker 1:** using MapPplotlib and Python, and you can do visualisation and
[00:32:06:079 - 00:32:06:819] **Speaker 1:** console as well.
[00:32:08:900 - 00:32:14:449] **Speaker 1:** Yeah And there are some inbuilt reports, but I wouldn't
[00:32:14:449 - 00:32:16:250] **Speaker 1:** bother with, bother with those.
[00:32:17:150 - 00:32:20:550] **Speaker 1:** So documentation, as with any commercial software, they have time
[00:32:20:550 - 00:32:23:630] **Speaker 1:** and money to spend on producing really good quality documentation.
[00:32:23:910 - 00:32:25:670] **Speaker 1:** So it's a really good place to start if you're
[00:32:25:670 - 00:32:28:449] **Speaker 1:** stuck, and we actually follow this documentation to go through
[00:32:28:449 - 00:32:30:189] **Speaker 1:** for that first lab this week.
[00:32:32:729 - 00:32:36:089] **Speaker 1:** So you can access via file help documentation or control
[00:32:36:089 - 00:32:36:650] **Speaker 1:** F1.
[00:32:37:170 - 00:32:41:790] **Speaker 1:** Uh, so that will be sort of HTML PDF, uh,
[00:32:42:099 - 00:32:42:949] **Speaker 1:** documentation.
[00:32:43:130 - 00:32:46:650] **Speaker 1:** If you want in context or dynamic help, then it's
[00:32:46:650 - 00:32:47:729] **Speaker 1:** file help, help.
[00:32:49:280 - 00:32:50:780] **Speaker 1:** Model application libraries.
[00:32:51:119 - 00:32:54:069] **Speaker 1:** So under application libraries, there's a, there's a large number
[00:32:54:069 - 00:32:55:819] **Speaker 1:** of models that I've created already.
[00:32:56:349 - 00:32:59:719] **Speaker 1:** So next year when you're doing your FYP projects, you
[00:32:59:719 - 00:33:01:959] **Speaker 1:** might find that you want to analyse something and you
[00:33:01:959 - 00:33:04:260] **Speaker 1:** want something as a, as a starting position.
[00:33:04:989 - 00:33:07:359] **Speaker 1:** Uh, so flicking through the application libraries or the online
[00:33:07:359 - 00:33:09:310] **Speaker 1:** models is the is the best place to start.
[00:33:10:329 - 00:33:12:609] **Speaker 1:** Um, so if you create something from scratch, it's a
[00:33:12:609 - 00:33:15:530] **Speaker 1:** bit harder than if you're starting from a, an example.
[00:33:19:359 - 00:33:21:540] **Speaker 1:** And there are step by step instructions for a lot
[00:33:21:540 - 00:33:24:469] **Speaker 1:** of the models and tutorials, and that's, we'll go through
[00:33:24:469 - 00:33:26:439] **Speaker 1:** at least a couple in the console labs.
[00:33:28:349 - 00:33:31:510] **Speaker 1:** Um, I mean, I haven't checked what the latest one
[00:33:31:510 - 00:33:31:790] **Speaker 1:** is.
[00:33:32:069 - 00:33:34:750] **Speaker 1:** That's probably from a couple of years ago, but there's
[00:33:34:989 - 00:33:36:869] **Speaker 1:** many pages, so you're not going to read all of
[00:33:36:869 - 00:33:37:410] **Speaker 1:** those.
[00:33:37:910 - 00:33:39:089] **Speaker 1:** Um.
[00:33:40:260 - 00:33:42:459] **Speaker 1:** But if you're stuck and want to read about the,
[00:33:42:540 - 00:33:44:939] **Speaker 1:** the theory, then that's a good place to, to hunt.
[00:33:47:380 - 00:33:49:300] **Speaker 1:** And that's what I just said, it's more helpful to
[00:33:49:300 - 00:33:52:660] **Speaker 1:** work through a similar problem, uh, and then continue from
[00:33:52:660 - 00:33:52:859] **Speaker 1:** there.
[00:34:02:680 - 00:34:04:479] **Speaker 1:** And there's a learning centre as well.
[00:34:05:040 - 00:34:06:229] **Speaker 1:** I have online videos.
[00:34:06:939 - 00:34:07:510] **Speaker 1:** Um.
[00:34:08:179 - 00:34:10:810] **Speaker 1:** It's sort of outside the scope of this course.
[00:34:10:969 - 00:34:13:300] **Speaker 1:** We teach you everything that you require within the labs,
[00:34:13:449 - 00:34:15:888] **Speaker 1:** uh, but if you're motivated, you're more than welcome to
[00:34:15:888 - 00:34:16:388] **Speaker 1:** explore.
[00:34:17:539 - 00:34:22:360] **Speaker 1:** And The last while, Oh, I've got plenty of time.
[00:34:22:658 - 00:34:25:500] **Speaker 1:** Power through, um, I want to do a demonstration.
[00:34:26:449 - 00:34:29:290] **Speaker 1:** Because Yeah.
[00:34:30:179 - 00:34:31:929] **Speaker 1:** It's a bit tedious reading through all of that.
[00:34:32:060 - 00:34:33:378] **Speaker 1:** You can read through it in your own time if
[00:34:33:378 - 00:34:33:719] **Speaker 1:** you want.
[00:34:34:729 - 00:34:39:020] **Speaker 1:** Um, But I just like to learn by doing.
[00:34:41:229 - 00:34:44:850] **Speaker 1:** Um, so we're gonna look at the class equation, which
[00:34:44:850 - 00:34:47:290] **Speaker 1:** is what we've already done quite a bit, and the
[00:34:47:290 - 00:34:49:110] **Speaker 1:** dependent variable field that we're looking at is a temperature,
[00:34:49:330 - 00:34:51:489] **Speaker 1:** so that's why we've got capital T, uh.
[00:34:53:378 - 00:34:54:360] **Speaker 1:** In the equation.
[00:34:55:398 - 00:35:15:050] **Speaker 1:** Uh, probably Uh We'll see what happens.
[00:35:15:379 - 00:35:17:139] **Speaker 1:** I'm just thinking the resolution might not look very good
[00:35:17:139 - 00:35:18:540] **Speaker 1:** on the projector, but we'll see.
[00:35:19:239 - 00:35:20:889] **Speaker 1:** Um, so we've got a Laplace equation, we've got a
[00:35:20:889 - 00:35:24:429] **Speaker 1:** rectangular domain of L by H, so length and height,
[00:35:24:929 - 00:35:26:810] **Speaker 1:** and we've got some boundary conditions.
[00:35:27:050 - 00:35:28:909] **Speaker 1:** So equations A 2 to 5.
[00:35:29:780 - 00:35:31:399] **Speaker 1:** And we're gonna use a structured mesh.
[00:35:32:159 - 00:35:34:760] **Speaker 1:** And we're going to look at the heat flux Q
[00:35:34:760 - 00:35:38:800] **Speaker 1:** dot, which is evaluated with the gradient minus K gravity.
[00:35:47:979 - 00:35:50:149] **Speaker 1:** That's still, it's still loading, so that's great.
[00:36:00:719 - 00:36:04:199] **Speaker 1:** Um, so the first step, well, It's loaded.
[00:36:16:070 - 00:36:16:870] **Speaker 1:** It's a bit painful.
[00:36:25:540 - 00:36:27:120] **Speaker 1:** So we've got 2 options.
[00:36:27:409 - 00:36:29:510] **Speaker 1:** Let me just open console initially.
[00:36:29:810 - 00:36:31:649] **Speaker 1:** We can either select the model wizard.
[00:36:33:010 - 00:36:34:729] **Speaker 1:** Which will guide you through setting up or you can
[00:36:34:729 - 00:36:36:310] **Speaker 1:** set with a start with a blank model.
[00:36:36:760 - 00:36:38:689] **Speaker 1:** So I'd suggest starting with the Model Wizard.
[00:36:40:560 - 00:36:41:739] **Speaker 1:** And it'll guide you through.
[00:36:42:199 - 00:36:45:600] **Speaker 1:** So in this case, we've got a two-dimensional domain.
[00:36:46:590 - 00:36:49:030] **Speaker 1:** So if we think back to chapter 2.
[00:36:50:209 - 00:36:51:729] **Speaker 1:** It's sort of similar to what we described here.
[00:36:51:810 - 00:36:55:159] **Speaker 1:** We've got a maybe a three-dimensional object because things are
[00:36:55:159 - 00:36:56:090] **Speaker 1:** 3D in real life.
[00:36:56:409 - 00:36:58:489] **Speaker 1:** But if it's fully insulated on the front and back,
[00:36:58:810 - 00:37:01:810] **Speaker 1:** essentially the heat transfer is not going in and out
[00:37:01:810 - 00:37:02:510] **Speaker 1:** of the page.
[00:37:02:729 - 00:37:05:370] **Speaker 1:** So we can approximate it as a 2D domain, which
[00:37:05:370 - 00:37:06:169] **Speaker 1:** is what we've done here.
[00:37:07:260 - 00:37:08:669] **Speaker 1:** So we're going to stick the 2D.
[00:37:09:969 - 00:37:11:290] **Speaker 1:** Uh, space dimension.
[00:37:13:729 - 00:37:16:330] **Speaker 1:** And we're going to solve the Laplace equation.
[00:37:17:360 - 00:37:19:820] **Speaker 1:** And I must have done this recently to check.
[00:37:20:280 - 00:37:21:860] **Speaker 1:** So this is recently used.
[00:37:22:560 - 00:37:24:000] **Speaker 1:** This is a list of all the physics that we
[00:37:24:000 - 00:37:25:399] **Speaker 1:** have um access to.
[00:37:26:780 - 00:37:30:100] **Speaker 1:** So fluid flow has a bunch of different types of
[00:37:30:100 - 00:37:30:300] **Speaker 1:** models.
[00:37:30:379 - 00:37:33:050] **Speaker 1:** So creeping flows, so really low stoke, uh, low renal
[00:37:33:050 - 00:37:36:810] **Speaker 1:** slumber, so maybe Stokes flow, laminar, sort of, sort of
[00:37:36:810 - 00:37:39:060] **Speaker 1:** a little bit low renal sums, and then higher renal
[00:37:39:060 - 00:37:40:179] **Speaker 1:** sums for turbulent flow.
[00:37:41:189 - 00:37:43:330] **Speaker 1:** Uh, so there's a whole bunch of different turbulence models
[00:37:43:330 - 00:37:45:750] **Speaker 1:** that you can learn about maybe if you take ENGR
[00:37:45:750 - 00:37:46:929] **Speaker 1:** 401 next year.
[00:37:47:659 - 00:37:48:850] **Speaker 1:** Uh, multi-phase.
[00:37:49:879 - 00:37:51:229] **Speaker 1:** And non-isothermal flow.
[00:37:52:699 - 00:37:55:020] **Speaker 1:** There's heat transfer, which we'll be doing a bit in
[00:37:55:020 - 00:37:55:580] **Speaker 1:** this class.
[00:37:55:899 - 00:37:58:659] **Speaker 1:** So we use heat transfer because it's reasonably straightforward and
[00:37:58:659 - 00:37:59:790] **Speaker 1:** intuitive to think about.
[00:38:00:139 - 00:38:02:260] **Speaker 1:** There's just one scalar field, so the temperature field.
[00:38:04:379 - 00:38:06:399] **Speaker 1:** Structural mechanics, we also look at this.
[00:38:07:110 - 00:38:08:620] **Speaker 1:** And this last one, mathematics.
[00:38:10:889 - 00:38:14:570] **Speaker 1:** Uh, we'll introduce this coefficient form PDE, but it's just
[00:38:14:570 - 00:38:16:909] **Speaker 1:** a more generic form of the equations.
[00:38:17:750 - 00:38:19:189] **Speaker 1:** And there are.
[00:38:19:860 - 00:38:21:139] **Speaker 1:** Classical PDs.
[00:38:23:110 - 00:38:26:149] **Speaker 1:** And Laplace equation is one of these, these classical ones.
[00:38:26:229 - 00:38:27:729] **Speaker 1:** So we'll just use this interface.
[00:38:28:830 - 00:38:32:229] **Speaker 1:** So we're going to add it to our physics interfaces.
[00:38:32:709 - 00:38:34:709] **Speaker 1:** So here we can select what we're going to label
[00:38:34:709 - 00:38:35:889] **Speaker 1:** the dependent variable.
[00:38:36:399 - 00:38:39:550] **Speaker 1:** So by default, it's you and we've used you as
[00:38:39:550 - 00:38:41:530] **Speaker 1:** a generic dependent variable before.
[00:38:42:000 - 00:38:43:739] **Speaker 1:** In this example, we're looking at temperature fields.
[00:38:43:790 - 00:38:46:110] **Speaker 1:** So it makes sense to relabel this to a capital
[00:38:46:110 - 00:38:46:389] **Speaker 1:** T.
[00:38:48:159 - 00:38:51:120] **Speaker 1:** We need to specify the units of the dependent variable
[00:38:51:120 - 00:38:51:959] **Speaker 1:** and the source term.
[00:38:53:409 - 00:38:56:250] **Speaker 1:** So we can search or insert our own.
[00:38:58:840 - 00:39:01:550] **Speaker 1:** So that sort of standard unit is Calvin.
[00:39:04:120 - 00:39:07:060] **Speaker 1:** And the source term, any idea what the source term
[00:39:07:479 - 00:39:09:000] **Speaker 1:** units would be for this equation?
[00:39:10:149 - 00:39:12:100] **Speaker 1:** I'll get you to think a little bit and uh,
[00:39:12:489 - 00:39:14:590] **Speaker 1:** so you don't get too tired, too sleepy.
[00:39:19:570 - 00:39:22:909] **Speaker 1:** The, yeah, the, um, coordinate systems and metres.
[00:39:23:969 - 00:39:26:879] **Speaker 1:** So the source term would be like the right-hand side.
[00:39:29:919 - 00:39:32:159] **Speaker 1:** If we think back to chapter one, this is quite
[00:39:32:159 - 00:39:35:040] **Speaker 1:** good, I think it's back to what we did earlier.
[00:39:38:739 - 00:39:39:959] **Speaker 1:** I'm not gonna find my chocolate one.
[00:39:48:919 - 00:39:50:139] **Speaker 1:** Equation 1.9.
[00:39:50:500 - 00:39:53:100] **Speaker 1:** So G is our source term that we require.
[00:39:53:179 - 00:39:56:100] **Speaker 1:** So to be dimensionally consistent, every term of this equation
[00:39:56:100 - 00:39:57:590] **Speaker 1:** has to have the same units, right?
[00:39:57:899 - 00:40:02:939] **Speaker 1:** So the units of that first term, any idea what
[00:40:02:939 - 00:40:06:419] **Speaker 1:** the units of second order derivative of temperature?
[00:40:07:280 - 00:40:09:600] **Speaker 1:** I mean, if we think of displacement and differentiate it
[00:40:09:600 - 00:40:10:500] **Speaker 1:** twice, what do we get?
[00:40:14:260 - 00:40:16:300] **Speaker 1:** Acceleration, so metres per second squared.
[00:40:16:899 - 00:40:20:290] **Speaker 1:** So we've got units of kelvin and differentiate with respect
[00:40:20:290 - 00:40:22:100] **Speaker 1:** to space twice.
[00:40:23:750 - 00:40:24:699] **Speaker 1:** Yeah, precisely.
[00:40:25:120 - 00:40:27:959] **Speaker 1:** So each term of this equation has to be kelvins
[00:40:27:959 - 00:40:28:679] **Speaker 1:** per metre squad.
[00:40:28:919 - 00:40:30:679] **Speaker 1:** So our source term has to be kelvins per metre
[00:40:30:679 - 00:40:31:120] **Speaker 1:** squared.
[00:40:31:520 - 00:40:36:060] **Speaker 1:** So we're gonna I don't know if there's a Um
[00:40:40:929 - 00:40:42:290] **Speaker 1:** I'm just going to type it out because I don't
[00:40:42:290 - 00:40:43:929] **Speaker 1:** want to look for it there.
[00:40:44:280 - 00:40:45:550] **Speaker 1:** So we've got Calvin.
[00:40:46:669 - 00:40:47:500] **Speaker 1:** Per metre squared.
[00:40:47:820 - 00:40:51:389] **Speaker 1:** So you could use the slash metre squared or times
[00:40:51:389 - 00:40:52:389] **Speaker 1:** metres to the -2.
[00:40:54:459 - 00:40:55:000] **Speaker 1:** All right.
[00:40:56:810 - 00:40:58:800] **Speaker 1:** So that is our units.
[00:41:01:899 - 00:41:04:620] **Speaker 1:** Now we can only solve this in city-state stationary.
[00:41:04:780 - 00:41:07:379] **Speaker 1:** There's no time dependence in our Laplace equation.
[00:41:07:699 - 00:41:10:260] **Speaker 1:** So that's why it's narrowed everything down and only given
[00:41:10:260 - 00:41:13:639] **Speaker 1:** us the option of, of a stationary, uh, solver.
[00:41:16:419 - 00:41:18:060] **Speaker 1:** And that gives you some details.
[00:41:19:989 - 00:41:20:949] **Speaker 1:** So, done.
[00:41:22:379 - 00:41:23:850] **Speaker 1:** I don't think we did anything earlier.
[00:41:33:540 - 00:41:33:979] **Speaker 1:** All right.
[00:41:35:010 - 00:41:36:620] **Speaker 1:** So this is sort of the interface of console.
[00:41:37:139 - 00:41:39:620] **Speaker 1:** Along the top you've got that ribbon, which is now
[00:41:39:620 - 00:41:42:729] **Speaker 1:** featured in the Microsoft products like Word and PowerPoint.
[00:41:42:780 - 00:41:45:899] **Speaker 1:** They put this ribbon at the top, um, and you
[00:41:45:899 - 00:41:48:060] **Speaker 1:** can flick through these tabs.
[00:41:48:879 - 00:41:50:679] **Speaker 1:** And generally you're starting from left to right.
[00:41:50:919 - 00:41:52:770] **Speaker 1:** So from the left through to the right.
[00:41:52:959 - 00:41:55:500] **Speaker 1:** And then, in the model builder is that model tree,
[00:41:56:040 - 00:41:57:800] **Speaker 1:** uh, and you go from top to bottom.
[00:41:58:280 - 00:42:02:340] **Speaker 1:** So We have the the parent or the major settings,
[00:42:02:389 - 00:42:04:040] **Speaker 1:** and then we've got some definitions that we can set
[00:42:04:040 - 00:42:04:419] **Speaker 1:** up.
[00:42:04:879 - 00:42:08:159] **Speaker 1:** So we've been told that we've got a length of
[00:42:08:159 - 00:42:09:340] **Speaker 1:** L and a height of H.
[00:42:10:280 - 00:42:12:139] **Speaker 1:** So we can create a new parameter.
[00:42:12:760 - 00:42:14:080] **Speaker 1:** Sort of similar to what you do in Python, you've
[00:42:14:080 - 00:42:16:300] **Speaker 1:** got your parameters set at the top of the code.
[00:42:17:050 - 00:42:18:989] **Speaker 1:** Um, an expression for L.
[00:42:19:929 - 00:42:21:520] **Speaker 1:** We've got a length of 2 metres.
[00:42:25:750 - 00:42:28:270] **Speaker 1:** And as I say, to insert units, we use square
[00:42:28:270 - 00:42:29:469] **Speaker 1:** brackets with the unit.
[00:42:30:340 - 00:42:32:620] **Speaker 1:** And a height of one.
[00:42:35:489 - 00:42:41:459] **Speaker 1:** You know So we have to find out uh domain
[00:42:41:459 - 00:42:41:870] **Speaker 1:** parameters.
[00:42:42:909 - 00:42:48:949] **Speaker 1:** The next step Is to create the geometry.
[00:42:50:280 - 00:42:54:310] **Speaker 1:** So There's a few inbuilt uh shapes.
[00:42:54:520 - 00:42:55:729] **Speaker 1:** So there's one for rectangle.
[00:42:56:860 - 00:42:59:100] **Speaker 1:** So we use that and it's got a width of
[00:42:59:100 - 00:43:01:459] **Speaker 1:** L and a height of H.
[00:43:04:610 - 00:43:08:100] **Speaker 1:** So by default, it's positioning it in the, at the
[00:43:08:100 - 00:43:10:659] **Speaker 1:** origin 00 and that's what we want.
[00:43:10:939 - 00:43:12:239] **Speaker 1:** So we'll leave it as the default.
[00:43:13:370 - 00:43:19:659] **Speaker 1:** The next step is to define our physics, the equation.
[00:43:19:969 - 00:43:23:709] **Speaker 1:** So under the Laplace equation, we can expand the equation
[00:43:23:889 - 00:43:26:000] **Speaker 1:** section and just check what we're solving.
[00:43:26:250 - 00:43:28:370] **Speaker 1:** So this is the equation that console's going to solve
[00:43:28:370 - 00:43:28:610] **Speaker 1:** for us.
[00:43:28:689 - 00:43:29:550] **Speaker 1:** We've got grad.
[00:43:29:729 - 00:43:31:850] **Speaker 1:** minus grad T equal to 0.
[00:43:33:600 - 00:43:35:840] **Speaker 1:** It's not exactly the same form as what we've got
[00:43:35:840 - 00:43:37:080] **Speaker 1:** here, but they're equivalent.
[00:43:37:479 - 00:43:43:409] **Speaker 1:** So if you've got grad T, Um, grad grad, uh,
[00:43:43:489 - 00:43:48:129] **Speaker 1:** it expands to D2T by DX2 plus D2T by DY2
[00:43:48:129 - 00:43:48:770] **Speaker 1:** and 2D.
[00:43:54:939 - 00:44:00:679] **Speaker 1:** The default boundary conditions for finite elements is um 0
[00:44:00:679 - 00:44:01:520] **Speaker 1:** Neumann conditions.
[00:44:01:620 - 00:44:03:719] **Speaker 1:** So the gradient is going to be equal to 0.
[00:44:03:840 - 00:44:05:639] **Speaker 1:** So I can expand the equation tab as well.
[00:44:05:959 - 00:44:08:229] **Speaker 1:** So grad T equal to 0 on all of those
[00:44:08:229 - 00:44:08:860] **Speaker 1:** perimeters.
[00:44:09:479 - 00:44:13:399] **Speaker 1:** So that's essentially insulating at these boundaries.
[00:44:13:600 - 00:44:16:229] **Speaker 1:** So there's no heat transfer across because we know from
[00:44:16:229 - 00:44:19:830] **Speaker 1:** um Is a Fourer's law that the heat flux is
[00:44:19:830 - 00:44:21:179] **Speaker 1:** equal to -K gravity.
[00:44:23:780 - 00:44:26:600] **Speaker 1:** The boundary conditions that we've been asked to impose.
[00:44:28:260 - 00:44:32:919] **Speaker 1:** Is this Norman 0 or homogeneous norman boundary condition for
[00:44:32:919 - 00:44:34:810] **Speaker 1:** X equals 0 and Y equals 0.
[00:44:35:139 - 00:44:36:840] **Speaker 1:** So that's on the left and bottom.
[00:44:37:270 - 00:44:38:520] **Speaker 1:** So we don't need to do anything there.
[00:44:39:620 - 00:44:43:219] **Speaker 1:** We've been asked to set the temperature field on the
[00:44:43:219 - 00:44:47:260] **Speaker 1:** top edge, equal to the coordinate X.
[00:44:48:760 - 00:44:51:739] **Speaker 1:** So the temperature is going to rise from 0 up
[00:44:51:739 - 00:44:52:520] **Speaker 1:** to 2.
[00:44:54:879 - 00:44:58:709] **Speaker 1:** So what type of boundary condition is, is this?
[00:44:58:770 - 00:45:00:959] **Speaker 1:** Is this Dereklay Neumann, or Robin?
[00:45:05:699 - 00:45:07:979] **Speaker 1:** If we're setting the temperature directly.
[00:45:09:600 - 00:45:10:120] **Speaker 1:** Directly, yeah.
[00:45:11:040 - 00:45:13:030] **Speaker 1:** So we're going to create a new boundary.
[00:45:13:879 - 00:45:15:149] **Speaker 1:** Of a boundary condition.
[00:45:17:110 - 00:45:18:050] **Speaker 1:** And on the top.
[00:45:21:030 - 00:45:23:219] **Speaker 1:** We're going to set that value equal to the x
[00:45:23:219 - 00:45:23:689] **Speaker 1:** coordinate.
[00:45:24:479 - 00:45:29:800] **Speaker 1:** So the temperature Field has units Kelvin and obviously X
[00:45:29:800 - 00:45:32:040] **Speaker 1:** has got units of metres, so it's going to whinge
[00:45:32:320 - 00:45:34:020] **Speaker 1:** to us that it's not right.
[00:45:35:300 - 00:45:36:899] **Speaker 1:** You, I don't know if you can see, you can
[00:45:36:899 - 00:45:38:479] **Speaker 1:** see it's got a little red squiggle.
[00:45:39:060 - 00:45:41:060] **Speaker 1:** And if you hover over it, it says that the
[00:45:41:060 - 00:45:43:770] **Speaker 1:** unit given is metres and it should be kelvin.
[00:45:43:820 - 00:45:44:899] **Speaker 1:** So it's just reminding you.
[00:45:45:689 - 00:45:47:550] **Speaker 1:** You could just do a little bit of a quick
[00:45:47:770 - 00:45:53:389] **Speaker 1:** um Heck, I guess, um, to to fix the unit,
[00:45:53:889 - 00:45:55:090] **Speaker 1:** but this is just an example.
[00:45:58:290 - 00:46:00:590] **Speaker 1:** We've got another directly bounded condition on the right-hand side
[00:46:00:590 - 00:46:01:909] **Speaker 1:** at X equal to L.
[00:46:05:250 - 00:46:09:850] **Speaker 1:** So we can create a new directly boundary condition and
[00:46:09:850 - 00:46:11:370] **Speaker 1:** select the right-hand side.
[00:46:13:399 - 00:46:15:760] **Speaker 1:** And this time it is equal to Y.
[00:46:21:550 - 00:46:25:090] **Speaker 1:** Now we've defined our pity that we want to solve
[00:46:25:090 - 00:46:25:879] **Speaker 1:** the domain.
[00:46:26:770 - 00:46:27:959] **Speaker 1:** And the boundary conditions.
[00:46:27:969 - 00:46:30:770] **Speaker 1:** The next step is to create the mesh, and it's
[00:46:30:770 - 00:46:32:709] **Speaker 1:** asked us to create a structured grid.
[00:46:33:750 - 00:46:36:110] **Speaker 1:** So if we just build the default maybe as an
[00:46:36:110 - 00:46:36:570] **Speaker 1:** example.
[00:46:37:669 - 00:46:41:070] **Speaker 1:** It's just unstructured, it's all these triangles, but we can
[00:46:41:070 - 00:46:43:409] **Speaker 1:** create a map mesh by selecting.
[00:46:45:320 - 00:46:49:000] **Speaker 1:** That You'll go through these in the labs later on,
[00:46:49:100 - 00:46:50:520] **Speaker 1:** don't worry about too much of the detail.
[00:46:50:560 - 00:46:52:679] **Speaker 1:** I just wanna give you an overview of the the
[00:46:52:679 - 00:46:53:239] **Speaker 1:** workflow.
[00:46:53:800 - 00:46:54:939] **Speaker 1:** So this is a structured grid.
[00:46:55:919 - 00:46:58:340] **Speaker 1:** The next step is to solve, so study one.
[00:46:59:750 - 00:47:09:320] **Speaker 1:** Compute So it's informing us the uh Well, there's, there
[00:47:09:320 - 00:47:13:820] **Speaker 1:** was 310 elements for the unstructured grid and then 120
[00:47:13:989 - 00:47:14:919] **Speaker 1:** for the structured grid.
[00:47:15:770 - 00:47:19:459] **Speaker 1:** Which resulted in 2 527 degrees of freedom solved.
[00:47:19:820 - 00:47:21:739] **Speaker 1:** So that's sort of how many equations it's solving.
[00:47:22:100 - 00:47:23:979] **Speaker 1:** So even on this quite small problem, you can see
[00:47:23:979 - 00:47:25:860] **Speaker 1:** that the matrices are going to get quite large if
[00:47:25:860 - 00:47:28:699] **Speaker 1:** we're going to do a direct, um, solve.
[00:47:29:500 - 00:47:31:709] **Speaker 1:** So it took 4 seconds for that to solve.
[00:47:33:439 - 00:47:39:219] **Speaker 1:** Now One way to visualise these is to exaggerate the
[00:47:39:219 - 00:47:40:429] **Speaker 1:** vertical direction.
[00:47:40:679 - 00:47:50:149] **Speaker 1:** So that was with Hot, uh I think that's a
[00:47:50:149 - 00:47:50:989] **Speaker 1:** hard exhibition.
[00:47:51:850 - 00:47:52:250] **Speaker 1:** Yeah.
[00:47:52:989 - 00:47:57:659] **Speaker 1:** So I just sort of Holds the domain as a
[00:47:57:659 - 00:47:58:610] **Speaker 1:** function of temperature.
[00:47:59:350 - 00:48:01:290] **Speaker 1:** That doesn't really help too much, to be honest.
[00:48:06:989 - 00:48:07:590] **Speaker 1:** Disable.
[00:48:11:639 - 00:48:13:419] **Speaker 1:** So we want to try and replicate what we've done
[00:48:13:570 - 00:48:13:889] **Speaker 1:** here.
[00:48:14:050 - 00:48:16:090] **Speaker 1:** So instead of having filled contours, we're going to have
[00:48:16:090 - 00:48:17:310] **Speaker 1:** unfilled contours.
[00:48:26:919 - 00:48:28:510] **Speaker 1:** So we're gonna hide that initial one.
[00:48:30:169 - 00:48:32:110] **Speaker 1:** Probably should have got the mouse out for this, but.
[00:48:33:399 - 00:48:34:520] **Speaker 1:** We can use the trackpad.
[00:48:37:399 - 00:48:41:560] **Speaker 1:** So that's the contours, um, again, making sure that the
[00:48:41:560 - 00:48:43:540] **Speaker 1:** solution satisfies the boundary conditions.
[00:48:44:729 - 00:48:49:729] **Speaker 1:** The contour lines are perpendicular to the boundaries, which is
[00:48:49:729 - 00:48:51:000] **Speaker 1:** expected when the gradient is zero.
[00:48:51:379 - 00:48:53:330] **Speaker 1:** So it's on the left and bottom, and then it's
[00:48:53:330 - 00:48:55:729] **Speaker 1:** equal to those prescribed values of X and Y on
[00:48:55:729 - 00:48:56:429] **Speaker 1:** the top and right.
[00:48:57:550 - 00:49:02:229] **Speaker 1:** Last step is to display the the um heat flux
[00:49:02:229 - 00:49:03:550] **Speaker 1:** vectors, so Q dot.
[00:49:04:840 - 00:49:07:800] **Speaker 1:** So what we can do is, if I remember.
[00:49:10:800 - 00:49:12:090] **Speaker 1:** Harrow's surface.
[00:49:16:330 - 00:49:20:639] **Speaker 1:** Yeah So at the moment it's scaling with size, so
[00:49:20:639 - 00:49:21:780] **Speaker 1:** we can probably disable.
[00:49:23:360 - 00:49:24:290] **Speaker 1:** The scaling.
[00:49:29:899 - 00:49:33:860] **Speaker 1:** And at the moment all we've done is plotted the
[00:49:33:860 - 00:49:38:949] **Speaker 1:** gradient TX, but we actually want minus K times T
[00:49:39:580 - 00:49:40:429] **Speaker 1:** I DX.
[00:49:40:939 - 00:49:45:360] **Speaker 1:** So We know that ah heat transfers from hot to
[00:49:45:360 - 00:49:47:560] **Speaker 1:** cold, not cold to hot, so we can flip around
[00:49:47:560 - 00:49:48:360] **Speaker 1:** those arrows.
[00:49:50:389 - 00:49:53:739] **Speaker 1:** And Yeah, that was.
[00:49:54:679 - 00:49:58:120] **Speaker 1:** This exercise That I wanted to go through.
[00:49:58:389 - 00:50:00:639] **Speaker 1:** So, I just wanted to show you because otherwise it's
[00:50:00:639 - 00:50:02:159] **Speaker 1:** a little bit daunting when you open a console to
[00:50:02:159 - 00:50:07:270] **Speaker 1:** start with, um, on Thursday, and The lab that you're
[00:50:07:270 - 00:50:08:399] **Speaker 1:** gonna be working through.
[00:50:10:020 - 00:50:11:899] **Speaker 1:** Is this wrench, so.
[00:50:12:709 - 00:50:14:810] **Speaker 1:** Following the instructions, file help documentation.
[00:50:16:889 - 00:50:19:129] **Speaker 1:** And that's pretty much it for this week.
[00:50:19:370 - 00:50:23:649] **Speaker 1:** So we'll see you tomorrow, um, and the labs are
[00:50:23:649 - 00:50:24:489] **Speaker 1:** working on console.
[00:51:10:709 - 00:51:17:120] **Speaker 0:** I've got I like.
[00:51:18:550 - 00:51:28:550] **Speaker 0:** You F.
[00:51:30:169 - 00:51:30:189] **Speaker 0:** It was.
[00:51:38:639 - 00:51:50:669] **Speaker 0:** What Thank you.
[00:51:55:939 - 00:52:11:000] **Speaker 0:** Yeah Yes, that's I I think I do I.
[00:52:11:790 - 00:52:14:540] **Speaker 0:** Oh God That's ridiculous.
[00:52:15:500 - 00:52:18:020] **Speaker 0:** I don't I like this.
[00:52:58:030 - 00:52:59:189] **Speaker 0:** It was like none of us.
[00:53:00:100 - 00:53:01:149] **Speaker 0:** There's no way I would have said it.
[00:54:15:320 - 00:54:15:330] **Speaker 0:** Mm.

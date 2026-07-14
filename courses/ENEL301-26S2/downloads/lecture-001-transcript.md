# ENEL301-26S2 Lecture 1 local ASR transcript

Date: July 14, 2026 1:00pm-1:55pm
Transcript type: Hermes-generated local ASR from validated Echo audio, not a native Echo transcript.
Backend/model: faster-whisper small.en, CPU int8, beam_size=5, vad_filter=True.
Source audio SHA-256: `66b24ef3b7ee7ac752338022cbe4efad6cc752cbb2ffa8836c65ac02c3a2b00a`
Generated: 2026-07-14T23:17:21.084728+12:00
Caveat: technical terms, equations, names and Māori words may require checking against slides/audio.

[00:00:03.540 - 00:00:13.920] Okay, tenne koutou, tenne koutou, tenne koutou katoa, nou mai hari mai kite ne aka longa,
[00:00:13.920 - 00:00:15.760] koa enda krosan takawingawa.
[00:00:15.760 - 00:00:22.880] Hi everyone, I'm Enda, I'm the course coordinator and main lecturer for 301.
[00:00:22.880 - 00:00:28.200] So today is going to be largely a little bit of administration, but we'll also start getting
[00:00:28.200 - 00:00:29.520] into some ethics.
[00:00:30.240 - 00:00:38.660] But first off, I'd just like to introduce myself to you all, so I was born in Northern
[00:00:38.660 - 00:00:45.740] Ireland, so that's where my funny first name comes from, but my family moved to Australia
[00:00:45.740 - 00:00:52.520] when I was a young boy due to the terrorism problems in Northern Ireland, so I grew up
[00:00:52.520 - 00:00:53.520] in Australia.
[00:00:53.520 - 00:00:55.720] So that's where my accent comes from.
[00:00:55.720 - 00:01:02.560] I studied manufacturing and materials engineering at the University of Queensland in Brisbane,
[00:01:02.560 - 00:01:10.820] and then I worked in industry for about seven years in a number of roles, including Queensland
[00:01:10.820 - 00:01:13.920] Rail, which was good fun, and then some consulting work.
[00:01:13.920 - 00:01:20.880] I then went back and did a PhD also in materials engineering, and during that time I also
[00:01:20.880 - 00:01:26.480] went to live in Germany for a year, which is really awesome fun to help commercialise
[00:01:26.480 - 00:01:29.600] some of the research that I was doing.
[00:01:29.600 - 00:01:39.460] Then I moved to Melbourne, where I started my academic career back in 2010, so I was a lifecycle
[00:01:39.460 - 00:01:49.780] assessment consultant at RMIT University for about five years, and then I moved into lecturing
[00:01:49.780 - 00:01:59.260] mechanical engineering, so I was helping out with design teaching, and then I moved to
[00:01:59.260 - 00:02:07.180] Screenburne University, helped set up a new Bachelor of Engineering honours, and in 2019
[00:02:07.180 - 00:02:14.580] I found a job ad from New Zealand, and it was basically me on a page.
[00:02:14.580 - 00:02:19.760] My wife is from Wonganui in the North Island, and we'd always wanted to move back to
[00:02:19.760 - 00:02:23.500] New Zealand, and the stars kind of aligned.
[00:02:23.500 - 00:02:31.760] So I moved to UC in 2020, I was looking after the Master of Engineering management postgraduate
[00:02:31.760 - 00:02:37.400] programme for a number of years, and then I got shoulder tapped to become the Head of
[00:02:37.400 - 00:02:40.360] Department in electrical and computer engineering.
[00:02:40.360 - 00:02:47.900] So that's what I'm doing now, as well as a bit of teaching.
[00:02:47.900 - 00:02:56.440] So look, I took over this course last year, it was in a pretty bad state before that, so
[00:02:56.440 - 00:03:03.820] you might have heard that 301 is kind of like Eng 101, but I'm hoping to make it a little
[00:03:03.820 - 00:03:05.780] bit better than that, in fact much better.
[00:03:05.780 - 00:03:12.860] So I really revamped the course last year, and got some really positive feedback from people
[00:03:13.020 - 00:03:18.900] who took it, which is awesome, but look, I'm really trying to bring to you a course that
[00:03:18.900 - 00:03:25.900] is really useful and practical for your work as an emerging engineer.
[00:03:26.920 - 00:03:32.300] That being said, it is one of the hardest courses to teach, and there's a number of
[00:03:32.300 - 00:03:40.180] reasons for that which we'll unpack over the next few weeks, but the best thing I
[00:03:40.180 - 00:03:43.500] can do is to say this to you.
[00:03:43.500 - 00:03:50.020] This will be one of the most important courses that you do as your engineer in training,
[00:03:50.020 - 00:03:56.020] and if you don't believe me, come back five years after you graduate, and prove to me
[00:03:56.020 - 00:03:59.440] why it isn't.
[00:03:59.440 - 00:04:05.980] So you becoming and developing an engineer will take decades, and our role here at UC,
[00:04:05.980 - 00:04:09.700] including this course, is to make sure that you've got enough skills and knowledge to
[00:04:09.700 - 00:04:17.360] get you going in your graduate engineering career.
[00:04:17.360 - 00:04:20.360] So why does this course exist?
[00:04:20.360 - 00:04:25.560] Well, despite what you may have heard, this is not a course about teaching you to be a
[00:04:25.560 - 00:04:30.960] manager, nor is it a course about teaching you how to write.
[00:04:30.960 - 00:04:36.680] Someone last year said, oh, this course is about writing, so no, it's not.
[00:04:36.680 - 00:04:42.680] The following points are a synthesis of some of the existing research on practicing engineers.
[00:04:42.680 - 00:04:48.360] So it's actually my research specialization as well, as I study what engineers do in their
[00:04:48.360 - 00:04:50.640] work.
[00:04:50.640 - 00:04:57.160] So this work, these points are drawing upon a guy called James Trevelyan, he's a retired
[00:04:57.160 - 00:05:02.500] mechatronics engineer from Western Australia.
[00:05:02.500 - 00:05:11.180] So one of the interesting observations is that global productivity is dropping.
[00:05:11.180 - 00:05:15.780] And with that, people's standards of living are also dropping.
[00:05:15.780 - 00:05:21.980] In fact, a lot of the political unrest, including all seeing in Western countries, is arguably
[00:05:21.980 - 00:05:27.220] driven by these degrading standards of living.
[00:05:27.220 - 00:05:29.860] So why is productivity slipping?
[00:05:30.180 - 00:05:37.460] Well, one theory that's been put forward is that social media use could actually be undermining
[00:05:37.460 - 00:05:41.820] collaboration and how we work together.
[00:05:41.820 - 00:05:47.620] Collaboration drives performance in engineering, and with that, value.
[00:05:47.620 - 00:05:55.370] And I'll talk more about what value means later in the semester.
[00:05:55.370 - 00:06:02.050] One of the great things about engineering is that we'll, oops, sorry, where's my cursor
[00:06:02.050 - 00:06:08.970] gone, is that we get to spend lots of people's money.
[00:06:08.970 - 00:06:12.050] It's usually not yours.
[00:06:12.050 - 00:06:19.650] So I remember when I worked at Queensland Rail, I had responsibility over, I think, a $300
[00:06:19.650 - 00:06:21.810] million contract.
[00:06:21.810 - 00:06:25.370] It's like, that's pretty cool.
[00:06:25.370 - 00:06:30.130] But with that comes a great responsibility.
[00:06:30.130 - 00:06:39.970] Problem is, though, is that engineers, unfortunately, aren't very good at managing money.
[00:06:39.970 - 00:06:44.570] In fact, we're really good at wasting it.
[00:06:44.570 - 00:06:48.810] Some statistics around this are really quite shocking.
[00:06:48.810 - 00:06:56.450] So there's a company that came out of the Rand Corporation in the US, and they do post-mortems
[00:06:56.450 - 00:06:59.210] on why projects fail.
[00:06:59.210 - 00:07:07.810] And they say that one in six projects end up in financial disaster and financial ruin.
[00:07:07.810 - 00:07:15.130] So hundreds of millions of dollars get spent on projects with nothing to show for it.
[00:07:15.130 - 00:07:25.380] And there was a very recent one in the media here just recently relating to software.
[00:07:25.380 - 00:07:27.860] So what are the reasons for this?
[00:07:27.860 - 00:07:35.860] Well, collaboration, or poor collaboration, is the number one reason why projects fail.
[00:07:35.860 - 00:07:41.900] Or in other words, if you get collaboration right, your projects are going to succeed.
[00:07:41.900 - 00:07:46.740] And culture and communication are also key determinants for successful collaboration.
[00:07:46.740 - 00:07:51.180] And that's going to be the focus of the first part of the course.
[00:07:51.180 - 00:07:58.270] Next, engineers need to do the right thing.
[00:07:58.270 - 00:07:59.270] But what does that mean?
[00:07:59.710 - 00:08:04.310] That's what we're going to focus on today, a bit of ethics.
[00:08:04.310 - 00:08:14.630] And finally, so with doing the right thing, we need to recognize that social culture shapes
[00:08:14.630 - 00:08:18.470] us and therefore our ethics and how we view the world.
[00:08:18.470 - 00:08:21.390] And everyone is different.
[00:08:21.390 - 00:08:24.630] You need to follow the law, but what does that actually mean?
[00:08:24.630 - 00:08:29.590] And engineers also must ensure sustainable resource use.
[00:08:29.590 - 00:08:36.870] Finally, engineers are experts in making things happen in the face of uncertainty.
[00:08:36.870 - 00:08:43.350] How we do that is by managing risk as well as working with stakeholders closely to make
[00:08:43.350 - 00:08:50.230] sure that we get their views incorporated into projects very early on to maximize value and
[00:08:50.230 - 00:08:51.590] acceptance.
[00:08:54.050 - 00:09:04.970] OK, so this is what industry have told us at UC about what they expect UC graduates to come
[00:09:04.970 - 00:09:05.730] out with.
[00:09:05.730 - 00:09:08.970] And these are the learning outcomes for this course.
[00:09:08.970 - 00:09:16.170] So you'll be expected to apply ethical principles within engineering contexts, also
[00:09:16.170 - 00:09:22.090] recognizing the social and cultural factors which affect ethics, apply individual and
[00:09:22.090 - 00:09:28.090] inclusive management and teamwork practice techniques, conduct financial analysis,
[00:09:28.090 - 00:09:33.610] including estimations of cost, cash flow, financial balances and financial viability.
[00:09:33.610 - 00:09:36.970] OK, going to look after that next term.
[00:09:36.970 - 00:09:41.530] Evaluate the viability of different engineering projects, accounting for a whole heap of
[00:09:41.530 - 00:09:42.490] different factors.
[00:09:44.770 - 00:09:50.690] And then implement engineering risk management and project management techniques,
[00:09:50.690 - 00:09:54.450] including managing different stakeholders.
[00:09:54.450 - 00:09:56.610] Please excuse my voice today.
[00:09:56.610 - 00:10:01.210] I caught a cold over the weekend, but I think I'm on the mend.
[00:10:01.210 - 00:10:03.130] OK, so a little bit of admin.
[00:10:03.130 - 00:10:05.330] So lectures, yeah, good that you're here today.
[00:10:05.330 - 00:10:08.530] Please turn up on Friday as well.
[00:10:08.530 - 00:10:09.890] Same place.
[00:10:09.890 - 00:10:14.010] And then tutorials and workshops.
[00:10:14.010 - 00:10:16.290] So there's two types of tutorials here.
[00:10:16.290 - 00:10:19.490] There's tutorial A and then tutorial B.
[00:10:19.490 - 00:10:26.530] Tutorial A runs for week this week and then weeks four to 12 inclusive.
[00:10:26.530 - 00:10:36.130] And there's two timetable slots, Wednesday three to four or Wednesday four to five.
[00:10:36.130 - 00:10:42.530] And then you also have tutorial B, which happens in week two or three.
[00:10:42.530 - 00:10:47.170] And that's a two hour workshop from three to five.
[00:10:47.170 - 00:10:51.530] So please check your timetable for your room.
[00:10:51.530 - 00:10:58.570] If you haven't allocated yourself already, please do so by the end of next Monday.
[00:10:58.570 - 00:11:04.450] If you haven't allocated yourself, I'll allocate for you.
[00:11:04.450 - 00:11:08.690] If you've got a conflict, a timetable conflict, and you can't actually timetable
[00:11:08.690 - 00:11:11.410] in, send me an email and I can help.
[00:11:11.410 - 00:11:16.730] OK, and I'll manually push you into one of the tutorials.
[00:11:16.730 - 00:11:25.250] OK, so again, just make sure that you have yourself locked into one of these tutorials,
[00:11:25.250 - 00:11:28.450] A and B, by Monday.
[00:11:28.450 - 00:11:36.170] And just a heads up too, that if you were in E12 tomorrow at three to four,
[00:11:36.170 - 00:11:40.450] we realized yesterday that timetabling stuffed up,
[00:11:40.450 - 00:11:45.770] that we're going to try and put 80 of you into a room of 46.
[00:11:45.770 - 00:11:55.260] That doesn't sound very comfortable, so we have to move a whole lot of people out into the drawing rooms.
[00:11:55.260 - 00:11:59.740] OK, so lectures will be recorded as per usual.
[00:11:59.740 - 00:12:07.300] So after this lecture, I'll put the recording on Learn under this section.
[00:12:07.300 - 00:12:09.980] The tutorials and workshops are not recorded.
[00:12:09.980 - 00:12:15.500] And the reason for that is that there's a really substantial interactive component to it.
[00:12:15.500 - 00:12:22.220] So turn up to make sure you get the most out of those sessions.
[00:12:22.220 - 00:12:25.980] OK, assessment wise, look, it's pretty straightforward.
[00:12:25.980 - 00:12:32.820] So you've got the bi-cultural confidence and competence workshops next week and the week after.
[00:12:32.820 - 00:12:37.500] Again, just allocate yourselves to one of those.
[00:12:37.500 - 00:12:42.780] You get a 1% there for rocking up and attending.
[00:12:42.780 - 00:12:55.500] And then got a video PPI submission due basically nine days after your workshop.
[00:12:55.500 - 00:13:03.100] And then a midterm test on the Tuesday immediately after the mid-semester break.
[00:13:03.100 - 00:13:12.500] And that's been scheduled in for 6.30 to 7.30 on Tuesday night in the C1, C2 lecture theatres.
[00:13:12.500 - 00:13:18.780] So refer to your timetable just to make sure that you're in the – get your room right.
[00:13:18.780 - 00:13:22.020] Have a sustainability assignment due towards the end of semester.
[00:13:22.020 - 00:13:25.140] I think that's week 11 from memory.
[00:13:25.140 - 00:13:27.780] And then a final exam.
[00:13:27.780 - 00:13:34.660] So pretty similar assessment structure to what we had last year.
[00:13:34.660 - 00:13:39.460] The attendance of the week two and three workshop is compulsory.
[00:13:39.460 - 00:13:45.140] And if you don't attend, you won't get the 1% grade.
[00:13:45.140 - 00:13:52.420] OK, the PPIHA and sustainability assignment are all submitted via Learn.
[00:13:52.420 - 00:13:55.940] And we're both subject to turn it in.
[00:13:55.940 - 00:14:01.300] OK, but turn it in doesn't work on videos, obviously.
[00:14:01.300 - 00:14:03.780] OK, late penalties.
[00:14:03.780 - 00:14:08.580] So it's a 10% in absolute terms per day late or part thereof.
[00:14:09.220 - 00:14:12.100] That'll be deducted from the original mark, OK?
[00:14:12.100 - 00:14:19.380] So if you end up with a raw grade of 83%, but it was one day late,
[00:14:19.380 - 00:14:24.180] we'd knock off 10% in total from that.
[00:14:24.180 - 00:14:28.100] And then likewise, it just keeps going down from there.
[00:14:28.100 - 00:14:32.010] Cool, any questions about that so far?
[00:14:32.010 - 00:14:34.970] Cool, nice and easy.
[00:14:34.970 - 00:14:41.970] OK, yeah, if you've got a request for an extension for those assignments,
[00:14:41.970 - 00:14:45.690] please let me know via email.
[00:14:45.690 - 00:14:49.410] Just note that I'm pretty unlikely to give you an extension
[00:14:49.410 - 00:14:56.100] for your group assignment, the sustainability assignment later on.
[00:14:56.100 - 00:15:00.020] OK, yeah, so special considerations.
[00:15:00.020 - 00:15:06.860] So, yeah, if you can't sit, test or an exam, say if you're sick on the day,
[00:15:06.860 - 00:15:11.380] you just need to apply to special consideration centrally.
[00:15:11.380 - 00:15:15.260] You've got a five-day time limit to do that, OK?
[00:15:15.260 - 00:15:23.180] So if you fail the whole course, we don't offer a reset by default, OK?
[00:15:23.180 - 00:15:27.900] So I know you probably experienced that, those of you who went through first year here,
[00:15:27.900 - 00:15:32.890] but we don't do that in our department.
[00:15:32.890 - 00:15:40.730] Cool, yeah, and Gen AI, you can use it for your assignments,
[00:15:40.730 - 00:15:45.050] just check the details, just the usual things,
[00:15:45.050 - 00:15:50.130] needing to declare it and so on, and away we go.
[00:15:50.130 - 00:15:56.570] I think, yeah, most people did a pretty decent job of the assignment last year.
[00:15:56.570 - 00:16:01.890] And, yeah, some people used AI, didn't really improve things.
[00:16:01.890 - 00:16:10.940] OK, all right, we also have a hurdle requirement for the test and the exam.
[00:16:10.940 - 00:16:16.820] So basically what this means is that you've got to achieve at least 40%
[00:16:16.820 - 00:16:24.380] averaged across these two assessment in order for you to get at least a pass in 301.
[00:16:24.380 - 00:16:31.060] OK, so we're introducing that as a new requirement this year.
[00:16:31.060 - 00:16:34.820] So, yeah, just be wary of that.
[00:16:34.820 - 00:16:41.260] Cool, so I live up in the top of the link building in A506.
[00:16:41.260 - 00:16:47.100] I think online I'm still in A507, but wander around and you'll find me eventually.
[00:16:47.100 - 00:16:51.540] If you want, you can make an appointment to see me via Learn.
[00:16:51.540 - 00:16:54.980] So under Learn you'll find a little booking link,
[00:16:54.980 - 00:17:04.420] and you can come and make it time to see me either from Monday 9 to 9.45 or Tuesday at the same time.
[00:17:04.420 - 00:17:14.060] If that doesn't work for you, just let me know and I'll make it time to catch you some other time.
[00:17:14.060 - 00:17:21.460] Cool, if you have any questions, it's best to actually post that on the forum rather than emailing me.
[00:17:21.460 - 00:17:27.660] That way, if you've got a question, there's a very good chance that someone else in the course has a question as well.
[00:17:27.660 - 00:17:33.180] There's I think 275 of you, so it's a pretty chunky course.
[00:17:33.180 - 00:17:37.780] And it's just easier to post your questions on there.
[00:17:37.780 - 00:17:43.100] Generally, if I do have questions coming in via my email, I'll reply to it,
[00:17:43.100 - 00:17:49.660] but I'll also post that question and answer up on to Learn as well.
[00:17:49.660 - 00:17:51.980] There's my email address.
[00:17:51.980 - 00:17:59.300] I'm not always in my office just because with being a head of department, I've got meetings all the time.
[00:17:59.300 - 00:18:06.140] So yeah, just do feel free to send me an email to come and see me.
[00:18:06.140 - 00:18:09.660] We've got a number of guest lecturers this semester, too.
[00:18:09.660 - 00:18:18.180] So Matt Barber from Law, he's going to take you for two lectures on Law in New Zealand.
[00:18:18.180 - 00:18:28.220] And Virginia Nichols, who's a graduate of our department, she's going to be the lecturer for intellectual property.
[00:18:28.220 - 00:18:41.610] If you do have any questions about that content, it's best to ask me rather than those two lecturers.
[00:18:41.610 - 00:18:49.810] Cool, on top of those folk and me, you've also got a really awesome bunch of tutors.
[00:18:49.810 - 00:18:57.650] So you've got Cam, Chris, Felix, Gabriella and Hannah helping out in the drawing rooms.
[00:18:57.650 - 00:19:07.850] And then Gabby and Car, who are in the smaller E12 room for the tutorial A slots.
[00:19:07.850 - 00:19:15.130] Gabby's not here tomorrow, so I'm going to step in just as a back-filling Gabby in that tutorial slot tomorrow.
[00:19:15.130 - 00:19:18.090] So if you see me, don't panic.
[00:19:18.730 - 00:19:26.970] Yeah, so everyone has taken or tutored this course before.
[00:19:26.970 - 00:19:34.310] So there are really a good bunch of people, and hopefully you know a few of them.
[00:19:34.310 - 00:19:42.590] And then for your bicultural incompetence and confidence workshops, you'll have a different tutor.
[00:19:42.590 - 00:19:51.390] So some of you might get lucky and have Gabby and Car, who is the tutor for both.
[00:19:51.390 - 00:19:59.390] But yeah, just be wary that week two and three, you'll have a different tutor, but also you're in a different room.
[00:19:59.390 - 00:20:03.390] So just keep an eye on that timetable.
[00:20:03.390 - 00:20:13.620] Just a reminder, too, you only need to book yourself into one of those slots, B1 through to B14.
[00:20:13.620 - 00:20:16.740] Cool. So feedback from last year.
[00:20:16.740 - 00:20:27.260] So look, I take course evaluations really seriously, and I put a lot of effort in to really continually improve the course.
[00:20:27.260 - 00:20:34.020] So I've been working on the changes from last year since about February.
[00:20:34.020 - 00:20:37.740] So hopefully things keep improving.
[00:20:37.740 - 00:20:46.540] But so the positive feedback from last year is that everyone thought that the teaching team was really helpful and responsive.
[00:20:46.540 - 00:20:51.380] Last year was the first time I tried or introduced tutorials and workshops.
[00:20:51.380 - 00:20:54.660] And most people said that actually worked really well.
[00:20:54.660 - 00:20:57.460] Overall, the workload felt about right.
[00:20:57.460 - 00:21:05.180] And people said that they were pleasantly surprised that the course was decent because they heard otherwise.
[00:21:05.180 - 00:21:09.300] So that's a good thing.
[00:21:09.300 - 00:21:16.820] The bad case, so I got some pretty strong criticism about the sustainability assignment that it was confusing.
[00:21:16.820 - 00:21:25.460] There wasn't enough guidance in the in the tutorials on that learn was really tricky to navigate.
[00:21:25.460 - 00:21:33.140] And the assignment was causing some workload problems at the end of the semester.
[00:21:33.140 - 00:21:34.580] And the test was too easy.
[00:21:34.580 - 00:21:40.740] So yeah, the test last year, like I think the average grade was like 80 percent.
[00:21:40.740 - 00:21:44.300] It's like I completely undercooked it.
[00:21:44.300 - 00:21:57.700] So yes, this year I'm going to make the assignment clearer and I'm going to bring in more support into the tutorials.
[00:21:57.700 - 00:22:05.500] I've reorganized learn and helps remove some of the jargon and the funny wording that is in there.
[00:22:05.500 - 00:22:17.780] If you do have any comments about how you're finding learn either easy or difficult to navigate, please let me know so I can help.
[00:22:17.780 - 00:22:23.820] Yes, so to give you an idea, one of the things I did this year is on the learn home page,
[00:22:23.820 - 00:22:29.380] you can click on some hyperlinks that will bring you straight into the lecture content.
[00:22:29.380 - 00:22:36.020] So you're not having to sift around and find the different content.
[00:22:36.020 - 00:22:44.460] I'll be releasing the sustainability assignment earlier this year and providing more support in the tutorials for that.
[00:22:44.460 - 00:22:47.820] And I'm going to make the test more difficult.
[00:22:47.820 - 00:22:49.980] So that's what's changing.
[00:22:49.980 - 00:22:58.260] But, yeah, look, if you do have any other comments on how I can improve, please let me know throughout the semester.
[00:22:58.260 - 00:23:00.740] OK, overview of what we're going to do then.
[00:23:00.740 - 00:23:07.380] So, yeah, today doing engineering practice introduction and a bit of ethics.
[00:23:07.380 - 00:23:10.300] Next week we'll do collaboration and teamwork.
[00:23:10.300 - 00:23:21.060] And then on the right hand side, the tutorials are usually timed in a way to reinforce the prior week's content or the content that's happening that week.
[00:23:21.060 - 00:23:27.820] So you've got many perspectives in engineering next week as a guest lecturer, which will be cool.
[00:23:27.820 - 00:23:35.900] Bias diversity and ethics, IP lectures, law in week four, data privacy and data ethics.
[00:23:35.900 - 00:23:47.140] And then we start to move into more of the business side of things, get into some sustainability before the semester break.
[00:23:47.140 - 00:23:52.540] And we come back, polish off some stuff on sustainability.
[00:23:52.540 - 00:23:55.980] And then we start looking at people's favorite content.
[00:23:55.980 - 00:23:58.620] And that's money.
[00:23:58.620 - 00:24:05.860] OK, so net present value techniques, cost accounting, financial reporting and accounting.
[00:24:05.860 - 00:24:08.860] I will try to make that as exciting as possible.
[00:24:08.860 - 00:24:14.740] OK, but it's kind of tricky to make it exciting.
[00:24:14.740 - 00:24:20.020] I'm thinking about hot chocolate and maybe in the corner there.
[00:24:20.020 - 00:24:26.060] OK, then finishing off with some project management, risk management, how do you make integrated decisions?
[00:24:26.060 - 00:24:33.820] And then we've got a really awesome guest lecturer at the end, Michael Rick's going to come in from Fisher and Paykel Technologies.
[00:24:33.820 - 00:24:36.340] I think they've actually just changed names.
[00:24:36.340 - 00:24:46.540] He's a graduate of Tripoli Engineering, but he spans basically all of the disciplines that are within this room.
[00:24:46.540 - 00:24:54.300] And he's got an amazing career and he's shed some light about how all of this stuff is actually really important.
[00:24:54.300 - 00:24:59.550] And then we wrap things up at the end.
[00:24:59.550 - 00:25:06.190] OK, so on to the first week's content on ethics.
[00:25:06.190 - 00:25:10.030] Just checking though, can you all get this all learn?
[00:25:10.030 - 00:25:12.230] Cool, because last year it didn't happen.
[00:25:12.230 - 00:25:14.190] Something was a bug.
[00:25:14.190 - 00:25:22.110] OK, so this is largely a revision of the ethics module that happened in Eng 101.
[00:25:22.110 - 00:25:25.710] For those of you who went through first year here.
[00:25:25.710 - 00:25:34.550] But what I'll do today is I'll quickly recap on some of the really important things that comes out of the Eng 101 module.
[00:25:34.550 - 00:25:41.230] And that's really going to help us with next week and the weeks after.
[00:25:41.230 - 00:26:03.910] OK, so this relates to the following outcomes is for you to apply ethical principles within engineering context and recognize social and cultural factors which affect ethics as well as evaluating the viability of different engineering projects.
[00:26:03.910 - 00:26:06.990] Now, there was a slide I included last year.
[00:26:06.990 - 00:26:10.830] I didn't include it this year, but I'll talk about it.
[00:26:10.830 - 00:26:23.350] There was a graduate from AUT who got done for corruption fraud very, very recently.
[00:26:23.350 - 00:26:26.230] I think it happened in 2024.
[00:26:26.230 - 00:26:40.310] I actually found the academic record of this graduate and identified that they actually did a course very, very similar to this one.
[00:26:41.270 - 00:26:45.310] So they did a third or fourth year ethics module.
[00:26:45.310 - 00:26:48.660] It didn't help.
[00:26:48.660 - 00:26:55.220] So there is a bit of a debate about whether or not ethics can be taught.
[00:26:55.220 - 00:27:05.740] So didn't do that guy any good, but hopefully it will open your eyes to make you a better engineer.
[00:27:05.740 - 00:27:08.780] So engineers need to do the right thing.
[00:27:08.780 - 00:27:14.500] And the reason being is that the work that we do affects all New Zealanders every day.
[00:27:14.500 - 00:27:21.380] And we create the foundation for New Zealand's social, environmental and economic fabric.
[00:27:21.380 - 00:27:27.180] The economic contribution for engineers in New Zealand is massive.
[00:27:27.180 - 00:27:32.700] So, yeah, have a look at the world around you.
[00:27:32.700 - 00:27:38.900] It's been shaped rightly or wrongly by engineers.
[00:27:38.900 - 00:27:45.420] OK, so this is a recreation of the THERAC-25's malfunction 54 era,
[00:27:45.420 - 00:27:52.100] which was directly involved in the deaths of two cancer patients in Tyler, Texas.
[00:27:52.100 - 00:28:04.780] The THERAC-25 is a computer controlled radiation therapy machine produced by then the Atomic Energy Council of Canada in 1982.
[00:28:04.780 - 00:28:12.460] So because of concurrent programming errors, known as race conditions, which you probably studied,
[00:28:12.460 - 00:28:23.980] it gave some patients radiation doses that were hundreds of times greater than normal resulting in death or serious injury.
[00:28:23.980 - 00:28:31.180] In 2018 and 2019, Boeing's poor mechanical system and software design caused two crashes,
[00:28:31.180 - 00:28:35.420] one in Indonesia and the other in Egypt.
[00:28:35.420 - 00:28:42.980] Three hundred and forty six people died. OK, Boeing blamed the pilots.
[00:28:42.980 - 00:28:48.660] The poor designs, though, were eventually attributed to poor corporate culture,
[00:28:48.660 - 00:28:55.820] which prioritized returning profits to shareholders rather than designing things to be safe.
[00:28:55.820 - 00:29:01.940] So some really good docos. If you want to look those up, I'm pretty sure there was one on Netflix.
[00:29:01.940 - 00:29:11.140] I don't know if it's on there anymore, but yeah, pretty, pretty fascinating case studies on on engineering failures.
[00:29:11.140 - 00:29:21.100] OK, so ethics is the study of moral principles comes from the Greek ethos,
[00:29:21.100 - 00:29:26.180] which means, you know, someone's character or personal disposition.
[00:29:26.180 - 00:29:49.500] It's about what people ought to do or should do or what character or traits a person should have and what values and morals a person ought to adopt.
[00:29:49.500 - 00:29:54.140] OK, but yes, there's a subtle difference between ethics and the law, though.
[00:29:54.140 - 00:30:10.100] So ethics is what a person ought to do and law is what a person is required to do by the state and law establishes a minimum standard of conduct.
[00:30:10.100 - 00:30:20.580] And sometimes that can actually be expanded to include the expectations of professional societies like engineering New Zealand.
[00:30:20.580 - 00:30:28.660] So just because something is ethical doesn't necessarily mean it's legal and vice versa.
[00:30:28.660 - 00:30:33.100] So you can be breaking the law and also be ethical.
[00:30:33.100 - 00:30:36.780] You can be ethical and potentially breaking the law.
[00:30:36.780 - 00:30:44.660] So, yeah, there's two don't always perfectly overlap.
[00:30:44.660 - 00:30:57.980] But the goal in engineering is to understand ethical theories and apply them to make really solid sound decisions.
[00:30:57.980 - 00:31:02.260] Speaking from experience, this is all good in theory.
[00:31:02.260 - 00:31:13.300] But in reality, as an engineer, particularly as a graduate engineer, you're going to find yourselves at times put in a really awkward position where,
[00:31:13.300 - 00:31:18.780] you know, you don't have time to necessarily apply all of these ethical principles.
[00:31:18.780 - 00:31:22.020] You'll put all the spot to make a decision.
[00:31:22.020 - 00:31:25.380] And it can be really, really hard.
[00:31:25.380 - 00:31:27.940] And sometimes you get it wrong and that's OK.
[00:31:27.940 - 00:31:30.540] OK, we just need to learn from that.
[00:31:30.540 - 00:31:36.260] So a few examples from my own experience.
[00:31:36.260 - 00:31:56.940] So I was working as a process engineer and we had a technician come into the control room and the technician needed to calibrate some some gas lines to make sure that they're detecting impurities in the gas.
[00:31:56.940 - 00:32:08.260] And the technician needed to drop high pressure gas, you know, it's probably at 50 or 60 bar down to atmospheric pressure to make this thing work.
[00:32:08.260 - 00:32:11.900] And he needed a pressure regulator to do that.
[00:32:11.900 - 00:32:14.940] So went in to see my boss.
[00:32:14.940 - 00:32:17.620] Boss gave him the pressure regulator.
[00:32:17.620 - 00:32:22.140] He looked at it and went, no, this isn't going to do the job because it's going to go.
[00:32:22.140 - 00:32:24.100] That's medium pressure to low.
[00:32:24.100 - 00:32:25.460] I need high to low.
[00:32:25.540 - 00:32:27.820] It wasn't really rated for it.
[00:32:27.820 - 00:32:37.020] Anyway, my boss assured the guy, the technician, that everything was going to be OK.
[00:32:37.020 - 00:32:41.180] So I'm just working away and I hear a bang and then I turn around.
[00:32:41.180 - 00:32:45.220] This guy's holding his his wrist and hand.
[00:32:45.220 - 00:32:49.620] The pressure regulator blew up in his hand.
[00:32:49.620 - 00:32:54.100] Then my boss came over a few hours after the incident.
[00:32:54.100 - 00:33:00.380] He was fine. He didn't lose a hand, just sprayed it pretty badly.
[00:33:00.380 - 00:33:11.160] My boss came over with the broken bits of pressure regulator and he gave them to me and he said, get rid of these.
[00:33:11.160 - 00:33:16.080] I was two weeks into the job.
[00:33:16.080 - 00:33:21.460] What did I do?
[00:33:21.460 - 00:33:27.100] I'm on probation too, so they can sack me any minute.
[00:33:27.100 - 00:33:33.460] Any guesses?
[00:33:33.460 - 00:33:36.140] Yeah, I chucked him in the bin.
[00:33:36.220 - 00:33:46.220] But then I sneakily pushed the bin away to make sure that the cleaners who used to come around at seven in the morning,
[00:33:46.220 - 00:33:50.980] I was working on night shifts, they didn't actually get access to it.
[00:33:50.980 - 00:33:55.620] And then the boss's boss turned up and said, where is it?
[00:33:55.620 - 00:33:57.260] I went, here it is.
[00:33:57.260 - 00:34:00.020] And he goes, did he ask you to get rid of that?
[00:34:00.020 - 00:34:00.700] I went, yep.
[00:34:00.700 - 00:34:05.500] Yeah, so it happens.
[00:34:05.500 - 00:34:12.740] Another interesting one was later on when I was working as a materials engineering consultant.
[00:34:12.740 - 00:34:22.620] We hired this mechanical engineer, looked amazing on paper, said that he was able to use ultrasonic inspection equipment.
[00:34:22.620 - 00:34:28.500] So you can scan a little bit of ultrasonic probe onto a bit of metal and you can detect that cracks are.
[00:34:29.180 - 00:34:32.540] He said that he was really proficient in this.
[00:34:32.540 - 00:34:43.580] And so we sent him out onto a site and with some of the other technicians, one of whom used to work for the Air Force.
[00:34:43.580 - 00:34:46.900] So the guy worked for the Air Force, knew his stuff.
[00:34:46.900 - 00:34:54.660] Anyway, technician hands the engineer the equipment and he doesn't know how to operate it.
[00:34:54.660 - 00:34:59.100] The engineer had no idea.
[00:34:59.100 - 00:35:06.020] And so the technician starts to go, is this guy actually legitimate?
[00:35:06.020 - 00:35:07.220] Is he an engineer?
[00:35:07.220 - 00:35:13.580] So he reports back to me saying, oh, I've got this concern.
[00:35:13.580 - 00:35:22.260] And then I recalled a meeting the week before when I was going through some very basic,
[00:35:22.260 - 00:35:29.460] for those of you who've done mechanical design, stress strain codes, this guy had no idea what I was talking about.
[00:35:29.460 - 00:35:35.500] I was like, mechanical engineer of 30 years experience should actually know this.
[00:35:35.500 - 00:35:38.140] Anyway, he went to my boss.
[00:35:38.140 - 00:35:46.500] Boss calls up this guy's university, not an engineer.
[00:35:46.500 - 00:35:50.100] Yes, he got sacked on the spot.
[00:35:50.100 - 00:35:55.460] Yeah, and then we managed to get him blacklisted on Engineers Australia.
[00:35:55.460 - 00:35:57.940] Do not employ these people.
[00:35:57.940 - 00:36:02.340] Register and think you got kicked out of the country, too.
[00:36:02.340 - 00:36:06.620] Yeah, so yeah, so yeah, all good in theory, right?
[00:36:06.620 - 00:36:10.140] OK.
[00:36:10.140 - 00:36:10.420] Cool.
[00:36:10.420 - 00:36:15.740] So the three main ethical theories that we talk about in Angie 101 in this course are rules based thinking.
[00:36:15.740 - 00:36:25.940] So do the right thing or deontology, ends based thinking or to get the best outcome, consequentialism.
[00:36:25.940 - 00:36:31.340] Hopefully this is starting to trigger some good memories of Angie 101.
[00:36:31.340 - 00:36:37.260] And then virtues based thinking, which is what it means to be a good person or virtue ethics.
[00:36:37.260 - 00:36:45.660] So later on, I'd like you to go away and actually look at the revision videos that I've posted on the 301 site.
[00:36:46.020 - 00:36:51.220] Just so you can remember what all of these theories are about.
[00:36:51.220 - 00:36:54.860] OK, so deontology.
[00:36:54.860 - 00:36:58.460] The main thing about rules based thinking is that there are no clear rules.
[00:36:58.460 - 00:37:01.140] In fact, rules change over time.
[00:37:01.140 - 00:37:05.940] Rules shift with culture and law and the rest of it.
[00:37:05.940 - 00:37:12.660] But yes, some of the simplest rules that we should all do is obviously to follow the law.
[00:37:12.660 - 00:37:15.060] And it is the most basic thing that we need to do.
[00:37:15.060 - 00:37:19.500] But generally speaking, we all do that anyway.
[00:37:19.500 - 00:37:28.300] Another commonly accepted rule in society is that you should treat others based on how you want to be treated yourself.
[00:37:28.300 - 00:37:33.980] And that's often termed the golden rule.
[00:37:33.980 - 00:37:43.780] And for professionals, if you're signed up to a professional society like IEEE, ACM,
[00:37:43.780 - 00:37:49.260] Engineering New Zealand, you are expected to follow a code of conduct.
[00:37:49.260 - 00:37:52.420] So that becomes part of your rules.
[00:37:52.420 - 00:37:58.500] Likewise, if you're within a company, you'll be expected to follow their rules.
[00:37:58.500 - 00:38:07.260] So as an example here at UC, as a student, you're expected to follow the student code of conduct,
[00:38:07.260 - 00:38:12.960] along with all of the different policies and procedures that we've got here.
[00:38:12.960 - 00:38:24.120] OK, another fundamental rule is that people have fundamental rights to duty and respect.
[00:38:24.120 - 00:38:33.300] In fact, in New Zealand, we've actually got a Bill of Rights, which entrenches some of these expectations in there.
[00:38:33.300 - 00:38:39.500] OK, yes, so the golden rule, just a little bit more about that.
[00:38:39.500 - 00:38:49.900] It's really quite interesting is that the golden rule actually spans lots of different cultures.
[00:38:49.900 - 00:38:55.180] So it's in lots of different religious texts as well.
[00:38:55.180 - 00:39:06.100] But the problem with that is that it assumes that what we need is the same as whatever one else wants and needs.
[00:39:06.100 - 00:39:15.780] So for example, I might wish to be treated in a certain way, but you might not want to be treated in that same way.
[00:39:15.780 - 00:39:26.850] And because of this, you need to sort of step out of your own worldview and look back the other way to try and get an understanding of what other people want.
[00:39:26.850 - 00:39:35.170] OK, the other problem with the golden rule is that it doesn't allow you to distinguish between people's different needs.
[00:39:35.170 - 00:39:41.580] And so it doesn't give you a way of managing that conflict.
[00:39:41.580 - 00:39:47.780] So a better way to phrase the golden rule might be to say that you should treat people the way you wish to be treated.
[00:39:47.780 - 00:39:59.740] So in order to do that, this requires us to understand what people want and need to treat them accordingly rather than based on our own preferences.
[00:39:59.740 - 00:40:03.860] So cool.
[00:40:03.860 - 00:40:07.740] The next theory then is consequentialism.
[00:40:07.740 - 00:40:16.220] So this is where you look at competing actions according to what the outcome is.
[00:40:16.220 - 00:40:22.820] So you might recall the trolley problem, OK, from Eng 101 where you've got, you know,
[00:40:22.820 - 00:40:29.700] a train fiddling down some tracks and you've got a switch that can either, you know,
[00:40:29.700 - 00:40:34.380] save one person or kill, you know, five others.
[00:40:34.380 - 00:40:36.660] Do you save yourself and this sort of thing?
[00:40:36.660 - 00:40:39.620] That's kind of the idea of consequentialism.
[00:40:39.620 - 00:40:42.700] So, yeah, the ends justify the means.
[00:40:42.700 - 00:40:52.580] A particular subset of consequentialism is utilitarianism, and that's where acts seem to be ethical.
[00:40:52.580 - 00:40:57.060] When they achieve the greatest good for the greatest number of people.
[00:40:57.060 - 00:41:06.540] So Ford classically applied this during the Pinto fiasco of the 70s.
[00:41:06.540 - 00:41:22.100] You might recall this scenario, but basically if the Pinto was rear-ended, the fuel tank would rupture, spilling vapor and fuel everywhere and causing pretty horrific fires.
[00:41:22.100 - 00:41:27.300] So, yeah, lots of people died, lots of people were maimed in the rest of it.
[00:41:27.300 - 00:41:40.540] Ford actually calculated that it was easier and cheaper to pay people out for dying or being injured than to replace all of the faulty Pintos or to fix them up.
[00:41:40.540 - 00:41:51.940] OK, and they got away with it, OK, for a few years before finally they realized the errors in their way and started to retrofit the Pintos correctly.
[00:41:55.220 - 00:41:59.820] OK, so then you've got virtues-based thinking.
[00:41:59.820 - 00:42:09.660] So this is where, yeah, a virtuous person, what would a good or a virtuous person do in those circumstances?
[00:42:09.660 - 00:42:15.540] And then there's all sorts of traits that you need to think about with what a virtuous person would be.
[00:42:15.540 - 00:42:24.380] So there'd be honest, courageous, compassionate, self-regarding, generous and so on.
[00:42:24.380 - 00:42:31.140] OK, that's all good in theory. But how do you actually apply this in practice?
[00:42:31.140 - 00:42:39.340] So there is a systematic decision making process that you can revise yourself on. It's like the eight step process.
[00:42:39.340 - 00:42:43.580] Yeah, we're not going to test or examine that this year.
[00:42:43.580 - 00:42:48.490] But just again, you might want to familiarize yourself with it.
[00:42:48.490 - 00:42:53.610] OK, so how do you actually apply these theories in practice?
[00:42:53.610 - 00:43:01.290] You don't have to align yourself to any one of those particular ethical theories.
[00:43:01.290 - 00:43:10.930] Yeah, you don't need to be a strict deontologist or a teleologist, but you can do something that's called rule consequentialism.
[00:43:10.930 - 00:43:22.370] So you can say follow the rules. But if there is a conflict, choose the outcome that's got the best consequences or least impact.
[00:43:22.450 - 00:43:33.290] In reality, engineers typically apply blended ethical theories through their codes of conduct.
[00:43:33.290 - 00:43:41.010] So I'll just show you the Engineering New Zealand one of a very brief version of that now.
[00:43:41.010 - 00:43:51.090] But it is designed to make sure that you make appropriate ethical decisions within those eight different points.
[00:43:51.090 - 00:43:59.330] So these are not rules. OK, so just be careful of that. They're not rules. They're just eight points.
[00:43:59.330 - 00:44:07.410] Within that, you have different ethical theories embedded within the code of conduct.
[00:44:07.410 - 00:44:16.210] OK, so for example, protecting health and safety of people.
[00:44:16.210 - 00:44:36.500] What ethical theory do you think that aligns with? Virtues? Why virtues? Yeah, a good person would be protecting other people.
[00:44:36.500 - 00:44:47.700] Yeah, it's also rules based. Why? There's health and safety legislation. Yeah, cool. What else?
[00:44:47.700 - 00:44:53.740] Consequentialism? Little bit in there, too, is that you want to try and protect people so they don't get hurt later on.
[00:44:53.740 - 00:45:01.660] Yep. OK, so occasionally you're going to have one clause that actually touches on multiple ethical theories.
[00:45:01.660 - 00:45:16.940] Act competently. What do you reckon? Probably virtues based. Yeah, that's right. OK, so they do integrate different ethical theories.
[00:45:16.940 - 00:45:28.380] OK, so engineering designs are a result of a series of choices and those choices are actually affected by your values.
[00:45:28.380 - 00:45:43.420] You might not be completely aware of it, but it does happen. And engineering designs are never ethically neutral because they are influenced by your values.
[00:45:43.420 - 00:45:55.860] I've got a link there, too, if you want to check that out later. It's a really interesting paper about written by an academic about how we actually teach engineering ethics.
[00:45:55.860 - 00:46:05.060] Are we actually doing the right thing? A bit meta, but it's pretty interesting. Just a couple of minutes left.
[00:46:05.060 - 00:46:15.020] So preparations for the for the rest of this week. So under the introduction to engineering practice and ethics section, again,
[00:46:15.020 - 00:46:24.620] just a reminder to watch those ethical recap videos from from one and also review the workshop material.
[00:46:24.620 - 00:46:28.900] So you can scroll down, check out the workshop material in particular.
[00:46:28.900 - 00:46:43.860] I want you to have a look at the IEEE code of conduct. So in the workshop, you'll have a little exercise to work through where you're going to be comparing the IEEE code of conduct with a whole bunch of other ones.
[00:46:43.860 - 00:46:56.940] And then before Friday, I want you to listen to a podcast. It takes about an hour or 45 minutes if you speed it up.
[00:46:56.940 - 00:47:04.860] But it's all about collaboration and teamwork in engineering. Yeah, hyperlinks are up on learn.
[00:47:04.860 - 00:47:14.540] So Apple and Spotify. I'm pretty sure it's free. Cool. So what's next? Collaboration and teamwork on Friday.
[00:47:14.540 - 00:47:22.660] But yet you've got your ethics workshops tomorrow. Any questions before we wrap up?
[00:47:22.660 - 00:47:26.500] Awesome. Okay. See you tomorrow or Friday.
[00:48:23.540 - 00:48:31.060] Yeah. Thank you.
[00:49:26.300 - 00:50:05.380] I don't know.
[00:50:05.380 - 00:54:30.660] Downloaded them. All good. Yeah. And the handout. Thank you. Nice to see you.

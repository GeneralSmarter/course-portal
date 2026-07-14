# ENMT301-26W Lecture 04 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_04_audio_16k_mono_32k.mp3`
Source audio SHA-256: `5307ed159c9e8514c4f2c0ea3fdc14121df14772ff265b339bbef2853988b6b5`
Generated: 2026-06-06T04:57:42.317164+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:05 - 00:00:20] Okay, Kiloco time. Well, good afternoon. We'll make a start. So, well, welcome back to the Megatronics
[00:00:21 - 00:00:29] program. I know you've had three and a half four days of lectures already, but this is, I guess, the first one
[00:00:29 - 00:00:33] sort of just as Megatronics. You've already had a lecture for this class, I think with George,
[00:00:34 - 00:00:41] was it yesterday or Tuesday? But you're also going to have two lectures a week with me, so
[00:00:41 - 00:00:48] that's down Friday for this term. So, if you don't really know who I am, I'm Chris Priti. I am one of the
[00:00:48 - 00:00:55] co-directors of the Megatronics Engineering program along with Michael Hayes. So, I set in the
[00:00:55 - 00:00:59] mechanical engineering department, Michael sets in the electrical engineering department.
[00:01:00 - 00:01:05] But I also have a course coordinator for this course, and I'm also your third year coordinator,
[00:01:05 - 00:01:13] so it's busy time at the moment. But if you need to get in touch with me, you can either email me
[00:01:13 - 00:01:20] this often the best bit. Otherwise, my room is offices if I've won three sets on the fifth floor
[00:01:20 - 00:01:27] of the mechanical silver building. So, you know, come and knock on the door if I'm in, I can often
[00:01:28 - 00:01:35] help. But also, yeah, a lecture that's a course in sort of the design side of things for it.
[00:01:36 - 00:01:44] Here's my background as I came through my undergrad here at Henry in the late 90s and the early
[00:01:44 - 00:01:49] northeast. During mechanical engineering, because Megatronics wasn't a thing, but the Megatronics
[00:01:49 - 00:01:55] program started in 2004, and I finished a couple years before that. But I was always,
[00:01:56 - 00:02:00] I suppose on the Megatronics, I chose mechanical, but I was tossing up between mechanical and
[00:02:00 - 00:02:06] electrical. Back then, electrical was the biggest program in the college engineering,
[00:02:06 - 00:02:13] faculty of engineering. But you end up doing mechanical, but doing the Megatronics,
[00:02:13 - 00:02:20] he betts of mechanical light controls and stuff, which was an elective. But also,
[00:02:20 - 00:02:25] there was some feedback, some embedded systems and stuff, and mechanical that's one.
[00:02:25 - 00:02:32] But then also did a master straight after that with Jeff Chase. He just started then. And that was
[00:02:32 - 00:02:41] ended up being a lot of a syndicate programming of a digital DSP check for video processing
[00:02:41 - 00:02:47] back when cell phones were just starting to implement video and they needed a really compressed
[00:02:47 - 00:02:53] form of impact for transmitting video. So I guess that sort of sent me off down the,
[00:02:54 - 00:02:59] some more Megatronics, these other things as well. But after that, I went and worked for Becca
[00:02:59 - 00:03:05] and Wellington, and so for Becca, I worked in the industrial section back then doing mostly
[00:03:05 - 00:03:11] transmission design and analysis with the jobs being for like trans carats and stuff like that.
[00:03:12 - 00:03:20] And then after that, and doing a similar role at National Grid in the UK. But it was related to
[00:03:20 - 00:03:25] power, but it was very much, I guess, it was kind of interesting, somewhat fine, a lot more
[00:03:25 - 00:03:30] than of power lines and how they say more when they heat up, when you're putting more current
[00:03:31 - 00:03:36] what you have to do. So New Zealand transmission lines have also transmission lines,
[00:03:36 - 00:03:40] it always designed to run at 50 degrees Celsius as the maximum operating temperature. But
[00:03:40 - 00:03:44] trans power wanted to put a bunch more current through them because they're on lots of build more
[00:03:44 - 00:03:49] transmission lines. And so we had to do a lot of work, especially at Becca, around what modifications
[00:03:49 - 00:03:54] I have to make to those to run them at 90 degrees. And obviously you get a lot more than when
[00:03:54 - 00:04:00] you're running at 90 degrees, the conduct is explained and if we get more sag and therefore it's
[00:04:00 - 00:04:03] closer to the ground and then your stuff and financial statutory experiences and stuff like that.
[00:04:04 - 00:04:13] So that was interesting. Now to the PhD and Biomedical through the area and a postdoc in Belgium
[00:04:13 - 00:04:17] before I came back here. So you have been teaching me electronics here for
[00:04:19 - 00:04:26] since 2013, it's quite a long time now. But yeah, so I've also ended up, I mean I teach, I teach
[00:04:26 - 00:04:29] three, one, three for the mechanical students. So that's like the electrical paper they take,
[00:04:29 - 00:04:35] so you've probably got friends taking that. I also teach half of the robotics courses in elective
[00:04:35 - 00:04:42] and fourth year Michael Hayes teaches L a half of that and I teach this, which is interesting
[00:04:42 - 00:04:49] because this one was the worst my shit subject at year. There's an undergrad here I am. So maybe I can
[00:04:49 - 00:04:57] impart some useful knowledge, things not to do. But yeah, so that's about me. A little bit about
[00:04:57 - 00:05:03] this course so that you've got a general gist of how it works. It's a bit of a funny one because
[00:05:03 - 00:05:10] it's a whole year course and there aren't many of those anymore. And up until 2020 I teach some
[00:05:10 - 00:05:15] of this material we have one lecture with me through terms one and two and then Michael Hayes
[00:05:15 - 00:05:20] at that time we'll teach the second part and he would do that in some history. But that was the
[00:05:20 - 00:05:24] year COVID came along and we're all scaring and trying to figure out what we're going to do.
[00:05:25 - 00:05:31] And so we didn't think we'd necessarily have access to the labs. We could kind of do lectures
[00:05:32 - 00:05:39] through remote sort of ways. And so we kind of crammed all of the course content into the lecture
[00:05:39 - 00:05:46] material into semester one. And then at that time we were hoping that hell that we could get back
[00:05:46 - 00:05:50] into the labs because Robocut was going to be a bit of a show if you couldn't actually come into
[00:05:50 - 00:05:55] the labs and build anything. Fortunately you couldn't, the second half of the year. But what it taught
[00:05:55 - 00:06:00] us was that that way of running the course was actually better for US students because you'd learned
[00:06:01 - 00:06:05] and a lot of that stuff that you get in the second term. So the sensors and signal processing,
[00:06:05 - 00:06:11] which is now thought by Richard Clear, that's really useful for your Robocut because you're looking
[00:06:11 - 00:06:15] at filtering signals and you're getting noisy signals from the IR sensors and from the range
[00:06:15 - 00:06:19] sensors and all this sort of stuff and you have to process that so that you can use it. And having
[00:06:19 - 00:06:26] that taught early made it a lot better for you and doing the Robocut. So we've subsequently
[00:06:26 - 00:06:31] stuck with that. But what that means and you might have noticed this on your time tables if you've
[00:06:31 - 00:06:37] looked that far ahead as there are no lectures in semester two. So you're quite heavily front-loaded
[00:06:37 - 00:06:43] with lectures for this course in semester one. So you've got a lecture a week with George
[00:06:44 - 00:06:49] and the mechanical students and that's kind of the mechanical design aspects. You have in term
[00:06:49 - 00:06:53] two, you have two lectures a week with me and that's kind of around the Megatron system design
[00:06:53 - 00:06:57] fundamentals. Some sort of system design tools a little bit about reliability,
[00:06:57 - 00:07:03] risk and sustainability. And then in term two, I stopped teaching and Richard teaches you and
[00:07:04 - 00:07:10] you have three lectures a week and that's cramming in the sensors and signal processing stuff.
[00:07:10 - 00:07:18] And the reason we also cram their answer here this course is it's a little bit of a work around
[00:07:18 - 00:07:23] and that gives you all the prerequisites if you want to do advanced signal processing is a 400
[00:07:23 - 00:07:31] level elective for E&L 420 course. Then you can do that. You're largely getting to what the same
[00:07:31 - 00:07:37] stuff that the electrical students get to and E&L 320. And it kind of fits under the idea of design
[00:07:37 - 00:07:43] because it's you know, signal processing stuff is a bit of a design tool with information about
[00:07:43 - 00:07:48] how some of the sensors you use in the Robocut work and bits and pieces in there. So it does set
[00:07:49 - 00:07:57] sits reasonably well. So all those lectures occur in semester one and semester two is pretty much
[00:07:57 - 00:08:03] just dedicated to the Robocut project. So you have to do some of the Robocut project initially in
[00:08:03 - 00:08:10] semester one like the first report, the conceptual designers. If you do, that leaves you that mid
[00:08:10 - 00:08:16] semester break to work on it. If you'd like, and I suggest you try and do some work on that
[00:08:16 - 00:08:21] during that period of time because you don't have any other courses due or running. And
[00:08:23 - 00:08:31] in that handy, I think Thursday's technology screw up day because this morning I had a lecture for
[00:08:31 - 00:08:39] 313 and I was 20 minutes into it and PowerPoint just went four. And then I double clicked to bring it
[00:08:39 - 00:08:43] back up and it just went to this window, it was much of a splash screen, nothing,
[00:08:44 - 00:08:50] killed in task manager, nothing had to restart. Eventually it came back and we've got a
[00:08:50 - 00:09:02] simple thing going on here. Although this time it's not PowerPoint, we'll see if I can get another
[00:09:03 - 00:09:35] we'll try this. See if USB-C works. Hurrah. And then now we have to, yes, we're working. And I don't
[00:09:36 - 00:09:40] okay so anyway what this means is that semester two is largely dedicated to the Robocut because
[00:09:40 - 00:09:45] there's a lot of the building occurs. So this is the one you get your kits, you figure out your
[00:09:45 - 00:09:50] teams, you do some concept design and then you start to build it but the vast bulk of the building
[00:09:50 - 00:09:56] occurs in semester two. Hopefully you spread that over semester two, you don't do what some groups do
[00:09:56 - 00:10:01] and kind of leave it all till the last week and try and make something work. That's not a good way
[00:10:01 - 00:10:08] of doing the project. Anyway so let's have this course of structured in terms of lectures and so on.
[00:10:08 - 00:10:16] There is one layer per week in semester one. During this first term of it, we'll use it occasionally
[00:10:16 - 00:10:25] for things like the induction that we used on yesterday with Julian and occasionally for other bits
[00:10:26 - 00:10:32] but largely unless I tell you don't bother going to the labs that are scheduled in your timetable
[00:10:32 - 00:10:39] during term one. I'll put notes out on learn about it when we use it. During term two we'll use
[00:10:39 - 00:10:43] those. I'll have TAs there during term two because you can start working on the Robocut and stuff like that.
[00:10:45 - 00:10:52] So there's more information about this on the course on learn, the notes and stuff. Some of you
[00:10:52 - 00:10:59] have already found if you look on the learn page under the Robocut section on the bar on the left,
[00:10:59 - 00:11:05] there's a survey for group formation and they'd ask some key questions that we used to
[00:11:05 - 00:11:11] put the groups together which are things like how much do you enjoy the mechanical aspect of
[00:11:11 - 00:11:16] design, the electrical aspect of design, the computer aspect of design, the technology experience
[00:11:16 - 00:11:23] you've got in terms of making or playing with robotics or hobbyist stuff and is there anyone in
[00:11:23 - 00:11:32] the class who you absolutely cannot work with in a group? If you fill that out and I think I've
[00:11:32 - 00:11:39] given you into the first of March to complete that then we pull that together and we roll the
[00:11:39 - 00:11:45] magic dice and put you into groups of three. So please get on to that if you haven't done so already.
[00:11:49 - 00:11:56] And yeah, that is as I think as I mentioned at the induction on Monday, that's largely random.
[00:11:57 - 00:12:04] We try to match what we try to do is ensure that each group has got somebody who likes the
[00:12:04 - 00:12:08] mechanical, the electrical, the computational parts, there's somewhat matched in terms of
[00:12:09 - 00:12:17] self-depressed experience and there's somewhat matched in sort of aggregate GPA from last year so
[00:12:17 - 00:12:28] that there's somewhat even across the class. And that's largely where to are. I will say you are
[00:12:28 - 00:12:38] likely there will be some groups who have issues and this seems unavoidable. Part of this is that
[00:12:38 - 00:12:44] you will start to learn how to work through those. Because of that, I organize some sessions,
[00:12:44 - 00:12:49] actually that brings us to this. I organize some sessions with Dominic from Academic Skills and
[00:12:49 - 00:12:55] there's a couple of sessions in there. One is around writing and it's really a reminder around
[00:12:56 - 00:13:00] things like structure and how you use paragraphs and sentences and to some extent it's pretty
[00:13:00 - 00:13:05] basic and to some extent AI helps you with these days. But it's good to have as a reminder
[00:13:05 - 00:13:14] and talking about writing in terms of engineering sort of a seems. Because one of the things
[00:13:14 - 00:13:21] I think people often don't appreciate is that as engineers, once you go out into the real world,
[00:13:21 - 00:13:25] you'll do a lot of writing. You'll be writing reports, you'll be writing emails, you'll be
[00:13:25 - 00:13:29] communicating. If you're doing a lot of communicating a lot of that has written communication.
[00:13:29 - 00:13:35] And so you need to do quite a bit of that and so we teach you a little bit of that and also
[00:13:35 - 00:13:42] have some assessment around report writing. But the other thing is in these sessions,
[00:13:43 - 00:13:45] or are they?
[00:13:47 - 00:13:59] I can't say the mouse. The Friday session in the last week of the term is team work competencies
[00:13:59 - 00:14:06] and so that's run again by Dominic and that has got it's kind of pre-loading you with some things
[00:14:06 - 00:14:14] to work on and do with your teams to ensure that they work as smoothly as they can do. Because
[00:14:14 - 00:14:21] there's a lot of things that cause teams to not work too well. And sometimes, you know,
[00:14:21 - 00:14:25] stuff that you don't think about it's what your values. One person might want to learn a lot
[00:14:25 - 00:14:30] and do in a project. One person might want to get a good mark by doing the minimum possible
[00:14:31 - 00:14:36] and one person might know what their values are. But when you've got these different values,
[00:14:36 - 00:14:40] they're kind of in-up clashing and it can make it hard. And so Dominic covers some
[00:14:41 - 00:14:49] tools that you can use in a team to kind of head these issues off. And you'll note there's a
[00:14:49 - 00:14:52] few guest lectures there. So there's guest lectures around, you know, the report writing, the
[00:14:52 - 00:14:58] team with competencies, also doing poems on life cycle analysis. I might do the folk tree one. I'll just
[00:14:58 - 00:15:06] see how that fits. But with these guest lectures, you have to turn up. So I'll send around all
[00:15:06 - 00:15:12] in the lectures. We'll just have a sign-up sheet so you can just sign that you turn up. And if you
[00:15:12 - 00:15:18] don't, there's the threat of a 5% penalty on your overall grade at the end. Because if I make it
[00:15:18 - 00:15:24] a positive thing like it's worth 5% turning up. And then for some reason, I can't get a guest
[00:15:24 - 00:15:28] lecture to come in and stuff like that. It kind of misses other. We're just having a negative
[00:15:28 - 00:15:36] assessment values. I don't have to put on the assessment schedule. And the other thing is,
[00:15:36 - 00:15:40] that's very embarrassing when you organize guest lectures and no one turns up. So we had that
[00:15:40 - 00:15:47] number of years ago, I had someone coming in from Hamilton, and I think there was a 361 test that day
[00:15:47 - 00:15:51] and two students turned up from the class. And so you get someone coming in from industry and two
[00:15:51 - 00:15:56] people turn up. It's not a good look and they don't really want to come back. And so these guest
[00:15:56 - 00:16:03] lectures have a requirement for turning up. And this you've got a good excuse, like your sec,
[00:16:04 - 00:16:08] that sort of thing. But if everyone emails me and tells me this sec, I don't believe that.
[00:16:09 - 00:16:20] But otherwise, all right. So this is available on the course schedule on the
[00:16:20 - 00:16:25] low-impact. And I've kind of color coded things. So you'll see the stuff and the red on the left
[00:16:25 - 00:16:33] of the lectures you attend with George with the mechanical students in A1. You can see my lectures
[00:16:33 - 00:16:48] are in blue. So what you can see is, let's see if I can, I think I can get a laser pointer somehow almost.
[00:16:49 - 00:17:09] Right, laser pointer. All right. Okay. So these two are the lectures those down Friday.
[00:17:10 - 00:17:17] What you'll see is there's lectures D&E, which don't start for a couple of weeks. And so we'll
[00:17:17 - 00:17:23] only use those when they're put in here. So I'll use them this week. We may use it this week,
[00:17:24 - 00:17:28] you know, if we do, we use it here because we've got some lectures. It's a little bit up and down.
[00:17:30 - 00:17:35] Then there's the lab slot for this course. I didn't fill in the fact that we used it this
[00:17:35 - 00:17:39] week for the induction. But in a couple of weeks time, we're going to use that for a multi-domain modeling
[00:17:39 - 00:17:47] tutorial which I'll go in the trial. Over here, we've got these are the tutorials again that
[00:17:47 - 00:17:53] relates to georgias material. So thank you for all guys. This is to the E&M E 301 page as well.
[00:17:53 - 00:17:58] So just be aware. Obviously this is the E&M T301. You have that learned page. You also have
[00:17:58 - 00:18:04] access to E&M E 301 where you'll find georgias notes and all the communications relating to the assignments
[00:18:04 - 00:18:10] for E&M E 301. So that's the aluminium beam assignment and the bearing assignment and stuff like that.
[00:18:10 - 00:18:16] So just make sure you're using the right one. And then in turn two, obviously you continue a
[00:18:16 - 00:18:22] georgias and these three lectures per week are run by Richard and those are around the signal
[00:18:22 - 00:18:29] single processes and stuff. Then we'll be running up the labs for Robocup during this time.
[00:18:30 - 00:18:35] And Richard also has a tutorial that relates to signals and georgias tutorials continue.
[00:18:36 - 00:18:42] So it's a little bit complicated but you'll figure it out. It's a little bit too easy.
[00:18:42 - 00:18:49] The labs labs labs labs labs labs labs labs. One thing to note with the labs for this course is they
[00:18:49 - 00:18:58] aren't taught labs. What these are are their scheduled times in your time tables so that you can come.
[00:18:58 - 00:19:04] You know that you and your teammates don't have other stuff on. So you can come and you can work on
[00:19:04 - 00:19:09] your robot together in the lab. There's generally TA support and drill in there if you'll be
[00:19:09 - 00:19:14] there as well so you can get some help with stuff. Don't have to come for them. Don't have to use them
[00:19:14 - 00:19:19] at all but outside of those times you may find it harder to get support from TA and that sort of thing.
[00:19:19 - 00:19:25] Okay. All right. See any questions about this sort of structure of the course in how it's working?
[00:19:27 - 00:19:33] You'll kind of figure it out as we go along. Okay. So there's some learning outcomes or learning
[00:19:33 - 00:19:39] objectives. At a high level they are apply the Megatron's design principles to a broad multi-disciplinary
[00:19:39 - 00:19:46] engineering project that's open-ended. That's the robot cut predominantly and it is very open-ended
[00:19:46 - 00:19:51] and you'll discover that more as you dive into it. You apply modern Megatron engineering design
[00:19:51 - 00:19:57] and analysis tools methods and going through this and you also effectively communicate design ideas,
[00:19:57 - 00:20:01] project work, engineering drawings, calculations, sets and engineering design reports.
[00:20:02 - 00:20:07] But in those those other two there's some sub-objective light. We're not going to go through
[00:20:07 - 00:20:13] them all here and now but you can see you know there's a bunch of stuff that you're going to learn
[00:20:13 - 00:20:19] through this course and some of it is through the robot cut project. Some of it's through
[00:20:19 - 00:20:25] the lectures with Richard and Segal. Some of it's through the lectures and assignments that
[00:20:25 - 00:20:31] happen with mechanical students in E&M E3R1. The way that we assist this
[00:20:31 - 00:20:37] and to make sure that you've achieved these learning outcomes. Here's the assessment schedule.
[00:20:37 - 00:20:43] So this is up on the course information system but it's also in the course schedule. So what you'll see
[00:20:44 - 00:20:53] is we've got these three the mechanical parts of the project that the assignments that you do
[00:20:53 - 00:20:58] with geology. So you've got the structure design, you've got the structure test and then you've got
[00:20:58 - 00:21:05] the bearing assignment and there were 6% 6% and 12%. Now every year people tell me that for mechanical
[00:21:05 - 00:21:14] those that were 15 I think it's 15 15 and 30% and that's true except that's not a problem
[00:21:14 - 00:21:20] because for one thing this is a 30 point course mechanicals is a 15 point course. So we can double
[00:21:20 - 00:21:24] these values and you'll look at that in Gecko so that's 12, 12, 24, it's still not 15, 15,
[00:21:24 - 00:21:31] do. Also doesn't matter because you're not being assessed like it's worth let's say 12% for you and
[00:21:31 - 00:21:37] it's so 15% for mechanical that's irrelevant. Those marks that you get in this course
[00:21:38 - 00:21:42] get aggregated with all the other marks you get in this course and then you get a grade that's
[00:21:42 - 00:21:47] relative to your classmates and this course it's got nothing to do with the mechanical students
[00:21:47 - 00:21:53] so don't stress about it okay. I'll say that now some people still stress about it there's nothing
[00:21:53 - 00:21:59] nothing that we can do about it. It's just the way it is don't worry. Then there's a few other
[00:21:59 - 00:22:04] bits and pieces so there's a multi-domain modeling assignment which is pretty low key. You follow
[00:22:04 - 00:22:09] the tutorial and then you've got to do a couple of extensions and then you write a page report.
[00:22:12 - 00:22:18] There's a test here it's worth 30% and that's in the midyear exam period because it's a test
[00:22:18 - 00:22:24] and it's not the end of course test that generally sits in the last part of the exam period
[00:22:25 - 00:22:32] and that's around the signal sensing stuff but also design related bits and pieces of the stuff
[00:22:32 - 00:22:41] I'm teaching you in this part of the course as well as record stuff. Richard also has
[00:22:41 - 00:22:45] there's a again a relatively low key assignment around the I&U and the reason like that relates to
[00:22:45 - 00:22:50] the sensor's material he teaches but the reason it's around the I&U is you get an I&U with the
[00:22:50 - 00:22:57] RoboCup kits and it's good to be able to use that effectively in your RoboCup robot so you'll learn
[00:22:57 - 00:23:03] some bits around that. Then the rest of the assessment really is around RoboCup so there's report one
[00:23:03 - 00:23:07] which is essentially the conceptual design you come up with some concepts you develop them you
[00:23:07 - 00:23:13] evaluate them you decide what you're going to go forward with in that you research previous
[00:23:13 - 00:23:19] robots and what worked well and what didn't go well and then make your concepts and go on.
[00:23:19 - 00:23:25] So on. The report who's basically a progress report you do you have some engineering drawings and
[00:23:25 - 00:23:29] that you'll have a fault tree analysis kind of predicting what might go wrong and how you can
[00:23:29 - 00:23:35] mitigate that and you'll then just provide a bit of an update on the progress to date that's what's
[00:23:35 - 00:23:42] worth a little bit less. There's then there's the competition which is in this week's
[00:23:42 - 00:23:47] that's like the third to last week or two and four obviously who's all the competition last year
[00:23:47 - 00:23:54] we'll get to the video. Okay so you'll be on the front end of the head this year. The competition is
[00:23:54 - 00:24:03] worth eight percent. The bulk of those marks do not come from where you get in that competition so it's
[00:24:03 - 00:24:07] not like warm and where your marks are largely dictated and mechanical with how well you did.
[00:24:08 - 00:24:14] What like the whole idea of this project with Rover Couples to go around and pick up weights right and
[00:24:14 - 00:24:19] so that's what defines a good design whether your robot happens to pick up slightly more weights
[00:24:19 - 00:24:25] slightly less weights than the other robot isn't a huge importance so the bulk of those marks
[00:24:25 - 00:24:32] come from did you successfully have a robot turn up with a robot that could a drive off its own base
[00:24:32 - 00:24:38] be navigates autonomously to some extent I didn't just go straight down the end and had the wall
[00:24:38 - 00:24:45] and saw and then three to pack up some weights and then and so you get more points for the average
[00:24:45 - 00:24:48] number of weights you pick up across the rounds because different robots will compete in the
[00:24:48 - 00:24:55] different number of rounds depends on how you progress through the competition and then finally
[00:24:55 - 00:25:00] there's a small amount of weighting that comes to your position in class so that doesn't have a
[00:25:00 - 00:25:05] huge impact on how you do and then finally there's the last report and that last report is kind of like
[00:25:05 - 00:25:09] a commissioning report and so in that you report on how your robot did and the competition and you
[00:25:09 - 00:25:15] compare it to three other robots and you make some commentary about how they did and then you kind
[00:25:15 - 00:25:19] of sum it up and say you know what would you have done better should you should you go back what
[00:25:19 - 00:25:29] could you have done to improve your robot and that sort of thing so is there any questions about that
[00:25:29 - 00:25:37] there's this sort of just I was review that so we only have one test in the middle of the year
[00:25:37 - 00:25:43] known as him test and no in the year that's correct there's a design course like in the past we didn't
[00:25:43 - 00:25:55] used to have tests but it's that's the person who lived their phone here we could answer it
[00:25:55 - 00:26:25] but believe it there it will stop oh was that you want to look in the phone no no no no I don't know
[00:26:25 - 00:26:33] had a shuttle that I push I push the button in the store so we'll be fine but it's not someone
[00:26:34 - 00:26:43] very good so yeah so it's a design course but there's two things that have
[00:26:44 - 00:26:52] come sort of caused us to add their test and we're slowly up weighted at over time one is what
[00:26:52 - 00:26:57] typically happens with group projects so Robocup is a relatively large group project overall ends up
[00:26:57 - 00:27:03] making up a reasonable chunk of the marks for this the structure design and the bearing
[00:27:03 - 00:27:08] housings I think get done in pairs as well so they are self chosen but again group projects
[00:27:08 - 00:27:14] what happens with group projects is they tend to cluster scores because those maybe the students
[00:27:14 - 00:27:20] who don't necessarily have generally get good scores get pulled up and sometimes the students who
[00:27:20 - 00:27:26] normally get better scores maybe get pulled down and it kind of pulls everything in and so by having
[00:27:26 - 00:27:33] the test and a few other elements in there it spodes that distribution back out and it also gives
[00:27:33 - 00:27:44] us a little bit of you know it prevents AI having such a large impact on the course although I don't
[00:27:44 - 00:27:52] think you get necessary a lot of help from AI at this point because the development of what you
[00:27:52 - 00:27:58] have to do in these design reports is not yet something you can easily ask to do before you yet
[00:28:01 - 00:28:06] we might have to change that later one thing I am doing though and so that's will make it a little
[00:28:06 - 00:28:13] bit interesting for you I'm trying to like we cut these reports kind of down in the amount of words
[00:28:13 - 00:28:18] that you had to write or the students had to write last year I'm trying to do that further this year
[00:28:18 - 00:28:24] mostly because it's bloody hard to mark them all because we have I don't know I think
[00:28:25 - 00:28:32] about 120 students in the class so that's 40 odd groups and when you've got 40 large reports in
[00:28:32 - 00:28:39] you're trying to mark these and provide you know valuable feedback or useful feedback it takes quite
[00:28:39 - 00:28:44] a long time and it's for various reasons it's harder to get tears than you know the ceiling
[00:28:45 - 00:28:52] and thus we're trying to kind of condense them down so for example and I haven't finished
[00:28:52 - 00:28:56] we haven't finished figuring it out yet but report one I think will be a lot more
[00:28:57 - 00:29:03] kind of average sketch based and less words for example because it's easier to mark but it's
[00:29:03 - 00:29:11] always a good for you as a way to communicate your ideas the second reports actually relatively
[00:29:11 - 00:29:18] light in terms of writing as well so we'll see how that goes. Hello we have to a phone
[00:29:28 - 00:29:36] okay also I'm also in the process at the moment of figuring out the differences for
[00:29:36 - 00:29:41] over this year compared to last year because we always tweak the rules a little bit I haven't
[00:29:42 - 00:29:48] settled on that yet but one thing I think I'm going to do is ban rubber bands so that'll be interesting
[00:29:50 - 00:29:56] so yeah when you get into the research or let's you see that that'll make a bit of an interesting
[00:29:58 - 00:30:08] change okay anyway so more details on my part of the course so this is the stuff that I teach in
[00:30:08 - 00:30:14] this term the first few lectures I said to recap in the design process fundamentals because I think
[00:30:14 - 00:30:19] you've got a little bit of this with Temanelae last year but I think I go to a little bit more detail
[00:30:20 - 00:30:26] we require a bit more detail in the robocup assessment and this is stuff like requirements
[00:30:26 - 00:30:32] and evaluating the designs some of this you would have seen in my angel 101 and bits and pieces
[00:30:32 - 00:30:37] like that but I want it to be a bit more systematic and so we go through there there's a few
[00:30:37 - 00:30:42] lectures on modeling and simulating systems from a physical systems point of view and some of that
[00:30:42 - 00:30:47] is understanding and will in the tutorial and the assignment around us using cincescape
[00:30:48 - 00:30:53] which sits in with matlab and we'll talk more about that later but that's for modeling
[00:30:53 - 00:30:57] multi-domain systems so you know electrical mechanical, rotational mechanical,
[00:30:57 - 00:31:03] and you may have hydraulic all connecting and being able to to model and then we've also got a
[00:31:03 - 00:31:09] little bit about dependability and risk because you have to think about that with design
[00:31:09 - 00:31:15] we'll talk about the details on the minute and also life cycle analysis so we only do like one
[00:31:15 - 00:31:20] brief lecture about life cycle analysis and you'll get much more of that with india and eony
[00:31:20 - 00:31:25] all through a one in a second semester but this is just like a light introduction so you kind of
[00:31:25 - 00:31:37] have it in your head good so we'll start with some of the the more you know what we're going to
[00:31:37 - 00:31:45] teach in the design side things what is engineering design I've done lots of talking somebody
[00:31:45 - 00:31:55] can tell me now what is what I'm going to teach you somewhat circular yeah
[00:31:57 - 00:32:04] yeah anyway we've got a different version of that iteration yeah there's a lot of iteration
[00:32:05 - 00:32:13] frustration yeah iteration frustration engineering design process yeah but what are you actually
[00:32:13 - 00:32:17] trying to do it when we design something what are we trying to differentiate why we design something
[00:32:18 - 00:32:24] to solve a problem yeah specifically with engineering design we're using the engineering science
[00:32:24 - 00:32:30] you've learned in other courses right so the stuff you learned in 202 and 203 and 303 and
[00:32:30 - 00:32:40] all that those those that fundamental applied physics material and you're using that creatively
[00:32:40 - 00:32:45] to solve some problem right it might be a problem that somebody's come to you with maybe it's a problem
[00:32:45 - 00:32:50] you're just trying to solve the fun for yourself but that's what engineering design is
[00:32:50 - 00:32:58] and so that's largely what you're going to get in this course around well if the robot got
[00:33:00 - 00:33:04] that's a project that you're going to have to solve a problem and go around and pick up these weights
[00:33:04 - 00:33:08] but similarly for georgia stuff you're going to have to design an aluminium beam so it can take a
[00:33:08 - 00:33:14] certain amount of weight but it'll fail with a different and additional weight and other bits and
[00:33:15 - 00:33:24] so in this course we are going to teach a bit about the engineering design process but and what I'd
[00:33:24 - 00:33:30] like to acknowledge with that is there's certainly not one this is the engineering design process
[00:33:32 - 00:33:38] you'll find as you have internships as you have more experiences you've got to see your careers
[00:33:38 - 00:33:43] different companies different people do this differently and they're all variations like they're
[00:33:43 - 00:33:49] all trying to solve a problem but the way they go about it they may have some elements that we
[00:33:49 - 00:33:53] talk about in this course they may have different elements they may emit some and they may
[00:33:53 - 00:34:00] say include other ones and that's fine like I can't teach you all of that what will teach in this
[00:34:00 - 00:34:08] as a reasonably structured sort of well established way of thinking about things that's bear in
[00:34:08 - 00:34:12] mind that when you go out you might go away from a company who do it wholly differently unless
[00:34:12 - 00:34:18] absolutely fine you know you'll be able to recognise you know the things that are similar
[00:34:18 - 00:34:22] and the things that are different who has done some design but you all haven't you because you
[00:34:22 - 00:34:31] all don't like one for one and stuff like that who enjoyed it you're enjoying a system
[00:34:32 - 00:34:38] you're says part difficult I was talking to somebody at the Inter-Moberk at last year
[00:34:39 - 00:34:46] and they said why didn't you just assess what was a good robot you know that's that's fear isn't
[00:34:46 - 00:34:51] we designing a robot you give us marks if it's a good robot and I said to them well what defines
[00:34:51 - 00:35:00] if it's good for a robot what defines if that design is good yeah it's got to pick up a lot of
[00:35:00 - 00:35:07] weights right so it's got to be able to pick up weights and yeah there might be some other things
[00:35:07 - 00:35:11] so what how else do we define a design in there for whether it's good?
[00:35:12 - 00:35:25] Organoids that's getting closer to it that would sit one level that would be one of these things
[00:35:25 - 00:35:31] I'm asking about at a higher level yes or requirements rather than yes so there's a difference
[00:35:31 - 00:35:35] between specifications or requirements before about that later but requirements you've got a
[00:35:35 - 00:35:38] design and it's got some requirements this stuff that has to do it's got to pick up weights
[00:35:39 - 00:35:41] probably has to move
[00:35:42 - 00:35:47] probably has to be able to avoid walls there's a bunch of these requirements so what is a good
[00:35:47 - 00:35:52] design though is it makes the requirements and that's essentially what we were
[00:35:53 - 00:35:59] assessing in that competition because you've got points for it did it move did it navigate
[00:35:59 - 00:36:03] did it pick up weights and when I was talking to their students about that he was like oh you're
[00:36:03 - 00:36:10] supposed because I can't just look at it and go gee that's a good design that once yet
[00:36:12 - 00:36:18] it comes down to what they do do they meet the requirement and therefore requirements are extremely
[00:36:18 - 00:36:23] important as you go out into your careers you will I don't know whether you're working for a design
[00:36:23 - 00:36:28] company or something else you can't design anything until you've got some requirements so you
[00:36:28 - 00:36:32] know what you're designing and so having a good design requirements is really good
[00:36:32 - 00:36:43] important but we'll talk about that in the next lecture so this course is mechatronic system
[00:36:43 - 00:36:52] design and that's a newish paradigm the two mechatronics was coined in 1964 in Japan by an
[00:36:52 - 00:36:58] engineer who worked for Yuxawa and Yuxawa still make like robots and a bunch of stuff
[00:36:58 - 00:37:08] traditionally prior to mechatronic system design kind of this idea what used to happen in the old days
[00:37:08 - 00:37:14] the head electro mechanical systems and largely what happened is someone would design the mechanical
[00:37:14 - 00:37:19] bit and they would go shit we need some electronics or electric motors or something and so then
[00:37:19 - 00:37:25] they design some electric motors and so on to fit on and around the mechanical stuff and then they
[00:37:25 - 00:37:30] might think oh we need some sort of computation to be able to run that control whatever and then that
[00:37:30 - 00:37:39] would be designed in a very sequential manner shown on the left the whole idea with mechatronic system
[00:37:39 - 00:37:46] design is that we consider the mechanical the electrical computational part kind of all at the start
[00:37:46 - 00:37:52] and you might make selections on how you do stuff differently for different projects but from those
[00:37:52 - 00:38:01] domains so you could for example choose maybe you want a mechanical speed governor for something
[00:38:01 - 00:38:07] you could have an electrical speed governor using electric circuits or you could have a computation based
[00:38:07 - 00:38:14] speed governor and depending on the project you might choose different ones and so the idea is that
[00:38:14 - 00:38:21] we've got the synergistic integration of mechanical electrical computational elements where synergistic
[00:38:21 - 00:38:28] means that the complementary beneficial not just because that was the shinier thing in the shelf
[00:38:30 - 00:38:36] and so that's the idea of mechatronic system design as opposed to that's from a hierarchical design
[00:38:38 - 00:38:44] and I've tried to illustrate that here this is with speed governor's that have you all heard
[00:38:44 - 00:38:50] of the watch governor before there's and James Watt WTT that's the thing on the left if you had a
[00:38:51 - 00:38:58] traditional used on steam engines and you wanted to govern the speed and so you had those balls and as
[00:38:58 - 00:39:02] they spent they were connected to the rotating system and as they spun faster they moved out and
[00:39:02 - 00:39:06] then that closed their throttle the system sort of slowed it down so it was a mechanical way of governing the
[00:39:06 - 00:39:18] speed you could use a electronic circuit with a DC motor to govern the speed so that it maintains a
[00:39:18 - 00:39:26] relatively constant speed or you could use basically an lc which is governing the speed as well
[00:39:26 - 00:39:31] so that's in the computational domain and so you've got more freedom with mechatronics design
[00:39:31 - 00:39:37] because you've got all these domains at your fingertips and you have to choose what you want to do
[00:39:38 - 00:39:43] to some extent that might make things harder because you've got more choice but it gives you some
[00:39:43 - 00:39:50] more freedom and what this nasty spiral in here is relating to is the iterative part that
[00:39:50 - 00:39:57] was mentioned before because annual design projects today who had a perfectly linear design
[00:39:57 - 00:40:01] where you sat down and you made a requirement and then you came up with a concept and then that
[00:40:01 - 00:40:06] doesn't make doing doing it in a straight line. Is that ever happened? No it doesn't happen.
[00:40:07 - 00:40:12] It's a very iterative thing you maybe build something in your test and that's not quite right
[00:40:12 - 00:40:18] so you circle back and you make a change and then that makes another change and so it's very much
[00:40:18 - 00:40:27] an iterative process. So you've got any thoughts on that? So make sense? Cool.
[00:40:29 - 00:40:33] So zooming out a little bit so looking at this right we've got mechanical electrical
[00:40:33 - 00:40:41] computation. If we zoom out a little bit further that sets in here so you know we're used to
[00:40:41 - 00:40:49] thinking about this functional design of the thing that we're designing but these days you
[00:40:49 - 00:40:54] can't think about that in isolation. There's a few other things we have to consider. We have to
[00:40:54 - 00:40:58] consider design for safety so you can't it's not like now you just design something and then
[00:40:58 - 00:41:08] think, oh, we probably put some guarding on there or you know you make a change or anything. How are we
[00:41:08 - 00:41:14] going to stop people cutting off their limbs? That should be baked in from the start with your
[00:41:14 - 00:41:23] design. Constantly thinking about risk and how you can mitigate those risks and similarly sustainability
[00:41:23 - 00:41:29] so the life cycle. These days as we go forward you don't just design something and then look and
[00:41:29 - 00:41:35] go, geez there, a lot of carbon emissions. Oh well. There's something to China because there's
[00:41:35 - 00:41:44] a manufacturing. These days people are expecting you to design things with a view to not only
[00:41:44 - 00:41:51] the safety and the function but also the life cycle of it. So what happens like what manufacturing
[00:41:51 - 00:41:58] process is a required? How do they impact the environment? But also what happens at the end? Like when
[00:41:58 - 00:42:04] that device or machine has reached its end of life, what happens to it? We don't want to just throw
[00:42:04 - 00:42:12] them all on the landfill. There can be some consideration to the end of life recycling and things
[00:42:12 - 00:42:19] like that that has been official when you're designing these projects. So we'll cover some
[00:42:19 - 00:42:25] aspects of this. The function of design I already mentioned, that's the making China's design
[00:42:25 - 00:42:31] process and things like that. Design for safety we come up with that will broadly covers the
[00:42:31 - 00:42:37] pinability and reliability and then like risk and you know you can start to predict what might go
[00:42:37 - 00:42:42] wrong and what can you mitigate with that and then the sustainability and the life cycle stuff will
[00:42:42 - 00:42:48] cover as well. And a very briefly incident end will take more detail giving more detail on any of
[00:42:48 - 00:43:00] everyone. So what is the design process? Somebody mentioned the design process before?
[00:43:09 - 00:43:20] You define the problem first and that's all. So you define the problem but then the next part
[00:43:20 - 00:43:25] really, well there's a few steps but effectively you need to solve it and that uses creativity and
[00:43:25 - 00:43:32] I think often people forget that engineering is quite creative and different because it's not
[00:43:32 - 00:43:37] like there's just steps that you follow and you look at like the roger cup kits that we've provided
[00:43:37 - 00:43:45] for the last, I don't know if given those out, they've been expanded upon but they're started in 2014
[00:43:45 - 00:43:52] largely with this architecture and over those last 12 years like Julian's editor more now you get
[00:43:52 - 00:43:57] time of flight sensors and you get some additional sensors and motors and other bits and pieces
[00:43:57 - 00:44:02] but largely the architecture is the same and if you look back at the videos in 2014-2015 you'll
[00:44:02 - 00:44:08] absolutely recognize those robots, they'll be picking up those weights but my goodness the variability
[00:44:08 - 00:44:14] and the creativity around the different designs over that period is you look at it, it's amazing
[00:44:14 - 00:44:20] like so many different ways to achieve that same simple task of picking up these weights.
[00:44:22 - 00:44:29] And so the design process is defining the problem and then you've got to come up with some
[00:44:29 - 00:44:34] potential concepts and that's a creative part then you've got a largely evaluate those concepts
[00:44:34 - 00:44:41] to decide which one is the best concept to go forward and you kind of prototype that you might
[00:44:41 - 00:44:46] break it down into sub modules which you develop and test and then you integrate them back together
[00:44:46 - 00:44:52] and then you'll have a final thing which you then validate against the requirements, did it do
[00:44:52 - 00:44:59] what it was supposed to do. Now the Megatron X design process is there on steroids so there's a little
[00:44:59 - 00:45:06] bit more with how the designs are created, maybe we do a lot more modelling and some model-based
[00:45:06 - 00:45:13] design is starting to become a big part of Megatron X design process and also what the designs
[00:45:13 - 00:45:20] are created from going back to the different domains do we use a mechanical part for this
[00:45:20 - 00:45:26] an electrical part for this a computational part or for some combination of those and the other
[00:45:26 - 00:45:32] part is that Megatron X design tries to it's not always easy but so I consider the whole system
[00:45:32 - 00:45:38] simultaneously thinking how those things might interact obviously that gets a bit difficult.
[00:45:39 - 00:45:45] There's a picture here of the Boeing T7 this is a train agenda it's well it's been a
[00:45:45 - 00:45:52] development for a while for the US Air Force and Navy and the whole thing with it is that Boeing
[00:45:52 - 00:45:57] used model-based engineering tools and advanced manufacturing and they had a full digital model of
[00:45:57 - 00:46:03] us and the idea was that model that digital aerodynamics and using things like console and
[00:46:03 - 00:46:10] whatever and all the electrical aeronic subsystems and then they validated all that and the digital
[00:46:10 - 00:46:15] sensor and they can just go up the start to the manufacturing system and everything would be
[00:46:16 - 00:46:21] manufactured very accurately and then they could slap them together and it would work.
[00:46:22 - 00:46:29] I think it's proven about harder and reality for them because that quote was from back in 2021
[00:46:29 - 00:46:34] and I think it was the case the concert went from concept to flight in three years but we're now in
[00:46:34 - 00:46:41] 2026 and I think they've just delivered the first one out of serial production and so the idea was
[00:46:41 - 00:46:47] good I think there's been a few hiccups along the way but the idea was you can do a lot more of this
[00:46:47 - 00:46:57] design and the digital scenes using model-based design and then from the you can you can optimize it
[00:47:02 - 00:47:06] and so this goes back to what you talked about before what are we trying to do requirements how do
[00:47:06 - 00:47:10] we do it so that's the designs and we specify and then how do we know if it's been done and that's
[00:47:10 - 00:47:16] validation verification but those processes are shown in what's known as the engineering V model so
[00:47:16 - 00:47:27] you should have seen this before I think right something like this yes no karate there's no one
[00:47:27 - 00:47:32] single engineering V model you can see different versions of it in different places but they're largely
[00:47:32 - 00:47:38] covered the same thing so you can see on this one there's a concept phase and so we come up with
[00:47:38 - 00:47:46] requirements maybe we do some analysis and architecture thinking then we come up with our design
[00:47:47 - 00:47:52] then we do some coding and prototyping and engineering modeling and then we go back up until we
[00:47:52 - 00:47:57] might develop the units the model subsystem tests and then we've got verification
[00:47:58 - 00:48:03] going back to the design and then we do integration tests of these modules to make sure that they
[00:48:04 - 00:48:07] you know when they're integrated they start to work well and then finally you've got acceptance
[00:48:07 - 00:48:13] tests so the design is coming down here and then they're sort of building it back up there's going
[00:48:13 - 00:48:18] up the right-hand side and we've got different versions of that the difference between is you
[00:48:18 - 00:48:21] and got no idea what the difference between verification and validation is
[00:48:31 - 00:48:36] yeah you're not far wrong so verification is like an internal thing that's checking that
[00:48:36 - 00:48:42] it's meeting the requirements that you said validations and external things so verification is
[00:48:43 - 00:48:49] did we build it right to our requirements whereas validation is did we build the right thing so that's
[00:48:49 - 00:48:54] going back to what the original customer or whatever design and wanted and did you build the right
[00:48:55 - 00:49:02] and so there's a somewhat subtle difference between those and in the robot cup we'll ask you to do a
[00:49:02 - 00:49:09] little bit about their verification so in the and the progress report sort of part way through
[00:49:09 - 00:49:13] we ask you to provide you know you should have done some testing at that point to see if you've
[00:49:13 - 00:49:21] met some of your requirements and you'll add some stuff to that to the report how many slides
[00:49:21 - 00:49:25] we've got a couple more slides and we've got 40 seconds so do it quick
[00:49:26 - 00:49:32] there's a version of us for model-based design this one comes from MATLAB and you can see it's
[00:49:32 - 00:49:36] somewhat similar requirements definition but then we do some desktop modeling and simulation
[00:49:36 - 00:49:40] some rapid control prototypes hyping some code generation software in the loop
[00:49:40 - 00:49:47] process and hardware in the loop and then some validation with the differences with those
[00:49:48 - 00:49:57] so software in the loop so this works for me to try on its systems but this parallel process is
[00:49:57 - 00:50:03] a lot due to the a lot related to the software firmware right software in the loop is the code for
[00:50:03 - 00:50:10] your control and simulation of the plan is compiled and run on a PC in non-real-time so you use
[00:50:10 - 00:50:14] something like cinascape or simulink and you run it and you check that the functionality is right
[00:50:14 - 00:50:21] but there's nothing to do with real-time then you've got processor in the loop and so that the code
[00:50:21 - 00:50:28] for control is compiled on the target processor but then it's connected to a PC and so rather than
[00:50:28 - 00:50:35] can rather than controlling the physical plant that it's going to control it's that it's talking
[00:50:35 - 00:50:40] to a PC and the PC is simulating that plant and so obviously with simulation it's a model
[00:50:40 - 00:50:46] so there's some abstraction and simplification but you're checking that you know with a simulator
[00:50:46 - 00:50:51] plant does that processor code behave correctly and then hardware in the loop is the code for controls
[00:50:51 - 00:50:57] compiled on the target processor and the simulation of the plant is compiled and run as a real-time
[00:50:57 - 00:51:06] model with external hardware inputs and outputs so you might have sensors and actuators and batteries
[00:51:06 - 00:51:10] and things which are all connected and so it starts to behave probably a nice way to think about
[00:51:10 - 00:51:16] hardware in the loop is something like a flat simulator so in this case the pilot's part of the hardware
[00:51:16 - 00:51:21] but you're sitting in there and you've got a full it looks like you're inside a plane and the pilot's
[00:51:21 - 00:51:28] controller that's going to a processor which is taking that it's got a dynamic model of the aircraft
[00:51:28 - 00:51:33] and so then what it shows on the gauges and on the screen is the output of that simulation
[00:51:33 - 00:51:39] and then the pilot controls it so that kind of captures the idea of hardware in the loop so you've
[00:51:39 - 00:51:44] got the hardware of controllers but you've got the hardware of the input output devices and also
[00:51:44 - 00:51:52] you've got the weight wear of the pilots and the dynamics in the actual system as all being looked
[00:51:52 - 00:52:00] after by a model running in real time you know so in this course you'll get a taste of this
[00:52:00 - 00:52:05] with a robot cap not the hardware and the loop stuff unfortunately but the megatron its design
[00:52:05 - 00:52:11] process and hopefully some more experience with design and you'll have some fun along the way
[00:52:12 - 00:52:22] cool all right we'll see tomorrow
[00:52:36 - 00:52:38] no
[00:52:44 - 00:52:46] we did
[00:52:51 - 00:52:54] last year some of it we're doing some pretty silly
[00:52:54 - 00:52:58] to get a good direction, because somebody wants to do that.
[00:52:58 - 00:53:06] Somebody, like in the past, who are hearing people say,
[00:53:06 - 00:53:10] they're always trying to try and come to a place
[00:53:10 - 00:53:12] because they have data, like we can talk about,
[00:53:12 - 00:53:15] you know, you're absolutely kind of like,
[00:53:15 - 00:53:18] you've just heard somebody, the main thing I was saying
[00:53:18 - 00:53:20] is kind of make sure that you do the same for stuff.
[00:53:20 - 00:53:22] First, yeah.
[00:53:22 - 00:53:24] I'm sure.
[00:53:24 - 00:53:25] Hi.
[00:53:25 - 00:53:27] Sure.
[00:53:27 - 00:53:29] I'll just pick up for the last game.
[00:53:29 - 00:53:30] Okay.
[00:53:30 - 00:53:32] It just depends if someone else is coming in.
[00:53:32 - 00:53:34] No one else is coming in with goods.
[00:53:34 - 00:53:38] I'm just like looking for a book for the first three.
[00:53:38 - 00:53:41] And I realize that I'm not, I don't believe.
[00:53:41 - 00:53:42] I want not.
[00:53:42 - 00:53:45] I'm not sure because I have a room to make a wrong bed,
[00:53:45 - 00:53:47] but I just, it's probably...
[00:53:47 - 00:53:49] Okay. Do you want a flick me an email?
[00:53:49 - 00:53:52] And I will add, so when did your enrollment go through, do you know?
[00:53:52 - 00:53:53] Was it relative or recently?
[00:53:53 - 00:53:55] No, it was like a month ago.
[00:53:55 - 00:53:56] I approved my green.
[00:53:56 - 00:54:01] Because what happens is to get, so that's the idea.
[00:54:01 - 00:54:04] So, because you have access to this course when you're in NT 301.
[00:54:04 - 00:54:05] Yes, yes.
[00:54:05 - 00:54:08] Because Tonya Schuper goes through and makes,
[00:54:08 - 00:54:10] because it's a very manual process,
[00:54:10 - 00:54:13] assigning students to the John Burdier,
[00:54:13 - 00:54:15] John fourth year, John Burdier, John Burdier,
[00:54:15 - 00:54:17] John Burdier, John Burdier, John Burdier,
[00:54:17 - 00:54:19] and so I think she did the walls back,
[00:54:19 - 00:54:22] but she couldn't absolutely have just missed people.
[00:54:22 - 00:54:23] Right, should I contact her?
[00:54:23 - 00:54:26] No, I flip me an email because I think I can probably add it to you.
[00:54:26 - 00:54:30] I'll aid you to add, and if I can, I'll just for that to tell you.
[00:54:30 - 00:54:31] Cool.
[00:54:31 - 00:54:32] Thank you so much.
[00:54:32 - 00:54:34] Goodly. Thanks for letting me know,
[00:54:34 - 00:54:36] because otherwise, yeah, I don't know, I don't know.
[00:54:36 - 00:54:38] I know, I was thinking, how am I gonna be able to...
[00:54:38 - 00:54:40] Yeah, yeah, yeah, that's your all guess.
[00:54:40 - 00:54:41] I'll see you.
[00:54:41 - 00:54:50] I'll see you.

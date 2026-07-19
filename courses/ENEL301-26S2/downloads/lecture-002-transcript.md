# ENEL301-26S2 Lecture 2 local ASR transcript

Date: July 17, 2026 10:00am-10:55am
Transcript type: Hermes-generated local ASR from validated Echo audio, not a native Echo transcript.
Backend/model: faster-whisper small.en, CPU int8, beam_size=5, vad_filter=True.
Source audio SHA-256: `8298cc3e4c4c885e18c9d96eaf4fa95d4d3cbe31e6aa8b0618a98016f8d1dcc6`
Generated: 2026-07-19T18:04:30.926018+12:00
Caveat: technical terms, equations, names and Māori words may require checking against slides/audio.

[00:00:02.900 - 00:00:07.900] Good morning, everyone. I hope you're all doing well on a frosty Friday.
[00:00:07.900 - 00:00:11.900] So, yeah, tonight's going to be about collaboration and teamwork.
[00:00:11.900 - 00:00:14.900] My voice is improving, but my hearing is not.
[00:00:14.900 - 00:00:18.900] So I can't really hear properly yet out of the right-hand side.
[00:00:18.900 - 00:00:20.900] So apologies if you are singing out.
[00:00:20.900 - 00:00:24.900] It might take me a while to hear you on that side.
[00:00:24.900 - 00:00:30.900] So before we start, look, I've just added a couple of slides for discussion
[00:00:30.900 - 00:00:37.900] based on some of what I was hearing in the tutorial earlier in the week.
[00:00:37.900 - 00:00:39.900] So, yeah, some really great discussion.
[00:00:39.900 - 00:00:42.900] And thanks for everyone for turning up and contributing.
[00:00:42.900 - 00:00:46.900] It sounded like it was all good.
[00:00:46.900 - 00:00:51.900] Yeah, so look, I will update these slides on Learn immediately after the lecture.
[00:00:51.900 - 00:00:55.900] So what you'll see, I'll just add to it.
[00:00:55.900 - 00:00:58.900] You'll see the corrected PDF.
[00:00:58.900 - 00:01:07.900] Okay, so, yeah, what came out in the room that I was in
[00:01:07.900 - 00:01:13.900] was the people were starting to pick up things like the ACM code of conduct.
[00:01:13.900 - 00:01:16.900] It seemed to be really focused on computer engineering,
[00:01:16.900 - 00:01:21.900] and whereas the IEEE one was really quite broad
[00:01:21.900 - 00:01:26.900] and was probably, as so, was really less specific.
[00:01:26.900 - 00:01:30.900] So I think an important outcome from the workshop
[00:01:30.900 - 00:01:36.900] is really that those codes of conduct are shaped by context.
[00:01:36.900 - 00:01:41.900] Okay, so the culture in which they're developed
[00:01:41.900 - 00:01:45.900] actually shapes what the different clauses look like.
[00:01:45.900 - 00:01:50.900] One of the questions that came up in one of the groups
[00:01:50.900 - 00:01:56.900] was what happens if you actually breach one of these codes of conduct?
[00:01:56.900 - 00:02:01.900] The reality is that if you're a member of one of those professional societies,
[00:02:01.900 - 00:02:05.900] usually it's managed within that society.
[00:02:05.900 - 00:02:13.900] So there's usually a complaints process that you would go through,
[00:02:13.900 - 00:02:16.900] rights to appeal, and so on.
[00:02:16.900 - 00:02:21.900] And look, if you're found to breach a code of conduct,
[00:02:21.900 - 00:02:24.900] the remedy or the outcome from that can vary.
[00:02:24.900 - 00:02:26.900] But, you know, typically it can include censure,
[00:02:26.900 - 00:02:31.900] so you might not actually be allowed to say certain things.
[00:02:31.900 - 00:02:35.900] Fines, okay, so you get hit with some money.
[00:02:35.900 - 00:02:38.900] You might be suspended for a period of time
[00:02:38.900 - 00:02:41.900] or even kicked out of that professional society.
[00:02:41.900 - 00:02:45.900] Okay, so it can happen.
[00:02:45.900 - 00:02:51.900] Ethical dilemma hit my desk just overnight.
[00:02:51.900 - 00:02:53.900] I'll talk about it in a second, really interesting one.
[00:02:53.900 - 00:02:58.900] I'm not sure how I'm going to tackle it just yet.
[00:02:58.900 - 00:03:02.900] Okay, but look, other legal options exist.
[00:03:02.900 - 00:03:06.900] So depending where you are in the world,
[00:03:06.900 - 00:03:10.900] there can actually be further legal implications
[00:03:10.900 - 00:03:16.900] if someone makes a pretty major breach of a code of conduct
[00:03:16.900 - 00:03:18.900] because they might have actually broken the law.
[00:03:18.900 - 00:03:23.900] Okay, so this happened a couple of years ago in New Zealand.
[00:03:23.900 - 00:03:29.900] There was a student who studied engineering at University of Auckland
[00:03:29.900 - 00:03:32.900] that didn't actually complete the qualification.
[00:03:32.900 - 00:03:37.900] Okay, they were a student member of Engineering New Zealand
[00:03:37.900 - 00:03:44.900] and went around the country saying that they were not only an engineer
[00:03:44.900 - 00:03:48.900] but also a chartered professional engineer.
[00:03:48.900 - 00:03:55.900] So that was reported to Engineering New Zealand
[00:03:55.900 - 00:04:01.900] and because that person was a student member of Engineering New Zealand,
[00:04:01.900 - 00:04:05.900] Engineering New Zealand then could apply the code of conduct
[00:04:05.900 - 00:04:13.900] and all the policies onto that particular person or student.
[00:04:13.900 - 00:04:19.900] Yeah, so Engineering New Zealand also reported this person to the police
[00:04:19.900 - 00:04:27.900] and then that person was eventually found guilty of 38 counts of fraud.
[00:04:27.900 - 00:04:35.900] Yeah, so yeah, and got 5,000 all fine as well as a reprimand.
[00:04:35.900 - 00:04:38.900] You're a naughty person.
[00:04:38.900 - 00:04:44.620] Okay, but here's the really interesting bit.
[00:04:44.620 - 00:04:47.620] The person can still say they're an engineer.
[00:04:47.620 - 00:04:51.620] Okay, so even after being convicted of fraud,
[00:04:51.620 - 00:04:54.620] being fined and reprimanded by Engineering New Zealand,
[00:04:54.620 - 00:04:59.620] there is nothing stopping that person saying in New Zealand
[00:04:59.620 - 00:05:03.620] that they are an engineer.
[00:05:03.620 - 00:05:10.620] Yeah, so the term engineer remains an unprotected title in New Zealand.
[00:05:10.620 - 00:05:13.620] Engineering New Zealand is trying to change that.
[00:05:13.620 - 00:05:18.620] So in the not this government's term but the previous government's term,
[00:05:18.620 - 00:05:22.620] there was a bit of legislation that was going to go through Parliament
[00:05:22.620 - 00:05:25.620] but time ran out.
[00:05:25.620 - 00:05:29.620] It wasn't on this current government's agenda but watch this space.
[00:05:29.620 - 00:05:36.620] So things might change and the term engineer isn't always protected
[00:05:36.620 - 00:05:39.620] depending on where you work in the world.
[00:05:39.620 - 00:05:43.620] It even depends, say, in Australia,
[00:05:43.620 - 00:05:45.620] it depends on what state you're working in,
[00:05:45.620 - 00:05:48.620] whether or not the term is protected.
[00:05:48.620 - 00:05:51.620] Yeah, so you're pretty interesting.
[00:05:51.620 - 00:05:59.000] Cool. So this is what we're going to cover today, collaboration and teamwork.
[00:05:59.000 - 00:06:07.000] And yeah, collaboration is the key to your success as an engineer.
[00:06:07.000 - 00:06:13.000] Okay, so hopefully some of you spent a little bit of time
[00:06:13.000 - 00:06:18.000] listening to the podcast that I suggested earlier in the week.
[00:06:18.000 - 00:06:28.300] And yeah, any thoughts on those who listened to James?
[00:06:28.300 - 00:06:29.300] I know one person did.
[00:06:29.300 - 00:06:32.300] I might have to resort to him to ask questions.
[00:06:32.300 - 00:06:34.300] Anybody else have a listen?
[00:06:34.300 - 00:06:39.580] Yeah. What did you think? What did you learn?
[00:06:39.580 - 00:06:49.670] That's all right.
[00:06:49.670 - 00:06:57.670] So what did James talk about when it comes to what the focus is
[00:06:57.670 - 00:07:03.670] as you, as you all, are learning engineering at a university.
[00:07:03.670 - 00:07:08.670] How is the assessment designed to reward you?
[00:07:08.670 - 00:07:15.160] Yeah, it rewards individual endeavors.
[00:07:15.160 - 00:07:16.160] Yep.
[00:07:16.160 - 00:07:21.160] So sometimes people call this the hidden curriculum,
[00:07:21.160 - 00:07:26.160] is that we're potentially training engineers by stealth
[00:07:26.160 - 00:07:30.160] to be working as individuals, and that's not always a good thing.
[00:07:30.160 - 00:07:34.160] Okay, so by and large, through your education,
[00:07:34.160 - 00:07:38.160] you have been awarded for your individual performance
[00:07:38.160 - 00:07:41.160] rather than the collaboration performance.
[00:07:41.160 - 00:07:48.160] Okay, and that's in stark contrast with the realities of engineering.
[00:07:48.160 - 00:07:54.160] Okay, what else came up in that podcast?
[00:07:54.160 - 00:08:04.460] Yep, yeah, cool. Yep, yep, yep.
[00:08:04.460 - 00:08:08.460] So yeah, to keep an open mind about other disciplines,
[00:08:08.460 - 00:08:10.460] they're probably even beyond engineering, right?
[00:08:10.460 - 00:08:13.800] Yeah, cool, yep.
[00:08:13.800 - 00:08:14.800] Yep, learning to listen.
[00:08:14.800 - 00:08:19.800] Yeah, so he describes it, I think, as the most under-taught,
[00:08:19.800 - 00:08:23.800] yet probably the most valuable skill in engineering.
[00:08:23.800 - 00:08:24.800] Yep, for sure.
[00:08:24.800 - 00:08:26.800] Okay, anything else?
[00:08:26.800 - 00:08:35.290] Yeah, they don't produce value by and large.
[00:08:35.290 - 00:08:40.290] Yeah, so we'll talk about how engineers generate value later on.
[00:08:40.290 - 00:08:43.290] Yeah, and what's interesting, though,
[00:08:43.290 - 00:08:48.290] is that engineers actually don't necessarily know
[00:08:48.290 - 00:08:51.290] what value they're actually creating in their work.
[00:08:51.290 - 00:08:52.290] Okay, so they do all this work,
[00:08:52.290 - 00:08:53.290] but they don't really understand why
[00:08:53.290 - 00:08:56.290] and what the greater benefit is.
[00:08:56.290 - 00:08:59.760] Cool, okay.
[00:09:00.760 - 00:09:05.760] What did he say about sort of emailing and texting?
[00:09:05.760 - 00:09:09.460] Bad.
[00:09:09.460 - 00:09:12.460] Yeah, so yeah, over the last couple of decades,
[00:09:12.460 - 00:09:15.460] there's been a bit of a shift in society
[00:09:15.460 - 00:09:19.460] to convenient text messaging and flicking emails to people,
[00:09:19.460 - 00:09:21.460] rather than actually picking up the phone
[00:09:21.460 - 00:09:25.460] or going down and seeing someone to have a chat.
[00:09:25.460 - 00:09:31.460] Yeah, so there's a bit of a resentment
[00:09:31.460 - 00:09:38.460] or, yeah, towards collaboration.
[00:09:38.460 - 00:09:39.460] It's hard work.
[00:09:39.460 - 00:09:40.460] Collaboration is hard work.
[00:09:40.460 - 00:09:44.460] It's easier for some and more difficult for others.
[00:09:44.460 - 00:09:47.460] It's a learned skill,
[00:09:47.460 - 00:09:52.460] and it is actually shaped by you and how you've grown up.
[00:09:52.460 - 00:09:55.460] Okay, so working through that
[00:09:55.460 - 00:09:58.460] and getting the understanding of the culture
[00:09:58.460 - 00:10:05.460] and context that you're working in is the key to success.
[00:10:05.460 - 00:10:07.460] Yeah, and another interesting thing
[00:10:07.460 - 00:10:10.460] about the work of James Trevelyan,
[00:10:10.460 - 00:10:13.460] and maybe this after this lecture,
[00:10:13.460 - 00:10:16.460] if I've got time, I might show you some of my own research,
[00:10:16.460 - 00:10:20.460] but engineers like to avoid things
[00:10:20.460 - 00:10:23.460] that they don't think is engineering,
[00:10:23.460 - 00:10:27.460] even though it is engineering.
[00:10:27.460 - 00:10:34.460] And those individual views are shaped by your own experiences,
[00:10:34.460 - 00:10:38.460] and your experiences are going to be different to everyone else's.
[00:10:38.460 - 00:10:41.460] So what you think is engineering,
[00:10:41.460 - 00:10:44.460] someone else will hold a very different view.
[00:10:44.460 - 00:10:48.460] So, yeah, and again, if I've got some time,
[00:10:48.460 - 00:10:53.460] I'll see if I can dig out some of the research I've done on this.
[00:10:53.460 - 00:10:57.460] Yeah, the other one, too, is that informal conversations
[00:10:57.460 - 00:11:01.460] are really, really important to engineering.
[00:11:01.460 - 00:11:04.460] They call them the water cooler conversations,
[00:11:04.460 - 00:11:10.460] but, yeah, engineering is a socio-technical discipline,
[00:11:10.460 - 00:11:13.460] and engineering works really well
[00:11:13.460 - 00:11:19.020] when people are actually starting to talk informally.
[00:11:19.020 - 00:11:26.020] OK, so coming back to what I spoke about earlier in the week,
[00:11:26.020 - 00:11:30.020] engineers can't achieve much without a lot of help from other people,
[00:11:30.020 - 00:11:33.020] so your collaboration skills will determine
[00:11:33.020 - 00:11:38.020] how far you go in your engineering career.
[00:11:38.020 - 00:11:44.070] So, yeah, you can't get anything done without the help of others.
[00:11:44.070 - 00:11:48.070] OK, so as an example, as a graduate engineer,
[00:11:48.070 - 00:11:52.070] one of your main roles is to understand, interpret
[00:11:52.070 - 00:11:56.070] and negotiate technical requirements for a design.
[00:11:56.070 - 00:12:00.070] There can be physical design, software design, you name it.
[00:12:00.070 - 00:12:04.070] But without collaboration, you won't be able to do this.
[00:12:04.070 - 00:12:06.070] You won't even be able to conceive a design
[00:12:06.070 - 00:12:11.700] unless you actually collaborate in the first place.
[00:12:11.700 - 00:12:16.700] OK, I'd also just want to challenge preconceived notions,
[00:12:16.700 - 00:12:20.700] again, coming back to what James Trevillian was talking about,
[00:12:20.700 - 00:12:25.700] about individual work that engineers do.
[00:12:25.700 - 00:12:27.700] OK, so you might think that in the first few years
[00:12:27.700 - 00:12:30.700] after you graduate, you're just going to focus
[00:12:30.700 - 00:12:34.700] on technical stuff by yourself.
[00:12:34.700 - 00:12:37.700] And you'll develop management skills later on,
[00:12:37.700 - 00:12:41.700] and the communication skills, you need those later on.
[00:12:41.700 - 00:12:44.700] That's not true. You need them now.
[00:12:44.700 - 00:12:48.700] OK, so from the very start of your career,
[00:12:48.700 - 00:12:51.700] you need these skills.
[00:12:51.700 - 00:12:57.100] OK, you might think that your discipline is different.
[00:12:57.100 - 00:13:00.100] OK, that, I don't know, mechatronics,
[00:13:00.100 - 00:13:03.100] you might think that, oh, my discipline is different,
[00:13:03.100 - 00:13:07.100] I'm unique. But that's not true.
[00:13:07.100 - 00:13:14.100] OK, there are some nuances within the discipline,
[00:13:14.100 - 00:13:17.100] but overall, it doesn't matter what your discipline,
[00:13:17.100 - 00:13:20.100] you will be collaborating, including collaborating
[00:13:20.100 - 00:13:23.100] with people outside your discipline.
[00:13:23.100 - 00:13:27.580] So if you don't believe me, check this out.
[00:13:27.580 - 00:13:31.580] OK, so this is some results from the research project that I run.
[00:13:31.580 - 00:13:35.580] So I run a big project that tracks hundreds of engineers'
[00:13:35.580 - 00:13:41.580] careers over time, and I asked them a question years ago
[00:13:41.580 - 00:13:46.580] about how much time do you spend in your work working individually
[00:13:46.580 - 00:13:51.580] versus working with others or collaborating.
[00:13:51.580 - 00:13:56.580] Overall, it's about 50% of the time engineers
[00:13:56.580 - 00:13:59.580] are actually collaborating with others.
[00:13:59.580 - 00:14:01.580] There are some slight nuances differences
[00:14:01.580 - 00:14:03.580] between the different disciplines.
[00:14:03.580 - 00:14:06.580] So working from left to right, you've got mechatronics,
[00:14:06.580 - 00:14:08.580] computer engineering, software engineering,
[00:14:08.580 - 00:14:12.580] electrical engineering, and electronic engineering.
[00:14:12.580 - 00:14:15.580] And you can see there's some real extremes.
[00:14:15.580 - 00:14:22.580] There's some people who are working with others 100% of the time,
[00:14:22.580 - 00:14:26.580] and then you've got some people right down at the bottom there
[00:14:26.580 - 00:14:32.580] that they're working by themselves nearly all the time.
[00:14:32.580 - 00:14:37.580] But, yeah, the vast majority of people within those quartiles,
[00:14:37.580 - 00:14:40.580] yeah, they're collaborating a lot.
[00:14:40.580 - 00:14:45.580] Cool, so just be wary, though, with like any research,
[00:14:45.580 - 00:14:48.580] there are some limitations.
[00:14:48.580 - 00:14:54.580] So, yeah, these values were self-reported.
[00:14:54.580 - 00:15:00.580] They might be real, but some of them might not actually be real
[00:15:00.580 - 00:15:02.580] as well.
[00:15:02.580 - 00:15:06.580] So it's not necessarily representative of the entire engineering population,
[00:15:06.580 - 00:15:10.580] but it's an interesting data point.
[00:15:10.580 - 00:15:13.580] It also doesn't show the effect of other factors.
[00:15:13.580 - 00:15:17.580] So one of the other things that I found in this research
[00:15:17.580 - 00:15:22.580] is that the amount of collaboration time actually increases
[00:15:22.580 - 00:15:26.580] as people's experience increases, the years of experience.
[00:15:26.580 - 00:15:29.580] So as a graduate, you'll be collaborating less
[00:15:29.580 - 00:15:32.580] within that build-up over time.
[00:15:32.580 - 00:15:35.580] I also didn't take into account things like, you know,
[00:15:35.580 - 00:15:38.580] whether or not someone was working in a small company
[00:15:38.580 - 00:15:44.580] versus a big company, what country they were working in, and so on.
[00:15:44.580 - 00:15:52.860] Okay, but nevertheless, it's pretty clear engineers collaborate a lot.
[00:15:52.860 - 00:15:59.580] Cool, okay, so what is collaboration?
[00:15:59.580 - 00:16:02.580] And I'm leaning on James Trevelyan a lot here.
[00:16:02.580 - 00:16:07.580] So he says the collaboration is working together on the same thing
[00:16:07.580 - 00:16:11.580] to purposely exploit differences in the way that we act and think
[00:16:11.580 - 00:16:15.580] through technical and social interactions.
[00:16:15.580 - 00:16:18.580] Okay, so what makes it a good collaboration?
[00:16:18.580 - 00:16:21.580] So we'll unpack this statement.
[00:16:21.580 - 00:16:26.580] First of all, we need to understand what that same thing is,
[00:16:26.580 - 00:16:30.580] need to understand our differences in the way that we act and think
[00:16:30.580 - 00:16:36.580] so that we can exploit our strengths and have really purposeful technical
[00:16:36.580 - 00:16:44.620] and social interactions using effective communication.
[00:16:44.620 - 00:16:52.620] Okay, so working together on the same thing.
[00:16:52.620 - 00:17:01.920] Okay, so what I'd really recommend that you do if you don't already do this,
[00:17:01.920 - 00:17:09.920] whenever you start a team project is to get your processes right from the beginning.
[00:17:09.920 - 00:17:15.920] Okay, so I've done this a little bit in Eng 101, maybe some other courses as well,
[00:17:15.920 - 00:17:19.920] but plan how you're going to work together.
[00:17:19.920 - 00:17:24.920] You might want to establish a team charter, okay, so what is your purpose,
[00:17:24.920 - 00:17:28.920] how are you going to work together, how are you going to communicate,
[00:17:28.920 - 00:17:31.920] how are you going to reward each other for successes,
[00:17:31.920 - 00:17:36.920] how are you going to hold each other to account if things aren't going well,
[00:17:36.920 - 00:17:43.920] how are you going to escalate things and manage things when things don't go well,
[00:17:43.920 - 00:17:51.920] and then also clearly identifying tasks like project planning,
[00:17:51.920 - 00:17:55.920] who's going to do what, when, how, to what standard, and so on.
[00:17:55.920 - 00:17:59.920] I'll talk a little bit more about that in 301 later on.
[00:17:59.920 - 00:18:04.460] I'm going to pause there because I just realized I didn't actually talk about
[00:18:04.460 - 00:18:10.460] my little ethical problem that I had that landed overnight.
[00:18:10.460 - 00:18:16.460] I am involved in a professional society that runs an annual conference.
[00:18:16.460 - 00:18:20.460] Over the last few days, the technical committee is reviewing a lot
[00:18:20.460 - 00:18:26.460] of conference paper submissions and generative AI has raised its head.
[00:18:26.460 - 00:18:31.460] We've identified two or three papers already that have been submitted
[00:18:31.460 - 00:18:35.460] by academics which contain fictitious references.
[00:18:35.460 - 00:18:48.600] Yeah, so it's a pretty big red flag that a pretty bad version of chat GBT was used.
[00:18:48.600 - 00:18:55.600] And I realized this morning, ooh, what if those people are actually members
[00:18:55.600 - 00:18:59.600] of a professional society that I am in?
[00:18:59.600 - 00:19:05.600] So if I'm a member of Engineers Australia and Engineering New Zealand,
[00:19:05.600 - 00:19:10.600] this is an Australasian conference, so there's a very good chance that
[00:19:10.600 - 00:19:16.600] that academic is probably from Engineers Australia or Engineering New Zealand.
[00:19:16.600 - 00:19:21.600] I've been made aware of this. Do I need to snitch them?
[00:19:22.600 - 00:19:30.600] Yeah, so that's something that I probably need to go away
[00:19:30.600 - 00:19:33.600] and have a look at the codes of conduct.
[00:19:33.600 - 00:19:39.600] I probably actually need to talk with the conference committee.
[00:19:39.600 - 00:19:44.600] We actually have got a process in place for the conference for dealing with this.
[00:19:44.600 - 00:19:51.600] But even outside of that, I've got responsibilities as a professional engineer.
[00:19:51.600 - 00:19:55.600] So I'm a charter professional engineer in Australia,
[00:19:55.600 - 00:20:02.600] and yeah, I've got a pretty strong binding to their code of conduct.
[00:20:02.600 - 00:20:13.250] What do you think I should do for the obligations? Yeah.
[00:20:13.250 - 00:20:17.250] Someone actually sort of logged into Teams and there's a bit of a chat
[00:20:17.250 - 00:20:22.250] going on this morning saying it's scientific misconduct.
[00:20:22.250 - 00:20:28.250] I went, ooh, I don't know about misconduct, like scientific misconduct,
[00:20:28.250 - 00:20:32.250] because that's probably more about fabrication of results
[00:20:32.250 - 00:20:34.250] and that sort of thing.
[00:20:34.250 - 00:20:41.250] It's certainly pretty bad. Yeah. Anything else? Yeah.
[00:20:41.250 - 00:20:48.260] This is going to be the problem. Yeah, yeah. How do you actually prove it?
[00:20:49.260 - 00:20:54.260] With fictitious references, it's – yeah, and this is probably – again,
[00:20:54.260 - 00:20:55.260] it comes down to due process.
[00:20:55.260 - 00:21:03.260] We probably do need to actually follow a process and give them a right to appeal.
[00:21:03.260 - 00:21:10.260] And then – yeah, so probably I should follow that process first
[00:21:10.260 - 00:21:13.260] and give them a hearing, because maybe they've got a reason
[00:21:13.260 - 00:21:19.260] why there's fictitious references with fake HTML –
[00:21:19.260 - 00:21:28.260] oh, sorry, hyperlinks that take you nowhere. Yeah. Interesting, eh? Cool.
[00:21:28.260 - 00:21:35.260] So anyway, back to this. Yeah, something for me to ponder about over the weekend.
[00:21:36.260 - 00:21:43.260] Okay, so, yeah, we're purposefully exploiting the way we think and act
[00:21:43.260 - 00:21:49.260] through technical and social interactions to get things happening on that same thing.
[00:21:49.260 - 00:21:53.260] Okay, so the first thing that we need to do is really clearly identify
[00:21:53.260 - 00:21:56.260] what that same thing is, okay?
[00:21:56.260 - 00:22:00.260] And again, we'll talk a little bit about that more later in the semester.
[00:22:00.260 - 00:22:05.540] Okay, then we need to purposely exploit differences in the way that we act
[00:22:05.540 - 00:22:08.540] and think. So we all have strengths.
[00:22:08.540 - 00:22:14.540] The key is identifying and exploiting those strengths, okay?
[00:22:14.540 - 00:22:19.540] So one of my strengths as an example is that I'm quite systematic
[00:22:19.540 - 00:22:26.540] and quite details-focused. So give me a complex, usually administrative task –
[00:22:26.540 - 00:22:29.540] it's probably why I'm ahead – and I'll try and break it down
[00:22:29.540 - 00:22:32.540] and I'll keep chipping away at it, okay?
[00:22:33.540 - 00:22:39.540] I'm also pretty good at understanding different engineering disciplines.
[00:22:39.540 - 00:22:44.540] Some would call me a generalist, but for me I actually see that as a bit of a strength.
[00:22:44.540 - 00:22:48.540] So I'm able to actually jump between different engineering disciplines
[00:22:48.540 - 00:22:54.540] and actually get a pretty good understanding about what they're talking about fairly quickly.
[00:22:54.540 - 00:22:58.540] Okay, so have a think about what your differences are
[00:22:58.540 - 00:23:05.460] and that you think you could exploit when working with others.
[00:23:05.460 - 00:23:13.960] So what we'll do now – do a little mentimeter exercise.
[00:23:13.960 - 00:23:32.370] So, okay, so what do you think some of the characteristics are that make us different?
[00:23:32.370 - 00:23:50.900] I was always waiting. You know, this is always a risk doing this, right?
[00:24:19.680 - 00:24:35.640] I can't control it now. It's the most important – it's a popular response, of course.
[00:24:35.640 - 00:25:23.790] Cool, okay, so we'll hit stop there. Okay, and hopefully we can show that. Cool.
[00:25:23.790 - 00:25:31.460] Okay, so I'm going to get rid of this one if I can.
[00:25:31.460 - 00:25:41.460] Anyway, okay, so excluding the phallic references, yeah, so look, there's lots in here, right?
[00:25:41.460 - 00:25:48.460] You've got, yeah, how you brought up your education, your background, your culture, your morals.
[00:25:48.460 - 00:25:56.460] Might be neurodivergence in there as well. Your experiences, yeah, the extracurricular activities
[00:25:57.460 - 00:26:06.460] that you've been involved with. Yeah, maturity, so perhaps there's a bit of luck of that with the girth and length thing.
[00:26:06.460 - 00:26:17.460] Yeah, physical abilities and disabilities, how you look, okay, so there's all sorts of things, okay, that makes us different.
[00:26:18.460 - 00:26:27.460] And yeah, how do we actually capitalize on those things to make engineering work really awesome?
[00:26:27.460 - 00:26:39.080] Okay, so going back to the – okay, so yeah, we need to recognize and positively exploit differences.
[00:26:39.080 - 00:26:47.080] We'll talk a little bit about some of this stuff next Friday, okay,
[00:26:47.080 - 00:26:55.080] where we're talking about understanding different views of diversity and so on and how to get the most out of it.
[00:26:55.080 - 00:27:12.080] Okay, yeah, then technical and social interactions, okay, so knowledge development, how you develop knowledge is usually developed based on two things.
[00:27:12.080 - 00:27:22.080] Okay, there's explicit knowledge, okay, that's the knowledge that is usually written and that you receive.
[00:27:22.080 - 00:27:28.080] And then there is tacit knowledge, okay, and that's developed through social interactions.
[00:27:28.080 - 00:27:35.080] You need both of those in order to be an awesome engineer.
[00:27:35.080 - 00:27:48.080] The tacit knowledge requires you to build really excellent relationships, okay, so you'll need to learn how to do this.
[00:27:48.080 - 00:27:52.080] Some of you are probably really quite skilled already, but it comes with time.
[00:27:52.080 - 00:28:01.080] So building trust and rapport is the key to developing great relationships.
[00:28:01.080 - 00:28:06.080] Part of it, too, is recording information, so yeah, really excellent listening.
[00:28:06.080 - 00:28:20.080] That's what James Trevelyan was talking about, taking really good notes, okay, so I can see a couple of people taking awesome notes and taking photos and videos if you're allowed.
[00:28:21.080 - 00:28:31.080] And yeah, when you're interacting with someone, you know, show some matters, you know, like listen to them, make really good eye contact.
[00:28:31.080 - 00:28:42.080] Sometimes that can be inappropriate depending on your culture and appropriate culture, so you know, appropriate posture, okay, these are subtle things.
[00:28:42.080 - 00:28:48.080] And they are key to helping you with your social interactions.
[00:28:48.080 - 00:29:06.080] I'm still learning to do this, so one of my bad habits is that I'm not very good at holding a neutral face when I disagree with something, okay, so I don't have a good poker face.
[00:29:06.080 - 00:29:15.080] Yeah, so if I disagree, I'll actively show it in my face, okay, and that's not a good thing necessarily.
[00:29:15.080 - 00:29:21.610] Okay, all right.
[00:29:21.610 - 00:29:34.610] Yeah, on kind of social media messages, you might think that the best thing to do as an engineer is to immediately respond to a message.
[00:29:34.610 - 00:29:44.610] What I did this morning, I got a message through Teams, I saw the person was online, said, no, I'm not going to type this because it's too tricky, I'm going to hit call instead.
[00:29:44.610 - 00:29:59.610] Okay, and they came up, we had a conversation, job was done, okay, and there's a lot more contextual nuance that came out of that conversation than me smashing away on the keyboard, okay.
[00:29:59.610 - 00:30:06.610] Yeah, so sometimes, yeah, emails are absolutely needed, but you know what, pick up the phone.
[00:30:06.610 - 00:30:13.610] It's nice and convenient, okay.
[00:30:13.610 - 00:30:33.610] Yeah, and likewise, emails and text messages, although they're convenient, if you don't get them right, people can misread it, okay, so yeah, seeing someone calling them, please try to do that if you can.
[00:30:33.610 - 00:30:47.270] Okay, right. Okay, very brief slide on meetings.
[00:30:47.270 - 00:30:55.270] Engineers hate meetings, but it's one of the most frequent activities that an engineer has to do.
[00:30:55.270 - 00:31:07.270] Okay, and there should only really be four reasons to go to a meeting or to hold a meeting, to build relationships, to share information, make a decision or to solve a problem.
[00:31:07.270 - 00:31:16.270] Okay, if it's not any of those four, you are welcome to question whether or not you need to actually go to that meeting or hold that meeting.
[00:31:16.270 - 00:31:24.270] Okay, so yeah, and a bit of a funny flow chart about meetings.
[00:31:24.270 - 00:31:40.270] Yeah, so yeah, my calendar is filled with meetings, but it's part of my job, okay, and nearly all the time, it is about this stuff, okay.
[00:31:40.270 - 00:31:48.860] Tell me about when collaboration doesn't work.
[00:31:48.860 - 00:31:52.860] What are some behaviours that inhibit collaboration?
[00:31:52.860 - 00:32:19.570] Yeah, just give me a second, I've got a new laptop this morning, so it's not playing the game, I'll just extend that so I can drag it across, sorry.
[00:32:19.570 - 00:32:45.570] Okay, so the tyranny of distance, okay, so working across time, distance, like yeah, face-to-face interactions are usually best, right, so yeah, that can be tricky.
[00:32:45.570 - 00:33:00.410] Okay, cool, what else inhibits collaboration? Yeah, we'll find common ground. Yeah, yeah, for sure, yep.
[00:33:00.410 - 00:33:07.410] Cool, so yeah, when you've got someone who's fixated on a view or an outcome, yeah, that can really inhibit things.
[00:33:07.410 - 00:33:21.620] We'll go there and then we'll come down to you, yep, yep, yep.
[00:33:21.620 - 00:33:49.500] Yeah, yep, another one that was done here, yeah.
[00:33:49.500 - 00:34:30.110] Oh yeah, so one person in the team wanting to solve it, anything else? I'll fix up the typos later, yeah, yeah, sure, yeah, good one.
[00:34:30.110 - 00:34:42.110] Yeah, so James Trevelyan, he talks about this as actually one of the other main reasons why projects fail is that during those technical requirement discussions,
[00:34:42.110 - 00:34:49.110] the engineers actually can't communicate and understand what the person actually wants.
[00:34:49.110 - 00:34:57.110] Now, some people view it the other way is that it's actually up to the customer or the client to explain what they want,
[00:34:57.110 - 00:35:06.110] but it's actually a two-way thing, is that if the engineer doesn't understand, they should be asking more questions, yeah, cool.
[00:35:06.110 - 00:35:34.260] Yeah, heaps more, yeah, one at the back there. If you neutralize, oh yeah, sure, yes, so shutting people down, yeah, cool, yep, yep, yeah, sure.
[00:35:54.750 - 00:36:14.200] So we'll talk a little about that next week as well. There's a bias called guru bias, which talks about, sorry, I'll just type this out,
[00:36:14.200 - 00:36:26.200] where there's a view that someone who is more experienced and is seen as the technical expertise, they're the holder of the truth, and that's not always true.
[00:36:26.200 - 00:36:30.200] Oh, good one, a few more, yeah.
[00:36:30.200 - 00:37:01.050] Oh yeah, yep, anything else, a couple more, squeeze a few more in, yeah, yeah, sure.
[00:37:01.050 - 00:37:11.050] Yeah, it's a tricky one too because sometimes you actually want to give some work or tasks to someone to actually help them develop as an engineer,
[00:37:11.050 - 00:37:17.050] otherwise they kind of get pigeonholed into being, you know, the expert in this particular thing.
[00:37:17.050 - 00:37:27.050] Now, what's interesting is that sometimes actually they want to be that expert in that thing, but maybe they don't, they're getting sick of being pigeonholed into that, yeah, last one.
[00:37:27.050 - 00:38:00.350] Yeah, sure, this is interpreted, yep, cool, very good, all right, so yeah, all sorts of good stuff there.
[00:38:01.350 - 00:38:10.350] Okay, so yeah, and look, those that you shared with me, that's your experiences, right?
[00:38:10.350 - 00:38:21.350] And yeah, it happens a lot, okay, so hopefully it won't happen later on in the semester with your group assignment,
[00:38:21.350 - 00:38:26.350] but you know, you need to try and bring in some processes to really help with this.
[00:38:26.350 - 00:38:38.350] So this is the way, or one of the approaches that I like to apply when I think about collaboration, okay, a mate of mine in Melbourne, he calls me the engineer's engineer,
[00:38:38.350 - 00:38:49.350] and so I view collaboration as a bit of a process, okay, so you have this input, process and an output.
[00:38:49.350 - 00:38:59.350] And sure enough, there's actually some literature, research to actually suggest that that's probably a good way of looking at it.
[00:38:59.350 - 00:39:12.350] Okay, so on the left-hand side, you've got your inputs, so the task design, so you know, what does the group look like, who are they, what are their experiences,
[00:39:12.350 - 00:39:19.350] what is the task that they have to do, and then you've got all these contextual or environmental factors that already exist.
[00:39:19.350 - 00:39:27.350] Okay, then you've got your processes for collaboration, how are you going to deal with conflict, how are you going to communicate with each other.
[00:39:27.350 - 00:39:35.350] There might be some external processes, maybe your company actually has got some stuff on how you can actually work together.
[00:39:36.350 - 00:39:52.350] And you also have yet ways of working, okay, or group traits that emerge, okay, and you won't know those until you actually start to work together.
[00:39:53.350 - 00:40:11.350] Okay, and from that comes, hopefully, effective performance, as well as, you know, behavioral outcomes, okay, so that can include people wanting to stay in their job, okay, or go on to the next project.
[00:40:11.350 - 00:40:26.350] Or unfortunately, sometimes it can actually lead to people leaving, okay, so I do a lot of research on why engineers stay and leave the profession, as well, and this does come up.
[00:40:26.350 - 00:40:31.350] Yeah, hopefully, I've got a bit of time, again, through the semester to show you some of that.
[00:40:32.350 - 00:40:43.350] Okay, one of the things that I also like to think about is when you're looking at processes, what are the things that you can control, and what are the things that you can influence.
[00:40:43.350 - 00:40:49.350] There's some things that you can never influence or control, okay, and you just have to kind of let it go.
[00:40:49.350 - 00:41:17.350] This is one of those things, okay, so for example, someone's level of introversion versus extroversion, okay, so if they want to keep to themselves or be really outspoken, good luck trying to change that, okay, that is an individual trait that is probably locked in for life, okay, so good luck trying to change that.
[00:41:18.350 - 00:41:39.350] But there's some things that you can control and influence, so you can certainly control things like task design, the composition of the group, things that you can influence is, you know, during group work is, you know, how you're actually going to get on with each other.
[00:41:40.350 - 00:41:59.350] No one solved this problem, okay, so, yeah, if we knew the solution to perfect teamwork, we would have told you by now. We don't know what it is, okay, but it's something to keep working on.
[00:42:00.350 - 00:42:25.350] Another good way that I like to look at it is the task relationship process triangle, okay, so if you, and these are all reflected in that diagram also on the left-hand side, if you don't define what you need to do, nothing can happen.
[00:42:25.350 - 00:42:54.350] Without relationships, nothing can happen, okay, and if you don't have the processes right, nothing can happen, okay, so usually when an engineering or any project collaboration, if it breaks down, it's because one or two of these things are broken, okay, so, yeah, I'll give you an example about 10 years ago, I remember,
[00:42:56.350 - 00:43:16.350] I was working on a project, a meeting was called to try and resolve it, okay, and I quickly realized that during the meeting, I had one person over here ripping into this engineer over here because they thought that this engineer was not technically competent,
[00:43:18.630 - 00:43:42.630] and it's like, oh, because they'd found all sorts of errors in their work, and it's like, oh, wow, okay, so I kind of had to dial things down a little bit, and the problem was, this person had no idea who this person was, the first thing that they did in this relationship was attack each other,
[00:43:43.630 - 00:43:52.630] okay, they'd communicated via email, and then when it came face-to-face, they just started to tear shreds, I was like, this is not good.
[00:43:53.630 - 00:44:11.630] Now, I had to do some relationship repair work later on, but what I'd also realized during that discussion was that there was a process problem, okay, that this person over here saw this engineer's work as not being up to standard,
[00:44:12.630 - 00:44:32.630] but we actually didn't have a quality assurance or control process to make sure that that work was checked before it went up to the next person, okay, and if we had that process right, this performance would have been so much better, okay, and we would have protected that relationship as well.
[00:44:33.630 - 00:44:58.170] So, post-meeting, first thing I did, well, got to sort out this relationship problem, that took a couple months to build back up, okay, but I made sure that we had some really good quality processes in place to make sure, so it's just like an internal review process to make sure that that didn't happen again, okay.
[00:44:58.170 - 00:45:26.170] Yeah, so the justification for doing any engineering project is focused on an outcome, okay, not an output like a deliverable, okay, so in order to understand what the outcome is, you need to build relationships and communicate with key stakeholders, and it's only when you've got established some really strong foundations, that's when you start to build trust, okay.
[00:45:27.170 - 00:46:08.890] But what does trust look like? What does a trustworthy person look like to you? Any suggestions? Yeah, yep, yep, so yeah, dependable, reliable, what else, yep, respectful, what else, yep, open and honest, yeah, that they can or can't do the work, yep, for sure, yeah, happens a lot, right, as people say, yeah, I can do this, and they go, no, they can't, yep.
[00:46:09.890 - 00:46:31.190] Open to criticism, yep, cool, okay, other things could be legitimate, credible, fair, known for doing quality work, and so on, okay, and that trust in someone actually can take years to develop, okay.
[00:46:32.190 - 00:46:42.980] So yeah, as I said, without relationships, nothing can happen in engineering, and relationships are built on trust, okay.
[00:46:45.980 - 00:47:00.360] Yeah, and coming back to the podcast a little bit too, understanding culture is the key to great results in engineering, okay.
[00:47:00.360 - 00:47:08.360] So when we're talking about trust as well, there's a term that we use called a social license, or a social license to operate.
[00:47:09.360 - 00:47:24.250] We've got a guest lecturer coming in next week, and he's actually going to talk a little bit about the social license to operate, okay, so yeah, keep that little triangle in mind, I use it quite regularly.
[00:47:26.820 - 00:47:46.820] Okay, so some closing words, collaboration is typically the number one skill that employers look for, okay, so your technical skills, employers will know that a graduate from UC's got it in spades, okay.
[00:47:47.820 - 00:47:55.820] What can differentiate you from everyone else is making your collaboration expertise awesome, okay.
[00:47:56.820 - 00:48:10.820] So you've got about 15 months left, maybe some of you a little bit longer, a little bit shorter, left to develop those collaboration performances in a really safe environment before you become a graduate engineer.
[00:48:11.820 - 00:48:20.820] As I said, pick up the phone and go and speak to someone, go and see them, buy them a coffee, okay, these are the ways that relationships are built.
[00:48:21.820 - 00:48:38.820] For the sustainability assignment that's coming up, again, within this I'm actually going to do a bit of a peer assessment task, okay, so I'm going to get you all to set the criteria for what good collaboration actually looks like,
[00:48:39.820 - 00:48:50.820] and you'll get to score each other on that. I'm going to have two points of peer feedback, okay, so early on in the assignment, so you can actually respond to that, hopefully improve,
[00:48:51.820 - 00:49:03.820] and then do it again the second time around, and I can use that to adjust your assignment grade based on what your peers think of you and your collaboration performance.
[00:49:04.820 - 00:49:15.820] Okay, so next week we've got a guest lecturer coming in, so Andrey Conninger from Meridian Energy, he's going to talk about Marley Perspectives and Engineering.
[00:49:16.820 - 00:49:27.820] Kahoo Jones, a fourth year computer engineering student who did his summer internship with Meridian, he's going to join Andrey in that presentation.
[00:49:28.820 - 00:49:33.820] And then next week, next Friday, we'll talk about bias, diversity and ethics.
[00:49:34.820 - 00:49:44.820] Just a reminder, you've got your bi-cultural competence and confidence workshops over the next couple of weeks, you only need to go to one of those, two-hour workshop.
[00:49:45.820 - 00:49:57.820] So if you haven't already allocated yourself to tutorial A or B, please do so by Monday morning, otherwise I'll be allocating you automatically.
[00:49:58.820 - 00:50:07.820] Okay, so that's all we have for this week, a couple of references if you want to have a look at it. Have an awesome Friday and enjoy your weekend.
[00:50:08.820 - 00:50:34.780] Okay, Maris, see you.
[00:50:37.990 - 00:50:38.990] All right, see you later.
[00:51:07.900 - 00:51:09.900] Hey.
[00:51:37.900 - 00:51:39.900] Ed Norris, stay here.
[00:52:07.900 - 00:52:09.900] Thank you.
[00:52:37.900 - 00:52:39.900] Thank you.

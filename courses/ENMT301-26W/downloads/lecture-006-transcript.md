# ENMT301-26W Lecture 06 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_06_audio_16k_mono_32k.mp3`
Source audio SHA-256: `7e352fc1599909c72d0acb6463d6399967bc10fd70a48587efb88c20cab854d2`
Generated: 2026-06-06T05:05:44.820097+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:26 - 00:00:28] Alright, thanks everyone, we'll make a start there.
[00:00:28 - 00:00:54] Alright, thanks everyone, we'll make a start there.
[00:00:54 - 00:00:56] Alright, thanks everyone, we'll make a start there.
[00:00:56 - 00:00:58] Cool.
[00:00:58 - 00:01:01] As you're ongoing, first week pretty much done.
[00:01:01 - 00:01:03] Thumbs up, that's what I'd like to see.
[00:01:03 - 00:01:06] Hopefully you have an exciting Friday late afternoon,
[00:01:06 - 00:01:08] slash weekend planned for after this,
[00:01:08 - 00:01:11] but the idea is that by the end of this tutorial
[00:01:11 - 00:01:14] we have basically a really, really good understanding of
[00:01:14 - 00:01:17] at least what the tasks are that we need to do for this design assignment.
[00:01:17 - 00:01:20] So hopefully we can kind of get stuck into it,
[00:01:20 - 00:01:25] and then avoid having the chaos that might kind of occur later in the tomb.
[00:01:25 - 00:01:29] Has anyone seen when the first one A for this is due?
[00:01:29 - 00:01:37] Sometimes you get, does anyone know what it is?
[00:01:37 - 00:01:43] So if you go on learn, and you go under the
[00:01:43 - 00:01:48] assessment tab, you'll see that it sort of stays there as well.
[00:01:48 - 00:01:52] So, 20 or 12, the third, so that's about roughly a month's time.
[00:01:52 - 00:01:55] So, it's slightly less.
[00:01:55 - 00:01:57] So, it seems like a long time away,
[00:01:57 - 00:02:01] but there's no reason why you couldn't have this, you know,
[00:02:01 - 00:02:05] a week early, quite easily.
[00:02:05 - 00:02:06] Cool.
[00:02:06 - 00:02:12] So, as you can see on the slide, there is this B-VOC poll.
[00:02:12 - 00:02:15] Has anyone had to go at filling that out and saying what time
[00:02:15 - 00:02:19] they might want to have this kind of drop in the session?
[00:02:19 - 00:02:24] If you haven't, I'll give you a quick moment just to scan the QR code
[00:02:24 - 00:02:26] or take a photo of that.
[00:02:26 - 00:02:28] But essentially what this is, as we've talked about,
[00:02:28 - 00:02:32] is an opportunity to have informal office hours,
[00:02:32 - 00:02:35] rather than being formal in my office.
[00:02:35 - 00:02:38] There'll be in the FOIA of the EPA's library.
[00:02:38 - 00:02:41] That'll be an opportunity for people to click their aluminium strips
[00:02:41 - 00:02:43] if they haven't already, and they want to,
[00:02:43 - 00:02:48] or to ask any questions that they didn't feel comfortable with asking in class.
[00:02:48 - 00:02:53] All during the tutorials that I've signed popped up afterwards.
[00:02:53 - 00:03:02] So, if I have a look, you can see that it looks like at this stage,
[00:03:02 - 00:03:05] Monday morning, there's going to be the winner.
[00:03:05 - 00:03:07] But I guess I'll leave that.
[00:03:07 - 00:03:09] I'll leave that open.
[00:03:09 - 00:03:11] If someone's away, or you're watching this on,
[00:03:11 - 00:03:12] I'll leave it open.
[00:03:12 - 00:03:15] I'll check it on Monday, I guess.
[00:03:15 - 00:03:18] But then I'll have to make a post on Monday about when it is.
[00:03:18 - 00:03:21] If people are going to come on Monday.
[00:03:21 - 00:03:24] But as I said, I'll make it only be half an hour
[00:03:24 - 00:03:27] if I'm getting heaps of questions, then I'll stay for longer.
[00:03:27 - 00:03:32] But at least we'll make it quite clear for everyone.
[00:03:32 - 00:03:34] So, keep answering away.
[00:03:34 - 00:03:36] If you haven't, I'll leave it open for a week while.
[00:03:36 - 00:03:39] Cool. So, notice how many people are still looking for partners?
[00:03:39 - 00:03:41] Cool. So, if you're still looking for partners,
[00:03:41 - 00:03:43] you could have linked it out with other people.
[00:03:43 - 00:03:47] They put their hand up, or you can use the forum that is on the website.
[00:03:47 - 00:03:52] Learn, or you can kind of hang around here and ask each other
[00:03:52 - 00:03:54] if you want to become partners at the end of it.
[00:03:54 - 00:03:58] But obviously, that's one of the tasks that will need to be
[00:03:58 - 00:04:02] completed before you can undertake the assignment.
[00:04:02 - 00:04:03] Now, the Easter egg winner's.
[00:04:03 - 00:04:08] Three people emailed me the correct answers of who it was.
[00:04:08 - 00:04:13] And I do have a little prize for them.
[00:04:13 - 00:04:16] Hopefully they're not lactose intolerant.
[00:04:16 - 00:04:19] So, I can get another gift.
[00:04:19 - 00:04:21] Let's see. We're going to do it.
[00:04:21 - 00:04:22] So, I've got...
[00:04:22 - 00:04:24] I guess they'll know who they are.
[00:04:24 - 00:04:28] So, Marco Anthony and Michael were either of you guys here.
[00:04:28 - 00:04:31] I got one over there.
[00:04:31 - 00:04:38] If you want to come down to collect your prizes,
[00:04:38 - 00:04:40] anyone else in you have other people?
[00:04:40 - 00:04:42] I can see how good my...
[00:04:42 - 00:04:44] Are you not lactose intolerant?
[00:04:44 - 00:04:45] Okay.
[00:04:45 - 00:04:49] One and two. I guess it's honesty. I'm not going to do...
[00:04:49 - 00:04:51] Not going to do that.
[00:04:51 - 00:04:53] Oh, it's pretty good.
[00:04:53 - 00:04:55] All right.
[00:04:55 - 00:04:57] Pretty good. Well done.
[00:04:57 - 00:05:00] So, for those who didn't know who the random names were,
[00:05:00 - 00:05:01] there was...
[00:05:01 - 00:05:04] Calvin Harris and Diplo, I think, right?
[00:05:04 - 00:05:07] Yeah. So, obviously, I have to make the spiritual existence.
[00:05:07 - 00:05:11] So, I've put in a measure that I'm teaching famous DJs,
[00:05:11 - 00:05:13] but, you know, I'll probably stop talking there
[00:05:13 - 00:05:16] because there's a few rabbit holes I could go down.
[00:05:16 - 00:05:19] Notice number three is the notice just about testing of your aluminium.
[00:05:19 - 00:05:26] So, obviously, some of you guys will have collected your aluminium strips.
[00:05:26 - 00:05:27] And you...
[00:05:27 - 00:05:30] Who have asked, oh, when are we timetable to test them?
[00:05:30 - 00:05:31] That's not how this kind of works.
[00:05:31 - 00:05:33] You guys are the bosses.
[00:05:33 - 00:05:36] So, you can test it when the lab is open,
[00:05:36 - 00:05:39] but it's up to you that they're into your schedule
[00:05:39 - 00:05:42] to kind of make your dog bones and to kind of complete that.
[00:05:42 - 00:05:44] So, hopefully that's kind of clear.
[00:05:44 - 00:05:46] If you don't have aluminium, obviously you'll be able to pick it up.
[00:05:46 - 00:05:48] And the drop-in session on Monday,
[00:05:48 - 00:05:51] or at the end of the tutorials on Tuesday.
[00:05:51 - 00:05:57] But I think about half of the people have sort of collected their aluminium already.
[00:05:57 - 00:05:58] Cool.
[00:05:58 - 00:06:03] Is everyone sort of aware of what we went through pretty quickly in the last Tuesday?
[00:06:03 - 00:06:05] What we actually needed to go through for the testing?
[00:06:05 - 00:06:09] Is everyone kind of clear what it is that they actually need to do for that
[00:06:09 - 00:06:13] what testing entails?
[00:06:13 - 00:06:15] Is there one person that's a little bit of Fiona?
[00:06:15 - 00:06:17] Just give me a little, I echo.
[00:06:17 - 00:06:22] So, essentially, what we can do is,
[00:06:22 - 00:06:27] I mentioned in this slide that there was a specific standard that could be followed.
[00:06:27 - 00:06:32] Things like ASTM E8 or something with a very memorable name like that.
[00:06:32 - 00:06:35] And obviously that standard requires you to do dog bones.
[00:06:35 - 00:06:42] It should be linear section where the thick area.
[00:06:42 - 00:06:45] The standard size at this bit here needs to be 50mm.
[00:06:45 - 00:06:50] So, it's sort of mentioned in the tutorial that's quite hard to do with what only got 20mm strips.
[00:06:50 - 00:06:57] So, as we sort of showed there are different ways that you can go about it.
[00:06:57 - 00:07:05] That you will have to basically make your own dog bone shaped kind of
[00:07:05 - 00:07:06] components.
[00:07:06 - 00:07:08] And the idea is that you know this length.
[00:07:08 - 00:07:13] Well, this will work here so that you can work out what the stress area is and then get all of your things from there.
[00:07:13 - 00:07:17] So, obviously this bit here is going to be 20mm.
[00:07:17 - 00:07:22] Does anyone know what the size of the pinholes were for the houndsville tin some of the grips?
[00:07:22 - 00:07:23] 8mm.
[00:07:23 - 00:07:24] 8mm.
[00:07:24 - 00:07:26] So, we can just do this.
[00:07:26 - 00:07:27] So, this is 8mm.
[00:07:27 - 00:07:29] So, how much would be either side?
[00:07:29 - 00:07:30] 12mm.
[00:07:30 - 00:07:32] Like 12mm here.
[00:07:32 - 00:07:43] So, you probably want this one here to be smaller than 12mm.
[00:07:43 - 00:07:47] Yeah.
[00:07:47 - 00:07:49] Less than 12mm, more than 12mm.
[00:07:49 - 00:07:50] Yeah.
[00:07:50 - 00:07:54] So, if we make this bit here like 15 or something, then it's just going to break with us.
[00:07:54 - 00:07:58] It depends on then we don't necessarily get anything useful.
[00:07:58 - 00:07:59] Cool.
[00:07:59 - 00:08:00] Hopefully that's kind of clear.
[00:08:00 - 00:08:02] People often ask, how do I make that?
[00:08:02 - 00:08:06] I would just describe what they're just kind of liners.
[00:08:06 - 00:08:08] You're going to have to come up with your rough dimensions.
[00:08:08 - 00:08:10] You kind of want to make them smaller than not too small.
[00:08:10 - 00:08:11] That there's a stress concentration.
[00:08:11 - 00:08:15] Remember how we sort of talked about if this eventually just comes a notch?
[00:08:15 - 00:08:20] So, we want to have some kind of region where it is the same kind of dimension of the whole way.
[00:08:20 - 00:08:28] And ideally we get our kind of failure occurring in that linear sections that we know that's not due to some stress concentration from the radius
[00:08:28 - 00:08:31] or some stress concentration from our whole.
[00:08:31 - 00:08:32] Cool.
[00:08:32 - 00:08:36] So, there's a task that if you've got your aluminium strips, you pretty much can do.
[00:08:36 - 00:08:42] Whenever you want, I think there is files in those big A-frame.
[00:08:42 - 00:08:46] So, you know, if you want to make some strips over the weekend, I feel like there's no reason why you couldn't.
[00:08:46 - 00:08:49] I guess it's what I'm sort of saying.
[00:08:49 - 00:08:53] So, up to you how many you do think like a minimum of three is probably what I'd say.
[00:08:53 - 00:08:56] But sometimes you might have some tests that don't really go to plan.
[00:08:56 - 00:08:59] You might have to retest them or you might get some variations.
[00:08:59 - 00:09:02] So, you might cross that bridge as you get to it.
[00:09:02 - 00:09:04] Cool.
[00:09:04 - 00:09:08] So, from there, is there any questions about that before I keep kind of going?
[00:09:08 - 00:09:15] I realise that we know about like super rapidly because I was like, I just want to make sure I get through all the slides and I don't have to start this lecturing like,
[00:09:15 - 00:09:17] oh those slides that I didn't get over there.
[00:09:17 - 00:09:18] Yep.
[00:09:18 - 00:09:30] Yep. So, you're talking about like, later down the track, if you want to test your stress concentration.
[00:09:30 - 00:09:31] Yes.
[00:09:31 - 00:09:40] So, you could later on the track. I'll just say like, you know, we'll talk about this next week when we go over stress concentrations and then affect that stress concentrations.
[00:09:40 - 00:09:50] Often, if we're brittle materials, we've got a ductile material so it's going to make us have to have some sort of experimental or approximation.
[00:09:50 - 00:09:57] You could be confident that I reckon the K-value is this and then hopefully it is.
[00:09:57 - 00:10:06] Okay, later down the piece, if you have designed your stress concentration, you could do another mini type tensile test to check with a,
[00:10:06 - 00:10:11] what you've assumed for your K-value is appropriate and then you could adjust your design to go from there.
[00:10:11 - 00:10:18] But I'm not going to draw that just because then people might start doing that before they've done the baseline material testing.
[00:10:18 - 00:10:19] Cool. Any other questions?
[00:10:19 - 00:10:20] Really good question.
[00:10:20 - 00:10:25] Right.
[00:10:25 - 00:10:26] So, back to the slides.
[00:10:26 - 00:10:30] So, you kind of keep me on track.
[00:10:30 - 00:10:33] So, today we'll be focusing on your burning questions you have.
[00:10:33 - 00:10:35] Got an example calculation to do.
[00:10:35 - 00:10:41] We'll discuss what possible designs and shapes are available and what I kind of recommend not doing, I guess.
[00:10:41 - 00:10:43] More than, I mean, yeah.
[00:10:43 - 00:10:44] All right.
[00:10:44 - 00:10:46] One particular design I recommend not doing.
[00:10:46 - 00:10:50] We'll do a sample calculation of different designs.
[00:10:50 - 00:10:57] There's big questions at the end and then if we have time, probably go over some oil or buckwing revision.
[00:10:57 - 00:10:58] Cool.
[00:10:58 - 00:11:03] So, with that, are there any further questions that you have?
[00:11:03 - 00:11:08] Yep.
[00:11:08 - 00:11:13] So, in terms of the material testing lab you've been inducted as long as you've kind of watched those videos.
[00:11:13 - 00:11:18] I think there's also like a basic, basic testing procedure that's been outlined.
[00:11:18 - 00:11:23] So, if you go in a Summit one on Learn, you'll see down the bottom.
[00:11:23 - 00:11:28] We've got these videos which kind of show you how to use it.
[00:11:28 - 00:11:37] And then there should be somewhere in this basic testing procedure which kind of tells you things that you might want to make sure that you do.
[00:11:37 - 00:11:54] So, if you're really unsure of this should kind of guide you, but if you go in here and show an Oscar's beard then you could just say, hey, we've got this and having this problem or you probably, if you're the first person, then you might have to see where they're kind of computer that you're operating in that right software is opening that sort of thing.
[00:11:54 - 00:11:59] But obviously, remember that you need to bring like a USB drive to kind of get your results.
[00:11:59 - 00:12:06] So, there'll be a note that I'll do because there's nothing worse than being all good to go and then not know how you can save your data.
[00:12:06 - 00:12:11] And I'm not sure if those computers are connected to it and it's not similar to that, but funny.
[00:12:11 - 00:12:13] That's good question.
[00:12:13 - 00:12:15] Any other questions?
[00:12:15 - 00:12:25] So, the other thing I was just going to show, I can't remember what I was planning on doing this earlier or later, but under the aluminium assignment tab,
[00:12:25 - 00:12:32] I think I mentioned it that there is a frequently asked question box somewhere.
[00:12:32 - 00:12:38] Oh, does it hit him?
[00:12:38 - 00:12:39] Oh, maybe it is?
[00:12:39 - 00:12:40] Is it hit him?
[00:12:40 - 00:12:43] Is it?
[00:12:43 - 00:12:45] No, it would be in here.
[00:12:45 - 00:12:46] Okay, that's good for me.
[00:12:46 - 00:12:56] When we have it like strict right in the middle, I'll like make it visible, but there's like a frequently asked question sort of thing that I've already kind of compiled from previous years questions.
[00:12:56 - 00:13:07] Hopefully, avoid the same questions coming through, so that if you have the same question, you can see the answer there rather than emailing me and having me have to email back and then put it on this.
[00:13:07 - 00:13:13] But there might be some new questions that kind of come up and then I'll still put them up there and say that it's been updated and the lecture.
[00:13:13 - 00:13:18] But yeah, I must have not heard in it.
[00:13:18 - 00:13:19] Cool.
[00:13:19 - 00:13:21] Any other burning questions?
[00:13:21 - 00:13:28] Cool.
[00:13:28 - 00:13:36] At the end of the last tutorial, we did a very quick fire or rapid version of our planning slash task review route.
[00:13:36 - 00:13:47] So if I get it up on the document camera on one of the sides, we can see that depending on what tutorial we're on, we kind of wrote the same thing.
[00:13:47 - 00:14:00] So just to you know, speaking, if I go into this, we can see there were some sort of like initial work.
[00:14:00 - 00:14:06] Which, you know, there's no reason why you couldn't have completed quite early next week.
[00:14:06 - 00:14:14] When it comes to sketching your designs and doing the calculations, we'll kind of make a start on discussing that today.
[00:14:14 - 00:14:19] So that there's no reason that you couldn't basically make a good start of that over the weekend.
[00:14:19 - 00:14:21] Material testing was sort of talked about.
[00:14:21 - 00:14:29] We've actually already talked about the fact that there are two types of material testing that you might be doing, but just getting a basic material properties is probably going to be.
[00:14:29 - 00:14:32] good in the first instance.
[00:14:32 - 00:14:35] Then obviously there's a report drawing and time sheet.
[00:14:35 - 00:14:39] As you go, there will also be kind of required, right?
[00:14:39 - 00:14:51] Now what we had is what we had said is that that is basically a list that has been made following information that was actually on the assignment brief front.
[00:14:51 - 00:14:55] So if I switch my screen again.
[00:14:55 - 00:15:04] I'm not going to download it this time, but on this page here, there are some suggested steps to follow.
[00:15:04 - 00:15:06] Alright.
[00:15:06 - 00:15:12] Now with that here, we can see that the first step here, say, is to determine the ultimate material strength and young's modulus.
[00:15:12 - 00:15:17] Funscaling your test data and your own results and from other sources, if you want, you don't have to.
[00:15:17 - 00:15:19] You could just trust your own.
[00:15:19 - 00:15:23] To do this, you need to make your samples.
[00:15:23 - 00:15:35] The question for you guys is, if you haven't done that, can you do number three?
[00:15:35 - 00:15:37] So I think I've done the like double negative thing.
[00:15:37 - 00:15:44] So like, must you do number one to do number three?
[00:15:44 - 00:15:46] And you want to go out on the loan?
[00:15:46 - 00:15:47] Yes, no.
[00:15:47 - 00:15:51] You can be right or can be wrong.
[00:15:51 - 00:15:52] Some people think yes, let's say.
[00:15:52 - 00:15:53] Who runs?
[00:15:53 - 00:15:56] You have to do material testing before you do any calculations.
[00:15:56 - 00:15:58] It was a yes and it doesn't stick to the handout.
[00:15:58 - 00:15:59] Few people.
[00:15:59 - 00:16:02] And if you're looking at the same time, you don't have to do it.
[00:16:02 - 00:16:03] Cool.
[00:16:03 - 00:16:04] And then some people are like, oh, I feel like you're just drinking.
[00:16:04 - 00:16:06] So I'm just not going to answer.
[00:16:06 - 00:16:07] Fair enough.
[00:16:07 - 00:16:12] Sometimes that can be devious like that, I guess.
[00:16:12 - 00:16:18] What I'm trying to say is that if I was to think about it like a block diagram,
[00:16:18 - 00:16:25] I've got one block, which is how I'm just going to call material testing.
[00:16:25 - 00:16:35] So this is like UTS, maybe you're yield, maybe you're young's modulus,
[00:16:35 - 00:16:39] maybe the stress concentration factor, right?
[00:16:39 - 00:16:42] And so that is the task that will needs to be done.
[00:16:42 - 00:16:52] Over here, we have, I'm going to say initial design.
[00:16:52 - 00:16:56] So what do we think that their initial design might encompass?
[00:16:56 - 00:16:59] Yeah, okay.
[00:16:59 - 00:17:09] So I'm going to say shape, shape, slash number of members.
[00:17:09 - 00:17:10] Any?
[00:17:10 - 00:17:11] Cool.
[00:17:11 - 00:17:15] From there, what would the next thing be to do?
[00:17:15 - 00:17:22] Now, when you guys were in inch 102, doing the structures part of it,
[00:17:22 - 00:17:26] did you have Charlie, Charles?
[00:17:26 - 00:17:30] Like, this should fish, man?
[00:17:30 - 00:17:31] No?
[00:17:31 - 00:17:32] No?
[00:17:32 - 00:17:33] Okay.
[00:17:33 - 00:17:34] Wow.
[00:17:34 - 00:17:38] You must have stopped doing that course, but I have like burned in my brain
[00:17:38 - 00:17:42] and saying, you guessed it, draw a free body diagram.
[00:17:42 - 00:17:44] And that's pretty much what you'll do here.
[00:17:44 - 00:17:45] You guessed it.
[00:17:45 - 00:17:49] Draw a free body diagram, because once you have your shape,
[00:17:49 - 00:17:52] then that's going to dictate what the forces are on the member,
[00:17:52 - 00:17:55] based on something else that we needed to find.
[00:17:55 - 00:17:58] What else do we need to know if we're going to do our free body diagram?
[00:17:58 - 00:18:09] Yeah, yeah, yeah, yeah, yeah.
[00:18:09 - 00:18:16] I'll say target, failure, mass.
[00:18:16 - 00:18:17] Yeah?
[00:18:17 - 00:18:20] So obviously you need to know, like, when it breaks,
[00:18:20 - 00:18:22] what was the force on this member?
[00:18:22 - 00:18:25] And then you'll use that to know, I want the force and this member
[00:18:25 - 00:18:29] to make the stress on the member be such that it breaks.
[00:18:29 - 00:18:30] Yeah?
[00:18:30 - 00:18:31] Cool.
[00:18:31 - 00:18:32] So that sort of stuff.
[00:18:32 - 00:18:35] You can do without doing any of that, sir.
[00:18:35 - 00:18:38] Yeah?
[00:18:38 - 00:18:43] Following that, we're going to have, I'm going to say,
[00:18:43 - 00:18:54] dress slash failure analysis.
[00:18:54 - 00:18:59] So what do we think that this would incorporate,
[00:18:59 - 00:19:06] what kind of calculations might we do sort of in there, right?
[00:19:06 - 00:19:23] So I'm going to say stress, each, how will our,
[00:19:23 - 00:19:26] how will our compressors be in this likely fails?
[00:19:26 - 00:19:29] Could be stress, but unlikely.
[00:19:29 - 00:19:32] Buckling, so I'm going to write buckling there.
[00:19:32 - 00:19:33] Cool.
[00:19:33 - 00:19:40] No, I'm going to write, maybe I'm going to write stress concentration
[00:19:40 - 00:19:41] failure.
[00:19:41 - 00:19:45] I don't miss with that.
[00:19:45 - 00:19:48] I don't miss with that next, to be honest.
[00:19:48 - 00:19:56] So I just say, plus other chain of rule failure.
[00:19:56 - 00:20:00] Cool.
[00:20:00 - 00:20:04] So from that, you're probably going to want some information,
[00:20:04 - 00:20:05] right?
[00:20:05 - 00:20:09] So for your buckling, what value do you need it for buckling?
[00:20:09 - 00:20:16] I'll give you a hint.
[00:20:16 - 00:20:21] It's one of these four things here.
[00:20:21 - 00:20:28] Is buckling based on stress?
[00:20:28 - 00:20:29] 50, 50.
[00:20:29 - 00:20:30] Who reckons?
[00:20:30 - 00:20:32] Yes.
[00:20:32 - 00:20:33] Who reckons?
[00:20:33 - 00:20:34] No.
[00:20:34 - 00:20:35] Cool.
[00:20:35 - 00:20:37] It were not feeling very engaged.
[00:20:37 - 00:20:38] That's a Friday afternoon.
[00:20:38 - 00:20:39] It's hot.
[00:20:39 - 00:20:40] You wish you had the beach, I do too.
[00:20:40 - 00:20:44] But buckling is due to our young's modulus, right?
[00:20:44 - 00:20:51] It's a ratio based on basically how long our memorize based on how
[00:20:51 - 00:20:52] I'm flexible it is.
[00:20:52 - 00:20:54] We'll go over there in a little bit to detail later.
[00:20:54 - 00:20:55] Cool.
[00:20:55 - 00:20:59] So if you don't know young's modulus, though, does that just mean
[00:20:59 - 00:21:04] you can't do any buckling calculations?
[00:21:04 - 00:21:08] Or can we roughly make an approximate and then update it later?
[00:21:08 - 00:21:09] Yes.
[00:21:09 - 00:21:14] And so four, four metals, generally speaking, is there much
[00:21:14 - 00:21:16] variation in our young's modulus?
[00:21:16 - 00:21:19] Maybe it's something you're not sure.
[00:21:19 - 00:21:21] Maybe, you know, if you ask, oh, it will be our failure.
[00:21:21 - 00:21:23] I'm guessing that's what people use for Google these days.
[00:21:23 - 00:21:28] But generally speaking, if you just looked up, what is the young's
[00:21:28 - 00:21:31] modulus range for L-minium?
[00:21:31 - 00:21:33] Then you'd probably at least get a range there.
[00:21:33 - 00:21:36] And if you wanted to be conservative, you could pick the one that
[00:21:36 - 00:21:38] had the worst effect on the buckling, right?
[00:21:38 - 00:21:40] And then you could update that later if you didn't have that value.
[00:21:40 - 00:21:44] But it means that what I'm trying to say is that it's no reason why you
[00:21:44 - 00:21:47] can not do any buckling calculations, even if you don't have that
[00:21:47 - 00:21:49] from your material testing it, right?
[00:21:49 - 00:21:51] And it's just an easy sub-identulator.
[00:21:51 - 00:21:53] I assumed it was 60.
[00:21:53 - 00:21:57] Now it's 70 or I don't know, 50 or whatever it is, yeah?
[00:21:57 - 00:21:59] Cool.
[00:21:59 - 00:22:04] Similarly, I guess the point I'm trying to make there is that we're
[00:22:04 - 00:22:06] not designing a thing to buckle.
[00:22:06 - 00:22:09] So there's going to be kind of like a factor of safety in there.
[00:22:09 - 00:22:12] Anyway, there's going to be a bit of fat there so that we know
[00:22:12 - 00:22:15] that unless we're trying to go for like the most risky shrink
[00:22:15 - 00:22:18] to weight ratio, then obviously it becomes pretty important that
[00:22:18 - 00:22:20] you've got that number for E-dilden.
[00:22:20 - 00:22:25] But 50 to 80% of people will just go, ah, I'm just going to make
[00:22:25 - 00:22:27] my eye being way bigger than it needs to be.
[00:22:27 - 00:22:29] Or my TV or whatever it is.
[00:22:29 - 00:22:31] So I know it definitely doesn't buckle.
[00:22:31 - 00:22:33] Yeah?
[00:22:33 - 00:22:34] Cool.
[00:22:34 - 00:22:39] And then similarly for our stress analysis, do we think that
[00:22:39 - 00:22:44] do we have to have our failure stress-y to row?
[00:22:44 - 00:22:46] We put our use-face or our yield.
[00:22:46 - 00:22:49] Do we have to have that to be able to do that calculation?
[00:22:49 - 00:22:51] We'll see if you check the head.
[00:22:51 - 00:22:53] We probably want to if we want to work out what our kind of factor
[00:22:53 - 00:22:54] of safety is.
[00:22:54 - 00:22:57] So for our butts that we don't want to fail, right?
[00:22:57 - 00:23:01] So if you did your bearings stress calculation with the punters,
[00:23:01 - 00:23:03] you can work out what that stress value is.
[00:23:03 - 00:23:06] And you could just you could just hold fire and wait until
[00:23:06 - 00:23:09] you've got your yield or your ultimate tensile stress for your
[00:23:09 - 00:23:10] factor of safety.
[00:23:10 - 00:23:13] And then do that last bit of working where you work out the factor of
[00:23:13 - 00:23:14] safety next, right?
[00:23:14 - 00:23:18] The only point where it's going to become important is when you do
[00:23:18 - 00:23:25] your I'm going to call it stress concentration failure.
[00:23:25 - 00:23:26] Right?
[00:23:26 - 00:23:33] And for that one, dear, this is the stress stress at stress concentration.
[00:23:33 - 00:23:34] Right?
[00:23:34 - 00:23:40] And for that one, dear, we probably need to know a K value.
[00:23:40 - 00:24:00] So either either approximate or experimental or it might be kind of both.
[00:24:00 - 00:24:04] You might approximate it and then use an experiment to do all right.
[00:24:04 - 00:24:10] And then that, I don't know, splits out your final design.
[00:24:10 - 00:24:11] Yeah?
[00:24:11 - 00:24:14] All I'm trying to do is like make crystal clear that if you want to
[00:24:14 - 00:24:17] do your stress analysis after you've done this example of our forces,
[00:24:17 - 00:24:21] there's no reason why you couldn't do heat to the stuff and then keep going, right?
[00:24:21 - 00:24:26] So idea is that this week you guys have like lots of what you need to get stuck
[00:24:26 - 00:24:28] into it while you're not too busy with other things.
[00:24:28 - 00:24:31] And then that should free up your mind for, if you get busy with how to
[00:24:31 - 00:24:34] coarse this later.
[00:24:34 - 00:24:38] Obviously I've made it on the fly, so hopefully that is kind of a clear diagram.
[00:24:38 - 00:24:44] But any comments we're happy to keep flying along.
[00:24:44 - 00:24:48] So I'll just show you the fact that our list that we made is a list.
[00:24:48 - 00:24:52] It's not, doesn't have to be in that order.
[00:24:52 - 00:24:57] Cool.
[00:24:57 - 00:24:58] So now we're into the fun stuff.
[00:24:58 - 00:25:01] What shapes slash possible designs are available.
[00:25:01 - 00:25:05] I'll do a quick like two minute timer, sketch out what kind of shapes,
[00:25:05 - 00:25:09] how many members possible, and then we'll go through those.
[00:25:09 - 00:25:10] Surely.
[00:25:10 - 00:26:46] Got some good shapes out on there.
[00:26:46 - 00:26:47] Nice.
[00:26:47 - 00:26:50] There could be more to that, but yeah.
[00:26:50 - 00:26:53] Nice.
[00:26:53 - 00:26:55] Cool.
[00:26:55 - 00:27:00] I'll look like people made some pretty good ideas.
[00:27:00 - 00:27:03] Sweet.
[00:27:03 - 00:27:05] Everything we're pretty good for time.
[00:27:05 - 00:27:07] Do we need more time?
[00:27:07 - 00:27:10] Source to do all ideas.
[00:27:10 - 00:27:11] Good ideas.
[00:27:11 - 00:27:12] Get into it.
[00:27:12 - 00:27:13] Sweet.
[00:27:13 - 00:27:30] Alright, let's get back into it there.
[00:27:30 - 00:27:31] We'll make it start.
[00:27:31 - 00:27:48] So just get back to quiet.
[00:27:48 - 00:28:00] Cool.
[00:28:00 - 00:28:03] So this is where we're in that engagement.
[00:28:03 - 00:28:04] It was good.
[00:28:04 - 00:28:09] I saw quite a lot of nice, nice kind of sketches to see how,
[00:28:09 - 00:28:11] many shapes that they want me to draw.
[00:28:11 - 00:28:12] It's one of those things.
[00:28:12 - 00:28:15] It would be good if you could just like show me a drawing,
[00:28:15 - 00:28:19] but you have to tell me now like in descriptive terms what the shape looks like.
[00:28:19 - 00:28:21] So I can draw it.
[00:28:21 - 00:28:23] Equal lateral triangle.
[00:28:23 - 00:28:25] I like it nice and clear.
[00:28:25 - 00:28:29] And I'm guessing that has to be a three-member design.
[00:28:29 - 00:28:34] Now I can't remember if this is,
[00:28:34 - 00:28:38] I think on my sketch on the assignment I drew this other way around it.
[00:28:38 - 00:28:39] I'm just going to have to do it.
[00:28:39 - 00:28:42] Flip this like we're looking at it from the other side of the assignment.
[00:28:42 - 00:28:43] There you go.
[00:28:43 - 00:28:44] My bad.
[00:28:44 - 00:28:46] All around with it.
[00:28:46 - 00:28:48] But the people want me to change it.
[00:28:48 - 00:28:52] Is it okay, clear enough that this is the lowest point even though?
[00:28:52 - 00:28:53] Yeah.
[00:28:53 - 00:28:54] Okay.
[00:28:54 - 00:28:55] Cool.
[00:28:55 - 00:28:56] Sweet.
[00:28:56 - 00:28:58] Yeah, so this is the one that's got the roller-boar.
[00:28:58 - 00:28:59] Cool.
[00:28:59 - 00:29:01] Alright, that's what we got.
[00:29:01 - 00:29:06] Alright, angle what they round.
[00:29:06 - 00:29:07] Lay it on the bottom.
[00:29:07 - 00:29:08] Cool.
[00:29:08 - 00:29:09] Anyone else got any ideas?
[00:29:09 - 00:29:17] The label fat one.
[00:29:17 - 00:29:18] Cool.
[00:29:18 - 00:29:19] So I don't want to say it.
[00:29:19 - 00:29:20] I like it.
[00:29:20 - 00:29:21] Cool.
[00:29:21 - 00:29:22] Sweet.
[00:29:22 - 00:29:23] That's pretty classic.
[00:29:23 - 00:29:24] What else we got?
[00:29:24 - 00:29:25] What else?
[00:29:25 - 00:29:27] What else?
[00:29:27 - 00:29:28] I'll say.
[00:29:28 - 00:29:31] Isn't this one the else I'll say this triangle?
[00:29:31 - 00:29:32] Oh, this one's equal.
[00:29:32 - 00:29:33] Can it be equal lateral?
[00:29:33 - 00:29:34] It probably could have been.
[00:29:34 - 00:29:36] It could have been like 400.
[00:29:36 - 00:29:37] You know?
[00:29:37 - 00:29:39] It would be like you could do that.
[00:29:39 - 00:29:42] You would just like lose marks because it wouldn't fit the thing.
[00:29:42 - 00:29:46] Yeah, it's like this is the dotted line.
[00:29:46 - 00:29:49] Yeah.
[00:29:49 - 00:29:52] Say, I just put a little ex to say like,
[00:29:52 - 00:29:54] I'll make it a star.
[00:29:54 - 00:29:56] Not recommended.
[00:29:56 - 00:30:03] That is definitely an option and I appreciate you guys saying that.
[00:30:03 - 00:30:04] Cool.
[00:30:04 - 00:30:06] What else?
[00:30:06 - 00:30:19] Like this?
[00:30:19 - 00:30:25] Oh, yeah, yeah, yeah, like this.
[00:30:25 - 00:30:26] Yeah, okay.
[00:30:26 - 00:30:31] Cool, cool, cool, cool.
[00:30:31 - 00:30:34] This is kind of us.
[00:30:34 - 00:30:35] Cool.
[00:30:35 - 00:30:39] What other ideas do we have?
[00:30:39 - 00:30:57] All the pins I have, I said do not have any red pins.
[00:30:57 - 00:31:00] Maybe one of these is a different color.
[00:31:00 - 00:31:01] Okay, cool.
[00:31:01 - 00:31:06] Okay, so this is good.
[00:31:06 - 00:31:09] This is good, but not evaluating them yet.
[00:31:09 - 00:31:13] Any other ideas, any other ideas?
[00:31:13 - 00:31:14] Yep.
[00:31:14 - 00:31:20] To give a structure, which we sort of mentioned before.
[00:31:20 - 00:31:23] So it's going to be slightly, I've drawn that way too big.
[00:31:23 - 00:31:27] But there'd be some sort of, some angle here.
[00:31:27 - 00:31:29] Say, say, what you'd have to calculate for.
[00:31:29 - 00:31:30] But yep.
[00:31:30 - 00:31:35] Cool.
[00:31:35 - 00:31:36] Any other ideas?
[00:31:36 - 00:31:37] Yeah.
[00:31:37 - 00:31:40] Someone's always sort of say, is that one?
[00:31:40 - 00:31:42] I might put that.
[00:31:42 - 00:31:49] I mean, it's sort of a hard one to imagine, but yeah, maybe you could sort of somehow.
[00:31:49 - 00:31:57] Cool, cool, cool.
[00:31:57 - 00:32:00] Right.
[00:32:00 - 00:32:03] Are there any other ideas that we can think of?
[00:32:03 - 00:32:05] Rectangle.
[00:32:05 - 00:32:06] Yeah, we could do rectangle.
[00:32:06 - 00:32:07] We could do rectangle.
[00:32:07 - 00:32:11] We could do rectangle and then probably have to have like, one of those kind of structures in
[00:32:11 - 00:32:12] the middle or similar.
[00:32:12 - 00:32:13] Oh, sure.
[00:32:13 - 00:32:18] Never seeing one over before, but it would be heavy, right?
[00:32:18 - 00:32:19] Heavy.
[00:32:19 - 00:32:20] Cool.
[00:32:20 - 00:32:22] Any other ideas?
[00:32:22 - 00:32:31] I don't think it's says that you're limited.
[00:32:31 - 00:32:34] But you are getting points for your strength to weight ratio.
[00:32:34 - 00:32:37] So you're kind of discouraged.
[00:32:37 - 00:32:40] And that seems of the mark scene.
[00:32:40 - 00:32:41] Yeah.
[00:32:41 - 00:32:46] I'm not sure, not sure if you were to do a square what the benefit is compared to doing
[00:32:46 - 00:32:50] the triangle that is there.
[00:32:50 - 00:32:51] Cool.
[00:32:51 - 00:32:55] Are we got any other ideas?
[00:32:55 - 00:33:00] Or is that, is that our, oh, yeah.
[00:33:00 - 00:33:01] An owl?
[00:33:01 - 00:33:04] Yeah.
[00:33:04 - 00:33:09] I mean, if you were to do an owl, it would still have to be like a third member sort of similar
[00:33:09 - 00:33:10] like this.
[00:33:10 - 00:33:15] You could also have like a, something that maybe had some sort of structure.
[00:33:15 - 00:33:20] I'm not too sure getting pins, pins there, right?
[00:33:20 - 00:33:27] So to start with, so I'll talk through these and then I've got some slides there.
[00:33:27 - 00:33:31] We'll probably help facilitate what I'm also going to say, but we'll see what I can kind of
[00:33:31 - 00:33:34] of cover just by going on the fly.
[00:33:34 - 00:33:44] So generally speaking, I'm going to draw a boundary around these ones here and put those
[00:33:44 - 00:33:50] all with the asterisks that would have my knot endorsement.
[00:33:50 - 00:33:57] I mean, this one, this one here I think the struggle of doing this one is that you probably
[00:33:57 - 00:34:00] don't have enough owl minim strips to actually be able to do it.
[00:34:00 - 00:34:06] So although you're not, you're not officially told you can't do a form in the structure,
[00:34:06 - 00:34:11] you do only have four strips of owl minim to allocate for all of your testing and your building.
[00:34:11 - 00:34:19] So this one here runs a high risk of not having enough materials to kind of actually complete the design, right?
[00:34:19 - 00:34:20] Cool.
[00:34:20 - 00:34:26] This one here, we know that's not recommended because we won't meet the specification of being the distance
[00:34:26 - 00:34:29] horizontally out that point 0 needs to be.
[00:34:29 - 00:34:36] And then I guess these ones here, they're in their own sort of sub category.
[00:34:36 - 00:34:41] Does anyone, can anyone tell me what is not good with these ones?
[00:34:41 - 00:34:47] Bearinstrace, they potentially could be more bearinstrace.
[00:34:47 - 00:34:57] I've not done the calculation, but at the pen, at the pen connections, they might be more a higher load, I'm not sure.
[00:34:57 - 00:35:02] It's probable, but I've not done the caps, like, you know, engineer, I can't see.
[00:35:02 - 00:35:05] But what other kind of stresses there?
[00:35:05 - 00:35:10] What is the nice and simple thing about these top three in this one?
[00:35:10 - 00:35:15] That these ones don't have ending moment, yeah?
[00:35:15 - 00:35:23] So if we have our pens in our corners, or just where the supports are and where the load is attached,
[00:35:23 - 00:35:29] is no moment there, so there'll be no bending in our members, right?
[00:35:29 - 00:35:35] They'll be either pure axial tension or compression, which is really nice when it comes to doing the hand calculations
[00:35:35 - 00:35:39] because you can work out the tin style stress, you can work out the compressive stress.
[00:35:39 - 00:35:43] It's in compression, we probably also want to check the buckling, then obviously around the pens,
[00:35:43 - 00:35:51] there'll be some kind of things like earrings, dress, and other considerations, maybe tear out or that sort of thing.
[00:35:51 - 00:35:53] So, yeah?
[00:35:53 - 00:35:57] Cool, so these ones here have, have bending.
[00:35:57 - 00:36:04] And what we'll see is that that, that just makes you think more complicated than it needs to.
[00:36:04 - 00:36:09] Some people might be tempted to do something like this, or maybe just depending on the geometry,
[00:36:09 - 00:36:16] because maybe you can get away with having a lighter design, but again, stress concentration and bending
[00:36:16 - 00:36:27] is not very many diagrams that kind of describe that very clearly, but there's lots of diagrams that describe stress concentrations and pure axial kind of stress.
[00:36:27 - 00:36:38] Cool, so then I guess what I was going to come down to is what kind of strength to weight ratio are you trying to get versus the simplicity of your calculations here?
[00:36:38 - 00:36:51] So some of them, I mean you could do each of them, you could work out watch loads in the menders for the different designs and then which one you think would be a better bang for buck for what strength weight ratio you might get.
[00:36:51 - 00:36:58] Or you might just be the type of group that want to kind of pick one and be done, and that is completely fine to do, right?
[00:36:58 - 00:37:07] But when it comes to finding a design, having some of these sketches and sort of saying why you chose the shape that you did is sort of what we would expect, I guess.
[00:37:07 - 00:37:21] Or at least some sort of justification for why you did it, you know, so you might go, oh, this one here, although it might have the best strength weight ratio, maybe, I don't know, log schools that we do it, I like symmetry, I don't know.
[00:37:21 - 00:37:31] This one here you might say, the tinsel, the tinsel in the mender might be the longest membrane that means that we're kind of going to use less material because of that, yeah?
[00:37:32 - 00:37:34] Any questions on any of that?
[00:37:34 - 00:37:42] What was that kind of gone, have I explained what I think clearly?
[00:37:42 - 00:37:47] I should have rephrase my question, I said what questions do you have?
[00:37:47 - 00:37:56] What questions do you have?
[00:37:56 - 00:38:06] In terms of our supports, this bottom pen here, it's fixed in place, so there's like a little bracket that sits on the table,
[00:38:06 - 00:38:14] and this one here is on a slider, so it's got a bearing, so we have a slide up and down.
[00:38:14 - 00:38:23] So obviously if you have a mender here, then that's going to define the length as long as you've drilled your holes in the right place, it should be able to be within, it plus minus three tolerance.
[00:38:23 - 00:38:43] Yep, yep, so all the pins will be supplied on the day, as I said, I might give a couple of pins to the workshop, and they always seem to somehow grow legs and walk away.
[00:38:43 - 00:38:52] So yeah, basically you just want to make sure those pins are going to be able to be supplied on the day, and then you'll give them back on the day,
[00:38:52 - 00:38:58] and then we keep on using them indefinitely as part of our sustainability goals, you know?
[00:38:58 - 00:39:06] Yeah, but they're 70 mill long and they fit inside each of these brackets, so that's why this is a thing that says it needs to be 50 mill,
[00:39:06 - 00:39:12] because that's to make sure you're definitely fit inside the brackets, so I think it's actually the load attachment one that's slightly narrower.
[00:39:12 - 00:39:14] Question?
[00:39:14 - 00:39:22] Yep, so it's on the diagram.
[00:39:22 - 00:39:24] Yep, you want to say it for us?
[00:39:24 - 00:39:30] It's just a bit of, like I know where it, it's a bit of, in some time we wanted the range for the dimensions there, we're looking at.
[00:39:30 - 00:39:32] Last one minus how many millimeters?
[00:39:32 - 00:39:33] Three millimeters.
[00:39:33 - 00:39:41] Three millimeters, yep, so yeah, we've obviously done that as well to show that like, generally speaking,
[00:39:41 - 00:39:49] there's a clear idea that you can have for when you dimension that hold dimension, you could actually say that it's possible minus three mill.
[00:39:49 - 00:39:50] Yeah?
[00:39:50 - 00:39:56] Rather than having the general tolerance of an impossible minus half mill, then you can make it be, I don't know, 401 millimeters,
[00:39:56 - 00:40:01] but technically that's out of specification, but it's in size, specification, if you know what I mean.
[00:40:01 - 00:40:05] So it'll be a bit of to put on your drawing possible minus three mill for those dimensions.
[00:40:05 - 00:40:10] If you have a nice, you know, if you've done these right angle ones, then it's pretty clear that
[00:40:10 - 00:40:14] where you drew the holes is where the fence is going to be in those dimensions will be met.
[00:40:14 - 00:40:15] Yep?
[00:40:15 - 00:40:24] Yep.
[00:40:24 - 00:40:29] Yeah, that's a really good question.
[00:40:29 - 00:40:39] The answer is, so the question is, if I design my mimba in a way, my compressor mimba, or my, or slash and my,
[00:40:39 - 00:40:47] teen problem inverse, such that I don't need any glue or rivets, do I have to use rivets or glue?
[00:40:47 - 00:40:50] And the answer is no.
[00:40:50 - 00:40:51] Yeah?
[00:40:51 - 00:40:56] Should probably write that somewhere.
[00:40:56 - 00:41:00] I'll update the assignment brief to make that clear.
[00:41:00 - 00:42:05] So, cool.
[00:42:05 - 00:42:08] So, we'll just go quite again.
[00:42:08 - 00:42:11] Is that really clear for everyone?
[00:42:11 - 00:42:18] So, so if, yeah, if you're designed, so if you've got a two-beam structure,
[00:42:18 - 00:42:23] there could be a, a common case where you might just have a teen tummy in there that's just,
[00:42:23 - 00:42:26] straight up just a piece of aluminium or some holes in it, right?
[00:42:26 - 00:42:29] Like a hole for the pens and a hole for your stress concentration, for example.
[00:42:29 - 00:42:32] Then, you know, you wouldn't have to add rivets to that.
[00:42:32 - 00:42:35] Some people are pretty crafty with how they make their cross-section.
[00:42:35 - 00:42:38] They might use the binder or something similar.
[00:42:38 - 00:42:45] So, in that case, if you design your design such that you don't actually have it joined together with a, with a glue or a fastener,
[00:42:45 - 00:42:48] like our rivets, then that's okay.
[00:42:48 - 00:42:51] So, I have to kind of, that's what I've just said here.
[00:42:51 - 00:42:56] Maybe this is the wording I use, maybe I just think different, but you may have less than one of each joining method
[00:42:56 - 00:42:59] if no glue slash rivets are required.
[00:42:59 - 00:43:00] You know?
[00:43:00 - 00:43:05] But if you do need to use a joining method, then you have to have one of each at least.
[00:43:05 - 00:43:06] Yeah?
[00:43:06 - 00:43:08] Hopefully that's clear.
[00:43:08 - 00:43:11] I'll update it in the assignment brief and I'll make it in red.
[00:43:11 - 00:43:12] Any other questions?
[00:43:12 - 00:43:13] That was really good.
[00:43:13 - 00:43:24] Yeah?
[00:43:24 - 00:43:27] So, you could have, yeah.
[00:43:27 - 00:43:29] I guess I should reword it to say,
[00:43:29 - 00:43:31] well, then you can't even do it that way.
[00:43:31 - 00:43:35] Because if you have three in the structure, you could have two of one joining method
[00:43:35 - 00:43:37] and one of the other, that's acceptable.
[00:43:37 - 00:43:42] Yeah.
[00:43:42 - 00:43:43] Yeah.
[00:43:43 - 00:43:46] So, that's where I think this is probably the clear way that I write it that I'd just say,
[00:43:46 - 00:43:52] you have to have at least one, unless you have two with none, or one with none.
[00:43:52 - 00:43:55] Yeah.
[00:43:55 - 00:43:58] It's hard about the word, it's hard to offer me, you know?
[00:43:58 - 00:43:59] Yeah.
[00:43:59 - 00:44:00] You know?
[00:44:00 - 00:44:01] Keep it at work stories.
[00:44:01 - 00:44:09] So, just to keep the time, I'm going to quickly go over this stuff here,
[00:44:09 - 00:44:13] and then we'll go, and we should be able to do an example calculation,
[00:44:13 - 00:44:14] which should be quite useful.
[00:44:14 - 00:44:17] So, thanks for all the questions and comments that's being really good.
[00:44:17 - 00:44:20] So, ensure what you are the designer.
[00:44:20 - 00:44:23] You have freedom of choice to do what you want to do.
[00:44:23 - 00:44:27] I'm not your mom or your dad or your parental figure,
[00:44:27 - 00:44:29] so you can do whatever you want.
[00:44:29 - 00:44:34] But I strongly recommend that you don't do anything that has been doing,
[00:44:34 - 00:44:39] just makes more work for you, and it also increases the design complexity as we sort of discussed.
[00:44:39 - 00:44:43] So, if you do decide to do it, you'll have to, you know,
[00:44:43 - 00:44:47] be the engineer and take it on the chin in terms of understanding that complexity
[00:44:47 - 00:44:51] to make sure that your design still fails in a way that it is required.
[00:44:51 - 00:44:56] So, here we see one example that has sort of done one of these crafty-looking things,
[00:44:56 - 00:45:01] but basically this photo has taken moments before it exploded,
[00:45:01 - 00:45:06] where the glue has kind of come apart from the flat and the web,
[00:45:06 - 00:45:11] and then there's been some sort of localized buckling per se,
[00:45:11 - 00:45:13] but after you keep off that terminology,
[00:45:13 - 00:45:15] because that can be its own sort of thing, right?
[00:45:15 - 00:45:19] Local buckling can be when it's while they want to fly in shape, you know?
[00:45:19 - 00:45:20] Engineering, technical things.
[00:45:20 - 00:45:22] Use the right terminology.
[00:45:22 - 00:45:27] Cool. So, in terms of my optimization, it's up to you.
[00:45:27 - 00:45:31] To do that, you might use that to dictate what shape you choose,
[00:45:31 - 00:45:32] because you might, you know,
[00:45:32 - 00:45:35] and definitely be able to kind of say, oh, is there either a number of members
[00:45:35 - 00:45:39] or the type of members that's up to you as to how much detail you go
[00:45:39 - 00:45:43] in terms of defining what shape you want to do and why.
[00:45:43 - 00:45:47] There's always a good range of designs, and sometimes what they'll do,
[00:45:47 - 00:45:51] which is percocinable shape and then reduce member cross-sections to still be for purpose.
[00:45:51 - 00:45:57] Well, they might kind of, you know, take the shape into a major consideration.
[00:45:57 - 00:46:02] In the first instance, and then not necessarily care as much about the air,
[00:46:02 - 00:46:05] the optimization, but you guys are really good at doing that,
[00:46:05 - 00:46:09] and you'll see when I upload the frequently asked questions,
[00:46:09 - 00:46:17] that's something that you guys will be able to include as an appendix to your report,
[00:46:17 - 00:46:22] if you do have an additional kind of analysis that you've done.
[00:46:22 - 00:46:25] So, here we see here the shrink weight ratio marks.
[00:46:25 - 00:46:29] So, if you know the mass of your, of your other menu,
[00:46:29 - 00:46:35] and you can kind of estimate if you want before you can kind of get a ballpark kind of idea of where you might be sort of sitting
[00:46:35 - 00:46:37] in terms of your shrink to weight.
[00:46:37 - 00:46:44] Cool. So, before we do this, I think maybe just like you might have like a stand-up and a little stretch,
[00:46:44 - 00:46:49] I will make the, figuring out how many questions available,
[00:46:49 - 00:46:54] and then we'll get into an example question.
[00:46:54 - 00:46:56] So, if you're free to stand up, you know.
[00:46:56 - 00:47:51] I think you've got that as kind of like, as far as the air,
[00:47:51 - 00:47:57] but I'm like, I'm down the air my way, and then with like a longer phase.
[00:47:57 - 00:48:01] I'm looking at my internship, using like a uni-strap bracket.
[00:48:01 - 00:48:07] It has like very much like a cantilever that tends to the bottom to a half way or lower part.
[00:48:07 - 00:48:09] How would you feel?
[00:48:09 - 00:48:14] Same kind of thing. It's not meaning the next to the hard of you, so that's completely there.
[00:48:14 - 00:48:17] You would have to understand, but yeah.
[00:48:17 - 00:48:21] You'd have to pause you, you could look at like what the loading is and that sort of thing,
[00:48:21 - 00:48:24] and then decide where it's worth it in terms of, you've got,
[00:48:24 - 00:48:27] each member has these other stresses that they have to then,
[00:48:27 - 00:48:30] I'm not sure what the compressor stress would be in this member here, so,
[00:48:30 - 00:48:36] up to you at the end of the day, but, quite a nice gym relationship for keeping simple.
[00:48:36 - 00:48:40] All right, thanks everyone. We'll get back into an hour.
[00:48:40 - 00:48:48] Yeah, I'll answer your question. Just ask me and, oh, yes.
[00:48:48 - 00:48:51] All right, thanks everyone. We've got a couple of questions,
[00:48:51 - 00:48:54] but we'll answer them as a holistic class.
[00:48:54 - 00:49:04] Yeah. Yeah, well, we'll ask them, I'll answer them in front of everyone.
[00:49:04 - 00:49:32] All right, thanks everyone. If we just take our seats, we'll get back into it.
[00:49:32 - 00:49:37] This is a difficult task to do. I'm not sure what best way to make you guys
[00:49:37 - 00:49:42] would get quiet, but, you know, maybe if I just ramble along on my microphone
[00:49:42 - 00:49:44] or eventually get quiet.
[00:49:44 - 00:49:49] Cool, so I think a few people had some questions that had arisen as they stretched,
[00:49:49 - 00:49:53] often happens. So we'll answer those questions before getting into our
[00:49:53 - 00:49:58] practice free body diagram. You guys want to go first?
[00:49:58 - 00:50:05] Well, there's a question that you had. Cool, good question.
[00:50:05 - 00:50:08] So the question is, can we put glue and rivets in the same member
[00:50:08 - 00:50:12] or does it have to be separate members and the idea is that it's separate members.
[00:50:12 - 00:50:16] So, yeah, people sort of did that last year, and there wasn't really my intent.
[00:50:16 - 00:50:20] The idea is that you either, you know, you back the member that you've,
[00:50:20 - 00:50:24] joining method that you've chosen and make sure that you understand it.
[00:50:24 - 00:50:27] Because, yeah, the only reason that you'd kind of
[00:50:27 - 00:50:31] river a glue joiners is if you didn't trust the glue and then kind of vice versa
[00:50:31 - 00:50:35] for the LA round, right? Cool, but yeah.
[00:50:35 - 00:50:38] Yeah, one one, one thing with it.
[00:50:38 - 00:50:40] Permiuma is what we're looking at. And I think,
[00:50:40 - 00:50:45] I think that does say it kind of clearly in the assignment brief.
[00:50:45 - 00:50:49] So, yeah. Next question.
[00:50:49 - 00:50:52] There's another one.
[00:50:52 - 00:51:00] Things also about the joining methods. Who got their question?
[00:51:00 - 00:51:03] There's a couple of people, right?
[00:51:03 - 00:51:06] So, there was someone that asked me a question about one of the
[00:51:06 - 00:51:10] L-shaped kind of structures and I sort of sort of reiterated it.
[00:51:10 - 00:51:14] I'll keep you design simple when I wouldn't choose one with bending.
[00:51:14 - 00:51:18] There was the E-L equations that you had as you kind of stretched and,
[00:51:18 - 00:51:31] so, yeah, there's no silly questions and don't feel like you do need to wait till the end.
[00:51:31 - 00:51:36] I'm sure there are other people that have the same.
[00:51:36 - 00:51:42] Yeah. So, you can see at least one member using only two-part
[00:51:42 - 00:51:45] epoxy or one member using only this.
[00:51:45 - 00:51:47] And if we're two member structures, I'll probably,
[00:51:47 - 00:51:52] as well as sort of update it. All structures that use, you know,
[00:51:52 - 00:51:55] geometry instead of having.
[00:51:55 - 00:51:59] But yeah, I'm not sure if you can actually do that idea or not.
[00:51:59 - 00:52:02] So, you can't go to the one and then two.
[00:52:02 - 00:52:15] If you have two members that are made with more than just one strip of aluminium,
[00:52:15 - 00:52:19] then, yeah, you need to have one that uses glue and one that uses a rivet.
[00:52:19 - 00:52:23] There, it's really good to clarify that.
[00:52:23 - 00:52:24] No, we had another one here.
[00:52:24 - 00:52:29] No, that's what we're saying.
[00:52:29 - 00:52:33] You could have none if you really, if you really were thinking
[00:52:33 - 00:52:38] innovatively and if the geometries and the dimensions of this assignment
[00:52:38 - 00:52:40] actually allow you to, right?
[00:52:40 - 00:52:43] So, you might think, oh, I can bend it to be this kind of geometry
[00:52:43 - 00:52:49] and then gives a little bit tricky because you have to have enough for the pen hole, right?
[00:52:49 - 00:52:52] Yeah, I'm saying you can do none, possibly,
[00:52:52 - 00:52:55] for asterisks of like, I don't actually know if it's possible or not.
[00:52:55 - 00:52:57] But if it is possible, it's allowed.
[00:52:57 - 00:53:00] If it's not possible, it probably won't work.
[00:53:00 - 00:53:07] Yeah? Hopefully it won't sit there, clear?
[00:53:07 - 00:53:12] Yeah, as I'm saying, I'll update that note to say that, you know,
[00:53:12 - 00:53:16] list joining methods may be allowed if they are not required.
[00:53:16 - 00:53:20] I.E. can push them in as are made from one single piece of aluminium
[00:53:20 - 00:53:25] and T-cell members are also made from one single piece of aluminium.
[00:53:25 - 00:53:28] Yeah, yeah, it's good to have clarified and I agree.
[00:53:28 - 00:53:32] Once I see that and it kind of makes this be like not correct, so,
[00:53:32 - 00:53:34] it's a fair play.
[00:53:34 - 00:53:40] Co, you know, the questions will sort of rip into this practice-free body diagram.
[00:53:40 - 00:53:44] Now, with this, if you've got a calculator,
[00:53:44 - 00:53:46] get it out.
[00:53:46 - 00:53:49] It helps me to trust my own calculations.
[00:53:49 - 00:53:54] And we'll try to do this relatively quickly so that we don't have to panic at the end.
[00:53:54 - 00:54:04] So, what I'm going to do is just draw a shape, in this case.
[00:54:04 - 00:54:06] It's this triangle here.
[00:54:06 - 00:54:10] I'm going to have some random dimensions that are not the same as the ones in your assignment.
[00:54:10 - 00:54:12] So, we've got 250 millimetres there.
[00:54:12 - 00:54:15] And then I'm going to say, I'm not drawn this very well.
[00:54:15 - 00:54:18] So, I'm going to roll out not too scale.
[00:54:18 - 00:54:31] Ideally, this dimension here to here would have been drawn such that that's 100 millimetres.
[00:54:31 - 00:54:36] And this one here, which looks awfully similar, is actually 50 millimetres.
[00:54:36 - 00:54:38] Cool.
[00:54:38 - 00:54:46] So, with that there, we probably also need to just make sure that we have to find what our coordinate system is.
[00:54:46 - 00:54:53] And we also would want to show that there's actually a load thing placed, right?
[00:54:53 - 00:54:55] So, we call that load if.
[00:54:55 - 00:54:59] In this case, I'm going to say if there's 25 kg,
[00:54:59 - 00:55:04] which I'm going to be really crude in the proximate as 250 newtons.
[00:55:04 - 00:55:09] Something lazy for this example, but if you guys are wanting to do a fine job,
[00:55:09 - 00:55:15] you probably will use like 9.8 or 9.8, 1 for gravity, and have some decimal places there, right?
[00:55:15 - 00:55:16] Cool.
[00:55:16 - 00:55:23] So, following this, what we would typically do is also,
[00:55:23 - 00:55:27] we can estimate what our reaction forces would be.
[00:55:27 - 00:55:32] And what direction they would be, right?
[00:55:32 - 00:55:37] So, does anyone want to tell me what reaction forces or what arrows I should draw?
[00:55:37 - 00:55:41] So, if we're looking at this bottom, this bottom fixed bracket,
[00:55:41 - 00:55:46] what forces do we think would be there?
[00:55:46 - 00:55:48] Reaction force.
[00:55:48 - 00:55:51] Yeah, so we have vertical and horizontal here, right?
[00:55:51 - 00:55:58] So, I'm going to draw my vertical, R, Y.
[00:55:58 - 00:56:01] Actually, there was a number these are, of course, one number two.
[00:56:01 - 00:56:06] Of course, one number one, of course, one number three, just for consistency,
[00:56:06 - 00:56:08] we're just kind of working out what our forces are.
[00:56:08 - 00:56:13] So, R, two, Y is going upwards, right?
[00:56:13 - 00:56:14] Cool.
[00:56:14 - 00:56:24] And then, well, I think that I'm just going to draw this one in as positive.
[00:56:24 - 00:56:26] R, two, X.
[00:56:26 - 00:56:30] We'll see if what my assumed is correct, right?
[00:56:30 - 00:56:32] Doesn't actually really matter what you put in.
[00:56:32 - 00:56:35] If you get it the wrong way around, it'll come out as a negative.
[00:56:35 - 00:56:36] Right?
[00:56:36 - 00:56:38] And then you know, I have to draw my arrow the wrong way around.
[00:56:38 - 00:56:39] Cool.
[00:56:39 - 00:56:41] And then for this top one, what arrows do we do?
[00:56:41 - 00:56:45] We just do the same.
[00:56:45 - 00:56:46] What was the difference?
[00:56:46 - 00:56:52] The difference, someone said, what's different about it?
[00:56:52 - 00:56:55] Does it have both horizontal and vertical sport?
[00:56:55 - 00:56:58] Only horizontal, right?
[00:56:58 - 00:56:59] Why is that?
[00:56:59 - 00:57:01] Well, it's on a roller.
[00:57:01 - 00:57:06] So, you can't provide any support at the side of the roller, right?
[00:57:06 - 00:57:11] I think that if we're going to have our forces, my first assumption was right,
[00:57:11 - 00:57:14] then this one is going to have to be the opposite way for our sum of the forces
[00:57:14 - 00:57:16] and the extra kind of equal out, right?
[00:57:16 - 00:57:22] Hopefully this is like either like, oh, this is super familiar to what we did like,
[00:57:22 - 00:57:27] previously, otherwise this is a nice refresher.
[00:57:27 - 00:57:28] Cool.
[00:57:28 - 00:57:33] So, following that, we have a few options to calculate first,
[00:57:33 - 00:57:41] but I will push us down the route of first calculating R1X, right?
[00:57:41 - 00:57:45] So, what would we need to do to calculate R1X?
[00:57:45 - 00:57:54] I'll speak of one.
[00:57:54 - 00:57:58] So, I know you guys know this, but as we have to at least think about it rather than just like,
[00:57:58 - 00:58:01] mindlessly, like, writing out the same thing.
[00:58:01 - 00:58:05] Yeah, so we're going to do, we can use, yeah, we can either use cell force in the next
[00:58:05 - 00:58:09] sum of forces and why are sort of our two options.
[00:58:09 - 00:58:13] All there's a third one, we could also use our moments, right?
[00:58:13 - 00:58:15] Yeah, and could we have pin joints?
[00:58:15 - 00:58:17] What are the moments going to equal?
[00:58:17 - 00:58:18] Zero, right?
[00:58:18 - 00:58:22] Yeah, that's why we're not having glue joints and then flex joints and then there's a moment there
[00:58:22 - 00:58:24] and then it's, if you guys can't cut.
[00:58:24 - 00:58:27] So, instead of a purpose of using pin joints so that it's kind of simple,
[00:58:27 - 00:58:34] and I think that realistically what we might want to do is calculate our sum of the bowel
[00:58:34 - 00:58:39] we'll calculate, if we did some of the forces, we don't know we need the horizontal forces, right?
[00:58:39 - 00:58:48] So, we can't actually do some of the forces, all we'll get is that R1X equals two X, right?
[00:58:48 - 00:58:50] So, what do we have to do instead?
[00:58:50 - 00:58:57] Sum of, yeah, moments around two should work.
[00:58:57 - 00:59:04] Cool, so if we do that there, so we're doing at two, our force, right?
[00:59:04 - 00:59:10] So, we've got, so this way positive, right?
[00:59:10 - 00:59:16] There's an eigenuantly asking that our way is positive, right?
[00:59:16 - 00:59:27] Yeah, cool, so that means that R1X times by the distance 0.15 liters take away
[00:59:27 - 00:59:38] now if, which we can write as 250 newtons, times by 0.250 equals 0, right?
[00:59:38 - 00:59:44] No, yes?
[00:59:44 - 00:59:48] Okay, some people saying yes, some people make me like panic in front of 300 people,
[00:59:48 - 00:59:50] that's all good, don't worry.
[00:59:50 - 00:59:57] So, if I do that and I rearrange it, I should, if I just do that sneakily in one step,
[00:59:57 - 01:00:11] should get this one here, 0.25 meters, times by 250 newtons over 0.15 meters,
[01:00:11 - 01:00:14] should give me the number of newtons, right?
[01:00:14 - 01:00:18] Does anyone got the calculator?
[01:00:18 - 01:00:22] And I do what I get for one, seven newtons.
[01:00:22 - 01:00:29] And I do, encourage at least someone to like fact check me because I am very human.
[01:00:29 - 01:00:37] So, following that, we can probably do what that person said earlier of some of the forces
[01:00:37 - 01:00:43] and the X to find out our reaction to and the X, right?
[01:00:43 - 01:00:47] Yeah, it's just sort of like, yeah, I'm struggling to understand.
[01:00:47 - 01:00:53] I think, I think it's really easy for you guys, but if it's not and it's confusing then that's also all good.
[01:00:53 - 01:00:58] That's what we're doing it just to go like, oh, that's right, this is the way that we do it and this is the process.
[01:00:58 - 01:01:06] So, to calculate our two weeks, this time I think we will use some of the forces in our X equaling 0, right?
[01:01:06 - 01:01:10] Because this thing's not moving anywhere, it's not the dynamic version of this.
[01:01:10 - 01:01:21] Yep, so from that, yeah, we just get sort of sort of cheaper just to, well, we can do it.
[01:01:21 - 01:01:25] So, two weeks is in the positives, right?
[01:01:25 - 01:01:29] Take away our 1X equals 0.
[01:01:29 - 01:01:40] And then we can say that our 2X equals X, right?
[01:01:40 - 01:01:47] Checkers for 1, 7, Newton as well.
[01:01:47 - 01:01:55] Cool, so I'll see this is, I think I must have rounded that to 3 as if.
[01:01:55 - 01:02:00] which would be good to do if you have done it.
[01:02:00 - 01:02:03] I need to check that up done that correctly.
[01:02:03 - 01:02:11] Cool, and then 3, how do we reckon we would find out our 2Y?
[01:02:11 - 01:02:17] What do we need to do?
[01:02:17 - 01:02:21] Oh, some of the forces in the Y equals 0, cool.
[01:02:21 - 01:02:26] And what do we get?
[01:02:26 - 01:02:35] Our 2Y equals, yeah, yeah, yeah, so I'm doing it.
[01:02:35 - 01:02:50] Our 2Y equals, yeah, yeah, so 2Y equals as we've cheated to 115 units.
[01:02:50 - 01:02:54] Cool, so we can see there.
[01:02:54 - 01:02:58] There's nothing sort of stuff you guys can be able to do that for other shapes.
[01:02:58 - 01:03:06] So hopefully that's just shown you that you're kind of happy with what you've kind of been tasked to do.
[01:03:06 - 01:03:11] And then what I would say is a really good thing to do is conclude what you've done, right?
[01:03:11 - 01:03:15] So I think at the end of any calculation, you want to have a comment.
[01:03:15 - 01:03:29] So you could say, I know this means the reaction forces.
[01:03:29 - 01:03:40] 1X2X2Y, we get both of these being 417.
[01:03:40 - 01:03:47] So I can add positive, so we're happy that our arrows are correct into 115 units, yeah?
[01:03:47 - 01:03:59] I think our is should.
[01:03:59 - 01:04:04] So we've got, yeah, it's good to check.
[01:04:04 - 01:04:06] And these are the things that engineers are very good at doing.
[01:04:06 - 01:04:11] If you ever want to have a really fun time, so let our free body diagram to a conference,
[01:04:11 - 01:04:14] and you'll be told you're wrong.
[01:04:14 - 01:04:17] Not speaking from experience, of course.
[01:04:17 - 01:04:21] Cool, so following that, what would be the next thing that we need to do?
[01:04:21 - 01:04:23] This is our reaction forces at the pins.
[01:04:23 - 01:04:28] It's kind of useful if we were designing the supports, but we're not, and we can assume that they're strong enough, right?
[01:04:28 - 01:04:35] Cool, so what do we need now to calculate the forces in each member?
[01:04:35 - 01:04:48] Cool, so following that, let's just say determine member forces.
[01:04:48 - 01:04:57] Cool, and so I'm going to take a cut of 0.1, and that's going to go our arrows like this.
[01:04:57 - 01:05:03] So we're going to have F13 and F12 based on our diagram, right?
[01:05:03 - 01:05:09] And then we said that our reaction force, hopefully this was the right pinels using, right?
[01:05:09 - 01:05:14] Now one there is our R1, yes, yeah.
[01:05:14 - 01:05:16] Cool, so that's that.
[01:05:16 - 01:05:18] Meath of the cuts, I think there's a couple ways you can do this.
[01:05:18 - 01:05:21] If you want to use the other way, that's all good.
[01:05:21 - 01:05:23] If the other way doesn't work, all good.
[01:05:23 - 01:05:27] It's also been a while since I've done the N1202.
[01:05:27 - 01:05:38] Sweet, and so to determine, say, that's just right, do you want to determine if we can do this?
[01:05:38 - 01:05:49] If 1, 3, so try and do this one here, what might we need to do?
[01:05:49 - 01:05:52] Not quite, so we're going to use the forces.
[01:05:52 - 01:05:55] So we'll, we've got three options again, I think.
[01:05:55 - 01:05:59] We use the sum of the forces in the x, the sum of the force in the y or the moment, yeah?
[01:05:59 - 01:06:01] We will need to use the length to work out the angle.
[01:06:01 - 01:06:03] They'll come in a bit.
[01:06:03 - 01:06:04] Someone tell me what do we need to do?
[01:06:04 - 01:06:10] Sum of force in the y, yeah?
[01:06:10 - 01:06:18] Sum of the forces in x equals zero, because we know this one here, so we can work out this one here, yeah?
[01:06:18 - 01:06:28] Cool, and to do that, as we kind of do, we need to actually use the lengths to work out what the angle is.
[01:06:28 - 01:06:39] So if we're doing 100, so we're out, point where our load is, now this is 250 here, then if we want to do,
[01:06:39 - 01:06:50] our angle, I believe that it will be a tan minus 1, and it'll be opposite over adjacent.
[01:06:50 - 01:06:58] So 250 over 100, we could use the decimals, because it's a ratio, it shouldn't matter up.
[01:06:58 - 01:07:05] So if you wanted to write 0.1501 and 0.25, that's all good.
[01:07:05 - 01:07:10] You don't have a calculator handy.
[01:07:10 - 01:07:13] We can just calculate that and check that at just a 1 dp.
[01:07:13 - 01:07:16] That'll be super useful.
[01:07:16 - 01:07:20] Sweet, that's what I got.
[01:07:20 - 01:07:23] Cool, so now we should have everything that we need.
[01:07:23 - 01:07:29] So if our sum of the forces in the x zero, if 1, 3 is in the positive direction,
[01:07:29 - 01:07:38] so I think what we will have is if 1, 3 times by, now what component of a
[01:07:38 - 01:07:40] x, we're trying to find.
[01:07:40 - 01:07:47] So we know the hypotenit, while we're trying to find the hypotenuse value,
[01:07:47 - 01:07:52] and this component is the opposite value, right?
[01:07:52 - 01:08:01] So there would be what trig function, sine, right?
[01:08:01 - 01:08:08] So I should be the sine component of that force as the x component of that force, right?
[01:08:08 - 01:08:12] So I'm breaking it down to be like, you did this in years of the thing physics,
[01:08:12 - 01:08:14] I'm pretty sure.
[01:08:14 - 01:08:19] But there's nothing going up in front of quite a few people to really
[01:08:19 - 01:08:22] sec and guess everything you've ever done.
[01:08:22 - 01:08:25] Hope, so we should have a question like that.
[01:08:25 - 01:08:28] And I'm sure someone will be able to tell me if I'll use the wrong trig function.
[01:08:28 - 01:08:34] And then if we do a little bit of algebra, we can get that if 1, 3 will equal
[01:08:34 - 01:08:39] 1, x over sine, they say, right?
[01:08:39 - 01:08:48] And that should be 4, 1, 7, Newton's over sine of 68.2.
[01:08:48 - 01:08:50] Yeah?
[01:08:50 - 01:08:55] So I get 4, 4, 9, Newton's.
[01:08:55 - 01:08:58] Now, what does that mean?
[01:08:58 - 01:09:06] Someone's whispered it, they can say it later.
[01:09:06 - 01:09:09] In teaching, right?
[01:09:09 - 01:09:14] So we probably want to make that nice and clear so that then when it comes to do our calculations for our
[01:09:14 - 01:09:17] member, we do distress as if it's in tension.
[01:09:17 - 01:09:21] Now, you might think that that seems pointless.
[01:09:21 - 01:09:26] But I've seen people have liked their design being a complete opposite way around
[01:09:26 - 01:09:31] and they just put the first thing on and like buckles because they had single men going there for there was an
[01:09:31 - 01:09:33] tension, not compression.
[01:09:33 - 01:09:36] So make sure you fact check yourself.
[01:09:36 - 01:09:41] And so because it's positive, that's how we define our tension notation, right?
[01:09:41 - 01:09:49] So if you're not sure, then just make sure you're confident as you kind of follow through with what you would expect to get.
[01:09:49 - 01:09:50] Cool.
[01:09:50 - 01:09:56] So obviously the next thing that we'll do is determine the other unknown, right?
[01:09:56 - 01:09:58] Which will be if 1, 2.
[01:09:58 - 01:09:59] Yeah?
[01:09:59 - 01:10:00] Add it.
[01:10:00 - 01:10:03] And so what do we need to use for that one?
[01:10:03 - 01:10:08] Some of the forces in there.
[01:10:08 - 01:10:09] And why?
[01:10:09 - 01:10:10] Yeah.
[01:10:10 - 01:10:11] So the reason I'm asking you just that I'm actually running along.
[01:10:11 - 01:10:15] I feel like my speed is all good, but if it's not then make sure you let me know.
[01:10:15 - 01:10:23] So in that case here we've got going downward, negative, if 1, 2, right?
[01:10:23 - 01:10:35] And then we've also got going downward, negative, if 1, 3.
[01:10:35 - 01:10:38] And in this case what trig function would be used?
[01:10:38 - 01:10:43] Cosine, yeah.
[01:10:43 - 01:10:47] So be times by cos of the angle, right?
[01:10:47 - 01:10:48] 68.
[01:10:48 - 01:10:49] 22.
[01:10:49 - 01:10:52] And that should all equal zero.
[01:10:52 - 01:10:53] Cool.
[01:10:53 - 01:11:02] And so if someone wants to give me that, then we should just get f1, 2, take away something,
[01:11:02 - 01:11:15] equals zero, and then f1, 2, equals, what do we get?
[01:11:15 - 01:11:26] Yeah?
[01:11:26 - 01:11:28] So negative 1.67.
[01:11:28 - 01:11:30] So we get negative f1, 2.
[01:11:30 - 01:11:32] Don't forget to drop that negative.
[01:11:32 - 01:11:33] It's very easy to do.
[01:11:33 - 01:11:35] There's 167 newtons.
[01:11:35 - 01:11:42] So that means that f1, 2, equals negative 1.67 newtons.
[01:11:42 - 01:11:45] What she calls compression, right?
[01:11:45 - 01:11:50] You want to have your fat?
[01:11:50 - 01:11:51] So I feel like hopefully we can get that.
[01:11:51 - 01:11:56] So I feel like hopefully you had the same, like, many heart attack that I had when I was, like, doing the, doing the free body diagram.
[01:11:56 - 01:11:58] I was like, wait, I've got two negatives here.
[01:11:58 - 01:12:01] That's not going to work, but it's going to come out in the wash, right?
[01:12:01 - 01:12:04] So really this arrow would have been gone the other way.
[01:12:04 - 01:12:08] But if we consistent, then we know that we'll get the right answer eventually.
[01:12:08 - 01:12:09] Cool.
[01:12:09 - 01:12:13] And so for this third one, we're going to have to got our vertical.
[01:12:13 - 01:12:20] Got our f, if, 2, 3, f1, 2, and we've got some other angle.
[01:12:20 - 01:12:23] This pick alpha.
[01:12:23 - 01:12:25] So what would alpha be?
[01:12:25 - 01:12:36] We'd have to do that opposite triangle wrap.
[01:12:36 - 01:12:39] I think I was 50, and this one was 2, 50 wrap.
[01:12:39 - 01:12:43] So what would alpha be?
[01:12:43 - 01:12:47] Does someone tell me just to have some confidence in myself?
[01:12:47 - 01:12:54] In first hand, sweet.
[01:12:54 - 01:12:58] So obviously you can draw these little triangles if they make it happen.
[01:12:58 - 01:13:03] So when I put that in my calculator, I get 78, and 7 degrees.
[01:13:03 - 01:13:06] So we can double-shift if that is the right answer.
[01:13:06 - 01:13:09] Then it should be happy days.
[01:13:09 - 01:13:10] Cool.
[01:13:10 - 01:13:15] So then what do we want to use to calculate this one?
[01:13:15 - 01:13:24] Got two options.
[01:13:24 - 01:13:27] Can we use either option or do we have to use one?
[01:13:27 - 01:13:43] Can we use x?
[01:13:43 - 01:13:44] Yep.
[01:13:44 - 01:13:45] I'll use x.
[01:13:45 - 01:13:49] Some of the forces and x equals zero.
[01:13:49 - 01:13:50] Cool.
[01:13:50 - 01:13:55] So we get f2.
[01:13:55 - 01:13:59] All right, that's something on here.
[01:13:59 - 01:14:00] Is that?
[01:14:00 - 01:14:04] Yeah, the reaction is nice and way more confusing if you don't have the reaction in there.
[01:14:04 - 01:14:07] The reactions should be going like this, right?
[01:14:07 - 01:14:12] 2x, and then this reaction is going up, right?
[01:14:12 - 01:14:13] 2y.
[01:14:13 - 01:14:20] So in theory, we could use either x or y, right?
[01:14:20 - 01:14:23] Yeah?
[01:14:23 - 01:14:26] Yeah.
[01:14:26 - 01:14:27] Yeah, we could.
[01:14:27 - 01:14:28] Yeah.
[01:14:28 - 01:14:31] Everyone's looking at it like, I don't know, George, you're the person teaching us.
[01:14:31 - 01:14:35] But all I'm saying is that, you know, sometimes students will say to me, oh, why did you use
[01:14:35 - 01:14:36] x at the end?
[01:14:36 - 01:14:39] So that's why I'm saying, you know, going through it.
[01:14:39 - 01:14:40] Cool.
[01:14:40 - 01:14:46] So if we use some of the forces and x equals zero, then we'll get r2x.
[01:14:46 - 01:14:49] So we need to really write r2x.
[01:14:49 - 01:14:53] And then we've got again an issue going on here.
[01:14:53 - 01:14:58] We've got plus f23, and then what would we need to?
[01:14:58 - 01:15:01] What trig function would we use this time?
[01:15:01 - 01:15:05] We also want the x component, which is the opposite, right?
[01:15:05 - 01:15:07] And then it's opposite, and we want the hypotenuse.
[01:15:07 - 01:15:09] So it'll be sine, right?
[01:15:09 - 01:15:10] So, yeah.
[01:15:10 - 01:15:16] So just make sure that you do, like, make sure that you agree with those things, because
[01:15:16 - 01:15:19] obviously if you choose the wrong thing, then it's not going to work properly, right?
[01:15:19 - 01:15:23] And I've also had students have that sort of happen, and then go like, why am I some of the forces not working now?
[01:15:23 - 01:15:27] And say, oh, yeah.
[01:15:27 - 01:15:42] Cool. So if we do a bit of rearranging, we get f23 equals negative r2x over sine of alpha.
[01:15:42 - 01:15:43] Yeah.
[01:15:43 - 01:15:49] And then if we put in the actual numbers, that would be what is r2x?
[01:15:49 - 01:15:51] So, we're going back, right?
[01:15:51 - 01:15:53] After x was 250 Newton.
[01:15:53 - 01:15:57] Yeah, so it should be negative 250 Newton.
[01:15:57 - 01:16:02] Ah, there we go.
[01:16:02 - 01:16:03] Good work.
[01:16:03 - 01:16:09] So this should be positive or negative.
[01:16:09 - 01:16:13] And then it's negative of the positive 4, 1, 7, right?
[01:16:13 - 01:16:16] Hopefully, I've written that kind of clearly, right?
[01:16:16 - 01:16:19] Like, the value is positive, but there's a negative sign in front of it.
[01:16:19 - 01:16:26] All over sine of 78, 1, 7 degrees.
[01:16:26 - 01:16:27] Yeah.
[01:16:27 - 01:16:29] And what does that give us?
[01:16:29 - 01:16:54] Wait, let's go.
[01:16:54 - 01:16:57] Negative 4, 2, 5.
[01:16:57 - 01:17:03] And because it's negative, that means we're in compression, right?
[01:17:03 - 01:17:04] So we need it.
[01:17:04 - 01:17:09] And so they've now again, we should really write a comment saying no.
[01:17:09 - 01:17:31] So this means the mean-beers forces are, so if 1, 3, if 1, 2, and if 2, 3,
[01:17:31 - 01:17:34] and that's just summarized what we had.
[01:17:34 - 01:17:40] So we're for nine tension.
[01:17:40 - 01:17:50] We had negative 1, 6, 7, Newton, compression.
[01:17:50 - 01:17:55] We had negative 4, 2, 5, Newton, compression, right?
[01:17:55 - 01:18:00] You're right, have it there.
[01:18:00 - 01:18:02] So the thing is, once you've got it nice and clear,
[01:18:02 - 01:18:06] the enemies there when it comes to doing your next calculations, you know?
[01:18:06 - 01:18:10] You can't argue with that kind of comment, but if you just write negative 1, 6, 7,
[01:18:10 - 01:18:14] there's a chance that you can kind of make a mistake when it comes to kind of
[01:18:14 - 01:18:18] your following kind of calculation that you might do, right?
[01:18:18 - 01:18:19] Cool.
[01:18:19 - 01:18:22] Any questions on that?
[01:18:22 - 01:18:26] What questions do you have?
[01:18:26 - 01:18:31] Apparently they're like, makes you like 1 million times more likely to answer the question.
[01:18:31 - 01:18:32] It's crazy.
[01:18:32 - 01:18:43] So you'll see and here, probably should have had this, but here, but this is kind of the format
[01:18:43 - 01:18:46] that we would require for each of your hand calculations.
[01:18:46 - 01:18:49] I'll kind of go over this briefly in class as well.
[01:18:49 - 01:18:54] So for example, here, here's an example of someone doing a calculation on a key,
[01:18:54 - 01:18:57] key way looking at the shaft crushing in the shaft.
[01:18:57 - 01:19:01] No, sorry, the key crushing and the key sharing.
[01:19:01 - 01:19:04] And then there were also added some times, there's an added some dimensions there,
[01:19:04 - 01:19:09] but we can see that along the way they've kind of used or tickled each of those things.
[01:19:09 - 01:19:15] And the comment saying what it means is really important, especially in the world of
[01:19:15 - 01:19:21] AI, where you know, it's pretty easy just to get an answer for something,
[01:19:21 - 01:19:25] but really what we're trying to show is that you have the engineering kind of intuition
[01:19:25 - 01:19:28] to show what your calculation means, right?
[01:19:28 - 01:19:29] Yeah.
[01:19:29 - 01:19:33] So if you've done a calculation on the bearing stress near the pin,
[01:19:33 - 01:19:37] the requirement might be showing that, you know, this shows that the bearing stress is
[01:19:37 - 01:19:42] and it should not fail the meaning from bearing stress at this load.
[01:19:42 - 01:19:43] Cool.
[01:19:43 - 01:19:49] So we could have an improvement, you know, engineers like to critique other engineers.
[01:19:49 - 01:19:52] Do you want me to add another example calculation on learn?
[01:19:52 - 01:19:54] You know, that's my nice and things people said.
[01:19:54 - 01:19:56] Some people said, no, some people said yes.
[01:19:56 - 01:19:59] I'll go with the equal majority.
[01:19:59 - 01:20:04] I'll put it up and if you don't want to look at it, I'll look at it.
[01:20:04 - 01:20:05] Cool.
[01:20:05 - 01:20:11] So are any people thinking about doing the two mimbar for everybody?
[01:20:11 - 01:20:12] No.
[01:20:12 - 01:20:13] Some people are.
[01:20:13 - 01:20:14] Do we want to have a quick discussion about it?
[01:20:14 - 01:20:15] You're sort of happy.
[01:20:15 - 01:20:20] Arms up for happy or thumbs up for sort of.
[01:20:20 - 01:20:21] Yeah.
[01:20:21 - 01:20:24] That's the same question.
[01:20:24 - 01:20:30] Other people, you're happy or do I mean, just sort of one thing even though you haven't asked for it,
[01:20:30 - 01:20:36] which is fine, is that you will need or you may want to include the mess of this
[01:20:36 - 01:20:37] role, right?
[01:20:37 - 01:20:43] So in everybody diagram, you'll see that I've made a pretty bold assumption that this
[01:20:43 - 01:20:46] mess of this role here doesn't exist.
[01:20:46 - 01:20:50] And that's appropriate because I have a three-game structure, but it is an assumption that I've
[01:20:50 - 01:20:52] made that's not necessarily true, right?
[01:20:52 - 01:20:53] Yeah.
[01:20:53 - 01:20:59] It's like a classic, I mean, it's so many means about engineering assumptions, but that's
[01:20:59 - 01:21:06] why it is, on the world's slowest scroll wheel.
[01:21:06 - 01:21:12] We have these messes here, and that's why we can see that sometimes people want to include
[01:21:12 - 01:21:16] this mess of the load attachment and chain.
[01:21:16 - 01:21:19] And then the hook to the total mess, right?
[01:21:19 - 01:21:27] So in my one there, I just see that the total mess is 25 kg, but on the day to get 25 kg is actually
[01:21:27 - 01:21:34] like impossible because I don't have like a 0.9 mess and a one mess, right?
[01:21:34 - 01:21:38] So the total mess is what you would put in your calculation as well, I'm trying to say.
[01:21:38 - 01:21:46] So realistically, it would have been smarter if I put 26.1, if you pass those here then roughly
[01:21:46 - 01:21:49] you approximate, or 0.2, you know?
[01:21:49 - 01:21:51] Is that clear?
[01:21:51 - 01:21:54] I'd sort of like, sometimes I start rambling and I'm just like, oh no, I don't know if I've,
[01:21:54 - 01:21:57] actually see it in your thing useful.
[01:21:57 - 01:22:00] So the mess that you'll put in your calculation needs to be the total mess.
[01:22:00 - 01:22:05] If you're doing a premium structure, then this upper support force needs to be taken into
[01:22:05 - 01:22:10] consideration because when you have that upper membe obviously the forces in the Y are going
[01:22:10 - 01:22:14] to have to equal and this gives you that unknown that you'll need to know to find
[01:22:14 - 01:22:16] other angle to get that force.
[01:22:16 - 01:22:17] Cool.
[01:22:17 - 01:22:24] Yep.
[01:22:24 - 01:22:29] So the measurement of the dimensions for two infrastructures happens at 20 kg of mass
[01:22:29 - 01:22:30] supplied.
[01:22:30 - 01:22:31] Yeah.
[01:22:31 - 01:22:34] So it actually, yeah, 20 kg of masses.
[01:22:34 - 01:22:41] So actually we have 20 plus the mass of the hook plus the mass of the chain and load, which
[01:22:41 - 01:22:49] we can see on there is 0.65 and 0.69.
[01:22:49 - 01:22:50] Yeah.
[01:22:50 - 01:22:51] Cool.
[01:22:51 - 01:22:52] Yeah.
[01:22:52 - 01:22:58] 1, 2.
[01:22:58 - 01:22:59] Yeah.
[01:22:59 - 01:23:05] If you have a two-year structure that fails before 20 kgs, it's good question.
[01:23:05 - 01:23:08] Well, we won't be able to measure on the day real quickly.
[01:23:08 - 01:23:10] We won't be able to measure the dimensions.
[01:23:10 - 01:23:13] So you'll just get whatever mass you've got.
[01:23:13 - 01:23:17] You wouldn't get the penalty because you probably don't deserve the penalty at that point
[01:23:17 - 01:23:18] if you don't need.
[01:23:18 - 01:23:23] You know, if you're available 20 kgs and you've not got the first all the second marks,
[01:23:23 - 01:23:25] you'll have some sort of strength to write ratio.
[01:23:25 - 01:23:27] You'll be based on your predicted load.
[01:23:27 - 01:23:32] So the max of the marks you can get is 10 there and probably is not going to fail
[01:23:32 - 01:23:36] be predicted failure mode, otherwise something sort of sucks is happening before you've
[01:23:36 - 01:23:38] calculated if you know what I mean.
[01:23:38 - 01:23:39] Yeah.
[01:23:39 - 01:23:44] If you calculate, you think to fail before 20 kgs then, yeah.
[01:23:44 - 01:23:45] So yeah.
[01:23:45 - 01:23:49] If you don't get to it, then we can't penalize you because you can't measure it.
[01:23:49 - 01:23:50] Cool.
[01:23:50 - 01:23:53] If you do, then you would start.
[01:23:53 - 01:23:55] Me personally.
[01:23:55 - 01:23:58] Now or like when I was a third year.
[01:23:58 - 01:24:03] Now, now I'll just do a two-year structure because I'd like to think that I can trust
[01:24:03 - 01:24:08] my calculations, but at the time I did a three-minute structure, it was very slim.
[01:24:08 - 01:24:13] I think it was like second or third lives in the class.
[01:24:13 - 01:24:16] Now I remember doing some crazy machining.
[01:24:16 - 01:24:22] It was like plus or minus like 500 or something of my time.
[01:24:22 - 01:24:27] Yeah, I knew exactly what mess would break out, but then we actually might have before
[01:24:27 - 01:24:28] something that I was like.
[01:24:28 - 01:24:34] We win a bit to low on our factor of safety for buckling, which could kind of flow nicely
[01:24:34 - 01:24:38] into talking about buckling if there's no other questions.
[01:24:38 - 01:24:43] Cool.
[01:24:43 - 01:24:48] So I found it to remember what I've got on the slides, but I'm going to take this by the
[01:24:48 - 01:24:50] horns and talk about buckling for a little bit.
[01:24:50 - 01:24:53] So we've got about 15, 16, 30 minutes to go.
[01:24:53 - 01:24:58] We'll probably finish it 22 since we didn't have a huge crack in the middle, but it might
[01:24:58 - 01:25:00] be 18 minutes too.
[01:25:00 - 01:25:06] So what I'm going to do is unfortunately for you guys some reading, I guess.
[01:25:06 - 01:25:13] So what we see here is a snippet from Shugley.
[01:25:13 - 01:25:18] It might not be the same page number and the version that you might have.
[01:25:18 - 01:25:26] And you'll see that there are two versions of this equation, right?
[01:25:26 - 01:25:35] So sometimes when you look it up, you might see a version that says PCR equals pi squared
[01:25:35 - 01:25:43] EI over K L squared, right?
[01:25:43 - 01:25:45] So this is another version.
[01:25:45 - 01:25:50] Same thing though.
[01:25:50 - 01:25:55] So if the version that of the buckling equation that you have has the K on the bottom, obviously
[01:25:55 - 01:26:00] refer to the diagram that they have and the values that they define there, not the ones
[01:26:00 - 01:26:03] in this because they'll be inverse, right?
[01:26:03 - 01:26:08] You don't have your vector star with, because otherwise sometimes they get people panicked
[01:26:08 - 01:26:13] that not everything's used the same notation, which is like just classic for engineering.
[01:26:13 - 01:26:18] So here we see here the fact to see is called the inconversion constant and it may
[01:26:18 - 01:26:26] have any of the theoretical values, emphasizing theoretical of a quarter, one, two, or four,
[01:26:26 - 01:26:29] depending upon the manner in which the load is applied.
[01:26:29 - 01:26:38] In practice, it is difficult if not impossible to fix the column ends so that the factors
[01:26:38 - 01:26:42] of C equals two will see equals four will apply.
[01:26:42 - 01:26:51] So for, for emphasis, I'll read this line again just because this could be where things could
[01:26:51 - 01:26:58] go wrong if you were to under or to use an optimized or use only the theoretical value.
[01:26:58 - 01:27:05] So in practice, it is difficult if not impossible to fix the column ends so that the factors
[01:27:05 - 01:27:09] of C equals two or C equals four will apply.
[01:27:09 - 01:27:17] Even if the ends are welded, some deflection will occur because of this, some designers never use a value
[01:27:17 - 01:27:20] of C greater than unity.
[01:27:20 - 01:27:22] So greater than one.
[01:27:22 - 01:27:23] All right?
[01:27:23 - 01:27:31] So what we see here in this table below is that for each of our end conditions, which are related
[01:27:31 - 01:27:38] to these diagrams up here, so we can see here both ends rounded or pivoted, would be our fixed
[01:27:38 - 01:27:39] fixed, right?
[01:27:39 - 01:27:47] So this would be like, what would be a, I know it's fixed for x-ray, rounder would be a, right?
[01:27:47 - 01:27:50] Yeah, seems like it's put small, maybe.
[01:27:50 - 01:27:53] Whoa, that was intense.
[01:27:53 - 01:27:54] Yeah?
[01:27:54 - 01:28:00] So we can see here that we get our theoretical value, which says in theory it's one, the
[01:28:00 - 01:28:04] conservative value is one, and the recommended value is one.
[01:28:04 - 01:28:06] How nice is that?
[01:28:06 - 01:28:11] So we have a, for our fixed free, which is I think C above, right?
[01:28:11 - 01:28:13] We look at that up here.
[01:28:13 - 01:28:16] Number C, fixed at the bottom, it's free at the top.
[01:28:16 - 01:28:20] We see that a theoretical value is a quarter.
[01:28:20 - 01:28:25] The conservative value is a quarter, and the recommended value is a quarter.
[01:28:25 - 01:28:28] Why did they not change it?
[01:28:28 - 01:28:37] So if we look at our equation, if C is smaller, if C was bigger, would that make it more likely
[01:28:37 - 01:28:45] likely to happen, or like which is more conservative or less conservative?
[01:28:45 - 01:28:50] Yeah, so the larger the C value is, the larger the critical buckling force, which is saying
[01:28:50 - 01:28:52] this is where it's going to buckle.
[01:28:52 - 01:28:53] Yeah?
[01:28:53 - 01:28:57] So if you were to use, if you were to be conservative, you would use a smaller value, and
[01:28:57 - 01:29:03] because this is the smallest value, that's why they said there's no smaller value to use, right?
[01:29:03 - 01:29:07] Well, and so then this is where things get super interesting.
[01:29:07 - 01:29:15] If you've got fixed rounded, so fixed pinned, which is like D above, I believe.
[01:29:15 - 01:29:16] Yeah?
[01:29:16 - 01:29:19] D above, fixed at the bottom, pinned at the top.
[01:29:19 - 01:29:24] You can see that because of this ratio of where they're effective length is, that gives us
[01:29:24 - 01:29:28] a theoretical value of two for our in-conditioned constant.
[01:29:28 - 01:29:35] If you want to be conservative, you'd use a conditioned value of one, and if you want to use the recommended value,
[01:29:35 - 01:29:38] you could use 1.2, right?
[01:29:38 - 01:29:46] So I think this handout is also on-learn under the two tools lines, if you're wanting to check it again.
[01:29:46 - 01:29:47] Cool.
[01:29:47 - 01:29:52] So in that case, you can see that even though the theoretical value is two, they're saying
[01:29:52 - 01:29:57] use one to make sure that you don't buckle, because it'll be real shame if you think buckle, right?
[01:29:57 - 01:30:02] And then here where it gets even crazier, if you're having flat dinner, and you have to say like,
[01:30:02 - 01:30:09] oh, we learned something interesting today, you'll be like, well, the theoretical value of a fixed fixed-in-conditioned
[01:30:09 - 01:30:14] will buckle, and it's four, but the conservative value is one.
[01:30:14 - 01:30:18] Which is crazy because there's a factor of four different, right?
[01:30:18 - 01:30:25] So like, that's saying that in reality, the value that you would trust is a quarter of what the theory says.
[01:30:25 - 01:30:29] And so this is possibly where people sometimes might get into trouble,
[01:30:29 - 01:30:37] where they like to use this theoretical value instead of either the conservative or the recommended value, which is significantly less.
[01:30:37 - 01:30:42] Yeah? And in general, I mean, there's not many equations that you'll experience as an engineer.
[01:30:42 - 01:30:50] We have a wrong, in-conditional, wrong assumption could put you a difference of 16 between the worst and the best here, right?
[01:30:50 - 01:30:53] So, again, something kind of interesting.
[01:30:53 - 01:31:03] And so, hopefully, if I've done my job right, there should be some steps here about buckling.
[01:31:03 - 01:31:07] So we had this buckling here, we've gone through this, so we can take that off.
[01:31:07 - 01:31:10] Here we see an example of buckling failure.
[01:31:10 - 01:31:12] And so this is a good question for you.
[01:31:12 - 01:31:17] So what would the in-conditions be for this value, for this member on the left?
[01:31:17 - 01:31:21] So I'm going to just tell me, fixed, rounded, cool.
[01:31:21 - 01:31:30] So based on how our handout, fixed, rounded, what value would you use for your C?
[01:31:30 - 01:31:33] You would use one. Cool.
[01:31:33 - 01:31:35] And we're on both, all right?
[01:31:35 - 01:31:40] Now, next one, what would we use for this?
[01:31:40 - 01:31:50] What theoretically, top is acting like a schoon that has got a real tight tolerance up here.
[01:31:50 - 01:31:55] Yeah, it is rotated, yeah?
[01:31:55 - 01:32:01] So look at where the pin is. What do we want to say?
[01:32:01 - 01:32:04] Well, at the bottom, oh, yeah, okay, fixed, fixed, right?
[01:32:04 - 01:32:05] The bottom is obviously fixed.
[01:32:05 - 01:32:09] The top, people could say that that's fixed, that these are tight times.
[01:32:09 - 01:32:13] If you knew, like, hot with drills and big holes, then it might actually kind of
[01:32:13 - 01:32:16] slopping, you know, it's definitely like a pin, right?
[01:32:16 - 01:32:18] But you can see we've got our member here.
[01:32:18 - 01:32:20] That's exactly the kind of locust here.
[01:32:20 - 01:32:23] So this one here, where we've got a pin and a pin.
[01:32:23 - 01:32:26] If it's buckling like this, kind of obvious that it's pin-pin.
[01:32:26 - 01:32:30] So this one here, you could be tempted to say that that's fixed fixed.
[01:32:30 - 01:32:33] But really, what the theory is saying to you is that if you want to be consumed,
[01:32:33 - 01:32:36] you'd be much closer to saying that it's still acting like pin-pin.
[01:32:36 - 01:32:42] Because really, it's impossible to get this to actually be fixed unless we have some pretty
[01:32:42 - 01:32:45] heavy engineering there, right?
[01:32:45 - 01:32:47] Cool. Sweet. All right.
[01:32:47 - 01:32:48] We're doing great.
[01:32:48 - 01:32:53] So with that, there's one more question.
[01:32:53 - 01:32:57] There's another one that we can see buckling the other way.
[01:32:57 - 01:33:00] We can talk about eccentric loads as well.
[01:33:00 - 01:33:04] So with eccentric loading, we might just happen.
[01:33:04 - 01:33:07] So this is one of those things that might be a little bit too early to discuss about.
[01:33:07 - 01:33:14] But in terms of your compression members, what types of members could you use?
[01:33:14 - 01:33:19] Well, it's a classic one that we've just seen here.
[01:33:19 - 01:33:24] So I'll just say, types of compression.
[01:33:24 - 01:33:29] So we've got i-beam.
[01:33:29 - 01:33:31] Yeah, once again.
[01:33:31 - 01:33:33] Yep. What else could you do?
[01:33:33 - 01:33:37] Could you do an h-beam anything else?
[01:33:37 - 01:33:41] Could Navy try to square-hollers section or RHS?
[01:33:41 - 01:33:45] I don't know how good your bending skills are or how you would glue that.
[01:33:45 - 01:33:49] It could be quite problematic, but maybe people are nifty and they can get it to work.
[01:33:49 - 01:33:50] Yep.
[01:33:50 - 01:33:51] What's that?
[01:33:51 - 01:33:52] DSE.
[01:33:52 - 01:33:57] DSE.
[01:33:57 - 01:33:58] DSE.
[01:33:58 - 01:33:59] C-beam here.
[01:33:59 - 01:34:00] Sorry.
[01:34:00 - 01:34:03] Just like my brain took a second to compute.
[01:34:03 - 01:34:06] Yeah, so it could be like a just a C-beam like that, right?
[01:34:06 - 01:34:07] Look at that.
[01:34:07 - 01:34:15] That's sort of, I mean, that's meant to be longer, but obviously H, obviously high.
[01:34:15 - 01:34:16] Cool.
[01:34:16 - 01:34:19] So these are all going to have different considerations as to where the pinholes go.
[01:34:19 - 01:34:23] You can see this one here, the pins are like here and then these members with this.
[01:34:23 - 01:34:25] Is it area where it is not?
[01:34:25 - 01:34:32] But for those members here, I don't think we have had the one that has any other shapes
[01:34:32 - 01:34:34] that there could be, any other letters that we could use.
[01:34:34 - 01:34:35] T-beam.
[01:34:35 - 01:34:37] Was there another one?
[01:34:37 - 01:34:38] L.
[01:34:38 - 01:34:39] Yeah, or an L.
[01:34:39 - 01:34:49] Yeah, so for some of these ones, there may be times when the centroid of your nimba is not in the
[01:34:49 - 01:34:53] center of the cross section of the rat.
[01:34:53 - 01:34:55] I don't know if I'm described there.
[01:34:55 - 01:34:57] Well, I didn't know that.
[01:34:57 - 01:35:02] Yeah, so the center of like the bending wouldn't be at the center of your nimba.
[01:35:02 - 01:35:05] And because of that, like where your puns are, if your puns are not where your center of
[01:35:05 - 01:35:12] bending or center of centroid is, then that's going to cause an eccentric buckling load.
[01:35:12 - 01:35:15] Yeah, so sometimes I can show some examples.
[01:35:15 - 01:35:21] These ones here, depending on the dimensions, they could be susceptible to a centric buckling.
[01:35:21 - 01:35:26] But if you've got an H-beam or a i-beam or a square hollow section where the centroid
[01:35:26 - 01:35:31] is in the middle of where the loading is, you know, it'll be kind of not a consideration
[01:35:31 - 01:35:33] that you need to do.
[01:35:33 - 01:35:39] So if you're assuming that you're centroid, protecting along your centroid, you're all good.
[01:35:39 - 01:35:45] If it's like a t-beam and you have your pun here, well, this might be with a low
[01:35:45 - 01:35:49] supply and then maybe this is where the center might be even closer there.
[01:35:49 - 01:35:51] You know, so there's a gap here.
[01:35:51 - 01:35:59] That could mean this is the load.
[01:35:59 - 01:36:02] Cool, so I do have a couple of little things to go over.
[01:36:02 - 01:36:04] So let's just keep moving.
[01:36:04 - 01:36:06] Hopefully that's just good for a note.
[01:36:06 - 01:36:09] I'm sure we'll come back to that if people have kind of problems.
[01:36:09 - 01:36:14] But it means that you don't have to do, I'd say do the, do the, do the, you will buckling
[01:36:14 - 01:36:15] in the first instance.
[01:36:15 - 01:36:21] And if you've got a t-beam or something similar with a, the pun with a pun is located as
[01:36:21 - 01:36:26] not where the centroid of your cross-section is, then make sure that you probably check
[01:36:26 - 01:36:27] that out.
[01:36:27 - 01:36:30] If that's something that you're worried about because that's how some of the people fail
[01:36:30 - 01:36:32] because they didn't do that calculation or check.
[01:36:32 - 01:36:35] Let us assume that it was close enough.
[01:36:35 - 01:36:37] Cool.
[01:36:37 - 01:36:39] Just quickly, we can spend one minute on it.
[01:36:39 - 01:36:48] If we were to try and make our, our minder be less resistant or less likely to buckle, what
[01:36:48 - 01:36:52] can we realistically do?
[01:36:52 - 01:36:55] Can we change pie?
[01:36:55 - 01:36:56] No.
[01:36:56 - 01:37:03] Can we change our in-conditioned constant?
[01:37:03 - 01:37:04] Not really.
[01:37:04 - 01:37:08] If we're using conservative, super conservative of one, not really, right?
[01:37:08 - 01:37:09] Cool.
[01:37:09 - 01:37:11] Can we change e?
[01:37:11 - 01:37:13] Oh, young's modulus.
[01:37:13 - 01:37:14] No.
[01:37:14 - 01:37:20] Unless you were somehow able to like change the properties of your aluminium, which realistically
[01:37:20 - 01:37:23] for all anti-napeps is not, right?
[01:37:23 - 01:37:24] Cool.
[01:37:24 - 01:37:26] Can we change i?
[01:37:26 - 01:37:27] Yes.
[01:37:27 - 01:37:29] So this one we can change?
[01:37:29 - 01:37:30] Can we change l?
[01:37:30 - 01:37:34] Yes, we could also change l depending on what our geometry is.
[01:37:34 - 01:37:40] So that's the classic engineering design optimization problem where some geometries might
[01:37:40 - 01:37:42] have different loads, because the links might be different.
[01:37:42 - 01:37:46] One might be lighter than the other, or able to be lighter than the other, right?
[01:37:46 - 01:37:51] So that's where it's your guys job to kind of either pick one and just optimise it from there,
[01:37:51 - 01:37:55] or as I'm saying, some people might like pick two and then work out which one is actually
[01:37:55 - 01:37:56] better.
[01:37:56 - 01:37:59] That's your guys' decision as to what you do.
[01:37:59 - 01:38:04] And you can see obviously the link being squared is going to have a larger impact when you change
[01:38:04 - 01:38:09] it compared to just changing your eye value, right?
[01:38:09 - 01:38:10] Cool.
[01:38:10 - 01:38:18] So, from there, we do have just one more thing that I want to kind of talk about and it should
[01:38:18 - 01:38:20] hopefully take less than the time that we need.
[01:38:20 - 01:38:27] So in terms of a discussion about riveting and adheres, I'm going to do that on next week,
[01:38:27 - 01:38:30] because I don't think we're quite there yet.
[01:38:30 - 01:38:35] The best thing is that you work out how you're going to what kind of shape the environment
[01:38:35 - 01:38:40] you want and you might come up with ideas and then we can talk about that, unless we somehow
[01:38:40 - 01:38:42] do this really quickly.
[01:38:42 - 01:38:46] And then do we want to do a list or do we want to do this verbally?
[01:38:46 - 01:38:50] This is your guys' question answer time.
[01:38:50 - 01:38:52] We do want the list.
[01:38:52 - 01:38:57] It's just like last year, I don't know why, but everyone was like anti-list.
[01:38:57 - 01:39:04] And I'm like kind of pro-list and then it was like a bit tense.
[01:39:04 - 01:39:13] So all I want to do is, for example, if we have that exact same, I feel that the wrong way
[01:39:13 - 01:39:15] or wrong way around it, that's okay.
[01:39:15 - 01:39:17] Imagining that this is exactly the same as we had.
[01:39:17 - 01:39:20] So now that this is our answer.
[01:39:20 - 01:39:22] Thanks for telling me.
[01:39:23 - 01:39:25] I wish I wasn't streaming it.
[01:39:25 - 01:39:26] Look at that.
[01:39:26 - 01:39:27] It's terrible.
[01:39:27 - 01:39:36] But imagining that this bit here, which I've drawn twice as big as 50, so the bit was 100,
[01:39:36 - 01:39:40] means that we would get the same values here.
[01:39:40 - 01:39:41] Right?
[01:39:41 - 01:39:54] We've got compression, compression, tension.
[01:39:54 - 01:40:11] So four member, one, three.
[01:40:11 - 01:40:13] What calculations do we do?
[01:40:13 - 01:40:15] No.
[01:40:15 - 01:40:16] We don't know what the shape is.
[01:40:16 - 01:40:20] I don't know what orientation it is, but generally speaking, we should still be able to
[01:40:20 - 01:40:23] list what kind of calculations that we could do.
[01:40:23 - 01:40:26] Anyone who got any ideas to start us off?
[01:40:26 - 01:40:30] Can we further the map sheet if we need to?
[01:40:30 - 01:40:36] Come on guys, it's time.
[01:40:36 - 01:40:43] I want to go home, but we need to get this list done.
[01:40:43 - 01:40:45] Normal stress, good start.
[01:40:45 - 01:40:49] So normal stress, which would be away from any stress concentration, right?
[01:40:50 - 01:40:57] I'll just say away from Sc.
[01:40:57 - 01:40:58] Coop, visit, huh?
[01:40:58 - 01:41:01] Well, how's could we calculate?
[01:41:01 - 01:41:06] Coops, we could go stress at Sc.
[01:41:06 - 01:41:09] Coop, what else could we do?
[01:41:09 - 01:41:11] Coop, be there in stress.
[01:41:11 - 01:41:12] What else could we do?
[01:41:12 - 01:41:15] Anything else?
[01:41:15 - 01:41:17] Buckling, probably not.
[01:41:17 - 01:41:22] Buckling, we'll come out next to you just a little bit early.
[01:41:22 - 01:41:26] The other thing could be, depending on how our minder is, so if this is our minder,
[01:41:26 - 01:41:31] we've got a hole, there could also be some stress in here.
[01:41:31 - 01:41:42] So I'm going to say like stress.
[01:41:42 - 01:41:49] So there could be stress that pins that could also have tear out.
[01:41:49 - 01:41:52] This is me being very, very thorough.
[01:41:52 - 01:41:53] Yeah?
[01:41:53 - 01:41:54] I like you can imagine that.
[01:41:54 - 01:42:00] If this hole was, yeah, it's good.
[01:42:00 - 01:42:03] I kind of don't want to show the drawing, but you know.
[01:42:03 - 01:42:04] It's all good.
[01:42:04 - 01:42:06] I'm not going to show it.
[01:42:06 - 01:42:07] Yeah.
[01:42:07 - 01:42:11] Can you imagine that where the holes are, you could do the stress above them below the
[01:42:11 - 01:42:12] hole.
[01:42:12 - 01:42:22] If the hole was really close to the end, then maybe it would actually just tear out.
[01:42:22 - 01:42:29] And the other one that I was looking at was the stress here in the pins, right?
[01:42:29 - 01:42:30] Cool.
[01:42:30 - 01:42:42] Now quickly for our compression members, oh man, what else can we do?
[01:42:42 - 01:42:45] Someone said it before, what was it?
[01:42:45 - 01:42:47] Buckling.
[01:42:47 - 01:42:57] And I guess to work out buckling, we need to calculate eye values, right?
[01:42:57 - 01:43:01] What else can we also do?
[01:43:01 - 01:43:02] Possibly.
[01:43:02 - 01:43:04] I mean, not many.
[01:43:04 - 01:43:10] Some people might do eccentric buckling.
[01:43:10 - 01:43:13] Oh man.
[01:43:13 - 01:43:17] And if we wanted to be really detailed, which I guess we are today because we can do
[01:43:17 - 01:43:19] more completeness, I guess.
[01:43:19 - 01:43:27] I'm just going to write as well in buckling, which we may come back to.
[01:43:27 - 01:43:31] But obviously this part here where the cross-section is no longer the same, which you'd
[01:43:31 - 01:43:33] also probably check that it's not going to buckle here.
[01:43:33 - 01:43:36] But we'll talk about that a little bit next week.
[01:43:36 - 01:43:39] So I think it's probably jumping the gun to go.
[01:43:39 - 01:43:42] And the too much detail there.
[01:43:42 - 01:43:44] Any other questions that we could do?
[01:43:44 - 01:43:53] Is there anything on that March sheet, better say?
[01:43:53 - 01:44:00] So the only, the only other one would be our pins.
[01:44:00 - 01:44:01] Right.
[01:44:01 - 01:44:02] Have a great week in everyone.
[01:44:02 - 01:44:56] I've forgotten that my bed is the two-mail structure.
[01:44:56 - 01:45:02] I'm guessing the biggest problem is the moving up the tower.
[01:45:32 - 01:45:34] It's quite useful for instance.
[01:45:34 - 01:45:37] So even though it's very good, should go up to the footwork point.
[01:45:37 - 01:45:39] So as you put all the metal in it,
[01:45:39 - 01:45:42] there you go, get smaller, there will be a bit of going there.
[01:45:42 - 01:45:45] So I really want to make sure that it's not as accessible.
[01:45:45 - 01:45:47] You don't have to worry too much about where it starts.
[01:45:47 - 01:45:49] You'll be able to just, if you give it a lot of places,
[01:45:49 - 01:45:53] you put my five or whatever, otherwise it won't be safe.
[01:45:53 - 01:45:55] It's a good idea.
[01:45:55 - 01:45:58] On the day, the people are doing a few new shots.
[01:45:58 - 01:46:01] They're kind of hold it to make sure that there is some teaching
[01:46:01 - 01:46:05] that's on their own, they'll be in a bit of teaching either.
[01:46:05 - 01:46:07] And then they can do a thing.
[01:46:07 - 01:46:11] Then we just check in 20 in the stages and the bounds of it.
[01:46:11 - 01:46:13] And that's all the two.
[01:46:13 - 01:46:14] Yeah.
[01:46:14 - 01:46:15] Yeah.
[01:46:15 - 01:46:16] Yeah.
[01:46:16 - 01:46:17] Yeah.
[01:46:17 - 01:46:18] Four.
[01:46:18 - 01:46:19] Four.
[01:46:19 - 01:46:20] Great.
[01:46:20 - 01:46:21] Yeah.
[01:46:21 - 01:46:22] Yeah.
[01:46:22 - 01:46:23] Go.
[01:46:23 - 01:46:24] Yeah.
[01:46:24 - 01:46:25] Yeah.
[01:46:25 - 01:46:26] Yeah.
[01:46:26 - 01:46:27] Yeah.
[01:46:27 - 01:46:28] Yeah.
[01:46:28 - 01:46:29] Yeah.
[01:46:29 - 01:46:31] Yeah.
[01:46:31 - 01:46:33] Yeah.
[01:46:33 - 01:46:35] Yeah.
[01:46:35 - 01:46:38] Yeah.
[01:46:38 - 01:46:39] Yeah.
[01:46:39 - 01:46:48] Yeah.
[01:46:48 - 01:46:49] Yeah.
[01:46:49 - 01:46:51] Yeah.
[01:46:51 - 01:46:52] It should be enough at the end of it.
[01:46:52 - 01:46:53] Yeah.
[01:46:53 - 01:46:54] Yeah.
[01:46:54 - 01:46:56] You know, you went 20 tests,
[01:47:26 - 01:47:29] So it's just a hundred more than that's what the force will say.
[01:47:29 - 01:47:31] It doesn't actually matter if it's a roller or not.
[01:47:31 - 01:47:32] And the only reason you look for it,
[01:47:32 - 01:47:34] the only thing that the roller means is they're in a dark room.
[01:47:34 - 01:47:36] It could move, if it could move,
[01:47:36 - 01:47:39] but if you have an underneath it, they would go to a cat.
[01:47:39 - 01:47:41] Yeah, but it's just going to see the force.
[01:47:41 - 01:47:43] Yeah. But that's the beauty of the assignment.
[01:47:43 - 01:47:44] It's like, what's your plan?
[01:47:44 - 01:47:45] I think that they say we're going to be like,
[01:47:45 - 01:47:47] oh, yeah, this is always a thing.
[01:47:47 - 01:47:48] I think that's a good idea.
[01:47:48 - 01:47:49] I think that's a good idea.
[01:47:49 - 01:47:50] I think that's a good idea.
[01:47:50 - 01:47:51] I think that's a good idea.
[01:47:51 - 01:47:52] There's a two memory of it.
[01:47:52 - 01:47:53] Yeah.
[01:47:53 - 01:47:54] I think that's a good idea.
[01:47:54 - 01:47:55] I think we're going to work down there
[01:47:55 - 01:47:57] and we want to bring the abs down.
[01:47:57 - 01:47:58] Down, down, down like around.
[01:47:58 - 01:48:00] There's never ends up sometimes.
[01:48:00 - 01:48:01] We'll look one other time.
[01:48:01 - 01:48:03] So that way you do it now.
[01:48:03 - 01:48:04] Can you just say,
[01:48:04 - 01:48:05] what can we get that part of force?
[01:48:05 - 01:48:06] I'm not sure.
[01:48:06 - 01:48:07] I understand you question about it.
[01:48:07 - 01:48:08] Oh, okay.
[01:48:08 - 01:48:09] I think that's a good idea.
[01:48:09 - 01:48:10] Okay.
[01:48:10 - 01:48:11] This is rational.
[01:48:11 - 01:48:12] I think if you did it,
[01:48:12 - 01:48:14] it's a pretty muddy diagram.
[01:48:14 - 01:48:15] Breathe in the right amount of force.
[01:48:15 - 01:48:16] I'm trying to do it, but yeah.
[01:48:16 - 01:48:17] Yeah.
[01:48:17 - 01:48:18] Yeah.
[01:48:18 - 01:48:20] He's selling it and he's going to have a good,
[01:48:20 - 01:48:21] good force.
[01:48:21 - 01:48:22] Yeah.
[01:48:22 - 01:48:23] Yeah.
[01:48:23 - 01:48:24] Yeah.
[01:48:24 - 01:48:25] Yeah.
[01:48:25 - 01:48:26] Yeah.
[01:48:26 - 01:48:27] Yeah.
[01:48:27 - 01:48:28] Yeah.
[01:48:28 - 01:48:29] Yeah.
[01:48:29 - 01:48:30] Yeah.
[01:48:30 - 01:48:31] Yeah.
[01:48:31 - 01:48:32] So if you do have a nice idea,
[01:48:32 - 01:48:33] if you're doing that thing like that,
[01:48:33 - 01:48:36] if you have to do a slight gain of ground,
[01:48:36 - 01:48:37] if you do,
[01:48:37 - 01:48:40] I don't want to say it's just that looks like this.
[01:48:40 - 01:48:41] Yeah.
[01:48:41 - 01:48:42] It's not.
[01:48:42 - 01:48:43] It's not.
[01:48:43 - 01:48:44] It's not.
[01:48:44 - 01:48:45] It's not.
[01:48:45 - 01:48:46] It's not.
[01:48:46 - 01:48:47] It's not.
[01:48:47 - 01:48:48] It's like.
[01:48:48 - 01:48:49] It's like.
[01:48:49 - 01:48:50] Yeah.
[01:48:50 - 01:48:51] Yeah.
[01:48:51 - 01:48:52] Yeah.
[01:48:52 - 01:48:53] Yeah.
[01:48:53 - 01:48:54] I don't want to tell you that.
[01:48:54 - 01:48:55] Yeah.
[01:48:55 - 01:48:59] Let's turn it kinda probably,
[01:48:59 - 01:49:02] obviously you're stuck in the right side.
[01:49:02 - 01:49:03] Right anchored are back.
[01:49:03 - 01:49:04] I want to put that.
[01:49:04 - 01:49:05] They make it last.
[01:49:05 - 01:49:06] We're actually having to do,
[01:49:06 - 01:49:07] we're just going to put that.
[01:49:07 - 01:49:08] One layer of work in here.
[01:49:08 - 01:49:10] We made a picture of how it could hold the layer.
[01:49:10 - 01:49:11] Oh yeah,
[01:49:11 - 01:49:12] Yeah.
[01:49:12 - 01:49:13] Yeah.
[01:49:13 - 01:49:14] Kind of people know something,
[01:49:14 - 01:49:15] we're actually talking about something
[01:49:15 - 01:49:16] that we do a stick because we do a stick
[01:49:16 - 01:49:17] to tango andunk of the water.
[01:49:17 - 01:49:18] adjusting,
[01:49:18 - 01:49:23] and the thing is as you add more and more of this,
[01:49:24 - 01:49:26] the force for this paper goes up
[01:49:26 - 01:49:27] and then we'll make that for A,
[01:49:27 - 01:49:28] we'll be spotless.
[01:49:28 - 01:49:30] I'm not supposed to be all out of here.
[01:49:30 - 01:49:31] Hot 500.
[01:49:32 - 01:49:34] How do you get a new one?
[01:49:34 - 01:49:35] Anybody want to see that out of it?
[01:49:35 - 01:49:36] Yeah, I read it.
[01:49:36 - 01:49:37] Yeah.
[01:49:37 - 01:49:38] More what you get, yeah?
[01:49:38 - 01:49:40] But this wasn't going to be like,
[01:49:40 - 01:49:41] you know what I'm doing?
[01:49:41 - 01:49:43] So the money orders, yeah, also,
[01:49:43 - 01:49:43] yeah, pulling it.
[01:49:45 - 01:49:46] That's why I think about it.
[01:49:46 - 01:49:47] You're just looking at it.
[01:49:47 - 01:49:49] It gives out roll-ups.
[01:49:49 - 01:49:49] I don't mind.
[01:49:49 - 01:49:51] You know what's about something bad?
[01:49:51 - 01:49:53] Yes, something bad.
[01:49:53 - 01:49:55] It's a good thing.
[01:49:55 - 01:49:56] You've got something.
[01:49:56 - 01:49:57] You can't get it here.
[01:49:57 - 01:49:58] I know.
[01:49:58 - 01:49:59] I don't know.
[01:49:59 - 01:50:00] Can't get this here.
[01:50:00 - 01:50:01] The sports game,
[01:50:01 - 01:50:03] you know, the sports game will get like a sports game.
[01:50:03 - 01:50:04] You can see it's in front of it.
[01:50:04 - 01:50:06] And so we want to compute.
[01:50:06 - 01:50:08] I wouldn't want to have a little bit for a night.
[01:50:08 - 01:50:09] One last time.
[01:50:09 - 01:50:10] If you're doing a training instruction,
[01:50:10 - 01:50:12] these two have to be updated.
[01:50:12 - 01:50:13] One is it work,
[01:50:13 - 01:50:15] but then you can get your own math.
[01:50:15 - 01:50:17] You can get your own math.
[01:50:17 - 01:50:19] You can get your own math.
[01:50:19 - 01:50:20] You can get your own math.
[01:50:20 - 01:50:22] You can get your math.
[01:50:22 - 01:50:23] You can get your math.
[01:50:23 - 01:50:25] So when it's added,
[01:50:25 - 01:50:26] what is it?
[01:50:26 - 01:50:27] That's what you're not measuring.
[01:50:27 - 01:50:28] We don't get it.
[01:50:28 - 01:50:30] It's not going to be a good idea.
[01:50:30 - 01:50:31] You can get my math.
[01:50:31 - 01:50:32] You can get my math.
[01:50:32 - 01:50:33] You can get my math.
[01:50:33 - 01:50:36] I mean, do you have to do two free words.
[01:50:36 - 01:50:38] At least I'm ready to make the free.
[01:50:38 - 01:50:40] I think it's a good idea about that.
[01:50:40 - 01:50:41] I think I'll be sure it was a good idea.
[01:50:41 - 01:50:43] You can rest your head on the show.
[01:50:43 - 01:50:43] You can rest your head on the show.
[01:50:43 - 01:50:44] Yeah.
[01:50:44 - 01:50:46] You can rest my math.
[01:50:46 - 01:50:47] What's the good idea right now?
[01:50:47 - 01:50:48] All right.
[01:50:48 - 01:50:50] I wouldn't want to go ahead and put that thing that was good.
[01:50:50 - 01:50:51] Good?
[01:50:51 - 01:50:52] You can just put it in a little bit.
[01:50:52 - 01:50:54] Can you get a little bit of the coloring?
[01:50:54 - 01:50:56] I just put the color in the middle.
[01:50:56 - 01:50:57] So you can see it's really bad.
[01:50:57 - 01:50:58] I'm sure it's a good idea.
[01:50:58 - 01:50:59] Because we're not going to do that.
[01:50:59 - 01:51:00] But I know we're gone.
[01:51:00 - 01:51:01] I'm actually going to put it in.
[01:51:01 - 01:51:03] So you're going to put it in the show.
[01:51:03 - 01:51:04] Yeah.
[01:51:04 - 01:51:05] So the training structure,
[01:51:05 - 01:51:07] the idea is that at the top,
[01:51:07 - 01:51:11] it is some math by having a role.
[01:51:11 - 01:51:12] Yeah.
[01:51:12 - 01:51:16] So we needed the sum of the forces of the Y at 20 kgs.
[01:51:16 - 01:51:18] You have to do it when you're getting a number of forces.
[01:51:18 - 01:51:22] You can do it when you're working on what the angle of that is.
[01:51:22 - 01:51:24] But then would you know you're changing that in an hour?
[01:51:24 - 01:51:26] How much force you are?
[01:51:26 - 01:51:28] I think you're going to take the unit.
[01:51:28 - 01:51:31] You're going to do two, but if you don't want the brake at that force,
[01:51:31 - 01:51:32] you have to do the brake like that.
[01:51:32 - 01:51:35] And again, you know, the force that's getting about the unit.
[01:51:35 - 01:51:36] Right?
[01:51:36 - 01:51:37] Yeah.
[01:51:37 - 01:51:38] Yeah?
[01:51:38 - 01:51:40] I think that's the best for your pushing work.
[01:51:40 - 01:51:41] Yeah.
[01:51:41 - 01:51:43] So basically, if you're doing two new structures,
[01:51:43 - 01:51:46] there's a joint here at the moment we have to do 20 kgs.
[01:51:46 - 01:51:48] So you have to do a different free 20 dollar gap at the 20 kgs.
[01:51:48 - 01:51:51] You work out what the angle is with 20 kgs.
[01:51:51 - 01:51:54] And make sure that the joint here is working.
[01:51:54 - 01:51:58] And then if you want a 30 kg, it's the same thing.
[01:51:58 - 01:51:59] The 30 kgs.
[01:51:59 - 01:52:02] You don't actually care if the joint can change it.
[01:52:02 - 01:52:03] I do a point.
[01:52:03 - 01:52:04] I do a point.
[01:52:04 - 01:52:05] I do a point.
[01:52:05 - 01:52:06] I do a point.
[01:52:06 - 01:52:07] I do a point.
[01:52:07 - 01:52:08] I do a point.
[01:52:08 - 01:52:09] Okay.
[01:52:09 - 01:52:25] So we're going to pull some foot.
[01:52:25 - 01:52:37] I'm not sure what you're saying or what you're saying, but I'm not sure what you're saying
[01:52:37 - 01:52:38] or what you're saying.
[01:52:38 - 01:52:40] But you only get to see someone on the day.
[01:52:40 - 01:52:41] I don't know what they're saying.
[01:52:41 - 01:52:44] I want to like to find those things that you're saying.
[01:52:44 - 01:52:48] Yeah, but you would just use the, why can you just put the good one in the company?
[01:52:48 - 01:52:50] Because you're saying that.
[01:52:50 - 01:52:51] Yeah.
[01:52:51 - 01:52:57] I can still move the person, but I'm just going to chat because you could, but I'm not sure
[01:52:57 - 01:52:59] that would be beneficial for you to be in theory.
[01:52:59 - 01:53:04] Yeah, and I've not seen someone split that into the model of the media, but yeah, you could.
[01:53:04 - 01:53:05] Yeah.
[01:53:05 - 01:53:11] But then it also means like making sure that again one member and it seems like that.
[01:53:11 - 01:53:15] Like how I've been this like, now I've been this like this and I mean, there's like that.
[01:53:15 - 01:53:17] Yeah, I know that the force is going to extract them in there.
[01:53:17 - 01:53:18] Yeah.
[01:53:18 - 01:53:24] If you had like multiple, then all of a sudden you might have one on the side of the model
[01:53:24 - 01:53:25] and then start to see it.
[01:53:25 - 01:53:26] But it's centric.
[01:53:26 - 01:53:27] Yeah.
[01:53:27 - 01:53:28] I'm like, I think it's something you can see.
[01:53:28 - 01:53:29] Yeah.
[01:53:29 - 01:53:30] Yeah.
[01:53:30 - 01:53:32] If anyone had a part of this or if I might not call them, I'm not saying it.
[01:53:32 - 01:53:33] Yeah.
[01:53:33 - 01:53:39] I mean, I, I appreciate that I created thinking that my, yeah, my philosophy will always go
[01:53:39 - 01:53:43] over to like keeping the shape, the shape simple and it's not that you can do it optimise.
[01:53:43 - 01:53:48] Well, you can just, you know, put a picture in this look like or, you know, this can kind of
[01:53:48 - 01:53:51] decal design and this is actually actually put a picture in it.
[01:53:51 - 01:53:56] If we were to cock out this member and it's moving to the material, if you ran out of
[01:53:56 - 01:54:01] material or is it strictly on the, if you had a failure and there was not a speaker, the
[01:54:01 - 01:54:04] idea is that I have enough material for the number of people that are in it.
[01:54:04 - 01:54:05] Yeah.
[01:54:05 - 01:54:06] Yeah.
[01:54:06 - 01:54:07] Yeah.
[01:54:07 - 01:54:08] Yeah.
[01:54:08 - 01:54:09] Yeah.
[01:54:09 - 01:54:11] I'm saying it as that.
[01:54:11 - 01:54:16] On Tuesday, if you didn't have much material with Dover and then some happened, we'd work out
[01:54:16 - 01:54:17] something to make it.
[01:54:17 - 01:54:18] Yeah.
[01:54:18 - 01:54:19] Everyone's doing it.
[01:54:19 - 01:54:20] Yeah.
[01:54:20 - 01:54:21] Yeah.
[01:54:21 - 01:54:22] I definitely don't have enough for everyone.
[01:54:22 - 01:54:23] Yeah.
[01:54:23 - 01:54:24] Yes.
[01:54:24 - 01:54:25] Yeah.
[01:54:25 - 01:54:29] When we go to the last few examples of fractions, that are what we have made, and those
[01:54:29 - 01:54:31] were these, the chip.
[01:54:31 - 01:54:32] Chip block would work.
[01:54:32 - 01:54:33] Yes.
[01:54:33 - 01:54:35] There's a few ways we got a bit of this.
[01:54:35 - 01:54:39] You can imagine when we, I can't find them in, but I was kind of like, this is the best
[01:54:39 - 01:54:40] I've ever got.
[01:54:40 - 01:54:46] I'm gonna get rid of the drill trees and I forget the drill wonders too much when the
[01:54:46 - 01:54:48] Joe Lee is breaking hole and before he's not at the loss of, yeah.
[01:54:48 - 01:54:49] Yeah.
[01:54:49 - 01:54:50] Did you use a middle stock?
[01:54:50 - 01:54:51] I'm not even ashamed.
[01:54:51 - 01:54:52] Yeah.
[01:54:52 - 01:54:53] I didn't know that.
[01:54:53 - 01:54:54] Yeah.
[01:54:54 - 01:54:55] You know them not.

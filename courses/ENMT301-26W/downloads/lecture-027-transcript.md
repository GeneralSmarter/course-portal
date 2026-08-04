# ENMT301-26W Lecture 27 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `e24b876402642b0dd9dd24298dc4e66e048b003ee71a2f6fb37813c66de7b08c`
Generated: 2026-06-06T06:05:58.344859+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:01:30 - 00:01:40] All right, thanks everyone. We'll get started there.
[00:01:40 - 00:01:48] We have a little, a little, a little.
[00:01:48 - 00:01:57] So, just before you leave, I'll just show what we've been talking about.
[00:01:57 - 00:02:04] I've got a, a little list of things that we'll be able to go through as a group before answering general questions.
[00:02:04 - 00:02:09] Obviously, if the questions kind of come up, but one of the main things that we were highlighting last week,
[00:02:09 - 00:02:16] and just to reiterate is that your assignment hand-in will include each of these kind of things, right?
[00:02:16 - 00:02:20] My idea is that these could be a separate PDF. Some people will stitch them together.
[00:02:20 - 00:02:27] So you've got a cover sheet, a report which details with 800 words and good uses of figures and tables,
[00:02:27 - 00:02:30] what your designers, how it's going to fail, and that sort of stuff.
[00:02:30 - 00:02:37] You're going to have eight pages of hand calculations which have your clear titles, sketches, and result from your calculations.
[00:02:37 - 00:02:41] Then you'll have your drawings which should be exported from SOLIDWORKS as PDFs and just attached.
[00:02:41 - 00:02:49] So if you have information in your report relating to the drawings, you could just say you can refer to the drawing attached after the appended,
[00:02:49 - 00:02:55] after the report, right? So for any information about what your designers, this figure of final design,
[00:02:55 - 00:03:00] that might just be like a screenshot of what your final designers, so that it's really clear to someone looking at your report,
[00:03:00 - 00:03:09] what it is. But the actual manufacturing drawings will just be separate PDFs that are of good quality, so that they can be marked.
[00:03:09 - 00:03:14] So don't put those drawings into your report as figures, yeah?
[00:03:14 - 00:03:17] Cool. And then following that, you may have other appendices.
[00:03:17 - 00:03:29] These include things like your AI declaration, additional workings, such as if you use Python or Excel to kind of iterate or improve your workflows.
[00:03:29 - 00:03:39] This will also include things like your time sheet, which is just the estimate of showing how much time you spend on each of the main tasks, so that as you kind of continue as engineers,
[00:03:39 - 00:03:43] you kind of start to gauge how long certain tasks will take.
[00:03:43 - 00:03:53] We also saw that some people may have written up like a working document or a process that they used to process their testing results.
[00:03:53 - 00:04:00] That would be another thing that I'll just include after your report calculations and drawings, right? Cool.
[00:04:00 - 00:04:10] So with that, have a good afternoon. We will go to the slide and I'll sort of start with where I started last time,
[00:04:10 - 00:04:21] which was with a nice pretty picture. And then obviously in mentioning that we don't really have a formal structure, but we sort of do have a formal structure defined by what last tutorials kind of voted for.
[00:04:21 - 00:04:31] What we'll see is that those general things to cover or that we kind of covered that I sort of had thought about and that's really nice plan.
[00:04:31 - 00:04:38] To review what happens on test day and to look at another video of someone testing just there we're sort of familiar with how it kind of works.
[00:04:38 - 00:04:42] We'll review what we submit which we've just done.
[00:04:42 - 00:04:47] So are there any questions I suppose on that flow chart of what we submit?
[00:04:47 - 00:04:55] I mean this is just like another, this is exactly what it says on the assignment.
[00:04:55 - 00:05:03] It's just like putting a flow diagram rather than that and we talked about that in detail last week, right?
[00:05:03 - 00:05:14] Any questions about that? We're happy. It's kind of funny. I still get questions like, hey, yeah.
[00:05:14 - 00:05:27] Yeah, so if you have like a working document that shows how you got those but some information, then you could include that afterwards.
[00:05:27 - 00:05:32] You probably will obviously in your report need to mention what testing you do and what the main result was, right?
[00:05:32 - 00:05:37] But you might not have space in terms of words to say like lots and lots and lots of detail.
[00:05:37 - 00:05:41] So it needs to be kind of like high level concise like we did this.
[00:05:41 - 00:05:47] You know to get the material properties we did three dog bone tests to the dimension shown in figure one
[00:05:47 - 00:05:53] and the results of those dog bone tests are shown in table one following this when we were completing the details.
[00:05:53 - 00:06:03] I don't have our stress concentration for the tests were completed to work out that our K value was 1.69 and this is included at the end of this mission.
[00:06:03 - 00:06:10] Or at the end of after the report or the documentation after the report or in their pen to see after the report.
[00:06:10 - 00:06:17] Yeah, so you will probably keep things pretty concise in there because 800 words is like pretty short, right?
[00:06:17 - 00:06:22] Yeah, I still get sort of funny questions. I just have to tell myself it's funny with people like hey George.
[00:06:22 - 00:06:32] So the word count include writing on my figure, something like that or like, doesn't include our title page.
[00:06:32 - 00:06:35] It's like no, it's just the body of ticks of the report.
[00:06:35 - 00:06:41] But obviously using tables and figures is a good way to communicate information nice and clearly.
[00:06:41 - 00:06:45] Cool, so that's any other questions on like what to submit or what to clear.
[00:06:45 - 00:06:50] So obviously you need to print out your drawings and submit them into the drop box.
[00:06:50 - 00:06:53] Those would be what we use on test data kind of check.
[00:06:53 - 00:06:58] We did a drawing review, we'll do it again.
[00:06:58 - 00:07:02] Time sheet equals yes. I think we just talked about that, right?
[00:07:02 - 00:07:05] Feel like I'm groundhog down a wee bit.
[00:07:05 - 00:07:08] But I'll make that clear for the next assignment kind of what we're.
[00:07:08 - 00:07:13] Entailed it. Yeah, as I said, the whole idea is that engineers are pretty good at estimating how much time they spend on things.
[00:07:13 - 00:07:17] And then we're not going to fill in an example where we're going to talk about it.
[00:07:17 - 00:07:22] So there's that beautiful table that I've said you could attach to your physical drawings, right?
[00:07:22 - 00:07:25] So on this, it will have your names.
[00:07:25 - 00:07:29] The total mass that your predicted failure will occur at.
[00:07:29 - 00:07:32] Right, so anytime we're talking about the masses, the total mass.
[00:07:32 - 00:07:36] So it's plus the hook and the load attachment. Yeah.
[00:07:36 - 00:07:41] So if you say I think it's going to break when I put 35 kg of masses on,
[00:07:41 - 00:07:47] that in my mind is including the hook and the chain, right?
[00:07:47 - 00:07:51] So if you actually mean 36.4, probably need to say 36.4, yeah.
[00:07:51 - 00:07:58] Cool. I'll see some mostly slight nods rather than looks of concern.
[00:07:58 - 00:08:04] And then for that you'll have to say what your top three modes of failure are, right?
[00:08:04 - 00:08:07] So just stop myself getting sick of hearing my own voice.
[00:08:07 - 00:08:10] What will your first mode of failure be?
[00:08:10 - 00:08:12] Your stress concentration.
[00:08:12 - 00:08:19] And then from there, it sort of depends on your calculations and what you've designed as to what the most likely next mode of failure will be, right?
[00:08:19 - 00:08:24] So some people might have gone like really strong on trying to get a good strength to weight ratio
[00:08:24 - 00:08:28] and therefore they might have buckling likely to happen next.
[00:08:28 - 00:08:33] And so if that's the case you need to say what does the mimba and what is the direction it's buckling into, right?
[00:08:33 - 00:08:38] So buckling of my horizontal i-beam instead of aspects.
[00:08:38 - 00:08:40] And then I don't know.
[00:08:40 - 00:08:44] Number three might be earring stress of my tensile mimba.
[00:08:44 - 00:08:50] Yeah, earring stress would sort of find that it'll happen at off, but you need to say the mimba, yeah?
[00:08:50 - 00:08:53] Cool. Any questions on that?
[00:08:53 - 00:09:14] Mm-hmm. Total mess.
[00:09:14 - 00:09:15] Yeah.
[00:09:15 - 00:09:18] Strengthening weight is the total mess that it breaks on the test day.
[00:09:18 - 00:09:22] The Strengthening weight is based on your predicted failure load, right?
[00:09:22 - 00:09:24] That's it.
[00:09:24 - 00:09:39] Well, I'll clarify when answering a slightly different set of questions, but hopefully just means I can make sure that the
[00:09:39 - 00:09:42] I articulate myself clearly, right?
[00:09:42 - 00:09:48] So, strength of weight ratio, there's 10 points out of 50 for that, right?
[00:09:48 - 00:09:52] That is based on the mess of your structure without pins.
[00:09:52 - 00:09:58] So we wait on test day and your predicted failure weight.
[00:09:58 - 00:10:01] Yeah, so the one that you write on that, shape that you hand in.
[00:10:01 - 00:10:08] So on test day doesn't matter if you think about it 5 kg.
[00:10:08 - 00:10:13] Your strength of weight ratio is based on your predicted failure load.
[00:10:13 - 00:10:20] Cool. Happy?
[00:10:20 - 00:10:22] Not necessarily.
[00:10:22 - 00:10:23] Yeah?
[00:10:23 - 00:10:41] So you need to make sure that whatever you choose for your predictive failure load is accurate, because then the other points from the test day are related to it being over 20 kg, breaking before 39 kg, and then the range of your predicted failure load, right?
[00:10:41 - 00:10:50] So there's a risk associated to what you design to, but your predicted failure load should be based on your counts.
[00:10:50 - 00:10:53] We designed it to be 35 and we're going to write 40.
[00:10:53 - 00:10:55] It's like, that's not really how it works, right?
[00:10:55 - 00:10:58] So, unless you've said, you know, we've designed it.
[00:10:58 - 00:11:03] Yeah, the fact you're saying it's this and there's actually logic behind.
[00:11:03 - 00:11:07] Yeah, whatever you calculate it to break it will be what your predicted failure load is.
[00:11:07 - 00:11:08] Cool.
[00:11:08 - 00:11:12] But you can fix something that's not like technically possible.
[00:11:12 - 00:11:15] You know, you could say, I predict it's going to break it.
[00:11:15 - 00:11:20] 33.74.
[00:11:20 - 00:11:23] How'd you find it?
[00:11:23 - 00:11:28] Just as long as that's what you used in your free body diagram to do it, right?
[00:11:28 - 00:11:36] Because it might be like strategic ones where it's like, oh, if I choose that, then plus or minus 15 percent is like two days that actually exist rather than being slightly above or below.
[00:11:36 - 00:11:43] You guys, the engineers are sure you've all worked, worked it out in that kind of regard.
[00:11:43 - 00:11:44] Cool.
[00:11:44 - 00:11:47] Does that answer your question?
[00:11:47 - 00:12:03] Yeah, so the reason that the strength to weight ratio is based off the predicted failure load is like,
[00:12:03 - 00:12:09] from my experience, when I decided to do that, I think people were more likely to overshoot than undershoot.
[00:12:09 - 00:12:18] So you're sort of like, you'd be benefiting people for doing a bad job.
[00:12:18 - 00:12:23] So they're like, don't do their design calculation right and it breaks their like 50 kg.
[00:12:23 - 00:12:26] I'm like, this is if it were the massive strength to weight ratio.
[00:12:26 - 00:12:28] Right, that's not really well, but I'm in for.
[00:12:28 - 00:12:31] So that's why that's the thought process from me behind that.
[00:12:31 - 00:12:35] But that's probably like too much information.
[00:12:35 - 00:12:36] Cool.
[00:12:36 - 00:12:45] So the next thing that I was going to do is show a video about what happens on test day.
[00:12:45 - 00:12:50] So, a little weak one.
[00:12:50 - 00:12:55] So on test day, obviously you'll have your drawings there, ready for you to pick up.
[00:12:55 - 00:13:00] You'll pick them up, you'll have your time that's been kind of worked out by the timetable.
[00:13:00 - 00:13:04] So we'll post that once everyone's kind of submitted something.
[00:13:04 - 00:13:09] My name will work out what time should suit you and your partner for doing the testing.
[00:13:09 - 00:13:14] There'll be a lot of people, maybe about six or seven groups in each slot.
[00:13:14 - 00:13:18] So it's like kind of needs to run like a pretty tight operation.
[00:13:18 - 00:13:21] All the drawings will be there.
[00:13:21 - 00:13:23] You'll click your drawing, have your stuff.
[00:13:23 - 00:13:26] The technicians will weigh it without the pins like that.
[00:13:26 - 00:13:32] They'll check that you've made your structure to what you've said it should be on the drawings.
[00:13:32 - 00:13:39] Then once you've passed that, then you'll go see me telling me what your failure mass will be.
[00:13:39 - 00:13:43] And your first three modes of failure so that it's all on the spreadsheet.
[00:13:43 - 00:13:50] Then from there you'll track some safety glasses on, pin your structure together, and then you'll be doing what the spruce is doing here.
[00:13:50 - 00:13:52] So as we go, we can see that.
[00:13:52 - 00:13:57] They'll put it on so that that mess is applied and is included in that predicted failure mess.
[00:13:57 - 00:14:01] So the moment it'll be 1.39, right?
[00:14:01 - 00:14:06] Then they're putting the 5 kg on so then that would mean they're up to 6.39.
[00:14:06 - 00:14:07] So we'll go from there.
[00:14:07 - 00:14:17] Put another 5 kg.
[00:14:17 - 00:14:20] So we're at 11.4, right?
[00:14:20 - 00:14:28] Another one.
[00:14:28 - 00:14:29] 5 kg.
[00:14:29 - 00:14:34] 1, 2.
[00:14:34 - 00:14:37] So that's how about that, right?
[00:14:37 - 00:14:39] Another 5 kg.
[00:14:39 - 00:14:42] This will be 21.39.
[00:14:42 - 00:14:46] Now, got up past the 20.
[00:14:46 - 00:14:48] We've got those points locked in.
[00:14:48 - 00:14:52] Now with that, just before we keep going too far, we've got another 5 kg on.
[00:14:52 - 00:14:54] So they're at 26 at the moment.
[00:14:54 - 00:14:57] And the way that the person's putting it on is very good.
[00:14:57 - 00:15:02] You can see that very carefully putting it on, which is what is required of you.
[00:15:02 - 00:15:04] In this case here, they actually sort of cheated the end.
[00:15:04 - 00:15:06] I can't remember what happened on the test day.
[00:15:06 - 00:15:08] But watch them there, put the last one on.
[00:15:08 - 00:15:11] They sort of drop it and it makes like a very clear length length length length.
[00:15:11 - 00:15:12] Like noise.
[00:15:12 - 00:15:14] They've obviously just been lacking.
[00:15:14 - 00:15:15] All the best.
[00:15:15 - 00:15:19] And so there are like pinwalls associated with inducing failure in that way, right?
[00:15:19 - 00:15:22] So keep an eye out for that.
[00:15:22 - 00:15:26] And then obviously the two second rules are what we kind of used to work out.
[00:15:26 - 00:15:28] There's recorded as the failure mass, right?
[00:15:28 - 00:15:31] So hopefully you won't remember how we talked about that in the past.
[00:15:31 - 00:15:34] But essentially if you put a mess on straightaway,
[00:15:34 - 00:15:40] if it breaks with N2 seconds, that mess is not used in the calculation for the final mess, right?
[00:15:40 - 00:15:46] But if it holds it from more than two seconds, then it does count, right?
[00:15:46 - 00:15:50] So in this case here, say if it just ran in the growth right now, whatever's on there,
[00:15:50 - 00:15:54] because it's been more than two seconds, would be what's recorded.
[00:15:54 - 00:15:57] So it's like 26.39.
[00:15:57 - 00:15:58] Cool.
[00:15:58 - 00:15:59] Alright, we'll keep it going.
[00:15:59 - 00:16:05] What are they doing?
[00:16:05 - 00:16:06] Another five.
[00:16:06 - 00:16:11] We've got 31.39.
[00:16:11 - 00:16:15] Another five.
[00:16:15 - 00:16:16] Oh.
[00:16:16 - 00:16:19] Change and game plan.
[00:16:19 - 00:16:20] Two kg.
[00:16:25 - 00:16:28] So 33.39.
[00:16:28 - 00:16:29] Cool.
[00:16:29 - 00:16:32] They see that one there.
[00:16:32 - 00:16:39] It wasn't very subtle.
[00:16:39 - 00:16:42] I've had some weird misunderstandos as people.
[00:16:42 - 00:16:45] I'm like, how man, why did you drop it?
[00:16:45 - 00:16:47] And the light didn't drop it.
[00:16:47 - 00:16:48] It's on video.
[00:16:48 - 00:16:49] You have dropped it.
[00:16:49 - 00:16:53] So I think that it would have definitely still broke at the same spot,
[00:16:53 - 00:16:57] but make sure that you don't try and cheat, I suppose.
[00:16:57 - 00:16:59] We engineers, we act with integrity.
[00:16:59 - 00:17:01] But in that case, because it broke straightaway,
[00:17:01 - 00:17:04] and if we ignore the fact that you kind of dropped the mess on there,
[00:17:04 - 00:17:08] it would have been 33.39 that is recorded as the failure mess.
[00:17:08 - 00:17:13] And we can see broke at the stress concentration.
[00:17:13 - 00:17:14] Cool.
[00:17:14 - 00:17:32] Inclusions on any of that.
[00:17:32 - 00:17:34] Hook and load attachments.
[00:17:34 - 00:17:35] You're right.
[00:17:35 - 00:17:38] I think it's like 600 grams for the hook,
[00:17:38 - 00:17:41] but in the load attachment and the chain is also,
[00:17:46 - 00:17:51] yeah, always be 0.4 essentially.
[00:17:51 - 00:17:59] Yeah, yeah, one thing, one thing, one thing.
[00:17:59 - 00:18:03] Because there's going to be this load attachment.
[00:18:03 - 00:18:04] And this.
[00:18:04 - 00:18:09] Yeah, so it's not just that one,
[00:18:09 - 00:18:11] but go for them combined.
[00:18:11 - 00:18:27] Yeah.
[00:18:27 - 00:18:30] It will always be plus 1.39.
[00:18:30 - 00:18:33] What are those two plus together?
[00:18:33 - 00:18:34] A8.
[00:18:34 - 00:18:35] Was it 1.19?
[00:18:35 - 00:18:40] I had a typo because I had to change the hook one year of the chain or something.
[00:18:40 - 00:18:52] Because I remember someone in one of the tutorials reminded me that
[00:18:52 - 00:18:55] this slide here is wrong.
[00:18:55 - 00:18:57] Is the old version.
[00:18:57 - 00:19:00] So 1.19.
[00:19:00 - 00:19:01] Yeah.
[00:19:01 - 00:19:03] I've been saying 1.39.
[00:19:03 - 00:19:04] That is wrong.
[00:19:04 - 00:19:05] It's 1.19.
[00:19:05 - 00:19:08] I haven't messed correctly.
[00:19:08 - 00:19:09] Yeah.
[00:19:09 - 00:19:15] But this is annoying because this is my USB version of this first tutorial,
[00:19:15 - 00:19:17] which I've since updated.
[00:19:17 - 00:19:19] So I don't make the same mistake this year.
[00:19:19 - 00:19:21] I had to update the chain.
[00:19:21 - 00:19:23] So it used to be 1.09.
[00:19:23 - 00:19:24] Now it's 1.19.
[00:19:24 - 00:19:27] But the whole idea is it's slightly more than 1 kg.
[00:19:27 - 00:19:31] So you're thinking about saying about 1.39 is sort of fine.
[00:19:31 - 00:19:33] But I've probably just gotten a need.
[00:19:33 - 00:19:36] It's slightly more confusing than it needed to be.
[00:19:36 - 00:19:39] I apologize.
[00:19:39 - 00:19:42] Are we happy with that?
[00:19:42 - 00:19:43] Yeah.
[00:19:43 - 00:19:45] So all I'd think about it for you need to remember,
[00:19:45 - 00:19:48] it's just like on t-stay whatever we're putting on,
[00:19:48 - 00:19:50] actually just over 1.0.
[00:19:50 - 00:19:52] It's actually 1.2 more than that.
[00:19:52 - 00:19:55] So I put 5 kg on.
[00:19:55 - 00:19:57] It's actually 6.2.
[00:19:57 - 00:19:59] Cool.
[00:19:59 - 00:20:00] Cool.
[00:20:00 - 00:20:01] All right.
[00:20:01 - 00:20:10] So that is a tick tick tick.
[00:20:10 - 00:20:12] It's done the time sheet thing.
[00:20:12 - 00:20:13] It talks about playing the example.
[00:20:13 - 00:20:15] So the only thing is the drawing review.
[00:20:15 - 00:20:16] Right?
[00:20:16 - 00:20:17] Is everyone happy to review a drawing?
[00:20:17 - 00:20:19] I know a lot of people were having a lot of fun at electric
[00:20:19 - 00:20:21] Avenue when we were going over that.
[00:20:21 - 00:20:25] And so what we will do is if I can find the other version of
[00:20:25 - 00:20:29] this drawing that I've just done with the previous tutorial.
[00:20:29 - 00:20:30] Uh-huh.
[00:20:30 - 00:20:32] Here we go.
[00:20:32 - 00:20:34] And we can review that.
[00:20:34 - 00:20:36] But before we kind of review it,
[00:20:36 - 00:20:45] I just want to very quickly, for my own sake, show that I have
[00:20:45 - 00:20:49] actually talked about this previously and given a
[00:20:49 - 00:20:50] guide.
[00:20:50 - 00:20:52] So use those slides to guide you.
[00:20:52 - 00:20:56] So what was the tutorial for?
[00:20:56 - 00:20:57] Yeah.
[00:20:57 - 00:21:00] tutorial for because it was the fourth time that we had a tutorial,
[00:21:00 - 00:21:02] which was week 2 on Friday.
[00:21:02 - 00:21:03] Cook math.
[00:21:03 - 00:21:04] Yeah.
[00:21:04 - 00:21:08] So if you remember correctly, we first roasted this drawing,
[00:21:08 - 00:21:12] which was one that yours truly George Still or had made when I
[00:21:12 - 00:21:16] was doing a project for making an arm race for a Paralympic
[00:21:16 - 00:21:17] cyclist.
[00:21:17 - 00:21:20] And we can see that it's a very good example of a bad drawing.
[00:21:20 - 00:21:22] Because there's a lot going on.
[00:21:22 - 00:21:25] And unless you were me, you might be thinking,
[00:21:25 - 00:21:27] this makes no sense.
[00:21:27 - 00:21:28] Yeah?
[00:21:28 - 00:21:31] That's, you know, I thought about that when I was doing this project.
[00:21:31 - 00:21:33] And I was like, maybe one day I'll be a lecturer.
[00:21:33 - 00:21:36] And I can talk to thousands of students about how bad this
[00:21:36 - 00:21:38] particular drawing was.
[00:21:38 - 00:21:41] And then the middle of kind of the year that was covered.
[00:21:41 - 00:21:42] 19.
[00:21:42 - 00:21:45] We can see that we've got one part here with no labels and
[00:21:45 - 00:21:47] extra views to make it nice and cluttered.
[00:21:47 - 00:21:50] Again, we've got this random part here with no label,
[00:21:50 - 00:21:52] two views.
[00:21:52 - 00:21:55] And I mean, it's got good dimensions for what are there.
[00:21:55 - 00:21:57] But then there's also lots of missing dimensions.
[00:21:57 - 00:22:00] Then we have this one here that has some crazy stuff like a
[00:22:00 - 00:22:03] length to find as M6 a part that's shown as one part that's
[00:22:03 - 00:22:05] actually made from two pieces.
[00:22:05 - 00:22:10] And then actually some OK dimensions if you know what the
[00:22:10 - 00:22:13] design reasoning is behind it.
[00:22:13 - 00:22:14] Yeah?
[00:22:14 - 00:22:18] But from that, that led us to sort of talk about how do we make
[00:22:18 - 00:22:20] an efficient or effective drawing?
[00:22:20 - 00:22:25] And I made this nice checklist here to review before you submit
[00:22:25 - 00:22:28] your drawing to definitely make a look like you've tried.
[00:22:28 - 00:22:32] And so what we're going to do is use this to go through the
[00:22:32 - 00:22:34] drawing that we see here now.
[00:22:34 - 00:22:36] Because people can look at this online in the future.
[00:22:36 - 00:22:41] I don't know which side of the screen is like part of the screen.
[00:22:41 - 00:22:44] So they may just be looking either at the right thing, which is
[00:22:44 - 00:22:45] this the whole time.
[00:22:45 - 00:22:49] Or they might be just looking at like the PDF version of it
[00:22:49 - 00:22:50] the whole time in the flat-sattening.
[00:22:50 - 00:22:53] I'm apologizing that eventually I'll show both screens and it
[00:22:53 - 00:22:58] should be kind of back to, you know, piece of harmony and all
[00:22:58 - 00:22:59] that sort of stuff.
[00:22:59 - 00:23:04] So start with, if we as a class or suddenly you guys tell me what
[00:23:04 - 00:23:07] you think because it's more for your benefit.
[00:23:07 - 00:23:11] But if we start with the title lock, is the title block filled
[00:23:11 - 00:23:12] out appropriately.
[00:23:12 - 00:23:16] So using the list that we've got from the slide.
[00:23:16 - 00:23:19] So we can start by what is either good or bad.
[00:23:19 - 00:23:21] Anyone got any ideas?
[00:23:21 - 00:23:28] Or we can do the blunt instrument of who thinks that it's
[00:23:28 - 00:23:29] good.
[00:23:29 - 00:23:32] Okay, no one thinks it's good.
[00:23:32 - 00:23:33] I had some people think it's okay.
[00:23:33 - 00:23:35] Who thinks it's bad?
[00:23:35 - 00:23:40] All right, we can't all not vote and then be like,
[00:23:40 - 00:23:41] sick.
[00:23:41 - 00:23:44] You know, I'm like, cool, all right, onto the next one.
[00:23:44 - 00:23:47] So for those that sit it was good.
[00:23:47 - 00:23:48] What was something good about it?
[00:23:48 - 00:23:50] Is the least where we can start?
[00:23:50 - 00:23:57] You're doing the whole talking over each other thing again.
[00:23:57 - 00:24:00] It's really hard to, what was it?
[00:24:00 - 00:24:03] What's one thing that's good about it?
[00:24:03 - 00:24:05] It is filled out yet.
[00:24:05 - 00:24:08] Which puts a filled out correctly?
[00:24:08 - 00:24:10] Is the material actually persmixed?
[00:24:10 - 00:24:11] And that year it was.
[00:24:11 - 00:24:12] Took.
[00:24:12 - 00:24:15] Yeah, if it was me though, I probably write like, you know,
[00:24:15 - 00:24:18] 1.2 by 20 millimeter aluminum strip.
[00:24:18 - 00:24:22] Could even say bracket provided or as provided.
[00:24:22 - 00:24:25] Yeah, because we don't know the grade or anything.
[00:24:25 - 00:24:26] Cool, finish.
[00:24:26 - 00:24:28] Is smooth a good finish.
[00:24:28 - 00:24:32] People are sort of saying no.
[00:24:32 - 00:24:35] What would be a better thing to write there?
[00:24:35 - 00:24:44] Yeah, you could say file, sharp edges or sharp discontinuities
[00:24:44 - 00:24:50] or remove sharp discontinuities as required.
[00:24:50 - 00:24:51] Yeah?
[00:24:51 - 00:24:55] Or if you have like more information or they might be specific kind of
[00:24:55 - 00:24:58] material or different finishes on different areas.
[00:24:58 - 00:25:01] You could say refer to notes and then they might be like,
[00:25:01 - 00:25:03] for this do this or this do that.
[00:25:03 - 00:25:05] Yeah, so I don't know.
[00:25:05 - 00:25:09] Maybe if, if when you had a hole you really wanted it.
[00:25:09 - 00:25:12] So this is not really relevant to this specific drawing.
[00:25:12 - 00:25:15] But say maybe for some of your holes you wanted that to be
[00:25:15 - 00:25:16] deburred.
[00:25:16 - 00:25:19] And maybe for your edges you wanted it to be filed.
[00:25:19 - 00:25:22] You might have note that then specifies in detail that, you know,
[00:25:22 - 00:25:26] all holes should be deburred using this.
[00:25:26 - 00:25:27] And.
[00:25:27 - 00:25:30] Arices should be removed using a file.
[00:25:30 - 00:25:31] I don't know.
[00:25:31 - 00:25:33] Whatever's actually appropriate for the thing that you've got.
[00:25:33 - 00:25:36] In this case you might just say as we said, you know,
[00:25:36 - 00:25:41] remove all sharp edges or whatever you actually want.
[00:25:41 - 00:25:44] If you want it just to be rough as guts just right.
[00:25:44 - 00:25:46] None.
[00:25:46 - 00:25:48] In slash A right.
[00:25:48 - 00:25:49] Cool.
[00:25:49 - 00:25:52] So I'm just going to write as a question mark for you now.
[00:25:52 - 00:25:55] This is good for being through the angle projection,
[00:25:55 - 00:25:57] but we'll talk about whether it actually is through the angle
[00:25:57 - 00:25:59] projection shortly.
[00:25:59 - 00:26:01] Our tolerance is good.
[00:26:01 - 00:26:03] No.
[00:26:03 - 00:26:04] Okay.
[00:26:04 - 00:26:06] Well, what would be better, particularly I think this is the one
[00:26:06 - 00:26:07] that we've got leafless.
[00:26:07 - 00:26:10] What should that one be better?
[00:26:10 - 00:26:11] 0.5.
[00:26:11 - 00:26:12] Yeah.
[00:26:12 - 00:26:15] So possible minus 0.5 is sort of what we've said is approximately
[00:26:15 - 00:26:17] kind of typical for a hand-made structure.
[00:26:17 - 00:26:24] And then we might have some specific tolerances.
[00:26:24 - 00:26:25] Our suite, right?
[00:26:25 - 00:26:27] So that's actually we're getting a bit of heat about cells.
[00:26:27 - 00:26:30] We'll talk about tolerances a little bit later.
[00:26:30 - 00:26:31] Right?
[00:26:31 - 00:26:34] For now I'll just hold the phone.
[00:26:34 - 00:26:35] Leave that like that.
[00:26:35 - 00:26:36] Cool.
[00:26:36 - 00:26:39] Then if we go down here, we've got a name of our drawing part,
[00:26:39 - 00:26:40] which is good.
[00:26:40 - 00:26:44] Drawing number is a number suite.
[00:26:44 - 00:26:46] So it doesn't make any sense, right?
[00:26:46 - 00:26:49] So not a number.
[00:26:49 - 00:26:52] So I often like to, you know, even if there's only three drawings,
[00:26:52 - 00:26:56] I'll be like drawing 0, 0, 1, 0, 0, 2, and 0, 0, 3.
[00:26:56 - 00:26:59] But sort of up to you.
[00:26:59 - 00:27:00] Just make sure it makes sense.
[00:27:00 - 00:27:03] And if it says it's a number, it probably should be a number.
[00:27:03 - 00:27:06] And then project that filled it out kind of nicely.
[00:27:06 - 00:27:07] Got a date.
[00:27:07 - 00:27:10] And we can assume that this was all filled out appropriately,
[00:27:10 - 00:27:12] drawing up the scalars font.
[00:27:12 - 00:27:13] Fill.
[00:27:13 - 00:27:16] So if you're deciding that you don't want to use a UC template
[00:27:16 - 00:27:19] for your drawings, that's fine.
[00:27:19 - 00:27:21] Just make sure that the same details are included.
[00:27:21 - 00:27:26] So if you want to use like on-shape or use Fusion 360 or something,
[00:27:26 - 00:27:27] then suite-outs.
[00:27:27 - 00:27:31] Just make sure that if you have enough shoes trying to get the UC template uploaded,
[00:27:31 - 00:27:37] make sure the same information is communicated on your drawing.
[00:27:37 - 00:27:38] Cool.
[00:27:38 - 00:27:45] So then what we see here is that's actually a drawing of a part of one of the members, right?
[00:27:45 - 00:27:49] And what I've recommended when we were going through our flow diagram,
[00:27:49 - 00:27:50] what do I recommend?
[00:27:50 - 00:27:54] So I say that this is probably the clearest way to do it, or is there a simpler way?
[00:27:54 - 00:27:55] So it's not the clearest way.
[00:27:55 - 00:28:00] The simpler way would be to have one GA drawing.
[00:28:00 - 00:28:05] And then I'll just say one drawing per constructed member.
[00:28:05 - 00:28:10] Otherwise you could like have way more drawings than you need to.
[00:28:10 - 00:28:11] Yeah?
[00:28:11 - 00:28:16] So if there are drawings that are members that are manufactured using rivets or glue,
[00:28:16 - 00:28:21] then that's where you can kind of use the notes up here to kind of specify what's going on there,
[00:28:21 - 00:28:25] or add a metric manufacturing note to that, right?
[00:28:25 - 00:28:29] So some people ask, you know, if I've got 3.2 millimeter holes,
[00:28:29 - 00:28:30] do I have to show the rivet?
[00:28:30 - 00:28:32] Or can I just show the hole?
[00:28:32 - 00:28:34] And I'll say that, I think showing the rivet makes it look cool.
[00:28:34 - 00:28:37] But if you want to just leave a hole, that's fine.
[00:28:37 - 00:28:46] Just make it clear and the notes that all 3.2 millimeter holes will be pop riveted with whatever the specific type of rivet that we've got in our classes.
[00:28:46 - 00:28:47] Yeah?
[00:28:47 - 00:28:49] If you want to draw it in, you can draw it in.
[00:28:49 - 00:28:54] Probably it would still have a note showing, you know, rivets has been shown.
[00:28:54 - 00:28:58] And that 3.2 millimeter holes are required at the center of the rivet.
[00:28:58 - 00:29:06] I think that was all the questions that people would ask earlier.
[00:29:06 - 00:29:09] If you've got questions, then we can hold onto them.
[00:29:09 - 00:29:10] Cool.
[00:29:10 - 00:29:15] So next on the list, have you used capital letters? Great job.
[00:29:15 - 00:29:19] Everywhere that has capital letters got capital letters or has writing has capital letters,
[00:29:19 - 00:29:23] is the layout slash size of the drawing appropriate.
[00:29:23 - 00:29:27] So we could rephrase this. Could the drawing views be made slightly bigger?
[00:29:27 - 00:29:29] Yes, they could be made slightly bigger.
[00:29:29 - 00:29:31] So it would probably be slightly better if they did that.
[00:29:31 - 00:29:34] But we're starting to get into a trivial one in this case.
[00:29:34 - 00:29:39] But if this was all like on this size of the drawing here inside my hands,
[00:29:39 - 00:29:41] definitely would be like not good.
[00:29:41 - 00:29:43] Yeah?
[00:29:43 - 00:29:44] Cool.
[00:29:44 - 00:29:47] Next, do the selective views.
[00:29:47 - 00:29:50] Show all the key details and functionality.
[00:29:50 - 00:29:52] Do we need another view?
[00:29:52 - 00:29:54] Or is it show enough with this?
[00:29:54 - 00:29:56] So in this case, I think it's fine, right?
[00:29:56 - 00:30:00] Because we can kind of tell that it's this thick and this high.
[00:30:00 - 00:30:02] So we don't really need an extra side view.
[00:30:02 - 00:30:06] But if you've got an IB or a T-beam, you might need that side view to show
[00:30:06 - 00:30:12] whether it's a regular T-beam or I-beam or whether the flange,
[00:30:12 - 00:30:16] the web is like all centered, right?
[00:30:16 - 00:30:19] Which you wouldn't be able to tell if you just had a top in a front view.
[00:30:19 - 00:30:21] And we don't use hidden details.
[00:30:21 - 00:30:23] So, yeah.
[00:30:23 - 00:30:27] So the side view might actually be useful for some of your drawing cases.
[00:30:27 - 00:30:29] Cool.
[00:30:29 - 00:30:30] Happy.
[00:30:30 - 00:30:33] And then there's the drawing uncluttered and easy to read.
[00:30:33 - 00:30:36] Could it be made clearer?
[00:30:36 - 00:30:38] Could there be any dimensions reduced?
[00:30:38 - 00:30:44] So do we like these dimensionings like this?
[00:30:44 - 00:30:46] What's that called?
[00:30:46 - 00:30:47] Change dimensionings.
[00:30:47 - 00:30:48] Someone heard it.
[00:30:48 - 00:30:50] I heard the murmur cut through.
[00:30:50 - 00:30:51] Nice.
[00:30:51 - 00:30:52] Very good.
[00:30:52 - 00:30:56] Typically, I think people like Tony and Workshop technicians,
[00:30:56 - 00:30:57] they prefer this, right?
[00:30:57 - 00:31:03] They like the job to be a little bit harder than it needs to be just so that they keep their minds sharp, right?
[00:31:03 - 00:31:07] I like George instead of telling me that it just needs to be 300 millimeters.
[00:31:07 - 00:31:13] I prefer that you make me go 60 plus 60 plus 50 plus 50 plus 20 plus 20 plus 20.
[00:31:13 - 00:31:16] Or am I being facetious?
[00:31:16 - 00:31:18] I'm sort of taking the purse, right?
[00:31:18 - 00:31:20] They don't like that at all.
[00:31:20 - 00:31:21] Don't say that.
[00:31:21 - 00:31:22] I George said you like that.
[00:31:22 - 00:31:26] I mean, it could be funny, but probably not worth it.
[00:31:26 - 00:31:31] Yeah, but ideally, if this is the hold of whole dimension and that's an important one for your assignment,
[00:31:31 - 00:31:36] that should really be included specifically, right?
[00:31:36 - 00:31:40] Now, what would the dimensions possibly be for this?
[00:31:40 - 00:31:42] What should I write in here?
[00:31:42 - 00:31:44] Doesn't actually matter what the value is.
[00:31:44 - 00:31:45] Some amount of 100.
[00:31:45 - 00:31:47] Now, what would our tolerance be?
[00:31:47 - 00:31:54] Plus 1 is 0.1 plus or minus.
[00:31:54 - 00:31:58] What do you guys reckon for a hold of whole dimension for this assignment?
[00:31:58 - 00:32:12] I haven't really good at this game.
[00:32:12 - 00:32:18] I haven't really got a 0.5.
[00:32:18 - 00:32:25] Anyone, I mean, it would be appropriate and it would be acceptable, but,
[00:32:25 - 00:32:27] imagine if I had it at this 0.5.
[00:32:27 - 00:32:33] What happens on the test day if I actually make it to be plus 1?
[00:32:33 - 00:32:37] So, when I did it to mention, maybe I need to read out the drill slips a little bit.
[00:32:37 - 00:32:41] And I've drilled it and it's the only thing that's wrong with my drawing, but I make it plus 1.
[00:32:41 - 00:32:46] I didn't have to in theory throw that in the bin and make the whole thing again, right?
[00:32:46 - 00:32:54] But, for example, if it was your horizontal member, what is the allowable tolerance for that horizontal pen to pen to mention on the,
[00:32:54 - 00:32:56] on the marksheet?
[00:32:56 - 00:33:00] Plus or minus 3?
[00:33:00 - 00:33:04] So, because it's allowed to be plus or minus 3 on Tuesday, that's probably what I've put on my drawing.
[00:33:04 - 00:33:09] But, if you had plus or minus 0.5 and I appreciate that answer, it's still technically not wrong, right?
[00:33:09 - 00:33:16] It's just like, you could end up making something that is fit for purpose in terms of the assignment.
[00:33:16 - 00:33:23] Like, you wouldn't lose any marks because it was plus or minus 0.3, but you've not made it to your own drawing spec, which is like the, you know, tiny will be like,
[00:33:23 - 00:33:27] this is not an quality assurance, you know?
[00:33:27 - 00:33:29] I'll find out how sirens go north.
[00:33:29 - 00:33:30] Yeah?
[00:33:30 - 00:33:31] Cool.
[00:33:31 - 00:33:36] So, with that though, if we did put that dimension there, what do we have to do to one of these?
[00:33:36 - 00:33:42] Bracket, one of them is an easy solution or delete one of them, right?
[00:33:42 - 00:33:46] So, you're only measuring from one datum and then it's kind of going.
[00:33:46 - 00:33:47] Now, what if these repeated dimensions?
[00:33:47 - 00:33:52] What is something that we could put after the dimension to save us having to dimension at every time?
[00:33:52 - 00:33:58] Yeah, so it goes right, T-Y-P, which stands for typical, and then we can just delete that one there.
[00:33:58 - 00:34:04] So, that typical just means any similar dimension is assumed to be the same dimension, yeah?
[00:34:04 - 00:34:09] And then with this, typically speaking of something symmetric, which in this case it is,
[00:34:09 - 00:34:19] it can be assumed, although in this case I probably would include the T-Y-P, but symmetry can mean that dimensions are assumed to be the same on the other side, right?
[00:34:19 - 00:34:29] But again, all I'm saying is that we could probably remove these ones and then just have T-Y-P,
[00:34:29 - 00:34:37] and then that means it's less cluttered, even though it's not really that cluttered right now, but it's still less cluttered, yeah?
[00:34:37 - 00:34:40] Cool. Next question, do we like this?
[00:34:40 - 00:34:45] Because I know people are being a little bit reluctant to answer for some reason.
[00:34:45 - 00:34:49] We're going to do a vote with our hands, hopefully if you'll comfortable with that.
[00:34:49 - 00:34:54] So, if you think that this is a good way to dimension the diameter of that hole,
[00:34:54 - 00:35:00] you hand up for yes, one person, two people, cool.
[00:35:00 - 00:35:02] Who reckons? No.
[00:35:02 - 00:35:04] S to be everyone else.
[00:35:04 - 00:35:05] And there you are, right?
[00:35:05 - 00:35:09] So, for the big no say is what don't you like about it?
[00:35:09 - 00:35:10] Because the thing is you could both be right.
[00:35:10 - 00:35:12] I just want to hear both sides of the story.
[00:35:12 - 00:35:14] But what don't you like about this?
[00:35:14 - 00:35:28] You make holes with drills and drill bits of specific sizes, yeah?
[00:35:28 - 00:35:32] But you might, your whole might, why?
[00:35:32 - 00:35:35] I guess another question could be why might you want it to be?
[00:35:35 - 00:35:37] So, what is this telling us?
[00:35:37 - 00:35:40] It needs to be between 8 and 8.1.
[00:35:40 - 00:35:43] So, what is the intent of that?
[00:35:43 - 00:35:50] Yes, so that the pin that's 8-mill should definitely be able to fit through, right?
[00:35:50 - 00:35:56] So, try to enforce clearance fit rather than dimensioning it such that it's an interference fit,
[00:35:56 - 00:35:58] which is like one of those kind of theory things.
[00:35:58 - 00:36:02] So, one of those imaginary things that doesn't necessarily exist, right?
[00:36:02 - 00:36:07] Like, when you actually make the hole in the shaft, like, it's either going to be clearance,
[00:36:07 - 00:36:10] or it's going to be interference, right?
[00:36:10 - 00:36:12] It's not like, oh, that was a transition fit.
[00:36:12 - 00:36:15] It's like in between a interfering and not interfering.
[00:36:15 - 00:36:18] So, let's try to make sure that when you're on test day,
[00:36:18 - 00:36:22] you're not trying to like put the pins through your members
[00:36:22 - 00:36:25] and then it's like not fitting and then panic is being induced.
[00:36:25 - 00:36:27] And I'm sort of saying, oh, can you please hurry up?
[00:36:27 - 00:36:30] We've got to get going and then you're like, you know?
[00:36:30 - 00:36:33] So, it's like, so I guess the other question is like,
[00:36:33 - 00:36:37] for the people that said that, no, is there a preferred way that you would
[00:36:37 - 00:36:38] dimension the same thing?
[00:36:38 - 00:36:43] Or is there something that you don't like about it that's not being articulated yet?
[00:36:43 - 00:36:55] Would you just say clearance fit?
[00:36:55 - 00:36:58] So, we typically have to follow the drawing standard.
[00:36:58 - 00:37:00] So, this is one way to enforce the clearance fit.
[00:37:00 - 00:37:05] The other way though, could be if you said diameter 8.0 plus 0.1 minus 1.
[00:37:05 - 00:37:09] 0.1 minus 0.0.
[00:37:09 - 00:37:10] That would be another way.
[00:37:10 - 00:37:12] Sometimes people would like that method.
[00:37:12 - 00:37:16] If it was like a shaft and a hole, then you would have like a,
[00:37:16 - 00:37:19] you could use the letters, right?
[00:37:19 - 00:37:20] Without ISO symbols.
[00:37:20 - 00:37:22] So, it could be like a H7, whatever.
[00:37:22 - 00:37:25] And that actually has a predefined tolerance based on the size of the hole.
[00:37:25 - 00:37:28] But then again, sometimes the technicians are like,
[00:37:28 - 00:37:29] don't make me look it up in the book.
[00:37:29 - 00:37:30] Just tell me what it is, right?
[00:37:30 - 00:37:32] So, either of them are fine.
[00:37:32 - 00:37:35] Personal sort of preference.
[00:37:35 - 00:37:37] You might even make it be a bigger tolerance, right?
[00:37:37 - 00:37:41] If you really don't care that it's, yeah, because I don't know what the tolerance
[00:37:41 - 00:37:42] sort of depends.
[00:37:42 - 00:37:44] Probably neither clean them up a little bit.
[00:37:44 - 00:37:46] They might have a little bit of rust on them, you know?
[00:37:46 - 00:37:48] They'd be doing a lot of service.
[00:37:48 - 00:37:49] Okay.
[00:37:49 - 00:37:51] Now, there's things real blur.
[00:37:51 - 00:37:57] But, anything else that we need to talk about?
[00:37:57 - 00:38:05] Yeah, so that's the sort of thing that we could have T-wappy.
[00:38:05 - 00:38:06] Yeah?
[00:38:06 - 00:38:07] There'll be one way.
[00:38:07 - 00:38:10] Or you could say two times there's another option.
[00:38:10 - 00:38:14] Or, technically, like, because there's not any other holes here,
[00:38:14 - 00:38:19] it's probably like, would be okay to assume that the other side is the same.
[00:38:19 - 00:38:23] If you're at T-wappy or like two times, then, like,
[00:38:23 - 00:38:25] you know that you've definitely made it clear.
[00:38:25 - 00:38:27] You don't get the technician going like,
[00:38:27 - 00:38:28] oh, what size is this hole when you're drawing?
[00:38:28 - 00:38:29] It's not specified.
[00:38:29 - 00:38:30] Yeah?
[00:38:30 - 00:38:36] So, similarly, like, if you had lots of people like to chuck heaps of,
[00:38:36 - 00:38:38] well, not lots of people.
[00:38:38 - 00:38:43] Some people like to chuck lots of weight relieving holes or weight reducing holes.
[00:38:43 - 00:38:46] That's a classic one where you need to think carefully about what the dimensions are.
[00:38:46 - 00:38:51] And whether you actually care about whether it's the plus or minus 0.5 or something different,
[00:38:51 - 00:38:57] or whether it's just six holes on this member, roughly this space, plus or
[00:38:57 - 00:39:01] minus 1, can you just dimension from this to this T-wappy?
[00:39:01 - 00:39:04] And then you don't have the dimension on the other side, right?
[00:39:04 - 00:39:07] Lots of right ways to do it, but just don't over-define.
[00:39:07 - 00:39:08] Cool.
[00:39:08 - 00:39:10] Quickly, we need to keep going.
[00:39:10 - 00:39:12] What else is missing on these drawing views?
[00:39:12 - 00:39:14] So, a third angle orthographic.
[00:39:14 - 00:39:17] The question is, which view is the front view?
[00:39:17 - 00:39:19] It's not labeled, right?
[00:39:19 - 00:39:21] Which label are we used?
[00:39:21 - 00:39:23] So, which one would be the front view?
[00:39:23 - 00:39:24] Is this one the front view?
[00:39:24 - 00:39:28] Yeah, that's confusing though, right?
[00:39:28 - 00:39:29] So, this one is the front view.
[00:39:29 - 00:39:30] I'd agree with you.
[00:39:30 - 00:39:31] Why?
[00:39:31 - 00:39:32] Yeah.
[00:39:32 - 00:39:39] So, on our last-metra view, this is always our front side, right?
[00:39:39 - 00:39:41] So, if you're looking from that side, that's what you would see.
[00:39:41 - 00:39:43] So, they match.
[00:39:43 - 00:39:44] And then what does that mean?
[00:39:44 - 00:39:46] This one is top.
[00:39:46 - 00:39:47] But they'll put it below, right?
[00:39:47 - 00:39:49] So, it really should be moved up here.
[00:39:49 - 00:39:52] Because we're saying that it's third angle orthographic.
[00:39:52 - 00:39:55] So, we need to follow what the standard convention is.
[00:39:55 - 00:39:56] Cool.
[00:39:56 - 00:39:57] Cool.
[00:39:57 - 00:40:01] Cool.
[00:40:01 - 00:40:03] So, we've got some specific clearances.
[00:40:03 - 00:40:05] We've got some general challenges.
[00:40:05 - 00:40:08] We've said that that could be updated.
[00:40:08 - 00:40:10] And if you remember, we talked about in class.
[00:40:10 - 00:40:15] I sort of showed some ICO 2, 7, 6, 8.
[00:40:15 - 00:40:17] Follow its dimensions.
[00:40:17 - 00:40:21] And you can get these kind of tables online that sort of show that if you don't have an idea of
[00:40:21 - 00:40:25] what an appropriate time it says for the type of tolerance class you've got, i.e.
[00:40:25 - 00:40:29] Maybe your thing is a coarse tolerance, except for all your stress concentration is.
[00:40:29 - 00:40:35] You could actually have a table like this, like the first three or four or five or a few of these,
[00:40:35 - 00:40:39] to show that, oh, for links of this to this, this is what I want the tolerance to be.
[00:40:39 - 00:40:42] Well, the links of this to this is what I want the tolerance to be.
[00:40:42 - 00:40:47] If you're not happy with just having one general tolerance of plus or minus 0.5,
[00:40:47 - 00:40:52] just highlighting that as an option and some groans that you'll see will have these kind of things, right?
[00:40:52 - 00:40:58] But often it's more the case where you have lots of dimensions that are of different magnitudes, right?
[00:40:58 - 00:41:06] So plus or minus 0.5 is like a tiny dimension tolerance for say something that's like plus or minus,
[00:41:06 - 00:41:09] well, it's up to, like say, 1000 millimeters, you know?
[00:41:09 - 00:41:14] If you're told a builder, like, you know, make my house to the nearest half millimeter,
[00:41:14 - 00:41:17] they would have some not kind of things to say, you know?
[00:41:17 - 00:41:22] Because for that kind of link, that's a tiny percentage difference in the link.
[00:41:22 - 00:41:27] But plus or minus 0.5 or something that's 1 millimeter, that's 50%.
[00:41:27 - 00:41:30] Right? So it's like a really big tolerance here.
[00:41:30 - 00:41:37] So you'll see that, for example, 0.2 here is this, and then there, and then there,
[00:41:37 - 00:41:38] and then it doesn't even exist.
[00:41:38 - 00:41:43] It's too tight for a very coarse defined tolerance class.
[00:41:43 - 00:41:45] Cool.
[00:41:45 - 00:41:46] All right.
[00:41:46 - 00:41:52] One more thing that I can remember, we'll think of before we finish this here.
[00:41:52 - 00:42:03] So we said size could be slightly bigger, size could be slight,
[00:42:03 - 00:42:04] bigger.
[00:42:04 - 00:42:08] And then there's also, in SOLIDWORKS, there's not like some silly revisions table here.
[00:42:08 - 00:42:14] They've done a really good job in deleting it, but if you really have issues with deleting it, fill it out.
[00:42:14 - 00:42:21] But if I see like x, x, j, 13, it's like soul destroying, you know?
[00:42:21 - 00:42:24] It just makes it look like it haven't really tried.
[00:42:24 - 00:42:25] Cool.
[00:42:25 - 00:42:31] So I think inadvertently we've actually talked through some of these next things here.
[00:42:31 - 00:42:35] So we've talked about the fact that you might actually have specific end general tolerances,
[00:42:35 - 00:42:38] the things like your holes, you might have a bigger distance between your holes,
[00:42:38 - 00:42:39] you might have a bigger one.
[00:42:39 - 00:42:44] For things like stress concentration, you might have a smaller one, like plus or minus 0.1.
[00:42:44 - 00:42:49] And then we've done the other things of talking about how the dimensions could be improved
[00:42:49 - 00:42:52] to follow the drawing standard.
[00:42:52 - 00:42:58] So question time for you guys, any other general questions before I walk around?
[00:42:58 - 00:43:09] So I've got a bunch of members around that we can obviously look at if you want some inspiration,
[00:43:09 - 00:43:14] any other questions generally.
[00:43:14 - 00:43:24] Yeah, that will be measured.
[00:43:24 - 00:43:29] For question was like a question I could simplify to say, are you going to measure our structure on the day?
[00:43:29 - 00:43:30] Yes.
[00:43:30 - 00:43:31] Yeah.
[00:43:31 - 00:43:37] And for things like your stress concentration, I'll definitely have to check that to make sure it is what you see that was
[00:43:37 - 00:43:41] because you can imagine that a small change in a stress concentration, depending on the geometry of your member,
[00:43:41 - 00:43:46] could have quite a big effect on the percentage of nominal area that is there, right?
[00:43:46 - 00:43:49] So yes, make it to your drawing.
[00:43:49 - 00:44:01] And the penalties are so said, are not meeting there is only a sum of brief here.
[00:44:01 - 00:44:05] So for stress concentrations, the tolerance is plus or minus 0.1, right?
[00:44:05 - 00:44:07] I think I've got this on the assignment brief here.
[00:44:07 - 00:44:14] So just again, my own sake, apparently, the student comments got to me last year and people were like,
[00:44:14 - 00:44:15] stuff wasn't clear.
[00:44:15 - 00:44:21] And it was like three people were like 300 that filled out the survey and they were the only ones that were putting you coffee.
[00:44:21 - 00:44:32] But we can see here, but outside of time, it's on the stress concentration, up to 20 marks, 10 marks of an infinite or close,
[00:44:32 - 00:44:34] which is my discretion.
[00:44:34 - 00:44:41] But basically, what we want to do is make it really clear like what you lock in is what you need to make.
[00:44:41 - 00:44:46] So make sure I'm happy with what you submit and you need to make with that.
[00:44:46 - 00:44:51] Obviously, if you realize something or you spot an area before the Tuesday, let me know about it.
[00:44:51 - 00:44:56] Don't just be like, no, I'm not sure which one, find it.
[00:44:56 - 00:44:57] It'll be fine.
[00:44:57 - 00:44:58] Yeah?
[00:44:58 - 00:45:10] So the value of all penalties, a professional approach in four warning rule will just be on this.
[00:45:10 - 00:45:20] So if you did it, if you let me know, then we'll make it sort of worth your while for sort of being out of make that change.
[00:45:20 - 00:45:28] Otherwise, there would be no point in telling you to tell me, oh, we see that hole was going to be diamond a 20 and we realize that's too big.
[00:45:28 - 00:45:32] Because our strips are only 20 mils. We need to change it in our zone. Okay.
[00:45:32 - 00:45:40] That will follow that process here. Cool. Other general questions.
[00:45:40 - 00:45:46] Obviously, there'll probably a lot of like it.
[00:45:46 - 00:45:50] I know specific things that you guys want checked.
[00:45:50 - 00:45:52] At 10 to 12, I'll just go outside.
[00:45:52 - 00:45:58] And then we can answer more questions there. But I'll ask for now, I'll float around.
[00:45:58 - 00:46:01] I'll leave this on for the next five minutes, but I'll be floating around so I can go.
[00:46:01 - 00:46:05] Questions for me then just check your hand up and I'll wander around.
[00:46:05 - 00:46:07] I'll find out a little bit that way.
[00:47:46 - 00:47:54] I'll just do those.
[00:49:24 - 00:49:26] I'll do them.
[00:49:27 - 00:49:29] I'll do them.
[00:49:29 - 00:49:31] I'll do them.
[00:49:31 - 00:49:33] I'll do them.
[00:49:33 - 00:49:34] I'll do them.
[00:49:34 - 00:49:35] I'll take them.
[00:49:35 - 00:49:37] I'll do them.
[00:49:37 - 00:49:39] I'll put them.
[00:49:39 - 00:49:42] You could make the lights up there.
[00:50:42 - 00:50:53] I know lots of people have got questions.
[00:50:53 - 00:50:59] I'm just aware that there will be a class coming in probably from now.
[00:50:59 - 00:51:04] So I'll just loiter outside and answer your questions there.
[00:51:04 - 00:51:52] You can answer your questions.
[00:51:52 - 00:52:00] It's more likely to be close to 1.1 to 2.0.
[00:52:00 - 00:52:07] Should you 1.1 go to the top and then I would whatever something you have to decide
[00:52:07 - 00:52:12] actually that there's something that's justified to do.
[00:52:12 - 00:52:15] But the way that I use those black out there,
[00:52:15 - 00:52:18] there's something here, it's Christmas and Christmas,
[00:52:18 - 00:52:23] and it's like maybe this person that you can put black by something into it.
[00:52:23 - 00:52:27] So, therefore we have designed the concept of the assumption
[00:52:27 - 00:52:30] that we have our users equally.
[00:52:30 - 00:52:33] Thank you.
[00:52:33 - 00:52:35] When we add more answers to the brothers,
[00:52:35 - 00:52:38] we're going to sort of as long as we can.
[00:52:38 - 00:52:40] You should still mention the books.
[00:52:40 - 00:52:43] You should leave that table to think of the book.
[00:52:43 - 00:52:47] But we're at all these paths.
[00:52:47 - 00:52:52] I don't know if you can do anything else.
[00:52:52 - 00:52:53] I'm going to feel like this.
[00:52:53 - 00:52:57] But I am looking forward to this video.
[00:52:57 - 00:52:58] If I feel good, I'm ready to give up.
[00:52:58 - 00:53:01] I'm ready to put the word easy or something.
[00:53:01 - 00:53:05] I think that you have to take it all the time.
[00:53:05 - 00:53:09] But then you want to keep this upside up to use.
[00:53:09 - 00:53:12] If I want some good luck, I'm ready to use it.
[00:53:12 - 00:53:13] Except that we're trying to help them, like,
[00:53:13 - 00:53:14] it's like yo...
[00:53:14 - 00:53:17] I'm ready to put my face over.
[00:53:17 - 00:53:18] I'm ready to put it in the corner.

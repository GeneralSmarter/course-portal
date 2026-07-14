# ENMT301-26W Lecture 15 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_15_audio_16k_mono_32k.mp3`
Source audio SHA-256: `3b6af4c486e84e2b7a8f9eaf0722e38c8b490c1ddea6664d7b187359e9ebf9b0`
Generated: 2026-06-06T05:31:22.572987+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:00 - 00:00:04] Well you could have something like that when there's a clearance and you have to just make sure it's a seat out before you start flying alone.
[00:00:04 - 00:00:08] But once it's there it's not just going to like, just go to town if you don't know.
[00:00:08 - 00:00:12] I was like, what was the way of life?
[00:00:12 - 00:00:13] You know what I mean?
[00:00:13 - 00:00:19] At least it's on an angle where it actually pulls it when you put the weight on, then it should be pulled.
[00:00:19 - 00:00:27] As long as that hole, long as that hole there is like, in line and not like, also do you have to rub it so it won't go there.
[00:00:27 - 00:00:31] But if you don't want the hole in there, then it's there to just like, single.
[00:00:31 - 00:00:32] It's only the front shape.
[00:00:32 - 00:00:34] You don't need a rubber to do that.
[00:00:34 - 00:00:38] So either if you've got more than one, 20 minutes, you need to use one of each.
[00:00:38 - 00:00:41] It needs always going to be one of the other.
[00:00:41 - 00:00:42] Yeah?
[00:00:42 - 00:00:43] The combination of one.
[00:00:43 - 00:00:45] So that's good for your half.
[00:00:45 - 00:00:46] So that's good for you.
[00:00:46 - 00:00:47] Cool.
[00:00:47 - 00:00:48] All right sweet.
[00:00:48 - 00:00:49] All right, thanks everyone.
[00:00:49 - 00:00:50] We'll get started there.
[00:00:50 - 00:00:52] It's lovely to see everyone again.
[00:00:52 - 00:00:57] Hope you had a enjoyable morning.
[00:00:57 - 00:00:59] I've been flat out.
[00:00:59 - 00:01:00] She says it's crazy this year.
[00:01:00 - 00:01:03] Yeah, just so much things happening.
[00:01:03 - 00:01:08] So based on what happened in the last tutorial,
[00:01:08 - 00:01:16] we're probably going to spend about half an hour talking through tutorial related stuff that I've pre-prepared and answering questions that you have.
[00:01:16 - 00:01:24] And then it's probably going to be what they voted for, which I guess means to what they voted for for you as well.
[00:01:24 - 00:01:28] So that's that independent work on your project time for the like remainder of the time.
[00:01:28 - 00:01:53] And I'll float around and answer questions that you have as you go through your thing just because I suspect that a lot of people are not really at the stage where they have a question that is appropriate to ask in front of the whole class because you haven't had time to kind of mull over and think what those kind of questions might be because I've just been given you a lot of content and not much time to actually kind of think about what you're doing and working on it.
[00:01:53 - 00:02:01] So what we'll do is head out notices.
[00:02:01 - 00:02:05] So I've got some aluminium strips here.
[00:02:05 - 00:02:07] I'm getting less, which is good.
[00:02:07 - 00:02:12] So if you've come to click them today then at some point come and click them for yourself.
[00:02:12 - 00:02:15] Please don't sign for your partner.
[00:02:15 - 00:02:19] Just grab them for yourself and your partner can grab them later.
[00:02:19 - 00:02:22] And then following that I will kind of put them up.
[00:02:22 - 00:02:23] What is going on?
[00:02:23 - 00:02:27] I'll put them up on the fifth floor of the civil neck admin.
[00:02:27 - 00:02:32] Reception and those that'll be the place that you can ask for and get them signed off.
[00:02:32 - 00:02:37] I know that there's some people that obviously haven't been able to make it to the tutorials to kind of click them there.
[00:02:37 - 00:02:41] Maybe I'll try on you to bring that some to the drop in session next week.
[00:02:41 - 00:02:47] But we're getting pretty close. I think that most people should have their stuff sort of sort of.
[00:02:47 - 00:02:59] If you later on with the track say when you come to manufacturer, if something went wrong and you need like another 400mm or something of a strip, then just make sure that you email me about that kind of request.
[00:02:59 - 00:03:03] So you don't have an unlimited supply.
[00:03:03 - 00:03:06] Cool. So similar to what I was intuitively saying at the start.
[00:03:06 - 00:03:12] At this point I'm hoping that you're at least confident and have an understanding of the task at hand and what you're doing.
[00:03:12 - 00:03:18] I realize that you guys too need a bit of time to think and work on your project to be able to come up with questions.
[00:03:18 - 00:03:20] And that's kind of the goal of this tutorial.
[00:03:20 - 00:03:25] So there might be some group questions that we are able to answer and then I'll be able to float around after it.
[00:03:25 - 00:03:31] But obviously your engagement is kind of key to make sure that everything goes on track.
[00:03:31 - 00:03:36] So this is what we've got. So we'll do our booting questions. I'll go through what test results I've got.
[00:03:36 - 00:03:41] There's only been about 10 to 15 kind of people that have actually put up what they got.
[00:03:41 - 00:03:43] So we'll update that again next week.
[00:03:43 - 00:03:48] Do a couple little design discussions which you guys will be able to just tell me the answer that you already know.
[00:03:48 - 00:03:56] So that I have confidence that you guys know what's happening otherwise it seems to be done a kind of panic mode I guess.
[00:03:56 - 00:04:11] So with that what burning questions do you have?
[00:04:11 - 00:04:25] Is your structure allowed to fail due to buckling where there's a hole in it.
[00:04:25 - 00:04:30] I mean yeah would I recommend that as your first value mode?
[00:04:30 - 00:04:39] Probably not. Just because in terms of that buckling equation is nothing that screen's confidence of when the bucking actually appear about it.
[00:04:39 - 00:04:46] So often similar to normal machine design we don't we design it have a factor of safety such that it won't fail right.
[00:04:46 - 00:04:52] You kind of weird if you suppose in certain orientations you might be able to go oh yeah,
[00:04:52 - 00:04:56] shoom it's going to be pin-pined but that's still an approximate.
[00:04:56 - 00:05:01] It's not like a definitive it would definitely buckle up this time right.
[00:05:01 - 00:05:08] So but you could say for example I guess where I was interpreting your question is you might have a hole or a notch on your tensile member.
[00:05:08 - 00:05:17] That's value mode number one and then you know that the second most likely place that it might fail might be at a reduced section in your
[00:05:17 - 00:05:20] compression member where you think it might be susceptible to buckling.
[00:05:20 - 00:05:22] So you'd put that as your second motor failure.
[00:05:22 - 00:05:52] Cool. Sweet. Other questions.
[00:05:52 - 00:06:00] So the question which is good question was the notes.
[00:06:00 - 00:06:07] A vague about the exact value of the parent stress concentration factor.
[00:06:07 - 00:06:13] So that's what I would also in your notes I would if you've got your calculation I would use that terminology.
[00:06:13 - 00:06:20] I've assumed that the apparent stress concentration factor for my hole is approximately 1.1 yeah.
[00:06:20 - 00:06:27] And the question was how do we know that it is going to be that and what is influencing that value.
[00:06:27 - 00:06:31] is one way to rephrase it hopefully. Yeah happy with that.
[00:06:31 - 00:06:42] So on one side of things in terms of all our stress concentration factor sort of theory we see that it is a geometry or a geometric kind of problem right.
[00:06:42 - 00:06:45] We don't have stress concentration plots for specific materials.
[00:06:45 - 00:06:49] We just say that if this is the geometry this is the K value right.
[00:06:49 - 00:06:59] And then what we've said is that for ductile materials those values that have for K become very conservative.
[00:06:59 - 00:07:04] Because that apparent stress concentration factor is a lot lower for those materials right.
[00:07:04 - 00:07:12] Which is great if we don't want our things to fail. So for example in our shafts if we're doing calculations there we find to say the stress concentration factor is 2.
[00:07:12 - 00:07:16] And if it actually had a stress concentration factor there was lower that's all good.
[00:07:16 - 00:07:24] We're on the right side of that kind of equation right. Kind of bad if it is opposite sort of thing and we're being less conservative than we need to.
[00:07:24 - 00:07:39] So the question I'm going to ask another question to sort of continue this train of thought which is okay if we are assuming an apparent stress concentration factor are we allowed to do like small scale tests to verify our assumption or
[00:07:39 - 00:07:48] to validate that what we've assumed is our K value or our parent stress concentration factor are we allowed to test that and verify it right.
[00:07:48 - 00:07:58] And the answer is yes you are allowed to do a small scale test that kind of validates or updates what you've done based on your calculation right.
[00:07:58 - 00:08:07] The idea that you use another kind of small test piece and obviously make sure that you've got enough for the rest of your manufacturer of your part yeah.
[00:08:07 - 00:08:29] So one way that you might go about this stress concentration and failure member is that the assumption that we sort of talked about this morning was if I design the stress in my tensile member to be approximately the stress UTS of my from my test results.
[00:08:29 - 00:08:47] And when I add more weight will happen it will break yeah that's the idea right because stress concentrations are not indicative of failure that's not the way that they are typically used yeah.
[00:08:47 - 00:09:03] So to make sure that you're confident that whatever K value you've decided which is most likely going to be around 1.1 but it might be I don't know 1.02 it might be 1.11 it depends on the geometry and the sharpness of that stress concentration.
[00:09:03 - 00:09:13] And that you've got right so you might want to make an assumption and then test that what K value you've used is appropriate right.
[00:09:13 - 00:09:19] So using that same formula of your next stress being K times your nominal stress.
[00:09:19 - 00:09:32] If it fails at a student force you can approximate that to be your ultimate tensile stress and then you could back calculate to work out what was the K value for that specific case.
[00:09:32 - 00:09:41] Which might make hopefully that makes sense intuitively some people will think of the 18th into it and it will be a good problem to kind of overcome.
[00:09:41 - 00:09:43] There's more than one way to do it as well.
[00:09:43 - 00:09:57] So other people in the past you know you might have tested a couple couple whole sizes to actually work out what the K value was and do it that way kind of almost making your own plot for object because only a finite material I think.
[00:09:57 - 00:10:05] This way of making an approximation and then validating it or checking it is more probably both time and resource effective.
[00:10:05 - 00:10:11] It's more than one way that you can do that aspect of the assignment.
[00:10:11 - 00:10:15] Cool great great questions other questions.
[00:10:15 - 00:10:34] I think we've had my 10 second waiting times that's good.
[00:10:34 - 00:10:41] Probably means you genuinely don't have questions rather than you didn't have time to think about a question and ask it.
[00:10:41 - 00:10:47] So another question that we did have which I thought was particularly good as on the test day.
[00:10:47 - 00:10:50] You're able to use two kg weights.
[00:10:50 - 00:11:01] Sorry two kg masses and five kg masses right up to you what ones you use when and what order they go on and you can also take weights off right.
[00:11:01 - 00:11:08] So you could go like put on a two take off the two put on a five and what would be recorded as they have gone.
[00:11:08 - 00:11:11] So two kg have five kg.
[00:11:11 - 00:11:14] So there is ways that you can kind of slowly go up.
[00:11:14 - 00:11:18] You could go to two to take off two to and then go five.
[00:11:18 - 00:11:21] So you could go to one.
[00:11:21 - 00:11:22] You know, essentially.
[00:11:22 - 00:11:30] Cool so your own control of that obviously there's also a finite amount of two kg and five kg but that's not normally a lot of factor.
[00:11:30 - 00:11:36] If you just mean like two kg two kg two kg and you're kind of DJ Caled in on the day you'll lose.
[00:11:36 - 00:11:40] You'll run out of eventually there won't be another one you know.
[00:11:40 - 00:11:46] So from that point then you'll have to take some awful start using five kg ones right.
[00:11:46 - 00:11:47] Cool.
[00:11:47 - 00:11:51] Finally we all had the confidence of DJ Caled.
[00:11:51 - 00:11:59] So with that we thought I might be useful just to show slash talk through another example.
[00:11:59 - 00:12:07] Test day orientate or test day video to show kind of what's happened and you'll sort of see that sort of strategy possibly coming.
[00:12:07 - 00:12:20] We're not coming because what we need to remember is that the total mass is the mass of your masses plus the mass of the hook chain and load attachment which is about 1.19.
[00:12:20 - 00:12:23] And someone corrected from there.
[00:12:23 - 00:12:26] So we'll go from here they're all set up they're ready to go.
[00:12:26 - 00:12:33] We'll also can look at this one towards the end of all review how it actually gets put into the testing apparatus right.
[00:12:33 - 00:12:37] So I've got nothing on that moment.
[00:12:37 - 00:12:41] Now put on a five kg so we're at five kg.
[00:12:41 - 00:12:42] Cool.
[00:12:42 - 00:12:44] What are they going to go for next?
[00:12:44 - 00:12:50] Another five kg nice.
[00:12:50 - 00:12:53] So currently once this gets put on.
[00:12:53 - 00:13:00] So if we had like a live read out currently there at 11.19 I think.
[00:13:00 - 00:13:01] Yeah.
[00:13:01 - 00:13:03] Another five kg.
[00:13:03 - 00:13:05] 16.19.
[00:13:05 - 00:13:09] Now they've done a two kg.
[00:13:09 - 00:13:12] So 18.19.
[00:13:12 - 00:13:13] Cool.
[00:13:13 - 00:13:24] And so the amount of mass that is rotated broke written down is following what we call the two second rule.
[00:13:24 - 00:13:27] So if it holds the next for two seconds then it counts.
[00:13:27 - 00:13:31] If you put it on and it breaks for four two seconds doesn't count right.
[00:13:31 - 00:13:34] So you put on instantly it breaks it was whatever the previous mass was.
[00:13:34 - 00:13:38] Put it on one second breaks still the previous one.
[00:13:38 - 00:13:43] So sometimes we have to like do the TMO thing and I like look at the video and like check that.
[00:13:43 - 00:13:45] Yeah it was or was not two seconds.
[00:13:45 - 00:13:46] Yeah.
[00:13:46 - 00:13:47] Cool.
[00:13:47 - 00:13:51] So I think that they were at 18.19 right.
[00:13:51 - 00:13:53] Tell me if I'm wrong.
[00:13:53 - 00:13:57] And they're about to put on another two kg.
[00:13:57 - 00:13:59] Yeah.
[00:13:59 - 00:14:01] So two seconds they're happy.
[00:14:01 - 00:14:03] About 20.19.
[00:14:03 - 00:14:06] Happy days of that kind of threshold.
[00:14:06 - 00:14:08] Now they're going to another five.
[00:14:08 - 00:14:10] So 25.19.
[00:14:10 - 00:14:14] What are they going to go for?
[00:14:14 - 00:14:17] So I have no idea what their failure mass was another five.
[00:14:17 - 00:14:22] So they're going for 30.19.
[00:14:22 - 00:14:24] Cool.
[00:14:24 - 00:14:28] Next script getting started you see we run a real smooth operation.
[00:14:28 - 00:14:30] They're really deliberating.
[00:14:30 - 00:14:33] I wonder if this is maybe what their failure target mass was.
[00:14:33 - 00:14:34] I don't know.
[00:14:34 - 00:14:36] So maybe they're thinking do we do it too?
[00:14:36 - 00:14:37] Do we do it five?
[00:14:37 - 00:14:39] They're done a two.
[00:14:39 - 00:14:43] So that's 32.19 now right.
[00:14:43 - 00:14:48] So obviously this is kind of probably something I would recommend.
[00:14:48 - 00:14:50] I would almost have a game plan so that you're not like,
[00:14:50 - 00:14:52] should we do a two or a five.
[00:14:52 - 00:14:55] I reckon this I'd kind of work out what order you want to put on.
[00:14:55 - 00:14:58] And then you know you're feeling confident what you want and what you want to fail.
[00:14:58 - 00:15:03] Because sometimes when it gets a bit here at the end there's a bit of a
[00:15:03 - 00:15:07] risk risk reward I suppose in terms of do I put a five kg in a break straight away
[00:15:07 - 00:15:10] or do I put a two kg in risk at holding it for two seconds,
[00:15:10 - 00:15:15] especially when we have that part of the mark sheet that's with your within 15 or 25%
[00:15:15 - 00:15:24] of your projected load right.
[00:15:24 - 00:15:28] Yeah there's somewhere between like I think there's at least four.
[00:15:28 - 00:15:33] But with that you could for example go two two take off two twos,
[00:15:33 - 00:15:35] put a five and then keep doing it.
[00:15:35 - 00:15:40] So you still can sort of, yeah I don't have an official number of the number of twos.
[00:15:40 - 00:15:45] But yeah if we need a wait for like if you started testing while the other one was testing,
[00:15:45 - 00:15:48] we could just like hold five.
[00:15:48 - 00:15:53] So sometimes there's people that like put four twos on and then they might
[00:15:53 - 00:15:56] wait a little bit for the oh and a fail because they have all the two kgs.
[00:15:56 - 00:15:57] Yeah.
[00:15:57 - 00:16:00] But I'll answer your question just after we watched this so.
[00:16:00 - 00:16:04] Well yeah I think we're at 32 let's just say that and they're putting on a two.
[00:16:04 - 00:16:08] So this is 34.19 yeah.
[00:16:08 - 00:16:11] So 34.19 what are they going for?
[00:16:11 - 00:16:14] So this is a bold move you know.
[00:16:14 - 00:16:16] No it could be the move.
[00:16:16 - 00:16:22] But I'm putting a five kg on which means like if it doesn't fail straight away,
[00:16:22 - 00:16:25] they're over shooting 39 right.
[00:16:25 - 00:16:28] But it means that maybe they're within there 25% you know.
[00:16:28 - 00:16:34] So we see could be could be the move hopefully a break straight away.
[00:16:34 - 00:16:38] We see just like clockwork that pulled it off right.
[00:16:38 - 00:16:39] So I know.
[00:16:39 - 00:16:42] They're seeing relatively happy they will have lives.
[00:16:42 - 00:16:43] So.
[00:16:43 - 00:16:44] It's true.
[00:16:44 - 00:16:45] It went sort of well yeah.
[00:16:45 - 00:16:48] Cool just before we answer that other question.
[00:16:48 - 00:16:54] If we look here what we'll see is typically when people put their structure into the
[00:16:54 - 00:16:58] the test rig what we want you to do with have it all pungent together when you're
[00:16:58 - 00:17:01] when you're seeing that you're at see the technicians.
[00:17:01 - 00:17:05] They'll talk to you about your drawings and they'll weigh it and you'll go see me at that point
[00:17:05 - 00:17:08] you'll pin it all together put your safety glasses on.
[00:17:08 - 00:17:11] Make sure that I've got the right loads and modes for your failure.
[00:17:11 - 00:17:15] And then once there's a free station you'll go and load it up with the pins
[00:17:15 - 00:17:16] in there ready.
[00:17:16 - 00:17:22] And then typically what you'll do is put the bottom corner in first and then you'll
[00:17:22 - 00:17:27] attach this horizontal vertical support.
[00:17:27 - 00:17:30] Sorry here and then you'll add the load attachment.
[00:17:30 - 00:17:34] So we should sort of see that here but I think lock you sort of standing in the way for most of it.
[00:17:34 - 00:17:39] You can see here they're putting in into the slot the bottom pin first.
[00:17:39 - 00:17:43] Then the other team in that's going to put this roller support in place.
[00:17:43 - 00:17:46] Yeah so they've got that pin in place.
[00:17:46 - 00:17:53] And then from there they're just making sure they're happy with how centered it is before adding that kind of load attachment.
[00:17:53 - 00:18:00] And then they'll add the hook and we ideally want the hook to only really be like about a
[00:18:00 - 00:18:10] a centimeter off our kind of foam pad so that there's not like a massive falling weight splaying out every where you're sweet.
[00:18:10 - 00:18:18] So, oh last time I didn't see that's unfortunate people watching online hopefully you can see me now.
[00:18:18 - 00:18:22] Last time we were fully on that that's all good.
[00:18:22 - 00:18:25] So we had a cushion over this side.
[00:18:25 - 00:18:38] Yeah so if it breaks while you're kind of taking away or forming a new bring it
[00:18:38 - 00:18:43] in the next minimum weight that it has howls will be what's recorded.
[00:18:43 - 00:18:52] Yeah so say you put 25 kg on then as you were taking off the 5 kg a broke it will be 25 kg.
[00:18:52 - 00:18:55] Yeah so still that two second rule will be what applies.
[00:18:55 - 00:18:57] Cool.
[00:18:57 - 00:19:04] Any other questions?
[00:19:04 - 00:19:05] Yeah.
[00:19:05 - 00:19:12] So I guess it's a good last thing.
[00:19:12 - 00:19:15] Yeah so if you put it so sometimes it does get down to the last.
[00:19:15 - 00:19:20] So if you're at 25 kg and you edit it 5 and how to for exactly with just over 2 seconds
[00:19:20 - 00:19:24] 30 would be what's recorded rather than a break straight away at 25.
[00:19:24 - 00:19:25] Yeah.
[00:19:25 - 00:19:33] That's good to clarify because otherwise the wording could easily be less interpreted because you say well if I had when you put this mess on but
[00:19:33 - 00:19:37] two second rule was sort of what we want to have hopefully memorable when there.
[00:19:37 - 00:19:38] Yep.
[00:19:38 - 00:19:52] So the question was relating to strategy is there a best strategy when it comes to putting messes on.
[00:19:52 - 00:19:55] You guys are the bosses there.
[00:19:55 - 00:20:00] Yeah answer is that it sort of depends and as we saw there.
[00:20:00 - 00:20:06] Depends on what the move is and what you're trying to get out of you know so this sort of three things going on.
[00:20:06 - 00:20:11] One you want to be between 20 and 39.
[00:20:11 - 00:20:19] And the other thing is you want to be either within 15 to see know what your predicted failure mess was or within 25.
[00:20:19 - 00:20:25] So there might be times where if you put a two on maybe you'll still be within your 25 but not your 15.
[00:20:25 - 00:20:30] And then you might put a five on after that to hope that it definitely breaks and then you get those points like that.
[00:20:30 - 00:20:40] But there's not one right answer in terms of the approach here just doing five year.
[00:20:40 - 00:20:45] Or you could for example say your failure mess was 25 right.
[00:20:45 - 00:20:54] You could get to 20 and go 20 22 24 take two twos off 25.
[00:20:54 - 00:21:00] And if you wanted to really you could take off the five input two two two twenty six you know.
[00:21:00 - 00:21:04] And you could take off one and then go you know me.
[00:21:04 - 00:21:10] Takes ages and maybe on the day I'll be kind of like oh man I wish I'd be hurry up but like you guys are the boss.
[00:21:10 - 00:21:13] And you could do it at the speed that you want to only me.
[00:21:13 - 00:21:15] Only the TA tell you what to do.
[00:21:15 - 00:21:26] If you've got a strategy you can go and execute the strategy yeah zero twenty zero twenty maybe not that but you know.
[00:21:26 - 00:21:35] You can take off one five and you can put on to and take off twos but you start taking off two five's we might be going like hang on.
[00:21:35 - 00:21:36] Cool.
[00:21:36 - 00:21:37] Yep.
[00:21:37 - 00:21:44] So your stated failure mess is the total combined everything yeah.
[00:21:47 - 00:21:48] Cool.
[00:21:48 - 00:21:57] And it will be assumed there unless you've written 24 plus 1.13 or what 9.3 or whatever it is 1.19 I think yeah.
[00:21:57 - 00:21:59] Yeah total mess use your total mess.
[00:21:59 - 00:22:03] You do calculation total and now yeah.
[00:22:03 - 00:22:04] Cool.
[00:22:04 - 00:22:06] All right.
[00:22:06 - 00:22:08] This is going good.
[00:22:08 - 00:22:11] I missed anything else nothing else mainly the things.
[00:22:11 - 00:22:12] Cool.
[00:22:12 - 00:22:19] So let's go through these quickly so as I said there's not he sort of data point so this is really just to say.
[00:22:19 - 00:22:26] Oh yeah what I have is sort of similar to other people have had or it's not very similar I probably should do more testing.
[00:22:26 - 00:22:37] We do want to see in the markers what we're looking for like you describing how you got your your material property results so if you just say I'm just going to use these various here then you kind of lose.
[00:22:37 - 00:22:43] The marks were showing how you did your testing material testing and the right up of the assignment right.
[00:22:43 - 00:22:51] So Z here the most common values seems to be 4 to 5 this which is I know 120 to 144 yield.
[00:22:51 - 00:22:56] For UTS we see it's more likely 5 to 6 this.
[00:22:56 - 00:23:06] So slightly higher some overlap possibly and again as I'd say I take these sort of with a semi grain of salt A because there's a low sample size and B because sometimes
[00:23:06 - 00:23:17] sometimes people might have put the wrong thing in other places you know but we see that looks like UTS is more likely between 140 to 160 plus minus 10ish.
[00:23:17 - 00:23:20] Yeah.
[00:23:20 - 00:23:23] Cool.
[00:23:23 - 00:23:37] With this so this is just reminding me with this this is an average value right typically unless you really like just picked one test and going like oh it is doing one and we're going to go with it.
[00:23:37 - 00:23:41] You bought our more than one test to get your data point that you're putting here right.
[00:23:41 - 00:23:50] That means that there is also like a range of results either in terms of your maximum or like your average kind of standard deviation you might have right.
[00:23:50 - 00:23:58] So holding that and then I'm sort of doing that classic thing where your parents like what's the answer.
[00:23:58 - 00:24:05] We're going to look at this March sheet and we see that we're getting marks for our predicted failure loads.
[00:24:05 - 00:24:18] Hopefully it's kind of clear in the fact that oh we know that our first motor failure will happen at this load second at this load third at this load and then we see this predicted failure range.
[00:24:18 - 00:24:28] So my question to you is how you meant to come up with what your predicted failure range is for your primary failure mode.
[00:24:28 - 00:24:38] So we see I would expect that this is determined based on the range of values in your data from your material testing.
[00:24:38 - 00:24:51] So it could be you use your linen your next value from your ultimate tensile test testing or it might be I would use some other kind of statistical metric of like our within one or two standard deviations that was this.
[00:24:51 - 00:24:55] So it depends on how many you've done but I'd probably just use your next and then right.
[00:24:55 - 00:25:01] So means you're going to have to kind of like back calculate to work out what the force would be for that range right.
[00:25:01 - 00:25:07] Sort of for deeper. That's how you go about it right.
[00:25:07 - 00:25:17] Cool. Keep moving. We see a young's modulus is between basically two to three-ish.
[00:25:17 - 00:25:23] Most commonly three. So 60 plus minus five. Some people for 70 plus minus five.
[00:25:23 - 00:25:36] And again what this is really trying to do is make you know that okay if I had option I don't know below 35 and I know something might be wrong or if I had 120 I know something might be wrong.
[00:25:36 - 00:25:42] And we sort of discussed on how you might approach if you need to update what value you use.
[00:25:42 - 00:25:58] So any questions relating to any of this material testing stuff. It's weak.
[00:25:58 - 00:26:06] Cool. So this is meant to be quick fire before we kind of open the force for me to roam around and you guys to kind of make progress on whatever you're working on.
[00:26:06 - 00:26:15] But can you tell me what has happened in the design that's caused failure? What kind of failure has occurred at these ends?
[00:26:15 - 00:26:28] Buckling. Yeah. And so what could we do to avoid that failure? Yeah. So we could move the flange closer to the hole which would reduce the length.
[00:26:28 - 00:26:35] Yeah. What else could we do? All we could reinforce it as primarily the sort of two options.
[00:26:35 - 00:26:43] So this is saying that if you're watching this is sort of tricky. People if they watch the first two toys I wouldn't have seen me like, oh look at this thing here.
[00:26:43 - 00:26:49] We sort of did have it on the document camera. But we see these sort of those two options once it goes into focus.
[00:26:49 - 00:26:57] Oh, of what we see here. So we could extend the flange and then sometimes we might have to cut out a little bit so we don't have interference between our two members.
[00:26:57 - 00:27:03] All we might kind of double up the thickness here. All we might do a combination of the two right.
[00:27:03 - 00:27:12] The main idea is that if we have a teen song member, this isn't a teen song member, but it needs to, whatever other members need to sort of be out of fit in here.
[00:27:12 - 00:27:22] It's still be in line with that hole, right? So if they didn't have this cut out here, I suspect that they wouldn't have been out actually construct their structure here.
[00:27:22 - 00:27:33] Cool. It'll work. All right. What do we need to be careful about if you have a T section, compression member or an I beam with the protruding
[00:27:33 - 00:27:49] or extended fluid, or an I beam with a long extended flange. Same thing, right? Those are all kind of possible issues for buckling.
[00:27:49 - 00:28:00] Make sure your design can fit. We manufactured in a similar to the testing apparatus. What effect would a clearance fit have on compressor failure?
[00:28:00 - 00:28:11] So I'm primarily meaning for these kind of things here. So if we're looking here, what are our in conditions in this plane? Pen, pen.
[00:28:11 - 00:28:24] That one must be what we get right, right? This plane, if we had a really tight fit on our pins and our holes, what could the theoretical, what would the theoretical in conditions be?
[00:28:24 - 00:28:33] Fixed flex, right? But as we've learned, fixed flex is pretty much impossible. Yeah? And so if we had a clearance fit, i.e.
[00:28:33 - 00:28:44] the pins are a little bit wobbly in there. What is a more appropriate in condition to assume? Pen, pen, right? Some people might still want to use their recommended value, which I think is maybe 1.2.
[00:28:44 - 00:28:56] So if those me, I'll just keep it simple and use pen pen and then I know, definitely not going to hopefully buckle. But the main thing is that you need to make sure that you do those I value calculations for both planes.
[00:28:56 - 00:29:09] Now, have any people done or once that question next? Many people have done any buckling calculations here. Cool, yeah. And what did you have to do to be able to do your buckling calculation?
[00:29:09 - 00:29:20] You had to make an assumption of what your cross-section is, right? So if you don't know what your cross-section is, you can't work out the I value and then you can't do the buckling calculation.
[00:29:20 - 00:29:29] And so if you don't know where to start, just start with the thickest option that you had, which might be a 20 by 20 by 20 I mean, right?
[00:29:29 - 00:29:36] Then you can always update your design from there, where you could say, okay, if it was a T-beam, I haven't been the section, this is what it will be.
[00:29:36 - 00:29:41] You obviously have to make some sort of assumption to work out the cross-section to work out the I value, yeah?
[00:29:41 - 00:29:47] And you have to start somewhere so you just have to draw a line to the sand. Questions?
[00:29:47 - 00:29:55] Yep.
[00:29:55 - 00:30:08] Are these ones? Cool, so that's good questions. The question is for these holes where we have reduced weight-reducing holes, does that affect our buckling calculation?
[00:30:08 - 00:30:24] The answer is, well, yes, but we can kind of check that with a failure is going to occur by if we assumed that that was a square would it buckle and that reduced if that was our length, you know?
[00:30:24 - 00:30:46] I can draw it on a bit of paper maybe. So if our hole was looking for a member like this, and we have a hole like this, what you could do is assume that there is actually a square,
[00:30:46 - 00:30:53] i.e. that your cross-section is just looking like this, right?
[00:30:53 - 00:30:57] And that your length would just be that length, yeah?
[00:30:57 - 00:31:05] There would be one back of the envelope way to be able to check, and you probably find that as long as that's not super long,
[00:31:05 - 00:31:11] probably shouldn't buckle, but good thing to check and you can do the same kind of assumption for those in ones, right?
[00:31:11 - 00:31:28] I think we've already drawn. Yeah? Cool. So it's good questions and I think it sort of leads on to what is the trade-off of adding weight-reducing holes in your design?
[00:31:28 - 00:31:36] So structure is the more risk or less risk. There's more risk, right?
[00:31:36 - 00:31:46] So if you add holes, then that's going to change some of the cross-sections and possibly in just your concentrations into a design, depending on what kind of members they are, right?
[00:31:46 - 00:32:02] So, substitute to decide whether or not you want to add different kind of geometric features to your design, which ones are risk-y or worse, less risky, and that's where it's up to you to kind of make some decisions about where you lay, right?
[00:32:02 - 00:32:09] Remember when I was doing this way back in the day? Two of my friends were like, yeah, we don't like design particularly very much.
[00:32:09 - 00:32:15] So we're just going to make it the simplest design possible. We don't care about strength to be able to do it right all.
[00:32:15 - 00:32:24] They spent a lot less time than I would have actually doing the design of their design and the manufacturer of their design, and it worked on the day and they were happy.
[00:32:24 - 00:32:28] Everyone was happy. It was all joyful, you know? Some people would do the same thing.
[00:32:28 - 00:32:36] I've got a cool view that I've been there with this. Sure, it's heavy, but I'm happy to try and get 41 out of 50 on the test day.
[00:32:36 - 00:32:43] So it's your guys calling in terms of how much time and effort you want to spend on that.
[00:32:43 - 00:32:56] And I guess that sort of relates if we show the document camera and that flow diagram that we had, that kind of relates to some of the stuff here, right?
[00:32:56 - 00:33:07] So you could just go through this in a pretty linear fashion. Some people might want to kind of actually look at, oh, two minutes, this is three member and do a little bit more detailed analysis.
[00:33:07 - 00:33:09] Both of mine, right?
[00:33:09 - 00:33:19] But some people might, you know, do a buckling cow and then update their cross-section and then redo that calculation so that they get a lower weight of their total design.
[00:33:19 - 00:33:30] So as we sit there, don't forget to consider the impact of these kind of features on your design.
[00:33:30 - 00:33:38] The other thing that I wanted to show, so here we see, I've got a bunch of members around.
[00:33:38 - 00:33:45] You can kind of look at them shortly, but here we see an example of a member that's buckled.
[00:33:45 - 00:33:56] So I'm not sure if it was that they got their stress concentration wrong or whether they just like head and ear it and their assumptions of maybe they didn't do the calculation for both planes, I don't know.
[00:33:56 - 00:34:06] But here's an example of a buckling. Here's another example of a team member buckling and this is more just to show you like it's pretty clear when it buckles that it has buckled.
[00:34:06 - 00:34:16] And then this one here is sort of an interesting one showing it up hoping that the camera can see, but I can also almost get it in the document camera.
[00:34:16 - 00:34:20] But here what we see is that it's sort of similar.
[00:34:20 - 00:34:31] It's tried to do a similar thing to this design here where we have one or two pieces of aluminium that have been folded and glued together to make an IBM, right?
[00:34:31 - 00:34:37] I think that these students who made this one thought it was going to be really easy and straightforward.
[00:34:37 - 00:34:43] It turned out to be very fiddly to get the bend, I think it was quite a small kind of bend here that they needed to do.
[00:34:43 - 00:34:53] And so what they did was ended up changing their design so that they could actually try and manufacture something because they couldn't get the bending kind of happening.
[00:34:53 - 00:34:59] So what ended up happening is there are something that would act as a kind of complete cross-section.
[00:34:59 - 00:35:06] Well, it wasn't really valid and we had some buckling of basically the C channel in the middle.
[00:35:06 - 00:35:17] And I guess what is just a clear warning or a clear indicator that whatever you say that your designers make sure you're confident that you can manufacture it.
[00:35:17 - 00:35:31] And so if that means doing a sort of test bin or test small test piece, I would recommend doing that because the last thing that you want is my design and now I'm not sure if I can actually make it by hand.
[00:35:31 - 00:35:39] Cool. So with that are there any open class questions before I start wandering around?
[00:35:39 - 00:35:49] So other comment that I had that I did make was, in terms of your calculations, there's eight pages.
[00:35:49 - 00:35:53] There needs to be hand calculations and it's just a hand calculations of your final designer.
[00:35:53 - 00:36:02] So if you do these iterations of your I-bin cross-section, we don't want to know the whole story of this engineering member.
[00:36:02 - 00:36:06] We just want to know the final design calculation here.
[00:36:06 - 00:36:09] So I'm reading through it and say, okay, cool, this is your final design. Okay, cool.
[00:36:09 - 00:36:11] This is the result of the calculation here.
[00:36:11 - 00:36:18] We don't need to have the full history of like first we did this free body diagram and then we did this free body diagram.
[00:36:18 - 00:36:21] And then we decided that actually we might do this.
[00:36:21 - 00:36:28] So just keep it matter of fact, we don't have heaps of pages and those can be hand written on paper.
[00:36:28 - 00:36:30] Obviously A4 is our standard size.
[00:36:30 - 00:36:34] All they could be done on the tablet, a game, A4 is just standard size.
[00:36:34 - 00:36:47] That's fine, but we don't want any like typed out the equations on word or typed out the equations on any other software and we don't want your calculations just to be some Python or Excel,
[00:36:47 - 00:36:49] or Excel document, right?
[00:36:49 - 00:36:58] You might have those things and you can incorporate them as additional kind of fits alongside your submission, like an dependency.
[00:36:58 - 00:37:08] But for your actual hand calculations that you submit they need to be hand-written, clear title sketch working common time result.
[00:37:08 - 00:37:14] So next week I'll go through what is required for the assignment submissions.
[00:37:14 - 00:37:17] But I think that that's pretty much everything that I covered.
[00:37:17 - 00:37:28] The only other thing was someone here has said that the rivets that we have are these ones here, 6.7 mill rivets,
[00:37:28 - 00:37:32] which is good for connecting two sheets but possibly not three.
[00:37:32 - 00:37:39] And so we're going to get Tony to order hopefully some of these ones here that can do three sheets of aluminium.
[00:37:39 - 00:37:49] Yeah, but we can see there that this is their share value that they've kind of indicated for those, but that's just a little kind of small bit of information.
[00:37:49 - 00:37:56] So any other bits, questions, I'll eyes off-flight around. Feel free to work on your assignment.
[00:37:56 - 00:37:59] For I'll put your hand up and I'll float around if you have any specific questions.
[00:37:59 - 00:38:03] If you need to click aluminium, please only click it for yourself.
[00:38:03 - 00:38:05] We've got that sheet there.
[00:38:05 - 00:38:11] If you want to look at some of these fairly menders, non-failing menders, common-heavy look,
[00:38:11 - 00:38:29] otherwise that's pretty much us done.
[00:39:19 - 00:39:21] Thank you.
[00:39:49 - 00:39:51] Thank you.
[00:40:19 - 00:40:21] Thank you.
[00:40:49 - 00:40:51] Thank you.
[00:41:19 - 00:41:21] Thank you.
[00:41:49 - 00:41:51] Thank you.
[00:42:19 - 00:42:21] Thank you.
[00:42:49 - 00:42:51] Thank you.
[00:43:19 - 00:43:21] Thank you.
[00:43:49 - 00:43:51] Thank you.
[00:44:19 - 00:44:21] Thank you.
[00:44:49 - 00:44:51] Thank you.
[00:45:19 - 00:45:21] Thank you so much.
[00:45:21 - 00:45:23] Thank you so good.
[00:45:23 - 00:45:25] Thank you.
[00:45:27 - 00:45:31] Thank you.
[00:45:31 - 00:45:33] And, thank you.
[00:45:33 - 00:45:37] Thank you.
[00:45:37 - 00:45:39] Thank you.
[00:47:39 - 00:47:41] And we could sue the other round.
[00:47:41 - 00:47:43] We had our pieces.
[00:47:43 - 00:47:45] We had our pieces.
[00:47:45 - 00:47:47] We had our pieces.
[00:47:47 - 00:47:49] We had our pieces.
[00:47:49 - 00:47:51] We've ever been through all the steps.
[00:47:51 - 00:47:53] We just got one.
[00:47:53 - 00:47:55] No, I think you can try for us.
[00:47:55 - 00:47:57] We can't do anything else.
[00:47:57 - 00:47:59] I'm not going to let people talk to us.
[00:47:59 - 00:48:01] I really want to say that I'm fine.
[00:48:01 - 00:48:02] I'm fine.
[00:48:02 - 00:48:03] I'm fine.
[00:48:03 - 00:48:04] I'm fine.
[00:48:04 - 00:48:05] I'm fine.
[00:48:05 - 00:48:07] It's the end of the day.
[00:48:10 - 00:48:11] Hello?
[00:48:14 - 00:48:19] Did you just think I feel?
[00:48:19 - 00:48:20] I think I'm fine.
[00:48:21 - 00:48:24] Do I go and match up and travel in all of this day, the whole time?
[00:48:24 - 00:48:27] I'm going to go and do it again.
[00:48:27 - 00:48:29] None of that would have happened.
[00:48:29 - 00:48:32] I'm not going to get something to hang it out on my couch.
[00:48:32 - 00:48:39] I don't know what it is that you're looking at the house, but I'm not looking at the house
[00:48:39 - 00:48:41] but I'm not looking at the house.
[00:48:41 - 00:48:44] And that's precisely what I'm looking at.
[00:48:44 - 00:48:49] Maybe I'll have one that will make the house all the way down.
[00:48:49 - 00:48:53] So, really you're looking at the house.
[00:48:54 - 00:48:59] So, here's a little template to be bought.
[00:48:59 - 00:49:01] So, I'm still on.
[00:49:01 - 00:49:03] I'm buying a pound of pounds.
[00:49:03 - 00:49:05] And we have a lot of coffee.
[00:49:05 - 00:49:08] And we have early classes.
[00:49:08 - 00:49:11] Because I'm going to get a pot when you come on.
[00:49:11 - 00:49:13] Can you see?
[00:49:13 - 00:49:14] Yeah.
[00:49:14 - 00:49:15] Can you see?
[00:49:15 - 00:49:16] Can you see?
[00:49:16 - 00:49:17] Can you see?
[00:49:17 - 00:49:19] It's really hard to get in there.
[00:49:19 - 00:49:20] I think you're out.
[00:49:20 - 00:49:21] I don't know.
[00:49:21 - 00:49:23] I'm not looking at the house.
[00:49:23 - 00:49:32] I'm looking at the house.
[00:49:32 - 00:49:35] I'm not looking at the house.
[00:49:35 - 00:49:41] I'm looking at the house.

# ENMT301-26W Lecture 14 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_14_audio_16k_mono_32k.mp3`
Source audio SHA-256: `f28419233fa1eb485d9fbb0204a7386350b864e85245a1f12fa225f50f4c35f2`
Generated: 2026-06-06T05:28:20.939960+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:08 - 00:00:13] Alright, thanks everyone for making a start there.
[00:00:13 - 00:00:30] We'll just finish up our conversations every useful.
[00:00:30 - 00:00:33] Awesome, well welcome to another Lectoral.
[00:00:33 - 00:00:35] It's great to have you all here.
[00:00:35 - 00:00:39] And you'll see that I guess going forward other than week 8,
[00:00:39 - 00:00:42] which will be a little bit different.
[00:00:42 - 00:00:48] We'll probably have this kind of Tuesday format being our typical kind of contact for the week
[00:00:48 - 00:00:51] where we don't have any more of those Friday workshops.
[00:00:51 - 00:00:58] But the whole reason that we had those is that that meant that we could cover the content that we would otherwise have to have covered over the next two weeks.
[00:00:58 - 00:01:01] So, yeah.
[00:01:01 - 00:01:03] Cool, so notices.
[00:01:03 - 00:01:05] If you need aluminium strips.
[00:01:05 - 00:01:10] Following two days tutorial I'll kind of leave some with the Nick admin team and have the sign-up sheet
[00:01:10 - 00:01:14] so that if you haven't collected your strips already, that's where you get them from.
[00:01:14 - 00:01:20] Obviously, like down the track, for some reason you need more than your two per person allocation.
[00:01:20 - 00:01:24] You'll need to make sure that you send me an email and kind of go about it that way.
[00:01:24 - 00:01:26] Because we do only have a limited supply.
[00:01:26 - 00:01:32] And the idea is that force strips per team should definitely be enough.
[00:01:32 - 00:01:36] See, please make sure you sign in name off.
[00:01:36 - 00:01:42] Just quickly, I think a few people have emailed me about trying to find partners.
[00:01:42 - 00:01:49] But I do wonder if there's anyone or if there's multiple people in the room who don't have a partner.
[00:01:49 - 00:01:55] Is there anyone that doesn't have a partner at the moment?
[00:01:55 - 00:01:57] Sweet, well.
[00:01:57 - 00:01:58] Great.
[00:01:58 - 00:02:07] But if you drive to the partner, I can try and link you up because I know that the forum sort of has been working.
[00:02:07 - 00:02:14] But just make sure that once you have had success in using that take your post down so that people don't have to follow false leads if you know what I mean.
[00:02:14 - 00:02:16] Cool.
[00:02:16 - 00:02:20] So, this point I'll open you a compliment with the task at hand.
[00:02:20 - 00:02:26] And I realise that you guys need a bit of processing time and thinking time to actually come up with questions,
[00:02:26 - 00:02:30] which is kind of my goal for the tutorials.
[00:02:30 - 00:02:34] That your questions hopefully going forward will kind of guide what we discuss.
[00:02:34 - 00:02:40] As I said, we've kind of covered a lot of the base kind of core concepts for each of the elements of the assignment that are required.
[00:02:40 - 00:02:45] I'm more than happy to re or go over or explain more detail, any kind of aspect.
[00:02:45 - 00:02:48] But it's better coming from you guys.
[00:02:48 - 00:02:53] I've already sort of tried to lay the foundation and lay some kind of questions that I would ask.
[00:02:53 - 00:02:55] But basically don't be shy.
[00:02:55 - 00:03:00] And I'm just saying I understand if you don't have any questions because you haven't had a chance.
[00:03:00 - 00:03:03] But this engagement and interaction will be key.
[00:03:03 - 00:03:10] So, the RoadNet 4.3.4.5 is always keeps me.
[00:03:10 - 00:03:12] And stuff and stuff.
[00:03:12 - 00:03:13] Cool.
[00:03:13 - 00:03:14] Anybody any questions you have?
[00:03:14 - 00:03:18] We'll review some of our kind of preliminary participants results.
[00:03:18 - 00:03:21] Things aren't any roughly like 10 to 15 entries in that.
[00:03:21 - 00:03:24] So, as I said, we have to sort of take without a grain of grain of salt.
[00:03:24 - 00:03:31] But at least it'll give you some answer to the question of is what I have reasonable.
[00:03:31 - 00:03:35] And then we can go through some design discussions.
[00:03:35 - 00:03:38] And depending on what we exactly have time for.
[00:03:38 - 00:03:42] And then could go through an example of if we want to.
[00:03:42 - 00:03:45] So, at this point, the floor is yours.
[00:03:45 - 00:03:47] Questions do you have?
[00:03:47 - 00:04:13] Cool.
[00:04:13 - 00:04:29] So, I'm summarised the question is on Tuesday, when we're testing, are we as students in control of what weights are added to our
[00:04:29 - 00:04:31] family members?
[00:04:31 - 00:04:32] Cool.
[00:04:32 - 00:04:34] So, the answer is there's great question.
[00:04:34 - 00:04:37] And it probably actually highlights something that I can discuss at the moment.
[00:04:37 - 00:04:42] So, the answer is you guys are the boss, you're in control.
[00:04:42 - 00:04:44] Do I have the videos here?
[00:04:44 - 00:04:45] Cool.
[00:04:45 - 00:04:48] So, you get to decide whether you put two KGs or five KGs on.
[00:04:48 - 00:04:51] Obviously, there's a finite number of two KG ones.
[00:04:51 - 00:04:54] So, if you just make two, two, two, two, two, two, two, two, two, two, two, two, two,
[00:04:54 - 00:04:56] eventually you'll run out of two, right?
[00:04:56 - 00:05:02] But, there's nothing stopping you from going like, I put on two, I take off two, I put on five.
[00:05:02 - 00:05:05] If you wanted to go like a step of three KG, right?
[00:05:05 - 00:05:12] The weight that is held for two seconds is the, that's how we say that it held the weight, right?
[00:05:12 - 00:05:18] So, if I put a five KG on and it breaks instantly, it broke at the previously held weight.
[00:05:18 - 00:05:24] If I put on and it breaks, holds for one second in breaks, it doesn't get still the previous one.
[00:05:24 - 00:05:28] Once it's two seconds or more, then that holds the weight, right?
[00:05:28 - 00:05:33] So, that's what we call the two second rule and sometimes we have to do the TMO and I'll look at the camera
[00:05:33 - 00:05:36] and decide whether it's like how it's for two seconds or not.
[00:05:36 - 00:05:38] There's only a couple of those.
[00:05:38 - 00:05:46] So, if I show this one, then we can maybe just like talk through what's happened there, right?
[00:05:46 - 00:05:48] So, this could be you.
[00:05:48 - 00:05:52] You see that, I know some people would ask about how they put their apparatus in.
[00:05:52 - 00:05:55] We might see someone else sit up at the same time, right?
[00:05:55 - 00:05:58] At the moment, they've put on five KG.
[00:05:58 - 00:06:01] That's the first one of the second one. I can't really tell.
[00:06:01 - 00:06:03] Looks like two, right?
[00:06:03 - 00:06:05] So, that's 10 KG.
[00:06:05 - 00:06:11] Next, they've put it on 15 KG.
[00:06:11 - 00:06:13] Nice work, man.
[00:06:13 - 00:06:16] Put it on, they've put on a two this time, right?
[00:06:16 - 00:06:22] So, they're at, what's that? 17 plus one, right?
[00:06:22 - 00:06:30] So, the moment they put on three fives in one two, plus the weight of the hanger and the chain, right?
[00:06:30 - 00:06:38] So, if we had some sort of live scoring mechanism, you'd see like 18 point one on the readout of total mass, right?
[00:06:38 - 00:06:44] Cool. So, they're hoping to get over 20 to pass that first kind of benchmark, right?
[00:06:44 - 00:06:48] So, next what they're going to do, they've got another two KG.
[00:06:48 - 00:06:54] So, you can see that they're kind of trading carefully getting above the 20 KG back, right?
[00:06:54 - 00:07:00] Most commonly people just go 5, 5, 5, 5, 5 because they know what I confident that they won't break bang on 20.
[00:07:00 - 00:07:03] I don't know what their failure target was, right?
[00:07:03 - 00:07:10] So, they put this on, hold the two seconds, they're sort of happy that they've passed that threshold of getting those points on the match, right?
[00:07:10 - 00:07:20] So, next they've put on a 5 KG. So, what's that? That'll be 25 points something, right?
[00:07:20 - 00:07:26] Another 5 KG. So, now they're at like 30 I think, right?
[00:07:26 - 00:07:34] Now, the team's coming to get set up. As you can see, we'll make it run like clockwork.
[00:07:34 - 00:07:41] I think they're working out what we're going to do a two or five, I guess, is what the goal is, right?
[00:07:41 - 00:07:48] So, put a two on, it's hard for two seconds, so that counts. What are they 32, I think?
[00:07:48 - 00:07:56] I'm not too sure. Put another one on. 34, it's how'd 34 are at?
[00:07:56 - 00:08:00] What are they going to bring? They're bringing the big guns. This might be the pivotal moment, right?
[00:08:00 - 00:08:04] So, they might have had a target failure massive 34 in the hook in that.
[00:08:04 - 00:08:07] They put this on and they break straight away and they're like within their tolerance.
[00:08:07 - 00:08:13] They put the 5 KG on, technically, I think they'll be over their 39 KG limit, right?
[00:08:13 - 00:08:17] They're unhappy following, maybe it's like annoying that I'm talking for it.
[00:08:17 - 00:08:24] So, just like that. See? That's the kind of celebration there.
[00:08:24 - 00:08:27] Good old first problem, double five-fly.
[00:08:27 - 00:08:36] Cool. So, in that case it would have been 34 KG if I've done my math correctly at the same time, right?
[00:08:36 - 00:08:41] And then for those who are interested, because some people want to see this GIS rig and as I say,
[00:08:41 - 00:08:46] they're just heavy and it causes me physical pain to carry around.
[00:08:46 - 00:08:52] But you can see here this team, if we watch them sort of see what they do, right? Hopefully, lucky moves out of the way.
[00:08:52 - 00:08:58] They'll put... So, the devices got the pins and they're at the moment, right?
[00:08:58 - 00:09:02] Obviously you can't do that if you've got your two-minute structure or you can, but it's only...
[00:09:02 - 00:09:05] It's still floppy, you know, but for the triangle, it'll be sort of solid.
[00:09:05 - 00:09:10] And the idea is that they'll put their bottom corner into the kind of fixed support, right?
[00:09:10 - 00:09:17] And then what they'll do is move the top-pin and latch on this kind of roller support here, right?
[00:09:17 - 00:09:23] And then the final thing they'll do is add this chain attachment and then they'll adjust the hook to make sure that it's not too far off the ground,
[00:09:23 - 00:09:28] because we don't want these masses having to fall a large distance, right?
[00:09:28 - 00:09:33] So, hopefully, lucky takes a step back and we can sort of see what's actually going on.
[00:09:33 - 00:09:42] But they'll put it... Just can see it. Oh, it's painful, isn't it? It's right in the way.
[00:09:42 - 00:09:45] Also, if you look at the next video, we might be able to see it.
[00:09:45 - 00:09:48] If you can see, first they get down there, didn't have the hook to this one on there.
[00:09:48 - 00:09:55] You can see it's loose. And when they add this chain attachment, like this, they'll pull this forward, right?
[00:09:55 - 00:10:04] So, lock them low to ready to go. And the final thing they'll do is add the chain or add the low to attachment, right?
[00:10:04 - 00:10:09] Cool. Do we want to look at another video? Is that sort of answer the question?
[00:10:09 - 00:10:18] Answer it? You know, I want to see another video in the... Someone answered for the group.
[00:10:18 - 00:10:22] Nah, we don't. Sweet. Sure.
[00:10:22 - 00:10:34] Other questions? It's good? Yep. Yep, cool.
[00:10:34 - 00:10:41] So, the question I'll ask and answer it by looking at our nice flow diagram, which I've, you know,
[00:10:41 - 00:10:46] maybe I should have done a better job and taking some more care with making the look kind of nice.
[00:10:46 - 00:10:53] But what we've been asked is here, when we have our stress concentration member that we're designing for in our stress concentration,
[00:10:53 - 00:11:00] are you allowed to do some experimental testing to see whether you're assumed apparent stress concentration factor?
[00:11:00 - 00:11:07] If we use the quote from the notes, whether our assumption for our parents' stress concentration is correct, right?
[00:11:07 - 00:11:12] The answer is yes. You can do small scale tests to verify your assumption there, right?
[00:11:12 - 00:11:16] We don't want you to make a whole kind of your whole tensile piece and sort of test that.
[00:11:16 - 00:11:22] But similar kind of link to your dog bones. It's fine to do that. And you might test more than one
[00:11:22 - 00:11:29] because you'll have some experimental variation, possibly. Yeah. But with that, I will just make sure that you take particular care.
[00:11:29 - 00:11:37] In terms of your surface finish and care or at least consistency that, from whatever you do,
[00:11:37 - 00:11:45] you do it when you make a fit and forms your final designer. Cool. That kind of makes sense for everyone. Yeah.
[00:11:45 - 00:11:59] So that's completely all good. Yeah. So yeah. I've sort of seen a process of, for when it comes to designing your stress concentration,
[00:11:59 - 00:12:11] similar to what I talked through this morning that you might want to make the assumption that if the stress is designed to be approximately your ultimate tensile stress at your load of failure,
[00:12:11 - 00:12:20] that when you add another load, failure will occur, right? That's one approach that you could use. There are other ways you could approach it.
[00:12:20 - 00:12:28] And that's acceptable. But for now, I think that that's sort of fine. So other way could be if you really wanted to test multiple holes,
[00:12:28 - 00:12:35] which is probably a more work, you might be able to make your own relationship for whole size for a sitting wet throughout.
[00:12:35 - 00:12:44] And then you could use that to inform your design. But more than one way to skin the care as the sand goes. Cool.
[00:12:44 - 00:13:13] Other questions? What other questions do you have? I think anyone wants to ask. It's all good. I'm assuming that it's because you haven't come to having questions yet.
[00:13:13 - 00:13:22] So all my plan from here is, as I've got some sort of stuff to prompt us along. And then we'll see how we end up or where we land.
[00:13:22 - 00:13:26] I just have to make sure that I'm sort of consistent with this tutorial and the next tutorial.
[00:13:26 - 00:13:32] So hopefully for you guys, there don't have any banging questions that solve the world's problems, but it's probably unlikely.
[00:13:32 - 00:13:43] So next thing is our assignment tasks. I think I kind of got the vibe today that most people seem like about happy.
[00:13:43 - 00:13:48] we've done their free body diagram and stuff and how people are sort of done their experimental testing.
[00:13:48 - 00:13:59] So those first two boxes on the flow chart that I had, but yeah, feel free to update that choice poll just to keep me informed as you go.
[00:13:59 - 00:14:05] So here we see some material testing results for our yield stress.
[00:14:05 - 00:14:17] And it looks like option four slash five, which is 140 to 120. There's about what people are getting for the yield stress.
[00:14:17 - 00:14:29] Again, you can take these with a grain of salt, but the main reason that I'm sort of showing you these is that if, for example, you had option one was the result that you'd got.
[00:14:29 - 00:14:35] You might know something's wrong. Or if you know you were option eight, you might also know something's wrong.
[00:14:35 - 00:14:45] But if you're somewhere in this region, you can probably have confidence in your own results because your results are probably what I would have based my own calculations on my own results rather than other people.
[00:14:45 - 00:14:51] Right. It's more just to help the people if they know that they've got something that doesn't line up.
[00:14:51 - 00:15:00] I'm going to find, yeah, about 10 to 15 very low sample size. I've purposely done that so that purposely haven't shown them the count.
[00:15:00 - 00:15:01] Yeah.
[00:15:01 - 00:15:08] Because otherwise people just go second, I don't have to do any testing and they say, well, if you don't do the testing, you don't get the marks for describing how you got your material testing values.
[00:15:08 - 00:15:13] Right. So it's not really any benefit from doing it as, as I say, it's just the sort of.
[00:15:13 - 00:15:18] But you go, okay, cool. I think we've got something that's at least within the ballpark.
[00:15:18 - 00:15:27] So similarly, we've got UTS option, typically occurring around five six.
[00:15:27 - 00:15:31] So as I say, trust your own results.
[00:15:31 - 00:15:35] I don't know if people here necessarily understood that it was yield or UTS.
[00:15:35 - 00:15:47] There could be some crossover there. I don't know. But we see here, our UTS is typically a bit higher with most results being between option five and six, which is what on 40 to 160.
[00:15:47 - 00:15:58] Cool. So as I'd say, if you've done some testing, you'll have your own average value that you might use for your calculations.
[00:15:58 - 00:16:03] And you also have a variation in your results, right? Like standard deviation.
[00:16:03 - 00:16:11] Yeah. You want to agree with that. That's like so, that exists. Unless you're like, oh, we're one and done here. Hopefully it's right. Yeah.
[00:16:11 - 00:16:14] It's exactly this and good luck if we're wrong.
[00:16:14 - 00:16:23] Cool. So with that, the tangent that I was about to go on was related to our mark sheet for assignment one.
[00:16:23 - 00:16:29] Who do I have it here? One.
[00:16:29 - 00:16:31] Hey. Yeah.
[00:16:31 - 00:16:35] So I've mentioned explicitly this variation thing, right?
[00:16:35 - 00:16:37] The B1 and B2.
[00:16:37 - 00:16:42] And so here what we see, protected failure loads.
[00:16:42 - 00:16:46] So what are the failure loads of your first second and third mode of failure?
[00:16:46 - 00:16:48] That was what we're particularly interested in.
[00:16:48 - 00:16:54] And in particular, predicted failure range, I think is also something that's useful to incorporate.
[00:16:54 - 00:17:08] Does anyone want to let you know how you might come up with your predicted failure range?
[00:17:08 - 00:17:13] Yeah. You just like, okay. You're just like, oh, yeah. We designed it to be 35 kg.
[00:17:13 - 00:17:18] So my predicted failure ranges plus or minus two kg.
[00:17:18 - 00:17:32] Yeah. So ideally the answer to the question is that your predicted failure range should not be pulled out of
[00:17:32 - 00:17:35] the position here. It should be based on your results from testing.
[00:17:35 - 00:17:40] There's a number of ways you could base it. But for example, if you used an average,
[00:17:40 - 00:17:51] UTS value to calculate your failure member, you could also then use maybe your maximum and minimum to work out what the maximum and minimum load would be, right?
[00:17:51 - 00:18:01] So there's that same equation. If you're assuming that stress of UTS equals some k value times 4 over area, right?
[00:18:01 - 00:18:09] So using the two values in here for UTS, you could rearrange that to get two kind of load deductions, right?
[00:18:09 - 00:18:13] It's a bit of math there, but that's essentially what it's talking about.
[00:18:13 - 00:18:20] Oh, all right. Nice. And then finally we get Dung's modular,
[00:18:20 - 00:18:31] looking like it's between option two and three, which is 50 to 60 maybe. I know two three and four.
[00:18:31 - 00:18:41] It's kind of three plus or minus one option, right? So seems to be people are getting between 60 plus or minus maybe 15.
[00:18:41 - 00:18:48] But obviously we've already talked about, if we think about age low, whether that's conservative or not and what our approach can be,
[00:18:48 - 00:19:01] if we're wanting to update that or not, right? Is there any questions there? So the idea was like in the,
[00:19:01 - 00:19:08] I can update these values next week if we get more results. So there'll be helpful for you that go from there, right?
[00:19:08 - 00:19:13] Cool. So this is some quick fire questions just to test our understanding.
[00:19:13 - 00:19:19] So instead of asking you how this member failed, can you tell me what happened in this design?
[00:19:19 - 00:19:37] Well, kind of failure has occurred. Well, also failure, sorry. You're telling each other like I'm out of here.
[00:19:37 - 00:19:40] Yeah, you probably should be though. Yeah.
[00:19:40 - 00:19:44] Yeah, I know. So I mean, yeah, you probably shouldn't be.
[00:19:44 - 00:19:50] So, yeah, sorry. It's just, it is very hard when you're at the front and like you hear this murmuring,
[00:19:50 - 00:19:55] especially if it's off topic. So it's not a dig, but it's sort of just like a,
[00:19:55 - 00:20:01] please be respectful of your friend in the class kind of blood. So yeah, can anyone say what was,
[00:20:01 - 00:20:05] the reason that this is failed? What's happened at the end here?
[00:20:05 - 00:20:13] Nothing. Yeah, perfect. Thank you very much, right? So we've had buckling and then how could we avoid this?
[00:20:13 - 00:20:16] There's sort of two options we've discussed in the past.
[00:20:16 - 00:20:29] We could either make the flange longer yet so we could have like this middle book come all the way into the middle here.
[00:20:29 - 00:20:32] Or what else could we do?
[00:20:32 - 00:20:37] Could change the ideas of our webbed by adding more material on these two that's here.
[00:20:37 - 00:20:44] All we could make it shorter, right? Cool. Good stuff. Seems like we're all on board with that.
[00:20:44 - 00:20:49] Another question. What do we have to be careful about if we have a T-section,
[00:20:49 - 00:20:55] compressive member or an I-beam with a protruding extended web or an I-beam with a long extended flange.
[00:20:55 - 00:21:03] What kind of failure would be occurring? Most likely. Buckling it, yeah.
[00:21:03 - 00:21:19] So yeah, all of these things are something that you would need to make sure you're confident with your buckling that it won't buckle either in particular areas or in particular planes, right?
[00:21:19 - 00:21:28] So for example here, if we can zoom out enough, this is like so close.
[00:21:28 - 00:21:35] This is an example of a member that has buckled, right? And if you can see that, if you can see that up here.
[00:21:35 - 00:21:46] Yeah? So obviously with the I-value, that plane must have not been sufficient to resist the buckling out. It's pretty long in there.
[00:21:46 - 00:21:49] So do we have a team member that we had buckled?
[00:21:49 - 00:21:51] Here's the same sort of thing, right?
[00:21:51 - 00:21:58] It might again not be able to fit on our document camera, but we can see that it's definitely buckled.
[00:21:58 - 00:22:01] It looks like a smiley face. Yeah?
[00:22:01 - 00:22:08] So again, what might have happened is that they maybe just looked at the buckling in one plane and not the other plane.
[00:22:08 - 00:22:12] And that could have been what promoted the failure. All what could have happened is they didn't fail.
[00:22:12 - 00:22:18] They didn't design their failure member appropriately, so this might have been their second-load of failure.
[00:22:18 - 00:22:29] I'm not too sure. I didn't design it. So we can see that that can happen for our whole members or it can happen, particularly at the edges, right?
[00:22:29 - 00:22:34] And then this one here when we're talking about clearance fits on compressive failure.
[00:22:34 - 00:22:41] What aspect of the buckling in my kind of referring to?
[00:22:41 - 00:22:47] Secondly, if it was I beam, right? So if we think about it I beam,
[00:22:47 - 00:22:51] theoretically, if we have this direction, what are their incanditions?
[00:22:51 - 00:22:59] What's at the top? Ten, what's at the bottom? So that's pen turn right?
[00:22:59 - 00:23:03] This way, theoretically, what are our incanditions?
[00:23:03 - 00:23:08] Flex, flex, right? What we see is what is probably a more appropriate approximation
[00:23:08 - 00:23:13] for being super conservative. So again, yeah.
[00:23:13 - 00:23:15] What's our conservative approximation of our incanditions?
[00:23:15 - 00:23:20] Instead of flex six, we're thinking of pen turn right?
[00:23:20 - 00:23:25] And that's particularly the case if we have loose holes, right, where it can kind of wobble around, right?
[00:23:25 - 00:23:34] So yeah, this one here we can see that's our example of where they've actually these extended parts of the flange.
[00:23:34 - 00:23:42] You can see that they've doubled up the material there to make sure they're confident that buckling won't occur, yeah?
[00:23:42 - 00:23:45] Some people design the problem away.
[00:23:45 - 00:23:48] In other ways, like that, that's right.
[00:23:48 - 00:23:52] So they could keep that number there and then just have a slot to make sure they're down.
[00:23:52 - 00:23:56] Now, other than the timber still has their clearance, it needs to be able to go together.
[00:23:56 - 00:24:06] Cool. Well, things could we do to reduce weight in our design?
[00:24:06 - 00:24:16] What is the trade-off of adding weight reduction in your design, maybe?
[00:24:16 - 00:24:21] It's another way we can rephrase it.
[00:24:21 - 00:24:28] Rust, right? So what happens if we say if we want to reduce weight by adding a hole or a slot?
[00:24:28 - 00:24:33] What risk are we kind of introducing to our design?
[00:24:33 - 00:24:40] Could be a stress concentration, especially if it was on our tinsel, I'm in the right.
[00:24:40 - 00:24:44] What if it was on our compressor member? What material property would be changing?
[00:24:44 - 00:24:49] Our i-value, because we're changing across section, right?
[00:24:49 - 00:24:54] So if you're going to have these trade-off, if you want to make your design light more lightweight,
[00:24:54 - 00:24:59] it may also introduce additional work for you to do, right?
[00:24:59 - 00:25:05] Yes, I was on you as a designer to make sure that whatever weight reduction you employ in your design,
[00:25:05 - 00:25:09] that you're still confident that it's not going to fail because of that, right?
[00:25:09 - 00:25:14] And we sort of sometimes see that happened. I haven't brought some of the ones that have done that.
[00:25:14 - 00:25:17] That's sort of a slightly different thing.
[00:25:17 - 00:25:26] Yeah, cool. There we go. Got those two answers there for you.
[00:25:26 - 00:25:31] Cool. So that is pretty close to most of the main points that I had for you guys.
[00:25:31 - 00:25:38] What I do have is one other point before we go any further.
[00:25:38 - 00:25:42] So this design here, you can see it's buckled, right?
[00:25:42 - 00:25:48] And the main discussion point, it's sort of hard to see on the document camera, but like what it is,
[00:25:48 - 00:25:55] it's been an eye beam that's meant to have been made out of two pieces of aluminium, right?
[00:25:55 - 00:25:58] But what the students found was, actually, really difficult,
[00:25:58 - 00:26:02] well, they thought it'd be really easy to kind of do it as one piece.
[00:26:02 - 00:26:06] And it wasn't, so they made the design change that they are going to cut it up and
[00:26:06 - 00:26:08] the small bits and glue it together.
[00:26:08 - 00:26:13] And basically, what that meant is that at the point where it's actually failed,
[00:26:13 - 00:26:19] you can see that there's actually, the cross-section hasn't basically remained consistent
[00:26:19 - 00:26:24] in that they've had a buckling failure due to the fact that it's just one of these
[00:26:24 - 00:26:27] C-sections that's actually taken a load rather than two, right?
[00:26:27 - 00:26:33] I suppose a little, a little, listen here or the little warning is this, whatever you design
[00:26:33 - 00:26:38] and whatever you make on your drawings, make sure that you're confident that you can make it
[00:26:38 - 00:26:44] full stop and also to this piece of fashion that you say on your drawings, right?
[00:26:44 - 00:26:53] All right, so before we go any further, is there any other, has any of that opened up
[00:26:53 - 00:26:55] any questions that you might have?
[00:26:55 - 00:27:09] So, channel your decisive nature, I know that everyone's like,
[00:27:09 - 00:27:14] I don't want to have to make a decision for everyone, but for a question that someone
[00:27:14 - 00:27:19] or collectively we can do a vote if that's what we want to do, sort of needs to decide,
[00:27:19 - 00:27:26] but if you don't have any questions, we have options we could talk through a worked example
[00:27:26 - 00:27:30] or an approach for one of these calculations, and we ever us sort of suspect that a lot
[00:27:30 - 00:27:34] of people are actually confident with these kind of calculations, it's just that you haven't had the
[00:27:34 - 00:27:39] time to go over them, so option one is that we do one of these worked examples,
[00:27:39 - 00:27:44] option two is that we review another student's drawing in kind of critique it,
[00:27:44 - 00:27:47] which we did on Friday, some people might have missed that live experience,
[00:27:47 - 00:27:50] so we could do that as well.
[00:27:50 - 00:27:56] And the third option is that we say, oh that's tools downtime, you actually work on your assignment
[00:27:56 - 00:27:59] for the next 20 minutes and do the free body diagram, whatever,
[00:27:59 - 00:28:04] and I can just float round and ask or answer smaller questions that you might not want to ask in front of everyone.
[00:28:04 - 00:28:10] So have a think, I'm going to let you do a vote to say put your hand out for which one,
[00:28:10 - 00:28:14] you can vote multiple times if you want to I guess.
[00:28:14 - 00:28:22] So, option one, who wants to do a worked example?
[00:28:22 - 00:28:30] Okay, two, four, six, let's see.
[00:28:30 - 00:28:35] 18, cool. Option two, who wants to review some drawings?
[00:28:35 - 00:28:45] Cool. Option three, who wants to spend this time to do independent work and have me ask,
[00:28:45 - 00:28:50] slash answer questions as you go, two, four, six, eight.
[00:28:50 - 00:28:55] Yep, that's the con, let's, so we have a winner over there.
[00:28:55 - 00:29:02] Cool, so that's awesome. So the thing is, if you were one of the people that said I wanted to do a worked example,
[00:29:02 - 00:29:09] there are these examples here, better questions, so you could work on those and I'm happy to answer you as you go.
[00:29:09 - 00:29:12] Otherwise, I'll be floating around.
[00:29:12 - 00:29:25] Oh, there's also a bunch of example kind of test pieces if you want to look at those as you go in.
[00:29:25 - 00:29:26] Yeah.
[00:29:26 - 00:29:27] Yeah.
[00:29:27 - 00:29:28] Yeah.
[00:29:28 - 00:29:29] This one.
[00:29:29 - 00:29:30] Yeah.
[00:29:30 - 00:29:54] Just did it.
[00:29:54 - 00:29:55] Oh, yeah.
[00:29:55 - 00:30:04] Sorry.
[00:30:04 - 00:30:05] Yeah.
[00:30:05 - 00:30:06] Yeah.
[00:30:06 - 00:30:07] Yeah.
[00:30:07 - 00:30:08] Yeah.
[00:30:08 - 00:30:09] Yeah.
[00:30:09 - 00:30:10] Yeah.
[00:30:10 - 00:30:11] Yeah.
[00:30:11 - 00:30:12] Yeah.
[00:30:12 - 00:30:13] Yeah.
[00:30:13 - 00:30:14] Yeah.
[00:30:14 - 00:30:15] Yeah.
[00:30:15 - 00:30:16] Yeah.
[00:30:16 - 00:30:17] Yeah.
[00:30:17 - 00:30:18] Yeah.
[00:30:18 - 00:30:19] Yeah.
[00:30:19 - 00:30:20] Yeah.
[00:30:20 - 00:30:21] Yeah.
[00:30:21 - 00:30:22] Yeah.
[00:30:22 - 00:30:23] Yeah.
[00:30:23 - 00:30:24] Yeah.
[00:30:24 - 00:30:25] Yeah.
[00:30:25 - 00:30:26] Yeah.
[00:30:26 - 00:30:27] Yeah.
[00:30:27 - 00:30:28] Yeah.
[00:30:28 - 00:30:29] Yeah.
[00:30:29 - 00:30:30] Yeah.
[00:30:30 - 00:30:31] Yeah.
[00:30:31 - 00:30:32] Yeah.
[00:30:32 - 00:30:33] Yeah.
[00:30:33 - 00:30:34] Yeah.
[00:30:34 - 00:30:35] Yeah.
[00:30:35 - 00:30:36] Yeah.
[00:30:36 - 00:30:37] Yeah.
[00:30:37 - 00:30:38] Yeah.
[00:30:38 - 00:30:39] Yeah.
[00:30:39 - 00:30:40] Yeah.
[00:30:40 - 00:30:41] Yeah.
[00:30:41 - 00:30:42] Yeah.
[00:30:42 - 00:30:43] Yeah.
[00:30:43 - 00:30:44] Yeah.
[00:30:44 - 00:30:45] Yeah.
[00:30:45 - 00:30:46] Yeah.
[00:30:46 - 00:31:09] Yeah, that's not good.
[00:33:39 - 00:33:41] I think it's a good one.
[00:33:41 - 00:33:43] I think it's a good one.
[00:33:43 - 00:33:45] Yeah, it's a good one.
[00:33:45 - 00:33:47] Yeah.
[00:33:47 - 00:33:49] So we can get the,
[00:33:49 - 00:33:51] the,
[00:33:51 - 00:33:53] the,
[00:33:53 - 00:33:55] the,
[00:33:55 - 00:33:57] the,
[00:33:57 - 00:33:59] the,
[00:33:59 - 00:34:01] the,
[00:34:01 - 00:34:03] the,
[00:34:03 - 00:34:05] the,
[00:34:05 - 00:34:07] the,
[00:34:07 - 00:34:10] the
[00:34:10 - 00:34:13] the
[00:34:13 - 00:34:16] two.
[00:34:16 - 00:34:19] One.
[00:34:49 - 00:34:53] I can't see that.
[00:34:53 - 00:34:54] It's not much.
[00:34:54 - 00:34:57] I can see that.
[00:34:57 - 00:35:00] I can see that.
[00:35:00 - 00:35:02] It's not much.
[00:35:02 - 00:35:03] It's not much.
[00:35:03 - 00:35:08] It's not much.
[00:35:08 - 00:35:11] It's not much.
[00:35:11 - 00:35:15] It's just a multitude of opportunities.
[00:35:15 - 00:35:26] but at once only they were supposed to want
[00:36:56 - 00:37:06] I think we're going to say I like that.
[00:37:06 - 00:37:08] I feel like when you leave it all like that,
[00:37:08 - 00:37:10] you can keep it.
[00:37:10 - 00:37:12] And how good do you attend.
[00:37:42 - 00:37:49] I don't know how they call it.
[00:37:49 - 00:37:56] I don't know how they call it.
[00:37:56 - 00:37:59] I'm going to do that.
[00:37:59 - 00:38:02] I'm going to do that.
[00:38:02 - 00:38:05] I'm going to do that.
[00:38:05 - 00:38:08] I think we'll knock there.
[00:38:39 - 00:38:40] You know what thing is happening?
[00:38:40 - 00:38:44] The second is that the new show where they are in the area.
[00:38:44 - 00:38:46] They're like living in the material.
[00:38:46 - 00:38:47] You know?
[00:38:47 - 00:38:49] You have an attempt to put the materials.
[00:38:49 - 00:38:51] I was like, what have you got?
[00:38:51 - 00:38:52] I've been sitting there all night.
[00:38:52 - 00:38:53] I've been sitting there all night.
[00:38:53 - 00:38:54] Yeah, but that's really cool.
[00:38:54 - 00:38:56] I've been sitting there all night.
[00:38:56 - 00:38:57] I've been sitting there all night.
[00:38:57 - 00:38:59] I've been sitting there all night.
[00:38:59 - 00:39:01] I've been sitting there all night.
[00:39:01 - 00:39:03] So I've gone away from my...
[00:39:03 - 00:39:04] I am.
[00:39:04 - 00:39:06] at the first time.
[00:39:06 - 00:39:08] So it's yeah.
[00:39:08 - 00:39:10] So it's yeah.
[00:39:10 - 00:39:13] And I'm doing that.
[00:39:13 - 00:39:16] So that's right.
[00:39:16 - 00:39:18] I'm doing that.
[00:39:18 - 00:39:22] It's, it's good to be in the area.
[00:39:22 - 00:39:24] I am doing the video.
[00:39:24 - 00:39:26] I'm doing that.
[00:39:26 - 00:39:28] This is kind of a sense of it.
[00:39:28 - 00:39:33] Since I was in 2000, you know, it's really great to meet you group.
[00:40:03 - 00:40:05] I'm not sure if anyone's left or anything else.
[00:40:05 - 00:40:07] It's just a few days ago.
[00:40:07 - 00:40:09] So that's why I'm...
[00:40:09 - 00:40:11] Thank you, Bitch.
[00:40:11 - 00:40:13] I'm glad to be here.
[00:40:13 - 00:40:15] I'm glad to be here.
[00:40:15 - 00:40:17] I'm glad to be here.
[00:40:17 - 00:40:21] Well, just to talk about being a mother of a young baby,
[00:40:21 - 00:40:23] I'm glad to be here.
[00:40:23 - 00:40:25] I'm glad to be here.
[00:40:25 - 00:40:27] I'm glad to be here.
[00:40:27 - 00:40:29] I'm glad to be here.
[00:40:29 - 00:40:31] I'm glad to be here.
[00:40:31 - 00:40:33] I'm glad to be here.
[00:40:33 - 00:40:35] I'm glad to be here.
[00:40:35 - 00:40:37] I'm glad to be here.
[00:40:37 - 00:40:39] I'm glad to be here, too.
[00:40:39 - 00:40:41] We're glad to be here.
[00:40:41 - 00:40:43] If you're happy to be here, you know.
[00:40:43 - 00:40:45] Now you're's beautiful.
[00:40:45 - 00:40:47] I'm glad to be here.
[00:40:47 - 00:40:49] I thought I was able to be here.
[00:40:49 - 00:40:51] So, maybe I'm keen to be here?
[00:40:51 - 00:40:53] Maybe maybe I'm anxious,
[00:40:53 - 00:40:57] but you think there's something that might be a lot too much to do with them.
[00:41:27 - 00:41:31] I'm getting sick.
[00:41:31 - 00:41:33] I'm sick.
[00:41:33 - 00:41:35] I'm sick.
[00:41:35 - 00:41:37] Yeah, I'm sick.
[00:41:37 - 00:41:41] So, I'm sick.
[00:41:41 - 00:41:46] Yeah, I'm sick.
[00:41:46 - 00:41:48] I'm sick.
[00:41:48 - 00:41:51] But I don't know why.
[00:42:21 - 00:42:24] All my friends are made with a shake.
[00:42:24 - 00:42:27] I'm leaving for a few minutes.
[00:42:27 - 00:42:29] I'm not going to have to say that.
[00:42:29 - 00:42:31] But you think that you're just doing the same?
[00:42:31 - 00:42:33] I'm doing the same.
[00:42:33 - 00:42:35] I'm doing the same.
[00:42:35 - 00:42:37] I'm doing the same.
[00:42:37 - 00:42:39] I'm doing the same.
[00:42:39 - 00:42:41] I'm doing the same.
[00:42:41 - 00:42:43] I'm doing the same.
[00:42:43 - 00:42:45] I'm doing the same.
[00:42:45 - 00:42:47] Yeah, I thought it was a construction.
[00:43:17 - 00:43:19] I've already ordered this, really.
[00:43:19 - 00:43:23] Now that people are going to try to prove it.
[00:43:23 - 00:43:25] I think it's been created.
[00:43:25 - 00:43:27] I'm in the middle.
[00:43:27 - 00:43:29] I'm not an isker.
[00:43:29 - 00:43:31] I'm not going to do this.
[00:43:31 - 00:43:33] I think it's been created.
[00:43:33 - 00:43:37] That's why I do that, it's not going to do it.
[00:43:37 - 00:43:40] I don't know.
[00:43:40 - 00:43:42] I don't know.
[00:43:42 - 00:43:44] I don't know.
[00:43:44 - 00:43:51] I'm just going to take it out of place.
[00:43:51 - 00:43:58] I'm just going to take it out of place.
[00:43:58 - 00:44:03] I'm just going to take it out of place.
[00:44:03 - 00:44:12] And I say bimos.
[00:44:12 - 00:44:14] I do want bums.
[00:44:14 - 00:44:16] I'm kind of flimsy.
[00:44:16 - 00:44:19] I'm really losing.
[00:44:19 - 00:44:21] Small.
[00:44:21 - 00:44:23] Look at what you want.
[00:44:23 - 00:44:26] How long are I going to get?
[00:44:26 - 00:44:30] I go more.
[00:44:30 - 00:44:32] I call on fall, and fall.
[00:48:02 - 00:48:08] Hey everyone, just before we start sort of finishing, I will still float around right up until
[00:48:08 - 00:48:11] two so if you've got questions I've got a couple over there to answer and then I'll come
[00:48:11 - 00:48:16] kind of through but just quickly there was a question around the calculations and whether
[00:48:16 - 00:48:21] or not you're allowed to use electronic calculations or not. As long as it's handwritten
[00:48:21 - 00:48:25] that's fine right? So you could write it down a bit of a paper, a four paper is sort
[00:48:25 - 00:48:30] of your standard size, you could write it on an iPad that's also fine but we're not wanting
[00:48:30 - 00:48:36] like typed out on word or typed out calculations right? So that's probably maybe I'll
[00:48:36 - 00:48:43] go through that next week as to what is actually required in the submission right? Because
[00:48:43 - 00:49:15] that'll be nice. Otherwise I'll keep floating around but yeah.
[00:53:08 - 00:53:15] I don't know what it's supposed to be. Not that in but then I've broken it out.
[00:54:08 - 00:54:15] I don't know what I'm saying. I don't know what I'm saying. I don't know what I'm saying.
[00:54:15 - 00:54:22] I don't know what I'm saying. I don't know what I'm saying. I don't know what I'm saying
[00:54:45 - 00:54:52] but I don't know what I'm saying. I don't know what I'm saying. I don't know what I'm

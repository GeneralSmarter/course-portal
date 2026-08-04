# ENMT301-26W Lecture 54 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `1dc3ae56a354bc76e77e5e1e31be419019e25cf7ee6b57db21849bfaa7cb3aab`
Generated: 2026-06-06T07:04:13.651382+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:00 - 00:00:05] attention side of the chain.
[00:00:05 - 00:00:14] If you really need to, if you want to, that might be a bit expensive.
[00:00:14 - 00:00:21] Alright, you could ask them in the global questions or I'll be free at 10 to a game, but
[00:00:21 - 00:00:32] we should probably get the next one going.
[00:00:32 - 00:00:35] We aren't business time, but we're going.
[00:00:35 - 00:00:36] Oh, good.
[00:00:36 - 00:00:41] Yeah.
[00:00:41 - 00:00:46] I think it's the time of the semester as well, but possibly something they like to update
[00:00:46 - 00:00:56] for timetableing in the future, but I don't know.
[00:00:56 - 00:00:59] I think it depends on workload and what's happening.
[00:00:59 - 00:01:01] Normally, I get the very start of the semester there.
[00:01:01 - 00:01:07] It'll be like pretty much people and the room that we essentially be full, but then there's
[00:01:07 - 00:01:12] the semester goes on.
[00:01:12 - 00:01:15] People decide, or they might be watching online.
[00:01:15 - 00:01:16] So, yeah.
[00:01:16 - 00:01:17] Alright, welcome everyone.
[00:01:17 - 00:01:22] Thank you for showing up or watching this in the future.
[00:01:22 - 00:01:23] You'll see that Rebecca's here.
[00:01:23 - 00:01:25] She is evaluating me, not you.
[00:01:25 - 00:01:30] So, that's that.
[00:01:30 - 00:01:35] We can, yeah, we can keep it relatively as we normally do.
[00:01:35 - 00:01:40] So, in the last tutorial, I made a very bold move to, well, I saw this diagram that I'd made
[00:01:40 - 00:01:44] and showed you guys before, and I thought, oh man, this is a great flow diagram.
[00:01:44 - 00:01:47] I should really show it more often.
[00:01:47 - 00:01:52] And so, what we can see here is that this might be the step that you take when you're completing
[00:01:52 - 00:01:56] your bearing housing assignment, which we are getting things full questions about, which
[00:01:56 - 00:01:57] is great to see.
[00:01:57 - 00:02:06] And so, with this here, what I wanted to use it to do was to see how far through you guys
[00:02:06 - 00:02:12] are, so that then I sort of know the level of question and answer, I would be expecting
[00:02:12 - 00:02:15] if I was in your situation.
[00:02:15 - 00:02:21] So, for the people in the room, who has determined this system loads and have taken
[00:02:21 - 00:02:23] that one off.
[00:02:23 - 00:02:24] Cool.
[00:02:24 - 00:02:28] So, if you have at least started, if you have started it, or...
[00:02:28 - 00:02:29] Okay.
[00:02:29 - 00:02:36] So, the idea is that that part, which I talked about in the lecture today, it's sort of like
[00:02:36 - 00:02:39] sets you up to then do all the other bits, right?
[00:02:39 - 00:02:43] And now, idea is that once you've got your system loads, then you can have that to do
[00:02:43 - 00:02:48] often that you shouldn't have to iterate because a lot of the forces and the placements
[00:02:48 - 00:02:51] of our machine elements are very well defined this year, right?
[00:02:51 - 00:02:57] So, we're not going to change things that are going to change our loads and our systems.
[00:02:57 - 00:03:02] And so, just to summarize, so I have still had a couple questions from people who I think
[00:03:02 - 00:03:06] are a little bit unsure, is that to start with this, what is the first assumption that you
[00:03:06 - 00:03:08] guys need to make?
[00:03:08 - 00:03:10] The chain direction.
[00:03:10 - 00:03:16] And so, I've broadly said that there are three possible directions that you might choose.
[00:03:16 - 00:03:23] Either the chain is acting vertically intention, it's acting horizontally intention, or it's acting in some
[00:03:23 - 00:03:24] angle, right?
[00:03:24 - 00:03:25] Now, why is this important?
[00:03:25 - 00:03:27] And why is it important to show?
[00:03:27 - 00:03:33] Well, I've asked you guys to make sure that you show your shear force in binima-mid diagrams for
[00:03:33 - 00:03:35] both your front and your top view, right?
[00:03:35 - 00:03:41] And so, if you pick at to be horizontal or vertical in one of the other planes, there's
[00:03:41 - 00:03:46] going to be no force from this standard loading case.
[00:03:46 - 00:03:48] That is okay.
[00:03:48 - 00:03:49] Yeah?
[00:03:49 - 00:03:54] Those three options are all possible options for this, and I've purposely done that, so there's some
[00:03:54 - 00:04:00] variation in what you get, so everyone's not just ending up the exact same bearing and bearing housing arrangement.
[00:04:00 - 00:04:09] When we're choosing our chain load, we are assuming that we are having max power from the motor,
[00:04:09 - 00:04:12] from this otherwise specified, right?
[00:04:12 - 00:04:17] And then from that, what are we going to check before going too much further?
[00:04:17 - 00:04:29] Yeah, so you've just been told, we're using this motor, and no one that you are aware of has actually done any calculations
[00:04:29 - 00:04:33] or showed that this motor is big enough for the design situation.
[00:04:33 - 00:04:38] So that's where you would need to verify before going too much further.
[00:04:38 - 00:04:44] And then you would go through and you would have your shear force and bending moment diagrams for your front and your top view,
[00:04:44 - 00:04:45] which is great.
[00:04:45 - 00:04:48] Once you've done that, we would look at our secondary moments,
[00:04:48 - 00:04:53] who here has done the secondary moment analysis, cool.
[00:04:53 - 00:05:02] And then, depending on the initial assumption of your chain loads, you'll have to combine the effect of this additional
[00:05:02 - 00:05:06] secondary moment on your shaft to your standard loading case, right?
[00:05:06 - 00:05:11] So sometimes this may just be acting all on the same plane and you'll just combine it,
[00:05:11 - 00:05:15] we'll sum it together, sometimes they may be acting perpendicular,
[00:05:15 - 00:05:18] you might have to do some Pythagoras to work out.
[00:05:18 - 00:05:23] What the moment is at the specific point in the shaft of interest.
[00:05:23 - 00:05:26] Any questions on any of that?
[00:05:26 - 00:05:34] Cool, so I think we're, I think, do you really speaking, I think most people are like a fair way through,
[00:05:34 - 00:05:41] but I guess I'm just trying to make sure and encourage to keep moving because a lot of people can get just stuck.
[00:05:41 - 00:05:45] Looking at system loads for infinite amounts of time.
[00:05:45 - 00:05:50] So once you've got those system loads, they'll allow you to work out your shaft size, who's done that.
[00:05:50 - 00:05:56] Cool was the shaft big or small, it was big, and so we saw that it was a predefined
[00:05:56 - 00:06:02] process, a rocket with a sprocket or, so if your shaft size is bigger than this sprocket's
[00:06:02 - 00:06:07] or just make sure that you state that, I don't expect you to update the design,
[00:06:07 - 00:06:11] but I expect you to make that clear in your report that this is probably something that
[00:06:11 - 00:06:19] either needs to be remedied by taking a different sprocket or by boring out a larger hole in the
[00:06:19 - 00:06:23] sprocket or similar, right?
[00:06:23 - 00:06:28] And then if we have a big shaft, that means we're going to have big bearings.
[00:06:28 - 00:06:31] So has anyone done your bearing selection in life?
[00:06:31 - 00:06:38] Yep, and was, have you done any life calculations in the past?
[00:06:38 - 00:06:46] So, okay, we can probably cut touching in a little bit, but I guess my main point that I'm trying to make here is that if you have a large shaft,
[00:06:46 - 00:06:54] you're going to have a big bearing, big bearings are strong and useful, big loads, which might mean that your life is relatively large.
[00:06:54 - 00:07:00] So, if we're possible, we want to make sure that our life is not unreasonably large.
[00:07:00 - 00:07:06] We don't want to make you pick a big bearing of the options that you've got,
[00:07:06 - 00:07:12] but if you've picked the smallest kind of bearing that you could for the war size that you have of your shaft,
[00:07:12 - 00:07:16] that's all you can kind of really do in this instance, right?
[00:07:16 - 00:07:21] But if you've used the roller bearing, that might mean, as a roll bearing is way too strong,
[00:07:21 - 00:07:31] it might mean that you actually want to investigate whether using a ball bearing or similar might be more appropriate for the kind of life that we are wanting, right?
[00:07:31 - 00:07:57] So, we're seeing, this is a sketch of what your system is and we've said that.
[00:07:57 - 00:08:03] One of our bearings we will show is a fixed fin and one is a roll of pen, right?
[00:08:03 - 00:08:07] For the assumptions for our Geforce minimum diagrams yet.
[00:08:07 - 00:08:14] And so, if we're assuming it's a pin, what kind of loading does that need to be capable of holding?
[00:08:14 - 00:08:21] Right, right? So, it's definitely going to be axial loads, but this one here is also going to be actually restraining our system,
[00:08:21 - 00:08:26] left and right. So, we need to make sure that we pick a bearing that does that,
[00:08:26 - 00:08:33] because if we just pick like a cylindrical roller bearing, you know, just slide apart if any load was applied to it,
[00:08:33 - 00:08:44] and that's kind of what we're trying to avoid especially in transit or similar, right?
[00:08:44 - 00:08:49] Did you look at the tables on the spec sheets?
[00:08:49 - 00:08:54] Let's see again. Just to make sure we're comparing apples with apples.
[00:08:54 - 00:09:09] Yeah. So, what I would do, if I look at the PDF of additional bearing information, what I'm sort of talking about is that when we see these kind of tables from our bearing manufacturer,
[00:09:09 - 00:09:16] that's not the best one, but this one's a little bit better. We can see that some of them tell you whether it can have axial or combined loading,
[00:09:16 - 00:09:22] and whether it's in both directions or only one direction. So, the S-F handout, I mean this one sort of shows here.
[00:09:22 - 00:09:30] I think the example that we've seen in the past is if you had a cylindrical roller bearing, it's really good at having a large radial load.
[00:09:30 - 00:09:37] And in this case, it can have axial load in one direction, so maybe that's not fully cylindrical.
[00:09:37 - 00:09:41] I don't have to have a look at that, but I can't really tell on the screen.
[00:09:41 - 00:09:48] But if we had, say, a deep groove ball bearing, we can see I can hold a radial load, and it can hold an axial load in both directions.
[00:09:48 - 00:09:53] And that's what I'd kind of be using to narrow down my bearing selection in the first instance.
[00:09:53 - 00:10:16] But basically, you'll need to work out your equivalent dynamic load, and that's where it's incorporated.
[00:10:16 - 00:10:25] So you don't look at it in that granular way, they've kind of bastardized it or simplified it, and that's what that life calculation is doing,
[00:10:25 - 00:10:31] is validating that for your scenario, that will be appropriate.
[00:10:31 - 00:10:38] I can go on more detail, but I'm like, so if you remember when you work out the equivalent dynamic load,
[00:10:38 - 00:10:43] I'm really pulling from my mind here, like some real niche like SKF bearing catalog stuff,
[00:10:43 - 00:10:49] but it'll be like some factor times the radial force, and another factor times the axial force.
[00:10:49 - 00:11:01] So you'll see there that there'll be a few things,
[00:11:01 - 00:11:07] in terms of the type needed, that space that you have in the life, that you'll have to basically put one and see what it is.
[00:11:07 - 00:11:14] And then maybe that's right, at least once, unless you're picked for a bearing that is appropriate,
[00:11:14 - 00:11:23] and you'll design the rest of your system around that, but this kind of flow diagram will help you in doing that process.
[00:11:23 - 00:11:28] So I go to the start of these slides here,
[00:11:28 - 00:11:32] we can see what we'll do.
[00:11:32 - 00:11:37] I've been updating the frequently asked questions, so make sure that you're aware of those.
[00:11:37 - 00:11:42] Do have a new paper published, which we talked about I think last week.
[00:11:42 - 00:11:49] Now as I've put this up before, we even went to the term break, so very much playing in advance.
[00:11:49 - 00:11:53] We'll see today, I'll spend some time answering any questions that you've got as they come up.
[00:11:53 - 00:11:58] We'll go through some reminders for our drawings, and we'll review some drawings.
[00:11:58 - 00:12:04] Then in subsequent tutorials, we only have really next week, I think,
[00:12:04 - 00:12:08] we'll be having that pretty similar to how we did last semester,
[00:12:08 - 00:12:12] where after that we'll kind of follow the bearing questions globally answered,
[00:12:12 - 00:12:18] and then I can just float around if there are specific things that people have to go over.
[00:12:18 - 00:12:22] And so the notes that I had, the only thing I wanted to remember,
[00:12:22 - 00:12:27] was that for the retesting, if you're not making any changes, you just show up,
[00:12:27 - 00:12:33] but thanks to your run for the patience, if you were, there are Monday, a lot of people.
[00:12:33 - 00:12:36] So you appreciate that.
[00:12:36 - 00:12:42] So, open floor time, questions that are currently working you.
[00:12:42 - 00:12:54] Oh yeah.
[00:12:54 - 00:12:58] Approximately, if there's zero per night right with the sprocket size.
[00:12:58 - 00:13:00] No issues there.
[00:13:00 - 00:13:03] You bet outside of the scope of what you need to do.
[00:13:03 - 00:13:05] We'll just see it.
[00:13:05 - 00:13:09] So I'll just, it will be in reality 0.8 seconds.
[00:13:09 - 00:13:11] Yeah.
[00:13:11 - 00:13:15] Yes, the question is, you would respond to the error in your math
[00:13:15 - 00:13:21] when you worked out the shaft RPM in the speed of the sprocket, the size of the sprocket right?
[00:13:21 - 00:13:22] Yeah.
[00:13:22 - 00:13:27] Yeah.
[00:13:27 - 00:13:32] Yeah, that's my bed, but it's to be updated on, well, I'll say on the frequent ask questions,
[00:13:32 - 00:13:37] but it's sort of, it's not really used for anything other than the enjoyment of the rider, I suppose.
[00:13:37 - 00:13:41] But just use the RPM that you've been given.
[00:13:41 - 00:13:46] Cool.
[00:13:46 - 00:13:51] So for the bearing life, should I do the basic life or the new bearing life or both?
[00:13:51 - 00:13:56] And so some people will be like, what is that, other people?
[00:13:56 - 00:14:02] And so the answer is, you get rewarded for doing more detail.
[00:14:02 - 00:14:04] So definitely do at least the basic life.
[00:14:04 - 00:14:10] And then the new life equation, this is an improved equation that incorporates
[00:14:10 - 00:14:16] environmental conditions and operating conditions, right?
[00:14:16 - 00:14:36] So you could do both and then compare what other questions do you currently have?
[00:14:36 - 00:14:41] So for the secondary moments where people relatively comfortable are you feeling relatively
[00:14:41 - 00:14:44] comfortable about what's happening there and how that works?
[00:14:44 - 00:14:57] So there's a few people that sort of just mentioned, I guess.
[00:14:57 - 00:15:02] The way that I'll think about it is that there's a moment being applied to the end of the shaft
[00:15:02 - 00:15:03] cyclically.
[00:15:03 - 00:15:09] So that means that for that moment diagram, it's going to be like we're seeing in one of the
[00:15:09 - 00:15:14] examples where the moment is an axiom of that at the end, it once again to the bearing,
[00:15:14 - 00:15:19] that's kind of linearly, linearly going to zero the other bearing, right?
[00:15:19 - 00:15:23] I think we're happy with secondary moments.
[00:15:23 - 00:15:24] So we're okay.
[00:15:24 - 00:15:26] Cool.
[00:15:26 - 00:15:32] What other questions do we have?
[00:15:32 - 00:15:36] So has anyone done any of the calculations relating to the spring?
[00:15:36 - 00:15:42] Has anyone looked at that?
[00:15:42 - 00:15:46] Is there one aware that you have to do a calculation for a spring?
[00:15:46 - 00:15:49] Yeah, we've got some nods there.
[00:15:49 - 00:15:52] So there was a few questions last tutorial.
[00:15:52 - 00:15:54] So we're going to summarize them.
[00:15:54 - 00:16:01] They kind of said, for the spring calculation, do we have to look up something in a textbook?
[00:16:01 - 00:16:04] Or what is the best way to approach it?
[00:16:04 - 00:16:12] And so in the assignment handout, you'll see that we have had some specifications about what's happening with this spring.
[00:16:12 - 00:16:18] So what kind of displacements and what kind of forces are going to be provided by the spring.
[00:16:18 - 00:16:21] So you'll need to incorporate those into your calculation.
[00:16:21 - 00:16:30] And you don't need to justify any of the values, but you'll just use those to complete some initial calculations.
[00:16:30 - 00:16:36] I'll note here that for your spring, you need to specify what the material was.
[00:16:36 - 00:16:44] So you'll need to do some research there and make sure that whatever calculations you do in terms of the spring steel diameter,
[00:16:44 - 00:16:48] that is an allowable or a standard size.
[00:16:48 - 00:17:00] So there probably be questions asked if you try and say that I'm specifying a spring that's going to be made from a material with a wire diameter of 6.67 millimeters or something.
[00:17:00 - 00:17:06] So generally for the smaller diameters, there'll be an every half millimeter increment.
[00:17:06 - 00:17:15] And then as your spring gets bigger, more likely to be millimeter or five millimeter increments depending on how large we're actually getting, right?
[00:17:15 - 00:17:22] But with that, you'll see that the main equations that you'll need to complete the specification of the spring.
[00:17:22 - 00:17:35] In the handout that we covered a couple weeks ago, and if you want an example to scaffold yourself with, then I would do it very similarly to this kind of work example here.
[00:17:35 - 00:17:46] We use that information about your system to determine what kind of spring constant you need, and then from there, using the equations that have been noted on the page.
[00:17:46 - 00:17:53] I'll create some sort of tabulated, tabulated results.
[00:17:53 - 00:18:01] And you can specify which would be appropriate, noting the spring bound condition.
[00:18:01 - 00:18:09] Question is just on this 1.08.
[00:18:09 - 00:18:11] So we just need one point away.
[00:18:11 - 00:18:20] I think that's varies from 1.03 to 1.08 or something like that, but just make sure your assumption is clear and then goes from there.
[00:18:20 - 00:18:22] Yeah, good.
[00:18:22 - 00:18:25] The other question is you've got a spring.
[00:18:25 - 00:18:27] This is a compression spring.
[00:18:27 - 00:18:33] So what do we have to be concerned or what do we need to check if we have something loaded in compression?
[00:18:33 - 00:18:52] Well, it's a buckling check, and so to do a buckling check which seems quite appropriate for the type of spring we have, I would use or utilize the plot here to work out of our spring is going to be stable or not using these values here.
[00:18:52 - 00:18:59] So we've got a critical value, which is if over L0 over D, and then our relative deflection.
[00:18:59 - 00:19:09] So if you do this and show this unstable, then I'd probably pick one of the columns or the rows in your answers that is stable.
[00:19:09 - 00:19:20] If it was really the last thing that you were doing beforehand and your learning it for last minute, then the theory list should say it's not stable when someone needs to update the calculation, but ideally you would do that piece of work out.
[00:19:20 - 00:19:28] So those were questions that people asked.
[00:19:28 - 00:19:35] So once you've filled out that table, what will we use to summarize what we've done?
[00:19:35 - 00:19:37] This brings specification for them.
[00:19:37 - 00:19:43] So for this here there will be some things that are mandatory, which probably means you'll fill out kind of each of the bits.
[00:19:43 - 00:19:49] One after fill out every single row, but if we want to have enough information here, so that's made.
[00:19:49 - 00:19:52] Some things might be sort of trivial.
[00:19:52 - 00:20:04] For example, in terms of your ends, I think that we don't want to have an open end, but it doesn't really matter if we have closed but not ground or ground and open or ground enclosed.
[00:20:04 - 00:20:15] So there's some things that you'd either say any ground end or we're not really too concerned about that detail.
[00:20:15 - 00:20:21] So that's why we've got these key kind of specifications about the size and the material.
[00:20:21 - 00:20:28] So if it's not possible to kind of indicate, then you can just write an article.
[00:20:28 - 00:20:30] Otherwise you can just approximate things.
[00:20:30 - 00:20:39] So similarly for your operating temperature, if you're to show that it's operating outside and you might give a temperature range, you think it's reasonable for cross-jitch.
[00:20:39 - 00:20:44] Or wherever you think it's going to be here.
[00:20:44 - 00:20:48] So those are the main questions that people would ask about springs.
[00:20:48 - 00:21:03] Has that sparked any other questions that you guys have had as you've been going through your assignment?
[00:21:03 - 00:21:17] So the only other question that I can think of right now that I had written down on my piece of paper that was discussed last time was about fatigue.
[00:21:17 - 00:21:23] So in this assignment, there's a question for you guys. Do you need to design for fatigue?
[00:21:23 - 00:21:26] We see three people checking the head, which is pretty good.
[00:21:26 - 00:21:29] Kind of response rate for the number of people who have in the class.
[00:21:29 - 00:21:31] And that is correct, right?
[00:21:31 - 00:21:35] So in this case here, we're not seeing yet we're designing for fatigue.
[00:21:35 - 00:21:38] We haven't really gone over much detail about fatigue.
[00:21:38 - 00:21:44] But we have mentioned it some week and anyone remember what licks here or when we might have talked about fatigue.
[00:21:44 - 00:21:48] Nature 3, are we good here?
[00:21:48 - 00:21:50] Right at the top of the first time I've been given it out.
[00:21:50 - 00:21:59] But for lecture 3, we did have this mention of the listing house formula, which talks about designing for fatigue.
[00:21:59 - 00:22:07] Now the thing that I need to make really clear is one of the assumptions for this is a concept called infinite life.
[00:22:07 - 00:22:10] Can anyone tell me what infinite life is?
[00:22:10 - 00:22:30] Less means in a very broad way.
[00:22:30 - 00:22:36] Yeah, so basically infinite life means if the stress in the part is smaller than a defined limit.
[00:22:36 - 00:22:38] Now for fatigue limit.
[00:22:38 - 00:22:39] Around drone slum sorry.
[00:22:39 - 00:22:41] Then the part will last forever, right?
[00:22:41 - 00:22:48] Which any material is forced, I would debate whether that's realistic and people who have had hot debates about whether it is or it is in.
[00:22:48 - 00:22:55] And I think the bottom line isn't, but people still sort of use it anyway because it works good enough for the number of socks that we're talking about, right?
[00:22:55 - 00:23:02] But only it's more than 2 million cycles in a like there's a knee in that curve that you discussed.
[00:23:02 - 00:23:06] So I used a sort of weird analogy in the last lecture.
[00:23:06 - 00:23:11] I'll be like it'll be the equivalent of for 3 year olders punching you.
[00:23:11 - 00:23:13] You could probably last it forever.
[00:23:13 - 00:23:21] But in a 5 year old or a 7 year old or a 10 year old, they might be getting kind of stronger and you're only able to last the student.
[00:23:21 - 00:23:25] That's cycles right before you fatigue in your break, right?
[00:23:25 - 00:23:29] If it's like a big person then maybe it's not many at all.
[00:23:29 - 00:23:34] You know if it's like professional blocks or something then it might be pretty low cycles.
[00:23:34 - 00:23:35] That same sort of thing.
[00:23:35 - 00:23:37] And that's what this is assuming.
[00:23:37 - 00:23:43] All that's saying is that if it's going to be safe or fatigue forever, this is the shaft diameter that you need.
[00:23:43 - 00:23:48] This could be an additional check that you do for your shaft diameter calculations.
[00:23:48 - 00:23:53] But if the result is not, I don't know.
[00:23:53 - 00:23:56] If it's not safe or fatigue, do you need to update your design?
[00:23:56 - 00:24:05] I would say no in this instance but I would probably highlight that through the work as needed to make sure that the system is safe for fatigue.
[00:24:05 - 00:24:11] The reason that I'm doing or the reason that I'm saying that is that all the's saying is that it wouldn't be safe for infinite life.
[00:24:11 - 00:24:20] But what is not giving us any information on is actually how many cycles it would be safe for or how many years it would be safe for.
[00:24:20 - 00:24:26] And so to do this you wouldn't need to find out for your material, what the endurance limit is.
[00:24:26 - 00:24:29] Which there are ways to approximate based on the UTS.
[00:24:29 - 00:24:36] It's normally about half the UTS for a steal but that answers that question there.
[00:24:36 - 00:24:49] Any other questions before we move on to looking into our drawings?
[00:24:49 - 00:24:53] So, questions come up.
[00:24:53 - 00:24:55] Don't be shy.
[00:24:55 - 00:24:57] Oh, there's another thing I was going to ask.
[00:24:57 - 00:24:59] So this is our assignment mark sheet.
[00:24:59 - 00:25:03] And what I've talked about is some of the stuff that's happening for our spring.
[00:25:03 - 00:25:08] And we've talked about some of our bearing selection and bearing life calculations.
[00:25:08 - 00:25:11] So that's why it's got the plural there of the new life fuses.
[00:25:11 - 00:25:14] Just the standard alting.
[00:25:14 - 00:25:19] And then make sure that you justify your bearing selection and provide alternatives.
[00:25:19 - 00:25:22] This is kind of what we sort of said there, right?
[00:25:22 - 00:25:27] Oh yeah, if you were asked about the shaft shoulder calculation and the axial load to assume,
[00:25:27 - 00:25:34] what axial load should we assume for our system?
[00:25:34 - 00:25:36] 500 to 1500 newtons is appropriate.
[00:25:36 - 00:25:39] All we're trying to do is make sure that it's not coming apart.
[00:25:39 - 00:25:44] If someone wants to push on it or pull on it, especially when it's assumed to be in transit, right?
[00:25:44 - 00:25:47] Cool.
[00:25:47 - 00:25:50] As long as you make an assumption that should be okay.
[00:25:50 - 00:25:57] Has anyone done the clutch calculations yet?
[00:25:57 - 00:25:58] Cool.
[00:25:58 - 00:26:02] So I'm just going to foreshadow for that thing I foreshadow to the other one.
[00:26:02 - 00:26:06] Whatever result you have, you can then comment on whether the result is reasonable or not.
[00:26:06 - 00:26:12] So in the past, it has been situation where, for example, they did the clutch calculation.
[00:26:12 - 00:26:15] And to get a clutch that didn't.
[00:26:15 - 00:26:21] So to get an actuation force that wasn't above the maximum permissible stress on the clutch,
[00:26:21 - 00:26:24] they needed something like 500 clutch plates, right?
[00:26:24 - 00:26:28] So if that's the result of your calculation, that is okay.
[00:26:28 - 00:26:33] You need to say, okay, to meet the specification, 500 clutch plates would be needed.
[00:26:33 - 00:26:38] But you probably also want to highlight that that's not really an appropriate solution
[00:26:38 - 00:26:42] and that someone should investigate whether this is the type of coupling that's used
[00:26:42 - 00:26:47] or whether a slip coupling or similar is actually better suited, right?
[00:26:47 - 00:26:51] Because a lot of sort of done as a classic in-year, well, clearly,
[00:26:51 - 00:26:54] keyery thing where it's like, oh, yeah, we could definitely use this in this way.
[00:26:54 - 00:26:57] And I guess you guys are going to find out whether we could definitely use it in that way.
[00:26:57 - 00:26:59] But I haven't run the numbers myself this year.
[00:26:59 - 00:27:00] So it might be appropriate.
[00:27:00 - 00:27:05] It might be, yeah, you just need one clutch plate at this material in this force.
[00:27:05 - 00:27:06] That's okay.
[00:27:06 - 00:27:11] But I guess I'll get questions about that once you've got to start kind of working onto it.
[00:27:11 - 00:27:14] Cool.
[00:27:14 - 00:27:23] So with that there, I just want to remind ourselves of our drawing tips that we've been over last term.
[00:27:23 - 00:27:28] And then we'll look at some tips for detail in assembly drawings and we'll be doing, well,
[00:27:28 - 00:27:31] we'll talk about what we need to do for the assignment.
[00:27:31 - 00:27:36] So if you remember, our basics does it look like you have tried.
[00:27:36 - 00:27:41] And when we evaluate some of the other student drawings that I've got pre-prepared,
[00:27:41 - 00:27:48] we'll be able to kind of go through this checklist to see if it looks like those students have, in fact, tried.
[00:27:48 - 00:27:54] So as the title box filled out, every used capital letters is the size and layout appropriate.
[00:27:54 - 00:27:57] I think it's big enough that we can see them clearly.
[00:27:57 - 00:28:04] Do this, like, to view show all of the key details and functionality as our drawing uncluttered and easy to read.
[00:28:04 - 00:28:07] And then our intermediate steps, I suppose,
[00:28:07 - 00:28:13] or the next level of kind of critique is making sure that we've followed the drawing standard.
[00:28:13 - 00:28:17] So other Torrance is appropriate, specifically our sphere.
[00:28:17 - 00:28:26] Specific Torrance is for important parts and an appropriate general Torrance for the types of links that we have in our drawing.
[00:28:26 - 00:28:29] Do the dimensions follow the drawing standard.
[00:28:29 - 00:28:33] Do the select of use, show all of the key details and functionality.
[00:28:33 - 00:28:39] And if they don't, there's the own additional view that could be used to kind of show that.
[00:28:39 - 00:28:44] So we've got access to the drawing standard, which is on the Learn page.
[00:28:44 - 00:28:48] And general, a clear drawing is a really good drawing.
[00:28:48 - 00:28:55] And if in doubt, and you have conflicting ideas around what looks clear and what the drawing standard says,
[00:28:55 - 00:28:58] clarity in my mind, is the winner.
[00:28:58 - 00:29:05] So clarity being cleaned dimensions, reasonable tolerances, and use of notes we're appropriate.
[00:29:05 - 00:29:14] So with the aluminium structure assignment, I think we've probably got some first hand experience where reasonable tolerances help you in manufacturing things,
[00:29:14 - 00:29:22] and make sure that a past quality assurance, quote unquote, before a part goes into do its job.
[00:29:22 - 00:29:38] And that if you had written some things in the notes, especially some of the kind of important things for manufacture or noting what is actually important, then that might as made things go a little bit more smoothly when talking to the Dave's or
[00:29:38 - 00:29:43] Owen or me on the test days.
[00:29:43 - 00:29:49] So where possible, it's helpful to discuss the drawing with the person who'll be making it, which is a good tip.
[00:29:49 - 00:30:05] If you've got a summer job with a workshop and we had many conversations with technicians about tolerances, feel the engineer that you know the design intent, and you will know what dimensions are critical for your design.
[00:30:05 - 00:30:11] And so make sure that you use this information wisely to communicate what you want to communicate.
[00:30:11 - 00:30:19] Otherwise, you might accidentally must communicate stuff that is really difficult to manufacture for is over kind of specified, right?
[00:30:19 - 00:30:28] And so one thing that we've talked about in the past is that because the tyrants or the percentage tyrants kind of changes,
[00:30:28 - 00:30:37] sort of the percentage of the tyrants compared to the length of the dimension changes the specificity of your tyrants.
[00:30:37 - 00:30:45] There are guidelines from ISO 2768, which kind of tell you what reasonable tolerances are for different linear dimensions.
[00:30:45 - 00:30:57] And so depending on what links you have in your drawing, you might want to update your general tolerances to kind of specify some of these, right?
[00:30:57 - 00:31:07] And so if you have a big range of links in your drawing, it's not uncommon to have a table that says basically the same information of this.
[00:31:07 - 00:31:20] For example, four dimensions between six and 30 millimeters, possible minus five is the dimension, but for dimensions of up to 120 possible minus 0.8, right?
[00:31:20 - 00:31:28] So you will see this when it was our aluminium, the thickness of your part is 1.20 ideally, right?
[00:31:28 - 00:31:37] So if we had the general clients of possible minus 0.5 in theory, we could have given you the like the most like whisper thin piece of aluminium,
[00:31:37 - 00:31:40] and you had to make it to it and technically it would have been in specification, right?
[00:31:40 - 00:31:47] Similarly though, for our 400 millimeter plus a minus 0.5, all of a sudden there's actually not very much, right?
[00:31:47 - 00:31:50] So this is what this is, uh, limiting.
[00:31:50 - 00:32:07] And then four out of fits because we're going to have a bearing on our shaft using isotyring and our limits and fits will be useful to specify what an acceptable dimension would be for our shaft diameter.
[00:32:07 - 00:32:16] And so people have covered this before I believe there was a lab on it last year, some people are nodding, but if you've forgotten about it, we have this here.
[00:32:16 - 00:32:21] Do we think we want an interference fit for our bearing and our housing?
[00:32:21 - 00:32:23] We see some shakes over here.
[00:32:23 - 00:32:32] If we have an interference fit, we either need lots of force or some heat, heat and cooling kind of magic to get things to actually go together, right?
[00:32:32 - 00:32:37] Second question, do transition fits exist in reality?
[00:32:37 - 00:32:42] It's not a trick question.
[00:32:42 - 00:32:47] Can you, can you look at a part that's being mowed and say, oh, that's a transition fit?
[00:32:47 - 00:32:52] What do the transition fit mean?
[00:32:52 - 00:33:02] It means depending on the tolerances of your shaft and the tolerances of your say bearing or it might be an interference fit or it might be a clearance fit, right?
[00:33:02 - 00:33:06] But once you actually make the part, it's definitively one or the other, yeah?
[00:33:06 - 00:33:09] So we probably don't really want to transition fit either.
[00:33:09 - 00:33:18] We want some sort of slightly clearance or tight kind of clearance fit to make sure that we can assemble our thing without too much.
[00:33:18 - 00:33:19] Pay.
[00:33:19 - 00:33:20] Yeah.
[00:33:20 - 00:33:22] I will get the idea of how you're doing the engineering fit.
[00:33:22 - 00:33:30] So it's actually got some really good descriptions about the different levels of these kind of clearance fits or interference fits.
[00:33:30 - 00:33:37] I'd sort of broadly call them the different genres of them that it kind of gives examples for what they are used for.
[00:33:37 - 00:33:45] So as you hear some example drawings and just some kind of things that have been highlighted that help the drawing to be clear.
[00:33:45 - 00:33:51] So obviously having a completed title block, clean dimensions where we don't have too many of them overlapping.
[00:33:51 - 00:33:54] We start off with smaller dimensions going to our larger dimensions.
[00:33:54 - 00:34:04] And we've got some notes that kind of help the person manufacturing it to manufacture it as intended and not have to do any guesswork.
[00:34:04 - 00:34:14] So next we've just got a few kind of specialist views that you might use and some of your drawings depending on what kind of information you're wanting to communicate and six views.
[00:34:14 - 00:34:18] So you can see that the
[00:34:18 - 00:34:22] section views are useful if you're wanting to show the internal details of the symbolies with high clarity.
[00:34:22 - 00:34:26] Do not section shafts or fasteners.
[00:34:26 - 00:34:30] Do not section shafts or fasteners.
[00:34:30 - 00:34:33] Do not section shafts or fasteners.
[00:34:33 - 00:34:39] So being told that if I say things like three times, like six in your head a little bit more.
[00:34:39 - 00:34:43] In your drawing you're going to be drawing shafts and fasteners.
[00:34:43 - 00:34:50] And what we'll be looking for is that these are not sectioned because we don't section shafts or fasteners.
[00:34:50 - 00:35:00] Cool. When we are doing sectioning we want to make sure that the cross-hatching is going different directions to signify that the different parts.
[00:35:00 - 00:35:05] And we'll see an example here where the internal details are kind of being shown.
[00:35:05 - 00:35:11] There's a few things here that are a little bit northy on this where we have actually got dimensions inside our part,
[00:35:11 - 00:35:16] which I wouldn't recommend but in this case the designer has thought it was appropriate.
[00:35:16 - 00:35:20] And we also see here what is the symbol here specifying?
[00:35:20 - 00:35:26] Surface finish which might be useful if you're wanting to specify a surface finish for where your sealers,
[00:35:26 - 00:35:31] because if there's not your seal may fail.
[00:35:31 - 00:35:44] What was the... I've got half of it.
[00:35:44 - 00:35:47] I will touch on keyways how you do it.
[00:35:47 - 00:35:50] So it's actually a good question. I'll just maybe I'll answer that as a question.
[00:35:50 - 00:35:56] George, how do you show the keyway if you're not allowed a section of shaft?
[00:35:56 - 00:36:01] And that's where a partial section would be used.
[00:36:01 - 00:36:07] So they call it also a cutaway section, but essentially what you can do is only section the part where you want to show that.
[00:36:07 - 00:36:13] You could, otherwise show that detail in theory, very much in theory, could be to use it in detail.
[00:36:13 - 00:36:17] That's sort of outlawed in the real world, right?
[00:36:17 - 00:36:23] People do not like it. And then you're not allowed to dimension to her in detail.
[00:36:23 - 00:36:26] So you still can't really use it in a useful way.
[00:36:26 - 00:36:31] So using cutaway section would be a useful way to show your keyway.
[00:36:31 - 00:36:35] And then just quickly we have some information here.
[00:36:35 - 00:36:38] So the previous one here was talking about detailed views.
[00:36:38 - 00:36:41] So I think some people learn this about the menu structure,
[00:36:41 - 00:36:45] but there's a lot of things that are really small and hard to give details on.
[00:36:45 - 00:36:49] That's when you'd want to use a detailed view like this view here,
[00:36:49 - 00:36:57] where you can actually see some more intricate detail exploded and zoomed in to show the specifics.
[00:36:57 - 00:37:03] And then for you're assembly, just remember that you're allowed to shrink the bill of materials.
[00:37:03 - 00:37:08] Color is often not useful in not used to make it harder to interpret.
[00:37:08 - 00:37:12] I don't expose your parts if it's really needed.
[00:37:12 - 00:37:15] That's dimly from looking at your assembly,
[00:37:15 - 00:37:18] we should be able to see how your thing kind of goes together.
[00:37:18 - 00:37:22] And we saw that with some of the end earring,
[00:37:22 - 00:37:26] or the end details of bearings in the lecture this morning,
[00:37:26 - 00:37:30] we're able to sort of see that detail and we'll see that.
[00:37:30 - 00:37:32] We'll go through some drawings now.
[00:37:32 - 00:37:37] Overall you would provide some important overall dimensions or critical dimensions.
[00:37:37 - 00:37:40] For your part to hear we see an example,
[00:37:40 - 00:37:44] I'll have an assembly drawing just for completeness.
[00:37:44 - 00:37:48] Because we've got about 13 minutes,
[00:37:48 - 00:37:52] I think it's about time that we look at some drawings,
[00:37:52 - 00:38:00] and we check whether we think they have been done to a high quality or not.
[00:38:00 - 00:38:06] So for each of these I'll give you a brief amount of time before we can do that.
[00:38:06 - 00:38:11] For the whole time before we can start opening the floor to what was done well
[00:38:11 - 00:38:14] and what was not done well.
[00:38:14 - 00:38:24] So all of these are like student examples of bearing housings.
[00:38:24 - 00:38:29] I have shown once to highlight a couple things.
[00:38:29 - 00:38:36] So the bubbles are tidy, yeah okay.
[00:38:36 - 00:38:40] So I'm just going to write around and take care for the bubbles.
[00:38:40 - 00:38:41] Cool, what else is good?
[00:38:41 - 00:38:47] The shaft is not sectioned, that's good.
[00:38:47 - 00:38:55] What else is the cross sectioned good?
[00:38:55 - 00:39:03] Ah, yeah, so the cross sectioning there,
[00:39:03 - 00:39:06] this makes it a little bit unclear because it's like,
[00:39:06 - 00:39:10] is this two individual bearings or is it one double,
[00:39:10 - 00:39:13] ball, double row ball bearing, right?
[00:39:13 - 00:39:19] But otherwise, like generally these ones are quite clear that you can tell that these things are different parts, right?
[00:39:19 - 00:39:20] Cool.
[00:39:20 - 00:39:24] And so on that, this is a common thing that I think I've mentioned.
[00:39:24 - 00:39:28] Where I suspect what has happened is the student did the bearing life calculation,
[00:39:28 - 00:39:30] the bearing life calculation was like,
[00:39:30 - 00:39:32] yeah, your bearing's not strong enough.
[00:39:32 - 00:39:36] And they're like, that's DJ Khaled, another one.
[00:39:36 - 00:39:44] And it doesn't really work like that because now we've incorporated having two bearings in the system,
[00:39:44 - 00:39:46] basically, means we've got like two pin joints here.
[00:39:46 - 00:39:51] And the assumption might be that both of these bearings really sheer
[00:39:51 - 00:39:54] are though nice and equally, and it's nice.
[00:39:54 - 00:39:59] But really what I've done has made the system difficult to determine or aesthetically
[00:39:59 - 00:40:03] indeterminate depending on what's happening on the other side,
[00:40:03 - 00:40:08] which is, you know, apparently these two bearings which are sharing both the
[00:40:08 - 00:40:10] axial and the radial forces at this point.
[00:40:10 - 00:40:15] So, if your bearing's not for life,
[00:40:15 - 00:40:19] take a bigger bearing rather than pickin' two.
[00:40:19 - 00:40:20] Cool.
[00:40:20 - 00:40:22] Any other comments that we wanna make about this one?
[00:40:22 - 00:40:26] So we can see here that we've got our partial section to kind of show the key way.
[00:40:26 - 00:40:29] We've got a couple dimensions on it.
[00:40:29 - 00:40:34] You can't really see them, but those would be useful to kind of add.
[00:40:34 - 00:40:36] Is there any rubbing on the part?
[00:40:36 - 00:40:43] Or any parts that are rubbing?
[00:40:43 - 00:40:47] So obviously our shaft is rotating, and this part of our bearing is rotating,
[00:40:47 - 00:40:51] and that should hopefully not be touching anything that is not rotating.
[00:40:51 - 00:40:53] So you can see we've got a gap there,
[00:40:53 - 00:40:57] and a gap there, and our seals are fine.
[00:40:57 - 00:41:00] The lip of the seal will be touching the shaft, which is what we want.
[00:41:00 - 00:41:05] And we can actually, we can get that shell or the seal installed relatively easily.
[00:41:05 - 00:41:08] Other thing we can do is if we look at our axial restraint,
[00:41:08 - 00:41:11] we started having good examples of this.
[00:41:11 - 00:41:15] Is it actually restrained in this direction if I push on the shaft?
[00:41:15 - 00:41:16] Yep.
[00:41:16 - 00:41:21] So if we go through here or we'd go through one slash both of the bearings
[00:41:21 - 00:41:24] into this part here, through this fastener,
[00:41:24 - 00:41:27] and through that fastener into our plate track.
[00:41:27 - 00:41:34] And we're assuming that that plate is rigidly connected and perpendicular to our shaft track.
[00:41:34 - 00:41:35] Cool.
[00:41:35 - 00:41:38] If we push it on the other direction though, is it actually restrained?
[00:41:38 - 00:41:53] So if we push on the shaft, all will happen.
[00:41:53 - 00:41:54] It's not restrained right.
[00:41:54 - 00:42:02] So this has no circular for a lock nut or anything to hold the bearing racing.
[00:42:02 - 00:42:06] Basically the whole shaft will just move to no ideal.
[00:42:06 - 00:42:15] And then eventually this key where we'll probably hit this and, you know, bad things will happen.
[00:42:15 - 00:42:17] Any other questions or comments about this?
[00:42:17 - 00:42:20] Those were the main points that I wanted to make.
[00:42:20 - 00:42:23] So we'll look at another...
[00:42:23 - 00:42:26] Look at this one.
[00:42:26 - 00:42:38] So what is either good or not so good?
[00:42:38 - 00:42:41] So the dimensions are bad right?
[00:42:41 - 00:42:44] So if we're not following the drawing standard in multiple ways,
[00:42:44 - 00:42:46] they're not the orientation.
[00:42:46 - 00:42:48] They're also saying millimeters and stuff.
[00:42:48 - 00:42:50] So maybe it was a bit of a last minute job.
[00:42:50 - 00:42:52] We'll probably see some bits of that.
[00:42:52 - 00:42:55] Things like this, you know, naughty.
[00:42:55 - 00:42:59] What else is either good or not so good?
[00:42:59 - 00:43:03] Have they six in the shaft?
[00:43:03 - 00:43:10] Well, you can hand up if you're looking yellow.
[00:43:10 - 00:43:12] Six in the shaft.
[00:43:12 - 00:43:14] Hands up if you're looking to heaven.
[00:43:14 - 00:43:15] I go, go with them.
[00:43:15 - 00:43:16] They have burnt.
[00:43:16 - 00:43:21] So the telltale sign is normally this shoulder here, right?
[00:43:21 - 00:43:26] So it wasn't section, then we would see a line across that edge.
[00:43:26 - 00:43:28] Do you want to agree with that?
[00:43:28 - 00:43:30] So that's sectioned.
[00:43:30 - 00:43:32] And then I think that this is actually meant to be thread.
[00:43:32 - 00:43:35] And similarly you would actually see the thread because it's like a...
[00:43:35 - 00:43:37] If it was a cat drawing, right?
[00:43:37 - 00:43:40] So they have sectioned it.
[00:43:40 - 00:43:41] That's not good.
[00:43:41 - 00:43:46] With the bearing, have they done a good job of the bearing details?
[00:43:46 - 00:43:49] You see a lot of shacks of the head.
[00:43:49 - 00:43:52] So we would want to see what is the bearing detail,
[00:43:52 - 00:43:56] what kind of bearing do you have so that we can check whether the part is rubbing, right?
[00:43:56 - 00:43:57] So I've drawn that in there.
[00:43:57 - 00:43:59] Is the ear rubbing on this part?
[00:43:59 - 00:44:02] Yes.
[00:44:02 - 00:44:09] Yes, so we've got...
[00:44:09 - 00:44:12] So this bit of stationary, this bit of stationary.
[00:44:12 - 00:44:15] But this bit is moving and this bit is stationary.
[00:44:15 - 00:44:19] So we've got some rubbing, major rubbing happening there.
[00:44:19 - 00:44:22] And then on this side here, this bit is rotating.
[00:44:22 - 00:44:23] This bit is stationary.
[00:44:23 - 00:44:25] So we've got rubbing there.
[00:44:25 - 00:44:27] Then this is the real fun bit.
[00:44:27 - 00:44:30] If we push on the shaft, what happens?
[00:44:30 - 00:44:40] Then if we push on the shaft, basically it's just going to push our shaft into
[00:44:40 - 00:44:41] our housing.
[00:44:41 - 00:44:43] We've got more rubbing, right?
[00:44:43 - 00:44:51] So these are the kind of things for a workable design that we want you to do appropriately.
[00:44:51 - 00:44:54] We've talked about things like cross-heaching.
[00:44:54 - 00:44:58] Cross-heaching could probably be made clearer in this instance.
[00:44:58 - 00:45:02] But in the sake of time, I'm going to move us on to the next one,
[00:45:02 - 00:45:05] which is our more recent student drawing.
[00:45:05 - 00:45:10] And we can go through our checklist of, does it look like they have tried?
[00:45:10 - 00:45:13] So to start with, what would we...
[00:45:13 - 00:45:16] Will you mark it in the more, do we be thinking?
[00:45:16 - 00:45:17] No tolerances.
[00:45:17 - 00:45:19] No tolerances, okay?
[00:45:19 - 00:45:22] So this needs to be filled out.
[00:45:22 - 00:45:23] Right?
[00:45:23 - 00:45:25] What else needs to be filled out?
[00:45:25 - 00:45:27] Fill out the title block?
[00:45:27 - 00:45:28] Yep.
[00:45:28 - 00:45:30] I'll just say that as well.
[00:45:30 - 00:45:31] Fill out.
[00:45:31 - 00:45:32] Cool.
[00:45:32 - 00:45:34] They've used capital letters on their title block, which is good.
[00:45:34 - 00:45:37] Have they used capital letters elsewhere?
[00:45:37 - 00:45:46] So what would we say could be improved in their bill of materials?
[00:45:46 - 00:45:47] Capital letters?
[00:45:47 - 00:45:49] Cool.
[00:45:49 - 00:45:50] What else could be improved?
[00:45:50 - 00:45:53] Yep.
[00:45:53 - 00:45:55] So it would be probably nicer if the...
[00:45:55 - 00:45:57] The amount of materials come to you up.
[00:45:57 - 00:46:00] This amount of space, and then we could actually make this drawing view
[00:46:00 - 00:46:01] a bunch bigger, right?
[00:46:01 - 00:46:03] Because it's kind of sort of crammed on the side.
[00:46:03 - 00:46:04] Cool.
[00:46:04 - 00:46:09] Now, what if this bill of materials do we explicitly need each column?
[00:46:09 - 00:46:19] Which I don't know why, but that works for me way more than it should.
[00:46:19 - 00:46:23] Because part number, part number should be like, if I've used...
[00:46:23 - 00:46:24] I don't know.
[00:46:24 - 00:46:26] A classic SKF bearing.
[00:46:26 - 00:46:27] Like if it was...
[00:46:27 - 00:46:28] I don't know.
[00:46:28 - 00:46:31] One of my personal favourites, WB2001Z.
[00:46:31 - 00:46:32] You know?
[00:46:32 - 00:46:36] I can't remember if that's a shield or a sealed bearing, right?
[00:46:36 - 00:46:39] But that would be a part number that you would put in this bit here, right?
[00:46:39 - 00:46:43] But the classic that I see is people doing this.
[00:46:43 - 00:46:47] It's part number is coupling and its description is model coupling.
[00:46:47 - 00:46:53] I'm not here to critique what it is, but if it's not a part number,
[00:46:53 - 00:46:57] we could delete that whole kind of column and just say the description, right?
[00:46:57 - 00:47:04] And then they would make a more concise and they would make it clearer and would have more space instantly for making out other views bigger.
[00:47:04 - 00:47:07] But if you do want to have the part number, that's all good.
[00:47:07 - 00:47:09] Only fill out the part numbers.
[00:47:09 - 00:47:18] Well, if the part numbers that are actually, you know, standard parts that will have a number that a manufacturer has given you.
[00:47:18 - 00:47:20] Cool.
[00:47:20 - 00:47:25] If we're looking at our actual drawing views, what is good and what is not so good?
[00:47:25 - 00:47:30] Not sectioned.
[00:47:30 - 00:47:32] So I'll take this, but here I guess.
[00:47:32 - 00:47:34] Yeah.
[00:47:34 - 00:47:40] Yeah.
[00:47:40 - 00:47:42] It's saying slightly weird's gone on there as well, but I'll give it a take for now.
[00:47:42 - 00:47:48] Looks like they've drawn on the tangent edge, but we'll let it go.
[00:47:48 - 00:47:52] But yeah, the key way is not the key way to do the part full section, right?
[00:47:52 - 00:47:54] That'll be better.
[00:47:54 - 00:47:55] Cool.
[00:47:55 - 00:47:57] What else is good or not so good?
[00:47:57 - 00:48:00] Yep.
[00:48:00 - 00:48:01] Cross-section is good.
[00:48:01 - 00:48:02] Is there any rubbing?
[00:48:02 - 00:48:12] I'll zoom in so you can see maybe any rubbing.
[00:48:12 - 00:48:14] I think it's okay, right.
[00:48:14 - 00:48:18] There's this thing here, but that's a dust seal, which is meant to be touching.
[00:48:18 - 00:48:20] Everything else has a gap.
[00:48:20 - 00:48:22] We can see the bearing detail.
[00:48:22 - 00:48:25] Is it actually restrained in both directions?
[00:48:25 - 00:48:27] So we push on this one.
[00:48:27 - 00:48:31] It's going to go through here, then into there and into there, which is probably all good.
[00:48:31 - 00:48:35] If we push on this direction, there's nothing stopping our shaft.
[00:48:35 - 00:48:37] So it's not on that direction, right?
[00:48:37 - 00:48:43] So that's where we would want to make sure it is actually restrained in both directions.
[00:48:43 - 00:48:51] Other points, just for completeness, because I want to quickly go through another one,
[00:48:51 - 00:49:00] as surface conditions would be useful to make sure that our seals are going to last a reasonable amount of time, right?
[00:49:00 - 00:49:07] Now, just seals.
[00:49:07 - 00:49:11] The main thing with your seals, do you need to actually leave Australian seals in both directions?
[00:49:11 - 00:49:17] No, and you need to leave them open on one edge, if it's an individual, one single part.
[00:49:17 - 00:49:21] Just to make sure that you can actually get the seal in there and install properly, right?
[00:49:21 - 00:49:27] So it's a really good point, but sometimes I've seen, for example, a shaft that looks like this.
[00:49:27 - 00:49:31] And apparently you'll need to get a bearing to sit into this little bit here, right?
[00:49:31 - 00:49:34] And there's actually Australian-based directions, I think, as the thought process, you know?
[00:49:34 - 00:49:37] But it's like, how do you magic that in there?
[00:49:37 - 00:49:43] The same kind of thing for the seal, if you had your seal in a characteristic looking like that,
[00:49:43 - 00:49:47] then it's kind of impossible to get the seal in there without damaging it.
[00:49:47 - 00:49:55] So we can get the seal just again.
[00:49:55 - 00:49:58] We've got not much time. Five seconds.
[00:49:58 - 00:50:04] So maybe we have to leave it there, but I guess what I'm trying to say with this one,
[00:50:04 - 00:50:09] we can't really see it, just really quickly, similar kind of things that are happening.
[00:50:09 - 00:50:14] For a vision's table, full or complete. Make sure that the title block is filled out.
[00:50:14 - 00:50:17] We don't have any dimensions on this.
[00:50:17 - 00:50:23] The cross-hatching is average, but we actually see what we were just talking about as a bad example.
[00:50:23 - 00:50:28] So we sort of already talked about it, for folks'.
[00:50:28 - 00:50:34] So that seal you wouldn't really be able to get in there, but they've done some things that are kind of good where we have
[00:50:34 - 00:50:41] just locating spaghetti as what they would call it, where you can actually slot your housing into it.
[00:50:41 - 00:50:44] So that's all we've got time on.
[00:50:44 - 00:50:50] If you want to see the points that I talked about last time, all we really did was talk about these things here.
[00:50:50 - 00:50:56] So using capitals, improving the size, making exactly the Australian-both direction,
[00:50:56 - 00:51:03] add the important dimensions because there's no dimensions, making sure the surface condition has been noted.
[00:51:03 - 00:51:05] I don't see that.
[00:51:05 - 00:51:09] We'll see that. Leave that one there for now.
[00:51:09 - 00:51:12] If you have any questions, then I'll be hanging around.
[00:51:12 - 00:51:15] That thing that next class is ready, so we must do those outside.
[00:51:15 - 00:51:26] So you're just one drawing here.
[00:51:26 - 00:51:31] One like, that's a good example of drawing with expect.
[00:51:31 - 00:51:35] Okay.
[00:51:35 - 00:51:37] Hopefully the sharp bone.
[00:51:37 - 00:51:43] And if we want to add any shoulders or the resistance for the surface guide,
[00:51:43 - 00:51:48] this is the diameter that we've covered, perhaps the minimum diameter,
[00:51:48 - 00:51:52] in which case we make everything larger than that.
[00:51:52 - 00:51:53] Yep.
[00:51:53 - 00:51:55] But your...
[00:51:55 - 00:52:00] The answer to the answer is yes, and then when you do your first principle check or reality check,
[00:52:00 - 00:52:03] the turn of reality check, and that will kind of show,
[00:52:03 - 00:52:08] because like your minimum shaft diameter calculation has not assumed,
[00:52:08 - 00:52:13] like there is a stress concentration, or it doesn't tell you what the factor of safety is.
[00:52:13 - 00:52:17] But there is a factor of safety in that calculation.
[00:52:17 - 00:52:21] So when you do that reality check there, we'll answer your question.
[00:52:21 - 00:52:22] Yeah.
[00:52:22 - 00:52:29] I'm just wondering, because if we do have the collect shoulders and the surface groups,
[00:52:29 - 00:52:33] the actual sharp diameter is going to be actually way overkill.
[00:52:33 - 00:52:35] And is that what you're saying?
[00:52:35 - 00:52:42] When you do the alternative reality check, you'll be able to know if it is way overkill or not.
[00:52:42 - 00:52:48] So your minimum shaft diameter calculation has a factor of safety in that.
[00:52:48 - 00:52:50] Yeah.
[00:52:50 - 00:52:53] So generally speaking though, what we've said for like things like keyways,
[00:52:53 - 00:52:59] the shortcut method is to then increase your shaft diameter by 25% or something like that.
[00:52:59 - 00:53:03] And then when you do your alternative reality check, that will show you,
[00:53:03 - 00:53:07] have I increased it enough or not.
[00:53:07 - 00:53:08] Okay.
[00:53:08 - 00:53:14] But often where you're saying when you're bearing is,
[00:53:14 - 00:53:17] the moment going through the shaft is,
[00:53:17 - 00:53:21] by actually in this case, the moment will still be there for a second moment.
[00:53:21 - 00:53:23] I don't know how to do this.
[00:53:23 - 00:53:25] I'm going to have to go to the left.
[00:53:25 - 00:53:31] No, I mean, so like, all I say is, maybe make sure that it's way overkill or something.
[00:54:52 - 00:54:54] So I'm going to go to the left.

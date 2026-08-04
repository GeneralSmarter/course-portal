# ENMT301-26W Lecture 05 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `49d72e2ef9cbff249ed70875057d3b60b0b0ea418e773111c74811ebafdf23fd`
Generated: 2026-06-06T05:00:16.948980+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:03 - 00:00:19] Okay, should we make a start? Pop quiz? Let's see if it works. What's the answer?
[00:00:19 - 00:00:23] I'll be guessing I don't know either, but this was on here when I walked in.
[00:00:23 - 00:00:30] Maybe D? Why have you done Campbell? Who knows?
[00:00:30 - 00:00:36] I don't know.
[00:00:36 - 00:00:42] Yeah, yeah, wow. Yeah, it could be his first exit ever.
[00:00:42 - 00:00:46] Very good. We'll go back to our staff.
[00:00:46 - 00:00:50] If I can make it all out.
[00:00:50 - 00:01:00] Okay, just a quick note before this lecture.
[00:01:00 - 00:01:06] Nice to mention to me yesterday that she wasn't a part of the third year
[00:01:06 - 00:01:11] Tron 2026 group on the Tron student page and if all could vote in the classroom.
[00:01:11 - 00:01:15] Anyway, so I looked into that and it turned out I guess
[00:01:15 - 00:01:19] when Tonya set up that group some of you hadn't finished enrolling.
[00:01:19 - 00:01:24] There are about 20 of you who didn't have access to that, but that's been updated now.
[00:01:24 - 00:01:29] If you found that in the past now, if you go back to the Tron student page, you're part of that.
[00:01:29 - 00:01:31] So you should be fine.
[00:01:31 - 00:01:35] The three of one of the classrooms for 2026 did not work.
[00:01:35 - 00:01:37] The open-source was four years.
[00:01:37 - 00:01:47] There are two more questions, but it would be a little touch for you.
[00:01:47 - 00:01:49] Okay, I'll check into that.
[00:01:49 - 00:01:50] I must have just...
[00:01:50 - 00:01:52] That would have been last year's one.
[00:01:52 - 00:02:00] The ENMT 301 page.
[00:02:00 - 00:02:03] I get you to know, I don't know why that's there.
[00:02:03 - 00:02:04] I will delete that.
[00:02:04 - 00:02:08] The one that you should go to is the one that's on the Megatron at students page.
[00:02:08 - 00:02:13] I definitely had one and tested one that's got students from this class,
[00:02:13 - 00:02:15] but there might have been another one left up.
[00:02:15 - 00:02:18] So if you see it in their fourth years and you think what on this go on,
[00:02:18 - 00:02:22] go to the Tron student page and that should work.
[00:02:22 - 00:02:29] We used AI to help generate that because if I need to make that quiz,
[00:02:29 - 00:02:32] because there was seven nominees this year and you had three votes,
[00:02:32 - 00:02:35] there's like 15 combinations of how it can be answered.
[00:02:35 - 00:02:41] And so, the board was very helpful in generating the associated XML file
[00:02:41 - 00:02:44] that worked out for the work it's called for.
[00:02:44 - 00:02:49] Well, they're technically, I should take ownership for that.
[00:02:49 - 00:02:51] Any other questions before we start?
[00:02:51 - 00:02:54] Somebody emailed me just before asking about this workshop this afternoon.
[00:02:54 - 00:02:56] That's a door to still well questions,
[00:02:56 - 00:02:59] so if you're not sure about that, you know, George, not me.
[00:02:59 - 00:03:00] Okay.
[00:03:00 - 00:03:02] Otherwise, yeah.
[00:03:02 - 00:03:04] Anything else?
[00:03:04 - 00:03:07] No.
[00:03:07 - 00:03:09] Okay, cool.
[00:03:09 - 00:03:11] So today we're going to talk about requirements.
[00:03:11 - 00:03:18] And reality, it should be a recap because I guess an ensuring 101 and probably last year
[00:03:18 - 00:03:23] an M T 221, you did a little bit about engineering requirements, right?
[00:03:23 - 00:03:27] It's not the first time I've heard this thing requirement.
[00:03:27 - 00:03:30] And so this is a bit of a recap about that.
[00:03:30 - 00:03:37] I'm probably going to try and make this a bit more discussion-y.
[00:03:37 - 00:03:43] So there's these lecture notes here and they're available on the NCO01 page.
[00:03:43 - 00:03:46] And so have a look through them in your own time.
[00:03:46 - 00:03:52] We might probably go through a few of them now, depending on how time goes.
[00:03:52 - 00:03:56] But if we don't look through them yourself, like the pre-self explanatory,
[00:03:56 - 00:04:00] if we don't get through all of this, will the lecture material, okay?
[00:04:00 - 00:04:03] Because it's probably better to have a bit of a discussion around what requirements are,
[00:04:03 - 00:04:09] what the requirements aren't and your experience with them and things like that.
[00:04:09 - 00:04:19] So with this, here's a couple of statements in a very at-do-book cartoon about requirements.
[00:04:19 - 00:04:24] And requirements come from, we know we're talking about this yesterday in the lecture.
[00:04:24 - 00:04:29] What is engineering design and someone who's up the front said, you know,
[00:04:29 - 00:04:33] solving a problem and therefore you have to define the problem, right?
[00:04:33 - 00:04:43] And so how do requirements fit into defining this problem that we're trying to solve?
[00:04:43 - 00:04:44] Yep.
[00:04:44 - 00:04:53] Yeah, I suppose so. I guess we'll get to a bit more detail around that.
[00:04:53 - 00:04:57] But broadly, what are we using requirements for?
[00:04:57 - 00:04:59] What are they doing?
[00:04:59 - 00:05:01] Yeah, outlining the problem, right?
[00:05:01 - 00:05:08] If we have a problem and there's a good sort of design,
[00:05:08 - 00:05:13] it's not really an analogy, a story about designing a bit of mouse track
[00:05:13 - 00:05:16] and I think you'll find it on Wikipedia.
[00:05:16 - 00:05:23] But somebody wants a bit of mouse track, because obviously mice are a problem.
[00:05:23 - 00:05:25] What is the problem that we're trying to solve?
[00:05:25 - 00:05:32] Catching mice?
[00:05:32 - 00:05:34] That would make sense.
[00:05:34 - 00:05:38] But is that really the problem that we're trying to solve potentially?
[00:05:38 - 00:05:41] This is what does to make you sort of think about this.
[00:05:41 - 00:05:43] Is it that we want to catch mice?
[00:05:43 - 00:05:47] I mean, if we wanted to catch mice to deep fry them or something,
[00:05:47 - 00:05:51] you absolutely would probably need a bit of mouse track to do that.
[00:05:51 - 00:05:55] But why might we want to be catching mice?
[00:05:55 - 00:05:56] To remove them, right?
[00:05:56 - 00:06:01] They might be eating, I don't know, the grain that you've got stored on your farm or something to that effect, right?
[00:06:01 - 00:06:08] So we really want to remove mice, but is a mouse track the only way to do that?
[00:06:08 - 00:06:11] No, what else could we use?
[00:06:11 - 00:06:12] So I poisoned your poison.
[00:06:12 - 00:06:13] I finished it.
[00:06:13 - 00:06:14] I posted it.
[00:06:14 - 00:06:15] I just...
[00:06:15 - 00:06:19] I mean, which is a colloquial way of saying you can't.
[00:06:19 - 00:06:20] Yes.
[00:06:20 - 00:06:23] You could have a cat that will keep the mice away.
[00:06:23 - 00:06:26] Probably the smell of a cat will keep the mice away.
[00:06:26 - 00:06:30] But poison will also do it, absolutely.
[00:06:30 - 00:06:36] And that comes down to defining the problem, because if you kind of jump to that initially,
[00:06:36 - 00:06:39] we jump to that, oh, we need to bit of mouse track.
[00:06:39 - 00:06:52] It might be absolutely like just ignoring a whole bunch of possible solutions which might be better or more cheaply or otherwise salt the problem, right?
[00:06:52 - 00:07:03] So we need to discuss or define these requirements, because is the requirement to catch more mice?
[00:07:03 - 00:07:06] That's the situation dependent, right?
[00:07:06 - 00:07:11] What might the requirement really do?
[00:07:11 - 00:07:19] It could be something like the increased grain of production or to reduce the impact of mice on grain production or something to that effect, right?
[00:07:19 - 00:07:20] And so that...
[00:07:20 - 00:07:27] What are we doing when we kind of open that up?
[00:07:27 - 00:07:28] Yeah.
[00:07:28 - 00:07:30] We're a bit more to flip that on its head.
[00:07:30 - 00:07:32] We're not constraining the design space.
[00:07:32 - 00:07:38] We're not saying it's got to be a mouse track because we've already constrained that quite heavily when we say that.
[00:07:38 - 00:07:44] We've opened that up and there are other avenues that we can explore like cats and poison and I don't know something else.
[00:07:44 - 00:07:47] We haven't thought about trapping and relocating.
[00:07:47 - 00:07:50] Do you know this file?
[00:07:50 - 00:07:52] Sun to that effect.
[00:07:52 - 00:08:02] So requirements are a really important part of design because that's kind of the first thing you do.
[00:08:02 - 00:08:12] Once you've obviously decided that you're going down this design avenue, like if a client comes to you in the future or you've come up with a project,
[00:08:12 - 00:08:22] you'll normally have to start thinking about what it is that you want to design the way you want to do it and that comes into a requirement specification or specifying the requirements.
[00:08:22 - 00:08:27] And that's where these quotes here kind of come in.
[00:08:27 - 00:08:31] And elegant solutions to the wrong problem is less than worthless.
[00:08:31 - 00:08:34] It is less than worthless to the person who has that problem.
[00:08:34 - 00:08:41] You might have invented something that's amazing for some other problem, which is fine.
[00:08:41 - 00:08:48] But who was a systems engineer at the University of Arizona.
[00:08:48 - 00:08:53] Dan Rome was here to book about visual problem solving.
[00:08:53 - 00:08:56] They're also there quite a bit of a best describes a problem.
[00:08:56 - 00:08:59] Who's the one that's most likely to solve it?
[00:08:59 - 00:09:05] If you best describe the problem, what does that mean for your design?
[00:09:05 - 00:09:16] Yeah, you've got a better understanding of it and things like the constraints and stuff like that about what you're trying to solve.
[00:09:16 - 00:09:19] And therefore, opens you up to other solutions.
[00:09:19 - 00:09:31] So going back to that mouse trap idea, if you just describe the problem in terms of a mouse trap, you're already running down this one avenue,
[00:09:31 - 00:09:44] where it's just getting a cat might solve the problem for you and see you may solve it in a more cost-effective manner, for example.
[00:09:44 - 00:09:52] And the deal with culture, and if you haven't read that, that's just straight on the nose really.
[00:09:52 - 00:09:54] So, right.
[00:09:54 - 00:10:02] So, with that, and I think this came up yesterday.
[00:10:02 - 00:10:10] Because this is called requirement specification, and then people come into the idea of what is it a requirement?
[00:10:10 - 00:10:14] Is it a specification? Is it specifying the requirement?
[00:10:14 - 00:10:16] Is it what is it?
[00:10:16 - 00:10:21] So, who's got some ideas on what the differences between requirements and specifications are?
[00:10:21 - 00:10:28] Are there differences between the more like they, for example,
[00:10:28 - 00:10:33] you want to be smaller or especially be like exact numbers that you want to have?
[00:10:33 - 00:10:35] That's not a bad answer.
[00:10:35 - 00:10:36] Yeah?
[00:10:36 - 00:10:41] The final thing about what it has to do is, is it patience and what we can to make it?
[00:10:41 - 00:10:44] That's also a pretty good answer, yeah?
[00:10:44 - 00:10:47] I mean, I guess there's no right answer to this.
[00:10:47 - 00:10:51] So, it's interesting to hear what you think from your experiences in my house going out of you.
[00:10:51 - 00:10:54] Is it a part of the specification?
[00:10:54 - 00:10:58] Yeah, I mean, very also very similar to what these guys have said, yes.
[00:10:58 - 00:11:02] So that comes down to the detail level of it.
[00:11:02 - 00:11:08] And also, yes, it's getting honestly right track.
[00:11:08 - 00:11:11] Yeah, the options.
[00:11:11 - 00:11:13] Yeah?
[00:11:13 - 00:11:17] I guess in like the business, like a requirement of these,
[00:11:17 - 00:11:21] some of the requirements are too far, but is it the definition of the environment that you can do?
[00:11:21 - 00:11:23] Yeah, so that's a pretty good answer as well.
[00:11:23 - 00:11:26] So, requirements are more in customer speak,
[00:11:26 - 00:11:30] whereas specifications are more in internal engineering or anything.
[00:11:30 - 00:11:35] To have a story about that, I had a PhD student who I co-supervised,
[00:11:35 - 00:11:37] Rachael and him, he finished to come easier.
[00:11:37 - 00:11:41] Before he came into this PhD, he did a Megatron's like you here,
[00:11:41 - 00:11:46] but he went and worked for Fisher and Pico, a client as first.
[00:11:46 - 00:11:52] And at one point they were working on one of the new oven units.
[00:11:52 - 00:11:59] And I guess the marketing people said that they wanted the buttons to have pop.
[00:11:59 - 00:12:04] From an engineering to, like, it was like, what the hell is pop?
[00:12:04 - 00:12:06] Like, how do we define this?
[00:12:06 - 00:12:09] What is it from a, you know, the marketing people do that wanted that?
[00:12:09 - 00:12:13] It felt popular or whatever, but from an engineering sort of view,
[00:12:13 - 00:12:15] sort of thing. How do you define that?
[00:12:15 - 00:12:19] What is it? How can you verify that buttons got pop?
[00:12:19 - 00:12:24] You know, how do you know you've achieved that design requirement?
[00:12:24 - 00:12:29] And so definitely there's this sort of attention between the customer speak
[00:12:29 - 00:12:34] or if you like the marketing speak and the engineering speak with this.
[00:12:34 - 00:12:37] So this is something that has always,
[00:12:37 - 00:12:40] the ever since I started teaching this part of the course,
[00:12:40 - 00:12:44] there's never a settle on a good answer for it.
[00:12:44 - 00:12:48] And every year I kind of flick back through and I think how should I do this?
[00:12:48 - 00:12:53] So this morning before this, I thought I'd have a conversation with chat GPT about the difference.
[00:12:53 - 00:12:56] There was quite a line there.
[00:12:56 - 00:13:00] And so I shared that with you and we can discuss some aspects of that.
[00:13:00 - 00:13:03] Because, and this I think is, I mean,
[00:13:03 - 00:13:09] some of you, you possibly really use AI in this way.
[00:13:09 - 00:13:12] And if you don't, you should certainly,
[00:13:12 - 00:13:15] and it's not, this is not particularly sophisticated,
[00:13:15 - 00:13:20] but in doing this, this is how we at university want to use AI.
[00:13:20 - 00:13:22] We don't want you to say, hey, right,
[00:13:22 - 00:13:29] you control the report about a single car driven by a DC mode and explain what happened.
[00:13:29 - 00:13:34] What we want is you to use it to kind of pull together a lot of information
[00:13:34 - 00:13:39] and synthesize it into a way that's enlightening for you and summarise its data.
[00:13:39 - 00:13:45] So what I asked at this morning, I said in the context of making fun of systems on what's the difference between requirements and specifications,
[00:13:45 - 00:13:47] which I think was fair enough.
[00:13:47 - 00:13:52] Now, this came up with some, pretty much,
[00:13:52 - 00:13:55] some of the answers that you guys have just come up with.
[00:13:55 - 00:13:58] The first thing at the top is a requirement is what the system must achieve,
[00:13:58 - 00:14:02] pretty poorly defined, the specification is how well it must achieve it.
[00:14:02 - 00:14:04] And that's with measurable detail.
[00:14:04 - 00:14:07] So just to give you a heads up,
[00:14:07 - 00:14:12] my personal thinking about this before I did this was that,
[00:14:12 - 00:14:16] which one of you see it, is requirements, maybe quantitative sort of staff,
[00:14:16 - 00:14:22] and then the specifications, the technical details of the engineering is how you meet those requirements.
[00:14:22 - 00:14:29] So something like the requirement might be something like the car must be able to drive it at least 100 kilometres now,
[00:14:29 - 00:14:34] but the specifications were stuff around the motor torque and power and that sort of thing.
[00:14:34 - 00:14:39] So that's what I came into this with.
[00:14:39 - 00:14:43] Anyway, so there's a lot of waffle here from check GBC,
[00:14:43 - 00:14:47] but it does have some useful stuff on here.
[00:14:47 - 00:14:56] And so, I printed it out and I've highlighted some bits because there's so much stuff I'm not just going to go through it.
[00:14:56 - 00:14:59] With the the what and the why and the how,
[00:14:59 - 00:15:01] a hidden example of a more,
[00:15:01 - 00:15:03] a more controlling robot arm, right?
[00:15:03 - 00:15:07] And so this is what somebody see it up there as it's kind of more customer speak.
[00:15:07 - 00:15:11] So things like, can you see it?
[00:15:11 - 00:15:16] You can see that the systems will pick and place objects that should operate safely around humans.
[00:15:16 - 00:15:21] Kind of waffly stuff. What does safely around humans mean?
[00:15:21 - 00:15:25] Does nothing like that's nothing that we can currently test if you like.
[00:15:25 - 00:15:29] I suppose you could put a lot of robots and a lot of humans together in county.
[00:15:29 - 00:15:37] He got hurt, possibly not the most ethically robust way of testing there.
[00:15:37 - 00:15:40] So that was, I thought that was interesting, but there's no list.
[00:15:40 - 00:15:45] These don't need to find numbers or detail performance, which is fine.
[00:15:45 - 00:15:49] And then down here with,
[00:15:49 - 00:15:52] where are we?
[00:15:52 - 00:15:54] How well and then,
[00:15:54 - 00:15:58] I guess the engineering view.
[00:15:58 - 00:16:01] There's a lot of stuff in here.
[00:16:01 - 00:16:04] The engineering view, why does function matters?
[00:16:04 - 00:16:08] Requirements is customer language, often qualitative, maybe ambiguous.
[00:16:08 - 00:16:12] The specifications engineering language quantitative must be precise.
[00:16:12 - 00:16:16] But they're conflicted with what I thought.
[00:16:16 - 00:16:19] And so I said to old chat GBC, that's interesting.
[00:16:19 - 00:16:21] Can you provide sources for this?
[00:16:21 - 00:16:24] Which is good. It does that. You should always do that.
[00:16:24 - 00:16:29] And so there's something from Incos, which is the International Council of Systems Engineering,
[00:16:29 - 00:16:32] which is, I guess, a level higher than mechatronics.
[00:16:32 - 00:16:35] It's looking at how systems engineer there's a hole.
[00:16:35 - 00:16:38] And it looks at ISO stuff.
[00:16:38 - 00:16:44] And it says, yeah, there's a bunch of stuff here.
[00:16:44 - 00:16:50] And if you look into it, the ISO stuff says the concept that
[00:16:50 - 00:16:54] specifications can be quantified, test it with human behavior,
[00:16:54 - 00:16:56] and that's fine.
[00:16:56 - 00:17:02] But there is a particularly interesting.
[00:17:02 - 00:17:10] It is a number of sources, but it's strong.
[00:17:10 - 00:17:16] The Incos is strongly emphasises that requirements must be necessary,
[00:17:16 - 00:17:18] but verifiable.
[00:17:18 - 00:17:20] So going back to what I said before,
[00:17:20 - 00:17:23] it's got to be safer around humans and things like that.
[00:17:23 - 00:17:27] That's not really verifiable, I think.
[00:17:27 - 00:17:38] And then under the ISO, IEC stuff says that the specifications have to be test-ool or verifiable.
[00:17:38 - 00:17:41] And so then I asked it again.
[00:17:41 - 00:17:47] There seems to be some crossover with these sources that same requirements need to be unusual.
[00:17:47 - 00:17:51] And verifiable, which means measurable.
[00:17:51 - 00:17:58] So then it says, and so this is why these things are quite useful.
[00:17:58 - 00:18:00] You can have a conversation with them.
[00:18:00 - 00:18:03] And the most important thing is don't just take what it says outright.
[00:18:03 - 00:18:06] Because if you say, well, that doesn't seem right.
[00:18:06 - 00:18:08] It comes back and goes, oh, it's right.
[00:18:08 - 00:18:09] You notice that.
[00:18:09 - 00:18:11] And then you get something that's different.
[00:18:11 - 00:18:21] So here, we can also say that these requirements are high-level and qualitative
[00:18:21 - 00:18:23] and specifications are measurable.
[00:18:23 - 00:18:24] Is that contradictory?
[00:18:24 - 00:18:25] No.
[00:18:25 - 00:18:35] What they get down to in the core of it, I'm sorry,
[00:18:35 - 00:18:41] our PPSS requirements must be verifiable, which usually implies measurable.
[00:18:41 - 00:18:45] So anyway, where I was getting with all of us is,
[00:18:45 - 00:18:56] they've got a nice summary down here, which I think lines up with what the more precise
[00:18:56 - 00:18:57] way to say it.
[00:18:57 - 00:18:59] And I'd like to hear what you think about this.
[00:18:59 - 00:19:02] To avoid ambiguity, we can use layered language.
[00:19:02 - 00:19:06] So there's something called a need, which is qualitative.
[00:19:06 - 00:19:08] And that's more like the customer need.
[00:19:08 - 00:19:10] That's the buttons got to have pop.
[00:19:10 - 00:19:13] That's got to be safe for humans.
[00:19:13 - 00:19:18] Then you've got a requirement, which is a measurable system level statement.
[00:19:18 - 00:19:22] So at a system level, like the robo-cup system,
[00:19:22 - 00:19:26] it's got to be able to move at maybe two minutes per second or something like that
[00:19:26 - 00:19:30] as a whole system, not as a tiny part of the system like the DC mode
[00:19:30 - 00:19:33] that's got to provide this amount of talk at system level.
[00:19:33 - 00:19:37] And then the technical specification has detailed engineering parameterization.
[00:19:37 - 00:19:42] So that's things like motor talks, motor powers, sensor,
[00:19:42 - 00:19:46] noise, SNR levels and stuff like that.
[00:19:46 - 00:19:51] What do we think about that?
[00:19:51 - 00:19:53] Does that make sense?
[00:19:53 - 00:19:54] I think this is one of these situations.
[00:19:54 - 00:19:57] It depends where you go, and people will call these things differently.
[00:19:57 - 00:20:01] So if you go to an engineering firm, they might call it a specification.
[00:20:01 - 00:20:04] And they'll engineering firm might call that a requirement.
[00:20:04 - 00:20:07] And so you've got to be, I guess, adaptable to that.
[00:20:07 - 00:20:10] But for the purposes of this course,
[00:20:10 - 00:20:13] I think this is the way we're going to continue working with it.
[00:20:13 - 00:20:16] So you might have some needs.
[00:20:16 - 00:20:18] So what are some needs for the robo-cup?
[00:20:18 - 00:20:20] I know, obviously, we haven't really...
[00:20:20 - 00:20:24] You haven't got all the details for that yet, but you know roughly what goes on.
[00:20:24 - 00:20:27] Yeah, it's got to be able to pick up weights.
[00:20:27 - 00:20:28] What else?
[00:20:28 - 00:20:31] Has to sort them?
[00:20:31 - 00:20:32] Yeah?
[00:20:32 - 00:20:34] No, I'm sorry too much at once.
[00:20:34 - 00:20:36] But good, keep talking.
[00:20:36 - 00:20:37] Yes, sir.
[00:20:37 - 00:20:39] Has to be able to move.
[00:20:39 - 00:20:41] I've got to be able to navigate on its own.
[00:20:41 - 00:20:43] It's got to be able to navigate on its own.
[00:20:43 - 00:20:45] So these are all things that are qualitative, right?
[00:20:45 - 00:20:47] What does navigate on its own mean?
[00:20:47 - 00:20:51] What does move mean in terms of how can we test these things?
[00:20:51 - 00:20:54] Or how can we tack it off as though that's achieved?
[00:20:54 - 00:20:56] So these are needs, which are good.
[00:20:56 - 00:21:02] Then we've got to kind of drill down a level into requirements.
[00:21:02 - 00:21:05] So for example, move, it needs to move.
[00:21:05 - 00:21:10] What sort of requirement were we starting to add quantitative values around it?
[00:21:10 - 00:21:15] We put to that.
[00:21:15 - 00:21:23] So for example, yeah, so it's got to get a move that's sitting around
[00:21:23 - 00:21:25] as like, it's meters per second.
[00:21:25 - 00:21:27] Yeah, it's got to pick up weights.
[00:21:27 - 00:21:33] How might we quantify that?
[00:21:33 - 00:21:34] Exactly.
[00:21:34 - 00:21:41] So I might have to lift at least two kilograms or be able to lift at least two kilograms.
[00:21:41 - 00:21:42] We're never going autonomously.
[00:21:42 - 00:21:43] What does that mean?
[00:21:43 - 00:21:45] How are we quantified that?
[00:21:45 - 00:21:55] I guess that you could have a robot that sets still for a long time,
[00:21:55 - 00:21:57] what meant that requirement.
[00:21:57 - 00:22:00] That would be an easy one to me.
[00:22:00 - 00:22:07] Yeah, so I guess more specifically possibly like an avoidance of water or obstacles
[00:22:07 - 00:22:11] or something to that effect without user input after being started
[00:22:11 - 00:22:13] or something like that sort of thing, right?
[00:22:13 - 00:22:22] Now, when we give you the robot cup design brief, if you like,
[00:22:22 - 00:22:24] what you'll start to realize is you go through that project.
[00:22:24 - 00:22:26] Does it's actually rather complicated?
[00:22:26 - 00:22:31] As a human, it's very easy to go, I need to go in this arena and pick up some weights.
[00:22:31 - 00:22:35] And I'll take them back to my home base, be getting a robot to this a bit harder.
[00:22:35 - 00:22:43] And in reality, the requirements for that entire project would amount to pages and pages.
[00:22:43 - 00:22:47] And you would really need to be able to talk to who we need to talk to
[00:22:47 - 00:22:52] to discuss these requirements if you were doing this in a commercial sense.
[00:22:52 - 00:22:59] So yeah, a customer would be a good one.
[00:22:59 - 00:23:03] Someone has done it before. I guess they're colleagues with experience.
[00:23:03 - 00:23:04] Yeah.
[00:23:04 - 00:23:05] Supplies.
[00:23:05 - 00:23:06] Supplies, yeah.
[00:23:06 - 00:23:12] People who are going to manufacture it, you'd want to be talking to them.
[00:23:12 - 00:23:14] To figure out these requirements.
[00:23:14 - 00:23:15] Who else?
[00:23:15 - 00:23:19] Project manager?
[00:23:19 - 00:23:20] Yeah.
[00:23:20 - 00:23:23] Who else?
[00:23:23 - 00:23:24] People who maintain it, right?
[00:23:24 - 00:23:27] Because it's likely it's going to be some maintenance at some point.
[00:23:27 - 00:23:33] Mobile robots are notoriously bad at keeping working.
[00:23:33 - 00:23:37] And so the maintenance people, the technicians probably,
[00:23:37 - 00:23:41] there's the manufacturers, but there's also the people who are going to assemble it potentially.
[00:23:41 - 00:23:45] Or those who manage those who are going to assemble it.
[00:23:45 - 00:23:50] Like there's the project managers, but there's also depending on who it's for.
[00:23:50 - 00:23:52] The company and stuff.
[00:23:52 - 00:23:54] And they might be the finance people.
[00:23:54 - 00:23:57] It depends on how much it's going to cost to develop these things and stuff.
[00:23:57 - 00:23:58] Right.
[00:23:58 - 00:24:00] So these are stakeholders.
[00:24:00 - 00:24:08] And so you need to have a quite a broad range of stakeholders when you're starting to figure out the requirements for your project.
[00:24:08 - 00:24:11] It's a bit hard for us to replicate that with the robot cup.
[00:24:11 - 00:24:16] Because you're kind of doing this university project.
[00:24:16 - 00:24:20] And it'll be lovely if I could meet with you all and pretend to be each of those stakeholders.
[00:24:20 - 00:24:23] But it's just not enough time in the day.
[00:24:23 - 00:24:28] And so what we ask you to do for the robot cup project is to come up with,
[00:24:28 - 00:24:31] I think it's about a page of requirements.
[00:24:31 - 00:24:35] But they've got to be non or call them non-trivial requirements.
[00:24:35 - 00:24:41] Because we give you a document, stuff like you can only use the controller board that Julian gives you.
[00:24:41 - 00:24:43] That's got a TNC 4.1.
[00:24:43 - 00:24:50] Don't go on then and tell me one of the requirements is it's got to use a TNC 4.1 because I already know that.
[00:24:50 - 00:24:52] We define that.
[00:24:52 - 00:24:58] Don't tell me that it's got to stay in the arena because that's one of the rules.
[00:24:58 - 00:25:06] What I want from you when it comes time is you to think pretty carefully about this project.
[00:25:06 - 00:25:11] And think what are some requirements that kind of define the project,
[00:25:11 - 00:25:17] the better the project that we've got control over and that makes sense.
[00:25:17 - 00:25:27] And also that it can test because in the progress report and the final report we want to see that you've done some testing to see whether your robots verify or verify against those requirements.
[00:25:27 - 00:25:30] So that's good.
[00:25:30 - 00:25:37] We've talked about what we see here that you've got the need for the requirements for these technical specifications and that sort of stuff.
[00:25:37 - 00:25:44] Now to get another example asked for a little bit more detail around what it was meaning by the engineering parameterization.
[00:25:44 - 00:25:53] And it came up with without me asking it and autonomous mobile robot, which is convenience because that's what you're doing in this class.
[00:25:53 - 00:25:57] And so the measurable system requirements.
[00:25:57 - 00:26:02] So this is the kind of thing that you'll need to come up with for requirements for robot cup.
[00:26:02 - 00:26:08] So their system level as it needs to be solution independent and shortly we'll talk a bit about that.
[00:26:08 - 00:26:12] It'll be expressed in terms of these externally observable performance.
[00:26:12 - 00:26:19] So effectively things you can measure kind of externalist behavior and you've got a verified system level.
[00:26:19 - 00:26:26] So the example would be the robot should travel over maximum speed of 1.5 minutes per second or flat ground.
[00:26:26 - 00:26:30] And so it's quantified 1.5 minutes per second or flat ground.
[00:26:30 - 00:26:31] That's testable.
[00:26:31 - 00:26:35] You can get a tape measure and a stopwatch and you can check there.
[00:26:35 - 00:26:38] And it doesn't prescribe how you're going to achieve it.
[00:26:38 - 00:26:40] So there are many ways that you could do this.
[00:26:40 - 00:26:44] You could have tracks, you could have wheels, it could be a hovercraft.
[00:26:44 - 00:26:46] Don't laugh.
[00:26:46 - 00:26:51] Several years ago one of the teams in the wacky races for the fourth year built a hovercraft for that.
[00:26:51 - 00:26:52] And it was pretty neat.
[00:26:52 - 00:26:55] And it moved around the really quickly round the trolley.
[00:26:55 - 00:26:58] It was a bit shit going up the ramps.
[00:26:58 - 00:27:01] But it was a nice example.
[00:27:01 - 00:27:07] And so here it says you could meet this with DC motors, BLDC, Steppers, hydraulic drive, differential gear ratios.
[00:27:07 - 00:27:10] Yeah, yeah, yeah.
[00:27:10 - 00:27:21] The specifications then which come down to the detailed engineering parameterization are then dependent on the architecture that you choose to meet this requirement with.
[00:27:21 - 00:27:26] So that's things like the motor has to have a talk of at least 2.8 meters.
[00:27:26 - 00:27:28] There needs to be a gear ratio of this.
[00:27:28 - 00:27:30] There's got to be a wheel radius of that.
[00:27:30 - 00:27:31] And that sort of thing.
[00:27:31 - 00:27:41] And so what we're coming back to with this is requirements are externally observable, measurable, quantifiable things.
[00:27:41 - 00:27:50] And then you've got specifications which are internal engineering things like motor talks and gear ratios and stuff like that.
[00:27:50 - 00:27:59] But if you meet those specifications, then assuming that you've done everything right, you'll therefore meet the requirements.
[00:27:59 - 00:28:00] Okay.
[00:28:00 - 00:28:02] Does that make sense?
[00:28:02 - 00:28:03] Good.
[00:28:03 - 00:28:06] Anyway, so check you please quite good while that.
[00:28:06 - 00:28:07] Having a conversation.
[00:28:07 - 00:28:13] But you've got to argue back because sometimes it does come up with a lot of shoes.
[00:28:13 - 00:28:22] And so you need to, and here's a nice table to summarize that, the structural difference, measurable system requirements, detailed engineering parameterization.
[00:28:22 - 00:28:34] So external versus internal architecture, neutral versus architecture specific, verified by system test, verified by analysis and subsystem models.
[00:28:34 - 00:28:41] The, the measurable system requirements custom and visible if you like whereas the specifications engineering visible.
[00:28:41 - 00:28:58] So I think that was, that's quite a nice way to, to really capture the difference between specifications and requirements.
[00:28:58 - 00:29:03] And then also need, so really we've got need requirement and specification.
[00:29:03 - 00:29:14] And so with that, as we sort of talked about, is the what's rather than the how.
[00:29:14 - 00:29:22] So it's really important not to go into too much detail with requirements about how you're going to do something.
[00:29:22 - 00:29:29] Because that obviously then can constrain what you're designing.
[00:29:29 - 00:29:37] It means that maybe you don't have options open to you.
[00:29:37 - 00:29:40] Any other thoughts on that?
[00:29:40 - 00:29:50] Who's, who's, have you had to come up with requirements in the past for, for, for line following?
[00:29:50 - 00:29:51] Yep.
[00:29:51 - 00:29:54] And had that work for you.
[00:29:54 - 00:29:59] Did anyone have problems with that or is that more of a, this is just an assessment task?
[00:29:59 - 00:30:01] Better come up with some.
[00:30:01 - 00:30:02] It's got to follow a line.
[00:30:02 - 00:30:10] Is there any learning that happened with that?
[00:30:10 - 00:30:19] There are some requirements that you get realising to do until you've got anything for you?
[00:30:19 - 00:30:22] That's a very good point.
[00:30:22 - 00:30:26] Which I think I'll get onto it, but we'll just talk about it now.
[00:30:26 - 00:30:32] Is yet not until you actually start building that you even think that this might be a requirement.
[00:30:32 - 00:30:33] It's never something you consider.
[00:30:33 - 00:30:37] Because it's very hard at the start of a project to consider everything at once.
[00:30:37 - 00:30:41] And I think you'll find exactly the same thing with the robot project.
[00:30:41 - 00:30:43] It's a bit more complicated yet again.
[00:30:43 - 00:30:47] And so you kind of want to go in there with some requirements.
[00:30:47 - 00:30:51] And then you'll refine those as you go.
[00:30:51 - 00:30:57] And that, you know, in the, in the conceptual design report, you'll have some requirements, which you present to us.
[00:30:57 - 00:31:00] But you can absolutely change those.
[00:31:00 - 00:31:02] And that's the same with final year projects.
[00:31:02 - 00:31:04] Every year the final year project start.
[00:31:04 - 00:31:11] It's an interesting, so for the final year projects, you've got to do your proposal.
[00:31:11 - 00:31:12] I think it's like two weeks in.
[00:31:12 - 00:31:14] Like, how did the project for two weeks?
[00:31:14 - 00:31:17] Which is not enough time to come up with a good set of requirements.
[00:31:17 - 00:31:19] Very relatively complicated project.
[00:31:19 - 00:31:24] And every year requirements have to be adjusted and changed and stuff like that.
[00:31:24 - 00:31:30] And that's just, that's a reasonably important part of it.
[00:31:30 - 00:31:36] I guess when you are out in industry, you've got to be a little bit careful about that.
[00:31:36 - 00:31:42] Because, you know, money starts to get spent on a project.
[00:31:42 - 00:31:46] And then you, you know, if you've spent all this time going here,
[00:31:46 - 00:31:50] and maybe the client comes and decides that and talking about that with you,
[00:31:50 - 00:31:52] they need to change the requirements.
[00:31:52 - 00:31:56] That's, that's of course for a variation and more billing comes in.
[00:31:56 - 00:31:59] And so you've got to be careful of it.
[00:31:59 - 00:32:03] But yeah, that comes with the nature of design being quite iterative.
[00:32:03 - 00:32:06] So one thing I've not here that the requirements are a,
[00:32:06 - 00:32:11] one thing that's really important about them is there are a tool for communicating a common understanding
[00:32:11 - 00:32:15] of what needs to be done to everybody, including the clients.
[00:32:15 - 00:32:16] Right.
[00:32:16 - 00:32:19] So if you've got a nice set of requirements, you, as the engineer,
[00:32:19 - 00:32:21] is understand what you have to design.
[00:32:21 - 00:32:27] The client understands who, you know, the person is paying for it, understands what you need to design.
[00:32:27 - 00:32:31] And when you've designed it, you can show that you meet those requirements
[00:32:31 - 00:32:35] or the system that you did on those requirements and everyone's happy.
[00:32:35 - 00:32:41] If you've got a shorty set of requirements that is kind of ambiguous or poorly written,
[00:32:41 - 00:32:47] you think you've solved the problem and the client thought you were solving something else.
[00:32:47 - 00:32:52] And then they've got to pay for, you know, they're not happy to pay for this because it's not what you did.
[00:32:52 - 00:32:55] You didn't do what they wanted, right?
[00:32:55 - 00:32:59] And so you can see that there's potential problems with it.
[00:32:59 - 00:33:07] So having this set of written down requirements is something that is really quite important
[00:33:07 - 00:33:13] so that everybody knows what's going on.
[00:33:13 - 00:33:14] Just jump through those.
[00:33:14 - 00:33:17] I'm so really talk about some with Rebecca.
[00:33:17 - 00:33:24] So, yeah, requirements should cover a bunch of things, you know, aspects.
[00:33:24 - 00:33:29] So this functional requirements, so what might be a functional requirement for Rebecca?
[00:33:29 - 00:33:34] Yeah, it's got to be able to pick up weights.
[00:33:34 - 00:33:36] We've put some numbers around there.
[00:33:36 - 00:33:41] Performance requirements, and sometimes this crossover between these, right?
[00:33:41 - 00:33:46] Performance requirement might be a year navigation,
[00:33:46 - 00:33:49] or it's got about a run for at least two minutes.
[00:33:49 - 00:33:53] If you're drawing so much current from your battery that can't run for two minutes,
[00:33:53 - 00:33:55] it might be a problem.
[00:33:55 - 00:33:58] What might be a non-functional requirement?
[00:33:58 - 00:34:09] Occasionally people have got to operate between minus 20 degrees and 40 degrees.
[00:34:09 - 00:34:12] You're like, yes, so do we all like.
[00:34:12 - 00:34:15] This is operating in the engineering building.
[00:34:15 - 00:34:18] We're not taking it to Mars.
[00:34:18 - 00:34:23] And so, but those sorts of things that might be an operational requirement,
[00:34:23 - 00:34:28] or it might be, it's got to be able to last a couple of rounds.
[00:34:28 - 00:34:29] There's put numbers on that.
[00:34:29 - 00:34:35] Several rounds without failing, because you're mostly watched a robot cup last year.
[00:34:35 - 00:34:37] You saw a number of failures.
[00:34:37 - 00:34:40] And there's also what we started to refer to as robot dandruff.
[00:34:40 - 00:34:43] Like when we're going around in the arena between the rounds,
[00:34:43 - 00:34:47] putting the weights back, there's always nuts and screws and shit.
[00:34:47 - 00:34:49] And there, every round.
[00:34:49 - 00:34:51] And I would know one knows who are these.
[00:34:51 - 00:34:57] And they're like, oh, so robots are shitting parts.
[00:34:57 - 00:35:00] And then there's also constraints.
[00:35:00 - 00:35:06] So when you're thinking about your requirements, start to classify them like this.
[00:35:06 - 00:35:12] And now that important thing, and this was also brought up in the chat,
[00:35:12 - 00:35:15] I had with chat GPT, is they need to be abstract.
[00:35:15 - 00:35:17] So that's the what, not the how.
[00:35:17 - 00:35:20] So you're not constraining your design space.
[00:35:20 - 00:35:23] The verifiable, which means that you can test them.
[00:35:23 - 00:35:26] And it becomes like, it needs to be something that it does it achieve it,
[00:35:26 - 00:35:28] or does it not achieve it.
[00:35:28 - 00:35:30] Right? It's a tech box exercise.
[00:35:30 - 00:35:33] An ambiguous, why is that important?
[00:35:33 - 00:35:37] Yeah.
[00:35:37 - 00:35:38] So what I said with the customer, right?
[00:35:38 - 00:35:43] If you think the requirement means this, and they think it means that.
[00:35:43 - 00:35:47] The one that comes up quite a lot that people put down is the robot should be reliable.
[00:35:47 - 00:35:53] Like, well, I think reliable is it goes for five minutes without crapping out.
[00:35:53 - 00:35:56] And they think reliable means it goes for a year without failing.
[00:35:56 - 00:35:58] Then we've got a problem.
[00:35:58 - 00:36:04] So we've got to be able to make that, you know, it might be something like it's got to be able to operate for
[00:36:04 - 00:36:12] at least X number of days without requiring maintenance or something like that becomes much more specific.
[00:36:12 - 00:36:14] Trasable.
[00:36:14 - 00:36:20] And so traceable, there's got to be effectively that shows the need for the requirement.
[00:36:20 - 00:36:26] And recall we had need requirement specification, and there should be traceable things from that.
[00:36:26 - 00:36:30] So the client says, the robot's got to be fast.
[00:36:30 - 00:36:35] You have converted that into the robot must move at least 1.5 meters per second.
[00:36:35 - 00:36:44] And then that becomes a specification that there's going to be a DC motor that provides X amount of power or talk or speed.
[00:36:44 - 00:36:45] Right?
[00:36:45 - 00:36:47] You can trace between those.
[00:36:47 - 00:36:54] It's not like you've got a requirement there that just says the requirement, the robot must use DC motors.
[00:36:54 - 00:36:57] And anyone else looking at it's like, why?
[00:36:57 - 00:37:03] Like there's no traceability that you've got to have a clear line of traceability.
[00:37:03 - 00:37:05] And necessity as well.
[00:37:05 - 00:37:10] Because what happens if we've got requirements that aren't necessary?
[00:37:14 - 00:37:17] Yeah, potential increases in cost.
[00:37:17 - 00:37:21] In potential constraints in the design space.
[00:37:21 - 00:37:27] If you think of NASA's rovers on Mars, for example, those supposed to have white design lives of some of them,
[00:37:27 - 00:37:31] white 90 days and things in the operating five years later.
[00:37:31 - 00:37:36] Which is good engineering, but it's probably a bit more expensive than it needed to be.
[00:37:36 - 00:37:41] And so, you know, the design life was 90 days.
[00:37:41 - 00:37:44] And you've got something that can run for five years.
[00:37:44 - 00:37:49] That's a massive cost.
[00:37:49 - 00:37:53] Here's some examples.
[00:37:53 - 00:37:58] Just from previous years, Robocar robots.
[00:37:58 - 00:38:01] There's anything that's particularly interesting in there.
[00:38:01 - 00:38:06] Does it need that you can look at and think that one's rubbish or that one's good?
[00:38:06 - 00:38:15] Hopefully, doesn't it?
[00:38:15 - 00:38:20] Yeah, the robot should use sensors to avoid undesired behaviour caused by the environment.
[00:38:20 - 00:38:22] But what's undesired?
[00:38:22 - 00:38:25] There's a good point.
[00:38:25 - 00:38:27] How does the environment have a good behaviour?
[00:38:27 - 00:38:37] So that's not a great one.
[00:38:37 - 00:38:43] You know, that one's, I mean, I guess there comes to why is that a required, like what,
[00:38:43 - 00:38:45] the necessity around there?
[00:38:45 - 00:38:50] Possibly, well, it's a weird number because if you're planning on your robot driving off the edge of the ramp,
[00:38:50 - 00:38:55] the ramp is about 70 metres, 70 millimetres tall, 70 metres.
[00:38:55 - 00:38:56] 70 metres.
[00:38:56 - 00:38:57] 70 mil tall.
[00:38:57 - 00:38:59] So I don't know where the 25 mil comes from.
[00:38:59 - 00:39:04] Maybe they just, maybe they made a robot and they dropped it from 26 mil I cracked out.
[00:39:04 - 00:39:12] So they're like, well, if we make it 25, we can pass this.
[00:39:12 - 00:39:13] No, you did right now.
[00:39:13 - 00:39:14] There wasn't really anything.
[00:39:14 - 00:39:18] I think it might have just said, yeah, it should survive.
[00:39:18 - 00:39:22] It should be able to operate normally.
[00:39:22 - 00:39:25] Yeah.
[00:39:25 - 00:39:32] So, oh, yes.
[00:39:32 - 00:39:33] Yeah.
[00:39:33 - 00:39:35] Which, there's two Julian's now department.
[00:39:35 - 00:39:40] Okay, they're both not particularly tall, but who's near who he's walking about.
[00:39:40 - 00:39:41] Yeah.
[00:39:41 - 00:39:44] So, Heather, yeah.
[00:39:44 - 00:39:51] How to think of these while you're thinking about your robot car.
[00:39:51 - 00:39:55] As I said, have a read over these notes as well.
[00:39:55 - 00:39:58] But how do you come up with these?
[00:39:58 - 00:40:04] So, as you mentioned up here before, once you start designing,
[00:40:04 - 00:40:11] that starts to help you come up with ideas for these requirements
[00:40:11 - 00:40:14] or you discover things that you need to put down.
[00:40:14 - 00:40:16] But you also think about the problem.
[00:40:16 - 00:40:20] Think about who has the problem and what are the goals?
[00:40:20 - 00:40:25] What are the side effects to be avoided shooting projectiles
[00:40:25 - 00:40:30] and to Julian's quads for example, clearly there's a side effect to be avoided.
[00:40:30 - 00:40:34] Which actions are admissible?
[00:40:34 - 00:40:38] Other things, you know, how should the system behave during a failure
[00:40:38 - 00:40:41] and expect a conditions?
[00:40:41 - 00:40:45] So, the reason I've got the picture of this ear bus up here is
[00:40:45 - 00:40:49] and you can look up on working for the terms of watch and on effort.
[00:40:49 - 00:40:54] It was an ear bus, so I think it was an 80-20, I can't remember.
[00:40:54 - 00:40:59] But anyway, the header condition and the engineers clearly thought about this
[00:40:59 - 00:41:04] that they didn't want the pilots engaging reverse thrust on those engines
[00:41:04 - 00:41:06] when the plane wasn't on the ground.
[00:41:06 - 00:41:10] Because obviously, it's not particularly conducive to fly.
[00:41:10 - 00:41:19] And so, they had some conditions that reverse thrust could not be engaged unless
[00:41:19 - 00:41:23] the main wheels were, the old wheels were down
[00:41:23 - 00:41:27] and the wheels were spinning at a certain speed.
[00:41:27 - 00:41:32] And so, they had the boat loads on the old wheels, so they had to be a certain weight on both the old wheels
[00:41:32 - 00:41:35] and the wheels were spinning at a certain speed.
[00:41:35 - 00:41:39] However, this particular flight was landing, I think it was in Sweden,
[00:41:39 - 00:41:45] and had been raining, so there was a lot of water on the runway and the header held on crosswind.
[00:41:45 - 00:41:49] So, it came in and pretty much all the planes' weight was on one old wheel,
[00:41:49 - 00:41:53] and the wheels were spinning fast away, equiplying across the water,
[00:41:53 - 00:41:56] and the pilots tried to engage reverse thrust and the planes said, no.
[00:41:56 - 00:42:03] And so, they couldn't see it fast enough and went off the end of the runway and it looked far.
[00:42:03 - 00:42:07] I think most people got out there, it was potentially a couple of fatalities,
[00:42:07 - 00:42:11] but the engineers who got through this had thought through it,
[00:42:11 - 00:42:15] but it's very hard to think through every possible scenario.
[00:42:15 - 00:42:23] And sometimes when you do, you may sort of put in other inadvertent conditions
[00:42:23 - 00:42:27] that more cause you problems later, but think about this with robot cup.
[00:42:27 - 00:42:31] What sort of situations or failures might occur on your robot?
[00:42:31 - 00:42:34] You should think about it. What have you seen?
[00:42:34 - 00:42:36] Yeah? Coligens?
[00:42:36 - 00:42:37] Yeah? Coligens? What? Okay.
[00:42:37 - 00:42:40] The collision itself is not a problem, but what might be the problem?
[00:42:40 - 00:42:44] Yeah, breaking a sensor off that happens every year.
[00:42:44 - 00:42:47] Getting stuck, it happens every year.
[00:42:47 - 00:42:48] Yeah.
[00:42:48 - 00:42:57] So, pretty much every year at least one of them has a track for off.
[00:42:57 - 00:43:01] What can you do in that case?
[00:43:01 - 00:43:04] I've seen, I've seen, like, there's a couple of ways you can fix this.
[00:43:04 - 00:43:07] Some students, some teams have put guards around their tracks,
[00:43:07 - 00:43:09] so that makes their a little bit harder.
[00:43:09 - 00:43:11] Other teams have made the track driving wheel.
[00:43:11 - 00:43:16] They'll have rubber on there so that there's a further traction from that wheel
[00:43:16 - 00:43:18] even if the track comes off.
[00:43:18 - 00:43:22] So, it doesn't work as well as it does, but that's not just going around in circles either.
[00:43:22 - 00:43:27] What other things?
[00:43:27 - 00:43:29] Wires getting ripped off?
[00:43:29 - 00:43:30] Like, it's very common.
[00:43:30 - 00:43:33] People have got a rat's nest of wires on their robot,
[00:43:33 - 00:43:37] and another one tangles one in, and wires get ripped out.
[00:43:37 - 00:43:41] So, have a think, you know, what could happen?
[00:43:41 - 00:43:44] Okay. The wires thing, tidy it up.
[00:43:44 - 00:43:49] The track thing, you know, there was a potential solution with that.
[00:43:49 - 00:43:54] Similarly, you can kind of have guarding for your senses and stuff.
[00:43:54 - 00:43:55] Yeah.
[00:43:55 - 00:43:58] And have a think about how you might do these.
[00:43:58 - 00:44:00] How you might test the system to not work.
[00:44:00 - 00:44:02] So, if you've got these requirements,
[00:44:02 - 00:44:03] you need to verify them.
[00:44:03 - 00:44:05] How might you do the testing?
[00:44:05 - 00:44:06] Sorry.
[00:44:06 - 00:44:08] Had it with a hammer?
[00:44:08 - 00:44:10] Don't break them.
[00:44:10 - 00:44:14] Drafty users manual, because often when you start thinking,
[00:44:14 - 00:44:18] how would you convey this information about how the thing works to a person?
[00:44:18 - 00:44:22] It makes you think about how it's going to be used.
[00:44:22 - 00:44:24] And so, there's a bunch.
[00:44:24 - 00:44:29] And the last thing down here drew your attention to the number to seven,
[00:44:29 - 00:44:31] which was described earlier.
[00:44:31 - 00:44:34] It's not designing the system, because when you start designing it,
[00:44:34 - 00:44:37] a lot of things come up that you didn't think about.
[00:44:37 - 00:44:43] That's also a good cutter in a barrel of requirements.
[00:44:43 - 00:44:54] Okay.
[00:44:54 - 00:44:57] We've got a couple of minutes left.
[00:44:57 - 00:45:00] What I will do is information about here, about stating them,
[00:45:00 - 00:45:05] what I will do is,
[00:45:05 - 00:45:11] where do I have it?
[00:45:11 - 00:45:14] So, key things, and I know this is about hard,
[00:45:14 - 00:45:16] because when you're writing essays at school,
[00:45:16 - 00:45:18] you often use synonyms,
[00:45:18 - 00:45:23] so that your essays and what you've done sound repetitive.
[00:45:23 - 00:45:27] But as engineers, don't use synonyms,
[00:45:27 - 00:45:30] because that can confuse people.
[00:45:30 - 00:45:32] Like, for example, when the button is pressed once,
[00:45:32 - 00:45:33] the LED should turn on,
[00:45:33 - 00:45:35] when the switch is pressed twice, the LED should be turned off.
[00:45:35 - 00:45:37] Isn't the button the same thing as the switch?
[00:45:37 - 00:45:41] Like, as that synonyms, or if we've got two separate user interfaces,
[00:45:41 - 00:45:44] so be really consistent with your phrasing.
[00:45:44 - 00:45:47] One term is equal to one thing.
[00:45:47 - 00:45:55] Tables, diagrams can be particularly useful.
[00:45:55 - 00:45:57] Avoid wishy-washy words.
[00:45:57 - 00:46:01] Things like flexible, fault-tolerant, rapid, optimum, easy.
[00:46:01 - 00:46:04] We're trying to quantify these things.
[00:46:04 - 00:46:08] I like this particular example from, I mean, okay, it's 1907.
[00:46:08 - 00:46:11] But it should be sufficiently simple in its construction,
[00:46:11 - 00:46:14] in operation, to permit an intelligent van,
[00:46:14 - 00:46:18] to become proficient, and it's used within a reasonable length of time.
[00:46:18 - 00:46:21] How is one verify this?
[00:46:21 - 00:46:27] So, there's a lot wrong with that.
[00:46:27 - 00:46:31] So, in doing this,
[00:46:31 - 00:46:35] specify, don't specify exact numbers,
[00:46:35 - 00:46:39] specify a range, so be exact-ish, or a tolerance, right?
[00:46:39 - 00:46:42] Don't ever say, my robot must go at 2.0 meters per second,
[00:46:42 - 00:46:44] because that's bloody hard.
[00:46:44 - 00:46:48] What you want to say is my robot must travel at least 1.5,
[00:46:48 - 00:46:51] because that gives you 1.5 plus, right?
[00:46:51 - 00:46:55] Or you might say, the cruising speed must be 60 plus or minus 1 can now.
[00:46:55 - 00:47:00] You need, like, numbers, but a bit of a range around those numbers.
[00:47:00 - 00:47:05] The position here should be no greater than 2 cm, for example.
[00:47:05 - 00:47:08] Now, this shell should well thing.
[00:47:08 - 00:47:13] I've pilfered this young to go from the NASA Systems Engineering Handbook.
[00:47:13 - 00:47:15] If you talk to your friends in mechanical engineering,
[00:47:15 - 00:47:18] they get told to use like this demands and wishes,
[00:47:18 - 00:47:23] which sounds like, I don't know, sounds shit to me.
[00:47:23 - 00:47:26] So, it does sound like that.
[00:47:26 - 00:47:29] And I think NASA's usually doing quite an engineering,
[00:47:29 - 00:47:30] and I'll stick with that.
[00:47:30 - 00:47:32] And interestingly, without me saying it,
[00:47:32 - 00:47:35] the examples provided by Chet, you can tell your shell should type so.
[00:47:35 - 00:47:38] So, shell is a mandatory behavior.
[00:47:38 - 00:47:41] We've got a phone again.
[00:47:41 - 00:47:46] The robot shell travel, and at least 2 meters per second.
[00:47:46 - 00:47:49] Right, so that's, it will go faster than that.
[00:47:49 - 00:47:53] Should as a typical behavior that might have special cases,
[00:47:53 - 00:47:59] or, you know, should not fail more than whatever.
[00:47:59 - 00:48:02] And well isn't a requirement, but that's a statement of fact.
[00:48:02 - 00:48:06] So, the vehicle test will be conducted at government test facilities.
[00:48:06 - 00:48:12] So, we will use the shell should well when you're putting together your requirements for Rebecca.
[00:48:12 - 00:48:20] And relating to the traceability, it's also really good to document your rationale.
[00:48:20 - 00:48:24] So, you have a requirement, like the Space Station of Comedy Launch Vehicle Watchplaces,
[00:48:24 - 00:48:31] the Space
[00:48:31 - 00:48:33] Works in Access, horizontal or vertical.
[00:48:33 - 00:48:35] Then there's a rationale for that.
[00:48:35 - 00:48:37] Why is that requirement there?
[00:48:37 - 00:48:41] And that's good practice in the robot cup.
[00:48:41 - 00:48:42] But it's also good because some projects you work on might go on for years and years and years.
[00:48:42 - 00:48:45] And you might leave the company before it's finished.
[00:48:45 - 00:48:48] And therefore, somebody coming along later is looking at this requirement,
[00:48:48 - 00:48:51] going, why on earth is this here?
[00:48:51 - 00:49:02] And that rationale provides that kind of explanation and traceability for them to understand why it's there.
[00:49:02 - 00:49:06] So, if you want to have a look at some more information, there's a NASA system,
[00:49:06 - 00:49:09] Handbook, you can get that from the NASA website.
[00:49:09 - 00:49:13] I've also got, the Mars Global Surveyor,
[00:49:13 - 00:49:18] on the design tool section of the Learn Page for this course, there's a PDF document,
[00:49:18 - 00:49:20] and it's quite long.
[00:49:20 - 00:49:24] You can have a look at some of the examples of this.
[00:49:24 - 00:49:26] That's all ignored it.
[00:49:26 - 00:49:31] But hopefully, that's a tool of my ship.
[00:49:31 - 00:49:34] The one on the right still on the planet, the one on the left,
[00:49:34 - 00:49:37] went to the sales years ago.
[00:49:37 - 00:49:42] So, hopefully, there's good enough idea about requirements and why they're important.
[00:49:42 - 00:49:49] But don't forget to kind of flick through the lecture slides to make sure you up to speed on some of those details.
[00:49:49 - 00:49:52] Otherwise, we'll see you next Thursday.
[00:49:52 - 00:49:59] I just don't mind if we won't be using the lab slot next week on the Wednesday, so you can pretty time.
[00:49:59 - 00:50:26] I've also got a quick question.
[00:50:26 - 00:50:33] I'm not sure if you meant that, but it's the lab today, one in like a four.
[00:50:33 - 00:50:35] It's not the rest of the storage tool.
[00:50:35 - 00:50:37] It's a rich object, isn't it?
[00:50:37 - 00:50:38] It's a light-dope.
[00:50:38 - 00:50:39] It's a storage tool.
[00:50:39 - 00:50:42] It's not my part of the course I'm afraid.
[00:50:42 - 00:50:45] But if you email George, you'll tell you.
[00:51:42 - 00:51:49] I'll see you next Thursday.
[00:51:49 - 00:52:05] Thank you very much.
[00:52:05 - 00:52:08] Thank you.
[00:52:08 - 00:52:13] Okay.
[00:52:13 - 00:52:14] Thank you.
[00:52:14 - 00:52:16] Thank you so much.
[00:52:16 - 00:52:18] Thank you.
[00:52:18 - 00:52:19] Thank you so much.
[00:52:19 - 00:52:20] Thank you so much.
[00:52:20 - 00:52:22] Thank you.
[00:52:22 - 00:52:24] Thank you.

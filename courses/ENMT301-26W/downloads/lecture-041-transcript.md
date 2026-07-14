# ENMT301-26W Lecture 41 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_41_audio_16k_mono_32k.mp3`
Source audio SHA-256: `0d9fd8aea4f6374aa34423e954c9302d91fcbbf6b2c9ca0686ff3560d6d1585f`
Generated: 2026-06-06T06:35:37.925036+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:29 - 00:00:32] Alright, thanks everyone. We'll make a start there.
[00:00:32 - 00:00:40] Right, hopefully you can hear me all good.
[00:00:40 - 00:00:43] Obviously as usual, welcome to Scrater Sea Rhine.
[00:00:43 - 00:00:47] It's been such a long time since 10 o'clock this morning.
[00:00:47 - 00:00:50] Also welcome to all the people watching online.
[00:00:50 - 00:00:52] Before I start and before I forget,
[00:00:52 - 00:00:55] I'd just like to acknowledge Rebecca,
[00:00:55 - 00:00:57] who is from Silhouin, Engineering.
[00:00:57 - 00:01:01] She's one of the academics, associate here at the Parliament.
[00:01:01 - 00:01:05] And she's just going to be evaluating my teaching.
[00:01:05 - 00:01:09] So just, economically, it's nothing to do with you,
[00:01:09 - 00:01:12] but it will help me to get some feedback.
[00:01:12 - 00:01:15] Moving forward. So, without further ado,
[00:01:15 - 00:01:18] I suppose today's focus on our Victoria,
[00:01:18 - 00:01:21] or our Victoria, is we'll have about half of it
[00:01:21 - 00:01:24] that's been on the bearing housing design.
[00:01:24 - 00:01:26] I'll probably talk about some of that stuff first.
[00:01:26 - 00:01:29] Then we'll talk about our kind of consideration
[00:01:29 - 00:01:32] for spring design, which I'll just go through
[00:01:32 - 00:01:35] some of the lecture notes that will kind of scaffold you
[00:01:35 - 00:01:37] in doing that part of the assignment.
[00:01:37 - 00:01:38] And then depending on how we're going for time,
[00:01:38 - 00:01:41] we can kind of complete kind of further discussions,
[00:01:41 - 00:01:45] depending on what kind of questions you guys have.
[00:01:45 - 00:01:48] So, yeah, we already had the exciting news.
[00:01:48 - 00:01:51] So, that's all good there.
[00:01:51 - 00:01:55] Notices, I've put a video on learn about it.
[00:01:55 - 00:01:57] Feels like a month ago now,
[00:01:57 - 00:01:59] but at the very start of the holidays,
[00:01:59 - 00:02:02] it was a video on learn,
[00:02:02 - 00:02:04] and then some recent examples
[00:02:04 - 00:02:08] that kind of show some of these kind of calculations here.
[00:02:08 - 00:02:10] So, just making sure that you're aware of those.
[00:02:12 - 00:02:16] Yeah, so, full completeness and for my own sanity,
[00:02:16 - 00:02:20] if we're on learn, and if we go into our bearing housing
[00:02:20 - 00:02:24] section, if I change my view to a student,
[00:02:24 - 00:02:26] then you'll be seeing the same stuff.
[00:02:27 - 00:02:29] There we can see we've got this example here,
[00:02:29 - 00:02:32] and then the video here, and then here we have
[00:02:32 - 00:02:35] our further examples that maybe of use,
[00:02:36 - 00:02:39] which I kind of talked through in each of those videos.
[00:02:39 - 00:02:43] So, I think the videos are only about 25, 30-ish minutes long.
[00:02:44 - 00:02:47] Kind of shows examples that you might find useful
[00:02:47 - 00:02:49] in completing your assignments.
[00:02:49 - 00:02:52] So, I know this morning we kind of talked about
[00:02:52 - 00:02:56] secondary moments, and then if you're reviewing that,
[00:02:56 - 00:02:59] this here is a similar arrangement,
[00:02:59 - 00:03:02] which might kind of help to scaffold you
[00:03:02 - 00:03:06] in doing a similar thing for your design situation.
[00:03:08 - 00:03:09] Any questions on any of those?
[00:03:09 - 00:03:12] If people looked at those videos,
[00:03:12 - 00:03:13] at least knew they existed.
[00:03:14 - 00:03:17] Yeah, so it's valuable for me to do that,
[00:03:17 - 00:03:20] but yeah, obviously you can see that that's there now.
[00:03:21 - 00:03:22] Then yeah.
[00:03:23 - 00:03:25] Cool, all right.
[00:03:25 - 00:03:27] Any questions on any of that so far?
[00:03:28 - 00:03:29] Seems like a few were haven't looked at it.
[00:03:29 - 00:03:31] It's hard to have questions about it.
[00:03:31 - 00:03:34] So, as I talked about, we'll focus on our design of springs.
[00:03:34 - 00:03:36] But before we do that, we will touch on any burning questions
[00:03:36 - 00:03:37] you have.
[00:03:37 - 00:03:41] Go over a little comment about our material selection
[00:03:41 - 00:03:45] for designing our shaft in the second assignment,
[00:03:45 - 00:03:49] as well as just going over what is expected
[00:03:49 - 00:03:51] for our clutch design.
[00:03:52 - 00:03:55] So we'll kind of do bullet point two, three, four,
[00:03:55 - 00:03:57] and then I'll go over bullet point one.
[00:03:57 - 00:03:59] And then depending on time,
[00:03:59 - 00:04:02] we can either review our bearing selection process
[00:04:02 - 00:04:05] or do a possible example.
[00:04:05 - 00:04:10] So, currently, give me about Summit one or Summit two.
[00:04:11 - 00:04:15] What questions do you have?
[00:04:15 - 00:04:16] I know someone had some questions,
[00:04:16 - 00:04:32] so I'll give them some time to pull them up.
[00:04:33 - 00:04:35] So, slightly summarize your question,
[00:04:35 - 00:04:37] but the question broadly speaking was,
[00:04:37 - 00:04:41] do we need to assume an axial force
[00:04:41 - 00:04:43] for our calculations, right?
[00:04:43 - 00:04:46] And so, we've said that one of our bearings,
[00:04:46 - 00:04:48] if we draw both of the bearings,
[00:04:48 - 00:04:52] one of them is free to move, and one of them is fixed, right?
[00:04:52 - 00:04:54] And this might be our shaft here.
[00:04:55 - 00:04:58] And so, when we're doing some calculations on our shaft,
[00:04:58 - 00:05:01] I e maybe this part of the shaft has some sort of
[00:05:01 - 00:05:05] shoulder on it and our bearing is going here.
[00:05:05 - 00:05:07] To check that out kind of housing
[00:05:07 - 00:05:09] or our fastness is gonna be strong enough,
[00:05:09 - 00:05:12] we're gonna have to assume some sort of axial load
[00:05:12 - 00:05:14] to do that calculation, right?
[00:05:14 - 00:05:17] So, I'm okay for you to assume a load.
[00:05:17 - 00:05:19] Suppose if you want to, you could write something
[00:05:19 - 00:05:22] about reasonable misuse, like you don't want
[00:05:22 - 00:05:23] some engineering student coming along
[00:05:23 - 00:05:26] and pulling this part of the component
[00:05:26 - 00:05:28] and falling apart, right?
[00:05:28 - 00:05:30] So, it'll probably be a pretty small amount of load.
[00:05:30 - 00:05:33] For example, you could choose a 500 newtons
[00:05:33 - 00:05:36] or something like that, but the main thing
[00:05:36 - 00:05:38] is just making it clear what your assumption is
[00:05:38 - 00:05:39] so that you can do that.
[00:05:39 - 00:05:43] And in this design context this year,
[00:05:43 - 00:05:45] we don't actually have like a big axial load, right?
[00:05:45 - 00:05:47] So, it would be kind of different.
[00:05:47 - 00:05:49] If our arrangement was such that, I don't know,
[00:05:49 - 00:05:51] maybe if it was a big fan on the end
[00:05:51 - 00:05:53] or if our shaft arrangement was vertical
[00:05:53 - 00:05:55] and there was some mass on it, obviously,
[00:05:55 - 00:05:57] we would have a load going actually
[00:05:57 - 00:05:58] throughout bearings.
[00:05:58 - 00:06:02] But in this case, we don't really have a clear axial load
[00:06:02 - 00:06:05] in our loading situation.
[00:06:06 - 00:06:08] Yeah, that's a good question in the game.
[00:06:09 - 00:06:11] Only is kind of useful for doing that
[00:06:11 - 00:06:13] compressor of shoulder check
[00:06:13 - 00:06:14] and then kind of helps you to think about
[00:06:14 - 00:06:17] if your arrangement is going to be fixed
[00:06:17 - 00:06:21] in this area here.
[00:06:21 - 00:06:22] Cool.
[00:06:23 - 00:06:25] Well, other burning questions, do you have
[00:06:25 - 00:06:40] as you've tried to make a start on that assignment?
[00:06:43 - 00:06:44] Good question.
[00:06:44 - 00:06:48] So the question was, do we have to calculate
[00:06:48 - 00:06:51] the chain force required to pull a carriage up
[00:06:51 - 00:06:55] the lift position or do we just use the max power?
[00:06:55 - 00:06:57] The answer is both.
[00:06:57 - 00:06:57] Yeah.
[00:06:57 - 00:07:00] So to explain that, I will just refer
[00:07:00 - 00:07:02] to one of the frequently asked questions
[00:07:02 - 00:07:05] that I put up that hopefully was trying to clarify that
[00:07:07 - 00:07:09] for the game, for my own sanity,
[00:07:09 - 00:07:12] that will make it easier to kind of see.
[00:07:12 - 00:07:14] So there's two things that are happening there.
[00:07:14 - 00:07:17] And I will kind of jump to the document camera
[00:07:17 - 00:07:18] to also discuss this.
[00:07:18 - 00:07:21] But if we see frequently asked questions,
[00:07:22 - 00:07:25] what I would say is the first steps that we see
[00:07:25 - 00:07:27] that to do our free body diagram
[00:07:27 - 00:07:30] and then thus work out our share force
[00:07:30 - 00:07:33] ending moment and then a talk moment diagram, right?
[00:07:33 - 00:07:34] Just for your standard kind of loading.
[00:07:34 - 00:07:37] And obviously for that loading case,
[00:07:37 - 00:07:40] we're assuming that there is some sort of,
[00:07:40 - 00:07:46] this is the plane of the sprocket.
[00:07:46 - 00:07:49] And we've said that if we were looking at a side view,
[00:07:49 - 00:07:52] that you have to tell me what angle
[00:07:52 - 00:07:55] that chain force is acting, right?
[00:07:55 - 00:07:57] I don't mind what angle it is.
[00:07:57 - 00:08:00] But if we look at my sketch kind of here,
[00:08:00 - 00:08:02] we can see that the way that I've drawn it,
[00:08:02 - 00:08:05] it's kind of unclear exactly what direction
[00:08:05 - 00:08:06] that force would be acting, right?
[00:08:07 - 00:08:09] So as long as you state on a side view,
[00:08:09 - 00:08:12] this is where I'm assuming my FT acting.
[00:08:12 - 00:08:14] And thus this is what my share force
[00:08:14 - 00:08:16] in vining moment diagram would look
[00:08:16 - 00:08:19] in the front plane and the top plane, right?
[00:08:19 - 00:08:20] So for the standard loading case,
[00:08:20 - 00:08:23] it might not be very much at all happening
[00:08:23 - 00:08:24] in one of those planes.
[00:08:24 - 00:08:27] To work out that chain force,
[00:08:27 - 00:08:29] we've been told in the assignment.
[00:08:29 - 00:08:36] So if I pull up the assignment brief as well,
[00:08:36 - 00:08:39] we've been told that is how many kilowatt engine
[00:08:40 - 00:08:42] did you kill the wire, right?
[00:08:43 - 00:08:48] So we wanna design our shaft to be able to hold
[00:08:48 - 00:08:51] that maximum power and knowing the radius
[00:08:51 - 00:08:53] or the diameter of our sprocket,
[00:08:53 - 00:08:57] we can work out what the theoretical max chain force might be.
[00:08:57 - 00:09:00] Yep, so that's answering one of your questions.
[00:09:00 - 00:09:04] And if you're unsure how to do that chain tension calculation,
[00:09:04 - 00:09:06] there is an example for, I think,
[00:09:06 - 00:09:08] a different kind of hydraulic sprocket
[00:09:08 - 00:09:10] that we've kind of done on the past, right?
[00:09:10 - 00:09:13] But as engineers, do you think
[00:09:13 - 00:09:14] that that's all good just to say?
[00:09:14 - 00:09:16] Yep, I trust my manager,
[00:09:16 - 00:09:18] they've definitely side to big enough motor.
[00:09:20 - 00:09:21] People are shaking their heads, right?
[00:09:21 - 00:09:25] So a second check, a sanity check for you
[00:09:25 - 00:09:28] to do as engineering designer would be to actually work out
[00:09:28 - 00:09:32] how much force would be required to pull,
[00:09:32 - 00:09:35] to pull one of these laser-key-we-carts
[00:09:35 - 00:09:36] up this left tool, right?
[00:09:37 - 00:09:40] And hopefully that chain,
[00:09:40 - 00:09:42] that tension force that's required to pull it up
[00:09:42 - 00:09:44] is less than this tension force
[00:09:44 - 00:09:47] that you've calculated using the max.
[00:09:47 - 00:09:49] So yeah, you wanna probably say,
[00:09:49 - 00:09:50] make sure that the motor's big enough
[00:09:50 - 00:09:53] is the calculation and I'm happy
[00:09:53 - 00:09:55] that it is adequately sized.
[00:09:55 - 00:09:58] If it's not, then you're gonna have to say,
[00:09:58 - 00:10:00] we're gonna take a bigger motor.
[00:10:00 - 00:10:04] Yep, cool, all good, all right, so.
[00:10:05 - 00:10:15] Yeah, would you not also be able to put a smaller sprocket on?
[00:10:15 - 00:10:20] So the sprocket size is defined, right?
[00:10:20 - 00:10:25] So we should just, in this case, like you could,
[00:10:25 - 00:10:26] but there wouldn't be any benefit
[00:10:26 - 00:10:31] in changing that sprocket size, yeah?
[00:10:31 - 00:10:35] So the main thought is,
[00:10:35 - 00:10:39] similar to what we were talking today about slip couplings,
[00:10:39 - 00:10:40] what we want to happen,
[00:10:40 - 00:10:41] this is a nice possible lead-in
[00:10:41 - 00:10:45] but we're gonna kinda talk about our clutches.
[00:10:45 - 00:10:48] If for some reason that cart got stuck,
[00:10:48 - 00:10:50] then we can imagine that the torque,
[00:10:50 - 00:10:52] that or the torque that's gonna be applied to,
[00:10:52 - 00:10:54] your sprocket and that's the chain force
[00:10:54 - 00:10:58] is gonna skyrocket as it kind of screams to a hulk, right?
[00:11:00 - 00:11:02] And so that's gonna reach a maximum.
[00:11:02 - 00:11:05] And then ideally, we've said that we wanna have
[00:11:05 - 00:11:07] some sort of a clutch,
[00:11:08 - 00:11:11] attached to our gearbox assembly
[00:11:11 - 00:11:14] so that it starts slipping rather than
[00:11:14 - 00:11:16] something exploding and braiding,
[00:11:16 - 00:11:19] probably just sharing a key, but yeah?
[00:11:19 - 00:11:27] So that is kinda what's covering their aspect of it.
[00:11:27 - 00:11:28] I don't know if there's any benefit
[00:11:28 - 00:11:30] to change the sprocket size.
[00:11:30 - 00:11:32] We could change the sprocket size
[00:11:32 - 00:11:34] to change the chain tension
[00:11:34 - 00:11:36] and then change the loading on our system,
[00:11:36 - 00:11:38] but that's kinda outside of the scope
[00:11:38 - 00:11:40] of what our specific assignment is.
[00:11:40 - 00:11:42] So in my mind, that would just be extra work
[00:11:43 - 00:11:47] for no real gain, yeah?
[00:11:47 - 00:11:49] Happy real fair answer.
[00:11:49 - 00:12:00] Other questions that everyone has?
[00:12:00 - 00:12:01] Great question.
[00:12:01 - 00:12:03] Let's talk about clutch stuff.
[00:12:04 - 00:12:05] So,
[00:12:06 - 00:12:08] again, the source of truth is the assignment,
[00:12:08 - 00:12:10] so I'll just use that.
[00:12:10 - 00:12:11] But what we can see,
[00:12:12 - 00:12:14] if we read our,
[00:12:16 - 00:12:18] where is it talk about the clutch?
[00:12:19 - 00:12:20] We see here an overload,
[00:12:20 - 00:12:23] something clutch will need to be scoped
[00:12:24 - 00:12:27] to go between the gearbox and the output shaft
[00:12:27 - 00:12:29] on the universal and the universal draft shaft.
[00:12:29 - 00:12:32] So then here.
[00:12:32 - 00:12:34] This purpose is to predict components
[00:12:34 - 00:12:37] if the system jams unexpectedly,
[00:12:37 - 00:12:39] as well as to protect components from shock loads
[00:12:39 - 00:12:43] that occur sometimes as the carriages engage with the chain.
[00:12:43 - 00:12:48] And if we look at what our outline of proposed tasks are,
[00:12:49 - 00:12:51] we can see that bullet point
[00:12:53 - 00:12:54] last two,
[00:12:54 - 00:12:57] well, second to last and third to last bullet points.
[00:12:57 - 00:12:58] Say that we need to,
[00:12:58 - 00:12:59] I'll here we go,
[00:12:59 - 00:13:02] undertake clutch calculations and show what options
[00:13:02 - 00:13:04] fit the available space.
[00:13:04 - 00:13:06] Present your results in such a way
[00:13:06 - 00:13:09] to enable someone to decide a suitably sized clutch
[00:13:09 - 00:13:13] and give a recommendation on what you think would be suitable.
[00:13:13 - 00:13:14] And you'll have to also specify
[00:13:14 - 00:13:17] what actuation force will allow the clutch
[00:13:17 - 00:13:20] to slip at just over the maximum torque.
[00:13:20 - 00:13:22] And then again,
[00:13:22 - 00:13:23] that next one is about the spring,
[00:13:23 - 00:13:25] which we'll sort of talk about.
[00:13:25 - 00:13:28] All right, so if we go back to my electric slides,
[00:13:29 - 00:13:33] I'll skip that bit there and go to this.
[00:13:33 - 00:13:35] We can see that this was the main slide
[00:13:35 - 00:13:38] that we sort of said gives us all the information
[00:13:38 - 00:13:42] about designing clutches that we thought would be useful.
[00:13:42 - 00:13:44] So I'll chuck that on one slide,
[00:13:44 - 00:13:47] have my page on the other.
[00:13:47 - 00:13:49] And so, generally speaking,
[00:13:49 - 00:13:51] just to check your understanding,
[00:13:51 - 00:13:55] the torque that is transmitted by a clutch
[00:13:56 - 00:14:03] is a function of what?
[00:14:03 - 00:14:05] We can assume it's uniform wear
[00:14:05 - 00:14:07] or we can assume it's uniform pressure.
[00:14:07 - 00:14:11] But both of those use the same parameters
[00:14:11 - 00:14:18] or variables in working out that calculation, right?
[00:14:18 - 00:14:19] So what are they?
[00:14:19 - 00:14:20] You're all going at one scan,
[00:14:20 - 00:14:22] you always do the science-friendly tricky.
[00:14:23 - 00:14:29] Here you're talking over each other.
[00:14:29 - 00:14:30] What parameters can we change?
[00:14:30 - 00:14:34] There will change the amount of torque a...
[00:14:35 - 00:14:36] Yep.
[00:14:36 - 00:14:40] So we've got the inner diameter.
[00:14:41 - 00:14:45] We've got the outer diameter.
[00:14:45 - 00:14:57] And that's just that right, that's what else can we change?
[00:14:57 - 00:15:01] So we've picked off this variable and this variable.
[00:15:01 - 00:15:06] What else is in the equation?
[00:15:06 - 00:15:09] Oh man, we're really having the next standard
[00:15:09 - 00:15:11] for a sake of guys who've grown so quickly.
[00:15:11 - 00:15:12] So you're almost fourth years,
[00:15:12 - 00:15:14] we're just like, we do not say anything
[00:15:14 - 00:15:15] unless it's worth marks.
[00:15:17 - 00:15:18] Friction, yeah.
[00:15:18 - 00:15:23] So we've got the coefficient of friction, right?
[00:15:23 - 00:15:26] Which is based on the material.
[00:15:26 - 00:15:29] And the other thing, capital worth stands for,
[00:15:29 - 00:15:32] yeah, the actuation force.
[00:15:33 - 00:15:34] Yeah?
[00:15:34 - 00:15:35] Cool.
[00:15:35 - 00:15:40] So knowing that, we're going to have to probably narrow down
[00:15:40 - 00:15:42] the amount of variables that we can adjust
[00:15:42 - 00:15:45] if we're going to make some sort of plot that we can use
[00:15:45 - 00:15:50] to size a clutch based on a certain material wrap.
[00:15:51 - 00:15:53] So what I would envision,
[00:15:53 - 00:15:55] but there's not one way to do this,
[00:15:55 - 00:15:57] there's kind of two ways to do it.
[00:15:57 - 00:16:00] One way would be that you could plot the torque
[00:16:00 - 00:16:03] that is transmitted by the clutch.
[00:16:03 - 00:16:06] And then you know that there's some limit
[00:16:06 - 00:16:09] that you're trying to achieve.
[00:16:09 - 00:16:12] And maybe there'll be different amounts of torque
[00:16:13 - 00:16:18] based on different materials or different sizes, right?
[00:16:18 - 00:16:20] So what would possibly be a variable
[00:16:20 - 00:16:22] that we could change down the bottom?
[00:16:22 - 00:16:24] Well, it could be, you could have friction,
[00:16:24 - 00:16:25] but that's kind of tricky
[00:16:25 - 00:16:27] because you're just going to get specific data points
[00:16:27 - 00:16:29] for different materials.
[00:16:29 - 00:16:32] But if, for example, you had locked in an inner
[00:16:32 - 00:16:35] or an outer diameter and then changed the other,
[00:16:35 - 00:16:38] then you would be able to get like a continuous curve
[00:16:39 - 00:16:40] that shows that, right?
[00:16:40 - 00:16:44] Obviously, if you're changing diameter
[00:16:44 - 00:16:47] and it will alter, you'd have to kind of lock in
[00:16:47 - 00:16:48] the other variables, right?
[00:16:48 - 00:16:51] And so in that, that's where you'd have to kind of
[00:16:51 - 00:16:53] state what your assumptions are.
[00:16:53 - 00:16:55] You might put multiple lines on one plot.
[00:16:56 - 00:16:59] This is where the ball is in your court,
[00:16:59 - 00:17:01] but other way that you could do it,
[00:17:01 - 00:17:05] or you could do both, would be instead to rearrange
[00:17:05 - 00:17:08] for possibly the actuation force
[00:17:08 - 00:17:10] and know that torque is a specified limit
[00:17:10 - 00:17:12] that you put into your equation.
[00:17:12 - 00:17:14] And again, you can get some plots.
[00:17:14 - 00:17:16] I don't know.
[00:17:16 - 00:17:16] Maybe they look this way.
[00:17:16 - 00:17:19] I don't know what the variable was down here.
[00:17:19 - 00:17:21] So I don't know what the lines look like,
[00:17:21 - 00:17:25] but what you might say is, okay, I pick this one here
[00:17:25 - 00:17:32] and talk about that as my recommendation.
[00:17:32 - 00:17:36] Questions from that?
[00:17:36 - 00:17:38] So you can see here that you could pick, okay,
[00:17:38 - 00:17:40] if I assume that maybe you want to compare,
[00:17:40 - 00:17:43] what difference does it make if I have cast iron on cast iron
[00:17:43 - 00:17:47] as my pair of plates versus wider space stars on metal?
[00:17:47 - 00:17:50] Obviously, you'd probably not choose the space stars one now,
[00:17:50 - 00:17:53] that sort of not that recommended
[00:17:53 - 00:17:55] as an engineering material anymore,
[00:17:55 - 00:17:57] especially the dust you can imagine
[00:17:57 - 00:18:00] that's coming out of your clutch if it is slipping.
[00:18:00 - 00:18:03] You can see that there are different coefficients
[00:18:03 - 00:18:05] of friction, so you might want to show those.
[00:18:06 - 00:18:12] Yeah, does that clarify what you need to do
[00:18:12 - 00:18:13] for the clutch?
[00:18:13 - 00:18:15] Citium, so we've given you some constraints,
[00:18:15 - 00:18:17] like the size, so obviously you can't just
[00:18:17 - 00:18:19] pick an outer diameter to be like one meter
[00:18:19 - 00:18:21] and have this tiny doughnut.
[00:18:23 - 00:18:30] Yeah, any other questions about that or is that clear enough?
[00:18:30 - 00:18:33] So you might also want to check that the allowable pressure
[00:18:33 - 00:18:36] is it's acceptable for the given situation that you have,
[00:18:36 - 00:18:39] and obviously that allowable pressure is using this area
[00:18:40 - 00:18:42] of your clutch, the inner and outer diameter
[00:18:42 - 00:18:44] and the actuation force that's required, right?
[00:18:45 - 00:18:50] Also the area given us pressure.
[00:18:50 - 00:18:52] Effie, I'm assuming we're happy.
[00:18:52 - 00:18:54] I don't know yet.
[00:18:54 - 00:19:02] Yeah, good.
[00:19:02 - 00:19:03] 202.
[00:19:03 - 00:19:06] Yeah, just here, fortunately, you're being moment diagrams.
[00:19:06 - 00:19:08] Exactly the same as air may turn to,
[00:19:09 - 00:19:11] but make sure you do it for the front plane
[00:19:11 - 00:19:12] and for the top plane.
[00:19:14 - 00:19:23] Even one of them might have nothing happening.
[00:19:23 - 00:19:27] This is from last term and I remember saying,
[00:19:27 - 00:19:29] don't quote me, I'm not sure which ones
[00:19:29 - 00:19:32] have they upside down because there is like a,
[00:19:32 - 00:19:34] probably something roughly like that.
[00:19:35 - 00:19:37] Obviously there's no values on that,
[00:19:37 - 00:19:39] but you've got a point load in between two fixed points.
[00:19:39 - 00:19:42] So that's for your standard loading case, right?
[00:19:42 - 00:19:45] And then for our moment,
[00:19:48 - 00:19:50] secondary moment, and there's an example
[00:19:50 - 00:19:52] that kind of shows what that would look like on the south,
[00:19:52 - 00:19:53] right?
[00:19:53 - 00:19:55] And then you have to work at how you combine those,
[00:19:55 - 00:19:57] which is sort of what the step three says
[00:19:57 - 00:19:59] on the frequently asked questions, right?
[00:19:59 - 00:20:03] So it says, don't try do everything at once
[00:20:03 - 00:20:06] and then panic and then set on it for four weeks
[00:20:06 - 00:20:11] and then panic real hard the night before.
[00:20:11 - 00:20:12] Nope, no, these are all really good questions
[00:20:12 - 00:20:14] and we're going good for time.
[00:20:14 - 00:20:17] So I might quickly keep things kind of moving.
[00:20:17 - 00:20:20] So obviously some people have done the,
[00:20:21 - 00:20:25] for everybody diagram and at least have some forces,
[00:20:25 - 00:20:28] either their moment and their talk,
[00:20:28 - 00:20:31] that their shaft needs to transmit.
[00:20:31 - 00:20:35] When you're using the ASME shaft calculation equation
[00:20:35 - 00:20:40] or similar, you will need to know E, I believe, right?
[00:20:47 - 00:20:50] You'll need to define a material for your design at some point,
[00:20:50 - 00:20:51] right?
[00:20:51 - 00:20:56] And one thing to note is that most steels
[00:20:56 - 00:20:59] have a very similar elastic modulus.
[00:20:59 - 00:21:01] It's roughly 200 GPA.
[00:21:01 - 00:21:04] So if you're not someone who likes to commit
[00:21:04 - 00:21:05] to a material straight away,
[00:21:05 - 00:21:08] then that can be a useful kind of value to use
[00:21:08 - 00:21:14] if you are gonna try and calculate any defletions, right?
[00:21:14 - 00:21:17] From there, my recommendation would probably be
[00:21:17 - 00:21:21] to use a medium density carbon steel for your shaft
[00:21:21 - 00:21:24] has good strength toughness and wear resistance.
[00:21:24 - 00:21:28] You could in theory use whatever material you want.
[00:21:28 - 00:21:30] Just make sure that you state it and why.
[00:21:31 - 00:21:34] So for example, if you really wanted to just use mild steel,
[00:21:34 - 00:21:35] you could use it.
[00:21:36 - 00:21:38] If you think that it's gonna be appropriate,
[00:21:38 - 00:21:40] obviously those kind of values
[00:21:40 - 00:21:42] with the different types of materials
[00:21:42 - 00:21:44] which kind of just change what the size
[00:21:44 - 00:21:46] of your shaft is gonna be.
[00:21:46 - 00:21:50] We see some more information about hot and cold-rolled options
[00:21:51 - 00:21:53] and the advantages that they have.
[00:21:53 - 00:21:56] So cold-rolled tending to be more expensive,
[00:21:56 - 00:22:01] but easier to machine.
[00:22:01 - 00:22:05] Oh, so that's just a common that people in the past
[00:22:05 - 00:22:07] have kind of quammed about.
[00:22:07 - 00:22:10] So just kind of clearing that there,
[00:22:10 - 00:22:15] hopefully before you get to it.
[00:22:15 - 00:22:17] So there, if you've got other questions,
[00:22:17 - 00:22:19] maybe we'll just go through our kind of design
[00:22:19 - 00:22:21] for springs now.
[00:22:21 - 00:22:22] The reason that we're kind of covering this now
[00:22:22 - 00:22:25] is because we do have a geese lecture happening
[00:22:25 - 00:22:29] in two weeks time, early May.
[00:22:30 - 00:22:33] So that's kind of bumped where this material needs to be.
[00:22:33 - 00:22:37] Because you do need to do the design of the spring
[00:22:37 - 00:22:38] in your assignment.
[00:22:38 - 00:22:44] So we can see here complete scoping calculations.
[00:22:45 - 00:22:48] I'll spring to determine the nominal spring parameters,
[00:22:48 - 00:22:51] including the chosen material wire diameter,
[00:22:51 - 00:22:54] the number of coils in spring constant.
[00:22:54 - 00:22:58] And show that the spring will not be coil bound.
[00:22:58 - 00:23:02] And then the results will be put in a compression spring
[00:23:03 - 00:23:06] manufacturing form.
[00:23:06 - 00:23:09] So what we can see, this is a PDF that is also on learn
[00:23:09 - 00:23:10] for you guys.
[00:23:10 - 00:23:13] And it gives a pretty big overview on guiding you
[00:23:13 - 00:23:16] on how you would design for springs.
[00:23:16 - 00:23:18] So we'll see the lecture summary there.
[00:23:18 - 00:23:20] We'll kind of go about it more generally.
[00:23:20 - 00:23:22] We'll talk about our specific kind of tension
[00:23:22 - 00:23:25] and compression springs, which are the main
[00:23:25 - 00:23:28] focus of the lecture content.
[00:23:28 - 00:23:31] And then have some other discussions.
[00:23:31 - 00:23:34] There's also a work example at the bottom.
[00:23:34 - 00:23:36] So you see that spring's going to come in a range
[00:23:36 - 00:23:38] of shapes and sizes.
[00:23:38 - 00:23:42] And broadly speaking, they are defined as any passive element
[00:23:42 - 00:23:46] which deflects elastically under load.
[00:23:46 - 00:23:49] So as an engineer, you may use these to exert a force,
[00:23:49 - 00:23:51] provide flexibility.
[00:23:51 - 00:23:54] You might use it to store energy, isolate vibration,
[00:23:54 - 00:23:57] or to actually measure forces, if you know,
[00:23:57 - 00:24:01] the properties of the spring that you're using.
[00:24:01 - 00:24:05] Broadly, you have wire springs, flat springs, air springs,
[00:24:05 - 00:24:08] and then some miscellaneous ones.
[00:24:08 - 00:24:11] And so we'll be mainly focusing on the wire springs.
[00:24:12 - 00:24:17] So generally speaking, when people are designing springs
[00:24:17 - 00:24:22] to be used in machinery, they want to make things as cheap
[00:24:22 - 00:24:23] as possible.
[00:24:23 - 00:24:29] And so the way to do this is to stress the spring material
[00:24:29 - 00:24:31] to its upper limit, not over the limit
[00:24:31 - 00:24:34] during the deflection kind of process.
[00:24:34 - 00:24:37] So what we see here often, we'll have remembered this from,
[00:24:37 - 00:24:41] I don't know, NCAA like little two or something.
[00:24:41 - 00:24:44] If it was KX and having this linear kind of region
[00:24:44 - 00:24:46] where we have our spring constant.
[00:24:47 - 00:24:48] So we can see there.
[00:24:48 - 00:24:52] And obviously if we apply two times the force
[00:24:52 - 00:24:56] on that linear region, we would get two times the deflection.
[00:24:57 - 00:25:02] So there we see that nice linear equation for our springs
[00:25:04 - 00:25:07] with our applied force extension and spring constant.
[00:25:07 - 00:25:09] And then we have a similar formula
[00:25:09 - 00:25:12] if we are trying to work out the spring rate
[00:25:12 - 00:25:13] for our torsion springs.
[00:25:13 - 00:25:16] So in this case, the angular rotation
[00:25:16 - 00:25:21] and the spring rate being the two kind of variables.
[00:25:21 - 00:25:27] In this case, we have different units for our spring rate.
[00:25:27 - 00:25:30] So for everything else, it's not a spring.
[00:25:30 - 00:25:35] You can actually calculate what the spring constant is.
[00:25:36 - 00:25:40] And so an example of this might be if you just have
[00:25:40 - 00:25:43] some cylinder of material and you want to work out
[00:25:43 - 00:25:46] what spring constant is, we can see on here
[00:25:46 - 00:25:48] where our elastic module is being defined
[00:25:48 - 00:25:50] as stress over strain.
[00:25:50 - 00:25:53] And then if we develop these equations
[00:25:53 - 00:25:57] or dissect them further and then rearrange,
[00:25:58 - 00:26:01] we can work out our extension being our change
[00:26:01 - 00:26:03] in length of our strain.
[00:26:03 - 00:26:06] And then we can rearrange this equation
[00:26:06 - 00:26:10] to get that our spring constant is our elastic modules
[00:26:10 - 00:26:16] times by our area divided by our.
[00:26:16 - 00:26:19] So this is also something that if you're
[00:26:19 - 00:26:22] an mechanical student and you're not doing enemy 3-1-1,
[00:26:22 - 00:26:25] we do something similar when we look at altered connections
[00:26:25 - 00:26:28] with a clamped material in between,
[00:26:28 - 00:26:29] a bolted kind of joint.
[00:26:29 - 00:26:34] Actually does have this kind of elastic spring-like property
[00:26:34 - 00:26:38] that has to be considered when looking at the loading
[00:26:38 - 00:26:39] in those kind of environments.
[00:26:39 - 00:26:42] So the example of it is this here,
[00:26:42 - 00:26:47] which basically shows if you have a clamped material,
[00:26:47 - 00:26:50] which is this outer spring here.
[00:26:50 - 00:26:51] And then you have a bolt,
[00:26:51 - 00:26:54] which is the inner tension spring,
[00:26:54 - 00:26:56] that as the bolt is tightened,
[00:26:56 - 00:27:00] the big material will have a small amount of compression,
[00:27:00 - 00:27:03] which then means as your bolt is slightly loosened,
[00:27:03 - 00:27:07] there's joint extension that kind of happens.
[00:27:07 - 00:27:11] And there that obviously that's not the focus
[00:27:11 - 00:27:14] of today's lecture, but it does show some springs,
[00:27:14 - 00:27:18] which I do have a few more examples of.
[00:27:19 - 00:27:22] Cool, so wire springs are what you're going to need to be,
[00:27:22 - 00:27:25] designing for our assignment,
[00:27:25 - 00:27:26] an only helically wound,
[00:27:26 - 00:27:28] can be wound in either direction,
[00:27:28 - 00:27:32] and there can be different kind of profiles,
[00:27:32 - 00:27:35] but typically rounders the most cost-effective
[00:27:35 - 00:27:37] with our square or flattened springs,
[00:27:37 - 00:27:40] generally being more expensive.
[00:27:40 - 00:27:44] The wire is frequently very high in strength,
[00:27:44 - 00:27:49] generally speaking approximately 1600 to 2000 megapascals.
[00:27:50 - 00:27:53] And we'll see some of the main kind of equations
[00:27:53 - 00:27:56] that we can use to calculate the stress,
[00:27:56 - 00:27:58] and now kind of here, look how springs.
[00:27:58 - 00:28:01] So this one here is from Shigglie's textbook.
[00:28:01 - 00:28:03] And we can see that the next shear stress
[00:28:03 - 00:28:07] is determined by this equation here.
[00:28:07 - 00:28:11] We have this wall correction factor,
[00:28:11 - 00:28:14] which is typically between one and 1.25,
[00:28:14 - 00:28:16] and what information about that factor can be found.
[00:28:16 - 00:28:19] In the textbook, but if you assume,
[00:28:19 - 00:28:21] whatever you assume, just make sure that it's clear,
[00:28:21 - 00:28:23] then we've got our applied load,
[00:28:23 - 00:28:27] our mean coil diameter, and our wire diameter.
[00:28:27 - 00:28:29] You'll see that those are all variables
[00:28:29 - 00:28:33] that we have asked you to define for your assignment.
[00:28:33 - 00:28:36] And we can see here that caution
[00:28:36 - 00:28:40] is the main cause of the shear stress in our wire.
[00:28:41 - 00:28:46] So if we look at our stresses in a helical spring,
[00:28:46 - 00:28:47] some people might just think,
[00:28:47 - 00:28:49] oh, it's the spring, you're compressing it.
[00:28:49 - 00:28:50] The spring is just bending.
[00:28:51 - 00:28:55] It's sort of like sometimes what people intuitively
[00:28:55 - 00:28:57] might think is happening.
[00:28:57 - 00:29:00] But actually, what is happening in our wire
[00:29:00 - 00:29:04] as our spring in total is compressed,
[00:29:04 - 00:29:08] is that there is a torsion where our wire
[00:29:08 - 00:29:12] is actually twisting as it is compressed.
[00:29:12 - 00:29:16] And so these diagrams here basically outline
[00:29:16 - 00:29:21] what considerations, the different types of loading have
[00:29:21 - 00:29:24] on our actually loaded helical spring.
[00:29:24 - 00:29:29] So what we can see here is that B is the free body diagram
[00:29:29 - 00:29:34] for direct shear stress and A is for pure torsional stress.
[00:29:34 - 00:29:36] And then we can see,
[00:29:36 - 00:29:40] is the resultant of the direct and torsional shear stress.
[00:29:40 - 00:29:44] And D is the resultant of direct torsional and curvature
[00:29:44 - 00:29:45] shear stress.
[00:29:45 - 00:29:49] So we can see that because of this shear stress,
[00:29:49 - 00:29:52] we end up getting a maximum stress value
[00:29:52 - 00:29:57] on the often on the inside edge of our spring wrap.
[00:29:58 - 00:29:59] So the spring was to fail.
[00:29:59 - 00:30:03] This is pretty much where we would expect it to fail.
[00:30:03 - 00:30:07] If you see something that was going to break in fatigue
[00:30:07 - 00:30:11] from repeated loading, there would often be a nucleation point
[00:30:11 - 00:30:14] where there's kind of maximum stress value.
[00:30:14 - 00:30:20] So right, we can see here that direct shear stress
[00:30:20 - 00:30:22] has a very small kind of consideration
[00:30:22 - 00:30:26] compared to the torsion.
[00:30:26 - 00:30:26] Cool.
[00:30:26 - 00:30:31] So once you've worked out that your spring stress
[00:30:31 - 00:30:34] is going to be safe, the other equation
[00:30:34 - 00:30:38] that you can use is working out what the spring constant will be.
[00:30:38 - 00:30:42] And again, we can see that we have this equation here,
[00:30:42 - 00:30:45] which incorporates our shear modulus and the coils
[00:30:45 - 00:30:48] since line diameter of our spring,
[00:30:48 - 00:30:53] along with our wired diameter and in the number of coils.
[00:30:54 - 00:30:59] So we can work out this for our shear modulus.
[00:30:59 - 00:31:04] I'm using this equation here and obviously,
[00:31:04 - 00:31:06] if you know what your material is,
[00:31:06 - 00:31:07] you will know the Poisson's ratio,
[00:31:07 - 00:31:12] but generally if it's still an approximation of 0.3 is okay.
[00:31:13 - 00:31:16] And so what we can see here is that if we wanted to stiffen
[00:31:16 - 00:31:19] or increase our spring constant, there's a few things
[00:31:19 - 00:31:20] that we can do.
[00:31:20 - 00:31:25] We could increase our wired diameter, we could decrease the number,
[00:31:25 - 00:31:29] decrease this coil, central line,
[00:31:29 - 00:31:32] or decrease the number of coils.
[00:31:32 - 00:31:34] Obviously taking into account the difference
[00:31:34 - 00:31:36] and the powers of these values,
[00:31:36 - 00:31:38] if you wanted to have the biggest effect
[00:31:38 - 00:31:43] in changing the wire diameter would make a bigger difference
[00:31:44 - 00:31:48] for the same change, change in the value.
[00:31:49 - 00:31:53] But obviously, wire diameter might be kind of predefined
[00:31:53 - 00:31:57] or we can't just get wire and any kind of diameter.
[00:31:57 - 00:32:00] We kind of talked about that with our standard sizes previously.
[00:32:01 - 00:32:05] So for our wire compression springs,
[00:32:05 - 00:32:08] we'll see that they're round with space in between them.
[00:32:08 - 00:32:11] There are three types of ends.
[00:32:11 - 00:32:15] So you can have open, we've got a bunch of springs here.
[00:32:15 - 00:32:17] And at open you can have closed
[00:32:17 - 00:32:22] where you can have ground where the edges ground flat
[00:32:23 - 00:32:26] and we can see some examples of that there
[00:32:26 - 00:32:27] on the document camera.
[00:32:28 - 00:32:33] So again, both of these are actually being ground flat.
[00:32:36 - 00:32:38] So there's this one here actually,
[00:32:38 - 00:32:42] you can see the machining marks on the diagrams
[00:32:42 - 00:32:44] and the lecture slides.
[00:32:44 - 00:32:49] I think show you the differences that you can have.
[00:32:49 - 00:32:52] So closing ground closed but not ground
[00:32:52 - 00:32:53] or completely open.
[00:32:55 - 00:32:57] Life coils are those that have space in between them.
[00:32:57 - 00:33:00] So obviously if you have a ground end
[00:33:00 - 00:33:04] or a closed end ground or a closed end,
[00:33:04 - 00:33:07] then you wouldn't count this as one of your coils.
[00:33:08 - 00:33:12] If your compression springs are too long, they may buckle.
[00:33:12 - 00:33:14] So use the design to have to kind of make sure
[00:33:14 - 00:33:18] that this is a consideration that has been addressed.
[00:33:18 - 00:33:21] And obviously we've kind of touched on our buckling
[00:33:21 - 00:33:24] kind of equations but the same thing can kind of happen
[00:33:24 - 00:33:27] and make sure you understand what the inc conditions
[00:33:27 - 00:33:29] of your springs are again,
[00:33:29 - 00:33:34] impact the type of a wing or the likelihood of buckling
[00:33:34 - 00:33:36] or those inc condition constants.
[00:33:36 - 00:33:40] And so obviously here is that here we have kind of worked out
[00:33:41 - 00:33:42] terms of its stability.
[00:33:43 - 00:33:47] If we have plotting, we plot these critical values
[00:33:47 - 00:33:51] of if over L0 over D and our relative deflection
[00:33:51 - 00:33:52] we can kind of actually work out
[00:33:52 - 00:34:01] where our compression spring is stable or not.
[00:34:01 - 00:34:03] Cool, so what we can see here,
[00:34:03 - 00:34:05] there's just as well as what's happening
[00:34:05 - 00:34:08] as our springers can compress.
[00:34:08 - 00:34:11] And at the bottom here we can see that all the coils
[00:34:11 - 00:34:13] are touching each other, they're bound together.
[00:34:13 - 00:34:17] And this is that coil bound situation
[00:34:17 - 00:34:22] that we want to avoid and our assignment, right?
[00:34:22 - 00:34:24] So obviously if you were thinking about plotting
[00:34:24 - 00:34:27] the stiffness or the force and deflection,
[00:34:27 - 00:34:31] once it's coil bound, a lot more force is needed
[00:34:31 - 00:34:35] to not get much more deflection, yeah?
[00:34:35 - 00:34:36] And then we just see some quirky things
[00:34:36 - 00:34:39] that people have done making
[00:34:40 - 00:34:43] compression springs, be tension springs essentially.
[00:34:43 - 00:34:45] That's this one on the right here,
[00:34:45 - 00:34:47] but we can do kind of fun things
[00:34:47 - 00:34:51] with these nested configurations.
[00:34:52 - 00:34:54] We have some notes here on surging in springs,
[00:34:54 - 00:34:57] which is something that you want to avoid,
[00:34:57 - 00:35:01] both transverse waves and compressor waves may exist.
[00:35:01 - 00:35:05] And to avoid this, you want to kind of avoid
[00:35:07 - 00:35:10] being having the loading occur
[00:35:10 - 00:35:13] near the critical frequency, which is when we'll get
[00:35:16 - 00:35:19] the thing to 20 times in the oscillatory motion.
[00:35:20 - 00:35:22] So the design should have ensure
[00:35:22 - 00:35:24] that the critical frequency is 15 to 20 times
[00:35:24 - 00:35:26] of any oscillatory motion.
[00:35:26 - 00:35:27] So you're pretty much meaning to make sure
[00:35:27 - 00:35:30] that your system is not exciting.
[00:35:30 - 00:35:36] The springs in causing surging in your system.
[00:35:36 - 00:35:40] So we'll see an example here of that failure.
[00:35:40 - 00:35:42] And we can see that a very typical failure
[00:35:42 - 00:35:47] of having it on a 45 degree angle that we see in sheer,
[00:35:49 - 00:35:50] being the main cause.
[00:35:51 - 00:35:53] So as we sort of touched on,
[00:35:53 - 00:35:56] if a fatigue failure was to happen in a spring,
[00:35:56 - 00:36:01] it's often going to occur at that nucleation point
[00:36:01 - 00:36:04] where the stress is the highest.
[00:36:05 - 00:36:07] So we can see here, my springs undergo no more
[00:36:07 - 00:36:09] than several thousand cycles in the lifetime.
[00:36:09 - 00:36:11] Other springs such as the valve spring
[00:36:11 - 00:36:14] and the car mass undergo many millions of cycles
[00:36:14 - 00:36:17] without failure, they must therefore be designed
[00:36:17 - 00:36:20] for infinite life using fatigue design methods.
[00:36:20 - 00:36:24] And then here we can see that nucleation point
[00:36:24 - 00:36:28] will have our crack kind of propagating slowly
[00:36:28 - 00:36:35] before our kind of final failure brittle failure at the end.
[00:36:35 - 00:36:39] So again, four springs, one method that they can use
[00:36:39 - 00:36:41] to make them a little bit more resistant.
[00:36:41 - 00:36:45] Resistant to fatigue is to do shot peening on the surface,
[00:36:45 - 00:36:49] to put compressive stresses into material surface
[00:36:49 - 00:36:53] and avoid at a possible kind of nucleation point
[00:36:53 - 00:36:58] from being open and readily available to propagate a crack.
[00:36:58 - 00:37:00] So pretty much shot peening is like shooting lots
[00:37:00 - 00:37:05] of little balls at the material surface of your spring.
[00:37:06 - 00:37:09] So I'm not sure exactly what it looks like.
[00:37:09 - 00:37:12] Maybe shot peening had happened in this spring here
[00:37:12 - 00:37:15] but it's a nice massive spring
[00:37:15 - 00:37:18] that we wanted to showcase in the little she notes.
[00:37:19 - 00:37:24] So here we see our compressive springs' classification form.
[00:37:24 - 00:37:28] So if you were to actually get one of these manufactured,
[00:37:28 - 00:37:30] this is the kind of thing that you would need to fill out.
[00:37:30 - 00:37:33] So given details about the diameters,
[00:37:33 - 00:37:38] what our loads are desired for what kind of displacements
[00:37:38 - 00:37:43] and also what the ends and direction of our spring that's right.
[00:37:43 - 00:37:47] So this is the kind of thing that has been coming there
[00:37:47 - 00:37:51] on the assignment information.
[00:37:51 - 00:37:55] We can see we do have that exact specification form
[00:37:55 - 00:38:02] for you to fill out following your calculations.
[00:38:02 - 00:38:03] Cool.
[00:38:03 - 00:38:06] So in terms of how you might go about actually design the spring,
[00:38:06 - 00:38:10] surprise surprise that sometimes can be an iterative process.
[00:38:10 - 00:38:11] The first thing you'll need to do is define
[00:38:11 - 00:38:14] what specification you need and work out
[00:38:14 - 00:38:16] what spring constant you need.
[00:38:16 - 00:38:20] Then you'll use the equations on seven, eight and 25
[00:38:20 - 00:38:23] to iterate between the parameters of interest.
[00:38:23 - 00:38:25] So some of them you might lock in or make assumptions
[00:38:25 - 00:38:27] for in the first instance.
[00:38:27 - 00:38:29] And then you'll probably make some sort of table
[00:38:29 - 00:38:34] that kind of results and giving you the values of interest.
[00:38:34 - 00:38:35] So there's more than one way that you can do this.
[00:38:35 - 00:38:39] But we'll see an example below that kind of shows
[00:38:39 - 00:38:42] how you might do this.
[00:38:42 - 00:38:46] And then once you've got a combination of these variables
[00:38:46 - 00:38:49] or parameters for your spring that is acceptable,
[00:38:49 - 00:38:52] you'll lock it into the specification form
[00:38:52 - 00:38:54] that's been provided.
[00:38:54 - 00:38:56] So here we see an example that's looking
[00:38:56 - 00:39:01] at a compression spring for a mountain bike.
[00:39:01 - 00:39:04] And we can see that we have defined what we want to happen
[00:39:04 - 00:39:04] and win.
[00:39:04 - 00:39:07] And we've made some estimates about what kind of load
[00:39:07 - 00:39:13] is going to occur during what kind of displacement
[00:39:13 - 00:39:16] that we want in this case here.
[00:39:16 - 00:39:18] And so from this here, we can see that we've
[00:39:18 - 00:39:21] worked out with the rider on the rear wheel,
[00:39:21 - 00:39:24] what our loaders with the rider in place,
[00:39:24 - 00:39:27] and then when the spring is bottomed out,
[00:39:27 - 00:39:30] we've defined it as being 80 mil long.
[00:39:30 - 00:39:33] So using these kind of values, we can plot them
[00:39:33 - 00:39:36] and kind of visualize what is happening
[00:39:36 - 00:39:38] with the forces and the displacements
[00:39:38 - 00:39:41] that we want at these two points here.
[00:39:41 - 00:39:45] And so broadly speaking, we can then work out what
[00:39:45 - 00:39:48] we want our spring constant to be by using
[00:39:48 - 00:39:53] this plot of basically just doing the change in the force,
[00:39:53 - 00:39:57] based on the change in displacement of our spring.
[00:39:57 - 00:39:59] From there, we want to work out what the number of coils
[00:39:59 - 00:40:03] and the wire diameter and spring diameter are
[00:40:03 - 00:40:08] to achieve the desired kind of output that we want.
[00:40:08 - 00:40:13] And so we can work out our K, our spring constant using
[00:40:13 - 00:40:16] the noons from above.
[00:40:16 - 00:40:19] We can work out our sheer modulus using the equation
[00:40:19 - 00:40:21] that we had defined earlier.
[00:40:21 - 00:40:24] And then we can tabulate our options,
[00:40:24 - 00:40:28] looking at our different wire diameters in this case.
[00:40:28 - 00:40:31] We then can determine the number of coils that
[00:40:31 - 00:40:33] would be needed, what the diameter of our spring
[00:40:33 - 00:40:35] would be needed, and then what the shear stress
[00:40:35 - 00:40:37] and our spring is.
[00:40:37 - 00:40:39] So ideally, we want that shear stress not
[00:40:39 - 00:40:42] to be above what our maximum shear stress is
[00:40:42 - 00:40:44] for our spring.
[00:40:44 - 00:40:49] So then we can see that we also, from there,
[00:40:49 - 00:40:55] then we can work out what we think it is or what we want
[00:40:55 - 00:41:00] our spring to be in this case.
[00:41:00 - 00:41:04] So for tension springs, it's relatively similar process
[00:41:04 - 00:41:05] and reverse.
[00:41:05 - 00:41:08] And we can see that sometimes our tension springs
[00:41:08 - 00:41:11] have pre-tension applied for them so that all coils
[00:41:11 - 00:41:14] are in contact in the unstretched state.
[00:41:14 - 00:41:18] So if you go ahead to put springs on the trampoline,
[00:41:18 - 00:41:22] that's showing that pre-tensioning that has occurred.
[00:41:22 - 00:41:25] And it can be a little bit fiddly to get them all in place
[00:41:25 - 00:41:27] when that is occurring.
[00:41:27 - 00:41:29] So pre-lighters are required before the spring will even
[00:41:29 - 00:41:31] start to stretch.
[00:41:31 - 00:41:33] There are many types of in-detachments.
[00:41:33 - 00:41:38] I simply only have examples of the hook attachments.
[00:41:38 - 00:41:41] But we can see that the camera in a range of shapes and sizes
[00:41:41 - 00:41:45] and materials and have many similarities
[00:41:45 - 00:41:48] to our compression springs of them being
[00:41:48 - 00:41:51] able to be wound in either way.
[00:41:51 - 00:41:53] The difference is, though, obviously,
[00:41:53 - 00:42:00] is not a coil-bound consideration for our tension springs.
[00:42:00 - 00:42:01] And they do not suffer from buckling
[00:42:01 - 00:42:04] as they are not loaded actually.
[00:42:04 - 00:42:08] But obviously, if we apply too much force to the spring,
[00:42:08 - 00:42:11] then we do get some permanent deformation
[00:42:11 - 00:42:16] that is not desirable in our system.
[00:42:16 - 00:42:18] So we can see here, to increase the spring's stiffness,
[00:42:18 - 00:42:21] we can use the same equation as earlier on page 9.
[00:42:21 - 00:42:24] We can increase the wider diameter.
[00:42:24 - 00:42:27] We can reduce the spring diameter, or we
[00:42:27 - 00:42:31] can reduce the number of active coils or shortens spring.
[00:42:31 - 00:42:33] So we can see here, for completeness,
[00:42:33 - 00:42:36] there's some examples of what kind of ends you might have
[00:42:36 - 00:42:41] on a compression spring, as well as a similar specification
[00:42:41 - 00:42:43] sheet that you would need.
[00:42:43 - 00:42:45] And then here, we see the same kind of information
[00:42:45 - 00:42:48] for torsion springs, which we don't
[00:42:48 - 00:42:52] need to go into in detail.
[00:42:52 - 00:42:54] Yeah, often you only want your spring
[00:42:54 - 00:42:57] to be operating on relatively small angles.
[00:42:57 - 00:43:01] You don't want to have to wind up your spring multiple kind
[00:43:01 - 00:43:08] of revolutions to get the type of force that you want.
[00:43:08 - 00:43:12] So I'm just going to basically leave that there.
[00:43:12 - 00:43:16] As red, you can see that we have similar or some
[00:43:16 - 00:43:20] other less kind of equations for our torsions spring calculations
[00:43:20 - 00:43:26] for both our spring constant, our maximum stress.
[00:43:26 - 00:43:28] So we can have helical torsions, springs, viral torsions,
[00:43:29 - 00:43:36] or other examples, which are all kind of illustrated in the diagrams.
[00:43:36 - 00:43:39] And again, we see our specifications sheet that
[00:43:39 - 00:43:42] would be required if you were to approach a manufacturer.
[00:43:42 - 00:43:45] Now, generally speaking, I've talked to a few still.
[00:43:45 - 00:43:47] Well, spring manufacturers, they always
[00:43:47 - 00:43:51] encourage early kind of communication to them.
[00:43:51 - 00:43:54] Because although, yes, you have the power
[00:43:54 - 00:43:57] to fill out the sheet, often there are kind of new answers
[00:43:57 - 00:44:00] to get the best result in the cheapest kind of way.
[00:44:00 - 00:44:03] So if you are an industry and kind of have this kind of requirement
[00:44:03 - 00:44:05] to specify a spring, it's definitely
[00:44:05 - 00:44:09] worth talking to the manufacturer before just giving them
[00:44:09 - 00:44:13] the specification sheet and hoping for the best.
[00:44:13 - 00:44:15] So follow us or the end of it, we do have
[00:44:15 - 00:44:18] your awesome miscellaneous springs.
[00:44:18 - 00:44:24] So you can just have torsion bars, which in old cars,
[00:44:24 - 00:44:28] they used to be a very common kind of spring.
[00:44:28 - 00:44:30] They were actually really popular in F1.
[00:44:30 - 00:44:32] Might still be popular in F1.
[00:44:32 - 00:44:37] People, anyone like F1 crazy?
[00:44:37 - 00:44:38] No.
[00:44:38 - 00:44:43] There was one of the suspension kind of additions
[00:44:43 - 00:44:45] a few years ago, but I'm not sure if the rules of change
[00:44:45 - 00:44:47] and I've gone away from that.
[00:44:47 - 00:44:49] I only say this because I've kind of got
[00:44:49 - 00:44:50] called out by a student when I was like,
[00:44:50 - 00:44:53] I have real old cars used to use these things now.
[00:44:53 - 00:44:55] Actually, it's pretty high-tech now.
[00:44:55 - 00:44:58] So everything can be kind of cyclic.
[00:44:58 - 00:45:01] Obviously, spring-free trampolines use
[00:45:01 - 00:45:06] paltruid fibroblast rods that are bent to provide
[00:45:06 - 00:45:08] that kind of spring action.
[00:45:08 - 00:45:11] If you've either had to deal with a trailer or similar,
[00:45:11 - 00:45:14] you might have seen leaf springs, which are also
[00:45:14 - 00:45:18] or we can have flat springs.
[00:45:18 - 00:45:20] So here we see an example for how you would actually
[00:45:20 - 00:45:23] work out the spring constant for something similar
[00:45:23 - 00:45:26] to the spring-free trampoline.
[00:45:26 - 00:45:31] And we have a few other miscellaneous options there, which
[00:45:31 - 00:45:34] I'll kind of just leave for completeness.
[00:45:34 - 00:45:37] But we can see that there are a few kind of nuanced types
[00:45:37 - 00:45:41] of springs that are used in different carcinaries.
[00:45:41 - 00:45:46] So we see here examples of our constant force spring,
[00:45:46 - 00:45:47] which is in your tape measure.
[00:45:47 - 00:45:51] You've either thought about how the tape is always
[00:45:51 - 00:45:54] kind of got the same amount of force on it.
[00:45:54 - 00:45:57] That's because it's coiled up like this.
[00:45:57 - 00:45:59] And then we see some clockwork springs, et cetera.
[00:45:59 - 00:46:03] But for completeness, I'm just going to leave it there.
[00:46:03 - 00:46:05] We've talked about the main equations
[00:46:05 - 00:46:09] that you need for completing this part of the assignment.
[00:46:09 - 00:46:12] So hopefully you're feeling happy enough
[00:46:12 - 00:46:16] that you have an idea of where to start that is
[00:46:16 - 00:46:18] aspect of the assignment.
[00:46:18 - 00:46:20] And obviously, you'll just need to make sure you're carefully
[00:46:20 - 00:46:24] worried what is required for the spring,
[00:46:24 - 00:46:31] probably the last paragraph has that detail.
[00:46:31 - 00:46:31] Cool.
[00:46:31 - 00:46:35] So while we're being talking, are there any other questions
[00:46:35 - 00:46:47] related to the assignment that you have?
[00:46:47 - 00:46:50] So in the lecture notes that I put together,
[00:46:50 - 00:46:55] I kind of had done this under the idea
[00:46:55 - 00:47:00] that you may not know what you want to do.
[00:47:00 - 00:47:03] So in future of these examples here,
[00:47:03 - 00:47:04] I mean, we do have time.
[00:47:04 - 00:47:07] We could possibly do half or one example
[00:47:07 - 00:47:09] to do how much detail we want.
[00:47:09 - 00:47:12] But would we want to do a clutch example?
[00:47:12 - 00:47:15] Would we want to review the bearing selection process?
[00:47:15 - 00:47:17] Would we want to do a bearing selection example
[00:47:17 - 00:47:22] or a shaft sizing example?
[00:47:22 - 00:47:23] All four.
[00:47:23 - 00:47:25] So we probably don't have time for all four.
[00:47:25 - 00:47:28] But I would say that a bearing selection example
[00:47:28 - 00:47:31] has been the bearing notes.
[00:47:31 - 00:47:36] So if you want to look at that, if you look at our design
[00:47:36 - 00:47:42] lecture slides, and then we go to our roller bearings.
[00:47:42 - 00:47:45] We've got this additional document.
[00:47:45 - 00:47:48] We will see that I have detailed an example
[00:47:48 - 00:47:53] for how to guard out choosing and completing a bearing life
[00:47:53 - 00:47:54] calculation.
[00:47:54 - 00:48:01] So soon there should be some, there we go,
[00:48:01 - 00:48:02] beautiful handwritten examples.
[00:48:02 - 00:48:06] So if you're unsure or you want to go over that,
[00:48:06 - 00:48:08] I've kind of stepped it out in terms of this
[00:48:08 - 00:48:10] is the steps that I'll take.
[00:48:10 - 00:48:15] And then I show all those steps in this handout here.
[00:48:15 - 00:48:17] So probably look at that.
[00:48:17 - 00:48:18] And then if you've got questions, we can definitely
[00:48:18 - 00:48:21] discuss what happened there.
[00:48:21 - 00:48:23] You'll see that I am very clear in saying
[00:48:23 - 00:48:25] where I got information from.
[00:48:25 - 00:48:27] And if you have a different type of bearing,
[00:48:27 - 00:48:30] make sure that you refer to the bearing catalog,
[00:48:30 - 00:48:34] that will tell you where to get the information
[00:48:34 - 00:48:36] that is important.
[00:48:36 - 00:48:38] We can review the bearing selection process,
[00:48:38 - 00:48:41] but in Wigdine, I'm going to spend a lot of time reviewing
[00:48:41 - 00:48:43] our cross-section drawings as well.
[00:48:43 - 00:48:46] So we'll sort of probably do half and half here.
[00:48:46 - 00:48:52] Shaft sizing example, that is also in our shaft lecture.
[00:48:52 - 00:48:55] So if you look at that here, we'll
[00:48:55 - 00:49:01] see in our shaft design, there is previous examples
[00:49:01 - 00:49:06] that have been completed using that ASME calculation.
[00:49:06 - 00:49:10] So one of those things I understand as a student,
[00:49:10 - 00:49:13] knowing that you go through a lot of information
[00:49:13 - 00:49:15] and might be difficult.
[00:49:15 - 00:49:19] This one here we can see is an example that
[00:49:19 - 00:49:24] is showing at one specific point using the ASME equation,
[00:49:24 - 00:49:27] what the minimum diameter would need to be.
[00:49:27 - 00:49:29] So what we see for your assignment
[00:49:29 - 00:49:32] is that you probably want to do that not just in one place,
[00:49:32 - 00:49:36] because there might be one place that has or multiple places
[00:49:36 - 00:49:39] that have more or less bending.
[00:49:39 - 00:49:41] And you might just through the design
[00:49:41 - 00:49:43] and how it's going to go together.
[00:49:43 - 00:49:45] Want to have a smaller diameter on one side
[00:49:45 - 00:49:46] of your bearings, right?
[00:49:46 - 00:49:50] So definitely want to check more than one place there.
[00:49:50 - 00:49:52] So that very broad brush, Lee, is saying
[00:49:52 - 00:49:56] that there is information about those two there.
[00:49:56 - 00:49:59] The review of the selection process we can probably do
[00:49:59 - 00:50:00] in the future.
[00:50:00 - 00:50:05] And then finally, as we really start the clock counting down,
[00:50:05 - 00:50:10] the shaft or the torque, clutch torque example,
[00:50:10 - 00:50:12] if you want to have a go at this one here,
[00:50:12 - 00:50:16] and that would pretty much answer that question.
[00:50:16 - 00:50:19] But what you'd see is that we've got a amount of torque
[00:50:19 - 00:50:21] to transmit.
[00:50:21 - 00:50:23] We then would have to, what do we need to define
[00:50:23 - 00:50:28] if we were to work out the actuation force?
[00:50:28 - 00:50:29] We have to be clicky.
[00:50:29 - 00:50:31] I'm going over time.
[00:50:31 - 00:50:32] So we know the torque, so that's good.
[00:50:32 - 00:50:37] What other things would we need to define?
[00:50:37 - 00:50:39] Our material, our seduce,
[00:50:39 - 00:50:40] torque, right?
[00:50:40 - 00:50:42] So that gives us our lower case if.
[00:50:42 - 00:50:46] We probably have to state that it's a single clear of clutches.
[00:50:46 - 00:50:50] And then we would have to work out what diameters
[00:50:50 - 00:50:55] would be suitable to get to the indeterminate force, right?
[00:50:55 - 00:50:58] So in that case, I was looking at these equations here.
[00:50:58 - 00:51:00] I'd probably rearranged this for if.
[00:51:00 - 00:51:04] And then I would have to calculate possibly iteratively
[00:51:04 - 00:51:06] or I could use that same sort of plot thing
[00:51:06 - 00:51:10] to work out what diameters would give me
[00:51:10 - 00:51:13] the actuation force or what that situation force would be there.
[00:51:13 - 00:51:15] But if you've got questions about that,
[00:51:15 - 00:51:19] feel free to email me about it or come and drop on office.
[00:51:19 - 00:51:21] Otherwise that's all we've got time for today.
[00:51:21 - 00:51:29] Thank you very much.
[00:51:29 - 00:51:31] Yeah, I'll just jump onto the side.
[00:51:47 - 00:51:49] You don't really know what diameters are going to be.
[00:51:49 - 00:51:52] So you've got just a few more things than chicken at the end.
[00:51:52 - 00:51:55] So I'll just make sure that you're looking at the end.
[00:51:55 - 00:51:58] So I'll just go back to the end.
[00:51:58 - 00:52:01] So I'll just go back to the end.
[00:52:01 - 00:52:02] So I'll just go back to the end.
[00:52:02 - 00:52:05] So I'll just go back to the end.
[00:52:05 - 00:52:10] But I'll just make sure that you're looking at the end.
[00:52:10 - 00:52:12] And I'll just go back to the end.
[00:52:12 - 00:52:15] And then we'll shall go back to the end.
[00:52:15 - 00:52:17] So I'll just go back to the end.
[00:52:17 - 00:52:19] And I'll just go back to the end.
[00:52:19 - 00:52:21] Good change y'all.
[00:52:21 - 00:52:24] You're using my name and I'll just let you know.
[00:52:24 - 00:52:29] It looks like from the top, you're not using my name.
[00:52:29 - 00:52:34] I'm actually awesome to see you guys still here.
[00:52:34 - 00:52:36] I'm just happy to see you guys here.
[00:52:36 - 00:52:39] I'm so happy to see you guys here.
[00:52:39 - 00:52:41] I'm so happy to see you guys here.
[00:52:41 - 00:52:43] I'm so happy to see you guys here.
[00:52:43 - 00:52:45] I'm so happy to see you guys here.
[00:52:45 - 00:52:47] That's what I'm doing at the final couple of years.
[00:52:47 - 00:52:48] I'm just not going to do anything.
[00:52:48 - 00:52:50] The people are just saying, what is the shift?
[00:52:50 - 00:52:51] It's not a soft range.
[00:52:51 - 00:52:53] What's not because I'm a pretty nice guy.
[00:52:53 - 00:52:55] Top-hand's hit right here, huh?
[00:52:55 - 00:52:57] You've got a sports movement and that's what you're talking about.
[00:52:57 - 00:52:58] You guys are crazy.
[00:52:58 - 00:53:01] And on the front, there's a very long range.
[00:53:01 - 00:53:03] I'm very curious.
[00:53:03 - 00:53:05] I've been here all the time.
[00:53:05 - 00:53:06] See you guys here here.
[00:53:06 - 00:53:07] Bye-bye.
[00:53:07 - 00:53:10] Alright, I'm just gonna say thank you guys for being here.
[00:53:10 - 00:53:13] Now we're going to have nothing longer than it is.
[00:53:13 - 00:53:16] Is the difference between the strong red and the fist.
[00:53:16 - 00:53:18] Someone just needs the beat.
[00:53:18 - 00:53:20] You guys should be nervous.
[00:53:20 - 00:53:24] If you're assuming that there's none for us, we may be not repeating it.
[00:53:24 - 00:53:26] Did the good eye"?
[00:53:56 - 00:54:01] I'm not sure what the most important thing is.
[00:54:01 - 00:54:02] Yeah.
[00:54:02 - 00:54:03] Yeah.
[00:54:03 - 00:54:05] But these are the examples that I've shown you,
[00:54:05 - 00:54:08] showed you, you see the range.
[00:54:08 - 00:54:09] Yeah.
[00:54:09 - 00:54:10] And the way that you're going to be,
[00:54:10 - 00:54:12] it'll be no forces.
[00:54:12 - 00:54:15] And that one of those is one of those.
[00:54:15 - 00:54:18] Which is my turn to clear the journey.
[00:54:18 - 00:54:20] All they would be, you could start out.
[00:54:20 - 00:54:22] It would be, let the front view.
[00:54:22 - 00:54:24] Yeah, you could say, I would be South right,
[00:54:24 - 00:54:26] I don't know if you want to calculate it.
[00:54:26 - 00:54:28] You could count the chicken and then you can't write it.
[00:54:28 - 00:54:29] I haven't shot down.
[00:54:29 - 00:54:31] The forces to work out the shot down,
[00:54:31 - 00:54:33] so I'll just issue them.
[00:54:33 - 00:54:37] The negligible limit that we shoot at the end is your point.
[00:54:37 - 00:54:38] Yeah.
[00:54:38 - 00:54:39] Yeah.
[00:54:39 - 00:54:40] Yeah.
[00:54:40 - 00:54:41] Yeah.
[00:54:41 - 00:54:42] Yeah.
[00:54:42 - 00:54:43] Yeah.
[00:54:43 - 00:54:44] Yeah.
[00:54:44 - 00:54:45] Yeah.
[00:54:45 - 00:54:46] Yeah.
[00:54:46 - 00:54:47] Yeah.
[00:54:47 - 00:54:48] Yeah.
[00:54:48 - 00:54:49] Yeah.
[00:54:49 - 00:54:50] Yeah.
[00:54:50 - 00:54:51] Yeah.
[00:54:51 - 00:54:52] Yeah.
[00:54:52 - 00:54:53] Yeah.
[00:54:53 - 00:54:54] Yeah.
[00:54:54 - 00:54:55] Yeah.
[00:54:55 - 00:55:19] I like your

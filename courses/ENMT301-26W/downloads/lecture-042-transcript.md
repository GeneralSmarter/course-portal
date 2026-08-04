# ENMT301-26W Lecture 42 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `910479c5dc7063625cf53b3696fb667c210b44ca4c6980d200c696b9015f7ea5`
Generated: 2026-06-06T06:37:47.431841+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:01:05 - 00:01:20] Oh man, we've got a full house today.
[00:01:20 - 00:01:21] How good?
[00:01:21 - 00:01:22] All right.
[00:01:22 - 00:01:24] This is good.
[00:01:24 - 00:01:27] How's your own going?
[00:01:27 - 00:01:30] Sweet.
[00:01:30 - 00:01:31] Double thumbs up.
[00:01:31 - 00:01:32] Single thumbs up.
[00:01:32 - 00:01:33] That's what we like to see.
[00:01:33 - 00:01:51] Obviously, we will have opportunities to talk about a few different things.
[00:01:51 - 00:01:58] So these are the lecture slides, which I'll put together.
[00:01:58 - 00:02:00] So we're in a week's event.
[00:02:00 - 00:02:03] This is to twirl about assignment two.
[00:02:03 - 00:02:08] About half the time we can talk about owl bearing housing design and some questions that
[00:02:08 - 00:02:12] you have, meaning that you're really clear about what the requirements are for designing
[00:02:12 - 00:02:13] the clutch.
[00:02:14 - 00:02:20] And then also we will talk about some lecture notes for designing springs to make sure that
[00:02:20 - 00:02:25] the side crystal design in the spring view design is also clear.
[00:02:25 - 00:02:32] Obviously, if you weren't in the lecture, you'll see that I was highlighting this paper,
[00:02:32 - 00:02:39] which I was trying to get some views on.
[00:02:39 - 00:02:40] And then also we have some notices.
[00:02:40 - 00:02:46] So a video has been put on learn, which covers example calculations for some secret room
[00:02:46 - 00:02:52] moments, compressive stresses on the shaft shoulder, as well as an example alternative
[00:02:52 - 00:02:58] reality check, which are things that we expect you to do in your assignment.
[00:02:58 - 00:03:01] Now, was everyone aware of these?
[00:03:01 - 00:03:02] Well, no.
[00:03:02 - 00:03:07] Some people are nodding, some people were shaking their head, which means that it's useful
[00:03:07 - 00:03:10] that I re-emphasized this here.
[00:03:10 - 00:03:18] And for completeness, if I go onto the bearing housing part of the course page, we will
[00:03:18 - 00:03:20] see there.
[00:03:20 - 00:03:23] We have this link here to the echo video.
[00:03:23 - 00:03:27] And we also have these examples that might be useful.
[00:03:27 - 00:03:32] So we see this one here for a zid configuration, looking at universal drive shaft secondary
[00:03:32 - 00:03:33] moments.
[00:03:33 - 00:03:39] So that might be useful to review when you start doing that part of your assignment.
[00:03:39 - 00:03:45] Here we have some axial force and compressive stress on the shoulder calculation.
[00:03:45 - 00:03:50] Now, a good question or comment was made in the last tutorial of George Goodeauer assignment.
[00:03:50 - 00:03:54] It doesn't have a axial force component.
[00:03:54 - 00:03:59] Do we just come up with one for this two completeness kind of calculation?
[00:03:59 - 00:04:04] And the answer is yes, you can just assume an axial load and it probably would relate to
[00:04:04 - 00:04:06] like a reasonable misused case.
[00:04:06 - 00:04:11] So it could be someone pulling on it or getting bumped during transport, but you can kind
[00:04:11 - 00:04:13] of pick the value of that axial force.
[00:04:13 - 00:04:19] I think I mentioned the words 500 newtons would be appropriate, but it really doesn't matter.
[00:04:19 - 00:04:25] I don't think about the amount of stress that's going to be put actually on your shaft
[00:04:25 - 00:04:27] when there's not an axial load.
[00:04:27 - 00:04:30] It's going to be pretty small regardless.
[00:04:30 - 00:04:31] Right.
[00:04:31 - 00:04:35] I'm not going to be like a failure.
[00:04:35 - 00:04:40] A likely failure for your design.
[00:04:40 - 00:04:46] And then subsequently there is also a possible alternative reality check.
[00:04:46 - 00:04:56] And I can see here that I haven't incorporated any stress concentrations or impact loading.
[00:04:56 - 00:05:00] So obviously those would be useful things to consider.
[00:05:01 - 00:05:05] Now you know that those information, a bit of information is there and there's also a kind
[00:05:05 - 00:05:10] of a video that talks to each of them if you're like looking at a video rather than just
[00:05:10 - 00:05:11] looking at PDF.
[00:05:11 - 00:05:16] So today we'll focus on the design of springs, but before we do that we'll answer any
[00:05:16 - 00:05:22] burning questions you have and we'll answer some questions about our clutch requirements
[00:05:22 - 00:05:24] for our assignment.
[00:05:24 - 00:05:35] And then if these types are already in the notes and then that might be helpful to kind
[00:05:35 - 00:05:40] of focus on further information.
[00:05:40 - 00:05:54] So with that what are the burning questions you currently have about either assignment?
[00:05:54 - 00:05:56] Yep.
[00:05:56 - 00:06:03] So I think we've been with having a channel of stroke at some functional stress for the
[00:06:03 - 00:06:04] shaft.
[00:06:04 - 00:06:10] Do you know what we did last year with you know, the sheet was driver ends and monitoring
[00:06:10 - 00:06:11] stuff.
[00:06:11 - 00:06:12] That's what we're currently doing.
[00:06:12 - 00:06:19] In terms of traditional stress, is that something I would have to start from right now
[00:06:19 - 00:06:20] if I had a little brush there?
[00:06:20 - 00:06:21] Oops.
[00:06:21 - 00:06:28] So the question was, I feel fairly confident about the sheath also been in moment diagrams
[00:06:28 - 00:06:29] for the system.
[00:06:29 - 00:06:34] And one way to think about it is we've got, um, those who aren't necessarily clear on
[00:06:34 - 00:06:36] that part of the assignment.
[00:06:36 - 00:06:43] If we're looking at our side view, we need to make it clear assumption about what angle
[00:06:43 - 00:06:46] our chain tension force is acting on our sprocket, right?
[00:06:46 - 00:06:48] So it could be vertically up and down.
[00:06:48 - 00:06:49] It could be horizontal.
[00:06:49 - 00:06:51] It could be some angle in between.
[00:06:51 - 00:06:53] And we sort of touched on this.
[00:06:53 - 00:06:59] When we looked at the assignment brief and sort of said, you know, I basically just said
[00:06:59 - 00:07:04] that the drawing that we have been given for the assignment is not very clear exactly
[00:07:04 - 00:07:12] what angle the chain is actually coming away from that shaft.
[00:07:12 - 00:07:14] What angle it's acting on the shaft, right?
[00:07:14 - 00:07:21] So you need to kind of clarify that at the beginning of your calculations because your
[00:07:21 - 00:07:24] sheath or some beginning moment diagrams will depend on that assumption.
[00:07:24 - 00:07:25] Yeah?
[00:07:25 - 00:07:27] Well, there's not one right way.
[00:07:27 - 00:07:30] I'm happy with whatever of those three kind of options.
[00:07:30 - 00:07:36] And then, um, normally speaking, we saw here that if this is a view where you have a force
[00:07:36 - 00:07:41] in the middle, which might be your sprocket load, then your sheath force and your beginning
[00:07:41 - 00:07:44] moment diagram might look like that, right?
[00:07:44 - 00:07:50] So that's the thing where you've seen your feeling pretty clear on, which is good, where
[00:07:50 - 00:07:57] you weren't sure is that at this point here where the sprocket is, is going to be a high
[00:07:57 - 00:07:58] amount of torque.
[00:07:58 - 00:08:05] And how do we calculate or check that our shaft is going to be safe at that point?
[00:08:05 - 00:08:06] Yeah?
[00:08:06 - 00:08:11] And so to flip the question and we, but if you were to work out what size your shaft is
[00:08:11 - 00:08:14] going to be, what equation or formula would you use?
[00:08:14 - 00:08:23] Can you remember, is there one?
[00:08:23 - 00:08:25] Is there an equation to work out the minimum shaft diameter?
[00:08:25 - 00:08:31] Yeah, this one on the lecture slide.
[00:08:31 - 00:08:34] So there's a, there's an ACME like minimum shaft diameter calculation.
[00:08:34 - 00:08:40] So using your sheath force and beginning moment diagram for a specific point, you'll therefore
[00:08:40 - 00:08:45] know what the bending and the torque is in your shaft.
[00:08:45 - 00:08:50] You can put those numbers in and we'll send load factors and get out of minimum diameter.
[00:08:50 - 00:08:55] And then if you were to check that the torque is not going to be in this view, you could
[00:08:55 - 00:09:02] do an alternative reality check, which is actually what one of those examples was here,
[00:09:02 - 00:09:03] right?
[00:09:03 - 00:09:06] So you could use this equation here and again, knowing the moment and torque that is at that
[00:09:06 - 00:09:11] point in the shaft, you could work out the maximum sheath stress and then compare that
[00:09:11 - 00:09:15] to what the maximum allowable sheath stress would be for your shaft.
[00:09:15 - 00:09:18] Cool.
[00:09:18 - 00:09:26] So to do that though, how do we work out what the maximum permissible sheath stress is?
[00:09:26 - 00:09:32] Is there a decision we have to have made?
[00:09:32 - 00:09:35] Not necessarily factor of safety broadly speaking.
[00:09:35 - 00:09:39] So if I was to complete this calculation here, I know the square root of three times
[00:09:39 - 00:09:40] UTS.
[00:09:40 - 00:09:46] What I need to know to be able to do that is how do I work out the UTSs?
[00:09:46 - 00:09:49] You're going to have to choose what your material is going to be, right?
[00:09:49 - 00:09:56] And so what we can see here is some questions that I was hoping there would come up.
[00:09:56 - 00:10:00] We can see that generally speaking, if you know you're using steel, there's like a
[00:10:00 - 00:10:05] general kind of comment because most deals have the same elastic modulus.
[00:10:05 - 00:10:09] You can often just assume approximately 200 GPA if that's a value that you need to use,
[00:10:09 - 00:10:10] right?
[00:10:10 - 00:10:15] So it's basically saying that four different shafts, regardless if it was a high carbon
[00:10:15 - 00:10:22] carbon or a medium carbon or a low carbon steel, an amount of deflection is going to be similar
[00:10:22 - 00:10:23] regardless, right?
[00:10:23 - 00:10:31] But we can see that these different materials have different kind of tinsile stresses in
[00:10:31 - 00:10:34] allowable therefore allowable stresses.
[00:10:34 - 00:10:40] So basically you could get away with a small shaft if you're using a stronger material.
[00:10:40 - 00:10:44] If you're unsure what kind of material would a pick, here's some information that may help
[00:10:44 - 00:10:45] you.
[00:10:45 - 00:10:47] This should not be like a major part of your assignment.
[00:10:47 - 00:10:54] So my kind of recommendation might be to use medium density carbon steel as good strings
[00:10:54 - 00:10:56] toughness and we resistance.
[00:10:56 - 00:11:01] But if you really wanted to, you could also use something more commonly available like mild
[00:11:01 - 00:11:02] steel.
[00:11:02 - 00:11:08] Sometimes it is used depending on the case and what kind of specialist kind of properties
[00:11:08 - 00:11:10] or quality is needed, right?
[00:11:10 - 00:11:14] So we don't really have that many constraints on our size so we can kind of use whatever.
[00:11:14 - 00:11:16] We don't have to pay for our thing as well.
[00:11:16 - 00:11:21] So but we can see here both hot rolled and cold old options are used and have their own
[00:11:21 - 00:11:22] advantages.
[00:11:22 - 00:11:29] Generally hot rolled is cheaper, more likely to have these material defects such as variations
[00:11:29 - 00:11:35] in hardness or residual stresses due to uneven cooling or voids in our material.
[00:11:36 - 00:11:41] And there's also less dimensionally accurate or you can have cold rolled bar which tends
[00:11:41 - 00:11:48] to be more expensive and it's easier to machine.
[00:11:48 - 00:11:52] So if you wanted to do that, it's, I'll turn it to the reality check and you need to know
[00:11:52 - 00:11:56] what your material is shaft is, right?
[00:11:56 - 00:11:59] You will have to decide the material you use in your design.
[00:11:59 - 00:12:00] Cool.
[00:12:00 - 00:12:01] Sweet.
[00:12:01 - 00:12:02] Other questions?
[00:12:02 - 00:12:03] Yep.
[00:12:03 - 00:12:04] Yep.
[00:12:04 - 00:12:07] Yeah.
[00:12:07 - 00:12:08] Yeah.
[00:12:08 - 00:12:11] I understand.
[00:12:11 - 00:12:28] I think it's 15 above and 15 below.
[00:12:28 - 00:12:29] Yeah.
[00:12:29 - 00:12:30] Okay.
[00:12:30 - 00:12:34] Yeah, I'm pretty sure it is but I'll just look.
[00:12:34 - 00:12:35] Yeah.
[00:12:35 - 00:12:39] For those that were online the question was around the mark sheet for the aluminium structure
[00:12:39 - 00:12:45] and with the, the plus or minus.
[00:12:45 - 00:12:48] Yeah, plus or minus 15% so moving that, yeah.
[00:12:48 - 00:12:49] Cool.
[00:12:49 - 00:12:51] Happy days.
[00:12:51 - 00:12:52] Nice.
[00:12:53 - 00:12:57] Other questions.
[00:12:57 - 00:13:02] So the other thing that I wanted to touch on relates to this slide here in the requirements
[00:13:02 - 00:13:11] that are required for do is doing a clutch design aspect of the assignment, right?
[00:13:11 - 00:13:22] So if we look at a bearing housing assignment brief, we'll see that an Apple at point of
[00:13:22 - 00:13:29] kind of outline of projective tasks is also outlined in the, why are the same?
[00:13:29 - 00:13:31] How do I get it to go away?
[00:13:31 - 00:13:34] So I'm going to listen.
[00:13:34 - 00:13:39] But we can see here that there is some information in here where it kind of outlines that
[00:13:39 - 00:13:47] we do need to look at whether it would be possible to have an overload slipping clutch.
[00:13:47 - 00:13:48] Yeah.
[00:13:48 - 00:13:55] And so the idea is that it protects the components of the system jams unexpectedly as well
[00:13:55 - 00:13:57] as from shock loads in right here.
[00:13:57 - 00:14:01] Sometimes we now care as a engaging or disengaging.
[00:14:01 - 00:14:02] Yeah.
[00:14:02 - 00:14:07] So put more straightforwardly.
[00:14:07 - 00:14:11] We can see that we've got the explicit requirement to undertake clutch calculations and show
[00:14:11 - 00:14:13] that they will fit in the available space.
[00:14:13 - 00:14:17] There's any results in such a way to enable someone to decide a suitable size clutch.
[00:14:17 - 00:14:23] We've a recommendation and specify the actuation force that allows the clutch to slip
[00:14:23 - 00:14:26] it just over the maximum torque.
[00:14:26 - 00:14:29] So that's going to be what you need to do.
[00:14:29 - 00:14:39] And to do that, we need to think about our clutch and what the torque and the clutch is
[00:14:39 - 00:14:41] a function of.
[00:14:41 - 00:14:47] So the torque that a clutch can transmit is a function of what?
[00:14:47 - 00:14:51] I'll put up one of the slides.
[00:14:51 - 00:14:58] I don't know which slide is online, but hopefully they got lucky and they can see things.
[00:14:58 - 00:14:59] Cool.
[00:14:59 - 00:15:07] So it's definitely a function of the coefficient of friction, which is the material essentially,
[00:15:07 - 00:15:08] yeah.
[00:15:08 - 00:15:09] And that the material is in, right?
[00:15:09 - 00:15:14] So we can see over here that we've got a bunch of different coefficients of friction,
[00:15:14 - 00:15:17] the different conditions if it's dry or you're lubricated.
[00:15:17 - 00:15:20] So you're just going to make sure that if you pick one or you pick multiple, it's clear
[00:15:20 - 00:15:22] what you've picked and why?
[00:15:22 - 00:15:24] Not necessarily why, but you've picked a few.
[00:15:24 - 00:15:26] You're making a few to check that out.
[00:15:26 - 00:15:27] Sort of different.
[00:15:27 - 00:15:28] What else?
[00:15:28 - 00:15:34] So the service area is a function of our outer and inner diameter.
[00:15:34 - 00:15:35] Yeah.
[00:15:35 - 00:15:36] What else?
[00:15:36 - 00:15:43] So to do that calculation, what do we require to do?
[00:15:43 - 00:16:00] We require to work out for a set slipping torque.
[00:16:00 - 00:16:08] What the actuation force and then other parameters would be of a clutch.
[00:16:08 - 00:16:09] Yeah.
[00:16:09 - 00:16:12] So there's a few ways that you could do that.
[00:16:12 - 00:16:17] All of the ways are going to require for you to make some sort of assumptions or clearly
[00:16:17 - 00:16:20] say what you are investigating, right?
[00:16:20 - 00:16:26] So the two ways that I've kind of described in previous, one way could be that you make a
[00:16:26 - 00:16:33] plot of torque, the other way it could be that you make a plot of actuation force.
[00:16:33 - 00:16:34] Yeah?
[00:16:34 - 00:16:38] And so this one here, what you might hold constant as a torque.
[00:16:38 - 00:16:41] So they might be like a constant torque line.
[00:16:41 - 00:16:44] Yeah?
[00:16:44 - 00:16:46] I've not defined a variable at the bottom here.
[00:16:46 - 00:16:51] So that curve that I've drawn might not be a curve in that direction depending on what variable
[00:16:51 - 00:16:52] you choose, right?
[00:16:52 - 00:16:59] Ideally, what you want to do is make a plot where there is some independent variable.
[00:16:59 - 00:17:01] What's the one you change on the bottom, right?
[00:17:01 - 00:17:04] So you want something to be an independent variable on the bottom.
[00:17:04 - 00:17:06] What could we use for that independent variable?
[00:17:06 - 00:17:11] Yeah.
[00:17:11 - 00:17:15] So in the outer diameter and your other diameter and for either of those ones, you would
[00:17:15 - 00:17:18] need to specify what it is.
[00:17:18 - 00:17:21] For example, when the other one might be constant, right?
[00:17:21 - 00:17:27] So you might assume that low case D is this and you're going to show that when the outer
[00:17:27 - 00:17:32] diameter changes, this is the amount of actuation force that's required for a certain
[00:17:32 - 00:17:35] torque and you might have different lines for different materials.
[00:17:35 - 00:17:36] I don't know.
[00:17:36 - 00:17:37] Up to you.
[00:17:37 - 00:17:38] Yeah?
[00:17:38 - 00:17:39] So you might have.
[00:17:40 - 00:17:43] The other way to do it would be you could even do it the same sort of way.
[00:17:43 - 00:17:48] You could have that independent variable being an error out of diameter.
[00:17:48 - 00:17:50] What do you think makes the most sense?
[00:17:50 - 00:17:55] And this case you might specify an actuation force, specify the material.
[00:17:55 - 00:18:01] And again, you'll get those some sort of line on there and then you'll get a read it off.
[00:18:01 - 00:18:04] This is the amount of torque that I need.
[00:18:04 - 00:18:09] This is what I give and what my result is.
[00:18:12 - 00:18:13] This is the list blur.
[00:18:13 - 00:18:20] Is that kind of clear on the approach there we would take?
[00:18:20 - 00:18:23] There's like lots of ways to do it.
[00:18:23 - 00:18:28] Basically we want you to have a play with those equations.
[00:18:28 - 00:18:34] So what you'll see here is you might want to look at these different materials that have
[00:18:34 - 00:18:35] different performance.
[00:18:35 - 00:18:39] What size clutch you would need if it was cast iron on cast iron versus cork on metal
[00:18:39 - 00:18:42] rock.
[00:18:42 - 00:18:45] And you need to specify if it was dry, greasy or lubricated.
[00:18:46 - 00:18:49] And we've said I think it's as in the matchary plots.
[00:18:49 - 00:18:51] So we're looking at more than one figure.
[00:18:51 - 00:18:52] Yeah.
[00:18:52 - 00:19:04] Why do we do the plots instead of capillary in the equations?
[00:19:04 - 00:19:06] Basically so that you can see the trends.
[00:19:06 - 00:19:11] So you're going to have to assume either uniform we or uniform pressure.
[00:19:11 - 00:19:16] I guess if you really wanted to you could specify a torque in specified
[00:19:16 - 00:19:19] the natural force in sole for diameter.
[00:19:19 - 00:19:24] But sometimes there might be a trade off of what actually you have.
[00:19:24 - 00:19:29] So if you look at those plots here, you know, there might be to get the torque you could
[00:19:29 - 00:19:30] do.
[00:19:30 - 00:19:33] There might be one line going through here, one line through here, one line through here.
[00:19:33 - 00:19:38] This size here obviously you probably want your maximum diameter to be smaller than your
[00:19:38 - 00:19:40] allowable maximum for the available space.
[00:19:40 - 00:19:48] So it kind of goes like, oh, I could use a 350 mill needle on metal arrangement with
[00:19:48 - 00:19:52] the higher actuation force or the same actuation force, depending on what plot you're using,
[00:19:52 - 00:19:56] versus if I used cork I could get away with it being this big or having a smaller actuation
[00:19:56 - 00:19:57] force.
[00:19:57 - 00:19:58] Yeah.
[00:19:58 - 00:20:01] So there's sort of a trade off set, lind.
[00:20:01 - 00:20:03] There now there's this link itself to be a little bit.
[00:20:03 - 00:20:04] I don't know.
[00:20:04 - 00:20:09] Things used to have like the plot and you're going to kind of read all the plots rather
[00:20:09 - 00:20:13] than just saying like, I know that I want the actuation force to be this in the area
[00:20:13 - 00:20:16] to be this therefore this here.
[00:20:16 - 00:20:22] When you use user?
[00:20:22 - 00:20:23] Yep.
[00:20:23 - 00:20:26] So we uniform.
[00:20:26 - 00:20:31] So we see this plot here which actually shows that the torque that is output from these
[00:20:31 - 00:20:37] equations gets very similar and more similar d in d in capital D.
[00:20:37 - 00:20:39] Yeah.
[00:20:39 - 00:20:47] So generally speaking uniform pressure is for a kind of more flexible clutch plate,
[00:20:47 - 00:20:52] which might be dependent on the material that you choose, where uniform wear is for more
[00:20:52 - 00:20:53] rigid plates.
[00:20:53 - 00:21:00] So again, if you assumed, yeah, I'm not too worried about which one you use because generally
[00:21:00 - 00:21:10] speaking, yeah, a new clutch might be more like uniform wear than as it gets older, it might
[00:21:10 - 00:21:13] act more like uniform pressure as the wear becomes.
[00:21:13 - 00:21:18] Well, yeah.
[00:21:18 - 00:21:23] I would just say your assumption if you've got a really rigid material, it might be appropriate
[00:21:23 - 00:21:25] to say I'm assuming uniform wear.
[00:21:25 - 00:21:33] And if you've got a more flexible material to assume uniform pressure.
[00:21:33 - 00:21:39] But if your value of d over d is relatively high, you could also just say that I'm going
[00:21:39 - 00:21:42] to use this and I know that the difference is relatively.
[00:21:47 - 00:21:48] Good questions.
[00:21:48 - 00:21:54] So yeah, you will need to make multiple plots I suppose.
[00:21:54 - 00:21:55] I didn't.
[00:21:55 - 00:21:57] Oh, I did sort of say that.
[00:21:57 - 00:21:58] I said we want more than one plots.
[00:21:58 - 00:21:59] Don't recreate this plot.
[00:21:59 - 00:22:01] This is just a generalized trend.
[00:22:01 - 00:22:05] But you probably also want to check that one of the solution you have allowable pressure
[00:22:05 - 00:22:06] is not exceed.
[00:22:06 - 00:22:09] Right?
[00:22:09 - 00:22:21] Say I can't see like a reasonable thing to do.
[00:22:21 - 00:22:24] I have flat plate, flat plate, flat plate, flat shoes.
[00:22:24 - 00:22:25] Yeah.
[00:22:26 - 00:22:29] So like this is pretty much like that.
[00:22:29 - 00:22:31] Key information all in one kind of slide.
[00:22:31 - 00:22:36] So if you were to use one, then that in theory should be the kind of the recipe or have
[00:22:36 - 00:22:47] the formulas and the recipe ingredients that you would need to kind of do that consideration.
[00:22:47 - 00:22:55] In questions about any of that.
[00:22:55 - 00:23:01] While I remember it was one question which I did then talk about some of what was shown
[00:23:01 - 00:23:02] and the frequently asked questions.
[00:23:03 - 00:23:05] Some people are not too sure where to start.
[00:23:05 - 00:23:09] We've kind of talked about the fact that you'll start with your free body diagram.
[00:23:09 - 00:23:13] You'll pick your direction that your change is acting.
[00:23:13 - 00:23:18] They're now mean that you can do your shear force and bending moment diagram just for
[00:23:18 - 00:23:20] your chain load.
[00:23:20 - 00:23:24] And then once you've got that locked in for your front and your top view, which one of
[00:23:24 - 00:23:26] them might basically have no loading on it.
[00:23:26 - 00:23:32] If it's acting only in one of the planes, then you will look at your secondary moments
[00:23:33 - 00:23:38] and then either add them directly if the secondary moment additional forces are acting in
[00:23:38 - 00:23:44] the same plane as the forces that are in your standard loading.
[00:23:44 - 00:23:49] Or you might have to use kind of trigger normal for you to work out what the maximum force
[00:23:49 - 00:23:50] in your shaft is.
[00:23:50 - 00:23:53] So you can see here I've said.
[00:23:53 - 00:23:59] Completely a force of movement moment diagrams in each plane.
[00:23:59 - 00:24:02] You'll need to work out the chain load.
[00:24:02 - 00:24:03] So how do we work out the chain load?
[00:24:03 - 00:24:08] I guess is the question that people asked previously, do we just use the maximum power
[00:24:08 - 00:24:10] from our motor?
[00:24:10 - 00:24:15] Or do we like work out how much force would be needed to pull the car up the left hole?
[00:24:15 - 00:24:18] There's an actual question for you guys.
[00:24:18 - 00:24:20] Well, you reckon.
[00:24:20 - 00:24:24] The latter, you know what else going to be ideas?
[00:24:24 - 00:24:27] The former, both of them.
[00:24:27 - 00:24:29] The answer is kind of both of them for completeness.
[00:24:29 - 00:24:31] It's probably a piece of the puzzle.
[00:24:31 - 00:24:35] I can't actually remember what the former in the letter was, but to start with I would
[00:24:35 - 00:24:42] use the maximum output of my motor to work out what the maximum possible chain force would
[00:24:42 - 00:24:44] be on my sprocket system.
[00:24:44 - 00:24:45] Right?
[00:24:45 - 00:24:47] And everything about it.
[00:24:47 - 00:24:52] If I've got this slipping clutch that will slip onto this torque, next torque is mid.
[00:24:52 - 00:24:57] Then that's the maximum kind of a chain force that might act on our system.
[00:24:57 - 00:24:58] Yeah?
[00:24:58 - 00:25:02] So that's like designing for like the worst case, which is good.
[00:25:02 - 00:25:10] However, have we actually done anything to verify that the size of motor that's insulated
[00:25:10 - 00:25:17] is actually big enough, not at the stage, right?
[00:25:17 - 00:25:26] So that's where that, looking at how much force would be required to pull two riders
[00:25:26 - 00:25:29] in the carriage up this kind of incline.
[00:25:29 - 00:25:33] You can have to make some assumptions in terms of what angle it's acting at.
[00:25:33 - 00:25:36] I don't know if it tells us.
[00:25:36 - 00:25:42] You'll have to do that and verify that the motor is actually big enough to do that job,
[00:25:42 - 00:25:47] right?
[00:25:47 - 00:25:49] Are we getting nods or are people lying?
[00:25:49 - 00:25:50] I'm not sure.
[00:25:50 - 00:25:51] Yeah, okay.
[00:25:51 - 00:25:52] Cool.
[00:25:52 - 00:25:55] We can't want to make sure that we don't just blindly trust our manager.
[00:25:55 - 00:25:59] And if it did happen that the motor wasn't big enough, then you'd have to say, I want you
[00:25:59 - 00:26:06] to be a big enough motor, but think it hopefully will be big enough.
[00:26:06 - 00:26:07] Any other questions?
[00:26:07 - 00:26:10] Right on top.
[00:26:10 - 00:26:13] Mm-hmm.
[00:26:13 - 00:26:20] Sweet.
[00:26:20 - 00:26:24] Oh well, without the next thing that I wanted to kind of talk about, because we're going to
[00:26:24 - 00:26:27] have a guest lecture in a couple weeks.
[00:26:27 - 00:26:32] I want to make sure that we cover the stuff for the spring section.
[00:26:33 - 00:26:35] We see here there's sort of two things that we need to do.
[00:26:35 - 00:26:39] One is to complete some scoping calculations to determine the nominal spring parameters,
[00:26:39 - 00:26:44] such as the chosen material with a wire diameter, the number of coils, the spring constant
[00:26:44 - 00:26:46] to show and show that the spring will not be coiled down.
[00:26:46 - 00:26:51] We also want to indicate the results of the scoping calculations by filling out a specification
[00:26:51 - 00:26:58] form, which is attached into your kinases, but we'll see the form, which we'll see in
[00:26:58 - 00:27:04] the lecture notes is this one here, right?
[00:27:04 - 00:27:05] Maybe.
[00:27:05 - 00:27:07] I was happy to see that there's a form there.
[00:27:07 - 00:27:08] Cool.
[00:27:08 - 00:27:13] So what I'll do, and I'll go through this round, let's have a leave quickly, but highlighting
[00:27:13 - 00:27:14] on the main kind of points.
[00:27:14 - 00:27:19] So here there's a lot of overview kind of information in these lecture slides here.
[00:27:19 - 00:27:25] And we can see there are a lot of them that are from Shiggly or our kind of machinery,
[00:27:25 - 00:27:30] handbook, or actually our design of manual design of engineering springs.
[00:27:30 - 00:27:33] So there is a standard that kind of helps us do it.
[00:27:33 - 00:27:37] So in general, what we'll be talking about at the types of springs, we'll go over how
[00:27:37 - 00:27:44] to calculate our spring rate and then for our wire springs working out what calculations
[00:27:44 - 00:27:51] are needed to determine what the sizes are from our how many coils are needed and what
[00:27:51 - 00:27:54] the diameter of those coils would be.
[00:27:54 - 00:27:59] So this one, this is a miscellaneous springs of the English, we'll just cover and realistically
[00:27:59 - 00:28:00] high detail.
[00:28:00 - 00:28:03] So you see here springs come in all shapes and sizes.
[00:28:03 - 00:28:09] The definition of the springs is that any passive element which deflects domestically
[00:28:09 - 00:28:14] under load and that way you can use springs for a range of things as machine designers,
[00:28:14 - 00:28:18] such as exerting forces, providing flexibility in our system.
[00:28:18 - 00:28:23] You might use it to store and then release energy to isolate vibration or you might
[00:28:23 - 00:28:27] actually use it as a measurement tool to measure forces.
[00:28:27 - 00:28:32] When we're really speaking there are wire springs, flat springs, air springs, miscellaneous
[00:28:32 - 00:28:41] springs which are not necessarily typical spring-like shaped or anything else and typically
[00:28:41 - 00:28:47] what we're focusing on this lecture is the information around the wire springs.
[00:28:47 - 00:28:53] So generally speaking, cost efficiency is a really important consideration when designing
[00:28:53 - 00:28:59] springs and what this basically means is that we don't want to have lots more material
[00:28:59 - 00:29:03] that is not really then stressed than we need.
[00:29:03 - 00:29:09] So we kind of want to stress our spring materials to the upper limits during this deflection
[00:29:09 - 00:29:14] process so that we can use smaller diameter or less material and if we have a slightly
[00:29:14 - 00:29:17] cheaper solution.
[00:29:17 - 00:29:23] So with that we can see here our kind of classic plot-cellers seen if England KX and then
[00:29:23 - 00:29:29] we have this linear kind of assumption for the linear region of our springs and with
[00:29:29 - 00:29:35] this hooks law we know that if we increase or double them on a force that's applied then
[00:29:35 - 00:29:40] we would double the amount of deflection in our system.
[00:29:40 - 00:29:44] So we see that that for the completeness has been included there and that we have the same
[00:29:44 - 00:29:52] sort of calculation or formula for our portion springs.
[00:29:52 - 00:29:56] So when you think about it though, here you think actually is a spring anything that you
[00:29:56 - 00:30:04] have will deflect some amount for nothing as truly rigid and if we then wanted to work out
[00:30:04 - 00:30:12] what is the K value or the spring constant for any material while using these steps and assumptions
[00:30:12 - 00:30:19] of our elastic modulus and then breaking it down into its individual kind of calculation
[00:30:19 - 00:30:24] components we can then work out what our spring constant is.
[00:30:24 - 00:30:34] So basically it's the inverse of this little bit here so we get eA over L being our spring
[00:30:34 - 00:30:42] constant if we use if and x in the form of this equation here.
[00:30:42 - 00:30:47] So what we'll see is actually a consideration that happens when we look at kind of voltage
[00:30:47 - 00:30:52] joints and stuff that bolt is actually compressing what if a system is looking at and that
[00:30:52 - 00:30:58] is actually a consideration and that we look into when you look at designing bolted
[00:30:58 - 00:31:00] connections.
[00:31:00 - 00:31:04] So our main focus is on these wire springs, typically they're here like they're well
[00:31:04 - 00:31:08] formed, they can be rounded in either direction both for compression and tension springs
[00:31:08 - 00:31:14] and this wire is typically a very high strength from 1600 to 2000 megapascals.
[00:31:14 - 00:31:19] Now to work out the maximum stress in here, the full spring we see this equation here
[00:31:19 - 00:31:26] where we have this well correction factor, we have our applied low, our coil diameter,
[00:31:26 - 00:31:27] our wire diameter.
[00:31:28 - 00:31:30] And we'll say apply.
[00:31:30 - 00:31:36] When you see that the shear stress is primarily the result of tension which some people
[00:31:36 - 00:31:40] might not be necessarily intuitive, some people might think that as you can press the spring
[00:31:40 - 00:31:46] that it's actually bending but realistically what is happening is that as it pushes together
[00:31:46 - 00:31:52] this is actually twisting our kind of individual wires and as we see in this kind of shear
[00:31:52 - 00:32:00] force or this free body diagram or of, well, the superposition of the stresses that we
[00:32:00 - 00:32:07] see in our helical spring, you can see that A is just our poor, pure torsional load, B is
[00:32:07 - 00:32:12] our direct shear stress and this kind of shows you that the shear stress generally is a
[00:32:12 - 00:32:17] lot smaller than our maximum stress from torsion.
[00:32:17 - 00:32:21] When you put those together and you get something that looks like C where you have this
[00:32:21 - 00:32:29] really high stress value on the inside of our wire diameter and then if you also take into account
[00:32:29 - 00:32:34] the curvature shear stress this day is even kind of more.
[00:32:34 - 00:32:36] So that's some as we'll see.
[00:32:36 - 00:32:42] Often when spring's fail, they'll fail due to torsion with a nice 45 degree kind of angle
[00:32:42 - 00:32:46] and the nucleation point is on that inner edge.
[00:32:46 - 00:32:50] Here's another kind of important equation that you'll probably use for your assignment.
[00:32:50 - 00:32:55] We'll see that to work out the spring constant for a helically bound spring.
[00:32:55 - 00:33:01] We'll use this equation here using our wire diameter, our shear modulus which is defined below
[00:33:01 - 00:33:09] our coil, scintaline diameter and the number of free coils in our compression spring arrangement.
[00:33:09 - 00:33:15] And so we can see that using this equation, if we want to increase our K value,
[00:33:15 - 00:33:21] we can either increase our wire diameter, we can decrease the number of coils or the
[00:33:21 - 00:33:36] length of our spring or we can decrease our nominal diameter.
[00:33:36 - 00:33:40] So in terms of features we can see that there are a range of ends.
[00:33:40 - 00:33:49] Some reason I only have ones that have ground ends, you'll see that here.
[00:33:49 - 00:33:57] So the ends in this case both of them have been ground to be flat.
[00:33:57 - 00:34:04] You can also have them open or closed, which we'll see some examples of below and here.
[00:34:04 - 00:34:07] The number of live coils are the coils that are spaced between them.
[00:34:07 - 00:34:13] So if you ever closed in, obviously that impacts the number of coils that you have.
[00:34:13 - 00:34:19] And if the spring and the spring is fully compressed, it will come to a state that is
[00:34:19 - 00:34:21] known as coil bound.
[00:34:21 - 00:34:25] So you can imagine that the stiffness of that whole arrangement, all of a sudden there's
[00:34:25 - 00:34:27] going to go skyrocketing.
[00:34:27 - 00:34:34] Yeah, a really large force will then be needed to only make a really small deflection
[00:34:34 - 00:34:38] once our spring system is coil bound.
[00:34:38 - 00:34:41] Buckling is also something that needs to be considered.
[00:34:42 - 00:34:48] And as we well know, in the in conditions are one of the considerations that we need to make.
[00:34:48 - 00:34:52] But what you can do to check that your spring is not going to buckle.
[00:34:52 - 00:35:00] There's if you plotted it on this kind of plot here, you could work out whether it is in the stable or unstable zone.
[00:35:00 - 00:35:07] Using these critical values of if over L naught over D in our relative deflection of the deflection
[00:35:07 - 00:35:11] of our L naught, so the initial length.
[00:35:11 - 00:35:17] So that's that easy way to check that your compression spring is not going to buckle.
[00:35:17 - 00:35:23] And then here we see that people can use these springs in a range of ways.
[00:35:23 - 00:35:30] This telescopic room instrument actually makes it act like tension spring.
[00:35:31 - 00:35:37] Yeah, you can have multiple arrangements to get different kind of responses.
[00:35:37 - 00:35:47] Surging is also something that can be a problem in spring systems, especially if there are a frequency load applied or a load applied
[00:35:47 - 00:35:49] at a set frequency.
[00:35:49 - 00:35:56] And so the main way that you can avoid this kind of surgeon from happening is to make sure that the critical
[00:35:56 - 00:36:06] frequency is 15 to 20 times any of the oscillary motions that are applied to your system.
[00:36:06 - 00:36:09] Here we see a valve spring that is failed.
[00:36:09 - 00:36:16] Again, you can see that there'll be a nucleation point always happens on that in the side.
[00:36:16 - 00:36:23] Then we've got a kind of classic 45 degree crack that has gone through our wire.
[00:36:23 - 00:36:25] So we can see here, the equation.
[00:36:25 - 00:36:34] Then we'd have some sort of beach marks before having a kind of brittle catastrophic failure of our spring.
[00:36:34 - 00:36:41] One way that we can kind of reduce the likelihood of fatigue failure in our springs is by shot painting which increases the fatigue
[00:36:41 - 00:36:46] life by putting compressive stresses into the material surface.
[00:36:46 - 00:36:52] Therefore, making it less likely for us to be able to have a tensile stress that opens.
[00:36:52 - 00:36:54] And let's a crack propagator up.
[00:36:54 - 00:37:02] Also closes any kind of or reduces the amount of potential voids there are for a crack to initiate.
[00:37:02 - 00:37:11] But again, I think these are being shot-pained and we can see that they are relatively large springs.
[00:37:11 - 00:37:20] And then this is that form which you'll need to fall out as part of your assignment.
[00:37:20 - 00:37:22] So how do you go about the spring design?
[00:37:22 - 00:37:36] Often it might be some element of iteration or you might tabulate some of your results to find what amount of what values for each of the parameters might yield you the results that you want.
[00:37:36 - 00:37:40] You need to start by really clearly defining the specification that you need.
[00:37:40 - 00:37:42] Your spring to operate in.
[00:37:42 - 00:37:47] So what does the amount of deflection and what does the amount of force that needs to be applied?
[00:37:47 - 00:38:01] Then you'll use equations on pages 7.8 and 25 to iterate or work out what values of these parameters would be suitable for your given situation.
[00:38:01 - 00:38:09] And then it can be aware that in some situations these further considerations may be required.
[00:38:09 - 00:38:15] So we see an example here of a compression spring calculation.
[00:38:15 - 00:38:20] So you see that our scenario knowing what amounts of force are being applied.
[00:38:20 - 00:38:26] And what amounts of friction we expect at those different force values.
[00:38:26 - 00:38:29] So we see this one spring constant from the loads in the given geometry.
[00:38:29 - 00:38:39] So if we plot our force in our deflection, we get these two points here and we can use that to work out what our spring constant that we desire is.
[00:38:40 - 00:38:51] In from there we can use this equation here to work out the number of coils the wire diameter and the spring diameter that is needed to achieve that spring constant that we want.
[00:38:51 - 00:38:56] You can work out the shear module as using the equation earlier in the slides.
[00:38:56 - 00:39:04] And just a note here that the number of coils in cannot be more than the coil bound condition when in equals 80 divided by d.
[00:39:04 - 00:39:14] So tabulating these options within C if we plot, if we put d into the equation, here we can work out these values here.
[00:39:14 - 00:39:20] We can use the shear stress equation as well to work out what that shear stress is.
[00:39:20 - 00:39:31] And eventually hopefully you'll get one solution that will be sufficient for your design application.
[00:39:31 - 00:39:39] The shear stress is also calculated and it's calculated using this equation here which is being mentioned earlier in the slides.
[00:39:39 - 00:39:44] So you'll probably do something similar to that for your design situation.
[00:39:44 - 00:39:50] The tension springs we can see that is some similarities but also some differences.
[00:39:50 - 00:39:59] So often the pre-tension, like this one here, there is a minimum amount of force that is required before any movement in the spring will occur.
[00:39:59 - 00:40:12] So this is a failed spring from the trampoline but each of these ones here you can see we're trying to sum them down the force before they open and act and then you're way following that.
[00:40:12 - 00:40:24] We have new types of attachments. Some reason again that seem to mainly already have hooks and they can also fail by being permanently stretched.
[00:40:24 - 00:40:33] So we can see an example of here, just to too far, you know see it's not going to go back to its original state.
[00:40:33 - 00:40:44] So to increase the spring stiffness, similarly we can increase the wire thickness or reduce the number of coils or reduce the mean diameter.
[00:40:44 - 00:40:51] So here we see some examples of those spring attachments and we see a specification sheet as well.
[00:40:51 - 00:40:55] Same sort of thing is also in these slides for torsion springs.
[00:40:55 - 00:41:08] So there are many types, they can be in either direction and they're normally designed to operate through a specific angle which we will see in the specification sheet.
[00:41:08 - 00:41:15] Here are our kind of synonymous spring constant in stress calculations for our torsional springs.
[00:41:15 - 00:41:20] And then also looking at some of the different types of springs that you can have.
[00:41:20 - 00:41:27] So you could have helical torsion or spiral torsion or a number of other kind of examples.
[00:41:27 - 00:41:37] And here we see an example of a spring specification form which would be filled out if you were going to get a torsion spring manufactured.
[00:41:37 - 00:42:01] I've talked to some spring manufacturers in the past and one of the main things I guess is that they like being consulted early in the process rather than just use filling out the form and saying make it because there are some nuances that they can kind of help with to make sure that you're getting the best area for money and also get the spring that's going to operate as intended.
[00:42:01 - 00:42:13] So as you are in a graduate position and doing some spring calculations for design, definitely talk to the person or the company that you think is going to be making it.
[00:42:13 - 00:42:17] The final bits of this we see some miscellaneous springs.
[00:42:17 - 00:42:25] So teal steel portion bars are an example of the spring system that used to be used in older kind of cars.
[00:42:25 - 00:42:38] They are also more recently been used in things like if one cars, but basically using the torsion of the bar that will act as a spring for kind of a certain
[00:42:38 - 00:42:53] amount of angles of deflection. Obviously you could have protruded rods or similar that are cantilever and the bending stresses related to what the spring constant of these would be.
[00:42:54 - 00:43:09] You can have leaf springs which you might have seen if you ever had to do anything with things like car trailers in the past and then there are a very broad range of flat strip springs in all kinds of states and sizes.
[00:43:09 - 00:43:23] Here we see an example for how you would work out the spring constant for cantilevered spring, like the ones that are used in the spring free trampoline.
[00:43:23 - 00:43:25] Some other ones here just will complete this.
[00:43:25 - 00:43:45] So we do have this full-eute spring. There are ear springs, spring springs and proper vibration mounts which are slightly different and more dampers but they can have some elastic springy nature initially at least.
[00:43:45 - 00:43:54] We are not going to focus too much on these miscellaneous types but they have mainly been included in these lines that are for completeness.
[00:43:54 - 00:44:04] But I would rather spend the last 5 or 7 minutes asking or answering any kind of questions that you have about things related to the assignment.
[00:44:04 - 00:44:18] So that is the last slide here. So with that, what are the questions to have?
[00:44:18 - 00:44:24] Yeah, pens that his toes are should.
[00:44:24 - 00:44:30] I could probably put some pens down in the workshop in a bowl.
[00:44:30 - 00:44:39] Otherwise, I think in the past people have 3D printed pens or use 8mm drill bits but I will put some pens in the workshop.
[00:44:39 - 00:44:48] Yep. You definitely want to make sure that you can construct or put together your structure before the test area.
[00:44:48 - 00:44:57] Other questions.
[00:45:02 - 00:45:08] So in subsequent weeks, I think next week we do not have a tutorial because obviously we have got the testing occurring.
[00:45:08 - 00:45:16] So either in your specific calculation examples that you would want to go over in the future.
[00:45:16 - 00:45:21] So in these lecture slides there is a review of the appearing selection process.
[00:45:21 - 00:45:30] Some of them are last, which I just said I would actually want to go through all of them, which I said is not realistically enough time to go through all of them.
[00:45:30 - 00:45:36] But I will highlight some elements of the notes that kind of go through some of the stuff.
[00:45:36 - 00:45:46] So if you look at our roll of bearing additional information, you will see that on, I do not know what page it is.
[00:45:46 - 00:45:49] Apparently page 25.
[00:45:49 - 00:45:59] The example started from page 20 I suppose, which kind of goes through the process that you might take.
[00:45:59 - 00:46:04] And then it has a hand calculation that actually shows those steps in action.
[00:46:04 - 00:46:08] You see that the first bearing that I have to actually do not need the life requirements.
[00:46:08 - 00:46:09] So then I have to go and do it again.
[00:46:09 - 00:46:18] But the main point of information is to make sure that you consult the engineering, the ISKF for its manufacturer's catalog
[00:46:18 - 00:46:22] to get the values of the constants that you need.
[00:46:22 - 00:46:26] So you will see here that I have pulled some constants x and y from the table.
[00:46:26 - 00:46:31] You may have to do something similar if you do not have the exact same type of bearing route.
[00:46:31 - 00:46:34] So those values might be slightly different.
[00:46:34 - 00:46:41] So that is sort of broadly speaking covering this bearing selection process in a bearing selection example.
[00:46:41 - 00:46:48] In terms of shaft sizing, we have also shown the alternative reality check earlier in the tutorial.
[00:46:48 - 00:47:00] And then in the lecture slides, when we are talking about the ISKF under the ASME shaft calculation,
[00:47:00 - 00:47:11] then we see that on page of lecture slide 35 that we do here have an example of this ASME A is in the formula in action.
[00:47:11 - 00:47:20] And I see we want to make sure that you complete the minimum shaft diameter calculations in more than one location on your shaft route.
[00:47:20 - 00:47:23] So you probably don't have just the same time that you're everywhere.
[00:47:23 - 00:47:28] Cool. So that is another one I am kind of ticked off.
[00:47:28 - 00:47:32] For example, let's go through.
[00:47:32 - 00:47:36] And that only leaves like a clutch example.
[00:47:36 - 00:47:42] Now we kind of talked about how you would actually approach doing that calculation.
[00:47:42 - 00:47:46] But you can see here as an example or a full experiment that we could go through.
[00:47:46 - 00:47:53] So what actuation force is required for a design situation where a shaft needs to transmit 20 Newton meters of torque.
[00:47:53 - 00:48:01] So initial calculation you can assume that as a cork clutch on metal and the clutch as a single pair of plates.
[00:48:01 - 00:48:13] Question for you guys, is this enough information?
[00:48:13 - 00:48:17] 50-50? No. What else would we need to know about our clutch?
[00:48:17 - 00:48:24] The size, right? So we need to know that in the outer diameter, right?
[00:48:24 - 00:48:32] So if we selected any inner and outer diameter, we could rearrange either one of these equations depending on what we think.
[00:48:32 - 00:48:34] So never we assume uniform pressure.
[00:48:34 - 00:48:38] If we think that a cork plate is relatively flexible.
[00:48:38 - 00:48:44] We could then rearrange this for capital F. We would use our, what was it again?
[00:48:44 - 00:48:50] Cork on metal. So maybe if we assumed it was dry, we could have an F of 0.35.
[00:48:50 - 00:48:55] We could assume the minimum diameter, the inner diameter is 200 millimeters and outer,
[00:48:55 - 00:49:04] diameter is 300 millimeters. If we plug that into the equation, we would get an actuation force that we wanted, right?
[00:49:04 - 00:49:12] Everyone have it there. So if you picked a different inner and outer diameter, what I sort of said there,
[00:49:12 - 00:49:18] then basically that's just going to change the actuation force required to get that torque.
[00:49:18 - 00:49:26] We're sort of happy with talking through that example. But obviously if there are specific examples or you get stuck on suit and element self,
[00:49:26 - 00:49:33] the assignment, then if you're synonym our through saying it would be useful if we covered something like this in the lecture or the tutorial,
[00:49:33 - 00:49:36] then we can definitely make sure that that happens.
[00:49:36 - 00:49:49] Hopefully you're feeling that you have at least got a good kind of roadmap of what to do when we're to get the information that you need to come of do the assignment.
[00:49:49 - 00:49:55] And yeah, I suppose just I can reiterate that the assignment,
[00:49:55 - 00:50:01] frequently asked questions kind of says a good starting kind of point before,
[00:50:01 - 00:50:07] basically everything up until then doing your shaft diameter stuff. So the free body diagram,
[00:50:07 - 00:50:13] as I mentioned, is described there, which we touched on at the very start of the lecture.
[00:50:13 - 00:50:25] And then obviously using this March sheet as a guide is a good idea to make sure that you're spending adequate time on different aspects of your design.
[00:50:25 - 00:51:01] Cool with us with that. That's that's time. So thank you very much and we will see you next week.
[00:51:02 - 00:51:05] I once again I'll just quickly just get this up to you.
[00:51:05 - 00:51:08] That's the next slide is done then.
[00:51:34 - 00:51:36] Oh, now you're over.
[00:51:36 - 00:51:42] Thank you for that.
[00:52:25 - 00:52:29] Thank you.
[00:52:55 - 00:52:59] Thank you.
[00:53:25 - 00:53:29] Thank you.
[00:53:55 - 00:53:59] Thank you.
[00:54:25 - 00:54:29] Thank you.
[00:54:29 - 00:54:33] Thank you.
[00:54:33 - 00:54:35] Thank you.
[00:54:35 - 00:54:41] Thank you.
[00:54:41 - 00:54:45] Thank you.
[00:54:45 - 00:54:47] Thank you for that.
[00:54:47 - 00:54:51] I'll get this card point and I'll come back and see you.
[00:54:51 - 00:54:55] Thank you.

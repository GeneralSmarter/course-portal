# ENMT301-26W Lecture 52 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `168b2b92df4e33824e1bb3063bf86042c09df8753946aaa6a4e1ef7f87009f41`
Generated: 2026-06-06T06:59:50.796548+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:01:54 - 00:02:14] We'll make a start there.
[00:02:14 - 00:02:15] Right, everyone, we'll make a start there.
[00:02:15 - 00:02:21] Thank you.
[00:02:21 - 00:02:25] So as you may imagine, something
[00:02:25 - 00:02:28] to happen to our guest speaker, I've just been on the phone
[00:02:28 - 00:02:31] with her, and she's not pulled up very well this morning.
[00:02:31 - 00:02:36] So after all this effort in this folder, I guess,
[00:02:36 - 00:02:39] we've had a slight anti-climactic kind of result.
[00:02:39 - 00:02:44] She was extremely apologetic, but I
[00:02:44 - 00:02:47] guess there's that time of the year, and I remind everyone
[00:02:47 - 00:02:51] to make sure that we take care of ourselves.
[00:02:51 - 00:02:52] I do have the sheet.
[00:02:52 - 00:02:55] I don't know if we want to have it pass around or not.
[00:02:55 - 00:02:57] We get a quick vote.
[00:02:57 - 00:03:01] Does anyone really feel like they want to sign the sheet?
[00:03:01 - 00:03:02] No.
[00:03:02 - 00:03:05] If you do, OK, well, we'll pass it up to those guys.
[00:03:05 - 00:03:07] We'll get it done.
[00:03:07 - 00:03:08] It's a pass of backwards, you know.
[00:03:08 - 00:03:13] But yeah, I do apologize a lot if it, but it's not lost.
[00:03:13 - 00:03:15] I did try and see if we can reschedule it for next week.
[00:03:15 - 00:03:18] I think she might be away, though.
[00:03:18 - 00:03:21] Or being cons with what a better time might be.
[00:03:21 - 00:03:24] Possibly the following week, and it might mean that we
[00:03:24 - 00:03:27] decide what we do with next week's lecture time.
[00:03:27 - 00:03:28] But don't worry.
[00:03:28 - 00:03:32] No, nothing lost and we'll still get some really useful
[00:03:32 - 00:03:35] knowledge out of this lecture like we always do.
[00:03:35 - 00:03:39] So to start with, I do have a timely reminder, I
[00:03:39 - 00:03:44] suppose, about performance and what
[00:03:44 - 00:03:47] I would recommend in terms of, let's try a bit.
[00:03:47 - 00:03:51] Focus a bit better.
[00:03:51 - 00:03:52] Is that clear?
[00:03:52 - 00:03:55] So here we see a graph.
[00:03:55 - 00:03:57] And stress is one of those interesting things.
[00:03:57 - 00:03:59] You have too much stress.
[00:03:59 - 00:04:02] You're too stressed to be able to do anything.
[00:04:02 - 00:04:04] But if there's not enough stress, for example,
[00:04:04 - 00:04:07] if I said, oh, yeah, guys, this bearing housing,
[00:04:07 - 00:04:10] and so I'm going to stew 20th of December,
[00:04:10 - 00:04:15] no, I would give it about it until maybe
[00:04:15 - 00:04:16] like the 15th of December.
[00:04:16 - 00:04:17] You know what I mean?
[00:04:17 - 00:04:19] Not enough stress to kind of make it top of mind.
[00:04:19 - 00:04:25] So obviously, as we kind of come to the end of the semester
[00:04:25 - 00:04:27] and the deadline is kind of being due.
[00:04:27 - 00:04:29] And there's sort of, if you're feeling a little bit
[00:04:29 - 00:04:32] stressed about this, I mean, normally that's a good thing
[00:04:32 - 00:04:36] to have a little bit of stress that moves you into an
[00:04:36 - 00:04:38] action kind of mode.
[00:04:38 - 00:04:41] The second kind of plot that I've got here
[00:04:41 - 00:04:46] is essentially the law of diminishing returns, right?
[00:04:46 - 00:04:50] So at some point in the assignment,
[00:04:50 - 00:04:53] you're going to start kind of doing work that doesn't really
[00:04:53 - 00:04:55] result in any difference in the grade that you're kind of
[00:04:55 - 00:04:56] kidding, right?
[00:04:56 - 00:04:57] I'm sure we've all kind of been there.
[00:04:57 - 00:04:59] And this is just a reminder for everyone, I suppose,
[00:04:59 - 00:05:00] as engineers.
[00:05:00 - 00:05:04] Each year's really good at being quite efficient with their time
[00:05:04 - 00:05:06] and being able to judge what is about the amount of time
[00:05:06 - 00:05:08] that should be spent on something.
[00:05:08 - 00:05:11] That's part of why we get you to do time sheets so that then
[00:05:11 - 00:05:13] when you have similar kind of design assumptions,
[00:05:13 - 00:05:16] oh yeah, and the past has taken me about this much time
[00:05:16 - 00:05:19] to write it up or this much time to do the CAD or similar.
[00:05:19 - 00:05:21] But if you start feeling like you're just going around
[00:05:21 - 00:05:25] in circles and updating things that have already kind of been
[00:05:25 - 00:05:29] OK, but you want to just double make sure then.
[00:05:29 - 00:05:33] That's a good reality check to kind of think, OK, is this
[00:05:33 - 00:05:37] actually going to make a difference in my grade?
[00:05:37 - 00:05:41] And so for this assignment in particular, what I often see
[00:05:41 - 00:05:48] is that people will spend a lot of time on these 17 marks.
[00:05:48 - 00:05:50] So a lot of the questions that I've got so far are about these.
[00:05:50 - 00:05:54] And I think it is good to get them right or at least get them
[00:05:54 - 00:05:56] 80% right.
[00:05:56 - 00:06:00] But I wouldn't recommend once you've got some loads and
[00:06:00 - 00:06:01] moment diagrams.
[00:06:02 - 00:06:04] You go and do those multiple times because you want to make
[00:06:04 - 00:06:11] slight changes to the layout or the specifics of your system.
[00:06:11 - 00:06:14] So this year I've tried to avoid that for you guys by making it
[00:06:14 - 00:06:16] really clear that the sprocket is in the middle of the two
[00:06:16 - 00:06:19] bearings and the bearings are at a set-set distance.
[00:06:19 - 00:06:23] And as Caitlin reminded me, the zid configuration of the
[00:06:23 - 00:06:27] secondary moments only relies on that A distance there.
[00:06:27 - 00:06:29] So we won't have students coming and telling me, oh, I have to
[00:06:29 - 00:06:32] redo my free body diagrams because I didn't have enough space
[00:06:32 - 00:06:34] at it into my shaft.
[00:06:34 - 00:06:39] So hopefully you're all able to kind of get the loads and
[00:06:39 - 00:06:42] moment diagrams kind of done and ticked off.
[00:06:42 - 00:06:45] Is anyone who's done their loads and moments?
[00:06:45 - 00:06:47] No, I'm happy with them.
[00:06:47 - 00:06:50] Cool, maybe six of the class.
[00:06:50 - 00:06:54] I'd say that this is like it's a good thing to get done
[00:06:54 - 00:06:57] because anything just kind of relays back to it.
[00:06:57 - 00:07:00] So then when you go to do your shaft calculation, it can be
[00:07:00 - 00:07:03] very much once you get a shaft diameter.
[00:07:03 - 00:07:05] You're okay and you're done sort of thing.
[00:07:05 - 00:07:11] So the, yeah, so you're a pecum material.
[00:07:11 - 00:07:14] And if you've got your sheer force in beginning moment diagrams,
[00:07:14 - 00:07:16] you'll know, oh, this is what the moment is at this point in the
[00:07:16 - 00:07:17] shaft.
[00:07:17 - 00:07:19] I know how much torque is being transmitted at this point in the
[00:07:19 - 00:07:20] shaft.
[00:07:20 - 00:07:22] Therefore, this is the shaft diameter.
[00:07:22 - 00:07:24] And that is done and can be moved on.
[00:07:24 - 00:07:27] So similar with each of these things, alternative reality
[00:07:27 - 00:07:29] checks, having a key way.
[00:07:29 - 00:07:31] So we want to make sure that you've at least got one key way in
[00:07:31 - 00:07:32] your design.
[00:07:32 - 00:07:34] It could be for the sprocket.
[00:07:34 - 00:07:38] It could be for the coupling.
[00:07:38 - 00:07:39] We just want to make sure that you've got one there.
[00:07:39 - 00:07:44] And then so we see that in there are our machine elements
[00:07:44 - 00:07:45] selections that we want.
[00:07:45 - 00:07:48] So our bearing selection, our seals, and some of our overall
[00:07:48 - 00:07:49] design.
[00:07:49 - 00:07:53] And so often, if a student is to not do well, what ends up
[00:07:53 - 00:07:56] happening is they spend lots of time on this part.
[00:07:56 - 00:07:58] They get 17 out of 17.
[00:07:58 - 00:08:00] They do about half of this.
[00:08:00 - 00:08:03] And then they do no clutch calculations.
[00:08:03 - 00:08:07] And if we're unlucky, they don't submit drawings or
[00:08:07 - 00:08:07] something like that.
[00:08:07 - 00:08:11] And they very quickly lose a large proportion of the marks.
[00:08:11 - 00:08:14] So making sure that you're working on stuff that's going to
[00:08:14 - 00:08:19] add to what your assignment is important.
[00:08:19 - 00:08:20] Cool.
[00:08:20 - 00:08:23] So what I'm going to do because Josie wasn't able to be here
[00:08:23 - 00:08:25] today is basically go over what we were going to go over
[00:08:25 - 00:08:26] the next week.
[00:08:26 - 00:08:31] And then we do have a plan of attack going forward, which
[00:08:31 - 00:08:34] will communicate to you on learn.
[00:08:34 - 00:08:38] So one of the notices that we've got is obviously the main
[00:08:38 - 00:08:42] design area is in the dotted circle.
[00:08:42 - 00:08:46] And so that is the bearing and the housing that we want you
[00:08:46 - 00:08:49] to be designing.
[00:08:49 - 00:08:54] You should be aware in any design that some effects may be
[00:08:54 - 00:08:56] insignificant and can be ignored.
[00:08:56 - 00:09:01] Now, as we are relatively speaking young engineers,
[00:09:01 - 00:09:05] we don't necessarily have the engineering intuition and the
[00:09:05 - 00:09:08] cloud-co-hind our name of being a child of permission engineer
[00:09:08 - 00:09:11] to just be able to say, oh, this isn't significant, so I'm
[00:09:11 - 00:09:11] not going to do it.
[00:09:11 - 00:09:15] And so that's why in these assignments I ask you to kind of
[00:09:15 - 00:09:18] show things that might be semi pointless.
[00:09:18 - 00:09:21] For example, some people when they do their any moment in
[00:09:21 - 00:09:25] shear force diagrams, it might only be one direction that the
[00:09:25 - 00:09:29] forces are actually acting, but I want you to show that other
[00:09:29 - 00:09:36] directions that we definitely can see that I at zero and that's
[00:09:36 - 00:09:40] relevant and OK when you go moving forward to make your
[00:09:40 - 00:09:44] shaft diameter calculations.
[00:09:44 - 00:09:45] Cool.
[00:09:45 - 00:09:47] So please include a discussion of how the system is to be
[00:09:47 - 00:09:50] in simple domain teams, how the components are properly
[00:09:50 - 00:09:53] located, referred to a penises that's required.
[00:09:53 - 00:09:55] So this is just something to highlight in your report.
[00:09:55 - 00:10:00] And when it comes to the assignment, we do want to make sure
[00:10:00 - 00:10:03] that you have a workable design.
[00:10:03 - 00:10:06] And so one way to do that is if you explicitly say, oh,
[00:10:06 - 00:10:10] this is how it goes together in your report and then take it
[00:10:10 - 00:10:14] apart, you do the steps and reverse, then that is a really
[00:10:14 - 00:10:17] clear way to communicate that.
[00:10:17 - 00:10:18] Cool.
[00:10:18 - 00:10:21] So from the last lecture, we had these kind of relationships
[00:10:21 - 00:10:26] between our belt tension and our torque, that is, we
[00:10:26 - 00:10:28] transmitted in our radius.
[00:10:28 - 00:10:31] And I'm sure many of you have used this in coming up with
[00:10:31 - 00:10:35] your chain tension for your system.
[00:10:35 - 00:10:40] Now a reminder that we do want your hand calculations set
[00:10:40 - 00:10:42] out nice and clearly.
[00:10:42 - 00:10:44] I didn't have any major issues actually in the first
[00:10:44 - 00:10:47] assessment, but this is just an encouragement to keep up
[00:10:47 - 00:10:48] the good work.
[00:10:48 - 00:10:51] And also an opportunity to highlight to you that this
[00:10:51 - 00:10:54] example calculation, which earlier had sort of been saying,
[00:10:54 - 00:10:57] oh, this is the layout that we want you to use.
[00:10:57 - 00:11:00] There's actually an example of a keyway calculation, which
[00:11:00 - 00:11:03] also might be a useful example to highlight as you go into
[00:11:03 - 00:11:05] doing your bearing housing.
[00:11:05 - 00:11:10] So we can see here that this person has done a sharing of
[00:11:10 - 00:11:14] their key calculation, along with a crushing of their shafts,
[00:11:14 - 00:11:16] to work out what links would be required.
[00:11:16 - 00:11:20] And then to determine which link they would use and
[00:11:20 - 00:11:23] they therefore also would know what does the likely mode
[00:11:23 - 00:11:26] of failure for their keyway.
[00:11:26 - 00:11:27] And so they've gone the step further following their
[00:11:27 - 00:11:31] tolerance of also while following the effect of safety
[00:11:31 - 00:11:32] of provided a tolerance.
[00:11:32 - 00:11:36] That we see that these are the kind of main parts of our
[00:11:36 - 00:11:41] equations that we want to have highlighted.
[00:11:41 - 00:11:41] Cool.
[00:11:41 - 00:11:44] So because I wasn't expecting to be doing a casting
[00:11:44 - 00:11:46] which, as I walked over here, I didn't bring any of my
[00:11:46 - 00:11:48] casting neck necks.
[00:11:48 - 00:11:52] But what we'll talk about in brief on this lecture is the
[00:11:52 - 00:11:53] casting process.
[00:11:53 - 00:11:56] We'll talk about the importance of the part line and
[00:11:56 - 00:12:00] wear this part lineers and how complicated it can or can
[00:12:00 - 00:12:01] not be.
[00:12:01 - 00:12:04] We'll talk about patterns, cores and runners.
[00:12:04 - 00:12:08] And then we'll go over some design points to keep in mind,
[00:12:08 - 00:12:13] which are useful if you have to design any kind of casting or
[00:12:13 - 00:12:15] injection molded part.
[00:12:15 - 00:12:19] A lot of the time these are quite comparable design points
[00:12:19 - 00:12:20] to consider.
[00:12:20 - 00:12:24] And at the end, we will see some stuff with investment
[00:12:24 - 00:12:26] casting as a comparison.
[00:12:26 - 00:12:28] So these are the references that we use.
[00:12:28 - 00:12:32] And again, you can see there are lots of useful books on
[00:12:32 - 00:12:36] these kinds of things that have been around for a long time.
[00:12:36 - 00:12:41] So before the invention of 3D printing, it wasn't too
[00:12:41 - 00:12:45] many ways that you could get a really complex organic shape
[00:12:45 - 00:12:47] into your past.
[00:12:47 - 00:12:53] So the two ways that you could do it is you might form it or
[00:12:53 - 00:12:54] you might kind of cast it.
[00:12:54 - 00:12:59] And so what we see here, we are subject to the zal
[00:12:59 - 00:13:00] machining.
[00:13:00 - 00:13:03] And so in the past, what you can see is that we didn't have
[00:13:03 - 00:13:06] this blue line of additive manufacturing.
[00:13:06 - 00:13:09] And so there was this trade-off point that if you were
[00:13:09 - 00:13:13] only making a very small number of complicated parts, it was
[00:13:13 - 00:13:17] still more cost-effective to use subjective manufacturing
[00:13:17 - 00:13:22] processes to get Tony on the CNC or the mill or the
[00:13:22 - 00:13:26] lathe to create your part.
[00:13:26 - 00:13:29] But if you were making large numbers of the parts, forming them,
[00:13:29 - 00:13:34] using something like casting becomes a very more
[00:13:34 - 00:13:37] attractive manufacturing process.
[00:13:37 - 00:13:39] But then once the additive manufacturing is coming here, we can
[00:13:39 - 00:13:45] see that the cost per part is a relatively linear kind of
[00:13:45 - 00:13:46] relationship.
[00:13:46 - 00:13:51] And so you can kind of see that that becomes really useful for
[00:13:51 - 00:13:54] coming up with prototypes that have complicated shapes.
[00:13:54 - 00:13:58] And I'm sure everyone here has kind of done 3D printing, but if
[00:13:58 - 00:14:02] you even look back maybe 15 years ago, maybe one person in the
[00:14:02 - 00:14:07] class would have been lucky enough to have had that opportunity.
[00:14:07 - 00:14:10] So we can see here that the advantages are that once you've got a
[00:14:10 - 00:14:15] pattern or a diamond, you can make many copies quite easily.
[00:14:15 - 00:14:19] And that it allows for these complex shapes, including compound curves.
[00:14:19 - 00:14:23] You're able to have varied thickness out well.
[00:14:23 - 00:14:27] And this also enables you to be able to design out any kind of
[00:14:27 - 00:14:29] stress concentrations.
[00:14:30 - 00:14:33] With these kind of variations in thickness and geometry, we do
[00:14:33 - 00:14:40] need to be aware of hard and soft zones that can be created.
[00:14:40 - 00:14:46] So you can see here comes cheaper once we have a large enough number of
[00:14:46 - 00:14:48] parts to make.
[00:14:48 - 00:14:52] So the main kind of methods include sand casting, die casting,
[00:14:52 - 00:14:58] investment casting, and centrifugal casting, they will involve
[00:14:58 - 00:15:03] injecting molten metal into a mold, but there are different kind of ways
[00:15:03 - 00:15:05] that this is done.
[00:15:05 - 00:15:11] And depending on the type of pattern that you're putting it into,
[00:15:11 - 00:15:14] or mold that you're putting it into, there's differences in the type of surface
[00:15:14 - 00:15:15] finish that you'll get.
[00:15:15 - 00:15:20] And we'll talk about a little bit of this in the future.
[00:15:20 - 00:15:23] So obviously here this is the basic kind of sand casting.
[00:15:23 - 00:15:27] You can use it for a range of metals and involves normally a wooden
[00:15:27 - 00:15:30] pattern and sand to make the mold.
[00:15:30 - 00:15:34] And often this will be done in two kind of halves.
[00:15:34 - 00:15:38] Die casting is a kind of stiff more expensive.
[00:15:38 - 00:15:43] You can imagine in terms of actually coming up with making this mold.
[00:15:43 - 00:15:48] But this middle mold or this middle die so is reusable.
[00:15:48 - 00:15:50] We're for your sand casting one obviously.
[00:15:50 - 00:15:53] Once you've pulled all the sand out and got your part,
[00:15:53 - 00:15:57] and you would have to recreate your sand mold,
[00:15:57 - 00:15:59] kind of make another part.
[00:15:59 - 00:16:03] So you see here that there's two types.
[00:16:03 - 00:16:07] You can have gravity fed or you can have pressure die casting and often
[00:16:07 - 00:16:12] different types of materials used for these processes.
[00:16:12 - 00:16:16] Investment casting uses a lost wax process.
[00:16:16 - 00:16:21] We're going to have a wax replica that then is used to make the mold.
[00:16:21 - 00:16:25] It can be used for a number of different materials as well.
[00:16:25 - 00:16:30] You'll see here the common kind of experience that the everyday kind of
[00:16:30 - 00:16:33] consumer would have is some of their jewelry.
[00:16:33 - 00:16:38] Might be done using a casting or gold twos and crowns.
[00:16:38 - 00:16:43] Again, you can imagine before we had options to 3D print or
[00:16:43 - 00:16:50] fabricate complex shapes that this was the method of choice that was used for
[00:16:50 - 00:16:51] this.
[00:16:51 - 00:16:55] Basically we've got centrifugal casting which uses molten metal and
[00:16:55 - 00:16:59] a preheated spinning die with a centrifugal force
[00:16:59 - 00:17:02] distributes this molten metal into the mold.
[00:17:02 - 00:17:07] And so I kind of often like to think of this similar to how Easter eggs
[00:17:07 - 00:17:11] can't have manufactured the same kind of idea of rotating it,
[00:17:11 - 00:17:16] but possibly spinning it at slightly higher rp ends.
[00:17:16 - 00:17:17] Cool.
[00:17:17 - 00:17:23] So typically this is just an overview of how this kind of casting process would work.
[00:17:23 - 00:17:27] So we have a hot chamber and a clamping unit on the end.
[00:17:27 - 00:17:31] And once we've got our molten metal, it will, once it's molten.
[00:17:31 - 00:17:36] It will be pushed through this chamber into the die assembly.
[00:17:36 - 00:17:43] We will get our casting in that part.
[00:17:43 - 00:17:43] Cool.
[00:17:43 - 00:17:47] So typically for sand casting components, which is the main focus that we'll be
[00:17:47 - 00:17:49] talking on, there are tin steps.
[00:17:49 - 00:17:52] So you'll have your part designed and drawn.
[00:17:52 - 00:17:55] And then you need to talk to a pattern maker who will make up the pattern.
[00:17:55 - 00:18:01] And any core boxes that are required if there are internal cavities in your
[00:18:01 - 00:18:02] part.
[00:18:02 - 00:18:08] From there, the pattern maker and foundry will install the run-off system into
[00:18:08 - 00:18:15] the pattern and then make a sand mold and use the core box to make a core.
[00:18:15 - 00:18:20] So this mold is coated and assembled with the core inside.
[00:18:20 - 00:18:24] And then once that's, I suppose, really, you're good to go in terms of
[00:18:24 - 00:18:31] unpouring your molten metal into your mold, breaking it out, removing your
[00:18:31 - 00:18:38] run-off system, and then holding and machining your component as required.
[00:18:38 - 00:18:45] So once it's finally done, it will be kind of quality assured before going into any
[00:18:45 - 00:18:50] further kind of steps if it's going into another part or another assembly or
[00:18:50 - 00:18:51] similar.
[00:18:51 - 00:18:57] So with these days, you'll see that anyone remember when only half of you had to do
[00:18:57 - 00:18:58] the drawing?
[00:18:58 - 00:19:00] Do you know what spot-facing is?
[00:19:00 - 00:19:01] Some people were nodding.
[00:19:01 - 00:19:07] Spot-facing is a classic kind of machining operation that's done on cast parts where
[00:19:07 - 00:19:11] it's just to get a nice flat surface just on the edge of the part.
[00:19:11 - 00:19:17] It's kind of similar to the counterbored part of the hole.
[00:19:17 - 00:19:18] Yeah.
[00:19:18 - 00:19:21] It's kind of like countersinking of the countersink was flat as another way,
[00:19:21 - 00:19:23] if I was really trying to do it.
[00:19:23 - 00:19:27] So those are the kind of things that, because you have this rough uneven surface,
[00:19:27 - 00:19:32] there'll be some things on your cast part that you will need to machine to make sure
[00:19:32 - 00:19:37] that it then functions correctly as the part.
[00:19:37 - 00:19:44] So in terms of the casting features, the dies have to open and close and therefore
[00:19:44 - 00:19:50] they'll be a part line where those two kind of parts of your casting of your pattern
[00:19:50 - 00:19:52] are coming together.
[00:19:52 - 00:19:53] So where is the part line?
[00:19:53 - 00:19:55] It's a fundamental question.
[00:19:55 - 00:19:58] And generally this is where I would have some parts and I would show you on the document
[00:19:58 - 00:20:02] camera, or you can see this is the part line here.
[00:20:02 - 00:20:06] And you'll be able to see that on a number of injection moulded and cast parts.
[00:20:06 - 00:20:15] So ideally, as we've kind of heard before, simple is better, basically a wall void
[00:20:15 - 00:20:20] cause of possible and all make your part cheaper to make.
[00:20:20 - 00:20:24] And so you also need to make sure that you've got an idea for suitable datums.
[00:20:24 - 00:20:29] I'm sure after doing the aluminium assignment we have a bit more an appreciation for how
[00:20:29 - 00:20:33] useful having cleared datums can be.
[00:20:34 - 00:20:39] Just to tip here, similar to I suppose making any kind of machine part, but if you talk to
[00:20:39 - 00:20:43] the person that's going to make it, they'll make your life a whole lot easier rather than
[00:20:43 - 00:20:48] trying to tell someone who's an expert how to do their job.
[00:20:48 - 00:20:55] So in this kind of slide here we see that here are our two wooden patterns and that
[00:20:55 - 00:21:01] we would use those to make our disposable sand mould.
[00:21:01 - 00:21:05] So we've got this pattern that then we can use to make the mould, we can use this pattern
[00:21:05 - 00:21:10] many times to make many moulds if we want to make many parts.
[00:21:10 - 00:21:19] So for those who are doing anything with carbon layouts in UCM or in UCHP in the future,
[00:21:19 - 00:21:27] then these kind of moulds are kind of a similar sort of thing that you will be experiencing.
[00:21:28 - 00:21:33] So from there you'll assemble your sand mould and you can see here we've got top half
[00:21:33 - 00:21:36] and our bottom half in our part in the middle.
[00:21:36 - 00:21:42] So the sand will often contain some sort of resin to stop it falling out of the box and
[00:21:42 - 00:21:46] makes it just strong enough to survive the casting process because it's not good if your
[00:21:46 - 00:21:51] sand isn't going to hold in the place that it needs to be.
[00:21:51 - 00:21:56] So in die casting the two sand moulds are replaced by two halves with a steel die.
[00:21:57 - 00:21:59] Now these can be used repeatedly.
[00:21:59 - 00:22:06] So another mould in core example we can see in this case here we've got our pattern on
[00:22:06 - 00:22:10] the top there we can use to make our mould and then we've got our core box which we can
[00:22:10 - 00:22:14] use to make our core which will sit inside our mould and this would mean that we can
[00:22:14 - 00:22:23] make this T-pipe fitting that has a hollowed out part in the middle of your part.
[00:22:23 - 00:22:30] So obviously you want to design these cores such that that easy to kind of remove when
[00:22:30 - 00:22:34] it comes to actually taking away your parts.
[00:22:34 - 00:22:38] So next we see there was talk earlier about runners and risers and it might not have been
[00:22:38 - 00:22:43] clear exactly what those are but essentially there has to be a passage for the molten
[00:22:43 - 00:22:45] metal to into the die.
[00:22:45 - 00:22:50] So we've got this pouring cup and then from there it will go into the runner and there's
[00:22:50 - 00:22:56] a riser here which basically will enable any kind of slag that's on the top to get caught
[00:22:56 - 00:23:02] and not pushed into our part as we are pouring the molten metal and obviously there's
[00:23:02 - 00:23:07] a gas vent to lift the air out as we kind of pour the middle in.
[00:23:07 - 00:23:11] So basically we'll just pour this in here and then we'll know that there's a certain
[00:23:11 - 00:23:17] level that corresponds to the top of our part once we're above that and then we can stop
[00:23:17 - 00:23:25] and then once we have lit our molten metal cool bit then we would be able to kind of
[00:23:25 - 00:23:34] cut off and machine the next parts of our cook.
[00:23:34 - 00:23:38] So we can see the runners and risers come out of the part of the finished die and must
[00:23:38 - 00:23:45] be removed and here we see the example of this external runner system still attached
[00:23:45 - 00:23:50] to the automotive sump that is being manufactured.
[00:23:50 - 00:23:55] So in terms of the runner system it's normally the responsibility for foundry to kind
[00:23:55 - 00:24:02] of design this, the experts in that area but these days there are a number of computer
[00:24:02 - 00:24:09] packages that sort of help to streamline the process in terms of designing and optimising
[00:24:09 - 00:24:12] the feed and runner systems for these kind of things.
[00:24:12 - 00:24:16] So auto-dist does have a software package called mould flow.
[00:24:16 - 00:24:23] Do you know when over there's summer job had to do anything with an addiction moulding?
[00:24:23 - 00:24:28] No one or someone might and then you might go oh yeah but basically this would be the
[00:24:28 - 00:24:34] software that modern kind of foundries would be kind of running to help with making their
[00:24:34 - 00:24:35] parts.
[00:24:35 - 00:24:41] So of course a separate piece of sand moulded by their own pattern using a core box and
[00:24:41 - 00:24:44] these create those internal cavities.
[00:24:44 - 00:24:49] So we can see that there simple component where we have our coke in our drag which are
[00:24:49 - 00:24:56] the names for our top and bottom side of our sand mould and then we've got this core in
[00:24:56 - 00:24:57] the middle.
[00:24:57 - 00:25:05] So the core has extensions which recius into the sand to make sure that we don't have any
[00:25:05 - 00:25:11] kind of molten metal there and basically makes a nicer finish in the corner.
[00:25:13 - 00:25:20] Then we have here a more complicated part with our core shape that would have to fit this
[00:25:20 - 00:25:22] internal cavity in here.
[00:25:22 - 00:25:28] So in this case again we've got these extensions on the main part.
[00:25:28 - 00:25:34] So idea would be once the part is kind of being cast then you're able to pull out the kind
[00:25:34 - 00:25:42] of sand from the core to get your finished part that has a cavity in the middle.
[00:25:42 - 00:25:48] So here we see an example of a good part line that's straight.
[00:25:48 - 00:25:56] It goes straight which makes it easy to basically make the top and bottom halves and it's
[00:25:56 - 00:26:00] also if we really needed to machine the edges here then we would be able to get rid of that
[00:26:00 - 00:26:05] part line if it was, if it was important.
[00:26:05 - 00:26:10] But often for these kind of cast for things you'll just see that surface finishes not
[00:26:10 - 00:26:15] really important unless it's where there is some sort of threaded section where it'll
[00:26:15 - 00:26:17] be connecting to other parts.
[00:26:17 - 00:26:23] So here we see an original part line which is not desirable and it means that we would
[00:26:23 - 00:26:27] have to have a much more complex mould for our part.
[00:26:27 - 00:26:34] So one thing that we would do is designers is actually to aim for having a straight part
[00:26:34 - 00:26:39] line and so we can still get the same kind of function out of the system so we can see
[00:26:39 - 00:26:44] that if it was critical that the different levels of each of these parts of the part
[00:26:44 - 00:26:50] are fairly connecting to other parts in a machine or similar then we can maintain that part
[00:26:50 - 00:26:59] of the design that improve it for casting by having that straight parting line.
[00:26:59 - 00:27:00] Cool.
[00:27:00 - 00:27:04] So when the part is to be removed we need to make sure that there is adequate draft on
[00:27:04 - 00:27:06] our mould.
[00:27:06 - 00:27:11] I know that UCM whenever they're making beer kind of carbon monocleve.
[00:27:11 - 00:27:17] This is often like the stressful time where if they haven't had enough draft angle then
[00:27:17 - 00:27:24] they have the completed chassis inside their mould and sometimes it needs a bit of encouragement
[00:27:24 - 00:27:30] over the years they have had to have some encouragement to actually get it out if they haven't
[00:27:30 - 00:27:34] kind of designed it adequately to be removed.
[00:27:34 - 00:27:40] So generally one to three degrees it's thinly enough to eight degrees internally.
[00:27:40 - 00:27:46] So the other thing here is obviously by having that angle as soon as the part is lifted
[00:27:46 - 00:27:50] out then there's a gap that is maintained right.
[00:27:50 - 00:27:57] So often for things that have a surface finish that can be easily damaged these kind of drafting
[00:27:57 - 00:28:02] angles help to reduce the risk of having damages you pull it up the surface.
[00:28:02 - 00:28:06] So you can imagine if it was completely parallel then it's just going to be completely
[00:28:06 - 00:28:12] scratched if there is some sort of surface and perfection on the edge.
[00:28:12 - 00:28:20] So again basically an example showing that.
[00:28:20 - 00:28:25] So we're possible we want to simplify our mould and to do this we would reduce the number
[00:28:25 - 00:28:26] of parts.
[00:28:26 - 00:28:31] So if they have some funny terminologies you can see here in this case in the left we have
[00:28:31 - 00:28:38] designed our part in a way that we have to have a drag, a cope, and a cheek which basically
[00:28:38 - 00:28:43] is going to take more time to manufacture and that's going to mean that it costs more
[00:28:43 - 00:28:44] to make your part.
[00:28:44 - 00:28:49] So similarly you'll see that if it wasn't critical that there is this flanged part on
[00:28:49 - 00:28:57] the edge you can slightly update your design such that you have a nice kind of angled
[00:28:57 - 00:29:02] surface here and then you only need to have a cope and a drag and a core to make the
[00:29:02 - 00:29:03] part.
[00:29:03 - 00:29:08] So fewer part lines is better.
[00:29:08 - 00:29:13] Here we see some examples showing that you should avoid having undercuts.
[00:29:13 - 00:29:21] So again we can see in this case here we would have to have multiple cores.
[00:29:21 - 00:29:26] Here we don't have to have a core on the inside and then with this part here we wouldn't
[00:29:26 - 00:29:30] need to have a core to make the part.
[00:29:30 - 00:29:36] So avoiding having those undercuts is desirable and this is the kind of thing that as you
[00:29:36 - 00:29:39] talk, what if you're at the start of the process of designing a part, if you talk to someone
[00:29:39 - 00:29:45] that is at the founder or a pedemaker then they'll pretty quickly be able to point out how
[00:29:45 - 00:29:50] to simplify your part to avoid unneeded pieces.
[00:29:50 - 00:29:56] So here we see that same part that we saw earlier a couple of slides ago that in 3D
[00:29:56 - 00:30:00] to improve the design.
[00:30:00 - 00:30:05] So again ideally because we're dealing with molten metal and this metal will have to
[00:30:05 - 00:30:13] cool as the part is being made we want to aim to have sections as uniform as possible.
[00:30:13 - 00:30:20] So if we have a design like this then that's going to cause the outside to cool faster
[00:30:20 - 00:30:25] and then we're going to get lots of voids in this kind of part here which is not good
[00:30:25 - 00:30:30] for strength and may result in kind of early failure in our part and so here we see some
[00:30:30 - 00:30:38] improvements that help to ensure that our part has beautiful wall thickness in the uniform
[00:30:38 - 00:30:40] properties throughout.
[00:30:40 - 00:30:48] So similarly you'll see that for parts like this here that you'll often reduce material
[00:30:48 - 00:30:54] that is not critically needed by changing what the section of the part looks to try and
[00:30:54 - 00:31:00] maintain this uniform cross-section.
[00:31:00 - 00:31:06] So similarly when you have some sort of lugs or feet on a part there are ways to kind of
[00:31:06 - 00:31:11] improve it through making sure that that wall thickness is uniform.
[00:31:11 - 00:31:16] So again similar to the example earlier but for this part here because this wall thickness
[00:31:16 - 00:31:21] here is a lot thicker than the rest of the part and when it cools that's going to cause
[00:31:21 - 00:31:26] porous spots which will be weakening the foot.
[00:31:26 - 00:31:31] So a bit of design would actually end this test to have this material around the feet
[00:31:31 - 00:31:33] there.
[00:31:33 - 00:31:38] And so these hot spots can also occur if we do have sharp angles in our part.
[00:31:38 - 00:31:43] So that's another thing that you would end up avoiding when you manufacture.
[00:31:43 - 00:31:50] So where possible you avoid having these really sharp corners because basically the heat
[00:31:50 - 00:31:56] will not be able to dissipate this area very well and so you'll end up getting hot
[00:31:56 - 00:32:02] spot which is another defect that can be caused.
[00:32:02 - 00:32:11] So to put that into context we can see here that if we did have just a single piece of
[00:32:11 - 00:32:14] material and it was to solidify in three minutes.
[00:32:14 - 00:32:20] If we made it be a T junction then the redjuck reduction in the cross-section of the area
[00:32:20 - 00:32:25] that enables heat to be dissipated means that this part in here is actually solid in
[00:32:25 - 00:32:28] four minutes, we have the rest, there's in three minutes.
[00:32:28 - 00:32:34] We had another one then this junction takes a lot longer to cool and so to try and avoid
[00:32:34 - 00:32:42] that if we remove the sharp edges and we're able to kind of avoid some of the manufacturing
[00:32:42 - 00:32:49] defects or the significance of the manufacturing defects that happen in the part.
[00:32:49 - 00:32:56] So what we've seen here is that if we do have chilled parts that are cooled really
[00:32:56 - 00:33:04] quickly then this is not very desirable especially if you're the person who's machining
[00:33:04 - 00:33:05] it.
[00:33:05 - 00:33:11] So if there are these sections that cool really fast then they create hard spots due
[00:33:11 - 00:33:17] to your kind of iffy curves, I'm sure you're all familiar with your metrology but essentially
[00:33:17 - 00:33:24] as at martensite that is the kind of needle that they don't really like forming with
[00:33:24 - 00:33:28] that and so basically that's what happens there and then it's a real pain to machine
[00:33:28 - 00:33:32] and it blunts their tools and the machine is tell you about it.
[00:33:32 - 00:33:38] So again in this case we want to maintain either the heating or how it cools to make it
[00:33:38 - 00:33:43] as uniform as possible and in this case we're actually trying to make it cool slower to
[00:33:43 - 00:33:45] avoid that from happening.
[00:33:45 - 00:33:52] So we can see a few examples there where we could have a part before and after improvements
[00:33:52 - 00:33:57] being made to make it easier for people helping to manufacture.
[00:33:57 - 00:34:02] We also have to think about how you're going to get sand out of the mould in this case
[00:34:02 - 00:34:08] here as you can see if there's no opening then it's going to be super fiddly to shake
[00:34:08 - 00:34:13] all the sand just out of these openings here so the improved design is relatively simple
[00:34:13 - 00:34:20] we've just added a massive hole that the sand can be poked out of the part and we see
[00:34:20 - 00:34:25] another example of that there.
[00:34:25 - 00:34:34] So this contraction stress will happen as your part is solidifying and so similar to our
[00:34:34 - 00:34:44] idea of those porous kind of spots in your part from occurring if it is a part that is
[00:34:44 - 00:34:50] wanting to maintain a certain shape then these kind of contraction stresses need to be taken
[00:34:50 - 00:34:51] into account.
[00:34:51 - 00:34:57] So this part here if we do just have our spokes being straight when they cool depending
[00:34:57 - 00:35:04] on how they all cool there will be some amount of variation in how consistent they are
[00:35:04 - 00:35:11] and so that may alter the kind of dimensional accuracy of our part and it will induce
[00:35:11 - 00:35:17] some residual stresses into our part which aren't desirable in this case.
[00:35:17 - 00:35:21] But in this case here if we have curved spokes then the idea is that these contraction
[00:35:21 - 00:35:27] stresses will actually cause these curved members to actually straighten either so slightly
[00:35:27 - 00:35:33] and then you maintain the kind of shape and function of the part that you desire and
[00:35:33 - 00:35:39] you see that often be done that often do this in more than one plane.
[00:35:39 - 00:35:44] So again in this case here the residual contraction stresses will help to kind of keep it being
[00:35:44 - 00:35:50] straight pulling it in the tension as these cool.
[00:35:50 - 00:35:58] Again I would normally have some parts where we can kind of show that.
[00:35:58 - 00:36:04] So for all your cast parts it's often the case that some amount of machining will be done
[00:36:04 - 00:36:11] and it's important that you have considered how the data insures services will be defined.
[00:36:11 - 00:36:15] Castings are never flat or square and a good design will build data points.
[00:36:15 - 00:36:20] And so the design of the casting this will help to make sure that things can be located
[00:36:20 - 00:36:27] in machining can be done in the correct kind of place.
[00:36:28 - 00:36:35] That's the basic kind of overview for our sand castings and we will have some top 10 points
[00:36:35 - 00:36:37] at the end to consider.
[00:36:37 - 00:36:42] So in this mitt casting it is another kind of casting process that is used.
[00:36:42 - 00:36:48] You'll use a wax replica of your product before casting the final middle part and kind
[00:36:48 - 00:36:50] of similar to die casting.
[00:36:50 - 00:36:59] So with this lost wax process you're able to produce a part with a very fine surface finish
[00:36:59 - 00:37:04] and you can also handle like other casting processes, complex shapes.
[00:37:04 - 00:37:13] But this type of process is better at dealing with undercut that are challenging with other methods.
[00:37:13 - 00:37:21] So we get excellent dimensional accuracy and intricate detail which is ideal for parts
[00:37:21 - 00:37:27] in aerospace, automotive, jewellery and other industries like dentistry.
[00:37:27 - 00:37:36] So you see here here's an example of our wax replica of a part from there it will be coated
[00:37:36 - 00:37:42] with a ceramic shell or immersed in a ceramic slurry.
[00:37:42 - 00:37:49] So the wax has been melted out which will then leave you with this kind of hollow shell.
[00:37:49 - 00:37:52] So is anyone ever seen how they make candles?
[00:37:52 - 00:37:54] Is it kind of weird in the way to say?
[00:37:54 - 00:37:57] That candles you normally just start stringing in their light would dip it right.
[00:37:57 - 00:38:02] It's kind of the same thing except the parts already wax and you're dipping it into like
[00:38:02 - 00:38:03] a ceramic slurry.
[00:38:03 - 00:38:08] So you just keep dipping it in this ceramic slurry and then drying it and then you've
[00:38:08 - 00:38:14] got this nice kind of hard coating around your part.
[00:38:14 - 00:38:18] So then what they'll do is turn the part upside down and heat it up and then you'll
[00:38:18 - 00:38:23] lift with your mould and then once you've poured your molten little in there and you can
[00:38:23 - 00:38:30] break away your kind of ceramic mould round the outside and that will leave you with
[00:38:30 - 00:38:33] your nice kind of part there.
[00:38:33 - 00:38:35] So this is the process that they will kind of follow.
[00:38:35 - 00:38:40] So you'll make your cason and then make your pettin assembly and make a wax tree which
[00:38:40 - 00:38:47] is pretty exciting and then you'll dry your shell preheat it before pouring your
[00:38:47 - 00:38:50] millen and then removing your shell before finishing.
[00:38:50 - 00:38:55] So we can see here that's what we were kind of talking about and we've got some of the
[00:38:55 - 00:39:03] terminology on the slide that you would use if you were doing this.
[00:39:03 - 00:39:12] So here we see some jet ski impellers where the wax is being coated in this ceramic coat
[00:39:12 - 00:39:19] and then each pier of impellers has a shead kind of run a system and here we see them drying
[00:39:19 - 00:39:24] upside down and once dry we will max it wetter.
[00:39:24 - 00:39:30] The wax will be melted out and the molten metal will be turned, well I'll pour the molten
[00:39:30 - 00:39:32] metal into the mould here.
[00:39:32 - 00:39:36] As you'll see in all of these kind of processes, they're dealing with molten metals, they
[00:39:36 - 00:39:40] have some pretty wicked PPE that they wear.
[00:39:40 - 00:39:47] So we can see them there, there'll be two guys or two people pouring that liquid into
[00:39:47 - 00:39:48] one.
[00:39:48 - 00:39:55] So the key kind of points that you should remember or have handy if you are required
[00:39:55 - 00:39:57] to do any kind of cast part.
[00:39:57 - 00:40:00] Now for your bearing housing assignment.
[00:40:00 - 00:40:07] If you wanted to have a cast part of your housing you could or you could just work it out
[00:40:07 - 00:40:09] there that it would be machined right.
[00:40:09 - 00:40:11] You don't really have to go into too much detail.
[00:40:11 - 00:40:17] We just want to make sure that whatever you make is manufacturable.
[00:40:17 - 00:40:23] So we're not asking for detailed manufacturing drawings but possibly I'll talk about that
[00:40:23 - 00:40:28] in a hot second before we go through or after we go through these design considerations.
[00:40:28 - 00:40:33] So if possible keep the stressed areas of the part in compression and materials like cast
[00:40:33 - 00:40:37] iron have higher compressive strength compared to thin sauce strength.
[00:40:37 - 00:40:43] Around our corner and round our corners and wherever possible we should try and maintain
[00:40:43 - 00:40:46] a uniform section thickness.
[00:40:46 - 00:40:51] So this achieves our uniform cooling and avoids our hot spots or cool spots.
[00:40:51 - 00:40:56] Avoid concentrations in metal at the junction and avoid very thin sections.
[00:40:56 - 00:41:05] So on learn I have put this one here.
[00:41:05 - 00:41:11] So we see there's a few more points there but I often realize that this kind of mixture
[00:41:11 - 00:41:17] people if you're not having to use or apply the casting stuff in the very first instance
[00:41:17 - 00:41:26] then sometimes it's better to make this slightly shorter rather than longer.
[00:41:26 - 00:41:33] So with that we do have a few minutes and I wondered if you had any questions or points
[00:41:33 - 00:41:38] that you would want clarified before we go into our tutorials this afternoon.
[00:41:38 - 00:41:43] So this afternoon I'll be talking about your drawings mostly in detail.
[00:41:43 - 00:41:47] There'll obviously be an opportunity for any burning questions that you have.
[00:41:47 - 00:41:55] We'll talk about kind of what we're looking for in terms of the drawing for your assignment.
[00:41:55 - 00:42:03] So it'll be one section view of your shaft of the components attached.
[00:42:03 - 00:42:08] So you'll have some sort of the materials there and you include only really the key dimensions.
[00:42:08 - 00:42:15] So you don't have to assume that each of the parts would have a manufacturing drawing but
[00:42:15 - 00:42:19] you're not required to do that.
[00:42:19 - 00:42:31] So any questions that people have at the moment about any aspects of the assignment essentially?
[00:42:31 - 00:42:32] Yep.
[00:42:32 - 00:42:38] So for actual load the question was how much actual, actual load should we design to accommodate?
[00:42:38 - 00:42:40] It doesn't need to be a significant amount.
[00:42:40 - 00:42:48] So what I just would want to make clear is when you're assuming your shaft and your bearings
[00:42:48 - 00:42:54] in your two bearings I would assume have this kind of set up.
[00:42:54 - 00:42:58] So we've got one bearing that's actually restrained in both directions.
[00:42:58 - 00:43:03] And this is the one that attaches to our universal drive shaft.
[00:43:03 - 00:43:09] And all we want to make sure is that this thing is not going to come apart either during transport.
[00:43:09 - 00:43:16] If it's for some reason going to be put together onto a truck and then take into rainbow's end or whatever kind of place
[00:43:16 - 00:43:19] is going to have our awesome new roller coaster.
[00:43:19 - 00:43:23] And you also want to make sure that during operation someone's going to push on it or whatever
[00:43:23 - 00:43:28] that's not just like able to wander and fall apart, right?
[00:43:28 - 00:43:31] So it will be some sort of nominal value.
[00:43:31 - 00:43:32] Excellent.
[00:43:32 - 00:43:37] Could be 500 to, I don't know, 500 newtons.
[00:43:37 - 00:43:44] That's like very approximate and it's more just so that you can show me.
[00:43:45 - 00:43:53] Here we can see that I've kind of said shaft features calculations, e.g. shoulders.
[00:43:53 - 00:44:00] So there's an example of doing a compressive shoulder calculation and to do that you need an axial load.
[00:44:00 - 00:44:09] So that's where I would make some sort of assumption where you know if it was if a 500 or 1000 or 1500 newton force was applied
[00:44:09 - 00:44:12] during transportation or install.
[00:44:12 - 00:44:15] This shows that it wouldn't break.
[00:44:15 - 00:44:19] But again, this is one of those ones where this year because we don't have a massive axial load.
[00:44:19 - 00:44:26] Don't think that's going to be a huge kind of issue for your design or just a thing to check.
[00:44:26 - 00:44:33] And the main thing that we want to see is that the way that this part of your housing is designed
[00:44:33 - 00:44:40] actually makes sure that it is axially restrained in both directions.
[00:44:40 - 00:44:42] Now, is there one?
[00:44:42 - 00:44:44] Is actually restrained in both directions?
[00:44:44 - 00:44:50] Does that mean anything or is it best to look at a couple of examples?
[00:44:50 - 00:44:59] So I'll roll the bearings.
[00:44:59 - 00:45:07] This is probably got a few diagrams that will show what I am talking about.
[00:45:07 - 00:45:11] So down the end here we see this slide here, right?
[00:45:11 - 00:45:15] Which at the time you're almost like you're a George, that's some nice pretty pictures.
[00:45:15 - 00:45:20] I appreciate you going through them that I don't really see why you're talking so much about what's happening.
[00:45:20 - 00:45:29] But for each of these ones on the bottom or on the top, we should be able to tell if it's axial restrained or not, right?
[00:45:29 - 00:45:37] So this first one here, if I was, there's one where I like, I wish I had the confidence to use this pin, but every single time I've tried,
[00:45:37 - 00:45:41] it goes like things catch on fire, it's crazy.
[00:45:41 - 00:45:48] But if I was to draw an arrow, if I pushed on my shaft here, if this was my 500-newton of force,
[00:45:48 - 00:45:50] there's force going to go through this face here, right?
[00:45:50 - 00:45:54] Because this end of ring is held together with this lock nut.
[00:45:54 - 00:45:56] You won't can agree with us there.
[00:45:56 - 00:46:02] So if I push on this, the force will go through our bearing and then we'll go into this housing here.
[00:46:02 - 00:46:09] And I would assume similar to this side that there is some sort of fastness holding it in place, right?
[00:46:09 - 00:46:11] So if I push on this way, it's actually restrained.
[00:46:11 - 00:46:17] If I pulled on the shaft, force would come through this lock nut through my inner bearing race,
[00:46:17 - 00:46:23] through this ball bearing, and then through into this circle, right?
[00:46:23 - 00:46:25] And then into my housing.
[00:46:25 - 00:46:30] So this one here, I'm happy that it's actually restrained in both directions.
[00:46:30 - 00:46:34] And that's what we'll be checking for your bearing, that you're designing in the dotted line,
[00:46:34 - 00:46:36] that it does this in some way, right?
[00:46:36 - 00:46:38] So there are a number of ways that you can do that.
[00:46:38 - 00:46:45] For this one here, is this actually restrained in both directions?
[00:46:45 - 00:46:47] Americans, yes.
[00:46:47 - 00:46:49] Americans know.
[00:46:49 - 00:46:52] All right, have a think that we're going to ask that one again.
[00:46:52 - 00:46:54] So we're looking at this one here.
[00:46:54 - 00:46:56] Is there actually restrained in both directions?
[00:46:56 - 00:47:01] If I push on the shaft, will the bearing move or will it not move?
[00:47:01 - 00:47:03] So who reckons the bearing is actually restrained?
[00:47:03 - 00:47:05] Yes.
[00:47:05 - 00:47:05] Okay?
[00:47:05 - 00:47:08] Who reckons us not?
[00:47:08 - 00:47:09] Be it a response?
[00:47:09 - 00:47:09] Cool.
[00:47:09 - 00:47:11] And so we do the same process, right?
[00:47:11 - 00:47:18] If we push on the side here and there's an arrow going through, then we know that as the inner ring is how it
[00:47:18 - 00:47:19] emplace, right?
[00:47:19 - 00:47:21] So the inner ring's not going to move.
[00:47:21 - 00:47:26] However, as we keep going, there's nothing here, right?
[00:47:26 - 00:47:28] There's a gap.
[00:47:28 - 00:47:31] So in this case, it would not be actually restrained.
[00:47:31 - 00:47:34] In the same thing would happen if we pulled on it, right?
[00:47:34 - 00:47:39] So that is a purposeful design feature, because if we have like a long shaft and there are
[00:47:39 - 00:47:44] some amount of temperature differences, then we want one side that's going to keep actually
[00:47:44 - 00:47:48] restrained and one side that would be able to slightly move.
[00:47:48 - 00:47:54] And if it did have that kind of axial load put on it, that wasn't desirable, right?
[00:47:54 - 00:47:59] Where the both fixed, then when we heat it up, in the bearings we're going to have this
[00:47:59 - 00:48:04] added load, which may lead to an early failure of your system of it hasn't been designed
[00:48:04 - 00:48:05] in that way.
[00:48:05 - 00:48:06] Cool.
[00:48:06 - 00:48:07] Just one here.
[00:48:07 - 00:48:10] Put a rig and figure for a thing.
[00:48:10 - 00:48:13] Actually restrained will not actually restrained.
[00:48:13 - 00:48:14] I'm going to ask you to pull your hand up.
[00:48:14 - 00:48:22] So who reckons it?
[00:48:22 - 00:48:24] Is actually restrained?
[00:48:24 - 00:48:25] Good.
[00:48:25 - 00:48:26] Who reckons it?
[00:48:26 - 00:48:28] Is not actually restrained?
[00:48:28 - 00:48:29] Good.
[00:48:29 - 00:48:30] Cool.
[00:48:30 - 00:48:36] So we can see here again we've got everything on the bearing race held together, right?
[00:48:36 - 00:48:40] In this case there's some sort of spaces of some description or collars, but we know that
[00:48:40 - 00:48:44] the bearing in the ring is held together so we can't move in either direction.
[00:48:44 - 00:48:51] And then we've got this kind of a circular and our housing holding it together in our top
[00:48:51 - 00:48:52] unit, right?
[00:48:52 - 00:48:58] Could argue maybe there's a little bit of movement here, but I'll give it to you.
[00:48:58 - 00:48:59] Cool.
[00:48:59 - 00:49:02] So here figure 14 can be our final one that we go over.
[00:49:02 - 00:49:06] This one here is obviously X here restrained.
[00:49:06 - 00:49:08] It's got snap rings on this case.
[00:49:08 - 00:49:11] This one here might be sort of something more similar that you do.
[00:49:11 - 00:49:15] So is this one actually restrained or not?
[00:49:15 - 00:49:20] So again, hands up for X here restrained.
[00:49:20 - 00:49:22] Oh, who hands up for not?
[00:49:22 - 00:49:24] Cool.
[00:49:24 - 00:49:30] So what we see if we push on the inside, we're assuming if we assume that this is held
[00:49:30 - 00:49:32] by some sort of thing, right?
[00:49:32 - 00:49:34] If there's some sort of lock nut at the end here, then it's OK.
[00:49:34 - 00:49:37] I think for us to assume it is actually restrained.
[00:49:37 - 00:49:42] The top bearing race is definitely actually restrained.
[00:49:42 - 00:49:48] Yeah, you might do something similar to this where you have part of your housing holding
[00:49:48 - 00:49:53] it in and then the plate at the end holding your bearing in place.
[00:49:53 - 00:49:54] Cool.
[00:49:54 - 00:49:57] So I'll be floating around if you do have any questions.
[00:49:57 - 00:50:01] We'll probably probably more appropriate to do at least on that table there for the next
[00:50:01 - 00:50:04] five minutes and there are lots of questions.
[00:50:04 - 00:50:08] Then we can take it into the space outside.
[00:50:08 - 00:50:12] And otherwise I'll see you this afternoon.
[00:50:12 - 00:50:34] Yeah, it was.
[00:50:34 - 00:50:37] But I'm totally with the sector that I've seen right now.
[00:50:37 - 00:50:38] We want to see around.
[00:50:38 - 00:50:39] Oh, yeah.
[00:50:39 - 00:50:41] I bought it into your technology.
[00:50:41 - 00:50:43] Yeah, I've really got a little bit of a drink.
[00:50:43 - 00:50:44] I went from the door.
[00:50:44 - 00:50:45] So I'll see the nut data.
[00:50:45 - 00:50:46] I've made it on.
[00:50:46 - 00:50:47] Yeah.
[00:50:47 - 00:50:48] Yeah.
[00:50:48 - 00:50:49] I've made it on.
[00:50:49 - 00:50:50] I've made it on.
[00:50:50 - 00:50:51] Yeah.
[00:50:51 - 00:50:52] Yeah.
[00:50:52 - 00:50:55] I'm sure it was very important.
[00:50:55 - 00:50:57] So I'm going to go to the space.
[00:50:57 - 00:51:00] That's such a fun.
[00:51:00 - 00:51:03] I think your lecture would have been more interesting than my one, but.
[00:51:03 - 00:51:06] I thought that that kind of sucks a little bit.
[00:51:06 - 00:51:07] Yeah.
[00:51:07 - 00:51:08] OK, what about it?
[00:51:08 - 00:51:09] Yeah.
[00:51:09 - 00:51:10] OK.
[00:51:10 - 00:51:11] All right.
[00:53:11 - 00:53:12] Yeah.
[00:53:12 - 00:53:13] Yeah.
[00:53:13 - 00:53:14] Yeah.
[00:53:14 - 00:53:15] Yeah.
[00:53:15 - 00:53:16] Yeah.
[00:53:16 - 00:53:17] Yeah.
[00:53:17 - 00:53:18] Yeah.
[00:53:18 - 00:53:19] Yeah.
[00:53:19 - 00:53:20] Yeah.
[00:53:20 - 00:53:21] Yeah.
[00:53:21 - 00:53:22] Yeah.
[00:53:22 - 00:53:23] Yeah.
[00:53:23 - 00:53:24] Yeah.
[00:53:24 - 00:53:25] Yeah.
[00:53:25 - 00:53:26] Ideally.
[00:53:26 - 00:53:27] Yeah.
[00:53:27 - 00:53:28] Ideally.
[00:53:28 - 00:53:29] Yeah.
[00:53:29 - 00:53:31] Ideally you want to be like.
[00:53:31 - 00:53:32] OK.
[00:53:32 - 00:53:33] Those were years.
[00:53:33 - 00:53:34] Yeah.
[00:53:34 - 00:53:35] Yeah.
[00:53:35 - 00:53:36] 300 years.
[00:53:36 - 00:53:37] I'm probably a bit of a small bit.
[00:53:37 - 00:53:38] Yeah.
[00:53:38 - 00:53:39] Sometimes it's kind of a good good.
[00:53:39 - 00:53:40] Yeah.
[00:53:40 - 00:53:41] Yeah.
[00:53:41 - 00:53:42] Good.
[00:53:42 - 00:53:43] Yeah.
[00:53:43 - 00:53:44] I'm just like clicking on the back.
[00:53:44 - 00:53:45] All right.
[00:53:45 - 00:53:46] All right.
[00:53:46 - 00:53:47] Oh my.
[00:53:47 - 00:53:49] Yeah.
[00:53:49 - 00:53:50] Yeah.
[00:53:50 - 00:53:51] Yeah.
[00:53:51 - 00:53:53] Yeah.
[00:53:53 - 00:53:54] I mean,
[00:53:54 - 00:53:55] that's so,
[00:53:55 - 00:53:58] I can just play with the pen.
[00:53:58 - 00:54:00] It's no bigger,
[00:54:00 - 00:54:01] Yeah.
[00:54:01 - 00:54:02] I mean,
[00:54:02 - 00:54:06] so I'll just pick the big screen that I can find.

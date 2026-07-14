# ENMT301-26W Lecture 19 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_19_audio_16k_mono_32k.mp3`
Source audio SHA-256: `ba36e4f52e13621f01385c9bcd47b88ad09feba38baa236a7e5d52e288cf4480`
Generated: 2026-06-06T05:40:32.524601+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:17 - 00:00:18] Just does that.
[00:00:18 - 00:00:36] Alright, thanks everyone. We'll probably make a start there.
[00:00:36 - 00:00:37] Awesome.
[00:00:37 - 00:00:38] Great to see everyone here.
[00:00:38 - 00:00:42] Hopefully you're enjoying coming to a lecture when it's not raining.
[00:00:42 - 00:00:49] I know that I definitely am enjoying that, although there's a bit more chillies in
[00:00:49 - 00:00:50] I would have hoped.
[00:00:50 - 00:00:58] So in terms of notices, obviously I can see through the attendance of last yesterday's
[00:00:58 - 00:01:05] question and answer session.
[00:01:05 - 00:01:10] There's lots of work that's been happening over the last week, which is really good
[00:01:10 - 00:01:11] to see.
[00:01:11 - 00:01:15] And if you do have any questions, make sure to come to the tutorial this afternoon and
[00:01:15 - 00:01:19] we'll kind of go through a few kind of final things.
[00:01:19 - 00:01:21] We'll go through some more test results.
[00:01:21 - 00:01:25] There's a lot more people that have submitted their data and then we can kind of clarify
[00:01:25 - 00:01:30] anything that might be unclear, including making it crystal clear what you'll kind of
[00:01:30 - 00:01:31] be submitting.
[00:01:31 - 00:01:36] Even though it is already on the kind of a silent handout, I know that sometimes you'll
[00:01:36 - 00:01:39] just like a bit of reassurance about that doing is the right thing.
[00:01:39 - 00:01:43] So in terms of question and answers, there's not any specific ones to review.
[00:01:43 - 00:01:49] Obviously there is already like a populated, frequently asked question sort of area, which
[00:01:49 - 00:01:55] has been well, question and answer for and learn, which has got a lot of answers there.
[00:01:55 - 00:01:59] So before emailing, I'd say make sure you definitely check that and check that your answer
[00:01:59 - 00:02:01] hasn't already been answered.
[00:02:01 - 00:02:07] And if things aren't clear, I think it's often a lot easier to talk those questions and
[00:02:07 - 00:02:09] answers through.
[00:02:09 - 00:02:11] In person, so come along to the tutorial.
[00:02:11 - 00:02:16] Similar to last week, I don't think that what I've got planned will probably take the majority
[00:02:16 - 00:02:20] of the time, maybe take half the time, so there will be time for me to kind of float
[00:02:20 - 00:02:22] around and ask any specific questions that you have.
[00:02:22 - 00:02:25] So many people have been asking about calculations.
[00:02:26 - 00:02:30] I know that this is a frustrating one for students because you like different
[00:02:30 - 00:02:36] nuances, but unfortunately in this case, because the design is up to you, different
[00:02:36 - 00:02:40] designs will have different calculations that are required to do, right?
[00:02:40 - 00:02:49] So depending on the way that you design it, for example, if you have no extended flange
[00:02:49 - 00:02:54] at the end of your compression member, then there's no need to check that check there,
[00:02:55 - 00:03:00] so basically a good engineer will know how and when their design will fail and you'll
[00:03:00 - 00:03:04] do that by doing the relevant calculations for your design.
[00:03:04 - 00:03:10] If there's any questions about that, we can kind of touch on that or clarify any kind
[00:03:10 - 00:03:15] of types of calculations and how to do them in the tutorial of the staff to know.
[00:03:15 - 00:03:20] So last click here, we learned about how to design and size the shaft, and we see that
[00:03:20 - 00:03:27] we have this really nice equation here from AECME, which, I don't know why it says
[00:03:27 - 00:03:32] it's from AECME, but we see that we have our load factors in our moments as inputs
[00:03:32 - 00:03:36] and that gives us an indicative value of what our shaft diameter should be.
[00:03:36 - 00:03:41] So this is really good for a first approximation before doing any kind of further checks,
[00:03:41 - 00:03:42] right?
[00:03:42 - 00:03:47] So because you're lining the sand to kind of fill your design off.
[00:03:47 - 00:03:52] And so these are the load and load factors here for the types of loading that might be applied
[00:03:52 - 00:03:56] both for your moment and your torque.
[00:03:56 - 00:03:57] Cool.
[00:03:57 - 00:04:03] So the above equation, so this one here, you can see here it does not have anything to do
[00:04:03 - 00:04:04] with stress concentrations, right?
[00:04:04 - 00:04:09] So if you have like a shaft picture, like a shoulder, there will be a stress concentration
[00:04:09 - 00:04:11] there.
[00:04:11 - 00:04:18] So that would be a further check that you'd be required to do as an engineer to make
[00:04:18 - 00:04:23] your particular point in the shaft that your stresses with the stress concentration
[00:04:23 - 00:04:26] are not going to cause failure.
[00:04:26 - 00:04:30] Similarly, we know that it does not consider fatigue, right?
[00:04:30 - 00:04:36] So we've talked about there that we can do a first principle check and then for fatigue
[00:04:36 - 00:04:43] and we do have this example that we talked through last time where we might have a shaft
[00:04:43 - 00:04:49] that's cyclically going in between conversion and tension and that there is another
[00:04:49 - 00:04:56] similar equation that kind of includes our endurance limits to actually give a similar
[00:04:56 - 00:05:03] kind of indication for what an appropriate shaft size would be taking into account fatigue,
[00:05:03 - 00:05:04] right?
[00:05:04 - 00:05:11] So we're going to be covering fatigue a little bit more in a lace a little bit, but briefly,
[00:05:11 - 00:05:17] if you're an industry and you're designing welded or bolted joints or structural steel
[00:05:17 - 00:05:23] for loading in fatigue, AS 3990 is basically the standard that you would be using.
[00:05:23 - 00:05:25] Do you not hear the down on the floor?
[00:05:25 - 00:05:28] No one's done a summit internship with a veggie?
[00:05:28 - 00:05:29] Nope.
[00:05:29 - 00:05:30] Cool.
[00:05:30 - 00:05:35] So essentially what it does is it kind of kind of bastardizes, I suppose, your kind of
[00:05:35 - 00:05:39] factors of safety or what you're allowable stress does, right?
[00:05:39 - 00:05:45] So we drew a little plot last time that showed that, you know, depending on how big
[00:05:45 - 00:05:52] the fluctuating load is, it will indicate how many cycles your fatigue failure load
[00:05:52 - 00:05:55] will require to occur, right?
[00:05:55 - 00:06:00] So if you have a really high cyclic load then it's not going to last many cycles, but
[00:06:00 - 00:06:04] it's only a small fluctuating load then it can last a lot longer.
[00:06:04 - 00:06:10] And so what they have done is using these lines, actually defined allowable stress
[00:06:10 - 00:06:16] amplitudes, such that you design one fail in the number of cycles there that will be
[00:06:16 - 00:06:17] further better for.
[00:06:17 - 00:06:23] So just highlighting there that this is a resource that you probably may be more likely
[00:06:23 - 00:06:27] to use depending on what you do in industry.
[00:06:27 - 00:06:28] Cool.
[00:06:28 - 00:06:34] So for this lecture, we're focusing on roll of bearings, how we select them.
[00:06:34 - 00:06:38] What their features are and how you calculate their life.
[00:06:38 - 00:06:41] So we'll be going over our bearing basics and types of bearings.
[00:06:41 - 00:06:46] You see I've got a bunch that I can pass around which I think is quite nice just to see
[00:06:46 - 00:06:49] how the different kind of bearing actually differ.
[00:06:49 - 00:06:55] We'll look through how you would go about selecting a bearing for a specific design, how
[00:06:55 - 00:07:02] you would do this life calculation and how we need to consider design features to make
[00:07:02 - 00:07:06] sure that they can be installed and maintained appropriately.
[00:07:06 - 00:07:12] So obviously this stuff will be really useful for our second assignment, which I'll probably
[00:07:12 - 00:07:14] be releasing to be honest in weeks six.
[00:07:14 - 00:07:19] Obviously, I don't expect you guys to make a start in that as as common with what I've done
[00:07:19 - 00:07:23] with our first assignment, I don't want to give you guys any reason to not be able to work
[00:07:23 - 00:07:25] on it if you do want to kind of be proactive.
[00:07:25 - 00:07:31] And we will have covered most of the relevant kind of information by that time.
[00:07:31 - 00:07:34] So it's going to be useful.
[00:07:34 - 00:07:38] So we can see here there's a bunch of kind of references and then number one reference
[00:07:38 - 00:07:41] I suppose for this kind of thing is A bearing catalog.
[00:07:41 - 00:07:46] I'm not paid by SKF but they had a lot of really good resources.
[00:07:46 - 00:07:51] So back in the day, I guess this was kind of like the gold standard, I guess, in terms
[00:07:51 - 00:07:53] of the four websites being super popular.
[00:07:53 - 00:07:57] But you can see here for each of our different types of bearings, they have a bunch of
[00:07:57 - 00:07:58] information.
[00:07:58 - 00:08:04] So if I wanted to, for example, look at a spherical roller bearing, I can go down to this
[00:08:04 - 00:08:09] part of the book and it has a bunch of information about how the bearings work, what we
[00:08:09 - 00:08:14] need to consider, how we'd lubricate them, et cetera.
[00:08:14 - 00:08:20] So there's a bunch of just general information about them before actually getting into
[00:08:20 - 00:08:22] like product specifications, right?
[00:08:22 - 00:08:26] So there's like a version of this online, there's a number of versions of this online.
[00:08:26 - 00:08:29] This is the gold standard.
[00:08:29 - 00:08:32] If you had a specific question about a specific bearing, not me.
[00:08:32 - 00:08:36] I mean, I can get the same information as you.
[00:08:36 - 00:08:40] But for example, what you'll see here is on this page here, it's talking about how you calculate
[00:08:40 - 00:08:45] the equivalent dynamic load or this particular type of bearing.
[00:08:45 - 00:08:50] And so it has this formula here and then there's some kind of variables that you'll have
[00:08:50 - 00:08:53] to look up based on information that's in here, right?
[00:08:53 - 00:08:56] And so for different specific types of bearings, whether it be a spherical roller bearing
[00:08:56 - 00:09:02] or a thrust bearing or a tapered roller bearing, those equivalent dynamic loads, which
[00:09:02 - 00:09:05] I know is not really a word that needs anything to you right now.
[00:09:05 - 00:09:10] But the definitions for those for each bearing type are defined in the bearing catalog
[00:09:10 - 00:09:12] from the manufacturer.
[00:09:12 - 00:09:17] So other manufacturers will have similar types of resource, right?
[00:09:17 - 00:09:19] Cool.
[00:09:19 - 00:09:24] So it's news of the day is just some slight recent use, I suppose, in terms of bearing
[00:09:24 - 00:09:26] development.
[00:09:26 - 00:09:31] And so interestingly, SPF has unveiled a new series of bearings designed for circular
[00:09:31 - 00:09:40] use, which uses laser metal deposition, with the idea being that you can re-clare and then
[00:09:40 - 00:09:42] reuse your bearing rather than throw it out.
[00:09:42 - 00:09:47] So just an interesting thing that although these machine elements are kind of things
[00:09:47 - 00:09:52] that engineers have been developing for hundreds of years, there's still innovation
[00:09:52 - 00:09:55] happening in those areas.
[00:09:55 - 00:09:56] Cool.
[00:09:56 - 00:09:57] So what do you want to use roller bearings?
[00:09:57 - 00:10:03] Well, they will support and guide rotating machine elements with minimal friction.
[00:10:03 - 00:10:11] So this is useful as it enables a transfer of loads between different machine components.
[00:10:11 - 00:10:15] So in terms of types of rolling elements is two main types, right?
[00:10:15 - 00:10:21] So you've probably heard of before, is our ball bearing or our ball rolling elements.
[00:10:21 - 00:10:26] And generally speaking, this has a particularly small contact area, which means it has the
[00:10:26 - 00:10:30] benefits of lower friction being able to operate at higher speeds.
[00:10:30 - 00:10:35] But the trade-offers that it can hold lower loads, right?
[00:10:35 - 00:10:40] So if we look at it there, we can see that we kind of have a point contact for our ball
[00:10:40 - 00:10:42] rolling elements.
[00:10:43 - 00:10:48] Now the other kind of element that we can have is a roller where we'll have a line contact.
[00:10:48 - 00:10:53] And so as this has a larger contact area, sort of has the inverse kind of trade-off.
[00:10:53 - 00:10:59] So it's really good at holding high loads, but it has higher friction and thus is better
[00:10:59 - 00:11:01] for lower speed applications.
[00:11:01 - 00:11:08] So we can kind of see that idealized line contact lit.
[00:11:08 - 00:11:12] So what does it mean by point contact and line contact?
[00:11:12 - 00:11:20] Well if we just think about what happens when those elements deform, this is the kind
[00:11:20 - 00:11:25] of shake that those surface areas or contact areas will be.
[00:11:25 - 00:11:31] And so if we look at whose contact stresses, this is the theory that describes how curved
[00:11:31 - 00:11:35] surfaces interact when they contact each other.
[00:11:35 - 00:11:36] And we can see that.
[00:11:36 - 00:11:43] How they actually act in real life is different to this idealized point or line point
[00:11:43 - 00:11:45] of contact, right?
[00:11:45 - 00:11:50] So as they deform, you can imagine if they were something like rubber that would deform really
[00:11:50 - 00:11:57] easily, we would see that we get different kind of shapes rather than our idealized point.
[00:11:57 - 00:12:02] So under normal conditions these deformations are elastic.
[00:12:03 - 00:12:12] You can see that we get this non-linear kind of curved surface for our point contact and
[00:12:12 - 00:12:20] similarly we get a kind of rectangular contact area for our line point of contact.
[00:12:20 - 00:12:25] And so this is just useful to kind of think of when we talk about how bearings might
[00:12:25 - 00:12:28] fail and what kind of where you would expect on a bearing.
[00:12:28 - 00:12:33] You can see that these are kind of the shapes that you would end up seeing if there was
[00:12:33 - 00:12:38] particular types of wear on the surface of those bearings.
[00:12:38 - 00:12:44] So in terms of bearing components, this is more here for a general kind of terminology
[00:12:44 - 00:12:50] and clarity purposes, but we can see that bearings may have seals or shields on the outside.
[00:12:50 - 00:12:52] We have our outer ring in our inner ring.
[00:12:52 - 00:12:54] We have some sort of rolling elements.
[00:12:55 - 00:12:58] And depending on what those rolling elements are, we may have a cage to make sure that
[00:12:58 - 00:13:04] they're spaced adequately and not kind of rubbing up against each other.
[00:13:04 - 00:13:11] And so for our all rolling elements, we're our ball bearing type earrings, we use either
[00:13:11 - 00:13:17] this kind of terminology, we can see with what our bore size being, the inner diameter
[00:13:17 - 00:13:23] of our bearing, we've got our outside diameter and then we've got things like our shoulders
[00:13:23 - 00:13:26] in our inner and outer ring.
[00:13:26 - 00:13:31] So we can see an example, sure, let's give them to some examples.
[00:13:31 - 00:13:36] See that, I suppose with this one here.
[00:13:36 - 00:13:42] So this one here we have a shield on each side of our rolling element.
[00:13:42 - 00:13:46] And you can see that they come in a range of sizes.
[00:13:46 - 00:13:47] Right?
[00:13:47 - 00:13:50] So here we have a smaller ball bearing.
[00:13:50 - 00:13:56] Again, if you've ever had to replace your skateboard bearings, then you'll have seen similar
[00:13:56 - 00:13:57] kind of ones there.
[00:13:57 - 00:14:02] So what I'll pass around, this one here we can see it's been cut so that you can actually
[00:14:02 - 00:14:08] see the shields that the bearing has in it as well as the rolling element.
[00:14:08 - 00:14:13] So once I'll start passing some things around, we can have a little look.
[00:14:13 - 00:14:18] I know that these might not be the most exciting ones, but just wait, it's going to get
[00:14:18 - 00:14:19] better.
[00:14:20 - 00:14:30] So for those, for the ball bearings that I have passed around, they are just a deep groove
[00:14:30 - 00:14:31] ball bearing.
[00:14:31 - 00:14:34] So they, you can't kind of twist the bearing.
[00:14:34 - 00:14:40] It can't have any kind of moment where this one here, which I'm not going to pass around
[00:14:40 - 00:14:45] just because it's quite dirty, but you can see it's a spherical roller bearing, which
[00:14:45 - 00:14:50] enables no moment to be held at the bearing.
[00:14:50 - 00:14:57] So there's a bit of shaft misalignment that can happily kind of keep running with it.
[00:14:57 - 00:15:00] So we'll look at these kind of differences a little bit later.
[00:15:00 - 00:15:07] If you want to look at this one in a little bit, well, I've got a big spherical roller
[00:15:07 - 00:15:08] bearing.
[00:15:08 - 00:15:10] So we can wait past that one around.
[00:15:10 - 00:15:14] Go up into the next type of bearing are our roller bearings.
[00:15:14 - 00:15:16] And in this case, we're a tapered roller bearing.
[00:15:16 - 00:15:22] The main difference in terminology is that we have our cup and our cone.
[00:15:22 - 00:15:26] The rest of the terminology is fairly similar.
[00:15:26 - 00:15:27] Cool.
[00:15:27 - 00:15:33] One thing that you'll see here is that we do have this face and this kind of shoulder.
[00:15:33 - 00:15:43] So those that will be used for axle or strength and you're kind of bearing housing as required.
[00:15:43 - 00:15:45] So look at one example.
[00:15:46 - 00:15:50] World, it was talked through these before kind of chucking the rest of them on the dot camera
[00:15:50 - 00:15:53] and talking through them before our ball bearings.
[00:15:53 - 00:15:58] We can see that we have a bunch of different type of bearings.
[00:15:58 - 00:16:05] So we have some where we have our suffer lining bearings, which have those ability to kind of
[00:16:05 - 00:16:09] adjust and take some shaft misalignment.
[00:16:09 - 00:16:16] And then we have thrust bearings, which are good for having axial loads only with these
[00:16:16 - 00:16:20] ones here, deep, fruitful bearing would be good for axial and radial loads.
[00:16:20 - 00:16:28] And as we'll see here, for our roller bearings, some of these are really good at taking
[00:16:28 - 00:16:34] certain loads of directions and very bad at others.
[00:16:34 - 00:16:39] So for this straight cylindrical roller bearing, what you can see is that it will be very
[00:16:39 - 00:16:41] good at holding a radial load on the top.
[00:16:41 - 00:16:48] But if there was any load going axially, if there's absolutely nothing that stops the bearing
[00:16:48 - 00:16:50] from just falling apart.
[00:16:50 - 00:16:56] So we'll see that on the document camera and then similarly, if we have a tapered roll bearing,
[00:16:56 - 00:17:01] it's good at holding a radial load and really good at holding an axial load only in one
[00:17:01 - 00:17:02] direction.
[00:17:02 - 00:17:05] Yeah, one dead wood, one dead.
[00:17:05 - 00:17:06] So long ago.
[00:17:06 - 00:17:07] Cool.
[00:17:07 - 00:17:12] So if it goes, if we had a force gun in the other direction here, again, you're seeing that
[00:17:12 - 00:17:13] it would come apart.
[00:17:13 - 00:17:16] And so I can show that here.
[00:17:16 - 00:17:19] So we've got our cylindrical roller bearing.
[00:17:19 - 00:17:23] It's really good at holding a force going straight downwards.
[00:17:23 - 00:17:28] But if I pushed on the inner ring, it would just come out.
[00:17:28 - 00:17:29] Yeah.
[00:17:29 - 00:17:32] So we'll shut that on via.
[00:17:32 - 00:17:36] And so these are kind of considerations that you'll need to make sure that you understand
[00:17:36 - 00:17:41] and do correctly for the assignment, because generally you'll want one of your bearings
[00:17:41 - 00:17:44] to be the locating bearing, which holds the axial load.
[00:17:44 - 00:17:45] Right?
[00:17:45 - 00:17:50] So this one here, you can hold an axial load if I push on this direction going into the,
[00:17:50 - 00:17:53] I don't know, from my right to the left.
[00:17:53 - 00:17:57] But if we pushed on the other direction, we'd just completely fall apart.
[00:17:57 - 00:17:58] Right?
[00:17:58 - 00:18:03] But again, you can kind of see the different types of bearing and rolling elements.
[00:18:04 - 00:18:09] And then here we have self aligning roller bearing or a spherical roller bearing.
[00:18:09 - 00:18:13] So similar to the one that I said was a super dirty.
[00:18:13 - 00:18:19] And we can see the same sort of thing where it's able to have some amount of adjustability
[00:18:19 - 00:18:26] or take a shaft that is missile locked.
[00:18:26 - 00:18:27] Pass around, it is heavy.
[00:18:27 - 00:18:30] So don't envy yourself, I guess.
[00:18:31 - 00:18:35] I think it's nice just about a fee, different types of bearings.
[00:18:35 - 00:18:40] So only other ones that we'll have to look at next are our kind of needle roller bearings.
[00:18:40 - 00:18:48] So some of them, if space is a really important consideration, i.e., you don't have very much space.
[00:18:48 - 00:18:50] You may use a needle roller bearing.
[00:18:50 - 00:18:53] So we'll quickly have a look at some of these here.
[00:18:53 - 00:18:59] So similar to our other roller bearings, we can see a bit this one here.
[00:18:59 - 00:19:01] So there's our inner element.
[00:19:01 - 00:19:07] And then we've got a thrust bearing which is just for taking an axial load run.
[00:19:07 - 00:19:11] So often they'll be now into kind of vertically and there might be a mass kind of going
[00:19:11 - 00:19:13] down into those.
[00:19:13 - 00:19:14] Cool.
[00:19:14 - 00:19:20] I feel like we're probably okay to not pass this one around or I don't know.
[00:19:20 - 00:19:21] I think you've got enough there.
[00:19:21 - 00:19:24] If you want to look at these ones here, we can chuck them around.
[00:19:24 - 00:19:31] So before I move on, I suppose, back in the day, if you sort of say, oh, you know, you can
[00:19:31 - 00:19:33] get bearings of all kinds of sizes.
[00:19:33 - 00:19:35] And these ones here are really small.
[00:19:35 - 00:19:42] So here we see three millimeter internal diameter with a six millimeter alpha diameter stainless
[00:19:42 - 00:19:45] steel shielded deep groove ball bearing.
[00:19:45 - 00:19:49] Apparently it costs $30 probably like 20 years ago.
[00:19:49 - 00:19:54] So I'm not sure what inflation is sort of done to what that price might be now.
[00:19:55 - 00:19:58] When I started taking over this course, I thought I could really do better than that.
[00:19:58 - 00:20:02] And so like any person I went on Google and sort of tried to find out who in New Zealand
[00:20:02 - 00:20:06] stocks the smallest bearings.
[00:20:06 - 00:20:11] And there's a company called NZ miniature bearing.
[00:20:11 - 00:20:15] So I put them up and found these bad boys.
[00:20:15 - 00:20:17] So I have to zoom in quite a bit.
[00:20:17 - 00:20:25] So these are a one millimeter inner diameter or bore size three millimeter outer diameter
[00:20:25 - 00:20:27] by one millimeter width.
[00:20:27 - 00:20:29] Or footness, right?
[00:20:29 - 00:20:34] So when I first did this, what I did is I 3D printed what I claimed is New Zealand smallest
[00:20:34 - 00:20:35] refrigerant spinner.
[00:20:35 - 00:20:39] And I made the fullest decision of passing around the class and someone else dropped it
[00:20:39 - 00:20:41] and then never came back.
[00:20:41 - 00:20:45] So I won't get a pass this around, but I guess there's not like a fun fidget spinner
[00:20:45 - 00:20:46] to kind of use.
[00:20:46 - 00:20:50] But you can see that there are also sort of smaller thrust bearings here.
[00:20:50 - 00:20:56] So I think this is a 3 millimeter bore size by 8 millimeter outer diameter and again another
[00:20:56 - 00:21:00] needle roller bearing which we can kind of see there.
[00:21:00 - 00:21:04] So yeah, you can get them in the range of sizes.
[00:21:04 - 00:21:10] Obviously there's way bigger bearings than what we're passing around class as well.
[00:21:10 - 00:21:11] All right.
[00:21:11 - 00:21:13] You've got it all loaded in the catalog.
[00:21:13 - 00:21:14] Cool.
[00:21:14 - 00:21:18] So in terms of your bearing, a lot of the time that they will have some sort of protection,
[00:21:18 - 00:21:21] you'll see in the bearings that we're passing around.
[00:21:21 - 00:21:25] Some of them have no protection, some of them have a seal or a shield.
[00:21:25 - 00:21:28] So you see there's a cross-section showing each of those.
[00:21:28 - 00:21:31] And then there are a bunch of different types of seals.
[00:21:31 - 00:21:38] So we can see here there is low friction versions or non-contact seals, depending on what
[00:21:38 - 00:21:40] is required by the application.
[00:21:40 - 00:21:46] So normally for bearing manufacturers like SKF, it'll be a soft except the end of their
[00:21:46 - 00:21:53] bearing code which relates to the type of protection that is being included in that bearing.
[00:21:53 - 00:21:54] Cool.
[00:21:54 - 00:21:58] So the question you're going to probably asking right now is that you can get a bit
[00:21:58 - 00:22:00] how do you select the bearing?
[00:22:00 - 00:22:02] So what I've made is a nice flow diagram.
[00:22:02 - 00:22:07] So that if you haven't had to select the bearing before, you have a logical kind of step-by-step
[00:22:07 - 00:22:11] process that you can do to complete the process, right?
[00:22:11 - 00:22:15] So there are going to be some parts of this that are iterative.
[00:22:15 - 00:22:19] But if you go through an systematic way, it should reduce the number of iterations that
[00:22:19 - 00:22:20] you do.
[00:22:20 - 00:22:25] So to start with, if you've done your assignment, you're doing your assignment, you'll
[00:22:25 - 00:22:27] have done a free body diagram.
[00:22:27 - 00:22:30] That will have enabled you to work out what the forces are and the moments are in your
[00:22:30 - 00:22:31] shaft.
[00:22:31 - 00:22:36] That will enable you to work out what your shaft size slash sizes are for different components
[00:22:36 - 00:22:38] or different areas in your shaft.
[00:22:38 - 00:22:39] Right?
[00:22:39 - 00:22:43] From there, you'll also know what the forces are for your bearings.
[00:22:43 - 00:22:49] And that will basically be all you need to start the process of selecting a bearing.
[00:22:49 - 00:22:52] So there's three kind of main things that you'll need to consider when it comes to selecting
[00:22:52 - 00:22:53] a bearing.
[00:22:53 - 00:22:54] What is the type that is needed?
[00:22:54 - 00:22:59] What is the space that is available in your system and what are the operating conditions?
[00:22:59 - 00:23:03] Because this will enable you to make sure you pick a bearing that has the correct kind
[00:23:03 - 00:23:07] of our seal or protection or similar.
[00:23:07 - 00:23:12] In terms of type, we'll tut on that a little bit more and similarly with available space.
[00:23:12 - 00:23:15] From there, this is where it may be iterative.
[00:23:15 - 00:23:18] You need a sheet of bearing life that's going to be such that it is for purpose for your
[00:23:18 - 00:23:19] design.
[00:23:19 - 00:23:23] i.e., you might not want to replace these bearings every year.
[00:23:23 - 00:23:26] You might want to have them last 14 or 15 or 20 years.
[00:23:26 - 00:23:32] And so this, for you, and similar other bearing manufacturers, provided me instead of working
[00:23:32 - 00:23:37] out that life so you can verify that it is going to last or go to the distance.
[00:23:37 - 00:23:41] And then from there, you'll also need a sheet that's the geometry that's going to integrate
[00:23:41 - 00:23:47] with both your shaft and your bearing housing on each side of your inner outer race.
[00:23:47 - 00:23:53] From there, you'll continue with your design, specifying things like lubrication, seals,
[00:23:53 - 00:23:56] sifts, conditions, and designing the housing etc.
[00:23:56 - 00:24:00] So how do you select the type that is needed?
[00:24:00 - 00:24:05] Well, it depends on what kind of loads you'll be wearing needs to hold.
[00:24:05 - 00:24:10] So we can see if we have a deep groove ball bearing like this, it's able to take a combined
[00:24:10 - 00:24:15] load, so a small axial load and a larger radial load more generally.
[00:24:15 - 00:24:20] If we have our cylindrical roller bearings, you can see that only really good at taking
[00:24:20 - 00:24:24] a big radial load and in the opposite kind of way, if we had a thrust bearing, that
[00:24:24 - 00:24:26] only good at taking axial loads.
[00:24:27 - 00:24:32] So there is this kind of chart here that kind of shows all these different bearings
[00:24:32 - 00:24:36] that we've kind of talked through, different types are good for different kind of loads.
[00:24:36 - 00:24:43] Our roller, all bearing rolling elements have a lighter or medium load kind of holding
[00:24:43 - 00:24:47] capability where our roller elements are able to do heavier loads, right?
[00:24:47 - 00:24:56] We've seen that they're sort of similar types, similar types essentially of different
[00:24:56 - 00:24:59] roller and all bearing elements.
[00:24:59 - 00:25:02] So this is just kind of the figure to show what the difference is.
[00:25:02 - 00:25:05] I wouldn't use this to actually do any selection.
[00:25:05 - 00:25:09] I've been saying, oh yeah, if I need something that can hold combined loads, there's
[00:25:09 - 00:25:12] something in the middle here, right?
[00:25:12 - 00:25:17] The actual contact angle is not something I'll use as a design principle.
[00:25:17 - 00:25:23] What I would use is one of the tables that are in SKF of earring manufacturer, so that
[00:25:23 - 00:25:27] if you know what kind of load you need, whether it be a radial load or an axial load, you
[00:25:27 - 00:25:29] can kind of go through this and work out, okay?
[00:25:29 - 00:25:34] If I pick the deep group groove ball bearing, it's good at holding a radial load and good
[00:25:34 - 00:25:36] at holding an axial load in both direction, right?
[00:25:36 - 00:25:42] If you only needed a really strong axial load in one direction, then we would possibly
[00:25:42 - 00:25:48] pick something like an angled contact ball bearing with a single row which can hold radial
[00:25:48 - 00:25:53] loads and it's really good at holding an axial load the only in one direction.
[00:25:53 - 00:26:00] Yes, so this is only a snippet of the bearing selection table and we can see that the two
[00:26:00 - 00:26:04] that have highlighted here basically show opposite types of bearings, right?
[00:26:04 - 00:26:08] So this cylindrical roller bearing is really good at holding radial loads, that really
[00:26:08 - 00:26:15] bad at axial loads and similarly our thrust bearing really bad at radial loads, really good
[00:26:15 - 00:26:17] at axial loads in one direction.
[00:26:18 - 00:26:24] In terms of the moment load, typically we don't design our bearings to hold a moment.
[00:26:25 - 00:26:29] Yes, so you wouldn't have some like extended shaft with a mass of the
[00:26:29 - 00:26:34] end and just have one bearing typically we'd want to try and face out with those bearings
[00:26:34 - 00:26:38] after so that we only have radial loads and then we can check that the angle
[00:26:38 - 00:26:42] then our shaft does such that it's not going to impact the performance of the bearings,
[00:26:42 - 00:26:46] but we can touch on that in a little bit more detail, most likely once you have a
[00:26:46 - 00:26:49] done the assignments and you've had to think about what that kind of means.
[00:26:50 - 00:26:57] So before I forget, there is an additional PDF with these lickshaw slides that basically covers
[00:26:58 - 00:27:02] all the stuff that I have been going through and you'll see that it is
[00:27:03 - 00:27:08] these tables here which go through in more detail than what I just have on the screen.
[00:27:09 - 00:27:13] Those are also in the bearing catalogue, but you'll see here that we talk about each of the things
[00:27:13 - 00:27:18] we're going to talk about along with how the life calculations,
[00:27:18 - 00:27:23] all phenomenon load and life calculations are come seizes and there is an example calculation.
[00:27:26 - 00:27:32] Cool. So as we sort of said, moment loads, moments will arise when the bearing is loaded
[00:27:32 - 00:27:37] essentially so you have a load at the end, fire away from your bearing and so some double
[00:27:37 - 00:27:44] row bearings can take these moments but it's uncommon for bearings to be used in this way,
[00:27:44 - 00:27:50] as I sort of touched on before. What is misalignment and what kind of bearings are able to
[00:27:50 - 00:27:55] support difference alignment? So if there is static misalignment, so it could just be that your
[00:27:56 - 00:28:02] two bearings are not co-linear, so there's some angle or alignment area between your different
[00:28:02 - 00:28:08] bearings or you may have some sort of shaft deflection that causes misalignment between your inner
[00:28:08 - 00:28:16] and outer rings of your bearing. So the other type of misalignment is dynamic misalignment which may
[00:28:17 - 00:28:24] happen while the shaft is rotating and the bearing shaft deflection is what creates the misalignment.
[00:28:28 - 00:28:33] So as we said, there are some, so generally what you want to do is kind of avoid
[00:28:33 - 00:28:36] this kind of misalignment where you're possible and you might use something like a,
[00:28:37 - 00:28:43] what you've got, couplings, that's one way that you can kind of improve the flexibility of your
[00:28:43 - 00:28:49] system such that it's not the bearings that are having to take this misalignment and we do also know
[00:28:49 - 00:28:54] that bearings will be able to take some small amount of misalignment and that could be something
[00:28:54 - 00:28:59] that you could check if you were worried about this occurring. So if there was some sort of
[00:28:59 - 00:29:03] deflection in your shaft, you could work out what the angle of your shaft deflection is and
[00:29:03 - 00:29:09] make sure that that is very small so that it doesn't impact your bearings. If there was,
[00:29:09 - 00:29:14] I'm a case where there was a really large moment and that's where these kind of self, sorry,
[00:29:14 - 00:29:19] if there was a case where there was a really large deflection or shaft misalignment,
[00:29:19 - 00:29:26] that may be a case where the self-aligned earrings would be used. So they can accommodate
[00:29:26 - 00:29:34] this angular misalignment and your shaft. So the two kind of cases that we've talked about is one,
[00:29:34 - 00:29:38] there's this moment load case where a bearing is designed to purposely carry a moment,
[00:29:39 - 00:29:43] which we said was quite an uncommon thing to kind of do. All you may have to miss the alignment case
[00:29:43 - 00:29:49] where the bearing is explicitly kind of allowed to have that misalignment and you pick a bearing
[00:29:49 - 00:29:56] that can and not hold any moment, even if it wanted to. So the other thing that we saw on that,
[00:29:56 - 00:30:02] the diagram was how much space is available and so the amount of radial and axial space available
[00:30:02 - 00:30:07] and it simply may limit what bearing you can select because not every bearing is going to fit
[00:30:07 - 00:30:14] and every sort of space. So we can see here an example where we have four different needle
[00:30:14 - 00:30:20] roller bearings and each take out different amounts of space. So that may be something that you kind
[00:30:20 - 00:30:27] of toggle or iterates depending on what is allowable in your design. Similarly we see here for
[00:30:28 - 00:30:34] our deep groove ball bearings, there are a number of bearings that have the same board diameter
[00:30:34 - 00:30:41] but different outer diameters and obviously this one here would hold a lower load
[00:30:42 - 00:30:46] in this one here. So it might be a trade off when you do your bearing last calculation that you
[00:30:46 - 00:30:52] go up to it on there. Hypothetically I picked this one here and it wasn't going to be strong enough to
[00:30:52 - 00:30:58] hold the number of cycles that are needed. So I picked a bigger bearing that has the same
[00:30:58 - 00:31:03] board size. I don't have to go and change all my shaft calculations but I can show that the
[00:31:03 - 00:31:09] bearing would last the time that it is required to. Cool, you also may need to consider our
[00:31:09 - 00:31:16] operating conditions. So these are things like the bearing speed and speed ratings of the lubricant
[00:31:16 - 00:31:21] so we don't want to exceed these. It may be environmental factors such as dust
[00:31:22 - 00:31:26] and then what kind of sealing requirements are required for your bearing.
[00:31:27 - 00:31:32] Lubrication you need to make sure that if it's not like a fully sealed lubricated bearing
[00:31:32 - 00:31:40] that there is access to actually get lubrication into your system. And then depending on
[00:31:40 - 00:31:47] if you have... Well, typically this is with roller element bearings but you need to make sure that
[00:31:47 - 00:31:53] the minimum load is required because if there's not enough load on some of these bearings they
[00:31:53 - 00:32:00] will actually skid the rolling elements will kind of skid around rather than rolling. So these are
[00:32:00 - 00:32:07] all kind of things that need to be passed go checked before kind of committing to a particular bearing.
[00:32:07 - 00:32:11] So we've got a little bit more detail on each of these things. So if the bearing speed,
[00:32:11 - 00:32:17] there are limits outlined in the catalog for what speed your bearings can run at. So you want to
[00:32:17 - 00:32:23] make sure that that is net. The speed capability of the bearing is normally determined by the
[00:32:23 - 00:32:30] operating temperature. So if you go too fast in your bearing it gets too hot and that basically promotes
[00:32:30 - 00:32:40] a premature failure of your bearing. Nice. Bearing lubrication so obviously to ensure our operation
[00:32:40 - 00:32:48] is reliable our bearings need to be lubricated to prevent metal on metal kind of rubbing or
[00:32:48 - 00:32:54] contact kind of happening between moving parts. And we also want to predict against corrosion.
[00:32:54 - 00:33:01] And so lubricant is what does the job of both of these things. So there are a range of different
[00:33:01 - 00:33:05] types of lubricants. Yes, they have to share the really good tool. They say oh if you've got
[00:33:05 - 00:33:12] the bearing this is the kind of lubricant or type of grease that we would recommend. So you can
[00:33:12 - 00:33:18] use that tool to your advantage that you can see here that there are different types of lubricants
[00:33:18 - 00:33:25] of different viscosities. And depending on what the kind of speed and lubricants are it may be
[00:33:25 - 00:33:32] a grease. Basically the most common lubricant for bearings they use to consider some
[00:33:33 - 00:33:39] applications may use oil or gas if it's going really fast or you may use like a solid kind of
[00:33:39 - 00:33:48] graphite type lubricant if you've got a really slow high load application. Again this is just
[00:33:48 - 00:33:53] indicative and what I would say is just do what the bearing catalog kind of says to do.
[00:33:54 - 00:33:58] Also we see that we've got grease and oil as possible lubrications.
[00:34:00 - 00:34:06] Under normal conditions grease is basically the go-to type of lubrication where oil is used for
[00:34:06 - 00:34:13] higher operating speeds where the temperature that grease would get to would be an issue.
[00:34:15 - 00:34:21] So we can see here as an example of an oil bar. So if you had oil in your system as your lubrication
[00:34:21 - 00:34:25] you might have some sort of oil bar for the bottom here. So in the area where the oil just sits
[00:34:26 - 00:34:32] that will enable the bearing to kind of self lubricate itself as it rolls around. They can show
[00:34:32 - 00:34:39] that the oil is kind of getting into the bearing. Cool. In terms of speed ratings we can see
[00:34:40 - 00:34:48] that these are quoted by the lubrication in the bearing tables. Speed ratings give the bearing
[00:34:48 - 00:34:53] speed rating for a given bearing representative. The speed at work under the load cross-plumbing to a
[00:34:53 - 00:35:03] life of 10,000,000 hours or a life of 150,000 hours L-10H. So this is a bearing life. This is a type of
[00:35:03 - 00:35:11] bearing life calculation. So L-10H is like a specific length of time. We can see speed ratings apply
[00:35:11 - 00:35:20] to bearings with a no ring rotates. As we talked about earlier in order to provide set
[00:35:20 - 00:35:26] as a very satisfactory operation. Sometimes you may have to meet the minimum load requirement.
[00:35:26 - 00:35:31] And generally, if it's not explicitly told to you by the bearing manufacturer,
[00:35:32 - 00:35:40] you can use 0.02 of C or 0.01 of C which is, I believe, your static load, but you'll see this in
[00:35:40 - 00:35:47] the tables as we go. What this value kind of is. So again, there'll also be calculated using
[00:35:47 - 00:35:52] equations in the handout. If it's not met, the bearing must be subject to an additional
[00:35:52 - 00:35:57] radial load. So you might have to add each of mass into your system to make sure that your bearing
[00:35:57 - 00:36:04] is going to meet this requirement. So here we see an example where the minimum load has not been
[00:36:04 - 00:36:11] met. So it can be caused by a number of kind of things such as improper lubricant or a combination
[00:36:11 - 00:36:20] of high speed and light loads or sudden acceleration or dewcelerations or things like entry of water
[00:36:20 - 00:36:27] where this is impacted to the performance of the lubrication. Sort of hard to see, but basically
[00:36:27 - 00:36:33] this should be a nice shiny surface, but instead there's lots of marks down the top and down the
[00:36:33 - 00:36:41] bottom with the bearing and the rolling element can actually rubbing rather than rolling. So what
[00:36:41 - 00:36:48] affects the life of the bearing? Bearing life is a function of our life and our race phase, rolling
[00:36:48 - 00:36:55] elements, cage lubrication and seals. And so luckily we don't have to think about those things
[00:36:55 - 00:37:01] too specifically that will get our last kind of equation that we're able to use to calculate it.
[00:37:01 - 00:37:07] So once we're selected our bearing, we can then calculate what is called the equivalence dynamic load.
[00:37:08 - 00:37:14] Once we have this equivalent dynamic load, we can use the bearing life calculation to calculate
[00:37:14 - 00:37:23] our life and then we can evaluate and repeat if the required life was not met. So the dynamic load
[00:37:23 - 00:37:30] with rotation is 100% of the dynamic load. Static load is typically about 40% of the static load.
[00:37:30 - 00:37:38] So we can see here that C value is specified by our bearing. So this is an example of like the
[00:37:38 - 00:37:44] SPF handout. We've got our speed rating again and our limiting speed. So those are things that
[00:37:44 - 00:37:51] we would need to consider and then again. In this case we've got two zid at the end of this bearing.
[00:37:51 - 00:37:57] And so that represents this one here which looks like it has low friction seal.
[00:37:59 - 00:38:04] Oops, I'm going to see that different similarly sized bearings slightly larger.
[00:38:04 - 00:38:10] We can get it with and without the seal as these two ones here. And then here we can see on the
[00:38:10 - 00:38:17] the second page of the catalog there are a bunch of geometric dimensions and calculation factors
[00:38:17 - 00:38:26] that you'll need to note for your calculation. So for bearings loaded radially and actually
[00:38:26 - 00:38:31] generally this is the equation that you would use. This has been taken from the bearing catalog
[00:38:32 - 00:38:39] for I think a deep proof for bearing. So sometimes the specific values of x and y will depend on
[00:38:39 - 00:38:44] what type of bearing you have and you'll need to get those values from the table in that section.
[00:38:44 - 00:38:49] Rather than just what it has specifically in the notes for the one example that I've done.
[00:38:50 - 00:38:57] So we can see as I was talking about in this case table nine and table 10 of the S-CAD log that I was
[00:38:57 - 00:39:07] looking at provide information about our bearings for getting these values x and y. So the way
[00:39:07 - 00:39:11] that I kind of describe is a little bit of a following the green comes type thing because to get
[00:39:11 - 00:39:17] x and y we need to work out what our calculation factors are. Work out this number here and then
[00:39:18 - 00:39:24] use the number that's closest to get our values for e x and y to put in the equation.
[00:39:25 - 00:39:32] Now these three more like the large columns relate to these C values which are the clearances
[00:39:33 - 00:39:39] within our bearings. So types of different types of bearings will have a different kind of bearing
[00:39:39 - 00:39:48] clearance noted. So this is the equation and it looks really really simple.
[00:39:50 - 00:39:57] Sort of is but basically we can get C from our bearing catalog. This P is our equivalent dynamic load.
[00:39:57 - 00:40:01] And what we see is we need to calculate using these days here. So we need to know what our
[00:40:01 - 00:40:07] radial and axial load is at our bearings and we need to get x and y using these tables here.
[00:40:09 - 00:40:15] Cool so what you see here this life tin is the basic life rating for 90% reliability
[00:40:16 - 00:40:23] and it gives us an answer and millions of revolutions. So this exponent lowercase P don't know
[00:40:23 - 00:40:28] why they do this. They could have chosen any other letter but they just have to use the same one twice
[00:40:28 - 00:40:34] but the lowercase P is either three for ball bearings or ten over three for roller bearings.
[00:40:36 - 00:40:42] So if you do this calculation and you need a bigger life basically you need a bigger value of C.
[00:40:43 - 00:40:48] And so I don't have time to go through this example now but I probably will do it in one of the
[00:40:48 - 00:40:54] tutorials in a bit more detail but you can see here what I've done is given myself a hypothetical
[00:40:55 - 00:41:00] question and requirement for a bearing and I've gone through and done each of the steps
[00:41:01 - 00:41:06] that you guys would need to do to get that life calculation. So I think the start-off with I find out
[00:41:06 - 00:41:13] that it doesn't work for the number of cycles that I require. So then I have to redo the calculation
[00:41:13 - 00:41:18] with a bigger bearing. Hopefully at the end of the time this meets the required specification but
[00:41:18 - 00:41:24] just note it here that is an example that you can look at when you get to doing that
[00:41:24 - 00:41:28] or needing to do it in more detail. Alright, now there's also this thing called the new life
[00:41:28 - 00:41:36] equation. It has these factors out the front A1 and ASPF which basically improve the accuracy
[00:41:36 - 00:41:42] of our calculation based on environmental conditions. So we see we've got our life adjustment factor
[00:41:43 - 00:41:52] and another one based on the new life theory which are basically in tables in the catalog.
[00:41:52 - 00:41:57] So this could be a further kind of check that you could do to get a more accurate life
[00:41:57 - 00:42:05] estimate for your bearing. Cool, so finally you're the value and see if your life has been met
[00:42:05 - 00:42:10] and if not, pick another bearing either a different type or a larger bearing and repeat process.
[00:42:12 - 00:42:18] Cool, you're at also online tools which I can highlight and I had to check quickly that the links
[00:42:18 - 00:42:26] still work but if we let's see it these. So this is something that you can use to double check
[00:42:27 - 00:42:34] your hand calculation. So if you search what kind of requirements you need it. I don't know if I
[00:42:34 - 00:42:42] have that much time to do this and we see that we can pick, ooh, it's many, you can pick different
[00:42:43 - 00:42:49] earrings that may fit what we need, right? So that's another tool that you can use to kind of
[00:42:49 - 00:42:55] facilitate your selection rather than just using the catalog and you can also use that to check
[00:42:56 - 00:43:04] your kind of calculation for bearing life. And similarly we can look up, I don't know why
[00:43:04 - 00:43:13] nothing's working but if we have our bearing, so we've selected this one here, then it'll get
[00:43:13 - 00:43:22] us a bunch more information about what kind of lubrication would be appropriate. We've got to get
[00:43:22 - 00:43:27] the CAD for your bearing and a bunch of other information that will be useful for your assignment.
[00:43:27 - 00:43:30] So we're going to come to the doing your drawing, we're going to expect you to have to
[00:43:30 - 00:43:37] CAD up the drawing for the part for your bearing once you're selected when you can kind of download
[00:43:37 - 00:43:45] that. Let me see here, the same information that would be in the bearing catalog is also online.
[00:43:46 - 00:43:51] Yeah, but there also be online making nice big PDF of that bearing catalog.
[00:43:52 - 00:43:56] Cool, so before we finish I just want to go over some quick notes about bearing failure,
[00:43:57 - 00:44:04] just to make sure that we have an understanding of how you might categorize failure because
[00:44:04 - 00:44:08] a lot of the time, if you're working as an engineer you might not necessarily just be
[00:44:09 - 00:44:13] giving out new bearings here, there might be trying to work out other bearings fail and why
[00:44:13 - 00:44:17] and what do we need to redesign or change to make sure it doesn't happen again.
[00:44:17 - 00:44:23] So about 35% of failures are caused by lubrication issues, either the wrong lubrication
[00:44:23 - 00:44:29] for wrong amount or it's been applied incorrectly. About 35% are material fatigue,
[00:44:30 - 00:44:37] which can be normal life or unusual loading or caused by excessive stress. Some of it may be
[00:44:37 - 00:44:44] contamination where we've got particles kind of getting into our bearings and then other is
[00:44:44 - 00:44:51] sort of roughly a kind of 50% So I'm just going to hear you can see that each of those kind of
[00:44:51 - 00:44:59] different types of failure have a different few different possible ways that it may happen.
[00:44:59 - 00:45:05] So for example, for fatigue you may have surface initiated fatigue where there's an
[00:45:05 - 00:45:09] infection on the surface which promotes the crack or similar or maybe something that's
[00:45:09 - 00:45:16] happening within the part itself which they categorize as sub surface fatigue. Similarly you can see
[00:45:16 - 00:45:22] that for things like plastic deformation if it's overloaded then you would kind of see a specific
[00:45:22 - 00:45:29] pattern on the surface of your rolling element. So just kind of showing this here for completeness
[00:45:29 - 00:45:34] but if you do want to learn more about some of these modes of failure then there is this handy
[00:45:34 - 00:45:44] video from SKF that you can look at. So often the wear pattern is what will help you know what type of
[00:45:44 - 00:45:50] failure has occurred. So if we look at this kind of example here and we have a radial load on our
[00:45:50 - 00:45:56] bearing the rolling element down the bottom here is going to have the highest load and thus be
[00:45:56 - 00:46:02] deforming, a less thick lever most around where if we look out to the sides there's going to be
[00:46:02 - 00:46:07] less of the load transmitted through these rolling elements. Therefore we're going to have less
[00:46:07 - 00:46:15] amount of linear deformation. And so often what you'll then see on the bearing is that in the
[00:46:15 - 00:46:21] it would be a kind of consistent pattern because wear this rolling element or this part of the
[00:46:21 - 00:46:27] inner race is at the bottom there would always be the kind of maximum amount of deformation
[00:46:28 - 00:46:33] where on our outer ring we would see this pattern where it actually tapers from a very small
[00:46:33 - 00:46:40] wear pattern to the kind of maximum pattern. So this is what you'd expect from a normal wear
[00:46:40 - 00:46:48] at the end of a life of a bearing. This one here we see some lines and we've seen that it's shiny.
[00:46:48 - 00:46:54] So what this actually indicates is that there's improper lubrication essentially and that there's some
[00:46:54 - 00:47:00] metal or metal kind of contact. We can see that these lines are consistent rings around our whole
[00:47:00 - 00:47:05] kind of bearing race. And so that's why we know that that's probably not a kind of failure that's
[00:47:05 - 00:47:09] happened under normal loading conditions. We just went here as sort of what we would expect
[00:47:09 - 00:47:15] to up. So that could be caused by either particles kind of getting into your lubrication
[00:47:15 - 00:47:20] improper lubrication or it could be that whole thing of a minimum load requirement's not being met.
[00:47:22 - 00:47:28] This one here instead the pattern we see is nicely kind of spaced out. It's almost like exactly
[00:47:28 - 00:47:35] where the rolling elements are is where the wear has happened right. So it's telling us that the wear
[00:47:35 - 00:47:42] has occurred when the bearing is not rolling. So this is often indicative of something like water
[00:47:42 - 00:47:49] kind of getting into your bearing and causing corrosion between your rolling element and your
[00:47:50 - 00:47:57] races of your bearing. So again just sort of showing examples where we get those differences.
[00:47:58 - 00:48:06] Cool. So we've got not heaves of time but I'll quickly go over some of our kind of ideas around how
[00:48:06 - 00:48:11] we select our bearings if we have two bearings in an arrangement. So most typically you'll have a
[00:48:11 - 00:48:19] locating and non-locating bearing element, i.e. one that can take your axial load and then one that
[00:48:19 - 00:48:24] does not take any axial load so that our shaft is able to expand if there is heat or similar.
[00:48:24 - 00:48:30] I think we mentioned that in the past now what I've got here is a bunch of different examples
[00:48:30 - 00:48:34] which we will go through in some of the two tutorials. But essentially this one here on the left you
[00:48:34 - 00:48:42] can see is our located bearing. The inner race is held between the shaft and this locknut and the
[00:48:42 - 00:48:49] outer race by this part of our bearing housing and we have a circle at the this side. We are on this
[00:48:49 - 00:48:54] side on the right. The outer race is free to go through the left and right. So that's our
[00:48:54 - 00:49:00] locating versus non-locating. You can see here that it is a bunch of different ways that this can
[00:49:00 - 00:49:07] be done. So we see some examples here. Cost locating may be, occurs when you really want a super
[00:49:07 - 00:49:13] stiff arrangement. So one of your axial bearings, one of your bearings is taking axial load in one
[00:49:14 - 00:49:20] direction where the other is taking the axial load in the other direction. This is often for really
[00:49:20 - 00:49:27] kind of short shafts. We require a really stiff arrangement and in that case to make sure that the
[00:49:27 - 00:49:32] adequate three load is kind of knit. You will or the minimum load on your bearing is knit. You will
[00:49:32 - 00:49:40] apply a preload to your bearing arrangement by other locking nuts. So we can see some examples
[00:49:40 - 00:49:46] of that there where these kind of nuts will be fastened to get that preload mix.
[00:49:48 - 00:49:55] So we see here that there is a bunch of different methods that you can do your axial location of the
[00:49:55 - 00:50:01] bearing. And so what we can see is that these may be worth considering when it comes to doing your
[00:50:01 - 00:50:07] bearing housing assignment. There's not just one way you can actually locate a particular bearing.
[00:50:07 - 00:50:12] So you can have a lock nut. You could have some kind of plate that's put in place. You could have
[00:50:13 - 00:50:20] some sort of syruflip or have parts that are in series with one another.
[00:50:21 - 00:50:25] We'll talk about some of these things in a little bit more detail. That's all that we've got time for
[00:50:25 - 00:50:30] for today and I'll talk about a little bit of the stress concentration and stuff in the tutorial
[00:50:30 - 00:50:33] this afternoon. Thanks everyone.
[00:50:34 - 00:51:25] What's the problem with the bearing?
[00:51:25 - 00:51:30] Yep. You have any advice about the factor of safety and we should put on the PCR?
[00:51:32 - 00:51:36] Not really. So that's sort of the question where it's like
[00:51:40 - 00:51:41] and it's sort of a bit of a walk.
[00:51:53 - 00:51:58] That's fine. Like if it's going to be like for example, if there's one particular
[00:51:58 - 00:52:01] safety and one thing that's been covered in some of the problems,
[00:52:01 - 00:52:03] there's a particular block quality.
[00:52:04 - 00:52:09] All that needs to be sure is to well into the rest of the three marks of the motor face.
[00:52:12 - 00:52:16] Now where does it feel like? I'd rather be gently bright.
[00:52:17 - 00:52:18] Make that think this out. So again, you can go and work out.
[00:52:18 - 00:52:22] What load of strange motor pressure you can do now?
[00:52:22 - 00:52:24] It feels like it's super safe.
[00:52:24 - 00:52:25] It's good.
[00:52:25 - 00:52:27] It's that kind of...
[00:52:27 - 00:52:29] It's probably fine.
[00:52:29 - 00:52:32] I mean if you're using a signal, it's like it's fine.
[00:52:32 - 00:52:34] The median is one.
[00:52:34 - 00:52:36] I don't know if you can run one, but it's super warm.
[00:52:36 - 00:52:37] Two for you.
[00:52:37 - 00:52:38] Information.
[00:52:38 - 00:52:41] So yeah, unfortunately it's not really like it.
[00:52:41 - 00:52:43] I'm sure I don't think it's really good.
[00:52:43 - 00:52:45] Other than things, probably fine.
[00:52:45 - 00:52:47] I guess you can do something really hard.
[00:52:47 - 00:52:48] I guess.
[00:52:48 - 00:52:49] I guess.
[00:52:49 - 00:52:50] I guess.
[00:52:50 - 00:52:55] It's a great one, because these are the straight-ups of people.
[00:52:55 - 00:52:57] They're going to fall in the water.
[00:52:57 - 00:52:59] That's what we do.
[00:52:59 - 00:53:01] I thought it was like, are you playing at the left?
[00:53:01 - 00:53:03] I think it's not right.
[00:53:03 - 00:53:05] I think we've played with one practice.
[00:53:05 - 00:53:07] Yeah.
[00:53:07 - 00:53:09] Okay, let's get to now.
[00:53:09 - 00:53:11] Yes, that's fine.
[00:53:11 - 00:53:13] Yeah, I guess it's fine.
[00:53:13 - 00:53:15] Yes.
[00:53:15 - 00:53:17] All right, that's fine.
[00:53:17 - 00:53:18] I think we're good.
[00:53:18 - 00:53:20] Thank you so much.
[00:53:20 - 00:53:23] Okay, thank you.
[00:53:23 - 00:53:25] Okay, thank you very much.
[00:53:25 - 00:53:27] Okay, thank you.
[00:53:27 - 00:53:29] So good, thank you.
[00:53:29 - 00:53:31] Thank you, thank you.
[00:53:31 - 00:53:33] Thank you.
[00:53:33 - 00:53:35] Yeah, thank you.
[00:53:35 - 00:53:37] Thank you.
[00:53:37 - 00:53:39] All right.

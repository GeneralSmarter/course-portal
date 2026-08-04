# ENMT301-26W Lecture 25 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `d76420b8029ddf17f72b6cbe7933f4ab196ea43c087a3343b697bc1c71bc659b`
Generated: 2026-06-06T05:59:09.100539+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:07 - 00:00:40] Alright, thanks everyone. I think we'll make a start there. Alright, thanks everyone. I think we'll make a start there. Alright, thanks everyone. I think we'll make a start there.
[00:00:40 - 00:00:56] Welcome everyone. We're into episode 5, I suppose. It feels like we're in the busy time of the year. I don't know about you, but for me I'm like, holy heck how's it going.
[00:00:56 - 00:01:11] So notice as before we start and before I get into our lecture content for our tutorial today, there won't be any throughout tutorial today. There won't be any kind of formal structure.
[00:01:11 - 00:01:26] I say and then I present a formal structure, but the informal formal structure is that generally I'll ask any burning questions that people have. I think a lot of the things that I've been kind of talking about is a lot of more like clarification or just a word of encouragement of like, yeah,
[00:01:26 - 00:01:44] that sounds fine. But obviously everything that we needed for our assignment 1A, we'd kind of covered almost before last Tuesday, right? So last Tuesday we kind of really just having home exactly what we want you to make sure that you submit and remember to submit.
[00:01:44 - 00:01:52] And obviously there's an online portal that you have to submit your work to. You submit everything there and then you also do a physical copy of your drawings, right?
[00:01:52 - 00:02:12] Alongside that. So under the tutorial I'll ask, well, I don't say any burning questions generally you have before wandering around the class. So those kind of burning questions I suspect will probably go like, oh gosh, do we say something that we need to do a time sheet? Do we need to do a time sheet? And I'll go, yeah, you need to do a time sheet.
[00:02:12 - 00:02:20] And just detail what you've done on what kind of aspects of the assignment, right? So those are sort of the kind of clarification zone.
[00:02:20 - 00:02:35] So expecting rather than, you know, George, how do we do the free body diagrams or something like that, right? Cool. And then here is your I suppose your formal official reminder that the peer review was open, do it.
[00:02:35 - 00:02:47] If you're not, if you're someone that I'd like to instigate, like literally just do it right now and hope that something crazy doesn't happen over the next three days with you and your partner, right?
[00:02:47 - 00:02:55] But it's a multi choice Christian's there. You can add some details to explain your answer if you think that's required. That's not essential. That's not applicable.
[00:02:55 - 00:03:04] So just write, you know, if there were all fives, for example, believe it's one to five scale, but you'll be able to tell there and make sure that your partner does it as well.
[00:03:04 - 00:03:06] Yeah, so.
[00:03:06 - 00:03:16] So there's a penalty of five percent if you don't do it. Now this is all just like automatically calculated using the online tool. And the tool really doesn't like it.
[00:03:16 - 00:03:33] So you can forget. Basically it makes a very hard for it to calculate any grade for that 10 percent component. So that's where I say, make sure you get it done. Here's your formal thing. I'll make a post the data remind and I only make one post before it closes.
[00:03:33 - 00:03:45] Because last year I didn't do that and I got means made about me, but it's sort of fine. But we had lots of people like not answering it because it's like, it's a little bit of a pain of a tool from my end.
[00:03:45 - 00:03:58] It is a good blunt instrument. But yeah, as I say, if people haven't submitted it because there was no penalty this time last time because the first time we used it, it would just ignore it and then I'd be like, I've reopened it again.
[00:03:58 - 00:04:08] Because there's still people that haven't done it. So hopefully that kind of hits the nail on the head there.
[00:04:08 - 00:04:19] We're just having a nice clearing of concise information since we know how the kind of tool works now and what is required for everyone to get it done.
[00:04:19 - 00:04:32] So last lecture, we sort of gave a very good overview of what process you might follow when you complete the design of a bearing housing shaft arrangement.
[00:04:32 - 00:04:47] So to start with, obviously you're going to have to, you guessed it, draw a free body diagram, work out the forces at the bearings, use those pieces of information to work out what your minimum shaft sizes are at key kind of points along your shaft.
[00:04:47 - 00:05:07] So that's sort of what we talked about there. And the reason that I say key points along your shaft is sometimes you might want to calculate it with a next load, so then the awesome might be specific points of interest when you know that the bearing wants to maybe be on slightly smaller shaft and you still need to verify that that small size is going to be appropriate.
[00:05:07 - 00:05:17] Once you've got that kind of all locked in or approximately got some values to base your bearing solution off, you can go into that stage.
[00:05:17 - 00:05:26] We work out what kind of type you need, what kind of loads the bearing needs to be able to hold, whether it's just radio or just excell or a combination.
[00:05:26 - 00:05:33] How much space you've got on operating conditions will now be a bearing that has the right kind of characteristics for what you want.
[00:05:33 - 00:05:43] We're kind of highlighted there that the SKF bearing catalog or the online bearing selection tool, a very useful to kind of guide you, especially if you haven't had to select a bearing before.
[00:05:43 - 00:05:51] If you talk to someone who's been in industry for like 30 years, it's crazy how nuanced what they know about specific bearings can be.
[00:05:51 - 00:05:55] We'll have that off of that now you definitely want to more than just a deep groove ball bearing.
[00:05:55 - 00:05:58] We'll typically use this kind of one here, right?
[00:05:58 - 00:06:03] We don't have that kind of intuition yet, but that's what we're kind of developing as we go through the year.
[00:06:03 - 00:06:11] So it's probably likely that the first bearing you select might not be perfect and then you have to kind of pick another one and get it to kind of fit what you need.
[00:06:11 - 00:06:20] So to fit what you need you to make sure that's bearing life makes whatever the requirements are for your design situation and that the geometry kind of suits and it's able to be a symbol
[00:06:20 - 00:06:22] and just a symbol, right?
[00:06:22 - 00:06:27] From there you'll continue with your design and that's what we'll be sort of talking about today with lubrication and seals.
[00:06:27 - 00:06:37] You also want to specify things like the surface conditions on your housing which will impact the life of your seals as well as the rest of your design.
[00:06:37 - 00:06:41] So I'll see housing selection slash design etc.
[00:06:41 - 00:06:43] So we can see here to calculate that life.
[00:06:43 - 00:06:48] We get this brilliantly easy calculation on the face of it.
[00:06:48 - 00:06:57] So to work out our basic life, it's just capital C over capital P divided by to the power of lowercase P, right?
[00:06:57 - 00:07:03] And we're lucky that that lowercase P is either three for ball bearings or 10 over three for roller bearings.
[00:07:03 - 00:07:10] C is a load that's given by the bearing that you select, but P is something that you would calculate.
[00:07:10 - 00:07:14] So that's what they call the equivalent dynamic load.
[00:07:14 - 00:07:20] And for that different types of bearings might have a slightly different type of equation that they use.
[00:07:20 - 00:07:28] So that's kind of the following of the breadcrumbs because again that calculation for P is often quite simple at the face of it.
[00:07:28 - 00:07:34] But you have to kind of look up on tables to work out the constants that go into that calculation.
[00:07:34 - 00:07:38] So there's an example in the additional notes for the bearing selection lecture.
[00:07:38 - 00:07:43] And I'm sure we'll talk about that calculation in one of the tutorials eventually.
[00:07:43 - 00:07:46] So for today's lecture we'll be continuing.
[00:07:46 - 00:07:49] We'll start by talking a little bit about journal bearings.
[00:07:49 - 00:07:51] We'll talk a little bit about lubrication.
[00:07:51 - 00:07:53] We had a basic slide on that last week.
[00:07:53 - 00:08:02] And then we'll review a few different types of seals and sealing techniques as well as finishing on mechanical seals.
[00:08:02 - 00:08:10] So in terms of the references we can see that the classic kind of ones are coming through of Shiggly and machine design by Deutschmann.
[00:08:10 - 00:08:29] But for this and for your assignment the SKF catalog and the CR seals catalog are going to be your kind of key resource that I would select when it comes to selecting your bearing and selecting your seals for your bearing and selecting your lubrication for the bearing.
[00:08:29 - 00:08:30] All right.
[00:08:30 - 00:08:34] Because the people that make the seals often feel the make the bearings.
[00:08:34 - 00:08:35] They also make seals.
[00:08:35 - 00:08:41] They also make lubrication because they want to make sure that their whole kind of complete product works effectively.
[00:08:41 - 00:08:43] So it's kind of easy.
[00:08:43 - 00:08:49] And then here we see a nice meme that was made by students last year and I just stole one shuck in.
[00:08:49 - 00:08:55] So I thought, you know, that kind of maybe hits the point home of what I'm trying to communicate.
[00:08:55 - 00:08:56] Cool.
[00:08:56 - 00:09:10] So in terms of journal bearings, these are basically a very simple version or mechanism to make a shaft rotate freely or more freely.
[00:09:10 - 00:09:11] Right.
[00:09:11 - 00:09:17] And so basically what we have is a supportive sleeve that has a low coefficient of friction.
[00:09:17 - 00:09:20] So we can see here that there's two kind of the gym rule types.
[00:09:20 - 00:09:26] You might just have a solid bushing, maybe that we made of something like brass or similar.
[00:09:26 - 00:09:34] Or you might have a lined bushing which has some sort of super slippery coating, tifflon probably, or similar that will be one of those for
[00:09:34 - 00:09:36] other chemicals that it never goes away.
[00:09:36 - 00:09:39] But super really good for slipperyness, right?
[00:09:39 - 00:09:47] So we can see here that in terms of the types you can see that you may also have ones that are impregnated with grease.
[00:09:47 - 00:09:57] Or you might have nylon or plastic or other types of either metallic or lubricated rubber type journal bearings.
[00:09:57 - 00:10:03] And so before I kind of show you a few examples, we can see here that we can have flanged ones or straight ones.
[00:10:03 - 00:10:14] And they might have a particular preference depending on the application that you're using these to make sure that they kind of stay where you want them or to make sure that they're easily replaced.
[00:10:14 - 00:10:21] And then you will also see that in all ones that I show that they kind of have boring, groove patterns.
[00:10:21 - 00:10:35] But as kind of highlighted and shiggly there are a range of different patterns that can be applied to the inside of these journal bearings to make sure that you get either good heat dissipation or lubrication dissipation.
[00:10:35 - 00:10:37] Or a point of difference if you will.
[00:10:37 - 00:10:42] So you can have just a, you know, standard ones with no kind of pattern.
[00:10:42 - 00:10:47] We can have a kind of groove in the middle where we might be able to add lubrication.
[00:10:47 - 00:10:50] This one here, not sure if you can see, but I can pass it around.
[00:10:50 - 00:10:57] It does have a different pattern going through the journal.
[00:10:57 - 00:11:01] And then obviously sometimes you'll get ones that are made in halves.
[00:11:01 - 00:11:03] And you put two halves together.
[00:11:03 - 00:11:08] Or you might have a kind of complete ring which is often replaceable route.
[00:11:08 - 00:11:14] So the fact that it's not kind of got that flanging them is that you could kind of push it out and push another one in.
[00:11:14 - 00:11:19] And so because there's not much point, these just being up here.
[00:11:19 - 00:11:21] And it's nice to kind of look at things sometimes.
[00:11:21 - 00:11:25] I'll pass them around for people to at least kind of see.
[00:11:25 - 00:11:31] So sometimes if you just need a kind of simple solution to make sure that your shaft is going to rotate more smoothly,
[00:11:31 - 00:11:34] these are options that might be used.
[00:11:34 - 00:11:39] Also sometimes if space is a consideration, obviously these take up a lot less space.
[00:11:39 - 00:11:49] And so just in terms of some nomenclature for how these journal bearings are kind of sometimes these are the equations you might want to use.
[00:11:49 - 00:11:54] Essentially what we can see here is a bunch of definitions.
[00:11:54 - 00:12:00] And then if it was a lubricated bearing, what we see here is that because of the no slip rule,
[00:12:00 - 00:12:11] if you remember from fluids, basically there's always going to be a minimum film thickness that occurs in our bearing to make sure that the two kind of needles aren't rubbing against each other.
[00:12:11 - 00:12:15] And so there are methods that you can use to kind of calculate that.
[00:12:15 - 00:12:22] And similarly there are kind of equations that you can use to determine the coefficient of friction based on exciting things,
[00:12:22 - 00:12:28] such as the pressure that your system is running at and the dynamic viscosity of the lubrication that you're using.
[00:12:28 - 00:12:36] So sometimes if you need to calculate your coefficient of friction, that would be the method that you would use.
[00:12:36 - 00:12:44] So as we sort of touched on or as we have highlighted, there are types of journal bearings that use lubrication.
[00:12:44 - 00:12:46] And over that there are two kind of main types.
[00:12:46 - 00:12:52] We have our hydro dynamic where the lubricant is drawn into place by the motion of the services.
[00:12:52 - 00:13:00] So if we look at that past kind of example, if this is rotating, then the no slip rule is going to kind of be pulling our fluid into this kind of small gap.
[00:13:00 - 00:13:09] Alternatively what we might have is a hydrostatic where the lubrication is actually pumped and forced into our system.
[00:13:09 - 00:13:22] And we'll see that there are options of both hydro dynamic and hydrostatic solutions for both of our lubrication of bearings as well.
[00:13:22 - 00:13:26] So not always just journal bearings.
[00:13:26 - 00:13:37] As we can see here, by having the lubrication, we get a kind of a more or at least friction kind of solution.
[00:13:37 - 00:13:50] So we can see there are some slight differences in how our shaft may run in our bearing or our journal bearing, compared to being either dry or lubricated.
[00:13:50 - 00:13:56] Then again here we see a distribution of what that pressure film may be.
[00:13:56 - 00:13:59] And sometimes you may want to calculate this.
[00:13:59 - 00:14:04] But it's not always something that we'll be doing, but it's sort of useful kind of information I suppose.
[00:14:04 - 00:14:11] One of the things that you will want to do though is make sure that your working pressure is appropriate for what your journal bearing is.
[00:14:11 - 00:14:15] And we can see on the right there how our area is calculated.
[00:14:15 - 00:14:22] And we can use that area and the four set is on our shaft over that area to work out what the pressure is.
[00:14:22 - 00:14:27] And in this case, they have some nice, funny units of pounds per square inch.
[00:14:27 - 00:14:34] But basically we can see that for different types of applications, different allowable pressures exist.
[00:14:34 - 00:14:42] There's probably an SI unit version of this, but have just kind of kept that there for completeness.
[00:14:42 - 00:14:45] Cool. So why do we use lubrication?
[00:14:45 - 00:14:48] There's a kind of bit on journal bearings kind of finished.
[00:14:48 - 00:14:58] And obviously we know that lubrication plays a critical role in ensuring the life efficiency or life effectiveness of any piece of rotating equipment.
[00:14:58 - 00:15:12] If we remember last week when we talked about our bearings, about 50% of them fail due to a lubrication related type of failure.
[00:15:12 - 00:15:17] So if there's too much friction or there's rubbing in our bearing, then that causes premature failure.
[00:15:17 - 00:15:21] That's what our bearings are trying to avoid.
[00:15:21 - 00:15:30] So we see reduced friction reduced, we reduce heat off machine parts to move relative to each other.
[00:15:30 - 00:15:33] So what should a suitable lubricant do?
[00:15:33 - 00:15:42] To start with, it should form this separate separation layer between our rolling elements so that we don't have any kind of metal or metal contact.
[00:15:42 - 00:15:45] We want to protect our bearings against corrosion.
[00:15:45 - 00:15:56] And I don't know if we remember the last week, we saw the photos that had the pattern on the bearing race where we had corrosion, obviously playing a role in that bearing failure.
[00:15:56 - 00:16:01] We also want to remove heat that is generated from the bearing when it's in operation.
[00:16:01 - 00:16:11] And if we're in a situation where we actually regenerating lots and lots of heat, we can even have some sort of heat exchange or unit within our kind of system to make sure that that heat is managed.
[00:16:11 - 00:16:19] And then we also want to make sure that we prevent any dirt or other foreign matter from entering the bearing.
[00:16:19 - 00:16:22] So there we go.
[00:16:22 - 00:16:32] So the lubricants will be specified by the engineer, i.e. you will need to make sure that for your assignment, the bearing lubricant is specified.
[00:16:32 - 00:16:44] And then, General, you would discuss, if you were actually practicing an industry, often you would have a kind of a specific kind of company that you'd be working with.
[00:16:44 - 00:16:49] And it often be a sales representative that you might discuss these kinds of things with.
[00:16:49 - 00:16:51] So they may say, are you getting this bearing here?
[00:16:51 - 00:16:54] We often recommend that this is the type of lubrication.
[00:16:54 - 00:17:01] Or they might be kind of new stuff that's kind of coming out with different editors or different properties or it's more environmentally friendly.
[00:17:01 - 00:17:07] So you may kind of work out what those are through talking with this kind of sales representative.
[00:17:07 - 00:17:18] So for example, this could have bearing company have their own grease and they'll have a recommendation on what they think would be best for their product.
[00:17:18 - 00:17:21] So I think we sort of saw a similar kind of slide.
[00:17:21 - 00:17:26] We might be the same slide as this, I think this one's got a little bit more detail than last week.
[00:17:26 - 00:17:35] But basically we do have oils which are useful for our high speed, low load kind of applications.
[00:17:35 - 00:17:43] Grease is kind of our most kind of common I suppose lubrication that we would use in these kind of applications.
[00:17:43 - 00:17:47] Do you know how to deal with grease before or a flag grease?
[00:17:47 - 00:17:53] Yeah, it's wheat lots people. When I was like 18, my first car was like a 1980 mini.
[00:17:53 - 00:17:59] And the first thing I learned is that there's all these different types of grease points that you have to do to make sure that like your steering doesn't like,
[00:17:59 - 00:18:02] I don't know, stop working because it's not lubricated.
[00:18:02 - 00:18:09] The funny, well funny story, but I had that car, I got a summer job and then driving to my summer job made myself break my car.
[00:18:09 - 00:18:13] Because you needed a little petrol for those kind of old cars.
[00:18:13 - 00:18:15] Yank lubrication right?
[00:18:15 - 00:18:21] And then I didn't know that. So I was just putting regular petrol and I didn't realise the person before me hadn't put the additive in.
[00:18:21 - 00:18:25] So then they were like, what's going home on down? I'm like, ooh, I'm getting a little bit hot here.
[00:18:25 - 00:18:32] Had to get towed by my dad. And then running on three cylinders and they had to replace the head gas because they had a blonde.
[00:18:32 - 00:18:37] So that was like all my summer work, which I said I kind of cracked up job by the Christmas tree farmer.
[00:18:37 - 00:18:48] But I'm really getting aside. But yeah, make sure you've got lubrication in your cars and for your assignment, just like my many, you'll need to make sure that if you use grease, you have a grease nipple.
[00:18:48 - 00:18:51] I guess is the main kind of thing that I was trying to say.
[00:18:51 - 00:18:59] And we also see here that you may have some sort of like solid lubricants, which might be either films or like graphite.
[00:18:59 - 00:19:07] Or you might either have animal fats or different kind of materials that are suitable for high temperatures.
[00:19:07 - 00:19:11] So we've got plastics, middles, mineral films. Cool.
[00:19:11 - 00:19:18] So often these kind of lubrications will have some additives added to them to enable the following kind of things.
[00:19:18 - 00:19:27] So preventing wear, preventing rust, absorbing water so that we don't have water kind of just floating around in our system.
[00:19:27 - 00:19:36] And then we might have de-firming agents or similar to kind of make sure that our lubrication continues to kind of operate as we would expect.
[00:19:36 - 00:19:41] And we don't have heaps of bubbles just coming out of our bearing housing, right?
[00:19:41 - 00:19:46] But the thing is that these additives will deteriorate over time and with heat.
[00:19:46 - 00:19:50] And so this is why you know you have to change your oil in your car, for example.
[00:19:50 - 00:19:56] We've kind of six to twelve months or 10,000 kilometers or whatever your manufacturer kind of recommends.
[00:19:56 - 00:20:09] Right? So otherwise if you don't do that, your lubrication is not going to kind of be working in a way that was as it wasn't intended.
[00:20:09 - 00:20:18] So we'll see that lubrication can be delivered in a number of ways and we will discuss or show a few more exciting examples of that.
[00:20:18 - 00:20:26] We'll see that full grease. Typically you have the following options. You may pick a bearing that is packed for life, which is great.
[00:20:26 - 00:20:36] It means that you don't have to kind of forget to grease your bearing and then you would just replace it after a certain interval with another kind of packed for life bearing.
[00:20:36 - 00:20:45] Those ones are kind of outlawed for the assignment. If you do want to make a little kind of thing because we want to make sure that you guys have to kind of think about how the lubrication would be delivered.
[00:20:45 - 00:20:52] You may have a grease nipple, which does require a maintenance task. All you may have some automatic greasers.
[00:20:52 - 00:21:02] So think of like a can of grease that has like a spring in it. That kind of slowly is going to allow a small amount of grease to constantly kind of be flowing.
[00:21:02 - 00:21:09] Then if you have oil, you may have an oil bath or an oil splash. You may have sort of a drop feeder, which we will see some examples of.
[00:21:09 - 00:21:21] You may have circulation oil where it's kind of pumped and these kind of systems with a pump or so enable it quite easily to be able to take heat away from your lubrication.
[00:21:21 - 00:21:31] Or you may have kind of a jet of oil or a oil mist. We'll be able to often form your magnetic kind of systems. You might have like a oil dropper that makes really fine oil particles.
[00:21:31 - 00:21:41] And then those particles are sent through your system to make sure that when you're using your kind of air tools that the motors in there and the bearings in there are lubricated.
[00:21:41 - 00:21:48] Cool. So we can see here, packed for lift, packed for life grease. We're meant to be introduced in the last lecture. I don't actually think I talked about them.
[00:21:48 - 00:21:56] In detail, we're having too much fun. As we talked about though already sold with everything that you need and avoid that's maintenance task.
[00:21:56 - 00:22:06] However, they have seals that add a little bit more friction and the range of packed for life bearings limited to smaller deep groove ball bearings.
[00:22:06 - 00:22:12] So not every single type of bearing comes in this convenient packed for life type.
[00:22:13 - 00:22:28] Built in terms of grease delivery systems. Here we see an example of our kind of grease nipple where the grease will come down here and then get pushed through our bearing and hopefully not too much through our kind of seals that we kind of see here.
[00:22:28 - 00:22:37] We may have the classic grease own mesh which is that can of grease that kind of constantly allows grease to be going into our system.
[00:22:37 - 00:22:42] And we can see in this case here it looks like they've actually got what is called like a standard kind of pillow block.
[00:22:42 - 00:22:55] So you can get kind of off the shelf kind of bearing housings if you're wanting to kind of whip up a quick prototype or you don't have a kind of specific shaft that you have you might use something like that.
[00:22:55 - 00:23:05] And then in here we have our kind of more modern automatic greaser which looks like it's free fillable of the grease nipple on the side.
[00:23:05 - 00:23:19] Cool. So with grease nipples, grease is injected into the housing and you would normally do this at regular intervals and then to prevent excessive drag and heat bolt up the bearing should not be more than one third to one half filled with grease.
[00:23:19 - 00:23:29] So sometimes that's kind of difficult to exactly know but often as an engineer you kind of would recommend or at least make a note of that in the maintenance things.
[00:23:29 - 00:23:44] Because if it has got too much grease that's actually going to have a need of impact on the life and then again you need to make sure that your automatic grease if selected kind of has this appropriate rate for the selected time.
[00:23:44 - 00:24:10] Next what we can see is our oil baths and oil splash systems. These are suitable when you have low speeds or gears for example that are partially immersed and then you can kind of splash or transfer the oil throughout the system or it might be at high speeds where we really want to have a bit of a party in our housing with oil splashing everywhere so that it gets on every kind of membrane.
[00:24:10 - 00:24:32] So I think we saw an example of this last week that we see here in our bearing housing we could have a kind of oil reservoir and then as the bearing rotates that's going to lubricate our entire bearing and then we see another example of this same idea that in this case with a deep groove ball bearing.
[00:24:33 - 00:24:49] In this case we can see that the seal that we have is a lip seal. Cool. We've got some more complicated types of seals on this one here. Looks like a V kind of hard to see.
[00:24:50 - 00:25:11] Similarly we could have a kind of oil splash system and classic example that is easy to think of example as having a gearbox where you know as big gears engaged and rotate that this transfers our oil across our system and across the different gears.
[00:25:11 - 00:25:41] Cool. We can also have kind of a drop feed system so we showed this last lecture this slide that the main thing that we see here is that we'll have our oil kind of reservoir and this will constantly kind of drip oil into our system and it's most common and older systems mainly because very messy and you end up getting oil basically everywhere because your housing isn't going to be able to kind of
[00:25:41 - 00:25:53] contain all of this oil otherwise it would kind of just be 100% oil in there. Right. So useful for making sure that things are lubricated also useful for making a big mess.
[00:25:53 - 00:26:10] And then as we see we sort of talked about you might have some sort of pump system where instead of having your reservoir and your bath just in the bottom of your housing you may have a larger kind of reservoir or similar and then you may pump your fluid or your lubricant into
[00:26:10 - 00:26:35] the top of your housing and this will now where you to provide some cooling or filtering or both if you see fit. So this is sort of like quite common or a common kind of concept or idea for if you were designing a hydraulic system which obviously is quite different but a similar kind of a pumped system I suppose.
[00:26:39 - 00:27:00] So this in a sense is a system that lubricates your cage and delivers the hydrostatic lubrication on slide 4. Cool. So the next thing we've got here is you may have if you've got really high bearing speeds a jet oil lubrication where we have a high pressure stream of lubrication that is shot into our bearing.
[00:27:01 - 00:27:20] And then as we've seen here you might have oil mists where often the misters created by splashing oil and then using or pushing that kind of lubricated air into the applications where it is needed and as we see it's often used again with very high speeds.
[00:27:20 - 00:27:50] Cool. So in terms of our seals the main seals that we have here there are ten types that we see and I have included the skitchers by Richard Harmon who was a lecturer from 1975 to 1993 basically because I don't want to be the guy that through where these nice drawings and it kind of highlights the idea of being able to have some really useful kind of skitchers.
[00:27:51 - 00:28:11] So the first one that we'll kind of talk about is in our seal catalog obviously all the bearing all the seals are basically in this catalog but before I go into the details of each kind of seal I just wanted to highlight this resource we probably can get it open.
[00:28:12 - 00:28:34] The lot you'll see here is that there's really lots of information there's lots of great bearing and seal propaganda so I was even thinking yes then when I saw this image again I said oh man I need to get this like in my office or something the best friend of bearing ever had and it's a V V ring seal.
[00:28:34 - 00:28:48] Oh it's very old let's see what am I talking about there you know classic and then we also see here that there's lots of useful information such as working out the seal service life based on what the pressure in your system is.
[00:28:48 - 00:29:07] So often this is quite a difficult thing to calculate but the seal life is kind of detailed in the seal kind of catalog and you see that there's also lots of different kind of illustrations and different situations for different types of seals and why they are the way that they are.
[00:29:07 - 00:29:33] So here we see these excellent sketches by Mr Harmon we see that we could have a bland seal or a stuffing box which is pretty much where you just know I'm going to talk about these in a little bit more detail but we'll just go through them basically you'll have rope or similar and just stuff it into your bearing and hope that this doesn't restrict the shaft too much but also doesn't allow too much.
[00:29:34 - 00:29:44] The lubrication to get through your system you may have a kind of cup seal where it kind of looks like a cup and it fits into a kind of cylindrical system.
[00:29:44 - 00:29:57] You may have these kind of lip seals that we were still talking about previously and you'll show that there are a very wide range of lip seals in the direction that you put them all depend on the kind of function that you're wanting to do.
[00:29:57 - 00:30:04] You'll have o-rings, what's your very useful and we provide a design guide about those.
[00:30:04 - 00:30:10] But often the other kind of thing that you will just follow what the manufacturer says and as we'll see,
[00:30:10 - 00:30:18] amount that the o-ring is compressed is something that the engineer will need to kind of design for but we'll talk about some of the benefits of those.
[00:30:18 - 00:30:32] Shortly you may have a mechanical seal where it kind of just has kind of really low smooth parts grabbing against each other with a really tight tolerance and then going to apply.
[00:30:32 - 00:30:47] Force could have a spiral groove and then we also have things like a labyrinth seal to make it really hard for lubrication or to get out or dust in most cases to get in.
[00:30:47 - 00:30:53] You may have your kind of piston rings or other kind of ring seals.
[00:30:53 - 00:31:03] So to go over and elaborate on some of these skitches as we can see here for our packed gland seal or often called a stuffing box.
[00:31:03 - 00:31:08] We'll use some type of soft packing as what they call it.
[00:31:08 - 00:31:15] It might be woven, it might be just a middle foil or it could be loose fibers which we see examples of it here.
[00:31:15 - 00:31:38] And the idea is that you would make a cavity in your housing where you would actually stuff and wrap this rope or woven material into the stuffing box to try and stop things from getting in and out but inadvertently these things are sort of like not the 100% success kind of solution.
[00:31:38 - 00:31:49] So you can imagine that if you were using this to propel a shaft that's underwater, after a certain amount of time it's very likely that the water would get into your system.
[00:31:49 - 00:31:57] Cool, lip seals. These are the ones that you guys will probably have the most experience with when you do your bearing housing assignment.
[00:31:57 - 00:32:10] They used to keep oil or grease, lubricant inside the application and prevent other things like water or dirt to get into your system.
[00:32:10 - 00:32:12] So we call those often contaminants.
[00:32:12 - 00:32:16] So there's sort of two purposes that we would have for those.
[00:32:16 - 00:32:26] For us the CSCR seals handbook is a great resource and here are a couple photos as what we can see about those seals.
[00:32:26 - 00:32:32] So the main idea is that there is a lip on this inner surface.
[00:32:32 - 00:32:42] So in this case here the inner surface would be this one here and that lip comes to a point and kind of seals against our shaft.
[00:32:42 - 00:32:48] So often you'll be a kind of spring and we'll keep that held in place.
[00:32:48 - 00:32:51] So we've got lots of examples of these.
[00:32:51 - 00:33:05] So in this case here what I'll hand around is one of our Teflon coated journal bearings and what we see is that these have been matched with a lip seal.
[00:33:05 - 00:33:09] So I don't know if I can show it very easily.
[00:33:09 - 00:33:13] But it is a lip surface. It's kind of hard.
[00:33:13 - 00:33:16] You can see it. You can see that lip surface is in there.
[00:33:16 - 00:33:19] So that's what would be rubbing against your shaft.
[00:33:19 - 00:33:27] In this case they've got two of those there and then we also just some reason on this chain.
[00:33:27 - 00:33:31] There's also a deep groove ball bearing if you want to look at those.
[00:33:31 - 00:33:34] And so as you pass it around there's actually two of them.
[00:33:34 - 00:33:36] So I can maybe check one round the side.
[00:33:36 - 00:33:38] This one here is obviously in pass around a few times.
[00:33:38 - 00:33:44] So the spring that's inside it has gone missing.
[00:33:44 - 00:33:50] But the main thing that I want you to think about is, or note, is that for these radio lip seals,
[00:33:50 - 00:33:55] because we have this quite a small and important surface,
[00:33:55 - 00:34:02] one of the things that you'll need to specify on your drawing is the surface requirements on your shaft.
[00:34:02 - 00:34:07] So if you have super rough surface on your shaft,
[00:34:07 - 00:34:13] then that's going to increase the wear of your lip seal and basically make it fail early.
[00:34:13 - 00:34:20] Right? And so what we'll see is that, I mean we can use this as an example.
[00:34:20 - 00:34:26] You'll often have a surface requirement specified on your drawing to kind of show.
[00:34:26 - 00:34:31] So the bearing manufacturer will normally say, you know, for this type of lip seal,
[00:34:31 - 00:34:36] this is what we recommend that surface references between.
[00:34:36 - 00:34:41] So you can either machine your shaft surface, or ISTAF,
[00:34:41 - 00:34:46] have a great catalog of products, but they also have a thing that's called a speedy sleeve.
[00:34:46 - 00:34:50] And the idea is that if you don't want to have to machine your surface,
[00:34:50 - 00:34:55] then you could put the sleeve onto your shaft and that has the appropriate kind of surface.
[00:34:55 - 00:35:00] So if you see that mentioned in the catalog, that's what they're talking.
[00:35:00 - 00:35:06] So as we said, there are sort of two ways that you can mount your radial lip seals.
[00:35:06 - 00:35:16] In this case here, this is the outside environment and we have put our radial lip seal in this orientation
[00:35:16 - 00:35:21] so that any contaminants that try to come in can't get in.
[00:35:21 - 00:35:25] Yeah? We're in this case here.
[00:35:25 - 00:35:34] It's being mounted instead to keep our naughty lubricant inside our bearing housing, right?
[00:35:34 - 00:35:39] And so sometimes you might have more than one seal.
[00:35:39 - 00:35:47] If you really have an application where you need, definitely no contaminants in or no contaminants out.
[00:35:47 - 00:35:55] Yeah? So currently today is the day that I decided to go on random tangents,
[00:35:55 - 00:36:07] but what we will see for example in this example here is that we see an example where if you're in something like a nuclear power plant,
[00:36:07 - 00:36:12] you really don't want the lubrications getting out, right?
[00:36:12 - 00:36:22] So here we see a more complicated example where there is lots of different seals being used to basically make sure
[00:36:22 - 00:36:26] that our system does not leak.
[00:36:26 - 00:36:34] We'll talk about another more complicated example towards the end with an example from Hamilton jet.
[00:36:34 - 00:36:42] But it's just to show that there might be combinations sometimes used to do specific kind of features.
[00:36:42 - 00:36:47] So we can see that often while they are that mountain in the housing and they remain stationary.
[00:36:47 - 00:36:52] And with that that means you need to make sure that you can actually get it in and out of the housing, right?
[00:36:52 - 00:37:03] So what we will see is that if you don't have four thoughts and you just try and draw something on CAD that you think might work,
[00:37:03 - 00:37:13] what we'll see if we have for example, so in that case there they had something that looked kind of like this as they're housing, right?
[00:37:13 - 00:37:19] So maybe they had the bearing coming in here.
[00:37:19 - 00:37:23] I don't know, this probably is where our shaft is.
[00:37:23 - 00:37:36] In this case here I've sort of not drawn this particularly well, but what we would want to know is to make sure that if we did have some sort of real long lip seal,
[00:37:36 - 00:37:41] that there is a way that you could get it on and off, right?
[00:37:41 - 00:37:44] So in this case here we might go to take this whole housing part off.
[00:37:44 - 00:37:47] I don't know if this has got split in our housing.
[00:37:47 - 00:37:50] This is our center of our shaft.
[00:37:50 - 00:37:56] Obviously there's nothing kind of restraining our bearing, but you know we're just talking about the seal in this case here.
[00:37:56 - 00:38:17] But what I have seen multiple times is something that looks more like this as the housing and there's no way to get your lip seal in there without then and out without kind of damaging it, right?
[00:38:17 - 00:38:28] So really we don't want to dial on that but there we want to make sure that however you get access to your lip seal that you can do it.
[00:38:28 - 00:38:33] So this case catalog has lots of cross-situing examples that kind of show how you might do it.
[00:38:33 - 00:38:42] So in this case here you can see what you would have to do is take this part of the housing off, take your lock nut off, take your bearing out,
[00:38:42 - 00:38:53] and then you would be able to pull out or push out the amount of your specific tool you use to push this lip seal out and then be able to carefully put in a new kind of one, right?
[00:38:53 - 00:38:58] There's sort of special tools that you'll use because anyone had to replace a radial lip seal before.
[00:38:58 - 00:39:06] Yep, and so you'll know that there are specific tools that you do to make sure that you don't just rip the thing that you're trying to put in before you can do it, right?
[00:39:06 - 00:39:11] So we've talked about that service condition and the importance of maintaining that.
[00:39:11 - 00:39:25] So you'll see in the catalog there are very very wide range of different types of seals and this is where if you're unsure where to start you could review what you're kind of bearing manufacturer.
[00:39:25 - 00:39:28] It recommends for a specific kind of application, right?
[00:39:28 - 00:39:35] So as long as you've got some sort of justification that you can see that's kind of the main thing that we're looking for.
[00:39:35 - 00:39:40] There are different kind of less to me that are used to make up these kind of seals.
[00:39:40 - 00:39:51] There are different kind of operating conditions either surface speed, diameter, that are kind of appropriate for those different ones.
[00:39:51 - 00:40:05] So basically the USK, if kind of catalog and tools will help to recommend this, but this is an older kind of plot that we've been used to kind of make sure that whatever type of material for your looks
[00:40:05 - 00:40:09] that you're using is appropriate for your application.
[00:40:09 - 00:40:16] Cool as we're seeing here, we'll talk about your can have seals used together.
[00:40:16 - 00:40:24] So in this case here we've got a kind of felt dust seal to try and stop dust getting in and then we've got our radial lip seal and again.
[00:40:24 - 00:40:30] This is mounted in a way that it's intended to mostly keep contaminants out, right?
[00:40:30 - 00:40:33] But we can see in this case here to replace both of those things.
[00:40:33 - 00:40:45] If we pulled out the system here, we might be able to then place the felt and then carefully either put our lip seal into those housing and then slowly slide it carefully onto our shaft, right?
[00:40:45 - 00:40:57] So every kind of cross-situ that you see, if you want to play a really fun game with you, if flatmates before dinner, you could talk about how you would assemble and disassemble the kind of bearing housing that you see, right?
[00:40:57 - 00:41:07] And so we see that here, you may have some sort of press fitting tool to kind of make sure that you don't damage the seal before it's even got an opportunity to do its job.
[00:41:07 - 00:41:23] Cool, there are kind of operational limits. Here's one that's been taken from SDKF, but obviously depending on if you have a high-pressure system and different speeds, there are kind of limits and you just have to make sure that you've verified that.
[00:41:23 - 00:41:27] What seal you're selected as appropriate for your operation?
[00:41:27 - 00:41:37] Cool, next we've got some o-ring seals that are very common and they're kind of quite useful and effective when designed and used correctly.
[00:41:37 - 00:41:46] They come in a huge range of sizes. I've got a few right here that just show different thicknesses and diameters.
[00:41:46 - 00:41:55] You can also get lots of really small ones. Sometimes you may have had to replace these if you have been replacing your cartwheel or similar.
[00:41:55 - 00:42:05] Some manufacturers using o-ring around the filter and they're ideal for static or slow-moving applications.
[00:42:05 - 00:42:16] So we can see here just some information that shows how they can be used under pressure and what kind of regulations you might need.
[00:42:16 - 00:42:21] So just some figures basically showing how they might be used.
[00:42:21 - 00:42:31] The main thing that I do want to highlight is that there is this kind of design tool on learn if you do need to design an o-ring and in that design tool,
[00:42:31 - 00:42:39] or the benefit for using kind of o-rings rather than gaskets a lot of the time is that if we have some sort of system.
[00:42:39 - 00:42:46] So if we have some plate like this and we wanted to have, I don't know, some kind of gasket here.
[00:42:46 - 00:42:52] This is our gasket and we have, I don't know, some bolts that are going to hold the things together.
[00:42:52 - 00:42:57] It can be quite hard to make sure that the distribution across the gasket is even.
[00:42:57 - 00:43:04] Unless you're kind of talking each of your bolts particularly carefully in the same.
[00:43:04 - 00:43:08] It can be quite hard to get even surface seal, right?
[00:43:08 - 00:43:14] So I imagine that maybe this is actually just like a pipe or something, right?
[00:43:14 - 00:43:17] We've got a flange there and then a gasket in between it.
[00:43:17 - 00:43:30] So what you'll often see is that instead, if we look at a cross-section, you'll have a kind of cavity for a o-ring to go into.
[00:43:30 - 00:43:34] And this cavity is designed to have the right geometry.
[00:43:34 - 00:43:48] So that wind we have our metal on metal kind of surface and we've contacted it together that we will see our o-ring as compressed to this specifications of our kind of catalog or our manufacturer.
[00:43:48 - 00:43:51] So it's really easy to install this one correctly.
[00:43:51 - 00:43:59] It's really easy to install this one incorrectly if it's important that the seal surfaces evenly come up there.
[00:43:59 - 00:44:04] Got a full supply to cross the whole thing, right?
[00:44:04 - 00:44:05] Sweet.
[00:44:05 - 00:44:07] So next we've got mechanical seals.
[00:44:07 - 00:44:09] We've sort of touched on them and there's little sketches.
[00:44:09 - 00:44:16] But they are a method that are used by engineers to contain rotating shafts that pass through a stationary housing.
[00:44:16 - 00:44:20] And they're often used in high pressure or vacuum applications.
[00:44:20 - 00:44:23] So here we see a cross-section of one.
[00:44:23 - 00:44:28] We have this two parts here, our rubbing surfaces.
[00:44:28 - 00:44:31] So this is actually where the seal is being formed.
[00:44:31 - 00:44:32] Right?
[00:44:32 - 00:44:36] In this case here we've got an o-ring that's stopping anything from getting through that way.
[00:44:36 - 00:44:41] And then this whole part here is rotating with the shaft.
[00:44:41 - 00:44:46] Yes, I feel like if I could color that in yellow, that's obviously everything here is attached to the shaft.
[00:44:46 - 00:44:47] Right?
[00:44:47 - 00:44:49] So we're rotating with the shaft.
[00:44:49 - 00:44:51] This bit here is stationary.
[00:44:51 - 00:44:52] Yeah?
[00:44:52 - 00:44:54] And that's part of our housing.
[00:44:54 - 00:45:01] So what we can see there, probably even though we only have about six minutes, we'll pass this around just so that some people can see it.
[00:45:01 - 00:45:04] But here is our kind of example of that.
[00:45:04 - 00:45:08] So we've got our kind of, in this case, a ceiling surface on the inside.
[00:45:08 - 00:45:11] This bit here is attached in rotating with our shaft.
[00:45:11 - 00:45:15] This bit here is attached to our housing and stationary.
[00:45:15 - 00:45:18] And so it's kind of doing this sort of thing here.
[00:45:18 - 00:45:25] So those two surfaces there are the kind of the ceiling surfaces that you'll use.
[00:45:25 - 00:45:39] So a laborant seal has the name for the suggests.
[00:45:39 - 00:45:45] Make there be a way less direct path for any contaminants to get in or oil to get out.
[00:45:45 - 00:45:47] They have no rubbing surface.
[00:45:47 - 00:45:51] So we'll always have some amount of minor leakage.
[00:45:51 - 00:45:54] And they depend on these kind of small clearances.
[00:45:54 - 00:45:59] But they're particularly good either when you can't have your seal replaced.
[00:45:59 - 00:46:02] All we're gross is used in a horizontal shaft.
[00:46:02 - 00:46:16] So you can see again, they're also used in this application where wooders to be contained under low pressure and some minor leakage is acceptable.
[00:46:16 - 00:46:19] Here we see next we've got our B ring seals.
[00:46:19 - 00:46:25] So these are quite different to lip seals in the fact that they are mounted on the shaft.
[00:46:25 - 00:46:29] Yeah? So our B ring seals are on the shaft.
[00:46:29 - 00:46:36] And then there's going to be some sort of stationary surface that they seal up against where our lip seals are going to be opposite.
[00:46:36 - 00:46:37] Right? They're in our housing.
[00:46:37 - 00:46:41] And there's just this really fine point that's touching our shaft.
[00:46:41 - 00:46:44] And so because of the effect that they're mounted on the shaft,
[00:46:44 - 00:46:49] it'll often be a stationary surface that's perpendicular to our shaft.
[00:46:49 - 00:46:53] Often these are more used for dust seals rather than oil seals.
[00:46:53 - 00:47:03] But use it as per what your manufacturer kind of recommends and is not just one hard and fast rule depending on what the application is.
[00:47:03 - 00:47:06] So I've got one of the B ring seals here.
[00:47:06 - 00:47:10] And basically that figure there shows exactly what we would be seeing.
[00:47:10 - 00:47:13] So in this case here it's kind of hard to see there.
[00:47:13 - 00:47:15] But this thing here would be in our shaft.
[00:47:15 - 00:47:19] And this is our sealing surface on this kind of side here.
[00:47:19 - 00:47:22] So do we want to pass this one around?
[00:47:22 - 00:47:25] I could throw it up to the top or something or we're okay.
[00:47:25 - 00:47:27] If you want to see it, someone wants to see it.
[00:47:27 - 00:47:31] I don't know if I've got enough beans.
[00:47:31 - 00:47:34] But it's so close.
[00:47:34 - 00:47:35] Oh wow.
[00:47:35 - 00:47:37] Someone can have a look at the B ring seal.
[00:47:37 - 00:47:41] It kind of feels like throwing confetti out into a crowd.
[00:47:41 - 00:47:45] But what we can see here is that depending on how fast our shaft is spinning,
[00:47:45 - 00:47:54] the faster it spins, the more kind of axial or restraint it needs to prevent it from kind of wandering.
[00:47:54 - 00:48:00] And making sure that it continues to kind of work effectively as a seal.
[00:48:00 - 00:48:04] So the idea is that it's stopping things getting through and here.
[00:48:04 - 00:48:08] So what's being the outside of our system.
[00:48:08 - 00:48:15] So we can see in there, in this case here we've got kind of back to back the ring seals on our stationary surface.
[00:48:15 - 00:48:20] Hard to see here but there is a gap below our kind of shaft and our thing.
[00:48:20 - 00:48:24] And if you have a similar kind of cross-section in your assignment,
[00:48:24 - 00:48:28] you really want to make sure that that is clear that there's no rubbing parts.
[00:48:28 - 00:48:33] We can see there we've got two lots of back-to-back figuring seals,
[00:48:33 - 00:48:38] which are getting used for sealing oil and preventing dust in this application.
[00:48:38 - 00:48:46] Cool. So then here we see this drawing of our Hamilton jet HJ 362 water jet.
[00:48:46 - 00:48:55] And we can see that there is lots of sealing mechanisms or pieces of equipment used in the system.
[00:48:55 - 00:49:01] So we've got our bearing housing on the outside here with our crosshatching all going that way there.
[00:49:01 - 00:49:04] Within that we have two lip seals.
[00:49:04 - 00:49:12] Yeah, we can see that they look like the maintained or they're trying to maintain oil in our system with the weight that they are orientated.
[00:49:12 - 00:49:15] We also see that there is a mechanical seal.
[00:49:15 - 00:49:21] So we'll see that with the spring in our system.
[00:49:21 - 00:49:24] There'll be a couple faces rubbing against each other.
[00:49:24 - 00:49:34] We also see that there are o-rings to stop water from getting into our boat or into our pieces of rotating equipment.
[00:49:34 - 00:49:37] And then we also see we have our two bearings.
[00:49:37 - 00:49:45] And in this case, because there's the spring here that is going to be applying the minimum load to make sure that our bearings are operating correctly.
[00:49:45 - 00:49:50] And they're not just sliding around and rubbing on each surface, right?
[00:49:50 - 00:49:52] So a nice kind of example there.
[00:49:52 - 00:49:57] So we see that we should have the arrow for the mechanical seal on this side here, right?
[00:49:57 - 00:49:59] So that's the rotating bit to the shaft.
[00:49:59 - 00:50:06] And then we've got that kind of a citizen there, kind of hard to see with the kind of photocopier-esque of it, right?
[00:50:06 - 00:50:13] So there are some additional notes which I've kind of shown you briefly here for fun.
[00:50:13 - 00:50:17] Just sort of has a few little bit more of an information about some of our mechanical seals,
[00:50:17 - 00:50:20] which I have kind of talked about, but might be interesting.
[00:50:20 - 00:50:26] Then obviously the SKF website also has lots of useful kind of information.
[00:50:26 - 00:50:33] So check that out if you're unsure about any of the terminology or wants to know sort of more things, right?
[00:50:33 - 00:50:57] Thanks everyone. We'll see how the tutorial.
[00:50:57 - 00:51:04] So we're going to see if we can kind of play.
[00:51:34 - 00:51:41] So I can answer that. I'll just make sure that I can pack up my coat.
[00:51:41 - 00:51:48] I'll shut it down under there, try to do the nearest loosely, throw it in there. Perfect.
[00:51:48 - 00:51:55] So I'll just take this.

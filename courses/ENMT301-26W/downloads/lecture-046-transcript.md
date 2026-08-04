# ENMT301-26W Lecture 46 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `ce9853f66a0e5d0746467b462fb41d0d32b2cd17323da6c87281e22847a21593`
Generated: 2026-06-06T06:45:01.852455+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:30 - 00:00:32] Alright, thanks a round will make a start there.
[00:00:32 - 00:00:47] You can definitely hear me, because I can hear me.
[00:00:48 - 00:00:53] How's everyone going?
[00:00:53 - 00:00:57] Terrible, I only heard terrible, which is quite terrible, honestly.
[00:00:57 - 00:01:03] But hopefully everyone's feeling a little bit excited, a little bit nervous.
[00:01:04 - 00:01:09] I don't know if you guys have favourite comedians, but the James Acust,
[00:01:09 - 00:01:15] that I cracked me up every time, and he definitely has a thing about.
[00:01:15 - 00:01:19] People telling you, like, I am so excited when you're nervous, but...
[00:01:20 - 00:01:26] You know, it's that whole play on the fact that the experience of being nervous
[00:01:26 - 00:01:29] is essentially the same, and your nervous system is being excited.
[00:01:29 - 00:01:33] So, you know, you might have heard before you can just tell yourself
[00:01:33 - 00:01:35] when you're nervous that you're actually excited.
[00:01:35 - 00:01:37] But anyway, we're rambling.
[00:01:38 - 00:01:43] Week eight, we're on lecture eight, we're getting through the tail ends of things.
[00:01:44 - 00:01:48] And if I had a sample, I definitely would be playing this business time, right?
[00:01:48 - 00:01:52] Because this week, if you guys are definitely business-armed,
[00:01:52 - 00:01:59] to kind of put your calculations to the test in the sense of testing your aluminium structure
[00:01:59 - 00:02:05] and seeing whether it fails the way that the engineering science says it should or whether
[00:02:05 - 00:02:08] you learn something about how you did your calculations.
[00:02:09 - 00:02:13] So, hopefully you've seen the fact that they're just teaching evaluation out.
[00:02:13 - 00:02:15] We talked about that last week.
[00:02:15 - 00:02:19] Obviously, we've got testing starting today, and I'll be sort of running around
[00:02:19 - 00:02:22] like a headless chicken after the selection, making sure that everything is looking
[00:02:22 - 00:02:26] so in span for our 12 o'clock kickoff.
[00:02:26 - 00:02:30] And make sure that if you're not aware of the fact that you've got your testing this week,
[00:02:30 - 00:02:35] that you, in particular, your partner knows that you've got your test times
[00:02:35 - 00:02:38] and they're on learn on the PDF.
[00:02:38 - 00:02:41] It runs Manage to Find That PDF, I hope.
[00:02:41 - 00:02:43] Cool. I know. I just say that.
[00:02:43 - 00:02:48] It's like, I really crack up like before I left on Friday.
[00:02:48 - 00:02:53] I was like, oh, should I leave some aluminium out in case someone still hasn't picked up the aluminium?
[00:02:53 - 00:02:56] And there was people that still had them picked up the aluminium which I was like,
[00:02:56 - 00:02:59] this is a bold move. I don't know.
[00:02:59 - 00:03:02] So, we've got to respect the lateness of it.
[00:03:02 - 00:03:03] I was like, yes, I've hidden them here.
[00:03:03 - 00:03:06] Is there like a picture of it?
[00:03:06 - 00:03:09] I guess if you make sure that you're doing part of those, I guess,
[00:03:09 - 00:03:12] because I wouldn't be surprised.
[00:03:12 - 00:03:15] Cool. And then I guess one thing that I just want to make really clear here is
[00:03:15 - 00:03:18] some people have emailed me about making changes and obviously there's penalties
[00:03:18 - 00:03:22] that's so set of any design changes.
[00:03:22 - 00:03:27] But if you made that change under the assumption that you couldn't do something,
[00:03:27 - 00:03:31] so for example, it was meant to be glued, but then there was no glue
[00:03:31 - 00:03:35] and then you couldn't work out over the weekend how to make it for your thing on Tuesday.
[00:03:35 - 00:03:40] If you re-test your structure as originally intended and you do not make any design
[00:03:40 - 00:03:43] change, then there's no penalty associated with it, right?
[00:03:43 - 00:03:46] But on the test out, it's probably going to be a little bit like,
[00:03:46 - 00:03:48] this is a difference to your drawings.
[00:03:48 - 00:03:51] So there is the penalty associated to it, right?
[00:03:51 - 00:03:53] And we've talked about, we've talked about that, yeah.
[00:03:53 - 00:03:55] But we're sort of like the clock is ticking.
[00:03:55 - 00:03:58] So, at 12 o'clock, if you start email me about the design change,
[00:03:58 - 00:04:01] then the penalty is what the penalty is on the assignment briefer.
[00:04:01 - 00:04:04] So, if you've got any last minute things that you're like,
[00:04:04 - 00:04:06] oh, that's right, we can completely change that member,
[00:04:06 - 00:04:08] probably in an email.
[00:04:08 - 00:04:10] Yeah.
[00:04:10 - 00:04:11] Cool.
[00:04:11 - 00:04:14] So we see here that we re-testing happening over the next two weeks.
[00:04:14 - 00:04:17] I've got a sheet, I can't remember off the top of my head,
[00:04:17 - 00:04:22] but I believe it is on Monday mornings either slightly before or slightly after.
[00:04:22 - 00:04:26] I think it's slightly after the drop-in session time.
[00:04:26 - 00:04:29] So, the re-testing happened there.
[00:04:29 - 00:04:31] So, those things don't go to plan.
[00:04:31 - 00:04:35] And then obviously, team at ratings, this is my reminder about that.
[00:04:35 - 00:04:38] So, I believe that's opening today or opened today.
[00:04:38 - 00:04:41] And it closes sometime in May.
[00:04:41 - 00:04:44] They make sure you check that out and do it.
[00:04:44 - 00:04:47] So, there we don't have issues with that.
[00:04:47 - 00:04:48] Oh, cool, yes.
[00:04:48 - 00:04:49] Some more exciting news.
[00:04:49 - 00:04:51] We had another paper published.
[00:04:51 - 00:04:53] This one, I was looking at some emails about.
[00:04:53 - 00:04:57] It's been a very long and unrestrode.
[00:04:57 - 00:05:00] The thing has been like two years just trying to get published, but.
[00:05:00 - 00:05:07] I'm not a security check, but if you want to help me improve my statistics on the algorithm,
[00:05:07 - 00:05:11] you can do me a solid by clicking the link or scanning the QR code.
[00:05:11 - 00:05:13] I'll take you to this page here.
[00:05:13 - 00:05:17] And then if you click this link here, which I was really failing to describe last time
[00:05:17 - 00:05:21] and show that you're not a robot, then you can actually see the paper,
[00:05:21 - 00:05:22] which is open source.
[00:05:22 - 00:05:27] So, this is actually to do with some clenched joining strength prediction,
[00:05:27 - 00:05:33] which we could actually incorporate into our minimiss diamond if we did have the dies needed.
[00:05:33 - 00:05:39] Essentially, instead of using a rivet, which you guys might have had some tedious undertakings with,
[00:05:39 - 00:05:45] a clenched join is just mechanically fastened, joined through deformation.
[00:05:45 - 00:05:49] So, basically, you make a little puck and a punch,
[00:05:49 - 00:05:53] and it pushes a certain shape, which kind of the cross-section looks like this.
[00:05:53 - 00:05:55] So, you end up getting like a button.
[00:05:55 - 00:05:58] If you look at this here, you end up getting a button in the middle,
[00:05:58 - 00:06:01] if there's actually not the clenched joint.
[00:06:01 - 00:06:02] There we see.
[00:06:02 - 00:06:03] That's what it kind of looks like.
[00:06:03 - 00:06:10] So, that's the way of joining sheet middle properties in this paper looked at how to improve making estimates of that
[00:06:10 - 00:06:15] strength of that joint, which is probably useful if you want to know how strong you join to as a fewer designer.
[00:06:15 - 00:06:16] Cool.
[00:06:16 - 00:06:23] So, for final things for what happens today, we talked about this last time, but actually, you've got your structure with you,
[00:06:23 - 00:06:27] and you know that it goes together, and make sure that you know your three modes of failure.
[00:06:27 - 00:06:32] So, those can change compared to what you've got on the sheet, the modes can,
[00:06:32 - 00:06:35] but the failure load and no provisions for changing.
[00:06:35 - 00:06:41] So, what I've said in the past, maybe if you're a gluis of it wet or now on reflection,
[00:06:41 - 00:06:45] this hole here that's close to the edge of my teach member,
[00:06:45 - 00:06:49] I'm worried that that's going to do this, then you could make that your second mode of failure as what we're saying.
[00:06:49 - 00:06:53] So, your tester, and then we'll basically go from there.
[00:06:53 - 00:06:57] So, we've got 5 kg and 2 kg rates, and the chain and the hang is added on.
[00:06:57 - 00:07:00] So, this is a game because I know that there's still, if you were today, that'll like,
[00:07:00 - 00:07:03] what, I didn't know that the chain and hang out was included.
[00:07:03 - 00:07:07] It's just to make sure that if you get to 3D8 kg, if you're going to write down anything right down,
[00:07:07 - 00:07:11] when we're at 3D8 kg, that is over 39 kg.
[00:07:11 - 00:07:14] Yeah? So, that's outside that upper bound.
[00:07:14 - 00:07:17] So, proceed with core sheet marks.
[00:07:17 - 00:07:21] You sort of want to, the next you want to get up to is 30 C for nice bows,
[00:07:21 - 00:07:24] and then you want it to break straight away if it hasn't already broken.
[00:07:24 - 00:07:30] Cool. So, if it doesn't go to plan, then we talked about our stages of grief.
[00:07:30 - 00:07:36] So, just remember that that might happen, we'll get through it and eventually work out a resolution
[00:07:36 - 00:07:39] in a way that you can read here to face the way that you want to proceed.
[00:07:39 - 00:07:43] Or you might just accept that things aren't going to be perfect with that assignment
[00:07:43 - 00:07:46] and move on to the next thing that you have.
[00:07:46 - 00:07:53] So, here are some tips I suppose for handling that failure, but the main thing is just to avoid making any comments
[00:07:53 - 00:08:01] and decisions if possible until you truly understand what has caused, what has happened to happen essentially.
[00:08:01 - 00:08:05] Cool. So, some key slides from the last lecture.
[00:08:05 - 00:08:17] Now analysis of clutches, and we see here that the analysis of clutches' trick is obtained between our actuating force,
[00:08:17 - 00:08:20] if and the certain talk will be coefficient of if.
[00:08:20 - 00:08:27] So, this will produce a pressure and that there are two methods to calculate that amount of talk
[00:08:27 - 00:08:32] that a clutch will be able to transmit depending on the kind of assumptions you have around that clutch.
[00:08:32 - 00:08:38] So, you might have uniform wear, which is basically when you are a Sherman that is a very rigid plate,
[00:08:38 - 00:08:46] which will eventually after its first kind of been worn in, have a uniform wear occurring on that plate.
[00:08:46 - 00:08:53] So, essentially the assumption is that the rate of wear is proportional to the pressure times the radius,
[00:08:53 - 00:08:57] which is what they use to derive the equation.
[00:08:57 - 00:09:01] The alternative one that you can use is if you have an assumption of uniform pressure,
[00:09:01 - 00:09:06] which often is more applicable for flexible plates,
[00:09:06 - 00:09:09] where there is uniform pressure over that plate.
[00:09:09 - 00:09:14] So, this has got the underlying assumption that pressure is constant, which is often the case for a new clutch.
[00:09:14 - 00:09:22] Now, as we saw, depending on what your ratio of diameter over diameter is,
[00:09:22 - 00:09:25] it may make a bigger or smaller difference.
[00:09:25 - 00:09:29] The difference in the talk that these two calculations would give you, right?
[00:09:29 - 00:09:32] So, we are happy for you just to say which one you are assuming,
[00:09:32 - 00:09:39] or if you want to compare it to you can, essentially what we are saying is we don't want you just to recreate a plot that we have seen.
[00:09:39 - 00:09:48] So, here we see those two equations, and we talked about what is required for the assignment using these.
[00:09:48 - 00:09:50] Any questions on that?
[00:09:50 - 00:10:00] So, because we don't have a drop in session yesterday, if you want to answer this question on these objects,
[00:10:00 - 00:10:05] they'll be good, and then we'll be getting into our bouts and chains content.
[00:10:05 - 00:10:12] Here's the main thing here, it's like, if you don't want a drop in session, and let me know.
[00:10:12 - 00:10:14] Because we don't have to do one.
[00:10:14 - 00:10:20] But if you do, then there are some times there on Friday, which I'm available, and hopefully you guys are also available,
[00:10:20 - 00:10:38] but I guess we'll find out through the pole.
[00:10:38 - 00:10:42] So, it looks like my system, because I can't help but have a look.
[00:10:42 - 00:10:47] So, 44 seen.
[00:10:47 - 00:10:51] I mean, that's still not a bad number, but it looks like 230 will be the time.
[00:10:51 - 00:11:00] Guess I'll make a post on Thursday or Friday, and it will probably say good job for all of the structure testing.
[00:11:00 - 00:11:04] Here's some information about retesting, here's some information about the drop in the session.
[00:11:04 - 00:11:06] But at this stage, it will be 230.
[00:11:06 - 00:11:10] And if you don't want to come, then that is all good.
[00:11:10 - 00:11:17] So, obviously, if you're watching this in the future, and it's before Friday, feel free to still complete the pole.
[00:11:17 - 00:11:19] I'll leave it open.
[00:11:19 - 00:11:20] Yeah.
[00:11:20 - 00:11:21] Awesome.
[00:11:21 - 00:11:27] So, today what we're going to be talking about is our fund, the minimum concepts for power transmission through bouts and chains.
[00:11:27 - 00:11:34] We'll look at a few different types of bouts, from flat bouts, view bouts, and then some variable speed bouts,
[00:11:34 - 00:11:39] and then have a discussion I suppose on timing bouts and timing chains.
[00:11:39 - 00:11:47] And as usual, the machine design books are very good at these explaining these topics and concepts.
[00:11:47 - 00:11:57] And then also we have some information from some of the manufacturers of these different pieces of equipment.
[00:11:57 - 00:12:01] So, different bouts and chains manufacturers also have a lot of useful resources.
[00:12:01 - 00:12:14] And I guess that's just an underlying theme of like, if you're unsure when you're in your engineer, where to go, then the local manufacturer that you're dealing with will often have the resources you need to select the products appropriately.
[00:12:14 - 00:12:15] Cool.
[00:12:15 - 00:12:19] So, we see here the basic relationship between bouts and chains.
[00:12:19 - 00:12:27] And then we get this ratio between either our number of teeth or our diameter, depending on if it's tooth or a bout.
[00:12:27 - 00:12:35] And our speed, well, this is just telling us between our speeds and our radiuses.
[00:12:35 - 00:12:40] And then we can work it out about tension, is at least t1 over R1.
[00:12:40 - 00:12:44] And I think we will have done something similar for your assignment.
[00:12:44 - 00:12:50] When you're working out orders, our chain tension is going to be on this spot here.
[00:12:50 - 00:12:52] So, we've been told that we've got an engine.
[00:12:52 - 00:12:55] That engine has a certain amount of power.
[00:12:55 - 00:13:07] And if we're assuming that all of that next engine, well, if the maximum engine power is being transmitted into this chain, then that is basically what we're wanting to size our shaft to be.
[00:13:07 - 00:13:12] And we did put up a chain tensioning example earlier.
[00:13:12 - 00:13:19] So, if you're really unsure about how to kind of approach that, then this example here might be useful.
[00:13:19 - 00:13:26] But essentially what we can see is that we can determine our torque by working out our power over our angular velocity.
[00:13:26 - 00:13:34] And that's going to give us a number of newton litres, which, as far as it's worth noting, that that's going to be useful when it comes to working out your secondary moments.
[00:13:34 - 00:13:40] Right? Because torque shaft torque is one of the inputs that you'll need to work out what that is.
[00:13:40 - 00:13:41] Right?
[00:13:41 - 00:13:48] And then from here, we're actually trying to just work out what is the chain tension that we can again use that relationship that we saw there with our.
[00:13:48 - 00:13:51] force radius and torque.
[00:13:51 - 00:13:54] So, we have some sort of chain tension there.
[00:13:54 - 00:14:05] So, other thing that we sort of talked about I suppose was just to make sure that if we're assuming next power on our chain, we probably also want to check that that is going to be enough power.
[00:14:05 - 00:14:10] Well, that's going to be enough force to pull our carriage up the lift hill.
[00:14:10 - 00:14:17] So, that's the secondary check that you would just do based on the masses and the angle you'd have to in a human engine.
[00:14:17 - 00:14:24] So, we have to have a human angle as opposed to this lift hill to do that.
[00:14:24 - 00:14:27] Cool. So, one of the main functions of a belt or a chain.
[00:14:27 - 00:14:30] Well, obviously we want it to be able to transmit power.
[00:14:30 - 00:14:40] We may use it to change the shaft speed, so either if it's going too fast or too slow, you want to be flexible and have a low tolerance.
[00:14:40 - 00:14:43] Well, it's a low tolerance kind of shaft coupling.
[00:14:43 - 00:14:47] So, you should have to go to work fairly easily.
[00:14:47 - 00:14:59] And if we think about this easy examples of these functions for chain speed, then if you do go ahead to change the belt on the drill press, that everyone had to do that, making the element structure.
[00:14:59 - 00:15:09] And we'll see that down there just has basically different pulleys that you can put the belt on and that will change the speed to make sure that you got your drill operating at the recommended.
[00:15:09 - 00:15:22] And then, belts don't need all components to be perfectly aligned, which is a real benefit, especially if you don't have much control over those kind of tolerances.
[00:15:22 - 00:15:29] So, remember when we're talking about couplings and how couplings are useful to allow for a smaller amount of misalignment.
[00:15:29 - 00:15:43] We did see that for some of our rigid couplings, they were often driven by belts, which is kind of showing you that that's a place where they are allowing some tolerance or flexibility in their system.
[00:15:43 - 00:15:53] So, in those kind of cases, instead of having something like your coupling braking, your belt would just be able to slip.
[00:15:53 - 00:16:02] So, we see here, we can drive shafts that are in parallel, we can drive civil shafts from one single source, we can transmit power over quantized distances.
[00:16:02 - 00:16:13] They're often cheaper than shafting or gears, but relatively light and elastic, so it can absorb some amount of shock.
[00:16:13 - 00:16:17] It also can develop resonance, which is something we have to be aware of.
[00:16:17 - 00:16:22] If we have multiple belts that are running on the same pulley.
[00:16:22 - 00:16:36] So, a thought experiment for you. To transmit a given power, the belt or chain strand can be lighter if the strand moves at a higher speed, or the sheaves or pulleys are larger and diameter.
[00:16:36 - 00:16:49] So, I guess what this is trying to say here, or the thought experiment that I was meant to have the membit prompts you guys was, wouldn't it be possible, I suppose, to kind of pull something like a car with your pinky finger if you really wanted to.
[00:16:49 - 00:17:06] The answer is yes, as long as you're able to manipulate how fast you pulling that strand, obviously you need to pull it like pretty quickly, because you're going to want to have some really large pulleys or small pulleys larger and diameter.
[00:17:06 - 00:17:21] So, basically we can manipulate this relationship between our higher speed and larger diameter to pull really large amounts of power with really small forces if that is the constraint that we have.
[00:17:21 - 00:17:28] So, this is kind of why you might incorporate these into some of your systems to make use of this manipulation.
[00:17:28 - 00:17:34] So, this means there's possible to transmit larger amounts of power if you have a large pulley and high speeds.
[00:17:34 - 00:17:38] Yeah, which makes sense, right? Obviously, let's go really, really fast for your own pulley.
[00:17:38 - 00:17:45] You're famous, so there's some other kind of logistical considerations there that we may not have thought about.
[00:17:45 - 00:17:51] In terms of abouts, there are a number of bouts. We've got flat bouts, bouts that are shaped like a V.
[00:17:51 - 00:17:56] Also, have lengthy bouts, poly V bouts, micro V bouts, and timing bouts.
[00:17:56 - 00:18:02] These are the ones that will at least be mentioning or giving you some insights into in this lecture today.
[00:18:02 - 00:18:10] So, in terms of flat outs, they're generally strong horse around the by and the less than a row, or in the past we've made of liver.
[00:18:10 - 00:18:16] They do have high efficiency and they need some initial tension to achieve grip.
[00:18:16 - 00:18:24] There also be some slip, which can be useful in some cases if you want to have some clutching action.
[00:18:24 - 00:18:30] But it does mean that if you want to use it for a precision environment, i.e., you want to re-rotate.
[00:18:30 - 00:18:39] If we turn the bow for pulled about this distance that we want to exactly have this amount of angular displacement, then it's probably not the bout of choice to use.
[00:18:39 - 00:18:50] So, they may be used to give right-angled drives with extra idlers, so we can use them in a number of kind of, I suppose, designs situations.
[00:18:50 - 00:19:02] And they can be reversed if we cross over our direction and again useful, as they can be made to link, which is good for kind of custom sorts of situations.
[00:19:02 - 00:19:12] Now, often our police will have crowning on them, which is basically probably easier if I just draw a little bit to show that.
[00:19:12 - 00:19:22] I do have a little demonstration of how these kind of flat out police work and look.
[00:19:22 - 00:19:30] But essentially, if we have, I know, these are our police and we've got our bout to go in on them.
[00:19:30 - 00:19:43] So, what we can have, if we're looking front on, is that the pulley can either be crowned like this, or it's convicts, or it can be cotton-cave.
[00:19:43 - 00:19:51] Essentially, if we crown crowning it in the middle, then we're getting our tinsion, I think you see that.
[00:19:51 - 00:19:56] So, the cross-sictions look like that. They won't just look flat in the corners.
[00:19:56 - 00:20:05] The idea is that that will provide some tension on the bout, which keeps it kind of centered and from slipping off to one side.
[00:20:05 - 00:20:15] So, here we see an example that we've seen in the past, reflect out as being used in the mountains and observatory and ala.
[00:20:15 - 00:20:18] So, here we see that flat bout here.
[00:20:18 - 00:20:30] In this case, here we can see that they are not crossed over, but we will see some examples of that if we really want to change what the direction of our pulley.
[00:20:30 - 00:20:40] So, here we see a bunch of kind of equations that may be useful if you are trying to make some designs using flat belts.
[00:20:40 - 00:20:50] You can see here that there are some considerations that need to be made in terms of the angle of wrap and the coefficient of friction.
[00:20:50 - 00:20:59] So, if you don't have enough wrap angle, then basically you're just going to have your bout slipping rather than driving what it is system that you have.
[00:20:59 - 00:21:05] So, here we see again some of our equations for working out our bout length.
[00:21:05 - 00:21:08] And then also some examples for our open bout.
[00:21:08 - 00:21:12] This is our cross bout if we want to change the direction.
[00:21:12 - 00:21:18] So, as bouts can come to standard sizes, distances between shafts may need to be calculated.
[00:21:18 - 00:21:25] Just to make sure that you're about that you're forced kind of fits what you want to design for.
[00:21:25 - 00:21:28] And it does not should allow for adjustment for tensioning.
[00:21:28 - 00:21:40] So, basically the way to do that is to make sure that one of your pulleys or both of your pulleys are able to actually move horizontally to be displaced.
[00:21:40 - 00:21:55] So, you often see standard kind of parts, what you call bout tensioners, which essentially have a little mechanism of pulling the shaft that this pulley is on forward and backwards so that you can
[00:21:55 - 00:22:00] achieve the required kind of pretension that your bout requires.
[00:22:00 - 00:22:12] So, the next kind of bout they will talk about is V bouts, which again they have a strong cord which is intention and then the section is surrounded by nalestema.
[00:22:12 - 00:22:19] They are lower efficiency than flat bouts and they do need some initial tension to achieve grip.
[00:22:19 - 00:22:26] It's smaller than what would be required for about a flat bout of kind of similar sizing.
[00:22:26 - 00:22:34] And this is because of the fact that the geometry enables some wedging to occur between your bout and your pulley.
[00:22:34 - 00:22:42] So, we also have the potential for a lot larger kind of surface area on these areas, depending on the geometry of our bout.
[00:22:42 - 00:22:52] Compared to a flat bout of the same kind of width, we would see that these two sides here are a lot bigger than just a distance straight across.
[00:22:52 - 00:23:10] Cool, so we can see again they come in a bunch of standard sizes and they come in a bunch of standard sections and therefore there are kind of preferred sizes that you will then choose and then need to design around.
[00:23:10 - 00:23:23] There will be some stretch and there will be some slip and so again you will need to have some adjustment in your design to allow for this.
[00:23:23 - 00:23:33] So, typically V bouts will run between five and twenty five, maybe a second and this is what determines the power that is transmitted.
[00:23:33 - 00:23:46] And you may have multiple or single bouts on a single sheave, so we can see here is an example that has three V bouts so that more power can be transmitted.
[00:23:46 - 00:24:03] The whole but I guess the catch is that you don't want to have this kind of sit up in situations where those bouts are really long and extended because this may cause or the vibration that occurs when you have these
[00:24:03 - 00:24:13] kind of distances will shorten the life and so the general design guide is that you have a centre to centre distance of less than three times the largest pulley dimers are.
[00:24:13 - 00:24:30] Cool, so in terms of the different types of V bouts, we will look at a few of them now but we see power band bouts where we have a situation like this where we have multiple bouts but they are actually joined all together.
[00:24:30 - 00:24:43] You may have a moulded notch bout for smaller sheaves and then we also have both linked V bouts and micro V bouts which will show you some photos of in the upcoming slides.
[00:24:43 - 00:24:57] So again as we see here the power band out avoids the problems of vibrations and natural frequencies by connecting the outside of each of the single V bouts.
[00:24:57 - 00:25:13] Here we see an example from the Gates catalog which shows five separate bouts and you can see that vibrating from lift to right quite a lot so we can see it's kind of hard to see that.
[00:25:13 - 00:25:29] As wobbling with throughout which is not going to be good for the life of the bouts and we see the power band V bout in the same situation which is acting a lot more rigidly.
[00:25:29 - 00:25:44] Cool, in terms of our moulded or notched bouts, I guess the real question here is well, I guess in your mind you can think why do you think you might have notches and you're about to get rid of the same size.
[00:25:44 - 00:26:02] So the answer in this case is that they are not, if you said I've got obviously teeth so that they can run on some sort of gear.
[00:26:02 - 00:26:25] The wrong answer unfortunately, the reason that we've got our notches in the bout is to make them more flexible in terms reduce the compressive stress that's happening in the size of the side here and that's useful because it means that you're able to get these bouts around smaller sheaves if you do require that basically.
[00:26:25 - 00:26:32] So you can see here a more flexible and they can run on smaller sheaves and save on weight.
[00:26:32 - 00:26:46] So before I forget we can show some of these examples of that so here I also don't do any to be.
[00:26:46 - 00:27:05] So here we see a V bout from Trojan, not really sure exactly what I can show you, but we do have our sheaves which has also got a V and then our bout sits in that sheaves as we saw in the different photos.
[00:27:05 - 00:27:13] And then the example that we've just kind of talked about is a notched V bout which will be a lot more flexible.
[00:27:13 - 00:27:28] So in a really unscientific way we can see that this V bout here I can push and squeeze around this much if I try to do the same thing for this bout I have to push a lot harder to get that around the sheave.
[00:27:28 - 00:27:40] So you can do that experiment yourself, our pasties around so that they have the yearly outing before being put back into the storage area.
[00:27:40 - 00:27:49] Cool. And then obviously here we see I won't pass it around but here is a multiple sheave, multiple bout sheave.
[00:27:49 - 00:27:55] We've got two provisions for two bouts on the same sheave.
[00:27:55 - 00:28:15] That'll be the one we want. Cool. So we can also have these link bouts which I suppose in one sense.
[00:28:15 - 00:28:22] A very useful book that means that if you want to change the length of your bout all of the sun this gives you the provision to do that.
[00:28:22 - 00:28:28] So instead of it having to be a standard size and it can actually manipulate what you've got.
[00:28:28 - 00:28:42] So the suitable alternatives to standard bouts on all industrial applications and they often are used in a kind of emergency or quick about replacement kind of situation.
[00:28:42 - 00:28:49] All they're used when it's really difficult to get into the tight space to actually get a full size kind of belt on.
[00:28:49 - 00:28:58] So we see some examples of this here operating on a machine running between two different sized sheaves.
[00:28:58 - 00:29:04] We see that there's a special tool that you're used to kind of link them together and again similar to our multiple bebouts.
[00:29:04 - 00:29:10] You can have multiple link bouts on the same sheave as well.
[00:29:10 - 00:29:21] Cool. Next we've got our poly V or micro V bouts which are essentially are a cross between V bouts and flat bouts.
[00:29:21 - 00:29:30] So they have high efficiency like flat bouts because they have a thin section and they cannot be used around relatively small sheaves.
[00:29:30 - 00:29:35] And they are lighter than V bouts but maybe used over several sheaves.
[00:29:35 - 00:29:41] So you can use both sides of the bout to actually run a machine round.
[00:29:41 - 00:29:48] So we see again here a bunch of different sections with types of sections with width and thicknesses.
[00:29:48 - 00:29:56] And that manufacturer will kind of outline what the differences are of these in their catalogs.
[00:29:56 - 00:30:04] So here we see on the left here a very kind of small sheave that the micro V bout is on.
[00:30:04 - 00:30:14] Then on the right here we see a particularly worn V bout micro V bout on an engine.
[00:30:14 - 00:30:21] So you can see here that there's some cracks kind of occurring but I'll see them as he probably want to have this replaced.
[00:30:21 - 00:30:29] This might be kind of looks like you might be running your alternator or your water pump or those sort of things in your car.
[00:30:29 - 00:30:33] I'm sure that there are some people that have had to replace these kind of bouts.
[00:30:33 - 00:30:36] And the past now particularly.
[00:30:36 - 00:30:48] I guess the main thing that we're trying to show here as well is that you can run both on the inside and the outside of the bout.
[00:30:48 - 00:30:57] So again for completeness and for the people watching online here we see our example of our micro V bout.
[00:30:57 - 00:31:04] And then again a poly V bout same sort of thing just different terminology.
[00:31:04 - 00:31:06] And then again a small size one there.
[00:31:06 - 00:31:16] So pass that around as well and you can kind of see how much more flexible that is compared to your standard V bout that you just had passed around.
[00:31:16 - 00:31:24] So in terms of teaching about this is one way that you can do it based on the deflection.
[00:31:24 - 00:31:35] So if you have the span length between the center of your two pulleys, you can then work out by measuring the amount of force that it takes to deflected a certain amount.
[00:31:35 - 00:31:38] What the tension is on your belt.
[00:31:38 - 00:31:49] So again this will be information that is provided by suppliers to make sure that you do have the right kind of recommended deflections.
[00:31:49 - 00:31:56] So that your belt is not slipping too much and then failing early or wearing faster than it should.
[00:31:56 - 00:32:03] Or that it's not overly kind of our teaching which is also bad for the life of the bout.
[00:32:03 - 00:32:12] Cool. So you can also use V bout's for variable speed drive.
[00:32:12 - 00:32:21] There's a commonly referred to as CVT or continuous variable transmission which are used on vehicles such as no mobules.
[00:32:21 - 00:32:24] This is not actually driven as no bill before.
[00:32:24 - 00:32:26] A few people.
[00:32:26 - 00:32:34] I wish one day maybe I will be able to but it seems like a good kind of field test to do to look at these kind of continuous variable transmissions.
[00:32:34 - 00:32:54] But what we see is that allows us to move in seamless variation of the gear ratio basically by combining the action of two pulleys where the diameters of these pulleys are different or have a, I suppose, a change.
[00:32:54 - 00:32:59] Well if they change as you operate through different velocities.
[00:32:59 - 00:33:09] So basically this is useful because it means that our engine can be at an optimal speed for optimal performance and efficiency.
[00:33:09 - 00:33:12] And then there's also no kind of manual shifting of gears.
[00:33:12 - 00:33:20] So this is essentially replacing what you would have if you did have a gearbox.
[00:33:20 - 00:33:35] So what we can see here is that as a vehicle will accelerate that the engine speed increases which will also cause the driver pulley to move outwards and the driven pulley to move endwards.
[00:33:35 - 00:33:41] So this adjustment and pulley diameters allows for the bout to ride at these varying positions.
[00:33:41 - 00:33:46] We have the diameters and bus the gear ratios have been changed.
[00:33:46 - 00:33:55] So we can see here in low speed we have this kind of situation here and then at a higher speed we have this situation here.
[00:33:55 - 00:33:59] So look at this.
[00:33:59 - 00:34:06] This will be our driving pulley in our driving pulley.
[00:34:06 - 00:34:14] So basically it means we able to go faster by having our smaller diameter as we speed it up.
[00:34:14 - 00:34:25] So there are some funny videos that in the past I have kind of shown where people have used these snowmobiles on water.
[00:34:25 - 00:34:29] I think there's a particular place in Texas that's like real keen.
[00:34:29 - 00:34:37] They're like a festival of driving snowmobiles on water, but they can go at quite high speeds.
[00:34:37 - 00:34:44] As well as just a practically shows how our CVT kind of operates.
[00:34:44 - 00:34:54] So you won't see them changing gears or anything but in here we see an example of that CVT on a snowmobile.
[00:34:54 - 00:35:04] So I'll leave that here I suppose for further reading if you do want to look at some of those in action.
[00:35:04 - 00:35:13] Cool so next we are talking about timing outs which as the name sort of suggests they are often used for timing and our engines.
[00:35:13 - 00:35:19] And in this case there is, well we want there to be no slip.
[00:35:19 - 00:35:27] If you've had your timing about slip then it sounds like a costly kind of occurrence because if you're well.
[00:35:27 - 00:35:40] This is where all engineers here we kind of know but we kind of want our valves and our piston to be operating in synchrony and not kind of clashing each other which is basically what would happen if you did have slip on your timing.
[00:35:40 - 00:35:50] So we can see again is a range of standard sizes and our sheaves have to be made accurately to match our belt.
[00:35:50 - 00:35:54] So we're just useful to make sure that we avoid wear.
[00:35:54 - 00:36:00] They can be used at high speeds, they're light, they're quiet, they're quiet, they're in the chain.
[00:36:00 - 00:36:09] They'll need some amount of adjustment and basically because basically the width of our bowels what would determine the amount of power that can be transmitted.
[00:36:09 - 00:36:19] because each of the forces is going to be on each of the teeth so if we have a bigger area then we can have more force for the same amount of stress.
[00:36:19 - 00:36:23] So there's pretty much two types.
[00:36:23 - 00:36:32] We may have flat teeth which are mainly used for round sorry flat teeth which are mainly used for timing or we can have rounded teeth which are for power.
[00:36:32 - 00:36:48] And so I've talked about those things there but again you have to make sure you choose choose a standard kind of belt from a manufacturer not go to them and say this is the kind of belt and length that I want.
[00:36:48 - 00:36:55] So we see here for some synchronous running we do have some standard patches that are available.
[00:36:55 - 00:37:01] For example showing some of the key terminology for these kind of systems.
[00:37:01 - 00:37:06] Then again for power we see that we have a more rounded profile.
[00:37:06 - 00:37:11] What we do actually have to example of this here as well.
[00:37:11 - 00:37:20] So we'll have a quick look before passing these around on document camera just for the people in light.
[00:37:20 - 00:37:28] So the first one here that we can see the teeth are relatively square.
[00:37:28 - 00:37:36] But nice and flexible a lot more flexible than our V-bout and then again this one here for power we can see we have a lot more rounded teeth.
[00:37:36 - 00:37:47] It looks like we've got some bonus very small toothbouts just highlighting the fact that you can get a range of different sizes.
[00:37:47 - 00:38:00] So they might be used in things like your printers if you need kind of precision in your different elements of your machine.
[00:38:00 - 00:38:12] So here we see that example for the timing belt and obviously making the connection between our pistons and our cam shaft which is operating our valves.
[00:38:12 - 00:38:22] So we want to make sure that this doesn't slip and we want to make sure that our engine is able to continue running without kind of clashing into each other.
[00:38:22 - 00:38:30] So these kind of timing belts are also used on devices such as our hovercraft.
[00:38:30 - 00:38:41] They often power the large kind of fan which in this case here we can see 200 kilowatt motor is used to drive the fan and it's a toothbout which is the connection.
[00:38:41 - 00:38:47] between these two components.
[00:38:47 - 00:38:52] So there's pretty much our stuff on belt now we're talking about chains.
[00:38:52 - 00:38:56] So similar to the balance here are the large variety in chains as well.
[00:38:56 - 00:38:59] They're kind of two main types of chains.
[00:38:59 - 00:39:04] So we have chains that are for power transmission or we have conveyor chains.
[00:39:04 - 00:39:13] So in each case they are kind of specific kind of conventions around each of these different types.
[00:39:13 - 00:39:20] So we can see that there's as the rougheners have brought us standard in an American standard.
[00:39:20 - 00:39:27] So these are now referred to with different ISO type A and type B for our power transmission chains.
[00:39:27 - 00:39:39] And then we also have some other types of chains that are also used for power transmission including agricultural role chains, side bow chains and tablet top chains.
[00:39:39 - 00:39:47] And if our conveyors we often have this be S-conveyor or these other types of chains as well.
[00:39:47 - 00:39:53] mainly be focusing on chains for power transmission in these slides.
[00:39:53 - 00:40:01] So we can see here is our example of what the cross section or the top view of a side bow chain looks like.
[00:40:01 - 00:40:12] Again we have our B-S-S conveyor chain here on the right and then range of other chains on the spot on the central photo.
[00:40:12 - 00:40:21] In your assignment you do have all the other chains but we don't have to specify right.
[00:40:21 - 00:40:25] We just told it we go standard pulley that there will be a chain that runs in it.
[00:40:25 - 00:40:38] Now I can't remember how much detail what I wrote into the assignment brief but I actually kind of sized the pulley from one of the Reynolds Kennel dialogues.
[00:40:38 - 00:40:45] I'm always amazed when I saw the scroll through this catalogues with the amount of information and detail that is provided there.
[00:40:45 - 00:40:51] But basically these are the guys that make power transmission chains for roller coasters.
[00:40:51 - 00:40:55] They have specific products that they are like.
[00:40:55 - 00:40:58] If you've got a roller coaster this is the chain for you.
[00:40:58 - 00:41:03] So I kind of just wanted to highlight that there and also I found like down things like this.
[00:41:03 - 00:41:25] I also wanted to highlight ISK if propaganda I quite like seeing the family tree of chains and learning how roller chains had offspring of our kind of European and American chains which we sort of saw now which just lies in the different types of offspring that they would have all the commonalities that they have.
[00:41:25 - 00:41:44] So again if you want to have some further reading or you have to do some stuff around picking a chain then I'm just trying to highlight that the resources that manufacturers provide is actually really useful to make sure that you do things in a systematic and efficient way.
[00:41:44 - 00:41:52] As I said earlier in the machine when we first started doing machine alignment things, the machines have been made for hundreds of years.
[00:41:52 - 00:41:58] So we really can just build on the knowledge of people who have done it before us rather than trying to reinvent the wheel.
[00:41:58 - 00:42:00] So similarly you'll see that that's why.
[00:42:00 - 00:42:07] And each of these lectures is pretty much a design catalog that is useful to kind of show.
[00:42:07 - 00:42:14] So I think eventually here they actually start talking about the actual products that they have that do a lot of information.
[00:42:14 - 00:42:16] I'll just one might just leave the design guide actually.
[00:42:16 - 00:42:23] But yeah they have another catalog that looks very similar to your bearing catalog.
[00:42:23 - 00:42:32] We pretty much you just have oh this is this type of chain and it comes in these kind of links and this is the information that you need as a designer.
[00:42:32 - 00:42:52] So as we saw in the pictures we can get a range of standard pictures for each of our different chains and they can be arranged in multiple kind of strands if our kind of design requirement desires.
[00:42:52 - 00:43:14] So we have my style have in my box of toys I suppose is three strands that we can have as we see here a range of different sizes with different kind of chains and then sprochts for those chains to run on.
[00:43:14 - 00:43:31] So chain length is defined by the number of pictures which I suppose makes sense and then we also have a minimum number of teeth that is recommended on our sprochts.
[00:43:31 - 00:43:47] So a transmit more power than bouts for there are a lot noisier than bouts and they do not require pretension although allowance for stretch is required and ideally we should have no slip.
[00:43:47 - 00:43:55] Now I don't have don't have this well because I've got the other V-box Christian open I don't have this one open.
[00:43:55 - 00:44:03] In the design scenario where no slip is required what options would there be to transmit power.
[00:44:03 - 00:44:10] So I guess I'll give you two options and we can go 5050 with what would be the best answer.
[00:44:10 - 00:44:25] So option one would be a flat bout or option two would be a timing bout which one would be better.
[00:44:25 - 00:44:30] So hands up if you think option one would be better.
[00:44:30 - 00:44:48] So I kind of simplified the question obviously on V-box there was actually like six options but the kind of two things in terms of your design specification where you if you want no slip you pretty much need to use a timing bout.
[00:44:48 - 00:44:54] So a square-tooth timing bout or you can use a chain and a smock it right.
[00:44:54 - 00:45:08] So those were the two kind of quick answers but last year when I did it I remember I don't know if you were cooking like V-gaffin stuff and I'm like am I getting pranked but I appreciate you guys for not pranking me today.
[00:45:08 - 00:45:20] So in terms of our all the chain features there is some slight variation in the chain velocity which is called called all speed variation and we'll talk about this a little bit.
[00:45:20 - 00:45:29] but basically it has to do with that number of the minimum number of teeth and then what the actual velocity of our chain is.
[00:45:29 - 00:45:34] So chains need lubrication often light oil and not grease.
[00:45:34 - 00:45:41] They are standard power ratings which are given for having a life of 15,000 hours.
[00:45:41 - 00:45:48] So these standard power ratings will be reduced if we have multiple strands extra large or extra small sprockets.
[00:45:48 - 00:45:57] More than two sprocket drives, shock loads in our system or poor lubrication or poor environmental conditions.
[00:45:57 - 00:46:07] So a worn chain will stretch and ride high on the sprocket which we'll talk about in a little bit again and the factor is catalogs.
[00:46:07 - 00:46:22] So this stretch that occurs what I'm trying to say is that it's not actually that your chain is acting like a piece of elastic kind of rubber band.
[00:46:22 - 00:46:35] And much stretch of a very little bit but obviously the stiffness of your chain is such that it's not really going to move in the orders of magnitude that we're going to talk about.
[00:46:35 - 00:46:38] So what is the stretch that we're talking about?
[00:46:38 - 00:46:52] Well as a chain gets worn what you may find, maybe I'll do on this bigger one here, is that eventually what used to ride on your pulley,
[00:46:52 - 00:46:57] well you just ride on your sprocket quite well, stopped riding quite well.
[00:46:57 - 00:47:04] So I don't know if you can see that here but it's perfectly aligned on this bit here and as we keep coming around.
[00:47:04 - 00:47:11] And around and around eventually it doesn't even sit into our sprocket.
[00:47:11 - 00:47:21] So this is taken out of an old bike. Couldn't very well have been one of my old bikes because I remember when I was at uni my bike would always be like slipping the chain.
[00:47:21 - 00:47:26] That's because the chain is pretty much worn and then they see that stretched.
[00:47:26 - 00:47:33] But essentially this stretch has actually just occurred from where I try to, where I change the connection, connecting.
[00:47:33 - 00:47:41] So that kind of changes the distance between each of the chains very slightly, what's kind of adds up over time, right?
[00:47:41 - 00:47:47] So again it's almost like that whole similar discussion of our torrenting kind of combining.
[00:47:47 - 00:47:52] And often I think what people will do if they're in a bike shop, they will have a sort of sit,
[00:47:52 - 00:47:56] standing the kind of measurement tool that they use to check that your chain is not overly stretched.
[00:47:56 - 00:48:00] And they might also look at what the flexibility of your chain is.
[00:48:00 - 00:48:06] Because if it's really flexible then that's like a telltale sign that your chain is really old.
[00:48:06 - 00:48:11] So I guess the annoying thing from a consumer's point of view is that then you have to replace the whole sit.
[00:48:11 - 00:48:20] You can't just buy a new chain but often you need to buy the new kind of spockets as well because they will have some wear on them as well.
[00:48:20 - 00:48:24] And so we see some information about this here.
[00:48:24 - 00:48:28] And if you want to learn more about that about the bicycle kind of chains, sort of stuff that we talked about.
[00:48:28 - 00:48:34] Again there's a nice video here that I'll leave in your capable hands.
[00:48:34 - 00:48:43] Cool. So again we can see some examples of double strand roller chains which are from Shiggly.
[00:48:43 - 00:48:48] And then we see our sprockets, some information on those there.
[00:48:48 - 00:48:52] So we get some terminology that's defined in the image.
[00:48:52 - 00:48:56] And then we want to talk about our quarter-speed variation.
[00:48:56 - 00:49:01] So the radius of the chain that enters this rocket theory between teeth.
[00:49:01 - 00:49:08] By the dimension E. So we see that E is this dimension here.
[00:49:08 - 00:49:16] This is a result of a slight variation in speed that is significant only when the sprockets are small.
[00:49:16 - 00:49:28] So when the sprocket with an insufficient number of teeth is used, each tooth on the sprocket engages in disengages, the driving opponent at a more significant and full compared to a sprocket with more teeth.
[00:49:28 - 00:49:35] This uneven engagement causes fluctuations in the effective radius of the sprocket during rotation,
[00:49:35 - 00:49:38] resulting in our varying speed.
[00:49:38 - 00:49:41] So we see the sprocket here kind of describes that.
[00:49:41 - 00:49:45] It shows that if you get less than kind of 17 teeth, I think was the recommendation.
[00:49:45 - 00:49:53] And you get a lot of variation in your chain velocity as your sprocket rotates.
[00:49:53 - 00:50:00] So if you want the harker, we don't have time for it.
[00:50:00 - 00:50:10] But if again, if you want to kind of look at a visualization of this, there are definitely some gifts that kind of demonstrate that as your number of teeth kind of decrease,
[00:50:10 - 00:50:12] they're being there for velocity changes.
[00:50:12 - 00:50:23] But essentially, it's same thing as that magic number for your sprocket teeth to kind of avoid this speed variation from being significant.
[00:50:23 - 00:50:26] Cool. So we've also talked about, I suppose, timing belts.
[00:50:26 - 00:50:33] So timing chains is what we'll sort of finish on, which are used and can be used on our internal combustion engines.
[00:50:33 - 00:50:37] We see some pros and cons of each of them here, with our chains.
[00:50:37 - 00:50:43] So last much longer, you really need to replace them, but they are more expensive up front, especially if you do need to replace it.
[00:50:43 - 00:50:50] Whereas timing belts need to be replaced every, I think, about 80 to 100,000 kilometres.
[00:50:50 - 00:50:54] So if you've got a car and you're not sure if it's a timing belt or a timing chain,
[00:50:54 - 00:51:05] it's definitely get that kind of checked out, because if it is a camp out, then again, the last thing you want to have happen is your cart will explode essentially.
[00:51:05 - 00:51:09] So with that sharing note, I'll leave it there.
[00:51:09 - 00:51:15] All the best for the final manufacturer, and next week we have a guest lecture at this time.
[00:51:15 - 00:51:19] It's not a new time though. I'll make a post on Friday about that.
[00:51:19 - 00:51:43] Thank you.
[00:52:00 - 00:52:14] So I think you've not said something just before we came in.
[00:52:14 - 00:52:18] I'm aware of the things.
[00:53:14 - 00:53:40] That's a good question.
[00:53:40 - 00:53:47] So, I think that's a good question.
[00:53:47 - 00:53:56] So we need to say it's that this is a new time.
[00:53:56 - 00:54:17] So, I think that's a good question.
[00:54:17 - 00:54:44] So, I think that's a good question.
[00:54:44 - 00:54:53] So, I think that's a good question.
[00:54:53 - 00:55:17] So, I think that's a good question.

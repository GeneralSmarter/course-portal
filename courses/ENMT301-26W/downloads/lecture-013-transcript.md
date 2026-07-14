# ENMT301-26W Lecture 13 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_13_audio_16k_mono_32k.mp3`
Source audio SHA-256: `f8a0be65a816db8665f1991c36ec9917f974019c163fea5c5dd8981278481d61`
Generated: 2026-06-06T05:23:55.037854+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:09 - 00:00:24] Alright, thank you Rob. We'll make a start there if that's all good.
[00:00:26 - 00:00:28] Just wait for these people to take their seats.
[00:00:28 - 00:00:30] I'll just get them to it.
[00:00:36 - 00:00:38] Alright, thank you Rob. We'll make a start there now.
[00:00:38 - 00:00:51] Week three feels like it feels like we've been going a long time now, but
[00:00:51 - 00:00:55] apparently it's only week three. I don't know about you guys, but feel like we're
[00:00:55 - 00:00:58] really quite well into things.
[00:00:58 - 00:01:10] So you'll see obviously that you will see that there is some poll
[00:01:10 - 00:01:14] questions on learn, which we're going to review in the tutorial.
[00:01:14 - 00:01:17] And I looked at them yesterday and I've put them in the tutorial slides because
[00:01:17 - 00:01:20] I like to be organized and give you things in advance.
[00:01:20 - 00:01:25] And some of them didn't have the most response to it, which you know,
[00:01:25 - 00:01:31] it's all good for me because I'm not having to kind of, I don't know,
[00:01:31 - 00:01:36] appear my results to these results. But if you do have any material testing that you've done,
[00:01:36 - 00:01:41] please make sure you track your questions. Just one person per team obviously.
[00:01:41 - 00:01:46] And then they'll kind of help to give a better, well, the interesting to
[00:01:46 - 00:01:50] compare what the results that were showed this week in the tutorial are compared to
[00:01:50 - 00:01:52] kind of following which I guess is what I'm trying to say.
[00:01:52 - 00:01:56] So if you've done your material testing, then make sure that you put that in there
[00:01:56 - 00:02:01] just so that I can pull that data for future use.
[00:02:01 - 00:02:08] Cool. So today's lecture is going to be primarily focusing on shaft design and
[00:02:08 - 00:02:13] key way design. So we've pretty much gone through most of the content that we need to
[00:02:13 - 00:02:18] for your alien structure assignment as I sort of tried to make really clear.
[00:02:18 - 00:02:23] We've tried to front load a lot of the information so that you guys have everything that you need to basically
[00:02:23 - 00:02:27] do the assignment. So at this point in time, there's nothing stopping you
[00:02:27 - 00:02:32] from working hard in submitting this assignment this week essentially.
[00:02:32 - 00:02:36] So we've gone through everything. So that's sort of the door that I'll try to leave open for you guys,
[00:02:36 - 00:02:41] especially because I know things get really busy towards week five and week six of this
[00:02:41 - 00:02:47] term. So if you're in your partner like to kind of want to get something out of the way,
[00:02:47 - 00:02:52] there's no reason why you can't do that in regards to this assignment.
[00:02:52 - 00:02:55] Cool. So, it looks good.
[00:02:55 - 00:03:00] I said the looks today will be focusing on shaft design and obviously because we're in academic
[00:03:00 - 00:03:05] institution, a lot of what our lecturers are doing is kind of doing research as
[00:03:05 - 00:03:08] for you to send it to their time and also publishing that research.
[00:03:08 - 00:03:13] So just to give you some experience or some insights into what some of these might look like,
[00:03:13 - 00:03:19] there is this review paper which is on common kind of modes of failure for shaft in mechanical
[00:03:19 - 00:03:24] equipment. So I've just put that on learn as a kind of further reading reference
[00:03:24 - 00:03:27] if that's something that you're particularly interested in.
[00:03:27 - 00:03:32] If we have time we can kind of have a look at it that kind of is going to be kind of
[00:03:32 - 00:03:37] quite interesting I suppose in terms of looking at a shaft design more generally,
[00:03:37 - 00:03:40] especially if you're not really sure or haven't had much experience with that.
[00:03:40 - 00:03:44] So all of the stuff that we're covering on the literature is kind of going forward.
[00:03:44 - 00:03:49] It's related to our second kind of main assignment and similarly the idea is that we want to make sure
[00:03:49 - 00:03:53] sure that you've got a good amount of information so that when we give you the assignment
[00:03:53 - 00:03:57] if you want to get started with it you can you don't have to kind of wait and get kind
[00:03:57 - 00:04:01] of food feed or bread crumb along the process.
[00:04:01 - 00:04:06] So before we get into things a couple things to note.
[00:04:06 - 00:04:13] So one the tasks on our flow chart that we drew in one of the very early tutorials
[00:04:13 - 00:04:15] look like something like this right.
[00:04:15 - 00:04:22] And so what I wanted to see is how many people have done will make a crack at some of the material testing.
[00:04:22 - 00:04:23] Cool.
[00:04:23 - 00:04:27] Yeah so I thought that there was going to be the case a lot of people have done that.
[00:04:27 - 00:04:34] So that's kind of one task that you're going to need to do but you can also do these tasks over here parallel at the same time.
[00:04:34 - 00:04:40] So who has kind of at least decided the number of members, the shape that their members are going to be,
[00:04:40 - 00:04:46] done with their free body diagram and decided what their failure mess is going to be on the day.
[00:04:46 - 00:04:48] Okay slightly less.
[00:04:48 - 00:04:57] For those that have not done, done list but then I'm just going to assume that maybe it's because you haven't made out of your partner yet and you don't really want to think about it.
[00:04:57 - 00:05:04] But I wouldn't dwell on, I wouldn't leave starting this to too long because this weird mentality things happens.
[00:05:04 - 00:05:09] I've got so much work on now I don't want to start because it seems like a lot.
[00:05:09 - 00:05:23] So I would break down these decisions and sort of if I was to give you a goal I'd say by the end of the day at least have your shape, your free body diagram and your target failure mess kind of completed because that leads in to all the other staff right.
[00:05:23 - 00:05:31] If you know that then at least that's one thing that you can kind of say sweet that's done on my assignment and I at least know what I'm kind of going for.
[00:05:31 - 00:05:34] I'm going for a three-view infrastructure and it's going to break it through the kgs.
[00:05:34 - 00:05:36] That's the way to start the going.
[00:05:36 - 00:05:39] So I'm going to start looking at it, I'll look at it on the 19th.
[00:05:39 - 00:05:48] So then from that has many people done be kind of stress analysis or any kind of failure or non-failure calculations.
[00:05:48 - 00:05:51] Okay, so that's all good.
[00:05:51 - 00:06:02] What we'll see is there's no reason why for each of our members we can't kind of basically make a checklist and work out what it is that you would need to calculate.
[00:06:02 - 00:06:07] So for these ones here the reason that I put this first is because it's our non-failure members right.
[00:06:07 - 00:06:19] So the calculation or the comment on the calculation is a lot less anxiety inducing, a lot less stressful because all you're trying to say is, yeah,
[00:06:19 - 00:06:24] I think it's not going to buckle and I know that a load needs to be five times what the load that's going to be on it when it's got the
[00:06:24 - 00:06:28] the 2d kg on for it to actually not fail, right?
[00:06:28 - 00:06:36] So for these non-failure ones you're going to have a factor of safety and then be happy with the fact that it probably is not from a bracket, right?
[00:06:36 - 00:06:52] Then we're going to go and do our stress concentrations which we discussed a little bit on Friday, I'm sure everyone has had a look at that tutorial but I kind of wanted to make sure that we are aware that that is kind of like the next step that you would be doing, right?
[00:06:52 - 00:06:56] So has anyone done this stress concentration or an stress concentration stuff?
[00:06:56 - 00:07:11] Cool, I know some people were asking about it so that's okay but because we, I might leave the comment that I was going to kind of have or discussion I was going to have about this for the tutorial on the afternoon and just because it will probably more closely align right?
[00:07:11 - 00:07:21] So if you haven't done this stuff and you've got some time in the day I'd say try and get that kind of tick off and then when I'm talking about these non-failure kind of calculations that we can do,
[00:07:21 - 00:07:29] I know that we did a list somewhere for each member, yeah there's ones here.
[00:07:29 - 00:07:34] So these ones here for example for our compression members doing this kind of buckling calculator,
[00:07:34 - 00:07:41] you know your eye values is kind of something that you can do without even having a material testing data as long as you assume a young's modular, right?
[00:07:41 - 00:07:45] So yeah, cool.
[00:07:45 - 00:07:53] We'll talk about some of the stress concentration assumptions I think in this afternoon since I don't think we're all
[00:07:53 - 00:07:56] on that kind of thing on that way now.
[00:07:56 - 00:08:07] So for your failure calculations obviously you have to have an idea of your design so I think it's really important that you lock in what that is so you least know what kind of what kind of work you need to complete
[00:08:07 - 00:08:13] and then from there you know if you know that you have a compression member you'll know that I can do work out my eye values in each plane
[00:08:13 - 00:08:22] and then I can work out which way it's going to be most likely to kind of buckle and then once you have kind of built up that catalogue of all of those calculations,
[00:08:22 - 00:08:29] you'll be able to know which ones are the most likely to happen and that will be what dictates your failure modes, right?
[00:08:29 - 00:08:40] So first value mode should always be your stress concentration and then what does failure mode do and what does failure mode three will kind of depend on your design and the design decisions you've made, right?
[00:08:40 - 00:08:55] Obviously I think most people will be aware but material testing this week I believe is available after midday because there's a ton of little class happening at the moment and another reminder just to make sure that you guys know not to be
[00:08:55 - 00:09:01] used the one so one so's which are being freshly painted all the warm and table as a workspace.
[00:09:01 - 00:09:09] Don Pukas came into Martha's other day and kind of made sure that I told you guys so I'm just taking that one off.
[00:09:09 - 00:09:24] Cool so as we saw the key side from the last tutorial was this idea of our stress concentrations and we know that it's defined by our kind of our next stress compared to our nominal stress that we see.
[00:09:24 - 00:09:33] we get these cave A's and for a lot of simple kind of loading cases where we have stress concentrations there are these kind of plots that exist, right?
[00:09:33 - 00:09:47] So we've been over these kind of ideas of what is the nominal stress at the whole and away from the whole and the main reason is that we want to make it really clear that this nominal stress is different at these places, right?
[00:09:47 - 00:10:01] because the area is different so at the whole the area would just be above and below the whole so we have a smaller area which means the stress will be higher before even considering the fact that there is a stress concentration at the edge, right?
[00:10:01 - 00:10:15] So then away from the whole we have a bigger a bigger area so we have a lower stress and so then the next stress which would be by our whole would be our cave value times by our nominal stress at the whole right?
[00:10:15 - 00:10:23] So that's just something that we went through a few you'll remember on Friday we kind of went through and wrote out those kind of calculations.
[00:10:23 - 00:10:35] So the thing that we need to just make sure we're all clear about is what is the difference for brittle and ductile materials in terms of stress concentrations?
[00:10:35 - 00:10:40] Are they the same or do they act slightly differently?
[00:10:40 - 00:11:07] And so what we see is we went over again I'm just trying to do this so I know some people had a big Friday Saturday and then might have when they watch this not necessarily been paying attention so I want to make it really clear so that we don't have on test a lots of unexpected failures that intro to we had what I think is probably my favourite line of any notes either because it's just like don't trust me, you know?
[00:11:07 - 00:11:32] That's like that's the vibe that it gives. So we see here however for ductile materials it will be localized failure that results in permanent information around the stress concentration region this relaxation may deregis to root the load below the yield string around the stress concentration region thus reducing the apparent stress concentration factor not to one but to possibly approximately 1.1.
[00:11:32 - 00:11:46] So the reason that we have this apparent stress concentration factor coefficient which could be the terminology that you use is because typically we don't really use stress concentrations to be indicative of failure, right?
[00:11:46 - 00:11:56] Now we'll use them to go cool. It's not going to fail when we've taken this into account it was being conservative and used a pay value that means that I know it's definitely not going to fail.
[00:11:56 - 00:12:17] In this case we're wanting it to fail so you guys are going to have to do some verification of what your apparent stress concentration is and what we talked about which is what I was going to talk about in the tutorial but it seems like I sort of just feed myself into this pipeline of telling you right now is that this is something that you'll have to kind of check.
[00:12:17 - 00:12:26] And so roughly speaking what my process would be is that if you've got a hole you could look at what the K-value would be on a graph and say oh it looks like it's going to be too.
[00:12:26 - 00:12:40] However based on the notes that I've been given the fact that I know it's ductile material I might pick a value of approximately 1.1 for my K-value to start with to the size my whole slash thickness of my mender.
[00:12:40 - 00:12:56] Yeah and so what assumption what we'd be making when we're doing that failure calculation we're showing it the next stress would approximately be equal to our something from your testing.
[00:12:56 - 00:13:03] Is that the yield stress that you guys are designed to or do you think that the ultimate tin cells just would be more appropriate.
[00:13:03 - 00:13:22] See some more notes for ultimate tin cells stress so what you're saying and what the kind of approximation or assumption is is that if the stress in the mender at the failure mass is approximately the stress of your ultimate tin cell testing.
[00:13:22 - 00:13:27] Yeah when you add more mass on on the test day what do you think will happen.
[00:13:27 - 00:13:36] That's a bigger one it's super hard to hear.
[00:13:36 - 00:13:42] Yeah so you know you assume that and then you know you're going to add on the test day your next 5 kg what happens.
[00:13:42 - 00:13:51] The bracket right even like blistering as quietly as possible as well I see that you just didn't hear me.
[00:13:51 - 00:14:02] Yeah and so the reason that I'm making that really clear is that yeah that whole point of that stress concentrations are not used to be indicative of failure.
[00:14:02 - 00:14:18] So we have to kind of make sure that our our thinking about that is kind of clear and I think if I am not incorrect that when you do your stress strain plots that for aluminum they kind of look kind of like this and then they break right.
[00:14:18 - 00:14:20] Or do they have a hump.
[00:14:20 - 00:14:27] Do you have a hump you have some strong laws but like this or do they keep coming down like this.
[00:14:27 - 00:14:37] Yeah cool so what you're saying is that if I assume that I designed this just to be this point when I add more force and I go up here more it's definitely going to be past that way right.
[00:14:37 - 00:14:42] Because we're doing we're not like a tin cell tin cell t's where we just go slowly right.
[00:14:42 - 00:14:47] We're adding like slowly adding or the loading right is kind of a bit quicker.
[00:14:47 - 00:14:49] I'll see not shock loading it yeah.
[00:14:49 - 00:14:56] Cool see some faces that seem like that may sense some that are like Georgia haven't even looked at this I don't want to think about it.
[00:14:56 - 00:15:04] I'm not sure if they're morning so I'll leave it there but we can revisit that in the tutorial if it was something about that that we can clarify.
[00:15:04 - 00:15:07] Just want to make that okay very thing quite clear.
[00:15:07 - 00:15:14] Cool so we've done our notices and our silent one discussion and now we're into our shaft design stuff.
[00:15:14 - 00:15:25] So similar to most of our other kind of machines on lectures you'll see that should be the SKF kind of catalog for bearings and these kind of do which men and fundamental machine elements are really good.
[00:15:25 - 00:15:27] resources to use.
[00:15:27 - 00:15:33] So the thing is with machines there's that machine has been designed for hundreds of years and people have kind of the
[00:15:33 - 00:15:39] reprocess of making bad designs and then working out how you can't do that to make it a machine that's going to work.
[00:15:39 - 00:15:44] It's really good kind of gold standard references in terms of what it works.
[00:15:44 - 00:15:54] So often a lot of the time these books are kind of like the goal to place because very concise or the kettle logs are very concise in terms of the information that they tell you and it's all quite kind of the kind of
[00:15:54 - 00:15:57] key information to use.
[00:15:57 - 00:16:02] So a little note to get us start while we're sort of thinking about stress concentrations.
[00:16:02 - 00:16:06] So suppose we end up specifying an 18 millimeter bar for lecture two.
[00:16:06 - 00:16:15] For this the overall vector of safety can be determined as the following if we assume a yield stress of 245 meter per skills.
[00:16:15 - 00:16:20] So a vector of safety of approximately 3.1.
[00:16:20 - 00:16:33] However, suppose when you check the bar and the workshop that is going to use you find out that there's actually a circle of groove around the center 2.5 millimeters deep with a radius at the bottom of 0.5 millimeters.
[00:16:33 - 00:16:37] The same two-ton load is applied. What is the stress now?
[00:16:37 - 00:16:44] So what do we think the circle of groove is going to do to the stress in the bar around the circle of groove?
[00:16:44 - 00:16:50] We'll increase it.
[00:16:50 - 00:17:04] Cool. So what we see here is if we refer to our stress concentration factors for our kind of bar and our groove we can work out what our K-value is using our ratios of R over D and big D over little D.
[00:17:04 - 00:17:09] And we get that the stress concentration factor from the plot is approximately 3.5.
[00:17:09 - 00:17:15] So does this mean that the max stress is simply 78.59 times 3.5.
[00:17:15 - 00:17:20] So the nominal stress we had before times 3.5.
[00:17:20 - 00:17:27] Hands up if you reckon yes. Hands up if you reckon no. Cool.
[00:17:27 - 00:17:30] So most people who answered answer correctly.
[00:17:30 - 00:17:37] And what we actually would need to do is work out what the nominal stresses at that kind of area with a circle of us to work out what the stresses.
[00:17:37 - 00:17:41] So we see that the nominal stress is actually slightly higher than what we had before.
[00:17:41 - 00:17:47] And that gives our max stress which is our stress concentration times our nominal stress being 291.
[00:17:47 - 00:17:51] And our factor of safety is now 0.84.
[00:17:51 - 00:18:00] So this introduction of a circle of groove has basically mean that the bar is beyond the yield with a steady load.
[00:18:00 - 00:18:05] So it might be appropriate to assume that if the weight was jerk off the ground of the crane or similar,
[00:18:05 - 00:18:09] there was some kind of shock load applied that our bar would fail.
[00:18:09 - 00:18:18] So stress concentration is a real thing and something that you would need to consider if you want to make sure things are designed with due diligence.
[00:18:18 - 00:18:24] So this is the kind of typical process that you would use and it's slightly different to what we see in our assignment.
[00:18:24 - 00:18:27] We're actually wanting it to fail, right?
[00:18:27 - 00:18:32] Cool. So into our kind of shaft design stuff, we start with just a nice definition.
[00:18:32 - 00:18:40] The shaft is a rotating member, usually a circular cross-section due to transmitt power or motion.
[00:18:40 - 00:18:46] It provides an axis of rotation from machine elements including gears, pulleys, flywheels, cranks and sprockets.
[00:18:46 - 00:18:51] And we'll see some examples of shafts and how those kind of machine elements are attached.
[00:18:51 - 00:18:56] A spindle is a rotating element which with a foot shift or holding a load.
[00:18:56 - 00:19:03] So you'll see that that's kind of what Tony and the workshop refers to when they have the mill kind of spinning.
[00:19:03 - 00:19:05] There's the spindle in the middle.
[00:19:05 - 00:19:09] So an axle as well is slightly different.
[00:19:09 - 00:19:13] It's non-rotating so it's not a shaft and it carries no torque.
[00:19:13 - 00:19:17] Up does support rotating wheels or pulleys.
[00:19:17 - 00:19:23] Cool. So we see that there are a range of attributes related to designing shafts
[00:19:23 - 00:19:28] and these can typically be categorized into functional geometric and material properties.
[00:19:28 - 00:19:35] So in terms of function, obviously you want it to be able to transmit power from one point to another retention.
[00:19:35 - 00:19:38] You don't want things to be able to move along the place.
[00:19:38 - 00:19:45] You want some sort of rigidity. You can imagine if you were trying to use a piece of kind of cooked spaghetti as a shaft.
[00:19:45 - 00:19:49] That probably wouldn't work very well because of its low rigidity.
[00:19:49 - 00:19:51] And then also a seam mobility.
[00:19:51 - 00:19:56] So this is the kind of thing that we really want you to have some experience with when you do the bearing housing assignment.
[00:19:56 - 00:20:05] And you'll have to think about each of these kind of functional attributes to make sure that the shaft that you guys design is fit for purpose in these ways.
[00:20:05 - 00:20:13] What we see geometric wise is as we said that's typically circular because we have some amount of a seam mobility.
[00:20:13 - 00:20:18] So we might want to be able to put shafts on and off and we might want them not to be able to just slide wherever they want to.
[00:20:18 - 00:20:28] So we have some retention that those will typically introduce shoulders which then this change in geometry rule and choose stress concentration factors.
[00:20:28 - 00:20:36] And the layout and spacing is also quite important to make sure that you can actually assemble or disassemble it with enough space.
[00:20:36 - 00:20:47] And then you will have to pick a material that is kind of fit for purpose both in terms of stiffness and hardness and then possibly corrosion resistance depending on the environment that it is in.
[00:20:47 - 00:20:55] So typically the process that you would follow is the picker material so that you have no one material properties.
[00:20:55 - 00:21:03] You would do what we all have to do as a free body diagram and a geometric layout of your design depending on what the specifications and constraints are.
[00:21:03 - 00:21:10] And how many kind of other machine elements are going to be on our shaft and what kind of forces those will be transmitting.
[00:21:10 - 00:21:13] We'll do some stress and strength calculations.
[00:21:13 - 00:21:22] So we'll look at the statics strength which can include beding portion compression, thermal effects and effects of stress concentrations.
[00:21:22 - 00:21:29] And we may also look at our fatigue strength since these lows will be applied in cyclic kind of way.
[00:21:29 - 00:21:39] And then for our deflection and rigidity analysis we'll look at both our bending and torsional deflection and the slope of the bearings to make sure that they
[00:21:39 - 00:21:45] are not going to make the bearings fail prematurely.
[00:21:45 - 00:21:52] So she had the friction and drew transverse loadings of the short shafts can also be something worth considering.
[00:21:52 - 00:21:58] And then you may do some further analysis depending on the nature of the machine you are designing.
[00:21:58 - 00:22:03] And obviously drawings before manufacture.
[00:22:03 - 00:22:08] So here we see a few kind of pieces of information about the terminology of the shaft.
[00:22:08 - 00:22:17] In this case we have a spline at the end. If anyone's ever had a no attractor with a has like a narrow attachment or something like that.
[00:22:17 - 00:22:21] You'll probably have kind of seen these kind of splines and stuff in the past.
[00:22:21 - 00:22:24] These kind of reduced sections are called undercuts.
[00:22:24 - 00:22:32] And then obviously we've got radiists, radiists and shoulders so that we could have something like a bearing sitting in here.
[00:22:32 - 00:22:38] We've got a stress relief cutout in here to reduce the stress concentration from this radius.
[00:22:38 - 00:22:45] Similarly we have a circuit roof here which would be introducing a stress concentration and then towards the end.
[00:22:45 - 00:22:48] In this case we have a tapered face with a keyway.
[00:22:48 - 00:22:53] We might have kind of like a half a half moon or a semi circular keyway in there.
[00:22:53 - 00:22:59] And then some sort of thread that we can lock, but even machine element on the edge on it.
[00:22:59 - 00:23:00] Cool.
[00:23:00 - 00:23:04] So three body diagrams will always be critical to analyze your no loads.
[00:23:04 - 00:23:13] And something like this is sort of indicative of what we might see for our assignment later on in the semester.
[00:23:13 - 00:23:21] So for some types of gears you may have both axial and radial loads that you need to consider.
[00:23:21 - 00:23:30] So you'll need to make sure that shear force and binny moment and torque diagrams are completed in each plane so that you can design your shaft.
[00:23:30 - 00:23:36] So a little bit of a full experiment which is the better layout.
[00:23:36 - 00:23:38] The top or the bottom.
[00:23:38 - 00:23:45] So if you have a couple seconds to kind of think about it hopefully we can all kind of vote so that I can make sure we're all following a long.
[00:23:45 - 00:23:50] So through here thinks that number the top one is better.
[00:23:50 - 00:23:53] And then who thinks that the bottom one is better.
[00:23:53 - 00:23:54] Cool.
[00:23:54 - 00:24:02] So depending on what our constraints are if it was no constraint about the distance that we need for like a similar ability.
[00:24:02 - 00:24:04] And that's all the side of things.
[00:24:04 - 00:24:14] Then the bottom one is going to reduce the kind of binny moment that we see in our shaft which will might mean that we can have a lower shaft size.
[00:24:14 - 00:24:21] So typically if we're trying to reduce the loads and then design things more economically than this would be a better kind of consideration.
[00:24:21 - 00:24:26] Sometimes there might be a minimum requirement that forces you to have to do this above that.
[00:24:26 - 00:24:32] Generally speaking on the question that we see here the bottom answer is probably more appropriate.
[00:24:32 - 00:24:39] So we see an example of that binny moment for the plane that we see in this one here.
[00:24:39 - 00:24:40] Cool.
[00:24:40 - 00:24:49] Typically shafts will have to also have a fixed bearing location and a free bearing location.
[00:24:49 - 00:24:55] And we'll talk about this a little bit more when it comes to actually our bearing housing and bearing kind of design.
[00:24:55 - 00:25:04] So what we can see here is that this one in the shaft the bearing is kind of in a race and the outer acts are both locked in the fixed position.
[00:25:04 - 00:25:09] And then the other one is actually free at the top so that it can slide either way.
[00:25:09 - 00:25:22] The idea is that this means that if it's working over a certain kind of temperature gradient that our shaft is not going to have to endure that thermal stress from trying to push if we had both two fixed bearings right.
[00:25:22 - 00:25:29] We'll talk about this a little bit more when it comes to our bearing housings design.
[00:25:29 - 00:25:36] So then we see another kind of example, in this case for high rigidity we have two tapered roll bearings very short shaft.
[00:25:36 - 00:25:45] But again just another example showing how we have different shaft features in this case we've got a shoulder here.
[00:25:45 - 00:25:54] And it looks like another smaller shoulder here but to make sure that our earrings and shaft arrangement work together.
[00:25:54 - 00:26:05] Then another one here, this one here is a little bit more complex and we see that it also has these kind of oil drippers which is interesting and it's a couple kind of things to see.
[00:26:05 - 00:26:18] So we can see here that our shaft similar to what we saw in our kind of terminology has a number of different features from tapered areas, shoulders and radiuses.
[00:26:18 - 00:26:25] So here we see a student design probably an example of not a good design to copy.
[00:26:25 - 00:26:33] But what we can see is that this is an example of what you might end up doing in your assignment for your kind of drawing.
[00:26:33 - 00:26:42] The main thing that's kind of quite bad here is that we've got two bearings side by side and because of that it's going to mean that there's kind of a moment.
[00:26:42 - 00:26:43] Well it's quite hard.
[00:26:43 - 00:26:50] Things as a spec what's happened is that the student's picked up earring and then thought, oh, don't go to calculation and thought, oh this is not a sprig enough bearing.
[00:26:50 - 00:26:51] I just add two bearings there.
[00:26:51 - 00:27:01] The thing is that that sort of changes the assumptions that send your free body diagram and it's not a assumption that you can make that the force would be shared equally.
[00:27:01 - 00:27:05] And then at the same time because we've kind of got two pin joints here and here.
[00:27:05 - 00:27:08] So that means that there's going to be different loading in our shaft.
[00:27:08 - 00:27:17] So typically what you'll want to make sure is that you just have one bearing that is big enough to hold the loading requirements of your design.
[00:27:17 - 00:27:21] So we'll talk about, and then some of the other stuff is not too bad.
[00:27:21 - 00:27:23] It's got some locating spriggots.
[00:27:23 - 00:27:25] The cross-hatching is going the right way.
[00:27:25 - 00:27:28] Got a key way that's been shown.
[00:27:28 - 00:27:30] The shaft hasn't been positioned.
[00:27:30 - 00:27:38] So there are some good things but the fact that it's got two bearing size probably not the best thing.
[00:27:38 - 00:27:47] So generally, axial thrust load should be taken to ground through a single thrust bearing for load direction.
[00:27:47 - 00:27:56] So we want to have one bearing that kind of takes all of the axial load rather than having two in a game trying to work out how much load is shared between each of them.
[00:27:56 - 00:28:02] So don't split those axial loads between two bearings and then shaft lengths slash distances.
[00:28:02 - 00:28:09] The twin components and bearings should be kept as short as possible to minimize both deflections and stresses.
[00:28:09 - 00:28:16] But sometimes there's practical kind of reasons why you can't just have everything exactly close by each other.
[00:28:16 - 00:28:20] So there are also some practical kind of considerations.
[00:28:20 - 00:28:22] Do you always have to do it yourself?
[00:28:22 - 00:28:29] Sometimes when you're trying to support your bearing if you're just doing something that you're doing is a one-off kind of thing,
[00:28:29 - 00:28:32] then you might just use what's called a plumber's block.
[00:28:32 - 00:28:36] As you can we can talk about a little bit more in our bearing housing.
[00:28:36 - 00:28:51] Lature, but basically these are a bearing and bearing housing component that can be bought off the shelf rather than trying and designing a kind of specific purpose built the spoke kind of shaft and bearing housing arrangement,
[00:28:51 - 00:28:54] which is kind of what the second assignment will be focusing on.
[00:28:54 - 00:29:02] So we won't be using these in their assignment, but I think most people have gone through a lab last year that talked about the idea of a spoke manufacturing.
[00:29:02 - 00:29:13] I think there's a whisper tick sort of stuff from Don Lucas where we saw different tolerances and limits and fits for the bearing and shaft arrangement versus there's our mass produced sorry.
[00:29:13 - 00:29:26] So if we're doing a spoke or one-off thing we might just use something like this will be have a shaft and then have a bearing that can just attach to our shaft or be located through tightening this lock nut.
[00:29:26 - 00:29:33] Cool. So standard shaft formula just to show you where we kind of get some of these equations that we use.
[00:29:33 - 00:29:39] We can see that we know that our stress and shear stress and Benin stress are defined as the following.
[00:29:39 - 00:29:43] And that using more circle we can put those together to get a max shear stress.
[00:29:43 - 00:29:49] And then if we substitute the equations from this slide into there and rearrange a little bit we can get this.
[00:29:49 - 00:29:57] So I'm this equation here where I'm actually stressed is based on our diameter and moment and talk.
[00:29:57 - 00:30:09] And then from our maximum shear stress failure theory we can work out to incorporate into this what our factor of safety will be.
[00:30:09 - 00:30:19] Assuming that we want to keep our stress below half of the next shear stress or divide by two at least and then the factor of safety over there.
[00:30:19 - 00:30:24] So we get something that looks like this for a static loading case.
[00:30:24 - 00:30:33] So we can work out what our diameter should be based on the moments the talks and our factor of safety as well as our material properties.
[00:30:33 - 00:30:39] So similarly, shegley has got a sorry, the ACME.
[00:30:39 - 00:30:48] So session of mechanical engineering, American association of mechanical engineering has this formula which does the same kind of thing.
[00:30:48 - 00:30:50] Has a very similar kind of format.
[00:30:50 - 00:30:55] We can see that it also incorporates our kind of load factors which we talked about last week.
[00:30:55 - 00:31:02] So whatever your moment in your talkers depending on what the situation is you can have a factor that you apply to it.
[00:31:02 - 00:31:06] And then this equation here has no in anywhere.
[00:31:06 - 00:31:09] So there is a factor of safety that's being built in.
[00:31:09 - 00:31:17] Often this is quite a useful kind of first calculation you kind of do to work out what your minimum shelf thickness should be based on your loading requirements.
[00:31:17 - 00:31:26] So if I was not annotating here this is the kind of one where I'd say like use this to work out the initial shaft diameter in this sum.
[00:31:26 - 00:31:33] So here we see those C values for different kind of loading conditions.
[00:31:33 - 00:31:35] Cool, so a little question for you.
[00:31:35 - 00:31:42] Before you're designing the following shaft obviously we want to design for the minimum shaft thickness, right?
[00:31:42 - 00:31:46] Which one here would be the shaft that we need to design for?
[00:31:46 - 00:31:48] Which location?
[00:31:48 - 00:31:55] So get your finds out and answer is probably what sort of a suggesting here.
[00:31:55 - 00:31:58] Put a lot of time in there for making this question for you guys.
[00:31:58 - 00:32:41] Hopefully most people are finalising the answer of what they think.
[00:32:41 - 00:32:53] Which diameter, which position in the shaft should be the one that you calculate for.
[00:32:53 - 00:32:56] So, it's interesting.
[00:32:56 - 00:33:06] If I said D8 is an answer I wonder what people would change the answer to be.
[00:33:06 - 00:33:07] So this is the thing about it.
[00:33:07 - 00:33:10] Why would D8 possibly not be the right answer?
[00:33:10 - 00:33:16] Well if we think about where the force is transmitted, we've obviously got some torque being applied through our spigot here.
[00:33:16 - 00:33:21] So definitely through our shaft and then this face here is another key way, right?
[00:33:21 - 00:33:27] So the force is going to go through there and then this here is just sort of like this cutout here is to enable us to have
[00:33:27 - 00:33:30] into our thread.
[00:33:30 - 00:33:34] So if you were to change your answer, I don't know if you're allowed to do that.
[00:33:34 - 00:33:36] Are we allowed to change it?
[00:33:36 - 00:33:37] Well thank you are.
[00:33:37 - 00:33:43] So if we are to change the answer we see two is making power moves and there we have it.
[00:33:43 - 00:33:46] The correct answer is number two.
[00:33:46 - 00:33:51] So if we look there we can see that the torque is definitely going through diameter two.
[00:33:51 - 00:33:57] And that this is the smallest diameter throughout that kind of place with the load is transmitted, right?
[00:33:57 - 00:34:03] So what we would need to do is kind of if we were looking at this from a kind of an analytics point of view,
[00:34:03 - 00:34:08] we would have our shear force and be in moment diagram for our shaft along that kind of length.
[00:34:08 - 00:34:15] And we would need to pick what our kind of moment is and our torque is at that point there, right?
[00:34:15 - 00:34:18] So we might also need to do that in another case.
[00:34:18 - 00:34:28] Somewhere in the middle maybe if there's like a particularly high moment in that location just to make sure that this bigger diameter is still big enough for that.
[00:34:28 - 00:34:31] We'll go through that a little bit in the future.
[00:34:31 - 00:34:36] So we can see here that we've got power coming in and out of those two faces that we saw.
[00:34:36 - 00:34:42] And here we see a quick example of using this ACME diameter calculation.
[00:34:42 - 00:34:47] So if we were to kind of calculate what that diameter was and our arrangement looked at something like this.
[00:34:47 - 00:34:56] So we might have a couple bearings in between and we have some sort of force from a flywheel that will be creating a moment.
[00:34:56 - 00:34:58] We could work out for that point.
[00:34:58 - 00:35:00] What is our moment and what is our torque?
[00:35:00 - 00:35:06] Work out what our kind of low factors are for both our bending and torque.
[00:35:06 - 00:35:11] And then we can plug those values into the equation to work out that at that location there.
[00:35:11 - 00:35:16] We should have a minimum diameter of at least 41.8.
[00:35:16 - 00:35:21] So just a nice example.
[00:35:21 - 00:35:30] Cool. So cyclic loads occur when applied loads are applied over and over again or being applied and then removed.
[00:35:30 - 00:35:38] So for example, if we see the shaft in this kind of diagram here, if we have a belt that's got some tension on it.
[00:35:38 - 00:35:43] As our shaft is rotating, one side of the shaft will be in compression.
[00:35:43 - 00:35:54] The other side will be in tension and so we can see that at any one point in the shaft that will be fluctuating between those two loads.
[00:35:54 - 00:36:03] And so what we need to do in this case is we would define what these kind of mean loads are and alternating loads are.
[00:36:03 - 00:36:11] And so in this case here if we're looking at this diagram, our amplitude of our moment would just be what the moment is.
[00:36:11 - 00:36:17] And then that's being reversed. And so because it's being completely reversed, the mean value would be zero.
[00:36:17 - 00:36:24] And then in the opposite kind of way, we don't have any fluctuations or we're not assuming any fluctuations in our torque,
[00:36:24 - 00:36:27] which is the shoom that is applying a steady torque.
[00:36:27 - 00:36:31] And so our mean torque would be that torque value there.
[00:36:31 - 00:36:47] And so, for cyclic loads, we can't just use this equation here because we see that there's no kind of none of these kind of alternating loads have actually been taken into consideration.
[00:36:47 - 00:36:53] So there are other formulas that we think has formula as one of those that does take this into consideration.
[00:36:53 - 00:37:05] And we can see that it does still follow a pretty similar kind of format that we do also have our mean load divided by our yield, right?
[00:37:05 - 00:37:09] And then we've got S e here, which stands for our endurance limit.
[00:37:09 - 00:37:13] For those, do you mind remember endurance limits?
[00:37:13 - 00:37:15] We have heard of them before.
[00:37:15 - 00:37:24] So if you're unfamiliar with what they are, basically it's an old assumption that if the stress is below this endurance limit,
[00:37:24 - 00:37:26] the T is not going to be the failure.
[00:37:26 - 00:37:33] So we have this kind of idea that if we have a really high stress, then it only has a certain number of cycles before it fails.
[00:37:33 - 00:37:41] And once we get down now, down now kind of down now kind of curves, I can kind of draw that makes a little bit more sense.
[00:37:41 - 00:37:45] I feel like I'm just waving my hands around a little bit.
[00:37:45 - 00:37:59] But if we have a plot that is our stress and our number of cycles, what we often see is that there is this kind of curve that the failures might happen along.
[00:37:59 - 00:38:02] So as we lower the stress, it can last more cycles.
[00:38:02 - 00:38:10] But at some point, it typically does no failures in this kind of area here.
[00:38:10 - 00:38:20] So that value there is what they define as the endurance limit and form materials that have had some material testing done on them.
[00:38:20 - 00:38:23] Then you actually get to this value here.
[00:38:23 - 00:38:27] Otherwise we can talk about ways to kind of estimate it.
[00:38:27 - 00:38:34] But this won't be kind of a small part of the assignment because fatigue is like a further consideration.
[00:38:34 - 00:38:39] And I'd rather that we do all of our kind of static loading a lot better.
[00:38:39 - 00:38:48] Cool. So before I keep moving, what I'm just going to show, because I think the next thing, so we have a number of stress concentration plots.
[00:38:48 - 00:38:49] That's the effort completeness.
[00:38:49 - 00:38:52] And then we're talking about key ways and pens.
[00:38:52 - 00:39:01] So before I go through it, what we can just see in part of round is some examples of shafts that have been have failed.
[00:39:01 - 00:39:04] So this one here is actually kind of failed.
[00:39:04 - 00:39:17] There used to be a guy in our department, Marla Croul, who did a lot of material investigations or stuff using the scanning electron microscope and material testing equipment to try and work out what those kind of failures were.
[00:39:17 - 00:39:22] But what we can see here is just some examples of shafts and shaft features.
[00:39:22 - 00:39:27] So obviously we've got some sort of key way where our power will be being transmitted.
[00:39:27 - 00:39:32] We can see that it's just been cut slotted out all the way to the end.
[00:39:32 - 00:39:38] And then we had some circuit groves and it looks like they probably would have been a bearing or similar in this case here.
[00:39:38 - 00:39:40] Right up against this shaft, right?
[00:39:40 - 00:39:43] So we can measure the effort bearing was in here and then we put a circuit on it.
[00:39:43 - 00:39:47] The bearing is not allowed. We're not able to kind of slide around the place.
[00:39:47 - 00:39:54] So our shaft and our bearing are kind of locating it so that it can't just float out into eternity, right?
[00:39:54 - 00:39:55] Cool.
[00:39:55 - 00:39:58] We see similar kind of things here.
[00:39:58 - 00:40:03] So this one here we have different kind of key way or key kind of dimensions.
[00:40:03 - 00:40:10] But we see that we still have had some sort of key way milled or similar into our shaft.
[00:40:10 - 00:40:18] And then we also have some shoulders that might help us to locate student parts, right?
[00:40:18 - 00:40:25] So in this case here, not sure if there was a lock nut or similar to actually actually restraint,
[00:40:25 - 00:40:32] or whether there was actually two components up against each other and then a surclup to hold them in this location here.
[00:40:32 - 00:40:37] Again, just some examples of a different kind of key way.
[00:40:37 - 00:40:46] Following on from that, just to put into reality what we saw with some of our example terminology.
[00:40:46 - 00:40:54] Sometimes we might have some of our machine kind of components actually integrated into part of our system.
[00:40:54 - 00:41:06] And then in this case here again, we've got this kind of tapered region at the end with a key way hole so that we can have some sort of a flange or tapered flange kind of come onto here.
[00:41:06 - 00:41:13] And we know that when we tighten this, that there's going to be located based on that taper.
[00:41:13 - 00:41:21] And then similarly we do have some sort of radiuses that reduce kind of the stress concentrations that we see.
[00:41:21 - 00:41:27] So there'll probably be some sort of lock nut that you put on the end in that tightens that flange that you see there.
[00:41:27 - 00:41:31] Cool. And then finally another way that you can see.
[00:41:31 - 00:41:42] Sometimes you might have a shoulder and then a threaded kind of lock nut to show where the bearing or machine element is kind of how it in place, right?
[00:41:42 - 00:41:54] In this case here, it looks like it isn't actually a... it doesn't look like there is a keyway or whatever this machine element is.
[00:41:54 - 00:42:01] So it's most likely that it's a bearing where it doesn't actually need a key way to hold it in place.
[00:42:01 - 00:42:09] But if you did have like a spigot or similar, then you would actually need one more thing that's sprocket.
[00:42:09 - 00:42:15] So if you had a sprocket and you would want to have some sort of keyway there, make sure that that force and power is transmitted, right?
[00:42:15 - 00:42:18] But obviously what you see is where this thread is.
[00:42:18 - 00:42:23] There has to be a lower or a smaller diameter before the thread, right?
[00:42:23 - 00:42:26] Otherwise you can't get this threaded and lock nut in.
[00:42:26 - 00:42:31] And these are all kind of considerations that need to be taken into account.
[00:42:31 - 00:42:36] So past these around, maybe some got this side and some got this side.
[00:42:36 - 00:42:44] But sometimes it's nice to see something sort of physical rather than just looking at the terminology that we're kind of been covering.
[00:42:44 - 00:42:54] And then we're going to be talking about the keyways so you'll see that there are a few different kind of ways of doing the keyways on those shafts.
[00:42:54 - 00:43:03] So here we see that keys and pins are used to secure rotating elements on the shaft where we need to transmit torque.
[00:43:03 - 00:43:06] So at the bearing we don't really need to transmit torques.
[00:43:06 - 00:43:12] We don't need these kind of features unless it's used to kind of locate them.
[00:43:12 - 00:43:18] So a regular shortcut is that we have a keyway in our shaft.
[00:43:18 - 00:43:25] We need to increase the diameter by 10% to try and address any stress concentrations that are right.
[00:43:25 - 00:43:29] So that's kind of normally done in the first instance.
[00:43:29 - 00:43:35] So in case otherwise you don't know how much to increase the part of the end of the other check whether it's going to be safe or not.
[00:43:35 - 00:43:38] So here we see a couple examples.
[00:43:38 - 00:43:46] So we have a good key which is tapered and firmly driven into your between your shaft and your machine element.
[00:43:46 - 00:43:55] So it's easy to remove which is a pro but it has a protruding edge which can be hazardous which is one of the cons.
[00:43:55 - 00:44:02] So you can see that there is still a keyway that's been kind of cut out based on the dotted line here which is shown kind of hidden detail.
[00:44:02 - 00:44:13] And then another one that we've seen which has also been in our tapered kind of fixtures that we see woodruff key can be used.
[00:44:13 - 00:44:17] And that's used in smaller shafts to prevent the key from rolling.
[00:44:17 - 00:44:30] So once you kind of get it in the right spot then you know that it will be not able to roll based on the kind of geometry of your machine element.
[00:44:30 - 00:44:39] Cool. So there are a number of resources that decal standard dimensions and torrents for keyways to make sure that you can actually get your key in and out easily.
[00:44:39 - 00:44:43] And you'll see that this is just one example that kind of shows up.
[00:44:43 - 00:44:51] in this kind of key and it's a square parallel key that these are the torrents that you can use typically.
[00:44:51 - 00:44:54] Cool.
[00:44:54 - 00:45:06] For example of key so you can have either your standard square key, you can have a flatter key or an extra fin key depending on what they kind of space requirements and talk.
[00:45:06 - 00:45:16] Talk requirements of your situation and you'll see that these different kind of keyways can have different manufacturing techniques that are used.
[00:45:16 - 00:45:21] So you could have a profiled keyway which we see some of some of those in the examples that we're putting around.
[00:45:21 - 00:45:24] All you might have one that's been made with a slid runner.
[00:45:24 - 00:45:31] Sometimes they'll also go all the way out to the end to give it easy access to get your kind of keyway in there.
[00:45:32 - 00:45:54] Cool. So in terms of calculating the stress and then the strength of your key, keys can be failed in a number of ways including sharing, compressing failure of your key and then similarly share or compressive failure of your shaft or the pulley or other piece of machine arm and that's on the other side of your shaft.
[00:45:54 - 00:46:05] So the beginning failure and the shaft at the keyway can also happen to the stress concentration or bending failure of the couple can also be something that happens.
[00:46:05 - 00:46:19] So it's normal to choose a key cross-section to be a quarter of the shaft diameter to have a square kind of cross-section and then you just use a calculation to determine the length of the key can be one approach to use.
[00:46:19 - 00:46:23] So otherwise you have too many unknowns and you sort of have to start somewhere.
[00:46:23 - 00:46:28] So this is a recommendation that can help you in terms of getting started.
[00:46:28 - 00:46:41] So here are the two important calculations that have key calculations for calculating the shear stress and compressive stress for keyways.
[00:46:41 - 00:46:53] So obviously for a squeaky I believe these equations will be the same or the result of the equation will be the same but if you have a different dimension then there may be different.
[00:46:53 - 00:47:06] But there are the difference in being a shear or a compressive stress does need to be taken into consideration when you then work out what your factor of safety is or what the likely mode of failure is.
[00:47:06 - 00:47:22] So for our shear we can obviously see that this is shear of our key then we do have compressive stress which can be based or you need to use compressive stress on both your coupling or your shaft.
[00:47:22 - 00:47:25] So let's see that there.
[00:47:25 - 00:47:44] So if the key is the weakest part which is normally the way that you were designed your shaft and keyway then the calculations on this page will be sufficient if other components fail first and calculations through the sex would need to be taken more seriously or considered.
[00:47:44 - 00:47:52] So for dimensions and tolerances that is this nice kind of book engineers black book in the library which is a pretty good resource.
[00:47:52 - 00:47:55] So if you do want to know some machine kind of element.
[00:47:55 - 00:48:02] Tiringists and similar and this is the thing that Tony has a copy of when he's machining different kind of things.
[00:48:02 - 00:48:12] So if we go back and just have a look at what our example calculation was we'll see hello this is actually a shearing of a key in a crushing of a shaft calculation.
[00:48:12 - 00:48:17] And that's basically the equation or the calculation that they have done.
[00:48:17 - 00:48:21] And I've also indicated what the tolerances are of that keyway.
[00:48:21 - 00:48:31] So we make sure that the key and that kind of keyway adequately sized to be able to get our key in there nicely.
[00:48:31 - 00:48:41] And so just to finish we do also have some examples that kind of visualize these kind of calculations because I know sometimes the crushing calculations are a little bit weird.
[00:48:41 - 00:48:45] To think about if you don't just see here's an example of this.
[00:48:45 - 00:48:52] So obviously keyway shearing is easy and intuitive to think about the keyway is basically just getting cut in half.
[00:48:52 - 00:48:59] But shaft crushing would be where we have this big deformation from the compressive stress on our shaft.
[00:48:59 - 00:49:06] So this way here would be the fact that our shaft is deformed and shows that kind of happening.
[00:49:06 - 00:49:10] We could also have our hub or our coupling crushing.
[00:49:10 - 00:49:15] And again we can see there's a large deformation of in this case this upper piece here.
[00:49:15 - 00:49:27] So to do that if you're doing that kind of calculation in the different material properties you'd have to use those when you're working out what the shis, the stress is in the factor of safety in comparing those.
[00:49:27 - 00:49:36] And then here we see an example of our shaft breaking where the stress concentration from the keyway has initiated a crack.
[00:49:36 - 00:49:42] Cool. So in summary we've got shafts that support our bearings and transmit power through devices.
[00:49:42 - 00:49:45] And must be sized adequately and sustained.
[00:49:45 - 00:49:52] Being able to sustain a combination of bending and torsional loads.
[00:49:52 - 00:49:55] Shout out mentions can be calculated in verified using first principles.
[00:49:55 - 00:49:59] And we may have other components and un-sids using keyways.
[00:49:59 - 00:50:02] And we'll learn about those in upcoming glitches.
[00:50:02 - 00:50:03] Thanks, Aron.
[00:50:03 - 00:50:32] I just probably closed this in just in case the next keyway can run.
[00:50:32 - 00:50:35] Are you?
[00:51:21 - 00:51:26] I'm not sure.
[00:51:26 - 00:51:29] I'm not sure.
[00:51:29 - 00:51:32] I'm not sure.
[00:51:32 - 00:51:35] I'm sure.
[00:51:35 - 00:51:40] I'm sure.
[00:51:40 - 00:51:47] I'm sure.
[00:51:47 - 00:51:54] I'm sure.
[00:51:54 - 00:52:01] I'm sure.
[00:52:01 - 00:52:08] I'm sure.
[00:52:08 - 00:52:15] I'm sure.
[00:52:15 - 00:52:22] I'm sure.
[00:52:22 - 00:52:29] I'm sure.
[00:52:29 - 00:52:36] I'm sure.
[00:52:36 - 00:52:43] I'm sure.
[00:52:43 - 00:52:50] I'm sure.
[00:52:50 - 00:52:57] I'm sure.
[00:52:57 - 00:53:04] I'm sure.
[00:53:04 - 00:53:11] I'm sure.
[00:53:11 - 00:53:18] I'm sure.
[00:53:18 - 00:53:25] I'm sure.
[00:53:25 - 00:53:32] I'm sure.
[00:53:32 - 00:53:39] I'm sure.
[00:53:39 - 00:53:46] I'm sure.
[00:53:46 - 00:53:53] I'm sure.
[00:53:53 - 00:54:00] I'm sure.
[00:54:00 - 00:54:07] I'm sure.
[00:54:07 - 00:54:14] I'm sure.
[00:54:14 - 00:54:23] I'm sure.
[00:54:23 - 00:54:30] I'm sure.
[00:54:30 - 00:54:37] I'm sure.
[00:54:37 - 00:54:44] I'm sure.
[00:54:44 - 00:54:51] I'm sure.
[00:54:51 - 00:54:58] I'm sure.

# ENMT301-26W Lecture 08 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `1b0a9d38b71a1f630f323dd4a3f7506512e2bc977f77c8a2fcba713e4fb9368f`
Generated: 2026-06-06T05:10:56.081557+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:20 - 00:00:21] Alright, thanks for having us.
[00:00:21 - 00:00:22] We'll make a start there.
[00:00:22 - 00:00:41] Alright, thanks everyone, we'll get into it.
[00:00:41 - 00:00:48] Oh, tenoco too-co-tore.
[00:00:48 - 00:00:56] If Pihyana-co-to, how are you all doing some thumbs up big day?
[00:00:56 - 00:01:00] Do you guys think like back to back stuff all day today or do you have a gap?
[00:01:00 - 00:01:01] Lunch break?
[00:01:01 - 00:01:02] Yes.
[00:01:02 - 00:01:03] Oh, that's nice.
[00:01:03 - 00:01:06] That's better than not having a lunch break.
[00:01:06 - 00:01:12] I don't know why our university doesn't enforce a no-class during lunchtime rule,
[00:01:12 - 00:01:19] but hopefully you're a manager to have some sustenance before our tutorial today.
[00:01:19 - 00:01:26] Cool, so as the title suggests, the tutorial today will be focusing on further kind of design
[00:01:26 - 00:01:32] considerations for our aluminium structure assignment and it'll kind of be building on some of the stuff we know
[00:01:32 - 00:01:38] over last week and then also hopefully iron out some potential gotchers that you might not have
[00:01:38 - 00:01:44] considered in terms of your design and the assumptions that you are making within your design.
[00:01:44 - 00:01:51] So obviously if you have done your material testing, feel free to fill out these kind of quizzes
[00:01:51 - 00:01:57] and as I said in the lecture, I'll hopefully be able to collect these so that this time next week I can have a little section where I highlight
[00:01:57 - 00:02:04] what results people have been sort of getting, but obviously this data is really indicative
[00:02:04 - 00:02:05] of what you think is important.
[00:02:05 - 00:02:10] You'll all need to do your own material testing if you get any results that you actually sort of trust for yourself.
[00:02:10 - 00:02:18] So as I sort of highlighted, some people might accidentally put the yield or the UTS at the wrong way around or vice versa.
[00:02:18 - 00:02:26] So make sure that you as the engineer have a good understanding of what you think the material properties are for your aluminium strips.
[00:02:26 - 00:02:31] As we found, we do have our drop-in sessions on Mondays.
[00:02:31 - 00:02:37] So it might be something that if later in the week you've got some questions or some questions or answers you've worked on.
[00:02:37 - 00:02:44] The assignment, this is a really good opportunity to kind of ask some questions in the low-stakes environment.
[00:02:44 - 00:02:50] And obviously there will be the opportunity to collect the aluminium strips during this time too.
[00:02:50 - 00:02:52] Cool. So roadmap for tutorial three.
[00:02:52 - 00:02:58] Folks on any burning questions you guys have. We'll go to an overview slash summary of rivets and adhesives.
[00:02:58 - 00:03:09] And then we'll discuss some future work considerations, including quickly going over buckling and sort of also looking at what might happen in terms of buckling of your ends.
[00:03:09 - 00:03:21] We'll talk about rivets and glue as we sit above and also discuss some in details to hopefully avoid you making the same mistakes students have previously kind of made.
[00:03:21 - 00:03:34] But one of those funny things where I feel like I can tell, I could say this every single time about some of these considerations and there will always be someone in the class that still manages to ignore the discussion.
[00:03:34 - 00:03:41] But hopefully they'll mean that we don't have as many unexpected failures during the test day and week eight.
[00:03:41 - 00:03:46] Cool. So what burning questions do you guys currently have?
[00:03:46 - 00:04:08] So I get told when I've done that, like, you know, teaching stuff that like, give students 10 seconds to answer a question after.
[00:04:08 - 00:04:12] So otherwise find some questions. No, sweet. We're good to go and then get nothing.
[00:04:12 - 00:04:15] But seems like there's nothing that far.
[00:04:15 - 00:04:20] Is there a question or there's just a stretch? Looks like there's just a stretch. Fair enough.
[00:04:20 - 00:04:27] So this is good. It either means everything's crystal clear and the world is fine or it means we're not sure what we don't know yet.
[00:04:27 - 00:04:32] So we can't ask you any questions which is also fine. I'm sure those questions will pop up as we go.
[00:04:32 - 00:04:41] So I prepared some questions and I thought you guys might ask or want to at least discuss all that if I was a student I would want to discuss.
[00:04:41 - 00:04:49] And so I guess one of them is sort of a question flipped back on you to see if whether what we went through last week kind of, uh,
[00:04:49 - 00:04:58] checks out. But where do we think that the best ways to optimize our design would be?
[00:04:58 - 00:05:03] Does that open question? We're a small class like we're half the size would normally be probably just under half.
[00:05:03 - 00:05:08] So don't feel afraid. There's not many people here. No, I would judge why you say.
[00:05:08 - 00:05:14] So where should we be? Where is the way that we can optimize our design in terms of strength to wait?
[00:05:14 - 00:05:21] The number of members is one way. So some people from the get go, they know two is smaller than three.
[00:05:21 - 00:05:25] Therefore two equals lighter than three, right? Cool. That's a pretty good one.
[00:05:25 - 00:05:31] Some people won't want to take the risk of, I know having their math kind of work out.
[00:05:31 - 00:05:37] Trust physics. Some people have have a problem with doing that in the first instance, which is fair enough.
[00:05:37 - 00:05:47] What if you test on a nominally day? So if you have selected a three member structure, we might be able to optimize from there.
[00:05:47 - 00:05:52] What things can you toggle and what things do I recommend not necessarily to be?
[00:05:52 - 00:05:59] Can remove material so we can either make material like our teacher member who can make that thinner rather than being 20 mil the whole way, right? Cool.
[00:05:59 - 00:06:07] We can do that in a number of ways. I think we've seen examples of people drilling these other holes in them or thinning out sections.
[00:06:07 - 00:06:16] Obviously this is not a failure member that looks kind of dog bone-esque. You could have a failure member that or a non-fail member that has reduced material cool.
[00:06:16 - 00:06:26] For our compression members, what can we do? I don't know, speaker wants us so hard to hear you over each other.
[00:06:26 - 00:06:31] What can we do for our compression members?
[00:06:31 - 00:06:37] Clear the geometry to reduce buckling.
[00:06:37 - 00:06:41] Yes, so you can have a small cross section without...
[00:06:41 - 00:06:46] Yeah, so we can toggle what our cross section looks like, right?
[00:06:46 - 00:06:51] Some people go for your standard kind of I-beam or H-beam depending on what orientation it is.
[00:06:51 - 00:06:58] These people here have drilled some holes for weight reduction, but you might also want to have a different kind of cross section.
[00:06:58 - 00:07:01] So here we have a T-member.
[00:07:01 - 00:07:07] We went through this last week a bunch of different options for those, right?
[00:07:07 - 00:07:09] So we said we could do all of these things here.
[00:07:09 - 00:07:17] This was sort of like a C-weather we remember what happened last week, but seems like everyone's still a little bit shy in the class, but that's all good.
[00:07:17 - 00:07:25] Cool. And then what I guess is the recommended not to do in terms of that particular design,
[00:07:25 - 00:07:28] to relate it to where the pins are.
[00:07:28 - 00:07:33] It's the best to keep the pins in all the corners, what have some pins going halfway through your members.
[00:07:33 - 00:07:39] Keep them in the corners. Why, what does that do?
[00:07:39 - 00:07:50] It's not buckling, but I said the keyword I was looking for at the end there.
[00:07:50 - 00:07:55] So there's going to be an additional force which means there's bending in the design, right?
[00:07:55 - 00:08:01] And so my recommendation is avoid bending, go for simplicity, so I might as well just sit in the lecture today.
[00:08:01 - 00:08:07] Simple as good, we can trust it. If we have pin joints in the corners, those pin joints can't hold any moments.
[00:08:07 - 00:08:13] Therefore our members are an axial tension or compression, right? Cool.
[00:08:13 - 00:08:18] So I'm assuming that was all like it runs on the vibe of George McGetless.
[00:08:18 - 00:08:23] I wish you didn't talk about it. And if that's the case, just make sure you say that to me and I can go straight through.
[00:08:23 - 00:08:26] You just say I think we're happy with where we can optimize.
[00:08:26 - 00:08:40] We've talked about ways we can reduce the weight of our design and we'll discuss some kind of considerations in terms of how you know or how to calculate as too much material has been removed or not.
[00:08:40 - 00:08:54] Cool. For those that are doing two member design questions, we did have a few people discuss this in the drop in sessions, but the key thing to remember us, is that the mess of, so if we go on our almaemus assignment,
[00:08:54 - 00:09:01] the mess of our roller support needs to be considered, right?
[00:09:01 - 00:09:09] So the reason that we have a slight upwards angle is that this upper support has a mess, right?
[00:09:09 - 00:09:18] So in that calculation that we did last week, the example calculation, I assumed that there was no mess related to the upper support, right?
[00:09:18 - 00:09:28] So has anyone done a free body diagram for a right angle triangle with the right angle at the top corner?
[00:09:28 - 00:09:32] Yeah. And what did you find happen in your vertical member?
[00:09:32 - 00:09:48] Yeah. So this, so if you do it that way, right? I'm not going to draw it, but if we had a right angle triangle with the right angle at the top, because we've assumed that there's no mess on that roller, the force, then your vertical member ends up being zero, right?
[00:09:48 - 00:09:55] Which obviously is like not real, because it's actually a small force related to this upper support, right? Cool.
[00:09:55 - 00:10:09] So for your two-member structure, that's definitely something you need to consider, and that's why there's a slight angle in that angle will be there in relation to your sum of your forces and your y direction to make sure that those are equal.
[00:10:09 - 00:10:13] Yeah. Cool. See some slight nods.
[00:10:13 - 00:10:27] So what's that? Is that raised any other further questions that people have about the assignment or anything that we're doing in general?
[00:10:27 - 00:10:33] Sweet. So, Riekat, let's think about each member and the complete free body diagram.
[00:10:33 - 00:10:42] So on Friday we did make a list that kind of showed us what we were doing, what calculations we recommended kind of doing, right?
[00:10:42 - 00:10:55] So, does anyone made a start on any of those? We can do better, like, tell me yes or down we know, but I really cannot read your mind.
[00:10:55 - 00:11:02] Has anyone done any stress calculations so far? No. Has anyone done any free body diagrams so far?
[00:11:02 - 00:11:13] Some people say no, some people say yes. So once you've got your free body diagram for your failure load, that opens the door to be able to do some of these calculations, right?
[00:11:13 - 00:11:31] I guess what I was trying to emphasize last week is that you could design your non-failure members, I hear your buckling members, they'd be pretty happy that they get locked in early before we talk about our stress concentrations and the failure member, right?
[00:11:31 - 00:11:57] Cool. Is there anything on here that's missing? We did it pretty quickly in the end. There's something that's missing that's the little like hint, but any ideas, any ideas?
[00:11:57 - 00:12:11] Then member buckling. So, we said, I like it, but we said we did say end buckling, which I guess I'm going to kind of put in the same kind of rounders, thinned member buckling.
[00:12:11 - 00:12:18] The same to do with the thing that's not mentioned on the page at all, but something that you have to use for putting together your compression members.
[00:12:18 - 00:12:28] Or you're teaching members if you're making them out of more than one piece.
[00:12:28 - 00:12:38] Rivets or glue, right? And so you can see on here we don't have rivets or glue mentioned anywhere, and this is often a question that people ask me.
[00:12:38 - 00:12:46] George, do we need to do calculation of rivets, strength or glue? And what do you guys reckon the answer is?
[00:12:46 - 00:12:57] Yes, if it's practical to do so. And so this is possibly the start of a frustrating series of answers of sometimes an engineering design.
[00:12:57 - 00:13:12] The answer is genuinely it depends, right? And the reason for that is I can show on a little sketch, because sometimes it might be impossible to actually work out what the stress is going through a rivet or through a glued joint, right?
[00:13:12 - 00:13:21] So to put it a simple way for us to show a simple example where it makes sense and it's a nice easy kind of calculation to do.
[00:13:21 - 00:13:28] This here we can see, and if you can see it, there's three members of the aluminium.
[00:13:28 - 00:13:34] They've added an extra one, but sometimes people will have the member look like this.
[00:13:34 - 00:13:44] So they might have three like this. Or they have in this case they've done three altogether which actually makes it slightly more problematic for me.
[00:13:44 - 00:13:50] So in this case here, we can imagine we've got a pin going through this, and we can assume that it might be in tension.
[00:13:50 - 00:14:04] In this case here, where is our forces going to go through our members? We would draw our load path.
[00:14:04 - 00:14:16] You might want to say it, so I don't have to hear my voice. So if we had rivets here, we had one rivet here.
[00:14:16 - 00:14:28] So we can imagine the forces probably in the either go, it's coming through the member, thing going to go through the rivet, and then into, and so kind of the back here where our pin is joining, right?
[00:14:28 - 00:14:34] You're right, so I'm happy with that. So in this case, what forces acting on our rivet?
[00:14:34 - 00:14:42] Shear, right? That's a nice easy calculation to do. It's literally like the textbook examples that you see.
[00:14:42 - 00:14:51] You might not agree with that. Same sort of thing. Imagine that if it wasn't riveted, that instead it was glued, right?
[00:14:51 - 00:15:03] Again, the glues and shear, and often they give you a shear strength of the glue, which is a little bit more dubious because you have to assume that you've made the correct manufacturing process steps as per day requirements, which we can have a look at.
[00:15:03 - 00:15:12] If you know how to look at those technical data sheets, but they don't give you a kind of stress that it should be able to be strong enough to hold, right?
[00:15:12 - 00:15:26] Cool. Where it gets kind of complicated, and this is why it depends, some people might not ever have a loading case in their design where that is a possible loading case, right?
[00:15:26 - 00:15:38] So the other option is if we had something looks like this, we've got our pin for our eye beam, and this could be glued or it could be riveted that connector, right?
[00:15:38 - 00:15:52] This is the Anyforce, or how much force is going to go through the the glued part, which is essentially going through here. Hard to say, right?
[00:15:53 - 00:15:58] There's not any clear load path, kind of showing it.
[00:15:58 - 00:16:07] We've seen some examples where things have kind of come unglued and then there's been like a local or a localized kind of buckling of a specific member that's come detached.
[00:16:07 - 00:16:11] But that's also not really like a glue failure calculation that you could do, right?
[00:16:11 - 00:16:15] That's just the single member by itself kind of buckling.
[00:16:15 - 00:16:33] So in this case, what we can really say to you is that you would have to make an assumption that your glue will be strong enough, and I guess the reason you can make that assumption is by looking at past years designs and the fact that they seem to have been over glue it and it's held, right?
[00:16:33 - 00:16:39] That would be the case where it's not really practical to do a calculation on the glue or the rivet's strength, right?
[00:16:39 - 00:16:48] But if there's one like this and it's really obvious that the force is clearly in sheer, then that would be an appropriate time to do that calculation.
[00:16:48 - 00:16:56] Any questions about any of that?
[00:16:56 - 00:17:02] Cool. So here we go, little recap. What are the in conditions of this one here? Can someone remind me?
[00:17:02 - 00:17:09] It's got fixed pinned. Yep, the fixed theoretical. And then what about this one here, theoretical?
[00:17:09 - 00:17:15] Fixed fixed. But in reality, what assumption would we use for our in condition?
[00:17:15 - 00:17:21] For being ultra conservative, we'll use a value of one for our constant.
[00:17:21 - 00:17:25] If we want to use a recommended value, it might be more like 1.2 or something yet.
[00:17:25 - 00:17:28] But again, just making that really clear, good work.
[00:17:28 - 00:17:32] And so what we can see here is another question for you.
[00:17:32 - 00:17:42] How might we calculate the buckling of an extended end or a whole, a long, kind of slotted hole in our mid-ratt?
[00:17:42 - 00:17:50] So for example, I mean, yeah, I mean, we could use this here as a good example, right?
[00:17:50 - 00:17:58] So if we look at this member here, how might we calculate with a from, let's just draw that?
[00:17:58 - 00:18:07] How might we calculate this? This is our member. I'll draw it this way. I'll make it ultra exaggerated.
[00:18:07 - 00:18:11] I can imagine that this is our pattern going here.
[00:18:11 - 00:18:17] How might we calculate with it this location here might buckle?
[00:18:17 - 00:18:37] What assumptions might we want to do? Can we use this equation?
[00:18:37 - 00:18:41] We've got 50-50, someone going to learn? Yes. Yeah, we can use that equation.
[00:18:41 - 00:18:45] Great. What would we need to update in this?
[00:18:45 - 00:18:49] So what else? See value change? Probably not, right? We can still assume it's a pen pen.
[00:18:49 - 00:18:58] Does pie change? No. Does E change? Well, if we're not changing our material, which we're not, no.
[00:18:58 - 00:19:01] Does I change? Yes.
[00:19:01 - 00:19:05] This is where we need to make it really clear what our assumption is.
[00:19:05 - 00:19:08] And then does L change? Yes.
[00:19:08 - 00:19:14] And so the easiest way for me to kind of close the loop on that would be that if I was doing this calculation,
[00:19:14 - 00:19:19] I would just assume that this is my loading condition, right?
[00:19:19 - 00:19:25] I've got one strip of aluminium and I've got some compressive force idolized going on it, right?
[00:19:25 - 00:19:33] So if I was to cut it here, my cross-section would just look kind of like a rough.
[00:19:33 - 00:19:37] Just look like one strip of aluminium ideally if it's just one strip of aluminium, right?
[00:19:37 - 00:19:43] And then our link would be whatever length from here to here.
[00:19:43 - 00:19:51] And so if you do have an extended flange, yeah, then that would be an appropriate calculation to do.
[00:19:51 - 00:20:03] What we will have seen in the past is that some people design this problem away by keeping this web as close to this pen as possible.
[00:20:03 - 00:20:09] And sometimes they might have been a cutout just for where the aluminium is all intersect with each other, right?
[00:20:09 - 00:20:12] I think I've shown an example of that previously.
[00:20:12 - 00:20:17] We can see that's exactly what this example one here has done, right?
[00:20:17 - 00:20:24] So the pen is very close there, then there's a cutout. Cool, you're unhappy.
[00:20:24 - 00:20:33] And so we can use a similar kind of train of thought to work out what might be happening if we have an ibeam.
[00:20:33 - 00:20:37] We're taking out some weight, right?
[00:20:37 - 00:20:44] So if we, I know I'm going to do it as a big square, maybe we've taken a dual two holes and they cut them between them.
[00:20:44 - 00:20:50] We can do the same idea where we could look at just in this area here where this is our length.
[00:20:50 - 00:20:57] What does our cross-section looking like and it might look more like this, right?
[00:20:57 - 00:21:04] And that's something that you guys can do and you have to decide what is appropriate to this sort of,
[00:21:04 - 00:21:13] when you have this kind of cross-section here, you're sort of inherently assuming that this geometry or this cross-section will stay constant as a force as a place.
[00:21:13 - 00:21:16] So that's why it's a constant as a force as applied to it, right?
[00:21:16 - 00:21:22] You can imagine that if this hole is really, really long, it might just have a lot of flexibility.
[00:21:22 - 00:21:26] It might actually be kind of acting as if it's just one by itself, right?
[00:21:26 - 00:21:31] Taking half the load or taking the full load, so that's your assumption to kind of make.
[00:21:31 - 00:21:34] Hopefully that kind of sheds light on.
[00:21:34 - 00:21:42] If you try and do these kind of design decisions, what approach you might use to be able to do that calculation of those sort of things, yeah?
[00:21:42 - 00:21:50] Any questions on any of that?
[00:21:50 - 00:21:57] So has anyone thought about adding those holes or what those sort of design details in the past?
[00:21:57 - 00:21:59] We haven't got up to that yet.
[00:21:59 - 00:22:00] Have a good up to it yet.
[00:22:00 - 00:22:07] We're just completely fine, but as I said, I'm really trying to front load this course just so that when you do get to it,
[00:22:07 - 00:22:09] you know that we've at least talked about it.
[00:22:09 - 00:22:14] You can kind of maybe make an asterisk to say a call if we have reduced cross-section in our compression members.
[00:22:14 - 00:22:18] Make sure to relook at this one here.
[00:22:18 - 00:22:19] Cool.
[00:22:19 - 00:22:22] Next another question that comes up is a centric loads.
[00:22:22 - 00:22:28] Can anyone tell me whether you would need to do any calculation of a centric loading?
[00:22:28 - 00:22:31] You guys can tell me the answer that I would normally say.
[00:22:31 - 00:22:35] It depends for you to for response, yeah, A plus.
[00:22:35 - 00:22:43] So it depends on whether the assumptions for oil or buckling are being completed or not, right?
[00:22:43 - 00:22:49] And so what do we think there?
[00:22:49 - 00:22:55] So if we have an I beam, the oil or buckling equation is quite, quite well-met,
[00:22:55 - 00:23:01] because our loading is going through the centroid of our member and its in simple compression, right?
[00:23:01 - 00:23:02] Axial compression.
[00:23:02 - 00:23:05] Because a few other assumptions there, but they're basically will meet.
[00:23:05 - 00:23:09] Like we have a homogenous material in the cross-section that's constant throughout, right?
[00:23:09 - 00:23:18] Cool. But if we have something like a T, T member, that's a classic kind of a centric buckling kind of case, right?
[00:23:18 - 00:23:22] So sometimes people think, oh, this would be great.
[00:23:22 - 00:23:24] I'll take some material away.
[00:23:24 - 00:23:28] And then, uh, as I say, that's great.
[00:23:28 - 00:23:31] I'll buckle where you took the material away.
[00:23:31 - 00:23:37] So we can see this one here is sort of a more, oh, that's wrong.
[00:23:37 - 00:23:38] That's me.
[00:23:38 - 00:23:42] So this is sort of a sort of an example of it.
[00:23:42 - 00:23:49] It's not the best example of it, though we can see that this has actually been a spuckle and this kind of localized area.
[00:23:49 - 00:23:53] So maybe that was actually just due to our, our changing cross-section rather than,
[00:23:53 - 00:23:58] this is certainly the fact that the loading might have been off-center.
[00:23:58 - 00:24:04] Often the ones that we see this kind of thing happen for, if we were to draw it.
[00:24:04 - 00:24:13] Can imagine that if in our ultra, um, over-emphasized kind of way, if this was our T member now,
[00:24:13 - 00:24:18] holds it right up here, and we can see that there would be some sort of distance.
[00:24:18 - 00:24:22] This is our centroid line between with the load as being a collider.
[00:24:22 - 00:24:28] So it's easy to think about that as being in the centric buckling load.
[00:24:28 - 00:24:32] That's another one just to hopefully make clear and it's one of those unfortunate things.
[00:24:32 - 00:24:37] Sort of depends on how complicated you make a design as to whether you'd need a checklist.
[00:24:37 - 00:24:41] If you just have an I-beam and oil of buckling's met, then that will be appropriate.
[00:24:41 - 00:24:47] So if you need to use the Poisson's ratio, then you can make that assumption.
[00:24:47 - 00:24:50] We can assume that local buckling's not going to occur.
[00:24:50 - 00:24:53] Does anyone know what local buckling is?
[00:24:53 - 00:25:00] It's where it just buckles either in the flange or the web kind of looks funny like a dance move or something there.
[00:25:00 - 00:25:11] But in the past, I've said localised buckling or local buckling, when I'm referring to these small, either in buckling at the end or buckling at a reduced section.
[00:25:11 - 00:25:14] So we can assume that local buckling's not going to occur.
[00:25:14 - 00:25:17] It's kind of the horrendous equation to look at.
[00:25:17 - 00:25:23] Yeah. Cool. Any questions about that?
[00:25:23 - 00:25:26] Just wanted to make sure it was nice and clear as we go forward.
[00:25:26 - 00:25:31] One day maybe we'll warm up.
[00:25:31 - 00:25:33] I'm just going to assume that it's because of you guys.
[00:25:33 - 00:25:35] I'm not sure what you don't.
[00:25:35 - 00:25:37] Not sure you don't know as to why.
[00:25:37 - 00:25:39] You don't have any questions.
[00:25:39 - 00:25:50] So I'll keep going and hopefully it's still, it's being useful going through these things probably preemptively before you have to think about them for real.
[00:25:50 - 00:25:52] So obviously here is we're going to have another option.
[00:25:52 - 00:25:54] The engineers can use the joint sheet middles.
[00:25:54 - 00:25:57] We can sketch the cross section of a riveted joint in possible failures.
[00:25:57 - 00:26:14] So if we were to quickly do that here, we can see that we might have, let's just draw two enders like this.
[00:26:14 - 00:26:21] And then normally there would be some sort of deformed area within our rivet.
[00:26:21 - 00:26:27] And then every big bead.
[00:26:27 - 00:26:35] So this is our cross section of our rivet.
[00:26:35 - 00:26:38] Probably look roughly something like this.
[00:26:38 - 00:26:45] So when you're putting the rivet into the hole, then you're obviously using the tool which pulls.
[00:26:45 - 00:26:50] And this kind of plug in and deforms the material.
[00:26:50 - 00:26:59] So what ways could this possibly fail?
[00:26:59 - 00:27:05] What was the one that we said before?
[00:27:05 - 00:27:06] Sure.
[00:27:06 - 00:27:14] What other stresses might be occurring?
[00:27:14 - 00:27:15] Earing, yep.
[00:27:15 - 00:27:21] So we got bearing on our rivet.
[00:27:21 - 00:27:34] And we got bearing base, material, and anything else.
[00:27:34 - 00:27:43] So we could also have tear out or like a tin-style stress.
[00:27:43 - 00:27:48] So this is more just like we're the ones going outwards versus at the end if you know what I mean.
[00:27:48 - 00:27:57] Yeah, I've seen a few nods there, but basically thinking about if this is our hole, tear out would be where it goes out this way, right?
[00:27:57 - 00:27:59] And that would be the area that we'd use.
[00:27:59 - 00:28:05] Whereas if we had just looking at the tin-style stress, we might be doing a cross section through here.
[00:28:05 - 00:28:08] And that's actually breaking either side of the rivet.
[00:28:08 - 00:28:09] Cool.
[00:28:09 - 00:28:16] So that's a pretty good indication of the way that they could fail.
[00:28:16 - 00:28:19] There's a video there for how to use the riveting tool.
[00:28:19 - 00:28:20] We don't need to go that there.
[00:28:20 - 00:28:23] And we kind of see that there.
[00:28:23 - 00:28:27] So we've got bearing and shearing the main ones.
[00:28:27 - 00:28:29] And that this is different to bolt connections.
[00:28:29 - 00:28:32] So bolt connections, because they have preload.
[00:28:32 - 00:28:39] There's kind of an assumption that the shear force is not really seen by the bolt unless the bolt is loose, right?
[00:28:39 - 00:28:40] Cool.
[00:28:40 - 00:28:43] So the shear strength is probably the main one that I'd be checking out.
[00:28:43 - 00:28:50] You might want to also look at the bearing stress, but shear is probably the most common one to look at.
[00:28:50 - 00:28:54] This force is typically given by the manufacturer.
[00:28:54 - 00:29:01] So if we click on, ooh, which one is it?
[00:29:01 - 00:29:03] That seems like the same link.
[00:29:03 - 00:29:05] See what we've got there.
[00:29:05 - 00:29:08] So I believe these are the ones that we have been given.
[00:29:08 - 00:29:10] And maybe it's that last link.
[00:29:10 - 00:29:12] Might be actually the data sheet for it, right?
[00:29:12 - 00:29:16] So you can see there's what I tried to draw.
[00:29:16 - 00:29:18] Hopefully it was kind of nice and clear.
[00:29:18 - 00:29:22] And then depending on what our rivet code was.
[00:29:22 - 00:29:25] So we might need a check here.
[00:29:25 - 00:29:27] Series 73.0.
[00:29:27 - 00:29:31] So maybe look at that.
[00:29:31 - 00:29:34] What are we at 3.2 millimeter?
[00:29:34 - 00:29:36] Check the length here.
[00:29:36 - 00:29:39] But that makes purpose 3.2.
[00:29:39 - 00:29:41] Crip range, max, purpose 2.2.
[00:29:41 - 00:29:44] So 3.2 millimeter, 3.2.
[00:29:44 - 00:29:46] I think I might be the ones here.
[00:29:46 - 00:29:49] We can see that doesn't really matter as long as we look at this.
[00:29:49 - 00:29:53] So we can see here we get a standard strength and share and intention
[00:29:53 - 00:29:59] of this many newtons or this much tinsel force, right?
[00:29:59 - 00:30:02] So that kind of answers that question of that kind of simple loading case
[00:30:02 - 00:30:06] where we had just our rivet being loaded and shared.
[00:30:06 - 00:30:12] You could then check whether the rivet will share based on this.
[00:30:12 - 00:30:14] Happy?
[00:30:14 - 00:30:18] Cool.
[00:30:18 - 00:30:22] Similarly, I guess we can just talk about this here.
[00:30:22 - 00:30:26] We can see that depending on what glue we've got,
[00:30:26 - 00:30:29] this is the best source that I could find.
[00:30:29 - 00:30:35] But I believe there is a lap share strength that's also been given.
[00:30:35 - 00:30:41] Obviously depending on how long you've given it to dry in it, what temperature
[00:30:41 - 00:30:43] and whether it's actually bonding.
[00:30:43 - 00:30:47] But again, we get a mere pescils for our lap share strength
[00:30:47 - 00:30:49] and there we can look at the iraq.
[00:30:49 - 00:30:51] So a lap share strength is just being one on the top,
[00:30:51 - 00:30:53] then with our pull in it.
[00:30:53 - 00:30:54] Cool.
[00:30:54 - 00:30:59] So similar kind of loading to what we saw previously,
[00:30:59 - 00:31:05] or we sketch previously.
[00:31:05 - 00:31:07] Any questions on that?
[00:31:07 - 00:31:10] I've sort of just tried to show you.
[00:31:10 - 00:31:13] You know, there might be one of the like,
[00:31:13 - 00:31:16] I'd say the second phase calculations that you do,
[00:31:16 - 00:31:19] start with our really look at whether you're a global buckling
[00:31:19 - 00:31:22] of the kind of global stresses that are occurring
[00:31:22 - 00:31:26] and you're bearing stresses at your pins are kind of all good.
[00:31:26 - 00:31:29] And then when it comes to some of your detailed design,
[00:31:29 - 00:31:33] depending on what kind of nuances you have about your particular design,
[00:31:33 - 00:31:36] there might be some subsequent calculations that are worth checking out.
[00:31:36 - 00:31:40] Yeah.
[00:31:40 - 00:31:45] So for just to make sure we're all on the same page again,
[00:31:45 - 00:31:50] we can definitely check out on our mark sheet,
[00:31:50 - 00:31:54] sort of specified in there what we're looking for.
[00:31:54 - 00:31:55] All right.
[00:31:55 - 00:31:58] So we can see free body diagrams,
[00:31:58 - 00:32:02] loads, stresses, which is sort of our general stresses,
[00:32:02 - 00:32:04] stress concentration factors.
[00:32:04 - 00:32:07] Then we've got our I values buckling and two planes,
[00:32:07 - 00:32:09] compressive stress it pins.
[00:32:09 - 00:32:12] Then we've got our rivet slash glue and weight calculations
[00:32:12 - 00:32:21] that you might want to do kind of subsequently, right?
[00:32:21 - 00:32:27] Any other questions while we're going through?
[00:32:27 - 00:32:30] Hopefully it's just like, oh, this is helpful when it's making sense.
[00:32:30 - 00:32:35] So in terms of adhesive's use, you'll see that nowadays there are a lot of different things
[00:32:35 - 00:32:37] that are manufactured using adheases.
[00:32:37 - 00:32:43] They provide a nice kind of clean solution when it comes to kind of heat distortion
[00:32:43 - 00:32:46] and speed when it comes to manufacturing stuff.
[00:32:46 - 00:32:50] And so you'll see that it can be used in a very broad range of applications
[00:32:50 - 00:32:53] from things on your car, obviously all the things in your phone
[00:32:53 - 00:32:55] are probably glued in there.
[00:32:55 - 00:33:03] And that kind of, yeah, can be a pain if you then have to try and re-blue things together.
[00:33:03 - 00:33:13] So what I've done, I think it is also under our tutorial slides is I have put this,
[00:33:13 - 00:33:21] on which call it, Notesbook from Derek Pons on the page for completeness
[00:33:21 - 00:33:30] for those who really want to get into the nitty gritty, I guess, of our adhesable designing with adhesive.
[00:33:30 - 00:33:38] So obviously this has a lot more detail than you might want to go over, but it will be kind of useful
[00:33:38 - 00:33:44] and we can cover some of the kind of main points within this and in some of the designs,
[00:33:44 - 00:33:50] sort of considerations that might be useful to consider.
[00:33:50 - 00:33:59] So just to do that generally, what we can do is kind of discuss more broadly
[00:33:59 - 00:34:08] about what are the benefits for using adhesives.
[00:34:08 - 00:34:19] So does anyone have any ideas about why using adhesives might be kind of useful for the manufacturing context?
[00:34:19 - 00:34:23] Lightweight?
[00:34:23 - 00:34:24] Yep.
[00:34:24 - 00:34:32] So in applications, i.e. aerospace, where you want things to be lighter,
[00:34:32 - 00:34:38] that might be one way or one way to make sure that that kind of design requirement is met.
[00:34:38 - 00:34:39] Cool?
[00:34:39 - 00:34:42] Yep.
[00:34:42 - 00:34:52] So we just say, yeah, all right, easy in quotation marks, but it's not like welding where you have to have a specialised welding ticket
[00:34:52 - 00:34:55] to do a certain kind of process.
[00:34:55 - 00:35:03] As long as you've got the right kind of manufacturing process and environment there, relatively easy to do, right?
[00:35:03 - 00:35:19] Cool? Cool? Yep. So we've got, so I guess what I'm going to put there is that it is a liquid to solid, right?
[00:35:19 - 00:35:35] So this means that it can spread easily, easily slash over areas.
[00:35:35 - 00:35:39] Cool?
[00:35:39 - 00:35:40] Yep.
[00:35:40 - 00:35:54] And also form slash contour to, or form slash con form maybe to contours.
[00:35:54 - 00:35:55] Cool?
[00:35:55 - 00:35:59] And what about temperature?
[00:35:59 - 00:36:01] Is it a hot process or a cold process?
[00:36:01 - 00:36:07] Cold process, right?
[00:36:07 - 00:36:15] So if you were to use a spot weld instead of gluing something, you would have this heat-deficted zone, you'll have temperature.
[00:36:15 - 00:36:19] You might have to wait for that part to cool down before you let people kind of touch it.
[00:36:19 - 00:36:23] So with glue, it's a cold process which is kind of useful.
[00:36:23 - 00:36:27] And I guess the other thing that we can include here is that it's kind of scalable, right?
[00:36:27 - 00:36:30] Yep.
[00:36:30 - 00:36:41] And it's cold and then I guess no part of the formation slash holds.
[00:36:41 - 00:36:42] Cool?
[00:36:42 - 00:36:44] Easy as.
[00:36:44 - 00:36:47] So I suppose it's pretty easily informed.
[00:36:47 - 00:36:58] So that means I guess what we're trying to say here is that I can access difficult areas, right?
[00:36:58 - 00:37:02] Cool.
[00:37:02 - 00:37:09] So we've got about 13 minutes.
[00:37:09 - 00:37:19] So what we'll see on this document is that Duke has done a very detailed job about what you would want to know.
[00:37:19 - 00:37:25] I suppose in terms of increases right from the history all the way through to advantages and disadvantages,
[00:37:25 - 00:37:28] which we've gone through a bunch of the advantages now.
[00:37:28 - 00:37:39] We can see here some of the disadvantages that it can be relatively low strength compared to some of the other material joining methods we can use.
[00:37:39 - 00:37:48] And it has four strength and peel and cleavage, which is often the way that they may fail right.
[00:37:48 - 00:37:53] So we can kind of look at a lap joint and sort of discuss that a little bit.
[00:37:53 - 00:38:00] But basically, these are the two kind of common failure modes that we might see.
[00:38:00 - 00:38:08] So before we go through any of that, what I also wanted to talk about is that for your assignment,
[00:38:08 - 00:38:15] making sure that you have good adhesion between your services and the glue,
[00:38:15 - 00:38:19] it's going to be one of the most important things that you do.
[00:38:19 - 00:38:28] And you also want to make sure that your services are clean and dust free and that you give yourself enough time to allow the glue to set.
[00:38:28 - 00:38:31] Otherwise, it won't be at its full strength.
[00:38:31 - 00:38:35] So what you can see here is we'll be using an epoxy, which is two parts.
[00:38:35 - 00:38:36] They're mixed.
[00:38:36 - 00:38:44] And then once they are mixed, the hard nut obviously makes the epoxy kind of set as long as it is at a temperature.
[00:38:44 - 00:38:48] So it's hot enough, right?
[00:38:48 - 00:38:53] If you see some more information there, which I'm not really going to go over.
[00:38:53 - 00:38:59] And I'm just going to go back over to here and to look at our surface preparation.
[00:38:59 - 00:39:08] So obviously, there are a number of ways in a manufacturing process that you would use to actually make sure that your surface is clean and free from.
[00:39:08 - 00:39:14] grease or similar that might stop it from bonding correctly.
[00:39:14 - 00:39:24] But in your case, what you might be able to do is if you ask the workshop nicely, they may have some alcohol that you can wipe on it.
[00:39:24 - 00:39:27] Then I'd also make sure that you adjust your surface roughness.
[00:39:27 - 00:39:35] So use this abrasion technique here to make sure that there is a good surface for your glue to adhere to.
[00:39:35 - 00:39:44] We don't really have any of these other processes available for your silent.
[00:39:44 - 00:39:59] So just to kind of expose closed that little intro, obviously that document is there if you want to go over it in more detail.
[00:39:59 - 00:40:04] But for the sake of time, I think we want to kind of keep things moving here.
[00:40:04 - 00:40:13] So the other thing that we can kind of look at is that if we did have a joint which was a lap joint.
[00:40:13 - 00:40:17] So we've got attention force pulling on each of these ends.
[00:40:17 - 00:40:25] And what we'll see is that if we have glue in the middle here, that because this is not centered,
[00:40:25 - 00:40:32] we'll get a high area of stress as the load is applied.
[00:40:32 - 00:40:40] Occuring at the corner, this may then promote peel failure causing the glue then kind of fail as it goes along.
[00:40:40 - 00:40:52] So you can imagine that as you start to pull kind of harder, the deformed shape may start looking kind of more like this.
[00:40:52 - 00:41:04] Especially if you don't have a rigid material and that these areas here is where your max stress would be occurring.
[00:41:04 - 00:41:20] So in terms of making a better design, if you had a lap joint for example, what way might you be able to improve that?
[00:41:20 - 00:41:24] Add another piece to make it symmetrical. Do you mean here?
[00:41:24 - 00:41:26] That would be one.
[00:41:26 - 00:41:31] Yeah, I need to look at top one for the other side.
[00:41:31 - 00:41:37] That's one here. Oh yeah, so you could make it like this at the other option, right?
[00:41:37 - 00:41:46] Cool. Those would all be better in call-up. Anything else that we could do?
[00:41:46 - 00:41:49] What about if I just said, oh, what if I just glue it like a butt joint like that?
[00:41:49 - 00:41:52] They'll keep it in line.
[00:41:52 - 00:41:54] What's the issue there?
[00:41:54 - 00:41:55] Surface area.
[00:41:55 - 00:41:56] Surface area.
[00:41:56 - 00:41:59] Low surface area.
[00:41:59 - 00:42:04] So similarly, even if you had a slight angle on it, same sort of issue you're at.
[00:42:04 - 00:42:12] Cool. And so what you'll see is that you can even go, as well as a step further and you can have,
[00:42:12 - 00:42:16] could have a member of the line. That's to really need it to be intention.
[00:42:16 - 00:42:20] If these were the two members that had.
[00:42:20 - 00:42:24] Cool. Just finally.
[00:42:24 - 00:42:26] I guess the other thing that we can think of.
[00:42:26 - 00:42:32] So what we'll see in there, I'll show it just at the end in case I kind of spilled the beans too early.
[00:42:32 - 00:42:36] But if this is, I don't know, a wall or something that we're flowing.
[00:42:36 - 00:42:38] Our, this owl bracket too.
[00:42:38 - 00:42:40] All right.
[00:42:40 - 00:42:42] We've got two options here.
[00:42:42 - 00:42:48] So this is grow.
[00:42:48 - 00:42:50] Yeah.
[00:42:50 - 00:42:51] Glue in here.
[00:42:51 - 00:42:56] And the load, quite at the end.
[00:42:56 - 00:42:59] Which one would be a better?
[00:42:59 - 00:43:04] So if this is A, this is B.
[00:43:04 - 00:43:14] Which one would be a smarter design if you had your adhesive and you were trying to stop it from peeling?
[00:43:14 - 00:43:19] So some people said A, some people said B.
[00:43:19 - 00:43:22] So if we think about what happens with A, if we pull here,
[00:43:22 - 00:43:25] then this thing might deflect a little bit downward.
[00:43:25 - 00:43:30] And the moment is going to push this into the surface, right?
[00:43:30 - 00:43:31] Which is pretty good.
[00:43:31 - 00:43:35] If we think about the same thing happening here, if this deflects in our moment,
[00:43:35 - 00:43:39] it's going to be trying to kind of fail in this point here.
[00:43:39 - 00:43:48] So this one here would be the one that is better in terms of understanding what your glue failure might be.
[00:43:48 - 00:43:51] And making sure that you don't have an unexpected kind of failure.
[00:43:51 - 00:43:52] Yeah.
[00:43:52 - 00:43:53] Cool.
[00:43:53 - 00:43:59] So as I said, this designing for adhesives has a lot of information.
[00:43:59 - 00:44:03] And it might also have a lot of stuff that's not strictly relevant to your assignment.
[00:44:03 - 00:44:09] But I think it is just useful for you guys to have a resource that you can use.
[00:44:09 - 00:44:11] To kind of help.
[00:44:11 - 00:44:14] Understand a little bit more about it if you see fit.
[00:44:14 - 00:44:19] But as I said, we've gone over the kind of laps you're stressed if you do want to do.
[00:44:19 - 00:44:24] And the calculation here and somewhere we were going over it just before.
[00:44:24 - 00:44:31] We can see that there are some ideas or some examples of good, poor, good and best design.
[00:44:31 - 00:44:37] So in these cases here, sometimes you'll have a variable cross-section,
[00:44:37 - 00:44:43] because it's actually the strain that's occurring that's sort of causing more failure at.
[00:44:43 - 00:44:49] So if we have more material here, then we don't have that information which then promotes the failure of that adhesive.
[00:44:49 - 00:44:57] It's good to have caught through.
[00:44:57 - 00:45:04] So I think we have time to go over a buckling calculation that's something that we could do.
[00:45:04 - 00:45:09] What we really want to do in this last five minutes is talk about these in conditions here.
[00:45:09 - 00:45:12] So can anyone guess what caused these members to fail?
[00:45:12 - 00:45:27] Buckling is a good idea, good answer, but it's not the correct answer.
[00:45:27 - 00:45:32] So you can see these two members here go together.
[00:45:32 - 00:45:33] There's maybe a hint.
[00:45:33 - 00:45:35] So this one here is normally attached to this.
[00:45:35 - 00:45:38] This might be going up this way if it was a right-angle triangle.
[00:45:38 - 00:45:44] Actually an example of it.
[00:45:44 - 00:45:45] Sort of here.
[00:45:45 - 00:45:53] You see that it's just the end, it seems to be bent.
[00:45:53 - 00:45:56] What do we think might have caused that?
[00:46:03 - 00:46:11] It's kind of similar or kind of goes in line with what are the assumptions of our all-wheeler buckling?
[00:46:11 - 00:46:20] You haven't got any other ideas why?
[00:46:20 - 00:46:24] What would cause it to do to do that?
[00:46:24 - 00:46:28] Definitely drew a diagram to imagine.
[00:46:28 - 00:46:34] So from the front view maybe what we're seeing is we've got one member going here.
[00:46:34 - 00:46:37] We've got another member going here.
[00:46:37 - 00:46:38] Hold there.
[00:46:38 - 00:46:41] That line.
[00:46:41 - 00:46:43] Cool.
[00:46:43 - 00:46:45] What would I force here?
[00:46:45 - 00:46:48] What might they look like on the front?
[00:46:48 - 00:46:51] Kind of might look like we've got a member going up that way.
[00:46:51 - 00:46:53] A member there.
[00:46:53 - 00:46:56] I don't know if that's been like a T-section or something.
[00:46:56 - 00:46:58] Does that look like in the diagram?
[00:46:58 - 00:47:00] Yep, they've got a T-section.
[00:47:00 - 00:47:02] So I've sort of drawn what it is.
[00:47:02 - 00:47:04] So based on that, just looking there.
[00:47:04 - 00:47:07] So we can see this is probably our alarm member.
[00:47:07 - 00:47:09] We've got our T-section, the zow.
[00:47:09 - 00:47:11] T-section is our member on the top.
[00:47:11 - 00:47:14] So what might cause that failure that we saw there?
[00:47:14 - 00:47:19] Put a pin coming through here.
[00:47:19 - 00:47:24] And this would be on our loaded attachment.
[00:47:24 - 00:47:31] That's why what happened when we loaded up.
[00:47:31 - 00:47:34] We see some arm movements.
[00:47:34 - 00:47:39] So this one here is having force basically going into the page
[00:47:39 - 00:47:41] where this one might be going out, right?
[00:47:41 - 00:47:45] Sort of like probably not the most clear arrow.
[00:47:45 - 00:47:46] So I've drawn there.
[00:47:46 - 00:47:49] But what we can see is probably from the top view
[00:47:49 - 00:47:53] that that occurs or that relates to from the top view
[00:47:53 - 00:47:57] a twisting moment into the page, right?
[00:47:57 - 00:47:59] Yep.
[00:47:59 - 00:48:03] And so that twisting is a real force.
[00:48:03 - 00:48:05] And if you don't have any resistance to that twisting,
[00:48:05 - 00:48:08] then the loaded attachment that we see here
[00:48:08 - 00:48:11] will just twist around, right?
[00:48:11 - 00:48:16] So how might we solve, how might we fix that kind of idea?
[00:48:16 - 00:48:28] Make it symmetrical.
[00:48:28 - 00:48:43] Make load transfer symmetrically.
[00:48:43 - 00:48:45] i.e.
[00:48:45 - 00:48:50] You know, if this was a fork, right?
[00:48:50 - 00:48:53] I remember in class we talked about adding forks with airwoven on.
[00:48:53 - 00:48:56] There was a fork and then we had our sicker member here.
[00:48:56 - 00:48:58] We had our pump going through there.
[00:48:58 - 00:49:01] Then we know that the load is going to be synced, right?
[00:49:01 - 00:49:03] So sometimes that's quite easy to do.
[00:49:03 - 00:49:06] We saw some of our bi-beams without notches in the middle.
[00:49:06 - 00:49:09] It's pretty obvious that this is going to be synced in the middle, right?
[00:49:09 - 00:49:11] Depending on what kind of end you choose
[00:49:11 - 00:49:13] or what kind of cross-section you choose,
[00:49:13 - 00:49:15] that's another thing that you might need to consider
[00:49:15 - 00:49:20] to make sure that the load is symmetrically placed, right?
[00:49:20 - 00:49:22] So there's the example happening in action.
[00:49:22 - 00:49:23] Another one where it's twisted.
[00:49:23 - 00:49:25] Another one where it's twisted in the same way
[00:49:25 - 00:49:27] where they've just put one beside the other.
[00:49:27 - 00:49:30] And it kind of twists.
[00:49:30 - 00:49:33] This one here has been mid-catastrophic failure
[00:49:33 - 00:49:36] and in previous years they still kind of keep happening.
[00:49:36 - 00:49:40] And so that's why you might end up using an end like this.
[00:49:40 - 00:49:43] So it's similar to what we saw there where the load is kind of synted.
[00:49:43 - 00:49:45] In other cases they've even gone stiff through there
[00:49:45 - 00:49:49] and they've kind of notched out one side more than the other.
[00:49:49 - 00:49:52] And while they've done that in reference to how much glue area
[00:49:52 - 00:49:54] what have they done by doing that?
[00:49:54 - 00:49:59] They would there to be a larger glue area
[00:49:59 - 00:50:01] for the force to be on, right?
[00:50:01 - 00:50:03] So there's a bigger area, then the stress will be less,
[00:50:03 - 00:50:06] which is kind of good news if you're a student
[00:50:06 - 00:50:09] wanting to go not to fail there, right?
[00:50:09 - 00:50:13] Cool, so we see there are a few kind of versions of that.
[00:50:13 - 00:50:15] There was seen there.
[00:50:15 - 00:50:18] And then this is an example I guess of just where glue
[00:50:18 - 00:50:23] has failed due to bad surface preparation.
[00:50:23 - 00:50:26] Cool, so that's pretty much everything that we wanted to go over.
[00:50:26 - 00:50:28] We've got any questions or we want to grab some strips
[00:50:28 - 00:50:38] so we hit the back.
[00:52:38 - 00:52:42] Okay, so we'll go over and like trust.
[00:52:42 - 00:52:44] Yeah, yeah, okay.
[00:52:44 - 00:52:46] So I can do that, but I'm like, oh, so weird.
[00:52:46 - 00:52:50] So we're then leaving them.
[00:52:50 - 00:52:52] Yeah.
[00:52:52 - 00:52:54] One more time.
[00:52:54 - 00:52:56] There you go.
[00:52:56 - 00:52:58] I'm leaving.
[00:52:58 - 00:53:00] We're leaving.
[00:53:00 - 00:53:02] We're leaving.
[00:53:02 - 00:53:04] Yeah, it is very interesting.
[00:53:04 - 00:53:06] Yeah, it is very interesting.
[00:53:06 - 00:53:08] So what did you just make?
[00:53:08 - 00:53:11] Someone said, like,
[00:53:11 - 00:53:14] I think it's like,
[00:53:14 - 00:53:15] it's not, it's not,
[00:53:15 - 00:53:17] it's just a bit of a heritage.
[00:53:17 - 00:53:18] Yeah, they said,
[00:53:18 - 00:53:19] they said,
[00:53:19 - 00:53:20] like,
[00:53:20 - 00:53:21] yeah,
[00:53:21 - 00:53:22] like,
[00:53:22 - 00:53:23] they said,
[00:53:23 - 00:53:25] just a little bit of stuff.
[00:53:25 - 00:53:26] So what did you just,
[00:53:26 - 00:53:27] I said,
[00:53:27 - 00:53:30] do you just make one part of your life?
[00:53:30 - 00:53:31] Yeah, it was,
[00:53:31 - 00:53:33] it was for one piece of it.
[00:53:34 - 00:53:35] How do you get back here?
[00:53:35 - 00:53:36] Yeah,
[00:53:36 - 00:53:37] yeah.
[00:53:37 - 00:53:40] Do you want to finish up with my
[00:53:41 - 00:53:43] A Pyj playing dance?
[00:53:43 - 00:53:44] I already figured it was very fancy
[00:53:44 - 00:53:46] I've already figured it was fancy.
[00:53:46 - 00:53:47] No, it's not.
[00:53:47 - 00:53:49] I wanna see the dance.
[00:53:49 - 00:53:51] What's your place in yours?
[00:53:51 - 00:53:52] Yes.
[00:53:52 - 00:53:53] Try it,
[00:53:53 - 00:53:55] try it
[00:53:55 - 00:53:57] You're right so…
[00:54:27 - 00:54:32] I can give a quick look at the food.
[00:54:32 - 00:54:33] Yeah.
[00:54:33 - 00:54:36] I think we can have a good food.
[00:54:36 - 00:54:38] It's really good.
[00:54:38 - 00:54:41] It's like you know, it's so good.
[00:54:41 - 00:54:43] It's really good.
[00:54:43 - 00:54:44] It's really good.
[00:54:44 - 00:54:45] It's really good.
[00:54:45 - 00:54:47] I don't know, it's really good.
[00:54:47 - 00:54:48] I don't know.
[00:54:48 - 00:54:49] I don't know.
[00:54:49 - 00:54:50] I don't know.
[00:54:50 - 00:54:51] Yeah.
[00:54:51 - 00:54:52] Can I get a good look at the food?
[00:54:52 - 00:54:53] Yeah.
[00:54:53 - 00:54:54] I don't know.
[00:54:54 - 00:54:55] How are you going?

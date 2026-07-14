# ENMT301-26W Lecture 12 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_12_audio_16k_mono_32k.mp3`
Source audio SHA-256: `d2f01117c8808b8b139133e788b76d6e1efeaf6b265da1c340bdf410341f0f8b`
Generated: 2026-06-06T05:21:37.947259+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:13 - 00:00:32] Alright, thanks everyone. I think we'll make a start there. Alright, thanks everyone. I think we'll make a start there
[00:00:33 - 00:00:37] Is this mic working all good?
[00:00:37 - 00:00:44] Sweet. Alright, so before I forget I've had two notices one was told to me twice, but
[00:00:45 - 00:00:49] The warm and tables are the warm and tables. Please don't use them as work benches
[00:00:50 - 00:00:52] So that's ticked off
[00:00:52 - 00:00:54] And the other one was
[00:00:55 - 00:01:02] For the material testing the house field team someone is again, I've been used by a 200 level lab in the mornings next week
[00:01:03 - 00:01:04] So if you're wanting to do your testing
[00:01:05 - 00:01:07] You'll need to do it in the afternoon's next week
[00:01:09 - 00:01:13] Probably summarize that in a post on the learn that I have like I try to only
[00:01:13 - 00:01:18] Maximum post once a week on learn because otherwise like you guys are just annoying again
[00:01:18 - 00:01:23] I'm gonna not gonna read it so my idea is that if I reduce my frequency then
[00:01:24 - 00:01:26] Hopefully they get more attention
[00:01:28 - 00:01:32] Cool, this is just in here because I had put it in
[00:01:33 - 00:01:36] Previously, but if you are interested I suppose on
[00:01:37 - 00:01:41] What people do in terms of research. This is one of my
[00:01:42 - 00:01:45] My earlier works, I guess quite weird thing to say, but
[00:01:46 - 00:01:51] Obviously my PhD was on understanding the strength abilities of people with teacher pleasure
[00:01:51 - 00:01:53] So if you want to try and
[00:01:53 - 00:01:55] help me improve my
[00:01:56 - 00:02:00] Research statistics i.e. Reads by scanning the link
[00:02:01 - 00:02:07] So it's greatly appreciated, but hopefully in the next kind of month one of my
[00:02:09 - 00:02:11] More recent publications might be coming out
[00:02:12 - 00:02:16] But it's often a headache to do so. Yeah
[00:02:17 - 00:02:20] Cool and so key slide from
[00:02:20 - 00:02:28] The last lecture I guess is just really trying to reiterate the fact that when you had in your hand calculations that they all
[00:02:28 - 00:02:30] Follow this really clear structure
[00:02:30 - 00:02:33] And that is something that the markers will be looking for right so
[00:02:35 - 00:02:42] One day you'll review someone else's calculations and when you review ones that haven't got any of these things like a title or a sketch and
[00:02:42 - 00:02:49] No interpretation and it's a complete minefield in terms of what is going on, right? So
[00:02:50 - 00:02:55] Notion down with the title is or any assumptions and any references to where you get those from
[00:02:56 - 00:03:01] I really important to make sure that your calculations can be interpreted by another engineer
[00:03:02 - 00:03:04] reasonably without any kind of a
[00:03:04 - 00:03:07] Prign or with that's most of exactly what you're doing in the context of what you're doing
[00:03:08 - 00:03:14] So I'd say err on the score err on the side of being more obvious
[00:03:15 - 00:03:16] rather than less
[00:03:16 - 00:03:19] Even if you think other sketch doesn't really help
[00:03:19 - 00:03:21] Include the sketch
[00:03:22 - 00:03:25] So see there there. I mean you can imagine that if we just had
[00:03:26 - 00:03:28] This button here
[00:03:29 - 00:03:32] Who knows what they'll be in calculating right could be the link for anything?
[00:03:33 - 00:03:38] Cool, so today we've got some time for some bearing questions that you might have already iterate one of the questions
[00:03:38 - 00:03:41] I was asked earlier and one that someone asked me about
[00:03:42 - 00:03:45] Off the other day we're gonna cover stress concentrations
[00:03:46 - 00:03:52] Be more of a recap. I guess I'm pretty sure you're aware of them before we can go over around what reportings are useful
[00:03:52 - 00:03:55] I believe it's a document on land as well
[00:03:56 - 00:03:58] And then we're gonna review some drawings
[00:03:59 - 00:04:01] starting by kind of
[00:04:01 - 00:04:02] roasting
[00:04:02 - 00:04:05] Adroying that I've made don't worry of
[00:04:06 - 00:04:08] I've been roasted by a lot worse people
[00:04:09 - 00:04:11] What I say is when you when you publish something
[00:04:11 - 00:04:15] I don't know if you guys realize this but like you do this work and then you like submit it to a journal
[00:04:15 - 00:04:18] And then they're like yeah your work sucks, but we'll accept it
[00:04:19 - 00:04:21] You know these slight changes
[00:04:21 - 00:04:24] So those are the ones that often hurt more rather than this one
[00:04:24 - 00:04:29] So don't worry you guys are will encourage you to be very explicit with what you think is wrong with it once we get to that
[00:04:31 - 00:04:37] So for any questions, I'm just gonna start and then maybe we can keep going from there
[00:04:37 - 00:04:39] So one of the questions that was asked was
[00:04:40 - 00:04:44] I George we have done our material testing and found that our young's modulus is
[00:04:44 - 00:04:46] Lullen expected
[00:04:46 - 00:04:50] I remember the exact quote of value something like for you a 50 giga Pascal's
[00:04:50 - 00:04:53] We think that this is wrong. What should we do? So
[00:04:54 - 00:04:57] It's an interesting question and my answer was
[00:04:58 - 00:05:04] Well if you use that value does that give you a more conservative or less conservative
[00:05:05 - 00:05:07] Estimate of your critical buckling force
[00:05:10 - 00:05:12] You and remember is
[00:05:12 - 00:05:16] Elastic modulus on the top of the equation for critical buckling or on the bottom
[00:05:17 - 00:05:19] So on the top right so if it's smaller is there going to be
[00:05:21 - 00:05:25] More conservative right so the smaller that means there's going to be a lower critical buckling force
[00:05:25 - 00:05:28] Estimate of which means you're estimating that you're thinking of buckle
[00:05:29 - 00:05:31] Earlier than it would if it was a high value, right?
[00:05:32 - 00:05:34] So one option would be just to go
[00:05:34 - 00:05:37] Okay, I'm gonna use it that you anyway. I know that it's probably low
[00:05:38 - 00:05:43] But it's conservative and I'm not expecting my thing to buckle anyway. I don't think you've got a
[00:05:44 - 00:05:49] Alone going through your completion unit. That's exactly the same as your critical buckling unit. Hopefully right
[00:05:50 - 00:05:53] Cool other option you know what I'm going to add is what other option might be
[00:05:57 - 00:06:00] Yep, so you could talk to other people and see what they got which I think
[00:06:02 - 00:06:04] Might sort of sort of lead on to next week
[00:06:04 - 00:06:09] If you've run filled out or enough people have filled out their material testing results on the learned
[00:06:10 - 00:06:12] Quiz choice quiz is you're unseen there
[00:06:13 - 00:06:16] So I'm nothing before they are then I'll be able to like show
[00:06:16 - 00:06:19] I found a histogram or like random curve fitted curve
[00:06:20 - 00:06:24] Their show is kind of what other people got so you can kind of see if if you're getting something whacky or not
[00:06:25 - 00:06:32] So why don't approach could be to look at that or I'd say quote that and then maybe update what you use based on that if you want to
[00:06:32 - 00:06:34] Obviously this
[00:06:34 - 00:06:36] You'd have to say why you're doing that and
[00:06:38 - 00:06:40] The other option
[00:06:40 - 00:06:46] Sort of similar would be just to say oh as you think that you know the less you're modulus of aluminium shouldn't really change
[00:06:47 - 00:06:52] So I'm gonna see what the range of typical range of published values for elastic modulus of four
[00:06:53 - 00:06:57] aluminium and I'll pick one of the middle or one on the edge that is
[00:06:57 - 00:06:59] more conservative
[00:06:59 - 00:07:02] This conservative in my very low bay that I got from my own testing
[00:07:04 - 00:07:06] heavy cool
[00:07:06 - 00:07:14] Then the other one that was asked which is sort of on a similar thing I've done some testing the dog bone didn't break where I wanted it to
[00:07:14 - 00:07:16] What should I do should I do more testing?
[00:07:17 - 00:07:19] Yeah, I'd probably recommend you do more testing
[00:07:20 - 00:07:21] Yeah
[00:07:21 - 00:07:27] So if you want to be you want to be in control of your results unless maybe you had like two then you're like
[00:07:27 - 00:07:29] I'm just super confident that those are right then
[00:07:30 - 00:07:37] You're the boss so don't let me tell you what to do but I think normally three is a good minimum number for
[00:07:38 - 00:07:40] getting consistent results
[00:07:40 - 00:07:44] So now of that the floor is yours what operating questions you guys have
[00:07:48 - 00:08:00] Yeah, yeah, so aluminium strips we can pick them up on Monday at the drop-in session or and choose there in the tutorial
[00:08:02 - 00:08:04] And then I might leave some
[00:08:05 - 00:08:10] For those who haven't collected them to be available click from the McEdman team
[00:08:11 - 00:08:15] But I didn't do them the first and since because there's like quite a lot of you in this line not there much space in the
[00:08:15 - 00:08:17] European area so yeah
[00:08:17 - 00:08:28] Oh, so you know easy. Well other questions do you guys have so
[00:08:29 - 00:08:31] One thing that's sort of helpful for me
[00:08:32 - 00:08:34] to know ideas
[00:08:36 - 00:08:39] We had this lovely diagram that was drawn on the fly
[00:08:40 - 00:08:42] Week ago maybe
[00:08:44 - 00:08:50] In terms of these sort of tasks how many people have done this material testing
[00:08:51 - 00:08:54] Sweet no good work thought that that was
[00:08:54 - 00:08:56] Sing a lot of people down there, so that's not surprising
[00:08:57 - 00:09:00] Cool so nice pat on the back if you've done that very proud
[00:09:01 - 00:09:04] How many people have done their initial design i?
[00:09:04 - 00:09:07] Chosen what kind of shape they're going to go for and done the free body diagram
[00:09:08 - 00:09:11] Cool instead of do that you've picked a target failure matter
[00:09:12 - 00:09:17] Awesome, so again if you haven't done that I'd recommend doing that ASAP like you know
[00:09:19 - 00:09:25] Soon as you get out of here do your free body diagrams, but um you guys have all the tools that you need to do that and then
[00:09:26 - 00:09:27] Is not really any benefit
[00:09:28 - 00:09:32] Benefit for delaying because like that's kind of one of those things that once you've decided
[00:09:32 - 00:09:34] Obviously you might be kind of optimizing our door on a picker
[00:09:35 - 00:09:39] This kind of I saw sleet triangle or a right angle triangle once you've made that decision
[00:09:40 - 00:09:44] That's not going to be the part of your design that you change and optimize to improve your strength to weight ratio, right?
[00:09:46 - 00:09:50] Cool and so then from there how many people have started designing some of the emitters
[00:09:52 - 00:09:58] Okay, so that's where we're sort of a couple people but seems like less people have
[00:09:58 - 00:10:00] Is it any particular reason why people have?
[00:10:02 - 00:10:04] Shied away from getting stuck into that element of things
[00:10:07 - 00:10:09] Time yeah, it's fair enough
[00:10:10 - 00:10:14] I know that I have been kind of giving you all the information now once which I think is
[00:10:15 - 00:10:16] I think it's a good thing
[00:10:16 - 00:10:18] I suppose at least to make sure that you guys know where you're going to go
[00:10:18 - 00:10:22] But what you need to do and obviously this is the last Friday afternoon tutorial that we have so
[00:10:23 - 00:10:28] We'll sort of slow down our pace going forward, but it will give you a bit of breathing room to do these kind of tasks
[00:10:29 - 00:10:31] But um the stress and the buckling I suppose
[00:10:32 - 00:10:40] Again things that you can at least do once and then you might iterate some of the shapes or look at different kind of cross-sections to use
[00:10:43 - 00:10:46] And I guess with that you would also think about some of those end
[00:10:47 - 00:10:50] Considerations for how the pen joints go together, right?
[00:10:51 - 00:10:56] It runs pretty clear that individual members are either to be single piece of aluminium or
[00:10:57 - 00:10:59] fully glued or fully rivetive
[00:11:00 - 00:11:02] Yep, and then in the corners
[00:11:02 - 00:11:05] We have those holes with his pens that will be supplied
[00:11:06 - 00:11:08] They'll pen each member together
[00:11:10 - 00:11:13] Sweet so make sure that you think about like with it pen goes
[00:11:14 - 00:11:16] I think I passed around a bunch of different
[00:11:16 - 00:11:23] Compression members, but obviously there's different ways that those pens can kind of interact with adjacent members and you want to make sure that they don't
[00:11:24 - 00:11:26] Clash or contact each other
[00:11:27 - 00:11:29] Yep
[00:11:29 - 00:11:34] So if there's any other questions or it's like are we haven't really come up with any what we've followed so far?
[00:11:44 - 00:11:46] Can you pop up?
[00:11:46 - 00:11:49] Sure
[00:11:49 - 00:11:52] Cool, so now we're going to get into our recap of stress concentrations
[00:11:53 - 00:11:55] do run sort of at least heard that term before
[00:11:56 - 00:11:59] Often happens in like weeks 6 and week 12 and exam period
[00:12:00 - 00:12:02] concentration of stress if one's not very
[00:12:03 - 00:12:08] Happy that everything's due at once and so that's why this course was sort of push everything
[00:12:08 - 00:12:11] Slowly head of the of the wave, right?
[00:12:12 - 00:12:14] But generally if we start with stress
[00:12:14 - 00:12:19] Stress is force over area and this is defined as our nominal stress formula, right?
[00:12:20 - 00:12:25] So it's used to calculate the average stress and it's kind of true as long as there's not any
[00:12:26 - 00:12:31] Sharp change in geometry nearby with a force that we're calculating is
[00:12:31 - 00:12:36] All whether it's exactly we or close to we're a load as applied, right?
[00:12:37 - 00:12:40] So one way that we can kind of visualize that I guess is that
[00:12:41 - 00:12:43] For example if we were doing
[00:12:43 - 00:12:45] I know actual tension in a
[00:12:46 - 00:12:48] cylinder or something
[00:12:49 - 00:12:51] We're kind of assuming that
[00:12:52 - 00:12:54] The stress that we're calculating
[00:12:56 - 00:12:58] This is our cylinder
[00:12:58 - 00:13:00] We're assuming that
[00:13:00 - 00:13:02] The stress is all
[00:13:03 - 00:13:05] Uniformed everywhere along
[00:13:06 - 00:13:10] Right good draw heats of areas, but our idea is that they're all the same high, right?
[00:13:11 - 00:13:14] And if we had if we had some
[00:13:17 - 00:13:20] I know a hole that was going through
[00:13:20 - 00:13:24] And this is where like a pin was or something then obviously the stress profile through here
[00:13:25 - 00:13:28] Would not be this nominal stress that we're seeing
[00:13:28 - 00:13:30] Yeah, there'd be like stress
[00:13:30 - 00:13:35] Raises near where the load is being applied or context stresses are the bare interest that you guys calculate
[00:13:36 - 00:13:38] Yep, cool. I know that this is all like
[00:13:39 - 00:13:41] Probably like yep, this is super obvious
[00:13:41 - 00:13:45] But we've so as good to start from a nicer simple sort of spot
[00:13:46 - 00:13:52] So as we've seen the sketch of for me for the form of that would be accurate assumed at the cross section of the members constant
[00:13:52 - 00:13:54] Or only changes very slowly
[00:13:54 - 00:13:56] This is not always going to be the case
[00:13:56 - 00:13:58] So when developing function designs
[00:13:58 - 00:14:05] It's inevitable that at some point the cross-section will have some amount of geometrical complexity
[00:14:07 - 00:14:12] So all differences in young smodulus which we can see in adhesive's part
[00:14:14 - 00:14:19] So obviously the adhesive has a different young smodulus to the material that is joining a lot of the time
[00:14:20 - 00:14:23] Cool, so you have a number of reasons why you might have geometric complexity
[00:14:24 - 00:14:26] This might be to perform a specific function
[00:14:28 - 00:14:30] Might be to perform multiple functions
[00:14:30 - 00:14:36] Be more lightweight or to fit the specifications of the design
[00:14:36 - 00:14:39] So we've got some examples here, but
[00:14:40 - 00:14:43] If you're designing a shaft, then obviously you need to have shoulders
[00:14:44 - 00:14:49] On your shaft to support the bearings which we'll see in our second kind of design assignment
[00:14:50 - 00:14:53] Sometimes you might want to perform multiple functions
[00:14:54 - 00:14:56] Which we'll see an example of
[00:14:57 - 00:14:59] Sometimes you might want it to be more lightweight
[00:14:59 - 00:15:02] I might be removing material which changes your geometry
[00:15:03 - 00:15:07] And then you might also just need it to fit specifications
[00:15:08 - 00:15:12] So space might be a consideration for your given kind of part
[00:15:14 - 00:15:17] Or you may want a longer life and lower cost
[00:15:17 - 00:15:21] Or another, it might be other kind of design requirements that
[00:15:22 - 00:15:24] Kind of impact the type of shape that you have
[00:15:25 - 00:15:27] So here we see a classic
[00:15:29 - 00:15:30] Everybody diagram of a shaft
[00:15:30 - 00:15:34] We can see that there are changes in where our shaft has shoulders
[00:15:35 - 00:15:40] So that we can kind of put machine elements and locate them using those parts in the geometry
[00:15:41 - 00:15:43] This one here is a nice, um, zero notices
[00:15:46 - 00:15:49] As a whistle rat, whistle that's like on the clip of an off spray pet
[00:15:49 - 00:15:52] Great pets, but again, multiple functions
[00:15:54 - 00:15:56] The clips are not naturally a whistle, but
[00:15:56 - 00:16:00] Some sneaky little design in there, but obviously that changes the cross-section
[00:16:01 - 00:16:02] This is a whistle
[00:16:02 - 00:16:02] Cool
[00:16:03 - 00:16:04] We might want it to have um
[00:16:05 - 00:16:11] To be more lightweight, so I believe this is a drink bottle holder on for a bike
[00:16:11 - 00:16:16] So you know, they've gone full carbon or something maybe so make sure that it's super lightweight
[00:16:17 - 00:16:19] Cool, so um
[00:16:19 - 00:16:24] Following this we can think about the definition of our stress concentrations
[00:16:25 - 00:16:29] As often there's this factor k which is used to describe
[00:16:30 - 00:16:36] What the maximum stresses or the ratio between what the maximum stresses and that nominal stress that we
[00:16:36 - 00:16:38] Kind of drew earlier right
[00:16:39 - 00:16:41] So k is defined as the ratio
[00:16:42 - 00:16:45] Between that maximum stress and the nominal stress
[00:16:45 - 00:16:48] Cool, so it's another classic kind of one where
[00:16:50 - 00:16:55] Sometimes people would don't use the same notation so in shiggly they have sigma zero used as
[00:16:56 - 00:16:58] The nominal stress rat
[00:16:58 - 00:17:03] If you look at British standards stresses yes and this whole nother thing sometimes just ah
[00:17:04 - 00:17:06] Whole nother thing right so
[00:17:07 - 00:17:07] Um
[00:17:07 - 00:17:13] Stress concentration we can sketch this as to what it might look like
[00:17:18 - 00:17:24] so um instead of having this kind of a nice cylindrical even
[00:17:24 - 00:17:27] um zone where this one here is our sigma
[00:17:28 - 00:17:29] nominal
[00:17:29 - 00:17:33] What we might end up having is if we drew
[00:17:34 - 00:17:38] Imagine that we have our tints arm in the maybe
[00:17:39 - 00:17:43] So something where there's a tints. I'll force
[00:17:45 - 00:17:47] I'm just gonna zoom out a little bit
[00:17:49 - 00:17:51] So if we had something like this
[00:17:51 - 00:17:54] Going if we had a hole and then we have a zone where there's no hole
[00:17:55 - 00:17:59] Our nominal stress away from any kind of stress concentration
[00:17:59 - 00:18:02] Would probably we could just draw it
[00:18:03 - 00:18:04] To be
[00:18:04 - 00:18:10] Basically all on the same line right sigma nominal
[00:18:10 - 00:18:12] Obviously this might have
[00:18:12 - 00:18:15] Some thickness to it if it's gonna be in area right
[00:18:15 - 00:18:18] But we're just gonna sketching a visualization
[00:18:19 - 00:18:21] Cool
[00:18:21 - 00:18:23] Then
[00:18:23 - 00:18:25] With a hole here is anyone who got new ideas
[00:18:25 - 00:18:28] We would be higher or be higher than edge of the hole
[00:18:28 - 00:18:33] Or at the edge of our kind of heart 50 50
[00:18:35 - 00:18:40] Edge of the hole right so we see some sort of stress profile where it kind of goes down
[00:18:42 - 00:18:46] Um like this right so it's lower at the end
[00:18:50 - 00:18:51] This one here
[00:18:51 - 00:18:53] with our
[00:18:53 - 00:18:53] Sigma max
[00:18:55 - 00:18:57] And then depending on how wide that part is
[00:18:59 - 00:19:00] This probably is gonna be
[00:19:00 - 00:19:03] Sigma non but obviously if it was not super wide
[00:19:03 - 00:19:07] Then it might be affected everywhere might be a crisscross
[00:19:07 - 00:19:09] Everywhere might be a
[00:19:10 - 00:19:15] Might have some stress level above the nominal stress that would have occurred right
[00:19:15 - 00:19:22] They were okay see I just flip on that quickly
[00:19:23 - 00:19:25] Didn't realize that wasn't on both
[00:19:26 - 00:19:28] So if you're watching this online
[00:19:28 - 00:19:31] Obviously there's gonna be a few people there to like end the mosh put at the moment like
[00:19:31 - 00:19:35] What if phone listening to this so shout out to those people
[00:19:36 - 00:19:38] Hope you have a good time
[00:19:38 - 00:19:39] Cool
[00:19:39 - 00:19:40] So
[00:19:40 - 00:19:45] We saw the sketch there and we can see an example of that there which is
[00:19:46 - 00:19:48] Sort of been explained
[00:19:48 - 00:19:50] What we had there
[00:19:50 - 00:19:51] Cool
[00:19:51 - 00:19:54] So obviously there's gonna be some thickness to your part to get that stress
[00:19:54 - 00:19:58] Based on the area right
[00:19:58 - 00:19:59] So
[00:20:00 - 00:20:03] What we see instead of kind of sketching that since we've already sketched that is that
[00:20:04 - 00:20:10] These kind of ratios or these kind of cave values are based on the geometry that you see right so
[00:20:11 - 00:20:14] The are a number of different stress concentration plots
[00:20:15 - 00:20:25] Which give engineers a way to kind of estimate what this cave a or stress intensity factor would be based on the kind of part and the geometry and the loading
[00:20:25 - 00:20:32] Has right so you'll see ones for portion or ones for bending or ones for tension more compression here
[00:20:33 - 00:20:37] So we can see and this one here. We've got our kind of variables of our
[00:20:38 - 00:20:40] Dealing the diameter of the hole
[00:20:40 - 00:20:42] W being the width of our part
[00:20:42 - 00:20:49] Then we've also got thickness and so we see here if our ratio of d of a w is really small
[00:20:50 - 00:20:53] Our cave a you gets there go right
[00:20:54 - 00:20:55] So
[00:20:55 - 00:20:58] D over w what does that mean? Well that means our hole is
[00:21:01 - 00:21:03] Very small compared to the width of our part
[00:21:03 - 00:21:05] Yeah
[00:21:05 - 00:21:10] So in my mind I think about it's like that's like cut sharp stress concentration
[00:21:10 - 00:21:17] Whereas if you go down this way d is getting bigger and w could be staying the same for example if the ratio is increasing
[00:21:17 - 00:21:20] So I'll say you've got a bigger hole in the same size part
[00:21:21 - 00:21:22] Yeah
[00:21:22 - 00:21:26] And so later on a few times like if we want to what we can see is
[00:21:26 - 00:21:28] interesting that sometimes
[00:21:29 - 00:21:34] Because the way that the stress formula will work based on the area that's available in the part
[00:21:35 - 00:21:37] It's not always clear cut what is worse
[00:21:40 - 00:21:44] In terms of like what we have a higher stress there a hole that's smaller or a hole that's bigger
[00:21:47 - 00:21:53] Yeah, so what I'm trying to say is like the other way that I could ask that obviously is a rhetorical question
[00:21:53 - 00:21:59] Or would have a higher stress if this part was 10 more wide and had a three millimeter hole
[00:22:00 - 00:22:02] Or a seven millimeter hole
[00:22:04 - 00:22:08] That's all right, and your mind folks be like I reckon it's this one without one
[00:22:08 - 00:22:13] Yeah, and then if we think about it what happens to the cave value if it's three
[00:22:14 - 00:22:24] It's bigger right, but then what's the area lift? It's also bigger
[00:22:25 - 00:22:27] so it's like
[00:22:27 - 00:22:32] Have to do some calculations to tell you the exact answer for the exact geometry is not always clear cut
[00:22:32 - 00:22:37] Cool, but the sharpness idea we can kind of keep and we agree that if there's a smaller hole
[00:22:37 - 00:22:39] You know that the cave area will be bigger up
[00:22:40 - 00:22:44] Awesome, so we see here's another plot. This one could be useful for
[00:22:45 - 00:22:50] Looking at the stress where your pins are so we can see the stress of a
[00:22:51 - 00:22:55] A loaded pin on a square kind of part and tension
[00:22:56 - 00:22:59] So for example if you were here, you know d over w was
[00:23:00 - 00:23:04] 0.25 you would have a cave value of five
[00:23:05 - 00:23:09] Which is pretty big right so the stress of the edge of the hole will be five times the normal stress
[00:23:11 - 00:23:12] Cool
[00:23:12 - 00:23:20] Yeah, the cave value itself. It's good Christian the question was
[00:23:21 - 00:23:24] Do these graphs ever depend on the material?
[00:23:25 - 00:23:27] The specific answer that question is no
[00:23:28 - 00:23:36] Right, but as we'll see one of my favorite pieces of written notes ever probably probably higher than my oil of buckling
[00:23:37 - 00:23:39] Banger of a line, but
[00:23:40 - 00:23:44] Will answer the weirdo material or type of material comes into it?
[00:23:45 - 00:23:49] Or do we want to just jump to the jump to the chase you tell me other minds
[00:23:50 - 00:23:55] Well, how far are we can we'll keep it in our mind though. Is this the same? Does this?
[00:23:57 - 00:23:59] Basically what your glasses does this hold for all
[00:24:01 - 00:24:08] Does this hold for all materials the technical answer is yes, but the mechanisms of what happens with different materials?
[00:24:09 - 00:24:12] Grays that answer so we'll cover that in a little bit, right?
[00:24:13 - 00:24:17] So you see here at the circuit point the stress is five times what you would have calculated
[00:24:18 - 00:24:23] If there was no stress razor or cave value that existed right
[00:24:24 - 00:24:27] It was just the cross-section without any kind of
[00:24:28 - 00:24:31] Hole or not true cross sign that raised the stress profile
[00:24:32 - 00:24:34] Cool so as you can see here there are
[00:24:35 - 00:24:40] Different kind of shapes that can be used and they can have different kind of profiles
[00:24:40 - 00:24:46] So similarly if you're using a notch other than a hole then you have the same kind of thing happening where the edge of the notch
[00:24:46 - 00:24:48] Is it increase in the stress that you see?
[00:24:51 - 00:24:52] Cool so
[00:24:52 - 00:24:54] in design
[00:24:54 - 00:24:59] Obviously having these stress concentrations is like not that good if you want your part to last a long time
[00:24:59 - 00:25:01] especially if you don't want to fail
[00:25:02 - 00:25:11] In ways like fatigue with is repeated loading and then these high stress areas be a typical kind of nucleation point for any kind of failure crack
[00:25:11 - 00:25:12] They're like a care
[00:25:12 - 00:25:14] And so what we do as designers is
[00:25:15 - 00:25:19] We try and avoid the sharpness of our
[00:25:20 - 00:25:25] Geometry such that the stress concentration is lower at those points
[00:25:26 - 00:25:27] Right
[00:25:27 - 00:25:32] So here's one example here another one that we could do as if we have just one notch
[00:25:33 - 00:25:35] we could actually
[00:25:35 - 00:25:37] Put some smaller notches next to it
[00:25:38 - 00:25:39] To kind of reduce that flow field
[00:25:39 - 00:25:41] And so sometimes this is something that doesn't really
[00:25:42 - 00:25:47] Make sense in people's brains. But the way that I think about it is by adding these two other notches
[00:25:47 - 00:25:52] It's almost like you've got one even bigger notch if you were the stress flow field, right?
[00:25:53 - 00:25:56] So instead of the flow kind of coming along and going
[00:25:57 - 00:26:04] And moving around this feature they kind of start moving away from these features earlier which kind of reduces
[00:26:05 - 00:26:09] The concentration of those stress or those force flow lines
[00:26:11 - 00:26:13] happy
[00:26:14 - 00:26:17] Cool, so there are a number of places you can get stress concentration plots are open to
[00:26:18 - 00:26:21] Shugley or Peterson stress concentrations book
[00:26:22 - 00:26:28] So here are some of the ones that you might want from Shugley. So you don't know she has to like go and look them up if you don't want to
[00:26:29 - 00:26:31] Obviously this one here is for bending
[00:26:31 - 00:26:35] But we've got a whole intention or a notch intention if you
[00:26:36 - 00:26:38] Outside of the bounds
[00:26:38 - 00:26:42] You can kind of extrapolate the data that is acceptable just make it clear to anyone
[00:26:43 - 00:26:45] What you did
[00:26:45 - 00:26:51] And I'd probably even like put these into your calculations if possible to kind of show how you got those values, right?
[00:26:53 - 00:26:55] So this is this other
[00:26:55 - 00:26:59] stress concentration book which has got more complex formulas and graphs
[00:27:00 - 00:27:03] I'd keep it simple for with me some people like on
[00:27:04 - 00:27:09] Not simple and that's up to you but two two options kind of for you
[00:27:10 - 00:27:15] Cool, so in terms of visualizing the stress concentrations there are different ways that this can be done
[00:27:16 - 00:27:21] One of the ways is by using polarized light in photo-allistic materials
[00:27:22 - 00:27:28] So back in the day when they used to use some perspicks if you actually did have like a polarized kind of
[00:27:28 - 00:27:36] Screen you could actually see these kind of stress concentrations might actually seem in the floor and are they clear kind of plastic parts
[00:27:37 - 00:27:40] Maybe we're any glasses or something, but you see all these kind of weird like colors
[00:27:40 - 00:27:46] Like rainbow colors weird is kind of this stress concentration happening and so you can see
[00:27:47 - 00:27:50] The difference as opposed by adding a small notch
[00:27:51 - 00:27:53] For a part that was in bending
[00:27:53 - 00:27:57] So this one here is showing that kind of stress concentration area
[00:27:58 - 00:28:02] So it's a pretty cool kind of plots or cool kind of visualizations
[00:28:03 - 00:28:07] Which I just kept in so that the people that let you go if you could have a fun time with this
[00:28:09 - 00:28:10] lecture
[00:28:10 - 00:28:13] Cool, so other way that we do it in the modern day
[00:28:13 - 00:28:17] I suppose is if you do if you are on a part it's normally pretty clear
[00:28:17 - 00:28:22] Where you're gonna get stress raises and where you're gonna see their stress contour plots kind of go
[00:28:22 - 00:28:26] Into those colors that represent high stress
[00:28:26 - 00:28:32] So here we see an example of a cricket bat simulation that I've done and no surprise that we see we're the
[00:28:33 - 00:28:37] little handle kind of attaches to our bat and there's a change in our geometry
[00:28:38 - 00:28:40] There is a large
[00:28:40 - 00:28:41] Stress
[00:28:41 - 00:28:45] Razor at that kind of point there so we get high stress at that region
[00:28:45 - 00:28:49] So obviously if you guys not saying you need to do for your assignment
[00:28:49 - 00:28:55] But if there is a course where we focus or you learn more about if you do a little bit of a net sheet
[00:28:55 - 00:28:57] And you need to be three one one but
[00:28:58 - 00:29:01] Indeed how if you sort of stuff is
[00:29:02 - 00:29:03] Net course
[00:29:03 - 00:29:06] So now coming to the question that we asked earlier. What is it?
[00:29:07 - 00:29:09] What difference does it make depending on what material you have?
[00:29:10 - 00:29:12] Well, we see full-broole materials
[00:29:13 - 00:29:14] Stress
[00:29:14 - 00:29:21] concentration can be indicative of failure, right? So the easy way to visualize this is like glass if you're
[00:29:22 - 00:29:30] If you're part for your element structure is made out of glass as soon as the stress in that part goes above they're kind of
[00:29:31 - 00:29:33] UTS or the yield stress
[00:29:33 - 00:29:37] That's gonna propagate pretty rapidly in the whole part's gonna break right
[00:29:38 - 00:29:40] Pretty easy to
[00:29:41 - 00:29:43] Think about here
[00:29:43 - 00:29:44] So
[00:29:44 - 00:29:47] Basically once failure begins it's all over
[00:29:47 - 00:29:49] But for ductile materials
[00:29:49 - 00:29:54] Right there's localized failure which results in permanent deformation
[00:29:54 - 00:29:56] Around the stress concentration
[00:29:57 - 00:29:59] And this distribution
[00:30:00 - 00:30:02] may redistribute the load
[00:30:03 - 00:30:07] Such that were redistribute the load such that the stress around that kind of feature
[00:30:08 - 00:30:11] may not necessarily be higher than
[00:30:11 - 00:30:13] What would cause the part to fail, right?
[00:30:13 - 00:30:15] So the propagation of the crack is kind of
[00:30:16 - 00:30:21] Is blocked or another way to think about is that our sharp stress concentration might be blunted
[00:30:22 - 00:30:25] Right? You want to have to have that?
[00:30:27 - 00:30:29] People are discussion on this and they're two tutorials
[00:30:29 - 00:30:31] Good, we're in the tutorials. So
[00:30:32 - 00:30:34] Last year I believe you run dead
[00:30:34 - 00:30:36] Inimme 202
[00:30:37 - 00:30:39] Sweet so
[00:30:40 - 00:30:44] One of my notes I've annotated it a couple times because I don't
[00:30:44 - 00:30:46] Get you course notes every year
[00:30:47 - 00:30:50] And what we see here is basically what we've got on
[00:30:50 - 00:30:54] The slot right again this year. I'm not saying oh look at your notes and work it out
[00:30:54 - 00:31:00] I'm just gonna sort of cut the chase and let us have no reason to sort of get this
[00:31:01 - 00:31:03] wrong, but I say so
[00:31:03 - 00:31:05] Full-bit of materials
[00:31:06 - 00:31:08] Our stress concentration factors
[00:31:10 - 00:31:15] If the stress is above our yield or our failure stress uts then it's indicative of failure
[00:31:15 - 00:31:22] However, for ductile materials, there will be localized failure that results in permanent definition around the stress concentration region
[00:31:23 - 00:31:25] This is one of my favorite lines here
[00:31:26 - 00:31:33] This relaxation may distribute the load below the yield strength around the stress concentration region
[00:31:34 - 00:31:37] Thus reducing the apparent stress concentration factor
[00:31:38 - 00:31:41] Not by one but to possibly
[00:31:41 - 00:31:43] Approximately
[00:31:43 - 00:31:44] 1.1
[00:31:44 - 00:31:48] So if there was ever a time that you're reading notes and you're like yo this person
[00:31:48 - 00:31:50] So confident
[00:31:50 - 00:31:54] It's not the time right
[00:31:55 - 00:31:57] But it is useful
[00:31:57 - 00:31:59] In the context of your assignment, right?
[00:31:59 - 00:32:01] So what we can see is
[00:32:01 - 00:32:06] This is what I do need your participation if we did our stress concentration in the
[00:32:07 - 00:32:10] Imagine that this was our membrane. We've got this holes in the middle
[00:32:13 - 00:32:15] If we designed this with a cave value of 2.3
[00:32:16 - 00:32:18] How confident will be that it would break
[00:32:20 - 00:32:22] At the load that we have planned it to break it
[00:32:26 - 00:32:30] So if I go through the sticks of the design process they are used
[00:32:31 - 00:32:33] I've done my free body diagrams
[00:32:33 - 00:32:37] I want it to break it 39 kg because I want to maximize my strength to weight ratio
[00:32:38 - 00:32:39] The force in the mimba
[00:32:39 - 00:32:43] I don't know which is going to pick a random number who was going to be 600 newtons and tension
[00:32:44 - 00:32:46] And then I used
[00:32:47 - 00:32:49] The cave values and the plots, right?
[00:32:50 - 00:32:53] To work out what kind of stress I need
[00:32:54 - 00:32:56] So I've done my material with this thing and I know
[00:32:56 - 00:32:58] Okay, I need to have
[00:32:59 - 00:33:03] It's failed at some amount of megapascals
[00:33:03 - 00:33:09] I plugged that into the equation and then kind of either by guessing and checking with what the cave
[00:33:09 - 00:33:12] A will be in the stress in the remaining nominal stress on the outside
[00:33:13 - 00:33:19] I can work out that the fairly stress should equal that if I use that cave A of 2.3
[00:33:21 - 00:33:33] What do we think might happen? Did everyone follow so far?
[00:33:34 - 00:33:36] So if we basically we do a calculation
[00:33:39 - 00:33:46] Do how assuming I don't know we could say
[00:33:48 - 00:33:50] Sick my UTS
[00:33:51 - 00:33:53] is approximately
[00:33:53 - 00:33:55] when failure
[00:33:59 - 00:34:04] Okay, obviously that's like an assumption
[00:34:05 - 00:34:08] You might think it's appropriate. You might use the max force
[00:34:08 - 00:34:12] Which would give you the UTS that you guys have done from your material system, right?
[00:34:13 - 00:34:14] So then if I say
[00:34:14 - 00:34:18] If I solve
[00:34:18 - 00:34:21] Sigma UTS equals k times
[00:34:23 - 00:34:27] Sigma none
[00:34:28 - 00:34:30] I know get
[00:34:34 - 00:34:47] Size, got someone should be here
[00:34:48 - 00:34:53] Who else is like yeah it works
[00:34:53 - 00:34:58] So with the cave A, okay, so we do this and I don't know the cave A means I've been 2.3
[00:34:59 - 00:35:03] So I don't know works out that 2.3 is our cave A
[00:35:03 - 00:35:05] For the whole size that we've got I don't know
[00:35:05 - 00:35:09] There was a 5 millimeter hole or something and I don't know what effect this was it sort of
[00:35:10 - 00:35:13] Low key irrelevant and this kind of general kind of example
[00:35:14 - 00:35:16] But if we use 2.3
[00:35:16 - 00:35:20] Does that do we think that our stress our actual stress in the part
[00:35:21 - 00:35:23] Will be
[00:35:23 - 00:35:28] The same as UTS for wall failure appear
[00:35:30 - 00:35:34] Well one person confidently shaking the head. No, everyone else is looking at me like
[00:35:35 - 00:35:37] George
[00:35:37 - 00:35:48] I don't know man
[00:35:48 - 00:35:50] so
[00:35:50 - 00:35:52] Yeah, I
[00:35:52 - 00:35:54] Think we're just
[00:35:54 - 00:36:00] Easiest way to do it. What does the note say might happen to the cave A?
[00:36:02 - 00:36:04] It decreases right
[00:36:04 - 00:36:07] So what is this apparent stress concentration
[00:36:08 - 00:36:11] Which is like using the same kind of process, right? So
[00:36:12 - 00:36:14] Using the same kind of plots
[00:36:14 - 00:36:17] Basically what it's saying is that the value whatever the value is or be reduced and
[00:36:18 - 00:36:21] That the amount that is reduced is quite hard to say
[00:36:21 - 00:36:26] Because you haven't given us any other information and the cave A is based on the geometry, right?
[00:36:28 - 00:36:47] Yeah, so
[00:36:48 - 00:36:49] What the comment was is if you look
[00:36:50 - 00:36:56] We all drove looked at the stress concentration plots for the one for a whole no matter kind of what our
[00:36:57 - 00:37:02] Whole sizes and never drops really below two if we assume that two is like an asymptote if this is hot
[00:37:02 - 00:37:05] Hollering only getting more and more horizontal so that makes me think that
[00:37:06 - 00:37:10] Regardless of your aim and might be quite close to 1.1
[00:37:11 - 00:37:14] Yeah, that's why you that's one way to rephrase what you've sort of said
[00:37:15 - 00:37:19] Well season some faces. They know that is not what I see at George. You're not quite me insane there
[00:37:25 - 00:37:30] Yeah, so the way that this if you think about how this could be tested, right is
[00:37:31 - 00:37:35] We work out we can compare so if we go back to our
[00:37:37 - 00:37:40] We go back to our definition of a stress concentration, right?
[00:37:41 - 00:37:43] What's the definition of the stress concentration?
[00:37:53 - 00:37:55] What is it k equals
[00:37:57 - 00:37:59] sigma max
[00:37:59 - 00:37:59] over
[00:37:59 - 00:38:01] sigma non-ra
[00:38:02 - 00:38:05] Cool so the other way that we could sort of see that is that sigma max
[00:38:06 - 00:38:09] Equals k times sigma non-ra
[00:38:12 - 00:38:18] Yeah, so if we drilled a certain hole size, right?
[00:38:22 - 00:38:24] So imagine we drilled
[00:38:24 - 00:38:30] Whatever whole size for our width of material they ended up being a value of say 2.4
[00:38:32 - 00:38:35] Well, we could do is drill that hole and we would know
[00:38:36 - 00:38:41] The nominal stress would just be the stress area if it was no k value
[00:38:42 - 00:38:47] So we could test it and see when it fails the failure might indicate what our max stresses
[00:38:47 - 00:38:51] We can compare that to what we expected to be if it didn't have this k value
[00:38:58 - 00:39:00] sort of like a
[00:39:01 - 00:39:04] One of those yeah, I'm not sure if I've
[00:39:06 - 00:39:08] Communicated clearly
[00:39:08 - 00:39:10] Sort of hard to mind read but
[00:39:13 - 00:39:18] What I'm sort of saying is okay, imagine that we assumed it having a k value of 2.3
[00:39:19 - 00:39:27] Yeah, so we thought that the stress will get to be equaling what our utuses if we went and test it and the force for example
[00:39:28 - 00:39:30] It breaks at twice
[00:39:30 - 00:39:32] the amount of force
[00:39:33 - 00:39:35] What does that mean our k value actually would be?
[00:39:39 - 00:39:42] Be half of this, right?
[00:39:42 - 00:39:44] Yeah, I think that's what you said
[00:39:45 - 00:39:50] Is that kind of make more sense and so then if you've done that you kind of know are
[00:39:53 - 00:39:55] That's probably what the k value is for this case but then
[00:39:56 - 00:40:00] You probably want to do the calculation chicken and that's the case
[00:40:02 - 00:40:06] Yeah, see some frowns for those who are frowning
[00:40:07 - 00:40:12] Is there a way that I has there another is there a question that you could ask or is there a do you want me to try and
[00:40:13 - 00:40:15] Describe it in another way
[00:40:20 - 00:40:22] So one question you might have is okay George
[00:40:23 - 00:40:28] What do you expect us to do or what approach would you recommend and obviously this is taken with a grain of?
[00:40:29 - 00:40:34] You can do whatever approach you want but I like to follow notes
[00:40:35 - 00:40:41] If it was me I would probably add a interest have a look at the k value for plot and go okay
[00:40:42 - 00:40:46] If I had a whole size of this that would mean a k value of this
[00:40:47 - 00:40:50] However, if I was to actually assume that the k value was
[00:40:51 - 00:40:53] 1.1
[00:40:54 - 00:40:57] What kind of stress area would I need to get the stress
[00:40:58 - 00:41:00] That's similar to the utiists that I think will make it fail
[00:41:02 - 00:41:04] Yeah
[00:41:04 - 00:41:07] Then I would choose that one
[00:41:07 - 00:41:15] Quite similar to how we saw on the other page and I'd work out whether the stress or the force that was applied to make it break
[00:41:15 - 00:41:18] How that compares to the force I would expect to be applied
[00:41:19 - 00:41:22] To make it break based on using a k value of 1.1
[00:41:23 - 00:41:25] Okay, the over 1.1 will be
[00:41:25 - 00:41:33] A lot closer than using whatever k value above two and then because obviously when you change that whole size what happens to your k value on the plots
[00:41:39 - 00:41:41] Well, I have instead of a k value if we change our whole size
[00:41:43 - 00:41:45] Changes the k value, right?
[00:41:45 - 00:41:47] And so this is where it frustrates students because
[00:41:48 - 00:41:50] The k value will still depend on the geometry
[00:41:52 - 00:41:56] And for some geometries if you'll weigh out here it may go close to 1
[00:41:57 - 00:41:59] k value may approach 1
[00:42:00 - 00:42:04] And if you'll weigh over here and you have a very small gimme with a small hole
[00:42:06 - 00:42:10] It might be closer to 1.15. I don't know it depends. I've seen a range
[00:42:11 - 00:42:18] Right, and so because of that my recommendation is to do a calculation assuming a k value that's
[00:42:18 - 00:42:22] In line with what our very confident notes say of approximately
[00:42:23 - 00:42:27] Apparently 1.1 and then I would do what kind of small scale test to kind of
[00:42:28 - 00:42:30] Verify the value that you got
[00:42:34 - 00:42:35] Yeah
[00:42:36 - 00:42:42] Yep, so as soon as how you guys have done dog bone tests
[00:42:42 - 00:42:47] The small scale test would be okay. I'm gonna create a cross-section that has
[00:42:47 - 00:42:50] You know what I might expect to see in my
[00:42:51 - 00:42:52] final design
[00:42:52 - 00:42:55] And I'm gonna test to see whether the k value that I've assumed
[00:42:56 - 00:43:00] Is the k value that is occurring or the apparent k value, right?
[00:43:01 - 00:43:04] So that's all good you do it on the team'someter
[00:43:05 - 00:43:08] Um, obviously you're not allowed to just like make your full scale one and test that
[00:43:09 - 00:43:11] This might help to refine your design
[00:43:13 - 00:43:15] Yep, and so with that obviously I'd make
[00:43:16 - 00:43:20] I'd take particular here in the construction of those test pieces and making sure that
[00:43:21 - 00:43:25] Whatever you make in your final design is made in a consistent way because if you're really rough and
[00:43:26 - 00:43:30] I know has some rough edges and you'll probably get a bit of variation in what you test
[00:43:31 - 00:43:37] Yeah, see varying levels of like I'm following versus
[00:43:39 - 00:43:41] I'm not feeling good
[00:43:42 - 00:43:45] Um, so if we go back to where we started
[00:43:46 - 00:43:51] For the flow diagram
[00:43:51 - 00:43:54] You'll see that I sort of have preemptively
[00:43:55 - 00:43:57] Structured
[00:43:57 - 00:43:59] What I would recommend tasks to do, right?
[00:44:00 - 00:44:02] So if this is like
[00:44:02 - 00:44:03] George I want to put my hand to sand
[00:44:03 - 00:44:07] You've told me about stress concentrations and I really wish you didn't all good
[00:44:08 - 00:44:11] Take a slow breather. Don't think about it for a week
[00:44:12 - 00:44:14] Half a week. I don't know do these other things first
[00:44:15 - 00:44:17] And then
[00:44:17 - 00:44:21] Once you know, okay, we're based on my stress concentration. I based on my sorry my geometry
[00:44:21 - 00:44:24] I know that this is the force in the member. That's not gonna change, right?
[00:44:25 - 00:44:27] Then you could go okay for this little element
[00:44:28 - 00:44:33] This is another kind of separate design task that I need to make sure that I'm confident that
[00:44:33 - 00:44:36] This part of the design will break when this load is met
[00:44:37 - 00:44:39] And you'll use that ratio between
[00:44:39 - 00:44:42] Sigma max equaling k sigma nom to do that
[00:44:44 - 00:44:46] Now just to check that you guys are following
[00:44:49 - 00:44:52] Can we have so say you do that experimental test, right?
[00:44:53 - 00:44:59] And your k value to make their equation work the k value comes out as 0.95
[00:45:00 - 00:45:05] That all good some people are shaking their head
[00:45:06 - 00:45:09] Why can't we have a k value over less than one?
[00:45:13 - 00:45:16] What does that what does that mean? What's another way to rephrase it? What does that mean?
[00:45:20 - 00:45:22] Yeah, what it means is
[00:45:22 - 00:45:25] You drill a hole it becomes stronger near the hole
[00:45:27 - 00:45:31] Right so like if that was true it'll be like let's go straight to nature
[00:45:31 - 00:45:35] Let's get this published where we become rich guys with salt that you can make all the things stronger
[00:45:35 - 00:45:40] Just drill hips or holes in them. Who be sweet right? So if that happens
[00:45:41 - 00:45:43] What do we think that that actually really means?
[00:45:46 - 00:45:52] Could be that you've done something wrong or it could just be experimental variation and realistically the k value is one
[00:45:53 - 00:45:58] Yeah, and so for some people as I said if you have a really wide member and a really big hole
[00:45:59 - 00:46:01] It could be very close to one
[00:46:03 - 00:46:06] Yeah, but the sharper your hole is the sharper the stress concentration
[00:46:06 - 00:46:10] The more likely it is to be closer or above 1.1
[00:46:10 - 00:46:14] But obviously that depends on your geometry and that's why I recommend
[00:46:15 - 00:46:21] Kind of utilizing this or doing this as a bit of a side quest as a task to do but not to sort of stress it out too much
[00:46:22 - 00:46:26] Yeah, because all of these ones up here you're just trying to show that your part won't fail
[00:46:35 - 00:46:37] If you have a hole or a notch
[00:46:37 - 00:46:42] We're happy that that's a stress concentration even if once you do your testing and you find this very close to one
[00:46:43 - 00:46:53] No, you can't have a slot slot is not a hole. I guess
[00:46:54 - 00:46:56] Yeah, so I said think we wrote it somewhere kind of
[00:46:58 - 00:47:01] Sort of clearly right, but stress concentration we've defined as a hole or a notch
[00:47:03 - 00:47:11] Yeah, and so a slot or a dog bone a slot is not a hole a dog bone is not a notch
[00:47:13 - 00:47:14] Yeah
[00:47:14 - 00:47:22] You run sort of happy happy with that. So if you off the back go, I'm gonna make this super gradual so that my K value is one
[00:47:23 - 00:47:28] No, but actually like okay, it's actually a hole that you've drilled with a drill bit. That's fair game. Yeah
[00:47:29 - 00:47:31] Similarly if it's a notch that has a
[00:47:32 - 00:47:35] Radius that's consistent. That's also fair game. Yeah
[00:47:36 - 00:47:42] Once I suppose I guess the notch one I guess the way I think about it is once you're not starts being
[00:47:43 - 00:47:46] less than
[00:47:46 - 00:47:49] Listen actually a width of a hole on saying and I was getting a bit sus
[00:47:50 - 00:47:54] Yeah, so ideally I'd say it's sort of one up to at least
[00:47:54 - 00:47:56] be sort of
[00:47:56 - 00:48:00] Like this and you'd show okay if it was a better material the K value would be this
[00:48:01 - 00:48:06] Because I have a ductile material. I'm gonna assume it's gonna be this and do my calculation based on that and then
[00:48:07 - 00:48:11] update it from there
[00:48:11 - 00:48:15] Cool, do you want feeling a little bit better about that than they were 10 minutes ago
[00:48:17 - 00:48:19] Some people are yeah, some people want
[00:48:23 - 00:48:28] You could just you could do whatever you want. That's easier to probably manufacture if you do
[00:48:29 - 00:48:33] Something that's a more gradual shape like a circular shape
[00:48:33 - 00:48:39] Yeah, you can make out a lot more consistently and you can could follow or get in there with the mary tape if you want to check the edges
[00:48:40 - 00:48:42] If you have a if you had like a V then sure but
[00:48:43 - 00:48:46] Again, I'm actually next saying that's consistent
[00:48:46 - 00:48:52] Is a consideration for you guys because it's a bit of a stretch up if you like make a test piece test in and you make something
[00:48:52 - 00:48:54] That's not the same and then
[00:48:54 - 00:48:55] It doesn't
[00:48:55 - 00:49:00] Operate the same in action
[00:49:00 - 00:49:04] Cool, you know the questions about that. I know I feel like with this year. We've been able to talk a lot of
[00:49:05 - 00:49:07] About a lot of things
[00:49:07 - 00:49:12] Before possibly you get your teeth sunken to them. So if questions do kind of pop up as you go
[00:49:13 - 00:49:16] Make sure that we kind of talk about that in either dropping session or in the
[00:49:16 - 00:49:18] Um
[00:49:18 - 00:49:20] Two toils as we go, right?
[00:49:22 - 00:49:26] Any questions about that is there a certain aspect that some people sort of are still not too sure about?
[00:49:27 - 00:49:38] Questions pop up
[00:49:39 - 00:49:44] So that's just concentrations
[00:49:46 - 00:49:48] Done and then hit we see here
[00:49:49 - 00:49:52] Jim low when you're designing machines and stuff, but you're not actually wanting it to fail
[00:49:53 - 00:49:58] So the fact that we you know if you use the bigger K-value that then would happen in reality
[00:49:59 - 00:50:01] That's not a bad thing
[00:50:01 - 00:50:06] Yeah, it's just that we're on this kind of weird Q&A case where we're like designing something to fail
[00:50:06 - 00:50:08] Which is like basically what engineers never really do
[00:50:10 - 00:50:15] Yeah, so we can see if we want to reduce stress concentrations we can make load piles
[00:50:16 - 00:50:21] Have a or make geometries have a broader kind of slower
[00:50:21 - 00:50:25] Change in geometry so we can avoid sharp corners or make
[00:50:26 - 00:50:36] List dramatic changes in our cross-section we can add features like holes or slits to the end of sharp edges to reduce their
[00:50:37 - 00:50:40] Reduce that radius that the stress field would see
[00:50:41 - 00:50:43] We would ideally not put
[00:50:45 - 00:50:52] Stress concentrations in areas or in designs that we'll have high cyclic loading because fatigue will become an issue
[00:50:52 - 00:50:54] And then we can say
[00:50:55 - 00:50:58] Remember that the stress concentrations are based on ratio
[00:50:59 - 00:51:02] So even if you have a hole that's five millimeter
[00:51:03 - 00:51:08] What that hole is a part of kind of matters in terms of that K-value. We see that in our plots
[00:51:09 - 00:51:11] Cool
[00:51:11 - 00:51:13] So we can talk about this
[00:51:15 - 00:51:18] Conceptually I think is the vibe that I'm getting at the moment
[00:51:19 - 00:51:22] So imagine that we have this load case here
[00:51:23 - 00:51:26] Actually, I think it would take it heaps to draw out
[00:51:27 - 00:51:30] But if we were to do in this case here
[00:51:30 - 00:51:35] So what is if we have D over W what is our D over W for this case here?
[00:51:37 - 00:51:38] 0.5
[00:51:38 - 00:51:42] Cool, so if we go up here we get a value I'm just going to crudely say 2.2, right?
[00:51:43 - 00:51:44] So
[00:51:44 - 00:51:46] Basically the question is
[00:51:47 - 00:51:49] What is the nominal stress?
[00:51:59 - 00:52:03] The people online they might be able to see what I'm writing or they might just see the screen but
[00:52:04 - 00:52:06] I'll show both of them soon
[00:52:06 - 00:52:10] We'll see that our K-value is 2.2
[00:52:11 - 00:52:12] Using
[00:52:12 - 00:52:16] Shugley plot, right
[00:52:16 - 00:52:21] Cool, so question is what is the nominal
[00:52:23 - 00:52:25] Stress
[00:52:25 - 00:52:27] At hole
[00:52:28 - 00:52:30] Can you want to tell me down
[00:52:30 - 00:52:31] What do we need to use?
[00:52:33 - 00:52:35] So we need to use the area here and here, right?
[00:52:39 - 00:52:40] Just but here would be
[00:52:42 - 00:52:43] I said this is nominal
[00:52:45 - 00:52:46] Stress
[00:52:46 - 00:52:49] Area at hole, right?
[00:52:51 - 00:52:54] So for this case here, what would that be?
[00:52:56 - 00:52:59] So the stress would equal force over the area which would equal
[00:53:00 - 00:53:03] A 10 kilonewton over
[00:53:04 - 00:53:08] Forward out area B
[00:53:08 - 00:53:10] Could do what they've done right
[00:53:12 - 00:53:16] W take away D times by t which would be
[00:53:16 - 00:53:18] 10 kilonewton over
[00:53:19 - 00:53:23] 0.2
[00:53:23 - 00:53:25] 2 take away 0.
[00:53:27 - 00:53:29] 0.1 times by 0.0
[00:53:33 - 00:53:34] Yeah
[00:53:34 - 00:53:35] That's all the meters
[00:53:36 - 00:53:37] Sorry it's not so tidy there
[00:53:39 - 00:53:41] Give it a good job
[00:53:41 - 00:53:43] Cool, so 7 non
[00:53:45 - 00:53:45] Say at
[00:53:47 - 00:53:48] Hole, you don't have a calculator
[00:53:52 - 00:53:53] Leave someone to do that
[00:53:54 - 00:53:55] And then if we do 2
[00:53:57 - 00:53:57] nominal
[00:53:59 - 00:53:59] Stress
[00:54:01 - 00:54:02] Away
[00:54:02 - 00:54:04] From hole
[00:54:07 - 00:54:09] In this case that's going to be like over here, right?
[00:54:11 - 00:54:13] There's our nominal
[00:54:13 - 00:54:15] Stress
[00:54:15 - 00:54:16] Area
[00:54:17 - 00:54:18] Away
[00:54:19 - 00:54:20] From
[00:54:20 - 00:54:22] To go
[00:54:22 - 00:54:26] This one we should get stress equals force over area
[00:54:26 - 00:54:29] Chicles 10 kilonewton over
[00:54:30 - 00:54:32] This case would just be 0.0
[00:54:33 - 00:54:38] 2 meters times by 0.0 0 2 meters right?
[00:54:40 - 00:54:41] Yeah
[00:54:42 - 00:54:43] Cool
[00:54:43 - 00:54:46] From 2
[00:54:46 - 00:54:46] 3
[00:54:47 - 00:54:48] Done a different notation
[00:54:49 - 00:54:51] What would our max stress be?
[00:55:13 - 00:55:14] Do you want to go on one of these guys here?
[00:55:18 - 00:55:19] 500
[00:55:19 - 00:55:20] Maybe our pass gals
[00:55:20 - 00:55:22] Cool
[00:55:27 - 00:55:28] This one I
[00:55:28 - 00:55:29] Yeah
[00:55:29 - 00:55:31] So they will now if we go 2.2 times by
[00:55:32 - 00:55:33] This one right
[00:55:34 - 00:55:38] Chicles what is that one point?
[00:55:43 - 00:55:44] Yeah
[00:55:44 - 00:55:45] Cool
[00:55:46 - 00:55:47] So we can see
[00:55:47 - 00:55:50] Sometimes what people think is that you would use this nominal stress
[00:55:51 - 00:55:52] To work out the max stress
[00:55:52 - 00:55:55] But obviously as I'm saying as we sort of discussed to an hour
[00:55:55 - 00:55:57] Comparing some different holes. What has the higher stress?
[00:55:58 - 00:56:03] Sometimes it might depend on what that K-value is and what the remaining area is right
[00:56:03 - 00:56:04] That's really clear that the
[00:56:05 - 00:56:10] Quasion for our stress concentration our max stress uses the nominal stress at that location
[00:56:12 - 00:56:14] Okay, cool
[00:56:14 - 00:56:19] Hopefully that just sort of clears it through
[00:56:20 - 00:56:23] So you can use that method or use that K-value in there to kind of verify
[00:56:24 - 00:56:27] Your assumptions and then these are some of the things that we
[00:56:28 - 00:56:30] Just need to remember
[00:56:31 - 00:56:33] So obviously this is an unusual kind of design
[00:56:34 - 00:56:36] Context this bit of the design
[00:56:37 - 00:56:45] So we see here you might use your use to be indicative of failure, but it's not really saying it's easy to calculate
[00:56:47 - 00:56:50] And if it aluminium sometimes they look a little bit more like this
[00:56:50 - 00:56:57] So that might be a bit better than what we see as a typical stress or load the fortune curve for steel
[00:57:00 - 00:57:04] So they don't stress concentration threat don't tell you about when fracture will go
[00:57:05 - 00:57:10] And that we recommend you find this out yourself to save you having to do
[00:57:11 - 00:57:14] It's the most most streamlined way to do it, right?
[00:57:20 - 00:57:23] In equations about our stress concentrations
[00:57:36 - 00:57:38] So the question is
[00:57:38 - 00:57:42] Is your particular context to your question like what kind of calculation you're thinking about?
[00:57:45 - 00:57:55] So for you said for your stress concentration do we assume it's brittle
[00:57:57 - 00:58:04] Or
[00:58:04 - 00:58:10] So I think what we've got to be clear here is that a K-value is not changing, but they're the apparent K-values
[00:58:10 - 00:58:14] I think about it is
[00:58:14 - 00:58:19] So it's not like you're going to see the information that you're talking about I think
[00:58:21 - 00:58:24] Yeah, so I guess where I was trying to think about it's like
[00:58:24 - 00:58:28] Are you talking about if you're trying to work out what the stress concentration is
[00:58:28 - 00:58:32] You know at a secondary hole and so you might want to just use the same
[00:58:33 - 00:58:35] Same assumption that you've used for the big one
[00:58:35 - 00:58:40] Yeah, that would be appropriate you might do a similar thing for the stress concentration at your pants, right?
[00:58:40 - 00:58:42] Because otherwise what your calculations will say is like
[00:58:43 - 00:58:45] If you assume that this bit was a brittle K-value
[00:58:45 - 00:58:47] It is going to break your pen before the hole
[00:58:47 - 00:58:50] Which doesn't really make any sense, right?
[00:58:51 - 00:58:54] You don't need to go and test all these other ones
[00:58:56 - 00:59:00] Yeah, any other questions about stress concentrations
[00:59:03 - 00:59:06] Cool, well, I'm going to keep things moving we can talk about these notes in a bit
[00:59:07 - 00:59:08] but
[00:59:09 - 00:59:11] Instead let's get into our drawings
[00:59:11 - 00:59:14] So obviously the drawings are going to be something that you're going to have to use
[00:59:14 - 00:59:19] Matter factor that'll be marked and then you use them to manufacture your part, right?
[00:59:19 - 00:59:25] So make sure you save your CAD files regularly like the worst thing ever when you're like about to submit it and
[00:59:27 - 00:59:32] It doesn't work. So these are all means that students in the past have kind of made to try and wyvern up my lectures
[00:59:34 - 00:59:36] So let's get right into the money
[00:59:36 - 00:59:38] Well for people next to you discuss
[00:59:40 - 00:59:42] How this could be improved
[01:00:12 - 01:00:16] So like you guys start making a list make sure you don't miss anything
[01:00:16 - 01:00:19] Right hopefully you guys can see it all good
[01:00:56 - 01:00:58] So you think it's guys
[01:01:00 - 01:01:03] What we got listen improvements if you are marking it or you had some bit of this
[01:01:03 - 01:01:09] What would you be unsurprised to hear from the marker as the lock could improve this your drawing?
[01:01:11 - 01:01:14] Too many dimensions, okay, so let's have a look at it
[01:01:15 - 01:01:16] so
[01:01:16 - 01:01:18] Just say number of
[01:01:18 - 01:01:20] dimensions so we said
[01:01:21 - 01:01:23] Too many
[01:01:23 - 01:01:25] See sometimes I know
[01:01:26 - 01:01:28] Do you know my work and I justify what I've done here?
[01:01:28 - 01:01:32] So any particular dimensions that you think are not needed
[01:01:34 - 01:01:43] Yeah, but water so it doesn't again, maybe it looks a bit flusses, but are there any dimensions?
[01:01:43 - 01:01:46] So I'll go back to you know point A
[01:01:46 - 01:01:50] Sometimes, you know I might surprise you maybe I've actually done a okay job
[01:01:50 - 01:01:51] I don't know
[01:01:52 - 01:01:55] So is there any dimension that you think is not needed?
[01:01:56 - 01:02:03] I think you know I'd agree with your your lack of comment of you know some of these orientations and where how they're looking look a little bit spicy
[01:02:11 - 01:02:13] Yeah, so what does the brackets mean?
[01:02:15 - 01:02:17] Yeah, it means like if you measure it
[01:02:18 - 01:02:20] It should be about this but like don't make it to this
[01:02:21 - 01:02:22] Yeah
[01:02:22 - 01:02:24] So it's like a useful for a machine as to check
[01:02:24 - 01:02:26] Cool
[01:02:26 - 01:02:28] If we look at these ones here
[01:02:28 - 01:02:32] 5.1 is telling us the distance between here 12.6 is telling us this between here
[01:02:32 - 01:02:35] So that's kind of fine. It's just trying to orientate with us
[01:02:36 - 01:02:39] Whatever this part is sort of hard to see what's actually going on
[01:02:39 - 01:02:42] But this here is a like cut out section
[01:02:42 - 01:02:47] Yeah, so that that reduced section is also 12.6 by 15.1
[01:02:47 - 01:02:49] possible minus 0.1 apparently and
[01:02:50 - 01:02:53] Then we've got some locations of holes
[01:02:54 - 01:02:58] Don't know if that one's actually located that one's not located
[01:02:59 - 01:03:03] Right cool. There's one real dusty dimension, but you are saying that go that way
[01:03:04 - 01:03:06] Yeah, the M6 length
[01:03:06 - 01:03:08] What does that mean so that one there?
[01:03:09 - 01:03:16] Probably not all good and terms of having two medium engines. I'd probably actually argue the opposite and say there's not enough
[01:03:17 - 01:03:20] So for example this part here and this part here
[01:03:20 - 01:03:22] This heats the stuff that's missing
[01:03:23 - 01:03:28] Yeah, I couldn't actually probably make that like how long is this thing in don't know what are these views here showing
[01:03:28 - 01:03:30] Don't know how thick is it?
[01:03:31 - 01:03:33] So I would actually
[01:03:34 - 01:03:36] say
[01:03:36 - 01:03:38] Not
[01:03:38 - 01:03:39] enough
[01:03:39 - 01:03:44] Yeah, but then M6 question mark would be one that I put there and then
[01:03:44 - 01:03:46] tidy
[01:03:46 - 01:03:48] tidy
[01:03:48 - 01:03:49] Turdiness
[01:03:49 - 01:03:51] So like the orientation
[01:03:53 - 01:03:55] Cool, all right. What else is bear with it?
[01:03:58 - 01:04:01] So two different parts on one page so you could say it's cluttered or
[01:04:02 - 01:04:09] You could argue that it just needs something else to make it a I think there are too many views so like
[01:04:10 - 01:04:15] I'll let you in in the secret this bit here was like wire cut so like
[01:04:16 - 01:04:18] the profile and stuff is
[01:04:18 - 01:04:21] Defined by a Dx file so like we're not making it too adoring
[01:04:21 - 01:04:22] um
[01:04:22 - 01:04:27] And then similarly like these holes are all kind of pre predefined on there
[01:04:27 - 01:04:28] I had to kind of make this be here by hand
[01:04:28 - 01:04:33] But these two views here are probably not giving much and like the fact that this is on there probably needs to get
[01:04:34 - 01:04:35] front way, right
[01:04:35 - 01:04:37] What would be more useful?
[01:04:37 - 01:04:42] Is this like missing between these? There's three different things here. What's missing on all of the views
[01:04:43 - 01:04:45] label graph so
[01:04:45 - 01:04:47] That would be another thing
[01:04:48 - 01:04:49] So add
[01:04:50 - 01:04:52] labels
[01:04:52 - 01:05:14] Remove used yep, so overall dimensions
[01:05:15 - 01:05:17] Missing on these two parts. Yeah
[01:05:18 - 01:05:20] That's good. Oh, right there down. What else?
[01:05:21 - 01:05:40] Go with specifications
[01:05:40 - 01:05:42] Right, so that is like
[01:05:42 - 01:05:47] Probably not too drawing standard so like technically could be okay, but like manufacturing notes are not uncommon
[01:05:48 - 01:05:53] Depending on the workplace. There's a sliding scale of what's acceptable to be not acceptable
[01:05:53 - 01:05:57] And at the end of the day if you want the part to be made right and you have to write a note
[01:05:57 - 01:06:02] Something to do that then that is all good probably would be more official if I added it as a note up here
[01:06:03 - 01:06:04] um
[01:06:04 - 01:06:06] But basically what this is saying is
[01:06:07 - 01:06:12] This here is actually two parts of 20 mil plate not one
[01:06:13 - 01:06:15] a 40 mil thing, right
[01:06:15 - 01:06:20] It's a little bit like cheeky engineering here where like you can't drill half a hole
[01:06:20 - 01:06:25] If I have a hole drill between two things that are how to get it then I can drill half a hole
[01:06:26 - 01:06:29] Right, so sorry didn't like me when I see it. I'm gonna drill half a hole
[01:06:30 - 01:06:32] So you can't do that
[01:06:34 - 01:06:39] Go yeah, manufacturing notes. Okay anything else we can just discuss it quickly. I guess yeah
[01:06:43 - 01:06:48] Yeah, the countersunk is well. Yeah, there should be a symbol that shows that it's been counter-sunkle
[01:06:48 - 01:06:53] Counter-board it's not really clear what the heat's going on there, but yeah, they were for catch-screw
[01:06:53 - 01:06:55] So they were counter-board
[01:06:55 - 01:06:57] Yeah, it's one of those things because I was the machineist
[01:06:58 - 01:07:02] I don't need to talk to the machineist because I am the machineist. I know what's going on right
[01:07:02 - 01:07:05] Obviously if I was to sit at this path. I would definitely
[01:07:06 - 01:07:11] deserve to sort of have the dummy spat at me and told to draw again. Yeah
[01:07:11 - 01:07:13] Cool, are the things that have been done?
[01:07:17 - 01:07:26] So obviously the material being material with incomplete finish being finished also incomplete, but in terms of actually having my initials a date
[01:07:27 - 01:07:29] and
[01:07:29 - 01:07:31] What was happening during covert is crazy?
[01:07:32 - 01:07:37] Drawing number and I like I'll use capital letters. There are some things that acceptable about that
[01:07:38 - 01:07:44] Cool, so for those of you you that might be going on I didn't really know exactly what I would
[01:07:44 - 01:07:52] Critique about the drawing. I've kind of made this little slide deck just like I'm trying to make it really clear
[01:07:53 - 01:07:57] That if you were thinking about it if you were marking your drawing these are the things that you should be looking for
[01:07:58 - 01:08:00] So to start with I did what any
[01:08:01 - 01:08:04] personal do before the world of AI was a thing and
[01:08:04 - 01:08:09] Google what is the purpose of an engineering drawing just to see if I actually gave a kind of okay result
[01:08:10 - 01:08:15] We can see here the goes of the drawing is to communicate your ideas to other people in the simplest form possible
[01:08:16 - 01:08:20] Your drawings don't need to be a laborer fancy. They just need to get your ideas across
[01:08:21 - 01:08:26] Which I think is a good kind of sentiment to take and it kind of goes to your comment there of like
[01:08:27 - 01:08:32] The file was in a cat turn into over. Do I add a comment and it typically doesn't follow the drawing standard or not?
[01:08:32 - 01:08:34] I'll definitely edit because clarity. I think
[01:08:35 - 01:08:38] Is more important at the end of the day
[01:08:39 - 01:08:43] So knowing this we can go through some basic things to get the most out of your drawings
[01:08:43 - 01:08:48] So the basics I describe as does it look like you have tried?
[01:08:50 - 01:08:55] Just because I think sometimes you might do these light late and night and quite last minute
[01:08:55 - 01:08:59] So is the title block filled out appropriately now if you want to go through that last
[01:09:00 - 01:09:04] I know knows that this might be something that you forget to do later you can edit
[01:09:05 - 01:09:09] Your kind of standard sheets such that things like your initials are already filled out
[01:09:10 - 01:09:14] So that if you forget to do you have already done it right you can see up your own sort of templates
[01:09:14 - 01:09:18] Have you used capital letters? That's another thing that the markers will be looking for
[01:09:19 - 01:09:24] Keeps an nice and tidying consistent because we teach you a certain drawing standard. That's what we kind of marking you
[01:09:25 - 01:09:29] a guest as the size slash layout of the drawing appropriate
[01:09:29 - 01:09:34] Do you have like one tiny part on a message drawing or vice versa
[01:09:34 - 01:09:38] or is it relatively well balanced for clarity right? So your drawings used
[01:09:38 - 01:09:39] They don't necessarily have to be the scale
[01:09:40 - 01:09:42] But if you do do them to the hidden scale you should probably
[01:09:43 - 01:09:47] Include that in your title or your label or you just need to explicitly say
[01:09:48 - 01:09:50] drawings not to scale
[01:09:50 - 01:09:57] Do the selected views show all the key details and functionality if they don't you might want to add another view
[01:09:57 - 01:10:00] Which will sort of be on some of our intermediate steps
[01:10:01 - 01:10:03] as the drawing uncluttered slash easy to read
[01:10:04 - 01:10:06] We know about that because my one
[01:10:06 - 01:10:08] Was not cluttered
[01:10:08 - 01:10:11] Was cluttered and was not easy to read right?
[01:10:12 - 01:10:18] Cool and then we have our intimate intermediate and a steps does it follow the drawing standard so
[01:10:19 - 01:10:24] If you want to go up above a level of just making a look like you've tried and you're filled in the basics
[01:10:24 - 01:10:26] We would
[01:10:26 - 01:10:28] Check that your taurances are appropriate
[01:10:29 - 01:10:34] Which might mean that there's a combination of specific and general taurances, right?
[01:10:34 - 01:10:36] So what do I mean when a
[01:10:36 - 01:10:39] What's an example of a specific taurance and a general tolerance?
[01:10:46 - 01:10:48] Let's say related back to your assignment
[01:10:49 - 01:10:51] Say you've got your tinge of your number, right?
[01:10:51 - 01:10:55] Or be a specific taurance on that and what would be a general tolerance on that?
[01:11:01 - 01:11:05] Yep, so
[01:11:05 - 01:11:07] Cool and so what values
[01:11:08 - 01:11:10] Could be used for that doesn't have to be exact but
[01:11:12 - 01:11:15] So for your stress concentration that would be a specific taurance, right?
[01:11:16 - 01:11:19] So you might say this whole is six millimeters plus or minus point one
[01:11:21 - 01:11:22] Yeah
[01:11:22 - 01:11:28] Because it'd be a bit of a nightmare if you said this whole is six millimeters plus or minus one millimeter
[01:11:29 - 01:11:34] It's like yeah, it's definitely gonna break it the same time regardless of if it's actually five mill or seven millimeter
[01:11:35 - 01:11:42] So that's why that one that's why you would have a specific tight tolerance on that kind of component, right?
[01:11:44 - 01:11:47] And then generally would be your general tolerance everywhere
[01:11:47 - 01:11:50] What do we say the next set called general tolerance would be for handmade structures like this?
[01:11:55 - 01:11:57] 0.5 mill possible minus, right?
[01:11:57 - 01:12:03] And this is where solar works kind of does your duty because I think the standard team played that a lot of people use has possible minus 0.1
[01:12:04 - 01:12:06] Right and so then the
[01:12:07 - 01:12:09] Tony like goes on like
[01:12:09 - 01:12:14] No, one of those like repeat those where everything person is like oh your tolerance is too small. I would
[01:12:14 - 01:12:18] Go out of business if I was trying to make these take me forever or something. Yeah
[01:12:18 - 01:12:23] So again, you know this preemptively. I'll change your general tolerance to probably plus minus point five
[01:12:23 - 01:12:25] I mean, you know that that's gonna be sorted
[01:12:26 - 01:12:29] Cool where is there gonna be a specific tolerance that is bigger
[01:12:30 - 01:12:34] Then your general tolerance so think it back to our teaching member again
[01:12:35 - 01:12:38] What else is gonna be on that guaranteed to be on that?
[01:12:42 - 01:12:44] How do our different members connect to each other?
[01:12:47 - 01:12:48] Pens, right?
[01:12:49 - 01:12:52] So what would the distance between those pins need to be plus or minus?
[01:12:52 - 01:12:54] Imagine it's our students our teach me because
[01:12:55 - 01:12:57] that could be a
[01:12:57 - 01:13:01] diagonal member answer
[01:13:01 - 01:13:04] The tolerance I'd have to kind of do some geometry and work out. I'll be acceptable
[01:13:04 - 01:13:09] But imagine if it was our vertical member or the tolerance between those two pen holes be
[01:13:11 - 01:13:15] Also minus three millimeters, right? It's 285 plus minus three millimeter, right?
[01:13:16 - 01:13:21] So again, if you just left it as a general tolerance you could make it in a cookie to 86
[01:13:22 - 01:13:25] Technically there is within the simple limits of the assignment
[01:13:26 - 01:13:29] but the workshop technicians could go oh no, no, this hasn't been made
[01:13:30 - 01:13:32] To what you have done in drawings, right?
[01:13:33 - 01:13:39] Oops, so I guess that these are examples where I've noticed down and check that you do that before submitting your drawing
[01:13:40 - 01:13:42] Do your dimensions follow the drawing standard?
[01:13:42 - 01:13:44] Obviously if you have something like Msec to the length
[01:13:45 - 01:13:48] It wouldn't be following the drawings standard. Don't have to have millimeter after each of them
[01:13:49 - 01:13:52] The way that you show those tolerances as well. There's a number of acceptable ways
[01:13:53 - 01:14:00] Again, does the review show will key details and functionality? Do you need a section view or have you included a section view if it's required?
[01:14:01 - 01:14:05] Or some other detailed view of the dimensions are quite hard to see
[01:14:07 - 01:14:09] So there are no where access the drawing standard
[01:14:10 - 01:14:14] Well, I'm pretty sure I put on learn as well
[01:14:15 - 01:14:17] If you have issues and you want to find out that we can cool
[01:14:18 - 01:14:20] Here's a little fun limit I've clicked on
[01:14:20 - 01:14:26] Or worked out so another thing that people I think have struggled with in the past is the idea that
[01:14:27 - 01:14:31] It's great talking about the fact that these specific or general times exist
[01:14:31 - 01:14:34] But I don't really know what is an appropriate
[01:14:35 - 01:14:37] Specifically, they go geomile tyrants for my partner
[01:14:38 - 01:14:42] So the way that I think about it is you know if you have a length that's 5 millimeter
[01:14:43 - 01:14:49] 5 millimeter plus or minus 1 is quite a lot of variation compared to those 500 millimeter plus or minus 1
[01:14:50 - 01:14:53] That's a very small amount of variation, right?
[01:14:53 - 01:14:55] So what you see is that there are
[01:14:56 - 01:15:02] There is an ISO standard for these linear dimensions that help you to work out what is an appropriate kind of size
[01:15:03 - 01:15:06] For your kind of tolerances and this is a tool
[01:15:07 - 01:15:09] There you could use for other assignments, right?
[01:15:10 - 01:15:16] So we've got these different tolerance classes fine medium course and very course and then for different lengths
[01:15:17 - 01:15:19] There are different acceptable tolerances
[01:15:20 - 01:15:22] So instead of just having one geomile tyrants
[01:15:22 - 01:15:26] You imagine that if your part has a range of different lengths i.e
[01:15:27 - 01:15:31] Ones that are different on these ones. Oh, you know, you're probably gonna be these four lines here
[01:15:32 - 01:15:34] You can see that
[01:15:34 - 01:15:36] For some of the smaller dimensions
[01:15:36 - 01:15:38] It'll be appropriate to have plus and minus point two
[01:15:39 - 01:15:42] Up to even plus minus point eight for some of your bigger ones out
[01:15:44 - 01:15:51] So this is just I guess a PSA. We'll have for your reference, but if you really wanted to you could
[01:15:53 - 01:15:57] You know have a table that's similar to this that says for dimensions from this to this
[01:15:57 - 01:16:01] This is the tolerance for the new dimensions of this this this is the tolerance
[01:16:02 - 01:16:04] Don't necessarily have to do that for this assignment
[01:16:04 - 01:16:07] But in other things that might be something that you see sometimes
[01:16:07 - 01:16:11] There'll be a table like that at the bottom of the drawing to make it kind of clear
[01:16:13 - 01:16:19] Cool so similar thing has been already included in the frequently asked questions and then you can see there are
[01:16:19 - 01:16:24] Similar tables that exist for your radii for your angular dimensions
[01:16:25 - 01:16:27] straightness and flatness and
[01:16:27 - 01:16:29] except your
[01:16:29 - 01:16:31] First ones probably the most useful
[01:16:31 - 01:16:33] Cool and then while we're talking about
[01:16:34 - 01:16:38] Tolerance is this will be something that kind of is more relevant when it comes to your bearing housing
[01:16:39 - 01:16:41] but the idea of engineering fits and
[01:16:42 - 01:16:46] hopefully the words
[01:16:46 - 01:16:48] interference fit or
[01:16:49 - 01:16:51] Clearance fit or
[01:16:52 - 01:17:03] Transition fit ring about questions. I would impress only specify for the buttons as I say
[01:17:03 - 01:17:09] I'm just gonna show it now so that we only talk about engineering fits for the bearing housing where you have your bearing in your shaft
[01:17:09 - 01:17:15] That you would define what kind of fit you want to make sure that you can get your bearing onto your shaft
[01:17:16 - 01:17:19] All your bearing into the bearing housing and that it's not like
[01:17:20 - 01:17:23] Interference and you can't get it on unless that's what you really want
[01:17:24 - 01:17:27] Yeah, so I'm not gonna talk about this in much more detail
[01:17:27 - 01:17:32] I assume that you at least have heard of the types of fits and then the fact that they are
[01:17:32 - 01:17:36] definitions for what types of subcategories that
[01:17:37 - 01:17:41] Within that so you know if there are clearance fits that a tighter
[01:17:42 - 01:17:44] or lucid depending on the application and again
[01:17:44 - 01:17:46] This is a nice
[01:17:46 - 01:17:51] Place to start if you weren't sure what would be an appropriate engineering fit
[01:17:52 - 01:17:56] So you might do this if this might be part of your finding your project next year or something something like that
[01:17:56 - 01:17:58] They might be a resource that's helpful
[01:18:01 - 01:18:01] Cool
[01:18:02 - 01:18:04] So with that
[01:18:04 - 01:18:06] I have another one
[01:18:15 - 01:18:17] So this one is a real student example
[01:18:20 - 01:18:25] So what I can probably zoom in the moment. I could put slightly easier
[01:18:28 - 01:18:29] What is?
[01:18:29 - 01:18:31] We can say what it's good. What is bad make a list?
[01:18:32 - 01:19:54] I'm happy to start the list
[01:19:54 - 01:19:58] Yeah, okay, so
[01:19:59 - 01:20:01] What's good? What's not so good?
[01:20:01 - 01:20:03] I
[01:20:03 - 01:20:08] Got the red can now
[01:20:08 - 01:20:11] Are you just red for bad? Look can be for good so then the green can?
[01:20:17 - 01:20:20] Yeah, it does repeat it a lot. Is it consistent?
[01:20:22 - 01:20:23] No
[01:20:23 - 01:20:26] So like it's over defined as like the technical term, right?
[01:20:26 - 01:20:31] So what happens here is like 50 mil is like plus or minus 0.1, right?
[01:20:32 - 01:20:34] That's like each of these are plus or minus 0.1
[01:20:34 - 01:20:37] Which means we've got one two three four five
[01:20:38 - 01:20:41] six seven so we're actually plus or minus
[01:20:41 - 01:20:43] 0.7
[01:20:43 - 01:20:47] If we add all those little ones up, right change dimensioning as well. It's called
[01:20:47 - 01:20:53] Yeah, but then this is saying that needs to be 260 plus or minus 0.1 which like doesn't
[01:20:54 - 01:20:56] It doesn't fit right
[01:20:56 - 01:21:06] So again, Tony would be like which one is it? Or it'd be a simple fix. How can we fix it?
[01:21:11 - 01:21:12] Uh
[01:21:12 - 01:21:18] It's to do with this. I don't think taking the point. I would be appropriate unless it was like another
[01:21:19 - 01:21:21] Put a bracket around around right so it's saying
[01:21:21 - 01:21:27] All bracket around some other ones. Yeah, if we put a bracket around one then it means like yeah
[01:21:28 - 01:21:31] This is what it should be when you measure it, but like don't make it to this
[01:21:32 - 01:21:34] So it's dimensions over defined
[01:21:36 - 01:21:38] Right. Well, how do we have?
[01:21:42 - 01:21:51] I've done some other thing that I did that was bad. We go through the basics. What all the basic things that we're looking for
[01:21:51 - 01:22:04] I do that is no distance
[01:22:05 - 01:22:07] You know missing this one. Yeah
[01:22:10 - 01:22:12] Yep, cool. What else?
[01:22:14 - 01:22:16] Yep, so
[01:22:16 - 01:22:18] You know, this should really say front
[01:22:19 - 01:22:23] And then this should say top right now from that
[01:22:23 - 01:22:26] We remember in 101 like it was yesterday
[01:22:26 - 01:22:29] When we look at it. I submit review this one here
[01:22:31 - 01:22:34] This is our kind of our bounding box around around
[01:22:35 - 01:22:37] Which one of those views
[01:22:37 - 01:22:43] Is the front like oh?
[01:22:43 - 01:22:48] Which face would be the front this one this one or this one one two or three
[01:22:49 - 01:22:52] One right so looking from this view should be that
[01:22:53 - 01:22:55] So also the
[01:22:55 - 01:22:57] Orthographic it's like a convention, right?
[01:22:59 - 01:23:01] Convention
[01:23:01 - 01:23:03] Assume
[01:23:03 - 01:23:05] So ISO
[01:23:05 - 01:23:09] Orthographic right or vice versa, right this here is our front officially, right?
[01:23:10 - 01:23:12] So really it should be looking
[01:23:12 - 01:23:14] Like this way
[01:23:14 - 01:23:21] Then coming out
[01:23:21 - 01:23:31] What else so
[01:23:32 - 01:23:38] If we look at our title block is it completely filled out the date is there good project
[01:23:39 - 01:23:42] Good drawing number bad
[01:23:43 - 01:23:47] Not number right revisions fine
[01:23:49 - 01:23:52] Part name
[01:23:52 - 01:23:55] Average could be better. It's not the worst I've seen
[01:23:56 - 01:23:59] Yeah, and then again these things here could also be
[01:24:00 - 01:24:04] Areas to improve right
[01:24:04 - 01:24:06] Cool are our
[01:24:07 - 01:24:13] Tolerance is okay
[01:24:13 - 01:24:15] So
[01:24:15 - 01:24:19] updated
[01:24:19 - 01:24:25] Poetry is i e
[01:24:25 - 01:24:27] General
[01:24:27 - 01:24:28] Is plus or minus 0.5
[01:24:29 - 01:24:33] So this one here. It's sort of a weird thing. It's the weird the oven i-beam
[01:24:33 - 01:24:36] That's why it doesn't have the holes for the pens
[01:24:37 - 01:24:38] Cool
[01:24:38 - 01:24:50] What about size has the size look good
[01:24:56 - 01:24:58] And then generally I think how the dimensions
[01:24:59 - 01:25:01] They're okay. They're above and left
[01:25:01 - 01:25:07] I would probably do this slightly different with my radius. I'll show the center of the radius as well
[01:25:07 - 01:25:09] Yeah
[01:25:09 - 01:25:12] Cool
[01:25:12 - 01:25:14] Yeah, so that's your drawing is not to scale
[01:25:15 - 01:25:16] Is that what you mean?
[01:25:16 - 01:25:21] I think that this is
[01:25:22 - 01:25:24] I would say that that's okay
[01:25:25 - 01:25:28] With a city drawings not to scale so they don't need to sail with the scalars
[01:25:29 - 01:25:30] Yeah
[01:25:30 - 01:25:32] If it was the scale then you wouldn't need to say what it was
[01:25:33 - 01:25:36] And even if it was the scale enough sit as not to scale
[01:25:39 - 01:25:44] How can you tell if it is to scale for i don't know you know that's getting into a hard to define area
[01:25:44 - 01:25:47] Cool while we're on on form
[01:25:48 - 01:25:49] What
[01:25:49 - 01:25:54] Powerably improve this one. Can you see that very well? I can see it okay
[01:25:55 - 01:26:00] Cool so this one here is an assembly drawing so often when you've got your drawings
[01:26:00 - 01:26:04] It's kind of common to say like here's in the assembly drawing or it all together
[01:26:04 - 01:26:06] And then here are our manufacturing drawings for each of the parts, right?
[01:26:06 - 01:26:07] So that's why I've said
[01:26:08 - 01:26:12] I recommend for this assignment having two to four drawings depending on the number of members that you have
[01:26:13 - 01:26:18] I wouldn't break it down into each of your little individual parts of other member
[01:26:18 - 01:26:23] Right? I would just show it glued together and I'd probably make a note that sort of says you know
[01:26:23 - 01:26:25] This is the part being made from multiple aluminium bits
[01:26:26 - 01:26:30] It showed the limits or show the glue or make a note to say where the glue should go
[01:26:30 - 01:26:32] Cool so if you're marking this
[01:26:32 - 01:26:34] How we going should we start with a title block
[01:26:35 - 01:26:41] Is it good?
[01:26:41 - 01:26:43] Feel okay. What's good about the title up?
[01:26:44 - 01:26:46] It's got the date. How yeah
[01:26:48 - 01:26:50] It's got the project
[01:26:51 - 01:26:53] You know we're gonna shimmed it. They're filled out
[01:26:53 - 01:26:55] They're name and who drew it in the supervisor
[01:26:56 - 01:26:58] Cool, this is also fine. You're a assembly drawing
[01:26:58 - 01:27:01] So you could say refer to your manufacturing or your part drawings
[01:27:01 - 01:27:03] And then that is also good, right?
[01:27:04 - 01:27:08] Only thing that I'd say is if he is that should be like a number that makes sense
[01:27:09 - 01:27:12] Yeah, so if this is drawing one the next one should be drawing two next one should be drawing three
[01:27:13 - 01:27:15] I always like to use three numbers. I don't know why
[01:27:15 - 01:27:18] So I'll like style of 001, you know
[01:27:20 - 01:27:24] Seems optimistic but makes it a little bit of than just having like one digit there
[01:27:24 - 01:27:26] Cool in terms of this year
[01:27:26 - 01:27:31] What do we think is this clear or could it be clearer if we had not exploded?
[01:27:31 - 01:27:36] It'll done it a different way
[01:27:36 - 01:27:38] So it could be larger make bigger
[01:27:42 - 01:27:47] Which is our size, right?
[01:27:47 - 01:27:49] Yeah, I mean it's like one of those
[01:27:50 - 01:27:52] Technical things. I would have think the same as you
[01:27:52 - 01:27:57] I'd be like start with one the one next that should be two the one next that should be three that like
[01:27:57 - 01:27:59] Technically it's probably okay
[01:28:00 - 01:28:02] But it's sort of confusing
[01:28:03 - 01:28:05] The way that they've exploded it
[01:28:06 - 01:28:10] So they've got part
[01:28:10 - 01:28:12] Does it match up part one?
[01:28:13 - 01:28:16] Well, I mean what's this is this bill of materials good to start with
[01:28:18 - 01:28:21] No, so like either the so part number. I'll probably remove
[01:28:22 - 01:28:27] Unless it actually referred to like a partner, but a lot of the time like this would refer to like say
[01:28:27 - 01:28:29] I picked a standard bearing from SKF
[01:28:30 - 01:28:32] There would actually have a part number
[01:28:32 - 01:28:36] For your assignment these aren't like standard paths that have a part number or product code
[01:28:36 - 01:28:41] So I'd probably just delete that and then just have description and then it kind of goes okay, right?
[01:28:41 - 01:28:46] And then I guess our comment was does it make it more clear if it's exploded in my opinion
[01:28:47 - 01:28:52] It would be clearer if it was not exploded and actually just had here's number one
[01:28:52 - 01:28:57] It's how compression into here's number two. It's our second compression in there here's number three
[01:28:57 - 01:29:01] It's our failure member. Yeah, you could add a descriptor if it's an I beam or a
[01:29:01 - 01:29:06] T beam or whatever, but I would keep it pretty simple and make it nice and nice and clear because
[01:29:07 - 01:29:10] All of these details of how it goes together should be clear in your part drawing
[01:29:11 - 01:29:13] Yeah
[01:29:13 - 01:29:18] Do you have to include the pin up to you you do don't have to not also
[01:29:18 - 01:29:20] I feel like they've picked a really weird view
[01:29:22 - 01:29:24] Yeah, I as technically isometric
[01:29:26 - 01:29:28] But it's like you're looking at it from behind
[01:29:29 - 01:29:32] Yeah, because they don't have the other views. It's kind of hard to see that
[01:29:33 - 01:29:35] That's kind of fine right?
[01:29:35 - 01:29:39] Cool
[01:29:40 - 01:29:42] What else do we have
[01:29:42 - 01:29:44] Here's one here finally
[01:29:44 - 01:29:48] So we can review this one and then we can quickly go over the notes about our
[01:29:50 - 01:29:53] Our reports and then we should be pretty all good
[01:29:54 - 01:29:58] To have a lovely weekend and a well-deserved break from lectures and people like me
[01:29:59 - 01:30:00] Yeah
[01:30:00 - 01:30:03] Cool, so this one here you can see it is our team sound in there
[01:30:03 - 01:30:09] So shall we start where do we want to start or can someone tell me something that is done well or not done well
[01:30:12 - 01:30:15] Okay, yeah, so size size is okay. Yeah, okay
[01:30:17 - 01:30:22] So it's not way too small obviously you might be able to make it a tiny bit bigger, but then it's gonna get kind of interacting with this
[01:30:23 - 01:30:28] Right what's missing if we look at our two views what's missing?
[01:30:30 - 01:30:34] View labels right so technically this one here is our front
[01:30:35 - 01:30:37] Which means that this has to sort of either be our top
[01:30:38 - 01:30:44] Right, so that really should be moved up here and follow third angle also graphic
[01:30:45 - 01:30:53] Because that's what I said it is here. It's not the standard convention that you would use for all the graphic so
[01:30:55 - 01:30:57] that would be
[01:30:57 - 01:30:57] like
[01:30:57 - 01:30:59] technically
[01:30:59 - 01:31:04] I know it's like trying to fight your mass teacher. I guess you know, it's like oh you didn't have units as well
[01:31:05 - 01:31:09] I did it all right though, so you didn't show all of your working. So technically
[01:31:10 - 01:31:14] Could go either way if you know who would probably minor you might get a comment and not lose a mark
[01:31:14 - 01:31:19] But it'll be way easier for everyone if you just follow the convention that you said you're using
[01:31:19 - 01:31:23] If you said bottom then you could say no, I understand the convention. I just want to do it like that
[01:31:24 - 01:31:26] I know yeah
[01:31:26 - 01:31:28] If you see that was top
[01:31:29 - 01:31:32] Then the market has you know grounds
[01:31:32 - 01:31:34] Cool
[01:31:34 - 01:31:37] What else we got how are our dimensions?
[01:31:40 - 01:31:42] 40 so it's kind of a tricky one
[01:31:45 - 01:31:50] Yeah, I would probably have just had it in like this and then out like that and it's also
[01:31:51 - 01:31:54] It's quite a difficult one like this is the thing that's crazy, right?
[01:31:54 - 01:31:58] It's like it's R 40 to zero and it's past minus one
[01:31:58 - 01:32:05] So like realistically I expecting a technician to like get out a radii and like check the radii
[01:32:05 - 01:32:11] Right, so that might be something that you haven't note that like or I haven't note here or a note in the thing
[01:32:11 - 01:32:14] So you know all you just should be smooth and that you know the radii
[01:32:15 - 01:32:18] It's not actually that important if it's to plus or minus point one
[01:32:19 - 01:32:21] Yeah, but technically it's the litter of the law
[01:32:21 - 01:32:25] This could be quite a pain to do because then it's also like with these radii
[01:32:26 - 01:32:28] Like this one here in particular. What's wrong with this dimension here?
[01:32:29 - 01:32:31] So what makes me go bald at night
[01:32:34 - 01:32:36] Is it possible like was everyone see it?
[01:32:42 - 01:32:44] Can you like is that all good?
[01:32:46 - 01:32:48] Well like is that possible to measure?
[01:32:50 - 01:32:54] No, right? So this is a classic like SOLIDWORKS CAD do it to like tangent edges
[01:32:55 - 01:33:00] Yeah, so like they in the CAD you see like a line there that like does not exist in real life
[01:33:01 - 01:33:03] So for you to measure
[01:33:03 - 01:33:07] Then the first place good luck to measure that to possible minus point one
[01:33:08 - 01:33:15] Yeah, so again having a note note that just says you know smooth all ages to remove any sharp radii
[01:33:16 - 01:33:19] Or you could have this in brackets in a note again
[01:33:20 - 01:33:24] Some of those what I've said might miss it not necessarily follow the litter of the law
[01:33:24 - 01:33:27] But um as long as it's really clear and you have like
[01:33:27 - 01:33:32] Something that you can justify as to why you put that there then you could have a happy conversation with a technician
[01:33:32 - 01:33:35] And it should be fine. If you do something like this then like
[01:33:36 - 01:33:40] Maybe that just makes the technician want to go and smoke as soon as they get your job
[01:33:41 - 01:33:43] So they don't have to look at it
[01:33:44 - 01:33:46] Cool um
[01:33:46 - 01:33:50] So there are some sort of similar problems to previous ones
[01:33:51 - 01:33:54] So game this part here. I'm not sure how they've done it that
[01:33:55 - 01:34:00] The dimension line is touching the feature that it's dimensioning so they should actually be a gap in here, right?
[01:34:03 - 01:34:11] What else can we see it could be on specific launches? There is specific
[01:34:11 - 01:34:14] Thiances which is kind of good they kind of type that
[01:34:14 - 01:34:16] We'll give them the power on the back for at least doing that
[01:34:16 - 01:34:21] But for you it might not need to be so this is that limits and fits thing that you can see in action
[01:34:21 - 01:34:25] If you really want to you could you know so saying that because the pen is 8 mil
[01:34:26 - 01:34:30] We want it to be between 8 and 8.1 because otherwise the pen can't fit
[01:34:31 - 01:34:33] Well if it's just 8 plus or minus point one
[01:34:34 - 01:34:37] Then it's not going to fit if it's less than that and typically in specification, right?
[01:34:38 - 01:34:39] That's good
[01:34:39 - 01:34:44] But then they haven't done a specific dimension for this because this is quite small
[01:34:44 - 01:34:47] What could we use to show this a little bit clearer?
[01:34:51 - 01:34:52] What kind of you could we add?
[01:34:56 - 01:34:58] Part of you or a detailed view I think is the one
[01:34:59 - 01:35:07] So if there's small features that are kind of like hard to dimension
[01:35:07 - 01:35:11] If you had a detail view there then there could be some sort of bubble over here
[01:35:12 - 01:35:16] It says detail away and then it has that hole
[01:35:18 - 01:35:19] Yeah
[01:35:19 - 01:35:21] There's the details about that
[01:35:22 - 01:35:24] Cool sizes okay
[01:35:25 - 01:35:27] Other dimensions okay
[01:35:27 - 01:35:31] Same issue right one of these needs to be in brackets. We have over-dimensioned
[01:35:32 - 01:35:34] Over-defined
[01:35:35 - 01:35:39] And then we've got radii again. I would probably question
[01:35:40 - 01:35:42] Question that
[01:35:42 - 01:35:44] That holes are located
[01:35:46 - 01:35:50] But possibly this one here. I mean that's fine 20 and then that's there
[01:35:52 - 01:35:55] Okay, so that's you they they haven't done what I said there but
[01:35:57 - 01:35:59] Yeah, if they had dimension there as well
[01:35:59 - 01:36:01] So actually
[01:36:10 - 01:36:11] Yeah, it's one of those fiddly things with SOLIDWORKS
[01:36:11 - 01:36:13] But it would depend on where and the line you click
[01:36:14 - 01:36:18] So if they clicked like this line in this line then that's why the line projection line is going along it
[01:36:19 - 01:36:23] But if they clicked this point here, this should actually be a gap
[01:36:24 - 01:36:33] Yeah, okay
[01:36:33 - 01:36:37] So I mean we possibly want to try and keep our dimensions off the part
[01:36:38 - 01:36:43] Which is why the detail view will help this one here. Similarly, I would probably
[01:36:43 - 01:36:45] I mean, there's not necessarily a good way
[01:36:47 - 01:36:50] To keep it clear. So what they've done is probably okay
[01:36:51 - 01:36:57] But I would try and probably pull it this way so that it's not having an error on the part there. I don't have my error there
[01:37:00 - 01:37:02] Yeah
[01:37:02 - 01:37:06] Yeah, sometimes you'll get sort of friendly ones like that that similarly you could just
[01:37:07 - 01:37:09] Say, you know remove
[01:37:09 - 01:37:10] Oh, yeah
[01:37:10 - 01:37:14] Have typical or bigger dimensions or bigger times as for those radii and they comment that says it is
[01:37:15 - 01:37:17] There for a functional reason rather than
[01:37:17 - 01:37:20] Manufacture it exactly to the litter of the law to this
[01:37:21 - 01:37:26] Cool so just because we don't have heaps of time if we want to we can always review some more drawings
[01:37:27 - 01:37:29] But what I wanted to do was
[01:37:30 - 01:37:38] Well, I'd use this kind of has it doesn't look like you've tried in the intermediate steps as a like as a checklist that you can use
[01:37:39 - 01:37:41] to go over what your
[01:37:42 - 01:37:44] Review your drawings poison at them
[01:37:45 - 01:37:51] Cool and then obviously the other thing that you'll need to do is write a report with your
[01:37:53 - 01:37:59] Son, right, so what we can see here is just some comments. I know that we've already kind of touched on the fact that we can use our
[01:38:00 - 01:38:02] main headings that are in the
[01:38:02 - 01:38:05] Mark sheet as headings for our report, right so
[01:38:07 - 01:38:08] We want to know introduction
[01:38:08 - 01:38:10] Why you chose the design that you chose?
[01:38:10 - 01:38:25] Some of the things that I see definitely include in that section do we just want
[01:38:26 - 01:38:29] Only a written description of what your designers
[01:38:30 - 01:38:37] No, it will be better to have a figure or a screenshot of your cab that shows what it is so that when you talk about it
[01:38:37 - 01:38:40] If there's a look in it I can go. Oh, yeah, you know, they do have three members
[01:38:40 - 01:38:45] I can see in the figure. Yep, and then there's information about the failure loads in a failure modes, right?
[01:38:46 - 01:38:47] Cool, so overall
[01:38:48 - 01:38:50] This is a general kind of note on
[01:38:51 - 01:38:53] Expectations for engineering reports
[01:38:53 - 01:38:59] It's just to clarify what I expect in terms of when you put together an in-ear report because sometimes
[01:39:00 - 01:39:05] I've had feedback from students saying like I didn't know that I need to include a figure in my final design
[01:39:05 - 01:39:08] I didn't realize that they're the same enough as looking for and so
[01:39:09 - 01:39:12] That's why I wrote this at the start
[01:39:12 - 01:39:18] So overall the main purpose of engineering reports screen you call it communicate what you have done to anyone who is skilled in the art
[01:39:18 - 01:39:23] i.e. Another engineer of what you did why you did it and how you did it
[01:39:23 - 01:39:27] So we can see here. What do you want us to write for the description of the final design?
[01:39:27 - 01:39:32] For this I would respond by staying at the description of the final design should make it clear to the reader
[01:39:32 - 01:39:36] What your final designer's what the key features are slash how it works
[01:39:36 - 01:39:40] What are the limitations if there are some relevant results from testing and calculations?
[01:39:41 - 01:39:44] If you have not done this in a pre-section of the report already
[01:39:45 - 01:39:48] Cool, so you can all agree that it's very difficult to read other people's minds
[01:39:49 - 01:39:52] And if you look at a solution to an engineering problem
[01:39:52 - 01:39:56] There's almost impossible to understand the depth of work and how well the engineer
[01:39:56 - 01:40:00] Understand the project purely by looking at the solution
[01:40:00 - 01:40:02] So this is analogous to
[01:40:02 - 01:40:06] Working being shown in the mass problem or engineering calculation
[01:40:06 - 01:40:09] If you have a report that details why you did it
[01:40:09 - 01:40:14] Someone can agree with you that that's an appropriate solution if they're just looking at something with no context
[01:40:14 - 01:40:16] They might think that is terrible or not understand
[01:40:16 - 01:40:21] Oh, why is there this little design picture here or was there something to do with that right so
[01:40:22 - 01:40:26] If the approach to the problem is unstructured with no clear steps and no clear working
[01:40:26 - 01:40:31] It is difficult for the marketer judge the depth of work and give you a mark for it
[01:40:31 - 01:40:33] The report should show and tell
[01:40:33 - 01:40:38] The approach to your work and the steps you took to arrive at your final solution
[01:40:38 - 01:40:42] So if you're unsure when you're writing up your report
[01:40:42 - 01:40:46] That is the kind of the main kind of points that I would re highlight
[01:40:47 - 01:40:50] And then generally for communications is going to be useful
[01:40:50 - 01:40:53] Is that the three things that I think about
[01:40:54 - 01:40:57] Purpose audience and content
[01:40:58 - 01:41:03] So those are kind of that's the hierarchy that I'll use when it comes to defining or deciding what type of
[01:41:03 - 01:41:05] Communication you'll use
[01:41:05 - 01:41:06] Gently
[01:41:06 - 01:41:09] So what is the purpose of communication? Who is the audience?
[01:41:10 - 01:41:12] This is important because that will change
[01:41:13 - 01:41:15] What kind of content you deliver up?
[01:41:15 - 01:41:17] So if I was trying to explain
[01:41:17 - 01:41:23] Stress concentrations to primary schoolers, I probably would not be using formulas and drawing sketches
[01:41:24 - 01:41:26] Like I was today
[01:41:27 - 01:41:28] So
[01:41:28 - 01:41:30] You can't see that there
[01:41:30 - 01:41:34] Two of common structures often it sort of depends on exactly what you're working on
[01:41:34 - 01:41:39] But you'll see that this is a very common structure that you'll have for engineering reports
[01:41:39 - 01:41:42] So some sort of abstract or summary
[01:41:42 - 01:41:44] Intro slash background some problem definition
[01:41:45 - 01:41:48] proposed solutions, final solutions, conclusions, preferences
[01:41:48 - 01:41:50] And then depending on what the project is
[01:41:50 - 01:41:53] There may be other types of sections
[01:41:54 - 01:41:58] Such as testing or testing methodologies or discussions
[01:41:59 - 01:42:00] But for now
[01:42:01 - 01:42:03] I'm just going to leave this and say
[01:42:03 - 01:42:05] Here's a resource that you can use if you want to see some examples
[01:42:06 - 01:42:10] But basically a lot of the time the table of contents is kind of your guiding
[01:42:12 - 01:42:14] Guiding tool to kind of structure a report
[01:42:14 - 01:42:18] So someone looks at the table of contents. They should sort of know roughly
[01:42:18 - 01:42:21] This is what the report is going to give us information about right?
[01:42:21 - 01:42:23] So you can see here. This is one
[01:42:24 - 01:42:28] That's been taken from one of the final projects a few years ago that I was helping with
[01:42:28 - 01:42:31] Where they've kind of got sub-sections to kind of show you know
[01:42:31 - 01:42:34] What other bits of background that are being covered?
[01:42:34 - 01:42:38] What are the main bits of the scope and deliverables or resources right?
[01:42:39 - 01:42:41] So with that
[01:42:42 - 01:42:44] That's everything that I have for today
[01:42:44 - 01:42:48] I hope you have a really good weekend and if you've got any questions I'll be further right
[01:43:31 - 01:43:33] I
[01:44:01 - 01:44:20] Use that on my
[01:44:21 - 01:44:25] I
[01:44:28 - 01:44:33] Just a quick question with the drawings one second. I'll just before I forget
[01:44:33 - 01:44:39] I will close this and then answer your question.
[01:44:39 - 01:44:40] Oh, okay.
[01:44:40 - 01:44:41] Let's go.
[01:44:41 - 01:44:42] Let's go.
[01:44:42 - 01:44:47] Oh, let's make me out.
[01:44:47 - 01:44:48] What is that?
[01:44:48 - 01:44:49] I also told this out.
[01:44:49 - 01:44:51] Otherwise, it's kind of problematic.
[01:44:51 - 01:44:52] I don't have it.
[01:44:52 - 01:44:53] Cool.
[01:44:53 - 01:44:54] I can ask you a question.
[01:44:54 - 01:45:02] I would still draw a number of, yeah,
[01:45:02 - 01:45:04] probably, two days.
[01:45:04 - 01:45:06] Remember, yeah, I just remember,
[01:45:06 - 01:45:07] just a number of, yeah, I guess,
[01:45:07 - 01:45:09] I don't want to draw one.
[01:45:09 - 01:45:11] I don't want to draw one.
[01:45:11 - 01:45:12] So, okay.
[01:45:12 - 01:45:13] Draw one.
[01:45:13 - 01:45:14] Draw one.
[01:45:14 - 01:45:15] Draw one.
[01:45:15 - 01:45:16] Draw one.
[01:45:16 - 01:45:18] See, we draw a kid.
[01:45:18 - 01:45:20] And that's what I'm saying.
[01:45:20 - 01:45:22] And then, you can see,
[01:45:22 - 01:45:23] pop one.
[01:45:23 - 01:45:26] And then, draw a kid.
[01:45:26 - 01:45:27] And then, draw a kid.
[01:45:27 - 01:45:29] So, I'm going to bring one.
[01:45:29 - 01:45:30] I'm going to bring one.
[01:45:30 - 01:45:31] Okay.
[01:45:31 - 01:45:32] Okay.
[01:45:32 - 01:45:33] So, clearly.
[01:45:33 - 01:45:36] No, it's not like you're going to get one.

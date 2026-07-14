# ENMT301-26W Lecture 07 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_07_audio_16k_mono_32k.mp3`
Source audio SHA-256: `da624bbf8d3bd3592a13764665511c4ff9c1b2f2499c9c177d177f24108e4c10`
Generated: 2026-06-06T05:07:56.589405+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:06 - 00:00:10] Alright, thanks everyone. We'll make a start there. It's lovely to see you all.
[00:00:10 - 00:00:24] Alright, can you guys hear me in the back?
[00:00:24 - 00:00:27] Good with my La Palette. Perfect.
[00:00:27 - 00:00:34] So we're into lecture two of week two, although it seems like we have really covered quite a lot, which is really quite good.
[00:00:34 - 00:00:41] So hopefully you've run sort of as at least a weird that we have this assignment and know something related to it,
[00:00:41 - 00:00:44] maybe that it involves aluminium strips.
[00:00:44 - 00:00:54] So we'll continue this week and by the end of the week you pretty well have everything that you'll need to finish the assignment the following week if you really wanted to.
[00:00:54 - 00:01:01] So for those that like to be old for organised, the idea this year is that I've tried to give everything that's important for the assignment.
[00:01:01 - 00:01:09] It's quickly as possible so that then you guys can simmer on it rather than waiting until week four to do the thing that you need to do at the end of week five.
[00:01:09 - 00:01:14] So we'll keep powering you here. So notices.
[00:01:14 - 00:01:19] You're panicking me anywhere in the class then we asked down last week.
[00:01:19 - 00:01:25] Material testing clarification for those that didn't tend to watch the lecture on, well, the lictorial on Friday.
[00:01:25 - 00:01:30] We kind of went through what our dog will unshade my luck like.
[00:01:30 - 00:01:34] I think some people have made some. Has anyone done any testing yet?
[00:01:34 - 00:01:39] Yeah, was the testing all good? Yeah, double thumbs up. I had a quick double thumbs up again.
[00:01:39 - 00:01:50] Perfect. So obviously someone asked a really good question yesterday in the drop-in session around like, you know, what is actually realistically the minimum size your dog bone could be in us with it.
[00:01:50 - 00:01:59] Depending on the length of the reduce section, that's probably going to be what kind of defines it and the extent some of the foot on it is going to be kind of that long-term factor.
[00:01:59 - 00:02:08] So you want to make them small, but they can't be like, I only have a reduced section of say 10 millimeter because then you wouldn't be able to get your iced in some.
[00:02:08 - 00:02:15] But on a set, what you're trying to do and you probably would also be having some sort of stress concentration if you're not.
[00:02:15 - 00:02:20] Was that kind of steep, right? So for those who did them, how long were they roughly?
[00:02:20 - 00:02:24] Around 150-ish mills seem to be the typical kind of area.
[00:02:24 - 00:02:30] You can kind of see it in the photo that I had shown the last one that might be coming up as well.
[00:02:30 - 00:02:34] So obviously to make them, you can file or cut them to shape.
[00:02:34 - 00:02:41] I would make sure that you keep those edges that are on that reduced section kind of as blemish-free as possible.
[00:02:41 - 00:02:45] So if there's a little notch where you've gone a little bit to keen the front of the files,
[00:02:45 - 00:02:51] I would kind of try and make sure that there's not any sharp pinks because that's going to affect your results.
[00:02:51 - 00:02:54] Especially if that's where it kind of fails, right?
[00:02:54 - 00:02:59] So on learn, I've put up some quizzes as I say because we're rocketing ahead this year.
[00:02:59 - 00:03:11] So that hopefully next week I can kind of actually summarize some of the class results because it seems to be a little bit of anxiety sometimes around whether your results or the real results in everyone else has different results to yours.
[00:03:11 - 00:03:16] So it's just kind of like a nice, deep breath that you can only go like, oh, look my results.
[00:03:16 - 00:03:21] I'm on to what our everyone else in the class is kind of done.
[00:03:21 - 00:03:31] So you don't need to do this one person, your group basically to submit this, but you'll see here that I've got these little questions in the class.
[00:03:31 - 00:03:43] So if you've done your material testing and you want to share that, then what I kind of do is anonymize it and then just give a distribution kind of curve that at least shows kind of what the values people are getting.
[00:03:43 - 00:03:48] So actually you put in the right one, so obviously yield versus ultimate tensile, right?
[00:03:48 - 00:03:52] So just make sure you do the right one, the right place to otherwise.
[00:03:52 - 00:03:57] That's another thing that can impact the results that I showed here and we might see that anyway.
[00:03:57 - 00:04:01] And is anyone worked out the Young's Modulus?
[00:04:01 - 00:04:03] No, you have a fixed instinter.
[00:04:03 - 00:04:09] Obviously you'll use that for doing your buckling stuff which we talked a bit about last Friday.
[00:04:09 - 00:04:10] Cool.
[00:04:10 - 00:04:13] So you might end up having some sort of table like this.
[00:04:13 - 00:04:19] And then there's an example of kind of what our dog bones might look like, right?
[00:04:19 - 00:04:20] Cool.
[00:04:20 - 00:04:25] So today we'll cover some quick, please just what the references are that I used to make this lecture.
[00:04:25 - 00:04:34] We'll go over one of the key slides that we'll build on in this lecture and then we'll build the other design process specifically in designing for safety, cost, and strength.
[00:04:34 - 00:04:43] We'll do an example calculation and talk about factors of safety and low factors and that will be hopefully us within our kind of 50 minute kind of time zone.
[00:04:43 - 00:04:50] And so with that example calculation we'll also talk about preferred sizes and why you might want to use the preferred size.
[00:04:50 - 00:04:55] Generally in all of your engineering design stuff, almost ever in a way.
[00:04:55 - 00:04:59] Unless you've got a huge budget and a real need for some niche things.
[00:04:59 - 00:05:00] Cool.
[00:05:00 - 00:05:04] Does anyone heard of this sugly guy, top one?
[00:05:04 - 00:05:06] Wow, so beautiful day.
[00:05:06 - 00:05:11] So this guy is what I would say is like, he's the go, he's the OG.
[00:05:11 - 00:05:14] I guess when it comes to mechanical engineering design.
[00:05:14 - 00:05:22] And so if there's one textbook to like at least look at, then any of the sugly mechanical engineering design books are kind of the go-to things.
[00:05:22 - 00:05:27] Like there's one thing that happens when you, I don't know, maybe you travel the world like I did and work overseas.
[00:05:27 - 00:05:30] You'll probably say, oh, what was the textbooks that you used?
[00:05:30 - 00:05:32] Probably going to be stupidly.
[00:05:32 - 00:05:33] Nine times out of 10.
[00:05:33 - 00:05:34] Cool.
[00:05:34 - 00:05:40] Obviously, fused total design is one that we just got that nice diagram from our design process from.
[00:05:40 - 00:05:44] And then there are these other design books which are quite useful.
[00:05:44 - 00:05:49] This is the one in particular is quite nice just looking at machine elements and general.
[00:05:49 - 00:05:52] But it covers very similar stuff to sugly.
[00:05:52 - 00:05:57] And then again, this one Ipenger which has got some more kind of product development sort of.
[00:05:57 - 00:06:03] Twist on the engineering design process, but a lot of them sort of follow very similar kind of concepts.
[00:06:03 - 00:06:04] But yeah.
[00:06:04 - 00:06:05] Cool.
[00:06:05 - 00:06:09] So I guess this is just a plug there I suppose.
[00:06:09 - 00:06:15] With our machine design stuff that we'll be doing later in the semester without bearing housing assignment in shaft design,
[00:06:15 - 00:06:20] a lot of that material we'll be taking from sugly as a guiding kind of principle.
[00:06:20 - 00:06:21] Cool.
[00:06:21 - 00:06:25] So last week we focused on basically the course introduction.
[00:06:25 - 00:06:34] But we did also mention the design process and the fact that there are lots of different types of design depending on what kind of realm you are living in.
[00:06:34 - 00:06:46] And for us as engineers, we have engineering design process which I guess simply put as an iterative way to systematically solve unstructured problems.
[00:06:46 - 00:07:05] So we see that this is one of the kind of design process diagrams that kind of shows what engineers might be doing as they take a possible idea and analyse with it or actually has any kind of purpose in the market to identify what the specifications are that are required to make it a really good product.
[00:07:05 - 00:07:14] And then going through what you may have had some experience with from the past of actually coming up with concepts and evaluating them and then developing the one that you think will be the best.
[00:07:14 - 00:07:19] A bit more and then kind of getting into testing and then effect your before you can kind of sell it, right?
[00:07:19 - 00:07:32] So for some people this might be they might be doing elements of these kind of different causes what they call them, these each of the exhibits here as they're kind of job-wrapped.
[00:07:32 - 00:07:34] So depending on what you're doing.
[00:07:34 - 00:07:43] So if you're working as a consulting engineer you might always be doing the detailed design for a specific kind of project and a niche technical area that you're an expert.
[00:07:43 - 00:07:54] And I see like in this engineering we can do as this possible iterative process and you may go back to step two if you haven't done step three right the first time.
[00:07:54 - 00:08:09] Cool, so you'll see that ensure a need will come apparent, you'll use your specifications and background research to basically identify what the need is and what the specifications are to make sure that that need is met really well.
[00:08:09 - 00:08:14] So ideally you want to answer these kind of questions here. What is the problem you're trying to solve?
[00:08:14 - 00:08:18] Is this a true problem? How you define this problem frame?
[00:08:18 - 00:08:20] Well how you frame the problem is kind of critical.
[00:08:20 - 00:08:28] So I've had this yesterday I was talking to some clinicians about a new kind of medical walker device that we're thinking about kind of trying to make.
[00:08:28 - 00:08:33] And that's saying oh be really great if you did this or you did this or you did this because these existing workers have these problems.
[00:08:33 - 00:08:39] And it's like oh that's a really interesting insight. We'll probably see how we go that might not be what we do.
[00:08:39 - 00:08:56] But if you just jump and shred away so for example I said design a device that does it's been automatically you're narrowing your thought I suppose and to it has to be a device where if I see that our device and means of doing it then it might not necessarily be a device that you design right.
[00:08:56 - 00:09:01] How you frame the problem is like kind of critical to make sure that you a.
[00:09:01 - 00:09:09] So the right problem and b don't kind of not think about some possible solutions because of the way you frame the problem.
[00:09:09 - 00:09:20] So from there you'll do your concept ideation so brainstorming in analysis and selection and then your detailed design where you'll be doing your drawing calculations and running a report.
[00:09:20 - 00:09:24] Sort of sounds familiar hopefully so these are sort of this area here.
[00:09:24 - 00:09:30] We've sort of given you a specifications that you're jumping in here for our aluminium structure assignment.
[00:09:30 - 00:09:38] Last week we talked about some of the concept design that you can do obviously with the shape and overall kind of ideas around your design.
[00:09:38 - 00:09:46] So we're going through those detailed design elements and making it and testing it on tester and week eight.
[00:09:46 - 00:09:57] Cool so we probably won't be selling our aluminium structures but you can see there's a better work then also goes there in terms of how the distribution works and how the sales model works and all of that sort of side thing.
[00:09:57 - 00:10:03] So those are also kind of key considerations while going along the process.
[00:10:03 - 00:10:14] So the use of engineering design process helps engineers to understand the whole picture and doing this well hopefully we will reduce the number of iterations needed to arrive at a final solution.
[00:10:14 - 00:10:23] So if you do a really good job with earlier things should mean that you have to do less iteration going back and forward where you found out the thing that I showed you maybe wasn't the best.
[00:10:23 - 00:10:26] Then we've got this nice quote here from Hodgson.
[00:10:26 - 00:10:31] So technical excellence is not enough without commercial competitiveness.
[00:10:31 - 00:10:33] Well that's really good breeding from me.
[00:10:33 - 00:10:41] But basically what we can see there is that just having technical excellence which is sort of like engineers bred in biode.
[00:10:41 - 00:10:52] Look at this really cool thing. Sort of all for nothing if there's not a need or a commercial competitiveness to it where actually someone wants to buy this cool thing that you're doing right rather than it just being.
[00:10:52 - 00:10:56] something that you can show off in parties or something.
[00:10:56 - 00:11:03] So what we see is this idea here does anyone know what this is?
[00:11:03 - 00:11:04] Yeah.
[00:11:04 - 00:11:05] Google Glass.
[00:11:05 - 00:11:08] How many of you guys will I? I don't know.
[00:11:08 - 00:11:10] I see if you're in I see.
[00:11:10 - 00:11:13] I probably I didn't make this lecture would probably be in that boat as well.
[00:11:13 - 00:11:21] So this is a really good example of talking through this kind of idea of technical excellence versus commercial competitiveness.
[00:11:21 - 00:11:26] So Google Glass was meant to be a revolutionary product.
[00:11:26 - 00:11:29] But as we all know the product never really caught on.
[00:11:29 - 00:11:30] I don't know.
[00:11:30 - 00:11:34] It's like maybe there's like an nostalgia about the 10 to 20s now.
[00:11:34 - 00:11:36] I know 20s to 20s.
[00:11:36 - 00:11:39] We're like there's all this like real good modern tech hype.
[00:11:39 - 00:11:43] I know like random iPhone videos that will ask me to do this and do that.
[00:11:43 - 00:11:45] I guess this is kind of like similar.
[00:11:45 - 00:11:47] It's like tech propaganda.
[00:11:47 - 00:11:49] It's like this is going to be revolutionary.
[00:11:49 - 00:11:56] Everyone's going to have one of these and then like I don't know if I either saw anyone ever where one of these.
[00:11:56 - 00:12:00] So why might it be that it really never really caught on?
[00:12:00 - 00:12:06] So one place to start is to ask what problem does this solve?
[00:12:06 - 00:12:08] Do you haven't got any ideas here?
[00:12:08 - 00:12:14] So is it easy to answer?
[00:12:14 - 00:12:17] Is there a commercial competitiveness for this product?
[00:12:17 - 00:12:19] Or is it just technical excellence?
[00:12:19 - 00:12:21] So I've thought about this before.
[00:12:21 - 00:12:24] And like anything that you can't use Google Glass for,
[00:12:24 - 00:12:28] you can kind of use like a watch or a phone smartphone or smartwatch kind of for.
[00:12:28 - 00:12:31] Yeah.
[00:12:31 - 00:12:34] Or a GoPro I guess if you really want to be recording stuff.
[00:12:34 - 00:12:38] So problems for Google Glass included a range of things,
[00:12:38 - 00:12:41] including how the case the how the safety concerns.
[00:12:41 - 00:12:45] So one was having radiation close to your eyes.
[00:12:45 - 00:12:50] The other one was that people got quite aggressive towards people that were wearing this.
[00:12:50 - 00:12:55] Because they didn't like the fact that they might have been recorded at the time.
[00:12:55 - 00:12:58] So it's like it was actually unsafe to wear them.
[00:12:58 - 00:13:02] Because there was a council thing of people being assaulted because of wearing them.
[00:13:02 - 00:13:05] They had a really high price competitive value.
[00:13:05 - 00:13:08] I can't remember how much they cost but it was like thousands of dollars.
[00:13:08 - 00:13:13] And I'm pretty sure that they didn't actually have enough kind of battery performance to last like a whole day.
[00:13:13 - 00:13:16] Sort of have to charge it as you'd go.
[00:13:16 - 00:13:19] There was a lot of privacy concerns, lots of data.
[00:13:19 - 00:13:24] And with this data was being managed kind of appropriately.
[00:13:24 - 00:13:31] The aesthetics were up to the base and people thought that they didn't necessarily look all that nice.
[00:13:31 - 00:13:34] Maybe it was ahead of its time.
[00:13:34 - 00:13:35] I don't know to me.
[00:13:35 - 00:13:40] Just kind of as one of those things that looks a little bit like episode of Black Mirror.
[00:13:40 - 00:13:42] That TV program.
[00:13:42 - 00:13:47] But this is essentially I suppose an example of what it kind of looks like.
[00:13:47 - 00:13:51] Some reason it looks like a GTA kind of screen or something.
[00:13:51 - 00:13:53] It doesn't really look like real life.
[00:13:53 - 00:14:02] But the idea that you can talk to your glasses and live your life through the lens, I guess.
[00:14:02 - 00:14:07] And then I guess following that, there's been a lot of AR and VR glasses.
[00:14:07 - 00:14:13] I know that those Apple or they're called Apple Vision Pro or something.
[00:14:13 - 00:14:15] Is there a label?
[00:14:15 - 00:14:16] Yeah, I.
[00:14:16 - 00:14:18] Is anyone used those?
[00:14:18 - 00:14:20] So again, it's like sort of the same thing.
[00:14:20 - 00:14:22] It runs like, oh yeah, this is definitely revolutionary.
[00:14:22 - 00:14:23] I'm not sure if it is.
[00:14:23 - 00:14:25] Maybe for some people it is.
[00:14:25 - 00:14:26] Yeah.
[00:14:26 - 00:14:30] Kind of an interesting sort of evolution to ponder and think about.
[00:14:30 - 00:14:32] And I wonder what the next thing might be next.
[00:14:32 - 00:14:36] I know that there are some people I mean for some of my research stuff at the moment.
[00:14:36 - 00:14:45] We've got a research project that's looking at using VR to try and give students in this place a different perspective of a design scenario that they're trying to design for.
[00:14:45 - 00:14:50] So I can see them quite useful as a tool, but I'm not sure all I can get.
[00:14:50 - 00:14:52] I feel like people must game on them or whatever.
[00:14:52 - 00:14:54] Not got hits of time for gaming.
[00:14:54 - 00:14:57] But yeah.
[00:14:57 - 00:14:59] I guess we'll see where they kind of go.
[00:14:59 - 00:15:02] But again, similar kind of thing of not sure if you'd see people walking down the street,
[00:15:02 - 00:15:05] things or some longer bus wearing there.
[00:15:05 - 00:15:07] Big set of VR glasses.
[00:15:07 - 00:15:09] Cool.
[00:15:09 - 00:15:11] So the specification design core.
[00:15:11 - 00:15:19] After identifying the market need, you're making sure that there's a real need and that there is a, I guess, money to be made.
[00:15:19 - 00:15:25] You'll need to make sure that you understand the user needs and the specifications of what is required.
[00:15:25 - 00:15:32] And so in pews book, you outlined a number of aspects to consider to do a thorough job of understanding the situation.
[00:15:32 - 00:15:40] So again, just highlighting the fact that these different design methodologies give us options to do a really thorough job.
[00:15:40 - 00:15:53] So for example here, you can see if you're doing a good thorough job of your specification, identification, you would look at each of these things and actually understand what is required for the thing that you design.
[00:15:53 - 00:16:01] So some of them are kind of obvious, like maybe the weight or the safety or the size.
[00:16:01 - 00:16:10] And then some of them might be things that you might not necessarily have thought about like how things might be installed or what the exact product last fan is.
[00:16:10 - 00:16:22] So all in all what they say is to fill out what he calls product design specification, which is basically a key document and a list of kind of specifications that can be updated as you go through this process.
[00:16:22 - 00:16:28] Cool. So there's huge amounts of detail that can be fleshed out for each of these considerations.
[00:16:28 - 00:16:39] So for example, if we just looked at an environment, these could include specific temperatures, pressures or humidity ranges that your device would need to be able to operate in.
[00:16:39 - 00:16:47] Could include things like dust, dirt or moisture or weakness of the environment, possibly corrosion considerations.
[00:16:47 - 00:16:55] There might be noise levels that need to be met, there might be vibrations and shock loadings, there might be insects or other things.
[00:16:55 - 00:17:10] And so that's the kind of thing, well these are the kind of things that would enable you to do a really thorough job just to make sure that you have clear idea of what is acceptable and what is sort of possibly less relevant or doesn't necessarily need to be met.
[00:17:10 - 00:17:18] So you'll learn a little bit more about that if you do for when you do for a one next year for the mechanical students.
[00:17:18 - 00:17:28] Cool. So what defines best for an engineer? Best comes from juggling a range of things, including design considerations and constraints.
[00:17:28 - 00:17:44] So for example, an engineer is often having to kind of weave the way in, tie together the optimized kind of best in regards to time price labour availability, social norms, cultural values, aesthetics, etc.
[00:17:44 - 00:17:55] So I often kind of chuckle to myself when I see the structural engineering lab. And I think this is a building that's been made by engineers, because for them, they're sort of building.
[00:17:55 - 00:18:04] And some people might like the big, big rectangle maybe I should be kind of careful what I say. But it seems like a very functional building for testing large things that are really tall, right?
[00:18:04 - 00:18:15] And so in that case, the best thing, maybe they toned down the aesthetics kind of knob of the building so that they could spend some more money on some of the kind of functional stuff on the inside, right?
[00:18:15 - 00:18:20] So engineers, like the best, doesn't really exist, you can't just turn everything to max.
[00:18:20 - 00:18:28] Cool. So this is from Shugley and we see that Jimi design considerations that might be requested for a given product as shown here.
[00:18:28 - 00:18:39] So very similar to what Pew head, but with a more nuanced kind of less in relation to actual kind of machine design considerations.
[00:18:39 - 00:18:49] So stiffness and surface finish and lubrication might not be a general kind of specifications you might do for every single product you're designing.
[00:18:49 - 00:19:01] So what we'll talk about is some of these ones bolded here, which are quite common for us in this class to kind of understand and know what we're trading off.
[00:19:01 - 00:19:09] So to start with, we just need to make sure that we understand design for safety in terms of this duty of trust.
[00:19:09 - 00:19:13] So this one of the things I think is going to be quite interesting with the world of AI.
[00:19:13 - 00:19:25] In fact, that anyone eventually is probably going to kind of almost be able to do anything or there's a lot lower barrier to high technical work with devices that just tell you things great and that there's an answer that it can be do it.
[00:19:25 - 00:19:37] But engineers have a certain level of trust within the community and there's something designed by an engineer if people kind of trust that it's not going to break and be a kind of mesh catastrophe, right?
[00:19:37 - 00:19:42] And so the way that we do this is with the design for safety and mine.
[00:19:42 - 00:19:52] So the public expect that if they are normal sense pool, human beings that they will be okay when using everyday kind of products, right?
[00:19:52 - 00:19:58] They even expect that if they are a little bit stupid or kids are a little bit stupid, they will also be okay.
[00:19:58 - 00:20:02] So what we call this an engineering is reasonable misuse.
[00:20:02 - 00:20:06] This is what the factor of safety kind of comes in with our calculations.
[00:20:06 - 00:20:11] We don't just design it to only have a factor of safety of one or one point two, right?
[00:20:11 - 00:20:21] So it's the engineers responsibility to design equipment and machinery that is safe for both the operator and the surrounding community to honor this level of trust.
[00:20:21 - 00:20:31] And so this is actually something that's, I suppose, tied in with engineering New Zealand's protovipics where engineers are required to report adverse consequences.
[00:20:31 - 00:20:41] So as you can see here, if you have reasonable grounds to believe that an engineering matter has or could have adverse consequences, you must bring that matter to the relevant regulatory body,
[00:20:41 - 00:20:48] unless having that inquiry is you are satisfied on reasonable grounds that the matter is being dealt with in a appropriate kind of manner.
[00:20:48 - 00:20:56] So essentially, if you see saying that's unsafe, as an engineer, you are now liable if you know that that's going to be unsafe and cause kind of messes.
[00:20:56 - 00:21:03] Let's use unless you kind of one up it if you were thinking about it in that way.
[00:21:03 - 00:21:05] So telling every regulatory body.
[00:21:05 - 00:21:12] So there has been stuff where I think there's a thing in the cross-jouche actually where an engineering student sort of building that had been designed in here.
[00:21:12 - 00:21:13] This is not right.
[00:21:13 - 00:21:15] I told the engineering come in.
[00:21:15 - 00:21:16] I'm like, yeah, you're right.
[00:21:16 - 00:21:17] It's not right.
[00:21:17 - 00:21:18] When you fix this ASAP.
[00:21:18 - 00:21:19] Yeah.
[00:21:19 - 00:21:25] It's something else to go bad and people knew that you knew that it was going to go bad.
[00:21:25 - 00:21:29] Then you could be liable for that.
[00:21:29 - 00:21:33] You've only heard of engineering in New Zealand before.
[00:21:33 - 00:21:34] Yeah.
[00:21:34 - 00:21:36] So sign up if you're a student, which you are.
[00:21:36 - 00:21:38] It's a free phase student member.
[00:21:38 - 00:21:45] And can give you some nice insights into what engineers do before you work out in the engineering career.
[00:21:45 - 00:21:48] So definitely recommend getting involved.
[00:21:48 - 00:21:51] So advanced consequences is defined.
[00:21:51 - 00:21:55] Significant harmless significant damage.
[00:21:55 - 00:21:56] Cool.
[00:21:56 - 00:21:58] So common safety design issues.
[00:21:58 - 00:22:07] I think Don Klugus might have talked about some of these in previous years, but covers our enclosures should be incorporated into areas where they're moving paths.
[00:22:07 - 00:22:10] So you can't kind of stick your fingers or other limbs into them.
[00:22:10 - 00:22:14] Fasten the train, pause injury to operator should not perform.
[00:22:14 - 00:22:16] Should not project from equipment.
[00:22:16 - 00:22:21] So, generally things that can be caught on clothing or on limbs.
[00:22:21 - 00:22:29] As long as you'll be such that any adjustments, lubrication or gym or maintenance can be performed with little difficulty or hazard.
[00:22:29 - 00:22:39] So unfortunately for many of the cars I've had to work on in the past, the version you need sometimes didn't necessarily make it have little difficulty.
[00:22:39 - 00:22:47] But what we see here, number four equipment should be an operable as long as his hands, fingers and feet are in the working zone.
[00:22:47 - 00:22:50] As we'll see a little example of ideas of that.
[00:22:50 - 00:23:00] Obviously sharp edges have ordered that your core equipment should be adequately designed and incorporated into relevant standards.
[00:23:00 - 00:23:07] Natural or force ventilation should be provided where the atmosphere contaminated with fumes, dust or other particles.
[00:23:07 - 00:23:12] For instance, we may to avoid exposures from forms of radiation.
[00:23:12 - 00:23:20] So we see a pretty, hopefully, list that makes sense and everything there you sort of understand.
[00:23:20 - 00:23:29] If you imagine if there were pieces of equipment that had been designed that didn't have any of these things adequately designed for that you're going to have issues.
[00:23:29 - 00:23:39] So what we see here is an example of a hydraulic press that was used, I believe, for making some of the spring free trampoline equipment.
[00:23:39 - 00:23:45] And the key thing that we can see here is kind of hard to tell, but there's these two buttons on the left and the right.
[00:23:45 - 00:23:51] And so you have to press both of those buttons to make the hydraulic press press, right?
[00:23:51 - 00:23:57] So the idea of that is so that you can't stick your hand in it and then crush your hand.
[00:23:57 - 00:24:01] So safety has been designed with safety in mind.
[00:24:01 - 00:24:08] However, because workers sometimes like to be a little bit more efficient if they're getting paid for partless perhaps, I'm not sure.
[00:24:08 - 00:24:11] They decided that it was possibly a good idea.
[00:24:11 - 00:24:19] If they teamed up, someone could hold the right button, someone could hold the left button, and then someone could quickly pass them as they go.
[00:24:19 - 00:24:21] So they could speed it up.
[00:24:21 - 00:24:31] So I'm just saying that actually Keith, I was ironed to tell me about on his travels and that as an engineer, he sort of had the duty that because there was an possible address,
[00:24:31 - 00:24:39] consequence, he knew that he would have been liable if there was kind of something bad to happen to these workers and that they would get their hands kind of crushed.
[00:24:39 - 00:24:50] So had to talk to the manager and make sure that these kind of processes were followed or out here so that we weren't having people putting their fingers within the hydraulic, hydraulic press as it was actually
[00:24:50 - 00:24:53] operating.
[00:24:53 - 00:24:56] Cool, so about halfway, pretty much bang on time.
[00:24:56 - 00:25:01] We've got this little question for you on V-box, so I think this should work.
[00:25:01 - 00:25:11] So if money were no object and you were the leader of a large organization looking to develop a new product, would you want to use an existing but perhaps unzoomorous product?
[00:25:11 - 00:25:15] Will spin money to be able to paint your own unique solution?
[00:25:15 - 00:25:20] So that should be the right number.
[00:25:20 - 00:26:13] The Q-
[00:26:13 - 00:26:15] for developing a new product.
[00:26:15 - 00:26:24] No, exactly sure why you might want to do that. Maybe just like the whole idea that it's not unglemorous, in that it's unique I'm not sure.
[00:26:24 - 00:26:35] But most often, even if money is no object and that's a statement that you're told by a client or a similar, it would be prepared to propose a cheaper,
[00:26:35 - 00:26:40] simple way of doing things. Most often, more than not, it will come down to cost.
[00:26:40 - 00:26:53] So if you can do the same thing cheaper, the client will most often want that cheaper kind of option as long as there's not too many other trade-offs, like you've completely turned all the aesthetics down or something similar like that.
[00:26:53 - 00:26:58] So originally when I kind of came up with this question, I was trying to relate it to the space bin.
[00:26:58 - 00:27:16] I'm not sure if it actually called that, which was developed by the Paul Fisher pin company or the Fisher pin company, which is basically being designed to write in any conditions, whether it's in space, high or low-term for your environments and the outdoors and plants that have all the conditions.
[00:27:16 - 00:27:20] Maybe if you even work underwater, I'm not exactly too sure.
[00:27:20 - 00:27:25] It was kind of like a fake kind of myth going around that.
[00:27:25 - 00:27:35] The Americans used the space bin where Soviet Union just took a pencil and sort of called it a day.
[00:27:35 - 00:27:39] But there's actually like fake milk which I was quite pleasantly surprised to kind of learn about.
[00:27:39 - 00:27:42] Apparently there's actually like a reason that you don't use.
[00:27:42 - 00:27:47] pencils have a little shards of graphite that will come out and can cause issues.
[00:27:47 - 00:27:53] So that was one of the reasons why the pin was decided, but originally it kind of fit the narrative of the question that are.
[00:27:53 - 00:28:02] So again, if you're having a discussion at your flat dinner table and you want to have an interesting fact, then this could be kind of one of the ones.
[00:28:02 - 00:28:03] Yeah.
[00:28:03 - 00:28:08] The main idea was that more than not, more often than not, the cheaper solution is the one.
[00:28:08 - 00:28:12] And then here's an example that doesn't quite take the box, I guess.
[00:28:12 - 00:28:16] So the reason that the simplest, the simplest solution is often.
[00:28:16 - 00:28:23] The reason for wanting to have lower costs is also related to the fact that the simplest,
[00:28:23 - 00:28:26] the simplest, possible solution is often the major goal.
[00:28:26 - 00:28:29] And cost is frequently if not always a design consideration.
[00:28:29 - 00:28:36] So if you make things really simple, they often helps to make them also costless, so it kind of goes hand in hand.
[00:28:36 - 00:28:40] Do not underestimate the fact that in the end, it will all come down to cost.
[00:28:40 - 00:28:51] And to do this, your ideal goal is to make sure that your engineering design meets all of the specifications that are demanded or required in the simplest possible way.
[00:28:51 - 00:28:57] This is often much more difficult than coming up with a complicated solution.
[00:28:57 - 00:28:58] Cool.
[00:28:58 - 00:29:02] So here we have our little practice question for you guys to do.
[00:29:02 - 00:29:07] So we've got your phone calculator, then you'll be able to give me an answer, ideally.
[00:29:07 - 00:29:16] So we can see here, the workshop brings you and asks you to tell them what don't do to make a bar to lift the two tons steel block on and off a truck.
[00:29:16 - 00:29:21] Where it is to be used is a way to help the truck pull a trailer.
[00:29:21 - 00:29:27] The bar will be welded to the block at the bottom and will have an eye at the top.
[00:29:27 - 00:29:33] So suddenly you can, on a layer of hook there, you can kind of put a rope or something similar to sling onto.
[00:29:33 - 00:29:35] So what does your reply?
[00:29:35 - 00:29:44] So if you quickly can kind of do a back of the envelope calculation, you can tell me what size bar you might recommend.
[00:29:44 - 00:29:56] Do we need some scaffolding?
[00:29:56 - 00:29:58] We're not sure we'd have to say.
[00:29:58 - 00:30:01] What kind of material might we make this bar?
[00:30:01 - 00:30:04] What is the material of the bar?
[00:30:04 - 00:30:05] Steel?
[00:30:05 - 00:30:06] All right.
[00:30:06 - 00:30:10] What is the steel stress of steel?
[00:30:10 - 00:30:12] 200 finger pass skills.
[00:30:12 - 00:30:16] It's a good rough estimate.
[00:30:16 - 00:30:20] Probably a good one to have like, lays it in your brain.
[00:30:20 - 00:30:22] Miles Steel, 200 finger pass skills.
[00:30:22 - 00:30:24] You even know when you might need it.
[00:30:24 - 00:30:25] Cool.
[00:30:25 - 00:30:29] So if you do that, does anyone go to an answer?
[00:30:29 - 00:30:30] What?
[00:30:30 - 00:30:32] How many millimeters?
[00:30:32 - 00:30:48] You've got an answer.
[00:30:48 - 00:30:49] It's quite an entry.
[00:30:49 - 00:31:08] Do we want to start working on it together?
[00:31:08 - 00:31:10] Well, you work.
[00:31:10 - 00:31:11] Yep.
[00:31:11 - 00:31:12] You do want to work on this together.
[00:31:12 - 00:31:13] Cool.
[00:31:13 - 00:31:14] Cool, cool, cool.
[00:31:14 - 00:31:16] So if you've got an answer, there's going to be good.
[00:31:16 - 00:31:20] You can either like pat yourself in the back and tell you stuff you did a good job.
[00:31:20 - 00:31:25] So what I've got here is a nice little way that I would probably lay it out.
[00:31:25 - 00:31:28] So I'm known as that the force is going to be what?
[00:31:28 - 00:31:37] Two ton, which is approximately 2,000 kg, which would be,
[00:31:37 - 00:31:39] I'm going to be real crude.
[00:31:39 - 00:31:42] I know I'd be not crude, 9.81.
[00:31:42 - 00:31:45] We'll give us the number of newtons.
[00:31:45 - 00:31:46] All right.
[00:31:46 - 00:31:47] So use gravity as that.
[00:31:47 - 00:31:57] Material, we've said was mild steel and yield stress.
[00:31:57 - 00:32:01] We said was 200 megapascals, all right.
[00:32:01 - 00:32:10] So anyone who has actually started the question, did you get a number of millimeters?
[00:32:10 - 00:32:11] No?
[00:32:11 - 00:32:12] No one's done it.
[00:32:12 - 00:32:15] Surely you've had a...
[00:32:15 - 00:32:16] I know someone's done it.
[00:32:16 - 00:32:18] That's a big shy.
[00:32:18 - 00:32:20] We've got four sort of area, right?
[00:32:20 - 00:32:22] And you guys know that area of a circle, so you would have been out of it.
[00:32:22 - 00:32:23] And I'll do it.
[00:32:23 - 00:32:25] But I'm sure that you really...
[00:32:25 - 00:32:28] I'm really sure that someone has done this, but that's right.
[00:32:28 - 00:32:34] So our question is to define bar size needed, right?
[00:32:34 - 00:32:38] So our sketch, we can just draw.
[00:32:38 - 00:32:39] I don't know.
[00:32:39 - 00:32:46] Imagine that this is our bar, and it's going to be well that I guess to some two ton.
[00:32:46 - 00:32:51] Lock and for now we're not really too interested in terms of actually the manufacturing here.
[00:32:51 - 00:32:56] We're just going to do a crude assumption to work out what's happening kind of here.
[00:32:56 - 00:32:57] Right?
[00:32:57 - 00:33:03] So I'm sort of just going to do a really simplified calculation of shipping that all of the load
[00:33:03 - 00:33:07] is just going through a bar of some size, right?
[00:33:07 - 00:33:10] Some radius there, yeah?
[00:33:10 - 00:33:11] Cool.
[00:33:11 - 00:33:13] So working what's the formula for stress?
[00:33:13 - 00:33:19] I know you're asking an answer.
[00:33:19 - 00:33:20] You can do it.
[00:33:20 - 00:33:21] I believe in you.
[00:33:21 - 00:33:22] Nice.
[00:33:22 - 00:33:23] A plus.
[00:33:23 - 00:33:24] Cool.
[00:33:24 - 00:33:39] And so we know that the force is 2000 kg times 9.81 nudens per kg all over our area, which should be pi r squared, yeah?
[00:33:39 - 00:33:48] And so if we do some rearranging, we should get r on the side and then we square root it, and then it's pretty much the same thing, right?
[00:33:48 - 00:33:59] So we're going to do 2000 kg times 9.81 nudens per kg all over stress, right?
[00:33:59 - 00:34:07] Which would be 200 megapascals times pi.
[00:34:07 - 00:34:08] Yeah?
[00:34:08 - 00:34:15] Do you want agreeing with that very quick rearrangement?
[00:34:15 - 00:34:18] Does anyone done, punched in the calculator?
[00:34:18 - 00:34:30] Yeah, 5.6 or 5.59 if we really wanted to go to 2DP?
[00:34:30 - 00:34:31] Cool.
[00:34:31 - 00:34:36] So diameter we just times by 2, right?
[00:34:36 - 00:34:39] So it's like a 11.18.
[00:34:39 - 00:34:41] So we just say that to that workshop eight.
[00:34:41 - 00:34:44] We just cooled 20 back, like Tony, we've got it.
[00:34:44 - 00:34:47] You want a 11.8 millimeter bar?
[00:34:47 - 00:34:49] Yeah?
[00:34:49 - 00:34:50] No?
[00:34:50 - 00:34:52] So I heard some good murmurs.
[00:34:52 - 00:34:59] So one thing is, would we ask for this bar size or would we just go up to the next preferred or standard size?
[00:34:59 - 00:35:00] Yep.
[00:35:00 - 00:35:07] So we could say 12 millimeters would be slightly better, but someone else already told me what is wrong with what we just did there.
[00:35:07 - 00:35:09] The factor is safety, right?
[00:35:09 - 00:35:12] So what is the factor of safety of this?
[00:35:12 - 00:35:13] Yeah.
[00:35:13 - 00:35:19] So this is like four a factor of safety of approximately one.
[00:35:19 - 00:35:20] Yeah?
[00:35:20 - 00:35:23] So I mean, technically it could work.
[00:35:23 - 00:35:25] I mean, we've gone slightly above.
[00:35:25 - 00:35:26] Right?
[00:35:26 - 00:35:28] So it's going to be slightly over one.
[00:35:28 - 00:35:33] So as long as you lift it very, very carefully, it's going to be fine and not yield, right?
[00:35:33 - 00:35:42] But there's probably a little bit not so acceptable for avoiding as opposed to workplace health and safety incidents, right?
[00:35:42 - 00:35:55] So if we just make a little note here, our factor of safety is normally defined as your yield over the actual stress that's in your part, right?
[00:35:55 - 00:36:01] And so to work out the factor of safety that we would, what factor of safety might be one?
[00:36:01 - 00:36:02] Safe it was three.
[00:36:02 - 00:36:07] Then realistically what we're going to do is divide this number here by three.
[00:36:07 - 00:36:10] And now working right, then now I make everything bigger.
[00:36:10 - 00:36:14] So we've got to be a little bit because it's got the squared relationship.
[00:36:14 - 00:36:20] It's kind of, if you just times the diode of I3 that you're going to get a real massive factor of safety, right?
[00:36:20 - 00:36:33] So ideally you would, I'm just going to write, do kelp again using I know, Sigma y equals
[00:36:33 - 00:36:42] or Sigma or stress equals a third.
[00:36:42 - 00:36:43] Yeah?
[00:36:43 - 00:36:46] So there we give her four.
[00:36:46 - 00:36:51] Here's some approximately three.
[00:36:51 - 00:36:57] Go and then I'm just for completeness, we would also need to make a comment once you had done that,
[00:36:57 - 00:36:59] just because we're kind of short on time.
[00:36:59 - 00:37:02] So yeah, I mean, I'll write a comment.
[00:37:02 - 00:37:21] I'll say the current kelp gives a 12 millimeter bar required for sector of safety of,
[00:37:21 - 00:37:25] yep, obviously right, do it in its kelp.
[00:37:25 - 00:37:26] Cool.
[00:37:26 - 00:37:31] So with that, do we have any other ideas?
[00:37:31 - 00:37:41] Do we think that this method, I suppose, of actually welding our bar to our block is the best way to do it?
[00:37:41 - 00:37:43] See some people shaking their head.
[00:37:43 - 00:37:50] What could be a bita or simpler way to use instead of possibly having a round bar?
[00:37:50 - 00:37:55] So maybe this is our block.
[00:37:55 - 00:37:56] Do we have a block?
[00:37:56 - 00:37:59] Any other ideas there might be bita?
[00:37:59 - 00:38:03] Well, lifting lug, yeah.
[00:38:03 - 00:38:08] With a lifting lug, which could be put slightly more simply is just being like a bit of flat bar.
[00:38:08 - 00:38:14] It's a crude way of having a lifting lug with like a hole or something punched through it, right?
[00:38:14 - 00:38:17] So what we want.
[00:38:17 - 00:38:21] So if you're welding circular bar, I don't know how good you are routing.
[00:38:21 - 00:38:24] I'm pretty average and done it for a wee while.
[00:38:24 - 00:38:28] But can be a bit of a pain to get around the corner and doing a really nice weld.
[00:38:28 - 00:38:31] It's way easier to weld in straight lines.
[00:38:31 - 00:38:35] So you can imagine that if you had this bar here and it was kind of relatively slick,
[00:38:35 - 00:38:38] then you could just do a full-out weld all the way around.
[00:38:38 - 00:38:41] You get way big of a full-out weld area which is going to be good for the stress in your weld,
[00:38:41 - 00:38:46] which is something that we end up learning how to calculate in 3-1-1.
[00:38:46 - 00:38:51] Yeah, there would be ideally a bit of solution, but it's like, again, one of those things,
[00:38:51 - 00:38:54] if you just get told calculate the size of the bar,
[00:38:54 - 00:38:56] you don't say, hang on, why do you actually need a bar?
[00:38:56 - 00:38:58] Would something else be more appropriate, right?
[00:38:58 - 00:39:05] So just kind of looping it back into those kind of initial discussions around how it's important
[00:39:05 - 00:39:10] to define your specifications on your part before you kind of go through and propose a solution.
[00:39:10 - 00:39:11] Cool.
[00:39:11 - 00:39:16] Did anyone plug in the number for when it was a factor?
[00:39:16 - 00:39:20] When you put the stress in as a third of the stress?
[00:39:20 - 00:39:22] 90.4?
[00:39:22 - 00:39:23] 19.4.
[00:39:23 - 00:39:27] Okay, so we can actually just update and say,
[00:39:27 - 00:39:38] so I don't know, this is the answer as 20 millimeter would give.
[00:39:38 - 00:39:42] I think it was safety of approximately three.
[00:39:42 - 00:39:48] So again, 19.4 versus 20, we make sure that we pick the standard kind of preferred size,
[00:39:48 - 00:39:52] which we have slide on at the end of the lecture, kind of showing that.
[00:39:52 - 00:39:57] So as we kind of went through, we went through these kind of steps,
[00:39:57 - 00:40:01] and we talked about the factor, safety and whether it was reasonable.
[00:40:01 - 00:40:05] We were down there for a reality check.
[00:40:05 - 00:40:08] 20 millimeter seems like about right, just intuitively.
[00:40:08 - 00:40:11] It was like 200 millimeter, I'd be like, yeah, that's probably way too big.
[00:40:11 - 00:40:14] And for was two millimeter, it probably would be too small,
[00:40:14 - 00:40:18] but making sure you've got that kind of order of magnitude feeling about right,
[00:40:18 - 00:40:23] which is something that you'll develop as you go through your engineering career.
[00:40:23 - 00:40:28] And then, we call the calculation, so at least consider the term you are actually
[00:40:28 - 00:40:29] dedicating the calculation.
[00:40:29 - 00:40:32] I didn't just pull 20 mill out of nowhere.
[00:40:32 - 00:40:34] Cool.
[00:40:34 - 00:40:35] Sweet.
[00:40:35 - 00:40:41] So in engineering designs are preferred, designs using preferred sizes should be used
[00:40:41 - 00:40:45] to be impossible, as simplifies drawings and reduced manufacturing costs.
[00:40:45 - 00:40:49] And next people like Tony Heppy, suppliers should be consulted
[00:40:49 - 00:40:53] with selecting materials to ensure signs that are chosen are available.
[00:40:53 - 00:40:59] Now, I put that in as like something that I wish one of my funny project groups did like two years ago,
[00:40:59 - 00:41:06] where they didn't call the supplier of the material before they did all the calculations.
[00:41:06 - 00:41:09] So they do the calculations, assuming that this material was available,
[00:41:09 - 00:41:14] then when they got Tony to go order it wasn't available, then they had to redesign and redo all the work that they did,
[00:41:14 - 00:41:16] which they weren't really that stoked about.
[00:41:16 - 00:41:24] And so typically what I would say is if you try to make something that's like just a prototype,
[00:41:24 - 00:41:27] the best material that you can use is the material that is on the shelf,
[00:41:27 - 00:41:29] because you know that it's there and you can use it.
[00:41:29 - 00:41:33] And then the next step, if you're having to get some links and stuff ordered in,
[00:41:33 - 00:41:38] that you definitely make sure that the thing is getting ordered and it's on its way and it's available,
[00:41:38 - 00:41:44] because even though it's in a catalog of the manufacturer, sometimes it won't be stopped item.
[00:41:44 - 00:41:48] So they have to like special order in which can cause delays,
[00:41:48 - 00:41:53] which then ends up costing businesses money when you're unforeseen delays.
[00:41:53 - 00:41:59] So you can see as per the example, don't ask for steel rod with a diameter of 11.28 millimeters,
[00:41:59 - 00:42:03] instead you would pick a preferred size.
[00:42:03 - 00:42:10] So this has actually got kind of slightly more preferred sizes than as kind of typical, maybe.
[00:42:10 - 00:42:14] Some of them will be more preferred than others, I guess as what I'm trying to say.
[00:42:14 - 00:42:19] So you'll probably have experience there when you're kind of selecting drill bits or similar.
[00:42:19 - 00:42:22] It's pretty hard to get like a 6.7 millimeter drill.
[00:42:22 - 00:42:28] And it says, I don't know, a very well used seven millimeter drill, I don't know,
[00:42:28 - 00:42:32] what it's drilling in, whether it's being removed.
[00:42:32 - 00:42:40] So you can see here that as the sizes kind of get bigger, the preferred sizes start to go up in different increments of different millimeters.
[00:42:40 - 00:42:47] So this is something that's probably quite useful for you when it comes to making your aluminium structure,
[00:42:47 - 00:42:51] because obviously you've got things like pins in your stress concentration holes,
[00:42:51 - 00:42:57] and it's kind of going to be hard to calculate, well, it's going to be hard to drill a hole that's not a standard size, right?
[00:42:57 - 00:43:08] So with that, just because I'm, I know, got a bit of a, a whim to discuss this with you.
[00:43:08 - 00:43:15] So imagine that this is our tinsel strip of our aluminium, and we've decided we've done our calculation,
[00:43:15 - 00:43:19] and the hole size, oh, I know.
[00:43:19 - 00:43:24] Someone pick a number for me, feeling uncreative today.
[00:43:24 - 00:43:28] 14. 14. So imagine that a 14 millimeter hole,
[00:43:28 - 00:43:37] that's making something weird if it was, say that it would need it to be 14.1, right?
[00:43:37 - 00:43:44] So say it needed the hole needed to be 14.1 to get the stress, what you needed it to be, right?
[00:43:44 - 00:43:51] There's actually going to be some KV value there for our max, but what I would say is, can we drill a 14.1 mill hole?
[00:43:51 - 00:43:54] So I'm imagining that this is 20, yeah?
[00:43:54 - 00:43:58] I don't know, these are just random numbers that we've put from the crowd, right?
[00:43:58 - 00:44:04] So how could we get the same reduced section either side?
[00:44:04 - 00:44:22] We could drill a 14 mill hole, and then we could file, what would it be, 0.05 millimeter, or each end, right?
[00:44:22 - 00:44:26] And then that way you also know that, because the other thing that might happen is like,
[00:44:26 - 00:44:32] you make this beautiful 10-style piece, then you drill the hole, and then it's off-center.
[00:44:32 - 00:44:38] And you're like, ah, but if you've purposely got a hole size, that's a standard size,
[00:44:38 - 00:44:43] and maybe smaller than, there's needed, you can give yourself some manufacturing wiggle room to kind of
[00:44:43 - 00:44:46] re-center where that hole would be.
[00:44:46 - 00:44:49] If the hole is kind of what is preferred over a notch.
[00:44:49 - 00:44:55] Personally, I think notches might be easier just because you don't sort of have that issue of that needing to be perfectly in the center.
[00:44:55 - 00:44:58] But that's the other way that you can kind of get around doing that for your hole.
[00:44:58 - 00:45:02] And it kind of refers to preferred sizes.
[00:45:02 - 00:45:03] Cool.
[00:45:03 - 00:45:06] So when we have our hand calculations, we talked about this last week,
[00:45:06 - 00:45:13] we did some example calculations in our tutorials, but they should always kind of follow a clear kind of structure.
[00:45:13 - 00:45:17] That means that they can be interpreted really easily by other people.
[00:45:17 - 00:45:20] So we want to make sure that they have a title sketch, no one's equations.
[00:45:20 - 00:45:25] You've got your working calculator result in an interpretation of what it means or a comment.
[00:45:25 - 00:45:28] And this is what the markers will be looking for when they're marking your assignment.
[00:45:28 - 00:45:32] Making sure that everyone of your calculations follows this same structure.
[00:45:32 - 00:45:38] So you can see here, here's an example of someone calculating a key wave.
[00:45:38 - 00:45:42] And again, we can see that it has each of these things of a title sketch equations.
[00:45:42 - 00:45:44] Some working calculator results.
[00:45:44 - 00:45:47] And then an example of what it means.
[00:45:47 - 00:45:52] And I think last week I also added another example calculations,
[00:45:52 - 00:45:54] since people were kind of keen on it.
[00:45:54 - 00:45:57] And we were going to gain a see kind of what someone's done,
[00:45:57 - 00:46:02] what they're calculating and what the kind of main result was from the calculation.
[00:46:02 - 00:46:08] So I'm just going to say, you can see that they worked out what their eye values are.
[00:46:08 - 00:46:13] And then they've worked out what the buckling is for the member.
[00:46:13 - 00:46:19] And they've also done a calculation looking at the buckling of the end,
[00:46:19 - 00:46:24] which is something that we'll touch on this week in the tutorials.
[00:46:24 - 00:46:29] So one improvement could be, as you know, the factor of safety is there,
[00:46:29 - 00:46:34] but this factor of safety is we do a successful, we do another calculation as needed,
[00:46:34 - 00:46:37] much like our kind of calculation that we did.
[00:46:37 - 00:46:45] So in terms of the factors of safety, we saw that it's defined typically by the stress you're allowed.
[00:46:45 - 00:46:47] This is just stress it failure.
[00:46:47 - 00:46:53] And for design engineers most of the time we'll use yield as our failure.
[00:46:53 - 00:46:59] But sometimes you might use not yield, so that's why we've used this notation here.
[00:46:59 - 00:47:04] So in general, it's a good idea to use factors that define in standards.
[00:47:04 - 00:47:11] And if you don't have a standard for the exact situation to use one that is of similar kind of situation,
[00:47:11 - 00:47:17] use factors that are set up by your organization or by engineering handbooks for your design situation.
[00:47:17 - 00:47:22] So basically, what does this saying is use a reference source to define what your factor of safety is,
[00:47:22 - 00:47:29] unless, I guess, you're the expert in kind of come up with that factor of safety.
[00:47:29 - 00:47:34] And where possible use personal judgment when you're experienced enough.
[00:47:34 - 00:47:38] So to give you a given when you're using factors of safety that you do not allow them to stack,
[00:47:38 - 00:47:42] you should not have factors of safety on factors of safety, which is easy to do,
[00:47:42 - 00:47:47] especially if you're using that equation where you put just the factor of safety on the stress,
[00:47:47 - 00:47:52] and then you don't realize that they might already be the factor of safety kind of in here.
[00:47:52 - 00:47:57] So what we see here from Blochman is that there's a range of different factors of safety.
[00:47:57 - 00:48:04] And you can see that for really well, no unreliable materials under controllable conditions,
[00:48:04 - 00:48:12] you can have low factors of safety, but more generally you'll have factors of safety that are at least 2-4,
[00:48:12 - 00:48:18] depending on what you know about the load conditions.
[00:48:18 - 00:48:25] And so with that, before we talk about load factors, which will only take a hot minute, I guess,
[00:48:25 - 00:48:32] everyone here has done enemy 202, and I'm not sure if the notebooks have changed, this one from 2014.
[00:48:32 - 00:48:37] Hopefully you've seen some sort of table that looks like this before, right?
[00:48:37 - 00:48:43] Yeah, and it kind of, it's a point that I've got on the slides or that Blochman's got on the slides,
[00:48:43 - 00:48:52] but a lot simpler, so we can see here, as our cost or failure increases,
[00:48:52 - 00:49:00] so does our factor of safety, and as our level of confidence, our no one's about the material properties,
[00:49:00 - 00:49:04] increase our factor of safety decreases, right?
[00:49:04 - 00:49:10] And so we get this zone here where we can have those low factors of safety, and we have these zones here,
[00:49:10 - 00:49:17] because it's either going to be caused death, close to people end to the business.
[00:49:17 - 00:49:25] Probably you shouldn't be building things that have those kind of consequences where you're designing something that you don't know anything about the material.
[00:49:25 - 00:49:27] Often people aren't.
[00:49:27 - 00:49:30] This can be a useful reference for your non-fatalier members.
[00:49:30 - 00:49:34] I'll just make sure that that was shown in both screens quickly.
[00:49:34 - 00:49:36] Okay, so it wasn't online.
[00:49:36 - 00:49:42] Basically, this was just showing, you could use this as a reference to pick whether your factors of safety are acceptable
[00:49:42 - 00:49:46] for your aluminium structure, because you're the E-N-A, you're the kind of boss.
[00:49:46 - 00:49:49] So the last thing that we want to talk about is the low factors.
[00:49:49 - 00:49:52] These will sometimes be applied in equations.
[00:49:52 - 00:49:55] We don't just have a solid standard load being applied.
[00:49:55 - 00:49:57] There might be some kind of impact factor.
[00:49:57 - 00:50:02] That means that the peak load is actually more than what the load would be.
[00:50:02 - 00:50:08] So we'll ample if we have amber is here standing on this diving board.
[00:50:08 - 00:50:10] We've got a 7-TKG load.
[00:50:10 - 00:50:13] As soon as you go to the jump, then we're getting a load factor,
[00:50:13 - 00:50:18] which might be upwards of twice what is actual mass would be.
[00:50:18 - 00:50:23] So what we'll see is that in some of our equations that we use with things like shaft design,
[00:50:23 - 00:50:25] depending on the conditions that they are operating in,
[00:50:25 - 00:50:29] we would apply a load factor that's being defined to our loads.
[00:50:29 - 00:50:33] And that's slightly different to this factor of safety, which you get at the E-N's,
[00:50:33 - 00:50:36] comparing your actual stress to the failure stress.
[00:50:36 - 00:50:38] Thanks for your all seeing this afternoon.
[00:50:38 - 00:51:15] Thanks.
[00:52:09 - 00:52:11] Thank you.
[00:52:39 - 00:52:41] Thank you.
[00:53:09 - 00:53:11] Thank you.
[00:53:39 - 00:53:41] Thank you.
[00:54:09 - 00:54:11] Thank you.
[00:54:11 - 00:54:15] Thank you.
[00:54:15 - 00:54:17] Thank you.
[00:54:47 - 00:54:54] .

# ENMT301-26W Lecture 31 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_31_audio_16k_mono_32k.mp3`
Source audio SHA-256: `bf3f956baf12ac47077f1b76513d7d084804d958ed044e20f0b929dc7b4a738f`
Generated: 2026-06-06T06:13:52.922885+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:03 - 00:00:06] Alright, thanks everyone. We'll make a start there.
[00:00:06 - 00:00:21] So obviously last week was a big week,
[00:00:21 - 00:00:23] because I'm sure this week is also a big week for you.
[00:00:23 - 00:00:30] It's a time of big weeks I suppose, but firstly, Cara, where?
[00:00:30 - 00:00:33] Excellent work on getting a Summit 1A in.
[00:00:33 - 00:00:37] I'm sure that you know, I think about some of the things
[00:00:37 - 00:00:41] that we talked about in tutorials and hopefully you've got a nice design
[00:00:41 - 00:00:46] ready to start kind of again building season I suppose.
[00:00:46 - 00:00:56] So, Blue and Re
[00:00:56 - 00:00:59] and I suppose, you know, remember to glue things on the workbenches,
[00:00:59 - 00:01:05] not on the windowsills or other horizontal sifsters.
[00:01:05 - 00:01:11] And we will get a kind of test schedule developed.
[00:01:11 - 00:01:14] So this is sort of a bit of a manual sort of process just because
[00:01:14 - 00:01:17] people have different kind of labs and different spaces.
[00:01:17 - 00:01:19] But now you've done the Summit 1A.
[00:01:19 - 00:01:21] I know who your partner is so we can kind of make sure that
[00:01:21 - 00:01:24] there'll be a time in week 8 that will suit both you.
[00:01:24 - 00:01:28] So this won't be something that's like automatically put in your timetable.
[00:01:28 - 00:01:30] It'll be a PDF that's uploaded on learn.
[00:01:30 - 00:01:34] You can see when your test time is during week 8.
[00:01:34 - 00:01:38] So what information you can't suppose on that?
[00:01:38 - 00:01:41] Other notices, the Summit 2 will be released later today.
[00:01:41 - 00:01:44] We'll talk about it during the tutorial just to make sure that, you know,
[00:01:44 - 00:01:50] if you really want to get stuck in and get things done early before next term
[00:01:50 - 00:01:55] gets really busy, then you'll have the opportunity to kind of get started on that.
[00:01:55 - 00:02:00] And we'll talk about, you know, what kind of approach might be useful to take
[00:02:00 - 00:02:05] to step through the assignment in a way that's not too iterative.
[00:02:05 - 00:02:11] So I think the classic thing that happened last year was we're having a bearing
[00:02:11 - 00:02:14] and then we have the end of our shaft.
[00:02:14 - 00:02:15] And that's kind of in our design here.
[00:02:15 - 00:02:17] I know I'm sort of skipping ahead.
[00:02:17 - 00:02:22] But my one, I suppose, thing to remember would be if and doubt when you're first
[00:02:22 - 00:02:27] starting, make that slightly longer than you think it needs to be.
[00:02:27 - 00:02:30] Because last year what they had is I think a lot of people sort of went a bit
[00:02:30 - 00:02:32] on the lean side and then they worked out.
[00:02:32 - 00:02:33] They didn't have enough space.
[00:02:33 - 00:02:37] And then because they're making their shaft longer, they felt that they needed to do
[00:02:37 - 00:02:40] all of their free body diagram and their bending moments again.
[00:02:40 - 00:02:42] So basically you have to think about it.
[00:02:42 - 00:02:46] From a designer's point of view, there has to be enough space to get these things
[00:02:46 - 00:02:50] that you haven't designed to be assembled and disassembled.
[00:02:50 - 00:02:52] And so yeah, that would be my little tip for you.
[00:02:52 - 00:02:55] Just if you give yourself a little bit more space than you think you need,
[00:02:55 - 00:03:00] then you definitely won't have to redo the kind of tedious bit of your free body
[00:03:00 - 00:03:03] diagram bending moment, cheerful, spinning, cheerful diagram.
[00:03:04 - 00:03:10] Bill, yeah, we'll go with us in more detail today in the tutorial and there's only one tutorial.
[00:03:10 - 00:03:15] Okay, so if you're normally in the two PM1, feel free to come along to the one PM1.
[00:03:15 - 00:03:20] Obviously it's also recorded, but this is just because last year when I had two,
[00:03:20 - 00:03:23] it was like three people that came to the second one.
[00:03:23 - 00:03:28] And although I do like a great staff to student ratio, seemed like it wasn't the best
[00:03:28 - 00:03:30] use of everyone's time.
[00:03:31 - 00:03:35] I think that if you were in the two PM1, it should have been my remove from your time table and learn.
[00:03:35 - 00:03:40] So that's happened to you and that will explain that.
[00:03:40 - 00:03:41] Cool.
[00:03:41 - 00:03:49] So just before we get into this week's lecture content, the key slide from last lecture is really about these radio lip seals.
[00:03:49 - 00:03:57] These will be most likely the type of seals that you integrate into your bearing housing to make sure that your lubricant
[00:03:57 - 00:04:06] is kept inside and that more share or other kind of contaminants are kept outside of your bearing housing.
[00:04:06 - 00:04:20] So basically the SKF seals catalog or the SKF resources online are a really good source of information to describe what kind of sealers useful for what kind of situation.
[00:04:20 - 00:04:25] And like many engineering things, it's not just going to be one perfect seal.
[00:04:25 - 00:04:37] I mean, statistically maybe it is one perfect seal for your specific design scenario, but there in reality will be a number of seals that are for purpose for your use case.
[00:04:37 - 00:04:47] So basically I'll just follow the guides from these kind of seal manufacturers and pick one that is appropriate for your situation.
[00:04:47 - 00:04:55] And then we see here that the way around that you put the seal is kind of important as opposed in terms of its intended function.
[00:04:55 - 00:05:04] So the one on the left there we can see that this is primarily being mounted to stop contaminants from getting into our bearing housing.
[00:05:04 - 00:05:12] And then thus kind of causing early bearing failure, I guess, by making our lubricant not be able to work properly.
[00:05:12 - 00:05:21] Or if we're trying to make sure that our lubricant is kept inside our bearing housing, what we want to do is have it this way around.
[00:05:21 - 00:05:26] Basically to make sure that our lubricant continues doing its job inside, right?
[00:05:26 - 00:05:34] So you probably want to write in your assignment, I'll put it this way around to do this kind of function, then at least the mark and nose.
[00:05:34 - 00:05:40] Why you've done that rather than like sometimes I see them on the left and right side being the opposite way around.
[00:05:40 - 00:05:44] Which I might seem like people are not sure what it is, right?
[00:05:44 - 00:05:57] So they should probably match and then as we've seen here are times where you have a number of kind of bearings and a number of seals in a certain design.
[00:05:57 - 00:06:01] So this one here we've got our mechanical seal on the inside here.
[00:06:01 - 00:06:07] We've got some labyrinth seals that are sort of forcing things to take the long path.
[00:06:07 - 00:06:10] We have our radial lip seal here and here.
[00:06:10 - 00:06:14] In this case here, if we think about it, what does it try to do in this case?
[00:06:14 - 00:06:18] Keep the lubrication and right? So we've got our two bearings in here and here.
[00:06:18 - 00:06:23] And these are mounted in a way that they're trying to keep the lubrication in.
[00:06:23 - 00:06:31] And then I suppose the other thing that we can sort of see is we've got our coupling to whatever is on the outside here.
[00:06:31 - 00:06:38] Might be some sort of impeller or similar, but we've got something that can be bolted to this section here.
[00:06:38 - 00:06:46] And then we're using this lock nut to actually restrain everything in series here.
[00:06:47 - 00:06:52] So if you think about what's stopping this inner bearing housing from moving,
[00:06:52 - 00:06:56] same thing with this inner bearing race, sorry, here and here.
[00:06:56 - 00:07:07] Then what we've got is these kind of collars that are put in series so that when we tighten this bolt everything from the bolt to the shoulder can't move this in right.
[00:07:07 - 00:07:11] So that is one method that you can do and similar to the idea of me saying,
[00:07:11 - 00:07:15] make sure you leave yourself enough space. Sometimes tools might think,
[00:07:15 - 00:07:19] oh, you know, I don't want to have to have a really long thread along my shaft.
[00:07:19 - 00:07:30] And then have my lock nut. You can put some sort of collar to sort of avoid having to do that kind of annoying addition of thread too far onto your shaft.
[00:07:30 - 00:07:36] So there's lots of examples out there and we see the different kind of seals.
[00:07:36 - 00:07:40] Oh yeah, we're saving an O ring in there.
[00:07:40 - 00:07:51] Cool. So, lecture six, we're going to talk about types of shaft misalignment and then we'll be going over and mainly focusing on our rigid and flexible
[00:07:51 - 00:08:00] couplings as well as universal joints and universal drive lines and then also secondary moments that can occur.
[00:08:00 - 00:08:04] And we do have a universal drive line.
[00:08:04 - 00:08:08] Cool connections to shafts. We've already talked about our keyways.
[00:08:08 - 00:08:19] So all sorts of emphasizes, re-emphasize some of the key information around those and then also cover our tape a lot of cut links which we'll see some examples of.
[00:08:19 - 00:08:28] And, depending on if this time we may have a look at some of the resources that has kind of been provided with this lecture.
[00:08:28 - 00:08:33] Cool. So, while cut links needed might be one question that you have.
[00:08:33 - 00:08:38] Often in practical machines, simply it's likely to be there a Lego model.
[00:08:38 - 00:08:40] So there's lots of little bits.
[00:08:40 - 00:08:47] One thing that's always, I suppose, amazed me with Lego is that their tolerances and their precision is actually quite good, right?
[00:08:47 - 00:08:54] However, when we make things in real life, that might not be as good as our legal model or our CAD model online.
[00:08:54 - 00:09:02] So there might be various precision components that have to be connected in a non-precision environment.
[00:09:02 - 00:09:07] So what does that non-precision environment look like? Well, it might look like what we've got on the slide here.
[00:09:07 - 00:09:10] So obviously we have our motor and our pump.
[00:09:10 - 00:09:22] And we want to make sure that those two shafts are aligned such that they don't cause either of those pieces of machinery to fail prematurely due to induced, I suppose, stresses from that misalignment.
[00:09:22 - 00:09:24] Or our shaft to break early, right?
[00:09:24 - 00:09:31] And so, one thing that we could do, if we really wanted to make sure that it was in a precise location,
[00:09:31 - 00:09:41] is we could get a ginormous slab of steel, get the most expensive CNC machine that we've got, and very precisely make sure it's perfectly in the level that it needs to be,
[00:09:41 - 00:09:45] and that all of the mounting holes are perfectly where they need to be, right?
[00:09:45 - 00:09:51] That would be one solution to get these two components and the shafts of those two components are lined perfectly,
[00:09:51 - 00:09:55] such that we wouldn't really need to have any fancy coupling in between them, right?
[00:09:55 - 00:09:57] We could just connect them and it would be happy.
[00:09:57 - 00:10:01] But obviously the problem of that is it's very costly to do that.
[00:10:01 - 00:10:12] And so what we see is a lot simpler and cheaper option is to have this piece of folded sheet metal or steel plate to make a skid,
[00:10:12 - 00:10:17] and then that is on some concrete, which is at the best of times, okay?
[00:10:17 - 00:10:24] I don't know if anyone's had much experience with concrete, but it's only once you realise you can't really change it that you realise it's probably not perfect, right?
[00:10:24 - 00:10:38] And so what we do to remedy this kind of non-precision environment that we have made is to have some sort of coupling that can deal with whatever misalignment there is in the shaft, whether that be axial,
[00:10:38 - 00:10:44] whether it's not collinear, whether there's some sort of angular misalignment, and we'll see that there.
[00:10:44 - 00:10:46] So we can see here.
[00:10:46 - 00:10:50] Generally, we might have cheat mounts, if it is in those mounts,
[00:10:50 - 00:10:54] we might have distorted base frames, which we'll see an example of soon.
[00:10:54 - 00:10:59] There may be vibration in our components, which our coupling might be able to provide some dampening for.
[00:10:59 - 00:11:13] And then we may also want to then have flexible mountings or rubber mounts, also to control vibration in our machinery to make sure that they don't go too crazy.
[00:11:13 - 00:11:21] Yeah. Cool. So obviously the key word I suppose is slightly if things are just completely misalignment,
[00:11:21 - 00:11:25] sometimes there will be a point of no change here.
[00:11:25 - 00:11:32] So one other example that we see here is a motor and one retrieval system for the bin-nivist bungee jump.
[00:11:32 - 00:11:37] Has anyone done that bungee jump? Anyone bungee jump before?
[00:11:37 - 00:11:44] Maybe like, I don't know how many people are in here. Maybe we've got like 2% bungee jumping.
[00:11:44 - 00:11:46] One day maybe I'll do it.
[00:11:46 - 00:11:56] But what we see here is that this component that we see in here, we have this center-flix coupling type 112.
[00:11:56 - 00:12:04] And what it is doing is connecting our electric motor to our winch so that when you've done your bungee jump,
[00:12:04 - 00:12:08] then you can be retrieved and hauled back up.
[00:12:08 - 00:12:14] And so this is your classic case of a welded component.
[00:12:14 - 00:12:22] So this frame that's holding everything together would be welded together and that would cause some amount of distortions that you wouldn't have.
[00:12:22 - 00:12:25] We're your mounting perfectly aligned, right?
[00:12:25 - 00:12:29] And so what we have is a center-flix coupling to remedy that.
[00:12:29 - 00:12:35] If we look at the document camera here is a version of a center-flix coupling.
[00:12:35 - 00:12:37] This one here is size 8.
[00:12:37 - 00:12:40] But what we can see is that you would have one input shaft here.
[00:12:40 - 00:12:43] It has some sort of coupling on the other side.
[00:12:43 - 00:12:45] Obviously the holes aren't very aligning there.
[00:12:45 - 00:12:56] And then the flexible nature of this elastomer will mean that it can deal with some amount of shaft misalignment in your system.
[00:12:56 - 00:13:10] So here we see the example, the reason for this example is the well-known spring-free champerline
[00:13:10 - 00:13:13] treeator, Keith Alexander.
[00:13:13 - 00:13:19] This was one of his patents that he actually, you know, he painted it the design that we sort of saw there.
[00:13:19 - 00:13:25] And then this is how my spows and the sun testing the said device, right?
[00:13:25 - 00:13:27] Just a nice stir.
[00:13:27 - 00:13:30] It should be for those who have gone before me.
[00:13:30 - 00:13:32] So types of shaft misalignment.
[00:13:32 - 00:13:42] What we can see here is, as we sort of talked about, we may have some axial misalignment where our shafts are not possibly where exactly we wanted them to be.
[00:13:42 - 00:13:49] There may be some parallel offset alignment where our two shafts are not collinear.
[00:13:49 - 00:13:57] We also may have some angular misalignment, and this can be both symmetrical or asymmetrical.
[00:13:57 - 00:14:03] So we see those just define there in nice, clear detail.
[00:14:03 - 00:14:04] Cool.
[00:14:04 - 00:14:09] And then we also may have cutblings that enable some torsional flexibility.
[00:14:09 - 00:14:12] So I think we have one of these big, heavy ones here.
[00:14:12 - 00:14:13] Whoops.
[00:14:13 - 00:14:16] So we'll show that on this.
[00:14:16 - 00:14:24] So we see there that in this case here, what we have is a mounting plate on the outside.
[00:14:24 - 00:14:27] And then obviously a shaft that goes on the inside.
[00:14:27 - 00:14:45] And then we have some less demeric elements that provide some amount of flexibility in our system, which can be kind of useful if we got really sharp kind of input or output characteristics in our system.
[00:14:45 - 00:14:58] So to try and reduce those impact loads and those load factors that we have seen in our shaft design calculations, we can use a coupling that has some torsional flexibility as well.
[00:14:58 - 00:15:06] So here we see from S.K.F a list of functions that couplings will provide.
[00:15:06 - 00:15:12] And the top three ones, I suppose, the three kind of maintenance iterations that I would recommend.
[00:15:12 - 00:15:18] So obviously we've got to size a coupling such that it can actually transmit the torque that is required.
[00:15:18 - 00:15:27] And we also have to pick one that's going to be acceptable for the amount of shaft misalignment that we might expect in our design scenario.
[00:15:27 - 00:15:31] And it also has to be allowance for easy, assembly and discipline.
[00:15:31 - 00:15:41] So we've got some further things here, such as allowing some dampening or dim or expansion or appropriate amount of rigidity.
[00:15:41 - 00:15:47] But we'll see that those things are sort of taken into account when you select them.
[00:15:47 - 00:15:54] So the top three ones would be what I've focused on for now or to try and make sure that we're happy with if someone is at our staffs.
[00:15:54 - 00:16:03] Maybe at the dinner table over, I don't know if that might really be going like, why would you use a different coupling?
[00:16:03 - 00:16:06] I need to transmit power or whatever.
[00:16:06 - 00:16:13] Cool. So what we see here is rigid couplings are the first kind of coupling that you may use.
[00:16:13 - 00:16:18] And the idea with these is you have to make sure that the shaft will be co-linear.
[00:16:18 - 00:16:25] Because if you don't have the shaft being co-linear, then it's impossible to get that rigid coupling on.
[00:16:25 - 00:16:28] So there may be some misalignment in your system.
[00:16:28 - 00:16:36] And because your coupling is rigid, if your shaft is very stiff, then this will cause an early amount of failure.
[00:16:36 - 00:16:45] And so because of this, you'll often see rigid couplings used in scenarios where there are long unsupported sections of shafts.
[00:16:45 - 00:16:56] And so that those uncooled decisions can provide the necessary flexibility in your system to make sure that misalignment is manageable.
[00:16:56 - 00:16:59] And so here we see some examples of those there.
[00:16:59 - 00:17:04] So we've got our two shafts and then our two, each is of our rigid coupling.
[00:17:04 - 00:17:09] And our fixed in place with some number of bolts.
[00:17:09 - 00:17:20] And you can see that you also have ones that have some sort of tapered geometry so you can reduce the way that you can reduce the number of parts that you kind of need.
[00:17:20 - 00:17:30] So those sort of slide together, again, got many different kind of examples of how those couplings go together.
[00:17:30 - 00:17:36] So you can kind of follow the same principle of two rigid components that connect each of your shafts.
[00:17:36 - 00:17:47] One thing that's kind of not shown here in all of these is that a lot of the time, those couplings may have some sort of keyway or similar in your system, right?
[00:17:47 - 00:17:50] So what's not shown in the cross-section is that little cutaway.
[00:17:50 - 00:17:54] So there might be a keyway that goes to make sure that that torque is transmitted.
[00:17:54 - 00:18:02] So obviously if there's no keyway and you just had this loosely around your shaft, then it would be causing us both.
[00:18:02 - 00:18:03] Mass builds up for heat.
[00:18:03 - 00:18:10] So I'll start passing some of these things around so that they get to see the light of day that they've deserved.
[00:18:10 - 00:18:21] So a good example of where these kind of rigid couplings are used are in the line shafts of wool spinning machines.
[00:18:21 - 00:18:31] And so what we can see in there is that we have these kind of long shafts and then we have these foots or rigid couplings in between those long shafts.
[00:18:31 - 00:18:39] Now, the flexibility in the system that we can see is we have some amount of flexibility by having the shaft being long and slender.
[00:18:39 - 00:18:47] And then also because we have belts, if anything was to go really badly for the system or one of the wool machines was to jam and the other ones weren't.
[00:18:47 - 00:18:51] And the belt is going to enable the system to slip.
[00:18:51 - 00:18:59] So you can see that there's sort of a gun that's being built kind of into that system inherently.
[00:18:59 - 00:19:05] So then we've got flexible couplings and for flexible couplings is kind of two types.
[00:19:05 - 00:19:12] So there's ones that have resilient elements made of either rubber or less than one that are made from metal.
[00:19:12 - 00:19:20] And so we've got a design in a way that there is some flexibility provided in the coupling itself.
[00:19:20 - 00:19:22] So for these are less demerit couplings.
[00:19:22 - 00:19:31] The amount of flexing and resilience is obviously dependent on the elements that are in the coupling itself.
[00:19:31 - 00:19:39] And so if we have too much flex, in fact that's still not going to be a good thing because that's going to mean that our less demerit,
[00:19:39 - 00:19:43] will heat up and our system will kind of fail earlier.
[00:19:43 - 00:19:55] So in all these kind of couplings, they'll often be operating constraints that are provided by the manufacturer to make sure that you don't have premature failure.
[00:19:55 - 00:20:10] So obviously we also have to just make a note here of if we get that hardness or flexibility of our coupling wrong that this can contribute to machine resonance or vibration problems.
[00:20:10 - 00:20:19] And we see an example of a coupling failure that has resulted in a failure.
[00:20:19 - 00:20:23] So here we see it's a 700 kilowatt flexible coupling which is shredding.
[00:20:23 - 00:20:29] You can see these strands shredding everywhere.
[00:20:29 - 00:20:38] And this was caused by torsional vibrations in the system which ended up shutting down one of the milk plants.
[00:20:38 - 00:20:52] And peak milk during 2008. So it was kind of crisis front page news sort of stuff and it was all because some engineer had not necessarily understood the system that they were designing for.
[00:20:52 - 00:21:04] So obviously it was remedied eventually but just a nice example that shows that doing these things kind of incorrectly in industry can cause quite a big financial burden on the person who owns the machinery.
[00:21:04 - 00:21:08] And so there are a range of different types of couplings.
[00:21:08 - 00:21:15] We've got these kind of spider ones that we see here and we have some examples that we can show and pass around.
[00:21:15 - 00:21:28] So obviously they come in a range of sizes and we have these kind of elements in the middle which can be replaced if required or changed if you wanted a slightly different amount of flexibility in your system.
[00:21:28 - 00:21:39] Now in this case here we have this grub screw on each of our hulls of our coupling which will enable us to kind of attach to our shaft.
[00:21:39 - 00:21:49] So these wouldn't be used for super high torque kind of situations but that grub screw is what kind of stops the coupling from being out of sliver it was.
[00:21:49 - 00:22:00] And you can kind of inherently see here that there is some amount of flexibility that would be provided if the shaft was slightly misaligned.
[00:22:00 - 00:22:18] We also see ones similarly that might have an element that looks more like this shape on the slide we saw that there are a range of different shapes for these spider type couplings and we'll see a few more examples of those in the bearing.
[00:22:18 - 00:22:25] And the catalogs from the manufacturers.
[00:22:25 - 00:22:34] So then we see some further examples where we might have bonded rubber discs, we might have rubber inserts inside of our coupling.
[00:22:34 - 00:22:39] All we might have these kind of cushioned sleeve ones which I believe were part.
[00:22:39 - 00:22:44] I think that's what is actually shown in the example of the failed coupling.
[00:22:44 - 00:22:50] As you can see that we just have this sleeve I think it is actually a sleeve somewhere.
[00:22:50 - 00:23:00] Here's an example I suppose of a sleeve for a coupling that can provide that kind of flexibility in your system.
[00:23:00 - 00:23:04] As you can see lots of people have come up with lots of innovative designs for these sort of things.
[00:23:04 - 00:23:19] So we see again ones that have either flanges or similar and just kind of highlighting that there are a wide variety I suppose of these kind of styles of flexible couplings.
[00:23:19 - 00:23:28] So often companies will have a signature ones that they are more well known for.
[00:23:28 - 00:23:41] Cool. There are also some types such as the power stream which allow for replacement of your resilient elements without having to remove the coupling hubs.
[00:23:41 - 00:23:49] So again just talking to that idea of making sure that when you design machinery you thought about how it's going to be maintained in the symbol.
[00:23:49 - 00:23:54] And what we can see here I don't know how often this gets pulled apart.
[00:23:54 - 00:24:04] But what we can see is that the idea would be that a thieves to blue elements attached to your driving and driven shaft.
[00:24:04 - 00:24:11] Well what we can do is we don't have to take the whole thing away or pull it apart to replace the elements.
[00:24:11 - 00:24:26] What we can do is just slide that sleeve off which I slid off so easily and then you can pull apart this part here and replace it without having to have a lot of disassembly in your entire system.
[00:24:26 - 00:24:31] So I'll just pass those around as well.
[00:24:31 - 00:24:54] So the idea is that it's main selling point is like you don't need these extra fasteners or extra tools or time to get your machine back and operating after its maintenance has been done.
[00:24:54 - 00:24:55] Cool.
[00:24:55 - 00:25:02] Then the other type of flexible couplings that we kind of mentioned are these metal component ones.
[00:25:02 - 00:25:08] So we can have a slider block which works relatively similar to the idea about spider couplings.
[00:25:08 - 00:25:16] We can have these flexible metal couplings that have a slitter or spiral that's been kind of cut into them.
[00:25:16 - 00:25:20] You often see these I suppose in sort of smaller devices.
[00:25:20 - 00:25:25] We've used them in the past when we've had it wheeled here, dyno.
[00:25:25 - 00:25:31] There was measuring, when we were measuring the power from our dyno.
[00:25:31 - 00:25:38] We had a coupling like this that was attached to that system to make sure that we can measure the rotations.
[00:25:38 - 00:25:42] So it was attached to the shaft that was doing the instrumentation.
[00:25:42 - 00:25:47] And then also we have these double roller chain and gear couplings.
[00:25:47 - 00:25:52] Some of these can be quite useful because they are good and I suppose do the environments.
[00:25:52 - 00:25:59] And especially if you have kind of higher load carrying requirements.
[00:25:59 - 00:26:04] So again here we see an example of the chain.
[00:26:04 - 00:26:07] And we can see again by kind of playing with it.
[00:26:07 - 00:26:21] You can see that kind of amount of misalignment both actually and also in terms of angular that this would be able to kind of deal with.
[00:26:21 - 00:26:22] Cool.
[00:26:22 - 00:26:28] It's like Christmas, right?
[00:26:28 - 00:26:31] Giving given all these things and past around.
[00:26:31 - 00:26:47] So the next things that we're talking about here I suppose are our flexible couplings that you may or may not be familiar with.
[00:26:47 - 00:26:55] So a constant velocity joint or a CV joint is a classic thing I suppose to go wrong in your car.
[00:26:55 - 00:26:58] You don't ever have your CV joint fail.
[00:26:58 - 00:27:04] So that's this thing and the idea, I know it's sort of cryptic.
[00:27:04 - 00:27:08] Scripting the name, you know sometimes engineers don't like to do a good job of it.
[00:27:08 - 00:27:22] But the idea is that for these types of flexible couplings the input shaft is going to be driven at the same speed or there will go at the same speed as the output shaft.
[00:27:22 - 00:27:26] So that's why they call it a constant velocity joint.
[00:27:26 - 00:27:38] And what we normally have is some sort of ball bearings or similar that enable the force to be transmitted from the driving to the driven shaft.
[00:27:38 - 00:27:51] So when you're inputting the steering, there may be a CV joint that kind of makes sure that the torque is still being transmitted and the velocity is going at the same speed.
[00:27:51 - 00:27:55] So this is quite quite useful.
[00:27:55 - 00:28:02] If you have a scenario where you do need that kind of maintained velocity in your system.
[00:28:02 - 00:28:16] So we do have an example of one of these here so you can see, so again, we can see that as we rotate this one,
[00:28:16 - 00:28:25] that out other side, we'll also rotate and then it's able to operate through a range of different kind of angles.
[00:28:25 - 00:28:32] So useful if you need a change, the angle of the shaft in your system.
[00:28:32 - 00:28:49] Cool. The next sort of similar idea is one called a universal joint or a UJ or a hook joint.
[00:28:49 - 00:28:59] So you haven't had to play with these before. So if you're from a farming background, then I feel like every machinery has something attached to the PTO at the back of the tractor.
[00:28:59 - 00:29:02] And they often have these kind of things.
[00:29:02 - 00:29:08] If you've got a Maurer attachment or similar, then you may have had some experience with these here.
[00:29:08 - 00:29:12] Now in the name, it doesn't say constant velocity.
[00:29:12 - 00:29:27] And as you may guess what I'm about to say, and as shown in the GIF, is that the velocity of our driving and driven shaft is not the same when we have a universal joint.
[00:29:27 - 00:29:39] So the universal joint is just one of these. And we'll see you often use them in peers to try and remedy some of this kind of a...
[00:29:39 - 00:29:48] system property, right? So I'll be a bit annoying if you're like, oh, yo, we've got this sweet car just let us go and drive.
[00:29:48 - 00:29:55] And then this is how the velocity of your driven shaft is going to be constantly getting accelerated and decelerated right.
[00:29:55 - 00:30:07] Wouldn't be good. And so what we can see is that the angle that our system or our universal joint or the angle of our universal joint has a bigger fit,
[00:30:07 - 00:30:13] that's both on that lead and lag or the difference in the velocity of the driven and the driving shaft, right?
[00:30:13 - 00:30:20] So as we get a bigger angle, we get a larger lead and lag on our shaft.
[00:30:20 - 00:30:35] And so this is normally dealt with for not really an issue in practice because you'll see that you would have a pair of universal joints aligned at 90 degrees to each other on an intermediate shaft.
[00:30:35 - 00:30:41] The second joint will cancel the speed change of the first, so the output is a constant velocity.
[00:30:41 - 00:30:45] So provided that the joint angles are the same, nor three shafts are the same.
[00:30:45 - 00:30:48] Are in the same place or in the same plane, sir.
[00:30:48 - 00:30:58] So what we see is that you'll often see that these configurations are used in this universal-drive shaft configuration.
[00:30:58 - 00:31:03] So here we see an example of those universal-drive shaft.
[00:31:03 - 00:31:12] They also have some other names that they go by and often you'll see that they use for these kind of splined ends,
[00:31:12 - 00:31:18] which is, as I sort of alluded to, if you ever had to deal with tractor attachments on the PTO at the back,
[00:31:18 - 00:31:25] then those are how they operate and transmit the torque through the system.
[00:31:25 - 00:31:33] So we'll see that there's two kind of main configurations for our universal drive lines.
[00:31:33 - 00:31:42] So we've got our Z configuration where it kind of looks like a Z, and then we also have a W configuration that can be used.
[00:31:42 - 00:31:55] And so if you have a rear wheel drive car, then it probably has some sort of universal-drive shaft in it to make sure that our torque is going to our back wheels.
[00:31:55 - 00:31:59] And so we see some examples of that there.
[00:31:59 - 00:32:06] So this cross-section here shows that coming out of the transmission, we've got this kind of, in this case, it's a flanged connection.
[00:32:06 - 00:32:10] that attaches our transmission to our rear axle.
[00:32:10 - 00:32:17] And if you look at this one, what kind of configuration would it be if you don't look at this word right here?
[00:32:17 - 00:32:27] I bet you'd see down there we've got our two axis of our shafts being parallel to each other.
[00:32:27 - 00:32:31] And then we've got this intermediate shaft on some angle A.
[00:32:31 - 00:32:45] And impuratively we see the angle A is the same as angle B due to our kind of, you know, year nine or year 10 parallel lines, alternate angles are equal.
[00:32:45 - 00:32:50] So you knew of the use for your math teachers, like you should learn about these things.
[00:32:50 - 00:32:54] And cool. And then we have here an example of our W configuration.
[00:32:54 - 00:32:59] And as we can see in this case, we still have our angle E equaling angle F.
[00:32:59 - 00:33:07] But that means that the angle that our transmission and our rear axle is on is not parallel.
[00:33:07 - 00:33:14] Cool. So you'll see that there is a wide, rasp range of ways that these things can be kind of mounted together.
[00:33:14 - 00:33:19] And so in this case here, we have a few different examples.
[00:33:19 - 00:33:23] Some of them are having splined connections, some of them are having flanged connections.
[00:33:23 - 00:33:35] And then some of them having some flexibility in the system where you can actually change the length of our intermediate shaft by loosening, a component,
[00:33:35 - 00:33:42] and then sliding it along or having some sort of splined connection that has a range of positions where it will operate.
[00:33:42 - 00:33:46] So all you may have a completely kind of fixed shaft.
[00:33:46 - 00:33:49] And so we'll see that here.
[00:33:49 - 00:33:53] Now I'll just try not to yet grease everywhere.
[00:33:53 - 00:33:58] Obviously this is just a universal drive line connection.
[00:33:58 - 00:34:01] And it could be operated in either kind of way.
[00:34:01 - 00:34:07] So we could, if we wanted to have it in a W configuration, where our shaft ends may be like this.
[00:34:07 - 00:34:21] Or we may have it in the z configuration where our two shafts are still parallel to each other, but are in some position that's not in line in the plane that we're seeing here.
[00:34:21 - 00:34:26] Right. So instead of being in line like this, which there's no reason why you can't use a universal drive shaft like that.
[00:34:26 - 00:34:40] But then it also gives you this added flexibility of being able to operate in some unfavorable, typically kind of environments or situations.
[00:34:40 - 00:34:41] Right.
[00:34:41 - 00:34:55] So often these are a practical kind of tool, especially if you have something like your engine or similar slightly away from whatever system you're trying to operate.
[00:34:55 - 00:35:03] Yeah, gives you a way to transmit that tool for your system of that suppose what I'm trying to say.
[00:35:03 - 00:35:05] Cool. So secondary moments.
[00:35:05 - 00:35:13] So because of the fact that we have a angle as the best way to.
[00:35:13 - 00:35:16] So secondary moments that go into a career.
[00:35:16 - 00:35:22] And these are something that are not, I suppose, super intuitive when you use a universal drive shaft.
[00:35:22 - 00:35:35] And what we're going to talk through is about a describe or explain where these kind of forces come from and why they end up bending our shaft in a way that we weren't necessarily intending.
[00:35:35 - 00:35:44] So if we see what I've written here when the universal joint angles are greater than zero oscillating moments are applied to the three shafts as they rotate.
[00:35:44 - 00:35:49] These tend to bend them in a direction perpendicular to the common plane of the shaft.
[00:35:49 - 00:35:57] This applies forces to the support bearings and can cause vibration sometimes called launch shiver.
[00:35:57 - 00:36:04] Each of us is appearing cyclically on the bearings needs to be taken into account in the design.
[00:36:04 - 00:36:13] So obviously the bigger the angle, the bigger the secondary moments are going to be and we'll talk through how you actually calculate these.
[00:36:13 - 00:36:26] here. So just to try and visualize a little bit of what's been written in that what it's saying is that this is our universal drive shaft with an angle of zero.
[00:36:26 - 00:36:33] And our plane, we've got one plane going through, slicing through our system.
[00:36:33 - 00:36:38] And what it's saying is that both of the input and output shards are on that plane.
[00:36:38 - 00:36:51] Now if we have some universal drive line operated like this, what's saying is cyclically a bending moment is going to be applied through up and down.
[00:36:51 - 00:37:01] So we've got our torque going like this and our shaft over here is going to be getting a moment applied, bending it either up and down.
[00:37:01 - 00:37:11] So that's what the wording there where it says about this perpendicular force, so the direction perpendicular to the common plane.
[00:37:11 - 00:37:30] So often the reason that that's important is if you can imagine if we had an engine here and then we had our universal drive shaft attached to something in all of the force, most of the time or commonly a lot of the force will be in that plane that you're seeing there like up and down.
[00:37:30 - 00:37:42] And what this is saying is that there's a force that's going into or side to side, which just makes things slightly less simple if they were all acting in the same plane.
[00:37:42 - 00:37:47] So how do these forces arrive and wires are shafting in?
[00:37:47 - 00:37:53] So what we can see here is a sketch that sort of just shows conceptually what's going on.
[00:37:53 - 00:37:59] It's not exactly representative of what is actually going on but the same kind of principles are applying.
[00:37:59 - 00:38:09] So we see here that we have a plan view in the front view which is of our system.
[00:38:09 - 00:38:12] In this case we've just got a simplified, flexible joint.
[00:38:12 - 00:38:18] And so the idea is that if this is our driving shaft, we have these two yolks.
[00:38:18 - 00:38:28] And in this plane here we can see very clearly that the yoke at the top is pushing at an inner line that is different to the yoke in the bottom.
[00:38:28 - 00:38:40] And so by doing some of our moments in our system, we can see that those are not zero win our yokes are in these two positions here.
[00:38:40 - 00:38:47] So that distance there is what causes this moment that bends our shaft in the other plane.
[00:38:47 - 00:38:57] Hopefully that's sort of a clear enough way to sort of describe it.
[00:38:57 - 00:39:09] It's sort of a little bit confusing that these are the equations that we would use to actually work out what the sizes of these forces would be.
[00:39:09 - 00:39:16] And so just to make it really clear what we can see here is that four hours zid arrangement.
[00:39:16 - 00:39:21] When we have a, what's the best way to describe this?
[00:39:21 - 00:39:30] So as our shaft rotates, we are cyclically going through an angle from zero all the way back to 360, right?
[00:39:30 - 00:39:36] So this angle here as I suppose what this angle here is the angle of the shaft, right?
[00:39:36 - 00:39:46] And so what it's saying is that twice every rotation, the additional force on the bearing which would be perpendicular is zero, which is great, right?
[00:39:46 - 00:39:53] That means that that is not something that we need to calculate because we know that it's not going to be having a negative impact on our system.
[00:39:53 - 00:40:07] However, when our shaft is at angles 9, 10, 270, when our drive shaft yokes look like this, then we get an additional moment that is applied to our system, right?
[00:40:07 - 00:40:11] So that's shown by these two arrows here.
[00:40:11 - 00:40:16] Now this equation here, you can see does not calculate that moment.
[00:40:16 - 00:40:21] You can work it out, but what it gives you is angle A and angle B.
[00:40:21 - 00:40:26] So can you know what is angle A, what is this value A max and B max?
[00:40:26 - 00:40:42] So you can see that we put in our input talk, again, classic engineering, where they've used M for a talk.
[00:40:42 - 00:40:49] Yeah, we put in our angle of our system, we divide it by this length A, which is the length between our bearings.
[00:40:49 - 00:40:53] Like air slight hand. So what are these two things here?
[00:40:53 - 00:41:09] So we can just read it out. Sometimes people get confused about this thing, so I'm trying to explain it in a way that I know that you guys are at least following along.
[00:41:09 - 00:41:10] So what is A and B?
[00:41:10 - 00:41:21] Next load on the bearing. Awesome, yeah? So what it's saying is that because of this moment, it needs to be resolved by two forces at the bearings, right?
[00:41:21 - 00:41:29] And those are just two radial forces and because we have a distance between the bearing and that can force, force times the distance equals a moment.
[00:41:29 - 00:41:37] So that's why we see it's all divided by A, right? And in this case, again, it's very nice that A max is the same as B max, right?
[00:41:37 - 00:41:44] So we can work out that our max moment, where our additional moment would be whatever those values times by A, yeah?
[00:41:44 - 00:41:50] Cool. So that's good. It sounds like we're following along.
[00:41:50 - 00:42:09] So then all we're saying is that if this is our view, this is our side view, right? And often we might have things that are, you know, if we have some sort of thing on our system here, you might have just done your free body diagram for this side view view.
[00:42:09 - 00:42:17] But from our top view, we're getting these additional forces on our bearings, right? So that's that perpendicular thing coming in.
[00:42:17 - 00:42:26] And again, all I'm sort of saying is that when we do our free body diagrams for our summit, we have to clearly go like here's what the sketches of our loads in our system in the front view.
[00:42:26 - 00:42:35] And then here's our sketch in our additional, I suppose, bending moment is shear force diagram of our top view, right?
[00:42:35 - 00:42:40] And then it might be that the max is some angle between them at certain points in our shaft.
[00:42:40 - 00:42:42] Sort of depends on the system.
[00:42:42 - 00:42:48] Cool. So then we see here the same sort of idea for our security moments for the W arrangement.
[00:42:48 - 00:43:04] But in this case, it's a lot more calculation and you have to check both sides and depending on the lengths and the torques and the angles of your system, one scenario, when the angle of the shaft is either this or this.
[00:43:04 - 00:43:07] Maybe a bit because then the other.
[00:43:07 - 00:43:12] Cool. But same kind of idea gives us a formula to give us that additional force on the bearing.
[00:43:12 - 00:43:17] Cool. So in any drive line or coupling arrangement, there isn't issues.
[00:43:17 - 00:43:22] There are issues that need to be checked. There's lots of things like this.
[00:43:22 - 00:43:33] But I guess the main things that I'm sort of talking about is we want to make sure that you guys understand that your misalignment has been sort of adequately, I suppose, cated for.
[00:43:33 - 00:43:40] But this is the complete list and a lot of the time you're sort of doing multiple things at the same time.
[00:43:40 - 00:43:47] So whirling is something that we want really be requiring you to check.
[00:43:47 - 00:43:59] That's when if you have a really long extended shaft, sometimes when it operates, they'll cause it to kind of to whirl, which is a dynamic instability, I suppose.
[00:43:59 - 00:44:06] So normally it's just a check for your system, but again, this is just our completed list.
[00:44:06 - 00:44:12] And we'll make it really clear for your assignment what we expect you guys to kind of consider.
[00:44:12 - 00:44:22] So as we touched on a couple of which was go, there are a number of different types of keys that can be used to both secure elements on the shaft and transmit the torque.
[00:44:22 - 00:44:31] And as we've seen on the things that we've passed around, you can use or have key ways to do this function for your couplings.
[00:44:31 - 00:44:51] And we see that these are those kind of two important slides and calculations that you need to do to make sure that your key or your housing or your shaft are not going to fail either by the key shearing or compressive forces on our shaft or our now coupling or housing or whatever it is.
[00:44:51 - 00:44:58] We also see that there are other ways that we can connect to our shaft such as these kind of tape a lot connections.
[00:44:58 - 00:45:13] These are useful because they're easy to install and remove. Basically you have two grubscrews that you're able to pull or loosen or tighten to either attach or detach to the shaft.
[00:45:13 - 00:45:27] In some cases, they mean that you don't need to have a key, but you'll see that often these kind of systems will still have a key way sort of slot for them and that key way can be different size of it needs to.
[00:45:27 - 00:45:40] But again, we see if we want to we can adjust these bits here and they'll make this gap either increase or decrease in the same sort of idea here where we have still got a key way,
[00:45:40 - 00:45:51] but we can again use these kind of take a lock kind of functions to kind of grip our shaft to make sure that our element has that torque transmitted.
[00:45:51 - 00:46:06] So again here we can see a breakdown of how they're kind of used. So we've got our removal holes that you can use depending on the exact kind of function of your kind of taper.
[00:46:06 - 00:46:20] So this is that summary from SKF and I've sort of highlighted the top three things that your coupling ideally will have taken into account sort of all of these ideas we're appropriate.
[00:46:20 - 00:46:33] And then here is again a summary that kind of just says what is the difference between our less demerit couplings in our metallic couplings and why might you choose one over another?
[00:46:33 - 00:46:49] So generally you'll see there's a lot of different types of flexible couplings anyway and what I would sort of recommend is actually following what the manufacturer kind of recommends for your given situation.
[00:46:49 - 00:47:16] But generally what we can see here is that there are some kind of useful differences I suppose between our metallic couplings generally being stiffer than our less demerit and that our metallic couplings are often used in environments that we need a good resistance to things like a chemical or similar.
[00:47:16 - 00:47:28] So as you'll see here here's an example from the SKF coupling selection book or catalog which I think we have a link on.
[00:47:28 - 00:47:42] And we can see here that for there types of couplings that they have they have given different kind of parameters that will be suitable for the different types of couplings that they have.
[00:47:42 - 00:47:52] They also have these kind of notes to check through to make sure that you don't pick something that is not going to be fit for purpose.
[00:47:52 - 00:48:02] But again here you can see depending on the amount of torque or power or the shaft kind of size those are kind of the things that may be of consideration.
[00:48:02 - 00:48:09] And we can also see here which kind of couplings are best for what which kind of shaft misalignment.
[00:48:09 - 00:48:16] So again here we've got our universal joint which is great if we have big shaft misalignment.
[00:48:16 - 00:48:28] Whereas the next kind of best thing that we see here is our flexible coupling which goes to approximately four degrees of misalignment.
[00:48:28 - 00:48:48] So if you know those sort of parameters or you know what is likely to be the thing that's really tricky in aligning your shafts then these are quite useful to our spokes guard you in what type of what type of coupling is required.
[00:48:48 - 00:49:00] So we see that there's that table there is that same table there and a slight different color and then what you also see is that is KF and other manufacturers I don't have any
[00:49:00 - 00:49:06] hate allegiance to is KF but sometimes just looking at the catalog can be a little bit tricky.
[00:49:06 - 00:49:21] So if you want to learn more about specific types of couplings then they do give a lot more detailed kind of breakdown and information and guides for how you might select those kind of components.
[00:49:21 - 00:49:30] And again is KF does also provide CAD drawings or CAD files of the bearings that they use.
[00:49:30 - 00:49:39] So you can use that in your assignment when you select your bearing don't need to go and draw the bearing that you have selected.
[00:49:39 - 00:49:55] Built so what I'll just touch on very quickly is that we do also have this guide here which has also been included on learn which just talked a little bit more about our universal drive lines in more detail.
[00:49:55 - 00:50:03] So you can see here this is where those bearing load calculations have come from and where those equations have come from.
[00:50:03 - 00:50:35] Cool so I'll see you guys at a tutorial today otherwise thank you very much and have a great holiday if I don't see you.
[00:51:15 - 00:51:19] Thank you.
[00:51:19 - 00:51:23] Thank you.
[00:51:49 - 00:51:56] Thank you.
[00:51:56 - 00:52:17] Thank you.
[00:52:17 - 00:52:24] Thank you.

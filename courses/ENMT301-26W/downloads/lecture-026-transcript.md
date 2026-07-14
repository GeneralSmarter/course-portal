# ENMT301-26W Lecture 26 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_26_audio_16k_mono_32k.mp3`
Source audio SHA-256: `02996105a6cccb59a64e948377b45935afcde1821a49a293dcf31b4f957c9b50`
Generated: 2026-06-06T06:02:49.242762+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:00 - 00:00:04] got something pretty on the screen.
[00:00:04 - 00:00:13] All right.
[00:00:13 - 00:00:16] Is that working? Sounds like it's working.
[00:00:16 - 00:00:34] All right, let's make a start with that.
[00:00:34 - 00:00:38] Thanks everyone. We're going to crack into it so I can ask you questions and then hopefully
[00:00:38 - 00:00:52] a time to kind of float around.
[00:00:52 - 00:00:58] All right, thanks everyone. We'll make a start now.
[00:00:58 - 00:01:03] All right, cool. So this was my small plan that I made for our final tutorial.
[00:01:03 - 00:01:07] And I sort of said in the lecture today,
[00:01:07 - 00:01:11] from my end there's nothing that I'm like, oh, here's something that you need to know for the assignment.
[00:01:11 - 00:01:15] You've sort of had everything you've need for more than a week now.
[00:01:15 - 00:01:20] And it's just hopefully to try and clarify kind of anything in the last minute queries that you might have.
[00:01:20 - 00:01:26] And we've got some useful things to clarify that people have already started kind of asking me about.
[00:01:26 - 00:01:31] So I did wonder whether we want to review anything of like what happens on test day or look at another video.
[00:01:31 - 00:01:38] We could also look at what to submit which I've already got on my piece of paper.
[00:01:38 - 00:01:49] We might want to look at any drawings or review what is included in drawings because I know that we went over drawings during a time that you probably hadn't even chosen exactly what your thing was.
[00:01:49 - 00:01:51] So you're like, yeah, this is all great and fine.
[00:01:51 - 00:01:55] But now I've got questions because I'm actually making my drawings.
[00:01:55 - 00:02:01] Time sheet equals yes. So just reiterating that peer review obviously needs to be done.
[00:02:01 - 00:02:07] And then we could also show or fill in the example of like the load on test day, right?
[00:02:07 - 00:02:12] So is everyone happy with any of that? Do we want to see a video?
[00:02:12 - 00:02:16] I guess is the first day or we're happy with what the videos are.
[00:02:16 - 00:02:20] Cool. We've got nods. That's enough to encourage me.
[00:02:20 - 00:02:25] So I'm going to pick one random video.
[00:02:25 - 00:02:28] I was seeing this one.
[00:02:28 - 00:02:31] Let's do another one. We've seen that episode.
[00:02:31 - 00:02:38] Cool. So just remember on test day what's going to happen is I'm going to have all your drawings nicely
[00:02:38 - 00:02:43] ordered in terms of like what time works with your timetable when we cake to do your testing, right?
[00:02:43 - 00:02:50] So there'll be probably like six or seven groups per half now slot and like ideally it runs like clots.
[00:02:50 - 00:02:59] Because like you know every minute is like every extra minute per group is like 160 minutes for me on the day, right?
[00:02:59 - 00:03:03] So like long it can scale quite a bit.
[00:03:03 - 00:03:06] So we try and run things like a tight ship.
[00:03:06 - 00:03:15] And sometimes I might be a little bit stressed in the day or like encouraging forcefully to get on the test rig and do your thing.
[00:03:15 - 00:03:25] So what we can see here is that these groups have obviously gone through the process of picking up their drawing, weighing the structure with our pins that get recorded on their drawing sheet.
[00:03:25 - 00:03:30] They talk to their technicians and make sure that what they've made is what they've submitted and said they're going to make.
[00:03:30 - 00:03:37] Then you go to me and you fill out the test day or you show me your test day sheet which has your modes and loads of failure.
[00:03:37 - 00:03:41] Now on that test day sheet as you run familiar with what I'm talking about.
[00:03:41 - 00:03:43] Here we've got nods.
[00:03:43 - 00:03:46] It's like a beautiful, it's a very beautiful document.
[00:03:46 - 00:03:52] It's a table, it has like a box to put your name in, a box for your target failure weight.
[00:03:52 - 00:03:55] So that's always going to be the total mess, right?
[00:03:55 - 00:04:00] So anything that we talked about in terms of failure, it's always the total mess.
[00:04:00 - 00:04:06] So plus that 1.39 kg, right?
[00:04:06 - 00:04:14] So if you put 20 kg on or if your target mess was 20, then on the day it's not likely to be exactly 20, right?
[00:04:14 - 00:04:18] The closest you could probably get is 20.39.
[00:04:18 - 00:04:21] Yeah? You can say whatever your target mess is.
[00:04:21 - 00:04:24] It doesn't have to be like a possible amount.
[00:04:24 - 00:04:32] If you're designed strategically so that you're possible minus the thing to send us two values that actually are possible, then people will do that.
[00:04:32 - 00:04:40] I've run my own numbers on that, but what I'm saying is like, you know, if you said that your target mess was 29.57 kg sweet.
[00:04:40 - 00:04:42] That's what I run on my spreadsheet.
[00:04:42 - 00:04:51] That's the total mess.
[00:04:51 - 00:04:56] Does the way that you pick have to be from your calculations? Ideally it would make sense to be.
[00:04:56 - 00:05:00] Yeah.
[00:05:00 - 00:05:07] So the way I'm not sure if I'm not interpreting this wrong or not interpreting this right,
[00:05:07 - 00:05:16] we're double negative sort of happening there, but what I was sort of suggested is that for your failure member, you might have a factor of safety of one.
[00:05:16 - 00:05:21] It's up to you whether you actually have a factor of safety of one or slightly above or slightly below, right?
[00:05:21 - 00:05:26] And so that may influence what you say your predicted failure mess is.
[00:05:26 - 00:05:48] But on the test day, yeah, now what you're designed to do on one age should be what your target failure mess is, right?
[00:05:48 - 00:05:57] Yeah. So there's no tolerance for what we ask on the test day.
[00:05:57 - 00:06:06] Yeah. So if you end up making it within your tolerance, but on the smaller or bigger side and you think that will influence the mess of your thing,
[00:06:06 - 00:06:11] it's up to you what you make and come with on the test day.
[00:06:11 - 00:06:18] But the target or the predicted failure mess should be based on your calculations and it should be not something that you just change on the day.
[00:06:18 - 00:06:20] It's not really how that works.
[00:06:20 - 00:06:28] So what you're looking now will be what is said on the test day and the whole thing is that we're getting you to write it down so that if you're some reason forget,
[00:06:28 - 00:06:31] they definitely know that it's there, right?
[00:06:31 - 00:06:35] Cool. Happy with that. So then you talked to me, you said yet, George.
[00:06:35 - 00:06:41] My total failure mess will be 31.39 kg. It's going to break it.
[00:06:41 - 00:06:48] The stress concentration first, the second motor failure is buckling off my horizontal membrane to their first big or into the X plane.
[00:06:48 - 00:06:51] But I'll probably just say into the perspyxer up and down.
[00:06:51 - 00:06:59] And my third motor failure is tear out at my hole on the top nimber.
[00:06:59 - 00:07:08] Yeah. So you want to make it clear what each of your second and third motor failure are so that if they happen we know very clearly what it was.
[00:07:08 - 00:07:13] So we can't just say like, buckling and say, oh, which buckling.
[00:07:13 - 00:07:17] Yeah. Cool. So then from there, this could be you and you can see that.
[00:07:17 - 00:07:24] they're designed into the apparatus and then now they're going to do the test.
[00:07:24 - 00:07:30] So I'll be quiet and with the video play.
[00:07:30 - 00:07:39] So 5 kg plus the hook in the mess.
[00:07:39 - 00:07:41] Look in the load attachment.
[00:07:41 - 00:08:06] 10 kg, 15 kg, 20 kg.
[00:08:06 - 00:08:11] Yeah. It's good. We're in the money here.
[00:08:11 - 00:08:16] Another 5. So we've got 25 plus 1.3. Right.
[00:08:16 - 00:08:25] 26.4 will call it. Another 5. So 31.1.2 is held.
[00:08:25 - 00:08:28] So there'll be 31.2.
[00:08:28 - 00:08:35] So every time that you put a mess on, if it breaks straight away within two seconds,
[00:08:35 - 00:08:38] they're previously hard mess as what is recorded.
[00:08:38 - 00:08:44] Yeah. If it's more than two seconds and then breaks, the mess that's on it is what's recorded.
[00:08:44 - 00:08:51] So sometimes we have to do some TMO sort of stuff, but we'll see there and you'll see that sort of getting prepared and ready to go.
[00:08:51 - 00:08:55] So that once these messes have been used, they can kind of start. Right.
[00:08:55 - 00:09:06] So I think they're going for 36 here. Alt-nurt, game plan may be changing.
[00:09:06 - 00:09:19] 1.2. So 33.4. Right. Now a 5.
[00:09:19 - 00:09:29] So you see there, that one's actually kind of a good example of someone that's probably getting a little bit too close to the line of dropping the weight on it.
[00:09:29 - 00:09:34] Like on the test day, that would be considered dropping it on it.
[00:09:34 - 00:09:39] So you want to kind of make sure that you don't do that. You carefully kind of put them out on.
[00:09:39 - 00:09:44] The same thing will happen, but you're not trying to have an impact kind of load.
[00:09:44 - 00:09:49] So because that one broke straight away and if we negate the fact that they sort of dropped it on there,
[00:09:49 - 00:09:53] we would count up the messes before that mess was added.
[00:09:53 - 00:09:58] So I think it was 33.4 if my math was nothing.
[00:09:58 - 00:10:06] Cool. Happy. Do we want to watch another one? Well that's fair enough.
[00:10:06 - 00:10:09] All right. Cool. Keep the party rolling. All right.
[00:10:09 - 00:10:14] So the other things I had on my list was that's test day tech.
[00:10:14 - 00:10:18] What to submit? So that was just basically what we covered last time.
[00:10:18 - 00:10:20] So we can see here.
[00:10:20 - 00:10:22] These may be separate PDF documents.
[00:10:22 - 00:10:27] You may have compiled them all into one, but we have our cover sheet, our report, which is 800 words.
[00:10:27 - 00:10:29] We only care about that. Andrew words in the report.
[00:10:29 - 00:10:32] You're encouraged to use figures and tables to present.
[00:10:32 - 00:10:39] Can you information about your final design and the clear and cost effective or concise way?
[00:10:39 - 00:10:45] Then you'll have your calculations set, which is eight pages and we'll have these beautiful titles and sketches and comments throughout them.
[00:10:45 - 00:11:01] And then you'll have your drawings, which may be two to four drawings and then other appendices, which may be your AI declaration, any additional working if you had kind of spreadsheet or similar that you might want to kind of highlight that you use in your design process or code.
[00:11:01 - 00:11:09] Or they might be additional kind of testing data or photos that you want to just include to really show some pizzazz in terms of how thorough you were.
[00:11:09 - 00:11:13] And then obviously you'll also have sort of a time sheet in there.
[00:11:13 - 00:11:16] Cool. So there was a question about these drawings that was just asked.
[00:11:16 - 00:11:19] George, do we have to use the UC template? No.
[00:11:19 - 00:11:29] You can use whatever you want. Just make sure that all the information that we've talked about in terms of what to include in your title block and in regard to your tolerances.
[00:11:29 - 00:11:35] Clearly in there, communicated effectively, followed the standard.
[00:11:35 - 00:11:44] Yeah? So similarly, you don't have to use SOLIDWORKS if you're like, I'm on the on-shape vibe or I'm on fusion or something like that, right?
[00:11:44 - 00:11:57] Cool. And then the other question I had about drawings is, do we have to have individual part drawings or components of our part drawings?
[00:11:57 - 00:12:03] Or is it fine just to say, this is my compression member. So I've been, but I draw all three in one drawing.
[00:12:03 - 00:12:07] And I'd say that is the recommendation. So two to four drawings.
[00:12:07 - 00:12:11] One thing is you're more assembly, which kind of guides the person looking at you.
[00:12:11 - 00:12:17] You're drawing to know kind of what your overall kind of setups lookin' like and what kind of number of members there are.
[00:12:17 - 00:12:21] And then depending on how many members you have, you might have two or three member drawings.
[00:12:21 - 00:12:29] And I would just make one drawing per member. So regardless of how many strips are used to make those members, I'll just put that all on one.
[00:12:29 - 00:12:38] And you can have a note, or a manufacturing note that shows where there are kind of different kind of members being joined and how those are being joined.
[00:12:38 - 00:12:47] So you can use that note to the top left of your drawing. If there's a general comment that you want to make or you can add annotations to your drawing.
[00:12:47 - 00:12:52] The main thing is that it's clearly communicated what is going on and how you think it's made.
[00:12:52 - 00:13:03] In questions about any of that, what else did I have on there?
[00:13:03 - 00:13:10] I've done our drawing overview. Do we want to review a drawing?
[00:13:10 - 00:13:18] Or are we wanting to go into general global questions that you guys have?
[00:13:18 - 00:13:22] Someone has to be decisive. Review a drawing? Sweet.
[00:13:22 - 00:13:28] So you remember in one of the tutorials we did go over this, right?
[00:13:28 - 00:13:35] So just want to make it really clear to myself that this is not new content.
[00:13:35 - 00:13:40] What was the tutorial for? There we did it.
[00:13:40 - 00:13:45] Maybe it was tutorial for.
[00:13:45 - 00:13:49] It was the end of week two when everyone was having a real fun time at Electric Ave.
[00:13:49 - 00:13:58] And I was lecturing everyone who missed out on tickets or didn't want to go to Electric Avenue because there's way too many people.
[00:13:58 - 00:14:04] So we saw a photographer in this that to start with,
[00:14:04 - 00:14:16] my memory is treating me correctly. What's drawing?
[00:14:16 - 00:14:19] Make sure you save your drawings.
[00:14:19 - 00:14:23] We roasted this drawing that I had done, right?
[00:14:23 - 00:14:27] There were common eras like no titles,
[00:14:27 - 00:14:32] no clear comments about how this thing here would be made.
[00:14:32 - 00:14:35] If it's made of two things but there's no line here.
[00:14:35 - 00:14:42] There's unnecessary views, there's multiple parts on one drawing, making it kind of cluttered.
[00:14:42 - 00:14:49] But luckily I was the technician in this case who manufactured this thing and it was more just like a personal note rather than a
[00:14:49 - 00:14:52] formal engineering drawing to be seen by other people.
[00:14:52 - 00:14:56] But here we go. It's probably been seen by like a thousand people now.
[00:14:56 - 00:15:05] And what we saw was that there are these general tips and tricks which I would use to at least tick off before you submit your assignment.
[00:15:05 - 00:15:13] Because it always blows my mind how close people can get to like making the thing like 25% better than drawing 25% better
[00:15:13 - 00:15:15] by not doing these things here.
[00:15:15 - 00:15:24] Make sure your title block is completely filled out. As the date, as the name has the title of your part,
[00:15:24 - 00:15:28] has appropriate kind of tolerances in there, right?
[00:15:28 - 00:15:30] Use capital letters.
[00:15:30 - 00:15:35] Look at the overall layout of your drawing. Make sure I separate it and let this selected views follow the drawing standard.
[00:15:35 - 00:15:38] And let they show all the key details and functionality.
[00:15:38 - 00:15:43] So if something's really small, you might want to use something like a detail view to kind of provide that.
[00:15:43 - 00:15:53] Overall, as you're drawing uncluttered and easy to read, then intermediate, if you really want to make sure you've done a good job looking at whether your
[00:15:53 - 00:15:57] tolerances have more than just a general tolerance, right?
[00:15:57 - 00:16:02] So if things like your stress concentration, I think we talked about the fact that it's probably going to be a lot tighter tolerance,
[00:16:02 - 00:16:06] maybe more like 0.1 rather than plus or minus 0.5.
[00:16:06 - 00:16:15] Similarly, for your distance of your holes, for your horizontal and vertical dimensions, those are allowed to be plus or minus 0.3, right?
[00:16:15 - 00:16:18] So you might as well make that be plus or minus 0.3 on your drawing.
[00:16:18 - 00:16:23] So otherwise, you could make something that doesn't make your drawing that meets the requirement of the assignment.
[00:16:23 - 00:16:26] And then you'll get Tony on the day being like, why have you done this?
[00:16:26 - 00:16:29] This is going to cost you $1 million to do now.
[00:16:29 - 00:16:31] Yeah?
[00:16:31 - 00:16:33] Cool.
[00:16:33 - 00:16:51] So I think we also talked about the fact that for linear dimensions, that's not there, if you look up ISO, linear dimension, taller answers.
[00:16:51 - 00:17:02] You'll see that there are tables that look like this that kind of show, if you're not really sure what an appropriate tolerance is for a specific length,
[00:17:02 - 00:17:07] what a guide could be for a different linear dimension tolerance.
[00:17:07 - 00:17:09] So four things that aren't super important.
[00:17:09 - 00:17:17] You could assume that it might be a tolerance class of course following ISO 2768.
[00:17:17 - 00:17:24] And that tells you, for these kind of dimensions, these kind of tolerances might be appropriate, right?
[00:17:24 - 00:17:31] So in some manufacturing drawings, they'll have actually a little table that says, you know, all tolerances are done to this table here.
[00:17:31 - 00:17:34] So that the things that are really small aren't impossible to make.
[00:17:34 - 00:17:39] All the things that are really big are getting un-overly constrained, right?
[00:17:39 - 00:17:42] Because plus or minus 0.5 is quite a tight tolerance.
[00:17:42 - 00:17:51] If you're going 1,000 millimeters, but it's kind of not a tight tolerance, if you're going very coarse, then there's only three or six millimeter.
[00:17:51 - 00:17:52] Cool.
[00:17:52 - 00:17:55] So let's pick a drawing.
[00:17:55 - 00:18:01] One that we haven't done.
[00:18:01 - 00:18:06] Oh, yeah, they were there.
[00:18:06 - 00:18:07] Cool.
[00:18:07 - 00:18:14] So say, although this doesn't follow what we said, oh, you guys were seeing what I was saying just before.
[00:18:14 - 00:18:15] I just changed it over.
[00:18:15 - 00:18:16] Yeah.
[00:18:16 - 00:18:17] Okay.
[00:18:17 - 00:18:18] Okay.
[00:18:18 - 00:18:24] What I was saying was this is a drawing that's kind of doing the thing that we said that we don't need to do, right?
[00:18:24 - 00:18:29] So this is someone's like broken up like the I-beam to be like, oh, this is the flange.
[00:18:29 - 00:18:32] And then this is the web.
[00:18:32 - 00:18:33] Yeah.
[00:18:33 - 00:18:37] So I think that this one here is the flange of it, right?
[00:18:37 - 00:18:42] So idea is that this is actually like realistically like an I-beam.
[00:18:42 - 00:18:45] Something like this, right?
[00:18:45 - 00:18:48] Super cool.
[00:18:48 - 00:18:50] Good drawing.
[00:18:50 - 00:18:51] Cool.
[00:18:51 - 00:18:56] So if we had to critique it together, what things could we do to improve the drawing?
[00:18:56 - 00:19:03] So let's just go through.
[00:19:03 - 00:19:09] So I don't know the people online whether they're seeing this one slide or this thing here, but for the people that are here,
[00:19:09 - 00:19:13] it makes most sense to have one screen showing one of the things.
[00:19:13 - 00:19:16] So if we look, is the title block filled out correctly?
[00:19:16 - 00:19:21] Assume that the design to buy and drawn by is filled out with capital letters.
[00:19:21 - 00:19:25] For any other thing in the title block that we should improve, or is it looking pretty good?
[00:19:25 - 00:19:38] Would you be happy to stand by this information?
[00:19:38 - 00:19:44] If you had submitted it to a, I know, auto bin.
[00:19:44 - 00:19:49] So I'm going to shake in the head.
[00:19:49 - 00:19:51] Is everyone shaking the head?
[00:19:51 - 00:19:59] So this is one of those times, but like, I'm asking to get you guys to say it because like, it means more coming from you rather than me just saying,
[00:19:59 - 00:20:01] like, do this, do this, do this.
[00:20:01 - 00:20:02] Yeah.
[00:20:02 - 00:20:03] Yeah.
[00:20:03 - 00:20:06] So what things could we, is the material kind of good?
[00:20:06 - 00:20:08] Yes.
[00:20:08 - 00:20:09] It's made from per split.
[00:20:09 - 00:20:10] That's fine.
[00:20:10 - 00:20:15] So if you, you might write manufactured or 1.2 millimeter by 20 millimeter.
[00:20:15 - 00:20:16] Yeah.
[00:20:16 - 00:20:22] You could have everything saying like, yeah.
[00:20:22 - 00:20:30] Provided or, provided material of, or just right, 1.2 times 20 millimeters of the strip, right?
[00:20:30 - 00:20:36] Aluminium strips bracket provided if you really want to, right?
[00:20:36 - 00:20:37] Cool.
[00:20:37 - 00:20:38] Finish.
[00:20:38 - 00:20:39] Smooth.
[00:20:39 - 00:20:40] Mm.
[00:20:40 - 00:20:41] Sort of confused.
[00:20:41 - 00:20:43] If you really wanted to, you might write something relating to the edges.
[00:20:43 - 00:20:44] Yeah.
[00:20:44 - 00:20:53] So you might have a note in there that says ensure all edges are free from sharp or smoothed or whatever.
[00:20:53 - 00:20:54] Right.
[00:20:54 - 00:20:57] Just saying smooth is sort of like what does that mean?
[00:20:57 - 00:21:05] But what we're talking about is sometimes there might be radii or similar that you want to put some in-re-tape on to make it not have like a sharp,
[00:21:05 - 00:21:08] lump or similar, right?
[00:21:08 - 00:21:09] Cool.
[00:21:09 - 00:21:14] Tolerances are, our tolerance is good.
[00:21:14 - 00:21:22] Would you be happy to talk to Tony or one of the other technicians if all of your dimensions are to point one of a millimeter?
[00:21:22 - 00:21:24] People are shaking the head.
[00:21:24 - 00:21:28] What would be better for this general tolerance?
[00:21:28 - 00:21:30] So this would be better.
[00:21:30 - 00:21:31] Oh, better.
[00:21:31 - 00:21:38] Eagles plus or minus 0.5.
[00:21:38 - 00:21:39] Cool.
[00:21:39 - 00:21:42] Now, we're going to assume that those are filled completely.
[00:21:42 - 00:21:43] This is good, right?
[00:21:43 - 00:21:45] We've got a name of our part.
[00:21:45 - 00:21:47] Is this drawing number good?
[00:21:47 - 00:21:48] No.
[00:21:48 - 00:21:51] It's not a number.
[00:21:51 - 00:21:52] Right.
[00:21:52 - 00:21:56] And I think I've told you before, I always try to keep people on the toes.
[00:21:56 - 00:21:57] I always go.
[00:21:57 - 00:22:01] Even if it's drawing one of three, I'm like, 001.
[00:22:01 - 00:22:05] There may be 999 drawings in this set.
[00:22:05 - 00:22:07] But there's only three, you know?
[00:22:07 - 00:22:08] Cool.
[00:22:08 - 00:22:11] And in project, pretty good, date, good.
[00:22:11 - 00:22:12] Drawing not to scale.
[00:22:12 - 00:22:13] That's fine.
[00:22:13 - 00:22:17] We've got here that a student angle orthographic, which is good, right?
[00:22:17 - 00:22:24] So if you don't use the UC template, probably make sure that all of the same sort of information is included.
[00:22:24 - 00:22:26] Sweet.
[00:22:26 - 00:22:31] Now, looking at the next thing that the Mark would be looking at.
[00:22:31 - 00:22:34] Have you used capital letters?
[00:22:34 - 00:22:35] Yes.
[00:22:35 - 00:22:36] Good job.
[00:22:36 - 00:22:39] Those person used capital letters.
[00:22:39 - 00:22:40] Next.
[00:22:40 - 00:22:45] There's the size slash layout of the drawing appropriate.
[00:22:45 - 00:22:50] So the real question is, could this be bigger without making it more cluttered?
[00:22:50 - 00:22:53] And I'd probably say, yeah, it could be a little bit bigger.
[00:22:53 - 00:23:03] Yeah, so size could be a bit bigger.
[00:23:03 - 00:23:05] It's not terrible.
[00:23:05 - 00:23:07] It's not like all on one half of the page.
[00:23:07 - 00:23:11] But yeah, on other things, just while it kind of pops my head,
[00:23:11 - 00:23:15] it's like this revisions table sometimes up here from like SOLIDWORKS.
[00:23:15 - 00:23:18] It's good that they've deleted that or fill it out.
[00:23:18 - 00:23:24] But the amount of times I've said like drawing to like x6 of jan 13 or something like that.
[00:23:24 - 00:23:27] And then it's just nothing.
[00:23:27 - 00:23:28] Yeah.
[00:23:28 - 00:23:33] Revisions table I'd normally add if there is a subsequent revision, not on the first release.
[00:23:33 - 00:23:34] But yeah.
[00:23:34 - 00:23:36] Cool.
[00:23:36 - 00:23:37] Cool.
[00:23:37 - 00:23:39] Next thing on the list.
[00:23:39 - 00:23:40] Do this like the views.
[00:23:40 - 00:23:43] Show all the key details slash functionality.
[00:23:43 - 00:23:46] What do you reckon?
[00:23:46 - 00:23:52] Yes or no?
[00:23:52 - 00:23:53] All right.
[00:23:53 - 00:23:54] Would you still hands up thing?
[00:23:54 - 00:23:55] Who reckons?
[00:23:55 - 00:23:56] No.
[00:23:56 - 00:23:57] All right.
[00:23:57 - 00:23:58] Rescue for me now.
[00:23:58 - 00:23:59] Who reckons?
[00:23:59 - 00:24:00] Yes.
[00:24:00 - 00:24:01] Cool.
[00:24:01 - 00:24:02] Who reckons?
[00:24:02 - 00:24:04] I don't want to answer a question.
[00:24:04 - 00:24:05] No one doesn't.
[00:24:05 - 00:24:07] Sort of like a, yeah.
[00:24:07 - 00:24:08] It does.
[00:24:08 - 00:24:14] I think having the two views that it has does show the required detail.
[00:24:14 - 00:24:18] We wouldn't add very much if we added another side view.
[00:24:18 - 00:24:22] Now, with that, what could we do to improve the clarity of the views that
[00:24:22 - 00:24:24] were showing?
[00:24:24 - 00:24:25] Lay with them.
[00:24:25 - 00:24:26] Right.
[00:24:26 - 00:24:27] So what should this one here be labeled?
[00:24:27 - 00:24:30] Ooh.
[00:24:30 - 00:24:31] Top.
[00:24:31 - 00:24:33] Wait, I'll leave you have a thing.
[00:24:33 - 00:24:34] Have a thing.
[00:24:34 - 00:24:37] So it's going to be top or front, right?
[00:24:37 - 00:24:40] So who reckons that it should be top?
[00:24:40 - 00:24:41] Oh, yeah.
[00:24:41 - 00:24:42] Couple.
[00:24:42 - 00:24:44] Who reckons that it should be front?
[00:24:44 - 00:24:45] Sweet.
[00:24:45 - 00:24:48] Now, someone who's put their hand up or front, why should this be front?
[00:24:48 - 00:24:58] Yeah.
[00:24:58 - 00:25:04] So when you, so assuming that this is, if we're looking, there's two answers in the
[00:25:04 - 00:25:05] both good.
[00:25:05 - 00:25:09] So if we think about our testing apparatus, we're just going to draw it.
[00:25:09 - 00:25:11] We'd leave like this.
[00:25:11 - 00:25:16] When we look from the front view, if that's all we're choosing, the front side that we might see if this is our
[00:25:16 - 00:25:18] eye beam would be this view here.
[00:25:18 - 00:25:19] Yeah?
[00:25:19 - 00:25:25] Also, that's a good, you know, that's good in terms of following natural orientation,
[00:25:25 - 00:25:28] you know, for using engineering drawing terminology.
[00:25:28 - 00:25:33] The main thing, though, is that this front view here matches the front view of our
[00:25:33 - 00:25:34] ICEMETRA view.
[00:25:34 - 00:25:35] Yeah?
[00:25:35 - 00:25:40] So if you had said that this was the front, then you'd drawn it like that, or if we're
[00:25:40 - 00:25:44] weird thickness there, technically no foul.
[00:25:44 - 00:25:45] You know?
[00:25:45 - 00:25:50] It's maybe not the natural orientation, but technically it would be fine.
[00:25:50 - 00:25:51] Yeah?
[00:25:51 - 00:25:52] As long as it follows the drawing standard.
[00:25:52 - 00:25:59] So then, therefore, watch this one be top, and that should really be above if we're doing third angle or
[00:25:59 - 00:26:00] check out.
[00:26:00 - 00:26:06] And we can see George is done a very good job in writing capital letters, not on there,
[00:26:06 - 00:26:08] like this or something.
[00:26:08 - 00:26:11] That'd be bad.
[00:26:11 - 00:26:12] Cool.
[00:26:12 - 00:26:16] Next thing, drawing is uncluttered and easy to read.
[00:26:16 - 00:26:17] Yes.
[00:26:17 - 00:26:22] And then the other thing that we just need to look at are tolerances appropriate and do the
[00:26:22 - 00:26:25] dimensions, follow the drawing standard and tell us everything we need to know.
[00:26:25 - 00:26:28] So what is good about the dimensions?
[00:26:28 - 00:26:36] What's a good dimension example on this?
[00:26:36 - 00:26:37] The link for the number.
[00:26:37 - 00:26:39] Maybe this overall one, like pretty good.
[00:26:39 - 00:26:40] Yeah?
[00:26:40 - 00:26:41] Nice.
[00:26:41 - 00:26:44] Yeah?
[00:26:44 - 00:26:46] What's not so nice?
[00:26:46 - 00:26:50] What's this thing happening here?
[00:26:50 - 00:26:51] What was it called?
[00:26:51 - 00:26:56] Chain dimensioning, right?
[00:26:56 - 00:27:00] So that's like massive like, cutting heads with like this one here, right?
[00:27:00 - 00:27:05] Like this one here has massive beef, but all of these ones here.
[00:27:05 - 00:27:06] Because they don't agree.
[00:27:06 - 00:27:10] This one here tells you that the overall link should be whatever those plus together is,
[00:27:10 - 00:27:15] which I'm assuming would be 320 plus or minus 0.1. 2.3.4.4.5.
[00:27:15 - 00:27:16] 0.6.
[00:27:16 - 00:27:17] 0.7.
[00:27:17 - 00:27:19] I mean, technically they actually don't have beef.
[00:27:19 - 00:27:20] I'm wrong, right?
[00:27:20 - 00:27:24] Because they don't have this one also dimensioned.
[00:27:24 - 00:27:33] So they're actually fine, but it's not the best way to kind of communicate with this, right?
[00:27:33 - 00:27:38] So if they had to mention this here, then that would have a clash.
[00:27:38 - 00:27:39] Yeah?
[00:27:39 - 00:27:41] But in this case, they haven't over defined their thing.
[00:27:41 - 00:27:45] But the chain dimensioning is not so nice because it could mean that if this part actually
[00:27:45 - 00:27:49] needed to be possible or is point 1 to fit the other bit that's being cut, you could make
[00:27:49 - 00:27:51] something that wouldn't go together.
[00:27:51 - 00:27:54] So two things that we could do.
[00:27:54 - 00:27:57] One thing would be with these repeated dimensions.
[00:27:57 - 00:28:03] If we want to make it uncluttered by reducing the number of dimensions, we could write
[00:28:03 - 00:28:06] T, Y, P after a repeated dimension.
[00:28:06 - 00:28:08] What does that mean?
[00:28:08 - 00:28:10] Typical, yeah?
[00:28:10 - 00:28:17] So typical, which means you could just have 60 T, Y, P, 20 T, Y, P, and 50 T, Y, P possibly.
[00:28:17 - 00:28:20] Or you might just have one there.
[00:28:20 - 00:28:25] But essentially what I'm trying to say is that's a really weird way to dimension the hole
[00:28:25 - 00:28:26] to hole dimension.
[00:28:26 - 00:28:29] And that's probably what you want to know when you're drilling your hole, right?
[00:28:29 - 00:28:31] You don't want your drawing.
[00:28:31 - 00:28:34] You don't, the person who's manufacturing this to go, oh, this is so fun.
[00:28:34 - 00:28:39] I get to go 60 plus 20 plus 50 plus 20 plus 50 plus 20 plus 60, just to work out the distance
[00:28:39 - 00:28:40] between those two holes.
[00:28:40 - 00:28:46] Or it would be better if you'd ridden 400 plus or minus 3 millimeters and then removed one
[00:28:46 - 00:28:49] of these or put one of them in brackets.
[00:28:49 - 00:28:52] So that they're not made to that.
[00:28:52 - 00:28:56] Because this is symmetrical, we have things that are symmetrical.
[00:28:56 - 00:29:00] If it's not the mentioned, it can be assumed that it is symmetrical.
[00:29:00 - 00:29:03] If you're worried about doing that and it feels wrong, you could make a note.
[00:29:03 - 00:29:07] Other top left to kind of communicate that.
[00:29:07 - 00:29:08] Yeah.
[00:29:08 - 00:29:11] So with dimensioning, it's kind of one of those annoying things as a student with this.
[00:29:11 - 00:29:13] Like lots of right ways to do it.
[00:29:13 - 00:29:19] But there are some things that can always be agreed on as not being correct.
[00:29:19 - 00:29:21] Cool.
[00:29:21 - 00:29:28] Is this, so it would be better to be, well, is there 400 even though it's not plus or minus 3?
[00:29:28 - 00:29:32] I'm sure that was made for a horizontal member.
[00:29:32 - 00:29:34] Whatever the dimension is.
[00:29:34 - 00:29:36] X, X, X.
[00:29:36 - 00:29:38] Cool.
[00:29:38 - 00:29:40] Is this tolerance here good?
[00:29:40 - 00:29:45] Are we taking that or are we crossing that?
[00:29:45 - 00:29:47] Is that a smart thing to do?
[00:29:47 - 00:29:49] So we've got a specific tolerance here.
[00:29:49 - 00:29:51] What are they trying to communicate?
[00:29:51 - 00:29:54] Well, we'll go 50-50 gain, hands up.
[00:29:54 - 00:29:55] It's good or bad.
[00:29:55 - 00:29:58] So who thinks that dimensioning of that hole to the right?
[00:29:58 - 00:30:00] I see it's a little bit blurry.
[00:30:00 - 00:30:02] You might as well sort of struggling.
[00:30:02 - 00:30:04] Is that good or bad?
[00:30:04 - 00:30:07] I see that's between 8.1 and 8.
[00:30:07 - 00:30:08] Who reckon it's good?
[00:30:08 - 00:30:12] Who reckon it's bad?
[00:30:12 - 00:30:13] Cool.
[00:30:13 - 00:30:17] So those who see that was good, what are you reckon?
[00:30:17 - 00:30:18] Why is it good?
[00:30:18 - 00:30:24] I say it can't be smaller than 8m, right?
[00:30:24 - 00:30:25] Cool.
[00:30:25 - 00:30:29] Those who reckon it's bad, why do you reckon it's bad?
[00:30:29 - 00:30:31] You could both be right.
[00:30:31 - 00:30:35] Lots of people see there was bad.
[00:30:35 - 00:30:37] Someone is front.
[00:30:37 - 00:30:50] Your honour, I believe it's bad because.
[00:30:50 - 00:30:52] Not possibly my second one.
[00:30:52 - 00:30:53] Okay.
[00:30:53 - 00:31:03] So you can actually just clarify and just say 8m plus or plus
[00:31:03 - 00:31:07] this and not say this is minus zero, but that's sort of like this more
[00:31:07 - 00:31:09] than one right way to kind of communicate it.
[00:31:09 - 00:31:10] This is making it super clear.
[00:31:10 - 00:31:12] Don't make it smaller than 8.
[00:31:12 - 00:31:15] Yeah, but you could do the same thing of plus.
[00:31:15 - 00:31:19] You could go 8m plus 0.1 minus zero.
[00:31:19 - 00:31:20] Yeah.
[00:31:20 - 00:31:21] Cool.
[00:31:21 - 00:31:22] That's good.
[00:31:22 - 00:31:23] I agree.
[00:31:23 - 00:31:24] It might be clear that way.
[00:31:24 - 00:31:26] Anyone else got any comments on it?
[00:31:26 - 00:31:30] What is it trying to do functionally for you on the test day?
[00:31:30 - 00:31:32] What's it trying to ensure?
[00:31:32 - 00:31:36] Make sure that you can put it together and that the pen actually
[00:31:36 - 00:31:37] goes through, right?
[00:31:37 - 00:31:40] We know that the pen does mean to be an 8m pen, so the idea is
[00:31:40 - 00:31:44] otherwise if you had plus or minus 0.1, you might drill it and it's allowed
[00:31:44 - 00:31:47] to be 7.9 and then when you go together, go to put it together, you're like
[00:31:47 - 00:31:50] massively stressing on test day and trying to put it together and
[00:31:50 - 00:31:53] sirens are going in the distance and I'm going like please get your
[00:31:53 - 00:31:56] thing together so that you can start doing your testing and you know?
[00:31:56 - 00:31:57] But this is like avoiding that.
[00:31:57 - 00:32:01] It means that you can definitely get your pen through your hole and
[00:32:01 - 00:32:03] therefore get your whole thing together.
[00:32:03 - 00:32:06] Cool.
[00:32:06 - 00:32:09] Any other comments that we have generally about that?
[00:32:09 - 00:32:13] Or are you kind of happy?
[00:32:13 - 00:32:17] So if it was a stress concentration, then we'd have a tighter
[00:32:17 - 00:32:20] hole inside the idea for our...
[00:32:20 - 00:32:25] I'm just going to take it but there's more than one right way that you can do that, right?
[00:32:25 - 00:32:30] So for those who are online, I'm not sure if you can see both screens and now
[00:32:30 - 00:32:35] you can definitely see both screens and then that's the full drawing that we're doing.
[00:32:35 - 00:32:42] Yeah, question?
[00:32:42 - 00:32:46] Yeah, so instead of having to mention both holes, which again,
[00:32:46 - 00:32:50] generally speaking, if you see two holes that look the same size,
[00:32:50 - 00:32:53] it's fair to assume that this hole is 8mm,
[00:32:53 - 00:32:55] therefore this hole is also 8mm.
[00:32:55 - 00:33:00] But if you really wanted to, you could write T-Y-P and that makes it super clear that person
[00:33:00 - 00:33:01] reading it.
[00:33:01 - 00:33:03] Yep, that one is the same as that one.
[00:33:03 - 00:33:04] Yeah?
[00:33:04 - 00:33:07] Often the typical will be classic for us if we had one where it was like,
[00:33:07 - 00:33:12] you know how people were doing like the a million white saving holes?
[00:33:12 - 00:33:15] Imagine mentioning all of them individually,
[00:33:15 - 00:33:17] just saying T-Y-P.
[00:33:17 - 00:33:23] And then similarly what I think about those is a change of mentioning you might be able to have like a bigger tolerance
[00:33:23 - 00:33:27] so that you know, you might actually not really care if it's like
[00:33:27 - 00:33:31] to half a mill, but you might be able to write a note or clone of
[00:33:31 - 00:33:35] adjusted specific torrents just to say, you know.
[00:33:35 - 00:33:41] So assume that there's 15 holes in there approximately space this to this.
[00:33:41 - 00:33:43] Yeah?
[00:33:43 - 00:33:47] Don't think I have anything more to say about that unless you've got questions about it.
[00:33:47 - 00:33:55] So that's pretty much everything.
[00:33:55 - 00:33:59] I don't think we need to fill out the load on test day because you should be able to do that.
[00:33:59 - 00:34:01] I believe and you would talk through it.
[00:34:01 - 00:34:03] So now we've got general questions which is great.
[00:34:03 - 00:34:18] We'll go to the front and then we'll go to the back.
[00:34:18 - 00:34:21] No, because you know, again, the symmetry will help you to know.
[00:34:21 - 00:34:24] So is it confusing for your 50 T-Y-P in 60 T-Y-P?
[00:34:24 - 00:34:25] No.
[00:34:25 - 00:34:29] If it was 50 and 51, I'd probably be on your side and be like,
[00:34:29 - 00:34:30] yeah, that's confusing.
[00:34:30 - 00:34:31] Make it clear.
[00:34:31 - 00:34:34] But again, you would at least dimension one of the 50 ones.
[00:34:34 - 00:34:38] And then it would be logical to assume that that's a metric.
[00:34:38 - 00:34:39] Yeah?
[00:34:39 - 00:34:41] Or if it looks, you know, that's saying that.
[00:34:41 - 00:34:42] But it does us from here to here.
[00:34:42 - 00:34:43] It's 60.
[00:34:43 - 00:34:46] I probably would actually remove that or only have it once.
[00:34:46 - 00:34:50] And then that means that it's not going to be over defined.
[00:34:50 - 00:34:55] Yeah.
[00:34:55 - 00:34:57] Do you actually have to?
[00:34:57 - 00:34:59] It's a great question.
[00:34:59 - 00:35:03] You don't have to, but it probably shows that you've thought about it.
[00:35:03 - 00:35:05] And it makes it clear.
[00:35:05 - 00:35:06] So I would.
[00:35:06 - 00:35:09] But as you say, because it's a metric, if you don't put it in there,
[00:35:09 - 00:35:12] it can be assumed by the person making it that it hasn't.
[00:35:12 - 00:35:16] But in this case, I don't think it makes it overly cluttered to put T-Y-P there.
[00:35:16 - 00:35:18] So sort of no.
[00:35:18 - 00:35:21] Nothing to lose by putting it in, I guess.
[00:35:21 - 00:35:22] Cool.
[00:35:22 - 00:35:32] And then we had another question in the back.
[00:35:32 - 00:35:33] That's a good question.
[00:35:33 - 00:35:35] Do you have to model the rivets?
[00:35:35 - 00:35:48] I mean, it would kind of cool to see the rivets, but don't have to, I guess.
[00:35:48 - 00:35:49] Yeah.
[00:35:49 - 00:35:52] So if you want, so I'm actually okay with either.
[00:35:52 - 00:35:53] Yeah.
[00:35:53 - 00:35:57] Some people like to put the fastens in just like when you have your,
[00:35:57 - 00:36:02] when you have your a general assembly, some people love to model the pins.
[00:36:02 - 00:36:04] Some people don't.
[00:36:04 - 00:36:07] My mind doesn't make too much difference.
[00:36:07 - 00:36:11] But all I would say is that if you only have a hole,
[00:36:11 - 00:36:15] or even if you hit show the river, you probably need to have a note kind of talking about what
[00:36:15 - 00:36:16] river is used.
[00:36:16 - 00:36:17] Yeah.
[00:36:17 - 00:36:23] So as you can say, for all 3.2 millimeter holes, or all 3.2 millimeter holes,
[00:36:23 - 00:36:27] are prepared for whatever the type of river that we've got is,
[00:36:27 - 00:36:29] you might be able to say the part number here.
[00:36:29 - 00:36:31] And there's two links of them.
[00:36:31 - 00:36:36] So there's one that can do for joining two members, one that can do for joining three members.
[00:36:36 - 00:36:37] Yeah.
[00:36:37 - 00:36:38] Make it clear.
[00:36:38 - 00:36:44] Yeah.
[00:36:44 - 00:36:50] We've used a line to make it a curve.
[00:36:50 - 00:36:53] That's what it is.
[00:36:53 - 00:36:55] Is it for when you're bending it?
[00:36:55 - 00:36:57] Like these kind of curves here?
[00:36:57 - 00:36:58] Yeah.
[00:36:58 - 00:37:03] It's just for the web of an ID and at the end, we've just got to spline.
[00:37:03 - 00:37:04] Yeah.
[00:37:04 - 00:37:09] So I would probably just, if it's a typical radius,
[00:37:09 - 00:37:11] then I would note what the radius is.
[00:37:11 - 00:37:14] You can change what those tolerances are on the radius as you see fit,
[00:37:14 - 00:37:18] because you might not actually clear if it's to plus or minus 0.5.
[00:37:18 - 00:37:21] Similarly, you might be able to have a note that says, you know,
[00:37:21 - 00:37:26] curve services, the exact radius of curve services, you know,
[00:37:26 - 00:37:27] is not important.
[00:37:27 - 00:37:32] You could say that or something.
[00:37:32 - 00:37:35] Yeah.
[00:37:35 - 00:37:36] Yeah.
[00:37:36 - 00:37:40] You could just say manufacture such that it approximately follows the shape,
[00:37:40 - 00:37:45] showing and the exact, you know,
[00:37:45 - 00:37:49] the exact radius is not important.
[00:37:49 - 00:37:50] Okay.
[00:37:50 - 00:37:51] Yeah.
[00:37:51 - 00:37:53] So you could just be.
[00:37:53 - 00:37:56] So similarly, you can see in here, like, this is a tangent edge,
[00:37:56 - 00:37:59] which really shouldn't exist, because it doesn't exist in reality.
[00:37:59 - 00:38:06] That's like a perfectly smooth surface going to a curve surface, right?
[00:38:06 - 00:38:09] So that would be, yeah.
[00:38:09 - 00:38:12] But you can use those notes just to make it clear what you do
[00:38:12 - 00:38:16] and just use like technical terminology when you do that.
[00:38:16 - 00:38:18] So, yeah.
[00:38:18 - 00:38:24] Sometimes you might have profiles that are sort of difficult to dimension concisely
[00:38:24 - 00:38:26] and also they might not really be important.
[00:38:26 - 00:38:30] You know, like this thing you're probably not going to make much difference
[00:38:30 - 00:38:34] of a 9.5 or 1.5 or 9.5.
[00:38:34 - 00:38:36] Yeah.
[00:38:36 - 00:38:37] Yeah.
[00:38:37 - 00:38:38] Yeah.
[00:38:38 - 00:38:52] So with your, the question is, if we're doing this possible minus three for our holes,
[00:38:52 - 00:38:54] how does it affect the overall dimension?
[00:38:54 - 00:38:57] Because this is symmetrical, I'd probably dimension them both on the same.
[00:38:57 - 00:39:01] I mean, you could put it down there as well, but all that's saying is that it's centered.
[00:39:01 - 00:39:02] Yeah.
[00:39:02 - 00:39:05] Unless you really have like it all centered, which some people might.
[00:39:05 - 00:39:08] But if you, if you just mentioned it like that,
[00:39:08 - 00:39:11] where you've got one coming from the hole and then one coming from the end,
[00:39:11 - 00:39:13] obviously, like that one where it's got a nice gap,
[00:39:13 - 00:39:18] not like that one where it's touching my part, then that will kind of show a both centered.
[00:39:18 - 00:39:23] This one has this, this one might have the same or different tolerance, right?
[00:39:23 - 00:39:25] Does that answer it?
[00:39:25 - 00:39:26] Yeah.
[00:39:26 - 00:39:27] So.
[00:39:27 - 00:39:29] Yeah.
[00:39:29 - 00:39:30] Cool.
[00:39:30 - 00:39:32] Other general questions there we've got.
[00:39:32 - 00:39:45] All right.
[00:39:45 - 00:39:47] We've got 10 minutes of wandering time.
[00:39:47 - 00:39:51] Unless there's anything else specific to answer.
[00:39:51 - 00:39:54] But yeah, if I get a question that I'm like, oh, this would be good if you're running here, then I will.
[00:39:54 - 00:39:56] Go back on to the mic.
[00:39:56 - 00:40:02] Otherwise, free time.
[00:40:02 - 00:40:04] Oh, this is a bunch of, if you do want to look at it.
[00:44:28 - 00:44:30] I'm sorry.
[00:44:52 - 00:44:53] No.
[00:51:28 - 00:51:30] I'm a student of mine.
[00:51:30 - 00:51:32] I'm a student of mine.
[00:51:32 - 00:51:34] I know you're really interested in setting up
[00:51:34 - 00:51:36] this whole little advantage.
[00:51:36 - 00:51:38] I think that's what we are doing.
[00:51:38 - 00:51:40] I think that's what we're doing.
[00:51:40 - 00:51:42] I don't think we're going to go with it.
[00:51:42 - 00:51:44] I'll take a photo around the experience
[00:51:44 - 00:51:46] and press it before I'm going to give you an answer.
[00:51:46 - 00:51:48] I'm going to take a photo of a student of mine.
[00:51:48 - 00:51:50] I'm going to give you a photo of a student of mine.
[00:51:50 - 00:51:52] I'm going to go to the photo of mine.
[00:51:52 - 00:51:55] Here is the slide and move.
[00:51:55 - 00:51:57] I'm going to do a photo of a student of mine.
[00:51:57 - 00:51:59] I'm going to do a photo of mine.
[00:51:59 - 00:52:01] I always do a video of a student of mine.
[00:52:01 - 00:52:05] I think one of them has been very good for this student.
[00:52:05 - 00:52:07] Starting point, for some people,
[00:52:07 - 00:52:09] I'll give you one of them.
[00:52:09 - 00:52:11] Some people might be about one,
[00:52:11 - 00:52:13] but really people in the geometry of the shaft.
[00:52:13 - 00:52:15] Some people might be using the geometry of the shaft.
[00:52:15 - 00:52:20] So the reason I'm doing this is that I'm doing this is that I would at least make at least one.
[00:53:20 - 00:53:28] If I don't like it, that's not going to change.
[00:53:28 - 00:53:30] I'm going to take a photo of one of them.
[00:53:30 - 00:53:35] I'm going to do a photo of one of them.
[00:53:35 - 00:53:39] I'm going to do a photo of one of them.
[00:53:39 - 00:53:42] Yeah, I'm going to do a photo of one of them.
[00:53:42 - 00:53:46] I'm going to tell you one tip, so that you can be able to.
[00:53:46 - 00:53:50] We want to work in a similar way.
[00:53:50 - 00:53:53] I think we're very much the hope.
[00:53:53 - 00:53:55] Is it in a different way?
[00:53:55 - 00:53:57] Yeah, just a few years ago.
[00:53:57 - 00:53:59] We're doing a C-C.
[00:53:59 - 00:54:01] It's a different way.
[00:54:01 - 00:54:05] I think it seems like the most important thing to do with the...
[00:54:05 - 00:54:06] Yeah.
[00:54:06 - 00:54:09] The other companies are the...
[00:54:09 - 00:54:11] They also...
[00:54:11 - 00:54:14] ...the most important thing that you're interested in.
[00:54:14 - 00:54:16] We've got some in that time.
[00:54:16 - 00:54:18] One over the last three minutes.
[00:54:18 - 00:54:20] One over the last three minutes.
[00:54:20 - 00:54:22] One over the last three minutes.
[00:54:22 - 00:54:24] One over the last three minutes.
[00:54:24 - 00:54:29] Okay, so I guess the third one is like a community
[00:54:29 - 00:54:30] that we're building.
[00:54:30 - 00:54:32] We're building a community that's working with.
[00:54:32 - 00:54:34] We're building a community that's working with.
[00:54:34 - 00:54:36] Some people like these things,
[00:54:36 - 00:54:38] you know, it seems to be a one-piece.
[00:54:38 - 00:54:40] You know, you might go like,
[00:54:40 - 00:54:41] up low.
[00:54:41 - 00:54:43] I don't think you know what's going to be.
[00:54:43 - 00:54:44] Uploading on the community.
[00:54:44 - 00:54:47] Don't be as familiar as there were.
[00:54:47 - 00:54:49] Do the motion to go like,
[00:54:49 - 00:54:50] or zoom, or I don't know.
[00:54:50 - 00:54:53] That's the big thing that we need to do.
[00:54:53 - 00:54:54] I don't know.
[00:54:54 - 00:54:55] I don't know.

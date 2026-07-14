# ENMT301-26W Lecture 02 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_02_audio_16k_mono_32k.mp3`
Source audio SHA-256: `2421aba70ddb48818bb74b871386264a78157122d6c0e2ecf47843ad147462dc`
Generated: 2026-06-06T04:53:10.070283+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:04 - 00:00:31] Alright, thanks everyone, we'll make a start there.
[00:00:31 - 00:00:43] Alright, thanks everyone, we'll make a start there.
[00:00:43 - 00:00:48] Cool, cool, is that working?
[00:00:48 - 00:00:49] Doesn't sound like it's working.
[00:00:49 - 00:00:50] Ah, is it working?
[00:00:53 - 00:00:54] You know what I'm off?
[00:00:55 - 00:00:57] Hello, yeah, that's working.
[00:00:57 - 00:00:59] Cool, alright, how's everyone going?
[00:00:59 - 00:01:02] Lovely to see you all again, it's been such a long time.
[00:01:03 - 00:01:09] Cool, so what I'm gonna do before I go into the very, uh,
[00:01:09 - 00:01:12] chicken conflation I've got, I thought it might just be nice
[00:01:12 - 00:01:18] to show a video, hopefully the audio's not crazy loud, just showing
[00:01:18 - 00:01:20] what we're gonna be doing.
[00:01:20 - 00:01:49] I think there's another one.
[00:02:23 - 00:02:24] Cool.
[00:02:24 - 00:02:29] So those two videos just show two examples of basically what you guys will be doing in a week-aid,
[00:02:29 - 00:02:36] as you kind of put your design structure to the test and see whether it actually kind of fails
[00:02:36 - 00:02:39] when you've designed it to fail with a stress concentration.
[00:02:39 - 00:02:43] So I know last year some people were sort of like took them a while to actually get the hit around,
[00:02:43 - 00:02:52] what was in the diagram in the assignment brief, so hopefully that video kind of makes it really nice and clear.
[00:02:52 - 00:02:59] Well, is it any, is it any questions right now, there would be like super general that you think are worth asking?
[00:02:59 - 00:03:07] Well, if they do pop up or have regular times that we can kind of bracket up.
[00:03:07 - 00:03:12] So what I'm gonna do is I'm actually gonna ask you about this on Friday for when the drop-in session is,
[00:03:12 - 00:03:17] it's looking like it's likely to be, I look at your combined timetables.
[00:03:17 - 00:03:23] I think that there's either space on Monday to live on Monday at 12, or winds at 12, or winds at four.
[00:03:23 - 00:03:28] So everything now, you know, you can simmer on it until Friday and we'll lock it in and then next week,
[00:03:28 - 00:03:34] I'll kind of actually learn available at those times just to have our kind of drop-in session,
[00:03:34 - 00:03:39] which is essentially sort of replacing the idea of having office hours, but it's hopefully a lot more accessible,
[00:03:39 - 00:03:44] nice in the space of the H-M space of the EPS kind of library.
[00:03:44 - 00:03:49] Cool, so as we kind of touched on, there'll be course communication through these kind of means.
[00:03:49 - 00:03:57] I'm gonna make a post on the Learn page, just kind of welcoming everyone and kind of cementing what we've done today.
[00:03:57 - 00:04:02] But yeah, if you do have emails enough, few people have emailed me, few people I haven't responded to, so I will get back to you,
[00:04:02 - 00:04:05] but things are going to be a hit deck this week.
[00:04:05 - 00:04:08] Yeah, keep the comms going. It's been good.
[00:04:08 - 00:04:11] It was good to chat to a few people after the lecture.
[00:04:11 - 00:04:13] So how do these tutorials work?
[00:04:13 - 00:04:18] There was something that someone asked earlier today and, in short, these are kind of operated.
[00:04:18 - 00:04:20] The Lictorial style.
[00:04:20 - 00:04:26] So there's some stuff that I kind of licks you about and there's some stuff that you guys work on in groups at your tables.
[00:04:26 - 00:04:32] And I'll make it really clear that the questions that I'm asking and stuff that I'm getting you guys to kind of work on,
[00:04:32 - 00:04:37] what I've kind of planned and thought would be the most valuable for you guys to do.
[00:04:37 - 00:04:43] And so either, yeah, I basically, I'd be in effect from you guys engaging,
[00:04:43 - 00:04:50] because I'm not really asking questions for my own genuine knowledge acquisition of their next sense.
[00:04:50 - 00:04:56] Yeah, so I'm trying to ask questions that I would be asking if I was in your position that would be helpful.
[00:04:56 - 00:05:00] Cool. So some aspects of the tutorial may feel similar to Lictorial.
[00:05:00 - 00:05:05] Our aspects will be more interactive and these work, the more interactive you are,
[00:05:05 - 00:05:10] otherwise we have this classic like mixed-constant or sort of situation where I'll be like,
[00:05:10 - 00:05:15] ask a question and have no response and I'll be in my mind kind of like panicking.
[00:05:15 - 00:05:20] I'm like, goodness, these people understand me as what I'm doing to complicated or too simple.
[00:05:20 - 00:05:23] You guys will be like, oh man, I wish George would just hurry up.
[00:05:23 - 00:05:26] He's really tried to hang my home at this point like three times now.
[00:05:26 - 00:05:28] We definitely got it the first time.
[00:05:28 - 00:05:31] But if you just tell me you get it and that's all good, then we can kind of move on with it.
[00:05:31 - 00:05:33] So it stops that from happening.
[00:05:33 - 00:05:38] Often tell people I have two traits that are kind of quite ineffective
[00:05:38 - 00:05:43] in those sorts of situations. So I'm really patient and I'm really bad at mind reading.
[00:05:43 - 00:05:47] So I'll just stand here and wait for you guys pretty much.
[00:05:47 - 00:05:50] So I'm keeping things moving like that.
[00:05:50 - 00:05:54] Cool. So I feel like this format of Lictorial is basically what gives you guys.
[00:05:54 - 00:05:57] The most value.
[00:05:57 - 00:06:01] So again, I think we can probably not write these down if you don't want to,
[00:06:01 - 00:06:05] but I do encourage people to write things down during these kind of sessions
[00:06:05 - 00:06:08] and annotate or write their own notes.
[00:06:08 - 00:06:12] But do as a participation, sort of like jump to the chase too early.
[00:06:12 - 00:06:16] What do you think I'm expecting sort of from you?
[00:06:16 - 00:06:18] Anyone can go on the fly here.
[00:06:18 - 00:06:20] We can get through this nice and quickly.
[00:06:20 - 00:06:23] Two participate yet. Anyone else?
[00:06:23 - 00:06:33] Yes. So to interact with other students and to do that in a positive and open way I suppose.
[00:06:33 - 00:06:36] So there'll be times we'll be writing down ideas.
[00:06:36 - 00:06:41] You know, we want to make sure that we're welcoming of ideas and not to judge me into one of the first instance.
[00:06:41 - 00:06:43] Yeah. Anything else?
[00:06:43 - 00:06:45] We said write down three things.
[00:06:45 - 00:06:47] Is the third thing that we think of?
[00:06:47 - 00:06:51] Ask impressions, especially when they're prompted.
[00:06:51 - 00:06:56] Or if something's like a not making sense or I've not done a good job of explaining it.
[00:06:56 - 00:06:59] Just shut your hand up and we can go through there again and that's super helpful for everyone.
[00:06:59 - 00:07:05] So I'm sure you wouldn't be the only person that's sort of having that sort of situation happening.
[00:07:05 - 00:07:09] Cool. So in this tutorial, we have 50 minutes.
[00:07:09 - 00:07:14] So actually 43 minutes going from now and to go over these things.
[00:07:14 - 00:07:21] Hopefully we'll kind of get through this which will mean that we're in a really good position for Friday to kind of get stuck into some of the example calculations.
[00:07:21 - 00:07:27] We should have a really good understanding of what is actually required of you for this assignment.
[00:07:27 - 00:07:30] And if you want to, you can kind of pick up some other menu strips.
[00:07:30 - 00:07:34] Hopefully, if then they will be kind of be out of the outside and sign you guys off if you want to.
[00:07:34 - 00:07:39] Kind of really get stuck into some of that material to this thing which I realized that Oscar was sort of talking about.
[00:07:39 - 00:07:45] We hadn't really talked about it yet. Hopefully, that will make a lot more sense while we had Oscar kind of come and chat to us this morning.
[00:07:45 - 00:07:50] Cool. So you can find the assignment brief under the assignment one tower loan.
[00:07:50 - 00:07:52] Has anyone seen it found it yet?
[00:07:52 - 00:07:55] Yeah, at least three people. That's pretty good.
[00:07:55 - 00:08:01] So I definitely recommend downloading it and making sure you're actually kind of read through it.
[00:08:01 - 00:08:05] In detail, or at least make sure you're understanding what it is.
[00:08:05 - 00:08:12] So if you go onto our enemie 301 page, we'll go into Summit 1, LA menu structure.
[00:08:12 - 00:08:16] And you'll see here on the top we have enemie 301, Summit 1.
[00:08:16 - 00:08:23] And I'll probably save this and it'll mean I can open it in this window here.
[00:08:23 - 00:08:28] So I'm just going to use this as my kind of document that I'll refer to as we talked through it.
[00:08:28 - 00:08:32] But there will also be a couple kind of prompts that have been re-emphasized in the PDF.
[00:08:32 - 00:08:41] But the idea is that this should be basically one source of truth for everything that you need to know about assignment, the assignment details and the instructions.
[00:08:41 - 00:08:49] So similar to what we said earlier today, these assignments are trying to get you to do what professional engineers do.
[00:08:49 - 00:08:58] And in this case, you'll be designing a structure to carry a load using your own calculations and material properties from tests.
[00:08:58 - 00:09:08] And so your task for the assignment, as we saw in the video, is to design and build a pen-jointed structure for the application shown in the diagram in figure 1.
[00:09:08 - 00:09:10] The structure must support a massive 20 kg.
[00:09:10 - 00:09:15] That's why they were like cheering and being real stoked when they got to 20 kg.
[00:09:15 - 00:09:21] And the video and it also needs to break before 39 kgs.
[00:09:21 - 00:09:23] Only materials to be used are those provided.
[00:09:23 - 00:09:28] So we have aluminium strips which we have a bunch of here.
[00:09:28 - 00:09:35] And then we will also provide you with a two-poxy glue, a rolled light.
[00:09:35 - 00:09:44] And also we will be able to use 3.2 millimeter aluminium pop rivets to join individual members together.
[00:09:44 - 00:09:52] So again, I've brought some individual members along that kind of show those jointing methods being used.
[00:09:52 - 00:09:58] So sort of hard to show you, if you're not super close, it doesn't make so much sense.
[00:09:58 - 00:10:02] But here we see an example of something that's being glued together.
[00:10:02 - 00:10:08] You can see there's lots of glue in there, but that's how they've made their individual member being the IB in this case.
[00:10:08 - 00:10:15] And then you could also, well, what we need to do is also have our pop rivets being used as a joining method, right?
[00:10:15 - 00:10:20] So here we see we have this kind of team member that has used those rivets,
[00:10:20 - 00:10:24] kind of put the individual member together.
[00:10:24 - 00:10:29] So all in all, you may have a 3-minber structure or a 2-minber structure.
[00:10:29 - 00:10:33] If you really wanted to, you could have them more than 3-minber structure,
[00:10:33 - 00:10:37] but because you'll see in the March sheet is a mark based on your strength-to-late ratio,
[00:10:37 - 00:10:40] you're not really benefited from doing that.
[00:10:40 - 00:10:48] And we'll kind of discuss a little bit more about kind of what our approach might be in the lecture or the electoral on Friday.
[00:10:48 - 00:10:55] Cool. So as it's to be done in peers, either kind of talk to your classmates and work out who you want to do with it.
[00:10:55 - 00:10:56] It just sounds like a group.
[00:10:56 - 00:11:01] And then you'll need to register that your partners on the Learn page.
[00:11:01 - 00:11:09] So if we go back to the Learn page under this tab here, we'll see that we have here, Summit 1 Group South-Select.
[00:11:09 - 00:11:15] So if you click on that, there'll be a bunch of different ones that you can become a member of.
[00:11:15 - 00:11:20] Obviously you want to kind of coordinate with your partner that you both become a member of the same team.
[00:11:20 - 00:11:24] Basically what that does is it links your submission for when you go to subnet anything on Learn,
[00:11:24 - 00:11:26] so that you'll kind of see the same sort of stuff right.
[00:11:26 - 00:11:31] So it makes it kind of straightforward as to who you both will see on Learn.
[00:11:31 - 00:11:39] Cool. If you're struggling to find a partner, you can also post on this partners for a Summit 1 Forum.
[00:11:39 - 00:11:43] And I just ask that you probably delete your posts if it's successful right.
[00:11:43 - 00:11:49] So that means that you know you can say I'm looking for a partner, then someone can provide you email.
[00:11:49 - 00:11:52] And they can email you and then you can kind of go from there.
[00:11:52 - 00:11:53] Cool.
[00:11:53 - 00:12:02] So the idea is that everyone is kind of partner up for this assignment because engineers often work in teams obviously.
[00:12:02 - 00:12:05] Cool. So that's those things there.
[00:12:05 - 00:12:13] We can also at the end of this lecture if you're like looking for a partner still, we could just say like, hang out over here and exchange details or that sort of thing.
[00:12:13 - 00:12:16] Cool. So we see here, main dimensions of the testing apparatus.
[00:12:16 - 00:12:22] The main dimensions on the testing apparatus and the required dimensions for your structure or detail in the figure 1A.
[00:12:22 - 00:12:27] There's detail in the figure, the horizontal distance between 0.0 where the load is attached.
[00:12:27 - 00:12:31] Where the load attachment is placed in the support pins is 400 millimeters.
[00:12:31 - 00:12:34] This point may be placed anywhere vertically inside the first big spools.
[00:12:34 - 00:12:37] It's indicated by the orange dotted lines for two new structures.
[00:12:37 - 00:12:39] All dimensions are measured at a load of 20 kg.
[00:12:39 - 00:12:45] Figure 1B is an example of an aluminum structure which we've also seen a video of.
[00:12:45 - 00:12:48] Sort of updated this figure hopefully to make it super clear.
[00:12:48 - 00:12:53] But the main thing is that this dotted line is where we have our load attachment.
[00:12:53 - 00:12:59] This thing here and as long as your device or your system is able to be inside this perspective,
[00:12:59 - 00:13:07] I'm not kind of a hit this table obviously is kind of a lower point that you could actually angle that you can go there.
[00:13:07 - 00:13:11] So here we have some one possible shape that your structure could be within.
[00:13:11 - 00:13:19] As you see it could be a right angle triangle with right angle in the bottom right corner or in the top or some combination or a two-mill infrastructure.
[00:13:19 - 00:13:23] Or something else. You guys are the designs that's your best decision.
[00:13:23 - 00:13:29] So is there any questions on this figure at the moment?
[00:13:29 - 00:13:36] Whereas they're like super clear that you understand that from this point to this pin it needs to be 400 millimeters plus a minus 3 millimeters.
[00:13:36 - 00:13:46] And from this pin to this pin 280, another than that the design is sort of up to you.
[00:13:46 - 00:13:50] So what we'll see here is that this support is on rollers.
[00:13:50 - 00:13:57] And so that means that if you have a two-mill infrastructure basically this point here is going to take no vertical load.
[00:13:57 - 00:14:04] So it will mean that if you have a two-mill infrastructure the shape is kind of locked in by physics.
[00:14:04 - 00:14:11] So there will be a slightly going to be a very small angle above the horizontal.
[00:14:11 - 00:14:16] That will talk about that. We can talk about that more and more and more if people are interested.
[00:14:16 - 00:14:25] Cool. So any questions?
[00:14:25 - 00:14:30] I mean the fighters of it will kind of show you everything you need to know.
[00:14:30 - 00:14:37] The bits are sort of distributed a wee bit around the place because I don't want to lose them because I've like weighed them in their all specific.
[00:14:37 - 00:14:45] Yeah. We can again bring it along but I don't know how helpful it is to actually see it or not.
[00:14:45 - 00:14:49] Basically what you have is these two kind of brackets they hold pins.
[00:14:49 - 00:14:55] So as long as you can pin and joint, if you made the structure and you pinned it together then you know we'll put in the testing apparatus as long as it's not.
[00:14:55 - 00:15:02] Why did it in 50 mill which we have is one of the things that if we really do want to see it, I can possibly bring it along to a tutorial.
[00:15:02 - 00:15:07] It's just like real heavy and like I'm not that strong.
[00:15:07 - 00:15:11] Otherwise I could just bring it up to my office or I could bring it to a drop in session.
[00:15:11 - 00:15:13] That's probably an easy one.
[00:15:13 - 00:15:16] Yeah. In different way they have them.
[00:15:16 - 00:15:20] Any other questions? Cool.
[00:15:20 - 00:15:25] All right. So submission you'll see here that we have two parts of the submission and there's also two parts of the assignment.
[00:15:25 - 00:15:32] Obviously one being your calculations, your report and your drawings and then one being the actual results of what you did on the test day.
[00:15:32 - 00:15:43] And so because you'll get your design checked off before you're able to do testing, what we need you to do is submit your drawings in A3 to the physical drop box.
[00:15:43 - 00:15:49] So that's why you'll see here that there's an electronic submission for your report calculations and drawings.
[00:15:49 - 00:15:53] That's so that we can market quite straightforwardly and not lose your physical assignment.
[00:15:53 - 00:15:56] Like they used to in the old days.
[00:15:56 - 00:16:04] But then we also do want this physical submission because for some reason students aren't always the best at having their name on their drawings.
[00:16:04 - 00:16:15] So that means if I go in front and all out I get like a million assignment ones done by student xxx which is then kind of problematic for me order in terms of the test day and stuff.
[00:16:15 - 00:16:17] So it's kind of a logistical thing.
[00:16:17 - 00:16:28] So you'll see there that there's also this modes of failure sheet which I encourage students to attach to their drawings and we'll see that that's this thing here.
[00:16:28 - 00:16:31] Which just says what your team name is.
[00:16:31 - 00:16:37] Well your team members both your names what failure load you're going for and what your first second and third mode of failure are.
[00:16:37 - 00:16:42] Because otherwise I've had students kind of get to the front of the line and go cool yet George I'm ready to go.
[00:16:42 - 00:16:45] My thing's going to break it 25 kg at the stress concentration.
[00:16:45 - 00:16:57] I go okay what's your second mode of failure and it's like I can't remember if it's the horizontal beam buckling in the explain or the why plane actually what is the explain what is the why beam I can't remember what we did so.
[00:16:57 - 00:17:13] That's why I encourage you guys to just have it written here so they're on the test day guys it goes smoothly and if you have forgotten at least your previous self is kind of seeing your a message to remind you what you did on the test well did for.
[00:17:13 - 00:17:30] So you can see at a glance this is what the assignment is required and this is a concise version of basically what it's telling us on the mark sheets which I think there's a better way to kind of go about it probably makes a little bit more sense than just these bullet points alone.
[00:17:30 - 00:17:37] So you can see that these are the rules I'm going to read them just for completeness so I know that you guys are aware of them.
[00:17:37 - 00:18:00] So all in connections must be pinned not glued so that's where those three attachments to the supports of the load attachments are individual members must be fabricated using either two part epoxy glue or aluminium pop rivets and you'll see in that earlier slide that we say at least one member needs to be constructed using each.
[00:18:00 - 00:18:15] So if you've got a premium destruction you could have two that are glued and one that's just riveted or vice versa but if you just go all glue or over in you'll kind of get a deduction and marks relative to not meeting that requirement.
[00:18:15 - 00:18:23] And no point shall the width of the structure be greater than 50 mill that's just because that's the inside dimension of the kind of load attachments.
[00:18:23 - 00:18:28] So if you're wider than that you can actually physically put your structure in the testing apparatus.
[00:18:28 - 00:18:37] You see that point oh maybe anywhere on that dotted line and within the perspicks eight millimeter pins will be supplied for you.
[00:18:37 - 00:18:45] I do put a cup out but they seem to always go missing we need to put one like on like a safety chain or something so that people can check their holes.
[00:18:45 - 00:18:57] So it depends but don't take them home because otherwise I get technicians complaining that they have to machine too many eight millimeter pins that exactly the same kind of links so that the masses sort of consistent.
[00:18:57 - 00:19:00] Plus the time I'm sure people ask me about that.
[00:19:00 - 00:19:09] Blaine and scrutiny and process will take place during the structure testing day and this will be the weight of the structure without pins which will use to calculate the strength to weight ratio.
[00:19:09 - 00:19:14] Only the two test supports shown and the figure can be used.
[00:19:14 - 00:19:23] You're testing apparatus well we can make it available in due course sounds like a drop-in session might be a good place for us to do that so I don't have to carry it.
[00:19:23 - 00:19:28] Too far your structure must be designed to fail at a stress concentration.
[00:19:28 - 00:19:34] The thing of members for weight reduction will be allowed as long as the failure is at a stress concentration.
[00:19:34 - 00:19:42] Now this is one of those things that I try and say kind of comically too many times so your device must fail at a stress concentration.
[00:19:42 - 00:20:01] The structure must fail at a stress concentration just because every year there's about one or two groups that shows up on Tuesday and they just have like a send out in the like verse and they're like I it's so reliable George I know it's going to break somewhere along this reduced section.
[00:20:01 - 00:20:02] So you're not.
[00:20:02 - 00:20:15] So similarly we've got these ones here these are probably actually not failure members but they are probably for a top right angle triangle three in the structure.
[00:20:15 - 00:20:26] As we can see here this person or this group has made a bunch of weight saving holes and they've had a notch at the end for this stress concentration.
[00:20:26 - 00:20:33] Alternatively this is one that hasn't broken so you can see that they have a hole for this stress concentration.
[00:20:33 - 00:20:44] Cool so hopefully that's really clear sometimes what people try to do is like obviously if you condense what this reduced section is eventually becomes a notch right.
[00:20:44 - 00:20:54] So it's like a great area of like if you made like a dog bone shaped thing in the middle how big does that dog go and have to be to not be a stress concentration.
[00:20:54 - 00:21:16] Yeah so just to make that really clear I say just do a hole or a notch you have a thing that looks like a dog bone then I kind of like stress on the day because it means I have to then interrogate the calculations and work out whether you actually assumed it was a stress concentration or whether you said we picked a dog bone because it was a cave area of one which is essentially no stress concentration.
[00:21:17 - 00:21:28] Cool hopefully that's clear but hole or a notch is probably something that I would note down now so that you know that you can't forget that and then again we also have.
[00:21:28 - 00:21:41] These are the set for a visual member is not allowed so you can't have some like little stress concentration fourth member that just has intention hanging off the load attachment to kind of make it fairer.
[00:21:41 - 00:21:44] So it has to be one of your kind of main members.
[00:21:44 - 00:22:10] Cool and then obviously manual assistance for a much failure will incur a loss of marks and for full transparency there is these similar typical penalties that have applied in previous years and so that just to make sure that you're aware of it and you don't say on test they are Georgia I didn't know that if we didn't make our structure to the horizontal vertical distances within the figure one that it loses in the marks.
[00:22:10 - 00:22:14] I can go well if you read this I'll remove the size of it in a completely.
[00:22:14 - 00:22:25] So you can see here on the test day we have these penalties so if you if you've made the dimensions not to the standard then there's a five mark penalty.
[00:22:25 - 00:22:31] If you've had to file some things or open up your pin holes that you make your thing go to gear they're causing time delay.
[00:22:31 - 00:22:45] There's a two mark penalty just because I want everything running like clockwork on the test days because here's a lot of you and the time that it takes to be able to delay can just really make things basically take forever.
[00:22:45 - 00:22:50] So if you don't have a stress concentration which is a whole or not there's a 10 mark penalty.
[00:22:50 - 00:22:59] If you're outside your tolerance on your stress concentration which we've said stress concentration tolerances plus or minus 0.1 up to 20 marks.
[00:22:59 - 00:23:01] Why is it such a house penalty?
[00:23:01 - 00:23:19] Well that basically means that you've deliberately tried to adjust what your calculations were because that's obviously the critical part of your of your design, deliberate changing the design from what was on the drawing with no forewarning up to 20 marks.
[00:23:19 - 00:23:27] So similar to I suppose like the warming competition or any other as soon as you have to do you sort of have to make what you say you're going to make is what we're saying there.
[00:23:27 - 00:23:35] So similarly if you just unbatently change your design the same thing as the one above just slightly differently phrased.
[00:23:35 - 00:23:41] So sometimes things will kind of go wrong late in the play and then I go oh the glue wasn't sitting so I checked upon some rivets in there.
[00:23:41 - 00:23:52] So I'm going to say well you need to paint an advance match we've done a time to do the glue and now you've changed your design which is going to not kind of make our quality assurance sort of side of things.
[00:23:52 - 00:24:04] Go in another see we've got this requirement of the different manufacturing techniques during testing if you kind of dropping or adding more force to make it break at a certain point.
[00:24:04 - 00:24:11] So you're going to use these of 20 or 10 marks and always make my kind of gap drop want to see people sort of do it.
[00:24:11 - 00:24:19] And then we have it all recorded so if we have to go to the TMA we can with ideas basically engineers act with integrity.
[00:24:19 - 00:24:29] So this realistically shouldn't be a problem but sometimes people kind of know that they might have over designed their thing based on looking whatever our house is doing and then panic on the day.
[00:24:29 - 00:24:35] What we try and do is make the be a smaller consequence for acting with integrity.
[00:24:35 - 00:24:43] And then if you have had some things go wrong that weren't kind of foreseen and you had to make a change to design and test it again.
[00:24:43 - 00:24:52] If you're often allow some retest to happen in the weeks after week eight these are kind of the penalties depending on what is that you're changing so that you can make your design.
[00:24:52 - 00:24:55] And you can make this specification and get a passing grade.
[00:24:55 - 00:25:00] And so just the highlight professional approach and forewarning will reduce the penalties.
[00:25:00 - 00:25:07] If you spot an error and you've designed for test aid get in touch with the lecturer immediately and we can work through these changes.
[00:25:07 - 00:25:21] So if you know our George on reflection where you have worked out that I think if you want to go to get it because we haven't done this then we can make that change in advance and did be a reduced penalty which is basically synonymous of what would happen.
[00:25:21 - 00:25:33] If you were working in the real world right so a lot cheaper to make a change before you start making something rather than go like sweet let's make this bridge and then I work out we needed to actually make this whole thing different.
[00:25:33 - 00:25:37] It's going to be a bit more expensive.
[00:25:37 - 00:25:38] Cool.
[00:25:38 - 00:25:45] So with that we can see that we've gone through that and we have read most of the detail.
[00:25:45 - 00:25:55] Here's an example of what our goal is and again just saying for completeness I've included some summaries of what we just kind of went over.
[00:25:55 - 00:26:04] One thing that I didn't touch on is that there is this teammate rating that you'll need to do.
[00:26:04 - 00:26:11] And so that's actually I need to kind of peek this thing I don't quite want to look at.
[00:26:11 - 00:26:13] So good we are a little bit.
[00:26:13 - 00:26:25] So AI useful saying that I kind of went through you can see these are the two things that we're kind of saying that you can use AI for and then just make sure that whether you use AI or not you just for that declaration.
[00:26:25 - 00:26:28] If you haven't used it it's easy to see no where I was used.
[00:26:28 - 00:26:33] If you have used it for some stuff then you can include that declaration of AI.
[00:26:33 - 00:26:36] And then similarly we have these teammate ratings.
[00:26:36 - 00:26:46] I think the one I've updated this I have explicitly put what the what the deadlines are for for these teammate ratings right.
[00:26:46 - 00:26:56] So they're just 10% of each of those grades will be based on the Web in D I think is the calculation software that learn users.
[00:26:56 - 00:27:02] Basically between the 17th and the 25th you'll be required to complete that.
[00:27:02 - 00:27:17] And there's just like three questions there just you know one to four or one to five scale to kind of feedback your to give feedback about what your how you guys worked as a team I suppose.
[00:27:17 - 00:27:25] And so if you don't complete it then you will lose the marks for completing the teammate rating.
[00:27:25 - 00:27:30] And last year I think it was a bit of a meme because it was the first time I've done it I could not be standing it because people hadn't done it.
[00:27:30 - 00:27:37] But I just have to be cut for it this year and say sorry guys this is the date set it's open and this is the date set it's closed and if you miss it.
[00:27:37 - 00:27:42] I'm sorry but you've missed it and the second one will be available during.
[00:27:42 - 00:27:49] I'll make it visible to you guys and due course with the idea is that it's something that you can fill out on the test day.
[00:27:49 - 00:27:56] Which being talks about actually how you guys work as a team to kind of manufacture your device.
[00:27:56 - 00:27:57] Yeah.
[00:27:57 - 00:28:00] So that kind of hopefully clear.
[00:28:00 - 00:28:08] There's a little bit of a headache for me because the sun raising the learn system which you think would just be able to like look nicely to different grades is like not that nice.
[00:28:08 - 00:28:10] So I've been manually put in all the grades for each of the groups.
[00:28:10 - 00:28:13] So then goes input for the teammate rating.
[00:28:13 - 00:28:21] So that's why I have to make sure that it's done by that time because then the mate teammate rating is kind of based on that next kind of thing.
[00:28:21 - 00:28:22] Yeah.
[00:28:22 - 00:28:23] Cool.
[00:28:23 - 00:28:26] So I do have some common questions.
[00:28:26 - 00:28:30] People ask can we use if you had to check hand calculations.
[00:28:30 - 00:28:34] The short answer is no we don't really talking about using if you are in this class.
[00:28:34 - 00:28:37] If you use it then I can't police you to not use it.
[00:28:37 - 00:28:43] But I don't think we've kind of gone over what the assumptions of the if you are and whether we're doing nonlinear.
[00:28:43 - 00:28:48] If you are to understand the failure or the plastic information of our simulation.
[00:28:48 - 00:28:55] So in short we're just basing doing the old school way the reliable way of hand calculations and clear assumptions.
[00:28:55 - 00:28:59] People ask about those 800 word report does it include words that are on the figures.
[00:28:59 - 00:29:02] Does it include words that are on the tables how strict you're going to be.
[00:29:02 - 00:29:04] It's just the body text.
[00:29:04 - 00:29:05] Yeah.
[00:29:05 - 00:29:08] That's obviously way too big that you're going to get penalized.
[00:29:08 - 00:29:13] But basically what you should do is write what your word counters for your body text.
[00:29:13 - 00:29:18] If this is in the figure we're not going to be in the figure you're going through that.
[00:29:18 - 00:29:23] And then eight page limit that's just for your calculations.
[00:29:23 - 00:29:29] You know advance it is quite compact but it means you have to just see that what you do quite clearly.
[00:29:29 - 00:29:34] So that it doesn't go over 20 pages or you know you can really try and drag things out.
[00:29:34 - 00:29:40] So obviously there not required and it's not marked if you do FBA.
[00:29:40 - 00:29:43] I get clear of the reader.
[00:29:43 - 00:29:46] And so we'll talk a little bit about the report hearings.
[00:29:46 - 00:29:51] And second do you want to discuss what I would recommend for hearings as your report.
[00:29:51 - 00:29:53] Do you want to discuss that?
[00:29:53 - 00:29:54] Cool.
[00:29:54 - 00:29:58] So here is the one A March sheet and I would use these as the headings for your report.
[00:29:58 - 00:30:07] So I'll start with the introduction design development, testing section, the results and then overall you'll be obviously marked on your report quality.
[00:30:07 - 00:30:09] I wouldn't put that as one of the headings.
[00:30:09 - 00:30:18] And so with that results and then I would probably just go final design and then that final design I'd make sure these things are clear.
[00:30:18 - 00:30:21] Do you want me to write it down on the piece of paper?
[00:30:21 - 00:30:22] Is that okay I would say?
[00:30:22 - 00:30:28] Introduction design development which is where you might say oh we thought we were going to do these ones.
[00:30:28 - 00:30:30] Then we chose this one for this reason.
[00:30:30 - 00:30:33] This is the sheet we used to get our material results.
[00:30:33 - 00:30:34] We did this material existing.
[00:30:34 - 00:30:36] Here's a summary of our results.
[00:30:36 - 00:30:38] And then here's our final design.
[00:30:38 - 00:30:41] Here are the failure modes and the failure loads.
[00:30:41 - 00:30:44] Cool.
[00:30:44 - 00:30:47] So this is the March sheet that the markers will be using.
[00:30:47 - 00:30:50] You can see for B1 and B2 it hasn't been completed yet.
[00:30:50 - 00:30:53] And these are time sheets.
[00:30:53 - 00:30:55] So time sheets should be kind of clear.
[00:30:55 - 00:30:58] Drawings also should be kind of clear.
[00:30:58 - 00:31:01] You'll have maybe any on how many members you have.
[00:31:01 - 00:31:06] Two to four drawings is probably a typical kind of amount.
[00:31:06 - 00:31:09] Enough detail so that it can be manufactured.
[00:31:09 - 00:31:12] You'll have a set of calculations which is our eight pages.
[00:31:12 - 00:31:16] And these are some ideas of the kind of calculations that you might be doing.
[00:31:16 - 00:31:18] And the markers might be looking for.
[00:31:18 - 00:31:22] And then these first four things are all looked for in your report.
[00:31:22 - 00:31:27] So you'll have these short introduction and design development.
[00:31:27 - 00:31:30] You'll have a short summary of this is the material system you did.
[00:31:30 - 00:31:35] You have some photos showing your dog bones in a table showing your average results or the main results.
[00:31:35 - 00:31:38] And then you'll have a description of your final design.
[00:31:38 - 00:31:42] Which you might say, you know, here's what my final design looks like.
[00:31:42 - 00:31:46] Does everyone agree to having a figure of your final design is probably a good idea?
[00:31:46 - 00:31:47] Every year.
[00:31:47 - 00:31:51] Someone will complaints me again going, I didn't know where to put a figure in well.
[00:31:51 - 00:31:54] It's kind of what the whole report's about.
[00:31:54 - 00:32:00] And then you'll have clear detail about what your failure loads are in your failure modes, right?
[00:32:00 - 00:32:03] Any questions on this?
[00:32:03 - 00:32:11] I feel like I'm often susceptible to going like this is so clear for me because I wrote this in review.
[00:32:11 - 00:32:13] But to you it might not be.
[00:32:13 - 00:32:16] Anything on that that doesn't make sense of sort of happy days.
[00:32:16 - 00:32:18] So that's on learn as well.
[00:32:18 - 00:32:26] And then similarly we can see that we have a fake mark sheet for,
[00:32:26 - 00:32:28] does anyone know who these people are?
[00:32:28 - 00:32:33] Little eastery for you can look about maybe one day.
[00:32:33 - 00:32:35] Tell me if you're, someone emails it to me.
[00:32:35 - 00:32:38] I can, I'll make a prize.
[00:32:38 - 00:32:42] But anyway, what we can see is this is what the mark sheet will look like.
[00:32:42 - 00:32:46] So on the test hour you'll be screwed in by Tony and co.
[00:32:46 - 00:32:50] And as long as they're happy that your design has been made to your drawings,
[00:32:50 - 00:32:54] you'll get a pass there and that will allow you to kind of talk to me.
[00:32:54 - 00:32:59] Outline what your loads and modes are and then go and complete the test.
[00:32:59 - 00:33:03] Depending on how well the test goes, it will either get a pass or fail
[00:33:03 - 00:33:05] if you are over 20 kg.
[00:33:05 - 00:33:09] Yes, so if you're at 21 kg you get the 10 marks.
[00:33:09 - 00:33:12] If you're at 60 kg you get the 10 marks.
[00:33:12 - 00:33:16] The second one here is 10 marks if you are within these range,
[00:33:16 - 00:33:17] this range wrap.
[00:33:17 - 00:33:19] So if you're in between 20 and 39.
[00:33:19 - 00:33:25] And the key thing to note here is that the total load includes the mess of the
[00:33:25 - 00:33:28] hanger which is like 1.09 kg.
[00:33:28 - 00:33:31] So then the slides for our tutorial.
[00:33:31 - 00:33:36] So if you put 20 kg mess on, basically that means the total load is 21.09.
[00:33:36 - 00:33:37] Right?
[00:33:37 - 00:33:39] Sometimes it's just people up when they start sharing it.
[00:33:39 - 00:33:44] They put 39 kg on but really they put 40.09 kg on and the outside the range wrap.
[00:33:44 - 00:33:45] Cool.
[00:33:45 - 00:33:49] So again, there could be just a little thing to the asterisk if you're on there.
[00:33:49 - 00:33:53] On your tablet or on writing down some notes is that the load is the total load.
[00:33:53 - 00:33:56] So, protected failure load.
[00:33:56 - 00:33:58] I've slightly updated this this year.
[00:33:58 - 00:34:02] If you're super close you'll get 10 marks so plus or minus 15 percent.
[00:34:02 - 00:34:05] And if you're within plus or minus 25 percent and you get 7 marks,
[00:34:05 - 00:34:09] the outside plus or minus 25 percent, no marks.
[00:34:09 - 00:34:10] Cool.
[00:34:10 - 00:34:13] Next we have predicted failure mode, first, second and third.
[00:34:13 - 00:34:16] So if it fails at your first stress concentration,
[00:34:16 - 00:34:18] you get 10 marks of it.
[00:34:18 - 00:34:21] Failed it a second could have been buckling of your horizontal membrane to the
[00:34:21 - 00:34:22] first picks.
[00:34:22 - 00:34:23] You get 7.
[00:34:23 - 00:34:27] If it's the third, maybe shear stress at the pins.
[00:34:27 - 00:34:30] It's unlikely I'm being stressed at the pins or pull out stress.
[00:34:30 - 00:34:31] I don't know.
[00:34:31 - 00:34:35] Whatever you guys work up by your calculations and you get 5 marks there.
[00:34:35 - 00:34:42] Strength to weight is calculated automatically based on your predicted load and your,
[00:34:42 - 00:34:46] the mass of your device without pins.
[00:34:46 - 00:34:48] And we can see that the breakdown is here.
[00:34:48 - 00:34:54] Last year I think there was one or two groups that got 10 out of 10 for that.
[00:34:54 - 00:34:55] Yeah.
[00:34:55 - 00:34:58] Most people kind of get somewhere in the middle.
[00:34:58 - 00:35:03] It's kind of the idea is that I've got a nice macro kind of running in my spreadsheet
[00:35:03 - 00:35:06] so I can just give you the marks kind of straight away.
[00:35:06 - 00:35:09] And so that reason that's why I've kind of outlined what these are just like.
[00:35:09 - 00:35:11] That's cool.
[00:35:11 - 00:35:12] Happy.
[00:35:12 - 00:35:14] Any questions on any of that?
[00:35:14 - 00:35:22] So you'll get a filled out with your names on this version after you've done your tests
[00:35:22 - 00:35:23] on the test day.
[00:35:23 - 00:35:30] So this is what it looks like on the test day.
[00:35:30 - 00:35:35] I really like Tony's leg in the, I know that I was trying to do, but you can see basically
[00:35:35 - 00:35:40] we have a stack of, stack of our drawing that you've submitted by hand.
[00:35:40 - 00:35:44] I'll have them perfectly ordered matching the test day kind of order, which will be organized
[00:35:44 - 00:35:45] relative to your schedules.
[00:35:45 - 00:35:48] I'm actually, you guys can both attend it.
[00:35:48 - 00:35:50] You'll get your way in and your scoot there.
[00:35:50 - 00:35:52] A little bit like botting.
[00:35:52 - 00:35:57] And then you'll come to me and I'll fill out what your modes of failure are and make sure
[00:35:57 - 00:35:58] that everything's right.
[00:35:58 - 00:36:02] And this big screen here makes sure that you can do, check that I'm doing a good job because
[00:36:02 - 00:36:05] it's pretty easy for me to write something slightly wrong.
[00:36:05 - 00:36:07] Then from here we've got two testing stations.
[00:36:07 - 00:36:11] There'll be a TA that kind of supervises it and makes sure you're doing the right thing.
[00:36:11 - 00:36:16] We'll have a video going on here so if we ever need to do any TMO stuff, we can go
[00:36:16 - 00:36:20] and look, there's sometimes two things might kind of fail very similarly and we need to know,
[00:36:20 - 00:36:25] okay, was it just concentration in that broken that cause that look like a buckled or was it vice versa?
[00:36:25 - 00:36:26] Cool.
[00:36:26 - 00:36:28] So that's what I look like on the test day.
[00:36:28 - 00:36:32] It's talked about screwing your checking that it's built to your drawings and that acceptable
[00:36:32 - 00:36:36] to lancers for your general tolerances plus or minus 0.5 millimeter.
[00:36:36 - 00:36:40] And we've talked about these things here, so I'm just going to keep going through them.
[00:36:40 - 00:36:43] Here's some historic photos.
[00:36:43 - 00:36:48] We're the one and only keyphal exam that in the middle there from what he kind of used to do back in the day,
[00:36:48 - 00:36:51] but now that can be replaced with me.
[00:36:51 - 00:37:00] Again, similarly we see some people getting the testing done and these photos kind of just let you see a bunch of the different kind of shapes
[00:37:00 - 00:37:03] or different ideas that people have kind of used.
[00:37:03 - 00:37:09] And hopefully these photos kind of give you some insights into what the different brackets kind of look like.
[00:37:09 - 00:37:14] So you can see there's this one here that's on a roller, this one here that's fixed in that load attachment in the middle.
[00:37:14 - 00:37:16] So that's our point O.
[00:37:16 - 00:37:20] We want that point there to be to be 400 mill plus or minus.
[00:37:20 - 00:37:21] Yeah.
[00:37:21 - 00:37:22] Cool.
[00:37:22 - 00:37:28] So the weights are only, I'm going to check my terminology.
[00:37:28 - 00:37:36] The masses are only 5 kg or 2 kg and that weight of the hanger and the chain is 1.09 kg.
[00:37:36 - 00:37:39] If it touches the wall, that's what we call a buckling failure.
[00:37:39 - 00:37:46] Otherwise a similar amount of deflection and the other excess is also what we would define as a failure.
[00:37:46 - 00:37:49] Ideally we want you to design to fail at the stress concentration.
[00:37:49 - 00:37:53] And when they did per speech you can actually see it sort of thinning which is kind of nice.
[00:37:53 - 00:37:56] You don't really keep that without current kind of thing.
[00:37:56 - 00:38:03] You must correctly predict how you structure fails and make sure you keep clear of the falling weights and you'll have shoes and safety glasses on.
[00:38:03 - 00:38:06] So here's some more design examples from previous years.
[00:38:06 - 00:38:09] So we can see this one here, a nice tube in the structure.
[00:38:09 - 00:38:17] It's been nicely thinned out with the top tension member and that's got a nice big chunk you can push them in but there.
[00:38:17 - 00:38:21] Here's another three in the structure so I possibly showed,
[00:38:21 - 00:38:26] could even be that exact one but a similar kind of member with the thinned ender.
[00:38:26 - 00:38:33] And here and then we have the classic right angle lower triangle here.
[00:38:33 - 00:38:36] Oh, there's another one there.
[00:38:36 - 00:38:39] Cool, so we've got a couple minutes.
[00:38:39 - 00:38:42] Can we quickly go through this?
[00:38:42 - 00:38:47] So before I can, it's just as simple I think we're good to hear what task you think need to be completed.
[00:38:47 - 00:39:01] So two minute timer, either talks to the person at you or write down what you think would be good to get started.
[00:40:01 - 00:40:06] Alright, alright, thank you everyone.
[00:40:06 - 00:40:12] What we're going to do is pause there.
[00:40:12 - 00:40:15] Alright, thanks everyone.
[00:40:15 - 00:40:19] We'll come in here.
[00:40:19 - 00:40:23] Need to do, I don't know.
[00:40:23 - 00:40:28] Hope thing very much, so what we're going to do is we're going to go through that list that you just kind of discussed in the hot second.
[00:40:28 - 00:40:33] But because I often can get sidetracked in the end of the end, have to be like that toy story,
[00:40:33 - 00:40:35] maybe I've just like going through everything super quickly.
[00:40:35 - 00:40:39] I'm just going to try and go through the material testing stuff so at least you know what's happening there.
[00:40:39 - 00:40:43] And then if we have time we can do some more on that planning tasks sort of thing.
[00:40:43 - 00:40:45] Otherwise we'll pick it up on Friday.
[00:40:45 - 00:40:50] So in terms of collecting your aluminium strips, which will be part of the tasks that you'll need to be completing.
[00:40:50 - 00:40:56] Hopefully if in the day we'll be kind of here shortly and we'll be able to sign off your nail on the sheets that you can click them.
[00:40:56 - 00:41:01] Please note that you're responsible for those strips where you put them in a safe place.
[00:41:01 - 00:41:03] I recommend you take them back to your flat.
[00:41:03 - 00:41:04] I know it's a bit of a pain.
[00:41:04 - 00:41:09] That's way better than like putting them somewhere that you think sneaky and somehow they've like being pet trapped by the cleaner or something.
[00:41:09 - 00:41:11] And then you've got no material.
[00:41:11 - 00:41:13] We've only got a limited amount of material.
[00:41:13 - 00:41:19] There's a little bit of buffer for like if people have to do retests, but the idea is that there's four strips per group.
[00:41:19 - 00:41:23] You're able to collect two strips per person.
[00:41:23 - 00:41:25] And that's what the way they will kind of manage it.
[00:41:25 - 00:41:28] So you have to pick up your own strips.
[00:41:28 - 00:41:38] Cool. Obviously from manufacturing your structure, there's drill presses and benches and the lights and handles in the workshop.
[00:41:38 - 00:41:41] Similar to what you guys were doing for your warm technology.
[00:41:41 - 00:41:45] So obviously these spaces here are also going to be useful as well as the undergraduate workshop.
[00:41:45 - 00:41:46] You heard from Tony.
[00:41:46 - 00:41:51] This is more for completeness, but I can show that you're aware of what hazards they might be in that you.
[00:41:51 - 00:41:52] Act appropriately.
[00:41:52 - 00:42:00] And the main thing is that if you see anything that's a little bit dusty or dangerous, make sure that you tell someone and report it.
[00:42:00 - 00:42:03] And don't be bringing in your own kind of power tools.
[00:42:03 - 00:42:07] That's another one that I've had strong words from the technicians about.
[00:42:07 - 00:42:14] But someone bought a micro grinder and it was using outside with jandals, which maybe is not the smartest idea.
[00:42:14 - 00:42:28] Built j
[00:42:28 - 00:42:39] general tips to make sure you look after your strip speed product.
[00:42:39 - 00:42:49] Use these folders or notches to make either notches or fold different kind of cross-sections.
[00:42:49 - 00:42:55] And obviously drill presses make sure that you're using the trick drills and that you don't have any kind of loose pieces.
[00:42:55 - 00:43:00] And we can see some information here about what they shoot with me tools.
[00:43:00 - 00:43:06] Again for completeness, I've finished this in here, but we'll probably go through this in a little bit more detail.
[00:43:06 - 00:43:09] But basically when you add glueing or come to glueing, it's all...
[00:43:09 - 00:43:24] Your preparation is very important to make sure that you get a nice surface bonding and we have also put up these links, which give you some more information about how to use those that glue appropriately.
[00:43:24 - 00:43:28] Please only glue on the workbenchers. There's another one there. Just got the windowsill's repainted.
[00:43:28 - 00:43:31] So the turning was like, oh, I forgot to tell them in the morning.
[00:43:31 - 00:43:37] So this is in here for completeness. And then pop rivets, both the glue and the pop rivets will be available.
[00:43:37 - 00:43:43] From the technicians, we have a video here that you can click on and see how you actually do some riveting.
[00:43:43 - 00:43:53] And I'm sort of closely linking this to our sustainable development goals to all mean that your structures will be a lot more recyclable if they don't have a bunch of set glue on them.
[00:43:53 - 00:44:06] So we're able to recycle that there. And so here are some of the documents that we can discuss in further that they just tell us the typical data about what is the strength of the glue in terms of an engineering metric like
[00:44:06 - 00:44:07] or a piece of steel.
[00:44:07 - 00:44:15] So if you want to be in convert that and similarly for our rivets, they do have like a tear out stress.
[00:44:15 - 00:44:18] So obviously you have to build your own drawings.
[00:44:18 - 00:44:24] I'll build your structure to your own drawings. It's your polyure using hand tools, cutting and filing and drilling.
[00:44:24 - 00:44:34] Well, drilling is not a hand tool, but you won't be using things like laser cutters or CNC machines, just because there's way too many of you to try and get either run through those.
[00:44:34 - 00:44:41] So obviously once you build your structure, make sure you do a trial assessment and make sure you give yourself enough time for the glue to set.
[00:44:41 - 00:44:46] There's always someone on t-stay that the glue is like goopy still when I'm like, I know if that's going to hold.
[00:44:46 - 00:44:49] How might be you fairly low there you might need to put us number one kind of thing.
[00:44:49 - 00:44:55] So yeah, and obviously be careful if you're sharp edges and that sort of thing.
[00:44:55 - 00:44:56] Cool.
[00:44:56 - 00:45:03] So when it comes to material testing, you'll be using those houndsfield tinsometers which Oscar talked about.
[00:45:03 - 00:45:09] So you'll want to find things like the ultimate tinsale strength, the yield points and the young's modulus.
[00:45:09 - 00:45:13] And then you also want to determine the failure force for a chosen stress concentration.
[00:45:13 - 00:45:17] So it's sort of two levels to the type of material testing that you do.
[00:45:17 - 00:45:22] You all need to bring your USB stick to kind of take your results away and make sure you save them.
[00:45:22 - 00:45:24] So I've also had people go like, oh, I forgot to save my results.
[00:45:24 - 00:45:27] And now I don't did all this work and have nothing to show for it.
[00:45:27 - 00:45:31] But if you're from Oscar, this is what the houndsfield tinsometer looks like.
[00:45:31 - 00:45:34] There's some videos online that kind of show you how to use them.
[00:45:34 - 00:45:40] If you go on there and you talk to Oscar, once you've got a dog bone here, we'll also be able to kind of assist very keen.
[00:45:40 - 00:45:45] But I think most of the time they're probably available actually slightly earlier if you're a morning person.
[00:45:45 - 00:45:48] I think Oscar's in there normally just after eight.
[00:45:48 - 00:45:54] But yeah, it'll be able to tell you what time they are available when that lab is kind of open.
[00:45:54 - 00:45:57] So you'll be making your own kind of dog bones.
[00:45:57 - 00:46:00] You'll probably follow them into the shape.
[00:46:00 - 00:46:03] And here's an example of some that are being made from perspex.
[00:46:03 - 00:46:10] And here's an example kind of result sheet that kind of talks about working out what the failure stress kind of was.
[00:46:10 - 00:46:13] So this could be a good thing to kind of do in the first instance.
[00:46:13 - 00:46:18] If you're just looking at your UTS, then you don't actually need to have that stress drained out.
[00:46:18 - 00:46:24] All you need is that next stress and to know what your engineering stress area is.
[00:46:24 - 00:46:27] So that's why they've got their effectiveness and their width.
[00:46:27 - 00:46:28] Cool.
[00:46:28 - 00:46:31] So here we see an example of one from previous years.
[00:46:31 - 00:46:34] A dog bone made from albuminium.
[00:46:34 - 00:46:40] And you'll see that there is a hole at the end because that's what the load attachment is for the homeschooling summer.
[00:46:40 - 00:46:47] So you want to make sure that this reduced section here is smaller in area in the area either side of the hole.
[00:46:47 - 00:46:50] Otherwise it's just going to break here.
[00:46:50 - 00:46:53] Normally what Oscar has done has recommended that for material testing.
[00:46:53 - 00:46:55] You would follow this standard here.
[00:46:55 - 00:46:59] However, we're not actually able to do this due to the thickness of our strips.
[00:46:59 - 00:47:04] So I think the thickness of the end where the puns are needs to be like 50 mil.
[00:47:04 - 00:47:08] Obviously if you've only got 20 mil in your strips, it's a little bit hard to make that 50 mil.
[00:47:08 - 00:47:10] So you'll have to kind of do a DIY thing.
[00:47:10 - 00:47:16] But as long as you're recording your data and you know the stress area, then you can work out the stress and work out your stress strain curve.
[00:47:16 - 00:47:19] And you're un-smodulus from that.
[00:47:19 - 00:47:25] So that's what we just talked about and making sure that the grip is kind of on.
[00:47:25 - 00:47:27] You'll use the extensometer.
[00:47:27 - 00:47:29] Do you know why you've used the extensometer?
[00:47:29 - 00:47:35] To measure the extension, which will then let you know what the slope of that curve is.
[00:47:35 - 00:47:38] So I've got those two videos on learn.
[00:47:38 - 00:47:42] And then if you have the extensometer, you'll get something that looks like this.
[00:47:42 - 00:47:47] Roughly speaking and the slope of this linear region would be your young-smodulus here.
[00:47:47 - 00:47:54] This put up here would be your UTS and your yield point is when it starts kind of test-edly deforming,
[00:47:54 - 00:47:55] which sometimes can be a little bit.
[00:47:55 - 00:48:04] Well if you've got the stress strain curve, you can actually work that out based on the percentage of plastic deformation or the strain that you've kind of got.
[00:48:04 - 00:48:06] Cool.
[00:48:06 - 00:48:09] So a normal design practice we would only really design to our yield.
[00:48:09 - 00:48:15] We've got a bit of a funky going on here, but we want to design it to failure, which I normally usually don't want their things to fail.
[00:48:15 - 00:48:18] So we'll be discussing that a little bit more.
[00:48:18 - 00:48:30] And there's more to come I suppose on in terms of our stress concentrations and what happens for stress concentrations for brittle materials versus ductile materials.
[00:48:30 - 00:48:33] But that's a conversation for Friday or next week.
[00:48:33 - 00:48:35] We've got some more examples of previous designs here.
[00:48:35 - 00:48:40] And we quickly have done so well, have about a minute and a half, they can use to write this list.
[00:48:40 - 00:48:42] So what do people have for their list?
[00:48:42 - 00:48:45] I might not have time to write it down in detail.
[00:48:45 - 00:48:47] Or as one of the first things that we had.
[00:48:47 - 00:48:53] So this is where you guys go to talk, you know.
[00:48:53 - 00:48:56] I'm writing things that I can only write a certain sort of speed.
[00:48:56 - 00:48:59] But someone said that you need to find a partner.
[00:48:59 - 00:49:00] Cool.
[00:49:00 - 00:49:02] Cool.
[00:49:02 - 00:49:03] Click.
[00:49:03 - 00:49:04] Click.
[00:49:04 - 00:49:05] There you are.
[00:49:05 - 00:49:06] Yeah.
[00:49:06 - 00:49:07] Maybe read.
[00:49:07 - 00:49:08] Read.
[00:49:08 - 00:49:11] So I'm like a list person.
[00:49:11 - 00:49:14] So I actually would be a kind of text box kind of guy.
[00:49:14 - 00:49:17] But this would be that you can kind of get things going as you go.
[00:49:17 - 00:49:19] What else would you need to do?
[00:49:19 - 00:49:20] Work.
[00:49:20 - 00:49:21] Yeah, assign.
[00:49:21 - 00:49:26] Yeah, that's good.
[00:49:26 - 00:49:31] And things are actual tasks for your structure.
[00:49:31 - 00:49:37] So yeah, you need a sketch design.
[00:49:37 - 00:49:42] What do you need to do with that as well?
[00:49:42 - 00:49:43] Calculations.
[00:49:43 - 00:49:44] Cool.
[00:49:44 - 00:49:45] Because we should on time.
[00:49:45 - 00:49:47] I'm going to leave this like with a massive star here.
[00:49:47 - 00:49:49] And we can talk about that on Friday.
[00:49:49 - 00:49:51] What else do you need to do to do your calculations?
[00:49:51 - 00:49:52] Is there any data you might need?
[00:49:52 - 00:49:53] Material testing.
[00:49:53 - 00:49:55] Material testing, right?
[00:49:55 - 00:50:01] And I'm also just going to write report and drawings, right?
[00:50:01 - 00:50:03] Yeah.
[00:50:03 - 00:50:05] So for now, that's a really short list.
[00:50:05 - 00:50:08] But what you'll see just before we pack up.
[00:50:08 - 00:50:17] If you go to this here, I've got some statistics.
[00:50:17 - 00:50:20] It's already.
[00:50:20 - 00:50:21] Yeah?
[00:50:21 - 00:50:28] Thank you, everyone.
[00:51:21 - 00:51:28] I'm impressed at that host.
[00:51:28 - 00:51:29] Yeah.
[00:51:29 - 00:51:38] I was thinking something like that.
[00:51:38 - 00:51:42] I see a channel.
[00:51:42 - 00:51:47] Hi, I think that's some stronger and lighter.
[00:51:47 - 00:51:51] I see a lot of people that are doing that.
[00:51:51 - 00:51:53] I say, what's good at doing that?
[00:51:53 - 00:51:54] Yeah.
[00:51:54 - 00:52:02] I'm just going to add a little bit of a pretty cute channel.
[00:52:02 - 00:52:08] I don't know why you choose the answer.
[00:52:08 - 00:52:11] I've seen this.
[00:52:11 - 00:52:12] Oh, yes.
[00:52:12 - 00:52:17] Let me see.
[00:52:17 - 00:52:20] I'm just going to say this one.
[00:52:20 - 00:52:24] I'm just going to say this one.
[00:52:24 - 00:52:26] Yeah.
[00:53:26 - 00:53:33] I'm just going to go to the other side.
[00:53:33 - 00:53:40] I'm just going to go to the other side.
[00:53:40 - 00:53:47] Yeah.
[00:53:47 - 00:53:48] Yeah.
[00:53:48 - 00:53:55] Yeah.
[00:53:55 - 00:54:02] Yeah.
[00:54:02 - 00:54:09] Yeah.
[00:54:09 - 00:54:16] Yeah.
[00:54:16 - 00:54:23] Yeah.
[00:54:23 - 00:54:30] Yeah.
[00:54:30 - 00:54:37] Yeah.
[00:54:37 - 00:54:44] Yeah.
[00:54:44 - 00:54:51] Yeah.
[00:54:51 - 00:54:58] Yeah.
[00:54:58 - 00:55:05] Yeah.

# ENMT301-26W Lecture 20 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_20_audio_16k_mono_32k.mp3`
Source audio SHA-256: `22e2448e5a454ce111db98ba63d693013fcfdd1d085a04aa2468e7e27eb803f8`
Generated: 2026-06-06T05:43:21.374046+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:03 - 00:00:26] Alright, thanks everyone. We'll make a start there if that's all good. Alright, thanks everyone. We'll make a start there if that's all right
[00:00:43 - 00:00:45] The old new trick
[00:00:45 - 00:00:47] I think that that should be working now yep
[00:00:48 - 00:00:52] All jeez if you're watching this live and just got your ears blasted or in the future
[00:00:53 - 00:00:55] Obviously this is recorded so you know shadow
[00:00:55 - 00:01:03] Yeah, I mean it will still pick it up with a smorgest like whether people want me like
[00:01:04 - 00:01:10] Breathing into it or not the night I appreciate making sure that you guys can hear you can see a lot bit of me cool
[00:01:10 - 00:01:16] Alright, so just be consistent with other tutorials before I get into this banger of the tutorial
[00:01:16 - 00:01:18] There's just a couple slides that I want to
[00:01:19 - 00:01:23] Make sure we got technical from this morning's lecture so
[00:01:23 - 00:01:29] What we ended up getting to or the one thing that we didn't touch is kind of stress concentrations on shafts
[00:01:29 - 00:01:34] And then how you might kind of avoid or reduce such stress concentrations on shafts
[00:01:34 - 00:01:38] So obviously in terms of when you have a bearing and you're using it
[00:01:39 - 00:01:47] In a way to basically exhale, restrain your shaft then you're going to utilize the faces of the bearing against the shoulders of your shaft
[00:01:47 - 00:01:54] So there's gonna be some kind of compressive force possibly going through those faces or that's gonna be where the fonts
[00:01:54 - 00:02:00] There's transmitted throughout the hearing right there and sort of probably can agree that for this one here
[00:02:00 - 00:02:04] If we push from the left to right the forces are gonna go through this face here
[00:02:04 - 00:02:07] Then it's gonna go through our rolling element back into this
[00:02:08 - 00:02:12] part of the housing and then ideally there's some sort of fastener that will
[00:02:12 - 00:02:17] Transmit the force to the rest of the housing and if we push on our shaft the other way
[00:02:17 - 00:02:21] in this case is gonna be going through the face between our lock nuts and
[00:02:21 - 00:02:25] face about bearing again through our bearing into our
[00:02:27 - 00:02:29] Circle up and into our housing, right?
[00:02:29 - 00:02:34] So to make sure that we utilize or make the most of our faces on our bearing
[00:02:34 - 00:02:38] We want to make sure that that load is basically evenly
[00:02:39 - 00:02:41] distributed around the face, right?
[00:02:41 - 00:02:42] So
[00:02:42 - 00:02:47] Sort of trivial, but you know you wouldn't want to just have only part of the shaft in contact with the bearing
[00:02:47 - 00:02:51] I want to keep it going all the way around and it's sort of like you'd almost have to go out of your way
[00:02:52 - 00:02:56] Sometimes to do that especially if some shaftness being turned right?
[00:02:56 - 00:03:02] So with that obviously you will have a radius on the corner of your bearing
[00:03:03 - 00:03:08] This one down here or this one up here and these are defined in the bearing catalog, right?
[00:03:08 - 00:03:14] And so that radius is gonna dictate what kind of radius your shaft can have
[00:03:15 - 00:03:18] With a little asterisks in there, right? Because there are ways kind of get around it
[00:03:18 - 00:03:23] But basically what I'm trying to say is that on the edge of your bearing you might have quite a sharp
[00:03:24 - 00:03:31] Radius if you make the radius the exact same on your shaft then that may cause a large stress concentration, right?
[00:03:32 - 00:03:34] Yeah, so if it's
[00:03:34 - 00:03:36] Yeah, cool, so you can see here
[00:03:36 - 00:03:41] An alternative to kind of have a bigger radius could be to use an undercut
[00:03:41 - 00:03:46] We see that there's a cross-section kind of showing what possible dimensions there are there
[00:03:46 - 00:03:52] So basically this undercut is allowing you to have a bigger radius and thus a blunter stress concentration
[00:03:54 - 00:03:57] There are other ways that you can minimize this
[00:03:58 - 00:04:05] Stress concentration and radius and we can see just for the sake of time and completeness here are three options
[00:04:05 - 00:04:13] So you may also use an undercut over on the face that it's actually on you may use some sort of stress
[00:04:14 - 00:04:19] relieving groove or you may use an undercut similar to the one that we saw on the previous slides, right?
[00:04:19 - 00:04:23] And so in all these cases what it's trying to do is
[00:04:24 - 00:04:32] Increase the apparent radius that's on your shoulder as seen by the force lines with the lines of force or flow forces
[00:04:33 - 00:04:34] through your shaft
[00:04:34 - 00:04:42] Cool, so yeah, it's super. We're talking about lubrication and then just for completeness
[00:04:43 - 00:04:47] Put that in there in case we had time and wanted to talk about it more
[00:04:47 - 00:04:51] But we'll come to kind of limit and that's a little bit more cool
[00:04:52 - 00:04:56] So with that we're into our tutorial enough
[00:04:57 - 00:05:02] Started with this fucker toky kawaii matsu fiki memati udou do lower
[00:05:02 - 00:05:08] Do not die like the octopus die like the hammerhead sharp so at this point in the term
[00:05:08 - 00:05:12] I know most of probably everyone that's in here has actually started the assignment
[00:05:12 - 00:05:14] But this one has probably
[00:05:14 - 00:05:18] Going out to those who maybe have done less than they had wanted to and it's saying
[00:05:19 - 00:05:24] What's me saying to you be strong fight for don't die like an octopus which apparently?
[00:05:24 - 00:05:28] I know I've never fought an octopus an octopus or court not for this apparently
[00:05:29 - 00:05:32] Apparently they don't fight as hard as a heavy-head sharp so
[00:05:33 - 00:05:37] All I'm trying to say is you know it's not too late to do a good job in the assignment
[00:05:37 - 00:05:41] do again if you haven't already and
[00:05:41 - 00:05:43] Yeah
[00:05:43 - 00:05:49] Cool, so obviously our home brought aluminium strips today. We can if you need them you can click them from the Nick admin team
[00:05:50 - 00:05:52] Please make sure to read some and
[00:05:53 - 00:05:54] Q&A's before emailing questions
[00:05:54 - 00:06:00] It has been a few kind of similar ones getting sent through which has caused me to then kind of go like oh cool
[00:06:00 - 00:06:02] This is similar to this question copy paste for me
[00:06:03 - 00:06:08] But obviously some of the questions. I think will be better asked than answered in this tutorial. So if you've got questions
[00:06:09 - 00:06:11] Make sure
[00:06:11 - 00:06:12] Ask them
[00:06:12 - 00:06:16] Cool, so what we're gonna cover in this tutorial real quickly is
[00:06:16 - 00:06:21] Reek heck of what the assignment deliverables are and what you're gonna be handing in on the 20th
[00:06:21 - 00:06:25] We'll go over what's happening with the teammate ratings and how those work
[00:06:26 - 00:06:32] Then there'll be open global questions for the class saying you're burning questions that you have that I can answer there
[00:06:32 - 00:06:34] We'll be ideally common between people
[00:06:35 - 00:06:36] and
[00:06:36 - 00:06:44] Then we'll go over an updated review of what we looked at last week in terms of the testing results that you guys have submitted
[00:06:44 - 00:06:47] Right the couple little design discussions to have
[00:06:48 - 00:06:53] That related to questions people have asked in the drop-in sessions and then depending on how long it takes
[00:06:53 - 00:06:58] I'll be able to kind of wander around and answer more nuanced questions if they exist
[00:06:59 - 00:07:05] Cool so from the summit brief you can see that on the I believe it's the 20th of March
[00:07:07 - 00:07:09] But check on Lynn don't quite me right now
[00:07:10 - 00:07:14] Whatever the due date is someone got up look it up
[00:07:14 - 00:07:15] I
[00:07:15 - 00:07:17] See the right date the wrong date
[00:07:18 - 00:07:20] There's the right yeah, okay
[00:07:21 - 00:07:24] So we got obviously 20th of the third at 9 a.m
[00:07:25 - 00:07:32] Cool so on slash before that date is two things that you need to do one is an electronic submission of everything
[00:07:32 - 00:07:37] So that we can mark it right so that electronic submission is like a PDF drop-offs
[00:07:37 - 00:07:41] Only one person your team needs to do this. You kind of your submissions are linked
[00:07:41 - 00:07:46] That you have to make sure that you've clicked there you're part of the same team on a teammate selection tool, right?
[00:07:47 - 00:07:54] And then we also require a physical submission of your printed in a3 drawings and the modes of failure sheet
[00:07:55 - 00:08:00] Cool so that's so that we have your exact drawings that you have submitted for the test day
[00:08:00 - 00:08:04] So we can actually you've made it to the specification that you've outlined
[00:08:05 - 00:08:11] Cool, yep
[00:08:11 - 00:08:16] It's up to you. Yeah. I mean the modes of failure sheet the question was do we have to do for that to them?
[00:08:16 - 00:08:20] I'd hear is that if you have that staple to your drawings that are submitted
[00:08:20 - 00:08:24] Then it's there for you on the test day if you were to forget. Yeah
[00:08:25 - 00:08:30] Yeah, so you'll you'll recollect these drawings and these will be what you talk through with the technicians
[00:08:30 - 00:08:33] It's just trying to save me possibly losing
[00:08:34 - 00:08:38] You're drawing or trying to print it out and then you know that on the drawing and then comes at you that for me
[00:08:38 - 00:08:42] So if you submit it in the drop box that means that you have to have filled out one of those blue slips
[00:08:42 - 00:08:47] And then your name is definitely on it and then we can kind of order. I'll have all the drawings perfectly ordered as to as
[00:08:48 - 00:08:53] per the test day order which will be determined by the Nick admin team based on new guys calendars
[00:08:54 - 00:08:58] I'm in a week a so that's still to be determined but the idea is that five all the physical drawings
[00:08:58 - 00:09:02] And I can get them ordered and on a test day out like smooth operating kind of thing
[00:09:02 - 00:09:05] Cool
[00:09:05 - 00:09:09] So for some people this might still be unclear and for that reason
[00:09:10 - 00:09:14] Draw a little diagram. So hopefully over emphasize or make it crystal clear
[00:09:15 - 00:09:18] What should be submitted and what kind of order?
[00:09:19 - 00:09:21] Cool so
[00:09:23 - 00:09:26] Focus the way that I think about it is
[00:09:27 - 00:09:30] It's nice of us in this order and you're annotated
[00:09:31 - 00:09:34] Well when you upload things to learn you can just upload multiple PDFs, right?
[00:09:34 - 00:09:36] So ideally you do it in this order
[00:09:37 - 00:09:41] Just to make it easier for the marker that as long as everything's there
[00:09:41 - 00:09:46] The end of the day doesn't really matter. So the first thing that you want is your cover sheet, right?
[00:09:49 - 00:09:52] And then the next thing I would put in there is your report
[00:09:54 - 00:09:59] So based on the assignment handout. What is the details that we need to know about the report?
[00:09:59 - 00:10:02] Is there a limit to the page or the words?
[00:10:04 - 00:10:06] Someone's nodding
[00:10:06 - 00:10:13] This is the one we're like it's more for me to feel better that you guys definitely know
[00:10:14 - 00:10:16] rather than
[00:10:16 - 00:10:20] Me actually wanting to know right because the last thing that I want as students to sort of say to me
[00:10:20 - 00:10:23] Oh, George was unclear. I didn't realize that there was a 800 word limit
[00:10:23 - 00:10:28] But if I say I remember we talked about that in tutorials six and you guys told me then I'm like
[00:10:28 - 00:10:34] I know that's at least someone does so if someone just repeats that is there is there a page or a word limit
[00:10:35 - 00:10:37] Yep, and what is it?
[00:10:37 - 00:10:40] 800 word, right? So 800 words
[00:10:40 - 00:10:44] And this is basically the body text, right?
[00:10:45 - 00:10:50] So it's quite concise and the means that you're going to have to be quite efficient with what you say, right?
[00:10:51 - 00:10:57] So in terms of that then I start giving questions of what are the specific things that you want to see in the report and so
[00:10:59 - 00:11:02] The details of the report we've talked about in terms of the assignment
[00:11:02 - 00:11:06] Mark sheet, right? So I think we want to know something along the lines of an introduction
[00:11:07 - 00:11:14] How you arrive at your design? What process you used something about the testing, right? And then it's all about your final
[00:11:14 - 00:11:18] Structure and your modes of failure and loads, right?
[00:11:19 - 00:11:21] Yep, so we see some nods
[00:11:22 - 00:11:24] Hopefully this is all just like
[00:11:24 - 00:11:26] super clear
[00:11:26 - 00:11:28] If we see here we got a assignment one
[00:11:29 - 00:11:34] Structure and we look these are cover sheet. If we look at this mark sheet here one a
[00:11:34 - 00:11:35] We can see that
[00:11:35 - 00:11:38] Introduction and design development testing
[00:11:39 - 00:11:44] Testing and results or testing and result testing or super results and then we've got description of fun design
[00:11:44 - 00:11:49] Predicted modes of failure and loads. So these things here are what we're marking your report on
[00:11:51 - 00:11:55] Cool so similar to my vibe of the last question that I asked you where it was like
[00:11:56 - 00:12:00] I know the answer, but it's better for me if I hear it coming from you when you're talking about
[00:12:01 - 00:12:02] your
[00:12:02 - 00:12:07] Final design if you were marking it. Do you think you would want to see a figure of your final design?
[00:12:09 - 00:12:10] Yes, right?
[00:12:10 - 00:12:17] So that could be a very good thing to include and it will also help you to really clearly communicate to the marker
[00:12:17 - 00:12:21] What the shape of your fingers rather than having to write a descriptive paragraph
[00:12:22 - 00:12:27] Yeah, so figures are really useful and you could annotate these figures as well to make them even more clear
[00:12:28 - 00:12:35] Similarly on Monday someone asked about testing. Do we have to show testing results? Do we have to show a figure of our
[00:12:36 - 00:12:42] Dog bone do we have to show a stress-strain plot and for these ones any time that I have a question that says have to it's like
[00:12:43 - 00:12:46] You don't have to do anything you could submit nothing in fail. Yeah
[00:12:47 - 00:12:52] But it probably sounds like if you were marking it if you were thinking about if you were reading someone else's report
[00:12:53 - 00:12:56] It's almost like a teaser for like yeah, I did some testing
[00:12:56 - 00:12:58] But I'm not gonna tell you about it
[00:12:58 - 00:13:03] Yeah, so I would say that you want to at least show some clear results
[00:13:03 - 00:13:07] This could be like a table. I think in one of the early entry tutorials
[00:13:07 - 00:13:10] We showed an example one of the table
[00:13:10 - 00:13:12] You could if you have more detail
[00:13:13 - 00:13:19] Attaching a tendency if there's more that's what happened or you wanted to show one of the stress-strain girls and you didn't have space
[00:13:20 - 00:13:23] Because it's a page from it
[00:13:23 - 00:13:26] That's fine. That's no page. Oh, sorry because it's a word limit is no
[00:13:27 - 00:13:34] No loss for adding that figure that shows is the testing sit up or here's what the dog bone look like or the fail dog bone
[00:13:34 - 00:13:36] Yeah
[00:13:36 - 00:13:39] Do you have to do anything? No, I don't have to do anything
[00:13:41 - 00:13:45] Cool all right, so if I go back any questions on the report side of things
[00:14:14 - 00:14:18] So is there any questions about anything in the mark sheet
[00:14:19 - 00:14:24] Here in terms of what we're looking like so in terms of your predictive loads and directed modes
[00:14:24 - 00:14:26] I think we've talked about that in the past
[00:14:27 - 00:14:30] But what it's saying here is we want to know that it's in the report
[00:14:38 - 00:14:40] I'm not sure what the vivas here like people are like
[00:14:41 - 00:14:42] Oh my go into slow
[00:14:42 - 00:14:46] You don't want to go over this and that's fine. We can move through it or if it's helpful
[00:14:47 - 00:14:50] If you're engaged in them gives me some confidence in front of you rather than being like I crap
[00:14:50 - 00:14:53] They already know this and I'm just like yettering. Yeah
[00:14:54 - 00:14:56] So what I'm trying to say is again
[00:14:56 - 00:15:01] If you were talking about your predicted failure loads and predictive failure modes
[00:15:01 - 00:15:07] What would be a very effective space and word wise way to present this information?
[00:15:09 - 00:15:12] Not equations. So this is like saying this is my failure load
[00:15:13 - 00:15:20] It's gonna break at 25 kg at a stress concentration. The second motor failure might be buffering in an x direction
[00:15:20 - 00:15:28] And that's gonna happen at 35 kg and the third motor failure might be the bearing stress and that's gonna happen at 72 kgs of applied load
[00:15:30 - 00:15:32] A table with a really good way
[00:15:33 - 00:15:37] To communicate all that information in a really concise way and similarly
[00:15:37 - 00:15:44] You can see that you could provide in the table or the failure loaders i.e. When this win each mode might occur
[00:15:44 - 00:15:47] And then is there any questions about this predicted failure range
[00:15:50 - 00:15:53] We're talking about this one in the past. How might we for our
[00:15:53 - 00:15:58] Number one failure mode. How might we estimate our predicted failure range
[00:16:06 - 00:16:11] Again, it was like talking about every channel. It's like oh my goodness. I cannot hear anything that's happening
[00:16:11 - 00:16:15] So if one person just decides to sort of summarize what you're right now
[00:16:15 - 00:16:32] It's sort of been saying
[00:16:32 - 00:16:37] Does everyone know the answer and you're like I don't want to say George. I want to ruin you. She's there afternoon
[00:16:54 - 00:16:57] Cool. Oh wow anyway onto the next thing
[00:16:58 - 00:17:01] I'm not asking for me. I know I know how to do it
[00:17:01 - 00:17:03] Is anyone want it written down
[00:17:04 - 00:17:06] You've got to tell me if you want it written down
[00:17:07 - 00:17:11] Yeah, so what would it be? How do we work at our failure range?
[00:17:14 - 00:17:16] Calculations and what are the calculations used?
[00:17:19 - 00:17:23] Yeah, the minute max values from testing right so
[00:17:24 - 00:17:26] first mode of
[00:17:28 - 00:17:30] failure
[00:17:30 - 00:17:32] range is
[00:17:32 - 00:17:34] based or
[00:17:35 - 00:17:37] Sigma UTS
[00:17:38 - 00:17:39] max
[00:17:39 - 00:17:39] slash
[00:17:39 - 00:17:41] min
[00:17:41 - 00:17:47] Then testing right and then I'm going to say loads
[00:17:48 - 00:17:50] should
[00:17:50 - 00:17:52] All be
[00:17:52 - 00:17:55] applied
[00:17:55 - 00:17:57] slash total
[00:17:58 - 00:18:00] Mass right
[00:18:00 - 00:18:02] So you want to say
[00:18:02 - 00:18:04] This is the community candidate on the t-state. You know
[00:18:05 - 00:18:10] I think it's gonna break at 35 kg of this true concentration, right? It's not very useful if you say
[00:18:12 - 00:18:16] It's gonna break when the force in the member is 2000 units. It's like oh cool
[00:18:16 - 00:18:21] Just let me do some calculations and tell you what that actually means, right? So make it super clear
[00:18:22 - 00:18:29] Awesome going good. I don't think there's anything else I want to comment on that side of things
[00:18:30 - 00:18:32] Next what you can do it doesn't really matter the order
[00:18:33 - 00:18:41] But you could do your calculations yet. So these are
[00:18:42 - 00:18:44] and
[00:18:44 - 00:18:46] helps
[00:18:46 - 00:18:49] Cool so if each of the calculations were to make sure that there's
[00:18:50 - 00:18:53] Right. Well start from the start you made it on lots of calculations
[00:18:54 - 00:19:01] Yeah, you might have iterated some of them for this assignment in four industry. We only really care about your final
[00:19:01 - 00:19:06] Set of calculations. Yeah, so this is why we sort of say there's only eight pages
[00:19:06 - 00:19:12] That means that you do have to be quite kind of concise with how you order your calculations and how you present them, right?
[00:19:12 - 00:19:18] So we don't want to go like oh, you know, it started on Tuesday the third we did this free body diagram
[00:19:18 - 00:19:21] It said that this was the first and then we decided to change your mind and we did this other triangle
[00:19:22 - 00:19:24] Just like be very matter effect. This is
[00:19:25 - 00:19:27] The geometry that we've decided this is the loads of members
[00:19:28 - 00:19:31] Therefore these are the calculations that are done for each one, right?
[00:19:34 - 00:19:36] So you can see here that I've drawn two boxes
[00:19:37 - 00:19:45] The reason I've got two boxes that should make it really clear that the report is not somehow like joined in holding hands with the calculations, right?
[00:19:46 - 00:19:50] So the calculation set will be eight pages
[00:19:50 - 00:19:52] with clear
[00:19:52 - 00:19:54] headings and as we've talked about it can be
[00:19:54 - 00:19:55] on
[00:19:55 - 00:19:59] done on a like a tablet handwritten or a can be on a bit of paper
[00:20:00 - 00:20:02] But what I don't want to some like hybrid
[00:20:02 - 00:20:06] Report calculations set up and you type out all your calculations on word, right?
[00:20:07 - 00:20:14] Cool question
[00:20:14 - 00:20:18] Yep, so you can risk the question was can we reference our calculations in the report?
[00:20:18 - 00:20:20] Yes, and they were being encouraged, right?
[00:20:20 - 00:20:25] So if you can say, you know, the failure load was determined to be to occur at when I load of 35
[00:20:26 - 00:20:31] Kg was applied. This is a show on this is detailed in the calculations. Yeah, and so
[00:20:33 - 00:20:35] What I'll just
[00:20:35 - 00:20:39] Try and make clear is there this one here is eight pages, right?
[00:20:40 - 00:20:42] And like
[00:20:42 - 00:20:47] Just I'll just refer to it as the calculation set or something. I wouldn't refer to it as like
[00:20:48 - 00:20:52] And a pindex just because this often opens a door that's hard to close, right?
[00:20:53 - 00:20:55] So I call that report
[00:20:55 - 00:21:00] calculation set drawings and then when we get to it, there may be additional
[00:21:00 - 00:21:02] Appinterseals. Got a question over here now
[00:21:04 - 00:21:11] Well, yeah, so for the calculation set eight pages hand counts clear title
[00:21:12 - 00:21:14] slash sketch
[00:21:15 - 00:21:16] slash
[00:21:16 - 00:21:18] working
[00:21:18 - 00:21:20] slash comment, right?
[00:21:23 - 00:21:25] Should be crystal clear something that reads it. I saw you didn't want
[00:21:26 - 00:21:30] Then we've got our drawings, right? So we review drawings a couple Fridays ago
[00:21:31 - 00:21:33] Feels like a lifetime ago
[00:21:34 - 00:21:36] And I think what's a good number of drawings
[00:21:40 - 00:21:42] Someone guess no
[00:21:42 - 00:21:45] Four is on the upper end of the argument yet and what would be the lowering
[00:21:46 - 00:21:47] Two to four. Yeah
[00:21:47 - 00:21:50] depends on how many members you have depends on
[00:21:51 - 00:21:56] How much information you want to show that generally what I would say is good is
[00:21:56 - 00:22:00] one times general assembly and then two to three
[00:22:01 - 00:22:02] Mender
[00:22:03 - 00:22:12] Yeah, so your general assembly drawing should just kind of show each of the parts. I know we kind of critiqued
[00:22:12 - 00:22:14] Some past examples, right?
[00:22:15 - 00:22:17] Probably find one of them
[00:22:20 - 00:22:24] This is your idea. So this was the gym. We'll see me that it sort of didn't like it that much
[00:22:25 - 00:22:26] That's right
[00:22:26 - 00:22:28] So this one here is a general assembly drawing
[00:22:28 - 00:22:32] You can see that there was something wrong with the part number because it wasn't even a part number. So
[00:22:33 - 00:22:38] What does that mean? So we said that that should be got frital. They've also chose a very odd
[00:22:38 - 00:22:44] Orientation to show the design and they've also exploded it which in my mind doesn't really make it clear
[00:22:45 - 00:22:51] You might want general assembly drawing that shows cool. This is an A B C or however you name them
[00:22:52 - 00:22:53] and then there'll be
[00:22:53 - 00:22:55] manufacturing drawing for each of your
[00:22:56 - 00:22:58] individual parts and
[00:22:58 - 00:23:00] It's okay to show
[00:23:01 - 00:23:06] Multiple pieces of aluminium being joined right. So for example, this one here is just a symbol
[00:23:06 - 00:23:12] Single member. So that's fine. There's no kind of joining method that's happened in this case here
[00:23:12 - 00:23:17] We see that the students drawn just one of the webs of the ibeam
[00:23:18 - 00:23:22] This is what I'm saying. I wouldn't recommend this because otherwise you're gonna have like 10 drawings
[00:23:23 - 00:23:29] Possibly, right? So I would just have one drawing with the ibeam and possibly have a note or something similar that says
[00:23:31 - 00:23:36] Individual members are assumed to be glued together or I'm rather than as shown on the drawing
[00:23:40 - 00:23:42] Cool any other drawing related questions. We can always
[00:23:43 - 00:23:48] Answer more if there's some of the burning questions or some things. If anyone done their drawing to it
[00:23:49 - 00:23:50] Nice
[00:23:50 - 00:23:57] Cool. Yeah, I reckon I wouldn't be surprised if people start submitting this week to be honest because like you've pretty much got everything that you need
[00:23:57 - 00:23:59] So it's just a measure of
[00:23:59 - 00:24:01] doing it wouldn't have happened
[00:24:01 - 00:24:05] Cool all right, well, let's finish off this little flow diagram
[00:24:06 - 00:24:08] So the next thing
[00:24:09 - 00:24:11] We see it was a pen to see is right
[00:24:13 - 00:24:14] I'm just gonna write this as other
[00:24:16 - 00:24:25] Appendices so this could be the AI declaration
[00:24:26 - 00:24:28] could be
[00:24:29 - 00:24:31] additional
[00:24:32 - 00:24:34] Working
[00:24:34 - 00:24:36] e.g
[00:24:36 - 00:24:38] Python or
[00:24:38 - 00:24:43] Cell right so I know that some people the very systematic and very efficient at the time
[00:24:43 - 00:24:52] They might have made some Excel document or Python to them like optimize for their buckling or optimize for their size of their shape of their
[00:24:52 - 00:24:54] Designer right do you want to do anything like that?
[00:24:55 - 00:24:59] Yep, so if you've done that and what you can do is at the end
[00:25:00 - 00:25:06] Say, you know when I was doing my design development and your report, you know when I was doing my design development to work out what the
[00:25:07 - 00:25:09] Most appropriate
[00:25:09 - 00:25:15] I value would be a spreadsheet was developed to aid with streamlining this process
[00:25:16 - 00:25:18] And then you would say this is included in the additional dependencies
[00:25:19 - 00:25:24] And then you would have that near new dependencies, right if you've done it I'd include if you haven't done it
[00:25:24 - 00:25:26] That's fine. It's not really an epinality, but there is
[00:25:27 - 00:25:29] You know, it's good to be clear of what you've done
[00:25:29 - 00:25:34] So that your report basically makes it really clear for someone else reading how you got to it, right?
[00:25:34 - 00:25:39] So especially if you like have used this to come up with a really creative design
[00:25:39 - 00:25:43] You want to make it just seem like yeah, we just came out with that. That's the first one we came up with right?
[00:25:44 - 00:25:46] It's sort of better can you get what your
[00:25:47 - 00:25:49] It process and you're thinking was behind that
[00:25:52 - 00:25:55] That's pretty much anything. Is any other questions you've got here?
[00:26:01 - 00:26:03] Cool. Well with that
[00:26:03 - 00:26:07] I jumped over here
[00:26:07 - 00:26:09] We'll see that we've done our flow diagram
[00:26:10 - 00:26:14] For team at ratings. This is pretty simple team to sing of assignment one and assignment two
[00:26:15 - 00:26:21] Will be adjusted based on the result of the team at ratings now for 98.5
[00:26:21 - 00:26:26] It's in a student. This makes no difference in your grade because you have a working relationship with your partner
[00:26:26 - 00:26:28] You're both put an equal kind of amount of work
[00:26:29 - 00:26:31] So makes no difference for some people
[00:26:32 - 00:26:37] Unfortunately this assignment ends up being a character building experience
[00:26:38 - 00:26:41] And this is the opportunity to outline
[00:26:42 - 00:26:44] Why that may not have been fair up
[00:26:45 - 00:26:47] Obviously if there are issues in your having issue with your partner
[00:26:47 - 00:26:51] I'd recommend that you email me before sooner rather than later
[00:26:51 - 00:26:53] But this is the kind of official
[00:26:54 - 00:26:57] Way that we consistently kind of adjust grades in a fair way
[00:26:57 - 00:26:59] Obviously it's only a very small percentage
[00:26:59 - 00:27:06] But this does mean that you will need to complete this peer assessment when it opens and complete it before it closes
[00:27:07 - 00:27:14] Yeah, so the way that it'll work is there'll be three questions. I can you write
[00:27:15 - 00:27:18] Each person's contribution on a scale of one to five
[00:27:19 - 00:27:21] Does anyone have to do these team mate rating things or peer reviews before?
[00:27:22 - 00:27:24] See some nods are you vaguely familiar with it?
[00:27:25 - 00:27:27] basically I'll make a reminder when it's
[00:27:27 - 00:27:31] Open and I'll make a reminder that day before it's closed and I won't piss to you other than that
[00:27:32 - 00:27:34] Yes, or something that I would make a note
[00:27:34 - 00:27:37] Maybe once once you submit your assignment I think it will be open
[00:27:37 - 00:27:41] And there'll be another one that's done in week 8 around the time of the test day
[00:27:42 - 00:27:45] Which relates to the manufacturing sort of side of your
[00:27:46 - 00:27:49] project, right?
[00:27:49 - 00:27:53] So we can see rate each person's contribution to the project in terms of time spent
[00:27:53 - 00:27:57] achieving material testing design calculations report care and drawings
[00:27:57 - 00:28:02] Rate each team members engagement of the project in relation to UC's organization of values
[00:28:02 - 00:28:06] Which are fucker for knowing the tongue of a market tongue and tearki tongue there
[00:28:06 - 00:28:09] And what it's doing with you and your group members active in providing constructive ideas
[00:28:09 - 00:28:14] Just in solutions and so for those who are unfamiliar with UC values
[00:28:15 - 00:28:21] We can see here is a brief summary of those here. So did they build
[00:28:23 - 00:28:26] Did they build kind of for knowing a tongue or did they build
[00:28:28 - 00:28:30] a positive working relationship
[00:28:30 - 00:28:35] Did you gear for each other in build the manner of each other?
[00:28:35 - 00:28:41] So a manaki tongueer and did you kind of take care of each other in terms of resources?
[00:28:41 - 00:28:43] Maybe our immune strips
[00:28:43 - 00:28:44] Net side of things, right?
[00:28:44 - 00:28:50] So just giving you some high or just highlighting or using this opportunity to highlight that these UC values are a thing and
[00:28:52 - 00:28:57] That they are kind of important in terms of the way that we work. We often don't explicitly
[00:28:58 - 00:29:02] Acknowledge them. We rather just do the right thing
[00:29:03 - 00:29:04] Cool
[00:29:04 - 00:29:11] Any questions with any of that. Cool. So with that
[00:29:12 - 00:29:15] What burning questions do you have generally about this? I'm an
[00:29:30 - 00:29:34] No question. It was like yo George you've done an amazing job so clear
[00:29:35 - 00:29:38] Or as they are George we don't know because we haven't done it yet
[00:29:40 - 00:29:50] Which is fine. We may become better. I hope you aren't like saving questions from whom I when I loit around because
[00:29:50 - 00:29:53] They know they'll be enough time. So I'll ask again
[00:29:53 - 00:29:55] What questions do you have? Does he don't have any?
[00:29:56 - 00:29:58] No silly questions, right?
[00:30:04 - 00:30:05] Yeah, there's a rule against that. Yeah
[00:30:07 - 00:30:11] Either way you think that yeah the question was can we laser cut out parts? The short answer is no
[00:30:13 - 00:30:15] We don't have enough laser cutters
[00:30:16 - 00:30:18] And it's not really fair
[00:30:19 - 00:30:23] Yeah, the other thing is though that unless you're the laser cut your dog bones
[00:30:24 - 00:30:26] Then you're not really sure if that
[00:30:26 - 00:30:31] Difference in the material each is going to play a role in promoting failure, right?
[00:30:32 - 00:30:38] So in terms of manufacture what we say is you can use the hand-operated machinery outlined in the first
[00:30:39 - 00:30:40] tutorial
[00:30:40 - 00:30:45] So there are things like drill presses that obviously are not like requiring you to like spin a drill yourself
[00:30:47 - 00:30:50] But yeah, do this as a class that's kind of the reason why
[00:30:51 - 00:30:53] Yeah
[00:30:53 - 00:31:01] Oh, yeah
[00:31:01 - 00:31:06] So the ideas that each of these things could be a separate PDF that you upload on the learn drop box
[00:31:07 - 00:31:12] Or if you want to you could do use some sort of compiling tool and like make it one thing right?
[00:31:12 - 00:31:14] But it's up to you please like
[00:31:14 - 00:31:18] Write on your phone or something like double check the use of them and everything right?
[00:31:18 - 00:31:23] Because I guarantee there'll be about five groups that don't submit the drawings online or they don't submit them in person and then
[00:31:24 - 00:31:28] After you like I'll see me it or show me you've done it, right?
[00:31:28 - 00:31:33] It was an instance last year where a very high performing student just forgot to submit their drawings
[00:31:33 - 00:31:35] They didn't realize until they grades are coming out. So
[00:31:36 - 00:31:40] Check check that the submission includes everything that you intend to submit because
[00:31:41 - 00:31:43] it is basically like
[00:31:43 - 00:31:46] On you and as an engineer you know, if you're like submitting for a job and you're like
[00:31:47 - 00:31:52] Oh, sorry, we forgot to attach the budget if you've missed the deadline then you've missed the deadline most of the time, right?
[00:31:52 - 00:31:54] So
[00:31:54 - 00:31:56] Cool is good other questions
[00:32:07 - 00:32:13] Yep. Yes, I feel you and my defaliar sometimes you might have weight reducing holes. That could be the second word of failure
[00:32:13 - 00:32:18] Right, so what I'm just gonna do as well. I'll just mention show it that on learn
[00:32:19 - 00:32:24] You'll see that under the assignment one tab. I've made a very beautifully formatted
[00:32:25 - 00:32:27] template
[00:32:27 - 00:32:30] Look at that which you can use to fill out, right?
[00:32:32 - 00:32:33] So
[00:32:33 - 00:32:37] Yeah, you can say first my family might be there. I don't know
[00:32:37 - 00:32:39] 25 millimeter hole
[00:32:39 - 00:32:42] Secret amount of failure might be there 23 millimeter hole
[00:32:42 - 00:32:46] Yeah, good metaphor. You might be buckling off the horizontal in the extension
[00:32:47 - 00:32:49] Yeah
[00:32:49 - 00:32:54] But this is more the edges of the almatista. You're not like oh, I can't remember it was incident. This speaks a ruffin down
[00:32:54 - 00:32:58] So I this is to help you and hopefully keep things being quick
[00:32:59 - 00:33:03] And all we really care about is like what is your failure load that you've designed for?
[00:33:04 - 00:33:17] So that's like the total applied load right so I mean the plus was it 1.19 kg for the hook and the load attachment cool
[00:33:18 - 00:33:28] Any other questions?
[00:33:28 - 00:33:29] movement
[00:33:29 - 00:33:30] so
[00:33:30 - 00:33:32] with this
[00:33:33 - 00:33:36] Done there. All right. We're doing the assignment
[00:33:36 - 00:33:39] So more people have submitted the material system results
[00:33:39 - 00:33:42] Obviously these slides are on learn as well, but for our yield stress
[00:33:42 - 00:33:47] We see people who are getting more likely between four and five
[00:33:47 - 00:33:49] Which is 120 to 140
[00:33:51 - 00:33:54] You'll see look at that so normally distributed
[00:33:55 - 00:33:57] between
[00:33:57 - 00:33:59] Five and six for our UTS
[00:33:59 - 00:34:01] So that's 140 to 160
[00:34:02 - 00:34:08] And for our young's modulus more commonly number three to number four are at
[00:34:10 - 00:34:12] So 60 to 70
[00:34:12 - 00:34:20] Cool so as we've kind of touched on in previous times if your material testing is on the outer bounds of what we see here
[00:34:20 - 00:34:23] It's up to you to decide what's one option that you guys could do
[00:34:25 - 00:34:30] You could reduce hopefully get better values and use those days and your results yet cool
[00:34:30 - 00:34:32] or see other option
[00:34:33 - 00:34:38] Good to complete obviously right you could do no more testing say if your young's modulus was low
[00:34:39 - 00:34:43] You know that it's low you make that comment and you know that that's on the conservative side
[00:34:43 - 00:34:50] If it's high or if it's low and you really want to change you could use the information presented here to update
[00:34:50 - 00:34:52] What you use in your calculations
[00:34:52 - 00:34:56] As the engineers you guys have to own whatever decision you make right
[00:34:56 - 00:35:00] If you change your your value and that ends up promoting failure
[00:35:01 - 00:35:05] That's the decision you have to own to make sure you're comfortable and confident
[00:35:05 - 00:35:08] If you do end up changing from what your test results are
[00:35:11 - 00:35:14] And you know the questions these ones
[00:35:18 - 00:35:24] Cool, so yeah, it was similar. I think similar question some of the amount about where two of the responses are two of the test results
[00:35:24 - 00:35:28] We're on the low side. The amount was on the high side. All right. What do I do?
[00:35:28 - 00:35:30] The answer was one of those three options
[00:35:31 - 00:35:40] Yeah, cool. Has anyone compared the results from the calculations with a physical test in regard to the stress concentration?
[00:35:42 - 00:35:44] Unperson how to go
[00:35:44 - 00:35:49] Bad right how many decisions you do though? Only one yeah, so
[00:35:50 - 00:35:52] a people sort of
[00:35:52 - 00:35:56] Familiar with what the approach could be for this member
[00:36:00 - 00:36:02] What people like nice wouldn't really get it
[00:36:02 - 00:36:04] Now I talked through it on
[00:36:04 - 00:36:07] The drop in the session a few of you asked those good questions
[00:36:08 - 00:36:17] They're useful to talk about it now. Yeah, couple nods. Cool. So what I will do to scaffold myself and be consistent as I recently answered
[00:36:18 - 00:36:20] frequently asked question
[00:36:21 - 00:36:25] They asked similar kind of thing right now. I just want to try and make it clear
[00:36:27 - 00:36:31] What the approach I would suggest is but there's not one right way to do this, right?
[00:36:32 - 00:36:34] Essentially we see someone see when I use the graph
[00:36:35 - 00:36:41] My my value for the stress concentration is off the graph. So what do I use?
[00:36:42 - 00:36:48] So the first answer to that question is it is okay to interpolate using a stress concentration plot
[00:36:48 - 00:36:50] Yeah, so
[00:36:50 - 00:36:53] Often sort of right there might be some ecentote. So if you're really fast at the right
[00:36:54 - 00:36:58] You'll be able to kind of make an approximation of what that K value might be or if you're faster to lift
[00:36:59 - 00:37:01] you could
[00:37:01 - 00:37:08] Interpolate but obviously it's getting really really high so maybe it might be a better idea to slightly change your geometry if that was okay, right?
[00:37:10 - 00:37:15] You're unhappy with that so far however are we going to use the K-day directly from the plot?
[00:37:17 - 00:37:20] No, we see people shaking the head right why not?
[00:37:23 - 00:37:25] What kind of material do we have?
[00:37:26 - 00:37:29] Duct-tial material what kind of materials is a
[00:37:30 - 00:37:32] Stressing above the
[00:37:32 - 00:37:34] UTS indicative of failure
[00:37:38 - 00:37:43] The bristle material, right? Which you imagine for was if we're giving you all glass and you think was made out of glass
[00:37:44 - 00:37:49] Then probably want to use that K-day there because as soon as one of the parts of that edge of the stress concentration gets above
[00:37:50 - 00:37:54] The UTS and it's going to be a crack and that's going to propagate pretty quickly and promote failure, right?
[00:37:55 - 00:37:57] But for duct-tial materials what happens?
[00:37:57 - 00:38:04] There are a bit tougher so they're going to have some stress redistribution around the stress concentration, right?
[00:38:05 - 00:38:07] So what we call this or the way that I kind of
[00:38:08 - 00:38:12] call the way that I describe this is that it's like blending the stress concentration, right?
[00:38:14 - 00:38:20] So that's what we've got one of my favorite lines where we see the apparent stress concentration factor
[00:38:21 - 00:38:29] maybe approximately 1.1. You're unhappy with where we've gone there.
[00:38:29 - 00:38:33] Now the reason that we say approximately 1.1 and why I can't just say,
[00:38:33 - 00:38:36] yep, use 1.1 and you'll be happy days is that the same
[00:38:37 - 00:38:42] Trenes that happen in terms of the sharpness of your stress concentration
[00:38:42 - 00:38:45] will still occur for your duct-tial materials, right?
[00:38:46 - 00:38:49] So on our stress concentration graph, I don't know if I've got one
[00:38:49 - 00:39:02] handy but what you'll see, what you'll see is that some of these stress concentration plots
[00:39:02 - 00:39:07] they may vary between say 1.4 to 3.
[00:39:08 - 00:39:14] Yeah, so if we look at this plot here in this case that goes approximately maybe you say
[00:39:14 - 00:39:19] k value of 2 is an asymptote and then we can see it goes up to 3, right?
[00:39:20 - 00:39:26] So similar kind of trend is possibly going to happen or would be acceptable to assume what happened
[00:39:26 - 00:39:32] in a duct-tial material but the range of these values on the left instead of being between 2 and 3
[00:39:32 - 00:39:48] might be between 1 and 1.25. Yeah, and so what I've said is that instead of just using 1.1 and going
[00:39:48 - 00:39:52] for gold, some people might do and I'll be okay that should hopefully get close enough to the range
[00:39:53 - 00:39:58] that you can use that value to size your hole and then you'll do some sort of experimental
[00:39:58 - 00:40:03] small scale test to verify your assumption about this apparent stress concentration.
[00:40:05 - 00:40:11] Yeah, so if you have a really sharp hole in a narrow member and your D over W is really small,
[00:40:11 - 00:40:16] maybe you're up here and that means that your k or your apparent stress concentration factor
[00:40:16 - 00:40:22] might be above 1.1 but if you're way over here, it might be a lot closer to what?
[00:40:25 - 00:40:32] So that's up to you guys' engineers to kind of do an experiment and to kind of validate for yourself,
[00:40:32 - 00:40:38] right? And so with that whatever assumption you make for designing that failure member make it really
[00:40:38 - 00:40:42] clear what your assumptions are. i.e. you will want to write something along the lines of, you know,
[00:40:42 - 00:40:47] I'm assuming that if the stress in the member is at the level of the ultimate tensile stress
[00:40:47 - 00:40:55] gain from testing when the failure load is applied, when I add a subsequent mass, I speak to my
[00:40:55 - 00:41:02] mere immersive fail. Cool. Now we've talked about this before but can you have an apparent stress
[00:41:02 - 00:41:09] concentration factor of less than 1? No, right? It'll be great if we could but basically what
[00:41:09 - 00:41:14] that's saying is like if you drill a hole in something you get stronger. It doesn't make any sense,
[00:41:14 - 00:41:19] and so the reason that that k value, if you did your calculation and it ends up coming out as a
[00:41:19 - 00:41:26] less than one, it probably downs to some experimental error in the way that you've made your dog bones
[00:41:26 - 00:41:31] or in the way that you've made your hole, right? So when you do your dog bones, how accurate did you
[00:41:31 - 00:41:39] measure the reduced section could be a question for think about, right? Because if there's a slight
[00:41:39 - 00:41:45] amount of, you know, if you're only doing it to a tenth of a millimeter, then that might be
[00:41:46 - 00:41:52] in on the size of your reduce session, there might enable a difference in what the actual
[00:41:52 - 00:42:02] area of your number is, right? So has that helped to clarify things rather than make them more
[00:42:02 - 00:42:14] confusing? Mainly not, so hopefully it's not for me clear enough not more confusing. Cool.
[00:42:14 - 00:42:20] So quickly before we finish, what I want to talk about or just show examples of, these things
[00:42:20 - 00:42:26] here. So if someone in the drop-in session can ask about how you go about calculating
[00:42:28 - 00:42:36] areas in your, the impact of introducing weight saving holes in your member
[00:42:36 - 00:42:41] and what kind of assumptions are okay, right? And so what we've sort of said is that if we have a
[00:42:41 - 00:42:49] hole in something like an eye beam, for example, this eye beam here, what we can assume or what
[00:42:49 - 00:42:55] I would recommend is that for the area where that hole is in your eye beam, if I draw it like this,
[00:42:55 - 00:43:02] you might be able to do a buckling calculation for this specific region of your design, right?
[00:43:03 - 00:43:07] Before that you might be assuming that the length is the diameter of the hole and that the cross
[00:43:07 - 00:43:14] section that you use, the kind of worst or the smallest cross-section that you see, right? So it might
[00:43:14 - 00:43:22] look like this, right? Cool. What I do want to show as a word of caution is that when you're doing that,
[00:43:23 - 00:43:29] you're assuming that this cross-section will remain the same, right? Which is a good assumption if you've
[00:43:29 - 00:43:35] just got a hole, right? So if I push on this member, it's not like super floppy and like acting as like
[00:43:35 - 00:43:42] two separate halves. Yeah, there's some nods to the nods of your encouraging for me. This one here
[00:43:44 - 00:43:50] possibly shows where an assumption was not necessarily appropriate, right? So they've kind of
[00:43:50 - 00:43:56] extrapolated this, done at the long way and decided that this here would be there out.
[00:43:57 - 00:44:03] Yeah? So what they have assumed is that cross-section is going to be consistent in terms of its
[00:44:03 - 00:44:08] eye value across that whole time, right? Now I kind of cracked myself up on Monday because actually
[00:44:08 - 00:44:14] it was like trying to show like, you know, are these things like holding the own,
[00:44:14 - 00:44:17] that they're going to stay in that shape and it literally is like bent in my hands because
[00:44:17 - 00:44:22] it's probably not good, right? So if I squeeze this, I'm going to see that there's nothing
[00:44:22 - 00:44:29] really stopping the cross-section from changing, yeah? So essentially what's actually happening
[00:44:29 - 00:44:34] is that this is like two individual nenders and you could assume that they've got half the load,
[00:44:34 - 00:44:38] but they might actually have more than half the load depending on if your holes are actually
[00:44:38 - 00:44:43] perfectly in line or not, right? So a word of course, if you do have a long extended nenders in the
[00:44:43 - 00:44:49] middle of your structure, or likewise if this was on the end of your structure, you may have
[00:44:50 - 00:44:56] a chip that you're happy with your assumptions. Yeah? Cool, designing the failure
[00:44:56 - 00:45:00] in the end. We've gone over that one there. The final thing is bearing versus tear out versus
[00:45:00 - 00:45:10] tinsile stress at the pin. That's, oh, this one here. So this one here shows an example of what kind
[00:45:10 - 00:45:17] of failure. So this is obviously where the pin would go, and then there was actually like a member
[00:45:17 - 00:45:24] going around like that. How's that one failed? Earring is a good cool good guess, but not quite.
[00:45:24 - 00:45:32] So if it was bearing, what we would see is like a deformed like a long hole. Yeah? If it was
[00:45:32 - 00:45:35] in compression and my look like that, if it was in tension, might have deformed that way.
[00:45:37 - 00:45:42] Yeah? So think about life. You had like Play-Doh, and then you like pull the pin and play-Doh,
[00:45:42 - 00:45:49] then it would like deformed, right? Cool. So who wants to come up next? Is it tear out or is it tinsile
[00:45:49 - 00:45:57] stress at the pin? Tinsile. Yeah, lock it in. So tinsile stress at the pin, that relates to the stress
[00:45:58 - 00:46:05] either side of the hole, right? So in this case here, what's happened is, yeah, the tinsile stress
[00:46:05 - 00:46:12] either side has been what has caused it to fail, right? The third thing that we talked about was tear
[00:46:13 - 00:46:22] and that would be if it tiered out and there was a cut slotted out that way, right? Cool. So those are,
[00:46:22 - 00:46:28] that's just showing the difference between those days there and we'll see where you could see in those
[00:46:29 - 00:46:36] stress concentration plots that we showed that there is four holes that are loaded with a pin.
[00:46:36 - 00:46:42] There are K values, again, because it's a ductile material, then you need to probably make an
[00:46:42 - 00:46:48] assumption about what this K value actually might be, but all that's trying to say is probably don't
[00:46:48 - 00:46:53] make the area either side of your hole too small and we've got a bunch of examples around
[00:46:53 - 00:47:00] that kind of show what has at least and dickatively worked in the past and what has not,
[00:47:00 - 00:47:05] right? So some of these obviously have two pieces of aluminium, definitely look at a bunch of tinsile
[00:47:05 - 00:47:31] in this and we will see that there. So any other questions, hopefully that's how to clarify things.
[00:47:31 - 00:47:39] What I've got here is some awards that I may or may not go out. So on Tuesday we'll have a range of
[00:47:39 - 00:47:47] types of designs and in the past these have been ones that I have allocated, but sometimes
[00:47:47 - 00:47:54] depending on how things go, they may or may not be some of these awards given out, right? But
[00:47:54 - 00:47:59] if you were trying to work out or wanting to be able to write on your CV, I was the overall winner
[00:47:59 - 00:48:05] of aluminium structure where I had the lightest member or I had the best drink for weight ratio,
[00:48:06 - 00:48:11] then these are things that I'll kind of be able to give out to you. There are three awards at
[00:48:11 - 00:48:18] the bottom here. So we've got an innovation award, if there's a design that I'm particularly
[00:48:18 - 00:48:25] impressed by, that doesn't use springs. We have the Michael Bay award for the most spectacular
[00:48:25 - 00:48:31] failure. So this is the, you know, the directed by Michael Bay kind of means sort of thing, you know,
[00:48:32 - 00:48:37] and then also for the heaviest structure where you'll have the civil engineering award.
[00:48:37 - 00:48:43] So with that, that's pretty much us for time. If you've got questions, I will be floating around.
[00:48:43 - 00:48:45] If you're afraid to look at these things otherwise I'll see you in the future.
[00:49:00 - 00:49:01] Yeah.
[00:49:01 - 00:49:05] That's in the, well, it doesn't matter.
[00:49:13 - 00:49:16] Yeah, that's just the moment of the area, the moment of your time.
[00:49:31 - 00:49:53] So we did go through
[00:50:01 - 00:50:09] to the
[00:51:01 - 00:51:03] You can do that.
[00:51:03 - 00:51:05] You can do that.
[00:51:05 - 00:51:08] I'm going to say that this is the one that you can do.
[00:51:08 - 00:51:09] Yeah.
[00:51:09 - 00:51:11] Yeah.
[00:51:11 - 00:51:18] If we just need to,
[00:51:18 - 00:51:20] what might happen if these are those ones?
[00:51:20 - 00:51:22] Do I think it's a little 20 or something?
[00:51:22 - 00:51:23] What is this?
[00:51:23 - 00:51:25] What does this have to do to do that?
[00:51:25 - 00:51:28] No, it's a little bit more interesting.
[00:51:28 - 00:51:29] Okay.
[00:51:29 - 00:51:32] I'm going to be the Toronto government.
[00:51:32 - 00:51:34] I'm going to be the Toronto government.
[00:51:34 - 00:51:37] I'm going to be the government.
[00:51:37 - 00:51:38] Yeah, well exactly.
[00:51:38 - 00:51:41] Well, you're still going to have to leave your phone.
[00:51:41 - 00:51:44] So, it would be somewhat yet.
[00:51:44 - 00:51:45] Yeah.
[00:51:45 - 00:51:46] So, I do as a...
[00:51:46 - 00:51:48] So, there's not any lockers.
[00:51:48 - 00:51:50] I'm going to make...
[00:51:50 - 00:51:52] Obviously, my name is Martin Luther.
[00:51:52 - 00:51:55] I realize that she needs to make this change.
[00:51:55 - 00:51:56] Yeah.
[00:51:56 - 00:51:59] So, all we want to do is...
[00:51:59 - 00:52:04] I'm going to be telling someone that this is a design change that this was made.
[00:52:04 - 00:52:05] I'm going to be writing this wrong.
[00:52:05 - 00:52:06] I'm going to write this wrong.
[00:52:06 - 00:52:07] I'm going to write this wrong.
[00:52:07 - 00:52:08] I'm going to write this wrong.
[00:52:08 - 00:52:09] I'm going to write this wrong.
[00:52:09 - 00:52:10] If you're ever going to make a change,
[00:52:10 - 00:52:11] it's also something that starts getting made.
[00:52:11 - 00:52:13] It has way better than being able to do.
[00:52:13 - 00:52:14] So, as soon as I just call it,
[00:52:14 - 00:52:16] the foundation now, it turns out that this is a drop.
[00:52:16 - 00:52:19] I think it's a few things you need to do.
[00:52:19 - 00:52:20] It would be similar.
[00:52:50 - 00:52:52] I'm guess.
[00:52:52 - 00:52:54] I just need to write it.
[00:52:54 - 00:52:56] If you would note,
[00:52:56 - 00:52:58] I'm going to choose...
[00:52:58 - 00:53:00] I'm going to write this wrong.
[00:53:00 - 00:53:02] So, this is...
[00:53:02 - 00:53:05] I'm going to write this wrong.
[00:53:05 - 00:53:07] As soon as you do,
[00:53:07 - 00:53:08] I'll say...
[00:53:08 - 00:53:10] I'm going to write this wrong.
[00:53:10 - 00:53:14] I'm going to write this wrong.
[00:53:14 - 00:53:17] I'm going to write this wrong.

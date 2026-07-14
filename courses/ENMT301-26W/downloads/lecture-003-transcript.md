# ENMT301-26W Lecture 03 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_03_audio_16k_mono_32k.mp3`
Source audio SHA-256: `bc76d70abfdefb48bcd873d1e1abb771b612a5c1a4ff9838f2ad60285045db89`
Generated: 2026-06-06T04:55:27.911648+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:36 - 00:01:05] So, just because there's a couple people walking in, I'll play that first one again.
[00:01:05 - 00:01:37] Just walking in, just walking in, waiting us.
[00:01:37 - 00:01:42] So, we have a pretty jam-packed, uh, electoral today.
[00:01:42 - 00:01:48] I'll try my best to do the exact same timing in jokes that I did in the previous electoral.
[00:01:48 - 00:01:54] But basically this will sit up quite well for our tutorial on Friday.
[00:01:54 - 00:02:00] We'll be able to get into some more examples, actually, of what we are of applying our design, kind of thinking,
[00:02:00 - 00:02:06] into this assignment and doing some example calculations and getting things started and that kind of respect.
[00:02:06 - 00:02:11] So, I'll do this on Friday.
[00:02:11 - 00:02:18] We can work out when the coffee drop-in session will be, which is sort of alluded to in the lecture.
[00:02:18 - 00:02:23] It's kind of a version of office hours that hopefully is less confronting where you can come to a common space.
[00:02:23 - 00:02:29] That's not my office on the fifth floor to ask any questions that you might have about the assignment.
[00:02:29 - 00:02:31] And those will be kind of going from next week.
[00:02:31 - 00:02:37] What I might do this year is actually make it time-tables for half an hour, but if people are asking more questions in half an hour,
[00:02:37 - 00:02:47] then we can go for the full hour, but otherwise I'll have time sometimes where either other things are happening or I've just done such a great job of explaining everything that no one's had any questions to come as soon about.
[00:02:47 - 00:02:51] And I've just been sitting in the EPS library by myself drinking coffee.
[00:02:51 - 00:02:57] So, we'll make some clear communication about that and I'll probably make a post on Learn.
[00:02:57 - 00:03:05] And then obviously this is one of the key kind of slides that we had in the lecture where, you know, I've been asking some good questions after the lecture.
[00:03:05 - 00:03:09] If you've got other questions, you can email me and make sure you keep it nice and formal.
[00:03:09 - 00:03:14] You can pop on the office and we'll sort out that coffee drop-in session.
[00:03:14 - 00:03:19] Yeah, but anything sort of a festival will basically definitely be posted on Learn.
[00:03:19 - 00:03:23] Sometimes I'll have discussions of things that are very sad of the lecture as a little update.
[00:03:23 - 00:03:28] So, you might be thinking this is a tutorial, why is George Lickering, what is going on here?
[00:03:28 - 00:03:31] Well, ensure that these tutorials are operated as a Licktorial.
[00:03:31 - 00:03:37] That's why I was split you in two and have an ice kind of flat room so that you can actually work at times as part of your group.
[00:03:37 - 00:03:41] So, part of the group being the group that people are sitting at your table.
[00:03:41 - 00:03:49] Some aspects may feel similar to a lecture, other aspects will be more interactive and they might be grouped at group activities and discussion.
[00:03:49 - 00:03:55] So, basically, I've designed this in this way because I think that that's what will be most valuable for you as students.
[00:03:55 - 00:04:01] The questions that I'm asking are questions that I would hope to be asking if I was a student in your position.
[00:04:01 - 00:04:04] I'm not asking you the questions for my own knowledge.
[00:04:04 - 00:04:08] I already kind of know the answers to the questions per se.
[00:04:08 - 00:04:18] But if you're able to answer them, that obviously means that you're doing a good job of keeping up to date with the content and following along with what we're trying to review in terms of how to do that.
[00:04:18 - 00:04:22] In terms of our engineering design process.
[00:04:22 - 00:04:32] Cool. So, with that, I will ask questions and ideally you guys can kind of engage in answer questions nice and easily.
[00:04:32 - 00:04:37] But sometimes I'll ask questions and I'll just get like crickets or silencer as the response.
[00:04:37 - 00:04:41] And that's really, really challenging for me because I've got these two traits.
[00:04:41 - 00:04:43] One of them is that I'm really patient.
[00:04:43 - 00:04:46] The other one is I'm terrible at reading minds.
[00:04:46 - 00:04:48] So, I might have explained something to ask you other questions.
[00:04:48 - 00:04:55] You guys might all be thinking like, far out, I wish this guy would stop talking about this thing that we already understand really well.
[00:04:55 - 00:04:57] But if you don't tell me that, I'll be thinking, holy here.
[00:04:57 - 00:05:02] If I've gone too detailed about this, I need to make it even simpler and go over it again.
[00:05:02 - 00:05:09] So, if you guys are things going too fast, or too slow, or you don't want to ask, well, answer a question, then just let me know that.
[00:05:09 - 00:05:10] And I keep it kind of going.
[00:05:10 - 00:05:14] As I say, the engagement is more so that I can understand where you guys are at.
[00:05:14 - 00:05:17] And actually, they were all kind of at the same kind of levels.
[00:05:17 - 00:05:22] So, I'm not talking about something that you haven't even considered yet because you haven't done the things sort of previous.
[00:05:22 - 00:05:27] So, instead of writing this down, we can just collectively as a group brain somewhat as three things.
[00:05:27 - 00:05:30] I've sort of spilled the beans and was, why don't you guys do that.
[00:05:30 - 00:05:35] What do you think might expectations for you might be in these tutorials?
[00:05:35 - 00:05:45] Don't all go along, so I can't hear you as a really tough one over this side somewhere.
[00:05:45 - 00:05:46] Questions?
[00:05:46 - 00:05:47] Well, sorry.
[00:05:47 - 00:05:48] Questions?
[00:05:48 - 00:05:51] Yeah, asking questions if you've got them, or answering questions when they're asked.
[00:05:51 - 00:05:52] Yeah.
[00:05:52 - 00:05:54] So, yeah, if the sign's not clear, just make it really clear to me.
[00:05:54 - 00:05:56] So, that's, oh, we can let us do things.
[00:05:56 - 00:05:57] Other things?
[00:05:57 - 00:05:59] See that, understanding?
[00:05:59 - 00:06:00] Yep.
[00:06:00 - 00:06:01] See that on understanding.
[00:06:01 - 00:06:06] So, definitely if you're like, I don't understand this, let me know, and I can go over it again.
[00:06:06 - 00:06:10] Or I can try and explain it in a different way that might make a little bit more sense.
[00:06:10 - 00:06:13] One other thing.
[00:06:13 - 00:06:23] So, sort of within, in terms of participation, then you do actually participate in that you kind of work in a positive and inclusive manner
[00:06:23 - 00:06:24] at your tables.
[00:06:24 - 00:06:27] Don't be kind of shooting down people's ideas if you're writing lists or similar.
[00:06:27 - 00:06:33] We can always critique what the perfect all might be later, but our idea is they will take kind of build on each other's ideas
[00:06:33 - 00:06:38] and not be super negative and put other people down.
[00:06:38 - 00:06:39] Cool.
[00:06:39 - 00:06:41] So, it's all right.
[00:06:41 - 00:06:42] Great stuff.
[00:06:42 - 00:06:50] So, today what we'll be focusing on is basically, while into this, you should have a pretty clear understanding of what this assignment is, what you're kind of required to do,
[00:06:50 - 00:06:57] and a lot of the little nuances that on Friday we can kind of get stuck into actually coming up with the design and going through that process.
[00:06:57 - 00:06:59] So, you can see we'll go over the assignment brief.
[00:06:59 - 00:07:03] The marking schedules will spin some time planning our tasks.
[00:07:03 - 00:07:07] We might build on that on Friday to start the electoral.
[00:07:07 - 00:07:15] We'll talk about how you do your material testing and there'll be opportunities for questions as well as showing you a bunch of what the past examples are.
[00:07:15 - 00:07:18] So, in two of the assignments brief, is anyone at all looking at it?
[00:07:18 - 00:07:19] Yep.
[00:07:19 - 00:07:21] The least two people, which is good three, yeah.
[00:07:21 - 00:07:22] It's sweet.
[00:07:22 - 00:07:25] So, definitely put that on you to do list.
[00:07:25 - 00:07:28] We'll find it and walk through it now.
[00:07:28 - 00:07:32] So, if you are on learn, this is what the page looks like.
[00:07:32 - 00:07:37] If you're on the homepage, all you want to do is go on the aluminium structures.
[00:07:37 - 00:07:41] And then up the top here what you'll see is if you click this link and download it,
[00:07:41 - 00:07:44] there will open this thing here.
[00:07:44 - 00:07:48] So, I've got in the slides some of the key information just re-highlighted.
[00:07:48 - 00:07:55] What I actually do is just talk through what I've got written here because this is meant to be basically the one source of the
[00:07:55 - 00:08:00] truth to make it clear what you actually need to do for the assignment.
[00:08:00 - 00:08:07] So, as we said in the lecture, you need to, well, the assignment is basically trying to get you to do what you need to do.
[00:08:07 - 00:08:14] In this case, that is designing a structure to carry a load, doing your own engineering calculations,
[00:08:14 - 00:08:20] working out some material properties from testing and then reporting what you've found both in terms of a calculations set,
[00:08:20 - 00:08:25] a design report and a set of drawings.
[00:08:25 - 00:08:34] The task is in peers to design, build and test a pin joint structure for the application shown in figure one.
[00:08:34 - 00:08:40] The structure must support a massive 20 kg and fail at a mass less than or equal to 39 kg.
[00:08:40 - 00:08:49] You're only allowed to use the material provided to you, namely 20 millimeter 1.2 thickness, aluminium strips.
[00:08:49 - 00:08:54] We have some steel pins for the connecting different menders inside the testing apparatus.
[00:08:54 - 00:09:13] And then you also to fabricate individual menders or use either have one or more menders made from using Araldart glue to part epoxy adhesive or at least one mender that is constructed using only pop rivets.
[00:09:13 - 00:09:18] So if I go on the document camera, we can see an example of each of those.
[00:09:18 - 00:09:22] So here we can see an I-beam that's being manufactured using glue.
[00:09:22 - 00:09:25] You can see the glue is absolutely everywhere.
[00:09:25 - 00:09:35] And then similarly, here's an example, or a couple of examples where individual menders have instead been manufactured using pop rivets.
[00:09:35 - 00:09:40] So if you've got a three-nimed structure, you get a choice.
[00:09:40 - 00:09:47] You can have two menders that use glue or two menders that use rivets or you might have one that just uses no joining material.
[00:09:47 - 00:09:50] That's fine. You might just have it just being a single piece.
[00:09:50 - 00:09:57] But if you do a two-nimed structure, unless you want to do one of each or have a two-nimed got.
[00:09:57 - 00:10:03] If one's not going to join to method or joining method, then only one is appropriate.
[00:10:03 - 00:10:06] Cool. Hopefully that's kind of clear.
[00:10:06 - 00:10:12] Cool. If you're unable to find a partner, please use the forum on Learn under the Assign One page.
[00:10:12 - 00:10:16] Or you can kind of just talk to people after class if we want to.
[00:10:16 - 00:10:21] We can kind of meet up like have an area if you're still looking for a partner.
[00:10:21 - 00:10:24] But obviously, it's only day two. So it's kind of early days.
[00:10:24 - 00:10:31] But what you'll see in here on this Assign One page, once you've found your partner, you'll click on this and you'll both select into the same team.
[00:10:31 - 00:10:35] Yeah. So there'll be kind of something that you do.
[00:10:35 - 00:10:40] And then if you're looking for a partner, you could make a puzzle in this forum if you were saying, hey, I'm looking for a partner.
[00:10:40 - 00:10:43] Email me on one of my UCE mailers.
[00:10:43 - 00:10:53] And then I'll ask is that you take down your puzzle once you have actually found a partner so that we kind of narrow down the number of people that are trying to email people in saying, oh, I've already got a pun.
[00:10:53 - 00:10:54] Christian.
[00:10:54 - 00:10:59] So in the video, were those two members in one type of connection?
[00:10:59 - 00:11:05] In the video, in the video, there was an Anken video. They only used glue.
[00:11:05 - 00:11:10] But we've kind of ordered them to 2026 and we're using rivets now.
[00:11:10 - 00:11:13] So pretty riveting stuff.
[00:11:13 - 00:11:15] Yeah.
[00:11:15 - 00:11:16] Yeah.
[00:11:16 - 00:11:21] Basically, as I'll sort of touch on it, sort of to do with making it easy to recycle.
[00:11:21 - 00:11:25] And I don't know if there's been any other instances.
[00:11:25 - 00:11:28] We actually have to work out that the rivets are kind of strong enough.
[00:11:28 - 00:11:36] A lot of times these joining techniques are kind of just used in a, what I would quote, as a cowboy engineering sense, if I just put it to rivets in there, and it'll be sweet, bro.
[00:11:36 - 00:11:42] But for this, we kind of want to, there's a trade off because you want to make your fingers light as possible.
[00:11:42 - 00:11:51] So if you do that, you know, you're, you're having to kind of work out what is the optimum design for your kind of marks that you want to get on with the assignment.
[00:11:51 - 00:11:52] Yeah.
[00:11:52 - 00:11:55] So in the video, they were all glued.
[00:11:55 - 00:11:57] I'll show you last year's videos. Some of them will be riveted.
[00:11:57 - 00:11:58] Yeah.
[00:11:58 - 00:11:59] Cool.
[00:11:59 - 00:12:07] I'll always be kind of bringing in various previous designs so that people can get some inspiration of what things are possible.
[00:12:07 - 00:12:08] Cool.
[00:12:08 - 00:12:12] So we can see here, we've got our main dimensions of the testing apparatus.
[00:12:12 - 00:12:21] And I've tried to make it really clear that this distance of 400 millimeters is from this lower pin here to anywhere on this top of line,
[00:12:21 - 00:12:26] as long as that dotted line is within the per-spec safety kind of zone.
[00:12:26 - 00:12:27] Yeah.
[00:12:27 - 00:12:30] So this shake here is only one possible shape that it could be.
[00:12:30 - 00:12:31] We'll see a bunch of examples.
[00:12:31 - 00:12:34] Here's an example of one that's a bottom, right angle triangle.
[00:12:34 - 00:12:38] Obviously that looks slightly different if I was to draw that in the diagram.
[00:12:38 - 00:12:39] Yeah.
[00:12:39 - 00:12:43] So what we can see here is that our structure needs to meet these specifications.
[00:12:43 - 00:12:50] So 400 millimeters or two and 280 millimeters from our vertical distance between those two pins.
[00:12:50 - 00:12:54] Plus or minus three millimeters for these specific links.
[00:12:54 - 00:12:55] Yeah.
[00:12:55 - 00:12:59] So we're giving some tolerance, which is what engineers love to work towards, right?
[00:12:59 - 00:13:00] Or within.
[00:13:00 - 00:13:01] Cool.
[00:13:01 - 00:13:04] So this one here, the slide, this is on a roller.
[00:13:04 - 00:13:12] So obviously if you have a three-view in the structure, it's going to be that length will be defined by the length of your member.
[00:13:12 - 00:13:18] But that just basically means that there's no vertical support on this mr.
[00:13:18 - 00:13:23] So if you were to have a two-meme structure, which we'll see a couple versions of,
[00:13:23 - 00:13:31] you'll see that they always sort of follow the exact same shape where this top nyender is always slightly above the horizontal.
[00:13:31 - 00:13:41] And that's because physics plays ball and you have to have an angle that will support exactly the mass of this roller.
[00:13:41 - 00:13:42] Yeah.
[00:13:42 - 00:13:43] Cool.
[00:13:43 - 00:13:44] Sweet.
[00:13:44 - 00:13:53] So in terms of submission, for the first part of the assignment, it'll be required to do an electronic submission of the cover sheet report calculations and drawings.
[00:13:53 - 00:14:01] It'll also be required to do a physical submission of all your drawings, which you might have two to four drawings depending on how many nims you have.
[00:14:01 - 00:14:03] And this will be put in the level two drop box.
[00:14:03 - 00:14:09] And you might also want to include this modes of failure sheet, which is on learn just a little on the test day.
[00:14:09 - 00:14:19] If you've had a mind-blink and count on your, what you're second and third mode of failure are if something, if your first mode of failure wasn't to kind of actually occur that you have them there.
[00:14:19 - 00:14:24] And we'll see when we go through the marksheet at the end marks associated to that.
[00:14:24 - 00:14:26] Why do we need a physical submission?
[00:14:26 - 00:14:33] Well, before you test, you'll be checked that your design has been made to your drawings.
[00:14:33 - 00:14:41] And then this is a really easy way for me to make sure that every student or every team actually has their physical drawings submitted with their name on them.
[00:14:41 - 00:14:55] The students seem to sometimes forget to put their name on the drawings, so then it means if I just get them all printed out, then I get like 20 to 40 groups that are just drawn by x6 on the 13th of January, 23 or something like that.
[00:14:55 - 00:15:03] So if you go on the assignment sheet, we can see we've got our color sheet there that you might want to use.
[00:15:03 - 00:15:08] And then this is our example test day modes of failure.
[00:15:08 - 00:15:14] So you put your team members on here, what your intended failure load is that's the total load.
[00:15:14 - 00:15:20] And then what you're first, second and third mode of failure is so first one should always basically be your stress concentration.
[00:15:20 - 00:15:27] And then it might be, I don't know, buckling of your horizontal member and then the third one might be bearing stress at the bottom pen.
[00:15:27 - 00:15:35] I don't know, you would have done calculations to work out what is the most likely modes of failure to occur after your stress concentration.
[00:15:35 - 00:15:36] Cool.
[00:15:36 - 00:15:45] And then on the test day, you'll be testing your device and there are these things that you will be kind of marked for.
[00:15:45 - 00:15:49] And we'll go over in a more detail when we actually look at the mark sheet.
[00:15:49 - 00:15:52] You can see two different types of handbooks structures generally.
[00:15:52 - 00:15:55] The general types as plus or minus 0.5.
[00:15:55 - 00:16:04] We'll note that they're a kind of different linear acceptable linear dimensions for different kind of links, but we'll touch on that in the future kind of tutorials.
[00:16:04 - 00:16:11] And also team to see in each of these grades will be derived from a team-mate rating.
[00:16:11 - 00:16:13] Have you guys had to do team-mate ratings for anything before?
[00:16:13 - 00:16:17] Yeah. So pretty simple, but there'll be this thing here that you click on.
[00:16:17 - 00:16:24] I think there's like three or four questions that you just rate on the scale of like 1 to 5 for like how you guys work because the team.
[00:16:24 - 00:16:34] And if you both rate each other well, then pretty much for like 99% of people would make absolutely no difference in the grade because both of the teams, so your grade doesn't change.
[00:16:34 - 00:16:40] Sometimes people have a bit of a tough time and things don't necessarily go to plan.
[00:16:40 - 00:16:52] This is one way that I can make it clear that it's important that you work effectively as a team early, so you're not like unknowingly sort of stitching up someone else by being a bad team-nimber and just disappearing from the face of the earth.
[00:16:52 - 00:17:06] And then this means that it kind of also automates the process of people have disproportionately kind of put in effort that has a little kind of response mechanism.
[00:17:06 - 00:17:07] We'll pull it.
[00:17:07 - 00:17:08] Yeah?
[00:17:08 - 00:17:09] But yeah.
[00:17:09 - 00:17:14] For most people, it's just a formality because you're greater working in a team and it's an easy thing to do.
[00:17:14 - 00:17:22] The thing that I do need to make really clear though is that these will only be open at these times.
[00:17:22 - 00:17:27] And then once they're closed, they'll be closed and if you don't do it in time, then you lose.
[00:17:27 - 00:17:29] It'll be appealing for not doing it right.
[00:17:29 - 00:17:37] So if you're annotating or making some notes of today, I'll just kind of make a note to definitely do your teammate racing or not to do it.
[00:17:37 - 00:17:49] So there's another one that will be done during the week of the testing just so that they'll relate to how you guys manufacture the device or just structure together.
[00:17:49 - 00:17:50] Cool.
[00:17:50 - 00:17:55] Any questions so far?
[00:17:55 - 00:17:57] We're doing really well.
[00:17:57 - 00:17:58] All right.
[00:17:58 - 00:18:01] So in terms of the rules, there are some rules that we need to make sure that we follow.
[00:18:01 - 00:18:09] And this basically just makes sure that you're device fits in the decent apparatus and that you're also able to,
[00:18:09 - 00:18:14] learn from the learning outcomes that are intended from this assignment.
[00:18:14 - 00:18:30] So all your ends will be connected via pins and individual members will either be blue or riveted as we sort of saw examples of as per the kind of requirements of having at least one of each type completely.
[00:18:30 - 00:18:34] So we don't want to head like something as glued and riveted needs to be one or the other.
[00:18:34 - 00:18:38] And no point shall the width of the structure be greater than 50 mil.
[00:18:38 - 00:18:42] That's just a little fits inside the brackets and the low detachment.
[00:18:42 - 00:18:49] If you have a structure that is wider than 50 mil, then that's going to be impossible to fit into the testing apparatus.
[00:18:49 - 00:18:55] The position I may be anywhere vertically within the double outline of the test structure walls.
[00:18:55 - 00:18:59] So within the test pitch there's detail about the orange dotted line in the figure.
[00:18:59 - 00:19:03] So we're going to apply some pins of 8mm and 7mm length.
[00:19:03 - 00:19:07] We'll give you some that you can test closer to the time.
[00:19:07 - 00:19:12] But I need to put them on like a safe chain or something so that they don't go missing because all of the other put them down.
[00:19:12 - 00:19:21] And then we have to get a bunch of all pins made and then the technicians complain to me that I haven't made for all these very precisely length.
[00:19:21 - 00:19:26] The size of length of pin because we want them to all be the same mess for consistency.
[00:19:26 - 00:19:29] Anyway, going into way too much detail.
[00:19:29 - 00:19:34] And the way in screw them in process will take place and they'll kind of be where they weigh.
[00:19:34 - 00:19:39] You're structured with out pins that will give the mess for the strength to weight ratio.
[00:19:39 - 00:19:48] And then also that will enable the technicians to check that you've made to design to the specifications of your drawings.
[00:19:48 - 00:19:54] Only two supports can be used either that top support or bottom support and we've talked about how the top support is on a roller.
[00:19:54 - 00:20:00] We'll probably bring the testing apparatus to one of the drop-in sessions so that it's not too far from the office.
[00:20:00 - 00:20:05] You need to design your structured afala stress concentration.
[00:20:05 - 00:20:10] Then you've got members for weight reduction as allowed as long as the failure is a stress concentration.
[00:20:10 - 00:20:19] And obviously we can't have just like a sacrificial timber that will hang all-fowl kind of nice, dirty triangle that we know it's going to break as soon as we kind of mess right.
[00:20:19 - 00:20:25] Because that way it's the mess too easy. It's just like the load on the members, the load that's supplied to it.
[00:20:25 - 00:20:27] So that's why we wanted you to have to do.
[00:20:27 - 00:20:34] Use that trigonometry and work out what the forces are on its humenders to make it kind of actually be designed in that way.
[00:20:34 - 00:20:38] Cool. So I've got some examples of people thinning their members.
[00:20:38 - 00:20:42] And this is a point that I really need to hammer home as that you need.
[00:20:42 - 00:20:47] Your design to fail at a stress concentration which is a hole or a notch.
[00:20:47 - 00:20:52] So if we look at these tenders here, let's get the zoom working.
[00:20:52 - 00:20:54] We can see that people have thinned them out.
[00:20:54 - 00:20:57] Whoop. But there's no hole or notch.
[00:20:57 - 00:21:01] So these are actually likely not failure members. That's why they're not broken.
[00:21:01 - 00:21:07] Yeah. So what we do want is something that might look like this.
[00:21:07 - 00:21:12] So this one here, they haven't thinned them in there, but they've done a bunch of weight saving holes.
[00:21:12 - 00:21:15] And then they've got their failure point in the middle.
[00:21:15 - 00:21:20] Or you might just make it without any failure, without any weight reduction.
[00:21:20 - 00:21:22] And you have a hole in the middle or not, you're not going to do right.
[00:21:22 - 00:21:26] That's going to make it really clear that we want a hole or a notch, not just a dog bone.
[00:21:26 - 00:21:29] Because then that means that you don't have a stress concentration.
[00:21:29 - 00:21:33] And obviously there's like a great area as you make your dog bone shorter and shorter.
[00:21:33 - 00:21:36] Like approximately becomes a notch at some point.
[00:21:36 - 00:21:38] Yeah, going with me.
[00:21:38 - 00:21:42] So then there becomes some dubious ones where you might have like quite a wide notch.
[00:21:42 - 00:21:45] And you're like, yeah, George, this is a stress concentration.
[00:21:45 - 00:21:51] And then I have to go, oh, I have to actually check whether your calculations have assumed it to be a stress concentration.
[00:21:51 - 00:21:55] Or you put the shapes specifically so that you don't have any stress concentration.
[00:21:55 - 00:21:58] And you really reliably know when your thing's going to fail.
[00:21:58 - 00:22:00] Does that make sense?
[00:22:00 - 00:22:02] So that's why I just try to make it really clear.
[00:22:02 - 00:22:05] Just do obviously a hole, obviously a notch.
[00:22:05 - 00:22:06] And then we're sort of happy days.
[00:22:06 - 00:22:15] But we'll talk about strength, stress concentrations and the difference between stress concentration failure for brutal materials and dark-con materials.
[00:22:15 - 00:22:18] Some point over the next kind of week.
[00:22:18 - 00:22:19] Cool.
[00:22:19 - 00:22:20] Obviously manually assistance.
[00:22:20 - 00:22:24] Annual assistance to promote failure will result in a penalty.
[00:22:24 - 00:22:27] And while we're here, we can also go through these penalties.
[00:22:27 - 00:22:33] So if your structure is not within the tolerances outline in figure one, it'll be a penalty.
[00:22:33 - 00:22:38] If you can't put your structure together on the test day and it causes a delay, there'll be a small penalty.
[00:22:38 - 00:22:41] Mainly because on the test day we really need everything to work like clockwork.
[00:22:41 - 00:22:44] Because otherwise it'll take a very, very long time for me.
[00:22:44 - 00:22:48] So we try and make sure that your run's kind of like testing, testing, testing, testing, testing.
[00:22:48 - 00:22:51] I think it takes all up probably like...
[00:22:51 - 00:23:00] But two and a half days, probably like 16 hours for me, just like doing the same thing of recording and making sure they're all went well.
[00:23:00 - 00:23:03] We try and make things go as smoothly as possible on the test day.
[00:23:03 - 00:23:08] If you're a stress concentration as outside of its tolerance, then you'll have a penalty.
[00:23:08 - 00:23:11] If there's no stress concentration, there's a penalty.
[00:23:11 - 00:23:18] If there's a deliberate change or you just change things because you had a feeling of it once a call tonight before, then again, there'll be a penalty.
[00:23:18 - 00:23:25] Because when you make sure that you've made things to your drawing, especially if there's a tight tolerance on your stress concentration,
[00:23:25 - 00:23:29] there's like a critical mode for failure, right?
[00:23:29 - 00:23:38] And then obviously you need to make sure you've made the requirement of having two part epoxy or pop rivets using being used.
[00:23:38 - 00:23:47] After doing testing, you are a bit naughty and pushed down on the weights or you drop the weights so that it had an impact load.
[00:23:47 - 00:23:54] Then there'll be a penalty associated to that, just because if we engineer the activity, so if you know that something's kind of wrong,
[00:23:54 - 00:24:00] sometimes people might, if they know that if things do strong, they might try and promote failure like by doing that.
[00:24:00 - 00:24:04] So basically we want to make it really clear that it's not really worth trying to cheat.
[00:24:04 - 00:24:07] It'll just put on the course or to change.
[00:24:07 - 00:24:10] If you know your things are wrong, to change it really.
[00:24:10 - 00:24:15] And then sometimes people might find out some things by doing the testing that they haven't really thought of,
[00:24:15 - 00:24:17] and they might need to make a design change.
[00:24:17 - 00:24:21] And then retest just to get a passing grade, and I'll talk about that in a little bit more detail.
[00:24:21 - 00:24:27] In the future, just to finish here, we can see a professional approach in four-wanning or reduced penalties.
[00:24:27 - 00:24:34] If you spot an error in your design before the test day, get in touch with me immediately, and we can work through design changes.
[00:24:34 - 00:24:39] In the value of the penalties are at my discretion, and they'll be lower most likely than this.
[00:24:39 - 00:24:42] If you come to me with reasonable four-wanning, right?
[00:24:42 - 00:24:50] So if you submitted your design and you're like, oh, we actually ended up doing this thing, we realized that this thing here is actually stopping it from being out even.
[00:24:50 - 00:24:58] If you put together, like there's an interference between parts, then we can work through those kind of changes, or if you work out, oh, I need to update my stress concentration,
[00:24:58 - 00:25:00] then we'll kind of go through that there, right?
[00:25:00 - 00:25:02] That's kind of common practice and industry.
[00:25:02 - 00:25:07] If you found out that there was something wrong with your design, you don't wait until the things being made to make the change.
[00:25:07 - 00:25:17] Right? It's a lot cheaper for everyone involved if you make the year or spot the error and change it immediately before it has a kind of flow on impact.
[00:25:17 - 00:25:19] We talked about this in class.
[00:25:19 - 00:25:21] You know, I can be used.
[00:25:21 - 00:25:23] Should be used for these things.
[00:25:23 - 00:25:29] Make sure that you submit a declaration of AI use, even if you haven't used it.
[00:25:29 - 00:25:31] You say you didn't use it.
[00:25:31 - 00:25:34] And then the team that rings was sort of talked about, but they'll be open.
[00:25:34 - 00:25:44] It's sort of time to make it really clear when they close, but that's the kind of thing that you and your partner can help remind each other to do as well.
[00:25:44 - 00:25:46] Cool. Any questions?
[00:25:46 - 00:25:55] Yeah. We'll talk about material testing.
[00:25:55 - 00:26:03] We definitely want to do some material testing so that you know some of the days that will be kind of important for doing your calculations.
[00:26:03 - 00:26:05] Any other questions?
[00:26:05 - 00:26:06] Yeah.
[00:26:06 - 00:26:20] So we'll go over this in a little bit of a decal design that we need to think about.
[00:26:20 - 00:26:26] But broadly speaking, if we just have two members, side by side like this,
[00:26:26 - 00:26:29] this means when I ask the question later, we're going to nail this question.
[00:26:29 - 00:26:34] When you apply a force there, then if you just have them side by side, imagine that there's a gap between them.
[00:26:34 - 00:26:37] Then when the force is resolved, one is pushing, one is pulling.
[00:26:37 - 00:26:39] Okay. So twist.
[00:26:39 - 00:26:45] And that means they're like basically a thing will fail in a way lower load, because it's not actually acting as a pendulum.
[00:26:45 - 00:26:49] It's actually like a moment out of plane there that your design thing is.
[00:26:49 - 00:26:54] So sometimes you'll like five Kg on and the thing just goes, and then it's like,
[00:26:54 - 00:27:04] game over try again, and that's when they would add forks to basically make sure that the load is evenly distributed in the center of the panel of the center of the member of the mix sense.
[00:27:04 - 00:27:05] Yeah.
[00:27:05 - 00:27:07] Cool.
[00:27:07 - 00:27:08] Yeah.
[00:27:08 - 00:27:16] So the thing is that's really nice and we'll talk about this on Friday, that the reason we're doing pendulented is because at pendulented there's no moments, right?
[00:27:16 - 00:27:23] So that means that we only have axial forces going through our members, which make it easy to use can calculations to kind of determine.
[00:27:23 - 00:27:26] That I need to keep on track.
[00:27:26 - 00:27:29] So I'll keep on task for now, but it's really good question.
[00:27:29 - 00:27:32] That's what the force referred to.
[00:27:32 - 00:27:34] Anything else?
[00:27:34 - 00:27:36] That's burning away.
[00:27:36 - 00:27:37] Cool.
[00:27:37 - 00:27:42] So as you'll see here, there's a bunch of slides that kind of just highlight some of the key points.
[00:27:42 - 00:27:46] And I've talked about all of these, so I'm not going to spend much time talking about them.
[00:27:46 - 00:27:50] We do have points to scuff about using ECA, can we use the ECA?
[00:27:50 - 00:27:52] No, it's not marked.
[00:27:52 - 00:27:54] We don't teach you how to do non-linear.
[00:27:54 - 00:28:05] If at this point, which is what would really be useful for this assignment, if you were to do it, but essentially what we'll be marking is your hand calculations and that's really effective because we've only got kind of simple loading cases.
[00:28:05 - 00:28:12] 800 word report houses the term and does include the images and our report.
[00:28:12 - 00:28:14] We'll be counting that as well.
[00:28:14 - 00:28:15] It's just the body text.
[00:28:15 - 00:28:18] It's just to give you a quick guide of basically how long it should be.
[00:28:18 - 00:28:20] And it is quite a concise report.
[00:28:20 - 00:28:21] And that's put these lots of you.
[00:28:21 - 00:28:28] And if we got you each right between page report about this, then it would take my markers years of their life to go in a mark.
[00:28:28 - 00:28:29] Eight page limit.
[00:28:29 - 00:28:30] That's for the calculations.
[00:28:30 - 00:28:31] Yes, I agree.
[00:28:31 - 00:28:32] That is quite short.
[00:28:32 - 00:28:38] That does mean that you need to be quite concise with how you do your calculations and make use of the space that you've got.
[00:28:38 - 00:28:40] But again, it's the same thing.
[00:28:40 - 00:28:43] You've really clicked that the market tax and that page loads.
[00:28:43 - 00:28:47] It's going to add time for them to market and we want to try and make everything as kind of streamlined.
[00:28:47 - 00:28:52] It's possible and it also makes it easier for them to see and not miss something if these list pages are up.
[00:28:52 - 00:28:56] So we've got also those answers noted there.
[00:28:56 - 00:29:00] We see this little star here about the report.
[00:29:00 - 00:29:05] Do you want to discuss what I would recommend as hitting for your report?
[00:29:05 - 00:29:07] Yes.
[00:29:07 - 00:29:08] Okay, cool.
[00:29:08 - 00:29:11] So on this time in one, March 8th is the March 8th.
[00:29:11 - 00:29:13] So available on learn it.
[00:29:13 - 00:29:17] We can see the report here is basically, oh, this is going to click isn't it?
[00:29:17 - 00:29:18] Yeah.
[00:29:18 - 00:29:21] The report here has got these four lines that we're looking for.
[00:29:21 - 00:29:28] And you can see that the body of your report we're looking at your introduction, which I'll use as a hitting, your design development.
[00:29:28 - 00:29:36] So how you arrive at your design, why you chose to shape your chosen your material testing and results would be three headings that I'll use.
[00:29:36 - 00:29:37] Yeah.
[00:29:37 - 00:29:45] Then obviously you need to have a description of your final design and have some sort of way to communicate your failure loads.
[00:29:45 - 00:29:49] Your failure modes and your protected failure load range, which we can also talk about indeed have it.
[00:29:49 - 00:29:53] That might come from your material testing.
[00:29:53 - 00:29:54] Yeah.
[00:29:54 - 00:29:56] Isn't that a question that I asked last time?
[00:29:56 - 00:30:03] Does anyone agree that it's probably a good idea to have a picture or a figure of their final design in their report?
[00:30:03 - 00:30:04] Yes.
[00:30:04 - 00:30:06] I'm glad we all agree with that.
[00:30:06 - 00:30:08] There's definitely something that we'll be looking for.
[00:30:08 - 00:30:14] And every year there's someone that kind of complains to me saying, oh, I didn't know that we had to have a figure of our final design.
[00:30:14 - 00:30:18] But it's like, well, it's kind of what your whole report is about.
[00:30:18 - 00:30:28] So if we want a description of your final design, I definitely would note that you have a figure there and that figure will probably also help you to describe what the members are and what they're doing.
[00:30:28 - 00:30:29] Cool.
[00:30:29 - 00:30:32] So you can see there we also got last three calculations.
[00:30:32 - 00:30:37] We've got some estimates of what we would expect you guys to have kind of done calculations on.
[00:30:37 - 00:30:40] And then drawings in a time sheet.
[00:30:40 - 00:30:45] Similarly, on the test day, do anyone know who these people's names are?
[00:30:45 - 00:30:47] We've not got B1 and B2 now.
[00:30:47 - 00:30:49] Little history if you want.
[00:30:49 - 00:30:52] I did say to the last group, you know, first person at email me who they are.
[00:30:52 - 00:30:56] I'll come up with some sort of prize and I really sure what kind of prize that would come up with.
[00:30:56 - 00:31:00] But it's the little thing if you want to get sidetracked I suppose.
[00:31:00 - 00:31:08] But on the test day, the first thing that will happen is obviously you'll have to pass your screw in your ring just to make sure that the design that you have is the design that you said that you're going to have.
[00:31:08 - 00:31:11] And then you'll go and start putting messes on.
[00:31:11 - 00:31:15] Once you get past 20 kg, you'll get this 10 marks.
[00:31:15 - 00:31:19] And if you think about the 20 and 39, you'll get these marks.
[00:31:19 - 00:31:21] If you don't, then you don't get any of those.
[00:31:21 - 00:31:25] If you go above, then you'll just get one of those obviously if you're above 20 kg.
[00:31:25 - 00:31:29] Then you get some marks for your predicted failure load.
[00:31:29 - 00:31:33] So if your plus or minus 15 percent, which is not much, you'll get 10 marks.
[00:31:33 - 00:31:37] If your plus or minus 25 percent, you'll get 7 marks.
[00:31:37 - 00:31:41] If you're outside 25 percent, you get 0 marks.
[00:31:41 - 00:31:49] If it fails and you're predicted failure mode, then you either get 10, 7 or 5 marks, depending on what mode or failure it actually did.
[00:31:49 - 00:31:57] So if it ended up buckling into the horizontal plane of your vertical member, and that was what your second motor failure was, you would get 7 marks, right?
[00:31:57 - 00:32:03] And then here you've got your strength to weight ratio, which is based on these breakdowns here.
[00:32:03 - 00:32:07] I think last year there might have been a couple people that managed to get 10 out of 10.
[00:32:07 - 00:32:12] It's purposely pretty tight to try and quite a difficult one to do.
[00:32:12 - 00:32:17] But the reason that I've got this kind of pre-defined is that I have a nice spreadsheet where I can fill out all your results
[00:32:17 - 00:32:21] and give you what your mark was as soon as you've done your testing, right?
[00:32:21 - 00:32:26] Other than how much go I'm going to scale the strength of weight, so that the best person got 10 out of 10.
[00:32:26 - 00:32:28] Yeah?
[00:32:28 - 00:32:30] Any questions on any of those?
[00:32:30 - 00:32:35] So you're doing really well.
[00:32:35 - 00:32:36] I know I'm doing really well.
[00:32:36 - 00:32:39] I've been here for a one and a half hours at this point.
[00:32:39 - 00:32:40] But what we see here is on the test there.
[00:32:40 - 00:32:42] This is what the sea-hop will look like.
[00:32:42 - 00:32:49] I like quite like this photo because something funky is happening with Tony's leg, but I was doing a piano, and it obviously captured that.
[00:32:49 - 00:32:53] But what you can see here is that this is where the technicians will be.
[00:32:53 - 00:32:55] They'll weigh your structure without tons.
[00:32:55 - 00:32:58] They'll check your drawings and make sure everything's kind of made.
[00:32:58 - 00:33:00] I'll just get the green light there.
[00:33:00 - 00:33:03] I'll be sitting here off and out the details onto the spreadsheet.
[00:33:03 - 00:33:09] You'll check that I'll put those details into the spreadsheet correctly, then you'll go under your test and there'll be a TA to help you.
[00:33:09 - 00:33:16] We do also have the thing kind of being video recorded just in case we need to do like a TMO, either for
[00:33:16 - 00:33:20] DVS reasons, if people have been like, no, I didn't drop it.
[00:33:20 - 00:33:24] And then I'll have to go, okay, we'll look at the camera and you can see here you clearly dropped it.
[00:33:24 - 00:33:28] Or sometimes things will kind of break simultaneously.
[00:33:28 - 00:33:32] So we need to look at the camera footage into a slow motor workout.
[00:33:32 - 00:33:36] I did the stress concentration break and then it buckled or vice versa.
[00:33:36 - 00:33:39] Cool.
[00:33:39 - 00:33:41] So this is basically what we've already talked about.
[00:33:41 - 00:33:46] And that template on Loom will help to guide you with providing the three failure modes.
[00:33:46 - 00:33:51] Because sometimes people will be stressed in the day and they kind of completely forget what they even did calculations on.
[00:33:51 - 00:33:54] And then they don't know what the second mod failure was.
[00:33:54 - 00:33:57] And I just really want things to be going through as quickly as possible.
[00:33:57 - 00:34:02] So the idea is that if you have that stamped to your drawings, past you has kind of done you a self-assolar.
[00:34:02 - 00:34:05] Because then you know what your mod's a failure work is.
[00:34:05 - 00:34:08] When you did it, you kind of wrote it down and you know what it is.
[00:34:08 - 00:34:09] Yep.
[00:34:09 - 00:34:12] So the top point there, so we have to...
[00:34:12 - 00:34:16] Yeah.
[00:34:16 - 00:34:19] So the general tolerance is 0.5 millimeters.
[00:34:19 - 00:34:21] But you guys are the engineers.
[00:34:21 - 00:34:23] So as long as it's made to your drawings and your...
[00:34:23 - 00:34:27] So if there was something where you didn't care if it was past a minus 5 millimeters,
[00:34:27 - 00:34:29] sweet for that on your drawing.
[00:34:29 - 00:34:30] Yeah?
[00:34:30 - 00:34:32] But sometimes people go like, oh, I didn't know.
[00:34:32 - 00:34:36] And it's like, well your drawing says everything is the past minus 0.5 or what.
[00:34:36 - 00:34:39] I think the standard on the UC template is past minus 0.1, right?
[00:34:39 - 00:34:42] Which is like, that's pretty tight.
[00:34:42 - 00:34:48] So yeah, this is trying to give you the have ownership of what times as you put on your drawing.
[00:34:48 - 00:34:50] You can put whatever you want.
[00:34:50 - 00:34:52] Like if it was just like some weight-saving holes.
[00:34:52 - 00:34:54] These ones here, for example.
[00:34:54 - 00:34:58] It probably does not matter if that was plus or minus 5 mill each of them, right?
[00:34:58 - 00:35:00] Just the number of holes.
[00:35:00 - 00:35:03] But yeah, you can kind of make that clear on your drawing.
[00:35:03 - 00:35:05] Otherwise you'll refer...
[00:35:05 - 00:35:09] The baseline one is what it says here.
[00:35:09 - 00:35:10] Yeah?
[00:35:10 - 00:35:17] And 0.14, your stress concentration and past or minus 3 millimeter on figure one.
[00:35:17 - 00:35:20] I think it's what it's said for those other dimensions.
[00:35:20 - 00:35:21] Cool.
[00:35:21 - 00:35:22] All right.
[00:35:22 - 00:35:24] So here we see some photos.
[00:35:24 - 00:35:28] Here's a start photo of Keith Alexander and some cool.
[00:35:28 - 00:35:31] This guy was like the old Oscar, pretty cool jumper.
[00:35:31 - 00:35:36] But we just put that in there for, I don't know, expecting our heritage reasons.
[00:35:36 - 00:35:39] Do see some examples of pericep structures.
[00:35:39 - 00:35:41] People putting them in the design.
[00:35:41 - 00:35:43] The masses are 5 kg and 2 kg.
[00:35:43 - 00:35:46] The weight of the hanger is 1.09.
[00:35:46 - 00:35:48] That is a key thing to note.
[00:35:48 - 00:35:54] So the mass that it breaks, the failure load is the load including the chain and the hanger, right?
[00:35:54 - 00:36:00] So this sometimes stitches people up because they start cheering because they just put their 9 kg on and then it broke.
[00:36:00 - 00:36:04] Then that she means that 40.09 and that he outside the zone.
[00:36:04 - 00:36:05] And that's the last thing you can do.
[00:36:05 - 00:36:06] Cool.
[00:36:06 - 00:36:08] So the mass includes this mass here of the hanger.
[00:36:08 - 00:36:13] I think it would be a failure if it touches the wall or the flexus similar amount.
[00:36:13 - 00:36:19] And the other plane here we see a nice pericep structure having some nicking happening at the stress concentration.
[00:36:19 - 00:36:21] That's kind of where we want our thing to fail.
[00:36:21 - 00:36:23] Make sure you keep in clear of the weights.
[00:36:23 - 00:36:26] When you are doing the testing, here we see some more examples.
[00:36:26 - 00:36:28] Here we see a nice two-millimeter structure.
[00:36:28 - 00:36:30] And upside down, three-millimeter structure.
[00:36:30 - 00:36:33] Bottom-right angle, three-millimeter structure.
[00:36:33 - 00:36:36] This one here's another bottom-right angle through the infrastructure.
[00:36:36 - 00:36:41] That's where we'll be talking more about this kind of what shapes you might want to do on Friday.
[00:36:41 - 00:36:46] The choice is basically yours as design engineers.
[00:36:46 - 00:36:52] So just quickly, in your table, we'll probably have like a one-minute discussion and we'll come back to this other end.
[00:36:52 - 00:36:57] What tasks do you think need to be done to complete this assignment?
[00:37:36 - 00:37:48] All right, thank you everyone.
[00:37:48 - 00:37:52] Just because I know that I've got a real tight timeframe, I'm going to keep our skin.
[00:37:52 - 00:37:57] But we'll be able to build on that list that you guys might have started towards the end.
[00:37:57 - 00:38:00] And then we'll start our Friday kind of tutorial by looking at it.
[00:38:00 - 00:38:04] So me starting with Friday, let's sort of a prank.
[00:38:04 - 00:38:06] But that's all good.
[00:38:06 - 00:38:08] So what we'll need to do as well.
[00:38:08 - 00:38:11] We'll have an opportunity to click your strips.
[00:38:11 - 00:38:13] We've got some aluminium strips here.
[00:38:13 - 00:38:16] I'll be hanging outside if we want to click them today.
[00:38:16 - 00:38:20] And the idea is that you pick two per person and you'll sign your name, which basically says,
[00:38:20 - 00:38:25] like, you know that I'm responsible for my aluminium strips and if I lose them, that's all mean.
[00:38:25 - 00:38:27] If I use too much, that's all me.
[00:38:27 - 00:38:33] But the idea that this should be plenty for everyone, four strips will be used for both your material testing and for actually making your structure.
[00:38:33 - 00:38:37] Cool. So I plan how to use them carefully.
[00:38:37 - 00:38:38] So we can see that there.
[00:38:38 - 00:38:44] When it comes to manufacturing your structure, we do have a range of spaces on our wing where we can do them.
[00:38:44 - 00:38:47] So we've got a bunch of clamps that you might use when you're gluing drill presses.
[00:38:47 - 00:38:50] A bunch of tops there are for gluing on.
[00:38:50 - 00:38:53] There's also the undergraduate workshop.
[00:38:53 - 00:38:55] Collectually known as the warm in room.
[00:38:55 - 00:38:57] I don't think it is called it anymore.
[00:38:57 - 00:39:03] And then we'll also have this kind of area under the stairs here where you can kind of as well build your own.
[00:39:03 - 00:39:08] As well build your structure or build your kind of material testing dog bones.
[00:39:08 - 00:39:11] Health and safety is in here for completeness.
[00:39:11 - 00:39:12] Make sure you're aware of hazards.
[00:39:12 - 00:39:14] Report anything that you think is dangerous.
[00:39:14 - 00:39:17] Forget how someone uses the first aid stuff.
[00:39:17 - 00:39:23] That's all the stuff that Oscar and Tony said today from the technicians.
[00:39:23 - 00:39:25] Make sure you look after your strips.
[00:39:25 - 00:39:28] So don't try and put them somewhere that you think safe and then they're cleaner.
[00:39:28 - 00:39:29] Kind of picks them up. You're responsible.
[00:39:29 - 00:39:30] Kind of for them.
[00:39:30 - 00:39:34] Pre-productive of your time trying to get some things done early while you don't have too much on.
[00:39:34 - 00:39:37] And then glue is not in the infinite supply.
[00:39:37 - 00:39:41] So as Tony said he's always about worried about running out of glue.
[00:39:41 - 00:39:46] Make sure you're always clamping your work piece that you're tidying up after yourself.
[00:39:46 - 00:39:54] There are also these hand tools that are available to some people may want to kind of make their notches using a notcher.
[00:39:54 - 00:39:59] Or they might want to build some interesting cross-sections using the folder.
[00:39:59 - 00:40:07] These are things that you'll kind of have to test hard to recommend doing sort of small test pieces to make sure that you can kind of do it.
[00:40:07 - 00:40:10] And some people are pretty crafty or what they're able to do.
[00:40:10 - 00:40:13] But it's not like a tutorial on how to use each of these things.
[00:40:13 - 00:40:17] So if you're unsure then you can always ask one of the technicians.
[00:40:17 - 00:40:21] In terms of the drills, the special kind of sheet needle drills that are used.
[00:40:21 - 00:40:24] And it's pretty clearly kind of labeled.
[00:40:24 - 00:40:27] And then this is also kind of in here for completeness.
[00:40:27 - 00:40:31] But we don't want to glue where our pins are.
[00:40:31 - 00:40:37] We'll be using pins for joining our individual mim, joining our three or two mim just together.
[00:40:37 - 00:40:40] And then for individual mim we'll either use glue.
[00:40:40 - 00:40:43] Which we have some tips on how to get the most out of your glue.
[00:40:43 - 00:40:47] And I can show that it is a get-a-bonne kind of properly.
[00:40:47 - 00:40:51] So if I can share a clean surface and that it's kind of got a little bit of roughness to it.
[00:40:51 - 00:40:53] It is kind of some of the main things.
[00:40:53 - 00:40:57] We'll see some links to the material data sheets.
[00:40:57 - 00:41:00] So if you want to know what the actual kind of defines.
[00:41:00 - 00:41:04] Drinkers don't use the windowsills for gluing up.
[00:41:04 - 00:41:06] They just got them repainted.
[00:41:06 - 00:41:12] So they might be a bit like annoyed with you if you do them on the windowsills.
[00:41:12 - 00:41:18] But that's why there's lots of the benches that have the steel benchtops to gals.
[00:41:18 - 00:41:20] That's kind of the place to be doing it.
[00:41:20 - 00:41:23] Similarly there's a video here for how you can actually use a river
[00:41:23 - 00:41:25] if you've not had to do that before.
[00:41:25 - 00:41:28] Obviously it kind of relates to sustainable development.
[00:41:28 - 00:41:37] Go 12 of reducing our waste and it just means we can recycle those mimers rather than having to try and work out what we do with all these semi-glue together.
[00:41:37 - 00:41:41] There's some more documents there we can discuss in the future.
[00:41:41 - 00:41:44] So your bill just druts your own drawings.
[00:41:44 - 00:41:47] They'll cut, farm and drill as required.
[00:41:47 - 00:41:54] There's not kind of a privilege for you to use the lazy color or seeing sea machines or similar.
[00:41:54 - 00:41:56] So basically there's way to be in your view.
[00:41:56 - 00:42:01] To be able to do that, so make sure you keep that in mind that you'll be making your own structure.
[00:42:01 - 00:42:04] You may want to finish critical edges with some care.
[00:42:04 - 00:42:13] So inside of your stress concentration for example, you'll probably want to make sure that that is as similar to your test pieces as possible.
[00:42:13 - 00:42:15] So you're getting reliable results.
[00:42:15 - 00:42:17] Give yourself enough time for the glue to sit.
[00:42:17 - 00:42:21] Every year there's one group that like the glue is still goopy.
[00:42:21 - 00:42:25] Then it like fails because of the glue.
[00:42:25 - 00:42:30] So stay in the head and make sure that you can have lots of time for the glue to be sit.
[00:42:30 - 00:42:37] And obviously there's going to be a lot of you so get an early and don't leave also last minute otherwise.
[00:42:37 - 00:42:40] And maybe difficult to do what you want to do.
[00:42:40 - 00:42:51] And I'll recommend doing a trial assembly which is just using pins to make sure that your holes that you have drilled are actually the right size to allow the pins to go through them.
[00:42:51 - 00:42:54] And take care of your structure.
[00:42:54 - 00:42:59] So we'll put the testing apparatus out of some point.
[00:42:59 - 00:43:03] But the pins will make it easy to a trial assembly.
[00:43:03 - 00:43:10] And yeah, don't let you do a trial run just fully test your thing before the test day.
[00:43:10 - 00:43:13] So that's why we don't have the apparatus out all the time.
[00:43:13 - 00:43:19] But I'll probably bring it along to one of the coffee droppings if people want to look at how those different mechanisms work.
[00:43:19 - 00:43:28] So material testing will be used to complete and find out what the ultimate test is of your material, the yield point possibly if you want to.
[00:43:28 - 00:43:30] And then also the young's modulus.
[00:43:30 - 00:43:33] So you'll need those for some of your calculations.
[00:43:33 - 00:43:38] And you also want to know what the failure forces for your chosen stress concentration.
[00:43:38 - 00:43:41] And from that you might be able to determine what the cave value is.
[00:43:41 - 00:43:47] But we'll talk a little bit more detail about stress concentration or remind you about them next week.
[00:43:47 - 00:43:51] You need to bring a USB stick for your material testing.
[00:43:51 - 00:43:56] And make sure that you don't lose that or forget to save it on there.
[00:43:56 - 00:44:00] Because there's always someone each year that does all this testing and it doesn't save the data.
[00:44:00 - 00:44:03] And then it's like, George, what do I do?
[00:44:03 - 00:44:05] And I might well guess you have to read tests.
[00:44:05 - 00:44:10] There's not really anything I can do to magically make your results reappear.
[00:44:10 - 00:44:14] We heard from Oscar, who's the kind of main person in those areas.
[00:44:14 - 00:44:19] These are estimates of times that the materials will be open.
[00:44:19 - 00:44:21] I think Oscar actually is in earlier.
[00:44:21 - 00:44:24] So if you're in one person and want to go on an eight o'clock, then that's probably all good.
[00:44:24 - 00:44:28] But this will hear from the technicians as terms of what the time is.
[00:44:28 - 00:44:35] So the process will go that you make your own dog bones from your strips of aluminium.
[00:44:35 - 00:44:39] You'll cut them to shape and maybe file them to shape and the student workshop.
[00:44:39 - 00:44:43] And then once it runs done some testing, you can kind of relate someone or results.
[00:44:43 - 00:44:50] But the best thing is that you know your own results because you know how those were actually kind of derived.
[00:44:50 - 00:44:56] So here's some examples from first picks where they've had different dog bones be tested.
[00:44:56 - 00:44:59] And you can see it's pretty straightforward if you just work out what your work thing is.
[00:44:59 - 00:45:05] You can use that to determine what the stress is based on those values there.
[00:45:05 - 00:45:09] If you're only looking at UTS and you can just use your failure load to determine that.
[00:45:09 - 00:45:14] So here we see an example of a dog bone using an aluminium strip.
[00:45:14 - 00:45:16] So that's what you're kind of making.
[00:45:16 - 00:45:22] You can see that there's two holes here because that's what the house field tips on the grips look like.
[00:45:22 - 00:45:25] So you want to make sure that you're getting a failure in the middle.
[00:45:25 - 00:45:26] Not at these pins there.
[00:45:26 - 00:45:33] And the way to do that is to make sure that your reduced section has smaller cross-sectional area than that area on either side of the pins.
[00:45:33 - 00:45:36] So sometimes people would do it and then at the broken at the pin.
[00:45:36 - 00:45:37] And they say, I do what's happened.
[00:45:37 - 00:45:39] It's like, oh, that's the weakest point.
[00:45:39 - 00:45:41] So that's the result that you've kind of been getting.
[00:45:41 - 00:45:44] Also in the past is recommended using this standard.
[00:45:44 - 00:45:47] Unfortunately, because we don't have 50 mil wide material.
[00:45:47 - 00:45:51] We can't make out the mentions of our dog bones exactly to this.
[00:45:51 - 00:45:56] And so that's why we recommend making something like this and just knowing what your own cross-section is.
[00:45:56 - 00:46:02] So as long as it breaks in that reduced section, you'll know that you've kind of done a good job.
[00:46:02 - 00:46:07] And to avoid unsweeted failure, basically do what we did there, make sure they reduce section.
[00:46:07 - 00:46:13] There's the place and then you can tighten that grip to make it less likely to break an at-pin there.
[00:46:13 - 00:46:16] Cool. I might want to use an 18-seamometer.
[00:46:16 - 00:46:25] So to get the yungs module right, so to use this, so if you're not exactly sure how it goes on, ask Oscar because they're kind of a little bit delicate.
[00:46:25 - 00:46:28] But that should be detailed in these videos here.
[00:46:28 - 00:46:31] And that will enable you to get a plot that looks like this.
[00:46:31 - 00:46:35] And then from there, using the slope of this line here, you can get your yungs module list.
[00:46:35 - 00:46:39] You can determine the yield point as well from the suit and amount of strain that is going to occur.
[00:46:39 - 00:46:43] I think it's maybe 0.1 per minute if you measure enough to the top of my head.
[00:46:43 - 00:46:46] But basically this point here, it starts plastically deforming.
[00:46:46 - 00:46:50] And then obviously your ultimate team's arsteres is the next point here.
[00:46:50 - 00:46:53] So those are three things that you might want to look at.
[00:46:53 - 00:47:01] In the past, on a normal year, just look at working about designing to the yield, because you don't want your thing to break.
[00:47:01 - 00:47:05] We've got a kind of interesting design task we were actually wanting, I think, to fail.
[00:47:05 - 00:47:13] So we have to kind of go a little bit more detailed in terms of our material testing and make sure we understand that mechanism as well.
[00:47:13 - 00:47:19] But we'll talk about this in a little bit more than upcoming classes.
[00:47:19 - 00:47:27] So you see here, if having just yield in the wooden of broken right, there's just where it's starting to plastically deform.
[00:47:27 - 00:47:28] And we're wanting fracture.
[00:47:28 - 00:47:32] So most materials, yield is not the same as fracture.
[00:47:32 - 00:47:37] It's a really brittle material like glass, maybe it can be the same.
[00:47:37 - 00:47:40] We'll talk about that in a little more detail.
[00:47:40 - 00:47:47] So here we see some examples of other geometries that have been used with perspia structures, just to give you some inspiration.
[00:47:47 - 00:47:50] I don't know why they have two holes.
[00:47:50 - 00:47:55] Maybe ones of different size, but maybe they'll be the second and first in sticking motor failure, for example.
[00:47:55 - 00:47:59] You know, you guys are the bosses, so you can pick what you want to do for your design.
[00:47:59 - 00:48:05] Here we see the classic two-meme structure, and there's that classic kind of shape that it ends up being.
[00:48:05 - 00:48:10] And another two-meme structure there.
[00:48:10 - 00:48:14] I had also filled out a bunch of previously asked frequently asked questions.
[00:48:14 - 00:48:26] And yeah, there's also these things I've just put in for completeness, but there's actually this table here is on our assignment on the last page, right?
[00:48:26 - 00:48:37] So if you're doing a two-meme structure, you'll want to know that there's a bit upper support, so that you can actually calculate what that angle is.
[00:48:37 - 00:48:40] To make sure that it's got the right dimensions, but that doesn't make any sense.
[00:48:40 - 00:48:42] Don't worry, we'll talk about that on Friday.
[00:48:42 - 00:48:46] When we do an example, free body diagram of a three-meme structure.
[00:48:46 - 00:48:50] Yep. There's two versions. There's two of them.
[00:48:50 - 00:48:53] Still everything. Yeah.
[00:48:53 - 00:49:01] Like there's two stations that you might be testing on, so just tested both of them there.
[00:49:01 - 00:49:04] Cool. So we've got like two, one minute.
[00:49:04 - 00:49:09] What do we got quickly? A planning session. What did you write down of cut-cut key tasks that you need to do?
[00:49:09 - 00:49:10] Cool.
[00:49:10 - 00:49:11] Next.
[00:49:11 - 00:49:12] Cool.
[00:49:12 - 00:49:15] Next.
[00:49:15 - 00:49:22] Okay. Yeah. I'll go calculations.
[00:49:22 - 00:49:23] No, right.
[00:49:23 - 00:49:24] As well.
[00:49:24 - 00:49:25] S C F.
[00:49:25 - 00:49:27] But we can add detail to that. What else?
[00:49:27 - 00:49:29] Yep.
[00:49:29 - 00:49:34] So I'm going to just say sketch design.
[00:49:34 - 00:49:35] Maybe. Yeah. Go.
[00:49:35 - 00:49:36] Next.
[00:49:36 - 00:49:39] Cool. Yeah.
[00:49:39 - 00:49:42] So I'm going to write CAD plus drawings.
[00:49:42 - 00:49:43] Next.
[00:49:43 - 00:49:54] You'll probably want to test all modes of failure, but I'll probably also do at least material tips.
[00:49:54 - 00:49:56] We'll just call it.
[00:49:56 - 00:50:02] I've done that. So it could be S C F plus I know.
[00:50:02 - 00:50:05] Youngs. Anything else?
[00:50:05 - 00:50:09] Yep. So there will definitely be later.
[00:50:09 - 00:50:12] Anything else. What else do we have to submit?
[00:50:12 - 00:50:14] Report.
[00:50:14 - 00:50:15] Report.
[00:50:15 - 00:50:17] So we've got caps. We've got report.
[00:50:17 - 00:50:22] And then up here what I sort of said would also be collect.
[00:50:22 - 00:50:24] Strips.
[00:50:24 - 00:50:28] And then probably also somewhere in here we want to have read the brief.
[00:50:28 - 00:50:36] Because we're basically all up on time, what we'll do is we'll probably expand this a little bit on Friday.
[00:50:36 - 00:50:44] And what I've done is actually I've already written a version of this list on the assignment handout, right?
[00:50:44 - 00:50:47] So there's some things that you can do in different orders.
[00:50:47 - 00:50:51] Basically this will be things to kind of take off for our process that you could follow.
[00:50:51 - 00:50:55] There's multiple ways you can kind of go about it, but we'll talk about it more on Friday.
[00:50:55 - 00:50:59] If you want to pick up a strip, I'll take them outside just so I'm a physical class.
[00:50:59 - 00:51:03] We're not like getting told to leave.
[00:51:05 - 00:51:07] Anything around?
[00:51:07 - 00:51:12] Anything so true to the handout?
[00:51:12 - 00:51:13] Yep.
[00:51:13 - 00:51:15] I'll always be there.
[00:51:15 - 00:51:16] I'll go up.
[00:51:16 - 00:51:18] Do you think we'll have a cut down?
[00:51:18 - 00:51:19] I think.
[00:51:19 - 00:51:21] Yeah.
[00:51:25 - 00:51:27] Anytime that something I'd like to click on now.
[00:51:27 - 00:51:28] But, um.
[00:51:28 - 00:51:33] Then actually, I'm just going to put me around this stuff before I forget.
[00:51:33 - 00:51:36] Yeah, I think everything's pretty much recorded.
[00:51:36 - 00:51:40] I'm just going to put me around this stuff before I forget.
[00:51:40 - 00:51:41] Yeah.
[00:51:41 - 00:51:42] Cool.
[00:51:42 - 00:51:44] These get recorded on post-electives.
[00:51:44 - 00:51:45] Yeah.
[00:51:45 - 00:51:46] I should be on Nickel yet.
[00:51:50 - 00:51:51] Thank you.
[00:51:58 - 00:51:59] Thanks.
[00:52:10 - 00:52:12] Thank you.
[00:52:40 - 00:52:42] Thank you.
[00:53:10 - 00:53:12] Thank you.
[00:53:40 - 00:53:44] Thank you.

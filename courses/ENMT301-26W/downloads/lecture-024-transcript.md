# ENMT301-26W Lecture 24 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `505491bf96bcb1b79fb3a913d3ff1f6b0be2a0d292ea90aec608bf7a47d33fd5`
Generated: 2026-06-06T05:56:50.635560+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:20 - 00:00:24] Okay, I'm sure you make a start.
[00:00:24 - 00:00:26] Is the...
[00:00:26 - 00:00:31] Can we attribute the lecture attendance to like the sunny weather or is just...
[00:00:31 - 00:00:34] Friday week four?
[00:00:34 - 00:00:35] What's that?
[00:00:35 - 00:00:39] That's the issue come along.
[00:00:39 - 00:00:40] You don't make a try.
[00:00:40 - 00:00:42] Surely you go to the make a try next lecture.
[00:00:42 - 00:00:46] Cool.
[00:00:46 - 00:00:48] It's a lot anymore.
[00:00:48 - 00:00:50] All right, so today we're going to start talking about...
[00:00:50 - 00:00:51] ...dependence.
[00:00:51 - 00:00:58] Right, so this comes down to...
[00:00:58 - 00:01:02] ...you know, sort of reliability of the systems that we're designing.
[00:01:02 - 00:01:11] So there's a few...
[00:01:11 - 00:01:15] I've got a couple of quotes here which are quite relevant.
[00:01:15 - 00:01:20] A number of you said who's Douglas Adams on the...
[00:01:20 - 00:01:22] ...good to quotes on the...
[00:01:22 - 00:01:25] ...on the robo-cut team formation.
[00:01:25 - 00:01:28] So Douglas Adams was a writer.
[00:01:28 - 00:01:29] He wrote the H.I.C.S.C.
[00:01:29 - 00:01:30] ...that's got to the galaxy.
[00:01:30 - 00:01:33] But he was also generally quite smart.
[00:01:33 - 00:01:35] He also wrote this.
[00:01:35 - 00:01:39] And that's spot on really to come a mistake that people make when trying to design something
[00:01:39 - 00:01:44] to do completely foolproof is to underestimate the ingenuity of complete force.
[00:01:44 - 00:01:47] People do some weird shit.
[00:01:47 - 00:01:50] And they may do things that...
[00:01:50 - 00:01:52] ...you know, when you're designing a system.
[00:01:52 - 00:01:57] Maybe you don't even take that into account.
[00:01:57 - 00:01:59] And sometimes it's not from foolishness.
[00:01:59 - 00:02:03] It's just from assumed knowledge I suppose.
[00:02:03 - 00:02:06] So work when I was doing my PhD,
[00:02:06 - 00:02:12] we were developing a tablet-based software decision support system in the hospital.
[00:02:12 - 00:02:16] So allowing the nurses to figure out how much insulin to give the patients...
[00:02:16 - 00:02:18] ...in the intensive care.
[00:02:18 - 00:02:22] And it turns out that they were just normal and joint tablets.
[00:02:22 - 00:02:27] And they were in some instances not getting charged.
[00:02:27 - 00:02:29] They knew they had to plug them in.
[00:02:29 - 00:02:33] But one of the other PhD students who was doing research went in one day.
[00:02:33 - 00:02:35] And they saw they plugged the tablet in.
[00:02:35 - 00:02:39] But the war war that it was plugged into wasn't plugged into the war.
[00:02:39 - 00:02:44] I mean, maybe that's just a one-off mistake.
[00:02:44 - 00:02:48] But you end up with things like you we assume perhaps that you...
[00:02:48 - 00:02:49] ...do you design something like that?
[00:02:49 - 00:02:54] You have to plug it in. You say in the instructions that you've got to plug it in.
[00:02:54 - 00:02:58] But it probably doesn't say then, make sure that's also plugged into the war.
[00:02:58 - 00:03:00] Because it's just an assumed thing.
[00:03:00 - 00:03:04] And in another instance, also with the intensive care,
[00:03:04 - 00:03:10] there was another support decision support system around choosing the level.
[00:03:10 - 00:03:12] The pressure, the positive in it's actually pressure.
[00:03:12 - 00:03:15] So when you're mechanically ventilated, it's a positive pressure system.
[00:03:15 - 00:03:18] So when we breathe normally, your diaphragm comes down.
[00:03:18 - 00:03:20] It causes negative pressure in your lungs.
[00:03:20 - 00:03:23] It goes in oxygen exchange occurs.
[00:03:23 - 00:03:24] And we're fine.
[00:03:24 - 00:03:26] But when you're mechanically ventilated, it's the opposite.
[00:03:26 - 00:03:31] So pressure pushes the ear into your lungs and something happens.
[00:03:31 - 00:03:36] But to stop the lungs collapsing, you know, if somebody's got pneumonia or if they've got liquid in the lungs,
[00:03:36 - 00:03:37] you leave.
[00:03:37 - 00:03:39] So it doesn't go back to atmospheric pressure at the end.
[00:03:39 - 00:03:42] They leave some pressure in your net positive in the respiratory pressure.
[00:03:42 - 00:03:49] And you want that to be high enough to keep the lungs inflated, but not so high as to damage the lungs.
[00:03:49 - 00:03:54] So some work around selecting values for that on the ventilator.
[00:03:54 - 00:03:58] And the system will come up and give a value.
[00:03:58 - 00:04:05] And the notice, like, whenever the value that was recommended was 13 doctors use silly units.
[00:04:05 - 00:04:11] So for pressure, air pressure that you see in the meters of water, blood pressure that is millimeters of mercury.
[00:04:11 - 00:04:14] I guess it's just going back to how things used to actually be measured.
[00:04:14 - 00:04:19] But whenever it came up as 13 centimeters of water that will never be selected,
[00:04:19 - 00:04:21] they will always just choose a different value.
[00:04:21 - 00:04:27] I suppose today's Friday the 13th, which is a good data to mention this.
[00:04:27 - 00:04:29] But the nurses had these superstitions.
[00:04:29 - 00:04:32] While optimally, that number was good.
[00:04:32 - 00:04:36] It's got negative connotations around it, so they just wouldn't choose them.
[00:04:36 - 00:04:44] So when you're designing things, stuff like this happens.
[00:04:44 - 00:04:46] So that's the important one.
[00:04:46 - 00:04:48] This other one is also really good.
[00:04:48 - 00:04:52] So you can look up this link, this guy, a forgious first name,
[00:04:52 - 00:04:55] Aiken. He was involved in spacecraft design for a long time.
[00:04:55 - 00:04:57] And he's got, I think there's 45 rules on there.
[00:04:57 - 00:05:02] Some of them are quite humorous. Most of them are very apt.
[00:05:02 - 00:05:06] And they apply much more generally than just spacecraft design.
[00:05:06 - 00:05:09] So there's on a spacecraft right takes an infinite amount of effort.
[00:05:09 - 00:05:12] That's why it's a good idea to design and to operate when something's wrong.
[00:05:12 - 00:05:17] I mean, that absolutely applies to your robot co-opters as well.
[00:05:17 - 00:05:18] Things will go wrong.
[00:05:18 - 00:05:20] You look at the videos of previous years.
[00:05:20 - 00:05:26] Things go wrong. Probably the most common thing I heard students say last year,
[00:05:26 - 00:05:31] during that competition was, it's not done that before.
[00:05:31 - 00:05:35] One of the teams of robots started going backwards during the competition.
[00:05:35 - 00:05:40] And they're like, there's nothing in the program that makes it go backwards.
[00:05:40 - 00:05:42] So it should happens.
[00:05:42 - 00:05:49] And so you need to design your system to be tolerant to things that are unexpected.
[00:05:49 - 00:05:53] And so to some extent, we're talking about the backgrounds of that
[00:05:53 - 00:05:56] and these next couple of lectures.
[00:05:56 - 00:06:02] If you guys are designing stuff for a light-long flying robot and elevator and stuff last year,
[00:06:02 - 00:06:07] if you had to pin the ability issues, you know, it went wrong.
[00:06:07 - 00:06:09] What didn't go wrong?
[00:06:09 - 00:06:13] Damage.
[00:06:13 - 00:06:15] Oh, damage.
[00:06:15 - 00:06:18] Yeah.
[00:06:18 - 00:06:19] For the elevator.
[00:06:19 - 00:06:21] Or for the line-filling.
[00:06:21 - 00:06:22] Yeah.
[00:06:22 - 00:06:24] Yes.
[00:06:24 - 00:06:26] Testing helps, right?
[00:06:26 - 00:06:27] And I mean, we'll come to that.
[00:06:27 - 00:06:33] But yeah, hopefully having that experience, you'll kind of relate to some of the stuff.
[00:06:33 - 00:06:35] We're talking about these next couple of lectures.
[00:06:35 - 00:06:40] So I don't get the dependability and analysis and design.
[00:06:40 - 00:06:44] That's across the entire design V, right?
[00:06:44 - 00:06:48] And you can be thinking about the dependability early on,
[00:06:48 - 00:06:50] like when you think about the design requirements.
[00:06:50 - 00:06:54] We can be thinking about it while you're thinking about your architecture
[00:06:54 - 00:06:57] and you're thinking about your sub-modules and you're thinking about your prototype
[00:06:57 - 00:06:59] and your starting to validate things.
[00:06:59 - 00:07:04] This sort of sets across that whole area.
[00:07:04 - 00:07:09] And so, you know, for that, you know, what we're talking about
[00:07:09 - 00:07:10] is design for dependability.
[00:07:10 - 00:07:14] And so we're generally like our systems that we designed to be dependable.
[00:07:14 - 00:07:15] What does that mean?
[00:07:15 - 00:07:30] What is dependability?
[00:07:30 - 00:07:32] I guess to some extent that captures a bit of it.
[00:07:32 - 00:07:33] Yep.
[00:07:33 - 00:07:36] I guess conversely it's not going to do something unexpected.
[00:07:36 - 00:07:41] I suppose rather than a suppose if it's doing the same thing every time that's what you want it to do.
[00:07:41 - 00:07:42] Good.
[00:07:42 - 00:07:47] The converse of that or the corollary that is that it's not going to do something unexpected.
[00:07:47 - 00:07:49] That's sort of hitting in the right direction.
[00:07:49 - 00:07:50] Anything else?
[00:07:50 - 00:07:59] Yeah.
[00:07:59 - 00:08:04] So dependability and reliability are almost synonymous with each other.
[00:08:04 - 00:08:05] Yeah.
[00:08:05 - 00:08:06] So it's reliable.
[00:08:06 - 00:08:09] Which means kind of doing what you'd expect it to do.
[00:08:09 - 00:08:11] Anything else?
[00:08:11 - 00:08:20] Anything about the levels of how much it does in it?
[00:08:20 - 00:08:22] We've got a definition here.
[00:08:22 - 00:08:26] There's not necessarily one definition, but this one is that the system does not
[00:08:26 - 00:08:29] fail more often or more severely than as acceptable.
[00:08:29 - 00:08:32] Now, you note that I've highlighted some waffley words.
[00:08:32 - 00:08:37] What does more often or more severely or acceptable mean?
[00:08:37 - 00:08:40] And that's kind of fine for a general definition.
[00:08:40 - 00:08:45] But in your requirements for a system, you certainly wouldn't put those words there.
[00:08:45 - 00:08:54] You would have to talk with your stakeholders, talk with the users, the clients, the maintenance people,
[00:08:54 - 00:08:58] and you would have to put values around those.
[00:08:58 - 00:09:03] What is more often or more severely than acceptable?
[00:09:03 - 00:09:06] So what I mean for a robot cup, what would you say?
[00:09:06 - 00:09:09] In terms of dependability, what would you want to say?
[00:09:09 - 00:09:14] What are the values for these sorts of things?
[00:09:14 - 00:09:17] Very good mind that these are things you're going to need about a test.
[00:09:17 - 00:09:23] It's all well and good saying our robot is not going to be able to never fail.
[00:09:23 - 00:09:26] Because good luck.
[00:09:26 - 00:09:37] Secondly, you want values or numbers that you can somehow test or quantify while you're sort of designing a prototype in your system.
[00:09:37 - 00:09:44] So what sort of things might, I mean, there's no right answer wrong answer to this, but what might be reasonable for a robot cup?
[00:09:44 - 00:09:46] Something like that. Which you can test, right?
[00:09:46 - 00:09:49] You can run that in the arena in the weeks leading up to it.
[00:09:49 - 00:10:02] You can do 50 tests and count how many times it picks it up.
[00:10:02 - 00:10:03] Yeah.
[00:10:03 - 00:10:11] So I guess in that you're assuming that obviously not actually home version or not picking up weights are the failures, right?
[00:10:11 - 00:10:18] What else? What other sort of failures do we see in all things that make the robot cup robots not dependable?
[00:10:18 - 00:10:20] Basically I saw last year.
[00:10:20 - 00:10:30] Yes, so you might have some sub-module failures, for example.
[00:10:30 - 00:10:38] And I know a few things last year, like the arranged sensors on one side would get knocked or the connectors would get pulled.
[00:10:38 - 00:10:41] And so then the robot was in the arena.
[00:10:41 - 00:10:47] And it's not getting information from one side of the robot.
[00:10:47 - 00:10:53] Do they have code that allowed that to be detected and compensated for or not?
[00:10:53 - 00:10:59] So the other mechanical phase too, what happens if you track four off?
[00:10:59 - 00:11:03] That happens relatively regularly.
[00:11:03 - 00:11:12] What happens? Well, I mean, I suppose if your battery connector comes off, then you know there's nothing much you can do about that, right?
[00:11:12 - 00:11:20] And thinking about robot cup, think about when you're putting together your requirements for that,
[00:11:20 - 00:11:29] also think about dependability type requirements and ones that are kind of sensible and testable and try and put those in.
[00:11:29 - 00:11:38] So that's what is dependability, but what then prevents us from achieving this dependability?
[00:11:38 - 00:11:55] What's the chain of events, if you like, that causes things to not work as they should basically to fail by the severely or often something to the defense?
[00:11:55 - 00:12:02] Yes, so there's a stochastic or a probabilistic element to it, right?
[00:12:02 - 00:12:14] So you're not fully being aware and therefore being able to model or think about those problems and what might fail.
[00:12:14 - 00:12:20] And then there are lazier- but systems or mechanisms in place to cope with things when they do fail.
[00:12:20 - 00:12:28] There's more deterministic, what's the chain of events?
[00:12:28 - 00:12:36] So if we've got a failure and we've got, I don't know, the track four and a half, what lead to that track four or more?
[00:12:36 - 00:12:41] Or what, like what may have led to that track four and a half, for example?
[00:12:41 - 00:12:53] So it could be a tangent with another robot, it could be something I try to turn against the wall or another obstacle.
[00:12:53 - 00:12:59] It might be the head poorly designed wheels that had like a taper or something.
[00:12:59 - 00:13:01] So, yeah.
[00:13:01 - 00:13:06] And so with this, there's a general chain of events that's accepted.
[00:13:06 - 00:13:09] We have faults and we have errors and we have failures.
[00:13:09 - 00:13:17] So these are the things that we note. So if we start there for a start, that's an event that occurs when externally observable behaviour of the system deviates from a specification.
[00:13:17 - 00:13:24] So in the case of your tracks, you expect the track system to stay on and that provides low commotion.
[00:13:24 - 00:13:30] If there's an externally observable behaviour that deviates from that, like a track falls off, that's a failure.
[00:13:30 - 00:13:32] But what led to that failure is an error.
[00:13:32 - 00:13:40] And that's an internal discrepancy between the intended and the actual behaviour that may lead to that failure if it's not contained.
[00:13:40 - 00:13:49] So, I mean, to some extent, you know, if you're saying your robot had a collision with another robot, sometimes that's out of your control, right?
[00:13:49 - 00:13:52] It may, that other robot might have come from behind.
[00:13:52 - 00:13:54] We've got no senses and there's nothing that you can do about it.
[00:13:54 - 00:14:01] But it may have been that your robot wasn't navigating away from obstacles very well and that sort of drove itself into something.
[00:14:01 - 00:14:05] But what leads to those errors and that error is caused by a fault.
[00:14:05 - 00:14:09] So a fault's a flaw in the system that may lead to an error if it's activated.
[00:14:09 - 00:14:15] It might not. You might have flaws in your system that never eventually, and so nothing happens.
[00:14:15 - 00:14:17] But if they do, that leads to an error.
[00:14:17 - 00:14:21] An error in itself is not necessarily bad.
[00:14:21 - 00:14:23] It's only bad when that becomes a failure.
[00:14:23 - 00:14:27] And so we've got this chain of events, a faults of errors and failures.
[00:14:27 - 00:14:34] And so what prevents us from achieving that is basically faults.
[00:14:34 - 00:14:35] That's what we want to avoid.
[00:14:35 - 00:14:38] So we've got a fault on this PCB.
[00:14:38 - 00:14:42] There's a sort of bridge between two of those pens.
[00:14:42 - 00:14:50] That might be, like, if win, win might that not be a fault.
[00:14:50 - 00:14:55] Yeah. So if those are both ground pens, who keeps?
[00:14:55 - 00:15:01] Well, if they're the same ground pen, you know, if we don't have separate and long digital ground or something like that.
[00:15:01 - 00:15:06] But if they're just standard ground pens or they're non-connected or something like that,
[00:15:06 - 00:15:08] this is not necessarily going to be an issue.
[00:15:08 - 00:15:13] If it turns out that that's ground and VCC, that might be a basic issue.
[00:15:13 - 00:15:21] And so that's the fault then that relates to is there an error and that error may cause the failure.
[00:15:21 - 00:15:28] And so we've got to be, while we're thinking about the pinability, we want to start thinking about it in terms of, you know, what are the faults?
[00:15:28 - 00:15:31] What are the errors and what are the failures?
[00:15:31 - 00:15:35] So I have, there's a couple of examples here.
[00:15:35 - 00:15:39] Do you all know about the, to have on comment?
[00:15:39 - 00:15:43] It was the first commercial jet airliner.
[00:15:43 - 00:15:48] It was designed in the late 1940s and the first ones.
[00:15:48 - 00:15:52] First ones were flying commercially in 1954.
[00:15:52 - 00:15:57] So I had four to have a guest, two-line engines.
[00:15:57 - 00:16:03] What the fault was, there's a myth around it that it's because it had square windows.
[00:16:03 - 00:16:07] And that caused stress concentrations.
[00:16:07 - 00:16:09] And that's not quite true.
[00:16:09 - 00:16:10] They weren't perfectly square.
[00:16:10 - 00:16:11] They were around in the corners.
[00:16:11 - 00:16:14] Another pressurized airline has also had square windows.
[00:16:14 - 00:16:18] That wasn't that, I think the word window got used in a report.
[00:16:18 - 00:16:23] It wasn't the passenger windows, but there were window cutouts for that would have made direction finders.
[00:16:23 - 00:16:26] And that's where the stress concentrations occur.
[00:16:26 - 00:16:29] But that, and in itself wasn't the problem.
[00:16:29 - 00:16:36] The problem was that the engines were a bit gutless and therefore to not stress them too much, they made it quite light structurally.
[00:16:36 - 00:16:44] So I had it in very thin skin and very thin, I guess structural members were there to cope with that.
[00:16:44 - 00:16:52] And therefore the skin couldn't properly distribute the stress and the fuselage.
[00:16:52 - 00:16:55] Which then led to stress concentrations.
[00:16:55 - 00:16:58] And that's these little cutouts.
[00:16:58 - 00:17:00] You can't see.
[00:17:00 - 00:17:06] I don't know if I have to get a little, the point I hold on.
[00:17:06 - 00:17:10] These little cutouts here were the ADF cutouts.
[00:17:10 - 00:17:11] So what a matte direction find the cutouts.
[00:17:11 - 00:17:15] And that's where the stress concentrations occurred because the skin was so thin.
[00:17:15 - 00:17:20] So those cracks propagated due to fatigue because of pressurization.
[00:17:20 - 00:17:23] So it was pressurized, pressurized, pressurized.
[00:17:23 - 00:17:28] One of them went crushed initially in flight.
[00:17:28 - 00:17:32] And at the time, they did a bit of an investigation.
[00:17:32 - 00:17:35] No one really knew they thought it could have been sabotaged.
[00:17:35 - 00:17:38] I mean something, they kind of wrote that off.
[00:17:38 - 00:17:41] And then shortly afterwards another one went down at which point they were,
[00:17:41 - 00:17:47] the airworthiness certificate was cancelled and they did a lot more investigation to figure out this.
[00:17:47 - 00:17:50] But the folks was that the skin was too thin.
[00:17:50 - 00:17:52] But they had done a bunch of testing.
[00:17:52 - 00:17:55] It worked and they flew for a thousand hours or whatever.
[00:17:55 - 00:17:57] And it was fine.
[00:17:57 - 00:18:01] But during that time, there were cracks propagating.
[00:18:01 - 00:18:04] And no one necessarily knew to those.
[00:18:04 - 00:18:07] And those were the, you know, that was the internal discrepancy.
[00:18:07 - 00:18:10] Those in and of themselves didn't cause the failure.
[00:18:10 - 00:18:13] When the crack got too large, basically the fuselage blow apart in flight.
[00:18:13 - 00:18:20] And obviously that was the failure that killed a number of people.
[00:18:20 - 00:18:26] Another, I've got this written down because I can never remember the long chain of events.
[00:18:26 - 00:18:32] But the first Ariane 5 rocket launch also in PS8.
[00:18:32 - 00:18:35] And that was an expensive wopsie bezie.
[00:18:35 - 00:18:41] And brief, the fault was that there was a software fault alone overflow from 64 to 16.
[00:18:41 - 00:18:44] During the 64 bits of 16 bit conversion.
[00:18:44 - 00:18:47] There was no flag overflow.
[00:18:47 - 00:18:51] The era was that then the guidance computers shut down.
[00:18:51 - 00:18:55] The head redundancy, so they had two identical guidance computers.
[00:18:55 - 00:18:57] And we'll talk about this later.
[00:18:57 - 00:18:58] Like they've got redundancy.
[00:18:58 - 00:19:00] You can have two identical ones running identical software.
[00:19:00 - 00:19:02] Then you test them and you know that they work.
[00:19:02 - 00:19:08] I suppose if you've got mechanical or that sort of failure with a guidance computer having that second one's good.
[00:19:08 - 00:19:13] If you have, let's say software type failure in the identical, you shut down one.
[00:19:13 - 00:19:14] The other one gets the same signal.
[00:19:14 - 00:19:15] It also shuts down.
[00:19:15 - 00:19:18] It's largely what occurred in this instance.
[00:19:18 - 00:19:25] And they sent an era code to the main computer which was mistaken for guidance information.
[00:19:25 - 00:19:29] And then the rocket tried to make a violent change in course.
[00:19:29 - 00:19:34] Basically there was a large area of dynamic forces and the activator that would have made a destroyed sequence.
[00:19:34 - 00:19:40] But for that was $500 million and four satellites of what's.
[00:19:40 - 00:19:47] But the sequence, and this is where it's interesting, the early part of the area and files trajectory differs from the area and for that it was based on.
[00:19:47 - 00:19:51] And it results in a considerably higher horizontal velocity.
[00:19:51 - 00:19:59] The 64-bit floating number was changed to a 16-bit signed integer in the internal reference system.
[00:19:59 - 00:20:05] And it overflowed due to that horizontal velocity component being higher than normal.
[00:20:05 - 00:20:08] And that conversion wasn't protected.
[00:20:08 - 00:20:11] Although most of the other conversions were.
[00:20:11 - 00:20:15] Their overflow caused an operating era resulting in a software exception.
[00:20:15 - 00:20:19] Due to the exception the inertial system sent a diagnostic code to the onboard computer.
[00:20:19 - 00:20:30] And it was misinterpreted as flight data and the onboard computer thought that the rocket thought that the rocket had made a turn and it tried to correct hard for a turn that didn't exist.
[00:20:30 - 00:20:33] And then that was full nozzle deflection on the solid boosters.
[00:20:33 - 00:20:41] They didn't separate it from the main stage and the rocket self-destructed due to its safety mechanism of the onboard.
[00:20:41 - 00:20:45] The backup inertial reference system was down for exactly the same reason.
[00:20:45 - 00:20:50] But the interesting thing was the software module in which the overflow occurred or was computed.
[00:20:50 - 00:20:54] The computer meaningful results only before liftoff as soon as the launcher lifts off.
[00:20:54 - 00:20:57] That function didn't serve any purposes anymore.
[00:20:57 - 00:21:06] However, it had been chosen long ago and Aaron fought a leave it running for the first 40 seconds of flight as a special feature.
[00:21:06 - 00:21:12] That meant to make it easy to restart the system and the event of a brief hold during countdown.
[00:21:12 - 00:21:20] That whole chain of events that caused that self-destruction occurred at 36.7 seconds.
[00:21:20 - 00:21:23] So, it's software that should never have been running.
[00:21:23 - 00:21:28] There was a failure to protect from those overflows.
[00:21:28 - 00:21:31] It was basically just a chain of events.
[00:21:31 - 00:21:33] But it comes down to these faults.
[00:21:33 - 00:21:36] There's a number of faults in the software.
[00:21:36 - 00:21:38] They lead to errors.
[00:21:38 - 00:21:42] They're head redundant systems, but they both shut down for the same reason.
[00:21:42 - 00:21:48] And then obviously that caused a really expensive failure of the first time in five launch.
[00:21:48 - 00:21:51] What can we take from this?
[00:21:51 - 00:22:03] And the previous one as well.
[00:22:03 - 00:22:08] Presumably, these are good engineers working on this system, right?
[00:22:08 - 00:22:10] So, even good engineers fuck up.
[00:22:10 - 00:22:11] That's what I take from it.
[00:22:11 - 00:22:15] Like, you want to try and avoid it, but it's really hard with unforeseen,
[00:22:15 - 00:22:17] and particularly with complicated systems.
[00:22:17 - 00:22:19] That rocker is really complicated.
[00:22:19 - 00:22:20] There's a lot going on.
[00:22:20 - 00:22:25] There's probably millions of lines of code and everything else that goes on with it.
[00:22:25 - 00:22:30] And it's really hard to make sure that you've got every base covered.
[00:22:30 - 00:22:34] And so, you've got to do your best to think through these sorts of things.
[00:22:34 - 00:22:39] Sometimes you'll have measures put in there to sort of head off potential problems,
[00:22:39 - 00:22:42] but they and themselves can end up causing potential problems.
[00:22:42 - 00:22:47] That's probably why I think, you know, when you did hazard analysis in in JL 101,
[00:22:47 - 00:22:52] I don't know if I forget how far it goes through, but if you maybe a designer system,
[00:22:52 - 00:22:58] and then you put a guard on that system, right, to prevent any, maybe a person jumping off their fingers.
[00:22:58 - 00:23:01] Then you've got to redo that hazard analysis with the guard in there,
[00:23:01 - 00:23:06] because that may have introduced additional hazards that weren't taken into account, right?
[00:23:06 - 00:23:09] Same sort of thing with this design.
[00:23:09 - 00:23:13] It's hard to predict, but you've got to do your best,
[00:23:13 - 00:23:18] but also think that sometimes the systems you're putting into place may end up,
[00:23:18 - 00:23:21] you know, also causing problems.
[00:23:21 - 00:23:26] But, yeah, obviously it'd be great if we can design systems that didn't have issues,
[00:23:26 - 00:23:29] that as you learn to run robo-cut your robots will probably have issues,
[00:23:29 - 00:23:31] and that's just part of the learning.
[00:23:31 - 00:23:33] You'll come up better for it.
[00:23:33 - 00:23:35] It'll build character.
[00:23:35 - 00:23:43] So, there are four ways that are generally recognized to prevent failures.
[00:23:43 - 00:23:49] There's fault prevention, so that makes sure that there's making sure that there aren't faults in the first place.
[00:23:49 - 00:23:51] And that's kind of from a design point of view, right?
[00:23:51 - 00:23:54] You do your best to make sure there aren't faults.
[00:23:54 - 00:23:57] Then there's fault removal, so that's things like inspection quality,
[00:23:57 - 00:24:04] quality assurance, testing, these sorts of things to make sure that they don't actually get out to the customer.
[00:24:04 - 00:24:06] Customers and so on.
[00:24:06 - 00:24:10] Then there's fault tolerance, so you have things like redundancy in error correction and stuff,
[00:24:10 - 00:24:20] so that if a fault occurs, the system continues to operate in a way that allows it to perhaps do what it's supposed to do.
[00:24:20 - 00:24:24] And then there's fault forecasting, which is sort of, it relates back to these,
[00:24:24 - 00:24:29] like trying to predict and mitigate any of these faults.
[00:24:29 - 00:24:37] But looking at there, what's the common thing about those in achieving the capability and preventing failures?
[00:24:37 - 00:24:55] Yeah, it's all faults.
[00:24:55 - 00:24:58] To prevent failures, we're trying to prevent faults.
[00:24:58 - 00:25:03] We don't, you're not trying to prevent the actual failure that's looking and ambulance at the bottom of the cliff.
[00:25:03 - 00:25:07] We're trying to prevent the faults that lead to the errors that lead to the failures.
[00:25:07 - 00:25:14] Right, so it's fault tolerance, it's fault removal, it's fault prevention, and that prevents those failures from occurring.
[00:25:14 - 00:25:23] And so, classical, sort of hardware engineering for the penability focuses on ensuring defect-free manufacture.
[00:25:23 - 00:25:29] So, fault prevention, providing a QA net to catch defective hardware before it reaches the customer,
[00:25:29 - 00:25:36] so that's the fault removal, and designing for random hardware failures or weir, and that's your fault tolerance.
[00:25:36 - 00:25:41] And then faults are failures due to ruin material defects, or essentially impossible to predict deterministically,
[00:25:41 - 00:25:44] because that's a probabilistic process.
[00:25:44 - 00:25:52] Right, and so, actually, probability factors into a lot of us, and so we'll just talk a little bit about sort of some of the terms,
[00:25:52 - 00:25:56] in terms of probability that are used within dependability.
[00:25:56 - 00:26:01] So, a couple of key ideas.
[00:26:01 - 00:26:11] I used you to wear and tear or material defects, assume to occur continuously and independently at a constant rate.
[00:26:11 - 00:26:15] It's a convenient assumption, and it kind of works reasonably well.
[00:26:15 - 00:26:25] But what that means, you know, is continuously as they just, it's not discrete, it's not our one at our two, at our three, for example.
[00:26:25 - 00:26:37] It's just a continuous spectrum of time, and independently means if part A fails, that doesn't have any impact on the probability of part B failing, for example.
[00:26:37 - 00:26:40] And then we've got this constant average rate.
[00:26:40 - 00:26:50] So, along the bottom, we've got time, up the side, we've got a number of failures, and so you can see that's approximating a constant average rate that diagonal on.
[00:26:50 - 00:26:57] And this type of failure rate is called a song process.
[00:26:57 - 00:27:06] Now, given that, so you have the failure rate, so that's the expected number of component failures per unit time.
[00:27:06 - 00:27:12] And that's just the gradient of that person process there.
[00:27:12 - 00:27:14] And that's something you could measure.
[00:27:14 - 00:27:25] You could have a whole lot of, if you're manufacturing something, you can have a whole lot of those, and you run them, and you count basically a technique when they fail, and you can build up that curve.
[00:27:25 - 00:27:31] There's another term that comes up quite a lot, so that's the meantime before failure.
[00:27:31 - 00:27:36] So, that's the average amount of time that passes before a component fails.
[00:27:36 - 00:27:40] So, the failure rate, a bit gradient is gamma.
[00:27:40 - 00:27:44] So, it's empty BF, it's just one over gamma, so it's reciprocal of gamma.
[00:27:44 - 00:27:46] Experimentally, you can determine that.
[00:27:46 - 00:27:52] You've got the number of hours the system is in use, the number of failures, and you divide one into the other.
[00:27:52 - 00:27:59] And another term, the often come into contact with us failures in time.
[00:27:59 - 00:28:08] So, it's typically those specify the amount of time, but it's generally like a billion hours, so they'll say 1,000 components fail in a billion hours.
[00:28:08 - 00:28:13] And so, it gives you a sort of expected period of time.
[00:28:13 - 00:28:18] So, then we have reliability.
[00:28:18 - 00:28:27] And I think this is why I call these pictures the Pingability, because reliability has got a specific meaning within this area.
[00:28:27 - 00:28:34] So, reliability, R of T, is a probability that a component of system is still functioning at time T.
[00:28:34 - 00:28:41] So, you might have the reliability at, I don't know, let's say 75 years or something up there.
[00:28:41 - 00:28:49] And that's the number, so you look at that and you'd say that there's 50% chance that after 75 years the system is still operating.
[00:28:49 - 00:29:03] But again, that's quite nice, because the reliability is governed by that gradient, that process on process, Lambda, which obviously you can capture experimentally by measuring the mean time between failures.
[00:29:03 - 00:29:08] There's another experimentally derived measure called availability.
[00:29:08 - 00:29:15] So, availability is based on mean time between failure, but also the mean time to repair.
[00:29:15 - 00:29:24] So, if you've got a failed system, so you've got your robot cup, robot, and maybe you do a bunch of testing on it.
[00:29:24 - 00:29:29] And you know that on average it takes you one hour to repair failure.
[00:29:29 - 00:29:34] And you've done, you had 10 failures.
[00:29:34 - 00:29:38] Then the mean time to repair is one divided by 10, right?
[00:29:38 - 00:29:39] That's a point one.
[00:29:39 - 00:29:49] You might have experimentally determined that the mean time before failure for your robot cup robot is, I don't know, two hours, for example.
[00:29:49 - 00:29:55] And don't laugh if you think that's low, like mobile robots have typically got a really high failure rate.
[00:29:55 - 00:29:57] Not just robot cup ones, but commercial ones as well.
[00:29:57 - 00:30:02] And so, then you've got this availability, which is the mean time between failures.
[00:30:02 - 00:30:07] And so, the value is divided by mean time before failures plus the time to repair.
[00:30:07 - 00:30:10] Each time there is a failure and turned into a percent.
[00:30:10 - 00:30:14] And so, that gives you an idea about how available that system is.
[00:30:14 - 00:30:20] So, what's the percentage of the time that that is working and available for use?
[00:30:20 - 00:30:28] Now, sometimes you see occasionally on the news it comes up.
[00:30:28 - 00:30:39] Like, I've seen it for, I think it's like F-35 and fighter that's used by the US and Australia that we've got a really crap availability.
[00:30:39 - 00:30:47] Something like 50% because either they fail a lot or they take a long time to repair when they do fail, right?
[00:30:47 - 00:30:57] And so, you know, these are terms that are used with an injury, but let's start to creep into, I guess, more common usage and stuff.
[00:30:57 - 00:31:00] Like, I can then use with that.
[00:31:00 - 00:31:07] Does this make sense?
[00:31:07 - 00:31:09] Cool.
[00:31:09 - 00:31:15] All right, so, looking at component reliability, you think, well, where do I get these numbers from?
[00:31:15 - 00:31:20] These days, individual components reliability is getting really, really high.
[00:31:20 - 00:31:21] Here's some examples.
[00:31:21 - 00:31:26] Like, if you look up individual components, you can often get reliability data for it.
[00:31:26 - 00:31:31] So, the little ultrasound sensors that you get with a robot cup kit.
[00:31:31 - 00:31:35] And else, other places are the max products, ultrasound sensors.
[00:31:35 - 00:31:41] The meantime between failure at, as long as it's running below 45 degrees,
[00:31:41 - 00:31:44] is nearly 233,000 hours.
[00:31:44 - 00:31:47] It's pretty good.
[00:31:47 - 00:31:55] If you just take a, your BC-5 will see them, which is a pretty old, crappy bipolar junction transistor.
[00:31:55 - 00:32:01] The meantime between, oh, before failures for there is 1.3 billion hours.
[00:32:01 - 00:32:04] Right, individual components are really good.
[00:32:04 - 00:32:14] The problem is not so much the individual component failures, but it's the aspects that haven't changed.
[00:32:14 - 00:32:21] So, environmental, operational conditions, things like it's hot, it's dusty, it's vibration, ESD.
[00:32:21 - 00:32:30] Like, most of the time, like with the electricity discharge damage, the system still works for a while,
[00:32:30 - 00:32:33] but it fails a lot quicker than you expect.
[00:32:33 - 00:32:39] It fails in ways that it's not like the system, although the component will, I see, just stops working.
[00:32:39 - 00:32:41] It stops doing some things.
[00:32:41 - 00:32:44] And it makes it really hard to diagnose.
[00:32:44 - 00:32:46] It's just misbehaving.
[00:32:46 - 00:32:51] So, things are operational conditions cause failures.
[00:32:51 - 00:32:57] Human factors, so design areas, software bugs, operational mistakes, or slips, slippers.
[00:32:57 - 00:32:59] They cause failures.
[00:32:59 - 00:33:04] And another big place where we see failures is the connections or interfaces between components.
[00:33:04 - 00:33:07] So, those might be like physical connectors, like wires.
[00:33:07 - 00:33:12] It might be solder joints, you know, that would dry solder joints, or the solder joints,
[00:33:12 - 00:33:14] and it's an vibrating environment.
[00:33:14 - 00:33:22] The solder joints ends up cracking, and it's intermittent at that point, sometimes it works, sometimes it doesn't.
[00:33:22 - 00:33:25] So, what do we think?
[00:33:25 - 00:33:31] Does that line up with your experience?
[00:33:31 - 00:33:39] So, the final year project, well, actually, this is the third year in a row that I've supervised one of the UC Aerospace-Fonia projects.
[00:33:39 - 00:33:46] Last year, this year is the, this towards the Space Plane thing, who were.
[00:33:46 - 00:33:50] Last year it was the height one of the, the Megatronic-Siderl Hybrid Rocket Engine.
[00:33:50 - 00:33:57] And then 2024, it was the Space Port attempt for the, the rocket.
[00:33:57 - 00:34:02] Now, part of that, that's, so the year before in 2023,
[00:34:02 - 00:34:05] I had one that Space Sport competition.
[00:34:05 - 00:34:08] And it was sheer luck, like they just got lucky.
[00:34:08 - 00:34:12] And the e-brick system that was supposed to work, it was supposed to deploy the e-brick.
[00:34:12 - 00:34:19] So, we're supposed to log all the data as it flew, and nothing was logged in the e-brick didn't activate.
[00:34:19 - 00:34:23] They just got lucky that happened to get closest to the mark.
[00:34:23 - 00:34:29] So, they went into 2024 with the idea of reusing the e-brick system.
[00:34:29 - 00:34:35] So, I don't know if you know, if it's a 30K, so there's a mark, a 30,000 feet above the launch site,
[00:34:35 - 00:34:38] and you had to get as close to that as you could.
[00:34:38 - 00:34:42] And that's, that's how you, effectively, got most points,
[00:34:42 - 00:34:44] as all the other aspects to it too.
[00:34:44 - 00:34:49] So, the team had e-bricks in it, so they would be, obviously monitoring how the rockets performing,
[00:34:49 - 00:34:52] and then they would have a model of the rocket, and they would think,
[00:34:52 - 00:34:56] right, it's time to deploy, start slowing it down to the head, these e-bricks that came out the side,
[00:34:56 - 00:35:00] and they were supposed to slide down and make sure it got close to 30,000 feet.
[00:35:00 - 00:35:04] And it was a nice design, I like,
[00:35:04 - 00:35:06] testing and stuff, the e-bricks.
[00:35:06 - 00:35:10] Well, and testing on the beach, the e-bricks worked well.
[00:35:10 - 00:35:14] And testing, when they did a launch, there was something wrong,
[00:35:14 - 00:35:16] and the e-bricks didn't deploy, but all that fine,
[00:35:16 - 00:35:20] we kind of fixed that problem in 2023.
[00:35:20 - 00:35:22] But they didn't work in the competition.
[00:35:22 - 00:35:26] And so, in 2020, 2024, though, look at this,
[00:35:26 - 00:35:30] they didn't have any data because it didn't log, and the e-bricks didn't deploy.
[00:35:30 - 00:35:33] So, they did a bunch of testing, and related to that.
[00:35:33 - 00:35:36] So, there's some vibration testing of the printed circuit board,
[00:35:36 - 00:35:40] the servo and the battery, and they were mounted on a shake table.
[00:35:40 - 00:35:45] The PCB was subjected to a sweep of frequencies from 10 hertz to the 5,000 hertz,
[00:35:45 - 00:35:48] over a period of 500 seconds, and they did seven tests of that,
[00:35:48 - 00:35:50] with that 2023 board.
[00:35:50 - 00:35:56] Four failed due to the battery connector losing connection due to the vibration,
[00:35:56 - 00:35:58] cutting the power of the board.
[00:35:58 - 00:36:02] Two tests had the SD card valve, so they're logging on to an SD card,
[00:36:02 - 00:36:05] but as you've probably used in the SD card, you push it in,
[00:36:05 - 00:36:12] there's little spring connectors that touch to the pads on the SD card.
[00:36:12 - 00:36:18] And obviously, during the vibration, those started to disconnect,
[00:36:18 - 00:36:22] but they were trying to simulate launch for those robots,
[00:36:22 - 00:36:25] for those rockets, the rockets experiencing 28G.
[00:36:25 - 00:36:29] So, it's a fairly violent launch, and so,
[00:36:29 - 00:36:32] these, and the rocket will be vibrating, because it's a solid rocket motor,
[00:36:32 - 00:36:35] it doesn't burn perfectly, this vibration occurring.
[00:36:35 - 00:36:39] And so, of the 7 tests, four failed due to a battery connector
[00:36:39 - 00:36:43] with losing power, two tests had the SD card failed to log,
[00:36:43 - 00:36:46] and one test had no failure.
[00:36:46 - 00:36:51] And so, they also did some drop testing of the PCBs and the servos and the battery.
[00:36:51 - 00:36:56] They built a custom drop tower, and they'll drop, dropping it.
[00:36:56 - 00:37:01] And they incrementally, just depending on how high they dropped it from,
[00:37:01 - 00:37:06] they could increase the G of the deceleration from 20G up to 100G.
[00:37:06 - 00:37:11] And the results from those tests showed that the PCB was able to function and log it up to 75G,
[00:37:11 - 00:37:14] in terms of a single deceleration event.
[00:37:14 - 00:37:18] And impact 81G caused the PCB to stop logging,
[00:37:18 - 00:37:21] and that was suspected that the power connector had failed on the PCB,
[00:37:21 - 00:37:23] causing it not to power on.
[00:37:23 - 00:37:28] So, basically, most of those failures were connection failures,
[00:37:28 - 00:37:34] due to acceleration, due to the vibration.
[00:37:34 - 00:37:38] The other thing that they'd suspected, but they weren't sure about is a crystal oscillator,
[00:37:38 - 00:37:40] so you never got clocks, right?
[00:37:40 - 00:37:41] The crystal oscillators.
[00:37:41 - 00:37:46] A crystal oscillator, it's piece of quartz that looks,
[00:37:46 - 00:37:48] it's like a little square of quartz, and it's got two legs,
[00:37:48 - 00:37:50] and that physically vibrates.
[00:37:50 - 00:37:56] But when that's accelerating at 28G, it certainly doesn't behave the way that it was expected to behave.
[00:37:56 - 00:37:58] They thought that might have been the case.
[00:37:58 - 00:38:02] You can buy high G crystal oscillators for these type of applications,
[00:38:02 - 00:38:04] but they were quite expensive.
[00:38:04 - 00:38:07] But they did buy a high G one, because they weren't sure if that was the problem,
[00:38:07 - 00:38:12] although I think it's turned out that it was more of a solid vibration.
[00:38:12 - 00:38:19] So, going into 2024, they basically had a lot more focus on making sure
[00:38:19 - 00:38:22] those connectors are all good.
[00:38:22 - 00:38:26] They managed to get the logging for 2024,
[00:38:26 - 00:38:31] but the airbracks still didn't work, because they were the separate software-ish.
[00:38:31 - 00:38:37] And they could have fixed it, but they got more points if they launched on the first day.
[00:38:37 - 00:38:38] You've got additional points.
[00:38:38 - 00:38:42] Then FUCED will take a day or fix the software-ish and will launch tomorrow.
[00:38:42 - 00:38:48] And so, they did that, and they got lucky again, and got the closest to the 30,000-fat again,
[00:38:48 - 00:38:52] and won it in 2024 without those airbracks working.
[00:38:52 - 00:38:57] So, it just goes to show connectors are problems.
[00:38:57 - 00:38:59] Sometimes you also just get lucky.
[00:38:59 - 00:39:06] But the takeaway from this is individual components are really good.
[00:39:06 - 00:39:11] Connectors are still one of the biggest potential issues
[00:39:11 - 00:39:16] where you might have problems, particularly in environment where there's vibration,
[00:39:16 - 00:39:19] and stuff like that.
[00:39:19 - 00:39:22] Do you have any questions about that?
[00:39:22 - 00:39:25] Often thought we should probably have a course in megatronics about connectors.
[00:39:25 - 00:39:29] It doesn't sound the most exciting, but once you get into designing projects,
[00:39:29 - 00:39:32] you've ever gone cross-watch connectors or we need for this.
[00:39:32 - 00:39:37] There's just millions of different ones, which ones best for this and the other.
[00:39:37 - 00:39:41] And I think it's something useful, but especially as an executive,
[00:39:41 - 00:39:45] I don't think anyone had to choose something that was called connectors.
[00:39:45 - 00:39:49] Unless you'd have experience here like, oh, those are tricky, I guess.
[00:39:49 - 00:39:53] Anyway, so that's hardware, right?
[00:39:53 - 00:39:56] Software is clearly different from hardware,
[00:39:56 - 00:40:01] because you've got no physical material to fail or to wear out essentially.
[00:40:01 - 00:40:05] The manufacturing process is repeatable and automated, right?
[00:40:05 - 00:40:06] You've got your compilers.
[00:40:06 - 00:40:12] And software's faults and failures then always come down to being designed floors.
[00:40:12 - 00:40:17] Obviously, that happened in 2024 with Facebook, because they had a design floor.
[00:40:17 - 00:40:25] And various studies are showing that up until the up to 90% of software fail is a result of errors and interfaces,
[00:40:25 - 00:40:31] so between different modules of the software or in the requirements.
[00:40:31 - 00:40:37] So in the ARIN 5 example, obviously that was a software failure.
[00:40:37 - 00:40:48] I'm guessing maybe software was reused from ARIN 4, but the requirements didn't have something to the effective.
[00:40:48 - 00:40:53] It needs to be able to cope with this horizontal velocity value.
[00:40:53 - 00:40:56] With interfaces, there's the Mars Climate Orbiter example.
[00:40:56 - 00:41:01] So this is another example of good engineers making mistakes.
[00:41:01 - 00:41:08] So I don't know, again, if you were aware of this one, but there was a,
[00:41:08 - 00:41:12] the board investigated this afterwards.
[00:41:12 - 00:41:16] And I forget, was either Lockheed or Boeing was a contractor for it.
[00:41:16 - 00:41:22] So NASA was building part of it, Lockheed or Boeing, one of those two was building another part of it.
[00:41:22 - 00:41:30] Now NASA's requirements specifically say all values are in SI units.
[00:41:30 - 00:41:35] So obviously, because you've got electronic systems or computational systems,
[00:41:35 - 00:41:41] it's just got a number that comes with it needs to be a new site unit.
[00:41:41 - 00:41:46] But Lockheed or Boeing or whoever is manufacturing it,
[00:41:46 - 00:41:49] sped out their numbers for a part of it in imperial units.
[00:41:49 - 00:41:52] NASA took those numbers for the partner connected to that,
[00:41:52 - 00:41:57] and assumed that those were metric units, obviously they're different.
[00:41:57 - 00:42:00] And what that meant that there was a,
[00:42:00 - 00:42:05] that information was critical to the manoeuvre required to place that spacecraft in the proper Mars orbit.
[00:42:05 - 00:42:09] And therefore, it encouraged trajectory correction occurs.
[00:42:09 - 00:42:15] And so you can see here, this, this here was the anticipated trajectory,
[00:42:15 - 00:42:21] and it was supposed to come in at 200 and 26 kilometers above Mars.
[00:42:21 - 00:42:27] The actual trajectory due to the software interface issue had that spacecraft coming in at
[00:42:27 - 00:42:30] 57 kilometers above Mars.
[00:42:30 - 00:42:34] NASA were tracking it, it went round behind Mars, and never came out the other site.
[00:42:34 - 00:42:38] Then you've found it, they assumed it and contacted with the atmosphere,
[00:42:38 - 00:42:46] and it slowed down and crashed into the back of the planet, but it just never came out.
[00:42:46 - 00:42:50] And so again, there's $195 million of whoops.
[00:42:50 - 00:42:57] NASA, I guess, being largely political organisation as it is,
[00:42:57 - 00:43:01] and not wanting to piss off their contractors too much,
[00:43:01 - 00:43:09] found out what it was, explained all of their, and at the end they had a quote that said people sometimes make error.
[00:43:09 - 00:43:12] Yes, they do.
[00:43:12 - 00:43:19] And as I said before, you know, we try not to, but that still happens, right.
[00:43:19 - 00:43:25] And so we try to go through these processes to sort of think through what might happen
[00:43:25 - 00:43:29] and what we can do about it, but sometimes the worst still occurs.
[00:43:29 - 00:43:34] And, you know, things like these space missions are a one-off flake.
[00:43:34 - 00:43:37] It's not letting you go back and have another crack at that as too expensive.
[00:43:37 - 00:43:41] You're as if you're designing, I don't know, a lawnmower or something like that.
[00:43:41 - 00:43:46] You can build it, you can test it, and you can, this being an opportunity to find where these areas are.
[00:43:46 - 00:43:50] Same with your robot.
[00:43:50 - 00:43:58] So how do we kind of do this fault prevention to get your requirements and your specifications,
[00:43:58 - 00:44:01] focus on getting those as right as you can, right.
[00:44:01 - 00:44:04] So if you've got a careful definition of your requirements,
[00:44:04 - 00:44:08] I mean, NASA carefully defined that shit had to be in S.I.U.
[00:44:08 - 00:44:15] I guess on the other side, the contractor needs to read that and take that in.
[00:44:15 - 00:44:22] But, you know, at a high level, your requirements are statements about the problem in the world.
[00:44:22 - 00:44:27] So obviously the changes that you want to see if the system's working.
[00:44:27 - 00:44:31] Then you've got the system that you're designing, so that's the thing that you design that solves that problem,
[00:44:31 - 00:44:32] post in the requirement.
[00:44:32 - 00:44:37] Then you've got the specifications that bridges the gap there between the world and the machine
[00:44:37 - 00:44:44] by describing the phenomena, the interfaces between those two, to design the system
[00:44:44 - 00:44:46] to meet those specifications.
[00:44:46 - 00:44:52] And then we have the assumption that if we meet those specifications, then the requirements will be met.
[00:44:52 - 00:44:59] And so probably the last slide, I think, before we stop for the day.
[00:44:59 - 00:45:02] So here's another yet another example.
[00:45:02 - 00:45:05] And this goes to where I mentioned before.
[00:45:05 - 00:45:08] I did talk about this one, I'd previously, it should be a little bit.
[00:45:08 - 00:45:15] This goes to where the engineers have thought through some situations of scenarios.
[00:45:15 - 00:45:23] And they've tried to prevent those occurring, but that, in itself, has caused another problem.
[00:45:23 - 00:45:29] So with this, as an Eboset through 20, and the header system in there,
[00:45:29 - 00:45:37] so as I mentioned, like a much earlier lecture, you didn't want the pilots accidentally engaging reverse thrust when the plane was still flying.
[00:45:37 - 00:45:42] Obviously, that would be a failure that would cause problems.
[00:45:42 - 00:45:51] And so they had a requirement largely that the aircraft that has touched down can be slowed to a stop before reaching the end of the runway.
[00:45:51 - 00:45:57] And so to ensure that pilots couldn't reverse thrust while it's still flying,
[00:45:57 - 00:46:04] the header check on it said that the wheel speed had to be greater than 133 kilometres per hour.
[00:46:04 - 00:46:13] Or there was 6.3 tonnes of weight on each, so on both of those wheel-o-o-starts before reverse thrust could be engaged.
[00:46:13 - 00:46:20] But that particular flight was coming in with a massive crosswind, and there had been rain on the runway.
[00:46:20 - 00:46:25] So when it touched down, the wheels were hard repaining on the water that was sitting on the runway.
[00:46:25 - 00:46:28] So the wheel speed wasn't meeting that requirement.
[00:46:28 - 00:46:37] And also, there wasn't 6.3 tonnes on each of those main wheel-starts, because it was in a massive crosswind to the bulk of the weight was on one of those wheel-starts,
[00:46:37 - 00:46:39] and there was not a lot of weight on the other.
[00:46:39 - 00:46:43] So when the pilots went to engage reverse thrust, the plane wouldn't let it happen.
[00:46:43 - 00:46:49] And so obviously, later on, down the runway, they could finally do it, but it was too far gone by that point.
[00:46:49 - 00:46:53] We went off into the runway and crashed and burned.
[00:46:53 - 00:46:57] And several people were killed if I remember correctly.
[00:46:57 - 00:47:03] So you can see that the engineers, again, had thought through that system,
[00:47:03 - 00:47:10] and they had managed to stop pilots being able to engage reverse thrust in, in minutes of flight.
[00:47:10 - 00:47:20] But in this particular weird one-off situation, it still caused a problem in a different way.
[00:47:20 - 00:47:24] Anyway, maybe we'll stop for today, and we'll continue next week.
[00:47:24 - 00:47:28] But if you have any questions or anything, feel free to come on up.
[00:47:28 - 00:47:32] Afterwards, I'll go ahead and enjoy the nice Friday before the rain comes.
[00:49:16 - 00:49:20] I'll go ahead and wait for the flight.
[00:49:20 - 00:49:23] How do you know how to do that?
[00:49:23 - 00:49:25] What's that?
[00:49:25 - 00:49:33] This can't be a comeback on four, three, two, eight.
[00:49:33 - 00:49:34] What's that?
[00:49:34 - 00:49:35] That's fine.
[00:49:35 - 00:49:36] It's all helpful.
[00:49:36 - 00:49:37] That's fine.
[00:49:37 - 00:49:39] This is the chance.
[00:49:39 - 00:49:44] Right, three, three, two, three.
[00:49:44 - 00:49:45] What's that?
[00:49:45 - 00:49:48] Do you reference the computer?
[00:49:48 - 00:49:53] The only one time is the one who gets someone to complete the description.
[00:49:53 - 00:49:55] So I think that's what I do.
[00:49:55 - 00:50:00] Do you just repeat the text that I like to do from the lab?
[00:50:00 - 00:50:05] Is it in space company and in reference from the lab, it makes me sense.

# ENMT301-26W Lecture 16 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_16_audio_16k_mono_32k.mp3`
Source audio SHA-256: `5ff5c876d70d8a8a9b8e6f9ddcfb10c0a192098e8d43de6b36f0673c486579b0`
Generated: 2026-06-06T05:33:22.981739+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:05 - 00:00:24] Alright, I assume that everyone left here is for Tron and I have a feeling there's some
[00:00:24 - 00:00:30] way of making this duplicate.
[00:00:30 - 00:00:34] So if you are in the Tron class, if you're up in the back, do you want to just move a bit
[00:00:34 - 00:00:46] forward to these tables? This is a bit of an average spot for lecturing. Maybe I should
[00:00:46 - 00:00:48] just sit down.
[00:00:48 - 00:00:58] Okay, right, I presume everyone has seen the RoboCup teams by this point. Is he or not?
[00:00:58 - 00:01:02] If you haven't, look on the learn page.
[00:01:02 - 00:01:12] Yes, as I mentioned in that message, if I want to suggest, as you contact the people
[00:01:12 - 00:01:17] in the team and maybe have a quick meetup and make sure everything seems alright, there's
[00:01:17 - 00:01:24] not any particular weirdness or anything. And if for some reason that team doesn't work
[00:01:24 - 00:01:31] for you, let me know by Friday, or do my best to accommodate changes if they really need
[00:01:31 - 00:01:39] to be. But you can't have a reason that you can explain to me that you need to change it
[00:01:39 - 00:01:45] not just like I think they're all stupid and not one a different team. Because that one's
[00:01:45 - 00:01:52] not going to fly. But you know what I mean? So if something is up and you don't, you know,
[00:01:52 - 00:02:00] you can't work with that team, you know. But that's a good opportunity to meet the members
[00:02:00 - 00:02:07] of your RoboCup team and start to think about the project itself. So we're aim to have the
[00:02:07 - 00:02:14] RoboCup kits to you by the beginning of turn two. Obviously you can see what sort of things are in
[00:02:14 - 00:02:22] it because you've seen the, you can see the robots that are in the, in the Tron lab. And you've got
[00:02:22 - 00:02:29] the brief now for the project. So you can start thinking about things and tossing around concepts
[00:02:29 - 00:02:35] ideas and stuff like that. Because the conceptual design report, I forget, make sure I need to just
[00:02:35 - 00:02:41] tweak the right, the brief of that on what you need to deliver. But regardless of that, you still
[00:02:41 - 00:02:47] need to start thinking about, you know, the concepts and that sort of thing and just letting those,
[00:02:47 - 00:02:52] letting those percolate in your mind. Because if you try and do it all last minute, obviously,
[00:02:52 - 00:02:58] doesn't work out there well. So is there any questions about that before we move on?
[00:03:02 - 00:03:08] No, good. The other thing to note, as I mentioned, the other day, Dominic will be giving some
[00:03:08 - 00:03:14] guest lectures one this Friday, one in a couple of Fridays that's around writing. And I know
[00:03:15 - 00:03:20] some of you can probably write quite well. So this is just a bit of a refresher based on my
[00:03:20 - 00:03:25] experience of reading reports in the past. Some of you can't write that well or at least not
[00:03:25 - 00:03:32] up through your clock on the morning where that report is due. So this might serve as a reminder
[00:03:32 - 00:03:40] on what you can do if you just start early. And so you are expected to come along to those. And so
[00:03:40 - 00:03:43] I'll just pass around to sign up sheet just for those of you here to sign off if you've got a
[00:03:43 - 00:03:49] good reason that you can't be here. That's okay. Let me know. Typically, it's not a problem.
[00:03:51 - 00:04:00] That's, yeah, do come along. And then next week, there is during the lab slot, which is on the Wednesday
[00:04:00 - 00:04:05] from like one to three, I think, we'll have the tutorial for the multi-domain modeling stuff. So
[00:04:05 - 00:04:12] if you want, you can, so with that, that's not, that's not compulsory to turn up to. It's just an
[00:04:12 - 00:04:18] opportunity for you to get some support in the Tron lab by myself and maybe a few TAs while you're
[00:04:18 - 00:04:23] working through that. If you want, you're welcome to start working through that tutorial
[00:04:24 - 00:04:30] anytime now, whatever. You could get it done. And then you might never even need to turn up to the
[00:04:30 - 00:04:35] lab next week if you want. If you want to get ahead of things, that's absolutely fine. If you're
[00:04:35 - 00:04:41] running any bothers or you need help, you can come along to that. So again, as that one's not a
[00:04:41 - 00:04:47] compulsory thing, but it is there are two support years you work through that because most of you
[00:04:47 - 00:04:53] haven't had any experience working with Simulink and that sort of thing. So it's possibly just a good
[00:04:53 - 00:04:59] opportunity. I think that's all those sort of announcements. It's a little bit messy with these
[00:04:59 - 00:05:08] guest lectures and stuff and the session being on and off sometimes. And also you've got
[00:05:08 - 00:05:20] classrooms now so that's good. Talk to them. Cool. Anything? Anyone got any questions? Good. Okay.
[00:05:21 - 00:05:29] So what the topic of this lecture is about is what's the introduction to modeling? Why are we
[00:05:29 - 00:05:35] interested in modeling? Why would I give this lecture and possibly the following ones?
[00:05:44 - 00:05:49] Yeah, I know. It's pulling blue steel on the faces like that. So what is modeling? What is modeling
[00:05:49 - 00:05:54] in the sense of megatronics? Not in the sense of power, you know, fashion week.
[00:05:55 - 00:06:06] What do I mean by modeling? It's a good question. He's a virtual or visual.
[00:06:07 - 00:06:13] Virtual. Okay. Yeah. So it may not even be digital, but you're getting there with the
[00:06:13 - 00:06:20] recursions of what might occur in real life. But I guess you can step back and look at a bit more
[00:06:20 - 00:06:38] height. What is a model? A prediction of what would happen? You have part of it. Yeah. A step
[00:06:38 - 00:06:42] before a prototype. I'm repeating it. So if anyone's watching on learn, they, because obviously they
[00:06:42 - 00:06:46] won't be a sorry, I'm not an eco. They won't be able to hear a step before a prototype. It probably
[00:06:46 - 00:06:51] is something that's going to be a step before a prototype. This I've got this part, the slide here. And it
[00:06:51 - 00:06:57] fits within the broader, you know, system design area. Where do we do modeling? In fact, we can do
[00:06:57 - 00:07:03] a little bit of modeling here, but often it occurs here around the design and prototyping stuff.
[00:07:03 - 00:07:09] So that's not a, not a silly answer the step before a prototype. It can be,
[00:07:09 - 00:07:17] one fact, actually, that probably also curves around a little bit. And models can occur elsewhere.
[00:07:17 - 00:07:26] I mean, obviously it's this model here too. So I missed that. What else might it be?
[00:07:26 - 00:07:32] What's another way of looking at it? That's, that's getting into it. So an estimation
[00:07:32 - 00:07:40] right. We're starting to get into a, I guess what is, when you say an estimation, what do you
[00:07:40 - 00:07:56] mean by that? Yeah. And so in doing that, what do we normally end up having to do to make the model
[00:07:56 - 00:08:03] that results in the system? Yeah. So model, model really will get there in a minute, but a model
[00:08:03 - 00:08:08] is largely a simplification. Because what is it? If we've got a system and they're, we're modeling
[00:08:08 - 00:08:18] it and it's not a simplification. So absolutely captures everything. What is it? It's the original
[00:08:18 - 00:08:27] system. Right. And so a model is by definition a simplification of our system that we're investigating.
[00:08:27 - 00:08:33] And so why do we want to do that? Well, having the model allows us to refine and perfect
[00:08:33 - 00:08:37] design before we commit to that product. And so obviously that's why, you know, you mentioned before
[00:08:37 - 00:08:43] a prototype. A prototype also allows us, but it's a little bit more of a costly exercise
[00:08:43 - 00:08:50] often to build and develop that prototype than if we can do it in a, let's say, maybe a digital model
[00:08:51 - 00:09:01] some form like that. And so that allows us to do a chunk of the design process. We can investigate what
[00:09:01 - 00:09:08] happens in certain situations with the thing that we're designing. And because we're doing that
[00:09:08 - 00:09:14] before we're committing to that final product or prototype, that can be a whole lot less expensive.
[00:09:14 - 00:09:19] And so there's a nice quickie. I mean, Frank Lloyd Wright was an architect like a building
[00:09:19 - 00:09:24] architect. And he's got it here. You can use an eraser on the drafting table or a switch hammer
[00:09:24 - 00:09:31] on the construction site. One's a whole lot cheaper than the other. If you change the building
[00:09:31 - 00:09:38] partway through, that's a very costly experience. So modeling allows us to do that in a relatively
[00:09:38 - 00:09:45] low cost way. Getting back to the simplifications that are for it also allows us to manage complexity.
[00:09:45 - 00:09:51] Because, you know, thinking about, I don't know how fast through you are with
[00:09:51 - 00:09:55] through us three yet. Have you been told about your, I don't think you've been told about your labs
[00:09:55 - 00:10:04] you know for that. Okay. So on Friday when you learn about the labs, it's a cart on us on a rail and
[00:10:04 - 00:10:10] it moves around. It's going to, when you model it, it's going to be a simplification because
[00:10:10 - 00:10:18] if you didn't simplify, you would have to take account of things like bank, cash, non-linear
[00:10:18 - 00:10:26] friction, non-viscus friction, air resistance, weird frictions like in the cable
[00:10:28 - 00:10:37] housing, I suppose, that moves with the cars. All sorts of weird stuff or complicated stuff,
[00:10:37 - 00:10:44] which is hard. A is hard to model hard to capture and it's also hard to put numbers on. Like,
[00:10:44 - 00:10:49] how do you put a number to that non-viscus friction? Like, how do you get that number?
[00:10:50 - 00:10:57] And so it allows us to manage complexity because what do we do? Like, when we're making simplifications
[00:10:57 - 00:11:02] like that sort of thing, what are we actually doing? What do we, you know, with air resistance as
[00:11:02 - 00:11:09] an example? What do we do with that in terms of modeling a dynamic system? A simple like
[00:11:09 - 00:11:17] three or three type dynamic system. Yeah, we ignore it. We ignore a lot of things. As engineers
[00:11:17 - 00:11:23] we like to ideally model systems and so anything that doesn't fit in nice solution, particularly
[00:11:25 - 00:11:32] differential equations like in dynamics, it's easier just to go sweet down to the table. Like,
[00:11:32 - 00:11:38] non-viscus friction, you know, like normally static and can edit friction or cool on friction,
[00:11:39 - 00:11:45] doesn't fit the form that we solve these equations. So we just ignore it. It's not too bad, right?
[00:11:45 - 00:11:50] It's not going to be that much of an effect. Backlash, it's a bit of a nuisance. What do we do
[00:11:50 - 00:11:58] with it? Just ignore it. Temperature effects, all these things. You know, for that system,
[00:11:58 - 00:12:07] air resistance is not going to have a particularly noticeable effect, probably. And so what do we do?
[00:12:07 - 00:12:15] We ignore it. And so that allows us to manage complexity and ideally boil the system down to something that
[00:12:15 - 00:12:23] is tractable with the analytical methods that we've got at hand. And, you know, in that case,
[00:12:23 - 00:12:28] for 3 or 3 that's stuff like being able to put them in an equation to motion,
[00:12:29 - 00:12:36] then into differential equations like emix double dot plus cx dot plus k x equals f, right? And that's
[00:12:36 - 00:12:41] just a nice form that we can then apply a solution to. We can see what it behaves like.
[00:12:43 - 00:12:50] And so modeling is nice for that aspect. But it might also be particularly in sort of the
[00:12:50 - 00:12:55] megatronic side of things. That model might explicitly be incorporated into the final design.
[00:12:56 - 00:13:01] And so in a couple of options, you might have a state estimator. So you might have a system
[00:13:01 - 00:13:07] until you learn about these more than 403 next to them. But you might have a system that has got
[00:13:08 - 00:13:15] states that you're interested in, that you can't directly measure. But there are other things,
[00:13:15 - 00:13:22] you can make an estimate of what they are by measuring other parts of the system. So, for example,
[00:13:23 - 00:13:26] it relatively trivial level, right? You might need to know displacement, but you can
[00:13:26 - 00:13:30] know the measure of velocity. So then you can estimate displacement, or calculate displacement,
[00:13:30 - 00:13:35] that's not too hard. But there are other states you might not be able to directly measure. And so
[00:13:35 - 00:13:41] therefore you want to estimate those. And in fact, I don't know, have you come across common
[00:13:41 - 00:13:48] heard of common filters? Or not yet? If you will possibly hear about them if you haven't already
[00:13:48 - 00:13:55] in the two material. It's got the term filter in it, which makes it sound like it's smoothing
[00:13:55 - 00:14:00] signals. And it can be used for that. But what it is actually doing, and smoothing the signal
[00:14:00 - 00:14:07] that's doing that by trying to underestimate what is the underlying system behavior. And just
[00:14:07 - 00:14:14] acknowledging that what you see is what looks like variability is noise on top of that system behavior.
[00:14:14 - 00:14:20] And so it's called a common filter, but it's actually a sadist's domain. And you might also use
[00:14:20 - 00:14:24] them in model predictive control. So you might have a system where it's, let's say, nonlinear.
[00:14:25 - 00:14:31] And what you do is model predictive control from a high level. As you say time in, or time t,
[00:14:32 - 00:14:38] you've got a dynamic model of the system. You've got some potential control inputs to that system.
[00:14:38 - 00:14:43] And so you forward simulate from where you are now, you forward simulate with control input one,
[00:14:43 - 00:14:47] see where it ends up, control input two, control input three, control input four. And you see where it
[00:14:47 - 00:14:54] ends up. And then at some point down the road, maybe five times steps down the road. And then you
[00:14:54 - 00:15:00] choose the one, the control input that gives you the output as closest to what you desire. Then you
[00:15:00 - 00:15:05] step forward and time and you repeat that process. So you're using that dynamic model of your system
[00:15:05 - 00:15:11] to estimate what happens when you control it. And then you're choosing the control inputs that
[00:15:11 - 00:15:19] provide that best input, best output. So, but obviously this is requiring quite a lot of
[00:15:19 - 00:15:28] simulation to occur quite rapidly between time steps. And so for something like this, it needs to be
[00:15:28 - 00:15:33] computable quite quickly because you're going to have to do a lot of these. It's not like you just
[00:15:33 - 00:15:38] don't have one. You're going to be doing t in hundreds of thousands to decide what you want to do.
[00:15:40 - 00:15:45] So modeling has quite a lot of impact potentially in the michatronic system.
[00:15:46 - 00:15:48] We've already talked about waters of model.
[00:15:49 - 00:15:59] There's one on the right. And these, I mean, this is just a slide to show a number of different models.
[00:15:59 - 00:16:04] Like a lease, even when you use Excel or Python and you do a linear list,
[00:16:04 - 00:16:10] squares fit, you've got some data and then you fit a line through that. That is a model of
[00:16:10 - 00:16:14] you're assuming that there's some underlying linear process and then you've got some noise on top
[00:16:14 - 00:16:19] of that and you're trying to figure out what model and determine what their underlying process is.
[00:16:19 - 00:16:23] You may have said a differential equation. That's a model you might have.
[00:16:24 - 00:16:31] Even an architecture diagram like this is a model control block diagrams, models free body diagrams,
[00:16:31 - 00:16:38] models, physical systems, when NASA were looking at their reentry vehicles,
[00:16:38 - 00:16:44] they have a physical model to see how things pan out. And so modeling encompasses quite a broad
[00:16:45 - 00:16:53] range of things. But I think one thing, which always have to remember and it comes back to what
[00:16:53 - 00:17:01] you said, it's a simplification. So George E.P. Box was a British statistician and he had wrote
[00:17:01 - 00:17:05] this quote in about three different ways. But one of them was essentially all models are wrong,
[00:17:05 - 00:17:08] but some are useful. So what was he meaning by that, all models are wrong?
[00:17:12 - 00:17:17] Yeah, because it's a simplification. Right. It's not exactly accurate because if it was
[00:17:17 - 00:17:21] exactly accurate, it's no longer the model. It's the thing that you were trying to model.
[00:17:21 - 00:17:26] And so they're all a bit wrong, but some are useful. Yet another form of this
[00:17:26 - 00:17:34] where it came down to, but some, the question is how useful can they be, sort of thing.
[00:17:35 - 00:17:39] And so when we do some modeling, we acknowledge our models are wrong.
[00:17:41 - 00:17:45] But we've got to appreciate that because a lot of people, a lot of time people get really
[00:17:45 - 00:17:50] caught up in how fancy their model is. And they sort of think it's the B's and A's,
[00:17:51 - 00:17:57] there's nothing wrong with it. But it's a simplification. And so they can be useful simplifications,
[00:17:57 - 00:18:04] but they're out there actual system. So you know, getting back to, I guess, what is a model,
[00:18:04 - 00:18:10] it's a simplified representation or it's an abstraction. Okay. And so that's what you came up with
[00:18:10 - 00:18:17] earlier. And that allows us to, you know, they can be useful for our design. It can be useful
[00:18:18 - 00:18:25] for your in our design as a model for the control or something like that.
[00:18:28 - 00:18:39] Any questions at this point or any, any, but have any thoughts about that modeling? Very good.
[00:18:40 - 00:18:47] Okay. This is, there's many ways to categorize models. This is a way
[00:18:48 - 00:18:54] I don't know how much about the shapes, but models can be kind of structural. So that's
[00:18:54 - 00:18:58] going, thinking back to what we talked about last week around architecture, like how things are
[00:18:58 - 00:19:05] connected. And not necessarily even just physically connected. It can be the connections between
[00:19:05 - 00:19:14] information flow, for example, or they can be behavioral. And so that's more just kind of capturing
[00:19:14 - 00:19:23] the behavior of the system. And to some extent, you know, there can be some crossover or,
[00:19:23 - 00:19:28] you know, it's almost depends sometimes on what you're using the model for as to what category it
[00:19:28 - 00:19:33] lies in. Right. More than maybe I'll talk about it in a minute when I've got some examples.
[00:19:33 - 00:19:37] Models can also be static or they can be dynamic. So what's the difference between
[00:19:37 - 00:19:43] aesthetics and dynamic and this sort of sort of sense? Yeah. So dynamic,
[00:19:43 - 00:19:49] specifically comes down to it without changes over time. And so there can be static models so
[00:19:49 - 00:19:54] that can just be, you know, it's time independent if you like. So you might have, what might be an
[00:19:54 - 00:20:03] example of a static behavioral model. So it's capturing the behavior of a system and it's not
[00:20:03 - 00:20:16] changing over time. Yeah. So something that's not moving physically. Right. Yeah.
[00:20:19 - 00:20:28] Could be depending on how, yeah, it depends on, I guess, how you're using the model, for example.
[00:20:29 - 00:20:35] You could argue, for example, that something like a flow diagram is a behavioral model because it's
[00:20:35 - 00:20:42] capturing what happens, but that behavior is static and that the flow diagram doesn't change.
[00:20:42 - 00:20:48] Whatever it is, the flow diagram is the model is not changing over time as fixed. Whatever it is
[00:20:48 - 00:20:55] that you're modeling with that flow diagram is changing over time, but the model itself is that
[00:20:55 - 00:21:01] flow diagram. So you could argue that that was static. But anyway, we'll kind of cover a little bit
[00:21:01 - 00:21:06] more of that shortly. So what are some kind of abstractions that we make in modeling? So we talked,
[00:21:06 - 00:21:11] we did talk about some before with like three or three. What things do we like to ignore?
[00:21:13 - 00:21:18] Yep. Air resistance. Four or two circumstances. Right. Three or three. We wouldn't ignore
[00:21:18 - 00:21:31] air resistance if we were designing a plant or a UAV. Yes. Yeah. So environmental factors often
[00:21:31 - 00:21:36] we ignore temperature. You don't go into the lab for three or three and take a temperature
[00:21:36 - 00:21:40] measurement. So it's 30 degrees today. It's going to behave differently yesterday when it's 28 degrees
[00:21:40 - 00:21:53] in the lab because largely that's going to be a negligible effect on that system. There's an
[00:21:53 - 00:22:01] acronym LTI which may have popped up. Maybe it hasn't yet. And controls. The linear time and
[00:22:01 - 00:22:08] variant. So you assume it's linear. And so that's things like linear in that sense as we'll use
[00:22:08 - 00:22:14] viscous friction but we'll ignore other stuff. Time and variant means if I test it now and then
[00:22:14 - 00:22:21] I test it 10 minutes later it's going to behave the same. Like the we knew test it in time doesn't
[00:22:21 - 00:22:27] change how that model behaves. And so that's quite a common abstraction. So things that you mentioned
[00:22:27 - 00:22:33] like neglecting small effects, things like air resistance and stuff, independent of the environment.
[00:22:34 - 00:22:39] Lumppt parameters. What do we mean by lumped parameters? Think about a cart on a like the
[00:22:39 - 00:22:49] mass cart system. Yeah. We assume it's a point mass. We don't acknowledge that that mass is actually
[00:22:49 - 00:22:56] distributed across the space that it takes up. Same with the spring, right? We assume that that
[00:22:56 - 00:23:02] spring is effectively a point spring. Well say it's got displacement or you know, length and stuff
[00:23:03 - 00:23:10] the force it exerts but we just treat it as k at a point in space. Same with damping and things like that.
[00:23:12 - 00:23:20] So that's the lumped parameter assumption because otherwise it gets you know it gets messy then
[00:23:20 - 00:23:25] you're going to have to integrate stuff across this mass. You know in terms of what you're doing for
[00:23:25 - 00:23:30] controls it doesn't matter if that thing weighs one kilo and maybe 800 grams of it's here and 200
[00:23:30 - 00:23:36] grams of it's here. It doesn't really matter but and so you can treat it as a one kilo point mass.
[00:23:37 - 00:23:42] But if you want to do other things with it you might not be able to do that. So linearity meaning
[00:23:43 - 00:23:57] what do we mean by linearity? Not that it goes in a straight line. That's quite of a circular
[00:23:57 - 00:24:15] argument. What do we mean by those linear systems? No, I mean that may end up there way
[00:24:15 - 00:24:25] but yeah that's not the not the answer I'm kind of looking for. That's kind of circular as well.
[00:24:29 - 00:24:34] I think you're getting to that. I guess what it comes down to is you got related to that.
[00:24:34 - 00:24:38] It's basically that superposition applies. If you've got this here you've got a solution to the
[00:24:38 - 00:24:44] cart and then you apply a force that's a little bit extra. The solution to the
[00:24:44 - 00:24:50] the behavior of the cart will be the original one plus the solution to the little bit extra
[00:24:50 - 00:24:56] that you've added. You can add them linearly. So basically that means superposition applies and
[00:24:57 - 00:25:05] therefore you can write out a more formal definition of it but if you can apply superposition.
[00:25:05 - 00:25:10] So if you've got twice the force then the behavior will be effectively twice the
[00:25:10 - 00:25:16] amplitude and stuff like that then it's that's largely what's captured by linear. Time independent
[00:25:16 - 00:25:21] as I mentioned. Well, technically it's an uncertainty. No wear and controls or anything like that.
[00:25:21 - 00:25:28] Do we say we've got encoder and it's uncertainty on any measure as thus and therefore we have
[00:25:28 - 00:25:33] to take that uncertainty into account. We just say we've got this value that's good enough. We
[00:25:33 - 00:25:39] might do something like filtering it or averaging it if you're like but we just we don't really
[00:25:39 - 00:25:45] do anything with that uncertainty. We assume that we've got this measure and it is perfect and
[00:25:45 - 00:25:53] jobs are good enough. So these are some common abstractions that we use in modeling.
[00:25:57 - 00:26:03] So there's just a few different type, these are some almost just examples of different types of
[00:26:03 - 00:26:08] modeling. Right, so these are structural modeling but they cover a range of things. One, we've got a
[00:26:08 - 00:26:15] a Lego model but you might have a CAD model. Right, so that's a digital representation of your system
[00:26:15 - 00:26:22] which you can use for then manufacturing. You can use it for testing or a developing the system
[00:26:22 - 00:26:27] and seeing if everything fits. You can also use it to do some kind of a modeling within solid
[00:26:27 - 00:26:34] works. You can use it to do some FBA calculations and stuff like it's got a lot of possibilities.
[00:26:35 - 00:26:42] You might have a real, you might then build it to make sure. So you've got a life size model but
[00:26:42 - 00:26:48] it's not necessarily the real thing. It's almost like a prototype if you like and then you've
[00:26:48 - 00:26:53] obviously got the real thing in the end whether it's being tested on earth or it's the actual thing
[00:26:53 - 00:27:00] of Mars. So there's some physical models. So let's try a few models aren't just necessarily limited
[00:27:00 - 00:27:07] to the models of the physical structure. So they can also be models of the process if you like.
[00:27:07 - 00:27:14] So and it also then comes down to what you want to use that model for. So if you've got a
[00:27:14 - 00:27:19] control block diagram like this depending on how you're looking at that you can use that to extract
[00:27:19 - 00:27:25] out your closed loop transfer function and so on and then get the behavior from that. You may
[00:27:25 - 00:27:30] be looking at it from a behavioral sense but if you're looking at the sort of the structure of
[00:27:30 - 00:27:36] the control system and how things are connected and where signals flow this you could consider as a
[00:27:36 - 00:27:42] structural model because it's how things are connected. You might have like a functional architecture
[00:27:42 - 00:27:47] block diagram or like we talked about the other week. That's a structural model of how things are
[00:27:47 - 00:27:56] connected. Not a physical model of it but you know trying to looking at the interactions between
[00:27:57 - 00:28:04] different modules on your system. So all of these there's still abstractions right. There's
[00:28:04 - 00:28:10] simplifications because you've got a block here that says wheel motors. Inside that there's a lot of
[00:28:10 - 00:28:18] complicated stuff but we can have a stretch that to a much higher level. You know there are other
[00:28:18 - 00:28:23] types of model. I mean we aren't going to listen to detail but the data flow diagram which you might
[00:28:23 - 00:28:28] use you know you have a function and a database and then put an output and flow which can help
[00:28:28 - 00:28:40] your model. What you know how you might build a system for taking book orders and payments and stuff
[00:28:40 - 00:28:49] like that. Linear graphs and bond graphs again initially again it comes down to what you know what
[00:28:49 - 00:28:58] we're using them for. So this obviously it's a mess spring damper. We can extract from this model
[00:28:58 - 00:29:05] we can extract the equations of motion which can allow us to calculate the behavior of that system
[00:29:05 - 00:29:11] over time so it becomes dynamic, the dynamic behavior model. But this in itself is also a model,
[00:29:11 - 00:29:20] a structural model how things are connected and they allow us to you know understand what's going
[00:29:20 - 00:29:23] on. Particularly obviously it's simple one like that's easy but you might have a more complicated
[00:29:23 - 00:29:34] system that that structural is looking at it is quite useful. Looking then into behavioral type
[00:29:34 - 00:29:39] models obviously ones we've talked about like differential equations they can capture they
[00:29:39 - 00:29:43] depending what you want to use them on but they can capture the behavior of the system and it's
[00:29:43 - 00:29:48] you know that's quite obvious. The flow diagram captures the behavior of the system but the model
[00:29:48 - 00:29:53] itself you could argue a structural because it's looking at the connections and how things are
[00:29:54 - 00:30:06] how things are connected or aspects of it are connected. So yeah I mean flow diagram is quite
[00:30:06 - 00:30:16] common in the robot cut reports. Here's one from a previous report. What's wrong with this?
[00:30:17 - 00:30:37] Maybe it actually designed the robot to behave like this I'm not sure. So what will you mean
[00:30:37 - 00:30:47] doesn't risk that? There's nothing coming out of clicked way right and so it's good that they're
[00:30:47 - 00:30:54] thinking about this and there's a lot of stuff here but in reality from here they probably should be
[00:30:54 - 00:31:00] a loop background or maybe the search state right. If you read that correctly that robot will click
[00:31:00 - 00:31:06] the way and then it'll just stop and I guess that hopes the other robot doesn't click the bigger
[00:31:06 - 00:31:18] one. And so again and these will have a look at them on the next page. These are quite good
[00:31:22 - 00:31:29] but there's another way which you might find more useful. So these are described again and so
[00:31:29 - 00:31:38] the NASA systems engineering handbook. There's three volumes of it but there are some bits which
[00:31:38 - 00:31:44] there's a lot of words in there. There's some pictures. Here's a picture. So these are called
[00:31:44 - 00:31:51] functional flow block diagrams and so they're really an enhancement of a flow diagram but I think
[00:31:51 - 00:31:55] they're quite a good one because they allow they've got a lot more aspects they're not just
[00:31:56 - 00:32:03] they probably think I suppose a bit more. So you can have things like you can have logical statements
[00:32:03 - 00:32:11] like hands and ores or have alternate functions or parallel functions. You can obviously have notes,
[00:32:11 - 00:32:19] you can have go and no go situations and you can have I think on the next slide you can kind of have
[00:32:19 - 00:32:30] some I want the next next slide. So you've got things like added constructs in here. So this
[00:32:30 - 00:32:37] concurrency so two things are occurring at once. As I said you can have logical stuff and ores. You
[00:32:37 - 00:32:46] can have loops and so this has got a looping type behavior and so you can start to capture I guess
[00:32:46 - 00:32:54] stuff that you would normally encode and software perhaps or the way you're thinking which just
[00:32:54 - 00:33:02] I think adds a bit more power than just a standard flow and so then additionally to that you can have
[00:33:03 - 00:33:14] more structure or levels of abstraction and that you can have a hierarchical nature. So at a top level
[00:33:14 - 00:33:23] being a NASA example it's a spacecraft and so you know one two three four a cent into orbit
[00:33:23 - 00:33:30] injection check out deploy transfer to opus orbit perform mission operations or
[00:33:30 - 00:33:36] contingency operations obviously quite high level and then each of these blocks breaks down so
[00:33:36 - 00:33:44] inside perform mission you can see provide electric power provide energy stabilization do this
[00:33:44 - 00:33:50] in this order and then you can break that down so you can have these hierarchical systems so that you
[00:33:50 - 00:33:56] can start at a high level what your systems doing and then dive down into each of those to the point
[00:33:56 - 00:34:03] where you could implement that you know whether it's whether it's in software or it's a
[00:34:03 - 00:34:11] mix of software and hardware and things like that. So I think those are quite a powerful way to
[00:34:13 - 00:34:26] capture the behavior of systems perhaps like robo car so yeah so you know what going back to that
[00:34:27 - 00:34:32] when we head before from robo car this was just a flow diagram right but you know we
[00:34:32 - 00:34:37] what sort of things thinking about you know the functional flow block diagrams how could we make
[00:34:37 - 00:34:49] this hierarchical wheat what would you do you know which of these blocks could you break down
[00:34:49 - 00:35:01] and and broke open if you like and then have more detail yes yeah for example click to wait right
[00:35:01 - 00:35:06] you don't just go click wait and just like bump I suppose if you've got a combine harvester it does
[00:35:06 - 00:35:11] but you guys can't really do this so let's imagine you've got like an electron magnet at pick up
[00:35:11 - 00:35:16] that's going to have a process inside it you've probably got an energized electron magnet you've got
[00:35:16 - 00:35:23] to lower the crane or whatever it is pick it up and put it somewhere you know what sort of things
[00:35:24 - 00:35:28] might you have you mentioned navigate towards so what sort of things might be a navigate towards
[00:35:37 - 00:35:41] yeah exactly these sorts of things and so and then each of those blocks you can then dive down how
[00:35:41 - 00:35:47] would you implement that in your code and it starts to allow you to figure out right in how to
[00:35:47 - 00:35:55] structure the code and so these are but they're also quite good to allow people who
[00:35:57 - 00:36:01] you know six feet deep in the project to be able to look at the project and figure out what you
[00:36:01 - 00:36:17] doing with each of these as a good communications to hint hint yeah so this the next few slides
[00:36:17 - 00:36:23] relate to basically what you're going to be doing in the multi-domain modeling tutorial because
[00:36:25 - 00:36:30] the whole thing with a multi-domain modeling well what do you think I mean by multi-domain modeling
[00:36:30 - 00:36:44] this isn't the name but what do I actually mean when you're doing this for 303
[00:36:47 - 00:36:59] in which domain are we working and I'll leave in this quite broad just to see what you give answers
[00:36:59 - 00:37:11] so time is the plus I guess those are the temporal frequency domains yeah I so because I
[00:37:11 - 00:37:16] live at wide open good answer they are two domains but you know there was so that's how it's
[00:37:16 - 00:37:24] looking at it's more in which energy domains are we so one of the energy domains I see you also
[00:37:24 - 00:37:30] good answer can you the computational energy also related to that let's say in terms of
[00:37:30 - 00:37:38] I don't know relates to kinetic I'll just give you answer translational mechanical right so you've
[00:37:38 - 00:37:44] got mechanical energy and so so how do we calculate what's the power of it or how do you calculate
[00:37:44 - 00:37:56] power for translational mechanical force times velocity right yep so energy domains so it comes down
[00:37:56 - 00:38:02] to power there you've got two power conjugate variables so in translational mechanical you've got
[00:38:02 - 00:38:06] force times velocity obviously there's rotational mechanical and that's what you get out of
[00:38:06 - 00:38:11] an electric motor so you've got torque times omega what are some other energy domains now that
[00:38:11 - 00:38:18] we know what I'm talking about and you're not just having to guess yeah electrical right and so
[00:38:18 - 00:38:27] there are power out conjugate variables are current and voltage I see you did rotation mechanical
[00:38:27 - 00:38:35] yeah no you're right good any others yeah hydraulic hydraulic and you made it right largely
[00:38:35 - 00:38:43] one's compressible fluid ones are non-comprezible fluid yeah there's other ones as well like thermal
[00:38:43 - 00:38:53] or heat and like chemical chemical energy domains so obviously battery type system so we've got
[00:38:53 - 00:38:58] multi-domain modeling is trying to model because at the moment when you do this and through a three
[00:38:59 - 00:39:05] you are doing transitional mechanical and all the modeling is with that you don't really deal with
[00:39:05 - 00:39:11] like that doesn't couple to any other domains we need to do for a three next year you do a little
[00:39:11 - 00:39:17] bit of coupling because you'll have an electric motor which is in which is taking it effectively
[00:39:17 - 00:39:22] you know you've got electric energy and electrical energy and you convert that into rotation
[00:39:22 - 00:39:25] mechanical energy and then you've got a rack and pen it well I think you just do it with a DC
[00:39:25 - 00:39:31] motor you don't even go so fast to translational mechanical and so there is a coupling in that
[00:39:31 - 00:39:37] with a 2x2 matrix or it's all matrix equations a 2x2 matrix but mostly what you're doing at
[00:39:37 - 00:39:42] the moment is just single domain the whole idea with multi-domain modeling in particularly
[00:39:42 - 00:39:50] multi-domain modeling software is that it's really because these are all linked by energy it's
[00:39:51 - 00:39:56] not too hard to couple them together and so you can model systems that go from
[00:39:57 - 00:40:01] electrical energy through a motor to rotational mechanical energy through say a
[00:40:01 - 00:40:08] rack and pen in to translational mechanical maybe that's then for example driving a hydraulic
[00:40:08 - 00:40:14] ramp to hydraulic energy and these all couple because they all relate to energy they
[00:40:15 - 00:40:22] actually all play quite nicely together and so the software that you will end up using for that
[00:40:22 - 00:40:28] there's a number of different pieces of software that do this and the using industry
[00:40:28 - 00:40:34] warframe system modeler I forget the other names but within math works they've got one
[00:40:34 - 00:40:42] called cinscape which sits on top of simulating and so what that does and you'll work through this
[00:40:42 - 00:40:51] in the tutorial it's kind of graphical which is nice so you end up with a mass because we're
[00:40:51 - 00:40:55] looking to model this right we've got a mass connected to a spring and a damper and there's a force
[00:40:55 - 00:41:02] and there's some reference so we've got a mass we've got a translational damper we've got a translational
[00:41:02 - 00:41:08] spring with this here is just a way to apply the force to the mass here's our reference our ground
[00:41:09 - 00:41:16] this just defines a solver that's going to deal with it this here is the sensor that takes
[00:41:16 - 00:41:23] the measurements from the so the the location of the mass and so it's very quick to draw up and
[00:41:23 - 00:41:32] then put in values for k and c and m and when you do that obviously then you click run and it
[00:41:32 - 00:41:37] comes up with the answer that you would expect and it's all well and good but water that allows
[00:41:37 - 00:41:44] you to do is actually very quickly develop much more complicated models and so this is maybe a
[00:41:44 - 00:41:50] more complicated version of what's going on with that cart you've got for 303 so it's no longer just
[00:41:50 - 00:41:57] a mass sort of cart you've got a rack and pinion you've got a DC motor you've got a gearbox
[00:41:58 - 00:42:03] you've got an electrical power source if you like and then you've got feedback control so that
[00:42:04 - 00:42:10] can also be drawn up quite quickly this is the electrical domain so you've got a controlled
[00:42:10 - 00:42:16] voltage source a current limiter DC motor that DC motor then has got a gearbox and it's got
[00:42:16 - 00:42:21] some inertia then it's got a wheel and axle so the rack and pinion so it's converted into
[00:42:21 - 00:42:27] linear translation mechanical which has got a mass some translational friction and then a sensor
[00:42:27 - 00:42:33] and then that feeds back through your PID control which and then it's got some rate
[00:42:33 - 00:42:39] limiters and some saturation on there and so it's relatively fast to draw this up
[00:42:40 - 00:42:45] and that allows you to do so well but more importantly than it just being fast
[00:42:47 - 00:42:55] what's on here that's particularly of interest which is hard to do the way that you're learning
[00:42:55 - 00:43:02] with through through with analytical methods yes absolutely you can just change values and in
[00:43:02 - 00:43:06] effect because it's well I guess they're all like this you can have a dashboard there and then you
[00:43:06 - 00:43:11] can have little slide as for the P&I and D gains and you can just wiggle them while it's simulating
[00:43:11 - 00:43:27] and see what happens which is pretty neat but what else is on here what's going on here we've
[00:43:27 - 00:43:33] got a rate limiter and we've got saturation so a rate limiter won't let it change above us all
[00:43:33 - 00:43:39] faster than a certain rate we've got saturation so the controller's spitting out I don't know output
[00:43:39 - 00:43:48] 1000 volts but that motor driver can't do 1000 volts it's limited to 30 volts so these
[00:43:48 - 00:43:54] and non-linear things happening where you cannot do this with an analytical method it just doesn't
[00:43:54 - 00:43:58] because they're non-linear behaviors they're in there we've got a current limiter as well
[00:43:59 - 00:44:03] this translational friction block when you look into it is not just a viscous friction it's got
[00:44:03 - 00:44:09] co-lum friction and other non-linear forms of friction that you can put in there so we can
[00:44:10 - 00:44:22] this this will allow you to model non-linear systems why do you think it can do that how how
[00:44:22 - 00:44:26] does this solve how's this giving us a solution what do you think's going on under the book
[00:44:33 - 00:44:37] yeah it's not quite doing that we'll do the next lecture covers exactly what's going on what this
[00:44:37 - 00:44:44] does this forms this solvent numerically right so when you do analytical solutions in 303
[00:44:44 - 00:44:49] largely you've got a differential equation you do Laplace on it because Laplace makes differential
[00:44:49 - 00:44:55] equations solving a lot easier because you have to convolution and then you get a solution and it's
[00:44:55 - 00:45:02] you know decaying sine wave or something to that effect this is avoiding the analytical solution
[00:45:02 - 00:45:08] so it's done it numerically so it's using the only solvers that you know normally built in
[00:45:08 - 00:45:13] and it's done numerically because it's done numerically these things don't have to conform to standard
[00:45:13 - 00:45:20] analytical looking equations or solvable equations and so you can have things in there that you can't
[00:45:20 - 00:45:26] do you can have hard stops and rate limiters and things so it's a really nice way because you can solve
[00:45:27 - 00:45:36] or you can investigate systems that you can't do in an analytical way and so
[00:45:40 - 00:45:47] it used to be a nice teaching point but Robnys fixed things going back two or three years
[00:45:47 - 00:45:55] the motor controller for the car that you will use used to be shite basically it had a really low
[00:45:55 - 00:46:01] slew rate so it couldn't it couldn't the ramp of voltage that it would output was really quite low
[00:46:02 - 00:46:06] and also couldn't deliver a lot of current and so your design controllers are met lab and you go
[00:46:06 - 00:46:11] down there and implement them and the output you got was nothing like what you'd simulated because
[00:46:11 - 00:46:18] the controller box there was rubbish most of the time when you write your reports you say
[00:46:18 - 00:46:23] oh it's because friction it's because of backlash and whatever but it wasn't it was because the
[00:46:23 - 00:46:28] the motor controller was a bit short and so it was quite nice because you could see that when
[00:46:28 - 00:46:34] you simulated that this and this part of it Robnys subsequently updated it and now the motor
[00:46:34 - 00:46:37] controller is rather fast and so when you go and simulate it and make a little bit analytically it's
[00:46:37 - 00:46:43] pretty much what you get out and so it's not such a convenient teaching point for me anymore with
[00:46:43 - 00:46:52] this but there are as I mentioned these other things like you know translational friction you've
[00:46:52 - 00:46:56] got breakaway friction for spray-confriction velocity cool on friction force of viscous friction
[00:46:56 - 00:47:04] coefficients you've got a lot of possibilities with the motors you know when you've got
[00:47:04 - 00:47:11] that DC motor how do you parameterize there there's some options if you buy expensive motors from
[00:47:11 - 00:47:15] like full harbor in Germany you pretty much get all of those parameters in the data sheet
[00:47:17 - 00:47:22] which is nice if you buy cheap motors from AliExpress you don't get there and you have to
[00:47:22 - 00:47:28] guess or do some testing and bits and pieces and so it opens up another problem where do we get
[00:47:28 - 00:47:38] these values from you know just finished just going back to that and it's a little bit hard for
[00:47:38 - 00:47:45] you to see going back to the old motor controller what you can see here is the this was the behavior
[00:47:45 - 00:47:53] of the car this yellow line so that was a command voltage sorry of the of the PID control for the
[00:47:54 - 00:47:59] and the blue line here was the actual output once it had gone through those rate limiters and
[00:47:59 - 00:48:07] saturation so the controller was asking something and the cart couldn't do that and therefore you
[00:48:07 - 00:48:13] get quite a difference between the behavior of the cart and what you're assimilated so no longer
[00:48:13 - 00:48:18] helpful for your 303 labs but you can see where this might be helpful if you're designing a system
[00:48:18 - 00:48:22] in reality because you can draw this up pretty quickly you can then test it and you can see
[00:48:22 - 00:48:29] is my motor controller gonna do what I want it to do yes or no do I need to change the design of
[00:48:29 - 00:48:36] my system and that sort of thing and then also and allows you to quickly
[00:48:37 - 00:48:45] increase complexity because you can use cut and paste and so this was the first cart here
[00:48:46 - 00:48:50] when you do 403 next year you do three carts and they're connected by spring so you've got one
[00:48:50 - 00:48:54] cart that's got a motor on it and you've got to get the third cart which is wobbling along like
[00:48:54 - 00:49:00] this to a certain point and so it's very easy to take this cart and go cut paste paste to connect
[00:49:00 - 00:49:06] them by springs and then you've got that model system really quickly as opposed to having to do
[00:49:06 - 00:49:13] it in a three by three three by three matrix analytical solution and obviously then you've
[00:49:13 - 00:49:23] got the nonlinearities and all that sort of thing so these sorts of tools are becoming much more
[00:49:24 - 00:49:30] widespread I was at Trimble recently and they use some scape and some scape
[00:49:30 - 00:49:34] multi-body to do a huge amount of their modeling and their agricultural business here like
[00:49:34 - 00:49:40] their developing controllers so that you can retrofit so you can make tractors and other agricultural
[00:49:40 - 00:49:45] equipment self-driving but it's retrofitting to old stuff so they have to have all these models
[00:49:45 - 00:49:51] of all these old tractors and then testing their controllers on them and they're doing their in this
[00:49:51 - 00:49:58] exact same pace as software and so having some experience doing this is an understanding of what's
[00:49:58 - 00:50:07] going on is quite valuable I think for you. Good so that's the summary. Modeling is a simplified
[00:50:07 - 00:50:13] representation they can help in the design process there's all sorts of different model types and
[00:50:13 - 00:50:20] methods and that's sort of called to the mechatronics design process and I think while we don't
[00:50:20 - 00:50:27] teach a huge amount of it here yet we're aiming to kind of try and push more in over time.
[00:50:29 - 00:50:46] So any questions? I would say that so typically for something like that if you're trying to find
[00:50:46 - 00:50:52] parameters like friction and motor parameters and stuff like that you would do some testing
[00:50:52 - 00:50:57] and again many of these pieces of software like MATLAB's got a parameter identification
[00:50:59 - 00:51:03] tool set if you like and so you can do you can take a motor and you can provide
[00:51:04 - 00:51:07] you know if you let say you measure current and you provide known voltages to it and you
[00:51:07 - 00:51:12] get the output you can run it through a different a couple of different runs and then feed that in
[00:51:12 - 00:51:19] there and then that will go broke an output a model a model parameter set for that motor again
[00:51:19 - 00:51:24] being a model that won't be perfect I mean a number of things with this actually in doing and trying
[00:51:24 - 00:51:30] to put this together a number of years ago we're luckily we had four hub of motors we've got all
[00:51:30 - 00:51:35] that sort of information but I was looking at another one which was just using a like a basically a
[00:51:35 - 00:51:45] DC motor for a drill that you just get off AliExpress it's like a $5 motor and I don't know when
[00:51:45 - 00:51:51] you when you learn electronics and let's say 270 what do you know about inductance or how do we treat
[00:51:51 - 00:51:58] inductance like you've got an inductance got a value L right and we just assume that it's
[00:51:59 - 00:52:04] but it's not inductance is frequency dependent which kind of misses with you when you
[00:52:05 - 00:52:11] you know you've got jmiga al for example if you're looking at the phaser at presentation
[00:52:11 - 00:52:20] or the impedance if you put an lcr meter over a motor and you're trying to measure the
[00:52:20 - 00:52:27] armature inductance you measure it at 100 Hertz a kilo Hertz 10 kilo Hertz but that inductance across
[00:52:27 - 00:52:33] I think was four or five orders of magnitude of frequency the value of inductance doubles right so
[00:52:33 - 00:52:38] you've got quite like the inductance changes quite a lot it's not fixed and so that's another thing
[00:52:38 - 00:52:43] we always just assume I've got an inductance inductance but that's not the case the inductance depends
[00:52:43 - 00:52:48] on the frequency these are just al by you know examples as engineers we just make these
[00:52:48 - 00:52:53] simplifications and they have instructions because it makes life easy but in reality it's not how
[00:52:53 - 00:53:00] it works and so that's why all models are wrong but they're still quite useful very good
[00:53:01 - 00:53:35] it's five o'clock it's probably time to go home so we'll see you all tomorrow
[00:54:51 - 00:54:54] yeah

# ENMT301-26W Lecture 23 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `112d09802b2f030d2f73a994707e8292f59c811a0358d40fc083c8b4bfd8cdd5`
Generated: 2026-06-06T05:54:40.767228+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:18 - 00:00:22] Okay, very quiet today.
[00:00:24 - 00:00:27] Right, so if it was like a long time ago,
[00:00:27 - 00:00:31] we talked about the start of this,
[00:00:31 - 00:00:33] physical systems modeling stuff.
[00:00:33 - 00:00:35] Obviously it was only last week.
[00:00:35 - 00:00:38] Many of you, how many in here,
[00:00:38 - 00:00:41] turned out the tutorial is cool.
[00:00:41 - 00:00:43] Well, so if you didn't turn up to that,
[00:00:43 - 00:00:44] you might have had already worked through that
[00:00:44 - 00:00:45] in your own time.
[00:00:45 - 00:00:47] Hopefully found that a little bit useful,
[00:00:47 - 00:00:49] interesting to see what you can do with this sort of stuff.
[00:00:49 - 00:00:54] It's quite fast to be able to develop these models
[00:00:55 - 00:01:00] and make changes and explore dynamic systems.
[00:01:03 - 00:01:06] And ultimately, that's helpful for design,
[00:01:06 - 00:01:10] for optimizing designs and things like that.
[00:01:12 - 00:01:16] In the future, I aim to have more of that in the course.
[00:01:16 - 00:01:18] It just takes some time to develop it
[00:01:18 - 00:01:21] in a way that kind of fits and makes sense.
[00:01:22 - 00:01:24] But anyway, so that's the start of it.
[00:01:24 - 00:01:28] So just to reiterate what we talked about last week,
[00:01:29 - 00:01:31] talking about these single-port elements.
[00:01:31 - 00:01:34] And so, what, because I wanna remind me,
[00:01:34 - 00:01:37] what we mean with single-port elements?
[00:01:37 - 00:01:49] What does that mean?
[00:01:49 - 00:01:52] Oh, yes, basically single-energy port, right?
[00:01:52 - 00:01:54] So, Ed will have two terminals,
[00:01:54 - 00:01:57] faulted in current, torque and omega or whatever.
[00:01:58 - 00:02:00] And often, I mean, that's a simplification.
[00:02:00 - 00:02:02] Like if we're talking about a resistor,
[00:02:02 - 00:02:04] that's a dissipator.
[00:02:04 - 00:02:08] We might decide to model that as a dissipator
[00:02:08 - 00:02:09] with single-energy port.
[00:02:09 - 00:02:13] In reality, it is turning the electrical energy into heat energy.
[00:02:13 - 00:02:15] So you could have it as a two-port element
[00:02:15 - 00:02:17] with electrical energy in and thermal energy coming out.
[00:02:17 - 00:02:19] And it really just depends on your intense
[00:02:19 - 00:02:20] with the modeling.
[00:02:20 - 00:02:22] If you're modeling it as a resistor and a circuit,
[00:02:22 - 00:02:25] where obviously, it limits current,
[00:02:25 - 00:02:26] as a voltage dropover,
[00:02:26 - 00:02:28] we don't really care about the thermal behavior.
[00:02:28 - 00:02:31] If we're modeling it as a heating element
[00:02:31 - 00:02:33] and a kettle or something like that,
[00:02:33 - 00:02:36] the thermal output is an important part of that.
[00:02:36 - 00:02:39] And so, it depends on our modeling choices
[00:02:39 - 00:02:41] dictate how we look at some of these things.
[00:02:42 - 00:02:43] So looking at the single-port elements,
[00:02:43 - 00:02:45] we talked about last week.
[00:02:45 - 00:02:47] We've got the energy domains down the left
[00:02:47 - 00:02:50] and you can see we've got the potential and flow.
[00:02:50 - 00:02:55] And so you'll recall potential is the conjugate power
[00:02:56 - 00:03:01] variable, energy variable that's measured across a component.
[00:03:02 - 00:03:06] So the easy ones to think of really with that
[00:03:06 - 00:03:07] as the electrical system, right?
[00:03:07 - 00:03:09] So your measure voltage across a component
[00:03:09 - 00:03:12] and then flow is the conjugate variable
[00:03:12 - 00:03:13] that you measure through.
[00:03:13 - 00:03:16] So that is current and the electrical sense.
[00:03:16 - 00:03:21] But we have the analogous power variables on that table
[00:03:24 - 00:03:27] and so you can see other relationships between them.
[00:03:27 - 00:03:29] And so we have potential and flow.
[00:03:29 - 00:03:31] So the two energy variables.
[00:03:32 - 00:03:34] And then we have the single-point elements
[00:03:34 - 00:03:35] we talked about last week.
[00:03:35 - 00:03:39] So dissipator stores and also we head.
[00:03:39 - 00:03:41] So flow stores, potential stores,
[00:03:41 - 00:03:43] we also head flow and potential sources, right?
[00:03:43 - 00:03:46] So that allows us to make up these circuits.
[00:03:48 - 00:03:50] So that's, we got to the,
[00:03:50 - 00:03:53] and we also then talked about having elements,
[00:03:53 - 00:03:55] these single-port elements and series in parallel.
[00:03:55 - 00:03:57] And it behaves just the same way
[00:03:57 - 00:04:00] as for an electrical circuit.
[00:04:00 - 00:04:04] And what that all leads down to is we can define
[00:04:04 - 00:04:06] continuity equations and compatibility equations
[00:04:06 - 00:04:09] for each of these which are a generalization
[00:04:09 - 00:04:12] of what you use in electric circuits.
[00:04:12 - 00:04:15] So Kirchhoff's current law is continuity,
[00:04:15 - 00:04:18] which basically means the current can't go anywhere
[00:04:18 - 00:04:20] if it comes into a component
[00:04:20 - 00:04:23] that goes out of that component and compatibility,
[00:04:23 - 00:04:28] which is essentially KVL or conservation of energy.
[00:04:28 - 00:04:31] So around a closed loop, there are some to zero.
[00:04:31 - 00:04:32] And so we have that principle
[00:04:32 - 00:04:34] but more broadly than just in electric circuits
[00:04:34 - 00:04:37] and in a rotational mechanical translation
[00:04:37 - 00:04:39] of a chemical thermal, all of these
[00:04:39 - 00:04:41] which we can draw up like this.
[00:04:41 - 00:04:43] And these principles remain.
[00:04:45 - 00:04:46] So then we just did an example
[00:04:46 - 00:04:49] with our hands of a mass spring damper
[00:04:49 - 00:04:53] and then showed how you can basically draw
[00:04:53 - 00:04:55] a electric circuit and we can analyze it the same way.
[00:04:55 - 00:04:58] So using KCL in this case,
[00:04:58 - 00:05:01] you end up with an equivalent form
[00:05:01 - 00:05:04] of the dynamic equations that you would otherwise get
[00:05:04 - 00:05:08] if you did this, the way that you do it in 202 and 203.
[00:05:08 - 00:05:13] And then you would have built one of these during the tutorial
[00:05:14 - 00:05:16] when you did that other yesterday or another day.
[00:05:16 - 00:05:18] So I don't need to show that example.
[00:05:18 - 00:05:19] What we'll move into today
[00:05:19 - 00:05:21] is this idea of multiple elements,
[00:05:21 - 00:05:24] which is an actual extension really.
[00:05:24 - 00:05:26] Single-port elements can be used to model range of things
[00:05:26 - 00:05:30] that if they can't model energy manipulation.
[00:05:30 - 00:05:33] And so that's what these multiple elements are for.
[00:05:33 - 00:05:36] What I might do is just make a note here
[00:05:36 - 00:05:41] that says the decision to use single-port elements
[00:05:41 - 00:05:44] just comes down to what is our intent with the modeling.
[00:05:46 - 00:07:35] And so described in that example before.
[00:07:35 - 00:07:40] Okay, so just graduating what I said before.
[00:07:40 - 00:07:42] Sometimes we might choose to model something
[00:07:42 - 00:07:44] as a single-port element because we don't care about,
[00:07:44 - 00:07:49] say the thermal energy or if we are trying to model
[00:07:49 - 00:07:51] a nature heater, for example,
[00:07:51 - 00:07:53] then the thermal energy is quite important.
[00:07:53 - 00:07:56] So we might want to model that as a two-port element
[00:07:56 - 00:07:57] in that instance, right?
[00:07:59 - 00:08:01] So, but the thing is,
[00:08:01 - 00:08:03] single-port elements basically ignore
[00:08:03 - 00:08:05] any energy transformation that occurs.
[00:08:06 - 00:08:10] And so they don't allow coupling between domains.
[00:08:10 - 00:08:13] So if we want these two-port elements,
[00:08:13 - 00:08:18] which allow us to basically manipulate energy,
[00:08:19 - 00:08:21] they then can't couple domains.
[00:08:22 - 00:08:26] And so, I've mentioned this before,
[00:08:26 - 00:08:27] but maybe someone can remind me
[00:08:27 - 00:08:29] what might be some of these transformers
[00:08:29 - 00:08:31] or couple of these two-port elements
[00:08:31 - 00:08:45] that we could use in our models.
[00:08:45 - 00:08:46] So they take energy from one domain
[00:08:46 - 00:08:48] and convert it into another domain.
[00:08:48 - 00:08:50] You want to use one yesterday in the tutorial?
[00:08:50 - 00:08:52] Yep, so this is a motor, for example.
[00:08:55 - 00:08:57] And that takes electrical energy in
[00:08:57 - 00:08:59] the outputs, rotational mechanical energy.
[00:08:59 - 00:09:03] Deci-motor, a generator on the other side, right?
[00:09:03 - 00:09:04] Takes an mechanical energy
[00:09:04 - 00:09:07] and it converts that into electrical energy.
[00:09:07 - 00:09:09] What else might be an example?
[00:09:10 - 00:09:11] Sorry.
[00:09:11 - 00:09:18] So, heating element, yep.
[00:09:18 - 00:09:19] Yes, you know.
[00:09:20 - 00:09:22] Remember it doesn't have to be between domains
[00:09:22 - 00:09:25] so it can transform energy within the same domain.
[00:09:25 - 00:09:27] So you want to use one of those yesterday as well.
[00:09:29 - 00:09:30] So, you know, a recompinance,
[00:09:30 - 00:09:33] but that does convert between the mechanical domains
[00:09:33 - 00:09:34] but absolutely.
[00:09:39 - 00:09:40] So that converts between rotational
[00:09:40 - 00:09:45] and translational mechanical, yeah, gearbox, right?
[00:09:45 - 00:09:48] So gearbox takes in rotational mechanical energy
[00:09:48 - 00:09:50] and outputs rotational mechanical energy,
[00:09:50 - 00:09:52] but you've got a relationship, a different relationship
[00:09:52 - 00:09:56] between the angle of velocity and the torque.
[00:09:57 - 00:10:01] What's the electrical equivalent of a gearbox?
[00:10:01 - 00:10:05] Yes, I'll transform it.
[00:10:05 - 00:10:07] So we've got all these sorts of things
[00:10:07 - 00:10:10] which can be a triple element
[00:10:10 - 00:10:12] which transform energy between the domains
[00:10:12 - 00:10:16] and then that allows the whole multi-domain modeling
[00:10:16 - 00:10:19] sort of aspect.
[00:10:19 - 00:10:22] So with a mechanical gearbox, as an example,
[00:10:24 - 00:10:29] we've got a system
[00:10:29 - 00:10:36] or just treated as a black box, really.
[00:10:36 - 00:10:37] So that's got an input shaft
[00:10:37 - 00:10:39] and it's got an output shaft here.
[00:10:42 - 00:10:45] And so there's torque on one side
[00:10:45 - 00:10:47] and omega on one side
[00:10:47 - 00:10:49] and there's torque on the other side
[00:10:49 - 00:10:51] and omega on the other side.
[00:10:55 - 00:10:56] So it's a two-point element.
[00:10:56 - 00:10:58] So it's got two power variables.
[00:10:58 - 00:10:59] So with the one-port element,
[00:10:59 - 00:11:02] we had just that single power variable
[00:11:02 - 00:11:05] but two-port have got two, so power on the input side
[00:11:05 - 00:11:07] and power on the output side.
[00:11:07 - 00:11:09] It has a constitutive relationship.
[00:11:09 - 00:11:11] And so for a gearbox,
[00:11:11 - 00:11:13] you have this sort of relationship here.
[00:11:13 - 00:11:16] So torque one over torque two is equal to omega two over omega one.
[00:11:16 - 00:11:20] So that means if torque two increases with respect
[00:11:20 - 00:11:25] to torque one, then the omega two will drop
[00:11:25 - 00:11:27] with respect to omega one
[00:11:27 - 00:11:30] and that captures the gear ratio.
[00:11:30 - 00:11:32] And then we can look at the power.
[00:11:32 - 00:11:33] So this is port one here.
[00:11:34 - 00:11:36] This is port two over here.
[00:11:37 - 00:11:39] The power up-port one.
[00:11:39 - 00:11:42] So P one is equal to torque times omega on that side
[00:11:42 - 00:11:47] and P two on the other side is equal to torque times omega.
[00:11:47 - 00:11:50] And so for an ideal situation,
[00:11:50 - 00:11:53] what can we say about the power
[00:11:53 - 00:11:55] and the port one and power port two?
[00:11:56 - 00:11:57] It's the same, right?
[00:11:57 - 00:12:01] In reality, we possibly could model this
[00:12:01 - 00:12:03] depending again what we wanted to do
[00:12:03 - 00:12:05] if we wanted to make it more accurate.
[00:12:05 - 00:12:08] We could possibly say power,
[00:12:08 - 00:12:09] we could have a third port if you like.
[00:12:09 - 00:12:11] You could have a third port
[00:12:11 - 00:12:14] because you might have some thermal energy
[00:12:14 - 00:12:16] coming out of a gearbox.
[00:12:16 - 00:12:18] Is it heats up as it's transmitting the power?
[00:12:18 - 00:12:23] And you could go down these ways, but typically we don't need to.
[00:12:24 - 00:12:37] But for the ideal assumption, P one of T is equal to P two of T.
[00:12:45 - 00:12:48] And so right in the earlier case more thoroughly,
[00:12:48 - 00:12:51] or more fully, we've got torque one times omega one,
[00:12:51 - 00:12:54] torque two times omega two.
[00:12:54 - 00:12:57] So the gearbox is a transformer of mechanical energy.
[00:12:59 - 00:13:08] It's conservation power for the ideal example.
[00:13:10 - 00:13:16] Assumption, so.
[00:13:16 - 00:13:18] And so then, as I said earlier,
[00:13:18 - 00:13:21] electrical transformers behave analogously to that.
[00:13:23 - 00:13:26] And so we already know that,
[00:13:26 - 00:13:31] we've seen the kind of considered equations before.
[00:13:31 - 00:13:36] Also, we've seen the torque one of the torque two,
[00:13:37 - 00:13:42] it was omega two over omega one type relationship.
[00:13:42 - 00:13:45] But we can also write that another way.
[00:13:46 - 00:13:49] Just make a note here that's ideal.
[00:13:49 - 00:13:51] An ideal two-port element,
[00:13:51 - 00:13:53] can you can write the constituent relationship
[00:13:53 - 00:13:55] and have metrics or vector form.
[00:13:56 - 00:13:59] So we've got potential one, flow one,
[00:14:01 - 00:14:11] is equal to some metrics, potential two, flow two.
[00:14:13 - 00:14:18] So it'll just remind potential, flow.
[00:14:19 - 00:14:22] So this is general to any two-port element.
[00:14:23 - 00:14:38] And so for a transformer or for a gearbox, for example,
[00:14:38 - 00:14:42] we would have something like this, p one, flow one,
[00:14:43 - 00:14:48] is equal to in zero zero, one over in,
[00:14:53 - 00:14:55] p two, f two.
[00:14:55 - 00:14:58] So you can write that out basically what we end up with there
[00:14:58 - 00:15:02] is like p one is equal to in times p two.
[00:15:04 - 00:15:07] And f one is equal to one over in times f two.
[00:15:08 - 00:15:15] And so that might be so the potential side then would be,
[00:15:18 - 00:15:21] for a rotational mechanical omega,
[00:15:21 - 00:15:24] omega one is equal to in times omega two.
[00:15:24 - 00:15:27] And then torque one is equal to one over in times talk two,
[00:15:27 - 00:15:28] for example.
[00:15:29 - 00:15:32] So we can put that in this matrix one.
[00:15:33 - 00:15:41] So we've got the idea,
[00:15:41 - 00:15:43] does everyone know how heavy is idea of these two-port elements?
[00:15:43 - 00:15:44] Right?
[00:15:44 - 00:15:48] And so we can then use those to couple these domains.
[00:15:48 - 00:15:52] So as we saw, you know, we can connect the single-port elements.
[00:15:53 - 00:15:56] And the earlier examples, we can add these two-port elements into the mix.
[00:15:56 - 00:16:02] And they behave like a dissipator on one side and a source on the other side.
[00:16:02 - 00:16:05] So it removes energy from one domain and it injects
[00:16:05 - 00:16:07] to the other domain.
[00:16:07 - 00:16:08] So I've got an example here.
[00:16:08 - 00:16:10] This is just a purely electric circuit,
[00:16:10 - 00:16:12] but we've got an ideal transformer here.
[00:16:13 - 00:16:19] And what we can see is our deal transformer behaves like a dissipator on this side.
[00:16:21 - 00:16:24] And it behaves like a source on this side.
[00:16:25 - 00:16:26] And then we can see.
[00:16:26 - 00:16:32] So what we can see we've got a resistive here as a dissipator.
[00:16:32 - 00:16:35] And we've got a capacitor that's a source.
[00:16:36 - 00:16:46] And then we've got the transformer, which behaves like that couple zoos to
[00:16:47 - 00:16:49] separate parts of that domain.
[00:16:50 - 00:16:52] And it behaves as a dissipator and a source.
[00:16:54 - 00:16:59] So as you would have used yesterday,
[00:16:59 - 00:17:01] you would have used a DC motor, for example.
[00:17:01 - 00:17:05] And so that couple is the electrical and the retational mechanical domain.
[00:17:06 - 00:17:11] You can obviously understand a transformer, a gearbox,
[00:17:11 - 00:17:12] does the same sort of thing.
[00:17:14 - 00:17:18] You other options that you might have if using SIMScape
[00:17:18 - 00:17:21] is something like a double-acting hydraulic cylinder.
[00:17:22 - 00:17:25] This thing called a dry raiser, which is
[00:17:27 - 00:17:28] it's a theoretical thing.
[00:17:28 - 00:17:30] It's like half a transformer, basically.
[00:17:30 - 00:17:33] But we're not really, you're not going to,
[00:17:33 - 00:17:38] it's available because it may be of interest to people doing maths
[00:17:38 - 00:17:39] with the sort of stuff.
[00:17:39 - 00:17:43] But it's not something, if you connect through dry raisers together,
[00:17:43 - 00:17:45] that basically makes an electrical transformer.
[00:17:49 - 00:17:52] OK, so I had a couple of, got a couple of examples here,
[00:17:52 - 00:17:56] which I can run quickly, to show you.
[00:17:56 - 00:18:00] Obviously you've already seen a mess spring damper and that sort of thing.
[00:18:01 - 00:18:08] OK, how's the best way to make this work?
[00:18:08 - 00:18:15] So there's some examples, these are just some built-in examples from
[00:18:15 - 00:18:22] SIMScape, but more specifically, they're from
[00:18:22 - 00:18:25] SIMScape multi-body.
[00:18:25 - 00:18:30] I'm just trying to make sure I have the right ones.
[00:18:40 - 00:18:53] See, this is tiny.
[00:18:53 - 00:18:54] So what this model is?
[00:18:55 - 00:18:59] So SIMScape is what you played with yesterday in the lab.
[00:18:59 - 00:19:01] And it's one dimensional, right?
[00:19:01 - 00:19:06] So you have time, but there was no real spatial dimensions in that.
[00:19:06 - 00:19:08] So you could, I mean, you could plot against x or anything,
[00:19:08 - 00:19:11] but there was no, it's not working in three spaces.
[00:19:11 - 00:19:13] There's just one spatial dimension.
[00:19:13 - 00:19:18] If you want some model stuff with three spatial dimensions
[00:19:18 - 00:19:21] being able to move around space, there's an extension to SIMScape
[00:19:21 - 00:19:23] and that's called SIMScape multi-body.
[00:19:23 - 00:19:30] And what that largely brings in is a lot of these frame
[00:19:30 - 00:19:32] transformations and joints.
[00:19:32 - 00:19:37] So it starts to, like these, and I am trying to slowly extend
[00:19:37 - 00:19:40] that tutorial to include some of this, but I haven't got it yet.
[00:19:40 - 00:19:45] A few take in MT4H2 and X-TIA robotics and the industrial
[00:19:45 - 00:19:46] manipulators part.
[00:19:46 - 00:19:48] This will start to make a lot more sense because we talk a lot about frame
[00:19:48 - 00:19:49] transforms.
[00:19:49 - 00:19:51] We talk a lot about real and prismatic joints.
[00:19:51 - 00:19:56] But by doing this, then we can simulate stuff in three space.
[00:19:56 - 00:20:07] And so if I run that and then try and find where that
[00:20:07 - 00:20:10] the sky is, right?
[00:20:10 - 00:20:14] So this, here we go.
[00:20:14 - 00:20:22] And so this is a double pendulum that's what their model was before.
[00:20:22 - 00:20:30] But it's on struggling because to go to the screen, I have to go off that
[00:20:30 - 00:20:31] side of mine.
[00:20:31 - 00:20:34] If you do not that side.
[00:20:34 - 00:20:35] And it causes issues.
[00:20:35 - 00:20:39] But these, so you can start to get the dynamics of it.
[00:20:39 - 00:20:48] There's another example here.
[00:20:48 - 00:21:06] So this one is a model of a aircraft landing gear and on work.
[00:21:06 - 00:21:15] So you can build up quite complicated models and have them
[00:21:15 - 00:21:19] actuated and then do a lot of this testing that you might want or
[00:21:19 - 00:21:25] optimization for design.
[00:21:25 - 00:21:26] If we open this up and have a look.
[00:21:26 - 00:21:31] So this is a model that they were using for there.
[00:21:31 - 00:21:36] There's obviously there's a controller inside that you can
[00:21:36 - 00:21:36] say.
[00:21:36 - 00:21:39] So the other thing is when you're using some skip multi body,
[00:21:39 - 00:21:44] you can just import step files from CAD and then connect them.
[00:21:44 - 00:21:46] So you can make them look quite nice.
[00:21:46 - 00:21:50] But again, there's a lot of frame transformations to make things
[00:21:50 - 00:21:54] that are make sure things are and they relate to each other
[00:21:54 - 00:21:55] other right and then you have joints.
[00:21:55 - 00:21:58] They always rotate around the z axis and all sorts of stuff like
[00:21:58 - 00:21:59] that.
[00:21:59 - 00:22:03] So there's a lot of capability within that software and we're
[00:22:03 - 00:22:05] really just scratching the surface of it.
[00:22:05 - 00:22:08] But it is something that depending on who you go and work for
[00:22:08 - 00:22:13] later, you might start to be exposed to a tremble and
[00:22:13 - 00:22:19] town use it when they're modeling some agricultural hardware that
[00:22:19 - 00:22:22] they are automating for example.
[00:22:22 - 00:22:27] Let's probably add.
[00:22:27 - 00:22:35] And so it's something that you just want to have some
[00:22:35 - 00:22:38] appreciation for and understand that it can be useful.
[00:22:38 - 00:22:43] I mentioned to a couple of students yesterday in the tutorial as
[00:22:43 - 00:22:44] well.
[00:22:44 - 00:22:47] During the last, I think last lecture I said that with the
[00:22:47 - 00:22:51] 303 apparatus because I think you start doing the 303 labs
[00:22:51 - 00:22:57] next week, I'd say that Ronni had fixed the motor amplifiers so
[00:22:57 - 00:22:59] they don't have this issue anymore.
[00:22:59 - 00:23:03] So how many people used today if you looked, I think if you
[00:23:03 - 00:23:05] followed it through, you could see that the controller was
[00:23:05 - 00:23:10] trying to drive quite an aggressive control strategy and then
[00:23:10 - 00:23:14] you could see that once it was saturated and the slew rate
[00:23:14 - 00:23:18] limit was applied, the actual motor couldn't keep up with
[00:23:18 - 00:23:23] when I said Ronni had fixed the motor controller on those
[00:23:23 - 00:23:26] rags, actually one of them is fixed, one of them is still
[00:23:26 - 00:23:28] slow like that.
[00:23:28 - 00:23:30] And I don't know, I don't recall which ones to work.
[00:23:30 - 00:23:33] So depending on which one you're on, you might find that
[00:23:33 - 00:23:38] it behaves really nicely and like your analytic model or you
[00:23:38 - 00:23:42] might find that you've selected gains and you've simulated it
[00:23:42 - 00:23:45] and it doesn't behave much like that and what you're seeing
[00:23:45 - 00:23:49] there is probably that you've got the one with the older
[00:23:49 - 00:23:52] motor controller which has got the slew rate limitations
[00:23:52 - 00:23:54] and what you're seeing is what your model deals today.
[00:23:54 - 00:23:58] And so there is an opportunity that you can kind of see the
[00:23:58 - 00:24:03] difference between these two motor controllers and these
[00:24:03 - 00:24:08] this multi-domain model or physical systems modeling is quite nice.
[00:24:08 - 00:24:10] You can start to think about how would you use that in design?
[00:24:10 - 00:24:14] You know you might be in a situation where you've got some options on
[00:24:14 - 00:24:17] motors and motor drivers which ones you choose,
[00:24:17 - 00:24:21] you'll have some lifetime considerations sort of then with
[00:24:21 - 00:24:24] considerations and other things and you can start to simulate and
[00:24:24 - 00:24:27] find out which one would do the job as opposed to buying a
[00:24:27 - 00:24:30] couple and testing them and figuring it out.
[00:24:30 - 00:24:38] Right, so these give you some power to do that in the design process.
[00:24:38 - 00:24:42] Good, see any questions at this point?
[00:24:42 - 00:24:44] No, good. All right.
[00:24:44 - 00:24:48] So I'm just going to walk through basically the process if you were to construct
[00:24:48 - 00:24:53] one of these models. Largely you know you walked through it yesterday
[00:24:53 - 00:24:57] in the or when you've done that tutorial but
[00:24:57 - 00:25:02] it's nice to sort of draw it out consistently.
[00:25:02 - 00:25:04] Right, so the first thing you need to do is if you've got your system,
[00:25:04 - 00:25:08] you identify all the basic elements and so you dissipate as your stores,
[00:25:08 - 00:25:12] your sources and your multiple elements. And so for this
[00:25:12 - 00:25:16] example, if we've got a mass spring damper type system,
[00:25:16 - 00:25:23] we would have a source, we've probably got some resistance on the
[00:25:23 - 00:25:32] motor, on the coils, we've got some inductance
[00:25:32 - 00:25:48] and then this motor goes through, it's got some inertia
[00:25:48 - 00:26:02] rotational torsion spring and perhaps some damping.
[00:26:02 - 00:26:06] Right, so we've got K and C. And so
[00:26:06 - 00:26:09] in here, what have we got in terms of what
[00:26:09 - 00:26:18] dissipators have we got? Yep, so the resistors of dissipator, is there anything else?
[00:26:18 - 00:26:28] The dampup from the rotational mechanical side, right?
[00:26:28 - 00:26:34] We've got some stores in that the inductor is a store, the spring is a store
[00:26:34 - 00:26:39] and the inertia is a store and then here
[00:26:39 - 00:26:44] we've got our multi-port element with the DC motor
[00:26:44 - 00:26:53] and we've got a source, electrical source, right?
[00:26:53 - 00:26:57] And so then once we've identified those, we can start to
[00:26:57 - 00:27:01] start to keep them up. We need to identify a reference potential in each
[00:27:01 - 00:27:04] domain, so you would have had to do that yesterday, there is an electrical
[00:27:04 - 00:27:07] reference, a rotational mechanical reference, a translational
[00:27:07 - 00:27:14] mechanical reference, so each domain needs a reference.
[00:27:15 - 00:27:19] So let me, I'll just go back to this rather than redrawing it right.
[00:27:19 - 00:27:30] So we've got an electrical reference here and
[00:27:30 - 00:27:34] here we've got a rotational mechanical reference,
[00:27:34 - 00:27:38] so every domain needs that.
[00:27:38 - 00:27:42] And so what that means is in this case that's V is equal to zero for the
[00:27:42 - 00:27:46] electrical reference and in the mechanical domain
[00:27:46 - 00:27:50] that means omega is equal to zero, right? So that's that point where
[00:27:50 - 00:28:14] the potential is equal to zero. So the next part then
[00:28:14 - 00:28:19] is we might want to identify the nodes in the system
[00:28:19 - 00:28:24] and then those are all the points where there is common potential, right?
[00:28:24 - 00:28:28] And so it's pretty simple with the electrical system.
[00:28:28 - 00:28:37] Maybe I need to redraw it. We've got a resistor, we've got our inductor,
[00:28:37 - 00:28:56] we've got our DC motor here, our reference, and our rotational
[00:28:56 - 00:29:09] uh, reference. So we're our nodes.
[00:29:09 - 00:29:15] So we've got a node here that's our ground node. There's a node here, there's a node here,
[00:29:15 - 00:29:23] there's a node here, one, two, three, zero.
[00:29:23 - 00:29:27] This is a ground node here, we'll call it node A,
[00:29:27 - 00:29:31] because we're in a different domain and then we've got another node here,
[00:29:31 - 00:29:37] node B. And so they've got the same potential. So they've all got the same
[00:29:37 - 00:30:03] rotational or angular velocity. So then the next step is we can connect that up
[00:30:04 - 00:30:09] like an electric circuit. We'll draw that up like an electric circuit.
[00:30:13 - 00:30:16] Oh look, that's handy. I can have a picture of it over there.
[00:30:16 - 00:30:21] So we can redraw this now in a more sort of conventional form. So again,
[00:30:21 - 00:30:26] we've got our voltage, we've got our resistor, we've got our inductor.
[00:30:42 - 00:30:49] Now that DC motor behaves like a dissipator from the electrical side, but it's going to behave
[00:30:49 - 00:30:56] like a current source, so like a flow source of torque and the, and the rotation on a
[00:30:56 - 00:31:01] mechanical side. Right. And so that's where it's going to be a little bit different draw in the
[00:31:01 - 00:31:10] side, like a electric circuit rather than on the electrical side, which is pretty natural
[00:31:10 - 00:31:52] to begin with. So that's supposed to be at home again, the voltage across it and talk.
[00:32:08 - 00:32:13] Right. So we end up with what looks like much more like an electric circuit.
[00:32:15 - 00:32:24] And then we need to next step in as we indicate the direction of flow and the polarity of
[00:32:24 - 00:32:28] the potential. So I might just go back to this. So I don't have to redraw it again.
[00:32:29 - 00:32:41] And so I'm going to say the direct direction of flow. So it's just like assuming a current direction
[00:32:43 - 00:32:58] and polarity of potential. So we've got the flow and we'll have voltage across the resistor,
[00:32:58 - 00:33:03] we end up with some voltage across our inductor, some voltage across our motor,
[00:33:03 - 00:33:10] then we end up with voltage. So again, potential is omega and the rotation of mechanical sense.
[00:33:10 - 00:33:23] So that's omega m there. And we've got torque m behaving like flow. And then we've got
[00:33:24 - 00:33:39] torque minus minus minus. So we've got torque over the damper, torque over the spring.
[00:33:40 - 00:34:00] And then torque over the inertia or through the inertia through those. So not over,
[00:34:03 - 00:34:16] through. And you've got the same omega because they're in parallel.
[00:34:18 - 00:34:22] Right. So we've got there and it's behaving like an electric circuit.
[00:34:23 - 00:34:36] And then we can basically apply any standard circuit analysis tool that you might want.
[00:34:39 - 00:34:44] So you could use no analysis. You could use mission analysis. You could do equivalent circuits.
[00:34:45 - 00:34:57] Anything like that. And so you might choose niche KVL type analysis in the electrical domain.
[00:34:58 - 00:35:19] And so you might then sort around here. I'm not going to reach all the circuit. But if you go
[00:35:19 - 00:35:30] around that loop, then the sum of the voltages has to equal zero. See, end up with the voltage source
[00:35:31 - 00:35:38] is equal to the voltage across the resistor plus the voltage across the inductor plus the voltage
[00:35:38 - 00:35:46] across the motor. And then you can use a constitutive equation. So the current to the resistor
[00:35:47 - 00:36:02] plus L dr by dt for the inductor plus K omega m for such one of the
[00:36:03 - 00:36:13] constitutive or coupling relationships for the DC motor. So that comes from back to mf for a motor.
[00:36:13 - 00:36:27] So the or Vb is equal to K times omega m. And on the other side, we also have talk for the motor
[00:36:27 - 00:36:42] is equal to K times I. So that's the motor constant. And so then we've got an equation
[00:36:43 - 00:36:49] for our electrical side that you can see that that's starting to couple into the mechanical side
[00:36:49 - 00:36:55] because we've got one of the mechanical variables. Only m has appeared in the electrical equation.
[00:36:59 - 00:37:07] Is any questions about that? Good. So then you do the same to on the mechanical side.
[00:37:07 - 00:37:17] So on the mechanical side, we might use no analysis or KCL. The current law
[00:37:21 - 00:37:29] um so just re resketching the mechanical side of things. We've got talk.
[00:37:57 - 00:38:02] So we've only got two nodes here. So we've got node B I think and we had node A.
[00:38:05 - 00:38:12] And so we can just use some occurrence and some occurrence and to node A as equal to zero.
[00:38:15 - 00:38:26] So we've got talk from the motor has to equal the talk into the inertia plus the talk to the spring
[00:38:27 - 00:38:36] plus the talk to the damper. Now we know that the motor talk from the equation I just showed you
[00:38:36 - 00:38:49] before is equal to K times I. I being the electrical current. The talk ends the inertia is equal
[00:38:49 - 00:38:57] to J obviously theta double dot that's what you used to. But since we're using omega that's J omega dot.
[00:38:58 - 00:39:12] So J d omega by dt. Talk on the spring is equal to K times theta which is therefore equal to
[00:39:12 - 00:39:30] spring K. K times integral of omega dt. And the talk to the damper is equal to C times omega.
[00:39:34 - 00:39:39] So from each side of that we end up with this equation and equation.
[00:39:44 - 00:39:55] So we had the one that we had from the electrical side which was VS is equal to
[00:39:56 - 00:40:11] l d i by dt plus r i plus K omega. And on the mechanical side we've got
[00:40:12 - 00:40:47] K i is equal to J d omega by dt plus K. So what we end up with there is these two coupled equations
[00:41:10 - 00:41:18] and the coupling occurs because we've got, I should say all right K m there and all right K m
[00:41:18 - 00:41:25] there so it's motor is a place to spring. This is how the coupling occurs. We see a term that
[00:41:25 - 00:41:30] relates to the mechanical domain within the electrical equation and we see a term that relates the
[00:41:30 - 00:41:36] electrical domain within the mechanical equation. So I'll just note now this is just for
[00:41:36 - 00:41:42] illustrative purposes. I'm absolutely not going to ask you in the exam or anything to derive one
[00:41:42 - 00:41:48] of these equations. Let's just see you can see what's happening behind the scenes. So when you draw
[00:41:48 - 00:41:53] one of these in Cinscape this is what MATLAB or Cinscape, a similar link is doing in the background.
[00:41:53 - 00:42:01] It's got these equations for each of the potentials and flows for each of the elements and
[00:42:01 - 00:42:08] it assembles them into the differential algebraic equations which is here which should then go
[00:42:08 - 00:42:13] through and solve those numerically and that's how you get out those simulation results.
[00:42:14 - 00:42:20] So kind of understand how this is happening, what's happening here but I don't expect you to
[00:42:20 - 00:42:26] remember this or repeat this for the exam. It's just so you know what's happening under the hood
[00:42:26 - 00:42:34] when you do this modeling. So just to reiterate that process you identify all the basic elements
[00:42:34 - 00:42:40] in the system, you identify the reference potentials in the domain, then to analyze it, you need
[00:42:40 - 00:42:45] to identify all the nodes, you connect your system or like electrical circuits, indicate your directions
[00:42:46 - 00:42:51] and flows, so your directions and potentials and then your placenta circuit analysis.
[00:42:52 - 00:42:59] In terms of actually building the model in something like Cinscape you do this and
[00:43:02 - 00:43:05] basically that's right then that does the rest for you.
[00:43:07 - 00:43:12] But you need to identify what your elements are and then be able to use those
[00:43:12 - 00:43:16] and connect them up and use the tools and stuff like that. Is there any questions about that?
[00:43:19 - 00:43:24] So there's now you've got an understanding like I think what is nice is you've done dynamics
[00:43:24 - 00:43:28] and two or three and you've done dynamics and three or three you know how to analyze that.
[00:43:29 - 00:43:32] When you get some software like this it seems a little bit like magic because you just
[00:43:32 - 00:43:35] connect your up and it does it but what's happening underneath is it is just assembling
[00:43:36 - 00:43:43] these equations using the fact that energy is just transformed between domains and
[00:43:44 - 00:43:49] and that provides a relationship when we've got these couplers like DC motors and whatever else between
[00:43:49 - 00:43:54] domains then it sets up these equations and then it just solves them numerically.
[00:43:54 - 00:44:00] And the fact that it's solving them numerically is what gives it both makes it powerful but it also
[00:44:00 - 00:44:05] means you know sometimes you have to be careful about what solvers you're using because
[00:44:07 - 00:44:11] it's powerful because it's numerical therefore you can do stuff that's non-linear like having
[00:44:11 - 00:44:15] saturations and having slew rate limits and having hard stops and stuff like that
[00:44:16 - 00:44:22] and having non-viscous friction but sometimes when you first do it you might find you get a
[00:44:22 - 00:44:27] solution that's a bit rubbish and then you have to go back and change the solverside to solver that
[00:44:27 - 00:44:34] can cope with you know the system that you've set up for example but typically you know if you run
[00:44:34 - 00:44:44] into issues like that and you've got that software it's you know there's documentation that helps
[00:44:44 - 00:44:52] you with that sort of thing that's not optional you've done it used to be optional but this is
[00:44:52 - 00:45:01] saying the same thing right what it means for physical systems and you know with numerical stuff
[00:45:02 - 00:45:07] you know using Python or any of those sometimes it used only 45 for standard second order
[00:45:07 - 00:45:11] differential equation for physical systems you have to be able to we have to use only
[00:45:11 - 00:45:18] solvers that are for stiff systems that's not stiff in terms of it's a stiff spring it means that
[00:45:19 - 00:45:24] it's a mathematical term in terms of how the system behaves and there's particular solvers that
[00:45:24 - 00:45:30] work for that but similarly it's pretty good at selecting those so it's just something to put
[00:45:30 - 00:45:35] attention to you know that's the end of that said lectures on the physical modeling stuff
[00:45:37 - 00:45:41] yeah if you've got any questions feel free to come up and ask otherwise for next
[00:45:42 - 00:45:48] tomorrow we start talking a little bit about the penability and things like
[00:45:49 - 00:45:53] redundancy and stuff and design and that sort of thing next week
[00:45:54 - 00:46:02] yeah next week in the following week we've got a few we've got and it's on the schedule
[00:46:02 - 00:46:09] but I'll send out learn reminders Dominique will be back to talk the second part about writing
[00:46:10 - 00:46:15] the following week she'll be talking about teamwork competencies and I will encourage everyone to come
[00:46:15 - 00:46:23] to that because when you're working groups sometimes it's good to have some skills in your tool box
[00:46:23 - 00:46:30] to help get a hit of any potential issues that might occur and so there's that's talking about that
[00:46:30 - 00:46:38] and then circle also be talking about fortune analysis and life cycle analysis in the last
[00:46:38 - 00:46:46] week but I will send out some reminders about those before we hit those. Cool otherwise you can go
[00:46:46 - 00:46:49] or if you've got any questions feel free to come up and ask
[00:47:09 - 00:47:18] I guess I guess it would be a bit of an instrument at the same stage. Sure.
[00:47:18 - 00:47:24] So we can then exercise to the model single-card system. That's correct.
[00:47:24 - 00:47:36] Yup. We use that to simulate a graph or the three or three or the last graph using the ID's that we have to handle.
[00:47:36 - 00:47:39] I don't see why not.
[00:47:39 - 00:47:49] It depends on what they ask for, what are they, what are they wanting to do to figure out some games?
[00:47:49 - 00:47:53] Yeah, I think you're probably, you're supposed to know if you're going to have a house or something like that.
[00:47:53 - 00:48:00] So do that on the side, but maybe the thing is, by all means, you use the model and figure out some games,
[00:48:00 - 00:48:04] because it's probably a bit of simulation violence to do that.
[00:48:04 - 00:48:08] The only thing is, I don't really know what friction values are.
[00:48:08 - 00:48:09] I chose some of those.
[00:48:09 - 00:48:17] That's part of the problem and part of the more complicated model you can do.
[00:48:17 - 00:48:22] But in that way, more parameters, it's not a sound value too.
[00:48:22 - 00:48:27] And sometimes, what you could do is on that transitional friction block,
[00:48:27 - 00:48:32] and the viscous friction, put a number that I think you've got given in the layer of sheet of u3,
[00:48:32 - 00:48:36] then you could twirl around with the non-biscous friction numbers,
[00:48:36 - 00:48:40] or just stick in the viscous one, I might not want to zero or something to it.
[00:48:40 - 00:48:41] Yeah.
[00:48:41 - 00:48:42] And that sort of thing.
[00:48:42 - 00:48:44] But I don't see why you shouldn't.
[00:48:44 - 00:48:48] What I'll ask the TAs for sure to double-check.
[00:48:48 - 00:48:49] Yeah.
[00:48:49 - 00:48:51] That's sweet.
[00:48:51 - 00:48:53] And if you might, I mean, it's good to use it, right?
[00:48:53 - 00:48:54] You've made an excuse.
[00:48:54 - 00:48:55] Yeah.
[00:48:55 - 00:49:02] If you hand in the assignment early, are you for the first?
[00:49:02 - 00:49:03] For the CIMS gate?
[00:49:03 - 00:49:04] Yeah.
[00:49:04 - 00:49:13] Can you update it and then re-for the actual due date?
[00:49:13 - 00:49:15] I don't know what I said that to be.
[00:49:15 - 00:49:16] Probably.
[00:49:16 - 00:49:17] Yeah.
[00:49:17 - 00:49:21] I forget, like, it's been sitting there for a few years, and so I forget what the settings are.
[00:49:21 - 00:49:23] I wouldn't be surprised.
[00:49:23 - 00:49:28] What I would say is try an effort, like submit it early,
[00:49:28 - 00:49:31] and then if you go to re-up data and it doesn't work,
[00:49:31 - 00:49:34] flick me an email, and then I can go and change the settings
[00:49:34 - 00:49:35] so that you can update it.
[00:49:35 - 00:49:37] But I have a feeling you should be able to update it.
[00:49:37 - 00:49:38] Sweet.
[00:49:38 - 00:49:39] So you should be fine.
[00:49:39 - 00:49:40] Cool.
[00:49:40 - 00:49:41] Good.
[00:49:41 - 00:49:42] Thank you.
[00:49:42 - 00:49:43] You're all good.

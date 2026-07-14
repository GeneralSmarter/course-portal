# ENMT301-26W Lecture 17 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_17_audio_16k_mono_32k.mp3`
Source audio SHA-256: `6b692b0217b5c6dd65208e85d6a60e2af181bba2432b68e33c6f8008d2433ac0`
Generated: 2026-06-06T05:35:20.743852+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:01:34 - 00:01:41] Okay, I'll go after that.
[00:01:41 - 00:01:55] All right, so today we're going to go into a little bit more detail about physical systems
[00:01:55 - 00:02:02] and this is a little bit more of a model, a little more of a domain model.
[00:02:02 - 00:02:04] It's got a couple of names, which are largely thing, interchangeable.
[00:02:04 - 00:02:14] And so this relates to, just get more scribbly pen, so more multi-domain model.
[00:02:14 - 00:02:20] Because you're modeling a physical system.
[00:02:20 - 00:02:24] And this relates to what you're going to be doing with the tutorial.
[00:02:24 - 00:02:28] Next week in the lab, and then the associated assignment.
[00:02:28 - 00:02:37] It really is more about this mixture today and the full-on lecture.
[00:02:37 - 00:02:39] Next week we'll finish it.
[00:02:39 - 00:02:43] It's a bit more about what's going on under the hood with this.
[00:02:43 - 00:02:46] Just so you've got an understanding of what's going on.
[00:02:46 - 00:02:52] So that's not like, you have to necessarily do this process by hand,
[00:02:52 - 00:02:57] but it gives you some grounding in what's happening underneath these pieces of software.
[00:02:57 - 00:03:02] So it's a bit more of a traditional lecture and it'll work through some stuff.
[00:03:02 - 00:03:11] I'm asking a few questions and stuff, but it's sort of the underpinnings of how these systems are modeled in software and in numerical scenes.
[00:03:11 - 00:03:17] So as yesterday, Cosmo talked about modeling and we're talking about multi-domain of physical systems modeling.
[00:03:17 - 00:03:22] Sort of gene really sits in this area here of the process.
[00:03:22 - 00:03:27] So every time I ask this, I get slightly different answer,
[00:03:27 - 00:03:29] but I presume you've done some finite state models.
[00:03:29 - 00:03:33] You'll understand what finite state models are, probably from 361.
[00:03:33 - 00:03:35] Is that correct?
[00:03:35 - 00:03:37] So they're quite useful.
[00:03:37 - 00:03:44] It's not uncommon to have your robot using a finite state model.
[00:03:44 - 00:03:50] And effectively, you've got discrete states, you know, search state on the pickup weight state.
[00:03:50 - 00:03:52] Return to base state.
[00:03:52 - 00:03:57] And then you've got transition conditions which determine if you move from one state to another.
[00:03:57 - 00:04:00] You might have other things going on underneath.
[00:04:00 - 00:04:08] So that is obviously some form of modeling and it's modeling information systems and how they sort of relate.
[00:04:08 - 00:04:16] If we're talking about physical systems, so then we're talking about dealing with energy rather than information.
[00:04:16 - 00:04:24] And typically in the real world, we have continuous states rather than discrete states.
[00:04:24 - 00:04:26] And that's sort of what we're going to be talking about today.
[00:04:26 - 00:04:34] So it's somewhat unparalleled for what you're doing with 303 and what you would have done in 203 previously.
[00:04:34 - 00:04:38] So, you know, continuous states that change over time.
[00:04:38 - 00:04:40] So it's dynamics.
[00:04:40 - 00:04:47] You might have a displacement and velocity then that change over time.
[00:04:47 - 00:04:57] Depending on the system that your modeling is parameters like its mass, the any stiffness and damping and stuff like that.
[00:04:58 - 00:05:03] And so don't have an analysis, you know, pregnant system down to small elements, you model for first principles,
[00:05:03 - 00:05:07] whatever I'm like you're doing through a through.
[00:05:07 - 00:05:11] And as we've talked about yesterday, we often use lumped parameters for doing that.
[00:05:11 - 00:05:13] So we assume that the masses are point.
[00:05:13 - 00:05:20] And we assume that the spring effectively is a point in the end, take a mean space if you like.
[00:05:20 - 00:05:26] and we have a finite number of state variables.
[00:05:26 - 00:05:28] What is a state variable?
[00:05:28 - 00:05:33] Can someone tell me what I think is state variables?
[00:05:33 - 00:05:35] Do you know what a state variable?
[00:05:35 - 00:05:37] Have you come across that too?
[00:05:37 - 00:05:38] Not yet?
[00:05:38 - 00:05:40] In the 303?
[00:05:40 - 00:05:41] If not.
[00:05:41 - 00:05:55] So a state variable is a state variables more broadly are the state of variables that allow you to provide a complete description of a system.
[00:05:55 - 00:06:00] And typically, you know, coupled first order differential equations.
[00:06:00 - 00:06:04] If you've got that for your system, those end up being a state variable.
[00:06:04 - 00:06:13] So for things like 303, you might have displacement and velocity are the state variables if you're modeling a spring mass damper.
[00:06:13 - 00:06:24] You'll learn more about this in forestry next year because you do a form of dynamic analysis with state space analysis where everything's broken down into your pot.
[00:06:24 - 00:06:29] So the fact of the x dot matrix is equal to a times x matrix.
[00:06:29 - 00:06:31] So those are your variables.
[00:06:31 - 00:06:34] A captures mass stiffness and all that stuff.
[00:06:34 - 00:06:42] x dot captures velocity or displacement velocity and acceleration.
[00:06:42 - 00:06:45] Or x and x dot and those are your state variables.
[00:06:45 - 00:06:49] So anyway, we have a finite number of state variables.
[00:06:49 - 00:06:55] And in doing this, it makes our lives easier as we talk to our easter.
[00:06:55 - 00:06:59] And we also assume some things like linearity and time and variance.
[00:06:59 - 00:07:09] And the way that you currently do this in 303 is you might draw a free body diagram and you do a sum of forces or some of the moments or something.
[00:07:09 - 00:07:14] It was mass times acceleration and you write equations in each domain.
[00:07:14 - 00:07:19] But as we sort of saw yesterday, that's good on an individual domain way.
[00:07:19 - 00:07:28] But if you want to start modeling complicated systems that span multiple energy demands,
[00:07:28 - 00:07:35] it can get a bit difficult doing that sort of from that perspective.
[00:07:35 - 00:07:36] If you like.
[00:07:36 - 00:07:44] And so then we end up with these methods which come about from multi-domain modeling or end up in multi-domain modeling.
[00:07:44 - 00:07:49] And you can generalize across these domains.
[00:07:49 - 00:08:01] Now, interestingly, a lot of these methods as we'll go through you see, you end up with what looks like circuit diagrams, even though they're across multiple domains.
[00:08:01 - 00:08:10] And they yourself them, the way that you solve them, that whole methodology was developed for a electrical engineering quite a long time ago.
[00:08:10 - 00:08:16] And it subsequently being sort of pushed to be used across these energy domains.
[00:08:16 - 00:08:19] So it's originally developed for that.
[00:08:19 - 00:08:22] But we've got these domains that we talked about yesterday.
[00:08:22 - 00:08:28] And so who can remind you what the key unifying concept across all these are domains as.
[00:08:28 - 00:08:35] what links them?
[00:08:35 - 00:08:49] Because there are other ones we talked about, is they're like hydraulic, mamatic, thermal, magnetic, for example.
[00:08:49 - 00:09:00] For looking at all these, what links are altogether?
[00:09:00 - 00:09:08] No, I'm talking about not linearity, because we can end up with nonlinearity in all of them.
[00:09:08 - 00:09:09] Energy.
[00:09:09 - 00:09:10] Yeah.
[00:09:10 - 00:09:12] So all of these are energy-making.
[00:09:12 - 00:09:13] Energy-making.
[00:09:13 - 00:09:17] You have electrical energy, translational mechanical energy, rotation mechanical energy.
[00:09:17 - 00:09:29] And when we go from one to another, so if we go from electrical system through a DC motor to a rotational mechanical system, all we're doing is transferring energy from the electrical side to the rotational mechanical side.
[00:09:29 - 00:09:32] All of these are energy transfer process.
[00:09:32 - 00:09:40] And so that's what lies underneath that energy.
[00:09:40 - 00:09:48] And they also brought up yesterday's energy power, which is basically rate of energy over time.
[00:09:48 - 00:09:56] And then you've got this conjugate power variable, so voltage in currents, force and velocity, angle of velocity and torque.
[00:09:56 - 00:10:07] Those conjugate power variables effectively are what are being converted between domains as we go across.
[00:10:07 - 00:10:16] And so looking at it from a, we're not just looking at an electrical system now, or a translational mechanical system like a spring rest car, or something like that.
[00:10:16 - 00:10:22] All of these are just different forms of energy, and their energy can be transferred between them.
[00:10:22 - 00:10:24] That allows us to couple them and link them.
[00:10:24 - 00:10:29] So we'll look at this to start off with one that you know, right?
[00:10:29 - 00:10:37] So in energy dissipator, now sort of resistor, right?
[00:10:37 - 00:10:42] You need that with plus minus, we've got some voltage over time.
[00:10:42 - 00:10:48] There's some current flowing through it at the time.
[00:10:48 - 00:10:50] Is that an energy dissipator?
[00:10:50 - 00:10:53] Obviously, I wrote it at the other, thinking about it.
[00:10:53 - 00:10:58] Is it getting rid of energy?
[00:10:58 - 00:11:00] Yes, so that's the thing actually.
[00:11:00 - 00:11:02] It's not, and then it's funny the way we model this.
[00:11:02 - 00:11:06] Depending on your view of what you're trying to model,
[00:11:06 - 00:11:12] if we've got this in the electric circuit, and let's just say we're modeling a motor, right?
[00:11:12 - 00:11:18] And it's got some resistance in the, in the coils.
[00:11:18 - 00:11:24] There is dissipating energy from the electrical side of things, and it's turning into heat.
[00:11:24 - 00:11:30] But if we don't care about that heat, like we're not trying to capture the thermal behaviours or anything like that,
[00:11:30 - 00:11:32] that's just disappearing into the environment.
[00:11:32 - 00:11:37] So you can treat it as energy lost because we're not kind of accounting for it.
[00:11:37 - 00:11:42] If, however, we're modeling an element in an electric jug,
[00:11:42 - 00:11:46] obviously the heat is an important part for that, right?
[00:11:46 - 00:11:50] And so it's not been, well, it's not so much an energy dissipator,
[00:11:50 - 00:11:56] but then an energy transformer, and it's converting electrical energy into thermal energy.
[00:11:56 - 00:12:10] So it's a dissipator, if we're not interested in the heat that comes out of it,
[00:12:10 - 00:12:26] or it can be a transformer of energy, I'll say, an electrical guy on the,
[00:12:26 - 00:12:34] a little heating element, I should say.
[00:12:34 - 00:12:40] So it's a lot of this, you know, when we're thinking about modeling,
[00:12:40 - 00:12:42] it comes down to what is the purpose of our modeling.
[00:12:42 - 00:12:47] That resistive can just behave as something that doesn't make energy disappear from our system,
[00:12:47 - 00:12:54] or it can be modeled as something is going to transform energy from one source to another,
[00:12:54 - 00:12:57] or one domain to another.
[00:12:57 - 00:13:04] Now, with a resistor, if we're treating this in a dissipator, it sort of sends,
[00:13:04 - 00:13:06] it's got two variables.
[00:13:06 - 00:13:27] We've got the currents, and we've got our voltage, and together we've got the power.
[00:13:27 - 00:13:32] So obviously the electrical power that's being dissipated is V times i.
[00:13:32 - 00:13:47] But if we want to think about this more generally, you'll probably all quite happy with the electrical side of things,
[00:13:47 - 00:13:53] but if we want to generalize this method across our energy domains,
[00:13:53 - 00:13:57] what we want to do is rather than, you know, obviously these currents in voltage,
[00:13:57 - 00:14:01] but they kind of set below another label.
[00:14:01 - 00:14:05] So I have taken current as a flow, right?
[00:14:05 - 00:14:09] And that's something that has to be the same input in the output, right?
[00:14:09 - 00:14:13] So you've got your resistor, if you put an emitter at the front and an emitter at the other end,
[00:14:13 - 00:14:19] the current goes through no currents disappearing in that resistor, it's not magically, you know,
[00:14:19 - 00:14:23] going away that currents is conserved.
[00:14:23 - 00:14:26] Obviously that's things like a curve has current law.
[00:14:26 - 00:14:36] So we've got a flow, and then we've got the V of T's of voltage as a potential.
[00:14:36 - 00:14:42] And so we've got a flow, we've got a potential.
[00:14:42 - 00:14:46] And the potential is something that's a difference that's measured across,
[00:14:46 - 00:14:49] so between the input and the output, right?
[00:14:49 - 00:14:54] When you're measuring voltage in the circuit, you put your voltmeter across the resistor,
[00:14:54 - 00:14:57] across the diode, or whatever, and that's how you measure that voltage.
[00:14:57 - 00:15:07] So what we're looking at here is something that's called the through-across analogy.
[00:15:07 - 00:15:12] And you can look up if you're interested on working PDF, for example.
[00:15:12 - 00:15:20] There's a number of different ways that you can make analogies between the energy domains.
[00:15:20 - 00:15:25] So there's through-across, and there's the impedance and the emitter's analogy.
[00:15:25 - 00:15:31] And there's different ways that you can treat them, and they've all got pros and cons.
[00:15:31 - 00:15:33] They all largely work out.
[00:15:33 - 00:15:39] They give you the result that's consistent in works.
[00:15:39 - 00:15:45] I'm teaching you about the this through-across analogy, just because flow on potential makes quite a bit of sense,
[00:15:45 - 00:15:49] when you're thinking about it.
[00:15:49 - 00:15:53] And so it gives you an idea, but there are other analogies.
[00:15:53 - 00:15:59] So resistance then is defined as the over-eye, because we have omezle obviously.
[00:15:59 - 00:16:03] But what that means then is it's potential per unit flow.
[00:16:03 - 00:16:11] So it's the amount of potential associated with a given flow.
[00:16:11 - 00:16:16] And the rate of energy dissipation is dissipation is the instantaneous power,
[00:16:16 - 00:16:22] which is obviously as we saw as V times i, so it's potential times flow.
[00:16:22 - 00:16:33] But these are the generalizations that occur across the domain.
[00:16:33 - 00:16:39] So in mechanical translational energy domain, there'll be a potential and a flow,
[00:16:39 - 00:16:42] which we'll talk about in just a minute.
[00:16:42 - 00:16:49] And then instantaneous power is potential times flow, and there'll be an equivalent.
[00:16:49 - 00:16:55] So what would be the equivalent to a resistor in terms of a translational mechanical system?
[00:16:55 - 00:17:02] Yeah, a damp ice. So a dash box of viscous damp ice is the equivalent of electrical resistor, right?
[00:17:02 - 00:17:11] So if we've got one of those, let me excuse my drawing.
[00:17:11 - 00:17:31] I forgot a shaft on the output side of the damp air.
[00:17:31 - 00:17:33] So we've got a damp air like this.
[00:17:33 - 00:17:41] What are the variables that with what are those conjugate power variables?
[00:17:41 - 00:17:49] Well, the equivalents of voltage and current, but in terms of a damp air.
[00:17:49 - 00:17:56] So we've got velocity.
[00:17:56 - 00:18:07] And what's the other thing that you multiply the velocity with to get power?
[00:18:07 - 00:18:09] Force.
[00:18:09 - 00:18:13] Good.
[00:18:13 - 00:18:21] So now this one's an interesting thing.
[00:18:21 - 00:18:25] So what of these? What's the flow variable?
[00:18:25 - 00:18:32] What's conserved across that device?
[00:18:32 - 00:18:40] What's got the same value ignore the vector nature of it in order to direction?
[00:18:40 - 00:18:45] Force, right? Because if it's not the same at both sides, that thing's accelerating rapidly away.
[00:18:45 - 00:18:52] And so flow is the equivalent of force in through across analogy,
[00:18:52 - 00:18:54] because it has the same value at both sides.
[00:18:54 - 00:18:59] Velocity is the equivalent of potential because you measure that across.
[00:18:59 - 00:19:04] If you have you've got those points A and B and you measure them relative to each other,
[00:19:04 - 00:19:07] A will be moving with respect to B.
[00:19:07 - 00:19:09] So that is the potential.
[00:19:09 - 00:19:34] And so that's velocity.
[00:19:34 - 00:19:36] And so that's just summarizing.
[00:19:36 - 00:19:41] So for a linear damper, as you should know,
[00:19:41 - 00:19:46] force F is equal to C times X dot.
[00:19:46 - 00:19:52] So force is equal to C times velocity.
[00:19:52 - 00:20:01] So effectively the limit got flow is equal to C times potential.
[00:20:01 - 00:20:08] And then so if we rearrange that, so we've got the potential, the unit flow,
[00:20:08 - 00:20:11] that's equal to 1 over C.
[00:20:11 - 00:20:15] And that's somewhat equivalent to the idea of resistance.
[00:20:15 - 00:20:17] Electrical resistance, hypertension, and unify.
[00:20:17 - 00:20:20] What you might know about this is it's 1 over C.
[00:20:20 - 00:20:25] Normally you think you bigger damper constants.
[00:20:25 - 00:20:28] That's like a bigger resistor, you're just very buoyant and stuff like that.
[00:20:28 - 00:20:30] And you're absolutely right.
[00:20:30 - 00:20:33] These analogies aren't perfect.
[00:20:33 - 00:20:37] And there's some inconsistencies in the way that we sort of think about things.
[00:20:37 - 00:20:42] And that's why there are multiple analogies because you've got other forms of this analogy
[00:20:42 - 00:20:45] where you've got C is approximately equal to R.
[00:20:45 - 00:20:50] So basically flow would be force.
[00:20:50 - 00:20:55] So flow would be velocity and potential would be force.
[00:20:55 - 00:20:58] But then that doesn't have the sort of a cross-through thing.
[00:20:58 - 00:21:02] And so you've got these ways that you have to think about them to make it work.
[00:21:02 - 00:21:05] And so this is one of those kind of weirdnesses.
[00:21:05 - 00:21:11] Because you've got 1 over C is approximately equal to your resistance there.
[00:21:11 - 00:21:21] So the analogies don't necessarily, you know, this is an inconsistencies in your head in the way that we think about them.
[00:21:21 - 00:21:24] But they do the track mathematically.
[00:21:24 - 00:21:33] And then obviously we've got power is equal to force times velocity, potential times flow.
[00:21:33 - 00:21:39] So if we were to generalize that with got, so energy dissipate is across all the domains.
[00:21:39 - 00:21:42] You characterize bi-2 variables, potential and flow.
[00:21:42 - 00:21:48] For a linear dissipator, you've got potential is equal to some constant times flow.
[00:21:48 - 00:21:51] And the power is equal to potential times flow.
[00:21:51 - 00:21:57] And these are all called single port elements.
[00:21:57 - 00:22:00] Because they've got one single power port.
[00:22:00 - 00:22:07] And that you've only got, like we can set up power going into a resistor, the electrical power n.
[00:22:07 - 00:22:09] And we ignore the heat that comes out.
[00:22:09 - 00:22:13] And the same with that dashpot, you can set a mechanical power going into it.
[00:22:13 - 00:22:16] And we ignore the heat that comes out of it.
[00:22:16 - 00:22:19] Because we're viewing it from, we don't care about that heat.
[00:22:19 - 00:22:25] If we were doing this in terms of a electrical heating element,
[00:22:25 - 00:22:27] we would do care about the heat coming out of it.
[00:22:27 - 00:22:31] Then it becomes a two-port element because you have two power ports.
[00:22:31 - 00:22:33] You'll have the electrical power coming in.
[00:22:33 - 00:22:37] You'll have the thermal power going out, for example.
[00:22:37 - 00:22:42] And so those are called two-port elements, which will get to shortly.
[00:22:42 - 00:22:45] But we've got these, we've talked about already.
[00:22:45 - 00:22:49] We've got electrical domain and potential as voltage flows current.
[00:22:49 - 00:22:51] And the dissipators are resistant.
[00:22:51 - 00:22:53] Sensational mechanical.
[00:22:53 - 00:22:55] We've got a dashpot or a damper.
[00:22:55 - 00:22:57] Potential is velocity.
[00:22:57 - 00:22:59] And flows force.
[00:22:59 - 00:23:05] So, for rotational mechanical, what's the potential variable?
[00:23:05 - 00:23:09] So, oh, yeah, angular velocity, right?
[00:23:09 - 00:23:12] So, that's angular velocity.
[00:23:12 - 00:23:18] And the flow, the equivalent force, is poor, right?
[00:23:18 - 00:23:25] Then in the hydraulic pneumatic system,
[00:23:25 - 00:23:29] what's the equivalent of potential?
[00:23:29 - 00:23:32] So, if we think about flows.
[00:23:32 - 00:23:33] Yep.
[00:23:33 - 00:23:34] All right.
[00:23:34 - 00:23:40] So, for potential, it's something that you measure across.
[00:23:40 - 00:23:41] So, pressure.
[00:23:41 - 00:23:43] Yes, our flow rate is the next one, right?
[00:23:43 - 00:23:46] So, we've got pressure here.
[00:23:46 - 00:23:52] And then specifically, it's volume flow rate.
[00:23:52 - 00:23:56] And then the hydraulic system, you know, a resistor or a dissipator
[00:23:56 - 00:23:59] is effectively a construction in the tube.
[00:23:59 - 00:24:03] And then for a thermal system, potential is temperature.
[00:24:03 - 00:24:05] The flow is heat flow.
[00:24:05 - 00:24:07] And then you can have a thermal resistance.
[00:24:07 - 00:24:13] And we do see thermal resistance values in the everyday life.
[00:24:13 - 00:24:15] Actually, you might not see them.
[00:24:15 - 00:24:17] But when you get older, you might.
[00:24:17 - 00:24:20] When you're buying a house or something.
[00:24:20 - 00:24:24] Yeah.
[00:24:24 - 00:24:25] An insulation value is right.
[00:24:25 - 00:24:27] If you go and buy a bank batch or something, it might attend.
[00:24:27 - 00:24:28] They'll have an R value on there.
[00:24:28 - 00:24:30] And that's capturing the thermal resistance.
[00:24:30 - 00:24:33] And so, how much heat flows through.
[00:24:33 - 00:24:36] Okay.
[00:24:36 - 00:24:38] So, the summary we've got so far flows pass through.
[00:24:38 - 00:24:40] Potentials are measured across.
[00:24:40 - 00:24:46] This is the through across analogy that's force and current.
[00:24:46 - 00:24:50] A related rather than force and voltage, which is another analogy.
[00:24:50 - 00:24:55] But these analogy methods are how, as I mentioned this,
[00:24:55 - 00:24:58] they have physical systems, model, multi-domain modeling.
[00:24:58 - 00:25:00] Depending on what the core software works.
[00:25:00 - 00:25:04] So, the one that obviously we're going to use is CIMSCAT.
[00:25:04 - 00:25:07] But we'll frame a one-quarter system model.
[00:25:07 - 00:25:10] Make, we'll do one-quarter, we'll make all CIMSCAT.
[00:25:10 - 00:25:15] There's an open framework called Modelica that does this.
[00:25:15 - 00:25:18] There's an open piece of software called OpenModelica.
[00:25:18 - 00:25:20] But when I'll plug around with it to see if we can use it,
[00:25:20 - 00:25:21] it was a bit shut.
[00:25:21 - 00:25:28] And so, we'll stuck with the MathWorks one for what we're doing.
[00:25:28 - 00:25:33] Because it gives you some good kind of experience.
[00:25:33 - 00:25:36] Is any questions up to this point about this?
[00:25:36 - 00:25:43] So, obviously I have this idea of the dissipator.
[00:25:43 - 00:25:49] But we can generalize these single-port elements.
[00:25:49 - 00:25:52] We've got their single-power points.
[00:25:52 - 00:25:55] So, effectively you've got two terminals.
[00:25:55 - 00:26:02] And the general form of it is you've got some thing that looks like this, right?
[00:26:02 - 00:26:08] You've got flow passing through, and that's the same on both sides.
[00:26:08 - 00:26:17] You've got a potential cross.
[00:26:17 - 00:26:20] And so, we're talking about dissipators.
[00:26:20 - 00:26:27] What there's two other types of single-port elements that we need to acknowledge.
[00:26:27 - 00:26:29] So, what could they do then?
[00:26:29 - 00:26:32] Think about circuits when you're first minute out circuits,
[00:26:32 - 00:26:35] because that'll give you an idea.
[00:26:35 - 00:26:38] Now, just for a two-port element, because you take a little power,
[00:26:38 - 00:26:44] and you put a little bit out, but you've just changed the relationship between voltage and current.
[00:26:44 - 00:26:45] Storage, yeah.
[00:26:45 - 00:26:48] So, we've got stores.
[00:26:48 - 00:26:52] And an electrical system, what would those be?
[00:26:52 - 00:26:53] Yeah.
[00:26:53 - 00:26:57] And, yeah, and I've got it, right?
[00:26:57 - 00:27:03] So, those two storage elements and a single-port source,
[00:27:03 - 00:27:11] or a single-port source, and what's other type of element.
[00:27:11 - 00:27:18] So, generator, are closed slightly more,
[00:27:18 - 00:27:21] less lower level, I think you're getting there.
[00:27:21 - 00:27:25] A generator, technically a generator, would be a two-port element,
[00:27:25 - 00:27:29] because you'll take in mechanical energy, or less of chemical energy,
[00:27:29 - 00:27:33] through rotational mechanical, through interelectrical.
[00:27:33 - 00:27:37] But, well, if you're doing a circuit, and it's got some resistors and some capacitors,
[00:27:37 - 00:27:40] what else would it need to actually be anything useful?
[00:27:40 - 00:27:41] EOS sources, right?
[00:27:41 - 00:27:44] Yes, it can cause voltage source.
[00:27:44 - 00:27:50] So, in single-port elements, we've got these.
[00:27:50 - 00:27:51] Right?
[00:27:51 - 00:27:55] So, we've got sources, and we've got energy stores.
[00:27:55 - 00:27:59] So, think about sources, so they'd supply energy to the system,
[00:27:59 - 00:28:07] so we've got potential sources, so things like an ideal voltage source,
[00:28:07 - 00:28:11] if we're doing a transnational mechanical.
[00:28:11 - 00:28:15] And flow sources will have an ideal current source,
[00:28:15 - 00:28:24] and a force source, for example.
[00:28:24 - 00:28:31] And so, they deliver potential or flow independent of the flow or potential of the support.
[00:28:31 - 00:28:38] Just like a voltage source, it will deliver five volts across its terminals,
[00:28:38 - 00:28:41] and whatever the current needs to be, the current is.
[00:28:41 - 00:28:43] Right? And so, that's the same with these sources.
[00:28:43 - 00:28:49] So, you might have a force source that delivers, you know, whatever how many newtons,
[00:28:49 - 00:28:54] and there will be whatever the velocity is that comes from that,
[00:28:54 - 00:28:57] because of the equilibrium of the whole system.
[00:28:57 - 00:29:01] So, that source is there pretty straightforward.
[00:29:01 - 00:29:04] In terms of energy stores, they're stored energy in the system.
[00:29:04 - 00:29:12] And so, for a potential store, for example,
[00:29:12 - 00:29:17] then the flow is a function of the accumulated potential.
[00:29:17 - 00:29:21] So, an example of this might be a spring, a mechanical system.
[00:29:21 - 00:29:26] And so, if we look at that, that's because you've got, if,
[00:29:26 - 00:29:29] is equal to k times x, right?
[00:29:29 - 00:29:32] So, force is equal to k times displacement.
[00:29:32 - 00:29:37] And so, force is our flow as well.
[00:29:37 - 00:29:41] So, in that way, flow is equal to k times.
[00:29:41 - 00:29:47] Now, we, to get x, we can integrate velocity.
[00:29:47 - 00:29:51] And so, that's our accumulated potential.
[00:29:51 - 00:30:08] So, the flow is equal to some constant times the accumulated potential for a spring.
[00:30:08 - 00:30:14] And so, another would be an inductor.
[00:30:14 - 00:30:21] Right? So, with an inductor, you've got your voltage is equal to L or dI over the T.
[00:30:21 - 00:30:26] So, if we rearrange that, we end up with i, which is our flow,
[00:30:26 - 00:30:33] is equal to 1 over L, dV, but it's indeed, indeed, dT, right?
[00:30:33 - 00:30:43] So, it gives us a flow as equal to the accumulated potential for an inductor.
[00:30:43 - 00:30:53] So, that's a potential store.
[00:30:53 - 00:30:57] For flow stores, it's the equivalent situation, right?
[00:30:57 - 00:31:01] So, potential is a function of the accumulated flow.
[00:31:01 - 00:31:09] And so, in the mechanical system, mass is a flow store.
[00:31:09 - 00:31:16] Because you've got the force is equal to mass times x double dot.
[00:31:16 - 00:31:19] And so, if we integrate both sides of that,
[00:31:19 - 00:31:32] so you end up with integrated force is equal to mass times that, which is equal to velocity.
[00:31:32 - 00:31:43] And so, we've got the accumulated flow, which is the integrated force,
[00:31:43 - 00:31:47] is equal to mass times of velocity, right?
[00:31:47 - 00:31:53] And so, in the electrical sense, we have a capacitor.
[00:31:53 - 00:31:55] There's a flow store.
[00:31:55 - 00:31:58] Is there any questions about that?
[00:31:58 - 00:32:02] So, there's a single-port elements.
[00:32:02 - 00:32:06] Now, we understand we've got dissapators and stores and sources.
[00:32:06 - 00:32:19] We can then generally put down the constitutive relation.
[00:32:19 - 00:32:28] So, each single-port element has a constitutive relation that forms this relationship between potential and flow.
[00:32:28 - 00:32:36] So, with dissapators, we've got potential is equal to some constant times flow.
[00:32:36 - 00:32:41] So, for example, ohm's law, v is equal to i times that.
[00:32:41 - 00:32:48] For sources, we've just got potential is equal to some value, right?
[00:32:48 - 00:32:51] Let's just call it x of t.
[00:32:51 - 00:32:59] Or for flow, y of t.
[00:32:59 - 00:33:03] So, as an example with the electrical system, you might have an ideal voltage source,
[00:33:03 - 00:33:14] and then for stores, we have potential is equal to integrative flow.
[00:33:14 - 00:33:36] So, these are all the exact same equations that you're using two, three, and three, three.
[00:33:36 - 00:33:39] But they've just been framed in a different way.
[00:33:39 - 00:33:49] So, rather than using for a mechanical system x x dot x double dot, we may be framing them as an integrative relationship.
[00:33:49 - 00:33:57] And the dynamics are all the same, but we're just looking at that system from a slightly different point of view.
[00:33:57 - 00:34:08] So, generalizing across single-port elements, whether it is domains that we looked at before,
[00:34:08 - 00:34:13] we did the dissipators before looking at the potential stores.
[00:34:13 - 00:34:18] So, four electrical circuits that's inducted for a transition of mechanical.
[00:34:18 - 00:34:32] It's a spring for rotational mechanicals, a torsional spring for fluid systems and netants.
[00:34:32 - 00:34:41] There is no potential store for thermal systems, unfortunately.
[00:34:41 - 00:34:48] So, what's the rotational equivalent of mass? So, is a flow store?
[00:34:48 - 00:34:52] And, you're sure, it's a rotational inertia. Don't worry.
[00:34:52 - 00:34:57] That happens the reason. Hopefully, not in lectures.
[00:34:57 - 00:35:02] Must end up here.
[00:35:02 - 00:35:13] So, what's a flow store?
[00:35:13 - 00:35:19] What's a flow store for a hydraulic or a pneumatic system?
[00:35:19 - 00:35:26] Who's done any hydraulics?
[00:35:26 - 00:35:32] Yeah, it's a reservoir or an accumulator.
[00:35:32 - 00:35:37] Unfortunately, you don't get really hydraulics during the de-grade, neither do the mechanical students.
[00:35:37 - 00:35:42] So, it's something you'll end up having to pick up an withdrawal if it's required.
[00:35:42 - 00:35:44] So, you've had a few final projects that need it.
[00:35:44 - 00:35:57] But you have accumulators or reservoirs, which store energy.
[00:35:57 - 00:36:07] And then, in a thermal system, you've got thermal capacitance.
[00:36:07 - 00:36:09] So, where's all this leading?
[00:36:09 - 00:36:14] We can basically connect all these together and get that with circuits.
[00:36:14 - 00:36:19] I don't think I need to tell you this, but basically you can connect them in series.
[00:36:19 - 00:36:24] These elements, so you might have a system like this.
[00:36:24 - 00:36:31] And as you know, with resistors, the current through is the same as the current all the way through.
[00:36:31 - 00:36:35] And the voltage across your add data.
[00:36:35 - 00:36:38] So, I'm not going to go into too much detail there.
[00:36:38 - 00:36:46] And similarly, you can have these elements in parallel where you've got the flow splits between them.
[00:36:46 - 00:36:48] And then joins up again.
[00:36:48 - 00:36:54] And the potential across them is the same across each other.
[00:36:54 - 00:36:58] So, you've got series and parallel systems.
[00:36:58 - 00:37:08] But more generally, what we can define is we've got continuity and compatibility.
[00:37:08 - 00:37:13] And so, those equations and potential and flow, basically these are analogous to KCL.
[00:37:13 - 00:37:20] So, if you've got this current law and calculus voltage law, saying that continuity says that all flows into a common connector, some to zero.
[00:37:20 - 00:37:24] So, obviously, that means flows in a positive and it's actually out of negative.
[00:37:24 - 00:37:31] And so, that is equivalent to KCL that you would have learned to see them do I think.
[00:37:31 - 00:37:37] And then you've got compatibility, which is all potentials around a closed loop, some to zero.
[00:37:37 - 00:37:41] And so, that's equivalent to calculus voltage law.
[00:37:41 - 00:37:46] And so, then you can analyze these circuits in the swing.
[00:37:46 - 00:37:56] And so, as an example, we can then, as an indicator, we can sort form circuits.
[00:37:56 - 00:38:21] Maybe if we've got a mass here, mass spring damper system, there's a force, this could be a source, so that force is driving.
[00:38:21 - 00:38:25] So, what are these are stores of energy?
[00:38:25 - 00:38:48] Yep, the springs are store, what's another store, mass is a store, basically through inertia.
[00:38:48 - 00:38:56] And then we've got a dissipator here with our damper.
[00:38:56 - 00:39:03] And so, thinking about this, we can draw this up like an electric circuit.
[00:39:03 - 00:39:10] So, we draw a reference point here, because it's our reference point, we'll do ground.
[00:39:10 - 00:39:14] Now, we've got a force source.
[00:39:14 - 00:39:20] So, force is a flow, so I'm going to draw that like a current source.
[00:39:20 - 00:39:36] We've got a spring, which I'm drawing it like a spring, or that sort of looks like a resistor there, right?
[00:39:36 - 00:39:49] So, that spring, then we've got a damper, which was 16 this down a little bit.
[00:39:49 - 00:40:00] Then we've got a mass.
[00:40:00 - 00:40:11] Now, the mass doesn't physically connect back to that reference point, but it's referred to the reference point,
[00:40:11 - 00:40:15] because the motion of that mass relates to that reference point.
[00:40:15 - 00:40:21] And therefore, we have to show that there's a reference to that.
[00:40:21 - 00:40:24] So, we end up having this here.
[00:40:24 - 00:40:35] And so, we end up with, it can look like an electric circuit, if I just change this color.
[00:40:35 - 00:40:42] In this case, we've got a node here, this is our reference node, node GC.
[00:40:42 - 00:40:48] This is a node here.
[00:40:48 - 00:40:55] And then we can apply KCL at node A.
[00:40:55 - 00:41:06] We can see that current's in as it equates out, and so it is a flow here, a flow here, a flow here.
[00:41:06 - 00:41:17] And so, we end up with F of t is equal to, say, that's F of k, F of c, F of m.
[00:41:17 - 00:41:26] And then if we use those constitutive equations, we head, so what do we know about the spring?
[00:41:26 - 00:41:33] The force is equal to k times the integral of velocity dt plus the damper.
[00:41:33 - 00:41:46] We've got 1 over c times the velocity plus for the mass.
[00:41:46 - 00:41:52] We've got in, b, v, b, t.
[00:41:52 - 00:41:58] So, that's the same for a mass spring damper that's just a reformatted equation that you would have
[00:41:58 - 00:42:03] derived using a free body diagram from 303, right?
[00:42:03 - 00:42:10] Except we have got the force is equal to, we were normally right there in terms of unit estate variable of,
[00:42:10 - 00:42:13] you know, as x is being the baseline.
[00:42:13 - 00:42:19] If you like our displacement and then x, x dot and x double dot, this has been formatted in a way where
[00:42:19 - 00:42:26] the base state variable is velocity, and so you end up with velocity, then to the velocity and the derivative of velocity.
[00:42:26 - 00:42:27] Okay?
[00:42:27 - 00:42:48] So, it ends up with same equation, um,
[00:42:48 - 00:42:55] and just forms in terms of velocity rather than, uh, displacement.
[00:42:55 - 00:43:01] Any questions about that?
[00:43:01 - 00:43:06] So, what's nice about it is, you know, this is a translational mechanical system,
[00:43:06 - 00:43:12] but you can end up drawing that so that it looks like a circuit, electrical circuit, and you can analyze it
[00:43:12 - 00:43:15] the same way that you would analyze an electric circuit.
[00:43:15 - 00:43:20] You can then do the same with serial rotational mechanical circuit or another one,
[00:43:20 - 00:43:26] and then, and this is what we'll get onto in the next picture, then when we have two poor elements,
[00:43:26 - 00:43:32] so maybe you've got a DC motor, the DC motor looks like to the electric circuit and looks like a dissipator,
[00:43:32 - 00:43:35] because it's taking energy out of the electric circuit.
[00:43:35 - 00:43:39] But on the other side, that's coupled to a rotational mechanical circuit,
[00:43:39 - 00:43:44] and there it looks like a source, so it's transforming energy from the electrical system to the rotational mechanical circuit.
[00:43:44 - 00:43:49] So, it looks like a dissipator here and a source here, but in doing that,
[00:43:49 - 00:43:54] then it allows you to develop these coupled equations quite easily,
[00:43:54 - 00:44:01] and in a way that looks like electric circuits, and in a way that you can analyze it like electric circuits.
[00:44:01 - 00:44:05] And this is basically what's happening underneath the hood when you use, um,
[00:44:05 - 00:44:10] cinscape or any of those multi-domain software, when you're dragging blocks together,
[00:44:10 - 00:44:15] that system is developing a series of equations,
[00:44:15 - 00:44:19] differential algebraic equations like this, and then it solves it numerically,
[00:44:19 - 00:44:23] and that's how you get the simulation results out.
[00:44:23 - 00:44:27] There's probably a hidden example, but I couldn't get it to work before I started here,
[00:44:27 - 00:44:30] so I'll try and make that work before.
[00:44:30 - 00:44:36] Next time, either way, you will also have some experience with that during the tutorial next week,
[00:44:36 - 00:44:38] so that necessarily needs to show that.
[00:44:38 - 00:44:43] Does any questions? Otherwise, we'll just stop for now and we'll continue next week.
[00:45:42 - 00:45:46] Thank you.
[00:45:46 - 00:45:48] Thanks.
[00:45:48 - 00:45:50] My pleasure.
[00:45:50 - 00:45:52] Thank you.
[00:45:52 - 00:45:54] Thank you.
[00:45:54 - 00:45:56] Thank you.
[00:45:56 - 00:45:58] You can't believe it.
[00:45:58 - 00:46:05] No.
[00:46:05 - 00:46:12] No.
[00:46:12 - 00:46:19] No.
[00:46:56 - 00:47:09] I'm just two examples of it.
[00:47:09 - 00:47:19] I'm just going to want to go to the next one.
[00:47:19 - 00:47:28] I'm going to go to the next one.

# ENMT301-26W Lecture 34 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_34_audio_16k_mono_32k.mp3`
Source audio SHA-256: `2feff831274c64fbccb1514e04604dc67d13e16ea508a07e45dd07c30b6bc75a`
Generated: 2026-06-06T06:20:19.295028+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:00 - 00:00:04] He is from the mechanical engineering department and Duke teaches
[00:00:05 - 00:00:08] by the mechanical design program, but also the
[00:00:09 - 00:00:12] Management program. Do you want to stop talking?
[00:00:13 - 00:00:26] You can't hear me because you're chattering. Okay, so
[00:00:28 - 00:00:33] Duke's gonna talk about fault train analysis today, and that's quite important because in your second
[00:00:33 - 00:00:37] Robocut report you have to do a fault train analysis and
[00:00:37 - 00:00:44] And you'll find it's actually quite useful because it allows you identify potential failure modes and then hopefully address them
[00:00:45 - 00:00:49] So a you need to know how to do it, but b is actually quite useful
[00:00:51 - 00:00:55] And I'll just leave Duke to talk about it from now because he knows more about what I do
[00:00:55 - 00:00:58] I do have the sign-up sheets. I'll pass that around
[00:00:59 - 00:01:09] Go ahead. Go ahead. Go ahead. Go ahead. Go ahead. Go on. Go on. So the fault train analysis is a tool that's widely used
[00:01:10 - 00:01:18] Typically it arose in Bell Aerospace and was first used in aerospace accidents, so it comes out of engineering it grew up in
[00:01:20 - 00:01:23] Looking at our rockets and other aircraft structures fail
[00:01:24 - 00:01:25] the
[00:01:25 - 00:01:31] So what do you've learned so far in terms of hazard safety risk assessment is the standard risk assessment
[00:01:32 - 00:01:37] Kind of table which has got consequence and likelihood you multiply them together you get a number you treat it
[00:01:37 - 00:01:39] You determine a risk as residual risk
[00:01:39 - 00:01:47] So that is technician level skills. So everyone in the world of technologies expect to be able to do those risk assessments
[00:01:47 - 00:01:55] You've probably lasted one in ENG or 200th work experience thing remember like that is just really rock bottom basics
[00:01:55 - 00:02:04] So I'm not going on on that one. So as engineers we get more complex problems and we need and we have a number of tools to do that
[00:02:04 - 00:02:09] And the one that we're choosing to show you here today is one called for tree analysis
[00:02:09 - 00:02:11] so
[00:02:11 - 00:02:13] I'm going to take an aerospace
[00:02:13 - 00:02:22] related theme because it's quite good because it includes both the mechanical and the electrical and the control system applications for this
[00:02:22 - 00:02:24] so
[00:02:24 - 00:02:26] this is one of the
[00:02:30 - 00:02:32] Landers and
[00:02:33 - 00:02:40] roughly seven hours after launch it had a problem with the propulsion system
[00:02:41 - 00:02:47] So you spend all that effort in the time making all that stuff and that gold foil here really is gold foil
[00:02:47 - 00:02:49] And you think of how many million dollars
[00:02:50 - 00:02:55] Go into creating a project like that and what a fun project. It would be the work on
[00:02:55 - 00:03:02] It's pretty much every trans student in this class would love to work on a project like that like budget is not really a major issue
[00:03:02 - 00:03:09] You know we've got millions to spend and you want to make it the best possible thing and then just seven hours after your launch
[00:03:09 - 00:03:12] It's somewhere in space that has even got to the moon and
[00:03:13 - 00:03:19] It's kind point to this it can't point to the Sun it can't maintain its orientation in space
[00:03:19 - 00:03:22] So if you think about what that means for a spacecraft
[00:03:22 - 00:03:24] This is like quite seriously problematic
[00:03:24 - 00:03:30] Because then all the thrusters all the other control systems are dependent on knowing where you are pointing in space
[00:03:31 - 00:03:37] And so what happened in this particular case is a propellant leak one small little thing some way
[00:03:37 - 00:03:42] Prevented the lander from completing its whole mission so that entire thing is scrap
[00:03:43 - 00:03:45] It's like a project fail
[00:03:45 - 00:03:53] Because the one small thing went wrong so we need tools and as I'll show you fortune analysis is really good tool to help us understand the
[00:03:53 - 00:03:55] interactions of these systems
[00:03:56 - 00:03:58] so
[00:03:58 - 00:04:02] Basically something happened there there's another one
[00:04:02 - 00:04:08] This is artist's artist's perspective of what it should look like on the moon and
[00:04:10 - 00:04:12] This is the actual
[00:04:12 - 00:04:14] on the moon
[00:04:14 - 00:04:16] It tipped over 30 degrees
[00:04:16 - 00:04:18] on
[00:04:18 - 00:04:23] Landing I think one of the legs crushed from memory I can't remember what is a mechanical what the issue was and
[00:04:24 - 00:04:28] Consequently it couldn't direct its antenna back at earth and again
[00:04:29 - 00:04:32] Epic fail so you can see that small little things
[00:04:33 - 00:04:35] Consider as you destabilize our missions
[00:04:36 - 00:04:42] There's a little content warning over here. I've got some stuff which does involve
[00:04:43 - 00:04:48] People people dying and that we have to realize is a consequence of our engineering activities
[00:04:48 - 00:04:54] And that's one of the reasons why we are really strong on safety as part of professional practice
[00:04:54 - 00:05:00] It's because people's life do you depend on it. This is space shuttle Columbia at launch. It's working perfectly fine
[00:05:00 - 00:05:02] Everything's going fine
[00:05:02 - 00:05:05] Well apparently so and this is it when it comes back
[00:05:06 - 00:05:10] onto earth's atmosphere you can see it has broken up into pieces and
[00:05:11 - 00:05:15] That kind of entry at mark 18
[00:05:16 - 00:05:20] when the stagnation air temperatures of the order of 3000 degrees C is
[00:05:21 - 00:05:25] Not easily survivable for people and indeed they crew all perished
[00:05:26 - 00:05:31] so if we have a look at how we approach an accident like that and
[00:05:32 - 00:05:38] NASA did use fault tree analysis to approach exactly that accident so
[00:05:40 - 00:05:44] I'll just take a break and say there's two main ways to use fault tree analysis
[00:05:44 - 00:05:47] The one is what we call prophylactic and the other one is
[00:05:48 - 00:05:56] Diagnostic and prophylactic we apply it beforehand just like you take anti-malirials before you go to malaria country
[00:05:56 - 00:05:58] that's called prophylactic
[00:05:58 - 00:06:04] and if you get malaria then you take treatment and that's diagnostic and the treatment component
[00:06:04 - 00:06:09] So the prophylactic we apply beforehand the diagnostic once we see the accident and
[00:06:10 - 00:06:16] We've got some video and perhaps some pieces on the ground we then start to piece together what might have happened
[00:06:16 - 00:06:19] And so fault tree analysis can be used in both modes
[00:06:19 - 00:06:28] So this example is a diagnostic one. We already know the space shuttle has disintegrated and there's some we've got some photographs and some pieces on the ground
[00:06:28 - 00:06:33] And now we kind of say well what actually happened in this particular situation
[00:06:33 - 00:06:36] So there's some kind of logic here to
[00:06:37 - 00:06:42] fault tree and that is that we have what is called a top event. We have a diagram
[00:06:42 - 00:06:48] It's a schematic systeming method. There's a block on the top of the page in the middle and that's called a top event
[00:06:49 - 00:06:55] Pretty logical because it's on the top of the page and everything flows down below that and then we have a tree structure and
[00:06:56 - 00:06:58] We're trying to work down to
[00:06:58 - 00:07:06] the root causes of that accident and we use a combination of Boolean logic and an all or the primary symbols
[00:07:06 - 00:07:11] but there are some others and we construct a logical kind of
[00:07:12 - 00:07:14] Model as to what we think could have happened
[00:07:15 - 00:07:17] So let me show you hard works
[00:07:17 - 00:07:23] So here we have lots of vehicle at tree entry in the yellow box and we've got the symbols
[00:07:24 - 00:07:29] For all and end on the top right. You can you should hopefully recognize those kinds of things
[00:07:29 - 00:07:35] We have a little call out symbol which is a one or two or an A or B whatever you like
[00:07:36 - 00:07:39] Which says here be another larger tree which
[00:07:40 - 00:07:45] Which expands on this particular thing because our piece of paper is not big enough
[00:07:45 - 00:07:52] So we have multiple levels of paper if you want to so if you look at the loss of vehicle and the crew at the entry
[00:07:52 - 00:07:54] There's the before and off the pictures again
[00:07:55 - 00:07:58] You work down from the top and you say it hasn't all
[00:07:59 - 00:08:07] Symbol and it's saying it could either be explosion of the vehicle or a fire occurring within the vehicle or
[00:08:08 - 00:08:10] overheating of the vehicle or
[00:08:11 - 00:08:15] Aerodynamic and inertial destruction of the vehicle. So what typically happens at
[00:08:17 - 00:08:19] Supersonic speeds for
[00:08:20 - 00:08:28] Aerodynamic situations is that if you have a craft that goes slightly skew at aerodynamic at
[00:08:28 - 00:08:30] Supersonic speeds
[00:08:30 - 00:08:36] Because a drag is related to the velocity squared and the velocity is a very high
[00:08:37 - 00:08:42] You suddenly expose the aircraft to a massive amount of drag on the side
[00:08:43 - 00:08:46] So if you've got a rocket and it goes slightly sideways
[00:08:46 - 00:08:50] now there's a massive amount of drag acting on it and
[00:08:50 - 00:08:58] Generally almost universally with most aerospace things the heaviest masses at the back because that's where the rocket motors on
[00:08:58 - 00:09:05] That was true the space shuttle as well. So the inertial effect of that means that there's a very strong moment
[00:09:05 - 00:09:13] That twists continue to twist the craft sideways to the flow because they're heavy and inertial components want to go ahead and
[00:09:14 - 00:09:20] The lights are fairings and other parts of the rocket want to get slowed down because of the drag forces
[00:09:20 - 00:09:22] so there's a massive twisting moment and
[00:09:23 - 00:09:27] In many situations the control systems do not have enough
[00:09:28 - 00:09:31] talk capability or moment capability on the aircraft
[00:09:32 - 00:09:38] structured to restore that at very high speeds and as a consequence you then have a situation
[00:09:38 - 00:09:46] Where the heavy parts of them of the rocket just continue going ahead and the light parts get pulled apart and the whole thing
[00:09:46 - 00:09:51] Just gets aerodynamically destroyed by being pulled apart in that kind of situation
[00:09:51 - 00:09:58] So that's what do we mean by aerodynamic and inertial destruction? It's the the opposing forces that swing the car
[00:09:58 - 00:10:06] Offed around and then just just shredded basically and the whole craft gets shredded into large chunks of metal and smaller chunks of
[00:10:07 - 00:10:11] Things like paper so if you ever sheet a pipette reentry
[00:10:12 - 00:10:18] It was its drag is so high, but its resistance. It's inertia so low
[00:10:18 - 00:10:25] It actually will just it'll just sort of almost instantly decelerate and then just flat it down unburnt
[00:10:26 - 00:10:31] Resear a heavy thing like a rocket motor. It's got so much momentum in it
[00:10:31 - 00:10:34] It'll just keep on climbing through the atmosphere and you get a large amount of
[00:10:36 - 00:10:42] 3000 degrees CE acting it over a long time and you get a lot of burn on those particular parts
[00:10:42 - 00:10:43] so
[00:10:43 - 00:10:45] And this is just another interesting fact
[00:10:45 - 00:10:53] So when you have a reentry situation like this the lighter pieces fall down first on the trail of debris and the heaviest ones go
[00:10:53 - 00:10:58] The furthest and will tend to show the most thermal damage as part of the process
[00:10:59 - 00:11:05] So you then start to say right if there's going to be an explosion of your call you with me
[00:11:05 - 00:11:12] We're on the far left now. You either say I can think of three different ways of that kind of coup on board energy source explodes
[00:11:14 - 00:11:17] sabotage or collision with somebody
[00:11:17 - 00:11:22] So you can say let's go to the onboard energy source exploding and you can say
[00:11:23 - 00:11:29] Maybe if you'll tank explode maybe there's another pressurized vessel like an oxygen cylinder that exploded
[00:11:29 - 00:11:32] That could be those could be artesons as well
[00:11:33 - 00:11:35] sabotage could someone a planted a bomb on board
[00:11:37 - 00:11:42] Collision with a major external body like could it have hit another satellite or a piece of space junk or
[00:11:43 - 00:11:51] Some piece of rockers was just orbiting around the what was could that occurred and you work those things down and down and down now
[00:11:52 - 00:11:59] Regarding sabotage you say well, that's extremely unlikely because of the very high strict
[00:12:00 - 00:12:04] Security controls around the launch of these kinds of vehicles not impossible
[00:12:04 - 00:12:08] But that's not something we might say we're just gonna stop right now
[00:12:09 - 00:12:16] Because some of the other evidence suggests that this idea of a inertial and aerodynamic destruction might be one that's worthwhile
[00:12:17 - 00:12:20] pursuing and thinking about further so we think
[00:12:20 - 00:12:25] Hmm in order to do that you need sufficiently high irredynamic forces
[00:12:25 - 00:12:31] Well at mark 18 you have sufficiently high irredynamic forces. No doubt about that. So that one's okay
[00:12:32 - 00:12:37] Although there's a complex interplay because all those doing mark 18 the air
[00:12:38 - 00:12:41] density is quite low at
[00:12:41 - 00:12:48] Elements of their atmosphere and so the peak heating occurs not so much when it first engages with the atmosphere
[00:12:48 - 00:12:54] But part way in so if you can imagine in your mind is a relationship between the heating
[00:12:55 - 00:12:57] related to the speed which is dropping slowly and
[00:12:58 - 00:13:05] The air density which is slowly increasing as the craft sinks into the atmosphere so some complex physics inside the two opposing effects
[00:13:05 - 00:13:11] So efficient to say there's a period of peak heating that occurs within a vehicle and
[00:13:12 - 00:13:18] You also have to have the vehicle rotating especially in picture your so there's an extra little block
[00:13:18 - 00:13:24] He symbol over here which has got the flat part the bottom and doesn't have the point and that's the end symbol
[00:13:24 - 00:13:28] So on the whole most fault trees will use an all symbol
[00:13:28 - 00:13:35] But occasionally you'll need the end and means this and that and anything else have to happen that all have to happen a
[00:13:36 - 00:13:38] typical case of that in other situations is fire
[00:13:39 - 00:13:41] So fire you need a fuel
[00:13:42 - 00:13:44] What else must be present?
[00:13:45 - 00:13:52] Yeah, an oxygen or an oxidizer more generally if we just want to be authentic about it and one other thing
[00:13:57 - 00:14:02] Yeah heat sort of your close, but I'll only give you two out of five for that three out of five many
[00:14:03 - 00:14:07] It's also ignition. Yeah, this what is called spark flame, etc
[00:14:07 - 00:14:14] So you need those three things so whenever you have a fire situation you can automatically know that you're gonna put a little end symbol
[00:14:14 - 00:14:16] And you're gonna have fuel
[00:14:16 - 00:14:19] Oxidizer ignition source and then you can break them down and have a look
[00:14:20 - 00:14:21] Well, we don't have fire here
[00:14:21 - 00:14:28] So I'm not gonna take that one further, but that's just a general tip if you're looking for fire fire is one of their standard
[00:14:29 - 00:14:31] hazards for domestic appliances
[00:14:32 - 00:14:36] Greenfield tower in the UK was a tower block
[00:14:36 - 00:14:41] that was an Edward burnt out burnt out with a lot of loss of life and
[00:14:41 - 00:14:45] The cause of that fire was a fridge or freezer
[00:14:45 - 00:14:48] Which had an electric fire the most dangerous?
[00:14:48 - 00:14:50] These are the plants in your home
[00:14:51 - 00:15:01] I can think of two of them for fire or what biggest cause of fire and houses
[00:15:02 - 00:15:04] Haven't no actually not
[00:15:05 - 00:15:09] So partly yet you can get nice bad kitchen fires
[00:15:10 - 00:15:12] Sorry
[00:15:12 - 00:15:16] No, not fine charger, but get closer make the phone a bit bigger and tell me what it's called
[00:15:17 - 00:15:24] Now go bigger still come on more killer. What's no?
[00:15:24 - 00:15:30] Hot water soon does not at all. Are your heat is at a bady radiant heaters?
[00:15:30 - 00:15:33] But people put towels over them. Yep. I mean that's obviously ignition. So
[00:15:35 - 00:15:37] No
[00:15:37 - 00:15:42] Your e-bike or your scooter so the big battery that never charge those things and tools of
[00:15:43 - 00:15:47] The domestic appliances or white way. What's the most dangerous?
[00:15:51 - 00:15:55] No, actually not
[00:15:55 - 00:15:58] Fred is one yet, but but think another one another thing or white way
[00:15:59 - 00:16:01] Dryer
[00:16:01 - 00:16:02] clothes dryer
[00:16:02 - 00:16:04] I refuse to have one at home
[00:16:05 - 00:16:13] They are most seriously seriously hazardous and that's because they form a fine lint which collects and that provides the
[00:16:13 - 00:16:15] really fuel
[00:16:15 - 00:16:19] And they've got heat because they're rotating and they get you know, you got electric
[00:16:19 - 00:16:23] What do you call a static electricity? So is it everything is there?
[00:16:23 - 00:16:27] We need to go there tuning there's nice oxygen mixed up all the time
[00:16:27 - 00:16:34] So so you watch what's your what's your dries if you use those things those are particularly hazardous for domestic fires
[00:16:35 - 00:16:37] Okay, so
[00:16:37 - 00:16:42] In this particular case we're coming back to this question. We've established this efficient
[00:16:42 - 00:16:48] Aerodynamic forces to cause a problem over here. We know neither question whether or not it's possible that the aircraft
[00:16:48 - 00:16:53] Good rotate and pitch or you're you're always going sideways like this
[00:16:54 - 00:16:58] And pitch is up and down motor cars generally don't pitch up and down much
[00:16:59 - 00:17:04] But we only see cars really just your like a skid sideways is a you're so
[00:17:05 - 00:17:06] a
[00:17:06 - 00:17:08] Roll is the other axis
[00:17:08 - 00:17:14] But roll is not generally so much of a problem in aerodynamics situations. Let's see other two
[00:17:14 - 00:17:18] So you then have to say hmm. How could the
[00:17:18 - 00:17:26] vehicle rotate in row in pitch or your and you have to say I will control system steered into a bad configuration
[00:17:26 - 00:17:33] There's a little bit unlikely there have multiple computers flight control computers on that craft and
[00:17:33 - 00:17:35] at a voting system and the
[00:17:35 - 00:17:37] computer computers were
[00:17:38 - 00:17:41] Running on different hardware so they wouldn't necessarily be a hardware
[00:17:42 - 00:17:43] induced
[00:17:43 - 00:17:48] homogeneity and at a voting system so as soon as there was a control decision to be made
[00:17:49 - 00:17:55] The three flat computers world say this would each one in thought to do and I'd vote on which way to go
[00:17:55 - 00:18:00] So there's unlikely to be a control system that just skewed the skewer the craft across
[00:18:01 - 00:18:04] So then you have to think about maybe the control system was overwhelmed
[00:18:06 - 00:18:10] And now you think well what was the control system at that speed?
[00:18:11 - 00:18:17] You don't know this but I'll tell you so up to speeds of Mach 3
[00:18:17 - 00:18:19] I'm just gonna make that number up. I don't know if I'm 100% right
[00:18:20 - 00:18:22] above that
[00:18:22 - 00:18:24] and attitude control pitch
[00:18:25 - 00:18:30] Your and and pitch is controlled by thrust digits. Sorry
[00:18:30 - 00:18:35] You always controlled by thrust digits on the nose that push the nose left and right and
[00:18:38 - 00:18:40] And pitch is controlled by allurons at the back of the wings
[00:18:41 - 00:18:47] When the speed gets below Mach 2 or 3 or something then the rudder is involved with your control
[00:18:47 - 00:18:52] So at the speed that occurred we know that if there's a control problem it wouldn't have been the rudder
[00:18:52 - 00:18:54] unless there wasn't a
[00:18:55 - 00:19:01] command error to the rudder a command error is when something operates when it should not have operated
[00:19:02 - 00:19:06] So the rudder could have been turned and that would have made a massive
[00:19:06 - 00:19:12] Aerodynamic force at that speed and would have been very difficult for the yorgeates to counter that kind of force
[00:19:13 - 00:19:17] So that's an unintended command error. They are very
[00:19:18 - 00:19:19] Not very common
[00:19:19 - 00:19:26] But there are source of concern for aircraft because you have a large number of wires running through aircraft fuselage
[00:19:27 - 00:19:31] And what tends to happen on some of the aircraft is the wires get rubbed
[00:19:31 - 00:19:37] Will I go through their aluminum compartments and then you can get short circuit in between cables
[00:19:37 - 00:19:39] So you put a
[00:19:39 - 00:19:41] Voltage down one cable to say go do this
[00:19:42 - 00:19:44] But some of the voltage leaks into another
[00:19:44 - 00:19:48] Control circuit and make something operate. So that's a typical
[00:19:48 - 00:19:54] Mechanical degradation and one of the big costs of running old aircraft is that the wiring
[00:19:54 - 00:19:58] To redo the wiring is a superheavatively expensive
[00:19:58 - 00:20:04] Even though the aircraft might be structurally okay the wiring once the installation starts to deteriorate the major problem
[00:20:05 - 00:20:09] So possibly it could have been that kind of situation control system fault
[00:20:09 - 00:20:12] But let's explore this thing about the control system overwhelmed
[00:20:13 - 00:20:19] And that's the little one. So now we're going to go down to another tree which says what it's going to do
[00:20:19 - 00:20:21] skip all that
[00:20:21 - 00:20:23] I didn't actually give it to you
[00:20:23 - 00:20:28] I better just talk to you about what actually happened. Let me just take my slides to see what it's what I've got
[00:20:29 - 00:20:31] Terms of explaining what actually happened
[00:20:44 - 00:20:46] This slide here is just says
[00:20:47 - 00:20:49] I'm just pointing out here that they used a fault tree
[00:20:51 - 00:20:53] So that is the
[00:20:54 - 00:20:59] Wheel well so I don't even know what I'm looking at here. I see complexity
[00:21:00 - 00:21:04] I see a hydraulic cylinder which is probably pushing the wheel up and down
[00:21:04 - 00:21:07] But look at all those little pipes and stuff pipes and cables
[00:21:08 - 00:21:14] So the problem occurred here at the wheel well and what had happened is during launch a piece of foam
[00:21:15 - 00:21:20] Really like foam about two kgs or so that broken off the nose of the aircraft
[00:21:20 - 00:21:24] The reason it was there in the first place is the aircraft was made it to a large
[00:21:25 - 00:21:27] hydrogen and oxygen tank
[00:21:27 - 00:21:30] Which provided a fuel for its rocket motors
[00:21:31 - 00:21:37] And because of hydrogen and oxygen being cryogenic it tended to form ice and the ice
[00:21:38 - 00:21:42] If it hit came off would hit the wings and cause damage
[00:21:42 - 00:21:44] So they covered it with insulation foam
[00:21:44 - 00:21:49] Unfortunately about two to three kgs of insulation foam came off
[00:21:49 - 00:21:54] And struck the wing with a red arrow is at about Mach 3
[00:21:55 - 00:22:00] Punch in a hole which is what that diagram's trying to show in the leading edge of the wing
[00:22:02 - 00:22:06] There's a cavity behind the leading edge. It's then during re-entry
[00:22:08 - 00:22:11] When stagnation temperatures about 3000 degrees C
[00:22:12 - 00:22:15] The hot air came in with effectively plasma
[00:22:16 - 00:22:20] Came in by that big red arrow through the big hole in the front of the wing
[00:22:20 - 00:22:23] And impinged upon the aluminum internal structures
[00:22:24 - 00:22:27] Which is what the second little black little circulars
[00:22:27 - 00:22:34] And from there the plasma behaves in a very unpredictable way because it's electrically charged
[00:22:34 - 00:22:38] So it's sort of like we'll bend around with magnetic and electric fields. It doesn't flow like a normal fluid
[00:22:39 - 00:22:44] But there's natural scavenging of airflow through the wing which heads towards the wheel well
[00:22:44 - 00:22:49] So the plasma was directed towards the wheel well cut through that
[00:22:49 - 00:22:56] And started burning those cables and they can see that afterwards in terms of various sensors suddenly going offline
[00:22:57 - 00:23:03] So they could reconstruct the accident based on the data that they actually could actually had
[00:23:03 - 00:23:08] And the arrows show that subsequently after the plasma is now melted also to stuff
[00:23:08 - 00:23:11] It's heading forward in the wing because that's the natural airflow
[00:23:12 - 00:23:18] Now recover the larger amount of stuff. It's really interesting that something can come in at supersonic speeds
[00:23:19 - 00:23:22] And you can slow recover pieces which are evidently
[00:23:23 - 00:23:27] You know, you can recognize them. That's the front wheel wheel landing wheel system
[00:23:32 - 00:23:34] Okay, so here we go to the rest of the
[00:23:35 - 00:23:40] One so if we look at control system overwhelmed we now move to the little one and
[00:23:41 - 00:23:44] You might have been able to see if you see it looking from quite far back
[00:23:45 - 00:23:50] But our hal added in red where things happened. So we've got an awesome below here
[00:23:50 - 00:23:54] And we say it could either be dynamic instability some kind of vibration
[00:23:54 - 00:23:57] Or aesthetically overwhelmed system or that what it was
[00:23:58 - 00:24:03] And so what happened is that the was an imbalanced error forces because this
[00:24:03 - 00:24:06] air cutting into the wing of the aircraft
[00:24:07 - 00:24:13] Massively increased the drag on that wing and started to yaw the aircraft across
[00:24:13 - 00:24:16] And at the same time the control system
[00:24:17 - 00:24:26] If you look at the record you can see that all five yaw jets are firing at 100% duty cycle to try and bring their yaw back under control
[00:24:27 - 00:24:30] But just before what it's it lost lost control
[00:24:31 - 00:24:36] As I said the yaw jets utilization was at 100% so it was maxed out
[00:24:36 - 00:24:42] There wasn't a control error. It's just that the control system was not designed to handle that degree of moment on the air
[00:24:43 - 00:24:45] aircraft which is pulling it away sideways
[00:24:46 - 00:24:48] interesting enough
[00:24:49 - 00:24:51] They produced a second report later
[00:24:52 - 00:24:56] Which takes a different perspective on this and it seems like two things happened at once
[00:24:56 - 00:25:01] The one was that the yaw jets failed to control their yaw excursion
[00:25:01 - 00:25:04] And you only need to get about I forget what the number is
[00:25:04 - 00:25:09] Three to five degrees excursion in yaw control and that set us all over
[00:25:10 - 00:25:14] But the second thing happened was that that and pairs my cutting into the wheel well
[00:25:15 - 00:25:21] burnt through the hydraulic pipes that control their hydraulic cylinder that I showed you for putting the wheel up and done
[00:25:22 - 00:25:24] Now they had three separate hydraulic systems
[00:25:25 - 00:25:31] But they all burnt through and so what happened is the hydraulic system lost pressure
[00:25:32 - 00:25:34] And that caused the
[00:25:35 - 00:25:38] Flight control surfaces which is the elevators at the back
[00:25:39 - 00:25:43] It caused them to lose control so the pilots had a loss of control situation
[00:25:43 - 00:25:50] They could no longer control the flight control surfaces at the rear of this delta wing and so consequently the aircock went up
[00:25:51 - 00:25:58] Into nose nose up kind of attitude which on its on its own is sort of survivable because it's actually
[00:25:59 - 00:26:03] Presenting the heat shield components to the airflow
[00:26:03 - 00:26:08] But it caused massive accelerations because now the drag force is high
[00:26:08 - 00:26:16] So at the same time it sort of like put its nose up and it started to your sideways and then the air and the aerodynamic
[00:26:16 - 00:26:19] aerodynamic and neutral forces just ripped the whole thing apart
[00:26:20 - 00:26:22] If you're a mechanical engineer
[00:26:23 - 00:26:29] Sometimes in 418 which you don't do but it's coolant of your management paper
[00:26:29 - 00:26:34] I give the students a set reading for each year and so some years it's the cruise availability report
[00:26:35 - 00:26:40] So there's no gruesome images as it will reject it but it talks about what actually happens in the situation
[00:26:40 - 00:26:47] You like the bulkiers get ripped and the seats the seats get ripped off the floor and seat belts
[00:26:47 - 00:26:52] They strong enough with a helmet strong enough that kind of thing which is obviously of interest to mechanical engineers
[00:26:53 - 00:26:58] But you're a trans student so you're probably a little less interested in that kind of detail
[00:26:58 - 00:27:04] But we got all of that detail if you really wanted to know exactly what happened their published reports that actually cover all of those things
[00:27:05 - 00:27:07] so here is the
[00:27:08 - 00:27:10] fault tree and
[00:27:10 - 00:27:14] It has got in at this idea here that there's this whole burnt into the wing
[00:27:14 - 00:27:17] There's little symbol here as an additional one which is yes time
[00:27:18 - 00:27:22] This is one of the major limitations with fault tree analysis
[00:27:22 - 00:27:24] It assumes that
[00:27:24 - 00:27:32] Propagation on the whole it assumes that propagation from the root causes towards the bottom is instant towards the top
[00:27:32 - 00:27:37] It doesn't really have a strong time dimension. It has a logical dimension to it
[00:27:38 - 00:27:41] And so as a consequence fault tree analysis one of its limitations
[00:27:42 - 00:27:49] Is that if there is a time dimension like a feedback loop or it takes time for something to occur in the case of the spatia
[00:27:50 - 00:27:51] a thermal
[00:27:51 - 00:27:53] Dlegration takes time to occur
[00:27:54 - 00:27:57] Then it can struggle to represent that adequately
[00:27:57 - 00:28:01] So it sort of assumes everything happens in some stainless steel. There's no time dimension
[00:28:02 - 00:28:06] But there are some symbols that you can use to show that there's a kind of a time delay
[00:28:07 - 00:28:10] in the evolution of their accident sequence
[00:28:12 - 00:28:17] Okay, so now I want to go back and look at some other stuff for you
[00:28:22 - 00:28:24] In the notes
[00:28:24 - 00:28:29] I've got some other examples for you, but I just want to go back and show you
[00:28:31 - 00:28:39] Another example a bit different and this is product liability. So this is when a company or a person a person can get
[00:28:39 - 00:28:44] Sorry a company can get sued because it's product failed and in order to
[00:28:45 - 00:28:49] Establish a legal case of product liability two things must happen
[00:28:50 - 00:28:54] The product must fail and harm must be caused. It's an end
[00:28:55 - 00:29:00] If the user was harmed, but it wasn't due to the product failing. There's no product liability
[00:29:01 - 00:29:04] If the product failed, but there was no harm
[00:29:05 - 00:29:08] Created there's no product liability case
[00:29:09 - 00:29:11] When it comes down to
[00:29:11 - 00:29:18] The work the harm is it can be personal injury or damage to property personal injury can be injury death
[00:29:18 - 00:29:22] Disability or in the United States emotional trauma
[00:29:23 - 00:29:25] So if you're selling a product
[00:29:25 - 00:29:29] An innovative new product into the United States. One of your biggest risks is
[00:29:30 - 00:29:32] Product liability people have a very litigated
[00:29:33 - 00:29:39] Approach to products in that part of the world and there are two needs who exist
[00:29:39 - 00:29:43] To who will take on product liability cases charging no fee
[00:29:44 - 00:29:48] But will seek to get a share of awards
[00:29:49 - 00:29:52] In New Zealand, you can't claim emotional trauma
[00:29:52 - 00:30:00] But the United States you can and they put big money to that. It's like millions to billions can be paid out for
[00:30:01 - 00:30:05] emotional trauma case even if the was no it was no death
[00:30:06 - 00:30:10] No permanent disability yet, but there was an element of injury and emotional trauma
[00:30:11 - 00:30:12] jurors
[00:30:12 - 00:30:17] That's a the panel that judges the cases are very sympathetic in that jurisdiction
[00:30:18 - 00:30:20] to emotional trauma
[00:30:20 - 00:30:23] So and that's just to help you understand that
[00:30:24 - 00:30:30] You can apply the faultry kind of thinking even to other situations like the representation of
[00:30:30 - 00:30:38] The legal logic regarding product. So I mentioned that as a different example to show you and especially if you're interested in innovation
[00:30:39 - 00:30:42] Here's a more mundane situation. This is the
[00:30:43 - 00:30:45] push-on pike or
[00:30:45 - 00:30:46] digital
[00:30:46 - 00:30:48] So the dish washer
[00:30:48 - 00:30:56] Door operation can be restricted. That's the top event. You see the logical structure and you can see that there's three
[00:30:56 - 00:30:58] four main things
[00:30:59 - 00:31:06] Perfect to the chassis which is typically a manufacturing quality system the wiring loom restricts the motion
[00:31:06 - 00:31:08] The door mechanism could be jammed
[00:31:09 - 00:31:14] And that'd be because could be because there's debris food debris or something like that in the mechanism
[00:31:14 - 00:31:22] Or the seal could be stuck and there could be a number of causes for that including sticky foods food substances
[00:31:22 - 00:31:25] These circles are the root causes
[00:31:26 - 00:31:31] Those are as far down as we have chosen to take it. You could take it further
[00:31:31 - 00:31:36] So food stuff sticky, which is on the follow-up item right corner
[00:31:36 - 00:31:39] You could make that go down further and further and further and say
[00:31:39 - 00:31:41] peanut butter is not very sticky, but
[00:31:42 - 00:31:44] Momelade is you know that kind of a thing
[00:31:44 - 00:31:47] But we've just chosen to say we're gonna stop at that point
[00:31:48 - 00:31:53] So key ideas within the faultry idea is a top event
[00:31:53 - 00:31:56] The use of end and ores symbols in a progressive
[00:31:57 - 00:32:00] Tree-based structure hence fault tree analysis
[00:32:01 - 00:32:07] Down to some level of root causes where you've decided I'm not going any further. That's sufficient for what I'm doing now
[00:32:07 - 00:32:10] You've also got not shown here, but shown elsewhere
[00:32:10 - 00:32:17] Little call out blocks where you can start a new tree to further expand on something that you think is particularly interesting and relevant
[00:32:20 - 00:32:22] Okay, so here's lawnmower fire
[00:32:22 - 00:32:24] So
[00:32:24 - 00:32:31] This is hand drawn so probably not all that legible if you're sitting far away, but this is the
[00:32:32 - 00:32:36] Fire thing so it's fuel source oxygen source and ignition source and here
[00:32:36 - 00:32:44] I've anticipated a number of different things like on the fuel source, which is an all fuel-lined leak tank leak manufacturing
[00:32:44 - 00:32:50] leak defect dry grass or operator error and likewise for the other ones
[00:32:50 - 00:32:55] So that's what a fault tree would look like for the top event of lawnmower catches fire
[00:32:56 - 00:33:01] I briefly want to show you what some of the other methods are like and what they look like in case you're interested
[00:33:02 - 00:33:06] This is called failure mode and effects analysis fnea
[00:33:06 - 00:33:12] It's a bit like the tabular risk assessment that you know and I've been already familiar with and this particular case
[00:33:12 - 00:33:14] You say the fuel tank
[00:33:15 - 00:33:22] Sheet steel inside that can fail in a number of ways which will cause fire it can rust
[00:33:22 - 00:33:24] it can rust
[00:33:25 - 00:33:31] Through the wall it can be dented and have a crack that can get hot due to the exhaust
[00:33:32 - 00:33:34] Okay, that's it's four failure modes
[00:33:35 - 00:33:44] Failure modes of the fuel tank if it gets dented and cracked then the effect hence the word of failure mode and
[00:33:44 - 00:33:51] Effect analysis is that you can have leak of the fuel and then a fire and then you have this likelihood and consequence
[00:33:52 - 00:33:58] Score like you know from the tabular risk assessment except they normally add one more and that is
[00:33:59 - 00:34:00] detectability
[00:34:00 - 00:34:08] So how easy would it be to detect that area that thing or else there's sometimes add a fourth number which is criticality?
[00:34:09 - 00:34:17] Our critical is that defect they're multi-fiber all those numbers together and they get what they call a risk priority number rp in
[00:34:18 - 00:34:23] If you add criticality then they call it failure mode effect and criticality analysis
[00:34:23 - 00:34:31] But you'll see there's a whole family of methods of which this one here shown is the simplest whereby we are taking each part
[00:34:32 - 00:34:40] Think care drawing you draw a fuel tank and then you say in what ways could this different ways could this fuel tank fail?
[00:34:40 - 00:34:43] So it's a different approach to fault tree analysis
[00:34:44 - 00:34:52] Because fault tree analysis already assumes fire and it doesn't know whether or not it's going to be fuel tank or
[00:34:52 - 00:34:56] Because the operator spilt the fuel and then try it smoking
[00:34:56 - 00:34:59] So the two approaches are very different
[00:35:00 - 00:35:05] The FMEA is quite often used in design detail design
[00:35:05 - 00:35:11] It's a method of choice for nuclear power stations by the way they produce volummus big documents with
[00:35:11 - 00:35:14] FMEA as to if this fell failed
[00:35:14 - 00:35:24] How would it fail in different ways like leak or burst or overheat or get too cold or whatever else and then what would be the effect on the risk to the plant?
[00:35:24 - 00:35:26] It could of course a whole plant to fail
[00:35:26 - 00:35:31] The other one
[00:35:31 - 00:35:33] These are the three main ones
[00:35:33 - 00:35:40] But there are others is what's called bow town analysis and bow town analysis. We put the
[00:35:41 - 00:35:47] Fire as the central knot of the bow town member bow tie with a like you know think a little penguin suit bow
[00:35:47 - 00:35:50] Tark it's got a knot in the middle and go taro
[00:35:50 - 00:35:53] horizontally so the fire of the lawn mows in the middle and
[00:35:54 - 00:35:56] On the left are the possible causes
[00:35:57 - 00:36:01] Rather confusingly this is called a top event where it should really be called a middle event
[00:36:01 - 00:36:07] It's called a top event because it borrows that terminology from poultry if you imagine this whole thing turned on its side
[00:36:07 - 00:36:13] Lift up the right hand side and push it upwards. It sort of looks like a fault tree. No logic
[00:36:14 - 00:36:18] I don't like logic and sides here and what they say they are multiple
[00:36:19 - 00:36:24] roots no logic and food as to how you can get to fire
[00:36:25 - 00:36:27] So for example
[00:36:27 - 00:36:29] You can have a
[00:36:30 - 00:36:38] Methodological problem like fuel spilling there could be a spill of a fuel during filling the lawn mow if it's a petrol one
[00:36:39 - 00:36:41] You could have
[00:36:42 - 00:36:45] Failure to clear wrapped up vegetation from the shaft
[00:36:45 - 00:36:48] So these things are called barriers
[00:36:49 - 00:36:51] In other words in order for
[00:36:51 - 00:36:58] This to occur these barriers will all have to be defeated. I don't have time to go into the concept very much
[00:36:58 - 00:37:04] But sufficient to say this is the primary method that's used in civil aviation against accidents
[00:37:05 - 00:37:08] So if we look at that accident, that's just occurred in Lagosia
[00:37:08 - 00:37:13] The God your airport in the New York. That's a standard accident. It's extremely well known
[00:37:13 - 00:37:20] It's called a runway incursion where some kind of other vehicle comes onto the runway when an aircraft is on it
[00:37:21 - 00:37:26] And there are plenty of bow ties which talk about exactly that kind of thing. It's well known
[00:37:27 - 00:37:29] and that particular case the controller
[00:37:29 - 00:37:32] aircraft the controller left the vehicle across and
[00:37:33 - 00:37:35] the
[00:37:35 - 00:37:39] You could have thought well why did the fire truck not detect there was an aircraft
[00:37:40 - 00:37:48] So that was another missed opportunity. They didn't they just went they could have looked left and right and said oh
[00:37:48 - 00:37:51] There's some lights done there on the runway. Maybe we should just stop
[00:37:51 - 00:37:56] So from a boat up perspective each of these things is a barrier that prevents
[00:37:57 - 00:37:58] the
[00:37:58 - 00:38:02] sequence from progressing from left to right which is the fire
[00:38:03 - 00:38:08] Bow time has this additional really useful concept of what happens afterwards?
[00:38:08 - 00:38:12] So what can you do to potentially recover the situation and
[00:38:12 - 00:38:16] Present prevent it from getting to catastrophic outcomes
[00:38:16 - 00:38:20] So the catastrophic outcomes for a lawn mower or destruction of the mower
[00:38:20 - 00:38:25] So it's like okay, we lose a couple hundred dollars harm to the operator. Someone gets
[00:38:25 - 00:38:31] Bad burns and needs to be hospitalised or destruction of the building like you pop that lawn mower in your garage
[00:38:31 - 00:38:36] And the fire occurs far minutes later than you potentially have lost the whole house
[00:38:36 - 00:38:39] And if you happen to have stored the petrol canister
[00:38:39 - 00:38:45] Right next to the lawn mower then you've added more fuel you see so the bow time method is looking at
[00:38:46 - 00:38:48] particularly human processes
[00:38:49 - 00:38:55] So I've shown you in detail the poultry analysis method, but there are other ways of looking at similar kinds of errors
[00:38:57 - 00:38:59] Okay
[00:38:59 - 00:39:01] I'm gonna just quickly change to
[00:39:02 - 00:39:08] Something in a few minutes that we've got left. I want to show you another example and I've put this
[00:39:10 - 00:39:12] Inside your folder
[00:39:13 - 00:39:15] Hopefully it's a funny example
[00:39:18 - 00:39:20] I put a set of notes called
[00:39:22 - 00:39:29] Systems engineering
[00:39:29 - 00:39:33] This is also got a space theme. I'm just gonna skip a little bit still. I get to the bit that I want
[00:39:35 - 00:39:37] You can read it if you're interested
[00:39:45 - 00:39:51] Now skip mowers missions
[00:39:52 - 00:39:55] So what is hard about landing on mowers?
[00:39:57 - 00:39:59] Well, I'll give you some clues
[00:39:59 - 00:40:08] You have a journey from earth surface to the insertion of mowers orbit, which means entering mowers orbit. Why is it challenging?
[00:40:10 - 00:40:14] Why is that hard?
[00:40:14 - 00:40:17] For a way. Thank you
[00:40:17 - 00:40:23] Anything else?
[00:40:23 - 00:40:30] Yep, you got to have you got to be earth and the mowers have got to be in the right relative position or the was it takes a long time?
[00:40:31 - 00:40:35] Is the space launch a gentle process or or is it quite rough?
[00:40:35 - 00:40:42] Massive enough massive vibrations occurred during launch as a rocket fast
[00:40:42 - 00:40:50] You know moving backwards and forwards. It's got I got supersonic e-speeds all that kind of stuff once it's in space. What's the problem there?
[00:40:53 - 00:40:55] No pressure anymore. Yep, but what else
[00:40:57 - 00:41:00] Sorry radiation yep good
[00:41:01 - 00:41:05] Freezing cold on the one side of the of the spacecraft boiling hot on the other side
[00:41:05 - 00:41:12] So your your payload is nice subject to some thermal gradient across it and you got some dinky little mechanism
[00:41:12 - 00:41:14] which is gonna unfold the
[00:41:14 - 00:41:16] antenna and
[00:41:16 - 00:41:22] This combination of effects is guaranteed to mean that when you land on Mars the antenna will not unfold
[00:41:22 - 00:41:28] It's happened to several things before so I'm not talking about a hypothetical situation and if you don't have an antenna
[00:41:29 - 00:41:31] You can't talk to earth anymore. It's just like bubeye
[00:41:32 - 00:41:40] Craft so that's the first thing. Secondly the entry velocity is up is 4.6 to 7.3 kilometers a second
[00:41:41 - 00:41:44] Well, why is that challenging?
[00:41:44 - 00:41:49] That's inting Mars atmosphere not that it has much atmosphere, which is the next point
[00:41:50 - 00:41:52] So what do you see as the challenge there?
[00:41:53 - 00:41:56] Slowing down with aerodynamic braking is going to be hard
[00:41:57 - 00:42:00] You have a lot of speed and you don't have much air density
[00:42:01 - 00:42:05] The landing ellipse tends to be 100 kilometers by 15 kilometers wide
[00:42:06 - 00:42:09] That's the best you can aim for so what challenges does that give you?
[00:42:14 - 00:42:20] a lot of terrain difficulties. Yep, so like are you heading towards a rock or not?
[00:42:20 - 00:42:24] It could be a lot of rocks within a hundred kilometer block of land
[00:42:25 - 00:42:30] Ambient conditions on the ground are extremely dusty very dark in winter or
[00:42:31 - 00:42:37] Not not sunshine times and extremely cold none of which are very helpful for small little mechanisms and
[00:42:39 - 00:42:41] batteries don't like it
[00:42:41 - 00:42:43] There's no planetary magnetic field
[00:42:44 - 00:42:46] What does that mean so what does that the consequences of that?
[00:42:48 - 00:42:54] Radiation comes streaming in so all your electronics is busy getting fried and you're gonna get in your
[00:42:55 - 00:42:58] Memory and stuff. It's gonna be I'm not electronics engineer
[00:42:58 - 00:43:02] But I can just imagine bits of ram getting their bits flipped
[00:43:02 - 00:43:06] And then I don't know what that'll do, but there probably won't be a good thing with it
[00:43:07 - 00:43:13] And the next one is the distance to earth is up to 400 million kilometers. So what's the impact of that?
[00:43:15 - 00:43:19] Yeah, communications delay. So what do you have to do design for?
[00:43:22 - 00:43:25] Thank you autonomous so when this thing is coming into land
[00:43:25 - 00:43:33] It has to sort itself out. It has to detect if there is a rock in the way and it has to steer
[00:43:33 - 00:43:39] You cannot steer it from 400 million kilometers away the time distance is I don't know what you can Google it
[00:43:39 - 00:43:44] There's something like eight minutes. So this is not exactly real-time control. Is it?
[00:43:45 - 00:43:51] Okay, so this is MOS land
[00:43:52 - 00:43:53] A
[00:43:53 - 00:43:58] Shaper really this is before the diagram shows the various components to this craft
[00:43:59 - 00:44:02] multiple layers of things at the bottom are
[00:44:04 - 00:44:06] Heat shields and stuff like that and in the middle is
[00:44:07 - 00:44:13] All the electronics and stuff and propulsion systems and at the top are parachutes and things like that
[00:44:15 - 00:44:17] This is after
[00:44:18 - 00:44:20] So it made a crater
[00:44:20 - 00:44:21] two meters
[00:44:21 - 00:44:23] wide
[00:44:23 - 00:44:25] It's smacked into Mars at
[00:44:26 - 00:44:28] 300 kilometers an hour
[00:44:29 - 00:44:32] So that was one rover which is not very happy
[00:44:34 - 00:44:36] So why what went wrong over there?
[00:44:38 - 00:44:39] So
[00:44:39 - 00:44:43] I don't have time to go through to in a detailed fault to analysis
[00:44:43 - 00:44:48] But if we thought about it from a fault to analysis, we would say as follows we'd say
[00:44:48 - 00:44:53] I'll just start drawing it we've got it just a few minutes yet. So
[00:44:57 - 00:44:59] land that impacts
[00:45:01 - 00:45:03] terrain
[00:45:03 - 00:45:05] This is a standard terminology for
[00:45:07 - 00:45:11] A terrain includes ocean as well by the way although that might not seem very logical
[00:45:11 - 00:45:14] But that's how we do it in this kind of industry
[00:45:14 - 00:45:20] So now you say I'm gonna give us an awesome book to start with and I'm gonna say right to give me some
[00:45:21 - 00:45:25] Give me some ideas as to what could of course this to very broadly to have
[00:45:26 - 00:45:35] Impacted the terrain
[00:45:39 - 00:45:41] Okay, so we'll say breaking system
[00:45:46 - 00:45:47] Good, okay anything else
[00:45:50 - 00:45:54] Control fair is a good one, but probably but to broad make it
[00:46:00 - 00:46:02] Attitude control yeah like that one
[00:46:03 - 00:46:05] One of which things could be
[00:46:06 - 00:46:13] So attitude is its orientation could this one sideways what's one of the possible causes could then be a controlled era
[00:46:15 - 00:46:18] Okay, another thing it could have been a
[00:46:21 - 00:46:32] Orbital insertion era could have come in too fast too high
[00:46:33 - 00:46:35] Too wrong side of the planet or something like that
[00:46:36 - 00:46:43] So you can work your way down and work out a different thing everyone to construct the fault tree will come up with one slightly
[00:46:43 - 00:46:48] Differently and that's a somewhat disadvantage of the mechanism. It doesn't result in a unique response
[00:46:49 - 00:46:51] Let's look at what actually happened
[00:46:51 - 00:46:54] The actual sequence was that it's entered at
[00:46:55 - 00:46:57] 21,000 kilometers an hour at
[00:46:58 - 00:47:01] 123 kilometers altitude and that worked as planned
[00:47:02 - 00:47:09] It used heat shield breaking to 1,600 kilometers an hour at 11 kilometers altitude and that worked fine
[00:47:11 - 00:47:17] Then jettison the heat shield at seven kilometers above the surface and deployed
[00:47:18 - 00:47:21] The parachute or sorry, there's a type of parachute
[00:47:22 - 00:47:27] Please this print check between altitude and attitude and anything related to aerospace
[00:47:28 - 00:47:33] An attitude the parachute break that down to 240 kilometers an hour
[00:47:34 - 00:47:39] And it was unfortunately jettisoned at 1.3 kilometers above
[00:47:40 - 00:47:42] terrain
[00:47:42 - 00:47:49] Why what was supposed to happen is that the retro rockets were supposed to fire down to 4 kilometers and
[00:47:52 - 00:47:54] Then
[00:47:54 - 00:47:58] 4 kilometers an hour at 2 meters hovering and
[00:47:58 - 00:48:04] Then they were to power off the lander was going to 4 2 meters to the surface
[00:48:05 - 00:48:08] And it had a crumple zone to absorb the impact
[00:48:08 - 00:48:11] What actually happened is the parachute deployment can
[00:48:12 - 00:48:14] created a spin on the aircraft. Why?
[00:48:16 - 00:48:21] Maybe the weight was packed. I don't know why but it caused the aircraft to suddenly have a rotation juke
[00:48:21 - 00:48:27] The national measurement unit I am you had a stack overflow as a result of the excessive rotation
[00:48:28 - 00:48:33] So the navigational computer then computed that it was already at negative altitude
[00:48:34 - 00:48:40] Below the ground earth below the margin surface and it prematurely released the parachute because of thought that we'd only
[00:48:40 - 00:48:42] Parrot eating more we're already on the ground
[00:48:44 - 00:48:49] And the soft we also shut down the retro rockets because the team there that the craft was really landed
[00:48:50 - 00:48:55] And so the lander impacted the terrain at 300 kilometers an hour end of that particular lander
[00:48:57 - 00:49:01] So the question is okay, there's something wrong with the parachute the way it unfolded
[00:49:01 - 00:49:03] It got twisted or something
[00:49:04 - 00:49:06] And you can blame the mechanicals for that
[00:49:06 - 00:49:13] Good, okay. What about the control system? What responsibility can the trans students or the software students
[00:49:13 - 00:49:16] Engineers take for the control system's response
[00:49:27 - 00:49:28] Not enough wiggle room
[00:49:29 - 00:49:30] Chris, what do you think?
[00:49:31 - 00:49:34] What do you think they should have done their software design? It said you got the microphone
[00:49:34 - 00:49:37] The last few minutes is yours. Can't tell us
[00:49:40 - 00:49:42] Okay, how would you design the software to avoid this problem?
[00:49:45 - 00:49:46] Well
[00:49:46 - 00:49:50] Tasting maybe simulation of things going wrong
[00:49:50 - 00:49:52] Simulation beforehand
[00:49:52 - 00:49:58] You know you've got test stuff or inputs to the system which you don't expect to see what happens
[00:50:00 - 00:50:02] How would you handle the stack overflow?
[00:50:03 - 00:50:05] I'm not a software engineer
[00:50:05 - 00:50:08] Okay, so let's just off move on. That's the job
[00:50:08 - 00:50:10] Some error trapping would be quite good, huh?
[00:50:12 - 00:50:17] And to be honest did you did it really have to make a decision in that one millisecond or one clock cycle?
[00:50:18 - 00:50:20] It could actually have held on and just said
[00:50:21 - 00:50:25] We are the critical phase. Can we just have a little loop which we just wait
[00:50:26 - 00:50:29] 0.5 seconds to see whether or not we really are on the ground
[00:50:29 - 00:50:34] Do you know what I'm saying? There's sort of things that could possibly have been done in that particular situation
[00:50:34 - 00:50:41] Okay, thanks everyone. I hope you find that useful and next time I will speak to you. It will be about life's upless assessment
[00:50:41 - 00:50:45] Thanks Chris
[00:50:45 - 00:50:57] So
[00:51:05 - 00:51:07] I cover a little bit of
[00:51:55 - 00:51:59] We all knew about that, it's a well known problem.
[00:51:59 - 00:52:05] And it's just a pretty truck driver to check the right,
[00:52:05 - 00:52:09] which they checked the computers of the right where it was clear.
[00:52:09 - 00:52:12] The students were very strong, very strong.
[00:52:12 - 00:52:16] The police were very strong, very strong.
[00:52:16 - 00:52:18] They were very strong.
[00:52:18 - 00:52:20] They were very strong, very strong.
[00:52:20 - 00:52:22] They were very strong, very strong.
[00:52:22 - 00:52:25] It was a complex activity, it was a complex activity.
[00:52:25 - 00:52:28] So, we're very strong.
[00:52:28 - 00:52:31] Okay, thanks.
[00:54:06 - 00:54:58] I'm going to be happy to see you guys next time.

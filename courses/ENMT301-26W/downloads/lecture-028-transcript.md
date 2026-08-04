# ENMT301-26W Lecture 28 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `a494765524b9906a8ccf2b8a971485907966c99c88350e978851c12f7a9a7959`
Generated: 2026-06-06T06:09:07.203663+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:01 - 00:00:02] Okay.
[00:00:02 - 00:00:29] If you hear for Toronto 301, do you want to just come a bit closer?
[00:00:29 - 00:00:34] Because if you're not here for Toronto 101 and you're in, I'm probably going to get annoyed
[00:02:15 - 00:02:20] to say, no, if you have done the enemy stereo three labs, do they want to get the
[00:02:20 - 00:02:26] cruddy amplifier that starts not behaving all that well?
[00:02:26 - 00:02:29] Yeah?
[00:02:29 - 00:02:30] No.
[00:02:30 - 00:02:32] You got the good one?
[00:02:32 - 00:02:33] Nice.
[00:02:33 - 00:02:34] Makes like a bit easier.
[00:02:34 - 00:02:35] Yeah.
[00:02:35 - 00:02:39] I thought people were going to have a temperature category.
[00:02:39 - 00:02:40] Right.
[00:02:40 - 00:02:44] I thought they were both effects, but Rodney told me, assured me that one of them's just an
[00:02:44 - 00:02:47] bridge and it's got the cruddy motor driver.
[00:02:47 - 00:02:51] So it's got the slew rate limits and stuff on it.
[00:02:51 - 00:02:54] But anyway, that's good.
[00:02:54 - 00:03:00] One other thing I guess before I start, just thought interests sake really more than anything.
[00:03:00 - 00:03:04] Well, it's not predicting.
[00:03:04 - 00:03:11] That's why because I'm going to push it right back.
[00:03:11 - 00:03:16] Why is that one not going?
[00:03:16 - 00:03:18] Anyways, I'll now it's going.
[00:03:18 - 00:03:24] So you guys unfortunately don't get it this year because I hadn't had enough time to develop it.
[00:03:24 - 00:03:30] But going forward with the multi-dimensional modeling, what I wanted to do was get a little bit,
[00:03:30 - 00:03:33] and I think I mentioned the Simscape Multibody stuff.
[00:03:33 - 00:03:37] And so here is part of the way through the development.
[00:03:37 - 00:03:40] So in the tutorial that we did, you should recognize this.
[00:03:40 - 00:03:46] This has got the separations and slew rate limits and the POD control and all that sort of stuff.
[00:03:46 - 00:03:51] And then we've got this Simscape DC motor and the current limiters.
[00:03:51 - 00:03:54] So that should all look familiar to you.
[00:03:54 - 00:03:56] And then there's a gearbox.
[00:03:56 - 00:03:57] So that's all the same.
[00:03:57 - 00:04:06] But rather than then attaching that to a rotational and inertia and just having that one degree of freedom system that you did in the tutorial,
[00:04:06 - 00:04:12] what I've got in here is about just three-dimensional stuff.
[00:04:12 - 00:04:16] And I guess we're, what I'll have to do with teacher.
[00:04:16 - 00:04:20] As this all comes down to, there's a lot of frames because everything's in three-dimensional now.
[00:04:20 - 00:04:28] So you've got all these rigid frame transforms, which I think you probably have a little bit of an idea about from two or three and stuff last year.
[00:04:28 - 00:04:30] But there's a little bit more in it.
[00:04:30 - 00:04:35] And you've got solid blocks, so a rack which is the base, the driven wheel.
[00:04:35 - 00:04:38] And then inside here I'll show it open that up in a minute.
[00:04:38 - 00:04:46] Then you've got a prismatic joint which slides so that captures the sliding motion and then a revolute joint, which is a reserve rotation.
[00:04:46 - 00:04:51] And that's how the wheel drives this on the, on the rack.
[00:04:51 - 00:04:59] And then inside, in these carts you've got the cart body.
[00:04:59 - 00:05:05] And these bodies you can just import from solid works, like this, step files and then wheels and just frame transforms.
[00:05:05 - 00:05:15] But what this means is you can make a lot more, if I, so then you end up with a system like this when you run it.
[00:05:15 - 00:05:17] So it's not just a one-dimensional system.
[00:05:17 - 00:05:19] This comes out of all that frame.
[00:05:19 - 00:05:20] The red ones are driven wheel.
[00:05:20 - 00:05:22] These are the cart bodies.
[00:05:22 - 00:05:31] And then while they're not looking to be attached by anything there, there's a prismatic joint between them, which has got some spring stiffness.
[00:05:31 - 00:05:36] Now as not work, I haven't got friction working yet, so it starts to get a bit unstable.
[00:05:36 - 00:05:42] But when you're simulate that it's driven by that same motor and they're starting to behave like they're connected by springs.
[00:05:42 - 00:05:47] Because this is essentially what you're doing for a three-inch gear, so you don't do that just that single cart.
[00:05:47 - 00:05:51] You do three that are attached by springs. You do one which has got an inverted pendulum on it.
[00:05:51 - 00:06:00] And so again, you can get deeper into the multi domain modelling and start to have, I guess, more realistic systems.
[00:06:00 - 00:06:14] And where I've got rather basic bodies and stuff here, if you've got a design that you've built, you can export those as step files, out of solid works or whatever, and then import them and it brings all the initial properties and all that sort of stuff with it.
[00:06:14 - 00:06:19] So you can do some interesting things.
[00:06:19 - 00:06:27] Any questions about that?
[00:06:27 - 00:06:30] We'll move on and continue.
[00:06:30 - 00:06:35] So today, we're just continuing to talk about dependability, really.
[00:06:35 - 00:06:41] There's today's lecture, normally there's a lecture tomorrow, depending on how far we get through this.
[00:06:41 - 00:06:50] It's just the risk that these lecture slides basically, so we might get far enough through that we don't have to do the lecture tomorrow or it'll just be short.
[00:06:50 - 00:06:55] But in the last lecture, we were talking about dependability.
[00:06:55 - 00:06:56] What is dependability?
[00:06:56 - 00:07:00] So can anyone remember what was dependability, the definition of it?
[00:07:00 - 00:07:12] Is there a simplification of it?
[00:07:12 - 00:07:16] It doesn't fail more severely or more often than as acceptable.
[00:07:16 - 00:07:28] And so, and then those waffley terms more often, more severely and acceptable is something that you discuss with your stakeholders.
[00:07:28 - 00:07:32] And those would form parts of your requirements.
[00:07:32 - 00:07:38] And we talked about a few examples during the lecture last time.
[00:07:38 - 00:07:48] And I think we'll just get back through it because what it came down to is we have faults, which are, so here, a flaw in the system that might lead to an error.
[00:07:48 - 00:07:54] An error is an experimental discrepancy between the intended and the actual behavior which might end up causing a failure or it might not.
[00:07:54 - 00:08:01] So if it's something like a soldier bridge between ground two ground pins, that's an error, but it's unlikely to cause a failure.
[00:08:01 - 00:08:09] And then a failure is an event that occurs with the externally observable behavior, the system deviates from its specification.
[00:08:09 - 00:08:17] And there's a few examples in the lecture last time.
[00:08:17 - 00:08:29] And I guess what they show is that, not only good engineers working for places like NASA and the European Space Organization and to have land and all these sort of places,
[00:08:29 - 00:08:40] make mistakes, we can try an engineer out or engineer out these faults as much as we like, but we're getting to be using really complicated systems a lot of the time.
[00:08:40 - 00:08:45] And so it can be difficult to sort of foresee all of those.
[00:08:45 - 00:08:55] But one of the ways we try to do that is try to prevent failures by kind of cutting them off at the root.
[00:08:55 - 00:08:59] So we try to prevent fault or stop faults causing failures, right?
[00:08:59 - 00:09:04] So it is either fault prevention so that the design doesn't have any faults, fault removal.
[00:09:04 - 00:09:16] So in the fiction, for example quality assurance, fault tolerance so that if there is a fault or a failure, the system can somewhat continue to work.
[00:09:16 - 00:09:22] And then for forecasting, which is sort of feeds back into these other parts.
[00:09:22 - 00:09:32] We talked about some statistics around failures, so mean time before failing, our fairness and time, reliability and so on.
[00:09:32 - 00:09:43] And then at the end of the lecture last time, we sort of said that I guess reliability of individual components is very high.
[00:09:43 - 00:09:49] and individual components on a circuit board can last for millions of hours, typically without failing.
[00:09:49 - 00:09:55] But the systems tend to fail with reasons that haven't really changed.
[00:09:55 - 00:10:04] That's typically our environment, all sort of things like it's hot, that's dusty, or there's electrostatic discharge or vibration.
[00:10:04 - 00:10:12] Software is a different beast, software, faults and failures typically come from design flaws and there's a couple of examples around there.
[00:10:12 - 00:10:17] So the Mars Climate Orbiter, the ARN5 rocket, for example.
[00:10:17 - 00:10:27] And so trying to prevent those, you really need to make sure that your requirements are very tight or carefully defined.
[00:10:27 - 00:10:30] That's one of the best ways to do that.
[00:10:30 - 00:10:34] And so this is where we're up to now as sort of fault prevention.
[00:10:34 - 00:10:39] And so there are a number of other ways to sort of prevent faults occurring.
[00:10:39 - 00:10:42] You can keep it simple.
[00:10:42 - 00:10:49] And so if you've got a simple system, it's a lot easier to understand in their fault test.
[00:10:49 - 00:10:58] And I guess that quote there by Tony Hawe, who again I think I mentioned earlier, he developed the quick short algorithm.
[00:10:58 - 00:11:02] So if you've done cost one, two, two, you will have seen that.
[00:11:02 - 00:11:06] There are two ways of constructing a software design.
[00:11:06 - 00:11:10] One way is to make it so simple that there are obviously no deficiencies.
[00:11:10 - 00:11:14] And the other way is to make it so complicated that there are no obvious deficiencies.
[00:11:14 - 00:11:16] The first method is far more difficult.
[00:11:16 - 00:11:20] And so it is really difficult to have a complicated or a simple system.
[00:11:20 - 00:11:26] So if you have a think of row or cap and have a think of some of the ones you saw last year,
[00:11:26 - 00:11:29] would you consider those reasonably simple?
[00:11:29 - 00:11:32] Were there simple ones?
[00:11:32 - 00:11:38] Yeah. What sort of design would you consider simple?
[00:11:38 - 00:11:40] Convent harvester.
[00:11:40 - 00:11:50] I guess the Convent harvester pack up was simple, but because you needed to only hold certain weights or certain number of weights
[00:11:50 - 00:12:01] and you didn't really want the dummy weights on board, they typically had a complicated sorting mechanism inside them to push the plastic weights out the back, for example.
[00:12:01 - 00:12:10] And so it is a relatively simple pickup mechanism, but then there was some heading complexity with any other simple-ish ones.
[00:12:10 - 00:12:18] So a couple of years ago there was a team in the office.
[00:12:18 - 00:12:27] I think it was about a week away from the competition and they were quite upset because for various reasons they hadn't managed to build the design that they had intended to build.
[00:12:27 - 00:12:33] And so we talked about it and they came up with it, they were trying to put together a minimal and viable product.
[00:12:33 - 00:12:43] And so what they ended up doing was they had the chassis working because that basic chassis is really easy to get working with the sort of tutorials that you've got.
[00:12:43 - 00:12:49] And in the end they just got permanent magnets and tied them with a bit of string to the back of the robot.
[00:12:49 - 00:12:56] So it just drove over the weights and it picked up the middle ones with the permanent magnets and it couldn't pick up the plastic ones.
[00:12:56 - 00:13:01] And how do you think they did in the competition?
[00:13:01 - 00:13:03] Yeah, I totally can't third right.
[00:13:03 - 00:13:10] And so simple, didn't have particularly good navigation, it sort of bounced around the place.
[00:13:10 - 00:13:15] And so it doesn't have to be a ridiculously complicated system.
[00:13:15 - 00:13:22] And you could build a system that simple and then test it a lot and get your navigation down.
[00:13:22 - 00:13:30] Obviously there's downsides to there that's pretty hard to drop them back off your home base if they're attached with a permanent magnet, but maybe they're a waste.
[00:13:30 - 00:13:41] So keeping it simple, as much as you understand the test, prototyping is allows you to find bugs before constructing the final system.
[00:13:41 - 00:13:48] You're in an interesting situation because you're not building a system that's going to be mess manufactured right.
[00:13:48 - 00:13:52] The robot that you build is effectively a prototype.
[00:13:52 - 00:13:57] And so it's not like you perfect that and then somebody's going to go out and build thousands of those.
[00:13:57 - 00:13:59] It is just a prototype.
[00:13:59 - 00:14:07] So you still want to use testing to find bugs, but that's just for that final competition.
[00:14:08 - 00:14:11] And also modeling and simulation, which can automate testing.
[00:14:11 - 00:14:14] So it's a little bit hard to do for a robot cup.
[00:14:14 - 00:14:24] What else can you do to sort of, what sort of things can we use or techniques for stuff we can use in robot cups to sort of help folks and failures?
[00:14:24 - 00:14:42] So you could get some review by what by another team perhaps, or other members of your team to try.
[00:14:42 - 00:14:51] What sort of failures will come in last year or you noticed last year?
[00:14:51 - 00:14:58] Sorry?
[00:14:58 - 00:15:04] You're getting stuck on all, or they physically stuck or as a software issue.
[00:15:04 - 00:15:11] Yeah, there's a lot of the time it's a software issue like with the walls because you can't like it's hard to get actually stuck.
[00:15:11 - 00:15:19] But with the software issue and it's a good point, what have we got that built into the tenses that can help with that sort of thing?
[00:15:19 - 00:15:23] Yeah, watch dog time.
[00:15:23 - 00:15:27] And interestingly, a lot of people don't end up using them right.
[00:15:27 - 00:15:37] So you can have some, I guess some circumstances set up so that if it's going through or it's in the same part of your program for a longer period of time,
[00:15:37 - 00:15:40] you can trigger a watch dog timer for example.
[00:15:40 - 00:15:44] So it boots out and it goes into another part of the program, for example.
[00:15:44 - 00:15:46] You can add random behavior.
[00:15:46 - 00:15:54] So if you're backing away from an obstacle, you may be back away from a random amount of time or you turn a random amount.
[00:15:54 - 00:16:02] So you'll see and sometimes people will back off from an obstacle and then they'll just go straight back towards it and then a loop where it goes far enough
[00:16:02 - 00:16:09] away that thinks it's okay and it drives forward and it then sees the same obstacle and it's very fearful to come out of that.
[00:16:09 - 00:16:22] And so there are certainly ways that you can develop your code and so on to make it harder for failures to occur or that you can deal with,
[00:16:22 - 00:16:26] I guess make it full torrents probably a bit of work point.
[00:16:26 - 00:16:37] But that typically requires you to get on to that code fairly early so you've got time to develop that.
[00:16:37 - 00:16:39] Testing.
[00:16:39 - 00:16:49] So testing testing, more testing and often the robots that do the best have done a lot of testing.
[00:16:49 - 00:16:51] There is a downside to testing, right?
[00:16:51 - 00:16:57] Because if you do huge amounts of testing with your robot, what could that cause?
[00:16:57 - 00:16:59] Yes, you could get where in here.
[00:16:59 - 00:17:06] So there's almost a point you can't really identify necessarily but if you do lots of testing you figure out the bugs,
[00:17:06 - 00:17:15] but the downside of it is you might wear parts out which then fail on you in a critical time which will be a shame.
[00:17:15 - 00:17:32] And so doing a chunk of testing is important but sort of think about simple things like making sure that you're scoot some screws and stuff a tightened back up that parts of your robot which may get worn,
[00:17:32 - 00:17:37] get replaced or at least serviced if you like.
[00:17:37 - 00:17:40] There's other sort of fancy testing.
[00:17:40 - 00:17:46] So randomised testing so you put random inputs into your, depending on the system as you're developing.
[00:17:46 - 00:17:51] You have random inputs so you can see how it copes with that.
[00:17:51 - 00:18:01] Alpha and beta testing so you put out a system to limited base of users who know that the testing is system and can then put them in.
[00:18:01 - 00:18:06] And can then provide feedback on that and so you can get feedback on how it works.
[00:18:06 - 00:18:10] And then accelerated life testing as well.
[00:18:10 - 00:18:30] And so accelerated life testing is quite interesting and that case you basically put your system into typically something like an environmental chamber where it's run at high temperatures, maybe high levels of humidity, other environmental factors that may cause it to be a bit of a
[00:18:30 - 00:18:33] cause it to wear out.
[00:18:33 - 00:18:39] And you do that and so maybe you've got a system that said that the meantime between failure was a million years or a million hours even right.
[00:18:39 - 00:18:43] You don't have time to test a bunch of those for that length of time.
[00:18:43 - 00:18:49] And so if you put it in a harsher environment then you can test it for a shorter period of time and so achieve those failures.
[00:18:49 - 00:18:56] But what you have to do with that is then you've got to have some model that takes, you know, if you test the system at 100 degrees,
[00:18:56 - 00:19:03] that relate them to the lifespan of that system when it's operating maybe at 40 degrees where it usually operates.
[00:19:03 - 00:19:16] So you can basically accelerate the rates of failure but you've got to have some sort of model that accounts for how those environmental factors impact that life expectancy.
[00:19:16 - 00:19:30] So Hamilton Jet do quite a bit of this, especially with their controls that may be outside the boat and they can be operating in freezing environments and it's sort of water spray all over them.
[00:19:30 - 00:19:41] And so they do quite a lot of accelerated life testing and they've got environmental chambers to test how, when like joysticks and screens and controls and so on fail.
[00:19:41 - 00:19:48] So that they are confident that they're going to be able to work through, you know, that they expect their life.
[00:19:48 - 00:20:02] So fault tolerance, so as well we're sort of talking about before really some fault to always slip through and so it's best to design for your system to cope with those.
[00:20:02 - 00:20:08] Basic characteristics of fault tolerance systems that you don't really want a single point of failure.
[00:20:08 - 00:20:20] You might have some fault isolation so that if a fault occurs it doesn't cause other parts to fail or fault containment so that fault shouldn't propagate through to the era or failure.
[00:20:20 - 00:20:26] In a way to sort of start to think about your designs in terms of this is you can use reliability block diagrams.
[00:20:26 - 00:20:34] So this is a serial system so you've got a part A, if you like, in a part B and they're connected in series.
[00:20:34 - 00:20:44] So that might be on Europa Cup something like a sensor and the CPU and maybe a power system and they're effectively connected in series.
[00:20:44 - 00:20:54] And then if you know the reliability for those individual components then the total system reliability is the product of all those individual reliability's.
[00:20:54 - 00:21:07] So because those reliability's always have a value of less than one and if you've got a large number of parts that are strong to get there in series they can get the overall system reliability can get pretty low pretty quickly.
[00:21:07 - 00:21:17] So this is an example and these reliability numbers are purely made up but just to give you an idea you might have an infrared sensor that you're using for detecting weights.
[00:21:17 - 00:21:41] There's lots of physical connections in terms of wires you've got the tints that's driving it maybe there are other parts in there and if they've all got reasonably good reliability's by the time you multiply those together you're starting to get down to a lower level of reliability because if any of one of those components fail that system fails right.
[00:21:41 - 00:21:50] So if you link them in a serial fashion then you can start to run into problems.
[00:21:50 - 00:21:56] So what else could we do or if we want to avoid serial systems what options do we have?
[00:21:56 - 00:22:21] We can have some redundancy right you end up being a parallel system and so there's two main families of parallel behavior.
[00:22:21 - 00:22:33] You can have active parallel systems so you've got so these are these are RANR be a doing the same thing they are maybe CPU's for example flight computers for a rocket.
[00:22:33 - 00:22:40] They're both operating at the same time so if one of them fails the other ones still they're working.
[00:22:40 - 00:23:09] And so that's that's called hot standby another sort of version of that is modular redundancy where you might have typically would have three or more of the same things so maybe it's a sensor and that's measuring the same thing and they vote or there's a vote between them and so if one of them fails you know let's say you've got three senses measuring the same thing one of them fails the two other ones are still reading correctly and it's basically a vote in terms of which which readings do you trust.
[00:23:09 - 00:23:16] And so that gives you some sort of tolerance to a single point of failure and that sense.
[00:23:16 - 00:23:25] So if you've got an active parallel system like this so let's say we've got two flight computers the overall system reliability.
[00:23:25 - 00:23:36] So each the reliability of each of those parts amb is here so therefore the probability of failure of that part is one minus that reliability.
[00:23:36 - 00:23:42] And so the overall system reliability is one minus the product of those probabilities of failure.
[00:23:42 - 00:24:06] So if you've got for example R and R be they're both 0.9 so here if they're both 0.9 so one minus 0.9 is 0.1 right so 0.1 squared so you end up with the overall system reliability is 0.9 9 and so because you've got their active hot standby system you can increase the amount of the
[00:24:06 - 00:24:11] system you can increase reliability of those individual components.
[00:24:11 - 00:24:25] Another option is a little bit more complicated but you have standby parallel and so you've got two systems maybe the two flight computers again this one's operating this one's not operating.
[00:24:25 - 00:24:37] It does require some complicated sort of fault detection and switching for this to occur so something's got to be monitoring this and say that's working okay and if it's not working okay it switches to the other option.
[00:24:37 - 00:24:55] And so that's that standby parallel and with standby parallel you end up with with this equation here so your overall system reliability is captures the system reliability of system A and then we've got the
[00:24:55 - 00:25:22] basically one over the mean table the constant failure rate lambda times time times the reliability of of part B and so it ends up being we can see here I've got an example it ends up being quite a good way although you are adding additional complexity with this sort of standby system.
[00:25:22 - 00:25:49] So the example which again is as fictitious in terms of the values but you know if you had an unmanned space probe and it was sent out to explore this whole system and it's got a flight computer with a reliability characterised again by the exponential distribution so the same one that we've been talking about so you have a mean a mean time before failure of 30 months so that relates that converts to a constant failure rate of 0.03, 3,3,3,3,3 months.
[00:25:49 - 00:26:01] So there's a two year mission the probability of surviving that just with that single computer just using that reliability equation that we had earlier is 45%.
[00:26:01 - 00:26:11] Right so it's not a particularly highly reliable system particularly for something that's cost and awful lot of money to put up into space.
[00:26:12 - 00:26:18] And so you've got 45% chance of that computers to be operating at the end of two years.
[00:26:18 - 00:26:40] If however we had a second computer and it was in that standby mode the reliability at 24 months then becomes so using that equation there we've got the same either the new of lambda t, lambda t times either the new of lambda t and so that ends up leaving us with a probability of 0.81 of that system still operating at the end of the two years.
[00:26:40 - 00:26:49] So we've got an improved reliability for that mission.
[00:26:49 - 00:26:54] What would be the reliability if we use the active parallel system?
[00:26:54 - 00:27:20] So the equation for that is here so we've got the reliability at the end of 24 months is 0.45 and so we've got 1 minus 0.5 times 1 minus 0.45 is and then 1 minus all of that.
[00:27:20 - 00:27:25] That's pretty much 70% so 0.6975.
[00:27:25 - 00:27:44] So if you've just got that single system the reliability is 45% if you've got standby parallel the reliability is 81% if we have hot standby so the two computers operating simultaneously the reliability still be operating at the end of two years is around about 70%
[00:27:44 - 00:27:58] So you've got some decisions to make which I guess you'd make with your stakeholders who's paying for the mission how would they feel if it fails and that sort of thing.
[00:27:58 - 00:28:09] But and then there's obviously trade offs in terms of complexity so it's relatively easy to have the hot standby both of them working.
[00:28:09 - 00:28:13] It's a bit more complicated to have standby parallel
[00:28:13 - 00:28:28] but that's not to say that it won't still fail for other reasons right so they're around five rocket they had two flight computers that were identical and the way that the failure occurred was because a code was sent to the computer and it caused it to shut down.
[00:28:28 - 00:28:35] It was misinterpreted as an error code and it causing the whole system to try and do something that shouldn't have done that.
[00:28:35 - 00:28:57] So if you're not a computer, you can't have methods to mitigate some of this but doesn't necessarily mean it'll necessarily work for you.
[00:28:57 - 00:29:11] So there's a mechanical design redundancy so this is just a nice example it's a V22 Osprey tilt rotor but if there's an engine failure on this you can't
[00:29:11 - 00:29:20] rotate it like you can with a normal helicopter and so there's got to be some means that one engine can drive the other rotor if it was in a hovering situation.
[00:29:20 - 00:29:33] And so they've got this ginormous power transmission shaft that runs through the wings of it so if one engine fails the other engine can drive both rotors and so they can make an emergency landing or continue operating.
[00:29:33 - 00:29:48] Right and that I mean that in a few other aspects all the why it was such an expensive aircraft to build and maintain just because I mean it probably doesn't help that it's a familiar to operations.
[00:29:48 - 00:30:08] You have more redundancy than you would because it's a fairly hostile environment but this has got to transmit a lot of power through gearboxes and so on which then you've got to manage the potentials of failures there as well, folks and families.
[00:30:08 - 00:30:31] Okay so where do we get our reliability data from and it depends on what you're looking at a lot of electrical components for example you can get information from so like the AVR might control as you don't use those anymore on the tenses but if you just got a little like a do you know you know or now no.
[00:30:31 - 00:30:44] And this plan of information like if that's operating at 105 degrees the mean time before failures 153 years fairly reliable should last a while.
[00:30:44 - 00:31:01] And I managed to find some stuff for the in XP process that runs the TNC 4.0 which you guys have and it depends on a few situations and how it's set up in terms of the DC power to the main processor and so on.
[00:31:01 - 00:31:17] So the core speed because the core speed then relates to the temperature of the junction temperatures for example but here's an example of it I mean it can be as low as 21,000 hours of power on hours or in that particular instance up to 76,000 hours.
[00:31:17 - 00:31:26] So again it's still pretty reliable and it's unlikely that the TNC will just happen to fail on you during row of account.
[00:31:26 - 00:31:40] And other things for example if you want to find out what the you know for I don't know capacitors resistors all that sort of stuff you can often get that information from the supplier.
[00:31:40 - 00:31:51] Any questions about that? Cool okay.
[00:31:51 - 00:32:04] So we've talked about you know fault prevention we've talked about sort of redundancies of fault torrents and stuff if you like.
[00:32:04 - 00:32:18] And then the last thing on that list was planning for dependability so how do you make plans for this and so to design something to be dependable you need a bit of a definition of what it means to be dependable.
[00:32:18 - 00:32:26] And so and therefore write appropriate specifications or requirements and stuff like that and so.
[00:32:26 - 00:32:44] As I mentioned earlier you know what is an acceptable security failure what so for robot cup what would be acceptable maybe maybe think about the locomotion system because obviously there's a lot of different subsystems that could go wrong what would be an acceptable level of.
[00:32:44 - 00:32:52] What would you have a severity failure and what you quantify.
[00:32:52 - 00:33:02] I don't know if I've gone to five but maybe like doesn't then it's round you can start it without.
[00:33:02 - 00:33:12] Yeah for example so maybe like it's repairable within repairable within some finite amount of time you know that means maybe you can take.
[00:33:12 - 00:33:19] And it depends you know if we're talking about locomotion system it's relatively easy to get stuff on the side something like that would be would be good.
[00:33:19 - 00:33:27] What else might be maybe do you want to just say it doesn't it doesn't crash it will not stop working.
[00:33:27 - 00:33:41] Something like that would be nice but it's never going to be the case right it's not really realistic sort of requirement because unfortunately things go wrong.
[00:33:41 - 00:33:47] And so what's an acceptable failure rate then again maybe for.
[00:33:47 - 00:33:54] So the locomotion system.
[00:33:54 - 00:34:00] How many so the rounds of two minutes each roughly how many rounds do you think you might go through.
[00:34:00 - 00:34:10] So more than what yeah well you will go through more than one because it's double elimination so you have to lose twice to get knocked out so you go through two rounds.
[00:34:10 - 00:34:15] So I'll operate for more than four minutes ideally right to have a chance.
[00:34:15 - 00:34:30] And it depends I think last year I think we had maybe 39 teams might be at 40 teams and so I think the winning team might have competed in eight rounds you can get information on learn some of the other teams depending on how you win.
[00:34:30 - 00:34:39] Might have competed in sort of 12 rounds at most right so 12 rounds say we'll just say 10 rounds right so it's got to be operate for 20 minutes without failure.
[00:34:39 - 00:34:50] Or at least you know you might say maybe it can operate for 10 minutes without failure and then you can fix it within a certain period of time.
[00:34:50 - 00:35:00] Because that failure may not end up and you're losing the competition you know you might have picked up some weights and the tracks fall off and then you still happen to win.
[00:35:00 - 00:35:04] But these are things that you need to kind of have a think about.
[00:35:04 - 00:35:09] Yeah out in the real world you'll have a think about those and discuss some of your clients and stakeholders.
[00:35:09 - 00:35:21] In terms of this competition you know this is something you need to discuss amongst your teams and figure out you know what sort of requirements you want to have around these sort of aspects.
[00:35:21 - 00:35:51] And so yeah and one thing that's there's a paper I've got a link there and you can there's a link to it on the learn page it's now 20 years old so it's 2005 but it was a group and they looked at the failure rates of unmanned ground vehicles in the field and so a lot of these were you know such risky type vehicles and things like that.
[00:35:51 - 00:36:09] And we've had 20 years to improve but what do you think the sort of mean time between failure was for these UGV so these are generally commercial or military type UGV's.
[00:36:09 - 00:36:17] There's six to 20 hours was the mean which is not a lot of operating time right.
[00:36:17 - 00:36:33] One of them they pointed out which I think was this so this was in that paper and they're talking about the Panther study which was I guess done by the Department of Defense and it was a they'd used an M1A
[00:36:33 - 00:36:40] and the new brooms tank and I guess they were making an unmanned mind clearing device from it.
[00:36:40 - 00:36:50] And it had 35 failures in 32 days of operation but some of them are quite interesting.
[00:36:50 - 00:36:57] Symptoms range from sluggishness to a complete loss of steering sometimes manifesting the only one direction of the time.
[00:36:57 - 00:37:08] So it's a very risky stop switch failed multiple times. It's not so good when you've got a 60 tons hang.
[00:37:08 - 00:37:11] Well with a 60 ton tank.
[00:37:11 - 00:37:15] It's dangerous right.
[00:37:15 - 00:37:23] The funny project team last year and the year before that I was supervising for the hybrid rocket for the UC aerospace.
[00:37:23 - 00:37:32] They had e-stops but we made sure that e-stop actually cut the physical power to the rocket the entire system.
[00:37:32 - 00:37:40] The power was routed 50 meters back and then 50 meters through the e-stop so that if something went wrong.
[00:37:40 - 00:37:49] You could have an e-stop wide into a processor right but if you've got something wrong with your code or something like that it may not stop.
[00:37:49 - 00:38:03] And so they had that and it turned out two years ago that was quite good because everything else in the system failed in terms of how they were trying to control it and the only thing they could do is they used the e-stop to start and stop it.
[00:38:03 - 00:38:08] So they could have power and they have it running so the e-stop was off and then they wanted it to run.
[00:38:08 - 00:38:16] You just will engage the e-stop disengaged it if you like and then it ran and then you pushed it back down so it just became the switch.
[00:38:16 - 00:38:20] Which is less than ideal.
[00:38:20 - 00:38:25] Yeah obviously it was a reported failures include uncontrolled acceleration.
[00:38:25 - 00:38:30] The RPM shooting up to a critical level for no apparent reason.
[00:38:30 - 00:38:35] A system shut down when you operate a try to switch to tell the operation mode.
[00:38:35 - 00:38:40] This sort of stuff happens all the time.
[00:38:40 - 00:38:46] And I guess make sure e-stops will work properly.
[00:38:46 - 00:38:51] But how do we do the planning for this dependability?
[00:38:51 - 00:38:55] And so there's a couple of systematic methods right.
[00:38:55 - 00:39:01] One is you consider the sources of your fault so which faults can you safely ignore as too unlikely?
[00:39:01 - 00:39:04] Be careful with that because sometimes they come back and bite you.
[00:39:04 - 00:39:12] Which faults will not adversely affect the overall system so it can still work even if those faults occur.
[00:39:12 - 00:39:15] And which faults do you need to protect against?
[00:39:15 - 00:39:19] And so once you've found that set of faults, that basically forms your fault model.
[00:39:19 - 00:39:24] And then you can decide what you want to do about that in terms of whether you've got quality assurance.
[00:39:24 - 00:39:26] It's particularly testing for that.
[00:39:26 - 00:39:28] Maybe you're doing additional testing.
[00:39:28 - 00:39:31] Maybe you've got some fault tolerance built around that.
[00:39:31 - 00:39:36] And so, yeah, basically can you prevent them?
[00:39:36 - 00:39:37] Can you remove them?
[00:39:37 - 00:39:43] Can you develop your system so that it can work in the presence of those faults?
[00:39:43 - 00:39:50] Or at least fail gracefully rather than blowing up, for example.
[00:39:50 - 00:39:55] So there's some systematic techniques for reliability analysis.
[00:39:55 - 00:40:01] And so there's fault tree analysis which I'm not going to talk much about now because
[00:40:01 - 00:40:05] Dirk Ponds is going to give you a bit of a lecture on it next week.
[00:40:05 - 00:40:10] I think I'll do maybe in this slot next week.
[00:40:10 - 00:40:15] So fault tree is a top down approach and I quite like it and you have to do one of these in
[00:40:15 - 00:40:16] robocup.
[00:40:16 - 00:40:22] And I think the reason it's quite useful is it kind of follows the way that you are or should
[00:40:22 - 00:40:26] be debugging a system in terms of your start at the top.
[00:40:26 - 00:40:30] So it might be something like robocup robot doesn't pick up weight.
[00:40:30 - 00:40:32] Like, okay, what could it cause that?
[00:40:32 - 00:40:34] So maybe the pickup mechanism failed.
[00:40:34 - 00:40:38] Maybe the sensor mechanism didn't see the weight.
[00:40:38 - 00:40:40] Maybe I don't know something else.
[00:40:40 - 00:40:46] And then so you work down from the top of ends down through the possible causes of that.
[00:40:46 - 00:40:48] And you have logical gates.
[00:40:48 - 00:40:50] So you have like and or type gates.
[00:40:50 - 00:40:56] So it could be that two or three things are contributing to one of those fails with an
[00:40:56 - 00:41:01] sort of behavior or they could be an or sort of behavior.
[00:41:01 - 00:41:06] But that's kind of how you debug systems.
[00:41:06 - 00:41:09] And so how many of you have had some experience having to debug a system probably
[00:41:09 - 00:41:12] line for a robot for example, right?
[00:41:12 - 00:41:19] I know when I started thinking about debugging systems like this.
[00:41:19 - 00:41:24] And I don't know if it becomes naturally because sometimes when you're running
[00:41:24 - 00:41:28] labs for like three, one, three, for example, for the mechanical class,
[00:41:28 - 00:41:30] you go and talk to them and something's wrong.
[00:41:30 - 00:41:33] And then they don't sort of stop and think, all right, you know,
[00:41:33 - 00:41:35] what have I got power to the system?
[00:41:35 - 00:41:38] Have I got a signal connection?
[00:41:38 - 00:41:42] Often they just dive in and start making random adjustments to their code,
[00:41:42 - 00:41:47] which is not the best way to do it.
[00:41:47 - 00:41:52] And so, you know, sort of thinking about debugging this top down approach is quite a good way of doing it.
[00:41:52 - 00:41:55] You know, what are the main things that what you're seeing?
[00:41:55 - 00:41:56] What could cause that?
[00:41:56 - 00:41:58] And then working back from that.
[00:41:58 - 00:42:00] Anyway, a difficult talk a bit more about that.
[00:42:00 - 00:42:05] And you'll end up with something like this or an expanded form of this
[00:42:05 - 00:42:13] and your Robocup second report and your progress report.
[00:42:13 - 00:42:18] So the other method which occurs reasonably commonly in industries,
[00:42:18 - 00:42:21] if in me, A is a fairly important effect analysis.
[00:42:21 - 00:42:26] So back in inch 101, you did hazard analysis, right?
[00:42:26 - 00:42:30] And so that is basically a method for looking at, you know,
[00:42:30 - 00:42:34] what things might cause you to get physically hurt, right?
[00:42:34 - 00:42:39] If in me A is basically like that, but rather than for you or the system
[00:42:39 - 00:42:45] to get physically hurt, it's looking at the system to fail to do what it needs to do.
[00:42:45 - 00:42:49] So you start at the bottom up and you look at each component or element of the system.
[00:42:49 - 00:42:54] You look at which, you know, what is the likelihood of each of those causing a failure?
[00:42:54 - 00:42:58] What are the effects of that failure and how critical would that failure be?
[00:42:58 - 00:43:02] And so it very much is like a hazard analysis, but it's from bottom up.
[00:43:02 - 00:43:07] But as I said, rather than looking at the harm that it can do to use,
[00:43:07 - 00:43:10] as it considers sort of the overall requirements, right?
[00:43:10 - 00:43:12] And so not being able to achieve those.
[00:43:12 - 00:43:18] And so safety, which is harm to humans, should be built into your requirements.
[00:43:18 - 00:43:22] But also those requirements are being achieved.
[00:43:22 - 00:43:26] That's what your customers are after.
[00:43:26 - 00:43:32] And so normally you deal with a thermostat colders and you'll have some sort of scoring system.
[00:43:32 - 00:43:39] And so for each component or function or input, you determine the ways it could go wrong.
[00:43:39 - 00:43:45] And then for each of those failure modes, you then determine the effects of how bad is that failure.
[00:43:45 - 00:43:48] And you choose a severity score.
[00:43:48 - 00:43:51] And so that's very much like the severity scores that you have for hazard analysis.
[00:43:51 - 00:43:54] Then you identify potential causes of each failure mode.
[00:43:54 - 00:43:56] So why would it occur? How much would it occur?
[00:43:56 - 00:43:58] So you haven't had a current score.
[00:43:58 - 00:44:02] Then you'll list the current controls for the course.
[00:44:02 - 00:44:06] So do you have anything in there to prevent their occurring?
[00:44:06 - 00:44:08] And so that's a detection or prevention score.
[00:44:08 - 00:44:12] And then you multiply them up just like you do with a hazard analysis.
[00:44:12 - 00:44:15] And that gives you a risk priority number.
[00:44:15 - 00:44:23] And then you may, if you get a high number for that, you may then develop some actions that you would do.
[00:44:23 - 00:44:25] And so you'd have a template like this.
[00:44:25 - 00:44:29] And it looks very much like what you have with those hazard analysis as well.
[00:44:29 - 00:44:34] So you've got a severity score, the current score, detection prevention, more apply it.
[00:44:34 - 00:44:35] And then what can you do?
[00:44:35 - 00:44:41] And then once you've made those actions, you redo the process because if you've introduced anything to that system to affect the
[00:44:41 - 00:44:47] effects there, you might actually have introduced another failure mode that you had considered.
[00:44:47 - 00:44:50] And so then, I mean, here's a standard issue.
[00:44:50 - 00:44:54] Actually going back to that, this template was from Fontara.
[00:44:54 - 00:44:59] I don't know if they use exactly the same template, but it's the same one in most industry organizations.
[00:44:59 - 00:45:00] I'll have something similar.
[00:45:00 - 00:45:03] They have a scoring system like this.
[00:45:03 - 00:45:09] So your severity score is things like may result in a safety issue or regulatory violation for a 10,
[00:45:09 - 00:45:13] or five as secondary function to reduce all the customers impacted.
[00:45:13 - 00:45:15] For example, ones little or no impact.
[00:45:15 - 00:45:19] The occurrence scores 10 certain, so daily occurrence.
[00:45:19 - 00:45:22] Five is likely ones almost impossible.
[00:45:22 - 00:45:29] Likelihood of detection is absolutely uncertain that the failure would be detected or prevented,
[00:45:29 - 00:45:32] going down to almost certain that the failure would be detected or prevented.
[00:45:32 - 00:45:34] So you might apply these all up.
[00:45:34 - 00:45:44] And it identifies the ways that a product would fail, but also by the likelihood of it occurring.
[00:45:44 - 00:45:46] I suppose estimates are risk associated with that.
[00:45:46 - 00:45:49] And that allows you to prioritize the actions.
[00:45:49 - 00:45:54] But the one thing that it doesn't consider multiple failures at once.
[00:45:54 - 00:45:57] So the top down you can have an end-and-aw type behavior.
[00:45:57 - 00:46:02] But if you may aid doesn't, you've got these systems and you're treating them in isolation.
[00:46:02 - 00:46:12] So, if you had system A and system B, and together they can cause something that would necessarily occur independently,
[00:46:12 - 00:46:19] that's not captured by the FMEA process.
[00:46:19 - 00:46:23] When I was looking for the stages ago I found this.
[00:46:23 - 00:46:28] FMEA for the death star, thermal exhaust course.
[00:46:28 - 00:46:33] Anyway, it's quite funny.
[00:46:33 - 00:46:39] So that's how you kind of start.
[00:46:39 - 00:46:42] And it occurs in industry planning for dependability.
[00:46:42 - 00:46:44] You might use something like a fault tree analysis.
[00:46:44 - 00:46:49] Because the idea with the fault tree with the rubber cup is that you make you do it.
[00:46:49 - 00:46:51] A, it's good for you to have done one.
[00:46:51 - 00:46:58] But be hopefully in going through that process it makes you think about some of the ways that your system might fail.
[00:46:58 - 00:47:01] And then you can do something about that.
[00:47:01 - 00:47:08] And hopefully reduce the number of failures.
[00:47:08 - 00:47:21] So, well, in summary then, with this dependability, we've got this chain of events where you have a fault that leads to an error which can lead to a failure.
[00:47:21 - 00:47:28] The general gist of this is if you remove or reduce your faults, you can prevent failures.
[00:47:28 - 00:47:31] To do those, you can prevent the faults.
[00:47:31 - 00:47:33] You can remove it with quality assurance.
[00:47:33 - 00:47:35] You can have some tolerance to it.
[00:47:35 - 00:47:41] You can predict because then if you predict that allows you to go back and think about these.
[00:47:41 - 00:47:48] So, planning for dependability and design for manufacture, for use maintenance, all of these sorts of things.
[00:47:48 - 00:47:54] You know, some of that plan for dependability might not be something that you can do in the design side,
[00:47:54 - 00:47:57] but that may then impact something about maintenance.
[00:47:57 - 00:48:06] You might in the user manual say that this system that you've designed has to be maintained at whatever regular period of time, for example.
[00:48:06 - 00:48:08] And bits and pieces like that.
[00:48:08 - 00:48:15] So, you can put some information out there to the customers about that.
[00:48:15 - 00:48:18] Good. So, that's, well, that's dependability.
[00:48:18 - 00:48:20] Is there any questions about that?
[00:48:20 - 00:48:23] I don't know.
[00:48:23 - 00:48:26] That's five o'clock on a Wednesday on neck.
[00:48:26 - 00:48:29] But the good thing is we've got two of those lectures.
[00:48:29 - 00:48:31] So, you'll probably cancel tomorrow's lecture.
[00:48:31 - 00:48:36] I'll send out a message on learn about that.
[00:48:36 - 00:48:37] But, cool.
[00:48:37 - 00:48:39] Otherwise, thanks for coming.
[00:48:39 - 00:48:45] And, well, I'll see you on Friday because Dominique will be giving the sick and
[00:48:45 - 00:48:47] the next lecture about writing.
[00:48:47 - 00:48:55] And I think there's more in there about using AI to help you write well, as well as some other aspects as well.
[00:48:55 - 00:48:57] So, you'll see it then.
[00:48:57 - 00:48:59] So, what is it?
[00:48:59 - 00:49:10] No, it's good.
[00:49:10 - 00:49:12] What's the second?
[00:49:12 - 00:49:14] Yeah, yeah.
[00:49:14 - 00:49:16] And I might have better than it.
[00:49:16 - 00:49:18] I'm not sure about it.
[00:49:18 - 00:49:20] No, I'm not sure.
[00:49:20 - 00:49:22] You might have.
[00:49:22 - 00:49:24] You might have.
[00:49:24 - 00:49:26] You might have.
[00:49:26 - 00:49:28] You might have.
[00:49:28 - 00:49:30] You might have.
[00:49:30 - 00:49:32] You might have.
[00:49:33 - 00:49:36] I integrity?
[00:49:36 - 00:49:38] I'm not familiar.
[00:49:38 - 00:49:41] Do you know to talk about this?
[00:49:41 - 00:49:42] I would go in a way that somehow, how is it going?
[00:49:42 - 00:49:43] How is it going?
[00:49:43 - 00:49:44] How do you know?
[00:49:44 - 00:49:45] How do you know?
[00:49:45 - 00:49:46] How do you know the.
[00:49:46 - 00:49:47] How do you know the.
[00:49:47 - 00:49:48] How do you know the?
[00:49:48 - 00:49:49] How do you know the?
[00:49:49 - 00:49:50] How?
[00:49:50 - 00:49:51] How do you go?
[00:49:51 - 00:49:52] I have to go on for you.
[00:49:52 - 00:49:53] The rest.
[00:49:53 - 00:49:54] I think.
[00:49:54 - 00:49:55] Can I see?
[00:49:55 - 00:49:56] So, Lynn, what are you telling me?
[00:49:56 - 00:49:57] What about?
[00:49:57 - 00:49:58] I think I'm like, what about that?
[00:49:58 - 00:50:01] I think it's still a cone wheels, all my counts are about,
[00:50:01 - 00:50:03] but they're not quite high, I suppose.
[00:50:03 - 00:50:04] That'd be great.
[00:50:04 - 00:50:05] Yep.
[00:50:05 - 00:50:08] That's why, because I figured if I said just rubber bands,
[00:50:08 - 00:50:10] people just get, I don't know, less,
[00:50:10 - 00:50:12] less, like, less, something else.
[00:50:12 - 00:50:15] So I had to come up with some definition.
[00:50:15 - 00:50:18] And I don't mind, like, because you can also do a common one
[00:50:18 - 00:50:22] with rigid stuff, but I figured it would just cause some creativity.
[00:50:22 - 00:50:24] And so that's cool.
[00:50:24 - 00:50:25] Yeah.
[00:50:25 - 00:50:27] Is that next right?
[00:50:27 - 00:50:28] Should we pull through?
[00:50:28 - 00:50:29] Yes.
[00:50:29 - 00:50:30] Okay.
[00:50:30 - 00:50:32] I'll try it out a little bit.
[00:50:32 - 00:50:33] I'll try it out a little bit.
[00:50:33 - 00:50:35] Yesterday, would you, I'd spend this.
[00:50:35 - 00:50:36] Yeah.
[00:50:36 - 00:50:37] So let's try it out.
[00:50:37 - 00:50:39] Whatever the front end of the floor is.
[00:50:39 - 00:50:40] Yeah.
[00:50:40 - 00:50:41] Very good.
[00:50:41 - 00:50:42] Oh, yeah.
[00:50:42 - 00:50:43] Oh, yeah.
[00:50:43 - 00:50:44] Oh, yeah.
[00:50:44 - 00:50:45] Oh, yeah.
[00:50:45 - 00:50:46] Yeah.
[00:50:46 - 00:50:47] Oh, yeah.
[00:50:47 - 00:50:48] Oh, yeah.
[00:50:48 - 00:50:49] Oh, yeah.
[00:50:49 - 00:50:50] Oh, yeah.
[00:50:50 - 00:50:51] Oh, it's like one.
[00:50:51 - 00:50:52] They're so big, no, no.
[00:50:52 - 00:50:53] They're so big.
[00:50:53 - 00:50:54] They're so big.
[00:50:54 - 00:50:55] Oh, yeah.
[00:50:55 - 00:50:56] Sorry.
[00:50:56 - 00:50:57] Oh, yeah.
[00:50:57 - 00:50:58] Yeah.
[00:50:58 - 00:50:59] I don't want to see that.
[00:50:59 - 00:51:00] Yeah.
[00:51:00 - 00:51:01] They're so big.
[00:51:01 - 00:51:02] Yes.
[00:51:02 - 00:51:03] Uh, yeah.
[00:51:03 - 00:51:04] Um, right.
[00:51:04 - 00:51:05] Okay.
[00:51:05 - 00:51:06] So I'll try it.
[00:51:06 - 00:51:07] I'll try it to.
[00:51:07 - 00:51:08] So I'll try it to.
[00:51:08 - 00:51:09] I'll try it.
[00:51:09 - 00:51:10] I'll try anything.
[00:51:10 - 00:51:11] And I'll try it.
[00:51:11 - 00:51:12] Wait.
[00:51:12 - 00:51:13] You can't tell me what you're doing.
[00:51:13 - 00:51:14] I don't want to try it.
[00:51:14 - 00:51:15] I'm trying to get you to.
[00:51:15 - 00:51:16] I'm trying to get you to.
[00:51:16 - 00:51:17] Yeah, I'm trying to get you to.
[00:51:17 - 00:51:18] Oh, what was it?
[00:51:18 - 00:51:19] It's easier.
[00:51:19 - 00:51:20] How are you?
[00:51:20 - 00:51:22] I'm going to try to eat a little bit.
[00:51:22 - 00:51:23] Let's do this.
[00:51:23 - 00:51:24] So we're going to go home.
[00:51:24 - 00:51:25] Come on, listen.
[00:51:25 - 00:51:28] Wow, it's very starting, but I know how money is going to be good.
[00:51:28 - 00:51:30] Next day, it is.
[00:51:30 - 00:51:32] It's weird how it's going to be good.
[00:51:32 - 00:51:34] It's still up.
[00:51:34 - 00:51:36] All the great brands I'd be like,
[00:51:36 - 00:51:38] they're like, they're all that good.
[00:51:38 - 00:51:39] They're all that good.
[00:51:39 - 00:51:40] They're all that good.
[00:51:40 - 00:51:42] Is that what it's going to cry?
[00:51:42 - 00:51:43] Yeah.
[00:51:43 - 00:51:45] Give me a quick drink, or something.
[00:51:45 - 00:51:46] Yeah.
[00:51:46 - 00:51:47] Time to take you in.
[00:51:47 - 00:51:51] Would you like to add a couple of things?
[00:51:51 - 00:51:53] Do you want to add a couple of things?
[00:51:53 - 00:51:55] One, two, three.
[00:51:55 - 00:51:57] One, two, three.
[00:51:57 - 00:51:59] What time does it feel?
[00:51:59 - 00:52:00] Yeah.
[00:52:00 - 00:52:01] Oh.
[00:52:01 - 00:52:04] You know, you're a lot of good.
[00:52:04 - 00:52:07] We should be doing a lot of things.
[00:52:07 - 00:52:08] Yeah.
[00:52:08 - 00:52:10] You know, these nickshows.
[00:52:10 - 00:52:12] You know, it has problems.
[00:52:12 - 00:52:14] You know, they usually get good.
[00:52:14 - 00:52:16] They're probably, like,
[00:52:46 - 00:52:49] and then he's turning to us to the past.
[00:52:49 - 00:52:50] And she's like, she's like,
[00:52:50 - 00:52:51] but this is probably like,
[00:52:51 - 00:52:53] it goes down to your report,
[00:52:53 - 00:52:54] if you want to like,
[00:52:54 - 00:52:55] you know, like,
[00:52:55 - 00:52:56] you know, like,
[00:52:56 - 00:52:57] you know, like,
[00:52:57 - 00:52:58] you know, like,
[00:52:58 - 00:52:59] you know,
[00:52:59 - 00:53:00] something to jump,
[00:53:00 - 00:53:01] it's a jump,
[00:53:01 - 00:53:02] it's a jump,
[00:53:02 - 00:53:03] it's like,
[00:53:03 - 00:53:04] it's like,
[00:53:04 - 00:53:05] it's like,
[00:53:05 - 00:53:06] it's like,
[00:53:06 - 00:53:07] it's like,
[00:53:07 - 00:53:08] what about this?
[00:53:08 - 00:53:09] It's a big,
[00:53:09 - 00:53:10] a lot of guys.
[00:53:10 - 00:53:12] And it's,
[00:53:12 - 00:53:13] the other one,
[00:53:13 - 00:53:14] it's just,
[00:53:14 - 00:53:15] like,
[00:53:15 - 00:53:16] not the bludual,
[00:53:16 - 00:53:17] but we're not Mr. Lane.
[00:53:17 - 00:53:18] There we go.
[00:53:18 - 00:53:19] The claim,
[00:53:19 - 00:53:20] the need to vote.
[00:53:20 - 00:53:21] I mean,
[00:53:21 - 00:53:22] what's the need to do?
[00:53:22 - 00:53:23] What's the need to do?
[00:53:23 - 00:53:24] I'm going to do it.
[00:53:24 - 00:53:25] I'm going to do it.
[00:53:25 - 00:53:27] Is that actually useful for real?
[00:53:27 - 00:53:28] Um,
[00:53:28 - 00:53:29] yeah, I don't know.
[00:53:29 - 00:53:30] Okay,
[00:53:30 - 00:53:31] we've tested,
[00:53:31 - 00:53:32] that's all we've done.
[00:53:32 - 00:53:33] I have not forgotten.
[00:53:33 - 00:53:34] So,
[00:53:34 - 00:53:35] no,
[00:53:35 - 00:53:36] that's so fine.
[00:53:36 - 00:53:37] Wait, do you mean the one that's going to be right?
[00:53:37 - 00:53:39] He's just doing very structured,
[00:53:39 - 00:53:41] and so now he's not very happy.
[00:53:41 - 00:53:42] So,
[00:53:42 - 00:53:43] it's not a party.
[00:53:43 - 00:53:44] We're not going to do that,
[00:53:44 - 00:53:45] but it's not.
[00:53:45 - 00:53:46] I'm going to do it.
[00:53:46 - 00:53:47] I guess.
[00:53:47 - 00:53:48] Oh,
[00:53:48 - 00:53:49] bro,
[00:53:49 - 00:53:50] I don't like it.
[00:53:50 - 00:53:51] I can like those,
[00:53:51 - 00:53:52] but it's not.
[00:53:52 - 00:53:53] I think it's not a party.
[00:53:53 - 00:53:54] I think it's a party.
[00:53:54 - 00:53:55] It's like,
[00:53:55 - 00:53:56] it's a party.
[00:53:56 - 00:53:57] It's a party.
[00:53:57 - 00:53:58] It's a party.
[00:53:58 - 00:53:59] It's a party.
[00:53:59 - 00:54:00] I'm really well-cared.
[00:54:00 - 00:54:01] So,
[00:54:01 - 00:54:02] so,
[00:54:02 - 00:54:03] but then I'm going to go,
[00:54:03 - 00:54:04] what?
[00:54:04 - 00:54:05] Because it's out in the floor,
[00:54:05 - 00:54:06] it's a party.
[00:54:06 - 00:54:07] Oh,
[00:54:07 - 00:54:08] okay.
[00:54:08 - 00:54:09] So,
[00:54:09 - 00:54:10] I'm going to,
[00:54:10 - 00:54:11] I'm going to,
[00:54:11 - 00:54:12] yeah.
[00:54:12 - 00:54:13] It's all right.
[00:54:13 - 00:54:14] I don't got it.
[00:54:14 - 00:54:15] I like it.
[00:54:15 - 00:54:24] My eyes are so same,
[00:54:24 - 00:54:25] so you're fine.
[00:54:25 - 00:54:26] I'm fine.
[00:54:26 - 00:54:27] Do you think there's a party that you've had?
[00:54:27 - 00:54:28] I'm fine.
[00:54:28 - 00:54:29] I'd have a party.
[00:54:29 - 00:54:30] The white side that you've had,
[00:54:30 - 00:54:31] I'm not a party.
[00:54:31 - 00:54:32] You're fine.
[00:54:32 - 00:54:33] So you're fine?
[00:54:33 - 00:54:34] So it's just,
[00:54:34 - 00:54:35] what's your five-so-side?
[00:54:35 - 00:54:36] It's just like a game.
[00:54:36 - 00:54:37] A,
[00:54:37 - 00:54:38] yeah.
[00:54:38 - 00:54:39] I think...
[00:54:39 - 00:54:40] Okay.
[00:54:40 - 00:54:41] Yeah.
[00:54:41 - 00:54:43] I'm just going to go to the department of my family.
[00:54:43 - 00:54:46] I'm just going to go to the department of my family.
[00:54:46 - 00:54:50] There wasn't a chance.
[00:54:50 - 00:54:54] The only thing that this is hard to shoot is your office.
[00:54:54 - 00:54:56] I'm just going to be there.
[00:54:56 - 00:54:58] I'm going to make it any further.
[00:54:58 - 00:55:01] I'm going to make it through the asset funds and the other funds.

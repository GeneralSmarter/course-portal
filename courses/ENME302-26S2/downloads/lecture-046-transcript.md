# ENME302-26S2 Lecture 46 native Echo transcript

Date: October 14, 2026 11:00am-11:55am
Transcript type: native Echo automated transcript.

[00:00:04:150 - 00:00:04:159] **Speaker 0:** So.
[00:00:09:439 - 00:00:13:000] **Speaker 1:** Can you seems far away.
[00:00:14:310 - 00:00:16:329] **Speaker 1:** Is that sort of, yeah, but.
[00:00:17:110 - 00:00:18:250] **Speaker 0:** I turn that on or off, but.
[00:00:21:319 - 00:00:21:329] **Speaker 0:** And.
[00:00:25:260 - 00:00:25:299] **Speaker 0:** Zoom in.
[00:00:28:049 - 00:00:28:120] **Speaker 1:** No.
[00:00:28:649 - 00:00:29:610] **Speaker 1:** Yeah, that's the same.
[00:00:29:889 - 00:00:30:209] **Speaker 0:** Oh.
[00:00:40:770 - 00:00:44:130] **Speaker 0:** That would be cool No Right.
[00:00:48:310 - 00:00:48:369] **Speaker 0:** No, uh.
[00:00:52:110 - 00:00:58:380] **Speaker 0:** Well, I imagine, so they might be over that, but
[00:00:58:380 - 00:01:00:389] **Speaker 2:** I'm not, I've written the exam already, so, yeah.
[00:01:04:638 - 00:01:06:138] **Speaker 0:** That's, yeah.
[00:01:07:239 - 00:01:09:540] **Speaker 1:** You'll probably start OK.
[00:01:10:250 - 00:01:12:949] **Speaker 2:** Um, we've got Theo, as I mentioned in the, the
[00:01:12:949 - 00:01:15:989] **Speaker 2:** learn post on Monday, um, so I'll let him.
[00:01:17:300 - 00:01:22:019] **Speaker 2:** Hi everyone, I'm Theo Ankerville, I'm senior TA for the
[00:01:22:019 - 00:01:22:339] **Speaker 1:** course.
[00:01:22:419 - 00:01:23:930] **Speaker 1:** I hope you all know that at this point in
[00:01:23:930 - 00:01:24:720] **Speaker 1:** the course, otherwise.
[00:01:26:230 - 00:01:28:589] **Speaker 1:** You might have a lot of studying to do um
[00:01:28:589 - 00:01:29:809] **Speaker 1:** if you haven't been to the labs.
[00:01:30:250 - 00:01:34:589] **Speaker 1:** OK, so, um, firstly I just wanted to say like
[00:01:34:589 - 00:01:36:110] **Speaker 1:** thank you so many people for coming.
[00:01:36:190 - 00:01:38:669] **Speaker 1:** I gave a guest lecture for the CFD course last
[00:01:38:669 - 00:01:40:669] **Speaker 1:** semester and there were like 4 people there, so.
[00:01:41:389 - 00:01:42:949] **Speaker 1:** I guess it was a little bit less stressful, but
[00:01:42:949 - 00:01:45:430] **Speaker 1:** like, it's also nice to have people to, to talk
[00:01:45:430 - 00:01:45:809] **Speaker 1:** to.
[00:01:46:309 - 00:01:49:760] **Speaker 1:** Um, I don't usually get super nervous for presentations, but
[00:01:49:760 - 00:01:52:230] **Speaker 1:** uh this is like the first like full length lecture
[00:01:52:230 - 00:01:52:809] **Speaker 1:** that I've given.
[00:01:53:349 - 00:01:54:989] **Speaker 1:** So I am a bit nervous, so bear with me.
[00:01:55:110 - 00:01:58:029] **Speaker 1:** um I've brought chocolate to bribe you in case my
[00:01:58:029 - 00:02:02:129] **Speaker 1:** teaching is bad, um, so hopefully that'll, that'll compensate.
[00:02:02:669 - 00:02:04:569] **Speaker 1:** Um, I want to talk about today.
[00:02:05:389 - 00:02:08:320] **Speaker 1:** Um, about a few things, but mostly about the, the
[00:02:08:449 - 00:02:11:419] **Speaker 1:** numerical simulation method that I use for my research, the
[00:02:11:419 - 00:02:12:419] **Speaker 1:** boundary element method.
[00:02:12:880 - 00:02:15:100] **Speaker 1:** Um, this is the first time that I've had a
[00:02:15:100 - 00:02:17:860] **Speaker 1:** long enough time slot to try and give some kind
[00:02:17:860 - 00:02:20:369] **Speaker 1:** of proper explanation of it, um.
[00:02:21:399 - 00:02:22:919] **Speaker 1:** So that might also be a train wreck.
[00:02:23:240 - 00:02:26:440] **Speaker 1:** Hopefully it works out and you understand, but it, it
[00:02:26:440 - 00:02:27:839] **Speaker 1:** took me about 2 years to get my head around
[00:02:27:839 - 00:02:29:919] **Speaker 1:** it, so if you don't get it in 20 minutes,
[00:02:30:039 - 00:02:30:860] **Speaker 1:** don't feel bad.
[00:02:31:479 - 00:02:31:919] **Speaker 1:** Um.
[00:02:32:839 - 00:02:36:070] **Speaker 1:** Yeah, so the things that I'm gonna cover today, I'm
[00:02:36:070 - 00:02:41:500] **Speaker 1:** going to briefly contextualise, um, numerical methods in, in the
[00:02:41:500 - 00:02:42:050] **Speaker 1:** course.
[00:02:42:389 - 00:02:44:869] **Speaker 1:** Um, I'm going to talk about computational fluid dynamics a
[00:02:44:869 - 00:02:48:070] **Speaker 1:** little bit because that's what I use this method for,
[00:02:48:149 - 00:02:52:169] **Speaker 1:** um, and it's a really big, uh, research area, big
[00:02:52:270 - 00:02:55:910] **Speaker 1:** field application for numerical methods and an opportunity for your
[00:02:55:910 - 00:02:58:149] **Speaker 1:** further study if you want to take the CFD course
[00:02:58:149 - 00:02:58:630] **Speaker 1:** next year.
[00:02:59:470 - 00:03:02:149] **Speaker 1:** And then I'm going to introduce the boundary element method
[00:03:02:149 - 00:03:03:869] **Speaker 1:** and then if I have any time left, which honestly
[00:03:03:869 - 00:03:06:789] **Speaker 1:** I probably won't, um, because I'm intending to do a
[00:03:06:789 - 00:03:10:029] **Speaker 1:** couple of derivations, which will probably take ages, um, then
[00:03:10:029 - 00:03:12:229] **Speaker 1:** I'll, I'll talk about what I actually use the boundary
[00:03:12:229 - 00:03:12:869] **Speaker 1:** element method for.
[00:03:12:949 - 00:03:16:589] **Speaker 1:** So, introduction to the boundary element method, a method for
[00:03:16:589 - 00:03:19:389] **Speaker 1:** solving PDEs numerically without having to mesh the domain.
[00:03:20:270 - 00:03:21:759] **Speaker 1:** Which might sound.
[00:03:22:889 - 00:03:25:070] **Speaker 1:** Like some kind of trick, but it sort of is,
[00:03:25:089 - 00:03:26:210] **Speaker 1:** and we'll talk about it.
[00:03:26:949 - 00:03:29:009] **Speaker 1:** Um, I thought I'd just give you a quick introduction
[00:03:29:669 - 00:03:30:369] **Speaker 1:** to me.
[00:03:30:910 - 00:03:33:130] **Speaker 1:** Um, I did my undergrad in Mech at UC.
[00:03:33:350 - 00:03:35:179] **Speaker 1:** Uh, I did this course in 2021.
[00:03:35:490 - 00:03:37:889] **Speaker 1:** I'm currently doing a PhD in the nech department under
[00:03:38:270 - 00:03:41:970] **Speaker 1:** Professor Matthew Cellier and CFD stuff using the BEM that
[00:03:41:970 - 00:03:42:729] **Speaker 1:** we'll talk about.
[00:03:42:889 - 00:03:45:149] **Speaker 1:** Um, this is a picture of me and my wife
[00:03:45:149 - 00:03:48:330] **Speaker 1:** at her, um, cousin's wedding recently.
[00:03:48:830 - 00:03:51:630] **Speaker 1:** Um, my wife, Izzy, she deserves a shout out because
[00:03:51:630 - 00:03:53:270] **Speaker 1:** I never would have made it as far through my
[00:03:53:270 - 00:03:55:729] **Speaker 1:** PhD as I have, um, without her support.
[00:03:56:309 - 00:03:58:429] **Speaker 1:** Uh, and I also thought I'd show you a photo,
[00:03:58:509 - 00:04:01:990] **Speaker 1:** a couple of photos of our rabbit Pinto, because she's
[00:04:01:990 - 00:04:02:630] **Speaker 1:** very cute.
[00:04:02:830 - 00:04:05:050] **Speaker 1:** Um, I thought everyone would appreciate that.
[00:04:05:550 - 00:04:08:830] **Speaker 1:** You're supposed to get rabbits in pairs, um, and we
[00:04:08:830 - 00:04:10:630] **Speaker 1:** did, we used to have a, a little white rabbit
[00:04:10:630 - 00:04:12:970] **Speaker 1:** called Buttercup, but unfortunately he passed away earlier this year,
[00:04:13:110 - 00:04:13:369] **Speaker 1:** so.
[00:04:14:169 - 00:04:17:088] **Speaker 1:** Um, that was hard, but Pinto's adapting well to being
[00:04:17:088 - 00:04:18:250] **Speaker 1:** a, a solo bunny.
[00:04:18:450 - 00:04:20:850] **Speaker 1:** So, anyway, onto the math.
[00:04:23:260 - 00:04:28:089] **Speaker 1:** OK, so Let's talk a little bit about PDEs.
[00:04:28:170 - 00:04:30:649] **Speaker 1:** So most physical processes are governed by, or at least
[00:04:30:649 - 00:04:32:570] **Speaker 1:** can be modelled as being governed by PDAs.
[00:04:33:350 - 00:04:37:869] **Speaker 1:** Um, and accordingly, good engineering design and analysis requires dealing
[00:04:37:869 - 00:04:40:149] **Speaker 1:** with the PDEs, by which I mean solving them or
[00:04:40:149 - 00:04:42:549] **Speaker 1:** approximating solutions to them, or things like this.
[00:04:42:700 - 00:04:45:790] **Speaker 1:** And so that's really what this course is for primarily.
[00:04:45:950 - 00:04:47:809] **Speaker 1:** So there's kind of two approaches that you can take
[00:04:47:989 - 00:04:48:869] **Speaker 1:** to solving a PDE.
[00:04:48:950 - 00:04:50:630] **Speaker 1:** You could solve it analytically or you could solve it
[00:04:50:630 - 00:04:51:309] **Speaker 1:** numerically.
[00:04:52:000 - 00:04:54:369] **Speaker 1:** And if you're going to solve it analytically, we teach
[00:04:54:369 - 00:04:57:089] **Speaker 1:** you separation of variables, and for that you need to
[00:04:57:089 - 00:04:58:250] **Speaker 1:** classify PDEs.
[00:04:59:850 - 00:05:03:769] **Speaker 1:** Because, uh, separation of variables gives you general solutions and
[00:05:03:769 - 00:05:06:529] **Speaker 1:** the general solutions are different for different types of PDEs.
[00:05:07:059 - 00:05:09:489] **Speaker 1:** So unless you can classify them, then you can't properly
[00:05:09:489 - 00:05:12:269] **Speaker 1:** apply the, the adequate general solution.
[00:05:12:609 - 00:05:14:130] **Speaker 1:** Um, and then once you have the general solution, then
[00:05:14:130 - 00:05:16:250] **Speaker 1:** obviously you can solve it just by substituting information from
[00:05:16:250 - 00:05:17:149] **Speaker 1:** boundary conditions.
[00:05:18:040 - 00:05:21:799] **Speaker 1:** Conversely, you might solve a PDE numerically because analytical solutions
[00:05:21:799 - 00:05:24:160] **Speaker 1:** are hard to come by and limited in scope.
[00:05:24:480 - 00:05:26:040] **Speaker 1:** So we teach you a little bit about how to
[00:05:26:040 - 00:05:28:239] **Speaker 1:** do that yourself so that you have a better understanding
[00:05:28:239 - 00:05:29:230] **Speaker 1:** of the process.
[00:05:29:679 - 00:05:31:429] **Speaker 1:** We teach you the finite difference method because it's easier
[00:05:31:429 - 00:05:33:519] **Speaker 1:** to understand, and we teach you the finite element method
[00:05:33:519 - 00:05:37:140] **Speaker 1:** because it's more powerful and kind of more generally applicable.
[00:05:37:809 - 00:05:42:649] **Speaker 1:** But really for flexibility and practicality reasons, you're probably going
[00:05:42:649 - 00:05:44:570] **Speaker 1:** to want to use commercial software if you ever have
[00:05:44:570 - 00:05:47:369] **Speaker 1:** to deal with PDEs in your actual job after your
[00:05:47:369 - 00:05:47:630] **Speaker 1:** degree.
[00:05:47:890 - 00:05:51:119] **Speaker 1:** And so for this, obviously we teach a console, um,
[00:05:51:369 - 00:05:55:049] **Speaker 1:** both to give you an introduction to the workflow for
[00:05:55:049 - 00:05:59:049] **Speaker 1:** a commercial CFD or sorry, a commercial um PDE solver,
[00:05:59:130 - 00:06:00:049] **Speaker 1:** numerical solver.
[00:06:00:480 - 00:06:02:519] **Speaker 1:** Um, and also to give you some idea of what
[00:06:02:519 - 00:06:05:119] **Speaker 1:** these programmes are capable of, there's also a nice link
[00:06:05:119 - 00:06:07:880] **Speaker 1:** because it's finite element method-based and, you know, we, we
[00:06:07:880 - 00:06:08:720] **Speaker 1:** teach you some of that.
[00:06:09:239 - 00:06:11:350] **Speaker 1:** Um, but there are other options outside of the course
[00:06:11:350 - 00:06:14:820] **Speaker 1:** context, which we'll talk about a little bit today, and,
[00:06:15:000 - 00:06:17:320] **Speaker 1:** um, we also teach you some optimisation, but I didn't
[00:06:17:320 - 00:06:18:839] **Speaker 1:** really know how to fit that into the tree, so.
[00:06:19:429 - 00:06:20:029] **Speaker 1:** It's just there.
[00:06:21:369 - 00:06:21:809] **Speaker 1:** OK.
[00:06:22:600 - 00:06:24:799] **Speaker 1:** The finite difference and finite element methods.
[00:06:25:769 - 00:06:27:890] **Speaker 1:** For a chocolate bar, can anyone give me the key
[00:06:27:890 - 00:06:28:970] **Speaker 1:** idea for the finite difference method?
[00:06:29:049 - 00:06:31:450] **Speaker 1:** You've got a PDE you wanna solve it, you're gonna
[00:06:31:450 - 00:06:34:489] **Speaker 1:** use the finite difference method, what is like the step,
[00:06:34:690 - 00:06:36:690] **Speaker 1:** the step one, the conceptual step one.
[00:06:40:269 - 00:06:41:980] **Speaker 1:** Yeah, but like more.
[00:06:44:079 - 00:06:45:160] **Speaker 1:** That's the same thing.
[00:06:52:220 - 00:06:53:040] **Speaker 1:** OK, points for trying.
[00:06:55:299 - 00:07:00:250] **Speaker 1:** Um, OK, so for the finite difference method, what we're
[00:07:00:250 - 00:07:03:850] **Speaker 1:** doing is we're approximating derivatives in the governing equation by
[00:07:03:850 - 00:07:06:329] **Speaker 1:** evaluating them as just being rise over run for a
[00:07:06:329 - 00:07:08:200] **Speaker 1:** small step in the direction of the derivative.
[00:07:08:850 - 00:07:12:410] **Speaker 1:** And when we do that, we use Taylor series approximations
[00:07:12:410 - 00:07:15:769] **Speaker 1:** of the grid points before and after, wherever we are
[00:07:15:769 - 00:07:19:100] **Speaker 1:** in the domain to construct various or more accurate representations
[00:07:19:100 - 00:07:20:929] **Speaker 1:** of that derivative based on the grid points around it.
[00:07:22:470 - 00:07:24:910] **Speaker 1:** Oh boy, I don't think we're gonna get any good
[00:07:24:910 - 00:07:25:609] **Speaker 1:** answers to this one.
[00:07:25:880 - 00:07:26:899] **Speaker 1:** For a chocolate bar.
[00:07:28:769 - 00:07:30:720] **Speaker 1:** Can anyone tell me the key idea of, of the
[00:07:30:720 - 00:07:31:739] **Speaker 1:** finite element method?
[00:07:32:829 - 00:07:33:570] **Speaker 1:** Not James.
[00:07:36:649 - 00:07:36:679] **Speaker 1:** Oats.
[00:07:39:309 - 00:07:44:910] **Speaker 1:** That's, yeah, that's, that's a relatively good yep, yep.
[00:07:45:510 - 00:07:47:549] **Speaker 1:** OK, you can both have chocolate bars, I'm probably gonna
[00:07:47:549 - 00:07:48:690] **Speaker 1:** miss, so.
[00:07:50:079 - 00:07:51:730] **Speaker 1:** Oh, that was not bad, OK.
[00:07:52:700 - 00:07:55:589] **Speaker 1:** Um, I don't really know much about the finite element
[00:07:55:589 - 00:07:57:200] **Speaker 1:** method, so take this with a grain of salt, but
[00:07:57:399 - 00:08:00:799] **Speaker 1:** basically we split the domain up into a bunch of
[00:08:00:799 - 00:08:03:839] **Speaker 1:** finite elements, right, and then the shape of the solution
[00:08:03:839 - 00:08:07:200] **Speaker 1:** to the PDE we approximate over each of those elements
[00:08:07:440 - 00:08:09:959] **Speaker 1:** using a polynomial function, a shape function because it takes
[00:08:09:959 - 00:08:12:519] **Speaker 1:** on the shape of the PDE, um, and then we
[00:08:12:519 - 00:08:16:279] **Speaker 1:** choose the, um, the coefficients for that PDE in order
[00:08:16:279 - 00:08:22:170] **Speaker 1:** to minimise error, uh, Between our approximation and the actual
[00:08:22:170 - 00:08:24:089] **Speaker 1:** answers when we integrate over the element.
[00:08:25:299 - 00:08:25:579] **Speaker 1:** Ish.
[00:08:26:500 - 00:08:29:040] **Speaker 1:** If you want more information about either of these, obviously
[00:08:29:040 - 00:08:30:660] **Speaker 1:** you're gonna want to rewatch James's lectures.
[00:08:31:519 - 00:08:31:959] **Speaker 1:** OK.
[00:08:33:000 - 00:08:35:520] **Speaker 1:** Moving on to computational fluid dynamics.
[00:08:35:559 - 00:08:38:080] **Speaker 1:** So like I said, um, a, a big area of
[00:08:38:080 - 00:08:42:840] **Speaker 1:** research, um, and application for numerical methods is understanding how
[00:08:42:840 - 00:08:43:530] **Speaker 1:** fluids behave.
[00:08:43:640 - 00:08:47:039] **Speaker 1:** So computational fluid dynamics is predicting fluid behaviour using numerical
[00:08:47:039 - 00:08:47:510] **Speaker 1:** methods.
[00:08:47:960 - 00:08:49:780] **Speaker 1:** Much easier question for a chocolate bar.
[00:08:50:520 - 00:08:51:320] **Speaker 1:** What is a fluid?
[00:08:56:739 - 00:09:01:270] **Speaker 1:** Yeah, can we, can we use engineering words?
[00:09:02:090 - 00:09:02:820] **Speaker 1:** Sorry, one more time.
[00:09:06:760 - 00:09:07:630] **Speaker 3:** Yeah.
[00:09:09:080 - 00:09:10:869] **Speaker 1:** OK, uh, you can have it.
[00:09:11:280 - 00:09:12:450] **Speaker 1:** Oh, that's way too much.
[00:09:12:609 - 00:09:14:780] **Speaker 1:** Well, you can get it later, sorry.
[00:09:15:049 - 00:09:17:929] **Speaker 1:** OK, um, a fluid is a material that deforms continuously
[00:09:17:929 - 00:09:18:809] **Speaker 1:** under a sheer stress.
[00:09:19:489 - 00:09:22:570] **Speaker 1:** Um, which, when you think about it, by that definition,
[00:09:22:679 - 00:09:24:530] **Speaker 1:** most things are fluids if, if you push them hard
[00:09:24:530 - 00:09:25:049] **Speaker 1:** enough, but.
[00:09:25:960 - 00:09:26:359] **Speaker 1:** Anyway.
[00:09:27:210 - 00:09:29:979] **Speaker 1:** OK, so why would you run CFD simulations?
[00:09:30:140 - 00:09:33:739] **Speaker 1:** Um, why would you approach fluid, predicting fluid behaviour numerically?
[00:09:34:099 - 00:09:35:280] **Speaker 1:** Um, fluids are important.
[00:09:35:950 - 00:09:36:780] **Speaker 1:** They're all around us.
[00:09:36:900 - 00:09:40:909] **Speaker 1:** Uh, everything that we, Every, everything that we do is
[00:09:40:909 - 00:09:43:590] **Speaker 1:** an interaction with a fluid and all of our engineered
[00:09:43:590 - 00:09:47:710] **Speaker 1:** components also have to interact with fluids or, or manage
[00:09:47:710 - 00:09:49:409] **Speaker 1:** fluid interaction in some way.
[00:09:49:510 - 00:09:53:429] **Speaker 1:** Um, and they're really difficult, um, to, to work out
[00:09:53:429 - 00:09:54:849] **Speaker 1:** what they're going to do, right?
[00:09:55:190 - 00:09:58:830] **Speaker 1:** Um, I'll show you the Navier Stokes equations on the
[00:09:58:830 - 00:10:00:989] **Speaker 1:** next slide as a bit of a refresher, but the,
[00:10:01:070 - 00:10:03:049] **Speaker 1:** the governing PDE is really complicated basically.
[00:10:04:760 - 00:10:06:679] **Speaker 1:** Is there like a seagull on the roof.
[00:10:09:400 - 00:10:10:809] **Speaker 1:** Anyway, OK.
[00:10:11:390 - 00:10:13:549] **Speaker 1:** So in terms of like, if you've got a, a
[00:10:13:549 - 00:10:15:909] **Speaker 1:** flow, a fluid dynamics problem, and you're like, OK, I
[00:10:15:909 - 00:10:18:059] **Speaker 1:** want to know what this is going to do, um,
[00:10:18:200 - 00:10:21:030] **Speaker 1:** we have one framework that kind of helps us work
[00:10:21:030 - 00:10:23:489] **Speaker 1:** out what's going to happen and it's non-dimensionalization.
[00:10:24:070 - 00:10:26:609] **Speaker 1:** Um, and then we have three kind of general approaches,
[00:10:26:669 - 00:10:30:909] **Speaker 1:** which are testing what will happen experimentally, applying some theory,
[00:10:31:030 - 00:10:34:190] **Speaker 1:** so doing some kind of analytical work, um, or using
[00:10:34:190 - 00:10:35:570] **Speaker 1:** numerical simulations.
[00:10:35:869 - 00:10:39:159] **Speaker 1:** Um, and for the sake of time, Uh, I'm just
[00:10:39:159 - 00:10:41:190] **Speaker 1:** not gonna talk about all the other ones, but they're
[00:10:41:190 - 00:10:44:760] **Speaker 1:** really important, um, and if you're interested in fluids, it's
[00:10:44:760 - 00:10:45:659] **Speaker 1:** good to understand.
[00:10:46:979 - 00:10:50:950] **Speaker 1:** OK, so why, you know, why are these fluids so
[00:10:50:950 - 00:10:51:590] **Speaker 1:** difficult, right?
[00:10:51:989 - 00:10:54:549] **Speaker 1:** Because they're mathematics, like the behaviour of fluids is very
[00:10:54:549 - 00:10:55:690] **Speaker 1:** mathematically challenging.
[00:10:56:070 - 00:10:59:989] **Speaker 1:** So to give you kind of the, the simplest general
[00:10:59:989 - 00:11:01:859] **Speaker 1:** case, the governing PDE.
[00:11:03:049 - 00:11:05:840] **Speaker 1:** For fluid flow where you as like the vectorial velocity,
[00:11:05:849 - 00:11:06:809] **Speaker 1:** right, is going to be.
[00:11:08:280 - 00:11:10:880] **Speaker 1:** Like this, and so obviously this is horrible because you
[00:11:10:880 - 00:11:14:359] **Speaker 1:** have this non-linear term here, um, you have lots of
[00:11:14:799 - 00:11:17:380] **Speaker 1:** different terms that are influencing the behaviour of you.
[00:11:18:080 - 00:11:20:960] **Speaker 1:** Um, for those of you who did fluids, like this
[00:11:20:960 - 00:11:24:000] **Speaker 1:** is your material derivative, and then this term and these
[00:11:24:000 - 00:11:26:559] **Speaker 1:** are, um, the, the forces that are acting on the
[00:11:26:559 - 00:11:29:260] **Speaker 1:** fluids, so it's divided by the mass.
[00:11:29:359 - 00:11:32:880] **Speaker 1:** So it's, um, it's like F equals MA but really
[00:11:32:880 - 00:11:33:570] **Speaker 1:** complicated.
[00:11:33:919 - 00:11:38:090] **Speaker 1:** And also, Additionally, the fluid behaviour needs to accord with
[00:11:38:090 - 00:11:40:559] **Speaker 1:** the continuity equation too, so not only is this really
[00:11:40:859 - 00:11:43:619] **Speaker 1:** complicated and nonlinear, but it's also coupled, so you need
[00:11:43:619 - 00:11:45:419] **Speaker 1:** to solve both of these at once, so.
[00:11:46:830 - 00:11:48:450] **Speaker 1:** And then this is like the easiest case, right?
[00:11:48:520 - 00:11:50:359] **Speaker 1:** Like it's, it can get a lot worse if, if
[00:11:50:359 - 00:11:53:039] **Speaker 1:** the food is like compressible or like can be affected
[00:11:53:039 - 00:11:54:700] **Speaker 1:** by magnetic fields or something like that.
[00:11:56:229 - 00:12:00:530] **Speaker 1:** So we take numerical approaches because the other approaches are
[00:12:00:869 - 00:12:04:549] **Speaker 1:** usually more expensive or or not viable or don't give
[00:12:04:549 - 00:12:05:909] **Speaker 1:** us the information that we want.
[00:12:06:349 - 00:12:08:510] **Speaker 1:** So almost any problem that can be mathematically modelled can
[00:12:08:510 - 00:12:12:750] **Speaker 1:** be solved numerically, provided you have infinite computer, which we
[00:12:12:750 - 00:12:13:270] **Speaker 1:** kind of do.
[00:12:13:979 - 00:12:18:010] **Speaker 1:** Um, Instead of solving the continuous equations, we discretize, so
[00:12:18:010 - 00:12:21:609] **Speaker 1:** we sample at discrete points, um, so that we can
[00:12:21:609 - 00:12:23:630] **Speaker 1:** make the equations approachable by a computer.
[00:12:24:000 - 00:12:26:289] **Speaker 1:** So computers can't solve PDEs, right, but they're really good
[00:12:26:289 - 00:12:27:169] **Speaker 1:** at linear algebra.
[00:12:27:289 - 00:12:30:049] **Speaker 1:** So we say, well, what if we take discrete samplings
[00:12:30:049 - 00:12:32:080] **Speaker 1:** of our PDEs, then we can form a system of
[00:12:32:080 - 00:12:34:400] **Speaker 1:** linear equations, then our computer can solve it.
[00:12:34:700 - 00:12:36:750] **Speaker 1:** And so pretty much all numerical methods follow that pattern.
[00:12:38:140 - 00:12:41:099] **Speaker 1:** Positives and numerical approaches, um, they're relatively quick to set
[00:12:41:099 - 00:12:43:460] **Speaker 1:** up, um, you might not be feeling that having just
[00:12:43:460 - 00:12:46:539] **Speaker 1:** done your assignment, but, um, you know, compared to like
[00:12:46:539 - 00:12:49:580] **Speaker 1:** an experiment, experiment can take months to get all, all
[00:12:49:580 - 00:12:52:059] **Speaker 1:** dialled in, so, um, they tend to be a lot
[00:12:52:059 - 00:12:52:619] **Speaker 1:** faster.
[00:12:52:849 - 00:12:56:039] **Speaker 1:** There's negligible cost per simulation unless you need supercomputer time.
[00:12:56:659 - 00:12:58:219] **Speaker 1:** You can have a high density of probe points.
[00:12:58:260 - 00:12:59:900] **Speaker 1:** I mean, you imagine if you're doing an experiment, you
[00:12:59:900 - 00:13:03:340] **Speaker 1:** want to do, um, sample surface pressure over some surface,
[00:13:03:419 - 00:13:03:539] **Speaker 1:** right?
[00:13:03:580 - 00:13:05:500] **Speaker 1:** You need, everywhere you want to sample the pressure, you've
[00:13:05:500 - 00:13:06:739] **Speaker 1:** got to drill a hole in the surface and put
[00:13:06:739 - 00:13:07:340] **Speaker 1:** a pressure tap.
[00:13:07:750 - 00:13:10:510] **Speaker 1:** So, and that might also interact with the flow, so
[00:13:10:510 - 00:13:12:469] **Speaker 1:** that kind of limits how many samples that you can
[00:13:12:469 - 00:13:13:150] **Speaker 1:** take of the pressure.
[00:13:13:900 - 00:13:16:469] **Speaker 1:** Um, you can see into places that experiments can't see,
[00:13:16:539 - 00:13:18:190] **Speaker 1:** you can look through walls, which is really hard to
[00:13:18:190 - 00:13:18:969] **Speaker 1:** do in the real world.
[00:13:19:770 - 00:13:22:840] **Speaker 1:** Um, and there's no physical limitations, so if you're trying
[00:13:22:840 - 00:13:24:159] **Speaker 1:** to work out what's going to happen to the space
[00:13:24:159 - 00:13:28:679] **Speaker 1:** shuttle on re-entry when it's going Mach 25, then, you
[00:13:28:679 - 00:13:30:239] **Speaker 1:** know, it's quite hard to build a wind tunnel that
[00:13:30:239 - 00:13:33:159] **Speaker 1:** fits the space shuttle and can simulate, you can, can
[00:13:33:159 - 00:13:34:669] **Speaker 1:** have a Mach 25 flow to go through it.
[00:13:34:799 - 00:13:37:359] **Speaker 1:** So, but that's fine, uh, obviously in the computer.
[00:13:38:219 - 00:13:40:140] **Speaker 1:** Um, there are a few drawbacks though.
[00:13:40:460 - 00:13:41:809] **Speaker 1:** Um, you need to know what you're doing.
[00:13:41:859 - 00:13:43:700] **Speaker 1:** You need to have access to software, maybe the licences
[00:13:43:700 - 00:13:44:479] **Speaker 1:** are expensive.
[00:13:44:940 - 00:13:47:179] **Speaker 1:** Um, the runtime can be really long, especially if you're
[00:13:47:179 - 00:13:49:159] **Speaker 1:** modelling complex turbulence conditions.
[00:13:49:460 - 00:13:52:179] **Speaker 1:** Um, you might think, oh, I had to sit and,
[00:13:52:780 - 00:13:54:140] **Speaker 1:** I had really small time steps and I had to
[00:13:54:140 - 00:13:55:580] **Speaker 1:** sit and wait for my patty to solve for 2
[00:13:55:580 - 00:13:58:950] **Speaker 1:** hours, but You know, if you have a complex turbulence
[00:13:58:950 - 00:14:01:140] **Speaker 1:** case and you're modelling it with like large duty simulation
[00:14:01:140 - 00:14:03:820] **Speaker 1:** or something like this, maybe it'll take a few months,
[00:14:04:159 - 00:14:06:669] **Speaker 1:** right, depending on how much computing power that you have
[00:14:06:669 - 00:14:07:289] **Speaker 1:** available to you.
[00:14:08:440 - 00:14:10:250] **Speaker 1:** And then at the end of that, the solution that
[00:14:10:250 - 00:14:13:280] **Speaker 1:** you get might not be like real if you set
[00:14:13:280 - 00:14:14:030] **Speaker 1:** it up wrong.
[00:14:14:320 - 00:14:16:359] **Speaker 1:** This is the kind of the biggest drawback is that
[00:14:16:359 - 00:14:18:119] **Speaker 1:** unless you know what you're doing and you're confident in
[00:14:18:119 - 00:14:20:400] **Speaker 1:** your simulation, you can't really be confident that the results
[00:14:20:400 - 00:14:22:739] **Speaker 1:** are not just like pretty pictures.
[00:14:24:510 - 00:14:25:900] **Speaker 1:** OK, so how do you do CFD?
[00:14:26:960 - 00:14:29:719] **Speaker 1:** Um, it's really basically from the user's point of view,
[00:14:29:909 - 00:14:32:640] **Speaker 1:** especially if you're using commercial software, pretty much the same
[00:14:32:640 - 00:14:35:000] **Speaker 1:** as the process that you went through to solve the
[00:14:35:000 - 00:14:36:280] **Speaker 1:** console parts of your assignment.
[00:14:37:390 - 00:14:40:599] **Speaker 1:** However, there are additional considerations and complicating factors compared to
[00:14:40:599 - 00:14:41:659] **Speaker 1:** simpler PDEs.
[00:14:41:989 - 00:14:44:299] **Speaker 1:** Uh, one of these that you probably don't have to
[00:14:44:299 - 00:14:48:359] **Speaker 1:** deal with if you're just using a commercial package is,
[00:14:48:640 - 00:14:50:710] **Speaker 1:** for example, the coupling between those equations, right?
[00:14:50:760 - 00:14:53:799] **Speaker 1:** The solver methods have to be more complicated because you
[00:14:53:799 - 00:14:55:919] **Speaker 1:** can't just, you're not just solving one PDE, you're solving.
[00:14:57:099 - 00:14:59:659] **Speaker 1:** Um, and because it's much more complicated, there's just like
[00:14:59:659 - 00:15:01:940] **Speaker 1:** lots more ways that you can get it wrong, which
[00:15:01:940 - 00:15:03:059] **Speaker 1:** is kind of unfortunate.
[00:15:03:890 - 00:15:08:049] **Speaker 1:** Um, so this is a plug, uh, take the CFD
[00:15:08:049 - 00:15:11:690] **Speaker 1:** course next year, um, if you're interested to, we'll help
[00:15:11:690 - 00:15:12:549] **Speaker 1:** you not mess it up.
[00:15:13:750 - 00:15:15:429] **Speaker 1:** So what are the, you know, how can you mess
[00:15:15:429 - 00:15:15:669] **Speaker 1:** it up?
[00:15:15:710 - 00:15:18:210] **Speaker 1:** Like what are the main pitfalls associated with CFD?
[00:15:19:479 - 00:15:21:510] **Speaker 1:** You've gotta have all your ducks in a row, like,
[00:15:21:679 - 00:15:25:159] **Speaker 1:** and even more so than, than your, um, for solving
[00:15:25:159 - 00:15:26:359] **Speaker 1:** some PDEs right so.
[00:15:27:140 - 00:15:30:090] **Speaker 1:** The geometry that you have in your simulation has got
[00:15:30:090 - 00:15:33:500] **Speaker 1:** to be representative of your geometry, otherwise, like the real
[00:15:33:500 - 00:15:35:479] **Speaker 1:** geometry, otherwise your solution's going to be rubbish.
[00:15:36:320 - 00:15:38:929] **Speaker 1:** The mesh has to be well resolved and capture the
[00:15:38:929 - 00:15:42:409] **Speaker 1:** dynamics in that domain well, otherwise the solution's going to
[00:15:42:409 - 00:15:42:989] **Speaker 1:** be rubbish.
[00:15:43:570 - 00:15:45:520] **Speaker 1:** You've got to have the right boundary conditions in the
[00:15:45:520 - 00:15:50:210] **Speaker 1:** right places, um, and they need to accord sensibly with
[00:15:50:210 - 00:15:52:789] **Speaker 1:** one another, otherwise your solution's going to be rubbish.
[00:15:53:330 - 00:15:55:640] **Speaker 1:** Um, you need to incorporate all of the physics that
[00:15:55:640 - 00:15:57:950] **Speaker 1:** actually exist in the problem and are relevant.
[00:15:58:289 - 00:16:00:919] **Speaker 1:** Um, and the big one for this is usually turbulence,
[00:16:00:929 - 00:16:03:130] **Speaker 1:** because those of you who took fluids will understand that.
[00:16:03:590 - 00:16:05:750] **Speaker 1:** If you model a flow that's actually turbulent as being
[00:16:05:750 - 00:16:09:070] **Speaker 1:** laminar, for example, like it's just not, what you get
[00:16:09:070 - 00:16:12:429] **Speaker 1:** is just not, it's not even related to what actually
[00:16:12:429 - 00:16:16:320] **Speaker 1:** happens, um, so then your solution would be rubbish.
[00:16:16:710 - 00:16:18:950] **Speaker 1:** Um, and then you're gonna want to use a solver
[00:16:18:950 - 00:16:22:030] **Speaker 1:** that is, um, has all of these qualities, and if
[00:16:22:030 - 00:16:24:789] **Speaker 1:** you wanna understand more about what these mean, uh, take
[00:16:24:789 - 00:16:25:830] **Speaker 1:** the CFD course next year.
[00:16:28:179 - 00:16:31:659] **Speaker 1:** So running a CFD simulation, I, I guess, just as
[00:16:31:659 - 00:16:33:179] **Speaker 1:** an aside, like part of the reason that I give
[00:16:33:179 - 00:16:35:820] **Speaker 1:** this presentation in this way is that I have a
[00:16:35:820 - 00:16:37:059] **Speaker 1:** lot of people come to me and they're like, so
[00:16:37:059 - 00:16:39:059] **Speaker 1:** I'm trying to CFD this thing, and I'm like, oh,
[00:16:39:539 - 00:16:43:260] **Speaker 1:** no, you know, um, I think it bears a bit
[00:16:43:260 - 00:16:46:159] **Speaker 1:** of, um, a bit of warning that it's kind of,
[00:16:46:960 - 00:16:49:200] **Speaker 1:** It's a process where you need to not only have
[00:16:49:200 - 00:16:52:539] **Speaker 1:** some understanding of what fluids do in general, but also
[00:16:53:080 - 00:16:56:119] **Speaker 1:** how, how to approach a, a numerical modelling problem.
[00:16:57:179 - 00:16:59:859] **Speaker 1:** Um, and, and you need to know the physics like
[00:16:59:859 - 00:17:01:260] **Speaker 1:** before you model the problem as well.
[00:17:01:340 - 00:17:04:300] **Speaker 1:** This is another classic where people will say, oh well,
[00:17:04:339 - 00:17:06:938] **Speaker 1:** we want to know like what something is doing in
[00:17:06:938 - 00:17:09:938] **Speaker 1:** greater detail, so I'm gonna make a computational model of
[00:17:09:938 - 00:17:11:660] **Speaker 1:** it, and that's fine if broadly you know what the
[00:17:11:660 - 00:17:14:599] **Speaker 1:** physics are that are involved, but if you don't, then
[00:17:14:819 - 00:17:17:099] **Speaker 1:** what model are you going to use, right?
[00:17:17:660 - 00:17:18:180] **Speaker 1:** You don't know.
[00:17:19:409 - 00:17:21:568] **Speaker 1:** Rule of thumb, if a fluids problem has more than
[00:17:21:568 - 00:17:24:928] **Speaker 1:** one significant complicating factor, it'll be at least one PhD
[00:17:24:928 - 00:17:25:359] **Speaker 1:** worth of work.
[00:17:25:409 - 00:17:30:369] **Speaker 1:** So this is like complex turbulence conditions, um, non-Newtonian rheology,
[00:17:30:848 - 00:17:36:678] **Speaker 1:** maybe super complicated boundary conditions or geometry, um.
[00:17:37:530 - 00:17:38:170] **Speaker 1:** Yeah, there are others.
[00:17:38:250 - 00:17:39:270] **Speaker 1:** James, can you think of anything?
[00:17:40:040 - 00:17:41:109] **Speaker 1:** No, not a spot.
[00:17:41:189 - 00:17:41:729] **Speaker 1:** OK.
[00:17:42:189 - 00:17:46:939] **Speaker 1:** Yeah, anyway, um, or, yeah, maybe, maybe coupled multi-physics is
[00:17:46:939 - 00:17:48:109] **Speaker 1:** another, another classic.
[00:17:49:010 - 00:17:53:099] **Speaker 1:** Um, And then lastly, the last point of warning is
[00:17:53:099 - 00:17:55:880] **Speaker 1:** that commercial CFD packages will always give you a pretty
[00:17:55:880 - 00:17:56:180] **Speaker 1:** solution.
[00:17:56:300 - 00:17:59:599] **Speaker 1:** We like to call them colourful flow diagrams, but, uh,
[00:17:59:739 - 00:18:02:060] **Speaker 1:** you have to determine whether the solution is valid, right?
[00:18:02:099 - 00:18:04:619] **Speaker 1:** Because you don't know whether that solution is actually what
[00:18:04:619 - 00:18:06:339] **Speaker 1:** happens, what will happen in the real world.
[00:18:08:089 - 00:18:11:339] **Speaker 1:** Some motivation for niche methods, methods that are not as
[00:18:11:339 - 00:18:14:500] **Speaker 1:** commonly used for general numerical modelling.
[00:18:15:910 - 00:18:18:829] **Speaker 1:** Finite element method and finite volume method, which we'll talk
[00:18:18:829 - 00:18:20:500] **Speaker 1:** about in CFD if you take the course.
[00:18:20:869 - 00:18:23:949] **Speaker 1:** Simulations are very versatile and have good fidelity and accuracy
[00:18:23:949 - 00:18:27:449] **Speaker 1:** for almost all flows and all other PDEs, right?
[00:18:28:250 - 00:18:29:869] **Speaker 1:** Um, but this doesn't mean that they're always the best
[00:18:29:869 - 00:18:33:290] **Speaker 1:** approach, and in fact, there are often lower fidelity approaches
[00:18:33:290 - 00:18:37:270] **Speaker 1:** to particular flows or PDE problems that give sufficient information
[00:18:37:270 - 00:18:40:430] **Speaker 1:** and accuracy and are also much less computationally expensive.
[00:18:40:709 - 00:18:43:719] **Speaker 1:** So, The boundary element method which we're about to discuss,
[00:18:44:040 - 00:18:46:560] **Speaker 1:** for example, is very limited in scope, but when you
[00:18:46:560 - 00:18:50:300] **Speaker 1:** can apply it, um, it's super efficient and fast.
[00:18:51:119 - 00:18:53:760] **Speaker 1:** So what are the advantages, the advantages of this boundary
[00:18:53:760 - 00:18:53:770] **Speaker 1:** method?
[00:18:55:270 - 00:18:57:270] **Speaker 1:** Um, like I said, it's super fast, which means it's
[00:18:57:270 - 00:18:59:310] **Speaker 1:** great for optimisation, right, because you can do lots of
[00:18:59:310 - 00:19:00:310] **Speaker 1:** PDE solutions.
[00:19:01:459 - 00:19:03:589] **Speaker 1:** Quickly discretization is much easier.
[00:19:03:670 - 00:19:06:839] **Speaker 1:** So again, from the name boundary element, we're only discretizing
[00:19:06:839 - 00:19:08:829] **Speaker 1:** the boundary, and that means that we're kind of one
[00:19:08:829 - 00:19:11:689] **Speaker 1:** dimension down, which means it's much easier to deal with
[00:19:11:689 - 00:19:12:709] **Speaker 1:** the, the discretization.
[00:19:13:099 - 00:19:15:030] **Speaker 1:** Um, you don't really need to know what that means
[00:19:15:030 - 00:19:17:449] **Speaker 1:** exactly, but it's basically like there are ways of porting
[00:19:17:670 - 00:19:21:739] **Speaker 1:** directly from CAD software into the simulation framework, um, but
[00:19:21:739 - 00:19:23:229] **Speaker 1:** I don't know how that works, so we're not going
[00:19:23:229 - 00:19:23:849] **Speaker 1:** to go into it.
[00:19:24:819 - 00:19:25:000] **Speaker 1:** Um.
[00:19:25:540 - 00:19:28:579] **Speaker 1:** You can analytically sample points in the domain once you've
[00:19:28:579 - 00:19:30:619] **Speaker 1:** solved the behaviour on the boundary, which means that there's
[00:19:30:619 - 00:19:32:939] **Speaker 1:** no degree of mesh refinement required in the domain, and
[00:19:32:939 - 00:19:34:859] **Speaker 1:** hence you don't need to mesh the domain at all.
[00:19:35:839 - 00:19:39:800] **Speaker 1:** And for certain flows, NLPDs, um.
[00:19:40:599 - 00:19:44:040] **Speaker 1:** There's sufficient accuracy, you get the same amount of information
[00:19:44:239 - 00:19:47:099] **Speaker 1:** that you would, depending on what you want, right, for,
[00:19:47:180 - 00:19:50:119] **Speaker 1:** as you would from a higher fidelity method, but we're
[00:19:50:119 - 00:19:54:989] **Speaker 1:** talking, Solving a flow field in like 5 milliseconds on.
[00:19:55:949 - 00:19:57:400] **Speaker 1:** One of the lab computers, so.
[00:19:59:170 - 00:19:59:859] **Speaker 1:** Way quicker.
[00:20:00:329 - 00:20:03:410] **Speaker 1:** Limitations only applicable to certain flows, so it's primarily useful
[00:20:03:410 - 00:20:06:189] **Speaker 1:** for solving elliptic PDEs, think the Laplace equation.
[00:20:07:989 - 00:20:11:069] **Speaker 1:** So it's best use is for potential or stokes flows.
[00:20:11:140 - 00:20:14:109] **Speaker 1:** These are flows that have Reynolds numbers of like 0
[00:20:14:109 - 00:20:16:410] **Speaker 1:** or infinity and, and nothing in the middle.
[00:20:16:869 - 00:20:19:209] **Speaker 1:** Um, don't think too hard about it.
[00:20:20:430 - 00:20:24:430] **Speaker 1:** Um, it's low fidelity, so the main reason it's low
[00:20:24:430 - 00:20:26:900] **Speaker 1:** fidelity is that because you have this limitation on the
[00:20:26:900 - 00:20:30:150] **Speaker 1:** governing PDE you can't always incorporate all the physics that
[00:20:30:150 - 00:20:31:949] **Speaker 1:** might actually be involved in the real world.
[00:20:32:839 - 00:20:36:119] **Speaker 1:** Um, and initially, because you're only measuring the boundary, you
[00:20:36:119 - 00:20:38:280] **Speaker 1:** only get solutions sampled on the boundary.
[00:20:38:359 - 00:20:40:489] **Speaker 1:** So you need to do additional computation if you want
[00:20:40:489 - 00:20:41:520] **Speaker 1:** to take domain samples.
[00:20:41:589 - 00:20:44:630] **Speaker 1:** But again, it's, it's very inexpensive, so it's not really
[00:20:44:630 - 00:20:44:959] **Speaker 1:** a biggie.
[00:20:45:979 - 00:20:46:849] **Speaker 1:** What's the process?
[00:20:48:569 - 00:20:52:890] **Speaker 1:** PEM is, I'm gonna frame it as a mathematical magic
[00:20:52:890 - 00:20:55:489] **Speaker 1:** trick plus a clever reframing.
[00:20:55:650 - 00:20:58:699] **Speaker 1:** So the mathematical magic trick is how we're going to
[00:20:58:699 - 00:21:01:000] **Speaker 1:** work out what the PDE is doing in the domain
[00:21:01:000 - 00:21:03:689] **Speaker 1:** just by looking at the behaviour on the boundary, and
[00:21:03:689 - 00:21:07:410] **Speaker 1:** then we'll do a clever reframing and use that information
[00:21:07:410 - 00:21:09:469] **Speaker 1:** to form a linear system that a computer can solve.
[00:21:10:569 - 00:21:11:010] **Speaker 1:** OK.
[00:21:12:160 - 00:21:13:800] **Speaker 1:** There are a few things that you need to understand
[00:21:13:800 - 00:21:16:000] **Speaker 1:** before we, oh, and by the way, if anyone's like,
[00:21:16:119 - 00:21:18:760] **Speaker 1:** I'm so lost, but I understand well enough to ask
[00:21:18:760 - 00:21:21:459] **Speaker 1:** the question, by all means, at any point, please ask
[00:21:21:459 - 00:21:21:800] **Speaker 1:** questions.
[00:21:22:359 - 00:21:24:920] **Speaker 1:** Um, there's a few things that you need to understand
[00:21:24:920 - 00:21:29:439] **Speaker 1:** before I start doing math, otherwise it's no, nothing's gonna
[00:21:29:439 - 00:21:29:920] **Speaker 1:** make sense.
[00:21:30:339 - 00:21:32:939] **Speaker 1:** So we're gonna talk about sources, dipoles, and greens functions,
[00:21:33:359 - 00:21:36:069] **Speaker 1:** which are essential for the formulation of the boundary island
[00:21:36:069 - 00:21:36:400] **Speaker 1:** method.
[00:21:36:869 - 00:21:39:069] **Speaker 1:** So you can think of a point source in the
[00:21:39:069 - 00:21:42:140] **Speaker 1:** context of the BEM as being like a Dirichlet or
[00:21:42:140 - 00:21:45:390] **Speaker 1:** direct boundary condition, but instead of being a boundary condition,
[00:21:45:430 - 00:21:46:790] **Speaker 1:** it's that condition at a point.
[00:21:47:660 - 00:21:53:099] **Speaker 1:** So you're going to directly specify the value of the
[00:21:53:099 - 00:21:56:579] **Speaker 1:** function that is in the PDE at a particular point
[00:21:56:579 - 00:21:57:260] **Speaker 1:** in your domain.
[00:21:57:540 - 00:22:00:300] **Speaker 1:** So you can think of, you have a temperature specified
[00:22:00:300 - 00:22:02:900] **Speaker 1:** at a point, a voltage specified at a point, a
[00:22:02:900 - 00:22:06:260] **Speaker 1:** specified species concentration if it's, if it's a concentration kind
[00:22:06:260 - 00:22:07:219] **Speaker 1:** of diffusion problem.
[00:22:08:199 - 00:22:10:719] **Speaker 1:** And a point dipole is the normal derivative of a
[00:22:10:719 - 00:22:13:239] **Speaker 1:** point source or a Neumann condition at a point, right?
[00:22:13:319 - 00:22:16:640] **Speaker 1:** And I'm sure you're thinking points don't have normals, so
[00:22:16:640 - 00:22:17:739] **Speaker 1:** that doesn't make any sense.
[00:22:17:839 - 00:22:19:880] **Speaker 1:** Um, and that's kind of true, but you can just
[00:22:19:880 - 00:22:22:000] **Speaker 1:** pick whatever direction that you want to take the derivative
[00:22:22:000 - 00:22:23:219] **Speaker 1:** in and call that the normal.
[00:22:24:349 - 00:22:26:439] **Speaker 1:** So you can think of a specified heat flux in
[00:22:26:439 - 00:22:30:189] **Speaker 1:** a direction at a point, or a specified concentration, concentration
[00:22:30:189 - 00:22:33:439] **Speaker 1:** gradient in a direction at a point, or perhaps a
[00:22:33:439 - 00:22:35:719] **Speaker 1:** specified flow velocity in a direction at a point.
[00:22:36:890 - 00:22:38:189] **Speaker 1:** And a greens function.
[00:22:39:290 - 00:22:42:869] **Speaker 1:** G of some location X and then some location of
[00:22:42:869 - 00:22:47:579] **Speaker 1:** the source X0 describes the behaviour that the PDE exhibits.
[00:22:47:689 - 00:22:51:410] **Speaker 1:** So Green's functions are specific to whatever PDE, um, you're
[00:22:51:410 - 00:22:51:900] **Speaker 1:** solving.
[00:22:52:209 - 00:22:54:900] **Speaker 1:** Exhibits at a point X, where this is a vectorial
[00:22:54:900 - 00:22:57:010] **Speaker 1:** quantity, right, like it could be a point in 3D
[00:22:57:010 - 00:23:00:369] **Speaker 1:** space, um, due to the influence of a point source
[00:23:00:369 - 00:23:01:089] **Speaker 1:** at X0.
[00:23:01:209 - 00:23:05:010] **Speaker 1:** So for an example, Imagine you have an infinite plate
[00:23:05:010 - 00:23:07:040] **Speaker 1:** at 0 Kelvin, and you want to know the temperature
[00:23:07:040 - 00:23:07:910] **Speaker 1:** that's induced at it.
[00:23:08:150 - 00:23:09:630] **Speaker 1:** If I pick some point in the plate and I
[00:23:09:630 - 00:23:12:109] **Speaker 1:** hold it at a given temperature, the greens function tells
[00:23:12:109 - 00:23:14:030] **Speaker 1:** me if I stand a certain distance away from that
[00:23:14:030 - 00:23:15:849] **Speaker 1:** point, what temperature do I expect to measure?
[00:23:16:300 - 00:23:20:709] **Speaker 1:** Where, The temperature returns to zero at infinity.
[00:23:21:729 - 00:23:22:170] **Speaker 1:** OK.
[00:23:23:930 - 00:23:26:810] **Speaker 1:** I had another slide I thought from an old presentation,
[00:23:26:849 - 00:23:28:459] **Speaker 1:** I thought this is a difficult concept, so I'll just
[00:23:28:459 - 00:23:29:109] **Speaker 1:** chuck it in.
[00:23:29:609 - 00:23:32:250] **Speaker 1:** Um, so the boundary element method makes use of these
[00:23:32:250 - 00:23:33:050] **Speaker 1:** Greens functions.
[00:23:33:170 - 00:23:35:890] **Speaker 1:** A Greens function for the Laplace equation satisfies that the
[00:23:35:890 - 00:23:39:250] **Speaker 1:** Laplacian of the Greens function plus the direct delta function
[00:23:39:250 - 00:23:40:229] **Speaker 1:** is equal to 0.
[00:23:41:000 - 00:23:42:640] **Speaker 1:** We'll talk about the direct delta function more in a
[00:23:42:640 - 00:23:43:219] **Speaker 1:** moment.
[00:23:43:719 - 00:23:45:380] **Speaker 1:** Um, it's very useful by construction.
[00:23:45:680 - 00:23:48:150] **Speaker 1:** So if a point source is again located at x0,
[00:23:48:239 - 00:23:50:199] **Speaker 1:** then the Greens function of X and X0 tells you
[00:23:50:199 - 00:23:53:099] **Speaker 1:** the potential induced by X at that point source.
[00:23:54:020 - 00:23:55:619] **Speaker 1:** Oh sorry, add X by that point source.
[00:23:55:880 - 00:23:58:260] **Speaker 1:** You can think of a point source for another analogy
[00:23:58:260 - 00:24:00:459] **Speaker 1:** is like water flowing out of a drain over the
[00:24:00:459 - 00:24:03:380] **Speaker 1:** bottom of a flat basin, um, in a, in a
[00:24:03:380 - 00:24:04:560] **Speaker 1:** 2D flow problem.
[00:24:05:099 - 00:24:07:459] **Speaker 1:** Um, and a point dipole is the directional derivative of
[00:24:07:459 - 00:24:09:979] **Speaker 1:** that source, so again, specify flow in a direction at
[00:24:09:979 - 00:24:10:380] **Speaker 1:** a point.
[00:24:11:939 - 00:24:13:400] **Speaker 1:** OK, let's talk about the magic trick.
[00:24:13:439 - 00:24:14:300] **Speaker 1:** Here's the domain.
[00:24:14:800 - 00:24:17:319] **Speaker 1:** Um, now we're gonna do a derivation, so.
[00:24:18:189 - 00:24:19:310] **Speaker 1:** Hope you're all engaged.
[00:24:20:160 - 00:24:22:520] **Speaker 1:** So imagine you've got a domain AC and it's bounded
[00:24:22:520 - 00:24:24:880] **Speaker 1:** by a closed curve C and you could sample some
[00:24:24:880 - 00:24:27:829] **Speaker 1:** points in that domain, um, and call them X0 or
[00:24:27:829 - 00:24:30:760] **Speaker 1:** X and then you could also um have an inward
[00:24:30:760 - 00:24:36:170] **Speaker 1:** facing normal vector X N X on the, On the
[00:24:36:170 - 00:24:37:369] **Speaker 1:** boundary, so.
[00:24:39:109 - 00:24:40:000] **Speaker 1:** We're gonna do.
[00:24:43:619 - 00:24:45:949] **Speaker 1:** Again, it's not accessible, so it's not like you really
[00:24:45:949 - 00:24:46:969] **Speaker 1:** have to follow along.
[00:24:50:290 - 00:24:54:489] **Speaker 1:** Oh I assumed Freeze was an autofocus, but.
[00:24:56:069 - 00:24:56:510] **Speaker 1:** Oh well.
[00:25:03:140 - 00:25:03:569] **Speaker 1:** OK.
[00:25:04:380 - 00:25:09:140] **Speaker 1:** So Consider two functions.
[00:25:13:089 - 00:25:13:849] **Speaker 1:** FNG.
[00:25:14:579 - 00:25:15:739] **Speaker 1:** Yeah, let's do little G.
[00:25:17:119 - 00:25:19:540] **Speaker 1:** Which alaplacian.
[00:25:23:520 - 00:25:26:199] **Speaker 1:** We're going to start with the Laplace equation and end
[00:25:26:199 - 00:25:27:800] **Speaker 1:** with the Laplace equation because it's.
[00:25:28:589 - 00:25:29:609] **Speaker 1:** The easiest option.
[00:25:31:180 - 00:25:34:180] **Speaker 1:** So the Laplacian of F is equal to 0.
[00:25:35:180 - 00:25:36:339] **Speaker 1:** The Laplacian of G.
[00:25:37:270 - 00:25:38:170] **Speaker 1:** is equal to 0.
[00:25:39:109 - 00:25:39:589] **Speaker 1:** OK.
[00:25:40:180 - 00:25:42:969] **Speaker 1:** So now, based on what I said before.
[00:25:44:930 - 00:25:46:310] **Speaker 1:** We know that a Greens function.
[00:25:48:550 - 00:25:49:810] **Speaker 1:** For the Laplace equation.
[00:25:52:010 - 00:25:55:770] **Speaker 1:** Satisfies that the Laplacian of G.
[00:25:58:890 - 00:26:00:390] **Speaker 1:** By the way, this is going to feel like.
[00:26:01:810 - 00:26:03:770] **Speaker 1:** It's all just being kind of pulled out of the
[00:26:03:770 - 00:26:05:189] **Speaker 1:** air and then at some point later.
[00:26:06:189 - 00:26:09:150] **Speaker 1:** Um, and you're like, bam, it all, it's all coming
[00:26:09:150 - 00:26:10:430] **Speaker 1:** together, so.
[00:26:11:479 - 00:26:13:380] **Speaker 1:** Just try not to fall asleep for the first part.
[00:26:15:489 - 00:26:15:930] **Speaker 1:** OK.
[00:26:17:219 - 00:26:22:219] **Speaker 1:** And actually, um, for the 2D Laplace equation.
[00:26:23:140 - 00:26:24:939] **Speaker 1:** We know the value of the Greens function.
[00:26:25:699 - 00:26:32:160] **Speaker 1:** It's not super crucial that Uh, well, how do I
[00:26:32:160 - 00:26:32:589] **Speaker 1:** put this?
[00:26:32:959 - 00:26:34:760] **Speaker 1:** We have to know what the value, like the actual
[00:26:34:760 - 00:26:38:560] **Speaker 1:** function that defines the Greens function is, um, otherwise we
[00:26:38:560 - 00:26:41:349] **Speaker 1:** can't apply the boundary element method, but in the derivation
[00:26:41:349 - 00:26:43:079] **Speaker 1:** of the boundary element method, the actual form of the
[00:26:43:079 - 00:26:44:540] **Speaker 1:** Greens function is not important at all.
[00:26:45:540 - 00:26:49:209] **Speaker 1:** OK, so we know the function, but we're probably just
[00:26:49:209 - 00:26:50:020] **Speaker 1:** gonna kind of leave it.
[00:26:51:030 - 00:26:52:150] **Speaker 1:** And come back to it later.
[00:26:52:979 - 00:26:54:369] **Speaker 1:** OK, and so this.
[00:26:56:180 - 00:27:00:890] **Speaker 1:** Where D is the direct delta function.
[00:27:08:310 - 00:27:12:829] **Speaker 1:** And the direct delta function has some very strange properties.
[00:27:12:869 - 00:27:18:369] **Speaker 1:** It's, Um 0 everywhere, except.
[00:27:20:040 - 00:27:20:829] **Speaker 1:** Headaches snort.
[00:27:23:630 - 00:27:29:650] **Speaker 1:** Um, Where it's unbounded.
[00:27:33:349 - 00:27:34:750] **Speaker 1:** Has the following properties.
[00:27:45:099 - 00:27:48:589] **Speaker 1:** So Because you're subtracting.
[00:27:49:810 - 00:27:51:089] **Speaker 1:** We say at 0.
[00:27:52:329 - 00:27:53:410] **Speaker 1:** It's equal to infinity.
[00:27:54:560 - 00:27:57:250] **Speaker 1:** By construction, I was gonna bring a textbook that has
[00:27:57:250 - 00:27:58:530] **Speaker 1:** a great figure for this but I forgot.
[00:27:58:849 - 00:28:03:400] **Speaker 1:** Anyway, OK, so by construction it has this um, this
[00:28:03:400 - 00:28:08:569] **Speaker 1:** interesting integral property where if you integrate, Over some domain,
[00:28:08:640 - 00:28:11:030] **Speaker 1:** AC that contains the direct delta function.
[00:28:11:770 - 00:28:14:280] **Speaker 1:** Oh, sorry, you integrate the direct delta function over that
[00:28:14:280 - 00:28:14:530] **Speaker 1:** domain.
[00:28:15:770 - 00:28:21:530] **Speaker 1:** Um, then you'll get one, provided that, Hicks snort.
[00:28:22:449 - 00:28:24:130] **Speaker 1:** Uh, is in the domain.
[00:28:24:569 - 00:28:27:400] **Speaker 1:** So what you can think is, we've got some function,
[00:28:27:569 - 00:28:30:410] **Speaker 1:** it's zero everywhere, at some location in the domain, it
[00:28:30:410 - 00:28:33:250] **Speaker 1:** has an infinite spike, but the infinitesimal width of that
[00:28:33:250 - 00:28:36:290] **Speaker 1:** spike and the infinite height of that spike by construction
[00:28:36:290 - 00:28:38:270] **Speaker 1:** perfectly cancel out so that if we take an integral
[00:28:38:270 - 00:28:39:089] **Speaker 1:** over it, we get 1.
[00:28:40:989 - 00:28:41:930] **Speaker 1:** Why would we do that?
[00:28:42:030 - 00:28:46:150] **Speaker 1:** Well, it has a very useful property that we'll make
[00:28:46:150 - 00:28:48:530] **Speaker 1:** use of in the rest of the derivation.
[00:28:49:750 - 00:28:51:530] **Speaker 1:** Where if you have some function.
[00:28:53:489 - 00:28:56:369] **Speaker 1:** And you, some function in the domain and you integrate
[00:28:56:369 - 00:28:59:130] **Speaker 1:** over the domain and you multiply the product of the
[00:28:59:130 - 00:29:02:050] **Speaker 1:** direct delta function and that function in the domain.
[00:29:03:520 - 00:29:06:010] **Speaker 1:** Than what you're going to get because this integral is
[00:29:06:010 - 00:29:06:449] **Speaker 1:** one.
[00:29:07:390 - 00:29:10:589] **Speaker 1:** Sort of, I'm not going to offer a proof, um,
[00:29:11:020 - 00:29:13:349] **Speaker 1:** you're going to get the, the value of the function
[00:29:13:349 - 00:29:15:170] **Speaker 1:** at the singular point.
[00:29:16:839 - 00:29:19:660] **Speaker 1:** Which, again, we're going to think of as our source.
[00:29:20:790 - 00:29:23:089] **Speaker 1:** Coming back to it, and again provided that.
[00:29:25:000 - 00:29:25:459] **Speaker 1:** Yes.
[00:29:27:469 - 00:29:30:520] **Speaker 0:** that 0 equals infinity.
[00:29:30:689 - 00:29:31:250] **Speaker 0:** Are you saying that?
[00:29:33:619 - 00:29:36:130] **Speaker 1:** Ah, yes, so, well.
[00:29:37:369 - 00:29:40:449] **Speaker 1:** So you've got some fixed point X0.
[00:29:44:380 - 00:29:46:130] **Speaker 1:** This is like one day, right, but.
[00:29:51:060 - 00:29:54:180] **Speaker 1:** You've got like some fixed point X0 and then because
[00:29:54:180 - 00:29:58:579] **Speaker 1:** you're subtracting it off, when this evaluates to zero, you'll
[00:29:58:579 - 00:29:59:500] **Speaker 1:** be at X0.
[00:30:00:439 - 00:30:02:500] **Speaker 1:** So, then you'll be at the singular point.
[00:30:03:160 - 00:30:05:359] **Speaker 1:** Um, and again, it, it just looks like this, right?
[00:30:05:420 - 00:30:07:079] **Speaker 1:** Where it's like an infinite spike.
[00:30:08:189 - 00:30:08:589] **Speaker 1:** OK.
[00:30:09:390 - 00:30:16:650] **Speaker 1:** So now, That we have kind of this um Establishing
[00:30:16:650 - 00:30:18:890] **Speaker 1:** stuff down, then we'll, we'll move on to talk about
[00:30:18:890 - 00:30:22:250] **Speaker 1:** how we use this for, um, actually kind of solving
[00:30:22:250 - 00:30:23:239] **Speaker 1:** the behaviour of a PDE.
[00:30:24:349 - 00:30:27:300] **Speaker 1:** So firstly, I'm gonna introduce.
[00:30:28:920 - 00:30:30:719] **Speaker 1:** Green 2nd identity.
[00:30:32:339 - 00:30:35:420] **Speaker 1:** Um, Green was a mathematician in the 1800s who did
[00:30:35:420 - 00:30:38:739] **Speaker 1:** a lot of work on electrostatics, but because electrostatics are
[00:30:38:739 - 00:30:40:579] **Speaker 1:** Laplacian, you can apply his work to a lot of
[00:30:40:579 - 00:30:41:380] **Speaker 1:** other things too.
[00:30:42:119 - 00:30:46:069] **Speaker 1:** Um Again, this is also gonna feel like it's coming
[00:30:46:069 - 00:30:50:540] **Speaker 1:** out of nowhere, but, um, we'll talk a little bit
[00:30:50:540 - 00:30:53:920] **Speaker 1:** about why you would want to use this construction.
[00:30:55:180 - 00:31:00:140] **Speaker 1:** Um, so again, F and G satisfy the Laplace equation,
[00:31:00:410 - 00:31:01:650] **Speaker 1:** so if you have two functions F and G that
[00:31:01:650 - 00:31:05:670] **Speaker 1:** satisfy the Laplace equation, G by the Laplacian of F
[00:31:05:670 - 00:31:08:079] **Speaker 1:** minus F by the Laplacian of G is equal to
[00:31:08:079 - 00:31:12:050] **Speaker 1:** the divergence of G by the gradient of F minus
[00:31:12:050 - 00:31:15:890] **Speaker 1:** F by the gradient of G, which you can verify
[00:31:15:890 - 00:31:16:949] **Speaker 1:** with the product rule.
[00:31:18:170 - 00:31:19:459] **Speaker 1:** Quite straightforwardly.
[00:31:20:260 - 00:31:23:260] **Speaker 1:** Now you're probably thinking, where did this come from?
[00:31:23:339 - 00:31:24:420] **Speaker 1:** And that's the wrong question.
[00:31:24:540 - 00:31:26:660] **Speaker 1:** The wrong, the right question is not where did this
[00:31:26:660 - 00:31:28:619] **Speaker 1:** come from, because you can easily verify that this is
[00:31:28:619 - 00:31:29:329] **Speaker 1:** true with the product or.
[00:31:29:369 - 00:31:32:520] **Speaker 1:** The right question is, what's the utility of this?
[00:31:32:819 - 00:31:34:380] **Speaker 1:** And that will become apparent shortly.
[00:31:35:280 - 00:31:41:829] **Speaker 1:** So Let's substitute our Greens function for G in the
[00:31:41:829 - 00:31:42:579] **Speaker 1:** above equation.
[00:31:44:369 - 00:31:47:250] **Speaker 1:** We'll get G by the Laplacian of F minus F
[00:31:47:250 - 00:31:52:050] **Speaker 1:** by the Laplacian of G is equal to the divergence
[00:31:52:050 - 00:31:54:229] **Speaker 1:** of G F.
[00:31:54:290 - 00:31:56:130] **Speaker 1:** uh, well, now I'm really.
[00:31:57:550 - 00:31:59:949] **Speaker 1:** Messing it up, but it's OK.
[00:32:00:430 - 00:32:03:229] **Speaker 1:** OK, and if is Laplacian.
[00:32:04:170 - 00:32:07:020] **Speaker 1:** So this is 0, and the Laplacian of G.
[00:32:09:380 - 00:32:11:180] **Speaker 1:** Is the negative of the direct delta function.
[00:32:18:780 - 00:32:21:260] **Speaker 1:** So we could rewrite this as this term goes to
[00:32:21:260 - 00:32:22:939] **Speaker 1:** 0, we can rewrite this as.
[00:32:23:699 - 00:32:27:760] **Speaker 1:** If I'll write the argument in too to make it
[00:32:27:760 - 00:32:28:150] **Speaker 1:** obvious.
[00:32:29:000 - 00:32:35:489] **Speaker 1:** Um, to the divergence of a can.
[00:32:37:050 - 00:32:40:069] **Speaker 1:** G F minus F G.
[00:32:41:030 - 00:32:43:050] **Speaker 1:** OK, here's where it all comes together.
[00:32:43:959 - 00:32:46:260] **Speaker 1:** What if we integrate this over a domain AC?
[00:32:47:239 - 00:32:50:119] **Speaker 1:** OK, we're gonna use our trick from earlier, so the
[00:32:50:119 - 00:32:54:400] **Speaker 1:** integral over AC of F of X delta.
[00:32:55:819 - 00:32:57:030] **Speaker 1:** X minus X.
[00:32:57:979 - 00:33:02:199] **Speaker 1:** 0 DA is equal to the integral over AC of
[00:33:02:780 - 00:33:06:140] **Speaker 1:** the divergence of the Greens function by the gradient of
[00:33:06:140 - 00:33:08:959] **Speaker 1:** F minus F by the gradient of the Greens function.
[00:33:09:920 - 00:33:10:849] **Speaker 1:** DA now.
[00:33:11:729 - 00:33:12:770] **Speaker 1:** We know what this is going to be, right?
[00:33:12:839 - 00:33:15:930] **Speaker 1:** We talked about it earlier, um, by construction, it's going
[00:33:15:930 - 00:33:18:609] **Speaker 1:** to be the value of F at the point x
[00:33:18:609 - 00:33:19:099] **Speaker 1:** 0.
[00:33:20:040 - 00:33:21:739] **Speaker 1:** Which we can kind of choose arbitrarily.
[00:33:22:319 - 00:33:26:619] **Speaker 1:** And then in order to evaluate this, For the purposes
[00:33:26:619 - 00:33:29:630] **Speaker 1:** of time, does everyone remember the divergence theorem?
[00:33:30:449 - 00:33:31:750] **Speaker 1:** If not, I'll explain it.
[00:33:32:290 - 00:33:32:770] **Speaker 1:** OK.
[00:33:33:609 - 00:33:35:390] **Speaker 1:** I'm, I'm taking that as a no.
[00:33:35:869 - 00:33:37:849] **Speaker 1:** OK, so if you've got some domain and you look
[00:33:37:849 - 00:33:39:130] **Speaker 1:** at the divergence at a point.
[00:33:43:619 - 00:33:47:369] **Speaker 1:** We can say that the integral over the over the
[00:33:47:369 - 00:33:50:619] **Speaker 1:** domain, um, where this is like a bounding curve, right?
[00:33:52:229 - 00:33:55:800] **Speaker 1:** So that the integral over that domain of the divergence
[00:33:55:800 - 00:33:59:699] **Speaker 1:** of some vectorial quantity is going to be equal to
[00:34:00:199 - 00:34:03:640] **Speaker 1:** the integral over the bounding curve of the dot product
[00:34:03:640 - 00:34:04:780] **Speaker 1:** of a unit normal vector.
[00:34:05:579 - 00:34:12:870] **Speaker 1:** Um With the bounding curve, because it's basically like, if
[00:34:12:870 - 00:34:14:790] **Speaker 1:** I want to know, like if you imagine shrinking this
[00:34:14:790 - 00:34:16:949] **Speaker 1:** curve to be infinitesimally small so that it wraps the
[00:34:16:949 - 00:34:20:870] **Speaker 1:** point, it's like, the vectorial flow out of that point
[00:34:20:870 - 00:34:23:469] **Speaker 1:** is equal to the, like the, the sum of it
[00:34:23:469 - 00:34:26:810] **Speaker 1:** is equal to the integral over the bounding curve of
[00:34:27:060 - 00:34:29:270] **Speaker 1:** the normal outflow across the curve.
[00:34:30:888 - 00:34:33:709] **Speaker 1:** OK, I'm gonna get another piece of paper.
[00:34:39:599 - 00:34:41:059] **Speaker 1:** OK, so.
[00:34:43:689 - 00:34:46:489] **Speaker 1:** Using that Where are we?
[00:34:48:449 - 00:34:51:770] **Speaker 1:** We can then say that F of X0 is going
[00:34:51:770 - 00:34:54:110] **Speaker 1:** to be equal to the integral over C.
[00:34:55:729 - 00:34:58:570] **Speaker 1:** Of G, my aunt thought, oh, Greta.
[00:35:00:439 - 00:35:06:659] **Speaker 1:** Minus if by, And dotrow you refer to.
[00:35:07:719 - 00:35:10:360] **Speaker 1:** Uh, domain diagram, if confused.
[00:35:11:250 - 00:35:11:689] **Speaker 1:** Hopefully.
[00:35:13:719 - 00:35:14:479] **Speaker 1:** The Olympics.
[00:35:15:139 - 00:35:15:580] **Speaker 1:** OK.
[00:35:16:540 - 00:35:18:350] **Speaker 1:** Um, and I could write this out with all the
[00:35:18:350 - 00:35:19:550] **Speaker 1:** arguments, but that's going to take a while.
[00:35:19:590 - 00:35:21:209] **Speaker 1:** I don't think it's going to help your understanding, so.
[00:35:22:629 - 00:35:23:500] **Speaker 1:** This is the trick.
[00:35:25:350 - 00:35:25:669] **Speaker 1:** Wait.
[00:35:27:919 - 00:35:28:989] **Speaker 1:** What is the trick.
[00:35:32:790 - 00:35:39:489] **Speaker 1:** OK, well, We have Gee.
[00:35:42:610 - 00:35:48:620] **Speaker 1:** And if Um, These are only evaluated.
[00:35:49:729 - 00:35:50:530] **Speaker 1:** On the boundary.
[00:35:57:350 - 00:36:03:300] **Speaker 1:** But We can choose the location of X0.
[00:36:11:070 - 00:36:14:270] **Speaker 1:** To be anywhere in the anywhere in the domain.
[00:36:20:580 - 00:36:21:139] **Speaker 1:** OK.
[00:36:21:899 - 00:36:26:459] **Speaker 1:** So this means that the only condition that we have
[00:36:26:459 - 00:36:29:219] **Speaker 1:** on F is that it's Laplacian, and then without knowing
[00:36:29:219 - 00:36:33:090] **Speaker 1:** the form of that function at all, Using this trick
[00:36:33:090 - 00:36:35:189] **Speaker 1:** up here, we can say, OK, if I know the
[00:36:35:189 - 00:36:37:649] **Speaker 1:** values of F and it's normal derivative on the boundary,
[00:36:37:699 - 00:36:40:629] **Speaker 1:** and also the greens function and it's normal derivative on
[00:36:40:629 - 00:36:43:270] **Speaker 1:** the boundary, which is just a function of geometry, because,
[00:36:46:929 - 00:36:49:159] **Speaker 1:** Because we have the Greens function, wherever it went.
[00:36:50:620 - 00:36:55:010] **Speaker 1:** Yeah So we can calculate that, then I can evaluate
[00:36:55:070 - 00:36:57:550] **Speaker 1:** the value of F anywhere in the domain, right, just
[00:36:57:550 - 00:36:59:449] **Speaker 1:** by choosing where I sample.
[00:37:00:560 - 00:37:01:679] **Speaker 1:** Uh, snort.
[00:37:02:560 - 00:37:04:840] **Speaker 1:** So, That is the magic trick.
[00:37:05:979 - 00:37:07:179] **Speaker 1:** Does anyone understand?
[00:37:09:310 - 00:37:09:830] **Speaker 1:** Somewhat.
[00:37:10:620 - 00:37:14:189] **Speaker 1:** is Just some function that satisfies the Laplace equation.
[00:37:14:389 - 00:37:15:830] **Speaker 1:** We want to know what values it takes on in
[00:37:15:830 - 00:37:18:790] **Speaker 1:** the domain, but we've come up with a way of
[00:37:18:790 - 00:37:22:550] **Speaker 1:** doing that without having to sample its values directly in
[00:37:22:550 - 00:37:24:580] **Speaker 1:** the domain, like with a grid or anything like that.
[00:37:25:219 - 00:37:27:570] **Speaker 1:** Right, we've got it on the boundary, then we can
[00:37:27:570 - 00:37:29:429] **Speaker 1:** directly calculate what's going to happen in the domain.
[00:37:33:959 - 00:37:37:600] **Speaker 1:** Uh, so, uh, is your question like, is Big G
[00:37:37:600 - 00:37:38:699] **Speaker 1:** truly Laplacian?
[00:37:41:790 - 00:37:45:389] **Speaker 1:** OK, little G is Laplacian, Big G is Laplacian.
[00:37:46:149 - 00:37:48:550] **Speaker 1:** Little G being Laplacian is the only stipulation on it
[00:37:49:550 - 00:37:51:469] **Speaker 1:** being allowed to be included in that formula.
[00:37:51:909 - 00:37:54:469] **Speaker 1:** So because big G is Laplacian, except at the singular
[00:37:54:469 - 00:37:56:229] **Speaker 1:** point, which we just ignore because it's really little.
[00:37:57:229 - 00:37:59:179] **Speaker 1:** Um, we're allowed to substitute that.
[00:38:00:560 - 00:38:03:989] **Speaker 0:** Is X not if this was a flow in a
[00:38:03:989 - 00:38:05:030] **Speaker 0:** boundary, are they like?
[00:38:05:729 - 00:38:09:870] **Speaker 0:** Points with a vector No, it's a source, so it's
[00:38:09:870 - 00:38:10:629] **Speaker 1:** like a fixed.
[00:38:11:080 - 00:38:13:350] **Speaker 1:** It's probably best not to think of this in terms
[00:38:13:350 - 00:38:15:120] **Speaker 1:** of flows yet, it's probably easier to think of it
[00:38:15:120 - 00:38:17:679] **Speaker 1:** in terms of temperatures, because when we do flows, we
[00:38:17:679 - 00:38:21:600] **Speaker 1:** don't use like the Laplacian quantity is not the flow,
[00:38:21:840 - 00:38:24:419] **Speaker 1:** it's the thing that the flow is the gradient of.
[00:38:25:870 - 00:38:28:389] **Speaker 1:** Which is a little bit confusing, and I don't think
[00:38:28:389 - 00:38:30:290] **Speaker 1:** we'll get time to talk about it unfortunately, but.
[00:38:31:020 - 00:38:31:889] **Speaker 1:** Yeah, so anyway.
[00:38:34:100 - 00:38:35:020] **Speaker 1:** Like that, right?
[00:38:36:989 - 00:38:37:429] **Speaker 1:** OK.
[00:38:38:179 - 00:38:40:000] **Speaker 1:** So what's the, the reframe?
[00:38:40:580 - 00:38:42:860] **Speaker 1:** The reframe is gonna be, we want to take this
[00:38:42:860 - 00:38:44:379] **Speaker 1:** into, into something that we can actually use as a
[00:38:44:379 - 00:38:47:570] **Speaker 1:** numerical method to solve the behaviour, uh, in the domain.
[00:38:47:629 - 00:38:49:080] **Speaker 1:** So we're gonna need discretization.
[00:38:49:620 - 00:38:52:340] **Speaker 1:** Um, so I now have elements on the boundary, boundary
[00:38:52:340 - 00:38:53:320] **Speaker 1:** elements if you will.
[00:38:53:780 - 00:38:56:219] **Speaker 1:** And at the centre of each of those elements, I've
[00:38:56:219 - 00:38:58:739] **Speaker 1:** defined a control point, and a control point is just
[00:38:58:739 - 00:39:00:860] **Speaker 1:** somewhere where I'm going to satisfy the boundary conditions, kind
[00:39:00:860 - 00:39:03:020] **Speaker 1:** of like you have degrees of freedom in your finite
[00:39:03:020 - 00:39:03:540] **Speaker 1:** element method.
[00:39:05:000 - 00:39:07:879] **Speaker 1:** OK, so first, this is gonna seem completely meaningless, but
[00:39:07:879 - 00:39:09:649] **Speaker 1:** we're going to switch the arguments to the Greens function,
[00:39:09:840 - 00:39:11:560] **Speaker 1:** which we can do because it's symmetric.
[00:39:11:879 - 00:39:15:919] **Speaker 1:** And it's important to do this because it reframes fundamentally
[00:39:15:919 - 00:39:17:760] **Speaker 1:** what we're doing before, kind of what we were saying
[00:39:17:760 - 00:39:20:159] **Speaker 1:** is I have a source in the domain.
[00:39:20:260 - 00:39:24:260] **Speaker 1:** And that induces a distribution of F, a normal derivative
[00:39:24:260 - 00:39:25:379] **Speaker 1:** of F on the boundary.
[00:39:25:659 - 00:39:27:780] **Speaker 1:** If I flip it around now, what I'm saying is
[00:39:27:780 - 00:39:30:979] **Speaker 1:** that I have a distribution of sources and dipoles on
[00:39:30:979 - 00:39:33:399] **Speaker 1:** the boundary, and that's going to introduce some, I'm sorry,
[00:39:33:459 - 00:39:35:560] **Speaker 1:** induce some behaviour at F, right?
[00:39:36:610 - 00:39:37:679] **Speaker 1:** Where you're at X not.
[00:39:39:600 - 00:39:42:919] **Speaker 1:** So this allows us to determine F of X0 at
[00:39:42:919 - 00:39:46:560] **Speaker 1:** F by setting F and the normal derivative of F
[00:39:46:679 - 00:39:47:830] **Speaker 1:** as boundary conditions.
[00:39:48:280 - 00:39:51:500] **Speaker 1:** But usually you don't want to do this, right, because
[00:39:51:919 - 00:39:54:760] **Speaker 1:** usually you have one of those things and you want
[00:39:54:760 - 00:39:56:129] **Speaker 1:** to work out the other one.
[00:39:56:239 - 00:40:00:080] **Speaker 1:** Otherwise you wouldn't be doing any simulations because you'd have
[00:40:00:080 - 00:40:01:159] **Speaker 1:** all the information already.
[00:40:02:080 - 00:40:06:520] **Speaker 1:** So, well, because, you know, implicitly, if you have both
[00:40:06:520 - 00:40:08:979] **Speaker 1:** of those boundary conditions within the framework that we're talking
[00:40:08:979 - 00:40:10:870] **Speaker 1:** about, you have all of the information to solve the
[00:40:10:870 - 00:40:13:199] **Speaker 1:** behaviour, so you don't really have to do any solutions.
[00:40:14:239 - 00:40:17:310] **Speaker 1:** OK, so secondly, our next trick is that instead of
[00:40:17:310 - 00:40:19:600] **Speaker 1:** X0 being somewhere in the domain, we're going to put
[00:40:19:600 - 00:40:22:060] **Speaker 1:** it on the control point of one of the elements.
[00:40:23:020 - 00:40:25:419] **Speaker 1:** And then we'll fulfil the boundary conditions at that control
[00:40:25:419 - 00:40:25:600] **Speaker 1:** point.
[00:40:26:800 - 00:40:29:040] **Speaker 1:** The 3rd, we're going to assume that that distribution on
[00:40:29:040 - 00:40:31:360] **Speaker 1:** the boundary of sources and dipoles is going to have
[00:40:31:360 - 00:40:34:159] **Speaker 1:** unit strength, because then we're going to be able to
[00:40:34:159 - 00:40:36:479] **Speaker 1:** form a nice system of equations for what their strengths
[00:40:36:479 - 00:40:36:979] **Speaker 1:** should be.
[00:40:38:199 - 00:40:40:610] **Speaker 1:** And then lastly we'll construct a linear system of equations
[00:40:40:610 - 00:40:43:409] **Speaker 1:** by realising the source and dipole strength at any control
[00:40:43:409 - 00:40:44:790] **Speaker 1:** point, let's say it's not.
[00:40:46:540 - 00:40:50:320] **Speaker 1:** Um, which must satisfy the boundary conditions, those values are
[00:40:50:320 - 00:40:53:719] **Speaker 1:** induced by the sum of the influence from each of
[00:40:53:719 - 00:40:55:000] **Speaker 1:** these points, right?
[00:40:55:179 - 00:40:58:260] **Speaker 1:** So it's like, I've got a distribution of sources and
[00:40:58:260 - 00:40:59:100] **Speaker 1:** dipoles on the boundary.
[00:40:59:199 - 00:41:01:360] **Speaker 1:** I assume that they have unit strength.
[00:41:01:739 - 00:41:03:419] **Speaker 1:** I then look at each of the points on the
[00:41:03:419 - 00:41:06:060] **Speaker 1:** boundary and I say, OK, based on the sum of
[00:41:06:060 - 00:41:09:580] **Speaker 1:** the influence from all of those other points, what kind
[00:41:09:580 - 00:41:11:790] **Speaker 1:** of influence is going to be induced here?
[00:41:12:340 - 00:41:16:129] **Speaker 1:** And then that gives me, uh, an expression for what
[00:41:16:129 - 00:41:18:290] **Speaker 1:** the strength of the dipole and source strengths at that
[00:41:18:290 - 00:41:18:929] **Speaker 1:** point are.
[00:41:19:179 - 00:41:20:830] **Speaker 1:** And I can do that for all of the points,
[00:41:20:889 - 00:41:22:300] **Speaker 1:** and I can use that to construct a system of
[00:41:22:300 - 00:41:23:600] **Speaker 1:** equations which I then invert.
[00:41:23:909 - 00:41:26:760] **Speaker 1:** And that tells me what the sources and dipole strengths
[00:41:26:760 - 00:41:28:790] **Speaker 1:** need to be around the boundary in order to satisfy
[00:41:28:790 - 00:41:30:000] **Speaker 1:** the boundary conditions everywhere.
[00:41:31:219 - 00:41:32:719] **Speaker 1:** OK, you're nodding.
[00:41:36:060 - 00:41:38:620] **Speaker 1:** Well, if you want, later, but you have all the
[00:41:38:620 - 00:41:40:979] **Speaker 1:** information on the boundary, and from the previous slide, you
[00:41:40:979 - 00:41:42:260] **Speaker 1:** know that if you have all the information on the
[00:41:42:260 - 00:41:44:209] **Speaker 1:** boundary, you can calculate the behaviour anywhere in the domain,
[00:41:44:260 - 00:41:44:800] **Speaker 1:** so yeah, sure.
[00:41:46:469 - 00:41:46:820] **Speaker 1:** Yeah.
[00:41:48:090 - 00:41:48:370] **Speaker 1:** Good.
[00:41:49:610 - 00:41:50:100] **Speaker 1:** OK.
[00:41:50:379 - 00:41:52:129] **Speaker 1:** Um, so I, you know, I considered, I was like,
[00:41:52:179 - 00:41:54:570] **Speaker 1:** ah, I could write, I could write some code, I
[00:41:54:570 - 00:41:55:199] **Speaker 1:** could show them.
[00:41:55:659 - 00:41:56:879] **Speaker 1:** And I was like, that'll take me 2 days.
[00:41:57:479 - 00:42:00:979] **Speaker 1:** So, um, fortunately, console has a BEM solver built into
[00:42:00:979 - 00:42:01:239] **Speaker 1:** it.
[00:42:01:870 - 00:42:05:989] **Speaker 1:** So I've repeated the assignment, the planar 2D problem from
[00:42:05:989 - 00:42:10:389] **Speaker 1:** the assignment, with one caveat, which is that because the
[00:42:10:389 - 00:42:12:989] **Speaker 1:** temperature distribution here has to be Laplacian to be solved
[00:42:12:989 - 00:42:16:100] **Speaker 1:** by the BEM, I, I can't have temperature dependent kappa.
[00:42:16:310 - 00:42:18:550] **Speaker 1:** So instead I ran an optimisation study to make it
[00:42:18:550 - 00:42:20:750] **Speaker 1:** so that at infinite time I get the same minimum
[00:42:20:750 - 00:42:22:870] **Speaker 1:** temperature in the domain as you would have in the
[00:42:22:870 - 00:42:23:530] **Speaker 1:** assignment.
[00:42:23:979 - 00:42:27:459] **Speaker 1:** Um, so I set the same boundary conditions, and this
[00:42:27:459 - 00:42:28:110] **Speaker 1:** is my mesh.
[00:42:29:090 - 00:42:30:929] **Speaker 1:** So you can see I've only meshed the boundary of
[00:42:30:929 - 00:42:33:219] **Speaker 1:** the domain and like I've done a pretty rubbish job,
[00:42:33:340 - 00:42:33:500] **Speaker 1:** right?
[00:42:33:540 - 00:42:35:969] **Speaker 1:** Like there's very, very few points here.
[00:42:36:560 - 00:42:39:969] **Speaker 1:** So I do the solution, it takes like instant, no
[00:42:39:969 - 00:42:41:139] **Speaker 1:** time, right?
[00:42:41:260 - 00:42:44:060] **Speaker 1:** And then afterwards, for a tiny little bit of extra
[00:42:44:060 - 00:42:46:659] **Speaker 1:** time, maybe like half a second, I sample a grid
[00:42:46:659 - 00:42:49:620] **Speaker 1:** of like 100 by 100 points within the domain, using
[00:42:49:620 - 00:42:52:060] **Speaker 1:** the information that I get on here and my, my
[00:42:52:060 - 00:42:55:879] **Speaker 1:** greenst identity relation, and I get ta da temperature distribution,
[00:42:56:040 - 00:42:56:780] **Speaker 1:** right, magic.
[00:42:57:229 - 00:43:00:229] **Speaker 1:** Never had to sample any points in the domain, recover
[00:43:00:229 - 00:43:01:949] **Speaker 1:** the whole temperature distribution in the domain.
[00:43:03:979 - 00:43:05:620] **Speaker 1:** I think it's very cool, this is why I wanted
[00:43:05:620 - 00:43:06:340] **Speaker 1:** to explain it.
[00:43:06:739 - 00:43:08:820] **Speaker 1:** um, hopefully some of you find that to be neat
[00:43:08:820 - 00:43:09:239] **Speaker 1:** as well.
[00:43:14:669 - 00:43:18:189] **Speaker 1:** Oh, so this is just because it's Laplacian, it's like,
[00:43:18:229 - 00:43:18:610] **Speaker 1:** wow.
[00:43:20:020 - 00:43:47:030] **Speaker 1:** In order for, To reduce to We need to say
[00:43:47:449 - 00:43:48:610] **Speaker 1:** that's 0.
[00:43:50:409 - 00:43:52:610] **Speaker 1:** And this is constant.
[00:43:54:020 - 00:43:56:850] **Speaker 1:** Because if those things are true, this side is 0,
[00:43:57:219 - 00:43:59:300] **Speaker 1:** these both come out of the front of the integral,
[00:43:59:419 - 00:44:02:500] **Speaker 1:** and then the second derivative with respect to X of
[00:44:02:500 - 00:44:04:979] **Speaker 1:** T plus the second derivative with respect to Z of
[00:44:04:979 - 00:44:07:610] **Speaker 1:** T and 2D X and Z is the Laplacian of
[00:44:07:610 - 00:44:07:739] **Speaker 1:** T.
[00:44:09:439 - 00:44:13:320] **Speaker 1:** So, like I said, It's not as powerful because I
[00:44:13:320 - 00:44:15:250] **Speaker 1:** have to make this approximation, otherwise I can't use the
[00:44:15:250 - 00:44:18:699] **Speaker 1:** method to solve it, because I don't have a Greens
[00:44:18:699 - 00:44:22:850] **Speaker 1:** function for that more complicated version of the 2D heat
[00:44:22:850 - 00:44:23:409] **Speaker 1:** equation.
[00:44:23:649 - 00:44:23:850] **Speaker 1:** Right?
[00:44:24:290 - 00:44:27:889] **Speaker 1:** There is, if you don't have, I, I did some
[00:44:27:889 - 00:44:28:389] **Speaker 1:** reading.
[00:44:28:889 - 00:44:32:810] **Speaker 1:** And if you don't care about the temperature dependent thermal
[00:44:32:810 - 00:44:37:169] **Speaker 1:** conductivity, there is a time dependent Greens function for the
[00:44:37:169 - 00:44:39:330] **Speaker 1:** for the 2D heat equation, so you could solve a
[00:44:39:330 - 00:44:40:489] **Speaker 1:** time dependent problem using this.
[00:44:40:850 - 00:44:44:929] **Speaker 1:** Maybe you could also do some kind of time-stepping behaviour
[00:44:44:929 - 00:44:47:169] **Speaker 1:** on the boundary, but I'm not sure how well that
[00:44:47:169 - 00:44:47:610] **Speaker 1:** would work.
[00:44:49:610 - 00:44:49:929] **Speaker 1:** Yeah.
[00:44:52:600 - 00:44:54:800] **Speaker 1:** Ah, how to think of the Laplacian.
[00:44:54:879 - 00:44:56:949] **Speaker 1:** I mean, so the Laplacian is just like the, the
[00:44:56:949 - 00:45:01:560] **Speaker 1:** classic example of the, um, oh, you, I see, you
[00:45:01:560 - 00:45:03:580] **Speaker 1:** just want to know like what the, sure, yeah.
[00:45:24:300 - 00:45:25:300] **Speaker 1:** That's what you wanted, right?
[00:45:25:659 - 00:45:25:820] **Speaker 1:** Yeah.
[00:45:27:530 - 00:45:27:770] **Speaker 1:** Cool.
[00:45:29:110 - 00:45:31:350] **Speaker 1:** I mean this is, so the, like the gradient of
[00:45:31:350 - 00:45:33:870] **Speaker 1:** this will be a vectorial quantity, and then so you
[00:45:33:870 - 00:45:35:989] **Speaker 1:** take the divergence of the gradient to get the Laplacian.
[00:45:38:850 - 00:45:40:679] **Speaker 1:** OK, we've got 5 minutes left, um.
[00:45:42:530 - 00:45:44:070] **Speaker 1:** I guess I'll give a 3 minute thesis talk.
[00:45:45:830 - 00:45:49:070] **Speaker 1:** Uh, so firstly, I said that I use the BEM
[00:45:49:070 - 00:45:50:649] **Speaker 1:** to do fluid flow problems.
[00:45:50:949 - 00:45:53:219] **Speaker 1:** You just saw the the Napier-Sokes equations and you're like,
[00:45:53:270 - 00:45:54:550] **Speaker 1:** that's not Laplacian.
[00:45:54:790 - 00:45:56:729] **Speaker 1:** Like, what are you talking about, right?
[00:45:57:110 - 00:45:59:870] **Speaker 1:** Um, so in order to make it Laplacian so that
[00:45:59:870 - 00:46:02:469] **Speaker 1:** I can do it, right, um, I'm gonna assume that
[00:46:02:469 - 00:46:07:310] **Speaker 1:** the flow is inviscid, irritational, um, so like the curl
[00:46:07:310 - 00:46:10:149] **Speaker 1:** of the flow at any point, like the, uh, Nabla
[00:46:10:149 - 00:46:12:290] **Speaker 1:** cross flow field is zero.
[00:46:12:770 - 00:46:15:739] **Speaker 1:** Um, and it's incompressible, so it has approximately an infinite
[00:46:15:739 - 00:46:17:909] **Speaker 1:** Reynolds number, but the Mach number is also very small.
[00:46:19:709 - 00:46:20:739] **Speaker 1:** Don't think about it too much.
[00:46:20:949 - 00:46:23:290] **Speaker 1:** It's, it's actually a reasonable model in some cases.
[00:46:23:629 - 00:46:26:949] **Speaker 1:** Um, consider the flow field, it's some math stuff that
[00:46:26:949 - 00:46:29:310] **Speaker 1:** you probably don't understand and don't really need to know,
[00:46:29:389 - 00:46:31:510] **Speaker 1:** but the point is that because of these things, the
[00:46:31:510 - 00:46:34:709] **Speaker 1:** flow field is conservative, so there's some potential function where
[00:46:34:709 - 00:46:37:929] **Speaker 1:** the gradient of that potential describes the flow field.
[00:46:38:689 - 00:46:41:050] **Speaker 1:** We call it the velocity potential for obvious reasons.
[00:46:42:820 - 00:46:45:739] **Speaker 1:** Since the field is solenoidal, which is because it's incompressible,
[00:46:45:800 - 00:46:48:260] **Speaker 1:** it satisfies the incompressible continuity equation.
[00:46:48:780 - 00:46:52:979] **Speaker 1:** Therefore, the divergence of U, the velocity field is the
[00:46:52:979 - 00:46:55:739] **Speaker 1:** Laplacian of Phi is 0.
[00:46:55:899 - 00:46:57:610] **Speaker 1:** Great, the flow is Laplacian, now we can use the
[00:46:57:610 - 00:46:57:780] **Speaker 1:** VM.
[00:47:00:010 - 00:47:05:959] **Speaker 1:** Yeah Um, yeah, so you can, you can do exactly
[00:47:05:959 - 00:47:07:959] **Speaker 1:** what we just did before, but like it's way worse
[00:47:07:959 - 00:47:09:459] **Speaker 1:** now because it's more complicated.
[00:47:09:879 - 00:47:12:040] **Speaker 1:** Um, but we're doing the same thing effectively where we
[00:47:12:040 - 00:47:14:419] **Speaker 1:** have a source distribution over a body surface.
[00:47:14:760 - 00:47:19:120] **Speaker 1:** Um, I'm interested in external flows, um, so there's a
[00:47:19:120 - 00:47:22:469] **Speaker 1:** like 20 more pages of math to get from not
[00:47:22:469 - 00:47:27:179] **Speaker 1:** external to external, um, and we introduce this additional corrections
[00:47:27:179 - 00:47:29:739] **Speaker 1:** that we can have circulation around the body while also,
[00:47:30:260 - 00:47:33:500] **Speaker 1:** Maintaining mathematically the fact that there is no circulation.
[00:47:34:260 - 00:47:34:899] **Speaker 1:** And some.
[00:47:36:620 - 00:47:38:739] **Speaker 1:** We're just going to ignore that because you don't need
[00:47:38:739 - 00:47:39:419] **Speaker 1:** to understand it.
[00:47:39:820 - 00:47:42:459] **Speaker 1:** Um, think about just these as being very much the
[00:47:42:459 - 00:47:44:340] **Speaker 1:** same as the kind of integrals that I showed you
[00:47:44:340 - 00:47:44:719] **Speaker 1:** before.
[00:47:45:030 - 00:47:48:780] **Speaker 1:** And I guess the factor of a half, just, just
[00:47:48:780 - 00:47:49:540] **Speaker 1:** ignore that too.
[00:47:49:979 - 00:47:52:620] **Speaker 1:** Um, so we can rearrange this equation to get all
[00:47:52:620 - 00:47:54:979] **Speaker 1:** of my velocity potentials on one side and my normal
[00:47:54:979 - 00:47:56:760] **Speaker 1:** derivatives on the other side.
[00:47:57:139 - 00:47:59:590] **Speaker 1:** Um, by assuming that I have a constant source or
[00:47:59:590 - 00:48:01:790] **Speaker 1:** dipole strength over each of my elements, I can then
[00:48:01:790 - 00:48:03:350] **Speaker 1:** bring those out of the front of my equations.
[00:48:03:669 - 00:48:07:750] **Speaker 1:** And then as, by evaluating this integral between any two
[00:48:07:750 - 00:48:10:270] **Speaker 1:** control points on the surface, I can form a system
[00:48:10:270 - 00:48:11:290] **Speaker 1:** of linear equations.
[00:48:11:709 - 00:48:13:389] **Speaker 1:** And if you have a system of linear equations, you
[00:48:13:389 - 00:48:14:110] **Speaker 1:** can solve it.
[00:48:14:649 - 00:48:17:310] **Speaker 1:** I can get the velocity potential, and I care about
[00:48:17:310 - 00:48:19:949] **Speaker 1:** that because the gradient of the velocity potential usually plus
[00:48:19:949 - 00:48:21:909] **Speaker 1:** some inflow is my flow field.
[00:48:22:699 - 00:48:24:899] **Speaker 1:** So I can do fluid flow simulations, very cool.
[00:48:26:929 - 00:48:30:949] **Speaker 1:** Um, Hm, OK, and now I'm just gonna give a
[00:48:30:949 - 00:48:32:540] **Speaker 1:** general explanation of the rest of the things I do
[00:48:32:540 - 00:48:34:310] **Speaker 1:** because I'm not gonna have time to really talk about
[00:48:34:310 - 00:48:34:699] **Speaker 1:** it properly.
[00:48:34:790 - 00:48:38:409] **Speaker 1:** So, um, do you know what cavitation is?
[00:48:39:560 - 00:48:40:159] **Speaker 1:** OK, yes.
[00:48:40:320 - 00:48:44:060] **Speaker 1:** So cavitation, if you have a flow in a liquid,
[00:48:44:469 - 00:48:46:239] **Speaker 1:** um, it's possible to get a pressure drop in that
[00:48:46:239 - 00:48:50:560] **Speaker 1:** flow that's sufficient to cause the local conditions to be
[00:48:50:560 - 00:48:52:439] **Speaker 1:** favourable for the fluid to vaporise.
[00:48:52:959 - 00:48:56:199] **Speaker 1:** Um, and when that happens, you get a vapor-filled cavity
[00:48:56:199 - 00:48:58:600] **Speaker 1:** forming, um, usually on a surface.
[00:48:58:679 - 00:49:01:500] **Speaker 1:** This happens in engineering applications because if you think of
[00:49:02:159 - 00:49:07:679] **Speaker 1:** the Bernoulli equation, Um, if the speed goes up, the
[00:49:07:679 - 00:49:10:000] **Speaker 1:** pressure goes down at constant height.
[00:49:10:449 - 00:49:15:600] **Speaker 1:** And so in the context that I care about, where
[00:49:15:600 - 00:49:18:000] **Speaker 1:** you have flows over hydrofoils, which are wings that work
[00:49:18:000 - 00:49:20:959] **Speaker 1:** underwater, I'm interested in looking at the flows over 2D
[00:49:20:959 - 00:49:22:239] **Speaker 1:** hydrofoil profiles.
[00:49:22:500 - 00:49:25:080] **Speaker 1:** The flow has to be accelerated over the two surfaces
[00:49:25:080 - 00:49:27:479] **Speaker 1:** of the hydrofoil in order to generate a pressure difference
[00:49:27:479 - 00:49:28:379] **Speaker 1:** to cause lift.
[00:49:29:139 - 00:49:32:659] **Speaker 1:** And that pressure differential is fixed by the angle of
[00:49:32:659 - 00:49:35:179] **Speaker 1:** attack and the geometry of the foil, so there, there
[00:49:35:179 - 00:49:38:060] **Speaker 1:** is some flow speed where the pressure drop is sufficient
[00:49:38:060 - 00:49:40:500] **Speaker 1:** that on the suction side of the foil, you'll get
[00:49:40:500 - 00:49:41:219] **Speaker 1:** cavitation.
[00:49:41:459 - 00:49:43:860] **Speaker 1:** And this we don't like because when the cavity collapses,
[00:49:43:899 - 00:49:47:540] **Speaker 1:** it can induce surface damage, and also because once the
[00:49:47:540 - 00:49:50:219] **Speaker 1:** cavity forms on the surface, it deforms the flow path
[00:49:50:219 - 00:49:52:060] **Speaker 1:** and therefore introduces a bunch of drag.
[00:49:52:820 - 00:49:54:699] **Speaker 1:** Right, the lift doesn't really change, but the lift to
[00:49:54:699 - 00:49:56:080] **Speaker 1:** drag ratio goes to rubbish.
[00:49:59:070 - 00:50:03:379] **Speaker 1:** So we'd like to prevent that, um, and in order
[00:50:03:379 - 00:50:05:840] **Speaker 1:** to change the way that a flow behaves, you can
[00:50:05:840 - 00:50:07:840] **Speaker 1:** do flow control, and there are two main types of
[00:50:07:840 - 00:50:08:320] **Speaker 1:** flow control.
[00:50:08:399 - 00:50:10:939] **Speaker 1:** You could change the geometry of the body that's interacting
[00:50:11:000 - 00:50:13:879] **Speaker 1:** with the flow, which is geometric flow control, for example,
[00:50:13:959 - 00:50:17:639] **Speaker 1:** streamlining, or you could have some some method of fluidic
[00:50:17:639 - 00:50:19:989] **Speaker 1:** flow control where you directly influence the behaviour of that
[00:50:19:989 - 00:50:20:360] **Speaker 1:** fluid.
[00:50:20:669 - 00:50:23:320] **Speaker 1:** There are many options, um, for this, but the one
[00:50:23:320 - 00:50:25:419] **Speaker 1:** that I'm interested in is well normal control.
[00:50:26:580 - 00:50:30:139] **Speaker 1:** All normal control is when you have transpiration through the
[00:50:30:139 - 00:50:33:020] **Speaker 1:** surface, so injection or suction of the ambient fluid through
[00:50:33:020 - 00:50:37:100] **Speaker 1:** the boundary where that injection or suction is always normal
[00:50:37:100 - 00:50:40:540] **Speaker 1:** for the boundary but can spread broadly over the boundary
[00:50:40:540 - 00:50:42:620] **Speaker 1:** and have arbitrary amplitude across its span.
[00:50:44:659 - 00:50:45:389] **Speaker 1:** Blah blah blah.
[00:50:46:500 - 00:50:48:590] **Speaker 1:** I'm interested in doing.
[00:50:49:409 - 00:50:51:689] **Speaker 1:** The flow control so that I can change the pressure
[00:50:51:689 - 00:50:53:649] **Speaker 1:** distribution on the hydrofoil surface so I can get rid
[00:50:53:649 - 00:50:54:290] **Speaker 1:** of cavitation.
[00:50:55:060 - 00:50:55:320] **Speaker 1:** Right.
[00:50:56:560 - 00:50:58:760] **Speaker 1:** So I do that and whatever.
[00:50:59:159 - 00:51:00:379] **Speaker 1:** And these are the results that I get.
[00:51:00:429 - 00:51:04:830] **Speaker 1:** So if you have this foil, this black profile underneath
[00:51:04:830 - 00:51:07:310] **Speaker 1:** here, then if it's at an angle of attack of
[00:51:07:310 - 00:51:11:050] **Speaker 1:** 10 degrees, you'll get this pressure coefficient distribution in black.
[00:51:11:629 - 00:51:13:709] **Speaker 1:** Now if I wanted to improve the lift of that,
[00:51:13:790 - 00:51:16:090] **Speaker 1:** I could use this grey profile.
[00:51:16:909 - 00:51:19:760] **Speaker 1:** Um, the grey profile has improved lift, but it maintains
[00:51:19:760 - 00:51:23:830] **Speaker 1:** the Moment coefficient about the aerodynamic centre so that once
[00:51:23:830 - 00:51:27:469] **Speaker 1:** you impose that profile, you won't immediately crash, which is
[00:51:27:469 - 00:51:27:709] **Speaker 1:** good.
[00:51:28:649 - 00:51:33:370] **Speaker 1:** Um, and then the red lines here are what I've
[00:51:33:370 - 00:51:36:010] **Speaker 1:** been able to calculate using the VEM for how much
[00:51:36:010 - 00:51:38:709] **Speaker 1:** more normal control I'd need to impose on the surface,
[00:51:39:409 - 00:51:41:729] **Speaker 1:** distributed over the surface in order to recover that pressure
[00:51:41:729 - 00:51:42:979] **Speaker 1:** distribution on that profile.
[00:51:43:330 - 00:51:47:750] **Speaker 1:** So this is a qualitative, Example of that distribution, and
[00:51:47:750 - 00:51:49:360] **Speaker 1:** this is a quantitative example.
[00:51:49:709 - 00:51:51:830] **Speaker 1:** And then this is the, the kind of more interesting
[00:51:51:830 - 00:51:54:790] **Speaker 1:** one where basically what you need to know here is
[00:51:54:790 - 00:51:57:870] **Speaker 1:** that you can non-dimensionalize cavitation so that on this plot,
[00:51:58:149 - 00:52:02:379] **Speaker 1:** if you never never get a pressure coefficient that's lower
[00:52:02:379 - 00:52:05:310] **Speaker 1:** than some particular value, then you won't get cavitation.
[00:52:05:750 - 00:52:07:830] **Speaker 1:** And so I've have a cavitation number of 2 here,
[00:52:07:870 - 00:52:09:350] **Speaker 1:** so I've capped this off at -2.
[00:52:10:199 - 00:52:13:040] **Speaker 1:** And you can see that more or less I'm able
[00:52:13:040 - 00:52:17:439] **Speaker 1:** to recover a pressure distribution where I don't, where cavitation
[00:52:17:439 - 00:52:20:500] **Speaker 1:** shouldn't be induced off oil surface using this method.
[00:52:21:510 - 00:52:22:209] **Speaker 1:** So there you have it.
[00:52:22:709 - 00:52:24:899] **Speaker 1:** Um, for like 7 chocolate bars, and I'm sorry I'm
[00:52:24:899 - 00:52:26:919] **Speaker 1:** over time, can anyone, um, tell me how the boundary
[00:52:26:919 - 00:52:27:649] **Speaker 1:** element method works?
[00:52:31:270 - 00:52:34:659] **Speaker 1:** James, no dang it.
[00:52:39:040 - 00:52:40:120] **Speaker 1:** OK, that's fine.
[00:52:40:239 - 00:52:42:469] **Speaker 1:** Um, there are extra chocolate bars, so I guess whoever
[00:52:42:469 - 00:52:43:719] **Speaker 1:** spent the most time in the next suite in the
[00:52:43:719 - 00:52:44:560] **Speaker 1:** last week can have them.
[00:52:44:959 - 00:52:46:270] **Speaker 1:** Um, thanks for listening.
[00:52:46:600 - 00:52:49:080] **Speaker 1:** Many thanks to Matthew for supervising this work and for
[00:52:49:080 - 00:52:51:100] **Speaker 1:** James, um, for giving me the time to speak.
[00:52:52:479 - 00:52:54:340] **Speaker 1:** Please enrol to vote by the 25th of October.
[00:52:54:520 - 00:52:55:580] **Speaker 1:** That's less than 2 weeks away.
[00:52:56:709 - 00:52:56:719] **Speaker 1:** OK.
[00:52:57:709 - 00:52:58:250] **Speaker 1:** Thank you.
[00:53:06:750 - 00:53:10:699] **Speaker 1:** Uh Thank you.
[00:53:21:919 - 00:53:22:320] **Speaker 0:** What's up?
[00:53:22:600 - 00:53:25:850] **Speaker 0:** Um, when you talk about fluid control, do you mean,
[00:53:26:159 - 00:53:28:679] **Speaker 3:** I may have missed what you mean, do you mean
[00:53:28:679 - 00:53:33:080] **Speaker 3:** like actually pushing fluid through like the pores in this
[00:53:33:080 - 00:53:33:580] **Speaker 1:** case, yeah.
[00:53:34:260 - 00:53:36:949] **Speaker 1:** Yeah, there, there are all kinds of ways that you
[00:53:36:949 - 00:53:40:189] **Speaker 1:** can do flow control, but generally what we mean is
[00:53:40:189 - 00:53:43:429] **Speaker 1:** like, I have some kind of component and it's interacting
[00:53:43:429 - 00:53:45:949] **Speaker 1:** with the flow, and I want that interaction to take
[00:53:45:949 - 00:53:47:290] **Speaker 1:** some particular form.
[00:53:47:870 - 00:53:49:280] **Speaker 1:** How do I impose that, right?
[00:53:49:550 - 00:53:51:909] **Speaker 1:** And if, if the form that you want that interaction
[00:53:51:909 - 00:53:53:419] **Speaker 1:** to take is I want there to be less drag
[00:53:53:419 - 00:53:55:820] **Speaker 1:** on my component, then you could streamline it, right?
[00:53:56:110 - 00:53:58:270] **Speaker 1:** But if you also wanted it to be, I don't
[00:53:58:270 - 00:54:01:790] **Speaker 1:** know, propelled or like take some certain pressure coefficient distribution.
[00:54:02:280 - 00:54:05:399] **Speaker 1:** Maybe you want to use some kind of like acoustic
[00:54:05:399 - 00:54:08:879] **Speaker 1:** oscillator to like induce some like wave, kind of like
[00:54:08:879 - 00:54:10:780] **Speaker 1:** behaviour over the surface or maybe you want to inject
[00:54:10:780 - 00:54:13:560] **Speaker 1:** or, or suck some air or some ambient fluid through
[00:54:13:560 - 00:54:14:120] **Speaker 1:** the surface.
[00:54:14:520 - 00:54:15:639] **Speaker 1:** There are lots of ways to do it.
[00:54:21:260 - 00:54:23:300] **Speaker 3:** Maybe I tried to think about it too much.
[00:54:23:610 - 00:54:26:939] **Speaker 3:** So was the idea to prevent cavitation by taking fluid
[00:54:26:939 - 00:54:31:139] **Speaker 3:** to bring the static pressure back up, does that end
[00:54:31:139 - 00:54:34:379] **Speaker 3:** up ruining the lift because you're it will make it
[00:54:34:379 - 00:54:39:129] **Speaker 1:** worse, but Not necessarily.
[00:54:40:199 - 00:54:42:050] **Speaker 1:** Uh, you know, it's possible that you can have a
[00:54:42:050 - 00:54:45:260] **Speaker 1:** lift to drag ratio, which is still better because the,
[00:54:45:449 - 00:54:48:370] **Speaker 1:** the drag becomes so large, um, when you get cavitation.
[00:54:48:449 - 00:54:49:850] **Speaker 1:** So it's possible that you can have a lift to
[00:54:49:850 - 00:54:53:340] **Speaker 1:** drag ratio, which is still better while still, you know,
[00:54:53:419 - 00:54:57:050] **Speaker 1:** even though the lift coefficient is lower, sure, like being
[00:54:57:050 - 00:54:58:750] **Speaker 1:** in a regime where you have sufficient lift.

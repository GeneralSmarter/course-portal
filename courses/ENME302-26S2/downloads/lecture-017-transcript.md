# ENME302-26S2 Lecture 17 native Echo transcript

Date: August 10, 2026 12:00pm-12:55pm
Transcript type: native Echo automated transcript.

[00:00:06:710 - 00:00:08:890] **Speaker 0:** Oh, uh, afternoon.
[00:00:08:930 - 00:00:10:350] **Speaker 1:** Is the mic working OK?
[00:00:11:329 - 00:00:12:529] **Speaker 1:** Maybe, yeah, sweet.
[00:00:16:469 - 00:00:16:940] **Speaker 1:** Chuck it there.
[00:00:17:379 - 00:00:19:420] **Speaker 1:** All right, um, so as I mentioned in the post
[00:00:19:420 - 00:00:22:700] **Speaker 1:** this morning, I'm delivering the remaining lectures for this class.
[00:00:22:959 - 00:00:24:340] **Speaker 1:** Hope I'm in the right, right place.
[00:00:24:579 - 00:00:28:219] **Speaker 1:** Um, so we're doing EME 302, and so far you've
[00:00:28:219 - 00:00:32:110] **Speaker 1:** looked at fun elements for particular cases like bars, um,
[00:00:32:240 - 00:00:35:099] **Speaker 1:** beams, trusses, those sorts of things, and you've got a
[00:00:35:099 - 00:00:36:860] **Speaker 1:** test on that coming up soon next week.
[00:00:38:020 - 00:00:43:090] **Speaker 1:** Um, and Yeah, so today it's more relaxed, maybe.
[00:00:43:270 - 00:00:47:200] **Speaker 1:** Uh, I'll just go through some slides and I've tucked.
[00:00:48:310 - 00:00:50:709] **Speaker 1:** These course readers outside my office if you want to
[00:00:50:709 - 00:00:51:830] **Speaker 1:** collect them whenever you want.
[00:00:52:229 - 00:00:53:750] **Speaker 1:** We'll start on this on Wednesday.
[00:00:53:990 - 00:00:55:360] **Speaker 1:** So we won't start today.
[00:00:55:990 - 00:00:58:560] **Speaker 1:** Uh, but essentially the fill in the blanks.
[00:00:58:750 - 00:01:01:049] **Speaker 1:** So some work for you to do as well.
[00:01:03:049 - 00:01:04:110] **Speaker 1:** Yeah, so I'll just get started.
[00:01:06:160 - 00:01:08:199] **Speaker 1:** So, a bit about me, you probably haven't seen me
[00:01:08:199 - 00:01:14:160] **Speaker 1:** yet, uh, so I've Do my uh education in Bachelor
[00:01:14:160 - 00:01:14:680] **Speaker 1:** of Engineering.
[00:01:14:800 - 00:01:16:550] **Speaker 1:** So I did mechanical engineering, same as you.
[00:01:16:860 - 00:01:18:919] **Speaker 1:** Well, some of you, or most of you, uh, some
[00:01:18:919 - 00:01:20:260] **Speaker 1:** of you are doing tronics.
[00:01:20:879 - 00:01:25:129] **Speaker 1:** So this at UC, then continued on with my PhD
[00:01:25:129 - 00:01:25:610] **Speaker 1:** at UC.
[00:01:26:370 - 00:01:27:930] **Speaker 1:** So I'm interested in fluid mechanics.
[00:01:28:050 - 00:01:30:690] **Speaker 1:** So I did a PhD on modelling evolving boundary problems
[00:01:30:690 - 00:01:31:830] **Speaker 1:** and fluid mechanics.
[00:01:32:250 - 00:01:34:730] **Speaker 1:** And then I did a postdoc, looking more inverse problems.
[00:01:34:809 - 00:01:36:169] **Speaker 1:** So that's more like optimisation.
[00:01:36:529 - 00:01:37:730] **Speaker 1:** And you might have touched a little bit on that
[00:01:37:730 - 00:01:40:089] **Speaker 1:** annual controls courses and maybe a little bit more next
[00:01:40:089 - 00:01:40:330] **Speaker 1:** year.
[00:01:41:739 - 00:01:44:419] **Speaker 1:** And then my current work is with a fellowship looking
[00:01:44:419 - 00:01:48:000] **Speaker 1:** at biomechanical properties of blood clots, so more biomed focus.
[00:01:48:819 - 00:01:50:970] **Speaker 1:** So within our department, we've got a couple of miners,
[00:01:51:050 - 00:01:53:129] **Speaker 1:** the biomed miner and the aerospace miner.
[00:01:53:300 - 00:01:55:000] **Speaker 1:** Some of you might be in those already.
[00:01:56:080 - 00:01:58:480] **Speaker 1:** Um, so my work sort of aligns with biomed.
[00:01:59:099 - 00:02:01:870] **Speaker 1:** Some of my research interests include CFD, so computational fluid
[00:02:01:870 - 00:02:02:230] **Speaker 1:** dynamics.
[00:02:02:279 - 00:02:03:830] **Speaker 1:** This is a course that you can take next year
[00:02:03:830 - 00:02:08:029] **Speaker 1:** as a fourth-year student and is open to all engineering
[00:02:08:029 - 00:02:08:470] **Speaker 1:** students, I think.
[00:02:08:550 - 00:02:10:869] **Speaker 1:** So you might need to have done the fluid mechanics
[00:02:10:869 - 00:02:14:210] **Speaker 1:** course, uh, but Mick should have done those already.
[00:02:15:830 - 00:02:17:270] **Speaker 1:** I'm interested in moving boundary problems.
[00:02:17:309 - 00:02:19:789] **Speaker 1:** So instead of having a static case, maybe you have
[00:02:19:789 - 00:02:20:850] **Speaker 1:** a moving interface.
[00:02:21:080 - 00:02:22:929] **Speaker 1:** I'll show some examples shortly.
[00:02:23:910 - 00:02:25:610] **Speaker 1:** And fluid solid couplings.
[00:02:26:490 - 00:02:30:610] **Speaker 1:** So again, those sort of fluid structure interaction problems, non-Newtonian
[00:02:30:610 - 00:02:31:089] **Speaker 1:** theology.
[00:02:31:309 - 00:02:35:339] **Speaker 1:** So if you're familiar with Newtonian fluids like water.
[00:02:36:360 - 00:02:37:339] **Speaker 1:** This is quite funny.
[00:02:38:080 - 00:02:40:440] **Speaker 1:** But if you have a non-Newtonian fluid that changes the
[00:02:40:440 - 00:02:44:479] **Speaker 1:** sheer rate, viscosity, then you can think of things like
[00:02:44:479 - 00:02:47:380] **Speaker 1:** toothpaste or quicksand.
[00:02:47:500 - 00:02:51:080] **Speaker 1:** So that the behaviour of those materials change depending on
[00:02:51:080 - 00:02:53:000] **Speaker 1:** how quickly you interact with that material.
[00:02:53:429 - 00:02:54:429] **Speaker 1:** So toothpaste is quite neat.
[00:02:54:440 - 00:02:59:490] **Speaker 1:** It doesn't Um, yeah, except the tube prior to to
[00:02:59:490 - 00:03:01:779] **Speaker 1:** squeezing it and then when it's on the toothbrush, it
[00:03:01:779 - 00:03:02:199] **Speaker 1:** stays static.
[00:03:02:300 - 00:03:05:059] **Speaker 1:** So it's quite a neat visco plastic fluid as an
[00:03:05:059 - 00:03:07:990] **Speaker 1:** example and inverse problems I talked about earlier.
[00:03:08:539 - 00:03:10:070] **Speaker 1:** So some of some of the applications that I look
[00:03:10:070 - 00:03:14:570] **Speaker 1:** at is climate change, the melting icebergs, silica scale deposition.
[00:03:14:630 - 00:03:16:619] **Speaker 1:** So that's more geothermal related.
[00:03:16:860 - 00:03:18:580] **Speaker 1:** We've got a few geothermal power plants up in the
[00:03:18:580 - 00:03:19:199] **Speaker 1:** North Island.
[00:03:19:779 - 00:03:21:899] **Speaker 1:** So the top of volcanic region, some of you might
[00:03:21:899 - 00:03:24:020] **Speaker 1:** have visited some of those power plants up there or
[00:03:24:020 - 00:03:24:559] **Speaker 1:** nearby.
[00:03:25:089 - 00:03:27:169] **Speaker 1:** Uh, so that's a good way of having sort of
[00:03:27:169 - 00:03:30:919] **Speaker 1:** renewable energy for, for our, um, grid.
[00:03:32:289 - 00:03:33:160] **Speaker 1:** Lava flows.
[00:03:33:610 - 00:03:36:369] **Speaker 1:** So we've got a few volcanoes in New Zealand.
[00:03:37:179 - 00:03:40:050] **Speaker 1:** Uh, none of them are actively spewing lava at the
[00:03:40:050 - 00:03:42:929] **Speaker 1:** moment, but they may in the future.
[00:03:43:369 - 00:03:45:270] **Speaker 1:** So looking at those sort of hazards.
[00:03:46:389 - 00:03:48:570] **Speaker 1:** Biofluids, biomedical engineering, I touched on.
[00:03:50:119 - 00:03:52:759] **Speaker 1:** So this meaning of the course is looking at modelling
[00:03:52:759 - 00:03:55:020] **Speaker 1:** techniques and numerical simulations and sort of a little bit
[00:03:55:020 - 00:03:56:320] **Speaker 1:** of maths, but not too much.
[00:03:56:720 - 00:03:58:759] **Speaker 1:** So I wanted to give some examples of what we
[00:03:58:759 - 00:04:00:460] **Speaker 1:** could apply these models to.
[00:04:01:000 - 00:04:03:570] **Speaker 1:** So here's an example I did do my PhD.
[00:04:03:679 - 00:04:06:360] **Speaker 1:** I looked at the erosion of a clay cylinder and
[00:04:06:360 - 00:04:07:020] **Speaker 1:** crossflow.
[00:04:07:360 - 00:04:09:119] **Speaker 1:** So if we think back to fluid mechanics, if we
[00:04:09:119 - 00:04:13:470] **Speaker 1:** have A clay cylinder that we're looking in on.
[00:04:13:889 - 00:04:16:070] **Speaker 1:** We've got fluid from the left to the right.
[00:04:16:450 - 00:04:18:670] **Speaker 1:** And we got this laminar shear separation.
[00:04:19:010 - 00:04:21:989] **Speaker 1:** And we've got these water seas forming downstream of the
[00:04:21:989 - 00:04:22:809] **Speaker 1:** clay cylinder.
[00:04:23:250 - 00:04:25:200] **Speaker 1:** So this Reynolds number is at 30,000.
[00:04:25:450 - 00:04:28:209] **Speaker 1:** So if we had a really slow flow, then we
[00:04:28:209 - 00:04:31:950] **Speaker 1:** would expect the flow to remain attached around the cylinder.
[00:04:32:609 - 00:04:34:570] **Speaker 1:** So that's just an example of why we care about
[00:04:34:570 - 00:04:35:170] **Speaker 1:** Reynolds numbers.
[00:04:35:250 - 00:04:39:450] **Speaker 1:** We calculate them to predict or analyse the flow field.
[00:04:40:660 - 00:04:44:140] **Speaker 1:** So in this case, the clay cylinder was eroding due
[00:04:44:140 - 00:04:46:420] **Speaker 1:** to that wall shear stress, and we can see that
[00:04:46:420 - 00:04:50:100] **Speaker 1:** the shape changes and panel B towards a more triangular
[00:04:50:100 - 00:04:50:339] **Speaker 1:** form.
[00:04:50:700 - 00:04:53:820] **Speaker 1:** So instead of saying circular and eroding uniformly, it started
[00:04:53:820 - 00:04:56:200] **Speaker 1:** to produce this uh different shape.
[00:04:56:779 - 00:04:59:440] **Speaker 1:** So they observed this in some experiments in 2012.
[00:05:00:559 - 00:05:03:299] **Speaker 1:** And I looked at modelling this, uh, with CFT.
[00:05:04:679 - 00:05:06:880] **Speaker 1:** So here's just a couple of schematics on the right.
[00:05:07:079 - 00:05:07:720] **Speaker 1:** So C and D.
[00:05:07:799 - 00:05:11:410] **Speaker 1:** C is the initial condition of the clay cylinder and
[00:05:11:410 - 00:05:14:200] **Speaker 1:** D is towards the final form.
[00:05:15:040 - 00:05:19:679] **Speaker 1:** We have a more uniform was stress distribution that emerges
[00:05:19:679 - 00:05:20:799] **Speaker 1:** on this, this panel.
[00:05:23:940 - 00:05:26:619] **Speaker 1:** So some equations, uh, if you've done fluid mechanics, these
[00:05:26:619 - 00:05:29:299] **Speaker 1:** will be familiar to you, uh, but they're just, uh,
[00:05:29:589 - 00:05:33:339] **Speaker 1:** the Navier-S Stokes equations that we use for analysing the
[00:05:33:339 - 00:05:33:940] **Speaker 1:** fluid flow.
[00:05:34:660 - 00:05:37:000] **Speaker 1:** And we've got the continuity equation.
[00:05:37:609 - 00:05:40:049] **Speaker 1:** And I've introduced here a velocity of the interface.
[00:05:40:100 - 00:05:44:119] **Speaker 1:** So the end is the velocity of the interface around
[00:05:44:119 - 00:05:45:880] **Speaker 1:** the clay cylinder surface.
[00:05:46:459 - 00:05:50:730] **Speaker 1:** So this is essentially coupled between the fluid and the
[00:05:50:730 - 00:05:51:179] **Speaker 1:** solid.
[00:05:51:410 - 00:05:52:910] **Speaker 1:** So that's that fluids solid coupling.
[00:05:53:570 - 00:06:01:089] **Speaker 1:** And over time, I've drawn multiple outlines going to lighter
[00:06:01:089 - 00:06:02:589] **Speaker 1:** and lighter shades over time.
[00:06:03:179 - 00:06:04:670] **Speaker 1:** So that's what we have here.
[00:06:05:010 - 00:06:08:130] **Speaker 1:** And I'm just showing this was just produced for the
[00:06:08:130 - 00:06:10:929] **Speaker 1:** logo thing, but essentially this is the turbulent structure downstream.
[00:06:11:049 - 00:06:15:380] **Speaker 1:** So if you if you're modelling Uh, with larger simulations,
[00:06:16:049 - 00:06:18:640] **Speaker 1:** a particular turbance model, you can capture these vortex wakes.
[00:06:18:980 - 00:06:21:100] **Speaker 1:** So you'll learn about that in your CFT course if
[00:06:21:100 - 00:06:21:500] **Speaker 1:** you want.
[00:06:22:500 - 00:06:23:980] **Speaker 1:** Um, but essentially, these are three dimensional.
[00:06:24:059 - 00:06:27:140] **Speaker 1:** So the clay cylinder was only a two-dimensional geometry, but
[00:06:27:140 - 00:06:30:220] **Speaker 1:** we're observing three-dimensional fluid behaviour downstream.
[00:06:30:950 - 00:06:33:459] **Speaker 1:** Based on the Renal's number, so, yeah.
[00:06:35:390 - 00:06:38:190] **Speaker 1:** Another case that I looked at was a sphere, so
[00:06:38:190 - 00:06:39:510] **Speaker 1:** nice axis symmetrical.
[00:06:40:579 - 00:06:42:420] **Speaker 1:** Again, this, I don't know what Real number this one
[00:06:42:420 - 00:06:42:920] **Speaker 1:** was on.
[00:06:44:089 - 00:06:47:579] **Speaker 1:** But we're seeing two vortices formed downstream.
[00:06:48:010 - 00:06:49:799] **Speaker 1:** So we still have laminar shear separation.
[00:06:50:010 - 00:06:51:250] **Speaker 1:** And we've got these vortex forming downstream.
[00:06:53:529 - 00:06:55:899] **Speaker 1:** So again, they observed something that had a melting rate
[00:06:55:899 - 00:06:57:160] **Speaker 1:** that wasn't uniform.
[00:06:57:290 - 00:06:58:829] **Speaker 1:** It wasn't spherical over time.
[00:06:59:250 - 00:07:00:589] **Speaker 1:** So that's what I looked at modelling.
[00:07:01:609 - 00:07:03:989] **Speaker 1:** We've got some more equations to solve.
[00:07:04:679 - 00:07:07:720] **Speaker 1:** So now we've got temperature because the ice is melting
[00:07:07:720 - 00:07:10:670] **Speaker 1:** as a function of temperature gradient at the interface.
[00:07:11:790 - 00:07:14:959] **Speaker 1:** So we need to solve for temperature and that interface
[00:07:14:959 - 00:07:18:079] **Speaker 1:** velocity is related to the temperature gradient DT by DM.
[00:07:18:359 - 00:07:22:269] **Speaker 1:** So DN is just the normal component at the surface.
[00:07:22:359 - 00:07:27:019] **Speaker 1:** So it's moving uh per perpendicular to the surface.
[00:07:28:079 - 00:07:31:730] **Speaker 1:** And we've got some scaling, uh, terms with thermal connectivity,
[00:07:31:989 - 00:07:34:049] **Speaker 1:** uh, and density and heat capacity.
[00:07:35:399 - 00:07:37:100] **Speaker 1:** So this is the shape that it forms.
[00:07:37:480 - 00:07:40:359] **Speaker 1:** We can see that it's reasonably spherical upstream.
[00:07:40:600 - 00:07:42:290] **Speaker 1:** So again, flows from left to right.
[00:07:42:519 - 00:07:45:019] **Speaker 1:** And over time, we go from left to right pictures
[00:07:46:350 - 00:07:49:059] **Speaker 1:** downstream, we see that it's quite a straight back.
[00:07:49:440 - 00:07:51:299] **Speaker 1:** So that could be because of that vortex.
[00:07:54:160 - 00:07:57:119] **Speaker 1:** Energy sort of, uh, melting the, the, the ice quicker
[00:07:57:119 - 00:07:57:600] **Speaker 1:** downstream.
[00:08:00:630 - 00:08:02:760] **Speaker 1:** Another example is lava.
[00:08:03:760 - 00:08:06:359] **Speaker 1:** So we did some work with some geologists.
[00:08:06:579 - 00:08:08:679] **Speaker 1:** So we've got a good geology department as well on
[00:08:08:679 - 00:08:09:040] **Speaker 1:** campus.
[00:08:10:079 - 00:08:11:500] **Speaker 1:** So I've been collaborating with them.
[00:08:11:959 - 00:08:14:660] **Speaker 1:** So that they're more into the observations in the field.
[00:08:15:890 - 00:08:17:600] **Speaker 1:** Whereas I'm more into numerical simulations.
[00:08:17:880 - 00:08:21:640] **Speaker 1:** So we look at approximating the lava field with numerical
[00:08:21:640 - 00:08:22:179] **Speaker 1:** models.
[00:08:22:720 - 00:08:26:899] **Speaker 1:** So we might have a volcano that's really large scale.
[00:08:27:529 - 00:08:31:250] **Speaker 1:** Uh, and then the lava might be reasonably wide, several
[00:08:31:250 - 00:08:33:809] **Speaker 1:** metres, but the thickness might only be a few 100
[00:08:33:809 - 00:08:34:280] **Speaker 1:** mills.
[00:08:34:770 - 00:08:38:049] **Speaker 1:** So thinking of how to approximate that, we could solve
[00:08:38:049 - 00:08:41:669] **Speaker 1:** it in a classical sense with CFD or we might
[00:08:41:669 - 00:08:44:270] **Speaker 1:** be able to make some assumptions and make it easier.
[00:08:44:690 - 00:08:47:169] **Speaker 1:** So I guess my main point here is that depending
[00:08:47:169 - 00:08:49:489] **Speaker 1:** on what you're modelling, you might want to make some
[00:08:49:489 - 00:08:53:469] **Speaker 1:** good assumptions for your model, and then validate that against
[00:08:53:469 - 00:08:56:659] **Speaker 1:** the observed data once you're finished.
[00:08:59:359 - 00:09:02:849] **Speaker 1:** So in this case, uh, we had the thickness of
[00:09:02:849 - 00:09:03:940] **Speaker 1:** the lava H.
[00:09:04:289 - 00:09:05:960] **Speaker 1:** So H is our dependent variable.
[00:09:06:010 - 00:09:07:849] **Speaker 1:** It's the thing that we're trying to solve for the
[00:09:07:849 - 00:09:10:489] **Speaker 1:** independent variables being just space and time X and T.
[00:09:11:369 - 00:09:16:530] **Speaker 1:** And we've got some PDE um that we're solving.
[00:09:16:890 - 00:09:19:919] **Speaker 1:** So I don't worry too much about the terms, but
[00:09:19:919 - 00:09:21:609] **Speaker 1:** essentially we're solving for the height profile.
[00:09:21:690 - 00:09:25:010] **Speaker 1:** So if we have initial Gaussian distribution, maybe it's erupting
[00:09:25:010 - 00:09:27:150] **Speaker 1:** from some hole, uh, from the volcano.
[00:09:28:200 - 00:09:30:919] **Speaker 1:** We've got this in purple x 0 and then over
[00:09:30:919 - 00:09:33:900] **Speaker 1:** time, if we've got gravity, it's sliding down the mountain.
[00:09:34:080 - 00:09:36:580] **Speaker 1:** So that's essentially what it's modelling here.
[00:09:39:049 - 00:09:41:690] **Speaker 1:** What we were interested in here is to approximate the
[00:09:41:690 - 00:09:44:460] **Speaker 1:** viscosity or the reality of the lava.
[00:09:44:969 - 00:09:50:090] **Speaker 1:** So lava rheology or viscosity, how, how it moves based
[00:09:50:090 - 00:09:54:330] **Speaker 1:** on sheer rates is very dependent on the composition.
[00:09:54:580 - 00:09:56:349] **Speaker 1:** So lots of chemistry and things.
[00:09:56:929 - 00:10:00:530] **Speaker 1:** So it can vary between volcanoes, and it can also
[00:10:00:530 - 00:10:02:460] **Speaker 1:** vary at the same volcano over time.
[00:10:02:989 - 00:10:05:750] **Speaker 1:** So if we can predict what that reality is in
[00:10:05:750 - 00:10:09:909] **Speaker 1:** real-time, then we can, um, create better forecasting and predicting
[00:10:09:909 - 00:10:11:450] **Speaker 1:** of the the lava flows.
[00:10:13:510 - 00:10:15:690] **Speaker 1:** So this is sort of just an example of optimisation
[00:10:16:109 - 00:10:18:869] **Speaker 1:** problem where we're trying to match some observed with our
[00:10:18:869 - 00:10:19:450] **Speaker 1:** model data.
[00:10:21:119 - 00:10:23:229] **Speaker 1:** We've got a viscosity expression.
[00:10:23:390 - 00:10:28:289] **Speaker 1:** So mu viscosity is a function of T temperature and
[00:10:28:289 - 00:10:33:270] **Speaker 1:** mu is some unknown value or coefficient and alpha is
[00:10:33:270 - 00:10:35:469] **Speaker 1:** an exponential coefficient that we're trying to figure out.
[00:10:35:869 - 00:10:38:869] **Speaker 1:** So we've got two unknowns and we're going to try
[00:10:38:869 - 00:10:41:770] **Speaker 1:** and match our model with the observed data.
[00:10:42:479 - 00:10:45:130] **Speaker 1:** So I've just created a plot essentially of the error.
[00:10:46:020 - 00:10:49:900] **Speaker 1:** And error being highest, uh, being in yellow and smallest
[00:10:49:900 - 00:10:50:409] **Speaker 1:** in purple.
[00:10:50:460 - 00:10:53:900] **Speaker 1:** So around this region, we see a good close match.
[00:10:55:559 - 00:10:58:080] **Speaker 1:** Uh, so that belongs to some series of immuno and
[00:10:58:080 - 00:10:59:049] **Speaker 1:** alpha pairs.
[00:10:59:450 - 00:11:03:760] **Speaker 1:** So that's just a brief introduction to, to the optimisation
[00:11:03:760 - 00:11:03:979] **Speaker 1:** process.
[00:11:05:479 - 00:11:07:229] **Speaker 1:** But that's why we might want to look at it
[00:11:07:849 - 00:11:10:150] **Speaker 1:** is because we don't have that data before we start
[00:11:10:150 - 00:11:10:890] **Speaker 1:** simulating.
[00:11:12:710 - 00:11:15:789] **Speaker 1:** Another project that I've been working on more recently is
[00:11:15:789 - 00:11:16:599] **Speaker 1:** on blood clotting.
[00:11:17:169 - 00:11:20:909] **Speaker 1:** Uh, so this is quite a common issue with people.
[00:11:21:460 - 00:11:25:429] **Speaker 1:** Uh they they form blood clots, uh, maybe, yeah, not
[00:11:25:429 - 00:11:29:229] **Speaker 1:** on purpose, uh, but they'll end up sometimes if it
[00:11:29:229 - 00:11:33:109] **Speaker 1:** dislodges and it hardens and then dislodges, it can lead
[00:11:33:109 - 00:11:34:390] **Speaker 1:** to strokes and heart attacks.
[00:11:34:429 - 00:11:38:469] **Speaker 1:** So that's quite a high rate of mortality for for
[00:11:38:469 - 00:11:39:049] **Speaker 1:** humans.
[00:11:39:780 - 00:11:43:380] **Speaker 1:** So we're trying to understand and characterise the properties, so
[00:11:43:380 - 00:11:45:739] **Speaker 1:** the mechanical properties of the clock.
[00:11:46:099 - 00:11:48:299] **Speaker 1:** So that's what my, my work at the moment is
[00:11:48:299 - 00:11:48:590] **Speaker 1:** on.
[00:11:49:450 - 00:11:51:409] **Speaker 1:** Uh, and maybe later on in the term, I'll give
[00:11:51:409 - 00:11:52:549] **Speaker 1:** more, more details.
[00:11:53:840 - 00:11:56:840] **Speaker 1:** Um, so another example I want to give is of
[00:11:56:840 - 00:11:57:900] **Speaker 1:** tsunami modelling.
[00:11:58:599 - 00:12:02:169] **Speaker 1:** So, We've not had too many tsunamis recently, but it
[00:12:02:169 - 00:12:04:510] **Speaker 1:** has been the odd one over the last while.
[00:12:05:119 - 00:12:07:869] **Speaker 1:** Uh, Japan is often hit quite badly.
[00:12:08:349 - 00:12:12:549] **Speaker 1:** Uh you've probably seen videos online of tsunamis, um, and
[00:12:12:549 - 00:12:14:609] **Speaker 1:** I've actually got like those rocks that are up the
[00:12:14:609 - 00:12:17:669] **Speaker 1:** hills that sort of indicate historic high levels.
[00:12:18:200 - 00:12:19:539] **Speaker 1:** Uh, so it's a non-problem.
[00:12:20:049 - 00:12:23:520] **Speaker 1:** uh, and it's a I guess it's important for forecasters,
[00:12:23:640 - 00:12:27:520] **Speaker 1:** weather forecasters, hazard management to predict how quickly the tsunami
[00:12:27:520 - 00:12:29:400] **Speaker 1:** is going to arrive based on an earthquake, what's the
[00:12:29:400 - 00:12:30:950] **Speaker 1:** chance of it happening and all of that.
[00:12:31:039 - 00:12:36:159] **Speaker 1:** So we have our own um NA NEA service.
[00:12:36:200 - 00:12:38:799] **Speaker 1:** They keep changing their names or different groups, but they
[00:12:38:799 - 00:12:40:719] **Speaker 1:** tell us whether or not the tsunami might be hitting
[00:12:40:719 - 00:12:41:190] **Speaker 1:** New Zealand.
[00:12:41:510 - 00:12:44:020] **Speaker 1:** Um, so they'll use different forecasting techniques.
[00:12:45:419 - 00:12:46:590] **Speaker 1:** So this example.
[00:12:59:789 - 00:13:00:840] **Speaker 1:** I take the dino, I don't want to play the
[00:13:00:840 - 00:13:01:320] **Speaker 1:** dino.
[00:13:07:989 - 00:13:08:669] **Speaker 1:** We'll trust that.
[00:13:09:309 - 00:13:10:020] **Speaker 1:** I won't say that.
[00:13:10:330 - 00:13:10:869] **Speaker 1:** It'll be fine.
[00:13:13:429 - 00:13:13:869] **Speaker 1:** I don't know.
[00:13:13:989 - 00:13:14:869] **Speaker 1:** Why is it not working?
[00:13:31:109 - 00:13:33:210] **Speaker 1:** This is how often I use this laptop, um.
[00:13:50:020 - 00:13:50:030] **Speaker 1:** Right.
[00:13:54:599 - 00:13:54:799] **Speaker 1:** Cool.
[00:13:54:919 - 00:13:55:340] **Speaker 1:** All right.
[00:13:55:750 - 00:14:00:280] **Speaker 1:** So here we have, uh, there's an open-source soft open-source
[00:14:00:280 - 00:14:04:159] **Speaker 1:** sort of um package that they have available for solving
[00:14:04:159 - 00:14:04:940] **Speaker 1:** equations.
[00:14:05:640 - 00:14:11:940] **Speaker 1:** So Basilisk and I just want to briefly.
[00:14:13:710 - 00:14:16:059] **Speaker 1:** I don't want to scare you, but I'll briefly go
[00:14:16:059 - 00:14:16:539] **Speaker 1:** through.
[00:14:18:059 - 00:14:19:299] **Speaker 1:** Um, this guy's equation.
[00:14:19:380 - 00:14:24:179] **Speaker 1:** So Stephane Paine is, uh, French, um, academic, but he
[00:14:24:179 - 00:14:27:059] **Speaker 1:** studied, he stayed in Wellington for a while in early
[00:14:27:059 - 00:14:30:760] **Speaker 1:** 2010s, um, with Nwa, and he's actually coming back for
[00:14:30:760 - 00:14:32:219] **Speaker 1:** a conference that we're hosting at the end of the
[00:14:32:219 - 00:14:32:380] **Speaker 1:** year.
[00:14:32:460 - 00:14:34:659] **Speaker 1:** So that should be cool to, cool to meet him.
[00:14:36:059 - 00:14:39:809] **Speaker 1:** Um, but his work is on, well, he does a
[00:14:39:809 - 00:14:42:340] **Speaker 1:** lot of work on shallow water approximation or, um, Saint
[00:14:42:340 - 00:14:43:059] **Speaker 1:** Berne equations.
[00:14:43:179 - 00:14:47:880] **Speaker 1:** So, Essentially the equations that we're solving for the tsunami
[00:14:47:880 - 00:14:49:419] **Speaker 1:** models, these guys.
[00:14:49:919 - 00:14:52:159] **Speaker 1:** So we've got 3 equations, and we solved that on
[00:14:52:159 - 00:14:53:340] **Speaker 1:** a computational grid.
[00:14:53:960 - 00:14:56:489] **Speaker 1:** So the unknowns are the height.
[00:14:57:239 - 00:14:59:119] **Speaker 1:** So I looked at the height for that lava flow,
[00:14:59:440 - 00:15:01:039] **Speaker 1:** but he's also looked at the velocities.
[00:15:01:239 - 00:15:04:400] **Speaker 1:** So how quickly the tsunami propagates across the ocean.
[00:15:04:520 - 00:15:07:880] **Speaker 1:** So that's with some velocity vector UV.
[00:15:09:099 - 00:15:12:119] **Speaker 1:** So the important approximations or assumptions that he's made.
[00:15:13:900 - 00:15:16:599] **Speaker 1:** is that he's used a long wave approximation.
[00:15:17:489 - 00:15:20:760] **Speaker 1:** So essentially he's assuming that the depth of the ocean
[00:15:20:760 - 00:15:24:539] **Speaker 1:** is much smaller than the depth range of the ocean,
[00:15:24:659 - 00:15:27:250] **Speaker 1:** so the width and the height, um, yeah, span.
[00:15:28:099 - 00:15:32:080] **Speaker 1:** So with those assumptions, we can reduce the Navier-Sokes equations
[00:15:32:080 - 00:15:32:940] **Speaker 1:** to these equations.
[00:15:33:340 - 00:15:35:219] **Speaker 1:** So those of you who are more familiar with the
[00:15:35:219 - 00:15:37:659] **Speaker 1:** mechanics, hopefully, you'll see these as being a little bit
[00:15:37:659 - 00:15:38:059] **Speaker 1:** simpler.
[00:15:38:380 - 00:15:42:559] **Speaker 1:** They're still nonlinear equations to solve, but they are much
[00:15:42:650 - 00:15:44:219] **Speaker 1:** less time consuming to solve for.
[00:15:47:190 - 00:15:49:820] **Speaker 1:** Or some, some pictures and animations.
[00:15:50:099 - 00:15:54:429] **Speaker 1:** So this is with um, Some wave elevation.
[00:15:55:590 - 00:16:00:739] **Speaker 1:** Originating from Japan, um, because I'm at that full screen.
[00:16:01:559 - 00:16:01:940] **Speaker 1:** No.
[00:16:03:250 - 00:16:03:880] **Speaker 1:** Not full screen.
[00:16:04:489 - 00:16:06:450] **Speaker 1:** Uh, so yeah, you can sort of see that it's
[00:16:06:450 - 00:16:11:349] **Speaker 1:** quite Diffractive or wavy, that bounces back off objects.
[00:16:11:789 - 00:16:13:830] **Speaker 1:** So that's sort of inherent with that that equation.
[00:16:16:929 - 00:16:19:390] **Speaker 1:** So we'll be looking at the wave equation later on.
[00:16:21:260 - 00:16:23:130] **Speaker 1:** Uh, here we have.
[00:16:26:109 - 00:16:28:330] **Speaker 1:** The animation of the level of refinement.
[00:16:28:989 - 00:16:32:030] **Speaker 1:** So we don't want to refine the entire ocean with
[00:16:32:030 - 00:16:34:419] **Speaker 1:** a really high resolution when we only look at the
[00:16:34:419 - 00:16:36:609] **Speaker 1:** tsunami that's propagating from one point.
[00:16:37:739 - 00:16:39:080] **Speaker 1:** And that's not gonna load.
[00:16:39:739 - 00:16:40:760] **Speaker 1:** It's great tech.
[00:16:41:419 - 00:16:42:099] **Speaker 1:** Oh gosh.
[00:16:45:919 - 00:16:47:039] **Speaker 1:** That's windows for you.
[00:16:58:140 - 00:17:01:619] **Speaker 1:** Alright, it's just slow, um.
[00:17:02:340 - 00:17:03:840] **Speaker 1:** So you can kind of see those big blocks on
[00:17:03:840 - 00:17:05:540] **Speaker 1:** the outside are forming.
[00:17:05:869 - 00:17:07:319] **Speaker 1:** And that's a course grid.
[00:17:07:599 - 00:17:09:040] **Speaker 1:** So this is called adaptive mesh refinement.
[00:17:09:079 - 00:17:12:760] **Speaker 1:** It's quite a neat algorithm, where it's refining where you
[00:17:12:760 - 00:17:14:050] **Speaker 1:** have interesting behaviour.
[00:17:14:079 - 00:17:16:459] **Speaker 1:** So you could define it based on local error, local
[00:17:16:459 - 00:17:17:880] **Speaker 1:** velocity gradients and things.
[00:17:18:709 - 00:17:21:500] **Speaker 1:** So they they're more refined near those red regions.
[00:17:21:760 - 00:17:23:890] **Speaker 1:** So that's all I wanted to show in this example.
[00:17:27:500 - 00:17:28:180] **Speaker 1:** All right.
[00:17:28:660 - 00:17:31:180] **Speaker 1:** So because it's open source, you're welcome to download that
[00:17:31:180 - 00:17:33:180] **Speaker 1:** and go through the tutorials and things like that like
[00:17:33:180 - 00:17:33:540] **Speaker 1:** that.
[00:17:33:780 - 00:17:38:859] **Speaker 1:** Um, so that Is, you know, bacillus.
[00:17:39:410 - 00:17:40:000] **Speaker 1:** Fr.
[00:17:41:390 - 00:17:44:719] **Speaker 1:** Cool So some learning outcomes for the rest of this
[00:17:44:719 - 00:17:45:150] **Speaker 1:** course.
[00:17:46:099 - 00:17:48:660] **Speaker 1:** So we're going to look at some different partial differential
[00:17:48:660 - 00:17:49:260] **Speaker 1:** equations.
[00:17:49:479 - 00:17:50:400] **Speaker 1:** So PDEs.
[00:17:50:939 - 00:17:53:819] **Speaker 1:** We're going to look at elliptic, parabolic and hyperbolic.
[00:17:54:099 - 00:17:56:300] **Speaker 1:** So they have sort of different shapes and different solution
[00:17:56:300 - 00:17:58:079] **Speaker 1:** strategies that we might want to employ.
[00:17:59:229 - 00:18:00:739] **Speaker 1:** We're going to look at different boundary conditions.
[00:18:00:989 - 00:18:03:250] **Speaker 1:** So to make a unique solution, we need to have
[00:18:03:260 - 00:18:04:750] **Speaker 1:** a set of boundary conditions.
[00:18:04:949 - 00:18:07:089] **Speaker 1:** Otherwise, you have an infinite number of solutions.
[00:18:09:189 - 00:18:12:630] **Speaker 1:** For example, for the ice example, if you have melting
[00:18:12:630 - 00:18:17:910] **Speaker 1:** ice, if the boundary condition in the pot was 10
[00:18:17:910 - 00:18:19:630] **Speaker 1:** degrees, that would give a different solution to 50 or
[00:18:19:630 - 00:18:20:260] **Speaker 1:** 60 degrees.
[00:18:20:310 - 00:18:21:449] **Speaker 1:** It's going to melt quicker.
[00:18:23:560 - 00:18:27:300] **Speaker 1:** for unsteady solutions, solutions that change with time, we need
[00:18:27:300 - 00:18:28:819] **Speaker 1:** an initial condition as well.
[00:18:29:760 - 00:18:30:920] **Speaker 1:** We're going to use separation of variables.
[00:18:30:989 - 00:18:33:199] **Speaker 1:** You probably come across this in your math courses so
[00:18:33:199 - 00:18:35:660] **Speaker 1:** far, but we continue with those and PDEs.
[00:18:36:520 - 00:18:40:530] **Speaker 1:** Uh, some Laplace transform, some Di Lambert solutions, so these
[00:18:40:530 - 00:18:41:869] **Speaker 1:** are for wave equation.
[00:18:42:869 - 00:18:48:589] **Speaker 1:** And Yeah, just some general PD models, city and transient
[00:18:48:589 - 00:18:52:890] **Speaker 1:** heat transfer, uh, potential flow, transient flow, elastic bending and
[00:18:52:890 - 00:18:53:599] **Speaker 1:** waves.
[00:18:55:050 - 00:18:58:890] **Speaker 1:** So we want to introduce you to some more analytical
[00:18:58:890 - 00:19:02:130] **Speaker 1:** methods, which we can use and to the extent that
[00:19:02:130 - 00:19:02:939] **Speaker 1:** they are possible.
[00:19:03:060 - 00:19:04:310] **Speaker 1:** So there's limitations with them.
[00:19:04:930 - 00:19:08:170] **Speaker 1:** And then we'll also introduce numerical methods to discretization as
[00:19:08:170 - 00:19:08:510] **Speaker 1:** well.
[00:19:10:680 - 00:19:14:500] **Speaker 1:** So numerical methods, we're going to talk about accuracy, uh,
[00:19:14:579 - 00:19:19:050] **Speaker 1:** consistency, convergence, I recognise and apply some different numerical solution,
[00:19:19:449 - 00:19:20:400] **Speaker 1:** uh, techniques.
[00:19:20:780 - 00:19:22:300] **Speaker 1:** So spatial discretization.
[00:19:22:500 - 00:19:25:989] **Speaker 1:** So across the ocean, uh, finite differenceencing weight of residuals.
[00:19:26:060 - 00:19:27:699] **Speaker 1:** So you've already looked at some of these with your
[00:19:27:699 - 00:19:33:160] **Speaker 1:** finite elements so far, uh, polynomial interpolating or interpolations, uh,
[00:19:33:180 - 00:19:35:599] **Speaker 1:** finite element methods and optimisation methods.
[00:19:37:920 - 00:19:39:770] **Speaker 1:** Uh, so some more things.
[00:19:40:170 - 00:19:42:530] **Speaker 1:** So console, so we're gonna use console as our software
[00:19:42:530 - 00:19:43:010] **Speaker 1:** package.
[00:19:43:449 - 00:19:46:050] **Speaker 1:** Uh, I'll talk more about that maybe next week just
[00:19:46:050 - 00:19:48:530] **Speaker 1:** to not sort of bombard you with everything at once,
[00:19:48:890 - 00:19:51:150] **Speaker 1:** uh, but we'll, we'll go over that next week.
[00:19:51:890 - 00:19:54:130] **Speaker 1:** Um, so essentially we're gonna use, well, we're gonna do
[00:19:54:130 - 00:19:56:530] **Speaker 1:** what we can with Python, uh, and then essentially use
[00:19:56:530 - 00:19:58:670] **Speaker 1:** console for, for the more tricky problems.
[00:19:59:300 - 00:20:01:180] **Speaker 1:** But we, I guess the point that I want to
[00:20:01:180 - 00:20:03:260] **Speaker 1:** make is that we don't want to have a black
[00:20:03:260 - 00:20:07:500] **Speaker 1:** box that we just trust implicit or explicitly, uh, and
[00:20:07:500 - 00:20:08:380] **Speaker 1:** hope that it works.
[00:20:08:699 - 00:20:11:300] **Speaker 1:** Uh, you need to have a good foundational understanding of
[00:20:11:300 - 00:20:14:270] **Speaker 1:** how these tools work, uh, so that you have confidence
[00:20:14:270 - 00:20:15:040] **Speaker 1:** in their results.
[00:20:15:459 - 00:20:18:339] **Speaker 1:** So there's no point producing some results and them being
[00:20:18:339 - 00:20:18:839] **Speaker 1:** wrong.
[00:20:19:550 - 00:20:21:199] **Speaker 1:** So that's can't be understated.
[00:20:24:479 - 00:20:24:489] **Speaker 1:** Yeah.
[00:20:25:859 - 00:20:28:660] **Speaker 1:** So a bit of a roadmap for the remainder 5
[00:20:28:699 - 00:20:29:699] **Speaker 1:** weeks 5 to 12.
[00:20:30:099 - 00:20:34:780] **Speaker 1:** So we're going through this introduction today and probably finish
[00:20:34:780 - 00:20:35:819] **Speaker 1:** it on Wednesday morning.
[00:20:36:099 - 00:20:37:479] **Speaker 1:** Oh, yeah, I think it's morning.
[00:20:38:050 - 00:20:39:500] **Speaker 1:** We're talking about partial differential equations.
[00:20:39:589 - 00:20:40:469] **Speaker 1:** That's chapter one.
[00:20:41:520 - 00:20:42:900] **Speaker 1:** Of the course reader.
[00:20:43:719 - 00:20:45:479] **Speaker 1:** Then we're going to talk about those elliptic PDEs.
[00:20:45:680 - 00:20:47:959] **Speaker 1:** So there's one of those three types that we're going
[00:20:47:959 - 00:20:48:729] **Speaker 1:** to discuss.
[00:20:49:280 - 00:20:54:640] **Speaker 1:** I'll talk through the console next week, including some geometry
[00:20:54:640 - 00:20:56:380] **Speaker 1:** modelling and fundamentals of grid generation.
[00:20:56:599 - 00:20:58:380] **Speaker 1:** So that's that mesh of discretization.
[00:20:59:449 - 00:21:03:979] **Speaker 1:** Talk about finite differences in term for some transient PDEs,
[00:21:04:209 - 00:21:06:199] **Speaker 1:** hyperbolic, which is the wave equation.
[00:21:06:900 - 00:21:07:579] **Speaker 1:** So it's a good fun.
[00:21:07:880 - 00:21:11:979] **Speaker 1:** They're quite unstable, finite element method for PDEs in 1
[00:21:11:979 - 00:21:14:859] **Speaker 1:** day and an application of that, and then extending to
[00:21:14:859 - 00:21:16:979] **Speaker 1:** multiple dimensions and you'll find that it's quite a lot
[00:21:16:979 - 00:21:19:030] **Speaker 1:** of housekeeping or bookkeeping.
[00:21:19:380 - 00:21:21:829] **Speaker 1:** So we just delegate that to console, but the idea
[00:21:21:829 - 00:21:23:609] **Speaker 1:** is that we're going to teach you how how it
[00:21:23:609 - 00:21:24:020] **Speaker 1:** works.
[00:21:26:599 - 00:21:28:810] **Speaker 1:** Consistency, stability and convergence.
[00:21:29:300 - 00:21:32:959] **Speaker 1:** So these are all really important tech, um, terms or
[00:21:32:959 - 00:21:34:810] **Speaker 1:** features of numerical methods.
[00:21:35:199 - 00:21:37:069] **Speaker 1:** Uh, I might bring it up a bit earlier in
[00:21:37:069 - 00:21:38:069] **Speaker 1:** the the term.
[00:21:39:270 - 00:21:40:670] **Speaker 1:** And optimisation methods.
[00:21:40:949 - 00:21:43:560] **Speaker 1:** So yeah, I think that's that's fun.
[00:21:44:349 - 00:21:46:790] **Speaker 1:** And then last week, we'll just revise and prepare for
[00:21:46:790 - 00:21:47:229] **Speaker 1:** the exam.
[00:21:47:589 - 00:21:50:310] **Speaker 1:** So the exams only on my content, not not the
[00:21:50:310 - 00:21:51:089] **Speaker 1:** 1st 4 weeks.
[00:21:55:750 - 00:21:56:849] **Speaker 1:** So assessments.
[00:21:57:869 - 00:22:01:939] **Speaker 1:** We've got 51% quizzes due each Friday, starting from week
[00:22:01:939 - 00:22:02:880] **Speaker 1:** 6.
[00:22:03:739 - 00:22:06:420] **Speaker 1:** So there'll be a combination.
[00:22:06:739 - 00:22:10:500] **Speaker 1:** Well, I'll be reasonably short quizzes through learn that you
[00:22:10:500 - 00:22:12:589] **Speaker 1:** just do in your own time and submit by the
[00:22:12:589 - 00:22:13:520] **Speaker 1:** end of Friday.
[00:22:14:790 - 00:22:18:760] **Speaker 1:** Uh, they'll be a mixture of sort of multi-choice coding
[00:22:19:270 - 00:22:21:699] **Speaker 1:** and uh console questions.
[00:22:22:069 - 00:22:23:979] **Speaker 1:** So do some work in console and then produce your
[00:22:23:979 - 00:22:24:359] **Speaker 1:** results.
[00:22:26:010 - 00:22:29:109] **Speaker 1:** We've got an assignment, uh, that's during the last week.
[00:22:29:969 - 00:22:32:170] **Speaker 1:** So I'll talk more about that.
[00:22:33:030 - 00:22:35:989] **Speaker 1:** In the term 4, and try and get onto it
[00:22:35:989 - 00:22:36:270] **Speaker 1:** early.
[00:22:36:420 - 00:22:39:390] **Speaker 1:** I know the trans students are already into RoboCup in
[00:22:39:390 - 00:22:42:949] **Speaker 1:** term 4 each every year, um, which is good, but
[00:22:42:949 - 00:22:44:609] **Speaker 1:** yep, time management.
[00:22:44:790 - 00:22:48:089] **Speaker 1:** And then the final exam is 50% of the course
[00:22:48:430 - 00:22:50:609] **Speaker 1:** and that's during the normal exam period.
[00:22:51:229 - 00:22:53:750] **Speaker 1:** Uh, it's often the first or second day of the
[00:22:53:750 - 00:22:57:329] **Speaker 1:** exam period, but who knows when it will be allocated.
[00:22:58:750 - 00:23:01:829] **Speaker 1:** Uh, so a good rule of thumb that I find,
[00:23:01:949 - 00:23:04:040] **Speaker 1:** or I found as a student, uh, was to spend
[00:23:04:040 - 00:23:06:109] **Speaker 1:** about 1 hour per% of the course grade.
[00:23:06:349 - 00:23:08:229] **Speaker 1:** So if you had a 10% assignment, you might spend
[00:23:08:229 - 00:23:08:869] **Speaker 1:** 10 hours.
[00:23:09:229 - 00:23:10:670] **Speaker 1:** You might want to spend a few more than 10
[00:23:10:670 - 00:23:12:829] **Speaker 1:** hours for my assignment, but just as a general rule
[00:23:12:829 - 00:23:16:569] **Speaker 1:** of thumb, so I, yeah, my feedback was to be,
[00:23:16:910 - 00:23:19:189] **Speaker 1:** yeah, um, so.
[00:23:19:790 - 00:23:20:270] **Speaker 1:** Roughly.
[00:23:20:560 - 00:23:22:910] **Speaker 1:** So you're not probably not gonna spend 50 hours preparing
[00:23:22:910 - 00:23:24:069] **Speaker 1:** for the exam.
[00:23:25:150 - 00:23:29:189] **Speaker 1:** Um, so we've got, I think it's 32 hours of
[00:23:29:189 - 00:23:34:180] **Speaker 1:** lectures, um, and Well, I've got 32 hours of labs,
[00:23:34:219 - 00:23:36:300] **Speaker 1:** but you guys will have a third of that 1010,
[00:23:36:380 - 00:23:40:810] **Speaker 1:** 10 hours or so of labs for, um, For preparing,
[00:23:40:939 - 00:23:43:180] **Speaker 1:** so yeah, that and the.
[00:23:44:560 - 00:23:46:760] **Speaker 1:** 1 hour per% as a good rule of thumb.
[00:23:47:209 - 00:23:50:130] **Speaker 1:** I'm not sure if that That works out for everyone,
[00:23:50:329 - 00:23:51:469] **Speaker 1:** but hopefully it will.
[00:23:52:530 - 00:23:56:709] **Speaker 1:** The contact times, um, you know them better than me,
[00:23:57:050 - 00:24:00:800] **Speaker 1:** uh, in the labs, you attend one of these three
[00:24:00:800 - 00:24:05:939] **Speaker 1:** streams, so You have them allocated in your timetable.
[00:24:06:369 - 00:24:11:109] **Speaker 1:** Uh, so I mean, every year the the first stream
[00:24:11:109 - 00:24:13:339] **Speaker 1:** is always more popular and we get too busy.
[00:24:13:390 - 00:24:15:430] **Speaker 1:** So make sure that you attend the stream that you've
[00:24:15:430 - 00:24:18:670] **Speaker 1:** been allocated to in the timetable so that we have
[00:24:18:670 - 00:24:21:609] **Speaker 1:** some good load balancing so you can answer everyone's questions.
[00:24:22:670 - 00:24:23:949] **Speaker 1:** And that's all in the next week.
[00:24:24:790 - 00:24:25:670] **Speaker 1:** Uh, office hours.
[00:24:25:750 - 00:24:27:910] **Speaker 1:** I've tried to do office hours at a set time
[00:24:27:910 - 00:24:29:869] **Speaker 1:** before or once I tried and it didn't really work
[00:24:29:869 - 00:24:30:250] **Speaker 1:** out.
[00:24:30:430 - 00:24:32:939] **Speaker 1:** Um, people just didn't show up and then showed up
[00:24:32:939 - 00:24:34:410] **Speaker 1:** at other times, so it's like whatever.
[00:24:34:790 - 00:24:36:729] **Speaker 1:** So just open door policy, um.
[00:24:37:609 - 00:24:40:170] **Speaker 1:** It's much easier to ask questions in the lectures, I
[00:24:40:170 - 00:24:42:859] **Speaker 1:** find rather than waiting, because we see each other practically
[00:24:42:859 - 00:24:43:479] **Speaker 1:** every day.
[00:24:44:099 - 00:24:47:280] **Speaker 1:** So make sure that you, yeah, ask questions in class.
[00:24:47:979 - 00:24:49:699] **Speaker 1:** I'll try to keep an eye out, otherwise, just yell
[00:24:49:699 - 00:24:50:069] **Speaker 1:** out.
[00:24:51:329 - 00:24:53:680] **Speaker 1:** Take advantage of our contact times.
[00:24:54:010 - 00:24:55:010] **Speaker 1:** Yeah, generally eager.
[00:24:55:109 - 00:24:56:869] **Speaker 1:** I think I'm still eager to answer questions.
[00:24:57:449 - 00:24:58:209] **Speaker 1:** So it's good.
[00:24:58:609 - 00:25:00:569] **Speaker 1:** Uh, and we've got a course forum.
[00:25:00:689 - 00:25:02:560] **Speaker 1:** I think one person used it so fast, that's neat.
[00:25:02:859 - 00:25:07:609] **Speaker 1:** Um, but Um, yeah, just use that as a way
[00:25:07:609 - 00:25:11:199] **Speaker 1:** of asking questions because if you're wondering one thing, obviously
[00:25:11:199 - 00:25:12:630] **Speaker 1:** it's going to be like a lot of other people
[00:25:12:630 - 00:25:13:770] **Speaker 1:** that are wondering the same thing.
[00:25:14:349 - 00:25:18:069] **Speaker 1:** And I can't answer every single person with the same
[00:25:18:069 - 00:25:18:329] **Speaker 1:** energy.
[00:25:18:630 - 00:25:22:040] **Speaker 1:** So, um, it's much easier to use a, use the
[00:25:22:040 - 00:25:22:380] **Speaker 1:** farm.
[00:25:22:739 - 00:25:26:069] **Speaker 1:** Um, I've also collected a series of frequently asked questions,
[00:25:26:099 - 00:25:28:829] **Speaker 1:** which I'll figure out what's the best way to include
[00:25:28:829 - 00:25:29:380] **Speaker 1:** that on then.
[00:25:30:390 - 00:25:33:079] **Speaker 1:** As well, but that's probably more towards the assignment and
[00:25:33:079 - 00:25:33:780] **Speaker 1:** the exam.
[00:25:34:640 - 00:25:36:839] **Speaker 1:** Um, and then use email if you've got, if you're
[00:25:36:839 - 00:25:39:619] **Speaker 1:** like sick or you've missed something or something like that.
[00:25:42:349 - 00:25:43:050] **Speaker 1:** All right.
[00:25:43:569 - 00:25:49:469] **Speaker 1:** Um, so our remaining lectures will be with these these
[00:25:49:469 - 00:25:50:329] **Speaker 1:** course readers.
[00:25:50:750 - 00:25:53:239] **Speaker 1:** So the printed ones are black and white and the
[00:25:53:239 - 00:25:55:709] **Speaker 1:** digital one is colour because it's way cheaper to print
[00:25:55:709 - 00:25:56:390] **Speaker 1:** black and white.
[00:25:56:790 - 00:26:00:469] **Speaker 1:** I've tried to, I mean, the there's only a handful
[00:26:00:469 - 00:26:05:979] **Speaker 1:** of figures that are colours and Yeah, it doesn't, it
[00:26:05:979 - 00:26:06:790] **Speaker 1:** doesn't really matter.
[00:26:07:069 - 00:26:09:099] **Speaker 1:** Um, you can tell what what they represent.
[00:26:09:459 - 00:26:12:079] **Speaker 1:** Uh, in fact, if you have a good colour scheme
[00:26:12:079 - 00:26:14:579] **Speaker 1:** when you're plotting, uh, you want to make sure that
[00:26:14:579 - 00:26:17:660] **Speaker 1:** it transfers across to black and white well, so it
[00:26:17:660 - 00:26:18:719] **Speaker 1:** goes from black to white.
[00:26:19:060 - 00:26:23:060] **Speaker 1:** So I, I won't bore you with that detail.
[00:26:24:300 - 00:26:25:900] **Speaker 1:** So skim read notes before class.
[00:26:26:099 - 00:26:26:660] **Speaker 1:** I, I don't know.
[00:26:26:739 - 00:26:28:750] **Speaker 1:** I mean that would be uh ideal.
[00:26:28:900 - 00:26:30:160] **Speaker 1:** I don't know if anyone does that.
[00:26:30:380 - 00:26:33:479] **Speaker 1:** Um, fill in the gaps and write additional notes.
[00:26:33:540 - 00:26:36:199] **Speaker 1:** So the idea is that when I'm working through, uh,
[00:26:36:209 - 00:26:38:140] **Speaker 1:** problems and writing in the course reader, you're doing the
[00:26:38:140 - 00:26:38:479] **Speaker 1:** same.
[00:26:38:859 - 00:26:41:290] **Speaker 1:** So trying to engage your brain more rather than just
[00:26:41:290 - 00:26:43:839] **Speaker 1:** listening to me like today, everyone's gonna fall asleep.
[00:26:44:380 - 00:26:46:880] **Speaker 1:** Um, so that's, that's the general idea.
[00:26:47:780 - 00:26:49:699] **Speaker 1:** And at the end of each chapter, we've got some
[00:26:49:699 - 00:26:52:280] **Speaker 1:** exercises, uh, some questions for you to work through.
[00:26:52:900 - 00:26:57:420] **Speaker 1:** So attempt those, I guess ideally at after we've done
[00:26:57:420 - 00:26:59:930] **Speaker 1:** the chapter, but just when you get a spare moment,
[00:27:00:250 - 00:27:02:459] **Speaker 1:** and I've provided the solutions in the back.
[00:27:02:660 - 00:27:03:589] **Speaker 1:** So Appendix E.
[00:27:04:739 - 00:27:06:619] **Speaker 1:** So you can check for yourself, but as with anything
[00:27:06:619 - 00:27:08:260] **Speaker 1:** you want to give it a good shot the first
[00:27:08:260 - 00:27:08:500] **Speaker 1:** time.
[00:27:08:619 - 00:27:12:400] **Speaker 1:** Otherwise, you're just, yeah, that doesn't work very well.
[00:27:12:750 - 00:27:15:780] **Speaker 1:** Um, because if, if you can read my solutions and
[00:27:15:780 - 00:27:17:859] **Speaker 1:** make sense of it, that's great, but you need to
[00:27:17:859 - 00:27:20:160] **Speaker 1:** be able to work through that problem yourself first.
[00:27:21:969 - 00:27:23:949] **Speaker 1:** And then final revision before the exam.
[00:27:24:449 - 00:27:25:569] **Speaker 1:** So that's study week.
[00:27:27:520 - 00:27:28:989] **Speaker 1:** I don't know, I picked these out a few years
[00:27:28:989 - 00:27:29:380] **Speaker 1:** ago.
[00:27:29:680 - 00:27:32:260] **Speaker 1:** I don't know if anyone has actually read them, but
[00:27:32:920 - 00:27:35:949] **Speaker 1:** I, I, my feeling is that writing with pen and
[00:27:35:949 - 00:27:37:800] **Speaker 1:** paper is is better for my learning.
[00:27:38:189 - 00:27:41:030] **Speaker 1:** Um, and the fill in the gaps was the most
[00:27:41:030 - 00:27:41:390] **Speaker 1:** popular.
[00:27:41:469 - 00:27:43:270] **Speaker 1:** I asked, I think it's 24.
[00:27:43:890 - 00:27:47:060] **Speaker 1:** Um, I asked the class in the student survey, uh,
[00:27:47:069 - 00:27:50:869] **Speaker 1:** what, what format they preferred, and it was 74% that
[00:27:50:869 - 00:27:54:209] **Speaker 1:** preferred fill in the blanks versus PowerPoint versus Complete notes.
[00:27:54:709 - 00:27:57:069] **Speaker 1:** Uh, so it gives me a little bit of confidence
[00:27:57:069 - 00:27:59:449] **Speaker 1:** that the majority of the class prefers this method.
[00:28:00:089 - 00:28:05:010] **Speaker 1:** I will upload the scanned versions to learn afterwards, so
[00:28:05:010 - 00:28:06:959] **Speaker 1:** if you don't want to write anything in the class,
[00:28:07:290 - 00:28:08:219] **Speaker 1:** that's fine as well.
[00:28:10:849 - 00:28:11:890] **Speaker 1:** The learn page.
[00:28:13:410 - 00:28:16:619] **Speaker 1:** So you're familiar with how Len works.
[00:28:16:819 - 00:28:20:900] **Speaker 1:** Uh, so everything that I'm teaching is going to be
[00:28:20:900 - 00:28:21:550] **Speaker 1:** on this part.
[00:28:22:050 - 00:28:25:719] **Speaker 1:** Uh, so that's including the quizzes and assignment details.
[00:28:27:270 - 00:28:34:829] **Speaker 1:** The course material link or folder uh has Yeah, Python
[00:28:34:829 - 00:28:38:349] **Speaker 1:** scripts console model files and things like that.
[00:28:38:390 - 00:28:41:439] **Speaker 1:** And I'll also upload the scanned versions of the course
[00:28:41:439 - 00:28:42:260] **Speaker 1:** reader as well.
[00:28:42:800 - 00:28:44:520] **Speaker 1:** You can download that in bulk.
[00:28:44:880 - 00:28:46:319] **Speaker 1:** So I think it's got like a download folder on
[00:28:46:319 - 00:28:47:060] **Speaker 1:** the top right.
[00:28:47:319 - 00:28:49:319] **Speaker 1:** You don't have to download every single file separately and
[00:28:49:319 - 00:28:51:099] **Speaker 1:** it's in a nice folder structure.
[00:28:53:020 - 00:28:57:300] **Speaker 1:** And maybe I'll send out those change notifications when I
[00:28:57:300 - 00:28:59:750] **Speaker 1:** update it just so you know, when I've updated it,
[00:28:59:910 - 00:29:01:280] **Speaker 1:** otherwise it's a bit hard to keep track.
[00:29:02:449 - 00:29:05:890] **Speaker 1:** Um, because it doesn't have the edit uploaded version like
[00:29:05:890 - 00:29:06:469] **Speaker 1:** the PDF.
[00:29:07:489 - 00:29:09:689] **Speaker 1:** So the course discussion from there's a link elsewhere, but
[00:29:09:689 - 00:29:12:410] **Speaker 1:** this is the same, same link to that that from
[00:29:12:410 - 00:29:14:180] **Speaker 1:** that someone's used once.
[00:29:14:650 - 00:29:16:770] **Speaker 1:** And in the contact times just reiterating what I've just
[00:29:16:770 - 00:29:17:089] **Speaker 1:** said.
[00:29:17:489 - 00:29:20:890] **Speaker 1:** Some additional reading, uh, so.
[00:29:22:300 - 00:29:25:859] **Speaker 1:** Yeah, if you want to do some background reading on
[00:29:26:060 - 00:29:28:510] **Speaker 1:** on these topics, I've provided a few textbooks.
[00:29:28:859 - 00:29:30:619] **Speaker 1:** Uh, don't feel like you do need to read them.
[00:29:30:829 - 00:29:33:579] **Speaker 1:** Everything I cover in here will be in the exam.
[00:29:34:589 - 00:29:38:310] **Speaker 1:** So don't worry too much, but just for those really
[00:29:38:310 - 00:29:39:449] **Speaker 1:** motivated people.
[00:29:43:500 - 00:29:44:099] **Speaker 1:** All right.
[00:29:44:420 - 00:29:48:300] **Speaker 1:** Any questions so far about the admin and logistics?
[00:29:49:349 - 00:29:49:359] **Speaker 1:** No.
[00:29:51:939 - 00:29:54:380] **Speaker 1:** That's pretty straightforward.
[00:29:54:650 - 00:29:55:050] **Speaker 1:** All right.
[00:29:55:319 - 00:29:59:530] **Speaker 1:** So talk a little bit about designing uh components and
[00:29:59:530 - 00:30:01:069] **Speaker 1:** systems within engineering.
[00:30:01:569 - 00:30:04:609] **Speaker 1:** So what are some of the examples or options that
[00:30:04:609 - 00:30:05:209] **Speaker 1:** we have?
[00:30:06:420 - 00:30:08:130] **Speaker 1:** So we could use existing guidelines.
[00:30:08:489 - 00:30:14:119] **Speaker 1:** So there's heaps of standards that industry, government council produce
[00:30:14:119 - 00:30:17:180] **Speaker 1:** that engineers or whoever needs to follow.
[00:30:17:459 - 00:30:21:180] **Speaker 1:** So those are sort of been established that good practise
[00:30:21:180 - 00:30:25:359] **Speaker 1:** generally, and I use so just copy and paste, essentially,
[00:30:25:619 - 00:30:27:770] **Speaker 1:** we'll work out the solutions.
[00:30:30:489 - 00:30:35:650] **Speaker 1:** Uh, or we could make some simplifying assumptions and apply
[00:30:35:650 - 00:30:37:369] **Speaker 1:** some basic engineering analysis.
[00:30:37:969 - 00:30:40:569] **Speaker 1:** So you've done some of this with your free body
[00:30:40:569 - 00:30:44:569] **Speaker 1:** diagrams and things in 102, and you've probably done all
[00:30:44:569 - 00:30:46:310] **Speaker 1:** those in your design courses as well.
[00:30:46:689 - 00:30:48:390] **Speaker 1:** I think the existing guidelines you might have touched on
[00:30:48:390 - 00:30:49:689] **Speaker 1:** in your design courses as well.
[00:30:49:770 - 00:30:52:709] **Speaker 1:** If not next year, usually look at some pressure vessels
[00:30:52:849 - 00:30:53:550] **Speaker 1:** and things like that.
[00:30:55:270 - 00:31:00:680] **Speaker 1:** Um, so you might use some spreadsheets, Python cals, um,
[00:31:01:099 - 00:31:04:359] **Speaker 1:** yeah, to, to, to maybe extend the guidelines.
[00:31:05:020 - 00:31:07:439] **Speaker 1:** Third option here is an experimental investigation.
[00:31:07:619 - 00:31:09:819] **Speaker 1:** So this is like a physical setup where we go
[00:31:09:819 - 00:31:10:959] **Speaker 1:** out and do something.
[00:31:11:810 - 00:31:15:449] **Speaker 1:** So this can improve our existing data, can also be
[00:31:15:449 - 00:31:17:410] **Speaker 1:** used to create new data.
[00:31:17:530 - 00:31:20:329] **Speaker 1:** So maybe we're testing an aerofoil and we want to
[00:31:20:329 - 00:31:22:010] **Speaker 1:** look at different angles of attack, trying to figure out
[00:31:22:010 - 00:31:22:910] **Speaker 1:** where it stalls.
[00:31:23:410 - 00:31:26:130] **Speaker 1:** If we adjust it, maybe add those little winglets or
[00:31:26:130 - 00:31:29:849] **Speaker 1:** wingtips at the end, which yeah, which was quite cool.
[00:31:29:890 - 00:31:31:849] **Speaker 1:** They did that a few years ago to reduce the
[00:31:31:849 - 00:31:32:670] **Speaker 1:** fuel usage.
[00:31:34:829 - 00:31:38:609] **Speaker 1:** Uh, the fourth option here is numerical simulation, so using,
[00:31:38:699 - 00:31:41:310] **Speaker 1:** um, sort of high fidelity or high resolution numerical models.
[00:31:43:109 - 00:31:46:270] **Speaker 1:** So, That's sort of what we're going to be focusing
[00:31:46:270 - 00:31:47:849] **Speaker 1:** on in this course.
[00:31:48:880 - 00:31:50:680] **Speaker 1:** But be aware of these other three options.
[00:31:51:140 - 00:31:53:020] **Speaker 1:** So you might use a combination of these approaches.
[00:31:53:119 - 00:31:54:439] **Speaker 1:** You might go as far as you can with options
[00:31:54:439 - 00:31:57:250] **Speaker 1:** one and two, and then sort of have a close
[00:31:57:250 - 00:32:00:680] **Speaker 1:** think about is it worthwhile doing some physical experiments or
[00:32:00:680 - 00:32:01:670] **Speaker 1:** numerical simulations.
[00:32:01:719 - 00:32:04:660] **Speaker 1:** They both have their drawbacks and expenses.
[00:32:05:160 - 00:32:06:680] **Speaker 1:** So if someone's already done all the work for you,
[00:32:06:800 - 00:32:08:359] **Speaker 1:** obviously, just go with the guidelines.
[00:32:08:589 - 00:32:09:260] **Speaker 1:** So that's great.
[00:32:09:910 - 00:32:10:640] **Speaker 1:** Um.
[00:32:11:089 - 00:32:14:449] **Speaker 1:** But yeah, if you want to do something more new,
[00:32:14:569 - 00:32:17:209] **Speaker 1:** distinct, novel research, uh, you'll want to do some more
[00:32:17:209 - 00:32:18:790] **Speaker 1:** experiments or simulations.
[00:32:20:550 - 00:32:23:680] **Speaker 1:** So when will these 1st 3 options be unsatisfactory?
[00:32:24:310 - 00:32:29:949] **Speaker 1:** So maybe We want to create an entirely new concept,
[00:32:30:170 - 00:32:31:569] **Speaker 1:** which the rules don't exist for.
[00:32:32:150 - 00:32:34:609] **Speaker 1:** Uh, so the example I gave is that little wing
[00:32:34:609 - 00:32:36:439] **Speaker 1:** wingtip on the air falls.
[00:32:36:449 - 00:32:38:219] **Speaker 1:** I guess when they first designed that they had to
[00:32:38:219 - 00:32:41:599] **Speaker 1:** go through the Federal Aviation Authority to to validate all
[00:32:41:599 - 00:32:44:849] **Speaker 1:** of that and get it approved for flight.
[00:32:46:599 - 00:32:50:119] **Speaker 1:** So, yeah, or when existing data doesn't cover the design
[00:32:50:119 - 00:32:50:310] **Speaker 1:** space.
[00:32:50:359 - 00:32:54:540] **Speaker 1:** So maybe it was designed for a different environment, um,
[00:32:55:199 - 00:32:56:079] **Speaker 1:** so maybe.
[00:32:58:319 - 00:33:00:729] **Speaker 1:** I don't know what example, but, um, if it, if
[00:33:00:729 - 00:33:04:020] **Speaker 1:** it wasn't designed for below 0 degrees temperature, for example.
[00:33:05:660 - 00:33:07:050] **Speaker 1:** Engineering analysis, so.
[00:33:08:140 - 00:33:10:609] **Speaker 1:** When the geometry or physics can't be simplified, so if
[00:33:10:609 - 00:33:15:489] **Speaker 1:** we can't just assume it's like a lumped mass or
[00:33:15:489 - 00:33:18:579] **Speaker 1:** a simple sphere or cube, maybe we're trying to model
[00:33:18:579 - 00:33:20:380] **Speaker 1:** a car and we can't just model it as a
[00:33:20:380 - 00:33:23:540] **Speaker 1:** cylinder or some sort of basic geometry to create a
[00:33:23:540 - 00:33:24:560] **Speaker 1:** simple model.
[00:33:25:770 - 00:33:28:160] **Speaker 1:** Or when we need a high level of confidence required.
[00:33:28:479 - 00:33:31:380] **Speaker 1:** So maybe the aerospace example again, we might have uh
[00:33:32:660 - 00:33:34:000] **Speaker 1:** I don't I don't know what what it is, but
[00:33:34:000 - 00:33:38:920] **Speaker 1:** it might be a few percent in terms of accuracy
[00:33:38:920 - 00:33:39:680] **Speaker 1:** that we require.
[00:33:39:949 - 00:33:41:839] **Speaker 1:** Whereas if we're just designing a barrier on the side
[00:33:41:839 - 00:33:45:750] **Speaker 1:** of the road to stop cars from driving off the
[00:33:45:750 - 00:33:48:040] **Speaker 1:** road, maybe we just chuck a factor of safety of
[00:33:48:040 - 00:33:51:439] **Speaker 1:** 2 to 4 or 10 because it's cheap to do.
[00:33:51:640 - 00:33:53:069] **Speaker 1:** So we just overengineering.
[00:33:56:170 - 00:33:59:869] **Speaker 1:** Uh, so physical experiments, maybe the component is too small
[00:33:59:869 - 00:34:00:369] **Speaker 1:** or too big.
[00:34:00:449 - 00:34:03:089] **Speaker 1:** So if you're looking at the nanoscale, uh, or if
[00:34:03:089 - 00:34:06:209] **Speaker 1:** you're looking at very large scale like earthquakes, so earthquakes
[00:34:06:209 - 00:34:08:250] **Speaker 1:** are very large scale, but also large scale in time.
[00:34:08:449 - 00:34:09:750] **Speaker 1:** So not just space.
[00:34:10:408 - 00:34:12:648] **Speaker 1:** And it's hard to sort of just get an earthquake
[00:34:12:648 - 00:34:14:550] **Speaker 1:** to happen on on your schedule.
[00:34:15:128 - 00:34:18:929] **Speaker 1:** So if there's a process, yeah, that you can't can't.
[00:34:19:790 - 00:34:20:770] **Speaker 1:** Experiment with.
[00:34:22:250 - 00:34:24:810] **Speaker 1:** Or for New Zealand, we're sort of we we're against
[00:34:24:810 - 00:34:25:530] **Speaker 1:** nuclear energy.
[00:34:25:648 - 00:34:27:648] **Speaker 1:** So if you want to do some more nuclear testing,
[00:34:27:810 - 00:34:29:770] **Speaker 1:** then you wouldn't be able to do that in the
[00:34:29:770 - 00:34:30:110] **Speaker 1:** lab.
[00:34:31:260 - 00:34:32:040] **Speaker 1:** Very easily.
[00:34:34:729 - 00:34:37:799] **Speaker 1:** So some advantages for numerical models.
[00:34:38:039 - 00:34:38:968] **Speaker 1:** So why bother?
[00:34:39:079 - 00:34:39:958] **Speaker 1:** Why are we doing this?
[00:34:40:398 - 00:34:43:099] **Speaker 1:** So we might want to get some more accurate predictions
[00:34:43:678 - 00:34:44:599] **Speaker 1:** if the physics is correct.
[00:34:44:877 - 00:34:47:468] **Speaker 1:** So we've made some assumptions if we're using Navia Stokes,
[00:34:47:627 - 00:34:48:999] **Speaker 1:** then we hope that that is sufficient.
[00:34:49:860 - 00:34:53:709] **Speaker 1:** Uh, we might want to be able to predict data
[00:34:53:709 - 00:34:54:969] **Speaker 1:** for a range of points.
[00:34:55:469 - 00:34:59:270] **Speaker 1:** So I think at least those in fluid mechanics would
[00:34:59:270 - 00:35:00:669] **Speaker 1:** have done the wind tunnel.
[00:35:00:989 - 00:35:02:189] **Speaker 1:** Have you done wind tunnel test?
[00:35:02:270 - 00:35:02:550] **Speaker 1:** Yeah.
[00:35:02:820 - 00:35:04:649] **Speaker 1:** So you would have looked at maybe those little tufts
[00:35:06:100 - 00:35:06:709] **Speaker 1:** or smoke.
[00:35:06:830 - 00:35:08:750] **Speaker 1:** I don't know if you do the smoke and visualise
[00:35:08:750 - 00:35:09:310] **Speaker 1:** the flow.
[00:35:09:840 - 00:35:13:510] **Speaker 1:** Uh, but if you want to visualise the uh the
[00:35:13:510 - 00:35:18:699] **Speaker 1:** pressure and the streamlines entirely throughout the volume, not just
[00:35:18:699 - 00:35:19:409] **Speaker 1:** a slice.
[00:35:19:800 - 00:35:24:919] **Speaker 1:** or discrete points with those tufts, then you could use
[00:35:24:919 - 00:35:27:560] **Speaker 1:** numerical simulations because that would give you essentially an infinite
[00:35:27:560 - 00:35:28:500] **Speaker 1:** number of senses.
[00:35:31:080 - 00:35:33:080] **Speaker 1:** We might want to have better predictions for for lighter
[00:35:33:080 - 00:35:33:899] **Speaker 1:** components.
[00:35:34:679 - 00:35:36:199] **Speaker 1:** Uh, so maybe an optimisation problem.
[00:35:36:320 - 00:35:37:639] **Speaker 1:** We want to look at a whole bunch of different
[00:35:37:639 - 00:35:38:419] **Speaker 1:** geometries.
[00:35:41:949 - 00:35:47:709] **Speaker 1:** And for example, if we did an experiment and we
[00:35:47:709 - 00:35:50:030] **Speaker 1:** looked at a car and we changed the length by
[00:35:50:030 - 00:35:53:409] **Speaker 1:** 10 mills, and we ended up with 50 cars.
[00:35:53:879 - 00:35:56:030] **Speaker 1:** That's a lot of expense to create all of those
[00:35:56:030 - 00:35:56:570] **Speaker 1:** cars.
[00:35:57:189 - 00:35:59:270] **Speaker 1:** So if you just did it in a simulation, you'd
[00:35:59:270 - 00:36:02:419] **Speaker 1:** adjust that parameter and the parameter sweep, which will cover
[00:36:02:419 - 00:36:05:969] **Speaker 1:** on console, and you get data from all of those
[00:36:07:270 - 00:36:07:629] **Speaker 1:** results.
[00:36:07:830 - 00:36:09:169] **Speaker 1:** So all of those length scales.
[00:36:10:449 - 00:36:12:590] **Speaker 1:** You might choose one that is best and then validate
[00:36:12:590 - 00:36:14:810] **Speaker 1:** that against an experiment, but you don't want to do
[00:36:14:810 - 00:36:16:840] **Speaker 1:** 50 experiments with those cars.
[00:36:18:699 - 00:36:22:179] **Speaker 1:** And I talked about parametric design, more competitive products.
[00:36:22:389 - 00:36:24:439] **Speaker 1:** Yeah, just staying in staying in business.
[00:36:25:060 - 00:36:29:659] **Speaker 1:** So some disadvantages include that new models might not be
[00:36:29:659 - 00:36:33:860] **Speaker 1:** commercially, not available commercially, um.
[00:36:35:350 - 00:36:39:030] **Speaker 1:** So there's a whole bunch of open-source software online.
[00:36:39:310 - 00:36:42:090] **Speaker 1:** Um, I'm not sure how familiar you are with these
[00:36:42:550 - 00:36:47:270] **Speaker 1:** packages, but quite often they Yeah, they are enthusiasts or
[00:36:47:270 - 00:36:48:550] **Speaker 1:** hobbyists that create them.
[00:36:48:629 - 00:36:51:429] **Speaker 1:** So they might not be extensive documentation or tutorials.
[00:36:51:469 - 00:36:53:219] **Speaker 1:** So it might be a little bit hard to learn.
[00:36:53:429 - 00:36:54:770] **Speaker 1:** So the learning curve is a bit higher.
[00:36:55:570 - 00:36:57:649] **Speaker 1:** Um, so they might not be user guides and things
[00:36:57:649 - 00:36:57:949] **Speaker 1:** like that.
[00:36:58:149 - 00:37:01:080] **Speaker 1:** Whereas commercial software like answer and console that we've got
[00:37:01:389 - 00:37:05:750] **Speaker 1:** in the department has extensive tutorials, user guides, all of
[00:37:05:750 - 00:37:05:870] **Speaker 1:** that.
[00:37:05:949 - 00:37:09:310] **Speaker 1:** So they're much easier to get a to get a
[00:37:09:310 - 00:37:09:889] **Speaker 1:** hold of.
[00:37:11:010 - 00:37:12:800] **Speaker 1:** Uh, it's also a graphical user interface, so you just
[00:37:12:800 - 00:37:14:050] **Speaker 1:** click and point, so.
[00:37:18:379 - 00:37:21:159] **Speaker 1:** licencing costs can be significant, just like with Windows.
[00:37:21:310 - 00:37:23:830] **Speaker 1:** Um, I think they give the universities a deal so
[00:37:23:830 - 00:37:24:889] **Speaker 1:** that they get you hooked.
[00:37:25:310 - 00:37:28:090] **Speaker 1:** Um, they do the same for ASIS and console, etc.
[00:37:28:669 - 00:37:30:479] **Speaker 1:** um, but it is still.
[00:37:31:489 - 00:37:34:229] **Speaker 1:** Manageable in the workplace if if that's what you require.
[00:37:36:310 - 00:37:40:090] **Speaker 1:** Um, because they're sort of closed systems or commercial systems,
[00:37:40:300 - 00:37:44:229] **Speaker 1:** uh, we can't see how exactly that they've done everything.
[00:37:44:310 - 00:37:49:350] **Speaker 1:** So we're just trusting that the, uh, models and physics
[00:37:49:350 - 00:37:50:570] **Speaker 1:** work correctly.
[00:37:51:149 - 00:37:54:770] **Speaker 1:** So they have done benchmark cases and tested validated the
[00:37:54:780 - 00:37:58:090] **Speaker 1:** the software, but you are still trusting them.
[00:37:58:629 - 00:38:01:169] **Speaker 1:** So it's sort of, yeah, I guess quite similar to
[00:38:01:169 - 00:38:01:870] **Speaker 1:** the AI models.
[00:38:01:909 - 00:38:03:030] **Speaker 1:** You don't really know what's going on.
[00:38:03:139 - 00:38:05:459] **Speaker 1:** It gives you a result, um.
[00:38:06:370 - 00:38:09:129] **Speaker 1:** So you're trusting that that's correct or hopefully not trusting
[00:38:09:129 - 00:38:10:219] **Speaker 1:** it's correct.
[00:38:10:889 - 00:38:12:310] **Speaker 1:** Training time can be quite large.
[00:38:12:770 - 00:38:17:250] **Speaker 1:** So console I've got like 5 labs that we spend
[00:38:17:250 - 00:38:18:229] **Speaker 1:** on console.
[00:38:18:979 - 00:38:21:120] **Speaker 1:** Maybe it takes an hour or so to go through
[00:38:21:120 - 00:38:21:510] **Speaker 1:** those.
[00:38:22:449 - 00:38:25:810] **Speaker 1:** So it's not too bad to get the basics, uh,
[00:38:26:370 - 00:38:29:090] **Speaker 1:** but it can be quite a lot of overhead if
[00:38:29:090 - 00:38:32:889] **Speaker 1:** you're learning a particular software like Open phone or Basilisk,
[00:38:33:090 - 00:38:34:389] **Speaker 1:** those open-source ones.
[00:38:37:010 - 00:38:38:739] **Speaker 1:** And it's not just a matter of being able to
[00:38:38:739 - 00:38:41:639] **Speaker 1:** know which buttons to click, but having some more intuitive,
[00:38:41:979 - 00:38:46:899] **Speaker 1:** um, Experience that can get correct results.
[00:38:47:139 - 00:38:50:100] **Speaker 1:** So you can always get a result with, with, well,
[00:38:50:260 - 00:38:51:159] **Speaker 1:** no, that's not true.
[00:38:51:580 - 00:38:54:969] **Speaker 1:** You can often get results in the numerical simulations, but
[00:38:54:969 - 00:38:56:199] **Speaker 1:** you need to make sure that they're correct.
[00:38:58:250 - 00:39:00:810] **Speaker 1:** So grid and model generation for complex systems can be
[00:39:00:810 - 00:39:01:699] **Speaker 1:** very extensive.
[00:39:02:290 - 00:39:07:689] **Speaker 1:** So the tsunami model example, they had adaptive, adaptive mesh
[00:39:07:689 - 00:39:08:199] **Speaker 1:** refinement.
[00:39:08:290 - 00:39:09:899] **Speaker 1:** So they're only resolved where they needed to.
[00:39:10:530 - 00:39:12:449] **Speaker 1:** But it still would have taken days or weeks to
[00:39:12:449 - 00:39:14:129] **Speaker 1:** solve for those simulations.
[00:39:14:409 - 00:39:16:250] **Speaker 1:** And that's only in 2D, not 3D.
[00:39:18:899 - 00:39:21:159] **Speaker 1:** Uh, so we got 10.
[00:39:22:810 - 00:39:23:429] **Speaker 1:** 10 minutes.
[00:39:24:179 - 00:39:27:389] **Speaker 1:** Um, so I wanted to go through like a survey
[00:39:27:389 - 00:39:29:959] **Speaker 1:** of Yeah, maybe a survey.
[00:39:35:159 - 00:39:37:280] **Speaker 1:** I'll briefly flick through this because it's a bit dry.
[00:39:37:500 - 00:39:39:280] **Speaker 1:** Um, so numerical simulation.
[00:39:41:300 - 00:39:43:219] **Speaker 1:** Wasn't really around prior to 1960s.
[00:39:43:580 - 00:39:47:000] **Speaker 1:** So it's reasonably new in some, in some regards.
[00:39:47:979 - 00:39:51:260] **Speaker 1:** And initially started out with sort of the defence, um,
[00:39:51:459 - 00:39:54:260] **Speaker 1:** which is always a way of getting money to develop
[00:39:54:260 - 00:39:55:080] **Speaker 1:** technologies.
[00:39:55:260 - 00:39:58:800] **Speaker 1:** Um, just that's, that's just how it is.
[00:39:59:100 - 00:40:01:000] **Speaker 1:** Um, so it is.
[00:40:01:760 - 00:40:05:909] **Speaker 1:** Often used now across the board, uh, so they'll use
[00:40:05:909 - 00:40:09:189] **Speaker 1:** it, I guess for fluid mechanics, we've got Hamilton jet
[00:40:09:189 - 00:40:12:340] **Speaker 1:** down the road, um, so they'll use CFD for, for
[00:40:12:340 - 00:40:17:129] **Speaker 1:** analysing the, the jets, um, and then all the aerospace
[00:40:17:199 - 00:40:20:850] **Speaker 1:** and then biomed they'll be using it, um, when you're
[00:40:20:850 - 00:40:22:929] **Speaker 1:** looking at designing products.
[00:40:24:070 - 00:40:26:709] **Speaker 1:** So I guess, yeah, fish and Paiu, etc.
[00:40:29:479 - 00:40:32:300] **Speaker 1:** So there's been a lot of advances since the 1960s
[00:40:32:520 - 00:40:36:350] **Speaker 1:** uh for both hardware, so how quick those chips work,
[00:40:36:479 - 00:40:38:679] **Speaker 1:** CPU GPUs, as well as the software.
[00:40:38:719 - 00:40:41:060] **Speaker 1:** So the algorithms that we're going to introduce.
[00:40:41:729 - 00:40:43:399] **Speaker 1:** So here's a plot just sort of showing with a
[00:40:43:399 - 00:40:47:360] **Speaker 1:** log scale and the vertical that the algorithms that uh
[00:40:47:689 - 00:40:50:459] **Speaker 1:** sort of developed a sort of, I don't know, maybe
[00:40:51:030 - 00:40:53:320] **Speaker 1:** um flattening out a little bit, uh but they have
[00:40:53:320 - 00:40:56:790] **Speaker 1:** jumped orders of magnitude since the early days and computers
[00:40:56:790 - 00:40:59:820] **Speaker 1:** have also stepped it up in terms of processing.
[00:41:09:209 - 00:41:11:929] **Speaker 1:** I'll start this on Wednesday and I'll just go through
[00:41:11:929 - 00:41:15:070] **Speaker 1:** a survey just to keep everyone awake.
[00:41:17:580 - 00:41:19:139] **Speaker 0:** I'll just disconnect.
[00:41:41:000 - 00:41:42:699] **Speaker 1:** Uh, it's not right.
[00:42:03:820 - 00:42:04:739] **Speaker 1:** OK, I don't know.
[00:42:04:820 - 00:42:05:489] **Speaker 1:** Hopefully this works.
[00:42:05:540 - 00:42:06:439] **Speaker 1:** I sort of only just.
[00:42:11:760 - 00:42:14:139] **Speaker 1:** Uh, copied it from last year and added some, but,
[00:42:14:719 - 00:42:15:870] **Speaker 1:** um, hopefully it's open actually.
[00:42:17:199 - 00:42:19:310] **Speaker 1:** If you, yeah, if you just scan that QR code.
[00:42:23:600 - 00:42:25:060] **Speaker 1:** Maybe I'll check it works as well.
[00:42:30:679 - 00:42:31:439] **Speaker 1:** Oh jeez.
[00:42:32:520 - 00:42:34:300] **Speaker 1:** Um, one minute.
[00:42:35:889 - 00:42:38:479] **Speaker 1:** This is what happens if you leave it to the
[00:42:38:479 - 00:42:39:830] **Speaker 1:** day of, um.
[00:42:49:000 - 00:42:50:870] **Speaker 1:** Uh, just talk to your neighbour if you haven't met
[00:42:50:870 - 00:42:54:409] **Speaker 1:** them before, um, yeah, for a couple of minutes.
[00:43:06:840 - 00:43:06:850] **Speaker 0:** no.
[00:43:08:209 - 00:43:09:129] **Speaker 1:** OK, that's not gonna work.
[00:43:09:250 - 00:43:12:330] **Speaker 1:** That's uh, I'm not gonna, I'm not gonna wait for
[00:43:12:330 - 00:43:12:449] **Speaker 1:** that.
[00:43:12:689 - 00:43:14:030] **Speaker 1:** So, um.
[00:43:17:530 - 00:43:18:100] **Speaker 1:** OK.
[00:43:21:929 - 00:43:24:129] **Speaker 1:** Obviously, the Wi Fi is slow, it's not connecting so
[00:43:24:129 - 00:43:25:330] **Speaker 1:** I can't edit the form.
[00:43:25:729 - 00:43:27:610] **Speaker 1:** Um, all right, so we can do that Wednesday.
[00:43:27:729 - 00:43:28:590] **Speaker 1:** It's not a big deal.
[00:43:31:000 - 00:43:32:280] **Speaker 1:** All right, we can continue on.
[00:43:32:439 - 00:43:35:320] **Speaker 1:** All right, so, um, hopefully you've met their at least
[00:43:35:320 - 00:43:36:189] **Speaker 1:** know their name now.
[00:43:37:120 - 00:43:42:530] **Speaker 1:** Um, so, A bit of an overview of numerical simulations.
[00:43:42:939 - 00:43:45:350] **Speaker 1:** So we start in the top left and we're gonna
[00:43:45:350 - 00:43:47:070] **Speaker 1:** go all the way around and end up at the
[00:43:47:070 - 00:43:47:669] **Speaker 1:** top right.
[00:43:49:139 - 00:43:50:689] **Speaker 1:** So I'll try and make, I don't know, it's not
[00:43:50:689 - 00:43:51:439] **Speaker 1:** full screen.
[00:43:57:139 - 00:43:57:879] **Speaker 1:** Full screen mode.
[00:43:58:580 - 00:44:02:500] **Speaker 1:** Uh, so we start with some real problem with complex
[00:44:02:500 - 00:44:04:459] **Speaker 1:** physics and complex geometry.
[00:44:05:629 - 00:44:07:590] **Speaker 1:** So the example I'd like to give is if we're
[00:44:07:590 - 00:44:11:409] **Speaker 1:** looking at the um, HVAC of this room.
[00:44:11:879 - 00:44:15:919] **Speaker 1:** We've got A room that's not just a rectangle.
[00:44:16:050 - 00:44:17:290] **Speaker 1:** That's sort of got tiered seating.
[00:44:17:649 - 00:44:19:370] **Speaker 1:** You've got quite intricate details.
[00:44:19:489 - 00:44:21:790] **Speaker 1:** I guess that's the sound on the on the sides.
[00:44:22:209 - 00:44:24:530] **Speaker 1:** And then you've got lots of stuff up there.
[00:44:24:889 - 00:44:27:729] **Speaker 1:** So you can't just approximate as a box if you
[00:44:27:729 - 00:44:29:459] **Speaker 1:** want it to be absolutely correct.
[00:44:31:080 - 00:44:32:399] **Speaker 1:** There's quite a lot of complex physics.
[00:44:32:520 - 00:44:35:169] **Speaker 1:** Every single person in this room is giving off heat.
[00:44:35:679 - 00:44:37:729] **Speaker 1:** So it's changing that the temperature locally.
[00:44:38:840 - 00:44:40:300] **Speaker 1:** You'll have fans.
[00:44:41:550 - 00:44:43:840] **Speaker 1:** I must have HVAC going, I guess, or air conditioning
[00:44:43:840 - 00:44:44:540] **Speaker 1:** going in here.
[00:44:45:360 - 00:44:47:919] **Speaker 1:** So we've got that as as a source.
[00:44:48:280 - 00:44:50:199] **Speaker 1:** So source for heat or cool.
[00:44:52:459 - 00:44:54:689] **Speaker 1:** And yeah, so physics, so fluid flow.
[00:44:54:860 - 00:44:58:479] **Speaker 1:** So natural convection, maybe there's some air flowing as well.
[00:44:58:739 - 00:44:59:739] **Speaker 1:** And then that temperature.
[00:44:59:899 - 00:45:02:520] **Speaker 1:** So we've got temperature and fluid flow being the main
[00:45:02:979 - 00:45:03:750] **Speaker 1:** dependent variables.
[00:45:04:179 - 00:45:07:090] **Speaker 1:** So identifying the central physics and central geometry, we might
[00:45:07:090 - 00:45:10:820] **Speaker 1:** want to approximate this as sort of a polygon, just
[00:45:10:820 - 00:45:13:219] **Speaker 1:** as a straight line for all the tiered seating and
[00:45:13:219 - 00:45:14:080] **Speaker 1:** then flat top.
[00:45:15:399 - 00:45:18:639] **Speaker 1:** And the temperature we might sort of approximate.
[00:45:19:689 - 00:45:23:770] **Speaker 1:** The tiered seating as a heat flux or some sort
[00:45:23:770 - 00:45:28:750] **Speaker 1:** of um heat source rather than multiple individual bodies.
[00:45:29:929 - 00:45:33:360] **Speaker 1:** We're gonna define a simplified, uh, mathematical model with a
[00:45:33:360 - 00:45:34:429] **Speaker 1:** simplified geometry.
[00:45:35:479 - 00:45:39:280] **Speaker 1:** Um, that's what I've discussed, and then we wanna decide
[00:45:39:280 - 00:45:41:679] **Speaker 1:** how to discretize this equation, so.
[00:45:43:969 - 00:45:45:750] **Speaker 1:** We can discretize it with a whole bunch of different
[00:45:45:750 - 00:45:46:510] **Speaker 1:** techniques.
[00:45:47:010 - 00:45:49:389] **Speaker 1:** We're going to talk about finite elements, a little bit
[00:45:49:389 - 00:45:51:189] **Speaker 1:** about finite volume and infinite difference.
[00:45:52:209 - 00:45:53:469] **Speaker 1:** So discretizing the problem.
[00:45:54:659 - 00:45:56:699] **Speaker 1:** Now we've got a system of equations.
[00:45:56:979 - 00:45:59:739] **Speaker 1:** So maths, linear algebra, we solve.
[00:45:59:979 - 00:46:01:399] **Speaker 1:** So that's the compute stage.
[00:46:01:979 - 00:46:04:030] **Speaker 1:** And then we're going to check whether or not our
[00:46:04:030 - 00:46:05:159] **Speaker 1:** solution makes sense.
[00:46:05:820 - 00:46:09:820] **Speaker 1:** So have we actually solved that set of linear algebra
[00:46:10:060 - 00:46:10:580] **Speaker 1:** equation?
[00:46:12:379 - 00:46:14:199] **Speaker 1:** So that's checking for convergence.
[00:46:15:060 - 00:46:19:360] **Speaker 1:** We also want to verify using some non-benchmark solutions.
[00:46:20:060 - 00:46:22:580] **Speaker 1:** So if we've got a a simple model, maybe a
[00:46:22:580 - 00:46:26:399] **Speaker 1:** cube or a rectangle, uh we can validate against existing
[00:46:26:540 - 00:46:27:800] **Speaker 1:** uh results.
[00:46:29:370 - 00:46:31:080] **Speaker 1:** So that's the verification step.
[00:46:31:500 - 00:46:36:060] **Speaker 1:** We then want to postprocess and visualise the results and
[00:46:36:060 - 00:46:38:540] **Speaker 1:** determine whether or not it's a good approximation for our
[00:46:38:540 - 00:46:39:320] **Speaker 1:** real problem.
[00:46:40:020 - 00:46:43:899] **Speaker 1:** So I guess we could validate that with a temperature
[00:46:43:899 - 00:46:46:419] **Speaker 1:** probe in the room or a few of those scattered
[00:46:46:419 - 00:46:46:879] **Speaker 1:** around.
[00:46:47:409 - 00:46:48:340] **Speaker 1:** It's a time-dependent problem.
[00:46:48:419 - 00:46:49:719] **Speaker 1:** So we'd be looking at over time.
[00:46:51:179 - 00:46:54:649] **Speaker 1:** And that's that validation against measured data.
[00:46:55:219 - 00:46:59:739] **Speaker 1:** So yeah, there's key difference between validation and verification.
[00:47:00:050 - 00:47:04:199] **Speaker 1:** Verification is just checking that our equations actually working correctly,
[00:47:04:570 - 00:47:05:560] **Speaker 1:** that they're converging.
[00:47:06:419 - 00:47:08:570] **Speaker 1:** Maybe we're checking out some simplified data.
[00:47:08:780 - 00:47:11:780] **Speaker 1:** Validation is when we take a step back and look
[00:47:11:780 - 00:47:16:060] **Speaker 1:** at making sure that our model accurately represents the real
[00:47:16:060 - 00:47:16:840] **Speaker 1:** physics.
[00:47:20:120 - 00:47:21:780] **Speaker 1:** Yeah, I think that's pretty good timing.
[00:47:22:199 - 00:47:23:500] **Speaker 1:** Any, any questions?
[00:47:27:149 - 00:47:27:899] **Speaker 1:** Alright, cool.
[00:47:28:399 - 00:47:30:199] **Speaker 1:** We'll see you on Wednesday.
[00:48:01:399 - 00:48:12:969] **Speaker 0:** No it's That's.
[00:48:23:280 - 00:48:23:689] **Speaker 0:** structure.
[00:48:29:370 - 00:48:29:409] **Speaker 0:** You just.
[00:48:50:550 - 00:48:50:560] **Speaker 0:** so.
[00:48:52:169 - 00:48:52:179] **Speaker 0:** Yes.
[00:48:54:100 - 00:48:54:110] **Speaker 0:** I.
[00:48:59:520 - 00:49:11:439] **Speaker 0:** And OK.
[00:49:15:580 - 00:49:27:709] **Speaker 0:** I So What.
[00:49:28:669 - 00:49:36:560] **Speaker 0:** Just I, I I went, I went to a bundle.
[00:49:42:350 - 00:49:42:370] **Speaker 0:** You guys.
[00:49:48:310 - 00:49:49:520] **Speaker 0:** Can you go climbing the floor.

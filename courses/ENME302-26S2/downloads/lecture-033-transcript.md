# ENME302-26S2 Lecture 33 native Echo transcript

Date: September 21, 2026 12:00pm-12:55pm
Transcript type: native Echo automated transcript.

[00:00:00:449 - 00:00:04:369] **Speaker 0:** I'm just, yeah.
[00:00:11:189 - 00:00:11:920] **Speaker 0:** It's probably um.
[00:00:21:489 - 00:00:45:049] **Speaker 0:** I And Yeah.
[00:00:56:880 - 00:00:57:860] **Speaker 1:** Cool, uh, good afternoon.
[00:00:58:279 - 00:00:59:500] **Speaker 1:** Is the mic OK?
[00:01:00:159 - 00:01:00:740] **Speaker 1:** It's alright.
[00:01:01:520 - 00:01:02:159] **Speaker 1:** Cool, alright.
[00:01:03:709 - 00:01:07:709] **Speaker 1:** So today we're gonna go through uh quiz 3, just
[00:01:07:709 - 00:01:08:730] **Speaker 1:** as a bit of a recap.
[00:01:11:269 - 00:01:12:319] **Speaker 1:** So I'll try and share.
[00:01:21:440 - 00:01:21:870] **Speaker 1:** Yeah.
[00:01:22:809 - 00:01:27:529] **Speaker 1:** Um, So 79%.
[00:01:28:050 - 00:01:30:110] **Speaker 1:** Question one was the one on coding.
[00:01:30:730 - 00:01:34:010] **Speaker 1:** And then question two and three were on console questions.
[00:01:34:089 - 00:01:37:129] **Speaker 1:** So we'll just go through the model solutions as usual.
[00:01:39:779 - 00:01:41:360] **Speaker 1:** So, question one.
[00:01:43:150 - 00:01:44:629] **Speaker 1:** was looking at the Laplace equation.
[00:01:44:809 - 00:01:47:040] **Speaker 1:** So this is based on chapter 4, mostly.
[00:01:47:510 - 00:01:52:110] **Speaker 1:** And we looked at applying the finite difference with the
[00:01:52:110 - 00:01:55:230] **Speaker 1:** Leapen method and then using over relaxation as well to
[00:01:55:230 - 00:01:57:209] **Speaker 1:** sort of hurry up the convergence rate.
[00:01:58:169 - 00:02:00:620] **Speaker 1:** And we went to some tolerance of 0.1%. So here
[00:02:00:620 - 00:02:03:540] **Speaker 1:** we've got four Derrick clay boundary conditions around our uh
[00:02:03:540 - 00:02:03:900] **Speaker 1:** domain.
[00:02:04:599 - 00:02:07:650] **Speaker 1:** Uh, the X domain extends across 1 and then Y
[00:02:07:650 - 00:02:09:779] **Speaker 1:** across 4, so it's a rectangular domain.
[00:02:10:520 - 00:02:16:500] **Speaker 1:** Uh, you've been given some sign functions for the left
[00:02:16:500 - 00:02:17:820] **Speaker 1:** and right-hand boundaries.
[00:02:19:910 - 00:02:26:660] **Speaker 1:** And This is based on our chapter 4 example.
[00:02:27:320 - 00:02:29:020] **Speaker 1:** So this is what we did in class.
[00:02:29:610 - 00:02:32:520] **Speaker 1:** And we showed that we set up our grid, computational
[00:02:32:520 - 00:02:32:820] **Speaker 1:** grid.
[00:02:33:000 - 00:02:35:470] **Speaker 1:** We set the boundary conditions and then apply our Liebman
[00:02:35:470 - 00:02:35:899] **Speaker 1:** method.
[00:02:36:240 - 00:02:39:369] **Speaker 1:** I'm not sure why that's Here we go.
[00:02:39:910 - 00:02:42:000] **Speaker 1:** And we've got our while loop, so you might wanna
[00:02:42:000 - 00:02:43:889] **Speaker 1:** use a for loop instead, doesn't matter too much.
[00:02:45:149 - 00:02:45:949] **Speaker 1:** And then some plotting.
[00:02:46:100 - 00:02:48:110] **Speaker 1:** So for this quiz, we're just looking at the number
[00:02:48:110 - 00:02:50:330] **Speaker 1:** of iterations required to reach that tolerance.
[00:02:50:809 - 00:02:52:250] **Speaker 1:** So I've prepared the quiz.
[00:02:55:279 - 00:02:56:339] **Speaker 1:** 3 A.
[00:02:58:059 - 00:03:02:570] **Speaker 1:** Um, So this one is.
[00:03:03:710 - 00:03:07:949] **Speaker 1:** Setting up a coefficient for the sign boundary conditions, 3.6
[00:03:07:949 - 00:03:10:250] **Speaker 1:** in this case, so maybe we apply it to our.
[00:03:12:199 - 00:03:12:789] **Speaker 1:** Christian.
[00:03:14:970 - 00:03:17:500] **Speaker 1:** So here we've got 2.4, so we can adjust that.
[00:03:18:529 - 00:03:19:270] **Speaker 1:** Coefficient.
[00:03:19:649 - 00:03:23:630] **Speaker 1:** Uh, we've got a domain that varies 1 in X
[00:03:24:289 - 00:03:26:009] **Speaker 1:** and 4 in Y.
[00:03:27:710 - 00:03:31:380] **Speaker 1:** The X and Y coordinates evaluated.
[00:03:31:619 - 00:03:33:020] **Speaker 1:** We need DX and DY.
[00:03:33:460 - 00:03:36:679] **Speaker 1:** So the key difference for this equation, this question rather,
[00:03:37:259 - 00:03:39:619] **Speaker 1:** compared to our example in chapter 4, was that we've
[00:03:39:619 - 00:03:41:149] **Speaker 1:** got a non-uniform grid spacing.
[00:03:41:990 - 00:03:44:860] **Speaker 1:** So the non-uniform grid spacing instead of having over X
[00:03:44:860 - 00:03:47:309] **Speaker 1:** 2 cancelling with the Y 2s, we have to keep
[00:03:47:309 - 00:03:47:889] **Speaker 1:** track of them.
[00:03:48:190 - 00:03:50:110] **Speaker 1:** And that's what we've got in this, this line of
[00:03:50:110 - 00:03:52:009] **Speaker 1:** code down here.
[00:03:52:350 - 00:03:54:470] **Speaker 1:** So it's a little bit longer, uh, but it's the
[00:03:54:470 - 00:03:55:850] **Speaker 1:** same, same sort of form.
[00:03:57:850 - 00:04:00:429] **Speaker 1:** I've applied the boundary conditions without a for loop.
[00:04:00:850 - 00:04:06:070] **Speaker 1:** So you can Evaluate the whole dimension.
[00:04:06:389 - 00:04:11:580] **Speaker 1:** So every single coordinate and and Y at X equals
[00:04:11:580 - 00:04:13:630] **Speaker 1:** 0 and then at X equal to L.
[00:04:14:490 - 00:04:19:088] **Speaker 1:** Using the -1 and the 0 indices and the bottom
[00:04:19:088 - 00:04:22:079] **Speaker 1:** and top are set with these uh scalar values.
[00:04:22:369 - 00:04:25:510] **Speaker 1:** So that's why I've evaluated the Y array up here
[00:04:25:929 - 00:04:27:480] **Speaker 1:** and then inserted that into our expression.
[00:04:27:570 - 00:04:31:049] **Speaker 1:** So taking numberpi.s sign, taking of an array and it
[00:04:31:049 - 00:04:31:869] **Speaker 1:** returns an array.
[00:04:33:660 - 00:04:36:200] **Speaker 1:** Uh, the wildlife is much the same as earlier.
[00:04:38:140 - 00:04:41:779] **Speaker 1:** And That's, that's pretty much it.
[00:04:42:359 - 00:04:43:989] **Speaker 1:** So I don't know if it'll work or not, but
[00:04:43:989 - 00:04:44:839] **Speaker 1:** we'll give it a go.
[00:04:47:200 - 00:04:53:350] **Speaker 1:** Maybe precheck Oh, this is dangerous, um.
[00:04:56:510 - 00:04:57:700] **Speaker 1:** Maybe I've done something wrong.
[00:04:58:160 - 00:04:59:339] **Speaker 1:** So 6.5.
[00:05:07:179 - 00:05:10:799] **Speaker 1:** So we've got, this is 4.5 instead of 6.5.
[00:05:14:059 - 00:05:15:839] **Speaker 1:** Live coding is always good fun.
[00:05:17:399 - 00:05:19:339] **Speaker 1:** Maybe it'll work, yep, alright, good enough.
[00:05:20:320 - 00:05:21:929] **Speaker 1:** So obviously you have more time to go in detail
[00:05:21:929 - 00:05:25:029] **Speaker 1:** in your, in your quizzes, but this is the worked
[00:05:25:029 - 00:05:25:390] **Speaker 1:** solution.
[00:05:26:320 - 00:05:28:320] **Speaker 1:** So the key difference here is again, that we've got
[00:05:28:320 - 00:05:30:640] **Speaker 1:** these DX's and DY terms that we're including in our
[00:05:30:640 - 00:05:33:040] **Speaker 1:** code rather than just having them equal to the same
[00:05:33:040 - 00:05:33:480] **Speaker 1:** value.
[00:05:34:519 - 00:05:38:160] **Speaker 1:** Any questions on approaching this type of coding problem?
[00:05:42:100 - 00:05:42:459] **Speaker 1:** No.
[00:05:44:119 - 00:05:44:559] **Speaker 1:** All right.
[00:05:46:679 - 00:05:48:450] **Speaker 1:** As I say, it was done reasonably well within the
[00:05:48:450 - 00:05:49:709] **Speaker 1:** class, so that's, that's good.
[00:05:50:709 - 00:05:54:869] **Speaker 1:** Uh, second question is looking at the, the classic beam
[00:05:54:869 - 00:05:55:329] **Speaker 1:** problem.
[00:05:56:579 - 00:05:59:500] **Speaker 1:** So this one continued on from what we did in
[00:05:59:500 - 00:06:00:130] **Speaker 1:** lab 3.
[00:06:00:380 - 00:06:02:799] **Speaker 1:** So I just want to briefly go over the results
[00:06:02:980 - 00:06:04:739] **Speaker 1:** of, of this.
[00:06:06:529 - 00:06:07:589] **Speaker 1:** So lab 3.
[00:06:10:089 - 00:06:12:079] **Speaker 1:** And this is where you looked at refining the mesh
[00:06:12:079 - 00:06:12:679] **Speaker 1:** resolution.
[00:06:18:529 - 00:06:20:730] **Speaker 1:** And we can try and flick between the two with
[00:06:20:730 - 00:06:21:540] **Speaker 1:** our single screen.
[00:06:23:100 - 00:06:23:440] **Speaker 1:** Yeah.
[00:06:23:940 - 00:06:25:420] **Speaker 1:** Um, so we've got a coarse mesh and then we
[00:06:25:420 - 00:06:26:160] **Speaker 1:** refine the mesh.
[00:06:26:380 - 00:06:29:660] **Speaker 1:** So that was the discretization of our computational domain.
[00:06:29:940 - 00:06:31:670] **Speaker 1:** We also looked at discretization order.
[00:06:31:739 - 00:06:34:350] **Speaker 1:** So element orders, linear quadratic cubic.
[00:06:34:820 - 00:06:37:679] **Speaker 1:** So I've got two different parameters that we're varying.
[00:06:40:799 - 00:06:42:239] **Speaker 1:** And I'm just showing the results here.
[00:06:42:600 - 00:06:45:179] **Speaker 1:** So we're looking at the first principal stress, Gauss point,
[00:06:45:760 - 00:06:48:480] **Speaker 1:** and I varied it with linear and on the x-axis,
[00:06:48:519 - 00:06:49:899] **Speaker 1:** we've got the number of degrees of freedom.
[00:06:50:519 - 00:06:53:380] **Speaker 1:** So linear elements only have two degrees of freedom.
[00:06:53:600 - 00:06:56:500] **Speaker 1:** Uh, the quadratic had 3 and cubic head 4.
[00:06:56:880 - 00:06:58:320] **Speaker 1:** So you can see that you've got more degrees of
[00:06:58:320 - 00:07:01:100] **Speaker 1:** freedom for the higher-order elements, as you might expect.
[00:07:01:679 - 00:07:07:239] **Speaker 1:** We see that the linear curve converges to that 75.2
[00:07:07:239 - 00:07:08:200] **Speaker 1:** megapascales.
[00:07:08:880 - 00:07:12:760] **Speaker 1:** Um, with, with, it requires more degrees of freedom to
[00:07:12:760 - 00:07:14:880] **Speaker 1:** achieve the same order of accuracy as the other two
[00:07:14:880 - 00:07:16:799] **Speaker 1:** schemes, and you can see that the cubic is very
[00:07:16:799 - 00:07:17:399] **Speaker 1:** accurate.
[00:07:18:320 - 00:07:20:790] **Speaker 1:** Um, compared to the other two.
[00:07:22:059 - 00:07:23:899] **Speaker 1:** So that's just one way of representing your results.
[00:07:23:940 - 00:07:26:019] **Speaker 1:** You could also export the data and put it in
[00:07:26:019 - 00:07:29:160] **Speaker 1:** Excel or Python or wherever else you're most familiar with.
[00:07:29:779 - 00:07:32:579] **Speaker 1:** But in this case, what I've done is created solution
[00:07:32:579 - 00:07:33:160] **Speaker 1:** copies.
[00:07:33:940 - 00:07:36:540] **Speaker 1:** So when you solve your parametric solutions, you can right
[00:07:36:540 - 00:07:39:820] **Speaker 1:** click solution copy and it just saves that data within
[00:07:39:820 - 00:07:40:720] **Speaker 1:** your console model.
[00:07:40:899 - 00:07:42:040] **Speaker 1:** So you can refer back to it.
[00:07:42:279 - 00:07:45:140] **Speaker 1:** And under each of these I've labelled from the data
[00:07:45:140 - 00:07:47:600] **Speaker 1:** set that corresponds to that set of parametric solutions.
[00:07:50:190 - 00:07:52:100] **Speaker 1:** So it can be quite complicated otherwise if you save
[00:07:52:100 - 00:07:54:980] **Speaker 1:** multiple models and multiple data sets, it's tidier if you
[00:07:54:980 - 00:07:58:290] **Speaker 1:** just keep your uh solutions and uh solver configurations.
[00:08:01:570 - 00:08:04:929] **Speaker 1:** So, out of the ones that got this question wrong,
[00:08:05:049 - 00:08:08:070] **Speaker 1:** quite a few had 75.2 megapascales, so they must have
[00:08:08:290 - 00:08:10:619] **Speaker 1:** kept the result from this, the lab.
[00:08:11:600 - 00:08:12:829] **Speaker 1:** Um, inadvertently.
[00:08:13:279 - 00:08:16:940] **Speaker 1:** So, in this case, we've been asked to.
[00:08:19:380 - 00:08:21:970] **Speaker 1:** Change the Young's modulus to 190 gigappas scales.
[00:08:23:380 - 00:08:26:980] **Speaker 1:** So under the material properties we can adjust E to
[00:08:26:980 - 00:08:27:820] **Speaker 1:** be 190.
[00:08:29:209 - 00:08:31:170] **Speaker 1:** Again, gigapascales is important.
[00:08:31:230 - 00:08:32:739] **Speaker 1:** It's 10 to 9 pascales.
[00:08:33:210 - 00:08:35:380] **Speaker 1:** Um, I know there were some that were out by
[00:08:35:380 - 00:08:37:080] **Speaker 1:** orders of magnitude, so maybe you had a different Young's
[00:08:37:080 - 00:08:38:280] **Speaker 1:** modular supplied.
[00:08:40:820 - 00:08:43:469] **Speaker 1:** Uh, we've got a boundary force being applied of 150
[00:08:43:469 - 00:08:44:679] **Speaker 1:** kilonewtons down.
[00:08:45:859 - 00:08:48:700] **Speaker 1:** So we're gonna apply that to our boundary condition.
[00:08:49:869 - 00:08:57:650] **Speaker 1:** Boundary load So change that to a total force of
[00:08:57:650 - 00:09:00:010] **Speaker 1:** minus 150 kilonewtons.
[00:09:01:210 - 00:09:04:049] **Speaker 1:** So it's helpful to write the units next to the
[00:09:04:059 - 00:09:07:929] **Speaker 1:** the value that is associated with and killer will be
[00:09:07:929 - 00:09:09:510] **Speaker 1:** timing it by 103.
[00:09:10:109 - 00:09:13:169] **Speaker 1:** And we've got a sign of i times X over
[00:09:13:169 - 00:09:14:619] **Speaker 1:** L which was 1 metre.
[00:09:16:640 - 00:09:19:890] **Speaker 1:** So we've adjusted the boundary condition and we've adjusted the
[00:09:19:890 - 00:09:20:609] **Speaker 1:** material properties.
[00:09:20:809 - 00:09:22:849] **Speaker 1:** So we've essentially changed what equations that we're solving.
[00:09:22:890 - 00:09:23:750] **Speaker 1:** So we have to compute.
[00:09:25:320 - 00:09:26:679] **Speaker 1:** The the solution again.
[00:09:28:780 - 00:09:30:419] **Speaker 1:** So if you went straight to the results, it wouldn't
[00:09:30:419 - 00:09:32:809] **Speaker 1:** have updated that system of equations and you'd be plotting
[00:09:32:809 - 00:09:35:780] **Speaker 1:** the results from your last calculation, which I suspect maybe
[00:09:35:780 - 00:09:39:440] **Speaker 1:** some of you had done when you recorded the 75.2
[00:09:39:619 - 00:09:40:320] **Speaker 1:** megapasca.
[00:09:41:969 - 00:09:43:909] **Speaker 1:** So we'll go under derive values.
[00:09:46:940 - 00:09:49:520] **Speaker 1:** Point evaluation still at that point B at the bottom.
[00:09:50:140 - 00:09:53:359] **Speaker 1:** And just for good measure, we'll create a new table.
[00:09:54:359 - 00:09:57:559] **Speaker 1:** And we can see here that it's converging to 228.9.
[00:09:57:760 - 00:09:59:900] **Speaker 1:** I've left it on the linear elements in this case.
[00:10:00:479 - 00:10:01:679] **Speaker 1:** Uh, so you can see it takes a little bit
[00:10:01:679 - 00:10:04:039] **Speaker 1:** of time to converge, uh, but it's converging to that
[00:10:04:039 - 00:10:04:679] **Speaker 1:** 228.
[00:10:04:840 - 00:10:07:419] **Speaker 1:** So maybe 229 to 3 significant figures.
[00:10:08:719 - 00:10:16:130] **Speaker 1:** Um And again, the formatting for the the quiz uh
[00:10:16:130 - 00:10:20:309] **Speaker 1:** stack questions is multiplied by the units, which is different
[00:10:20:309 - 00:10:22:280] **Speaker 1:** to mega times pascals.
[00:10:22:859 - 00:10:24:799] **Speaker 1:** Uh, mega pascal is 10 to 6 pascals.
[00:10:24:969 - 00:10:28:489] **Speaker 1:** You can also write it as 106 and just get
[00:10:28:489 - 00:10:29:090] **Speaker 1:** rid of that.
[00:10:33:460 - 00:10:35:099] **Speaker 1:** Alright, so that's happy.
[00:10:36:020 - 00:10:40:750] **Speaker 1:** Any questions on this console problem?
[00:10:43:320 - 00:10:44:890] **Speaker 1:** There are a few others that I couldn't work out
[00:10:44:890 - 00:10:47:530] **Speaker 1:** how you got to the answers that you got, but
[00:10:48:799 - 00:10:52:859] **Speaker 1:** it might have been the material properties or The mesh
[00:10:52:859 - 00:10:53:409] **Speaker 1:** resolution.
[00:10:53:750 - 00:10:55:669] **Speaker 1:** So if you use the really coarse mesh, you'd get
[00:10:55:669 - 00:10:58:549] **Speaker 1:** quite a different result for those linear shape elements.
[00:10:58:750 - 00:11:01:229] **Speaker 1:** So that's what we saw here, 150 versus 230.
[00:11:02:590 - 00:11:05:109] **Speaker 1:** So the aim of this lab and this quiz question
[00:11:05:109 - 00:11:07:190] **Speaker 1:** was really just getting a bit of a masterclass on
[00:11:07:190 - 00:11:09:869] **Speaker 1:** mesh convergence and using those different discretization schemes.
[00:11:11:479 - 00:11:12:770] **Speaker 1:** Hopefully convince you somewhat.
[00:11:14:159 - 00:11:16:950] **Speaker 1:** And the last question that we looked at last week
[00:11:17:130 - 00:11:18:130] **Speaker 1:** was.
[00:11:20:309 - 00:11:22:830] **Speaker 1:** Um, looking at this domain, so we've got a circular
[00:11:22:830 - 00:11:26:000] **Speaker 1:** domain, and perhaps it represents some sort of membrane.
[00:11:26:210 - 00:11:28:929] **Speaker 1:** Uh, we've set the displacement of the circumference to be
[00:11:29:150 - 00:11:31:630] **Speaker 1:** the equal to the Y coordinate, and we've applied some
[00:11:31:630 - 00:11:33:250] **Speaker 1:** force underneath, so maybe some pressure.
[00:11:34:570 - 00:11:37:130] **Speaker 1:** So I'll just quickly go through uh this as an
[00:11:37:130 - 00:11:37:650] **Speaker 1:** example.
[00:11:39:030 - 00:11:41:169] **Speaker 1:** So if we create a new.
[00:11:42:760 - 00:11:44:929] **Speaker 1:** Model And Tootie.
[00:11:46:859 - 00:11:51:380] **Speaker 1:** And We're told that this is the Laplace equation, so
[00:11:51:380 - 00:11:52:280] **Speaker 1:** we can use this.
[00:11:54:520 - 00:11:58:830] **Speaker 1:** And we're We, we can't make that smaller, which is
[00:11:58:830 - 00:12:00:000] **Speaker 1:** a pain, but.
[00:12:01:580 - 00:12:01:619] **Speaker 1:** There we go.
[00:12:02:679 - 00:12:05:789] **Speaker 1:** Um, so the dependent variable here is still a displacement
[00:12:05:789 - 00:12:07:299] **Speaker 1:** field, so we can leave it as you.
[00:12:07:840 - 00:12:10:880] **Speaker 1:** Uh, the unit for the displacement is gonna be in
[00:12:10:880 - 00:12:11:239] **Speaker 1:** metres.
[00:12:11:359 - 00:12:12:530] **Speaker 1:** That's the SI units.
[00:12:12:799 - 00:12:15:419] **Speaker 1:** So we can put that as displacement metres.
[00:12:17:369 - 00:12:20:770] **Speaker 1:** The source term will be metres per metre squared, which
[00:12:20:770 - 00:12:23:429] **Speaker 1:** goes to metres to the power of -1.
[00:12:25:929 - 00:12:30:190] **Speaker 1:** And We also have a stationary state.
[00:12:30:469 - 00:12:32:419] **Speaker 1:** Laplace has no time dependence, it's not like the heat
[00:12:32:419 - 00:12:32:989] **Speaker 1:** equation.
[00:12:33:469 - 00:12:35:450] **Speaker 1:** So we've got a, a stationary study.
[00:12:38:869 - 00:12:41:890] **Speaker 1:** We're asked to insert a circle of radius 3 metres.
[00:12:42:549 - 00:12:45:570] **Speaker 1:** Um, it might be helpful to create a parameter.
[00:12:46:630 - 00:12:48:309] **Speaker 1:** So just like you do in Python, you can create
[00:12:48:309 - 00:12:50:830] **Speaker 1:** parameters at the top of the code, so parameters are
[00:12:50:830 - 00:12:54:070] **Speaker 1:** is global throughout all the components that you're analysing and
[00:12:54:070 - 00:12:55:169] **Speaker 1:** we've got 3 metres.
[00:12:56:479 - 00:12:58:440] **Speaker 1:** Again, square brackets to donate for units.
[00:12:58:880 - 00:13:00:140] **Speaker 1:** Uh, this is centred at the origin.
[00:13:00:210 - 00:13:01:210] **Speaker 1:** So I think that's the default.
[00:13:01:400 - 00:13:05:880] **Speaker 1:** The right click geometry, circle radius of R and build.
[00:13:06:429 - 00:13:07:679] **Speaker 1:** You can see that it's got a radius of 3
[00:13:07:679 - 00:13:08:260] **Speaker 1:** metres.
[00:13:08:840 - 00:13:11:320] **Speaker 1:** We've got a directly boundary condition on the circumference equal
[00:13:11:320 - 00:13:12:460] **Speaker 1:** to the Y coordinates.
[00:13:14:210 - 00:13:17:690] **Speaker 1:** So under the Laplace equation, we can create a Derick
[00:13:17:690 - 00:13:21:250] **Speaker 1:** Clay boundary condition and prescribe the displacement equal to Y.
[00:13:22:289 - 00:13:24:390] **Speaker 1:** The units match because they're both in metres.
[00:13:25:049 - 00:13:26:289] **Speaker 1:** Don't have to do anything fancy.
[00:13:26:570 - 00:13:27:799] **Speaker 1:** And we've also got a source term.
[00:13:28:330 - 00:13:30:690] **Speaker 1:** So this is under physics domain source or if we
[00:13:30:690 - 00:13:33:190] **Speaker 1:** right click the physics interface, we can select source.
[00:13:34:469 - 00:13:38:090] **Speaker 1:** Need to select the domain that we're applying this force
[00:13:38:090 - 00:13:38:510] **Speaker 1:** to.
[00:13:39:130 - 00:13:41:270] **Speaker 1:** Uh, so this was a step that some of you
[00:13:41:270 - 00:13:42:729] **Speaker 1:** uh skipped over in the lab.
[00:13:43:979 - 00:13:47:979] **Speaker 1:** And it's equal to 31 metre squared.
[00:13:48:900 - 00:13:53:630] **Speaker 1:** Multiplied by R minus the square root of X2 +
[00:13:53:630 - 00:13:54:750] **Speaker 1:** Y2.
[00:13:55:590 - 00:13:59:869] **Speaker 1:** So as you've seen so far, these expression boxes can
[00:13:59:869 - 00:14:04:250] **Speaker 1:** include uh simple functions like square root, sign, cosine, etc.
[00:14:04:789 - 00:14:06:309] **Speaker 1:** So we'll put another bracket in there.
[00:14:07:630 - 00:14:10:140] **Speaker 1:** That's our sauce term, uh, you could create a OH
[00:14:10:140 - 00:14:11:700] **Speaker 1:** good mesh, um.
[00:14:13:179 - 00:14:14:419] **Speaker 1:** As it takes a couple of minutes.
[00:14:14:500 - 00:14:16:020] **Speaker 1:** I don't, well, do you want me to do that
[00:14:16:020 - 00:14:16:729] **Speaker 1:** or you, no?
[00:14:16:900 - 00:14:17:390] **Speaker 1:** Yes.
[00:14:18:020 - 00:14:18:260] **Speaker 1:** No.
[00:14:20:520 - 00:14:21:320] **Speaker 1:** Silence.
[00:14:22:799 - 00:14:23:549] **Speaker 1:** I'm not gonna do it.
[00:14:23:679 - 00:14:24:979] **Speaker 1:** If you want to do it, you can.
[00:14:25:500 - 00:14:28:520] **Speaker 1:** Um I did spot that someone used the free quad
[00:14:28:520 - 00:14:29:419] **Speaker 1:** and that worked quite well.
[00:14:31:809 - 00:14:34:030] **Speaker 1:** So we'll do that instead.
[00:14:36:190 - 00:14:43:349] **Speaker 1:** And compute So Study computing.
[00:14:45:650 - 00:14:49:289] **Speaker 1:** Um So resulting independent variable is gonna sort of look
[00:14:49:289 - 00:14:50:159] **Speaker 1:** like this, so.
[00:14:51:010 - 00:14:52:840] **Speaker 1:** This is a surface plot, so we might want to
[00:14:52:840 - 00:14:57:320] **Speaker 1:** delete that, that one and include contours.
[00:14:59:210 - 00:15:01:580] **Speaker 1:** So plotting contours of the displacement field.
[00:15:02:580 - 00:15:05:010] **Speaker 1:** And we can change the number of levels, uh, you
[00:15:05:010 - 00:15:07:630] **Speaker 1:** can change the colour as well, um.
[00:15:09:150 - 00:15:09:650] **Speaker 1:** Somewhere.
[00:15:15:690 - 00:15:20:150] **Speaker 1:** I think I've got Oh, there we go.
[00:15:22:340 - 00:15:25:289] **Speaker 1:** And we also want to analyse the peak displacement within
[00:15:25:289 - 00:15:26:429] **Speaker 1:** the membrane.
[00:15:26:969 - 00:15:29:760] **Speaker 1:** So under more surface plots, maximum surface.
[00:15:31:460 - 00:15:32:599] **Speaker 1:** Uh, we can plot this.
[00:15:33:510 - 00:15:35:000] **Speaker 1:** So it's 11.35.
[00:15:35:419 - 00:15:37:520] **Speaker 1:** So this mesh is reasonably coarse.
[00:15:37:659 - 00:15:40:940] **Speaker 1:** I mean it's symmetrical, so it might do OK um
[00:15:40:940 - 00:15:43:500] **Speaker 1:** but maybe we'll just cheat and just check what results
[00:15:43:500 - 00:15:44:239] **Speaker 1:** we're expecting.
[00:15:45:580 - 00:15:47:900] **Speaker 1:** So it is, it is matching quite well, so we
[00:15:47:900 - 00:15:49:239] **Speaker 1:** don't need to do anything too fancy.
[00:15:50:770 - 00:15:52:669] **Speaker 1:** Um, so 11.36.
[00:15:54:729 - 00:15:57:260] **Speaker 1:** And 0.234.
[00:15:57:369 - 00:16:00:840] **Speaker 1:** So we're a bit out by the displacement in the
[00:16:00:929 - 00:16:03:059] **Speaker 1:** position of the peak displacement.
[00:16:04:080 - 00:16:06:400] **Speaker 1:** So what we'll do and what you should do anyway
[00:16:06:400 - 00:16:07:940] **Speaker 1:** is to do a mesh convergence study.
[00:16:09:599 - 00:16:12:479] **Speaker 1:** So, it's a little bit manual, but maybe we just
[00:16:12:479 - 00:16:14:080] **Speaker 1:** try extra fine.
[00:16:16:830 - 00:16:22:719] **Speaker 1:** And Did that solve?
[00:16:25:150 - 00:16:26:030] **Speaker 1:** That's very quick.
[00:16:31:049 - 00:16:31:469] **Speaker 1:** OK.
[00:16:31:890 - 00:16:34:760] **Speaker 1:** So we're getting closer, so now we've got 0.215.
[00:16:35:010 - 00:16:36:030] **Speaker 1:** So that's converging.
[00:16:36:489 - 00:16:39:260] **Speaker 1:** And maybe we do another one just for a good,
[00:16:39:409 - 00:16:40:020] **Speaker 1:** good measure.
[00:16:41:169 - 00:16:42:409] **Speaker 1:** Since it's so quick at solving.
[00:16:45:989 - 00:16:48:250] **Speaker 1:** Now we've got 0.246, which is getting closer.
[00:16:50:349 - 00:16:50:359] **Speaker 1:** Alright.
[00:16:53:890 - 00:16:54:919] **Speaker 1:** 4 times speeders.
[00:16:56:280 - 00:16:58:739] **Speaker 1:** So I'm sorry you don't get the answers underneath your
[00:16:59:159 - 00:17:00:760] **Speaker 1:** question boxes, but um.
[00:17:02:650 - 00:17:05:709] **Speaker 1:** I've got to get some Some help.
[00:17:06:329 - 00:17:07:750] **Speaker 1:** So 0.246.
[00:17:09:279 - 00:17:10:418] **Speaker 1:** And hopefully that's.
[00:17:11:250 - 00:17:13:589] **Speaker 1:** So always graded partial, so I think I was quite
[00:17:13:589 - 00:17:16:060] **Speaker 1:** picky with the displacement of the.
[00:17:16:787 - 00:17:17:769] **Speaker 1:** Um, location.
[00:17:18:688 - 00:17:20:029] **Speaker 1:** So 0.2.
[00:17:22:979 - 00:17:23:599] **Speaker 1:** Yeah.
[00:17:24:140 - 00:17:25:739] **Speaker 1:** So maybe you have to do your OH grid to
[00:17:25:739 - 00:17:26:400] **Speaker 1:** get full credit.
[00:17:27:510 - 00:17:28:800] **Speaker 1:** But I know a lot of people got the full
[00:17:28:800 - 00:17:29:560] **Speaker 1:** marks for that one.
[00:17:30:189 - 00:17:32:349] **Speaker 1:** any questions on that workflow?
[00:17:38:030 - 00:17:38:579] **Speaker 1:** All good.
[00:17:40:569 - 00:17:43:939] **Speaker 1:** Right That's all right.
[00:17:44:020 - 00:17:45:920] **Speaker 1:** You don't have to be engaged, I guess.
[00:17:46:260 - 00:17:50:410] **Speaker 1:** Um, so quiz 4 is another quiz that we've got
[00:17:50:410 - 00:17:51:140] **Speaker 1:** open this week.
[00:17:51:390 - 00:17:55:060] **Speaker 1:** Again, I do these quizzes because otherwise, We get to
[00:17:55:060 - 00:17:58:489] **Speaker 1:** the assignment and Many people don't know what's going on.
[00:18:00:089 - 00:18:02:250] **Speaker 1:** So try and keep you up to date.
[00:18:02:369 - 00:18:05:000] **Speaker 1:** So quiz 4 we're gonna do method of separation variables
[00:18:05:000 - 00:18:05:790] **Speaker 1:** again for the heat equation.
[00:18:06:569 - 00:18:07:469] **Speaker 1:** So that was chapter.
[00:18:09:000 - 00:18:13:589] **Speaker 1:** 5 Chapter 5 was analytical for heat equation.
[00:18:13:890 - 00:18:17:410] **Speaker 1:** And then question 2 is looking at discrets, using the
[00:18:17:410 - 00:18:18:530] **Speaker 1:** backward in time centre in space.
[00:18:18:569 - 00:18:19:989] **Speaker 1:** So that was from chapter 6.
[00:18:20:609 - 00:18:21:910] **Speaker 1:** And then question 3.
[00:18:22:869 - 00:18:25:770] **Speaker 1:** Is solving a heat transfer problem.
[00:18:26:729 - 00:18:29:530] **Speaker 1:** Uh, and console, so this is of a cube.
[00:18:29:849 - 00:18:33:089] **Speaker 1:** We have a fixed temperature at the base and initial
[00:18:33:089 - 00:18:36:369] **Speaker 1:** temperature and then analysing the influence of a heat source
[00:18:36:609 - 00:18:38:569] **Speaker 1:** being applied throughout the cube over time.
[00:18:38:689 - 00:18:42:650] **Speaker 1:** So seeing what the temperature is, our average temperature after
[00:18:42:650 - 00:18:43:229] **Speaker 1:** one hour.
[00:18:47:209 - 00:18:49:040] **Speaker 1:** So you might want to think about how can you
[00:18:49:040 - 00:18:50:089] **Speaker 1:** simplify this problem?
[00:18:50:199 - 00:18:52:489] **Speaker 1:** Can you model it as 3D?
[00:18:52:689 - 00:18:55:170] **Speaker 1:** Could, could you model it as 2D or even 1D?
[00:18:55:689 - 00:18:58:790] **Speaker 1:** Um, think about what boundary conditions are being imposed.
[00:18:59:410 - 00:19:02:569] **Speaker 1:** And if you can make some assumptions or make some
[00:19:02:569 - 00:19:04:550] **Speaker 1:** simplifications for your computational domain.
[00:19:05:280 - 00:19:07:079] **Speaker 1:** And just speed up that computation time.
[00:19:08:979 - 00:19:13:949] **Speaker 1:** So that's a good segue into The lab this week,
[00:19:14:239 - 00:19:15:140] **Speaker 1:** so lab 4.
[00:19:17:130 - 00:19:22:400] **Speaker 1:** Page 143 So we're gonna solve the heat equation using
[00:19:22:400 - 00:19:25:660] **Speaker 1:** both the inbuilt physics interface for heat transfer in solids.
[00:19:26:609 - 00:19:28:359] **Speaker 1:** And the coefficient form PDE.
[00:19:28:890 - 00:19:31:449] **Speaker 1:** So the coefficient from PDE allows you to solve pretty
[00:19:31:449 - 00:19:32:790] **Speaker 1:** much generic PDEs.
[00:19:33:010 - 00:19:33:829] **Speaker 1:** So it's pretty neat.
[00:19:34:209 - 00:19:36:750] **Speaker 1:** And and but one is sort of set up specifically
[00:19:36:750 - 00:19:38:449] **Speaker 1:** for heat transfer and solids.
[00:19:41:180 - 00:19:43:089] **Speaker 1:** So the heat transfer in solids, you'll go through, this
[00:19:43:089 - 00:19:47:430] **Speaker 1:** is a two-dimensional domain uh that we're analysing this week.
[00:19:48:920 - 00:19:51:709] **Speaker 1:** And we have a set of equations.
[00:19:51:800 - 00:19:54:819] **Speaker 1:** Again, you've got some arbitrary unit uh of depth DZ.
[00:19:56:000 - 00:19:58:819] **Speaker 1:** We've got some directly boundary conditions that vary in space.
[00:20:00:270 - 00:20:02:030] **Speaker 1:** And a heat source being applied as well.
[00:20:03:030 - 00:20:04:410] **Speaker 1:** So using a suitable mesh.
[00:20:05:339 - 00:20:06:819] **Speaker 1:** It's just a square domain, so you could use a
[00:20:06:819 - 00:20:08:420] **Speaker 1:** mapped uh structured grid.
[00:20:09:209 - 00:20:11:540] **Speaker 1:** The next part is to analyse what the coefficient form
[00:20:11:540 - 00:20:11:890] **Speaker 1:** PDE.
[00:20:12:890 - 00:20:15:569] **Speaker 1:** And we're going to match the coefficients in the general
[00:20:15:569 - 00:20:18:650] **Speaker 1:** form, this coefficient form PD with the heat transfer module
[00:20:18:650 - 00:20:20:329] **Speaker 1:** or with the heat heat equation.
[00:20:21:189 - 00:20:25:150] **Speaker 1:** So we'll be matching up the coefficients given with that
[00:20:25:150 - 00:20:25:949] **Speaker 1:** from the heat equation.
[00:20:28:109 - 00:20:30:819] **Speaker 1:** The same initial and directly boundary conditions, so be careful
[00:20:30:819 - 00:20:33:890] **Speaker 1:** of using uh units, so degrees Celsius.
[00:20:34:670 - 00:20:36:170] **Speaker 1:** uh this.
[00:20:37:500 - 00:20:39:459] **Speaker 1:** Yeah, by default it's gonna be using Kelvin's as a
[00:20:39:459 - 00:20:40:239] **Speaker 1:** base SI unit.
[00:20:40:500 - 00:20:43:020] **Speaker 1:** They want to convert it to degrees Celsius, and that
[00:20:43:020 - 00:20:45:300] **Speaker 1:** can be achieved by just typing zero and then square
[00:20:45:300 - 00:20:47:619] **Speaker 1:** brackets, degrees C, D E G C.
[00:20:49:900 - 00:20:50:900] **Speaker 1:** And you're solving.
[00:20:51:060 - 00:20:52:900] **Speaker 1:** The last step is to how to export to Python,
[00:20:52:979 - 00:20:55:140] **Speaker 1:** so that'll be helpful for your, your assignment when you're
[00:20:55:140 - 00:20:58:300] **Speaker 1:** trying to analyse and pull in together uh results.
[00:20:59:599 - 00:21:01:859] **Speaker 1:** So you can use a cut line.
[00:21:02:719 - 00:21:05:339] **Speaker 1:** And also a surface top.
[00:21:06:010 - 00:21:08:689] **Speaker 1:** So I've gone through uh and provided the code that
[00:21:08:689 - 00:21:10:150] **Speaker 1:** you require for the Python script.
[00:21:10:369 - 00:21:12:569] **Speaker 1:** I've also provided the Python script on Learn in the
[00:21:12:569 - 00:21:13:550] **Speaker 1:** course material folder.
[00:21:14:319 - 00:21:15:369] **Speaker 1:** In case you're stuck.
[00:21:16:229 - 00:21:18:589] **Speaker 1:** Uh, but that's the lab that we'll do this week.
[00:21:18:739 - 00:21:20:750] **Speaker 1:** Again, you can do the lab at any time, uh,
[00:21:20:819 - 00:21:23:329] **Speaker 1:** but we've got the next week and help sessions sort
[00:21:23:329 - 00:21:24:189] **Speaker 1:** of built, um.
[00:21:25:640 - 00:21:27:189] **Speaker 1:** timetabled for that Thursday afternoon.
[00:21:27:810 - 00:21:29:310] **Speaker 1:** I just remember to try and go to your own
[00:21:29:310 - 00:21:30:150] **Speaker 1:** timetabled slot.
[00:21:30:209 - 00:21:32:099] **Speaker 1:** I know the one o'clock is like super busy.
[00:21:32:369 - 00:21:34:650] **Speaker 1:** Uh, everyone finds that to be the most popular.
[00:21:35:050 - 00:21:36:849] **Speaker 1:** So especially if you want extra help, come to the
[00:21:36:849 - 00:21:39:369] **Speaker 1:** later ones when it's really quiet, um, and we're just
[00:21:39:369 - 00:21:40:689] **Speaker 1:** really bored, um.
[00:21:41:709 - 00:21:43:910] **Speaker 1:** Standing around, not really doing anything.
[00:21:44:189 - 00:21:46:130] **Speaker 1:** So make sure you make the most of those.
[00:21:46:550 - 00:21:48:949] **Speaker 1:** Um, you probably will do the following week when you
[00:21:48:949 - 00:21:50:270] **Speaker 1:** go through the assignment anyway.
[00:21:53:239 - 00:21:54:079] **Speaker 1:** All right.
[00:21:58:310 - 00:22:01:709] **Speaker 1:** Any Questions.
[00:22:03:989 - 00:22:06:760] **Speaker 1:** Um, anything, otherwise we'll, yep.
[00:22:09:989 - 00:22:12:050] **Speaker 1:** Uh, soon, so I heard that they are marked and
[00:22:12:050 - 00:22:13:920] **Speaker 1:** I'm sort of just getting collated and, and things like
[00:22:13:920 - 00:22:17:000] **Speaker 1:** that, so probably in the next day or two, yeah.
[00:22:25:530 - 00:22:26:040] **Speaker 1:** Cool.
[00:22:26:199 - 00:22:27:400] **Speaker 1:** No other questions?
[00:22:27:760 - 00:22:29:140] **Speaker 1:** No questions for my stuff.
[00:22:30:000 - 00:22:31:420] **Speaker 1:** It's too easy, that's why.
[00:22:36:380 - 00:22:36:880] **Speaker 1:** Maybe.
[00:22:37:150 - 00:22:37:520] **Speaker 1:** All right.
[00:22:37:939 - 00:22:38:680] **Speaker 1:** So chapter 11.
[00:22:38:900 - 00:22:41:500] **Speaker 1:** So this is page 93 for those following along in
[00:22:41:500 - 00:22:42:359] **Speaker 1:** your course reader.
[00:22:43:140 - 00:22:46:150] **Speaker 1:** That seems to be a little bit delayed, like I
[00:22:47:189 - 00:22:47:689] **Speaker 1:** I dunno.
[00:22:48:969 - 00:22:51:329] **Speaker 1:** Maybe I'll just write slower or just move my hand
[00:22:51:329 - 00:22:51:709] **Speaker 1:** away.
[00:22:52:489 - 00:22:53:949] **Speaker 1:** Let me know if you can't read.
[00:22:56:640 - 00:22:59:500] **Speaker 1:** All right, so we've touched a little bit on stability
[00:22:59:500 - 00:23:01:109] **Speaker 1:** of the explicit scheme.
[00:23:01:199 - 00:23:03:290] **Speaker 1:** We said that if lambda was too large, the time
[00:23:03:290 - 00:23:06:300] **Speaker 1:** steps are too large, then the solution becomes unstable.
[00:23:06:859 - 00:23:08:319] **Speaker 1:** So we want to dive a little bit deeper into
[00:23:08:319 - 00:23:11:030] **Speaker 1:** consistency, stability and convergence and chapter 11.
[00:23:11:119 - 00:23:13:589] **Speaker 1:** So we'll start that today and finish it off on
[00:23:13:589 - 00:23:14:160] **Speaker 1:** Wednesday.
[00:23:15:109 - 00:23:19:650] **Speaker 1:** So numerical methods um are generally used in engineering.
[00:23:19:739 - 00:23:22:680] **Speaker 1:** So we'll use simulation software packages uh we we're teaching
[00:23:22:680 - 00:23:26:619] **Speaker 1:** you console, but others uh we'll use fluent may maybe
[00:23:26:619 - 00:23:30:540] **Speaker 1:** for CFD Abacus for FEA, um, and a whole host
[00:23:30:540 - 00:23:31:979] **Speaker 1:** of other simulation tools.
[00:23:32:459 - 00:23:33:660] **Speaker 1:** But the principles are very similar.
[00:23:33:739 - 00:23:37:560] **Speaker 1:** You've got pre-processing, solving, and then post-processing with the results.
[00:23:38:099 - 00:23:40:859] **Speaker 1:** And they all have some sort of discrete approximation to
[00:23:40:859 - 00:23:43:160] **Speaker 1:** the true physics or true equations.
[00:23:43:859 - 00:23:45:699] **Speaker 1:** So they're always applying numerical methods.
[00:23:47:209 - 00:23:50:270] **Speaker 1:** So that typically employed when there's no analytical solution.
[00:23:50:849 - 00:23:52:920] **Speaker 1:** So we've already seen that we can use the separation
[00:23:52:920 - 00:23:55:310] **Speaker 1:** of variables for some really simple cases, which is great.
[00:23:55:800 - 00:23:57:689] **Speaker 1:** Uh, but as soon as you try to have boundary
[00:23:57:689 - 00:24:00:170] **Speaker 1:** conditions that are a little bit different, the geometry changes
[00:24:00:170 - 00:24:02:910] **Speaker 1:** or anything, you'll find that it comes really, really challenging.
[00:24:04:949 - 00:24:07:510] **Speaker 1:** So, in contrast to those analytical methods, which are sort
[00:24:07:510 - 00:24:11:670] **Speaker 1:** of true solutions for those schemes, those PDUs, uh, we
[00:24:11:670 - 00:24:14:030] **Speaker 1:** have some errors that are approximated.
[00:24:15:349 - 00:24:18:420] **Speaker 1:** We introduced as approximations for our numerical solutions.
[00:24:19:920 - 00:24:21:540] **Speaker 1:** And we're gonna talk a bit about that.
[00:24:22:000 - 00:24:24:640] **Speaker 1:** So as we're just on the heat equation, we're gonna
[00:24:24:640 - 00:24:27:400] **Speaker 1:** focus on the heat equation, the one-dimensional heat equation that
[00:24:27:400 - 00:24:28:160] **Speaker 1:** we derived earlier.
[00:24:28:359 - 00:24:30:369] **Speaker 1:** So back in the equation 5.2.
[00:24:31:000 - 00:24:33:650] **Speaker 1:** So just as a recap, this was a temperature.
[00:24:36:000 - 00:24:39:000] **Speaker 1:** Um, temperature being a dependent variable, we're seeing how it
[00:24:39:000 - 00:24:41:719] **Speaker 1:** changes over time and equating that with a diffusive, uh,
[00:24:41:760 - 00:24:42:619] **Speaker 1:** diffusive rate.
[00:24:42:959 - 00:24:46:810] **Speaker 1:** So alpha D2 T I D X 2.
[00:24:49:369 - 00:24:51:150] **Speaker 1:** So that's our heat equation that we've come across, the
[00:24:51:150 - 00:24:52:859] **Speaker 1:** parabolic type.
[00:24:53:430 - 00:24:56:589] **Speaker 1:** And we're gonna analyse this across a unit length of
[00:24:56:589 - 00:24:56:949] **Speaker 1:** one.
[00:25:02:040 - 00:25:03:959] **Speaker 1:** Alpha as a recap is K over row C is
[00:25:03:959 - 00:25:04:839] **Speaker 1:** a heat divisivity.
[00:25:05:199 - 00:25:06:880] **Speaker 1:** Again, I know that the trans students don't do the
[00:25:06:880 - 00:25:10:280] **Speaker 1:** heat transfer course, but it's just an equation you can
[00:25:10:280 - 00:25:12:760] **Speaker 1:** think of as other things like the species transport um
[00:25:12:760 - 00:25:15:199] **Speaker 1:** that we looked at in the earlier chapter.
[00:25:16:089 - 00:25:18:329] **Speaker 1:** So our boundary conditions in this case are just gonna
[00:25:18:329 - 00:25:20:579] **Speaker 1:** be set at 0 at either end.
[00:25:21:290 - 00:25:21:930] **Speaker 1:** So T.
[00:25:24:020 - 00:25:26:660] **Speaker 1:** On the left-hand side, so X equal to 0 for
[00:25:26:660 - 00:25:28:719] **Speaker 1:** all time, it's gonna be set to 0.
[00:25:29:689 - 00:25:33:849] **Speaker 1:** T at the right-hand side for all time is equal
[00:25:33:849 - 00:25:34:540] **Speaker 1:** to 0.
[00:25:34:890 - 00:25:37:729] **Speaker 1:** And for our initial condition, we're going to prescribe a
[00:25:37:729 - 00:25:38:530] **Speaker 1:** sine wave.
[00:25:44:250 - 00:25:45:400] **Speaker 1:** So sin of pi X.
[00:25:52:829 - 00:25:54:189] **Speaker 1:** I think that's OK.
[00:25:54:349 - 00:25:55:390] **Speaker 1:** That's as bright as it is.
[00:25:55:469 - 00:25:56:010] **Speaker 1:** I don't know.
[00:25:56:390 - 00:25:57:790] **Speaker 1:** That's bright enough for you.
[00:25:58:729 - 00:26:01:069] **Speaker 1:** Um, alright, so we've got the temperature being set at
[00:26:01:069 - 00:26:02:410] **Speaker 1:** 0 at either end and then we've got a sine
[00:26:02:410 - 00:26:04:609] **Speaker 1:** wave and.
[00:26:05:390 - 00:26:07:229] **Speaker 1:** That should uniquely identify this problem.
[00:26:07:630 - 00:26:10:849] **Speaker 1:** We've got 2 boundary conditions, 2 initial conditions for our
[00:26:11:150 - 00:26:13:530] **Speaker 1:** second order derivative in space and first order in time.
[00:26:15:280 - 00:26:18:280] **Speaker 1:** Now, we're going to just set up some terminology or
[00:26:18:280 - 00:26:20:900] **Speaker 1:** some definitions for where these errors come from.
[00:26:21:640 - 00:26:23:680] **Speaker 1:** So if we're analysing a point in space and time,
[00:26:23:750 - 00:26:26:979] **Speaker 1:** we've got X subscript I to denote the index of
[00:26:26:979 - 00:26:29:739] **Speaker 1:** our spatial coordinate TN for the nth time level.
[00:26:30:859 - 00:26:34:130] **Speaker 1:** And the exact solution of our PDE is going to
[00:26:34:130 - 00:26:38:420] **Speaker 1:** be evaluated at that point in space and time, so
[00:26:38:420 - 00:26:39:260] **Speaker 1:** XITN.
[00:26:41:260 - 00:26:42:339] **Speaker 1:** So you can think of that as sort of the
[00:26:42:349 - 00:26:44:479] **Speaker 1:** the continuous or true solution.
[00:26:45:119 - 00:26:48:719] **Speaker 1:** Uh, the exact solution of the discretized equation is our
[00:26:48:719 - 00:26:52:469] **Speaker 1:** standard form of using subscript I superscript N, so TIN,
[00:26:52:560 - 00:26:54:380] **Speaker 1:** that's what we used for our finite differencing.
[00:26:54:959 - 00:26:58:180] **Speaker 1:** And then the final computed solution for our numerical scheme.
[00:26:58:520 - 00:27:01:439] **Speaker 1:** So after we solve maybe with a direct method or
[00:27:01:439 - 00:27:05:739] **Speaker 1:** the iterative method with Lieben, uh, we've got another solution
[00:27:06:439 - 00:27:08:550] **Speaker 1:** with T hat in IN.
[00:27:13:500 - 00:27:15:410] **Speaker 1:** So those are the three sort of stages that we
[00:27:15:410 - 00:27:15:910] **Speaker 1:** go through.
[00:27:17:050 - 00:27:22:209] **Speaker 1:** Uh, and correspondingly we've got some errors associated with each
[00:27:22:209 - 00:27:22:630] **Speaker 1:** step.
[00:27:23:500 - 00:27:27:449] **Speaker 1:** So the model era Might be that the mesh does
[00:27:27:449 - 00:27:29:510] **Speaker 1:** not precisely capture the geometry.
[00:27:29:890 - 00:27:33:760] **Speaker 1:** So if we use triangular elements or rectangular elements to
[00:27:34:170 - 00:27:36:510] **Speaker 1:** approximate a curve would be an example.
[00:27:37:209 - 00:27:40:650] **Speaker 1:** Discretization error is the difference between the exact solution and
[00:27:40:650 - 00:27:42:569] **Speaker 1:** the discretized solution.
[00:27:43:000 - 00:27:47:250] **Speaker 1:** The solution error is the error between the discretized and
[00:27:47:250 - 00:27:48:319] **Speaker 1:** the final computed.
[00:27:48:609 - 00:27:51:369] **Speaker 1:** So maybe due to that Liebman method, and then the
[00:27:51:369 - 00:27:54:229] **Speaker 1:** total is the difference between the exact and final computed.
[00:27:55:109 - 00:27:56:510] **Speaker 1:** So you can think of this in terms of a
[00:27:56:510 - 00:27:57:209] **Speaker 1:** flow chart.
[00:28:01:239 - 00:28:04:010] **Speaker 1:** And we'll have 3 Boxes.
[00:28:13:810 - 00:28:17:160] **Speaker 1:** So we start from uh our governing PDE so formula.
[00:28:20:489 - 00:28:21:349] **Speaker 1:** Our governing.
[00:28:23:569 - 00:28:33:130] **Speaker 1:** PDE I've got dial-up for the video.
[00:28:34:449 - 00:28:34:930] **Speaker 1:** All right.
[00:28:35:369 - 00:28:38:250] **Speaker 1:** So we've got formulating the governing PDE and then we
[00:28:38:250 - 00:28:39:810] **Speaker 1:** need to go and discretize it.
[00:28:39:969 - 00:28:41:329] **Speaker 1:** So we use our central differenceerencing.
[00:28:42:390 - 00:28:43:449] **Speaker 1:** So discretized.
[00:28:45:910 - 00:28:48:869] **Speaker 1:** From Of PDE.
[00:28:49:650 - 00:28:51:780] **Speaker 1:** So that's where we've got all the TINs, etc.
[00:28:52:300 - 00:28:54:520] **Speaker 1:** And then we want to solve that system of equations
[00:28:54:819 - 00:28:55:699] **Speaker 1:** to solve.
[00:28:57:410 - 00:29:01:790] **Speaker 1:** System Of equations.
[00:29:05:890 - 00:29:09:869] **Speaker 1:** So that initial true solution is just XI.
[00:29:11:349 - 00:29:17:810] **Speaker 1:** T N The discretized form we used TIN.
[00:29:19:010 - 00:29:22:010] **Speaker 1:** And we're sort of introducing this now just for completeness,
[00:29:22:250 - 00:29:24:770] **Speaker 1:** just because we want to distinguish between the final computed
[00:29:24:770 - 00:29:28:010] **Speaker 1:** solution and discretize, we're adding a hat for this final
[00:29:28:010 - 00:29:28:540] **Speaker 1:** computed DIN.
[00:29:33:349 - 00:29:34:400] **Speaker 1:** So we've got 3 stages.
[00:29:34:770 - 00:29:38:819] **Speaker 1:** Uh, when we say consistency, we're going to compare the
[00:29:38:819 - 00:29:43:020] **Speaker 1:** difference between our analytical or true solution with our discretized
[00:29:43:170 - 00:29:43:780] **Speaker 1:** equation.
[00:29:44:140 - 00:29:46:280] **Speaker 1:** So our first stage is consistency.
[00:29:51:969 - 00:29:56:359] **Speaker 1:** And this is related to Discretization error.
[00:29:59:479 - 00:29:59:920] **Speaker 1:** Lost it.
[00:30:02:280 - 00:30:04:780] **Speaker 1:** Um Sorry.
[00:30:06:579 - 00:30:07:640] **Speaker 1:** Maybe if I zoom in.
[00:30:08:969 - 00:30:12:000] **Speaker 1:** 00, no, I'll keep you on your toes.
[00:30:16:349 - 00:30:19:400] **Speaker 1:** Um, All right.
[00:30:20:099 - 00:30:24:319] **Speaker 1:** So, That's where we do like used all those Taylor
[00:30:24:319 - 00:30:27:430] **Speaker 1:** series expansions, and we approximated those derivatives.
[00:30:27:550 - 00:30:29:790] **Speaker 1:** If we didn't include lots of Taylor series terms or
[00:30:29:790 - 00:30:32:430] **Speaker 1:** have a fine mesh, we'd have large discretization error.
[00:30:32:589 - 00:30:33:709] **Speaker 1:** So that's where that's coming from.
[00:30:35:060 - 00:30:39:079] **Speaker 1:** If our discretized, um, form vowel equations.
[00:30:40:469 - 00:30:43:150] **Speaker 1:** Match our governing equations, you know, we can say that
[00:30:43:150 - 00:30:43:869] **Speaker 1:** it's consistent.
[00:30:45:119 - 00:30:47:959] **Speaker 1:** So now between the discrete size form and the final
[00:30:47:959 - 00:30:50:900] **Speaker 1:** computed form, uh, we talked a bit about stability.
[00:30:54:750 - 00:30:56:729] **Speaker 1:** And this is related to the solution error.
[00:31:12:719 - 00:31:13:199] **Speaker 1:** Cool.
[00:31:13:479 - 00:31:13:859] **Speaker 1:** All right.
[00:31:14:239 - 00:31:16:359] **Speaker 1:** So all of our numerical schemes that at least that
[00:31:16:359 - 00:31:19:880] **Speaker 1:** we're looking at in this class, um, involve some sort
[00:31:19:880 - 00:31:22:880] **Speaker 1:** of form of error due to this discretization process.
[00:31:22:989 - 00:31:26:280] **Speaker 1:** As I say, Taylor series expansions were approximating and ignoring
[00:31:26:280 - 00:31:27:420] **Speaker 1:** those higher-order terms.
[00:31:28:229 - 00:31:30:790] **Speaker 1:** Uh, so when we're partitioning the solution space and data
[00:31:30:790 - 00:31:34:890] **Speaker 1:** X and data T for approximating our, uh, derivatives.
[00:31:36:119 - 00:31:40:760] **Speaker 1:** So consistency is where our discretization equations and the differential
[00:31:40:760 - 00:31:44:760] **Speaker 1:** equations are equivalent as we reduce the step size.
[00:31:44:880 - 00:31:46:849] **Speaker 1:** So data X and T to 0.
[00:31:47:520 - 00:31:52:439] **Speaker 1:** So as we reduce our mesh sizing in space and
[00:31:52:439 - 00:31:54:670] **Speaker 1:** time, we expect that the solution is going to converge
[00:31:54:670 - 00:31:55:439] **Speaker 1:** to the true solution.
[00:31:57:689 - 00:31:58:770] **Speaker 1:** So that should be the case.
[00:31:58:969 - 00:32:01:250] **Speaker 1:** So we're gonna analyse the forward in time central in
[00:32:01:250 - 00:32:04:550] **Speaker 1:** space, the explicit scheme that we looked at earlier and
[00:32:04:560 - 00:32:07:530] **Speaker 1:** and see whether or not this this numerical scheme is
[00:32:07:530 - 00:32:08:209] **Speaker 1:** consistent.
[00:32:09:739 - 00:32:10:689] **Speaker 1:** So we applied.
[00:32:13:359 - 00:32:17:219] **Speaker 1:** Um, we're looking at our heat equation.
[00:32:17:890 - 00:32:18:579] **Speaker 1:** Nice and easy.
[00:32:19:000 - 00:32:20:920] **Speaker 1:** We've got an initial profile, so I've plotted the sine
[00:32:20:920 - 00:32:23:880] **Speaker 1:** wave that that you can sort of see, and it
[00:32:23:880 - 00:32:26:300] **Speaker 1:** peaks at 1 and at 0 at the ends.
[00:32:26:719 - 00:32:29:000] **Speaker 1:** So we already know that the initial and boundary conditions
[00:32:29:000 - 00:32:32:719] **Speaker 1:** are consistent because the the temperature is at 0 at
[00:32:32:719 - 00:32:35:400] **Speaker 1:** the ends, which is the same initial and boundary.
[00:32:39:750 - 00:32:43:859] **Speaker 1:** And we're going to apply our finite differencing scheme.
[00:32:44:060 - 00:32:46:869] **Speaker 1:** So this was forward in time, central in space.
[00:32:47:310 - 00:32:50:449] **Speaker 1:** So the forward in time for our time derivative.
[00:32:51:910 - 00:32:56:239] **Speaker 1:** We are approximating DT by DT.
[00:33:00:010 - 00:33:05:390] **Speaker 1:** With TIN + 1 minus TINT.
[00:33:08:410 - 00:33:10:930] **Speaker 1:** So it's that sort of one-sided, all explicit scheme.
[00:33:12:569 - 00:33:13:510] **Speaker 1:** Finite differencing.
[00:33:13:890 - 00:33:16:989] **Speaker 1:** And we're gonna use central differencing for the spatial derivatives.
[00:33:17:969 - 00:33:23:260] **Speaker 1:** So D2 T by DX2 is approximately.
[00:33:24:810 - 00:33:29:369] **Speaker 1:** TI + 1 minus 2 TI + TI minus 1
[00:33:29:650 - 00:33:31:439] **Speaker 1:** over X2.
[00:33:33:010 - 00:33:34:329] **Speaker 1:** Uh, this is an explicit scheme.
[00:33:34:369 - 00:33:36:010] **Speaker 1:** It's the forward in time, central in space.
[00:33:36:050 - 00:33:38:489] **Speaker 1:** So we're gonna evaluate all the temperature values of this
[00:33:38:489 - 00:33:41:459] **Speaker 1:** derivative at the previous time level, time level in.
[00:33:42:010 - 00:33:44:250] **Speaker 1:** So all these superscripts are in.
[00:33:49:099 - 00:33:51:369] **Speaker 1:** So we've got our two derivatives that we're approximating with
[00:33:51:369 - 00:33:52:140] **Speaker 1:** our finite differenceferencing.
[00:33:52:319 - 00:33:54:380] **Speaker 1:** We're gonna combine into our heat equation and we're left
[00:33:54:380 - 00:34:00:939] **Speaker 1:** with TIN + 1 minus TIN divided by T equal
[00:34:00:939 - 00:34:01:219] **Speaker 1:** to.
[00:34:01:930 - 00:34:05:040] **Speaker 1:** Well, on It's a trap.
[00:34:05:349 - 00:34:06:800] **Speaker 1:** So this is minus alpha.
[00:34:08:110 - 00:34:10:669] **Speaker 1:** We're gonna put all of our terms or our discretized
[00:34:10:669 - 00:34:11:888] **Speaker 1:** terms on the left-hand side.
[00:34:12:620 - 00:34:13:790] **Speaker 1:** So we've got minus alpha.
[00:34:17:239 - 00:34:23:100] **Speaker 1:** TI + 1 N minus 2 TIN plus TI minus
[00:34:23:100 - 00:34:25:840] **Speaker 1:** 1 N divided by X 2.
[00:34:27:830 - 00:34:30:810] **Speaker 1:** So this should equal 0 in theory.
[00:34:31:229 - 00:34:31:830] **Speaker 1:** We've moved.
[00:34:32:908 - 00:34:35:199] **Speaker 1:** Our, our heat equation all onto one side, so it
[00:34:35:199 - 00:34:36:138] **Speaker 1:** leaves 0 on the right.
[00:34:45:059 - 00:34:48:938] **Speaker 1:** So we already know that this is not quite true
[00:34:48:938 - 00:34:51:617] **Speaker 1:** because the exact solution to our PDE is not going
[00:34:51:617 - 00:34:54:779] **Speaker 1:** to satisfy the discretization, um, discretized equation.
[00:34:55:178 - 00:34:56:678] **Speaker 1:** Otherwise, our discretized.
[00:34:57:590 - 00:35:01:739] **Speaker 1:** Values, TIN is going to equal the true values T
[00:35:01:739 - 00:35:02:370] **Speaker 1:** at XT.
[00:35:04:830 - 00:35:08:250] **Speaker 1:** So what we're gonna do is um evaluate.
[00:35:09:399 - 00:35:12:800] **Speaker 1:** That difference or that error and label it the truncation
[00:35:12:800 - 00:35:13:239] **Speaker 1:** error.
[00:35:14:790 - 00:35:16:750] **Speaker 1:** So we're gonna label towel.
[00:35:18:110 - 00:35:19:399] **Speaker 1:** At some time level in.
[00:35:22:469 - 00:35:23:790] **Speaker 1:** To be equal to.
[00:35:27:399 - 00:35:29:360] **Speaker 1:** Now we're going, what we're gonna do here, I guess
[00:35:29:360 - 00:35:31:879] **Speaker 1:** taking a step back, is we're gonna substitute in the
[00:35:31:879 - 00:35:34:360] **Speaker 1:** true solution into our discretized equation.
[00:35:36:419 - 00:35:38:929] **Speaker 1:** So this holds for our numerics and that's what we're
[00:35:38:929 - 00:35:41:250] **Speaker 1:** going to try and solve with our final computed solution.
[00:35:41:770 - 00:35:44:409] **Speaker 1:** But if we substitute in the true solution, so T
[00:35:44:409 - 00:35:47:929] **Speaker 1:** evaluated at those points in space and time, then we
[00:35:47:929 - 00:35:49:350] **Speaker 1:** should find that there's some residual.
[00:35:49:649 - 00:35:53:879] **Speaker 1:** So we're going to substitute in T at XITN.
[00:35:56:729 - 00:35:57:340] **Speaker 1:** Plus one.
[00:35:58:570 - 00:36:00:550] **Speaker 1:** It's too many times.
[00:36:02:459 - 00:36:13:989] **Speaker 1:** Um So T X I TN + 1 minus T.
[00:36:14:969 - 00:36:16:820] **Speaker 1:** At XITN.
[00:36:18:370 - 00:36:20:310] **Speaker 1:** Divided by T.
[00:36:24:899 - 00:36:26:520] **Speaker 1:** So it's the 1st term and the 2nd term we'll
[00:36:26:520 - 00:36:29:689] **Speaker 1:** do the same substituting in our analytical the true solution.
[00:36:29:909 - 00:36:31:229] **Speaker 1:** We've got minus alpha.
[00:36:32:030 - 00:36:36:350] **Speaker 1:** T at XI + 1 and TN.
[00:36:37:389 - 00:36:45:580] **Speaker 1:** -2 T evaluated at XITN plus T at Xi minus
[00:36:45:580 - 00:36:49:300] **Speaker 1:** 1 TN divided by X2.
[00:36:52:669 - 00:36:56:870] **Speaker 1:** So we're substting in the True solution into our discretized
[00:36:57:409 - 00:36:58:149] **Speaker 1:** uh equation.
[00:37:03:060 - 00:37:05:050] **Speaker 1:** And we haven't finished with Taylor series yet, so we're
[00:37:05:050 - 00:37:05:879] **Speaker 1:** coming back to those.
[00:37:06:899 - 00:37:10:070] **Speaker 1:** So we're gonna drive Each of these terms we've got
[00:37:10:070 - 00:37:14:149] **Speaker 1:** XI TN + 1, XI + 1 and Xi minus
[00:37:14:149 - 00:37:14:989] **Speaker 1:** 1 at TN.
[00:37:17:260 - 00:37:20:120] **Speaker 1:** And then we're going to substitute them back in.
[00:37:20:260 - 00:37:22:379] **Speaker 1:** So essentially we're trying to figure out how much discretization
[00:37:22:379 - 00:37:25:739] **Speaker 1:** error there is associated with this finite differenceencing.
[00:37:27:229 - 00:37:32:669] **Speaker 1:** So first T at XITN + 1.
[00:37:35:219 - 00:37:39:889] **Speaker 1:** So we're doing a tailored series about TXITN.
[00:37:42:860 - 00:37:44:030] **Speaker 1:** So first term we've got Tarati.
[00:37:46:760 - 00:37:52:939] **Speaker 1:** And then DT by DT at XITN.
[00:37:54:209 - 00:37:56:310] **Speaker 1:** Plus some order of delta T2.
[00:37:58:500 - 00:38:02:590] **Speaker 1:** So we know that this is a first accurate one-sidedwer
[00:38:02:979 - 00:38:03:699] **Speaker 1:** um.
[00:38:04:820 - 00:38:07:479] **Speaker 1:** Discretization for our time derivative dt by dt.
[00:38:07:530 - 00:38:10:010] **Speaker 1:** So that's why we've gone up to order 2, because
[00:38:10:010 - 00:38:11:540] **Speaker 1:** it's dividing by data t.
[00:38:12:189 - 00:38:15:169] **Speaker 1:** So we get back that order outity accuracy.
[00:38:16:810 - 00:38:21:929] **Speaker 1:** Uh, for the spatial terms, so Xi + 1 and
[00:38:21:929 - 00:38:24:090] **Speaker 1:** Xi minus 1, we're gonna have to go up to
[00:38:24:090 - 00:38:26:050] **Speaker 1:** the 4th order of terms.
[00:38:26:330 - 00:38:28:590] **Speaker 1:** So with rema remainder of that x 4.
[00:38:29:850 - 00:38:32:850] **Speaker 1:** So when it cancels with divides by data X2, we're
[00:38:32:850 - 00:38:35:449] **Speaker 1:** left with some order of accuracy scaling with data X2.
[00:38:36:419 - 00:38:37:850] **Speaker 1:** So there's more writing to do.
[00:38:38:310 - 00:38:38:790] **Speaker 1:** So T.
[00:38:39:760 - 00:38:42:840] **Speaker 1:** At XI + 1 TN.
[00:38:43:780 - 00:38:45:929] **Speaker 1:** It's gonna be TXITN.
[00:38:46:620 - 00:38:50:459] **Speaker 1:** So we're gonna approximate our temperature at I + 1
[00:38:50:459 - 00:38:51:419] **Speaker 1:** based on I.
[00:38:53:199 - 00:38:59:010] **Speaker 1:** So Taylor series, we've got data XDTI DX at the
[00:38:59:510 - 00:39:01:830] **Speaker 1:** spatial point XI time level TN.
[00:39:02:909 - 00:39:06:550] **Speaker 1:** Plus Delta X2 over 2.
[00:39:08:320 - 00:39:11:479] **Speaker 1:** D2T by DX2.
[00:39:12:449 - 00:39:13:739] **Speaker 1:** X I T N.
[00:39:16:709 - 00:39:22:159] **Speaker 1:** And then We've got data X cubed over 6.
[00:39:23:540 - 00:39:29:300] **Speaker 1:** D cubet by DX cubed, also XITN.
[00:39:30:570 - 00:39:33:620] **Speaker 1:** Plus some order of Days to power 4.
[00:39:37:590 - 00:39:38:629] **Speaker 1:** It's a 3.
[00:39:42:050 - 00:39:42:409] **Speaker 1:** Yeah.
[00:39:46:449 - 00:39:48:489] **Speaker 1:** So that last term that we wanna include into our
[00:39:48:489 - 00:39:51:489] **Speaker 1:** long equation is gonna be T.
[00:39:53:110 - 00:39:55:510] **Speaker 1:** X1 minus 1 TN.
[00:39:57:000 - 00:39:59:030] **Speaker 1:** And that's just gonna be exactly the same except it's
[00:39:59:030 - 00:40:01:429] **Speaker 1:** minus on the odd ones, we've got minus x and
[00:40:01:429 - 00:40:02:889] **Speaker 1:** minus x about 3.
[00:40:05:330 - 00:40:10:899] **Speaker 1:** So T X I T N minus X DT by
[00:40:10:899 - 00:40:17:239] **Speaker 1:** DX at XITN plus stat X squared over 2 D2T
[00:40:17:239 - 00:40:24:030] **Speaker 1:** by DX 2 XITN minus X cubed over 6.
[00:40:25:479 - 00:40:28:530] **Speaker 1:** D Q T Y D X cubed at X I
[00:40:28:530 - 00:40:32:110] **Speaker 1:** T N plus that order of data x 4.
[00:40:43:050 - 00:40:44:270] **Speaker 1:** So we expressed.
[00:40:45:530 - 00:40:50:889] **Speaker 1:** The temperatures at these discrete points, so X I TN
[00:40:50:889 - 00:40:51:969] **Speaker 1:** + 1, etc.
[00:40:52:250 - 00:40:54:550] **Speaker 1:** and we're gonna substitute that into our truncation error.
[00:40:59:800 - 00:41:08:260] **Speaker 0:** And I can give you a little bit of an
[00:41:08:260 - 00:41:09:530] **Speaker 1:** overview of what we're doing.
[00:41:09:620 - 00:41:13:080] **Speaker 1:** So we've got XITN +1.
[00:41:16:250 - 00:41:20:169] **Speaker 1:** minus TXITN, so that's gonna cancel and we're left with
[00:41:20:169 - 00:41:22:350] **Speaker 1:** data TDT by DT.
[00:41:24:189 - 00:41:27:310] **Speaker 1:** Divided by delta T, so those delta Ts cancel and
[00:41:27:310 - 00:41:33:669] **Speaker 1:** we're left with DT by DT at XITN.
[00:41:43:830 - 00:41:47:810] **Speaker 1:** Uh, so that is our first term.
[00:41:49:330 - 00:41:52:629] **Speaker 1:** The spatial term You've got minus alpha.
[00:41:53:820 - 00:41:58:189] **Speaker 1:** Multiplied by all these, all these terms.
[00:41:58:550 - 00:42:04:570] **Speaker 1:** So maybe, So we've got TI TXI plus 1.
[00:42:05:129 - 00:42:07:699] **Speaker 1:** So that's one T and then another T at Xi
[00:42:07:699 - 00:42:08:510] **Speaker 1:** minus 1.
[00:42:09:169 - 00:42:12:340] **Speaker 1:** So those are gonna cancel with this middle term 2
[00:42:13:050 - 00:42:14:250] **Speaker 1:** T X I TN.
[00:42:15:709 - 00:42:18:459] **Speaker 1:** And then we've got the first order derivatives.
[00:42:18:590 - 00:42:22:409] **Speaker 1:** They're gonna cancel with one another, Dax minus data X.
[00:42:23:270 - 00:42:27:929] **Speaker 1:** And then we've got 2/2 plus X2 over 2, so
[00:42:27:929 - 00:42:29:250] **Speaker 1:** that goes to 1.
[00:42:30:110 - 00:42:32:000] **Speaker 1:** And then it's divided by delta X2.
[00:42:33:149 - 00:42:37:290] **Speaker 1:** So the letter with D2T by DX2.
[00:42:38:739 - 00:42:40:090] **Speaker 1:** At XITN.
[00:42:44:110 - 00:42:45:580] **Speaker 1:** If you really wanted, you could write all of it
[00:42:45:580 - 00:42:48:550] **Speaker 1:** out and then cross them all off, but um we'll
[00:42:48:550 - 00:42:49:530] **Speaker 1:** just do it by sight.
[00:42:50:689 - 00:42:53:290] **Speaker 1:** So that is, well, what are the terms we've got
[00:42:53:290 - 00:42:56:379] **Speaker 1:** we've got this plus and minus x 3/6.
[00:42:56:449 - 00:42:58:709] **Speaker 1:** They cancel and we've got this remainder.
[00:42:59:169 - 00:43:03:120] **Speaker 1:** So the remainder terms we've got is of order X2.
[00:43:04:500 - 00:43:06:659] **Speaker 1:** Again, because we're dividing by delta X2, so it's gonna
[00:43:06:659 - 00:43:10:979] **Speaker 1:** scale with x2 overall, and we've got a time of
[00:43:10:979 - 00:43:11:550] **Speaker 1:** order delta T.
[00:43:15:010 - 00:43:15:409] **Speaker 1:** Cool.
[00:43:25:199 - 00:43:25:919] **Speaker 1:** So what have we done?
[00:43:26:000 - 00:43:27:459] **Speaker 1:** What are, what are we trying to prove here?
[00:43:28:040 - 00:43:29:580] **Speaker 1:** So as we refine.
[00:43:30:800 - 00:43:36:169] **Speaker 1:** Uh, spatial discretization delta X and the time discretization, the
[00:43:36:169 - 00:43:40:100] **Speaker 1:** time step data T as these 10 to 0, our
[00:43:40:100 - 00:43:40:790] **Speaker 1:** um.
[00:43:42:090 - 00:43:44:820] **Speaker 1:** Our equation is going to convert to the the heat
[00:43:44:820 - 00:43:45:320] **Speaker 1:** equation.
[00:43:50:959 - 00:43:53:580] **Speaker 1:** So in words, our forward and time central space scheme
[00:43:53:580 - 00:43:59:080] **Speaker 1:** is unconditionally consistent because as we take the limit of
[00:43:59:080 - 00:44:04:959] **Speaker 1:** T and X to 0, our truncation error is gonna
[00:44:04:959 - 00:44:05:479] **Speaker 1:** be zero.
[00:44:17:879 - 00:44:21:610] **Speaker 1:** And we know that because the heat equation is already
[00:44:21:610 - 00:44:22:590] **Speaker 1:** saying that this.
[00:44:23:760 - 00:44:26:689] **Speaker 1:** The term in brackets is equal to 0 by definition.
[00:44:29:439 - 00:44:32:879] **Speaker 1:** So I said that the discretize and continuous equations are
[00:44:32:879 - 00:44:36:679] **Speaker 1:** equivalent as we reduce the step size X and data.
[00:44:37:879 - 00:44:38:280] **Speaker 1:** Cool.
[00:44:39:040 - 00:44:42:879] **Speaker 1:** So the truncation error tau tau n is also uh
[00:44:42:879 - 00:44:45:479] **Speaker 1:** determining the order of the error in the numerical scheme.
[00:44:45:540 - 00:44:47:919] **Speaker 1:** So we saw that we've had these uh remainders of
[00:44:47:919 - 00:44:50:199] **Speaker 1:** data x have 2 and T.
[00:44:50:949 - 00:44:53:989] **Speaker 1:** So we've got uh quadratic convergence in X and then
[00:44:53:989 - 00:44:55:389] **Speaker 1:** linear convergence in time.
[00:44:56:969 - 00:44:59:530] **Speaker 1:** Uh, so we've got that, that order of 1 and
[00:44:59:530 - 00:44:59:929] **Speaker 1:** 2.
[00:45:03:290 - 00:45:03:689] **Speaker 1:** Cool.
[00:45:04:830 - 00:45:06:560] **Speaker 1:** Any questions on how we got to there?
[00:45:11:250 - 00:45:13:260] **Speaker 1:** No, it's just lots of terms.
[00:45:13:320 - 00:45:14:840] **Speaker 1:** I mean, it's not that scary.
[00:45:15:000 - 00:45:17:580] **Speaker 1:** It's just some Taylor series terms and sub-shooting.
[00:45:18:120 - 00:45:19:159] **Speaker 1:** But we're just showing that.
[00:45:20:189 - 00:45:22:669] **Speaker 1:** As we reduce the step sizes, we should, we should
[00:45:22:669 - 00:45:24:669] **Speaker 1:** converge and get a good, good result.
[00:45:24:830 - 00:45:27:580] **Speaker 1:** We're going to look at an example that doesn't doesn't
[00:45:27:580 - 00:45:28:050] **Speaker 1:** do that.
[00:45:28:469 - 00:45:30:570] **Speaker 1:** So um quite interesting.
[00:45:30:870 - 00:45:34:550] **Speaker 1:** So there's heaps of different numerical schemes we mainly just
[00:45:34:550 - 00:45:36:070] **Speaker 1:** doing the Ford and time back from time and crack
[00:45:36:070 - 00:45:37:429] **Speaker 1:** Nicholson for the heat equation.
[00:45:37:949 - 00:45:38:850] **Speaker 1:** But there are others.
[00:45:40:000 - 00:45:42:629] **Speaker 1:** One of these others is the Du Fort-Frankel numerical scheme.
[00:45:42:669 - 00:45:44:500] **Speaker 1:** So we're going to just show this as an example
[00:45:44:500 - 00:45:46:330] **Speaker 1:** of one that isn't consistent.
[00:45:48:310 - 00:45:50:830] **Speaker 1:** So this is another stencil for finite differencing.
[00:45:52:360 - 00:45:55:479] **Speaker 1:** Uh, that is essentially a central difference in time.
[00:45:55:639 - 00:46:01:679] **Speaker 1:** So we've got TIN + 1 minus TIN minus 1.
[00:46:05:209 - 00:46:06:850] **Speaker 1:** Was it a cattle or something?
[00:46:08:780 - 00:46:11:570] **Speaker 1:** Oh no, so we're good, right, so 2 out of.
[00:46:12:530 - 00:46:15:979] **Speaker 1:** Um So it's essentially central difference in time.
[00:46:16:020 - 00:46:19:219] **Speaker 1:** We've got TIN + 1 minus TIN minus 1 divided
[00:46:19:219 - 00:46:20:699] **Speaker 1:** by the interval to data.
[00:46:22:320 - 00:46:23:889] **Speaker 1:** The spatial term.
[00:46:24:919 - 00:46:28:239] **Speaker 1:** Has a similar structure, but alpha.
[00:46:29:409 - 00:46:32:689] **Speaker 1:** And we've got TIN + 1.
[00:46:35:560 - 00:46:39:360] **Speaker 1:** Minus, instead of 2 times TIN we've got.
[00:46:40:860 - 00:46:43:620] **Speaker 1:** TIN + 1.
[00:46:44:550 - 00:46:47:669] **Speaker 1:** And TIN minus 1.
[00:46:49:199 - 00:46:52:159] **Speaker 1:** So instead of evaluating that temperature value at the midpoint,
[00:46:52:280 - 00:46:55:100] **Speaker 1:** it's evaluating the map positive and negative data to.
[00:46:56:270 - 00:46:59:070] **Speaker 1:** And the last term is the same, TI minus 1.
[00:47:02:739 - 00:47:04:590] **Speaker 1:** And this is divided by data X2.
[00:47:06:600 - 00:47:08:209] **Speaker 1:** Make sure we finish on time today.
[00:47:09:280 - 00:47:10:300] **Speaker 1:** To, to let you out.
[00:47:10:760 - 00:47:16:449] **Speaker 1:** Um, so, This is very similar to our forward in
[00:47:16:449 - 00:47:19:250] **Speaker 1:** time sent in space, um, but it's different.
[00:47:19:330 - 00:47:21:969] **Speaker 1:** So the midpoint, uh, we've got these two values and
[00:47:21:969 - 00:47:23:290] **Speaker 1:** also TIN plus.
[00:47:23:810 - 00:47:24:570] **Speaker 1:** Oh, that's an error.
[00:47:24:810 - 00:47:25:169] **Speaker 1:** Sorry.
[00:47:29:629 - 00:47:33:830] **Speaker 1:** That's T I Plus one.
[00:47:35:020 - 00:47:36:939] **Speaker 1:** Put the +1 on the wrong one, so it's TI
[00:47:36:939 - 00:47:38:000] **Speaker 1:** + 1 at N.
[00:47:44:729 - 00:47:45:669] **Speaker 1:** TI + 1.
[00:47:46:090 - 00:47:46:360] **Speaker 1:** All right.
[00:47:46:570 - 00:47:47:409] **Speaker 1:** So it looks very similar.
[00:47:47:560 - 00:47:49:929] **Speaker 1:** The only difference is this midpoint is evaluating at the
[00:47:49:929 - 00:47:50:870] **Speaker 1:** next and previous time.
[00:47:51:949 - 00:47:54:129] **Speaker 1:** All right, so we're gonna apply the same consistency analysis
[00:47:54:129 - 00:47:54:770] **Speaker 1:** for the scheme.
[00:47:55:540 - 00:47:58:639] **Speaker 1:** Uh, and we're gonna find that the truncation error TN
[00:47:59:260 - 00:48:00:290] **Speaker 1:** is equal to.
[00:48:01:139 - 00:48:02:239] **Speaker 1:** I'll save you all the working.
[00:48:02:540 - 00:48:09:500] **Speaker 1:** So we've got DT by DT at XITN minus alpha.
[00:48:10:929 - 00:48:13:729] **Speaker 1:** D2T by DX2.
[00:48:14:479 - 00:48:17:060] **Speaker 1:** At XITN, so far so good.
[00:48:17:600 - 00:48:22:379] **Speaker 1:** But we also have an extra term alpha, T2 over
[00:48:22:770 - 00:48:30:360] **Speaker 1:** delta X2, D2T by DT2 at XITN.
[00:48:31:790 - 00:48:35:929] **Speaker 1:** And we've got other residuals of order.
[00:48:37:340 - 00:48:38:870] **Speaker 1:** Delta T2.
[00:48:40:340 - 00:48:46:110] **Speaker 1:** Of order X2, and another one of order T, the
[00:48:46:110 - 00:48:49:699] **Speaker 1:** power of 4 over X2.
[00:48:56:780 - 00:48:58:370] **Speaker 1:** So I'll give you a moment to write that out
[00:48:58:469 - 00:49:01:729] **Speaker 1:** and Um, I'll give you.
[00:49:03:110 - 00:49:05:040] **Speaker 1:** A couple of steps to think about why this might
[00:49:05:040 - 00:49:08:919] **Speaker 1:** not be uh consistent, and we'll continue that on Wednesday.
[00:49:13:570 - 00:49:18:879] **Speaker 1:** Yes TIN.
[00:49:31:399 - 00:49:33:830] **Speaker 1:** So, I mean, this is, we're, we're rearranging for TIN
[00:49:33:830 - 00:49:34:620] **Speaker 1:** plus one.
[00:49:34:870 - 00:49:36:389] **Speaker 1:** That's what we're aiming for.
[00:49:37:290 - 00:49:41:830] **Speaker 1:** We, it's not using TIN which is a good observation.
[00:49:42:449 - 00:49:44:209] **Speaker 1:** Um, so we're not going to include it in our
[00:49:44:209 - 00:49:45:870] **Speaker 1:** discretized equation.
[00:49:49:000 - 00:49:50:629] **Speaker 1:** But yeah, all of these, all we're trying to do
[00:49:50:629 - 00:49:52:020] **Speaker 1:** is, yeah, TIN plus one.
[00:49:52:850 - 00:49:54:280] **Speaker 1:** That's essentially what we was hoping for.
[00:49:55:810 - 00:49:57:610] **Speaker 1:** So you can see that's on both sides, we've got
[00:49:57:610 - 00:49:58:469] **Speaker 1:** another one over here.
[00:50:03:699 - 00:50:04:320] **Speaker 1:** Cool.
[00:50:04:820 - 00:50:07:550] **Speaker 1:** I'm keeping track of the time so there's no clock,
[00:50:07:820 - 00:50:08:540] **Speaker 1:** but yeah.
[00:50:09:560 - 00:50:10:280] **Speaker 1:** Cool.
[00:50:10:800 - 00:50:11:399] **Speaker 1:** All right.
[00:50:11:959 - 00:50:13:659] **Speaker 1:** So have a think about that and we can go
[00:50:13:659 - 00:50:15:979] **Speaker 1:** through the rest of the, the chapter on Wednesday.
[00:50:29:310 - 00:50:29:320] **Speaker 0:** OK.
[00:50:37:209 - 00:50:37:219] **Speaker 0:** it.
[00:51:03:199 - 00:51:05:370] **Speaker 0:** OK I.
[00:51:10:939 - 00:51:14:320] **Speaker 0:** Hey, I was wondering if you could get an extension
[00:51:14:320 - 00:51:15:340] **Speaker 0:** of last week's quiz.
[00:51:15:580 - 00:51:16:790] **Speaker 0:** I had a hockey tournament.
[00:51:17:370 - 00:51:19:300] **Speaker 1:** Oh right, yeah, if you email, yeah, send me an
[00:51:19:300 - 00:51:20:350] **Speaker 1:** email, yeah, yeah, yeah, yeah, yeah.
[00:51:21:209 - 00:51:24:260] **Speaker 1:** Was that for, um, like sport like national, yeah, national,
[00:51:24:379 - 00:51:25:610] **Speaker 1:** yeah, yeah, yeah, yeah, just send me an email.
[00:51:25:689 - 00:51:29:280] **Speaker 1:** I represented Manaa too, but, um, we almost got relegated.
[00:51:29:429 - 00:51:31:540] **Speaker 0:** Oh right, yeah, so it was a tough one.
[00:51:31:719 - 00:51:33:189] **Speaker 0:** Yeah, OK, yeah, I'll just email.
[00:51:35:899 - 00:51:40:560] **Speaker 0:** No, no, it's it.
[00:51:41:219 - 00:54:23:149] **Speaker 0:** I I There Oh No.
[00:54:50:040 - 00:54:50:770] **Speaker 0:** I know.
[00:54:52:649 - 00:54:55:100] **Speaker 0:** Uh, uh.
[00:54:58:100 - 00:54:58:379] **Speaker 0:** So

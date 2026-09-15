# ENME302-26S2 Lecture 27 native Echo transcript

Date: September 10, 2026 10:00am-10:55am
Transcript type: native Echo automated transcript.

[00:00:07:190 - 00:00:34:040] **Speaker 0:** just doesn't.
[00:00:35:950 - 00:00:37:069] **Speaker 1:** Uh, good morning class.
[00:00:37:150 - 00:00:38:090] **Speaker 1:** We'll make a start.
[00:00:39:029 - 00:00:41:990] **Speaker 1:** Are there any burning questions before we dive into our,
[00:00:42:389 - 00:00:43:110] **Speaker 1:** our lecture?
[00:00:45:310 - 00:00:49:509] **Speaker 1:** N Alright, so, uh, this afternoon we're gonna go through
[00:00:49:509 - 00:00:53:779] **Speaker 1:** lab two in the, um, course reader, so page 134.
[00:00:54:400 - 00:00:58:610] **Speaker 1:** Uh, so most of these, Questions or instructions are within
[00:00:58:610 - 00:01:01:049] **Speaker 1:** the course reader rather than going to an external PDF,
[00:01:01:610 - 00:01:03:970] **Speaker 1:** um, but follow along.
[00:01:04:330 - 00:01:06:410] **Speaker 1:** So we're gonna look at a tapered cantilever and look
[00:01:06:410 - 00:01:07:949] **Speaker 1:** at a couple of different loading cases.
[00:01:08:610 - 00:01:10:290] **Speaker 1:** So this is a stress distribution.
[00:01:11:110 - 00:01:12:160] **Speaker 1:** Within the cantilever.
[00:01:13:099 - 00:01:15:819] **Speaker 1:** Uh, we're looking at different meshes, so you'll look at
[00:01:15:819 - 00:01:19:940] **Speaker 1:** the, uh, untructed triangular mesh, Delaunay mesh.
[00:01:20:669 - 00:01:22:129] **Speaker 1:** And also they're structured.
[00:01:23:690 - 00:01:25:779] **Speaker 1:** So this is a free quad mesh, so it's not
[00:01:25:779 - 00:01:27:290] **Speaker 1:** structured, but it has quadrilateral elements.
[00:01:28:300 - 00:01:30:099] **Speaker 1:** And then we've got the mat mesh and we're also
[00:01:30:099 - 00:01:31:639] **Speaker 1:** looking at some refinement as well.
[00:01:32:529 - 00:01:37:779] **Speaker 1:** So Uh, other refinement can include, include a region, so
[00:01:37:779 - 00:01:41:080] **Speaker 1:** on the bottom right we've refined the mesh further.
[00:01:41:540 - 00:01:43:660] **Speaker 1:** Uh, we'll also talk a little bit about swept meshing.
[00:01:44:430 - 00:01:49:129] **Speaker 1:** And then Applied that slip mesh machine, so essentially you're,
[00:01:49:300 - 00:01:51:970] **Speaker 1:** you're meshing one face and then sweeping it across the
[00:01:51:970 - 00:01:53:360] **Speaker 1:** domain in the other direction.
[00:01:54:410 - 00:01:57:849] **Speaker 1:** And that last example, the feeder clamp, um, is a
[00:01:57:849 - 00:01:59:860] **Speaker 1:** tutorial, so you can just open the model file, you
[00:01:59:860 - 00:02:02:500] **Speaker 1:** don't have to go through the geometry steps, uh, it's
[00:02:02:500 - 00:02:05:300] **Speaker 1:** quite, quite painful, so don't do that.
[00:02:07:150 - 00:02:09:389] **Speaker 1:** Um, but you can if you wish, but it just
[00:02:09:389 - 00:02:10:210] **Speaker 1:** takes a bit longer.
[00:02:10:789 - 00:02:12:710] **Speaker 1:** Uh, so there's some more steps, and essentially we want
[00:02:12:710 - 00:02:17:990] **Speaker 1:** to compare structured versus unstructured measures and the accuracy.
[00:02:18:110 - 00:02:21:589] **Speaker 1:** So is an unstructured grid more or less accurate than
[00:02:21:589 - 00:02:23:949] **Speaker 1:** a structured grid for the same number of degrees of
[00:02:23:949 - 00:02:26:619] **Speaker 1:** freedom or the same number of, um, equations that we're
[00:02:26:619 - 00:02:27:250] **Speaker 1:** solving for?
[00:02:28:220 - 00:02:28:869] **Speaker 1:** It's that.
[00:02:29:529 - 00:02:31:550] **Speaker 1:** The gist of what you're doing today in the labs.
[00:02:36:529 - 00:02:39:089] **Speaker 1:** Any question on console, so you'll use these for the
[00:02:39:089 - 00:02:41:750] **Speaker 1:** quiz that I showed you earlier in the week, um,
[00:02:42:130 - 00:02:43:309] **Speaker 1:** those last two questions.
[00:02:45:580 - 00:02:47:449] **Speaker 1:** So it should be pretty straightforward if you've done the
[00:02:47:589 - 00:02:48:289] **Speaker 1:** the console there.
[00:02:51:660 - 00:02:52:779] **Speaker 1:** All right, cool.
[00:02:53:059 - 00:02:54:300] **Speaker 1:** We'll continue with chapter 4.
[00:02:54:660 - 00:02:58:500] **Speaker 1:** So, in chapter 3, we use finite differenceferencing, so page
[00:02:58:500 - 00:02:59:759] **Speaker 1:** 135.
[00:03:00:750 - 00:03:04:380] **Speaker 1:** So, uh, yeah, yesterday we were looking at chapter 3.
[00:03:04:619 - 00:03:06:600] **Speaker 1:** We derived that system of equations.
[00:03:07:059 - 00:03:09:940] **Speaker 1:** So we had an equation for each node and we
[00:03:09:940 - 00:03:13:460] **Speaker 1:** solved that just using the L solve in Python.
[00:03:14:149 - 00:03:15:789] **Speaker 1:** So there's some other techniques that we can use to
[00:03:15:789 - 00:03:17:309] **Speaker 1:** solve a system of equations, and that's what we're going
[00:03:17:309 - 00:03:18:130] **Speaker 1:** to talk about today.
[00:03:19:529 - 00:03:21:360] **Speaker 1:** So we're gonna talk about the Liebman method.
[00:03:22:860 - 00:03:25:339] **Speaker 1:** As a nice iterative scheme to solve that system of
[00:03:25:339 - 00:03:26:080] **Speaker 1:** equations.
[00:03:28:009 - 00:03:30:250] **Speaker 1:** So we discretized our heat equation and we had that
[00:03:30:250 - 00:03:33:289] **Speaker 1:** system of uh of equations, equation 3:15.
[00:03:35:289 - 00:03:37:740] **Speaker 1:** We only had 9 unknowns or degrees of freedom.
[00:03:38:699 - 00:03:41:580] **Speaker 1:** So frequently we'll have more degrees of freedom than that.
[00:03:41:660 - 00:03:45:059] **Speaker 1:** So the venture example that you did last week, uh,
[00:03:45:880 - 00:03:49:440] **Speaker 1:** Week 6, a few weeks ago now, um, had maybe
[00:03:49:440 - 00:03:51:559] **Speaker 1:** tens or hundreds of thousands of degrees of freedom, so
[00:03:51:559 - 00:03:53:919] **Speaker 1:** that's how many equations that console is solving.
[00:03:55:070 - 00:03:56:509] **Speaker 1:** So much larger systems.
[00:03:57:110 - 00:03:59:110] **Speaker 1:** So if we had a heat equation on a 20
[00:03:59:110 - 00:04:01:869] **Speaker 1:** by 20 grid, we would have 400 unknowns.
[00:04:02:149 - 00:04:05:610] **Speaker 1:** So 400 nodes, 400 equations to solve.
[00:04:06:270 - 00:04:09:429] **Speaker 1:** So the matrix of coefficients A, which we looked at
[00:04:09:429 - 00:04:14:130] **Speaker 1:** last time was a Oh, I can help you pull
[00:04:14:130 - 00:04:14:509] **Speaker 1:** it out.
[00:04:15:160 - 00:04:16:959] **Speaker 1:** From notes.
[00:04:26:529 - 00:04:31:010] **Speaker 1:** We had a 5x5 matrix for those 5 equations, so
[00:04:31:010 - 00:04:34:329] **Speaker 1:** we had 25 entries, so immediately it can already get
[00:04:34:329 - 00:04:35:029] **Speaker 1:** quite large.
[00:04:35:790 - 00:04:38:829] **Speaker 1:** So if we had 400 unknowns, we'd have 400 squared
[00:04:38:829 - 00:04:40:549] **Speaker 1:** entries, 400 by 400.
[00:04:42:540 - 00:04:44:540] **Speaker 1:** But most of this matrix is empty.
[00:04:44:869 - 00:04:48:390] **Speaker 1:** We observed that we had that pentadiagonal shape for the
[00:04:48:390 - 00:04:50:589] **Speaker 1:** 2D matrix.
[00:04:50:950 - 00:04:52:380] **Speaker 1:** This is our system of equations.
[00:04:52:510 - 00:04:55:089] **Speaker 1:** We converted it to matrix form, and we had that
[00:04:55:089 - 00:04:56:070] **Speaker 1:** penta diagonal.
[00:04:58:179 - 00:05:02:140] **Speaker 1:** Um, matrix of coefficients A, so most of the entries
[00:05:02:140 - 00:05:03:420] **Speaker 1:** within the matrix is going to be zero.
[00:05:04:510 - 00:05:06:459] **Speaker 1:** So it's not going to be very efficient use of
[00:05:06:459 - 00:05:09:859] **Speaker 1:** space or compute resources if we have a really large
[00:05:09:859 - 00:05:11:619] **Speaker 1:** matrix that is mostly zeros.
[00:05:13:970 - 00:05:15:910] **Speaker 1:** So inefficient use of computer memory.
[00:05:17:260 - 00:05:19:029] **Speaker 1:** So these direct solution methods.
[00:05:20:049 - 00:05:22:619] **Speaker 1:** Require the full storage of our matrix A.
[00:05:23:510 - 00:05:26:730] **Speaker 1:** And that includes calcium elimination or lower upper decomposition.
[00:05:28:179 - 00:05:30:100] **Speaker 1:** So some of these you you you've covered earlier in
[00:05:30:100 - 00:05:30:700] **Speaker 1:** math courses.
[00:05:31:019 - 00:05:35:459] **Speaker 1:** So an alternative to uh these direct or coupled fully
[00:05:35:459 - 00:05:37:769] **Speaker 1:** coupled systems, we can use an iterative scheme.
[00:05:38:179 - 00:05:39:440] **Speaker 1:** So the Gauss-Sider method.
[00:05:40:570 - 00:05:44:290] **Speaker 1:** Is going to be applied um for our PDEs and
[00:05:44:290 - 00:05:45:980] **Speaker 1:** we're gonna label this the Lieben method.
[00:05:47:970 - 00:05:51:329] **Speaker 1:** So you might see Gau-Sidel or Liebmann method, that's sort
[00:05:51:329 - 00:05:53:750] **Speaker 1:** of the same or very similar method.
[00:05:54:250 - 00:05:56:359] **Speaker 1:** So the idea is that we start from an initial
[00:05:56:359 - 00:05:58:209] **Speaker 1:** guess to our solution.
[00:05:58:970 - 00:06:01:640] **Speaker 1:** And then iteratively try to improve on that, yes.
[00:06:03:250 - 00:06:05:690] **Speaker 1:** So we need some more equations to solve, so we're
[00:06:05:690 - 00:06:07:690] **Speaker 1:** going to rewrite our equation 314.
[00:06:15:640 - 00:06:18:399] **Speaker 1:** Which we derived for.
[00:06:19:040 - 00:06:22:399] **Speaker 1:** A uniform grid, we had that x equal toy spacing
[00:06:22:399 - 00:06:26:269] **Speaker 1:** and we simplified it to our temperature, essentially being an
[00:06:26:269 - 00:06:28:220] **Speaker 1:** average of the neighbouring nodes.
[00:06:28:670 - 00:06:31:579] **Speaker 1:** So we want to rearrange for point IJ.
[00:06:32:399 - 00:06:33:320] **Speaker 1:** That's our first step.
[00:06:39:100 - 00:06:44:070] **Speaker 1:** And rearranging We've got the other 4 nodes divided by
[00:06:44:070 - 00:06:44:429] **Speaker 1:** 4.
[00:06:44:690 - 00:06:45:529] **Speaker 1:** So we've got T.
[00:06:47:040 - 00:06:48:399] **Speaker 1:** I + 1, J.
[00:06:49:230 - 00:06:55:350] **Speaker 1:** TI minus 1 JTIJ plus 1 and TIJ minus 1.
[00:06:56:359 - 00:06:57:220] **Speaker 1:** Divided by 4.
[00:07:00:959 - 00:07:04:170] **Speaker 1:** And I mean, that's directly just the average of the
[00:07:04:170 - 00:07:04:890] **Speaker 1:** neighbouring nodes.
[00:07:05:170 - 00:07:08:529] **Speaker 1:** Uh, so for a uniform grid for our heat equation,
[00:07:08:619 - 00:07:11:350] **Speaker 1:** for so the plus equation, it's fully diffuse, it's just
[00:07:11:750 - 00:07:14:230] **Speaker 1:** representing the average temperature of the neighbouring nodes.
[00:07:18:260 - 00:07:20:779] **Speaker 1:** So our temperature at all of the nodes, RJ representing
[00:07:20:779 - 00:07:24:339] **Speaker 1:** an individual node of those interior points, we're going to
[00:07:24:339 - 00:07:27:649] **Speaker 1:** iteratively update the estimate for TIJ.
[00:07:31:320 - 00:07:35:670] **Speaker 1:** Now I guess we've we've stated it here, but just
[00:07:35:670 - 00:07:37:809] **Speaker 1:** to be explicit, so the most recent estimate.
[00:07:39:170 - 00:07:40:209] **Speaker 1:** Of the temperature.
[00:07:41:190 - 00:07:43:160] **Speaker 1:** is used on that right hand side of the equation.
[00:07:45:720 - 00:07:49:000] **Speaker 1:** So if we go back to our sample.
[00:07:52:630 - 00:07:55:829] **Speaker 1:** If we had a node at T22, we were taking
[00:07:55:829 - 00:07:58:290] **Speaker 1:** the average of these four neighbouring nodes.
[00:07:59:320 - 00:08:01:959] **Speaker 1:** When we went to 3.2, we would have an updated
[00:08:01:959 - 00:08:06:149] **Speaker 1:** version for the temperature, uh, guest at 22.
[00:08:06:489 - 00:08:08:119] **Speaker 1:** So we're always using the latest information.
[00:08:08:480 - 00:08:09:839] **Speaker 1:** So in terms of coding, you can think of it
[00:08:09:839 - 00:08:12:510] **Speaker 1:** as just having an array of temperature values.
[00:08:12:720 - 00:08:14:160] **Speaker 1:** You don't need to keep track of what was the
[00:08:14:160 - 00:08:15:519] **Speaker 1:** last term.
[00:08:15:679 - 00:08:18:359] **Speaker 1:** You just keep track of the current temperature estimate.
[00:08:20:500 - 00:08:22:480] **Speaker 1:** And it helps with convergence as well.
[00:08:24:239 - 00:08:26:179] **Speaker 1:** So we'll go through an example, cos.
[00:08:27:130 - 00:08:28:750] **Speaker 1:** Maybe my descriptions aren't the best.
[00:08:29:239 - 00:08:33:359] **Speaker 1:** So considering our system of equations, 315 and assuming a
[00:08:33:359 - 00:08:35:390] **Speaker 1:** zero temperature is an initial guess.
[00:08:36:609 - 00:08:39:010] **Speaker 1:** So we had a boundary condition of zero on the
[00:08:39:010 - 00:08:39:479] **Speaker 1:** bottom.
[00:08:40:250 - 00:08:42:780] **Speaker 1:** Because it's the Laplace equation, it's fully diffuse, we know
[00:08:42:780 - 00:08:45:299] **Speaker 1:** that the temperature field within the domain has to be
[00:08:45:299 - 00:08:47:210] **Speaker 1:** bounded by these boundary conditions.
[00:08:47:750 - 00:08:51:190] **Speaker 1:** So it doesn't make sense to have -100 or 300
[00:08:51:299 - 00:08:52:520] **Speaker 1:** as your starting guess.
[00:08:53:140 - 00:08:54:900] **Speaker 1:** Maybe a better guess would be the average, but we're
[00:08:54:900 - 00:08:55:820] **Speaker 1:** going to start with 0.
[00:09:01:799 - 00:09:04:440] **Speaker 1:** So we'll start with that node at 22.
[00:09:10:750 - 00:09:12:789] **Speaker 1:** And maybe it's helpful to have that.
[00:09:13:479 - 00:09:17:000] **Speaker 1:** Well So node 22 is gonna be the average of
[00:09:17:000 - 00:09:19:260] **Speaker 1:** 233221, and 12.
[00:09:19:799 - 00:09:23:179] **Speaker 1:** So we're left with uh 75 for the lymph node.
[00:09:24:400 - 00:09:25:690] **Speaker 1:** Which is our boundary condition.
[00:09:27:669 - 00:09:30:789] **Speaker 1:** And we've got D32.
[00:09:34:539 - 00:09:39:099] **Speaker 1:** And then we've got D21, which is 0 on our
[00:09:39:099 - 00:09:39:770] **Speaker 1:** boundary.
[00:09:41:289 - 00:09:43:330] **Speaker 1:** And on the top, D 23.
[00:09:47:179 - 00:09:48:640] **Speaker 1:** Divided by 4.
[00:09:53:369 - 00:09:55:450] **Speaker 1:** So again, 75 and 0 are boundary conditions.
[00:09:55:510 - 00:09:57:979] **Speaker 1:** They're not going to change over time or iterations, they're
[00:09:57:979 - 00:09:58:609] **Speaker 1:** just fixed.
[00:09:59:010 - 00:10:00:809] **Speaker 1:** The only ones that are going to be varying are
[00:10:00:809 - 00:10:04:510] **Speaker 1:** the temperature variables or degrees of freedom, D32 and T23.
[00:10:05:130 - 00:10:09:049] **Speaker 1:** We can evaluate this expression and get 18.75.
[00:10:10:440 - 00:10:11:280] **Speaker 1:** Degrees Celsius.
[00:10:14:179 - 00:10:17:830] **Speaker 1:** Right We'll continue along this row.
[00:10:18:190 - 00:10:20:429] **Speaker 1:** So we'll next go with node 32.
[00:10:23:830 - 00:10:26:390] **Speaker 1:** So 32, we've got 22.
[00:10:36:659 - 00:10:38:070] **Speaker 1:** Uh, I've got T42.
[00:10:41:940 - 00:10:46:559] **Speaker 1:** We've got 0 And we have T33.
[00:10:52:859 - 00:10:53:700] **Speaker 1:** Divided by 4.
[00:11:06:789 - 00:11:09:809] **Speaker 1:** Um, maybe write smaller, I'm gonna squish in another fraction,
[00:11:10:270 - 00:11:16:250] **Speaker 1:** um, so we've got, An estimate for T22 of 18.75
[00:11:16:909 - 00:11:20:179] **Speaker 1:** and we're going to use that at our subsequent iteration.
[00:11:20:229 - 00:11:23:849] **Speaker 1:** So T22 is equal to 18.75, so make that substitution.
[00:11:27:659 - 00:11:32:969] **Speaker 1:** Tier 42 It is unknown at the moment and our
[00:11:32:969 - 00:11:34:549] **Speaker 1:** initial guess was 0.
[00:11:34:909 - 00:11:35:830] **Speaker 1:** So it's + 0.
[00:11:37:549 - 00:11:40:159] **Speaker 1:** Plus the boundary condition at the bottom of 0 and
[00:11:40:159 - 00:11:44:039] **Speaker 1:** T33 is also zero, you don't know.
[00:11:49:409 - 00:11:50:630] **Speaker 1:** And we can evaluate this.
[00:11:51:909 - 00:11:53:739] **Speaker 1:** Fraction and we're left with 4.
[00:11:56:960 - 00:12:00:320] **Speaker 1:** Um, I'll write a vertical 4.
[00:12:01:200 - 00:12:04:059] **Speaker 1:** 0.6875.
[00:12:06:830 - 00:12:08:390] **Speaker 1:** It's a bit unconventional, but.
[00:12:09:489 - 00:12:10:890] **Speaker 1:** Alright, T42.
[00:12:14:369 - 00:12:15:820] **Speaker 1:** I'll try to write smaller.
[00:12:17:359 - 00:12:20:659] **Speaker 1:** Um, so T42 is the one on the far right
[00:12:20:659 - 00:12:21:659] **Speaker 1:** of the bottom row.
[00:12:22:679 - 00:12:25:250] **Speaker 1:** Again, we don't evaluate 52 because that's the boundary of
[00:12:25:250 - 00:12:26:109] **Speaker 1:** 50 degrees.
[00:12:26:609 - 00:12:28:570] **Speaker 1:** So we have T32.
[00:12:31:590 - 00:12:33:890] **Speaker 1:** Uh, 52, which we just said was 50.
[00:12:35:030 - 00:12:38:270] **Speaker 1:** 0 NT 43.
[00:12:41:580 - 00:12:45:840] **Speaker 1:** Now we've just evaluated node 32 equal to 4.
[00:12:46:750 - 00:12:49:940] **Speaker 1:** 0.6875.
[00:12:53:380 - 00:12:54:659] **Speaker 1:** And we don't know what 43 is.
[00:12:54:780 - 00:12:56:880] **Speaker 1:** This is initial guess of 0.
[00:12:58:349 - 00:12:59:530] **Speaker 1:** Divided by 4.
[00:13:01:130 - 00:13:04:049] **Speaker 1:** And we evaluate to 13.672.
[00:13:06:280 - 00:13:07:650] **Speaker 1:** So we've done those lower 3 nodes.
[00:13:07:690 - 00:13:09:609] **Speaker 1:** We can do the same for the upper 3 and
[00:13:09:609 - 00:13:12:609] **Speaker 1:** upper 3 or mid 3 and upper 3 nodes.
[00:13:12:929 - 00:13:16:609] **Speaker 1:** So we've got 9 equations, 9 iterative steps.
[00:13:19:159 - 00:13:22:830] **Speaker 1:** Once we've done all 9 nodes, that's 1 iteration.
[00:13:24:640 - 00:13:28:760] **Speaker 1:** So this process is repeated multiple times, and then we
[00:13:28:760 - 00:13:30:140] **Speaker 1:** sort of have to decide when to finish.
[00:13:30:440 - 00:13:31:440] **Speaker 1:** We could just go on forever.
[00:13:32:830 - 00:13:38:390] **Speaker 1:** So what we're going to do is label one iteration
[00:13:38:390 - 00:13:39:510] **Speaker 1:** as T new.
[00:13:39:989 - 00:13:44:369] **Speaker 1:** So TIJ superscript new for the new computer value and
[00:13:44:369 - 00:13:45:609] **Speaker 1:** the old, the old one.
[00:13:46:469 - 00:13:48:950] **Speaker 1:** And we're going to define the relative error.
[00:13:49:700 - 00:13:53:059] **Speaker 1:** By comparing one iteration to the next, so new and
[00:13:53:059 - 00:13:53:500] **Speaker 1:** old.
[00:14:05:400 - 00:14:08:520] **Speaker 1:** So epsilon IJ is gonna be our relative error.
[00:14:09:780 - 00:14:11:859] **Speaker 1:** Which is defined as the tea.
[00:14:13:309 - 00:14:13:710] **Speaker 1:** New.
[00:14:15:390 - 00:14:20:330] **Speaker 1:** Minus T old, scaled by T.
[00:14:21:330 - 00:14:24:780] **Speaker 1:** New And we'll just take the absolute value of this,
[00:14:25:000 - 00:14:26:489] **Speaker 1:** so that it's always a positive value.
[00:14:36:000 - 00:14:38:719] **Speaker 1:** Now we've got an error representing each node.
[00:14:39:669 - 00:14:42:169] **Speaker 1:** Or how, how much is varied between each iterations.
[00:14:42:669 - 00:14:45:320] **Speaker 1:** To have one value to compare against maybe a set
[00:14:45:320 - 00:14:50:700] **Speaker 1:** tolerance, we're going to take, um, Norm of the relative
[00:14:50:700 - 00:14:54:590] **Speaker 1:** error, so essentially root means squared, so we've got epsilon.
[00:14:55:979 - 00:14:57:659] **Speaker 1:** Norm with the double bars.
[00:14:58:659 - 00:15:04:559] **Speaker 1:** Is equal to Some of all of our nodes, all
[00:15:04:559 - 00:15:05:280] **Speaker 1:** IJ.
[00:15:07:359 - 00:15:11:729] **Speaker 1:** We take epsilon IJ, our relative error for each node,
[00:15:11:880 - 00:15:17:900] **Speaker 1:** square, And then square root So this is the norm
[00:15:17:900 - 00:15:19:289] **Speaker 1:** of of the relative error.
[00:15:20:330 - 00:15:23:559] **Speaker 1:** Another technique is just looking at the maximum error, so.
[00:15:45:239 - 00:15:47:429] **Speaker 1:** And if we wanted a percent, we'd times it by
[00:15:47:429 - 00:15:48:000] **Speaker 1:** 100.
[00:16:02:750 - 00:16:05:909] **Speaker 1:** So when this relative error, or the norm of the
[00:16:05:909 - 00:16:06:549] **Speaker 1:** relative error.
[00:16:07:280 - 00:16:10:539] **Speaker 1:** Reaches some threshold, maybe it's 10 to 3.1%, something like
[00:16:10:539 - 00:16:14:450] **Speaker 1:** that, we can say that a convergence is achieved.
[00:16:16:510 - 00:16:19:030] **Speaker 1:** So that's when we can stop our, our coding.
[00:16:21:200 - 00:16:24:570] **Speaker 1:** So this system or this method is best suited for
[00:16:24:570 - 00:16:26:049] **Speaker 1:** systems that are diagonally dominant.
[00:16:26:789 - 00:16:29:429] **Speaker 1:** For example, the one we just showed with that heterodiagonal
[00:16:30:010 - 00:16:32:890] **Speaker 1:** matrix coefficients A for the 2D heat equation.
[00:16:38:349 - 00:16:43:849] **Speaker 1:** All right So maybe we can compare.
[00:16:45:229 - 00:16:48:450] **Speaker 1:** Our nodal values along the bottom.
[00:16:49:690 - 00:16:51:599] **Speaker 1:** Against what we calculated directly.
[00:16:52:510 - 00:16:55:020] **Speaker 1:** So we had 18.75 compared to 43.
[00:16:56:000 - 00:17:02:000] **Speaker 1:** 4.7 versus 33 and 13.7 versus 33.9, so they're still
[00:17:02:000 - 00:17:04:819] **Speaker 1:** quite far away from the converged solution, so we'd probably
[00:17:04:819 - 00:17:07:319] **Speaker 1:** expect quite a few iterations before it reaches those those
[00:17:07:319 - 00:17:08:140] **Speaker 1:** final values.
[00:17:09:188 - 00:17:11:790] **Speaker 1:** Um, so if it's kind of slow, we might want
[00:17:11:790 - 00:17:13:209] **Speaker 1:** to improve that speed.
[00:17:13:630 - 00:17:16:209] **Speaker 1:** So one way of doing that is to use over
[00:17:16:209 - 00:17:16:989] **Speaker 1:** relaxation.
[00:17:19:808 - 00:17:22:869] **Speaker 1:** So over relaxation is essentially just pushing the, the next
[00:17:22:869 - 00:17:27:198] **Speaker 1:** guest further away or closer towards the, um, the true
[00:17:27:198 - 00:17:27:698] **Speaker 1:** solution.
[00:17:28:159 - 00:17:29:298] **Speaker 1:** So it's giving a bit of a bump.
[00:17:29:468 - 00:17:31:838] **Speaker 1:** I mean you can use under relaxation if it's not
[00:17:31:838 - 00:17:34:838] **Speaker 1:** converging well in other scenarios, but in this case, we're
[00:17:34:838 - 00:17:37:948] **Speaker 1:** using over relaxation and this is defined with T.
[00:17:39:670 - 00:17:41:069] **Speaker 1:** I knew.
[00:17:45:979 - 00:17:47:979] **Speaker 1:** There's going to be a waiting between.
[00:17:50:310 - 00:17:51:550] **Speaker 1:** What we've just calculated.
[00:17:54:479 - 00:18:00:880] **Speaker 1:** TIJ new star multiplied by some factor lambda, and this
[00:18:00:880 - 00:18:02:359] **Speaker 1:** is the over relaxation factor.
[00:18:04:079 - 00:18:05:369] **Speaker 1:** Which is between 1 and 2.
[00:18:06:619 - 00:18:09:510] **Speaker 1:** Plus 1 minus lambda.
[00:18:10:449 - 00:18:13:530] **Speaker 1:** Multiplied by TIJ old.
[00:18:15:640 - 00:18:19:229] **Speaker 1:** So from this equation we can see that it's biassing
[00:18:19:969 - 00:18:24:290] **Speaker 1:** more towards the next estimate and being pulled back by
[00:18:24:290 - 00:18:24:849] **Speaker 1:** the old.
[00:18:25:250 - 00:18:29:949] **Speaker 1:** So if lambda is equal to one, Then we just
[00:18:29:949 - 00:18:33:760] **Speaker 1:** have TIJ equal to TIJ new star.
[00:18:34:280 - 00:18:37:119] **Speaker 1:** If you have really high over relaxation factor value, then
[00:18:37:119 - 00:18:41:760] **Speaker 1:** it's pushing it higher for TIJ new star.
[00:18:42:439 - 00:18:48:739] **Speaker 1:** So I just want to say that TIJ new star.
[00:18:49:520 - 00:18:53:800] **Speaker 1:** Is Just an intermediate or auxiliary variable.
[00:19:01:380 - 00:19:03:780] **Speaker 1:** Um, that we just calculated from Liebman's method.
[00:19:09:680 - 00:19:11:770] **Speaker 1:** Depending on how you code it, you might not actually
[00:19:11:770 - 00:19:14:849] **Speaker 1:** define that star or that auxiliary variable and just go
[00:19:14:849 - 00:19:19:420] **Speaker 1:** straight to the, Equation 4.4, so otherwise we run out
[00:19:19:420 - 00:19:22:219] **Speaker 1:** of too many variable names and subscripts and superscripts.
[00:19:26:540 - 00:19:28:969] **Speaker 1:** So we're gonna do an example and apply an over
[00:19:28:969 - 00:19:31:729] **Speaker 1:** relaxation factor of 1.5 and see whether or not we
[00:19:31:729 - 00:19:34:050] **Speaker 1:** get closer to that converged solution quicker.
[00:19:34:900 - 00:19:37:670] **Speaker 1:** So T22 new.
[00:19:39:910 - 00:19:42:709] **Speaker 1:** is now equal to the over relaxation factor of 1.5.
[00:19:42:829 - 00:19:46:109] **Speaker 1:** Again, it's between 1 and 2.1 essentially disables the over
[00:19:46:109 - 00:19:48:689] **Speaker 1:** relaxation and getting close to 2 is the upper limit
[00:19:48:689 - 00:19:49:849] **Speaker 1:** and might be unstable.
[00:19:51:079 - 00:19:53:650] **Speaker 1:** So we've got 1.5 multiplied.
[00:19:54:859 - 00:19:57:520] **Speaker 1:** By our estimate from Lee Lieb's method.
[00:19:58:489 - 00:20:01:349] **Speaker 1:** So that was from the top of that page.
[00:20:02:819 - 00:20:04:119] **Speaker 1:** So we've got 75.
[00:20:06:300 - 00:20:07:500] **Speaker 1:** 32.
[00:20:08:589 - 00:20:12:150] **Speaker 1:** Plus 0 + D +23 divided by 4.
[00:20:19:109 - 00:20:21:660] **Speaker 1:** Plus 1 minus 1.5.
[00:20:23:119 - 00:20:26:760] **Speaker 1:** So 1 minus lambda, 1.5, and then TIJ old, so
[00:20:26:760 - 00:20:27:000] **Speaker 1:** T.
[00:20:28:189 - 00:20:30:310] **Speaker 1:** To, to hold.
[00:20:35:819 - 00:20:39:300] **Speaker 1:** So on that first iteration, T22 old will just be
[00:20:39:300 - 00:20:39:770] **Speaker 1:** zero.
[00:20:39:939 - 00:20:41:040] **Speaker 1:** That's our initial guess.
[00:20:42:670 - 00:20:46:550] **Speaker 1:** And essentially we've got 1.5 times 18.7, which is going
[00:20:46:550 - 00:20:50:550] **Speaker 1:** to be 28.125.
[00:20:54:530 - 00:20:56:119] **Speaker 1:** So don't worry too much about doing.
[00:20:57:209 - 00:20:59:900] **Speaker 1:** Arithmetic, we can let Python do that for us.
[00:21:03:699 - 00:21:05:439] **Speaker 1:** So 28.125.
[00:21:07:020 - 00:21:09:540] **Speaker 1:** Compared to 18.75 is a lot better.
[00:21:09:819 - 00:21:13:500] **Speaker 1:** I mean, we, we're trying to get to 43, so
[00:21:13:579 - 00:21:14:130] **Speaker 1:** that's better.
[00:21:15:170 - 00:21:15:780] **Speaker 1:** Much better.
[00:21:18:300 - 00:21:20:920] **Speaker 1:** For completeness, we're going to do another node at T32.
[00:21:26:489 - 00:21:31:189] **Speaker 1:** T Applying that same over relaxation of 1.5.
[00:21:34:089 - 00:21:37:290] **Speaker 1:** Now the Lieben method, we did it that just earlier.
[00:21:37:640 - 00:21:39:910] **Speaker 1:** So we've got T22.
[00:21:43:430 - 00:21:44:790] **Speaker 1:** 42.
[00:21:45:979 - 00:21:49:479] **Speaker 1:** 0 NT 33.
[00:21:50:869 - 00:22:00:109] **Speaker 1:** Divided by 4 And 1 minus 1.5 times T320.
[00:22:09:339 - 00:22:14:810] **Speaker 1:** We've just calculated T22 again to be 28.1, so we
[00:22:14:810 - 00:22:18:359] **Speaker 1:** can insert that into our, Uh, leave method.
[00:22:19:859 - 00:22:22:760] **Speaker 1:** And we're ending up with 10.5.
[00:22:24:400 - 00:22:26:000] **Speaker 1:** 47.
[00:22:34:069 - 00:22:38:209] **Speaker 1:** So, yeah, applying over relaxation is getting to the solution
[00:22:38:209 - 00:22:40:180] **Speaker 1:** quicker, so we use fewer iterations.
[00:22:40:260 - 00:22:42:579] **Speaker 1:** We haven't really used that much more computing power.
[00:22:42:739 - 00:22:46:119] **Speaker 1:** We had to evaluate this expression 1 minus 1.5 times
[00:22:46:119 - 00:22:48:239] **Speaker 1:** T3 too old, but that's not too expensive.
[00:22:49:160 - 00:22:54:150] **Speaker 1:** Um Yeah So over relaxation can be quite, quite handy.
[00:23:00:459 - 00:23:01:530] **Speaker 1:** Any questions so far?
[00:23:02:729 - 00:23:07:140] **Speaker 0:** Time we We Wouldn't.
[00:23:07:239 - 00:23:10:069] **Speaker 1:** Um, we're gonna go through some fun examples shortly, just
[00:23:10:069 - 00:23:12:959] **Speaker 1:** to just demonstrate what happens if we use a overrelaxation
[00:23:12:959 - 00:23:13:780] **Speaker 1:** factor that's too large.
[00:23:14:959 - 00:23:19:310] **Speaker 1:** Um Which is pretty much the only reason that you
[00:23:19:310 - 00:23:20:810] **Speaker 1:** might not want to use it, so if you have
[00:23:20:810 - 00:23:22:589] **Speaker 1:** an unstable solution.
[00:23:27:030 - 00:23:27:510] **Speaker 1:** Yeah.
[00:23:27:910 - 00:23:30:699] **Speaker 1:** And then, and CFD, yeah, if you take CFD next
[00:23:30:699 - 00:23:33:459] **Speaker 1:** year, um, I often use under relaxation to try and
[00:23:33:459 - 00:23:37:319] **Speaker 1:** improve the convergence of some of the equations, but Um
[00:23:37:949 - 00:23:39:689] **Speaker 1:** Yeah, the heat equation is nice and easy to solve,
[00:23:39:800 - 00:23:40:520] **Speaker 1:** nice and linear.
[00:23:41:829 - 00:23:44:550] **Speaker 1:** Straightforward, so we can, yeah.
[00:23:46:119 - 00:23:48:599] **Speaker 1:** Give it a bit of a thrashing with relaxation.
[00:23:49:119 - 00:23:52:050] **Speaker 1:** All right, so derived variables and results.
[00:23:52:560 - 00:23:54:699] **Speaker 1:** So we're gonna solve for the temperature field.
[00:23:55:750 - 00:23:58:430] **Speaker 1:** And now we want to visualise what does it look
[00:23:58:430 - 00:23:58:939] **Speaker 1:** like.
[00:23:59:439 - 00:24:01:579] **Speaker 1:** We did it briefly on this plot.
[00:24:03:359 - 00:24:06:229] **Speaker 1:** Um, which works, but you might want to make some
[00:24:06:229 - 00:24:06:859] **Speaker 1:** plots.
[00:24:07:319 - 00:24:09:420] **Speaker 1:** So once the solution to our PDE has been found,
[00:24:09:719 - 00:24:10:959] **Speaker 1:** we want to post-process.
[00:24:11:589 - 00:24:14:530] **Speaker 1:** And visualise and analyse the results, maybe make a report
[00:24:14:790 - 00:24:15:949] **Speaker 1:** and an assignment, so that's good.
[00:24:16:640 - 00:24:18:760] **Speaker 1:** A common way to visualise the results is to plot
[00:24:18:760 - 00:24:20:439] **Speaker 1:** isolines or contour lines.
[00:24:20:479 - 00:24:23:660] **Speaker 1:** So think of weather forecasting, you've got isobars, constant pressure.
[00:24:25:079 - 00:24:29:310] **Speaker 1:** So that's where lines are created that have the same.
[00:24:30:199 - 00:24:31:310] **Speaker 1:** Value for the dependent variables.
[00:24:31:359 - 00:24:34:020] **Speaker 1:** So isotherms being an example for the heat equation.
[00:24:34:359 - 00:24:37:459] **Speaker 1:** So lines with the same temperature isotherms.
[00:24:37:959 - 00:24:40:280] **Speaker 1:** Another variable of interest we might want to plot is
[00:24:40:280 - 00:24:41:000] **Speaker 1:** the heat flux.
[00:24:41:400 - 00:24:44:349] **Speaker 1:** So we looked at um 4 years the law before,
[00:24:44:390 - 00:24:46:550] **Speaker 1:** so we've got Q dot.
[00:24:48:290 - 00:24:52:890] **Speaker 1:** Um, It's a dot because it's a rate, and it's
[00:24:52:890 - 00:24:55:869] **Speaker 1:** a little vector because it has vector components.
[00:24:59:000 - 00:25:00:459] **Speaker 1:** We said it is equal to -KT.
[00:25:05:729 - 00:25:10:209] **Speaker 1:** Gravity is taking the derivative of temperature in each direction.
[00:25:10:449 - 00:25:12:709] **Speaker 1:** So in 2D we've got DT by DX.
[00:25:14:420 - 00:25:17:699] **Speaker 1:** I've used i hat for the unit vector in the
[00:25:17:699 - 00:25:18:479] **Speaker 1:** X direction.
[00:25:19:209 - 00:25:21:969] **Speaker 1:** And DT by DYJ hat.
[00:25:26:369 - 00:25:30:329] **Speaker 1:** And these Can be split up in components, we've got
[00:25:30:329 - 00:25:30:589] **Speaker 1:** Q.
[00:25:30:780 - 00:25:31:069] **Speaker 1:** X.
[00:25:32:989 - 00:25:35:359] **Speaker 1:** And X And Q.
[00:25:35:790 - 00:25:36:239] **Speaker 1:** Y.
[00:25:37:319 - 00:25:55:160] **Speaker 1:** And what So we've got a Python demonstration, so I'll
[00:25:55:160 - 00:26:01:180] **Speaker 1:** just start my laptop, but, We're gonna Evaluate the derivatives
[00:26:01:180 - 00:26:02:329] **Speaker 1:** using central difference.
[00:26:02:619 - 00:26:05:140] **Speaker 1:** So I'll get you to do something if you're paying
[00:26:05:140 - 00:26:05:540] **Speaker 1:** attention.
[00:26:05:819 - 00:26:10:319] **Speaker 1:** So Q.X is equal to minus KDT by DX.
[00:26:11:069 - 00:26:13:949] **Speaker 1:** So I want you to apply a central differencing for
[00:26:13:949 - 00:26:16:069] **Speaker 1:** that derivative DT by DX.
[00:26:51:709 - 00:26:53:469] **Speaker 1:** Uh, 2nd order accurate.
[00:26:54:400 - 00:26:57:349] **Speaker 1:** So 1st order derivative, 2nd order accurate central difference.
[00:27:30:300 - 00:27:33:250] **Speaker 1:** So K is a material property, the thermal conductivity of
[00:27:33:250 - 00:27:36:890] **Speaker 1:** the plate, and for this example, we'll just treat it
[00:27:36:890 - 00:27:37:489] **Speaker 1:** as constant.
[00:27:37:689 - 00:27:38:589] **Speaker 1:** So it's just going to be.
[00:27:39:290 - 00:27:40:219] **Speaker 1:** Still minus K.
[00:27:41:510 - 00:27:43:329] **Speaker 1:** The central difference.
[00:27:48:250 - 00:27:50:270] **Speaker 1:** That read the book that was in chapter.
[00:27:52:630 - 00:27:53:069] **Speaker 1:** 3.
[00:28:08:750 - 00:28:12:369] **Speaker 1:** So first order derivative, 2nd order accuracy, it's minus 12
[00:28:12:699 - 00:28:15:900] **Speaker 1:** on the left, minus plus 12 on the right.
[00:28:16:260 - 00:28:19:699] **Speaker 1:** So just rise over run, um, grad.
[00:28:20:650 - 00:28:22:750] **Speaker 1:** T by grad X, so T.
[00:28:27:219 - 00:28:28:560] **Speaker 1:** I plus one.
[00:28:30:839 - 00:28:34:160] **Speaker 1:** J minus TI minus 1 J.
[00:28:35:459 - 00:28:40:920] **Speaker 1:** Divided by The spacing, so this is across two node
[00:28:40:920 - 00:28:42:250] **Speaker 1:** points, so 2.
[00:28:43:079 - 00:28:44:010] **Speaker 1:** Delta X.
[00:28:46:219 - 00:28:49:670] **Speaker 1:** This is a first order derivative of T with respect
[00:28:49:670 - 00:28:50:209] **Speaker 1:** to X.
[00:28:50:329 - 00:28:54:250] **Speaker 1:** So we've held the Y component or Y coordinate constant.
[00:28:54:449 - 00:28:57:449] **Speaker 1:** So we've used the same index J for both terms.
[00:28:57:729 - 00:29:00:270] **Speaker 1:** We're only looking at the varied temperature in X.
[00:29:02:150 - 00:29:03:750] **Speaker 1:** And this is the 2nd order accurate, so we've got
[00:29:03:750 - 00:29:06:270] **Speaker 1:** an order of delta X2 remainder.
[00:29:13:239 - 00:29:16:040] **Speaker 1:** And we do the same for.
[00:29:18:380 - 00:29:18:510] **Speaker 1:** Q.
[00:29:18:790 - 00:29:19:119] **Speaker 1:** Y.
[00:30:10:859 - 00:30:14:020] **Speaker 1:** So again, holding X constant or the I index and
[00:30:14:020 - 00:30:17:949] **Speaker 1:** then varying J and the spacing is 2y and we've
[00:30:17:949 - 00:30:19:439] **Speaker 1:** got an order of accuracy scaling with Y2.
[00:30:21:689 - 00:30:24:390] **Speaker 1:** All right, so, yeah, as, as one of the um
[00:30:24:930 - 00:30:26:869] **Speaker 1:** one of your classmates pointed out, when can we use
[00:30:26:869 - 00:30:28:410] **Speaker 1:** the over relaxation, when can't we?
[00:30:28:689 - 00:30:30:709] **Speaker 1:** So we're gonna go through this.
[00:30:32:010 - 00:30:34:010] **Speaker 1:** On the screen.
[00:30:34:989 - 00:30:35:469] **Speaker 1:** Python.
[00:30:37:880 - 00:30:43:229] **Speaker 1:** This is, Hopefully going to be the same example that
[00:30:43:229 - 00:30:43:890] **Speaker 1:** we did earlier.
[00:30:45:319 - 00:30:46:000] **Speaker 1:** With any luck.
[00:30:51:930 - 00:30:53:930] **Speaker 1:** So we've got a size of our domain and X,
[00:30:54:010 - 00:30:56:849] **Speaker 1:** our thermal conductivity, grid spacing.
[00:30:58:449 - 00:31:00:189] **Speaker 1:** That's gonna be a different size, but that's all right.
[00:31:01:229 - 00:31:04:310] **Speaker 1:** Um, setting the temperature at the boundaries.
[00:31:04:420 - 00:31:05:949] **Speaker 1:** So they're all directly boundary conditions.
[00:31:06:310 - 00:31:09:069] **Speaker 1:** The ones at the corner, I've just averaged the, the
[00:31:09:069 - 00:31:10:810] **Speaker 1:** two boundary conditions because they're inconsistent.
[00:31:11:579 - 00:31:12:619] **Speaker 1:** At the corners.
[00:31:14:430 - 00:31:18:069] **Speaker 1:** Um, the Lieben method, there's lots of different ways of
[00:31:18:069 - 00:31:18:829] **Speaker 1:** making your own code.
[00:31:18:910 - 00:31:20:040] **Speaker 1:** This is just one example.
[00:31:20:520 - 00:31:22:189] **Speaker 1:** So I've got a loop equal to true, which I
[00:31:22:189 - 00:31:24:390] **Speaker 1:** always think is a little bit dangerous, but, um, that's,
[00:31:24:469 - 00:31:25:369] **Speaker 1:** that's how it's been set up.
[00:31:26:489 - 00:31:27:390] **Speaker 1:** Iteration starting at 1.
[00:31:27:829 - 00:31:30:420] **Speaker 1:** We've got a stopping criteria of 10 to -3, so
[00:31:30:420 - 00:31:33:780] **Speaker 1:** 0.1%. For now I've just set the ovary relaxation parameters
[00:31:33:780 - 00:31:36:010] **Speaker 1:** to be um 1, so it's disabled.
[00:31:36:800 - 00:31:39:660] **Speaker 1:** And I've set t equal to t copy.
[00:31:40:959 - 00:31:42:880] **Speaker 1:** So in Python, I find that you need to use
[00:31:42:880 - 00:31:46:160] **Speaker 1:** .copy, otherwise it just points to the old variable, which
[00:31:46:160 - 00:31:48:280] **Speaker 1:** is a little bit frustrating for for someone that's not
[00:31:48:280 - 00:31:51:060] **Speaker 1:** familiar with Python, but maybe you are familiar with this,
[00:31:51:099 - 00:31:51:959] **Speaker 1:** this workflow.
[00:31:52:859 - 00:31:55:180] **Speaker 1:** Um, we've got a couple of 4 loops for our
[00:31:55:180 - 00:31:59:619] **Speaker 1:** interior nodes, starting from 1 up to and not including
[00:31:59:619 - 00:32:00:540] **Speaker 1:** the N minus 1.
[00:32:02:439 - 00:32:03:699] **Speaker 1:** Line 43.
[00:32:04:729 - 00:32:14:550] **Speaker 1:** Is, Our equation 4.4, so we've used the Lieben method
[00:32:14:930 - 00:32:17:209] **Speaker 1:** and also the over relaxation in one step, which is
[00:32:17:209 - 00:32:20:489] **Speaker 1:** why I didn't bother defining the star auxiliary variable.
[00:32:22:989 - 00:32:24:849] **Speaker 1:** We have calculated the relative error.
[00:32:25:819 - 00:32:27:640] **Speaker 1:** With times by 100 to make it a percent.
[00:32:31:030 - 00:32:32:199] **Speaker 1:** The norm era.
[00:32:33:890 - 00:32:37:369] **Speaker 1:** That And so forth, so.
[00:32:39:119 - 00:32:42:310] **Speaker 1:** It's taken 117 iterations to converge to that 10 to
[00:32:42:310 - 00:32:45:500] **Speaker 1:** -3, I assume that's not absolute.
[00:32:46:920 - 00:32:52:160] **Speaker 1:** Um, Uh, I should probably change the resolution on this
[00:32:52:160 - 00:32:56:250] **Speaker 1:** screen, but this is the log of the norm percent
[00:32:56:250 - 00:32:57:089] **Speaker 1:** relative error.
[00:32:57:969 - 00:33:01:459] **Speaker 1:** We can see that it's decreasing with iterations, so that's
[00:33:01:609 - 00:33:02:170] **Speaker 1:** reassuring.
[00:33:02:209 - 00:33:03:010] **Speaker 1:** It's converging.
[00:33:05:530 - 00:33:10:560] **Speaker 1:** And When we go to plot We can plot the
[00:33:10:560 - 00:33:14:979] **Speaker 1:** isotherms, so these contour lines showing lines of constant temperature.
[00:33:17:260 - 00:33:20:290] **Speaker 1:** And we expect them to be about 56.
[00:33:22:550 - 00:33:25:510] **Speaker 1:** So that corresponds to around this colour range, 54 to
[00:33:25:510 - 00:33:26:890] **Speaker 1:** 63, so that's good.
[00:33:27:739 - 00:33:33:060] **Speaker 1:** We've plotted the Arrows of heat flux, so Q dot.
[00:33:34:619 - 00:33:35:020] **Speaker 1:** With Q.
[00:33:35:140 - 00:33:35:660] **Speaker 1:** X and Q.
[00:33:35:859 - 00:33:36:280] **Speaker 1:** Y.
[00:33:39:920 - 00:33:43:500] **Speaker 1:** This is using the gradient operator in the NumPy library.
[00:33:44:079 - 00:33:47:160] **Speaker 1:** We've got our temperature vector field and spacings DX.
[00:33:48:589 - 00:33:51:310] **Speaker 1:** Our heat flux in the X and Y directions are
[00:33:51:310 - 00:33:55:709] **Speaker 1:** evaluated with minus K times the gradients, and we've used
[00:33:55:709 - 00:34:00:910] **Speaker 1:** quiver as part of Mattpotler library uh to to generate
[00:34:00:910 - 00:34:02:030] **Speaker 1:** those little arrowheads.
[00:34:04:260 - 00:34:04:660] **Speaker 1:** Cool.
[00:34:05:650 - 00:34:08:290] **Speaker 1:** So that was with without over relaxation essentially.
[00:34:08:408 - 00:34:10:388] **Speaker 1:** If we set it to 1.5.
[00:34:12:169 - 00:34:15:148] **Speaker 1:** We find that we only took 35 iterations to converge.
[00:34:16:059 - 00:34:19:979] **Speaker 1:** So that's a decent speed up in terms of saving
[00:34:19:979 - 00:34:20:319] **Speaker 1:** time.
[00:34:22:290 - 00:34:25:020] **Speaker 1:** Again, this example is very quick anyway, but if you
[00:34:25:020 - 00:34:27:719] **Speaker 1:** were solving a larger problem, it would be more pronounced.
[00:34:30:520 - 00:34:32:770] **Speaker 1:** Uh, we can see that the convergence plot is still
[00:34:32:770 - 00:34:33:070] **Speaker 1:** good.
[00:34:33:878 - 00:34:36:830] **Speaker 1:** Uh, the error is reducing with the number of iterations.
[00:34:38:648 - 00:34:43:949] **Speaker 1:** If we increase Our over relaxation further 1.7.
[00:34:46:510 - 00:34:49:219] **Speaker 1:** Now it's taking a little bit more iterations, so 42,
[00:34:49:429 - 00:34:50:850] **Speaker 1:** so that's greater than 35.
[00:34:52:070 - 00:34:53:250] **Speaker 1:** And 1.8.
[00:34:55:138 - 00:34:57:199] **Speaker 1:** 64, um.
[00:34:57:929 - 00:35:01:469] **Speaker 1:** I guess we can look at So it's starting to
[00:35:01:469 - 00:35:03:189] **Speaker 1:** look a little bit maybe unstable, but it is still
[00:35:03:189 - 00:35:03:750] **Speaker 1:** converging.
[00:35:03:949 - 00:35:05:889] **Speaker 1:** So this is the error against iterations.
[00:35:06:610 - 00:35:09:110] **Speaker 1:** If we still increase further 1.9.
[00:35:11:639 - 00:35:13:469] **Speaker 1:** Now we're back up to 135.
[00:35:14:139 - 00:35:16:449] **Speaker 1:** And I was looking a little bit Dodgy.
[00:35:17:189 - 00:35:19:669] **Speaker 1:** And 1.95, getting close to 2.
[00:35:21:229 - 00:35:24:750] **Speaker 1:** That's starting to, to sort of not work so well.
[00:35:25:780 - 00:35:27:699] **Speaker 1:** Um, but, yeah.
[00:35:29:639 - 00:35:35:639] **Speaker 1:** Um, It is still converging, so that's, that's reassuring, that's
[00:35:35:639 - 00:35:36:729] **Speaker 1:** reasonably robust.
[00:35:37:209 - 00:35:39:270] **Speaker 1:** Um, the over relaxation factor.
[00:35:40:860 - 00:35:46:370] **Speaker 1:** Optimum one will be probably around that 1.6 or 1.7
[00:35:46:370 - 00:35:50:399] **Speaker 1:** that we were looking at earlier, so 35 iterations.
[00:35:51:239 - 00:35:56:330] **Speaker 1:** Um, Depending on the geometry, the equation, and the setup,
[00:35:56:570 - 00:35:59:370] **Speaker 1:** you might find that the over relaxation that's optimum varies.
[00:35:59:489 - 00:36:03:090] **Speaker 1:** So there's no global factor lambda that we want to
[00:36:03:090 - 00:36:03:610] **Speaker 1:** always use.
[00:36:03:889 - 00:36:04:250] **Speaker 1:** So.
[00:36:05:090 - 00:36:06:750] **Speaker 1:** Don't latch on it too hard.
[00:36:09:270 - 00:36:10:100] **Speaker 1:** Um, yeah.
[00:36:10:149 - 00:36:12:870] **Speaker 1:** Any questions on this codes set?
[00:36:13:790 - 00:36:15:379] **Speaker 1:** I didn't go through every single step.
[00:36:15:439 - 00:36:17:919] **Speaker 1:** It's mostly similar to what we've done earlier.
[00:36:19:189 - 00:36:20:310] **Speaker 1:** In the earlier scripts.
[00:36:21:199 - 00:36:28:010] **Speaker 1:** Um, Yeah, I'll leave it to you to investigate in
[00:36:28:010 - 00:36:29:590] **Speaker 1:** your own time if you want to look at the.
[00:36:30:239 - 00:36:31:010] **Speaker 1:** The plots.
[00:36:33:580 - 00:36:39:080] **Speaker 1:** Right All right, next, uh, I'll talk about boundary conditions.
[00:36:39:159 - 00:36:41:239] **Speaker 1:** So we've already seen how to do the Diri boundary
[00:36:41:239 - 00:36:42:560] **Speaker 1:** condition, which was essentially nothing.
[00:36:42:679 - 00:36:43:939] **Speaker 1:** It was just existing.
[00:36:44:439 - 00:36:46:639] **Speaker 1:** So how do we deal with the Neumann boundary?
[00:36:46:719 - 00:36:49:030] **Speaker 1:** So that means when we set the gradient, so dot
[00:36:49:030 - 00:36:51:679] **Speaker 1:** by DX, for example, uh, we might have a constant
[00:36:51:679 - 00:36:53:239] **Speaker 1:** flux or the flux might be zero.
[00:36:53:439 - 00:36:54:639] **Speaker 1:** So if it's fully insulated.
[00:36:55:590 - 00:36:57:590] **Speaker 1:** So the fully insulated boundary condition is where we have
[00:36:57:590 - 00:37:02:590] **Speaker 1:** gradt.nn being the unit normal vector, um, is equal to
[00:37:02:590 - 00:37:03:030] **Speaker 1:** 0.
[00:37:07:649 - 00:37:16:229] **Speaker 1:** So I just wanna Point out This in hat.
[00:37:18:840 - 00:37:23:100] **Speaker 1:** In hat is representing the unit vector normal to the
[00:37:23:479 - 00:37:25:840] **Speaker 1:** boundary or the edge that it's representing.
[00:37:26:550 - 00:37:31:580] **Speaker 1:** We evaluated at So depending on which edge we look
[00:37:31:580 - 00:37:33:199] **Speaker 1:** at, it'll hold a different value.
[00:37:33:949 - 00:37:37:500] **Speaker 1:** But it's just easier to write gradT.in than all the
[00:37:37:500 - 00:37:38:699] **Speaker 1:** other terms.
[00:37:39:300 - 00:37:41:419] **Speaker 1:** So in hat on the top.
[00:37:42:129 - 00:37:47:090] **Speaker 1:** Is parallel or equal to Jhap being the the Y
[00:37:47:090 - 00:37:48:850] **Speaker 1:** coordinate unit vector.
[00:37:50:000 - 00:37:52:040] **Speaker 1:** N hat on the bottom is equal to minus J
[00:37:52:040 - 00:37:52:419] **Speaker 1:** hat.
[00:37:57:719 - 00:38:02:040] **Speaker 1:** In hat on the right is equal to I, hat,
[00:38:02:320 - 00:38:03:199] **Speaker 1:** and on the left.
[00:38:06:179 - 00:38:07:620] **Speaker 1:** Minus I have.
[00:38:40:560 - 00:38:41:850] **Speaker 1:** I don't know, I think I included it in the
[00:38:41:850 - 00:38:44:209] **Speaker 1:** exam and someone was like, oh, I didn't, didn't see
[00:38:44:209 - 00:38:44:949] **Speaker 1:** that before, but.
[00:38:46:070 - 00:38:47:959] **Speaker 1:** I know that you've all seen it now, so that's
[00:38:47:959 - 00:38:48:159] **Speaker 1:** good.
[00:38:49:389 - 00:38:49:709] **Speaker 1:** All right.
[00:38:51:229 - 00:38:54:590] **Speaker 1:** So what we're gonna do is introduce ghost nodes again.
[00:38:55:350 - 00:38:57:189] **Speaker 1:** So we did that earlier when we were looking at
[00:38:57:189 - 00:38:58:070] **Speaker 1:** the Neumann boundary condition.
[00:38:58:149 - 00:38:58:870] **Speaker 1:** We'll do the same here.
[00:38:58:989 - 00:39:02:360] **Speaker 1:** So we've got These extra points that don't exist, which
[00:39:02:360 - 00:39:05:810] **Speaker 1:** is why they're called ghost nodes, and they, On the
[00:39:05:810 - 00:39:08:169] **Speaker 1:** other side of the node that we're analysing.
[00:39:08:419 - 00:39:10:620] **Speaker 1:** So our insulated boundary condition is going to be on
[00:39:10:620 - 00:39:11:679] **Speaker 1:** that left hand edge.
[00:39:12:659 - 00:39:15:659] **Speaker 1:** DT by DX equal to 0, we're gonna create a
[00:39:15:659 - 00:39:19:780] **Speaker 1:** series of ghost nodes to the left and label these
[00:39:19:780 - 00:39:22:419] **Speaker 1:** T0 as T1 minus 1.
[00:39:31:520 - 00:39:36:449] **Speaker 1:** And we're going to apply equation 314.
[00:39:37:919 - 00:39:39:790] **Speaker 1:** Which was our general form.
[00:39:49:590 - 00:39:51:540] **Speaker 1:** So we've got TI plus one.
[00:39:55:030 - 00:39:57:790] **Speaker 1:** So 1 + 1 is 2.
[00:40:00:959 - 00:40:01:439] **Speaker 1:** OK.
[00:40:02:840 - 00:40:04:199] **Speaker 1:** And we've got.
[00:40:05:110 - 00:40:09:370] **Speaker 1:** DI minus 1, which is gonna be D0J.
[00:40:11:669 - 00:40:15:449] **Speaker 1:** And we have, TIJ plus one.
[00:40:22:750 - 00:40:26:189] **Speaker 1:** Anti IJ minus 1.
[00:40:29:100 - 00:40:30:840] **Speaker 1:** -4 TI.
[00:40:32:310 - 00:40:36:389] **Speaker 1:** Jay So I'm replacing um eyes with one.
[00:40:41:760 - 00:40:44:870] **Speaker 1:** So this equation holds for each of those nodes on
[00:40:44:870 - 00:40:45:810] **Speaker 1:** the left-hand edge.
[00:40:54:219 - 00:40:54:620] **Speaker 1:** All right.
[00:40:56:760 - 00:40:59:610] **Speaker 1:** So we're gonna use the ghost node to discretize that
[00:40:59:610 - 00:41:02:469] **Speaker 1:** boundary condition DT by DX at X equal to 0.
[00:41:13:310 - 00:41:16:870] **Speaker 1:** Using that first order derivative, 2nd order accurate, we've got
[00:41:16:870 - 00:41:21:570] **Speaker 1:** T2J minus T0J.
[00:41:22:909 - 00:41:24:570] **Speaker 1:** Divided by 2 X.
[00:41:34:739 - 00:41:37:250] **Speaker 1:** We're gonna rearrange for that ghost node, which is 200
[00:41:37:250 - 00:41:37:500] **Speaker 1:** J.
[00:41:41:949 - 00:41:46:870] **Speaker 1:** So that's equal to T2J minus 2 X.
[00:41:47:919 - 00:41:50:679] **Speaker 1:** DT by DX at X equal to 0.
[00:41:56:439 - 00:41:59:479] **Speaker 1:** We're gonna substitute that ghost node point T0J into our
[00:41:59:479 - 00:42:02:080] **Speaker 1:** equation 4/6, so our general form.
[00:42:02:830 - 00:42:09:209] **Speaker 1:** And we're left with Um, T2J and T2J.
[00:42:09:310 - 00:42:10:489] **Speaker 1:** So we've got two of those.
[00:42:14:209 - 00:42:20:300] **Speaker 1:** Then I've got minus 2 X DT by DX at
[00:42:20:300 - 00:42:21:340] **Speaker 1:** X equals 0.
[00:42:25:340 - 00:42:30:100] **Speaker 1:** Um We've got D1, J +1.
[00:42:33:850 - 00:42:36:810] **Speaker 1:** D1 J minus 1.
[00:42:38:620 - 00:42:41:500] **Speaker 1:** And -41 J.
[00:42:54:570 - 00:42:58:510] **Speaker 1:** So the general form 4/6, we've discretized the boundary and
[00:42:58:510 - 00:43:00:239] **Speaker 1:** substituted for the the ghost node.
[00:43:01:379 - 00:43:04:939] **Speaker 1:** So if the left-hand edge was fully insulated, so that
[00:43:04:939 - 00:43:07:100] **Speaker 1:** gradient was equal to 0, so no heat flux.
[00:43:08:000 - 00:43:10:810] **Speaker 1:** Um, then we can make the substitution of DT by
[00:43:10:810 - 00:43:11:810] **Speaker 1:** DX equals 0.
[00:43:12:649 - 00:43:16:070] **Speaker 1:** so this new equation no longer includes the unknown at
[00:43:16:070 - 00:43:16:989] **Speaker 1:** the close point.
[00:43:17:429 - 00:43:18:330] **Speaker 1:** So it's a key step.
[00:43:19:280 - 00:43:22:659] **Speaker 1:** But it incorporates the boundary condition, so DT5 DX.
[00:43:25:850 - 00:43:26:929] **Speaker 1:** And this can be generalised.
[00:43:26:969 - 00:43:28:570] **Speaker 1:** So this applies to all of those on the left-hand
[00:43:28:570 - 00:43:28:979] **Speaker 1:** edge.
[00:43:29:129 - 00:43:30:929] **Speaker 1:** You can imagine if you had similar boundary conditions on
[00:43:30:929 - 00:43:33:290] **Speaker 1:** the other places, you'd have the same.
[00:43:33:500 - 00:43:35:530] **Speaker 1:** If you had one in a corner, then you would
[00:43:35:530 - 00:43:36:689] **Speaker 1:** have two of these.
[00:43:38:580 - 00:43:42:129] **Speaker 1:** Any questions on how we've applied this boundary condition, the
[00:43:42:129 - 00:43:42:340] **Speaker 1:** Neumann?
[00:43:54:409 - 00:43:54:689] **Speaker 1:** Cool.
[00:43:55:510 - 00:43:57:090] **Speaker 1:** All right, curve boundaries.
[00:43:57:909 - 00:43:58:270] **Speaker 1:** So.
[00:43:59:199 - 00:44:02:360] **Speaker 1:** Generally we're going to just deal with structured mapped measures
[00:44:02:360 - 00:44:04:120] **Speaker 1:** for our finite differencing, but you can.
[00:44:04:850 - 00:44:07:489] **Speaker 1:** With a little bit more work adapted to curved surfaces
[00:44:07:489 - 00:44:08:610] **Speaker 1:** or curved edges.
[00:44:09:540 - 00:44:11:969] **Speaker 1:** So that's what we're gonna go through now, um.
[00:44:13:360 - 00:44:16:330] **Speaker 1:** It's just more bookkeeping, to be honest, but, but we'll
[00:44:16:330 - 00:44:17:000] **Speaker 1:** do it anyway.
[00:44:17:419 - 00:44:20:199] **Speaker 1:** So many domains are not simple, um, like a square
[00:44:20:199 - 00:44:20:860] **Speaker 1:** domain.
[00:44:21:399 - 00:44:23:739] **Speaker 1:** So we're going to look at this curve boundary.
[00:44:23:959 - 00:44:26:260] **Speaker 1:** We can use this finite difference method and adapt it
[00:44:26:439 - 00:44:27:580] **Speaker 1:** for this particular case.
[00:44:28:129 - 00:44:30:179] **Speaker 1:** And we're going to analyse this.
[00:44:30:959 - 00:44:32:929] **Speaker 1:** Sort of filleted or rounded edge.
[00:44:33:699 - 00:44:34:489] **Speaker 1:** In that bottom figure.
[00:44:36:370 - 00:44:39:330] **Speaker 1:** So the general spacing has spacings of X and X
[00:44:39:330 - 00:44:41:110] **Speaker 1:** and Y in the vertical direction.
[00:44:41:840 - 00:44:45:239] **Speaker 1:** We're going to analyse a node located.
[00:44:46:040 - 00:44:46:360] **Speaker 1:** Here?
[00:44:50:639 - 00:44:53:550] **Speaker 1:** And we want to discretize our Laplace equation on this
[00:44:53:550 - 00:44:56:330] **Speaker 1:** irregular domain, so varying delta X and Y.
[00:44:57:840 - 00:45:01:169] **Speaker 1:** In order to estimate our 2nd order derivatives, we're going
[00:45:01:169 - 00:45:03:649] **Speaker 1:** to estimate the 1st order derivatives and then take the
[00:45:03:649 - 00:45:05:889] **Speaker 1:** derivative of the 1st order derivatives.
[00:45:06:919 - 00:45:12:840] **Speaker 1:** So And X, so D2T by DX2, we want to
[00:45:12:840 - 00:45:16:040] **Speaker 1:** look at the first order derivatives at A and B.
[00:45:16:239 - 00:45:19:139] **Speaker 1:** So these are the midpoints between the adjacent nodes.
[00:45:20:629 - 00:45:24:310] **Speaker 1:** So we've got DT B D X.
[00:45:25:250 - 00:45:27:850] **Speaker 1:** Evaluated at the midpoint, A.
[00:45:49:879 - 00:45:52:679] **Speaker 1:** So just as we've done before, it's gonna be rise
[00:45:52:679 - 00:45:55:379] **Speaker 1:** over run between these two points.
[00:45:56:110 - 00:45:58:040] **Speaker 1:** So we've got TIJ.
[00:46:00:179 - 00:46:01:939] **Speaker 1:** I + 1 J.
[00:46:02:500 - 00:46:04:179] **Speaker 1:** I minus 1 J.
[00:46:05:239 - 00:46:09:800] **Speaker 1:** IJ + 1 and IJ minus 1.
[00:46:11:110 - 00:46:13:429] **Speaker 1:** So DT by DX at point A is going to
[00:46:13:429 - 00:46:15:689] **Speaker 1:** be the temperature at 1 + 1.
[00:46:19:250 - 00:46:21:110] **Speaker 1:** J minus the temperature.
[00:46:22:260 - 00:46:29:250] **Speaker 1:** Uh, at I Jay, So change in temperature divided by
[00:46:29:250 - 00:46:30:149] **Speaker 1:** that spacing.
[00:46:31:179 - 00:46:35:060] **Speaker 1:** That spacing is delta X, or we'll generalise it and
[00:46:35:060 - 00:46:38:260] **Speaker 1:** call it some fraction of delta X, so alpha 2.
[00:46:43:429 - 00:46:45:129] **Speaker 1:** Just keep this form alpha 2 is probably just equal
[00:46:45:129 - 00:46:47:149] **Speaker 1:** to 1 in this case because it's still uniform here.
[00:46:47:530 - 00:46:49:330] **Speaker 1:** But we can see on the left-hand side that we've
[00:46:49:330 - 00:46:50:770] **Speaker 1:** got alpha 1 X.
[00:46:51:050 - 00:46:53:010] **Speaker 1:** So we'll just keep that same terminology.
[00:46:54:949 - 00:46:57:939] **Speaker 1:** So that's the first order derivative at A.
[00:46:58:350 - 00:47:02:429] **Speaker 1:** We want to get evaluate the derivative DT by DX
[00:47:02:429 - 00:47:03:629] **Speaker 1:** at B.
[00:47:04:790 - 00:47:08:159] **Speaker 1:** That's very similar, we're looking at the temperature varying between
[00:47:08:159 - 00:47:09:820] **Speaker 1:** I minus 1 and I.
[00:47:17:360 - 00:47:20:919] **Speaker 1:** And that spacing or nodal spacing is alpha 1 X.
[00:47:31:840 - 00:47:34:709] **Speaker 1:** So we've got the first order derivatives at those midpoints
[00:47:35:250 - 00:47:37:610] **Speaker 1:** and essentially we're going to do a central difference of
[00:47:37:610 - 00:47:41:010] **Speaker 1:** a central difference to get that second order, um, derivative
[00:47:41:010 - 00:47:42:290] **Speaker 1:** D2T by DX2.
[00:47:55:419 - 00:47:58:310] **Speaker 1:** And we'll just introduce another variable for fun, gamma.
[00:47:59:320 - 00:48:01:199] **Speaker 1:** Which is the distance between A and B.
[00:48:20:479 - 00:48:23:129] **Speaker 1:** So gamma is going to be equal to.
[00:48:28:169 - 00:48:30:250] **Speaker 1:** Half of the spacing of alpha 1.
[00:48:31:989 - 00:48:36:270] **Speaker 1:** Delta X and half the spacing of alpha 2D X.
[00:48:45:110 - 00:48:45:129] **Speaker 1:** All right.
[00:48:47:790 - 00:48:51:810] **Speaker 1:** So again, central difference, so rise over run, we've got
[00:48:52:919 - 00:48:55:530] **Speaker 1:** The change in our gradients, ET.
[00:48:57:919 - 00:48:59:199] **Speaker 1:** Uh, the X.
[00:49:03:429 - 00:49:08:350] **Speaker 1:** At A minus DT by DX at E.
[00:49:12:409 - 00:49:15:919] **Speaker 1:** So change in gradients over the displacement gamma.
[00:49:19:899 - 00:49:27:370] **Speaker 1:** And this is equal to To Over alpha 1 X
[00:49:27:370 - 00:49:36:810] **Speaker 1:** plus alpha2X multiplied by TI + 1 J minus TIJ
[00:49:37:370 - 00:49:40:800] **Speaker 1:** divided by alpha 2 X, so that's subshooting and DT
[00:49:40:800 - 00:49:41:570] **Speaker 1:** by DX at A.
[00:49:42:379 - 00:49:47:350] **Speaker 1:** And DT by DX at B is TIJ minus TI
[00:49:47:350 - 00:49:52:070] **Speaker 1:** minus 1 J divided by alpha 1 delta X.
[00:49:58:510 - 00:50:01:580] **Speaker 1:** So with some rearrangement, we can write it out as
[00:50:01:580 - 00:50:02:459] **Speaker 1:** equation 10.
[00:50:03:219 - 00:50:06:840] **Speaker 1:** We do the same procedure in Y, same steps, uh,
[00:50:06:939 - 00:50:09:330] **Speaker 1:** we've got equation 11, then we're substituting back into our
[00:50:09:330 - 00:50:12:060] **Speaker 1:** Laplace equation, which we said was equation 9.
[00:50:13:189 - 00:50:16:830] **Speaker 1:** And this is our discretized equation.
[00:50:17:070 - 00:50:19:790] **Speaker 1:** So equation 12 is our discretized equation for that nodal
[00:50:19:790 - 00:50:21:159] **Speaker 1:** point along the boundary.
[00:50:21:590 - 00:50:23:919] **Speaker 1:** So quite a bit more complicated than the uniform grid
[00:50:23:919 - 00:50:27:649] **Speaker 1:** spacing case, uh, but it's still possible with finite differencing.
[00:50:28:149 - 00:50:28:629] **Speaker 1:** So.
[00:50:29:370 - 00:50:31:000] **Speaker 1:** Yeah, just a bit of an exercise in.
[00:50:33:600 - 00:50:34:479] **Speaker 1:** Finite difference.
[00:50:36:830 - 00:50:37:229] **Speaker 1:** All right.
[00:50:39:040 - 00:50:39:360] **Speaker 1:** Cool.
[00:50:41:360 - 00:50:42:659] **Speaker 1:** That's a good spot to leave it.
[00:50:42:719 - 00:50:45:379] **Speaker 1:** Um, so this afternoon we've got the labs, so bring
[00:50:45:379 - 00:50:48:040] **Speaker 1:** along all your questions from the course and the quiz
[00:50:48:040 - 00:50:49:840] **Speaker 1:** and console labs, and we'll see you there.
[00:51:12:919 - 00:51:38:300] **Speaker 0:** The Oh, I'm going to say.
[00:51:53:550 - 00:51:54:239] **Speaker 0:** Exactly the same.
[00:52:02:820 - 00:52:03:800] **Speaker 0:** That's like.
[00:52:17:239 - 00:52:22:800] **Speaker 0:** But know.
[00:52:25:090 - 00:52:25:100] **Speaker 0:** I.
[00:52:31:760 - 00:52:31:770] **Speaker 0:** Right.
[00:52:35:439 - 00:52:35:449] **Speaker 0:** No.
[00:52:37:919 - 00:52:40:149] **Speaker 0:** Are you guys I'm like.
[00:52:48:899 - 00:52:49:909] **Speaker 0:** What did you watch?
[00:52:53:260 - 00:52:54:149] **Speaker 0:** Well, actually no.
[00:53:00:149 - 00:53:00:510] **Speaker 0:** years.
[00:53:04:350 - 00:53:05:590] **Speaker 0:** They're introducing the.

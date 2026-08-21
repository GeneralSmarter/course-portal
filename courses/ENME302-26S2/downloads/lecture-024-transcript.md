# ENME302-26S2 Lecture 24 native Echo transcript

Date: August 21, 2026 11:00am-11:55am
Transcript type: native Echo automated transcript.

[00:00:00:300 - 00:00:02:140] **Speaker 0:** Some He.
[00:00:06:659 - 00:00:07:989] **Speaker 0:** Oh God, I mean.
[00:00:16:360 - 00:00:18:440] **Speaker 0:** I checked the, I checked other people's ones as well,
[00:00:18:969 - 00:00:19:559] **Speaker 0:** you know.
[00:00:29:489 - 00:00:32:159] **Speaker 1:** I Uh, good morning.
[00:00:32:229 - 00:00:32:939] **Speaker 1:** We'll make a start.
[00:00:33:360 - 00:00:35:950] **Speaker 1:** Any questions before we dive back into our meeting?
[00:00:38:270 - 00:00:40:009] **Speaker 0:** Yeah there.
[00:00:41:340 - 00:00:46:380] **Speaker 1:** Anyone stuck with the quiz questions or whatever, that's due
[00:00:46:380 - 00:00:46:880] **Speaker 1:** tonight.
[00:00:48:459 - 00:00:49:299] **Speaker 1:** All good.
[00:00:49:900 - 00:00:50:180] **Speaker 1:** Cool.
[00:00:51:529 - 00:00:52:069] **Speaker 1:** All right.
[00:00:52:569 - 00:00:57:909] **Speaker 1:** So yesterday we're going through this, uh, section on mesh.
[00:00:59:520 - 00:01:04:120] **Speaker 1:** So we talked about different terminology, uh, different types of
[00:01:04:120 - 00:01:05:620] **Speaker 1:** meshes, so different shapes.
[00:01:06:319 - 00:01:10:370] **Speaker 1:** And structured versus unstructured is where we got up to.
[00:01:11:169 - 00:01:15:690] **Speaker 1:** So structured mesh, uh we have essentially a number of
[00:01:15:690 - 00:01:18:129] **Speaker 1:** rows and columns that define a mesh.
[00:01:28:519 - 00:01:30:459] **Speaker 1:** Well, it's all muted, that's very helpful, isn't it?
[00:01:31:230 - 00:01:34:610] **Speaker 1:** Um OK, it's, oh, yeah.
[00:01:35:569 - 00:01:35:800] **Speaker 1:** Cool.
[00:01:35:930 - 00:01:37:089] **Speaker 1:** Alright, you didn't miss much.
[00:01:37:209 - 00:01:40:419] **Speaker 1:** Alright, so the mesh, um, for a structured grid has
[00:01:40:419 - 00:01:41:730] **Speaker 1:** all these rows and columns.
[00:01:42:569 - 00:01:46:330] **Speaker 1:** And The advantage here is that we always know the
[00:01:46:330 - 00:01:46:900] **Speaker 1:** neighbouring nodes.
[00:01:47:099 - 00:01:49:699] **Speaker 1:** So left, right, top and bottom, we can just switch
[00:01:49:699 - 00:01:51:410] **Speaker 1:** the indices by, by one.
[00:01:54:889 - 00:01:56:599] **Speaker 1:** So the advantage here is that it's really easy to
[00:01:56:599 - 00:01:57:099] **Speaker 1:** generate.
[00:01:57:559 - 00:02:01:790] **Speaker 1:** Uh, we Define where we want every single node to
[00:02:01:790 - 00:02:03:750] **Speaker 1:** be and then that's generated the mesh.
[00:02:04:349 - 00:02:07:470] **Speaker 1:** And there's a low storage requirement for keeping track of
[00:02:07:470 - 00:02:09:990] **Speaker 1:** neighbouring nodes because we have that by definition.
[00:02:11:880 - 00:02:16:000] **Speaker 1:** It typically uh creates a well-behaved algebraic system of equations
[00:02:16:000 - 00:02:16:500] **Speaker 1:** as well.
[00:02:17:580 - 00:02:19:960] **Speaker 1:** So we'll come to that a bit later on.
[00:02:20:880 - 00:02:24:800] **Speaker 1:** The main disadvantage here is that the mesh is hard
[00:02:24:800 - 00:02:27:679] **Speaker 1:** to sort of adapt to curved surfaces or other, uh,
[00:02:27:690 - 00:02:29:660] **Speaker 1:** non-straight domains.
[00:02:30:199 - 00:02:34:160] **Speaker 1:** So we'll have a nice example down here shortly on
[00:02:34:160 - 00:02:35:149] **Speaker 1:** how we can tackle that.
[00:02:35:520 - 00:02:38:479] **Speaker 1:** But here we have a structured Cartesian mesh with a
[00:02:38:479 - 00:02:42:190] **Speaker 1:** normal regular grid and then a boundary fitted mesh where
[00:02:43:220 - 00:02:46:160] **Speaker 1:** we can adapt the, the structured grid or map it
[00:02:46:160 - 00:02:48:279] **Speaker 1:** across a few different regions.
[00:02:49:899 - 00:02:54:399] **Speaker 1:** The unstructured mesh is essentially just a chaos, um, or
[00:02:54:399 - 00:02:56:220] **Speaker 1:** a chaotic mesh or not too bad.
[00:02:56:460 - 00:02:58:279] **Speaker 1:** We can see that they are mostly the same size
[00:02:58:699 - 00:02:59:000] **Speaker 1:** throughout.
[00:03:02:289 - 00:03:04:509] **Speaker 1:** And they're all triangles.
[00:03:04:970 - 00:03:06:610] **Speaker 1:** Uh, so this is, this is an example of an
[00:03:06:610 - 00:03:07:630] **Speaker 1:** untracked mesh.
[00:03:08:160 - 00:03:10:369] **Speaker 1:** So there's no regularity in the arrangement or good point.
[00:03:10:449 - 00:03:13:529] **Speaker 1:** So if we selected one arbitrarily, we wouldn't necessarily know
[00:03:13:529 - 00:03:16:289] **Speaker 1:** which one was, uh, the neighbours without keeping track of
[00:03:16:289 - 00:03:22:179] **Speaker 1:** that in our, um, System So the advantage here is
[00:03:22:179 - 00:03:25:750] **Speaker 1:** that we can distribute through an arbitrary geometry or domain.
[00:03:26:399 - 00:03:28:199] **Speaker 1:** And the disadvantages that data structure.
[00:03:29:419 - 00:03:32:580] **Speaker 1:** So typically, it's best to use a structured grid if
[00:03:32:580 - 00:03:33:119] **Speaker 1:** you can.
[00:03:34:210 - 00:03:37:610] **Speaker 1:** They typically behave better and give better results or quicker
[00:03:37:610 - 00:03:40:210] **Speaker 1:** convergence rates rather than unstructured grid.
[00:03:41:360 - 00:03:43:479] **Speaker 1:** But if you can't create the structured grid, then do
[00:03:43:479 - 00:03:44:279] **Speaker 1:** the unstructured.
[00:03:45:649 - 00:03:47:300] **Speaker 1:** So I want to look at an example of a
[00:03:47:300 - 00:03:48:039] **Speaker 1:** circle.
[00:03:48:460 - 00:03:51:440] **Speaker 1:** So we have an unstructured grid at the top.
[00:03:52:220 - 00:03:55:779] **Speaker 1:** If we try to map a single structured grid to
[00:03:55:779 - 00:03:59:899] **Speaker 1:** the circle and selected four vertices, so we have essentially
[00:03:59:899 - 00:04:02:300] **Speaker 1:** all these, uh, columns and all these rows.
[00:04:03:309 - 00:04:05:110] **Speaker 1:** Created for our structured mesh.
[00:04:06:259 - 00:04:08:380] **Speaker 1:** What we've got here at the vertices are really skewed
[00:04:08:380 - 00:04:08:940] **Speaker 1:** elements.
[00:04:09:789 - 00:04:13:419] **Speaker 1:** And This will cause trouble when we're trying to solve
[00:04:13:419 - 00:04:14:470] **Speaker 1:** the equations.
[00:04:14:860 - 00:04:16:898] **Speaker 1:** So we want to try and avoid these skewed elements.
[00:04:17:640 - 00:04:21:920] **Speaker 1:** What we could do instead is uh generate an OH
[00:04:21:920 - 00:04:22:480] **Speaker 1:** type grid.
[00:04:23:549 - 00:04:25:339] **Speaker 1:** Has anyone got any idea of how we might go
[00:04:25:339 - 00:04:27:799] **Speaker 1:** about generating this mesh?
[00:04:28:540 - 00:04:30:700] **Speaker 1:** And console maybe.
[00:04:42:209 - 00:04:44:170] **Speaker 1:** So the unstructured mesh will probably be the default one,
[00:04:44:440 - 00:04:45:829] **Speaker 1:** especially if it was in solid mechanics.
[00:04:46:209 - 00:04:49:769] **Speaker 1:** The mapped mesh, you could define it with these vertices.
[00:04:50:630 - 00:04:54:119] **Speaker 1:** How would we go about creating an OH type grid?
[00:04:58:720 - 00:05:04:230] **Speaker 1:** It might help if I identify the Mapped regions, so
[00:05:04:230 - 00:05:05:410] **Speaker 1:** we've got 5.
[00:05:06:859 - 00:05:15:519] **Speaker 1:** Partitions For like two separate missions.
[00:05:16:230 - 00:05:16:829] **Speaker 0:** For the.
[00:05:18:010 - 00:05:20:730] **Speaker 0:** Like you, you have one niche that you would like
[00:05:20:730 - 00:05:22:529] **Speaker 0:** set parameters for it to only be in the centre.
[00:05:23:299 - 00:05:23:959] **Speaker 1:** Yes.
[00:05:25:359 - 00:05:25:709] **Speaker 1:** Yeah.
[00:05:26:079 - 00:05:28:220] **Speaker 1:** So essentially we've got 5 regions.
[00:05:28:720 - 00:05:32:119] **Speaker 1:** So the inner region is just a straight square.
[00:05:32:239 - 00:05:33:670] **Speaker 1:** We can create a structured mesh here.
[00:05:34:040 - 00:05:36:779] **Speaker 1:** And the, the circumference of the outer region, we could
[00:05:37:359 - 00:05:40:440] **Speaker 1:** decompose that into 4 grids, 4 parts.
[00:05:41:239 - 00:05:46:320] **Speaker 1:** So We looked at um geometry modelling yesterday in in
[00:05:46:320 - 00:05:48:910] **Speaker 1:** console, but you could create a sketch and create these,
[00:05:48:950 - 00:05:51:119] **Speaker 1:** these objects and then create the mesh that way.
[00:05:51:239 - 00:05:54:190] **Speaker 1:** So, Even though it looks a little bit more complicated.
[00:05:55:200 - 00:05:57:720] **Speaker 1:** You can break it up into smaller pieces and then
[00:05:57:720 - 00:06:01:359] **Speaker 1:** mash each of those five as mapped structured grids.
[00:06:09:250 - 00:06:11:010] **Speaker 1:** And this is an OH type grid.
[00:06:11:209 - 00:06:14:970] **Speaker 1:** The O represents the outer regions and H is the
[00:06:14:970 - 00:06:16:989] **Speaker 1:** standard form for the, the structured grid in the middle.
[00:06:20:859 - 00:06:21:660] **Speaker 1:** Some other mesh types.
[00:06:21:739 - 00:06:25:059] **Speaker 1:** So if we had a whole bunch of Um, well,
[00:06:25:350 - 00:06:26:890] **Speaker 1:** maybe we are looking at.
[00:06:27:649 - 00:06:31:850] **Speaker 1:** A bluff body with some fluid from left to right,
[00:06:32:089 - 00:06:34:769] **Speaker 1:** perhaps, and we wanted to resolve the boundary layer, we
[00:06:34:769 - 00:06:37:500] **Speaker 1:** might have a more refined mesh at the, the bottom.
[00:06:38:010 - 00:06:39:600] **Speaker 1:** So here we can see that we've got a, a
[00:06:39:600 - 00:06:42:089] **Speaker 1:** smaller spacing in the vertical direction to capture those velocity
[00:06:42:089 - 00:06:42:850] **Speaker 1:** gradients.
[00:06:52:179 - 00:06:54:010] **Speaker 1:** I can't think of a nice example for the trans
[00:06:54:010 - 00:06:55:859] **Speaker 1:** students that haven't done the fluids, but.
[00:06:57:160 - 00:07:01:790] **Speaker 1:** Um Just think of a river or something like that,
[00:07:01:799 - 00:07:04:649] **Speaker 1:** and we've got flow and then there's no slip on
[00:07:04:649 - 00:07:05:029] **Speaker 1:** the bottom.
[00:07:05:250 - 00:07:07:209] **Speaker 1:** So the velocity gradients fall the way to zero.
[00:07:08:029 - 00:07:10:290] **Speaker 1:** So if we want to create a mesh that has,
[00:07:10:470 - 00:07:13:709] **Speaker 1:** uh, different refinements, that's fine to do with a structured
[00:07:13:709 - 00:07:14:119] **Speaker 1:** grid.
[00:07:14:510 - 00:07:17:149] **Speaker 1:** We need to make sure that each region has matching
[00:07:17:149 - 00:07:17:670] **Speaker 1:** faces.
[00:07:18:600 - 00:07:22:429] **Speaker 1:** So You can see that in regions 1 and 2,
[00:07:22:549 - 00:07:25:709] **Speaker 1:** they match at that interface and, and so forth through
[00:07:25:709 - 00:07:26:269] **Speaker 1:** to 5.
[00:07:27:339 - 00:07:30:220] **Speaker 1:** If we had a non-matching cell interface, so we can
[00:07:30:220 - 00:07:31:980] **Speaker 1:** see here that we've got double elements.
[00:07:33:109 - 00:07:35:700] **Speaker 1:** Between regions 1 and 6, then we would have to
[00:07:35:700 - 00:07:38:640] **Speaker 1:** have some sort of interpolation function to, to map between
[00:07:38:640 - 00:07:39:880] **Speaker 1:** those two domains.
[00:07:42:140 - 00:07:44:160] **Speaker 1:** The overlapping chimeogrids.
[00:07:44:339 - 00:07:46:420] **Speaker 1:** So I showed an example of this in that first
[00:07:46:420 - 00:07:47:279] **Speaker 1:** lecture as well.
[00:07:48:609 - 00:07:50:809] **Speaker 1:** And we've got here some little flap that, that needs
[00:07:50:809 - 00:07:52:559] **Speaker 1:** to be maybe moving over time.
[00:07:53:769 - 00:07:56:329] **Speaker 1:** So we could create a new mesh for just that
[00:07:56:329 - 00:08:00:260] **Speaker 1:** piece and then overlap it with the, the background mesh
[00:08:00:450 - 00:08:02:850] **Speaker 1:** and again some interpolating between the two.
[00:08:04:029 - 00:08:06:480] **Speaker 1:** So this is one way of approaching a moving boundary
[00:08:06:480 - 00:08:06:880] **Speaker 1:** problem.
[00:08:07:690 - 00:08:09:850] **Speaker 1:** Uh, the other way is to actually just have the
[00:08:09:850 - 00:08:12:070] **Speaker 1:** one mesh and then deform the mesh over time.
[00:08:12:570 - 00:08:16:570] **Speaker 1:** So this may or may not be more, uh, computationally
[00:08:16:570 - 00:08:17:010] **Speaker 1:** efficient.
[00:08:17:170 - 00:08:19:489] **Speaker 1:** It just depends how you set up the, the code.
[00:08:22:380 - 00:08:26:470] **Speaker 1:** And some more comments about partitioning geometries.
[00:08:26:899 - 00:08:28:660] **Speaker 1:** So if we have a squibble.
[00:08:29:630 - 00:08:32:989] **Speaker 1:** snake, ah, it could be quite challenging to mesh this.
[00:08:33:190 - 00:08:36:390] **Speaker 1:** If you just use the default measure in console, it
[00:08:36:390 - 00:08:38:669] **Speaker 1:** will create a whole bunch of unstructured grids.
[00:08:40:169 - 00:08:42:669] **Speaker 1:** What we could do is split it down the centre,
[00:08:42:890 - 00:08:43:700] **Speaker 1:** so partition it.
[00:08:43:849 - 00:08:44:859] **Speaker 1:** It's still one body.
[00:08:45:140 - 00:08:47:729] **Speaker 1:** So even though we've got a mesh in two halves,
[00:08:48:020 - 00:08:50:940] **Speaker 1:** when we solve for the physics, it's one domain.
[00:08:51:900 - 00:08:53:619] **Speaker 1:** So we could split it down the middle, or we
[00:08:53:619 - 00:08:55:309] **Speaker 1:** could split it, uh.
[00:08:56:849 - 00:08:58:450] **Speaker 1:** So that we have these long lengths.
[00:08:59:239 - 00:09:00:650] **Speaker 1:** And then use a swept mesh.
[00:09:00:960 - 00:09:03:799] **Speaker 1:** So if we mesh the cross section and then sweep
[00:09:03:799 - 00:09:06:640] **Speaker 1:** it through the domain, that's, that's what we could do
[00:09:06:640 - 00:09:06:880] **Speaker 1:** here.
[00:09:09:729 - 00:09:12:950] **Speaker 1:** So this is We do look at sweat measures in
[00:09:12:950 - 00:09:14:760] **Speaker 1:** the console labs next term.
[00:09:16:900 - 00:09:20:700] **Speaker 1:** So grid accuracy The more elements the better.
[00:09:20:820 - 00:09:22:640] **Speaker 1:** We saw that with the wrench yesterday.
[00:09:22:979 - 00:09:26:020] **Speaker 1:** You looked at refining the grid using that divider length
[00:09:26:020 - 00:09:26:799] **Speaker 1:** scale HD.
[00:09:27:460 - 00:09:30:820] **Speaker 1:** So you increased it by a factor of 2 times,
[00:09:30:900 - 00:09:32:099] **Speaker 1:** 3 times, and 4 times.
[00:09:33:400 - 00:09:37:080] **Speaker 1:** And you found that you had um a convergence, so
[00:09:37:080 - 00:09:40:419] **Speaker 1:** you looked at the stress concentration somewhere or max stress
[00:09:40:840 - 00:09:44:080] **Speaker 1:** and you found that the change between those mesh resolutions
[00:09:44:080 - 00:09:47:559] **Speaker 1:** were, were narrowing with um higher refined mesh.
[00:09:48:280 - 00:09:50:510] **Speaker 1:** So you found that it would have taken longer to
[00:09:50:510 - 00:09:52:960] **Speaker 1:** solve with the more defined grid.
[00:09:53:280 - 00:09:54:500] **Speaker 1:** There's more equations to solve.
[00:09:54:940 - 00:09:57:679] **Speaker 1:** So more elements are better, but there are some practical
[00:09:57:679 - 00:09:58:030] **Speaker 1:** limits.
[00:09:58:309 - 00:10:02:020] **Speaker 1:** So your CPU, for example, How much accuracy do you
[00:10:02:020 - 00:10:02:140] **Speaker 1:** need?
[00:10:02:219 - 00:10:03:179] **Speaker 1:** How do you quantify that?
[00:10:03:299 - 00:10:06:159] **Speaker 1:** So there were a few questions in the class, um,
[00:10:06:849 - 00:10:09:690] **Speaker 1:** Some of you saw that the 4th resolution was a
[00:10:09:690 - 00:10:12:489] **Speaker 1:** little bit higher than the 3rd rather than lower, I
[00:10:12:489 - 00:10:15:549] **Speaker 1:** think um as as shown in the tutorial.
[00:10:16:169 - 00:10:18:369] **Speaker 1:** So the main thing to look at is the difference
[00:10:18:369 - 00:10:21:669] **Speaker 1:** between each subsequent mesh rather than the actual absolute value,
[00:10:22:210 - 00:10:28:729] **Speaker 1:** um, because ultimately we're trying to Converge our simulation and
[00:10:28:729 - 00:10:30:049] **Speaker 1:** then matched against experiments.
[00:10:30:090 - 00:10:31:429] **Speaker 1:** So that's that validation step.
[00:10:32:820 - 00:10:35:559] **Speaker 1:** So we've got some examples here of different element orders.
[00:10:37:369 - 00:10:40:869] **Speaker 1:** So if we have a large problem, halving the element
[00:10:40:869 - 00:10:41:450] **Speaker 1:** size.
[00:10:43:500 - 00:10:50:630] **Speaker 1:** Will increase sorry, halving the element size, so, HD equals
[00:10:50:630 - 00:10:53:359] **Speaker 1:** 2, for example, is going to increase the solution time
[00:10:53:359 - 00:10:55:479] **Speaker 1:** by um orders of magnitude.
[00:10:55:799 - 00:10:59:400] **Speaker 1:** So here we've said maybe 2020 times for 2D and
[00:10:59:400 - 00:11:00:659] **Speaker 1:** maybe 100 for 3D.
[00:11:01:000 - 00:11:03:859] **Speaker 1:** Uh, and this is particularly the case for time-dependent problems
[00:11:04:440 - 00:11:07:080] **Speaker 1:** because not only are you increasing the number of elements
[00:11:07:080 - 00:11:10:440] **Speaker 1:** in X, Y, and Z, you're also constraining the time
[00:11:10:440 - 00:11:11:760] **Speaker 1:** step size, so delta T.
[00:11:13:820 - 00:11:16:919] **Speaker 1:** Because the solution was also dependent on that that timestamp.
[00:11:17:820 - 00:11:20:750] **Speaker 1:** So that, yeah, sort of blows up really quick in
[00:11:20:750 - 00:11:22:640] **Speaker 1:** terms of um computational time.
[00:11:28:520 - 00:11:35:849] **Speaker 1:** So these 3 examples of approximating, Some defendant variable field,
[00:11:35:900 - 00:11:39:900] **Speaker 1:** maybe it's a displacement, and we're using 101st order elements.
[00:11:41:679 - 00:11:44:799] **Speaker 1:** Versus 16 first-order elements, or we could just use a
[00:11:44:799 - 00:11:46:390] **Speaker 1:** higher-order element like a quadratic.
[00:11:46:479 - 00:11:48:619] **Speaker 1:** So this is the 2nd-order elements.
[00:11:51:750 - 00:11:54:950] **Speaker 1:** So we could either increase the order of the elements,
[00:11:55:030 - 00:11:58:830] **Speaker 1:** so how many, um, Tailor series terms, etc.
[00:11:58:909 - 00:12:01:630] **Speaker 1:** that we're using for, for a particular element, or we
[00:12:01:630 - 00:12:04:229] **Speaker 1:** could just increase the number of elements to linear elements.
[00:12:05:409 - 00:12:08:090] **Speaker 1:** And there's a bit of a trade-off between each, each
[00:12:08:090 - 00:12:08:349] **Speaker 1:** approach.
[00:12:10:309 - 00:12:14:650] **Speaker 1:** Now How do we know that we have a converged
[00:12:14:650 - 00:12:14:909] **Speaker 1:** solution?
[00:12:15:909 - 00:12:20:369] **Speaker 1:** So here we've got a uh A beam and we've
[00:12:20:369 - 00:12:23:210] **Speaker 1:** applied some load at the end, and we might be
[00:12:23:210 - 00:12:26:130] **Speaker 1:** looking at the displacement, subject to that load.
[00:12:27:200 - 00:12:30:750] **Speaker 1:** So we have an unstructured grid here and we've refined
[00:12:30:750 - 00:12:31:530] **Speaker 1:** methodically.
[00:12:32:150 - 00:12:34:869] **Speaker 1:** It looks like it's doubling or quadrupling each time.
[00:12:37:880 - 00:12:41:000] **Speaker 1:** So along the x-axis, we want to define something that
[00:12:41:000 - 00:12:41:919] **Speaker 1:** we're varying.
[00:12:42:039 - 00:12:44:119] **Speaker 1:** So in the, the venture example, we looked at number
[00:12:44:119 - 00:12:47:200] **Speaker 1:** of degrees of freedom on the X-axis or the HD,
[00:12:47:760 - 00:12:48:619] **Speaker 1:** uh, parameter.
[00:12:49:840 - 00:12:52:099] **Speaker 1:** And then on the vertical axis we want to measure.
[00:12:52:909 - 00:12:55:590] **Speaker 1:** Uh, some particular quantity that we're most interested in.
[00:12:55:950 - 00:12:58:549] **Speaker 1:** So if we're interested in the max displacement for this
[00:12:58:549 - 00:13:00:510] **Speaker 1:** beam, that's what we're going to use for the criteria
[00:13:00:510 - 00:13:01:630] **Speaker 1:** for mesh convergence.
[00:13:01:669 - 00:13:03:750] **Speaker 1:** And for the wrench, we looked at that peak stress.
[00:13:06:739 - 00:13:10:539] **Speaker 1:** And we want to compare, perhaps normalising based on the
[00:13:10:539 - 00:13:12:169] **Speaker 1:** most refined mesh, or we could just look at the
[00:13:12:169 - 00:13:13:710] **Speaker 1:** difference between each subsequent mesh.
[00:13:18:359 - 00:13:19:909] **Speaker 1:** So that's mesh convergence.
[00:13:20:609 - 00:13:22:890] **Speaker 1:** So we'll have heaps of practise with that and I
[00:13:22:890 - 00:13:25:450] **Speaker 1:** always make that as a feature in the, um, assignment
[00:13:25:450 - 00:13:27:130] **Speaker 1:** because that's a really important concept.
[00:13:28:340 - 00:13:30:469] **Speaker 1:** Um, the last step here is just looking at different
[00:13:30:469 - 00:13:31:650] **Speaker 1:** element shape functions.
[00:13:32:070 - 00:13:34:830] **Speaker 1:** So not only can we use different interpolating functions to
[00:13:34:830 - 00:13:37:630] **Speaker 1:** represent the independent variable field, so linear versus quadratic elements
[00:13:37:630 - 00:13:38:950] **Speaker 1:** for temperature fields, etc.
[00:13:39:229 - 00:13:43:030] **Speaker 1:** we can also represent the physical shape with different element
[00:13:43:030 - 00:13:44:510] **Speaker 1:** shape function orders.
[00:13:44:909 - 00:13:48:070] **Speaker 1:** So if it's a first-order triangular element, it can't approximate
[00:13:48:070 - 00:13:51:309] **Speaker 1:** this curve very well versus one that has um a
[00:13:51:309 - 00:13:52:270] **Speaker 1:** polynomial fit.
[00:14:00:000 - 00:14:01:190] **Speaker 1:** Roundoff error.
[00:14:01:489 - 00:14:08:250] **Speaker 1:** So Um, It's not so important for our double precision
[00:14:08:250 - 00:14:11:450] **Speaker 1:** computers, but if we have a single precision, so only
[00:14:11:450 - 00:14:12:219] **Speaker 1:** 7 digits.
[00:14:13:030 - 00:14:16:789] **Speaker 1:** To represent a number, uh, we can lose quite a
[00:14:16:789 - 00:14:18:450] **Speaker 1:** bit of accuracy in our results.
[00:14:18:789 - 00:14:20:549] **Speaker 1:** So an example here is that if we, if we
[00:14:20:549 - 00:14:24:869] **Speaker 1:** have two large numbers, 7 with lots of 7s, and
[00:14:25:140 - 00:14:26:609] **Speaker 1:** -7 with a 6.
[00:14:27:570 - 00:14:30:250] **Speaker 1:** Um, and we've got another number that we want to
[00:14:30:250 - 00:14:32:369] **Speaker 1:** compare against, which is smaller than these two.
[00:14:34:940 - 00:14:39:780] **Speaker 1:** If we evaluate A + B + C, so in
[00:14:39:780 - 00:14:44:780] **Speaker 1:** that first order, we have um a large number minus
[00:14:44:780 - 00:14:46:700] **Speaker 1:** a slightly smaller number, so we end up with 1.
[00:14:47:419 - 00:14:50:840] **Speaker 1:** And then plus C, so 1.44 is the result.
[00:14:51:809 - 00:14:52:570] **Speaker 1:** Which is correct.
[00:14:52:969 - 00:14:56:770] **Speaker 1:** If we reordered that operation, which mathematically is equivalent.
[00:14:57:820 - 00:14:58:929] **Speaker 1:** So A, C, and B.
[00:14:59:250 - 00:15:02:690] **Speaker 1:** So A and then plus 0.4, because we've only got
[00:15:02:690 - 00:15:06:890] **Speaker 1:** seven digits in our computer, then it's lost that resolution.
[00:15:07:130 - 00:15:08:650] **Speaker 1:** So it's resolved back to 7.
[00:15:12:150 - 00:15:14:940] **Speaker 1:** And if we take off that next number, we end
[00:15:14:940 - 00:15:17:710] **Speaker 1:** up with 1, so it's now 30% off.
[00:15:18:510 - 00:15:20:789] **Speaker 1:** So that's just an example of the Randolph error.
[00:15:21:400 - 00:15:30:570] **Speaker 1:** Um, So Yeah, I You've probably come across non-dimensionalization already.
[00:15:30:710 - 00:15:32:440] **Speaker 1:** We cover a little bit as well in this course,
[00:15:32:659 - 00:15:38:419] **Speaker 1:** but one of the Advantages for non-dimensionalizing equations is that
[00:15:38:419 - 00:15:42:099] **Speaker 1:** they become more normalised and more uh closer to unity
[00:15:42:099 - 00:15:43:719] **Speaker 1:** or or smaller numbers.
[00:15:44:140 - 00:15:46:059] **Speaker 1:** So that can also reduce the round of error that
[00:15:46:059 - 00:15:47:340] **Speaker 1:** you that you experience.
[00:15:51:190 - 00:15:55:700] **Speaker 1:** So the total error Well, I guess one other point
[00:15:55:700 - 00:15:58:340] **Speaker 1:** is that you'll always have some round of error because
[00:15:58:340 - 00:16:00:520] **Speaker 1:** you're doing lots of, uh, calculations.
[00:16:00:890 - 00:16:04:119] **Speaker 1:** For example, in console, there's thousands and thousands of equations,
[00:16:04:580 - 00:16:06:739] **Speaker 1:** and they're all going to accumulate even if they're very
[00:16:06:739 - 00:16:06:960] **Speaker 1:** small.
[00:16:07:500 - 00:16:09:859] **Speaker 1:** So if you have a really refined mesh, then you
[00:16:09:859 - 00:16:15:719] **Speaker 1:** will have more, um, Uh, more Randolph era.
[00:16:16:489 - 00:16:18:479] **Speaker 1:** So if we have a really fine mesh on the
[00:16:18:479 - 00:16:22:200] **Speaker 1:** left hand side, We have higher roundoff error.
[00:16:23:030 - 00:16:24:440] **Speaker 1:** So that's this first curve.
[00:16:27:859 - 00:16:33:059] **Speaker 1:** And as we have a larger mesh, so coarser resolution,
[00:16:33:510 - 00:16:36:150] **Speaker 1:** our discretization error increases.
[00:16:39:229 - 00:16:42:390] **Speaker 1:** And our total error is the combination of these two.
[00:16:50:890 - 00:16:52:020] **Speaker 1:** And that's what we're left with.
[00:16:52:159 - 00:16:54:940] **Speaker 1:** So the optimum step size might not be the most
[00:16:54:940 - 00:16:55:729] **Speaker 1:** refined mesh.
[00:16:56:340 - 00:16:58:989] **Speaker 1:** In practical terms, uh, you probably won't.
[00:16:59:820 - 00:17:03:770] **Speaker 1:** Reach this region that has, that has, um, significant roundoff
[00:17:03:770 - 00:17:06:180] **Speaker 1:** error, so don't be too concerned, but that's just for
[00:17:06:180 - 00:17:06:859] **Speaker 1:** terminology.
[00:17:09:619 - 00:17:10:099] **Speaker 1:** All right.
[00:17:10:979 - 00:17:12:500] **Speaker 1:** So some guidelines for missing.
[00:17:13:520 - 00:17:17:958] **Speaker 1:** So Obviously straight edges can be represented with those structured
[00:17:17:958 - 00:17:19:499] **Speaker 1:** grids in the single elements.
[00:17:19:958 - 00:17:23:198] **Speaker 1:** Uh, if we had an arc, 90-degree arc, we could
[00:17:23:198 - 00:17:25:159] **Speaker 1:** mesh with two second-order elements.
[00:17:27:109 - 00:17:29:180] **Speaker 1:** Sort of like these type.
[00:17:29:920 - 00:17:34:160] **Speaker 1:** And we'd have um an accuracy of about 0.1%. If
[00:17:34:160 - 00:17:38:000] **Speaker 1:** we meshed with several or eight first-order elements, then we'd
[00:17:38:000 - 00:17:39:040] **Speaker 1:** only get to about 1%.
[00:17:39:160 - 00:17:43:479] **Speaker 1:** So obviously, polynomials fit or quadratics fit better than a
[00:17:43:479 - 00:17:47:280] **Speaker 1:** line to a curve, so nothing too exciting there.
[00:17:49:140 - 00:17:51:609] **Speaker 1:** Um, but with the wrench, you would have seen that
[00:17:51:609 - 00:17:54:900] **Speaker 1:** you had those elements, the, the tetrahedrals and the, the
[00:17:54:900 - 00:17:55:239] **Speaker 1:** mesh.
[00:17:56:089 - 00:18:00:319] **Speaker 1:** So most CFD problems use first-order elements, uh, thermal, thermal
[00:18:00:319 - 00:18:02:270] **Speaker 1:** problems also use first-order elements in there.
[00:18:03:569 - 00:18:07:239] **Speaker 1:** So it was And the idea is that we want
[00:18:07:239 - 00:18:10:280] **Speaker 1:** to try and use gradual transitions between small and large
[00:18:10:280 - 00:18:10:839] **Speaker 1:** elements.
[00:18:14:239 - 00:18:18:099] **Speaker 1:** Emission refinement So start with a mesh that you think.
[00:18:19:189 - 00:18:20:969] **Speaker 1:** will resolve the gradients that you expect.
[00:18:21:069 - 00:18:24:150] **Speaker 1:** So if we think back to this case, where do
[00:18:24:150 - 00:18:24:630] **Speaker 1:** we start?
[00:18:24:709 - 00:18:26:410] **Speaker 1:** What is a suitable mesh to start with?
[00:18:26:829 - 00:18:28:989] **Speaker 1:** It's always best to start with the coarsest mesh because
[00:18:28:989 - 00:18:31:260] **Speaker 1:** that runs quicker, uh, and then refine.
[00:18:31:869 - 00:18:35:750] **Speaker 1:** So in the venture example, You, I think just had
[00:18:35:750 - 00:18:38:349] **Speaker 1:** a sort of a default mesh, uh, and then refined
[00:18:38:349 - 00:18:38:989] **Speaker 1:** it further.
[00:18:41:020 - 00:18:43:140] **Speaker 1:** So start with the mesh that you think will generally
[00:18:43:140 - 00:18:43:760] **Speaker 1:** work well.
[00:18:44:670 - 00:18:48:189] **Speaker 1:** Uh, and then add in some more elements where you
[00:18:48:189 - 00:18:53:079] **Speaker 1:** think there will be high, um, Gradient, so In fluid
[00:18:53:079 - 00:18:55:569] **Speaker 1:** mechanics, we want to resolve those boundary layers.
[00:18:55:729 - 00:19:00:939] **Speaker 1:** So you'd have inflation layers, um, Temperature isn't as exciting
[00:19:01:439 - 00:19:04:040] **Speaker 1:** in terms of having to resolve nonlinear effects.
[00:19:04:160 - 00:19:06:339] **Speaker 1:** So you don't need to have two refined goods.
[00:19:06:880 - 00:19:10:709] **Speaker 1:** Um, but if there is some Stress concentration or something,
[00:19:10:719 - 00:19:12:260] **Speaker 1:** you might want to add in more elements.
[00:19:14:560 - 00:19:17:329] **Speaker 1:** You can use adaptive mesh refinement to automatically refine the
[00:19:17:329 - 00:19:20:449] **Speaker 1:** mesh subject to some error or those ah gradients.
[00:19:22:290 - 00:19:25:150] **Speaker 1:** And it takes time and RAM to solve.
[00:19:26:979 - 00:19:30:170] **Speaker 1:** If the solution doesn't change to some sort of tolerance,
[00:19:30:420 - 00:19:33:380] **Speaker 1:** so the wrench, uh, I think it was changing within
[00:19:33:380 - 00:19:35:599] **Speaker 1:** one or two, megapa scales.
[00:19:35:979 - 00:19:38:780] **Speaker 1:** Uh, maybe if it's within like 1% or 0.1%, then
[00:19:38:780 - 00:19:39:959] **Speaker 1:** that's, that's good.
[00:19:40:400 - 00:19:43:010] **Speaker 1:** So obviously that's going to be case dependent or problem-specific.
[00:19:43:380 - 00:19:46:420] **Speaker 1:** If you were looking at a bridge design and it
[00:19:46:420 - 00:19:48:380] **Speaker 1:** was within a couple of percent, that's probably fine.
[00:19:48:459 - 00:19:50:400] **Speaker 1:** You've got a factor of safety of 3 or 4,
[00:19:50:979 - 00:19:52:030] **Speaker 1:** because you don't know what trucks are going to go
[00:19:52:030 - 00:19:52:640] **Speaker 1:** over the bridge.
[00:19:53:099 - 00:19:56:219] **Speaker 1:** But if you're designing an error, um, like a, like
[00:19:56:219 - 00:19:59:239] **Speaker 1:** a plane, then you might want to have tighter tolerances
[00:19:59:739 - 00:20:03:260] **Speaker 1:** because every kilogramme or whatever you're adding is is going
[00:20:03:260 - 00:20:04:420] **Speaker 1:** to cost fuel.
[00:20:05:239 - 00:20:07:420] **Speaker 1:** And um yeah, safety.
[00:20:08:959 - 00:20:10:910] **Speaker 1:** So that is dependent on the problem.
[00:20:17:000 - 00:20:18:609] **Speaker 1:** How finely do we need to mesh?
[00:20:19:079 - 00:20:22:979] **Speaker 1:** So start as close as possible, compute, refine, refine, refine
[00:20:23:280 - 00:20:26:560] **Speaker 1:** and monitor of what is, um, what is of interest
[00:20:26:560 - 00:20:26:839] **Speaker 1:** to you.
[00:20:26:949 - 00:20:30:500] **Speaker 1:** So again, there's no point looking at the, the stress
[00:20:30:500 - 00:20:33:920] **Speaker 1:** and the um bolt of that example if we wanted
[00:20:33:920 - 00:20:35:119] **Speaker 1:** to analyse the wrench.
[00:20:35:520 - 00:20:37:260] **Speaker 1:** Um, so obviously pick a value.
[00:20:38:170 - 00:20:39:469] **Speaker 1:** That that is suitable.
[00:20:42:130 - 00:20:43:930] **Speaker 1:** Or use adaptive mesh refinement.
[00:20:44:199 - 00:20:46:209] **Speaker 1:** So console has this, uh, we don't cover it in
[00:20:46:209 - 00:20:46:829] **Speaker 1:** this course.
[00:20:48:310 - 00:20:49:790] **Speaker 1:** In detail, um.
[00:20:51:500 - 00:20:53:780] **Speaker 1:** Here's just repeating what we said earlier, so we've got
[00:20:53:780 - 00:20:56:579] **Speaker 1:** an increasing number of elements or degrees of freedom, and
[00:20:56:579 - 00:20:59:550] **Speaker 1:** then we're checking what the solution, uh, provides at each
[00:20:59:550 - 00:21:00:619] **Speaker 1:** of these steps.
[00:21:02:099 - 00:21:04:780] **Speaker 1:** And this is a flow chart for the adaptive mesh
[00:21:04:780 - 00:21:06:000] **Speaker 1:** refinement algorithm.
[00:21:08:760 - 00:21:11:380] **Speaker 1:** And At least in this class.
[00:21:12:359 - 00:21:15:229] **Speaker 1:** You can just refine the mesh more and more rather
[00:21:15:229 - 00:21:16:199] **Speaker 1:** than bothering with this.
[00:21:16:560 - 00:21:19:140] **Speaker 1:** But if you've got quite a complex case, this might,
[00:21:19:280 - 00:21:21:239] **Speaker 1:** might be worthwhile investigating.
[00:21:22:069 - 00:21:23:569] **Speaker 1:** Um, most of the problems I get you to do
[00:21:23:569 - 00:21:26:459] **Speaker 1:** a smaller scale and maybe 2D.
[00:21:32:089 - 00:21:33:180] **Speaker 1:** Um, Med quality.
[00:21:34:160 - 00:21:38:579] **Speaker 1:** So We talked a little bit about skewness, so we
[00:21:38:579 - 00:21:40:979] **Speaker 1:** don't want the elements to be too skewed, um, just
[00:21:40:979 - 00:21:43:000] **Speaker 1:** with how the interplating functions work.
[00:21:44:069 - 00:21:46:619] **Speaker 1:** So we can define a SKU.
[00:21:47:599 - 00:21:49:520] **Speaker 1:** With this equation.
[00:21:50:209 - 00:21:52:890] **Speaker 1:** Um, so essentially it's just how far away it is
[00:21:52:890 - 00:21:54:589] **Speaker 1:** from the optimal angle.
[00:21:55:209 - 00:21:56:189] **Speaker 1:** So a triangle.
[00:21:57:599 - 00:22:00:319] **Speaker 1:** Um, has 180 degrees on the interior.
[00:22:00:819 - 00:22:04:400] **Speaker 1:** So if each one is 60, then it's sort of
[00:22:04:400 - 00:22:05:640] **Speaker 1:** equal angle.
[00:22:06:530 - 00:22:12:920] **Speaker 1:** Um So, Yeah.
[00:22:14:130 - 00:22:16:260] **Speaker 1:** You can evaluate that, so that's what theta E will
[00:22:16:260 - 00:22:16:459] **Speaker 1:** be.
[00:22:18:540 - 00:22:25:319] **Speaker 1:** Um So SKUN ranges from 0 up to 1, and
[00:22:25:319 - 00:22:27:680] **Speaker 1:** you can analyse the mesh quality and and console or
[00:22:27:680 - 00:22:29:219] **Speaker 1:** any other sort of software package.
[00:22:30:520 - 00:22:33:239] **Speaker 1:** Smoothness, so we want to change the element size gradually.
[00:22:33:560 - 00:22:36:319] **Speaker 1:** So rather than having really large jumps, like we see
[00:22:36:319 - 00:22:37:979] **Speaker 1:** on the right, we want to have a smooth change.
[00:22:39:339 - 00:22:41:869] **Speaker 1:** Uh, the exception here is for those inflation layers.
[00:22:41:939 - 00:22:44:989] **Speaker 1:** The boundary layers are OK to have, um, a bit
[00:22:44:989 - 00:22:45:469] **Speaker 1:** of a jump.
[00:22:47:180 - 00:22:48:290] **Speaker 1:** Aspect ratio.
[00:22:48:619 - 00:22:50:780] **Speaker 1:** So sort of similar to these large jump sizes, we,
[00:22:50:900 - 00:22:53:979] **Speaker 1:** we want to reduce the um the aspect ratio.
[00:22:54:060 - 00:22:57:979] **Speaker 1:** So ideally it's about one, but the inflation layers will
[00:22:57:979 - 00:22:58:880] **Speaker 1:** be a little bit higher.
[00:23:02:520 - 00:23:04:329] **Speaker 1:** Striving for a quality mesh.
[00:23:04:520 - 00:23:08:839] **Speaker 1:** So a poor quality grid will cause inaccurate solutions or
[00:23:08:839 - 00:23:10:020] **Speaker 1:** a slow convergence.
[00:23:11:000 - 00:23:15:280] **Speaker 1:** Um I don't think we give an example of that
[00:23:15:280 - 00:23:15:729] **Speaker 1:** in your labs.
[00:23:15:770 - 00:23:18:270] **Speaker 1:** We try and avoid that, um, but you might find
[00:23:18:270 - 00:23:21:209] **Speaker 1:** that in your final year projects next year, um, if
[00:23:21:209 - 00:23:24:199] **Speaker 1:** you create measures that aren't quite Good.
[00:23:25:020 - 00:23:27:939] **Speaker 1:** So minimising the equal angle ske SKU, uh, we've got
[00:23:27:939 - 00:23:30:979] **Speaker 1:** hexin quad cells, SKUness should not exceed 0.85 as a
[00:23:30:979 - 00:23:34:939] **Speaker 1:** rule of thumb and tri is 0.85 and tetrahedral is
[00:23:34:939 - 00:23:35:680] **Speaker 1:** 0.9.
[00:23:36:810 - 00:23:38:410] **Speaker 1:** Um, yeah.
[00:23:40:849 - 00:23:41:489] **Speaker 1:** All right.
[00:23:41:890 - 00:23:43:689] **Speaker 1:** So generation of structured grids.
[00:23:43:729 - 00:23:45:920] **Speaker 1:** So how can we create these, these mapped grids?
[00:23:46:290 - 00:23:48:449] **Speaker 1:** They should be reasonably straightforward, especially if it was just
[00:23:48:449 - 00:23:49:589] **Speaker 1:** a square or rectangle.
[00:23:50:189 - 00:23:52:290] **Speaker 1:** Uh, we're going to talk about the algebraic grid generation
[00:23:52:290 - 00:23:54:369] **Speaker 1:** and the elliptic grid generation.
[00:23:55:270 - 00:23:58:489] **Speaker 1:** So both of these techniques rely on finding some mapping.
[00:23:59:670 - 00:24:00:979] **Speaker 1:** Between the physical space.
[00:24:01:810 - 00:24:07:329] **Speaker 1:** Ah denoted with X and Y, and the logical, or
[00:24:07:329 - 00:24:11:410] **Speaker 1:** um, yeah, logical domain, Shy and Ada.
[00:24:13:630 - 00:24:17:680] **Speaker 1:** Sort of Got discrete values of shy and ata that
[00:24:17:680 - 00:24:21:319] **Speaker 1:** are integers 0 to n and m and they represent
[00:24:21:319 - 00:24:22:619] **Speaker 1:** the the computational domain.
[00:24:24:459 - 00:24:26:180] **Speaker 1:** And those X Y's are the physical coordinates.
[00:24:26:420 - 00:24:28:400] **Speaker 1:** So here's an example.
[00:24:29:989 - 00:24:33:229] **Speaker 1:** Of, uh, an arc, so that could be part of
[00:24:33:229 - 00:24:34:849] **Speaker 1:** the OH grid that we looked at earlier.
[00:24:36:060 - 00:24:38:140] **Speaker 1:** And this is the physical domain, and we want to
[00:24:38:140 - 00:24:41:250] **Speaker 1:** map that across to these nice Excel spreadsheet looking rows
[00:24:41:250 - 00:24:42:859] **Speaker 1:** and columns in the logical domain.
[00:24:43:939 - 00:24:46:760] **Speaker 1:** So that's what these two schemes are, the algebraic and
[00:24:46:760 - 00:24:48:550] **Speaker 1:** elliptic techniques.
[00:24:49:050 - 00:24:50:729] **Speaker 1:** So first algebraic grid generation.
[00:24:52:180 - 00:24:57:400] **Speaker 1:** Essentially what we're gonna do is look at our Domain,
[00:24:57:479 - 00:24:58:420] **Speaker 1:** we have 4 edges.
[00:24:58:579 - 00:25:02:500] **Speaker 1:** So we've got 4 edges to map across and we're
[00:25:02:500 - 00:25:06:000] **Speaker 1:** going to uniformly distribute the nodes along each edge.
[00:25:07:000 - 00:25:08:520] **Speaker 1:** And then draw between them.
[00:25:09:349 - 00:25:12:479] **Speaker 1:** So We prescribe our good points at the boundary of
[00:25:12:479 - 00:25:13:260] **Speaker 1:** the physical domain.
[00:25:14:800 - 00:25:19:069] **Speaker 1:** With X S and S on the southern.
[00:25:20:260 - 00:25:22:390] **Speaker 1:** Northern, eastern and western faces.
[00:25:24:500 - 00:25:28:339] **Speaker 1:** And the points within the interior are given by this
[00:25:28:339 - 00:25:29:060] **Speaker 1:** equation.
[00:25:29:540 - 00:25:33:780] **Speaker 1:** So I guess if you just look at each term,
[00:25:33:819 - 00:25:36:800] **Speaker 1:** it's just ranging between each edge.
[00:25:37:339 - 00:25:40:920] **Speaker 1:** So 1 minus ata over M, theta being the logical.
[00:25:41:780 - 00:25:45:599] **Speaker 1:** Part, so it's just ranging from 0 up to 1.
[00:25:49:160 - 00:25:52:209] **Speaker 1:** The feature of this, uh, algebraic regeneration method is that
[00:25:52:209 - 00:25:54:969] **Speaker 1:** the coordinates of all the interior points are defined in
[00:25:54:969 - 00:25:56:180] **Speaker 1:** terms of the boundary points.
[00:25:56:449 - 00:25:57:890] **Speaker 1:** So it's really straightforward to calculate.
[00:25:58:020 - 00:26:01:729] **Speaker 1:** This is deterministic or just you evaluate it directly and
[00:26:01:729 - 00:26:02:189] **Speaker 1:** quickly.
[00:26:05:380 - 00:26:07:930] **Speaker 1:** It's also known as the transfinite interpolation.
[00:26:09:439 - 00:26:11:989] **Speaker 1:** Uh, and the advantages are that it's very easy to
[00:26:11:989 - 00:26:12:439] **Speaker 1:** implement.
[00:26:12:640 - 00:26:15:479] **Speaker 1:** You could write some code, and it's got very little
[00:26:15:479 - 00:26:18:500] **Speaker 1:** computational effort because they were just evaluating this expression.
[00:26:19:500 - 00:26:20:900] **Speaker 1:** For each point.
[00:26:21:099 - 00:26:22:439] **Speaker 1:** So that's equation 5.
[00:26:25:030 - 00:26:27:339] **Speaker 1:** So the disadvantage is that it might not always be
[00:26:27:339 - 00:26:28:119] **Speaker 1:** applicable.
[00:26:28:579 - 00:26:30:060] **Speaker 1:** So depending on the shape, if it's sort of got
[00:26:30:060 - 00:26:36:670] **Speaker 1:** a curve that you can't interpolate between, um, Then it's,
[00:26:36:880 - 00:26:37:000] **Speaker 1:** yeah.
[00:26:37:920 - 00:26:42:760] **Speaker 1:** Not, not civil, uh, the boundary irregularities can also propagate
[00:26:42:760 - 00:26:45:880] **Speaker 1:** throughout the domain representing a, a poor mesh quality.
[00:26:49:949 - 00:26:51:609] **Speaker 1:** So the example here.
[00:26:52:890 - 00:26:55:969] **Speaker 1:** At the top is the algebraic grid generation.
[00:26:57:270 - 00:27:00:699] **Speaker 1:** So we can see that it has quite skewed elements
[00:27:00:709 - 00:27:02:339] **Speaker 1:** close to the interior corner.
[00:27:03:089 - 00:27:05:670] **Speaker 1:** And that's just how, how it's set up.
[00:27:06:670 - 00:27:09:670] **Speaker 1:** Um So what could we do instead?
[00:27:10:079 - 00:27:11:949] **Speaker 1:** So we're gonna look at the elliptic grid generation.
[00:27:12:150 - 00:27:14:989] **Speaker 1:** So some more Laplace equations because we've learned about those
[00:27:14:989 - 00:27:15:329] **Speaker 1:** now.
[00:27:16:160 - 00:27:19:589] **Speaker 1:** So this requires us to solve these two equations.
[00:27:20:310 - 00:27:23:800] **Speaker 1:** We've got Shai and Ada differentiated in X and Y.
[00:27:25:000 - 00:27:26:660] **Speaker 1:** So this is solved in the physical domain.
[00:27:28:810 - 00:27:32:010] **Speaker 1:** But these equations are actually in the logical domain.
[00:27:33:680 - 00:27:37:329] **Speaker 1:** So There's maths involved, which I'm not going to go
[00:27:37:510 - 00:27:41:380] **Speaker 1:** into, but applying the chain rule, we can get some
[00:27:41:380 - 00:27:42:790] **Speaker 1:** more equations, 8 and 9.
[00:27:44:030 - 00:27:47:550] **Speaker 1:** So we've converted from the logical domain to the physical
[00:27:47:550 - 00:27:48:010] **Speaker 1:** domain.
[00:27:49:050 - 00:27:51:849] **Speaker 1:** And then we're going to solve these equations 8 and
[00:27:51:849 - 00:27:54:319] **Speaker 1:** 9 to to generate the elliptic.
[00:27:57:530 - 00:27:59:599] **Speaker 1:** So you can see here that it looks more diffuse,
[00:27:59:680 - 00:28:04:520] **Speaker 1:** it's more curved and, uh, distributed better.
[00:28:05:250 - 00:28:08:609] **Speaker 1:** So that's the main advantage for these elliptic, uh, grids.
[00:28:09:089 - 00:28:11:770] **Speaker 1:** It takes longer to generate because we're solving some more
[00:28:11:770 - 00:28:12:489] **Speaker 1:** PDEs.
[00:28:16:300 - 00:28:18:699] **Speaker 1:** And the main features that we want to list is
[00:28:18:699 - 00:28:23:300] **Speaker 1:** the governing equations are nonlinear, um, that's equations 8 and
[00:28:23:300 - 00:28:23:760] **Speaker 1:** 9.
[00:28:25:680 - 00:28:28:449] **Speaker 1:** And require an iterative solution process.
[00:28:28:839 - 00:28:31:050] **Speaker 1:** So the main advantage is that it generates more smoother
[00:28:31:750 - 00:28:32:239] **Speaker 1:** grids.
[00:28:32:949 - 00:28:35:770] **Speaker 1:** And that disadvantage being that it's more computationally expensive.
[00:28:41:780 - 00:28:42:219] **Speaker 1:** All right.
[00:28:43:260 - 00:28:47:069] **Speaker 1:** So it was structured grids, now some unstructured grid techniques.
[00:28:47:790 - 00:28:51:469] **Speaker 1:** So unstructured mass generation, uh, have been developed because we
[00:28:51:469 - 00:28:54:390] **Speaker 1:** don't always have nice, uh, domains that we can decompose
[00:28:54:390 - 00:28:55:910] **Speaker 1:** into for structured grids.
[00:28:57:089 - 00:29:00:760] **Speaker 1:** So a couple of techniques that were Uh, briefly skip
[00:29:00:760 - 00:29:05:160] **Speaker 1:** over is the advan advancing front method and the Delaunay
[00:29:05:160 - 00:29:06:060] **Speaker 1:** triangulation method.
[00:29:06:959 - 00:29:09:900] **Speaker 1:** So the advancing front method goes back to the 80s,
[00:29:10:319 - 00:29:10:849] **Speaker 1:** um.
[00:29:11:760 - 00:29:14:310] **Speaker 1:** It's constructed by adding mesh elements.
[00:29:14:520 - 00:29:19:170] **Speaker 1:** So if we've got a square, Domain We're going to,
[00:29:19:290 - 00:29:21:619] **Speaker 1:** uh, sort out the perimeter and then we're going to
[00:29:21:619 - 00:29:24:900] **Speaker 1:** scatter a whole bunch of nodes on the interior and
[00:29:24:900 - 00:29:27:949] **Speaker 1:** the advancing front is essentially going to be connecting those
[00:29:27:949 - 00:29:29:920] **Speaker 1:** nodes and forming triangles.
[00:29:34:109 - 00:29:37:089] **Speaker 1:** So the advantage here is that we can uh create
[00:29:37:319 - 00:29:40:760] **Speaker 1:** reasonably good quality meshes with arbitrary geometries.
[00:29:41:520 - 00:29:47:739] **Speaker 1:** And that disadvantage is, um, That as the front advances,
[00:29:47:750 - 00:29:49:709] **Speaker 1:** we have to compute which is the nearest point.
[00:29:49:869 - 00:29:52:750] **Speaker 1:** So probably doesn't matter too much for smaller domains or
[00:29:52:750 - 00:29:56:069] **Speaker 1:** 2D, but if we're getting into larger 3D with very
[00:29:56:069 - 00:30:00:510] **Speaker 1:** many mesh elements, it could take longer to to create.
[00:30:01:199 - 00:30:05:300] **Speaker 1:** Um So this is the procedure.
[00:30:05:579 - 00:30:08:010] **Speaker 1:** So edges on the boundary are numbered and stored in
[00:30:08:010 - 00:30:09:959] **Speaker 1:** a front vector, so 1 through 12.
[00:30:10:300 - 00:30:13:280] **Speaker 1:** The node closest to the last boundary edge is located
[00:30:13:660 - 00:30:19:030] **Speaker 1:** and that's where we form um Edge 13.
[00:30:20:170 - 00:30:24:180] **Speaker 1:** So edge 12 is removed from the front vector, and
[00:30:24:180 - 00:30:26:859] **Speaker 1:** we're now, This is our front.
[00:30:29:390 - 00:30:32:729] **Speaker 1:** And we repeat that process, so now we form.
[00:30:34:260 - 00:30:37:229] **Speaker 1:** Uh, a new triangle, so edge 13 is removed and
[00:30:37:229 - 00:30:38:310] **Speaker 1:** replaced by 13A.
[00:30:39:250 - 00:30:42:829] **Speaker 1:** And so on So you could imagine that this is,
[00:30:42:890 - 00:30:45:729] **Speaker 1:** uh, yeah, it's a step by step process.
[00:30:45:890 - 00:30:49:010] **Speaker 1:** Maybe you can't do this for in parallel.
[00:30:49:209 - 00:30:52:569] **Speaker 1:** So if you had parallel computing, you'd have to first
[00:30:52:569 - 00:30:56:449] **Speaker 1:** decompose the whole mesh or domain intersections and then operate
[00:30:56:449 - 00:30:59:290] **Speaker 1:** this method on each one and then combine afterwards.
[00:31:01:410 - 00:31:05:250] **Speaker 1:** So the De Launay triangulation method is also from the
[00:31:05:250 - 00:31:07:209] **Speaker 1:** 80s and.
[00:31:08:959 - 00:31:11:119] **Speaker 1:** This provides uh a criterion.
[00:31:13:459 - 00:31:18:010] **Speaker 1:** So, This essentially is making sure that we have a
[00:31:18:010 - 00:31:21:739] **Speaker 1:** reasonably good quality mesh, and that the element sizes aren't
[00:31:21:739 - 00:31:24:180] **Speaker 1:** changing too much between each neighbouring element.
[00:31:28:189 - 00:31:31:750] **Speaker 1:** So we're we're fitting a circle to an element.
[00:31:31:989 - 00:31:34:949] **Speaker 1:** So in blue, we've got a triangle element on the
[00:31:34:949 - 00:31:35:390] **Speaker 1:** left.
[00:31:35:709 - 00:31:38:310] **Speaker 1:** If we fit a circle from those three points, we
[00:31:38:310 - 00:31:40:869] **Speaker 1:** can always define a circle from those three points uniquely.
[00:31:41:689 - 00:31:44:209] **Speaker 1:** We do the same for a matching red element on
[00:31:44:209 - 00:31:44:739] **Speaker 1:** the right.
[00:31:47:170 - 00:31:54:680] **Speaker 1:** And We need to make sure that the the circle
[00:31:54:680 - 00:31:58:079] **Speaker 1:** or sphere does not include any other vertex point of
[00:31:58:079 - 00:31:58:449] **Speaker 1:** the mesh.
[00:31:58:520 - 00:32:02:650] **Speaker 1:** So in this case, The blue circle encompasses all of
[00:32:02:650 - 00:32:04:930] **Speaker 1:** the, the three red nodes.
[00:32:06:310 - 00:32:07:699] **Speaker 1:** So that's not satisfactory.
[00:32:08:410 - 00:32:12:060] **Speaker 1:** The example below we can see that it doesn't quite
[00:32:12:060 - 00:32:14:300] **Speaker 1:** enclose those other nodes, so that's good.
[00:32:14:729 - 00:32:15:770] **Speaker 1:** Likewise with the bottom.
[00:32:21:300 - 00:32:21:979] **Speaker 1:** All right.
[00:32:24:800 - 00:32:27:880] **Speaker 1:** So if we had an existing grid, what we could
[00:32:27:880 - 00:32:31:300] **Speaker 1:** do to more uh refine.
[00:32:32:280 - 00:32:34:680] **Speaker 1:** And we'll do that in the console labs later on,
[00:32:34:880 - 00:32:38:300] **Speaker 1:** um, is to add a new node in the interior.
[00:32:39:719 - 00:32:43:719] **Speaker 1:** And then form a mesh that that corresponds with that
[00:32:43:719 - 00:32:44:160] **Speaker 1:** new node.
[00:32:46:719 - 00:32:49:959] **Speaker 1:** So, yeah, not terribly exciting, but.
[00:32:51:609 - 00:32:55:890] **Speaker 1:** We have only introduced the, um, basics of grid generation.
[00:32:56:099 - 00:32:59:510] **Speaker 1:** So there's, there must be whole courses on, on mesh
[00:32:59:510 - 00:33:03:109] **Speaker 1:** generation, I'm sure, not here, but somewhere in the world.
[00:33:03:640 - 00:33:05:390] **Speaker 1:** Um, it's a very vast topic.
[00:33:05:609 - 00:33:07:729] **Speaker 1:** It's very mature in the sense that it's been researched
[00:33:07:729 - 00:33:08:410] **Speaker 1:** for a long time.
[00:33:08:560 - 00:33:12:770] **Speaker 1:** Um as those mesh generation techniques that are quite elementary
[00:33:12:770 - 00:33:13:930] **Speaker 1:** were developed back in the 80s.
[00:33:14:010 - 00:33:15:619] **Speaker 1:** Obviously, there's newer ones since.
[00:33:17:020 - 00:33:20:219] **Speaker 1:** Most of the software packages come with some mesh generation,
[00:33:21:140 - 00:33:25:160] **Speaker 1:** Features so console does fluent for CFD etc.
[00:33:25:619 - 00:33:30:180] **Speaker 1:** Um, there's an open source one or freeware Gesh ah
[00:33:30:180 - 00:33:33:180] **Speaker 1:** you could use for your for your open-source packages.
[00:33:35:660 - 00:33:36:239] **Speaker 1:** All right.
[00:33:38:869 - 00:33:41:030] **Speaker 1:** Any questions on meshing?
[00:33:44:630 - 00:33:46:709] **Speaker 1:** It's really just a whole bunch of theory, which is
[00:33:46:709 - 00:33:50:140] **Speaker 1:** always My least favourite to get work through in the
[00:33:50:140 - 00:33:52:939] **Speaker 1:** lecture, but um hopefully a lot of it will sort
[00:33:52:939 - 00:33:54:420] **Speaker 1:** of be mapping across to what you've done in the
[00:33:54:420 - 00:33:57:780] **Speaker 1:** lab so far yesterday and also in the next week's.
[00:34:03:670 - 00:34:07:449] **Speaker 1:** Um, I posted this up on the Um, announcement on
[00:34:07:449 - 00:34:10:648] **Speaker 1:** Monday, but this seminar next week.
[00:34:10:800 - 00:34:12:469] **Speaker 1:** I don't know if anyone's still around over the lech
[00:34:12:469 - 00:34:12:898] **Speaker 1:** break.
[00:34:13:229 - 00:34:16:699] **Speaker 1:** Um, but if you're interested to see what people are
[00:34:16:699 - 00:34:19:709] **Speaker 1:** doing, I guess, in research, uh, especially the ones that
[00:34:19:709 - 00:34:23:449] **Speaker 1:** are doing the biomed minor, but also for everyone, um,
[00:34:23:719 - 00:34:25:878] **Speaker 1:** to see what people are doing with simulations, maybe it
[00:34:25:878 - 00:34:27:219] **Speaker 1:** would be interesting to some of you.
[00:34:27:550 - 00:34:30:658] **Speaker 1:** That's over in the John Britton building, um, 1 to
[00:34:30:658 - 00:34:32:219] **Speaker 1:** 2 p.m. on Thursday next week.
[00:34:34:669 - 00:34:35:378] **Speaker 1:** All right.
[00:34:37:020 - 00:34:38:908] **Speaker 1:** The classic question is always, oh, what, what, why are
[00:34:38:908 - 00:34:41:030] **Speaker 1:** we doing these equations, why, why are we doing this
[00:34:41:030 - 00:34:43:530] **Speaker 1:** work, so I don't know, it's a, it's an applied
[00:34:43:898 - 00:34:47:810] **Speaker 1:** um, seminar in, in a sense.
[00:34:49:128 - 00:34:53:280] **Speaker 1:** From some, yeah, quite advanced or senior professors, so should
[00:34:53:280 - 00:34:53:570] **Speaker 1:** be good.
[00:34:55:590 - 00:35:00:770] **Speaker 1:** All right So we've got some time, we can go
[00:35:00:770 - 00:35:01:149] **Speaker 1:** through.
[00:35:02:250 - 00:35:04:419] **Speaker 1:** Whatever you want, or we can go through chapter 3.
[00:35:05:959 - 00:35:07:699] **Speaker 1:** Has anyone got any questions?
[00:35:09:280 - 00:35:11:449] **Speaker 1:** No one ever has questions, which is, which is fine,
[00:35:11:560 - 00:35:12:189] **Speaker 1:** but yeah.
[00:35:20:610 - 00:35:20:870] **Speaker 1:** No fishing.
[00:35:22:659 - 00:35:23:020] **Speaker 1:** All right.
[00:35:29:100 - 00:35:33:030] **Speaker 1:** Alright, I'm going to chapter 3, page 25 on your
[00:35:33:030 - 00:35:33:429] **Speaker 1:** course reader.
[00:35:34:399 - 00:35:38:310] **Speaker 1:** So we've looked at solving the elliptic PDEs with the
[00:35:38:310 - 00:35:40:320] **Speaker 1:** separation of variables, so the analytical method.
[00:35:40:600 - 00:35:42:520] **Speaker 1:** What we can do also is to use a finite
[00:35:42:520 - 00:35:43:199] **Speaker 1:** difference scheme.
[00:35:44:459 - 00:35:49:060] **Speaker 1:** So different scheme is essentially discretizing the whole grid or
[00:35:49:239 - 00:35:51:520] **Speaker 1:** discretizing the computational domain into a grid.
[00:35:52:300 - 00:35:55:709] **Speaker 1:** Of, of these nodes and then we're going to approximate
[00:35:55:709 - 00:35:58:469] **Speaker 1:** the equation at each of these nodes.
[00:35:58:939 - 00:36:02:810] **Speaker 1:** So we're gonna apply differencing for our PDE.
[00:36:03:979 - 00:36:06:209] **Speaker 1:** So some characteristics of our finite difference model.
[00:36:06:449 - 00:36:10:729] **Speaker 1:** So we've got a computational grid covered by these nodes.
[00:36:11:689 - 00:36:13:969] **Speaker 1:** In 2D, it's so.
[00:36:14:040 - 00:36:15:969] **Speaker 1:** In 3D, you can imagine that the same in a
[00:36:15:969 - 00:36:16:649] **Speaker 1:** third direction.
[00:36:18:550 - 00:36:20:979] **Speaker 1:** So the problem is specified in terms of our PDEs
[00:36:20:979 - 00:36:24:709] **Speaker 1:** and math statement and our boundary conditions, so.
[00:36:26:110 - 00:36:28:560] **Speaker 1:** Yeah, I guess had a good conversation with one of,
[00:36:28:689 - 00:36:30:229] **Speaker 1:** one of your classmates about the boundary conditions.
[00:36:30:280 - 00:36:35:479] **Speaker 1:** So we need boundary conditions to solve our PDEs, um,
[00:36:36:520 - 00:36:38:129] **Speaker 1:** Otherwise, yeah, we don't have a solution.
[00:36:38:330 - 00:36:40:530] **Speaker 1:** We don't have a unique solution to our equation, and
[00:36:40:530 - 00:36:41:679] **Speaker 1:** it's not specific to our case.
[00:36:41:729 - 00:36:45:550] **Speaker 1:** So whether it has a temperature distribution or that force
[00:36:45:550 - 00:36:47:610] **Speaker 1:** that we apply to that wrench, uh, we, we need
[00:36:47:610 - 00:36:49:389] **Speaker 1:** a boundary condition to, to solve.
[00:36:51:209 - 00:36:55:060] **Speaker 1:** So the values of our variable temperature, for example, are
[00:36:55:060 - 00:36:56:979] **Speaker 1:** defined at each of these grid points.
[00:36:57:260 - 00:36:58:620] **Speaker 1:** So I've labelled T.
[00:37:00:290 - 00:37:03:489] **Speaker 1:** IJ as an arbitrary node.
[00:37:05:120 - 00:37:08:860] **Speaker 1:** So depending on which node we look at corresponds to
[00:37:09:120 - 00:37:09:959] **Speaker 1:** this convention.
[00:37:11:040 - 00:37:14:659] **Speaker 1:** The node to the right is 1 + 1 and
[00:37:14:659 - 00:37:16:679] **Speaker 1:** then to the left is I minus 1 and the
[00:37:16:679 - 00:37:21:840] **Speaker 1:** vertical direction is uh described with the second index J.
[00:37:22:050 - 00:37:23:719] **Speaker 1:** So we've got J +1, J minus 1.
[00:37:25:409 - 00:37:27:689] **Speaker 1:** The derivatives at each good point is going to be
[00:37:27:689 - 00:37:30:889] **Speaker 1:** approximated by our finite difference scheme.
[00:37:32:310 - 00:37:34:899] **Speaker 1:** And we're gonna have an order of accuracy that scales
[00:37:34:899 - 00:37:38:330] **Speaker 1:** with delta X and delta Y, which is our spacings.
[00:37:38:989 - 00:37:39:949] **Speaker 1:** So delta X.
[00:37:42:659 - 00:37:43:340] **Speaker 1:** And data.
[00:37:44:409 - 00:37:44:899] **Speaker 1:** Why?
[00:37:49:429 - 00:37:51:550] **Speaker 1:** So our discrete solution.
[00:37:53:179 - 00:37:55:379] **Speaker 1:** Once we've discretized it, is going to be forced to
[00:37:55:379 - 00:37:57:939] **Speaker 1:** satisfy the governing PDEs and boundary conditions.
[00:37:58:939 - 00:38:00:300] **Speaker 1:** At these grid points.
[00:38:01:169 - 00:38:03:030] **Speaker 1:** And what we're going to end up with is an
[00:38:03:030 - 00:38:04:469] **Speaker 1:** algebraic set of equations.
[00:38:05:449 - 00:38:07:929] **Speaker 1:** And we're gonna have all these unknown temperature values at
[00:38:07:929 - 00:38:09:489] **Speaker 1:** each node, DIJ.
[00:38:14:040 - 00:38:16:550] **Speaker 1:** So this is going to be linear for our, this
[00:38:16:550 - 00:38:18:949] **Speaker 1:** is gonna be a linear set of equations for a
[00:38:18:949 - 00:38:20:030] **Speaker 1:** linear PDE.
[00:38:20:750 - 00:38:23:590] **Speaker 1:** So we're really only looking at linear PDEs in this
[00:38:23:590 - 00:38:28:110] **Speaker 1:** course, um, so elliptic, parabolic hyperbolic equations, um.
[00:38:28:909 - 00:38:34:300] **Speaker 1:** Yeah We're not going to dive into nonlinear equations.
[00:38:37:570 - 00:38:39:020] **Speaker 1:** All right, so an example.
[00:38:39:520 - 00:38:41:500] **Speaker 1:** If we've got an elastic bod fixed at one end
[00:38:41:760 - 00:38:43:699] **Speaker 1:** and loaded with a force on the other.
[00:38:44:629 - 00:38:47:929] **Speaker 1:** Uh, so this is a fixed displacement on the left
[00:38:48:550 - 00:38:49:750] **Speaker 1:** and then a force on the right.
[00:38:50:590 - 00:38:53:879] **Speaker 1:** Our displacement field and the axial direction is given by
[00:38:53:879 - 00:38:54:219] **Speaker 1:** you.
[00:38:55:080 - 00:38:58:810] **Speaker 1:** Uh, sigma is our axial stress and A is our
[00:38:58:810 - 00:38:59:870] **Speaker 1:** cross-sectional area.
[00:39:05:149 - 00:39:09:889] **Speaker 1:** So the equation governing the displacement inside this rod.
[00:39:10:310 - 00:39:12:669] **Speaker 1:** So our dependent variable is you, the displacement, we want
[00:39:12:669 - 00:39:15:469] **Speaker 1:** to figure out how much is the rod stretched or
[00:39:15:469 - 00:39:15:870] **Speaker 1:** performed.
[00:39:17:530 - 00:39:22:489] **Speaker 1:** We've got a differential DY D X A E.
[00:39:23:520 - 00:39:26:639] **Speaker 1:** D U I D X equal to 0.
[00:39:29:719 - 00:39:31:600] **Speaker 1:** So this is essentially a statement of the, the force
[00:39:31:600 - 00:39:37:729] **Speaker 1:** balance and we Have F of X equal to a
[00:39:37:729 - 00:39:40:139] **Speaker 1:** sigma X or varying with X.
[00:39:41:040 - 00:39:43:689] **Speaker 1:** Equal to AEDu by DX and this is from Hook's
[00:39:43:689 - 00:39:43:800] **Speaker 1:** law.
[00:39:58:590 - 00:40:02:000] **Speaker 1:** And we have a full derivative, so that it is
[00:40:02:000 - 00:40:02:699] **Speaker 1:** a D.
[00:40:04:699 - 00:40:06:870] **Speaker 1:** So it's not a partial derivative, it's a full derivative
[00:40:06:870 - 00:40:09:219] **Speaker 1:** because the displacement field in this case is only varying
[00:40:09:219 - 00:40:09:510] **Speaker 1:** in X.
[00:40:09:750 - 00:40:12:870] **Speaker 1:** So if it was in 2D, uh, then we'd have
[00:40:12:870 - 00:40:13:790] **Speaker 1:** partial derivatives.
[00:40:15:909 - 00:40:17:750] **Speaker 1:** So our boundary conditions.
[00:40:20:739 - 00:40:23:379] **Speaker 1:** What are our, well, what is our boundary condition on
[00:40:23:379 - 00:40:24:120] **Speaker 1:** the left-hand side?
[00:40:38:679 - 00:40:41:520] **Speaker 1:** It's fixed, yeah, which, if it's fixed, it means it's
[00:40:41:520 - 00:40:42:020] **Speaker 1:** not moving.
[00:40:42:340 - 00:40:43:959] **Speaker 1:** So our displacement is going to be zero.
[00:40:49:250 - 00:40:51:429] **Speaker 1:** And the boundary condition on the right.
[00:40:56:580 - 00:40:58:159] **Speaker 1:** So it's something for the force if.
[00:41:00:709 - 00:41:02:270] **Speaker 1:** At the right-hand side.
[00:41:02:350 - 00:41:04:870] **Speaker 1:** So where X is equal to L, that right-hand end.
[00:41:07:939 - 00:41:12:000] **Speaker 1:** is equal to AE D by D X.
[00:41:16:750 - 00:41:25:270] **Speaker 1:** evaluated at X equal to L is equal to Our
[00:41:25:270 - 00:41:26:310] **Speaker 1:** prescribed force.
[00:41:27:489 - 00:41:35:090] **Speaker 1:** If not So what you can do and we'll do
[00:41:35:090 - 00:41:37:520] **Speaker 1:** later, uh, it's, I don't know if we'll have time.
[00:41:37:770 - 00:41:41:449] **Speaker 1:** We'll finish this chapter off, um, next term, but you
[00:41:41:449 - 00:41:43:689] **Speaker 1:** can obviously solve this equation analytically.
[00:41:43:929 - 00:41:45:429] **Speaker 1:** It's a 2nd order derivative.
[00:41:46:209 - 00:41:48:729] **Speaker 1:** And X so we can integrate twice and we get
[00:41:48:729 - 00:41:49:250] **Speaker 1:** the solution.
[00:41:49:949 - 00:41:52:560] **Speaker 1:** But we're going through this example, uh, because it's just
[00:41:52:560 - 00:41:54:919] **Speaker 1:** a nice gentle introduction to finite differencing.
[00:41:56:780 - 00:42:00:310] **Speaker 1:** So instead of solving analytically, we're going to discretize the
[00:42:00:310 - 00:42:02:590] **Speaker 1:** rod into a series of nodes.
[00:42:03:270 - 00:42:08:479] **Speaker 1:** And then Approximate this PDE using finite differencing.
[00:42:09:479 - 00:42:13:659] **Speaker 1:** So Ranging from 1 up to N + 1 nodes,
[00:42:14:139 - 00:42:15:629] **Speaker 1:** we can describe our rod.
[00:42:17:189 - 00:42:21:229] **Speaker 1:** And we're going to create our finite difference patterns or
[00:42:21:229 - 00:42:23:250] **Speaker 1:** schemes using the tater series.
[00:42:26:739 - 00:42:30:679] **Speaker 1:** So Yeah, I guess I only use tailor series for
[00:42:30:679 - 00:42:33:679] **Speaker 1:** this course and you probably all forgot from your math
[00:42:33:679 - 00:42:34:120] **Speaker 1:** courses.
[00:42:34:520 - 00:42:37:620] **Speaker 1:** So you, so the the pattern for tailor series.
[00:42:39:090 - 00:42:44:360] **Speaker 1:** Is An infinite sum, so infinite series, N equals 0
[00:42:44:360 - 00:42:45:239] **Speaker 1:** up to infinity.
[00:42:47:199 - 00:42:50:520] **Speaker 1:** Of if, so some function.
[00:42:52:280 - 00:42:55:020] **Speaker 1:** Different, uh, so the nth derivative.
[00:42:55:790 - 00:42:59:169] **Speaker 1:** Evaluated at some point A divided by N.
[00:43:00:439 - 00:43:01:969] **Speaker 1:** Factorial, so.
[00:43:03:280 - 00:43:05:199] **Speaker 1:** And then X minus A.
[00:43:06:610 - 00:43:07:300] **Speaker 1:** To have in.
[00:43:09:060 - 00:43:13:620] **Speaker 1:** That's the tailor series um expression, and we use that
[00:43:13:629 - 00:43:22:350] **Speaker 1:** to approximate, A function So we're going to use potato
[00:43:22:350 - 00:43:23:080] **Speaker 1:** series around.
[00:43:25:689 - 00:43:29:850] **Speaker 1:** Uh, I plus 1, so we're going to approximate.
[00:43:30:649 - 00:43:35:620] **Speaker 1:** Our displacement at The right-hand side at I +1, using
[00:43:35:620 - 00:43:38:820] **Speaker 1:** the Taylor series terms about the I node.
[00:43:40:010 - 00:43:49:459] **Speaker 1:** So U1 + 1 is equal to You, I Plus.
[00:43:51:260 - 00:43:53:780] **Speaker 1:** DU by DX.
[00:43:54:639 - 00:43:57:550] **Speaker 1:** At I X.
[00:43:58:979 - 00:44:01:179] **Speaker 1:** So you, I will be that first term when we've
[00:44:01:179 - 00:44:04:149] **Speaker 1:** got um zero factorial.
[00:44:05:739 - 00:44:06:860] **Speaker 1:** No derivative.
[00:44:11:270 - 00:44:16:050] **Speaker 1:** And Our 3rd term will be, and then the 2nd
[00:44:16:050 - 00:44:18:479] **Speaker 1:** term is the 1st order derivative D by DX.
[00:44:19:080 - 00:44:22:159] **Speaker 1:** And that distance X minus A is the distance between
[00:44:22:159 - 00:44:24:879] **Speaker 1:** I and I + 1, which is delta X.
[00:44:25:280 - 00:44:26:320] **Speaker 1:** That's where this comes from.
[00:44:27:350 - 00:44:35:239] **Speaker 1:** We've got D 2 U by, D X 2.
[00:44:37:629 - 00:44:40:659] **Speaker 1:** Evaluated at the I point again and then got delta
[00:44:40:659 - 00:44:42:659] **Speaker 1:** X2 over 2.
[00:44:45:469 - 00:44:49:070] **Speaker 1:** That's for In equals to, I've got 2 times 1.
[00:44:50:840 - 00:44:53:959] **Speaker 1:** And it goes on forever, but we'll just do one
[00:44:53:959 - 00:44:54:360] **Speaker 1:** more term.
[00:44:54:560 - 00:44:55:219] **Speaker 1:** So D.
[00:44:56:300 - 00:45:02:399] **Speaker 1:** Cubed You by DX cubed, evaluated I.
[00:45:03:620 - 00:45:06:169] **Speaker 1:** Now we've got delta X to the power of 3.
[00:45:09:879 - 00:45:13:719] **Speaker 1:** Divided by 3 factorial, so 3 times 2 times 1.
[00:45:14:939 - 00:45:15:379] **Speaker 1:** 6.
[00:45:16:379 - 00:45:17:699] **Speaker 1:** And as I say, this goes on forever.
[00:45:17:939 - 00:45:20:429] **Speaker 1:** So we're gonna group all of those other terms together
[00:45:20:620 - 00:45:22:199] **Speaker 1:** and they're going to be of order.
[00:45:23:620 - 00:45:25:360] **Speaker 1:** Delta X 4.
[00:45:45:679 - 00:45:45:899] **Speaker 1:** Cool.
[00:45:46:260 - 00:45:48:189] **Speaker 1:** Is it sort of familiar maybe for like.
[00:45:50:389 - 00:45:50:800] **Speaker 1:** OK.
[00:45:52:320 - 00:45:52:659] **Speaker 1:** Cool.
[00:45:52:840 - 00:45:56:550] **Speaker 1:** So, yeah, I guess some concept concepts here is that
[00:45:57:469 - 00:46:01:030] **Speaker 1:** Well these higher order terms have a smaller contribution, sort
[00:46:01:030 - 00:46:03:110] **Speaker 1:** of like what we saw with those Foyer sign series,
[00:46:03:550 - 00:46:06:270] **Speaker 1:** um, we included more and more and got closer to
[00:46:06:270 - 00:46:10:270] **Speaker 1:** the real constant value in that Python scope, um, so
[00:46:10:270 - 00:46:11:629] **Speaker 1:** they have diminishing return.
[00:46:12:310 - 00:46:13:500] **Speaker 1:** But the higher audit.
[00:46:14:229 - 00:46:17:030] **Speaker 1:** It's, it's, yeah, more accurate as we include more terms.
[00:46:18:189 - 00:46:19:989] **Speaker 1:** But we can't include them all because it would take
[00:46:19:989 - 00:46:20:889] **Speaker 1:** too long to solve.
[00:46:23:330 - 00:46:24:989] **Speaker 1:** So how many do we use?
[00:46:25:889 - 00:46:26:679] **Speaker 1:** In this case.
[00:46:27:300 - 00:46:28:540] **Speaker 1:** So first of all, we'll do the same for the
[00:46:28:540 - 00:46:29:270] **Speaker 1:** left-hand node.
[00:46:29:620 - 00:46:31:379] **Speaker 1:** We've done the tailor series for the i+1.
[00:46:31:500 - 00:46:33:000] **Speaker 1:** We do the same for I minus 1.
[00:46:34:169 - 00:46:36:449] **Speaker 1:** So you I'm -1.
[00:46:37:600 - 00:46:38:570] **Speaker 1:** So it's very similar.
[00:46:38:909 - 00:46:40:830] **Speaker 1:** The only difference is that now instead of positive data
[00:46:40:830 - 00:46:42:389] **Speaker 1:** x, we've got minus X.
[00:46:42:949 - 00:46:46:750] **Speaker 1:** So the second term is gonna be minus DU by
[00:46:46:750 - 00:46:47:360] **Speaker 1:** DX.
[00:46:49:389 - 00:46:52:389] **Speaker 1:** Dot X The third term is gonna be positive because
[00:46:52:389 - 00:46:56:360] **Speaker 1:** we've got minus X2, so minus times minus it's gonna
[00:46:56:360 - 00:46:57:159] **Speaker 1:** be positive.
[00:46:58:169 - 00:46:59:929] **Speaker 1:** D2U by DX2.
[00:47:01:820 - 00:47:03:179] **Speaker 1:** Data X2 over 2.
[00:47:04:169 - 00:47:06:929] **Speaker 1:** Minus D cubed uy D X cubed.
[00:47:08:239 - 00:47:10:139] **Speaker 1:** Data x to the power of 3.
[00:47:11:239 - 00:47:12:489] **Speaker 1:** Divided by 6.
[00:47:14:520 - 00:47:17:100] **Speaker 1:** And all those other terms of order data for.
[00:47:21:399 - 00:47:23:479] **Speaker 1:** So that big O notation.
[00:47:25:120 - 00:47:26:639] **Speaker 1:** Is that order of the remainder.
[00:47:27:770 - 00:47:30:290] **Speaker 1:** What we can do is add those two equations together,
[00:47:30:370 - 00:47:41:919] **Speaker 1:** equations 4 and 5, and we're left with So the
[00:47:41:919 - 00:47:42:780] **Speaker 1:** UI.
[00:47:44:149 - 00:47:46:429] **Speaker 1:** And you, I will come back, I don't know Pins.
[00:47:47:060 - 00:47:49:209] **Speaker 1:** I don't know if it's really that worthwhile going through
[00:47:49:209 - 00:47:50:159] **Speaker 1:** this, but we can.
[00:47:53:899 - 00:47:55:580] **Speaker 1:** So we've got UI and UI.
[00:47:56:179 - 00:47:58:899] **Speaker 1:** The DU by DX, that first order derivative is going
[00:47:58:899 - 00:48:02:100] **Speaker 1:** to cancel between the two, and then the D2U by
[00:48:02:100 - 00:48:03:840] **Speaker 1:** D2U is going to combine.
[00:48:04:709 - 00:48:07:449] **Speaker 1:** Um, the 3rd order term is going to cancel.
[00:48:08:510 - 00:48:10:790] **Speaker 1:** And we're going to be left with some remainder of
[00:48:10:790 - 00:48:11:810] **Speaker 1:** data XR 4.
[00:48:15:040 - 00:48:20:379] **Speaker 1:** Now We're going to then rearrange for D2U by DX2.
[00:48:21:610 - 00:48:25:389] **Speaker 1:** And what we're left with Is.
[00:48:26:620 - 00:48:32:489] **Speaker 1:** D2U by DX2 evaluated at a point I.
[00:48:33:510 - 00:48:36:030] **Speaker 1:** So we're approximating the 2nd order of derivative at that
[00:48:36:030 - 00:48:37:270] **Speaker 1:** nodal position I.
[00:48:38:139 - 00:48:41:020] **Speaker 1:** Equal to UI + 1.
[00:48:42:149 - 00:48:43:500] **Speaker 1:** -2 UI.
[00:48:44:639 - 00:48:46:090] **Speaker 1:** Plus UI minus 1.
[00:48:47:580 - 00:48:49:429] **Speaker 1:** Over delta X 2.
[00:48:53:860 - 00:48:58:020] **Speaker 1:** Plus some remainder, so the remainder is divided by delta
[00:48:58:020 - 00:49:01:280] **Speaker 1:** X2 because we've rearranged for D2U by DX2.
[00:49:02:350 - 00:49:08:739] **Speaker 1:** So Order delta X4 reduces down to order delta X2.
[00:49:16:600 - 00:49:23:489] **Speaker 1:** So now, We're approximating this 2nd, uh, 2nd order derivative
[00:49:23:489 - 00:49:27:090] **Speaker 1:** in space, and we've got some residual or remainder that
[00:49:27:090 - 00:49:28:310] **Speaker 1:** scales without X2.
[00:49:28:870 - 00:49:30:379] **Speaker 1:** So we can say that this is a 2nd order
[00:49:31:229 - 00:49:32:189] **Speaker 1:** accurate scheme.
[00:49:35:729 - 00:49:38:729] **Speaker 1:** And this is we've derived the central difference scheme for
[00:49:38:729 - 00:49:39:389] **Speaker 1:** finite differenceferencing.
[00:49:41:919 - 00:49:43:409] **Speaker 1:** So this is probably the one that some of you
[00:49:43:409 - 00:49:45:570] **Speaker 1:** might have already encountered before, but it doesn't matter if
[00:49:45:570 - 00:49:47:909] **Speaker 1:** you haven't, uh, we've arrived it just now.
[00:49:49:030 - 00:49:50:270] **Speaker 1:** Proof that it exists.
[00:49:53:030 - 00:49:59:129] **Speaker 1:** And finally, If we assume a constant cross-sectional area and
[00:49:59:129 - 00:50:00:290] **Speaker 1:** Young's modulus E.
[00:50:02:810 - 00:50:07:610] **Speaker 1:** We can push these uh constants out of the derivative
[00:50:07:610 - 00:50:08:929] **Speaker 1:** and we're left with A E.
[00:50:11:520 - 00:50:15:239] **Speaker 1:** D2 U by DX2 equal to 0.
[00:50:16:219 - 00:50:19:669] **Speaker 1:** And now zoomed up to it So when we discretize
[00:50:19:669 - 00:50:24:949] **Speaker 1:** at a point I We're going to take our finite
[00:50:24:949 - 00:50:27:570] **Speaker 1:** difference pattern equation 6.
[00:50:28:320 - 00:50:32:040] **Speaker 1:** And apply it to our 2nd order derivative in X.
[00:50:32:689 - 00:50:34:370] **Speaker 1:** So we've got AE.
[00:50:35:340 - 00:50:37:449] **Speaker 1:** That's the first term, and then the derivative.
[00:50:38:479 - 00:50:43:000] **Speaker 1:** UI + 1 minus 2 UI + UI minus 1.
[00:50:43:850 - 00:50:46:250] **Speaker 1:** Divided by X2.
[00:50:49:219 - 00:50:54:600] **Speaker 1:** Cool Brilliant.
[00:50:57:530 - 00:51:00:429] **Speaker 1:** So Cool.
[00:51:00:870 - 00:51:01:260] **Speaker 1:** All right.
[00:51:01:590 - 00:51:03:389] **Speaker 1:** So then the next step is to do boundary conditions.
[00:51:03:469 - 00:51:04:620] **Speaker 1:** So we'll look at that next term.
[00:51:05:669 - 00:51:07:750] **Speaker 1:** And yeah, alright.
[00:51:08:149 - 00:51:10:530] **Speaker 1:** Any questions or no questions, good.
[00:51:11:030 - 00:51:12:030] **Speaker 1:** Alright, we'll see you next time.
[00:51:13:340 - 00:51:15:250] **Speaker 1:** So yeah, remember to do the quiz tonight and you've
[00:51:15:250 - 00:51:18:060] **Speaker 1:** got your assignment for assignment one to, to do as
[00:51:18:060 - 00:51:18:320] **Speaker 0:** well.
[00:51:26:879 - 00:51:27:270] **Speaker 0:** Uh yeah.
[00:51:54:199 - 00:51:59:780] **Speaker 0:** John Good holidays, have a good holiday.
[00:52:03:889 - 00:52:04:229] **Speaker 0:** I don't.
[00:52:09:000 - 00:52:09:469] **Speaker 0:** the question.
[00:52:16:620 - 00:52:16:629] **Speaker 0:** Yeah.
[00:52:20:459 - 00:52:22:689] **Speaker 0:** I just emailed my her so that I could be
[00:52:22:689 - 00:52:23:570] **Speaker 0:** the first person to visit.
[00:52:26:149 - 00:52:28:760] **Speaker 0:** I went through.
[00:52:37:600 - 00:52:37:610] **Speaker 0:** I.
[00:52:39:000 - 00:52:43:699] **Speaker 0:** I right You.
[00:52:45:889 - 00:52:49:810] **Speaker 0:** Yeah, some of our group didn't stay and some left
[00:52:49:810 - 00:52:52:110] **Speaker 0:** and also didn't have time.
[00:53:04:250 - 00:53:41:600] **Speaker 0:** So Minister's focus And Um Uh play road and With
[00:53:43:479 - 00:53:43:500] **Speaker 0:** so like.
[00:53:50:570 - 00:53:55:879] **Speaker 0:** Yes score.
[00:53:57:879 - 00:53:57:889] **Speaker 0:** Yeah.
[00:54:01:739 - 00:54:03:030] **Speaker 0:** I OK.
[00:54:04:010 - 00:54:06:169] **Speaker 0:** So and it's funny.
[00:54:08:739 - 00:54:17:070] **Speaker 0:** like I And In a snowy place, but your preferred
[00:54:17:070 - 00:54:17:629] **Speaker 0:** landscapes.
[00:54:18:919 - 00:54:20:379] **Speaker 0:** Yeah, I feel.
[00:54:21:429 - 00:54:22:879] **Speaker 0:** Poling isn't as yet, but that's true.
[00:54:26:659 - 00:54:32:530] **Speaker 0:** A Yeah, I was the lowest Yeah, especially the first
[00:54:32:530 - 00:54:32:780] **Speaker 0:** few months just right now.
[00:54:46:030 - 00:54:46:389] **Speaker 0:** It was.
[00:54:52:000 - 00:54:59:969] **Speaker 0:** to Yeah I can't do the, yeah, so.

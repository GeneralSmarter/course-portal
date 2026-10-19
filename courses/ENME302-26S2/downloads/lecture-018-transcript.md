# ENME302-26S2 Lecture 18 native Echo transcript

Date: August 12, 2026 11:00am-11:55am
Transcript type: native Echo automated transcript.

[00:00:51:470 - 00:00:52:630] **Speaker 0:** Well, uh, we'll make it stop.
[00:00:52:740 - 00:00:53:849] **Speaker 0:** Is the mic working good?
[00:00:54:029 - 00:00:56:099] **Speaker 0:** I think, I think, maybe.
[00:00:56:310 - 00:00:57:290] **Speaker 0:** Alright, cool.
[00:00:57:869 - 00:00:58:889] **Speaker 0:** Alright, welcome back.
[00:00:59:189 - 00:01:03:229] **Speaker 0:** Uh, so, Monday, uh, we looked at a few things.
[00:01:03:340 - 00:01:04:370] **Speaker 0:** I'll skipped through.
[00:01:08:339 - 00:01:09:510] **Speaker 0:** This is the slide version.
[00:01:09:620 - 00:01:11:470] **Speaker 0:** I've given you just the handout, which is a bit
[00:01:11:470 - 00:01:11:970] **Speaker 0:** easier.
[00:01:12:389 - 00:01:13:889] **Speaker 0:** Uh, we talked a bit about the lecture.
[00:01:15:480 - 00:01:17:730] **Speaker 0:** Designing different systems.
[00:01:17:970 - 00:01:20:970] **Speaker 0:** So when can we actually use numerical simulations versus experiments
[00:01:20:970 - 00:01:25:040] **Speaker 0:** and um just Uh, like guidelines or standards.
[00:01:26:470 - 00:01:31:019] **Speaker 0:** Talked about advantages and disadvantages, some history, and we talked
[00:01:31:019 - 00:01:34:440] **Speaker 0:** about verification versus validation, so it's an important concept.
[00:01:35:309 - 00:01:37:709] **Speaker 0:** Uh, and now we're just gonna go through some cases
[00:01:37:709 - 00:01:40:029] **Speaker 0:** of whether or not things can go wrong and what
[00:01:40:029 - 00:01:42:769] **Speaker 0:** we could do to address those, and to mitigate those
[00:01:43:150 - 00:01:43:959] **Speaker 0:** potential risks.
[00:01:44:389 - 00:01:47:690] **Speaker 0:** So one example is, uh, that the model is too
[00:01:47:690 - 00:01:48:569] **Speaker 0:** simplified.
[00:01:50:309 - 00:01:51:879] **Speaker 0:** Uh, yet it's still too demanding.
[00:01:52:279 - 00:01:57:209] **Speaker 0:** So if we have a model that Is I, I
[00:01:57:209 - 00:02:01:120] **Speaker 0:** don't know if we're trying to model aer aerofo and
[00:02:01:559 - 00:02:05:120] **Speaker 0:** we've got, Every single piece of that aerofoil, so the
[00:02:05:120 - 00:02:08:339] **Speaker 0:** wing tip, um, through to the fuselage, uh, all the
[00:02:08:339 - 00:02:10:000] **Speaker 0:** turbine pieces.
[00:02:10:580 - 00:02:12:380] **Speaker 0:** Maybe what we want to do is just model a
[00:02:12:380 - 00:02:13:000] **Speaker 0:** cross section.
[00:02:13:029 - 00:02:15:259] **Speaker 0:** So we want to further reduce that complexity.
[00:02:15:979 - 00:02:18:839] **Speaker 0:** So reducing from 3 dimensions down to 2 dimensions.
[00:02:20:070 - 00:02:23:500] **Speaker 0:** Uh, Another risk is computer resources, whether it's memory or
[00:02:23:500 - 00:02:26:610] **Speaker 0:** time, is not adequate to solve for our simplified problem.
[00:02:27:570 - 00:02:28:750] **Speaker 0:** In a reasonable time.
[00:02:29:410 - 00:02:32:850] **Speaker 0:** So we could look at some more efficient implementations, so
[00:02:32:850 - 00:02:34:470] **Speaker 0:** either more efficient solvers.
[00:02:35:449 - 00:02:37:990] **Speaker 0:** So those are those algorithms that we talked on earlier,
[00:02:38:529 - 00:02:40:000] **Speaker 0:** or better use of parallellyzation.
[00:02:40:089 - 00:02:41:889] **Speaker 0:** So a lot of the computers these days have multiple
[00:02:41:889 - 00:02:44:479] **Speaker 0:** cores and I think most CPUs will have multiple cores,
[00:02:44:729 - 00:02:47:630] **Speaker 0:** uh, and you can distribute the workload across those cores.
[00:02:48:000 - 00:02:51:729] **Speaker 0:** Uh, it isn't always trivial, uh, and it doesn't always
[00:02:51:729 - 00:02:54:610] **Speaker 0:** give you 3 or 4 times as much speed for
[00:02:54:610 - 00:02:56:570] **Speaker 0:** those 3 or 4 extra cores because you still have
[00:02:56:570 - 00:02:58:570] **Speaker 0:** to piece together the problem at the end of it.
[00:02:58:729 - 00:03:01:130] **Speaker 0:** So partitioning is, is part of that process.
[00:03:03:350 - 00:03:06:949] **Speaker 0:** Uh, whether or not the numerical solution can replicate the
[00:03:06:949 - 00:03:08:089] **Speaker 0:** benchmark results.
[00:03:08:960 - 00:03:11:619] **Speaker 0:** So we talked about that with the verification case, uh,
[00:03:11:630 - 00:03:12:550] **Speaker 0:** in the last flow chart.
[00:03:12:789 - 00:03:15:589] **Speaker 0:** So if you had a numerical scheme or some solver,
[00:03:15:669 - 00:03:18:630] **Speaker 0:** some software, and it wasn't matching what the benchmark results
[00:03:18:630 - 00:03:22:070] **Speaker 0:** were expecting, uh, we might need to go back and
[00:03:22:070 - 00:03:23:789] **Speaker 0:** check our, uh, solution setup.
[00:03:24:059 - 00:03:25:350] **Speaker 0:** So you might want to increase the resolution.
[00:03:25:429 - 00:03:26:320] **Speaker 0:** So that's the mesh.
[00:03:26:589 - 00:03:30:789] **Speaker 0:** So we discretize the, the physical space, uh, into a
[00:03:30:789 - 00:03:33:649] **Speaker 0:** set of small cells, and we also look at time,
[00:03:34:039 - 00:03:35:289] **Speaker 0:** uh, discretization as well.
[00:03:36:360 - 00:03:39:759] **Speaker 0:** So tweaking the existing model or try another method entirely.
[00:03:40:850 - 00:03:43:800] **Speaker 0:** So, the last one here is maybe our predicted solution
[00:03:43:800 - 00:03:46:490] **Speaker 0:** doesn't match the supported, uh, measured data.
[00:03:46:570 - 00:03:49:130] **Speaker 0:** So that was the validation step, the last step in
[00:03:49:130 - 00:03:49:970] **Speaker 0:** that last flow chart.
[00:03:50:330 - 00:03:51:419] **Speaker 0:** So we might need to go back to the drawing
[00:03:51:419 - 00:03:51:610] **Speaker 0:** board.
[00:03:51:690 - 00:03:53:710] **Speaker 0:** Maybe we've made some simplifying assumptions.
[00:03:54:169 - 00:03:56:529] **Speaker 0:** So if we did heat transfer in the lecture theatre,
[00:03:56:809 - 00:04:00:410] **Speaker 0:** um, looking at air conditioning, and we assumed isothermal flow,
[00:04:00:570 - 00:04:03:389] **Speaker 0:** so no heat change, uh, obviously that's going to be
[00:04:03:889 - 00:04:06:229] **Speaker 0:** not helpful for, for modelling the heat transfer.
[00:04:06:679 - 00:04:09:690] **Speaker 0:** Uh, so, yeah, that's a pretty stupid example, but it's
[00:04:09:690 - 00:04:11:389] **Speaker 0:** just a, An example there.
[00:04:13:350 - 00:04:14:889] **Speaker 0:** So numerical methods.
[00:04:15:710 - 00:04:17:428] **Speaker 0:** So some of you have already come through, I think,
[00:04:17:510 - 00:04:17:950] **Speaker 0:** finite difference.
[00:04:18:028 - 00:04:19:678] **Speaker 0:** We did finite elements for the 1st 4 weeks.
[00:04:19:989 - 00:04:22:230] **Speaker 0:** So you, you know some of these terms, uh, but
[00:04:22:230 - 00:04:24:869] **Speaker 0:** I just want to introduce 3 different sets.
[00:04:24:980 - 00:04:28:070] **Speaker 0:** So we've got finite element, volume, and difference methods.
[00:04:29:679 - 00:04:32:049] **Speaker 0:** So finite element method which we've used so far with
[00:04:32:049 - 00:04:33:239] **Speaker 0:** those bars and bees.
[00:04:33:839 - 00:04:36:839] **Speaker 0:** So this is typically used for structural mechanics and for
[00:04:36:839 - 00:04:39:480] **Speaker 0:** steady field problems, but it can also be applied to
[00:04:39:480 - 00:04:43:380] **Speaker 0:** steady, um, or transient, so time-dependent cases.
[00:04:43:760 - 00:04:47:079] **Speaker 0:** And this is of course described by partial differential equations,
[00:04:47:239 - 00:04:48:119] **Speaker 0:** so PDEs.
[00:04:49:250 - 00:04:52:649] **Speaker 0:** So the history from these is from the 1950s, uh,
[00:04:52:739 - 00:04:57:209] **Speaker 0:** with some early commercial codes, cosmic, Nastran, 1968.
[00:04:57:369 - 00:04:58:489] **Speaker 0:** I'm not familiar with that one.
[00:04:59:440 - 00:05:03:320] **Speaker 0:** Uh, so over time, I guess we see that with
[00:05:03:320 - 00:05:06:279] **Speaker 0:** other companies as well, but a lot of the big
[00:05:06:279 - 00:05:07:679] **Speaker 0:** software companies sort of merge together.
[00:05:07:799 - 00:05:08:959] **Speaker 0:** They buy out each other.
[00:05:09:239 - 00:05:12:359] **Speaker 0:** Uh, ASIS being one of those that purchased a lot
[00:05:12:359 - 00:05:16:079] **Speaker 0:** of individual products and they combine them into their workbench.
[00:05:16:320 - 00:05:18:359] **Speaker 0:** So you can see that in the next week there's
[00:05:18:359 - 00:05:19:679] **Speaker 0:** ASIS Workbench installed.
[00:05:20:619 - 00:05:23:769] **Speaker 0:** Which is essentially just a table, uh, that you can
[00:05:23:769 - 00:05:24:820] **Speaker 0:** add in different features.
[00:05:24:920 - 00:05:27:859] **Speaker 0:** So you might have solid mechanics, ah, fluid flow, so
[00:05:27:859 - 00:05:30:100] **Speaker 0:** there's fluent in there and a whole bunch of others
[00:05:30:100 - 00:05:31:640] **Speaker 0:** that I haven't, haven't really used myself.
[00:05:32:989 - 00:05:36:220] **Speaker 0:** So Yeah, at the moment, we've got all these big,
[00:05:36:359 - 00:05:37:320] **Speaker 0:** uh, software packages.
[00:05:37:519 - 00:05:39:670] **Speaker 0:** So Abacus is another one that's often used for finite
[00:05:39:670 - 00:05:42:600] **Speaker 0:** elements, uh, and console, which we'll be using in, in
[00:05:42:600 - 00:05:43:220] **Speaker 0:** this course.
[00:05:44:250 - 00:05:46:750] **Speaker 0:** So there's a high level of integration with CAD modelling.
[00:05:47:130 - 00:05:50:209] **Speaker 0:** So you've done CAD and SolidWorks in, in your first
[00:05:50:209 - 00:05:52:329] **Speaker 0:** few years and you're still doing that in your design
[00:05:52:329 - 00:05:53:369] **Speaker 0:** course, probably.
[00:05:53:760 - 00:05:57:690] **Speaker 0:** Uh, so you can either create your geometries in your
[00:05:57:690 - 00:06:00:489] **Speaker 0:** CAD software that you're more familiar with and import it
[00:06:00:489 - 00:06:02:570] **Speaker 0:** to the numerical solver, or you can create some basic
[00:06:02:570 - 00:06:04:410] **Speaker 0:** geometry within the numerical solver itself.
[00:06:04:649 - 00:06:06:579] **Speaker 0:** So we'll do that in, in this class.
[00:06:07:709 - 00:06:10:470] **Speaker 0:** Finite volume method, so finite volume.
[00:06:11:339 - 00:06:13:339] **Speaker 0:** There's another scheme of discretization.
[00:06:13:899 - 00:06:17:179] **Speaker 0:** So this is often used for CFD, computational fluid dynamics,
[00:06:17:579 - 00:06:19:570] **Speaker 0:** and it is often used for transport phenomena.
[00:06:19:619 - 00:06:22:940] **Speaker 0:** So if you're looking at momentum flux, um, species transport,
[00:06:23:179 - 00:06:24:619] **Speaker 0:** heat transfer, etc.
[00:06:25:739 - 00:06:28:890] **Speaker 0:** Uh, the classic example is fluent as being a commercial
[00:06:28:890 - 00:06:31:230] **Speaker 0:** software that uses a finite volume method.
[00:06:31:579 - 00:06:34:299] **Speaker 0:** Open foam is an open-source, uh, software package that uses
[00:06:34:299 - 00:06:35:119] **Speaker 0:** finite volume.
[00:06:35:820 - 00:06:40:000] **Speaker 0:** Um, the equivalent open source finite elements would be, uh,
[00:06:40:019 - 00:06:40:739] **Speaker 0:** Phoenix.
[00:06:44:179 - 00:06:47:160] **Speaker 0:** So this is the basis for most commercial CFD software,
[00:06:47:859 - 00:06:54:309] **Speaker 0:** um, And Yeah, typically, CFD codes will use the finite
[00:06:54:309 - 00:06:55:109] **Speaker 0:** volume method.
[00:06:55:309 - 00:06:57:070] **Speaker 0:** We'll go through these in detail a little bit shortly,
[00:06:57:429 - 00:06:58:269] **Speaker 0:** uh, but.
[00:06:59:260 - 00:07:01:760] **Speaker 0:** Yeah, you can use finite element for CFD as well.
[00:07:03:220 - 00:07:05:109] **Speaker 0:** The last one we'll talk about here is the finite
[00:07:05:109 - 00:07:07:790] **Speaker 0:** difference method and you would have probably come into this,
[00:07:07:859 - 00:07:10:670] **Speaker 0:** into your math courses already, uh, but this is on
[00:07:10:670 - 00:07:11:769] **Speaker 0:** a structured grid.
[00:07:12:309 - 00:07:16:510] **Speaker 0:** So it's really suited for more research application, uh, and
[00:07:16:510 - 00:07:19:589] **Speaker 0:** simplified geometry, so not heavily used in industry.
[00:07:22:149 - 00:07:24:540] **Speaker 0:** And requires that structured mesh, as I say.
[00:07:26:140 - 00:07:29:070] **Speaker 0:** So finite element and finite volume, those first two cases
[00:07:29:070 - 00:07:32:170] **Speaker 0:** are suited for unstructured meshes, so ones that don't have
[00:07:32:170 - 00:07:34:799] **Speaker 0:** just nice rows and columns associated with the mesh.
[00:07:35:649 - 00:07:38:269] **Speaker 0:** Uh, whereas the finite difference requires that structured mesh.
[00:07:39:890 - 00:07:43:429] **Speaker 0:** So in this course we're looking at finite element method
[00:07:43:790 - 00:07:44:970] **Speaker 0:** and finite difference.
[00:07:45:709 - 00:07:48:359] **Speaker 0:** The finite volume method we leave for the CFD course
[00:07:48:359 - 00:07:49:760] **Speaker 0:** next year if you're interested in that.
[00:07:49:839 - 00:07:53:269] **Speaker 0:** That's ENGR 401, uh, taught by Matthew Cider.
[00:07:54:040 - 00:07:56:679] **Speaker 0:** So that's useful if you want to look at that
[00:07:56:679 - 00:07:58:059] **Speaker 0:** fluid flows in particular.
[00:07:58:299 - 00:08:01:140] **Speaker 0:** We don't really do that in this course.
[00:08:01:980 - 00:08:04:570] **Speaker 0:** Um, but the tools that you learn in this course,
[00:08:04:579 - 00:08:06:089] **Speaker 0:** you can apply to CFD as well.
[00:08:07:649 - 00:08:10:410] **Speaker 0:** The, there was a question on Monday, uh, from one
[00:08:10:410 - 00:08:13:010] **Speaker 0:** of your classmates about how much solid structural mechanics we
[00:08:13:010 - 00:08:14:070] **Speaker 0:** do with console.
[00:08:14:480 - 00:08:16:570] **Speaker 0:** Uh, so we don't do too much.
[00:08:16:609 - 00:08:20:170] **Speaker 0:** We do a couple of console labs that use the
[00:08:20:170 - 00:08:24:350] **Speaker 0:** solid mechanics, uh, just because they're introductory classes or labs.
[00:08:25:799 - 00:08:30:290] **Speaker 0:** If you want to continue learning about FEA and design,
[00:08:30:600 - 00:08:33:809] **Speaker 0:** uh, there's enemy 406, so that's with degree 7s next
[00:08:33:809 - 00:08:35:250] **Speaker 0:** year if you're interested in that.
[00:08:36:190 - 00:08:39:659] **Speaker 0:** Um, yeah, so I guess just reiterating that what we're
[00:08:39:659 - 00:08:42:229] **Speaker 0:** learning in this course is sort of the basics and
[00:08:42:229 - 00:08:45:630] **Speaker 0:** the fundamentals, uh, which some people might like more than
[00:08:45:630 - 00:08:48:549] **Speaker 0:** others, uh, but it should be very useful to give
[00:08:48:549 - 00:08:51:210] **Speaker 0:** you a solid foundation for your, for your courses next
[00:08:51:210 - 00:08:55:710] **Speaker 0:** year, especially the more design, uh, and funnier projects, research-based
[00:08:55:710 - 00:08:56:369] **Speaker 0:** courses.
[00:08:56:909 - 00:08:58:630] **Speaker 0:** You'll be able to apply what you've learned in this
[00:08:58:630 - 00:08:59:049] **Speaker 0:** course.
[00:09:01:619 - 00:09:04:159] **Speaker 0:** So some of those meshes, just putting uh pictures to
[00:09:04:159 - 00:09:05:369] **Speaker 0:** what I tried to describe.
[00:09:05:729 - 00:09:08:909] **Speaker 0:** So on the left, we have a structured mesh.
[00:09:09:789 - 00:09:10:750] **Speaker 0:** We've got an O grid.
[00:09:10:830 - 00:09:13:280] **Speaker 0:** I don't know if you We can try and zoom
[00:09:13:280 - 00:09:13:940] **Speaker 0:** in, but.
[00:09:17:479 - 00:09:19:570] **Speaker 0:** That's a pretty poor quality image.
[00:09:19:840 - 00:09:22:559] **Speaker 0:** Um, but that's an O grid mesh, meaning that it
[00:09:22:559 - 00:09:23:320] **Speaker 0:** looks like an O.
[00:09:24:159 - 00:09:28:580] **Speaker 0:** so you've got all these radial and circumferential, uh, edges
[00:09:28:869 - 00:09:31:359] **Speaker 0:** that form the mesh, and you could imagine that gets
[00:09:31:359 - 00:09:34:979] **Speaker 0:** mapped out to a regular rows, columns, structured grid.
[00:09:35:530 - 00:09:37:320] **Speaker 0:** So the nice thing about these structured grids is that
[00:09:37:320 - 00:09:39:780] **Speaker 0:** you always know the neighbouring cells.
[00:09:40:159 - 00:09:41:719] **Speaker 0:** You've got north, south, east, west.
[00:09:42:530 - 00:09:45:619] **Speaker 0:** Ah, and that's, that's one of the advantages here.
[00:09:48:109 - 00:09:50:799] **Speaker 0:** In this case, we've got some overlapping meshes.
[00:09:51:359 - 00:09:55:880] **Speaker 0:** So we've turned this chimaera, overlapping grid.
[00:09:56:669 - 00:09:59:669] **Speaker 0:** So perhaps we have a moving domain, so it's an
[00:09:59:669 - 00:10:02:630] **Speaker 0:** aerofoil or some sort of object that's shifting throughout the
[00:10:02:630 - 00:10:03:039] **Speaker 0:** flow.
[00:10:03:270 - 00:10:07:669] **Speaker 0:** We might want to resolve that, um, accurately around the
[00:10:07:669 - 00:10:07:989] **Speaker 0:** object.
[00:10:08:739 - 00:10:11:979] **Speaker 0:** And then that's going to flow through the, the outer
[00:10:11:979 - 00:10:12:380] **Speaker 0:** domain.
[00:10:14:090 - 00:10:18:150] **Speaker 0:** And the blue region inside is another object that's meshed
[00:10:18:330 - 00:10:19:090] **Speaker 0:** with a structured grid.
[00:10:20:929 - 00:10:23:750] **Speaker 0:** The examples on the right, but that we've skipped now.
[00:10:25:960 - 00:10:29:080] **Speaker 0:** Yeah, 2D axiommetric unstructured intake mesh.
[00:10:29:599 - 00:10:32:719] **Speaker 0:** So unstructured in the sense that it has just a
[00:10:32:719 - 00:10:34:140] **Speaker 0:** scatter of nodes.
[00:10:35:020 - 00:10:36:739] **Speaker 0:** Uh, in fact, we'll talk a little bit about meshing
[00:10:36:739 - 00:10:38:909] **Speaker 0:** later on, but essentially there's a scatter of nodes that
[00:10:38:909 - 00:10:41:349] **Speaker 0:** sort of uniformly distributed and then it joins up the
[00:10:41:349 - 00:10:41:940] **Speaker 0:** elements.
[00:10:42:429 - 00:10:44:929] **Speaker 0:** So it looks quite chaotic.
[00:10:45:349 - 00:10:48:510] **Speaker 0:** If you select a random point, you don't necessarily know
[00:10:48:510 - 00:10:50:739] **Speaker 0:** the neighbouring nodes, so you don't know which one's left,
[00:10:50:830 - 00:10:53:929] **Speaker 0:** right, top, bottom, uh, without storing that information.
[00:10:54:349 - 00:10:57:469] **Speaker 0:** So in terms of, uh, compute power and RAM memory,
[00:10:57:710 - 00:10:59:940] **Speaker 0:** you'd have to store that data, uh, separately.
[00:11:00:349 - 00:11:02:270] **Speaker 0:** So it is a little bit more expensive to, to
[00:11:02:270 - 00:11:02:669] **Speaker 0:** solve.
[00:11:08:500 - 00:11:11:830] **Speaker 0:** And in 3D, you can imagine that it extends to
[00:11:11:830 - 00:11:13:190] **Speaker 0:** the third dimension.
[00:11:15:679 - 00:11:16:070] **Speaker 0:** Who.
[00:11:22:190 - 00:11:25:630] **Speaker 0:** So, I've listed those three cases, finite element difference and
[00:11:25:630 - 00:11:27:070] **Speaker 0:** finite volume methods.
[00:11:27:349 - 00:11:29:969] **Speaker 0:** And now we're just gonna give a really top overview
[00:11:29:969 - 00:11:32:150] **Speaker 0:** of, of what those, uh, entail.
[00:11:34:340 - 00:11:35:479] **Speaker 0:** So the finite element model.
[00:11:36:599 - 00:11:38:210] **Speaker 0:** is in 2D.
[00:11:39:030 - 00:11:41:729] **Speaker 0:** For example, for a structured grid, we'd have a series
[00:11:41:729 - 00:11:45:590] **Speaker 0:** of lines, uh, for rows and columns, and then each
[00:11:45:590 - 00:11:46:030] **Speaker 0:** element.
[00:11:47:409 - 00:11:52:200] **Speaker 0:** Shaded here is defined by nodes on the edges or
[00:11:52:200 - 00:11:52:979] **Speaker 0:** on the points.
[00:11:53:260 - 00:11:55:729] **Speaker 0:** So I've got 4 nodes for a for a square
[00:11:55:729 - 00:12:05:580] **Speaker 0:** or rectangle and, E Each node, yeah, makes up that,
[00:12:05:679 - 00:12:11:669] **Speaker 0:** that element, um, And it will fit the surrounding domain.
[00:12:11:890 - 00:12:17:710] **Speaker 0:** So if we have A triangle or something that's not
[00:12:18:010 - 00:12:20:210] **Speaker 0:** square, then you'd have to use that unstructured grid.
[00:12:22:270 - 00:12:24:520] **Speaker 0:** Uh, the nodal values of the dependent variables, so maybe
[00:12:24:520 - 00:12:29:099] **Speaker 0:** it's temperature or velocity field, UVW, are the unknown quantities,
[00:12:29:640 - 00:12:32:039] **Speaker 0:** and these are being evaluated at those nodal points.
[00:12:33:080 - 00:12:34:880] **Speaker 0:** We use interpolation schemes.
[00:12:34:919 - 00:12:37:640] **Speaker 0:** So you've done some of these already, uh, between those
[00:12:37:640 - 00:12:37:919] **Speaker 0:** nodes.
[00:12:38:039 - 00:12:41:469] **Speaker 0:** So within each element, we, uh, use interpolation functions to
[00:12:41:469 - 00:12:45:200] **Speaker 0:** approximate or evaluate those temperature or velocity.
[00:12:46:250 - 00:12:46:750] **Speaker 0:** Terms.
[00:12:48:679 - 00:12:52:469] **Speaker 0:** And we're imposing the physics with a weak or integrated
[00:12:52:469 - 00:12:52:919] **Speaker 0:** sentence.
[00:12:53:349 - 00:12:59:369] **Speaker 0:** So typically we use, um, Yeah, principle of virtual work,
[00:12:59:830 - 00:13:00:669] **Speaker 0:** and.
[00:13:01:530 - 00:13:05:400] **Speaker 0:** Yeah, then solve that, that weak form of equations, and
[00:13:05:400 - 00:13:08:049] **Speaker 0:** we'll go through that, uh, I think it's chapter 8
[00:13:08:190 - 00:13:08:619] **Speaker 0:** or so.
[00:13:11:119 - 00:13:13:619] **Speaker 0:** Finite difference is a little bit easier to think about.
[00:13:13:799 - 00:13:16:940] **Speaker 0:** Uh, again, we've got a structured grid, we've got some
[00:13:17:559 - 00:13:20:000] **Speaker 0:** point of interest, we're going to label it at point
[00:13:20:000 - 00:13:20:559] **Speaker 0:** IJ.
[00:13:21:580 - 00:13:24:900] **Speaker 0:** So our arbitrary variable Q at point IJ, we've got
[00:13:24:900 - 00:13:27:340] **Speaker 0:** nodes to the right, so I + 1 and nodes
[00:13:27:340 - 00:13:29:299] **Speaker 0:** to the left, I minus 1, and then north and
[00:13:29:299 - 00:13:32:099] **Speaker 0:** south will be J + 1 and -1.
[00:13:33:929 - 00:13:36:239] **Speaker 0:** So our computational domain is covered by a grid of
[00:13:36:239 - 00:13:39:090] **Speaker 0:** points, uh, aligned in those two or three dimensions, so
[00:13:39:090 - 00:13:40:809] **Speaker 0:** you can imagine that there's also the depth.
[00:13:43:489 - 00:13:48:020] **Speaker 0:** And we're going to solve our partial differential equations by,
[00:13:49:059 - 00:13:50:690] **Speaker 0:** Apply a pot difference to each term.
[00:13:51:909 - 00:13:55:030] **Speaker 0:** So the values of these variables Q are evaluated at
[00:13:55:030 - 00:13:55:989] **Speaker 0:** the grid points again.
[00:13:56:859 - 00:13:59:630] **Speaker 0:** The derivatives, as I say, is evaluated at those grid
[00:13:59:630 - 00:13:59:940] **Speaker 0:** points.
[00:14:01:549 - 00:14:05:270] **Speaker 0:** And we use Taylor series approximations to approximate those derivatives,
[00:14:05:390 - 00:14:07:710] **Speaker 0:** so it's to some sort of order of accuracy.
[00:14:08:380 - 00:14:11:330] **Speaker 0:** And that scales with the spacing between each node, so
[00:14:11:429 - 00:14:12:340] **Speaker 0:** delta X and Y.
[00:14:13:580 - 00:14:16:380] **Speaker 0:** And the discrete solution is forced to satisfy our governing
[00:14:16:380 - 00:14:20:099] **Speaker 0:** PDEs and boundary conditions at the grid points, and we
[00:14:20:099 - 00:14:22:619] **Speaker 0:** end up with a system of linear equations to solve.
[00:14:23:580 - 00:14:27:039] **Speaker 0:** So for your, your bars and beams, you've only got
[00:14:27:039 - 00:14:29:140] **Speaker 0:** a handful or 2 or 3 maybe degrees of freedom
[00:14:29:140 - 00:14:32:539] **Speaker 0:** for each nodal point, and you'll set up an equation
[00:14:32:539 - 00:14:37:520] **Speaker 0:** that has 5, 1015 odd, um, Equations and you're solving
[00:14:37:520 - 00:14:39:559] **Speaker 0:** that, that, uh, system of equations.
[00:14:39:669 - 00:14:41:979] **Speaker 0:** So if you had a mesh like we saw earlier
[00:14:42:119 - 00:14:44:479] **Speaker 0:** that had maybe 10s of thousands or hundreds of thousands
[00:14:44:479 - 00:14:47:359] **Speaker 0:** of nodes, you'd have very large systems of equations to
[00:14:47:359 - 00:14:47:799] **Speaker 0:** solve.
[00:14:48:400 - 00:14:52:609] **Speaker 0:** Uh, so there's, yeah, you can't always use the inverse
[00:14:52:609 - 00:14:55:900] **Speaker 0:** function or similar methods with Python to, to solve that
[00:14:56:080 - 00:14:56:640] **Speaker 0:** efficiently.
[00:14:56:799 - 00:14:59:599] **Speaker 0:** So that's why people have developed all those different algorithms
[00:14:59:599 - 00:15:01:000] **Speaker 0:** that we, we talked to.
[00:15:03:270 - 00:15:06:559] **Speaker 0:** So for uncity problems, so something changing with time, uh,
[00:15:06:630 - 00:15:10:510] **Speaker 0:** the vertical axis or any other sort of depth axis
[00:15:10:510 - 00:15:12:210] **Speaker 0:** we can use, use for time.
[00:15:13:969 - 00:15:14:809] **Speaker 0:** Finite volume.
[00:15:15:049 - 00:15:16:489] **Speaker 0:** We've just chuck this in for your information.
[00:15:16:609 - 00:15:19:210] **Speaker 0:** We don't really use this in this class, but for
[00:15:19:210 - 00:15:24:059] **Speaker 0:** the CFD course next year, you'll essentially I follow a
[00:15:24:059 - 00:15:28:299] **Speaker 0:** similar procedure, you're looking at a cell that surrounds a
[00:15:28:299 - 00:15:28:760] **Speaker 0:** point.
[00:15:30:919 - 00:15:32:960] **Speaker 0:** So a body or region of space is divided into
[00:15:32:960 - 00:15:34:679] **Speaker 0:** non-overlapping control volumes.
[00:15:35:359 - 00:15:38:159] **Speaker 0:** So instead of elements, we call them cells or control
[00:15:38:159 - 00:15:38:859] **Speaker 0:** volumes.
[00:15:40:840 - 00:15:42:299] **Speaker 0:** And they surround some point.
[00:15:42:719 - 00:15:44:080] **Speaker 0:** So a structured grid is not needed.
[00:15:44:280 - 00:15:46:559] **Speaker 0:** We're just looking at a mass balance within that cell.
[00:15:48:690 - 00:15:52:109] **Speaker 0:** And we're integrating again the equation over the control volume.
[00:15:53:030 - 00:15:55:049] **Speaker 0:** Uh, making sure that we've got a consistent.
[00:15:55:979 - 00:15:59:320] **Speaker 0:** Uh, continuity or momentum balance.
[00:15:59:820 - 00:16:02:179] **Speaker 0:** So using Navier Stokes or continuity equation.
[00:16:06:070 - 00:16:07:489] **Speaker 0:** That's what I've discussed.
[00:16:10:820 - 00:16:13:849] **Speaker 0:** I guess if we do a nice flux balance on
[00:16:13:849 - 00:16:16:809] **Speaker 0:** one cell, the argument is that it exists also for
[00:16:16:809 - 00:16:17:570] **Speaker 0:** the full domain.
[00:16:18:349 - 00:16:20:669] **Speaker 0:** So it's consistent and, and conserved.
[00:16:20:710 - 00:16:23:549] **Speaker 0:** So those other, or at least the finite difference doesn't
[00:16:23:549 - 00:16:26:599] **Speaker 0:** have this property, uh, which is why people tend to
[00:16:26:599 - 00:16:30:349] **Speaker 0:** use finite volume for CFD rather than finite difference.
[00:16:34:080 - 00:16:34:679] **Speaker 0:** Cool.
[00:16:35:039 - 00:16:35:640] **Speaker 0:** All right.
[00:16:39:880 - 00:16:43:159] **Speaker 0:** Any questions on these slides?
[00:16:44:700 - 00:16:45:500] **Speaker 0:** It's a bit of an overview.
[00:16:45:539 - 00:16:47:900] **Speaker 0:** I, I just want to give some sort of roadmap
[00:16:47:900 - 00:16:49:219] **Speaker 0:** to where we're going for the rest of the course,
[00:16:49:299 - 00:16:51:260] **Speaker 0:** so I don't get too hung up on the details.
[00:16:51:580 - 00:16:53:900] **Speaker 0:** So it should make a lot more sense after a
[00:16:53:900 - 00:16:54:419] **Speaker 0:** few weeks.
[00:16:56:330 - 00:16:56:799] **Speaker 0:** Yeah.
[00:16:57:739 - 00:16:58:260] **Speaker 0:** Who?
[00:16:59:469 - 00:17:03:080] **Speaker 0:** So I've I think you've already probably gone through the
[00:17:03:080 - 00:17:05:199] **Speaker 0:** synopsis, but I just wanted to point out a couple
[00:17:05:199 - 00:17:06:180] **Speaker 0:** of things.
[00:17:12:989 - 00:17:16:729] **Speaker 0:** That's a synopsis that's up on the learn page under
[00:17:16:729 - 00:17:20:188] **Speaker 0:** assessment, or, I don't know, course information somewhere we've uploaded
[00:17:20:188 - 00:17:20:489] **Speaker 0:** it.
[00:17:21:619 - 00:17:30:839] **Speaker 0:** Um So Yeah, I guess, yeah, the main goal, or
[00:17:30:839 - 00:17:32:839] **Speaker 0:** one of the main goals of this course is to
[00:17:32:839 - 00:17:34:880] **Speaker 0:** try and get you to sort of understand how to
[00:17:34:880 - 00:17:38:780] **Speaker 0:** solve partial differential equations, how you're approaching a, a problem
[00:17:39:079 - 00:17:42:660] **Speaker 0:** of approximating, uh, true physics with a model.
[00:17:44:390 - 00:17:48:030] **Speaker 0:** And obviously we're going to make assumptions that may or
[00:17:48:030 - 00:17:48:890] **Speaker 0:** may not be true.
[00:17:49:310 - 00:17:50:829] **Speaker 0:** So just because you have a result doesn't mean that
[00:17:50:829 - 00:17:51:829] **Speaker 0:** it's going to be accurate.
[00:17:52:900 - 00:17:55:760] **Speaker 0:** We're also gonna be using console, uh, but we're first,
[00:17:56:270 - 00:17:59:079] **Speaker 0:** we're also alongside going to be looking at the finite
[00:17:59:079 - 00:18:04:280] **Speaker 0:** element method, so how does console solve these, uh, problems.
[00:18:05:449 - 00:18:07:369] **Speaker 0:** So trying to not treat it as a black box
[00:18:07:650 - 00:18:10:410] **Speaker 0:** in the sense that we just have some input and
[00:18:10:410 - 00:18:12:270] **Speaker 0:** hope that an output makes sense.
[00:18:18:650 - 00:18:22:489] **Speaker 0:** Uh, well, the, so the final exam is worth 50%,
[00:18:22:569 - 00:18:25:739] **Speaker 0:** but you need at least At least 40% in the
[00:18:25:739 - 00:18:30:430] **Speaker 0:** exam to pass the course as well, um, Yeah.
[00:18:32:280 - 00:18:34:959] **Speaker 0:** So just, just to note that, but hopefully, I think
[00:18:34:959 - 00:18:37:479] **Speaker 0:** if you have a good understanding of the course, 40%
[00:18:37:479 - 00:18:38:880] **Speaker 0:** should be fine for the exam.
[00:18:41:380 - 00:18:42:010] **Speaker 0:** OK.
[00:18:46:579 - 00:18:52:369] **Speaker 0:** Any questions on Admin or course structure.
[00:18:59:189 - 00:19:04:819] **Speaker 0:** No I've sorted out the, the, um, that survey.
[00:19:04:890 - 00:19:05:579] **Speaker 0:** I opened it up.
[00:19:05:859 - 00:19:06:619] **Speaker 0:** It worked out quite well.
[00:19:06:699 - 00:19:08:180] **Speaker 0:** I added some questions in at the end.
[00:19:08:900 - 00:19:09:979] **Speaker 0:** Um, on AI use.
[00:19:10:060 - 00:19:13:119] **Speaker 0:** So I'm, I'm keen to hear your opinions.
[00:19:14:189 - 00:19:17:290] **Speaker 0:** The survey, you have to log in just to make
[00:19:17:290 - 00:19:18:189] **Speaker 0:** sure that it's not.
[00:19:19:060 - 00:19:20:750] **Speaker 0:** I guess you know you're not doing heaps of surveys
[00:19:20:750 - 00:19:22:420] **Speaker 0:** for one person, but it is anonymous.
[00:19:22:469 - 00:19:24:589] **Speaker 0:** I don't know what you've answered per person.
[00:20:51:989 - 00:21:32:979] **Speaker 0:** Um So I can start to share results.
[00:21:33:920 - 00:21:34:609] **Speaker 0:** Um.
[00:21:43:380 - 00:21:45:619] **Speaker 0:** I can't multitask, but I'll talk over.
[00:21:46:660 - 00:21:50:579] **Speaker 0:** You anyway, as, as people are filling them out, so.
[00:21:51:410 - 00:21:53:890] **Speaker 0:** I, I guess it's not that very interesting, but we
[00:21:53:890 - 00:21:56:520] **Speaker 0:** kind of already know what this, the ratios are, but,
[00:21:56:530 - 00:22:01:060] **Speaker 0:** um, Yeah, I think that's about right, 2:1 ratio-ish.
[00:22:01:219 - 00:22:03:910] **Speaker 0:** I think there's some more trans students, but they probably
[00:22:03:910 - 00:22:06:550] **Speaker 0:** doing the aerobic Cup already, um.
[00:22:09:880 - 00:22:11:800] **Speaker 0:** That's, that's fun, that it's always refreshing.
[00:22:13:390 - 00:22:17:189] **Speaker 0:** Uh, so, uh, quite a few people from Auckland, um.
[00:22:18:219 - 00:22:20:109] **Speaker 0:** A lot of people from Auckland, so they chose against
[00:22:20:109 - 00:22:22:310] **Speaker 0:** Auckland Uni, which is great, um.
[00:22:26:390 - 00:22:28:430] **Speaker 0:** And yeah, a decent amount.
[00:22:28:829 - 00:22:30:010] **Speaker 0:** So quite a few from Wellington.
[00:22:31:079 - 00:22:34:150] **Speaker 0:** So I'm from Taranaki or New Plymouth, one person from
[00:22:34:150 - 00:22:35:140] **Speaker 0:** Taranaki, so that's cool.
[00:22:35:969 - 00:22:38:530] **Speaker 0:** Um, yeah, so I grew up in New Plymouth and
[00:22:38:530 - 00:22:40:810] **Speaker 0:** I came down here for my studies and stayed on.
[00:22:42:229 - 00:22:49:750] **Speaker 0:** Um, Some people from overseas, I think there's some that
[00:22:49:750 - 00:22:51:020] **Speaker 0:** do study abroad.
[00:22:51:069 - 00:22:51:550] **Speaker 0:** I don't know.
[00:22:51:829 - 00:22:53:189] **Speaker 0:** I mean, when I went through, there was one or
[00:22:53:189 - 00:22:54:949] **Speaker 0:** two of my classmates that went over to the States
[00:22:54:949 - 00:22:56:510] **Speaker 0:** to like a semester abroad.
[00:22:56:790 - 00:22:58:459] **Speaker 0:** I don't know if you're that familiar with that process,
[00:22:58:550 - 00:23:00:550] **Speaker 0:** but if you're interested in that, maybe you want to
[00:23:00:550 - 00:23:01:209] **Speaker 0:** do that too.
[00:23:07:949 - 00:23:09:630] **Speaker 0:** I don't know if we can scroll down or if
[00:23:09:630 - 00:23:11:050] **Speaker 0:** it's just gonna keep refreshing.
[00:23:11:469 - 00:23:13:020] **Speaker 0:** Oh, Python, do nothing.
[00:23:13:069 - 00:23:13:910] **Speaker 0:** Oh no.
[00:23:14:630 - 00:23:15:469] **Speaker 0:** Oh, no, no, that's 0.
[00:23:15:520 - 00:23:16:619] **Speaker 0:** OK, so that's purple.
[00:23:17:739 - 00:23:19:589] **Speaker 0:** Alright, take the upcoming Tuesday.
[00:23:19:819 - 00:23:22:650] **Speaker 0:** OK, so that's reassuring that cos Tuesday's not too far
[00:23:22:650 - 00:23:23:910] **Speaker 0:** away now, um.
[00:23:28:270 - 00:23:28:739] **Speaker 0:** Yeah.
[00:23:34:540 - 00:23:38:099] **Speaker 0:** So I think mechatronics don't do finite differencing in your,
[00:23:38:660 - 00:23:39:500] **Speaker 0:** in your class.
[00:23:39:579 - 00:23:41:619] **Speaker 0:** You do different maths course, which is fine.
[00:23:41:790 - 00:23:45:540] **Speaker 0:** Don't feel like you're behind because what I go through
[00:23:45:540 - 00:23:47:099] **Speaker 0:** in this course is from the basics.
[00:23:47:300 - 00:23:48:229] **Speaker 0:** So you have the same.
[00:23:49:109 - 00:23:51:199] **Speaker 0:** Grounding or same fundamental start.
[00:23:52:569 - 00:23:53:449] **Speaker 0:** So, yeah.
[00:23:55:180 - 00:23:57:119] **Speaker 0:** Uh, this one's confusing because it's.
[00:23:58:109 - 00:24:02:630] **Speaker 0:** Yeah It's a mixture, so it's not 21% of everyone
[00:24:02:630 - 00:24:03:750] **Speaker 0:** can solve linear equations.
[00:24:03:800 - 00:24:07:699] **Speaker 0:** It's, yeah, it's not a great, great visual, um, but
[00:24:07:699 - 00:24:08:989] **Speaker 0:** it looks like most people can.
[00:24:09:750 - 00:24:11:920] **Speaker 0:** And Yeah.
[00:24:12:849 - 00:24:14:939] **Speaker 0:** I've gone away from a cheat sheet for the exam
[00:24:14:939 - 00:24:16:180] **Speaker 0:** to a formula sheet.
[00:24:16:420 - 00:24:17:579] **Speaker 0:** So I did that last year and I'll do the
[00:24:17:579 - 00:24:20:219] **Speaker 0:** same this year, um, because I often get questions of,
[00:24:20:270 - 00:24:22:229] **Speaker 0:** oh, what should I include in my cheat sheet, etc.
[00:24:22:300 - 00:24:22:660] **Speaker 0:** etc.
[00:24:22:859 - 00:24:25:180] **Speaker 0:** And then there's all, always those who like to include
[00:24:25:180 - 00:24:26:280] **Speaker 0:** everything on their cheat sheet.
[00:24:26:810 - 00:24:28:979] **Speaker 0:** Um, so I can't remember.
[00:24:29:020 - 00:24:31:069] **Speaker 0:** I think I did put the differential of sign, but
[00:24:32:300 - 00:24:35:150] **Speaker 0:** Yeah, I guess in an exam, maybe you get busted
[00:24:35:150 - 00:24:36:589] **Speaker 0:** or you're, you're not sure what's happening.
[00:24:36:750 - 00:24:39:910] **Speaker 0:** Uh, that's always Some sometimes in a shoe.
[00:24:40:760 - 00:24:43:020] **Speaker 0:** Um, I have been asked if you have to do
[00:24:43:020 - 00:24:45:410] **Speaker 0:** integration in the exam, and you should be able to
[00:24:45:410 - 00:24:46:719] **Speaker 0:** do integration as well.
[00:24:49:050 - 00:24:50:020] **Speaker 0:** Separation of variables.
[00:24:50:219 - 00:24:52:410] **Speaker 0:** So again, I think that's something that you cover a
[00:24:52:410 - 00:24:54:819] **Speaker 0:** little bit in, in 1 or 2nd year, and we
[00:24:54:819 - 00:24:55:819] **Speaker 0:** just go through that a little bit.
[00:24:56:109 - 00:24:59:239] **Speaker 0:** It's a nice tool for analytical solutions to LPDs.
[00:25:00:290 - 00:25:03:560] **Speaker 0:** And solving systems of linear equations again, it's something that
[00:25:03:560 - 00:25:06:910] **Speaker 0:** you do with like the Gs, um, sad and other
[00:25:06:910 - 00:25:10:670] **Speaker 0:** sort of schemes or Jacobi method, uh, or you could.
[00:25:11:449 - 00:25:13:770] **Speaker 0:** Delegate it to Python or something else, if you have
[00:25:13:770 - 00:25:14:290] **Speaker 0:** a computer.
[00:25:15:699 - 00:25:17:810] **Speaker 0:** So fluid mechanics, again, I think there's quite a few
[00:25:17:810 - 00:25:20:540] **Speaker 0:** mechatronic, mechatronics students that did fluids this year.
[00:25:20:780 - 00:25:23:420] **Speaker 0:** Uh, it's quite a popular course, but I realise not
[00:25:23:420 - 00:25:25:619] **Speaker 0:** everyone is doing that and we don't focus it on
[00:25:25:619 - 00:25:28:560] **Speaker 0:** this course, but it is my background, uh, so that's
[00:25:28:979 - 00:25:31:459] **Speaker 0:** obviously better than FEA but, um, yeah.
[00:25:32:349 - 00:25:33:949] **Speaker 0:** So course reader.
[00:25:37:199 - 00:25:39:640] **Speaker 0:** Oh yeah, so there are still course readers outside my
[00:25:39:640 - 00:25:39:839] **Speaker 0:** office.
[00:25:39:890 - 00:25:43:339] **Speaker 0:** I think there's still 80 or more copies.
[00:25:43:859 - 00:25:48:199] **Speaker 0:** Um, I always print, obviously not as many copies as
[00:25:48:199 - 00:25:50:719] **Speaker 0:** students because not everyone picks up one, but I always
[00:25:50:719 - 00:25:54:040] **Speaker 0:** seem to throw away boxes of course readers, so I
[00:25:54:040 - 00:25:58:170] **Speaker 0:** try to sort of, Yeah, printed enough, but there should
[00:25:58:170 - 00:26:00:089] **Speaker 0:** be plenty, um.
[00:26:03:640 - 00:26:07:270] **Speaker 0:** But that being fifty-fifty, I guess, is, is interesting.
[00:26:08:130 - 00:26:12:209] **Speaker 0:** So your ideas So do you still use Wing in
[00:26:12:209 - 00:26:12:750] **Speaker 0:** 1st year?
[00:26:12:930 - 00:26:13:859] **Speaker 0:** Do they do that or not?
[00:26:14:020 - 00:26:14:680] **Speaker 0:** They do.
[00:26:15:609 - 00:26:18:380] **Speaker 0:** And then you're using Spider because Jeff is using it,
[00:26:18:420 - 00:26:18:880] **Speaker 0:** or?
[00:26:19:500 - 00:26:22:699] **Speaker 0:** Yeah, yeah, because we switched to Python, it must have
[00:26:22:699 - 00:26:24:979] **Speaker 0:** been 3 or 4 years ago now from MATLAB, and
[00:26:24:979 - 00:26:27:900] **Speaker 0:** Spider is the closest to MATLAB, in my opinion, which
[00:26:27:900 - 00:26:29:689] **Speaker 0:** is why I've used it for this course.
[00:26:30:060 - 00:26:32:770] **Speaker 0:** It's nice that you can have, I guess the figures
[00:26:32:770 - 00:26:37:780] **Speaker 0:** inside, um, and you have a variables explorer, uh, and
[00:26:37:780 - 00:26:38:219] **Speaker 0:** things like that.
[00:26:38:300 - 00:26:39:819] **Speaker 0:** So a few features that are quite handy.
[00:26:41:239 - 00:26:43:849] **Speaker 0:** Visual Studio code, I think that's what people sort of
[00:26:43:849 - 00:26:44:989] **Speaker 0:** use in industry, they.
[00:26:46:000 - 00:26:48:540] **Speaker 0:** More familiar with that and you can embed, embed other
[00:26:49:000 - 00:26:49:719] **Speaker 0:** apps into it.
[00:26:50:400 - 00:26:54:079] **Speaker 0:** And yeah, Pie charm, I've seen, um, yep.
[00:26:55:189 - 00:26:57:599] **Speaker 0:** Class reps, so I, I didn't really talk to my
[00:26:57:599 - 00:26:58:859] **Speaker 0:** class reps when I was a student.
[00:26:59:739 - 00:27:02:979] **Speaker 0:** And I guess we only get feedback if it's bad,
[00:27:03:420 - 00:27:05:780] **Speaker 0:** um, at the end of the course, which is too
[00:27:05:780 - 00:27:06:199] **Speaker 0:** late.
[00:27:06:500 - 00:27:09:020] **Speaker 0:** So I, I guess make sure that you communicate with
[00:27:09:020 - 00:27:09:959] **Speaker 0:** your class reps.
[00:27:10:250 - 00:27:12:500] **Speaker 0:** Um, I don't know exactly.
[00:27:12:619 - 00:27:16:670] **Speaker 0:** Yeah, it's not something that I'm not sure how heavily
[00:27:16:670 - 00:27:20:579] **Speaker 0:** advertised it is, but if you go on the Um,
[00:27:20:670 - 00:27:24:900] **Speaker 0:** undergraduate learn course page, which is quite heavy, there's a
[00:27:24:900 - 00:27:27:229] **Speaker 0:** lot of tabs, but you can find the, the class
[00:27:27:229 - 00:27:27:930] **Speaker 0:** reps there.
[00:27:28:709 - 00:27:31:010] **Speaker 0:** Um, so I might reach out to those class reps.
[00:27:32:060 - 00:27:33:930] **Speaker 0:** At the end of the term or early next term
[00:27:33:930 - 00:27:36:280] **Speaker 0:** just to get a feeling of what's, what's going on.
[00:27:37:199 - 00:27:42:640] **Speaker 0:** Um, Yeah So the AI stuff, well, we have to
[00:27:42:640 - 00:27:44:260] **Speaker 0:** figure out what we're doing for the assessments.
[00:27:45:020 - 00:27:47:189] **Speaker 0:** Uh, in the past, I've just said no AI use
[00:27:47:560 - 00:27:49:579] **Speaker 0:** because I want you to learn how to code.
[00:27:50:500 - 00:27:56:359] **Speaker 0:** And do analysing, problem solving, um, I don't think it's
[00:27:56:359 - 00:27:57:290] **Speaker 0:** worthwhile outsourcing.
[00:27:57:410 - 00:27:59:069] **Speaker 0:** So we had the net industry event.
[00:28:00:010 - 00:28:02:130] **Speaker 0:** Uh, it was last week, I saw one or two
[00:28:02:130 - 00:28:02:969] **Speaker 0:** of you, which was cool.
[00:28:03:319 - 00:28:04:810] **Speaker 0:** Uh, and I was talking to some of the guys
[00:28:04:810 - 00:28:05:930] **Speaker 0:** that were recent graduates.
[00:28:06:079 - 00:28:07:609] **Speaker 0:** So that some, some of them are using it for
[00:28:07:609 - 00:28:08:449] **Speaker 0:** coding and things like that.
[00:28:08:770 - 00:28:11:530] **Speaker 0:** Uh, but obviously they have a little bit more background
[00:28:11:530 - 00:28:14:489] **Speaker 0:** knowledge of, is the output correct so they can scan
[00:28:14:489 - 00:28:17:010] **Speaker 0:** through the output of Cloud or Gemini or whatever code
[00:28:17:010 - 00:28:17:609] **Speaker 0:** that they're using.
[00:28:18:290 - 00:28:22:420] **Speaker 0:** Uh, to ensure that what the Sending to the client
[00:28:22:420 - 00:28:23:599] **Speaker 0:** is, is accurate.
[00:28:24:020 - 00:28:27:550] **Speaker 0:** So whereas you, you're learning how to, hopefully learning everything,
[00:28:27:650 - 00:28:30:060] **Speaker 0:** um, so you're learning how to code and how, how
[00:28:30:060 - 00:28:30:630] **Speaker 0:** everything works.
[00:28:31:060 - 00:28:35:380] **Speaker 0:** So I feel that outsourcing that learning is, is a
[00:28:35:380 - 00:28:36:099] **Speaker 0:** bad idea.
[00:28:36:500 - 00:28:38:660] **Speaker 0:** So I just wanted to know what the class felt.
[00:28:44:400 - 00:28:45:510] **Speaker 0:** Yeah, so.
[00:28:46:829 - 00:28:50:640] **Speaker 0:** That's reasonably reassuring that, that, that is also felt in
[00:28:50:640 - 00:28:52:530] **Speaker 0:** the class, so that, that's, that's good.
[00:28:54:069 - 00:29:00:069] **Speaker 0:** Um, Yeah, I don't know what the other classes, other
[00:29:00:069 - 00:29:04:390] **Speaker 0:** courses actually do for these in the end, um, I
[00:29:04:390 - 00:29:05:829] **Speaker 0:** feel like it's a slippery slope as well.
[00:29:05:910 - 00:29:08:949] **Speaker 0:** If you, if you permit some use, then it can
[00:29:08:949 - 00:29:09:609] **Speaker 0:** be a little bit.
[00:29:10:829 - 00:29:12:290] **Speaker 0:** Challenging to differentiate.
[00:29:13:219 - 00:29:17:000] **Speaker 0:** Um, and those, it's always dangerous to have, to have,
[00:29:17:619 - 00:29:20:699] **Speaker 0:** uh, uh, you, uh, open questions, I'll look at that
[00:29:20:699 - 00:29:22:040] **Speaker 0:** later, um.
[00:29:23:630 - 00:29:24:530] **Speaker 0:** I'm sure it's fine.
[00:29:24:869 - 00:29:26:189] **Speaker 0:** Alright, so.
[00:29:27:390 - 00:29:28:540] **Speaker 0:** OK, so I think that's.
[00:29:29:750 - 00:29:32:630] **Speaker 0:** Everything prior to starting on the course, reader, is there
[00:29:32:630 - 00:29:36:069] **Speaker 0:** any questions, comments?
[00:29:40:540 - 00:29:40:560] **Speaker 0:** Cool.
[00:29:42:060 - 00:29:44:219] **Speaker 0:** Alright, so apart from those 9 that don't have their
[00:29:44:219 - 00:29:48:599] **Speaker 0:** course readers, um, we can start on chapter 1.
[00:30:11:319 - 00:30:12:910] **Speaker 0:** All right, cool.
[00:30:13:329 - 00:30:16:800] **Speaker 0:** So don't have to roll on PDFs and slow computers,
[00:30:16:849 - 00:30:18:189] **Speaker 0:** we can just use pen and paper.
[00:30:19:000 - 00:30:21:000] **Speaker 0:** Uh, for the, for the remainder, or most of it.
[00:30:21:079 - 00:30:24:550] **Speaker 0:** So I'll also introduce some of the codes that are
[00:30:24:560 - 00:30:28:839] **Speaker 0:** associated with the examples with the laptop using spider.
[00:30:30:020 - 00:30:32:819] **Speaker 0:** Those scripts are all on the course material folder on
[00:30:32:819 - 00:30:34:900] **Speaker 0:** Learn, so you can download those ahead of time if
[00:30:34:900 - 00:30:36:160] **Speaker 0:** you want to, to flick through.
[00:30:38:199 - 00:30:41:479] **Speaker 0:** So partial differential equations, why are we here?
[00:30:41:560 - 00:30:42:589] **Speaker 0:** Why do we want to look at this?
[00:30:42:760 - 00:30:44:680] **Speaker 0:** So a lot of problems in engineering and physics involve
[00:30:44:680 - 00:30:47:050] **Speaker 0:** variables which change in space and time.
[00:30:47:520 - 00:30:49:640] **Speaker 0:** So some examples is temperature variation in a room.
[00:30:49:760 - 00:30:53:079] **Speaker 0:** So maybe we're looking at the air conditioning, um, so
[00:30:53:079 - 00:30:54:589] **Speaker 0:** displacement and the deformed body.
[00:30:54:880 - 00:30:58:540] **Speaker 0:** So we're looking at some beams, uh, maybe, uh, aerofoil
[00:30:58:540 - 00:30:58:800] **Speaker 0:** again.
[00:30:58:880 - 00:31:00:180] **Speaker 0:** I don't know why I keep going to that.
[00:31:00:520 - 00:31:03:199] **Speaker 0:** Um, and in the first lab next week with console,
[00:31:03:239 - 00:31:04:040] **Speaker 0:** we're gonna look at a wrench.
[00:31:04:119 - 00:31:06:479] **Speaker 0:** So how much does a wrench displace subject to some
[00:31:06:479 - 00:31:07:599] **Speaker 0:** force, some loading.
[00:31:09:300 - 00:31:11:699] **Speaker 0:** Another example here is velocity in a flowing fluid.
[00:31:12:020 - 00:31:15:579] **Speaker 0:** So maybe we want to look at um pipe flow,
[00:31:15:750 - 00:31:16:819] **Speaker 0:** blood clot or something like that.
[00:31:17:709 - 00:31:22:280] **Speaker 0:** Or Another example would be looking at dams and how
[00:31:22:280 - 00:31:22:880] **Speaker 0:** they work.
[00:31:24:310 - 00:31:28:119] **Speaker 0:** So the equation which governs the distribution and evolution of
[00:31:28:119 - 00:31:32:359] **Speaker 0:** these variables, so temperature would be T, displacement field would
[00:31:32:359 - 00:31:32:739] **Speaker 0:** be.
[00:31:33:630 - 00:31:36:589] **Speaker 0:** Um, I don't know what they use UVW maybe, velocity
[00:31:36:589 - 00:31:37:369] **Speaker 0:** is UVW.
[00:31:38:229 - 00:31:42:359] **Speaker 0:** So all of these variables are combined into these partial
[00:31:42:359 - 00:31:43:430] **Speaker 0:** differential equations.
[00:31:45:219 - 00:31:48:099] **Speaker 0:** So I'll usually refer to them as PDEs.
[00:31:48:869 - 00:31:49:530] **Speaker 0:** That's for sure.
[00:31:51:160 - 00:31:53:520] **Speaker 0:** So a little bit of a reminder about partial differential
[00:31:53:520 - 00:31:58:140] **Speaker 0:** equations you've used PDs before, uh, just, just as a
[00:31:58:140 - 00:31:59:140] **Speaker 0:** quick reminder.
[00:31:59:760 - 00:32:01:160] **Speaker 0:** If we have a function you.
[00:32:02:060 - 00:32:05:329] **Speaker 0:** So function being something that varies in, in space, so
[00:32:05:329 - 00:32:05:930] **Speaker 0:** X and Y.
[00:32:06:750 - 00:32:09:380] **Speaker 0:** Um, it might be the temperature field or displacement field.
[00:32:09:599 - 00:32:12:439] **Speaker 0:** The partial derivative of U, so how much is you
[00:32:12:439 - 00:32:17:219] **Speaker 0:** changing with respect to x is given with curly DU
[00:32:17:219 - 00:32:18:130] **Speaker 0:** by DX.
[00:32:20:619 - 00:32:23:420] **Speaker 0:** The curly D is because it's a partial derivative, it's
[00:32:23:420 - 00:32:24:520] **Speaker 0:** not a full derivative.
[00:32:25:020 - 00:32:26:780] **Speaker 0:** It's also varying in the other direction.
[00:32:27:189 - 00:32:28:609] **Speaker 0:** So this is equal to the limit.
[00:32:31:420 - 00:32:34:640] **Speaker 0:** As our spacing, so delta X tends to 0.
[00:32:39:760 - 00:32:42:160] **Speaker 0:** So we want to look at essentially rise over run,
[00:32:42:469 - 00:32:45:540] **Speaker 0:** so we want to evaluate our function variable U at
[00:32:45:540 - 00:32:46:900] **Speaker 0:** X + X.
[00:32:49:290 - 00:32:50:619] **Speaker 0:** And it's fixed at some position.
[00:32:50:729 - 00:32:51:000] **Speaker 0:** Why?
[00:32:51:209 - 00:32:52:050] **Speaker 0:** Maybe I zoom in.
[00:32:56:719 - 00:33:04:540] **Speaker 0:** Uh minus You Of X Y.
[00:33:06:469 - 00:33:08:209] **Speaker 0:** Divided by delta x.
[00:33:09:459 - 00:33:12:020] **Speaker 0:** So rise over run, you overtax.
[00:33:25:520 - 00:33:27:920] **Speaker 0:** And for partial derivative of U with respect to Y,
[00:33:28:040 - 00:33:28:780] **Speaker 0:** that's very similar.
[00:33:29:000 - 00:33:32:479] **Speaker 0:** So we're still doing a partial derivative of U with
[00:33:32:479 - 00:33:33:160] **Speaker 0:** respect to Y.
[00:33:34:569 - 00:33:36:640] **Speaker 0:** Is the limit of delta Y 1 to 0.
[00:33:37:660 - 00:33:39:979] **Speaker 0:** And instead of varying in X, we're now varying in
[00:33:39:979 - 00:33:40:410] **Speaker 0:** Y.
[00:33:40:750 - 00:33:42:040] **Speaker 0:** So U at X.
[00:33:42:540 - 00:33:46:780] **Speaker 0:** Y plus delta Y minus U of X and Y.
[00:33:48:079 - 00:33:49:439] **Speaker 0:** Divided by a delta Y.
[00:33:55:780 - 00:33:59:680] **Speaker 0:** So a PDE involves partial derivatives of an unknown function
[00:33:59:859 - 00:34:02:660] **Speaker 0:** of two or more independent variables.
[00:34:02:859 - 00:34:04:859] **Speaker 0:** So if it was just one independent variable, that's an
[00:34:04:859 - 00:34:06:750] **Speaker 0:** ordinary differential equation, ODE.
[00:34:07:219 - 00:34:08:719] **Speaker 0:** So you've done plenty of that already.
[00:34:09:260 - 00:34:10:939] **Speaker 0:** So we're just extending it to PDEs.
[00:34:18:110 - 00:34:27:709] **Speaker 0:** So Uh, we can visualise these functions in 1 and
[00:34:27:709 - 00:34:28:388] **Speaker 0:** 2 dimensions.
[00:34:28:628 - 00:34:31:570] **Speaker 0:** So on one day, maybe we have a curve.
[00:34:35:530 - 00:34:36:050] **Speaker 0:** Right, so.
[00:34:38:330 - 00:34:43:148] **Speaker 0:** And We want to evaluate at 2 points.
[00:34:46:679 - 00:34:49:040] **Speaker 0:** You can't see, oh, OK.
[00:34:50:148 - 00:34:50:949] **Speaker 0:** That's gonna be fun.
[00:34:51:860 - 00:34:52:860] **Speaker 0:** Alright, next one.
[00:34:53:520 - 00:34:56:360] **Speaker 0:** And another point at say X2.
[00:34:59:929 - 00:35:01:149] **Speaker 0:** So reasonably arbitrary.
[00:35:02:010 - 00:35:03:169] **Speaker 0:** Just pick 2 points.
[00:35:06:770 - 00:35:13:260] **Speaker 0:** And we want to evaluate if At X1 and F
[00:35:13:260 - 00:35:14:060] **Speaker 0:** at X2.
[00:35:15:020 - 00:35:16:830] **Speaker 0:** So FXX1.
[00:35:19:530 - 00:35:20:780] **Speaker 0:** And FLX 2.
[00:35:25:139 - 00:35:27:080] **Speaker 0:** So that delta X.
[00:35:29:780 - 00:35:31:219] **Speaker 0:** Ranges between the two.
[00:35:32:320 - 00:35:34:899] **Speaker 0:** Goes from X1 up to X2, so X2 minus X1.
[00:35:36:520 - 00:35:41:300] **Speaker 0:** And if we're approximating the gradient between those two points,
[00:35:41:760 - 00:35:44:080] **Speaker 0:** we'd end up with something like this because we're doing
[00:35:44:080 - 00:35:44:800] **Speaker 0:** wiser a run.
[00:35:45:040 - 00:35:46:340] **Speaker 0:** That's with our formula just before.
[00:35:47:270 - 00:35:50:050] **Speaker 0:** Um, which is going to be a pretty crude approximation
[00:35:50:050 - 00:35:52:489] **Speaker 0:** to the derivative at X1.
[00:35:53:090 - 00:35:56:209] **Speaker 0:** So that's why as delta X reduces to zero, we,
[00:35:56:719 - 00:35:59:870] **Speaker 0:** uh, approach the derivative at that point.
[00:36:01:100 - 00:36:03:340] **Speaker 0:** Just to be Pedantic.
[00:36:03:689 - 00:36:07:669] **Speaker 0:** So, This is illustrating why we might choose different mesh
[00:36:07:669 - 00:36:11:550] **Speaker 0:** resolutions later on, uh, in terms of spacings down to
[00:36:11:550 - 00:36:12:070] **Speaker 0:** X.
[00:36:13:360 - 00:36:15:000] **Speaker 0:** And as we reduce that to X, we expect to
[00:36:15:000 - 00:36:17:520] **Speaker 0:** have a more accurate approximation to those derivatives.
[00:36:19:919 - 00:36:24:649] **Speaker 0:** In 2D Think of those weather maps.
[00:36:24:729 - 00:36:27:439] **Speaker 0:** We've got those isobars or if you've gone hiking, you've
[00:36:27:439 - 00:36:28:610] **Speaker 0:** got the topology.
[00:36:29:250 - 00:36:31:909] **Speaker 0:** So these are just lines of constant value.
[00:36:37:870 - 00:36:39:350] **Speaker 0:** For example, maybe the inner.
[00:36:40:370 - 00:36:41:459] **Speaker 0:** Contour is 10.
[00:36:43:399 - 00:36:44:020] **Speaker 0:** 20.
[00:36:45:449 - 00:36:55:620] **Speaker 0:** And 30 So now if we select a point.
[00:36:56:530 - 00:36:57:760] **Speaker 0:** That's in 2D space.
[00:36:58:189 - 00:36:59:639] **Speaker 0:** So we've got X and Y coordinates.
[00:37:00:560 - 00:37:01:469] **Speaker 0:** And.
[00:37:08:120 - 00:37:09:689] **Speaker 0:** This will be X1 Y1.
[00:37:13:860 - 00:37:15:949] **Speaker 0:** And another point.
[00:37:22:850 - 00:37:25:239] **Speaker 0:** Acts 2 Y1.
[00:37:36:270 - 00:37:37:469] **Speaker 0:** Hopefully that's legible.
[00:37:38:750 - 00:37:41:610] **Speaker 0:** So this is visualising in 2D what we described earlier
[00:37:41:699 - 00:37:43:939] **Speaker 0:** with a partial derivative in X.
[00:37:44:149 - 00:37:45:350] **Speaker 0:** So we're varying X.
[00:37:46:699 - 00:37:48:409] **Speaker 0:** Looking at data X spacing.
[00:37:57:219 - 00:37:58:879] **Speaker 0:** So change in U over change in X.
[00:38:00:290 - 00:38:03:770] **Speaker 0:** For a partial derivative in X, likewise for Y.
[00:38:04:510 - 00:38:07:050] **Speaker 0:** You might want to look at point Y.
[00:38:08:129 - 00:38:29:050] **Speaker 0:** To So just Yeah, going back to basics, but just
[00:38:29:350 - 00:38:32:429] **Speaker 0:** try and visualise what these partial derivatives mean and what
[00:38:32:429 - 00:38:35:750] **Speaker 0:** happens as you reduce those discrete, uh, length scales so
[00:38:35:750 - 00:38:36:669] **Speaker 0:** x y.
[00:38:38:929 - 00:38:39:370] **Speaker 0:** All right.
[00:38:47:830 - 00:38:50:100] **Speaker 0:** So some examples of PDEs.
[00:38:50:429 - 00:38:52:709] **Speaker 0:** So these are just made up, they're just pretty arbitrary.
[00:38:52:790 - 00:38:54:629] **Speaker 0:** They're not the Navier- Stokes equations or anything like that,
[00:38:54:949 - 00:38:58:149] **Speaker 0:** but we can see that I've got the curly D's,
[00:38:58:350 - 00:39:00:429] **Speaker 0:** so U D 2 U by D X 2 is
[00:39:00:429 - 00:39:03:389] **Speaker 0:** the second order of derivative in space, next, next direction.
[00:39:04:100 - 00:39:06:540] **Speaker 0:** Uh, we've got just the value you, so the, the
[00:39:06:540 - 00:39:06:979] **Speaker 0:** function u.
[00:39:08:120 - 00:39:09:229] **Speaker 0:** And then a constant one.
[00:39:10:459 - 00:39:14:760] **Speaker 0:** So the variable U which we differentiate is called the
[00:39:14:760 - 00:39:17:679] **Speaker 0:** dependent variable because it depends on things.
[00:39:18:300 - 00:39:20:419] **Speaker 0:** Whereas the ones we differentiate with respect to are called
[00:39:20:419 - 00:39:21:479] **Speaker 0:** the independent variables.
[00:39:22:729 - 00:39:25:550] **Speaker 0:** So dependent variable will be like the temperature, velocity field,
[00:39:26:010 - 00:39:27:590] **Speaker 0:** independent variable will be space or time.
[00:39:29:639 - 00:39:33:739] **Speaker 0:** So We can see an equation 1.3.
[00:39:37:520 - 00:39:41:399] **Speaker 0:** That our dependent variable is a function of X and
[00:39:41:399 - 00:39:41:800] **Speaker 0:** Y.
[00:39:43:679 - 00:39:46:500] **Speaker 0:** 1.3, we've got X and Y being the independent variables.
[00:39:48:830 - 00:39:53:669] **Speaker 0:** So the Partial differentiation is sometimes denoted by using the
[00:39:53:669 - 00:39:54:800] **Speaker 0:** indifferent verbal.
[00:39:55:629 - 00:39:57:199] **Speaker 0:** As a subscript, so.
[00:39:58:270 - 00:39:59:949] **Speaker 0:** I don't know, I, I usually write it out in
[00:39:59:949 - 00:40:03:489] **Speaker 0:** full like this because my math is not too extreme.
[00:40:03:949 - 00:40:06:139] **Speaker 0:** But if you want to tighten everything and concise your,
[00:40:06:189 - 00:40:08:469] **Speaker 0:** your writing, you can write.
[00:40:10:969 - 00:40:11:979] **Speaker 0:** DU by DX.
[00:40:13:649 - 00:40:16:919] **Speaker 0:** Equal to You subscript X.
[00:40:24:689 - 00:40:26:600] **Speaker 0:** So if you're reading some papers or looking at some
[00:40:26:600 - 00:40:29:969] **Speaker 0:** textbooks, and they have this notation, that's just what that
[00:40:29:969 - 00:40:30:389] **Speaker 0:** means.
[00:40:33:179 - 00:40:37:419] **Speaker 0:** And it expands for second-order derivatives as well, D2U by
[00:40:37:419 - 00:40:38:179] **Speaker 0:** DX2.
[00:40:40:590 - 00:40:45:780] **Speaker 0:** We've just got two X's for subscript, um, and mixed
[00:40:45:780 - 00:40:48:510] **Speaker 0:** partial derivatives D by D X D by D Y.
[00:40:50:770 - 00:40:51:290] **Speaker 0:** All right.
[00:40:52:050 - 00:40:53:010] **Speaker 0:** So that's just some terms.
[00:40:53:530 - 00:40:54:770] **Speaker 0:** So how do we solve PDEs?
[00:40:54:929 - 00:40:58:350] **Speaker 0:** So we've been given some PDE that we're trusting is
[00:40:58:350 - 00:40:59:729] **Speaker 0:** representative of some physics.
[00:41:01:100 - 00:41:03:179] **Speaker 0:** And we want to go about solving them because we
[00:41:03:179 - 00:41:06:379] **Speaker 0:** want to know the temperature over time, the temperature within
[00:41:06:379 - 00:41:07:000] **Speaker 0:** the space.
[00:41:09:340 - 00:41:12:320] **Speaker 0:** PDs are difficult to solve, so we won't sugarcoat it.
[00:41:13:100 - 00:41:15:629] **Speaker 0:** So there are many different methods that we can use.
[00:41:16:969 - 00:41:20:969] **Speaker 0:** So most of the analytical techniques involve transforming the PDE
[00:41:20:969 - 00:41:22:050] **Speaker 0:** into ODEs.
[00:41:23:340 - 00:41:26:459] **Speaker 0:** So if we can transform our partial differential equation into
[00:41:26:459 - 00:41:30:820] **Speaker 0:** an ordinary differential equation, so just of one independent variable,
[00:41:31:469 - 00:41:33:780] **Speaker 0:** then you can use all your tools that you've learned
[00:41:33:780 - 00:41:34:360] **Speaker 0:** so far.
[00:41:37:520 - 00:41:40:729] **Speaker 0:** So the methods available for solving PDEs include separation of
[00:41:40:729 - 00:41:41:489] **Speaker 0:** variables.
[00:41:42:469 - 00:41:47:889] **Speaker 0:** So this technique essentially reduces the PDE with independent variables
[00:41:48:110 - 00:41:49:510] **Speaker 0:** to NODEs.
[00:41:49:669 - 00:41:54:790] **Speaker 0:** So if you had 2 Uh, in variables, so if
[00:41:54:790 - 00:41:56:909] **Speaker 0:** X and Y, you end up with two ODEs to
[00:41:56:909 - 00:41:57:330] **Speaker 0:** solve.
[00:41:59:449 - 00:42:03:560] **Speaker 0:** So integral transforms, so Laplace Foyer transforms also reduce the
[00:42:03:560 - 00:42:04:889] **Speaker 0:** number of independent variables.
[00:42:05:840 - 00:42:07:399] **Speaker 0:** You could use a change of coordinate.
[00:42:08:239 - 00:42:11:560] **Speaker 0:** So you've probably seen the polar and cylindrical coordinates are
[00:42:11:560 - 00:42:14:459] **Speaker 0:** really helpful for describing space.
[00:42:15:669 - 00:42:20:590] **Speaker 0:** That's circular, because if you try and describe space, a
[00:42:20:590 - 00:42:24:149] **Speaker 0:** circular domain with Cartesian coordinates, so X and Y, it
[00:42:24:149 - 00:42:24:909] **Speaker 0:** gets quite tricky.
[00:42:25:229 - 00:42:27:050] **Speaker 0:** So it's much easier just to use our theta.
[00:42:27:469 - 00:42:30:429] **Speaker 0:** So you can often, uh, get around.
[00:42:31:439 - 00:42:34:189] **Speaker 0:** Solving equations by changing the coordinate system.
[00:42:36:550 - 00:42:39:199] **Speaker 0:** Transformation of the dependent variable.
[00:42:39:479 - 00:42:45:550] **Speaker 0:** So this method Transforms our unknown, uh, in our PDE
[00:42:45:550 - 00:42:47:429] **Speaker 0:** into a new unknown that is easier to find.
[00:42:47:550 - 00:42:50:389] **Speaker 0:** So we've given an example of that as well, um.
[00:42:51:669 - 00:42:54:709] **Speaker 0:** Yep The last one here, which is a little bit
[00:42:54:709 - 00:42:57:350] **Speaker 0:** more easier to interpret is the numerical methods.
[00:42:57:590 - 00:42:59:530] **Speaker 0:** So we're going to discretize our PDE.
[00:43:00:070 - 00:43:02:909] **Speaker 0:** So instead of trying to solve it analytically, which we'll
[00:43:02:909 - 00:43:06:949] **Speaker 0:** mostly leave to the mathematicians, we can discretize that continuous
[00:43:06:949 - 00:43:09:260] **Speaker 0:** space into a discrete set of cells.
[00:43:09:629 - 00:43:13:310] **Speaker 0:** So I talked over finite difference, volume and elements before.
[00:43:13:669 - 00:43:15:250] **Speaker 0:** Those are all numerical methods.
[00:43:19:580 - 00:43:22:070] **Speaker 0:** And you end up with a system of equations, and
[00:43:22:070 - 00:43:22:909] **Speaker 0:** we can solve that.
[00:43:23:260 - 00:43:23:949] **Speaker 0:** We can underline.
[00:43:25:699 - 00:43:27:459] **Speaker 0:** So quite often this is the only method that will
[00:43:27:459 - 00:43:27:729] **Speaker 0:** work.
[00:43:27:899 - 00:43:31:060] **Speaker 0:** So if you had an analytical solution to a PDE
[00:43:31:060 - 00:43:33:139] **Speaker 0:** you're just going to use that because it solves.
[00:43:33:770 - 00:43:37:560] **Speaker 0:** Um, very quickly, so you're just evaluating some, some terms.
[00:43:37:850 - 00:43:41:229] **Speaker 0:** Numerical methods are typically taking longer to solve to compute.
[00:43:44:179 - 00:43:49:570] **Speaker 0:** But Analytical solutions are only for very basic geometries typically.
[00:43:50:600 - 00:43:52:409] **Speaker 0:** Simplified, simplified assumptions.
[00:43:53:689 - 00:43:56:379] **Speaker 0:** So we're gonna most, mostly focus on the numerical methods.
[00:43:56:760 - 00:43:59:639] **Speaker 0:** Uh, we are also gonna do separation of variables, which
[00:43:59:639 - 00:44:03:080] **Speaker 0:** is some people's favourites, and we're going to compare our
[00:44:03:080 - 00:44:04:879] **Speaker 0:** numerical results with the analytical solutions.
[00:44:04:939 - 00:44:08:060] **Speaker 0:** So I talked about verification and validation.
[00:44:08:399 - 00:44:11:239] **Speaker 0:** So to ensure that our numerical methods work and build
[00:44:11:239 - 00:44:15:959] **Speaker 0:** confidence in our code, we want to validate against those
[00:44:15:959 - 00:44:16:840] **Speaker 0:** analytical solutions.
[00:44:16:919 - 00:44:19:979] **Speaker 0:** So that's what we're gonna use analytical solutions primarily for,
[00:44:20:360 - 00:44:22:199] **Speaker 0:** uh, but it was, yeah.
[00:44:29:449 - 00:44:29:929] **Speaker 0:** All right.
[00:44:30:610 - 00:44:32:889] **Speaker 0:** Any questions so far or sort of keeping up?
[00:44:33:169 - 00:44:36:229] **Speaker 0:** Hopefully it's just revision of earlier stuff, uh, reasonably revision
[00:44:36:229 - 00:44:36:949] **Speaker 0:** of earlier things.
[00:44:38:139 - 00:44:39:500] **Speaker 0:** So some more definitions.
[00:44:41:000 - 00:44:44:120] **Speaker 0:** So a solution of a PDE in some region are
[00:44:45:040 - 00:44:48:159] **Speaker 0:** of the space of independent variables, so temperature field within
[00:44:48:159 - 00:44:48:760] **Speaker 0:** this room.
[00:44:49:989 - 00:44:52:040] **Speaker 0:** Uh, for which all the partial derivatives appearing in the
[00:44:52:040 - 00:44:55:479] **Speaker 0:** equation exist and satisfy the equation everywhere.
[00:44:56:679 - 00:45:02:459] **Speaker 0:** Um So generally, there is a whole bunch of solutions
[00:45:02:459 - 00:45:06:530] **Speaker 0:** or functions that satisfy a set of equations.
[00:45:06:689 - 00:45:09:719] **Speaker 0:** So It's easy just to think of an example.
[00:45:09:879 - 00:45:12:520] **Speaker 0:** So these three functions, they all look quite different.
[00:45:12:709 - 00:45:15:000] **Speaker 0:** One's got quadratics and X and Y.
[00:45:15:389 - 00:45:18:479] **Speaker 0:** One's got, um, sinusoidal term and exponential, and the last
[00:45:18:479 - 00:45:19:899] **Speaker 0:** one's got a log, natural log.
[00:45:20:439 - 00:45:22:000] **Speaker 0:** So these are all very different functions.
[00:45:22:080 - 00:45:24:000] **Speaker 0:** You can imagine them being plotted out in X Y
[00:45:24:000 - 00:45:25:459] **Speaker 0:** space and they're looking very different.
[00:45:26:239 - 00:45:28:919] **Speaker 0:** So that all solutions of the following PDE.
[00:45:32:979 - 00:45:38:489] **Speaker 0:** So 2nd order in X, so D2U by DX2 plus.
[00:45:39:850 - 00:45:41:840] **Speaker 0:** D2U by DY2.
[00:45:43:260 - 00:45:44:260] **Speaker 0:** Equal to 0.
[00:45:50:010 - 00:45:53:929] **Speaker 0:** So This is, I guess, one of the more basic
[00:45:54:330 - 00:45:55:600] **Speaker 0:** PDEs that we can solve.
[00:45:56:389 - 00:45:57:949] **Speaker 0:** Uh, in fact, it's got its own name.
[00:45:58:100 - 00:45:59:750] **Speaker 0:** This is called the Laplace equation.
[00:46:07:560 - 00:46:09:760] **Speaker 0:** And we're going to dive more into this equation in
[00:46:09:760 - 00:46:12:060] **Speaker 0:** the next few chapters and solve.
[00:46:14:909 - 00:46:19:580] **Speaker 0:** So How can we check whether or not these solutions
[00:46:20:120 - 00:46:23:879] **Speaker 0:** or these functions are a solution of this PDE?
[00:46:25:169 - 00:46:26:290] **Speaker 0:** I've got some paper.
[00:46:31:479 - 00:46:37:399] **Speaker 0:** Mm I'll just use this.
[00:46:42:129 - 00:46:44:840] **Speaker 0:** 1st, 1st math question of the day.
[00:46:46:750 - 00:46:48:260] **Speaker 0:** How do we check the.
[00:46:49:260 - 00:46:52:500] **Speaker 0:** This function is a solution to this equation.
[00:47:01:389 - 00:47:03:239] **Speaker 0:** We're just gonna substitute it directly in.
[00:47:03:590 - 00:47:08:909] **Speaker 0:** So what's the derivative of U with respect to D2U.
[00:47:10:070 - 00:47:16:280] **Speaker 0:** By DX 2 is equal to The second derivative of
[00:47:16:560 - 00:47:17:050] **Speaker 0:** D by DX.
[00:47:17:129 - 00:47:18:270] **Speaker 0:** So you can sort of break it up into two
[00:47:18:270 - 00:47:21:889] **Speaker 0:** bits, uh, instead of doing it twice, we're doing D
[00:47:21:889 - 00:47:24:570] **Speaker 0:** by DX and then we're differentiate differentiating that again.
[00:47:25:729 - 00:47:32:399] **Speaker 0:** So So D by DX, what's the derivative?
[00:47:33:340 - 00:47:36:459] **Speaker 0:** I won't wait, so 2 x um and then we
[00:47:36:459 - 00:47:37:260] **Speaker 0:** differentiate again.
[00:47:39:030 - 00:47:46:290] **Speaker 0:** What do we end up with Do And we can
[00:47:46:290 - 00:47:48:139] **Speaker 0:** do the same for.
[00:47:49:439 - 00:47:50:280] **Speaker 0:** And why?
[00:47:50:719 - 00:47:51:610] **Speaker 0:** Again, break it up.
[00:47:52:620 - 00:47:54:429] **Speaker 0:** Um, unless you would just want to go directly to
[00:47:54:429 - 00:48:01:340] **Speaker 0:** the result, but, UY DY, now we've got -2 Y.
[00:48:03:250 - 00:48:05:669] **Speaker 0:** And then we end up with -2.
[00:48:06:750 - 00:48:12:030] **Speaker 0:** So D2U by DX2 plus D2U by DY2.
[00:48:13:040 - 00:48:14:800] **Speaker 0:** Is equal to 2.
[00:48:15:699 - 00:48:17:110] **Speaker 0:** -2 equals 0.
[00:48:17:989 - 00:48:21:389] **Speaker 0:** And we said that our Laplace equation, equation 1.8 is
[00:48:21:389 - 00:48:22:110] **Speaker 0:** equal to 0.
[00:48:23:439 - 00:48:25:850] **Speaker 0:** So all we've done is substituted our function you equal
[00:48:25:850 - 00:48:28:770] **Speaker 0:** to X2 minus Y2 into our PDE and check that
[00:48:28:770 - 00:48:30:169] **Speaker 0:** it satisfies that equation.
[00:48:30:570 - 00:48:32:689] **Speaker 0:** So you can do these other two if you want
[00:48:32:689 - 00:48:36:100] **Speaker 0:** for homework if you are bored, but they will solve,
[00:48:36:239 - 00:48:40:530] **Speaker 0:** they will satisfy that Laplace equation, which brings to the
[00:48:40:530 - 00:48:42:149] **Speaker 0:** point, what is the solution.
[00:48:43:080 - 00:48:44:629] **Speaker 0:** Um, yeah.
[00:48:46:179 - 00:48:49:340] **Speaker 0:** So we're gonna talk about boundary.
[00:48:49:419 - 00:48:51:120] **Speaker 0:** Well, I guess we've got 2 minutes.
[00:48:51:739 - 00:48:52:659] **Speaker 0:** We can talk about these.
[00:48:53:060 - 00:48:56:419] **Speaker 0:** So essentially to constrain the solution, we're going to be
[00:48:56:419 - 00:48:58:860] **Speaker 0:** using boundary conditions to make sure that we've only got
[00:48:58:860 - 00:48:59:219] **Speaker 0:** one.
[00:48:59:889 - 00:49:01:550] **Speaker 0:** Uh, one final solution.
[00:49:04:780 - 00:49:07:139] **Speaker 0:** So the unique solution of a PDE corresponding to our
[00:49:07:139 - 00:49:11:060] **Speaker 0:** given physical problem, uh, is obtained by using those, those
[00:49:11:060 - 00:49:14:419] **Speaker 0:** boundary conditions or if it's time-dependent, we've got initial conditions,
[00:49:14:500 - 00:49:15:399] **Speaker 0:** so the initial state.
[00:49:17:010 - 00:49:19:139] **Speaker 0:** The order of a PDE is the highest order partial
[00:49:19:139 - 00:49:19:639] **Speaker 0:** derivative.
[00:49:20:070 - 00:49:22:780] **Speaker 0:** So if we flick back to equation 1.3, we've got
[00:49:22:780 - 00:49:26:860] **Speaker 0:** a second order derivative, uh, yeah, and Y and X.
[00:49:27:060 - 00:49:27:939] **Speaker 0:** So it's second order.
[00:49:31:050 - 00:49:36:429] **Speaker 0:** Linearity So PDE is linear if it is linear in
[00:49:36:429 - 00:49:39:229] **Speaker 0:** the unknown function and all its derivatives.
[00:49:41:439 - 00:49:44:580] **Speaker 0:** Um, so the coefficients only depend on the independent variables.
[00:49:44:699 - 00:49:46:989] **Speaker 0:** So essentially we don't want terms like U times U,
[00:49:47:219 - 00:49:48:540] **Speaker 0:** U times DU by DX.
[00:49:49:270 - 00:49:50:239] **Speaker 0:** Ah, etc.
[00:49:50:790 - 00:49:52:570] **Speaker 0:** So they shouldn't be multiplied by together.
[00:49:52:909 - 00:49:54:070] **Speaker 0:** So just some examples here.
[00:49:54:189 - 00:49:55:399] **Speaker 0:** The first equation.
[00:49:56:360 - 00:49:57:169] **Speaker 0:** will be linear.
[00:49:57:399 - 00:49:58:300] **Speaker 0:** The second one.
[00:50:00:370 - 00:50:01:469] **Speaker 0:** There's also linear.
[00:50:02:659 - 00:50:04:030] **Speaker 0:** The third one is not linear.
[00:50:04:149 - 00:50:06:909] **Speaker 0:** We've got this cube term, so it's a 2nd order
[00:50:06:909 - 00:50:10:510] **Speaker 0:** derivative of U, and then we cube it, so that's
[00:50:10:510 - 00:50:11:110] **Speaker 0:** nonlinear.
[00:50:12:439 - 00:50:14:719] **Speaker 0:** And the last one we've got U times D by
[00:50:14:719 - 00:50:17:639] **Speaker 0:** D D Y and that's, that's non-linear.
[00:50:20:010 - 00:50:23:290] **Speaker 0:** And a PD is homogeneous if all terms contain the
[00:50:23:290 - 00:50:25:469] **Speaker 0:** dependent variable or one of its derivatives.
[00:50:26:469 - 00:50:28:080] **Speaker 0:** Uh, so you can see here that we've got a
[00:50:28:080 - 00:50:30:760] **Speaker 0:** source term on the right, which is not, not a
[00:50:30:760 - 00:50:31:399] **Speaker 0:** function of you.
[00:50:33:419 - 00:50:33:739] **Speaker 0:** Cool.
[00:50:33:860 - 00:50:34:139] **Speaker 0:** All right.
[00:50:34:419 - 00:50:35:550] **Speaker 0:** So I think that's enough for today.
[00:50:35:939 - 00:50:36:590] **Speaker 0:** Um.
[00:50:37:939 - 00:50:40:389] **Speaker 0:** We will see you tomorrow.
[00:51:09:360 - 00:51:20:300] **Speaker 1:** Ah Uh, just a quick question.
[00:51:20:879 - 00:51:22:659] **Speaker 1:** I, I'm one of the students that's retaking this course
[00:51:22:659 - 00:51:23:129] **Speaker 1:** from last year.
[00:51:23:739 - 00:51:26:820] **Speaker 1:** Um, I found all the, they're getting clinically from last
[00:51:26:820 - 00:51:28:620] **Speaker 0:** year, and I was wondering out his pronouncement here that
[00:51:28:620 - 00:51:30:659] **Speaker 0:** you can apparently skip one of the tests if you
[00:51:30:659 - 00:51:31:780] **Speaker 0:** just use the same grade.
[00:51:31:889 - 00:51:32:340] **Speaker 0:** Is that possible?
[00:51:32:469 - 00:51:33:639] **Speaker 0:** Yep, yeah, just send me an email.
[00:51:33:899 - 00:51:34:469] **Speaker 0:** Just send you an email.
[00:51:34:709 - 00:51:36:840] **Speaker 0:** That's easy for the for the test on, uh, Monday,
[00:51:36:899 - 00:51:37:179] **Speaker 0:** yeah.
[00:51:37:495 - 00:51:38:004] **Speaker 0:** Just send me an email.
[00:51:38:024 - 00:51:38:375] **Speaker 0:** It's all good.
[00:51:38:465 - 00:51:40:455] **Speaker 0:** Send me an email, um, and I'll just check.
[00:51:40:534 - 00:51:41:574] **Speaker 0:** Did you pass last year?
[00:51:41:764 - 00:51:42:485] **Speaker 0:** Um, I did.
[00:51:42:534 - 00:51:43:254] **Speaker 0:** The test was easy.
[00:51:43:375 - 00:51:44:135] **Speaker 0:** Yeah, the test was fine.
[00:51:44:294 - 00:51:45:165] **Speaker 0:** Yeah, yeah, that should be fine.
[00:51:45:334 - 00:51:45:415] **Speaker 0:** Yeah.
[00:51:45:614 - 00:51:47:254] **Speaker 0:** The only thing I missed it last year was the
[00:51:47:254 - 00:51:49:235] **Speaker 0:** final exam, which I didn't have a good time for.
[00:51:50:215 - 00:51:51:245] **Speaker 0:** So, that I found that, you, pretty nice.
[00:51:51:294 - 00:51:52:274] **Speaker 0:** I liked your content as well.
[00:51:52:574 - 00:51:54:495] **Speaker 0:** So, yeah, yeah, send me an email and I can
[00:51:54:495 - 00:51:55:495] **Speaker 0:** just confirm it by writing.
[00:51:55:614 - 00:51:56:534] **Speaker 0:** But yeah, thank you.
[00:52:00:419 - 00:52:06:810] **Speaker 1:** Yeah, they related to them not, not, not directly.
[00:52:08:879 - 00:52:11:959] **Speaker 1:** So you get a people business.
[00:52:13:469 - 00:52:26:879] **Speaker 1:** uh I Uh, 8, it's pretty good.
[00:52:32:689 - 00:52:32:699] **Speaker 1:** I.
[00:52:35:780 - 00:52:35:790] **Speaker 1:** So.
[00:52:41:989 - 00:52:45:439] **Speaker 1:** Yeah Hey good how are you?
[00:52:46:300 - 00:52:48:739] **Speaker 2:** Um, I've done a lot of actual math lessons, so
[00:52:48:739 - 00:52:50:260] **Speaker 2:** I've done some stuff on linear.
[00:52:53:060 - 00:52:55:620] **Speaker 2:** Is there anything I should revise or?
[00:52:58:979 - 00:53:00:340] **Speaker 0:** I mean we touched on the question of where.
[00:53:01:540 - 00:53:04:080] **Speaker 0:** But I, I kind of just go through everything that
[00:53:04:080 - 00:53:04:649] **Speaker 0:** you need to know.
[00:53:07:320 - 00:53:09:280] **Speaker 2:** Is there anything you'd suggest if I wanted to go
[00:53:09:280 - 00:53:11:250] **Speaker 2:** a bit further than what we cover in this course?
[00:53:13:979 - 00:53:17:120] **Speaker 1:** In terms of Like what would you like to out
[00:53:17:120 - 00:53:17:739] **Speaker 0:** of it like.
[00:53:19:310 - 00:53:22:320] **Speaker 2:** My primary interest is probably CFD at the moment, so.
[00:53:23:030 - 00:53:27:250] **Speaker 0:** Um, so Yeah, I just do the FG course next
[00:53:27:250 - 00:53:28:489] **Speaker 0:** year intro.
[00:53:30:939 - 00:53:33:830] **Speaker 2:** Are there is there more advanced math that goes into
[00:53:33:830 - 00:53:36:790] **Speaker 2:** that course, or is it just applications of, I mean,
[00:53:36:949 - 00:53:40:239] **Speaker 0:** so he goes through finite volume method, which is the
[00:53:40:239 - 00:53:42:820] **Speaker 0:** 3 case that I that I showed today, um.
[00:53:43:659 - 00:53:44:860] **Speaker 0:** So it's similar sort of maths.
[00:53:45:550 - 00:53:46:229] **Speaker 0:** As the others.
[00:53:46:389 - 00:53:47:949] **Speaker 0:** I mean, it's different, but it's a similar level.
[00:53:49:199 - 00:53:51:189] **Speaker 0:** And then he talks a bit more about turbulence models.
[00:53:53:959 - 00:53:55:090] **Speaker 0:** So you can use ComSoft.
[00:53:57:360 - 00:53:58:870] **Speaker 0:** As well, if you want.
[00:54:01:449 - 00:54:02:600] **Speaker 0:** Yeah, I guess it depends if you want to do
[00:54:02:600 - 00:54:04:040] **Speaker 0:** the math or the simulation side of things.
[00:54:04:899 - 00:54:09:459] **Speaker 2:** The math does interest me, yeah, I guess you just
[00:54:09:459 - 00:54:11:899] **Speaker 2:** find a CFD textbook and yeah.
[00:54:18:000 - 00:54:20:199] **Speaker 0:** Well wait till, wait till next year, um.
[00:54:22:330 - 00:54:23:790] **Speaker 0:** Yeah, if you send me an email I can forward
[00:54:23:790 - 00:54:27:020] **Speaker 0:** you some textbooks or at least the recommended reading that
[00:54:27:020 - 00:54:30:429] **Speaker 0:** Matthew uses, um, but yeah, have a chat with Matthew
[00:54:30:429 - 00:54:31:629] **Speaker 2:** as well, um.
[00:54:32:520 - 00:54:33:610] **Speaker 0:** So his office is down there.
[00:54:36:290 - 00:54:41:100] **Speaker 0:** S Yeah, he's not in today, but All right, sweet,
[00:54:41:149 - 00:54:41:449] **Speaker 2:** thank you.
[00:54:41:979 - 00:54:42:979] **Speaker 2:** Have a good afternoon, you too.

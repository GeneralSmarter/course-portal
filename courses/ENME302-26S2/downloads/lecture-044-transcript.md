# ENME302-26S2 Lecture 44 native Echo transcript

Date: October 9, 2026 11:00am-11:55am
Transcript type: native Echo automated transcript.

[00:01:29:900 - 00:01:31:400] **Speaker 0:** Cool, uh, good morning.
[00:01:32:099 - 00:01:35:709] **Speaker 0:** Hopefully the, the dinner went well last night.
[00:01:36:319 - 00:01:38:800] **Speaker 0:** And we've lost a few people, but that's right.
[00:01:40:150 - 00:01:44:669] **Speaker 0:** Um, Hopefully if you had dinner, it was well cooked
[00:01:44:970 - 00:01:46:690] **Speaker 0:** and you didn't get food poisoning.
[00:01:47:400 - 00:01:49:419] **Speaker 0:** They did some modelling in the back, I don't know.
[00:01:49:800 - 00:01:52:309] **Speaker 0:** Um, so as I said in that post last night,
[00:01:52:639 - 00:01:56:120] **Speaker 0:** we'll just go through some questions that we've received on
[00:01:56:120 - 00:01:56:760] **Speaker 0:** the assignment.
[00:01:58:300 - 00:02:00:360] **Speaker 0:** Because I realise people aren't studying for the exam, but
[00:02:00:540 - 00:02:02:500] **Speaker 0:** in previous years I've really appreciated me going through the
[00:02:02:500 - 00:02:05:680] **Speaker 0:** exam questions during the lectures because there's no really other,
[00:02:06:099 - 00:02:07:930] **Speaker 0:** um, opportunities to go through them.
[00:02:08:160 - 00:02:10:649] **Speaker 0:** So we'll do that next week, and today we'll focus
[00:02:10:649 - 00:02:12:759] **Speaker 0:** on the assignment because that's due, uh, early next week.
[00:02:13:550 - 00:02:17:500] **Speaker 0:** And Printed out the questions and we'll just go through
[00:02:17:500 - 00:02:17:740] **Speaker 0:** them.
[00:02:19:380 - 00:02:20:940] **Speaker 0:** And have a think if you have any other questions,
[00:02:20:979 - 00:02:23:380] **Speaker 0:** we can go through them as well during the lecture.
[00:02:34:589 - 00:02:38:029] **Speaker 0:** So first we're looking at how to get the data
[00:02:38:029 - 00:02:39:009] **Speaker 0:** from the prem suite.
[00:02:39:550 - 00:02:40:229] **Speaker 0:** Can you read?
[00:02:41:259 - 00:02:41:679] **Speaker 0:** So I'm gonna vote.
[00:02:42:869 - 00:02:44:470] **Speaker 0:** How to get data from the parameter sweep and then
[00:02:44:470 - 00:02:47:029] **Speaker 0:** plotting it on a graph, uh, maybe to see what
[00:02:47:029 - 00:02:49:029] **Speaker 0:** you're looking at for the optimisation step.
[00:02:50:070 - 00:02:57:380] **Speaker 0:** And If we go back to lab 3, we're looking
[00:02:57:380 - 00:03:01:860] **Speaker 0:** at those mesh convergence using linear quadratic and cubic shaped
[00:03:01:860 - 00:03:02:419] **Speaker 0:** elements.
[00:03:05:419 - 00:03:08:929] **Speaker 0:** And We wait.
[00:03:09:410 - 00:03:11:619] **Speaker 0:** They went off, maybe they were fixing this before.
[00:03:12:039 - 00:03:15:949] **Speaker 0:** Um, so Here I've got 3.
[00:03:16:800 - 00:03:22:330] **Speaker 0:** Point graphs underneath this line graph node, so under results,
[00:03:22:440 - 00:03:24:960] **Speaker 0:** we can choose which plot groups to have, and here's
[00:03:24:960 - 00:03:29:320] **Speaker 0:** a 1D plot group, And several point graphs underneath and
[00:03:29:320 - 00:03:31:600] **Speaker 0:** it's plotting them on top of each other, so you
[00:03:31:600 - 00:03:34:990] **Speaker 0:** can have multiple child point graphs underneath the parent uh
[00:03:34:990 - 00:03:35:679] **Speaker 0:** plot group.
[00:03:36:690 - 00:03:40:520] **Speaker 0:** And here I've plotted the stress.
[00:03:42:639 - 00:03:47:279] **Speaker 0:** The midpoint at the lower um edge.
[00:03:53:339 - 00:03:55:880] **Speaker 0:** That's how we can put them onto one plot.
[00:03:56:779 - 00:04:01:020] **Speaker 0:** I'm wondering if We had a single value that we
[00:04:01:020 - 00:04:03:160] **Speaker 0:** wanted to plot across multiple entries.
[00:04:03:339 - 00:04:04:979] **Speaker 0:** We can use the global evaluation.
[00:04:06:119 - 00:04:08:130] **Speaker 0:** So global evaluation here we were just looking at the
[00:04:08:130 - 00:04:09:889] **Speaker 0:** number of degrees of freedom, but it might be like
[00:04:09:889 - 00:04:12:169] **Speaker 0:** the final time step or something like that.
[00:04:12:330 - 00:04:14:490] **Speaker 0:** In this case it's stationary, so it doesn't apply, but
[00:04:14:490 - 00:04:15:589] **Speaker 0:** if we have a new table.
[00:04:16:820 - 00:04:21:489] **Speaker 0:** We have our data set, that parametric set for solutions,
[00:04:21:500 - 00:04:22:100] **Speaker 0:** Sol 30.
[00:04:23:649 - 00:04:25:730] **Speaker 0:** I've saved them as multiple uh.
[00:04:27:559 - 00:04:31:510] **Speaker 0:** Solutions Somewhere, solver config.
[00:04:32:049 - 00:04:34:829] **Speaker 0:** So sol 2 is essentially where it's writing to, you
[00:04:34:829 - 00:04:36:049] **Speaker 0:** know, hit compute.
[00:04:36:730 - 00:04:40:410] **Speaker 0:** And then you can save solution copy, and I've done
[00:04:40:410 - 00:04:43:250] **Speaker 0:** that for the linear cubic and quadrate cases, just so
[00:04:43:250 - 00:04:44:769] **Speaker 0:** that I can plot them all in one plot down
[00:04:44:769 - 00:04:44:929] **Speaker 0:** here.
[00:04:45:890 - 00:04:50:700] **Speaker 0:** And We select the dataset that we want to extract
[00:04:50:700 - 00:04:51:220] **Speaker 0:** data from.
[00:04:51:920 - 00:04:54:269] **Speaker 0:** So in this case I might look at linear and
[00:04:54:269 - 00:04:56:910] **Speaker 0:** I've got the number of degrees of freedom plotting against
[00:04:56:910 - 00:05:00:309] **Speaker 0:** our um parameter value that I'm varying in Y.
[00:05:00:750 - 00:05:06:720] **Speaker 0:** If you had two parameters that you're varying, Um You
[00:05:06:720 - 00:05:09:980] **Speaker 0:** have, well, I think if you go into optimise optim
[00:05:09:980 - 00:05:10:709] **Speaker 0:** um.
[00:05:11:769 - 00:05:17:609] **Speaker 0:** optimisation then, I'll, I'll open that chapter 12.
[00:05:18:980 - 00:05:21:220] **Speaker 0:** It's a bit easier to show rather than trying to
[00:05:21:220 - 00:05:22:339] **Speaker 0:** talk about it.
[00:05:25:720 - 00:05:29:809] **Speaker 0:** So here we looked at the Cooling rod and figured
[00:05:29:809 - 00:05:32:369] **Speaker 0:** out when it would hit 50 degrees and we did
[00:05:32:369 - 00:05:33:420] **Speaker 0:** some optimisation.
[00:05:34:230 - 00:05:36:510] **Speaker 0:** And under derived values.
[00:05:37:420 - 00:05:39:109] **Speaker 0:** We can do global evaluation.
[00:05:40:459 - 00:05:43:179] **Speaker 0:** And I don't know what we want to sit.
[00:05:46:540 - 00:05:51:959] **Speaker 0:** Um For argument's sake.
[00:05:53:010 - 00:05:53:989] **Speaker 0:** The temperature.
[00:05:55:510 - 00:05:57:190] **Speaker 0:** At the main point maybe of.
[00:05:57:899 - 00:06:04:670] **Speaker 0:** 1.1T. So we can make that into a new table.
[00:06:05:730 - 00:06:09:170] **Speaker 0:** And it's plotting all of the alpha values over time.
[00:06:09:989 - 00:06:13:929] **Speaker 0:** In this case, I've only got one alpha value, so
[00:06:13:929 - 00:06:14:929] **Speaker 0:** one parameter.
[00:06:15:350 - 00:06:19:549] **Speaker 0:** Under general optimisation, we can save all of the solutions.
[00:06:22:480 - 00:06:22:920] **Speaker 0:** Somewhere.
[00:06:23:700 - 00:06:29:869] **Speaker 0:** Out By default it might only save the last one,
[00:06:29:920 - 00:06:32:260] **Speaker 0:** which is the optimal solution, which makes sense, but you
[00:06:32:260 - 00:06:34:070] **Speaker 0:** might want to save all of them so that you
[00:06:34:070 - 00:06:37:269] **Speaker 0:** can compare and contrast, so maybe we compute again.
[00:06:40:769 - 00:06:42:640] **Speaker 0:** So it's figuring out this 1.11.
[00:06:43:489 - 00:06:44:750] **Speaker 0:** centimetre squared per second.
[00:06:47:339 - 00:06:54:440] **Speaker 0:** Heativity And under global evaluation, Our parameter sweep We can
[00:06:54:440 - 00:06:58:239] **Speaker 0:** choose Which alpha values to to select from.
[00:06:59:380 - 00:07:04:010] **Speaker 0:** Or all of them And the time.
[00:07:06:420 - 00:07:08:989] **Speaker 0:** And now we've got this option of inner solution and
[00:07:08:989 - 00:07:09:540] **Speaker 0:** outer solution.
[00:07:09:589 - 00:07:10:970] **Speaker 0:** So if I just leave it as a default.
[00:07:13:549 - 00:07:16:250] **Speaker 0:** It gets a bit hectic because we're plotting over time
[00:07:16:750 - 00:07:17:929] **Speaker 0:** and those alpha values.
[00:07:19:200 - 00:07:21:720] **Speaker 0:** And if we want to have essentially columns that correspond
[00:07:21:720 - 00:07:24:720] **Speaker 0:** to each, we can change these to the inner solutions.
[00:07:27:299 - 00:07:32:779] **Speaker 0:** To denote or have columns for each time, so 0123
[00:07:32:779 - 00:07:34:549] **Speaker 0:** minutes for each alpha value.
[00:07:35:309 - 00:07:37:899] **Speaker 0:** Or if you want to reverse the columns and rows,
[00:07:37:950 - 00:07:39:109] **Speaker 0:** you'd have the outer.
[00:07:40:769 - 00:07:41:489] **Speaker 0:** a solution.
[00:07:43:140 - 00:07:46:570] **Speaker 0:** So here each row corresponds to a time in the
[00:07:46:570 - 00:07:51:059] **Speaker 0:** simulation, and these are the alpha values for the temperature
[00:07:51:059 - 00:07:51:899] **Speaker 0:** at that midpoint.
[00:07:54:899 - 00:08:03:570] **Speaker 0:** Cause it's covering Both the Time and the optimisation, objective
[00:08:03:570 - 00:08:03:940] **Speaker 0:** function.
[00:08:09:890 - 00:08:12:769] **Speaker 0:** Is that, has anyone got a question on that sort
[00:08:12:769 - 00:08:13:510] **Speaker 0:** of workflow?
[00:08:14:880 - 00:08:21:829] **Speaker 0:** Sure T Give me the best Yeah, you could plot
[00:08:21:829 - 00:08:28:510] **Speaker 0:** tea cooked versus tea flipped, for example, um, because I'll
[00:08:28:510 - 00:08:30:149] **Speaker 0:** get a spare piece of paper.
[00:08:32:210 - 00:08:34:210] **Speaker 0:** Actually, I have chapter 12.
[00:08:34:950 - 00:08:36:229] **Speaker 0:** I have all the chapters with me.
[00:08:37:119 - 00:08:37:960] **Speaker 0:** That we went through.
[00:08:42:008 - 00:08:45:098] **Speaker 0:** Chapter 12 we look at these different objective functions and
[00:08:45:098 - 00:08:48:539] **Speaker 0:** all we're plotting is our objective function against the control
[00:08:48:539 - 00:08:48:939] **Speaker 0:** variable.
[00:08:49:098 - 00:08:52:499] **Speaker 0:** Control variable is def, objective function is dcooked.
[00:08:53:479 - 00:08:55:039] **Speaker 0:** So you can think of it as these, we don't
[00:08:55:039 - 00:08:57:429] **Speaker 0:** know what the curve looks like yet, and that's why
[00:08:57:429 - 00:08:59:739] **Speaker 0:** you do your parameter sweep to explore the parameter space.
[00:09:00:690 - 00:09:03:289] **Speaker 0:** Once you figure out what interval would make sense to
[00:09:03:289 - 00:09:05:349] **Speaker 0:** start with, that's where you can start your optimizer.
[00:09:13:000 - 00:09:17:200] **Speaker 0:** And saving the data for each uh optimisation allows you
[00:09:17:200 - 00:09:17:840] **Speaker 0:** to plot that.
[00:09:18:659 - 00:09:19:650] **Speaker 0:** Um, on here.
[00:09:19:940 - 00:09:23:700] **Speaker 0:** Uh, although In the objective function table.
[00:09:29:010 - 00:09:31:450] **Speaker 0:** It's also recording that, so you can just plot directly
[00:09:31:450 - 00:09:32:140] **Speaker 0:** here with this.
[00:09:32:880 - 00:09:33:539] **Speaker 0:** Table graph.
[00:09:35:169 - 00:09:42:890] **Speaker 0:** Um, Which looks a little bit funky, but essentially this
[00:09:42:890 - 00:09:49:909] **Speaker 0:** is the, Objective function as a function of The control
[00:09:49:909 - 00:09:52:349] **Speaker 0:** variable, which in this case was alpha, if we set
[00:09:52:349 - 00:09:53:469] **Speaker 0:** it to.
[00:09:54:400 - 00:09:56:679] **Speaker 0:** No lying and just have it with markers.
[00:09:57:940 - 00:10:00:289] **Speaker 0:** It sort of makes a bit more sense.
[00:10:00:570 - 00:10:01:799] **Speaker 0:** So there's minimums down here.
[00:10:02:659 - 00:10:05:460] **Speaker 0:** Um, and this is sort of the space that it
[00:10:05:460 - 00:10:06:119] **Speaker 0:** explored.
[00:10:09:760 - 00:10:12:330] **Speaker 0:** So the reason that the lines were quite confusing is
[00:10:12:330 - 00:10:15:469] **Speaker 0:** because, Whatever method we're using.
[00:10:19:710 - 00:10:24:989] **Speaker 0:** Bobby Carr, so bound optimisation by quadratic approximation is essentially
[00:10:24:989 - 00:10:28:750] **Speaker 0:** searching the objective function space with quadratic interpretation and then
[00:10:29:109 - 00:10:30:789] **Speaker 0:** is is fitting to that minima.
[00:10:31:630 - 00:10:33:760] **Speaker 0:** So it probably starts up here, explores this way and
[00:10:33:760 - 00:10:36:840] **Speaker 0:** this way, fits a quadratic, goes over here and sort
[00:10:36:840 - 00:10:39:020] **Speaker 0:** of repeats that process until it reaches that minimum.
[00:10:54:710 - 00:10:59:309] **Speaker 0:** Calculating heat fluxes in Python, so heat flux.
[00:11:02:479 - 00:11:16:849] **Speaker 0:** Is defined, Using Foyer's law.
[00:11:17:750 - 00:11:20:669] **Speaker 0:** So in your Python code you've solved for the temperature
[00:11:20:669 - 00:11:22:270] **Speaker 0:** distribution throughout the patty.
[00:11:22:669 - 00:11:24:989] **Speaker 0:** You've got temperature values at each nodal point, including on
[00:11:24:989 - 00:11:26:260] **Speaker 0:** the boundaries and adjacent.
[00:11:27:109 - 00:11:29:590] **Speaker 0:** So you can evaluate the heat flux queue.
[00:11:30:450 - 00:11:35:799] **Speaker 0:** Uh, but Minus thermal conductivityk or kappa in the assignment
[00:11:35:799 - 00:11:39:200] **Speaker 0:** multiplied by the temperature gradient at the interface, so we
[00:11:39:200 - 00:11:52:479] **Speaker 0:** had, And the left hand boundary, then.
[00:11:53:280 - 00:11:53:489] **Speaker 0:** Q.
[00:11:55:489 - 00:11:59:239] **Speaker 0:** X is minus K D D Y D X.
[00:12:01:859 - 00:12:04:799] **Speaker 0:** And you can evaluate that derivative eT by DX with
[00:12:05:799 - 00:12:06:539] **Speaker 0:** finite differencing.
[00:12:06:739 - 00:12:08:260] **Speaker 0:** So you can do a one-sided difference.
[00:12:10:349 - 00:12:13:270] **Speaker 0:** By taking the temperature values at 1 + 1 and
[00:12:13:270 - 00:12:14:950] **Speaker 0:** I divided by delta X.
[00:12:20:729 - 00:12:22:630] **Speaker 0:** The example we did in class.
[00:12:26:659 - 00:12:27:619] **Speaker 0:** Was.
[00:12:29:719 - 00:12:30:770] **Speaker 0:** Using gradient.
[00:12:32:909 - 00:12:36:869] **Speaker 0:** Which will do The gradient, and we use this for
[00:12:36:869 - 00:12:37:909] **Speaker 0:** plotting the quivers.
[00:12:44:489 - 00:12:49:080] **Speaker 0:** These arrowheads Um, but I think at least for the
[00:12:49:080 - 00:12:52:049] **Speaker 0:** assignment, we'll just, just use this because we know that
[00:12:52:049 - 00:12:54:289] **Speaker 0:** it's going to be applied at the boundary condition.
[00:12:55:250 - 00:12:56:130] **Speaker 0:** At the boundaries rather.
[00:13:01:520 - 00:13:01:799] **Speaker 0:** Cool.
[00:13:04:489 - 00:13:06:000] **Speaker 0:** Uh, mesh convergence.
[00:13:09:979 - 00:13:10:049] **Speaker 0:** Pop.
[00:13:11:809 - 00:13:13:130] **Speaker 0:** 1 and 2.
[00:13:14:989 - 00:13:18:010] **Speaker 0:** So part one is the plain R2D case with Python
[00:13:18:010 - 00:13:19:510] **Speaker 0:** and a little bit with console just to check that
[00:13:19:510 - 00:13:21:809] **Speaker 0:** you've got the right answer, so you don't ask me.
[00:13:22:109 - 00:13:24:630] **Speaker 0:** Um, and then part two we've got the full 3
[00:13:24:630 - 00:13:25:549] **Speaker 0:** square patty.
[00:13:26:340 - 00:13:28:619] **Speaker 0:** So there might, there might be different solutions, and we
[00:13:28:619 - 00:13:32:539] **Speaker 0:** want to ensure that our numerical solution is converged in
[00:13:32:539 - 00:13:35:039] **Speaker 0:** our spatial discretization and temporal.
[00:13:36:559 - 00:13:38:429] **Speaker 0:** So it's showing mesh convergence.
[00:13:42:770 - 00:13:45:450] **Speaker 0:** I've generally asked for like the minimum temperature over time
[00:13:45:450 - 00:13:47:960] **Speaker 0:** because that's the critical uh value that we're interested in.
[00:13:48:049 - 00:13:49:789] **Speaker 0:** We want to make sure that it's a safe temperature
[00:13:49:789 - 00:13:50:169] **Speaker 0:** to eat.
[00:13:51:130 - 00:13:54:549] **Speaker 0:** So using mesh convergence on this value make sense.
[00:13:56:260 - 00:13:58:190] **Speaker 0:** Some of you have pointed out that it's quite hard
[00:13:58:190 - 00:13:59:489] **Speaker 0:** to see between.
[00:14:00:489 - 00:14:04:520] **Speaker 0:** Lines that are overlapping, so if they are overlapping values,
[00:14:05:010 - 00:14:07:530] **Speaker 0:** it's quite hard to see those.
[00:14:07:890 - 00:14:11:789] **Speaker 0:** So you could maybe zoom in and then expand out.
[00:14:12:679 - 00:14:14:700] **Speaker 0:** That would be one way of showing that.
[00:14:16:119 - 00:14:16:890] **Speaker 0:** Closeness.
[00:14:17:320 - 00:14:19:539] **Speaker 0:** This is a more qualitative approach.
[00:14:20:469 - 00:14:23:309] **Speaker 0:** The techniques that we discussed in class is trying to
[00:14:23:309 - 00:14:26:349] **Speaker 0:** pick a value in space and time, and compare them
[00:14:26:349 - 00:14:28:609] **Speaker 0:** directly, so it would be just like a line plot
[00:14:29:190 - 00:14:35:659] **Speaker 0:** of, Value of interest At a particular point in space
[00:14:35:659 - 00:14:36:559] **Speaker 0:** and time.
[00:14:37:450 - 00:14:39:690] **Speaker 0:** And look at that over the number of degrees of
[00:14:39:690 - 00:14:41:809] **Speaker 0:** freedom or the number of mesh elements or however you
[00:14:41:809 - 00:14:44:369] **Speaker 0:** set your mesh convergence study.
[00:14:46:390 - 00:14:48:479] **Speaker 0:** So other approaches are valid.
[00:14:49:099 - 00:14:52:020] **Speaker 0:** So that's T and over time.
[00:14:52:739 - 00:14:55:780] **Speaker 0:** We already need to plot this, as we've asked for
[00:14:55:780 - 00:14:57:179] **Speaker 0:** that, um.
[00:14:58:450 - 00:15:01:099] **Speaker 0:** You can also introduce this, the 2nd mesh as well,
[00:15:01:520 - 00:15:03:599] **Speaker 0:** 2nd mesh study uh figure as well.
[00:15:04:760 - 00:15:06:359] **Speaker 0:** For part two.
[00:15:09:270 - 00:15:09:960] **Speaker 0:** News.
[00:15:13:840 - 00:15:16:359] **Speaker 0:** So you need to, yeah, I guess, decide how you
[00:15:16:359 - 00:15:17:030] **Speaker 0:** want to evaluate this.
[00:15:17:080 - 00:15:19:799] **Speaker 0:** So you might choose the second option of just evaluating
[00:15:19:799 - 00:15:22:460] **Speaker 0:** the temperature at a fixed point in space and time.
[00:15:23:919 - 00:15:27:950] **Speaker 0:** Generally taking T min or the minimum value within a
[00:15:27:950 - 00:15:30:719] **Speaker 0:** domain is a little bit dangerous when you're using interpolation
[00:15:31:320 - 00:15:34:380] **Speaker 0:** because it might vary, like the minimum location might change
[00:15:34:679 - 00:15:35:739] **Speaker 0:** as you refine the mesh.
[00:15:36:580 - 00:15:39:419] **Speaker 0:** So you're not directly comparing like for like between mesh
[00:15:39:419 - 00:15:40:159] **Speaker 0:** resolutions.
[00:15:42:000 - 00:15:43:809] **Speaker 0:** If you think back to some of those examples with
[00:15:43:809 - 00:15:47:890] **Speaker 0:** the solid mechanics, and we have really high stress concentrations,
[00:15:48:010 - 00:15:51:729] **Speaker 0:** if we took the highest stress throughout the domain, it
[00:15:51:729 - 00:15:53:710] **Speaker 0:** would just keep increasing as we refine the mesh.
[00:15:55:599 - 00:15:59:280] **Speaker 0:** So generally we stick with keeping with dependent variable.
[00:15:59:590 - 00:16:01:539] **Speaker 0:** In this case, it's the temperature and then at a
[00:16:01:539 - 00:16:02:429] **Speaker 0:** fixed point in space.
[00:16:02:590 - 00:16:05:390] **Speaker 0:** So either using a point or something like that.
[00:16:07:750 - 00:16:12:179] **Speaker 0:** So you might find that it has not very much
[00:16:12:179 - 00:16:13:489] **Speaker 0:** difference between each mesh.
[00:16:15:900 - 00:16:21:140] **Speaker 0:** Uh Change as you resolve the mesh, so that's fine.
[00:16:21:260 - 00:16:23:260] **Speaker 0:** I mean the heat equation, it's not super exciting, it
[00:16:23:260 - 00:16:27:369] **Speaker 0:** doesn't have, That nonlinear behaviour, uh, you just need to
[00:16:27:369 - 00:16:30:869] **Speaker 0:** demonstrate that it has converged, so it's no longer changing
[00:16:30:869 - 00:16:32:140] **Speaker 0:** as you refine the niche.
[00:16:34:070 - 00:16:36:549] **Speaker 0:** And discussing your meshing strategy, did you use an unstructured
[00:16:36:549 - 00:16:36:799] **Speaker 0:** mesh?
[00:16:36:869 - 00:16:37:700] **Speaker 0:** Did you use structured?
[00:16:37:780 - 00:16:39:869] **Speaker 0:** How did you create the mesh, uh, that sort of
[00:16:39:869 - 00:16:40:109] **Speaker 0:** thing.
[00:16:42:219 - 00:16:48:460] **Speaker 0:** It's the easiest way to What Numbers and degrees of
[00:16:49:510 - 00:16:56:570] **Speaker 0:** So Yeah So if you think back to the wrench.
[00:16:57:520 - 00:16:58:950] **Speaker 0:** Oh, I have to connect again.
[00:16:59:840 - 00:17:02:440] **Speaker 0:** Um, so eventually we had, I think they call it
[00:17:02:440 - 00:17:07:449] **Speaker 0:** like HD or something, LDHD, and, We will find that,
[00:17:07:489 - 00:17:09:890] **Speaker 0:** I think that was scaling the minimum or maximum element
[00:17:09:890 - 00:17:15:219] **Speaker 0:** size, I think probably maximum element size and, That was
[00:17:15:219 - 00:17:15:780] **Speaker 0:** the wrench.
[00:17:15:900 - 00:17:17:280] **Speaker 0:** So that was an unstructured mesh.
[00:17:17:619 - 00:17:18:719] **Speaker 0:** For the structured mesh.
[00:17:23:359 - 00:17:25:000] **Speaker 0:** I have to reconnect it to.
[00:17:26:680 - 00:17:27:479] **Speaker 0:** Resolution.
[00:17:35:140 - 00:17:38:380] **Speaker 0:** So that was chapter 12, so we.
[00:17:40:089 - 00:17:40:829] **Speaker 0:** Chapter 3.
[00:17:47:020 - 00:17:49:300] **Speaker 0:** This was pretty much like the master class of mesh
[00:17:49:300 - 00:17:51:260] **Speaker 0:** mesh convergence and discretization.
[00:17:51:829 - 00:17:55:459] **Speaker 0:** So we had a parameter sweep on NY where NY
[00:17:55:459 - 00:17:59:020] **Speaker 0:** was the number of elements in the Y direction.
[00:18:00:130 - 00:18:01:969] **Speaker 0:** So we set the number, well, first of all we
[00:18:01:969 - 00:18:03:849] **Speaker 0:** had a map mesh because it's a nice rectangular grid.
[00:18:03:930 - 00:18:06:729] **Speaker 0:** Max needs to use a map mesh, structured grid, and
[00:18:06:729 - 00:18:09:829] **Speaker 0:** we've got a set number of elements in the vertical
[00:18:09:829 - 00:18:11:369] **Speaker 0:** direction with NY.
[00:18:12:300 - 00:18:15:469] **Speaker 0:** And we also need to enforce the number of elements
[00:18:15:469 - 00:18:18:660] **Speaker 0:** in X as we refine Y, um, number of elements,
[00:18:18:670 - 00:18:20:510] **Speaker 0:** we want to increase the number of X elements.
[00:18:21:380 - 00:18:26:510] **Speaker 0:** So Um, linked or coupled that by setting it to
[00:18:26:510 - 00:18:27:439] **Speaker 0:** be 2 NY.
[00:18:28:969 - 00:18:30:390] **Speaker 0:** This formed rectangular elements.
[00:18:30:439 - 00:18:32:560] **Speaker 0:** If we wanted square ones, we'd have to figure out
[00:18:32:560 - 00:18:35:520] **Speaker 0:** the length and height ratio and have that as a
[00:18:35:520 - 00:18:36:160] **Speaker 0:** suitable value.
[00:18:38:180 - 00:18:42:140] **Speaker 0:** Um, but ultimately, you want to have one parameter that
[00:18:42:140 - 00:18:44:180] **Speaker 0:** is driving the mesh generation.
[00:18:44:900 - 00:18:47:060] **Speaker 0:** And then refining that with your parameter suite.
[00:18:47:849 - 00:18:50:030] **Speaker 0:** So that's your parametric sweep and you can just plot
[00:18:50:329 - 00:18:55:050] **Speaker 0:** uh some particular value of interest against your mesh resolution.
[00:18:56:459 - 00:18:58:459] **Speaker 0:** So whether it's a number of degrees of freedom or
[00:18:58:459 - 00:19:04:239] **Speaker 0:** in number of elements Doesn't matter too much, they all
[00:19:04:239 - 00:19:04:900] **Speaker 0:** scale.
[00:19:05:660 - 00:19:10:109] **Speaker 0:** I think linearly The degrees of freedom is related to
[00:19:10:109 - 00:19:12:229] **Speaker 0:** like those number of equations that we're solving with that
[00:19:12:229 - 00:19:14:819] **Speaker 0:** big system of equations, and that depends on which physics
[00:19:14:819 - 00:19:15:569] **Speaker 0:** we're solving for.
[00:19:16:640 - 00:19:19:359] **Speaker 0:** And how many unknowns there are for each node.
[00:19:23:180 - 00:19:23:859] **Speaker 0:** think the same.
[00:19:25:189 - 00:19:26:890] **Speaker 0:** 3D Yes.
[00:19:28:150 - 00:19:31:630] **Speaker 0:** So the swift I don't think it'll even let, I
[00:19:31:630 - 00:19:33:719] **Speaker 0:** don't know if it'll let me do that, but um
[00:19:33:719 - 00:19:36:560] **Speaker 0:** there's a sweet option to do it in the other
[00:19:36:560 - 00:19:36:959] **Speaker 0:** direction.
[00:19:37:810 - 00:19:40:479] **Speaker 0:** So you can couple that with the the end scaling
[00:19:40:479 - 00:19:40:849] **Speaker 0:** as well.
[00:19:52:699 - 00:19:54:930] **Speaker 0:** To improve the model, yeah well I mean when I
[00:19:54:930 - 00:19:57:229] **Speaker 0:** was writing the assignment I was like oh, I I'll
[00:19:57:229 - 00:20:00:170] **Speaker 0:** just leave it up to you entirely, but um.
[00:20:01:800 - 00:20:03:900] **Speaker 0:** I was talking to one of the TAs and thought
[00:20:03:900 - 00:20:04:699] **Speaker 0:** that would be a little bit.
[00:20:05:420 - 00:20:06:680] **Speaker 0:** Difficult for the course.
[00:20:07:099 - 00:20:10:900] **Speaker 0:** So I've tried to be quite specific of what, of
[00:20:10:900 - 00:20:11:819] **Speaker 0:** what you're improving.
[00:20:12:099 - 00:20:14:959] **Speaker 0:** So several, we made some assumptions.
[00:20:16:060 - 00:20:18:699] **Speaker 0:** And we're going to improve on our axis symmetric 2D
[00:20:18:939 - 00:20:19:479] **Speaker 0:** patty.
[00:20:20:609 - 00:20:22:170] **Speaker 0:** So you're gonna include the frying pan.
[00:20:23:270 - 00:20:25:310] **Speaker 0:** So at the moment you're just setting the boundary condition
[00:20:25:310 - 00:20:28:979] **Speaker 0:** at the base of the patty, but That's not as
[00:20:28:979 - 00:20:29:599] **Speaker 0:** realistic.
[00:20:30:510 - 00:20:32:589] **Speaker 0:** And we've also got air that surrounds the patty rather
[00:20:32:589 - 00:20:36:229] **Speaker 0:** than just the convection boundary congestion that we impose with
[00:20:36:229 - 00:20:37:520] **Speaker 0:** a pretty arbitrary H value.
[00:20:38:729 - 00:20:40:520] **Speaker 0:** So I want you to use the heat transfer in
[00:20:40:520 - 00:20:41:469] **Speaker 0:** solids and fluids.
[00:20:42:000 - 00:20:44:819] **Speaker 0:** The fluids part will denote the air, the surrounding air,
[00:20:45:239 - 00:20:47:079] **Speaker 0:** and then the solid for the patty and the pan.
[00:20:48:569 - 00:20:52:160] **Speaker 0:** So some of you have looked at Essentially modelling the
[00:20:52:160 - 00:20:56:760] **Speaker 0:** ventilation above the cooktop, which is cool, but if, if
[00:20:56:760 - 00:20:59:839] **Speaker 0:** you just assume static air, so no velocity, you'll still
[00:20:59:839 - 00:21:01:239] **Speaker 0:** get full marks for this question.
[00:21:01:680 - 00:21:03:680] **Speaker 0:** It's really just adding in the pan.
[00:21:04:900 - 00:21:06:939] **Speaker 0:** Ah, and the surrounding air, so you have to make
[00:21:06:939 - 00:21:11:060] **Speaker 0:** some design decisions around what size pan, what shape, how
[00:21:11:060 - 00:21:13:469] **Speaker 0:** much air domain should you include and things like that,
[00:21:13:989 - 00:21:18:160] **Speaker 0:** and that's where we ask you to describe your methods
[00:21:18:380 - 00:21:20:180] **Speaker 0:** and providing some some results.
[00:21:28:680 - 00:21:29:709] **Speaker 0:** How do you model the air?
[00:21:32:500 - 00:21:39:670] **Speaker 0:** So, this, We, OK, I'll just use this model, um.
[00:21:40:489 - 00:21:46:729] **Speaker 0:** So physics I want to add Heat transfer in solids
[00:21:46:729 - 00:21:47:689] **Speaker 0:** and fluids.
[00:21:52:199 - 00:21:56:790] **Speaker 0:** So you've got solid And fluid domains, so you just
[00:21:56:790 - 00:21:57:609] **Speaker 0:** choose which.
[00:21:58:650 - 00:22:02:530] **Speaker 0:** Domain corresponds to which fluid or solid material.
[00:22:03:819 - 00:22:06:550] **Speaker 0:** Um, so if we select this one as a fluid,
[00:22:06:829 - 00:22:10:469] **Speaker 0:** then it can't be solid, so it's overridden, um, and
[00:22:10:469 - 00:22:12:189] **Speaker 0:** then you've got these properties.
[00:22:13:010 - 00:22:15:209] **Speaker 0:** That you can set, so you can use the materials
[00:22:15:209 - 00:22:18:219] **Speaker 0:** and we've done that mostly for our labs and things,
[00:22:18:619 - 00:22:20:609] **Speaker 0:** but you can just set them, sort of hard code
[00:22:20:609 - 00:22:24:290] **Speaker 0:** them down here, so use a defined, Chuck some variables
[00:22:24:290 - 00:22:24:589] **Speaker 0:** here.
[00:22:26:439 - 00:22:29:270] **Speaker 0:** So your material properties for your pan and your patty
[00:22:29:270 - 00:22:29:939] **Speaker 0:** might be different.
[00:22:30:400 - 00:22:32:050] **Speaker 0:** So maybe use the materials for that.
[00:22:32:959 - 00:22:36:079] **Speaker 0:** The fluid, you can have material properties for air, I
[00:22:36:079 - 00:22:37:280] **Speaker 0:** think that's probably an inbuilt one.
[00:22:38:640 - 00:22:39:839] **Speaker 0:** Or you can sit.
[00:22:41:729 - 00:22:43:040] **Speaker 0:** Yeah, set different types here.
[00:22:44:540 - 00:22:45:630] **Speaker 0:** So this is the velocity field.
[00:22:45:750 - 00:22:50:130] **Speaker 0:** If you had a Like laminar flow or some other
[00:22:50:130 - 00:22:53:089] **Speaker 0:** sort of fluid phase that you're modelling, you can hook
[00:22:53:089 - 00:22:57:280] **Speaker 0:** it into uh this space, so it's all about the
[00:22:57:369 - 00:23:02:260] **Speaker 0:** heat convection, the convection part is, What's driving uh from
[00:23:02:260 - 00:23:02:770] **Speaker 0:** the flow.
[00:23:04:680 - 00:23:06:800] **Speaker 0:** So U is the velocity field.
[00:23:08:300 - 00:23:11:130] **Speaker 0:** By default, that's just 0, and that's fine, so that's
[00:23:11:130 - 00:23:13:959] **Speaker 0:** assuming that there's no flow above the pan.
[00:23:15:199 - 00:23:17:550] **Speaker 0:** But you can change that to link to a fluid
[00:23:17:550 - 00:23:20:400] **Speaker 0:** phase, maybe I'll just do that, fluid flow.
[00:23:22:160 - 00:23:23:319] **Speaker 0:** Single M&I.
[00:23:26:890 - 00:23:30:209] **Speaker 0:** So again, this is beyond the scope of this assignment,
[00:23:30:290 - 00:23:33:089] **Speaker 0:** but if you want, you can look into this and
[00:23:35:260 - 00:23:35:780] **Speaker 0:** Where are we?
[00:23:40:609 - 00:23:42:569] **Speaker 0:** Velocity Field is is now here.
[00:23:48:290 - 00:23:51:329] **Speaker 0:** So changing the scale of the graph in the past
[00:23:51:329 - 00:23:52:069] **Speaker 0:** lecture.
[00:23:56:150 - 00:24:01:180] **Speaker 0:** So You, when comparing values from console and Python, it
[00:24:01:180 - 00:24:03:339] **Speaker 0:** might be easier to export values from console and then
[00:24:03:339 - 00:24:04:619] **Speaker 0:** plot it in Python, up to you.
[00:24:06:089 - 00:24:11:209] **Speaker 0:** The One of the methods I showed was scaling by
[00:24:11:209 - 00:24:13:270] **Speaker 0:** some values, so you just divide it by 10 or
[00:24:13:270 - 00:24:14:550] **Speaker 0:** 100, etc.
[00:24:15:270 - 00:24:17:469] **Speaker 0:** If you wanted to plot it in console, you can
[00:24:17:469 - 00:24:19:430] **Speaker 0:** do the same down here.
[00:24:19:550 - 00:24:21:670] **Speaker 0:** You've got your expression and just divide it by some
[00:24:21:670 - 00:24:23:550] **Speaker 0:** value like 100 or or whatever.
[00:24:24:349 - 00:24:25:989] **Speaker 0:** But if you do that, then you need to make
[00:24:25:989 - 00:24:27:069] **Speaker 0:** sure that your legend.
[00:24:27:989 - 00:24:30:040] **Speaker 0:** That corresponds to that line.
[00:24:32:109 - 00:24:36:650] **Speaker 0:** is now Like over 100.
[00:24:37:689 - 00:24:40:030] **Speaker 0:** So that the reader knows what, what value it is.
[00:24:43:979 - 00:24:45:939] **Speaker 0:** And then, yeah, yesterday, um.
[00:24:46:760 - 00:24:50:219] **Speaker 0:** Some of you are using, SI log, which I think
[00:24:50:219 - 00:24:52:260] **Speaker 0:** is like symmetric log, which I've not seen before, which
[00:24:52:260 - 00:24:52:920] **Speaker 0:** is quite cool.
[00:24:53:420 - 00:24:56:459] **Speaker 0:** Um, so you've got like positive and negative values, which
[00:24:56:459 - 00:24:58:979] **Speaker 0:** doesn't really make sense for log scales, but that's a
[00:24:58:979 - 00:25:02:060] **Speaker 0:** way of representing that or taking the absolute value and
[00:25:02:060 - 00:25:03:760] **Speaker 0:** just noting that in the report.
[00:25:05:199 - 00:25:07:479] **Speaker 0:** So don't get too, too hung up on that.
[00:25:08:449 - 00:25:10:689] **Speaker 0:** General tips for generating plots.
[00:25:11:739 - 00:25:14:119] **Speaker 0:** And editing axes.
[00:25:15:219 - 00:25:16:739] **Speaker 0:** So, I mean, this is a good example.
[00:25:16:810 - 00:25:18:920] **Speaker 0:** We've got a lot going on in this title.
[00:25:19:380 - 00:25:22:260] **Speaker 0:** Generally in reports, we, I guess we haven't really gone
[00:25:22:260 - 00:25:24:180] **Speaker 0:** through this, but you've got like a figure caption like
[00:25:24:180 - 00:25:25:660] **Speaker 0:** figure one, and then you've got a caption.
[00:25:26:349 - 00:25:28:050] **Speaker 0:** It's very rare that you actually have a title in
[00:25:28:050 - 00:25:30:550] **Speaker 0:** the figure, so it's best just not to include it.
[00:25:31:810 - 00:25:34:050] **Speaker 0:** Um, and just include it in your caption, so under
[00:25:34:050 - 00:25:37:310] **Speaker 0:** title, title type, none, removes that.
[00:25:38:020 - 00:25:41:140] **Speaker 0:** And you can set x and y axis labels to
[00:25:41:140 - 00:25:41:479] **Speaker 0:** be.
[00:25:43:369 - 00:25:44:939] **Speaker 0:** Stuff, I don't know, custom.
[00:25:48:819 - 00:25:50:819] **Speaker 0:** And remember, when you're exporting.
[00:25:51:560 - 00:25:53:140] **Speaker 0:** You can take the image snapshot.
[00:25:55:339 - 00:25:58:670] **Speaker 0:** And adjust the resolution and the font size.
[00:25:59:150 - 00:26:01:550] **Speaker 0:** So, again, you want the reader to be able to
[00:26:01:550 - 00:26:04:150] **Speaker 0:** see what, what you've written on the figure.
[00:26:04:989 - 00:26:06:479] **Speaker 0:** So having a large enough font size so you can
[00:26:06:479 - 00:26:06:959] **Speaker 0:** read it.
[00:26:07:680 - 00:26:10:439] **Speaker 0:** And you can adjust the resolution there as well and
[00:26:10:439 - 00:26:12:760] **Speaker 0:** also the the DPI dot dots per inch.
[00:26:18:750 - 00:26:23:670] **Speaker 0:** Yeah Again, you might want to export to Python Z.
[00:26:24:579 - 00:26:26:380] **Speaker 0:** I don't think we really use Excel very much.
[00:26:26:500 - 00:26:29:150] **Speaker 0:** I know Cape really likes Excel, but that's another option
[00:26:29:150 - 00:26:30:680] **Speaker 0:** if you're particularly stuck.
[00:26:36:630 - 00:26:38:550] **Speaker 0:** Mesh convergence for part two.
[00:26:47:439 - 00:26:48:949] **Speaker 0:** So, oh yeah, we did mention the word part part
[00:26:49:540 - 00:26:50:380] **Speaker 0:** part two earlier.
[00:26:51:729 - 00:26:53:719] **Speaker 0:** Deflip boundary conditions.
[00:26:57:750 - 00:27:00:550] **Speaker 0:** So some of you have used like study steps, and
[00:27:00:550 - 00:27:01:949] **Speaker 0:** I think some of you got it to work and
[00:27:01:949 - 00:27:03:390] **Speaker 0:** some of you are struggling with that yesterday.
[00:27:03:670 - 00:27:06:310] **Speaker 0:** I've not used that approach, but if it works, good
[00:27:06:310 - 00:27:06:770] **Speaker 0:** on you.
[00:27:06:989 - 00:27:15:130] **Speaker 0:** Um, what I've shown in class is from Chapter 5.
[00:27:19:410 - 00:27:29:420] **Speaker 0:** And essentially we're forcing The H value or the convective
[00:27:29:420 - 00:27:30:180] **Speaker 0:** heat transfer.
[00:27:32:500 - 00:27:33:329] **Speaker 0:** Coefficient.
[00:27:33:739 - 00:27:37:859] **Speaker 0:** If H is very large, the influence of this left-hand
[00:27:37:859 - 00:27:41:619] **Speaker 0:** side is very small and it essentially sets the temperature
[00:27:41:619 - 00:27:43:839] **Speaker 0:** to be the prescribed temperature that surrounds it.
[00:27:45:239 - 00:27:48:560] **Speaker 0:** So that's what I showed earlier this week with these
[00:27:48:560 - 00:27:49:660] **Speaker 0:** boundary fluxes.
[00:27:51:300 - 00:27:53:500] **Speaker 0:** And if you want to have that linked into the
[00:27:53:500 - 00:27:55:739] **Speaker 0:** time, you could do this.
[00:27:57:500 - 00:27:58:849] **Speaker 0:** T is less than tea.
[00:27:59:910 - 00:28:01:949] **Speaker 0:** Flip or whatever, you do this.
[00:28:03:239 - 00:28:05:000] **Speaker 0:** Else it does something else.
[00:28:06:520 - 00:28:08:660] **Speaker 0:** So you can do if statements within these expressions, which
[00:28:08:660 - 00:28:09:160] **Speaker 0:** is pretty cool.
[00:28:16:780 - 00:28:19:180] **Speaker 0:** Uh, and that's the way that I, I've, I've suggested
[00:28:19:180 - 00:28:19:959] **Speaker 0:** to approach it.
[00:28:20:339 - 00:28:22:930] **Speaker 0:** I think the study set, Should work.
[00:28:22:979 - 00:28:25:099] **Speaker 0:** It's just a bit tricky to get values from the
[00:28:25:099 - 00:28:26:420] **Speaker 0:** earlier studies, I think.
[00:28:28:099 - 00:28:29:609] **Speaker 0:** I've not had time to investigate.
[00:28:30:699 - 00:28:32:510] **Speaker 0:** So applying the optimisation study.
[00:28:39:189 - 00:28:41:150] **Speaker 0:** That's chapter 12 demo.
[00:28:43:930 - 00:28:46:109] **Speaker 0:** And I'll just briefly go through what we did here.
[00:28:48:719 - 00:28:50:660] **Speaker 0:** So we've got a.
[00:28:51:500 - 00:28:53:319] **Speaker 0:** Non-local coupling that we defined earlier.
[00:28:53:780 - 00:28:55:579] **Speaker 0:** In this case, I'm just looking at a single value,
[00:28:55:699 - 00:28:58:219] **Speaker 0:** so it's pretty arbitrary which one I select, but non-local
[00:28:58:219 - 00:29:01:010] **Speaker 0:** couplings allows you to integrate, take the average or take
[00:29:01:010 - 00:29:03:400] **Speaker 0:** a maximum value within the prescribed space.
[00:29:04:359 - 00:29:06:319] **Speaker 0:** If it was of a point, it's going to return
[00:29:06:319 - 00:29:07:400] **Speaker 0:** the same value for each.
[00:29:08:430 - 00:29:11:839] **Speaker 0:** So I've chosen the average operator at the midpoint, and
[00:29:11:839 - 00:29:14:859] **Speaker 0:** then I'm calling that in my optimisation study.
[00:29:15:339 - 00:29:16:640] **Speaker 0:** So it's my objective function.
[00:29:19:040 - 00:29:22:810] **Speaker 0:** We are calling comp 1 because it's from component 1.
[00:29:23:469 - 00:29:27:160] **Speaker 0:** op and evaluating the temperature at this midpoint node.
[00:29:27:930 - 00:29:33:989] **Speaker 0:** Subtracting off our target temperature of 50 and squaring it
[00:29:33:989 - 00:29:38:069] **Speaker 0:** to have essentially quadratic loss or objective.
[00:29:38:729 - 00:29:40:560] **Speaker 0:** And it's being evaluated at some point in time.
[00:29:41:489 - 00:29:44:869] **Speaker 0:** So for your case, Um, we've got this handy note
[00:29:44:869 - 00:29:45:150] **Speaker 0:** above.
[00:29:45:270 - 00:29:47:589] **Speaker 0:** The objective is only evaluated at the final time.
[00:29:47:949 - 00:29:53:189] **Speaker 0:** So if your cooking time goes until, well, if your
[00:29:53:189 - 00:29:56:680] **Speaker 0:** solver goes until it's fully cooked, Then you can just
[00:29:56:680 - 00:29:59:780] **Speaker 0:** leave T as your objective function.
[00:30:02:530 - 00:30:04:449] **Speaker 0:** Because you're trying to minimise tea.
[00:30:05:709 - 00:30:06:030] **Speaker 0:** Cooked.
[00:30:07:400 - 00:30:09:969] **Speaker 0:** And tea is equal to tea cooked and it's cooked.
[00:30:11:000 - 00:30:15:329] **Speaker 0:** So We can.
[00:30:16:300 - 00:30:20:329] **Speaker 0:** Enforce a stopped condition, so that's one of those links
[00:30:20:670 - 00:30:22:229] **Speaker 0:** on that, that help page.
[00:30:22:839 - 00:30:24:180] **Speaker 0:** But stop condition.
[00:30:25:069 - 00:30:29:390] **Speaker 0:** Adding a stock condition, we can say that when the
[00:30:29:390 - 00:30:32:989] **Speaker 0:** minimum value reaches The safe cooking temperature.
[00:30:35:500 - 00:30:36:709] **Speaker 0:** So that's a looming operator.
[00:30:37:469 - 00:30:40:109] **Speaker 0:** In terms of resolution and time.
[00:30:41:719 - 00:30:43:160] **Speaker 0:** We talked about.
[00:30:47:630 - 00:30:51:819] **Speaker 0:** The time slipping As well, so.
[00:30:52:489 - 00:30:53:989] **Speaker 0:** If you have quite a large time set.
[00:30:56:670 - 00:30:59:719] **Speaker 0:** Um, If you have a time set for like 10
[00:30:59:719 - 00:31:02:319] **Speaker 0:** seconds and it keeps going on and you want to
[00:31:02:319 - 00:31:06:199] **Speaker 0:** resolve the cooking time within like 1 2nd, obviously it
[00:31:06:199 - 00:31:06:920] **Speaker 0:** might overshoot.
[00:31:07:609 - 00:31:10:670] **Speaker 0:** Um, and stop once that condition is met.
[00:31:11:209 - 00:31:13:010] **Speaker 0:** So you might want to have a smaller time step
[00:31:13:010 - 00:31:16:290] **Speaker 0:** being enforced, so that is under the time dependence solver
[00:31:16:290 - 00:31:20:930] **Speaker 0:** time stepping, we can adjust the maximum step value.
[00:31:21:250 - 00:31:22:930] **Speaker 0:** We can set that to be a certain value.
[00:31:23:650 - 00:31:26:819] **Speaker 0:** And we want to ensure that the relative tolerance is
[00:31:26:819 - 00:31:29:400] **Speaker 0:** quite tight as well, because that's driving the time.
[00:31:34:209 - 00:31:36:569] **Speaker 0:** And modelling the solid and fluid is what we just
[00:31:36:569 - 00:31:36:910] **Speaker 0:** did.
[00:31:40:810 - 00:31:41:810] **Speaker 0:** For the code.
[00:31:43:699 - 00:31:44:939] **Speaker 0:** How to use Kepper.
[00:31:46:650 - 00:31:48:130] **Speaker 0:** So this is our governing equation.
[00:32:01:969 - 00:32:04:000] **Speaker 0:** We were asked to discretize this.
[00:32:10:920 - 00:32:13:800] **Speaker 0:** With finite difference, so FTCS scheme.
[00:32:18:500 - 00:32:24:130] **Speaker 0:** And And The values on the right hand side are
[00:32:24:130 - 00:32:25:890] **Speaker 0:** going to be evaluated like the previous time level for
[00:32:25:890 - 00:32:26:689] **Speaker 0:** the explicit scheme.
[00:32:27:540 - 00:32:28:900] **Speaker 0:** And we've got grad.
[00:32:29:569 - 00:32:30:979] **Speaker 0:** Kappa grad.
[00:32:33:069 - 00:32:33:229] **Speaker 0:** And.
[00:32:33:839 - 00:32:37:060] **Speaker 0:** And in 2D, I think I actually gave that equation
[00:32:38:000 - 00:32:38:930] **Speaker 0:** equation 4.
[00:32:39:359 - 00:32:45:859] **Speaker 0:** So we've got D Y D X D T Y
[00:32:45:859 - 00:32:46:699] **Speaker 0:** D X.
[00:32:48:020 - 00:32:50:150] **Speaker 0:** Plus divide D Z kappa.
[00:32:51:079 - 00:32:52:729] **Speaker 0:** DT 5 DZ.
[00:32:54:310 - 00:32:57:819] **Speaker 0:** And if we look at our we've got eyes, OK,
[00:32:59:189 - 00:33:00:550] **Speaker 0:** uh, that's a bit of a pain is it?
[00:33:00:630 - 00:33:01:829] **Speaker 0:** That's why I call this kappa, I think.
[00:33:02:030 - 00:33:04:510] **Speaker 0:** So we've got IK I + 1, OK.
[00:33:05:170 - 00:33:06:500] **Speaker 0:** 1 minus 1k.
[00:33:14:349 - 00:33:18:770] **Speaker 0:** So these are our domains that we wanna disize across.
[00:33:20:160 - 00:33:23:099] **Speaker 0:** And that is equal to row C P D T
[00:33:23:099 - 00:33:24:040] **Speaker 0:** Y D D.
[00:33:25:479 - 00:33:28:650] **Speaker 0:** So what I've suggested is to analyse essentially the inner
[00:33:28:650 - 00:33:29:349] **Speaker 0:** derivative.
[00:33:30:540 - 00:33:35:869] **Speaker 0:** So The inner derivative at the halfway point.
[00:33:37:060 - 00:33:38:689] **Speaker 0:** So I plus 1/2.
[00:33:39:630 - 00:33:41:829] **Speaker 0:** And I'm on as a huff, OK.
[00:33:43:239 - 00:33:44:459] **Speaker 0:** So, we can call.
[00:33:45:949 - 00:33:46:469] **Speaker 0:** 5.
[00:33:54:310 - 00:33:56:310] **Speaker 0:** Well maybe we call that a different variable.
[00:34:09:309 - 00:34:21:919] **Speaker 0:** So for X We've got 5 Um, I, plus a
[00:34:21:919 - 00:34:22:398] **Speaker 0:** half.
[00:34:23:020 - 00:34:26:699] **Speaker 0:** OK minus 51 minus 5, OK.
[00:34:27:469 - 00:34:29:628] **Speaker 0:** Divided by X.
[00:34:31:378 - 00:34:32:658] **Speaker 0:** And for our.
[00:34:37:350 - 00:34:38:030] **Speaker 0:** OK.
[00:34:39:658 - 00:34:43:110] **Speaker 0:** Plus, I'll leave that one for you, so I don't
[00:34:43:209 - 00:34:44:908] **Speaker 0:** do everything, um.
[00:34:46:259 - 00:34:49:269] **Speaker 0:** And so we need to evaluate these inner derivatives, Phi
[00:34:49:458 - 00:34:50:638] **Speaker 0:** at the midway point.
[00:34:51:299 - 00:34:54:398] **Speaker 0:** So 5 at 5 + 1/2.
[00:34:55:019 - 00:34:55:458] **Speaker 0:** OK.
[00:34:55:658 - 00:34:57:138] **Speaker 0:** Any idea what that will equal?
[00:35:19:010 - 00:35:21:969] **Speaker 0:** We're evaluating our inner derivative, the term that we just
[00:35:21:969 - 00:35:26:689] **Speaker 0:** said was kappa DT by Dx at that right-hand midway
[00:35:26:689 - 00:35:27:879] **Speaker 0:** 0.1 + 1/2.
[00:35:28:330 - 00:35:32:090] **Speaker 0:** So we've got kappa at 1 + 1/2, OK.
[00:35:33:719 - 00:35:36:169] **Speaker 0:** And then we're going to apply a central difference formula
[00:35:36:479 - 00:35:40:129] **Speaker 0:** for our first order derivative at 0.1 + 1/2.
[00:35:41:949 - 00:35:43:530] **Speaker 0:** So we go up.
[00:35:44:340 - 00:35:45:439] **Speaker 0:** TI + 1.
[00:35:45:810 - 00:35:46:260] **Speaker 0:** OK.
[00:35:47:429 - 00:35:52:090] **Speaker 0:** Linus TIK divided by.
[00:35:53:270 - 00:35:53:989] **Speaker 0:** That interval.
[00:35:55:169 - 00:35:55:830] **Speaker 0:** Dot X.
[00:36:02:780 - 00:36:10:820] **Speaker 0:** So This was for the curved boundaries, which I know
[00:36:10:820 - 00:36:11:540] **Speaker 0:** is a different case.
[00:36:11:620 - 00:36:14:699] **Speaker 0:** We've, we've just got uniform grid spacing, but we are
[00:36:14:699 - 00:36:18:379] **Speaker 0:** evaluating the derivatives at the midpoints, so at points A
[00:36:18:379 - 00:36:18:919] **Speaker 0:** and B.
[00:36:19:580 - 00:36:20:780] **Speaker 0:** And we've done the same here.
[00:36:20:820 - 00:36:23:360] **Speaker 0:** We're evaluating fire at the midpoint.
[00:36:24:479 - 00:36:28:320] **Speaker 0:** I plus 12 And we've got the temperature at 1
[00:36:28:320 - 00:36:29:729] **Speaker 0:** + 1 minus Ti.
[00:36:30:239 - 00:36:32:399] **Speaker 0:** The only difference is we've got this kappa value that
[00:36:32:399 - 00:36:34:280] **Speaker 0:** we need to evaluate at the midpoint.
[00:36:39:149 - 00:36:43:389] **Speaker 0:** So Kappa net 1 plus 1/2.
[00:36:46:080 - 00:36:50:959] **Speaker 0:** Is equal to kappa at Ti plus 1/2, OK?
[00:36:54:659 - 00:36:57:820] **Speaker 0:** But what, what, what temperature field are we actually solving
[00:36:57:820 - 00:36:57:899] **Speaker 0:** for?
[00:36:57:949 - 00:37:02:340] **Speaker 0:** We're only solving the points at I's, like integer values,
[00:37:02:510 - 00:37:03:949] **Speaker 0:** I, I plus 1, etc.
[00:37:05:040 - 00:37:06:500] **Speaker 0:** So we can approximate.
[00:37:09:709 - 00:37:14:459] **Speaker 0:** TI plus a half k is approximately the average of
[00:37:14:459 - 00:37:15:270] **Speaker 0:** the neighbouring two.
[00:37:25:939 - 00:37:28:100] **Speaker 0:** And as I think I said it earlier this week,
[00:37:28:300 - 00:37:31:580] **Speaker 0:** someone in the labs had done like linear interpolation for,
[00:37:31:729 - 00:37:35:139] **Speaker 0:** for that, which will work as well, um, I think
[00:37:35:139 - 00:37:35:500] **Speaker 0:** it should.
[00:37:36:179 - 00:37:37:179] **Speaker 0:** But it is just the average.
[00:37:37:340 - 00:37:39:000] **Speaker 0:** This is a linear interpolation as well.
[00:37:44:840 - 00:37:47:110] **Speaker 0:** So I think, I don't know, I think that was
[00:37:47:110 - 00:37:50:290] **Speaker 0:** the most tricky part of the discretization.
[00:37:52:189 - 00:37:55:989] **Speaker 0:** If you're stuck with the coding, that was chapter 6
[00:37:55:989 - 00:37:56:590] **Speaker 0:** demo.
[00:38:03:840 - 00:38:05:310] **Speaker 0:** Chapter 6.
[00:38:07:629 - 00:38:10:120] **Speaker 0:** And I just sort of fabricated some 2D case.
[00:38:10:199 - 00:38:12:639] **Speaker 0:** It was really 1D, but we just made a second
[00:38:12:639 - 00:38:14:860] **Speaker 0:** dimension for for this coding exercise.
[00:38:15:280 - 00:38:16:310] **Speaker 0:** So we have 34 loops.
[00:38:16:320 - 00:38:18:439] **Speaker 0:** We've got one for time and then one for the
[00:38:18:439 - 00:38:21:629] **Speaker 0:** X and Y coordinates, and then we've got conditions depending
[00:38:21:629 - 00:38:22:479] **Speaker 0:** on where we are.
[00:38:23:169 - 00:38:24:810] **Speaker 0:** Um, solving for.
[00:38:24:889 - 00:38:27:459] **Speaker 0:** So we've got a few different boundary conditions to solve
[00:38:27:459 - 00:38:28:939] **Speaker 0:** for in this case, so.
[00:38:29:729 - 00:38:31:810] **Speaker 0:** You'll have a few of our statements.
[00:38:40:080 - 00:38:43:709] **Speaker 0:** So exporting data as a text file from console to
[00:38:43:709 - 00:38:44:679] **Speaker 0:** plot in Python.
[00:38:47:239 - 00:38:50:479] **Speaker 0:** So in lab 4 we looked at exporting like a
[00:38:50:479 - 00:38:53:260] **Speaker 0:** line, a cut line and also a surface plot.
[00:38:53:850 - 00:38:56:560] **Speaker 0:** If there's a particular line graph within console that you
[00:38:56:560 - 00:38:57:580] **Speaker 0:** want to export.
[00:39:06:520 - 00:39:09:070] **Speaker 0:** Maybe these got these ones, but you can right click.
[00:39:12:500 - 00:39:15:580] **Speaker 0:** Um Maybe the point riff.
[00:39:16:379 - 00:39:16:959] **Speaker 0:** Point graph.
[00:39:17:969 - 00:39:21:000] **Speaker 0:** Add plot data to export and then it will only
[00:39:21:000 - 00:39:22:229] **Speaker 0:** take this data.
[00:39:23:899 - 00:39:27:909] **Speaker 0:** And you can copy to clipboard, but that isn't, you
[00:39:27:909 - 00:39:31:030] **Speaker 0:** have more, uh, choice if you go to export, you
[00:39:31:030 - 00:39:31:649] **Speaker 0:** can check.
[00:39:33:379 - 00:39:36:459] **Speaker 0:** If multiple curves, you can set as columns, which might
[00:39:36:459 - 00:39:37:060] **Speaker 0:** be helpful.
[00:39:39:530 - 00:39:41:929] **Speaker 0:** So I think that's, I know someone asked this in
[00:39:41:929 - 00:39:45:350] **Speaker 0:** the lab yesterday, so I think that that answers that
[00:39:45:729 - 00:39:46:409] **Speaker 0:** that query.
[00:39:50:530 - 00:39:53:919] **Speaker 0:** Glots within console, so using the heat equation.
[00:39:54:790 - 00:39:58:669] **Speaker 0:** Part one Calculate the average heat fluxes.
[00:39:59:590 - 00:40:01:909] **Speaker 0:** Across each boundary.
[00:40:03:479 - 00:40:05:389] **Speaker 0:** So we're trying to plot something over time.
[00:40:06:300 - 00:40:08:500] **Speaker 0:** So this is, what are we doing?
[00:40:08:649 - 00:40:09:679] **Speaker 0:** Chapter 12.
[00:40:11:250 - 00:40:13:639] **Speaker 0:** So this is the heat equation.
[00:40:20:939 - 00:40:21:379] **Speaker 0:** I think.
[00:40:23:360 - 00:40:23:679] **Speaker 0:** Yep.
[00:40:24:120 - 00:40:25:439] **Speaker 0:** So, oops.
[00:40:28:250 - 00:40:31:290] **Speaker 0:** Maybe just create a new plot group, um, so I
[00:40:31:290 - 00:40:33:669] **Speaker 0:** wanna plot the heat flux over time.
[00:40:35:600 - 00:40:37:010] **Speaker 0:** Which is going to be a line graph, so a
[00:40:37:010 - 00:40:37:790] **Speaker 0:** 1D plot group.
[00:40:38:590 - 00:40:42:750] **Speaker 0:** And we can choose a point graph if it was.
[00:40:45:409 - 00:40:49:340] **Speaker 0:** Uh, so, I'll answer this first and then talk about
[00:40:49:340 - 00:40:49:820] **Speaker 0:** the integration.
[00:40:49:939 - 00:40:51:159] **Speaker 0:** So we've got a point graph.
[00:40:52:659 - 00:40:54:600] **Speaker 0:** Here we can just plot the temperature over time.
[00:40:55:659 - 00:40:56:429] **Speaker 0:** It's fixed.
[00:40:56:739 - 00:40:59:320] **Speaker 0:** If we want to plot the gradient, we can append
[00:40:59:540 - 00:41:02:979] **Speaker 0:** the um the coordinate that we want to differentiate against.
[00:41:03:840 - 00:41:06:070] **Speaker 0:** So like, so, I think this is equivalent to D
[00:41:06:070 - 00:41:07:500] **Speaker 0:** of DX.
[00:41:09:850 - 00:41:10:669] **Speaker 0:** No, it's not.
[00:41:11:290 - 00:41:12:209] **Speaker 0:** So don't use that.
[00:41:13:199 - 00:41:14:090] **Speaker 0:** So it's DX.
[00:41:15:270 - 00:41:20:729] **Speaker 0:** And We've also got minus K times DX.
[00:41:21:199 - 00:41:23:520] **Speaker 0:** DT by DX is our definition for heat flux.
[00:41:24:739 - 00:41:26:300] **Speaker 0:** So I think that would be the easiest way to
[00:41:26:310 - 00:41:27:639] **Speaker 0:** to plot the heat fluxes.
[00:41:28:100 - 00:41:31:780] **Speaker 0:** If you want to plot it across a length, because
[00:41:31:780 - 00:41:34:340] **Speaker 0:** we want to know like the average or integral of
[00:41:34:340 - 00:41:36:219] **Speaker 0:** the heat flux across the boundary.
[00:41:36:979 - 00:41:38:689] **Speaker 0:** Essentially, we want to look at how much heat flux
[00:41:38:689 - 00:41:40:419] **Speaker 0:** is coming into the patty and how much is leaving.
[00:41:40:580 - 00:41:42:280] **Speaker 0:** That's the purpose of this exercise.
[00:41:43:739 - 00:41:50:129] **Speaker 0:** And We've got integration, we can do a line integration
[00:41:50:129 - 00:41:50:370] **Speaker 0:** here.
[00:41:51:330 - 00:41:54:719] **Speaker 0:** So evaluating across some some boundary and again typing in
[00:41:54:719 - 00:41:55:780] **Speaker 0:** your minus KD.
[00:41:57:649 - 00:41:57:669] **Speaker 0:** Thanks.
[00:42:02:290 - 00:42:16:030] **Speaker 0:** So, uh, For the full 3D Patty question, what would
[00:42:16:030 - 00:42:19:129] **Speaker 0:** you consider an acceptable level of detail?
[00:42:22:590 - 00:42:24:949] **Speaker 0:** I guess so that one of your classmates could, could
[00:42:24:949 - 00:42:25:649] **Speaker 0:** create the mesh.
[00:42:26:290 - 00:42:31:919] **Speaker 0:** So someone that's reasonably familiar with numerical modelling, but Um,
[00:42:32:239 - 00:42:33:959] **Speaker 0:** don't know what sittings you've chosen.
[00:42:38:459 - 00:42:41:560] **Speaker 0:** and I think I sort of showed that with this,
[00:42:42:159 - 00:42:45:479] **Speaker 0:** these two examples, so it makes sense to do some
[00:42:45:820 - 00:42:48:780] **Speaker 0:** temperature value at a particular point in space and time.
[00:42:48:899 - 00:42:50:979] **Speaker 0:** It needs to be at the same point of, Point
[00:42:50:979 - 00:42:53:379] **Speaker 0:** in space and time for each mesh resolution so that
[00:42:53:379 - 00:42:55:459] **Speaker 0:** you get the fair comparison.
[00:43:01:070 - 00:43:04:750] **Speaker 0:** How do you suggest we show mesh convergence?
[00:43:05:919 - 00:43:06:429] **Speaker 0:** For the 3.
[00:43:06:850 - 00:43:08:129] **Speaker 0:** OK, I think that was the same.
[00:43:09:570 - 00:43:11:850] **Speaker 0:** OK, where was I?
[00:43:21:139 - 00:43:23:120] **Speaker 0:** So the thermal conductivity.
[00:43:26:290 - 00:43:28:189] **Speaker 0:** That I've provided here.
[00:43:31:510 - 00:43:35:669] **Speaker 0:** is sourced from this paper, so have a quick flick
[00:43:35:669 - 00:43:38:370] **Speaker 0:** through that and see where this equation is coming from
[00:43:38:590 - 00:43:43:959] **Speaker 0:** and Is it valid to use in our model?
[00:43:44:520 - 00:43:46:820] **Speaker 0:** That's, that's what I want you to, to think about.
[00:43:51:320 - 00:43:54:429] **Speaker 0:** So I guess it's sort of related to the actual
[00:43:54:429 - 00:43:56:399] **Speaker 0:** physical limitations of modelling Kappa T.
[00:43:56:600 - 00:43:57:989] **Speaker 0:** Well, not the mechanics.
[00:43:58:040 - 00:43:59:919] **Speaker 0:** I mean, we know that you can do it in
[00:43:59:919 - 00:44:02:879] **Speaker 0:** console and elsewhere, and T is in degrees Celsius, but
[00:44:02:879 - 00:44:05:000] **Speaker 0:** think about what the function of Kappa.
[00:44:08:080 - 00:44:10:860] **Speaker 0:** And font size, no, I think I was going around
[00:44:10:860 - 00:44:13:479] **Speaker 0:** and someone had like a super tiny font that's cheating
[00:44:13:479 - 00:44:16:290] **Speaker 0:** with like trying to squeeze more content into your report.
[00:44:16:760 - 00:44:19:600] **Speaker 0:** So I've set a page limit because it's really important
[00:44:19:600 - 00:44:24:080] **Speaker 0:** to be able to concisely report things in an engineering
[00:44:24:080 - 00:44:24:659] **Speaker 0:** context.
[00:44:25:040 - 00:44:30:760] **Speaker 0:** You don't want to have You know, AI slot that's
[00:44:30:760 - 00:44:33:800] **Speaker 0:** like hundreds of pages long that you can't follow that
[00:44:33:800 - 00:44:35:580] **Speaker 0:** supposedly derives some proof.
[00:44:35:959 - 00:44:38:699] **Speaker 0:** Um, so you want to try and have some nice
[00:44:39:439 - 00:44:42:959] **Speaker 0:** concise wording, not like I'm describing right now.
[00:44:44:020 - 00:44:47:770] **Speaker 0:** That someone can follow along and not spend like half
[00:44:47:770 - 00:44:49:120] **Speaker 0:** an hour just to read your report.
[00:44:50:239 - 00:44:54:649] **Speaker 0:** So, try to keep with the The font size that
[00:44:54:830 - 00:44:56:590] **Speaker 0:** is in the assignment template.
[00:44:57:310 - 00:45:00:790] **Speaker 0:** And remember to use the assignment template, um, and that
[00:45:00:790 - 00:45:01:550] **Speaker 0:** there is a page limit.
[00:45:03:340 - 00:45:15:639] **Speaker 0:** So, yep So I guess in general I've provided this
[00:45:15:639 - 00:45:18:239] **Speaker 0:** sort of high level marking rubric in terms of what
[00:45:18:239 - 00:45:20:360] **Speaker 0:** we'll be marking against just so that you have a
[00:45:20:360 - 00:45:21:540] **Speaker 0:** good idea of what we're including.
[00:45:23:919 - 00:45:27:510] **Speaker 0:** So include everything that I've included in these bullet points.
[00:45:27:750 - 00:45:29:760] **Speaker 0:** If you want to include further, that's fine as long
[00:45:29:760 - 00:45:30:600] **Speaker 0:** as it fits in.
[00:45:31:850 - 00:45:38:409] **Speaker 0:** Um, In particular, the 2D and the 3D cases, it
[00:45:38:409 - 00:45:40:399] **Speaker 0:** would be really good to see the temperature profile so
[00:45:40:399 - 00:45:41:520] **Speaker 0:** we can make a comparison.
[00:45:44:729 - 00:45:48:570] **Speaker 0:** place column spacing is sort of similar to.
[00:45:52:500 - 00:45:54:780] **Speaker 0:** That shouldn't be.
[00:45:57:120 - 00:46:00:110] **Speaker 0:** We have to Um.
[00:46:04:709 - 00:46:07:979] **Speaker 0:** I don't know if I just Yeah, I'll just, I'll
[00:46:07:979 - 00:46:09:300] **Speaker 0:** just bring it up now, but.
[00:46:11:469 - 00:46:13:030] **Speaker 0:** It'll just load, um.
[00:46:21:590 - 00:46:24:850] **Speaker 0:** But yeah, ever think if anyone has any other questions?
[00:46:27:580 - 00:46:30:459] **Speaker 0:** Assignment to template.
[00:46:48:330 - 00:47:06:179] **Speaker 0:** So That's probably a better way of doing this, using
[00:47:06:179 - 00:47:08:300] **Speaker 0:** the lips and package, but.
[00:47:11:659 - 00:47:12:550] **Speaker 0:** No, that's awesome.
[00:47:25:689 - 00:47:27:199] **Speaker 0:** I can put a lot of text on these.
[00:47:28:610 - 00:47:29:239] **Speaker 0:** Columns.
[00:47:33:169 - 00:47:37:010] **Speaker 0:** Is it So that's showing, is that not what you're
[00:47:37:010 - 00:47:37:330] **Speaker 0:** getting?
[00:47:40:129 - 00:47:41:709] **Speaker 0:** Maybe download it again.
[00:47:43:250 - 00:47:44:889] **Speaker 0:** Oh, I'm so.
[00:47:46:379 - 00:47:47:489] **Speaker 0:** Options.
[00:47:48:239 - 00:47:50:750] **Speaker 0:** So I'm using TechStudio, and it seems to work fine.
[00:47:51:500 - 00:47:53:679] **Speaker 0:** And PDF later, um.
[00:47:55:399 - 00:47:58:000] **Speaker 0:** If you use, what was it like lure latec and
[00:47:58:000 - 00:48:01:540] **Speaker 0:** all the the Lulac and ZAc might do something funky,
[00:48:01:959 - 00:48:04:360] **Speaker 0:** um, are you using PDF or?
[00:48:05:739 - 00:48:06:520] **Speaker 0:** I was happy.
[00:48:08:100 - 00:48:09:090] **Speaker 0:** Uh, over this.
[00:48:10:080 - 00:48:13:439] **Speaker 0:** I'm not a big fan of overfish, but um.
[00:48:15:600 - 00:48:16:919] **Speaker 0:** Oh, that's a pain.
[00:48:18:149 - 00:48:20:780] **Speaker 0:** Can you install TechStudio on your laptop, would be my
[00:48:20:780 - 00:48:21:820] **Speaker 0:** recommendation, but.
[00:48:26:580 - 00:48:30:159] **Speaker 0:** Um, yeah, I'll have a look after this with overleaf,
[00:48:30:280 - 00:48:31:040] **Speaker 0:** but um.
[00:48:32:750 - 00:48:35:949] **Speaker 0:** Yeah, that's, that's what I'm, I'm expecting.
[00:48:39:169 - 00:48:41:370] **Speaker 0:** But yeah, overleaf has at times out if you make
[00:48:41:370 - 00:48:42:929] **Speaker 0:** figures that are too detailed, so.
[00:48:43:620 - 00:48:46:739] **Speaker 0:** It's, it's probably fine for us, but, um, yeah.
[00:48:49:189 - 00:48:49:669] **Speaker 0:** Cool.
[00:48:50:110 - 00:48:50:709] **Speaker 0:** Uh, yep.
[00:48:51:439 - 00:48:54:120] **Speaker 0:** Uh, to the, uh, stop.
[00:48:56:179 - 00:48:57:050] **Speaker 0:** For the time skiing.
[00:48:57:830 - 00:49:20:250] **Speaker 0:** Um Um Could Expected produce So Yeah, so this can
[00:49:20:250 - 00:49:20:949] **Speaker 0:** be an expression.
[00:49:21:250 - 00:49:22:370] **Speaker 0:** I've not tried this, but you can.
[00:49:23:120 - 00:49:25:080] **Speaker 0:** You can make an expression that is a function of
[00:49:25:080 - 00:49:27:510] **Speaker 0:** that difference, so you could explore that.
[00:49:29:850 - 00:49:32:169] **Speaker 0:** The variables that were part of the.
[00:49:32:879 - 00:49:34:919] **Speaker 0:** You might have to call like Comp one or something
[00:49:34:919 - 00:49:37:229] **Speaker 0:** like that to call it from this global scope.
[00:49:38:600 - 00:49:40:879] **Speaker 0:** didn't didn't just did it to be.
[00:49:41:790 - 00:49:45:709] **Speaker 0:** A value that you're happy with and I, I wouldn't
[00:49:45:709 - 00:49:46:949] **Speaker 0:** spend too much time on that.
[00:49:47:110 - 00:49:47:310] **Speaker 0:** Yeah.
[00:49:48:899 - 00:49:50:879] **Speaker 0:** H Yeah.
[00:49:52:239 - 00:49:52:250] **Speaker 0:** Yep.
[00:49:54:350 - 00:49:57:489] **Speaker 0:** Is that for Yes.
[00:49:58:620 - 00:50:00:639] **Speaker 0:** So that's doing the swap between the dairy clay and
[00:50:00:639 - 00:50:03:520] **Speaker 0:** the bob and boundary conditions.
[00:50:04:800 - 00:50:06:959] **Speaker 0:** Yes, yes, yeah, yeah, precisely, yeah.
[00:50:09:080 - 00:50:17:889] **Speaker 0:** index a single In console How do you, um, so
[00:50:17:889 - 00:50:19:489] **Speaker 0:** that's these point graphs.
[00:50:20:860 - 00:50:22:199] **Speaker 0:** Uh, do you mean like this?
[00:50:23:239 - 00:50:24:550] **Speaker 0:** You can select a point.
[00:50:27:810 - 00:50:30:620] **Speaker 0:** The the degrees of freedom thing that we're doing right.
[00:50:32:290 - 00:50:36:260] **Speaker 0:** when, So you can do the point evaluation.
[00:50:37:120 - 00:50:38:939] **Speaker 0:** And then select like the last time.
[00:50:38:959 - 00:50:41:040] **Speaker 0:** If it was the last time or set a particular
[00:50:41:040 - 00:50:43:199] **Speaker 0:** point, maybe you choose a point.
[00:50:44:149 - 00:50:44:530] **Speaker 0:** Yeah.
[00:50:46:800 - 00:50:49:760] **Speaker 0:** So that's this is a one-dimensional domain, but you just
[00:50:49:760 - 00:50:50:120] **Speaker 0:** click.
[00:50:50:280 - 00:50:53:760] **Speaker 0:** So this is the selection, um, enabling and disabling the
[00:50:53:760 - 00:50:57:169] **Speaker 0:** selection and we can choose which, which, which points.
[00:50:57:280 - 00:50:58:750] **Speaker 0:** So there needs to be a point within the domain,
[00:50:58:760 - 00:51:00:780] **Speaker 0:** but I default the corners of points.
[00:51:01:040 - 00:51:01:239] **Speaker 0:** Yeah.
[00:51:02:500 - 00:51:02:959] **Speaker 0:** No worries.
[00:51:04:060 - 00:51:04:419] **Speaker 0:** Cool.
[00:51:04:739 - 00:51:07:699] **Speaker 0:** Oh, we managed to fit fit in in the lecture,
[00:51:07:870 - 00:51:08:530] **Speaker 0:** so that's good.
[00:51:08:800 - 00:51:10:979] **Speaker 0:** I think there was another question that came through as
[00:51:10:979 - 00:51:12:379] **Speaker 0:** I was walking over, but um.
[00:51:14:060 - 00:51:18:260] **Speaker 0:** Oh Have a look at that later, um, oh yes.
[00:51:19:020 - 00:51:21:030] **Speaker 0:** Is it On a log scale.
[00:51:22:590 - 00:51:24:229] **Speaker 0:** It would be good to be on a log scale,
[00:51:24:300 - 00:51:27:139] **Speaker 0:** but if it was negative, then it doesn't really make
[00:51:27:139 - 00:51:29:449] **Speaker 0:** sense because it's a log of negative value, which is
[00:51:29:449 - 00:51:34:100] **Speaker 0:** why using that, um, that sim log plotting function was
[00:51:34:100 - 00:51:36:989] **Speaker 0:** quite cool that I saw, um, but yeah, up to
[00:51:36:989 - 00:51:38:270] **Speaker 0:** you, otherwise just use absolute.
[00:51:42:469 - 00:51:42:770] **Speaker 0:** Cool.
[00:51:43:040 - 00:51:45:300] **Speaker 0:** Well, good luck with your, your assignment.
[00:51:45:750 - 00:51:49:129] **Speaker 0:** um, and we'll see you, we'll see you on Monday.
[00:51:50:820 - 00:51:53:139] **Speaker 0:** And yeah, use the form if you're like stuck.
[00:51:53:300 - 00:51:56:199] **Speaker 0:** I can reply to those posts.
[00:52:07:820 - 00:52:08:320] **Speaker 0:** No.
[00:52:22:979 - 00:52:24:949] **Speaker 0:** Just Elliott, let's change the thoughts on the candidate.
[00:52:26:199 - 00:52:27:560] **Speaker 0:** I'll try and keep it consistent.
[00:52:27:679 - 00:52:30:959] **Speaker 0:** It looked like to a slightly similar one, but the
[00:52:31:360 - 00:52:32:479] **Speaker 0:** default one looks a little.
[00:52:33:629 - 00:52:34:360] **Speaker 0:** Yeah, I know.
[00:52:34:689 - 00:52:36:320] **Speaker 0:** Well, you can, if it looks similar, that's fine as
[00:52:36:320 - 00:52:37:330] **Speaker 0:** long as it's the same font size.
[00:52:37:489 - 00:52:40:850] **Speaker 0:** Yeah, OK, I'll check to make sure that the page
[00:52:40:850 - 00:52:41:379] **Speaker 0:** count is the same.
[00:52:41:489 - 00:52:42:810] **Speaker 0:** Yeah, yeah, that's the main thing.
[00:52:42:959 - 00:52:43:560] **Speaker 0:** Yeah, yeah.
[00:52:52:239 - 00:52:52:659] **Speaker 1:** Thank you.
[00:54:46:689 - 00:54:47:120] **Speaker 1:** What do you think?
[00:54:47:169 - 00:54:48:689] **Speaker 1:** Do you think everyone's going to be here today, or
[00:54:48:689 - 00:54:50:830] **Speaker 1:** is everyone like working on their paper?

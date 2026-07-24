# ENME302-26S2 Lecture 6 fast-pass local ASR transcript

Date: July 22, 2026 11:00am-11:55am
Transcript type: Hermes fast-pass local ASR from validated Echo audio, not a native Echo transcript.
Backend/model: faster-whisper tiny.en, CPU int8, beam_size=1, vad_filter=True.
Quality note: fast catch-up transcript. Technical terms, equations, names and Māori words need checking against slides/audio before assessment use.
Source audio SHA-256: `fd6ce78b2af32911144f393e59d02a508f4e98d47c15facf74bc0f3d1c1e02da`
Generated: 2026-07-24T23:58:18.525726+12:00

[00:01:13.230 - 00:01:18.900] We have a co-tow, a clock of the long year round.
[00:01:18.900 - 00:01:20.500] Thanks for coming along.
[00:01:20.500 - 00:01:22.260] Before we jump into the next,
[00:01:22.260 - 00:01:23.580] I just want to cover sort of,
[00:01:23.580 - 00:01:25.380] conceptually what we're going to be doing today.
[00:01:25.380 - 00:01:27.020] So, in the course today,
[00:01:27.020 - 00:01:27.940] what we've done is we've gone through
[00:01:27.940 - 00:01:30.220] and we've covered some derivations.
[00:01:30.220 - 00:01:32.500] We've looked and used a couple of different
[00:01:32.500 - 00:01:35.060] derivation methods to define the stiffness matrix
[00:01:35.060 - 00:01:37.700] for a bar element that relates the applied loads
[00:01:37.700 - 00:01:39.500] for the corresponding deflections.
[00:01:39.500 - 00:01:41.900] And we actually now have a reasonable definition
[00:01:41.900 - 00:01:43.860] for that one element.
[00:01:43.860 - 00:01:46.140] We basically have our fundamental building block
[00:01:47.140 - 00:01:48.140] structures.
[00:01:49.220 - 00:01:54.220] And what we did on Monday was we just started dealing
[00:01:54.580 - 00:01:56.260] with transformations.
[00:01:56.260 - 00:01:58.900] So, we know elements within a structure,
[00:01:58.900 - 00:02:00.700] maybe on different orientations.
[00:02:00.700 - 00:02:02.500] And we developed a transformation matrix
[00:02:02.500 - 00:02:07.060] and a simple consistent generic matrix method,
[00:02:07.060 - 00:02:11.390] which can transform all the bar elements of the sort.
[00:02:11.390 - 00:02:13.430] So, we have kind of our wooden block,
[00:02:13.430 - 00:02:14.630] we have our transformation to account
[00:02:14.630 - 00:02:15.470] for different angles.
[00:02:15.470 - 00:02:17.190] The one piece that we're missing
[00:02:17.230 - 00:02:20.070] is how to actually join different elements together.
[00:02:20.070 - 00:02:21.550] So, within a structure,
[00:02:21.550 - 00:02:23.190] you could have any lower valements
[00:02:23.190 - 00:02:25.310] that are connected into making a overall structure.
[00:02:25.310 - 00:02:26.670] And we need to know how to connect them,
[00:02:26.670 - 00:02:28.590] how to methodically represent a connection
[00:02:28.590 - 00:02:31.190] between them and a connection to support points.
[00:02:31.190 - 00:02:33.190] And that's what we're going to be looking at today.
[00:02:34.110 - 00:02:35.990] So, it's just a very quick recap.
[00:02:35.990 - 00:02:38.310] We did this last week, this was the structure.
[00:02:38.310 - 00:02:41.470] Just reminded to you that when you give them a problem
[00:02:41.470 - 00:02:43.190] like this in the test,
[00:02:43.190 - 00:02:45.750] you wouldn't be given the Q1 Q2.
[00:02:45.750 - 00:02:48.190] You would have to make that decision yourself.
[00:02:48.190 - 00:02:50.350] So, essentially the lower point,
[00:02:50.350 - 00:02:51.270] because it's fully constrained,
[00:02:51.270 - 00:02:54.910] that there's no possibility of any deflection,
[00:02:54.910 - 00:02:57.070] any movement of those points.
[00:02:57.070 - 00:02:59.870] Then there's no degrees of freedom there.
[00:02:59.870 - 00:03:01.710] But there is the potential for non-zero displacements
[00:03:01.710 - 00:03:03.230] to the horizontal and vertical defection here.
[00:03:03.230 - 00:03:06.150] So, we have Q1 here in a Q2 here.
[00:03:06.150 - 00:03:10.030] So, the lower case Q1 is the permissible deflection
[00:03:10.030 - 00:03:12.030] that can exist within the structure.
[00:03:12.030 - 00:03:14.750] And the upper case Q1 is the corresponding applied load.
[00:03:14.750 - 00:03:16.710] So, the always comes a couple here.
[00:03:16.710 - 00:03:19.270] So, Q1, lower case Q1 and upper case Q1,
[00:03:20.270 - 00:03:22.710] and upper case Q2 and upper case Q2.
[00:03:22.710 - 00:03:24.830] That always, the sub-scriptal,
[00:03:24.830 - 00:03:25.870] the same number,
[00:03:25.870 - 00:03:27.670] that always in the same location,
[00:03:27.670 - 00:03:29.230] in the same direction as each other.
[00:03:30.550 - 00:03:33.950] What we saw was we had this element left across nicely,
[00:03:33.950 - 00:03:36.990] where the local corner systems,
[00:03:36.990 - 00:03:39.430] and the local corner systems are nicely aligned.
[00:03:39.430 - 00:03:41.710] But when we were in here, there was this disconnect.
[00:03:41.750 - 00:03:44.630] So, how we're gonna deal with that.
[00:03:45.990 - 00:03:48.190] And what we did was we went through,
[00:03:48.190 - 00:03:51.550] and we got this,
[00:03:51.550 - 00:03:53.870] we broke up the defection components
[00:03:53.870 - 00:03:55.390] into an exunwicant component,
[00:03:55.390 - 00:04:00.230] just basically a vector component of the total defection.
[00:04:00.230 - 00:04:03.910] Just like you've done many times before with forces.
[00:04:03.910 - 00:04:06.030] And we broke them up into an exunwicant component
[00:04:06.030 - 00:04:08.910] of the gene, so we now have four degrees of freedom
[00:04:08.910 - 00:04:10.830] rather than just two.
[00:04:10.830 - 00:04:13.750] And then we have our cosign and sign terms here.
[00:04:13.750 - 00:04:17.670] We've broken out into a particular equation.
[00:04:19.390 - 00:04:21.070] And then this is our transformation matrix.
[00:04:21.070 - 00:04:23.310] So this is the upper case lambda.
[00:04:23.310 - 00:04:24.510] And this is what transforms
[00:04:24.510 - 00:04:26.430] between one coordinate system and the other.
[00:04:27.910 - 00:04:33.460] It's a summary of the equations there.
[00:04:33.460 - 00:04:38.460] And then when we look at the overall stiffness matrix,
[00:04:39.740 - 00:04:41.100] we can go through and we can substitute
[00:04:41.900 - 00:04:43.540] the transformation.
[00:04:43.540 - 00:04:46.300] And what we often we come through with
[00:04:46.300 - 00:04:49.420] is this bracket of term here is little two by two
[00:04:49.420 - 00:04:51.100] stiffness matrix we've already derived.
[00:04:51.100 - 00:04:53.100] So we don't need to, we already know
[00:04:53.100 - 00:04:54.620] what that bracket of term is.
[00:04:54.620 - 00:04:56.500] We don't have to read or I've that.
[00:04:56.500 - 00:04:58.900] And then we have our delta, our lambda.
[00:04:58.900 - 00:05:01.580] So we pre-mop by the transpose of lambda.
[00:05:01.580 - 00:05:03.140] And we post-mop by lambda.
[00:05:03.140 - 00:05:04.380] That's the transformation matrix
[00:05:04.380 - 00:05:06.620] that was defined on the previous page.
[00:05:06.620 - 00:05:08.740] And then we get these equations here.
[00:05:09.020 - 00:05:12.020] So just to recap as I mentioned,
[00:05:12.020 - 00:05:14.740] and the lab this week you will have to define
[00:05:14.740 - 00:05:16.940] these matrices and use them into your code.
[00:05:16.940 - 00:05:18.540] But as strong as this,
[00:05:18.540 - 00:05:22.460] it's as strong as just that you use this transformation here
[00:05:22.460 - 00:05:24.820] and do this multiplication.
[00:05:24.820 - 00:05:26.540] That will give you this four by four matrix.
[00:05:26.540 - 00:05:27.820] You don't have to type it out.
[00:05:27.820 - 00:05:29.940] So while there's nothing wrong with this,
[00:05:29.940 - 00:05:31.060] they are mathematically equal.
[00:05:31.060 - 00:05:33.260] If you want to sit there and type out 16 numbers,
[00:05:33.260 - 00:05:34.260] go for it.
[00:05:34.260 - 00:05:36.860] This is perfectly fine, but it's a lot easier
[00:05:36.860 - 00:05:39.940] to do this more matrices through the multiplication
[00:05:39.940 - 00:05:45.970] and then Python do the hard work for you.
[00:05:45.970 - 00:05:48.170] So converting between here,
[00:05:48.170 - 00:05:51.850] just to do a quick recap of this,
[00:05:51.850 - 00:05:55.530] this is the element to go through them
[00:05:55.530 - 00:05:58.490] and deflections in local coordinates.
[00:05:58.490 - 00:06:00.970] And this is global coordinates.
[00:06:00.970 - 00:06:03.210] Let's just look and make sure that
[00:06:05.170 - 00:06:09.800] those equations on the previous page,
[00:06:09.800 - 00:06:11.000] we have this definition.
[00:06:11.000 - 00:06:14.520] But if we want to transform between our lowercase d
[00:06:14.520 - 00:06:16.800] and our uppercase d, how does that actually work?
[00:06:16.800 - 00:06:21.440] Well, to go from a lowercase to an uppercase,
[00:06:21.440 - 00:06:24.240] we can just resolve into the x and y components.
[00:06:24.240 - 00:06:25.680] That's relatively easy.
[00:06:25.680 - 00:06:27.400] But if we want to go to a lowercase d
[00:06:27.400 - 00:06:30.440] from the uppercase d to the other direction,
[00:06:30.440 - 00:06:31.880] how do we go about doing that?
[00:06:31.880 - 00:06:34.800] And what that actually comes down to
[00:06:34.800 - 00:06:39.800] is that our lowercase d is the long blue vector.
[00:06:41.400 - 00:06:42.760] On the diagonal.
[00:06:42.760 - 00:06:47.040] And if we say, so this is a 90 degree and 2 million here,
[00:06:47.040 - 00:06:48.120] we're actually going to break the triangle
[00:06:48.120 - 00:06:49.960] off into two smaller triangles.
[00:06:49.960 - 00:06:53.960] We actually have our d1 cos alpha is this, this here.
[00:06:53.960 - 00:06:56.160] And then d1 sin alpha is this piece here.
[00:06:56.160 - 00:06:58.760] And then we add them together as vectors
[00:06:58.760 - 00:07:00.840] we get the overall vector d1.
[00:07:00.840 - 00:07:02.720] So just to give you some confidence,
[00:07:02.720 - 00:07:04.400] as we have this equation has come from,
[00:07:04.400 - 00:07:07.160] hopefully, yeah, makes sense to you
[00:07:07.160 - 00:07:10.200] that this equation has actually proven
[00:07:10.200 - 00:07:15.980] through this little diagram here.
[00:07:15.980 - 00:07:18.500] And similarly, we're not going to redo this diagram,
[00:07:18.500 - 00:07:21.060] but we can apply the same thing at node 2.
[00:07:21.060 - 00:07:26.160] It's 0.01 and it would be the exact same process.
[00:07:26.160 - 00:07:30.280] And matrix form, how it's expressed as the lowercase d
[00:07:30.280 - 00:07:32.240] is the lambda times uppercase d.
[00:07:32.240 - 00:07:34.760] So it can be just using the transformation matrix
[00:07:34.760 - 00:07:37.640] we've already defined on the previous page.
[00:07:37.640 - 00:07:41.800] And in our, so this here is a vector of deflections
[00:07:41.800 - 00:07:42.840] and global coordinates.
[00:07:42.840 - 00:07:45.600] So it's broken up into the x and y components.
[00:07:45.600 - 00:07:52.180] And then these are the two that align with the element like this.
[00:07:52.180 - 00:07:58.500] So we've got the uppercase d is the lambda e transposed
[00:07:58.500 - 00:07:59.620] times the log sde.
[00:08:02.740 - 00:08:07.940] So we know that to go from uppercase d to log sd,
[00:08:07.940 - 00:08:09.700] we use lambda.
[00:08:09.700 - 00:08:13.540] Now to go the other way from log sd to uppercase d,
[00:08:13.540 - 00:08:16.780] we're saying here that you lambda transposed.
[00:08:16.780 - 00:08:20.340] Now that one will be re-enjoyed of because you
[00:08:20.340 - 00:08:23.540] cannot do the opposite to what the lambda matrix does.
[00:08:23.540 - 00:08:25.940] And it may be very thin thing.
[00:08:25.940 - 00:08:27.140] And I think that this is a student.
[00:08:27.140 - 00:08:30.740] This is where I thought, if lambda does the transverse at one
[00:08:30.740 - 00:08:32.100] way, why is it lambda inverse?
[00:08:32.100 - 00:08:34.060] Because we used to come up the matrix inverse
[00:08:34.060 - 00:08:37.580] doing the opposite of what the base matrix does.
[00:08:37.580 - 00:08:40.660] So to me, there's a quite non-discretion.
[00:08:40.660 - 00:08:43.740] Why not the inverse?
[00:08:43.740 - 00:08:47.100] Well, a good starting point is that the matrix is not
[00:08:47.100 - 00:08:47.420] square.
[00:08:47.420 - 00:08:48.620] It's rectangular.
[00:08:48.620 - 00:08:51.780] So that means if we try to calculate a matrix inverse,
[00:08:51.780 - 00:08:52.900] it doesn't exist.
[00:08:52.900 - 00:08:55.380] So that's a good start to say, well, why
[00:08:55.380 - 00:08:57.780] we don't use the inverse if it doesn't exist.
[00:08:57.780 - 00:09:00.860] But it doesn't necessarily tell us why lambda transpose is
[00:09:00.860 - 00:09:02.780] correct.
[00:09:02.780 - 00:09:05.100] So let's look at lambda transposed.
[00:09:05.100 - 00:09:06.860] If we just basically, the transpose
[00:09:06.860 - 00:09:10.060] will be essentially flipping the rows and columns
[00:09:10.060 - 00:09:11.540] about the main diagonal.
[00:09:11.540 - 00:09:16.580] And this here is our lambda for a given element.
[00:09:16.580 - 00:09:21.380] So we say that lambda e.
[00:09:21.380 - 00:09:30.620] And then this matrix here is the lambda e transposed.
[00:09:30.620 - 00:09:33.500] So if we simply switch the rows and columns,
[00:09:33.500 - 00:09:38.020] and we get this sort of width written
[00:09:38.020 - 00:09:41.500] this equation in a full matrix form.
[00:09:41.500 - 00:09:44.060] And what we can do there is we can just go through line by line.
[00:09:44.060 - 00:09:46.380] Remember when you do the matrix multiplication,
[00:09:46.380 - 00:09:48.660] across the row and down a column.
[00:09:48.660 - 00:09:51.860] So the first equation is the upper sD1 is equal to lower
[00:09:51.860 - 00:09:55.380] sD1 cos alpha plus zero times d2.
[00:09:55.380 - 00:09:58.100] And just writing these four equations just
[00:09:58.100 - 00:09:59.940] writing each of these out individually,
[00:09:59.940 - 00:10:04.990] rather than having them combined within the matrix.
[00:10:04.990 - 00:10:09.430] And what you can see here is that the d1 is just the upper
[00:10:09.430 - 00:10:13.230] sD1 is lower sD1 times cos alpha.
[00:10:13.230 - 00:10:16.870] Up sD2 is the lower sD1 times sine alpha.
[00:10:16.870 - 00:10:20.470] And in the same thing can be applied at node 2.
[00:10:20.470 - 00:10:25.230] So I do fully appreciate that it may not be
[00:10:25.230 - 00:10:28.150] immediately obvious why you're using the transpose
[00:10:28.150 - 00:10:29.390] and not be in this.
[00:10:29.390 - 00:10:31.910] But hopefully this gives you some confidence
[00:10:31.910 - 00:10:36.710] that both this equation and this equation are correct.
[00:10:36.710 - 00:10:38.230] And they can have multiple sense.
[00:10:38.230 - 00:10:41.790] If we go through them, we do the form matrix equation
[00:10:41.790 - 00:10:43.110] and we expand the now.
[00:10:43.110 - 00:10:46.190] It just reverse back to basic tree on the tree
[00:10:46.190 - 00:10:49.620] that we all know and love.
[00:10:49.620 - 00:10:57.570] So that's a key point here.
[00:10:57.570 - 00:11:00.010] So next thing we want to do is just go back to this problem.
[00:11:00.010 - 00:11:02.490] We started doing this problem before.
[00:11:02.490 - 00:11:04.730] But we abandoned it because we didn't have the tools
[00:11:04.730 - 00:11:07.090] we needed to do it.
[00:11:07.090 - 00:11:16.900] Now we have the tools to be able to transform the coordinates.
[00:11:16.900 - 00:11:27.410] So just remove here the degree of freedom assignment.
[00:11:27.410 - 00:11:30.890] Refer back to page 33.
[00:11:30.890 - 00:11:35.100] So that was when we assigned the degrees of freedom.
[00:11:35.100 - 00:11:36.980] So there's the potential for two non-zero space
[00:11:36.980 - 00:11:39.300] since that's why we've put two degrees of freedom here
[00:11:39.300 - 00:11:44.650] but not here or here.
[00:11:44.650 - 00:11:48.330] The first thing we've got here is element 1.
[00:11:48.330 - 00:11:52.290] So we have our local coordinates, low sD1, low sD2.
[00:11:52.290 - 00:11:54.170] And then we have our global coordinates,
[00:11:54.170 - 00:11:59.830] components, fst1, d2, d3, and d4.
[00:11:59.830 - 00:12:01.870] And then the transformation matrix.
[00:12:01.870 - 00:12:04.110] So the key thing in here is that the transformation matrix
[00:12:04.110 - 00:12:08.830] is a completely general form that applies to all bar elements.
[00:12:08.830 - 00:12:10.990] And you just got to put your corresponding w of alpha
[00:12:10.990 - 00:12:15.510] run and your guess the corresponding matrix.
[00:12:15.510 - 00:12:20.000] In this case, the transformation angle.
[00:12:20.000 - 00:12:32.620] So these align, these coordinate axes align.
[00:12:32.620 - 00:12:35.460] So that tells us that alpha for element 1.
[00:12:35.460 - 00:12:40.100] is equal to 0 degrees.
[00:12:40.100 - 00:12:44.300] Once we put an alpha of 0 degrees into this equation,
[00:12:44.300 - 00:12:45.420] the cosine terms go to 1.
[00:12:45.420 - 00:12:46.540] And the sine terms go to 0.
[00:12:46.540 - 00:12:50.850] And this is our transformation matrix.
[00:12:50.850 - 00:12:54.170] Now for element 2, just a quick reminder here.
[00:12:54.170 - 00:12:56.210] Our time convention is that we always
[00:12:56.210 - 00:13:00.130] start aligned with xg.
[00:13:00.130 - 00:13:02.170] And we rotate counterclockwise until we're
[00:13:02.170 - 00:13:03.090] aligned with an element.
[00:13:03.090 - 00:13:04.810] So here we start.
[00:13:04.810 - 00:13:07.210] Our monthly, we rotate counterclockwise.
[00:13:07.210 - 00:13:09.610] We're going to 90 degrees.
[00:13:09.610 - 00:13:11.930] We have through 180 degrees.
[00:13:11.930 - 00:13:14.170] And we've got through 270 degrees.
[00:13:14.170 - 00:13:17.410] Now the pin's pointing in the direction of xc.
[00:13:17.410 - 00:13:24.370] So this angle here is the value of plus 170 degrees.
[00:13:24.370 - 00:13:27.370] We could equally call it minus 19,
[00:13:27.370 - 00:13:29.010] but we can't call it plus 90.
[00:13:29.010 - 00:13:31.370] If we call it plus 90, that would be an element.
[00:13:31.370 - 00:13:32.890] We had with pointing upwards.
[00:13:32.890 - 00:13:37.810] And the coordinate for the element was
[00:13:37.810 - 00:13:41.410] with x upwards and y to the left.
[00:13:41.410 - 00:13:42.810] Once we have that equation, again, we just
[00:13:42.810 - 00:13:43.890] drop it into the equation.
[00:13:43.890 - 00:13:46.730] We, the sine terms go to negative 1.
[00:13:46.730 - 00:13:48.410] The cosine terms go to 0.
[00:13:48.410 - 00:13:51.090] And that's our transformation matrix.
[00:13:51.090 - 00:13:52.850] So all we have to do is just define the transformation
[00:13:52.850 - 00:13:53.450] angle.
[00:13:53.450 - 00:13:55.690] We fire that into our code.
[00:13:55.690 - 00:13:59.750] And everything falls out the way it needs to be.
[00:13:59.750 - 00:14:01.910] We have our element, local deflections.
[00:14:01.910 - 00:14:05.350] So d here.
[00:14:05.350 - 00:14:12.500] So one thing that's important here,
[00:14:12.500 - 00:14:24.950] show the pin on the floor, as the superscript
[00:14:24.950 - 00:14:44.310] refers to the element number.
[00:14:44.310 - 00:14:54.780] And then the subscripts here, they refer to the degree
[00:14:54.780 - 00:15:01.970] of freedom number within that element.
[00:15:01.970 - 00:15:12.120] Be very clear.
[00:15:12.120 - 00:15:28.430] D2 1 is the second local to greater freedom.
[00:15:29.430 - 00:15:53.410] In local coordinates, 1.
[00:15:53.410 - 00:15:55.410] If we did the multiplication, what we would get
[00:15:55.410 - 00:15:58.530] is because these are just ones zeros in here,
[00:15:58.530 - 00:16:00.170] it would just be reassigning values.
[00:16:00.170 - 00:16:03.170] It wouldn't actually be scaling or transform anything.
[00:16:03.170 - 00:16:05.890] It would just be reassigning the locations.
[00:16:05.890 - 00:16:13.130] So this matrix multiplication here has the implicit property
[00:16:13.130 - 00:16:15.250] that it would take d1.
[00:16:15.250 - 00:16:18.930] So up to d1, element 1, and align that
[00:16:18.930 - 00:16:21.410] into that into the location within the vector.
[00:16:21.410 - 00:16:25.370] And then we take the third upper case degree of freedom
[00:16:25.370 - 00:16:27.690] up to d1 and put that in here.
[00:16:27.690 - 00:16:29.730] So that is essentially referring back
[00:16:29.730 - 00:16:33.570] to your diagram here where your upper case d1
[00:16:33.570 - 00:16:37.410] is aligned with your lower case d1 and your upper case d3
[00:16:37.410 - 00:16:39.370] is aligned with your lower case d2.
[00:16:39.370 - 00:16:43.290] So you could look at that and manually create that.
[00:16:43.290 - 00:16:45.090] But actually, the transformation
[00:16:45.090 - 00:16:47.130] make it smell good that would have made before you see
[00:16:47.130 - 00:16:50.530] that industry have to do that manually.
[00:16:50.530 - 00:16:56.940] When we look at element 2, so lower case d1 and lower case
[00:16:56.940 - 00:17:00.740] 2 always align with the x-axis for the element.
[00:17:00.740 - 00:17:04.100] So in this case, the x-axis is pointing downwards.
[00:17:04.100 - 00:17:11.180] So then lower case d1 and lower case d2 also point downwards.
[00:17:11.180 - 00:17:14.020] Because the upper case d1 and d2 are always aligned
[00:17:14.020 - 00:17:19.420] with xj and yj, the lower case d1 is horizontal to the right
[00:17:19.420 - 00:17:22.420] and the upper case d2 is good if it upwards and equivalent
[00:17:22.420 - 00:17:24.460] that node 2.
[00:17:24.460 - 00:17:26.340] So that details us if we would have manually
[00:17:26.340 - 00:17:27.340] create this.
[00:17:27.340 - 00:17:30.780] That d1, the first local degree of freedom
[00:17:30.780 - 00:17:36.180] for element 2, is equal to the minus of the upper case d2
[00:17:36.180 - 00:17:37.820] for the element.
[00:17:37.820 - 00:17:41.860] And equal here, the lower case d2 is equal to the minus
[00:17:41.860 - 00:17:44.180] of d4 for element 2.
[00:17:44.180 - 00:17:46.340] So we could manually assign that, but actually
[00:17:46.340 - 00:17:49.380] the transformation matrix is going to do a hard work for us.
[00:17:50.100 - 00:17:52.220] Once we have defined that, we can just do it in a small
[00:17:52.220 - 00:17:55.580] application and it will sort of be thing out for us.
[00:17:55.580 - 00:17:59.460] If the element was at some 23 degrees from vertical,
[00:17:59.460 - 00:18:01.180] it wouldn't just be re-siding values or would actually
[00:18:01.180 - 00:18:06.340] be scaling and taking portions of displacements.
[00:18:06.340 - 00:18:09.340] And this would be a much more complex matrix.
[00:18:09.340 - 00:18:11.780] If you have values that weren't 0 or 1 in here,
[00:18:11.780 - 00:18:14.020] and you'd have numbers in here, that weren't
[00:18:14.020 - 00:18:18.410] represented in here.
[00:18:18.410 - 00:18:20.650] The element forcing terms, you've got a vector of 4
[00:18:20.690 - 00:18:24.090] forces, these are the forces in global coordinates.
[00:18:24.090 - 00:18:27.170] These are as they're drawn here of the upper case f's.
[00:18:27.170 - 00:18:31.210] And then we can also say what they would look like for the
[00:18:31.210 - 00:18:34.450] lower case f's, how they would fit into that larger forcing
[00:18:34.450 - 00:18:36.410] vector matrix.
[00:18:36.410 - 00:18:44.300] That's what's larger forcing vector.
[00:18:44.300 - 00:18:49.180] So we now have the information that explains the degrees
[00:18:49.180 - 00:18:53.060] of re-inferri-challiments and local coordinates, and how
[00:18:53.060 - 00:18:58.080] they cross ones to the global degrees of freedom.
[00:18:58.080 - 00:19:01.160] We can use the information that we obtained on the piece
[00:19:01.160 - 00:19:03.000] page is to define all this.
[00:19:03.000 - 00:19:05.800] So we've got down little two by two.
[00:19:05.800 - 00:19:10.400] We've got the way of transforming the little two by two
[00:19:10.400 - 00:19:13.400] and local coordinates into using a transformation matrix
[00:19:13.400 - 00:19:16.680] pre-enpose multiplying to get our ku hat.
[00:19:16.680 - 00:19:19.840] So our ku hat is the element stiffness matrix in global
[00:19:19.840 - 00:19:20.440] coordinates.
[00:19:20.440 - 00:19:26.200] Our ku is the element stiffness matrix in the local coordinates.
[00:19:26.200 - 00:19:30.000] So we'll only get so far.
[00:19:30.040 - 00:19:32.240] The equation for each element is still independent from our
[00:19:32.240 - 00:19:33.440] balance.
[00:19:33.440 - 00:19:35.840] It doesn't include information about how these elements
[00:19:35.840 - 00:19:38.800] connect to each other or how they connect to support
[00:19:38.800 - 00:19:41.700] points and boundaries.
[00:19:41.700 - 00:19:45.020] So if we're going to solve the overall system, we need
[00:19:45.020 - 00:19:49.490] this one piece of information that's missing.
[00:19:49.490 - 00:19:53.530] So these are our forcing terms, our prediction terms, and
[00:19:53.530 - 00:19:55.970] our stiffness matrix all in global coordinates.
[00:19:55.970 - 00:19:58.010] But we also know that there's this upper case q, the
[00:19:58.010 - 00:20:01.250] lower case q, and it's going to be some sort of kg.
[00:20:01.250 - 00:20:03.930] That kg is our global stiffness matrix.
[00:20:03.930 - 00:20:06.770] And then includes all the information about every element,
[00:20:06.770 - 00:20:09.730] their geometric and material properties, their
[00:20:09.730 - 00:20:14.090] orientation, and their connectivity into the structure.
[00:20:14.090 - 00:20:15.970] And it's that final piece, that connectivity that we
[00:20:15.970 - 00:20:20.240] don't have in the captured.
[00:20:20.240 - 00:20:22.640] So we've got this is just a summary of the equations we've
[00:20:22.640 - 00:20:24.960] developed to this point.
[00:20:24.960 - 00:20:32.600] We know that our kg, that can be defined as simply equal to
[00:20:32.600 - 00:20:36.120] the sum of our assembly matrix times the ke, times
[00:20:36.120 - 00:20:37.520] the assembly matrix transposed.
[00:20:37.520 - 00:20:40.360] And what we have in here defined is just what is a
[00:20:40.360 - 00:20:43.340] assembly matrix.
[00:20:43.340 - 00:20:47.500] What the assembly matrix is essentially a matrix of zeros and
[00:20:47.500 - 00:20:54.460] ones that maps or transform, translates locations within
[00:20:54.460 - 00:20:58.860] an element into locations for the overall structure.
[00:20:58.860 - 00:21:03.100] So this is what the assembly matrix does in maps,
[00:21:03.140 - 00:21:06.540] forces of space-max from local and global coordinates and
[00:21:06.540 - 00:21:09.380] up to the overall structure.
[00:21:09.380 - 00:21:16.340] So what we've got here is the key thing about assembly
[00:21:16.340 - 00:21:40.100] matrix is that assembly matrices contain only ones, zeros,
[00:21:40.100 - 00:21:49.900] so they don't scale anything.
[00:21:49.900 - 00:22:07.420] They just assign to appropriate locations.
[00:22:07.420 - 00:22:10.300] Now we will go through the next few pages around how do
[00:22:10.300 - 00:22:13.100] we actually define the assembly matrix.
[00:22:13.100 - 00:22:15.540] But initially here we're just going to say look at the size of
[00:22:15.540 - 00:22:17.730] them.
[00:22:17.730 - 00:22:19.890] So the number of columns within the assembly matrix is always
[00:22:19.890 - 00:22:22.850] equal to the number of element degrees of freedom and
[00:22:22.850 - 00:22:24.730] global coordinates.
[00:22:24.730 - 00:22:38.940] So this here is for a given elements type.
[00:22:38.940 - 00:22:49.500] The number of columns is always equal to 4, 4, 8 bar
[00:22:49.500 - 00:22:54.260] elements.
[00:22:54.300 - 00:22:58.460] So on the previous page, there was two components of
[00:22:58.460 - 00:23:01.180] the 16.0, 4 in total.
[00:23:01.180 - 00:23:04.220] That's why there's four columns, two assembly matrix for
[00:23:04.220 - 00:23:08.660] a bar element.
[00:23:08.660 - 00:23:11.460] Now the number of rows is equal to the number of degrees of
[00:23:11.460 - 00:23:14.590] freedom in the overall structure.
[00:23:14.590 - 00:23:15.470] But that varies.
[00:23:15.470 - 00:23:17.510] So that varies on the particular problem.
[00:23:17.510 - 00:23:36.210] So in this specific problem, it's too that this can be
[00:23:36.210 - 00:23:48.500] very with different structures.
[00:23:48.500 - 00:23:52.260] So as long as you use environments, and we will go to other
[00:23:52.260 - 00:23:54.140] elements that have more degrees of freedom in there for
[00:23:54.140 - 00:23:56.700] have more columns and assembly matrix.
[00:23:56.700 - 00:23:59.660] But a bar element structure using the element type that we've
[00:23:59.660 - 00:24:03.260] derived, there will always be four columns.
[00:24:03.260 - 00:24:06.340] But the number of rows does vary based upon the size of the
[00:24:06.340 - 00:24:10.020] problem and the total number of degrees of freedom that the
[00:24:10.020 - 00:24:18.670] problem has.
[00:24:18.670 - 00:24:21.190] Just going to go back to this problem.
[00:24:21.190 - 00:24:25.990] And we're going to work through and work out how to define
[00:24:25.990 - 00:24:36.360] in assembly matrix for a given problem.
[00:24:36.360 - 00:24:37.800] Now just thinking I'm going to do it's just quickly
[00:24:37.800 - 00:24:40.720] reschedule the diagram just that we have it there for a
[00:24:40.720 - 00:24:43.430] reference.
[00:24:43.430 - 00:24:59.950] So the overall problem that we did in the left, this is the
[00:24:59.950 - 00:25:02.070] overall structure before we've broken that up into
[00:25:02.070 - 00:25:03.470] elements.
[00:25:03.470 - 00:25:05.390] Now, no degrees of freedom here or here, because that
[00:25:05.390 - 00:25:06.670] fully constrained by the pen.
[00:25:06.670 - 00:25:08.830] There's no potential in any non-zero displacement, either
[00:25:08.830 - 00:25:10.430] the location.
[00:25:10.430 - 00:25:15.430] And therefore, we've got q1.
[00:25:15.430 - 00:25:18.430] So our lowercase q1, that's the degree of freedom, how much
[00:25:18.430 - 00:25:20.190] the node moves horizontally.
[00:25:20.190 - 00:25:23.230] And the uppercase q1 is the value of the applied
[00:25:23.230 - 00:25:25.910] external y-d exists there.
[00:25:25.910 - 00:25:30.190] And there's a corresponding set of q2, lowercase q2.
[00:25:30.190 - 00:25:34.580] And our uppercase q2 there.
[00:25:34.580 - 00:25:39.380] So when it comes to generating an assembly matrix, this is
[00:25:39.380 - 00:25:42.620] the one step in the process that is a little manual, and
[00:25:42.620 - 00:25:46.460] will remain a little bit manual throughout this course.
[00:25:46.460 - 00:25:48.260] There is a way you can go in and you can sort of
[00:25:48.260 - 00:25:50.420] automate this process, but it involves a lot more
[00:25:50.420 - 00:25:53.660] sort of iterations and looping and a whole lot more
[00:25:53.660 - 00:25:55.620] level of coding, which we just don't really have time to
[00:25:55.620 - 00:25:56.820] cover in the four weeks.
[00:25:56.820 - 00:26:01.500] So the step still does everything, but it is just a much
[00:26:01.500 - 00:26:04.820] simpler way of setting this up.
[00:26:04.820 - 00:26:06.740] So what we have here, when we are starting the assembly
[00:26:06.780 - 00:26:09.980] matrix, we essentially have the degrees of freedom for the
[00:26:09.980 - 00:26:13.060] element in global coordinates across the top.
[00:26:13.060 - 00:26:16.540] And we have our global degrees of freedom, these things
[00:26:16.540 - 00:26:18.820] down the left-hand side.
[00:26:18.820 - 00:26:21.020] And what we want to do is look at the local degrees of
[00:26:21.020 - 00:26:24.940] freedom, but the element degrees of freedom in global
[00:26:24.940 - 00:26:27.460] coordinates, and we want to see how they map across onto
[00:26:27.460 - 00:26:30.750] the overall structure.
[00:26:30.750 - 00:26:34.510] When there's a, when the two correspond, we put a one
[00:26:34.510 - 00:26:37.190] into the matrix, and if there's no relationship, we put a
[00:26:37.190 - 00:26:39.310] zero.
[00:26:39.310 - 00:26:40.990] So it's solid here.
[00:26:40.990 - 00:26:44.630] At the left-hand node, we have our capacity one and our
[00:26:44.630 - 00:26:49.670] capacity two, and they correspond to the snow here.
[00:26:49.670 - 00:26:53.230] And there's no allowable degrees of freedom here.
[00:26:53.230 - 00:26:56.950] So if we look here at D1, the element one, and at D2,
[00:26:56.950 - 00:27:03.980] the element one, that all zero, that all zero cons.
[00:27:03.980 - 00:27:07.500] The reason they call it all zero is there's no global
[00:27:07.500 - 00:27:09.900] degrees of freedom, which corresponds to either of these
[00:27:09.900 - 00:27:14.490] values, so that's why those columns remain zero.
[00:27:14.490 - 00:27:22.400] When we look at the second node, we have this D3, and we
[00:27:22.400 - 00:27:29.600] have this Q1, and we know that this here relates to this here.
[00:27:29.600 - 00:27:34.520] So it's the horizontal defection at this nodal point,
[00:27:34.520 - 00:27:37.560] in the horizontal direction.
[00:27:37.560 - 00:27:40.160] So what that tells us is the weirdos, two and six, we
[00:27:40.160 - 00:27:44.040] have D3, the element one, and Q1, and we have those two
[00:27:44.040 - 00:27:52.540] intersect, we put a one in the matrix at that location.
[00:27:52.540 - 00:27:59.260] Now D4, 4, 1, 1, and cross in that, is at the same location
[00:27:59.260 - 00:28:04.180] and in the same direction as our Q2.
[00:28:04.180 - 00:28:07.780] So then when D4, the element one comes down, and Q2 comes in
[00:28:07.780 - 00:28:12.660] here, that's where we put the one from the diagonal there.
[00:28:12.660 - 00:28:16.500] What is saying mathematically that one symbolizes that
[00:28:16.500 - 00:28:19.940] this quantity is equal to this quantity, and this quantity
[00:28:19.940 - 00:28:22.540] is equal to this quantity.
[00:28:22.540 - 00:28:25.180] Now because we're dealing with the element of degrees of
[00:28:25.180 - 00:28:28.460] freedom in global coordinates, things always align.
[00:28:28.460 - 00:28:31.860] Either they match exactly, or they don't match at all,
[00:28:31.860 - 00:28:34.220] which is why this is only zero's and ones in here.
[00:28:34.220 - 00:28:36.260] We should never see a value in a seemingly matrix that
[00:28:36.260 - 00:28:40.670] doesn't zero or one.
[00:28:40.670 - 00:28:48.910] Now for element two, we can see that D1 here, and that
[00:28:48.910 - 00:28:54.550] cross ones up to our lower case Q1.
[00:28:54.550 - 00:28:57.590] So that's at the same normal location, and in the same
[00:28:57.590 - 00:29:05.100] direction, so that says that D2 here matches our Q1 there.
[00:29:05.100 - 00:29:08.900] Then we've got our D2, so our second degree of freedom for the
[00:29:08.900 - 00:29:12.220] element, and global coordinates is at this normal point here,
[00:29:12.220 - 00:29:13.900] and it points upwards.
[00:29:13.900 - 00:29:19.620] Therefore we have this relationship between D2 and Q2,
[00:29:19.620 - 00:29:26.060] and that's why we put a one under that matrix there.
[00:29:26.060 - 00:29:28.980] D3 and D4 cross one to this node.
[00:29:28.980 - 00:29:30.660] There's no global difference between here and all,
[00:29:30.660 - 00:29:33.900] because it's fully constrained, which is why we have two
[00:29:33.900 - 00:29:37.100] all zero columns here, because there's nothing
[00:29:37.100 - 00:29:40.500] neither of these values cross ones to these.
[00:29:40.500 - 00:29:45.470] So that gives us why the zero's there.
[00:29:45.470 - 00:29:48.670] And doing that, it's really not immediately obvious to you,
[00:29:48.670 - 00:29:50.950] but in doing that, putting those zero's in there,
[00:29:50.950 - 00:29:53.470] that's the way that we actually introduced the information that
[00:29:53.470 - 00:29:55.550] those nodes are constrained.
[00:29:55.550 - 00:29:57.350] It seems like it's really kind of perhaps available
[00:29:57.350 - 00:30:03.070] after doing it, but that's what an all-zero column is
[00:30:03.070 - 00:30:05.670] essentially telling them a mathematical system.
[00:30:05.670 - 00:30:08.390] That degree of freedom for that element is fully constrained
[00:30:08.390 - 00:30:11.730] and can't move.
[00:30:11.730 - 00:30:18.730] Now, just as a quite summary, this is the information here
[00:30:18.730 - 00:30:21.610] that we've talked about, and that's the information that's
[00:30:21.610 - 00:30:24.890] contained within this matrix.
[00:30:24.890 - 00:30:28.210] And likewise, this is the information here
[00:30:28.210 - 00:30:33.290] that's contained as being conveyed by these numbers
[00:30:33.290 - 00:30:34.570] within the matrix.
[00:30:34.570 - 00:30:41.780] So also moved out quickly there.
[00:30:41.780 - 00:30:55.310] The D3, the element 2, and D4, the element 2 are fully constrained.
[00:30:55.310 - 00:31:00.550] That's also an implicit message that's being conveyed
[00:31:00.550 - 00:31:03.840] through that assembly matrix.
[00:31:03.840 - 00:31:05.640] So there's a bit of a manual step.
[00:31:05.640 - 00:31:07.600] And that assembly matrix is important,
[00:31:07.600 - 00:31:09.520] because that's the key step that introduces
[00:31:09.520 - 00:31:11.360] that connectivity information.
[00:31:11.360 - 00:31:13.960] That tells the mathematical system how
[00:31:13.960 - 00:31:15.840] the elements are connected to each other,
[00:31:15.840 - 00:31:17.760] and how that can exist to support points.
[00:31:17.760 - 00:31:19.440] And that's the key piece of information
[00:31:19.440 - 00:31:20.280] that we've been missing.
[00:31:20.280 - 00:31:23.320] That's the thing that now gives us a, before we
[00:31:23.320 - 00:31:25.800] have a singular matrix, we couldn't get a unique solution.
[00:31:25.800 - 00:31:27.680] Once we introduced this information,
[00:31:27.680 - 00:31:29.840] we now get a unique solution.
[00:31:29.840 - 00:31:31.720] The matrix is full rank.
[00:31:31.720 - 00:31:34.360] NP.lenel.zole will get us something useful,
[00:31:34.360 - 00:31:37.960] rather just splitting up a bunch of red text.
[00:31:37.960 - 00:31:42.720] And that's the key step.
[00:31:42.720 - 00:31:44.920] Now our upper-case queue, that's our external,
[00:31:44.920 - 00:31:47.280] a polystonal loads, our upper-case queue one,
[00:31:47.280 - 00:31:49.240] and our upper-case queue two.
[00:31:49.240 - 00:31:53.240] And that is equal to the summation from equal one
[00:31:53.240 - 00:31:55.280] to the number of elements of the assembly matrix
[00:31:55.280 - 00:31:56.360] that has the force in terms.
[00:31:56.360 - 00:31:58.200] So these are the two assembly matrices
[00:31:58.200 - 00:31:59.640] we're just defined above.
[00:31:59.640 - 00:32:00.960] These are the forcing vectors.
[00:32:00.960 - 00:32:03.560] And if we were to sum, multiply that through.
[00:32:03.560 - 00:32:06.880] That's what tells us there is that.
[00:32:06.880 - 00:32:11.920] The first one, the queue one, is equal to the summation
[00:32:11.920 - 00:32:16.480] of F3 for element one and F1 for element two.
[00:32:16.480 - 00:32:19.320] So it's basically saying if you add those two forces together,
[00:32:19.320 - 00:32:22.160] which are the internal element reactions,
[00:32:22.160 - 00:32:28.120] that equals to the sums up to be the applied external load.
[00:32:28.120 - 00:32:31.560] And likewise, if we looked at D4 for element one
[00:32:31.560 - 00:32:34.840] and D2 for element two, we add those forces together,
[00:32:34.840 - 00:32:37.880] that will add up to being Q2.
[00:32:37.880 - 00:32:40.800] So that's the, we don't just have to do that manually.
[00:32:40.800 - 00:32:43.400] The assembly matrices will do that for us.
[00:32:43.400 - 00:32:45.080] We've already done the hard work
[00:32:45.080 - 00:32:46.800] by generating the assembly matrix.
[00:32:46.800 - 00:32:48.600] We can now get that to do the job for us.
[00:32:48.600 - 00:32:51.840] We don't have to manually determine us
[00:32:51.840 - 00:32:53.960] that the assembly matrix will do.
[00:32:54.600 - 00:32:57.880] So what is saying is that any given node,
[00:32:57.880 - 00:33:01.680] the summation of all the element forces
[00:33:01.680 - 00:33:04.320] that the internal forces of all the elements
[00:33:04.320 - 00:33:07.360] that connect them to that node are equal
[00:33:07.360 - 00:33:08.760] to the applied external load.
[00:33:08.760 - 00:33:10.560] And if the applied external load is zero,
[00:33:10.560 - 00:33:12.160] then there's number zero.
[00:33:12.160 - 00:33:16.530] The overall structure is the first matrix,
[00:33:16.530 - 00:33:18.650] which we refer to as the global stiffness matrix
[00:33:18.650 - 00:33:22.210] can be found by using the assembly element,
[00:33:22.730 - 00:33:26.290] a similar element, global stiffness matrices.
[00:33:26.290 - 00:33:28.290] So that we use the assembly matrix that we've defined.
[00:33:28.290 - 00:33:30.530] We pre-moped by the assembly matrix.
[00:33:30.530 - 00:33:33.690] We post-moped by the assembly matrix transposed.
[00:33:33.690 - 00:33:38.690] Our K1 hat is our assembly element stiffness matrix
[00:33:38.690 - 00:33:39.890] in global coordinates.
[00:33:39.890 - 00:33:42.690] And then, so basically this piece here
[00:33:43.930 - 00:33:46.910] is what we refer to as Kg1.
[00:33:47.550 - 00:33:51.910] And this piece here is Kg2.
[00:33:52.790 - 00:33:57.230] So what this is is this is element one's contribution
[00:33:57.230 - 00:33:59.750] to the global stiffness matrix.
[00:33:59.750 - 00:34:03.510] This piece here is element two's contribution
[00:34:03.510 - 00:34:06.110] to the global stiffness matrix.
[00:34:06.110 - 00:34:07.870] And if the machine elements did be tinnellies
[00:34:07.870 - 00:34:12.440] that we had together.
[00:34:12.440 - 00:34:16.000] So just a quick recap as to what the sphere
[00:34:16.000 - 00:34:21.000] was this K hat is the transformation matrix
[00:34:23.040 - 00:34:26.680] transposed times Ke, which is that two by two times
[00:34:26.680 - 00:34:31.420] our transformation matrix.
[00:34:31.420 - 00:34:33.020] Now one thing just to be a wheel here
[00:34:34.860 - 00:34:52.510] is that note the difference between A,
[00:34:52.510 - 00:35:02.140] E, which is the assembly matrix,
[00:35:02.140 - 00:35:18.380] then which is the transformation matrix.
[00:35:18.380 - 00:35:23.720] They are similar looking symbols, but they are different.
[00:35:23.720 - 00:35:25.120] Yeah, the other question you might ask to me
[00:35:25.120 - 00:35:26.360] is well, why didn't you just use someone?
[00:35:26.360 - 00:35:27.480] It was wildly different.
[00:35:28.600 - 00:35:31.160] And I could, but the fact is that this is a fairly
[00:35:31.160 - 00:35:33.720] common sign connection across a lot of texts.
[00:35:33.720 - 00:35:35.880] So globally, that's a pretty common
[00:35:36.880 - 00:35:39.040] consistent, recognized sign convention.
[00:35:39.040 - 00:35:41.840] So that's why I've used it just to be consistent.
[00:35:41.840 - 00:35:46.080] If you're looking at Wikipedia or a subsequent text
[00:35:46.080 - 00:35:47.640] that you can sort of see the relationship.
[00:35:48.160 - 00:35:50.520] I am also aware that they do look
[00:35:50.520 - 00:35:56.480] a little bit similar to this trying to highlight that difference.
[00:35:56.480 - 00:36:02.490] So we have here is our Kg.
[00:36:02.490 - 00:36:09.350] This is the overall global stiffness matrix
[00:36:18.960 - 00:36:27.400] that represents the full structure.
[00:36:27.400 - 00:36:41.850] It includes all information about all balance
[00:36:41.850 - 00:37:02.160] and the connectivity.
[00:37:02.160 - 00:37:05.480] So we have our little Ke, the two by two,
[00:37:05.520 - 00:37:08.360] that is just geometric material properties.
[00:37:09.280 - 00:37:12.280] Once we transform that, we get our Ke hat.
[00:37:12.280 - 00:37:15.000] And that Ke hat is geometric material properties
[00:37:15.000 - 00:37:18.880] and elementarion and orientation information.
[00:37:20.320 - 00:37:24.720] Then we have our Kg, which is this Kd1 and Kg2.
[00:37:24.720 - 00:37:29.120] That includes all the information about element connectivity,
[00:37:29.120 - 00:37:31.720] orientation, geometric material properties
[00:37:31.720 - 00:37:32.920] for a given element.
[00:37:33.840 - 00:37:35.920] And then once we sum those up across the number of elements,
[00:37:35.920 - 00:37:38.760] we have Kg, which is every piece of information
[00:37:38.760 - 00:37:44.720] that we need to be able to solve the system.
[00:37:44.720 - 00:37:45.920] So we've got that there.
[00:37:47.200 - 00:37:48.520] The next step is to actually go through
[00:37:48.520 - 00:37:54.870] and sort of do the solution.
[00:37:54.870 - 00:37:59.870] So our element one, our Kg hat,
[00:37:59.870 - 00:38:02.710] transformation matrix and zero degrees.
[00:38:02.710 - 00:38:04.910] A transformation angle is zero degrees here.
[00:38:04.950 - 00:38:09.910] A transformation is minus 90 or plus 270 degrees.
[00:38:11.750 - 00:38:15.710] And then that's the Ke one hat and the Kg two hat.
[00:38:15.710 - 00:38:17.030] We can use these assembly matrices
[00:38:17.030 - 00:38:18.750] with to find on the previous page.
[00:38:18.750 - 00:38:20.550] We had to derive those.
[00:38:21.630 - 00:38:24.350] We do the multiplication and then this is the components
[00:38:24.350 - 00:38:25.190] here and here.
[00:38:26.190 - 00:38:28.230] This is element one's contribution to Kg
[00:38:28.230 - 00:38:30.110] and this is element two's contribution.
[00:38:30.110 - 00:38:33.430] We sum them here there and it gets our overall Kg.
[00:38:33.470 - 00:38:39.120] In this case it is a pretty small matrix.
[00:38:39.120 - 00:38:41.040] So one thing to note here,
[00:38:42.840 - 00:38:59.140] the overall Kg is always square with dimensions.
[00:39:00.620 - 00:39:07.640] In by in, we are in is equal to the number
[00:39:11.550 - 00:39:29.400] of global degrees of freedom of the structure,
[00:39:29.400 - 00:39:36.680] the Q values.
[00:39:36.680 - 00:39:38.080] One thing we've done here is group this.
[00:39:38.080 - 00:39:45.780] So this is assuming E one equals E two equals E
[00:39:45.940 - 00:39:50.940] E A one equals A two equals A and L one equals L two.
[00:39:56.720 - 00:40:00.760] So we're assuming that the two elements
[00:40:00.760 - 00:40:03.760] that frame into there have the same elastic modules
[00:40:03.760 - 00:40:09.450] cross-sectional area in length.
[00:40:09.450 - 00:40:11.010] We can go through and we can solve.
[00:40:13.410 - 00:40:15.970] This is the equation here and we can
[00:40:15.970 - 00:40:18.210] switch that around the use Kg inverse,
[00:40:18.210 - 00:40:21.450] which is this is the inverse of that matrix.
[00:40:21.730 - 00:40:33.380] That's the everything here Kg inverse.
[00:40:33.380 - 00:40:35.020] And then we've got our forcing terms
[00:40:35.020 - 00:40:36.580] and then it's the result that we get.
[00:40:37.860 - 00:40:39.900] Now in this particular instance,
[00:40:39.900 - 00:40:41.100] because we have two elements that are
[00:40:41.100 - 00:40:42.220] peneduated to each other.
[00:40:42.220 - 00:40:44.140] So there's no moment of shared connection
[00:40:44.140 - 00:40:46.300] and that perpendicular to each other.
[00:40:46.300 - 00:40:48.500] We actually know what no off-back or terms.
[00:40:49.500 - 00:40:50.900] And what that means is that we essentially
[00:40:50.900 - 00:40:53.820] have two independent equations within here.
[00:40:55.020 - 00:40:56.260] We could separate them out.
[00:40:57.140 - 00:40:59.540] And we don't actually have to solve them as a matrix system.
[00:41:00.540 - 00:41:02.220] But as soon as we would take one of those elements,
[00:41:02.220 - 00:41:04.380] instead of it being true to elements like this,
[00:41:04.380 - 00:41:05.500] if we inclined one,
[00:41:06.980 - 00:41:09.220] then they won't be in the equations.
[00:41:09.220 - 00:41:11.100] We would see the off- diagonal terms
[00:41:11.100 - 00:41:13.860] become populated with non-zero values.
[00:41:13.860 - 00:41:20.330] And then we would have to solve it as a matrix system.
[00:41:20.330 - 00:41:25.170] Now the key thing here is in any sort of finite element
[00:41:25.570 - 00:41:30.440] analysis.
[00:41:30.440 - 00:41:43.360] This is the point at which these system solved.
[00:41:44.880 - 00:41:47.160] Once we've done this matrix solution
[00:41:47.160 - 00:41:49.280] of a simple case equation,
[00:41:49.280 - 00:41:59.180] that's when we say the system is solved.
[00:41:59.180 - 00:42:23.030] This is the step where we simultaneously calculate
[00:42:25.280 - 00:42:39.880] all degrees of freedom for the structure.
[00:42:39.880 - 00:42:51.400] You need subsequent analysis is called post-processing.
[00:42:57.500 - 00:43:00.300] It's all partly a broader solution.
[00:43:00.300 - 00:43:03.340] But the key thing is that that solution of your matrix
[00:43:03.340 - 00:43:06.980] zero equations using your matrix inverse
[00:43:06.980 - 00:43:08.980] or NP dot LaNal dot solve,
[00:43:09.940 - 00:43:12.220] that's where we've solved for all the degrees of freedom.
[00:43:12.220 - 00:43:14.660] Now we may, we will,
[00:43:14.660 - 00:43:15.620] the open to more detail,
[00:43:15.620 - 00:43:19.060] we'll pull out strains and stresses within elements.
[00:43:19.060 - 00:43:21.380] And we might look at the individual element forces
[00:43:21.380 - 00:43:23.820] and look at the way the forces are developed
[00:43:24.700 - 00:43:26.260] and distributed through the structure.
[00:43:27.260 - 00:43:29.660] But that's the key step we think is solved
[00:43:29.660 - 00:43:32.980] and then we do sort of further in characterization
[00:43:32.980 - 00:43:37.400] and analysis of that.
[00:43:37.400 - 00:43:38.240] So,
[00:43:39.600 - 00:43:40.720] reaction lines,
[00:43:40.720 - 00:43:42.040] that's,
[00:43:42.040 - 00:43:43.440] let's look at something post-processing
[00:43:43.440 - 00:43:47.700] and what it might look like.
[00:43:47.700 - 00:43:49.100] So what about reaction lines?
[00:43:50.060 - 00:43:54.780] If we wanted to know what the required strength
[00:43:54.780 - 00:43:58.140] of these pen supports were to restrain the structure,
[00:43:58.180 - 00:44:01.500] we'd want to know what the forces are.
[00:44:02.820 - 00:44:06.320] And that's the key thing.
[00:44:06.320 - 00:44:07.160] When we do that,
[00:44:07.160 - 00:44:08.720] we look back at our free body diagrams.
[00:44:08.720 - 00:44:10.160] So we have,
[00:44:10.160 - 00:44:11.400] you know, we always start with the structure,
[00:44:11.400 - 00:44:12.480] we break it up into elements,
[00:44:12.480 - 00:44:18.100] then we draw free body diagram of those individual elements.
[00:44:18.100 - 00:44:19.460] In this case,
[00:44:19.460 - 00:44:20.820] forces F1 and F2,
[00:44:20.820 - 00:44:21.180] F4,
[00:44:21.180 - 00:44:22.180] element 1,
[00:44:22.180 - 00:44:24.980] other ones that connect to the support point
[00:44:24.980 - 00:44:27.220] and F3 and F4,
[00:44:27.220 - 00:44:31.800] are the forces that connect to the support point.
[00:44:31.800 - 00:44:34.640] So the question may be,
[00:44:34.640 - 00:44:36.480] why do we need to do free body diagrams?
[00:44:37.920 - 00:44:39.880] One easy answer is that in the test,
[00:44:39.880 - 00:44:42.080] there will be marks for doing that.
[00:44:42.080 - 00:44:44.000] The question is, why is there marks for doing that?
[00:44:44.000 - 00:44:46.120] Well, it's a really key step in terms of building
[00:44:46.120 - 00:44:48.520] up the structure and doing that correctly,
[00:44:48.520 - 00:44:50.080] but also for the D&B element interpret
[00:44:50.080 - 00:44:53.870] and understand the results that you get.
[00:44:53.870 - 00:44:55.390] So this is the equation here,
[00:44:55.390 - 00:44:57.190] key hat is the element's stiffness matrix
[00:44:57.190 - 00:44:58.550] and global coordinates.
[00:45:00.190 - 00:45:03.310] Well, so that's the equation we need
[00:45:03.350 - 00:45:05.870] to use to get these forces.
[00:45:05.870 - 00:45:06.870] But we don't know what D is,
[00:45:06.870 - 00:45:08.230] we don't know what the deflection is
[00:45:08.230 - 00:45:09.830] for the particular element yet.
[00:45:10.830 - 00:45:13.350] Well, what we can use is we can use our assembly matrix.
[00:45:13.350 - 00:45:15.190] We could manually kind of infer and say,
[00:45:15.190 - 00:45:16.870] well, if there's no goes this far,
[00:45:16.870 - 00:45:19.590] that means the element has to stretch by this amount.
[00:45:19.590 - 00:45:21.110] But we actually already have a matrix
[00:45:21.110 - 00:45:22.910] that can do all this for us.
[00:45:22.910 - 00:45:24.350] We've already gone to the effort of building it,
[00:45:24.350 - 00:45:26.070] let's just use it.
[00:45:26.070 - 00:45:27.150] So that's our assembly machine.
[00:45:27.150 - 00:45:29.870] We use the assembly matrix transpose times the Q,
[00:45:30.830 - 00:45:35.230] so the Q is what we can as a result of our solution.
[00:45:35.230 - 00:45:36.710] That will give us the deflection.
[00:45:36.710 - 00:45:38.350] So what this is the matrix will do
[00:45:38.350 - 00:45:40.110] is it will extract relevant pieces
[00:45:40.110 - 00:45:43.630] of that overall deflection vector.
[00:45:44.710 - 00:45:47.110] And it will insert them into the appropriate locations
[00:45:47.110 - 00:45:49.190] within the application D vector.
[00:45:49.190 - 00:45:51.150] And it will do all that for you automatically.
[00:45:52.750 - 00:45:54.670] Then once we've got that,
[00:45:54.670 - 00:45:57.430] we can just pre-multiply by our key hat,
[00:45:58.430 - 00:45:59.270] which is here,
[00:45:59.270 - 00:46:00.990] and then that gives us the forcing vector.
[00:46:00.990 - 00:46:02.670] So it's an extra couple of steps,
[00:46:02.670 - 00:46:03.790] but it's actually really simple.
[00:46:03.790 - 00:46:05.630] It's a really simple equation.
[00:46:05.630 - 00:46:07.390] We can back in into Python.
[00:46:07.390 - 00:46:09.150] We already have all the variables we need,
[00:46:09.150 - 00:46:11.230] and then now we have our forcing vector.
[00:46:12.350 - 00:46:14.110] Here they're for the two elements.
[00:46:14.110 - 00:46:14.950] And from that,
[00:46:14.950 - 00:46:18.230] we can relate them back to the diagram
[00:46:18.230 - 00:46:22.170] and determine our reaction loads.
[00:46:22.170 - 00:46:24.010] So the assembly matrix is really powerful.
[00:46:24.930 - 00:46:26.610] It takes a little bit of time to set it up.
[00:46:26.610 - 00:46:27.890] But once we've got us,
[00:46:27.890 - 00:46:32.280] it is incredibly useful.
[00:46:32.320 - 00:46:34.160] Just some final comments about the method.
[00:46:35.480 - 00:46:36.320] If you simply,
[00:46:36.320 - 00:46:37.160] I'm actually going to say,
[00:46:37.160 - 00:46:38.000] I'm going to add a maximum degrees of freedom
[00:46:38.000 - 00:46:40.560] for the element degree of freedom and global coordinates.
[00:46:42.520 - 00:46:44.440] This is how we always set it up.
[00:46:44.440 - 00:46:47.320] We have the element degrees of freedom
[00:46:47.320 - 00:46:49.440] and global coordinates across the top.
[00:46:49.440 - 00:46:52.400] We have our structural degrees of freedom down the left.
[00:46:52.400 - 00:46:53.640] When they relate to each other,
[00:46:53.640 - 00:46:54.480] we put a one.
[00:46:55.440 - 00:46:56.440] If they don't relate to each other,
[00:46:56.440 - 00:46:57.280] we've got a zero.
[00:46:58.240 - 00:47:01.920] And it should only ever be equal to one since zero.
[00:47:06.150 - 00:47:08.190] Just a quick recap here
[00:47:09.310 - 00:47:14.420] on the two-way diagram.
[00:47:14.420 - 00:47:15.740] We must match the coordinates.
[00:47:15.740 - 00:47:19.420] So the generic case is that Xg is d1 and d3.
[00:47:20.820 - 00:47:22.540] There's no one and no two respectively.
[00:47:22.540 - 00:47:27.540] And then d2 and d4 are the Yg as no one and no two,
[00:47:28.620 - 00:47:29.460] respectively.
[00:47:29.460 - 00:47:32.540] So that is a fixed known feature and approach.
[00:47:33.580 - 00:47:36.060] The reason that's fixed is that the numbers within
[00:47:36.980 - 00:47:40.620] our transformation matrix
[00:47:41.740 - 00:47:43.380] are based upon those number of seconds.
[00:47:43.380 - 00:47:45.660] So if we want to change the number of seconds,
[00:47:45.660 - 00:47:47.300] if we want to go back in time and change,
[00:47:47.300 - 00:47:48.140] choose something different.
[00:47:48.140 - 00:47:49.220] That will be fine.
[00:47:49.220 - 00:47:50.860] The things like our transformation matrix
[00:47:50.860 - 00:47:51.740] and our assembly matrix
[00:47:51.740 - 00:47:52.860] and these things will have changed.
[00:47:52.860 - 00:47:58.390] So we can't mix and match when you just be consistent.
[00:47:58.390 - 00:48:03.470] So local versus global degrees of freedom.
[00:48:03.470 - 00:48:05.270] Just a quick reminder here.
[00:48:05.270 - 00:48:08.710] Local Xe, the extraction, which is long and long.
[00:48:08.750 - 00:48:11.390] Think of the elements and node one is d1.
[00:48:11.390 - 00:48:14.270] Among the link to the element in the direction of Xe,
[00:48:14.270 - 00:48:15.470] node two is d2.
[00:48:15.470 - 00:48:17.810] So this is just some examples with different
[00:48:17.810 - 00:48:19.590] element orientations.
[00:48:19.590 - 00:48:22.590] And then, global Xe and node one is d1,
[00:48:22.590 - 00:48:23.550] up capacity one.
[00:48:24.590 - 00:48:27.430] Global Y and node one is up capacity two.
[00:48:27.430 - 00:48:30.190] Global X and node two is up capacity three.
[00:48:30.190 - 00:48:32.790] And global Y and node two is up capacity four.
[00:48:32.790 - 00:48:36.270] So this is just a range of examples here.
[00:48:37.230 - 00:48:39.390] The elements and different orientations
[00:48:39.390 - 00:48:41.910] showing their coordinate, their degrees of freedom
[00:48:41.910 - 00:48:44.150] and coordinates, lots of coordinates.
[00:48:44.150 - 00:48:46.510] And then the degrees of freedom and global coordinates.
[00:48:46.510 - 00:48:48.150] Just a nice reference page here.
[00:48:48.150 - 00:48:49.950] Just on here, it's the same element
[00:48:49.950 - 00:48:51.950] on the same element orientation,
[00:48:51.950 - 00:48:54.550] but we've chosen a different coordinate system here.
[00:48:54.550 - 00:48:57.030] In this case, we've chosen X to be the direction.
[00:48:57.030 - 00:48:59.390] And this to be node one, and this to be node two.
[00:48:59.390 - 00:49:02.150] So in this case, the angle there might be
[00:49:02.150 - 00:49:05.950] a transformation angle of 350 degrees.
[00:49:05.950 - 00:49:08.270] Maybe 360 degrees.
[00:49:08.270 - 00:49:10.830] Or we could say negative 20.
[00:49:10.830 - 00:49:11.630] This would be node one.
[00:49:11.630 - 00:49:13.110] This would be node two.
[00:49:13.110 - 00:49:17.110] And this would be the cross-running elements
[00:49:17.110 - 00:49:19.510] and global coordinates.
[00:49:19.510 - 00:49:20.710] If we show it in the same series, this
[00:49:20.710 - 00:49:23.070] will be the same node one and this node two.
[00:49:23.070 - 00:49:25.150] Then the element would be the orientation angle would
[00:49:25.150 - 00:49:30.590] start here with x, x, y, x g here.
[00:49:30.590 - 00:49:32.470] We would go through 90.
[00:49:32.470 - 00:49:35.110] And in a bit short of 180, it's the main way of 150
[00:49:35.110 - 00:49:37.030] and 360 degrees here.
[00:49:37.030 - 00:49:39.310] And then this would be d1 and d2.
[00:49:39.310 - 00:49:41.150] And this would be d3 and d4, which is different
[00:49:41.150 - 00:49:43.230] to that above.
[00:49:43.230 - 00:49:45.670] So either of these two element orientation angles
[00:49:45.670 - 00:49:46.750] is fine.
[00:49:46.750 - 00:49:49.630] We just need to be consistent.
[00:49:49.630 - 00:49:54.840] Once we've made the decision, we stick with it.
[00:49:54.840 - 00:49:57.720] And then just a quick summary here.
[00:49:57.720 - 00:50:00.760] All the major steps and equations,
[00:50:00.760 - 00:50:02.720] we have had degrees of freedom.
[00:50:02.720 - 00:50:05.440] We have a cross-running force in terms.
[00:50:05.440 - 00:50:07.400] We've got our local coordinate system.
[00:50:07.440 - 00:50:09.920] This stiffness equation, our global coordinate
[00:50:09.920 - 00:50:12.800] stiffness equation for an individual element.
[00:50:12.800 - 00:50:15.800] The process for the family are seemingly matrix building
[00:50:15.800 - 00:50:21.320] up the kg, the overall citizen of equations, solving them,
[00:50:21.320 - 00:50:23.080] and then push processing here.
[00:50:23.080 - 00:50:26.080] So we'll go through an example tomorrow, which will be what
[00:50:26.080 - 00:50:29.720] you'll be focusing on the name tomorrow.
[00:50:29.720 - 00:50:31.720] And thank you all for coming along.
[00:50:31.720 - 00:50:32.720] And I'll see you again tomorrow.
[00:51:30.260 - 00:51:39.900] Thank you.
[00:51:39.900 - 00:51:40.900] Good.
[00:51:40.900 - 00:51:41.900] Thank you.
[00:51:41.900 - 00:51:42.900] Good.
[00:51:42.900 - 00:51:43.900] Good.
[00:51:43.900 - 00:51:44.900] Good.
[00:51:44.900 - 00:51:45.900] Good.
[00:51:45.900 - 00:51:46.900] Good.
[00:51:46.900 - 00:51:47.900] Good.
[00:51:47.900 - 00:51:48.900] Good.
[00:51:48.900 - 00:51:49.900] Good.
[00:51:49.900 - 00:51:50.900] Good.
[00:51:50.900 - 00:51:51.900] Good.
[00:51:51.900 - 00:51:52.900] Good.
[00:51:52.900 - 00:51:53.900] Good.
[00:51:53.900 - 00:51:54.900] Good.
[00:51:54.900 - 00:51:55.900] Good.
[00:51:55.900 - 00:51:57.500] You're coming down that Q major.
[00:51:57.500 - 00:51:58.340] Good.
[00:51:58.340 - 00:51:59.340] Good.
[00:51:59.340 - 00:52:00.340] Good, I'm sorry.
[00:52:00.340 - 00:52:01.340] Good.
[00:52:01.340 - 00:52:02.340] Good.
[00:52:02.340 - 00:52:03.340] Good.
[00:52:03.340 - 00:52:04.340] Good.
[00:52:04.340 - 00:52:05.340] Good.
[00:52:05.340 - 00:52:06.340] Good.
[00:52:06.340 - 00:52:08.820] I'm just pointing to the degree of freedom.
[00:52:08.820 - 00:52:14.820] So that's actually the value of Q. What is Q?
[00:52:14.820 - 00:52:16.820] So let's leave it out by which that note moves.
[00:52:16.820 - 00:52:20.820] OK. So, yeah, so there's the depiction of that.
[00:52:20.820 - 00:52:22.820] But in the call also.
[00:52:22.820 - 00:52:24.820] Yes. So, and...
[00:52:24.820 - 00:52:28.820] So you can see the same result as what we got in the case.
[00:52:28.820 - 00:52:31.820] We can see the same solution as that.
[00:52:31.820 - 00:52:37.820] Yes. And actually what we do is, we're actually going to solve that same problem.
[00:52:37.820 - 00:52:41.820] So, one of the few pages.
[00:52:41.820 - 00:52:43.820] Does one?
[00:52:43.820 - 00:52:44.820] Yes.
[00:52:44.820 - 00:52:46.820] And then we go through and we get...
[00:52:46.820 - 00:52:47.820] This is the key.
[00:52:47.820 - 00:52:49.820] And then this is the same...
[00:52:49.820 - 00:52:50.820] Yes.
[00:52:50.820 - 00:52:53.820] And this is the lab tomorrow, so I see we're going to try...
[00:52:53.820 - 00:52:56.820] All the steps, this is the actual lab.
[00:52:56.820 - 00:52:58.820] I can see the same.
[00:52:58.820 - 00:53:00.820] The answers.
[00:53:00.820 - 00:53:01.820] Yeah.
[00:53:01.820 - 00:53:02.820] So...
[00:53:02.820 - 00:53:03.820] OK. Gotcha.
[00:53:03.820 - 00:53:07.820] It's the degree of freedom, but also how's that degree of freedom?
[00:53:07.820 - 00:53:11.820] Yes. So that makes sure that the answer is that they know.
[00:53:11.820 - 00:53:14.820] So the Q one is how much it moves horizontally into the sound.
[00:53:14.820 - 00:53:15.820] Which is very quickly.
[00:53:15.820 - 00:53:16.820] Thank you.
[00:53:16.820 - 00:53:17.820] Thank you.
[00:53:17.820 - 00:53:18.820] Yeah.
[00:53:18.820 - 00:53:25.800] Yeah.
[00:53:25.800 - 00:53:26.800] Yeah.
[00:53:26.800 - 00:53:27.800] Yeah.
[00:53:27.800 - 00:53:28.800] Okay.
[00:53:28.800 - 00:53:31.800] Why do you think we are on the other stage?
[00:53:31.800 - 00:53:35.110] Yeah.
[00:53:35.110 - 00:53:36.110] I can...
[00:53:36.110 - 00:53:40.110] I can see the key thing for this way.
[00:53:40.110 - 00:53:42.110] It's the same screen.
[00:53:42.110 - 00:53:43.110] It's actually not a lot of it.
[00:53:43.110 - 00:53:46.110] It's a bit of a subsequent connection, but the main thing we would do is...
[00:53:46.110 - 00:53:49.110] So basically, you can see the images that we see it.
[00:53:49.110 - 00:53:52.110] So it's basically right in the bottom.
[00:53:52.110 - 00:53:54.110] So we can see the picture.
[00:53:54.110 - 00:53:55.110] Yeah.
[00:53:55.110 - 00:53:56.110] Yeah.
[00:53:56.110 - 00:53:58.110] So it's actually very cool.
[00:53:58.110 - 00:53:59.110] Yes.
[00:53:59.110 - 00:54:01.110] The question is...
[00:54:01.110 - 00:54:03.110] The question is...
[00:54:03.110 - 00:54:05.110] I can see the key thing.
[00:54:05.110 - 00:54:07.110] But I will see.
[00:54:07.110 - 00:54:09.110] Yeah.
[00:54:09.110 - 00:54:10.110] So that's the key thing.
[00:54:10.110 - 00:54:11.110] Yeah.
[00:54:11.110 - 00:54:12.110] Good.
[00:54:12.110 - 00:54:15.110] But I will see.
[00:54:15.110 - 00:54:19.110] Here.
[00:54:19.110 - 00:54:21.110] Good.
[00:54:21.110 - 00:54:23.110] That's important.
[00:54:23.110 - 00:54:24.110] Good.
[00:54:24.110 - 00:54:25.110] Good.
[00:54:25.110 - 00:54:26.110] Good.
[00:54:26.110 - 00:54:27.110] Good.
[00:54:27.110 - 00:54:28.110] Good.
[00:54:28.110 - 00:54:29.110] Good.

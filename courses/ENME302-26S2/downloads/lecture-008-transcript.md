# ENME302-26S2 Lecture 8 fast-pass local ASR transcript

Date: July 24, 2026 11:00am-11:55am
Transcript type: Hermes fast-pass local ASR from validated Echo audio, not a native Echo transcript.
Backend/model: faster-whisper tiny.en, CPU int8, beam_size=1, vad_filter=True.
Quality note: fast catch-up transcript. Technical terms, equations, names and Māori words need checking against slides/audio before assessment use.
Source audio SHA-256: `22d65b805edfcacdff16002b616339411028b6a090251987503f56cbe228cfd8`
Generated: 2026-07-25T00:05:19.587891+12:00

[00:01:00.690 - 00:01:09.360] I've got a photo, like a line of room.
[00:01:09.360 - 00:01:13.560] I just wanted to start off just with this quick recap of this table.
[00:01:13.560 - 00:01:15.400] Obviously, you haven't worked with the lab yesterday.
[00:01:15.400 - 00:01:18.160] Hopefully, the point that they have is to give you an opportunity
[00:01:18.160 - 00:01:20.960] if you sit down and do and work through and think about things
[00:01:20.960 - 00:01:22.360] as you develop the code.
[00:01:22.360 - 00:01:25.760] And then like that, it's probably useful to refer back to this,
[00:01:25.760 - 00:01:31.840] so it's actually page 46 of the notes, which just covers the key steps
[00:01:31.840 - 00:01:34.240] here, all the different surface equations
[00:01:34.240 - 00:01:36.240] that the element level and element coordinates,
[00:01:36.240 - 00:01:38.160] element level and global coordinates,
[00:01:38.160 - 00:01:40.720] the element contribution to the overall kg,
[00:01:40.720 - 00:01:43.280] and then the overall stiffness matrix here,
[00:01:43.280 - 00:01:45.160] which is the summation of those.
[00:01:45.160 - 00:01:47.120] It's just quite a usual reference.
[00:01:47.120 - 00:01:49.480] I realise that there is a lot of different Ks,
[00:01:49.480 - 00:01:51.960] because the local stiffness matrix, local coordinates,
[00:01:51.960 - 00:01:56.400] they're just global coordinates, and it goes to the overall kg and the overall kg.
[00:01:56.400 - 00:01:59.160] I appreciate that that's maybe a lot to get you hit around,
[00:01:59.160 - 00:02:00.760] but this is actually quite a good reference page,
[00:02:00.760 - 00:02:04.400] just to show that the progression of information that's included
[00:02:04.400 - 00:02:06.600] at each of those pieces there.
[00:02:06.600 - 00:02:12.930] So useful to refer back to.
[00:02:12.930 - 00:02:14.810] So we worked through this problem.
[00:02:14.810 - 00:02:18.170] This was, we worked through this sort of directly.
[00:02:18.170 - 00:02:22.050] We had the assembly matrices, so that was the manual step
[00:02:22.050 - 00:02:26.650] that we've been through, and we ultimately got to our solution here.
[00:02:26.650 - 00:02:35.570] So this is the same solution that we saw from the...
[00:02:35.570 - 00:02:37.730] when we solved this by hand,
[00:02:37.730 - 00:02:41.330] but the keeping of the pipeline to here
[00:02:41.330 - 00:02:44.330] is that if we have an element,
[00:02:44.330 - 00:02:58.090] the presence of this third element
[00:02:58.090 - 00:03:08.060] makes the system strictly indeterminate,
[00:03:08.060 - 00:03:16.930] determinate, and much harder to solve by hand.
[00:03:16.930 - 00:03:30.780] However, through the final analysis,
[00:03:30.780 - 00:03:47.540] if we have this problem, there's not much harder at all.
[00:03:47.700 - 00:03:49.580] So all of that seemed like the...
[00:03:49.580 - 00:03:52.860] if you aim it, it's not that much different.
[00:03:52.860 - 00:03:56.860] If you do extend this to the effectiveness system,
[00:03:56.860 - 00:03:59.100] if you had three elements, five elements,
[00:03:59.100 - 00:04:04.780] three elements, whatever, the iffy method comes into its own
[00:04:04.780 - 00:04:06.460] and solves things a lot more easily.
[00:04:06.460 - 00:04:09.900] So in this case, suddenly by hand,
[00:04:09.900 - 00:04:12.260] you have to do a full step in the effectiveness solution.
[00:04:12.260 - 00:04:13.860] You have to look at components of stiffness.
[00:04:13.860 - 00:04:18.860] You'd have to then work out with those three arcs into six.
[00:04:18.860 - 00:04:25.660] Whereas in this case, here, you'd have one more element,
[00:04:25.660 - 00:04:27.180] one more simply matrix.
[00:04:27.180 - 00:04:29.500] You're just banging a couple of new angles,
[00:04:29.500 - 00:04:32.180] and on that surface matrix, so the same way.
[00:04:32.180 - 00:04:33.740] And then it comes out.
[00:04:33.740 - 00:04:36.020] There's maybe five of them seem harder.
[00:04:36.020 - 00:04:37.380] The code you've written already does this,
[00:04:37.380 - 00:04:39.340] you just need to extend this.
[00:04:39.340 - 00:04:42.340] So that's where the real difference is.
[00:04:42.500 - 00:04:44.740] The simple problem we work through may give you the false
[00:04:44.740 - 00:04:47.340] sense of security to think, actually, it's not that much
[00:04:47.340 - 00:04:50.900] harder to solve by hand, but only for a simple problem.
[00:04:50.900 - 00:04:52.860] And that changes dramatically once you introduce some
[00:04:52.860 - 00:04:56.950] extra elements.
[00:04:56.950 - 00:05:00.670] So towards the end of this problem, we work through,
[00:05:00.670 - 00:05:02.470] we work out all the reflection vectors.
[00:05:04.230 - 00:05:07.190] So we went through, we solved the system,
[00:05:07.190 - 00:05:10.350] then we solved individual reflections.
[00:05:10.350 - 00:05:11.390] We can calculate strain.
[00:05:11.390 - 00:05:13.590] So the strain change in length is the D2,
[00:05:13.630 - 00:05:15.390] the element one, once the D1,
[00:05:15.390 - 00:05:18.950] the D1 is the two, once D1 within a bar element
[00:05:18.950 - 00:05:21.830] is the axial compression or extension.
[00:05:23.230 - 00:05:25.990] And if you define the equation this way,
[00:05:25.990 - 00:05:30.390] it will always work and you'll always have a negative,
[00:05:30.390 - 00:05:36.950] if it's compressive and positive, if it's tensile.
[00:05:36.950 - 00:05:39.110] Then we go through here, so the end of the problem,
[00:05:39.110 - 00:05:41.830] we've worked through and we had a different force in terms.
[00:05:41.830 - 00:05:43.470] So here we have the forcing term.
[00:05:43.470 - 00:05:45.390] So we've gone through, we're extracted
[00:05:45.430 - 00:05:47.710] the values with more robust different spaces.
[00:05:47.710 - 00:05:50.870] So we've got our lower case Fs and our upper case Fs.
[00:05:52.550 - 00:05:54.350] So if we work to compare these,
[00:05:55.830 - 00:05:59.470] what's the difference between these two vectors?
[00:05:59.470 - 00:06:01.670] There's two vectors for the same element.
[00:06:01.670 - 00:06:04.190] So this is pretty quickly scheduled, they mean
[00:06:05.430 - 00:06:12.160] with the inclusion of our everybody diagram.
[00:06:12.160 - 00:06:15.000] So remember that the global coordinates,
[00:06:15.040 - 00:06:18.520] the upper case, the force in terms of global coordinates,
[00:06:18.520 - 00:06:21.080] the upper case Fs are always in the global reason,
[00:06:21.080 - 00:06:21.920] global Y.
[00:06:21.920 - 00:06:26.360] So this here is the direction, the first one here,
[00:06:26.360 - 00:06:27.320] that's negative 100.
[00:06:27.320 - 00:06:29.560] So to the right would be the default,
[00:06:29.560 - 00:06:31.720] but for this negative, I'm going to draw it to the left.
[00:06:31.720 - 00:06:34.360] So that's 100 kilonewtons,
[00:06:34.360 - 00:06:36.800] the same signal element,
[00:06:36.800 - 00:06:38.280] the difference sign from which has upwards,
[00:06:38.280 - 00:06:40.920] but because it's negative, I'm going to draw it downwards,
[00:06:40.920 - 00:06:44.840] I'm going to make the chute of 100 kilonewtons.
[00:06:46.560 - 00:06:48.080] And then over here,
[00:06:48.080 - 00:06:51.960] there's the upper positive, so we're going to have 100
[00:06:51.960 - 00:06:58.370] kilonewtons, the year and 100 kilonewtons here.
[00:07:01.830 - 00:07:05.110] Now we can also draw that same element,
[00:07:05.110 - 00:07:07.590] but we can label it in multiple coordinates.
[00:07:07.590 - 00:07:10.350] So here we've got X and Y, same coordinate axis
[00:07:10.350 - 00:07:13.510] as we had before, just add it to there as well,
[00:07:13.790 - 00:07:19.210] just indicate we're referring to element two.
[00:07:19.210 - 00:07:24.160] And if we take this, we enable the force like this.
[00:07:24.160 - 00:07:28.280] So one, 41 kilonewtons,
[00:07:28.280 - 00:07:29.640] and then force this way,
[00:07:30.920 - 00:07:34.080] same, one, 41 kilonewtons.
[00:07:38.700 - 00:07:43.700] So this is a multiple coordinates and this is a global coordinates.
[00:07:43.700 - 00:07:46.220] Now the obvious question you might have is,
[00:07:47.420 - 00:07:50.340] which one's better, which one's the one that we should use?
[00:07:50.340 - 00:07:52.420] Well, there is no simple answer to that.
[00:07:52.420 - 00:07:54.300] It's not like one is better and one is worse.
[00:07:54.300 - 00:07:55.820] It depends on what you're trying to do with it.
[00:07:55.820 - 00:07:57.660] So for example, you have a structure
[00:07:57.660 - 00:08:00.380] where there's multiple elements all coming in
[00:08:00.380 - 00:08:03.380] in different orientations to a single support point.
[00:08:03.380 - 00:08:05.700] And you want to know the total reaction and support.
[00:08:06.780 - 00:08:09.780] Then it makes a lot more sense to be using your global coordinates
[00:08:09.780 - 00:08:12.100] because different elements and different orientations
[00:08:12.100 - 00:08:15.340] will still have their forcing turns broken up
[00:08:15.340 - 00:08:17.020] and to global x and global y components
[00:08:17.020 - 00:08:18.580] that we have to get really nicely.
[00:08:19.660 - 00:08:21.660] So that's what you're trying to do.
[00:08:21.700 - 00:08:24.380] This vector and this format makes a lot more sense.
[00:08:25.460 - 00:08:26.860] Alternatively, if you were trying to do,
[00:08:26.860 - 00:08:29.060] say an axial stress calculation to work out
[00:08:29.060 - 00:08:31.100] what the minimum cross-section area was of an element
[00:08:31.100 - 00:08:35.740] to carry with sand the loads that's going to be applied,
[00:08:35.740 - 00:08:39.540] then this form here would be much more useful than to use.
[00:08:39.540 - 00:08:40.900] So it's just compared to what you're going to use
[00:08:40.900 - 00:08:43.740] for this not like one's better ones,
[00:08:43.740 - 00:08:46.260] with different ones that are more useful
[00:08:46.260 - 00:08:50.700] in different circumstances.
[00:08:50.700 - 00:08:52.180] You just got to cover a couple of final things
[00:08:52.180 - 00:08:53.420] from the babies today.
[00:08:54.420 - 00:08:58.540] I was going to try and do some stuff through my laptop.
[00:08:58.540 - 00:08:59.860] But it seems to be some connection problems
[00:08:59.860 - 00:09:00.860] to my distal.
[00:09:00.860 - 00:09:03.060] So I'm actually kind of resolve those and have that on Monday.
[00:09:06.950 - 00:09:08.870] Just there was the summary page there.
[00:09:08.870 - 00:09:10.950] Then this was where we went through
[00:09:10.950 - 00:09:12.870] so you've set up the code.
[00:09:12.870 - 00:09:15.070] You've got a nice local bar given
[00:09:15.070 - 00:09:17.430] the elastic module that's cost-section area and length
[00:09:17.430 - 00:09:18.910] for a given element,
[00:09:18.910 - 00:09:21.190] it returns the K1.
[00:09:22.310 - 00:09:24.150] Then you've got a Google bar,
[00:09:24.150 - 00:09:25.430] so you're giving the result K1
[00:09:25.630 - 00:09:29.190] the alpha value given K1 hat and lambda.
[00:09:29.190 - 00:09:32.590] It seems to be matrix the two different components
[00:09:32.590 - 00:09:35.790] of Kg to let each element's contribution to that overall
[00:09:35.790 - 00:09:36.950] stiffness matrix.
[00:09:38.190 - 00:09:39.950] Then we have our overall Kg here.
[00:09:41.830 - 00:09:43.430] We've been through under the simplest processing
[00:09:43.430 - 00:09:47.810] and couple of depictions values, the strains.
[00:09:47.810 - 00:09:53.350] And then what we have here was the plotting function.
[00:09:53.350 - 00:09:55.670] One thing actually I'll go back a couple of pages.
[00:09:55.670 - 00:09:57.670] I did actually make a mistake here,
[00:09:57.710 - 00:10:01.970] but it was radian, it should have been radians.
[00:10:01.970 - 00:10:06.250] So that was on page 55.
[00:10:06.250 - 00:10:07.690] It's NP dot radians.
[00:10:08.770 - 00:10:10.370] No apologies, effect cost and confusion.
[00:10:10.370 - 00:10:12.730] There may be still a full overview
[00:10:12.730 - 00:10:15.450] to work that out, should you avoid.
[00:10:15.450 - 00:10:19.370] Correct the better shoe, but just to correct that
[00:10:19.370 - 00:10:23.520] for the record.
[00:10:23.520 - 00:10:24.680] So all of the times we've defined some
[00:10:24.680 - 00:10:25.800] displacement coefficient factor
[00:10:25.800 - 00:10:27.960] with my say, a clarification factor of 100,
[00:10:27.960 - 00:10:29.160] it's good same point.
[00:10:29.160 - 00:10:30.280] And the few things we apply,
[00:10:30.320 - 00:10:32.960] a single magnification factor that applies
[00:10:32.960 - 00:10:35.800] to all nodal points in all directions.
[00:10:35.800 - 00:10:38.320] So we don't want to apply in different values
[00:10:38.320 - 00:10:40.040] of different nodes or in different directions
[00:10:40.040 - 00:10:41.880] because it's going to distort everything.
[00:10:41.880 - 00:10:44.400] Because you just signal, single magnification factor
[00:10:44.400 - 00:10:45.400] across everything.
[00:10:46.680 - 00:10:49.560] So this is the true position of that true
[00:10:49.560 - 00:10:51.160] defecive position of that node.
[00:10:51.160 - 00:10:53.880] And then this is the exaggerated down defecion.
[00:10:55.200 - 00:10:56.880] Now some of you might have noticed
[00:10:56.880 - 00:10:58.760] that the way we can draw coordinates like this
[00:10:58.800 - 00:11:00.200] is always p of x and y.
[00:11:00.200 - 00:11:02.720] And then the bottom code is p of x and p of y.
[00:11:02.720 - 00:11:05.720] So there's perhaps a little bit
[00:11:07.560 - 00:11:14.190] vexing the terms of trying to get brain around
[00:11:14.190 - 00:11:17.190] the mismatch and the way the things apply.
[00:11:17.190 - 00:11:19.830] So there just be the say x is got plot.
[00:11:19.830 - 00:11:24.310] And then we'd have zero to two x's and two y's.
[00:11:24.310 - 00:11:28.990] So if this was element one,
[00:11:28.990 - 00:11:30.230] when we're doing the defecive position,
[00:11:30.510 - 00:11:33.430] we start at zero team because the first nodal point
[00:11:33.430 - 00:11:35.870] is zero team that hasn't changed.
[00:11:35.870 - 00:11:40.870] And then second one is 10 plus Q1 and 10 plus Q2.
[00:11:43.710 - 00:11:47.070] So defecive position and then we could just say label
[00:11:48.390 - 00:12:01.910] equals deflected.
[00:12:01.910 - 00:12:03.750] Now the one question I just want to go back to
[00:12:03.750 - 00:12:05.710] is the concierge shape functions.
[00:12:05.710 - 00:12:27.080] So what if I wanted to know the internal defecion
[00:12:27.120 - 00:12:36.980] within an element based upon these
[00:12:38.740 - 00:12:48.820] liberal defecions?
[00:12:48.820 - 00:12:51.220] So suppose we want to know a position half way along
[00:12:53.380 - 00:13:11.660] element one.
[00:13:11.660 - 00:13:14.540] What we'll do there is we would define our shape functions.
[00:13:14.540 - 00:13:19.540] So U evaluated at x equals 0.5,
[00:13:19.540 - 00:13:24.540] L1 would be U evaluated as 10 meters long.
[00:13:24.900 - 00:13:27.540] So we evaluated x equals five meters.
[00:13:27.980 - 00:13:31.940] And then within the, we'd use our shape functions here.
[00:13:31.940 - 00:13:33.940] So we're going to go to the right of those.
[00:13:35.220 - 00:13:38.940] That's psi one of x,
[00:13:38.940 - 00:13:42.180] the one plus psi two of x,
[00:13:42.180 - 00:13:46.550] the two, which can also be written as the,
[00:13:47.630 - 00:13:49.950] so that should be U of x, they're not another psi.
[00:13:51.510 - 00:13:56.510] U of x is one minus x upon L, d1.
[00:13:57.270 - 00:14:00.910] d1 and x over L times d2.
[00:14:01.870 - 00:14:03.150] So in this case we would just write
[00:14:05.070 - 00:14:10.070] one minus five over 10 times our value of zero.
[00:14:11.630 - 00:14:16.630] And then plus five over 10 times our value of negative
[00:14:17.310 - 00:14:20.790] 0.6366 millimeters.
[00:14:23.270 - 00:14:24.750] And when we go through that,
[00:14:24.750 - 00:14:27.870] we get a value of negative 0.31,
[00:14:28.150 - 00:14:29.950] 0.83 millimeters.
[00:14:31.430 - 00:14:42.760] So this is the axial deflection internally halfway,
[00:14:44.040 - 00:15:07.900] along element one.
[00:15:07.900 - 00:15:09.380] So those shape functions,
[00:15:09.380 - 00:15:11.500] they were derived based on some assumptions.
[00:15:11.500 - 00:15:13.220] We assumed constant cross-section,
[00:15:13.220 - 00:15:17.420] and less modular and constant x equals four.
[00:15:18.580 - 00:15:19.980] We used those to build up a system
[00:15:19.980 - 00:15:21.420] and generate astrophysmatrix,
[00:15:21.420 - 00:15:23.820] but implicit part of how we solved this.
[00:15:23.860 - 00:15:26.980] Then we can use the same things to sort of pull apart
[00:15:26.980 - 00:15:28.700] and then furl what's going on,
[00:15:28.700 - 00:15:37.090] internally from those solved, no reflections.
[00:15:37.090 - 00:15:41.130] Now what I wanna do here is just do one more problem,
[00:15:41.130 - 00:15:42.290] it's a good problem three,
[00:15:42.290 - 00:15:44.530] and it's a three element bar structure.
[00:15:44.530 - 00:15:46.730] So most we already on the code,
[00:15:46.730 - 00:15:49.130] you could go and do this problem quite quickly,
[00:15:49.130 - 00:15:52.130] based on the code that you've developed in the lab.
[00:15:52.130 - 00:15:58.380] You still do that?
[00:15:58.380 - 00:15:59.740] So we have this problem three.
[00:16:00.740 - 00:16:03.140] It's been up to three power elements supported by a pen,
[00:16:03.140 - 00:16:05.460] at eight, and a roller at eight.
[00:16:05.460 - 00:16:08.180] So the pen constraints all motion,
[00:16:08.180 - 00:16:11.980] and the roller at eight prevents any vertical motion
[00:16:11.980 - 00:16:13.860] but at a vast horizontal motion.
[00:16:14.740 - 00:16:16.300] Receive a lot of them is five years long,
[00:16:16.300 - 00:16:18.380] we have a hollow cross-section of 100 millimeter
[00:16:18.380 - 00:16:20.740] outside diameter and two millimeter wall thickness,
[00:16:20.740 - 00:16:22.180] and then made with an elastic modulus
[00:16:22.180 - 00:16:24.260] of C-me-gegepascal.
[00:16:24.260 - 00:16:25.660] We've been asked to solve the fictions,
[00:16:25.660 - 00:16:27.260] element forces and fictions,
[00:16:27.260 - 00:16:32.040] and determine the support reaction forces.
[00:16:32.040 - 00:16:33.800] So the first thing we need to do here
[00:16:33.800 - 00:16:35.960] is determine the allowable degrees of freedom.
[00:16:37.120 - 00:16:39.520] In this case, they are given to us on the diagram,
[00:16:39.520 - 00:16:40.520] but when it comes to the test,
[00:16:40.520 - 00:16:42.040] you will not be given that information
[00:16:42.040 - 00:16:45.760] and you need to be confident to determine that yourself.
[00:16:45.760 - 00:16:46.760] So very quickly,
[00:16:48.320 - 00:16:57.220] the pen constraints motion in the XG
[00:16:59.700 - 00:17:03.580] and YG direction.
[00:17:08.040 - 00:17:17.080] So that means there's no allowable reflection,
[00:17:17.080 - 00:17:18.600] so there's no degree to freedom,
[00:17:18.600 - 00:17:32.530] there's no Q values assigned here.
[00:17:32.530 - 00:17:38.130] Up at this point,
[00:17:38.130 - 00:17:51.570] so we're gonna say two potential non-zero deflections,
[00:17:51.570 - 00:18:00.720] and that means two Q values.
[00:18:00.720 - 00:18:04.250] And at the roller,
[00:18:04.250 - 00:18:10.770] vertical, which is the YG direction,
[00:18:10.770 - 00:18:16.630] this constraint,
[00:18:16.630 - 00:18:27.650] so no Q value in that direction.
[00:18:27.690 - 00:18:38.900] However, there is permissible deflection in XG,
[00:18:39.140 - 00:18:42.700] in our frontal direction,
[00:18:42.700 - 00:18:46.380] so there is one Q value.
[00:18:48.060 - 00:18:59.550] There's a good, you do need to be confident
[00:18:59.550 - 00:19:00.710] to make those decisions
[00:19:00.710 - 00:19:02.430] and assign the degrees of freedom
[00:19:02.430 - 00:19:03.910] because they will be expected step
[00:19:03.910 - 00:19:09.780] that you complete during the test.
[00:19:09.780 - 00:19:12.500] Then what we do is we do our all important
[00:19:12.500 - 00:19:13.660] free body diagrams.
[00:19:13.660 - 00:19:16.300] So free body diagrams are really, really crucial.
[00:19:17.300 - 00:19:18.700] Sometimes people are reluctant
[00:19:18.700 - 00:19:20.780] to look like interested by memory
[00:19:20.780 - 00:19:22.780] and you don't need to write them down.
[00:19:22.780 - 00:19:23.940] But they're really important
[00:19:23.940 - 00:19:26.420] because they are a record of the assumptions you've played.
[00:19:26.420 - 00:19:28.500] You write them down,
[00:19:28.500 - 00:19:30.620] you've really put on paper,
[00:19:30.620 - 00:19:32.300] this is the element orientation that I chose,
[00:19:32.300 - 00:19:34.820] this is the corresponding numbering sequence.
[00:19:34.820 - 00:19:36.620] So in later on when you have a vector
[00:19:36.620 - 00:19:38.580] with forces or displacements,
[00:19:38.580 - 00:19:39.460] you've got the sphere of effort
[00:19:39.460 - 00:19:41.300] actually to interpret it.
[00:19:41.300 - 00:19:43.260] So please don't skip the free body diagram,
[00:19:43.260 - 00:19:45.060] they are a really, really important step.
[00:19:45.060 - 00:19:46.500] And it comes to the test
[00:19:46.500 - 00:19:48.300] where we do the CAD marks for writing,
[00:19:48.300 - 00:19:49.420] for presenting those.
[00:19:49.420 - 00:19:54.030] So there's an extra motivation.
[00:19:54.030 - 00:19:56.070] So we've gone through and we've got our,
[00:19:56.070 - 00:19:57.190] we've drawn three of these diagrams
[00:19:57.190 - 00:19:58.030] of our three elements.
[00:19:58.030 - 00:19:59.990] We've got our global coordinate system here
[00:19:59.990 - 00:20:01.110] and we've got some,
[00:20:01.110 - 00:20:04.430] we've chosen some element coordinate systems here.
[00:20:04.430 - 00:20:05.910] So we have this coordinate system here
[00:20:05.910 - 00:20:06.910] which means for this element,
[00:20:06.910 - 00:20:09.350] this is node one and this is node two.
[00:20:10.590 - 00:20:13.430] This is the element system we've chosen here.
[00:20:13.430 - 00:20:15.790] So this is node one and this is node two.
[00:20:16.670 - 00:20:18.190] In this case we've actually chosen
[00:20:18.190 - 00:20:20.470] the extra point downwards here,
[00:20:20.470 - 00:20:23.190] which means this one at the top is node one
[00:20:23.190 - 00:20:27.500] and this one down here is node two.
[00:20:27.500 - 00:20:28.500] So in this case,
[00:20:28.500 - 00:20:31.340] your alpha for element two
[00:20:31.340 - 00:20:34.060] is going to be a zero degree translation angle
[00:20:34.060 - 00:20:35.740] because the coordinate system's match.
[00:20:36.780 - 00:20:37.620] In this case,
[00:20:37.620 - 00:20:40.020] we start with xg and we rotate counter-clockwise
[00:20:40.020 - 00:20:41.940] until we align with the element.
[00:20:41.940 - 00:20:43.620] So this one here,
[00:20:43.660 - 00:20:46.020] alpha for element one
[00:20:46.020 - 00:20:48.300] is going to be plus 30 degrees,
[00:20:48.300 - 00:20:53.900] so it's 60 degrees just defined right there.
[00:20:55.780 - 00:20:56.980] Now in this third element,
[00:20:58.500 - 00:20:59.340] we've got two options.
[00:20:59.340 - 00:21:04.340] We start with xg and we can go around 90, 180, 270,
[00:21:04.620 - 00:21:11.020] and then another 60, sorry, 30 degrees on top of that.
[00:21:11.300 - 00:21:13.460] So we'd get 300 degrees.
[00:21:13.460 - 00:21:15.580] So this could be alpha three
[00:21:15.620 - 00:21:19.260] is equal to plus 300 degrees
[00:21:19.260 - 00:21:20.820] or if we were good to go clockwise,
[00:21:20.820 - 00:21:23.500] we'd start here and we'd go clockwise by 60 degrees
[00:21:23.500 - 00:21:25.540] but of course that would be a negative value
[00:21:25.540 - 00:21:27.300] because it's moving in the opposite direction
[00:21:27.300 - 00:21:29.660] to our agreed sign convention.
[00:21:31.140 - 00:21:32.540] So we can use either of those two,
[00:21:34.180 - 00:21:35.860] based upon our element sequence.
[00:21:37.180 - 00:21:40.980] Now what we need to do is just through the translation
[00:21:40.980 - 00:21:45.050] although the relationship between degrees are freedom.
[00:21:45.050 - 00:21:47.330] So let's look here at element one.
[00:21:47.330 - 00:21:49.570] Now D1 and D2 for element one
[00:21:49.570 - 00:21:52.530] don't cross ones to anything in the global structure.
[00:21:53.530 - 00:21:58.530] However, D3 and D4 cross ones to Q1 and Q2 respectively.
[00:21:59.370 - 00:22:01.690] So we can write D3 for element one
[00:22:02.850 - 00:22:06.530] as equal to Q1 and D4 for element one
[00:22:06.530 - 00:22:10.260] is equal to Q2.
[00:22:10.260 - 00:22:12.420] So that there is the sort of comic-to-view information
[00:22:12.420 - 00:22:16.340] that we need to be able to feed into our
[00:22:19.900 - 00:22:24.900] to be able to feed into the generation of SME matrix.
[00:22:26.890 - 00:22:28.450] So element three.
[00:22:28.450 - 00:22:32.290] Well D1 and D2 cross ones to Q1 and Q2.
[00:22:32.290 - 00:22:37.290] So D1 for element three is equal to Q1
[00:22:37.770 - 00:22:41.530] and D2 for element three is equal to Q2.
[00:22:43.530 - 00:22:47.650] D3 for element three that corresponds
[00:22:47.650 - 00:22:49.170] to the horizontal depiction of the roller
[00:22:49.210 - 00:22:53.010] which is defined as Q3 and D4
[00:22:53.010 - 00:22:54.130] as the cross one to anything.
[00:22:54.130 - 00:22:58.850] So this is the key information that we have here.
[00:22:58.850 - 00:23:02.250] Now one question you might have is why did I call
[00:23:02.250 - 00:23:04.010] this Q1 and Q2 in the Q3?
[00:23:06.010 - 00:23:08.010] Could I have just called this Q1 and this Q2
[00:23:08.010 - 00:23:09.170] in the Q3?
[00:23:09.170 - 00:23:10.610] And the answer is yes, you could.
[00:23:10.610 - 00:23:11.770] There's nothing.
[00:23:11.770 - 00:23:16.290] Within an element, we must follow our sign convention,
[00:23:16.290 - 00:23:17.530] our number of convention.
[00:23:17.530 - 00:23:19.570] Where we go, globally, slow, wide, node one,
[00:23:19.570 - 00:23:22.430] but we'll extend the number of y at node two for D1,
[00:23:22.430 - 00:23:24.170] D4 respectively.
[00:23:24.170 - 00:23:27.370] So we have no flexibility in the number and sequence
[00:23:27.370 - 00:23:29.810] that we apply within an element.
[00:23:29.810 - 00:23:32.570] Once we've chosen the element orientation.
[00:23:32.570 - 00:23:34.730] At the structural level, we do actually
[00:23:34.730 - 00:23:35.650] have a bit of flexibility.
[00:23:35.650 - 00:23:37.170] So we could have called this Q1,
[00:23:37.170 - 00:23:40.690] we could have called this Q2 and Q3 and it would all
[00:23:40.690 - 00:23:41.610] work out fine.
[00:23:41.610 - 00:23:45.090] There's FU do follows for the same sort of broad process
[00:23:45.090 - 00:23:46.730] and you can have work progressively through the structure
[00:23:46.730 - 00:23:48.090] and follow x, y.
[00:23:49.090 - 00:23:51.930] The assembly matrices will be slightly nicer form,
[00:23:51.930 - 00:23:53.050] but there's nothing saying this.
[00:23:53.050 - 00:23:56.890] This was Q1, Q2 and Q3, there's nothing wrong with that.
[00:23:56.890 - 00:24:00.290] You would still guess you get different assembly matrices
[00:24:00.290 - 00:24:01.530] because the way they connect to those
[00:24:01.530 - 00:24:03.570] of those degrees are framework be different.
[00:24:03.570 - 00:24:06.610] And when you open myself, that's using the Neo-Houjo
[00:24:06.610 - 00:24:09.490] Assert solution, you would get the same numbers
[00:24:09.490 - 00:24:11.690] in the QDIC that they'll be in a different order.
[00:24:11.690 - 00:24:15.970] So as long as you're consistent, it will all work out.
[00:24:16.010 - 00:24:20.690] With regards to the test, there won't any number of
[00:24:20.690 - 00:24:23.370] signals that your pliers on this consistent are correct.
[00:24:23.370 - 00:24:24.730] It will be enough as correct.
[00:24:24.730 - 00:24:27.090] It doesn't mean there's multiple sets of model solutions
[00:24:27.090 - 00:24:30.770] so that the test like this must make it the hardest mark.
[00:24:30.770 - 00:24:34.210] That's come the point of not penalizing someone for something.
[00:24:34.210 - 00:24:38.340] It's not wrong.
[00:24:38.340 - 00:24:44.340] And finally here, for element 2, then we know that D1 and D2
[00:24:44.340 - 00:24:45.620] don't cross-mod anything.
[00:24:45.620 - 00:24:47.500] D4 doesn't cross-mod anything.
[00:24:47.500 - 00:24:55.460] But D3, 4 element 2 is equal to Q3.
[00:24:55.460 - 00:24:57.740] So that's the key connectivity information
[00:24:57.740 - 00:25:10.500] that we need here to generate our assembly matrices.
[00:25:10.500 - 00:25:25.210] The next thing we've got here is we've got,
[00:25:25.210 - 00:25:29.170] it's just the surface matrices of K1, K2, K3.
[00:25:29.170 - 00:25:30.850] So that's expressed in element level.
[00:25:30.850 - 00:25:33.050] And we'll call it nuts to the results later.
[00:25:33.050 - 00:25:34.450] OK, one without a hat.
[00:25:34.450 - 00:25:36.970] And K2 and K3 previously, which isn't presented.
[00:25:38.490 - 00:25:41.490] But this will be independent steps there.
[00:25:41.490 - 00:25:43.810] Now here are our assembly matrices.
[00:25:43.810 - 00:25:46.730] And that's just the information that we've just gone through
[00:25:46.730 - 00:25:47.530] on the previous page.
[00:25:47.530 - 00:25:49.730] So we just were presenting that on the matrix and putting
[00:25:49.730 - 00:25:53.690] ones with those components there.
[00:25:53.690 - 00:25:55.290] Now there are some really nice and interesting things
[00:25:55.290 - 00:25:57.810] to see in these assembly matrices.
[00:25:57.810 - 00:26:01.530] So first thing we're going to do is look at element 1.
[00:26:01.530 - 00:26:04.970] And the assembly matrix that corresponds to it.
[00:26:04.970 - 00:26:19.570] So we've got two all zero columns here.
[00:26:19.570 - 00:26:20.890] These degree of freedom.
[00:26:20.890 - 00:26:39.030] So d1, 1, and d2, 1 do not have a global structural degree
[00:26:39.030 - 00:26:51.310] of freedom, which means that are fixed.
[00:26:51.310 - 00:26:54.550] So within an assembly matrix, we're given element and all
[00:26:54.550 - 00:26:58.350] zero column means that that degree of freedom is fixed.
[00:26:58.350 - 00:27:00.230] And what that actually does when we go through the matrices,
[00:27:00.230 - 00:27:03.270] it actually constrains that degree of freedom out of a solution.
[00:27:03.270 - 00:27:06.230] We already know that as zero, we don't need to solve for it.
[00:27:06.550 - 00:27:10.380] It actually removes the information out.
[00:27:10.380 - 00:27:14.500] What we also see here, there for element 1,
[00:27:14.500 - 00:27:19.050] is we see in all zero row.
[00:27:19.050 - 00:27:23.050] And why does the all zero row exist?
[00:27:23.050 - 00:27:24.130] Now that's something a little bit different.
[00:27:24.130 - 00:27:24.890] And it just comes back.
[00:27:24.890 - 00:27:27.170] If we look back at everybody diagram,
[00:27:27.170 - 00:27:30.170] this is element 1 up here.
[00:27:30.170 - 00:27:33.250] And it connects to this node that has these degrees of freedom.
[00:27:33.250 - 00:27:35.050] But Q3 is over here.
[00:27:35.050 - 00:27:36.690] It's at a completely different node.
[00:27:36.690 - 00:27:39.930] And element 1 doesn't have any direct connection to that node.
[00:27:39.930 - 00:27:52.190] So all that all zero row is saying is that there is no direct
[00:27:52.190 - 00:28:06.740] connection between element 1 and Q3.
[00:28:06.740 - 00:28:10.420] So basically that the node at which Q3 exists
[00:28:10.420 - 00:28:13.780] isn't directly connected to element 1.
[00:28:13.780 - 00:28:15.220] So the problem and the larger structure,
[00:28:15.220 - 00:28:19.900] we might see quite a few all zero rows.
[00:28:19.900 - 00:28:24.420] Because there might be 10 or 100 or 1,000 nodes within a larger
[00:28:24.420 - 00:28:25.300] structure.
[00:28:25.300 - 00:28:31.020] And their element doesn't happen to connect to them.
[00:28:31.020 - 00:28:33.420] The same thing can be seen here, if element 2.
[00:28:33.420 - 00:28:38.140] There's two all zero rows that cross 1 to Q1 and Q2.
[00:28:38.140 - 00:28:43.100] And if we look back at this, element 2 is down here at the bottom.
[00:28:43.100 - 00:28:45.300] The node with Q1 and Q2 is at the top.
[00:28:45.300 - 00:28:48.860] There's no direct connection, which is why we see those all two
[00:28:48.860 - 00:28:54.560] all zero rows.
[00:28:54.560 - 00:28:59.820] So we'll see that here.
[00:28:59.820 - 00:29:21.700] Element 2 doesn't directly connect to the node with Q1.
[00:29:21.700 - 00:29:27.540] There's also two all zero columns, which just relates to the fact that
[00:29:27.540 - 00:29:30.460] degrees are freedom 1 and 2 were at a end support.
[00:29:30.460 - 00:29:36.410] I was looking strange, just like the same as above.
[00:29:36.410 - 00:29:42.970] And then for the element 3, it connects to the node with Q1, Q2 and Q3.
[00:29:42.970 - 00:29:48.290] And there has an all zero column.
[00:29:48.290 - 00:30:01.520] This is an all zero column due to the constraints from the
[00:30:01.520 - 00:30:36.810] rower, which prevented YG.
[00:30:36.810 - 00:30:38.690] So that's just a good look.
[00:30:38.690 - 00:30:40.770] I just want to take that moment to go through.
[00:30:40.770 - 00:30:42.050] I don't want you to see me matrices.
[00:30:42.050 - 00:30:44.530] You just have to be some sort of black box or mystery thing.
[00:30:44.530 - 00:30:48.570] There's clear messages being conveyed through how they're
[00:30:48.570 - 00:30:53.750] assembled and what the numbers in them are.
[00:30:53.750 - 00:30:55.190] The next page is fairly procedural.
[00:30:55.190 - 00:30:58.870] We're going through we're applying this method with
[00:30:58.870 - 00:30:59.910] summing up.
[00:30:59.910 - 00:31:02.510] We've got our individual components, the K2 is just some of
[00:31:02.510 - 00:31:03.550] those.
[00:31:03.550 - 00:31:07.630] And then we do our matrix solution here.
[00:31:07.630 - 00:31:10.470] So this is our NP.
[00:31:10.470 - 00:31:12.870] Blot on the now.
[00:31:12.870 - 00:31:22.830] So now one question here might be what is up the case Q?
[00:31:22.830 - 00:31:28.940] Well, that information is given on the question.
[00:31:28.940 - 00:31:32.180] So here we had 500 kilonewtons horizontally at Q1.
[00:31:32.180 - 00:31:34.340] We had zero kilonewtons vertically.
[00:31:34.340 - 00:31:38.020] And then we had zero kilonewtons horizontally.
[00:31:38.020 - 00:31:54.900] So given in the question, that Q is equal to 500,000
[00:31:54.900 - 00:32:02.900] mutants, zero newtons, and zero newtons.
[00:32:02.900 - 00:32:04.700] Once we do that, we give a solution out.
[00:32:04.700 - 00:32:08.700] We can do all the forcing firms.
[00:32:08.700 - 00:32:13.940] And then of course, when we want to do deflections,
[00:32:13.940 - 00:32:16.140] we're going to do reactions.
[00:32:16.140 - 00:32:23.740] We can use these steps here.
[00:32:23.740 - 00:32:27.140] So this is a reaction force that the supports we've gone through
[00:32:27.140 - 00:32:29.740] with extractive the relevant degrees of freedom using our
[00:32:29.740 - 00:32:32.860] assembly matrix within multiply by the appropriate stiffness
[00:32:32.860 - 00:32:33.300] matrices.
[00:32:33.300 - 00:32:35.220] And we've got our forcing terms.
[00:32:35.220 - 00:32:42.780] If we want to know the reaction force required at A,
[00:32:42.780 - 00:32:47.660] then we've got basically two different elements are framing in
[00:32:47.660 - 00:32:47.860] here.
[00:32:47.860 - 00:32:53.140] So we have element one comes into this pen so is element two.
[00:32:53.140 - 00:32:56.540] So the total reaction in the extraction is going to be the
[00:32:56.540 - 00:33:00.420] summation of F1, element one, and F2, element F1,
[00:33:00.420 - 00:33:01.260] element two.
[00:33:01.260 - 00:33:03.420] So the two horizontal forces here.
[00:33:03.420 - 00:33:06.140] This is a prime example of when you've got different elements
[00:33:06.140 - 00:33:08.140] coming in on different orientations.
[00:33:08.140 - 00:33:11.380] And you want to add up the contributions using global
[00:33:11.380 - 00:33:12.740] coordinates comes into its own here.
[00:33:12.740 - 00:33:15.220] Because you can just add them directly.
[00:33:15.220 - 00:33:20.540] And when you do that here, you went up with a total reaction
[00:33:20.540 - 00:33:35.610] force here on the pen, which is 500 kiln new things this way,
[00:33:35.610 - 00:33:50.900] and then 433 kiln newtons, particularly.
[00:33:50.900 - 00:33:52.860] We can apply some of the thing at the roller.
[00:33:52.860 - 00:33:59.740] So in this case, based upon our original free-body diagrams,
[00:33:59.740 - 00:34:02.540] it's the third and fourth forcing terms.
[00:34:02.540 - 00:34:07.260] So element three, and it's the third and fourth element terms for
[00:34:07.260 - 00:34:08.420] element two.
[00:34:08.420 - 00:34:12.380] And that's the contributions that add up here.
[00:34:12.380 - 00:34:16.980] And once we sketch that, we end up with the roller.
[00:34:16.980 - 00:34:21.300] And we've got the elements that say coming in here.
[00:34:21.300 - 00:34:26.980] And we have a horizontal force of zero kiln newtons and a
[00:34:26.980 - 00:34:36.560] vertical force here of 43 kiln newtons.
[00:34:36.560 - 00:35:08.340] Now, if we're going to do a horizontal reaction, so X
[00:35:08.340 - 00:35:16.400] has equal to zero kiln newtons as expected.
[00:35:16.400 - 00:35:18.400] And I do really encourage you to just do those
[00:35:18.400 - 00:35:22.600] sort of sanity checks, those do a reference check.
[00:35:22.600 - 00:35:27.400] And say, does the solution that I've obtained match the physical
[00:35:27.400 - 00:35:30.040] system that I thought I was modeling?
[00:35:30.040 - 00:35:31.240] Because it's very easy.
[00:35:31.240 - 00:35:32.560] There's lots of indices here.
[00:35:32.560 - 00:35:35.880] And maybe you've grabbed the wrong vector, and you've pulled the
[00:35:35.880 - 00:35:38.120] forcing terms out of the wrong vector for element two and
[00:35:38.120 - 00:35:40.200] zero and zero and three, or element one and zero on two,
[00:35:40.200 - 00:35:41.880] or something like that.
[00:35:41.880 - 00:35:46.200] If you do see that, you can put a non-zero value here, the
[00:35:46.200 - 00:35:49.320] huge red flag to just say, look, this is for a minute.
[00:35:49.320 - 00:35:51.840] Go back and check that my working is correct, because this
[00:35:51.840 - 00:35:58.390] doesn't match the result that I would expect.
[00:35:58.390 - 00:36:07.770] If we look quickly at the top node, what we've got there is
[00:36:07.770 - 00:36:14.960] actually if three to four thousand one, which is equal to
[00:36:14.960 - 00:36:18.680] one hundred and fifty thousand, and four hundred and
[00:36:18.680 - 00:36:25.440] thirty three thousand, that's rounded, but nice.
[00:36:25.440 - 00:36:32.840] And if two, that was one to two of that forcing vector, we have
[00:36:32.840 - 00:36:36.600] two hundred and fifty thousand, and then we have negative
[00:36:36.600 - 00:36:39.880] four hundred and three to three thousand, so this is
[00:36:39.880 - 00:36:40.880] what we can do.
[00:36:40.880 - 00:36:53.490] Now, if we add that up together, what we get is five hundred
[00:36:53.490 - 00:36:57.490] hundred and three thousand point, and zero
[00:36:57.490 - 00:37:03.740] hundred and three thousand, basically.
[00:37:03.740 - 00:37:14.770] The reason I've done that is we see that the internal element
[00:37:14.770 - 00:37:26.860] forces at this node sum up to the applied external nodes.
[00:37:26.860 - 00:37:34.820] So that's the applied external node given to us in the
[00:37:34.820 - 00:37:39.140] question.
[00:37:39.140 - 00:37:41.140] Again, it's a good trick to do because that is by
[00:37:41.140 - 00:37:43.140] definition what must happen.
[00:37:43.140 - 00:37:47.140] There's a five hundred kiln Newton applied external load, and
[00:37:47.140 - 00:37:50.140] what our system tells us is how those loads get developed internally
[00:37:50.140 - 00:37:56.120] within those elements.
[00:37:56.120 - 00:37:59.120] We can go through, we can just do sort of a quick sketch of
[00:37:59.120 - 00:38:02.120] what the effective shape might look like, and we can work
[00:38:02.120 - 00:38:03.120] through that on next page.
[00:38:03.120 - 00:38:20.840] There's the actual defections that we get.
[00:38:20.840 - 00:38:25.840] We can work through, we can just solve the equation, put some
[00:38:25.840 - 00:38:27.840] specific values and solve them.
[00:38:27.840 - 00:38:32.840] We can sketch and exaggerate it to fit the plot, and then
[00:38:32.840 - 00:38:35.840] we can solve for internal defections, and then do
[00:38:35.840 - 00:38:37.840] strains and stresses from that as well.
[00:38:37.840 - 00:38:48.390] So this is just those steps there.
[00:38:48.390 - 00:38:51.390] This is an exaggerated defection.
[00:38:51.390 - 00:38:54.390] Individual defection vectors are how much each element has
[00:38:54.390 - 00:38:56.390] stretched or compressed.
[00:38:56.390 - 00:39:02.390] And for D1 and D2, the first coordinate was the
[00:39:02.390 - 00:39:05.390] node one for balance one and two was at this node, so we
[00:39:05.390 - 00:39:09.390] would expect those first entries in those vectors to be zero,
[00:39:09.390 - 00:39:14.390] whereas elements three here on the incline actually is a
[00:39:14.390 - 00:39:16.390] non-zero value at both ends.
[00:39:16.390 - 00:39:22.390] So the element itself has compressed because the
[00:39:22.390 - 00:39:26.390] left hand, the node one has moved more than node two, so
[00:39:26.390 - 00:39:29.390] actually that's a compressive displacement that's been
[00:39:29.390 - 00:39:32.390] applied in there, but it's also moved in space as a result
[00:39:32.390 - 00:39:36.390] of the elements that it's connected to deflecting as
[00:39:36.390 - 00:39:37.390] well.
[00:39:37.390 - 00:39:39.390] There's a multiple things going on.
[00:39:39.390 - 00:39:42.390] We can then calculate, this is our definition of strain,
[00:39:42.390 - 00:39:44.390] the change in the length along the element, by the original
[00:39:44.390 - 00:39:47.390] length, and when we get twoteenths out and one compressive
[00:39:47.390 - 00:39:50.390] stress, it comes out of that.
[00:39:50.390 - 00:39:55.080] There's any questions on that example?
[00:39:55.080 - 00:40:08.000] Just want to quickly work through the additional
[00:40:08.000 - 00:40:11.000] lab sheet that was done in the Navi's today and just want to
[00:40:11.000 - 00:40:15.000] highlight a couple of key things in that process.
[00:40:15.000 - 00:40:29.300] So this was the problem that we were asked to solve.
[00:40:29.300 - 00:40:33.300] Two bars connected, different material and properties and
[00:40:33.300 - 00:40:37.300] things in here, and we're asked to solve for this
[00:40:37.300 - 00:40:38.300] load.
[00:40:38.300 - 00:40:40.300] So what's going to happen here?
[00:40:40.300 - 00:40:42.300] This is going to want to swing downwards.
[00:40:42.300 - 00:40:44.300] This bar is going to constrain it.
[00:40:44.300 - 00:40:46.300] So both bars are going to wind up in tension.
[00:40:46.300 - 00:40:48.300] One is going to extend slightly out of here.
[00:40:48.300 - 00:40:51.300] And one is going to extend slightly out of here.
[00:40:51.300 - 00:40:55.300] And then we essentially want to find the sort of
[00:40:55.300 - 00:40:57.300] intersection point down here.
[00:40:57.300 - 00:40:59.300] Just get that a bit better.
[00:40:59.300 - 00:41:02.300] This is the intersection point.
[00:41:02.300 - 00:41:05.300] We're looking for, and we want to know all the
[00:41:05.300 - 00:41:09.300] forcing turns and the two element actions as well.
[00:41:09.300 - 00:41:12.300] So we quickly work through this by hand.
[00:41:12.300 - 00:41:14.300] We get an internal forcing.
[00:41:14.300 - 00:41:18.300] We can work out element elongations.
[00:41:18.300 - 00:41:21.300] And this is the linearized version here.
[00:41:21.300 - 00:41:23.300] This is how much element one stretches and one two
[00:41:23.300 - 00:41:24.300] stretches this way.
[00:41:24.300 - 00:41:26.300] And this is the final position here.
[00:41:26.300 - 00:41:28.300] So we can trace that through.
[00:41:28.300 - 00:41:34.300] So we get ultimately one nine two five millimeters to the right.
[00:41:34.300 - 00:41:37.300] And point three three four millimeters downwards.
[00:41:37.300 - 00:41:39.300] And that's with the manual intervention and tracing things
[00:41:39.300 - 00:41:40.300] through.
[00:41:40.300 - 00:41:44.340] What we did in this example is the first time we just made
[00:41:44.340 - 00:41:46.340] an assumption on our orientation.
[00:41:46.340 - 00:41:48.340] Now this is probably the most intuitive one.
[00:41:48.340 - 00:41:50.340] Zero degree transmission angle here.
[00:41:50.340 - 00:41:54.340] And then 55 degree transmission angle here.
[00:41:54.340 - 00:41:57.340] Remember the lower case D's were always aligned along the
[00:41:57.340 - 00:41:58.340] element.
[00:41:58.340 - 00:42:01.340] Whereas the upper case D's are always aligned with our ex-mye
[00:42:01.340 - 00:42:02.340] global.
[00:42:02.340 - 00:42:05.340] And then we have the corresponding assembly matrices.
[00:42:05.340 - 00:42:07.340] So D3 is element one cross-month to Q1.
[00:42:07.340 - 00:42:10.340] And D4 is element one cross-month to Q2.
[00:42:10.340 - 00:42:15.340] And as D1 and D2 cross-month to Q1 and Q2 for
[00:42:15.340 - 00:42:16.340] element two.
[00:42:16.340 - 00:42:19.340] So this is what the cross-whelming assembly matrices look like.
[00:42:19.340 - 00:42:24.940] We go through a general stiffness matrices and things.
[00:42:24.940 - 00:42:26.940] And the standard process that we apply here.
[00:42:26.940 - 00:42:30.940] This is the forcing turn that was given in the question.
[00:42:30.940 - 00:42:32.940] And these are the answers that we get out.
[00:42:32.940 - 00:42:40.870] I'm sorry, that should actually be an at symbol there,
[00:42:40.870 - 00:42:45.870] not a star.
[00:42:45.870 - 00:42:48.870] And those that are splot.
[00:42:48.870 - 00:42:52.870] Now one interesting thing here is just a little form of the
[00:42:52.870 - 00:42:54.870] way we solve this.
[00:42:54.870 - 00:42:57.870] When we solved this by hand, the first thing we did was solve
[00:42:57.870 - 00:42:59.870] the forces.
[00:42:59.870 - 00:43:01.870] Then we solved the element of fictions.
[00:43:01.870 - 00:43:04.870] And once we had that information, we could piece together the
[00:43:04.870 - 00:43:05.870] overall deflections.
[00:43:05.870 - 00:43:15.030] When we go through and do it this way, the first thing we get is
[00:43:15.030 - 00:43:17.030] actually the final answer we got before.
[00:43:17.030 - 00:43:20.030] So this is the overall deflections, which they match the numbers
[00:43:20.030 - 00:43:22.030] we just got before.
[00:43:22.030 - 00:43:27.030] So this forces millimeters and millimeters.
[00:43:27.030 - 00:43:29.030] Then we can go through and get our force in terms.
[00:43:29.030 - 00:43:32.030] So we have our force in terms F1 and F2.
[00:43:32.030 - 00:43:37.030] And we can then pull those out and then we get back to the
[00:43:37.030 - 00:43:38.030] force in terms here.
[00:43:38.030 - 00:43:42.030] So the final answer we get in this process is actually the 2.4
[00:43:42.030 - 00:43:44.030] and the 140.
[00:43:44.030 - 00:43:47.030] So that's the first thing we got when we solved it by hand.
[00:43:47.030 - 00:43:49.030] That's the last thing we get through this process.
[00:43:49.030 - 00:43:53.030] And we also get these deflection values, which are the same values
[00:43:53.030 - 00:43:56.030] that we solved by hand.
[00:43:56.030 - 00:44:02.860] So this value matching, this value, this value matching,
[00:44:02.860 - 00:44:08.860] this value, and then the put 195 there.
[00:44:08.860 - 00:44:10.860] It's a little bit of routing in there.
[00:44:10.860 - 00:44:13.860] And then those numbers matching here.
[00:44:13.860 - 00:44:28.620] We go through and we solve this.
[00:44:28.620 - 00:44:38.060] We can go through and solve this a second time.
[00:44:38.060 - 00:44:41.060] And what we have is the first time we assumed the element,
[00:44:41.060 - 00:44:43.060] this was the element orientation, the second time we flipped it
[00:44:43.060 - 00:44:45.060] to 180 degrees.
[00:44:45.060 - 00:44:48.060] This one was with X going upwards.
[00:44:48.060 - 00:44:50.060] And this is X going downwards.
[00:44:50.060 - 00:44:55.060] So we've done this with actually flipped both elements through
[00:44:55.060 - 00:44:57.060] 180 degrees.
[00:44:57.060 - 00:44:59.060] Now there are four possible combinations here.
[00:44:59.060 - 00:45:01.060] We can have this orientation.
[00:45:01.060 - 00:45:04.060] We can flip just this element or we can flip just this element
[00:45:04.060 - 00:45:05.060] or we can flip both.
[00:45:05.060 - 00:45:06.060] This is the one that's flipped both.
[00:45:06.060 - 00:45:09.060] So it's only two or four possibilities here.
[00:45:09.060 - 00:45:13.060] Not going to work through all four.
[00:45:13.060 - 00:45:16.060] By having flipped the element, what was an alpha of zero
[00:45:16.060 - 00:45:19.060] degrees now becomes an alpha of 180?
[00:45:19.060 - 00:45:24.060] What was d1 and d2 here becomes d3 and d4?
[00:45:24.060 - 00:45:27.060] What was d3 and d4 becomes d1 and d2?
[00:45:27.060 - 00:45:29.060] And the same thing happens here.
[00:45:29.060 - 00:45:35.060] What was an element orientation here of 55?
[00:45:35.060 - 00:45:40.060] Now alpha of the two is equal to 235 degrees.
[00:45:40.060 - 00:45:43.060] And the number of sequences changed.
[00:45:43.060 - 00:45:45.060] That means there are a single matrices of change.
[00:45:45.060 - 00:45:47.060] Because d1 and d2 now map d1 and d2.
[00:45:47.060 - 00:45:50.060] This is what the semi matrix looks like here, which is
[00:45:50.060 - 00:45:52.060] different to what we had here.
[00:45:52.060 - 00:45:55.060] A2 is different here to what we had here because the
[00:45:55.060 - 00:45:58.060] number of sequences changed because we've flipped the element.
[00:45:58.060 - 00:45:59.060] So quite a lot.
[00:45:59.060 - 00:46:01.060] The element orientation has changed.
[00:46:01.060 - 00:46:03.060] There are simply matrices have changed.
[00:46:03.060 - 00:46:10.650] The songs we're consistent, you'll see that it'll work itself out.
[00:46:10.650 - 00:46:11.650] So we've worked through this.
[00:46:11.650 - 00:46:14.650] One of the semi matrices are quite similar.
[00:46:14.650 - 00:46:17.650] We end up with the same result.
[00:46:17.650 - 00:46:22.660] The numbering here is the same because we've
[00:46:22.660 - 00:46:29.570] labeled the global degrees of freedom and structure the same way.
[00:46:29.570 - 00:46:33.570] And then what you'll see here in your forcing term,
[00:46:33.570 - 00:46:36.570] this forcing vector is different to this one.
[00:46:36.570 - 00:46:39.570] So true is this different to this.
[00:46:39.570 - 00:46:42.570] Well, is that something's gone wrong?
[00:46:42.570 - 00:46:43.570] Well, no, it doesn't mean anything's wrong at all.
[00:46:43.570 - 00:46:46.570] It just means that we have to take this forcing vector
[00:46:46.570 - 00:46:49.570] and interpret that relative to this free body diagram.
[00:46:49.570 - 00:46:51.570] So the three good diagrams are different.
[00:46:51.570 - 00:46:53.570] The forcing labeling is different.
[00:46:53.570 - 00:46:57.570] But as long as we take those vectors and we apply them to the
[00:46:57.570 - 00:47:01.570] corresponding free body diagram, then the final result will be the same.
[00:47:01.570 - 00:47:04.570] The same thing we can look at here is the defection vectors
[00:47:04.570 - 00:47:06.570] data of different.
[00:47:06.570 - 00:47:10.570] So we're going to look at the final result of the same.
[00:47:10.570 - 00:47:15.570] The same thing we can look at here is the defection vectors data of
[00:47:15.570 - 00:47:18.570] different.
[00:47:18.570 - 00:47:21.570] So this is a little different as to this and this.
[00:47:21.570 - 00:47:25.570] You see that the numbers have changed order.
[00:47:25.570 - 00:47:29.570] And you'll see that one was previously negative.
[00:47:29.570 - 00:47:33.570] There's now a positive and vice versa here.
[00:47:33.570 - 00:47:39.570] So within this, there's also the elements,
[00:47:39.570 - 00:47:42.570] deflections and local coordinates.
[00:47:42.570 - 00:47:45.570] So this here would actually be d1,
[00:47:45.570 - 00:47:49.570] element 1, and then this here would be d2,
[00:47:49.570 - 00:47:51.570] element 1.
[00:47:51.570 - 00:48:00.570] And in this case, now d1 for element 2 would point this way.
[00:48:00.570 - 00:48:13.380] So I'm compared with this one here.
[00:48:13.380 - 00:48:16.380] Add these, appointing in opposite directions.
[00:48:16.380 - 00:48:19.380] So they've moved from one into the other and then out pointing
[00:48:19.380 - 00:48:22.380] in opposite directions to what they were here.
[00:48:22.380 - 00:48:26.380] Which is why these vectors look different
[00:48:26.380 - 00:48:28.380] inside of these.
[00:48:28.380 - 00:48:31.380] Same thing holds true with the forcing terms if one,
[00:48:31.380 - 00:48:34.380] if one, and if two, and if two.
[00:48:34.380 - 00:48:37.380] So the one thing I just want to give you a take from that is that
[00:48:37.380 - 00:48:39.380] we work through.
[00:48:39.380 - 00:48:41.380] There's a lot of the results that look different.
[00:48:41.380 - 00:48:43.380] In between results change, vectors change,
[00:48:43.380 - 00:48:45.380] but as long as we get consistent, we're applying the same method
[00:48:45.380 - 00:48:46.380] methodology.
[00:48:46.380 - 00:48:49.380] Everything works out in the wash, and you'll be the same
[00:48:49.380 - 00:48:51.380] fine answers.
[00:48:51.380 - 00:48:53.380] Now that really concludes what we're going to do on our
[00:48:53.380 - 00:48:54.380] balance.
[00:48:54.380 - 00:48:57.380] What we're going to do and jump in on to on Monday is looking
[00:48:57.380 - 00:48:59.380] at introducing moments in sheer.
[00:48:59.380 - 00:49:01.380] Now you might think, oh, we're spending two weeks,
[00:49:01.380 - 00:49:03.380] and I'm finding some people hold with us.
[00:49:03.380 - 00:49:05.380] We're throwing everything out the window and doing another
[00:49:05.380 - 00:49:06.380] element type.
[00:49:06.380 - 00:49:10.380] Well, we can look at the more complex reaction mechanisms.
[00:49:10.380 - 00:49:13.380] And what that means is that the size of the matrix will change
[00:49:13.380 - 00:49:16.380] the specific numbers within the matrix will change,
[00:49:16.380 - 00:49:18.380] but everything still has the same meaning.
[00:49:18.380 - 00:49:20.380] The transformation still has the same meaning and does what
[00:49:20.380 - 00:49:21.380] it does now.
[00:49:21.380 - 00:49:24.380] It still benefits the other variables the same way it does now.
[00:49:24.380 - 00:49:25.380] And all that's whole stroke.
[00:49:25.380 - 00:49:27.380] So we're not throwing anything out.
[00:49:27.380 - 00:49:28.380] We're just building it on it.
[00:49:28.380 - 00:49:32.380] So thank you all for coming along, and I'll see you back in
[00:49:32.380 - 00:49:34.380] Monday and I'll try to die.
[00:49:34.380 - 00:50:33.590] Thanks.
[00:51:05.180 - 00:51:07.180] Thank you.
[00:51:35.180 - 00:51:58.740] Thank you.
[00:52:58.300 - 00:53:02.300] Thank you.

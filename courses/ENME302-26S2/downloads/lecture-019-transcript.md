# ENME302-26S2 Lecture 19 fast-pass local ASR transcript

Date: August 13, 2026 10:00am-10:55am
Transcript type: Hermes fast-pass local ASR from validated Echo audio, not a native Echo transcript.
Backend/model: faster-whisper tiny.en, CPU int8, beam_size=1, vad_filter=True.
Quality note: fast catch-up transcript. Technical terms, equations, names and Māori words need checking against slides/audio before assessment use.
Source audio SHA-256: `e58e12f32abbdaca32319194c0fb8c46892d3cbe9e37defd4e254f540d66297c`
Generated: 2026-08-13T13:10:38.212481+12:00

[00:00:36.850 - 00:00:38.850] We'll make a start.
[00:00:38.850 - 00:00:43.850] So last time we looked at some PDUs, so that was in chapter one.
[00:00:43.850 - 00:00:46.850] I'll just briefly go through what we did.
[00:00:46.850 - 00:00:54.110] We've got a part of the right class.
[00:00:54.110 - 00:00:59.110] So we've got part of the derivatives in each direction that we want to look at.
[00:00:59.110 - 00:01:04.550] So all the end of the variable, so x and y in this case, and we're looking at you.
[00:01:04.550 - 00:01:10.550] I just want to remind everyone about linear versus non-linear equations that sometimes chips people up.
[00:01:10.550 - 00:01:15.550] So like a non-linear function would be like u squared.
[00:01:15.550 - 00:01:23.550] So if you see the dependent variable times itself in a way, it will be non-linear.
[00:01:23.550 - 00:01:26.550] So this is a second order derivative in x.
[00:01:26.550 - 00:01:29.550] So even though it's got a squared term, it's not on the u.
[00:01:29.550 - 00:01:31.550] It's just differentiating u twice.
[00:01:31.550 - 00:01:36.550] So if you think of displacement, it would be like acceleration.
[00:01:36.550 - 00:01:40.550] So we have a 1.5 is an example of a non-linear equation.
[00:01:40.550 - 00:01:44.550] So it's got d squared u by d squared to power 3.
[00:01:44.550 - 00:01:48.550] So it's being cubed. So there's some non-linear.
[00:01:48.550 - 00:01:54.550] So we're going to look at mostly linear equations in this class, because it's much easier than non-linear equations.
[00:01:54.550 - 00:01:59.120] So, yep, this one is like that out.
[00:01:59.120 - 00:02:07.580] And we looked at homogeneous terms whether or not it's got a source term on the right hand side.
[00:02:07.580 - 00:02:13.580] So classifying PDEs, we've got a few different cases.
[00:02:13.580 - 00:02:18.580] So we're going to look at elliptic, parabolic and hyperbolic equations in this class.
[00:02:18.580 - 00:02:20.580] How do we know which one is which?
[00:02:20.580 - 00:02:25.580] So what we're going to look at is the coefficients in front of the derivative terms.
[00:02:25.580 - 00:02:32.580] So we're mostly going to look at linear second order PDEs because they sharpen engineering a lot more than others.
[00:02:32.580 - 00:02:35.580] So that's what we're going to focus on.
[00:02:35.580 - 00:02:38.580] And if we have two independent rebels, for example x and y,
[00:02:38.580 - 00:02:40.580] but they don't have to be x and y.
[00:02:40.580 - 00:02:43.580] They could be x and t or any other independent rebels.
[00:02:43.580 - 00:02:45.580] This is just a general form.
[00:02:45.580 - 00:02:50.580] We're going to place coefficients a through g for each term.
[00:02:50.580 - 00:02:53.580] And these also may depend on x and y.
[00:02:53.580 - 00:02:55.580] So just some terminology.
[00:02:55.580 - 00:03:01.580] And we're going to look at the coefficients a, b and z to figure out whether it's elliptic, parabolic or hyperbolic.
[00:03:01.580 - 00:03:07.920] And this is going to be helpful because we can tackle the problems in different ways.
[00:03:07.920 - 00:03:09.920] So if it's elliptic, we might use one approach.
[00:03:09.920 - 00:03:12.920] If it's parabolic or hyperbolic, we might use other approaches.
[00:03:12.920 - 00:03:17.920] So elliptic, for example, is the Laplace equation that we looked at earlier.
[00:03:17.920 - 00:03:21.920] Parabolic would be the heat equation and hyperbolic, the wave equation.
[00:03:21.920 - 00:03:28.920] So the way the equation is what we saw in that first day on Monday with the tsunamis.
[00:03:28.920 - 00:03:30.920] So you can see those ripples.
[00:03:30.920 - 00:03:32.920] So they have quite different behavior and characteristics.
[00:03:32.920 - 00:03:39.540] And you can imagine maybe solving them would be slightly different.
[00:03:39.540 - 00:03:41.540] So we go through these three examples.
[00:03:41.540 - 00:03:44.540] The first one we're going to look at is the Laplace equation.
[00:03:44.540 - 00:04:00.900] So this is a steady state and two dimensions to the.
[00:04:00.900 - 00:04:09.380] For example, if we want to look at the steady state distribution within a thin plate,
[00:04:09.380 - 00:04:16.380] it would be d squared t by dx squared plus d squared t by dy squared.
[00:04:16.380 - 00:04:23.720] Equals zero. And we'll drive that in the next chapter, chapter two.
[00:04:23.720 - 00:04:25.720] But for now you can just trust me.
[00:04:25.720 - 00:04:32.720] So we're going to look at matching the coefficients from our general form equation 1.5.
[00:04:32.720 - 00:04:37.720] 1.9, so against our Laplace equation.
[00:04:37.720 - 00:04:41.720] So we're trying to identify the coefficients a, b, and z.
[00:04:41.720 - 00:04:45.720] And then we're going to evaluate the expression b squared minus 4ac.
[00:04:45.720 - 00:04:48.720] So it's actually good determinant.
[00:04:48.720 - 00:04:52.720] And figure out if it's positive, negative, or equal to zero.
[00:04:52.720 - 00:04:56.720] And that's identified as these three different categories.
[00:04:56.720 - 00:05:03.720] So a is equal to our first, first time.
[00:05:03.720 - 00:05:06.720] So we've got d squared t by dx squared.
[00:05:06.720 - 00:05:10.720] And we've got d squared u by dx squared.
[00:05:10.720 - 00:05:13.720] We're replacing u with t is out of the variable.
[00:05:13.720 - 00:05:17.720] So a is equal to 1.
[00:05:17.720 - 00:05:21.510] Do we have any mixed partial derivatives?
[00:05:21.510 - 00:05:24.510] So d squared t by dx dy.
[00:05:24.510 - 00:05:25.510] Nope.
[00:05:25.510 - 00:05:27.510] So b is equal to zero.
[00:05:27.510 - 00:05:34.400] And then c is the coefficient in front of the second term.
[00:05:34.400 - 00:05:36.400] So d squared t by dy squared.
[00:05:36.400 - 00:05:37.400] And we've got nothing.
[00:05:37.400 - 00:05:39.400] Or just one in front of that.
[00:05:39.400 - 00:05:41.400] So c is equal to 1.
[00:05:41.400 - 00:05:48.320] And if we evaluate e squared, so that's zero minus 4,
[00:05:48.320 - 00:05:50.320] times 1 times 1.
[00:05:50.320 - 00:05:53.320] We get minus 4, which is this in zero.
[00:05:53.320 - 00:05:58.320] And this is our lip pick for the dip equation.
[00:05:58.320 - 00:06:01.320] So that's the first equation.
[00:06:01.320 - 00:06:05.320] So parabolic, sort of the classical example is the heat equation.
[00:06:05.320 - 00:06:09.720] This one's time dependent.
[00:06:09.720 - 00:06:14.500] It depends on time.
[00:06:14.500 - 00:06:20.500] So we have those initial conditions, as well as the boundary conditions.
[00:06:20.500 - 00:06:26.900] We're just going to look at 1d for this example.
[00:06:26.900 - 00:06:29.900] So we have the first order time derivative.
[00:06:29.900 - 00:06:34.900] D capital T for temperature, d lowercase t for time.
[00:06:34.900 - 00:06:37.900] Equal to kappa.
[00:06:37.900 - 00:06:40.900] So some diffusion coefficient.
[00:06:40.900 - 00:06:51.620] D squared t by dx squared.
[00:06:51.620 - 00:06:52.620] We'll do that same process.
[00:06:52.620 - 00:06:53.620] A, B, and C.
[00:06:53.620 - 00:06:56.620] So a, well, I guess hold on.
[00:06:56.620 - 00:06:59.620] Maybe we can think about which side of the equation
[00:06:59.620 - 00:07:01.620] should be move all the terms to it.
[00:07:01.620 - 00:07:04.620] So we're trying to match up with equation 1.9.
[00:07:04.620 - 00:07:08.620] We can identify that all the derivatives are on the left-hand side.
[00:07:08.620 - 00:07:11.620] And there's a source term on the right.
[00:07:11.620 - 00:07:17.620] So you want to be careful with how you pick the coefficients A through g.
[00:07:20.210 - 00:07:24.210] For simplicity, we're just going to look at the right-hand side start with.
[00:07:24.210 - 00:07:28.210] So the coefficient in front of the second order derivative, then x.
[00:07:28.210 - 00:07:32.210] So d squared t by dx squared is equal to a.
[00:07:32.210 - 00:07:36.740] So a is equal to kappa.
[00:07:36.740 - 00:07:45.680] Maybe it's not the best handwriting, but that's the fancy looking k.
[00:07:45.680 - 00:07:50.680] So b is the next partial derivative coefficient.
[00:07:50.680 - 00:07:51.680] We don't have any of those terms.
[00:07:51.680 - 00:07:53.680] So b is equal to zero.
[00:07:53.680 - 00:08:03.180] And c is the second order derivative and time that we don't have any of those.
[00:08:03.180 - 00:08:08.180] So that would be d squared t by dt squared.
[00:08:08.180 - 00:08:13.320] We evaluate again b squared minus 4 at c.
[00:08:13.320 - 00:08:17.320] B squared is zero minus 4 times kappa times zero.
[00:08:17.320 - 00:08:18.320] Zero.
[00:08:18.320 - 00:08:20.320] So we have a parabolic equation.
[00:08:20.320 - 00:08:21.320] A square of the equation.
[00:08:21.320 - 00:08:29.540] The last example, the hyperbolic, we're going to analyze the wave equation.
[00:08:29.540 - 00:08:37.570] And we'll dedicate whole chapters on each of these equations.
[00:08:37.570 - 00:08:41.570] So you'll get more familiar with them and deriving them and then
[00:08:41.570 - 00:08:47.570] how to solve them analytically and then numerically with our finite different tools.
[00:08:47.570 - 00:08:51.570] So the wave equation is also time dependent.
[00:08:51.570 - 00:09:00.390] And for this example, we're just looking in 1d.
[00:09:00.390 - 00:09:04.390] So one special dimension.
[00:09:04.390 - 00:09:08.390] And we've got a second order derivative in space.
[00:09:08.390 - 00:09:10.390] d squared u by dx squared.
[00:09:10.390 - 00:09:12.390] So u is the displacement.
[00:09:12.390 - 00:09:16.390] So you can think of a good task string or a violent string or those waves in the ocean.
[00:09:16.390 - 00:09:18.390] That's representing the vertical displacement.
[00:09:18.390 - 00:09:24.390] It's being the longitudinal spatial coordinate.
[00:09:24.390 - 00:09:26.390] This is equal to 1 over c squared.
[00:09:26.390 - 00:09:29.390] So c is related to the wave number.
[00:09:29.390 - 00:09:37.140] And we've got a second order derivative and time d squared u by dt squared.
[00:09:37.140 - 00:09:45.620] You can read that OK or your squinting as well.
[00:09:45.620 - 00:09:51.700] But I'll try to write clearly.
[00:09:51.700 - 00:09:57.010] So in this case, we're going to go through the same process.
[00:09:57.010 - 00:10:02.380] Now we can't see the other equation 1.9.
[00:10:02.380 - 00:10:05.380] We're matching those coefficients a, b, and c.
[00:10:05.380 - 00:10:15.400] So which is a equal to 1?
[00:10:15.400 - 00:10:16.400] Yep.
[00:10:16.400 - 00:10:21.400] And then we've not got any partial or mixed partial derivatives of b is 0.
[00:10:21.400 - 00:10:22.400] And what about c?
[00:10:22.400 - 00:10:27.400] Now we need to be able to get for which side of the equal sign that we're looking at.
[00:10:27.400 - 00:10:35.020] So this will be capital C, I suppose, rather than like a c.
[00:10:35.020 - 00:10:46.700] So minus 1 over c squared.
[00:10:46.700 - 00:10:47.700] It's not very helpful.
[00:10:47.700 - 00:10:48.700] There's a line there.
[00:10:48.700 - 00:10:55.930] So c is equal to minus 1 over c squared.
[00:10:55.930 - 00:10:57.930] So then we're going to be at b squared minus 4,
[00:10:57.930 - 00:11:03.930] a c. So 0 minus 1 over c squared times minus 1.
[00:11:03.930 - 00:11:06.930] So minus minus is going to be positive.
[00:11:06.930 - 00:11:10.930] So we're going to have a greater than 0 expression.
[00:11:10.930 - 00:11:13.930] And this is a hyperbolic pd.
[00:11:13.930 - 00:11:23.470] So just some specification of those equations.
[00:11:23.470 - 00:11:27.470] Maybe we can try and interpret these physically.
[00:11:27.470 - 00:11:33.470] So let the problems generally a steady state value problem.
[00:11:33.470 - 00:11:37.470] So the solution at one point is influenced by all the other points.
[00:11:37.470 - 00:11:39.470] One example would be like a membrane.
[00:11:39.470 - 00:11:46.470] So if you had a thin, the formal ball material that was constrained on the
[00:11:46.470 - 00:11:48.470] the perimeter and you applied a pressure difference.
[00:11:48.470 - 00:11:50.470] So maybe you're higher pressure on the bottom.
[00:11:50.470 - 00:11:53.470] It would rise up with a peak in the middle.
[00:11:53.470 - 00:11:55.470] But it would be in steady state.
[00:11:55.470 - 00:12:06.150] For example, for membrane.
[00:12:06.150 - 00:12:10.150] So the boundary of the solution domain is closed.
[00:12:10.150 - 00:12:13.150] So we need to know the boundary conditions around the perimeter.
[00:12:13.150 - 00:12:19.150] You could imagine if we didn't know the displacement at one point,
[00:12:19.150 - 00:12:21.150] there would be infinite number of solutions.
[00:12:21.150 - 00:12:26.150] So thinking back to the class equation,
[00:12:26.150 - 00:12:29.150] 1.8, we saw that these three functions.
[00:12:29.150 - 00:12:31.150] Well, for homework, you might have done the other two.
[00:12:31.150 - 00:12:33.150] But we looked at this first one.
[00:12:33.150 - 00:12:36.150] The solutions to the Laplace equation.
[00:12:36.150 - 00:12:39.150] So there's infinite number of solutions to this equation.
[00:12:39.150 - 00:12:44.150] To be able to define a unique solution, we need to apply those boundary conditions.
[00:12:44.150 - 00:12:48.150] And if we don't have those, then we don't have a unique solution.
[00:12:48.150 - 00:12:52.150] Parabolic problems, quite diffusive in nature.
[00:12:52.150 - 00:12:57.150] We saw that it's got a diffusive term in front of the second order derivative in space.
[00:12:57.150 - 00:13:01.150] So the thermal connectivity, or related to the thermal connectivity.
[00:13:01.150 - 00:13:03.150] So essentially it's a rate.
[00:13:03.150 - 00:13:05.150] How quickly is the heat transferring?
[00:13:05.150 - 00:13:09.590] So there's some sort of time or time like coordinate.
[00:13:09.590 - 00:13:12.590] And we're generally marching forward in time.
[00:13:12.590 - 00:13:17.590] So maybe if you had coffee this morning, you added your spoon into the cup.
[00:13:17.590 - 00:13:19.590] It would heat up over time.
[00:13:19.590 - 00:13:29.260] So the solution is defined by the initial conditions.
[00:13:29.260 - 00:13:32.260] Otherwise, we can't solve it.
[00:13:32.260 - 00:13:34.260] So it's fully dependent on the initial conditions.
[00:13:34.260 - 00:13:39.260] If it starts at a higher temperature, then the solution will look different to a lower temperature.
[00:13:39.260 - 00:13:47.020] Hyperbolic problems are quite wave like or propagative.
[00:13:47.020 - 00:13:52.020] So those are those waves that we saw that were deflecting off the posts from the tsunamis.
[00:13:52.020 - 00:13:57.020] I said that a lot of them two or three years ago, the faster the nature need to sign.
[00:13:57.020 - 00:14:00.020] And actually it was last year.
[00:14:00.020 - 00:14:07.020] So they looked at the lake telephone and we had an asteroid that had to lake.
[00:14:07.020 - 00:14:09.020] And they looked at the wave, the sleeping out.
[00:14:09.020 - 00:14:11.020] So it was a good fun problem.
[00:14:11.020 - 00:14:15.020] One of the interesting challenges with hyperbolic equations is that they're quite unstable.
[00:14:15.020 - 00:14:19.020] So it's a little bit tricky to get good numerical solutions.
[00:14:19.020 - 00:14:23.020] But challenges always good.
[00:14:23.020 - 00:14:27.020] Again, there's generally a time or time like waternut.
[00:14:27.020 - 00:14:30.020] And the open boundary is sort of in time.
[00:14:30.020 - 00:14:31.020] You can go off to infinity.
[00:14:31.020 - 00:14:34.020] You might reach a sort of steady state solution maybe.
[00:14:34.020 - 00:14:37.020] But generally probably not for the hyperbolic problems.
[00:14:37.020 - 00:14:42.020] If there's no damping, you could have mentioned that if you pluck a guitar string,
[00:14:42.020 - 00:14:46.020] it would just continually propagate for infinity.
[00:14:46.020 - 00:14:49.020] It's the damping that would slide down.
[00:14:49.020 - 00:15:00.340] So, yeah, like down those examples, so spoon and hot coffee.
[00:15:00.340 - 00:15:12.860] So there's a rising temperature and it's instantaneous.
[00:15:12.860 - 00:15:21.310] As soon as the spoon touches the hot water, as I'm certainly heating up,
[00:15:21.310 - 00:15:25.310] it's not heating up to the temperature of the liquid.
[00:15:25.310 - 00:15:28.310] And instantly, but it's beginning to heat up instantly.
[00:15:28.310 - 00:15:34.310] So we can see that the change in temperature over time is proportional to the difference.
[00:15:34.310 - 00:15:37.310] So the second order derivative of the square t by dx squared.
[00:15:37.310 - 00:15:52.050] And the last example for the wave equation, we said the ocean wave will maybe a tight rope.
[00:15:52.050 - 00:16:02.260] So these solutions are also disseminated by the initial conditions.
[00:16:02.260 - 00:16:07.260] But the information or wave sort of propagates with the finite speed.
[00:16:07.260 - 00:16:13.260] You can usually, while you can see waves in the ocean, as they move across.
[00:16:13.260 - 00:16:20.690] And guitar strings, I guess if you have a high speed camera, you could capture that as well.
[00:16:20.690 - 00:16:26.690] All right, so that's sort of some of the physical reasoning for those three types of equations.
[00:16:26.690 - 00:16:35.690] So according to our definition earlier, Hd is homogeneous if the source term on that right hand side, g.
[00:16:35.690 - 00:16:39.690] So we're saying source term because it isn't a function of the dependable.
[00:16:39.690 - 00:16:43.690] So it's not a function of the temperature directly.
[00:16:43.690 - 00:16:46.690] And it's homogeneous if g is equal to zero.
[00:16:46.690 - 00:16:58.980] So just some terminology, it'll come into play later on.
[00:16:58.980 - 00:17:04.980] So if the coefficients are constant, it's so h root g.
[00:17:04.980 - 00:17:07.980] The pd is to have constant coefficient.
[00:17:07.980 - 00:17:08.980] So it's easy to remember.
[00:17:08.980 - 00:17:12.980] The pd in equation 1.9 was written in terms of x and y.
[00:17:12.980 - 00:17:16.980] But we can also apply it to other infinite variables such as x and t.
[00:17:16.980 - 00:17:20.980] So it's what we did for our parabolic and high-volic examples.
[00:17:20.980 - 00:17:32.970] Now some examples of pd is an engineering.
[00:17:32.970 - 00:17:34.970] So what can we use these for?
[00:17:34.970 - 00:17:36.970] So we already looked at the last equation.
[00:17:36.970 - 00:17:39.970] So this would be an example of a steady state heat transfer within a plate.
[00:17:39.970 - 00:17:42.970] And we'll drive that in chapter two.
[00:17:42.970 - 00:17:44.970] So there's infinite variables, temperature.
[00:17:44.970 - 00:17:47.970] We could also look at ground water flow through an aquifer.
[00:17:47.970 - 00:17:50.970] So we did assign it on this a few years ago as well.
[00:17:50.970 - 00:17:52.970] So essentially we're looking at the hydraulic head.
[00:17:52.970 - 00:17:57.970] So h being the variable that's viewing throughout the aquifer and the ground.
[00:17:57.970 - 00:18:01.970] And we're seeing how it varies in space, x and y.
[00:18:01.970 - 00:18:05.970] The last examples for those electronic students don't feel left out with the next
[00:18:05.970 - 00:18:08.970] values equation looking at electric potential.
[00:18:08.970 - 00:18:14.970] I don't know too much about that, but that's another example.
[00:18:14.970 - 00:18:21.910] And parabolic, so transient heat conduction.
[00:18:21.910 - 00:18:25.910] So instead of using keper, if we break it out to row c and k,
[00:18:25.910 - 00:18:28.910] it might be more familiar for those terms.
[00:18:28.910 - 00:18:32.910] And we might be looking at the heating or cooling of a long thin rod.
[00:18:32.910 - 00:18:34.910] So we'd have different boundary connotations.
[00:18:34.910 - 00:18:36.910] It might be convicted of heat transfer.
[00:18:36.910 - 00:18:38.910] We might have a source term.
[00:18:38.910 - 00:18:42.910] We might have a fixed boundary condition, etc.
[00:18:42.910 - 00:18:46.910] But we need an initial condition and also a boundary condition as well.
[00:18:46.910 - 00:18:48.910] The solve.
[00:18:48.910 - 00:18:51.910] So this is first order and time.
[00:18:51.910 - 00:18:53.910] So we need to have one initial condition.
[00:18:53.910 - 00:18:56.910] It's second order in space and one coordinate.
[00:18:56.910 - 00:18:58.910] So we need two boundary conditions.
[00:18:58.910 - 00:19:00.910] So that's just a rule of thumb.
[00:19:00.910 - 00:19:05.910] This first case we've got two second order and x, second order and y.
[00:19:05.910 - 00:19:07.910] So two boundary conditions.
[00:19:07.910 - 00:19:10.910] So we need four boundary conditions to solve that unit.
[00:19:10.910 - 00:19:12.910] Let's just a bit of a side note.
[00:19:12.910 - 00:19:17.910] And fixed law can be used to describe species diffusion.
[00:19:17.910 - 00:19:20.910] So here, five represents the concentration.
[00:19:20.910 - 00:19:27.910] So if we have a beaker of water and we insert some dye and we watch it diffuse out.
[00:19:27.910 - 00:19:31.910] If we don't do any mixing, so we don't have any conviction,
[00:19:31.910 - 00:19:34.910] it's only going to distribute by diffusion.
[00:19:34.910 - 00:19:36.910] And that's what this term represents.
[00:19:36.910 - 00:19:39.910] So d, d squared, phi by dx squared.
[00:19:39.910 - 00:19:41.910] These are diffusion coefficient.
[00:19:41.910 - 00:19:45.910] So if you have already high diffusion coefficient, it would diffuse quicker.
[00:19:45.910 - 00:19:48.910] Because it's directly related to the change of phi at the time.
[00:19:48.910 - 00:19:57.640] So all of these equations, that's mass, but they sort of represent what's observed in life.
[00:19:57.640 - 00:20:01.640] So, yeah, you can think of it in real terms.
[00:20:01.640 - 00:20:09.920] So last example is the hyperbolic equations of the wave equation, which is the tricky or tricky year one.
[00:20:09.920 - 00:20:11.920] So we've got some vertical displacement u.
[00:20:11.920 - 00:20:18.920] We've got a wave, a speed or wave propagation of c, related to the tension and row.
[00:20:18.920 - 00:20:28.420] And if to look at what row represented, I think it's the density of the string or wave.
[00:20:28.420 - 00:20:30.420] So c is the speed of sound.
[00:20:30.420 - 00:20:36.420] If we see as a bit, the speed of sound and u is the pressure,
[00:20:36.420 - 00:20:39.420] we can also look at sound propagation.
[00:20:39.420 - 00:20:49.740] So looking at acoustic problems as well.
[00:20:49.740 - 00:20:53.740] Any questions on these definitions?
[00:20:53.740 - 00:21:01.480] It's all sort of making sense.
[00:21:01.480 - 00:21:05.480] We've got some exercises to practice, so that's good.
[00:21:05.480 - 00:21:11.480] So as I say, each chapter has a, well, I think most chapters have exercises at the end of them.
[00:21:11.480 - 00:21:14.480] And the solutions are in the back of the book.
[00:21:14.480 - 00:21:21.480] We'll spend five or ten minutes to go through these just to get you, I don't know, in the swing of things.
[00:21:21.480 - 00:21:26.480] So when we get to each end of chapter, you can work on exercises.
[00:21:26.480 - 00:21:30.480] So the first one, we're going to look at that little class equation.
[00:21:30.480 - 00:21:36.480] equation one, ten, d squared t by dx squared plus d squared t by dy squared, equal to zero.
[00:21:36.480 - 00:21:42.480] So if we have two generic functions, t1 and t2,
[00:21:42.480 - 00:21:46.480] and these are solutions to our Laplace equation.
[00:21:46.480 - 00:21:57.450] So for example, we just choose two of these, but we're saying that the arbitrary, so that any new function.
[00:21:57.450 - 00:22:02.450] Then we're going to show that a combination, a linear combination of those two.
[00:22:02.450 - 00:22:11.450] So alpha and beta being some constant values, multiplied by those two functions, is also a solution to the Laplace equation.
[00:22:11.450 - 00:22:13.450] So this is essentially the superpositioning principle.
[00:22:13.450 - 00:22:20.450] So it can we have a series of functions added together that it's also a solution to the Laplace equation.
[00:22:20.450 - 00:22:27.870] So how can we go about showing that, do you think?
[00:22:27.870 - 00:22:33.600] It's very similar to what we did last time.
[00:22:33.600 - 00:23:25.800] We're told that t1 and t2 are solutions to our Laplace equation.
[00:23:25.800 - 00:23:30.800] And we're trying to figure out if the combination of those two solutions are also a solution.
[00:23:30.800 - 00:23:40.450] So we're going to insert our assumed function into our equation.
[00:23:40.450 - 00:23:43.450] So t equal alpha t1 plus beta t2.
[00:23:43.450 - 00:24:04.700] So substituted t into our Laplace equation plus second order ny.
[00:24:04.700 - 00:24:15.170] And if that holds true, then we know it's equal to zero.
[00:24:15.170 - 00:24:22.580] So we're going to check for that.
[00:24:22.580 - 00:24:25.580] What do we know about derivatives can we break these up?
[00:24:25.580 - 00:24:51.310] So the derivative of alpha t1 plus beta t2 is equal to the derivative of alpha t1 plus beta t2.
[00:24:51.310 - 00:24:57.320] That's one of the rules of differentiation.
[00:24:57.320 - 00:25:02.840] And we'll do the same for the second term.
[00:25:02.840 - 00:25:10.840] So we've got d squared by dy squared of alpha t1 plus d squared t by dy squared of beta.
[00:25:10.840 - 00:25:11.840] Sorry.
[00:25:11.840 - 00:25:12.840] Yep, beta t2.
[00:25:12.840 - 00:25:33.350] What else can we do to this equation?
[00:25:33.350 - 00:25:36.350] What do we know about alpha and beta?
[00:25:36.350 - 00:25:37.350] These are constants.
[00:25:37.350 - 00:25:50.500] So constants could be taken outside of the derivative.
[00:25:50.500 - 00:25:52.500] So you could use the product rule.
[00:25:52.500 - 00:25:55.500] We'll just go straight to checking it outside the derivative.
[00:25:55.500 - 00:26:01.500] So we know the derivative of alpha being a constant by dx squared is going to be equal to zero.
[00:26:01.500 - 00:26:06.500] So by the product rule, we've got alpha d squared t1 by dx squared.
[00:26:06.500 - 00:26:13.900] Do the same for each term.
[00:26:13.900 - 00:26:26.900] So we've got beta multiplied by d squared t2 by dx squared plus alpha d squared t1 by dy squared.
[00:26:26.900 - 00:26:30.900] And beta d squared t2 by dy squared.
[00:26:30.900 - 00:26:37.240] So simplified or expanded each term.
[00:26:37.240 - 00:26:44.970] Now we've been informed that t1 and t2 are solutions to the equation.
[00:26:44.970 - 00:26:56.970] So we know that d squared t1 by dx squared plus d squared t1 by dy squared is equal to zero.
[00:26:56.970 - 00:27:08.970] And d squared t2 by dx squared plus d squared t2 by dy squared is equal to zero.
[00:27:08.970 - 00:27:10.970] So we're given that.
[00:27:10.970 - 00:27:15.970] We're going to try and adapt our equation with these terms.
[00:27:15.970 - 00:27:19.970] So we're going to group coefficients.
[00:27:19.970 - 00:27:21.970] Alpha and beta.
[00:27:21.970 - 00:27:30.080] So we've got alpha d squared t1 by dx squared.
[00:27:30.080 - 00:27:36.080] And we've got d squared t1 by dy squared.
[00:27:36.080 - 00:27:40.080] So that's these two terms.
[00:27:40.080 - 00:27:52.420] And the coefficient beta has the terms d squared t2 by dx squared plus d squared t2 by dy squared.
[00:27:52.420 - 00:28:03.310] So a little bit of manipulation with the equation.
[00:28:03.310 - 00:28:10.310] But yeah, this is still holds true to what we said initially.
[00:28:10.310 - 00:28:16.310] Now we've said that this expression is equal to zero.
[00:28:16.310 - 00:28:23.310] And this expression is equal to zero also because we said that they were solutions to the past equation.
[00:28:23.310 - 00:28:32.310] So we have confirmed that a linear combination of solutions to the past equation is also a solution to the past equation.
[00:28:32.310 - 00:28:34.310] Which is pretty neat because it's sort of a linear superpositioning.
[00:28:34.310 - 00:28:38.310] So if we found one solution that satisfy the whole past equation and another,
[00:28:38.310 - 00:28:41.310] we could add them together and that also be a solution.
[00:28:41.310 - 00:28:47.310] So that will come in useful later on for some of our analytical solutions.
[00:28:47.310 - 00:28:54.170] But it's just a way of sort of showing you and proving to you that it works okay.
[00:28:54.170 - 00:29:04.980] And a little bit of a refresher of how they're able to work.
[00:29:04.980 - 00:29:10.980] The next question is asking us to show that doesn't hold when we've got a source term on the right hand side.
[00:29:10.980 - 00:29:16.980] So if we've got a source term, so if of x and y, this is called the Poisson equation.
[00:29:16.980 - 00:29:21.980] So it's got a special name as well because it's quite a common one.
[00:29:21.980 - 00:29:24.980] Yeah. And we want to figure out, well,
[00:29:24.980 - 00:29:28.980] at first of all, is the Poisson equation homogeneous?
[00:29:28.980 - 00:29:31.980] No. No. Because it's got that source term.
[00:29:31.980 - 00:29:36.970] And you want to, so I'm not going to go through that work.
[00:29:36.970 - 00:29:40.970] Because it's very similar and you can do that for homework.
[00:29:40.970 - 00:29:43.970] But you'll find that it shouldn't hold.
[00:29:43.970 - 00:29:54.710] All right. We can do one of these, I guess.
[00:29:54.710 - 00:30:03.040] So I'll give you a couple of minutes to work through, but maybe do the second one.
[00:30:03.040 - 00:30:11.040] So if we've got x cubed minus 3xy squared is this function, our solution to the Laplace equation.
[00:30:11.040 - 00:30:18.630] So your Plagarism, let's take me to what we just, what we've just done.
[00:30:18.630 - 00:31:04.130] So it's the same, same as in.
[00:31:04.130 - 00:31:10.130] So we've got our Laplace equation, which has this sort of form d squared, d squared by d x squared,
[00:31:10.130 - 00:31:12.130] and d squared by d y squared.
[00:31:12.130 - 00:31:19.590] And we're going to answer our function t, which is x cubed.
[00:31:19.590 - 00:31:22.590] Minus 3xy squared.
[00:31:22.590 - 00:31:30.560] And evaluate these second order derivatives.
[00:31:30.560 - 00:31:46.660] So if we differentiate these terms once, so we've got 3x squared minus 3y squared.
[00:31:46.660 - 00:31:49.660] And d by d y.
[00:31:49.660 - 00:31:56.660] So x cubed is just going to be zero. And we left with minus 6xy.
[00:31:56.660 - 00:32:01.480] And we differentiate again.
[00:32:01.480 - 00:32:03.480] So now we've got 6x.
[00:32:03.480 - 00:32:08.760] 3y squared is zero when we differentiate with respect to x.
[00:32:08.760 - 00:32:11.760] And this one's going to be minus 6x.
[00:32:11.760 - 00:32:21.460] So we can confirm that that function, x cubed minus 3xy squared, is a solution to the Laplace equation.
[00:32:21.460 - 00:32:41.680] Any questions on the formatting PDFs?
[00:32:41.680 - 00:32:44.680] Check the one.
[00:32:44.680 - 00:33:08.820] So I've been through the feedback for the survey from yesterday, so I can share.
[00:33:08.820 - 00:33:25.170] I don't know what this computer doesn't like me or something.
[00:33:25.170 - 00:33:30.170] The PDF is a very problematic.
[00:33:30.170 - 00:34:14.940] Yeah, we went through some of these before, but just to reiterate, I guess there's a mixture within the class.
[00:34:14.940 - 00:34:19.940] And it's mostly hovering around neutral with a little bit of a bias between disagreeing.
[00:34:19.940 - 00:34:32.980] And a lot of you felt that some tools for certain parts of the assessment would be worthwhile.
[00:34:32.980 - 00:34:36.980] And I did read through the comments.
[00:34:36.980 - 00:34:38.980] So I just wanted to spend a few minutes to get to the recipes.
[00:34:38.980 - 00:34:45.980] I think it's quite important for the scores especially with the last couple of years with the whole introduction of algorithms.
[00:34:45.980 - 00:34:47.980] So they're large language models.
[00:34:47.980 - 00:34:55.980] So I've highlighted some just because they're represented with a sample of the rest of them.
[00:34:55.980 - 00:35:03.980] So obviously, yeah, using for top of treating and debugging is obviously a very handy tool for following through your code.
[00:35:03.980 - 00:35:05.980] So you can understand that.
[00:35:05.980 - 00:35:08.980] We should be using AI for the scores.
[00:35:08.980 - 00:35:11.980] There's one of the opinions.
[00:35:11.980 - 00:35:16.980] Some feeling that it's not used.
[00:35:16.980 - 00:35:19.980] I'm not being too interested in selling the topic.
[00:35:19.980 - 00:35:23.980] So this understanding probably how it will be done in future.
[00:35:23.980 - 00:35:25.980] So I guess this is also in the back of my mind.
[00:35:25.980 - 00:35:28.980] So what should we be teaching you?
[00:35:28.980 - 00:35:30.980] So AI is efficient.
[00:35:30.980 - 00:35:32.980] So as long as it was checked over.
[00:35:32.980 - 00:35:37.980] So the checking over at least at the moment seems to be a really key part of those models.
[00:35:37.980 - 00:35:41.980] And if you don't know what it should be, then you can't be the purifier.
[00:35:41.980 - 00:35:45.980] And if you can't be the purifier, then they're going to employ someone else that can.
[00:35:45.980 - 00:35:49.980] So I feel like it's important to know how it should be done.
[00:35:49.980 - 00:35:52.980] And then you're sort of overseeing the coding process.
[00:35:52.980 - 00:35:58.860] Explaining and troubleshooting code.
[00:35:58.860 - 00:36:02.860] And giving direction if you're completely lost.
[00:36:02.860 - 00:36:09.860] And now I have noticed even just in the last couple of years, the number of questions that I get in the labs has diminished.
[00:36:09.860 - 00:36:12.860] Which makes my job easier.
[00:36:12.860 - 00:36:17.860] But yeah, I guess that's only one way to look at it.
[00:36:17.860 - 00:36:20.860] So you shouldn't be entirely relying on it, but it will be used at it at B.
[00:36:20.860 - 00:36:26.860] So I understand that's a very little bit of a common thought.
[00:36:26.860 - 00:36:30.860] Finds to use when the coding isn't the learning, which is true.
[00:36:30.860 - 00:36:37.860] So this course is sort of the mechanics or the algorithms that are required for the
[00:36:37.860 - 00:36:39.860] discretization of numerical methods.
[00:36:39.860 - 00:36:43.860] So we are trying to teach you how it all works.
[00:36:43.860 - 00:36:46.860] So once you have a better understanding of what convergence,
[00:36:46.860 - 00:36:49.860] those consistency in our numerical methods,
[00:36:49.860 - 00:36:52.860] then you can apply these tools in a workplace.
[00:36:52.860 - 00:36:56.860] I guess more directly next year for your research projects.
[00:36:56.860 - 00:37:02.860] So if you skip that step, you're just going to be running in blind and hoping that it's correct.
[00:37:02.860 - 00:37:07.860] So that applies to both console when you commercial software that you're using,
[00:37:07.860 - 00:37:17.140] as well as large-language models.
[00:37:17.140 - 00:37:25.140] So they are using AI in the workplace in some cases that I'm aware of.
[00:37:25.140 - 00:37:27.140] I think at the university level,
[00:37:27.140 - 00:37:31.140] first thing I feel like you should be learning for yourself,
[00:37:31.140 - 00:37:36.140] rather than outsourcing that learning, obviously it's going to be quicker and easier for check tbte
[00:37:36.140 - 00:37:39.140] or some other model to do the problems.
[00:37:39.140 - 00:37:42.140] I don't know if they can do the quizzes themselves.
[00:37:42.140 - 00:37:44.140] I haven't tried that out.
[00:37:44.140 - 00:37:48.140] I feel like that defeats the purpose entirely.
[00:37:48.140 - 00:37:54.780] Not useful if you don't have access to this.
[00:37:54.780 - 00:38:02.780] So last year I had a question on an exam for coding.
[00:38:02.780 - 00:38:06.780] Just I guess there's one way to address the challenge of individual coding.
[00:38:06.780 - 00:38:11.780] So the class was asked to debug some code that I had prepared.
[00:38:11.780 - 00:38:20.780] And it was five marks and the average and the class was 34.6% which was not great.
[00:38:20.780 - 00:38:22.780] I guess I wasn't too surprised.
[00:38:22.780 - 00:38:27.780] There was I think three or four students that got all the areas identified and corrected, which was cool.
[00:38:27.780 - 00:38:35.780] But I feel if you've done any debugging, it would have been quite obvious which areas were present in the code.
[00:38:35.780 - 00:38:39.780] And there were problems that I sort of went through in class quite a bit as well.
[00:38:39.780 - 00:38:45.780] There was a gimme question that 95% got for one mark.
[00:38:45.780 - 00:38:54.780] So all of the coding questions in that exam was average of 44.8% for six marks,
[00:38:54.780 - 00:38:58.780] which was 10% of this exam which is 5% of course grade.
[00:38:58.780 - 00:39:00.780] So as much as all because it's combined.
[00:39:00.780 - 00:39:08.780] So I guess in context, I think it's worthwhile trying to understand the coding so that you can do well in the exam.
[00:39:08.780 - 00:39:12.780] So that you get that 40% threshold to pass the course.
[00:39:12.780 - 00:39:18.700] So it could be helpful engineering, base code.
[00:39:18.700 - 00:39:22.700] So the code that we do in this class is reasonably short, especially the quizzes.
[00:39:22.700 - 00:39:24.700] It'll be like a handful of lines of code.
[00:39:24.700 - 00:39:30.700] So I don't think it's not onerous to work through.
[00:39:30.700 - 00:39:38.650] I've not adjusted the course since AI has been in common use.
[00:39:38.650 - 00:39:43.650] So I also understand how to control those videos to not restrict it.
[00:39:43.650 - 00:39:52.650] So one of the students last year and for me that, yeah, they had worked through the problem and I guess struggled through the coding.
[00:39:52.650 - 00:39:58.650] And felt disadvantage because some others had used AI models.
[00:39:58.650 - 00:40:03.650] Again, I feel like they would be good off for the exam and better prepared.
[00:40:03.650 - 00:40:14.650] And yeah, I guess it's a bit cheesy, but you may be just treating yourself if you're just using external tools.
[00:40:14.650 - 00:40:23.020] So again, generally, I am not used, understanding how it works as valuable.
[00:40:23.020 - 00:40:26.020] Using AI as a generic code is good.
[00:40:26.020 - 00:40:29.020] Testing exam is invigilated, so I've talked to that.
[00:40:29.020 - 00:40:35.020] Debugging is neat. Sometimes if I'm completely stuck, I can sort of help you through.
[00:40:35.020 - 00:40:39.020] So I've tried to get a scaffold through the course.
[00:40:39.020 - 00:40:43.020] So we go through the chapter and work through derivations and examples.
[00:40:43.020 - 00:40:47.020] Then you apply that knowledge to the exercises and work through those.
[00:40:47.020 - 00:40:50.020] And I provide the model solutions in the back of the book.
[00:40:50.020 - 00:40:52.020] So that's one step.
[00:40:52.020 - 00:40:58.020] And then the next step is the quizzes to sort of apply that learning and then you're the exam at the end.
[00:40:58.020 - 00:41:06.020] So if you're stuck with exercises, I guess that's a good place to sort of use external tools.
[00:41:06.020 - 00:41:15.580] But we've also got the model solutions here as well.
[00:41:15.580 - 00:41:17.580] So I don't know if I can let anyone.
[00:41:17.580 - 00:41:22.580] I hope you have to mention some people are not to use AI for the quizzes.
[00:41:22.580 - 00:41:30.340] So I've added, that's a bit.
[00:41:30.340 - 00:41:34.340] It's really aggressive looking, but that's a little bit.
[00:41:34.340 - 00:41:37.340] assessment tool that we're supposed to include.
[00:41:37.340 - 00:41:40.340] So yeah, don't use that AI for the quizzes themselves.
[00:41:40.340 - 00:41:47.340] If you're stuck with a particular problem, maybe work through those examples outside of the quiz.
[00:41:47.340 - 00:41:51.340] But the quiz, I mean the quiz is quite short, but yeah.
[00:41:51.340 - 00:41:57.340] So use them as an opportunity to learn.
[00:41:57.340 - 00:42:01.340] A couple of years ago, based on feedback, I made the quizzes optional.
[00:42:01.340 - 00:42:08.340] So they didn't contribute to the course waiting to have this pressure and they have more time to do the rubric up.
[00:42:08.340 - 00:42:14.340] But I think by that quiz 4 or 5, I think 5% of the class had assembled it.
[00:42:14.340 - 00:42:17.340] So it's quite, it's really low, I think.
[00:42:17.340 - 00:42:25.340] So I've gone back to having a normal amount, so 1% of the course grade for each quiz.
[00:42:25.340 - 00:42:28.340] And yeah, that's the case for this year.
[00:42:28.340 - 00:42:32.380] I don't know what I'll do for next year.
[00:42:32.380 - 00:42:36.380] I've tried to increase zero, because Python actually started zero.
[00:42:36.380 - 00:42:45.060] And this is just so that you get familiar with all the different question types.
[00:42:45.060 - 00:42:47.060] So it opens today and finishes tomorrow.
[00:42:47.060 - 00:42:51.060] So there's a multi-choice, so lots of current year, some even.
[00:42:51.060 - 00:42:53.060] So I have to update this each year.
[00:42:53.060 - 00:42:56.060] So it should be right this year.
[00:42:56.060 - 00:43:00.060] So we're going to have the following numbers even.
[00:43:00.060 - 00:43:03.060] So this is what I call a stack.
[00:43:03.060 - 00:43:05.060] Yeah, this one's a stack question.
[00:43:05.060 - 00:43:08.060] So it allows algebraic input.
[00:43:08.060 - 00:43:11.060] And we'll use this for the separation of variables they run.
[00:43:11.060 - 00:43:14.060] It allows you to type numbers.
[00:43:14.060 - 00:43:19.060] And so it's three times x squared over three.
[00:43:19.060 - 00:43:21.060] Well, you could just do x squared.
[00:43:21.060 - 00:43:23.060] So this is interpreted as the separation.
[00:43:23.060 - 00:43:27.060] You've probably seen in your math courses, but it's quite neat.
[00:43:27.060 - 00:43:28.060] So you could type that.
[00:43:28.060 - 00:43:30.060] Well, you could type x squared.
[00:43:30.060 - 00:43:34.980] And they should be the same answer.
[00:43:34.980 - 00:43:37.980] Question four is an example of using code.
[00:43:37.980 - 00:43:40.980] So using code banner.
[00:43:40.980 - 00:43:41.980] I think it's actually one out.
[00:43:41.980 - 00:43:44.980] Well, it's been developed by some over-and-computers science.
[00:43:44.980 - 00:43:46.980] So that's pretty cool.
[00:43:46.980 - 00:43:52.980] So this plug-in into the Moodle and to what learn uses allows us to evaluate
[00:43:52.980 - 00:43:55.980] reasonably short snippets of code, because it's one on the server.
[00:43:55.980 - 00:43:58.980] We don't want to run massive functions.
[00:43:58.980 - 00:44:05.980] So here you want to write out Python, Python function, which is square.
[00:44:05.980 - 00:44:08.980] And we have an input argument.
[00:44:08.980 - 00:44:11.980] Maybe as an example is minus 4 and 7.
[00:44:11.980 - 00:44:13.980] And this is expected result.
[00:44:13.980 - 00:44:16.980] So define our function square.
[00:44:16.980 - 00:44:18.980] And we want to return a value.
[00:44:18.980 - 00:44:21.980] So if we want to square, we can go in times n.
[00:44:21.980 - 00:44:27.980] I think the Python one for exponents is the double asterisks.
[00:44:27.980 - 00:44:34.500] So we can pre-check.
[00:44:34.500 - 00:44:38.500] It's going to compare against the two cases that are provided here.
[00:44:38.500 - 00:44:40.500] There's examples.
[00:44:40.500 - 00:44:44.500] I've added an third example, which is using the same function.
[00:44:44.500 - 00:44:46.500] But you don't have the result.
[00:44:46.500 - 00:44:50.500] Because otherwise you just do n is minus 4 returns 16.
[00:44:50.500 - 00:44:54.500] So you sort of bypass that, which I think only two students have actually tried that in the past.
[00:44:54.500 - 00:44:56.500] I don't know why they've got it through that.
[00:44:56.500 - 00:45:05.860] It does have a third, a third check just so it doesn't circumvent that code.
[00:45:05.860 - 00:45:15.650] If you had a typo, the pre-check will inform you that you've got some error.
[00:45:15.650 - 00:45:17.650] So there's some basic checking here.
[00:45:17.650 - 00:45:22.650] But you might want to develop the functions in spider or something outside and then copy it across.
[00:45:22.650 - 00:45:30.910] And you're ready.
[00:45:30.910 - 00:45:34.910] So the quizzes are due Friday each week.
[00:45:34.910 - 00:45:38.910] They start from week six.
[00:45:38.910 - 00:45:44.900] So week six, seven through to ten.
[00:45:44.900 - 00:45:47.900] And they're due Friday, midnight.
[00:45:47.900 - 00:45:51.900] If you don't submit the quizzes then it's automatically...
[00:45:51.900 - 00:45:53.900] There's one attempt.
[00:45:53.900 - 00:45:59.900] So instead of having multiple attempts, I feel like the exercises facilitate that.
[00:45:59.900 - 00:46:03.900] Whereas the quizzes I want you to have confidence in what you write down.
[00:46:03.900 - 00:46:07.900] So that's the reason for the one attempt.
[00:46:07.900 - 00:46:13.900] And I'll go through the solutions on that following Monday of each quiz.
[00:46:13.900 - 00:46:16.900] So that's the general structure for the quizzes.
[00:46:16.900 - 00:46:21.900] I'll talk about more on term four and the exam later on in term four.
[00:46:21.900 - 00:46:28.780] Are there any questions on how the quizzes work?
[00:46:28.780 - 00:46:37.470] So some of the questions will be related to commsaw.
[00:46:37.470 - 00:46:41.470] So if it's starting commsaw next week, I'll start there on the Wednesday.
[00:46:41.470 - 00:46:46.470] I think just so that you finish your test and so start fresh with commsaw on the Wednesday.
[00:46:46.470 - 00:46:52.840] And they'll have similar questions and answer boxes.
[00:46:52.840 - 00:46:55.840] All right.
[00:46:55.840 - 00:47:01.600] I don't know if anyone wants to go through another one of these examples.
[00:47:01.600 - 00:47:04.600] So these equations being elliptic, parabolic, or hyperbolic,
[00:47:04.600 - 00:47:10.940] it's just applying data equation 1.9 again, looking at the term.
[00:47:10.940 - 00:47:12.940] These squared minus 4SC.
[00:47:12.940 - 00:47:22.460] I don't know if question 3 was a total question or not, but essentially this PDE,
[00:47:22.460 - 00:47:36.340] DU by DX equal to 0, what solutions or functions satisfy this equation?
[00:47:36.340 - 00:47:41.340] So any function that is only dependent on Y, for example, would be a solution to this
[00:47:41.340 - 00:47:46.340] because the derivative of Y with respect to X is 0.
[00:47:46.340 - 00:47:53.860] And finding a solution of this PDE and in the wave equation.
[00:47:53.860 - 00:48:01.180] So this is related to that DLE and method that I talked about earlier in the week.
[00:48:01.180 - 00:48:05.290] I don't think anyone's to vote.
[00:48:05.290 - 00:48:08.290] I'm not too motivated to get into the questions for a couple of minutes.
[00:48:08.290 - 00:48:13.290] So if there's no other questions, I'll leave it there.
[00:48:13.290 - 00:48:18.290] So you still have labs this afternoon, but I assume it's preparation for the test.
[00:48:18.290 - 00:48:24.290] Have you been told about what's in the labs or is there things that you want?
[00:48:24.290 - 00:48:27.290] That's probably going to be a hub position then, I think, for the test.
[00:48:27.290 - 00:48:33.290] So is everyone ready for the test or you've got your code?
[00:48:33.290 - 00:48:35.290] Is it up?
[00:48:35.290 - 00:48:36.290] Yeah.
[00:48:36.290 - 00:48:38.290] Cool.
[00:48:38.290 - 00:48:41.290] So next week we'll start with the console labs.
[00:48:41.290 - 00:49:06.340] Good luck for the back-to-click.
[00:49:06.340 - 00:49:25.630] Nice.
[00:49:25.630 - 00:49:30.630] Nice.
[00:49:30.630 - 00:49:32.630] Nice.
[00:49:32.630 - 00:49:33.630] Nice.
[00:49:33.630 - 00:49:34.630] No.
[00:49:34.630 - 00:49:37.630] So pretty much our sessions.
[00:49:37.630 - 00:49:38.630] Yep.
[00:49:38.630 - 00:49:40.630] So you can do the work beforehand.
[00:49:40.630 - 00:49:42.630] And I have sessions for the first time.
[00:49:42.630 - 00:49:48.630] So we sort of have console labs on through five.
[00:49:48.630 - 00:49:51.630] And yeah, we'll start with the quiz as well.
[00:49:51.630 - 00:49:54.630] Awesome.
[00:49:54.630 - 00:49:57.630] Yeah.
[00:49:57.630 - 00:49:58.630] Yeah.
[00:49:58.630 - 00:50:03.630] I guess you could submit the email to ask on the farm for you to cut your free stuff.
[00:50:03.630 - 00:50:06.880] Thank you.
[00:50:06.880 - 00:50:37.540] Nice.
[00:50:37.540 - 00:50:39.540] You're welcome.

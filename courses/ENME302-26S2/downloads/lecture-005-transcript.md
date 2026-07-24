# ENME302-26S2 Lecture 5 fast-pass local ASR transcript

Date: July 20, 2026 12:00pm-12:55pm
Transcript type: Hermes fast-pass local ASR from validated Echo audio, not a native Echo transcript.
Backend/model: faster-whisper tiny.en, CPU int8, beam_size=1, vad_filter=True.
Quality note: fast catch-up transcript. Technical terms, equations, names and Māori words need checking against slides/audio before assessment use.
Source audio SHA-256: `e0acb28f08fa36975515bd5cb0d29f29305d14dc448b186fd4a478547323aaf0`
Generated: 2026-07-24T23:55:30.562166+12:00

[00:00:26.740 - 00:00:27.740] We're going to put the long everyone.
[00:00:27.740 - 00:00:33.660] We'll quickly recap what cover what we're going to work on this week.
[00:00:33.660 - 00:00:35.660] So in the last week we've finished up,
[00:00:35.660 - 00:00:37.660] putting about the principle of digital space,
[00:00:37.660 - 00:00:40.660] and so we're going to do a few different energy methods
[00:00:40.660 - 00:00:43.660] in terms of methods of solving the same problem.
[00:00:43.660 - 00:00:47.660] And hopefully if you just summarize what you learned there,
[00:00:47.660 - 00:00:51.660] we first worked through that as you would have last year in total.
[00:00:51.660 - 00:00:55.660] So we worked out the forces in turning with an edge member.
[00:00:55.660 - 00:00:59.660] We would have the how much those members stretch or contract
[00:00:59.660 - 00:01:01.660] as a result of the loads they carry.
[00:01:01.660 - 00:01:03.660] And then we worked through that kind of awkward,
[00:01:03.660 - 00:01:07.660] quadrilateral shape to work out what the final difficult position of that
[00:01:07.660 - 00:01:09.660] neural point was.
[00:01:09.660 - 00:01:11.660] When we used the working energy method for single loads,
[00:01:11.660 - 00:01:15.660] we saw that we got that answer much more easily without having to do
[00:01:15.660 - 00:01:17.660] their manual intervention, but ahead limitations
[00:01:17.660 - 00:01:22.000] and it couldn't determine the holes until deflection.
[00:01:22.000 - 00:01:26.000] Then we went into and we introduced the concept of virtual displacement.
[00:01:26.000 - 00:01:29.000] Now the purpose of this is not primarily,
[00:01:29.000 - 00:01:32.000] we're not going to do a whole lot of examples using this,
[00:01:32.000 - 00:01:36.000] but the principle of virtual displacement is going to be embedded into our derivation.
[00:01:36.000 - 00:01:39.000] So to give you some context as to what there is,
[00:01:39.000 - 00:01:41.000] written nice in the end of choice, it's very busy.
[00:01:41.000 - 00:01:45.000] And while you have seen the difference before,
[00:01:45.000 - 00:01:50.000] maybe not quite as much detail to cover virtual displacements.
[00:01:50.000 - 00:01:55.950] The key thing here is that we worked through
[00:01:55.950 - 00:02:01.950] and we got the solution here with once we extended the working energy method
[00:02:01.950 - 00:02:05.950] for virtual loads, virtual displacements.
[00:02:05.950 - 00:02:09.950] We were able to determine both the holes onto a vertical deflection,
[00:02:09.950 - 00:02:13.950] and it enables us to determine the deflection at any given point.
[00:02:13.950 - 00:02:16.950] It doesn't just have to be at the point the load is applied,
[00:02:16.950 - 00:02:19.950] and doesn't necessarily have to be in the direction of which the load is applied.
[00:02:19.950 - 00:02:22.950] So it is a more general approach.
[00:02:22.950 - 00:02:25.950] However, you can understand that if we would add an extra membrane here,
[00:02:25.950 - 00:02:29.950] when it's determineers, we could make the structure step in determinants,
[00:02:29.950 - 00:02:32.950] and we would make it a lot much larger structure.
[00:02:32.950 - 00:02:37.950] The problem is by hand would be still pretty difficult to be very very time-consuming.
[00:02:37.950 - 00:02:41.950] So we see a little bit more work to go through
[00:02:41.950 - 00:02:44.950] and be able to assemble larger structures and be able to solve those.
[00:02:44.950 - 00:02:49.950] Put that mathematical framework in place to be able to solve problems like this much more easily.
[00:02:49.950 - 00:02:57.950] So that takes us through to page 27 of the notes.
[00:02:57.950 - 00:03:01.950] And what we're actually going to do here is we're going to derive the same surface matrix we already have.
[00:03:01.950 - 00:03:04.950] We've already got a surface matrix which we determined last week.
[00:03:04.950 - 00:03:14.950] We derived that, but we're going to go through and we're essentially going to derive this in a slightly different way.
[00:03:14.950 - 00:03:18.950] We're now able to same answer, but then we've got two key frameworks that we can use.
[00:03:18.950 - 00:03:24.100] So if you have a quick conduct vector, I'll see what I can do.
[00:03:24.100 - 00:03:27.100] I think that everything is mixed out here.
[00:03:27.100 - 00:03:31.100] I'll move it a little bit closer, so maybe my voice comes through a bit louder.
[00:03:31.100 - 00:03:35.890] Is that better? Thanks for speaking up.
[00:03:35.890 - 00:03:40.890] So what we're going to do is we're going to work through another derivation for the baron surface matrix.
[00:03:40.890 - 00:03:43.890] It's going to give us essentially the same result we had previously,
[00:03:43.890 - 00:03:46.890] but we need to use a different methodology there.
[00:03:46.890 - 00:03:56.890] And I said this to you last week, but it might seem in this early element type that we're going to a very high level of mathematical rigor to derive a relatively simple answer.
[00:03:56.890 - 00:03:58.890] And there are some choices there.
[00:03:58.890 - 00:04:03.890] However, when we go to the more complex element types, which include bin, dang and shear,
[00:04:03.890 - 00:04:12.890] then the derivation will really come into a zone then, and it will enable us to capture some quite complex reaction mechanisms with the same mathematical process.
[00:04:12.890 - 00:04:23.140] So this is a reminder, what we have here is that the rate of change with respect to x of the domestic model of the scarcission area and du by the exit to u by the exit,
[00:04:23.140 - 00:04:30.140] the rate of change of internal displacement within the element with respect to position in the bar, which is always known as strain.
[00:04:30.140 - 00:04:33.140] And we know some bounding values here.
[00:04:33.140 - 00:04:39.140] So once the A times the strain at x equals zero is equal to our individual.
[00:04:39.140 - 00:04:47.140] Our force in term at node one, so that's F1, so that relates back to this force in term here.
[00:04:47.140 - 00:04:52.140] So we have this one, which acts at node one and points in the direction of x.
[00:04:52.140 - 00:04:56.140] We have F2, that's at node two and x in the direction of x.
[00:04:56.140 - 00:04:59.140] So x-round always goes from node one towards node two.
[00:04:59.140 - 00:05:04.140] And that's why those two definitions are defined the way they are.
[00:05:04.140 - 00:05:10.450] So when we've got the right strain at x equals zero, mod by N, A, we get the force in term F1.
[00:05:10.450 - 00:05:17.210] And then we define the value right there at x equals our will get F2.
[00:05:17.210 - 00:05:23.210] Now what we're going to do is mod by both sides of the equation by a small virtual displacement.
[00:05:23.210 - 00:05:27.740] You're going to feed back this.
[00:05:27.740 - 00:05:38.130] Maybe that's filled with that way that seems to be a bit better.
[00:05:38.130 - 00:05:43.130] We're going to mod by both sides of the equation by a little virtual displacement delta U.
[00:05:43.130 - 00:05:50.130] And that's got to be true for all x from x equals zero to x equals L.
[00:05:50.130 - 00:05:55.130] So we're putting this little incremental virtual displacement on both sides of the equation.
[00:05:55.130 - 00:06:00.130] What we're going to do is integrate over the element domain so we're going to integrate all the way from zero to L,
[00:06:00.130 - 00:06:04.130] which is a list of your requirement and equation we previously used.
[00:06:04.130 - 00:06:09.130] So when we pre-seated this derivation is called the strong form where this has to be true at every value of x.
[00:06:09.130 - 00:06:14.130] And then we can also do it on an integral term across the whole element, which is this stringent.
[00:06:14.130 - 00:06:20.130] It's not what's called the weak form, but ultimately it's the, but just the equation is always to be true.
[00:06:20.130 - 00:06:27.820] And it has to be true in an aggregate integrated scenes across the element.
[00:06:27.820 - 00:06:32.820] What we then need to do here is we take that equation and we get integrated by paths.
[00:06:32.820 - 00:06:36.820] And the reason we're integrating it by paths is that we have different orders of integration here.
[00:06:36.820 - 00:06:40.820] So we have the diffuse, the first order,
[00:06:40.820 - 00:06:42.820] and we have a second order derivative there.
[00:06:42.820 - 00:06:48.820] So just what we're doing is we're applying the integration by paths here.
[00:06:48.820 - 00:06:55.820] Now just for your memory, that's the integration by paths,
[00:06:55.820 - 00:07:01.820] you may be more familiar with seeing this in represented as UDV.
[00:07:01.820 - 00:07:06.820] It's equal to UV minus the integral of the DU.
[00:07:06.820 - 00:07:09.820] So that's the form of the equation that you're going to miss in.
[00:07:09.820 - 00:07:13.820] I'm just going to pull mine through that because one of those are correct equation.
[00:07:13.820 - 00:07:19.820] We use U and V as our axial displacement variable and our transverse displacement variable.
[00:07:19.820 - 00:07:23.820] So we're just going to rewrite the integration by paths formula,
[00:07:23.820 - 00:07:25.820] which I'm sure you'll know and love.
[00:07:25.820 - 00:07:28.820] And we're going to rewrite that as g of x times h prime of x dx,
[00:07:28.820 - 00:07:32.820] can be equal to g of x times h of x minus the integral of h of x,
[00:07:32.820 - 00:07:34.820] g prime of x dx.
[00:07:34.820 - 00:07:38.820] So this is kind of color coded for those of you that are using a tablet
[00:07:38.820 - 00:07:41.820] and have the electronic equation of the notes.
[00:07:41.820 - 00:07:44.820] Just reference g of x in this case is our W.
[00:07:44.820 - 00:07:46.820] Just defined here.
[00:07:46.820 - 00:07:50.820] And g prime of x is d by dx of W.
[00:07:50.820 - 00:07:54.820] The derivative of our incremental virtual displacement,
[00:07:54.820 - 00:08:00.820] h of x is ea times h prime of x is ea times the second derivative of a few,
[00:08:00.820 - 00:08:02.820] which is with dx.
[00:08:02.820 - 00:08:06.820] Once we substitute those things in, we get the equation here.
[00:08:06.820 - 00:08:10.820] And then what we can do is we essentially pull our boundary conditions from a bar.
[00:08:10.820 - 00:08:13.820] So we take these two equations here.
[00:08:13.820 - 00:08:17.820] The first thing we're going to do is we're going to evaluate that x equals zero.
[00:08:17.820 - 00:08:20.820] So we have this equation here.
[00:08:20.820 - 00:08:22.820] That is actually defined here.
[00:08:22.820 - 00:08:24.820] So we're going to take this down.
[00:08:24.820 - 00:08:34.800] We're going to bring, and that's actually the negative's out the front here.
[00:08:34.800 - 00:08:37.800] Negative times that is what's defined here.
[00:08:37.800 - 00:08:42.800] So between that negative and the piece in the square here,
[00:08:42.800 - 00:08:44.800] that is equal to f1.
[00:08:44.800 - 00:08:50.340] And then we'll take our other definition, our other boundary condition.
[00:08:50.340 - 00:08:52.340] We're going to bring that down.
[00:08:52.340 - 00:08:55.810] And that's going to form part of the equation there.
[00:08:55.810 - 00:09:00.810] So we just substitute those into our equation that we're going to grade it by parts.
[00:09:00.810 - 00:09:01.810] We're going to plan those boundary conditions.
[00:09:01.810 - 00:09:05.810] That's where if two comes from here, that bracket of term is minus f1,
[00:09:05.810 - 00:09:11.310] then when we simplify that, we get this equation here.
[00:09:11.310 - 00:09:18.620] So we have the derivative of our virtual displacement.
[00:09:18.620 - 00:09:25.620] We have ea times the strain, du by dx, and then the right hand side has substituted in our boundary conditions.
[00:09:25.620 - 00:09:30.620] And we're taking this and we're just taking the two terms here across the other side of the equation side.
[00:09:30.620 - 00:09:38.470] So it's called the weak form because it's the most mature of integrated terms only.
[00:09:38.470 - 00:09:51.010] And that's compared with the strong form, which we'd find previously, which must be true.
[00:09:51.010 - 00:10:09.700] So it's just two different ways of deriving the stiffness matrix.
[00:10:09.700 - 00:10:16.700] And this guy's going to be looking up with often the same answer, but if it gives you some confidence into the robustness of what we're doing.
[00:10:16.700 - 00:10:33.340] And then we'll use this method to define multiple complex reaction mechanisms in the next element type.
[00:10:33.340 - 00:10:37.340] So now we can use a given or not check.
[00:10:37.340 - 00:10:40.720] So we've already defined what these are.
[00:10:40.720 - 00:10:43.720] But I just want to be careful about the difference in here.
[00:10:43.720 - 00:11:12.430] So the uppercase psi, then there's a vector, a vector, or axial,
[00:11:12.430 - 00:11:23.620] modulus, and the actual modulus is quite simple.
[00:11:23.620 - 00:11:25.620] I just x over l and 1 minus x over l.
[00:11:25.620 - 00:11:27.620] This is the definition of the two.
[00:11:27.620 - 00:11:37.100] The functions which interpret internal element actions and relate into the behavior at the node of points.
[00:11:37.100 - 00:11:38.100] We can substitute in here.
[00:11:38.100 - 00:11:42.100] So our u of x is equal to our uppercase psi times our displacement vector d.
[00:11:42.100 - 00:11:45.100] And we can multiply that through like this.
[00:11:45.100 - 00:12:00.100] So that would be essentially a vector like this, which is psi 1 of x and psi 2 of x times a depiction vector, which is d1 and d2.
[00:12:00.100 - 00:12:03.100] That's when we mark one of the major senses.
[00:12:03.100 - 00:12:11.100] psi 1 of x times d1 plus psi 2 of x times d2, which is just this difference in here.
[00:12:11.100 - 00:12:14.100] We can also apply that in an incremental sense.
[00:12:14.100 - 00:12:20.100] What's down for you is the uppercase psi times d over d.
[00:12:20.100 - 00:12:24.100] And lowercase psi 1 times the d1.
[00:12:24.100 - 00:12:27.100] And then we can also apply that in a transpose sense.
[00:12:27.100 - 00:12:31.100] So we're just transposing this into the transpose of the vectors.
[00:12:31.100 - 00:12:33.100] And it could just transform here.
[00:12:33.100 - 00:12:38.100] So these shape functions are the same as what we've seen previously.
[00:12:38.100 - 00:12:45.100] And our pre-to-term and pre-find or interpolated shape functions are relating to an element action to the value of the node of points.
[00:12:45.100 - 00:12:51.100] And that's what enables us to just solve it a few discrete positions that have those values.
[00:12:51.100 - 00:12:55.100] Those discrete values be represented by the continuous solid.
[00:12:55.100 - 00:13:00.860] So equation 18 becomes this big beast here.
[00:13:00.860 - 00:13:02.860] Now we can simplify that.
[00:13:02.860 - 00:13:05.860] We've got this big long vector of stuff.
[00:13:05.860 - 00:13:09.860] But there's some things that we can take out in cancel out of there.
[00:13:09.860 - 00:13:12.860] So let's take out our delta dt.
[00:13:12.860 - 00:13:15.860] That's a common factor to all three of those things.
[00:13:15.860 - 00:13:21.650] So that gives us this piece.
[00:13:21.650 - 00:13:27.940] And it's just our forcing vector here.
[00:13:27.940 - 00:13:31.940] So once we've made this substitution, we have this equation here.
[00:13:31.940 - 00:13:37.940] And what I want you to do here is before we go too much further, I just want to take a skip back.
[00:13:37.940 - 00:13:43.930] And let's look at the form of this equation.
[00:13:43.930 - 00:13:52.620] We've gone through a bunch of math, we've done some substitution,
[00:13:52.620 - 00:13:55.620] we've grouped some light terms, we've done some cancellation,
[00:13:55.620 - 00:13:57.620] and we've ended up this equation.
[00:13:57.620 - 00:14:03.620] So essentially what I want you to see here is you've got a bracketed term with a bunch of stuff in it.
[00:14:03.620 - 00:14:07.620] Times of deflection as equal to a force.
[00:14:07.620 - 00:14:12.700] Hopefully, if you look at that equation here, I know what that is.
[00:14:12.700 - 00:14:14.700] I've seen that type of equation before.
[00:14:14.700 - 00:14:24.860] So what that is is all of that stuff in the brackets.
[00:14:24.860 - 00:14:35.110] We know that I'll fix the equation.
[00:14:35.110 - 00:14:39.110] We know that stiffness times the space point is equal to force.
[00:14:39.110 - 00:14:41.110] That's essentially what this equation is saying.
[00:14:41.110 - 00:14:45.110] It's just now the definition of stiffness is a bit more complicated.
[00:14:45.110 - 00:14:49.110] So we're relating that via to this equation.
[00:14:49.110 - 00:14:55.420] And then this is our element stiffness matrix.
[00:14:55.420 - 00:14:57.420] Can you hear me a couple of back?
[00:14:57.420 - 00:15:00.080] Looking at that?
[00:15:00.080 - 00:15:02.080] The sound in here is not all it could be.
[00:15:02.080 - 00:15:09.080] Now, this bracket does set of equations with a box around it.
[00:15:09.080 - 00:15:12.080] And it's quite significant in terms of where we're going this course.
[00:15:12.080 - 00:15:22.420] So the key thing here is that the equations provide a definition,
[00:15:22.420 - 00:16:01.890] the relationship between a glides to definition of stiffness,
[00:16:01.890 - 00:16:03.890] our chosen shape functions.
[00:16:03.890 - 00:16:24.960] I think it's about as sharp as we can get it.
[00:16:24.960 - 00:16:28.620] So when we define that shape functions,
[00:16:28.620 - 00:16:32.620] we look at it and we basically work out the internal reaction mechanisms,
[00:16:32.620 - 00:16:34.620] how that would relate to the total of functions,
[00:16:34.620 - 00:16:36.620] and we made some assumptions.
[00:16:36.620 - 00:16:38.620] And when we define these equations,
[00:16:38.620 - 00:16:41.620] they did put some limitations on the type of reactions
[00:16:41.620 - 00:16:47.620] and the type of deformation mechanics that we're able to model with this element type.
[00:16:47.620 - 00:16:50.620] And that also then goes through and defines that stiffness matrix.
[00:16:50.620 - 00:16:52.620] So they're all wrapped up together.
[00:16:52.620 - 00:16:57.220] Now we can multiply that through.
[00:16:57.220 - 00:17:01.220] So we have the derivative with respect to x of actually a function.
[00:17:01.220 - 00:17:04.220] So the first one is one my 6 o'erl.
[00:17:04.220 - 00:17:07.220] And when you do a fringe out that with respect to x,
[00:17:07.220 - 00:17:09.220] you just get one over l.
[00:17:09.220 - 00:17:11.220] And then the second one with just x over l,
[00:17:11.220 - 00:17:12.220] and we need different shape that with respect to x,
[00:17:12.220 - 00:17:13.220] you just get one over l.
[00:17:13.220 - 00:17:15.220] So that's where those have come from.
[00:17:15.220 - 00:17:17.220] There's the transpose of it there.
[00:17:17.220 - 00:17:20.220] And then the non transpose version there,
[00:17:20.220 - 00:17:23.220] and we're more of a classroom, we get this definition here.
[00:17:23.220 - 00:17:27.630] So ultimately what we know here is this stiffness matrix.
[00:17:27.630 - 00:17:32.630] And this is the exact same thing that we derived through the other method.
[00:17:32.630 - 00:17:37.630] So of this, of this reassuring that the two of them is of given the same result.
[00:17:37.630 - 00:17:45.720] It's just as before,
[00:17:45.720 - 00:17:47.720] but this derivation makes kE easy.
[00:17:47.720 - 00:17:49.720] So the definition that stiffness matrix is easy
[00:17:49.720 - 00:17:53.720] to calculate given the shape functions to relate or interpret
[00:17:53.720 - 00:17:58.720] motion along the element from one end into a total displacement values.
[00:17:58.720 - 00:18:01.720] So while this gives us a simple result,
[00:18:01.720 - 00:18:04.720] we would have a result of may not seem like something new.
[00:18:04.720 - 00:18:07.720] The framework we've developed is going to be really powerful in the next week
[00:18:07.720 - 00:18:09.720] when we go to more complex element types.
[00:18:09.720 - 00:18:16.140] So if you points to recap on this,
[00:18:16.140 - 00:18:20.900] this is our definition.
[00:18:20.900 - 00:18:22.900] It's a one-dimensional element, node one,
[00:18:22.900 - 00:18:25.900] and node two, x always goes from node one towards node two,
[00:18:25.900 - 00:18:28.900] and we have our forcing and displacement terms that he jeaned
[00:18:28.900 - 00:18:31.900] always aligned with x for the element.
[00:18:31.900 - 00:18:36.900] We've seen a definition for our stiffness equation,
[00:18:36.900 - 00:18:39.900] and this is at an individual element level.
[00:18:39.900 - 00:18:42.900] We have a vector of forces, our vector of defections,
[00:18:42.900 - 00:18:46.900] and then we have a stiffness matrix which defines the relationship between those.
[00:18:46.900 - 00:18:52.730] So we can basically put all this together,
[00:18:52.730 - 00:18:55.730] and we can write that into a matrix equation,
[00:18:55.730 - 00:18:59.730] which is that if one for a given element,
[00:18:59.730 - 00:19:01.730] and if two for a given element,
[00:19:01.730 - 00:19:08.300] has equal to EA over L,
[00:19:08.300 - 00:19:11.300] one negative one, negative one,
[00:19:11.300 - 00:19:15.300] one times the defection, which is D1 for the element,
[00:19:15.300 - 00:19:17.300] and D2 for the element.
[00:19:17.300 - 00:19:21.300] So that's just everything piece together into a matrix equation.
[00:19:21.300 - 00:19:26.960] The element stiffness k is a function of EA and L,
[00:19:26.960 - 00:19:28.960] and the given shape functions.
[00:19:28.960 - 00:19:30.960] So those shape functions are really important,
[00:19:30.960 - 00:19:32.960] they are the things that we've decided.
[00:19:32.960 - 00:19:35.960] We want to capture as reaction mechanisms,
[00:19:35.960 - 00:19:36.960] we embed them into a derivation,
[00:19:36.960 - 00:19:42.960] and also they use to break down and interpret results once we've solved the matrix system of equations.
[00:19:42.960 - 00:19:45.960] The actual forces so far, we're assuming those to be zero,
[00:19:45.960 - 00:19:47.960] so we're assuming there is no,
[00:19:47.960 - 00:19:50.960] the absence of any distributed axial load,
[00:19:50.960 - 00:19:54.960] and that there's a constant normal force all along the way along the bar.
[00:19:54.960 - 00:19:57.960] It captures only axial deformation,
[00:19:57.960 - 00:19:59.960] and force displacement behavior.
[00:19:59.960 - 00:20:01.960] At this point, this top element does not pair any moments,
[00:20:01.960 - 00:20:04.960] and it has no rotations.
[00:20:04.960 - 00:20:08.960] We'll get there, we will add that in, but we just not the,
[00:20:08.960 - 00:20:11.960] the stiffness matrix is based on the shape functions,
[00:20:11.960 - 00:20:16.960] the bar element deformation can be defined through this nice handy equation,
[00:20:16.960 - 00:20:18.960] and the coordinate system,
[00:20:18.960 - 00:20:20.960] as always aligned with the x-long element,
[00:20:20.960 - 00:20:23.960] and y transverse to that.
[00:20:23.960 - 00:20:33.230] Now, one thing we know is the dissipation,
[00:20:33.230 - 00:20:37.230] as we've thought, we now have this matrix in a equation,
[00:20:37.230 - 00:20:39.230] because two unknowns, there's two equations,
[00:20:39.230 - 00:20:41.230] they might seem like we can solve that,
[00:20:41.230 - 00:20:43.230] but they're not independent equations.
[00:20:43.230 - 00:20:46.230] So at the moment, this element is just floating in space,
[00:20:46.230 - 00:20:49.230] we haven't yet introduced the information which ties it into a support point,
[00:20:49.230 - 00:20:51.230] or makes it into a large structure.
[00:20:51.230 - 00:20:55.760] That's to become.
[00:20:55.760 - 00:21:00.760] So bars and the beam elements and frame elements that are coming are 1D elements,
[00:21:00.760 - 00:21:03.760] so the shape functions are only along the dimension.
[00:21:03.760 - 00:21:06.760] So the cipher is that we've defined or any function of x,
[00:21:06.760 - 00:21:08.760] but if we had a plate, for example,
[00:21:08.760 - 00:21:10.760] so suppose this might be a plate,
[00:21:10.760 - 00:21:17.390] so we can, if we had a diaphragm action at a plate,
[00:21:17.390 - 00:21:21.770] we may have some sort of two-dimensional element like this.
[00:21:21.770 - 00:21:27.610] Now, this we're looking at, and we might have,
[00:21:27.610 - 00:21:31.610] say four elements there, so we might be calling this element 1,
[00:21:31.610 - 00:21:35.950] this element 2, 3,
[00:21:35.950 - 00:21:38.950] so node nodes 1, 2, 3, and 4,
[00:21:38.950 - 00:21:43.950] and then we want, if we want to determine the defection of x and y defection,
[00:21:43.950 - 00:21:47.950] of some point internally within that plate,
[00:21:47.950 - 00:21:51.950] we would have to interpret, and interpolate in both the x and y directions.
[00:21:51.950 - 00:21:55.950] So in the x direction, the closer we are to nodes 3, 2 and 3,
[00:21:55.950 - 00:21:58.950] the more influence we would draw from them, and the less from 1 and 4,
[00:21:58.950 - 00:22:01.950] and then vertically, to further up the element are,
[00:22:01.950 - 00:22:06.950] the more influence we would draw from nodes 1 and 2, and less from nodes 3 and 4.
[00:22:06.950 - 00:22:28.630] So in a 2D plane, have to interpolate in both
[00:22:28.630 - 00:22:37.830] x, and that just does mean it's actually drawing the larger influence from the nodes you're closest to.
[00:22:37.830 - 00:22:41.830] Now, whether it's a linear interpolation, and it's just a linear progression,
[00:22:41.830 - 00:22:48.830] or whether you perhaps have a parabolic or a cubic relationship between how close
[00:22:48.830 - 00:22:51.830] how much influence you draw to the closest node,
[00:22:51.830 - 00:22:55.830] that comes down to what you expect the internal reaction because there's some stability.
[00:22:55.830 - 00:23:02.160] If we were to extend this into a 3D element,
[00:23:02.160 - 00:23:07.160] so we've got, say, an x here, a y here, and a z out this way,
[00:23:07.160 - 00:23:11.160] then we would actually have an element that looks like this.
[00:23:11.160 - 00:23:17.740] So if we're defining a rectangular element,
[00:23:17.740 - 00:23:22.740] we're going to have a minimum of 8 nodes, and we have 6 spaces.
[00:23:22.740 - 00:23:28.740] And if we wanted to determine the point internally within there,
[00:23:28.740 - 00:23:32.740] what the internal behavior of an element somewhere in the internal way,
[00:23:32.740 - 00:23:38.740] we would then have to interpolate between x, y, and z.
[00:23:38.740 - 00:23:40.740] And it would be the same thing.
[00:23:40.740 - 00:23:44.740] In the Extirection, we would draw the most influence from the nodes to the closest to it,
[00:23:44.740 - 00:23:47.740] in the Extirection, and the least influence from the nodes to the further away,
[00:23:47.740 - 00:23:50.740] and the same thing in the y and z directions.
[00:23:50.740 - 00:23:52.740] So the keeping improvement from this here,
[00:23:52.740 - 00:23:58.740] then trying to convey here is that we're dealing with a relatively simple one-dimensional element.
[00:23:58.740 - 00:24:03.740] If you're looking at this and go, well, this isn't what I envisaged, for an element to be,
[00:24:03.740 - 00:24:06.740] this is probably more what you might initially think of,
[00:24:06.740 - 00:24:08.740] we talk about a finite element analysis.
[00:24:08.740 - 00:24:11.740] It's the same thing just a plot and multiple dimensions.
[00:24:11.740 - 00:24:17.740] It's all the same principles hold, and more we're learning here does relate to a more complex 3D element time.
[00:24:17.740 - 00:24:23.500] It's also for a region, so given a governing ODA, and boundary conditions,
[00:24:23.500 - 00:24:28.500] we can define check functions and set up a system like this,
[00:24:28.500 - 00:24:35.500] and now we may approach from a way to understand most finite elements you might encounter in a software package in the future.
[00:24:35.500 - 00:24:43.340] One thing I will also reinforce is that our governing ODA,
[00:24:43.340 - 00:24:46.340] when we set this up, was for small deflections.
[00:24:46.340 - 00:24:51.340] So our KEMatrix is also valid for small deflections.
[00:24:51.340 - 00:24:58.440] And when we started working through that problem,
[00:24:58.440 - 00:25:04.580] what I said here was that we went through this problem,
[00:25:04.580 - 00:25:11.580] that there was sort of two arcs here, and the true position would be the intersection of those two arcs.
[00:25:11.580 - 00:25:14.580] But when we do our manual and investigation here,
[00:25:14.580 - 00:25:17.580] we actually determined that linearized it could be one to the first.
[00:25:17.580 - 00:25:21.960] Now, we went through some processes into this by hand,
[00:25:21.960 - 00:25:24.960] but even when we jump into the finite element system,
[00:25:24.960 - 00:25:28.960] and we solve, we'll get this not too much more simply,
[00:25:28.960 - 00:25:32.960] but it will still be the linearized vision.
[00:25:32.960 - 00:25:35.960] We're not actually going to be solving for the true intersection point,
[00:25:35.960 - 00:25:38.960] we're still going to be finite on the linearized version,
[00:25:38.960 - 00:25:42.960] and that small deflection assumption is implicit to this method.
[00:25:42.960 - 00:25:46.960] So it's sometimes called the computational cardinalson,
[00:25:46.960 - 00:25:50.960] where you go in and you use two different independent mathematical methods,
[00:25:50.960 - 00:25:54.960] with the same underlying assumptions and go, hey look, they agree with each other, isn't it great?
[00:25:54.960 - 00:25:55.960] Everything's fine.
[00:25:55.960 - 00:25:57.960] But actually if your assumption is wrong,
[00:25:57.960 - 00:25:59.960] their error is common to both.
[00:25:59.960 - 00:26:05.960] So there is that assumption that we are using small deflections,
[00:26:05.960 - 00:26:07.960] that this sort of pulse weird terms,
[00:26:07.960 - 00:26:10.960] and the second order terms are negligible.
[00:26:10.960 - 00:26:18.960] It also assumes that the initial geometry is a fair approximation of the deflected geometry.
[00:26:18.960 - 00:26:20.960] So our stiffness matrix,
[00:26:20.960 - 00:26:24.960] the way that we relate applied loads to cross-running deflections
[00:26:24.960 - 00:26:27.960] is based upon the initial geometry.
[00:26:27.960 - 00:26:30.960] It's a sense of deficking a very large way,
[00:26:30.960 - 00:26:34.960] and the deflected geometry doesn't look like the initial geometry.
[00:26:34.960 - 00:26:37.960] Then the calculations are being done on a stiffness matrix,
[00:26:37.960 - 00:26:40.960] which isn't represented of that deflected shape.
[00:26:40.960 - 00:26:44.960] So that's the key thing that we need to understand.
[00:26:44.960 - 00:26:52.900] So say for example, we have a cantilever being like this.
[00:26:52.900 - 00:26:55.900] We're not quite at the start of element just yet.
[00:26:55.900 - 00:26:59.900] But if we did, we had some sort of load P on here,
[00:26:59.900 - 00:27:02.900] and then we drew some sort of defected shapes.
[00:27:02.900 - 00:27:05.900] We start out flat because of the fact that it's a fixed support,
[00:27:05.900 - 00:27:07.900] and then over the link of the element,
[00:27:07.900 - 00:27:11.900] we sort of, we go through and this thing kind of sat down here.
[00:27:11.900 - 00:27:14.900] Like this.
[00:27:14.900 - 00:27:18.900] I mean, if this is a rather fixed-forward defection here,
[00:27:18.900 - 00:27:22.900] it may be that's not a drawn-out or exaggerated.
[00:27:22.900 - 00:27:28.900] Then initial and final deflections may not be that different.
[00:27:28.900 - 00:27:32.900] But if we had something where this was, say, some sort of
[00:27:32.900 - 00:27:34.900] superlactic material, or it was made of rubber,
[00:27:34.900 - 00:27:42.340] and it was sagging significantly as a result of the load that's been applied,
[00:27:42.340 - 00:27:48.810] it may come down like this, and then now the load is hanging off the end of it.
[00:27:48.810 - 00:27:53.810] What was a transverse load has now actually become towards the much more of an axial load,
[00:27:53.810 - 00:27:56.810] and you've got this different loading pattern.
[00:27:56.810 - 00:27:59.810] So the loads that we're applied to initial geometry are now longer,
[00:27:59.810 - 00:28:04.310] and no longer represented, fixed shape.
[00:28:04.310 - 00:28:08.310] So the question is, how would you deal with that?
[00:28:08.310 - 00:28:12.310] There may be situations in engineering where you want to model that type of thing.
[00:28:12.310 - 00:28:16.690] Well, what you would do is you would, you would do an iterative process.
[00:28:16.690 - 00:28:20.690] So the first thing you do is you're a symbol based upon your initial geometry.
[00:28:20.690 - 00:28:24.690] You do a solution and you add a defected shape.
[00:28:24.690 - 00:28:28.690] You'd use those self-modal reflections, you'd get new neural deflections,
[00:28:28.690 - 00:28:33.690] and then you'd re-build your stiffness matrix based upon that defected shape.
[00:28:33.690 - 00:28:38.690] And you'd iterate on that process until you get a converged solution.
[00:28:38.690 - 00:28:44.690] So then because you're iterating and you're re-building your stiffness matrix based upon the defected geometry,
[00:28:44.690 - 00:28:49.690] then you would get to a point where you are modeling large deflections
[00:28:49.690 - 00:28:54.690] and those deflections are being calculated based upon stiffness matrix,
[00:28:54.690 - 00:28:57.690] which represents that defected geometry.
[00:28:57.690 - 00:29:01.690] Now it's a bit of a process to program,
[00:29:01.690 - 00:29:06.690] but if you are using a commercial package and you see this large defection analysis option,
[00:29:06.690 - 00:29:09.690] that's what's actually going on in the same line, the same steer.
[00:29:09.690 - 00:29:13.690] It's iterating on that and it's rebuilding and updating the stiffness matrix
[00:29:13.690 - 00:29:24.050] based upon the defected shape of the structure.
[00:29:24.050 - 00:29:26.050] So the moment we have one element,
[00:29:26.050 - 00:29:29.050] it's sitting there by itself and at the moment it's just floating in space.
[00:29:29.050 - 00:29:34.050] We haven't necessarily linked it into some specific location of the structure.
[00:29:34.050 - 00:29:37.050] So how do we take one element?
[00:29:37.050 - 00:29:40.050] How do we combine it together to do a model of something real?
[00:29:40.050 - 00:29:46.050] What if the barrel element axes, the different elements are on different orientations
[00:29:46.050 - 00:29:50.050] and their coordinate systems don't align?
[00:29:50.050 - 00:29:58.050] Well we need to go to a seemingly element stiffness matrices into a full model.
[00:29:58.050 - 00:30:01.050] Now the first thing I want to do before we jump into that is just really,
[00:30:01.050 - 00:30:04.050] hopefully, pretty clearly defines the terminology.
[00:30:04.050 - 00:30:07.050] So we have element level degrees of freedom.
[00:30:07.050 - 00:30:10.050] So these are the amount by which no each node moves,
[00:30:10.050 - 00:30:14.050] energy in the direction of the element.
[00:30:14.050 - 00:30:16.050] But then we've also got the structural level,
[00:30:16.050 - 00:30:19.050] when you've got multiple elements when the structural level degrees of freedom.
[00:30:19.050 - 00:30:24.300] Any position there's the potential for a non-zero displacement to occur
[00:30:24.300 - 00:30:25.300] and a nodal point.
[00:30:25.300 - 00:30:28.300] We're going to assign a degree of freedom at that location.
[00:30:28.300 - 00:30:31.300] So F is a fixed support, so if someone's penned
[00:30:31.300 - 00:30:33.300] and there's no absolute certainty,
[00:30:33.300 - 00:30:37.300] there is no potential for any non-zero displacement to occur there,
[00:30:37.300 - 00:30:39.300] then you don't put a degree for you.
[00:30:39.300 - 00:30:43.300] But if you have a support point where there is the potential for a non-zero
[00:30:43.300 - 00:30:47.300] displacement to occur, then we need to put a degree for you in there.
[00:30:47.300 - 00:30:53.300] It's also important to realize that the structural stiffness matrix is derived
[00:30:53.300 - 00:30:56.300] independent of the load that are applied.
[00:30:56.300 - 00:30:58.300] So you can look at the structure goal and this particular case
[00:30:58.300 - 00:31:02.300] I know that it's not going to move there, so I'm not going to put a degree of freedom.
[00:31:02.300 - 00:31:07.300] Well, the thing is that you're not building the structure for that specific loading case.
[00:31:07.300 - 00:31:12.300] You've been in the structure as a whole, but then afterwards you introduce the particular load in this
[00:31:12.300 - 00:31:16.610] introduced that's going to apply to the structure.
[00:31:16.610 - 00:31:18.610] So our lower case gives a similar degree of freedom.
[00:31:18.610 - 00:31:22.610] The point with the structure with is the potential for a non-zero displacement.
[00:31:22.610 - 00:31:26.610] And then our upper case cue is the applied load.
[00:31:26.610 - 00:31:30.610] The applied external load that exists at the location.
[00:31:30.610 - 00:31:32.610] So they're always coupled.
[00:31:32.610 - 00:31:36.610] And given no, any given direction, there might be a lower case cue and an upper case cue
[00:31:36.610 - 00:31:37.610] three.
[00:31:37.610 - 00:31:39.610] A lower case cue three and an upper case cue three.
[00:31:39.610 - 00:31:44.610] They're the same location in the same direction for, say, the same number.
[00:31:44.610 - 00:31:50.610] These, they don't, you know, two ones, a lower case cue one's over here and upper case cue two's over here.
[00:31:50.610 - 00:31:52.610] They're always together as a matched pair.
[00:31:52.610 - 00:31:57.950] So they will be compared once we start with improved problems.
[00:31:57.950 - 00:32:12.800] And before we jump into that, is there any questions?
[00:32:12.800 - 00:32:13.800] Which across to this?
[00:32:13.800 - 00:32:33.860] So we're going to start out looking at a system.
[00:32:33.860 - 00:32:37.860] Now, just to reinforce what I was just saying, here there's a no point.
[00:32:37.860 - 00:32:39.860] It's a pen joint.
[00:32:39.860 - 00:32:41.860] It's completely constrained.
[00:32:41.860 - 00:32:43.860] There's no possibility if the depiction's there or there.
[00:32:43.860 - 00:32:49.860] So there's no global degrees of freedom assigned at either location.
[00:32:49.860 - 00:32:51.860] And we're going to add this point.
[00:32:51.860 - 00:32:54.860] There could be motion horizontally or vertically.
[00:32:54.860 - 00:32:56.860] So we're going to apply a cue one.
[00:32:56.860 - 00:32:58.860] No case cue one and an upper case cue one.
[00:32:58.860 - 00:33:03.860] So it's the amount of which this affects in the corresponding applied load and in the same thing vertically.
[00:33:03.860 - 00:33:06.860] So for the structure, there's two global degrees of freedom.
[00:33:06.860 - 00:33:11.420] What we're going to do is break that up.
[00:33:11.420 - 00:33:13.420] So element one.
[00:33:13.420 - 00:33:15.420] We have some element coordinates here.
[00:33:15.420 - 00:33:18.420] Remembering x always goes along the element length.
[00:33:18.420 - 00:33:23.420] We have an element coordinate system here and a global coordinate system here.
[00:33:23.420 - 00:33:24.420] And these two align.
[00:33:24.420 - 00:33:25.420] So that's nice and easy.
[00:33:25.420 - 00:33:27.420] However, this element's vertical.
[00:33:27.420 - 00:33:30.420] x always runs along the length of the element.
[00:33:30.420 - 00:33:34.670] So if we start to look at that,
[00:33:34.670 - 00:33:35.670] there's some that's aligned.
[00:33:35.670 - 00:33:38.950] Those two match each other.
[00:33:38.950 - 00:33:40.950] That's nice and easy.
[00:33:40.950 - 00:33:50.730] Then when we look at this one, those two coordinate systems don't match.
[00:33:50.730 - 00:33:53.730] So everything is revolving in the chaos.
[00:33:53.730 - 00:34:03.290] And we need to some sort of other method here.
[00:34:03.290 - 00:34:09.290] So I might just quickly make a note there just to make sure that you're sort of confident with that.
[00:34:09.290 - 00:34:35.150] This nodal point fully constrained translate.
[00:34:35.150 - 00:34:58.260] So no degree of freedom cases.
[00:34:58.260 - 00:35:16.950] It's here four non-zero displacements in xg and yg.
[00:35:16.950 - 00:35:27.140] Good degrees of freedom here.
[00:35:27.140 - 00:35:29.140] And I might feel like I'm layering this point a little bit.
[00:35:29.140 - 00:35:30.140] And perhaps I am.
[00:35:30.140 - 00:35:31.140] But there's a reason for that.
[00:35:31.140 - 00:35:36.140] And so this is the very initial decision that you have to make to see a proper problem.
[00:35:36.140 - 00:35:41.140] If you get this wrong at this point, no amount of further analysis down the track has been a fixed there.
[00:35:41.140 - 00:35:43.140] So you need to be confident to make that.
[00:35:43.140 - 00:35:47.140] And when it comes to the test, you will be expected to make that decision yourself.
[00:35:47.140 - 00:35:50.140] You wouldn't be given the structure with these already labeled.
[00:35:50.140 - 00:35:51.140] You'd be given the structure without those.
[00:35:51.140 - 00:35:54.140] And you'd have to make that decision yourself.
[00:35:54.140 - 00:35:57.140] So you need to be confident in doing that.
[00:35:57.140 - 00:36:07.020] So we have just a quickly recap.
[00:36:07.020 - 00:36:09.020] We have this element sort of line here.
[00:36:09.020 - 00:36:14.020] So you can sort of, you can translate things from the school assistant to this one.
[00:36:14.020 - 00:36:15.020] It's nice and easily.
[00:36:15.020 - 00:36:18.020] But this one here is much more complicated.
[00:36:18.020 - 00:36:21.020] You've got this element that's going to flip 90 degrees.
[00:36:21.020 - 00:36:25.020] x doesn't match with x and y doesn't match with y.
[00:36:25.020 - 00:36:29.020] But if you look at this, it is ultimately just a rotator.
[00:36:29.020 - 00:36:34.020] So we could rotate through minus 90 degrees or plus 270 degrees.
[00:36:34.020 - 00:36:37.020] And then this element would align with this.
[00:36:37.020 - 00:36:44.020] So hopefully you can see where we go with this and seeing that this will all make sense.
[00:36:44.020 - 00:36:46.020] These are the transformation process.
[00:36:46.020 - 00:36:57.620] So what we're going to do, F the element is a some generic inclination angle alpha.
[00:36:57.620 - 00:36:59.620] So this is sort of a nice general case.
[00:36:59.620 - 00:37:03.620] where it's some, you know, 40 degrees or something.
[00:37:03.620 - 00:37:07.620] And these are aligned so that the local degrees are freedom.
[00:37:07.620 - 00:37:12.620] The lower case here from the lower case D are always, they always align with the element.
[00:37:12.620 - 00:37:14.620] So the elements are pretty degrees.
[00:37:14.620 - 00:37:16.620] They're also 40 degrees.
[00:37:16.620 - 00:37:20.620] The global coordinate systems are the upper case here from the upper case D.
[00:37:20.620 - 00:37:22.620] And they always align with that global coordinate.
[00:37:22.620 - 00:37:26.250] So our xg and myg.
[00:37:26.250 - 00:37:30.250] Now what we need to work out here is first of all,
[00:37:30.250 - 00:37:34.250] just really be sure about some some number of interventions.
[00:37:34.250 - 00:38:14.150] So D1 can if one always direction ways align with x the x coordinate for the element.
[00:38:14.150 - 00:38:16.150] So it's no case x.
[00:38:16.150 - 00:38:36.360] So this is the element.
[00:38:36.360 - 00:38:48.930] Now we covered this last week, but just to reinforce.
[00:38:48.930 - 00:38:50.930] It's always counterclockwise positive.
[00:38:50.930 - 00:38:53.930] So we start aligned with that x global coordinate to find just here.
[00:38:53.930 - 00:38:58.930] And then we rotate counterclockwise until we're aligned with x for the elements.
[00:38:58.930 - 00:39:00.930] In this case we start horizontally.
[00:39:00.930 - 00:39:02.930] We rotate counterclockwise until we get to here.
[00:39:02.930 - 00:39:05.930] Then we're aligned with xe and this elements.
[00:39:05.930 - 00:39:07.930] Yeah.
[00:39:07.930 - 00:39:09.930] 35 40 degrees in the right way.
[00:39:09.930 - 00:39:20.120] For the once we break this up into individual defection components.
[00:39:20.120 - 00:39:24.120] So we just basically breaking this up the same way you always would have with forces.
[00:39:24.120 - 00:39:30.120] So suppose we've got some sort of, this could be D1 here.
[00:39:30.120 - 00:39:36.120] What we want to do is break that up into a DX and Y components.
[00:39:36.120 - 00:39:40.120] So here we have our uppercase D1.
[00:39:40.120 - 00:39:46.370] And here we'd have our uppercase D2.
[00:39:46.370 - 00:40:01.910] Our uppercase D1 and uppercase D2 must add together in a vector sense,
[00:40:01.910 - 00:40:14.770] the equal D1.
[00:40:14.770 - 00:40:21.290] So this diagram is actually applied here and node 1.
[00:40:21.290 - 00:40:24.290] And it relates lowercase D1 to uppercase D1 and D2.
[00:40:24.290 - 00:40:27.290] But we could draw an identical diagram that sits over here.
[00:40:27.290 - 00:40:32.290] And there will relate lowercase D2 to uppercase D3 and uppercase D4.
[00:40:32.290 - 00:40:41.500] So the number x sequence here is that D1 is in the xg direction.
[00:40:41.500 - 00:41:03.630] At node 1 is yg. At node 1, D3 is xg2.
[00:41:03.630 - 00:41:17.140] That's our yg. But essentially just go on xy, node 1, xy, node 2.
[00:41:17.140 - 00:41:20.140] And that's the sequence that we follow.
[00:41:20.140 - 00:41:23.140] Seems like a logic one to me.
[00:41:23.140 - 00:41:25.140] We kind of chosen something different.
[00:41:25.140 - 00:41:26.140] But that's what we've chosen.
[00:41:26.140 - 00:41:28.140] That's what we've chosen. That's what we need to stick with.
[00:41:28.140 - 00:41:32.140] Because the entries into our matrices will be based upon this number of sequence.
[00:41:32.140 - 00:41:38.870] We want to use them. We have to be consistent with our convention.
[00:41:38.870 - 00:41:41.870] Now hopefully this becomes a big surprise to you.
[00:41:41.870 - 00:41:44.870] That transformation is going to evolve cos and sine.
[00:41:44.870 - 00:41:46.870] It's the same thing you've done.
[00:41:46.870 - 00:41:51.870] And the unit classes where you resolve forces into the xe on a cheer component.
[00:41:51.870 - 00:41:55.870] And you go through that. It's the exact same idea.
[00:41:55.870 - 00:41:59.870] So we've got our cosine alpha in our sine alpha.
[00:41:59.870 - 00:42:05.950] And what we need to do is just define our relationship between them.
[00:42:05.950 - 00:42:08.950] So basically, on the diagram above,
[00:42:08.950 - 00:42:13.950] the D1 is equal to D1.
[00:42:13.950 - 00:42:15.950] So the lower case D1 is up to D1.
[00:42:15.950 - 00:42:18.950] It could up a case D1 cos alpha and up a case D2 sine alpha.
[00:42:18.950 - 00:42:23.950] And we can just use this commandial hat with the c and s being shown here because of sine.
[00:42:23.950 - 00:42:30.250] And a matrix form, this is what it looks like here.
[00:42:30.250 - 00:42:36.910] So I think that everything here, this here is called our transformation matrix.
[00:42:36.910 - 00:42:58.740] Forms local, which is l1 and global.
[00:42:58.740 - 00:43:24.540] To be aware of here, this variable here is actually called an upper case lambda.
[00:43:24.540 - 00:43:30.080] It might look like in a capital way, but it's actually an upper case lambda.
[00:43:30.080 - 00:43:37.080] So that's what the really common convention for transformation matrix is
[00:43:37.080 - 00:43:41.080] in the literature. So most textbooks will use that same definition.
[00:43:41.080 - 00:43:50.360] So that's that here. That's the transformation matrix.
[00:43:50.360 - 00:44:00.360] And we can basically summarize everything here. So we've got lower case D is equal to our transformation matrix times our upper case D.
[00:44:00.360 - 00:44:09.360] So remember that when you're dealing with matrices, the matrix multiplication, the internal dimensions have to be conformable.
[00:44:09.360 - 00:44:15.360] So that has four columns that says to have four rows.
[00:44:15.360 - 00:44:22.360] We can usually use it in a transverse form to go from the lower case if to the upper case if.
[00:44:22.360 - 00:44:25.360] And then this is to remind her of what the definition is about.
[00:44:25.360 - 00:44:36.670] So let's have a quick look at the more detail.
[00:44:36.670 - 00:44:44.700] What about the difference matrix K.
[00:44:44.700 - 00:44:51.710] So if we want to if we want to operate in global coordinates.
[00:44:51.710 - 00:44:53.710] Then this diagram we have two degrees of freedom.
[00:44:53.710 - 00:44:56.710] One at each end of the member and the direction of the member.
[00:44:56.710 - 00:45:02.710] But here when we break it up into its components, we actually now have four components of the fiction.
[00:45:02.710 - 00:45:08.710] So if we want to do apply the stiffness equation based upon
[00:45:08.710 - 00:45:14.710] depictions which are broken up with the x and y components and forcing terms which are broken up into the x and y components.
[00:45:14.710 - 00:45:23.710] We need now to have a stiffness matrix which has a 4 by 4 because it needs to manipulate four components of the fiction not two.
[00:45:23.710 - 00:45:29.600] So how can we transform this from our little 2 by 2 into a 4 by 4?
[00:45:29.600 - 00:45:31.600] So how do we actually go about that?
[00:45:31.600 - 00:45:38.600] Well this comes back to why we had that relatively rigorous mathematical process to give our stiffness matrix.
[00:45:38.600 - 00:45:43.600] So this is what the definition was when we defined our little 2 by 2, the few pages ago.
[00:45:43.600 - 00:45:57.290] What we can do, we know that our Ubar, you can't sorry, has equal to our state functions times d.
[00:45:57.290 - 00:46:06.290] We can also incorporate its up case, our vector of state functions times our d e.
[00:46:06.290 - 00:46:15.290] And then we can say our up case state functions but what we can substitute here is the lower case d e is equal to the up case member times up case d e.
[00:46:15.290 - 00:46:20.290] And then we can group this so we can do the grouping slightly differently here to here.
[00:46:20.290 - 00:46:29.290] And what that means is that we can use the same variables but now we're doing a completely transformation.
[00:46:29.290 - 00:46:36.290] So we're going from our local coordinates to our global coordinates and there's some extra things up here and here.
[00:46:36.290 - 00:46:44.290] So what was just the shape functions is now the transformation matrix times the shape function and the same thing here.
[00:46:44.290 - 00:46:49.290] So those, the transformation matrix now appears in here, I mean it didn't before.
[00:46:49.290 - 00:46:54.290] So we're doing our little 2 by 2, the transformation matrix wasn't in here.
[00:46:54.290 - 00:47:02.290] Now it is and that leads us through here that basically we can group the terms.
[00:47:02.290 - 00:47:05.290] Everything within that bracket is what we defined as our K e.
[00:47:05.290 - 00:47:16.060] So this bracket is our K e, that's our 2 by 2.
[00:47:16.060 - 00:47:19.060] So that gives rise to the equation here.
[00:47:19.060 - 00:47:22.060] So that's the equation we've already listed matrix we've already defined.
[00:47:22.060 - 00:47:27.060] Then we have our we pre multiply by the transpose of the shape of the transformation matrix and
[00:47:27.060 - 00:47:32.060] post multiply by the transformation matrix and that gives us this.
[00:47:32.060 - 00:47:33.060] So the equation here.
[00:47:33.060 - 00:47:43.060] So now we have a stiffness equation which is a 4 by 4 and applies to the global coordinates but it's refined relative to the thing we already knew.
[00:47:43.060 - 00:47:50.060] If we do the multiplication here then we get this slightly longer version here.
[00:47:50.060 - 00:47:55.060] Now entering this into the code is one of the key things you'll be doing in the lab this way.
[00:47:55.060 - 00:48:21.280] So while this is correct I would strongly encourage you in the lab and the computer lab this week into the matrix using this information.
[00:48:21.280 - 00:48:35.580] And not saying that because the one below is wrong.
[00:48:35.580 - 00:48:44.580] They are methodically equal and if you want to sit there and type in 6 down 4 by 4 matrix with 16 individual components and
[00:48:44.580 - 00:48:46.580] you draw that way go right here.
[00:48:46.580 - 00:48:48.580] We'll give you the right answer there's nothing wrong with doing that.
[00:48:48.580 - 00:48:57.580] But you can actually just enter the 2 by 2 you can enter your transformation matrix and then just do this more location and Python will do all the hard work for you.
[00:48:57.580 - 00:49:05.580] So it's my strong advice that you use this way and get the computer to do the groundwork rather than entering all this manually.
[00:49:05.580 - 00:49:56.140] So this one here is the element stiffness matrix for woodnuts or 2 by 2 is the element stiffness matrix.
[00:49:56.140 - 00:50:01.140] Now one last thing about the lab this week is that this is a 2 by 2 and this is a 4 by 4.
[00:50:01.140 - 00:50:06.140] So if you enter change them and you're code you're generating that with things that just don't multiply together.
[00:50:06.140 - 00:50:12.140] So there'll be a nice red flag that's raised that can show you that perhaps you've done the code all wrong.
[00:50:12.140 - 00:50:17.140] In future works weeks we're going to have a matrix which is a such nice sex.
[00:50:17.140 - 00:50:21.140] And it will be 6 by 6 that are local level and at a global level.
[00:50:21.140 - 00:50:32.140] So it's a different matrices but they'll still have the same dimensions and that means that when you go through and code them, if you get them wrong, it will still more quite to get a fine and it will give you an answer.
[00:50:32.140 - 00:50:34.140] It will just give you the wrong answer.
[00:50:34.140 - 00:50:38.140] So this week's probably a good opportunity to go through that and see how that works.
[00:50:38.140 - 00:50:45.140] So thank you all for coming along. I'll see you again on Wednesday and we'll talk about how to build up an actual structure next promise.

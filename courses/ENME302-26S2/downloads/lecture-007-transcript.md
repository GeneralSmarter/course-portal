# ENME302-26S2 Lecture 7 fast-pass local ASR transcript

Date: July 23, 2026 10:00am-10:55am
Transcript type: Hermes fast-pass local ASR from validated Echo audio, not a native Echo transcript.
Backend/model: faster-whisper tiny.en, CPU int8, beam_size=1, vad_filter=True.
Quality note: fast catch-up transcript. Technical terms, equations, names and Māori words need checking against slides/audio before assessment use.
Source audio SHA-256: `974d2fc3cb9fa6a87411cb105af455a2c3ad01bbee7fe78474e9b952ad3e2d79`
Generated: 2026-07-24T23:32:43.664571+12:00

[00:00:00.460 - 00:00:03.870] Well, kabakoto.
[00:00:03.870 - 00:00:04.870] What?
[00:00:04.870 - 00:00:05.870] So, yeah.
[00:00:05.870 - 00:00:08.870] kabakoto, welcome along everyone.
[00:00:08.870 - 00:00:16.070] I guess the main purpose of today's lecture is going to just first off the summary of
[00:00:16.070 - 00:00:20.270] how to solve problems and we're going to work through the problem and conceptually that
[00:00:20.270 - 00:00:27.000] you'll be doing in the late afternoon and just touch a little bit on the coding approach.
[00:00:27.000 - 00:00:34.000] So, what we have here is the problems that we've been solving.
[00:00:34.000 - 00:00:38.000] We've been through the process of defining the overall Q values.
[00:00:38.000 - 00:00:41.000] So, Q1 is the degree of frame.
[00:00:41.000 - 00:00:46.000] So, it's the amount by which this node translates in the horizontal direction.
[00:00:46.000 - 00:00:50.000] Then the upper-case Q1 is the corresponding applied to external force.
[00:00:50.000 - 00:00:52.000] There was a number of matches here.
[00:00:52.000 - 00:00:55.000] The two here because there's the legitimate non-zero displacements, but none here are here because
[00:00:55.000 - 00:00:57.000] they can strain.
[00:00:57.000 - 00:01:02.000] The new step of introduced yesterday was this concept of an assembly matrix, which is
[00:01:02.000 - 00:01:08.000] essentially just the matrix that contains only zeroes and ones and the ones indicate that
[00:01:08.000 - 00:01:13.000] the degree of freedom, in this case, degree of frame 34, element 1 corresponds to Q1 for
[00:01:13.000 - 00:01:19.000] the structure and degree of frame 4, element 1, corresponds to the second degree of the
[00:01:19.000 - 00:01:20.000] structure.
[00:01:20.000 - 00:01:24.000] Similar approach for element 2 with a difference.
[00:01:24.000 - 00:01:26.000] The simulator is the constraint there.
[00:01:26.000 - 00:01:30.000] And once we have that, we can build up the system.
[00:01:30.000 - 00:01:35.500] So, the other thing that we saw, the sort of potential consistency for before, but at any
[00:01:35.500 - 00:01:42.000] no-repoint, the summation of the internal element forces that that node must sum up to the
[00:01:42.000 - 00:01:44.000] applied external load.
[00:01:44.000 - 00:01:48.000] So, if the applied external load is non-zero, we'll add value, and if there's no external load,
[00:01:48.000 - 00:01:50.000] we'll add a value at the zero.
[00:01:50.000 - 00:01:54.000] So, that's what it would look like in this case from our free-body diagrams.
[00:01:54.000 - 00:02:04.200] Essentially, F3, F1, and F1, F2 will sum up to be Q1, which is what's shown on represent
[00:02:04.200 - 00:02:11.000] here, and then F4, which is the upwards forcing term here, F4, F1, and F2, element 2,
[00:02:11.000 - 00:02:16.920] or sum up to the second value Q2.
[00:02:16.920 - 00:02:21.920] So, we're working through here, and this was just a summary of the process, the kg.
[00:02:21.920 - 00:02:27.920] We use our sinew matrix to build up our overall surface matrix kg.
[00:02:27.920 - 00:02:30.920] And then we went through here, and we solved the problem.
[00:02:30.920 - 00:02:34.920] And this was the point at which we sort of once we solved the system simultaneously, once we bring in that sort of
[00:02:34.920 - 00:02:39.920] NP.Linal.solve, that's sort of the nominal solutions dip.
[00:02:39.920 - 00:02:45.840] And any further analysis we do after that is generally referred to as post-processing.
[00:02:45.840 - 00:02:52.840] So, the two directional loads, so we'll do reaction of forces F1 and F2 at joint 1,
[00:02:52.840 - 00:03:01.840] and this is the, of course, is 4 element 1, because in this instance,
[00:03:01.840 - 00:03:06.840] element 1 is the only element that connects to this point here.
[00:03:06.840 - 00:03:16.840] Well, the reaction forces is 3 and F4 at joint 3, so these are, if 3 and F4, and that there is 4 elements.
[00:03:16.840 - 00:03:24.210] So, of course, if there was more than one element connecting into a given support point,
[00:03:24.210 - 00:03:28.210] the total reaction we would have to consider all those elements that connect in there.
[00:03:28.210 - 00:03:39.300] Once we hit the system solved, that's this stiffness equation that we need to work out what these forces are.
[00:03:39.300 - 00:03:44.300] But to get that, we need our OK.D, and we can, so we could work out, wow,
[00:03:44.300 - 00:03:48.300] let us know that most of the spine, therefore, that cross-volt into the settlement,
[00:03:48.300 - 00:03:53.300] the information to do that is already presented in our assembly matrix here.
[00:03:53.300 - 00:03:58.650] So, this little past cue is our solved global defections.
[00:03:58.650 - 00:04:17.520] Probably another important thing here is that there are assembly matrix, both builds up our system.
[00:04:17.520 - 00:04:36.100] That's because we use that to generate the overall kg, but also, breaks it down.
[00:04:36.100 - 00:04:46.470] So, it's a key skip in building up our overall system, but then also once we have the system solved,
[00:04:46.470 - 00:04:50.470] we can then use it to pull out relative pieces of cue.
[00:04:50.470 - 00:04:56.470] Now, for a much larger structure, this lower-case cue victim might have 20, 30, 100 elements.
[00:04:56.470 - 00:05:03.470] If I had 100 elements, the vast majority of those numbers aren't relevant to the particular element that we consider in.
[00:05:03.470 - 00:05:08.470] So, if there's 100 numbers in here, because there's 100 degrees for freedom and an overall structure,
[00:05:08.470 - 00:05:13.470] only four of them might be relevant to this particular element, but the assembly matrix will take care of that.
[00:05:13.470 - 00:05:19.070] So, we don't have to do it manually. We've already done the hard work in generating the assembly matrix.
[00:05:19.070 - 00:05:22.070] Let's use it to do what we need to do.
[00:05:22.070 - 00:05:25.070] Once we've done that, we can just go through and we can get it.
[00:05:25.070 - 00:05:32.070] We can get it forcing terms. Now, with all the forcing terms and when we're post-pretching and interpreting results,
[00:05:32.070 - 00:05:36.070] the key things refer back to our free body diagrams.
[00:05:36.070 - 00:05:38.070] It's a really, really important step.
[00:05:38.070 - 00:05:41.070] So, this here at the moment is just a vector of numbers.
[00:05:41.070 - 00:05:45.070] It's one of the immediately apparent what the physical meaning of it is.
[00:05:45.070 - 00:05:54.070] But if we take that and consider that alongside this diagram, then, quite quickly, we can attach significant and meaning to those numbers.
[00:05:54.070 - 00:06:13.140] So, this was x and y, common one, and then we just translating these numbers to here, then what we can not worth is, zero newtons.
[00:06:13.140 - 00:06:35.610] Really clean. And then we end up with the diagram of sort of y, that's a negative, so we can draw it to the left, q1.
[00:06:35.610 - 00:06:45.610] And the right hand side, the f3 is horizontal, so that there is our q1 and then the vertical component is zero newtons.
[00:06:45.610 - 00:06:54.610] So, as we would expect, because this is a pinduated bar, there's no shepherds, but there's an axial, axial force in there.
[00:06:54.610 - 00:07:07.800] Likewise, or element 2. To interpret that, the key thing is refer back to our free body diagram and see how that's all.
[00:07:07.800 - 00:07:16.800] So, this was no one and no two, so d1, d2, d3, d4, and corresponding forcing terms.
[00:07:16.800 - 00:07:38.220] So, if we would skip that there, noting that the axis were downwards on there, zero newtons that way.
[00:07:38.220 - 00:07:54.690] So, if one is zero, if two is the vertical component, that's q2, and then if three is zero, and then if one is equal to minus q2.
[00:07:54.690 - 00:08:01.690] So, it's drawn upwards in our free body diagram, or because it's negative, and I draw it downwards, and they will make the q2.
[00:08:01.690 - 00:08:10.270] We could equally draw upwards and put a negative q2 on there, but be the same thing.
[00:08:10.270 - 00:08:23.270] So, the important thing there is to recognize that there's that seepus to interpret, and understand this isn't just some array of numbers that actually has a physical structure.
[00:08:23.270 - 00:08:41.500] Some final general comments, which we covered briefly, you still have to govern them briefly again.
[00:08:41.500 - 00:08:47.500] So, number of columns is equal to the number of degrees of freedom.
[00:08:47.500 - 00:08:50.500] So, it's fully aligned in global coordinates, which is always four for a bar.
[00:08:50.500 - 00:08:54.500] The number of rows is pinned to the number of degrees of freedom for the structure.
[00:08:54.500 - 00:09:00.500] So, there's very few structure of the structure, and the larger the structure, the more degrees of freedom is likely to be.
[00:09:00.500 - 00:09:06.500] There should only be ones and zeros on there, so it only match things across, it doesn't create new numbers.
[00:09:06.500 - 00:09:11.500] So, it doesn't scale anything or create new numbers, it just max across, and puts them into the cross learning location.
[00:09:11.500 - 00:09:22.500] And of course, everything we do in space upon this number of sequence, which is global x, global y, and 1, being 10 to the 2, global x, global y, no 2, being 3, 24.
[00:09:22.500 - 00:09:29.100] Now, we did cover this just in the case today, I've got to begin very briefly.
[00:09:29.100 - 00:09:35.100] Local coordinates, global coordinates, this is the key number of sequence that we apply.
[00:09:35.100 - 00:09:38.100] In this case, this might be alpha of zero degrees.
[00:09:38.100 - 00:09:48.420] Here, alpha for the element, and alpha.
[00:09:48.420 - 00:09:52.420] That might be something like 35 degrees.
[00:09:52.420 - 00:09:58.420] As we start, a line with x, global, and we rotate count clockwise, and to where a line with x for the element.
[00:09:58.420 - 00:10:07.460] In this situation, with x is defined point in this way, the direction of the pin.
[00:10:07.460 - 00:10:23.460] So, for exactly here we would go say to 90, 180, 270, and then continue on to maybe around alpha for the element, in about 335 degrees.
[00:10:23.460 - 00:10:30.460] Or we could write alpha being minus 25 degrees.
[00:10:30.460 - 00:10:34.460] So, we could rotate clockwise if we want, but that's the opposite of our time convention.
[00:10:34.460 - 00:10:38.460] So, if we do that, we need to include a negative limit.
[00:10:38.460 - 00:10:45.460] The same element here, if we flip that through 180 degrees, these are equally valid choices.
[00:10:45.460 - 00:10:49.460] If the element was in the location, we could choose either of these assumptions in terms of the element.
[00:10:49.460 - 00:10:51.460] We just need to be consistent.
[00:10:51.460 - 00:10:59.460] In this case here, we'd be starting a line with x, global, and we'd be able to read 90, and then through to about 155 degrees.
[00:10:59.460 - 00:11:05.460] And that the element, alpha for that element, would be sort of 155 degrees here.
[00:11:05.460 - 00:11:07.460] Now, it's the same element with those numbers.
[00:11:07.460 - 00:11:11.460] The angular orientation is different.
[00:11:11.460 - 00:11:13.460] So, two is the numbering.
[00:11:13.460 - 00:11:16.460] So, what was D1 and D2 here is now D3 and D4.
[00:11:16.460 - 00:11:19.460] What was D3 and D4 is now D1 and D2?
[00:11:19.460 - 00:11:20.460] That would change.
[00:11:20.460 - 00:11:21.460] They're seemingly matrix.
[00:11:21.460 - 00:11:23.460] Some of the intermediate stuff will change.
[00:11:23.460 - 00:11:32.960] The final answer will not, as long as you're consistent.
[00:11:32.960 - 00:11:43.380] So, just to recap, we'd find all those degrees of freedom and allowable motions with an structure.
[00:11:43.380 - 00:11:45.380] And we'll label those with Q-dummies.
[00:11:45.380 - 00:11:47.380] So, there's a vehicle of numbers.
[00:11:47.380 - 00:11:52.380] We may represent the translations that have occurred at each node or point.
[00:11:52.380 - 00:11:55.380] Then we have our upper case Q.
[00:11:55.380 - 00:11:59.380] So, that is the vehicle of applied to neural nodes that are called some matches to this.
[00:11:59.380 - 00:12:05.380] Then we have our stuff mis equations at the element coordinate system, global coordinate system,
[00:12:05.380 - 00:12:07.380] and Dn our assembly matrix.
[00:12:07.380 - 00:12:42.850] So, this set here the number of Q's relates to number of nodal points and the number of support points.
[00:12:42.850 - 00:12:56.300] That course also feeds down here to be the number of rows and our assembly matrix.
[00:12:56.300 - 00:13:06.120] The number element degrees of freedom and global quarters is the number of columns and assembly matrix.
[00:13:06.120 - 00:13:12.120] And that there's always four, four-way by element.
[00:13:12.120 - 00:13:17.710] Once we get to frame elements, it will become six.
[00:13:17.710 - 00:13:20.710] But for now, for bar elements, everything we're done this week,
[00:13:20.710 - 00:13:23.710] that'll be four columns when we see the matrix.
[00:13:23.710 - 00:13:35.880] We can go through, this is the step of our building our path over all the stiffness matrix.
[00:13:35.880 - 00:13:37.880] This is the thing that we used to solve.
[00:13:37.880 - 00:13:43.880] We've used the matrix in this here or in P.
[00:13:43.880 - 00:13:45.880] We've built the L.
[00:13:45.880 - 00:13:54.460] The solve sorties matrix solution.
[00:13:54.460 - 00:13:57.460] And then we've got the cross-running breakdown,
[00:13:57.460 - 00:14:00.460] extracting relevant components, etc.
[00:14:00.460 - 00:14:07.460] From the post-processing interrogate the results to provide understanding.
[00:14:07.460 - 00:14:13.460] And the other thing, what the elements are doing, what the required root support reactions are, etc.
[00:14:13.460 - 00:14:24.340] So, the next couple of pages here, page 46 and 47.
[00:14:24.340 - 00:14:32.380] This is essentially, I'm well aware, we have a KE, we have a KE hat,
[00:14:32.380 - 00:14:35.380] we have a KG for an element, we have a KG.
[00:14:35.380 - 00:14:39.380] There's lots of different, there's essentially four different stiffness matrices that we're talking about.
[00:14:39.380 - 00:14:45.380] And this page here is trying to just make that really clear and help you understand.
[00:14:45.380 - 00:14:49.380] I know that with numerical methods half of the battles is understanding what everything means,
[00:14:49.380 - 00:14:51.380] what all the variable means.
[00:14:51.380 - 00:14:53.380] So this is hopefully trying to make that a little bit simpler.
[00:14:53.380 - 00:14:56.380] So, we start out here with this is the stiffness matrix.
[00:14:56.380 - 00:15:01.380] So this is the stiffness matrix supplied in local coordinates at an element level.
[00:15:01.380 - 00:15:05.380] So, the lower case here is K times the lower case D.
[00:15:05.380 - 00:15:08.380] This is the element stiffness matrix in local coordinates.
[00:15:08.380 - 00:15:12.380] And we have element information on geometric material properties.
[00:15:12.380 - 00:15:15.380] So, we have, this is comes in through E, A and L.
[00:15:15.380 - 00:15:19.860] We don't even have any information on the orientation of the element,
[00:15:19.860 - 00:15:24.860] how it's connected to other elements in the structure, or any information on any other element.
[00:15:24.860 - 00:15:28.860] So, any information about one element, and only a limited information.
[00:15:28.860 - 00:15:32.860] Once we introduce the transformation matrix.
[00:15:32.860 - 00:15:36.860] So, this is just depending on the angle of orientation alpha.
[00:15:36.860 - 00:15:39.860] And we do this multiplication, we go from KE to KE hat.
[00:15:39.860 - 00:15:42.860] And this is the corresponding stiffness equation.
[00:15:42.860 - 00:15:48.860] And once we've done that, we've introduced an information on element orientation.
[00:15:48.860 - 00:15:53.860] We don't need having information on support points connectivity or other elements.
[00:15:53.860 - 00:15:57.860] Then when we introduce the assembly matrix here.
[00:15:57.860 - 00:15:59.860] And we do this multiplication.
[00:15:59.860 - 00:16:02.860] We go from our KE hat to our KE for the elements.
[00:16:02.860 - 00:16:05.860] Now, that has taken us from all the information we had previously.
[00:16:05.860 - 00:16:09.860] But now it has also introduced the connectivity.
[00:16:09.860 - 00:16:12.860] How this element is connected to the structure.
[00:16:12.860 - 00:16:16.860] So, for that given element, it now has all the information that needs.
[00:16:16.860 - 00:16:19.860] That is the key thing is it is unusual one element onto that point.
[00:16:19.860 - 00:16:23.860] Then we just sum up those contributions across the whole structure.
[00:16:23.860 - 00:16:28.860] And then we have all the geometric material properties, information on element orientation.
[00:16:28.860 - 00:16:30.860] We have information on connectivity.
[00:16:30.860 - 00:16:33.860] And we now have information that you've read element with the structure.
[00:16:33.860 - 00:16:38.860] So, that progression there gives us the overall stiffness equation.
[00:16:38.860 - 00:16:42.860] And this is what we solve simultaneously to get a solution.
[00:16:42.860 - 00:16:48.860] So, hopefully this chart, this table, which sort of helps show that progression of information.
[00:16:48.860 - 00:16:51.860] And it gives meaning to what all these different variables mean.
[00:16:51.860 - 00:16:55.860] So, now that's half the better when we do the start with computational work.
[00:16:55.860 - 00:17:04.540] Now, further to that, and it's not a coincidence.
[00:17:04.540 - 00:17:11.540] These two are posing slides at the same open page on the book.
[00:17:11.540 - 00:17:14.540] Let's just look at a larger pinduated structure.
[00:17:14.540 - 00:17:18.540] So, we're going to assume we have this pinduated truss.
[00:17:18.540 - 00:17:21.540] This pends to the supports. All the elements are pinned to each other.
[00:17:21.540 - 00:17:26.540] We haven't yet looked to look at what loads are in here, but we won't worry about that.
[00:17:26.540 - 00:17:30.540] It could be anything as long as the loads are at the nodal points.
[00:17:30.540 - 00:17:32.540] Now, we assume we have a nice square grid.
[00:17:32.540 - 00:17:36.540] We have the vertical distance as 10 meters, the horizontal distance as 10 meters.
[00:17:36.540 - 00:17:45.580] If we assume that they're all made from the same path stop, we'll do a stop size.
[00:17:45.580 - 00:17:50.580] So, it could be a high section, it could be a solid section, we're assuming that we've got some sort of length,
[00:17:50.580 - 00:17:52.580] and we'll cover to link them as similar to the truss problem.
[00:17:52.580 - 00:17:57.580] So, everything in the area element has the same cross sectional area and the same on the step-on-jouess.
[00:17:57.580 - 00:18:03.580] Now, within here, all the horizontal and vertical elements have the same length.
[00:18:03.580 - 00:18:08.580] So, we've got a small 1.5937 and 4.8 are all 10 meters long.
[00:18:08.580 - 00:18:18.690] So, they're all equal to each other, and of course, also equal to 10 meters.
[00:18:18.690 - 00:18:25.690] The three-day elements, 2, 6 and 10, are going to be equal to each other.
[00:18:25.690 - 00:18:31.290] They're going to be about 14.1 meters just root 2 times 10.
[00:18:31.290 - 00:18:35.290] So, 7 of the 10 numbers have the same length,
[00:18:35.290 - 00:18:39.290] and the three of the 10 have a different length, and as a result of that,
[00:18:39.290 - 00:18:43.290] the k matrix for those three elements is going to be different.
[00:18:43.290 - 00:18:49.290] And that's just some people because the k matrix depends on the material property,
[00:18:49.290 - 00:18:54.290] E and geometry, geometric properties, AML, so cross sectional area and length.
[00:18:54.290 - 00:18:58.290] So, all those seven elements we have the same k matrix,
[00:18:58.290 - 00:19:02.290] but they'll have, and these three will have the same as each other.
[00:19:02.290 - 00:19:05.290] So, we're going to go to a group of seven, and that is a group of three.
[00:19:05.290 - 00:19:11.700] There's only two unique k matrices that exist for elements within the structure.
[00:19:11.700 - 00:19:15.700] However, when we go to the next step, and we introduce element orientation information,
[00:19:15.700 - 00:19:19.700] and once 1, 5, 9, 3 and 7 are all horizontal.
[00:19:19.700 - 00:19:22.700] They all have a zero degree transformation angle.
[00:19:22.700 - 00:19:28.700] So, once we go to that, the introduced the transformation matrix and go to k,
[00:19:28.700 - 00:19:36.700] all the horizontal elements are the same, but they are now different to the two k, 4 and k hat matrices.
[00:19:36.700 - 00:19:41.700] So, they were all the same up here, but now 4 and 8 broke out to be a different matrix,
[00:19:41.700 - 00:19:46.700] because they're on a different orientation, but all of the horizontal elements remain the same.
[00:19:46.700 - 00:19:52.700] And then the three vertical elements, sort of the three inclined elements to 16,
[00:19:52.700 - 00:19:57.700] they're all on the same orientation, have the same geometric or material properties,
[00:19:57.700 - 00:19:59.700] so they're 4 other things each other.
[00:19:59.700 - 00:20:04.700] So, hopefully you see this progression when things are the same initially in the breakout for different reasons,
[00:20:04.700 - 00:20:09.700] that supports the progression of information being introduced within these different matrices.
[00:20:09.700 - 00:20:15.260] Once we introduce element connectivity information,
[00:20:15.260 - 00:20:18.260] that's the information that comes in through these same lee matrix.
[00:20:18.260 - 00:20:23.260] Once we introduce that information, every single matrix here is different.
[00:20:23.260 - 00:20:27.260] And the reason for that is that they all connect them to the structure differently.
[00:20:27.260 - 00:20:32.600] So, that connectivity information is the final piece of the puzzle, and once you've done that,
[00:20:32.600 - 00:20:37.600] every single contribution to kG is different, and when just sum them all up,
[00:20:37.600 - 00:20:40.600] we would get the overall kG.
[00:20:40.600 - 00:20:45.600] Now, unfortunately the format is messed up a little bit here, so my apologies for that.
[00:20:45.600 - 00:20:46.600] It could be cleaner.
[00:20:46.600 - 00:20:55.420] So, hopefully that example just helps to underscore what the different meanings of the different matrices are,
[00:20:55.420 - 00:20:57.420] and how to interpret them.
[00:20:57.420 - 00:21:14.660] There's re-equitions on that before we proceed.
[00:21:14.660 - 00:21:20.660] So, this here, as the old arrow fringe, the two element bar problem.
[00:21:20.660 - 00:21:22.660] We've solved this a few times.
[00:21:22.660 - 00:21:24.660] We're at different methods.
[00:21:24.660 - 00:21:27.660] This is the same example we used when we did different sort of digital space events.
[00:21:27.660 - 00:21:31.660] We solved it by doing that weird quadrilateral thing.
[00:21:31.660 - 00:21:35.660] We're doing it again, but this time we're coming in it from finite elements analysis.
[00:21:35.660 - 00:21:38.660] And from the outset, I just want to say, you might look at this and say,
[00:21:38.660 - 00:21:40.660] well, we've done this problem a lot.
[00:21:40.660 - 00:21:42.660] It wasn't that hard to solve by hand.
[00:21:42.660 - 00:21:46.660] What we're doing is we've been smoking maximum, so this is a simple problem.
[00:21:46.660 - 00:21:50.660] If we made this step in the terminal, we put some extra support, some extra elements in.
[00:21:50.660 - 00:21:54.660] This would become really hard to solve by hand, but it wouldn't actually get much harder
[00:21:54.660 - 00:21:56.660] all through the finite element system.
[00:21:56.660 - 00:22:00.660] So, it might be an unfair comparison that you're looking at us at.
[00:22:00.660 - 00:22:07.660] You could actually solve this relatively easily by hand, but it is just a simple base structure that we can look at.
[00:22:07.660 - 00:22:11.660] So, I won't go through all the deep information there.
[00:22:11.660 - 00:22:14.660] It's the same structure we've looked at a few times now.
[00:22:14.660 - 00:22:18.040] We've also got two degrees of freedom there.
[00:22:18.040 - 00:22:21.040] So, this is very much like the problem we actually just solved,
[00:22:21.040 - 00:22:24.040] but we're the signal of being vertical.
[00:22:24.040 - 00:22:27.040] We've pulled around us down the line.
[00:22:27.040 - 00:22:32.040] So, the key information here is element one.
[00:22:32.040 - 00:22:34.040] This is the number one here.
[00:22:34.040 - 00:22:40.040] Defined this yes, this would mean alpha for one, and one is zero degrees.
[00:22:40.040 - 00:22:45.630] This is that means that's no one and that's no two.
[00:22:45.630 - 00:22:48.630] D1, D2, D3, D4.
[00:22:48.630 - 00:22:53.630] And what we can see here is that Q1 comes down and corresponds to D3.
[00:22:53.630 - 00:22:58.630] So, Q3 is equal to D3, what element one?
[00:22:58.630 - 00:23:08.090] Similarly, the vertical one comes down, and that's equal to D4.
[00:23:08.090 - 00:23:13.090] So, Q2 is equal to D4, the element one.
[00:23:13.090 - 00:23:24.360] That's the key information that we need to generate error-synded matrix.
[00:23:24.360 - 00:23:26.360] The other steps are relatively procedural.
[00:23:26.360 - 00:23:29.360] So, we've got our EANL, we've put that on the generator element,
[00:23:29.360 - 00:23:31.360] or two by two matrix.
[00:23:31.360 - 00:23:35.360] We can do our k hat using the transformation matrix.
[00:23:35.360 - 00:23:41.360] But this is the key, the two key pieces of information we need to generate
[00:23:41.360 - 00:23:45.360] a simply matrix, because that's the one more manual step that we need to.
[00:23:45.360 - 00:23:53.020] We can also we just put this structure of the element two
[00:23:53.020 - 00:23:55.020] after the side here.
[00:23:55.020 - 00:24:01.020] So, D1 and D2, cross-ventour fixed support,
[00:24:01.020 - 00:24:04.020] there's no Q values assigned here.
[00:24:04.020 - 00:24:08.020] So, they don't cross-vent anything globally.
[00:24:08.020 - 00:24:15.020] So, D3 here is cross-ventour Q1.
[00:24:15.020 - 00:24:19.020] So, that's the same level point, and in the same direction.
[00:24:19.020 - 00:24:26.270] So, Q1 is equal to D3, four element two, and then,
[00:24:26.270 - 00:24:47.790] Q2 is equal to D4, some of the key information that we need.
[00:24:47.790 - 00:24:49.790] So, we take that information we've just determined,
[00:24:49.790 - 00:24:52.790] and we use that to generate error-synded matrixes.
[00:24:52.790 - 00:24:59.790] D3, one, cross-ventour Q1, that's where the one comes from.
[00:24:59.790 - 00:25:04.790] D4, one, cross-ventour Q2, that's where that one comes from.
[00:25:04.790 - 00:25:13.360] And then, for a second element here, D3, one,
[00:25:13.360 - 00:25:19.360] two, Q1 correspond, D4, one, two, and Q2.
[00:25:19.360 - 00:25:23.360] So, that's the process of generating these semi-matrices.
[00:25:23.360 - 00:25:27.360] Once we've got that, we can discuss our equation here.
[00:25:27.360 - 00:25:35.360] So, the space piece here, that there is our KG1,
[00:25:35.360 - 00:25:41.360] and the space here is our KG2.
[00:25:41.360 - 00:25:46.980] We have them together to get our overall KG.
[00:25:46.980 - 00:25:50.980] And maybe you don't care that much.
[00:25:50.980 - 00:25:52.980] I think it's important.
[00:25:52.980 - 00:25:56.980] When we did this in the second element, it was vertical.
[00:25:56.980 - 00:25:59.980] Then, what we saw was that there was numbers on the main diagonal,
[00:25:59.980 - 00:26:03.980] but the off-diagonal terms were zero, which meant that there's essentially no cut-fung.
[00:26:03.980 - 00:26:05.980] You kind of solve them two end-of-end equations.
[00:26:05.980 - 00:26:09.980] Because we've now inclined the element, you see this is a fully populated element,
[00:26:09.980 - 00:26:15.980] a fully populated matrix, and we would have to solve that as a sort of a set of equations.
[00:26:15.980 - 00:26:17.980] That's not hard.
[00:26:17.980 - 00:26:28.110] We've got a computer that can do that for us, and we're going to do just that.
[00:26:28.110 - 00:26:32.110] Now we need to define, because this is the system of equation to be able to solve.
[00:26:32.110 - 00:26:35.110] KG, we've just determined we would build that up.
[00:26:35.110 - 00:26:37.110] The lower KG is what we want to solve for.
[00:26:37.110 - 00:26:39.110] So, that's an unknown.
[00:26:39.110 - 00:26:42.110] So, we need our upper KGQ.
[00:26:42.110 - 00:26:48.110] So, our upper KGQ here is equal to say Q1, and Q2,
[00:26:48.110 - 00:26:52.360] and that's equal to this information here.
[00:26:52.360 - 00:26:55.360] So, the question is, will be this come from?
[00:26:55.360 - 00:26:57.360] This is given in the question.
[00:26:57.360 - 00:27:08.380] So, initially we were told that there was a 100 kiln Newton vertical load,
[00:27:08.380 - 00:27:09.380] and there was nothing wrong.
[00:27:09.380 - 00:27:12.380] So, that's where this information has come from.
[00:27:12.380 - 00:27:15.380] Then we can solve, you can actually just manually look at the inverse,
[00:27:15.380 - 00:27:27.640] but let's just simply use in p.lml.
[00:27:27.640 - 00:27:38.020] So, and when we go through, and we solve this,
[00:27:38.020 - 00:27:42.020] you probably by the stage might recognize some of these numbers.
[00:27:42.020 - 00:27:45.020] These are the same numbers that we got previously.
[00:27:45.020 - 00:27:49.020] The same numbers we first time through, we had to do all these pesky quadri-laterals,
[00:27:49.020 - 00:27:52.020] and got a trace through the geometry.
[00:27:52.020 - 00:27:55.020] When we did the work in engineering method for single loads,
[00:27:55.020 - 00:27:58.020] we got one of those to values, but not the other.
[00:27:58.020 - 00:28:01.020] And then when we applied the principle a bit to the space once,
[00:28:01.020 - 00:28:07.020] we got a whole table, and we had to do two different virtual loads on the structure,
[00:28:07.020 - 00:28:11.020] and we had to have those tables, and we did quite a lot of work on that.
[00:28:11.020 - 00:28:14.020] Here it is, directly for us.
[00:28:14.020 - 00:28:18.020] There's no independent, there's no manual intervention,
[00:28:18.020 - 00:28:20.020] we don't have any trace through geometries,
[00:28:20.020 - 00:28:24.020] we don't have to generate tables of virtual loads and things,
[00:28:24.020 - 00:28:28.020] the principle of virtual space is embedded into our derivation,
[00:28:28.020 - 00:28:31.020] and it's automatically incorporated into our result.
[00:28:31.020 - 00:28:39.600] So, the key thing you want to see here,
[00:28:39.600 - 00:28:50.010] these are the same values obtained manually,
[00:28:50.010 - 00:29:07.070] the lot of effort, from pages 18 to 25.
[00:29:07.070 - 00:29:37.530] No annoying quadri-vaterals, no need to manually interpret geometry.
[00:29:37.530 - 00:29:46.490] So hopefully you'll see the Cisci quadraticia, all the hard work's done for us,
[00:29:46.490 - 00:29:49.490] and this is for a relatively simple problem.
[00:29:49.490 - 00:29:53.490] If we added an extra element there that made me quite upwards,
[00:29:53.490 - 00:30:09.910] so we had maybe something like this, like this,
[00:30:09.910 - 00:30:16.820] like from above, down from below,
[00:30:16.820 - 00:30:20.820] it's the same thing, but within a third element added above.
[00:30:20.820 - 00:30:23.820] That actually becomes a lot harder to solve by hand,
[00:30:23.820 - 00:30:26.820] because now the problem is that the independent,
[00:30:26.820 - 00:30:30.820] and you actually have to look at the relative differences of the numbers
[00:30:30.820 - 00:30:33.820] that work out what proportion of the applied load they carry,
[00:30:33.820 - 00:30:36.820] and then once you know them, you know how much they defec,
[00:30:36.820 - 00:30:39.820] and you now look at three intersecting arcs,
[00:30:39.820 - 00:30:42.820] and the whole thing gets a lot more complicated,
[00:30:42.820 - 00:30:44.820] but for the final element method adding that third element
[00:30:44.820 - 00:30:49.820] is going to add maybe five or 10% to the time it takes to solve the problem.
[00:30:49.820 - 00:30:53.820] So, this is really powerful means,
[00:30:53.820 - 00:30:57.820] and it would generalise to larger, more complex structures,
[00:30:57.820 - 00:31:00.820] and much, much more easily than the manual if it's good.
[00:31:00.820 - 00:31:03.820] So, well, this is a problem we can solve manually.
[00:31:03.820 - 00:31:06.820] It's just a really simple initial problem as a benchmark,
[00:31:06.820 - 00:31:13.820] and the larger system is the final system really comes into a time.
[00:31:13.820 - 00:31:27.500] So, the main one we have here is we've got the predictions that come out.
[00:31:27.500 - 00:31:32.500] We can basically explain to us how we solved some of the techniques they hear.
[00:31:32.500 - 00:31:36.500] We've got this piece here as d for the element,
[00:31:36.500 - 00:31:38.500] as equal to the assembly matrix,
[00:31:38.500 - 00:31:47.710] transposed times q, so that's the matrix multiplication of the one-pike,
[00:31:47.710 - 00:31:52.980] and then we've got, yeah, one-folding terms,
[00:31:52.980 - 00:32:24.380] but also knowing here, the assembly matrix extracts the relevant pieces of the solved,
[00:32:24.380 - 00:32:46.220] and the signs then into the appropriate place within the D8,
[00:32:46.220 - 00:32:49.220] the detection vector for the element.
[00:32:49.220 - 00:32:58.680] Now, we have our forcing vector here,
[00:32:58.680 - 00:33:00.680] and again, I don't want you to just look at this and think,
[00:33:00.680 - 00:33:03.680] it's a vector of numbers, and I don't know if that means something.
[00:33:03.680 - 00:33:06.680] I really like to, you know,
[00:33:06.680 - 00:33:09.680] explain that to think about, well, what is the physical meaning of those numbers?
[00:33:09.680 - 00:33:16.680] And that, this remaining comes about from the element,
[00:33:16.680 - 00:33:18.680] for everybody's librarian.
[00:33:18.680 - 00:33:38.740] This was the first element here,
[00:33:38.740 - 00:33:40.740] and what we have here,
[00:33:40.740 - 00:33:49.180] this, the first element is the one that acts in the description,
[00:33:49.180 - 00:33:52.180] 100, 85, or 100 kilo-hounds.
[00:33:52.180 - 00:33:57.380] The second one is beautiful,
[00:33:57.380 - 00:34:00.380] and that's zero-hootens.
[00:34:00.380 - 00:34:03.380] Then we have negative 100 kilo-hounds,
[00:34:03.380 - 00:34:10.380] so the coordinate system for this element is x and y.
[00:34:10.380 - 00:34:16.380] So this is actually 100 kilo-hounds and words,
[00:34:16.380 - 00:34:19.380] and then we have finally zero-hootens,
[00:34:19.380 - 00:34:20.380] vertically as well.
[00:34:20.380 - 00:34:31.220] So if you look back to when we've resolved this problem,
[00:34:31.220 - 00:34:36.220] previously we did also find that there was 100 kilo-hounds of compression within that element.
[00:34:36.220 - 00:34:44.070] So then we want to look at the element two,
[00:34:44.070 - 00:34:59.310] and we want to look at the force in terms that exist within that.
[00:34:59.310 - 00:35:03.310] So we've got reaction forces at point B,
[00:35:03.310 - 00:35:04.310] vertical components.
[00:35:04.310 - 00:35:08.310] So we can go through, we can extract the relative components using our assembly matrix
[00:35:08.310 - 00:35:11.310] and build up the force in term F2.
[00:35:11.310 - 00:35:13.310] Again, this is just a bit of numbers.
[00:35:13.310 - 00:35:18.850] We want to apply some physical meaning to this.
[00:35:18.850 - 00:35:23.700] So we'll sketch out the element like this,
[00:35:23.700 - 00:35:29.700] and, of course, we just go back to when we defined the free body diagram.
[00:35:29.700 - 00:35:31.700] So this was the free body diagram here.
[00:35:31.700 - 00:35:34.700] x is upwards, alpha is 45 degrees,
[00:35:34.700 - 00:35:36.700] therefore this is D1 and D2,
[00:35:36.700 - 00:35:39.700] and this is D3 and D4, and the corresponding force in terms.
[00:35:39.700 - 00:35:43.270] So we're going to take this vector,
[00:35:43.270 - 00:35:46.270] and we're going to apply it to this.
[00:35:46.270 - 00:35:48.270] So this were both negatives.
[00:35:48.270 - 00:35:50.270] They were to the right and upwards,
[00:35:50.270 - 00:35:52.270] and we're going to have a lot of negative.
[00:35:52.270 - 00:35:55.270] So we're going to say 100 kilo-nutens here,
[00:35:55.270 - 00:35:58.270] and 100 kilo-nutens here.
[00:35:58.270 - 00:36:02.740] Then at the other end, we have D3 and D4,
[00:36:02.740 - 00:36:04.740] which is to the right and upwards,
[00:36:04.740 - 00:36:09.740] and up a positive, so then we have 100 kilo-nutens here,
[00:36:09.740 - 00:36:12.740] and we want to have 100 kilo-nutens here.
[00:36:12.740 - 00:36:21.540] That's going to be indicative of the reaction forces at the bottom-pin support,
[00:36:21.540 - 00:36:25.540] and that also just tells us the forces that are induced within the main body diagram.
[00:36:25.540 - 00:36:32.510] So we can also look at the fictions.
[00:36:32.510 - 00:36:39.180] So once we've got, we can excuse the A-e transpose times Q,
[00:36:39.180 - 00:36:43.180] so this piece here is our D for the on,
[00:36:43.180 - 00:36:51.750] once we're more biobutant transformation matrix with our lower-case D.
[00:36:51.750 - 00:36:56.060] So this just gets that on the diagram.
[00:36:56.060 - 00:36:59.700] So this is the...
[00:36:59.700 - 00:37:04.130] We go through, we put them out,
[00:37:04.130 - 00:37:06.130] and this is the numbers that we get.
[00:37:06.130 - 00:37:10.130] So this is meters and meters.
[00:37:10.130 - 00:37:18.130] And what we see here is because this was the coordinates for our on one,
[00:37:18.130 - 00:37:21.410] x and y.
[00:37:21.410 - 00:37:27.410] We now say here that D1 for element one is equal to zero,
[00:37:27.410 - 00:37:29.410] because that's the first entry there.
[00:37:29.410 - 00:37:40.070] And then what we have here is that this one's moved D2
[00:37:40.070 - 00:37:45.070] is equal to negative 0.6 millimeters,
[00:37:45.070 - 00:37:47.070] because if you're in a compression, it's moved downwards.
[00:37:47.070 - 00:37:56.520] So we've gone through that process, and we've got our values now,
[00:37:56.520 - 00:38:10.390] just a quick sanity check here.
[00:38:10.390 - 00:38:16.390] So D1 for element one must be zero.
[00:38:16.390 - 00:38:23.300] It did, that's the answer we got, which is a good thing.
[00:38:23.300 - 00:38:27.300] But it's always good just to do a quick sanity check, as you work through it.
[00:38:27.300 - 00:38:31.300] So if you solve it, it could just be used the wrong assembly matrix,
[00:38:31.300 - 00:38:35.300] or you maybe use the wrong transformation matrix or something.
[00:38:35.300 - 00:38:39.300] And as a result of that, you've got a non-zero value for D1.
[00:38:39.300 - 00:38:41.300] You immediately know something's gone wrong.
[00:38:41.300 - 00:38:43.300] That's a huge red flag to say, let's just stop from a minute.
[00:38:43.300 - 00:38:45.300] Let's go back and just check the working,
[00:38:45.300 - 00:38:50.300] because the numerical result that I've got doesn't match the physical system.
[00:38:50.300 - 00:38:59.420] Equally 42, we've got the system here.
[00:38:59.420 - 00:39:05.520] We're going to draw the element.
[00:39:05.520 - 00:39:07.520] Look at this.
[00:39:07.520 - 00:39:11.520] And we have, this is the D2 vector.
[00:39:11.520 - 00:39:14.520] So the coordinate system was like this,
[00:39:14.520 - 00:39:16.520] with x outputs and y.
[00:39:16.520 - 00:39:23.520] That way, which then means that what we've got here is
[00:39:23.520 - 00:39:27.520] at node one, D1,
[00:39:27.520 - 00:39:30.520] node two is equal to zero meters.
[00:39:30.520 - 00:39:35.930] And then this one here, D2,
[00:39:35.930 - 00:39:40.930] the element two is 1.3 millimeters.
[00:39:40.930 - 00:39:45.240] So if this element's contracted, the compression,
[00:39:45.240 - 00:39:47.240] and this one's extended.
[00:39:47.240 - 00:39:51.240] These are rounded, but you'll see if you follow the full working.
[00:39:51.240 - 00:39:54.240] It will matches the numbers we had previously.
[00:39:54.240 - 00:39:56.240] Now down here, this was also a support point.
[00:39:56.240 - 00:39:58.240] So we're going to expect that to be zero.
[00:39:58.240 - 00:40:09.780] It's certainly a good thing that it is.
[00:40:09.780 - 00:40:12.780] Then we can look at strain.
[00:40:12.780 - 00:40:14.780] So x, your normal strain,
[00:40:14.780 - 00:40:18.780] is equal to the tangent length divided by the average norming.
[00:40:18.780 - 00:40:25.100] So we have that.
[00:40:25.100 - 00:40:27.100] If's long one,
[00:40:27.100 - 00:40:30.100] there's just, we can write that.
[00:40:30.100 - 00:40:35.100] The tangent length is equal to D2 for a given element,
[00:40:35.100 - 00:40:38.100] minus D1 for a given element.
[00:40:38.100 - 00:40:40.100] That's equal to the tangent length.
[00:40:40.100 - 00:40:43.100] So that's the amount I wish the second node has moved,
[00:40:43.100 - 00:40:45.100] minus D, and I wish the first node moves.
[00:40:45.100 - 00:40:47.100] So assume the second node was fixed.
[00:40:47.100 - 00:40:51.100] And there was a non-zero positive displacement in D1.
[00:40:51.100 - 00:40:53.100] There were the indicated compression.
[00:40:53.100 - 00:40:55.100] The element's shortening.
[00:40:55.100 - 00:40:57.100] But equally if D1 was fixed in D2,
[00:40:57.100 - 00:41:00.100] there was non-zero that would indicate a length of the entire strain.
[00:41:00.100 - 00:41:04.100] So you could press through those numbers.
[00:41:04.100 - 00:41:06.100] Then we have our surface equation again.
[00:41:06.100 - 00:41:13.350] We can also go into our forcing terms and local coordinates.
[00:41:13.350 - 00:41:22.870] So that gives us 100 kilonutes of compression within element one.
[00:41:22.870 - 00:41:24.870] So if we look back,
[00:41:24.870 - 00:41:27.870] element one's free body diagram,
[00:41:27.870 - 00:41:37.840] then local coordinates was D1 and F1.
[00:41:37.840 - 00:41:40.840] And then we have D2 and F2.
[00:41:40.840 - 00:41:43.840] So the fact that the first number is positive
[00:41:43.840 - 00:41:46.840] and the second number is negative means that this is,
[00:41:46.840 - 00:41:49.840] to N words, N words, N words, which means that this is a
[00:41:49.840 - 00:41:53.840] compressive load existing within here.
[00:41:53.840 - 00:41:58.840] So that these two numbers are the forcing glick that they must always be equal and opposite.
[00:41:58.840 - 00:42:04.840] But which one is negative and which one is positive,
[00:42:04.840 - 00:42:06.840] in the case with this is tangent or compression?
[00:42:06.840 - 00:42:08.840] So in this case, this would be compression.
[00:42:08.840 - 00:42:11.840] But in this case here, if two,
[00:42:11.840 - 00:42:16.840] we have a coordinate system like this.
[00:42:16.840 - 00:42:26.340] Then we have D1 and F1 down here, D2 and F2 up here.
[00:42:26.340 - 00:42:31.340] Then we've got the first number being negative means that that's actually an opposite direction,
[00:42:31.340 - 00:42:33.340] which is outwards, out of the element.
[00:42:33.340 - 00:42:37.340] This one is positive, that's outwards, which means this
[00:42:37.340 - 00:42:40.340] is pulling apart and this element is in tension.
[00:42:40.340 - 00:42:46.340] So both cases equal and opposite, but they still have different things there.
[00:42:46.340 - 00:42:48.340] There's a few extra things we can look at there,
[00:42:48.340 - 00:42:53.340] but I do want to just jump across a couple pages to page 55
[00:42:53.340 - 00:42:57.340] because this is the key thing we're looking at in the lab here this week.
[00:42:57.340 - 00:43:06.010] So this is really the point you want to start at in the lab this afternoon.
[00:43:06.010 - 00:43:11.770] We've got domestic modulus, links, the same problem again.
[00:43:11.770 - 00:43:14.770] So this is the problem we've just worked through.
[00:43:14.770 - 00:43:19.770] This is the step-by-step in Python with all the results.
[00:43:19.770 - 00:43:22.770] So local bar is not an endo function.
[00:43:22.770 - 00:43:24.770] As some of you are going to have to write.
[00:43:24.770 - 00:43:27.770] The best of all you have to do is give an EANL.
[00:43:27.770 - 00:43:30.770] You need to return this little too much of a matrix.
[00:43:30.770 - 00:43:34.770] It's going to be one of the easiest Python functions here we're going to write.
[00:43:34.770 - 00:43:36.770] You take three variables.
[00:43:36.770 - 00:43:39.770] You put them in one line of code to return a too much of a matrix.
[00:43:39.770 - 00:43:43.770] It's a bit too too major.
[00:43:43.770 - 00:43:49.770] But as I've written on the text here, I was strongly encouraged you to just make that code for one element.
[00:43:49.770 - 00:43:53.770] And then you call that code as many times as you have elements.
[00:43:53.770 - 00:43:57.770] Rather than writing a specific tutorial on this because then your structure has three or four.
[00:43:57.770 - 00:44:04.860] You've got to write your code.
[00:44:04.860 - 00:44:10.860] So then what we do here is we're taking the result KE from above
[00:44:10.860 - 00:44:32.860] the angle alpha, getting the transformation matrix and KE has.
[00:44:32.860 - 00:44:46.780] So what we're doing there is referring to the transformation matrix which is defined here.
[00:44:46.780 - 00:44:48.780] This is a value.
[00:44:48.780 - 00:44:55.120] It's just the case on the sign terms and then doing the multiplication.
[00:44:55.120 - 00:45:20.320] Now one thing just to be very obvious is that the angle alpha in Python is expected as radians into cause and sign functions.
[00:45:20.320 - 00:45:32.640] Now these are things to do there if you've got, if you put it for, if you want to put the angles and integrase,
[00:45:32.640 - 00:45:37.640] you can just use the NP dot radian command.
[00:45:37.640 - 00:45:40.640] And it does a degree to radians conversion.
[00:45:40.640 - 00:45:46.300] These seem to be matrix as something we just derived by hand.
[00:45:46.300 - 00:45:49.300] So we're just going through the process of generating that.
[00:45:49.300 - 00:45:54.300] Then we use this multiplication to get the KG terms.
[00:45:54.300 - 00:46:04.000] We go through on this page, we get our overall KG.
[00:46:04.000 - 00:46:08.000] And the whole point of this is to give you that play by play, the numerical results.
[00:46:08.000 - 00:46:09.000] You can skip forward.
[00:46:09.000 - 00:46:16.620] You can check the given result of every step and follow through the process.
[00:46:16.620 - 00:46:20.620] So we have this NP dot that alpha dot solve commands to get the deflections.
[00:46:20.620 - 00:46:41.160] When we're interpreting this, refer back to the free body diagrams, the FBT on page, pages 4950.
[00:46:41.160 - 00:46:52.150] It's a two-interpret key thing of the lab.
[00:46:52.150 - 00:46:58.150] It's not just producing the numbers, but also thinking through the physical significance of what you don't.
[00:46:58.150 - 00:47:02.150] Defection vectors have just gone through that and strained values.
[00:47:02.150 - 00:47:05.150] And then the forcing terms here.
[00:47:05.150 - 00:47:09.150] Now, it gives a plotting the final shape.
[00:47:09.150 - 00:47:20.010] So this week, because we're doing axial bars and not only carrying axial bars,
[00:47:20.010 - 00:47:24.010] there's no need to be no curvature in them, we can just draw straight lines between the initial
[00:47:24.010 - 00:47:28.010] motor point and the final motor point.
[00:47:28.010 - 00:47:31.010] So first thing we need to just define a coordinate origin.
[00:47:31.010 - 00:47:38.290] So if it was xg and yg down here, so that's the origin of our coordinate system.
[00:47:38.290 - 00:47:40.290] Hopefully, you see the right answer.
[00:47:40.290 - 00:47:42.290] That's an answer.
[00:47:42.290 - 00:47:47.290] Probably the most intuitive one and that goes zero, zero at the bottom of the thank corner.
[00:47:47.290 - 00:47:49.290] Then we have here we have x and y coordinates.
[00:47:49.290 - 00:47:54.290] So the x-coordinate is going to be zero and the y-coordinate is going to be 10.
[00:47:54.290 - 00:48:02.530] And in this corner, the unaffected is going to be equal to 10, 10.
[00:48:02.530 - 00:48:07.960] So x of 10 and y of 10.
[00:48:07.960 - 00:48:14.960] So this shouldn't be too hard to plot the baseline values.
[00:48:14.960 - 00:48:17.960] Then what we want to know is, well, what's the new position of this neural point?
[00:48:17.960 - 00:48:27.180] Well, this here, the deflected position is actually going to be 10,
[00:48:27.180 - 00:48:31.180] which was the initial x position, plus q1.
[00:48:31.180 - 00:48:35.180] So the first q value that we've solved for is the horizontal deflection.
[00:48:35.180 - 00:48:38.180] So that's going to be the solved, the neural deflection.
[00:48:38.180 - 00:48:40.180] That's the new node, the neural position.
[00:48:40.180 - 00:48:44.180] And then we have 10 plus q2 will be the y position.
[00:48:44.180 - 00:48:52.740] Now, generally plotting things at true scale isn't that interesting.
[00:48:52.740 - 00:48:58.740] So a good thing here is to define some magnification factor.
[00:48:58.740 - 00:49:12.720] So you might say something like this underscore mag,
[00:49:12.720 - 00:49:14.720] and maybe maybe at a value of 100.
[00:49:14.720 - 00:49:20.470] So you just amplify it and it starts 100.
[00:49:20.470 - 00:49:51.780] So then the exaggerated deflected position, 10 plus this mag times q1 and 10 plus this mag times q2.
[00:49:51.780 - 00:49:54.780] That's the amplified version.
[00:49:54.780 - 00:49:58.780] Generally true scale is not visible or useful.
[00:49:58.780 - 00:50:11.220] And just real quickly, n-python, this will be xe.plot.
[00:50:11.220 - 00:50:25.700] And it has x1, x2, and y1, comma, y2, as the wave plotting map.
[00:50:25.700 - 00:50:34.700] So, for example, the first one would be, say, xe is dot plot.
[00:50:34.700 - 00:50:41.300] And that these would be zero, ten, ten.
[00:50:41.300 - 00:50:45.300] So it would be the under-fic position of 0, 1.
[00:50:45.300 - 00:50:57.620] And then we'd have label is equal to undeflicted element 1.
[00:50:57.620 - 00:51:05.040] So one thing is to want to make you aware of there.
[00:51:05.040 - 00:51:10.040] The way we always draw coordinates, as we label them like x, y, x, y, x, y around the diagram.
[00:51:10.040 - 00:51:14.040] But then when we plot them, we actually group the x's together and the y's together.
[00:51:14.040 - 00:51:16.040] So I warn you now this is a thought trap.
[00:51:16.040 - 00:51:19.040] It's something that I do all the time, and I'm sure some of you will do this afternoon.
[00:51:19.040 - 00:51:22.040] It's thinking about this as an x, y, here.
[00:51:22.040 - 00:51:28.040] We actually, it's the x's group together and the y's group together, which differs from the way that this is shown on the diagram.
[00:51:28.040 - 00:51:30.040] So let me just do it where at that point.
[00:51:30.040 - 00:51:32.040] Otherwise that's the key thing.
[00:51:32.040 - 00:51:38.040] And I have said that in email with the additional worksheet, links, and some other work that I have sat on there.
[00:51:38.040 - 00:51:40.040] So thank you all for coming.
[00:51:40.040 - 00:52:06.080] And I'll see you at the start of the note.
[00:52:06.080 - 00:52:09.080] Probably don't look at it.
[00:52:09.080 - 00:52:14.080] I've got a map of sat on it and stuff that needs an open.
[00:52:14.080 - 00:52:42.810] I've got some...
[00:52:42.810 - 00:52:44.810] Is that some come sticks or...?
[00:52:44.810 - 00:52:46.810] Oh, do you not recognize that with this one?
[00:52:46.810 - 00:52:48.810] I can see the stuff.
[00:52:48.810 - 00:52:52.810] I've got to carry them on my bicycle, so I'm starting to preserve the chips.
[00:52:52.810 - 00:52:55.810] I guess it's something where, like, I was thinking we're doing it three days.
[00:52:55.810 - 00:52:57.810] There's nothing like just using three days.
[00:52:57.810 - 00:52:59.810] Absolutely. Yes. No, it's great.
[00:52:59.810 - 00:53:02.810] I'm also thinking once that I was trying to draw...
[00:53:02.810 - 00:53:05.810] There was a... East TL file, which is a geometry file.
[00:53:05.810 - 00:53:07.810] It's sort of...
[00:53:07.810 - 00:53:08.810] Cute.
[00:53:08.810 - 00:53:10.810] Like triangle, that's too close.
[00:53:10.810 - 00:53:11.810] And they trace.
[00:53:11.810 - 00:53:13.810] Then I'm trying to map with the coordinate system.
[00:53:13.810 - 00:53:14.810] Because it's just...
[00:53:14.810 - 00:53:15.810] Do you have one?
[00:53:15.810 - 00:53:17.810] I went and got a block of wood.
[00:53:17.810 - 00:53:18.810] Yeah.
[00:53:18.810 - 00:53:19.810] Absolutely.
[00:53:19.810 - 00:53:20.810] So much.
[00:53:20.810 - 00:53:21.810] All right.
[00:53:21.810 - 00:53:23.810] We'll see you, Joe.
[00:53:23.810 - 00:53:24.810] Good luck.
[00:53:24.810 - 00:53:26.810] See you at what you've got for us, too.
[00:53:26.810 - 00:53:27.810] One, one, eight.
[00:53:27.810 - 00:53:28.810] Yeah.
[00:53:28.810 - 00:53:29.810] So...
[00:53:29.810 - 00:53:30.810] It's a future student trust.
[00:53:30.810 - 00:53:31.810] Lovely student.
[00:53:31.810 - 00:53:51.180] Yeah.
[00:53:51.180 - 00:54:02.710] I'm going to give you some people to come to me.
[00:54:02.710 - 00:54:03.710] Because my legs get crushed.
[00:54:03.710 - 00:54:04.710] Yeah.
[00:54:04.710 - 00:54:07.710] I like the model.
[00:54:07.710 - 00:54:08.710] I like the model.
[00:54:08.710 - 00:54:18.140] I only have very much more than I did.
[00:54:18.140 - 00:54:23.140] I think I'm going to work for you.
[00:54:23.140 - 00:54:41.390] Thank you.
[00:54:41.390 - 00:54:42.390] Thank you.
[00:54:42.390 - 00:54:43.390] Thank you.
[00:54:43.390 - 00:54:52.300] Thank you.
[00:54:52.300 - 00:54:53.300] Thank you.
[00:54:53.300 - 00:54:54.300] Thank you.
[00:54:54.300 - 00:54:56.300] I'm going to do more.
[00:54:56.300 - 00:54:57.300] Thank you very much.
[00:54:57.300 - 00:54:58.300] Thank you.
[00:54:58.300 - 00:54:59.300] Thank you.
[00:54:59.300 - 00:55:00.300] Thank you.
[00:55:00.300 - 00:55:01.300] We'll get started.
[00:55:01.300 - 00:55:02.300] We'll get started.
[00:55:02.300 - 00:55:03.300] Alright.
[00:55:03.300 - 00:55:04.300] Alright.
[00:55:04.300 - 00:55:05.300] Thanks, guys.
[00:55:05.300 - 00:55:06.300] Thank you.
[00:55:06.300 - 00:55:07.300] Bye.

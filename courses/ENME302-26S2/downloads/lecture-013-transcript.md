# ENME302-26S2 Lecture 13 native Echo transcript

Date: August 3, 2026 12:00pm-12:55pm
Transcript type: native Echo automated transcript.

[00:00:31:059 - 00:00:31:069] **Speaker 0:** It.
[00:00:38:909 - 00:00:39:860] **Speaker 1:** Well, Karakoto.
[00:00:41:380 - 00:00:42:229] **Speaker 1:** Welcome along, everyone.
[00:00:44:430 - 00:00:46:029] **Speaker 1:** So hopefully you can hear me OK in the back.
[00:00:47:599 - 00:00:48:549] **Speaker 1:** Can you hear me at the back?
[00:00:48:689 - 00:00:51:049] **Speaker 1:** I'm not sure there's too much more I can do
[00:00:51:430 - 00:00:54:029] **Speaker 1:** if you can't, but um so what we're gonna do
[00:00:54:029 - 00:00:57:049] **Speaker 1:** this week is throughout all the derivations to this point,
[00:00:57:669 - 00:01:00:130] **Speaker 1:** we've gone through and we've derived things and we've said
[00:01:01:009 - 00:01:05:510] **Speaker 1:** that the internal axial load distribution for axial bars and
[00:01:05:510 - 00:01:10:120] **Speaker 1:** the distributed she load through beam element was zero.
[00:01:10:589 - 00:01:13:019] **Speaker 1:** And that was a simplifying assumption that we made and
[00:01:13:870 - 00:01:15:220] **Speaker 1:** I made the promise to you at the time that
[00:01:15:220 - 00:01:17:029] **Speaker 1:** we would come back and we would readdress that before
[00:01:17:029 - 00:01:18:129] **Speaker 1:** these 4 weeks were up.
[00:01:18:510 - 00:01:20:910] **Speaker 1:** And essentially today is my day to make good on
[00:01:20:910 - 00:01:21:589] **Speaker 1:** that promise.
[00:01:22:489 - 00:01:25:489] **Speaker 1:** So there's essentially two things we could do here is
[00:01:25:489 - 00:01:28:089] **Speaker 1:** one, we could go back through all the derivations, and
[00:01:28:089 - 00:01:30:489] **Speaker 1:** we could drive a new element type that does include
[00:01:30:489 - 00:01:31:349] **Speaker 1:** distributed loading.
[00:01:35:970 - 00:01:37:760] **Speaker 1:** Uh, I'll see what I can do here.
[00:01:41:629 - 00:01:43:790] **Speaker 0:** Um, Is that any better?
[00:01:44:690 - 00:01:47:330] **Speaker 1:** See if that I'm trying this one seems to come
[00:01:47:330 - 00:01:48:650] **Speaker 1:** through a bit, so I'll try and.
[00:01:49:580 - 00:01:51:750] **Speaker 1:** So there's essentially two options that are available to us.
[00:01:51:949 - 00:01:56:819] **Speaker 1:** And one of them is to distribute to derive a
[00:01:56:819 - 00:01:59:550] **Speaker 1:** new element type and the element type embedded in that
[00:01:59:550 - 00:02:02:169] **Speaker 1:** derivation is the presence of a distributed load.
[00:02:02:790 - 00:02:05:150] **Speaker 1:** So if we were to take that approach, we would
[00:02:05:150 - 00:02:07:790] **Speaker 1:** then have another element type and the element type would
[00:02:07:790 - 00:02:09:500] **Speaker 1:** be specific to that distributed load.
[00:02:09:589 - 00:02:12:660] **Speaker 1:** So then we'd have multiple, you know, the frame elements,
[00:02:12:990 - 00:02:16:149] **Speaker 1:** one with distributed load, one without, and the one with
[00:02:16:199 - 00:02:19:860] **Speaker 1:** Distributed load would still be specific to a particular profile
[00:02:19:860 - 00:02:21:080] **Speaker 1:** of distributed load.
[00:02:21:320 - 00:02:24:839] **Speaker 1:** So that is certainly an avenue available to us, but
[00:02:24:839 - 00:02:27:440] **Speaker 1:** it's not really a desirable one, because we'd end up
[00:02:27:440 - 00:02:28:350] **Speaker 1:** with all these different elements.
[00:02:28:399 - 00:02:31:639] **Speaker 1:** We have all these different stiffness matrices, like what I
[00:02:31:639 - 00:02:33:279] **Speaker 1:** said to you last week was when you coded this
[00:02:33:279 - 00:02:35:119] **Speaker 1:** up, and you had the 6 x 6 for the
[00:02:35:119 - 00:02:37:389] **Speaker 1:** frame element that you would have to type that in,
[00:02:37:559 - 00:02:39:119] **Speaker 1:** but you didn't only ever have to do it once.
[00:02:39:399 - 00:02:41:320] **Speaker 1:** So if we were to go through a bunch of
[00:02:41:320 - 00:02:45:369] **Speaker 1:** new more derivations, We would then end up having to
[00:02:45:369 - 00:02:46:839] **Speaker 1:** code up all the different element types.
[00:02:47:089 - 00:02:50:929] **Speaker 1:** So instead, the approach we're going to take is, at
[00:02:50:929 - 00:02:53:169] **Speaker 1:** the moment, what we do have is elements that don't
[00:02:53:169 - 00:02:54:679] **Speaker 1:** carry distributed loads.
[00:02:55:000 - 00:02:59:429] **Speaker 1:** And we have a method in an uppercase Q of
[00:02:59:479 - 00:03:01:869] **Speaker 1:** introducing applied external loads.
[00:03:02:809 - 00:03:05:949] **Speaker 1:** So what we We're going to do there is look
[00:03:05:949 - 00:03:08:910] **Speaker 1:** at a way, use the same principles that we've done
[00:03:08:910 - 00:03:12:229] **Speaker 1:** for derivations, but instead of driving your element type, we're
[00:03:12:229 - 00:03:14:679] **Speaker 1:** going to look at ways of taking those distributed loads
[00:03:14:990 - 00:03:17:630] **Speaker 1:** and lumping those into nodal loads, which we already know
[00:03:17:630 - 00:03:18:289] **Speaker 1:** how to model.
[00:03:19:100 - 00:03:21:869] **Speaker 1:** Um, in a way that they represent the distributed load.
[00:03:23:070 - 00:03:24:910] **Speaker 1:** So that's the the ultimate basis here.
[00:03:24:990 - 00:03:27:339] **Speaker 1:** So we've got say it could be an aircraft wing,
[00:03:27:369 - 00:03:30:910] **Speaker 1:** it could be say, self weight or some sort of
[00:03:30:910 - 00:03:31:850] **Speaker 1:** structure like this.
[00:03:32:270 - 00:03:35:270] **Speaker 1:** But what we want to do is take a true
[00:03:35:270 - 00:03:38:270] **Speaker 1:** case of a distributed load and work out how to
[00:03:38:270 - 00:03:42:229] **Speaker 1:** lump that together and apply that directly at the no
[00:03:42:229 - 00:03:46:009] **Speaker 1:** points because then at that point, that will match everything
[00:03:46:149 - 00:03:50:509] **Speaker 1:** that is based upon our existing element derivation.
[00:03:50:710 - 00:03:53:320] **Speaker 1:** So This is the concept of equivalent node loading.
[00:03:53:740 - 00:03:56:820] **Speaker 1:** Um, distributed loads are lumped and applied directly at nodal
[00:03:56:820 - 00:04:00:919] **Speaker 1:** points to approximate deflections that occurred, uh, from the actual
[00:04:01:279 - 00:04:01:970] **Speaker 1:** distributed loads.
[00:04:02:020 - 00:04:05:020] **Speaker 1:** We need to develop a mathematical framework to know what
[00:04:05:020 - 00:04:06:199] **Speaker 1:** nodal loads to apply.
[00:04:08:320 - 00:04:11:320] **Speaker 1:** So much like when you've done a little bit and
[00:04:11:320 - 00:04:14:440] **Speaker 1:** dynamics last year, often you have sort of this lumped
[00:04:14:440 - 00:04:16:579] **Speaker 1:** mass model for a multi-degree freedom system.
[00:04:17:118 - 00:04:17:928] **Speaker 1:** It's kind of the same thing.
[00:04:17:959 - 00:04:19:558] **Speaker 1:** We're taking them and we're putting them at the degrees
[00:04:19:558 - 00:04:21:880] **Speaker 1:** of freedom, because that's how we know how to model
[00:04:21:880 - 00:04:25:239] **Speaker 1:** them without having to have multiple element types for every
[00:04:25:239 - 00:04:26:720] **Speaker 1:** possible distributed load.
[00:04:30:809 - 00:04:34:649] **Speaker 1:** So the first slide here is to just revisit some
[00:04:34:649 - 00:04:36:290] **Speaker 1:** of our derivation.
[00:04:37:670 - 00:04:41:070] **Speaker 1:** So when we initially derived this, this was the equation.
[00:04:41:149 - 00:04:45:220] **Speaker 1:** So EI times the 2nd derivative of transverse deflection with
[00:04:45:220 - 00:04:47:420] **Speaker 1:** respect to X is by definition moment.
[00:04:47:510 - 00:04:49:609] **Speaker 1:** So this this embedded in here is the moment curvature
[00:04:49:609 - 00:04:52:149] **Speaker 1:** equation, where everything is equal to the moment and the
[00:04:52:149 - 00:04:54:670] **Speaker 1:** second derivative of that being equal to zero.
[00:04:57:429 - 00:05:09:959] **Speaker 1:** So when we initially did this, In this equation, We
[00:05:09:959 - 00:05:13:989] **Speaker 1:** sit The right-hand side, the RHS sector.
[00:05:17:839 - 00:05:18:690] **Speaker 1:** To 0.
[00:05:19:059 - 00:05:22:260] **Speaker 1:** And when we initially assumed that there was no, no
[00:05:22:260 - 00:05:25:200] **Speaker 1:** presence of any distributed loads within that element.
[00:05:26:799 - 00:05:28:480] **Speaker 1:** This is really just a recap of what we've already
[00:05:28:480 - 00:05:30:359] **Speaker 1:** done, because this is really important for what we're going
[00:05:30:359 - 00:05:31:019] **Speaker 1:** to do next.
[00:05:32:459 - 00:05:34:790] **Speaker 1:** So our transverse fiction vix anyone that did the plotting
[00:05:34:790 - 00:05:37:709] **Speaker 1:** code last week will be hopefully quite familiar with us
[00:05:37:709 - 00:05:39:450] **Speaker 1:** shape functions times out of fiction vector.
[00:05:41:040 - 00:05:45:320] **Speaker 1:** This here, of course, is in the beam element formulation.
[00:05:45:640 - 00:05:47:959] **Speaker 1:** And then these were our four shape functions that resulted
[00:05:47:959 - 00:05:48:500] **Speaker 1:** from that.
[00:05:49:119 - 00:05:55:679] **Speaker 1:** We had our equation for our stiffness matrix symbolically, and
[00:05:55:679 - 00:05:58:640] **Speaker 1:** then this is what we went through and complete all
[00:05:58:640 - 00:05:59:239] **Speaker 1:** those processes.
[00:05:59:320 - 00:06:01:700] **Speaker 1:** This is the actual matrix that we obtained.
[00:06:04:320 - 00:06:06:339] **Speaker 1:** So the key steps, two key steps there was the
[00:06:06:339 - 00:06:08:380] **Speaker 1:** first thing is we set the right hand side to
[00:06:08:380 - 00:06:10:790] **Speaker 1:** 0 and we assumed all the distributed loads were 0.
[00:06:11:140 - 00:06:16:359] **Speaker 1:** And then the integral term Here is the internal virtual
[00:06:16:359 - 00:06:18:220] **Speaker 1:** work integrated over the length of the element.
[00:06:18:480 - 00:06:20:160] **Speaker 1:** So what we're going to do is going to revisit
[00:06:20:160 - 00:06:21:079] **Speaker 1:** the derivation approach.
[00:06:21:160 - 00:06:22:720] **Speaker 1:** We're not going to redo the derivations, but we're going
[00:06:22:720 - 00:06:24:350] **Speaker 1:** to build upon that and use the same sort of
[00:06:24:350 - 00:06:27:320] **Speaker 1:** principles to look at the loading side of the equation
[00:06:27:320 - 00:06:31:279] **Speaker 1:** and what we can do there to introduce the distributed
[00:06:31:279 - 00:06:31:899] **Speaker 1:** loads.
[00:06:35:730 - 00:06:39:529] **Speaker 1:** So The one we initially used was the principle of
[00:06:39:529 - 00:06:40:570] **Speaker 1:** virtual displacements.
[00:06:40:940 - 00:06:42:649] **Speaker 1:** Now the right-hand side is no longer zero.
[00:06:43:399 - 00:06:47:679] **Speaker 1:** So we're no longer assuming that the distributed intensity distributed
[00:06:47:679 - 00:06:48:609] **Speaker 1:** share load intensity is 0.
[00:06:48:690 - 00:06:50:589] **Speaker 1:** We're actually going to put a non-zero value in here.
[00:06:51:170 - 00:06:53:470] **Speaker 1:** And we're going to work through this kind of symbolically
[00:06:53:470 - 00:06:55:239] **Speaker 1:** initially, and then we're going to start looking at some
[00:06:55:239 - 00:06:57:630] **Speaker 1:** specific values of WX.
[00:06:57:970 - 00:07:02:130] **Speaker 1:** Now, WX could be damn near anything infinite number of
[00:07:02:130 - 00:07:02:980] **Speaker 1:** things this could be.
[00:07:03:549 - 00:07:07:230] **Speaker 1:** But only a small number actually have common engineering significance.
[00:07:07:390 - 00:07:09:269] **Speaker 1:** So we'll work through the common ones and that will
[00:07:09:269 - 00:07:10:529] **Speaker 1:** cover pretty much everything we need.
[00:07:11:929 - 00:07:14:089] **Speaker 1:** So we've got our equation here, no longer with the
[00:07:14:089 - 00:07:14:730] **Speaker 1:** right-hand side here.
[00:07:14:790 - 00:07:15:929] **Speaker 1:** We've now got WXX.
[00:07:16:489 - 00:07:20:170] **Speaker 1:** We're putting a little virtual transverse deflection Delta be in
[00:07:20:170 - 00:07:20:549] **Speaker 1:** there.
[00:07:21:820 - 00:07:23:940] **Speaker 1:** Um, we integrate.
[00:07:24:820 - 00:07:25:589] **Speaker 1:** Along the elements.
[00:07:25:859 - 00:07:28:190] **Speaker 1:** So we're using the wig form here we're integrating across
[00:07:28:190 - 00:07:28:649] **Speaker 1:** an element.
[00:07:30:890 - 00:07:32:369] **Speaker 1:** And this WFX.
[00:07:34:279 - 00:07:36:250] **Speaker 1:** Is some.
[00:07:38:410 - 00:07:43:010] **Speaker 1:** Some As yet undefined.
[00:07:48:700 - 00:07:52:510] **Speaker 1:** Function Of distributed.
[00:07:57:910 - 00:08:01:230] **Speaker 1:** Sheer load Intensity.
[00:08:06:070 - 00:08:13:950] **Speaker 1:** Along the element So we haven't yet defined what that
[00:08:13:950 - 00:08:14:109] **Speaker 1:** is.
[00:08:14:179 - 00:08:16:130] **Speaker 1:** And as I said, it's pretty much an infinite number
[00:08:16:130 - 00:08:18:850] **Speaker 1:** of possibilities, but only a limited number of of meaningful
[00:08:19:390 - 00:08:20:010] **Speaker 1:** significance.
[00:08:22:600 - 00:08:24:880] **Speaker 1:** You know, the right-hand side can be modified.
[00:08:24:959 - 00:08:26:540] **Speaker 1:** We're gonna introduce this relationship.
[00:08:27:350 - 00:08:31:190] **Speaker 1:** Which is applying essentially the shape function equation in an
[00:08:31:190 - 00:08:32:250] **Speaker 1:** incremental sense.
[00:08:33:309 - 00:08:35:950] **Speaker 1:** We end up with this integration here.
[00:08:36:150 - 00:08:39:390] **Speaker 1:** So this is the um the left-hand side.
[00:08:39:469 - 00:08:40:750] **Speaker 1:** We've now got the right hand side, we've got a
[00:08:40:750 - 00:08:42:229] **Speaker 1:** W of X and we've got this integral.
[00:08:43:330 - 00:08:46:119] **Speaker 1:** Uh, we're gonna integrate by parts like we did previously.
[00:08:46:450 - 00:08:49:369] **Speaker 1:** Um, we're going to substitute in our boundary conditions.
[00:08:49:659 - 00:08:54:020] **Speaker 1:** So this is an F1, F2 and F3, F4.
[00:08:54:840 - 00:08:57:909] **Speaker 1:** It's just But actually spell substituting.
[00:08:59:049 - 00:09:00:130] **Speaker 1:** Substituting.
[00:09:01:679 - 00:09:03:179] **Speaker 1:** In boundary conditions.
[00:09:13:479 - 00:09:16:479] **Speaker 1:** And once we we can essentially group terms and get
[00:09:16:479 - 00:09:17:539] **Speaker 1:** to this equation here.
[00:09:18:679 - 00:09:21:640] **Speaker 1:** Now, this piece of the equation, that's the bit we've
[00:09:21:640 - 00:09:22:239] **Speaker 1:** seen before.
[00:09:22:559 - 00:09:25:799] **Speaker 1:** So that's the essentially everything in the bracket of term
[00:09:25:799 - 00:09:25:919] **Speaker 1:** there.
[00:09:26:000 - 00:09:28:059] **Speaker 1:** So maybe just extend that up a little bit.
[00:09:28:119 - 00:09:30:380] **Speaker 1:** So everything essentially up.
[00:09:31:849 - 00:09:35:210] **Speaker 1:** Through here, just to make the distinction that DE is
[00:09:35:210 - 00:09:35:549] **Speaker 1:** outside there.
[00:09:35:690 - 00:09:38:390] **Speaker 1:** So that's the, the KE.
[00:09:39:500 - 00:09:39:900] **Speaker 1:** Times.
[00:09:40:099 - 00:09:42:000] **Speaker 1:** So that's the total equation that exists there.
[00:09:42:780 - 00:09:45:299] **Speaker 1:** Um, and then the applied forcing terms.
[00:09:45:780 - 00:09:47:940] **Speaker 1:** And if I was to just essentially cover up this
[00:09:47:940 - 00:09:48:479] **Speaker 1:** space here.
[00:09:50:919 - 00:09:53:320] **Speaker 1:** Then this equation looks pretty much like what we've seen
[00:09:53:320 - 00:09:53:500] **Speaker 1:** before.
[00:09:54:140 - 00:09:57:380] **Speaker 1:** KA times D minus FE is equal to 0 or
[00:09:57:400 - 00:10:00:210] **Speaker 1:** KA times DE is equally the external forces.
[00:10:01:080 - 00:10:02:679] **Speaker 1:** There's now this extra piece.
[00:10:03:000 - 00:10:05:080] **Speaker 1:** So this is the equivalent nodal forces.
[00:10:05:159 - 00:10:06:380] **Speaker 1:** So this is we could take.
[00:10:07:239 - 00:10:10:380] **Speaker 1:** Some distributed load along the length of the elements.
[00:10:10:840 - 00:10:12:200] **Speaker 1:** We haven't yet defined what that is.
[00:10:12:520 - 00:10:14:479] **Speaker 1:** We can do the math and then we can basically
[00:10:14:479 - 00:10:17:000] **Speaker 1:** say, what are the loads that could be lumped and
[00:10:17:000 - 00:10:21:140] **Speaker 1:** applied at the nodal point that would approximate and model
[00:10:21:520 - 00:10:23:229] **Speaker 1:** this W X.
[00:10:27:549 - 00:10:32:049] **Speaker 1:** So that's what Essentially this piece here is, is that's
[00:10:32:049 - 00:10:34:590] **Speaker 1:** all the distributed loading effects.
[00:10:41:549 - 00:10:44:869] **Speaker 1:** So now, essentially we've got an equation looks very similar
[00:10:44:869 - 00:10:45:770] **Speaker 1:** to what we had previously.
[00:10:46:530 - 00:10:48:719] **Speaker 1:** But now we also have this.
[00:10:49:640 - 00:10:57:960] **Speaker 1:** Um Let's So we've got the, hopefully they'll be a
[00:10:57:960 - 00:10:58:799] **Speaker 1:** bit clearer.
[00:11:02:080 - 00:11:02:799] **Speaker 1:** Too much feedback.
[00:11:07:450 - 00:11:08:690] **Speaker 1:** Sorry, bear with me for a second here.
[00:11:12:250 - 00:11:14:130] **Speaker 1:** OK, um.
[00:11:16:320 - 00:11:18:099] **Speaker 1:** Just gonna pull this back a little bit.
[00:11:19:760 - 00:11:23:619] **Speaker 1:** So what we've got here is we have our um
[00:11:25:049 - 00:11:26:739] **Speaker 1:** If we were to cover this piece up, it looks
[00:11:26:739 - 00:11:28:390] **Speaker 1:** exactly like the equation we've seen before.
[00:11:29:140 - 00:11:30:869] **Speaker 1:** And this bit here.
[00:11:32:619 - 00:11:39:630] **Speaker 1:** Is the bumped Nodal forces.
[00:11:42:950 - 00:11:50:210] **Speaker 1:** That represent Some Distributed load.
[00:11:55:510 - 00:11:57:049] **Speaker 1:** So that's the F equivalent.
[00:11:58:299 - 00:11:59:809] **Speaker 1:** And this is the equation here.
[00:12:00:059 - 00:12:02:200] **Speaker 1:** Just taking this, looking at the equation above.
[00:12:02:549 - 00:12:06:049] **Speaker 1:** This is the piece that defines how to take uh
[00:12:06:049 - 00:12:08:340] **Speaker 1:** within an element, there's some sort of distributed load that
[00:12:08:340 - 00:12:09:200] **Speaker 1:** exists along it.
[00:12:09:739 - 00:12:11:940] **Speaker 1:** This is how we take that um and end up
[00:12:11:940 - 00:12:13:780] **Speaker 1:** with a lowercase FEQ.
[00:12:14:719 - 00:12:17:520] **Speaker 1:** And so this is the equivalent forcing vector for a
[00:12:17:520 - 00:12:18:340] **Speaker 1:** given element.
[00:12:19:729 - 00:12:21:450] **Speaker 1:** That represents the distributed load.
[00:12:24:590 - 00:12:26:590] **Speaker 1:** It's not important to note, we come about this a
[00:12:26:590 - 00:12:27:229] **Speaker 1:** little bit differently.
[00:12:27:349 - 00:12:28:950] **Speaker 1:** When we were doing this previously, we end up with
[00:12:28:950 - 00:12:31:909] **Speaker 1:** the uppercase Q immediately and we put that straight into
[00:12:31:909 - 00:12:32:609] **Speaker 1:** the equation.
[00:12:33:109 - 00:12:35:030] **Speaker 1:** When we're doing with distributed loads, we actually end up
[00:12:35:030 - 00:12:36:609] **Speaker 1:** with a lowercase at first.
[00:12:37:630 - 00:12:39:789] **Speaker 1:** Then we have to transform that into an uppercase F
[00:12:39:950 - 00:12:42:830] **Speaker 1:** and then use, uh, using our transformation matrix.
[00:12:43:150 - 00:12:45:109] **Speaker 1:** And then we use our assembly matrix to go from
[00:12:45:109 - 00:12:46:989] **Speaker 1:** our lowercase f to our uppercase F.
[00:12:47:150 - 00:12:49:460] **Speaker 1:** And then once we've done that, then we use this,
[00:12:49:469 - 00:12:52:510] **Speaker 1:** um, so the transformation matrix from our lowercase f to
[00:12:52:510 - 00:12:53:330] **Speaker 1:** our uppercase F.
[00:12:53:659 - 00:12:55:630] **Speaker 1:** And then the assembly matrix to build that into an
[00:12:55:630 - 00:12:58:210] **Speaker 1:** uppercase Q vector, which we'll work through some examples.
[00:13:01:380 - 00:13:05:690] **Speaker 1:** So from that This is where we have our transformation
[00:13:05:690 - 00:13:06:429] **Speaker 1:** matrix.
[00:13:07:169 - 00:13:09:109] **Speaker 1:** Then we have our assembly matrix here.
[00:13:09:489 - 00:13:12:530] **Speaker 1:** And this is the equivalent forcing terms Q equivalent.
[00:13:12:969 - 00:13:15:250] **Speaker 1:** That is how we introduce that into the overall system.
[00:13:15:409 - 00:13:17:349] **Speaker 1:** So a couple of steps there.
[00:13:18:539 - 00:13:20:919] **Speaker 1:** Um, and if there are multiple elements.
[00:13:21:929 - 00:13:26:890] **Speaker 1:** And they maybe multiple applied external loads exist on them,
[00:13:27:270 - 00:13:29:070] **Speaker 1:** we can just sum up like this.
[00:13:30:989 - 00:13:33:150] **Speaker 1:** And then once we go to the structural level equation,
[00:13:33:400 - 00:13:34:750] **Speaker 1:** we end up with this here.
[00:13:34:830 - 00:13:37:270] **Speaker 1:** So uh the same cuvector we've always used here.
[00:13:37:429 - 00:13:40:630] **Speaker 1:** So if we just essentially covered up um this piece
[00:13:40:630 - 00:13:41:090] **Speaker 1:** here.
[00:13:42:650 - 00:13:46:630] **Speaker 1:** Then everything else in that equation looks like the equation
[00:13:46:630 - 00:13:47:640] **Speaker 1:** we've always solved.
[00:13:48:130 - 00:13:50:489] **Speaker 1:** We now just have an extra piece on the the
[00:13:50:489 - 00:13:51:570] **Speaker 1:** load side of the equation.
[00:13:51:690 - 00:13:54:090] **Speaker 1:** So the what was just Q is now this total
[00:13:54:090 - 00:13:57:849] **Speaker 1:** bracketed term on the, um, which is the the values
[00:13:57:849 - 00:13:58:609] **Speaker 1:** we're solving for.
[00:13:59:489 - 00:14:02:210] **Speaker 1:** So solving for the lowercase q based upon these input
[00:14:02:210 - 00:14:02:729] **Speaker 1:** values.
[00:14:03:820 - 00:14:07:659] **Speaker 1:** So mathematically, um, we now have a method of incorporating
[00:14:07:659 - 00:14:10:159] **Speaker 1:** distributed loads into our system of equations.
[00:14:10:659 - 00:14:13:520] **Speaker 1:** Uh, everything else is just as it was before.
[00:14:13:770 - 00:14:16:500] **Speaker 1:** So we've we've relaxed that assumption, but we're not throwing
[00:14:16:500 - 00:14:18:580] **Speaker 1:** away anything we've done the last three weeks.
[00:14:18:739 - 00:14:19:919] **Speaker 1:** That is all still valid.
[00:14:20:580 - 00:14:22:760] **Speaker 1:** Um, we only use the basic 4 degree of freedom
[00:14:22:760 - 00:14:25:919] **Speaker 1:** frame element, so only 4 degree frame beam element here.
[00:14:26:359 - 00:14:30:380] **Speaker 1:** With the simplified 4x4 K matrix from pages 74 and
[00:14:30:380 - 00:14:34:190] **Speaker 1:** 75, not the full 6 degree of freedom, 6 degree
[00:14:34:190 - 00:14:35:080] **Speaker 1:** of freedom frame element.
[00:14:35:280 - 00:14:37:280] **Speaker 1:** Now, the only difference there is we just need to
[00:14:37:280 - 00:14:39:700] **Speaker 1:** add in the axial components.
[00:14:41:390 - 00:14:42:960] **Speaker 1:** So that's due to the fact that the distributed sheer
[00:14:42:960 - 00:14:46:500] **Speaker 1:** load um affects flexual o os only and not the
[00:14:47:000 - 00:14:48:510] **Speaker 1:** um axial loads.
[00:14:48:520 - 00:14:51:099] **Speaker 1:** And if you remember when we first arrived, this where
[00:14:51:919 - 00:14:54:119] **Speaker 1:** our system isn't assuming any coupling.
[00:14:54:239 - 00:14:57:200] **Speaker 1:** It's a bit independently solving the axial deflections and the
[00:14:57:200 - 00:15:01:369] **Speaker 1:** transverse deflections within the system and it's not um capturing
[00:15:01:369 - 00:15:02:419] **Speaker 1:** the coupling between that.
[00:15:04:340 - 00:15:07:520] **Speaker 1:** So, so far, what we haven't done is determine any
[00:15:07:520 - 00:15:09:929] **Speaker 1:** specific profile W X.
[00:15:11:200 - 00:15:15:159] **Speaker 1:** So We've just said use this sort of generic variable
[00:15:15:159 - 00:15:15:440] **Speaker 1:** in there.
[00:15:15:479 - 00:15:17:039] **Speaker 1:** So what we're going to do now is start to
[00:15:17:039 - 00:15:18:840] **Speaker 1:** look at some specific values.
[00:15:19:030 - 00:15:21:440] **Speaker 1:** So as I said, you know, this is basically an
[00:15:21:440 - 00:15:23:760] **Speaker 1:** infinite number of possibilities of what WX could be.
[00:15:24:159 - 00:15:27:500] **Speaker 1:** It could be some 7th, 8th, 15th order polynomial.
[00:15:28:359 - 00:15:30:659] **Speaker 1:** But realistically, though, I don't know what the loading case
[00:15:30:659 - 00:15:32:599] **Speaker 1:** in practise would be that would create that.
[00:15:32:880 - 00:15:36:869] **Speaker 1:** So um and most engineering applications, we have something quite
[00:15:36:869 - 00:15:37:419] **Speaker 1:** basic.
[00:15:40:440 - 00:15:43:599] **Speaker 1:** Now, the most basic one we could consider is if
[00:15:43:599 - 00:15:45:580] **Speaker 1:** WX is just some constant.
[00:15:45:869 - 00:15:47:960] **Speaker 1:** So in this case, we're gonna assume that W X
[00:15:47:960 - 00:15:50:880] **Speaker 1:** is just equal to some constant W bar, which is
[00:15:50:880 - 00:15:52:309] **Speaker 1:** a distributed she load intensity.
[00:15:52:359 - 00:15:57:119] **Speaker 1:** So we're gonna say that this is a um Uniformly
[00:15:57:119 - 00:15:59:640] **Speaker 1:** distributed load, often referred to as a UDL.
[00:16:06:409 - 00:16:10:690] **Speaker 1:** So That's the definition there and we've also repeated it
[00:16:10:690 - 00:16:12:070] **Speaker 1:** here that defines that.
[00:16:13:000 - 00:16:15:280] **Speaker 1:** And we're gonna find the equivalent nodal forcing term that
[00:16:15:280 - 00:16:16:400] **Speaker 1:** corresponds to that.
[00:16:16:450 - 00:16:17:780] **Speaker 1:** So what are the, what are the lump if we,
[00:16:18:330 - 00:16:21:289] **Speaker 1:** this is the true load that we currently capture, but
[00:16:21:289 - 00:16:24:090] **Speaker 1:** what is the lumped sheer force and moment that we
[00:16:24:090 - 00:16:27:349] **Speaker 1:** should apply to an element to capture the same behaviour
[00:16:27:349 - 00:16:29:659] **Speaker 1:** that this distributed load would have applied?
[00:16:31:830 - 00:16:33:479] **Speaker 1:** Now, one thing that we're gonna do across all of
[00:16:33:479 - 00:16:36:919] **Speaker 1:** these is we're going to define the UDL to act
[00:16:36:919 - 00:16:38:919] **Speaker 1:** upwards in the positive Y direction.
[00:16:43:989 - 00:16:46:929] **Speaker 1:** So that's just being consistent with our sign convention.
[00:16:47:809 - 00:16:50:039] **Speaker 1:** Now, I'm well aware that in a lot of cases,
[00:16:50:450 - 00:16:51:890] **Speaker 1:** the distributed load will be downwards.
[00:16:51:929 - 00:16:54:530] **Speaker 1:** If it's a horizontal element, gravity acts downwards, as you
[00:16:54:530 - 00:16:54:989] **Speaker 1:** all know.
[00:16:55:409 - 00:16:57:250] **Speaker 1:** So in a lot of cases, W bar might actually
[00:16:57:250 - 00:16:58:210] **Speaker 1:** be a negative number.
[00:16:58:570 - 00:17:03:849] **Speaker 1:** But equally, if we were putting this vertically, it could
[00:17:03:849 - 00:17:04:688] **Speaker 1:** be a wind pressure.
[00:17:05:800 - 00:17:08:390] **Speaker 1:** So when you're looking at the elements on different orientations,
[00:17:08:469 - 00:17:10:188] **Speaker 1:** the key thing is to just remember that the, the
[00:17:10:188 - 00:17:13:349] **Speaker 1:** default assumption is that the distributed load acts in the
[00:17:13:349 - 00:17:14:489] **Speaker 1:** positive Y direction.
[00:17:23:199 - 00:17:27:109] **Speaker 1:** So one thing just here to maybe, uh, elaborate on
[00:17:27:109 - 00:17:29:300] **Speaker 1:** that a little bit, it's a positive wide direction.
[00:17:30:619 - 00:17:34:260] **Speaker 1:** In local or element.
[00:17:36:380 - 00:17:37:329] **Speaker 1:** Coordinates.
[00:17:44:569 - 00:17:45:969] **Speaker 1:** So what we can do now is we've developed this
[00:17:45:969 - 00:17:46:719] **Speaker 1:** equation already.
[00:17:47:150 - 00:17:50:209] **Speaker 1:** Now all we need to do is substitute this equation
[00:17:50:650 - 00:17:51:170] **Speaker 1:** into here.
[00:17:52:069 - 00:17:53:800] **Speaker 1:** And then we get our equation here.
[00:17:53:880 - 00:17:56:900] **Speaker 1:** So uh what was WX is now just W bar.
[00:17:57:239 - 00:18:00:109] **Speaker 1:** Um, we can basically take W bar outside of the
[00:18:00:109 - 00:18:01:900] **Speaker 1:** integral because it is just a constant term.
[00:18:02:709 - 00:18:04:060] **Speaker 1:** So the first thing we need to put is the
[00:18:04:060 - 00:18:07:939] **Speaker 1:** transpose of our vector of um shape functions.
[00:18:08:140 - 00:18:11:260] **Speaker 1:** So the shape functions were the things that defined the
[00:18:11:260 - 00:18:13:239] **Speaker 1:** reaction mechanisms that we could model.
[00:18:14:199 - 00:18:17:939] **Speaker 1:** They also define how to transform distributed loads into lumped
[00:18:17:939 - 00:18:18:890] **Speaker 1:** modal loads.
[00:18:19:630 - 00:18:22:510] **Speaker 1:** This is the vector of those, those little things that
[00:18:22:510 - 00:18:24:229] **Speaker 1:** you coded in if you did the plotting code last
[00:18:24:229 - 00:18:24:410] **Speaker 1:** week.
[00:18:25:099 - 00:18:26:619] **Speaker 1:** So what we need to do is integrate that with
[00:18:26:619 - 00:18:28:849] **Speaker 1:** respect to X and evaluate between 0 and L.
[00:18:29:839 - 00:18:32:060] **Speaker 1:** And you can see here that.
[00:18:33:089 - 00:18:35:790] **Speaker 1:** The W is brought outside the integral because it's constant.
[00:18:36:050 - 00:18:38:729] **Speaker 1:** Um, this, this vector here is the integral of this
[00:18:38:729 - 00:18:40:300] **Speaker 1:** vector here with respect to X.
[00:18:40:729 - 00:18:42:680] **Speaker 1:** And then we need to evaluate that between X equals
[00:18:42:680 - 00:18:43:959] **Speaker 1:** 0 and X equals L.
[00:18:44:369 - 00:18:46:859] **Speaker 1:** When we do that, we end up with these, this
[00:18:46:859 - 00:18:47:650] **Speaker 1:** vector here.
[00:18:51:130 - 00:18:53:930] **Speaker 1:** And just a summary at the bottom here, so.
[00:18:57:369 - 00:19:11:270] **Speaker 1:** These victors Represent Equivalent nodal loads.
[00:19:13:900 - 00:19:15:839] **Speaker 1:** For a UDL.
[00:19:17:560 - 00:19:19:760] **Speaker 1:** In full degree of freedom.
[00:19:22:160 - 00:19:26:329] **Speaker 1:** Be Element notation.
[00:19:28:750 - 00:19:32:979] **Speaker 1:** And that's also um Noted here.
[00:19:33:040 - 00:19:36:260] **Speaker 1:** So the UDL acts upwards in the positive Y direction
[00:19:36:260 - 00:19:38:339] **Speaker 1:** and it's going to be consistent to all the cases
[00:19:38:339 - 00:19:38:920] **Speaker 1:** we consider.
[00:19:40:640 - 00:19:43:030] **Speaker 1:** And also just a reminder, um.
[00:19:44:140 - 00:19:51:949] **Speaker 1:** That is 4 degrees of freedom and We need to
[00:19:51:949 - 00:19:52:709] **Speaker 1:** modify.
[00:19:55:040 - 00:20:06:500] **Speaker 1:** The spectre Before We can use it With frames.
[00:20:14:319 - 00:20:16:660] **Speaker 1:** So at the moment, it's 4 degrees of freedom vector,
[00:20:17:520 - 00:20:20:040] **Speaker 1:** um, which corresponds to beams and we need to introduce
[00:20:20:040 - 00:20:21:260] **Speaker 1:** the axial component as well.
[00:20:21:680 - 00:20:22:680] **Speaker 1:** That's a pretty simple process.
[00:20:22:760 - 00:20:25:040] **Speaker 1:** We'll do that, um, in a few minutes, but first
[00:20:25:040 - 00:20:27:030] **Speaker 1:** of all, we're gonna look at is a few different
[00:20:27:359 - 00:20:28:040] **Speaker 1:** cases here.
[00:20:35:099 - 00:20:38:699] **Speaker 1:** So, The next thing we're gonna look at is a
[00:20:38:699 - 00:20:40:680] **Speaker 1:** linearly veering distributed load.
[00:20:41:020 - 00:20:44:540] **Speaker 1:** So this is a linearly varying load and it has
[00:20:44:540 - 00:20:46:869] **Speaker 1:** a peak intensity at X equals L.
[00:20:54:790 - 00:20:58:030] **Speaker 1:** So a linearly varying load, um, the functions linearly varying,
[00:20:58:069 - 00:20:59:819] **Speaker 1:** a simple value of X.
[00:20:59:989 - 00:21:01:859] **Speaker 1:** The peak intensity is at the right hand node node
[00:21:01:859 - 00:21:02:170] **Speaker 1:** 2.
[00:21:03:280 - 00:21:07:989] **Speaker 1:** So the key thing here is One of the very
[00:21:07:989 - 00:21:09:050] **Speaker 1:** few cases.
[00:21:13:729 - 00:21:15:189] **Speaker 1:** Were element orientation.
[00:21:17:489 - 00:21:18:209] **Speaker 1:** Matters.
[00:21:22:380 - 00:21:26:859] **Speaker 1:** We have said here That previously that, you know, orientation
[00:21:26:859 - 00:21:27:579] **Speaker 1:** kind of arbitrary.
[00:21:27:739 - 00:21:29:979] **Speaker 1:** You can choose whichever orientation you like as long as
[00:21:29:979 - 00:21:30:800] **Speaker 1:** you're consistent.
[00:21:31:989 - 00:21:33:829] **Speaker 1:** This is one case where you have to be careful
[00:21:33:829 - 00:21:36:670] **Speaker 1:** because of the fact that it assumes that, uh, this
[00:21:36:670 - 00:21:37:510] **Speaker 1:** is X here.
[00:21:37:709 - 00:21:39:670] **Speaker 1:** So this will be node 1 here, this will be
[00:21:39:670 - 00:21:40:229] **Speaker 1:** node 2.
[00:21:41:660 - 00:21:45:800] **Speaker 1:** And then This will have a peak intensity.
[00:21:48:250 - 00:21:49:430] **Speaker 1:** Uh W bar.
[00:21:51:530 - 00:21:53:689] **Speaker 1:** At X equals L.
[00:21:54:630 - 00:21:57:310] **Speaker 1:** So obviously when X equals L, the bracketed term goes
[00:21:57:310 - 00:21:59:969] **Speaker 1:** to 1 and X equals 0, it goes to 0
[00:22:00:229 - 00:22:01:819] **Speaker 1:** and a linear profile between there.
[00:22:04:060 - 00:22:06:780] **Speaker 1:** Just as we did before, we'll assume that it acts
[00:22:06:780 - 00:22:09:180] **Speaker 1:** up upwards in the positive Y direction.
[00:22:12:829 - 00:22:16:109] **Speaker 1:** And then what we do is we Start off with
[00:22:16:109 - 00:22:19:150] **Speaker 1:** the same basic equation we had previously with W X.
[00:22:19:229 - 00:22:21:750] **Speaker 1:** Now it's W bar times X over L.
[00:22:22:109 - 00:22:24:329] **Speaker 1:** So we can bring the W bar over L outside
[00:22:24:329 - 00:22:25:859] **Speaker 1:** the integral because they're constants.
[00:22:26:390 - 00:22:28:189] **Speaker 1:** But now there's also an X that goes into here.
[00:22:28:430 - 00:22:31:709] **Speaker 1:** So this is X times the shape functions in this
[00:22:31:709 - 00:22:32:390] **Speaker 1:** vector here.
[00:22:36:140 - 00:22:38:619] **Speaker 1:** So then we integrate that with respect to X.
[00:22:39:099 - 00:22:42:500] **Speaker 1:** Again, this is uh uh the integral here, evaluate that
[00:22:42:500 - 00:22:44:900] **Speaker 1:** between 0 and L and then we end up with
[00:22:44:900 - 00:22:46:709] **Speaker 1:** this set of vectors here.
[00:22:52:260 - 00:22:53:030] **Speaker 1:** So this here.
[00:22:58:000 - 00:23:04:250] **Speaker 1:** Of the victors That represent The LVL.
[00:23:07:689 - 00:23:10:390] **Speaker 1:** So they are of course the 4th degree of freedom.
[00:23:13:010 - 00:23:13:910] **Speaker 1:** The element formulation.
[00:23:22:900 - 00:23:24:300] **Speaker 1:** Now, there's a few things we can do just to
[00:23:24:300 - 00:23:24:520] **Speaker 1:** check.
[00:23:25:520 - 00:23:26:650] **Speaker 1:** Do a quick sanity check on this.
[00:23:26:729 - 00:23:28:609] **Speaker 1:** We've got this nice sort of summary table at the
[00:23:28:609 - 00:23:30:510] **Speaker 1:** bottom, which represents what's going on.
[00:23:33:670 - 00:23:35:709] **Speaker 1:** Now, we started as intensity of 0.
[00:23:35:790 - 00:23:38:270] **Speaker 1:** We end up with a maximum intensity of W bar.
[00:23:38:670 - 00:23:45:609] **Speaker 1:** So The Average or?
[00:23:47:040 - 00:23:47:430] **Speaker 1:** Mean.
[00:23:48:890 - 00:23:53:359] **Speaker 1:** W Of WF X.
[00:23:54:719 - 00:23:57:079] **Speaker 1:** Is going to be the peak value of W bar
[00:23:57:079 - 00:23:59:920] **Speaker 1:** plus the value of 0, divided by 2, so it's
[00:23:59:920 - 00:24:01:579] **Speaker 1:** gonna be W bar over 2.
[00:24:04:239 - 00:24:05:619] **Speaker 1:** The total share stress.
[00:24:10:510 - 00:24:13:660] **Speaker 1:** Along the elements, sorry, total sheer force.
[00:24:17:800 - 00:24:22:280] **Speaker 1:** Along the element Will be equal to the average intensity
[00:24:22:280 - 00:24:23:000] **Speaker 1:** times L.
[00:24:23:119 - 00:24:25:560] **Speaker 1:** So W bar L over 2.
[00:24:25:920 - 00:24:29:349] **Speaker 1:** So that's essentially the short again.
[00:24:29:479 - 00:24:31:770] **Speaker 1:** So W bar L upon 2.
[00:24:33:849 - 00:24:36:180] **Speaker 1:** So we would expect the total shear force to match
[00:24:36:180 - 00:24:36:560] **Speaker 1:** that.
[00:24:37:430 - 00:24:39:530] **Speaker 1:** Now, what is our equivalent nodal loading giving us?
[00:24:40:290 - 00:24:42:150] **Speaker 1:** We're gonna take this value, and we're gonna take this
[00:24:42:150 - 00:24:43:890] **Speaker 1:** value, and we'll bring those down.
[00:24:44:650 - 00:24:49:469] **Speaker 1:** We have 3 W L over 20 + 7.
[00:24:51:619 - 00:24:53:020] **Speaker 1:** W L over 20.
[00:24:54:160 - 00:24:57:839] **Speaker 1:** Which of course is equal to 10 W L over
[00:24:57:839 - 00:24:58:380] **Speaker 1:** 20.
[00:24:59:469 - 00:25:01:750] **Speaker 1:** Or W bar L over 2.
[00:25:02:800 - 00:25:04:719] **Speaker 1:** So just a quick sanity check there.
[00:25:05:319 - 00:25:09:079] **Speaker 1:** We would expect that this gives us the same total
[00:25:09:079 - 00:25:13:760] **Speaker 1:** sheer force that our original setup gave us and thankfully
[00:25:13:760 - 00:25:14:380] **Speaker 1:** it does.
[00:25:15:569 - 00:25:18:339] **Speaker 1:** Now, a couple, you know, we won't necessarily tell us
[00:25:18:339 - 00:25:21:609] **Speaker 1:** if these values are mathematically accurate, but we would expect
[00:25:21:609 - 00:25:26:199] **Speaker 1:** probably a greater portion of this distributed load to be
[00:25:26:199 - 00:25:28:500] **Speaker 1:** lumped at this node because the intensity is greater there.
[00:25:29:609 - 00:25:31:729] **Speaker 1:** And we do end up with a a greater share
[00:25:31:729 - 00:25:34:640] **Speaker 1:** of this load and a lesser share, uh, a lesser
[00:25:34:640 - 00:25:38:829] **Speaker 1:** component of this sheer force at the left-handing as well.
[00:25:40:189 - 00:25:42:310] **Speaker 1:** So just always good to do this sort of sanity
[00:25:42:310 - 00:25:45:589] **Speaker 1:** checks and say does this result that we get mathematically
[00:25:45:589 - 00:25:47:510] **Speaker 1:** kind of make physical sense?
[00:25:47:630 - 00:25:49:930] **Speaker 1:** And I think, you know, broadly, it does.
[00:25:51:479 - 00:25:53:880] **Speaker 1:** The other thing, if the load was upwards as it's
[00:25:53:880 - 00:25:57:479] **Speaker 1:** drawn here, and as our sign convention dictates, that's going
[00:25:57:479 - 00:26:01:680] **Speaker 1:** to be a um a hogging moment.
[00:26:01:839 - 00:26:03:880] **Speaker 1:** So it's gonna be a moment that kind of goes
[00:26:03:880 - 00:26:04:660] **Speaker 1:** up like this.
[00:26:05:989 - 00:26:10:640] **Speaker 1:** So that's what the defected shape of the The element
[00:26:10:640 - 00:26:11:380] **Speaker 1:** would look like.
[00:26:13:489 - 00:26:17:250] **Speaker 1:** So the first one here is a counterclockwise, we follow
[00:26:17:250 - 00:26:20:050] **Speaker 1:** our sign convention, and that's a positive number.
[00:26:20:290 - 00:26:22:839] **Speaker 1:** So that would induce if it was counterclockwise moment, that
[00:26:22:839 - 00:26:24:969] **Speaker 1:** would induce this type of deflection.
[00:26:25:500 - 00:26:27:900] **Speaker 1:** Uh, this one here is also drawn as counterclockwise, but
[00:26:27:900 - 00:26:28:910] **Speaker 1:** it's a negative number.
[00:26:29:420 - 00:26:31:180] **Speaker 1:** So that would actually be a clockwise moment, which would
[00:26:31:180 - 00:26:35:359] **Speaker 1:** also support this hogging moment rather than a sagging moment.
[00:26:35:500 - 00:26:37:920] **Speaker 1:** So again, just to do that quick sanity check to
[00:26:37:920 - 00:26:40:619] **Speaker 1:** say like, does it make the sense that we, you
[00:26:40:619 - 00:26:42:319] **Speaker 1:** know, fit what we might expect.
[00:26:42:900 - 00:26:44:099] **Speaker 1:** And thankfully, it does.
[00:26:46:810 - 00:26:49:650] **Speaker 1:** Now, um, I do appreciate that because this is one
[00:26:49:650 - 00:26:52:150] **Speaker 1:** of the few times when element orientation matters.
[00:26:52:719 - 00:26:55:599] **Speaker 1:** Suppose you've set up a problem, and you've actually oriented
[00:26:55:599 - 00:26:56:790] **Speaker 1:** the element the other way.
[00:26:58:199 - 00:27:00:979] **Speaker 1:** The next page may be helpful to you, which is
[00:27:01:680 - 00:27:04:589] **Speaker 1:** essentially the same thing, except now the intensity is is
[00:27:04:589 - 00:27:04:920] **Speaker 1:** flipped.
[00:27:05:040 - 00:27:07:260] **Speaker 1:** So it still acts upwards in the positive Y direction.
[00:27:08:219 - 00:27:10:489] **Speaker 1:** But now the peak intensity is at node one.
[00:27:11:709 - 00:27:13:530] **Speaker 1:** And the zero intensity is at node 2.
[00:27:16:130 - 00:27:23:369] **Speaker 1:** So Peak intensity, W bar.
[00:27:27:099 - 00:27:33:160] **Speaker 1:** Now occurs At note 2 Sorry, note one.
[00:27:37:290 - 00:27:39:589] **Speaker 1:** And zero intensity.
[00:27:43:670 - 00:27:46:170] **Speaker 1:** It No 2.
[00:27:46:329 - 00:27:48:209] **Speaker 1:** So it's just the, the mirror of what we did
[00:27:48:209 - 00:27:48:920] **Speaker 1:** previously.
[00:27:50:349 - 00:27:52:510] **Speaker 1:** What was X over L is now 1 minus X
[00:27:52:510 - 00:27:53:060] **Speaker 1:** over L.
[00:27:53:510 - 00:27:55:689] **Speaker 1:** These look like our axial shape functions, but that's just
[00:27:55:689 - 00:27:58:010] **Speaker 1:** because they're doing a similar sort of interpretation.
[00:28:01:400 - 00:28:04:099] **Speaker 1:** So uh some interpolation between the values.
[00:28:04:880 - 00:28:07:140] **Speaker 1:** What was now we take WX and we substitute in
[00:28:07:140 - 00:28:08:300] **Speaker 1:** 1 minus X over L.
[00:28:09:589 - 00:28:12:989] **Speaker 1:** We bring W bar outside the integral again, because it
[00:28:12:989 - 00:28:15:930] **Speaker 1:** is constant, then we end up with this as our
[00:28:16:050 - 00:28:16:569] **Speaker 1:** term.
[00:28:17:349 - 00:28:20:180] **Speaker 1:** We do the multiplication through and then we integrate with
[00:28:20:180 - 00:28:23:410] **Speaker 1:** respect to X and we get this kind of slight
[00:28:23:410 - 00:28:24:569] **Speaker 1:** beast of an equation here.
[00:28:25:420 - 00:28:27:540] **Speaker 1:** Um, now we evaluate that between 0 and L.
[00:28:27:699 - 00:28:31:130] **Speaker 1:** Again, we get this horrible looking, um, equation, but a
[00:28:31:130 - 00:28:32:979] **Speaker 1:** lot of that simplifies out and we get a relatively
[00:28:32:979 - 00:28:34:819] **Speaker 1:** simple vector that comes out of that.
[00:28:37:069 - 00:28:42:300] **Speaker 1:** Now what we have is A 7 WL over 20,
[00:28:42:339 - 00:28:45:579] **Speaker 1:** so that the higher intensity now occurs at the the
[00:28:45:579 - 00:28:48:579] **Speaker 1:** lump she load applies at node one, the lower node
[00:28:48:579 - 00:28:49:939] **Speaker 1:** two, which we expect.
[00:28:49:969 - 00:28:55:930] **Speaker 1:** And then um you'd also see here that Um, the
[00:28:55:930 - 00:28:59:130] **Speaker 1:** moments have, the magnitudes have switched as well.
[00:29:03:359 - 00:29:05:500] **Speaker 1:** So that's just a a couple of options there.
[00:29:06:520 - 00:29:08:290] **Speaker 1:** They're essentially modelling the same thing and you could use,
[00:29:08:359 - 00:29:10:560] **Speaker 1:** you could just flip the element through 180 degrees and
[00:29:10:560 - 00:29:13:260] **Speaker 1:** the sign change the sign, or you can use the
[00:29:13:270 - 00:29:15:199] **Speaker 1:** the different uh derivation there.
[00:29:18:729 - 00:29:22:390] **Speaker 1:** The next thing we can look at Is point loads
[00:29:22:390 - 00:29:23:410] **Speaker 1:** applied within an element.
[00:29:25:260 - 00:29:27:020] **Speaker 1:** So the first thing you can say here is, well,
[00:29:27:219 - 00:29:29:109] **Speaker 1:** if we've got a point not applied within an element,
[00:29:29:939 - 00:29:31:339] **Speaker 1:** why don't we just put a note to point there
[00:29:31:339 - 00:29:32:540] **Speaker 1:** and break it up into two elements?
[00:29:32:739 - 00:29:33:770] **Speaker 1:** Well, you'd be absolutely right.
[00:29:33:819 - 00:29:36:060] **Speaker 1:** That is totally an option to you and I will
[00:29:36:339 - 00:29:37:339] **Speaker 1:** give you the same answer.
[00:29:37:500 - 00:29:37:939] **Speaker 1:** Um.
[00:29:38:709 - 00:29:40:689] **Speaker 1:** This is more, yeah, if you really did want to
[00:29:40:829 - 00:29:43:150] **Speaker 1:** not write out another assembly matrix or code up another
[00:29:43:150 - 00:29:46:229] **Speaker 1:** element, or suppose you'd already set up the structure and
[00:29:46:229 - 00:29:48:750] **Speaker 1:** the loading changed and now there was a load partway
[00:29:48:750 - 00:29:49:349] **Speaker 1:** along an element.
[00:29:49:469 - 00:29:51:989] **Speaker 1:** So yeah, ultimately the same thing as putting a nodal
[00:29:51:989 - 00:29:52:390] **Speaker 1:** point here.
[00:29:52:550 - 00:29:55:130] **Speaker 1:** But nonetheless, if you did have a concentrated shear load
[00:29:55:130 - 00:29:56:609] **Speaker 1:** applied somewhere along the element.
[00:29:59:520 - 00:30:02:260] **Speaker 1:** So up until here, we've assumed that the, the concentrated
[00:30:02:260 - 00:30:03:689] **Speaker 1:** loads are only at the nodal points.
[00:30:05:150 - 00:30:08:189] **Speaker 1:** Um, now what we're gonna do is define W X
[00:30:08:189 - 00:30:11:859] **Speaker 1:** as equal to an intensity W bar times the direct
[00:30:11:859 - 00:30:12:530] **Speaker 1:** delta function.
[00:30:13:569 - 00:30:15:420] **Speaker 1:** Applied at a distance X minus A.
[00:30:15:579 - 00:30:18:359] **Speaker 1:** So what they're saying is that this function here.
[00:30:19:280 - 00:30:21:000] **Speaker 1:** is saying essentially as you move along, it has a
[00:30:21:000 - 00:30:24:040] **Speaker 1:** value of 00,0001,000.
[00:30:24:099 - 00:30:26:560] **Speaker 1:** So just only at X equals A is the have
[00:30:26:560 - 00:30:27:469] **Speaker 1:** a value of 1.
[00:30:27:760 - 00:30:29:579] **Speaker 1:** Every other point has a value of 0.
[00:30:30:640 - 00:30:33:760] **Speaker 1:** We then multiply by W bar and this is our
[00:30:34:550 - 00:30:40:619] **Speaker 1:** location of our um This is the equation which captures
[00:30:40:619 - 00:30:41:270] **Speaker 1:** this loading case.
[00:30:41:430 - 00:30:43:489] **Speaker 1:** So it's the direct director for function.
[00:30:45:569 - 00:31:03:180] **Speaker 1:** Also known As an Impulse Function Now, we can go
[00:31:03:180 - 00:31:04:739] **Speaker 1:** and we can substitute that in.
[00:31:05:930 - 00:31:10:089] **Speaker 1:** Bring the W bar outside the integral, um, plug that
[00:31:10:089 - 00:31:10:530] **Speaker 1:** in.
[00:31:10:780 - 00:31:13:459] **Speaker 1:** This is the equation that we would get.
[00:31:15:609 - 00:31:20:339] **Speaker 1:** So this one here Is the general case.
[00:31:22:420 - 00:31:26:959] **Speaker 1:** For A concentrated.
[00:31:31:199 - 00:31:46:069] **Speaker 1:** Sheer load Anywhere Along the element So it's just generic.
[00:31:48:310 - 00:31:49:089] **Speaker 1:** position.
[00:31:50:479 - 00:31:52:000] **Speaker 1:** X equals A.
[00:31:56:170 - 00:31:58:329] **Speaker 1:** And then this is the uh if we were to
[00:31:58:329 - 00:32:00:489] **Speaker 1:** look at a special case of a mid-span point load
[00:32:00:489 - 00:32:03:569] **Speaker 1:** and substitute A equals L over 2, this is the
[00:32:03:569 - 00:32:05:609] **Speaker 1:** vector that we would get out of that.
[00:32:08:280 - 00:32:10:160] **Speaker 1:** So this is the um.
[00:32:10:890 - 00:32:17:449] **Speaker 1:** The victors here again and Um Photography and be element
[00:32:17:449 - 00:32:17:790] **Speaker 1:** formulation.
[00:32:19:510 - 00:32:20:969] **Speaker 1:** So these are the special case.
[00:32:23:500 - 00:32:25:800] **Speaker 1:** Of A equals L upon 2.
[00:32:31:339 - 00:32:35:030] **Speaker 1:** So once again, 4 degree freedom beam, and it needs
[00:32:35:030 - 00:32:38:250] **Speaker 1:** to be transformed into the 6 degree of freedom frame.
[00:32:41:819 - 00:32:43:199] **Speaker 1:** So how do we go about this?
[00:32:43:819 - 00:32:45:739] **Speaker 1:** Well, thankfully, it's not actually that hard to do.
[00:32:45:900 - 00:32:47:979] **Speaker 1:** We're gonna go back to our good old friend, the
[00:32:47:979 - 00:32:49:760] **Speaker 1:** principle of linear superposition.
[00:32:50:699 - 00:32:52:439] **Speaker 1:** The same thing we did when we built up the
[00:32:52:449 - 00:32:54:000] **Speaker 1:** the overall stiffness matrix.
[00:32:54:780 - 00:32:57:500] **Speaker 1:** And we're just going to essentially put zeros on the
[00:32:57:500 - 00:32:58:180] **Speaker 1:** axial terms.
[00:32:58:339 - 00:33:01:060] **Speaker 1:** So we are assuming the axial terms and the flexual
[00:33:01:060 - 00:33:03:939] **Speaker 1:** terms are being solved independently and that adding a pure
[00:33:03:939 - 00:33:10:739] **Speaker 1:** axial load um doesn't um Contribute anything to the to
[00:33:10:739 - 00:33:14:459] **Speaker 1:** the shear and the pure shear load doesn't contribute anything
[00:33:14:459 - 00:33:15:760] **Speaker 1:** to the axial deformations.
[00:33:17:819 - 00:33:19:030] **Speaker 1:** So all we go through here.
[00:33:20:640 - 00:33:24:599] **Speaker 1:** This year, probably a a useful reference point here is
[00:33:24:599 - 00:33:25:819] **Speaker 1:** just to quickly sketch.
[00:33:26:640 - 00:33:29:790] **Speaker 1:** The elements, numbering sequence for beam elements.
[00:33:30:660 - 00:33:31:880] **Speaker 1:** And frame elements.
[00:33:35:780 - 00:33:42:150] **Speaker 1:** So this is the Beam, we have an D1.
[00:33:43:449 - 00:33:47:560] **Speaker 1:** If one A D2 and an F2.
[00:33:49:670 - 00:33:56:640] **Speaker 1:** AD3 And an F3, and then a D4 and an
[00:33:56:640 - 00:33:57:250] **Speaker 1:** F4.
[00:33:59:420 - 00:34:00:280] **Speaker 1:** For frames.
[00:34:10:969 - 00:34:13:500] **Speaker 1:** Our free body diagram here.
[00:34:17:898 - 00:34:19:299] **Speaker 1:** It's F1.
[00:34:21:530 - 00:34:26:419] **Speaker 1:** F2 If 3 only drawing the forces, there's of course
[00:34:26:419 - 00:34:28:340] **Speaker 1:** corresponding um.
[00:34:29:628 - 00:34:30:959] **Speaker 1:** Deflections as well.
[00:34:31:979 - 00:34:34:100] **Speaker 1:** F 5.
[00:34:34:939 - 00:34:36:239] **Speaker 1:** And F6.
[00:34:38:309 - 00:34:41:638] **Speaker 1:** So essentially what we're doing is that one, Now becomes
[00:34:41:638 - 00:34:43:540] **Speaker 1:** 22 now becomes 3.
[00:34:44:729 - 00:34:46:729] **Speaker 1:** The first term is 0.
[00:34:47:718 - 00:34:50:999] **Speaker 1:** And then what was 3 becomes 5 and what was
[00:34:50:999 - 00:34:52:099] **Speaker 1:** 4 becomes 6.
[00:34:53:079 - 00:34:55:299] **Speaker 1:** So we're just adding in the zeros here and here.
[00:34:56:479 - 00:34:58:158] **Speaker 1:** And the same is true here, you know, there's just.
[00:35:02:540 - 00:35:17:110] **Speaker 1:** No axial contribution And the same is true here.
[00:35:18:600 - 00:35:20:379] **Speaker 1:** 0 X your contribution here and here.
[00:35:24:189 - 00:35:28:510] **Speaker 1:** If we look at the equivalent nodal definition for a
[00:35:28:510 - 00:35:30:399] **Speaker 1:** generic point anywhere along A.
[00:35:30:949 - 00:35:33:229] **Speaker 1:** So this is a 0, then we have the equate
[00:35:33:229 - 00:35:36:830] **Speaker 1:** the two components for shear and moment, 0 for axial
[00:35:36:830 - 00:35:38:850] **Speaker 1:** equation for she and then an equation for the moment.
[00:35:39:719 - 00:35:41:840] **Speaker 1:** And then for the specific case of A equals L
[00:35:41:840 - 00:35:45:080] **Speaker 1:** over 2, this is the, the vector that results from
[00:35:45:080 - 00:35:45:479] **Speaker 1:** that.
[00:35:49:590 - 00:35:53:750] **Speaker 1:** So that there is that's all the different types of
[00:35:53:750 - 00:35:56:330] **Speaker 1:** distributed loading for share that we're going to consider.
[00:35:57:290 - 00:35:59:850] **Speaker 1:** It's Obviously, you know, 4 out of an infinite number,
[00:36:00:050 - 00:36:04:229] **Speaker 1:** but really, it's gonna cover almost every engineering application you're
[00:36:04:229 - 00:36:06:649] **Speaker 1:** gonna come across in the real world.
[00:36:09:179 - 00:36:12:179] **Speaker 1:** Now I did also promise you uh back in about
[00:36:12:179 - 00:36:14:939] **Speaker 1:** week one, maybe start of week two, that we will
[00:36:14:939 - 00:36:16:739] **Speaker 1:** also look at distributed axial loads.
[00:36:16:939 - 00:36:19:320] **Speaker 1:** And this is actually a very, very similar approach.
[00:36:24:419 - 00:36:27:000] **Speaker 1:** So these are dealt with in a very similar way.
[00:36:28:040 - 00:36:29:879] **Speaker 1:** So this looks like a similar equation.
[00:36:29:959 - 00:36:31:179] **Speaker 1:** It looks a little bit different now.
[00:36:33:590 - 00:36:36:870] **Speaker 1:** So what we're doing is using psi of X, which
[00:36:36:870 - 00:36:38:310] **Speaker 1:** is our axial-shaped functions.
[00:36:39:639 - 00:36:43:729] **Speaker 1:** In place of In of X, so we're using our
[00:36:43:729 - 00:36:46:110] **Speaker 1:** axial shaped functions instead of our transverse ones.
[00:36:50:500 - 00:36:51:879] **Speaker 1:** And PFX.
[00:36:53:750 - 00:36:57:870] **Speaker 1:** In place Of W of X.
[00:36:58:719 - 00:37:01:370] **Speaker 1:** So PX is our axial distributed load intensity.
[00:37:01:810 - 00:37:04:489] **Speaker 1:** W over X was our sheer load intensity that was
[00:37:04:489 - 00:37:05:709] **Speaker 1:** distributed along the element.
[00:37:06:250 - 00:37:08:530] **Speaker 1:** And then these are axial shape functions and our transverse
[00:37:08:530 - 00:37:09:129] **Speaker 1:** shape functions.
[00:37:09:330 - 00:37:13:739] **Speaker 1:** So we take a um Change a few things there,
[00:37:13:899 - 00:37:15:699] **Speaker 1:** but the equation has the same form.
[00:37:16:060 - 00:37:18:290] **Speaker 1:** We're just using the axial terms for the axial distributed
[00:37:18:290 - 00:37:21:379] **Speaker 1:** loads and the share ones for the shared loads.
[00:37:22:500 - 00:37:25:070] **Speaker 1:** Just a quick reminder, these were our axial shape functions
[00:37:25:070 - 00:37:27:239] **Speaker 1:** that we had from previously.
[00:37:29:760 - 00:37:32:760] **Speaker 1:** Now again, this could be any number of different uh
[00:37:32:760 - 00:37:34:179] **Speaker 1:** PFX could be down to anything.
[00:37:35:159 - 00:37:37:399] **Speaker 1:** Realistically, there's only a couple of cases that we're actually
[00:37:37:399 - 00:37:39:979] **Speaker 1:** gonna consider that you're actually gonna likely to come across.
[00:37:43:689 - 00:37:45:449] **Speaker 1:** So the first case is that PF X is a
[00:37:45:449 - 00:37:46:469] **Speaker 1:** constant P bar.
[00:37:47:959 - 00:37:51:429] **Speaker 1:** That just means there's some constant distributed load that exists
[00:37:51:429 - 00:37:51:979] **Speaker 1:** within an element.
[00:37:53:389 - 00:37:58:350] **Speaker 1:** Now what we are doing um static statics only in
[00:37:58:350 - 00:38:01:949] **Speaker 1:** this class, this could be something from uh dynamics, like
[00:38:01:949 - 00:38:04:790] **Speaker 1:** if this was um some sort of acceleration term.
[00:38:06:149 - 00:38:08:709] **Speaker 1:** Or, of course, we can turn it 90 degrees, and
[00:38:08:709 - 00:38:10:530] **Speaker 1:** that could be the self weight of the element.
[00:38:13:489 - 00:38:15:810] **Speaker 1:** So this is just a case of uh P bar
[00:38:15:810 - 00:38:18:350] **Speaker 1:** being a constant intensity all the way along the element.
[00:38:18:760 - 00:38:21:149] **Speaker 1:** And if we go through the same process we've applied,
[00:38:21:770 - 00:38:22:649] **Speaker 1:** we substitute this.
[00:38:22:770 - 00:38:26:209] **Speaker 1:** This is now in uh two degree of freedom bar
[00:38:26:209 - 00:38:27:229] **Speaker 1:** element formulation.
[00:38:33:590 - 00:38:37:419] **Speaker 1:** The other thing is maybe to, we're gonna be consistent
[00:38:37:419 - 00:38:39:729] **Speaker 1:** with our sign convention is that we assume.
[00:38:43:050 - 00:38:43:889] **Speaker 1:** PF X.
[00:38:45:590 - 00:38:49:330] **Speaker 1:** Act In the positive.
[00:38:51:429 - 00:38:54:479] **Speaker 1:** X Direction.
[00:38:56:800 - 00:38:58:709] **Speaker 1:** Same way we assumed Y of X for the share
[00:38:58:709 - 00:38:59:110] **Speaker 1:** load.
[00:39:01:340 - 00:39:03:780] **Speaker 1:** And once we go through and we substitute in our
[00:39:03:780 - 00:39:06:860] **Speaker 1:** axial shape functions, um, P bar can be pulled out
[00:39:06:860 - 00:39:07:600] **Speaker 1:** because it's a constant.
[00:39:08:179 - 00:39:10:260] **Speaker 1:** We integrate, we evaluate, and this is the answer that
[00:39:10:260 - 00:39:10:820] **Speaker 1:** we get.
[00:39:12:560 - 00:39:15:280] **Speaker 1:** Now, I suspect probably none of you are particularly surprised
[00:39:15:280 - 00:39:16:260] **Speaker 1:** by that answer.
[00:39:16:919 - 00:39:18:919] **Speaker 1:** Um, but essentially we would end up, we would expect
[00:39:18:919 - 00:39:21:959] **Speaker 1:** to see an equal distribution of load at each end
[00:39:21:959 - 00:39:22:500] **Speaker 1:** of the element.
[00:39:24:790 - 00:39:26:550] **Speaker 1:** Now, this is only a 2 degree freedom bar element.
[00:39:26:590 - 00:39:28:989] **Speaker 1:** We do want to know how to extend that to
[00:39:28:989 - 00:39:29:669] **Speaker 1:** a frame element.
[00:39:29:870 - 00:39:31:870] **Speaker 1:** Well, we just do the opposite of what we did
[00:39:31:870 - 00:39:32:209] **Speaker 1:** before.
[00:39:32:310 - 00:39:34:810] **Speaker 1:** We put those terms into the axial locations.
[00:39:35:350 - 00:39:37:750] **Speaker 1:** We put zeros on the sheer and moment locations, and
[00:39:37:750 - 00:39:40:149] **Speaker 1:** that's how we apply it to a frame element.
[00:39:40:510 - 00:39:43:159] **Speaker 1:** So This here is.
[00:39:44:590 - 00:39:45:510] **Speaker 1:** Our bar.
[00:39:46:959 - 00:39:55:360] **Speaker 1:** Element Formulation And this here is our Frame.
[00:39:57:879 - 00:39:58:520] **Speaker 1:** Element.
[00:40:02:770 - 00:40:02:780] **Speaker 1:** I.
[00:40:07:770 - 00:40:10:689] **Speaker 1:** Now, what we're also gonna do here is look at
[00:40:10:689 - 00:40:14:770] **Speaker 1:** a concentrated axial load that acts somewhere along the element
[00:40:14:770 - 00:40:16:790] **Speaker 1:** of distance A from node one.
[00:40:18:790 - 00:40:23:260] **Speaker 1:** So The load.
[00:40:24:649 - 00:40:27:060] **Speaker 1:** Acts in the Xi direction.
[00:40:32:800 - 00:40:34:580] **Speaker 1:** At distance A.
[00:40:37:590 - 00:40:38:510] **Speaker 1:** From note one.
[00:40:41:770 - 00:40:43:459] **Speaker 1:** So again, this goes back, you could just put a
[00:40:43:459 - 00:40:44:399] **Speaker 1:** nodal point there.
[00:40:45:969 - 00:40:48:250] **Speaker 1:** And break up the elements, but if you wanted to
[00:40:48:250 - 00:40:50:330] **Speaker 1:** instead introduce a load partway along, this is how you
[00:40:50:330 - 00:40:50:909] **Speaker 1:** could do it.
[00:40:55:800 - 00:40:58:639] **Speaker 1:** Now, you've got this direct delta function in here, 1
[00:40:58:639 - 00:41:00:389] **Speaker 1:** minus 6 over LX over L.
[00:41:01:040 - 00:41:03:360] **Speaker 1:** Um, you substitute that in and this is the the
[00:41:03:360 - 00:41:05:189] **Speaker 1:** load that you this is the vector that you get
[00:41:05:189 - 00:41:05:840] **Speaker 1:** out of that.
[00:41:08:929 - 00:41:11:510] **Speaker 1:** So what we have here is.
[00:41:12:889 - 00:41:23:969] **Speaker 1:** The result is essentially a Aesthetically Indeterminate.
[00:41:25:800 - 00:41:26:659] **Speaker 1:** Axial problem.
[00:41:30:219 - 00:41:32:260] **Speaker 1:** So hopefully this takes you back to the early parts
[00:41:32:260 - 00:41:35:060] **Speaker 1:** of 202, last year or any equivalent course that you
[00:41:35:060 - 00:41:35:479] **Speaker 1:** would have done.
[00:41:36:379 - 00:41:39:760] **Speaker 1:** And essentially, the closer, the closer the load is applied
[00:41:40:459 - 00:41:41:260] **Speaker 1:** to node one.
[00:41:42:860 - 00:41:46:320] **Speaker 1:** The section of bars, we're assuming constant elastic modulus, cross-sectional
[00:41:46:320 - 00:41:47:020] **Speaker 1:** area, etc.
[00:41:47:409 - 00:41:48:800] **Speaker 1:** cosmetic homogeneous bar.
[00:41:49:639 - 00:41:51:360] **Speaker 1:** So that means the closer the load is applied to
[00:41:51:360 - 00:41:53:909] **Speaker 1:** node one, this piece of bar is much shorter.
[00:41:53:959 - 00:41:55:800] **Speaker 1:** So it's going to be much stiffer than this space.
[00:41:56:000 - 00:41:58:840] **Speaker 1:** So essentially, the closer the load is applied to node
[00:41:58:840 - 00:42:02:389] **Speaker 1:** one, the greater the proportion of that load is carried
[00:42:02:389 - 00:42:03:129] **Speaker 1:** by node one.
[00:42:03:479 - 00:42:07:280] **Speaker 1:** And the closer the load gets to node two, then
[00:42:07:280 - 00:42:09:939] **Speaker 1:** this piece of bar becomes more flexible relative to this.
[00:42:10:280 - 00:42:13:000] **Speaker 1:** And because it's definitely the indeterminant, the relative stiffness is
[00:42:13:000 - 00:42:15:360] **Speaker 1:** governed the way that load is distributed, and you'd see
[00:42:15:360 - 00:42:18:179] **Speaker 1:** a greater percentage of that load going into node two.
[00:42:18:760 - 00:42:22:379] **Speaker 1:** So This is essentially um, just the way of representing
[00:42:22:379 - 00:42:22:679] **Speaker 1:** that.
[00:42:24:350 - 00:42:27:389] **Speaker 1:** So again, this is a a um it's not shouldn't
[00:42:27:389 - 00:42:30:360] **Speaker 1:** contradict anything that you learned last year in your mechanics
[00:42:30:360 - 00:42:30:689] **Speaker 1:** class.
[00:42:32:070 - 00:42:34:139] **Speaker 1:** It's just a computational framework on top of that.
[00:42:36:080 - 00:42:38:189] **Speaker 1:** So what we have here is we have our 1
[00:42:38:189 - 00:42:39:370] **Speaker 1:** minus 6 over L here.
[00:42:39:760 - 00:42:41:800] **Speaker 1:** We have 1 minus a over rail and A over
[00:42:41:800 - 00:42:42:020] **Speaker 1:** rail.
[00:42:42:679 - 00:42:44:120] **Speaker 1:** And then we just do the same thing here where
[00:42:44:120 - 00:42:47:360] **Speaker 1:** we put zeros on the uh flexural and moment terms
[00:42:47:360 - 00:42:53:489] **Speaker 1:** and then we put these values onto the um The,
[00:42:53:600 - 00:42:56:280] **Speaker 1:** the non-zero values onto the actual locations, so.
[00:42:57:810 - 00:42:58:949] **Speaker 1:** There's no sheer force.
[00:43:03:719 - 00:43:04:860] **Speaker 1:** No pending moment.
[00:43:09:649 - 00:43:11:270] **Speaker 1:** And again, just no sheer force.
[00:43:15:149 - 00:43:16:370] **Speaker 1:** And no bending moment.
[00:43:24:610 - 00:43:27:649] **Speaker 1:** Just a reminder, you know, X in the positive X
[00:43:27:649 - 00:43:28:449] **Speaker 1:** X direction.
[00:43:28:810 - 00:43:32:250] **Speaker 1:** That's just a, you know, nice consistent um sign convention.
[00:43:34:500 - 00:43:38:159] **Speaker 1:** And What we can do now is just work through
[00:43:38:159 - 00:43:41:600] **Speaker 1:** a relatively quick problem to apply this.
[00:43:41:879 - 00:43:44:010] **Speaker 1:** So that's kind of the theory theory.
[00:43:44:070 - 00:43:45:320] **Speaker 1:** And then we just had to look at how we
[00:43:45:320 - 00:43:50:070] **Speaker 1:** actually work through um and apply this situation um to
[00:43:50:070 - 00:43:51:060] **Speaker 1:** a to a structure.
[00:44:02:870 - 00:44:04:939] **Speaker 1:** Is there any questions on this derivation approach?
[00:44:11:250 - 00:44:11:409] **Speaker 1:** Right.
[00:44:11:530 - 00:44:14:969] **Speaker 1:** So what we're gonna do here is we're actually gonna
[00:44:14:969 - 00:44:16:610] **Speaker 1:** revisit a problem we've already solved.
[00:44:16:850 - 00:44:18:320] **Speaker 1:** So we did this on Friday.
[00:44:18:449 - 00:44:21:439] **Speaker 1:** We kind of work through this simple portal frame, um,
[00:44:21:689 - 00:44:25:110] **Speaker 1:** two columns and a, a bridge deck or something.
[00:44:25:840 - 00:44:28:149] **Speaker 1:** 10 kilonewton loads applied vertically.
[00:44:30:530 - 00:44:33:820] **Speaker 1:** We have some I and A values, elastic modulus, and
[00:44:33:820 - 00:44:35:939] **Speaker 1:** now we've got this approximately 5 tonne truck, which I'll
[00:44:35:939 - 00:44:36:800] **Speaker 1:** say is not.
[00:44:37:949 - 00:44:38:689] **Speaker 1:** To scale.
[00:44:39:709 - 00:44:40:780] **Speaker 1:** So that's 4.5 metres.
[00:44:40:860 - 00:44:42:800] **Speaker 1:** It's a pretty small truck to weigh 5 tonnes.
[00:44:43:659 - 00:44:46:060] **Speaker 1:** Maybe it's just not not concentrate too much on that
[00:44:46:060 - 00:44:46:719] **Speaker 1:** for too long.
[00:44:48:929 - 00:44:53:280] **Speaker 1:** Um, We're gonna assume that the structure represents the middle
[00:44:53:280 - 00:44:54:169] **Speaker 1:** section of a bridge.
[00:44:54:370 - 00:44:57:290] **Speaker 1:** The vertical elements represent the horizontal elements of the bridge
[00:44:57:290 - 00:45:00:489] **Speaker 1:** deck, and we're going to include self-weight from that distributed
[00:45:00:489 - 00:45:00:729] **Speaker 1:** element.
[00:45:00:850 - 00:45:04:090] **Speaker 1:** So we're gonna assume that the self-weight is a distributed
[00:45:04:090 - 00:45:05:810] **Speaker 1:** load, which is 10 kilonewtons per metre.
[00:45:06:290 - 00:45:08:689] **Speaker 1:** And then we're gonna have this lumped, they say approximately
[00:45:08:689 - 00:45:12:659] **Speaker 1:** 5 tonne, um, such that when we multiply by 9.81,
[00:45:12:810 - 00:45:14:669] **Speaker 1:** we get to exactly 50 kilonewtons.
[00:45:16:770 - 00:45:19:179] **Speaker 1:** And then this is what the the loading would look
[00:45:19:179 - 00:45:19:600] **Speaker 1:** like.
[00:45:19:979 - 00:45:21:659] **Speaker 1:** Now, the first thing we realised here is the structure
[00:45:21:659 - 00:45:22:760] **Speaker 1:** itself hasn't changed.
[00:45:23:100 - 00:45:25:360] **Speaker 1:** This is the exact same structure that we've solved before.
[00:45:26:260 - 00:45:28:060] **Speaker 1:** What we just have is we've just changed the loading
[00:45:28:060 - 00:45:28:820] **Speaker 1:** side of the equation.
[00:45:28:939 - 00:45:30:820] **Speaker 1:** So we just got some extra loads that didn't exist
[00:45:30:820 - 00:45:31:139] **Speaker 1:** before.
[00:45:34:199 - 00:45:35:620] **Speaker 1:** So if we look at the next page.
[00:45:37:580 - 00:45:43:010] **Speaker 1:** This is actually The exact same structure we've seen before.
[00:45:44:540 - 00:45:53:739] **Speaker 1:** So This is just A repeat.
[00:45:56:080 - 00:45:58:360] **Speaker 1:** Of page 110.
[00:46:00:429 - 00:46:02:550] **Speaker 1:** It's a different problem, but the structure's the same.
[00:46:03:070 - 00:46:04:629] **Speaker 1:** So we don't need to redo any of that.
[00:46:04:669 - 00:46:06:889] **Speaker 1:** We can just use the same structure we've done before.
[00:46:09:350 - 00:46:11:280] **Speaker 1:** Just a quick recap though, we had our element everybody
[00:46:11:280 - 00:46:17:110] **Speaker 1:** diagrams, um, connectivity information here, which informs how to generate
[00:46:17:110 - 00:46:19:030] **Speaker 1:** our corresponding assembly matrices.
[00:46:19:469 - 00:46:21:290] **Speaker 1:** That's the same process we've always applied.
[00:46:23:699 - 00:46:26:699] **Speaker 1:** We go through and we get a whole lot of
[00:46:27:909 - 00:46:30:439] **Speaker 1:** Um KG components.
[00:46:30:479 - 00:46:32:239] **Speaker 1:** So KG1, KG2, KG 3.
[00:46:32:320 - 00:46:33:959] **Speaker 1:** We sum those three together, we get this.
[00:46:34:199 - 00:46:37:639] **Speaker 1:** So this is the KG that represents the whole structure.
[00:46:37:879 - 00:46:39:719] **Speaker 1:** And again, this is exactly the same as it was
[00:46:39:719 - 00:46:43:679] **Speaker 1:** before because the structure itself hasn't changed, just the loading
[00:46:43:679 - 00:46:44:139] **Speaker 1:** conditions.
[00:46:45:639 - 00:46:47:860] **Speaker 1:** Now, what we had previously was just the nodal loans.
[00:46:49:889 - 00:46:53:639] **Speaker 1:** But what we have here is the process for introducing
[00:46:53:639 - 00:46:54:830] **Speaker 1:** the distributed loads.
[00:46:56:520 - 00:46:58:280] **Speaker 1:** Now, this is the the key steps which we've kind
[00:46:58:280 - 00:46:59:030] **Speaker 1:** of touched on.
[00:46:59:399 - 00:47:01:360] **Speaker 1:** But I don't think until we've worked through an example
[00:47:01:360 - 00:47:02:500] **Speaker 1:** that it really becomes clear.
[00:47:06:000 - 00:47:08:360] **Speaker 1:** So the first thing we look at is the UDL.
[00:47:09:709 - 00:47:12:520] **Speaker 1:** So this is the south weight of the bridge deck.
[00:47:14:800 - 00:47:16:699] **Speaker 1:** So it's 10 kilton per metre.
[00:47:17:199 - 00:47:19:020] **Speaker 1:** Uh, the element is 4.5 metres long.
[00:47:19:199 - 00:47:22:270] **Speaker 1:** So we're just taking this vector, we're substituting -10000.
[00:47:22:320 - 00:47:26:899] **Speaker 1:** So, um, In this example, the load acts in the
[00:47:26:899 - 00:47:27:939] **Speaker 1:** negative Y direction.
[00:47:28:260 - 00:47:30:879] **Speaker 1:** So that means the input value of W bar is
[00:47:31:280 - 00:47:33:419] **Speaker 1:** -10 kilomewtons per metre.
[00:47:34:719 - 00:47:37:790] **Speaker 1:** Or -10000 and that gives us this vector here.
[00:47:39:360 - 00:47:41:340] **Speaker 1:** So this here is an element.
[00:47:43:320 - 00:47:51:310] **Speaker 1:** Coordinates Then we want to look at using a transformation
[00:47:51:310 - 00:47:51:909] **Speaker 1:** matrix.
[00:47:53:459 - 00:47:54:360] **Speaker 1:** It's this here.
[00:47:58:169 - 00:47:59:919] **Speaker 1:** is a transformation matrix.
[00:48:04:600 - 00:48:08:040] **Speaker 1:** For The element.
[00:48:10:530 - 00:48:12:530] **Speaker 1:** To which the load is applied.
[00:48:22:510 - 00:48:25:510] **Speaker 1:** And then once we multiply by the pre-multiplied by the
[00:48:25:510 - 00:48:33:510] **Speaker 1:** transformation matrix transposed, we then end up in the Equivalent
[00:48:35:330 - 00:48:36:939] **Speaker 1:** Nodal forcing terms.
[00:48:43:699 - 00:48:45:360] **Speaker 1:** In global coordinates.
[00:48:46:810 - 00:48:50:159] **Speaker 1:** So it's aligned with the uppercase X and Y.
[00:48:52:780 - 00:48:54:360] **Speaker 1:** Then we bring in our assembly matrix.
[00:49:00:459 - 00:49:02:939] **Speaker 1:** And again, that's the assembly matrix for the elements to
[00:49:02:939 - 00:49:04:959] **Speaker 1:** which the distributed load is applied.
[00:49:08:689 - 00:49:10:030] **Speaker 1:** And what we end up with.
[00:49:11:129 - 00:49:18:989] **Speaker 1:** As the Equivalent Not all forcing terms.
[00:49:26:520 - 00:49:31:389] **Speaker 1:** That can be Directly included.
[00:49:33:669 - 00:49:41:760] **Speaker 1:** In our solution Now, one thing I would note here
[00:49:41:760 - 00:49:43:919] **Speaker 1:** is maybe in some ways, this isn't the best example
[00:49:43:919 - 00:49:47:149] **Speaker 1:** because this particular element to which these loads are applied
[00:49:47:479 - 00:49:51:500] **Speaker 1:** has a transformation matrix with an angle of 0 degrees.
[00:49:52:000 - 00:49:54:899] **Speaker 1:** So therefore, in this case, the transformation matrix happens to
[00:49:54:899 - 00:49:56:139] **Speaker 1:** be an identity matrix.
[00:49:56:649 - 00:49:59:830] **Speaker 1:** And it also so happens that the assembly matrix, so
[00:49:59:830 - 00:50:03:040] **Speaker 1:** the transformation matrix happens to be an identity matrix and
[00:50:03:040 - 00:50:06:679] **Speaker 1:** the assembly matrix also happens to be an identity matrix.
[00:50:06:800 - 00:50:11:169] **Speaker 1:** So in this particular example, That vector, that vector, and
[00:50:11:169 - 00:50:14:050] **Speaker 1:** that vector are actually the same vector, but that that
[00:50:14:050 - 00:50:15:189] **Speaker 1:** won't always be the case.
[00:50:15:610 - 00:50:17:510] **Speaker 1:** So even though you might look at this and go,
[00:50:17:580 - 00:50:19:250] **Speaker 1:** oh, well, I can just substitute and bang this straight
[00:50:19:250 - 00:50:19:590] **Speaker 1:** in.
[00:50:19:889 - 00:50:21:850] **Speaker 1:** And in this particular instance, you would get away with
[00:50:21:850 - 00:50:22:209] **Speaker 1:** that.
[00:50:22:639 - 00:50:24:370] **Speaker 1:** It's not a general approach and you do need to
[00:50:24:370 - 00:50:25:610] **Speaker 1:** follow through this process.
[00:50:26:010 - 00:50:29:409] **Speaker 1:** So um that's a pretty good place to start.
[00:50:29:479 - 00:50:30:949] **Speaker 1:** We'll finish this example on Wednesday.
[00:50:31:330 - 00:50:33:250] **Speaker 1:** Um, and then then I'll send out some information about
[00:50:33:250 - 00:50:34:770] **Speaker 1:** the um the lab for this week.
[00:50:34:889 - 00:50:36:909] **Speaker 1:** So thank you all for coming along.
[00:50:37:290 - 00:50:39:090] **Speaker 1:** And I'll see you again on Wednesday.
[00:51:08:639 - 00:51:08:649] **Speaker 0:** OK.
[00:51:26:699 - 00:51:28:270] **Speaker 0:** What your life.
[00:51:29:070 - 00:51:42:179] **Speaker 0:** I OK something the test.
[00:51:44:239 - 00:51:50:030] **Speaker 0:** Yeah, I understand, um, so I just think, I mean
[00:51:50:030 - 00:51:53:250] **Speaker 1:** if the do confirm a couple of details on that,
[00:51:53:729 - 00:51:57:080] **Speaker 1:** um, the intention is probably through, hopefully you can access
[00:51:57:080 - 00:51:59:429] **Speaker 0:** to my car or otherwise just through SSB but you
[00:51:59:429 - 00:51:59:840] **Speaker 0:** can bring in.
[00:52:02:179 - 00:52:02:699] **Speaker 0:** Restriction.
[00:52:04:979 - 00:52:06:449] **Speaker 1:** They have to just be parking cars.
[00:52:09:979 - 00:52:17:030] **Speaker 0:** You can't, uh, you can knuckle the information for that
[00:52:17:030 - 00:52:17:129] **Speaker 1:** in.
[00:52:20:750 - 00:52:22:060] **Speaker 0:** You can't do that because it's my test but How
[00:52:24:739 - 00:52:29:580] **Speaker 0:** I No, it's so.
[00:52:31:679 - 00:52:36:370] **Speaker 0:** we're here Thank you.
[00:52:43:790 - 00:52:45:030] **Speaker 0:** Thanks.
[00:52:46:330 - 00:52:48:770] **Speaker 0:** I've always, it's really funny, I tend to pack a
[00:52:48:770 - 00:52:49:040] **Speaker 0:** lot.
[00:52:49:169 - 00:52:50:250] **Speaker 0:** I always pack a lot.

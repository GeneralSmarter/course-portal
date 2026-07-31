# ENEL372-26S2 Lecture 9 native Echo transcript

Date: July 31, 2026 9:00am-9:55am
Transcript type: native Echo automated transcript.

[00:00:00:400 - 00:00:05:139] **Speaker 0:** All right, Kyorakoto, welcome along.
[00:00:07:260 - 00:00:10:229] **Speaker 0:** OK, well done on making it for the early class
[00:00:10:229 - 00:00:11:170] **Speaker 0:** on the Friday.
[00:00:11:430 - 00:00:15:989] **Speaker 0:** Um, alright, so we've, we've been looking at magnetic materials
[00:00:15:989 - 00:00:20:909] **Speaker 0:** initially and then, uh, a little bit about, um, magnetic
[00:00:20:909 - 00:00:25:670] **Speaker 0:** circuits specifically associated with, um, inductor cores.
[00:00:26:649 - 00:00:30:559] **Speaker 0:** All leading towards us looking at being able to um
[00:00:31:090 - 00:00:34:290] **Speaker 0:** design our own uh power inductor for our but converter.
[00:00:35:450 - 00:00:37:569] **Speaker 0:** So, we got up to the point with our magnetic
[00:00:37:569 - 00:00:42:529] **Speaker 0:** circuits where it seems like, uh, for the specific conditions
[00:00:42:529 - 00:00:45:290] **Speaker 0:** that we are considering, um, that it turns into a
[00:00:45:290 - 00:00:48:330] **Speaker 0:** fairly simple magnetic circuit that we are dealing with.
[00:00:48:650 - 00:00:52:310] **Speaker 0:** Um, so we have an MMF which is just equal
[00:00:52:310 - 00:00:54:729] **Speaker 0:** to the product between the number of turns that we
[00:00:54:729 - 00:00:59:470] **Speaker 0:** have for our um inductor winding, uh, multiplied by the
[00:00:59:470 - 00:01:02:310] **Speaker 0:** current that's flowing through it, through that winding.
[00:01:02:770 - 00:01:07:589] **Speaker 0:** So Uh, just a reminder, the magnetic flux that we
[00:01:07:589 - 00:01:13:029] **Speaker 0:** have is just equal to NI over R, which here
[00:01:13:029 - 00:01:16:190] **Speaker 0:** R is the reluctance of the magnetic circuit.
[00:01:23:699 - 00:01:26:819] **Speaker 0:** Alright, so the, the magnetic flux is uh NI over
[00:01:26:819 - 00:01:29:980] **Speaker 0:** R um or you could rearrange if you're trying to
[00:01:29:980 - 00:01:34:580] **Speaker 0:** solve for reluctance of course to R equals NI over
[00:01:34:580 - 00:01:35:029] **Speaker 0:** 5.
[00:01:36:190 - 00:01:39:470] **Speaker 0:** Right, and if you are thinking about the units that
[00:01:39:470 - 00:01:42:589] **Speaker 0:** we would save for that, then that's um amp.
[00:01:43:980 - 00:01:45:419] **Speaker 0:** Amp turns.
[00:01:48:209 - 00:01:53:080] **Speaker 0:** Per Weber Alright, I know it's a bit of an
[00:01:53:080 - 00:01:57:319] **Speaker 0:** odd one that, uh, and we also, just to keep
[00:01:57:319 - 00:01:59:160] **Speaker 0:** it clear in our minds that this is, this is
[00:01:59:160 - 00:02:02:000] **Speaker 0:** not, uh, a stretch from what we are used to
[00:02:02:000 - 00:02:05:400] **Speaker 0:** being able to do for our circuits, uh, we, we
[00:02:05:709 - 00:02:09:089] **Speaker 0:** also developed at the same time or considered an electric,
[00:02:09:199 - 00:02:10:639] **Speaker 0:** um, circuit analogy.
[00:02:17:649 - 00:02:22:210] **Speaker 0:** Alright, so we have an MMF, magnetomotive force, uh, for
[00:02:22:210 - 00:02:27:029] **Speaker 0:** electric circuit, we have an EMF or electromotive force, um,
[00:02:27:649 - 00:02:30:679] **Speaker 0:** so NI versus B, uh, and we just have a
[00:02:30:679 - 00:02:33:970] **Speaker 0:** circuit with resistance instead instead of reluctance and current instead
[00:02:33:970 - 00:02:34:750] **Speaker 0:** of flux.
[00:02:38:910 - 00:02:44:000] **Speaker 0:** Uh, when I looked or explained the BH curve in
[00:02:44:000 - 00:02:47:059] **Speaker 0:** the last lecture as well, I also, uh, showed there
[00:02:47:059 - 00:02:51:080] **Speaker 0:** that for the B, the magnetic flux density side of
[00:02:51:080 - 00:02:55:460] **Speaker 0:** things, that we have also that phi is equal to
[00:02:55:460 - 00:02:58:220] **Speaker 0:** the magnetic flux density, uh, times the area.
[00:02:59:029 - 00:02:59:039] **Speaker 0:** Right.
[00:03:03:970 - 00:03:07:570] **Speaker 0:** So we can utilise this expression for our flux uh
[00:03:07:570 - 00:03:11:449] **Speaker 0:** in our reluctance, um, expression just just as a substitute
[00:03:11:580 - 00:03:15:789] **Speaker 0:** and we end up with um NI over BA right.
[00:03:16:210 - 00:03:18:610] **Speaker 0:** We're gonna come back to this, so I'll label that
[00:03:18:610 - 00:03:19:710] **Speaker 0:** as equation one.
[00:03:37:250 - 00:03:42:559] **Speaker 0:** Alright, so As far as determining a value of conductance
[00:03:42:559 - 00:03:45:160] **Speaker 0:** that we might want to have in our um our
[00:03:45:160 - 00:03:48:759] **Speaker 0:** power electronic converter, um, we can do some circuit analysis.
[00:03:48:880 - 00:03:50:080] **Speaker 0:** We've been doing that anyway.
[00:03:50:399 - 00:03:53:279] **Speaker 0:** We maybe consider a certain amount of current ripple that's
[00:03:53:279 - 00:03:57:039] **Speaker 0:** allowable for our for our design, um, a certain amount
[00:03:57:039 - 00:04:01:000] **Speaker 0:** of average current Um, so, from all of these things,
[00:04:01:100 - 00:04:06:089] **Speaker 0:** uh, frequency, duty ratio, we can determine what the, um,
[00:04:06:229 - 00:04:10:289] **Speaker 0:** inductance value needs to be to achieve those sorts of,
[00:04:10:309 - 00:04:12:630] **Speaker 0:** um, values in our converter.
[00:04:13:360 - 00:04:17:118] **Speaker 0:** So, circuit analysis gives us an idea of the inductance
[00:04:17:118 - 00:04:17:600] **Speaker 0:** value.
[00:04:18:808 - 00:04:21:359] **Speaker 0:** Uh, now we need to see once we've designed that
[00:04:21:359 - 00:04:25:209] **Speaker 0:** as far as the converted needs, needs to have, how
[00:04:25:209 - 00:04:26:850] **Speaker 0:** do we actually build it in the real world?
[00:04:27:010 - 00:04:28:709] **Speaker 0:** How do we design that inductor?
[00:04:30:029 - 00:04:33:989] **Speaker 0:** Right, so, that's what we're going to basically uh work
[00:04:33:989 - 00:04:37:049] **Speaker 0:** through for the rest of the the uh lecture.
[00:04:37:390 - 00:04:41:209] **Speaker 0:** So, we have, I'm just going to draw um the
[00:04:41:220 - 00:04:43:670] **Speaker 0:** the most simple form of an inductor that we might
[00:04:43:670 - 00:04:46:630] **Speaker 0:** have, which is just a coil of wire around some
[00:04:46:630 - 00:04:48:350] **Speaker 0:** sort of um core material.
[00:04:48:779 - 00:04:51:410] **Speaker 0:** So, that's that diagram that I did last time.
[00:04:55:230 - 00:05:03:690] **Speaker 0:** Alright, so there are In turns to this inductor.
[00:05:07:109 - 00:05:10:609] **Speaker 0:** So Faraday's law tells us that if there's a flux.
[00:05:12:679 - 00:05:14:820] **Speaker 0:** Uh, linking through that coil.
[00:05:15:619 - 00:05:19:649] **Speaker 0:** So The fluxes going through that, um.
[00:05:20:619 - 00:05:24:279] **Speaker 0:** Then the voltage that's, uh, induced.
[00:05:27:399 - 00:05:32:170] **Speaker 0:** is equal to N, the number of turns defined by
[00:05:32:170 - 00:05:32:630] **Speaker 0:** DT.
[00:05:33:899 - 00:05:35:019] **Speaker 0:** That's paradise law.
[00:05:37:220 - 00:05:37:410] **Speaker 0:** Right.
[00:05:39:670 - 00:05:40:829] **Speaker 0:** What do I mean by being induced?
[00:05:40:880 - 00:05:41:899] **Speaker 0:** That's what we see.
[00:05:43:290 - 00:05:47:010] **Speaker 0:** Across the open terminals of that uh conductor.
[00:05:54:480 - 00:05:57:950] **Speaker 0:** Um, now, if we consider the magnetic circuit that could
[00:05:57:950 - 00:06:02:140] **Speaker 0:** be associated with our inductor, we've already stated that phi
[00:06:02:140 - 00:06:05:440] **Speaker 0:** is equal, the flux is equal to NI over R,
[00:06:05:609 - 00:06:06:369] **Speaker 0:** the reluctance.
[00:06:08:570 - 00:06:12:109] **Speaker 0:** So Just expanding on that, we would say that the
[00:06:12:109 - 00:06:17:390] **Speaker 0:** voltage on our inductor is equal to n.
[00:06:18:920 - 00:06:22:679] **Speaker 0:** D by DT, OK, this is, this is phi of
[00:06:22:920 - 00:06:24:410] **Speaker 0:** NI over R.
[00:06:26:329 - 00:06:30:929] **Speaker 0:** But the number of turns in our Inductor doesn't change
[00:06:30:929 - 00:06:35:190] **Speaker 0:** dynamically with time, so that's a constant and the reluctance
[00:06:35:190 - 00:06:38:339] **Speaker 0:** of the magnetic circuit, the dimensions of the circuit are
[00:06:38:339 - 00:06:41:589] **Speaker 0:** not changing either, right, so that's another constant.
[00:06:41:670 - 00:06:43:230] **Speaker 0:** So we can pull that out of the derivatives, the
[00:06:43:230 - 00:06:45:130] **Speaker 0:** only thing that's changing is the current.
[00:06:46:470 - 00:06:49:309] **Speaker 0:** So, if we pull in over R out of there
[00:06:49:309 - 00:06:51:609] **Speaker 0:** then we end up with N squad.
[00:06:53:109 - 00:06:56:149] **Speaker 0:** Over R DI by DT.
[00:07:03:019 - 00:07:06:459] **Speaker 0:** What's the other expression we know that relates voltage across
[00:07:06:459 - 00:07:09:899] **Speaker 0:** an inductor to a rate of change of current?
[00:07:12:149 - 00:07:14:920] **Speaker 0:** That must then also be equal to.
[00:07:15:760 - 00:07:18:019] **Speaker 0:** L DI by DT.
[00:07:20:260 - 00:07:23:160] **Speaker 0:** Voltage across an inductor equals LDI by DT.
[00:07:23:220 - 00:07:25:799] **Speaker 0:** We've been using that all the time with our analysis.
[00:07:34:140 - 00:07:39:100] **Speaker 0:** So By this equivalence, this must mean.
[00:07:40:040 - 00:07:42:700] **Speaker 0:** That L is equal to N2 over R.
[00:07:43:940 - 00:07:44:869] **Speaker 0:** For our inductor.
[00:07:46:410 - 00:07:50:320] **Speaker 0:** So we're starting to relate something which exists as um
[00:07:50:649 - 00:07:55:429] **Speaker 0:** an on paper analysis value to something that we can
[00:07:55:649 - 00:07:57:809] **Speaker 0:** think of existing in the real world.
[00:08:00:130 - 00:08:02:450] **Speaker 0:** Right, we'll call that equation 2.
[00:08:08:209 - 00:08:11:130] **Speaker 0:** Uh, for our inductive design, we've got the following things
[00:08:11:130 - 00:08:12:809] **Speaker 0:** to work with, the following parameters.
[00:08:13:089 - 00:08:17:850] **Speaker 0:** So, um, I and L are defined by the circuit
[00:08:17:850 - 00:08:19:070] **Speaker 0:** analysis that we're doing.
[00:08:20:000 - 00:08:20:200] **Speaker 0:** Right.
[00:08:29:579 - 00:08:38:888] **Speaker 0:** You Um, the maximum flux density that we have inside
[00:08:38:888 - 00:08:42:968] **Speaker 0:** the core of our inductor, that's the parameter that's defined
[00:08:42:968 - 00:08:47:989] **Speaker 0:** effectively by um the choice of core material and size.
[00:08:48:528 - 00:08:51:189] **Speaker 0:** Alright, so this is material properties.
[00:08:53:349 - 00:08:55:369] **Speaker 0:** Or is set by material properties.
[00:09:01:169 - 00:09:03:090] **Speaker 0:** Where we want to avoid saturation.
[00:09:12:570 - 00:09:18:090] **Speaker 0:** Um, area, A is here is, is identified the cross-sectional
[00:09:18:090 - 00:09:21:890] **Speaker 0:** area associated with our inductor and N is the number
[00:09:21:890 - 00:09:26:070] **Speaker 0:** of turns, right, so this will end up defining the
[00:09:26:080 - 00:09:29:690] **Speaker 0:** the physical size of our inductor.
[00:09:39:229 - 00:09:43:429] **Speaker 0:** And of course we've got the reluctance, um, so that
[00:09:43:429 - 00:09:46:510] **Speaker 0:** comes out of looking at the the physical arrangement of
[00:09:46:510 - 00:09:50:270] **Speaker 0:** the inductor again and the magnetic circuit that is created.
[00:10:02:890 - 00:10:05:940] **Speaker 0:** Uh, so that's the magnetic circuit, so we have the
[00:10:05:940 - 00:10:08:119] **Speaker 0:** core and the air gap.
[00:10:13:719 - 00:10:15:969] **Speaker 0:** That's the circuit that we looked at just in the
[00:10:15:969 - 00:10:16:929] **Speaker 0:** very last lecture.
[00:10:24:169 - 00:10:27:719] **Speaker 0:** OK, so We're getting up to the stage now where
[00:10:27:719 - 00:10:30:919] **Speaker 0:** we can really start honing in on what are the
[00:10:30:919 - 00:10:32:340] **Speaker 0:** important things for our design.
[00:10:35:349 - 00:10:37:770] **Speaker 0:** Right, so in the case of the solar car project.
[00:10:39:059 - 00:10:43:599] **Speaker 0:** We've, we've constrained you, which simplifies the design somewhat.
[00:10:44:099 - 00:10:47:500] **Speaker 0:** Um, you need to use the inductive core that we
[00:10:47:500 - 00:10:51:659] **Speaker 0:** have defined and we'll be providing to you, so this
[00:10:51:659 - 00:10:52:599] **Speaker 0:** core here.
[00:10:55:419 - 00:10:59:049] **Speaker 0:** Um, that then will give you a starting point for
[00:10:59:049 - 00:11:01:010] **Speaker 0:** the design process that you go through.
[00:11:03:729 - 00:11:04:640] **Speaker 0:** Right, so.
[00:11:06:320 - 00:11:09:150] **Speaker 0:** For the actual physical design, of course you on paper,
[00:11:09:239 - 00:11:13:000] **Speaker 0:** you figure out what you want that inductance value to
[00:11:13:000 - 00:11:14:119] **Speaker 0:** be in the first place.
[00:11:18:469 - 00:11:22:630] **Speaker 0:** So, we can just, just for now reluctance, we can
[00:11:22:630 - 00:11:25:510] **Speaker 0:** eliminate reluctance from our expressions, but we have to come
[00:11:25:510 - 00:11:29:909] **Speaker 0:** back to it because the inductor exists in the real
[00:11:29:909 - 00:11:32:590] **Speaker 0:** world and there will be reluctance associated with that that
[00:11:32:590 - 00:11:36:109] **Speaker 0:** determines the overall magnetic circuit um properties.
[00:11:36:979 - 00:11:39:760] **Speaker 0:** So, but for now, we can eliminate it from our
[00:11:39:760 - 00:11:45:849] **Speaker 0:** equations, we'll put, Equation one Into 2.
[00:11:48:349 - 00:11:56:359] **Speaker 0:** And that gives us L will be equal to N2BA
[00:11:56:659 - 00:11:58:020] **Speaker 0:** over NI.
[00:11:59:400 - 00:12:02:919] **Speaker 0:** Right, OK, the N squared and the ends cancel and
[00:12:02:919 - 00:12:04:320] **Speaker 0:** we're left with N.
[00:12:05:809 - 00:12:06:960] **Speaker 0:** BA over I.
[00:12:13:429 - 00:12:16:450] **Speaker 0:** Uh, we can do some rearranging, um, and we'll pull
[00:12:16:450 - 00:12:21:280] **Speaker 0:** together the number of turns and the, um, area, cross-sectional
[00:12:21:280 - 00:12:22:599] **Speaker 0:** area of the core.
[00:12:22:880 - 00:12:25:640] **Speaker 0:** Why have I now started doing a suffix of E?
[00:12:27:030 - 00:12:31:789] **Speaker 0:** Well, AE is just meaning the effective cross-sectional area of
[00:12:31:789 - 00:12:32:409] **Speaker 0:** the core.
[00:12:37:429 - 00:12:40:710] **Speaker 0:** Um, I'll be showing you the data sheet associated with,
[00:12:40:820 - 00:12:43:830] **Speaker 0:** with the core that you will be using, um, and
[00:12:43:830 - 00:12:46:820] **Speaker 0:** it is identified in there what the effect of cross-sectional
[00:12:46:820 - 00:12:47:530] **Speaker 0:** area is.
[00:12:47:869 - 00:12:50:989] **Speaker 0:** It takes into account the entire closed loop of the
[00:12:50:989 - 00:12:55:469] **Speaker 0:** magnetic, uh, circuit that is formed by that core and
[00:12:55:469 - 00:12:58:890] **Speaker 0:** understanding that the geometry of that core has some slightly
[00:12:58:890 - 00:13:02:950] **Speaker 0:** narrower and slightly wider paths for the for the cross-sectional
[00:13:02:950 - 00:13:03:369] **Speaker 0:** area.
[00:13:04:130 - 00:13:06:809] **Speaker 0:** Alright, so overall for the closed loop, then the effective
[00:13:06:809 - 00:13:09:309] **Speaker 0:** cross-sectional area is a particular value.
[00:13:10:950 - 00:13:15:669] **Speaker 0:** Uh, right, so then the product between the uh number
[00:13:15:669 - 00:13:18:849] **Speaker 0:** of turns in the area, um, will be a minimum.
[00:13:19:270 - 00:13:24:080] **Speaker 0:** It it providing you uh identify what the maximum current
[00:13:24:580 - 00:13:29:530] **Speaker 0:** you're expecting is and also defining the maximum flux density
[00:13:30:270 - 00:13:32:349] **Speaker 0:** that will be allowable in the core.
[00:13:35:690 - 00:13:38:909] **Speaker 0:** So this determines uh the inductor effective size.
[00:13:58:500 - 00:14:02:809] **Speaker 0:** Um, so we will be choosing, uh, suitable values for,
[00:14:02:869 - 00:14:06:369] **Speaker 0:** um, the maximum flux density and the current.
[00:14:07:369 - 00:14:12:239] **Speaker 0:** Um And we'll get up to identifying what the number
[00:14:12:239 - 00:14:16:570] **Speaker 0:** of turns are required in the um inductor.
[00:14:19:200 - 00:14:22:729] **Speaker 0:** And because of that we will end up um also
[00:14:22:729 - 00:14:27:780] **Speaker 0:** knowing that we have L equals N2 over R.
[00:14:29:140 - 00:14:32:820] **Speaker 0:** So once we've designed to the number of turns, we
[00:14:32:820 - 00:14:35:099] **Speaker 0:** can come back to the fact that we know what
[00:14:35:099 - 00:14:37:340] **Speaker 0:** conductance we have, we know what number of turns we
[00:14:37:340 - 00:14:41:859] **Speaker 0:** have, so that will dictate what we must make sure
[00:14:41:859 - 00:14:44:239] **Speaker 0:** the reluctance of that magnetic circuit is.
[00:15:07:159 - 00:15:08:820] **Speaker 0:** I don't need the is on that, do I?
[00:15:09:239 - 00:15:11:820] **Speaker 0:** Just calculate the required magnetic reluctance.
[00:15:17:849 - 00:15:21:919] **Speaker 0:** So, the design process, if you follow the process, you
[00:15:21:919 - 00:15:23:340] **Speaker 0:** can, you can't really go wrong.
[00:15:24:309 - 00:15:27:669] **Speaker 0:** So, if you, if you try to kind of circumvent
[00:15:27:669 - 00:15:29:869] **Speaker 0:** parts of it, then you might have some issues with
[00:15:29:869 - 00:15:30:830] **Speaker 0:** your physical design.
[00:15:33:789 - 00:15:39:140] **Speaker 0:** Alright, so Step one, do your circuit analysis, it's going
[00:15:39:140 - 00:15:41:780] **Speaker 0:** to define what value of inductor you're trying to design
[00:15:41:780 - 00:15:46:659] **Speaker 0:** to, um, right, that, uh, will give us that that
[00:15:46:659 - 00:15:50:859] **Speaker 0:** L, um, the design process will also tell us not
[00:15:50:859 - 00:15:56:239] **Speaker 0:** only what L is, but what your inductor peak current
[00:15:56:239 - 00:15:56:739] **Speaker 0:** is.
[00:15:59:309 - 00:16:00:900] **Speaker 0:** Alright, so what is the peak current?
[00:16:04:460 - 00:16:07:520] **Speaker 0:** We've been through this diagram a few times now, right?
[00:16:08:140 - 00:16:11:260] **Speaker 0:** That's the sort of current ripple that you'll be expecting,
[00:16:11:539 - 00:16:12:760] **Speaker 0:** so the peak current.
[00:16:13:500 - 00:16:15:260] **Speaker 0:** is the very peak of that.
[00:16:19:989 - 00:16:23:320] **Speaker 0:** Oh Oh yeah, I can just see that.
[00:16:28:059 - 00:16:30:289] **Speaker 0:** Then we go through the next step is to calculate
[00:16:30:289 - 00:16:32:299] **Speaker 0:** the turn area product that's the NA.
[00:16:34:020 - 00:16:38:210] **Speaker 0:** Then, once we have that and from that the number
[00:16:38:210 - 00:16:41:330] **Speaker 0:** of turns that we want, um, we need to make
[00:16:41:330 - 00:16:45:330] **Speaker 0:** sure that we've got an appropriate wire thickness, um, that's
[00:16:45:330 - 00:16:48:070] **Speaker 0:** the cross-sectional area or effectively the diameter.
[00:16:54:559 - 00:16:57:880] **Speaker 0:** that can carry the RMS current that's going to be
[00:16:58:770 - 00:17:00:809] **Speaker 0:** Flowing in that conductor.
[00:17:02:940 - 00:17:06:900] **Speaker 0:** Then we, you assess core sizes, um, to see what
[00:17:06:900 - 00:17:07:599] **Speaker 0:** would work.
[00:17:08:010 - 00:17:12:050] **Speaker 0:** So a bigger core, you've got A certain amount of
[00:17:12:050 - 00:17:14:569] **Speaker 0:** energy that you want to uh to store, you're going
[00:17:14:569 - 00:17:19:170] **Speaker 0:** to have to um go with a bigger physical size
[00:17:19:170 - 00:17:21:530] **Speaker 0:** of that core for the for the more energy that
[00:17:21:530 - 00:17:21:989] **Speaker 0:** you need.
[00:17:23:339 - 00:17:25:900] **Speaker 0:** You've been, like I said, you've been constrained, you've been
[00:17:25:900 - 00:17:29:260] **Speaker 0:** told what your core must be for, for use in
[00:17:29:260 - 00:17:29:939] **Speaker 0:** the project.
[00:17:31:180 - 00:17:35:500] **Speaker 0:** Then, um, you, uh, calculate the required air gap to
[00:17:35:500 - 00:17:39:219] **Speaker 0:** make sure that that reluctance value that satisfies, um, the
[00:17:39:219 - 00:17:40:420] **Speaker 0:** expression is met.
[00:17:43:439 - 00:17:44:510] **Speaker 0:** And then you're basically done.
[00:17:44:780 - 00:17:47:160] **Speaker 0:** You, you've got everything you need to go and physically
[00:17:47:160 - 00:17:48:060] **Speaker 0:** build your inductor.
[00:17:48:810 - 00:17:52:599] **Speaker 0:** So we'll go through a representative design process just to
[00:17:52:599 - 00:17:53:750] **Speaker 0:** show you step by step how we achieve this.
[00:17:57:770 - 00:18:01:290] **Speaker 0:** Um, the first thing, because I'll be referring to it
[00:18:01:290 - 00:18:04:079] **Speaker 0:** a bit, is just have a quick look at the
[00:18:04:079 - 00:18:06:369] **Speaker 0:** relevant parts of the data sheet for the core.
[00:18:09:819 - 00:18:13:750] **Speaker 0:** Um, so you'll need to know what is the um
[00:18:13:750 - 00:18:18:520] **Speaker 0:** cross-sectional area for this core, the effective uh cross-sectional area
[00:18:18:660 - 00:18:20:819] **Speaker 0:** which is identified here.
[00:18:22:000 - 00:18:26:260] **Speaker 0:** Right, so that's given as 63 millimetres squared.
[00:18:27:979 - 00:18:31:229] **Speaker 0:** Do not confuse this with the minimum area, as I
[00:18:31:229 - 00:18:33:790] **Speaker 0:** said, this has to do with the geometry of the
[00:18:33:790 - 00:18:33:949] **Speaker 0:** core.
[00:18:34:030 - 00:18:37:949] **Speaker 0:** There are parts of the core that the cross-section area
[00:18:37:949 - 00:18:40:930] **Speaker 0:** just diminishes a little bit for a very, very small
[00:18:40:930 - 00:18:45:010] **Speaker 0:** length, um, so that's what's being identified there.
[00:18:45:609 - 00:18:48:089] **Speaker 0:** It's the effective area that you're working to for the,
[00:18:48:189 - 00:18:49:189] **Speaker 0:** um, design.
[00:18:50:859 - 00:18:54:619] **Speaker 0:** The permeability, of course that comes into into play for
[00:18:54:619 - 00:19:02:339] **Speaker 0:** the calculations, so the permeability of this material um The
[00:19:02:339 - 00:19:04:599] **Speaker 0:** bulk material is 1600.
[00:19:05:060 - 00:19:05:569] **Speaker 0:** That's the mir.
[00:19:21:099 - 00:19:24:739] **Speaker 0:** We've also got um an effective length.
[00:19:26:260 - 00:19:30:619] **Speaker 0:** So this is the length of the magnetic circuit for
[00:19:30:619 - 00:19:31:900] **Speaker 0:** this particular core.
[00:19:32:380 - 00:19:36:319] **Speaker 0:** So the effective length is identified as being 38.4 millimetres.
[00:19:37:180 - 00:19:37:949] **Speaker 0:** So what do we mean by that?
[00:19:38:030 - 00:19:40:069] **Speaker 0:** It's the magnetic flux closed loop.
[00:19:40:430 - 00:19:45:189] **Speaker 0:** So the effective loop length that you would go.
[00:19:46:619 - 00:19:50:560] **Speaker 0:** Around each Limb and through the core.
[00:19:52:180 - 00:19:54:900] **Speaker 0:** OK, so that has a linked L associated with it.
[00:20:01:780 - 00:20:02:180] **Speaker 0:** Alright.
[00:20:06:469 - 00:20:10:219] **Speaker 0:** Uh, and the final thing to, to pay particular attention
[00:20:10:219 - 00:20:12:560] **Speaker 0:** to here is the flux density.
[00:20:13:810 - 00:20:17:290] **Speaker 0:** So whilst it's not immediately obvious from the way that
[00:20:17:290 - 00:20:19:349] **Speaker 0:** the figures are presented.
[00:20:20:469 - 00:20:23:250] **Speaker 0:** What the core that we've got is the 3C90.
[00:20:29:239 - 00:20:33:699] **Speaker 0:** Don't worry about the um the forcing uh the forcing
[00:20:33:699 - 00:20:36:939] **Speaker 0:** the force, magnetic force, um or the frequency, temperature.
[00:20:38:069 - 00:20:42:380] **Speaker 0:** What we're seeing here is that it's saying effectively that
[00:20:42:380 - 00:20:47:520] **Speaker 0:** we are looking at no more than 320 milli Tesla
[00:20:47:520 - 00:20:48:199] **Speaker 0:** before we hit.
[00:20:48:989 - 00:20:51:670] **Speaker 0:** The curving part of the BH curve to go into
[00:20:51:670 - 00:20:52:430] **Speaker 0:** saturation.
[00:21:07:810 - 00:21:10:739] **Speaker 0:** Alright, so that's what we take, that's the takeaway from
[00:21:10:739 - 00:21:14:540] **Speaker 0:** that um that value there is that when we do
[00:21:14:540 - 00:21:18:060] **Speaker 0:** our design we better make sure we don't get anywhere
[00:21:18:060 - 00:21:22:219] **Speaker 0:** close to 320 millers otherwise we could start moving into
[00:21:22:219 - 00:21:24:219] **Speaker 0:** saturation areas.
[00:21:26:069 - 00:21:26:969] **Speaker 0:** We don't want that.
[00:21:28:569 - 00:21:30:709] **Speaker 0:** I'll be coming back to this a few times, so.
[00:21:33:170 - 00:21:36:369] **Speaker 0:** Just to remind us what some, what some values are.
[00:21:39:540 - 00:21:41:439] **Speaker 0:** Alright, so the design process.
[00:21:56:630 - 00:22:01:130] **Speaker 0:** First up, one, I'll, I'll throw in some values.
[00:22:01:290 - 00:22:04:410] **Speaker 0:** These are just supposed to be representative, they're not the
[00:22:04:410 - 00:22:07:069] **Speaker 0:** values that you'll end up with for your design.
[00:22:24:189 - 00:22:27:800] **Speaker 0:** Alright, so let's say circuit analysis has given us um
[00:22:28:079 - 00:22:29:939] **Speaker 0:** the average output current.
[00:22:31:170 - 00:22:32:630] **Speaker 0:** Is equal to 1 amp.
[00:22:35:910 - 00:22:38:170] **Speaker 0:** The peak to peak.
[00:22:39:209 - 00:22:43:630] **Speaker 0:** Current ripple Oops, I should really go eye peak to
[00:22:43:630 - 00:22:47:270] **Speaker 0:** peak, um, is 200 milliamps.
[00:22:50:430 - 00:22:53:630] **Speaker 0:** And Because of the frequency that you've got and the
[00:22:53:630 - 00:22:58:310] **Speaker 0:** duty ratio, uh, the load conditions, you've got, you've determined
[00:22:58:310 - 00:23:01:650] **Speaker 0:** that the inductive value that you need is equal to
[00:23:01:939 - 00:23:02:349] **Speaker 0:** one.
[00:23:03:290 - 00:23:04:069] **Speaker 0:** Millie Henry.
[00:23:10:290 - 00:23:12:010] **Speaker 0:** So we'd end up with something.
[00:23:17:579 - 00:23:20:640] **Speaker 0:** That kind of looks like this where you average eye
[00:23:20:640 - 00:23:20:650] **Speaker 0:** out.
[00:23:23:130 - 00:23:24:420] **Speaker 0:** Is equal to one amp.
[00:23:25:150 - 00:23:29:969] **Speaker 0:** And we peak And bottom, so delta.
[00:23:32:189 - 00:23:33:589] **Speaker 0:** IL is 200.
[00:23:34:910 - 00:23:40:660] **Speaker 0:** Milliams So we would peak at what current?
[00:23:40:880 - 00:23:42:689] **Speaker 0:** What's our peak inductor current?
[00:23:48:819 - 00:23:50:290] **Speaker 0:** It's too early in the morning for this.
[00:23:51:400 - 00:23:52:609] **Speaker 0:** 1.1, yeah.
[00:23:54:510 - 00:23:56:719] **Speaker 0:** 1.1 amps is our peak.
[00:23:57:880 - 00:23:57:890] **Speaker 0:** Right.
[00:24:01:280 - 00:24:11:979] **Speaker 0:** So that was 12 Turns area product Alright, so we've
[00:24:11:979 - 00:24:19:630] **Speaker 0:** got In A equivalent or effective, sorry, um, and the
[00:24:19:630 - 00:24:25:290] **Speaker 0:** minimum value of that is equal to LI max over
[00:24:25:290 - 00:24:26:329] **Speaker 0:** B max.
[00:24:31:819 - 00:24:33:420] **Speaker 0:** Well, we know IMAX.
[00:24:35:140 - 00:24:37:380] **Speaker 0:** Is this equals 1.1 amps.
[00:24:38:520 - 00:24:39:160] **Speaker 0:** BMX.
[00:24:42:250 - 00:24:44:989] **Speaker 0:** Right, so we've said you do not go over.
[00:24:47:270 - 00:24:48:910] **Speaker 0:** 320 milli Tesla.
[00:24:51:439 - 00:24:54:030] **Speaker 0:** Just to give you a bit of design headroom in
[00:24:54:030 - 00:24:56:630] **Speaker 0:** case you get things a little bit wrong, um, I
[00:24:56:630 - 00:25:00:510] **Speaker 0:** recommend going no larger in your design than 300 milli-Henry,
[00:25:00:670 - 00:25:02:250] **Speaker 0:** um, um, milli Tesla.
[00:25:08:959 - 00:25:12:160] **Speaker 0:** Right, it gives you a decent amount of excess flux
[00:25:12:160 - 00:25:15:560] **Speaker 0:** density that you could um get into should things.
[00:25:16:430 - 00:25:18:469] **Speaker 0:** Not be quite too designed when you build it.
[00:25:23:650 - 00:25:25:780] **Speaker 0:** All right, so if that's the case, if that's what
[00:25:25:780 - 00:25:26:400] **Speaker 0:** we've chosen.
[00:25:37:790 - 00:25:42:229] **Speaker 0:** That's 1 by 10 to -3, so it's 1 milli
[00:25:42:229 - 00:25:42:729] **Speaker 0:** Henry.
[00:25:44:540 - 00:25:45:420] **Speaker 0:** 1.1.
[00:25:46:599 - 00:25:48:790] **Speaker 0:** Over 0.3.
[00:25:51:020 - 00:25:57:119] **Speaker 0:** That gives us 3.7 by 10 to -3 turns metres
[00:25:57:300 - 00:25:58:020] **Speaker 0:** squared.
[00:26:03:959 - 00:26:06:920] **Speaker 0:** So AE is fixed.
[00:26:14:099 - 00:26:17:660] **Speaker 0:** Alright, and That's equal to.
[00:26:20:760 - 00:26:22:260] **Speaker 0:** 63 mm squared.
[00:26:27:270 - 00:26:31:810] **Speaker 0:** So 63 by 10 need SI units, 10 to -6.
[00:26:32:609 - 00:26:33:369] **Speaker 0:** metres squared.
[00:26:45:540 - 00:26:47:500] **Speaker 0:** Right, so what is that, what are the number of
[00:26:47:500 - 00:26:50:760] **Speaker 0:** turns that we can use uh or need to think
[00:26:50:760 - 00:26:53:300] **Speaker 0:** at a minimum for our, our core.
[00:26:53:619 - 00:26:56:520] **Speaker 0:** So we've got, we just do some rearranging, so in
[00:26:56:739 - 00:27:06:739] **Speaker 0:** min is equal to In a A Over AE Which
[00:27:06:739 - 00:27:10:579] **Speaker 0:** is equal to 3.7 by 10.
[00:27:11:439 - 00:27:16:660] **Speaker 0:** To the -3, divided by 63 by 10 to -6.
[00:27:20:319 - 00:27:23:800] **Speaker 0:** Equals 58.2 turns.
[00:27:26:959 - 00:27:29:270] **Speaker 0:** Alright, it'd be interesting to see someone try to go,
[00:27:29:699 - 00:27:32:670] **Speaker 0:** you know, 56, 57, 58.
[00:27:33:660 - 00:27:38:050] **Speaker 0:** Went to We don't, we don't do partial turns on,
[00:27:38:130 - 00:27:42:810] **Speaker 0:** on these things, um, so you round it up this
[00:27:42:810 - 00:27:46:089] **Speaker 0:** value to the nearest integer or even a bit more
[00:27:46:089 - 00:27:51:229] **Speaker 0:** to give again some headroom for non-deal, uh, elements to
[00:27:51:229 - 00:27:54:449] **Speaker 0:** do with your your physical construction of your inductor.
[00:27:57:739 - 00:28:01:979] **Speaker 0:** So, we'd say, Uh, roundup.
[00:28:04:800 - 00:28:06:619] **Speaker 0:** Never down, and up.
[00:28:16:469 - 00:28:20:109] **Speaker 0:** To the nearest integer, at the very least or potentially
[00:28:20:109 - 00:28:20:530] **Speaker 0:** higher.
[00:28:28:750 - 00:28:34:060] **Speaker 0:** Um We'll choose 60 turns.
[00:28:50:109 - 00:28:51:670] **Speaker 0:** Alright, so step 3.
[00:28:54:439 - 00:29:00:089] **Speaker 0:** Boy, this is getting Step 3 is minimum conductor size.
[00:29:11:500 - 00:29:13:180] **Speaker 0:** Um, this actually depends.
[00:29:14:550 - 00:29:16:390] **Speaker 0:** On a few things, um.
[00:29:21:709 - 00:29:22:760] **Speaker 0:** Someone said, oh no.
[00:29:23:930 - 00:29:25:489] **Speaker 0:** Depends on a few things that you don't have to
[00:29:25:489 - 00:29:27:770] **Speaker 0:** worry too much about, honestly, um.
[00:29:28:689 - 00:29:32:729] **Speaker 0:** So, you know, you could be, uh, depends on the
[00:29:32:729 - 00:29:37:089] **Speaker 0:** insulation that's being used, how deeply embedded the winding is
[00:29:37:089 - 00:29:39:729] **Speaker 0:** within say multiple layers of turns and so forth.
[00:29:40:010 - 00:29:41:900] **Speaker 0:** Um, I'm going to give you a little bit of
[00:29:41:900 - 00:29:47:329] **Speaker 0:** an easy out for this, um, and say that you
[00:29:47:329 - 00:29:47:930] **Speaker 0:** don't.
[00:29:49:390 - 00:29:54:359] **Speaker 0:** Exceed Um, about 5 amps per millimetre squared.
[00:29:57:119 - 00:29:59:180] **Speaker 0:** For current in your winding.
[00:30:00:560 - 00:30:09:079] **Speaker 0:** Um, so, so if we had Uh, one amp RMS.
[00:30:13:910 - 00:30:16:130] **Speaker 0:** That would mean that you have a wire.
[00:30:17:119 - 00:30:18:979] **Speaker 0:** With an area.
[00:30:20:869 - 00:30:23:410] **Speaker 0:** greater than 0.2 millimetres squared.
[00:30:27:109 - 00:30:30:260] **Speaker 0:** Alright, so that's the cross-sectional area of that wire, um,
[00:30:30:319 - 00:30:32:180] **Speaker 0:** for the 5 amps per millimetre squared.
[00:30:33:459 - 00:30:36:000] **Speaker 0:** Then that gives us a diameter.
[00:30:38:989 - 00:30:43:290] **Speaker 0:** That has to be greater than 0.5 millimetres.
[00:30:44:050 - 00:30:46:449] **Speaker 0:** It's not a very thick wire, and that, and that
[00:30:46:449 - 00:30:49:689] **Speaker 0:** takes an amp RMS continuous.
[00:30:56:689 - 00:30:59:609] **Speaker 0:** That's a kind of like the limit of, of the,
[00:30:59:699 - 00:31:00:250] **Speaker 0:** the size.
[00:31:00:369 - 00:31:06:050] **Speaker 0:** What, why would we maybe choose a wire diameter that
[00:31:06:050 - 00:31:11:050] **Speaker 0:** is greater than 0.5, maybe 0.7 millimetres diameter, even up
[00:31:11:050 - 00:31:12:390] **Speaker 0:** to 1 millimetre diameter.
[00:31:12:530 - 00:31:16:099] **Speaker 0:** Why would we choose a greater wire diameter than The
[00:31:16:099 - 00:31:16:689] **Speaker 0:** minimum.
[00:31:19:369 - 00:31:20:130] **Speaker 0:** Spot on.
[00:31:20:459 - 00:31:22:699] **Speaker 0:** So yeah, so the answer there was that it would
[00:31:22:699 - 00:31:25:540] **Speaker 0:** be a lower resistance for the length of wire that
[00:31:25:540 - 00:31:29:260] **Speaker 0:** you're using, which means that the resistive loss in that
[00:31:29:260 - 00:31:32:020] **Speaker 0:** inductor is lower, helps with efficiency.
[00:31:32:770 - 00:31:35:530] **Speaker 0:** There is a slight trade-off, there's more weight, alright, and
[00:31:35:530 - 00:31:38:609] **Speaker 0:** this is a cart that you're trying to accelerate as
[00:31:38:609 - 00:31:42:729] **Speaker 0:** fast as possible, but the weight for the, the size
[00:31:42:729 - 00:31:46:339] **Speaker 0:** of the inductor relative to the physical weight of the,
[00:31:46:479 - 00:31:49:670] **Speaker 0:** the cart, it's not really a big difference percentage wise.
[00:31:55:500 - 00:31:55:859] **Speaker 0:** Right.
[00:32:05:229 - 00:32:06:199] **Speaker 0:** Step 4.
[00:32:08:599 - 00:32:11:280] **Speaker 0:** Will it, will those turns fit on the core?
[00:32:27:949 - 00:32:32:380] **Speaker 0:** Right, we've got Those, if I can kind of zoom
[00:32:32:380 - 00:32:32:819] **Speaker 0:** in a bit.
[00:32:36:349 - 00:32:37:849] **Speaker 0:** And refocus.
[00:32:40:619 - 00:32:41:060] **Speaker 0:** There we go.
[00:32:42:459 - 00:32:45:540] **Speaker 0:** Um, so those, all those turns that we just said
[00:32:45:540 - 00:32:47:579] **Speaker 0:** have got to be able to fit within the, within
[00:32:47:579 - 00:32:51:300] **Speaker 0:** the volume available inside the core there.
[00:32:51:739 - 00:32:54:680] **Speaker 0:** So you have a little plastic bobbin that you wind
[00:32:54:680 - 00:32:57:859] **Speaker 0:** the the turns onto, um, will it actually fit in
[00:32:57:859 - 00:32:59:560] **Speaker 0:** that in that available volume?
[00:33:05:719 - 00:33:10:099] **Speaker 0:** Um Technically, if we were going through a full, uh
[00:33:10:099 - 00:33:13:420] **Speaker 0:** full blown design process, we might use a packing equation.
[00:33:32:060 - 00:33:34:859] **Speaker 0:** So a packing equation will take into consideration the wire
[00:33:34:859 - 00:33:39:819] **Speaker 0:** diameter, the, um, the thickness of the insulation around the
[00:33:39:819 - 00:33:48:489] **Speaker 0:** wire, uh, how, um, Uh, circular or effectively cylindrical objects
[00:33:48:489 - 00:33:52:219] **Speaker 0:** can pack against each other, um, on multiple layers.
[00:33:54:030 - 00:33:57:270] **Speaker 0:** It turns into quite the thing, but we don't need
[00:33:57:270 - 00:33:58:930] **Speaker 0:** to worry about that for our design.
[00:33:59:660 - 00:34:02:839] **Speaker 0:** Uh I can tell you that if you're doing your
[00:34:02:839 - 00:34:10:040] **Speaker 0:** design right, um, and you've got The right sort of
[00:34:10:040 - 00:34:13:719] **Speaker 0:** parameters involved in your inductor level design, whatever number of
[00:34:13:719 - 00:34:18:080] **Speaker 0:** turns you come up with will definitely fit in the
[00:34:18:080 - 00:34:19:239] **Speaker 0:** volume available.
[00:34:19:989 - 00:34:24:638] **Speaker 0:** If you've got something like 500 turns for, for your
[00:34:24:638 - 00:34:26:540] **Speaker 0:** inductor, something's gone wrong.
[00:34:31:668 - 00:34:32:839] **Speaker 0:** Or the wire is too thick.
[00:34:34:179 - 00:34:36:189] **Speaker 0:** Again, if you say have.
[00:34:37:138 - 00:34:40:059] **Speaker 0:** 20 or 30 turns and you go right, I'm going
[00:34:40:059 - 00:34:43:539] **Speaker 0:** to take my lecturer's advice and I'm going to put
[00:34:43:539 - 00:34:48:218] **Speaker 0:** in, you know, a 5 millimetre diameter wire in there.
[00:34:48:529 - 00:34:51:339] **Speaker 0:** Good luck in trying to bend that um but it
[00:34:51:339 - 00:34:54:948] **Speaker 0:** won't fit, of course, but within the realms of the
[00:34:54:948 - 00:35:00:559] **Speaker 0:** currents that are expected for driving the motor, um, then.
[00:35:01:399 - 00:35:04:159] **Speaker 0:** You should be able to choose a wire diameter with
[00:35:04:159 - 00:35:05:679] **Speaker 0:** the number of turns that you come up with that
[00:35:05:679 - 00:35:08:399] **Speaker 0:** easily fit within that that volume.
[00:35:09:439 - 00:35:13:449] **Speaker 0:** Again, if it doesn't, you've done something wrong, like choose
[00:35:13:449 - 00:35:15:689] **Speaker 0:** a ridiculously large wire diameter.
[00:35:22:060 - 00:35:23:239] **Speaker 0:** Uh, right, so.
[00:35:45:840 - 00:35:47:459] **Speaker 0:** Alright, 5.
[00:35:48:840 - 00:35:49:280] **Speaker 0:** Oops.
[00:35:52:810 - 00:35:56:189] **Speaker 0:** That's uh calculate the necessary reluctance.
[00:35:59:649 - 00:36:01:969] **Speaker 0:** This is the, the trickiest bit of the whole design,
[00:36:02:010 - 00:36:02:409] **Speaker 0:** I think.
[00:36:18:620 - 00:36:28:340] **Speaker 0:** Right, um, so we have L equals N2 over R.
[00:36:29:429 - 00:36:32:909] **Speaker 0:** So we've already determined what is the, the number of
[00:36:32:909 - 00:36:34:669] **Speaker 0:** turns that we've got for our inductor.
[00:36:36:030 - 00:36:39:610] **Speaker 0:** So that's equal to 60 squared over.
[00:36:41:510 - 00:36:42:080] **Speaker 0:** Ah, sorry.
[00:36:42:959 - 00:36:46:939] **Speaker 0:** So I Equals N2 over L.
[00:36:49:000 - 00:36:54:840] **Speaker 0:** Right, this is 60 2 over the inductive um value
[00:36:54:840 - 00:36:56:659] **Speaker 0:** which is 1 by 10 to -3.
[00:37:00:949 - 00:37:03:649] **Speaker 0:** Equals 3.6 by 106.
[00:37:08:600 - 00:37:10:280] **Speaker 0:** Amp turns per Weber.
[00:37:15:459 - 00:37:17:739] **Speaker 0:** Right, so now if the core is made from this
[00:37:17:739 - 00:37:20:370] **Speaker 0:** ferrite material that we've just identified that has a mir
[00:37:20:370 - 00:37:21:939] **Speaker 0:** of 1600.
[00:37:23:520 - 00:37:25:959] **Speaker 0:** We've got R equals.
[00:37:26:770 - 00:37:29:350] **Speaker 0:** L over mm.
[00:37:31:280 - 00:37:32:120] **Speaker 0:** AE.
[00:37:33:580 - 00:37:41:229] **Speaker 0:** So rearranging Gives us L equals the reluctance times mm.
[00:37:42:780 - 00:37:50:899] **Speaker 0:** I eat With mu 0 equals 4 by 10 to
[00:37:50:899 - 00:37:51:679] **Speaker 0:** -7.
[00:37:52:919 - 00:37:56:360] **Speaker 0:** And new are equals from the data sheet that we
[00:37:56:360 - 00:37:59:159] **Speaker 0:** went over before uh 1600.
[00:38:05:010 - 00:38:09:610] **Speaker 0:** Let's just say that we are able to um construct
[00:38:09:610 - 00:38:14:129] **Speaker 0:** our inductor and we clamp it up so that The
[00:38:14:129 - 00:38:19:489] **Speaker 0:** whole magnetic circuit just looks like the ferrite material.
[00:38:20:399 - 00:38:23:500] **Speaker 0:** Right, so we've essentially eliminated the air gap by making
[00:38:23:500 - 00:38:27:399] **Speaker 0:** sure it was nice and firmly clamped together um between
[00:38:27:399 - 00:38:28:120] **Speaker 0:** the two halves.
[00:38:29:110 - 00:38:38:120] **Speaker 0:** Then The L With No ear gap.
[00:38:40:750 - 00:38:47:500] **Speaker 0:** L will equal 3.6 by 106, the reluctance value.
[00:38:49:159 - 00:38:55:030] **Speaker 0:** Uh, 4 by 10 to -7 times 1600 and you
[00:38:55:030 - 00:38:58:659] **Speaker 0:** are 63 by 106.
[00:38:59:939 - 00:39:00:739] **Speaker 0:** Equals.
[00:39:03:090 - 00:39:06:149] **Speaker 0:** 0.46 metres.
[00:39:10:399 - 00:39:15:639] **Speaker 0:** The magnetic circuit equivalent length for our core is.
[00:39:16:530 - 00:39:18:080] **Speaker 0:** 38 millimetres.
[00:39:21:550 - 00:39:22:989] **Speaker 0:** There's a little bit of a difference there.
[00:39:24:120 - 00:39:28:830] **Speaker 0:** Um, in fact, if you have to have that effective
[00:39:28:830 - 00:39:30:760] **Speaker 0:** length in your core.
[00:39:31:550 - 00:39:36:929] **Speaker 0:** Um, using that ferrite material, you would end up With
[00:39:37:510 - 00:39:39:129] **Speaker 0:** a core of that size.
[00:39:40:389 - 00:39:42:719] **Speaker 0:** That's the dimensions that you end up with the magnetic
[00:39:42:719 - 00:39:44:189] **Speaker 0:** path length that we have.
[00:39:44:669 - 00:39:44:760] **Speaker 0:** Um.
[00:39:47:780 - 00:39:50:479] **Speaker 0:** A little bit of a mismatch there on what's practical
[00:39:50:479 - 00:39:52:899] **Speaker 0:** for putting on your uh your converter.
[00:39:53:260 - 00:39:56:280] **Speaker 0:** Um, so of course we've got to do something here
[00:39:56:459 - 00:39:58:419] **Speaker 0:** that deals with this.
[00:40:04:580 - 00:40:08:060] **Speaker 0:** Uh, and that thing that we do is we make
[00:40:08:060 - 00:40:10:469] **Speaker 0:** sure there is an air gap.
[00:40:36:709 - 00:40:38:510] **Speaker 0:** So we need to introduce this air gap.
[00:40:47:290 - 00:40:49:729] **Speaker 0:** Alright, so what we're talking about there.
[00:40:51:239 - 00:40:52:909] **Speaker 0:** Is um.
[00:40:55:219 - 00:40:59:500] **Speaker 0:** Having our core, so I'll, I'll draw it as because
[00:40:59:500 - 00:41:01:860] **Speaker 0:** it's easier to draw this way, just like uh what
[00:41:01:860 - 00:41:14:580] **Speaker 0:** we call an ecore, so And bring the two halves
[00:41:14:620 - 00:41:16:250] **Speaker 0:** of that together.
[00:41:26:149 - 00:41:27:780] **Speaker 0:** Alright, where we have the flux.
[00:41:34:290 - 00:41:38:219] **Speaker 0:** Circulating around the two limbs from the central core.
[00:41:40:060 - 00:41:46:550] **Speaker 0:** So we have LG, which is the air gap.
[00:41:51:290 - 00:41:55:250] **Speaker 0:** That's the model and the magnetic circuit that we went
[00:41:55:250 - 00:41:57:149] **Speaker 0:** through effectively in the last lecture.
[00:41:58:159 - 00:42:01:600] **Speaker 0:** So we already know from that uh analysis that we
[00:42:01:600 - 00:42:03:340] **Speaker 0:** did that the air gap.
[00:42:15:479 - 00:42:18:179] **Speaker 0:** Right, the air gap dominates the overall reluctance value.
[00:42:19:919 - 00:42:24:199] **Speaker 0:** To the extent that we can effectively ignore the contribution
[00:42:24:199 - 00:42:28:520] **Speaker 0:** of reluctance by the core and just do the magnetic
[00:42:28:520 - 00:42:30:649] **Speaker 0:** circuit analysis with the air gap.
[00:42:35:590 - 00:42:39:120] **Speaker 0:** So R, the reluctance is equal to.
[00:42:39:820 - 00:42:45:439] **Speaker 0:** L Over m0 AE.
[00:42:46:120 - 00:42:49:370] **Speaker 0:** Alright, so just new naught now because it's the air
[00:42:49:370 - 00:42:52:290] **Speaker 0:** gap which has a relative permeability of one.
[00:42:58:010 - 00:43:01:030] **Speaker 0:** The L, though, since the flux.
[00:43:02:419 - 00:43:04:800] **Speaker 0:** The flux passes through the air gap.
[00:43:05:820 - 00:43:08:790] **Speaker 0:** Once And then twice.
[00:43:09:729 - 00:43:14:320] **Speaker 0:** The overall L of the magnetic circuit involving the air
[00:43:14:810 - 00:43:16:979] **Speaker 0:** is 2 times the air gap.
[00:43:32:060 - 00:43:36:050] **Speaker 0:** That's equal to RU0 AE.
[00:43:38:530 - 00:43:46:270] **Speaker 0:** Alright, so equals 3.6 by 106 times 0.
[00:43:49:510 - 00:43:51:090] **Speaker 0:** Times the equivalent.
[00:43:52:270 - 00:43:56:689] **Speaker 0:** Area 63 by 10 to -6 equals.
[00:43:57:350 - 00:44:00:850] **Speaker 0:** 285 microns.
[00:44:05:139 - 00:44:09:100] **Speaker 0:** So, the LG is half that.
[00:44:10:379 - 00:44:11:610] **Speaker 0:** To 85.
[00:44:13:729 - 00:44:16:389] **Speaker 0:** 2 is 142.
[00:44:17:389 - 00:44:23:149] **Speaker 0:** Microns Hm 142 microns.
[00:44:23:189 - 00:44:27:389] **Speaker 0:** Is there something practical or every day that we experience
[00:44:27:389 - 00:44:29:709] **Speaker 0:** that might give us an idea of what sort of
[00:44:29:709 - 00:44:30:949] **Speaker 0:** thickness that is?
[00:44:31:270 - 00:44:31:909] **Speaker 0:** Uh, yeah.
[00:44:34:719 - 00:44:38:820] **Speaker 0:** Our standard paper that we use is about that thick.
[00:44:40:610 - 00:44:46:050] **Speaker 0:** Alright, so a piece of paper in thickness is sufficient
[00:44:46:370 - 00:44:48:350] **Speaker 0:** for our air gap.
[00:45:09:389 - 00:45:15:979] **Speaker 0:** So we would construct then our Inductor, uh, with the
[00:45:15:979 - 00:45:18:860] **Speaker 0:** number of turns that we've defined, um, but before we
[00:45:18:860 - 00:45:22:540] **Speaker 0:** put the two halves together, we make sure that we've
[00:45:22:540 - 00:45:28:780] **Speaker 0:** got something to keep the two halves separated so that
[00:45:28:780 - 00:45:30:780] **Speaker 0:** the reluctance requirement is met.
[00:45:32:010 - 00:45:38:159] **Speaker 0:** And That's what we've got with this core in between
[00:45:38:159 - 00:45:42:020] **Speaker 0:** is a piece of paper on the surfaces of the
[00:45:42:020 - 00:45:43:020] **Speaker 0:** um the halves.
[00:45:51:949 - 00:45:57:919] **Speaker 0:** Thing to consider here, um, so the reluctance in the
[00:45:57:919 - 00:46:02:479] **Speaker 0:** amount of, uh, MMF that gets, uh, or the, the
[00:46:02:479 - 00:46:06:719] **Speaker 0:** amount of, yeah, MMF that gets dropped across the reluctance
[00:46:06:719 - 00:46:09:489] **Speaker 0:** as we go through a magnetic path, um.
[00:46:10:260 - 00:46:12:239] **Speaker 0:** Is proportional to the amount of energy.
[00:46:13:189 - 00:46:17:840] **Speaker 0:** That's stored Think of it like a resistive circuit again,
[00:46:17:919 - 00:46:21:580] **Speaker 0:** you have a um a voltage source, a small resistance,
[00:46:21:669 - 00:46:22:719] **Speaker 0:** and a large resistance.
[00:46:22:800 - 00:46:26:199] **Speaker 0:** That large resistance takes all of that voltage drop around
[00:46:26:199 - 00:46:27:179] **Speaker 0:** the closed circuit.
[00:46:27:600 - 00:46:31:790] **Speaker 0:** If you've got current flowing, then because that resistor is
[00:46:31:790 - 00:46:34:600] **Speaker 0:** taking virtually all the voltage, and you've got the current,
[00:46:34:790 - 00:46:39:199] **Speaker 0:** voltage times current means power and it's dissipating that power
[00:46:39:199 - 00:46:39:760] **Speaker 0:** as heat.
[00:46:40:810 - 00:46:42:979] **Speaker 0:** But all of the energy then for the, for that
[00:46:42:979 - 00:46:46:320] **Speaker 0:** circuit is associated with that large resistance.
[00:46:47:540 - 00:46:52:699] **Speaker 0:** Similarly, with the magnetic circuit, all of the energy associated
[00:46:52:699 - 00:46:57:919] **Speaker 0:** with storing the energy from the flux is, is attributed
[00:46:57:919 - 00:47:00:219] **Speaker 0:** to the reluctance.
[00:47:00:780 - 00:47:02:979] **Speaker 0:** So we've got the reluctance being dominated by the air
[00:47:02:979 - 00:47:03:300] **Speaker 0:** gap.
[00:47:04:729 - 00:47:09:280] **Speaker 0:** Which means when we have that constant current and or
[00:47:09:699 - 00:47:12:580] **Speaker 0:** the, the ramping up current, so we're imparting energy to
[00:47:12:580 - 00:47:13:439] **Speaker 0:** our inductor.
[00:47:14:280 - 00:47:15:879] **Speaker 0:** And then we have the energy coming out of the
[00:47:15:879 - 00:47:17:939] **Speaker 0:** inductor with the ramping down part of the current.
[00:47:18:830 - 00:47:26:020] **Speaker 0:** That energy Is stored in that inductor, predominantly in the
[00:47:26:020 - 00:47:26:540] **Speaker 0:** air gap.
[00:47:28:649 - 00:47:33:310] **Speaker 0:** So, all of the energy that we've got is located
[00:47:33:860 - 00:47:39:350] **Speaker 0:** within 120 or 130 micron zone within that core.
[00:47:40:590 - 00:47:43:350] **Speaker 0:** Alright, so, it's a bit of a, bit of a
[00:47:43:350 - 00:47:46:060] **Speaker 0:** weird thing to think that virtually all of the bulk
[00:47:46:060 - 00:47:50:629] **Speaker 0:** of that that inductor contains no energy, only that fractionally
[00:47:50:629 - 00:47:51:389] **Speaker 0:** small air gap.
[00:47:53:610 - 00:47:54:070] **Speaker 0:** Yes.
[00:47:54:590 - 00:47:55:300] **Speaker 0:** Doesn't the paper.
[00:47:58:580 - 00:48:07:939] **Speaker 0:** Yeah, it's, uh, things like paper, unless it's ferromagnetic, it
[00:48:07:939 - 00:48:11:179] **Speaker 0:** has effective permeability of around one.
[00:48:11:659 - 00:48:16:679] **Speaker 0:** Yeah, yeah, and with less than one?
[00:48:17:659 - 00:48:17:989] **Speaker 0:** No.
[00:48:20:020 - 00:48:24:260] **Speaker 0:** No, that would be a metamaterial that might exist within
[00:48:24:260 - 00:48:28:580] **Speaker 0:** the quantum realm, but not, not normal material, yeah.
[00:48:30:909 - 00:48:31:909] **Speaker 0:** Any other questions?
[00:48:32:229 - 00:48:32:750] **Speaker 0:** This is good.
[00:48:35:129 - 00:48:38:560] **Speaker 0:** No, oh well, well, it's basically time, so that's it
[00:48:38:560 - 00:48:39:070] **Speaker 0:** for today.

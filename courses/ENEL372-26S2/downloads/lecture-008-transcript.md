# ENEL372-26S2 Lecture 8 native Echo transcript

Date: July 30, 2026 3:00pm-3:55pm
Transcript type: native Echo automated transcript.

[00:00:00:439 - 00:00:02:930] **Speaker 0:** I know.
[00:00:05:119 - 00:00:05:769] **Speaker 0:** You do.
[00:00:10:710 - 00:00:10:720] **Speaker 0:** Yeah.
[00:00:20:659 - 00:00:20:670] **Speaker 0:** OK.
[00:00:23:219 - 00:00:25:399] **Speaker 0:** very good.
[00:00:25:409 - 00:00:26:700] **Speaker 0:** The first thing I say.
[00:00:27:440 - 00:00:27:450] **Speaker 0:** Yeah.
[00:00:31:540 - 00:00:33:319] **Speaker 1:** Right, Kyorakoto, welcome along.
[00:00:33:860 - 00:00:35:159] **Speaker 1:** Hang on, is that on?
[00:00:36:200 - 00:00:36:209] **Speaker 1:** Oh.
[00:00:39:060 - 00:00:40:040] **Speaker 1:** Kyorakoto, welcome along.
[00:00:40:159 - 00:00:41:310] **Speaker 1:** Oh, yeah, now it's on.
[00:00:41:639 - 00:00:43:770] **Speaker 1:** Alright, I'll turn that down a little bit.
[00:00:47:150 - 00:00:47:790] **Speaker 1:** All right.
[00:00:48:189 - 00:00:53:689] **Speaker 1:** OK, so, today, we're gonna move into looking at uh
[00:00:54:340 - 00:00:58:909] **Speaker 1:** elements to do with uh the magnetics involved with para
[00:00:58:909 - 00:00:59:740] **Speaker 1:** electronics.
[00:00:59:990 - 00:01:03:349] **Speaker 1:** Now, magnetics and para electronics is probably one of the
[00:01:03:349 - 00:01:08:389] **Speaker 1:** key areas that um enable the, the, the device or
[00:01:08:389 - 00:01:10:849] **Speaker 1:** the power electronics that we're designing to work the way
[00:01:11:029 - 00:01:12:250] **Speaker 1:** that we want it to.
[00:01:12:620 - 00:01:17:470] **Speaker 1:** Um, your, uh, foray into, into the magnetics of power
[00:01:17:470 - 00:01:20:940] **Speaker 1:** electronics will be in the design and construction of your
[00:01:20:940 - 00:01:22:720] **Speaker 1:** power inductor for the back converter.
[00:01:23:099 - 00:01:26:389] **Speaker 1:** Um, but before we get to that point of going
[00:01:26:389 - 00:01:30:540] **Speaker 1:** through the design, um, uh, process that you that you
[00:01:30:540 - 00:01:34:379] **Speaker 1:** should employ for the power inductor, um, let's get a,
[00:01:34:529 - 00:01:37:720] **Speaker 1:** a, a pretty decent idea of what's going on, um,
[00:01:37:779 - 00:01:39:819] **Speaker 1:** with regards to the magnetic components.
[00:01:41:209 - 00:01:43:760] **Speaker 1:** Now, just before we we get into even that, I
[00:01:43:760 - 00:01:48:610] **Speaker 1:** just wanted to show the internal workings of um a
[00:01:48:610 - 00:01:50:529] **Speaker 1:** little bit of an older power supply now, but it
[00:01:50:529 - 00:01:54:389] **Speaker 1:** is still a power supply which employs power electronics, um,
[00:01:54:410 - 00:01:57:349] **Speaker 1:** as its main operational um function.
[00:01:57:769 - 00:02:01:650] **Speaker 1:** So it takes in AC either from, uh, and this
[00:02:01:650 - 00:02:03:930] **Speaker 1:** one, it's quite power electronics can be very versatile.
[00:02:03:970 - 00:02:07:730] **Speaker 1:** It doesn't matter if it's Uh, 60Hz, 110 volts from
[00:02:07:730 - 00:02:11:399] **Speaker 1:** the US system or 230 volts, um, 60 uh 50
[00:02:11:399 - 00:02:15:289] **Speaker 1:** Hz, uh, from, um, European and and, uh, New Zealand
[00:02:15:289 - 00:02:15:850] **Speaker 1:** system.
[00:02:16:289 - 00:02:19:929] **Speaker 1:** Takes that in, does its power electronic conversion and outputs
[00:02:19:929 - 00:02:23:149] **Speaker 1:** either plus 15 volts, minus 15 volts or 24 volts,
[00:02:23:449 - 00:02:27:190] **Speaker 1:** um, all at about 200 watts, um, output power.
[00:02:28:179 - 00:02:30:229] **Speaker 1:** But what I'm getting at here is that, um, whilst
[00:02:30:229 - 00:02:34:149] **Speaker 1:** you've got your standard little capacitors and resistors, um, so
[00:02:34:149 - 00:02:37:339] **Speaker 1:** forth, uh, a few semiconductor devices that do the, the,
[00:02:37:380 - 00:02:40:990] **Speaker 1:** the power switching, um, a big chunk of what's going
[00:02:40:990 - 00:02:42:520] **Speaker 1:** on here is magnetics.
[00:02:42:710 - 00:02:46:070] **Speaker 1:** Um, so the devices that are magnetic within this power
[00:02:46:070 - 00:02:50:669] **Speaker 1:** supply, there's a honking great, um, Uh, inductor in the
[00:02:50:669 - 00:02:51:229] **Speaker 1:** middle here.
[00:02:51:589 - 00:02:55:669] **Speaker 1:** Uh, we've got transformers, we've got another inductor here.
[00:02:56:029 - 00:02:59:369] **Speaker 1:** So all of these here are, are magnetic components.
[00:02:59:630 - 00:03:03:429] **Speaker 1:** And then we've got some, um, Uh, inductors that are
[00:03:03:429 - 00:03:06:630] **Speaker 1:** designed to limit the rate of change of current.
[00:03:06:990 - 00:03:10:509] **Speaker 1:** So these are these kind of funny looking devices here.
[00:03:10:589 - 00:03:13:279] **Speaker 1:** So they're toroidal inductors, right?
[00:03:13:399 - 00:03:17:630] **Speaker 1:** So a big chunk of magnetic material doing a whole
[00:03:17:630 - 00:03:20:630] **Speaker 1:** bunch of work within the converter, um.
[00:03:21:369 - 00:03:24:619] **Speaker 1:** And for the buck converter, it's absolutely necessary to have
[00:03:24:619 - 00:03:27:860] **Speaker 1:** that power inducted to store energy and release it in
[00:03:27:860 - 00:03:30:919] **Speaker 1:** the manner that we need for our, our converter operation.
[00:03:34:309 - 00:03:41:220] **Speaker 1:** So For the type of material that we're talking about,
[00:03:41:309 - 00:03:43:350] **Speaker 1:** that's magnetics, if we're looking at this at a, at
[00:03:43:350 - 00:03:48:389] **Speaker 1:** a more classical physics space, um, magnetic fields will be
[00:03:48:389 - 00:03:51:149] **Speaker 1:** created whenever there's moving electric charge.
[00:03:52:119 - 00:03:55:729] **Speaker 1:** All right, so, often we consider that moving electric charge
[00:03:55:729 - 00:03:59:029] **Speaker 1:** in the form of electrical current, you know, um, with
[00:03:59:029 - 00:04:01:330] **Speaker 1:** electrical systems, it's not a big stretch.
[00:04:01:690 - 00:04:07:929] **Speaker 1:** Uh, so, for example, a coil, um, of wire carrying
[00:04:07:929 - 00:04:08:529] **Speaker 1:** a current.
[00:04:17:440 - 00:04:21:359] **Speaker 1:** So, I'm just going to draw this rather symbolically, so.
[00:04:23:869 - 00:04:26:630] **Speaker 1:** This is a coil which you can imagine some sort
[00:04:26:630 - 00:04:30:829] **Speaker 1:** of um core material that it's wrapping itself around so
[00:04:30:829 - 00:04:32:589] **Speaker 1:** you can see it at the front but not the
[00:04:32:589 - 00:04:32:970] **Speaker 1:** back.
[00:04:35:709 - 00:04:40:809] **Speaker 1:** Uh, and we have current flowing, uh, in this way
[00:04:41:029 - 00:04:44:329] **Speaker 1:** and therefore is out that way.
[00:04:45:769 - 00:04:48:089] **Speaker 1:** If we have current flowing in a coil like that,
[00:04:48:290 - 00:04:50:670] **Speaker 1:** uh, what we tend to find is that we have,
[00:04:50:690 - 00:04:54:670] **Speaker 1:** uh, flux generated and the flux wraps itself.
[00:04:56:269 - 00:05:00:149] **Speaker 1:** Around the coil, uh, with this being the north end
[00:05:00:149 - 00:05:01:269] **Speaker 1:** and this being the south end.
[00:05:01:670 - 00:05:02:809] **Speaker 1:** How did I come to that?
[00:05:03:109 - 00:05:05:649] **Speaker 1:** Well, there's kind of various rules that you can follow
[00:05:05:649 - 00:05:09:630] **Speaker 1:** with the, with regards to Magnetic fields being generated from,
[00:05:09:690 - 00:05:11:410] **Speaker 1:** um, from currents.
[00:05:11:609 - 00:05:14:570] **Speaker 1:** It's the right-hand rule is usually employed.
[00:05:14:850 - 00:05:17:160] **Speaker 1:** So what I've, hey, you can determine that as you
[00:05:17:160 - 00:05:20:410] **Speaker 1:** wrap your finger fingers around in the of your right
[00:05:20:410 - 00:05:23:450] **Speaker 1:** hand in the direction of the current, which is around
[00:05:23:450 - 00:05:26:850] **Speaker 1:** that way, and your thumb will point to the north
[00:05:26:850 - 00:05:29:489] **Speaker 1:** end of the flux that's being generated.
[00:05:35:649 - 00:05:39:269] **Speaker 1:** Right, um, but that's in the more traditional classic sense,
[00:05:39:450 - 00:05:39:859] **Speaker 1:** um.
[00:05:40:850 - 00:05:46:510] **Speaker 1:** We can also look down at the individual atom level,
[00:05:46:839 - 00:05:50:359] **Speaker 1:** um, and see how magnetic fields might be associated with,
[00:05:50:369 - 00:05:53:600] **Speaker 1:** uh, the specific, um, atoms.
[00:05:53:929 - 00:05:58:480] **Speaker 1:** Um, If we then consider electron spin.
[00:05:59:750 - 00:06:05:140] **Speaker 1:** of any unpaired electrons in the atom, then In a
[00:06:05:140 - 00:06:07:859] **Speaker 1:** particular unfilled shell that can result in a net magnetic
[00:06:07:859 - 00:06:10:839] **Speaker 1:** field for the particular atom.
[00:06:11:220 - 00:06:14:720] **Speaker 1:** And I think it won't come as a big surprise
[00:06:14:720 - 00:06:20:660] **Speaker 1:** that, that iron, uh has a quite substantial magnetic field
[00:06:20:660 - 00:06:21:570] **Speaker 1:** associated with it.
[00:06:21:700 - 00:06:25:769] **Speaker 1:** It's the strongest, well, it's a ferromagnetic material, where we,
[00:06:25:859 - 00:06:29:660] **Speaker 1:** we get the name ferromagnetic, magnetic because of the big
[00:06:29:660 - 00:06:30:880] **Speaker 1:** effect that we have with iron.
[00:06:32:980 - 00:06:35:739] **Speaker 1:** So iron has 4 unpaired electrons in its outer shell,
[00:06:36:019 - 00:06:38:579] **Speaker 1:** so I'm just gonna, uh, draw this in a very,
[00:06:38:820 - 00:06:42:929] **Speaker 1:** again, symbolic way, um, hardly any kind of accuracy.
[00:06:43:019 - 00:06:47:059] **Speaker 1:** So here's the nucleus of our iron atom, um, and
[00:06:47:059 - 00:06:53:720] **Speaker 1:** we've got Electrons in orbital shells.
[00:06:54:790 - 00:06:58:869] **Speaker 1:** Clouds around the, the nucleus, but each of these has
[00:06:58:869 - 00:07:04:269] **Speaker 1:** a spin of the unpaired electrons, all right, so they
[00:07:04:269 - 00:07:08:500] **Speaker 1:** have spin, but a unique property of the iron atom
[00:07:08:500 - 00:07:12:029] **Speaker 1:** is that though, all four of those um electrons have
[00:07:12:029 - 00:07:12:950] **Speaker 1:** the same spin.
[00:07:15:859 - 00:07:18:700] **Speaker 1:** Um, so with that being the case, then what we
[00:07:18:700 - 00:07:22:970] **Speaker 1:** end up conceptualise, if we kind of squint our eyes
[00:07:22:970 - 00:07:24:940] **Speaker 1:** a bit at it, and I think you probably do
[00:07:24:940 - 00:07:27:010] **Speaker 1:** need to do that to see an individual ion atom,
[00:07:27:600 - 00:07:33:820] **Speaker 1:** um, is That an iron atom can behave or appear
[00:07:33:820 - 00:07:37:559] **Speaker 1:** like a little tiny, smallest scale.
[00:07:40:190 - 00:07:43:940] **Speaker 1:** Bar magnet It has a north side and a south
[00:07:43:940 - 00:07:46:500] **Speaker 1:** side because of these electrons all spinning in the same
[00:07:46:500 - 00:07:46:959] **Speaker 1:** direction.
[00:07:47:339 - 00:07:49:779] **Speaker 1:** They cause one side just kind, kind of like we
[00:07:49:779 - 00:07:54:890] **Speaker 1:** had um With our coil, because they're all the electrons
[00:07:54:890 - 00:07:56:489] **Speaker 1:** are all spinning in the same direction, they end up
[00:07:56:489 - 00:07:59:190] **Speaker 1:** with a north end and a south end to the
[00:07:59:570 - 00:08:01:769] **Speaker 1:** each individual iron atom.
[00:08:03:570 - 00:08:10:529] **Speaker 1:** Um, so, what happens for permanent, uh, magnets that have
[00:08:10:529 - 00:08:12:380] **Speaker 1:** a north and a south when they come into close
[00:08:12:380 - 00:08:14:329] **Speaker 1:** proximity with each other.
[00:08:14:649 - 00:08:17:989] **Speaker 1:** So here I've got, um, a magnet, two magnets.
[00:08:18:450 - 00:08:22:079] **Speaker 1:** There's the north side, they, they're constructed so that they're
[00:08:22:079 - 00:08:24:929] **Speaker 1:** actually along the, the, the small axis, the short axis,
[00:08:25:089 - 00:08:26:350] **Speaker 1:** so there's the south side.
[00:08:27:109 - 00:08:29:869] **Speaker 1:** All right, so you would expect if you go like
[00:08:29:869 - 00:08:32:849] **Speaker 1:** poles for a, for a um a magnet like this,
[00:08:33:320 - 00:08:37:510] **Speaker 1:** that it's going to cause, cause it to flip or
[00:08:37:510 - 00:08:38:179] **Speaker 1:** push away.
[00:08:39:169 - 00:08:45:708] **Speaker 1:** As we can Or best laid plans, but if they,
[00:08:45:768 - 00:08:47:429] **Speaker 1:** if you, yeah, it's kind of pushes that away.
[00:08:47:468 - 00:08:49:129] **Speaker 1:** I don't know if you can see that very well.
[00:08:49:969 - 00:08:53:119] **Speaker 1:** But if I flip that around, of course, it's going
[00:08:53:119 - 00:08:55:609] **Speaker 1:** to do the exact opposite and it's gonna want to
[00:08:55:609 - 00:08:56:390] **Speaker 1:** do that.
[00:08:56:849 - 00:09:03:070] **Speaker 1:** All right, forming I, I Um, another effective bar magnet
[00:09:03:070 - 00:09:06:989] **Speaker 1:** now, but now with a stronger magnetic flux associated with
[00:09:06:989 - 00:09:07:359] **Speaker 1:** it.
[00:09:07:909 - 00:09:11:599] **Speaker 1:** So What happens when you bring permanent magnets together, so
[00:09:11:599 - 00:09:17:690] **Speaker 1:** you might have south, north, and As I just had
[00:09:17:690 - 00:09:21:950] **Speaker 1:** in south, north, um, that's going to go and form.
[00:09:24:479 - 00:09:32:219] **Speaker 1:** This overall clicked together with North, south, south, north, but
[00:09:32:219 - 00:09:35:969] **Speaker 1:** with the, the overall effect of bringing those together, of
[00:09:35:969 - 00:09:41:299] **Speaker 1:** having a larger flux associated with those joined together.
[00:09:44:309 - 00:09:47:650] **Speaker 1:** So the net magnetic flux from an individual iron atom
[00:09:47:909 - 00:09:51:210] **Speaker 1:** is strong enough to interact with other close by iron
[00:09:51:750 - 00:09:52:299] **Speaker 1:** neighbours.
[00:09:53:280 - 00:09:56:359] **Speaker 1:** Right, and you, it results in local magnetic force that
[00:09:56:359 - 00:10:00:119] **Speaker 1:** causes alignment of those, uh, of all of those.
[00:10:00:770 - 00:10:09:239] **Speaker 1:** Um Regions Uh, alignment of the atoms and reinforces the
[00:10:09:239 - 00:10:10:479] **Speaker 1:** overall magnetic flux.
[00:10:11:489 - 00:10:15:989] **Speaker 1:** Right, so if you take the iron and construct a
[00:10:15:989 - 00:10:20:650] **Speaker 1:** bulk material from that iron, then um you end up
[00:10:20:650 - 00:10:24:880] **Speaker 1:** with these uh solid materials that have discontinuities throughout the
[00:10:24:880 - 00:10:26:650] **Speaker 1:** bulk of that material.
[00:10:27:330 - 00:10:31:929] **Speaker 1:** Um, where you have local magnetic flux reinforcement within those
[00:10:31:929 - 00:10:32:969] **Speaker 1:** discontinuities.
[00:10:34:049 - 00:10:36:969] **Speaker 1:** Now combined to form the bulk material, each of those
[00:10:36:969 - 00:10:38:909] **Speaker 1:** is known as a domain.
[00:10:39:719 - 00:10:39:950] **Speaker 1:** Right.
[00:10:41:559 - 00:10:46:520] **Speaker 1:** Each domain itself is effectively a little permanent magnet.
[00:10:47:710 - 00:10:50:669] **Speaker 1:** But, uh, in the, in the way that we construct
[00:10:50:669 - 00:10:54:549] **Speaker 1:** the bulk material, each domain, it has a, usually a
[00:10:54:549 - 00:10:56:070] **Speaker 1:** random orientation.
[00:10:56:460 - 00:11:02:409] **Speaker 1:** So let's draw a bulk material, um, which has domains
[00:11:02:619 - 00:11:04:159] **Speaker 1:** uh associated with it.
[00:11:04:590 - 00:11:04:929] **Speaker 1:** So.
[00:11:05:929 - 00:11:09:080] **Speaker 1:** I'm just gonna, it's not completely random, I've already pre-drawn
[00:11:09:080 - 00:11:13:059] **Speaker 1:** this myself, but there are a bunch of domains, um,
[00:11:13:169 - 00:11:19:900] **Speaker 1:** and 1 may have a net flux direction that's like
[00:11:19:900 - 00:11:20:809] **Speaker 1:** that in it.
[00:11:21:159 - 00:11:23:969] **Speaker 1:** Another one that might have a net flux that's like
[00:11:23:969 - 00:11:24:510] **Speaker 1:** this.
[00:11:25:000 - 00:11:29:570] **Speaker 1:** Uh, this one could be quite a different direction, um,
[00:11:30:059 - 00:11:30:669] **Speaker 1:** another one.
[00:11:31:440 - 00:11:33:390] **Speaker 1:** Again, and.
[00:11:34:190 - 00:11:36:989] **Speaker 1:** So, as random as I can sort of show in
[00:11:36:989 - 00:11:38:109] **Speaker 1:** that number of domains.
[00:11:42:320 - 00:11:45:500] **Speaker 1:** Domain magnetic flux direction though can be manipulated.
[00:11:46:409 - 00:11:49:969] **Speaker 1:** If we apply an external magnetic force, and by that
[00:11:49:969 - 00:11:53:530] **Speaker 1:** I mean an external magnetic field, then we can influence
[00:11:53:530 - 00:11:55:229] **Speaker 1:** the direction of those domains.
[00:11:55:809 - 00:12:00:880] **Speaker 1:** So, drawing the same Block of material.
[00:12:02:080 - 00:12:05:039] **Speaker 1:** Which has its specific domains.
[00:12:08:330 - 00:12:12:609] **Speaker 1:** And instead we add And applied magnetic force.
[00:12:13:900 - 00:12:14:830] **Speaker 1:** In this direction.
[00:12:27:320 - 00:12:29:440] **Speaker 1:** Right, if we do that and then we start seeing
[00:12:29:440 - 00:12:32:679] **Speaker 1:** the domains begin to align.
[00:12:33:000 - 00:12:36:359] **Speaker 1:** So this one, this is the direction will be pulled
[00:12:36:359 - 00:12:37:419] **Speaker 1:** more in line.
[00:12:40:070 - 00:12:42:780] **Speaker 1:** This one maybe starts angling a bit more.
[00:12:44:580 - 00:12:47:159] **Speaker 1:** This one has a lot more.
[00:12:48:450 - 00:12:51:299] **Speaker 1:** Uh, rotation to go, so it's not quite aligned.
[00:12:51:700 - 00:12:57:080] **Speaker 1:** This one, from there starts coming out into that direction.
[00:12:58:299 - 00:13:02:500] **Speaker 1:** The bottom one again starts moving around and.
[00:13:03:330 - 00:13:04:760] **Speaker 1:** This one also.
[00:13:05:049 - 00:13:07:729] **Speaker 1:** So a bit of force applied and we start seeing
[00:13:07:729 - 00:13:11:989] **Speaker 1:** a net change in the overall direction of the domains.
[00:13:13:669 - 00:13:16:469] **Speaker 1:** In the end, um, we can get to a point
[00:13:16:469 - 00:13:18:210] **Speaker 1:** if we apply enough force.
[00:13:24:559 - 00:13:35:250] **Speaker 1:** A lot of force, then we can end up, Um,
[00:13:35:450 - 00:13:37:070] **Speaker 1:** completely aligning the domains.
[00:13:37:450 - 00:13:42:909] **Speaker 1:** So they are all exactly in line with the applied
[00:13:43:130 - 00:13:43:710] **Speaker 1:** force.
[00:13:46:809 - 00:13:51:400] **Speaker 1:** So here we have no net direction of the, of
[00:13:51:400 - 00:13:54:210] **Speaker 1:** the flux within the um the material, so there's no
[00:13:54:210 - 00:13:55:450] **Speaker 1:** north-south element.
[00:13:55:770 - 00:13:58:909] **Speaker 1:** Here, you might uh see that there's a little bit
[00:13:58:909 - 00:14:03:849] **Speaker 1:** of a north-south um net result in that material, and
[00:14:03:849 - 00:14:08:369] **Speaker 1:** ultimately you end up with a large north-south um element
[00:14:08:369 - 00:14:11:690] **Speaker 1:** to that material with a lot of um external force
[00:14:11:690 - 00:14:12:429] **Speaker 1:** applied.
[00:14:17:570 - 00:14:23:159] **Speaker 1:** OK, well, What does that kind of mean for using
[00:14:23:380 - 00:14:28:419] **Speaker 1:** these magnetic materials within our power converters or Enabling us
[00:14:28:419 - 00:14:31:760] **Speaker 1:** to store energy within the, within the magnetic material.
[00:14:32:460 - 00:14:36:960] **Speaker 1:** Well, we need to to look at and consider the
[00:14:37:359 - 00:14:43:210] **Speaker 1:** um magnetic flux density versus uh magnetising force curve cause
[00:14:43:210 - 00:14:45:159] **Speaker 1:** this explains a lot to us.
[00:14:53:229 - 00:14:58:020] **Speaker 1:** So Applying external force, so here that's what we're talking
[00:14:58:020 - 00:14:59:020] **Speaker 1:** about with H.
[00:14:59:179 - 00:15:01:559] **Speaker 1:** this is magnetic magnetising force.
[00:15:08:359 - 00:15:09:539] **Speaker 1:** Or a magnetic field.
[00:15:10:489 - 00:15:14:789] **Speaker 1:** Um, and we compare that against flux density.
[00:15:21:380 - 00:15:24:780] **Speaker 1:** Alright, so it's a scaling, uh, with respect to cross-sectional
[00:15:24:780 - 00:15:28:039] **Speaker 1:** area of the amount of flux that we have.
[00:15:28:700 - 00:15:33:500] **Speaker 1:** So units here of Tesla or Tesla.
[00:15:34:780 - 00:15:37:880] **Speaker 1:** Um, or Webers per metre squared.
[00:15:42:150 - 00:15:46:270] **Speaker 1:** Well, how does flux density relate to the magnetic flux
[00:15:46:270 - 00:15:47:700] **Speaker 1:** that we're just talking about?
[00:15:48:030 - 00:15:58:099] **Speaker 1:** So, um, So the flux is phi, so this is
[00:15:58:099 - 00:15:58:700] **Speaker 1:** flux.
[00:15:59:909 - 00:16:03:429] **Speaker 1:** And this is just the area over that that flux
[00:16:03:429 - 00:16:03:890] **Speaker 1:** exists.
[00:16:09:609 - 00:16:13:950] **Speaker 1:** Right, but we're interested in, we're applying an external force.
[00:16:14:289 - 00:16:19:580] **Speaker 1:** How readily do those domains line up with that external
[00:16:19:580 - 00:16:24:210] **Speaker 1:** force, producing larger and larger amounts of flux, and therefore
[00:16:24:210 - 00:16:27:770] **Speaker 1:** given a constant volume of constant area, a larger and
[00:16:27:770 - 00:16:29:330] **Speaker 1:** larger flux density.
[00:16:31:309 - 00:16:32:669] **Speaker 1:** Well, we can.
[00:16:33:510 - 00:16:40:010] **Speaker 1:** Describe that behaviour uh by utilising a um an A
[00:16:40:010 - 00:16:44:830] **Speaker 1:** property known as the relative permeability of the material.
[00:16:45:250 - 00:16:49:940] **Speaker 1:** So that's what m are, uh, stands for, relative permeability.
[00:16:50:489 - 00:16:55:049] **Speaker 1:** So you end up here with B again, is equal
[00:16:55:049 - 00:16:59:590] **Speaker 1:** to mm are times H.
[00:17:02:900 - 00:17:06:400] **Speaker 1:** We're munn, hopefully we've come across this before, that's just
[00:17:06:400 - 00:17:08:839] **Speaker 1:** the permeability of free space.
[00:17:21:989 - 00:17:24:609] **Speaker 1:** Uh, not a great huge quantity.
[00:17:24:650 - 00:17:27:729] **Speaker 1:** That's 4 pi by 10-7.
[00:17:29:219 - 00:17:31:880] **Speaker 1:** Um, and weathers per amp metre.
[00:17:40:030 - 00:17:44:969] **Speaker 1:** It's a 7 Uh, with mir.
[00:17:45:329 - 00:17:48:500] **Speaker 1:** So mir, like I said, is, is a scale or
[00:17:48:500 - 00:17:51:959] **Speaker 1:** a a factor that tells you how readily, um, with
[00:17:51:959 - 00:17:57:089] **Speaker 1:** an applied magnetic force or field that those domains line
[00:17:57:089 - 00:17:57:349] **Speaker 1:** up.
[00:17:58:750 - 00:18:02:959] **Speaker 1:** So a larger value of permeability relative permeability means that
[00:18:02:959 - 00:18:06:439] **Speaker 1:** it's easier to line those domains up.
[00:18:07:199 - 00:18:10:650] **Speaker 1:** Um, what sort of values are we talking about for
[00:18:10:650 - 00:18:13:579] **Speaker 1:** our magnetic materials, materials that we might have?
[00:18:14:239 - 00:18:18:599] **Speaker 1:** Well, in power electronics, because of the frequencies that are
[00:18:18:599 - 00:18:22:640] **Speaker 1:** involved, um, the magnetic material that's primarily used is known
[00:18:22:640 - 00:18:23:359] **Speaker 1:** as ferrite.
[00:18:24:130 - 00:18:26:890] **Speaker 1:** It's not a metal as such.
[00:18:26:959 - 00:18:29:189] **Speaker 1:** It's more like a ceramic in nature.
[00:18:30:130 - 00:18:33:939] **Speaker 1:** But it has loaded into it a lot of um
[00:18:33:939 - 00:18:35:589] **Speaker 1:** ferromagnetic molecules.
[00:18:37:780 - 00:18:38:939] **Speaker 1:** There's a lot of iron in it.
[00:18:40:290 - 00:18:44:199] **Speaker 1:** Um, the other material that we often use for magnetic,
[00:18:44:300 - 00:18:48:380] **Speaker 1:** uh, components is steel of special kinds, all right?
[00:18:48:479 - 00:18:53:140] **Speaker 1:** But steel has a problem with frequency, so it's not
[00:18:53:140 - 00:18:56:939] **Speaker 1:** used in power electronics, it's used down at the um
[00:18:56:939 - 00:18:58:579] **Speaker 1:** power frequency side of things.
[00:18:58:670 - 00:19:03:579] **Speaker 1:** So a few kilohertz down to low frequency, um, of
[00:19:03:579 - 00:19:04:540] **Speaker 1:** just a few hertz.
[00:19:05:869 - 00:19:09:729] **Speaker 1:** So for ferris, the thing that we're primarily interested in.
[00:19:12:550 - 00:19:14:089] **Speaker 0:** Um, new.
[00:19:14:949 - 00:19:19:300] **Speaker 1:** Ah It's bounded by around 300.
[00:19:20:290 - 00:19:22:949] **Speaker 1:** To about 5000.
[00:19:26:239 - 00:19:31:839] **Speaker 1:** Commonly That special steel, or that steel that I said
[00:19:31:839 - 00:19:35:479] **Speaker 1:** that works at lower frequencies for power type systems, um,
[00:19:39:229 - 00:19:39:589] **Speaker 1:** Oops.
[00:19:44:089 - 00:19:49:890] **Speaker 1:** That's a mir of around 77,000.
[00:19:51:790 - 00:19:54:939] **Speaker 1:** So, quite a lot better than ferrite but again it's
[00:19:54:939 - 00:19:58:250] **Speaker 1:** frequency limited, so we don't use it for power electronics.
[00:19:58:729 - 00:20:02:489] **Speaker 1:** Um, and then there's a special stuff called mu metal
[00:20:03:709 - 00:20:07:459] **Speaker 1:** or mu metal, it's mu supposed to be, so that's
[00:20:07:459 - 00:20:08:089] **Speaker 1:** mu metal.
[00:20:13:790 - 00:20:20:550] **Speaker 1:** Um, and that has, uh, a relative permeability that can
[00:20:20:550 - 00:20:29:239] **Speaker 1:** be up to around, um, 100,000.
[00:20:32:300 - 00:20:33:239] **Speaker 1:** Very, very large.
[00:20:34:020 - 00:20:38:469] **Speaker 1:** Um, but again, is, is frequency restricted and it being
[00:20:38:469 - 00:20:41:969] **Speaker 1:** a very, very specialised material is extremely expensive as well.
[00:20:44:250 - 00:20:46:599] **Speaker 1:** OK, so just to give you a ballpark idea of
[00:20:46:599 - 00:20:51:229] **Speaker 1:** what we're talking about for perme relative permeability for ferrites,
[00:20:51:650 - 00:20:53:729] **Speaker 1:** the thing that we find most often used in power
[00:20:53:729 - 00:20:54:449] **Speaker 1:** electronics.
[00:20:55:839 - 00:20:57:079] **Speaker 1:** What is this curve telling us?
[00:20:57:189 - 00:21:00:989] **Speaker 1:** Well, it shows then that we've got a slope here
[00:21:00:989 - 00:21:06:540] **Speaker 1:** where we have a change in um Uh, magnetic magnetising
[00:21:06:540 - 00:21:11:719] **Speaker 1:** force of a In this range, a linearly increasing flux
[00:21:11:719 - 00:21:12:300] **Speaker 1:** density.
[00:21:13:530 - 00:21:19:439] **Speaker 1:** Which has a slope Uh equal to mu naught mr.
[00:21:22:209 - 00:21:26:000] **Speaker 1:** So the larger our muir, the more steep that slope
[00:21:26:000 - 00:21:26:660] **Speaker 1:** will be.
[00:21:27:310 - 00:21:29:959] **Speaker 1:** Means that we don't need as much magnetising force to
[00:21:29:959 - 00:21:33:800] **Speaker 1:** line up those domains, producing a large, uh, flux at
[00:21:33:800 - 00:21:35:260] **Speaker 1:** the ends of that material.
[00:21:37:800 - 00:21:43:939] **Speaker 1:** Highly magnetic But you might notice that as we go
[00:21:43:939 - 00:21:47:819] **Speaker 1:** up in the force, that curves off to the point
[00:21:47:819 - 00:21:49:880] **Speaker 1:** where here the slope.
[00:21:51:099 - 00:21:53:099] **Speaker 1:** is pretty much just new naught.
[00:21:54:650 - 00:21:57:050] **Speaker 1:** Muir drops to being effectively one.
[00:21:57:859 - 00:22:01:180] **Speaker 1:** At high magnetising force.
[00:22:01:880 - 00:22:02:489] **Speaker 1:** Why?
[00:22:03:000 - 00:22:05:800] **Speaker 1:** Well, we've gone and hit this condition.
[00:22:07:619 - 00:22:09:839] **Speaker 1:** We have lined up all the domains as much as
[00:22:09:839 - 00:22:12:689] **Speaker 1:** you can and it does makes absolutely no difference how
[00:22:12:689 - 00:22:15:430] **Speaker 1:** much extra force you apply in that direction.
[00:22:15:619 - 00:22:17:400] **Speaker 1:** You can't line those domains up anymore.
[00:22:19:609 - 00:22:21:609] **Speaker 1:** Alright, so that's what we're seeing here, and that's known
[00:22:21:609 - 00:22:24:109] **Speaker 1:** as saturation of the magnetic material.
[00:22:38:189 - 00:22:40:609] **Speaker 1:** Alright, as soon as it stops being a linear change
[00:22:40:609 - 00:22:42:609] **Speaker 1:** with magnetising force.
[00:22:45:069 - 00:22:48:709] **Speaker 1:** It works both ways as well, so I showed one
[00:22:48:709 - 00:22:49:290] **Speaker 1:** direction.
[00:22:50:180 - 00:22:53:319] **Speaker 1:** Of force If we flipped that on its head and
[00:22:53:319 - 00:22:55:640] **Speaker 1:** had the force the other way, the domains would all
[00:22:55:640 - 00:22:57:699] **Speaker 1:** start lining up in the opposite direction.
[00:22:59:849 - 00:23:01:750] **Speaker 1:** So it's bipolar.
[00:23:02:439 - 00:23:03:680] **Speaker 1:** Has both directions.
[00:23:13:459 - 00:23:17:280] **Speaker 1:** So, if we're going to use this practically, this material,
[00:23:17:380 - 00:23:21:739] **Speaker 1:** uh, and we have this effect of the relative permeability
[00:23:21:739 - 00:23:25:699] **Speaker 1:** essentially decreasing once we get into the saturation zone, we
[00:23:25:699 - 00:23:32:300] **Speaker 1:** tend to only operate uh within The linear region of
[00:23:32:300 - 00:23:33:000] **Speaker 1:** the material.
[00:23:50:709 - 00:23:53:310] **Speaker 1:** So when you get to do your design for your
[00:23:53:310 - 00:23:57:869] **Speaker 1:** power inductor, you'll be looking at certain flux densities within
[00:23:57:869 - 00:24:00:949] **Speaker 1:** the core that must not be exceeded if you want
[00:24:00:949 - 00:24:04:589] **Speaker 1:** to stay within this linear region and not saturate your
[00:24:04:589 - 00:24:04:989] **Speaker 1:** core.
[00:24:06:760 - 00:24:09:400] **Speaker 1:** And I will be explaining why that's a really important
[00:24:09:400 - 00:24:10:640] **Speaker 1:** thing that you should not do.
[00:24:15:119 - 00:24:19:400] **Speaker 1:** OK, so that curve that I just showed, assumes that
[00:24:19:400 - 00:24:23:239] **Speaker 1:** you apply uh some sort of magnetising force, uh, and
[00:24:23:239 - 00:24:26:199] **Speaker 1:** it's just At that value, it doesn't go, it's not
[00:24:26:199 - 00:24:32:739] **Speaker 1:** changing, effectively a constant uh Application of the force.
[00:24:33:949 - 00:24:37:290] **Speaker 1:** But we already know that we change that, don't we?
[00:24:37:339 - 00:24:40:380] **Speaker 1:** We have flux that is changing in the core because
[00:24:40:380 - 00:24:44:800] **Speaker 1:** we're changing current that's in our winding.
[00:24:45:959 - 00:24:48:359] **Speaker 1:** So instead, we need to consider what happens in our
[00:24:48:359 - 00:24:52:339] **Speaker 1:** magnetic material when our magnetising force changes.
[00:24:54:520 - 00:24:56:380] **Speaker 1:** And things get a little more complicated.
[00:25:01:170 - 00:25:02:869] **Speaker 1:** So we've still got our BH curve.
[00:25:03:880 - 00:25:08:939] **Speaker 1:** Um But now we are going to make the magnetising
[00:25:08:939 - 00:25:13:119] **Speaker 1:** force, uh, initially increase in value and then decrease and
[00:25:13:119 - 00:25:14:959] **Speaker 1:** come back to increasing again.
[00:25:15:359 - 00:25:17:359] **Speaker 1:** When I, when I say decrease, we're going from positive
[00:25:17:359 - 00:25:20:800] **Speaker 1:** value of, of magnetising force to a negative value of
[00:25:20:800 - 00:25:21:900] **Speaker 1:** magnetising force.
[00:25:22:400 - 00:25:29:420] **Speaker 1:** So we'll start off assuming that we, everything was Zero.
[00:25:30:040 - 00:25:33:000] **Speaker 1:** So, we're at that point where we've never applied any
[00:25:33:000 - 00:25:36:920] **Speaker 1:** um magnetising force and all the domains are completely randomly
[00:25:36:920 - 00:25:37:500] **Speaker 1:** oriented.
[00:25:39:750 - 00:25:42:869] **Speaker 1:** So there's no flux density within the material.
[00:25:43:689 - 00:25:47:329] **Speaker 1:** Then we apply, um, in the bulk material.
[00:25:47:650 - 00:25:50:369] **Speaker 1:** Then we apply a magnetising force and we start moving
[00:25:50:369 - 00:25:54:010] **Speaker 1:** up that curve just like the previous um curve.
[00:25:54:329 - 00:25:56:089] **Speaker 1:** So here we go, we're moving up, that's why the
[00:25:56:089 - 00:25:57:250] **Speaker 1:** arrows are in this direction.
[00:25:58:530 - 00:26:01:170] **Speaker 1:** We push it into saturation, something we probably shouldn't do,
[00:26:01:410 - 00:26:02:930] **Speaker 1:** but it wouldn't matter if we did that or not,
[00:26:02:969 - 00:26:04:270] **Speaker 1:** it's just illustrative.
[00:26:04:650 - 00:26:06:050] **Speaker 1:** And then we get to a point where we say,
[00:26:06:170 - 00:26:08:709] **Speaker 1:** right, that's as high.
[00:26:09:619 - 00:26:12:380] **Speaker 1:** A force that we're going to apply in this direction,
[00:26:12:619 - 00:26:13:449] **Speaker 1:** we're going to move back.
[00:26:15:250 - 00:26:17:420] **Speaker 1:** Alright, so we're gonna apply less force and less force.
[00:26:17:699 - 00:26:20:260] **Speaker 1:** So those domains that you've all lined up tend to
[00:26:20:260 - 00:26:22:119] **Speaker 1:** revert back to where they were.
[00:26:23:750 - 00:26:31:750] **Speaker 1:** Tend to If you now reverse or reduce that magnetising
[00:26:31:750 - 00:26:33:349] **Speaker 1:** force down to zero.
[00:26:34:050 - 00:26:37:329] **Speaker 1:** You don't come back down here, you end up coming
[00:26:37:329 - 00:26:40:810] **Speaker 1:** down this curve, so that when you're back at 0,
[00:26:40:930 - 00:26:46:270] **Speaker 1:** there is a residual flux density associated with your material.
[00:26:48:040 - 00:26:52:069] **Speaker 1:** What you've done is you've kind of turned that magnetic
[00:26:52:069 - 00:26:57:989] **Speaker 1:** material into a somewhat weak but finite permanent magnet.
[00:26:59:109 - 00:27:01:089] **Speaker 1:** So this is residual flux density.
[00:27:09:349 - 00:27:10:930] **Speaker 1:** That's what it's technically called.
[00:27:11:550 - 00:27:15:670] **Speaker 1:** If you actually want to get those domains back to
[00:27:15:670 - 00:27:19:229] **Speaker 1:** their original state, so that there is no net flux
[00:27:19:229 - 00:27:23:069] **Speaker 1:** density at the ends of that material, then you have
[00:27:23:069 - 00:27:29:910] **Speaker 1:** to put a reverse magnetising force on that material to
[00:27:29:910 - 00:27:32:010] **Speaker 1:** zero that flux.
[00:27:34:030 - 00:27:36:800] **Speaker 1:** This is the point where that occurs.
[00:27:37:270 - 00:27:39:469] **Speaker 1:** The amount of force that you're adding is known as
[00:27:39:469 - 00:27:40:660] **Speaker 1:** the coercive force.
[00:27:42:369 - 00:27:47:170] **Speaker 1:** So this Is coercive.
[00:27:57:109 - 00:28:00:989] **Speaker 1:** Right, but we're going to push that even further, so
[00:28:00:989 - 00:28:04:729] **Speaker 1:** we're going to keep our magnetic flux, uh, magnetic force,
[00:28:04:869 - 00:28:09:589] **Speaker 1:** uh, increasing in a reverse sense, uh, so we keep
[00:28:09:589 - 00:28:10:709] **Speaker 1:** following this curve.
[00:28:11:890 - 00:28:15:219] **Speaker 1:** Along this pathway, and then we go, right, we're gonna
[00:28:15:219 - 00:28:15:640] **Speaker 1:** come back.
[00:28:16:699 - 00:28:19:800] **Speaker 1:** So we come back and we move along this path.
[00:28:21:900 - 00:28:25:390] **Speaker 1:** Again, ending up by the time you get back to
[00:28:25:390 - 00:28:27:849] **Speaker 1:** 0 with a residual flux density.
[00:28:32:339 - 00:28:34:670] **Speaker 1:** Residual, um, which is of the same.
[00:28:36:099 - 00:28:39:099] **Speaker 1:** Magnitude as it was in the in the previous case.
[00:28:39:180 - 00:28:41:099] **Speaker 1:** It's just now in the opposite direction.
[00:28:43:050 - 00:28:46:250] **Speaker 1:** Once again, to zero the flux in the, in that
[00:28:46:250 - 00:28:51:530] **Speaker 1:** material, you have to use uh a A magnetic force
[00:28:51:709 - 00:28:52:869] **Speaker 1:** that is positive.
[00:28:53:109 - 00:28:55:729] **Speaker 1:** So again, your coercive force.
[00:29:04:280 - 00:29:13:319] **Speaker 1:** So, by cycling through positive and negative magnetic force, you
[00:29:13:319 - 00:29:17:199] **Speaker 1:** end up, whether you go into saturation or not, you
[00:29:17:199 - 00:29:21:380] **Speaker 1:** end up um cycling around this curve.
[00:29:22:630 - 00:29:26:069] **Speaker 1:** All right, which doesn't pass through the centre or the
[00:29:26:069 - 00:29:27:109] **Speaker 1:** zero, the origin.
[00:29:30:260 - 00:29:37:699] **Speaker 1:** Um, because it takes energy to align the domains, they
[00:29:37:699 - 00:29:40:099] **Speaker 1:** don't, it just doesn't, it just, they don't align for
[00:29:40:099 - 00:29:40:420] **Speaker 1:** nothing.
[00:29:40:500 - 00:29:42:420] **Speaker 1:** If they did, then they would be moving all the
[00:29:42:420 - 00:29:45:880] **Speaker 1:** time, um, irrespective of what you're doing to it.
[00:29:46:260 - 00:29:49:939] **Speaker 1:** They take energy to align them and then to bring
[00:29:49:939 - 00:29:52:199] **Speaker 1:** them back and to another alignment.
[00:29:52:660 - 00:29:56:400] **Speaker 1:** So what we find is that the area encapsulated by
[00:29:56:400 - 00:29:59:160] **Speaker 1:** this curve, which is known as a hysteresis curve.
[00:29:59:630 - 00:30:00:650] **Speaker 1:** For the magnetic material.
[00:30:01:030 - 00:30:04:810] **Speaker 1:** The area encapsulated is the energy lost.
[00:30:15:170 - 00:30:20:959] **Speaker 1:** Right, so utilising magnetic material in this AC or bipolar
[00:30:20:959 - 00:30:25:250] **Speaker 1:** nature means that we are introducing loss, right?
[00:30:25:329 - 00:30:27:229] **Speaker 1:** So it's not a perfect material.
[00:30:28:349 - 00:30:32:270] **Speaker 1:** And that's an inefficiency associated with the material itself.
[00:30:34:810 - 00:30:41:310] **Speaker 1:** Um, and you Cycle around this once every cycle of
[00:30:41:310 - 00:30:41:609] **Speaker 1:** operation.
[00:30:42:229 - 00:30:45:989] **Speaker 1:** So if we're operating at a particular frequency, if we,
[00:30:46:060 - 00:30:49:369] **Speaker 1:** if we go up in frequency, we cycle around this
[00:30:49:750 - 00:30:56:449] **Speaker 1:** more frequently and therefore introduce more loss with increasing frequency.
[00:30:56:810 - 00:30:58:930] **Speaker 1:** It's one of those factors that I was talking about
[00:30:59:510 - 00:31:02:989] **Speaker 1:** for picking a sweet spot for switching frequency in our
[00:31:02:989 - 00:31:04:949] **Speaker 1:** power, power electronic converters.
[00:31:12:780 - 00:31:14:310] **Speaker 1:** Right, so.
[00:31:15:939 - 00:31:20:180] **Speaker 1:** That's not the only loss mechanism in uh a, a
[00:31:20:180 - 00:31:24:699] **Speaker 1:** magnetic core material for our magnetic devices.
[00:31:24:979 - 00:31:26:500] **Speaker 1:** There is another loss mechanism.
[00:31:29:290 - 00:31:32:869] **Speaker 1:** And that has to do with the finite electrical conductivity
[00:31:33:209 - 00:31:34:910] **Speaker 1:** of the core material itself.
[00:31:36:380 - 00:31:39:180] **Speaker 1:** Uh, and the generation of what's known as eddy currents.
[00:31:41:390 - 00:31:46:189] **Speaker 1:** So here we've got um again uh uh material with
[00:31:46:189 - 00:31:47:680] **Speaker 1:** a coil of wire around it.
[00:31:48:109 - 00:31:49:449] **Speaker 1:** We've got current flowing.
[00:31:53:880 - 00:31:57:050] **Speaker 1:** Um, and by our right-hand rule, then we know that
[00:31:57:050 - 00:31:59:910] **Speaker 1:** we've got a flux, um, with the North Pole.
[00:32:01:579 - 00:32:04:510] **Speaker 1:** On the side, and when it wraps around, this is
[00:32:04:510 - 00:32:05:270] **Speaker 1:** the south end.
[00:32:09:380 - 00:32:13:979] **Speaker 1:** So the magnetic magnetic flux is created and if I
[00:32:13:979 - 00:32:14:719] **Speaker 1:** is constant.
[00:32:17:170 - 00:32:19:369] **Speaker 1:** Then that gives us a flux that is constant.
[00:32:24:050 - 00:32:27:050] **Speaker 1:** Right, that's all well and good, but most often we
[00:32:27:050 - 00:32:30:130] **Speaker 1:** have a current that is, has a rate of change
[00:32:30:130 - 00:32:31:300] **Speaker 1:** associated with it.
[00:32:31:810 - 00:32:35:109] **Speaker 1:** Just think about the, the power inductor, we've always talked
[00:32:35:109 - 00:32:36:930] **Speaker 1:** about this rate of change of current, which is the
[00:32:36:930 - 00:32:37:699] **Speaker 1:** current ripple.
[00:32:38:290 - 00:32:42:130] **Speaker 1:** So that introduces a DI by DT.
[00:32:47:689 - 00:32:49:859] **Speaker 1:** So ADI.
[00:32:50:949 - 00:32:54:510] **Speaker 1:** By DT results in a D5 by DT.
[00:33:02:530 - 00:33:03:930] **Speaker 1:** Also, what's the importance of that?
[00:33:04:170 - 00:33:08:280] **Speaker 1:** Well, We have this thing known as Faraday's Law.
[00:33:14:800 - 00:33:18:219] **Speaker 1:** Faraday's law tells us that there is an induced voltage
[00:33:18:680 - 00:33:26:979] **Speaker 1:** which is equal to If they're In Turns, so a
[00:33:26:979 - 00:33:30:339] **Speaker 1:** number of loops that we've got around, there are in
[00:33:30:339 - 00:33:34:359] **Speaker 1:** turns in that coil that's equal to N times D5
[00:33:34:359 - 00:33:35:260] **Speaker 1:** by DT.
[00:33:42:229 - 00:33:50:199] **Speaker 1:** And then if we apply lenses law, It states that
[00:33:50:199 - 00:33:53:780] **Speaker 1:** we, the induced voltage tries to set up a current
[00:33:53:780 - 00:33:56:780] **Speaker 1:** that opposes the change in current.
[00:34:13:060 - 00:34:16:350] **Speaker 1:** So what we have here is, um, as far as
[00:34:16:350 - 00:34:19:550] **Speaker 1:** eddy currents are concerned, this will produce an eddy current.
[00:34:23:749 - 00:34:25:339] **Speaker 1:** Is this material has a finite.
[00:34:26:357 - 00:34:27:688] **Speaker 1:** Conductivity to it.
[00:34:28:069 - 00:34:31:968] **Speaker 1:** Um, we have a looping current around the outside here.
[00:34:33:628 - 00:34:36:669] **Speaker 1:** Faraday's law and Lenz's law combined show that there is
[00:34:36:669 - 00:34:40:709] **Speaker 1:** a looping current within the core that tries to oppose
[00:34:40:709 - 00:34:42:908] **Speaker 1:** that current, the changing current.
[00:34:47:638 - 00:34:49:388] **Speaker 1:** So we can call that.
[00:34:50:449 - 00:34:53:530] **Speaker 1:** IE, uh, eddy current.
[00:34:57:019 - 00:35:02:769] **Speaker 1:** So induced eddy current introduces I 2 losses in the
[00:35:02:769 - 00:35:03:668] **Speaker 1:** core itself.
[00:35:08:409 - 00:35:11:449] **Speaker 1:** So luckily the ferrite material that we have in our
[00:35:11:449 - 00:35:16:409] **Speaker 1:** power electronic converters um is constructed like a ceramic and
[00:35:16:409 - 00:35:18:729] **Speaker 1:** as such it's conductivity is very poor.
[00:35:19:949 - 00:35:22:939] **Speaker 1:** So we get very little by way of eddy current
[00:35:22:939 - 00:35:24:780] **Speaker 1:** loss in our ferrite material.
[00:35:25:340 - 00:35:31:899] **Speaker 1:** The steel material is actually quite conductive, um, so the
[00:35:31:899 - 00:35:35:800] **Speaker 1:** way that steel material is, uh, to try and minimise
[00:35:35:800 - 00:35:39:340] **Speaker 1:** eddy currents, um, what we do with steel that forms
[00:35:39:340 - 00:35:41:820] **Speaker 1:** the core of a, of a magnetic material like that
[00:35:41:820 - 00:35:43:379] **Speaker 1:** is that we laminate it.
[00:35:44:530 - 00:35:48:939] **Speaker 1:** People see laminated steel cores before, so you'd end up
[00:35:48:939 - 00:35:50:580] **Speaker 1:** with these laminations.
[00:35:51:689 - 00:35:57:169] **Speaker 1:** And each lamination is electrically insulated from the next, so
[00:35:57:169 - 00:35:59:729] **Speaker 1:** it has a coating on it that literally insulates it.
[00:36:00:290 - 00:36:04:189] **Speaker 1:** So your eddy current is trying to circulate within just
[00:36:04:330 - 00:36:05:969] **Speaker 1:** the thickness of the lamination.
[00:36:06:739 - 00:36:10:520] **Speaker 1:** And it's resistance, effective resistance is quite high.
[00:36:10:949 - 00:36:13:459] **Speaker 1:** So that's the way of limiting the eddy currents to
[00:36:13:459 - 00:36:16:739] **Speaker 1:** steel type materials is by laminating them.
[00:36:18:719 - 00:36:19:149] **Speaker 1:** OK.
[00:36:21:830 - 00:36:25:989] **Speaker 1:** So, double set of losses for our um for our
[00:36:25:989 - 00:36:27:189] **Speaker 1:** magnetic materials.
[00:36:31:409 - 00:36:33:179] **Speaker 1:** Alright, so all of that material was just to get
[00:36:33:179 - 00:36:35:850] **Speaker 1:** your head in the right sort of mind space to
[00:36:35:850 - 00:36:38:300] **Speaker 1:** understand that we have these materials and they behave a
[00:36:38:300 - 00:36:39:770] **Speaker 1:** certain way, um.
[00:36:40:580 - 00:36:42:219] **Speaker 1:** But when it comes down to it, once you've got
[00:36:42:219 - 00:36:45:020] **Speaker 1:** that understanding, you, what you need to do is be
[00:36:45:020 - 00:36:51:020] **Speaker 1:** able to produce an effective magnetic material circuit.
[00:36:51:929 - 00:36:55:010] **Speaker 1:** Because that's what it kind of behaves like, uh, and
[00:36:55:010 - 00:36:59:709] **Speaker 1:** use that information to design your own types of um
[00:37:00:209 - 00:37:01:649] **Speaker 1:** magnetic component from that.
[00:37:03:840 - 00:37:07:790] **Speaker 1:** So that's What we're talking about here are magnetic circuits.
[00:37:12:280 - 00:37:15:439] **Speaker 1:** So magnetic flux, OK, set up by current flowing in
[00:37:15:439 - 00:37:16:760] **Speaker 1:** the coil, um.
[00:37:17:840 - 00:37:23:280] **Speaker 1:** Luckily, can be thought of almost identically to an electrical
[00:37:23:280 - 00:37:23:919] **Speaker 1:** circuit.
[00:37:24:320 - 00:37:27:080] **Speaker 1:** So we're much, much used to dealing with electrical circuits
[00:37:27:080 - 00:37:29:919] **Speaker 1:** that has a voltage source, that has a certain amount
[00:37:29:919 - 00:37:33:199] **Speaker 1:** of resistance, and because of that voltage source and resistance,
[00:37:33:280 - 00:37:36:010] **Speaker 1:** there are certain current flowing through that circuit.
[00:37:37:870 - 00:37:41:989] **Speaker 1:** We can treat our magnetic circuits almost in an identical
[00:37:41:989 - 00:37:42:409] **Speaker 1:** way.
[00:37:44:129 - 00:37:45:649] **Speaker 1:** And that's the approach that we will take.
[00:37:45:729 - 00:37:47:770] **Speaker 1:** You don't have to do it this way, but it
[00:37:47:770 - 00:37:50:409] **Speaker 1:** certainly makes it a lot easier to wrap your head
[00:37:50:409 - 00:37:53:229] **Speaker 1:** around and do the design and analysis from.
[00:37:55:280 - 00:38:02:790] **Speaker 1:** So I've shown here, um, a physical representation of an
[00:38:02:790 - 00:38:03:500] **Speaker 1:** inductor.
[00:38:09:090 - 00:38:12:689] **Speaker 1:** We've got this, this sort of like the circles are
[00:38:12:689 - 00:38:17:030] **Speaker 1:** representing a coil of wire around the central pillar.
[00:38:18:010 - 00:38:23:510] **Speaker 1:** And we've got This E-type or shape material as being
[00:38:23:510 - 00:38:26:070] **Speaker 1:** the magnetic core of the inductor.
[00:38:30:260 - 00:38:33:340] **Speaker 1:** You will be given next week with your components handout.
[00:38:35:790 - 00:38:38:629] **Speaker 1:** Um, a core which kind of looks a bit like
[00:38:38:629 - 00:38:39:090] **Speaker 1:** this.
[00:38:43:040 - 00:38:46:780] **Speaker 1:** So, by the way, this is, this is the, um,
[00:38:46:959 - 00:38:49:239] **Speaker 1:** the circuit that I showed you, uh, when I introduced
[00:38:49:239 - 00:38:49:899] **Speaker 1:** the project.
[00:38:50:110 - 00:38:53:560] **Speaker 1:** It's basically your butt converter, um, and here's the core
[00:38:53:560 - 00:38:55:639] **Speaker 1:** that we will be giving you to make your inductor
[00:38:55:639 - 00:38:56:219] **Speaker 1:** out of.
[00:38:56:600 - 00:38:59:520] **Speaker 1:** So I've just taken it apart so that I can
[00:38:59:520 - 00:39:00:350] **Speaker 1:** pull it apart.
[00:39:00:719 - 00:39:10:169] **Speaker 1:** So Gee, That's one half The old Reese.
[00:39:12:820 - 00:39:16:389] **Speaker 1:** OK, so that's one half of that, that core, um,
[00:39:19:459 - 00:39:21:010] **Speaker 1:** Alright, so there's a central pillar.
[00:39:22:600 - 00:39:25:919] **Speaker 1:** And two side legs to the core, and it's built
[00:39:25:919 - 00:39:27:239] **Speaker 1:** in two halves.
[00:39:28:229 - 00:39:31:620] **Speaker 1:** So that you can wind Your inductive windings on the
[00:39:31:620 - 00:39:35:320] **Speaker 1:** central part, it's got a little plastic bobbin for that,
[00:39:35:939 - 00:39:36:429] **Speaker 1:** uh.
[00:39:37:550 - 00:39:39:889] **Speaker 1:** Plonk it on one half and then put the other
[00:39:39:889 - 00:39:42:649] **Speaker 1:** half of your core on top.
[00:39:42:989 - 00:39:44:870] **Speaker 1:** So that's what we're showing there is the two halves
[00:39:44:870 - 00:39:46:989] **Speaker 1:** with a little air gap in between.
[00:39:50:270 - 00:39:52:949] **Speaker 1:** That's what we're showing here with the two halves with
[00:39:52:949 - 00:39:54:250] **Speaker 1:** a little air gap in between.
[00:39:58:770 - 00:40:00:719] **Speaker 1:** Just so you can get your head around that.
[00:40:01:300 - 00:40:08:030] **Speaker 1:** Um, Then I've shown the Circuit equivalent.
[00:40:22:489 - 00:40:26:860] **Speaker 1:** So there is what's known as an MMF, a magnetomotive
[00:40:26:860 - 00:40:32:280] **Speaker 1:** force that is The thing that drives the flux creation
[00:40:32:280 - 00:40:33:850] **Speaker 1:** within the core.
[00:40:34:350 - 00:40:35:350] **Speaker 1:** So where does that come from?
[00:40:35:580 - 00:40:36:979] **Speaker 1:** It comes from the fact that you've got a coil
[00:40:36:979 - 00:40:39:139] **Speaker 1:** of wire with current flowing through it.
[00:40:41:260 - 00:40:44:439] **Speaker 1:** Right, so you end up with end times I where
[00:40:46:870 - 00:40:49:750] **Speaker 1:** The number of turns here gives us our in.
[00:40:50:840 - 00:40:54:669] **Speaker 1:** Right, how many times we're wrapping our wire around the,
[00:40:54:770 - 00:40:55:429] **Speaker 1:** the core?
[00:40:57:189 - 00:41:01:709] **Speaker 1:** So in times I, so there's the core is carrying
[00:41:01:709 - 00:41:02:209] **Speaker 1:** current.
[00:41:07:169 - 00:41:07:739] **Speaker 1:** Of I.
[00:41:12:159 - 00:41:17:689] **Speaker 1:** So that MMF is pretty much analogous to the voltage
[00:41:17:689 - 00:41:20:199] **Speaker 1:** source in an electrical circuit.
[00:41:21:770 - 00:41:23:270] **Speaker 1:** So, MMF.
[00:41:24:649 - 00:41:26:610] **Speaker 1:** Looks like a voltage source speed.
[00:41:28:620 - 00:41:33:899] **Speaker 1:** The reluctance is what's being identified with are here.
[00:41:34:300 - 00:41:39:639] **Speaker 1:** So it's how much the domains in the magnetic material
[00:41:39:639 - 00:41:43:879] **Speaker 1:** oppose the magnetic force to align them.
[00:41:44:919 - 00:41:49:419] **Speaker 1:** Right, so how much it it acts to oppose that
[00:41:49:600 - 00:41:50:120] **Speaker 1:** alignment.
[00:41:50:239 - 00:41:54:219] **Speaker 1:** So it's kind of like a resistance to alignment.
[00:41:54:840 - 00:41:58:979] **Speaker 1:** Hence, it behaves like a resistance in the electrical equivalent.
[00:42:00:600 - 00:42:04:760] **Speaker 1:** So, this is the reluctance, so it's the length of
[00:42:04:760 - 00:42:09:340] **Speaker 1:** the flux pathway divided by the cross-sectional area of the,
[00:42:09:429 - 00:42:13:120] **Speaker 1:** of the core, um, multiplied by the relative permeability and
[00:42:13:120 - 00:42:15:020] **Speaker 1:** that of the permeability of free space.
[00:42:17:600 - 00:42:20:250] **Speaker 1:** All right, so we end up with magnetic flux is
[00:42:20:250 - 00:42:24:090] **Speaker 1:** equal to the MMF divided by the reluctance.
[00:42:24:689 - 00:42:28:030] **Speaker 1:** Ah, so if this is the same as our voltage
[00:42:28:280 - 00:42:30:389] **Speaker 1:** and this is the same as resistance.
[00:42:33:060 - 00:42:41:570] **Speaker 1:** Equivalent Then what does that make that an equivalent to?
[00:42:43:129 - 00:42:44:100] **Speaker 1:** Yeah, I heard it.
[00:42:44:780 - 00:42:46:020] **Speaker 1:** Current, yes.
[00:42:51:889 - 00:42:57:939] **Speaker 1:** Alright, so if we transfer a magnetic circuit to our
[00:42:57:939 - 00:43:00:780] **Speaker 1:** understanding of electrical circuits that is only going to involve
[00:43:00:780 - 00:43:02:659] **Speaker 1:** a voltage source and some resistors.
[00:43:03:409 - 00:43:06:610] **Speaker 1:** The analysis becomes should become quite a lot easier to
[00:43:06:610 - 00:43:07:590] **Speaker 1:** get your head around.
[00:43:16:060 - 00:43:21:129] **Speaker 1:** Um, a point that probably didn't really make, uh, a
[00:43:21:139 - 00:43:24:939] **Speaker 1:** a big deal about is the cross-sectional area that's here
[00:43:25:169 - 00:43:28:000] **Speaker 1:** is, if we were to put this on its end,
[00:43:28:060 - 00:43:30:260] **Speaker 1:** you would see that, well, with the core that we've
[00:43:30:260 - 00:43:34:949] **Speaker 1:** got here, it's a circular, um, Material, so the cross
[00:43:34:949 - 00:43:36:090] **Speaker 1:** sectional area.
[00:43:37:689 - 00:43:40:469] **Speaker 1:** is the area of that central pillar.
[00:43:41:239 - 00:43:45:899] **Speaker 1:** The area that we see um on the limbs.
[00:43:47:310 - 00:43:50:280] **Speaker 1:** Is half the area of the central core.
[00:43:51:239 - 00:43:53:879] **Speaker 1:** So this, if this is A, then this would be
[00:43:53:879 - 00:43:56:959] **Speaker 1:** A over 2, and this is A over 2.
[00:44:13:679 - 00:44:15:570] **Speaker 1:** So what does that mean as far as our electrical
[00:44:15:570 - 00:44:17:409] **Speaker 1:** equivalent is concerned?
[00:44:20:800 - 00:44:22:139] **Speaker 1:** Well, we can redraw.
[00:44:23:270 - 00:44:26:250] **Speaker 1:** The circuit Pulling off your limb.
[00:44:27:139 - 00:44:30:699] **Speaker 1:** Reluctances onto one side, uh, and then you've got your
[00:44:30:699 - 00:44:32:560] **Speaker 1:** core as well.
[00:44:33:939 - 00:44:37:459] **Speaker 1:** Given the limb area was half what it was for
[00:44:37:459 - 00:44:40:419] **Speaker 1:** the core, then the R limb is going to be
[00:44:40:419 - 00:44:44:820] **Speaker 1:** equal to To our core.
[00:44:46:679 - 00:44:48:179] **Speaker 1:** Go to our core.
[00:44:49:909 - 00:44:52:939] **Speaker 1:** But they're in parallel Of the same value.
[00:44:53:020 - 00:44:57:179] **Speaker 1:** So what is the effect if it was resistances, what
[00:44:57:179 - 00:44:59:520] **Speaker 1:** is if these two are the same value.
[00:45:00:530 - 00:45:01:929] **Speaker 1:** And you've got them connected in parallel.
[00:45:02:090 - 00:45:04:070] **Speaker 1:** What is the total result of that?
[00:45:04:979 - 00:45:08:020] **Speaker 1:** It's equal to half, right, so you've got 2 our
[00:45:08:020 - 00:45:11:389] **Speaker 1:** core plus 2 our core divided by 2, it's just
[00:45:11:659 - 00:45:12:300] **Speaker 1:** our core.
[00:45:13:030 - 00:45:16:820] **Speaker 1:** So you've got our core plus our core equals our
[00:45:16:820 - 00:45:17:179] **Speaker 1:** core.
[00:45:21:520 - 00:45:22:280] **Speaker 1:** Uh, to our core.
[00:45:31:639 - 00:45:34:800] **Speaker 1:** But what we have not done here is include the
[00:45:34:800 - 00:45:37:040] **Speaker 1:** important effect of that little air gap that I just
[00:45:37:040 - 00:45:37:459] **Speaker 1:** mentioned.
[00:45:39:260 - 00:45:43:620] **Speaker 1:** So, if we assume, say for this magnetic material that
[00:45:43:620 - 00:45:46:459] **Speaker 1:** it has a relative permeability of 1600.
[00:45:47:100 - 00:45:49:340] **Speaker 1:** It's kind of mid-range for Fairrite.
[00:45:50:189 - 00:45:55:719] **Speaker 1:** But For air The mu is equal to one.
[00:45:58:189 - 00:46:01:860] **Speaker 1:** Well, given the reluctance is equal to l over a
[00:46:02:209 - 00:46:07:040] **Speaker 1:** mm naught, then The value of reluctance associated with the
[00:46:07:040 - 00:46:12:040] **Speaker 1:** air gap is huge with respect to the reluctance due
[00:46:12:040 - 00:46:13:060] **Speaker 1:** to the core material.
[00:46:14:209 - 00:46:17:409] **Speaker 1:** So if we actually have an air gap, that will,
[00:46:17:610 - 00:46:21:050] **Speaker 1:** that will completely dominate the entire reluctance of the, the
[00:46:21:050 - 00:46:21:810] **Speaker 1:** closed circuit.
[00:46:33:010 - 00:46:35:770] **Speaker 1:** So just in the last couple of minutes, I'll quickly
[00:46:35:770 - 00:46:38:959] **Speaker 1:** show, so we've got the MMF.
[00:46:40:620 - 00:46:43:050] **Speaker 1:** Alright, so that's effectively our voltage source.
[00:46:43:429 - 00:46:48:370] **Speaker 1:** We've got the Our core, which is a small value
[00:46:48:370 - 00:46:50:449] **Speaker 1:** of reluctance, so I'm gonna draw it as a small
[00:46:50:449 - 00:46:51:149] **Speaker 1:** resistor.
[00:46:52:159 - 00:46:58:280] **Speaker 1:** Then we've got The A gap reluctance.
[00:47:04:250 - 00:47:06:550] **Speaker 1:** And it's a big value of reluctance.
[00:47:08:229 - 00:47:14:409] **Speaker 1:** Then we have the resistance due to the Limb.
[00:47:14:689 - 00:47:15:810] **Speaker 1:** So limb.
[00:47:16:679 - 00:47:17:899] **Speaker 1:** The reluctance of the limb.
[00:47:22:600 - 00:47:25:270] **Speaker 1:** Which are both small values, but the limb has an
[00:47:25:270 - 00:47:25:669] **Speaker 1:** air gap.
[00:47:51:360 - 00:47:55:479] **Speaker 1:** OK, if these resistors are much, much larger than these
[00:47:55:479 - 00:47:57:840] **Speaker 1:** resistors, just like you would have for a circuit with
[00:47:57:840 - 00:48:01:479] **Speaker 1:** voltage drops, there's almost no voltage drop here, large voltage
[00:48:01:479 - 00:48:04:360] **Speaker 1:** drop, almost done, large voltage drop.
[00:48:05:229 - 00:48:08:790] **Speaker 1:** So we can essentially neglect the effect of those.
[00:48:10:010 - 00:48:13:260] **Speaker 1:** Small values of reluctance, and you end up with a
[00:48:13:260 - 00:48:13:879] **Speaker 1:** circuit.
[00:48:25:139 - 00:48:28:790] **Speaker 1:** Which is just The core air gap.
[00:48:31:280 - 00:48:37:909] **Speaker 1:** And then the two Uh, limb A gap.
[00:48:41:030 - 00:48:42:909] **Speaker 1:** Um, and we have the same situation.
[00:48:43:149 - 00:48:47:750] **Speaker 1:** The core is double the area of the two limbs.
[00:48:48:770 - 00:48:53:310] **Speaker 1:** So, the core reluctance of the ear gap will be
[00:48:53:719 - 00:48:58:129] **Speaker 1:** half the reluctance of each of the two limb ear
[00:48:58:129 - 00:48:58:689] **Speaker 1:** gaps.
[00:49:16:639 - 00:49:18:860] **Speaker 1:** So in the end, it devolves down.
[00:49:19:810 - 00:49:22:370] **Speaker 1:** to a very simple circuit with the MMF.
[00:49:24:439 - 00:49:29:409] **Speaker 1:** And a reluctance That's equal to 2 times the reluctance
[00:49:29:409 - 00:49:32:540] **Speaker 1:** of the core um air gap.
[00:49:36:320 - 00:49:42:979] **Speaker 1:** And our total Equals 2 times L air gap.
[00:49:45:550 - 00:49:48:790] **Speaker 1:** Over m A.
[00:49:49:729 - 00:49:50:169] **Speaker 1:** Cool.
[00:49:56:679 - 00:49:59:159] **Speaker 1:** OK, this is very important for you to keep track
[00:49:59:159 - 00:50:04:419] **Speaker 1:** of because that Will be the design expression or the
[00:50:04:419 - 00:50:07:750] **Speaker 1:** design formula that you would use in determining what is
[00:50:07:750 - 00:50:11:709] **Speaker 1:** the total reluctance of your power inductor that you've designed.
[00:50:13:419 - 00:50:14:459] **Speaker 1:** OK, that's it for today.
[00:50:14:820 - 00:50:18:820] **Speaker 1:** I'll carry on tomorrow with going right through the design
[00:50:18:820 - 00:50:20:229] **Speaker 1:** process for the specific inductor.
[00:50:41:580 - 00:50:41:590] **Speaker 0:** Yeah.
[00:50:44:429 - 00:50:48:879] **Speaker 0:** I Oh.
[00:50:52:469 - 00:50:52:479] **Speaker 0:** Yes.
[00:50:56:850 - 00:50:56:899] **Speaker 0:** Me.
[00:51:11:689 - 00:51:13:820] **Speaker 0:** It's OK, I don't you in my hand.
[00:51:19:969 - 00:51:19:979] **Speaker 0:** Hello.
[00:51:21:239 - 00:51:26:639] **Speaker 0:** Is the MMF and the the magnetic force or magnetic
[00:51:26:639 - 00:51:27:459] **Speaker 0:** field the same?
[00:51:31:679 - 00:51:33:790] **Speaker 1:** Effectively, yes.
[00:51:34:409 - 00:51:38:570] **Speaker 1:** So it sets up the the forcing function to align
[00:51:38:570 - 00:51:39:510] **Speaker 1:** the domains.
[00:51:39:889 - 00:51:40:389] **Speaker 1:** Um.
[00:51:41:320 - 00:51:42:429] **Speaker 0:** But it, it produces.
[00:51:44:570 - 00:51:44:580] **Speaker 0:** Yes.
[00:51:47:560 - 00:51:47:570] **Speaker 0:** OK.
[00:51:53:379 - 00:51:53:429] **Speaker 0:** circuit.
[00:51:53:810 - 00:51:55:659] **Speaker 0:** I wanna see stuff on E Spice with the solo
[00:51:55:659 - 00:51:58:830] **Speaker 0:** car, but I'm a little stuck on where I should
[00:51:58:889 - 00:52:00:870] **Speaker 0:** start with the sizing.
[00:52:01:879 - 00:52:01:899] **Speaker 0:** I see.
[00:52:03:469 - 00:52:04:270] **Speaker 0:** OK, so.
[00:52:05:750 - 00:52:08:229] **Speaker 1:** For the capacities I've already identified.
[00:52:09:610 - 00:52:13:909] **Speaker 0:** But Well, uh, what you should be aiming for for
[00:52:13:909 - 00:52:19:530] **Speaker 0:** certain voltage ripples given currents and voltages, so it's going
[00:52:19:530 - 00:52:21:370] **Speaker 1:** to make the, you have to make the assumption is
[00:52:21:370 - 00:52:24:570] **Speaker 1:** what is the voltage and current that you're expecting in
[00:52:24:570 - 00:52:25:489] **Speaker 0:** this simulation.
[00:52:26:159 - 00:52:28:229] **Speaker 0:** Um, given the conditions.
[00:52:28:850 - 00:52:33:399] **Speaker 0:** Uh, alright, and input voltage as well.
[00:52:33:719 - 00:52:37:199] **Speaker 0:** So we've got what 17 volts or something that we
[00:52:37:199 - 00:52:41:360] **Speaker 0:** input voltage, yeah, and if you have like a uh
[00:52:41:360 - 00:52:43:360] **Speaker 0:** they so saying in the labs that the solar panels
[00:52:43:360 - 00:52:44:639] **Speaker 0:** are about 10 volts, would you make.
[00:52:47:110 - 00:52:51:310] **Speaker 0:** The teams are the ideal so ideal.
[00:52:52:780 - 00:52:57:560] **Speaker 0:** Um, I like the one that you only get.
[00:53:02:850 - 00:53:02:860] **Speaker 0:** it.
[00:53:03:939 - 00:53:08:570] **Speaker 0:** I All right.
[00:53:12:219 - 00:53:12:229] **Speaker 0:** Mr.
[00:53:24:979 - 00:53:25:360] **Speaker 0:** No.
[00:53:45:179 - 00:53:45:989] **Speaker 0:** I the.
[00:53:53:929 - 00:54:04:760] **Speaker 0:** That Um, I Yeah.
[00:54:35:060 - 00:54:35:070] **Speaker 0:** Yeah.
[00:54:38:419 - 00:54:46:669] **Speaker 0:** I B.
[00:54:52:800 - 00:54:59:250] **Speaker 0:** I I get what was mean.

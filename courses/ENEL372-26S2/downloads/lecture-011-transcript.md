# ENEL372-26S2 Lecture 11 native Echo transcript

Date: August 6, 2026 3:00pm-3:55pm
Transcript type: native Echo automated transcript.

[00:00:01:139 - 00:00:02:930] **Speaker 0:** All right, Karakoto, whoa.
[00:00:04:179 - 00:00:05:159] **Speaker 0:** Welcome along.
[00:00:07:989 - 00:00:09:130] **Speaker 0:** Nice to see you all again.
[00:00:09:630 - 00:00:12:609] **Speaker 0:** All right, um, so I just had a couple of
[00:00:12:609 - 00:00:17:790] **Speaker 0:** slides left to, um, To finish off with, uh, from
[00:00:17:790 - 00:00:23:350] **Speaker 0:** last lecture, um, it was looking at utilising capacitors added
[00:00:23:350 - 00:00:27:549] **Speaker 0:** to our circuit in order to do, um, power supply
[00:00:27:549 - 00:00:29:309] **Speaker 0:** ground noise decoupling.
[00:00:30:420 - 00:00:35:020] **Speaker 0:** Um, so we, we looked at the, uh, first up,
[00:00:35:259 - 00:00:38:220] **Speaker 0:** the fact that we have not all capacitors being created
[00:00:38:220 - 00:00:38:540] **Speaker 0:** equal.
[00:00:38:619 - 00:00:41:169] **Speaker 0:** Some are better for using at higher frequencies than others,
[00:00:41:500 - 00:00:44:619] **Speaker 0:** which is quite often what you see in, um, circuit
[00:00:44:619 - 00:00:46:979] **Speaker 0:** diagrams, uh, for various circuits.
[00:00:47:099 - 00:00:50:180] **Speaker 0:** It's on application notes, there could be multiple parallel connected
[00:00:50:180 - 00:00:54:099] **Speaker 0:** capacitors of different values, um, in the schematic.
[00:00:54:419 - 00:00:56:610] **Speaker 0:** So they're usually, the smaller ones would be of a
[00:00:56:610 - 00:01:00:459] **Speaker 0:** higher frequency capacitants and the larger ones being, um, of
[00:01:00:459 - 00:01:02:919] **Speaker 0:** the lower frequency type, but of larger size.
[00:01:03:740 - 00:01:07:790] **Speaker 0:** Um, we also, uh, very often employ what's known as
[00:01:07:790 - 00:01:08:730] **Speaker 0:** pin decoupling.
[00:01:09:430 - 00:01:13:449] **Speaker 0:** That's where you take a capacitor, um, between your ground
[00:01:13:449 - 00:01:17:069] **Speaker 0:** and, um, and your power pin at the IC and
[00:01:17:069 - 00:01:20:569] **Speaker 0:** try to place it, uh, when you do your layout
[00:01:20:790 - 00:01:25:330] **Speaker 0:** as close to the pins of that IC as possible.
[00:01:25:709 - 00:01:27:269] **Speaker 0:** Uh, it, it, it, it doesn't have to be a
[00:01:27:269 - 00:01:30:300] **Speaker 0:** very large value capacitor, it can be around, uh, 0.1
[00:01:30:300 - 00:01:32:349] **Speaker 0:** microph, but it does want to be of the high
[00:01:32:349 - 00:01:34:769] **Speaker 0:** frequency nature, so film or ceramic.
[00:01:35:349 - 00:01:38:769] **Speaker 0:** Um, now that has a great, uh, ability of, uh,
[00:01:38:779 - 00:01:43:500] **Speaker 0:** blocking low-level noise, um, from the ICs propagating out into
[00:01:43:959 - 00:01:48:400] **Speaker 0:** the power supply, um, traces and ground traces, but also
[00:01:48:400 - 00:01:52:239] **Speaker 0:** if there is additional noise that's just managed to couple
[00:01:52:239 - 00:01:55:519] **Speaker 0:** in from the, the circuit before you get to the
[00:01:55:519 - 00:01:58:559] **Speaker 0:** IC, it's a great way of blocking into the IC
[00:01:58:559 - 00:01:58:940] **Speaker 0:** as well.
[00:02:00:250 - 00:02:03:319] **Speaker 0:** Uh, and then finally, you look at global decoupling, um,
[00:02:03:650 - 00:02:06:730] **Speaker 0:** so apart from the capacitances you might have right at
[00:02:06:730 - 00:02:11:210] **Speaker 0:** the, uh, start of your circuit, um, that, that tries
[00:02:11:210 - 00:02:15:169] **Speaker 0:** to do, uh, voltage stabilisation or something, so there's a
[00:02:15:169 - 00:02:18:110] **Speaker 0:** big capacitance right at the input from your power supply.
[00:02:18:410 - 00:02:21:410] **Speaker 0:** Um, you would also find that you generally try to
[00:02:21:410 - 00:02:26:669] **Speaker 0:** do this global decoupling, which is, um, uh, adding capacitants
[00:02:26:669 - 00:02:28:630] **Speaker 0:** throughout the circuit where necessary.
[00:02:29:210 - 00:02:31:949] **Speaker 0:** Across the, across the power supply to ground.
[00:02:32:369 - 00:02:35:130] **Speaker 0:** Um, so you'd have maybe a parallel combination of a
[00:02:35:130 - 00:02:39:889] **Speaker 0:** larger, say 10 microferrett electrolytic capacitor, um, if you've got
[00:02:39:889 - 00:02:43:050] **Speaker 0:** the budget for it, tantalum, um, and a medium value,
[00:02:43:160 - 00:02:47:690] **Speaker 0:** say 1 microferri high frequency capacitor, so ceramic, uh, or
[00:02:47:690 - 00:02:48:110] **Speaker 0:** film.
[00:02:48:589 - 00:02:51:149] **Speaker 0:** So, across the power and ground traces where the power
[00:02:51:149 - 00:02:53:850] **Speaker 0:** is connected to the PCB, that's the initial input part,
[00:02:53:869 - 00:02:58:029] **Speaker 0:** and these other locations where you, uh, you find the
[00:02:58:029 - 00:02:59:860] **Speaker 0:** circuit may be susceptible to noise.
[00:03:00:270 - 00:03:03:789] **Speaker 0:** So where you might have, um, analogue and digital traces
[00:03:03:789 - 00:03:05:910] **Speaker 0:** close to each other or perhaps where there is a
[00:03:05:910 - 00:03:10:429] **Speaker 0:** region in the circuit that's experiencing a high values of
[00:03:10:429 - 00:03:13:190] **Speaker 0:** current change, um, or voltage change even.
[00:03:13:869 - 00:03:14:210] **Speaker 0:** Right.
[00:03:15:600 - 00:03:17:699] **Speaker 0:** Uh, so we've already shown that the decoupling can be
[00:03:17:699 - 00:03:20:570] **Speaker 0:** used to help reduce the inductive loop area, which is
[00:03:20:570 - 00:03:22:570] **Speaker 0:** important for our power electronic circuits.
[00:03:23:399 - 00:03:24:940] **Speaker 0:** Just to finish that bit off.
[00:03:28:750 - 00:03:31:100] **Speaker 0:** Uh, here we have the solar car project where we
[00:03:31:100 - 00:03:35:509] **Speaker 0:** might, where we, well, we don't have the, um, luxury
[00:03:35:509 - 00:03:37:970] **Speaker 0:** for the most part of having PCBs unless you make
[00:03:38:470 - 00:03:40:960] **Speaker 0:** design one and we, we make it for you, um,
[00:03:41:179 - 00:03:44:190] **Speaker 0:** but on Verro board and so forth, other areas for
[00:03:44:190 - 00:03:46:130] **Speaker 0:** decoupling, well, we've already covered this.
[00:03:49:779 - 00:03:53:220] **Speaker 0:** So that's to minimise the uh the strain inductances associated
[00:03:53:220 - 00:03:56:440] **Speaker 0:** with that, um, that switching loop.
[00:03:57:100 - 00:04:00:699] **Speaker 0:** But, um, you might also want to consider at the
[00:04:00:699 - 00:04:05:679] **Speaker 0:** TL 494 um IC itself, that pin level decoupling.
[00:04:06:429 - 00:04:08:750] **Speaker 0:** Right, you want the power supply to the TL 494
[00:04:08:750 - 00:04:11:369] **Speaker 0:** to be as nice and stable as possible, that's where
[00:04:11:630 - 00:04:16:269] **Speaker 0:** uh you generate your um oscillator for the, um, keeping
[00:04:16:269 - 00:04:18:250] **Speaker 0:** a nice stable switching frequency.
[00:04:19:109 - 00:04:23:010] **Speaker 0:** So, and also where you do your, um, your control,
[00:04:23:459 - 00:04:25:309] **Speaker 0:** so again, you want all of the power, the power
[00:04:25:309 - 00:04:28:149] **Speaker 0:** supply here to be as, as nice and noise-free as
[00:04:28:149 - 00:04:28:589] **Speaker 0:** possible.
[00:04:28:989 - 00:04:33:429] **Speaker 0:** So pin-level decoupling, um, so, that pin-level decoupling using a
[00:04:33:429 - 00:04:35:730] **Speaker 0:** nice high frequency capacitor for that.
[00:04:36:170 - 00:04:39:709] **Speaker 0:** Uh, and even when you look to, uh, utilising the,
[00:04:39:769 - 00:04:43:970] **Speaker 0:** um, CMOS inverter part of it, you're switching these on
[00:04:43:970 - 00:04:45:359] **Speaker 0:** and off very rapidly.
[00:04:45:769 - 00:04:49:570] **Speaker 0:** So again, this could cause, um, noise associated with the
[00:04:49:570 - 00:04:52:970] **Speaker 0:** power supply in the ground line, so putting a global
[00:04:52:970 - 00:04:58:489] **Speaker 0:** decoupling, uh, capacitor across the inverter like that would be
[00:04:58:500 - 00:04:59:109] **Speaker 0:** beneficial.
[00:04:59:920 - 00:05:00:230] **Speaker 0:** Yeah.
[00:05:02:709 - 00:05:05:029] **Speaker 0:** Right, so these are things that we're starting to introduce
[00:05:05:029 - 00:05:08:510] **Speaker 0:** uh into our circuit design and uh and, and understand
[00:05:08:510 - 00:05:12:239] **Speaker 0:** that goes beyond just the base operation of what we're
[00:05:12:239 - 00:05:15:109] **Speaker 0:** trying to get the circuit to do, but understanding that
[00:05:15:109 - 00:05:19:070] **Speaker 0:** because we're operating at potentially higher frequencies, uh, noise is
[00:05:19:070 - 00:05:22:250] **Speaker 0:** an issue, how to mitigate uh those sorts of things.
[00:05:26:970 - 00:05:28:540] **Speaker 0:** OK, so we're caught up there.
[00:05:31:950 - 00:05:37:690] **Speaker 0:** And we're moving on now to Looking at more advanced
[00:05:38:309 - 00:05:43:269] **Speaker 0:** styles or types of DC to DC converters, um, The
[00:05:43:269 - 00:05:46:390] **Speaker 0:** types that we've been looking at so far, whilst still
[00:05:46:390 - 00:05:50:709] **Speaker 0:** common and in regular use, um, there are a number
[00:05:50:709 - 00:05:56:149] **Speaker 0:** of uh applications out there that need us to be
[00:05:56:149 - 00:06:02:350] **Speaker 0:** able to electrically isolate the input from the output.
[00:06:02:940 - 00:06:06:470] **Speaker 0:** Uh, some examples here would be like motor speed controllers
[00:06:06:470 - 00:06:10:029] **Speaker 0:** or, or, um, Because you, you don't want to have
[00:06:10:029 - 00:06:13:619] **Speaker 0:** uh big ground loops associated with driving those, those motors.
[00:06:13:950 - 00:06:18:390] **Speaker 0:** You might have medical devices where the output that's attached
[00:06:18:390 - 00:06:21:630] **Speaker 0:** to a patient needs to be electrically isolated from mains,
[00:06:21:989 - 00:06:22:190] **Speaker 0:** right?
[00:06:22:269 - 00:06:26:480] **Speaker 0:** So, absolutely a requirement for um voltage or or um
[00:06:26:480 - 00:06:27:750] **Speaker 0:** electrical isolation there.
[00:06:28:730 - 00:06:31:850] **Speaker 0:** There are quite often you might have um a circuit
[00:06:31:850 - 00:06:37:049] **Speaker 0:** that has sensitive electronic devices that would react badly to
[00:06:37:049 - 00:06:38:450] **Speaker 0:** high voltage transience.
[00:06:38:850 - 00:06:42:769] **Speaker 0:** You might then look at um electrically isolating an input
[00:06:42:769 - 00:06:46:589] **Speaker 0:** side which may experience those transients from the output side.
[00:06:47:739 - 00:06:51:739] **Speaker 0:** Uh, even communication systems, uh, that are spread over a
[00:06:51:739 - 00:06:56:709] **Speaker 0:** wide range of areas, uh, can experience different ground potential
[00:06:56:709 - 00:06:58:579] **Speaker 0:** issues, and you want to make sure that those are
[00:06:58:579 - 00:06:59:880] **Speaker 0:** isolated as well.
[00:07:00:579 - 00:07:04:420] **Speaker 0:** Right, so a number of different, uh, um, application spaces
[00:07:04:420 - 00:07:09:839] **Speaker 0:** which really does bring into, uh, into focus the need
[00:07:09:839 - 00:07:11:959] **Speaker 0:** to have, um, electrical isolation.
[00:07:15:220 - 00:07:22:339] **Speaker 1:** So, for switching base converters, that electrical isolation, uh, the
[00:07:22:339 - 00:07:25:619] **Speaker 0:** best way to achieve that, keep the efficiency nice and
[00:07:25:619 - 00:07:33:040] **Speaker 0:** high, uh, is to utilise, um, Switching frequency transformers.
[00:07:33:470 - 00:07:35:989] **Speaker 0:** So these aren't the type of transformers that uh you
[00:07:35:989 - 00:07:38:649] **Speaker 0:** might be used to seeing that are these big clunky
[00:07:39:309 - 00:07:43:470] **Speaker 0:** steel cord uh transformers that we get in the power
[00:07:43:470 - 00:07:46:570] **Speaker 0:** systems, uh, type of space that work at 50 hertz.
[00:07:46:950 - 00:07:49:230] **Speaker 0:** Um, these are the high frequency ones that utilise the
[00:07:49:230 - 00:07:50:890] **Speaker 0:** ferrites that we've talked about.
[00:07:55:589 - 00:08:02:070] **Speaker 0:** Um, there is an additional bonus to introducing a transformer
[00:08:02:070 - 00:08:05:829] **Speaker 0:** as well for the electrical isolation, and that is a
[00:08:05:829 - 00:08:09:070] **Speaker 0:** transformer because of its nature, you can do a turns
[00:08:09:070 - 00:08:15:250] **Speaker 0:** ratio, uh, design, into that, that can provide a voltage
[00:08:15:589 - 00:08:16:709] **Speaker 0:** transformation.
[00:08:17:190 - 00:08:20:510] **Speaker 0:** That is difficult to achieve for a directly coupled from
[00:08:20:510 - 00:08:23:549] **Speaker 0:** input to output converter, so we can do step up
[00:08:23:549 - 00:08:27:470] **Speaker 0:** and step down to our heart's content, uh, for whatever
[00:08:27:470 - 00:08:31:350] **Speaker 0:** the application might require, by choosing the right turns ratio
[00:08:31:350 - 00:08:32:450] **Speaker 0:** for our transformer.
[00:08:37:760 - 00:08:42:659] **Speaker 0:** Because of this being such a, a useful thing to
[00:08:42:659 - 00:08:45:289] **Speaker 0:** be able to do, the electrical isolation and the voltage
[00:08:45:289 - 00:08:51:530] **Speaker 0:** transformation, there are, there are a really large number of
[00:08:51:530 - 00:08:55:059] **Speaker 0:** possible transformer-based configurations that are out there.
[00:08:55:299 - 00:08:58:619] **Speaker 0:** Um, you look at any switch mode power supply design
[00:08:58:619 - 00:09:03:289] **Speaker 0:** handbook, and it's just this endless variety of converters that
[00:09:03:289 - 00:09:05:039] **Speaker 0:** you could end up looking at designing.
[00:09:06:010 - 00:09:10:489] **Speaker 0:** We're going to be keeping things constrained and focused, and
[00:09:10:489 - 00:09:12:010] **Speaker 0:** we were going to look at a few of the
[00:09:12:010 - 00:09:18:330] **Speaker 0:** more common types that are also um easier to understand
[00:09:18:330 - 00:09:19:330] **Speaker 0:** how they are working.
[00:09:20:859 - 00:09:23:010] **Speaker 0:** Having said that, to say that they're easy to understand,
[00:09:23:219 - 00:09:26:219] **Speaker 0:** it still does take a little bit of, of brainpower
[00:09:26:219 - 00:09:29:419] **Speaker 0:** and, and attention to figure out how these things are
[00:09:29:419 - 00:09:30:400] **Speaker 0:** actually operating.
[00:09:30:859 - 00:09:33:940] **Speaker 0:** And a transformer is being introduced into the circuit, so
[00:09:33:940 - 00:09:37:239] **Speaker 0:** that just is another added element of complexity that we
[00:09:37:239 - 00:09:40:020] **Speaker 0:** have to keep uh track of as we're trying to
[00:09:40:020 - 00:09:43:690] **Speaker 0:** figure out how these work, and then subsequently from that,
[00:09:43:940 - 00:09:46:900] **Speaker 0:** how we might do a design uh with these types
[00:09:46:900 - 00:09:47:659] **Speaker 0:** of converters.
[00:09:57:770 - 00:10:02:280] **Speaker 0:** Before we jump into the DC to DC converted topologies
[00:10:02:280 - 00:10:05:719] **Speaker 0:** that are different, um, and it's really loud.
[00:10:08:219 - 00:10:12:599] **Speaker 0:** Uh, we need to have a look at a transformer
[00:10:13:030 - 00:10:16:460] **Speaker 0:** again, um, and how we tend to model them with
[00:10:16:460 - 00:10:19:900] **Speaker 0:** these types of, um, switch mode converters.
[00:10:20:929 - 00:10:23:400] **Speaker 0:** So hopefully most of you come across at least the
[00:10:23:400 - 00:10:26:080] **Speaker 0:** concept of a transformer before, um.
[00:10:26:909 - 00:10:32:250] **Speaker 0:** That they are an electrically isolated device that enables voltage
[00:10:32:609 - 00:10:36:309] **Speaker 0:** step up or step down, depending on the ratio of
[00:10:36:309 - 00:10:39:950] **Speaker 0:** the number of turns on the primary winding with respect
[00:10:39:950 - 00:10:43:210] **Speaker 0:** to the secondary winding if it's a two winding transformer.
[00:10:44:119 - 00:10:47:760] **Speaker 0:** OK, and we're gonna call those, those number of uh
[00:10:47:760 - 00:10:51:799] **Speaker 0:** turns N1 and N2, respectively, meaning N1 being on the
[00:10:51:799 - 00:10:52:539] **Speaker 0:** primary side.
[00:10:53:549 - 00:10:57:419] **Speaker 0:** Traditionally identified as being the input, and into being the
[00:10:57:419 - 00:11:00:669] **Speaker 0:** number of turns of the winding on the secondary side,
[00:11:01:739 - 00:11:03:250] **Speaker 0:** often considered to be the output.
[00:11:06:900 - 00:11:10:820] **Speaker 0:** That would involve just a simple model that has um
[00:11:10:820 - 00:11:13:619] **Speaker 0:** a primary winding and a secondary winding, and everything else
[00:11:13:619 - 00:11:14:940] **Speaker 0:** is perfect about it.
[00:11:15:219 - 00:11:18:820] **Speaker 0:** Um, we are going to add a bit of extra
[00:11:18:820 - 00:11:20:960] **Speaker 0:** complexity to the transformer model.
[00:11:21:799 - 00:11:28:320] **Speaker 0:** Um, and introduce the concept of magnetising inductance.
[00:11:28:679 - 00:11:31:599] **Speaker 0:** Now the elite part of the, the class will probably
[00:11:31:599 - 00:11:34:479] **Speaker 0:** already have had this from an earlier course about magnetising
[00:11:34:479 - 00:11:39:080] **Speaker 0:** inductance, but it's worth going back to the basics here
[00:11:39:080 - 00:11:41:479] **Speaker 0:** just to get a firm understanding of what we're talking
[00:11:41:479 - 00:11:41:780] **Speaker 0:** about.
[00:11:42:080 - 00:11:45:039] **Speaker 0:** And uh for anyone that hasn't really come across this
[00:11:45:039 - 00:11:47:400] **Speaker 0:** before, it's an introduction to this concept.
[00:11:48:900 - 00:11:58:880] **Speaker 0:** I must emphasise, magnetising inductance is a circuit analysis concept
[00:11:59:140 - 00:11:59:760] **Speaker 0:** model.
[00:12:00:500 - 00:12:03:760] **Speaker 0:** A magnetising inductance does not physically exist.
[00:12:05:059 - 00:12:09:219] **Speaker 0:** There is no component that we have as part of
[00:12:09:219 - 00:12:14:539] **Speaker 0:** the transformer that is an inductor added into the primary
[00:12:14:539 - 00:12:15:179] **Speaker 0:** like this.
[00:12:16:049 - 00:12:20:450] **Speaker 0:** This is a model of what's happening in the core
[00:12:20:450 - 00:12:22:390] **Speaker 0:** of the actual transformer itself.
[00:12:23:130 - 00:12:25:469] **Speaker 0:** So it is a model.
[00:12:26:179 - 00:12:29:500] **Speaker 0:** Um, as we go through, we're gonna talk about current
[00:12:29:500 - 00:12:33:099] **Speaker 0:** flowing in the magnetising inductance.
[00:12:33:630 - 00:12:36:260] **Speaker 0:** Since it's not actually an inductance that physically exists, this
[00:12:36:260 - 00:12:39:979] **Speaker 0:** is just a circuit concept model that enables us to
[00:12:39:979 - 00:12:46:619] **Speaker 0:** do the analysis that we need to, uh, effectively, um,
[00:12:47:099 - 00:12:51:179] **Speaker 0:** cover the operation of the flux within the core.
[00:12:54:219 - 00:12:56:929] **Speaker 0:** So it all works, but it works because it's uh,
[00:12:57:159 - 00:13:01:020] **Speaker 0:** the magnetising conductance models what's going on inside the, the
[00:13:01:020 - 00:13:02:059] **Speaker 0:** core of the transformer.
[00:13:04:429 - 00:13:06:030] **Speaker 0:** OK, now.
[00:13:07:469 - 00:13:10:349] **Speaker 0:** So, we have the N1, N2, that would be an
[00:13:10:349 - 00:13:15:280] **Speaker 0:** ideal transformer, and then we conceptually model a parallel inductance
[00:13:15:280 - 00:13:18:549] **Speaker 0:** on the primary side, which is called a magnetising inductance.
[00:13:21:250 - 00:13:25:219] **Speaker 0:** It's critical that the periodic flux in our core sums
[00:13:25:219 - 00:13:25:940] **Speaker 0:** to zero.
[00:13:26:580 - 00:13:28:520] **Speaker 0:** If we don't, if there is a net.
[00:13:29:510 - 00:13:33:409] **Speaker 0:** These net amount of flux left over cycle by cycle,
[00:13:33:950 - 00:13:35:619] **Speaker 0:** then that flux will be additive.
[00:13:36:150 - 00:13:38:309] **Speaker 0:** So eventually you'll get to the point where the flux
[00:13:38:309 - 00:13:43:409] **Speaker 0:** density within the core will exceed the maximum flux density
[00:13:43:409 - 00:13:45:710] **Speaker 0:** allowed for the core and it will saturate.
[00:13:46:570 - 00:13:51:210] **Speaker 0:** So it's effective permeability will plummet, fall from something that
[00:13:51:210 - 00:13:54:739] **Speaker 0:** could be in the 1000 range down to 1, and
[00:13:54:739 - 00:14:00:140] **Speaker 0:** your Effective impedance on the primary of your transformer will
[00:14:00:140 - 00:14:02:979] **Speaker 0:** fall down to almost zero, almost looking like a short
[00:14:02:979 - 00:14:03:599] **Speaker 0:** circuit.
[00:14:04:020 - 00:14:05:320] **Speaker 0:** So that's disastrous.
[00:14:05:859 - 00:14:07:979] **Speaker 0:** So definitely we are talking that the periodic flux in
[00:14:07:979 - 00:14:09:679] **Speaker 0:** the transformer must sum to 0.
[00:14:12:429 - 00:14:14:349] **Speaker 0:** So that means that the average change in the core
[00:14:14:349 - 00:14:17:469] **Speaker 0:** flux must also sum to zero.
[00:14:19:849 - 00:14:24:750] **Speaker 0:** Right, so, as modelled, the average change of an inductor,
[00:14:25:130 - 00:14:28:969] **Speaker 0:** the magnetising inductor current must equal 0.
[00:14:29:130 - 00:14:32:450] **Speaker 0:** So the rise of the current, it's just the same
[00:14:32:450 - 00:14:36:849] **Speaker 0:** as we, if we've got any actual inductor, that the
[00:14:36:849 - 00:14:39:489] **Speaker 0:** current ripple through it must on average be equal to
[00:14:39:489 - 00:14:39:989] **Speaker 0:** 0.
[00:14:45:409 - 00:14:49:690] **Speaker 1:** Um, right, so the magnetising inductance here is shown on
[00:14:49:690 - 00:14:53:849] **Speaker 0:** the primary, it would have been perfectly reasonable and just
[00:14:53:849 - 00:14:58:289] **Speaker 0:** as valid to model that inductance on the secondary side.
[00:14:59:179 - 00:15:02:739] **Speaker 0:** The reason we don't do that is because we usually
[00:15:02:739 - 00:15:05:659] **Speaker 0:** consider that the input, as I mentioned, of the transformer
[00:15:05:659 - 00:15:07:739] **Speaker 0:** is on the primary and the output is the secondary.
[00:15:08:140 - 00:15:12:619] **Speaker 0:** So most of the analysis is simplified for the magnetising
[00:15:12:619 - 00:15:14:500] **Speaker 0:** inductance if we model it on the primary.
[00:15:18:570 - 00:15:21:900] **Speaker 0:** OK, um, I also, before we leave this, uh, this
[00:15:21:900 - 00:15:26:700] **Speaker 0:** slide, I want to emphasise the dot convention used in
[00:15:26:700 - 00:15:27:659] **Speaker 0:** the transformer.
[00:15:28:450 - 00:15:30:950] **Speaker 0:** So we've got these kind of funny looking dots here.
[00:15:32:520 - 00:15:38:030] **Speaker 0:** And they are to provide information about the phasing nature
[00:15:38:450 - 00:15:40:849] **Speaker 0:** between the primary, well, between the windings.
[00:15:41:700 - 00:15:46:219] **Speaker 0:** So what this tells us is this for a current
[00:15:46:219 - 00:15:48:580] **Speaker 0:** flow situation, so I1 is shown to be in this
[00:15:48:580 - 00:15:52:539] **Speaker 1:** direction, it would say that with current flowing through the
[00:15:52:539 - 00:15:54:619] **Speaker 0:** winding in that way, that this side would be positive
[00:15:54:619 - 00:15:55:880] **Speaker 0:** and that side would be negative.
[00:15:57:469 - 00:15:59:809] **Speaker 0:** In this instant with the current flowing in that direction.
[00:16:01:039 - 00:16:04:200] **Speaker 0:** The dot convention tells us with the, with the windings
[00:16:04:200 - 00:16:09:440] **Speaker 0:** that, that must mean that all other windings with the
[00:16:09:440 - 00:16:11:559] **Speaker 0:** dot on the side, that side must be positive and
[00:16:11:559 - 00:16:13:260] **Speaker 0:** that side must be negative as well.
[00:16:15:429 - 00:16:19:559] **Speaker 0:** And any other potential windings associated with that core.
[00:16:20:599 - 00:16:22:539] **Speaker 0:** Transformers can have more than 2 windings.
[00:16:25:000 - 00:16:29:010] **Speaker 0:** OK, so if for whatever reason, the current was in
[00:16:29:010 - 00:16:30:130] **Speaker 0:** the opposite direction.
[00:16:30:979 - 00:16:33:380] **Speaker 0:** On the primary, where we got power flow, the current
[00:16:33:380 - 00:16:36:770] **Speaker 0:** was this way, then that must tell us then that,
[00:16:37:020 - 00:16:39:340] **Speaker 0:** and that would mean that this was the positive side
[00:16:39:340 - 00:16:40:400] **Speaker 0:** and that was negative.
[00:16:41:380 - 00:16:44:349] **Speaker 0:** That by the dot convention that we have then this
[00:16:44:349 - 00:16:46:369] **Speaker 0:** side would be positive and that would be negative.
[00:16:50:500 - 00:16:51:250] **Speaker 1:** OK.
[00:16:54:530 - 00:16:56:640] **Speaker 0:** So just keep that in mind because we're going to
[00:16:56:640 - 00:17:01:919] **Speaker 0:** be seeing transformers with dots identified with the windings, and
[00:17:01:919 - 00:17:06:479] **Speaker 0:** that tells us the phasing information about the polarity that
[00:17:06:479 - 00:17:10:780] **Speaker 0:** we see, the voltage polarity we see on those windings.
[00:17:12:790 - 00:17:16:869] **Speaker 1:** Right, those of you who haven't come across the dock
[00:17:16:869 - 00:17:19:160] **Speaker 0:** convention before, it'll start making more sense as we go
[00:17:19:160 - 00:17:20:160] **Speaker 0:** through some examples.
[00:17:28:239 - 00:17:30:979] **Speaker 0:** All right, let's have a look at our very first
[00:17:31:218 - 00:17:34:359] **Speaker 0:** DC to DC converter that has electrical isolation associated with
[00:17:34:359 - 00:17:34:578] **Speaker 0:** it.
[00:17:35:640 - 00:17:37:199] **Speaker 0:** And that's the flyback converter.
[00:17:38:140 - 00:17:39:959] **Speaker 0:** It's actually quite a popular converter.
[00:17:40:339 - 00:17:46:489] **Speaker 0:** Um, it's popular because it's actually as far as number
[00:17:46:489 - 00:17:49:520] **Speaker 0:** of components and the way it works, pretty simple.
[00:17:51:069 - 00:17:58:469] **Speaker 0:** And in fact, the isolated flyback converter um behaves in
[00:17:58:469 - 00:18:01:670] **Speaker 0:** all intents and purposes, almost exactly like a buck boost
[00:18:01:670 - 00:18:03:589] **Speaker 0:** converter that has no isolation.
[00:18:04:030 - 00:18:07:589] **Speaker 0:** So here we've got the isolated version, and here is
[00:18:07:589 - 00:18:11:869] **Speaker 0:** the equivalent of this in function of a non-isolated buck
[00:18:11:869 - 00:18:12:390] **Speaker 0:** boost converter.
[00:18:12:459 - 00:18:15:069] **Speaker 0:** It's drawn in a funny sort of way from what
[00:18:15:069 - 00:18:18:150] **Speaker 0:** we analysed before, but it's to just to try and
[00:18:18:150 - 00:18:21:089] **Speaker 0:** highlight or make the output stage look the same.
[00:18:22:479 - 00:18:24:959] **Speaker 0:** But this is a buck boost converter.
[00:18:25:829 - 00:18:27:010] **Speaker 0:** With a low side switch.
[00:18:28:729 - 00:18:32:410] **Speaker 0:** Uh, having said that, low side switch for our flyback
[00:18:32:410 - 00:18:36:449] **Speaker 0:** converter, it's nothing that could have stopped us theoretically from
[00:18:36:449 - 00:18:40:290] **Speaker 0:** having a high side switch, because it's in series, but
[00:18:40:290 - 00:18:42:810] **Speaker 0:** of course a high side switch has its issues about
[00:18:42:810 - 00:18:47:489] **Speaker 0:** how we drive it, um, given certain power supply restrictions.
[00:18:50:209 - 00:18:52:530] **Speaker 0:** Much easier to drive it if it's in its low
[00:18:52:530 - 00:18:53:430] **Speaker 0:** sides position.
[00:18:54:290 - 00:18:57:469] **Speaker 0:** And we don't have any issues with with a separate
[00:18:57:469 - 00:19:01:750] **Speaker 0:** um Earth, because we're expecting a separate Earth anyway.
[00:19:05:069 - 00:19:06:770] **Speaker 0:** Right, OK, so.
[00:19:08:560 - 00:19:11:319] **Speaker 0:** We can, since it is actually derived from a buck
[00:19:11:319 - 00:19:15:709] **Speaker 0:** boost converter, we could, by changing the duty ratio, have
[00:19:15:709 - 00:19:19:969] **Speaker 0:** an output with a voltage that um is either less
[00:19:19:969 - 00:19:22:619] **Speaker 0:** than or greater than the input voltage.
[00:19:23:369 - 00:19:24:569] **Speaker 0:** Depending on that duty ratio.
[00:19:24:650 - 00:19:27:479] **Speaker 0:** So as soon as you hit 0.5, the duty ratio,
[00:19:27:719 - 00:19:30:410] **Speaker 0:** anything above, you can step up the voltage, anything below,
[00:19:30:489 - 00:19:31:869] **Speaker 0:** you're stepping down the voltage.
[00:19:33:619 - 00:19:36:939] **Speaker 0:** Although that step up function, uh, is a little bit
[00:19:36:939 - 00:19:41:339] **Speaker 0:** redundant, uh, for the, for the buck boost because the
[00:19:41:339 - 00:19:44:780] **Speaker 0:** step up can actually be handled by the turns ratio
[00:19:45:020 - 00:19:46:160] **Speaker 0:** of our transformer.
[00:19:47:489 - 00:19:48:630] **Speaker 0:** That's a bit of a benefit.
[00:19:49:050 - 00:19:53:410] **Speaker 0:** Remember, we talked about the non-deal behaviour of the power
[00:19:53:410 - 00:19:58:010] **Speaker 0:** inductor, uh, in a boost or back boost converter, and
[00:19:58:010 - 00:20:00:439] **Speaker 0:** it stated that we can't get that duty ratio too
[00:20:00:439 - 00:20:04:250] **Speaker 0:** high, otherwise we don't start boosting the voltage anymore, we
[00:20:04:250 - 00:20:05:770] **Speaker 0:** actually have a reduction.
[00:20:06:479 - 00:20:07:900] **Speaker 0:** In the output voltage.
[00:20:08:359 - 00:20:11:000] **Speaker 0:** So, instead of going up to that really high duty
[00:20:11:000 - 00:20:14:459] **Speaker 0:** ratio, we can utilise the step-up function of the transformer
[00:20:14:599 - 00:20:17:650] **Speaker 0:** and work at a lower duty ratio where the inductor,
[00:20:18:119 - 00:20:20:060] **Speaker 0:** um, behaves more ideal.
[00:20:21:089 - 00:20:23:069] **Speaker 0:** As, as we would, would want it to be.
[00:20:26:770 - 00:20:27:489] **Speaker 1:** OK.
[00:20:28:609 - 00:20:31:209] **Speaker 0:** So luckily as well, since this is based on a
[00:20:31:209 - 00:20:33:270] **Speaker 0:** buck boost, a lot of the analysis.
[00:20:34:140 - 00:20:36:099] **Speaker 0:** Is the same as what we've just gone, what we
[00:20:36:099 - 00:20:38:380] **Speaker 0:** had gone through with the buck boost, so that's going
[00:20:38:380 - 00:20:39:079] **Speaker 0:** to be handy.
[00:20:41:640 - 00:20:42:010] **Speaker 1:** Hm.
[00:20:43:209 - 00:20:47:530] **Speaker 0:** Whilst this is one of the easiest isolated converters that's
[00:20:47:530 - 00:20:51:630] **Speaker 0:** out there, um, and it's operation is pretty, pretty basic,
[00:20:52:209 - 00:20:57:000] **Speaker 0:** um, it's utilising the isolation transformer in a way that
[00:20:57:000 - 00:21:00:709] **Speaker 0:** virtually no other isolated converter does.
[00:21:01:500 - 00:21:07:020] **Speaker 0:** It's utilising the transformer as the power inductor of the,
[00:21:07:130 - 00:21:08:160] **Speaker 0:** of the converter.
[00:21:09:199 - 00:21:12:349] **Speaker 0:** It's essentially turned into a two winding inductor.
[00:21:14:010 - 00:21:16:550] **Speaker 0:** As used in the circuit rather than a transformer.
[00:21:19:959 - 00:21:21:790] **Speaker 0:** It's a bit, it's a bit of a mind stretch,
[00:21:21:880 - 00:21:25:839] **Speaker 0:** but it's all of the theory still is valid that
[00:21:25:839 - 00:21:27:400] **Speaker 0:** we would look at for a transformer.
[00:21:27:439 - 00:21:29:959] **Speaker 0:** It's just that a lot of energy is, is intended
[00:21:29:959 - 00:21:34:089] **Speaker 0:** to be stored in the core of that transformer.
[00:21:34:560 - 00:21:38:040] **Speaker 0:** And usually, for our power electronic converters, the transformer is
[00:21:38:040 - 00:21:42:479] **Speaker 0:** there to efficiently transfer energy without storing much within the
[00:21:42:479 - 00:21:45:020] **Speaker 0:** core itself, within the transformer itself.
[00:21:47:550 - 00:21:52:150] **Speaker 0:** That energy storage requirement actually starts to become a problem
[00:21:52:150 - 00:21:53:739] **Speaker 0:** at higher levels of energy.
[00:21:53:949 - 00:21:56:709] **Speaker 0:** You're trying to store a bunch of that in the
[00:21:56:709 - 00:22:01:430] **Speaker 0:** core cycle by cycle, um, and it starts to introduce
[00:22:01:430 - 00:22:06:010] **Speaker 0:** losses that are hard to justify for higher power converters.
[00:22:06:510 - 00:22:09:270] **Speaker 0:** So you tend to find flyback converters aren't used for
[00:22:09:270 - 00:22:10:949] **Speaker 0:** anything beyond about 200 watts.
[00:22:12:020 - 00:22:13:770] **Speaker 0:** As far as your power conversion goes.
[00:22:16:500 - 00:22:19:180] **Speaker 0:** Uh, but up to around 100 watts or so, it's
[00:22:19:180 - 00:22:22:400] **Speaker 0:** an extremely popular converter because of its simplicity.
[00:22:25:890 - 00:22:30:010] **Speaker 0:** Um, and because we're using ferrites for the high frequency
[00:22:30:010 - 00:22:35:219] **Speaker 0:** operation, um, to store that energy, the, um, converter will
[00:22:35:219 - 00:22:39:099] **Speaker 0:** need to introduce an air gap, just like your inductor
[00:22:39:430 - 00:22:41:219] **Speaker 0:** for your buck converter needs to have an air gap
[00:22:41:219 - 00:22:43:300] **Speaker 0:** in order to be able to store the energy it
[00:22:43:300 - 00:22:43:969] **Speaker 0:** needs to.
[00:22:44:420 - 00:22:47:020] **Speaker 0:** This is effectively a two winding conductor and it will
[00:22:47:020 - 00:22:48:359] **Speaker 0:** also need an air gap.
[00:22:54:839 - 00:22:58:270] **Speaker 0:** Right, we need to analyse this, uh, go through its
[00:22:58:270 - 00:23:00:579] **Speaker 0:** operation and check out what's happening with the converter.
[00:23:09:709 - 00:23:13:619] **Speaker 0:** Alright, so In a circuit diagram equivalent.
[00:23:14:199 - 00:23:18:689] **Speaker 0:** Um, here we have the converter, here's the transformer, a
[00:23:18:689 - 00:23:22:920] **Speaker 0:** single controlled switch input DC supply, and here's our output.
[00:23:24:209 - 00:23:27:459] **Speaker 0:** Free wheeling diode, philtre capacitor and load.
[00:23:28:989 - 00:23:32:510] **Speaker 0:** The switch operates in two states as usual, either it's
[00:23:32:510 - 00:23:35:510] **Speaker 0:** closed, in which case it looks like a a dead
[00:23:35:510 - 00:23:37:189] **Speaker 0:** short, or it's open, in which case it looks like
[00:23:37:189 - 00:23:37:989] **Speaker 0:** an open circuit.
[00:23:38:349 - 00:23:40:510] **Speaker 0:** So these are the two equivalent circuits that we end
[00:23:40:510 - 00:23:44:109] **Speaker 0:** up with, with the switch is closed or whether the
[00:23:44:109 - 00:23:44:890] **Speaker 0:** switch is open.
[00:23:46:069 - 00:23:50:650] **Speaker 0:** OK, we'll analyse those, but be aware that the transformer
[00:23:51:630 - 00:23:55:189] **Speaker 0:** includes this modelled magnetising inductance.
[00:23:56:839 - 00:24:01:040] **Speaker 0:** So when we say I1 being the primary current is
[00:24:01:040 - 00:24:04:719] **Speaker 0:** different to IS which is being the source current, that
[00:24:04:719 - 00:24:09:359] **Speaker 0:** is just a uh a result of the model that's
[00:24:09:359 - 00:24:10:219] **Speaker 0:** being used.
[00:24:12:569 - 00:24:16:390] **Speaker 0:** If we were to actually have a physical transformer or
[00:24:16:770 - 00:24:20:849] **Speaker 0:** this power inductor, we'd only have 4 terminals, 1234, that
[00:24:20:849 - 00:24:22:150] **Speaker 0:** we have access to.
[00:24:23:300 - 00:24:27:550] **Speaker 0:** Right, so Um, that current IS is the only thing
[00:24:27:550 - 00:24:30:390] **Speaker 0:** that we would actually be able to physically measure.
[00:24:30:579 - 00:24:34:089] **Speaker 0:** We can't measure this difference between ILM and I1.
[00:24:36:000 - 00:24:38:479] **Speaker 0:** They will only ever be added together to be what
[00:24:38:479 - 00:24:39:180] **Speaker 0:** you can measure.
[00:24:39:900 - 00:24:41:579] **Speaker 0:** At the primary of the transformer.
[00:24:44:949 - 00:24:45:380] **Speaker 0:** OK.
[00:24:47:949 - 00:24:51:680] **Speaker 0:** Uh, please remember that all of these DC to DC
[00:24:51:680 - 00:24:54:319] **Speaker 0:** converters that we're looking at, we're looking at it in
[00:24:54:319 - 00:24:55:260] **Speaker 0:** steady state.
[00:24:56:459 - 00:24:59:250] **Speaker 0:** Uh, so all the voltage and current fluctuations are periodic.
[00:25:00:189 - 00:25:03:949] **Speaker 0:** Um, we are going to be assuming ideal operations, so
[00:25:03:949 - 00:25:06:189] **Speaker 0:** power supplied by the source equals the power delivered to
[00:25:06:189 - 00:25:06:849] **Speaker 0:** the load.
[00:25:07:599 - 00:25:10:670] **Speaker 0:** If we ever mention non-ideal behaviour, it would be plus
[00:25:10:670 - 00:25:12:130] **Speaker 0:** any non-ideal losses.
[00:25:13:150 - 00:25:15:589] **Speaker 0:** Uh, and the philtre capacitor, we're going to say is
[00:25:15:589 - 00:25:18:310] **Speaker 0:** large enough to say that the output voltage for all
[00:25:18:310 - 00:25:19:910] **Speaker 0:** intents and purposes is constant.
[00:25:31:189 - 00:25:34:670] **Speaker 0:** Alright, so let's go through the flyback circuit for the
[00:25:34:670 - 00:25:36:479] **Speaker 0:** two states when the switch is closed and when it's
[00:25:36:479 - 00:25:36:829] **Speaker 0:** open.
[00:25:39:010 - 00:25:42:839] **Speaker 0:** So When the switch is closed, we're gonna have current
[00:25:42:839 - 00:25:45:689] **Speaker 0:** flowing into the primary of the transformer.
[00:25:46:680 - 00:25:50:920] **Speaker 0:** Um, and that will magnetise the core, and we will
[00:25:50:920 - 00:25:56:040] **Speaker 0:** experience a magnetization current for the magnetising inductance.
[00:25:58:040 - 00:26:01:400] **Speaker 0:** Right, and that's being, of course, magnetised the transformer core
[00:26:01:400 - 00:26:03:479] **Speaker 0:** being modelled by that magnetising inductance.
[00:26:04:459 - 00:26:07:619] **Speaker 0:** So we do have a uh a current that we
[00:26:07:619 - 00:26:12:459] **Speaker 0:** would measure from the source, but since from the dot
[00:26:12:459 - 00:26:14:880] **Speaker 0:** product, we see we got plus minus here.
[00:26:15:880 - 00:26:19:640] **Speaker 0:** We then must buy the dot product, uh, dot product,
[00:26:19:839 - 00:26:23:959] **Speaker 0:** by the dot convention, uh, experience plus minus that way
[00:26:23:959 - 00:26:26:829] **Speaker 0:** around, because see, there's the dot there, tells us the
[00:26:26:829 - 00:26:28:079] **Speaker 0:** phase relationship.
[00:26:28:280 - 00:26:32:560] **Speaker 0:** Since this side's positive, with the, um, because of the
[00:26:32:560 - 00:26:36:040] **Speaker 0:** current flow through the magnetising inductance, then this side must
[00:26:36:040 - 00:26:37:260] **Speaker 0:** be positive on the secondary.
[00:26:39:540 - 00:26:43:089] **Speaker 0:** With the diode connected that way around in the circuit,
[00:26:43:339 - 00:26:45:119] **Speaker 0:** that means the diode's reverse biassed.
[00:26:47:150 - 00:26:51:160] **Speaker 0:** Alright, positive through to negative, so positive to the negative
[00:26:51:160 - 00:26:54:640] **Speaker 0:** side, it's reverse bias, it cannot conduct and it looks
[00:26:54:640 - 00:26:55:780] **Speaker 0:** like an open circuit.
[00:26:58:239 - 00:27:02:689] **Speaker 0:** All right, so the current, We call this I2.
[00:27:03:079 - 00:27:05:939] **Speaker 0:** The current in that secondary one is 0.
[00:27:12:810 - 00:27:16:650] **Speaker 0:** Right, so that's something that a lot of people initially
[00:27:16:650 - 00:27:19:810] **Speaker 0:** don't, uh, it's difficult to understand.
[00:27:19:890 - 00:27:21:550] **Speaker 0:** We have primary current.
[00:27:22:680 - 00:27:25:839] **Speaker 0:** Well, we have current that comes from the source, so
[00:27:25:839 - 00:27:27:060] **Speaker 0:** there is current flowing.
[00:27:28:900 - 00:27:31:760] **Speaker 0:** Here, but there is no current flowing on the secondary.
[00:27:33:849 - 00:27:38:349] **Speaker 0:** All we are doing at the moment is imparting energy
[00:27:38:349 - 00:27:41:170] **Speaker 0:** to the magnetic field in, or the magnetic flux in
[00:27:41:170 - 00:27:41:739] **Speaker 0:** the core.
[00:27:51:900 - 00:27:55:699] **Speaker 0:** So, if I2 equals 0, then by this model, we
[00:27:55:699 - 00:28:00:819] **Speaker 0:** have an I1, which is our primary winding current.
[00:28:01:849 - 00:28:04:609] **Speaker 0:** Because of all the currents flowing through the magnetising conductance,
[00:28:04:689 - 00:28:07:910] **Speaker 0:** that I1 is also equal to 0.
[00:28:13:630 - 00:28:15:719] **Speaker 1:** All right, and then the source current is simply equal
[00:28:15:719 - 00:28:16:640] **Speaker 0:** to ILM.
[00:28:20:430 - 00:28:24:030] **Speaker 0:** Right, so we've got this condition or state where we
[00:28:24:030 - 00:28:28:369] **Speaker 0:** have connected a DC supply across what appears to be
[00:28:28:510 - 00:28:32:869] **Speaker 0:** a fixed value of inductance of LM.
[00:28:33:939 - 00:28:37:339] **Speaker 0:** We've done this many times before now, where we've got
[00:28:37:339 - 00:28:41:800] **Speaker 0:** a DC supply or a DC voltage across an inductor.
[00:28:42:099 - 00:28:43:699] **Speaker 0:** What's the current going to do if we've got a
[00:28:43:699 - 00:28:45:640] **Speaker 0:** DC voltage across an inductor?
[00:28:49:390 - 00:28:50:989] **Speaker 0:** It'll ramp, yep, it'll ramp up.
[00:28:51:229 - 00:28:54:810] **Speaker 0:** It'll ramp up because energy is being put into That
[00:28:54:810 - 00:28:55:630] **Speaker 0:** inductor.
[00:28:56:170 - 00:29:00:089] **Speaker 0:** So delta ILM with with the switch closed is equal
[00:29:00:089 - 00:29:04:209] **Speaker 0:** to VS because that's the voltage across the magnetising inductance.
[00:29:05:089 - 00:29:08:209] **Speaker 0:** DT because that's the period of time that the switch
[00:29:08:209 - 00:29:13:150] **Speaker 0:** is on, um, divided by the actual inductance value itself.
[00:29:17:599 - 00:29:24:640] **Speaker 0:** That maybe that, that will look uh uh familiar because
[00:29:24:640 - 00:29:26:880] **Speaker 0:** that is the identical expression to what we have for
[00:29:26:880 - 00:29:29:400] **Speaker 0:** a buck boost converter when the switch is closed.
[00:29:30:250 - 00:29:31:689] **Speaker 0:** It's also the same expression as we have for a
[00:29:31:689 - 00:29:34:030] **Speaker 0:** boost converter when the switch is closed, but yeah.
[00:29:36:219 - 00:29:39:020] **Speaker 0:** OK, so we don't we don't have anything new there.
[00:29:39:459 - 00:29:40:560] **Speaker 0:** We've done that before.
[00:29:47:540 - 00:29:51:969] **Speaker 1:** We've said That the output, uh has a capacitor that
[00:29:51:969 - 00:29:55:680] **Speaker 0:** means that, that stays constant at the out.
[00:29:57:250 - 00:29:59:560] **Speaker 0:** Whilst we've got the switch closed.
[00:30:00:260 - 00:30:05:060] **Speaker 0:** And that diode is reverse biassed, the average current eye
[00:30:05:060 - 00:30:09:300] **Speaker 0:** out is being um supplied solely by the philtre capacitor.
[00:30:20:219 - 00:30:22:560] **Speaker 0:** As it was for our buck boost converter.
[00:30:24:250 - 00:30:31:699] **Speaker 0:** Right Are we following?
[00:30:33:109 - 00:30:33:930] **Speaker 0:** Any questions?
[00:30:37:689 - 00:30:40:849] **Speaker 0:** Alright, so next up, this is where things get a
[00:30:40:849 - 00:30:41:609] **Speaker 0:** little bit curly.
[00:30:42:180 - 00:30:43:719] **Speaker 0:** Um, we'll open the switch.
[00:30:51:510 - 00:30:54:109] **Speaker 1:** Right, when the switch is open, the core magnetic flux
[00:30:54:109 - 00:30:55:290] **Speaker 0:** begins to collapse.
[00:30:56:229 - 00:30:56:689] **Speaker 1:** Yeah.
[00:30:58:790 - 00:31:01:369] **Speaker 0:** So we open the switch, we stop.
[00:31:02:550 - 00:31:06:729] **Speaker 0:** The source current, I is equals 0.
[00:31:10:729 - 00:31:14:880] **Speaker 0:** But with If we take it back to the equivalent
[00:31:14:880 - 00:31:18:459] **Speaker 0:** inductance to model what's happening in the core, we've got
[00:31:18:920 - 00:31:21:660] **Speaker 0:** the situation where we've energised that inductance.
[00:31:23:290 - 00:31:26:489] **Speaker 0:** And we had current flowing through it in this direction.
[00:31:26:569 - 00:31:27:810] **Speaker 0:** That was ILM.
[00:31:29:439 - 00:31:33:859] **Speaker 0:** And it had a voltage plus minus VS across it.
[00:31:36:750 - 00:31:39:989] **Speaker 0:** What happens when we try to stop the current flow
[00:31:39:989 - 00:31:45:630] **Speaker 0:** through the inductor, and it starts to de-energize, its voltage
[00:31:45:630 - 00:31:46:349] **Speaker 1:** flips.
[00:31:49:900 - 00:31:54:479] **Speaker 1:** And we'll try to keep that current flowing in the
[00:31:54:479 - 00:31:55:780] **Speaker 0:** same direction.
[00:31:56:609 - 00:31:58:589] **Speaker 0:** So it becomes an energy source.
[00:31:58:930 - 00:32:02:869] **Speaker 0:** So if that's the case, then we've got plus minus
[00:32:03:609 - 00:32:04:949] **Speaker 0:** across the primary winding.
[00:32:07:229 - 00:32:11:939] **Speaker 0:** All right, and on this side, it becomes, as it's
[00:32:11:939 - 00:32:14:459] **Speaker 0:** shown here, plus minus.
[00:32:14:750 - 00:32:16:229] **Speaker 0:** Oh, sorry, no.
[00:32:18:180 - 00:32:21:510] **Speaker 1:** Plus Minus.
[00:32:25:819 - 00:32:28:290] **Speaker 0:** Which is the same polarity as the output voltage.
[00:32:31:760 - 00:32:40:020] **Speaker 0:** Right, so, That ILM is being modelled as showing as
[00:32:40:020 - 00:32:44:619] **Speaker 0:** flowing through the primary, which means that uh Since that's
[00:32:45:040 - 00:32:48:199] **Speaker 0:** the case, we would expect a current to be flowing
[00:32:48:199 - 00:32:58:369] **Speaker 0:** out of that side of the Winding Uh, which is,
[00:32:58:430 - 00:33:01:750] **Speaker 0:** uh, the forward current, that's our dive current, but is
[00:33:01:750 - 00:33:05:050] **Speaker 0:** also, um, equal to the output current.
[00:33:09:579 - 00:33:13:199] **Speaker 0:** Assuming no voltage ripple for the capacitor.
[00:33:16:109 - 00:33:18:130] **Speaker 0:** What's the tricky thing to get your head around here
[00:33:18:130 - 00:33:23:489] **Speaker 0:** is that the voltage that we see here is specifically
[00:33:23:489 - 00:33:25:319] **Speaker 0:** related to the voltage that we see at the output.
[00:33:25:369 - 00:33:28:270] **Speaker 0:** Remember, this is being fixed by the output voltage.
[00:33:29:380 - 00:33:34:189] **Speaker 0:** Of the, of the converter, so we have Plus minus
[00:33:34:189 - 00:33:38:750] **Speaker 0:** the out, which, according to the convention that we used
[00:33:38:750 - 00:33:41:920] **Speaker 0:** before, with this being the dot side being positive or
[00:33:41:920 - 00:33:44:910] **Speaker 0:** negative, is V2 equals minus the out.
[00:33:45:650 - 00:33:48:319] **Speaker 0:** The magnitude is there, but by the convention, it's just
[00:33:48:729 - 00:33:49:560] **Speaker 0:** a negative sign.
[00:33:50:849 - 00:33:55:339] **Speaker 1:** That is what gets transferred back to the primary.
[00:33:56:300 - 00:34:00:500] **Speaker 0:** So transformer windings and the voltage ratio isn't just one
[00:34:00:500 - 00:34:00:959] **Speaker 0:** way.
[00:34:02:780 - 00:34:06:219] **Speaker 0:** It depends on which side has the current flowing, it's
[00:34:06:219 - 00:34:08:780] **Speaker 0:** considered to be the source, and which side is considered
[00:34:08:780 - 00:34:10:439] **Speaker 0:** to be the output side.
[00:34:11:449 - 00:34:16:330] **Speaker 0:** Uh So, in this instance, with the current flowing through
[00:34:16:330 - 00:34:19:850] **Speaker 0:** the primary, then it is causing the voltages on all
[00:34:19:850 - 00:34:21:010] **Speaker 0:** the other windings.
[00:34:21:530 - 00:34:24:850] **Speaker 0:** So the turns ratio that we use now is, because
[00:34:24:860 - 00:34:27:388] **Speaker 0:** we're looking at the voltage on the, on the primary
[00:34:27:388 - 00:34:30:560] **Speaker 0:** winding, because of what's happening on the secondary is N1
[00:34:30:560 - 00:34:31:550] **Speaker 0:** over N2.
[00:34:33:600 - 00:34:36:860] **Speaker 0:** All right, and that is times, what is that voltage
[00:34:36:860 - 00:34:38:679] **Speaker 0:** on the, on the secondary is minus VR.
[00:34:40:099 - 00:34:43:729] **Speaker 0:** So your primary voltage is equal to minus V times
[00:34:43:729 - 00:34:44:759] **Speaker 0:** N1 over N2.
[00:34:53:030 - 00:34:56:350] **Speaker 0:** That's why this magnetising inductance modelled on the primary is
[00:34:56:350 - 00:34:59:510] **Speaker 0:** a little bit misleading because there is no primary current
[00:34:59:510 - 00:35:00:709] **Speaker 0:** flowing here.
[00:35:00:989 - 00:35:05:209] **Speaker 0:** It is the flux within the core that is collapsing.
[00:35:05:510 - 00:35:08:830] **Speaker 0:** There is current flowing on the secondary because of the,
[00:35:08:919 - 00:35:11:469] **Speaker 0:** the now the voltage change and forward biassing that died.
[00:35:11:790 - 00:35:14:979] **Speaker 0:** So that energy that was in the core is being
[00:35:14:979 - 00:35:16:689] **Speaker 0:** transferred to the output.
[00:35:17:469 - 00:35:21:370] **Speaker 0:** There is no energy transferred at the input.
[00:35:27:000 - 00:35:31:459] **Speaker 0:** Right, so, that is the, the voltage, um, at the
[00:35:31:459 - 00:35:31:939] **Speaker 0:** input.
[00:35:32:120 - 00:35:36:360] **Speaker 0:** We've still got this modelled um magnetising inductance and we
[00:35:36:360 - 00:35:37:540] **Speaker 0:** are modelling.
[00:35:38:350 - 00:35:44:030] **Speaker 0:** An inductor current, so LMDI by DT is equal to
[00:35:44:030 - 00:35:47:189] **Speaker 0:** V1, which we've just said is minus V M1 over
[00:35:47:189 - 00:35:47:729] **Speaker 0:** N2.
[00:35:59:149 - 00:36:05:179] **Speaker 0:** So sometimes, it's actually more uh instructive and better to
[00:36:05:179 - 00:36:09:159] **Speaker 0:** get uh a practical working idea of thinking about the
[00:36:09:159 - 00:36:12:340] **Speaker 0:** flux rather than the modelled magnetising inductance.
[00:36:12:620 - 00:36:15:260] **Speaker 0:** We have this here because it makes the circuit analysis
[00:36:15:260 - 00:36:15:739] **Speaker 0:** easier.
[00:36:24:229 - 00:36:24:669] **Speaker 0:** Right.
[00:36:28:129 - 00:36:31:659] **Speaker 0:** So the switch then is open for a time that's
[00:36:31:659 - 00:36:33:320] **Speaker 0:** equal to 1 minus DT.
[00:36:34:360 - 00:36:39:250] **Speaker 0:** And we've already stated that that change in magnetising inductance
[00:36:39:250 - 00:36:43:969] **Speaker 0:** current um is from the previous expression, we just rearranged
[00:36:43:969 - 00:36:48:179] **Speaker 0:** that, so that delta ILM open is minus V out
[00:36:48:179 - 00:36:48:850] **Speaker 0:** over LM.
[00:36:48:969 - 00:36:51:560] **Speaker 0:** Here's their scaling by N1 over N2, and just the
[00:36:51:560 - 00:36:53:050] **Speaker 0:** time period that the switch is open.
[00:36:57:159 - 00:36:59:360] **Speaker 0:** It's almost the same as the buck boost converter as
[00:36:59:360 - 00:37:00:600] **Speaker 0:** far as an expression is concerned.
[00:37:00:669 - 00:37:03:360] **Speaker 0:** It's just scaled by N1 over N2 because we are
[00:37:03:360 - 00:37:06:540] **Speaker 0:** using this two-turn inductor.
[00:37:15:979 - 00:37:19:909] **Speaker 0:** Right, so we've got some Uh, indicative wave forms here.
[00:37:20:070 - 00:37:23:070] **Speaker 0:** So, ILM, this is the model of magnetising inductance.
[00:37:23:179 - 00:37:26:149] **Speaker 0:** When the switch is closed from time 0 to DT,
[00:37:26:709 - 00:37:30:689] **Speaker 0:** we have the current ramping up in that inductance.
[00:37:31:770 - 00:37:33:610] **Speaker 0:** It would be just as it would be for our
[00:37:33:610 - 00:37:34:889] **Speaker 0:** um buck boost converter.
[00:37:35:899 - 00:37:40:260] **Speaker 0:** Here's the, the um source current, it's equal to the
[00:37:40:260 - 00:37:42:679] **Speaker 0:** magnetising current, inductance current.
[00:37:45:060 - 00:37:50:179] **Speaker 0:** The um diode current that's on the secondary side, the
[00:37:50:179 - 00:37:52:679] **Speaker 0:** free-wheeling diode current, that's zero because it's reverse biassed.
[00:37:54:560 - 00:37:58:209] **Speaker 0:** The voltage across the capacitor is, it is minus B
[00:37:58:209 - 00:37:58:800] **Speaker 0:** out overr.
[00:37:58:889 - 00:38:01:639] **Speaker 0:** This is just by the convention that we've got, um,
[00:38:01:929 - 00:38:02:510] **Speaker 0:** so.
[00:38:03:729 - 00:38:05:229] **Speaker 0:** That's the capacitor current.
[00:38:05:570 - 00:38:08:090] **Speaker 0:** It's a constant, remember, uh.
[00:38:21:320 - 00:38:25:750] **Speaker 0:** It's a constant because when we have the um the
[00:38:25:760 - 00:38:29:159] **Speaker 0:** switch on reverse bias, we've just got the capacitor connected
[00:38:29:159 - 00:38:32:000] **Speaker 0:** to the load and that is at eye out.
[00:38:32:520 - 00:38:34:709] **Speaker 0:** So that's why the capacitor current is eye out.
[00:38:34:860 - 00:38:38:189] **Speaker 0:** It's leaving the capacitor and by convention we're, we're saying
[00:38:38:189 - 00:38:41:800] **Speaker 0:** that positive current for a capacitor is into the current,
[00:38:41:879 - 00:38:43:520] **Speaker 0:** so it's charging current.
[00:38:43:810 - 00:38:48:219] **Speaker 0:** This is now discharging the capacitor, so it's negative current.
[00:38:49:790 - 00:38:51:610] **Speaker 0:** Hence the negative current and it's constant.
[00:38:55:639 - 00:39:01:580] **Speaker 0:** And the voltage across the um Uh, primary winding is,
[00:39:01:719 - 00:39:02:360] **Speaker 0:** that's the one.
[00:39:02:639 - 00:39:06:120] **Speaker 0:** The voltage across it is VS when the switch is
[00:39:06:120 - 00:39:06:540] **Speaker 0:** closed.
[00:39:08:629 - 00:39:11:590] **Speaker 0:** Then we open the switch from time DT to T.
[00:39:11:750 - 00:39:16:689] **Speaker 0:** So 1 minus D times D, the The flux in
[00:39:16:689 - 00:39:19:840] **Speaker 0:** the cord collapses, we see this ramping down of the
[00:39:19:840 - 00:39:22:340] **Speaker 0:** current in the modelled magnetising inductance.
[00:39:24:429 - 00:39:26:820] **Speaker 0:** When that happens, there is no source current.
[00:39:28:719 - 00:39:29:139] **Speaker 0:** Alright.
[00:39:30:040 - 00:39:33:010] **Speaker 0:** The diode current looks like the ramping down.
[00:39:34:129 - 00:39:36:830] **Speaker 0:** Current from the magnetising inductance.
[00:39:37:330 - 00:39:40:689] **Speaker 0:** It's, but it is passed through the, um, passed through
[00:39:40:689 - 00:39:41:850] **Speaker 0:** the, the transformer.
[00:39:42:290 - 00:39:44:689] **Speaker 0:** For this to be the same magnitude as shown in
[00:39:44:689 - 00:39:47:530] **Speaker 0:** these graphs, that must mean that N1 equals N2.
[00:39:47:610 - 00:39:49:909] **Speaker 0:** It's a just a 1 to 1 transformer.
[00:39:50:850 - 00:39:52:489] **Speaker 0:** For those to be the same magnitude.
[00:39:55:270 - 00:39:59:600] **Speaker 0:** If we had N1 greater than N2.
[00:40:01:239 - 00:40:05:310] **Speaker 0:** So it was a step down transformer, then you would
[00:40:05:310 - 00:40:09:260] **Speaker 0:** expect the, uh, current to correspondingly step up.
[00:40:16:500 - 00:40:19:739] **Speaker 0:** Cause remember, it's the voltage current product, which is the
[00:40:19:739 - 00:40:20:179] **Speaker 0:** power.
[00:40:20:419 - 00:40:23:020] **Speaker 0:** We've got the same power on both sides, so if
[00:40:23:020 - 00:40:26:340] **Speaker 0:** we've got now a higher um voltage on the primary
[00:40:26:340 - 00:40:29:020] **Speaker 0:** than the secondary, stepping down the voltage, the current gets
[00:40:29:020 - 00:40:32:699] **Speaker 0:** stepped up to to give you the same uh product
[00:40:32:699 - 00:40:33:699] **Speaker 0:** between voltage and current.
[00:40:36:110 - 00:40:36:729] **Speaker 1:** Alright.
[00:40:39:850 - 00:40:43:689] **Speaker 1:** Now, uh, and of course, the capacitor current, it takes
[00:40:43:689 - 00:40:46:679] **Speaker 0:** all of the ripple of the, the current, so that
[00:40:46:679 - 00:40:48:530] **Speaker 0:** you end up with a constant current as far as
[00:40:48:530 - 00:40:50:770] **Speaker 0:** the load resistance is concerned.
[00:40:52:870 - 00:40:55:090] **Speaker 0:** We've got the average fluctuation inductor current.
[00:40:56:350 - 00:41:00:550] **Speaker 0:** Uh, Or average inductive voltage must be equal to 0.
[00:41:01:889 - 00:41:08:889] **Speaker 0:** I have put on learn a fully um derived set
[00:41:08:889 - 00:41:11:689] **Speaker 0:** of uh or a full derivation of how we get
[00:41:11:689 - 00:41:17:449] **Speaker 0:** from this state and the equation associated with having um
[00:41:17:449 - 00:41:20:570] **Speaker 0:** average fluctuation inducting current being equals zero or the average
[00:41:20:570 - 00:41:23:989] **Speaker 0:** inductive voltage being equals 0 to come up with this
[00:41:24:770 - 00:41:26:270] **Speaker 0:** expression, actually.
[00:41:30:610 - 00:41:33:449] **Speaker 0:** No, I've done that for continuous current design.
[00:41:34:550 - 00:41:37:090] **Speaker 0:** I haven't done that as an expression, but I will
[00:41:37:709 - 00:41:39:389] **Speaker 0:** do it right now.
[00:41:40:290 - 00:41:41:669] **Speaker 0:** So how do we get to this?
[00:41:42:330 - 00:41:44:469] **Speaker 0:** Well, we'll look at starting at this point here.
[00:41:44:810 - 00:41:47:370] **Speaker 0:** Um, by the way, this expression is just the same
[00:41:47:370 - 00:41:49:050] **Speaker 0:** as it is for the black boost, but scaled by
[00:41:49:050 - 00:41:50:229] **Speaker 0:** N1 over N2.
[00:41:51:780 - 00:41:55:449] **Speaker 0:** Right, that's right, I wanted to show two different ways.
[00:41:56:919 - 00:41:59:770] **Speaker 0:** of coming up with that um voltage relationship between the
[00:41:59:770 - 00:42:02:350] **Speaker 0:** input and output, due to the duty ratio.
[00:42:11:350 - 00:42:14:629] **Speaker 1:** Right, so one is based on um just looking at
[00:42:14:629 - 00:42:17:449] **Speaker 0:** the uh change in current.
[00:42:19:520 - 00:42:20:709] **Speaker 0:** Actually, the voltage.
[00:42:22:330 - 00:42:25:820] **Speaker 0:** So if we look at the voltage And we say
[00:42:25:820 - 00:42:27:780] **Speaker 0:** that the average voltage has to equal 0, then we've
[00:42:27:780 - 00:42:30:580] **Speaker 0:** got VS times DT.
[00:42:32:040 - 00:42:36:270] **Speaker 0:** Plus minus the N1 over NT 1 minus DT must
[00:42:36:270 - 00:42:37:290] **Speaker 0:** equal to 0.
[00:42:38:780 - 00:42:43:899] **Speaker 0:** So BS DT plus minus.
[00:42:45:040 - 00:42:49:370] **Speaker 1:** The out In one over into.
[00:42:52:080 - 00:42:54:760] **Speaker 0:** 1 minus DT equals 0.
[00:43:00:860 - 00:43:03:540] **Speaker 0:** We get the tease cancelling, so we'll be left with
[00:43:03:540 - 00:43:04:379] **Speaker 0:** VSD.
[00:43:05:600 - 00:43:08:979] **Speaker 0:** Equals, I'll bring the, since this is negative, we'll bring
[00:43:08:979 - 00:43:11:879] **Speaker 0:** that onto the other side, equals V out.
[00:43:13:199 - 00:43:16:580] **Speaker 0:** N1 over N2, 1 minus D.
[00:43:17:889 - 00:43:21:729] **Speaker 0:** So that we're left with V out over VS is
[00:43:21:729 - 00:43:26:689] **Speaker 0:** equal to N2 over N1, D over 1 minus D.
[00:43:28:090 - 00:43:29:360] **Speaker 0:** Pretty quick and easy, right?
[00:43:32:530 - 00:43:34:229] **Speaker 0:** There is another way that we could look at it,
[00:43:34:340 - 00:43:38:810] **Speaker 0:** and this actually just highlights the fact of the flux
[00:43:38:810 - 00:43:42:750] **Speaker 0:** change within the core is really driving this whole process.
[00:43:43:800 - 00:43:52:090] **Speaker 0:** By Faraday's law, We've got the voltage across the winding.
[00:43:53:129 - 00:44:00:199] **Speaker 0:** And the transformer is equal to ND5 by DT, the
[00:44:00:199 - 00:44:02:600] **Speaker 0:** rate of change of the flux in the core.
[00:44:04:600 - 00:44:07:899] **Speaker 0:** Which is going to give us that the delta Phi
[00:44:08:320 - 00:44:11:000] **Speaker 0:** is equal to V over N.
[00:44:11:949 - 00:44:12:590] **Speaker 0:** Delta T.
[00:44:13:439 - 00:44:15:939] **Speaker 0:** OK, this is linearly changing flux.
[00:44:18:570 - 00:44:23:879] **Speaker 1:** So if we plot that, The flux, we've got DT.
[00:44:24:729 - 00:44:26:100] **Speaker 0:** And tea.
[00:44:30:479 - 00:44:37:060] **Speaker 0:** Then we have Um, ramping up flux whilst the switch
[00:44:37:060 - 00:44:37:760] **Speaker 0:** is closed.
[00:44:38:580 - 00:44:41:840] **Speaker 0:** OK, we're imparting energy to the core of the transformer,
[00:44:42:260 - 00:44:47:290] **Speaker 0:** and then, when it's Open that flux ramps down.
[00:44:48:199 - 00:44:49:040] **Speaker 0:** What is the slope?
[00:44:49:270 - 00:44:54:439] **Speaker 0:** Well, the slope from this is VS Over in one,
[00:44:54:560 - 00:44:55:500] **Speaker 1:** is the voltage.
[00:44:59:270 - 00:45:01:110] **Speaker 1:** Right, when the switch is closed, and when the switch
[00:45:01:110 - 00:45:04:090] **Speaker 0:** is open, the, the, the voltage is minus the out.
[00:45:05:149 - 00:45:07:100] **Speaker 0:** Uh, and the number of turns is N2.
[00:45:09:679 - 00:45:10:860] **Speaker 1:** And that just repeats.
[00:45:13:310 - 00:45:14:739] **Speaker 0:** We know that the delta.
[00:45:17:040 - 00:45:17:979] **Speaker 0:** Average.
[00:45:19:610 - 00:45:20:760] **Speaker 0:** S to equals 0.
[00:45:22:530 - 00:45:25:810] **Speaker 0:** Changing the flux, so this, it's just like it is
[00:45:25:810 - 00:45:28:350] **Speaker 0:** for the case for the current in the inductor.
[00:45:30:600 - 00:45:33:939] **Speaker 0:** So we've got VS over N1DT.
[00:45:35:530 - 00:45:40:489] **Speaker 0:** Minus Plus minus B out over N2.
[00:45:41:699 - 00:45:44:439] **Speaker 1:** 1 minus DT equals 0.
[00:45:45:659 - 00:45:51:969] **Speaker 0:** To council So VS over N1D equals the out over
[00:45:51:969 - 00:45:54:290] **Speaker 0:** N2 1 minus D.
[00:45:55:770 - 00:45:59:919] **Speaker 0:** Giving us Via of BS.
[00:46:00:810 - 00:46:02:090] **Speaker 0:** Equals into.
[00:46:03:919 - 00:46:06:989] **Speaker 0:** Of M1D over 1 minus D.
[00:46:11:179 - 00:46:13:399] **Speaker 0:** Right, so again, it's just a different way of looking
[00:46:13:399 - 00:46:16:979] **Speaker 0:** at this time with the, I, I guess the more
[00:46:16:979 - 00:46:20:659] **Speaker 0:** accurate approach of looking at the flux and the core
[00:46:20:659 - 00:46:21:939] **Speaker 0:** of the transformer.
[00:46:36:969 - 00:46:39:729] **Speaker 0:** OK, so we've got the same sort of things happening
[00:46:39:729 - 00:46:41:209] **Speaker 0:** here for um our converter.
[00:46:41:250 - 00:46:46:360] **Speaker 0:** We need to consider um what are the minimum values
[00:46:46:360 - 00:46:50:129] **Speaker 0:** that we need in order to maintain continuous current and
[00:46:50:129 - 00:46:53:290] **Speaker 0:** maybe a capacitor size to make sure our voltage ripple
[00:46:53:290 - 00:46:55:389] **Speaker 0:** is below a certain threshold.
[00:47:00:590 - 00:47:03:129] **Speaker 0:** So we want to keep that inductive current continuous.
[00:47:05:120 - 00:47:10:120] **Speaker 0:** So that's the um magnetising inductance.
[00:47:13:120 - 00:47:16:389] **Speaker 0:** So we'd have an average, average.
[00:47:17:820 - 00:47:19:770] **Speaker 0:** Current for the magnetising inductance.
[00:47:19:810 - 00:47:23:489] **Speaker 0:** We're talking about the situation where that just touches on
[00:47:23:489 - 00:47:24:120] **Speaker 0:** zero.
[00:47:32:239 - 00:47:34:620] **Speaker 0:** So that's where this expression comes from.
[00:47:35:199 - 00:47:39:399] **Speaker 0:** magnetising inductance, you don't, if you, if you get a
[00:47:39:399 - 00:47:44:320] **Speaker 0:** transformer, then um you can design to try and get
[00:47:44:320 - 00:47:45:419] **Speaker 0:** that sort of value.
[00:47:46:399 - 00:47:48:610] **Speaker 0:** Alright, or you maybe just have.
[00:47:49:590 - 00:47:53:030] **Speaker 0:** The transformer already given, in which case the only thing
[00:47:53:030 - 00:47:54:510] **Speaker 0:** that you could adjust is the frequency.
[00:47:54:790 - 00:47:57:270] **Speaker 0:** So that's why those two are shown together as being
[00:47:57:270 - 00:47:59:050] **Speaker 0:** a product to give a minimum value.
[00:47:59:620 - 00:48:02:229] **Speaker 0:** So sometimes you can't play around with the inductance, but
[00:48:02:229 - 00:48:05:290] **Speaker 0:** other times you can, but then you could, um, change
[00:48:05:290 - 00:48:09:149] **Speaker 0:** the switching frequency to make sure that this uh current
[00:48:09:149 - 00:48:10:350] **Speaker 0:** stays continuous.
[00:48:12:270 - 00:48:14:989] **Speaker 0:** That's the expression that I've put on learn that I've
[00:48:14:989 - 00:48:17:510] **Speaker 0:** fully derived for you, just to show where it's come
[00:48:17:510 - 00:48:17:850] **Speaker 0:** from.
[00:48:18:479 - 00:48:21:870] **Speaker 0:** It's based on the understanding that the input power is
[00:48:21:870 - 00:48:24:320] **Speaker 0:** effectively the same as the output power if we've got
[00:48:24:320 - 00:48:25:760] **Speaker 0:** an ideal converter.
[00:48:28:879 - 00:48:31:260] **Speaker 0:** And finally, since the output.
[00:48:32:189 - 00:48:35:149] **Speaker 0:** Um, of the converter is identical to what it was
[00:48:35:149 - 00:48:38:229] **Speaker 0:** for the buck boost, then as far as designing for
[00:48:38:229 - 00:48:42:649] **Speaker 0:** a particular capacitance, that gives us a value of voltage
[00:48:42:649 - 00:48:46:189] **Speaker 0:** ripple that we might be designing for, the expression, the
[00:48:46:189 - 00:48:49:030] **Speaker 0:** way that we come to this conclusion and the expression
[00:48:49:030 - 00:48:51:870] **Speaker 0:** is identical to what it was for the buck boost
[00:48:51:870 - 00:48:52:389] **Speaker 0:** converter.
[00:48:53:540 - 00:48:56:139] **Speaker 0:** So I won't um spend time again just going through
[00:48:56:139 - 00:48:56:379] **Speaker 0:** that.
[00:48:56:659 - 00:48:59:020] **Speaker 0:** But this is the same expression as we had for
[00:48:59:020 - 00:48:59:760] **Speaker 0:** the buck boost.
[00:49:02:959 - 00:49:06:479] **Speaker 0:** OK, so that's the first of the converters that are
[00:49:06:479 - 00:49:07:820] **Speaker 0:** isolated that we'll be looking at.
[00:49:07:959 - 00:49:10:280] **Speaker 0:** Tomorrow, we're going to jump in and have a look
[00:49:10:280 - 00:49:14:479] **Speaker 0:** at another one, which utilises the transformer much more in
[00:49:14:479 - 00:49:16:679] **Speaker 0:** the way that we usually do and that it's not
[00:49:16:679 - 00:49:19:219] **Speaker 0:** designed to store very much energy at all.

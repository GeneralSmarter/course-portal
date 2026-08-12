# ENEL372-26S2 Lecture 12 native Echo transcript

Date: August 7, 2026 9:00am-9:55am
Transcript type: native Echo automated transcript.

[00:00:01:899 - 00:00:04:679] **Speaker 0:** All right, Kyorakoto, we'll get going.
[00:00:07:110 - 00:00:09:500] **Speaker 1:** Thank you for those, uh, that have braved the uh
[00:00:09:500 - 00:00:11:930] **Speaker 1:** the rather cool conditions for this morning to show up
[00:00:12:069 - 00:00:13:180] **Speaker 1:** face to face for the lecture.
[00:00:13:550 - 00:00:14:140] **Speaker 1:** Much appreciated.
[00:00:14:189 - 00:00:15:909] **Speaker 1:** This is the, this is the hardy bunch of the
[00:00:15:909 - 00:00:16:450] **Speaker 1:** class, right?
[00:00:17:899 - 00:00:21:860] **Speaker 1:** OK, so we're looking at a, a second type of
[00:00:21:860 - 00:00:26:940] **Speaker 1:** isolated um DC to DC converter today, um, it's called
[00:00:26:940 - 00:00:29:180] **Speaker 1:** the forward converter, um.
[00:00:30:069 - 00:00:32:189] **Speaker 1:** It is a convertible.
[00:00:32:349 - 00:00:34:349] **Speaker 1:** The reason we're looking at it is that for for
[00:00:34:349 - 00:00:35:189] **Speaker 1:** a couple of reasons.
[00:00:35:509 - 00:00:39:389] **Speaker 1:** Um, 1st, 1st off, it utilises the isolation transformer in
[00:00:39:389 - 00:00:42:310] **Speaker 1:** a more conventional way than the flyback.
[00:00:42:549 - 00:00:46:310] **Speaker 1:** This is, this doesn't, uh, store much energy in the
[00:00:46:310 - 00:00:47:470] **Speaker 1:** core of the transformer.
[00:00:47:509 - 00:00:50:610] **Speaker 1:** The idea is that it transfers energy straight through the
[00:00:50:610 - 00:00:54:250] **Speaker 1:** isolation transformer to the output, uh, primarily.
[00:00:54:830 - 00:00:58:520] **Speaker 1:** The other thing is that whilst this particular type of
[00:00:58:520 - 00:01:03:759] **Speaker 1:** what we call a single switch forward converter doesn't find
[00:01:03:759 - 00:01:07:250] **Speaker 1:** itself used in a lot of applications, it's used in
[00:01:07:250 - 00:01:10:000] **Speaker 1:** some, but it's not particularly common, um, not as common
[00:01:10:000 - 00:01:15:120] **Speaker 1:** as the flyback, uh, but it is a, a gateway
[00:01:15:120 - 00:01:19:879] **Speaker 1:** understanding converter which, um, The type of output that's utilised,
[00:01:19:980 - 00:01:22:139] **Speaker 1:** uh, which, where it gets its name from the forward
[00:01:22:139 - 00:01:25:540] **Speaker 1:** converter, is utilised in a number of other what we
[00:01:25:540 - 00:01:31:199] **Speaker 1:** call multi-switch, uh, converters, uh, that are used very commonly,
[00:01:31:540 - 00:01:31:620] **Speaker 1:** right?
[00:01:31:739 - 00:01:34:699] **Speaker 1:** So it's a, it, it uses the transformer more common
[00:01:34:699 - 00:01:37:620] **Speaker 1:** sense, uh, a common or conventional sense, which is why
[00:01:37:620 - 00:01:41:400] **Speaker 1:** we're looking at it, but also Understanding its operation helps
[00:01:41:400 - 00:01:43:959] **Speaker 1:** you then move on to understanding the operation of these
[00:01:43:959 - 00:01:45:480] **Speaker 1:** other converters that are more common.
[00:01:45:800 - 00:01:49:309] **Speaker 1:** These are things like push pull converters and bridge board
[00:01:49:309 - 00:01:49:839] **Speaker 1:** converters.
[00:01:50:000 - 00:01:52:480] **Speaker 1:** Um, if you do power electronics next year, you'll get
[00:01:52:480 - 00:01:53:620] **Speaker 1:** to learn about those.
[00:01:55:760 - 00:02:01:830] **Speaker 1:** OK, um So the forward converter shown here, as are
[00:02:01:830 - 00:02:06:150] **Speaker 1:** other forward converters, um, is partially derived from the non-isolated
[00:02:06:150 - 00:02:07:250] **Speaker 1:** buck converter.
[00:02:07:750 - 00:02:10:490] **Speaker 1:** We know quite a bit about buck converters now, um,
[00:02:10:910 - 00:02:13:380] **Speaker 1:** so a lot of the analysis that we go through
[00:02:13:380 - 00:02:15:050] **Speaker 1:** is very similar.
[00:02:15:550 - 00:02:18:350] **Speaker 1:** So we don't have to stretch, uh, our understanding too
[00:02:18:350 - 00:02:21:270] **Speaker 1:** far when we think just about the power transfer from
[00:02:21:270 - 00:02:24:589] **Speaker 1:** the the the source DC the DC source at the
[00:02:24:589 - 00:02:26:910] **Speaker 1:** input to the DC at the output.
[00:02:28:729 - 00:02:34:630] **Speaker 1:** Um Unlike the back converter though, we don't have the
[00:02:34:630 - 00:02:37:229] **Speaker 1:** option, we don't have the restriction of having an output
[00:02:37:229 - 00:02:40:250] **Speaker 1:** voltage that is always less than the input voltage.
[00:02:41:119 - 00:02:45:679] **Speaker 1:** Uh Because of the turns ratio that we can employ
[00:02:45:679 - 00:02:49:850] **Speaker 1:** with the um transformer, we can also uh utilise a
[00:02:49:850 - 00:02:51:059] **Speaker 1:** step up function.
[00:02:54:419 - 00:02:57:970] **Speaker 1:** Um, whilst I see that a lot of the analysis
[00:02:57:970 - 00:03:00:410] **Speaker 1:** is going to kind of be based on the the
[00:03:00:410 - 00:03:02:889] **Speaker 1:** back converter that we've already looked at, um, there is
[00:03:02:889 - 00:03:07:410] **Speaker 1:** a bit to this, the, the transformer that, um, does
[00:03:07:410 - 00:03:11:690] **Speaker 1:** complicate matters a bit, um, and we can see that
[00:03:11:690 - 00:03:15:570] **Speaker 1:** this transformer, uh, ignoring the magnetising conductance model there at
[00:03:15:570 - 00:03:19:089] **Speaker 1:** the moment, this transformer has 3 windings.
[00:03:19:880 - 00:03:23:960] **Speaker 1:** Right, so, we have the normal two windings for input
[00:03:23:960 - 00:03:28:869] **Speaker 1:** to output for power transfer from input to output, um,
[00:03:28:880 - 00:03:29:720] **Speaker 1:** and we'll go over that.
[00:03:30:000 - 00:03:34:639] **Speaker 1:** But then there's this third winding which is necessary in
[00:03:34:639 - 00:03:39:520] **Speaker 1:** this configuration to make sure the core of the transformer
[00:03:39:520 - 00:03:42:360] **Speaker 1:** is demagnetized cycle by cycle.
[00:03:43:630 - 00:03:46:990] **Speaker 1:** Right, if it's not demagnetized, then you'll get a net
[00:03:47:309 - 00:03:50:550] **Speaker 1:** flux that's in the core cycle on cycle and it
[00:03:50:550 - 00:03:53:190] **Speaker 1:** will just grow and grow and grow till eventually the
[00:03:53:190 - 00:03:54:029] **Speaker 1:** core saturates.
[00:03:54:860 - 00:03:57:309] **Speaker 1:** Alright, so we'll go through that and and and gain
[00:03:57:309 - 00:04:00:949] **Speaker 1:** an understanding of how that uh that extra winding will
[00:04:00:949 - 00:04:05:320] **Speaker 1:** make sure that the core has been completely demagnetized, uh,
[00:04:05:460 - 00:04:06:229] **Speaker 1:** cycle on cycle.
[00:04:08:940 - 00:04:12:839] **Speaker 1:** Um, I also want you to take note of um
[00:04:13:259 - 00:04:17:519] **Speaker 1:** the dot convention that we have applied for this converter.
[00:04:17:980 - 00:04:21:980] **Speaker 1:** Alright, so if we have plus minus occurring across this
[00:04:21:980 - 00:04:25:600] **Speaker 1:** winding primary winding one, then we will see plus minus
[00:04:25:940 - 00:04:27:880] **Speaker 1:** and plus minus on those other windings.
[00:04:28:339 - 00:04:33:660] **Speaker 1:** Also, conversely, if we um see uh plus minus say
[00:04:33:660 - 00:04:35:899] **Speaker 1:** on this winding then that would be plus minus plus
[00:04:35:899 - 00:04:36:480] **Speaker 1:** minus.
[00:04:37:109 - 00:04:41:470] **Speaker 1:** Right, so the dot convention tells you the phasing information
[00:04:41:470 - 00:04:44:390] **Speaker 1:** between all of the windings attached to the same core.
[00:04:54:000 - 00:04:59:420] **Speaker 1:** OK We're going to analyse this converter, uh, and we
[00:04:59:420 - 00:05:01:739] **Speaker 1:** do it in the same approach that we have always
[00:05:01:739 - 00:05:03:779] **Speaker 1:** made so far as we're going to look at what
[00:05:03:779 - 00:05:07:190] **Speaker 1:** happens when the controllable switch is closed and when it's
[00:05:07:190 - 00:05:07:760] **Speaker 1:** open.
[00:05:18:470 - 00:05:21:000] **Speaker 1:** OK, so, first up, switch clothes.
[00:05:23:000 - 00:05:26:359] **Speaker 1:** So while I said that uh we have the the
[00:05:26:359 - 00:05:28:989] **Speaker 1:** transformer being used in the more conventional sense, we're not
[00:05:28:989 - 00:05:31:880] **Speaker 1:** expecting much energy to be stored in that core cycle
[00:05:31:880 - 00:05:35:079] **Speaker 1:** by cycle, there is still some, there is still some,
[00:05:35:239 - 00:05:39:559] **Speaker 1:** so we continue with modelling the, the flux within the
[00:05:39:559 - 00:05:44:119] **Speaker 1:** core with our magnetising inductance on the primary winding.
[00:05:44:480 - 00:05:45:959] **Speaker 1:** So we're going to have this LM.
[00:05:48:500 - 00:05:56:559] **Speaker 1:** Um So we'll we'll look at that energy store um
[00:05:56:559 - 00:05:59:040] **Speaker 1:** and see that we have to zero that cycle on
[00:05:59:040 - 00:06:01:720] **Speaker 1:** cycle so that we don't end up with that flux
[00:06:02:070 - 00:06:04:279] **Speaker 1:** adding and walking away to saturation.
[00:06:05:989 - 00:06:07:730] **Speaker 1:** Right, so closing the switch.
[00:06:08:970 - 00:06:11:130] **Speaker 1:** On the primary side as it's got here, so this
[00:06:11:130 - 00:06:12:750] **Speaker 1:** is where the switch would be located.
[00:06:14:190 - 00:06:18:730] **Speaker 1:** It's been closed Um, so we have, I don't think
[00:06:18:730 - 00:06:21:250] **Speaker 1:** it, it's a big stretch, we see that if we've
[00:06:21:250 - 00:06:23:730] **Speaker 1:** got a voltage source of BS, we close that switch,
[00:06:23:929 - 00:06:27:290] **Speaker 1:** we have BS plus minus on the primary winding.
[00:06:31:670 - 00:06:36:910] **Speaker 1:** So that would mean that we have that's as shown
[00:06:36:910 - 00:06:40:730] **Speaker 1:** plus minus with BS then we would have plus minus
[00:06:41:029 - 00:06:47:540] **Speaker 1:** and Plus minus on those windings, with the positive, being
[00:06:47:540 - 00:06:53:420] **Speaker 1:** here and um the diode being connected, This way around
[00:06:54:290 - 00:06:56:559] **Speaker 1:** in the circuit, then we've got the positive side on
[00:06:56:559 - 00:06:59:320] **Speaker 1:** the cathode which reverse biases that died, which is why
[00:06:59:320 - 00:07:00:959] **Speaker 1:** it's showing us an open circuit.
[00:07:01:480 - 00:07:04:279] **Speaker 1:** There's no conduction, no current flowing through there.
[00:07:05:109 - 00:07:08:709] **Speaker 1:** Here on the on the back converter output side, it's
[00:07:08:709 - 00:07:10:309] **Speaker 1:** just like we have for the back converter here was
[00:07:10:309 - 00:07:12:679] **Speaker 1:** that diode um the.
[00:07:14:190 - 00:07:16:049] **Speaker 1:** 21.
[00:07:17:720 - 00:07:20:959] **Speaker 1:** It's forward bias, so it's conducting, and of course we
[00:07:20:959 - 00:07:22:779] **Speaker 1:** had the other diode sitting in here.
[00:07:23:970 - 00:07:25:429] **Speaker 1:** Our freewheeling diode.
[00:07:26:459 - 00:07:29:510] **Speaker 1:** That way around, so it's reverse biassed and open circuited.
[00:07:31:589 - 00:07:35:619] **Speaker 1:** Completely conventional way of looking at the output as we
[00:07:35:619 - 00:07:36:660] **Speaker 1:** do for a buck converter.
[00:07:40:059 - 00:07:43:160] **Speaker 1:** OK, so if we have that switch closed, we've got
[00:07:43:160 - 00:07:47:329] **Speaker 1:** a, a couple of situations occurring, so um we've got
[00:07:47:329 - 00:07:49:899] **Speaker 1:** plus minus VS across the magnetising inductance.
[00:07:51:269 - 00:07:54:679] **Speaker 1:** Alright, so this is the magnetising induction, so it's going
[00:07:54:679 - 00:07:58:820] **Speaker 1:** to, it's current, the magnetising current ILM will ramp up
[00:07:58:880 - 00:08:02:869] **Speaker 1:** at a rate of VS um over LM times DT,
[00:08:02:959 - 00:08:04:140] **Speaker 1:** the amount of time that it's on.
[00:08:05:239 - 00:08:06:660] **Speaker 1:** Yeah, so that's ramping up current.
[00:08:08:350 - 00:08:12:299] **Speaker 1:** For LX, that's our power inductor for our buck converter,
[00:08:12:350 - 00:08:12:730] **Speaker 1:** right?
[00:08:13:459 - 00:08:15:850] **Speaker 1:** So that's the output for the forward converter.
[00:08:17:179 - 00:08:19:660] **Speaker 1:** We need to know what is the voltage drop across
[00:08:19:660 - 00:08:21:380] **Speaker 1:** LX for when the switch is closed.
[00:08:21:500 - 00:08:24:579] **Speaker 1:** Well, voltage on that side, we're looking at the turns
[00:08:24:579 - 00:08:28:980] **Speaker 1:** ratio of the transformer is N2 over N1 times the
[00:08:28:980 - 00:08:29:640] **Speaker 1:** voltage.
[00:08:30:399 - 00:08:33:729] **Speaker 1:** That's on that primary winning, so N1 over 10, N2
[00:08:33:729 - 00:08:34:390] **Speaker 1:** times BS.
[00:08:37:109 - 00:08:38:630] **Speaker 1:** Alright, so that's that voltage on that side.
[00:08:38:710 - 00:08:41:840] **Speaker 1:** The other voltage, of course, just as we normally have
[00:08:41:840 - 00:08:43:869] **Speaker 1:** for the back converter, it's the out.
[00:08:44:469 - 00:08:45:190] **Speaker 1:** So we see.
[00:08:45:989 - 00:08:48:030] **Speaker 1:** BS times N2 over in 1 minus B out.
[00:08:49:280 - 00:08:52:799] **Speaker 1:** DT over LX, so exactly the same as the back
[00:08:52:799 - 00:08:56:919] **Speaker 1:** converter expression, just scaled the uh the voltage by N2
[00:08:56:919 - 00:08:57:630] **Speaker 1:** over N1.
[00:09:02:179 - 00:09:04:659] **Speaker 1:** Right, so that's ramping up current.
[00:09:08:349 - 00:09:11:419] **Speaker 1:** When that switch is closed, it has to deal with
[00:09:11:419 - 00:09:17:630] **Speaker 1:** both the ILM and the Effective current that's feeding into
[00:09:17:630 - 00:09:21:669] **Speaker 1:** the primary, so it would be uh IS which would
[00:09:21:669 - 00:09:25:510] **Speaker 1:** be your switch current is equal to ILM.
[00:09:26:760 - 00:09:28:880] **Speaker 1:** Plus, I won.
[00:09:39:539 - 00:09:41:630] **Speaker 1:** Any questions so far about this the operation with the
[00:09:41:630 - 00:09:42:390] **Speaker 1:** switch closed?
[00:09:44:119 - 00:09:46:229] **Speaker 1:** So this 3rd winding doesn't seem to be doing anything
[00:09:46:229 - 00:09:47:119] **Speaker 1:** at at present.
[00:09:47:200 - 00:09:48:599] **Speaker 1:** There's no current flowing through there.
[00:09:50:020 - 00:09:53:359] **Speaker 1:** And all we've got is the normal situation of transferring
[00:09:53:359 - 00:09:56:460] **Speaker 1:** energy to the output with the switch closed, uh, so
[00:09:56:460 - 00:09:59:700] **Speaker 1:** the current is ramping up, we're energising our power conductor,
[00:10:00:049 - 00:10:03:020] **Speaker 1:** uh, but we're also energising the core of the transformer.
[00:10:07:010 - 00:10:08:929] **Speaker 1:** Throw my pin down, right, uh.
[00:10:10:229 - 00:10:13:270] **Speaker 1:** Now, that amount of energy that we're storing is not
[00:10:13:270 - 00:10:15:549] **Speaker 1:** very much, uh, LM.
[00:10:16:719 - 00:10:18:580] **Speaker 1:** is actually quite large.
[00:10:25:520 - 00:10:27:400] **Speaker 1:** So, ILM.
[00:10:29:219 - 00:10:31:080] **Speaker 1:** We see, have a look at this, it's quite small.
[00:10:37:020 - 00:10:39:700] **Speaker 1:** And the amount of energy that we store uh in
[00:10:39:700 - 00:10:42:140] **Speaker 1:** an inductance and therefore in the core of this transformer
[00:10:42:140 - 00:10:44:979] **Speaker 1:** is proportional to the square of the current.
[00:10:45:820 - 00:10:48:809] **Speaker 1:** OK, so even though LM is getting bigger, sure, then,
[00:10:49:219 - 00:10:51:880] **Speaker 1:** then um it is for the flyback converters as such.
[00:10:52:650 - 00:10:55:210] **Speaker 1:** The the fact that it is larger means that the
[00:10:55:210 - 00:10:56:369] **Speaker 1:** current reduces.
[00:10:57:539 - 00:11:00:890] **Speaker 1:** But the energy is with a square of that current,
[00:11:01:210 - 00:11:03:090] **Speaker 1:** OK, so as that current goes down, the amount of
[00:11:03:090 - 00:11:05:729] **Speaker 1:** energy being stored is, is reducing even though the inductance
[00:11:05:729 - 00:11:06:770] **Speaker 1:** value is increasing.
[00:11:09:409 - 00:11:09:770] **Speaker 1:** Right.
[00:11:10:520 - 00:11:18:690] **Speaker 1:** Um OK So, because LM is so big, we're not
[00:11:18:690 - 00:11:20:429] **Speaker 1:** storing much energy in that core.
[00:11:21:130 - 00:11:21:809] **Speaker 1:** Why does it get big?
[00:11:21:969 - 00:11:25:140] **Speaker 1:** It's because, uh, there are with those transformer cores we,
[00:11:25:229 - 00:11:26:369] **Speaker 1:** we don't have an air gap.
[00:11:26:570 - 00:11:29:770] **Speaker 1:** The permeability of the magnetic circuit is actually very, very
[00:11:29:770 - 00:11:33:830] **Speaker 1:** large, so it doesn't take many turns of our, um,
[00:11:33:840 - 00:11:36:010] **Speaker 1:** of our windings to end up with quite a large
[00:11:36:010 - 00:11:37:969] **Speaker 1:** value of inductance being created.
[00:11:48:469 - 00:11:49:630] **Speaker 1:** Alright, switch open.
[00:11:58:979 - 00:11:59:640] **Speaker 1:** She fuck later.
[00:12:01:109 - 00:12:06:169] **Speaker 1:** Switch open, right, um, so when we open that switch.
[00:12:07:250 - 00:12:10:729] **Speaker 1:** We've had, we've got to take account of that magnetising
[00:12:10:729 - 00:12:11:590] **Speaker 1:** inductance.
[00:12:12:130 - 00:12:14:530] **Speaker 1:** Alright, we open the switch, that current falls to zero,
[00:12:15:000 - 00:12:18:690] **Speaker 1:** but we've got ILM that uh has been flowing in
[00:12:18:690 - 00:12:20:190] **Speaker 1:** that magnetising inductance.
[00:12:21:979 - 00:12:26:859] **Speaker 1:** What's going to happen is The energy starts collapsing or
[00:12:26:859 - 00:12:30:840] **Speaker 1:** the magnetic flux collapses in the core and as such
[00:12:30:969 - 00:12:36:619] **Speaker 1:** um The voltage flips across that magnetising inductance.
[00:12:36:919 - 00:12:38:260] **Speaker 1:** Remember it's a modelled inductance.
[00:12:39:219 - 00:12:41:590] **Speaker 1:** Um, and that current keeps flowing, so we're going to
[00:12:41:590 - 00:12:44:210] **Speaker 1:** end up with plus minus across M1.
[00:12:46:190 - 00:12:51:539] **Speaker 1:** We're going to end up with plus minus 3 and
[00:12:51:539 - 00:12:53:190] **Speaker 1:** plus minus for N2.
[00:12:57:840 - 00:13:02:239] **Speaker 1:** Well, looking at the, the, the main um converted element
[00:13:02:239 - 00:13:04:400] **Speaker 1:** of the of the power transfer, then if that's plus
[00:13:04:400 - 00:13:08:400] **Speaker 1:** minus, then that reverse bias is our diode D1.
[00:13:09:690 - 00:13:14:219] **Speaker 1:** And our diode D24 vices, so that's what the the
[00:13:14:219 - 00:13:15:219] **Speaker 1:** diode in here.
[00:13:16:909 - 00:13:19:380] **Speaker 1:** It's the normal operation of when the switch is off
[00:13:19:380 - 00:13:20:250] **Speaker 1:** for a butt converter.
[00:13:21:380 - 00:13:24:080] **Speaker 1:** Alright, the free wheeling diode takes over, of course this,
[00:13:24:090 - 00:13:27:380] **Speaker 1:** this boltage across the inductor changes plus minus and is
[00:13:27:380 - 00:13:28:440] **Speaker 1:** now equal to be out.
[00:13:37:679 - 00:13:40:840] **Speaker 1:** Alright, so we've got all of the um winding voltages
[00:13:40:840 - 00:13:41:539] **Speaker 1:** reverses.
[00:13:42:520 - 00:13:44:710] **Speaker 1:** D one now is forward biassed.
[00:13:46:820 - 00:13:49:320] **Speaker 1:** Alright, so we've got current flow is D1.
[00:13:52:950 - 00:13:55:239] **Speaker 1:** Alright, we've got current flow uh possible through D1.
[00:13:56:869 - 00:13:57:580] **Speaker 1:** Why is it possible?
[00:13:57:710 - 00:13:59:409] **Speaker 1:** Because this is now an energy source.
[00:14:00:450 - 00:14:01:739] **Speaker 1:** Alright, so current flows.
[00:14:02:770 - 00:14:06:280] **Speaker 1:** This way, as as shown by the arrow, blows this
[00:14:06:280 - 00:14:08:380] **Speaker 1:** way out of the the terminal.
[00:14:10:200 - 00:14:10:390] **Speaker 1:** Right.
[00:14:11:469 - 00:14:12:469] **Speaker 1:** Forming a closed loop.
[00:14:13:440 - 00:14:15:719] **Speaker 1:** So if that's the case and this is, this is,
[00:14:15:750 - 00:14:18:599] **Speaker 1:** uh, forward bias and we've got that side connected to
[00:14:18:599 - 00:14:21:559] **Speaker 1:** the negative of the supply, we go through this winding
[00:14:21:559 - 00:14:25:359] **Speaker 1:** here, it's conducting, it's connected to that side, so the
[00:14:25:359 - 00:14:28:539] **Speaker 1:** voltage drop across N3.
[00:14:29:219 - 00:14:31:719] **Speaker 1:** With that dog now conducting is BS.
[00:14:36:890 - 00:14:39:690] **Speaker 1:** With that that way around, plus minus DS.
[00:14:41:400 - 00:14:42:479] **Speaker 1:** Can you see, can you see that?
[00:14:42:640 - 00:14:43:859] **Speaker 1:** That, that makes sense?
[00:14:47:960 - 00:14:52:000] **Speaker 1:** OK, well, if that's the case, um, ignoring what's happening
[00:14:52:000 - 00:14:54:039] **Speaker 1:** on the secondary there's no current flow there, we're not
[00:14:54:039 - 00:14:55:640] **Speaker 1:** particularly interested in what's happening here.
[00:14:55:919 - 00:14:58:599] **Speaker 1:** We are interested in what's happening here though.
[00:14:58:840 - 00:15:01:760] **Speaker 1:** We want to know what is the effect of voltage
[00:15:01:760 - 00:15:04:500] **Speaker 1:** across, um, that primary winding.
[00:15:04:919 - 00:15:09:580] **Speaker 1:** Well, we've got a turns ratio for our transformer.
[00:15:10:349 - 00:15:15:710] **Speaker 1:** Here So we've got N1 and N3, so the voltage
[00:15:15:710 - 00:15:17:630] **Speaker 1:** here must be N1.
[00:15:18:750 - 00:15:21:690] **Speaker 1:** Over N3 times BS.
[00:15:32:299 - 00:15:35:219] **Speaker 1:** Now that we have that understanding, we can determine what
[00:15:35:219 - 00:15:40:619] **Speaker 1:** is the ramping function associated with LM de-energizing.
[00:15:42:000 - 00:15:43:859] **Speaker 1:** So we got um Delta.
[00:15:45:679 - 00:15:48:659] **Speaker 1:** ILM When the switch is open.
[00:15:51:960 - 00:15:54:559] **Speaker 1:** is equal to, so it's collapsing, this will be a
[00:15:54:559 - 00:15:58:140] **Speaker 1:** negatively sloped um ramp minus.
[00:16:01:630 - 00:16:05:590] **Speaker 1:** BS times N1 over N3.
[00:16:08:260 - 00:16:15:669] **Speaker 1:** That's the voltage Over LM Time Tx, so that's the
[00:16:15:669 - 00:16:19:380] **Speaker 1:** amount of time it takes to ramp down to zero.
[00:16:20:059 - 00:16:24:750] **Speaker 1:** Right, so we're gonna completely de-energize the the flux in
[00:16:24:750 - 00:16:25:309] **Speaker 1:** the core.
[00:16:26:630 - 00:16:28:869] **Speaker 1:** So we just call that TX at the moment, but
[00:16:28:869 - 00:16:29:669] **Speaker 1:** we know.
[00:16:30:479 - 00:16:34:080] **Speaker 1:** Oh sorry, Delta TX, the change in time or the
[00:16:34:080 - 00:16:41:440] **Speaker 1:** amount of time, um, where Delta TX, this has to
[00:16:41:440 - 00:16:44:210] **Speaker 1:** happen while the switch is in its off state.
[00:16:44:830 - 00:16:45:729] **Speaker 1:** When it's open.
[00:16:46:489 - 00:16:50:390] **Speaker 1:** So we know already that that amount of time is
[00:16:50:400 - 00:16:52:869] **Speaker 1:** 1 minus D times the period.
[00:16:53:239 - 00:16:54:969] **Speaker 1:** That's the amount of time the switch is open given
[00:16:54:969 - 00:16:56:489] **Speaker 1:** a particular duty ratio.
[00:17:04:560 - 00:17:06:959] **Speaker 1:** Um, I won't spend too much time here.
[00:17:07:000 - 00:17:10:280] **Speaker 1:** This is just looking at the ramping down current through
[00:17:10:280 - 00:17:12:930] **Speaker 1:** our magnetise our output power conductor.
[00:17:13:239 - 00:17:17:119] **Speaker 1:** This is exactly the same expression we have for a
[00:17:17:119 - 00:17:21:079] **Speaker 1:** buck converter when our switch is open.
[00:17:22:369 - 00:17:27:468] **Speaker 1:** Right OK.
[00:17:35:089 - 00:17:35:810] **Speaker 1:** Still following?
[00:17:36:060 - 00:17:36:699] **Speaker 1:** Still going alright?
[00:17:37:969 - 00:17:38:650] **Speaker 1:** Questions?
[00:17:41:739 - 00:17:45:439] **Speaker 1:** OK, Right, we'll we'll get to some waveforms that'll help
[00:17:45:819 - 00:17:47:010] **Speaker 1:** explain things a bit as well.
[00:17:51:609 - 00:17:55:089] **Speaker 1:** Right now, uh, first up we, uh, we're looking at
[00:17:55:089 - 00:17:58:310] **Speaker 1:** the, the, the power flow through the, through the converter
[00:17:58:569 - 00:18:01:729] **Speaker 1:** and we still have the this, um, situation, the average
[00:18:01:729 - 00:18:04:689] **Speaker 1:** fluctuation inductor current, oh by the way, what inductor are
[00:18:04:689 - 00:18:05:560] **Speaker 1:** we talking about here?
[00:18:05:880 - 00:18:06:969] **Speaker 1:** This is LX.
[00:18:09:550 - 00:18:11:250] **Speaker 1:** Um, must equal 0.
[00:18:12:469 - 00:18:15:550] **Speaker 1:** Then it turns out just as we have for our
[00:18:15:550 - 00:18:19:270] **Speaker 1:** normal buck converter, the output voltage is equal to the
[00:18:19:270 - 00:18:21:050] **Speaker 1:** input voltage times the duty ratio.
[00:18:21:829 - 00:18:27:359] **Speaker 1:** But of course the voltage that the secondary side, so
[00:18:27:359 - 00:18:31:000] **Speaker 1:** what the buck converter input sees is the scaled DC
[00:18:31:000 - 00:18:35:800] **Speaker 1:** voltage through the transformer, alright, so that's N2 over N1.
[00:18:44:569 - 00:18:47:579] **Speaker 1:** So here's the, here's the LX, so this is our
[00:18:47:579 - 00:18:49:930] **Speaker 1:** power inductor whilst the switch is on, it's ramping up,
[00:18:49:969 - 00:18:50:910] **Speaker 1:** it's getting energised.
[00:18:51:209 - 00:18:55:969] **Speaker 1:** When the switch is off, it's uh de-energizing, maintaining the
[00:18:55:969 - 00:18:58:030] **Speaker 1:** output voltage um on the load.
[00:19:00:469 - 00:19:03:689] **Speaker 1:** I want, this is the primary current that we see
[00:19:03:689 - 00:19:06:760] **Speaker 1:** in the um In the transformer.
[00:19:07:839 - 00:19:11:229] **Speaker 1:** Uh, here it is, we've got it, uh, being positive
[00:19:11:959 - 00:19:15:589] **Speaker 1:** for when the switch is on, and then It becomes
[00:19:15:589 - 00:19:19:469] **Speaker 1:** negative and this is the reversed ILM.
[00:19:28:630 - 00:19:33:869] **Speaker 1:** Alright, so This is when we got the switch off
[00:19:33:869 - 00:19:37:910] **Speaker 1:** and ILM is going this way through the primary winding
[00:19:37:910 - 00:19:38:869] **Speaker 1:** as as modelled.
[00:19:40:140 - 00:19:42:699] **Speaker 1:** OK, so that's why it's negative and it peaks at
[00:19:42:699 - 00:19:43:780] **Speaker 1:** the value of ILM.
[00:19:48:780 - 00:19:52:359] **Speaker 1:** Uh, and we can see here that that reduces down
[00:19:52:359 - 00:19:53:949] **Speaker 1:** to zero in time delta TX.
[00:19:54:030 - 00:19:54:890] **Speaker 1:** So here's ILM.
[00:19:55:180 - 00:19:56:989] **Speaker 1:** It's ramping up when we got the switch closed, and
[00:19:56:989 - 00:19:58:930] **Speaker 1:** then it ramps down when the switch is open.
[00:19:59:890 - 00:20:01:689] **Speaker 1:** Uh, over a time, Delta TX.
[00:20:06:689 - 00:20:10:209] **Speaker 1:** I2, this is the pri the secondary current, OK, so
[00:20:10:209 - 00:20:13:209] **Speaker 1:** it's ramping up with the switch closed and then as
[00:20:13:209 - 00:20:16:290] **Speaker 1:** soon as you open the switch, the current stops in
[00:20:16:290 - 00:20:20:729] **Speaker 1:** the secondary winding dio D1 is reversed by some open
[00:20:20:729 - 00:20:22:670] **Speaker 1:** circuits and your freewheeling diode D2.
[00:20:23:699 - 00:20:28:260] **Speaker 1:** Uh, conducts, uh, where the power conductor is transferring its
[00:20:28:260 - 00:20:28:819] **Speaker 1:** energy to the load.
[00:20:32:839 - 00:20:37:030] **Speaker 1:** Um, I3, which is the um current through the um
[00:20:37:239 - 00:20:39:030] **Speaker 1:** the third winding diode.
[00:20:39:849 - 00:20:44:280] **Speaker 1:** OK, it isn't conducting because it's reverse bias when we
[00:20:44:280 - 00:20:44:969] **Speaker 1:** have the switch closed.
[00:20:45:160 - 00:20:47:290] **Speaker 1:** As soon as we open the switch, it's carrying that
[00:20:47:290 - 00:20:49:510] **Speaker 1:** magnetising current, so it peaks.
[00:20:50:589 - 00:20:53:939] **Speaker 1:** Well, what As it shows, it seems to peak at
[00:20:53:939 - 00:20:54:579] **Speaker 1:** ILM.
[00:20:56:189 - 00:20:59:270] **Speaker 1:** And it would peak at ILM if the turns ratio
[00:20:59:270 - 00:20:59:910] **Speaker 1:** was the same.
[00:21:00:750 - 00:21:04:939] **Speaker 1:** So this curve is being shown for if N3 equals
[00:21:04:939 - 00:21:05:569] **Speaker 1:** N1.
[00:21:09:609 - 00:21:11:369] **Speaker 1:** To give it that same magnitude.
[00:21:13:270 - 00:21:15:060] **Speaker 1:** It's here, it's our ILM.
[00:21:15:750 - 00:21:16:140] **Speaker 1:** Oops sorry.
[00:21:16:849 - 00:21:18:680] **Speaker 1:** It's kind of hard to keep this still when we've
[00:21:18:680 - 00:21:20:699] **Speaker 1:** got these big curly edges on this thing.
[00:21:24:650 - 00:21:27:770] **Speaker 1:** And VX, that's just the input voltage to our back
[00:21:27:770 - 00:21:29:890] **Speaker 1:** converter side, so.
[00:21:32:520 - 00:21:37:280] **Speaker 1:** There's VX Which is just that PWM DC that we
[00:21:37:280 - 00:21:39:239] **Speaker 1:** would normally have for a for a buck converter.
[00:21:41:189 - 00:21:45:800] **Speaker 1:** Again, Just scaling the input source DC voltage by the
[00:21:45:800 - 00:21:47:099] **Speaker 1:** turns ratio of the transformer.
[00:21:52:489 - 00:21:57:260] **Speaker 1:** Right, so behaviour very much like a butt converter except
[00:21:57:260 - 00:22:00:489] **Speaker 1:** for that third winding which is there solely for the
[00:22:00:489 - 00:22:05:469] **Speaker 1:** purpose of making sure that that magnetised conductance, um, from
[00:22:05:479 - 00:22:09:729] **Speaker 1:** the core uh is zeroed for the flux every cycle.
[00:22:11:790 - 00:22:13:510] **Speaker 1:** We will be coming back to this though, because there
[00:22:13:510 - 00:22:16:310] **Speaker 1:** are some issues that we've got to really work through
[00:22:16:310 - 00:22:18:630] **Speaker 1:** if we want to actually design this converter and have
[00:22:18:630 - 00:22:20:550] **Speaker 1:** it function the way that we want it to.
[00:22:28:030 - 00:22:29:310] **Speaker 1:** So, what is that design?
[00:22:29:390 - 00:22:32:930] **Speaker 1:** Well, we want to keep that power inductor current continuous
[00:22:33:510 - 00:22:35:989] **Speaker 1:** for all the reasons that we normally uh expect for
[00:22:35:989 - 00:22:36:890] **Speaker 1:** our back converter.
[00:22:40:329 - 00:22:43:349] **Speaker 1:** Um, so it's minimum current must not drop to zero.
[00:22:49:760 - 00:22:51:810] **Speaker 1:** So if you've got an application where you've got a
[00:22:51:810 - 00:22:55:209] **Speaker 1:** particular duty ratio uh that you're working with some load
[00:22:55:209 - 00:22:56:910] **Speaker 1:** resistance that is defined.
[00:22:57:650 - 00:23:00:410] **Speaker 1:** Uh, we can show that just as we have done
[00:23:00:410 - 00:23:03:319] **Speaker 1:** for our back converter analysis right when the current, uh,
[00:23:03:560 - 00:23:06:260] **Speaker 1:** just touches on zero, we end up with this expression.
[00:23:07:520 - 00:23:10:900] **Speaker 1:** Um, and we've seen that this is also equal to
[00:23:11:140 - 00:23:13:619] **Speaker 1:** the out 1 minus D.
[00:23:14:469 - 00:23:17:410] **Speaker 1:** Over to I out are given.
[00:23:19:380 - 00:23:23:500] **Speaker 1:** By Ohm's law, R is equal to the over I
[00:23:23:500 - 00:23:23:770] **Speaker 1:** out.
[00:23:26:650 - 00:23:28:619] **Speaker 1:** So that's just substituting that in for ah.
[00:23:32:069 - 00:23:33:290] **Speaker 1:** That's all well and good.
[00:23:33:750 - 00:23:37:969] **Speaker 1:** We've been through that exercise before, but there's also another
[00:23:38:439 - 00:23:43:510] **Speaker 1:** uh requirement, and that's for the magnetising inductance current to
[00:23:43:510 - 00:23:44:630] **Speaker 1:** be discontinuous.
[00:23:44:869 - 00:23:47:250] **Speaker 1:** We need to make sure that goes down to zero.
[00:23:51:109 - 00:23:57:010] **Speaker 1:** Um With that, uh, requirement, we end up having a
[00:23:57:010 - 00:24:00:530] **Speaker 1:** restriction on the maximum size or the maximum value of
[00:24:00:530 - 00:24:01:449] **Speaker 1:** the duty ratio.
[00:24:02:630 - 00:24:06:260] **Speaker 1:** Depending on the turns ratio of N3 and N1.
[00:24:07:390 - 00:24:08:810] **Speaker 1:** Oh, where did that come from?
[00:24:09:109 - 00:24:12:430] **Speaker 1:** Well, it's, it comes from exactly the same way that
[00:24:12:430 - 00:24:15:189] **Speaker 1:** we've always looked at the, uh, the analysis of these
[00:24:15:189 - 00:24:15:790] **Speaker 1:** inductors.
[00:24:16:069 - 00:24:20:630] **Speaker 1:** We say that the change in current has to equal
[00:24:20:630 - 00:24:23:369] **Speaker 1:** zero on average cycle by cycle.
[00:24:23:790 - 00:24:24:699] **Speaker 1:** So let's go through that.
[00:24:24:790 - 00:24:26:550] **Speaker 1:** So we've got Delta ILM.
[00:24:27:560 - 00:24:28:859] **Speaker 1:** When the switch is closed.
[00:24:31:209 - 00:24:35:119] **Speaker 1:** Plus Delta ILM when the switch is open.
[00:24:35:949 - 00:24:37:189] **Speaker 1:** Must equal 0.
[00:24:40:290 - 00:24:45:020] **Speaker 1:** That gives us Uh, well, Delta ILM when the switches,
[00:24:45:119 - 00:24:49:459] **Speaker 1:** um, closed, we've, we've got an expression for that, BSDT.
[00:24:50:630 - 00:24:57:739] **Speaker 1:** Over LM Alright, um, and when it was, uh, open
[00:24:58:060 - 00:25:00:300] **Speaker 1:** VS, we had the negative here, so we're just pulling
[00:25:00:300 - 00:25:02:819] **Speaker 1:** it up onto the other side of the expression, so
[00:25:02:819 - 00:25:04:900] **Speaker 1:** that's positive, equals VSLM.
[00:25:06:750 - 00:25:12:050] **Speaker 1:** Delta TXN1 over N3, just separate it out.
[00:25:13:599 - 00:25:17:060] **Speaker 1:** Into, into an area that makes it obvious where we
[00:25:17:069 - 00:25:24:560] **Speaker 1:** we um are changing things over, um, and Delta TX
[00:25:24:560 - 00:25:27:439] **Speaker 1:** has to be less than or equal to 1 minus
[00:25:27:439 - 00:25:28:380] **Speaker 1:** D times T.
[00:25:29:469 - 00:25:30:910] **Speaker 1:** So we can throw this in.
[00:25:31:770 - 00:25:34:290] **Speaker 1:** To here for Delta TX.
[00:25:35:339 - 00:25:37:829] **Speaker 1:** Alright, and make this an inequality, alright?
[00:25:37:989 - 00:25:38:729] **Speaker 1:** So we go.
[00:25:39:920 - 00:25:46:180] **Speaker 1:** PS Of LMDT must be less than or equal to,
[00:25:47:619 - 00:25:51:949] **Speaker 1:** VS over LM, right, putting this in the delta TX.
[00:25:52:969 - 00:25:58:250] **Speaker 1:** 1 minus D times TN1 over N3.
[00:26:00:900 - 00:26:02:599] **Speaker 1:** So the tea is cancelled.
[00:26:04:430 - 00:26:07:670] **Speaker 1:** The, oh, BS over LM cancels.
[00:26:10:109 - 00:26:11:010] **Speaker 1:** Which is nice.
[00:26:11:810 - 00:26:18:640] **Speaker 1:** And we're left with Um We Bring over uh oh
[00:26:18:640 - 00:26:23:140] **Speaker 1:** no, we're left with, yes, N3 if we bring in
[00:26:23:140 - 00:26:26:479] **Speaker 1:** the turns ratio, so we've got N3 over N1, bringing
[00:26:26:479 - 00:26:27:699] **Speaker 1:** onto this sided.
[00:26:29:319 - 00:26:33:270] **Speaker 1:** Is less than or equal to 1 minus D.
[00:26:37:390 - 00:26:41:359] **Speaker 1:** Then bringing the duty ratios together, we end up with
[00:26:41:709 - 00:26:43:229] **Speaker 1:** D1.
[00:26:44:189 - 00:26:46:670] **Speaker 1:** Plus N3 over N1.
[00:26:48:099 - 00:26:50:060] **Speaker 1:** It's less than or equal to one, right?
[00:26:50:180 - 00:26:52:400] **Speaker 1:** And then you just, OK, bring this over to here
[00:26:52:400 - 00:26:53:900] **Speaker 1:** and you're left with this expression.
[00:26:59:160 - 00:27:01:060] **Speaker 1:** So if we want.
[00:27:04:469 - 00:27:08:189] **Speaker 1:** A wide range of D's, when I say a wide
[00:27:08:189 - 00:27:10:949] **Speaker 1:** range of duty ratio, means to go from up to
[00:27:10:949 - 00:27:13:430] **Speaker 1:** a larger value of duty ratio, something, you know, up
[00:27:13:430 - 00:27:17:290] **Speaker 1:** to 0.8, 0.9 or so duty ratio.
[00:27:17:790 - 00:27:21:369] **Speaker 1:** Then N3 has to be much less than N1.
[00:27:27:400 - 00:27:29:359] **Speaker 1:** What does that mean for our wave forms that we
[00:27:29:359 - 00:27:30:459] **Speaker 1:** looked at before?
[00:27:35:880 - 00:27:39:579] **Speaker 1:** Well, if N3 is less than N1, we get the
[00:27:39:579 - 00:27:43:459] **Speaker 1:** added benefit of the delta T being being less.
[00:27:44:550 - 00:27:48:369] **Speaker 1:** So this would be for N3 less than N1.
[00:27:50:719 - 00:27:52:439] **Speaker 1:** So Delta T would be smaller.
[00:27:58:689 - 00:28:01:569] **Speaker 1:** Your LM, it reduces down faster.
[00:28:04:270 - 00:28:08:819] **Speaker 1:** Keep going Uh, what's the, what's the other effect?
[00:28:09:099 - 00:28:14:619] **Speaker 1:** Well, I3, if it's going to uh get rid of
[00:28:14:619 - 00:28:17:380] **Speaker 1:** that energy in the core at a shorter amount of
[00:28:17:380 - 00:28:19:760] **Speaker 1:** time, the current has to be higher.
[00:28:21:270 - 00:28:23:369] **Speaker 1:** So I 3 actually comes up.
[00:28:25:910 - 00:28:25:920] **Speaker 1:** Alright.
[00:28:28:010 - 00:28:31:349] **Speaker 1:** So again this is for N3 less than N1.
[00:28:42:079 - 00:28:45:119] **Speaker 1:** Uh, the effect of that, um, can be seen if
[00:28:45:119 - 00:28:46:420] **Speaker 1:** we look at the source.
[00:28:49:790 - 00:28:51:099] **Speaker 1:** Is the source current.
[00:28:53:520 - 00:28:58:630] **Speaker 1:** So I'll keep it in red.
[00:29:00:839 - 00:29:03:550] **Speaker 1:** So it ramps up when it's closed when the switch
[00:29:03:550 - 00:29:05:420] **Speaker 1:** is closed, so to DT.
[00:29:06:699 - 00:29:15:589] **Speaker 1:** Um But this ramp up is I1 plus ILM.
[00:29:20:319 - 00:29:26:420] **Speaker 1:** Then it switches off, it goes negative because the current
[00:29:27:040 - 00:29:31:849] **Speaker 1:** um from The core is feeding back into the source.
[00:29:33:170 - 00:29:35:670] **Speaker 1:** So I3 is feeding back in, so this is.
[00:29:36:489 - 00:29:38:050] **Speaker 1:** -13.
[00:29:42:430 - 00:29:45:510] **Speaker 1:** And then finally you get tea and it switches on
[00:29:45:510 - 00:29:45:810] **Speaker 1:** again.
[00:29:51:069 - 00:29:51:349] **Speaker 1:** Yep.
[00:29:57:410 - 00:30:01:020] **Speaker 1:** Alright, so That seems not too bad.
[00:30:01:599 - 00:30:03:599] **Speaker 1:** We can get to higher duty ratios.
[00:30:04:560 - 00:30:07:599] **Speaker 1:** There is another effect that's happening, um, as we go
[00:30:07:599 - 00:30:10:400] **Speaker 1:** up then in duty ratio, and I've got the question
[00:30:10:400 - 00:30:12:699] **Speaker 1:** there, what about the switch voltage rating?
[00:30:15:880 - 00:30:18:079] **Speaker 1:** Alright, what about the switch voltage rating?
[00:30:24:119 - 00:30:26:800] **Speaker 1:** So if we go back uh one more slide where
[00:30:26:800 - 00:30:27:660] **Speaker 1:** the switch is open.
[00:30:29:319 - 00:30:32:099] **Speaker 1:** We've got, we're thinking here, what is, what is this,
[00:30:32:560 - 00:30:34:719] **Speaker 1:** um, voltage here, V switch.
[00:30:38:569 - 00:30:40:430] **Speaker 1:** When that uh when that's open, well.
[00:30:41:359 - 00:30:44:109] **Speaker 1:** Let's have a look at the voltages associated with the
[00:30:44:109 - 00:30:44:479] **Speaker 1:** windings.
[00:30:44:640 - 00:30:45:459] **Speaker 1:** So we've got.
[00:30:46:579 - 00:30:47:780] **Speaker 1:** This one conducting.
[00:30:49:290 - 00:30:52:729] **Speaker 1:** So we must have at this node, because that's the
[00:30:52:729 - 00:30:56:390] **Speaker 1:** negative, we've got VS so that node is at VS
[00:30:56:930 - 00:30:57:589] **Speaker 1:** voltage.
[00:30:58:170 - 00:31:01:209] **Speaker 1:** Then we've got the primary winding sitting there as well
[00:31:01:209 - 00:31:03:729] **Speaker 1:** before we get to the switch, and we've just said
[00:31:03:729 - 00:31:08:160] **Speaker 1:** that that winding has voltage across it plus minus N1
[00:31:08:160 - 00:31:09:650] **Speaker 1:** over N3 times VS.
[00:31:10:880 - 00:31:12:959] **Speaker 1:** So by the time you get to the switch.
[00:31:14:439 - 00:31:17:020] **Speaker 1:** That's equal to VS.
[00:31:18:119 - 00:31:22:380] **Speaker 1:** Plus N1 over N3 BS.
[00:31:25:219 - 00:31:26:979] **Speaker 1:** But we've just said that if we want to go
[00:31:26:979 - 00:31:30:719] **Speaker 1:** to larger duty ratios, N3 ends up being considerably less
[00:31:30:719 - 00:31:31:410] **Speaker 1:** than N1.
[00:31:34:060 - 00:31:37:109] **Speaker 1:** So you end up with a voltage rating for your
[00:31:37:130 - 00:31:38:770] **Speaker 1:** switch that has to be.
[00:31:39:839 - 00:31:43:479] **Speaker 1:** Well in excess of 2 times the voltage of the
[00:31:43:479 - 00:31:44:560] **Speaker 1:** source coming in.
[00:31:49:660 - 00:31:52:239] **Speaker 1:** Alright, so how does that kind of look?
[00:31:54:390 - 00:31:55:290] **Speaker 1:** Oh, here we go.
[00:32:04:839 - 00:32:09:780] **Speaker 1:** So whilst the, so this will be the switch.
[00:32:13:099 - 00:32:17:300] **Speaker 1:** On the switch is on, it's 0, right?
[00:32:17:489 - 00:32:18:459] **Speaker 1:** Effectively 0.
[00:32:19:449 - 00:32:20:680] **Speaker 1:** So we can go along there.
[00:32:21:060 - 00:32:23:439] **Speaker 1:** As soon as it turns off, we've just defined what
[00:32:23:439 - 00:32:31:569] **Speaker 1:** is that voltage, it peaks up at A voltage of
[00:32:32:229 - 00:32:37:839] **Speaker 1:** the, S1 + N1 over N3.
[00:32:42:849 - 00:32:46:790] **Speaker 1:** And it stays there for Delta T.
[00:32:55:180 - 00:33:01:719] **Speaker 1:** And then it comes down to Yes.
[00:33:03:839 - 00:33:05:160] **Speaker 1:** Why does it come down to BS?
[00:33:07:800 - 00:33:10:750] **Speaker 1:** Well, the switch is still open, but now the core
[00:33:10:750 - 00:33:12:079] **Speaker 1:** is being completely de-energized.
[00:33:12:160 - 00:33:16:439] **Speaker 1:** There is no current flowing in the third winding.
[00:33:17:219 - 00:33:19:020] **Speaker 1:** So if there's no current flowing in the 3rd winding,
[00:33:19:060 - 00:33:22:239] **Speaker 1:** there's no current flowing in the 2nd secondary winding, and
[00:33:22:239 - 00:33:24:579] **Speaker 1:** there's no current flowing in the primary winding because this
[00:33:24:579 - 00:33:25:380] **Speaker 1:** is open circuit.
[00:33:26:140 - 00:33:30:939] **Speaker 1:** Then After time Delta TX, is there flux in the
[00:33:30:939 - 00:33:31:319] **Speaker 1:** core?
[00:33:32:459 - 00:33:32:920] **Speaker 1:** No.
[00:33:33:339 - 00:33:35:339] **Speaker 1:** So if there's no flux in the core, then what
[00:33:35:339 - 00:33:37:739] **Speaker 1:** is the voltage drop across every single winding in that
[00:33:37:739 - 00:33:38:339] **Speaker 1:** transformer?
[00:33:43:260 - 00:33:45:189] **Speaker 1:** No flux, no current.
[00:33:46:819 - 00:33:47:619] **Speaker 1:** No voltage.
[00:33:48:579 - 00:33:49:920] **Speaker 1:** All the voltages are 0.
[00:33:51:770 - 00:33:53:020] **Speaker 1:** Across the windings.
[00:33:53:329 - 00:33:57:170] **Speaker 1:** So if this, if the voltage drop across here is
[00:33:57:170 - 00:33:59:910] **Speaker 1:** 0, what is the voltage on this terminal?
[00:34:00:569 - 00:34:01:579] **Speaker 1:** That's VS.
[00:34:02:449 - 00:34:04:369] **Speaker 1:** So the voltage that switch these.
[00:34:05:369 - 00:34:07:520] **Speaker 1:** When it's open and no current is flowing.
[00:34:08:250 - 00:34:15:010] **Speaker 1:** There's BS So that's what we have here, uh, and
[00:34:15:010 - 00:34:17:719] **Speaker 1:** finally, you turn the switch on again and it drops
[00:34:17:719 - 00:34:19:610] **Speaker 1:** down to 0, the cycle repeats.
[00:34:23:830 - 00:34:30:388] **Speaker 1:** Yeah, So, this can start getting this high voltage can
[00:34:30:388 - 00:34:35:188] **Speaker 1:** start getting rather large if you uh your application requires
[00:34:35:188 - 00:34:37:107] **Speaker 1:** the duty ratio to be large.
[00:34:39:279 - 00:34:43:759] **Speaker 1:** Hence the reason you might want to choose to rather
[00:34:43:759 - 00:34:46:357] **Speaker 1:** than going up to higher duty ratios, you make sure
[00:34:46:357 - 00:34:50:958] **Speaker 1:** the transformer turns ratio gives you that added voltage at
[00:34:50:958 - 00:34:53:438] **Speaker 1:** the output so that you don't need to go so
[00:34:53:438 - 00:34:55:117] **Speaker 1:** high with the duty ratio.
[00:34:59:419 - 00:34:59:429] **Speaker 1:** Right.
[00:35:13:800 - 00:35:15:000] **Speaker 1:** I put Bolton triple.
[00:35:25:080 - 00:35:27:959] **Speaker 1:** Um, I'm not going to go through the full analysis
[00:35:27:959 - 00:35:30:479] **Speaker 1:** because the output voltage riple is exactly the same as
[00:35:30:479 - 00:35:32:280] **Speaker 1:** it is for our butt converter and the way that
[00:35:32:280 - 00:35:35:439] **Speaker 1:** we get there for to get that expression is exactly
[00:35:35:439 - 00:35:38:639] **Speaker 1:** the same, right, so we've been through that, don't want
[00:35:38:639 - 00:35:41:239] **Speaker 1:** to rehash, um, all of that.
[00:35:43:120 - 00:35:45:419] **Speaker 1:** I did say um that.
[00:35:46:969 - 00:35:52:030] **Speaker 1:** Uh, this is a gateway converter, uh, the forward converter
[00:35:52:439 - 00:35:55:889] **Speaker 1:** back type output is very, very commonly used, um.
[00:35:56:979 - 00:35:59:340] **Speaker 1:** And I said that, you know, we end up going
[00:35:59:340 - 00:36:05:120] **Speaker 1:** with multiple switch, uh, converters, uh, that can then, uh
[00:36:06:879 - 00:36:10:469] **Speaker 1:** Be better um utilised for applications.
[00:36:10:760 - 00:36:15:199] **Speaker 1:** So here is one, it has two controlled switches which
[00:36:15:199 - 00:36:19:280] **Speaker 1:** we close and open synchronously, so at the same time.
[00:36:20:040 - 00:36:23:909] **Speaker 1:** Um, by doing this, it does away with having, uh,
[00:36:23:919 - 00:36:26:419] **Speaker 1:** the requirement for 3 windings on our transformer.
[00:36:27:820 - 00:36:29:790] **Speaker 1:** So when the switch is closed you end up with
[00:36:29:790 - 00:36:35:189] **Speaker 1:** BS across here, magnetising inductance not shown modelled.
[00:36:40:169 - 00:36:43:669] **Speaker 1:** LM uh gets energised, you open the switches.
[00:36:44:750 - 00:36:46:149] **Speaker 1:** It was plus minus.
[00:36:46:469 - 00:36:47:790] **Speaker 1:** You opened the switches.
[00:36:48:669 - 00:36:51:419] **Speaker 1:** Plus minus, forward biases your diodes.
[00:36:53:939 - 00:36:56:419] **Speaker 1:** And that energy gets put back into the, into the
[00:36:56:419 - 00:36:56:719] **Speaker 1:** source.
[00:37:00:389 - 00:37:03:830] **Speaker 1:** Alright, so it's a way of doing, uh, it's a
[00:37:03:830 - 00:37:05:350] **Speaker 1:** way of making sure that you don't need to have
[00:37:05:350 - 00:37:06:570] **Speaker 1:** that third winding.
[00:37:07:030 - 00:37:10:149] **Speaker 1:** Add the complexity, of course, of having, uh, two controllable
[00:37:10:149 - 00:37:12:300] **Speaker 1:** switches and one of them in the high side position,
[00:37:12:550 - 00:37:15:610] **Speaker 1:** you need to do some fancy stuff for your, um,
[00:37:15:949 - 00:37:21:739] **Speaker 1:** power supply that, uh, sources the the gate drive circuitry
[00:37:21:739 - 00:37:23:350] **Speaker 1:** for that high side switch.
[00:37:25:550 - 00:37:28:149] **Speaker 1:** OK, so I'm just showing that, you know, we, with
[00:37:28:149 - 00:37:31:669] **Speaker 1:** some slight modification and going to multiple control switches, we
[00:37:31:669 - 00:37:34:659] **Speaker 1:** can come up with uh basic configurations for our, for
[00:37:34:659 - 00:37:35:709] **Speaker 1:** our forward converter.
[00:37:39:649 - 00:37:44:530] **Speaker 1:** Just before we finish off for today, um, I did
[00:37:44:530 - 00:37:49:889] **Speaker 1:** want to just, um, mention the, the, the one of
[00:37:49:889 - 00:37:53:110] **Speaker 1:** the homework problems associated with the Ford converter.
[00:37:53:520 - 00:37:57:330] **Speaker 1:** Um, it, it, when you first see it, it can
[00:37:57:330 - 00:37:59:889] **Speaker 1:** be a little, maybe a little confusing of how to
[00:37:59:889 - 00:38:01:929] **Speaker 1:** approach it and come up with a solution.
[00:38:05:909 - 00:38:07:580] **Speaker 1:** So here is what it looks like.
[00:38:09:020 - 00:38:13:510] **Speaker 1:** In the homework, um, first thing that might jump out
[00:38:13:510 - 00:38:15:590] **Speaker 1:** at you is, is this the same circuit?
[00:38:16:840 - 00:38:20:000] **Speaker 1:** Because it's shown in a different way than what it
[00:38:20:000 - 00:38:21:129] **Speaker 1:** was in the lecture notes.
[00:38:21:800 - 00:38:25:800] **Speaker 1:** So just trying to get you used to seeing the
[00:38:25:800 - 00:38:29:870] **Speaker 1:** same circuit, um, shown or drawn in different ways.
[00:38:30:040 - 00:38:32:820] **Speaker 1:** So this is the forward converter still.
[00:38:33:879 - 00:38:38:409] **Speaker 1:** Alright, so the diode is, uh, still in the right
[00:38:38:409 - 00:38:43:489] **Speaker 1:** configuration, the dot convention, notice the dots, it's important to
[00:38:43:489 - 00:38:46:889] **Speaker 1:** follow, um, so this is still our forward converter.
[00:38:49:169 - 00:38:53:610] **Speaker 1:** The other thing is that LM is not expressly shown
[00:38:53:610 - 00:38:56:489] **Speaker 1:** in the in the diagram, but you need to assume
[00:38:56:489 - 00:38:57:169] **Speaker 1:** that it's there.
[00:38:58:129 - 00:39:06:330] **Speaker 1:** Right, so LM Where is it in the question?
[00:39:06:409 - 00:39:10:530] **Speaker 1:** The circuit shown here shows a single switch forward converter
[00:39:10:530 - 00:39:13:320] **Speaker 1:** winding in one has 50 turns and has an inductance
[00:39:13:320 - 00:39:14:330] **Speaker 1:** of 5 mil Henry.
[00:39:16:159 - 00:39:21:800] **Speaker 1:** The supply voltage is 240 volts, um, and switching frequency
[00:39:21:800 - 00:39:22:760] **Speaker 1:** is 60 kilohertz.
[00:39:23:270 - 00:39:25:520] **Speaker 1:** The converter is being designed to supply a maximum of
[00:39:25:520 - 00:39:29:060] **Speaker 1:** 60 volts at a duty cycle of 0.75.
[00:39:30:760 - 00:39:36:120] **Speaker 1:** Right, so LM, we've gone through the exercise of uh
[00:39:36:120 - 00:39:40:550] **Speaker 1:** or in the lecture of saying about using LM um
[00:39:40:550 - 00:39:42:540] **Speaker 1:** and making sure it gets zeroed.
[00:39:43:830 - 00:39:45:520] **Speaker 1:** Where is LM in, in this expression?
[00:39:45:600 - 00:39:47:179] **Speaker 1:** Well, this is just 5 mil Henry.
[00:39:49:229 - 00:39:51:219] **Speaker 1:** Alright, so it's telling you here.
[00:39:52:739 - 00:39:55:489] **Speaker 1:** 1 M1 has an inductance of 5 milliHenry.
[00:39:55:530 - 00:39:58:209] **Speaker 1:** That's what it appears like as far as it being
[00:39:58:209 - 00:39:59:870] **Speaker 1:** connected to this transformer.
[00:40:00:209 - 00:40:02:050] **Speaker 1:** So this is LM.
[00:40:12:540 - 00:40:15:379] **Speaker 1:** Alright, so you look at what happens when the switch
[00:40:15:379 - 00:40:19:020] **Speaker 1:** is closed, when the switch is open, we've just gone
[00:40:19:020 - 00:40:20:100] **Speaker 1:** through all of that.
[00:40:20:989 - 00:40:24:290] **Speaker 1:** It's asking you first of all sketch waveforms including their
[00:40:24:290 - 00:40:27:270] **Speaker 1:** alignment in time, so it's wanting you to kind of
[00:40:27:270 - 00:40:31:110] **Speaker 1:** do it vertically showing all the alignments, showing your source
[00:40:31:110 - 00:40:31:550] **Speaker 1:** current.
[00:40:33:100 - 00:40:38:580] **Speaker 1:** Kind of went through that, um, the current through dio
[00:40:38:580 - 00:40:39:239] **Speaker 1:** D3.
[00:40:40:100 - 00:40:42:580] **Speaker 1:** We've already kind of covered that in the lecture notes.
[00:40:42:939 - 00:40:45:239] **Speaker 1:** The switch voltage, we've also covered in the lecture notes.
[00:40:46:469 - 00:40:46:810] **Speaker 1:** Ha.
[00:40:47:949 - 00:40:53:229] **Speaker 1:** We haven't looked at the voltage across that diode, D3.
[00:40:55:270 - 00:40:57:300] **Speaker 1:** So this is asking you something that you haven't looked
[00:40:57:300 - 00:41:00:770] **Speaker 1:** at yet or haven't considered as part of the lecture.
[00:41:04:010 - 00:41:06:679] **Speaker 1:** So the voltage across the diet, what it's wanting you
[00:41:06:679 - 00:41:10:389] **Speaker 1:** to do is look at what's happening um across that
[00:41:10:889 - 00:41:13:889] **Speaker 1:** that winding when the switch is closed and when it's
[00:41:13:889 - 00:41:14:330] **Speaker 1:** open.
[00:41:15:899 - 00:41:25:870] **Speaker 1:** Yeah So the voltage across D3.
[00:41:26:580 - 00:41:29:449] **Speaker 1:** So of course you put that in the axis DT
[00:41:30:719 - 00:41:33:830] **Speaker 1:** said it's 0.75, so it's gonna be most of the,
[00:41:34:790 - 00:41:40:550] **Speaker 1:** Most of the period Uh, we want a Delta TX
[00:41:40:550 - 00:41:41:639] **Speaker 1:** as well, of course.
[00:41:43:169 - 00:41:47:750] **Speaker 1:** So Delta TX must be less than 1 minus.
[00:41:49:159 - 00:41:50:239] **Speaker 1:** D times T.
[00:41:50:679 - 00:41:52:320] **Speaker 1:** Oops, sorry, up there.
[00:41:55:169 - 00:41:56:739] **Speaker 1:** Alright, when the switch is closed.
[00:41:57:239 - 00:42:01:360] **Speaker 1:** When the switch is closed, you've got plus minus VS.
[00:42:04:929 - 00:42:05:360] **Speaker 1:** Yeah.
[00:42:08:070 - 00:42:10:949] **Speaker 1:** Plus minus BS across that winding with that switch closed.
[00:42:11:500 - 00:42:15:540] **Speaker 1:** So what is it you've got plus minus, plus minus
[00:42:15:540 - 00:42:18:199] **Speaker 1:** this one would be N2 over N1.
[00:42:19:030 - 00:42:21:209] **Speaker 1:** It is plus minus.
[00:42:24:780 - 00:42:25:739] **Speaker 1:** What's that voltage?
[00:42:25:850 - 00:42:27:560] **Speaker 1:** What, what's the turns ratio we're gonna do?
[00:42:28:780 - 00:42:28:790] **Speaker 1:** Yep.
[00:42:31:409 - 00:42:33:610] **Speaker 1:** N3 of N1 times BS.
[00:42:35:389 - 00:42:37:530] **Speaker 1:** When the switch is closed.
[00:42:39:300 - 00:42:44:020] **Speaker 1:** Is that the voltage across D3, N3 over N1 times
[00:42:44:020 - 00:42:44:560] **Speaker 1:** VS?
[00:42:49:250 - 00:42:49:899] **Speaker 1:** Yes, no.
[00:42:53:070 - 00:42:54:070] **Speaker 1:** Well, no.
[00:42:55:100 - 00:42:59:550] **Speaker 1:** Because if you look At this node So with that
[00:42:59:550 - 00:43:01:169] **Speaker 1:** switch closed, that's VS.
[00:43:03:610 - 00:43:07:560] **Speaker 1:** And you're saying across this winding that side is BS
[00:43:07:560 - 00:43:10:850] **Speaker 1:** and then you're adding N3 over N1 times VS.
[00:43:11:719 - 00:43:14:969] **Speaker 1:** So the voltage With the switch closed.
[00:43:15:770 - 00:43:21:179] **Speaker 1:** Is VS times 1 plus N3.
[00:43:22:090 - 00:43:23:010] **Speaker 1:** Of the N1.
[00:43:28:110 - 00:43:30:310] **Speaker 1:** Right, so that was, that was the bit that we
[00:43:30:310 - 00:43:31:530] **Speaker 1:** were looking at for there.
[00:43:31:959 - 00:43:33:129] **Speaker 1:** You turn off the switch.
[00:43:35:270 - 00:43:38:389] **Speaker 1:** The core flux starts collapsing.
[00:43:38:820 - 00:43:42:590] **Speaker 1:** We look at what happens across LM, uh, at the
[00:43:42:590 - 00:43:45:409] **Speaker 1:** voltage reverses across LM.
[00:43:45:909 - 00:43:49:370] **Speaker 1:** The voltage reverses on all the windings, D3 starts conducting.
[00:43:49:699 - 00:43:51:830] **Speaker 1:** D3 starts conducting, what's the voltage drop across it?
[00:43:55:219 - 00:43:58:929] **Speaker 1:** It's a diode 0, yep.
[00:44:01:120 - 00:44:04:159] **Speaker 1:** So its voltage drops down to zero whilst it's conducting
[00:44:04:360 - 00:44:09:560] **Speaker 1:** it only conducts until that core is completely de-energized, so
[00:44:09:560 - 00:44:11:030] **Speaker 1:** that takes time delta t.
[00:44:11:110 - 00:44:13:580] **Speaker 1:** I should have really chosen a different colour, shouldn't I?
[00:44:20:120 - 00:44:21:729] **Speaker 1:** Uh, so it goes down to 0 for DT.
[00:44:22:879 - 00:44:26:620] **Speaker 1:** And then for the rest of the time, we've got
[00:44:27:239 - 00:44:30:159] **Speaker 1:** no current flowing through, so we've got BS on this
[00:44:30:159 - 00:44:33:570] **Speaker 1:** side, so no voltage drop, so VS.
[00:44:35:320 - 00:44:38:439] **Speaker 1:** So it comes up to equal BS.
[00:44:46:750 - 00:44:48:590] **Speaker 1:** And then the cycle repeats.
[00:44:49:830 - 00:44:52:179] **Speaker 1:** So I should show that that starts at BS.
[00:44:53:330 - 00:44:56:659] **Speaker 1:** Goes up, starts at BS and then goes back up.
[00:45:04:250 - 00:45:08:090] **Speaker 1:** Alright, you can probably handle the rest of the uh
[00:45:08:090 - 00:45:10:209] **Speaker 1:** the problem yourself, so I'll leave that for you to
[00:45:10:209 - 00:45:13:449] **Speaker 1:** do, but those were the bits that might have confused
[00:45:13:449 - 00:45:14:949] **Speaker 1:** you to get started.
[00:45:15:409 - 00:45:15:830] **Speaker 1:** Alright.
[00:45:16:229 - 00:45:17:129] **Speaker 1:** OK, that's it for today.
[00:45:17:510 - 00:45:19:570] **Speaker 1:** Hope you have a good rest of your Friday.

# ENEL372-26S2 Lecture 16 native Echo transcript

Date: August 17, 2026 4:00pm-4:55pm
Transcript type: native Echo automated transcript.

[00:00:01:799 - 00:00:07:400] **Speaker 0:** Alright, Kyorakoto, we'll kick things off, right, um, I guess
[00:00:07:400 - 00:00:10:680] **Speaker 0:** maybe some people are working on some other, uh, activities
[00:00:10:680 - 00:00:12:420] **Speaker 0:** or Learning at the moment.
[00:00:12:579 - 00:00:15:220] **Speaker 0:** I, I do realise that this week is quite the
[00:00:15:220 - 00:00:18:260] **Speaker 0:** full-on week for a number of people, so I'm keeping
[00:00:18:260 - 00:00:22:860] **Speaker 0:** this, um, uh, the lectures this week fairly lightweight, relatively,
[00:00:23:059 - 00:00:26:500] **Speaker 0:** um, and we won't be needing the last lecture this
[00:00:26:500 - 00:00:27:579] **Speaker 0:** Friday at all.
[00:00:27:940 - 00:00:30:379] **Speaker 0:** So, uh, please don't show up on Friday because there
[00:00:30:379 - 00:00:31:840] **Speaker 0:** won't be, I won't be here.
[00:00:32:180 - 00:00:33:540] **Speaker 0:** The the lecture won't be on.
[00:00:33:900 - 00:00:36:119] **Speaker 0:** So we're finishing off with just two lectures this week.
[00:00:36:500 - 00:00:38:819] **Speaker 0:** And that, uh, the material that we're finishing off on
[00:00:38:819 - 00:00:44:259] **Speaker 0:** is to cover what is, um, another quite important area
[00:00:44:259 - 00:00:45:099] **Speaker 0:** for power electronics.
[00:00:45:220 - 00:00:48:520] **Speaker 0:** It's not just all about DC to DC conversion.
[00:00:48:939 - 00:00:52:759] **Speaker 0:** Uh, we do have, um, I guess next in line
[00:00:52:759 - 00:00:56:340] **Speaker 0:** is for importance is, um, DC to AC.
[00:00:56:700 - 00:01:00:220] **Speaker 0:** So taking a DC uh source and being able to
[00:01:00:220 - 00:01:04:459] **Speaker 0:** convert that into some AC, um, wave form, uh, in
[00:01:04:459 - 00:01:05:959] **Speaker 0:** a power type sense.
[00:01:07:300 - 00:01:10:940] **Speaker 0:** Uh, the DC to AC function for our converters has
[00:01:10:940 - 00:01:11:699] **Speaker 0:** a specific name.
[00:01:11:779 - 00:01:14:470] **Speaker 0:** I mentioned this, um, earlier on, and they are known
[00:01:14:470 - 00:01:15:739] **Speaker 0:** as inverters.
[00:01:16:860 - 00:01:21:930] **Speaker 0:** Right, um, The primary industrial application for inverters um is
[00:01:21:930 - 00:01:23:830] **Speaker 0:** in speed control of AC motors.
[00:01:24:209 - 00:01:27:790] **Speaker 0:** Uh, it's clearly, it's not the only, um, industrial application,
[00:01:27:889 - 00:01:28:849] **Speaker 0:** but it's one of the biggies.
[00:01:29:620 - 00:01:33:190] **Speaker 0:** Uh, so the load will often appear as a series
[00:01:33:190 - 00:01:34:250] **Speaker 0:** LRLS.
[00:01:35:730 - 00:01:38:730] **Speaker 0:** So I threw it there as, as an acronym straight
[00:01:38:730 - 00:01:38:949] **Speaker 0:** away.
[00:01:39:489 - 00:01:41:959] **Speaker 0:** Uh, does anyone have any idea of what an RLS
[00:01:41:959 - 00:01:44:209] **Speaker 0:** load might, might indicate?
[00:01:45:099 - 00:01:47:760] **Speaker 0:** The R and the L is fairly self-explanatory.
[00:01:47:839 - 00:01:52:279] **Speaker 0:** It's a resistive, inductive, but what else do do our
[00:01:52:279 - 00:01:54:339] **Speaker 0:** motors appear as a load?
[00:01:58:089 - 00:02:00:400] **Speaker 0:** That's source, yes.
[00:02:00:760 - 00:02:02:120] **Speaker 0:** So that's what we've got here.
[00:02:02:400 - 00:02:05:500] **Speaker 0:** There's resistance, inductance and source.
[00:02:06:300 - 00:02:09:729] **Speaker 0:** Alright, um, the source being the back EMF that is
[00:02:09:729 - 00:02:11:580] **Speaker 0:** created when a motor is spinning.
[00:02:12:809 - 00:02:15:389] **Speaker 0:** Um, we do have the other common types of applications
[00:02:15:389 - 00:02:19:699] **Speaker 0:** which utilise inverters, photovoltaic systems, so needing to go from
[00:02:19:699 - 00:02:22:779] **Speaker 0:** a DC that is produced by your, um, by your
[00:02:22:779 - 00:02:27:020] **Speaker 0:** solar panels into the AC needed to connect to the
[00:02:27:020 - 00:02:27:500] **Speaker 0:** mains.
[00:02:28:309 - 00:02:32:339] **Speaker 0:** Um, uninterruptible power supplies, kind of a similar type of
[00:02:32:339 - 00:02:36:649] **Speaker 0:** application there, uh, powering AC appliances from available DC sources,
[00:02:36:710 - 00:02:40:020] **Speaker 0:** you know, especially mobile type of applications, uh, where the,
[00:02:40:070 - 00:02:41:690] **Speaker 0:** the DC source could be batteries.
[00:02:42:850 - 00:02:48:460] **Speaker 0:** Um I, I guess a space for inverters that's kind
[00:02:48:460 - 00:02:51:699] **Speaker 0:** of, uh, come to the fore a bit, um, sort
[00:02:51:699 - 00:02:55:619] **Speaker 0:** of recently because of the advancement in how fast we
[00:02:55:619 - 00:02:58:940] **Speaker 0:** can switch our semiconductors these days, um, is that inverters
[00:02:58:940 - 00:03:02:240] **Speaker 0:** are being used for, um, audio power amplifiers.
[00:03:02:850 - 00:03:07:250] **Speaker 0:** OK, so those are known as Class D amplifiers, um,
[00:03:07:339 - 00:03:10:020] **Speaker 0:** if you're into that sort of amplifier classifications, yep.
[00:03:18:130 - 00:03:22:410] **Speaker 0:** OK, um, uh, the, the nice thing about, uh, the
[00:03:22:410 - 00:03:27:490] **Speaker 0:** switch mode inverters for, uh, for, um, power amplifiers for
[00:03:27:490 - 00:03:30:869] **Speaker 0:** audio, uh, use is that they're very, very high efficiency.
[00:03:31:130 - 00:03:33:770] **Speaker 0:** Uh, they've got lower cost and they weigh less.
[00:03:35:490 - 00:03:40:490] **Speaker 0:** Um, now, this is gonna sound a little counterintuitive, um,
[00:03:40:770 - 00:03:45:710] **Speaker 0:** but a really good way to, um, lead into, um,
[00:03:46:289 - 00:03:48:880] **Speaker 0:** understanding inverters is by looking at how we drive a
[00:03:48:880 - 00:03:51:110] **Speaker 0:** DC motor from a DC source.
[00:03:52:869 - 00:03:56:070] **Speaker 0:** There was one thing I wanted to mention, um, just
[00:03:56:070 - 00:04:02:039] **Speaker 0:** before jumping into this, um, where With the, the type
[00:04:02:039 - 00:04:05:839] **Speaker 0:** of inverted, um, they're not all created equal.
[00:04:06:199 - 00:04:09:399] **Speaker 0:** So for example, for a photovoltaic system that you might
[00:04:09:399 - 00:04:14:160] **Speaker 0:** have domestically at home, um, they output what's known as,
[00:04:14:279 - 00:04:17:910] **Speaker 0:** um, pure sinusoidal waveforms to connect to mains.
[00:04:18:239 - 00:04:22:640] **Speaker 0:** So their, their output waveform is nice and sinewsoil, so
[00:04:22:640 - 00:04:24:220] **Speaker 0:** you'd call this pure sign.
[00:04:30:200 - 00:04:33:799] **Speaker 0:** But, uh, there are other inverters, which may be, uh,
[00:04:33:809 - 00:04:36:329] **Speaker 0:** for very low-cost types of applications, maybe it is one
[00:04:36:329 - 00:04:39:929] **Speaker 0:** of these, uh, mobile situations where you could have trying
[00:04:39:929 - 00:04:44:989] **Speaker 0:** to power AC appliances, domestic appliances from a, an off-grid,
[00:04:45:209 - 00:04:47:760] **Speaker 0:** um, AC source, in which case you might find the,
[00:04:47:790 - 00:04:52:250] **Speaker 0:** uh, the inverter only outputs a signal that looks like
[00:04:52:250 - 00:04:52:750] **Speaker 0:** this.
[00:04:57:279 - 00:05:00:309] **Speaker 0:** And I think it's a bit of a stretch, but,
[00:05:00:399 - 00:05:05:040] **Speaker 0:** um, they call that kind of wave form, um, modified
[00:05:05:040 - 00:05:05:820] **Speaker 0:** sine wave.
[00:05:09:209 - 00:05:09:220] **Speaker 0:** Alright.
[00:05:10:890 - 00:05:12:079] **Speaker 0:** This is known as modified.
[00:05:21:149 - 00:05:24:829] **Speaker 0:** Clearly not a mathematician involved in that naming, uh, for
[00:05:24:829 - 00:05:25:929] **Speaker 0:** that sort of wave form.
[00:05:26:470 - 00:05:30:489] **Speaker 0:** All right, so we will be kind of relating, uh,
[00:05:30:670 - 00:05:33:049] **Speaker 0:** this terminology a little bit later on in the lecture,
[00:05:33:070 - 00:05:34:929] **Speaker 0:** as well as the, the waveforms involved.
[00:05:36:029 - 00:05:39:070] **Speaker 0:** OK, right, so, leading to understanding inverters.
[00:05:39:369 - 00:05:41:540] **Speaker 0:** Driving a DC motor from a DC source.
[00:05:43:480 - 00:05:44:880] **Speaker 0:** How's this gonna work, right.
[00:05:48:459 - 00:05:50:079] **Speaker 0:** Right, driving a DC motor.
[00:05:53:600 - 00:05:57:399] **Speaker 0:** Right, we can do this by utilising um a basic
[00:05:57:399 - 00:05:58:320] **Speaker 0:** DC chopper.
[00:05:58:670 - 00:06:02:119] **Speaker 0:** Now I have mentioned a basic DC chopper before, um,
[00:06:03:029 - 00:06:05:679] **Speaker 0:** And the 3rd lecture that I provided.
[00:06:05:880 - 00:06:09:920] **Speaker 0:** So but see lecture theory, if you want to um
[00:06:10:489 - 00:06:11:820] **Speaker 0:** go over that again.
[00:06:13:290 - 00:06:15:130] **Speaker 0:** But I will be going over it again here anyway,
[00:06:15:410 - 00:06:18:730] **Speaker 0:** um, so it's very much like a back converter, the
[00:06:18:730 - 00:06:22:570] **Speaker 0:** basic DC chopper, except we don't have, uh, when we're
[00:06:22:570 - 00:06:25:809] **Speaker 0:** connecting a motor for the load any philtre capacitance.
[00:06:26:649 - 00:06:28:410] **Speaker 0:** So we've got, and I'm gonna draw it in a
[00:06:28:410 - 00:06:30:450] **Speaker 0:** kind of funny way and it'll make sense why I'm
[00:06:30:450 - 00:06:32:010] **Speaker 0:** drawing it this way, uh, very shortly.
[00:06:32:130 - 00:06:35:190] **Speaker 0:** So you got your, your DC in and you have
[00:06:35:739 - 00:06:38:010] **Speaker 0:** your, I'm gonna do it as a, as a moss
[00:06:38:010 - 00:06:38:390] **Speaker 0:** fit.
[00:06:39:190 - 00:06:46:470] **Speaker 0:** In channel Alright, and I'm going to call that one.
[00:06:48:279 - 00:06:50:959] **Speaker 0:** And you know I'm gonna draw it out here and
[00:06:50:959 - 00:06:53:299] **Speaker 0:** I've got a little resistance.
[00:06:54:420 - 00:06:55:640] **Speaker 0:** And inductance.
[00:06:56:429 - 00:07:02:809] **Speaker 0:** And then Is our motor.
[00:07:04:799 - 00:07:08:890] **Speaker 0:** With Rotating at angular speed omega.
[00:07:10:570 - 00:07:12:329] **Speaker 0:** Uh, and back.
[00:07:14:179 - 00:07:17:630] **Speaker 0:** He's the negative and if this was a back converter,
[00:07:17:670 - 00:07:21:000] **Speaker 0:** we'd of course have a free-wheeling diode connected in here.
[00:07:22:160 - 00:07:23:040] **Speaker 0:** This way around.
[00:07:24:470 - 00:07:29:510] **Speaker 0:** This is RA, the armature resistance of the motor, and
[00:07:29:510 - 00:07:33:070] **Speaker 0:** this is LA, the inductance of the motor.
[00:07:34:959 - 00:07:38:559] **Speaker 0:** So, a lot of motors, and especially DC motors, you
[00:07:38:559 - 00:07:42:970] **Speaker 0:** can just simply model them this way, a simple RLS
[00:07:43:529 - 00:07:44:730] **Speaker 0:** series connected load.
[00:07:48:089 - 00:07:51:649] **Speaker 0:** Right, so if we turn on switch this one, then
[00:07:51:649 - 00:07:53:850] **Speaker 0:** we're going to expect there to be current flowing.
[00:07:54:790 - 00:07:58:429] **Speaker 0:** From this is our source, the S, through the, through
[00:07:58:429 - 00:08:00:769] **Speaker 0:** the switch, through the resistor and an inductor.
[00:08:03:799 - 00:08:06:420] **Speaker 0:** That current when the switch is one is turned on.
[00:08:09:029 - 00:08:13:730] **Speaker 0:** So we're imparting energy to, not only by driving current
[00:08:13:730 - 00:08:18:510] **Speaker 0:** reverse through a source, so energy from electrical energy to
[00:08:18:510 - 00:08:23:380] **Speaker 0:** mechanical energy, we are also Passing current through an inductance.
[00:08:23:500 - 00:08:28:040] **Speaker 0:** So we're energising the armature inductance.
[00:08:29:260 - 00:08:33:500] **Speaker 0:** So if we then take turn the switch off, the
[00:08:33:500 - 00:08:38:390] **Speaker 0:** energy that's in that inductor is going to uh Um,
[00:08:38:469 - 00:08:41:690] **Speaker 0:** well, the magnetic field will collapse and the energy will
[00:08:42:510 - 00:08:45:229] **Speaker 0:** come out of the inductance by trying to keep that
[00:08:45:229 - 00:08:46:609] **Speaker 0:** current flowing in the same direction.
[00:08:47:349 - 00:08:49:390] **Speaker 0:** Right, but it can only do that if it loops
[00:08:49:390 - 00:08:51:690] **Speaker 0:** around and forward biases the diode.
[00:08:52:229 - 00:08:54:130] **Speaker 0:** So it was plus minus.
[00:08:55:580 - 00:09:00:340] **Speaker 0:** You turn the switch off, becomes plus minus as the
[00:09:00:340 - 00:09:03:330] **Speaker 0:** source drives that current through until all of the energy
[00:09:03:330 - 00:09:05:059] **Speaker 0:** is gone from the inductance.
[00:09:05:500 - 00:09:07:619] **Speaker 0:** So it's it's a sort of like imparts a bit
[00:09:07:619 - 00:09:10:179] **Speaker 0:** more energy to the load, to the motor.
[00:09:11:989 - 00:09:13:640] **Speaker 0:** Uh, to the, to the mechanical load.
[00:09:17:729 - 00:09:19:650] **Speaker 0:** But for a lot of the times, we want to
[00:09:19:650 - 00:09:23:450] **Speaker 0:** be able to um operate this uh this machine, this
[00:09:23:450 - 00:09:27:690] **Speaker 0:** motor, so that we actively break the slowing down.
[00:09:28:409 - 00:09:31:020] **Speaker 0:** Alright, so, how do we achieve that?
[00:09:31:179 - 00:09:36:380] **Speaker 0:** Well, Let's put a 2nd switch in the system.
[00:09:38:119 - 00:09:42:679] **Speaker 0:** And that second switch is going to reside here.
[00:09:51:640 - 00:09:52:919] **Speaker 0:** We're going to call that S2.
[00:09:58:549 - 00:10:02:390] **Speaker 0:** So if we close, if, if we're not worried about
[00:10:02:390 - 00:10:06:510] **Speaker 0:** uh what's happening here now and we close uh S2.
[00:10:07:510 - 00:10:08:869] **Speaker 0:** And this is spinning.
[00:10:09:549 - 00:10:12:789] **Speaker 0:** The motor is spinning, then that will mean that current
[00:10:12:789 - 00:10:17:289] **Speaker 0:** flows from EA, this, this voltage source, through the inductor.
[00:10:18:000 - 00:10:19:340] **Speaker 0:** Down through the switch.
[00:10:20:989 - 00:10:23:109] **Speaker 0:** So now current is going this way.
[00:10:27:570 - 00:10:27:729] **Speaker 0:** Right?
[00:10:27:890 - 00:10:31:510] **Speaker 0:** So that is energy that is being uh taken from
[00:10:32:530 - 00:10:36:969] **Speaker 0:** The mechanical load, uh, it's creating the EMF, so it's
[00:10:36:969 - 00:10:41:289] **Speaker 0:** de-energizing or taking energy out of the load, uh, from
[00:10:41:289 - 00:10:44:750] **Speaker 0:** the momentum that's carried in, in the mechanical load, uh,
[00:10:45:049 - 00:10:49:429] **Speaker 0:** and that is, OK, driving down, uh, through the inductance
[00:10:49:770 - 00:10:52:630] **Speaker 0:** and down through the on switch.
[00:10:53:330 - 00:10:54:890] **Speaker 0:** That inductor is being energised.
[00:10:55:090 - 00:10:57:609] **Speaker 0:** If we turn that switch off now, there has to
[00:10:57:609 - 00:11:00:570] **Speaker 0:** be a current pathway to enable that.
[00:11:00:900 - 00:11:04:549] **Speaker 0:** The the energy in that inductor to get back, uh,
[00:11:04:609 - 00:11:05:849] **Speaker 0:** or, or to dissipate.
[00:11:06:250 - 00:11:08:090] **Speaker 0:** So we need to make sure there is a freewheeling
[00:11:08:090 - 00:11:08:750] **Speaker 0:** diode.
[00:11:11:640 - 00:11:13:599] **Speaker 0:** Connected to the source.
[00:11:16:919 - 00:11:22:380] **Speaker 0:** Because if that switch opens, that was positive negative.
[00:11:23:219 - 00:11:29:190] **Speaker 0:** Across the inductor That polarity reverses plus minus, so it
[00:11:29:190 - 00:11:33:390] **Speaker 0:** adds with EA to as far as it needs to
[00:11:33:390 - 00:11:35:109] **Speaker 0:** go to keep that current flowing.
[00:11:35:590 - 00:11:36:710] **Speaker 0:** What have I just described?
[00:11:36:869 - 00:11:38:590] **Speaker 0:** I've just described a boost converter.
[00:11:39:500 - 00:11:41:780] **Speaker 0:** Right, by having this switch here and this free-wheeling diode
[00:11:41:780 - 00:11:44:609] **Speaker 0:** here, if we were just looking at the circuit involved
[00:11:44:609 - 00:11:47:179] **Speaker 0:** with that, with the inductor here and the voltage source
[00:11:47:179 - 00:11:48:940] **Speaker 0:** here, that is a boost converter.
[00:11:54:570 - 00:11:57:450] **Speaker 0:** All right, so that can, if we operated that switch
[00:11:57:450 - 00:12:00:650] **Speaker 0:** after the, um, you know, we've gone through the the
[00:12:00:650 - 00:12:03:979] **Speaker 0:** uh situation where we'd closed switch one, we'd imparted energy
[00:12:03:979 - 00:12:07:830] **Speaker 0:** to uh the inductance, we're driving the motor.
[00:12:08:580 - 00:12:12:640] **Speaker 0:** Right, so we're doing forward driving quadrant one operation, um,
[00:12:13:070 - 00:12:14:369] **Speaker 0:** and then we turn that switch off.
[00:12:15:849 - 00:12:19:530] **Speaker 0:** Free-wheeling die goes, still imparting energy to the to the
[00:12:19:530 - 00:12:22:619] **Speaker 0:** load, but the energy collapses and falls to zero.
[00:12:22:890 - 00:12:24:799] **Speaker 0:** So all the, all that current would stop.
[00:12:26:239 - 00:12:29:159] **Speaker 0:** And the, and the, um, basically the motor would be
[00:12:29:159 - 00:12:29:739] **Speaker 0:** freewheeling.
[00:12:30:739 - 00:12:33:940] **Speaker 0:** Yeah, not, not, um, trying to slow it, break, break
[00:12:33:940 - 00:12:35:750] **Speaker 0:** it down at all, it'd just be coasting.
[00:12:37:070 - 00:12:39:349] **Speaker 0:** Then we turn on switch S2, right?
[00:12:39:429 - 00:12:42:030] **Speaker 0:** By turning on switch S2, we are now operating in
[00:12:42:030 - 00:12:47:030] **Speaker 0:** quadrant 4, so we're actively breaking a forward moving uh
[00:12:47:030 - 00:12:47:549] **Speaker 0:** load.
[00:12:48:520 - 00:12:48:700] **Speaker 0:** What?
[00:12:50:809 - 00:12:54:640] **Speaker 0:** And then we turn off switch 2 and that diode,
[00:12:54:719 - 00:12:57:450] **Speaker 0:** we'll call these diode 1s and diode diode 2, so
[00:12:57:450 - 00:12:59:450] **Speaker 0:** D2 and D1.
[00:13:01:229 - 00:13:06:179] **Speaker 0:** So dye D2 conducts and um allows that uh energy
[00:13:06:179 - 00:13:07:580] **Speaker 0:** and that conductance to dissipate.
[00:13:11:849 - 00:13:14:890] **Speaker 0:** In the, in the back converter operation, we're going turning
[00:13:14:890 - 00:13:17:669] **Speaker 0:** on S1, turning it off, D1 conducts.
[00:13:18:820 - 00:13:21:460] **Speaker 0:** Then we turn on this one again and turn it
[00:13:21:460 - 00:13:22:880] **Speaker 0:** off and D1 conducts.
[00:13:24:950 - 00:13:28:659] **Speaker 0:** What would happen if we did turn on this one.
[00:13:30:190 - 00:13:31:650] **Speaker 0:** Turned it off.
[00:13:32:419 - 00:13:34:900] **Speaker 0:** And then turned on S2 while D1 was conducting.
[00:13:40:400 - 00:13:41:210] **Speaker 0:** Would that be a bad thing?
[00:13:43:440 - 00:13:44:849] **Speaker 0:** Actually, no, it's not a bad thing at all.
[00:13:44:960 - 00:13:47:820] **Speaker 0:** What I've just described there is a synchronous back converter
[00:13:47:820 - 00:13:47:830] **Speaker 0:** operation.
[00:13:49:239 - 00:13:54:500] **Speaker 0:** So synchronous back converters will have two switches and one
[00:13:54:849 - 00:13:57:520] **Speaker 0:** controllable switch across the free-wheeling diode.
[00:13:57:989 - 00:14:01:239] **Speaker 0:** And the idea is that you turn on just like
[00:14:01:239 - 00:14:03:359] **Speaker 0:** normal but converter operation, you turn on the switch.
[00:14:04:419 - 00:14:05:500] **Speaker 0:** energise the inductance.
[00:14:05:539 - 00:14:07:080] **Speaker 0:** You turn that switch off.
[00:14:07:869 - 00:14:11:229] **Speaker 0:** And then to keep, keep it flowing, yep, the inductive
[00:14:11:229 - 00:14:15:510] **Speaker 0:** voltage reverses, drives the current through the diode, but then
[00:14:15:510 - 00:14:18:710] **Speaker 0:** you turn on S2 and because of the low RDS
[00:14:18:710 - 00:14:22:270] **Speaker 0:** on and the forward voltage drop across the diode, you
[00:14:22:270 - 00:14:24:010] **Speaker 0:** actually have less voltage drop.
[00:14:24:380 - 00:14:27:989] **Speaker 0:** There's no problem whatsoever of current flowing backwards through a
[00:14:27:989 - 00:14:31:150] **Speaker 0:** moss pit like this, so you end up with less
[00:14:31:150 - 00:14:35:869] **Speaker 0:** voltage drop across the diode and efficiency benefit because of
[00:14:35:869 - 00:14:37:309] **Speaker 0:** that because you've got the same current.
[00:14:38:450 - 00:14:40:330] **Speaker 0:** Same level of current, but less voltage drop.
[00:14:40:650 - 00:14:44:559] **Speaker 0:** So it's a more efficient converter by having that synchronous
[00:14:44:559 - 00:14:44:770] **Speaker 0:** operation.
[00:14:47:929 - 00:14:48:520] **Speaker 0:** OK.
[00:14:49:799 - 00:14:54:070] **Speaker 0:** So, um, it's kind of why the TL 494 for
[00:14:54:070 - 00:15:00:309] **Speaker 0:** your solar car project has two output BJTs.
[00:15:01:010 - 00:15:04:809] **Speaker 0:** It's because with the right configuration, you could use those
[00:15:04:809 - 00:15:09:489] **Speaker 0:** two outputs to separately drive the uh S1 and S2
[00:15:09:489 - 00:15:11:679] **Speaker 0:** in synchronous spark mode conversion uh um converter.
[00:15:18:090 - 00:15:20:539] **Speaker 0:** Right What about the other side?
[00:15:20:859 - 00:15:26:489] **Speaker 0:** If you've turned on switch S2, um, energising through this
[00:15:26:489 - 00:15:29:299] **Speaker 0:** way and then you turn that off and dial D2
[00:15:29:299 - 00:15:33:780] **Speaker 0:** conducts, could you not switch on S1 while D2 is
[00:15:33:780 - 00:15:34:340] **Speaker 0:** conducting?
[00:15:35:650 - 00:15:37:809] **Speaker 0:** Yeah, you could, and what you've just described there, well,
[00:15:37:859 - 00:15:40:729] **Speaker 0:** what I've just described there is a synchronous boost converter.
[00:15:41:539 - 00:15:41:559] **Speaker 0:** Huh.
[00:15:44:270 - 00:15:48:630] **Speaker 0:** And not only that, is that we can switch S1
[00:15:48:630 - 00:15:52:530] **Speaker 0:** and S2 since we've got the dives there, um, separately
[00:15:52:750 - 00:15:55:130] **Speaker 0:** at varying duty ratios.
[00:15:55:989 - 00:15:59:750] **Speaker 0:** And by just changing the duty ratio, we can define
[00:15:59:750 - 00:16:03:409] **Speaker 0:** whether we are making a power flow to the load
[00:16:03:909 - 00:16:05:950] **Speaker 0:** or taking power from the load.
[00:16:07:859 - 00:16:09:219] **Speaker 0:** Just by varying the duty ratio.
[00:16:17:309 - 00:16:21:030] **Speaker 0:** Um, there is a bit of an operational no no.
[00:16:21:679 - 00:16:24:250] **Speaker 0:** That we've got, if we, if we make a circuit
[00:16:24:250 - 00:16:27:239] **Speaker 0:** like that, it is we do never, we never turn
[00:16:27:239 - 00:16:29:380] **Speaker 0:** on S1 and S2 at the same time.
[00:16:30:880 - 00:16:34:159] **Speaker 0:** They, you can turn on S1, then S2, and then
[00:16:34:159 - 00:16:37:599] **Speaker 0:** S1 and then S2, but not together because if you
[00:16:37:599 - 00:16:40:280] **Speaker 0:** do, that's just a dead short to ground uh across
[00:16:40:280 - 00:16:41:900] **Speaker 0:** the power supply.
[00:16:42:280 - 00:16:45:000] **Speaker 0:** Lots and lots of current and lots of magic smoke.
[00:16:49:690 - 00:16:54:130] **Speaker 0:** Um, to absolutely ensure that it's foolproof and you can't
[00:16:54:130 - 00:16:58:599] **Speaker 0:** do that accidentally, then control chips like the TL 494
[00:16:58:599 - 00:17:02:169] **Speaker 0:** will build in what's called dead time, and it will
[00:17:02:169 - 00:17:05:180] **Speaker 0:** make sure that you can't turn them both on together,
[00:17:05:630 - 00:17:08:140] **Speaker 0:** and there's this little short amount of time in between
[00:17:08:140 - 00:17:09:969] **Speaker 0:** where one can turn off and the next one can
[00:17:09:969 - 00:17:10:430] **Speaker 0:** turn on.
[00:17:13:589 - 00:17:13:609] **Speaker 0:** All right.
[00:17:17:069 - 00:17:19:910] **Speaker 0:** With the motor load in commodation, and the switches and
[00:17:19:910 - 00:17:22:310] **Speaker 0:** dials that we've just got, we have the ability to
[00:17:22:310 - 00:17:23:589] **Speaker 0:** operate in two of the four quadrants.
[00:17:23:640 - 00:17:26:630] **Speaker 0:** I kind of mentioned that in buck mode, you've got,
[00:17:26:750 - 00:17:29:469] **Speaker 0:** well, we've got torque and speed, but then we just
[00:17:29:469 - 00:17:34:910] **Speaker 0:** convert that to current and voltage on those axes.
[00:17:37:459 - 00:17:41:099] **Speaker 0:** Then we have positive voltage and current, and that's forward
[00:17:41:099 - 00:17:41:560] **Speaker 0:** driving.
[00:17:42:420 - 00:17:42:540] **Speaker 0:** Right?
[00:17:42:619 - 00:17:43:619] **Speaker 0:** This is the buck mode.
[00:17:46:949 - 00:17:47:790] **Speaker 0:** In quadrant one.
[00:17:48:650 - 00:17:54:569] **Speaker 0:** Actively breaking a forward moving uh load is, is, as
[00:17:54:569 - 00:17:56:150] **Speaker 0:** I mentioned, is quadrant 4.
[00:17:56:890 - 00:17:58:369] **Speaker 0:** So this is boost mode.
[00:18:11:290 - 00:18:17:150] **Speaker 0:** Alright, that's driving a DC motor from a DC source.
[00:18:19:160 - 00:18:21:560] **Speaker 0:** The DC source is good, but is that an AC,
[00:18:22:000 - 00:18:23:040] **Speaker 0:** is that an AC load?
[00:18:23:239 - 00:18:24:979] **Speaker 0:** We've got current flowing in both directions.
[00:18:26:839 - 00:18:27:900] **Speaker 0:** We're not far away.
[00:18:28:920 - 00:18:33:040] **Speaker 0:** If we just Change up a little bit, just a
[00:18:33:040 - 00:18:36:650] **Speaker 0:** little bit the way that the load is connected to
[00:18:36:650 - 00:18:39:089] **Speaker 0:** that circuit with the two switches and the two dodes,
[00:18:39:449 - 00:18:40:589] **Speaker 0:** then we've, we've got it.
[00:18:44:979 - 00:18:49:540] **Speaker 0:** Just before I get there, I will identify that that
[00:18:49:540 - 00:18:52:900] **Speaker 0:** quadrant 1 and quadrant 4 operation isn't gonna cut it
[00:18:52:900 - 00:18:56:579] **Speaker 0:** if we want to uh drive an AC load from
[00:18:56:579 - 00:18:57:719] **Speaker 0:** a DC source.
[00:18:58:180 - 00:18:58:800] **Speaker 0:** Why not?
[00:18:59:459 - 00:19:05:660] **Speaker 0:** Well, consider these typical AC waveforms, including the phase difference
[00:19:05:660 - 00:19:05:859] **Speaker 0:** between them.
[00:19:06:020 - 00:19:09:140] **Speaker 0:** So in red, we've got the voltage that we might
[00:19:09:140 - 00:19:11:780] **Speaker 0:** have at the load, and in blue is the current
[00:19:11:780 - 00:19:13:180] **Speaker 0:** associated with that load.
[00:19:13:880 - 00:19:15:760] **Speaker 0:** There is a phase difference.
[00:19:16:319 - 00:19:18:380] **Speaker 0:** Uh, not only that, the phase difference.
[00:19:19:439 - 00:19:20:770] **Speaker 0:** Here, which we might call fire.
[00:19:22:219 - 00:19:34:089] **Speaker 0:** Oops Um, indicates that in this instance, the load is
[00:19:34:089 - 00:19:35:719] **Speaker 0:** slightly inductive.
[00:19:37:900 - 00:19:38:869] **Speaker 0:** How did I come by that?
[00:19:38:989 - 00:19:44:640] **Speaker 0:** Um, so there is this, um, acronym you can use.
[00:19:45:689 - 00:19:47:619] **Speaker 0:** Sybil, have we come across this before?
[00:19:49:380 - 00:19:51:660] **Speaker 0:** Have the Mch guys come across it before?
[00:19:51:939 - 00:19:52:180] **Speaker 0:** Yep.
[00:19:52:380 - 00:19:53:140] **Speaker 0:** Oh, sweet.
[00:19:53:300 - 00:19:55:359] **Speaker 0:** Soleck and Mac have, have covered this.
[00:19:56:020 - 00:19:59:819] **Speaker 0:** Um, so for a capacitive circuit, current leads voltage, and
[00:19:59:819 - 00:20:04:400] **Speaker 0:** voltage leads current for an inductive circuit, which is the
[00:20:04:849 - 00:20:05:920] **Speaker 0:** case that we have.
[00:20:06:260 - 00:20:08:969] **Speaker 0:** This is an inductive circuit and why we've shown a
[00:20:08:969 - 00:20:12:859] **Speaker 0:** special case of an inductive circuit because of the RL
[00:20:12:859 - 00:20:17:160] **Speaker 0:** source loads that we generally experience, right, where the L.
[00:20:17:949 - 00:20:19:849] **Speaker 0:** Causes this kind of phase shift.
[00:20:23:530 - 00:20:24:989] **Speaker 0:** A motor load.
[00:20:30:130 - 00:20:31:050] **Speaker 0:** It's seductive.
[00:20:33:000 - 00:20:36:369] **Speaker 0:** Um, and this alone tells us that we need 4
[00:20:36:369 - 00:20:37:660] **Speaker 0:** quadrant operation.
[00:20:38:050 - 00:20:38:369] **Speaker 0:** How?
[00:20:39:130 - 00:20:43:270] **Speaker 0:** Well, if you look here, where the current crosses 0.
[00:20:44:880 - 00:20:46:040] **Speaker 0:** And a different colour I think.
[00:20:48:229 - 00:20:49:000] **Speaker 0:** It's my green girl.
[00:20:54:130 - 00:20:57:010] **Speaker 0:** If we look vertically where the current goes from being
[00:20:57:010 - 00:20:59:449] **Speaker 0:** negative to positive, and we'll just draw a vertical line
[00:20:59:449 - 00:20:59:949] **Speaker 0:** up here.
[00:21:02:280 - 00:21:07:719] **Speaker 0:** Here, we've got negative current and positive voltage, so that's
[00:21:07:719 - 00:21:08:699] **Speaker 0:** quadrant 4.
[00:21:11:680 - 00:21:15:770] **Speaker 0:** Alright, then we go from there we have until the
[00:21:15:770 - 00:21:17:130] **Speaker 0:** voltage crosses zero.
[00:21:18:790 - 00:21:21:770] **Speaker 0:** We've got positive current and positive.
[00:21:22:560 - 00:21:23:199] **Speaker 0:** Voltage.
[00:21:23:979 - 00:21:25:589] **Speaker 0:** Which is quadrant one operation.
[00:21:30:930 - 00:21:33:599] **Speaker 0:** Then We've got positive current.
[00:21:34:439 - 00:21:37:400] **Speaker 0:** And Negative voltage.
[00:21:42:319 - 00:21:44:339] **Speaker 0:** So that's Q2, quadrant 2.
[00:21:46:739 - 00:21:50:569] **Speaker 0:** And then finally when, well, yeah, finally, when that uh
[00:21:50:569 - 00:21:53:150] **Speaker 0:** voltage crosses zero again.
[00:21:55:689 - 00:21:57:270] **Speaker 0:** And we've got negative current.
[00:21:58:650 - 00:22:00:829] **Speaker 0:** Negative voltage, negative current, that's quadrant 3.
[00:22:05:099 - 00:22:08:339] **Speaker 0:** And here from that point on, we are just repeating
[00:22:08:339 - 00:22:09:000] **Speaker 0:** the cycle.
[00:22:10:109 - 00:22:14:089] **Speaker 0:** Right, so there, there again.
[00:22:15:119 - 00:22:17:599] **Speaker 0:** We're back to quadrant 4.
[00:22:18:569 - 00:22:20:229] **Speaker 0:** And just the cycle repeats.
[00:22:22:880 - 00:22:27:239] **Speaker 0:** So, we're going to drive uh an AC load that
[00:22:27:239 - 00:22:31:579] **Speaker 0:** has some uh reactive element to it, either inductive capacitive
[00:22:31:579 - 00:22:32:839] **Speaker 0:** or something like that.
[00:22:33:199 - 00:22:35:400] **Speaker 0:** We have to be able to operate in 4 quadrants
[00:22:35:400 - 00:22:38:160] **Speaker 0:** for our driving circuit for the inverter.
[00:22:40:349 - 00:22:43:560] **Speaker 0:** Right, so the circuit that we just looked at, the
[00:22:43:560 - 00:22:46:979] **Speaker 0:** one that includes both the buck and the boost um
[00:22:46:979 - 00:22:47:630] **Speaker 0:** arrangement.
[00:22:48:459 - 00:22:52:500] **Speaker 0:** Can do this If we connect the load the right
[00:22:52:500 - 00:22:52:839] **Speaker 0:** way.
[00:22:56:609 - 00:22:58:189] **Speaker 0:** And what's the right way?
[00:23:01:280 - 00:23:03:800] **Speaker 0:** Well, we don't connect, so this is, this is the
[00:23:03:800 - 00:23:04:239] **Speaker 0:** circuit we have.
[00:23:04:280 - 00:23:07:520] **Speaker 0:** We have the two switches and the 2 free-wheeling diodes,
[00:23:07:800 - 00:23:11:540] **Speaker 0:** and we were taking the, uh, output from that centre
[00:23:11:540 - 00:23:14:319] **Speaker 0:** point between the two switches and diodes and connecting the
[00:23:14:319 - 00:23:16:199] **Speaker 0:** load directly to the negative side.
[00:23:17:910 - 00:23:18:199] **Speaker 0:** Right.
[00:23:18:560 - 00:23:21:680] **Speaker 0:** Instead, what we're going to do is create a 3rd
[00:23:21:680 - 00:23:24:410] **Speaker 0:** or a separate node, the 3rd node, that's at a
[00:23:24:410 - 00:23:26:060] **Speaker 0:** voltage halfway.
[00:23:27:469 - 00:23:31:310] **Speaker 0:** Between our input Voltage, right?
[00:23:31:430 - 00:23:34:109] **Speaker 0:** So we've got VD over 2 and VD over 2,
[00:23:34:150 - 00:23:38:150] **Speaker 0:** and we've created a separate node, because they're equal of
[00:23:38:150 - 00:23:39:069] **Speaker 0:** node O.
[00:23:42:819 - 00:23:45:699] **Speaker 0:** So the load connects between where we.
[00:23:46:479 - 00:23:49:060] **Speaker 0:** Have our output from our buck and our boost.
[00:23:50:770 - 00:23:53:640] **Speaker 0:** But instead of going to the negative, the low connects
[00:23:53:640 - 00:23:55:880] **Speaker 0:** to the halfway voltage point.
[00:24:05:280 - 00:24:09:439] **Speaker 0:** So, that circuit can supply voltages of + VD over
[00:24:09:439 - 00:24:09:939] **Speaker 0:** 2.
[00:24:10:640 - 00:24:13:300] **Speaker 0:** Well, plus VD over 2 if T+ is on.
[00:24:16:000 - 00:24:17:900] **Speaker 0:** And minus is off.
[00:24:21:410 - 00:24:21:890] **Speaker 0:** Can you see that?
[00:24:22:010 - 00:24:25:770] **Speaker 0:** So we turn T+ on the pathway there is to
[00:24:25:770 - 00:24:29:050] **Speaker 0:** here, so that's only VD over 2 across that lobe.
[00:24:30:349 - 00:24:32:430] **Speaker 0:** So BAO.
[00:24:36:989 - 00:24:40:790] **Speaker 0:** That would, you'd call that VA oops.
[00:24:41:979 - 00:24:46:479] **Speaker 0:** A Uh, and minus the other 2, so T+ is
[00:24:46:479 - 00:24:46:819] **Speaker 0:** open.
[00:24:49:010 - 00:24:54:589] **Speaker 0:** This is with T + off and T minus on,
[00:24:55:089 - 00:24:59:390] **Speaker 0:** then that node gets connected to, uh, to ground.
[00:25:00:930 - 00:25:05:189] **Speaker 0:** So A is it relative to O, is it minus
[00:25:05:189 - 00:25:06:030] **Speaker 0:** VD over 2.
[00:25:12:369 - 00:25:15:890] **Speaker 0:** And we can have any duty ratio, so long as
[00:25:15:890 - 00:25:17:609] **Speaker 0:** we don't turn on T+ and at the same time.
[00:25:22:449 - 00:25:24:650] **Speaker 0:** And that will allow current flow to go in both
[00:25:24:650 - 00:25:28:010] **Speaker 0:** directions and enable us to operate in all four quadrants.
[00:25:29:939 - 00:25:32:140] **Speaker 0:** It's known as the half bridge inverter.
[00:25:33:469 - 00:25:35:430] **Speaker 0:** And we can get plus and minus VD over 2.
[00:25:35:949 - 00:25:40:250] **Speaker 0:** There is a quick um change up to the configuration
[00:25:40:250 - 00:25:44:270] **Speaker 0:** to enable us to utilise the full DC voltage in
[00:25:44:550 - 00:25:48:229] **Speaker 0:** to give us plus and minus VD instead of VD
[00:25:48:229 - 00:25:48:750] **Speaker 0:** over 2.
[00:25:49:959 - 00:25:54:079] **Speaker 0:** Oh, by the way, C+ and minus those capacitances are
[00:25:54:079 - 00:25:58:040] **Speaker 0:** considered to be effectively infinitely large, so that the, the
[00:25:58:040 - 00:26:01:819] **Speaker 0:** voltage at O is completely constant and doesn't change.
[00:26:02:579 - 00:26:10:239] **Speaker 0:** It's a reference node Uh So if we double up
[00:26:10:239 - 00:26:12:359] **Speaker 0:** on the number of switches and the number of diodes,
[00:26:12:479 - 00:26:13:739] **Speaker 0:** we end up with a full bridge.
[00:26:17:770 - 00:26:22:130] **Speaker 0:** We still have the load connected, uh, as we did
[00:26:22:130 - 00:26:22:589] **Speaker 0:** before.
[00:26:30:650 - 00:26:35:949] **Speaker 0:** But this time, if we turn on uh TA plus,
[00:26:37:189 - 00:26:46:050] **Speaker 0:** And T minus are on, then that gives us VD.
[00:26:46:869 - 00:26:47:660] **Speaker 0:** Across the load.
[00:26:50:859 - 00:26:51:510] **Speaker 0:** Can you see that?
[00:26:51:900 - 00:26:55:099] **Speaker 0:** So turn TA plus on, you look at the low,
[00:26:55:260 - 00:26:59:109] **Speaker 0:** go through here and TB minus is on, then that's
[00:26:59:109 - 00:27:00:699] **Speaker 0:** the full VD across that load.
[00:27:02:030 - 00:27:11:550] **Speaker 0:** Alternatively, if you have TB plus on, And minus on.
[00:27:13:880 - 00:27:15:439] **Speaker 0:** That gives us minus VD.
[00:27:16:750 - 00:27:21:390] **Speaker 0:** So TP plus, this side of the of the load
[00:27:21:390 - 00:27:24:589] **Speaker 0:** gets connected to VD and the other side gets connected
[00:27:24:589 - 00:27:25:109] **Speaker 0:** to minus.
[00:27:25:189 - 00:27:28:670] **Speaker 0:** So we've got plus minus across the load the other
[00:27:28:670 - 00:27:29:209] **Speaker 0:** way around.
[00:27:38:959 - 00:27:41:300] **Speaker 0:** Right, so the switch sequence is a bit more involved,
[00:27:41:560 - 00:27:42:099] **Speaker 0:** um.
[00:27:43:280 - 00:27:47:020] **Speaker 0:** But We can get any duty ratio again so long
[00:27:47:020 - 00:27:51:010] **Speaker 0:** as we don't turn on um either of the, either
[00:27:51:010 - 00:27:53:260] **Speaker 0:** of the two, these are known as poles, by the
[00:27:53:260 - 00:27:53:560] **Speaker 0:** way.
[00:27:58:760 - 00:28:01:760] **Speaker 0:** Um, either of the TA and minus on a, on
[00:28:01:760 - 00:28:04:619] **Speaker 0:** a single pole together or TB+ and minus.
[00:28:05:400 - 00:28:09:040] **Speaker 0:** Never turn either one of those on together, um, otherwise
[00:28:09:040 - 00:28:12:030] **Speaker 0:** you're going to be, uh, in trouble once again, short
[00:28:12:030 - 00:28:13:839] **Speaker 0:** circuiting across the supply.
[00:28:16:140 - 00:28:19:260] **Speaker 0:** So, hopefully, we can see how we might start generating
[00:28:19:260 - 00:28:25:939] **Speaker 0:** that um That modified sine wave signals that we defined
[00:28:25:939 - 00:28:28:069] **Speaker 0:** before from this sort of a circuit.
[00:28:31:250 - 00:28:34:280] **Speaker 0:** It's time, so we've got that uh.
[00:28:35:290 - 00:28:37:310] **Speaker 0:** That's circuit from before.
[00:28:38:800 - 00:28:42:119] **Speaker 0:** I I mean that wave form from before, the modified
[00:28:42:119 - 00:28:42:979] **Speaker 0:** sine wave.
[00:28:44:420 - 00:28:45:359] **Speaker 0:** Highly modified.
[00:28:49:500 - 00:28:55:390] **Speaker 0:** Where if we've got VD and minus VD.
[00:28:56:770 - 00:29:05:060] **Speaker 0:** That would be TA plus, and T minus TB minus
[00:29:05:060 - 00:29:20:349] **Speaker 0:** on, and then TB+ and minus On I've not told
[00:29:20:349 - 00:29:23:750] **Speaker 0:** you how to get 0 volts across the load.
[00:29:25:410 - 00:29:29:380] **Speaker 0:** So 0 volts across the load.
[00:29:30:140 - 00:29:32:699] **Speaker 0:** How are we going to make sure that this node
[00:29:32:699 - 00:29:36:500] **Speaker 0:** and this node are at the same potential without short
[00:29:36:500 - 00:29:37:060] **Speaker 0:** circuiting.
[00:29:37:900 - 00:29:40:739] **Speaker 0:** Well, we do that by turning on the two upper
[00:29:40:739 - 00:29:45:530] **Speaker 0:** switches or the two lower switches, right?
[00:29:45:660 - 00:29:49:739] **Speaker 0:** So, if we turn on TA+, A goes to VD.
[00:29:50:099 - 00:29:53:459] **Speaker 0:** If we turn on TB+, B goes to VD.
[00:29:53:819 - 00:29:56:260] **Speaker 0:** So the voltage difference across the load is going to
[00:29:56:260 - 00:29:57:319] **Speaker 0:** be 0 volts.
[00:29:58:020 - 00:30:03:359] **Speaker 0:** So we could have TA plus and TB + on.
[00:30:05:310 - 00:30:11:349] **Speaker 0:** Or T minus and minus on.
[00:30:14:229 - 00:30:16:109] **Speaker 0:** To give us 0 volts across the globe.
[00:30:25:060 - 00:30:27:160] **Speaker 0:** Right, we need to do better.
[00:30:27:619 - 00:30:30:260] **Speaker 0:** This is a very, very poor sine wave, alright, for
[00:30:30:260 - 00:30:31:839] **Speaker 0:** our output of our inverter.
[00:30:32:880 - 00:30:36:760] **Speaker 0:** However, just because this is bad, doesn't mean this is
[00:30:36:760 - 00:30:37:260] **Speaker 0:** bad.
[00:30:37:719 - 00:30:39:920] **Speaker 0:** We just need to operate it in a different way.
[00:30:41:739 - 00:30:44:910] **Speaker 0:** Than just a single turn on turn off exercise to
[00:30:44:910 - 00:30:46:670] **Speaker 0:** give us the, the modified sine wave.
[00:30:48:900 - 00:30:54:550] **Speaker 0:** This is where We come in with sinusoidal pulse width
[00:30:54:550 - 00:30:55:380] **Speaker 0:** modulation.
[00:30:57:020 - 00:31:00:199] **Speaker 0:** You're doing pulse with modulation already with all of the,
[00:31:00:300 - 00:31:02:739] **Speaker 0:** the converters that we've looked at with the duty ratio
[00:31:02:739 - 00:31:06:619] **Speaker 0:** change, that's a pulse with change that modulates the output
[00:31:06:619 - 00:31:07:780] **Speaker 0:** voltage of the converter.
[00:31:08:680 - 00:31:13:800] **Speaker 0:** So these have just been DC-based pulse with modulated converters
[00:31:13:800 - 00:31:15:579] **Speaker 0:** that we've been working on with the duty ratio.
[00:31:16:050 - 00:31:19:300] **Speaker 0:** Now we're going to move that into the AC space.
[00:31:26:780 - 00:31:31:020] **Speaker 0:** Right, so the fundamentals of false modulation control, including for
[00:31:31:020 - 00:31:33:640] **Speaker 0:** DC, uh, involve.
[00:31:34:390 - 00:31:36:560] **Speaker 0:** This is, we're talking about inverters here, but it includes
[00:31:36:560 - 00:31:40:540] **Speaker 0:** DC involve the interaction or comparison of a reference.
[00:31:42:699 - 00:31:45:680] **Speaker 0:** The control signal and a modulating or carrier signal.
[00:31:47:500 - 00:31:50:699] **Speaker 0:** Right, so in this case, instead of the control signal
[00:31:50:699 - 00:31:54:380] **Speaker 0:** being a constant DC signal, which is kind of what
[00:31:54:380 - 00:31:57:260] **Speaker 0:** we have for our DC to DC converters, um, it
[00:31:57:260 - 00:32:01:359] **Speaker 0:** is an AC signal that is our control signal.
[00:32:01:859 - 00:32:06:180] **Speaker 0:** The, um, modulating or carrier signal is this V tri,
[00:32:06:339 - 00:32:07:719] **Speaker 0:** the triangular waveform.
[00:32:08:300 - 00:32:09:040] **Speaker 0:** Why V tri?
[00:32:09:619 - 00:32:13:859] **Speaker 0:** Because we've always, we will nearly always see for pulsates.
[00:32:14:310 - 00:32:18:660] **Speaker 0:** Modulation, a wave form that is triangular in nature, could
[00:32:18:660 - 00:32:22:500] **Speaker 0:** be sore tooth, so long rise time, short fall, sore
[00:32:22:500 - 00:32:25:900] **Speaker 0:** tooth, but it'll still be triangular because that gives us
[00:32:25:900 - 00:32:30:219] **Speaker 0:** a linear change in output voltage with a linear change
[00:32:30:219 - 00:32:31:119] **Speaker 0:** in input voltage.
[00:32:32:680 - 00:32:39:739] **Speaker 0:** Right The, the reference signal, usually a sinusoid for AC
[00:32:39:810 - 00:32:43:000] **Speaker 0:** applications, but could be any kind of AC signal, including
[00:32:43:000 - 00:32:43:599] **Speaker 0:** audio.
[00:32:46:390 - 00:32:49:310] **Speaker 0:** The modulating signal, as I mentioned, is nearly always a
[00:32:49:310 - 00:32:50:030] **Speaker 0:** triangle wave.
[00:32:50:189 - 00:32:54:069] **Speaker 0:** It's a linear behaviour with frequency, uh, and that.
[00:32:54:920 - 00:32:59:280] **Speaker 0:** Sets the switching frequency of our pulsate modulating converter.
[00:33:04:290 - 00:33:07:089] **Speaker 0:** We can already see that the control signal is a
[00:33:07:089 - 00:33:11:130] **Speaker 0:** very, very much lower frequency signal than our modulation signal.
[00:33:13:469 - 00:33:16:290] **Speaker 0:** We'll talk um in next week, uh next week.
[00:33:17:880 - 00:33:22:510] **Speaker 0:** The next lecture about the the comparison between those frequencies.
[00:33:23:739 - 00:33:28:500] **Speaker 0:** Um, but let's, let's look at what happens whenever, uh,
[00:33:28:510 - 00:33:31:930] **Speaker 0:** we have, since it is a difference or a comparison
[00:33:31:930 - 00:33:35:170] **Speaker 0:** that we're making between control and reference, uh, and modulation,
[00:33:35:579 - 00:33:36:030] **Speaker 0:** um.
[00:33:36:979 - 00:33:41:209] **Speaker 0:** What the the logic change um is between those states.
[00:33:41:410 - 00:33:45:290] **Speaker 0:** So here, we've got the dotted one, we've got the
[00:33:45:290 - 00:33:49:829] **Speaker 0:** control is greater in voltage than our modulation signal.
[00:33:51:989 - 00:33:56:619] **Speaker 0:** So whenever the control is greater than the try, then
[00:33:56:619 - 00:34:01:189] **Speaker 0:** we've got TA or T pluses on and T minuses
[00:34:01:189 - 00:34:01:680] **Speaker 0:** off.
[00:34:03:430 - 00:34:06:349] **Speaker 0:** Shouldn't really say TA because what are the voltage differences
[00:34:06:349 - 00:34:06:469] **Speaker 0:** here?
[00:34:06:550 - 00:34:09:270] **Speaker 0:** VD over 2 and minus VD over 2, which means
[00:34:09:270 - 00:34:11:250] **Speaker 0:** this is a half bridge.
[00:34:18:600 - 00:34:21:148] **Speaker 0:** Alright, so there isn't a set of B switches.
[00:34:21:689 - 00:34:25:689] **Speaker 0:** So saying TA is kind of misleading, this is just
[00:34:25:689 - 00:34:27:229] **Speaker 0:** T+ and minus.
[00:34:28:249 - 00:34:31:479] **Speaker 0:** So, T+ will be on and minus will be off.
[00:34:31:569 - 00:34:35:329] **Speaker 0:** So we have uh VD over 2 is the output
[00:34:35:329 - 00:34:35:989] **Speaker 0:** to the load.
[00:34:37:607 - 00:34:44:408] **Speaker 0:** Whenever the control is less than the modulation signal amplitude.
[00:34:45:239 - 00:34:46:708] **Speaker 0:** We have the opposite state.
[00:34:48:439 - 00:34:51:158] **Speaker 0:** Right, so whenever V control is less than V try,
[00:34:51:679 - 00:34:55:300] **Speaker 0:** T minus is on and T+ is off.
[00:34:55:959 - 00:34:58:679] **Speaker 0:** So we are connecting the load to minus VD over
[00:34:58:679 - 00:34:58:919] **Speaker 0:** 2.
[00:35:01:739 - 00:35:06:389] **Speaker 0:** But notice how as the control signal rises and then
[00:35:06:389 - 00:35:09:689] **Speaker 0:** falls, as it rises, the width.
[00:35:11:120 - 00:35:15:209] **Speaker 0:** Of the pulse for VD over 2 is larger, and
[00:35:15:209 - 00:35:17:330] **Speaker 0:** the width of the pulse for minus vd over 2
[00:35:17:330 - 00:35:20:459] **Speaker 0:** is narrower, as the amplitude goes higher.
[00:35:20:969 - 00:35:24:050] **Speaker 0:** Then, as the amplitude comes down and goes negative, we
[00:35:24:050 - 00:35:26:550] **Speaker 0:** see the opposite effect with minus VD over 2.
[00:35:26:889 - 00:35:29:689] **Speaker 0:** As it becomes more negative, minus VD over 2 pulse
[00:35:29:689 - 00:35:33:989] **Speaker 0:** witz increases, the VD over 2 pulse witz decreases.
[00:35:36:669 - 00:35:40:639] **Speaker 0:** So you're left with after this pulse modulation, a cycle
[00:35:40:639 - 00:35:45:080] **Speaker 0:** by cycle changing pulse width of your VDC and minus
[00:35:45:080 - 00:35:45:919] **Speaker 0:** VDC over 2.
[00:35:48:350 - 00:35:51:949] **Speaker 0:** It's still a, a DC waveform that's chopping between two
[00:35:51:949 - 00:35:54:989] **Speaker 0:** states, VD and minus VD VD over 2 minus VD
[00:35:54:989 - 00:35:55:629] **Speaker 0:** over 2.
[00:35:57:350 - 00:35:58:550] **Speaker 0:** that's not the waveform we want.
[00:35:58:590 - 00:36:00:929] **Speaker 0:** We want this wave form out.
[00:36:02:310 - 00:36:03:179] **Speaker 0:** So what do we do?
[00:36:04:090 - 00:36:06:429] **Speaker 0:** We just low pass philtre.
[00:36:07:239 - 00:36:08:500] **Speaker 0:** This wave form.
[00:36:09:629 - 00:36:12:159] **Speaker 0:** If we throw that through a low-pass philtre, what we
[00:36:12:159 - 00:36:15:679] **Speaker 0:** are doing is we are taking all of the of
[00:36:15:679 - 00:36:20:080] **Speaker 0:** the separate frequencies that the Fourier series for that wave
[00:36:20:080 - 00:36:23:560] **Speaker 0:** form would be, and we're just filtering out everything that's
[00:36:23:560 - 00:36:25:580] **Speaker 0:** higher than the fundamental frequency.
[00:36:27:199 - 00:36:29:219] **Speaker 0:** Alright, so we low pass philtre.
[00:36:42:709 - 00:36:45:800] **Speaker 0:** To leave just the fundamental, and the fundamental is the
[00:36:45:800 - 00:36:48:110] **Speaker 0:** wave form that we want to reproduce.
[00:36:48:679 - 00:36:50:239] **Speaker 0:** That is the control signal.
[00:36:54:570 - 00:36:58:639] **Speaker 0:** By the way, this VD over 2, minus VD over
[00:36:58:639 - 00:37:01:399] **Speaker 0:** 2, or if we got a full bridge, VD minus
[00:37:01:399 - 00:37:03:800] **Speaker 0:** VD is known as bipolar switching.
[00:37:17:959 - 00:37:20:719] **Speaker 0:** We will be, again in the next lecture, we'll be
[00:37:20:719 - 00:37:23:719] **Speaker 0:** looking at an alternative switching technique known as unipolar switching.
[00:37:24:689 - 00:37:26:360] **Speaker 0:** Which has certain advantages.
[00:37:29:379 - 00:37:32:729] **Speaker 0:** Um OK, so that's the output.
[00:37:33:090 - 00:37:35:070] **Speaker 0:** On the input we have a DC supply.
[00:37:36:159 - 00:37:36:600] **Speaker 0:** Alright.
[00:37:37:570 - 00:37:42:770] **Speaker 0:** It experiences pulsed, because we've got pulsed outputs, it experiences
[00:37:42:770 - 00:37:43:810] **Speaker 0:** pulsed currents.
[00:37:45:790 - 00:37:47:110] **Speaker 0:** I'm not gonna spend much time on this.
[00:37:47:149 - 00:37:51:629] **Speaker 0:** I just want to show, uh, to highlight, uh, the
[00:37:51:629 - 00:37:55:090] **Speaker 0:** effect of this pulse which modulated signal at the output
[00:37:55:629 - 00:37:57:750] **Speaker 0:** as to what the current looks like on the input.
[00:37:58:899 - 00:38:03:040] **Speaker 0:** This is also assuming we have a phase shifted.
[00:38:04:199 - 00:38:06:850] **Speaker 0:** Um, current and voltage at the load.
[00:38:07:360 - 00:38:10:120] **Speaker 0:** So we've got a a certain phase difference for the
[00:38:10:120 - 00:38:10:560] **Speaker 0:** current.
[00:38:11:750 - 00:38:13:219] **Speaker 0:** Again, it's inductive.
[00:38:16:699 - 00:38:20:810] **Speaker 0:** Uh, we see that as the pulse wits increased to
[00:38:20:810 - 00:38:24:270] **Speaker 0:** be of BD over 2, the pulse widths for the
[00:38:24:270 - 00:38:27:550] **Speaker 0:** current are also increasing, and we have, we have negative
[00:38:27:550 - 00:38:27:909] **Speaker 0:** current.
[00:38:28:179 - 00:38:30:409] **Speaker 0:** This is current flowing back into the supply.
[00:38:31:629 - 00:38:34:560] **Speaker 0:** But those are narrowing as the, the pulse width increases,
[00:38:34:639 - 00:38:35:800] **Speaker 0:** but with a phase shift.
[00:38:37:469 - 00:38:40:570] **Speaker 0:** And then as that drops down and goes negative, that.
[00:38:41:870 - 00:38:45:689] **Speaker 0:** The negative pulses of current don't go more negative.
[00:38:46:270 - 00:38:48:659] **Speaker 0:** It goes, it's like it's been almost like four wave
[00:38:48:659 - 00:38:50:030] **Speaker 0:** rectified in that respect.
[00:38:50:110 - 00:38:55:129] **Speaker 0:** It goes back to being larger pulse widths at, at
[00:38:55:129 - 00:38:56:530] **Speaker 0:** the, at the positive side.
[00:38:57:110 - 00:38:57:709] **Speaker 0:** Why?
[00:38:57:949 - 00:39:01:889] **Speaker 0:** It's because we are imparting power or energy to the
[00:39:01:889 - 00:39:02:439] **Speaker 0:** load.
[00:39:03:969 - 00:39:05:939] **Speaker 0:** Alright, so this is ID.
[00:39:06:280 - 00:39:08:629] **Speaker 0:** We've got an average current, so we would have VD
[00:39:09:110 - 00:39:09:949] **Speaker 0:** ID.
[00:39:11:810 - 00:39:15:830] **Speaker 0:** The average currents are going to equal the out.
[00:39:17:139 - 00:39:20:159] **Speaker 0:** RMS times I out.
[00:39:21:389 - 00:39:23:530] **Speaker 0:** RMS times.
[00:39:24:340 - 00:39:26:260] **Speaker 0:** The co-sign of the phasing.
[00:39:28:629 - 00:39:30:040] **Speaker 0:** So it's the power factor.
[00:39:35:219 - 00:39:37:000] **Speaker 0:** Alright, so those those balance up.
[00:39:43:149 - 00:39:46:340] **Speaker 0:** Why, why does it seem to be just kind of
[00:39:46:340 - 00:39:49:600] **Speaker 0:** almost rectifying this to be wider, because of the combination
[00:39:49:600 - 00:39:53:439] **Speaker 0:** of, of T plus and minus that you're activating as
[00:39:53:439 - 00:39:56:100] **Speaker 0:** to whether, which side of the, the, um, the current
[00:39:56:100 - 00:39:57:560] **Speaker 0:** of the load is being connected.
[00:39:58:899 - 00:40:01:629] **Speaker 0:** Alright, like I said, I just wanted to highlight that
[00:40:01:629 - 00:40:03:750] **Speaker 0:** this is the sort of currency that you can see
[00:40:03:750 - 00:40:05:129] **Speaker 0:** at the at the source side.
[00:40:11:360 - 00:40:14:149] **Speaker 0:** Right, so we've looked at a couple of circuits, the
[00:40:14:149 - 00:40:18:239] **Speaker 0:** half bridge and the full bridge, that can produce an
[00:40:18:239 - 00:40:20:560] **Speaker 0:** AC output waveform.
[00:40:22:870 - 00:40:26:179] **Speaker 0:** Um, we have a control wave form, and we have
[00:40:26:179 - 00:40:27:500] **Speaker 0:** the modulation wave form.
[00:40:30:840 - 00:40:35:909] **Speaker 0:** There are techniques and methods that we can employ that
[00:40:35:909 - 00:40:39:750] **Speaker 0:** mean we are able to deal with a lot of
[00:40:39:750 - 00:40:41:370] **Speaker 0:** the harmonic content.
[00:40:42:179 - 00:40:43:669] **Speaker 0:** Remember I said you need to low pass philtre to
[00:40:43:669 - 00:40:45:120] **Speaker 0:** get rid of all those harmonics.
[00:40:45:590 - 00:40:47:750] **Speaker 0:** You can get rid of a lot of that harmonic
[00:40:47:750 - 00:40:53:129] **Speaker 0:** content if we get the right combinations between the amplitude
[00:40:53:629 - 00:40:57:889] **Speaker 0:** of the control and the modulating signals and the frequency.
[00:40:58:360 - 00:41:02:530] **Speaker 0:** Between the uh modulating signal and the control signal.
[00:41:03:389 - 00:41:05:449] **Speaker 0:** So we need to make some definitions before we start
[00:41:05:449 - 00:41:06:350] **Speaker 0:** analysing that.
[00:41:07:330 - 00:41:08:010] **Speaker 0:** Some definitions.
[00:41:08:129 - 00:41:11:100] **Speaker 0:** First up, the amplitude modulation ratio MA.
[00:41:13:620 - 00:41:16:620] **Speaker 0:** So it's just a ratio, and we take that the
[00:41:16:620 - 00:41:21:820] **Speaker 0:** amplitude modulation ratio is just the uh the maximum reference
[00:41:21:820 - 00:41:27:239] **Speaker 0:** voltage, that's the peak divided by the maximum modulation voltage.
[00:41:29:870 - 00:41:35:479] **Speaker 0:** So if our Reference or control signal amplitude is less
[00:41:35:479 - 00:41:42:699] **Speaker 0:** than the the uh modulation amplitude, then The frequency component
[00:41:42:699 - 00:41:46:459] **Speaker 0:** of the output voltage is directly proportional to that ratio.
[00:41:48:010 - 00:41:48:770] **Speaker 0:** What does it mean?
[00:41:48:840 - 00:41:51:649] **Speaker 0:** It means that it's possible to linearly control the output
[00:41:51:649 - 00:41:56:129] **Speaker 0:** voltage through a linear change in the amplitude of the
[00:41:56:129 - 00:41:56:850] **Speaker 0:** control wave form.
[00:41:57:530 - 00:42:00:330] **Speaker 0:** So if we double the amplitude of the control waveform,
[00:42:00:610 - 00:42:03:320] **Speaker 0:** we'll double the amplitude of the output signal, the one
[00:42:03:320 - 00:42:05:889] **Speaker 0:** that we're trying to create from the um inverter.
[00:42:08:040 - 00:42:10:100] **Speaker 0:** It's a little bit of a fudge, we could change
[00:42:10:100 - 00:42:13:379] **Speaker 0:** the amplitude of the modulation signal.
[00:42:13:919 - 00:42:15:840] **Speaker 0:** We don't normally do that, it's, it's fixed.
[00:42:15:959 - 00:42:18:719] **Speaker 0:** We, we change the amplitude of our controls, it's the
[00:42:18:719 - 00:42:19:419] **Speaker 0:** control signal.
[00:42:21:370 - 00:42:25:939] **Speaker 0:** So long as the amplitude modulation ratio stays less than
[00:42:25:939 - 00:42:26:479] **Speaker 0:** unity.
[00:42:27:790 - 00:42:33:870] **Speaker 0:** If You have a control signal that exceeds the amplitude
[00:42:33:870 - 00:42:39:270] **Speaker 0:** of our uh modulation signal, uh, that generates a state
[00:42:39:270 - 00:42:40:790] **Speaker 0:** known as over-modulation.
[00:42:42:870 - 00:42:46:090] **Speaker 0:** And the effect is that we start squaring off.
[00:42:46:969 - 00:42:47:770] **Speaker 0:** The wave form.
[00:42:50:110 - 00:42:53:399] **Speaker 0:** So if we end up with an amplitude modulation ratio
[00:42:53:399 - 00:42:58:610] **Speaker 0:** greater than around 3.3, the switching scheme effectively becomes modified
[00:42:58:610 - 00:42:59:389] **Speaker 0:** sinusoid.
[00:43:00:760 - 00:43:06:379] **Speaker 0:** All right, so you end up with Uh, A little
[00:43:06:379 - 00:43:07:719] **Speaker 0:** bit of 0.
[00:43:08:429 - 00:43:11:870] **Speaker 0:** All DC one way and then all DC the other
[00:43:11:870 - 00:43:12:129] **Speaker 0:** way.
[00:43:15:179 - 00:43:18:560] **Speaker 0:** So that would be greater than 3.3.
[00:43:22:139 - 00:43:23:129] **Speaker 0:** We don't want that.
[00:43:23:500 - 00:43:24:899] **Speaker 0:** It's not a good situation.
[00:43:25:090 - 00:43:27:939] **Speaker 0:** We're not reducing the harmonics by any, we're increasing the
[00:43:27:939 - 00:43:29:810] **Speaker 0:** harmonics by doing that, right?
[00:43:29:860 - 00:43:32:100] **Speaker 0:** So, exactly the opposite job of what we're trying to
[00:43:32:100 - 00:43:32:379] **Speaker 0:** do.
[00:43:32:699 - 00:43:37:860] **Speaker 0:** So we always, uh, attempt to make sure, nearly always
[00:43:37:860 - 00:43:39:500] **Speaker 0:** attempt to make, I'll give you an example where we
[00:43:39:500 - 00:43:42:300] **Speaker 0:** don't, um, we nearly always attempt to make sure that
[00:43:42:300 - 00:43:47:290] **Speaker 0:** the control signal amplitude is less than the, um, modulation
[00:43:47:290 - 00:43:48:100] **Speaker 0:** signal amplitude.
[00:43:51:949 - 00:43:56:250] **Speaker 0:** Right Then a second definition.
[00:44:01:169 - 00:44:03:030] **Speaker 0:** The frequency modulation ratio.
[00:44:04:239 - 00:44:07:439] **Speaker 0:** In Savi Again, it's just another ratio.
[00:44:07:840 - 00:44:11:239] **Speaker 0:** So we take the frequency of our triangle wave, this
[00:44:11:239 - 00:44:12:659] **Speaker 0:** is the switching frequency.
[00:44:15:860 - 00:44:17:969] **Speaker 0:** Uh, and divide it by the frequency of the reference
[00:44:17:969 - 00:44:19:520] **Speaker 0:** signal, you control.
[00:44:23:600 - 00:44:27:840] **Speaker 0:** The higher the switching frequency is, then that results in
[00:44:27:840 - 00:44:29:479] **Speaker 0:** higher harmonic frequencies.
[00:44:31:979 - 00:44:35:340] **Speaker 0:** And because those frequencies are so much higher than the
[00:44:35:340 - 00:44:39:340] **Speaker 0:** fundamental, it becomes a lot easier to low pass philtre
[00:44:39:340 - 00:44:41:699] **Speaker 0:** those out, leaving just the fundamental.
[00:44:43:439 - 00:44:45:139] **Speaker 0:** All right, so it becomes easier.
[00:44:47:330 - 00:44:50:719] **Speaker 0:** And we can get away with smaller philtre components, uh,
[00:44:50:729 - 00:44:51:370] **Speaker 0:** lower cost.
[00:44:51:750 - 00:44:54:770] **Speaker 0:** However, there's a bit of a trade-off, um, higher switching
[00:44:54:770 - 00:44:58:790] **Speaker 0:** frequencies mean that we start to increase those switching losses.
[00:45:01:810 - 00:45:05:040] **Speaker 0:** Alright, so We have those two definitions, just a couple
[00:45:05:040 - 00:45:06:969] **Speaker 0:** of notes for the switches themselves.
[00:45:07:320 - 00:45:10:080] **Speaker 0:** If the load is inductive, we must make sure that
[00:45:10:080 - 00:45:13:300] **Speaker 0:** we have free-wheeling diodes across the switches to enable that
[00:45:13:300 - 00:45:14:459] **Speaker 0:** 4 quadrant operation.
[00:45:15:389 - 00:45:18:830] **Speaker 0:** And then if we were looking at really high frequency
[00:45:18:830 - 00:45:22:830] **Speaker 0:** switching into the megahertz type, uh, space, then we must
[00:45:22:830 - 00:45:27:510] **Speaker 0:** start considering that finite, um, transition of the, um, the
[00:45:27:510 - 00:45:33:419] **Speaker 0:** switching of those, those, uh, Switching states because they can
[00:45:33:419 - 00:45:37:679] **Speaker 0:** in that uh situation start introducing things to do with
[00:45:38:250 - 00:45:40:560] **Speaker 0:** shoot through currents and not being able to switch them
[00:45:40:560 - 00:45:43:060] **Speaker 0:** off in time for the next switch coming on even
[00:45:43:060 - 00:45:44:399] **Speaker 0:** with some dead time control.
[00:45:44:850 - 00:45:46:909] **Speaker 0:** So yeah, we've got to watch out for that.
[00:45:47:179 - 00:45:50:620] **Speaker 0:** And for our reference and modulation signals.
[00:45:52:010 - 00:45:57:139] **Speaker 0:** Unlike the output that we're supplying to the load, those
[00:45:57:139 - 00:46:01:060] **Speaker 0:** signals are very, very low power, usually generated through some
[00:46:01:060 - 00:46:02:540] **Speaker 0:** sort of microelectronic method.
[00:46:03:600 - 00:46:06:919] **Speaker 0:** OK, so, for example, self-starting oscillators.
[00:46:08:290 - 00:46:10:169] **Speaker 0:** you're gonna, uh, see a little bit about that later
[00:46:10:169 - 00:46:13:530] **Speaker 0:** on in the course, but, um, they can be generated
[00:46:13:530 - 00:46:16:129] **Speaker 0:** just from op amp, little op amp circuits and so
[00:46:16:129 - 00:46:18:409] **Speaker 0:** forth, so they don't, they're not very much power at
[00:46:18:409 - 00:46:18:419] **Speaker 0:** all.
[00:46:19:879 - 00:46:24:850] **Speaker 0:** Um, you can also rather than self-starting oscillators, you could
[00:46:24:850 - 00:46:26:489] **Speaker 0:** have sampling the mains.
[00:46:31:489 - 00:46:33:850] **Speaker 0:** That's the sort of thing that you might do for
[00:46:33:850 - 00:46:38:750] **Speaker 0:** a um a grid connected um photovoltaic inverter.
[00:46:39:510 - 00:46:42:689] **Speaker 0:** Um, they also tend to use things known as, um,
[00:46:43:340 - 00:46:44:469] **Speaker 0:** phase locked loops.
[00:46:46:060 - 00:46:48:500] **Speaker 0:** Right, which makes it so you don't drift away from
[00:46:48:500 - 00:46:51:209] **Speaker 0:** that frequency that's, uh, that's coming from mains.
[00:46:51:719 - 00:46:53:879] **Speaker 0:** Uh, but it also could be um an audio signal.
[00:46:55:030 - 00:46:56:639] **Speaker 0:** A low power audio signal.
[00:46:58:659 - 00:47:02:500] **Speaker 0:** That we are then using the inverter to produce our
[00:47:02:500 - 00:47:05:300] **Speaker 0:** high power output that could be driving loudspeakers or something.
[00:47:08:239 - 00:47:12:120] **Speaker 0:** And that's also how our modulation signal can be generated,
[00:47:12:229 - 00:47:14:679] **Speaker 0:** usually through some sort of self-starting oscillator.
[00:47:16:229 - 00:47:16:429] **Speaker 0:** Right.
[00:47:17:149 - 00:47:19:810] **Speaker 0:** And that's the oscillator part that you have in your
[00:47:19:810 - 00:47:20:820] **Speaker 0:** TL-494 chip.
[00:47:23:239 - 00:47:24:219] **Speaker 0:** Right, that's it for today.
[00:47:24:560 - 00:47:28:040] **Speaker 0:** Uh, last lecture of the week, we'll just uh go
[00:47:28:040 - 00:47:31:919] **Speaker 0:** on and have a look at uh optimising the those
[00:47:31:919 - 00:47:33:120] **Speaker 0:** uh ratios.

# ENEL372-26S2 Lecture 17 native Echo transcript

Date: August 20, 2026 3:00pm-3:55pm
Transcript type: native Echo automated transcript.

[00:00:00:050 - 00:00:03:099] **Speaker 0:** Right, Kyorakoto, welcome along.
[00:00:03:450 - 00:00:05:500] **Speaker 0:** This looks like it's gonna be us for today.
[00:00:08:130 - 00:00:12:460] **Speaker 0:** Alright, just, just a reminder, this is the last lecture
[00:00:12:460 - 00:00:16:950] **Speaker 0:** for 372 for this term, so they don't start again
[00:00:16:950 - 00:00:18:889] **Speaker 0:** until clearly next term.
[00:00:19:489 - 00:00:20:010] **Speaker 0:** Alright.
[00:00:20:860 - 00:00:26:340] **Speaker 0:** Um, OK, so we've been learning about, um, inverters, so
[00:00:26:340 - 00:00:30:420] **Speaker 0:** that's conversion of DC to AC, a very, very important
[00:00:30:420 - 00:00:33:000] **Speaker 0:** function to carry out for our power electronics.
[00:00:33:299 - 00:00:36:049] **Speaker 0:** Um, and the way that we've looked at how that's
[00:00:36:049 - 00:00:39:470] **Speaker 0:** implemented is via pulse width modulation or PWM.
[00:00:40:709 - 00:00:44:229] **Speaker 0:** And we saw that if we use PWM that results
[00:00:44:229 - 00:00:48:330] **Speaker 0:** in a variable pulse width wave form that we need
[00:00:48:330 - 00:00:54:830] **Speaker 0:** to low pass philtre to output the desired AC signal
[00:00:54:830 - 00:00:56:450] **Speaker 0:** or AC waveform to the load.
[00:00:58:770 - 00:01:03:540] **Speaker 0:** Um, in order to look at keeping our philtre component
[00:01:03:540 - 00:01:08:209] **Speaker 0:** size as small as we can get, um, we need
[00:01:08:209 - 00:01:11:290] **Speaker 0:** to have a look at what are the harmonics that
[00:01:11:290 - 00:01:15:610] **Speaker 0:** are generated when we do our pulsive modulation, um, and
[00:01:15:610 - 00:01:18:690] **Speaker 0:** from that knowledge about the harmonics, we might be able
[00:01:18:690 - 00:01:22:410] **Speaker 0:** to do something about those and therefore, the size of
[00:01:22:410 - 00:01:24:010] **Speaker 0:** the philtre requirements required.
[00:01:25:339 - 00:01:28:419] **Speaker 0:** Right, so, we did some definitions, um, in the last
[00:01:28:419 - 00:01:34:010] **Speaker 0:** lecture for our, uh, modulation frequency ratio and amplitude, um,
[00:01:34:019 - 00:01:36:129] **Speaker 0:** modulation, uh, ratio.
[00:01:36:459 - 00:01:43:120] **Speaker 0:** So, utilising, especially that, that modulation, um, Frequency modulation ratio,
[00:01:43:410 - 00:01:48:069] **Speaker 0:** we can identify the harmonics that are generated from the
[00:01:48:510 - 00:01:51:529] **Speaker 0:** bipolar switching technique that we talked about.
[00:01:51:620 - 00:01:54:889] **Speaker 0:** That's going, switching from BDC over 2, all the way
[00:01:54:889 - 00:01:57:569] **Speaker 0:** down to minus BDC over 2 in one transition.
[00:01:59:970 - 00:02:01:739] **Speaker 0:** Right, um, so.
[00:02:02:440 - 00:02:05:639] **Speaker 0:** If you look at that particular wave form and have
[00:02:05:639 - 00:02:08:880] **Speaker 0:** a look at the Fourier series that's, that's created from
[00:02:08:880 - 00:02:12:119] **Speaker 0:** that uh wave, that wave form, then you end up
[00:02:12:119 - 00:02:15:320] **Speaker 0:** seeing that the harmonics that are associated with the, with
[00:02:15:320 - 00:02:19:720] **Speaker 0:** the fundamental are equal to just this simple expression.
[00:02:20:710 - 00:02:24:199] **Speaker 0:** Alright, so what it means is that there are K
[00:02:24:199 - 00:02:28:720] **Speaker 0:** side bands associated with J times the modulation frequency.
[00:02:29:720 - 00:02:32:550] **Speaker 0:** J times the ratio here, but if you multiply it
[00:02:32:550 - 00:02:35:559] **Speaker 0:** by the reference signal, you're just left with the modulation
[00:02:35:559 - 00:02:36:160] **Speaker 0:** frequency.
[00:02:38:009 - 00:02:43:529] **Speaker 0:** Um, now, since that switching that we've got causes rectangular
[00:02:43:529 - 00:02:46:690] **Speaker 0:** waveforms, remember this is the pulse width modulation signal that
[00:02:46:690 - 00:02:49:169] **Speaker 0:** we're looking at here, which is just a series of
[00:02:49:169 - 00:02:52:009] **Speaker 0:** rectangular waveforms with variable widths.
[00:02:52:990 - 00:02:53:000] **Speaker 0:** Right.
[00:02:54:149 - 00:03:00:550] **Speaker 0:** Because of that rectangular waveform shape, immediately, the um harmonics
[00:03:00:550 - 00:03:02:610] **Speaker 0:** are frequency restricted.
[00:03:04:139 - 00:03:09:110] **Speaker 0:** OK, they only occur at specific uh harmonic frequencies.
[00:03:09:460 - 00:03:13:070] **Speaker 0:** Um, that, and we have that the sum of J
[00:03:13:070 - 00:03:15:990] **Speaker 0:** plus or minus K has to be odd.
[00:03:17:410 - 00:03:20:289] **Speaker 0:** For that Fourier series of those rectangular waveforms at a
[00:03:20:289 - 00:03:21:210] **Speaker 0:** fixed frequency.
[00:03:22:089 - 00:03:27:190] **Speaker 0:** Right, so, What we find is that it's possible to
[00:03:27:190 - 00:03:31:750] **Speaker 0:** actually eliminate some of those bipolar switching harmonics by choosing
[00:03:31:750 - 00:03:38:330] **Speaker 0:** our modulation, our frequency modulation ratio to be an odd
[00:03:38:330 - 00:03:39:130] **Speaker 0:** integer.
[00:03:41:059 - 00:03:44:179] **Speaker 0:** Right, so if we do that, if we make MF
[00:03:44:179 - 00:03:48:520] **Speaker 0:** an odd integer that results in only odd harmonics of
[00:03:48:520 - 00:03:49:679] **Speaker 0:** that ratio.
[00:03:50:419 - 00:03:53:259] **Speaker 0:** And the cosine coefficients, so that you've got your sine
[00:03:53:259 - 00:03:56:259] **Speaker 0:** coefficients and your cosign coefficients for your, for your series.
[00:03:56:740 - 00:03:59:279] **Speaker 0:** The cosine coefficients are all zero.
[00:04:01:679 - 00:04:03:940] **Speaker 0:** So it's a massive reduction in the number of uh
[00:04:03:940 - 00:04:08:050] **Speaker 0:** frequencies that we might uh occur from our um wave
[00:04:08:050 - 00:04:08:250] **Speaker 0:** form.
[00:04:10:179 - 00:04:12:570] **Speaker 0:** That's all well and good to state in text, right?
[00:04:12:699 - 00:04:15:619] **Speaker 0:** But what does, what does it look like in actual
[00:04:15:619 - 00:04:17:450] **Speaker 0:** reality for our harmonics?
[00:04:17:700 - 00:04:19:519] **Speaker 0:** Well, that's what the next plot shows us.
[00:04:27:040 - 00:04:30:279] **Speaker 0:** So this is just an example where our um amplitude
[00:04:30:279 - 00:04:33:700] **Speaker 0:** modulation ratio is 0.8, so we're in the linear zone,
[00:04:34:279 - 00:04:34:720] **Speaker 0:** um.
[00:04:35:500 - 00:04:39:700] **Speaker 0:** And we've got on the vertical axis, we've got um
[00:04:39:700 - 00:04:45:579] **Speaker 0:** the harmonic amplitude with respect to normalised to VD over
[00:04:45:579 - 00:04:45:890] **Speaker 0:** 2.
[00:04:46:649 - 00:04:49:500] **Speaker 0:** So we're looking at a half bridge, OK, and normalising
[00:04:49:500 - 00:04:50:220] **Speaker 0:** to VD over 2.
[00:04:50:299 - 00:04:53:609] **Speaker 0:** So 1, the value of 1 would be that the
[00:04:53:609 - 00:04:58:489] **Speaker 0:** peak of our um AC wave form, our control signal,
[00:04:58:859 - 00:05:03:290] **Speaker 0:** is exactly equal to the peak of our um control,
[00:05:03:299 - 00:05:04:700] **Speaker 0:** uh, of our reference.
[00:05:05:980 - 00:05:08:890] **Speaker 0:** Of our modulation signal, the triangular wave.
[00:05:12:190 - 00:05:16:549] **Speaker 0:** OK, so, here we've got MA 0.8, and we can
[00:05:16:549 - 00:05:18:790] **Speaker 0:** actually tell that it's 0.8 by just looking at the
[00:05:18:790 - 00:05:19:489] **Speaker 0:** fundamental.
[00:05:19:950 - 00:05:21:809] **Speaker 0:** So that's what this is, this is the fundamental.
[00:05:26:880 - 00:05:29:339] **Speaker 0:** Um, and see that it's amplitude is 0.8.
[00:05:29:589 - 00:05:32:559] **Speaker 0:** It's in the linear zone, so it's just the amplitude
[00:05:32:559 - 00:05:37:320] **Speaker 0:** of our, um, uh, of our control or reference signal
[00:05:37:320 - 00:05:40:540] **Speaker 0:** times the amplitude modulation ratio.
[00:05:42:260 - 00:05:42:269] **Speaker 0:** OK.
[00:05:44:440 - 00:05:47:230] **Speaker 0:** Uh, and we've got, uh, a frequency modulation ratio of
[00:05:47:230 - 00:05:47:760] **Speaker 0:** 15.
[00:05:48:760 - 00:05:50:309] **Speaker 0:** So our triangle wave.
[00:05:51:130 - 00:05:53:839] **Speaker 0:** The thing that we're comparing against to produce our PWM
[00:05:53:839 - 00:05:59:320] **Speaker 0:** is 15 times the frequency of our control signal, the,
[00:05:59:540 - 00:06:03:420] **Speaker 0:** the slow changing, usually sinusoidal wave form that we're trying
[00:06:03:420 - 00:06:04:500] **Speaker 0:** to produce at the output.
[00:06:07:119 - 00:06:10:059] **Speaker 0:** Right, so We can see.
[00:06:11:119 - 00:06:14:239] **Speaker 0:** That there are, from the fundamental, there are no other
[00:06:14:239 - 00:06:19:079] **Speaker 0:** frequencies until we hit around about the uh the frequency
[00:06:19:079 - 00:06:25:059] **Speaker 0:** modulation ratio value, times that um Uh, frequency.
[00:06:25:299 - 00:06:30:980] **Speaker 0:** So, We've got MF is 1, or MF here is
[00:06:30:980 - 00:06:34:579] **Speaker 0:** 1, so J is equal to 1 from the previous
[00:06:34:579 - 00:06:37:079] **Speaker 0:** expression where K is equal to 0.
[00:06:38:149 - 00:06:38:899] **Speaker 0:** So that's odd.
[00:06:40:369 - 00:06:42:769] **Speaker 0:** So J plus or minus K has to be odd,
[00:06:42:890 - 00:06:45:570] **Speaker 0:** it's odd, so here we can see our harmonica is
[00:06:45:570 - 00:06:46:809] **Speaker 0:** actually existing.
[00:06:47:459 - 00:06:49:720] **Speaker 0:** And it actually has an amplitude.
[00:06:50:929 - 00:06:53:410] **Speaker 0:** Which we'll see the actual values in a in a
[00:06:53:410 - 00:06:54:119] **Speaker 0:** later slide.
[00:06:54:290 - 00:06:56:230] **Speaker 0:** It's actually greater than the fundamental.
[00:06:58:029 - 00:07:00:510] **Speaker 0:** OK, um, and it has side bands.
[00:07:01:290 - 00:07:05:450] **Speaker 0:** So that's the plus and minus J, um OK, side
[00:07:05:450 - 00:07:06:559] **Speaker 0:** bands for this.
[00:07:06:850 - 00:07:10:369] **Speaker 0:** So here's MF + 2, so 1 + 2, that's
[00:07:10:369 - 00:07:12:170] **Speaker 0:** 3, and minus 2.
[00:07:17:519 - 00:07:19:809] **Speaker 0:** Uh, and then you jump up to the next.
[00:07:20:519 - 00:07:25:880] **Speaker 0:** A band which centres around 2 times the frequency modulation
[00:07:25:880 - 00:07:26:459] **Speaker 0:** ratio.
[00:07:27:459 - 00:07:31:140] **Speaker 0:** But since uh we've got 2 MF, that means J
[00:07:31:140 - 00:07:35:059] **Speaker 0:** is equal to 2, we can't have um any uh
[00:07:35:059 - 00:07:38:559] **Speaker 0:** component or harmonic at that frequency, because that's even.
[00:07:40:239 - 00:07:44:399] **Speaker 0:** Right, so the Fourier analysis just simply falls out that
[00:07:44:399 - 00:07:48:380] **Speaker 0:** these are the values of the harmonics with the weightings
[00:07:48:679 - 00:07:51:760] **Speaker 0:** associated with that, all those frequencies.
[00:07:54:679 - 00:07:55:109] **Speaker 0:** OK.
[00:07:55:450 - 00:07:57:890] **Speaker 0:** So that's, that's what that expression turns out to be
[00:07:57:890 - 00:07:58:079] **Speaker 0:** like.
[00:07:58:170 - 00:08:04:399] **Speaker 0:** If, if we make The switching frequency or our modulation
[00:08:04:399 - 00:08:11:399] **Speaker 0:** frequency, an integer number of the fundamental of our sinusoid.
[00:08:12:929 - 00:08:13:859] **Speaker 0:** A control signal.
[00:08:15:040 - 00:08:19:059] **Speaker 0:** That immediately tells us something about the two signals.
[00:08:19:329 - 00:08:23:339] **Speaker 0:** If they, if, if it's an integer, odd integer, it
[00:08:23:339 - 00:08:26:920] **Speaker 0:** doesn't matter, if it's an integer, then those two signals
[00:08:26:920 - 00:08:29:700] **Speaker 0:** have to be synchronous, alright.
[00:08:33:679 - 00:08:36:619] **Speaker 0:** Right, so the fact that they are are integer.
[00:08:40:129 - 00:08:51:900] **Speaker 0:** Means that our um control or reference I synchronous.
[00:09:06:820 - 00:09:10:219] **Speaker 0:** Right, with the modulation signal, they don't drift in time,
[00:09:10:419 - 00:09:11:380] **Speaker 0:** they are locked in.
[00:09:14:219 - 00:09:18:460] **Speaker 0:** Right, let's say though that maybe the, the frequency modulation
[00:09:18:460 - 00:09:20:520] **Speaker 0:** ratio is an even integer.
[00:09:21:929 - 00:09:24:229] **Speaker 0:** Or not an inch at all.
[00:09:25:369 - 00:09:28:090] **Speaker 0:** Um, if it's not an integer, you, you, you carry
[00:09:28:090 - 00:09:30:880] **Speaker 0:** a signal that's asynchronous with the reference signal.
[00:09:31:380 - 00:09:34:179] **Speaker 0:** Um, we're going to get subharmonics.
[00:09:35:239 - 00:09:40:059] **Speaker 0:** Um, and those harmonics can be close to zero frequency,
[00:09:40:840 - 00:09:43:320] **Speaker 0:** or at least hang around the same sort of frequency
[00:09:43:320 - 00:09:44:380] **Speaker 0:** as our fundamental.
[00:09:46:169 - 00:09:51:109] **Speaker 0:** Um, that can be very problematic with regards to efficiency,
[00:09:51:650 - 00:09:55:210] **Speaker 0:** uh, and magnetic material saturation, especially if the frequencies are
[00:09:55:210 - 00:09:56:650] **Speaker 0:** getting close to DC.
[00:09:57:090 - 00:10:01:130] **Speaker 0:** Remember, with our magnetic materials, they don't like having constant
[00:10:01:130 - 00:10:04:559] **Speaker 0:** amounts of flux, especially if it's on a cycle by
[00:10:04:559 - 00:10:08:130] **Speaker 0:** cycle basis for the, um, for the, for the actual
[00:10:08:130 - 00:10:11:570] **Speaker 0:** frequency that we're trying to, um, produce, um, if there's
[00:10:11:570 - 00:10:13:770] **Speaker 0:** residual flux, it'll just step up and up and up
[00:10:13:770 - 00:10:15:450] **Speaker 0:** until you get saturation occurring.
[00:10:18:869 - 00:10:23:710] **Speaker 0:** Um, that being said, if you've got the situation where
[00:10:23:710 - 00:10:27:109] **Speaker 0:** you don't have MF isn't an integer or maybe even
[00:10:27:109 - 00:10:30:909] **Speaker 0:** for bipolar switching, you can reduce the chances of something
[00:10:30:909 - 00:10:36:650] **Speaker 0:** problematic occurring by choosing your, um, modulation frequency to be
[00:10:37:190 - 00:10:42:270] **Speaker 0:** really quite large compared to the reference signal frequency.
[00:10:44:289 - 00:10:50:250] **Speaker 0:** Great example is using switch mode inverters for audio applications.
[00:10:51:090 - 00:10:53:409] **Speaker 0:** Audio has frequencies that are changing all the time.
[00:10:53:530 - 00:10:57:250] **Speaker 0:** They're definitely not an integer of the, of the switching
[00:10:57:250 - 00:10:57:849] **Speaker 0:** frequency.
[00:11:00:630 - 00:11:04:270] **Speaker 0:** So, if that was the case, um, you try to
[00:11:04:270 - 00:11:09:690] **Speaker 0:** make the switching frequency greater than at least 20 times.
[00:11:10:770 - 00:11:16:469] **Speaker 0:** The signal The maximum frequency of the signal that you're
[00:11:16:469 - 00:11:18:010] **Speaker 0:** trying to produce at the output.
[00:11:24:619 - 00:11:26:159] **Speaker 0:** So for audio.
[00:11:30:570 - 00:11:34:530] **Speaker 0:** That maximum frequency is around about 20 kilohertz.
[00:11:39:799 - 00:11:42:780] **Speaker 0:** So 20 times that means that our switching frequency.
[00:11:44:179 - 00:11:46:640] **Speaker 0:** is going to want to be greater than about 400
[00:11:46:640 - 00:11:47:400] **Speaker 0:** kilohertz.
[00:11:50:349 - 00:11:54:429] **Speaker 0:** If we're going to uh utilise um a switch mode
[00:11:54:429 - 00:11:56:849] **Speaker 0:** inverter as an audio amplifier of some sort.
[00:11:58:099 - 00:12:01:859] **Speaker 0:** That's not a trivial frequency to work with if you're,
[00:12:02:059 - 00:12:05:270] **Speaker 0:** if you're looking at transferring quite significant amounts of power,
[00:12:05:700 - 00:12:07:340] **Speaker 0:** but it is doable, it is doable.
[00:12:09:260 - 00:12:13:059] **Speaker 0:** So we've Come up with a system here if we
[00:12:13:059 - 00:12:16:500] **Speaker 0:** can make uh MF an odd integer, in this case
[00:12:16:500 - 00:12:17:460] **Speaker 0:** it's 15.
[00:12:18:229 - 00:12:22:409] **Speaker 0:** Then The larger and larger MF gets, the further and
[00:12:22:409 - 00:12:25:650] **Speaker 0:** further away these harmonics are from the, from the fundamental,
[00:12:25:849 - 00:12:29:130] **Speaker 0:** and it makes it easier and easier to low pass
[00:12:29:130 - 00:12:29:669] **Speaker 0:** philtre.
[00:12:34:219 - 00:12:40:400] **Speaker 0:** Um, the fundamental from the harmonics, because the harmonic frequencies
[00:12:40:400 - 00:12:42:859] **Speaker 0:** are such a higher frequency than that fundamental.
[00:12:52:229 - 00:12:52:900] **Speaker 0:** That make sense?
[00:12:54:500 - 00:12:57:940] **Speaker 0:** So, that means that we can get away because we've
[00:12:57:940 - 00:13:02:359] **Speaker 0:** got this integer, an odd integer at that, um, Uh,
[00:13:02:609 - 00:13:07:380] **Speaker 0:** frequency modulation ratio, that we can minimise or at least
[00:13:07:380 - 00:13:11:369] **Speaker 0:** greatly reduce the values of our philtre components that are
[00:13:11:369 - 00:13:13:799] **Speaker 0:** low pass filtering that signal.
[00:13:16:750 - 00:13:18:820] **Speaker 0:** OK That's great.
[00:13:21:000 - 00:13:23:340] **Speaker 0:** Can we do better?
[00:13:24:059 - 00:13:26:679] **Speaker 0:** With our pulsive modulation technique.
[00:13:27:299 - 00:13:28:710] **Speaker 0:** Well, as it turns out, yeah, we can.
[00:13:32:760 - 00:13:37:010] **Speaker 0:** And that's to move away from bipolar switching and go
[00:13:37:010 - 00:13:38:650] **Speaker 0:** to unipolar switching.
[00:13:42:609 - 00:13:46:289] **Speaker 0:** So, unipolar switching, when you first see it, I'll just
[00:13:46:289 - 00:13:49:369] **Speaker 0:** warn you now, when you first see it, it takes
[00:13:49:369 - 00:13:51:169] **Speaker 0:** a bit to wrap your head around.
[00:13:52:090 - 00:13:56:429] **Speaker 0:** Because you are controlling a full bridge, it doesn't work
[00:13:56:429 - 00:13:57:309] **Speaker 0:** with half bridges.
[00:13:58:190 - 00:14:01:809] **Speaker 0:** You're controlling a full bridge and the upper and lower
[00:14:01:809 - 00:14:03:330] **Speaker 0:** switches of your full bridge.
[00:14:04:039 - 00:14:08:760] **Speaker 0:** As individual poles, rather than switching diagonal pair.
[00:14:12:049 - 00:14:12:650] **Speaker 0:** OK.
[00:14:13:780 - 00:14:16:869] **Speaker 0:** To do the control of each of the two poles
[00:14:16:869 - 00:14:21:390] **Speaker 0:** in our full bridge, we need 2 reference signals, not
[00:14:21:390 - 00:14:22:409] **Speaker 0:** just 1.
[00:14:24:609 - 00:14:26:969] **Speaker 0:** The, the good thing, or the easier thing about it
[00:14:26:969 - 00:14:31:489] **Speaker 0:** is that the two reference signals are absolutely linked together
[00:14:31:489 - 00:14:34:609] **Speaker 0:** as far as what shape they are and what frequency
[00:14:34:609 - 00:14:34:890] **Speaker 0:** they are.
[00:14:34:969 - 00:14:37:349] **Speaker 0:** They're just one of the inverse of the other.
[00:14:37:849 - 00:14:42:450] **Speaker 0:** So we have still a single modulating wave form, that's
[00:14:42:450 - 00:14:43:390] **Speaker 0:** a triangle wave.
[00:14:43:849 - 00:14:48:599] **Speaker 0:** But we have not just one control signal, but two,
[00:14:49:049 - 00:14:52:150] **Speaker 0:** where the other control signal is just the inverse negative
[00:14:52:150 - 00:14:54:010] **Speaker 0:** of the first control signal.
[00:14:54:090 - 00:14:56:650] **Speaker 0:** So they're very easy to generate, right, just put it
[00:14:56:650 - 00:14:59:849] **Speaker 0:** through an invert, um, a, um an amplifier which inverts
[00:14:59:849 - 00:15:00:549] **Speaker 0:** the signal.
[00:15:01:890 - 00:15:05:479] **Speaker 0:** Right, these, remember, these are control signals, they're electronic level,
[00:15:06:289 - 00:15:08:809] **Speaker 0:** it's very, very easy to like use op amps and
[00:15:08:809 - 00:15:13:150] **Speaker 0:** so forth to do inverse waveforms and you know, phase
[00:15:13:150 - 00:15:13:650] **Speaker 0:** inversion.
[00:15:16:090 - 00:15:17:349] **Speaker 0:** OK, so.
[00:15:20:590 - 00:15:24:260] **Speaker 1:** Full bridge What I'm gonna do is just show you
[00:15:24:260 - 00:15:26:440] **Speaker 0:** the full bridge that I had in the last lecture,
[00:15:26:820 - 00:15:30:419] **Speaker 0:** uh, and I'm going to label one of the nodes
[00:15:30:419 - 00:15:33:380] **Speaker 0:** there and I'm gonna call this the positive negative with
[00:15:33:380 - 00:15:38:309] **Speaker 0:** the negative side being this node being called N, N
[00:15:38:309 - 00:15:39:020] **Speaker 0:** for negative.
[00:15:39:989 - 00:15:40:000] **Speaker 0:** Right.
[00:15:41:739 - 00:15:44:020] **Speaker 0:** Just to make it consistent with what we're seeing on
[00:15:44:020 - 00:15:45:780] **Speaker 0:** this, um, this diagram.
[00:15:47:539 - 00:15:50:799] **Speaker 0:** So, this fee control is for pole A.
[00:15:53:320 - 00:15:54:380] **Speaker 0:** So that's this side.
[00:15:56:679 - 00:15:58:940] **Speaker 0:** And this control is for pole B.
[00:16:02:260 - 00:16:02:739] **Speaker 0:** So that one.
[00:16:06:450 - 00:16:11:130] **Speaker 0:** So We still have the same control logic that we've
[00:16:11:130 - 00:16:15:890] **Speaker 0:** been identified before for the bipolar um pulse modulation.
[00:16:16:570 - 00:16:20:309] **Speaker 0:** So It says for.
[00:16:21:650 - 00:16:23:330] **Speaker 0:** For pole A, let's have a look at poll A.
[00:16:23:609 - 00:16:26:789] **Speaker 0:** For B control greater than pole A, T+ is on.
[00:16:28:239 - 00:16:30:760] **Speaker 0:** So we have a look here, here we go, V
[00:16:30:760 - 00:16:34:909] **Speaker 0:** control for pole A is greater than the control for
[00:16:34:909 - 00:16:39:000] **Speaker 0:** V tri, I mean, the uh um modulation signal, which
[00:16:39:000 - 00:16:39:739] **Speaker 0:** is V tri.
[00:16:40:200 - 00:16:43:780] **Speaker 0:** So whilst we're between here and here, then we're getting
[00:16:45:200 - 00:16:46:909] **Speaker 0:** T A plus is on.
[00:16:48:059 - 00:16:53:140] **Speaker 1:** Well if TA plus is on, then node A is
[00:16:53:140 - 00:16:56:099] **Speaker 0:** at + VD with respect to N.
[00:16:57:080 - 00:16:59:020] **Speaker 0:** Because we've got that node connected to here.
[00:16:59:760 - 00:17:02:880] **Speaker 0:** Don't worry about the minus it has to be off
[00:17:02:880 - 00:17:04:060] **Speaker 0:** if, if this one's on.
[00:17:04:900 - 00:17:05:239] **Speaker 0:** Right.
[00:17:05:819 - 00:17:08:010] **Speaker 0:** Don't worry about pole B, that's being controlled by the
[00:17:08:010 - 00:17:09:020] **Speaker 0:** other control signal.
[00:17:10:359 - 00:17:15:510] **Speaker 0:** Right, so That logic While we're in this state here,
[00:17:15:699 - 00:17:18:609] **Speaker 0:** for poll A, this is for poll A.
[00:17:20:859 - 00:17:22:959] **Speaker 0:** Then we see that the output is at VD.
[00:17:24:869 - 00:17:27:949] **Speaker 0:** What about pole B, the other control signal.
[00:17:28:040 - 00:17:30:319] **Speaker 0:** Well, let's have a look just down in this section
[00:17:30:319 - 00:17:30:739] **Speaker 0:** here.
[00:17:31:000 - 00:17:35:199] **Speaker 0:** Um, the voltage on control for pole B is still
[00:17:35:199 - 00:17:39:189] **Speaker 0:** greater than it is for The modulation signal.
[00:17:39:479 - 00:17:44:180] **Speaker 0:** So we would see for pole B, That for that
[00:17:44:180 - 00:17:46:199] **Speaker 0:** period of time in between here.
[00:17:47:010 - 00:17:50:489] **Speaker 0:** Where that control signal is greater than the modulation signal,
[00:17:50:530 - 00:17:52:510] **Speaker 0:** that we still, we also have VD.
[00:17:53:699 - 00:17:56:000] **Speaker 0:** So, B+ is turning on.
[00:17:57:589 - 00:18:00:510] **Speaker 0:** So the voltage at B will also be at VD
[00:18:00:510 - 00:18:01:310] **Speaker 0:** while it's closed.
[00:18:04:780 - 00:18:08:459] **Speaker 0:** And we can see as that that signal rises and
[00:18:08:459 - 00:18:11:420] **Speaker 0:** the amount of time in between uh increases that for
[00:18:11:420 - 00:18:13:969] **Speaker 0:** pole A we see an increase in the pulse width,
[00:18:14:380 - 00:18:16:859] **Speaker 0:** and then as it drops down and goes negative, then
[00:18:16:859 - 00:18:18:979] **Speaker 0:** we see that there is less and less amount of
[00:18:18:979 - 00:18:19:439] **Speaker 0:** time.
[00:18:20:280 - 00:18:26:839] **Speaker 0:** Where that voltage is greater than The triangle wave, right?
[00:18:26:959 - 00:18:29:660] **Speaker 0:** So we see pulse with increasing, pulse rate decreasing.
[00:18:31:579 - 00:18:35:660] **Speaker 0:** For the negative one, we see the opposite phase, OK?
[00:18:35:780 - 00:18:38:699] **Speaker 0:** So we see the pulse was decreasing and then the
[00:18:38:699 - 00:18:39:719] **Speaker 0:** pulse was increasing.
[00:18:42:260 - 00:18:44:119] **Speaker 0:** The output voltage.
[00:18:45:040 - 00:18:46:920] **Speaker 0:** What we see across the load.
[00:18:47:849 - 00:18:48:439] **Speaker 0:** Alright.
[00:18:49:140 - 00:18:52:739] **Speaker 0:** Then, it's just the difference between that voltage and that
[00:18:52:739 - 00:18:53:520] **Speaker 0:** voltage.
[00:18:54:099 - 00:18:55:459] **Speaker 0:** What is the voltage at node A?
[00:18:55:560 - 00:18:56:930] **Speaker 0:** What is the voltage at node B?
[00:18:57:140 - 00:19:00:839] **Speaker 0:** The difference in those voltages is the voltage drop across
[00:19:00:839 - 00:19:01:260] **Speaker 0:** the load.
[00:19:03:510 - 00:19:06:609] **Speaker 0:** So that's taking that voltage and subtracting that voltage.
[00:19:07:680 - 00:19:12:109] **Speaker 0:** So we see, oh, well, VD minus VD is 0.
[00:19:14:140 - 00:19:17:319] **Speaker 0:** But, can I draw it clearly enough?
[00:19:17:939 - 00:19:18:619] **Speaker 0:** I hope so.
[00:19:20:579 - 00:19:29:449] **Speaker 0:** If we see when For This one, it goes low.
[00:19:34:719 - 00:19:38:930] **Speaker 0:** That After this one goes low.
[00:19:39:209 - 00:19:42:800] **Speaker 0:** So while, So we've got this going low.
[00:19:43:520 - 00:19:45:780] **Speaker 0:** This one is still high at that point.
[00:19:46:060 - 00:19:51:640] **Speaker 0:** So now, the difference is, we've got plus VD minus
[00:19:51:780 - 00:19:54:020] **Speaker 0:** 0 equals + VD.
[00:19:55:060 - 00:20:00:020] **Speaker 0:** Yeah Right, so if you sum this line, this, this
[00:20:00:020 - 00:20:03:780] **Speaker 0:** voltage set of voltages with this set of voltages in
[00:20:03:780 - 00:20:07:229] **Speaker 0:** time, then you end up with it going from 0
[00:20:07:229 - 00:20:09:569] **Speaker 0:** to VD but with varying pulse width.
[00:20:10:260 - 00:20:12:949] **Speaker 0:** And then on the other half of it, it goes
[00:20:12:949 - 00:20:16:469] **Speaker 0:** from 0 but to minus VD with the varying width
[00:20:16:469 - 00:20:17:290] **Speaker 0:** pulse width.
[00:20:22:250 - 00:20:25:699] **Speaker 0:** OK, so we have, remember I showed that you can,
[00:20:25:819 - 00:20:28:189] **Speaker 0:** you can get to 0 volts by turning on either
[00:20:28:189 - 00:20:31:219] **Speaker 0:** TA + or TB+ or TA minus minus.
[00:20:31:310 - 00:20:32:800] **Speaker 0:** That's what's happening here.
[00:20:34:510 - 00:20:35:900] **Speaker 0:** For the zero condition.
[00:20:36:619 - 00:20:41:500] **Speaker 0:** Alright, so to produce our AC waveform out, we are.
[00:20:42:229 - 00:20:46:510] **Speaker 0:** Effectively, if we're looking at the same peak value of
[00:20:46:510 - 00:20:54:349] **Speaker 0:** our signal, halving the voltage transitions that we had for
[00:20:54:349 - 00:20:56:829] **Speaker 0:** our bipolar switching situation.
[00:21:00:619 - 00:21:04:479] **Speaker 0:** Having the voltage transitions means that we have a reduction
[00:21:04:479 - 00:21:06:640] **Speaker 0:** in the amount of harmonics being generated.
[00:21:08:119 - 00:21:11:319] **Speaker 0:** Not only that, the fact that we have two control
[00:21:11:319 - 00:21:17:280] **Speaker 0:** signals that are phase separated, controlling each pole, has the
[00:21:17:280 - 00:21:23:099] **Speaker 0:** effect of apparently doubling the control frequency.
[00:21:28:000 - 00:21:30:579] **Speaker 0:** Uh sorry, doubling the uh modulation frequency.
[00:21:32:739 - 00:21:35:630] **Speaker 0:** Right, oh, what does that look like as far as
[00:21:35:630 - 00:21:37:589] **Speaker 0:** our, our, um, Yeah.
[00:21:40:760 - 00:21:44:510] **Speaker 0:** Uh Wave, uh, harmonics are considered.
[00:21:44:750 - 00:21:47:829] **Speaker 0:** I should really, I, I meant to do this just
[00:21:47:829 - 00:21:48:209] **Speaker 0:** then.
[00:21:49:050 - 00:21:52:089] **Speaker 0:** I'll write down what the switching logic is, just so
[00:21:52:089 - 00:21:54:369] **Speaker 0:** that if you go back and look at a full
[00:21:54:369 - 00:21:57:030] **Speaker 0:** bridge, and you're trying to figure out what's going on,
[00:21:57:290 - 00:22:00:729] **Speaker 0:** um, you'll be able to follow the uh the logic
[00:22:00:729 - 00:22:01:349] **Speaker 0:** for it.
[00:22:01:810 - 00:22:03:750] **Speaker 0:** So, the control.
[00:22:06:109 - 00:22:12:250] **Speaker 0:** If that's greater than The tri, our modulation signal, then
[00:22:12:699 - 00:22:14:689] **Speaker 0:** TA plus is on.
[00:22:15:790 - 00:22:18:650] **Speaker 0:** And minus is off.
[00:22:20:109 - 00:22:23:829] **Speaker 0:** And the voltage from A to N, that node that
[00:22:23:829 - 00:22:25:109] **Speaker 0:** I've labelled as N.
[00:22:26:770 - 00:22:30:859] **Speaker 0:** Is equal to VD Right.
[00:22:31:979 - 00:22:35:469] **Speaker 0:** If the control is the opposite, is less than V
[00:22:35:469 - 00:22:35:930] **Speaker 0:** try.
[00:22:38:829 - 00:22:41:609] **Speaker 0:** Then T minus is on.
[00:22:42:290 - 00:22:46:709] **Speaker 0:** And TA plus is off.
[00:22:47:050 - 00:22:49:260] **Speaker 0:** OK, this is just the control for pole A.
[00:22:51:319 - 00:22:55:150] **Speaker 0:** And VAN equals 0 volts.
[00:22:56:500 - 00:22:58:599] **Speaker 0:** For the other pole, for pole B.
[00:22:59:770 - 00:23:02:109] **Speaker 0:** We have minus V control.
[00:23:03:199 - 00:23:05:099] **Speaker 0:** If that's greater than the try.
[00:23:06:670 - 00:23:09:930] **Speaker 0:** Then TB + is on.
[00:23:11:449 - 00:23:13:650] **Speaker 0:** TB minus of course is off.
[00:23:15:140 - 00:23:19:500] **Speaker 0:** And VBN is equal to VD.
[00:23:20:550 - 00:23:23:680] **Speaker 0:** And minus V control, less than the try.
[00:23:27:250 - 00:23:30:219] **Speaker 0:** TB minus is on.
[00:23:30:910 - 00:23:32:890] **Speaker 0:** TB plus is off.
[00:23:34:510 - 00:23:38:619] **Speaker 0:** And BBN is equal to 0.
[00:23:47:119 - 00:23:47:719] **Speaker 1:** Right.
[00:24:01:239 - 00:24:02:500] **Speaker 1:** The harmonics then.
[00:24:07:089 - 00:24:09:479] **Speaker 1:** Well, we all got that copy down?
[00:24:10:800 - 00:24:11:400] **Speaker 0:** Yeah.
[00:24:11:920 - 00:24:13:300] **Speaker 0:** No one, alright.
[00:24:17:650 - 00:24:18:689] **Speaker 1:** The harmonics.
[00:24:23:540 - 00:24:28:000] **Speaker 0:** Right, so the effect here, um, For the transitions in
[00:24:28:000 - 00:24:30:839] **Speaker 0:** unipolar switching being half the amplitude as for bipolar switching,
[00:24:30:880 - 00:24:34:119] **Speaker 0:** I know the bipolar switching had VD over 2 and
[00:24:34:119 - 00:24:37:599] **Speaker 0:** minus VD over 2, so overall the, the combined is
[00:24:37:599 - 00:24:42:959] **Speaker 0:** VD, but we're assuming that the, um, that the control
[00:24:42:959 - 00:24:44:439] **Speaker 0:** signal is the same amplitude.
[00:24:44:520 - 00:24:49:510] **Speaker 0:** So in order to have um Uh, that be the
[00:24:49:510 - 00:24:49:680] **Speaker 0:** case.
[00:24:49:760 - 00:24:52:219] **Speaker 0:** It would effectively be the same as saying that it's
[00:24:52:520 - 00:24:59:239] **Speaker 0:** um twice the amplitude for the, um, For the unipolar
[00:24:59:239 - 00:24:59:680] **Speaker 0:** case.
[00:25:00:689 - 00:25:03:609] **Speaker 0:** So, even though it goes from VD to 0 and
[00:25:03:609 - 00:25:07:010] **Speaker 0:** then from 0 to minus VD, the, if we've got
[00:25:07:010 - 00:25:10:849] **Speaker 0:** the same control signal amplitude, it's, it's half the actual
[00:25:10:849 - 00:25:11:670] **Speaker 0:** amplitude.
[00:25:12:130 - 00:25:15:250] **Speaker 0:** So those transitions are half the amplitude of what they
[00:25:15:250 - 00:25:16:510] **Speaker 0:** were for the bipolar case.
[00:25:18:709 - 00:25:21:270] **Speaker 0:** It's just the fact that we're using a general VD
[00:25:21:270 - 00:25:24:250] **Speaker 0:** term, it's the actual value of voltage would be less.
[00:25:25:569 - 00:25:29:250] **Speaker 0:** Right, um, the equivalent is effect of doubling the carrier
[00:25:29:250 - 00:25:34:000] **Speaker 0:** signal frequency so that the harmonics occur around even multiples
[00:25:34:000 - 00:25:35:250] **Speaker 0:** of switching frequency.
[00:25:36:680 - 00:25:39:650] **Speaker 0:** Alright, so now to eliminate some of the harmonic content,
[00:25:39:810 - 00:25:44:550] **Speaker 0:** our frequency modulation um ratio.
[00:25:45:530 - 00:25:48:920] **Speaker 0:** Should be an even integer, not odd as it was
[00:25:48:920 - 00:25:49:760] **Speaker 0:** for bipolar.
[00:25:51:839 - 00:25:53:579] **Speaker 0:** So the overall effect is given here.
[00:25:55:260 - 00:25:56:119] **Speaker 0:** Look at that.
[00:25:56:739 - 00:26:00:540] **Speaker 0:** When MF is equal to 1, we had a bunch
[00:26:00:540 - 00:26:03:459] **Speaker 0:** of harmonics before for bipolar switching.
[00:26:03:780 - 00:26:04:619] **Speaker 0:** Those are gone.
[00:26:05:500 - 00:26:09:329] **Speaker 0:** Anything where we've got an odd number for MF, uh,
[00:26:09:339 - 00:26:12:900] **Speaker 0:** an odd multiple of MF, then there are no harmonics
[00:26:12:900 - 00:26:13:760] **Speaker 0:** at all.
[00:26:14:300 - 00:26:17:540] **Speaker 0:** No side bands either, right?
[00:26:17:619 - 00:26:23:699] **Speaker 0:** They only occur when we've got an even Um, multiplying
[00:26:23:699 - 00:26:28:170] **Speaker 0:** of that modulation ratio, frequency modulation ratio.
[00:26:30:250 - 00:26:32:900] **Speaker 0:** Uh, we know that this is an MA, uh, of
[00:26:32:900 - 00:26:35:780] **Speaker 0:** equal to 8 because of that, of 0.8.
[00:26:39:339 - 00:26:42:140] **Speaker 0:** I don't forget here, this is normalised to VD, not
[00:26:42:140 - 00:26:43:280] **Speaker 0:** to VD over 2.
[00:26:49:089 - 00:26:53:099] **Speaker 0:** So with The harmonic content being further away from the
[00:26:53:099 - 00:26:55:920] **Speaker 0:** fundamental by a long shot.
[00:26:57:160 - 00:26:59:540] **Speaker 0:** Then, and it's also lower amplitude.
[00:27:00:530 - 00:27:05:209] **Speaker 0:** The filtering requirements are considerably reduced again compared to what
[00:27:05:209 - 00:27:06:910] **Speaker 0:** they were for bipolar switching.
[00:27:08:290 - 00:27:12:650] **Speaker 0:** OK, so unipolar switching can be very advantageous for higher
[00:27:12:650 - 00:27:15:060] **Speaker 0:** power applications where we need to get rid of the,
[00:27:15:329 - 00:27:18:089] **Speaker 0:** uh, the harmonic, so our philtre components can be much
[00:27:18:089 - 00:27:18:469] **Speaker 0:** smaller.
[00:27:23:619 - 00:27:28:390] **Speaker 0:** Uh, we could choose, um, a larger value of MF
[00:27:28:390 - 00:27:31:770] **Speaker 0:** again to, to pull those components, those frequencies away.
[00:27:32:140 - 00:27:37:709] **Speaker 0:** This case, an MF greater than around, um, 10, oops,
[00:27:38:030 - 00:27:38:630] **Speaker 0:** around 10.
[00:27:39:989 - 00:27:41:849] **Speaker 0:** Would be, would be fine.
[00:27:45:869 - 00:27:50:140] **Speaker 0:** For the bipolar case, um, you're looking more like, uh,
[00:27:50:150 - 00:27:55:939] **Speaker 0:** having an MF that's, uh, greater than 21.
[00:27:56:310 - 00:27:57:439] **Speaker 0:** Sorry, I didn't write that in.
[00:27:57:949 - 00:28:03:790] **Speaker 1:** So for The bipolar case, uh, to, to keep these
[00:28:03:790 - 00:28:05:750] **Speaker 0:** away at a reasonable amount, you might want to choose,
[00:28:05:869 - 00:28:07:670] **Speaker 0:** yeah, here we go, in excess of 21.
[00:28:15:500 - 00:28:15:959] **Speaker 0:** OK.
[00:28:18:979 - 00:28:22:500] **Speaker 0:** That's a way of reducing those harmonics.
[00:28:23:530 - 00:28:28:609] **Speaker 0:** I'm just, now I'm gonna revisit over modulation to show
[00:28:28:609 - 00:28:32:250] **Speaker 0:** you a situation where you might actually kind of break
[00:28:32:250 - 00:28:39:439] **Speaker 0:** the rules, um, and Create a lot more harmonics, uh,
[00:28:39:560 - 00:28:40:859] **Speaker 0:** for a really good reason.
[00:28:48:280 - 00:28:51:189] **Speaker 0:** So, if there was a situation where you had, for
[00:28:51:189 - 00:28:54:479] **Speaker 0:** example, a a motor driving a mechanical load and there
[00:28:54:479 - 00:29:00:839] **Speaker 0:** was an unexpected Uh, increase in that load that required
[00:29:00:839 - 00:29:03:800] **Speaker 0:** you just for a little short period of time to
[00:29:03:800 - 00:29:09:699] **Speaker 0:** produce additional torque beyond technically the rating of that motor.
[00:29:10:319 - 00:29:11:619] **Speaker 0:** How are you going to do that?
[00:29:12:530 - 00:29:15:569] **Speaker 0:** Well one thing that you can do for short periods
[00:29:15:569 - 00:29:18:410] **Speaker 0:** of time, because it's not good for efficiency, and it's
[00:29:18:410 - 00:29:23:229] **Speaker 0:** not good for keeping your motor um within thermal limits,
[00:29:23:729 - 00:29:27:430] **Speaker 0:** um, one thing you can do is push, The pulse
[00:29:27:430 - 00:29:30:930] **Speaker 0:** with modulation system into over modulation mode.
[00:29:33:739 - 00:29:39:170] **Speaker 0:** Alright, so, If you do that, if you go from
[00:29:39:369 - 00:29:46:380] **Speaker 0:** being within the linear Region and push your control signal
[00:29:46:380 - 00:29:51:949] **Speaker 0:** amplitude above the amplitude of your modulating signal, then you
[00:29:51:949 - 00:29:53:069] **Speaker 0:** go into over-modulation.
[00:29:53:109 - 00:29:55:790] **Speaker 0:** It's where you start seeing that waveform starting to square
[00:29:55:790 - 00:29:59:310] **Speaker 0:** up rather than reproducing the nice sine wave as these
[00:29:59:310 - 00:30:00:910] **Speaker 0:** flat tops and bottoms.
[00:30:05:540 - 00:30:08:300] **Speaker 0:** So that, what that will do is if you look
[00:30:08:300 - 00:30:13:829] **Speaker 0:** at the harmonics that are created, the fundamental actually exceeds.
[00:30:16:500 - 00:30:17:959] **Speaker 0:** The supply voltage.
[00:30:21:680 - 00:30:25:770] **Speaker 0:** The DC supply coming in, your fundamental from those harmonics
[00:30:25:770 - 00:30:30:209] **Speaker 0:** will be a greater amplitude, enabling you to drive more
[00:30:30:209 - 00:30:32:849] **Speaker 0:** power into the load.
[00:30:34:209 - 00:30:37:329] **Speaker 0:** Because you have a higher voltage, and from that you
[00:30:37:329 - 00:30:40:329] **Speaker 0:** can drive more current into your motor because the back
[00:30:40:329 - 00:30:43:550] **Speaker 0:** EMF um isn't limiting your current as much anymore.
[00:30:45:670 - 00:30:50:020] **Speaker 0:** Right, so it's a way of, Kind of a, a
[00:30:50:540 - 00:30:53:819] **Speaker 0:** not great way, but it is a way of addressing
[00:30:53:819 - 00:30:57:060] **Speaker 0:** a, a load situation that so long as you know
[00:30:57:060 - 00:30:59:939] **Speaker 0:** it's going to be very temporary, uh, and transient, that
[00:30:59:939 - 00:31:03:380] **Speaker 0:** you can utilise the system that you've got in play,
[00:31:03:660 - 00:31:05:819] **Speaker 0:** uh, for a very short period of time to, to
[00:31:05:819 - 00:31:06:569] **Speaker 0:** manage that.
[00:31:06:859 - 00:31:09:420] **Speaker 0:** But look at the, look at the harmonics.
[00:31:10:989 - 00:31:14:550] **Speaker 0:** Those are are no longer far away from the fundamental,
[00:31:14:650 - 00:31:17:890] **Speaker 0:** they've moved right up and they've got a nice, uh,
[00:31:18:310 - 00:31:23:189] **Speaker 0:** level of um of amplitude, so you end up with
[00:31:23:189 - 00:31:24:650] **Speaker 0:** considerably more harmonics.
[00:31:25:069 - 00:31:27:900] **Speaker 0:** You haven't changed the philtre components compared to what it
[00:31:27:900 - 00:31:32:189] **Speaker 0:** would normally be expected, uh, under the linear operation zone,
[00:31:32:510 - 00:31:35:390] **Speaker 0:** so they are not going to philtre those harmonics very
[00:31:35:390 - 00:31:36:170] **Speaker 0:** well at all.
[00:31:37:050 - 00:31:39:650] **Speaker 0:** So, the, the wave form that you'll see at the
[00:31:39:650 - 00:31:42:349] **Speaker 0:** load will be quite square wave looking.
[00:31:44:829 - 00:31:47:630] **Speaker 0:** Right, but it does get you out of a sticky
[00:31:47:630 - 00:31:51:069] **Speaker 0:** situation of the of that change in load stopping the
[00:31:51:069 - 00:31:51:890] **Speaker 0:** machine from working.
[00:31:53:040 - 00:31:53:160] **Speaker 1:** What?
[00:32:02:459 - 00:32:06:030] **Speaker 1:** Alright, we're coming Basically to the end of that material.
[00:32:06:069 - 00:32:08:290] **Speaker 0:** What I'm going to do now is just run through
[00:32:08:630 - 00:32:12:339] **Speaker 0:** a really quick example of how you might, uh, of,
[00:32:12:390 - 00:32:14:530] **Speaker 0:** of the sort of thing that you might, uh, see
[00:32:14:530 - 00:32:16:170] **Speaker 0:** that's needing to be solved.
[00:32:21:650 - 00:32:24:439] **Speaker 0:** So we've got a problem here, switch mode inverter, single
[00:32:24:439 - 00:32:25:430] **Speaker 0:** phase, half bridge.
[00:32:27:040 - 00:32:31:489] **Speaker 0:** Says general analysis of the inverter, shown here is to
[00:32:31:489 - 00:32:31:810] **Speaker 0:** be done.
[00:32:31:890 - 00:32:37:530] **Speaker 0:** The switching frequency identified as FS, which is also the
[00:32:37:530 - 00:32:42:349] **Speaker 0:** frequency of the triangular signal, is 1450 Hz.
[00:32:43:689 - 00:32:44:599] **Speaker 0:** There'll be a reason for that.
[00:32:45:550 - 00:32:49:280] **Speaker 0:** Um, the DC voltage, so that's the voltage here is
[00:32:49:280 - 00:32:50:290] **Speaker 0:** 600 volts.
[00:32:53:650 - 00:32:57:209] **Speaker 0:** The filtered output voltage is sinusoidal with a frequency equal
[00:32:57:209 - 00:32:58:060] **Speaker 0:** to 50 Hz.
[00:32:59:719 - 00:33:02:500] **Speaker 0:** The load is connected between the inverter.
[00:33:03:430 - 00:33:07:959] **Speaker 0:** League poll A And the DC voltage midpoint0.
[00:33:08:430 - 00:33:11:270] **Speaker 0:** So if we were to draw in, um, an actual
[00:33:11:270 - 00:33:24:079] **Speaker 0:** load, it's gonna be a little messy, but Would look
[00:33:24:079 - 00:33:24:569] **Speaker 0:** like that.
[00:33:32:719 - 00:33:33:319] **Speaker 0:** All right.
[00:33:37:520 - 00:33:40:339] **Speaker 0:** Part A, find the frequency modulation ratio.
[00:33:41:349 - 00:33:46:170] **Speaker 0:** And why is it chosen to be an odd number?
[00:33:47:150 - 00:33:59:869] **Speaker 1:** Right, so Hey MF we just apply the formula, right?
[00:34:00:069 - 00:34:04:689] **Speaker 0:** So that's the switching frequency divided by the reference.
[00:34:05:359 - 00:34:08:260] **Speaker 0:** And that's equal to, we're told the switching frequency is
[00:34:08:260 - 00:34:10:300] **Speaker 0:** 1450.
[00:34:11:459 - 00:34:15:540] **Speaker 0:** The reference is the same frequency as the output signal
[00:34:15:540 - 00:34:16:860] **Speaker 0:** that we're trying to produce.
[00:34:17:340 - 00:34:19:179] **Speaker 0:** So that's 50 Hz.
[00:34:20:388 - 00:34:21:870] **Speaker 0:** Right, so.
[00:34:22:820 - 00:34:24:120] **Speaker 0:** That's 29.
[00:34:28:860 - 00:34:32:479] **Speaker 0:** And why is it chosen as an odd number?
[00:34:34:080 - 00:34:41:878] **Speaker 0:** Well, That eliminates Dominant, even harmonics.
[00:34:51:418 - 00:34:52:829] **Speaker 0:** And the cosign.
[00:34:58:280 - 00:35:00:439] **Speaker 0:** Courier coefficients are 0.
[00:35:18:689 - 00:35:21:629] **Speaker 0:** So the fact that we've got an odd number.
[00:35:23:919 - 00:35:27:780] **Speaker 0:** Identifies to us that this must be bipolar switching operation.
[00:35:40:179 - 00:35:41:639] **Speaker 1:** That and the fact that it's a half bridge.
[00:35:42:449 - 00:35:45:310] **Speaker 0:** You can't do unipolar switching with a half bridge.
[00:35:46:169 - 00:35:48:830] **Speaker 0:** You can do bipolar switching with a full bridge.
[00:35:56:689 - 00:35:58:409] **Speaker 0:** OK, uh, B.
[00:35:59:899 - 00:36:04:969] **Speaker 0:** Calculate the output voltage, RMS of the fundamental when the
[00:36:04:969 - 00:36:08:510] **Speaker 0:** amplitude modulation ratio is equal to 0.8.
[00:36:08:810 - 00:36:10:510] **Speaker 0:** So that's why we have this table here.
[00:36:11:320 - 00:36:18:379] **Speaker 0:** So This table is a normalised uh harmonic amplitude, um,
[00:36:18:399 - 00:36:20:300] **Speaker 0:** normalised to VD over 2.
[00:36:21:570 - 00:36:21:580] **Speaker 1:** Alright.
[00:36:23:620 - 00:36:27:100] **Speaker 0:** Um, and like I said, it's the, it's relative to
[00:36:27:100 - 00:36:29:120] **Speaker 0:** the peak of the harmonic.
[00:36:30:100 - 00:36:31:959] **Speaker 0:** So we want the RMS value, right?
[00:36:32:459 - 00:36:34:860] **Speaker 0:** So we need a one over route 2 of the
[00:36:34:860 - 00:36:35:379] **Speaker 0:** peak.
[00:36:37:149 - 00:36:45:510] **Speaker 0:** So beat The out peak is equal to 0.8.
[00:36:46:709 - 00:36:50:870] **Speaker 0:** Times VD over 2, 600/2.
[00:36:52:209 - 00:36:56:320] **Speaker 0:** Equals 240 volts, but we want the RMS, that's the
[00:36:56:320 - 00:36:57:040] **Speaker 0:** peak value.
[00:36:58:110 - 00:37:05:340] **Speaker 0:** So V out Are remiss Is equal to 240, oops.
[00:37:06:570 - 00:37:10:290] **Speaker 0:** It's a 50 hertz sinusoid, so it's over route 2.
[00:37:14:040 - 00:37:15:489] **Speaker 0:** That's 170 volts.
[00:37:24:929 - 00:37:30:000] **Speaker 0:** See When the amplitude modulation ratio varies from 0 to
[00:37:30:000 - 00:37:32:659] **Speaker 0:** 1, the modulation is in the linear domain.
[00:37:33:709 - 00:37:42:679] **Speaker 0:** Why Well, see When MA is less than or equal
[00:37:42:679 - 00:37:45:540] **Speaker 0:** to one, the peak.
[00:37:46:750 - 00:37:51:909] **Speaker 0:** Of the Um, pole A output.
[00:37:52:969 - 00:37:56:989] **Speaker 0:** is equal to MA times VD over 2.
[00:37:58:239 - 00:37:59:260] **Speaker 1:** And it's linear.
[00:38:01:969 - 00:38:18:310] **Speaker 0:** As we're comparing Our control, Against a linear sloped waveform.
[00:38:28:919 - 00:38:33:239] **Speaker 0:** OK, so a linear change in comparison with our signal
[00:38:33:239 - 00:38:36:139] **Speaker 0:** results in a linear change in the uh pulse width.
[00:38:45:120 - 00:38:48:280] **Speaker 0:** Um, D, I'm not going to write down, it's a
[00:38:48:280 - 00:38:53:000] **Speaker 0:** little bit long-winded, and you can, you can immediately tell
[00:38:53:000 - 00:38:55:439] **Speaker 0:** from the, the table as to how to, how to
[00:38:55:439 - 00:38:56:439] **Speaker 0:** come up with a solution.
[00:38:56:919 - 00:39:00:639] **Speaker 0:** So, what it's saying there is, is compare or compute
[00:39:01:120 - 00:39:05:459] **Speaker 0:** the RMS values of the five most dominant harmonics of,
[00:39:06:040 - 00:39:10:879] **Speaker 0:** um, pole A at MA is equal to 0.8.
[00:39:10:959 - 00:39:12:899] **Speaker 0:** So we're talking about looking down this column.
[00:39:14:820 - 00:39:19:610] **Speaker 0:** I will identify what are the top 5 harmonic amplitudes,
[00:39:19:659 - 00:39:22:080] **Speaker 0:** so this is clearly number 1.
[00:39:22:580 - 00:39:23:979] **Speaker 0:** It's our top harmonic.
[00:39:24:679 - 00:39:26:899] **Speaker 0:** Um, that's not number 2.
[00:39:27:459 - 00:39:28:860] **Speaker 0:** Number 2 is down here.
[00:39:31:899 - 00:39:37:679] **Speaker 0:** That's our 2nd most or highest amplitude harmonic.
[00:39:38:010 - 00:39:39:280] **Speaker 0:** Number 3 is here.
[00:39:41:850 - 00:39:46:389] **Speaker 0:** Then we go, number 44 is down here.
[00:39:48:520 - 00:39:50:659] **Speaker 0:** And then 5.
[00:39:53:120 - 00:39:57:000] **Speaker 0:** Right, those are the top 5 most dominant harmonics, because
[00:39:57:000 - 00:39:57:919] **Speaker 0:** of their amplitude.
[00:40:03:310 - 00:40:06:800] **Speaker 0:** How you get the RMS value is you take that
[00:40:06:800 - 00:40:09:669] **Speaker 0:** amplitude, uh, and, and the frequencies, where you, for the
[00:40:09:669 - 00:40:12:479] **Speaker 0:** RMS value, you take that amplitude and we do exactly
[00:40:12:479 - 00:40:13:610] **Speaker 0:** what we've just done here.
[00:40:14:510 - 00:40:19:389] **Speaker 0:** So you take that uh 0.314, you go 0.314 times
[00:40:19:389 - 00:40:21:770] **Speaker 0:** 600/2 divided by route 2.
[00:40:23:949 - 00:40:25:310] **Speaker 0:** Yeah, that'll give you the RMS value.
[00:40:25:389 - 00:40:26:489] **Speaker 0:** What is the frequency?
[00:40:26:909 - 00:40:30:879] **Speaker 0:** Well, the frequency in each of these is just 2
[00:40:30:879 - 00:40:36:979] **Speaker 0:** times the modulation, frequency modulation ratio, plus or minus 1
[00:40:38:120 - 00:40:42:350] **Speaker 0:** times, The switching frequency.
[00:40:50:649 - 00:40:51:010] **Speaker 0:** OK.
[00:40:54:639 - 00:41:08:879] **Speaker 0:** E Uh, which frequencies are desirable for the switching frequency?
[00:41:09:030 - 00:41:12:689] **Speaker 0:** List advantages and disadvantages of low and high switching frequency.
[00:41:13:270 - 00:41:24:189] **Speaker 0:** OK, so, if it's bipolar switching, You want The modulation
[00:41:24:729 - 00:41:27:189] **Speaker 0:** ratio, frequency modulation ratio.
[00:41:28:540 - 00:41:29:860] **Speaker 0:** To be an odd integer.
[00:41:33:810 - 00:41:34:989] **Speaker 0:** If it's unipolar.
[00:41:36:810 - 00:41:40:229] **Speaker 0:** This is just for the sake of um completeness.
[00:41:44:060 - 00:41:46:419] **Speaker 0:** MMF wants to be an even integer.
[00:41:51:250 - 00:41:54:760] **Speaker 0:** As far as the switching frequencies, advantages, disadvantages.
[00:41:58:330 - 00:41:59:719] **Speaker 0:** So, we'll go.
[00:42:00:669 - 00:42:03:689] **Speaker 0:** Low If it high.
[00:42:05:139 - 00:42:10:260] **Speaker 0:** FS and then Advantage.
[00:42:12:570 - 00:42:13:800] **Speaker 1:** Disadvantage.
[00:42:18:709 - 00:42:22:379] **Speaker 0:** So For low switching frequency, what's an advantage?
[00:42:22:459 - 00:42:24:399] **Speaker 0:** Well, we have low switching losses.
[00:42:35:330 - 00:42:39:340] **Speaker 0:** Um, it's also because of the low frequency nature and
[00:42:39:340 - 00:42:42:399] **Speaker 0:** we need, if we're going to eliminate these harmonics and
[00:42:42:399 - 00:42:48:310] **Speaker 0:** have an integer value of our frequency modulation ratio, it's
[00:42:48:310 - 00:42:50:580] **Speaker 0:** easier to synchronise those signals.
[00:43:15:610 - 00:43:17:020] **Speaker 0:** Uh, what's the disadvantage?
[00:43:17:179 - 00:43:21:179] **Speaker 0:** Well, lower switching frequencies means that your harmonics are closer
[00:43:21:179 - 00:43:22:080] **Speaker 0:** to the fundamental.
[00:43:43:429 - 00:43:46:040] **Speaker 0:** Um, so you need larger philtre components.
[00:43:56:489 - 00:44:01:669] **Speaker 0:** Not only that, If it's low enough as it is
[00:44:01:669 - 00:44:07:449] **Speaker 0:** for some large um Uh, large power applications, um, and
[00:44:07:449 - 00:44:11:370] **Speaker 0:** you get below 20 kilohertz or so switching speed, then
[00:44:11:370 - 00:44:12:350] **Speaker 0:** you can hear it.
[00:44:13:090 - 00:44:14:649] **Speaker 0:** That's, and it gets annoying.
[00:44:15:620 - 00:44:18:879] **Speaker 0:** So it can create audible noise.
[00:44:25:459 - 00:44:28:409] **Speaker 0:** So the advantages are kind of the opposite, so um
[00:44:28:409 - 00:44:29:959] **Speaker 0:** harmonics are easy to philtre out.
[00:44:40:689 - 00:44:42:889] **Speaker 0:** Uh, so we have smaller philtre components.
[00:44:50:659 - 00:44:52:600] **Speaker 0:** Uh, and there's no audio noise.
[00:44:55:760 - 00:44:56:899] **Speaker 0:** No audible noise.
[00:44:59:080 - 00:45:00:250] **Speaker 0:** Disadvantages.
[00:45:01:250 - 00:45:04:449] **Speaker 0:** Opposite of the advantage for low switching frequencies, so we
[00:45:04:449 - 00:45:06:750] **Speaker 0:** have high higher switching losses.
[00:45:13:419 - 00:45:16:030] **Speaker 0:** And it's harder to synchronise those two signals.
[00:45:24:469 - 00:45:26:840] **Speaker 1:** Those are the main Things.
[00:45:27:239 - 00:45:30:439] **Speaker 0:** OK, so that's it for the quick example, and that's
[00:45:30:439 - 00:45:33:979] **Speaker 0:** it for the inverter material that we're covering at least.
[00:45:34:530 - 00:45:36:729] **Speaker 0:** And that's it for the material that I'm covering for
[00:45:36:729 - 00:45:37:449] **Speaker 0:** this course.
[00:45:37:729 - 00:45:41:399] **Speaker 0:** Um, you'll have Chris Hahn next term, uh, covering other
[00:45:41:399 - 00:45:41:830] **Speaker 0:** material.
[00:45:42:250 - 00:45:44:209] **Speaker 0:** He'll kick off kind of rounding off things to do
[00:45:44:209 - 00:45:46:889] **Speaker 0:** with power electronics and then move on to, um, analogue
[00:45:46:889 - 00:45:49:389] **Speaker 0:** electronic sort of domain stuff.
[00:45:49:770 - 00:45:52:030] **Speaker 0:** Um, but of course, you're not getting rid of me.
[00:45:52:290 - 00:45:55:679] **Speaker 0:** Um, I'm heading up the rest of the, the, the,
[00:45:55:689 - 00:45:57:780] **Speaker 0:** um, solar car assignment, uh, project.
[00:45:57:889 - 00:46:00:419] **Speaker 0:** So I do all of the rest of the assessments
[00:46:00:419 - 00:46:01:030] **Speaker 0:** on that.
[00:46:01:649 - 00:46:03:429] **Speaker 0:** Right, OK, that's it for today.
[00:46:07:060 - 00:46:07:229] **Speaker 1:** Thank you.
[00:46:09:350 - 00:46:11:169] **Speaker 0:** I didn't say you would be seeing me again.

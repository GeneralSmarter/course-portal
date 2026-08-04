# ENMT301-26W Lecture 65 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `09439d3c77d225c875b9901fdf6c69cdadf4dc2142ff512b9a2f1aef846088ef`
Generated: 2026-06-06T07:25:25.307207+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:00 - 00:00:05] I think it would be too difficult to be monitoring the ecosystem
[00:00:05 - 00:00:08] in the face of a question as well as the lecture.
[00:00:08 - 00:00:14] Okay.
[00:00:14 - 00:00:17] So, clock, so we'll get started.
[00:00:17 - 00:00:20] You record today.
[00:00:20 - 00:00:26] I won't say anything about changing my first question because I'm going to trouble.
[00:00:26 - 00:00:30] Right. So, just a recap of where we were at.
[00:00:30 - 00:00:32] You say, so we're looking at sensors.
[00:00:32 - 00:00:34] So, three examples we've got here.
[00:00:34 - 00:00:38] So, in our radar, in Lido, we're sending out a signal.
[00:00:38 - 00:00:40] We're waiting for an echo.
[00:00:40 - 00:00:44] And then we're capturing that echo, processing that echo.
[00:00:44 - 00:00:48] And then the time flight is how long it takes from our sending with the transducer,
[00:00:48 - 00:00:52] the antenna, or the laser to then receive it with our transducer antenna,
[00:00:52 - 00:00:55] or photo diode.
[00:00:55 - 00:00:59] Okay. So, hopefully this also aligns with what you're doing with your robo cups.
[00:00:59 - 00:01:09] Okay. So, we'll look at, we have to.
[00:01:09 - 00:01:14] Okay. So, we're looking at different types of types.
[00:01:14 - 00:01:15] Let me finish this today.
[00:01:15 - 00:01:20] Looking at this relationship between speed, frequency, and wavelength,
[00:01:20 - 00:01:22] which is hopefully high school physics.
[00:01:22 - 00:01:27] And then, so I've got four different modes of operation here.
[00:01:27 - 00:01:31] At the bottom, looking at sort of typical speeds, frequencies, and wavelengths for them.
[00:01:31 - 00:01:40] So, with ESOMar, so there's this sending a sound wave through ES,
[00:01:40 - 00:01:45] so the speed of sound in the air is 340 meters per second.
[00:01:45 - 00:01:48] And so, it ends up being here.
[00:01:48 - 00:01:50] So, typical speed is 40 kilohertz.
[00:01:50 - 00:01:53] So, that's slightly above what we can hear with the human ear.
[00:01:53 - 00:01:55] Probably not two times above.
[00:01:55 - 00:01:58] I think that's about 20 kilohertz as the cutoff.
[00:01:58 - 00:02:01] And then, okay.
[00:02:01 - 00:02:04] So, this is the speed of sound in the air.
[00:02:04 - 00:02:15] Okay. And then, with normal sonar,
[00:02:15 - 00:02:17] so that's through water.
[00:02:17 - 00:02:19] So, the speed is found in sea water,
[00:02:19 - 00:02:22] it's something 100 meters per second.
[00:02:22 - 00:02:28] And this is actually using the same frequency as the ESOMar,
[00:02:28 - 00:02:30] but because the speed's different.
[00:02:30 - 00:02:34] We give a longer wavelength.
[00:02:34 - 00:02:38] And then, so for radar and light up,
[00:02:38 - 00:02:44] the speed is approximately the speed of light,
[00:02:44 - 00:02:49] which is three times 10 to the eight meters per second.
[00:02:49 - 00:02:55] And then, the difference in radar and light up is we have different wavelengths.
[00:02:55 - 00:02:58] So, with radar, we're dealing with radio waves.
[00:02:58 - 00:03:06] And then, light up will either work in the visible or infrared.
[00:03:06 - 00:03:08] It's 700 nanometers here.
[00:03:08 - 00:03:11] This is the case of visible,
[00:03:11 - 00:03:19] and it's at the red end of the spectrum.
[00:03:19 - 00:03:24] And so, from memory, your IR range minus,
[00:03:24 - 00:03:28] and then, near and freed, 900 nanometers,
[00:03:28 - 00:03:30] so you can't actually see it.
[00:03:30 - 00:03:45] Okay. So, when we are sending our signal with our radar,
[00:03:45 - 00:03:50] and here, or our transducer for the sonar,
[00:03:50 - 00:03:53] the waves spreads out in a spherical waveform.
[00:03:53 - 00:03:56] So, let's draw this here.
[00:03:56 - 00:04:00] So, we're going to transducer.
[00:04:00 - 00:04:12] Okay. So, let's have our transducer here.
[00:04:12 - 00:04:21] And it's sending out waves, or to blue here.
[00:04:21 - 00:04:25] And so, from the point of origin,
[00:04:25 - 00:04:28] it propagates as a spherical wave,
[00:04:28 - 00:04:34] so that every point on this wavefront is the same distance away from the...
[00:04:34 - 00:04:36] transducer.
[00:04:36 - 00:04:40] Okay. So, as the wave propagates,
[00:04:40 - 00:04:43] the transmittance signal is spreading out,
[00:04:43 - 00:04:51] so we're losing then energy for a particular point.
[00:04:51 - 00:04:56] So, at the start, all the energy in the wavefront is in a small area,
[00:04:56 - 00:04:59] and as it propagates,
[00:04:59 - 00:05:05] the amount of energy in a particular area in the wavefront goes down.
[00:05:05 - 00:05:15] And so, if we have a target here,
[00:05:15 - 00:05:25] this...
[00:05:25 - 00:05:28] If we have our waves just going in one direction,
[00:05:28 - 00:05:34] because that was our amplitude of the wave,
[00:05:34 - 00:05:38] is proportional to 1 over R,
[00:05:38 - 00:05:40] where R is the range.
[00:05:40 - 00:05:48] Okay. So, the range here is this distance from the transducer to the target.
[00:05:48 - 00:05:56] And so, we have a reflection from the target,
[00:05:56 - 00:06:05] then going back transducer,
[00:06:05 - 00:06:10] and so, then for this two-way propagation,
[00:06:10 - 00:06:12] so we've gone from the transducer to the target,
[00:06:12 - 00:06:14] and then from the target back to the transducer.
[00:06:14 - 00:06:23] So, for two-way, the amplitude is then proportional to 1 over R,
[00:06:23 - 00:06:28] going there, times 1 over R coming back,
[00:06:28 - 00:06:32] so then our amplitude is 1 over R squared.
[00:06:32 - 00:06:49] Okay. And if we think about the power of the wave,
[00:06:49 - 00:06:53] the power is proportional to the amplitude squared,
[00:06:53 - 00:07:02] so that means the power is proportional to 1 over R squared,
[00:07:02 - 00:07:07] which is 1 over R to the 4.
[00:07:07 - 00:07:15] Okay. So, the further away,
[00:07:15 - 00:07:20] our target is the amount of energy that's coming back to us
[00:07:20 - 00:07:23] from the target,
[00:07:23 - 00:07:27] the output from the target is decreasing strongly with the range,
[00:07:27 - 00:07:29] the distance to the target.
[00:07:29 - 00:07:34] Okay. So, those are spreading losses,
[00:07:34 - 00:07:38] the effect of the spherical wave coming out of our transducer,
[00:07:38 - 00:07:40] as reflecting.
[00:07:40 - 00:07:42] So, spreading loss.
[00:07:42 - 00:07:46] We also have another loss called the absorption loss,
[00:07:46 - 00:07:48] which we'll do now,
[00:07:48 - 00:07:54] which is the medium absorbing some energy of the wave going through.
[00:07:54 - 00:08:04] Okay. So, some of the energy in the wave is lost as heat,
[00:08:04 - 00:08:06] as well.
[00:08:06 - 00:08:12] So, we can say the amplitude is going to decay exponentially
[00:08:12 - 00:08:15] with distance or range.
[00:08:15 - 00:08:18] So, we're at the same equation.
[00:08:18 - 00:08:22] The amplitude is equal to the initial amplitude,
[00:08:22 - 00:08:23] A naught.
[00:08:23 - 00:08:25] And then, let's say,
[00:08:25 - 00:08:27] next initial here,
[00:08:27 - 00:08:28] negative exponential,
[00:08:28 - 00:08:32] it's decaying e to the minus 2QR.
[00:08:32 - 00:08:34] So, we'll go through in the final these.
[00:08:34 - 00:08:36] R is the range, of course.
[00:08:36 - 00:08:42] Our distance, A is our amplitude.
[00:08:42 - 00:08:52] And this, A naught is our initial amplitude.
[00:08:52 - 00:09:01] And then, the thing we haven't defined yet is Q.
[00:09:01 - 00:09:06] And this is known as the absorption coefficient.
[00:09:06 - 00:09:20] And this depends a lot on the medium that we're sending our wave through.
[00:09:20 - 00:09:27] So, it depends on the frequency of the wave we're sending.
[00:09:27 - 00:09:30] Frequency of wavelength related.
[00:09:30 - 00:09:40] And also on the medium,
[00:09:40 - 00:09:48] so temperature, humidity,
[00:09:48 - 00:09:51] for sending is an,
[00:09:51 - 00:09:55] salinity, if we're sending it through salt water,
[00:09:55 - 00:09:58] these will affect our,
[00:09:58 - 00:10:01] how much of the wave gets absorbed.
[00:10:01 - 00:10:02] As we go through,
[00:10:02 - 00:10:03] it says,
[00:10:03 - 00:10:05] a coefficient Q there,
[00:10:05 - 00:10:12] which depends on all these parameters.
[00:10:12 - 00:10:16] Okay, so there's two different waves that we lose power in our wave.
[00:10:16 - 00:10:18] There's a propagates from the target,
[00:10:18 - 00:10:20] so that, from the transducers of the target,
[00:10:20 - 00:10:21] and back again,
[00:10:21 - 00:10:23] there's a spreading out of the wave,
[00:10:23 - 00:10:29] and also then some absorption of the energy of the wave inside the medium.
[00:10:29 - 00:10:46] Okay, so if we think of a torch,
[00:10:46 - 00:10:49] when you turn your torch,
[00:10:49 - 00:10:50] you get this pattern,
[00:10:50 - 00:10:51] the beam pattern,
[00:10:51 - 00:10:53] and it's generally strongest on axis,
[00:10:53 - 00:10:56] the direction you're pointing the beam,
[00:10:56 - 00:11:00] and then it decays away off axis.
[00:11:00 - 00:11:05] So this is the same with sonar or radar,
[00:11:05 - 00:11:06] or lighter,
[00:11:06 - 00:11:09] I'm not sure why I was left off there.
[00:11:09 - 00:11:11] And so,
[00:11:11 - 00:11:14] again, a signal is strongest on axis.
[00:11:14 - 00:11:17] If we consider,
[00:11:17 - 00:11:18] say,
[00:11:18 - 00:11:22] a rectangular transducer here,
[00:11:22 - 00:11:25] so this is our transducer,
[00:11:25 - 00:11:29] and it's got a width capital D.
[00:11:29 - 00:11:37] Okay, so this would also be then for radar signal,
[00:11:37 - 00:11:39] the width of the,
[00:11:39 - 00:11:42] or the linear dimension of the n,
[00:11:42 - 00:11:44] and tina,
[00:11:44 - 00:11:47] or the lighter,
[00:11:47 - 00:11:49] there would be the,
[00:11:49 - 00:11:51] the lens,
[00:11:51 - 00:11:53] the beam diameter of the laser.
[00:11:53 - 00:11:58] Okay, so we can define something called the,
[00:11:58 - 00:12:01] aperture,
[00:12:01 - 00:12:03] transmittance,
[00:12:03 - 00:12:08] function,
[00:12:08 - 00:12:12] or so this is a,
[00:12:12 - 00:12:13] the function of x,
[00:12:13 - 00:12:18] and so here we've got a rectangular function,
[00:12:18 - 00:12:21] this transducer is rectangular,
[00:12:21 - 00:12:26] and it's a function of how wide
[00:12:26 - 00:12:31] that transducer is.
[00:12:31 - 00:12:39] Okay, and so,
[00:12:39 - 00:12:40] our transducer is here,
[00:12:40 - 00:12:42] and then we're generating a wave,
[00:12:42 - 00:12:45] or beam in this direction,
[00:12:45 - 00:12:48] and we have our,
[00:12:48 - 00:12:54] angle of the beam is an angle of the cetera here.
[00:12:54 - 00:13:10] This would be here, theta.
[00:13:10 - 00:13:18] Okay, so we've got this rectangular function here,
[00:13:18 - 00:13:22] so it's between D over two,
[00:13:24 - 00:13:26] so this is very relaxed,
[00:13:26 - 00:13:28] and minus D over two,
[00:13:28 - 00:13:31] we have a value of our aperture transmittance of one,
[00:13:31 - 00:13:33] otherwise it has a value of zero.
[00:13:33 - 00:13:43] Okay, so we want to go through all the maths of this,
[00:13:43 - 00:13:48] but what happens is that we get a Fourier transform
[00:13:49 - 00:13:53] relationship between our aperture transmittance function,
[00:13:55 - 00:13:58] and then the beam pattern.
[00:13:59 - 00:14:01] So, for our own equation here,
[00:14:01 - 00:14:03] for our beam patterns,
[00:14:03 - 00:14:05] we're going to use capital B for the beam pattern,
[00:14:05 - 00:14:08] and we're going to write it as an angle theta.
[00:14:08 - 00:14:21] Okay, and so the Fourier transform of this rectangular function,
[00:14:21 - 00:14:26] our aperture transmittance from having a rectangular transducer,
[00:14:27 - 00:14:31] is then we're going to have a oscillation shape,
[00:14:31 - 00:14:36] beam pattern, same, yeah.
[00:14:36 - 00:14:40] So, because Fourier transform of a rect is a sigma,
[00:14:40 - 00:14:43] and well, I'll draw the sigma down along here,
[00:14:43 - 00:14:47] so our beam pattern is going to be,
[00:14:47 - 00:14:50] we can write this as D,
[00:14:50 - 00:14:52] so it was the width of our transducer,
[00:14:52 - 00:14:58] times sigma of D sin theta over x,
[00:14:59 - 00:15:10] and then we'll draw a single function at the bottom here,
[00:15:10 - 00:15:14] so we've got our main load of our sigma function,
[00:15:14 - 00:15:30] and then we've got recurring side loads as well.
[00:15:30 - 00:15:35] Okay, so we'll define the width of this main load here.
[00:15:36 - 00:15:46] Well, the 3D B width is approximately equal to lambda,
[00:15:46 - 00:15:49] the wavelength over D,
[00:15:49 - 00:15:51] the width of our transducer,
[00:15:51 - 00:15:53] or the width of our radar dish,
[00:15:53 - 00:15:55] or the width of our telescope.
[00:15:55 - 00:16:01] Okay, so these six,
[00:16:01 - 00:16:06] are crossing at then lambda over D,
[00:16:06 - 00:16:08] two lambda over D,
[00:16:08 - 00:16:12] three lambda over D, four lambda over D,
[00:16:12 - 00:16:15] this is minus lambda over D,
[00:16:15 - 00:16:18] minus two lambda over D,
[00:16:18 - 00:16:28] minus three lambda over D, et cetera.
[00:16:28 - 00:16:32] Okay, so the 3D B width of our sin function
[00:16:32 - 00:16:35] is defined as approximately lambda over D,
[00:16:35 - 00:16:38] the full width of the sin function,
[00:16:38 - 00:16:41] so that's from the first negative zero crossing,
[00:16:41 - 00:16:43] to the first positive zero crossing,
[00:16:43 - 00:16:48] is then two lambda over D.
[00:16:48 - 00:17:13] Okay, so let's look at some of these,
[00:17:13 - 00:17:17] being patterns or getting a couple of being patterns on the next slide.
[00:17:17 - 00:17:20] So we've got this sort of sin, like behavior.
[00:17:20 - 00:17:26] I know this last night when I was preparing that I'd written 3D B
[00:17:26 - 00:17:29] as a capital D, so if you downloaded your
[00:17:29 - 00:17:34] slide this today, or you paid it this today,
[00:17:34 - 00:17:37] you might want to cross that out and there'll be.
[00:17:37 - 00:17:43] Okay, so we've got here,
[00:17:43 - 00:17:48] so this is then these are width of our transducer,
[00:17:48 - 00:17:55] so the black thing here is our transducer,
[00:17:55 - 00:17:59] and it has width D,
[00:17:59 - 00:18:03] so we have a sin function that blue is the beam pattern.
[00:18:03 - 00:18:13] Okay, so we've got these side lobes,
[00:18:13 - 00:18:19] you can see here, and then this is our main lobe.
[00:18:19 - 00:18:32] Okay, and so going from the top figure to the bottom figure,
[00:18:32 - 00:18:37] our transducer with D is constant,
[00:18:37 - 00:18:47] so if we have the frequency,
[00:18:47 - 00:18:54] that means we then double the wavelength lambda,
[00:18:54 - 00:19:07] and so our beam width is approximately equal to lambda over the D,
[00:19:07 - 00:19:13] so our beam width, if we double lambda,
[00:19:13 - 00:19:24] doubles our beam width.
[00:19:24 - 00:19:25] Okay, so it's twice, I think.
[00:19:25 - 00:19:32] So you can see there in the bottom figure that the main lobe
[00:19:32 - 00:19:45] and also these side lobes have been got wider.
[00:19:45 - 00:19:52] So this in black top of the diagram,
[00:19:52 - 00:20:01] oh, so that's a here,
[00:20:01 - 00:20:05] bandwidth is lambda over D,
[00:20:05 - 00:20:08] but because we've doubled lambda,
[00:20:08 - 00:20:10] the beam width will be twice.
[00:20:10 - 00:20:11] Yeah, yeah.
[00:20:11 - 00:20:12] Yeah, the bottom one is...
[00:20:12 - 00:20:20] Yeah, the lambda's changed, the thing.
[00:20:20 - 00:20:24] Yeah, so here, lambda over D is...
[00:20:24 - 00:20:25] Okay, but I'll...
[00:20:25 - 00:20:34] Okay, lambda, yeah, so the one's in black,
[00:20:34 - 00:20:38] the one's in black are showing the full beam width,
[00:20:38 - 00:20:44] so that's the distance between the zero crossings.
[00:20:44 - 00:20:46] So that's the full width,
[00:20:46 - 00:20:51] and then what I've run here is that the lambda over D
[00:20:51 - 00:20:56] is the 3 dB, which is what people normally use.
[00:20:56 - 00:21:02] Okay, good.
[00:21:02 - 00:21:09] All right, and so just another note.
[00:21:09 - 00:21:14] So if we're going, some distance are here along,
[00:21:14 - 00:21:22] the beam width at range,
[00:21:22 - 00:21:33] but w is equal to lambda over D,
[00:21:33 - 00:21:35] so that's the width of the beam,
[00:21:35 - 00:21:40] and then because it's growing as we go with distance R,
[00:21:40 - 00:21:42] as lambda over D times R.
[00:21:42 - 00:22:17] Okay, so this lambda over D gives us our beam width
[00:22:17 - 00:22:23] or resolution, if we're thinking about a camera.
[00:22:23 - 00:22:33] So we've got three different examples here of different systems.
[00:22:33 - 00:22:38] So start off with that tweet of a dario's view.
[00:22:38 - 00:22:40] Here we go, the waffle tweeter,
[00:22:40 - 00:22:42] waffle does the low frequencies,
[00:22:42 - 00:22:45] tweet of as the higher frequencies.
[00:22:45 - 00:22:52] And so if we use typical values for frequency and wave length,
[00:22:52 - 00:22:57] and the size of the tweeter,
[00:22:57 - 00:23:00] we get an angle there of about 130 degrees.
[00:23:00 - 00:23:11] So for a stereo, actually we want a large angle,
[00:23:11 - 00:23:19] and a lambda over D, just spread sound.
[00:23:19 - 00:23:21] Okay, so if you've got your stereo,
[00:23:21 - 00:23:24] you don't want to just have a narrow beam that only one person can hear.
[00:23:24 - 00:23:27] You want a large angle, so you run in the room,
[00:23:27 - 00:23:31] can hear it.
[00:23:31 - 00:23:40] Okay, but then for the camera,
[00:23:40 - 00:23:45] for a camera, we want to have a larger angle,
[00:23:45 - 00:23:53] for a smaller angle, for a better resolution.
[00:23:53 - 00:24:07] Okay, so for a camera,
[00:24:07 - 00:24:15] so 600 nanometers here, this is visible light.
[00:24:15 - 00:24:20] So if we want a better resolution lambda over D,
[00:24:20 - 00:24:24] we have to make D larger.
[00:24:24 - 00:24:33] So D there is the diameter of the main lens of the camera.
[00:24:33 - 00:24:35] So if we want better resolution,
[00:24:35 - 00:24:37] not just digital resolution,
[00:24:37 - 00:24:39] the pixels are actual optical resolution,
[00:24:39 - 00:24:44] being able to distinguish two points along just the way,
[00:24:44 - 00:24:49] then we need a bigger lens in our camera.
[00:24:49 - 00:24:51] So this is true.
[00:24:51 - 00:24:54] If you remember my first lecture I talked about,
[00:24:54 - 00:24:57] I'd worked on large telescopes,
[00:24:57 - 00:24:59] and at the moment,
[00:24:59 - 00:25:01] they'd built in the largest telescope in the world in Chile,
[00:25:01 - 00:25:03] which I'd worked on for a bit.
[00:25:03 - 00:25:05] And then D is going to be 40 meters,
[00:25:05 - 00:25:10] the diameter of the main mirror of the telescope.
[00:25:10 - 00:25:14] So that layer of the D gives you your resolution,
[00:25:14 - 00:25:16] you make D really big.
[00:25:16 - 00:25:18] That means you can resolve two points.
[00:25:18 - 00:25:20] So two stars, when you first together,
[00:25:20 - 00:25:22] or star, and it's a planet,
[00:25:22 - 00:25:25] you can resolve them if you have a large diameter.
[00:25:25 - 00:25:28] They won't be on top of each other.
[00:25:28 - 00:25:34] So that's why this D is really important in the denominator.
[00:25:34 - 00:25:45] Okay, so let's do a little problem here.
[00:25:45 - 00:25:50] So we're going to calculate the lens dimension for a lighter.
[00:25:50 - 00:25:52] So a small size of one millimeter,
[00:25:52 - 00:25:54] and a distance of a kilometer.
[00:25:54 - 00:25:58] And I'm going to assume that we're invisible light 600 nanometers.
[00:25:58 - 00:26:03] Okay, so we've got our lens here.
[00:26:03 - 00:26:08] So this is a distance D,
[00:26:08 - 00:26:14] and we want to resolve,
[00:26:14 - 00:26:21] sort of a spot size of one millimeter,
[00:26:21 - 00:26:29] and our range here,
[00:26:29 - 00:26:32] one kilometer.
[00:26:32 - 00:26:40] Okay, lander is 600 nanometers.
[00:26:40 - 00:26:51] Okay, so if we use an equation from a couple of slides,
[00:26:51 - 00:26:58] you know, before so we've got our beam width is equal to lander over D.
[00:26:58 - 00:27:00] If we multiply that by the range,
[00:27:00 - 00:27:03] that's going to give us our spot size.
[00:27:03 - 00:27:11] So if we rearrange this equation,
[00:27:11 - 00:27:24] we'll have our lens dimension D is equal to then lander times our overall spot size W.
[00:27:24 - 00:27:38] So this then becomes 600 nanometers times one kilometer over our spot size,
[00:27:38 - 00:27:48] which is one millimeter to D is then equal to 0.6 meters.
[00:27:48 - 00:27:50] Okay, so that's a massive,
[00:27:50 - 00:27:52] that's like a telescope on top of Mount John.
[00:27:52 - 00:27:57] So this is not realizable and a commercial system.
[00:27:57 - 00:27:59] Realizable.
[00:27:59 - 00:28:42] Okay, so lastly, we'll just look at your light out for the rubber cup.
[00:28:42 - 00:28:45] So the BL53,
[00:28:45 - 00:28:48] hello X is a ton of flight sensor,
[00:28:48 - 00:28:53] and a simple laser diode at 940 nanometers.
[00:28:53 - 00:28:57] So lander is 940,
[00:28:57 - 00:29:00] so that's in the mirror infrared.
[00:29:00 - 00:29:17] Okay, so when we receive the light back to the sensor,
[00:29:17 - 00:29:21] a photodiode,
[00:29:21 - 00:29:26] then we'll emit an electron when it detects a photon.
[00:29:26 - 00:29:34] And so then these sensors have arranged typically up to 2 meters,
[00:29:34 - 00:29:46] and in terms of interfacing with the rest of your robot,
[00:29:46 - 00:29:53] the output of the sensor is a digital signal,
[00:29:53 - 00:29:58] this is a digital output,
[00:29:58 - 00:30:03] which then interfaces by the i-squared C serial communications protocol.
[00:30:03 - 00:30:15] Okay, so that was the ton of flight sensor.
[00:30:15 - 00:30:21] The other one we're going to look at is a train g
[00:30:21 - 00:30:25] or range sensor.
[00:30:25 - 00:30:30] So we'll do that to finish the lecture.
[00:30:30 - 00:30:34] Okay, so with ton of flight,
[00:30:34 - 00:30:37] we were measuring a time that gave us a distance.
[00:30:37 - 00:30:39] With the range sensor,
[00:30:39 - 00:30:41] we're going to measure an angle,
[00:30:41 - 00:30:46] which is going to give us a distance.
[00:30:46 - 00:30:50] So we're going to use infrared light,
[00:30:50 - 00:30:52] and we're going to measure an angle.
[00:30:52 - 00:30:55] So what we've got here in this schematic,
[00:30:55 - 00:31:00] so 101 here is our laser diode.
[00:31:00 - 00:31:04] So that's generating our signal.
[00:31:04 - 00:31:07] And then 102 is our detector,
[00:31:07 - 00:31:16] so this is known as a position sensitive detector,
[00:31:16 - 00:31:25] which is somewhat confusing,
[00:31:25 - 00:31:27] because we've had another piece in the scores,
[00:31:27 - 00:31:30] which was the power spectral density.
[00:31:30 - 00:31:33] So we've got two of those,
[00:31:33 - 00:31:35] somehow at the same course.
[00:31:35 - 00:31:39] Okay, so then we've got here,
[00:31:39 - 00:31:44] 133 here is our lens,
[00:31:44 - 00:31:46] which forms our beam,
[00:31:46 - 00:31:54] and then we've got 138 here
[00:31:54 - 00:31:59] as a lens to focus the beam on the detector.
[00:31:59 - 00:32:04] And we've got two things here.
[00:32:04 - 00:32:07] We'll call this object one,
[00:32:07 - 00:32:09] and object two.
[00:32:09 - 00:32:15] Okay, so we'll do this in a couple of colors.
[00:32:15 - 00:32:17] So object one,
[00:32:17 - 00:32:21] we're going to create our laser here.
[00:32:21 - 00:32:25] It's reflecting off this object,
[00:32:25 - 00:32:40] and then we're going to hit the bottom of the detector.
[00:32:40 - 00:32:45] Okay, and then we'll do the further away object.
[00:32:45 - 00:32:46] I've got object two here,
[00:32:46 - 00:32:52] so I'll just draw the red and parallel with the blue here.
[00:32:52 - 00:32:54] And this, okay,
[00:32:54 - 00:32:58] and then reflect off object two,
[00:32:58 - 00:33:01] and then just by drawing straight lines,
[00:33:01 - 00:33:06] we are going to end up with our focused beam
[00:33:06 - 00:33:11] from lens 138 on a different position
[00:33:11 - 00:33:14] on our detector.
[00:33:14 - 00:33:20] So the angle where the light has the detector
[00:33:20 - 00:33:22] gives us the range.
[00:33:22 - 00:33:36] Let's all to do with these triangles.
[00:33:36 - 00:33:38] Okay, so we'll look at the next slide,
[00:33:38 - 00:33:40] which has the same figure,
[00:33:40 - 00:33:44] and we'll just generate an equation for
[00:33:44 - 00:33:51] how we can work out the range from where it hits the detector.
[00:33:51 - 00:33:53] So it's the same figure,
[00:33:53 - 00:33:56] but we'll just define a few things here.
[00:33:56 - 00:33:58] So we'll just write this up again.
[00:33:58 - 00:34:01] So with the laser,
[00:34:01 - 00:34:02] diode,
[00:34:02 - 00:34:10] we've got our detector here,
[00:34:10 - 00:34:12] our PSD.
[00:34:12 - 00:34:15] And so this distance between the two
[00:34:15 - 00:34:16] is our,
[00:34:16 - 00:34:17] we call D,
[00:34:17 - 00:34:19] our lens separation.
[00:34:19 - 00:34:31] So we'll consider the further away object.
[00:34:31 - 00:34:34] This is our range,
[00:34:34 - 00:34:40] our,
[00:34:40 - 00:34:44] the distance between the lens and the detector
[00:34:44 - 00:34:47] is F,
[00:34:47 - 00:34:49] which is the focal length of the lens,
[00:34:49 - 00:34:50] 1-38,
[00:34:50 - 00:35:08] and then the last thing we have is the distance X here.
[00:35:08 - 00:35:12] Right over here,
[00:35:12 - 00:35:15] this is X,
[00:35:15 - 00:35:24] this is the displacement of the spot.
[00:35:24 - 00:35:28] From the center of the PSD,
[00:35:28 - 00:35:30] center of the detector.
[00:35:30 - 00:35:53] Okay, so we want to work out our F and D constants,
[00:35:53 - 00:35:59] and then X is our measured parameter.
[00:35:59 - 00:36:07] Okay, so from these four distances,
[00:36:07 - 00:36:10] we can do some maths.
[00:36:10 - 00:36:13] So we've got two triangles,
[00:36:13 - 00:36:15] which are similar dimensions.
[00:36:15 - 00:36:18] So we can write X,
[00:36:18 - 00:36:21] it's a small triangle,
[00:36:21 - 00:36:24] X over F is equal to then
[00:36:24 - 00:36:28] to the large triangle D over R.
[00:36:28 - 00:36:36] So X is then equal to
[00:36:36 - 00:36:40] the focal length of the lens,
[00:36:40 - 00:36:44] times the distance between the lens,
[00:36:44 - 00:36:45] the,
[00:36:45 - 00:36:47] the diode and the,
[00:36:47 - 00:36:50] the detector divided by the range.
[00:36:50 - 00:37:32] Because this is going to give us our displacement on the PSD.
[00:37:32 - 00:37:33] So our detector,
[00:37:33 - 00:37:35] this PSD,
[00:37:35 - 00:37:38] gives a voltage proportional to the displacement
[00:37:38 - 00:37:40] from the center of the PSD.
[00:37:40 - 00:37:42] So we can write this as an equation.
[00:37:42 - 00:37:47] So our voltage here V
[00:37:47 - 00:37:51] is equal to some constant A times the displacement X
[00:37:51 - 00:37:54] plus some offset B.
[00:37:54 - 00:37:57] So B is an offset.
[00:37:57 - 00:38:00] A is the scanner or constant,
[00:38:00 - 00:38:02] and X is our displacement.
[00:38:02 - 00:38:15] Okay, so the equation we have in the previous slide,
[00:38:15 - 00:38:23] we've got from similar triangles,
[00:38:23 - 00:38:27] was for X.
[00:38:27 - 00:38:30] So then X is equal to F the over R.
[00:38:30 - 00:38:32] So we're going to think of A times
[00:38:32 - 00:38:33] if time,
[00:38:33 - 00:38:35] so the focal length of the lens,
[00:38:35 - 00:38:40] times the distance between the,
[00:38:40 - 00:38:43] what the lens distance is,
[00:38:43 - 00:38:48] over the range R plus B.
[00:38:48 - 00:38:51] So that was using X is equal to,
[00:38:51 - 00:38:52] if the,
[00:38:52 - 00:38:58] okay,
[00:38:58 - 00:39:01] so we can then rewrite this in terms of two different constants.
[00:39:01 - 00:39:05] So the voltage V is in equal to some constant K1
[00:39:05 - 00:39:09] over the range R plus the constant K2.
[00:39:09 - 00:39:24] Okay, so the voltage we get from our detector
[00:39:24 - 00:39:31] is inversely proportional to the range.
[00:39:31 - 00:39:35] So there's a one over R relationship in this last equation
[00:39:35 - 00:39:36] with the voltage.
[00:39:36 - 00:39:47] Okay, so there's two constants,
[00:39:47 - 00:39:49] which we need to work out.
[00:39:49 - 00:39:55] We've got a measure of voltage.
[00:39:55 - 00:39:57] What we want to know is the range R.
[00:39:57 - 00:39:59] We want to know how far away the wall is
[00:39:59 - 00:40:01] that your robot is about to drive into.
[00:40:01 - 00:40:04] So we need to know this K1 and K2,
[00:40:04 - 00:40:08] and we can work those out from calibration.
[00:40:08 - 00:40:13] So we can measure for a number of different ranges
[00:40:13 - 00:40:17] what the voltages are.
[00:40:17 - 00:40:20] So those are the blue dots.
[00:40:20 - 00:40:22] So this is on the right here.
[00:40:22 - 00:40:25] We're plotting against R on the left.
[00:40:25 - 00:40:27] We've got one over R.
[00:40:27 - 00:40:29] So we see we've got these black dots.
[00:40:29 - 00:40:35] So blue dots are our measured range
[00:40:35 - 00:40:39] and voltage values.
[00:40:39 - 00:40:50] And so to get the calibration, we least squares.
[00:40:50 - 00:40:56] So curve fitting, and we do that using the curve on the left
[00:40:56 - 00:40:59] which we plot against one over R
[00:40:59 - 00:41:01] because what's straight line is easy to fit.
[00:41:01 - 00:41:08] That's straight line, then it is to fit a one over R curve.
[00:41:08 - 00:41:12] So let me out here.
[00:41:12 - 00:41:14] We do the calibration here.
[00:41:14 - 00:41:16] We get K1 and K2.
[00:41:16 - 00:41:19] And then when we get a new voltage measure,
[00:41:19 - 00:41:22] we can use that equation to then work out
[00:41:22 - 00:41:27] how far away an object is.
[00:41:27 - 00:41:43] So then lastly, we'll just finish on the sharp
[00:41:43 - 00:41:45] infrared range sensors.
[00:41:45 - 00:41:47] So it's in the robot cup kit.
[00:41:47 - 00:41:54] There are four different choices for these that you can choose between.
[00:41:54 - 00:41:57] So they have different parameters.
[00:41:57 - 00:42:04] So in particular, the lens separation means the range
[00:42:04 - 00:42:08] is going to be different.
[00:42:08 - 00:42:12] And then the other key thing here is that this is
[00:42:12 - 00:42:17] the output from these range sensors is an analog voltage,
[00:42:17 - 00:42:21] which then goes to an ADC of a microcontroller.
[00:42:21 - 00:42:27] So it's different to the time of flight since we looked at before,
[00:42:27 - 00:42:35] which was a digital output, which was then zero transmitted
[00:42:35 - 00:42:38] by a two C.
[00:42:38 - 00:42:44] So for the robot cup, you have to choose one of these four,
[00:42:44 - 00:42:46] or you don't have to use it,
[00:42:46 - 00:42:48] or I can just use it.
[00:42:48 - 00:42:51] So it's not a budget involved with choosing.
[00:42:51 - 00:42:54] All right.
[00:42:54 - 00:42:55] OK.
[00:42:55 - 00:42:56] Yeah.
[00:42:56 - 00:42:57] Yeah.
[00:42:57 - 00:43:03] Yeah.
[00:43:03 - 00:43:04] So yeah, exactly.
[00:43:04 - 00:43:06] So I mean, it's serial communication,
[00:43:06 - 00:43:08] and those bits will then tell you that the distance.
[00:43:08 - 00:43:13] Yeah.
[00:43:13 - 00:43:14] Good.
[00:43:14 - 00:43:15] So that's all I have for today.
[00:43:15 - 00:43:18] So tomorrow, I'll give a bit of a briefing at this moment.
[00:43:18 - 00:43:25] I've got a few less than 10 slides on oscilloscopes and multi-meters.
[00:43:25 - 00:43:30] And I can bring a previous test to me and go through some questions as well.
[00:43:30 - 00:43:31] So yeah.
[00:43:31 - 00:43:36] So we'll finish there because apparently I've got a test on.
[00:43:36 - 00:43:40] I wonder how many times I've got a tutorial.
[00:43:40 - 00:43:44] But yeah.
[00:43:44 - 00:43:46] Well, that one's been so far.
[00:43:46 - 00:43:48] Let's go to something else.
[00:43:48 - 00:43:49] OK.
[00:43:49 - 00:43:50] Good.
[00:43:50 - 00:43:53] So good luck for tonight, and I'll see you tomorrow for the last one.
[00:43:53 - 00:43:54] Thank you.
[00:43:54 - 00:44:07] Is that what I'm using?
[00:44:07 - 00:44:13] Like, with the increase in range, does that affect the accuracy?
[00:44:13 - 00:44:15] Yeah.
[00:44:15 - 00:44:16] Yeah.
[00:44:16 - 00:44:17] Well, we can turn it over.
[00:44:17 - 00:44:19] It'll be kind of a single threshold, I think.
[00:44:19 - 00:44:20] Yeah.
[00:44:20 - 00:44:23] So yeah, the further away you are, the precision.
[00:44:23 - 00:44:25] I've just seen the trial.
[00:44:25 - 00:44:26] OK.
[00:44:26 - 00:44:27] Awesome.
[00:44:27 - 00:44:33] I think we're going to do a full-length.
[00:44:33 - 00:44:35] I'm going to put a metric in my eye.
[00:44:35 - 00:44:39] Because it might have been a cool and a checkered.
[00:44:39 - 00:44:40] Yeah.
[00:44:40 - 00:44:42] But it's probably a very, very, very small.
[00:44:42 - 00:44:55] And some of the things that we'll just paste into, I don't do it right.

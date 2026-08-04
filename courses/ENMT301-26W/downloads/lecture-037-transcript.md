# ENMT301-26W Lecture 37 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `[local source path redacted]`
Source audio SHA-256: `250d2a9a29f3dbe7e39731c99285e8b757524fb5c6531743a77e703c99d73a15`
Generated: 2026-06-06T06:27:58.151334+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:04 - 00:00:12] Hello everyone, I'm Richard Claire, you should all know me from Nt260 from last year.
[00:00:12 - 00:00:14] I recognize some of your faces.
[00:00:14 - 00:00:19] Someone can teach you in Nt301 this term, signals and sensors.
[00:00:19 - 00:00:25] So, signal processing and then also some sensors.
[00:00:25 - 00:00:32] Hopefully this information will then be useful for you in your robot designing.
[00:00:32 - 00:00:35] In the second half of the year.
[00:00:35 - 00:00:40] So, I'll just start off with a couple of examples of signals.
[00:00:40 - 00:00:43] Do you like to click it?
[00:00:43 - 00:00:44] Probably just me.
[00:00:44 - 00:00:46] Oh, one, good.
[00:00:46 - 00:00:51] Okay, so, promises is my only correct example for the course.
[00:00:51 - 00:00:55] So, in cricket you got a bat, you're trying to ball.
[00:00:55 - 00:00:59] And what happens is sometimes you can just get a little hit.
[00:00:59 - 00:01:03] And the umpires don't know whether you're out or not.
[00:01:03 - 00:01:06] And so, people sometimes cheat and don't walk off.
[00:01:06 - 00:01:10] So, what they do in international cricket is they have a sensor,
[00:01:10 - 00:01:13] which they stick in one of these stumps.
[00:01:13 - 00:01:17] So, we've got a sensor which is a microphone.
[00:01:17 - 00:01:24] And so, the microphone is picking up a sound.
[00:01:24 - 00:01:29] The sound is, if the ball just hits the bat,
[00:01:30 - 00:01:33] then there'll be some circuitry that will be an amplifier.
[00:01:33 - 00:01:36] To amplify the voltage from the microphone,
[00:01:36 - 00:01:41] and then go into, through an L of the digital converter,
[00:01:41 - 00:01:44] into the microprocessor, and then microprocessor,
[00:01:44 - 00:01:47] and then microprocessor, there might be some filtering.
[00:01:47 - 00:01:52] And then in the end we get our signal.
[00:01:52 - 00:01:53] Okay?
[00:01:53 - 00:01:58] And so, the signal is then the sound of the ball heading the bat.
[00:01:58 - 00:02:00] And the process signal of the signal,
[00:02:00 - 00:02:03] and current games, is the umpires look to that.
[00:02:03 - 00:02:05] Biali is, oh yeah.
[00:02:05 - 00:02:07] There's some signal there.
[00:02:07 - 00:02:08] It's above a threshold.
[00:02:08 - 00:02:10] I'll give the batsman out.
[00:02:10 - 00:02:11] Okay?
[00:02:11 - 00:02:13] So, it's an example of a sensor.
[00:02:13 - 00:02:15] And then the signal you get from the sensor.
[00:02:15 - 00:02:18] And then the one on the right.
[00:02:18 - 00:02:20] Who has a heart?
[00:02:20 - 00:02:21] All of you.
[00:02:21 - 00:02:24] So, we're in a inclusive example.
[00:02:24 - 00:02:29] Okay, so the one on the right is an echo-cardiogram at ECG.
[00:02:29 - 00:02:33] Okay, so I've had one on these before.
[00:02:33 - 00:02:36] So, this stick, some electrodes to you.
[00:02:36 - 00:02:43] And then measuring your heart beat.
[00:02:43 - 00:02:50] And so each of these characteristic peaks is one heart beat.
[00:02:50 - 00:02:55] So, then a cardiologist would look at this signal
[00:02:55 - 00:02:58] out of those electrodes and the amplifiers, et cetera.
[00:02:58 - 00:03:03] And then they will be able to detect whether there's some arrhythmia
[00:03:03 - 00:03:07] or some other heart defect.
[00:03:07 - 00:03:13] Okay, but so one of the things with an ECG is you can have noise and interference.
[00:03:13 - 00:03:21] So, if you are in a room with just wine and the walls, et cetera,
[00:03:21 - 00:03:25] or the close to devices that have mains voltage,
[00:03:25 - 00:03:32] so that's 240 volts, your body is going to pick up that 240 volts,
[00:03:32 - 00:03:37] 50 Hertz through parasitic capacitance.
[00:03:37 - 00:03:44] And so, on the top signal here, you can see some sort of high frequency noise.
[00:03:44 - 00:03:49] There's also the noise of the electronics, the resistors, the opamps,
[00:03:49 - 00:03:52] and the oscillator, the oscillator, the oscillator,
[00:03:52 - 00:03:56] and the oscillator, the oscillator, the oscillator,
[00:03:56 - 00:04:00] and the oscillator, the oscillator, and the oscillator.
[00:04:00 - 00:04:07] So, the signal is going to be a couple of weeks of filters.
[00:04:07 - 00:04:11] This term, the top graph there is where it's noisy,
[00:04:11 - 00:04:14] and the bottom one is where we've filtered out
[00:04:14 - 00:04:20] that 50 Hertz interference that we're picking up from the mains.
[00:04:20 - 00:04:23] So, we're going to do analog filters.
[00:04:23 - 00:04:28] So, when we have filters made out of inductors, resistors, capacitors,
[00:04:28 - 00:04:34] and also digital filters, it's a filtering we do within the microcontroller.
[00:04:34 - 00:04:40] Okay, so it's a little overview of what we're going to do over the next six weeks.
[00:04:40 - 00:04:46] And so, I'll just go start my lecture with a bit of admin,
[00:04:46 - 00:04:51] sort of stuff for the term.
[00:04:51 - 00:04:53] So, I'm teaching in term two.
[00:04:53 - 00:04:58] I'm up on the fifth floor of link building, and you can reach me by email.
[00:04:58 - 00:05:03] And so, I'm going to teach this course the way I taught the embedded systems part of 260 last year,
[00:05:03 - 00:05:09] is that I have these power points, these PDFs, that I'll put on learn before the lecture,
[00:05:09 - 00:05:15] and then during the lecture, I'll do my annotations, write equations down,
[00:05:15 - 00:05:18] point out the key things in the graphs, etc.
[00:05:18 - 00:05:24] And then after the lecture, I'll post those PDFs to learn.
[00:05:24 - 00:05:27] Okay, so, there are also different ways to deal with this.
[00:05:27 - 00:05:30] So, lots of people will make their own notes on their tablets,
[00:05:30 - 00:05:33] or some people print them out and fill them in my hand.
[00:05:33 - 00:05:35] There's not that much on my slides generally,
[00:05:35 - 00:05:40] or they'll have them quite clean, so you can also write down, you know, it's yourself.
[00:05:40 - 00:05:45] And you can also, if you want, just use my notes that I put up on learn,
[00:05:45 - 00:05:51] but then you have to deal with my handwriting, and you get more out of it.
[00:05:51 - 00:05:57] If you write your own notes, you process it as we go.
[00:05:57 - 00:06:04] And so, on learn as well, I've started a formula sheet for the test,
[00:06:04 - 00:06:10] which occurs in the midyear exam period.
[00:06:10 - 00:06:18] So, the way the test is going to run is, I give it a formula sheet with every possible formula that you could use,
[00:06:18 - 00:06:20] but there's no cheat sheet.
[00:06:20 - 00:06:28] Okay, so there's a slight change from previous years.
[00:06:28 - 00:06:32] This is my first year teaching this course.
[00:06:32 - 00:06:35] I've taught the following course,
[00:06:35 - 00:06:42] an electrical engineering course, ENEO420, which is advanced equipment processing for about the last 10 years.
[00:06:42 - 00:06:47] But I no longer teach ENEO260, thankfully.
[00:06:47 - 00:06:50] And I now have a much smaller class.
[00:06:50 - 00:06:55] I don't have 450 students in 260, and they'll have fun problems to deal with.
[00:06:55 - 00:07:02] So, I have, instead, now some teaching in the first semester.
[00:07:02 - 00:07:09] Okay, so just a little bit about me and my engineering work and research.
[00:07:09 - 00:07:17] So, I do signal processing, and the signals I deal with, two-dimensional signals or images.
[00:07:17 - 00:07:23] And so, my PhD, and then I work for about 10 years overseas in the US and Germany,
[00:07:23 - 00:07:28] was an image processing for large telescopes,
[00:07:28 - 00:07:33] in particular to overcome the blurring effect of the atmosphere.
[00:07:33 - 00:07:36] So, when we go to telescope on the ground,
[00:07:36 - 00:07:42] and we're looking up through the Earth's atmosphere at some object-size star,
[00:07:42 - 00:07:45] the image we get on the ground is blurry.
[00:07:45 - 00:07:50] That's because the Earth's atmosphere consists of random airy,
[00:07:50 - 00:07:56] it is of light of different temperature, which means it's got different reflector index.
[00:07:56 - 00:08:01] It's a light that comes down through the atmosphere, gets the stored head or bent.
[00:08:01 - 00:08:06] And that means the images we take with the telescope on the ground are blurred.
[00:08:06 - 00:08:09] So, you can overcome this by putting a telescope in the space,
[00:08:09 - 00:08:13] like Hubble or James Webb, but that's incredibly expensive.
[00:08:13 - 00:08:21] So, a cheaper way of doing this on the ground is to then, in the feedback loop,
[00:08:21 - 00:08:26] we have the figure on the top left, we have a sensor,
[00:08:26 - 00:08:35] which is an optical sensor to measure the distortion that light goes through as it passes through the atmosphere.
[00:08:35 - 00:08:41] And then we have a, this thing here, down here, is a deformal mirror.
[00:08:41 - 00:08:52] And so, that is a mirror that we can change the shape of the mirror at hundreds of times per second.
[00:08:52 - 00:08:58] So, there are these actuators on the bottom actuators.
[00:08:58 - 00:09:03] And so, by changing the voltage to the actuator, we can push and pull them up and down,
[00:09:03 - 00:09:08] that changes the shape of the mirror, and we can then perfectly compensate,
[00:09:08 - 00:09:12] well, not perfectly, we can compensate for the effect of the atmosphere.
[00:09:12 - 00:09:16] So, we've got distorted light coming down from the atmosphere,
[00:09:16 - 00:09:21] when it heads out of the form of a mirror, it bounces off again and it becomes planar,
[00:09:21 - 00:09:25] which means we don't have any distortion.
[00:09:25 - 00:09:32] Okay, so we've got our sensor, we've got some sort of signal that we measure with the sensor
[00:09:32 - 00:09:38] and a signal that we then pass to this deformal mirror.
[00:09:38 - 00:09:48] Okay, so, this is me, that's on the summit of Monocaya and Hawaii, where I worked for about a year.
[00:09:48 - 00:09:54] And then these two telescopes behind me, the two largest telescopes in the world at the time,
[00:09:54 - 00:09:56] the kick of symmetry.
[00:09:56 - 00:09:59] And so, it's about 4,000 meters up.
[00:09:59 - 00:10:06] So, you have the telescope on top of the mountain, so you've got less of the atmospheric blur and...
[00:10:06 - 00:10:13] And so, then I went to Germany and I was working on the signal processing and sensors
[00:10:13 - 00:10:18] for the extremely large telescope, which will be the world's largest telescope,
[00:10:18 - 00:10:22] that's being built in the outer camera desert until eight at the moment.
[00:10:22 - 00:10:32] Okay, so then the example that's top right is showing the image on the left is the center of our galaxy
[00:10:32 - 00:10:40] without doing this signal processing, this control loop that happens on the right is with the signal processing,
[00:10:40 - 00:10:46] where we have a much cleaner image, we've been able to remove some of this atmospheric blurring
[00:10:46 - 00:10:50] with our signal processing and control loop.
[00:10:50 - 00:10:55] Okay, so there's just a bit about why...
[00:10:55 - 00:11:01] ...or what I do and why I'm teaching this course.
[00:11:01 - 00:11:05] Okay, so, enemy T3, I like this big course at 30 points.
[00:11:05 - 00:11:09] It's got lots of different learning outcomes.
[00:11:09 - 00:11:14] On one hand, you're learning about ball bearings and I'm going to be teaching you about 40 transforms.
[00:11:14 - 00:11:18] So, it has quite a range of things.
[00:11:18 - 00:11:24] When I was the third-year mechatronic scorebed, it was very hard to find for people who are going overseas
[00:11:24 - 00:11:30] in exchange course, that would be remotely similar, it would be filled by two different courses.
[00:11:30 - 00:11:37] Anyway, the relevant learning outcomes for energy 301 that we're going to be applying signal processing techniques
[00:11:37 - 00:11:45] and time frequency domains, so that's using Laplace and Fourier transforms to analyze data from one or more sensors.
[00:11:45 - 00:11:53] And so we're going to design and implement both analog and digital filters to condition signals,
[00:11:53 - 00:12:00] to remove noise and interference in particular.
[00:12:00 - 00:12:07] Okay, so the relevant assessments for my teaching, we've got this test in the mid-year exam period.
[00:12:07 - 00:12:09] It's worth 30% of the course.
[00:12:09 - 00:12:16] And this is a 30 point course, so that's effectively worth 60% of a 15 point course.
[00:12:16 - 00:12:22] And so that's signals and sensors is worth me.
[00:12:22 - 00:12:29] And then there is some material from Chris Pretty on design in the test as well.
[00:12:29 - 00:12:34] So we'll give you more information about the test later in the term.
[00:12:34 - 00:12:39] Okay, and obviously you can't use AI tools in a test.
[00:12:39 - 00:12:48] And then my other assessment is an IMU assignment, so this is a type of sensor.
[00:12:48 - 00:12:54] And I'll give you some measurements and then you have to do some filtering on those measurements.
[00:12:54 - 00:12:59] And so this is a 5% assessment and it's due.
[00:12:59 - 00:13:03] I think that's the end of the second week of term three.
[00:13:03 - 00:13:06] So it's in the second semester.
[00:13:06 - 00:13:09] You can start it in the after the exams.
[00:13:09 - 00:13:13] And you've got a couple of weeks at the start of opt-in three to work on it as well.
[00:13:13 - 00:13:19] And so for this assessment, we do allow restricted use of AI tools.
[00:13:19 - 00:13:24] And so the basic idea is we want you to do the assignment yourself.
[00:13:24 - 00:13:27] And then use the AI tools to tidy it up.
[00:13:27 - 00:13:35] So you write it yourself, you then get it to improve your spelling, grammar, critique, your writing.
[00:13:35 - 00:13:37] You can also use it as a research tool.
[00:13:37 - 00:13:38] It's point number two.
[00:13:38 - 00:13:48] And you can also use it to debug your code and help you improve your filter implementations.
[00:13:48 - 00:13:56] Okay, so the schedule we have, we've got three lectures.
[00:13:56 - 00:13:59] So four o'clock and router here.
[00:13:59 - 00:14:04] And then we're lecture tomorrow in A3 and election Friday also in A3.
[00:14:04 - 00:14:10] And then on Thursdays, we have a tutorial straight after the lecture.
[00:14:10 - 00:14:19] I decided not to have a tutorial this week because we wrote enough material to have a meaningful set of questions.
[00:14:19 - 00:14:29] And then like with ENC 260 last year, I'll have some sort of tutorial in the study week to refer you for the test as well.
[00:14:29 - 00:14:36] Okay, so I'll just say plus tutorial in the study week.
[00:14:36 - 00:14:44] Okay, so the way the tutorials work each week, there'll be a set of problems.
[00:14:44 - 00:14:50] If you work on those and I'll be there with the TA, we'll come round and answer your questions.
[00:14:50 - 00:14:55] It's also a chance for you to ask questions about the lecture content as well.
[00:14:55 - 00:14:58] So these are not assessed.
[00:14:58 - 00:15:03] I think in the age of AI, giving marks is something that an AI could do reasonably well.
[00:15:03 - 00:15:08] As a bit pointless, it's about for you to learn.
[00:15:08 - 00:15:11] And the tutorials are not recorded either.
[00:15:11 - 00:15:13] It's not me at a friend working on problems.
[00:15:13 - 00:15:16] It'd be like the ENC 260 tutorial last year.
[00:15:16 - 00:15:19] We work on the problems.
[00:15:19 - 00:15:24] So you're active rather than passively listening to me again.
[00:15:24 - 00:15:33] Okay, so I've put here kind of the weekly topics.
[00:15:33 - 00:15:38] So I'm not going to have an individual topic for each lecture.
[00:15:38 - 00:15:42] It gets quite hard to manage the exactly 50 minutes for a particular topic.
[00:15:42 - 00:15:48] So I'm sort of writing my lecture slides in big chunks.
[00:15:48 - 00:15:50] And so I've put up there.
[00:15:50 - 00:15:53] So for this week, we're doing signals and noise.
[00:15:53 - 00:15:55] Now we're going to take us about a week.
[00:15:55 - 00:15:59] Then we'll go on to Laplace transforms and Fourier transforms,
[00:15:59 - 00:16:02] then analog filters.
[00:16:02 - 00:16:06] And then we're going to move into the digital domain to look at the digital transforms,
[00:16:06 - 00:16:11] which are a digital form of Laplace and Fourier transforms.
[00:16:11 - 00:16:14] And then designing digital filters.
[00:16:14 - 00:16:17] I will go to the sampling process and the screw for the transforms.
[00:16:17 - 00:16:19] That's also on the digital domain.
[00:16:19 - 00:16:23] And then the last section will be on different types of sensors.
[00:16:23 - 00:16:28] So, SONAR, SUSOUND navigation ranging,
[00:16:28 - 00:16:34] radar, radio detection ranging, and LIDAR, which is light detection and ranging.
[00:16:34 - 00:16:37] I'll also talk a bit about the SELUS scopes.
[00:16:37 - 00:16:43] So the last section is the most directly applicable to your robot cup.
[00:16:43 - 00:16:50] And so I'm going to take the SELUS assignment.
[00:16:50 - 00:16:54] OK. So this is my first year teaching the course.
[00:16:54 - 00:16:58] Michael Hayes taught this course for about last ten years.
[00:16:58 - 00:17:00] So I've got his notes.
[00:17:00 - 00:17:02] And then I'm, which was kind of a booklet,
[00:17:02 - 00:17:07] but I prefer to have these slides I can annotate.
[00:17:07 - 00:17:12] And so I'm taking most of my material from his coursebook.
[00:17:12 - 00:17:17] And I'm taking the original engineering signal processing course.
[00:17:17 - 00:17:22] I'm taking some stuff from there as well as what I think is important.
[00:17:22 - 00:17:25] And making my own notes.
[00:17:25 - 00:17:29] And so my notes are kind of bullet point ones.
[00:17:29 - 00:17:30] If you want some more information,
[00:17:30 - 00:17:35] there are plenty of signal processing textbooks in the engineering and physical science libraries.
[00:17:35 - 00:17:40] I've highlighted to that I appropriate for this course as well.
[00:17:40 - 00:17:49] OK. So I think I saw and learned the other way that you were going to get your
[00:17:49 - 00:17:52] robot cup kits today or this week or something.
[00:17:52 - 00:17:57] So this is a little out of date.
[00:17:57 - 00:18:02] But last year, I'm not sure how much has changed the SELUS year.
[00:18:02 - 00:18:07] But these are the senses that you're given to the robot cup.
[00:18:07 - 00:18:09] There's lots of them.
[00:18:09 - 00:18:13] And so these all produce signals.
[00:18:13 - 00:18:16] These signals that get from these senses are going to have noise.
[00:18:16 - 00:18:20] So we're going to have to, well, in the robot cup, you're going to have to analyze
[00:18:20 - 00:18:25] these signals, filter them, possibly, and to rate them possibly.
[00:18:25 - 00:18:31] So that's also one of the underlying motivations for this block of teaching on signal processing.
[00:18:31 - 00:18:37] OK. And so this was the full list.
[00:18:37 - 00:18:42] Here of the senses.
[00:18:42 - 00:18:47] So there's various infrared and ultrasonic sensors.
[00:18:47 - 00:18:52] And then the one that I will highlight is the IMU.
[00:18:52 - 00:18:59] So this one here, M IMU BNO-055.
[00:18:59 - 00:19:06] And this is the one we're going to use in the IMU assignment.
[00:19:06 - 00:19:22] OK. So does anyone have any admin-type questions before we start doing this?
[00:19:22 - 00:19:23] No.
[00:19:23 - 00:19:25] OK.
[00:19:25 - 00:19:33] So what we need to do to start is to refine what a signal is.
[00:19:33 - 00:19:36] OK.
[00:19:36 - 00:19:38] So it's a single-valued function.
[00:19:38 - 00:19:47] So it can't take on multiple different values at the same point in time of one or more independent
[00:19:47 - 00:19:48] variables.
[00:19:48 - 00:19:55] So typically, we're looking at something like the output of sensor, which is a voltage signal
[00:19:55 - 00:19:56] as a function of time.
[00:19:56 - 00:19:59] So we've got V of T.
[00:19:59 - 00:20:08] OK. So that's a function of one variable T.
[00:20:08 - 00:20:12] OK. So that's an example of an output.
[00:20:12 - 00:20:15] We can also have the input to an actuator.
[00:20:15 - 00:20:20] So they are my overall mirror from the second or third slide.
[00:20:20 - 00:20:24] And that is a voltage signal as well as a function of time.
[00:20:24 - 00:20:32] And the signal processing is important to many of the sub-disciplines of megatronics.
[00:20:32 - 00:20:44] So the control system, you're feeding back a signal from your sensor to your controller.
[00:20:44 - 00:20:59] In robotics, you need to send signals about how you move your actuators, PWM signals for the motors, etc.
[00:20:59 - 00:21:06] So an imaging system, the signals can be two dimensional signals.
[00:21:06 - 00:21:15] And so also, say, biomedical sensing, ECG, EEG, the zerol sensors as well.
[00:21:15 - 00:21:22] OK. So it's a signal processing is common to many different fields and megatronics.
[00:21:22 - 00:21:32] OK. So let's go through a signal processing chain.
[00:21:32 - 00:21:35] So we've got some sort of sensor.
[00:21:35 - 00:21:45] Let's say this is our inertial measurement unit for our assignment and your robot.
[00:21:45 - 00:21:54] And I and you is actually about three sensors in one package.
[00:21:54 - 00:22:00] So there's an accelerometer, a gyroscope and a magnetometer.
[00:22:00 - 00:22:03] So it gives you three different signals out of it.
[00:22:03 - 00:22:07] But let's just consider this as one signal at the moment.
[00:22:07 - 00:22:14] OK. So the signal or the sensor can be quite small, small voltages.
[00:22:14 - 00:22:33] And so then to read that into our microcontroller, we want to have an amplifier to then increase our signal to noise ratio.
[00:22:33 - 00:22:39] So to hopefully amplify our signal and reject any common noise.
[00:22:39 - 00:22:46] OK. So through this chain here, so we've got it from our sensor.
[00:22:46 - 00:22:58] Oops. So let's say we've got our voltage V of T.
[00:22:58 - 00:23:03] And then we're going to amplify it by some gain A.
[00:23:03 - 00:23:11] And then before we go into our digital system, our microcontroller say,
[00:23:11 - 00:23:17] we need to pass it through an anti-AIS filter.
[00:23:17 - 00:23:25] We'll talk about AIS and sampling later in the course.
[00:23:25 - 00:23:38] But this filter is obviously to prevent AISing, which occurs from under sampling.
[00:23:38 - 00:23:46] OK. So if we don't take enough sample at a high enough frequency,
[00:23:46 - 00:23:48] we can get AISing.
[00:23:48 - 00:23:51] We can lose some of the high frequency components,
[00:23:51 - 00:23:57] and they get AIS down into lower frequency components.
[00:23:57 - 00:24:05] OK. So let's call the input to our ADC X of N.
[00:24:05 - 00:24:20] So ADC, like we learned in 360 last year, is the analog digital converter.
[00:24:20 - 00:24:29] And then so X of N, with round backouts, is a continuous signal.
[00:24:29 - 00:24:33] And then once we are inside our digital system,
[00:24:33 - 00:24:39] we now have a digital signal with discrete.
[00:24:39 - 00:24:44] So little X of N here with round brackets is continuous.
[00:24:44 - 00:24:49] And then after our analog to digital converter,
[00:24:49 - 00:24:53] we have a discrete or digital signal.
[00:24:53 - 00:25:04] OK. And then we might have in our signal processing chain here,
[00:25:04 - 00:25:08] we might have a digital filter.
[00:25:08 - 00:25:13] And that might be to remove our interference as 50 hertz.
[00:25:13 - 00:25:19] We might pick up from mains, or we might have noise from our electronics.
[00:25:19 - 00:25:27] So the resistors, opamps, et cetera in our circuit, all generate sort of thermal shot,
[00:25:27 - 00:25:31] flicker noise, we'll go through different noise types later in the week.
[00:25:31 - 00:25:37] And so here we have an example of a digital filter in pink.
[00:25:37 - 00:25:42] We can also deal with the noise with an analog filter as well.
[00:25:42 - 00:25:48] So as an example here, the anti-aliased filter will be an analog filter.
[00:25:48 - 00:26:07] OK. So that's the little example here.
[00:26:07 - 00:26:12] So let's say we've got a voltage signal from our sensor.
[00:26:12 - 00:26:14] And it's got some interference.
[00:26:14 - 00:26:24] We want to try and work out what is the voltage signal that's being sort of overwhelmed here by our interference.
[00:26:24 - 00:26:28] OK.
[00:26:28 - 00:26:36] So the interference here is the sort of sign-your-soids.
[00:26:36 - 00:26:42] And the sort of interference.
[00:26:42 - 00:26:46] So you don't know the frequency of this interference.
[00:26:46 - 00:26:54] I won't say the accounting, but there's 50 cycles here.
[00:26:54 - 00:27:03] And this is a one here in one second.
[00:27:03 - 00:27:06] So that means we have a 50 hertz interference.
[00:27:06 - 00:27:10] OK.
[00:27:10 - 00:27:12] So the interference is the sign-your-soil.
[00:27:12 - 00:27:16] But we also see some bits around here in particular.
[00:27:16 - 00:27:20] We can visually see some of the underlying signal.
[00:27:20 - 00:27:32] So there is something visible here in the signal.
[00:27:32 - 00:27:33] OK.
[00:27:33 - 00:27:40] So in order to get rid of our interference,
[00:27:40 - 00:27:45] we know it's the sign wave of a particular frequency.
[00:27:45 - 00:27:47] We can then design a filter.
[00:27:47 - 00:27:50] It's got a notch filter or band stop filter.
[00:27:50 - 00:27:56] Or we just filter out all frequency components at 50 hertz.
[00:27:56 - 00:28:06] And so if we do that, we can then get our underlying signal.
[00:28:06 - 00:28:07] OK.
[00:28:07 - 00:28:19] So this notch or band stop filter removes the interference.
[00:28:19 - 00:28:27] And then we have our underlying signal.
[00:28:27 - 00:28:27] OK.
[00:28:27 - 00:28:33] So the underlying signal here has much smaller energy than the interference.
[00:28:33 - 00:28:36] So we go back here basically all the power.
[00:28:36 - 00:28:42] Energy is in the sign-your-soil cosine there.
[00:28:42 - 00:28:45] But because this is purely deterministic,
[00:28:45 - 00:28:47] if we take out the 50 hertz component,
[00:28:47 - 00:28:51] we can get our underlying signal.
[00:28:51 - 00:28:55] So that's what's the filtering.
[00:28:55 - 00:29:05] So what can we say about our signal here?
[00:29:05 - 00:29:06] What?
[00:29:06 - 00:29:08] Let's run an equation for us.
[00:29:08 - 00:29:11] So what do we notice about the signal?
[00:29:11 - 00:29:17] What can you say about the signal?
[00:29:17 - 00:29:18] Yes.
[00:29:18 - 00:29:20] It's exponentially decaying.
[00:29:20 - 00:29:24] So I've got three different things as part of this equation.
[00:29:24 - 00:29:29] So it's got an exponential term or write this in the middle here.
[00:29:29 - 00:29:37] And so it's got a sigma of minus 10.
[00:29:37 - 00:29:42] What else can we say about this signal?
[00:29:42 - 00:29:43] Yes, it's got the late start.
[00:29:43 - 00:29:51] So we can write that using our unit step or heapside function,
[00:29:51 - 00:29:53] which we call u.
[00:29:53 - 00:29:55] And so this is starting at, that's one.
[00:29:55 - 00:29:57] This is 0.2.
[00:29:57 - 00:30:00] So we go u of t minus 0.2.
[00:30:00 - 00:30:03] This is the unit step.
[00:30:03 - 00:30:08] And this is also the exponential as delay by 0.2.
[00:30:08 - 00:30:15] And then what's the last part of the signal?
[00:30:15 - 00:30:19] So we've got this exponential decay that
[00:30:19 - 00:30:20] late start here.
[00:30:20 - 00:30:24] But we also have some sine-usoidal part as well.
[00:30:24 - 00:30:33] So we can write that then as sine of 2 pi and then
[00:30:33 - 00:30:43] it's got a frequency of 10 and it's also delayed by t minus 0.2.
[00:30:43 - 00:30:44] OK.
[00:30:44 - 00:30:50] So for the next week, we're going to be classifying and writing
[00:30:50 - 00:30:51] our signal.
[00:30:51 - 00:30:55] So we've got our sine, our unit step, and also an exponential term
[00:30:55 - 00:31:00] 2.
[00:31:00 - 00:31:05] And once we can write our signals in terms of these sorts of
[00:31:05 - 00:31:08] components, then we can take the past transforms and for
[00:31:08 - 00:31:17] our transforms of them to look at their frequency components.
[00:31:17 - 00:31:17] OK.
[00:31:17 - 00:31:23] So that was adding interference.
[00:31:23 - 00:31:26] This example here, we're adding white Gaussian noise for the
[00:31:26 - 00:31:30] signal of 0.1.
[00:31:30 - 00:31:40] So the signal business here is that's the standard deviation of
[00:31:40 - 00:31:49] our noise.
[00:31:49 - 00:32:02] White noise means that it has a flat spectrum or it's all frequencies.
[00:32:02 - 00:32:05] Light consists of all the different colors of light.
[00:32:05 - 00:32:14] White noise is then has a constant power spectrum.
[00:32:14 - 00:32:14] OK.
[00:32:14 - 00:32:26] So this is then quite high frequency noise compared to our original
[00:32:26 - 00:32:35] signal.
[00:32:35 - 00:32:42] So we can remove most of that noise, but not all that with a low
[00:32:42 - 00:32:43] pass filter.
[00:32:43 - 00:32:50] So we're going to use a low pass filter.
[00:32:50 - 00:32:53] Alt Pf.
[00:32:53 - 00:32:58] And a simple way to make a low pass filter is just average
[00:32:58 - 00:33:03] over the previous here eight samples.
[00:33:03 - 00:33:09] So if we average all these bits here, it's going to tend towards
[00:33:09 - 00:33:10] 0.
[00:33:10 - 00:33:13] So the effect of doing this averaging is going to smooth out our
[00:33:13 - 00:33:17] curve.
[00:33:17 - 00:33:17] OK.
[00:33:17 - 00:33:27] So this removes most of the noise that it was easier to
[00:33:27 - 00:33:31] remove the interference than the noise.
[00:33:31 - 00:33:56] OK.
[00:33:56 - 00:34:01] So an example that I've mentioned before on the title slide was
[00:34:01 - 00:34:05] that we get with an ECG from these electrodes attached to your
[00:34:05 - 00:34:09] chest is voltage signal.
[00:34:09 - 00:34:13] Use the voltage signal to diagnose hard conditions.
[00:34:13 - 00:34:15] But it can be corrupted by 50 hertz mains in the
[00:34:15 - 00:34:23] appearance from this device here will be connected up to 50 hertz
[00:34:23 - 00:34:24] voltage.
[00:34:24 - 00:34:26] You're not actually that far away from it.
[00:34:26 - 00:34:30] There'll be some parasitic capacitance between you and the
[00:34:30 - 00:34:32] device.
[00:34:32 - 00:34:39] And there'll also be measurement noise in the electronics in
[00:34:39 - 00:34:46] the ECG device as well.
[00:34:46 - 00:34:47] OK.
[00:34:47 - 00:34:49] So we can remove the interference with a notch, a
[00:34:49 - 00:34:50] band stop filter.
[00:34:50 - 00:34:55] So that's a filter where the notch is sent to the 50 hertz for
[00:34:55 - 00:35:00] our mains frequency.
[00:35:00 - 00:35:04] And then we can remove the high frequency noise from the
[00:35:04 - 00:35:07] electronics.
[00:35:07 - 00:35:15] So we've got here this sort of noise and interference on the
[00:35:15 - 00:35:16] top.
[00:35:16 - 00:35:24] So this is noisy on the top and filtered on the bottom.
[00:35:24 - 00:35:24] OK.
[00:35:24 - 00:35:28] And on the left here we have what the typical heartbeat looks
[00:35:28 - 00:35:31] like in terms of its ECG signal.
[00:35:31 - 00:35:37] And then it's easier in the filtered version on the bottom
[00:35:37 - 00:35:41] where it removes the noise and the interference for then
[00:35:41 - 00:35:45] the cardiologist to then be able to see where these are
[00:35:45 - 00:36:05] SQ&T parts of the heartbeat waveform.
[00:36:05 - 00:36:05] OK.
[00:36:05 - 00:36:10] So most of the signals we'll be dealing with in this course,
[00:36:10 - 00:36:12] not all the signals we'll be dealing with in this course are
[00:36:12 - 00:36:14] going to be one dimensional.
[00:36:14 - 00:36:21] So we're going to be dealing with mostly voltage as a
[00:36:21 - 00:36:24] function of time.
[00:36:24 - 00:36:27] But we can do a single process thing.
[00:36:27 - 00:36:32] We can do a Fourier transform of two dimensional signals.
[00:36:32 - 00:36:38] So the one on the left here, this is from my research,
[00:36:38 - 00:36:39] this is a phase screen.
[00:36:39 - 00:36:43] This is a mount that the light gets delayed as it passes
[00:36:43 - 00:36:45] through the atmosphere.
[00:36:45 - 00:36:48] But the important thing here is it's a function of two variables,
[00:36:48 - 00:36:50] x and y.
[00:36:50 - 00:36:55] So x say in this direction y in this direction.
[00:36:55 - 00:36:57] And so then when we analyze these signals,
[00:36:57 - 00:37:00] we need a two dimensional Fourier transform rather than a
[00:37:00 - 00:37:03] one dimensional Fourier transform.
[00:37:03 - 00:37:05] And we can also have three dimensional signals.
[00:37:05 - 00:37:09] So you might have say a movie, it's called an M,
[00:37:09 - 00:37:16] which is then a function of three variables, x, y, and T
[00:37:16 - 00:37:20] or we might have a three dimensional volume.
[00:37:20 - 00:37:22] So the example here is ocean salinity.
[00:37:22 - 00:37:26] So how salty the water is.
[00:37:26 - 00:37:28] And so then it's called salinity.
[00:37:28 - 00:37:34] Yes, this is a function of x, y, and z.
[00:37:34 - 00:37:37] OK, with z is going to be the depth.
[00:37:37 - 00:37:41] OK, so this course we're just going to do one dimensional
[00:37:41 - 00:37:43] one.
[00:37:43 - 00:37:46] There's an elective for you next year, any of 420 that I
[00:37:46 - 00:37:51] teach into where we deal with two dimensional signals and
[00:37:51 - 00:37:58] signal processing.
[00:37:58 - 00:38:02] OK, so we're now going to go through and classify some of the
[00:38:02 - 00:38:09] main functions we will use in our signal processing.
[00:38:09 - 00:38:13] And so we do analog and digital.
[00:38:13 - 00:38:18] And so analog signals like the one shown here,
[00:38:18 - 00:38:20] functions of continuous time.
[00:38:20 - 00:38:24] So they define for all values of time T and they've got
[00:38:24 - 00:38:29] continuous values for their voltage.
[00:38:29 - 00:38:35] OK, so our voltage in our circuit, so the voltage to
[00:38:35 - 00:38:39] a resistor is a continuous signal.
[00:38:39 - 00:38:46] OK, so the example here we've got some voltage V of T.
[00:38:46 - 00:38:50] OK, and we can write this then as our amplitude here to
[00:38:50 - 00:39:00] be, times the sign of 2 pi and the period here is 6.
[00:39:00 - 00:39:06] So we can write this as sign of 2 pi T over 6.
[00:39:06 - 00:39:13] OK, so the important thing with analog signals is then time is
[00:39:13 - 00:39:24] a member of real numbers and our voltage V of T is also a
[00:39:24 - 00:39:36] member of real numbers.
[00:39:36 - 00:39:41] OK, we're also going to be looking at digital signals.
[00:39:41 - 00:39:45] And so these are function of discrete time.
[00:39:45 - 00:39:50] So here instead of on the x-axis having T, we've now got in,
[00:39:50 - 00:39:52] we're in as our sample number.
[00:39:52 - 00:39:55] So we've sampled it in time.
[00:39:55 - 00:40:05] And we now have, so here in as the sample number.
[00:40:05 - 00:40:11] And we have quantized it in value.
[00:40:11 - 00:40:20] So we only have discrete values for our voltage.
[00:40:20 - 00:40:28] So here we've got five different voltage levels.
[00:40:28 - 00:40:32] And for that we would need at least three that's in our
[00:40:32 - 00:40:41] microcontroller.
[00:40:41 - 00:40:45] OK, so digital signal is sampled in time in quantized in
[00:40:45 - 00:40:47] value.
[00:40:47 - 00:40:53] And then in our sample number is a member of Z,
[00:40:53 - 00:40:56] which is integers.
[00:40:56 - 00:41:04] And our quantized voltage VQ of in the square brackets is
[00:41:04 - 00:41:11] also a member of integers.
[00:41:11 - 00:41:20] OK, and this way of drawing a digital signal here or
[00:41:20 - 00:41:27] quantized signal is called a lollipop plot.
[00:41:27 - 00:41:33] So that's during a stalk was the actual value as a circle on
[00:41:33 - 00:41:37] the top.
[00:41:37 - 00:41:40] OK, so it's analog digital.
[00:41:40 - 00:41:46] We can also have two sort of hybrid forms where we can have
[00:41:46 - 00:41:50] continuous values.
[00:41:50 - 00:42:00] But sample in time, I guess here we continuous in value,
[00:42:00 - 00:42:11] but here sampled in time.
[00:42:11 - 00:42:21] And so in this case we have our voltage signal V of n is real,
[00:42:21 - 00:42:26] but our samples are integers.
[00:42:26 - 00:42:33] OK, so this hybrid approach that's somewhere between analog
[00:42:33 - 00:42:36] and digital is more of a conceptual rather than a
[00:42:36 - 00:42:41] practical signal that you'll come across.
[00:42:41 - 00:42:45] And then the last of the possible combinations is the opposite
[00:42:45 - 00:42:52] to this one if we're continuous in time and discrete values.
[00:42:52 - 00:42:54] So we've quantized in value.
[00:42:54 - 00:42:59] So we've got these five different steps again, but we're
[00:42:59 - 00:43:05] continuous in time.
[00:43:05 - 00:43:25] So in this case we have our signal VQ of T integer, but our
[00:43:25 - 00:43:43] time values are real.
[00:43:43 - 00:43:46] So now we're just going to get through today.
[00:43:46 - 00:43:52] There's today and tomorrow some of the common functions that
[00:43:52 - 00:43:56] we will need to use these six weeks.
[00:43:56 - 00:44:00] And so to continuous time signals, we are going to use
[00:44:00 - 00:44:03] lower case letters with round brackets.
[00:44:03 - 00:44:08] So we'll use uppercase letters for our Fourier transforms and
[00:44:08 - 00:44:12] Laplace transforms next week.
[00:44:12 - 00:44:17] And so for example, V of T will be a voltage in the circuit
[00:44:17 - 00:44:23] as function of time T. If we want a particular point in time,
[00:44:23 - 00:44:28] so the voltage at time T is 0 as written as either V of 0 or
[00:44:28 - 00:44:32] at another time T naught, we have V of T naught for a particular
[00:44:32 - 00:44:40] time.
[00:44:40 - 00:44:45] So we'll start off with a DC signal.
[00:44:45 - 00:44:50] So we can write this simply then a voltage V of T is equal to
[00:44:50 - 00:45:03] some constant A. This is just a constant value.
[00:45:03 - 00:45:06] OK, so is this realizable?
[00:45:06 - 00:45:08] Is this actually possible?
[00:45:08 - 00:45:16] No, I'll take those to check in the head.
[00:45:16 - 00:45:19] No, because this would mean that actually it's defined for all
[00:45:19 - 00:45:20] values of time.
[00:45:20 - 00:45:24] So it can't go forever.
[00:45:24 - 00:45:36] So we can use it to model a battery say, but it's not really
[00:45:36 - 00:45:43] physically realizable as it would mean it was always on.
[00:45:43 - 00:45:45] So what we would do normally is we would have the unit step
[00:45:45 - 00:45:49] function u of T, which would mean we turn the battery on at
[00:45:49 - 00:45:56] T is 0.
[00:45:56 - 00:46:04] OK, so that's DC signal alternating current AC.
[00:46:04 - 00:46:08] So that's a cosine function here.
[00:46:08 - 00:46:16] So we've got then our voltage V of T if it's a cosine to how
[00:46:16 - 00:46:21] many different parameters do we have to define this cosine
[00:46:21 - 00:46:26] function 1.
[00:46:26 - 00:46:29] So we've got 2.
[00:46:29 - 00:46:32] So we've got amplitude.
[00:46:32 - 00:46:36] We've got our frequency, but we also have some phase shift
[00:46:36 - 00:46:37] or call 5.
[00:46:37 - 00:46:45] So if we shift our cosine wave in time, then that would be
[00:46:45 - 00:46:46] another parameter as well.
[00:46:46 - 00:46:58] So we've got amplitude A times the cosine of 2 pi if not T.
[00:46:58 - 00:47:03] So if not is our frequency.
[00:47:03 - 00:47:11] And then we've got plus 5 with 5 is the phase shift.
[00:47:11 - 00:47:30] So it's got 3 parameters.
[00:47:30 - 00:47:35] OK, we'll also make use of the exponential function.
[00:47:35 - 00:47:40] So in this case, we can write our voltage signal V of T is
[00:47:40 - 00:47:46] some amplitude A times e to the minus alpha T.
[00:47:46 - 00:47:56] So here we've got 2 parameters, which are A and alpha.
[00:47:56 - 00:47:56] OK.
[00:47:56 - 00:48:02] So if alpha is greater than 0, what's going to happen?
[00:48:02 - 00:48:06] It's going to go down decay.
[00:48:06 - 00:48:11] And if alpha is less than 0, what's going to happen?
[00:48:11 - 00:48:13] Yeah, it's going to rise up.
[00:48:13 - 00:48:23] So it's going to be increasing, which means it is unstable.
[00:48:23 - 00:48:25] It's not going to design a circuit where the voltage gets
[00:48:25 - 00:48:32] larger and larger and larger with time.
[00:48:32 - 00:48:32] OK.
[00:48:32 - 00:48:35] We'll finish off with one last one, which is the unit step.
[00:48:35 - 00:48:36] It already talked about.
[00:48:36 - 00:48:38] So this is a mathematician's call.
[00:48:38 - 00:48:43] This is a heavey side function.
[00:48:43 - 00:48:44] So this is going to be the unit step.
[00:48:44 - 00:48:56] So V of T here is equal to U of T, U for unit.
[00:48:56 - 00:49:04] And this is good for when we have a switch in our circuit.
[00:49:04 - 00:49:20] So this, for example, would model a switch closed at T equals 0.
[00:49:20 - 00:49:21] OK.
[00:49:21 - 00:49:24] So tomorrow, we've still got a couple of these signals
[00:49:24 - 00:49:28] to define in analog and digital space.
[00:49:28 - 00:49:32] Then we're going to start looking at noise.
[00:49:32 - 00:49:35] How noise appears in a circuit.
[00:49:35 - 00:49:38] And how we can calculate how much noise there is.
[00:49:38 - 00:49:43] And then we'll look at interference and how that arises
[00:49:43 - 00:49:45] in our circuits as well.
[00:49:45 - 00:49:45] OK.
[00:49:45 - 00:49:47] So I'll see you tomorrow in A3.
[00:49:47 - 00:49:54] And I'll put these lecture notes up online shortly.
[00:51:31 - 00:51:36] Yes.
[00:51:36 - 00:51:37] Yes.
[00:51:37 - 00:51:38] Yes.
[00:51:38 - 00:51:41] No, I love this.
[00:51:41 - 00:51:42] Do this.
[00:51:42 - 00:51:43] Do this.
[00:51:43 - 00:51:45] I'm here.
[00:51:45 - 00:51:46] I'm here.
[00:51:46 - 00:51:47] I'm here.
[00:51:47 - 00:51:48] I'm here.
[00:51:48 - 00:51:49] I'm here.
[00:51:49 - 00:51:50] I'm here.
[00:51:50 - 00:51:51] You're going to put it up.
[00:51:51 - 00:51:52] I'm here.
[00:51:52 - 00:51:54] I'm on my property, sure.
[00:51:54 - 00:51:55] I'm here.
[00:51:55 - 00:51:56] I'm here.
[00:51:56 - 00:51:57] I'm here before.
[00:51:57 - 00:51:58] Is he even going to?
[00:51:58 - 00:51:59] It's done.
[00:51:59 - 00:52:00] It's getting done.
[00:52:00 - 00:52:01] It's getting done.
[00:52:01 - 00:52:03] It's getting done.
[00:52:03 - 00:52:06] I'm sorry.
[00:52:06 - 00:52:10] I can't wait to see you.
[00:52:10 - 00:52:12] I can't wait.
[00:52:12 - 00:52:25] I don't know.
[00:52:25 - 00:52:26] No, I can't.
[00:52:26 - 00:52:27] I can't.
[00:52:27 - 00:52:28] I can't.
[00:52:28 - 00:52:29] I can't.
[00:52:29 - 00:52:30] I can't.
[00:52:30 - 00:52:31] Yeah.
[00:52:31 - 00:52:32] Yeah.
[00:52:32 - 00:52:32] Oh, I can't.
[00:52:32 - 00:52:33] I can't.
[00:52:33 - 00:52:34] Okay.
[00:52:34 - 00:52:36] My distance is now.
[00:52:36 - 00:52:38] Oh, okay.
[00:52:38 - 00:52:39] Yeah.
[00:52:39 - 00:52:40] Okay.
[00:52:40 - 00:52:44] I'm not gonna say, it's that bite and it's that bite, it's too good.
[00:52:44 - 00:52:49] Ooh.
[00:52:49 - 00:52:52] Top letter?
[00:52:52 - 00:52:53] Just this thing is a little smaller.
[00:52:53 - 00:52:54] It's smaller.
[00:52:54 - 00:52:57] Yeah, it is a little lower.
[00:52:57 - 00:52:59] Then my socks popped up.
[00:52:59 - 00:53:01] He thinks white socks please don't go well.
[00:53:01 - 00:53:02] No.
[00:53:02 - 00:53:03] I always go out.
[00:53:03 - 00:53:04] I don't know.
[00:53:04 - 00:53:05] I don't know.
[00:53:05 - 00:53:07] Look at the baby lady.
[00:53:07 - 00:53:13] The number, the number is Russia says, Happy Birthday to my family.
[00:53:13 - 00:53:15] We are not sure.
[00:53:15 - 00:53:17] Yeah, yeah, we are matching shoes.
[00:53:17 - 00:53:18] I like the shoes.
[00:53:18 - 00:53:19] We're different shoes.
[00:53:19 - 00:53:20] Yeah, we are.
[00:53:20 - 00:53:23] We have completely different shoes for them.
[00:53:23 - 00:53:24] We literally don't.
[00:53:24 - 00:53:25] We're not.
[00:53:25 - 00:53:26] We're not.
[00:53:26 - 00:53:27] We're not.
[00:53:27 - 00:53:28] We're really different.
[00:53:28 - 00:53:29] We're really different.
[00:53:29 - 00:53:30] We're really different.
[00:53:30 - 00:53:31] I'm not going wrong.
[00:53:31 - 00:53:33] Do they like other words?
[00:53:33 - 00:53:34] Mine's obviously not around.
[00:53:34 - 00:53:35] They're different.
[00:53:35 - 00:53:36] They're not.
[00:53:36 - 00:53:37] No, it's not wrong.
[00:53:37 - 00:53:39] She's like, but you're not a really different.
[00:53:39 - 00:53:41] You know, I was lying.
[00:53:41 - 00:53:42] I was trying to make your ball a little bit.
[00:53:42 - 00:53:43] or something.
[00:53:43 - 00:53:45] I don't know why you were the one with the same shoes.
[00:53:45 - 00:53:46] I'm gonna speed.
[00:53:46 - 00:53:47] Yeah, that's a really good point.
[00:53:47 - 00:53:49] Can you show us your fat chocolate sauce?
[00:53:49 - 00:53:51] Yeah, I'm going to put that one.
[00:53:51 - 00:53:52] It's not much.
[00:53:52 - 00:53:53] It's not much.
[00:53:53 - 00:53:54] It's really, really good.
[00:53:54 - 00:53:55] I'm not.
[00:53:55 - 00:53:56] Any hair.
[00:53:56 - 00:53:57] It's a good.
[00:53:57 - 00:53:58] I'm not going to see anything.
[00:53:58 - 00:53:59] Well, it's.
[00:53:59 - 00:54:00] Awesome.
[00:54:00 - 00:54:02] I'm feeling alright.
[00:54:02 - 00:54:03] Oh, sweet.
[00:54:03 - 00:54:04] Sweet.
[00:54:04 - 00:54:06] I'm feeling your joy.
[00:54:06 - 00:54:07] Yeah, it's nice.
[00:54:07 - 00:54:08] What is awesome into AI?
[00:54:08 - 00:54:09] No, I'm not going to.
[00:54:09 - 00:54:11] I was like, that's not going to be.
[00:54:11 - 00:54:12] I mean, I lose.
[00:54:12 - 00:54:13] I know you're such a workbox.
[00:54:13 - 00:54:14] I know.
[00:54:14 - 00:54:15] It was every topic inside fluids.
[00:54:15 - 00:54:16] This is not true.
[00:54:16 - 00:54:19] I did put my answers in board.
[00:54:19 - 00:54:23] I put the practice test and stuff that I didn't feel so comfortable.
[00:54:23 - 00:54:24] It's on.
[00:54:24 - 00:54:25] It's on.
[00:54:25 - 00:54:26] It's a dream.
[00:54:26 - 00:54:29] It doesn't happen.
[00:54:29 - 00:54:30] No, I look.
[00:54:30 - 00:54:31] You know, I look.
[00:54:31 - 00:54:34] Now the desk.
[00:54:34 - 00:54:36] Well, I'll let you in throughout.
[00:54:36 - 00:54:37] It's not going to show that.
[00:54:37 - 00:54:38] I always do.
[00:54:38 - 00:54:39] You'll touch me in here.
[00:54:39 - 00:54:42] you know, catch me in here tonight.
[00:54:42 - 00:54:43] Thank you.
[00:54:43 - 00:54:46] And you didn't bear my teeth in here, but they're not.
[00:54:46 - 00:54:47] Again.
[00:54:47 - 00:54:50] You're watching the
[00:54:50 - 00:54:52] Black Chantum Center where I actually do the same thing as I was in.
[00:54:52 - 00:54:55] Well, I really wanted to teach you my bullets.
[00:54:55 - 00:54:56] I wrote your teeth here.
[00:54:56 - 00:54:57] Yeah.
[00:54:57 - 00:54:58] I didn't see rail.
[00:54:58 - 00:54:59] I don't tell you right now.
[00:54:59 - 00:55:00] I'll read your off range.

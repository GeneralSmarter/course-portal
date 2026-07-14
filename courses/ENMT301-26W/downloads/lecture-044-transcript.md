# ENMT301-26W Lecture 44 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_44_audio_16k_mono_32k.mp3`
Source audio SHA-256: `1a5f827120cacd593fe8a91e95d86ff8ef36fbced81ea585ac3aaa51edf2c8a4`
Generated: 2026-06-06T06:41:18.544931+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:01 - 00:00:04] Okay, good afternoon everyone.
[00:00:04 - 00:00:09] So just start off with a little reminder that immediately following this lecture, we have
[00:00:09 - 00:00:15] a tutorial, which is back in engineering and the data during office.
[00:00:15 - 00:00:20] So there's a set of problems on learn, future workforce, those are kind of several test-type
[00:00:20 - 00:00:21] problems.
[00:00:21 - 00:00:25] And yes, I will post the solutions after the tutorial.
[00:00:25 - 00:00:31] But the idea is you try and go there and do the problems yourself with your colleagues.
[00:00:32 - 00:00:36] Rather than just trying to memorize the solutions I provide you just before the test, because
[00:00:36 - 00:00:40] the questions in the test will be different from the tutorial problems.
[00:00:40 - 00:00:46] So you need to be able to sort of rationally work through a problem rather than just memorize
[00:00:46 - 00:00:48] previous problems.
[00:00:48 - 00:00:56] Okay, so that's in the drawing office and I'll be wondering there after this.
[00:00:56 - 00:01:02] Okay, so today we're going to be finishing off the Laplace transform, which is good to
[00:01:02 - 00:01:05] do in transit and circuit analysis.
[00:01:05 - 00:01:08] And there's also the space that we'll be doing.
[00:01:08 - 00:01:12] Our analog filters and analog filters where we build them out of resistors, capacitors,
[00:01:12 - 00:01:13] and inductors.
[00:01:13 - 00:01:16] So that's all we're doing in the next week.
[00:01:16 - 00:01:21] And then we'll move on to the Fourier transform instead.
[00:01:21 - 00:01:29] So just the basic overview of the Laplace transform from the Fourier slide from yesterday
[00:01:29 - 00:01:34] is that if we have a set of equations in the time domain where we've got integrals and
[00:01:34 - 00:01:38] derivatives, that's quite difficult to solve.
[00:01:38 - 00:01:44] If we take the Laplace transform where you can convert a derivative in time to multiplying
[00:01:44 - 00:01:49] by S and an integral in time as a division base.
[00:01:49 - 00:01:55] So then we have an algebraic equation rather than some sort of integral differential equation.
[00:01:55 - 00:02:02] We can do some manipulations in the Laplace domain to get in the form that we can then use
[00:02:02 - 00:02:11] our known transform tables to convert back to a time domain solution.
[00:02:11 - 00:02:15] So it's easier to go through the fourth Laplace transform and then the inverse Laplace transform
[00:02:15 - 00:02:20] and try and solve a differential equation.
[00:02:20 - 00:02:28] So we were looking at our impedances in the Laplace domain yesterday.
[00:02:28 - 00:02:33] So the impedance of a capacitor in Laplace domain is 1 over SC.
[00:02:33 - 00:02:40] So S is our Laplace transform variable, our complex frequency, and C is the capacitance.
[00:02:40 - 00:02:45] And for resistor, it's R in the time domain as the impedance and it's also R in Laplace
[00:02:45 - 00:02:53] domain which just leaves us with our inductive impedance at Laplace domain.
[00:02:53 - 00:03:02] So in the time domain, our impedance Z is equal to J times our inductive reactance
[00:03:02 - 00:03:03] XL.
[00:03:03 - 00:03:10] This is J on omega L in arms.
[00:03:13 - 00:03:19] Okay, we start off then for the inductor, our governing equation is the voltage.
[00:03:19 - 00:03:29] This differential time is equal to the inductance L times the derivative of the current.
[00:03:29 - 00:03:33] This is the differential time, we'll expect time.
[00:03:33 - 00:03:39] So changing current will produce a voltage through the inductor.
[00:03:39 - 00:03:47] And so then when we convert this to the Laplace domain, we have our voltage V of S is
[00:03:47 - 00:03:55] equal to the inductance L times S times the current and the Laplace domain.
[00:03:55 - 00:04:05] So it's S is a function of S minus our initial current little i of zero.
[00:04:05 - 00:04:13] So this is the initial current.
[00:04:13 - 00:04:22] And so if we have our initial current little i of zero, zero, so we have no current flowing
[00:04:22 - 00:04:31] through our circuit, then our impedance for the inductor, said as the function of S,
[00:04:31 - 00:04:43] which is defined as the voltage divided by the current, is then equal to S times L.
[00:04:43 - 00:04:53] So one over C is our inductance for a capacitor in Laplace domain and S times L is in inductance.
[00:04:53 - 00:04:58] So the impedance for an inductor in the Laplace domain.
[00:04:58 - 00:05:08] So when we're doing our circuit analysis, we'll go back to that circuit.
[00:05:08 - 00:05:16] From yesterday we can use these impedances in our circuit equations in Laplace domain.
[00:05:17 - 00:05:24] Okay, we'll lose these equations a lot next week when we look at analog filters.
[00:05:24 - 00:05:37] Okay, so let's do an example and then we'll go back to our circuit from yesterday.
[00:05:37 - 00:05:41] Okay, so we've got the step function here.
[00:05:41 - 00:05:47] So we're applying a DC voltage of 10 volts to our circuit at time t is zero.
[00:05:47 - 00:05:51] So what is the S domain expression for the voltage signal?
[00:05:51 - 00:05:59] Okay, so let's start off with what our voltage signal is, V of t and the time domain.
[00:05:59 - 00:06:11] So it's our time domain signal going to be the attend, U of t, so it's 10 times the unit step.
[00:06:11 - 00:06:15] Okay, step.
[00:06:15 - 00:06:27] Okay, so then we need to then take the Laplace transform of 10 times the unit step.
[00:06:27 - 00:06:38] So we've got a constant here 10, so then what is our V of S in the Laplace domain?
[00:06:38 - 00:06:44] I'll go back to our table here.
[00:06:44 - 00:06:49] So we have been, we've got a constant.
[00:06:49 - 00:06:54] So this time domain is implying it's just for t greater than zero.
[00:06:54 - 00:07:02] For t less than zero, so the unit step is inherent in all this table.
[00:07:02 - 00:07:07] So the first case here we've got a constant value of k and the time domain.
[00:07:07 - 00:07:17] And so then in the frequency domain, our equation is k divided by S.
[00:07:18 - 00:07:26] Okay, so our V of S signal here is 10 divided by S.
[00:07:26 - 00:07:33] Okay, and then the following question, so actually I'll just write here.
[00:07:33 - 00:07:42] So this is table, since our Laplace transform table and it's here number one.
[00:07:42 - 00:07:44] Okay, so I got that.
[00:07:44 - 00:08:00] And then my following question is what are the units of V of S in one take guess?
[00:08:00 - 00:08:11] There is an element of Hertzmann.
[00:08:11 - 00:08:17] Okay, so if we think about, well, two ways to think about it.
[00:08:17 - 00:08:20] So V of t here, this is in volts.
[00:08:20 - 00:08:23] Okay, so V of t is in volts.
[00:08:23 - 00:08:34] So we've really got volts there and S is equal to sigma plus j omega.
[00:08:35 - 00:08:38] Omega is equal to 2 pi if.
[00:08:38 - 00:08:56] Okay, so the units of S are then frequency that's Hertz all one over second.
[00:08:56 - 00:09:04] Okay, so now units, we've got a volt from our voltage time domain.
[00:09:04 - 00:09:14] And then because we're dividing by S, which has units one over S, we have volts times seconds.
[00:09:14 - 00:09:26] Or the other way to think about it, and you'll have to excuse me here because I'm having a way back to find our Laplace transform equation.
[00:09:26 - 00:09:36] So our F of S here is a V of S. We've got V of t as volts.
[00:09:36 - 00:09:40] And they were integrating with respect to time t here.
[00:09:40 - 00:09:44] So we're multiplying volts by time and seconds.
[00:09:44 - 00:09:46] So it becomes volts seconds.
[00:09:46 - 00:10:05] Okay, so I think we're now really to tackle our circuit in the Laplace domain.
[00:10:05 - 00:10:13] So we tried to see this time domain and we developed this sort of messy differential equation.
[00:10:13 - 00:10:19] But now what we're not trying to do is we're trying to calculate the current flowing in our circuit.
[00:10:19 - 00:10:32] So I of t and we're using Kirchhoff's voltage law where the sum of voltages around the circuit is zero.
[00:10:32 - 00:10:44] Okay, so let's start off with our voltage source, V of t, which is equal to some constant V naught times the unit set U of t.
[00:10:44 - 00:10:50] So the switch gets switched at t is zero.
[00:10:50 - 00:10:56] And so that's why we have this unit set function here because of the switch.
[00:10:56 - 00:11:09] Okay, and so then if we take the Laplace transform of this,
[00:11:09 - 00:11:14] so we're going to do Kirchhoff's voltage law in the Laplace domain.
[00:11:14 - 00:11:24] So our voltage source then becomes an Laplace domain V naught over S.
[00:11:24 - 00:11:34] So that's exactly the same as the big example where V naught was 10 volts from our DC battery.
[00:11:34 - 00:11:41] Okay, so I'll just annotate these as well.
[00:11:41 - 00:11:50] So this was from the Laplace transform tables P01.
[00:11:50 - 00:11:57] Okay, and so then for our voltage drop across the resistor,
[00:11:57 - 00:12:10] from the time domain we have the current as a function of time times the resistance give us our voltage drop across the resistor.
[00:12:10 - 00:12:17] And so in the Laplace domain this becomes I of S times our resistance are.
[00:12:17 - 00:12:24] So from the slide we had to start, the impedance in the,
[00:12:24 - 00:12:31] the positive gain of the resistor is still, okay.
[00:12:31 - 00:12:38] And then for the inductor we have our equation at the time domain L,
[00:12:38 - 00:12:41] the I as a function of t by dt,
[00:12:41 - 00:12:47] we've got the Laplace transform of the positive transform of the positive transform.
[00:12:47 - 00:13:05] We then have the inductance L, S times the current in the Laplace domain I this minus our initial current I zero.
[00:13:05 - 00:13:14] Okay, so we'll do Kirchhoff's voltage law in our circuit and the Laplace domain.
[00:13:14 - 00:13:26] So we've got our voltage supply which has been over S is then equal to the voltage drop across the resistor.
[00:13:26 - 00:13:29] So we've got our current in the time domain.
[00:13:29 - 00:13:34] So what I'm going to do then is solve for our current.
[00:13:34 - 00:13:50] So then capital I this is equal to V naught over S times I of S minus I of zero.
[00:13:50 - 00:13:54] Okay, and so we're trying to find the current in the time domain.
[00:13:54 - 00:13:59] So what I'm going to do then is solve for our current.
[00:13:59 - 00:14:27] And capital I of S is equal to V naught over S plus our inductance L times our initial current I zero divided by S times the inductance L.
[00:14:27 - 00:14:37] Okay, this goes, probably goes over two slides.
[00:14:37 - 00:14:48] So I'll just the next step here is we're going to assume before we push the switch that is no current flowing in the circuit.
[00:14:48 - 00:14:52] So I of zero is zero.
[00:14:52 - 00:14:57] And the next thing we want to do is to manipulate the expression for I of S.
[00:14:57 - 00:15:05] So it's in a form that matches our tables and we can take the inverse Laplace transform easily.
[00:15:05 - 00:15:10] So we're not doing the integrals ourselves.
[00:15:10 - 00:15:12] We're just going to use these tables.
[00:15:12 - 00:15:41] So manipulate to a form in our tables which you can't jump with your pin.
[00:15:41 - 00:15:56] So then we'll go back to our tables and see which property we can use to get this back to the time domain that the inverse Laplace transform.
[00:15:56 - 00:16:04] Okay, so here we've got V naught over S.
[00:16:04 - 00:16:13] The L times I naught is going to disappear if we assume I of zero and was on the bottom of our R plus S L.
[00:16:13 - 00:16:24] Okay, so which one of these peers do you think we should make use of?
[00:16:24 - 00:16:39] Okay, pause again a bit too long.
[00:16:39 - 00:16:43] Okay, so we have an R equation.
[00:16:43 - 00:16:51] We have the V law over S and R plus S L.
[00:16:51 - 00:17:05] So effectively we've got then an S squared L times S R on the bottom.
[00:17:05 - 00:17:14] So this step response here, the one, two, three, four, fifth one down.
[00:17:14 - 00:17:22] We have some constant K over S, some constant tau S plus one.
[00:17:22 - 00:17:30] So this is the one we want to try and manipulate so we can do our inverse Laplace transform.
[00:17:30 - 00:17:45] And then in order to do that manipulation we're going to then multiply from the previous form by S over R.
[00:17:45 - 00:17:58] So that then gives us our current I of S is equal to V naught over R.
[00:17:58 - 00:18:10] Then we've got the denominator S S times L over R plus one.
[00:18:10 - 00:18:32] Okay, so then to get back our current in the time domain we'll use our Laplace transform here number five.
[00:18:32 - 00:18:40] We're our time constant tau is equal to the inductance L over the resistance R.
[00:18:40 - 00:18:45] And then the constant K and the numerator is equal to the V naught.
[00:18:45 - 00:18:52] Our DC voltage divided by R.
[00:18:52 - 00:19:01] Okay, so when we do that the inverse Laplace transform we get back our current in the time domain I of t.
[00:19:01 - 00:19:07] And then from that table we have the K is at the front that's V naught over R.
[00:19:07 - 00:19:20] And then inside the brackets we have one minus into the minus t divided by tau.
[00:19:20 - 00:19:25] So that's divided by L R over L.
[00:19:25 - 00:19:39] Okay, and that's defined for t greater than that, greater than zero.
[00:19:39 - 00:19:44] Or you can write that as by multiplying by unit function u of t.
[00:19:44 - 00:20:01] Okay, so that is hopefully easier than trying to solve that differential equation we had when we tried to catch our solka's law in the time domain.
[00:20:01 - 00:20:05] And we're not doing the integrals in the last domain.
[00:20:05 - 00:20:09] We can just use these tables of standard pairs.
[00:20:09 - 00:20:20] But we do have to have some algebraic manipulation to get our expressions into a form where they match the table.
[00:20:20 - 00:20:24] Okay, so there ends the lesson on Laplace analysis.
[00:20:24 - 00:20:27] And then we're going to move on to Fourier transforms.
[00:20:27 - 00:20:30] So I'll just save this one and open up the next one.
[00:20:30 - 00:20:34] So feel free to chat your neighbor for a minute.
[00:20:34 - 00:21:21] Okay, so the next thing we're going to look at is Fourier transforms.
[00:21:21 - 00:21:27] And Fourier transforms are great for looking at signals in the frequency domain.
[00:21:27 - 00:21:46] And so on the title slide here, we've got red function here that we defined in when we're looking at signals.
[00:21:46 - 00:21:50] That's defined as a value of 1 between minus a half and a half.
[00:21:50 - 00:21:54] And then that has a Fourier transform.
[00:21:54 - 00:22:00] So that's frequency component is given by this sync function, which we'll define later on if you haven't seen a Fourier.
[00:22:00 - 00:22:05] Who's seeing the sync before and that's, or no?
[00:22:05 - 00:22:07] It'll learn something.
[00:22:07 - 00:22:18] Okay, so this rectangular function has a Fourier transform, which is the sync, which has this ringing that goes on for ever.
[00:22:18 - 00:22:21] So the red function is finite in time.
[00:22:21 - 00:22:24] And then the spectrum will be infinite.
[00:22:24 - 00:22:29] So we'll go through and define and derive the sync function later on.
[00:22:29 - 00:22:33] Okay, so Fourier transforms are everywhere.
[00:22:33 - 00:22:43] So I presume in the evibrations courses you have looked at Fourier transforms defined different frequencies.
[00:22:43 - 00:22:45] Yep, good.
[00:22:45 - 00:22:52] But then, I've got lots of other examples on this slide about where we use them.
[00:22:52 - 00:22:54] So vibration analysis.
[00:22:54 - 00:23:02] So, in me, two or three, three or three, four or three, et cetera.
[00:23:02 - 00:23:17] Okay, so you've got, say your propeller, your planes vibrating, and you want to try and work out why you could take a signal of the mode power.
[00:23:17 - 00:23:25] And then look at the frequencies, the resonant frequencies to try and work out what's wrong with your propeller.
[00:23:25 - 00:23:35] Or in my case with designing telescopes, the telescope would vibrate at the wind frequencies of a resonant frequency and harmonics of it.
[00:23:35 - 00:23:39] So we use the Fourier transform for that.
[00:23:39 - 00:23:51] And so, in lots of different imaging modalities, so magneto-residence imaging, this is an MRI scanner on top here.
[00:23:51 - 00:23:55] Computer aided tomography and ultrasound imaging.
[00:23:55 - 00:23:59] I've had two of those three taken in my life.
[00:23:59 - 00:24:02] Various injuries and what have you.
[00:24:02 - 00:24:06] And they all use the Fourier transform.
[00:24:06 - 00:24:16] So computer aided tomography is where you take, like, say x-ray, which is just one angle with computer tomography.
[00:24:16 - 00:24:32] You take images at lots of different angles and then you use Fourier transforms to reconstruct a 3D volume of the body rather than just having a single angle or projection.
[00:24:32 - 00:24:43] So, to say you had, from the x-ray this way, basically a line integral summing up the absorption of the x-ray through the body.
[00:24:43 - 00:24:50] So you might be able to detect that there is a bit of a shrapnel in the body as x-ray goes through.
[00:24:50 - 00:24:57] But you need a 3D volume to work out exactly where that foreign object is.
[00:24:57 - 00:25:02] So the computer aided tomography in the following course, in here for 20.
[00:25:02 - 00:25:05] The sub-mechatonic students take next year.
[00:25:05 - 00:25:16] I teach the math for a transform's behind how they generate these 3D volumes from a number of 2D images.
[00:25:16 - 00:25:21] Okay. And so it's very common in optics as well, which is my field.
[00:25:21 - 00:25:28] Here, the second image down is a diffraction disc.
[00:25:28 - 00:25:39] Okay. So if you take an image with a circular lens or a circular telescope,
[00:25:39 - 00:25:44] you've got no aberrations. You're just taking a perforation.
[00:25:44 - 00:25:49] You will expect from geometric optics. If you focus all the light down to just be a point.
[00:25:49 - 00:25:56] Because of diffraction, the finite size of the aperture, you get this ringing pattern.
[00:25:56 - 00:26:05] And so the circular disc here is the Fourier transform of a circle, which is your lens or your telescope aperture.
[00:26:05 - 00:26:17] So this ringing of a circle here is much like the Fourier transform of this rectangular function on the title slide and we'll get to shortly.
[00:26:17 - 00:26:26] Okay. So in communications, if you think of amplitude modulation or frequency modulation for a and in radio,
[00:26:26 - 00:26:31] they're talking different frequencies. That's all to do with Fourier transform as well.
[00:26:31 - 00:26:44] And then for lots of remote sensing modalities, so radar, it's a radio detection and range finding.
[00:26:44 - 00:26:52] So now from a boat looking down, from sound navigation and ranging,
[00:26:52 - 00:26:59] as well as seismic imaging where you're taking images through the aircraft,
[00:26:59 - 00:27:09] say to look for oil or gas deposits, these processes all make use of the Fourier transform as well.
[00:27:09 - 00:27:20] And in lastly, crystallography, where if you've got some crystal or material and you take lots of images, say in a laser beam,
[00:27:20 - 00:27:28] you can then combine those diffraction images with a Fourier transform to get a 3D structure of the crystal.
[00:27:28 - 00:27:33] Okay, then the third image here is of radio astronomy.
[00:27:33 - 00:27:48] So these telescope dishes, so these are not optical frequencies, but at radio frequencies, and then to increase the resolution of the radio dishes,
[00:27:48 - 00:27:59] we have lots of them. So these are some in the out-counter desert and Chile, where there are dozens of these dishes,
[00:27:59 - 00:28:07] and then you combine the signals from each dish together to increase the resolution, and that's all done with Fourier transforms as well.
[00:28:07 - 00:28:21] Okay, so Fourier transforms are pervasive throughout engineering, not just making the trombonex of electrical engineering.
[00:28:21 - 00:28:27] Okay, so before we do Fourier transforms, we'll start with Fourier series.
[00:28:27 - 00:28:39] And so I've presented Fourier series of emaf to T and something similar to good, so just in three or four slides to redefine Fourier series.
[00:28:39 - 00:28:48] So the Fourier series allows us to decompose a periodic, so it's repeating.
[00:28:48 - 00:28:58] So this is our signal continuous times, it's not discrete, and a repeat over a period T, and that gives us a discrete frequency spectrum.
[00:28:58 - 00:29:09] So we can write our signal in the time domain X of T as some constant value A naught.
[00:29:09 - 00:29:19] So this is our constant DC, and then we have a weighted sum of signs and cosines.
[00:29:19 - 00:29:31] So we're going to do from little pairs one to infinity, we've got A k is our coefficients of the cosine.
[00:29:31 - 00:29:44] cosine 2 pi if naught, which is our fundamental frequency, times the integer k, times time T, and I'm going to call them online.
[00:29:44 - 00:29:51] So I'll just go down here plus then Bk is the coefficient of our signs.
[00:29:51 - 00:30:03] So Bk sine 2 pi if naught kT.
[00:30:03 - 00:30:08] So we can build up any periodic signals, like a square wave or a triangle wave,
[00:30:08 - 00:30:18] is the examples I'll do in the example of slides as a sum of DC term plus the sum of signs and cosines,
[00:30:18 - 00:30:28] and those signs and cosines increase in frequency with this integer k, where k is the case harmonic.
[00:30:28 - 00:30:35] So we can calculate our coefficients.
[00:30:35 - 00:30:51] So our DC constant offset A naught is equal to 1 over the period T times the integral over the period of the signal X of T dT.
[00:30:51 - 00:31:03] So A naught is just the average of the signal over that period.
[00:31:03 - 00:31:33] And then our cosine coefficients A k cos r equal to 2 over the period T, and we've got the integral over that period of our periodic continuous time signal of X of T times the cosine of 2 pi
[00:31:33 - 00:31:39] by if naught kT dT.
[00:31:39 - 00:31:55] So to find each coefficient, we multiply our cosine harmonic by the signal and take the integral over the period,
[00:31:55 - 00:31:59] and then multiply by 2 over T.
[00:31:59 - 00:32:22] And so, similarly, for the sine coefficients, the k is equal to 2 over the period T, the integral over the period T X of T times the sine of 2 pi if naught kT dT.
[00:32:22 - 00:32:41] So the Fourier series only works for a periodic signal, so the signal that repeats the time, and it gives us a spectrum which is discrete.
[00:32:41 - 00:32:45] We've got these coefficients, A k and B k, and that are discrete.
[00:32:45 - 00:32:50] So the coefficient of k is 0, k is 1, k is 2, etc.
[00:32:50 - 00:33:03] So the spectrum is not continuous, unlike the Fourier transform that we'll get to later on.
[00:33:03 - 00:33:06] Can't just make sure everyone's got your equations down.
[00:33:06 - 00:33:07] Looks like it.
[00:33:07 - 00:33:12] So, okay, let's look at our first example, which is our square wave.
[00:33:12 - 00:33:26] So the top of the sub figure here is our square wave, and we want to make up this square wave in terms of a D C term,
[00:33:26 - 00:33:30] sines, and cosines.
[00:33:30 - 00:33:45] Okay, so just considering our square wave at the top, what is our coefficient A 0 going to be?
[00:33:45 - 00:33:46] 0.
[00:33:46 - 00:33:47] Yep, good.
[00:33:47 - 00:33:52] So if we look at one period, say from 0 to...
[00:33:52 - 00:34:00] So what I'm here called T, so that's one period, the average value over that period is 0.
[00:34:00 - 00:34:16] Okay, so this has got no D C, average one period, so 0.
[00:34:16 - 00:34:25] Okay, so if we're going to build up the square wave in terms of sines and cosines, how many cosine functions do we want?
[00:34:25 - 00:34:30] 0. Yep, so this square wave is an odd function.
[00:34:30 - 00:34:32] So it's got odd symmetry.
[00:34:32 - 00:34:41] Okay, so cosines which have an even symmetry are no good to us.
[00:34:41 - 00:34:47] Okay, so let's write this down.
[00:34:47 - 00:35:01] So the cosine coefficients which are then a k equal to 0 for all k.
[00:35:01 - 00:35:11] So the square wave has...
[00:35:11 - 00:35:40] 2m is an is symmetry, odd symmetry like sine.
[00:35:40 - 00:35:46] Okay, so what we do want is then cosines.
[00:35:46 - 00:35:54] Okay, so a fundamental frequency here, we've got k equals 1.
[00:35:54 - 00:36:01] So this is our fundamental point.
[00:36:01 - 00:36:07] Here we've got k is 3 and k is 5.
[00:36:07 - 00:36:13] So this gun goes at 3 times f0 and this one goes at 5 times f0.
[00:36:13 - 00:36:49] Okay, so the even bk coefficients, so when k is 2 and k is 4, those coefficients are also 0.
[00:36:49 - 00:37:14] Okay, now if we consider what happens when k is 2, we have one repeating sine wave for the positive part of the square wave.
[00:37:14 - 00:37:22] And if we've got a whole period of that sine wave when k is 2, that's going to give us an average value of 0.
[00:37:22 - 00:37:27] So that's not going to help us build up a square wave.
[00:37:27 - 00:37:32] So the even bk coefficients are 0.
[00:37:32 - 00:37:37] And so the coefficients are shown here at the bottom.
[00:37:37 - 00:37:40] So these are the coefficients.
[00:37:40 - 00:37:55] And so it's only the odd values that are non-zero, odd k.
[00:37:55 - 00:38:05] Okay, these coefficients also decay exponentially.
[00:38:05 - 00:38:16] Okay, we can see that from the amplitudes of k, 1, 3 and 5, where the k is 1, the fundamental.
[00:38:16 - 00:38:20] It's got a coefficient of 1 matching our square wave.
[00:38:20 - 00:38:25] And then it's dropping down 3, 5, and getting smaller.
[00:38:25 - 00:38:40] Okay, so what we must do for the same example is what does it look like when we add up all these harmonics together?
[00:38:40 - 00:38:48] Okay, this should actually be a capital k here.
[00:38:48 - 00:38:52] So this is the sum of the first k harmonics.
[00:38:52 - 00:39:17] So now estimate of our signal to x hat of t is equal to a0 plus here we've now got a finite sum from k is little 1 to capital k of a k cos 2 pi f naught t.
[00:39:17 - 00:39:42] Oops, we've got the k, 8t plus bk sine 2 pi t.
[00:39:42 - 00:39:52] Okay, so here if we just try and approximate our square wave with 1 sine, we just have the fundamental frequency.
[00:39:52 - 00:40:00] And then if we've got the first 3 harmonics, it's getting a bit better.
[00:40:00 - 00:40:16] k is 5, still a bit lumpy, 7 dot dot dot, and here we've got k is 39, and then k is 79.
[00:40:16 - 00:40:33] Okay, so what we can say it always gets better with more harmonics.
[00:40:33 - 00:40:53] But it cannot be perfect square wave with a finite sum.
[00:40:53 - 00:41:01] And it's particularly apparent where it's not perfect, which is at the edges.
[00:41:01 - 00:41:19] And so this is known as Gibbs phenomenon, this ringing at the edges.
[00:41:19 - 00:41:28] At the edges is where we have the really high frequency content, and so that's where we can tell that we haven't got all our harmonics.
[00:41:28 - 00:41:38] So it's doing a reasonable job in the middle of the square waves, but the biggest era is at the edges.
[00:41:38 - 00:42:02] Okay, and then we'll do another quick example, but with a triangle wave rather than the square wave.
[00:42:02 - 00:42:11] Okay, so again here we've got plus the average value of a triangle wave over a period.
[00:42:11 - 00:42:17] So a zero is zero again, so we've got no DC term here.
[00:42:17 - 00:42:28] And so we're again showing here our first 3 non-zero harmonics.
[00:42:28 - 00:42:30] The coefficients are down here.
[00:42:30 - 00:42:53] Okay, and so cosine coefficients a k equal to zero for all k.
[00:42:53 - 00:43:08] And again, our even bk coefficients equals zero only.
[00:43:18 - 00:43:28] Okay, and so that coefficients here for the triangle wave decay much faster than they did for the square wave.
[00:43:28 - 00:43:39] So we are then better able to approximate our triangle wave for finite number of coefficients than for the square wave.
[00:43:39 - 00:43:49] And on the following side we've got the sum of the first capital K harmonics.
[00:43:49 - 00:43:53] We have been, so this is just the fundamental here.
[00:43:53 - 00:44:13] So we've got one harmonic, the sum of the first 3, then 5, 7, 39, and 79.
[00:44:13 - 00:44:18] So those square waves actually look pretty good.
[00:44:18 - 00:44:20] Better than the square wave approximations.
[00:44:20 - 00:44:35] So I'll just write that down so we have a better approximation.
[00:44:35 - 00:44:49] The triangle wave compared to Cf is compared to the square wave.
[00:44:49 - 00:44:53] And this is because the coefficients decrease more quickly.
[00:44:53 - 00:45:28] Okay, so that's the Fourier series.
[00:45:28 - 00:45:38] We've got, we can use it on a periodic signal and we get this grouped spectrum.
[00:45:38 - 00:45:42] The next thing we'll look at for the next 5 minutes and then again tomorrow is the Fourier transform.
[00:45:42 - 00:45:54] Where the signal doesn't think to be periodic and we get a continuous spectrum.
[00:45:54 - 00:46:00] Okay, so we have a continuous time to main signal, little x of t, and then the Fourier to main,
[00:46:00 - 00:46:03] we have a continuous spectrum capital X of f.
[00:46:03 - 00:46:20] So we can define our Fourier transform, capital X of f is equal to minus infinity to the integral of our signal x of t times the complex exponential,
[00:46:20 - 00:46:24] each minus j to pi f t.
[00:46:24 - 00:46:27] And we integrate with respect to time t.
[00:46:27 - 00:46:36] Now there are different definitions of the Fourier transform.
[00:46:36 - 00:46:47] So there are different definitions where we define it in terms of the angular frequency.
[00:46:47 - 00:46:59] This is angular frequency.
[00:46:59 - 00:47:06] But this gets a bit messy because we end up with factors of 2 pi floating in our equation.
[00:47:06 - 00:47:11] So the one I'll use here is just frequency and Hertz and time and seconds.
[00:47:11 - 00:47:15] I think that's easier to take care of.
[00:47:15 - 00:47:20] And so our spectrum, capital X of f, is going to be a complex number.
[00:47:20 - 00:47:27] So if our signal here is real and then this is complex, multiply this together and integrate it.
[00:47:27 - 00:47:31] x of f is going to be complex.
[00:47:31 - 00:47:39] So we have then our spectrum, capital X of f, this is a complex number.
[00:47:39 - 00:47:46] So we've got then our magnitude of our spectrum, magnitude.
[00:47:46 - 00:47:50] And then we also have it in terms of some phase.
[00:47:50 - 00:47:55] So e to the j, and then the angle of x f.
[00:47:55 - 00:48:10] And so you know the right angle of x f, or some angle theta f being the phase.
[00:48:10 - 00:48:12] So the spectrum is complex.
[00:48:12 - 00:48:14] It's got both magnitude and phase.
[00:48:14 - 00:48:21] So often we write the Fourier transform operation.
[00:48:21 - 00:48:29] So our spectrum, capital X of f, is equal to, I'll use this sort of calligraphic f.
[00:48:29 - 00:48:33] Let's quickly brackets of our signal x of t.
[00:48:33 - 00:48:35] This is some sort of fancy f.
[00:48:35 - 00:48:39] Now we had a fancy l for the little plus transform.
[00:48:39 - 00:48:43] And then we did a note before we transformed here with an angle,
[00:48:43 - 00:48:46] throw it with an arrow between the two.
[00:48:46 - 00:48:56] So the little x of t is a Fourier pair with capital X of.
[00:48:56 - 00:49:01] OK, so I'll leave it there for today because I know you've all got something to be.
[00:49:01 - 00:49:04] And so I can't miss.
[00:49:04 - 00:49:08] And hopefully that's in the drawing office.
[00:49:08 - 00:49:12] And then we'll look at the common properties of the Fourier transform,
[00:49:12 - 00:49:17] common function, common pairs, and hopefully I'll see you later on.
[00:49:17 - 00:49:21] So I'll just leave this off for a couple of minutes while you're finished writing down.
[00:49:59 - 00:50:02] and I'll get a question.
[00:50:02 - 00:50:03] Thank you.
[00:50:03 - 00:50:04] Thank you.
[00:50:04 - 00:50:05] Good, good, good.
[00:50:05 - 00:50:06] Thank you.
[00:50:06 - 00:50:07] Good.
[00:50:07 - 00:50:08] Good.
[00:50:08 - 00:50:10] Good.
[00:50:10 - 00:50:12] Good.
[00:50:12 - 00:50:14] Good.
[00:50:14 - 00:50:15] Thank you.
[00:50:15 - 00:50:17] I'm so glad to see you.
[00:50:17 - 00:50:18] Good.
[00:50:18 - 00:50:19] Good.
[00:50:19 - 00:50:27] Good.
[00:50:27 - 00:50:32] Good.
[00:50:32 - 00:50:33] Good.
[00:50:33 - 00:50:44] Thank you.
[00:50:44 - 00:50:45] Cheers.

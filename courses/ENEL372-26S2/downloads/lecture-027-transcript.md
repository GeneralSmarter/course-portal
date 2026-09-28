# ENEL372-26S2 Lecture 27 local ASR transcript

Date: September 25, 2026 9:00am-9:55am
Transcript type: Hermes-generated local ASR from validated Echo audio, not a native Echo transcript.
Backend/model: faster-whisper tiny.en, CPU int8, beam_size=5, vad_filter=True.
Source audio SHA-256: `a4c35a152a3969be08167734c1f8909dedc3b1e12eacfb4e4aaa262a7e0f8d68`
Generated: 2026-09-28T09:53:11.082690+13:00
Caveat: technical terms, equations, names and Māori words may require checking against slides/audio.

[00:00:26.290 - 00:02:12.690] Well, some people teamed up.
[00:02:12.690 - 00:02:38.960] I'm starting on new topic.
[00:02:38.960 - 00:02:39.960] Exciting.
[00:02:40.360 - 00:02:49.180] Thank you for coming.
[00:02:49.180 - 00:02:51.780] So, Brussels, D.C. Motors.
[00:02:51.780 - 00:02:59.260] I slightly or reorganised the slightly regor organised this learning outcomes.
[00:02:59.260 - 00:03:05.940] Because just to get them in line, it changed them.
[00:03:05.940 - 00:03:09.780] I just kind of just switched them around a bit.
[00:03:09.780 - 00:03:11.740] Move some of the others a bit later.
[00:03:11.740 - 00:03:20.060] Come on a bit behind.
[00:03:20.060 - 00:03:25.250] But behind what I'd get, anyway.
[00:03:25.250 - 00:03:28.570] So what I'll be doing today, I don't know if you...
[00:03:28.570 - 00:03:32.170] This is probably lots of learning outcomes in one.
[00:03:32.170 - 00:03:36.290] Stating applications of the BLDC motors and reviewing the basics.
[00:03:36.290 - 00:03:37.850] So that's you, all the way.
[00:03:37.850 - 00:03:41.090] Magnit, Feal, Becky, M.F, Torx Speed.
[00:03:41.090 - 00:03:49.610] And then now, lies in the four quadrant Torx Speed Qs.
[00:03:49.610 - 00:03:55.380] See how we go.
[00:03:55.380 - 00:03:59.100] Brushless, decent matters.
[00:03:59.100 - 00:04:03.600] Kind of amazing things.
[00:04:03.600 - 00:04:07.320] We're looking at special forms, synchronous motor.
[00:04:07.320 - 00:04:09.480] Here they are here.
[00:04:09.480 - 00:04:11.960] Typically here for like a permanent magnet,
[00:04:11.960 - 00:04:15.080] here permanent magnets that could be on the rotor
[00:04:15.080 - 00:04:20.960] and then you'd generate magnetic field to kind of
[00:04:20.960 - 00:04:24.000] repel all those magnets around and you keep switching them
[00:04:24.000 - 00:04:27.920] and you just create motion that way.
[00:04:27.920 - 00:04:35.260] Without any brushes, it's why they brush us.
[00:04:35.260 - 00:04:36.740] They will be...
[00:04:36.740 - 00:04:41.780] I'll be doing a couple of lectures, maybe three lectures.
[00:04:41.780 - 00:04:43.380] I think I'll be doing that three lectures
[00:04:43.380 - 00:04:45.580] because I'm covering what they are
[00:04:45.580 - 00:04:47.380] and the Torx Speed Qs.
[00:04:47.380 - 00:04:50.900] Then I'll be talking about some of the control aspects.
[00:04:50.900 - 00:04:54.060] So that will be three lectures on it.
[00:04:54.060 - 00:04:58.780] And there'll be here one exam question
[00:04:58.780 - 00:05:01.460] because here one big...
[00:05:01.460 - 00:05:04.020] Well, I suppose the third of the exam is rectifiers
[00:05:04.020 - 00:05:07.500] and then you kind of have my question two
[00:05:07.500 - 00:05:08.980] kind of has four parts.
[00:05:08.980 - 00:05:16.060] Yeah, well you could just say it's like the six questions
[00:05:16.580 - 00:05:18.740] in the exam but I'm trying to estimate
[00:05:18.740 - 00:05:23.100] what the brush is doing right as would probably be four, five, six,
[00:05:23.100 - 00:05:25.180] maybe one eighth.
[00:05:25.180 - 00:05:28.660] So what's that?
[00:05:28.660 - 00:05:33.660] For things to see maybe something like that, I'll be in.
[00:05:36.820 - 00:05:38.420] I'll do my math right.
[00:05:38.460 - 00:05:41.340] So not a massive amount but significant.
[00:05:41.340 - 00:05:42.900] More than 10% anyway.
[00:05:42.900 - 00:05:46.140] So more than 10% of the exam in terms of marks
[00:05:46.140 - 00:05:50.220] will be brush and steecing motors.
[00:05:50.220 - 00:05:52.140] But then obviously, like a lot more percentage
[00:05:52.140 - 00:05:53.580] as rectifiers, that's why I put a lot more
[00:05:53.580 - 00:06:01.900] into rectifiers.
[00:06:01.900 - 00:06:03.300] And just a reminder and I'll put a lot,
[00:06:03.300 - 00:06:06.060] I put the thing on learn as I'm gonna be going over
[00:06:06.060 - 00:06:10.340] the exam questions related to plotting in the rectifiers
[00:06:10.340 - 00:06:13.460] and I might just do one question,
[00:06:13.460 - 00:06:14.700] all that you do or question,
[00:06:14.740 - 00:06:18.940] and then I'll give the answer on getting the THD
[00:06:18.940 - 00:06:21.660] and just from an exam question.
[00:06:21.660 - 00:06:24.820] But I mostly wanna show you the plotting,
[00:06:24.820 - 00:06:26.700] how you do graphs and stuff.
[00:06:28.100 - 00:06:30.220] So that's at 12 o'clock today.
[00:06:31.660 - 00:06:33.260] I hope I get some people tuning up.
[00:06:33.260 - 00:06:35.100] I know it's really busy and stuff,
[00:06:35.100 - 00:06:38.540] but it's always happens in my part of the course,
[00:06:38.540 - 00:06:41.940] but I understand, do your best.
[00:06:42.900 - 00:06:45.940] All right, so yeah, why be I already seen motors?
[00:06:47.380 - 00:06:52.020] Got a few applications that I've put here.
[00:06:52.020 - 00:07:00.340] The electric cars, this is actually quite a no one actually,
[00:07:00.340 - 00:07:03.620] but I should actually update that,
[00:07:03.620 - 00:07:05.220] put the Tesla, put a Tesla in there
[00:07:06.580 - 00:07:08.620] because that's Porsche, what's your call,
[00:07:08.620 - 00:07:15.340] but it's about 220 kilowatt motors.
[00:07:18.100 - 00:07:23.740] Motor, electric, my brush is DC motors.
[00:07:23.740 - 00:07:25.580] They're about big motors.
[00:07:25.580 - 00:07:31.060] 220 kilowatts is a big barrel system owner.
[00:07:31.060 - 00:07:34.020] And yeah, the electric cars certainly store quite a thing
[00:07:34.020 - 00:07:37.460] that doing pretty well.
[00:07:41.350 - 00:07:45.390] This is actually an electric powered rocket.
[00:07:45.390 - 00:07:46.430] Can you guess what the rocket is?
[00:07:46.430 - 00:07:50.370] What's the name of the rocket?
[00:07:50.370 - 00:07:54.110] Anyone recognize it?
[00:07:54.110 - 00:07:55.030] Okay, I said.
[00:07:56.030 - 00:07:59.410] It's launched from New Zealand.
[00:07:59.410 - 00:08:01.450] What's the New Zealand rocket?
[00:08:01.450 - 00:08:02.970] There's no one know the name of it.
[00:08:02.970 - 00:08:04.690] Rocket-lage rocket.
[00:08:04.690 - 00:08:06.770] Ah, it's called a leit-chon.
[00:08:08.290 - 00:08:09.330] You should have known that.
[00:08:10.530 - 00:08:12.010] Because you're telling me.
[00:08:12.010 - 00:08:13.810] Because there you know.
[00:08:15.130 - 00:08:17.570] So this is the leit-chon rocket.
[00:08:17.570 - 00:08:19.770] It's actually very few people in New Zealand know that.
[00:08:19.770 - 00:08:22.170] So in America, and I ain't company now,
[00:08:22.170 - 00:08:26.010] because it used to be New Zealand-owned and Rocket-labs now.
[00:08:26.210 - 00:08:27.210] Yeah.
[00:08:27.210 - 00:08:32.800] So that's the leit-chon rocket.
[00:08:32.800 - 00:08:34.880] And so the turbo pumps,
[00:08:36.000 - 00:08:37.040] I know you're electric engineers,
[00:08:37.040 - 00:08:38.880] or you make a chon, as well.
[00:08:40.400 - 00:08:42.400] So you have turbo pumps that pump the fuel.
[00:08:42.400 - 00:08:47.160] Turbo pumps, but the turbo pumps that pump the fuel
[00:08:47.160 - 00:09:05.020] are paired by BLDC motors.
[00:09:05.020 - 00:09:07.580] Or you gotta, because you gotta get the pal in the main chamber
[00:09:07.580 - 00:09:09.060] and then keep the pressure efficient
[00:09:09.060 - 00:09:10.100] for stable combustion.
[00:09:10.100 - 00:09:12.380] And you gotta kind of mix the,
[00:09:12.380 - 00:09:14.540] I think they might be just doing kerosene
[00:09:14.540 - 00:09:18.380] and liquid oxygen.
[00:09:19.580 - 00:09:21.300] So they're now moving to methane,
[00:09:21.300 - 00:09:22.500] and it hung SpaceX are doing this.
[00:09:22.500 - 00:09:24.660] Well methane and liquid oxygen.
[00:09:25.900 - 00:09:27.340] And my own research group, we're actually doing
[00:09:27.340 - 00:09:31.020] propane and the production.
[00:09:31.020 - 00:09:33.420] And I'm, yeah, hoping maybe you'll in each year
[00:09:33.420 - 00:09:35.820] to want to say, look, if you're rocket.
[00:09:37.460 - 00:09:40.060] If I can get above 12K, it's a plate of world record.
[00:09:40.060 - 00:09:42.500] So that's not very high for a look
[00:09:42.500 - 00:09:44.620] if you're a rocket from the university.
[00:09:44.620 - 00:09:46.340] I'm not sure if I'm gonna use a brush of St C motors,
[00:09:46.340 - 00:09:50.180] but they'll be for the specific turbo pumps.
[00:09:50.180 - 00:09:52.300] But I'll probably use them throughout.
[00:09:54.220 - 00:09:55.740] We probably only have some canards on there.
[00:09:55.740 - 00:09:59.380] So yeah, they're just a canard here, but yeah.
[00:09:59.380 - 00:10:02.380] For the canards on our rocket, which has a silent
[00:10:02.380 - 00:10:03.860] on moving into the liquid fuel.
[00:10:05.780 - 00:10:11.230] These are paired by a brush of St C motors as well.
[00:10:11.230 - 00:10:13.070] Yeah, so they're really, really handy.
[00:10:15.190 - 00:10:19.810] Just very efficient.
[00:10:19.890 - 00:10:27.080] And this is just a metric plane.
[00:10:27.080 - 00:10:29.880] I'm also actually involved a little bit.
[00:10:29.880 - 00:10:32.640] I'm looking at developing hydrogen powered satellites,
[00:10:32.640 - 00:10:36.880] but we're looking at liquefying hydrogen in space.
[00:10:36.880 - 00:10:39.000] And then if we do that, it's actually gonna be much easier
[00:10:39.000 - 00:10:43.540] to do it for aviation.
[00:10:43.540 - 00:10:46.140] And so these would be, I think, lithium ion probably
[00:10:47.340 - 00:10:48.740] batteries that put it in here.
[00:10:48.740 - 00:10:50.220] And then obviously you got a brush of St C motors,
[00:10:50.220 - 00:10:53.380] but if you've got liquid hydrogen,
[00:10:54.180 - 00:10:56.900] hydrogen fuel cells, that's gonna mean
[00:10:57.940 - 00:10:59.820] yeah, you can carry a lot more batteries,
[00:10:59.820 - 00:11:00.940] have a lot more power.
[00:11:02.540 - 00:11:05.260] And then they'll be, they'll be powering
[00:11:05.260 - 00:11:08.340] the brush of St C motors.
[00:11:08.340 - 00:11:11.660] But the ones on this plane would be about 70 kilowatts.
[00:11:11.660 - 00:11:16.290] And the brush of St C motors are very, very light.
[00:11:16.290 - 00:11:21.050] Also, there's another company, one of my students,
[00:11:21.050 - 00:11:24.570] spun off with my rocket, which was called Kia-Ris,
[00:11:24.610 - 00:11:30.040] which, and they have a solar glider.
[00:11:30.040 - 00:11:31.680] Lots of brush of St C motors,
[00:11:31.680 - 00:11:36.680] so many motors they have, maybe four.
[00:11:37.840 - 00:11:39.960] And they're all brush of St C motors.
[00:11:39.960 - 00:11:42.360] Good reason for them, because they're,
[00:11:43.560 - 00:11:45.720] they don't wear out lots of reasons for them,
[00:11:45.720 - 00:11:48.600] but the big thing for ear spacers that they're very light,
[00:11:48.600 - 00:11:50.200] so for the power you get,
[00:11:52.720 - 00:11:56.720] power to weight, your power to weight is really high,
[00:11:56.760 - 00:12:01.410] which is why they use in the aviation industry.
[00:12:01.410 - 00:12:19.880] So yeah, that's why, I suppose.
[00:12:19.880 - 00:12:25.400] So we'll be looking at the general motor theory,
[00:12:25.400 - 00:12:28.600] maybe it'll touch a little bit on the AC induction motor,
[00:12:29.840 - 00:12:31.000] a tiny wee bit.
[00:12:32.320 - 00:12:35.480] And, but mostly I'm looking at the DC,
[00:12:35.480 - 00:12:36.960] the brush of St C of course.
[00:12:38.280 - 00:12:40.080] But, and you know, once again, the BOW DC
[00:12:40.080 - 00:12:42.480] is looking at different configurations,
[00:12:42.480 - 00:12:44.360] and then driving the BOW DC motors.
[00:12:44.360 - 00:12:47.160] So this is, when you drive them,
[00:12:47.160 - 00:12:49.440] that's like control systems, really.
[00:12:49.440 - 00:12:50.600] Control systems.
[00:12:51.520 - 00:12:53.800] And they're very, very sophisticated.
[00:12:55.120 - 00:12:58.000] How do you spell sophisticated?
[00:12:59.320 - 00:13:02.400] Because it's involving commutation,
[00:13:02.400 - 00:13:04.880] like switching at the right time in sensing,
[00:13:04.880 - 00:13:07.600] and then there's delays,
[00:13:07.600 - 00:13:08.960] and you have to take to account,
[00:13:08.960 - 00:13:10.880] and you've got to watch the dozen stall.
[00:13:10.880 - 00:13:15.880] So, that's one of the issues, I suppose,
[00:13:16.040 - 00:13:17.840] with the BOW DC motors,
[00:13:17.840 - 00:13:22.120] is it's very complex to get it right in efficient.
[00:13:22.120 - 00:13:25.480] Now you can probably get something running, approximately,
[00:13:25.480 - 00:13:37.500] but it is, it is really tough.
[00:13:37.500 - 00:13:39.540] So there's not really a lot of development
[00:13:39.540 - 00:13:41.100] of these, I don't think there's any of these.
[00:13:41.100 - 00:13:45.620] We don't build these in New Zealand or Australia.
[00:13:45.620 - 00:13:51.660] I'd love to, but we did kind of build one
[00:13:51.700 - 00:13:54.140] a rocket-wave sort of, it wasn't reused,
[00:13:54.140 - 00:13:57.780] but we did use not the actual underlying windings
[00:13:57.780 - 00:13:59.180] and everything, but we built the controller
[00:13:59.180 - 00:14:02.780] that we actually bought the components.
[00:14:04.340 - 00:14:08.420] But it had to kind of customize it to work on the rocket.
[00:14:08.420 - 00:14:11.420] And she went away, Master's students was a key leader
[00:14:11.420 - 00:14:14.260] on that years ago.
[00:14:15.260 - 00:14:19.180] Because rocket-lab, condor was it 27, 17,
[00:14:19.220 - 00:14:23.260] so it had been at 2018 or so, up to 2019.
[00:14:29.510 - 00:14:30.430] And there's yet another one
[00:14:30.430 - 00:14:33.030] on the studio that was doing the same thing,
[00:14:33.030 - 00:14:33.870] thank you for the key,
[00:14:33.870 - 00:14:36.510] I suppose we've had to customize it,
[00:14:36.510 - 00:14:37.910] I think the brush of Stissie motors as well,
[00:14:37.910 - 00:14:41.310] because you can't buy, then out of oil,
[00:14:41.310 - 00:14:43.390] we're just gonna buy off a shelf for something
[00:14:43.390 - 00:14:47.430] that'll work for a solar-foured glide up at 22Ks.
[00:14:50.470 - 00:14:53.510] It seems out at 22Ks, I'm deviating a bit here,
[00:14:53.510 - 00:14:56.150] at 22Ks, but just in terms of operating the brush
[00:14:56.150 - 00:15:00.110] of Stissie motor, it's the worst environment apparently.
[00:15:00.110 - 00:15:01.790] This was the Avionics engineer
[00:15:01.790 - 00:15:03.990] who's one of my sort of students.
[00:15:05.390 - 00:15:10.390] The engineer, it was saying that it's because you're a connet,
[00:15:10.390 - 00:15:15.230] the cusp, where you get like,
[00:15:15.750 - 00:15:17.230] something that you get a lot of atmospheric,
[00:15:17.230 - 00:15:18.750] looking at winds and you can get,
[00:15:18.750 - 00:15:19.950] but it's like really thin,
[00:15:19.950 - 00:15:21.070] so you're still getting radiation,
[00:15:21.070 - 00:15:24.830] but you're getting some atmospheric stuff as well,
[00:15:24.830 - 00:15:27.190] so it's like the worst of both worlds.
[00:15:27.190 - 00:15:30.430] When you come down to a normal like 10Ks, I always,
[00:15:31.590 - 00:15:36.030] it's much easier, but if then you're going to go into space.
[00:15:36.030 - 00:15:38.790] So what's interesting is,
[00:15:40.430 - 00:15:42.270] here his comment was, well,
[00:15:42.270 - 00:15:44.630] if we adapted our systems to a satellite,
[00:15:44.630 - 00:15:46.470] it'd be really easy.
[00:15:46.470 - 00:15:48.190] So I thought that was interesting,
[00:15:48.270 - 00:15:51.150] all the electronics and everything.
[00:15:51.150 - 00:15:52.710] So I showed the bus of Stissie motors
[00:15:52.710 - 00:15:56.670] are really hard to get going at about 22Ks altitude.
[00:15:56.670 - 00:15:59.870] It's pretty much the worst design point
[00:15:59.870 - 00:16:02.150] for electronics in the old Stissie motors.
[00:16:03.470 - 00:16:06.230] But anyway, they've kind of succeeded in that
[00:16:06.230 - 00:16:10.060] and they're doing really well.
[00:16:10.060 - 00:16:12.940] But the whole design around the bus of Stissie motors
[00:16:12.940 - 00:16:16.060] was pretty much key to their whole business.
[00:16:16.060 - 00:16:18.420] Like it's got to be so efficient,
[00:16:18.420 - 00:16:19.780] otherwise they don't have a business
[00:16:19.780 - 00:16:22.460] because you've got to be able to keep the glider flying
[00:16:22.460 - 00:16:24.100] through the night, that's the problem.
[00:16:25.300 - 00:16:27.700] So it's critical to get every bit of efficiency
[00:16:27.700 - 00:16:30.940] you can get for pairing the glider.
[00:16:31.980 - 00:16:35.870] It really bell DCs are the only way to do it.
[00:16:35.870 - 00:16:38.350] So I hope I've sold bell DCs to you.
[00:16:38.350 - 00:16:42.520] Anyway, so here we are, electric motors.
[00:16:42.520 - 00:16:46.300] This is interesting,
[00:16:46.300 - 00:16:50.400] I'm getting a new year.
[00:16:50.400 - 00:16:53.200] Weird year, it's not actually run here.
[00:16:53.200 - 00:16:55.200] Do you reckon, mate, notice?
[00:16:56.160 - 00:16:57.240] You can probably see it.
[00:16:58.520 - 00:16:59.800] Can you see where, can you see there
[00:16:59.800 - 00:17:01.280] where the bus of Stissie sets?
[00:17:01.280 - 00:17:04.660] Does that surprise you?
[00:17:04.660 - 00:17:07.340] Someone's nodding, not surprising you at all?
[00:17:08.940 - 00:17:11.220] Does anyone think that's surprising?
[00:17:12.620 - 00:17:14.860] Bus of Stissie motor?
[00:17:14.860 - 00:17:18.660] Wouldn't that be on the DC side?
[00:17:18.660 - 00:17:20.060] No.
[00:17:20.060 - 00:17:24.620] It's on the AC side.
[00:17:24.620 - 00:17:29.770] And that's because it is essentially like an AC motor.
[00:17:29.770 - 00:17:31.090] And it's the way that you do the switching
[00:17:31.090 - 00:17:32.010] with the magnet at field.
[00:17:32.050 - 00:17:35.570] Because it actually creates an AC, current,
[00:17:35.570 - 00:17:37.490] but it not could be trippes oil.
[00:17:38.530 - 00:17:42.690] And so it comes under asynchronous.
[00:17:43.970 - 00:17:46.130] Brushless DC comes under asynchronous motor
[00:17:46.130 - 00:17:59.040] and it's AC.
[00:17:59.040 - 00:18:01.480] And then you have the traditional commutator,
[00:18:01.480 - 00:18:05.640] like the, with the brushes and everything,
[00:18:05.640 - 00:18:08.900] which are coming over the side.
[00:18:08.900 - 00:18:09.940] There's all sorts of types.
[00:18:09.940 - 00:18:13.220] So I think the AC induction motor
[00:18:14.220 - 00:18:18.220] is probably around here for the vertical dry.
[00:18:18.220 - 00:18:20.300] You have the single face capacitor.
[00:18:21.580 - 00:18:30.900] It's like the PAO's vertical dry.
[00:18:30.900 - 00:18:36.340] Within the same family as the, the ODC, isn't it?
[00:18:36.340 - 00:18:40.500] And in the season three, seven, if you remember,
[00:18:40.500 - 00:18:49.960] single face.
[00:18:49.960 - 00:19:00.180] I think I also need to say in there.
[00:19:00.180 - 00:19:07.390] So you're looking at the general principles,
[00:19:07.390 - 00:19:10.790] motors, obviously traction, repulsion,
[00:19:10.830 - 00:19:13.710] being in a pole, so it'll be going over that
[00:19:13.710 - 00:19:16.110] with some really basic two pole motors.
[00:19:16.110 - 00:19:20.470] And then moving up to maybe four pole
[00:19:20.470 - 00:19:23.150] and maybe even just single pole pair actually.
[00:19:23.150 - 00:19:25.150] That demonstrates it quite well.
[00:19:25.150 - 00:19:26.910] And how you can get attraction and repulsion
[00:19:26.910 - 00:19:31.550] and how that spoons of motor and the right sequence
[00:19:31.550 - 00:19:34.110] through the phasing, that the phasing is the key.
[00:19:35.070 - 00:19:36.550] Between the rotor and stata,
[00:19:37.670 - 00:19:38.510] stata.
[00:19:42.160 - 00:19:44.240] And then you know that's why they call AC machines
[00:19:44.240 - 00:19:46.920] because you are reversing current
[00:19:46.920 - 00:19:48.440] because current flow will be going
[00:19:49.840 - 00:19:52.320] into the windings and then out again.
[00:19:54.000 - 00:19:55.440] You can see how all the switching takes
[00:19:55.440 - 00:19:57.480] as it starts to move around.
[00:19:57.480 - 00:20:00.520] So you get an AC waveform, but it could be like a trapezoid.
[00:20:00.520 - 00:20:02.040] Can be a sign wave.
[00:20:02.040 - 00:20:07.040] You can get sign a sort of backing if winding the coil
[00:20:07.320 - 00:20:15.100] or such, you get a sign wave backing if nothing much.
[00:20:17.200 - 00:20:22.850] So there, it's just the kind of overview,
[00:20:22.850 - 00:20:26.410] the general approach, which will really kind of be kind
[00:20:26.410 - 00:20:34.100] of looking at, turning the principles,
[00:20:35.300 - 00:20:36.380] leans this law.
[00:20:37.540 - 00:20:40.060] You've got a magnet field that's fearing
[00:20:41.820 - 00:20:45.460] and you're changing the magnet field through the coils
[00:20:45.460 - 00:20:48.180] and then switching to allow the current
[00:20:48.180 - 00:20:50.340] to flow in and out different coils and back again.
[00:20:50.340 - 00:20:52.860] So it's a very fast changing magnet
[00:20:52.900 - 00:20:56.660] field over time and that's what's actually moving
[00:20:56.660 - 00:20:58.660] the pavement magnets.
[00:20:58.660 - 00:21:06.820] But that generates a voltage that opposes the change.
[00:21:06.820 - 00:21:08.860] And so what I'm saying here in the motors,
[00:21:12.640 - 00:21:14.240] the magnet poles,
[00:21:15.520 - 00:21:17.200] because there are actually two configurations
[00:21:17.200 - 00:21:20.360] you could have the magnet, the permanent magnet poles
[00:21:20.360 - 00:21:23.240] which I like, permanent magnets, North and South,
[00:21:23.240 - 00:21:25.600] they could be on the rotor and they'll be rotating.
[00:21:26.440 - 00:21:30.040] And so then they're rotating past the motor windings,
[00:21:30.040 - 00:21:33.160] but then that's causing the time viewing,
[00:21:33.160 - 00:21:34.760] that's the time viewing then it failed
[00:21:34.760 - 00:21:36.120] that creates this relative movement.
[00:21:36.120 - 00:21:39.560] But sometimes you could have the magnet poles
[00:21:39.560 - 00:21:44.560] could be not on the stator, they'll be actually fixed.
[00:21:46.320 - 00:21:51.320] And then you can have the rotor can be what you can
[00:21:51.320 - 00:21:53.880] can pass the magnet field.
[00:21:53.920 - 00:21:56.280] So it all depends on the configuration,
[00:21:56.280 - 00:21:58.320] but in both cases you get relative movement
[00:21:59.880 - 00:22:02.400] over the magnet poles path of motor windings.
[00:22:03.440 - 00:22:05.400] Sometimes you have the magnets on the outside,
[00:22:05.400 - 00:22:07.360] sometimes on the inside with the,
[00:22:07.360 - 00:22:09.160] you'll see it later.
[00:22:09.160 - 00:22:11.120] There's different geometrical configurations
[00:22:11.120 - 00:22:13.280] for how you can create this relative movement.
[00:22:14.520 - 00:22:16.760] Okay, and just emf,
[00:22:18.320 - 00:22:19.800] or you just get the back emf,
[00:22:19.800 - 00:22:22.200] which is pretty standard for,
[00:22:22.240 - 00:22:25.720] and that can seem to oppose the motor current,
[00:22:25.720 - 00:22:29.140] which is a good thing,
[00:22:29.140 - 00:22:30.860] because as you, you know,
[00:22:30.860 - 00:22:34.580] so that's why you don't wanna rotate motors too slowly,
[00:22:34.580 - 00:22:36.900] because if you rotate them slowly,
[00:22:36.900 - 00:22:38.860] current builds up, they heat up.
[00:22:39.780 - 00:22:42.580] So you've motors like to go in really, really fast,
[00:22:42.580 - 00:22:44.820] and they run, because when they run fast,
[00:22:44.820 - 00:22:48.500] the current drops, because the becca in F increases
[00:22:48.500 - 00:22:51.300] as a function of the speed of the motor,
[00:22:51.300 - 00:22:59.930] and it limits the current, which is a good thing.
[00:23:00.010 - 00:23:02.130] So back emf plays quite a large role
[00:23:02.130 - 00:23:05.410] and gruscious DC motors and how you design for it.
[00:23:06.850 - 00:23:08.170] It's an important concept.
[00:23:09.810 - 00:23:23.700] So I'm still on my electric motor review.
[00:23:23.700 - 00:23:27.260] You know, we're converting from electric power
[00:23:27.260 - 00:23:29.260] into mechanical power, like you have batteries,
[00:23:29.260 - 00:23:31.420] that so it is DC source,
[00:23:31.420 - 00:23:33.540] there's a DC source, there's some battery.
[00:23:34.700 - 00:23:37.260] And then the battery is,
[00:23:38.260 - 00:23:42.260] yeah, that's providing the, your ability to give current
[00:23:42.260 - 00:23:44.500] to create magnetic field.
[00:23:45.380 - 00:23:46.940] So you need the battery to have the power
[00:23:46.940 - 00:23:48.900] to create the magnet at field.
[00:23:48.900 - 00:23:51.020] And in the magnet at field,
[00:23:51.020 - 00:23:53.060] is then interacting with the permanent magnets
[00:23:53.060 - 00:23:57.180] to actually repel for power in attracting,
[00:23:57.180 - 00:24:00.140] to create the motion, which is mechanical power.
[00:24:00.140 - 00:24:02.580] So effectively, you're converting from electric power
[00:24:02.580 - 00:24:07.660] to mechanical power.
[00:24:07.660 - 00:24:10.620] Course there are losses, and sometimes you need,
[00:24:10.620 - 00:24:11.820] depending on,
[00:24:13.180 - 00:24:15.740] because like the way that brush the DC motors are designed,
[00:24:15.740 - 00:24:20.740] because they like running really fast, high speed,
[00:24:22.700 - 00:24:25.100] it's normally too high speed for your application.
[00:24:25.100 - 00:24:27.140] Like if you have a propeller on the end of like,
[00:24:27.140 - 00:24:29.780] say the solar glider, propellers, you know,
[00:24:29.780 - 00:24:34.100] like really big propellers, they like to go slow,
[00:24:34.100 - 00:24:37.740] they don't want to go too fast with the way that the wind works.
[00:24:37.740 - 00:24:39.620] But the brush the DC motor wants to go fast.
[00:24:39.620 - 00:24:40.580] So there's a contradiction.
[00:24:40.580 - 00:24:42.820] This is always the problem in designing
[00:24:42.820 - 00:24:44.660] when you try and convert,
[00:24:44.660 - 00:24:47.820] they actually get the velocity DC motor into the load,
[00:24:47.820 - 00:24:51.860] is that, yeah, so what you'd probably do is,
[00:24:52.820 - 00:24:55.540] often, you try and avoid it if you can,
[00:24:55.540 - 00:24:57.620] but often you have to have gears
[00:24:57.620 - 00:25:01.820] to try and reduce the speed.
[00:25:01.820 - 00:25:03.140] So that's pretty common.
[00:25:03.140 - 00:25:05.900] But then you're making a loss from having gear ratios,
[00:25:05.900 - 00:25:08.940] gear ratios, every time you step them down,
[00:25:08.940 - 00:25:11.140] you're making a fair loss.
[00:25:11.140 - 00:25:14.260] So there are some designs that can try and avoid that,
[00:25:14.260 - 00:25:16.780] but it's hard to get around.
[00:25:18.100 - 00:25:20.620] But if we ignore the fact that some losses,
[00:25:21.620 - 00:25:26.620] then you can say that basically the power and watts,
[00:25:28.300 - 00:25:32.740] electric power is gonna be the mechanical power,
[00:25:32.740 - 00:25:36.580] which is the torque multiplied by the angle of angular speed.
[00:25:36.580 - 00:25:38.420] This is like a small M, like,
[00:25:40.020 - 00:25:45.020] PM and T, omega-N, in for motor.
[00:25:49.820 - 00:25:52.060] So, and that's kind of handy
[00:25:52.060 - 00:25:53.980] because if you, that's really hard
[00:25:53.980 - 00:25:57.340] to measure mechanical power, you can.
[00:25:57.340 - 00:26:02.700] But you're gonna have to get the angular speed
[00:26:02.700 - 00:26:06.580] of the motor, so that's requires,
[00:26:08.140 - 00:26:10.140] there's all sorts of ways of doing that, lasers,
[00:26:10.540 - 00:26:13.700] it's just a pain to try and measure RPM of a motor.
[00:26:13.700 - 00:26:15.020] It's much easier just to say,
[00:26:15.020 - 00:26:17.620] well, roughly the mechanical torque
[00:26:17.620 - 00:26:19.260] is the same as the electrical torque.
[00:26:20.500 - 00:26:22.420] So we can see that there is approximately
[00:26:22.420 - 00:26:24.340] the electric power, which is the right inside.
[00:26:24.340 - 00:26:30.880] So the electric power is the mechanical power,
[00:26:30.880 - 00:26:36.420] so that mechanical power here is approximately the electric power.
[00:26:36.420 - 00:26:37.780] Torque and speed up with a motor match
[00:26:37.780 - 00:26:40.620] the mechanical load, I'll be going over that later.
[00:26:41.620 - 00:26:46.620] It's sort of like, it's physics really, like it's,
[00:26:50.760 - 00:26:52.920] by definition, if you actually,
[00:26:54.280 - 00:26:56.600] the torque has to be able to actually rotate the load.
[00:26:56.600 - 00:26:59.040] If the load was too, too big,
[00:27:00.160 - 00:27:02.320] and the motor wasn't spicked enough
[00:27:02.320 - 00:27:05.160] so that it had enough torque, the motor is not gonna move.
[00:27:05.160 - 00:27:07.000] This is gonna struggle, it's not even gonna rotate it,
[00:27:07.000 - 00:27:09.360] which means it's gonna heat up and probably explode.
[00:27:09.360 - 00:27:12.600] So you'd have to make sure that you have enough torque
[00:27:12.680 - 00:27:15.920] on the motor, obviously, to impact the load.
[00:27:17.120 - 00:27:18.480] And then you have to take to account
[00:27:18.480 - 00:27:20.600] that the fact that you want it to go a certain speed,
[00:27:20.600 - 00:27:22.640] like I say, with the power on the glider.
[00:27:22.640 - 00:27:24.040] So you want to have it designed.
[00:27:24.040 - 00:27:26.000] So the torque and speed output
[00:27:26.000 - 00:27:26.840] have got a match,
[00:27:26.840 - 00:27:31.000] gonna be matched to the specific application of the load.
[00:27:31.920 - 00:27:36.570] And I'll be showing you that later.
[00:27:36.570 - 00:27:37.250] I won't be doing,
[00:27:37.250 - 00:27:38.490] like in the exam situation,
[00:27:38.490 - 00:27:40.330] you won't be doing have to do like full build
[00:27:40.330 - 00:27:42.530] DC motor design, I won't be saying,
[00:27:44.810 - 00:27:48.610] try and come up with the full specs.
[00:27:48.610 - 00:27:50.210] Here's a whole lot of DBL DC motors.
[00:27:50.210 - 00:27:54.330] Can you design, choose the right torque speed
[00:27:54.330 - 00:27:58.570] or get the right characteristics that enable you to,
[00:27:58.570 - 00:28:01.010] I don't know, fly a solar glider, 22K,
[00:28:01.010 - 00:28:04.730] say, I don't know, 10 kilometers an hour, 22Ks.
[00:28:05.810 - 00:28:07.250] But those are sort of things you've got to do.
[00:28:07.250 - 00:28:09.970] Actually, you have to figure out,
[00:28:09.970 - 00:28:11.490] and I won't be asking that in the exam.
[00:28:11.490 - 00:28:13.810] But I'll be giving you the tools, hopefully,
[00:28:13.810 - 00:28:16.370] where maybe you could do it.
[00:28:16.370 - 00:28:18.890] But it's a big subject.
[00:28:18.890 - 00:28:22.570] So I won't have much time to go too much into there.
[00:28:22.570 - 00:28:23.850] I'll then just give you an overview
[00:28:23.850 - 00:28:26.290] of what the Adiosa motors are, how they work,
[00:28:26.290 - 00:28:28.490] how they control, how you can control them,
[00:28:28.490 - 00:28:30.330] some of the applications.
[00:28:30.330 - 00:28:35.340] As much as I can do it in three-dixels,
[00:28:35.340 - 00:28:37.300] given the fact that there's only about 10 or 12%
[00:28:37.300 - 00:28:43.490] gonna be asked in the exam.
[00:28:43.530 - 00:28:44.650] Different types of motors.
[00:28:44.650 - 00:28:46.370] Yeah, obviously you've got different torque
[00:28:46.370 - 00:28:48.050] versus speed curves, because you want to have
[00:28:48.050 - 00:28:50.250] enough torque to be able to power the load,
[00:28:50.250 - 00:28:52.250] and then you want to have the speed to be right.
[00:28:53.330 - 00:29:01.470] And there's all different types that enable you to do that.
[00:29:01.470 - 00:29:04.670] Yeah, and it's got an intersect with the load.
[00:29:05.990 - 00:29:17.900] Let's just show you this in as normally
[00:29:17.900 - 00:29:19.780] the number of tens per minute or something,
[00:29:19.780 - 00:29:24.780] or could be RPM, or it could be ratings per second,
[00:29:24.780 - 00:29:25.980] or degrees per second.
[00:29:26.900 - 00:29:29.140] But Ian is often what it's called,
[00:29:29.140 - 00:29:31.660] just the number of tens per second.
[00:29:31.660 - 00:29:33.660] It's related to the speed of the rotor.
[00:29:34.660 - 00:29:38.980] If you want to do the torque speed curve,
[00:29:38.980 - 00:29:47.590] Ian is often used, and then the y-axis is the torque.
[00:29:47.590 - 00:29:51.710] So say we had an induction motor, AC induction motor,
[00:29:51.710 - 00:29:53.870] it's some sort of weird behavior at the start,
[00:29:53.870 - 00:30:01.860] but once it kicks in, you get over this peak,
[00:30:01.860 - 00:30:13.540] and you have this sort of operating range,
[00:30:13.540 - 00:30:17.390] you have your load.
[00:30:17.390 - 00:30:20.190] Think of the load as being,
[00:30:20.190 - 00:30:24.030] I think of it being like a big propeller or big fan or something.
[00:30:24.030 - 00:30:28.310] And imagine a big fan with blades.
[00:30:28.310 - 00:30:31.230] The faster it's going, the more the wind friction
[00:30:31.230 - 00:30:33.150] will go against the more torque required
[00:30:33.150 - 00:30:35.070] to keep it going faster, right?
[00:30:35.070 - 00:30:37.430] It actually goes up as a square line with aerodynamics,
[00:30:37.430 - 00:30:38.750] if you look a wind turbine.
[00:30:40.190 - 00:30:43.790] As you increase the speed, the torque goes up like this,
[00:30:43.790 - 00:30:44.750] and this is the load,
[00:30:44.790 - 00:30:46.910] but of course, it gets from the pure,
[00:30:46.910 - 00:30:50.950] the fan's heading the air resistance.
[00:30:50.950 - 00:30:53.870] So this is the load, and so you tend to have,
[00:30:53.870 - 00:30:57.110] you see you have a load as being a torque versus speed as well
[00:30:57.110 - 00:31:02.110] on a graph, and then you've got your motor characteristics.
[00:31:05.620 - 00:31:08.100] And so this is your motor that could be
[00:31:08.100 - 00:31:14.380] like an AC induction motor.
[00:31:14.380 - 00:31:16.540] Imagine it's got up to a certain speed,
[00:31:16.540 - 00:31:18.660] and then it's governed in this region here.
[00:31:19.340 - 00:31:23.980] So if you imagine that the motor is offering a day,
[00:31:23.980 - 00:31:26.300] so let's say for you a day,
[00:31:26.300 - 00:31:34.540] see if you're a day, that means the motor torque is greater
[00:31:34.540 - 00:31:37.140] than the torque required to rotate the fan.
[00:31:38.620 - 00:31:41.180] And so it wasn't having torque, right?
[00:31:41.180 - 00:31:43.220] It's greater than more torque than you need.
[00:31:43.220 - 00:31:44.820] The fan's going to speed up, right?
[00:31:45.740 - 00:31:50.740] So if you were back here and you were talks too high,
[00:31:52.020 - 00:32:02.190] so the torque is too high, well you're going to speed up.
[00:32:02.190 - 00:32:04.270] So it means you start to move in this direction here.
[00:32:04.270 - 00:32:08.150] If you're here, you start to move, and so it speeds up.
[00:32:08.150 - 00:32:10.390] As it speeds up, it's going to slow down again
[00:32:10.390 - 00:32:13.910] because it's reaching, it's feeling that resistance
[00:32:13.910 - 00:32:16.900] against it.
[00:32:16.900 - 00:32:19.940] If it happened to shoot past it for some reason,
[00:32:22.580 - 00:32:38.110] then your torque is going to be too low.
[00:32:38.150 - 00:32:46.580] So if you're talks too low, you're going to slow down again.
[00:32:46.580 - 00:32:49.140] So this is what's meant by matching the load.
[00:32:49.140 - 00:32:53.420] It's like a steady state condition where you have a transient
[00:32:53.420 - 00:32:55.900] where you may be too much and so you're depending on where you are.
[00:32:55.900 - 00:33:00.100] You always tend to oscillate and then you settle at this point here.
[00:33:01.540 - 00:33:06.380] And the point where you hit your steady state
[00:33:07.460 - 00:33:09.980] with your motor torque and the amount of speed under the blades
[00:33:09.980 - 00:33:13.220] or whatever that's happening, that is your design point.
[00:33:14.260 - 00:33:17.660] That's where you want the motor to be as most efficient as possible
[00:33:18.500 - 00:33:20.060] for your application.
[00:33:20.060 - 00:33:25.580] So all depends on where you intersect the torque speed of the motor
[00:33:25.580 - 00:33:27.340] with the torque speed of the load.
[00:33:28.460 - 00:33:34.580] So that is a really important point in a concept to get.
[00:33:34.580 - 00:33:36.900] So the torque speed must intersect with the torque speed
[00:33:36.900 - 00:33:46.400] of the mechanical load and the reason is to get steady state speed.
[00:33:48.580 - 00:34:01.250] Otherwise, you know, that it's alright or you decelerate to the steady state.
[00:34:05.920 - 00:34:12.130] So there's ways of, well, yeah, so you can obviously, you can manipulate
[00:34:13.010 - 00:34:16.530] the torque speed graph of the motor.
[00:34:16.530 - 00:34:22.770] One of the simplest ways to change the torque speed graph is to just put more power in.
[00:34:22.770 - 00:34:23.890] Have a bigger battery.
[00:34:25.970 - 00:34:29.810] Just have a bigger motor and create more power.
[00:34:30.930 - 00:34:35.490] Which means that this whole curve is then going to move to the right and up.
[00:34:35.490 - 00:34:39.010] Which means that then you're going to be driving the load at a higher speed.
[00:34:40.210 - 00:34:41.330] And so that's it.
[00:34:41.330 - 00:34:43.810] But you can't change the load really well.
[00:34:43.810 - 00:34:48.690] If you change the load, just ways you could, you could just have to get a different propeller
[00:34:48.690 - 00:34:50.690] or maybe a bigger fan.
[00:34:52.690 - 00:34:57.490] It's normally much harder to change the load and you normally don't have much option
[00:34:57.490 - 00:34:58.930] to change the load.
[00:34:58.930 - 00:35:00.930] The load is normally determined by the application.
[00:35:00.930 - 00:35:02.210] You don't have much choice.
[00:35:03.010 - 00:35:06.130] But what you can do is you can choose the right motor that matches to the load.
[00:35:06.690 - 00:35:08.050] And this is what this is saying.
[00:35:16.030 - 00:35:20.190] And here is a few cases someone will discuss.
[00:35:30.540 - 00:35:32.780] So we have our torque.
[00:35:33.580 - 00:35:35.020] And this is what I call it a fan.
[00:35:36.300 - 00:35:42.460] And the fan torque is proportional to the speed, to the speed, squared, velocity squared.
[00:35:45.120 - 00:35:47.440] This is always the case with aerodynamics.
[00:35:47.440 - 00:35:52.640] Aerodynamics always the torque, if you're running a race and you can feel the wind against you,
[00:35:54.080 - 00:35:59.200] the aerodynamic torque on you, or the force that's on you is proportional to the square.
[00:35:59.200 - 00:36:01.120] But torque is like force times distance.
[00:36:02.560 - 00:36:05.600] And so if you've got a fixed distance, it's going to be obviously just the square.
[00:36:07.280 - 00:36:09.600] And that would be the case of the fan going around.
[00:36:09.600 - 00:36:12.960] There's a certain torque because it's got a distance and it's got a force.
[00:36:12.960 - 00:36:15.200] The force is proportional to the velocity squared.
[00:36:15.200 - 00:36:19.680] And so the torque is obviously that times the constant, which is the distance to the
[00:36:19.680 - 00:36:21.520] center of pressure of the fan.
[00:36:23.360 - 00:36:24.560] It's how the aerodynamics work.
[00:36:25.600 - 00:36:28.320] Though it always focuses on a certain point along the fan.
[00:36:34.290 - 00:36:37.410] So t is proportional to the velocity squared.
[00:36:39.170 - 00:36:40.370] And that's a really basic load.
[00:36:42.050 - 00:36:43.490] Here's another type of load.
[00:36:43.970 - 00:36:47.730] The hoist or just hoisting something up.
[00:36:47.730 - 00:36:55.980] And so when you're here, you can hit very, very flat.
[00:36:57.260 - 00:37:01.660] And no load, you don't need any speed.
[00:37:01.660 - 00:37:12.210] But here, when you actually do have a load, there is a little bit of increase.
[00:37:12.210 - 00:37:15.330] But it's mostly gravity that you have to see.
[00:37:15.330 - 00:37:19.570] When you're accounting for gravity, it's not gravity is an acceleration.
[00:37:19.570 - 00:37:21.090] It doesn't actually depend on speed.
[00:37:31.250 - 00:37:33.330] So you've got a crane that's lifting up a load.
[00:37:37.970 - 00:37:41.970] You don't need much more torque to increase the speed,
[00:37:41.970 - 00:37:45.010] mainly just because of the fact that you're overcoming an acceleration.
[00:37:45.730 - 00:37:48.050] If you want to accelerate it, obviously that's completely different.
[00:37:48.050 - 00:37:52.610] But if you just want to increase the speed, it doesn't require too much more torque to increase
[00:37:52.610 - 00:37:53.010] the speed.
[00:37:53.730 - 00:37:55.650] Once you've overcome gravity.
[00:37:55.650 - 00:37:57.730] But this is the point where you overcome gravity.
[00:37:58.530 - 00:37:59.970] So you need to have a certain torque.
[00:37:59.970 - 00:38:02.530] So it's actually, you know, you get to the point where you overcome gravity.
[00:38:02.530 - 00:38:03.970] And then after that, it's easy.
[00:38:22.060 - 00:38:23.900] We're talking about steady state operation here.
[00:38:23.900 - 00:38:26.700] There might be an initial to increase it.
[00:38:26.700 - 00:38:32.220] You may have to initially accelerate the motor to a higher velocity.
[00:38:32.220 - 00:38:33.260] But then it's going to come back.
[00:38:34.860 - 00:38:38.860] Because the steady state, you know, to overcome gravity,
[00:38:38.860 - 00:38:46.380] once you've overcome gravity, yeah, that's, like, there's not much more torque at steady state.
[00:38:50.780 - 00:38:53.980] But there are real-world destruction losses and things.
[00:38:53.980 - 00:38:57.900] So it is going to mean the faster you go, even though you've overcome gravity,
[00:38:57.900 - 00:38:59.260] it's still going to take a little bit more torque.
[00:39:11.150 - 00:39:14.190] That's why there's just a really narrow slope here, and it's pretty linear.
[00:39:19.500 - 00:39:25.260] Because most, around most friction, you can assure him there's pretty linear,
[00:39:27.490 - 00:39:31.010] at least viscous friction and bearings and things like that,
[00:39:31.570 - 00:39:34.290] teams to be a lot more linear, it's different from wind speed.
[00:39:34.770 - 00:39:37.650] Even wind speed at low wind speeds can be reasonably linear,
[00:39:37.650 - 00:39:39.810] but at the typical wind speed you get with Feyn,
[00:39:39.810 - 00:39:43.410] it's more like a squared, and there's as much more linear
[00:39:43.410 - 00:39:45.010] to the teams of friction losses.
[00:39:45.010 - 00:39:48.450] It might have slightly go up a little bit, but mostly linear.
[00:39:49.650 - 00:39:51.250] I already kind of did that previously.
[00:39:51.250 - 00:39:57.500] I might showed you the graph, but here's a little bit more kind of
[00:39:57.500 - 00:39:58.220] term-to-moulogy.
[00:39:58.780 - 00:40:04.930] So you've got this period here with the torques increasing before it drops off.
[00:40:04.930 - 00:40:07.090] So you've got to kind of get over that points,
[00:40:07.090 - 00:40:08.690] over that points called the break down torque.
[00:40:10.210 - 00:40:12.530] And this is where the rotor torque, this is where it's locked.
[00:40:14.130 - 00:40:17.970] You're getting no speed here, so if you get it locked, if you come down here, and I just like,
[00:40:17.970 - 00:40:20.530] locks out, obviously your motor's going to seize up.
[00:40:21.970 - 00:40:24.690] But you get over that point, and it's called the break down torque,
[00:40:24.690 - 00:40:26.050] and this is where you operate here.
[00:40:29.950 - 00:40:31.390] And so that's the point.
[00:40:35.540 - 00:40:41.300] So what we want to do is, here we want to be operating around
[00:40:47.250 - 00:40:48.610] of optimal efficiency.
[00:40:54.800 - 00:40:59.280] If we're powering an AC induction motor for the using AC induction motor,
[00:40:59.280 - 00:41:01.280] preparing the vertical gyro, and Cm3-Z even,
[00:41:04.590 - 00:41:06.910] because that's creating as soon as being an inverter.
[00:41:06.910 - 00:41:11.630] That's being able to create an AC waveform for a DC waveform.
[00:41:11.630 - 00:41:13.070] And I don't teach that in this course.
[00:41:13.070 - 00:41:14.910] That's just an example of an inverter.
[00:41:15.870 - 00:41:19.230] With the inverter would be powered by a motor, and you would have to design,
[00:41:19.230 - 00:41:25.950] and you'd have to have the motor, and it would depend on how much power you have
[00:41:25.950 - 00:41:31.710] from the actual engines, ultimately, because the engines are acting as the alternator,
[00:41:31.710 - 00:41:32.350] alternator.
[00:41:32.350 - 00:41:33.870] That's creating power.
[00:41:33.870 - 00:41:38.430] You're storing the batteries, but then the batteries are then being used to power an AC
[00:41:38.430 - 00:41:39.470] to induction motors.
[00:41:39.470 - 00:41:43.950] You'd have to design your AC induction motor according to how much power you could generate
[00:41:43.950 - 00:41:44.830] from the Cm3-Z.
[00:41:45.070 - 00:41:51.310] And you would make sure that you had the optimum efficiency at the speed that you were doing
[00:41:51.310 - 00:41:52.110] in the inverting.
[00:41:52.110 - 00:41:58.030] It's all depending on the application.
[00:41:59.150 - 00:42:05.980] And efficiency, when I talk about efficiency, I'm talking about the power out
[00:42:07.580 - 00:42:08.940] divided by the power n.
[00:42:14.770 - 00:42:17.250] And that's your rated speed, and your rated torque.
[00:42:21.090 - 00:42:25.250] Yeah, this is best to do with a slip condition.
[00:42:27.010 - 00:42:37.730] The way that it works, the magnetic field is always out of phase with the actual mechanical
[00:42:38.930 - 00:42:39.330] motion.
[00:42:41.250 - 00:42:42.450] So it's rotating.
[00:42:42.450 - 00:42:49.250] The big mess that's in the vehicle gyro, that'd be rotating at a certain speed, right?
[00:42:50.530 - 00:42:53.170] But the magnetic field is going to be out of phase.
[00:42:53.170 - 00:42:55.970] In fact, it's going to be lagging it, because it's trying to push it around,
[00:42:55.970 - 00:42:59.890] like this, like there's always a little bit of a lag, like you give something a push,
[00:42:59.890 - 00:43:01.970] and there's a bit of a time lag.
[00:43:01.970 - 00:43:02.850] That's called slip.
[00:43:04.210 - 00:43:08.130] So it's when the magnet field's trying to rotate something, but it's slightly out of phase
[00:43:08.130 - 00:43:09.650] with that, it's trying to push it around.
[00:43:09.650 - 00:43:11.970] It's like, ah, get moving, please.
[00:43:11.970 - 00:43:13.570] And it's like, that's the slip condition.
[00:43:18.620 - 00:43:20.700] And then I'm not going to be going too much,
[00:43:20.700 - 00:43:23.820] teaching you're really not covering AC induction motors at all.
[00:43:23.820 - 00:43:26.380] There's a lot of theory that goes into those.
[00:43:28.770 - 00:43:30.450] This is the brush of st. motor.
[00:43:33.460 - 00:43:40.160] You have these different regions, and then it kind of comes down here.
[00:43:42.080 - 00:43:46.160] You can run it all the way up to here, but you've got to be, yeah, this is called the
[00:43:46.160 - 00:43:47.120] intimate torque zone.
[00:43:48.160 - 00:43:53.120] You can't run your motor too much in that before you actually start burning out,
[00:43:54.720 - 00:43:58.000] because the speed of the motor is coming down, right?
[00:43:58.560 - 00:44:00.320] So there's a limit there.
[00:44:01.280 - 00:44:06.560] But yeah, the actual curve is normally for a brush of st. motor as relatively
[00:44:06.560 - 00:44:12.000] non-year, which is one of the real nice properties of a brush of st. motor.
[00:44:13.360 - 00:44:23.700] Then, when you get here, you are speeding up in the torque as dropping.
[00:44:24.180 - 00:44:26.340] Why is the torque dropping?
[00:44:28.340 - 00:44:32.580] Well, the drop I set up before, the drop is G2,
[00:44:33.860 - 00:44:40.640] back in F, a st.
[00:44:40.640 - 00:44:51.410] Back in F, increasing as the speed increases.
[00:44:54.580 - 00:44:58.980] Speed increases, back in F increases, and then implies that the current
[00:45:01.140 - 00:45:02.100] decreases.
[00:45:02.100 - 00:45:06.900] I won't go too much longer than that.
[00:45:07.860 - 00:45:13.410] I will maybe come back to that a little bit later, and I'll go in for time.
[00:45:15.170 - 00:45:29.360] Here is the motor as an electric load.
[00:45:32.130 - 00:45:34.450] This is a way of modeling.
[00:45:36.130 - 00:45:41.970] And, Dr. You've got like a constant voltage, be it back in F. You've got your voltage that's
[00:45:41.970 - 00:45:48.030] been applied. This could be a converter.
[00:45:50.930 - 00:45:53.170] Probably is a little bit of resistance in here.
[00:45:53.170 - 00:45:55.010] Probably should have put some resistance.
[00:45:57.810 - 00:46:10.460] There's likely small winding resistance for this losses.
[00:46:13.980 - 00:46:21.420] If it was a really big, and if it has induction mode, obviously this L here would be really large.
[00:46:22.300 - 00:46:28.180] But if it was just like a motor that's seen in your solar car, you could probably make L
[00:46:28.180 - 00:46:32.580] really small. There's always a bit of resistance.
[00:46:32.660 - 00:46:43.660] So this is the back in F. And so the current is going actually through this voltage source.
[00:46:44.220 - 00:46:46.370] Just right there.
[00:46:47.330 - 00:46:56.100] The current is going through the voltage source.
[00:47:01.870 - 00:47:06.590] What you're getting is because the current's going through there, and that's slowing the current down,
[00:47:08.980 - 00:47:12.580] it's obviously creating an electronic power loss as you go through there.
[00:47:12.580 - 00:47:15.220] You're losing your electric power.
[00:47:15.220 - 00:47:17.140] You're getting lost.
[00:47:17.140 - 00:47:19.620] Electric power is being lost as you go through there.
[00:47:30.580 - 00:47:34.980] But the electric power has to be going somewhere. You're losing electric power because of the
[00:47:34.980 - 00:47:36.980] back in F. But it has to go somewhere.
[00:47:39.180 - 00:47:42.940] Well, where it goes is it goes into the load. It goes into the mechanical load.
[00:47:45.380 - 00:47:48.100] It's delivered into the mechanical load. That's where it disappears.
[00:47:57.870 - 00:48:04.990] So it is power delivered to the mechanical load.
[00:48:13.040 - 00:48:20.510] But if you're going at a very slow speed, in the back in F is a professional speed, it's going to
[00:48:20.510 - 00:48:28.100] be small. So you're going to load back in F and then you'd get a high current.
[00:48:32.700 - 00:48:39.820] So a lot of losses and heat. But if you haven't got a good heat sink,
[00:48:40.860 - 00:48:45.900] then you might just burn up all the insulation and it might just start smoking.
[00:48:46.700 - 00:48:48.540] And who knows, it might just blow up.
[00:48:49.420 - 00:48:57.780] Not a good thing. You don't want to be running brush the stc motors too slow for too long.
[00:48:57.780 - 00:49:09.620] I'll continue. It's an offset there.
[00:49:22.350 - 00:49:25.950] So I'm going to look at this maybe running a time.
[00:49:27.150 - 00:49:27.710] A few minutes.
[00:49:30.290 - 00:49:36.820] So we've got this different quadrants breaking a lowering load.
[00:49:38.340 - 00:49:43.940] It's going in the opposite direction of rotation. So it's rotating down
[00:49:43.940 - 00:49:48.020] because you're trying to break it. It's going down. But you're actually putting the torque
[00:49:48.980 - 00:50:00.660] in the opposite direction. So and it's a positive torque because it's to the right.
[00:50:01.540 - 00:50:03.460] Use your right hand roll with the current goes.
[00:50:17.890 - 00:50:22.290] So that's going to be a positive torque just because it's just the convention.
[00:50:28.750 - 00:50:32.590] So even though the torque is going in the opposite direction, that means that the back
[00:50:32.590 - 00:50:36.990] here in the F has got to be negative because it's going in the two as a minus sign there
[00:50:41.660 - 00:50:44.780] because the back here may have gone up the direction to where you're flowing the current to try and
[00:50:44.780 - 00:50:47.820] slow it down. And this is this is this quadrant.
[00:50:48.860 - 00:50:56.900] Torque is always proportional to the current. Here the current is also positive, but now the back
[00:50:56.900 - 00:51:11.890] here myth is going in the same direction. So that's a plus V plus I. So V is the rotational direction.
[00:51:11.970 - 00:51:30.450] I, as the torque direction, so basically anti clockwise is out of the page,
[00:51:30.450 - 00:51:42.370] which I say with my thumb. Using the right hand roll, power steering,
[00:51:43.810 - 00:51:56.420] you're powering it down. It's all connected. It's not like, you know, an example here could be a crane.
[00:51:56.420 - 00:52:02.100] You don't want to be breaking a lowering load with a heavy work platform with a work platform
[00:52:02.100 - 00:52:08.140] with your workers on there. So you'd want to be operating in this quadrant for that particular
[00:52:08.140 - 00:52:23.570] application. And so there's no free for you. The free for capability is locked out.
[00:52:30.690 - 00:52:37.010] So that's this quadrant here. This one's a really interesting one. This is breaking over hoisting
[00:52:37.010 - 00:52:51.010] load. It doesn't have to be a hoisting load. It could be just breaking even a forward translational
[00:52:51.890 - 00:52:59.810] load on the car, for example. You're not going to be breaking a car by putting the torque here
[00:53:01.090 - 00:53:15.740] in the opposite direction to where you want to go. This is called regenerative braking. So then
[00:53:15.740 - 00:53:20.700] you can actually use it in the car to store when you're wanting to break up to the lights. If
[00:53:20.700 - 00:53:28.270] you use regenerative braking, it can actually put power back into your batteries because you're
[00:53:28.270 - 00:53:36.370] using, yeah, you're actually trying to negate that forward motion. Here we are over time. Yep.
[00:53:41.220 - 00:54:22.020] Okay. Thank you.

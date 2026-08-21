# ENEL372-26S2 Lecture 18 local ASR transcript

Date: August 21, 2026 9:00am-9:55am
Transcript type: Hermes-generated local ASR from validated Echo audio, not a native Echo transcript.
Backend/model: faster-whisper small.en, CPU int8, beam_size=5, vad_filter=True.
Source audio SHA-256: `f2eff88a49a24a30e7902bf307e8c842e0a568b6b33ab64dbcef65cbd967afe5`
Generated: 2026-08-22T02:40:33.133400+12:00
Caveat: technical terms, equations, names and Māori words may require checking against slides/audio.

[00:00:02.100 - 00:00:06.100] Well, Kia ora koutou, welcome along.
[00:00:06.100 - 00:00:11.100] Better get started pretty much on time so that we don't drag things out too long.
[00:00:11.100 - 00:00:16.100] Apologies for having lecture at four to five. It could be worse, could be five to six.
[00:00:16.100 - 00:00:23.100] We kind of get dictated to a little bit by timetabling. We try to make it as accommodating as possible to your timetable.
[00:00:23.100 - 00:00:27.100] I know it's probably the end of a long first day back, right?
[00:00:27.100 - 00:00:33.100] So I'll try to make it not too not too hard on you for the first lecture in right.
[00:00:33.100 - 00:00:41.100] Well, welcome along to power and analog electronics. I'll be the your course coordinator for this course.
[00:00:41.100 - 00:00:47.100] So hopefully most of you will remember me from last year, the, you know,
[00:00:47.100 - 00:00:53.100] the wonderful, lovely transistor section of electronics last year.
[00:00:53.100 - 00:01:00.100] But if those of you don't, my name is Paul Gaynor and I will be taking you for the first half of this course, right?
[00:01:00.100 - 00:01:06.100] Which is the power electronics part of the of the course or most of the power power electronics.
[00:01:06.100 - 00:01:09.100] Chris Hahn is also lecturing. He'll do the second half of the course.
[00:01:09.100 - 00:01:15.100] He'll finish off with a little bit of just rounding off with some of the material for power electronics,
[00:01:15.100 - 00:01:17.100] but not sticking on for that for too long.
[00:01:17.100 - 00:01:25.100] And then he goes on and looks at some more advanced analog electronics material for you.
[00:01:25.100 - 00:01:30.100] So just before I get into a little bit about what's covered in the course outline,
[00:01:30.100 - 00:01:35.100] just to give you a bit of a flavor of what's coming up in the course.
[00:01:35.100 - 00:01:40.100] Just quick health and safety, fire evacuation. We exit out here.
[00:01:40.100 - 00:01:47.100] There is also exit out the back. Assembly area is at the car park on the west of the building.
[00:01:47.100 - 00:01:52.100] So on that side of the of the lecture building that's blocked.
[00:01:52.100 - 00:01:57.100] Of course, there is an exit that you can do on this side of the building as well.
[00:01:57.100 - 00:02:02.100] Having gone through all of that, of course, we're only in this in this lecture room for the very first lecture.
[00:02:02.100 - 00:02:11.100] Next week we're relocating into E16. Don't come back here again Monday next week.
[00:02:11.100 - 00:02:20.900] Right. The course. So I know you can't.
[00:02:20.900 - 00:02:26.900] This is not set up for you to read as part of the course material,
[00:02:26.900 - 00:02:29.900] but it is there on learn for you to consult.
[00:02:29.900 - 00:02:32.900] And I do recommend that you consult the course outline.
[00:02:32.900 - 00:02:41.900] There is a lot of information in there that was very helpful to you and will give you a pretty good idea of what's going to come along in the course.
[00:02:41.900 - 00:02:51.900] So just very, very briefly in this course, we kind of build on that basic knowledge that you gained last year in the NEL 270.
[00:02:51.900 - 00:02:59.900] But then we move on into more detailed elements of power electronics and the important basic or fundamental areas there.
[00:02:59.900 - 00:03:12.340] And also into some analog electronics, but for a greater understanding of what's happening when those those circuits.
[00:03:12.340 - 00:03:21.340] So this part of the course outline sort of like gives you a bit bit more of a breakdown of the things that we will cover through the course.
[00:03:21.340 - 00:03:31.340] Don't want to spend much time on that. You will be getting it as we go through in that in that in the coursework through the through the different lectures.
[00:03:31.340 - 00:03:38.340] I do want to just mention briefly, though, a little bit about the assessment.
[00:03:38.340 - 00:03:53.770] So a big chunk of this course is a group project, a design and build project where you do a power converter for a small model solar powered car.
[00:03:53.770 - 00:04:01.770] So it's worth 30 percent. And like I said, it's group project group of three.
[00:04:01.770 - 00:04:12.770] We it's a big a big thing. So we're spending an entire lecture talking about elements of the project next week.
[00:04:12.770 - 00:04:21.770] So just letting you know about that. There is also some invigilated assessment.
[00:04:21.770 - 00:04:27.770] So there's a test with 35 percent in an exam with 35 percent.
[00:04:27.770 - 00:04:35.770] There is also a requirement in this course to get an average 40 percent for passing the course overall.
[00:04:35.770 - 00:04:46.770] So even if you do really, really well in the project group project, then and but do very poorly in the test and an exam on average,
[00:04:46.770 - 00:04:52.770] then we can't let you pass the course if they did well in the project.
[00:04:52.770 - 00:05:00.770] So just keep an eye on that so that you do pay attention to when it comes to doing your invigilated assessments.
[00:05:00.770 - 00:05:18.960] Right. There is more information in the course outline about the use of generative AI where it can and can't be utilized in the different assessments.
[00:05:18.960 - 00:05:27.300] I think it's pretty self-explanatory so that you can't use it in the test or exam.
[00:05:27.300 - 00:05:41.080] OK. How are electronics then? That's the material that I'm going to be covering to a great extent for this first half of the course.
[00:05:41.080 - 00:05:53.080] So I'm going to take a little bit of a step back to the kind of the basic introductory material that I did go over in NEL 270 last year.
[00:05:53.080 - 00:05:58.080] Like I said, don't want to make this too hard for the first lecture, just getting back into the swing of things.
[00:05:58.080 - 00:06:02.080] Right. So just a bit of a refresher in this instance.
[00:06:02.080 - 00:06:07.080] We will be talking a little bit more detail, though, than what we did get into last year.
[00:06:08.080 - 00:06:27.080] Power electronics. What is it? Well, what we are really drilling down into here is the efficient conversion of electrical power between what can be various kinds of sources of that energy, electrical energy to different kinds of loads.
[00:06:27.080 - 00:06:31.080] That's what it boils down to in a nutshell.
[00:06:32.080 - 00:06:47.080] And power electronics, for a few decades now, has really, really taken off and it is found everywhere you find electronic systems.
[00:06:47.080 - 00:06:57.080] All right. So diagram here. I showed that diagram last year in NEL 270 just kind of threw out there as just some pictures and some examples.
[00:06:57.080 - 00:07:09.080] Just a little bit more detail this time around. So here on the top left hand, we've got examples of what's becoming more and more common in power networks.
[00:07:09.080 - 00:07:14.080] And that's distributed power generation, particularly from renewable sources.
[00:07:14.080 - 00:07:18.080] So we've got two examples of photovoltaic and wind.
[00:07:18.080 - 00:07:33.080] So these types of energy sources don't provide the electricity or the electrical power or energy in the form that is compatible with directly connecting to the mains network.
[00:07:33.080 - 00:07:39.080] All right. So there has to be some kind of interfacing that goes on there.
[00:07:39.080 - 00:07:44.080] And that's where the power electronics comes in. And it does it extremely efficiently.
[00:07:44.080 - 00:07:53.080] So it's a pretty big deal when you're looking at the power levels involved with our national level power networks.
[00:07:53.080 - 00:08:06.080] Hands in hand with that is there's a big move towards moving away from AC networks for power transmission, large scale, to DC.
[00:08:07.080 - 00:08:24.080] Some very, very good reasons for that. You lose all of the sort of losses associated with the reactive currents associated with parasitic inductance and capacitance over the transmission network if you go to DC.
[00:08:24.080 - 00:08:32.080] So there's a lot of work there, but it can only be done with modern power electronics.
[00:08:32.080 - 00:08:38.080] It doesn't mean that power electronics is going to be really, really tiny like you might be used to.
[00:08:38.080 - 00:08:43.080] Like this network here stands about 20 meters tall.
[00:08:43.080 - 00:08:48.080] So it's a very, very large power electronic systems we're talking about.
[00:08:48.080 - 00:08:59.080] It doesn't have to be all that sort of enormous scale. Of course, we're finding power electronics a lot more for the use of transportation applications,
[00:08:59.080 - 00:09:13.080] not only directly for tractive systems, so powering the vehicle to move along as we have in our electric vehicles, but also even in the management of electric power on other types of transportation like aircraft.
[00:09:13.080 - 00:09:23.080] So the power that comes from the generators on board and electric aircraft is not compatible with the various electronic systems throughout the aircraft.
[00:09:23.080 - 00:09:32.080] So there needs to be a very energy efficient way of converting from that source power from the generators to what's needed through that aircraft.
[00:09:32.080 - 00:09:44.080] It's not to say that just around the corner or a little bit down the track that we wouldn't also be starting to look at actual main motive power for aircraft as well.
[00:09:44.080 - 00:09:50.080] As well as other things like large scale transportation, trains and shipping.
[00:09:51.080 - 00:09:59.390] That's all well and good. Again, talking pretty large scale, but that's not just the only space that we find power electronics.
[00:09:59.390 - 00:10:03.390] Of course, there's been a big revolution in lighting.
[00:10:03.390 - 00:10:11.390] All the lighting that we have around here is LED based.
[00:10:11.390 - 00:10:15.390] And just a few short years ago, that wasn't the case.
[00:10:15.390 - 00:10:25.390] The efficiency levels of lighting were in general way, way less than a tenth the efficiency that it is now.
[00:10:25.390 - 00:10:33.390] So big changes being made in that space. Only possible through the use of power electronics.
[00:10:33.390 - 00:10:36.390] And the power management on mobile devices.
[00:10:36.390 - 00:10:39.390] So what do we need to have happen for our mobile devices?
[00:10:39.390 - 00:10:45.390] We need the energy in the battery to last as long as possible between charges.
[00:10:45.390 - 00:10:51.390] We don't want to be forever having to stop whatever activity we're doing on our mobile devices to recharge.
[00:10:51.390 - 00:10:58.390] So power management through our mobile devices is incredibly important.
[00:10:58.390 - 00:11:02.390] And again, only achievable through power electronic systems.
[00:11:02.390 - 00:11:13.390] And then finally, of course, industry. Industry, maybe we've got motor speed control, motors and movement in industry is a big deal.
[00:11:13.390 - 00:11:22.390] Any kind of process now where you are looking at generating a lot of heat, as you do in a number of industrial processes,
[00:11:22.390 - 00:11:28.390] is moving away from traditional things like gas and coal to electric power systems.
[00:11:28.390 - 00:11:33.390] Again, needing to rely very, very heavily on power electronics.
[00:11:33.390 - 00:11:52.110] All right. So we're focusing on a bit. Right. So in its most basic kind of sense,
[00:11:52.110 - 00:12:03.110] this efficient conversion of electric power is obtained through the utilization of using semiconductor switches in just two states,
[00:12:03.110 - 00:12:08.110] either in fully on state or fully off state.
[00:12:08.110 - 00:12:18.110] If we can do that, then we can use we basically have very, very little power loss or dissipation in the semiconductor switches themselves.
[00:12:18.110 - 00:12:28.110] And we use them hand in hand with low loss energy, temporary or transient energy storage components.
[00:12:29.110 - 00:12:36.110] It's just a fancy way of saying we also we use the switches in conjunction with inductors and capacitors.
[00:12:36.110 - 00:12:52.180] So those combined are really basically the cornerstone of virtually all of the power electronics and is the is the reason why we can achieve such high efficiencies.
[00:12:52.180 - 00:12:58.520] Sure, we could convert power using semiconductors in the linear mode and it is done.
[00:12:58.520 - 00:13:03.520] We have our linear voltage regulators, for example. Right.
[00:13:03.520 - 00:13:12.520] They can be sometimes done with reasonable efficiency, topping out at around about 80 percent or so.
[00:13:12.520 - 00:13:21.520] We find that way more often, though, in most applications, considerably less efficiency than that peaking of 80 percent.
[00:13:21.520 - 00:13:36.520] And also, there are some functions that you can achieve through the storage capabilities of especially inductors that offer this functionality that you just cannot get from linear systems.
[00:13:36.520 - 00:13:40.520] We'll be we'll be investigating some of that.
[00:13:40.520 - 00:13:48.520] So that being the case, linear power conversion, while it is power conversion, is not part of the space of power electronics.
[00:13:48.520 - 00:13:57.520] It is not part of the technical applications or theory space that we define as being power electronics.
[00:13:57.520 - 00:13:58.520] Right.
[00:13:58.520 - 00:14:00.520] They are something separate.
[00:14:00.520 - 00:14:03.520] They would just be high power analog electronics.
[00:14:03.520 - 00:14:06.540] OK.
[00:14:06.540 - 00:14:16.330] A general block diagram we've got there of it's just of a generic overall power electronics system.
[00:14:16.330 - 00:14:27.330] So we have input power that may have some kind of voltage waveform, could be DC, could be AC, some just just general voltage.
[00:14:27.330 - 00:14:35.330] Of course, power, if we've got an electrical system, always goes voltage, always goes hand in hand with current.
[00:14:35.330 - 00:14:36.330] Right.
[00:14:36.330 - 00:14:38.330] So we've got I of X as well at the input.
[00:14:38.330 - 00:14:43.330] So we'd say that's input power P X.
[00:14:44.330 - 00:14:48.330] There is usually some form of input filter.
[00:14:48.330 - 00:15:07.330] Now, filters, if just with the basic sort of experience, most of you have had you'd think of something like an RC low pass filter or even a high pass filter can can be structured out of a capacitor and then a resistor resistor component.
[00:15:07.330 - 00:15:08.330] Of course, it's lossy.
[00:15:08.330 - 00:15:11.330] If there's any current flowing through it, there's voltage drop across it.
[00:15:11.330 - 00:15:12.330] Power dissipated.
[00:15:12.330 - 00:15:23.330] The type of filter we're talking about here is a lossless filter that's comprised of capacitors and inductors to do the low pass and high pass function.
[00:15:23.330 - 00:15:24.330] Right.
[00:15:24.330 - 00:15:33.760] So they're effectively lossless in concept.
[00:15:33.760 - 00:15:44.760] Of course, everything that is physically existence based and carries current through it will have some physical resistance and therefore will dissipate some level of power.
[00:15:44.760 - 00:15:49.760] And you can't have perfect or 100 percent efficiency, but it's pretty good.
[00:15:49.760 - 00:15:51.760] There's not much loss.
[00:15:51.760 - 00:15:56.760] Then we have a switching converter switching.
[00:15:56.760 - 00:16:04.760] Sometimes you hear different terminologies being used for these converters switching converter or very often you would hear switch mode.
[00:16:04.760 - 00:16:13.440] All right.
[00:16:13.440 - 00:16:18.040] So switching converter or if you hear switch mode, they mean the same thing.
[00:16:18.040 - 00:16:25.770] An output filter also lossless made of capacitors and inductors.
[00:16:25.770 - 00:16:40.770] And then we have our because we've gone through a switching converter, our altered voltage and current still with effectively the same amount of power minus some kind of losses.
[00:16:40.770 - 00:16:53.300] So we'd say we've got an output P Y, which has some alternative voltage and current being completely general here.
[00:16:53.300 - 00:17:00.300] We'd say then that P X is equal to P Y plus whatever losses there might be.
[00:17:00.300 - 00:17:06.250] But those would be small.
[00:17:06.250 - 00:17:24.940] These losses and modern power electronics if you do the design right can be as low as just one or two percent.
[00:17:24.940 - 00:17:46.940] OK. That's all well and good. But most often we have in general terms electronic systems there with a load may have some variation or conversely even the source may have some variation that we need to adjust parameters within our switching converter to handle those changes.
[00:17:46.940 - 00:17:52.940] So if we're going to have that sort of situation and this one is an example of where the load might change.
[00:17:52.940 - 00:18:02.380] We need to do some measurements and feed that into some sort of electronic controller.
[00:18:02.380 - 00:18:21.380] You'll compare what you're measuring against some sort of reference and then from that the processing that goes on in the controller output some kind of control variable that changes the conditions in our switching converter to compensate for those changes either in the load or in the in the source.
[00:18:23.720 - 00:18:59.990] Most power electronic systems will involve some kind of feedback in it. You're going to experience this sort of overall arrangement in your in your design and build project, which is not just building a power converter, but it is a controlled power converter that will have feedback associated with it.
[00:18:59.990 - 00:19:15.400] All right. It's time to start defining some things to get our terminology correct for if we're talking knowledge of believe within the field of power electronics.
[00:19:15.400 - 00:19:30.400] So we'll talk about some classifications then for power electronics. So again, the idea is convert from some source of electrical power to provide energy to a load of some sort.
[00:19:31.400 - 00:19:56.920] And we need to do that efficiently. So that source of electrical power could be from a regulated source. So regulated just means that there are some controlled fixed parameters.
[00:19:56.920 - 00:20:16.560] So a regulated AC source is probably going to have voltage or current to a particular level and probably also frequency.
[00:20:16.560 - 00:20:28.980] For example, mains, as it's identified there, has all of those things fixed. Well, the voltage is fixed. Current can be variable depending on the load.
[00:20:28.980 - 00:20:37.980] So the source could be regulated AC unregulated AC, for example, from something that has a variable amount of energy that is being obtained.
[00:20:38.980 - 00:20:53.980] So wind turbine below a certain scale. So the sort of frequency and magnitude of the of the the voltage and current from those can be quite variable.
[00:20:53.980 - 00:20:58.980] So that's what's known as an unregulated source. That's the AC side.
[00:20:58.980 - 00:21:02.980] Of course, we've got DC as well. Right. So we could have a regulated DC.
[00:21:02.980 - 00:21:12.980] So something from, say, the output from a computer power supply or an unregulated DC. So a battery is a great example there.
[00:21:12.980 - 00:21:21.360] As you discharge a battery, its voltage will vary as the level of charge reduces.
[00:21:21.360 - 00:21:29.360] Then you have that and you would output to usually a regulated output of AC power.
[00:21:29.360 - 00:21:38.360] Now, that regulated output doesn't necessarily mean that you have to fix your parameters in time completely, but they are controlled parameters.
[00:21:38.360 - 00:21:50.360] So this could be some variability there, which you are controlling through some sort of feedback network and control and controller, but it is definitely a controlled system.
[00:21:53.220 - 00:22:14.330] Right. OK, so to encapsulate all of that, there is a diagram that we can utilize, which is a conversion function diagram.
[00:22:14.330 - 00:22:24.330] And it shows you the sort of, I guess, power electronic conversions in the basic type shown there.
[00:22:24.330 - 00:22:33.330] So these parallel lines here look like equals that is identifying a DC system.
[00:22:33.330 - 00:22:44.330] So we have the ability to go from DC to DC as a converter. That's the type like the buck converter from last year.
[00:22:44.330 - 00:22:53.330] So DC to DC. So you might show that as a system that looks like this. So it'd be a DC to DC converter.
[00:22:53.330 - 00:23:08.800] Then we might be talking about going from DC to AC. All right, so you'd show that like this or AC to AC, maybe even AC to DC.
[00:23:08.800 - 00:23:13.800] So those are the conversions that we find ourselves with. Don't worry necessarily about this.
[00:23:13.800 - 00:23:18.800] I'll come back to why we've broken it up into two blocks shortly.
[00:23:18.800 - 00:23:31.190] So power electronics enables all kinds of efficient power conversion and over a very, very wide power range.
[00:23:31.190 - 00:23:44.190] So all the way from gigawatts, which is your national level power transmission scale, utility scale, all the way down to milliwatts.
[00:23:44.190 - 00:23:57.190] So it doesn't show an actual application space there in between in your tens of watts to hundreds of watts, your consumer products, milliwatts.
[00:23:57.190 - 00:24:04.190] They're the sort of things that you might have saved for medical implants, electrical medical implants.
[00:24:04.190 - 00:24:10.190] So the power management of those, I think you understand, are pretty important to get right.
[00:24:10.190 - 00:24:24.980] So they don't take a lot of power, though. So that is milliwatts. Also, there are a number of Internet of Things sensor networks that work down at those sorts of power levels as well.
[00:24:24.980 - 00:24:39.200] So I'll keep that one there. We'll refer back to that because of the two fundamental forms of electric power.
[00:24:39.200 - 00:24:47.200] So whether it's AC or DC is what I'm talking about, the fundamental forms there, you find four major classifications.
[00:24:47.200 - 00:24:56.200] We've kind of just gone over. So you can have AC to DC converters, DC to DC, DC to AC and AC to AC.
[00:24:56.200 - 00:25:07.200] All right. So some terminology, DC to DC and AC to AC converters are simply known as converters, right?
[00:25:07.200 - 00:25:14.200] There's no sort of fancy name for those. There is, however, alternative names for the other two.
[00:25:14.200 - 00:25:26.200] So AC to DC is something that we have come across already in ENL 270. That's technically referred to as rectification.
[00:25:26.200 - 00:25:33.200] All right. So AC to DC. So those types of converters are called rectifiers.
[00:25:33.200 - 00:25:43.200] You can have not just the type that we did look at, which was just made up of diodes, you can have controlled rectifiers as well.
[00:25:43.200 - 00:25:50.200] All right. You can have also the DC to AC converters are often called inverters.
[00:25:50.200 - 00:26:01.200] So you're going from something which is a constant voltage or if a fixed polarity to a time varying AC waveform.
[00:26:01.200 - 00:26:12.960] Right. So those are called inverters. OK. So I mentioned with it, we'll be talking about those sort of separate blocks from the previous diagram.
[00:26:12.960 - 00:26:34.170] So this DC to DC conversion sometimes, depending on the type of application and what's required of our converters, you actually need to go DC to AC first and then take the AC and convert it back to DC.
[00:26:34.170 - 00:26:38.170] They sound rather counterintuitive to do that. Why would we do that?
[00:26:38.170 - 00:26:44.170] I'll explain further when we get into that material in the course.
[00:26:44.170 - 00:26:56.170] On the other side, for AC to AC, we may need to go from AC to DC and then do a DC to DC and back to DC to AC.
[00:26:56.170 - 00:27:01.170] This is beyond the scope of the course. But this for this type of it gets a little complicated.
[00:27:01.170 - 00:27:12.020] So we won't be covering that. But just be aware that sometimes we need to break break the systems up, which is what we have here.
[00:27:12.020 - 00:27:23.020] So sometimes to avoid nonlinearity problems or to match load conditions properly, we might need to also electrically isolate one from the other one side from the other.
[00:27:23.020 - 00:27:36.020] Then we break it up into the two types. So what I just mentioned. So if we had AC at the input and we want AC at the output.
[00:27:37.020 - 00:27:42.020] Actually, the better one, the more common that we would be considering is DC at the input.
[00:27:42.020 - 00:27:55.020] So you have DC to AC and converter one, some sort of filter, and then you go AC to DC at the output.
[00:27:55.020 - 00:28:01.020] So a DC to DC converter overall. So DC in and DC out.
[00:28:01.020 - 00:28:07.020] Different voltage levels, which means, of course, that the current would also be different.
[00:28:07.020 - 00:28:17.590] Each one having its own control circuits. So DC to AC inverter and AC to DC rectifier.
[00:28:17.590 - 00:28:47.430] OK, different types of application. They're really, it's everywhere.
[00:28:48.430 - 00:28:59.430] This is a table I pulled out of a textbook, one of the recommended textbooks that's identified in the course outline, which I kind of skipped over.
[00:28:59.430 - 00:29:06.430] There's the textbooks that are in there are actually on short term loan in the ESL.
[00:29:06.430 - 00:29:13.430] So if you need to refer to those from some of the material, then they're on short term loan there.
[00:29:14.430 - 00:29:33.060] So there's domestic applications, there's commercial, industrial, the transportation that I kind of mentioned before, utility systems, aerospace is gaining more and more, and of course telecoms.
[00:29:33.060 - 00:29:40.060] Transportation, just a bit of interest sake, that's an area where I personally do some research.
[00:29:40.060 - 00:29:51.060] So I'm looking at new types of power converter that go between the battery of an electric vehicle and the AC machines that drive the motion.
[00:29:51.060 - 00:29:59.060] Currently, the world is dominated by a particular type of inverter that is utilized.
[00:29:59.060 - 00:30:05.060] It's called a two level or three level inverter, which basically switches between high voltage buses.
[00:30:05.060 - 00:30:17.060] The type of converter that I'm looking at to alleviate some of the problems associated with that are known as multi-level inverters, and they behave much more like a staircase type of arrangement.
[00:30:17.060 - 00:30:21.060] I have a particular interest in the transportation area.
[00:30:21.060 - 00:30:42.410] All right, so just before we get into considering some of our power electronic converters and analyzing them and their behavior, we'll just take a review, a quick review.
[00:30:42.410 - 00:30:51.410] And even off our electronic switches that we tend to utilize, and even introduce a couple of new ones which most of you wouldn't have seen before.
[00:30:51.410 - 00:31:08.670] All right, so diodes. Hopefully diodes is something that we're comfortable with, come across before, and reasonably understand what sort of behavior we have with diodes.
[00:31:08.670 - 00:31:14.670] So two terminals, one's called the anode, one's called the cathode.
[00:31:14.670 - 00:31:23.670] Current can only flow once you've overcome the required forward bias conditions for the diode, can only flow from anode to cathode.
[00:31:23.670 - 00:31:36.670] All right, so you put a positive voltage on the anode with respect to the cathode beyond around about 0.7 volts for silicon diodes.
[00:31:36.670 - 00:31:40.670] And we'll have conduction through the diode.
[00:31:40.670 - 00:31:52.670] If the cathode is positive with respect to the anode, so it's positive-negative that way, no current can flow, no effective current can flow.
[00:31:52.670 - 00:31:57.670] So that's the blocking region for the diode.
[00:31:57.670 - 00:32:06.670] It's reverse biased. So here's a diagram of what you might think of a realistic diode would have.
[00:32:06.670 - 00:32:17.670] It doesn't immediately turn on at full capability, so it has some finite resistance, which gets less and less as it turns on.
[00:32:17.670 - 00:32:26.670] It's why the curve gets steeper and steeper. One over the slope is the effective forward resistance of the diode.
[00:32:26.670 - 00:32:33.670] So it becomes more conductive as you get a further forward bias on that diode.
[00:32:33.670 - 00:32:43.670] And in reverse, effectively, you might get a tiny amount of leakage current through the reverse that's measured in the nanoamps region.
[00:32:43.670 - 00:32:53.670] But until you get to a certain level where the diode can now no longer withstand the electrostatic forces involved and you'll get conduction going in the opposite direction.
[00:32:54.670 - 00:33:06.670] Usually in an avalanche type of situation, which, unless it's designed for it, doesn't like doing it and can very well destroy the diode if you go too far beyond the rated reverse voltage.
[00:33:06.670 - 00:33:18.660] That's all well and good for most applications, especially for power electronics, which involve slightly larger voltages.
[00:33:19.660 - 00:33:25.660] We, in first instances, usually consider a diode in its ideal state.
[00:33:25.660 - 00:33:37.660] So zero current for reverse bias. As soon as it goes forward bias, it's zero ohm forward bias situation.
[00:33:37.660 - 00:33:41.660] So it acts like a short circuit once we've forward biased it.
[00:33:41.660 - 00:33:46.380] And when it's reverse biased, it looks like an open circuit.
[00:33:46.380 - 00:33:56.380] Keep the concepts relatively clear of the complicating factors of looking at the forward diode voltage drop.
[00:33:56.380 - 00:34:12.760] We will be mostly assuming an ideal diode state because we will be utilizing diodes a bit.
[00:34:12.760 - 00:34:24.620] All right, transistors. Hopefully we can recall at least something about enhancement MOSFETs from last year.
[00:34:24.620 - 00:34:27.620] So that's what we've got on this side here.
[00:34:27.620 - 00:34:43.620] With this diode identified in reverse across the drain to source, it highlights the fact that to physically construct an enhancement MOSFET, there is an inherent body diode, which is part of that construction.
[00:34:43.620 - 00:34:50.620] So this is parasitic and we can't construct an enhancement MOSFET without it being there.
[00:34:50.620 - 00:35:00.100] So the output characteristic curves show in here.
[00:35:00.100 - 00:35:08.100] So here's the drain to source voltage and here are the separate curves for increasing gate to source voltage.
[00:35:08.100 - 00:35:15.100] So by the way, it's identifying the curve immediately below the label.
[00:35:15.100 - 00:35:24.880] So a gate to source voltage of zero volts and the MOSFET is in its off state.
[00:35:24.880 - 00:35:50.220] So for our enhancement MOSFETs, you need to, this is an N channel type, for our enhancement MOSFETs, you need to at least go with a gate to source voltage that is greater than the threshold voltage of that MOSFET.
[00:35:50.220 - 00:35:57.220] Threshold voltages, normally about two to three volts for a power MOSFET.
[00:35:57.220 - 00:36:07.220] And we would normally operate a power MOSFET at least in the realms of 10 volts for conventional power MOSFETs.
[00:36:07.220 - 00:36:31.630] So way, way, way above the threshold and making sure that we work in the ohmic region for turn on.
[00:36:31.630 - 00:36:41.630] So those are the only two regions that we would work in is the cutoff with the VGS is equal to zero and the ohmic region for a VGS that is really quite large.
[00:36:41.630 - 00:36:48.200] So we are extremely confident that we will be working in the ohmic region.
[00:36:48.200 - 00:36:59.200] Such that we see these curves, we would approximate in an ideal sense that in its off state, there is no current flow drain to source.
[00:36:59.200 - 00:37:11.820] And in its on state, there is no forward resistance, the RDS on is effectively zero for our MOSFET.
[00:37:11.820 - 00:37:20.820] Again, ignoring the middle transistor for a second and looking at the transistor on the right hand side, that's a bipolar junction transistor.
[00:37:20.820 - 00:37:23.820] So we've come across those before.
[00:37:23.820 - 00:37:33.820] MOSFETs, enhancement MOSFETs, voltage controlled current device, bipolar junction transistors, a current controlled current device.
[00:37:33.820 - 00:37:48.820] So to turn this on and off, you need to either have zero base current, zero base current will mean that the transistor is in its off state and it looks like it's in the cutoff region.
[00:37:48.820 - 00:38:00.820] So you can apply enough base current to provide the conditions for a large collector and therefore emitter current.
[00:38:00.820 - 00:38:04.820] So there is a current gain going through the device.
[00:38:04.820 - 00:38:16.480] So it's just a scalar for the amount, the more the base current, the greater the collector current, which is what those curves are telling us there.
[00:38:16.480 - 00:38:26.310] For power BJTs, they're not like small signal BJTs.
[00:38:26.310 - 00:38:38.310] Power BJTs, to enable them to carry a lot of current, have a semiconductor construction which means that they don't have great current gains.
[00:38:38.310 - 00:38:48.310] So small signal BJT, current gains 1, 2, 3, 100 amps per amp.
[00:38:48.310 - 00:38:51.310] So that's the kind of current gain that you get through.
[00:38:51.310 - 00:38:57.310] A power BJT, 50 to 80, so not very good.
[00:38:57.310 - 00:39:11.140] Which means if you've got a lot of current that you're trying to control for the power electronic converter, then potentially you need quite a lot of base current as well.
[00:39:11.140 - 00:39:15.140] To overcome that effect a little bit, there is a special configuration that's utilized.
[00:39:15.140 - 00:39:29.620] This is known as a Darlington pair, which basically is a cascaded connection of two power bipolar transistors.
[00:39:29.620 - 00:39:40.620] And what this does is it basically takes the current gain of one, which could be 50 or 80 or so, and multiplies it by the gain of the other.
[00:39:40.620 - 00:39:44.620] So it's a way of enhancing the overall current gain.
[00:39:44.620 - 00:39:48.620] There's a downside to that. I'll get to that very shortly.
[00:39:48.620 - 00:40:04.420] So, enhancement MOSFETs, they are extremely fast switching devices.
[00:40:04.420 - 00:40:11.420] It means they transition between the off state to the on state and from the on state to the off state extremely quickly.
[00:40:11.420 - 00:40:15.420] For good ones, you're talking tens of nanoseconds.
[00:40:15.420 - 00:40:18.420] So very quickly.
[00:40:18.420 - 00:40:30.240] Bipolar junction transistors is quite slow.
[00:40:30.240 - 00:40:43.240] However, for larger currents, they actually have a lower collector to emitter voltage than the drain to source voltages of MOSFETs.
[00:40:43.240 - 00:40:47.240] So they kind of effectively look like they've got a smaller on resistance.
[00:40:47.240 - 00:40:52.240] So their efficiency on the power side is actually a little bit better than it is for MOSFETs.
[00:40:52.240 - 00:40:56.240] So they don't get quite as hot at those higher currents.
[00:40:56.240 - 00:41:04.580] So they can handle higher currents.
[00:41:04.580 - 00:41:08.580] They handle high-ish currents, but not as high as bipolar transistors.
[00:41:08.580 - 00:41:18.820] So that's what we have. It's a bit of a trade off.
[00:41:18.820 - 00:41:22.820] So that's the sort of things that you start to consider in certain application spaces.
[00:41:22.820 - 00:41:27.820] Do we need really fast switching or do we need a little bit higher current capability?
[00:41:27.820 - 00:41:33.990] Right, the transistor in between.
[00:41:33.990 - 00:41:40.990] This is a special device that was developed as modern power electronics started taking hold.
[00:41:40.990 - 00:41:44.990] It's called the insulated gate bipolar transistor, or IGBT.
[00:41:44.990 - 00:41:58.170] The really cool thing about IGBTs is that they can give you characteristics that are a bit of both worlds from MOSFETs and BJTs.
[00:41:58.170 - 00:42:10.170] So they're a voltage controlled current device, but the input behaves like a MOSFET, but the output behaves like a bipolar transistor.
[00:42:10.170 - 00:42:16.170] So you have this nice effect of a low saturation voltage across the collector to emitter.
[00:42:16.170 - 00:42:19.170] So it still has a collector emitter, but it has a gate.
[00:42:19.170 - 00:42:26.170] So you have the positive effect of good efficiency at high currents.
[00:42:26.170 - 00:42:34.170] And because it's a voltage control across an insulated gate, it actually has quite high switching speeds.
[00:42:35.170 - 00:42:44.550] So fast switching, not extremely fast switching, fast switching with high current.
[00:42:44.550 - 00:42:58.010] So you will see it's in some applications the use of these things called IGBTs.
[00:42:58.010 - 00:43:01.010] And here you go, that's what they effectively are.
[00:43:01.010 - 00:43:10.010] A voltage controlled current device that has features of both MOSFETs as per the input and bipolar transistors in their output.
[00:43:10.010 - 00:43:19.980] Any questions?
[00:43:19.980 - 00:43:26.280] Try not to put you to sleep. We're just about there. Not too far.
[00:43:26.280 - 00:43:32.280] I talked a lot then. You might forget what I said.
[00:43:32.280 - 00:43:37.280] Most of what I've just said is there in text already following. All right.
[00:43:37.280 - 00:43:42.750] Done that part for you.
[00:43:42.750 - 00:43:47.750] Let's say, though, that we need to go to extremely high voltages and currents.
[00:43:47.750 - 00:43:54.750] So MOSFETs, IGBTs, bipolar transistors cannot satisfy that space of application.
[00:43:54.750 - 00:43:59.750] We need to go to another type of semiconductor switching set of devices.
[00:43:59.750 - 00:44:03.750] And this is where we find the thyristors.
[00:44:03.750 - 00:44:10.750] So they are big scale switching devices.
[00:44:10.750 - 00:44:14.750] They include something known as the silicon controlled rectifier.
[00:44:14.750 - 00:44:17.750] You can find small versions of these with lower current.
[00:44:17.750 - 00:44:21.750] Don't find much application space for them anymore, though.
[00:44:21.750 - 00:44:27.750] The triac, the gate turn off thyristor and the MOS controlled thyristor.
[00:44:27.750 - 00:44:35.020] So here's an SCR.
[00:44:35.020 - 00:44:42.020] The circuit diagram or the circuit symbol is quite instructive.
[00:44:42.020 - 00:44:50.020] It behaves like a diode that you can choose when it starts conducting in forward bias.
[00:44:50.020 - 00:44:59.020] So it won't conduct anode to cathode if you forward bias it unless you give it a pulse on the gate.
[00:44:59.020 - 00:45:04.020] So it could be your reverse bias. It behaves just like a reverse bias diode.
[00:45:04.020 - 00:45:11.340] Forward bias, it still will not conduct until you hit it with a gate pulse.
[00:45:11.340 - 00:45:16.340] As soon as you hit it with a gate pulse, so this is a voltage pulse that you apply.
[00:45:16.340 - 00:45:18.340] It doesn't have to be constant.
[00:45:18.340 - 00:45:22.340] Voltage pulse that you apply to the gate, it will suddenly turn on.
[00:45:22.340 - 00:45:26.340] So it might have been going forward bias, forward bias, a positive voltage.
[00:45:26.340 - 00:45:30.340] Hit the gate, boom, it starts conducting and its voltage drops to zero.
[00:45:30.340 - 00:45:33.940] And it starts conducting.
[00:45:33.940 - 00:45:38.940] To turn an SCR off, you cannot turn it off with the gate.
[00:45:38.940 - 00:45:46.940] You have to wait until the conditions in the circuit mean that the current falls to zero and the bias goes to reverse bias.
[00:45:46.940 - 00:45:50.940] It's the only way you can turn them off once they've been turned on.
[00:45:50.940 - 00:45:58.500] Once you've hit them with a gate, they act just like a diode.
[00:45:58.500 - 00:46:01.780] Right.
[00:46:01.780 - 00:46:06.780] If you do need that extra functionality of being able to turn it off under a controlled time,
[00:46:06.780 - 00:46:11.780] then you might need to go to a gate turn off, a GTO.
[00:46:11.780 - 00:46:13.780] So that's gate turn off.
[00:46:13.780 - 00:46:14.780] Right.
[00:46:14.780 - 00:46:22.780] So that's given a different symbol there, which identifies that you can both turn it on at forward bias and turn it off when it's forward biased.
[00:46:22.780 - 00:46:32.260] The gate pulse that you need, though, tends to be quite substantial in current.
[00:46:32.260 - 00:46:33.260] Right.
[00:46:33.260 - 00:46:42.260] So, whilst it's only a pulse to turn them, it is a significantly large current pulse, which can affect its overall efficiency.
[00:46:43.260 - 00:46:52.250] So these, when the current is in one direction, they act like diodes.
[00:46:52.250 - 00:47:03.130] If you need bipolar, bidirectional current flow, then you need to go to a triac.
[00:47:03.130 - 00:47:08.130] So a triac, it behaves like an SCR that's bidirectional.
[00:47:08.130 - 00:47:10.130] So you hit it with a gate pulse.
[00:47:10.130 - 00:47:13.130] If it's biased one way, it'll start conducting.
[00:47:13.130 - 00:47:16.130] You can't turn it off until the bias is reversed.
[00:47:16.130 - 00:47:24.130] And then under that reverse bias again, if you hit the gate pulse again, it will conduct in that reverse condition.
[00:47:24.130 - 00:47:31.130] And it'll keep conducting until, again, the bias conditions flip around and it reverse biases.
[00:47:31.130 - 00:47:35.470] So that's how a triac works.
[00:47:35.470 - 00:47:43.070] These are MOS-controlled thyristors, MCTs.
[00:47:44.070 - 00:47:50.070] They have the added functionality of being able to choose when to turn it on and off.
[00:47:50.070 - 00:47:53.630] Right.
[00:47:53.630 - 00:47:54.630] Right.
[00:47:54.630 - 00:47:59.630] So extremely high currents and voltages for these types of devices.
[00:47:59.630 - 00:48:01.630] What's the downside?
[00:48:01.630 - 00:48:28.340] They are extremely slow in their switching characteristics.
[00:48:28.340 - 00:48:32.340] To remain efficient, then you cannot be switching these things very quickly.
[00:48:32.340 - 00:48:38.340] Because of that, only ever utilized at mains frequency applications.
[00:48:38.340 - 00:48:56.940] It's all well and good to be stating what these switches, where they work and whether it's high current and high voltage.
[00:48:56.940 - 00:49:05.940] But to get a mental picture and where you might look at utilizing, by the way, that's just text to explain those various thyristors.
[00:49:06.940 - 00:49:11.940] It can really help to have that shown in a diagram, which is what we have here.
[00:49:11.940 - 00:49:17.370] So here's current.
[00:49:17.370 - 00:49:20.370] So as we go up in current, you go initially with MOSFETs.
[00:49:20.370 - 00:49:23.370] But if you need to hire current, you go to IGBTs.
[00:49:23.370 - 00:49:25.370] You can then go to MCTs.
[00:49:25.370 - 00:49:27.370] BJTs are there as well.
[00:49:27.370 - 00:49:33.370] Gate turnoffs and then the other thyristors involved here.
[00:49:34.370 - 00:49:37.370] So like an SCR.
[00:49:37.370 - 00:49:44.370] For the switching frequency, if you need to go up to really high frequency, the MOSFETs are your only choice.
[00:49:44.370 - 00:49:47.370] Lower and lower frequency, we get the big devices.
[00:49:47.370 - 00:49:49.370] And the voltage capability is shown here.
[00:49:49.370 - 00:49:53.370] So MOSFETs pop out a little above a KV.
[00:49:53.370 - 00:49:57.370] IGBTs, you can actually get 4 KV IGBTs now.
[00:49:58.370 - 00:50:03.370] GTOs come up and around 5,000 volts or so for your thyristors.
[00:50:03.370 - 00:50:09.300] Really just the last thing.
[00:50:09.300 - 00:50:15.300] Switch selection basically depends on the application space and what you are required from it.
[00:50:15.300 - 00:50:21.300] You can experience from different types of circuits.
[00:50:21.300 - 00:50:24.300] And finally, CAD and circuit simulation.
[00:50:24.300 - 00:50:29.300] Rather than having to build our power electronic circuits every time, we have a design idea.
[00:50:29.300 - 00:50:32.300] Very often use circuit simulation.
[00:50:32.300 - 00:50:36.300] It's based very often on a SPICE simulation engine.
[00:50:36.300 - 00:50:40.300] So that's simulation program with integrated circuit emphasis.
[00:50:40.300 - 00:50:47.300] And you will be using LTSPICE for the project to do some basic simulation work with.
[00:50:47.300 - 00:50:49.300] That's it.
[00:50:49.300 - 00:50:51.300] Well done.

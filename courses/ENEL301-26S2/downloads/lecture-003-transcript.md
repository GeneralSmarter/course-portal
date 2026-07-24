# ENEL301-26S2 Lecture 3 fast-pass local ASR transcript

Date: July 21, 2026 1:00pm-1:55pm
Transcript type: Hermes fast-pass local ASR from validated Echo audio, not a native Echo transcript.
Backend/model: faster-whisper tiny.en, CPU int8, beam_size=1, vad_filter=True.
Quality note: fast catch-up transcript. Technical terms, equations, names and Māori words need checking against slides/audio before assessment use.
Source audio SHA-256: `18f3625e9ac48aca2eb4e325c5034287ee7c2f8af3c5126fc081007caedacc30`
Generated: 2026-07-24T23:48:58.964939+12:00

[00:00:01.230 - 00:00:05.760] Yeah, it's all good.
[00:00:05.760 - 00:00:08.760] Yeah, oh, strange quiet.
[00:00:08.760 - 00:00:12.760] Kota Koto, I hope you're doing well on Tuesday.
[00:00:12.760 - 00:00:16.760] Welcome to the students in 300.
[00:00:16.760 - 00:00:23.760] So if you're in the only 300 just a reminder that you can use today's lecture as part of your guest lecture series.
[00:00:23.760 - 00:00:28.760] Just a couple of admin items before I hand over to Andre.
[00:00:28.760 - 00:00:33.760] So yeah, your tutorial rooms for our tutorial B,
[00:00:33.760 - 00:00:36.760] time-tabbling we're playing silly buggers in the last week,
[00:00:36.760 - 00:00:39.760] and they've changed some rooms at the last minute.
[00:00:39.760 - 00:00:44.760] So before your tutorial tomorrow just make sure you check your time table
[00:00:44.760 - 00:00:48.760] to make sure that you go into the right place.
[00:00:48.760 - 00:00:53.760] Yeah, and attendance for the bicultural workshops will be taken.
[00:00:53.760 - 00:00:56.760] Yeah, so make sure you're there.
[00:00:56.760 - 00:01:02.760] Yeah, so it's been great pleasure to introduce you to Andre Conia,
[00:01:02.760 - 00:01:05.760] who's one of two guest lectures today.
[00:01:05.760 - 00:01:08.760] And Carla who joins some of you might know from Compage.
[00:01:08.760 - 00:01:10.760] It's going to be your other one.
[00:01:10.760 - 00:01:13.760] So yeah, I'll hand over to Andre.
[00:01:13.760 - 00:01:14.760] Kota.
[00:01:14.760 - 00:01:15.760] Got my gilda.
[00:01:15.760 - 00:01:16.760] Gilda, Toto.
[00:01:16.760 - 00:01:22.040] Just before we get out, just want to set some expectations.
[00:01:22.040 - 00:01:27.040] Today's lesson is not on Tika Mommarri or the Tirit, or the Tittility.
[00:01:27.040 - 00:01:30.040] It's a conversational or corridor about engineering,
[00:01:30.040 - 00:01:33.040] organizational capability leadership and relationships.
[00:01:33.040 - 00:01:37.040] So if you were thinking you were going to get some spell about Tika Mommarri,
[00:01:37.040 - 00:01:39.040] then I apologize in advance.
[00:01:39.040 - 00:01:45.040] However, I am going to use the Mutateki Star constellation as a framework
[00:01:45.040 - 00:01:49.040] for the corridor that I am going to provide you guys this afternoon.
[00:01:49.040 - 00:01:54.040] So I'm going to use that particular framework to sort of go through
[00:01:54.040 - 00:01:59.040] organizational change, capability build and relation to Meridian's journey.
[00:01:59.040 - 00:02:04.040] And just to sort of clear things up for those that don't know Meridian's power company.
[00:02:04.040 - 00:02:08.040] So I just want to make sure that we all kind of knew what Meridian was.
[00:02:08.040 - 00:02:09.040] Couple of you.
[00:02:09.040 - 00:02:10.040] All right.
[00:02:10.040 - 00:02:14.480] So I'm going to get a few things sort of sort of first.
[00:02:14.480 - 00:02:16.480] This is the company's disclaimer.
[00:02:16.480 - 00:02:19.480] So I just need to make sure that I sort of mentioned some of this first and foremost.
[00:02:19.480 - 00:02:23.480] So I'm not just prepping off what I think Meridian do,
[00:02:23.480 - 00:02:27.480] just so that we can provide a wee bit of a context around what it is that Meridian do
[00:02:27.480 - 00:02:30.480] and where they sit inside out there all New Zealand.
[00:02:30.480 - 00:02:42.020] So Meridian being part of Altair to on New Zealand's energy transition out work is connected to renewable generation.
[00:02:42.020 - 00:02:48.040] And those four particular points there are part of our strategy.
[00:02:48.040 - 00:02:53.040] Those little circles down the bottom are our kind of company values.
[00:02:53.040 - 00:02:55.040] But I just want to sort of touch on these.
[00:02:55.040 - 00:02:58.040] 100% renewable, what are that energy comes from, what are all Sun?
[00:02:58.040 - 00:03:05.040] And I think if you saw those particular TV commercials that had that woman who was probably pretending to be pop or two in look,
[00:03:05.040 - 00:03:09.040] you would have probably picked up that renewable energy was our thing.
[00:03:09.040 - 00:03:16.040] So on top of that we generate approximately around about 35% of New Zealand's total electricity needs.
[00:03:16.040 - 00:03:21.040] Our hydropower is our main source of energy generation.
[00:03:21.040 - 00:03:27.040] Assets include the monopodie power station in the wire, way down south.
[00:03:27.040 - 00:03:33.040] And then which is using its largest and then six stations within the Waitaki hydro scheme.
[00:03:33.040 - 00:03:40.040] We also have wind and solar, one in sort of southland Waitheau,
[00:03:40.040 - 00:03:47.040] two in Wellington, three in the monowet, two, one in the Hughks Bay.
[00:03:47.040 - 00:03:55.040] And we're in the process of building a solar farm and a western side of Lake Topo.
[00:03:55.040 - 00:03:59.040] And also building just that sort of farm that a south of Fungare.
[00:03:59.040 - 00:04:06.040] So and we are on the build as the energy demand for wild turtles,
[00:04:06.040 - 00:04:09.040] and stripping our current supply.
[00:04:09.040 - 00:04:13.040] So I just wanted to sort of detail kind of company disclaimer.
[00:04:13.040 - 00:04:18.270] Just a little bit about myself.
[00:04:18.270 - 00:04:24.270] I think if you've done those cultural courses you kind of get to the stage where you kind of deal with a bit of a fair behind you introduce yourself.
[00:04:24.270 - 00:04:26.270] So I want to keep it really short.
[00:04:26.270 - 00:04:31.270] So you're more comfortable enough to tie it off to Hughru and O'Narti Prote, if I don't know what one we are.
[00:04:31.270 - 00:04:35.270] I'm going to talk about Rama Tiro and O'Narti and Rapakil and I'll keep up with that.
[00:04:35.270 - 00:04:39.270] So I'm a descendant of the east coast of the North Island.
[00:04:39.270 - 00:04:42.270] My Tiro and O'Narti Prote define our upon me.
[00:04:42.270 - 00:04:47.270] My connection to the Wai Poh Nami is through my wife.
[00:04:47.270 - 00:04:52.270] She's from a little sediment on the, if you go through the little tunnel and you sort of make your way around towards Governor Space.
[00:04:52.270 - 00:04:54.270] She's from a little place called Rapakil.
[00:04:54.270 - 00:04:59.270] And that's my connection to Wai Poh Nami, I met at University many, many moons ago.
[00:04:59.270 - 00:05:01.270] And I've been kind of following around ever since.
[00:05:01.270 - 00:05:03.270] We have a couple of kids.
[00:05:03.270 - 00:05:05.270] Two daughters.
[00:05:05.270 - 00:05:08.270] That was, I took a photo of that particular image of my father.
[00:05:08.270 - 00:05:13.270] And it's probably because that was at the time there were probably at the most cutest where they actually thought I was pretty good.
[00:05:13.270 - 00:05:17.270] However, they both had high school, not both the girls, so I just down the road.
[00:05:17.270 - 00:05:24.270] And these are a couple of, these are three of my Narti on the east coast.
[00:05:24.270 - 00:05:27.270] And the interesting thing is that when I started at Meridian,
[00:05:27.270 - 00:05:34.270] one of the induction courses they took us through the history of electricity in New Zealand.
[00:05:34.270 - 00:05:43.270] And the hilarious thing is all those three of my Narti have only just recently got onto Maine's electricity.
[00:05:43.270 - 00:05:49.270] And I thought that was a bit of a crack up because they're telling us about this history of electricity starting back in the 1800s.
[00:05:49.270 - 00:05:50.270] And I sort of tune around.
[00:05:50.270 - 00:05:51.270] So we'll do.
[00:05:51.270 - 00:05:55.270] We're on my family homesteads right next to this one I hear.
[00:05:55.270 - 00:05:59.270] And we were still on diesel generator right up till 2015.
[00:05:59.270 - 00:06:03.270] So that was only, yeah, it was only just recently.
[00:06:03.270 - 00:06:08.270] That one there still looks like it's kind of could be set in the 1800s.
[00:06:08.270 - 00:06:15.270] However, however, I digress, but this is kind of a wee bit about my family where I'm from on the east coast.
[00:06:15.270 - 00:06:19.270] Educated up north. I know it's a very contemporary and thing to ask you what school you attended.
[00:06:19.270 - 00:06:23.270] And so I don't know if I could have down here.
[00:06:23.270 - 00:06:25.270] I went to a Mardi Bautie school anyway.
[00:06:25.270 - 00:06:28.270] So most people would have pronounced it or wouldn't know where it was anyway.
[00:06:28.270 - 00:06:33.270] So on that note, that's a little bit about kind of my own fuckup hopper.
[00:06:33.270 - 00:06:53.930] The role I play at Meridian, co-hosts who Mardi, so 2020 KPMG that are report on how really corporate entities were to engage in
[00:06:53.930 - 00:06:58.930] relationships and partnerships with Ewe.
[00:06:58.930 - 00:07:06.930] And the development of not just the capability of staff, but also around employee data.
[00:07:06.930 - 00:07:12.930] And so we needed a bit of a survey and they produced the paper.
[00:07:12.930 - 00:07:18.930] What came out of it was the small amount of knowledge they knew about the treaty.
[00:07:18.930 - 00:07:23.930] A little than you about actually who they were, who worked for Meridian.
[00:07:23.930 - 00:07:31.930] And what the ethnic makeup was particularly of Mardi employees, which was quite astounding to be fair because there's around about 900 employees.
[00:07:31.930 - 00:07:37.930] Spread across four major offices and then we've got eight, nine sites or assets as well.
[00:07:37.930 - 00:07:39.930] So it was a bit sort of odd.
[00:07:39.930 - 00:07:43.930] I think it's quite good in terms of the Matariki concept here.
[00:07:43.930 - 00:07:49.930] But we understand we'll be coming from and we'll be out in order to sort of plot the path into we'll be hitting.
[00:07:49.930 - 00:07:55.930] So basically there were three points that came out of report that led to the creation of the co-hosts who Mardi role.
[00:07:55.930 - 00:08:00.930] So in 2023 they went out to market and I was appointed.
[00:08:00.930 - 00:08:04.930] Basically, there's a summary of what I do for a role.
[00:08:04.930 - 00:08:10.930] And the key part here is that I don't stick to just one particular aspect with a Meridian.
[00:08:10.930 - 00:08:17.930] So you have the those that go around and check out all of the different sites around the country.
[00:08:17.930 - 00:08:30.930] So this could be a really good place for solar energy or wind or there's a decent source river that could create enough to potentially invest in a particular hydro scheme.
[00:08:30.930 - 00:08:33.930] So we have that particular department of development.
[00:08:33.930 - 00:08:37.930] We also have those that once the asset is built referring to your generation.
[00:08:37.930 - 00:08:44.930] So once you've plugged it into the grid, you have that particular gig or business unit, shall I say.
[00:08:44.930 - 00:08:51.930] Then you have retail and then retails what you guys will see when you're ringing out to put your house or flat on onto the power.
[00:08:51.930 - 00:08:55.930] Whether or not it's Meridian or power shop, I think they're both owned by us.
[00:08:55.930 - 00:08:58.930] And then there's the retail.
[00:08:58.930 - 00:09:01.930] I'm not popped out all up. It's around about 900 employees.
[00:09:01.930 - 00:09:04.930] So we have quite a few.
[00:09:04.930 - 00:09:08.930] The biggest actual biggest office is actually here in crosshitch.
[00:09:08.930 - 00:09:10.930] And that's purely just retail.
[00:09:10.930 - 00:09:15.930] So most of the time, line up is into the time when you've got a complaint from power shop or Meridian.
[00:09:15.930 - 00:09:18.930] It's likely to get an operator from here in crosshitch.
[00:09:18.930 - 00:09:24.930] And that's just basically majority of our retail position here.
[00:09:24.930 - 00:09:28.930] However, I'm not sort of saying I've drank the call aid.
[00:09:28.930 - 00:09:30.930] Marine is a good employer.
[00:09:30.930 - 00:09:35.930] And we do believe in a public post COVID lockdown.
[00:09:35.930 - 00:09:42.930] There are not many of us, I'd say probably about 40% of our workforce now work from home or in a hybrid form.
[00:09:42.930 - 00:09:44.930] I'm one of them.
[00:09:44.930 - 00:09:49.930] So even though I love just like a form and a drive down the road from here,
[00:09:49.930 - 00:09:53.930] and about an eight minute drive from my house to the office,
[00:09:53.930 - 00:09:56.930] due to the nature of my work, I travel a lot.
[00:09:56.930 - 00:10:00.930] So the trade-off here has said I work in a hybrid role.
[00:10:00.930 - 00:10:06.930] And many of the future roles that we're going to be developing over the next 10, 15 years take out into account.
[00:10:06.930 - 00:10:10.930] I think the workforce has changed and as a result we need to change with it.
[00:10:10.930 - 00:10:18.790] So Matriaki, Matriaki represents reflection.
[00:10:18.790 - 00:10:23.790] And I think it's quite pertinent just because we had to not just go to be at the public holiday just recently.
[00:10:23.790 - 00:10:26.790] And I don't want to be preaching what all the nine stars of Matriaki is.
[00:10:26.790 - 00:10:29.790] If you wanted to do that, you could probably YouTube,
[00:10:29.790 - 00:10:34.790] bring you my tab who was a courted or an presentation on Matriaki.
[00:10:34.790 - 00:10:36.790] But I'm going to draw some environment here.
[00:10:36.790 - 00:10:42.790] So, representing reflection, connection, well-being and collective strength of the constellation.
[00:10:42.790 - 00:10:46.790] It kind of gets me thinking about a particular fokatoku.
[00:10:46.790 - 00:10:48.790] It's a takutori takutori.
[00:10:48.790 - 00:10:50.790] It's a takutori takutori.
[00:10:50.790 - 00:10:56.790] Which really kind of says my strength is not mine alone, but the strength of meaning.
[00:10:56.790 - 00:11:02.790] So for me the fokutoku sits alongside Matriaki because it reminds us that strength is collective.
[00:11:02.790 - 00:11:07.460] No single star creates the constellation.
[00:11:07.460 - 00:11:13.460] The power of Matriaki is not only the individual stars, but the relationship between them.
[00:11:13.460 - 00:11:17.740] So Matriaki gives us a great understand transition,
[00:11:17.740 - 00:11:22.740] because it asks us to pause on what was passed,
[00:11:22.740 - 00:11:24.740] said, of course, for the year ahead.
[00:11:24.740 - 00:11:28.740] Those are the same disciplines that carry a company
[00:11:28.740 - 00:11:30.740] through transition.
[00:11:30.740 - 00:11:33.740] Now, Meridian is managing a several of those transitions being
[00:11:33.740 - 00:11:37.740] fossil fuels to renewables, monocultural practice,
[00:11:37.740 - 00:11:42.740] to treaty honoring practice, consultation to partnership,
[00:11:42.740 - 00:11:45.740] and one generation of leaders to the next.
[00:11:45.740 - 00:11:52.080] We're not treating transition as only a technical challenge.
[00:11:52.080 - 00:11:55.080] It's also relationship challenge,
[00:11:55.080 - 00:11:57.080] a leadership challenge,
[00:11:57.080 - 00:12:01.080] and an organisational behaviour challenge.
[00:12:01.080 - 00:12:03.080] So when people never get it by the stars,
[00:12:03.080 - 00:12:07.080] they didn't just follow one single point.
[00:12:07.080 - 00:12:10.080] They read everything around them.
[00:12:10.080 - 00:12:14.080] And that's the lesson I want to carry into this particular kind of subject area,
[00:12:14.080 - 00:12:20.080] as you cannot manage transition by reading community and generational systems around it.
[00:12:20.080 - 00:12:24.080] So the first engineering lesson is no major transition
[00:12:24.080 - 00:12:28.080] as managed to retitenacle capability alone.
[00:12:28.080 - 00:12:30.080] So you can give a smartest step in the room,
[00:12:30.080 - 00:12:32.080] but unless you bring people along with you,
[00:12:32.080 - 00:12:36.080] that's probably going to fall on DFE as an important unlikely to take three of wings.
[00:12:36.080 - 00:12:39.080] Particularly in big companies like Meridian,
[00:12:39.080 - 00:12:42.080] I'm not saying that it's not completely out of the question.
[00:12:42.080 - 00:12:48.080] However, bringing people along for the right kind of sounds like basic human psychology in a way,
[00:12:48.080 - 00:12:53.080] that you've got to bring people along with you a bit like a sports team.
[00:12:53.080 - 00:12:55.080] Technical capability matters,
[00:12:55.080 - 00:12:59.080] because it enables change, but relationships sustain it.
[00:12:59.080 - 00:13:05.080] Now that's the thread I want you to hold onto as we sort of go through these different stars in the constellation of Matadiki.
[00:13:05.080 - 00:13:07.080] Before we can understand where we're going,
[00:13:07.080 - 00:13:10.080] we must first acknowledge those who came before us.
[00:13:10.080 - 00:13:15.950] But who to color?
[00:13:15.950 - 00:13:20.950] But who to color connects us to those who've gone before us and the legacies they leave behind?
[00:13:20.950 - 00:13:24.950] A kamu or kamu walking towards walking backwards into the future.
[00:13:24.950 - 00:13:27.950] Now that's a kind of a fucking talk here that basically,
[00:13:27.950 - 00:13:30.950] this is walking backwards into the future,
[00:13:30.950 - 00:13:35.950] what it's really kind of alluding to here is that even though you might be moving in this direction,
[00:13:35.950 - 00:13:38.950] what we're really staring at as those who've come before us,
[00:13:38.950 - 00:13:40.950] also understanding our history,
[00:13:40.950 - 00:13:48.950] understanding that we're standing on the shoulders of those that came before us to do a good job.
[00:13:48.950 - 00:13:52.950] So, at Meridian Technology,
[00:13:52.950 - 00:13:56.950] our storage history, we acknowledge those who've built the hydro schemes, the dams,
[00:13:56.950 - 00:13:59.950] tunnels and infrastructure from which we generate our powerful.
[00:13:59.950 - 00:14:02.950] We acknowledge those who lost their lives in the work.
[00:14:02.950 - 00:14:05.950] We acknowledge the staff that moved on.
[00:14:05.950 - 00:14:11.950] The leaders who shaped the organization, the external relationships that continue to influence,
[00:14:11.950 - 00:14:13.950] our thinking and operations.
[00:14:13.950 - 00:14:22.580] Because infrastructure can sometimes make us focus on what stands permanently in the landscape.
[00:14:22.580 - 00:14:28.580] But every dam, tunnel, station and scheme also carries human stories.
[00:14:28.580 - 00:14:31.580] Some are stories of innovation and courage,
[00:14:31.580 - 00:14:33.580] and some are stories of sacrifice,
[00:14:33.580 - 00:14:37.580] and some of the lessons we're still learning from.
[00:14:37.580 - 00:14:41.580] One of the things I've learned in my role was that none of us start from zero.
[00:14:41.580 - 00:14:44.580] So, we're not starting right at the very beginning.
[00:14:44.580 - 00:14:49.580] We can hear infrastructure, knowledge, relationships and responsibilities,
[00:14:49.580 - 00:14:53.580] and every generation leaves something behind for the next.
[00:14:53.580 - 00:14:55.580] But like the quarter of the car,
[00:14:55.580 - 00:15:04.580] we're here to take a car, which is a proverb that refers to the front on a silver spoon.
[00:15:04.580 - 00:15:07.580] We're from full zoop another one replaces it.
[00:15:07.580 - 00:15:10.580] It's a wee bit like the warrior analogy.
[00:15:10.580 - 00:15:13.580] We want warrior, dies another one more place.
[00:15:13.580 - 00:15:19.580] And so it's a kind of a nice way to consider that capability might leave a company,
[00:15:19.580 - 00:15:28.270] but it will be replaced with or not it's through a pathway or whether or not it's through bringing someone in.
[00:15:28.270 - 00:15:35.540] So, the inheritance can be technical and it can be operational.
[00:15:35.540 - 00:15:37.540] It also could be cultural.
[00:15:37.540 - 00:15:40.540] It could also be relational, just as we inherit assets.
[00:15:40.540 - 00:15:43.540] We also inherit relationships.
[00:15:43.540 - 00:15:47.540] The strength of those relationships influence the trust we hold today
[00:15:47.540 - 00:15:51.540] and the opportunities available to future generations.
[00:15:51.540 - 00:15:57.050] Now, when we invite and we host events,
[00:15:57.050 - 00:15:59.050] particular assets,
[00:15:59.050 - 00:16:09.050] we've very fixated on the health and safety procedures upon entering a hydro scheme.
[00:16:09.050 - 00:16:19.050] One of those particular aspects that was probably absent before I arrived was what was the cultural component
[00:16:19.050 - 00:16:21.050] that we overlaid.
[00:16:21.050 - 00:16:26.550] Because if we think about our values that we spoke of earlier,
[00:16:26.550 - 00:16:30.550] so being a good human, being gutsy or being in the walker,
[00:16:30.550 - 00:16:44.120] being able to host and ensure that there was an overlay or a perspective around the mari world view to health and safety.
[00:16:44.120 - 00:16:53.120] We also have an ESOP stand that operated procedure for hosting events with EWE with monofinua on our assets.
[00:16:53.120 - 00:17:02.120] And that's kind of all fits under that particular paradigm of a consultation,
[00:17:02.120 - 00:17:09.120] agreed expectations around how we host to ensure that we're not offending anyone.
[00:17:09.120 - 00:17:17.120] And we've taken into consideration what other processes related to the start of the event to the closing event,
[00:17:17.120 - 00:17:24.120] including those standard induction type courses, induction type processes.
[00:17:24.120 - 00:17:33.120] So the real challenge in terms of when KPNG did an audit, I suppose, around how well they could,
[00:17:33.120 - 00:17:40.120] how well Meridian treated Marty employees work with EWE and what the cultural capital literally looked like.
[00:17:40.120 - 00:17:46.120] Quite often, really up for good people just didn't know.
[00:17:46.120 - 00:17:50.120] And so as a result, now we're trying to apply what good looks like.
[00:17:50.120 - 00:17:56.120] So you might be doing this by cultural workshops over the week to understand what,
[00:17:56.120 - 00:18:00.120] what being a by cultural citizen and alter or new zinnomite looked like.
[00:18:00.120 - 00:18:05.120] The real challenge for most companies is how do we apply this treaty honoring practice?
[00:18:05.120 - 00:18:10.120] And so one of these examples we use is,
[00:18:10.120 - 00:18:20.120] we might be a body or there may have been an accident or an incident near or within the confines of our asset.
[00:18:20.120 - 00:18:25.120] So we have massive lake, we have a dam in the middle of it, and some was the form of the boat,
[00:18:25.120 - 00:18:27.120] which actually happened earlier this year.
[00:18:27.120 - 00:18:34.120] And the wire person fell from a boat, body bit missing for several days.
[00:18:34.120 - 00:18:37.120] We were missing, okay, what are the considerations?
[00:18:37.120 - 00:18:43.120] Obviously we need to, we work in class communications with the police.
[00:18:43.120 - 00:18:52.120] We also did, applying really good cultural practice was around aliasing and communicating with the local EWE down there and say,
[00:18:52.120 - 00:18:54.120] I can walk this look like for you guys.
[00:18:54.120 - 00:18:57.120] What would be a standard practice?
[00:18:57.120 - 00:19:00.120] What would be a standard practice?
[00:19:00.120 - 00:19:05.120] I think the translation means prohibition, you know, prohibitive.
[00:19:05.120 - 00:19:07.120] So we put our R we in place.
[00:19:07.120 - 00:19:09.120] We said, well what does that mean for us?
[00:19:09.120 - 00:19:14.120] Because we generate power, we had researchers doing some scientific research in that particular area.
[00:19:14.120 - 00:19:21.120] So we sort of sat down, had a bit of a discussion around where the area that they were looking.
[00:19:21.120 - 00:19:24.120] So basically they went from one end of the lake to the other.
[00:19:24.120 - 00:19:27.120] And can our scientists still operate in any area?
[00:19:27.120 - 00:19:29.120] What's the compromise there?
[00:19:29.120 - 00:19:35.120] What is it that we can do to help and support both those that are looking for this particular individual?
[00:19:35.120 - 00:19:37.120] How is it that we can still operate?
[00:19:37.120 - 00:19:42.120] As a company that's generating 55% of New Zealand's electricity?
[00:19:42.120 - 00:19:47.120] And how is it that we can be really good in terms of our cultural sensitivity and bi-cultural understanding?
[00:19:47.120 - 00:19:55.120] As treaty honouring company to ensure that we're taking care of what good sound,
[00:19:55.120 - 00:19:57.120] seek out a marty might look like.
[00:19:57.120 - 00:20:00.120] And so through those particular conversations we can at one room.
[00:20:00.120 - 00:20:02.120] It said this is what we're going to do.
[00:20:02.120 - 00:20:06.120] We can operate in student areas and tools.
[00:20:06.120 - 00:20:09.120] All of the search has been conducted.
[00:20:09.120 - 00:20:17.120] If we recover, if any of our employees or our science researchers discover the body,
[00:20:17.120 - 00:20:28.120] then we set up another set of rules and regulations to ensure that we're doing things not just safe by policing the search and rescue,
[00:20:28.120 - 00:20:32.120] but also by ensuring that cultural etiquette is taking care of.
[00:20:32.120 - 00:20:34.120] And so that's kind of what we adopt.
[00:20:34.120 - 00:20:42.120] And it's a similar process we do when we're hosting EWE on our assets to ensure that we're trying to get it right.
[00:20:42.120 - 00:20:47.120] So it's not something that we've had sitting in the cabinet for 23 years.
[00:20:47.120 - 00:20:51.120] This is an iterative process because it's a bit of a one-size-foot spot.
[00:20:51.120 - 00:20:56.120] We notice what works down here with Naito who does not work up in Horgesbae with Naito Gohununu.
[00:20:56.120 - 00:21:03.120] Nor does it work in Fangaray with Nāpa who is about having a loose enough guideline or a process that allows us to develop a body.
[00:21:03.120 - 00:21:10.120] So we develop a particular kind of engagement framework to allow us to move forward together.
[00:21:10.120 - 00:21:15.940] So, fresh water.
[00:21:15.940 - 00:21:23.940] As we kind of touched on a wee bit around that, majority of our assets are in the fresh water area.
[00:21:23.940 - 00:21:39.020] YT. YT, our generation renewable reminds me of a particular quarter of the Fatsunwara model, the Tama Tātoy Tū, the Finnur.
[00:21:39.020 - 00:21:45.020] That people are merely transient and the Finnur will remain.
[00:21:45.020 - 00:21:47.020] The landscape will still remain.
[00:21:47.020 - 00:21:49.020] People disappear.
[00:21:49.020 - 00:21:55.020] Land will remain from a really YT connects directly to our generation, both in the YT-C-Mina party.
[00:21:55.020 - 00:21:58.020] Fresh water systems that underpin renewable electricity.
[00:21:58.020 - 00:22:03.020] Traditionally, our engineers are often trying to think about resources in terms of utility.
[00:22:03.020 - 00:22:06.020] Design, productivity and efficiency.
[00:22:06.020 - 00:22:08.020] And those things matter.
[00:22:08.020 - 00:22:11.020] YT invites us to widen the lens.
[00:22:11.020 - 00:22:14.020] Fresh water should not be treated early as engineering input.
[00:22:14.020 - 00:22:18.020] It carries cultural, environmental and intergenerational responsibility.
[00:22:18.020 - 00:22:29.020] So, as an aside, sustainability is a important and critical business unit within our organization.
[00:22:29.020 - 00:22:32.020] It doesn't sit on purely on its own.
[00:22:32.020 - 00:22:38.020] It actually sits across the organization whether you're in development, generation or retail.
[00:22:38.020 - 00:22:41.020] So, we take that quite seriously.
[00:22:41.020 - 00:22:46.020] And we use international measures to ensure that we're kind of getting it right.
[00:22:46.020 - 00:22:54.020] And we actually work very closely with our E.V. partners around what this good sound sense of sustainability practices look like.
[00:22:54.020 - 00:23:07.020] Whether it's just looking at decarbonisation of all of our vehicles to modern day slavery in terms of our labour workforce.
[00:23:07.020 - 00:23:13.020] And on top of that, around impact that we have on the environment.
[00:23:13.020 - 00:23:22.020] And one of the mitigating reasons or mitigating measures that we've got in place that are annually reviewed to ensure that we're working towards getting that right.
[00:23:22.020 - 00:23:34.180] YT-C-C-C-T-I from the mountain to the sea.
[00:23:34.180 - 00:23:42.810] I won't spend too much on this particular area, but basically following the system from the top of the mountain out to the sea.
[00:23:42.810 - 00:23:49.810] We do, I'm probably for Monopodian in particular, we do discharge from fresh water environment out to the sea.
[00:23:49.810 - 00:23:55.810] But it also brings into account our trip and transfer program, which I believe,
[00:23:55.810 - 00:24:02.810] we'll talk a little bit about when it gets up and has a bit of a board at all with you.
[00:24:02.810 - 00:24:29.560] The key part here is that we put in place with a depth of our practices to ensure that the journey of an E.V. from the top out to sea is as best as we can kind of put together considering we've got a big scheme that takes up the entire river.
[00:24:29.560 - 00:24:41.560] And ensuring we've got these kind of little eel traps to be able to catch the eel before they get sort of chopped up in two bonds, transport them so that they can grow.
[00:24:41.560 - 00:24:48.560] And then once they get heavier enough, it's around about 4.4 kilograms, then we affect them up again because they get caught in the trap.
[00:24:48.560 - 00:24:54.560] And then we drop them down outside of that particular hydro scheme and then they go out to sea.
[00:24:54.560 - 00:25:10.560] And now that's a cultural consideration is we know that Naito, prolific around the ability to propagate and harvest food.
[00:25:10.560 - 00:25:14.560] I think the two mania choirs, what they would food to their heirs.
[00:25:14.560 - 00:25:23.560] So this particular cultural consideration, we don't have it operating across our assets because we'll go back to that beginning about one one size, that's one.
[00:25:23.560 - 00:25:43.560] But that's one of those particular considerations, the cultural consideration, which then becomes a technical way of actually ensuring that we are developing that we've got the capability to adapt our existing schemes to ensure that we're trying to minimize the risk of eels being caught up in our two bonds.
[00:25:43.560 - 00:25:48.560] I mean, it's not good for the two bond as well, definitely not good for the tuna.
[00:25:48.560 - 00:26:06.560] But we use data as a particular example around everything in that whole ecosystem as an issue and as important to us whether it be in the river beside it or other particular factors that affect their into the source then which we generate energy.
[00:26:06.560 - 00:26:19.570] Why Puneurang? Why water, Puneur, spring, rain and the sky?
[00:26:19.570 - 00:26:26.570] Enclosed catchments, climate variability or influence renewable energy generation and the long-term decision-making.
[00:26:26.570 - 00:26:40.910] So, as a corner, we have a code of corner and within that code of conduct we're doing the right thing, even when the right thing requires pausing, reassessing or changing course.
[00:26:40.910 - 00:26:55.910] And so our treaty honouring practice in that particular aspect was a classic example of using that rahui that was put in place by the local Roonunga and Muri Haku in February this year.
[00:26:55.910 - 00:27:20.910] It's sort of even though that corner hinders us as a business, taking a pause and seeing how we can support to ensure that, and I'm sure you've probably all heard of the two rahui before to show that we can kind of a balance the consideration of that.
[00:27:20.910 - 00:27:29.910] Also, the consideration in the environment and then being able to continue our generation of electricity.
[00:27:29.910 - 00:27:39.910] So, why Puneurang is really around managing for variable environments, the conditions.
[00:27:39.910 - 00:27:57.910] And that's where the smart cookies in the room come to play because it's about understanding the full context and having those particular ability to ascertain and articulate what are the key issues in order to make variations to our operations to get the best outcome possible.
[00:27:57.910 - 00:28:11.580] Roonungi, Wundan adaptation.
[00:28:11.580 - 00:28:18.580] So, the connection, Wundan is part of our renewable generation of future.
[00:28:18.580 - 00:28:36.580] Harapaki, the Harapaki Wundan farm, if you're coming into landing from the south into the Napier airport and you look to the left, you'll see on the hill landscape a whole lot of one-two bonds.
[00:28:36.580 - 00:28:47.580] And those two bonds are massive. Like if you think the ones in the Manuatu are big, you need to have a look at the ones in the whole space, huge.
[00:28:47.580 - 00:28:51.580] And that was considered during lockdown.
[00:28:51.580 - 00:29:05.580] And so, being able to have to build that around lockdown was a freedom itself being able to get consent for massive trucks, not just to build the road to get to the site,
[00:29:05.580 - 00:29:14.580] but actually being able to negotiate with government to bring a ship and that was big enough to hold these blades because we couldn't bring them in and parts.
[00:29:14.580 - 00:29:23.580] They came in big solar pieces and even those, we still needed to get certain trailers that were able to sort of bring them in.
[00:29:23.580 - 00:29:36.580] The trailers that you probably wouldn't see too often and it was lucky. I think lockdown was probably a blessing in the skies because there weren't too many sort of cars allowed out, but I think the feet here was actually getting this up and running.
[00:29:36.580 - 00:29:42.580] And I don't think, don't quote me, but I don't think we'll probably do something on that magnitude again.
[00:29:42.580 - 00:29:50.580] It was just the one-two-bines were massive and the land was pretty tough to build stuff on.
[00:29:50.580 - 00:29:59.580] However, however, it's probably generates the most of the power out of all of our one-desits.
[00:29:59.580 - 00:30:18.220] And I think the key part and the key looting for us at Meridian was the engineers succeeded more succeed not by controlling change but by depth into it.
[00:30:18.220 - 00:30:31.220] And so the key part for our teams was around the willingness to change and pivot in order to get the turbines up and running and an environment.
[00:30:31.220 - 00:30:38.220] Quite often due to the size of these particular turbines, sometimes too much wind is actually a bad thing.
[00:30:38.220 - 00:30:44.220] So sometimes we actually got to shut down some of these particular two ones. I know it sounds really crazy.
[00:30:44.220 - 00:30:51.220] Why would you want to do that? You know, that's just due to the corner. Safety part as well.
[00:30:51.220 - 00:31:02.220] We also, our assets are built on in near-significant cultural sites of significance to some of the EU that we work with.
[00:31:02.220 - 00:31:18.220] And even though that don't own the particular property, we still negotiate within our license to operate in terms of our permit to allow EUE to access those particular assets for certain events, a bit like Matadiki.
[00:31:18.220 - 00:31:40.020] So we've actually held a Matadiki ceremony up in Harapaki in the Hawkes Bay and needed to push back on some of those landowners, not all of the landowners are as...
[00:31:40.020 - 00:31:46.020] ...fotually cognizant of the changing world we find ourselves in today.
[00:31:46.020 - 00:31:52.020] And that's a challenge in itself, but that's... it is what it is.
[00:31:52.020 - 00:31:58.020] And it's the environment that we're working in. But I'm feeling hopeful for the future steering the...
[00:31:58.020 - 00:32:01.020] ...steering in the eyeballs at the moment, so I think it will be a good place.
[00:32:01.020 - 00:32:12.510] Two together. Super to grow, look who abbreviation on land, Papa Toula-Nooku, and super to grow.
[00:32:12.510 - 00:32:19.510] I don't even think you find in the year, birds, trees, fruit, everything is hanging up and up upon high.
[00:32:19.510 - 00:32:30.010] I brought those together just to sort of condense a wee bit, but also provide color to the wee bit more time to have a bit of a check.
[00:32:30.010 - 00:32:39.150] I think the key part here is that Toula-Nooku connects us to about shared aspirations.
[00:32:39.150 - 00:32:48.150] So as a company we were going through, we used to purchase a lot of the land that the assets we operate on.
[00:32:48.150 - 00:32:59.150] We don't now, we just lease it. It also allows opportunity if we do procure land for the use of developing an asset.
[00:32:59.150 - 00:33:08.150] We'll do that to ensure that it's not just a resource-consent consideration to work with historical owners.
[00:33:08.150 - 00:33:13.150] It's not just the landowners of the town. So it's not much aspiring a house.
[00:33:13.150 - 00:33:20.150] You sort of talk to the vendor and negotiate through your moors and make sure the bank can coffee up the money and away you go.
[00:33:20.150 - 00:33:28.150] So within our sort of resource-consent, the resource-consent will always tell us to work with the historical owners.
[00:33:28.150 - 00:33:34.150] And there might be civil groups of historical owners within their consent and most of the time of T-week.
[00:33:34.150 - 00:33:49.150] And for majority of the land we prospect and not saying that we're looking around for land every week, but quite often, most of the land owners of the land we're looking at for generating electricity,
[00:33:49.150 - 00:34:01.150] seem to be locked up in land trust, mighty land trust, or actually just owned by post-settlement governance entities, PSGs, like you have to do in a more nitro,
[00:34:01.150 - 00:34:05.150] who will do no more to-or-to-do, no more on the Apple.
[00:34:05.150 - 00:34:11.150] So our role in this particular aspect is to make sure that we've got a shared aspiration.
[00:34:11.150 - 00:34:17.150] And the only way we can get to that shared aspiration part is to make sure you're competent to be able to do that kind of stuff.
[00:34:17.150 - 00:34:31.150] So sometimes a bit like I'm not sure if you've seen a comedy called Key and Peel and Key and Peel used to have a, there was a skit about Barack Obama's anger translator.
[00:34:31.150 - 00:34:41.150] And then the anger translator hits something that plan and anguish and then has anger translator would speak in very ghetto foul-mouthed tombs.
[00:34:41.150 - 00:34:53.150] Well, quite often, we walk into negotiations, we actually need not just a sort of a translator if we go into a Marty medium environment, but we also just need to be a bit more culturally nuanced.
[00:34:53.150 - 00:35:04.150] You know, when we travel abroad, we need to be culturally nuanced to understand how we get to the table to actually be able to develop a partnership and an agreement.
[00:35:04.150 - 00:35:23.150] So some of that particular key and peel aspect is actually making sure that we're competent enough to read the social cues, to actually be confident and competent enough to be able to negotiate and push back when we think we're getting shafted, but also have really honest and honest conversations around what's been official for both parties.
[00:35:23.150 - 00:35:36.150] And so part of the capability up but left for Meridian, the Meridian the company is actually making sure that they are engaged in learning to real around going to a Marai.
[00:35:36.150 - 00:35:44.150] We have their exec, which is the senior leadership team, they go to a normal Marai that being said, our Pucki civil time is over.
[00:35:44.150 - 00:35:52.150] So the key part for us is to be able to build their competence so that they can have the critical conversations to develop these agreements.
[00:35:52.150 - 00:36:09.150] And a lot of those agreements is actually being out of sort of changed their perception around what partnership looks like because partnership, many of you that have worked in either the public service, they think partnership has been doing the dance card long enough to get the sign to consent and then they disappear like a thief in the night.
[00:36:09.150 - 00:36:21.150] And that's probably one of the biggest bug beers that E. We have. And even community as well as that you front-load your relationship about how good you are and what all the perceived benefits around it.
[00:36:21.150 - 00:36:28.150] And so all of a sudden you sign your life when you've agreed that you have this agreement and then they disappear.
[00:36:28.150 - 00:36:41.150] Or they've given you a payout and they're gone. I think the key part here is that she desperation means that she commitment that means actually developing a relationship that not just a one-way partnership.
[00:36:41.150 - 00:36:47.150] And one of those particular training sessions I run with some of our development managers.
[00:36:47.150 - 00:36:56.150] I say a partnership is like a like into a marriage. Now I'm not too sure how many people have married in this place in this particular room.
[00:36:56.150 - 00:37:02.150] But a marriage basically means that once they're ringers on their finger everything is negotiable.
[00:37:02.150 - 00:37:10.150] However, you know, I'm going to ensure that it's not about just consummating the relationship and the new bug roof for six months.
[00:37:10.150 - 00:37:16.150] And you come back and you ask them, how's the relationship? I bet you it's terrible. And it's the same rule applies.
[00:37:16.150 - 00:37:23.150] In this particular aspect here when we're going into agreements partnerships and relationships with communities and with Ewing.
[00:37:23.150 - 00:37:31.150] As we want to make sure that there are opportunities for us to communicate well regularly connecting and communicate.
[00:37:31.150 - 00:37:45.150] So one part here is being in communication. So two people are looking at super wide-wing is what I perceive benefits around aspirations to ensure that we get to a workable relationship that's not something that you do or snapchat or a bit of a teacher-specific kind of thing.
[00:37:45.150 - 00:37:59.420] But that's the litmus test of trust. The stress is brought over time. When you consider text messaging get a concrete decision from a relationship, the means of chronic work there.
[00:37:59.420 - 00:38:09.420] He was basically the bushing star. You see in Panocchio, he worked there. Tell us about what are those we're looking ahead.
[00:38:09.420 - 00:38:18.420] So we've looked back through Pahutukawa, Marta and he's bringing people together. Two people are not going to share their aspirations and collective consensus to move forward.
[00:38:18.420 - 00:38:27.420] And he was about putting that into practice around what are the opportunities and what is it that we want to leave for future generations.
[00:38:27.420 - 00:38:40.420] So he was at this stage is about managing the transition of not just going around fossil fuels to renewable energy, not just about monocultural capability to trigger honoring practice.
[00:38:40.420 - 00:38:54.420] It's also around the leaders that are ready and today and to the leaders of tomorrow, but also the engineers that are sitting in the room today are going to be here tomorrow or in the future.
[00:38:54.420 - 00:39:09.420] So it's about managing what that looks like. So our aspirations around looking at what does the future look like, what our hopes to ensure that we get to that particular future state that puts the next generation of leaders in a really strong place.
[00:39:09.420 - 00:39:14.420] On that note, I want to hand it over to our co, to have a wee bit of a quarter and then we'll close it up.
[00:39:14.420 - 00:39:58.180] You see me all good?
[00:39:58.180 - 00:40:27.180] Well, this is loading up. It's less good.
[00:40:27.180 - 00:40:32.180] It's not wanting to go back home.
[00:40:32.180 - 00:40:38.250] There we go. Technical difficulties.
[00:40:38.250 - 00:40:47.250] So, Q&A everybody, my name's Kaho. Some of you may admit me in some of our tutorials, so I'm over your E&E L3R-1 to choose.
[00:40:47.250 - 00:40:57.250] I'm also a fourth year computer engineer here at UC and as that lovely photo shows you, I was a head of the privilege of being one of the interns at Meridian E&G.
[00:40:57.250 - 00:41:11.250] So I'm going to sort of do a little bit of a, I'll make it quick today. Sort of a presentation around my internship and sort of how I took some of these ideas around Medicaid Māori and sort of interweave them into the engineering process and practices, sort of, sort of, sort of, sort of.
[00:41:11.250 - 00:41:17.250] So why this matters for engineering yourself? So you all guys will start learning about the digital E&E or YTANGU.
[00:41:17.250 - 00:41:21.250] And it's not just a sort of partnership framework, it's not a historical document.
[00:41:21.250 - 00:41:28.250] It shapes how we work as engineers today. It is something that we need to incorporate into all our thinking and our ideas.
[00:41:28.250 - 00:41:37.250] And it's key. Engineering is in Washington Court, now sort of expects cultural competency, not just technical competency.
[00:41:37.250 - 00:41:44.250] And it shows up as you consult and talk to people and communicate. It's part of the success criteria and design.
[00:41:44.250 - 00:41:50.250] So engineers with your land, water, infrastructure and museum will meet the main of the web.
[00:41:50.250 - 00:41:56.250] And relationships at some point. So a bit of a background for you guys, some of you may know.
[00:41:56.250 - 00:42:06.250] Some radians, white-team catchment flows from Lake Bukaki, Lake Ojo, all the way down through Lake Bemmoa, Lake Avinmoa, and then to the white-time year of it.
[00:42:06.250 - 00:42:14.250] Now, this is the white-team catchment. And all of these hydro schemes are part of the river.
[00:42:14.250 - 00:42:17.250] So, radians, they don't just sit near the rivers, they are part of it.
[00:42:17.250 - 00:42:25.250] And therefore, the E.E. we hold quite enduring relationships with these waterways through ancestral links.
[00:42:25.250 - 00:42:35.250] And it sort of predates the power station. So they are a critical and sort of key thing that you need to be thinking about when you're dealing with infrastructure like this.
[00:42:35.250 - 00:42:47.250] So cultural engagement, it's not just a side initiative. It's something that should be underlying and, I don't know if you'll see.
[00:42:47.250 - 00:43:00.250] E.E. we are going to see these waterways have relationships that go back to interest. Long before any of these dams existed, those relationships don't stop existing as we move forward, like Andre said, looking at the past as you're moving forward.
[00:43:00.250 - 00:43:08.250] So, cultural engagement actually sits inside engineering planning, inside environmental management, and now inside digital innovation projects.
[00:43:08.250 - 00:43:18.250] Like the one I'm going to present to you guys now. So, hydro sites are dangerous, large amounts of power is produced here, huge amounts of order.
[00:43:18.250 - 00:43:34.250] And this, come as we're in Fano who connects to the hour can't really access these sites. So, how can an engineer who only sees hazardous restricted item solve this problem?
[00:43:34.250 - 00:43:43.250] So, I came in with the idea of, well, I don't think it makes something cool. So I came up with the idea of the Meridian hydro vision.
[00:43:43.250 - 00:43:53.250] There's a virtual reality platform. So, this builds on some of the infrastructure we already have. So, our engineers at Meridian have 3D scans of all our hydro dams.
[00:43:53.250 - 00:44:05.250] So, we're going to take some of that ideas and go, can we use it for a wider purpose? So, I started to go through a pivot on the idea and completely change it for a purpose.
[00:44:05.250 - 00:44:14.250] So, targeting it towards people like you, students, people who could never actually sit foot on the dams now in a safe and secure environment.
[00:44:14.250 - 00:44:27.250] So, guiding it by health and safety and communications and cultural engagement. So, goal was transform existing site data into a user friendly VR platform, accessible and immersive experience operation.
[00:44:27.250 - 00:44:38.250] So, Fano and Kommato became the design target. I started to look beyond just your typical engineer and looking at who this was designed for.
[00:44:38.250 - 00:44:52.250] So, interaction mechanisms, how they would interface with something like VR, not just power users. So, going over visual clarity over pro realism, comfort and ease of feel more than technical showmanship.
[00:44:52.250 - 00:44:59.250] And as we can see here, we've got to have our lovely dam technicians having a goal, but right now anybody can get on it.
[00:44:59.250 - 00:45:06.250] And so, this was really starting to focus the idea of Fano and Kommato, who would never get to see the hydro dam and focusing on that.
[00:45:06.250 - 00:45:15.250] So, this is the outcome. These are 3D rendered designs and in the virtual space run and Unreal Engine.
[00:45:15.250 - 00:45:23.250] This is the white-key hydro dam in Lifestyle Scout. From here we were able to develop some interactive objects.
[00:45:23.250 - 00:45:34.250] So, as we can see the video playing, here is myself interacting within the environment. I'm going to put on my PPE because you know how it has our important.
[00:45:34.250 - 00:45:43.250] And yes, so this was able to start to get the interaction and start to be able to communicate some of the ideas and communication within the site.
[00:45:43.250 - 00:45:51.250] I love my fire extinguisher. So, this is the prototype. So, this is an application that runs primarily on the headset.
[00:45:51.250 - 00:45:59.250] Here we were that this was filmed by myself while trying to actually walk around inside the virtual and varying environments. So, my head is extremely shaky.
[00:45:59.250 - 00:46:07.250] But yeah, I'm still demonstrated off. I don't have hand-eye coordination at all.
[00:46:07.250 - 00:46:22.760] So, this is scaled to life size. So, this is one side of the white-key hydrohole.
[00:46:22.760 - 00:46:26.760] So, these scans through Lidar cameras that have been done.
[00:46:26.760 - 00:46:36.760] So, previously this was used for our engineers to be able to go through a measure-up parts of the site to be able to plan future installations and projects.
[00:46:36.760 - 00:46:42.190] Got a lot of the heart-hat.
[00:46:42.190 - 00:46:46.190] And so, part of the virtual reality scheme is we've got these informational panels.
[00:46:46.190 - 00:46:52.190] So, this gives a bit of the history and scope around what is around the hydro dam. So, why taking particular its history?
[00:46:52.190 - 00:46:57.190] Given it's one of the older of the white-key scheme.
[00:46:57.190 - 00:47:13.460] So, and this is one of the sort of more important that's here was, well, can we get inside the actual turbine itself?
[00:47:13.460 - 00:47:18.920] And here we go. So, this is the lower level.
[00:47:18.920 - 00:47:20.920] So, this is where the actual turbine is spinning.
[00:47:20.920 - 00:47:25.920] Those who have done power engineering, unlike myself, would probably know this a little bit better than I do.
[00:47:25.920 - 00:47:28.920] But this is inside the actual main turbine where the...
[00:47:28.920 - 00:47:31.920] It's spinning and the water...
[00:47:31.920 - 00:47:38.920] There is sound usually with this, but when you're standing inside there, it is a mountainous roar going through there with the amount of water.
[00:47:38.920 - 00:47:42.100] Yeah.
[00:47:42.100 - 00:47:47.100] I'm just going to sort of quickly go over the ton of trip and train, so the project has one.
[00:47:47.100 - 00:47:52.100] As Andre said, having eels goes through the turbines, not great.
[00:47:52.100 - 00:47:57.100] They are delicious and they are kim-winer that are sacred and very important.
[00:47:57.100 - 00:48:02.100] And what some e-mail relations have done is we've got the trip and transfer programs.
[00:48:02.100 - 00:48:07.100] So, that's working with local e-wees and so local knowledge who have them being able to go out.
[00:48:07.100 - 00:48:16.100] And so, they go around and like Andre says, go and track and weigh and measure all the toner in and around the hydro screens.
[00:48:16.100 - 00:48:19.100] So, on the top photo there, we can see one of our over-ledgers there.
[00:48:19.100 - 00:48:23.100] So, that's underneath the white-hacking dam itself.
[00:48:23.100 - 00:48:32.100] So, the juvenile elders in the bucket here swim up the ramp and into the little green trough.
[00:48:32.100 - 00:48:40.100] And so, that is where we are able to trap, weigh and move them to places where that they will be able to migrate and grow.
[00:48:40.100 - 00:48:50.100] And so, we're doing this in partnership with the e-wee and we're being able to do measurements on the GPS thing on location and migration of the e-mails and the helper.
[00:48:50.100 - 00:48:55.100] So, that's sort of building those relationships with e-wees and they're doing none as well.
[00:48:55.100 - 00:48:58.100] Big thing to sort of finish up on as we're coming to the idea.
[00:48:58.100 - 00:49:02.100] By culturalism isn't just a section of your report, it's a design input.
[00:49:02.100 - 00:49:09.100] It's something that can help shape the scope of your projects and can help change the target audience.
[00:49:09.100 - 00:49:14.100] So, I can see with my project it changed the audience, the interaction is not near anything.
[00:49:14.100 - 00:49:19.760] So, taking it in the beginning helps start the solution in the end.
[00:49:19.760 - 00:49:22.760] I thought I would finish with a proverb.
[00:49:22.760 - 00:49:25.760] So, I have to say, there will no idea what you are to do.
[00:49:25.760 - 00:49:27.760] So, what is the most important thing in the world?
[00:49:27.760 - 00:49:30.760] It is a tank of the tank of the tank of the tank of the tank of the tank of the tank.
[00:49:30.760 - 00:49:32.760] The people, the people.
[00:49:32.760 - 00:49:35.760] So, there we go guys.
[00:49:35.760 - 00:49:46.820] There's a couple more slides to leave with and then we are done.
[00:49:46.820 - 00:49:50.820] I think just to talk about that, the particular images,
[00:49:50.820 - 00:49:53.820] due to the timeframe of the Matorkei internship.
[00:49:53.820 - 00:50:00.820] So, for those that are unaware, we run an internship program every summer.
[00:50:00.820 - 00:50:03.820] We have run a truly synopt just for the engineers.
[00:50:03.820 - 00:50:07.820] We have usually run around at 12, you have about a thousand engineers every summer.
[00:50:07.820 - 00:50:11.820] And we have a Matorkei internship, which is a relationship we have with Naito.
[00:50:11.820 - 00:50:14.820] We also have as part of those relationships with the asset owner,
[00:50:14.820 - 00:50:17.820] while the local area of where our assets are positioned.
[00:50:17.820 - 00:50:22.820] We also have educational pathways, which is all connected to that keyword
[00:50:22.820 - 00:50:26.820] to run a kind of start constellation, bringing things together.
[00:50:26.820 - 00:50:36.820] That part of what we're wanting to do in terms of what Co-Hooded for Meridian was those images
[00:50:36.820 - 00:50:39.820] that were basically all available at the time.
[00:50:39.820 - 00:50:44.820] It's time to be able to take some really good images, but what he created.
[00:50:44.820 - 00:50:49.820] And this is kind of the measure across the post being able to have enough head space to say,
[00:50:49.820 - 00:50:52.820] okay, how can I bring value to Meridian?
[00:50:52.820 - 00:50:55.820] And that's the premise for our internship program.
[00:50:55.820 - 00:51:01.820] The value is Ed, and then we'll just throw whatever we can at that particular project.
[00:51:01.820 - 00:51:07.820] So I just wanted to sort of finish up with acknowledging that Co-Hood's contribution to Meridian,
[00:51:07.820 - 00:51:11.820] and all of the other engineers and majority of them have come from UC,
[00:51:11.820 - 00:51:15.820] and their contribution to the value that they brought to Meridian and the company,
[00:51:15.820 - 00:51:17.820] as it actually put us in really good stead.
[00:51:17.820 - 00:51:20.820] So on that particular note, Naito, he knew Calcoto.
[00:51:20.820 - 00:51:22.820] Yeah, we'll leave it at that.
[00:51:22.820 - 00:51:30.580] Thank you.
[00:51:30.580 - 00:51:34.590] That's all, folks.
[00:52:10.420 - 00:52:12.420] Thank you.
[00:52:40.420 - 00:52:42.420] Thank you.
[00:53:10.420 - 00:53:12.420] Thank you.
[00:53:40.420 - 00:53:42.420] Thank you.
[00:54:10.420 - 00:54:12.420] Thank you.
[00:54:12.420 - 00:54:14.420] Thank you.
[00:54:40.420 - 00:54:42.420] Thank you.

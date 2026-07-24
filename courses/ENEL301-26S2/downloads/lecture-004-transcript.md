# ENEL301-26S2 Lecture 4 fast-pass local ASR transcript

Date: July 24, 2026 10:00am-10:55am
Transcript type: Hermes fast-pass local ASR from validated Echo audio, not a native Echo transcript.
Backend/model: faster-whisper tiny.en, CPU int8, beam_size=1, vad_filter=True.
Quality note: fast catch-up transcript. Technical terms, equations, names and Māori words need checking against slides/audio before assessment use.
Source audio SHA-256: `ddfcc99420660f52d92ebe2a8c63f83185f40929d90c6215718d47b2caa16c26`
Generated: 2026-07-24T23:35:17.928787+12:00

[00:00:00.000 - 00:00:06.240] I'm going to go to Hope you're all doing well. Happy Friday. Got some folk from
[00:00:06.240 - 00:00:11.120] from Inchstock to talk to you about little vendors coming up. How are you?
[00:00:11.120 - 00:00:17.080] Hi everyone. We're here to talk about the UC interviews. So it's the first year we're
[00:00:17.080 - 00:00:21.920] running as a club and we're kind of putting on like a variety show with as soon as it
[00:00:21.920 - 00:00:26.240] skits and multiple sort of storylines. I'm the assistant stage manager so if you see
[00:00:26.240 - 00:00:30.960] in the on stage is something going wrong but I had a bit of a sneak peek of the show over
[00:00:30.960 - 00:00:35.200] the last week in Annathio was really cool and I think it's something that you know it's
[00:00:35.200 - 00:00:40.720] really cool to show so I thought you know might as well tell you guys about it. Hi I'm Alex and
[00:00:40.720 - 00:00:44.080] you should see me on the stage because I'm in the cast. If you don't see me, something has
[00:00:44.080 - 00:00:51.040] gone wrong. Creative wise the show was based around a main plot of a parody of Alice in Wonderland.
[00:00:51.040 - 00:00:55.360] Of course we call it Alice in Wonderland through the safety glass. Really on the nose. There's
[00:00:55.360 - 00:01:01.920] also a subplot murder mystery which features by name two of your favorite lecturers. I won't spoil
[00:01:01.920 - 00:01:06.960] it any further though and a whole bunch of comedy skits which I'm in and they're really unhinged
[00:01:06.960 - 00:01:11.200] and funny and basically the whole point is we make fun of engineering and all different disciplines
[00:01:11.200 - 00:01:16.080] and the worst types of engineers around. I play some really terrible engineers. It's really fun.
[00:01:16.640 - 00:01:25.040] There's also a jazz band which is cool. I'll and taskmaster featuring actual lecturers doing tasks
[00:01:25.120 - 00:01:33.280] on stage and I'm interested. Yeah. To get to selling fast. It's only $10 for students.
[00:01:34.000 - 00:01:39.680] It's about two hours long. You can come with a group of friends. It's really enjoyable and you can
[00:01:39.680 - 00:01:46.880] bring a drink in some snacks in so please get in fast these tickets are selling. So yeah thank you
[00:01:46.880 - 00:01:52.720] and follow the Instagram for any details and you see dot end dot review. Thank you guys.
[00:01:53.200 - 00:02:11.740] Yeah cool. Okay let's get going. So today's probably one of my favorite lectures to deliver
[00:02:12.700 - 00:02:18.620] on bias diversity. I think it's a pretty chunky one. We're going to move into a little bit of human
[00:02:18.620 - 00:02:26.060] psychology as well. It's just something different for a Friday and yeah then I'll talk about
[00:02:26.620 - 00:02:31.580] some fasts I'm going to give you at the end. Yeah I might be on taskmaster apparently as of a few
[00:02:31.580 - 00:02:38.860] minutes ago. Cool. So this is where you're at at the moment. So yeah we're up to a biased diversity
[00:02:38.860 - 00:02:45.660] in ethics. Just a couple of the last million items too. This lecture is not live strained. So there's
[00:02:45.660 - 00:02:51.100] some people that thought it was but it's not. We do record and that recording is shared immediately
[00:02:51.100 - 00:02:59.420] afterwards. The other one too is that someone suggested you know could I put the week numbers in
[00:02:59.420 - 00:03:05.500] the section on learn and I kind of can't really do that because as you'll see here sometimes
[00:03:05.500 - 00:03:09.580] we've got lectures in one week but then the follow-up workshop is actually in the following. So
[00:03:09.580 - 00:03:14.220] kind of confuses things. But look if you do have any other suggestions on how it can improve the
[00:03:14.220 - 00:03:21.740] structure of learn. Let you know well we are kind of constrained by the Moodle All Learn environment.
[00:03:21.740 - 00:03:27.580] So we're kind of love to be able to put in a hyperlink that jumps straight down into the sub sections.
[00:03:28.140 - 00:03:35.660] But it doesn't have that functionality. Cool. All right. So little bit of background for today.
[00:03:35.660 - 00:03:40.460] So just reinforcing some things that I'll be talked about in our last week. Engineering has
[00:03:40.460 - 00:03:48.700] hard achieved much without the help of other people and we need to do the right thing. And this
[00:03:48.700 - 00:03:55.420] social culture shaped us and therefore our ethics. I mean need to recognize that everyone's
[00:03:55.420 - 00:04:02.940] ethical compass if you like or their direction is different. And this is the little case study
[00:04:02.940 - 00:04:12.940] that I mentioned last week about a recent graduate who basically was invoicing himself.
[00:04:14.140 - 00:04:21.980] So he set himself up a little business on the side and was an engineer within water care
[00:04:22.700 - 00:04:29.900] and was contracting himself to do work that never actually existed. It's one of the oldest
[00:04:29.900 - 00:04:39.420] fraud tricks in the book and he got found out. So charged $1 million and was sentenced to two
[00:04:40.140 - 00:04:48.780] just over two years in prison. But yeah interestingly that graduate did a course with this learning
[00:04:51.630 - 00:04:57.950] looks like this one right. That's the learning outcome that we have. So as I said last week
[00:04:58.830 - 00:05:09.230] I might not be able to change your moral compass but hopefully I can. So there is a debate
[00:05:09.950 - 00:05:16.270] in the engineering education and ethics literature about whether or not you can actually teach someone
[00:05:17.230 - 00:05:25.070] how to be a good person. And some say no you can't teach that. While others say that actually
[00:05:25.070 - 00:05:32.110] ethical reasoning develops over time and it can be taught. So yeah the nevertheless
[00:05:33.710 - 00:05:41.790] it still needs to do our best. So today is more about how developing your own awareness
[00:05:42.350 - 00:05:50.750] about how decisions including ethical decisions can be affected by your bias. And we're also going to
[00:05:51.550 - 00:06:02.910] talk about how group decisions happen and some of the very strange things happen when we get people
[00:06:02.910 - 00:06:09.550] involved. So we're going to cover cognitive biases by C's diversity of perspectives in group
[00:06:09.550 - 00:06:15.310] dynamics. And then at the end we're going to have touch back on some of the codes of
[00:06:16.190 - 00:06:27.150] conduct that you looked at in the week one workshop. Okay so just some basics to start with. So
[00:06:27.630 - 00:06:36.350] cognitive biases relate to heuristics. Okay so heuristics are rules of thumb in your brain.
[00:06:36.430 - 00:06:45.390] Okay so it's wiring of how you process information. Okay and that develops over time.
[00:06:46.670 - 00:06:54.350] And the idea is with heuristics is that actually makes it easier for you to make decisions.
[00:06:54.910 - 00:07:00.910] Okay so and yeah and we develop these over time. So I like to sometimes bring in sporting
[00:07:00.910 - 00:07:09.630] analogies. Okay so if you're on a sporting field over the years you start to learn how to make
[00:07:09.630 - 00:07:14.430] quick decisions about what to do next and react to what's in front of you. Okay and that's a heuristic.
[00:07:15.230 - 00:07:25.070] So it simplifies decision making and speeds it up. Okay but a cognitive bias is when your heuristics
[00:07:25.710 - 00:07:33.710] are driving you to make a decision that might not necessarily be the right one. Okay so it's distorting
[00:07:35.070 - 00:07:46.750] your view of reality. Okay so and that can include stereotypes and implicit or unconscious bias
[00:07:47.710 - 00:07:55.070] and talk about those on the next slide. And the big thing to be aware of is that your cognitive
[00:07:55.070 - 00:08:02.190] biases, everyone has them but they affect how you operate and how you make decisions and how you
[00:08:02.190 - 00:08:11.630] interact with others. So on learn I've uploaded a little quiz if you want you can take later wrong.
[00:08:11.710 - 00:08:19.550] It's called project implicit run by Harvard University and you can actually start to see what
[00:08:19.550 - 00:08:26.830] cognitive biases you might have. Yeah so I've done a couple of those tests and yeah there was some
[00:08:26.830 - 00:08:35.150] things that I learned about myself. It can be helpful for you to be aware of. Just be wary though
[00:08:36.110 - 00:08:44.110] that you might get a bit of a surprise result that you weren't expecting and within the quiz as well
[00:08:44.110 - 00:08:50.750] you get to see how you compare with everyone else who's taken the test. Also really quite
[00:08:50.750 - 00:08:59.070] interesting task to do. Okay so stereotypes is a generalized belief about a particular group of people.
[00:08:59.950 - 00:09:03.870] Yeah so tell me about engineers what are some of our stereotypes?
[00:09:06.750 - 00:09:18.830] It's silly yet unhodenic. What else? Quiet so introverted perhaps? Yep anything else?
[00:09:20.270 - 00:09:30.770] Part to get along with it's not very personable. Yeah anything else. So devastatingly what?
[00:09:31.730 - 00:09:41.010] Oh how long? Yeah yeah. Mine's not doing myself any favors. Right yes so but yeah it's a generalized
[00:09:41.010 - 00:09:47.650] belief in what people are and how they act and so on. Yeah so the classic one is that engineers
[00:09:47.650 - 00:09:58.530] are introverted. Okay the truth is we're not okay on average the average engineer is no more introverted
[00:09:58.530 - 00:10:06.130] than anyone else. Okay so that's a bit of work that came out of my own research. So they you know 800
[00:10:06.130 - 00:10:15.810] engineers we used a validated test to ask them to report and I'll answer some questions. Yeah it came back
[00:10:15.810 - 00:10:22.290] actually on average they were about the same to everyone else. So that being said that's only an
[00:10:22.290 - 00:10:30.050] average and there's going to be people are on a bell curve if you like as you're going to have
[00:10:30.050 - 00:10:40.610] some people are really introverted and some who are very extroverted. Yeah so you'd just be wary
[00:10:40.610 - 00:10:47.970] again that when we're talking about these things is that it might not apply to individuals. Cool
[00:10:48.770 - 00:10:55.730] Yeah so what's interesting though is that sometimes stereotypes can actually be true.
[00:10:56.530 - 00:11:01.730] Yeah so I can't think of anyone in particular but yeah just be aware of that.
[00:11:03.730 - 00:11:10.930] Always challenge stereotypes. The introversion and extroversion thing is one of the ones that really annoys me.
[00:11:11.890 - 00:11:19.250] Another one that really annoys me is generational differences okay that millennials are somehow
[00:11:19.250 - 00:11:28.610] different to generation X's. It's like actually if you wind back my clock so I'm a gen at gen X if
[00:11:28.610 - 00:11:35.010] you wind back the clock I was probably behaving in a similar way to all of you. Okay and we've
[00:11:35.010 - 00:11:46.210] actually got more in common than we do have in differences. Okay right so yeah reinforcing cognitive
[00:11:46.210 - 00:11:57.490] biases are breakdown in heuristics. Systematic systematic error in reasoning. We've got explicit biases
[00:11:57.490 - 00:12:08.050] so that's where we openly express attitudes or beliefs that are biased. All we've got implicit bias
[00:12:08.050 - 00:12:15.330] okay so these are built in us that you can't actually observe them. Okay so they're hidden. Okay and
[00:12:15.330 - 00:12:23.890] these exist okay so this is a big the paper that I'm quoting here is a big systematic review or
[00:12:23.890 - 00:12:33.810] meta analysis of hundreds of bits of research on cognitive biases and yeah so what they found was
[00:12:33.810 - 00:12:40.210] that across different countries is that there are both implicit and explicit biases that do still
[00:12:40.210 - 00:12:49.490] exist including relation to the skin color how you look, the sexual orientation and so on.
[00:12:50.210 - 00:13:01.330] Okay so so bias these exist. There's all sorts of interesting biases yeah I think that I was just
[00:13:01.330 - 00:13:10.050] thinking about a so one of them is a sunk cost bias or sunk cost fallacy. We'll talk a little bit
[00:13:10.050 - 00:13:18.370] about this one later in finance but it's really interesting is that so in finance you might invest
[00:13:18.370 - 00:13:26.290] a couple of million dollars into a project midway through you realize this isn't going very well
[00:13:27.250 - 00:13:32.370] we need to invest more and more money into this to actually make it work in order to recoup that
[00:13:32.370 - 00:13:39.490] money. Now that money's already gone okay so it's an absolute sunk cost bias that you're going to get
[00:13:39.490 - 00:13:46.370] that money back okay it's it's disappeared it's not there anymore. Another one's sporting analogy
[00:13:46.370 - 00:13:54.210] is when you see a team on the sporting field committing to the same strategy even if they're
[00:13:54.210 - 00:14:01.570] getting absolutely wiped by the opposition okay so they believe in themselves that we've invested
[00:14:01.570 - 00:14:07.090] time and money in our strategy we're going to keep doing it because it's the right thing to do okay
[00:14:08.050 - 00:14:17.330] no it's not okay another interesting one is I'm thinking it's on here so look I mean look
[00:14:19.730 - 00:14:26.450] yeah confirmation bias okay so you might be thinking oh when I graduate I'm going to have you know
[00:14:26.450 - 00:14:33.490] heaps of money and I'm going to go out and buy a GTI golf and all of a sudden when you're walking
[00:14:34.210 - 00:14:41.570] you see all these really cool people driving GTI golfs you know so it's confirming what you already
[00:14:41.570 - 00:14:51.090] want that's confirmation bias. Another interesting one not on here is guru bias okay so that's
[00:14:51.090 - 00:15:00.450] where in a group situation people believe the person who is most experienced or perhaps is getting
[00:15:00.450 - 00:15:08.290] paid the most is the holder of the truth okay and we must listen to them because they know
[00:15:08.290 - 00:15:19.650] everything they must be right okay when in reality they might not be right okay and yeah sometimes
[00:15:19.650 - 00:15:26.370] it's right sometimes it's not so it comes back to you're thinking about again this this morning is
[00:15:26.370 - 00:15:32.450] that there's a company in Australia run it's one of the biggest companies called VisiGroups so they
[00:15:32.450 - 00:15:40.610] run all the big recycling systems but they're owned by the Pratt family and Richard Pratt's the
[00:15:41.490 - 00:15:47.730] CEO one of the wealthiest people in Australia and remember a few years ago someone asked him
[00:15:48.450 - 00:15:57.330] why are you so successful and his answer was I'm not very smart myself but I surround myself with
[00:15:57.330 - 00:16:03.730] very very smart people who know more than me okay so he was actually so challenging the guru
[00:16:03.730 - 00:16:09.170] bias is that he wasn't the holder of truth that is the people that work with him who do
[00:16:10.130 - 00:16:17.170] in their probably pay less than him okay generative AI has bias
[00:16:18.930 - 00:16:23.250] I was playing around with it this morning and it was coming up with absolute nonsense
[00:16:24.290 - 00:16:32.370] so I think I asked it was testing it out to see if it knew stuff around my department around the
[00:16:32.370 - 00:16:38.770] department of electrical engineering I said who in my department teaches electronics and I said
[00:16:38.770 - 00:16:45.970] Richard Green does I went well first of all he's not in my department and secondly he doesn't teach
[00:16:45.970 - 00:16:52.770] electronics where are you getting this from so I tested I started asking chat JPT where are you
[00:16:52.770 - 00:16:59.490] getting this information from and it was you know doubling down saying no Richard Green's
[00:16:59.490 - 00:17:04.130] definitely in department of electrical engineering so until I corrected it and went that was not
[00:17:05.010 - 00:17:10.370] he's in the other one and by the way he doesn't teach this and it is all you're you're very very
[00:17:10.370 - 00:17:18.770] right and then that came all the information okay so yeah so it does exhibit racial and gender biases
[00:17:20.370 - 00:17:30.290] and yeah so Zach and Lehman they looked at it from a medical diagnostic perspective
[00:17:30.290 - 00:17:38.930] and it started to for cough up in create all sorts of weird biases in medical diagnosis
[00:17:39.810 - 00:17:49.730] and so yeah it exists and open AI actually recognize this in their terms of reference you know
[00:17:49.730 - 00:17:56.930] so I did check that terms of reference earlier a couple of weeks ago it hasn't re-changed
[00:17:57.890 - 00:18:05.570] but yeah if you have a look down in those bottom last few terms of references basically it's saying
[00:18:06.290 - 00:18:14.450] yet I'm going to give you false information and I'm going to be offensive okay so yeah I think they
[00:18:14.450 - 00:18:22.770] are acknowledging that there are biases within the data set okay so be aware of that okay so
[00:18:23.410 - 00:18:32.050] yeah I've got a paper coming out later in the year about how engineers use generated AI in practice
[00:18:32.050 - 00:18:39.010] amazingly there's a whole lot of people who are using it for human resource stuff okay so they're
[00:18:39.010 - 00:18:43.730] managing people and they're actually using chat GPT to get advice on how to manage people
[00:18:44.370 - 00:18:52.690] including writing performance reviews it's like whoa and so you for people's performance reviews
[00:18:52.770 - 00:18:58.290] that are being written by chat GPT might have actually built in bias yeah pretty crazy
[00:19:00.530 - 00:19:06.930] cool and yeah so our characteristics so this is what you said last week except for some of the
[00:19:06.930 - 00:19:15.010] the big ones in the middle that I've taken out okay and yeah teams will be made up of people who
[00:19:15.010 - 00:19:22.610] are all different and be careful that sometimes when we choose teams or put into teams who
[00:19:22.610 - 00:19:30.130] are more like us we're more homogenous okay but even within that diversity will always exist
[00:19:31.330 - 00:19:37.330] in group decision-making coming back to what Chancellor Bellian was saying about what collaboration
[00:19:37.330 - 00:19:45.010] is about it's purposely exploiting our differences okay some of our different characteristics
[00:19:45.010 - 00:19:51.570] even more of them okay so we've got biological and physical similarities and differences
[00:19:52.210 - 00:19:59.970] cognitive and emotional personality identity okay so like personality traits like
[00:19:59.970 - 00:20:05.730] extra version and introversion okay they're largely some of these are actually locked in you know so
[00:20:07.650 - 00:20:13.810] yeah particularly a personality traits once you've you know matured yeah those things are pretty
[00:20:13.810 - 00:20:21.010] much locked in for life but then we've got our own values and beliefs our language and
[00:20:21.010 - 00:20:28.450] communication social cultural groups and ethical and moral perspectives okay so some of you
[00:20:28.450 - 00:20:35.650] tell them the workshop this week talked a little bit about that are these differences as it relates
[00:20:35.650 - 00:20:46.610] to culture so keep an eye off that if you're in b8 to b14 next week okay so to give you some
[00:20:46.610 - 00:20:56.850] examples it's often said that say for risk-taking that men are generally more likely to take risks than
[00:20:56.850 - 00:21:08.530] women okay and that's pretty true okay so that's why men have to pay higher current insurance premiums
[00:21:09.090 - 00:21:21.170] okay so it on average again it is a thing but there's other types of factors which affect
[00:21:22.450 - 00:21:32.450] your risk-taking approach okay your age the types of risk and so on so occasionally this
[00:21:33.410 - 00:21:40.690] stereotype is actually not true okay there are some instances where women will actually take more
[00:21:40.690 - 00:21:49.330] risk than men you know so be wary of that the other one too is that are be careful of
[00:21:49.330 - 00:21:59.570] no results so you might think that's not putting an judgment on you but you might think that
[00:21:59.570 - 00:22:05.730] perhaps older people are less created than younger people okay but that is not true okay so there's
[00:22:05.730 - 00:22:14.130] been work shown that age is not significantly significantly related to creativity okay so this is again a
[00:22:14.130 - 00:22:25.410] big study of studies and so it was not observed it was any correlation you know that paper if you
[00:22:25.410 - 00:22:34.610] understood actually found some other interesting things that were true things like ability to train
[00:22:34.610 - 00:22:43.090] someone actually declines as they get older yeah which is pretty interesting so from a say health and
[00:22:43.090 - 00:22:51.490] safety perspective yeah trying to teach someone older and how to safely say operate a machine
[00:22:51.490 - 00:23:02.180] a bit of equipment it'll take longer okay yes so yeah other factors and contexts can matter
[00:23:02.180 - 00:23:11.460] when we're thinking about characteristics that might affect our decisions okay so culture so we
[00:23:11.460 - 00:23:16.660] talked a little bit about that last week but it's a system of shared beliefs of behaviors
[00:23:17.300 - 00:23:24.260] that are common to a particular group of people there's a really interesting model of culture
[00:23:25.300 - 00:23:39.140] by a think of as a Belgian or a Dutchman called Hofstede so Hofstede worked for IBM and in the
[00:23:40.580 - 00:23:51.380] 80s surveyed 60,000 people who worked at IBM across 50 different countries so massive study
[00:23:52.020 - 00:24:01.300] and to this day yeah people are using Hofstede work as a way of describing different cultures
[00:24:02.980 - 00:24:15.700] okay so the models of culture include five or sorry six facets so the first one was power distance
[00:24:15.700 - 00:24:26.260] relationship and so deals with fact that individuals in society are not equal and it's the
[00:24:26.260 - 00:24:35.860] extent of which less powerful members of an organization within a country connects related to the
[00:24:35.860 - 00:24:43.060] people who are in power okay so in New Zealand our power distance relationship is enormously small
[00:24:44.020 - 00:24:53.620] okay so I have got two distances of freedom to the prime minister okay so my executive Dean is
[00:24:53.620 - 00:25:03.540] my boss knows the prime minister okay so now if you're in a much bigger country say the United States
[00:25:03.540 - 00:25:10.180] the number of degrees of separation between you and say Trump so we're going to be much more
[00:25:10.980 - 00:25:17.700] okay so that's actually can be a really important thing for things like entrepreneurship and developing
[00:25:17.700 - 00:25:27.140] businesses is that a short power distance relationship can help okay individualism is about how
[00:25:27.140 - 00:25:33.300] much you're looking out for yourself versus how much you're looking out for other people or
[00:25:33.620 - 00:25:42.820] collectivism okay uncertainty avoidance is to do with with risk and how you approach or our culture
[00:25:42.820 - 00:25:50.420] approaches risk and master willing and feminine femininity this one's a bit weird it's got nothing
[00:25:50.420 - 00:25:56.660] actually got nothing to do with gender but it depicts the degree to which traits like authority
[00:25:57.140 - 00:26:03.300] as performance and success are preferred to things like personal relationships quality of life
[00:26:03.300 - 00:26:12.260] service and welfare okay so it's not what it looks like on the in the words later on
[00:26:12.260 - 00:26:20.580] hostee to added long term orientation so how much do you think about the future in your decision
[00:26:21.460 - 00:26:26.980] and in indulgence okay so how much you on the flip side the opposite to an
[00:26:30.980 - 00:26:42.420] indulgence is restrained okay so hostee's model is disputed okay so some people think it's
[00:26:42.420 - 00:26:49.460] actually pretty good but there are some who dispute the model so I've got some homework for you
[00:26:50.100 - 00:26:57.220] later on which I'll show you about hostee's model off the top of your head though what do you
[00:26:57.220 - 00:27:07.090] think the problem might be okay so so they'd 60,000 people in IBM across 50 countries
[00:27:08.290 - 00:27:16.580] if you reckon that's a good sample of society pretty small they're pretty small for 60,000
[00:27:16.820 - 00:27:31.630] relative to probably billions of people yeah yeah so it's going to be very tech heavy
[00:27:32.430 - 00:27:40.080] engineering computing focused yeah mostly developed countries yeah yeah for sure yeah so
[00:27:41.040 - 00:27:45.440] yeah once you get into your homework you can actually start to have a look at some of the other
[00:27:46.320 - 00:27:56.000] challenges with applying hostee's model okay so if you want as well you can have a look
[00:27:56.000 - 00:28:03.920] at put a link up on learn as well you can check out how New Zealand compares to other different
[00:28:03.920 - 00:28:13.520] countries okay so how might low power distance relationships and high individualism affect ethical
[00:28:13.520 - 00:28:33.010] decision making yeah yep yep perfect yes so if you're in a low power distance culture yeah yeah there's
[00:28:33.010 - 00:28:44.860] probably more promotion for you to speak up yeah for sure yeah perfect yeah so yeah you can make
[00:28:46.060 - 00:28:51.740] yeah decisions that benefit you rather than for the greater good yeah interesting
[00:28:52.460 - 00:29:00.060] cool so yeah so yeah New Zealand is really quite high on the the individualistic measure
[00:29:01.020 - 00:29:07.420] and low on the power distance so you can check out some other very different countries so don't
[00:29:07.420 - 00:29:14.220] look at people who or cultures that might be like New Zealand so don't look at Australia look for
[00:29:14.220 - 00:29:20.940] all that very different countries okay what do you think some of the other problems with hostee's
[00:29:20.940 - 00:29:31.840] model is New Zealand one culture no way yeah so it's it's pretty rare that you have one culture
[00:29:31.840 - 00:29:38.400] in one country okay so you have lots of sub cultures hostee doesn't actually address that very well
[00:29:38.400 - 00:29:51.360] at all cool okay so then with that is the need to recognize cultural perspectives so these are
[00:29:51.360 - 00:30:01.040] my childhood values including for not only a tongue and an archetanga we talked about in an
[00:30:01.920 - 00:30:08.560] last week when we're looking at building relationships unpacking the word what it actually means
[00:30:08.560 - 00:30:15.920] is uplifting the power of someone else that's what it's about okay so when you're you know
[00:30:16.880 - 00:30:21.840] meeting someone hosting them you're actually trying to empower them
[00:30:22.480 - 00:30:32.880] um cool so always keep those in the back of your mind as well okay this is when things start
[00:30:32.880 - 00:30:37.600] get really interesting so we've talked a lot about the individual now we're moving into
[00:30:37.600 - 00:30:46.480] a decision making with groups and when you put people into groups things get weird okay so
[00:30:47.200 - 00:30:56.720] um yeah changes can occur and those changes in decision making can also depend on the structure of
[00:30:56.720 - 00:31:05.440] your group factors that uh affect through decision making include leadership the group norms are the
[00:31:05.440 - 00:31:13.840] rules of behavior social pressure conformity okay as well as the the individuals within that group okay
[00:31:14.320 - 00:31:24.000] um yeah so be aware of that yeah not only do you have different attitudes and behaviors within
[00:31:24.000 - 00:31:29.760] the group that as soon as you put people into their group those behaviors and attitudes change
[00:31:30.800 - 00:31:37.280] okay irrespective of who the individuals are okay so it's um no one's solved group work yet
[00:31:38.240 - 00:31:44.080] but yeah some interesting things now this one's wild um the ash experiment anybody's seen the ash
[00:31:44.080 - 00:31:56.640] experiments oh no one yeah a little bit yeah crazy stuff check it out play is one of the
[00:31:56.640 - 00:32:03.360] psychologists oldest and most popular pieces of research a volunteer is told that he's taking part
[00:32:03.360 - 00:32:09.360] in a visual perception test what he doesn't know is that the other participants are actors
[00:32:09.360 - 00:32:14.400] and he's the only person taking part in the real test which is actually about group conformity
[00:32:14.400 - 00:32:20.400] please begin the experiment you'll be taking part in today involves the perception of line length
[00:32:20.400 - 00:32:25.120] the task will be simply to look at the line here on the left and indicate which of the three lines
[00:32:25.120 - 00:32:30.640] on the right is equal to it in length so for example if the actors have been told to match the wrong
[00:32:30.640 - 00:32:37.200] lines the volunteer will be monitored to see if he gives the correct answer or if he goes along
[00:32:37.200 - 00:32:44.540] with the opinion of the group and gives the wrong answer in the first test the correct answer is two
[00:32:46.380 - 00:33:14.700] one one one once again the correct answer is two three three three three three three
[00:33:15.660 - 00:33:21.260] the ash experiment has been repeated many times and the results have been supported again and again
[00:33:22.060 - 00:33:28.380] we will conform to the group again with very social creatures we're very much aware of what the
[00:33:28.380 - 00:33:34.700] people around this tank we want to be liked we don't want to be seen to rock the boat so we will
[00:33:34.700 - 00:33:42.620] go along with the group even if we don't believe what people are saying we'll still go along one one
[00:33:43.100 - 00:33:47.980] one one group dynamics is one of the most powerful forces in human psychology
[00:33:50.380 - 00:33:59.950] one one crazy hey another one here but I'll probably skip it pretty similar idea
[00:34:02.270 - 00:34:09.150] yeah but in this one basically what they show is that group dynamics and conformity
[00:34:10.110 - 00:34:16.430] is actually passed down over time okay so they have an embedded culture and that culture will
[00:34:16.430 - 00:34:25.070] actually cascade into the future so yeah if you've got more time we'll come back to it okay
[00:34:26.590 - 00:34:33.870] yes so there's a whole bunch of symptoms you might have heard the term group think
[00:34:34.510 - 00:34:39.550] okay so group think is when you start to get a group of people together and they start to make
[00:34:39.550 - 00:34:49.310] decisions which don't make any sense okay so and there's eight different symptoms of group think
[00:34:49.950 - 00:34:57.550] okay so illusions of fault in vulnerability this is when optimism creates an environment that
[00:34:57.550 - 00:35:06.510] encourages risk or risk taking collective rationalization is when a group discount warnings
[00:35:07.870 - 00:35:15.230] or do not challenge their own assumptions belief in inherent some morality this is when group
[00:35:15.230 - 00:35:22.030] members own self-belief or conviction means that they ignore the ethical and moral consequences
[00:35:22.030 - 00:35:29.600] of their decision okay so stereotype views of external groups this is when group members have
[00:35:29.600 - 00:35:40.160] negative views of the enemy making some responses unnecessary okay so yeah they will convince themselves
[00:35:40.160 - 00:35:47.360] that there is an enemy and their views are wrong pressure on the centers okay so when group members
[00:35:47.440 - 00:35:53.200] are under pressure from others to not express arguments against the group view okay so
[00:35:54.720 - 00:36:01.040] being told off after a meeting that you shouldn't have said that that's
[00:36:02.800 - 00:36:11.840] yet pressure on the scent self censorship you know when the doubt is don't feel like they can actually
[00:36:11.840 - 00:36:20.160] speak up an illusion of unanimity this is when the group thinks that they were in 100% agreement
[00:36:20.640 - 00:36:29.520] but the reality is that it is not true at all okay often driven by a guru okay self appointed
[00:36:29.520 - 00:36:34.960] mind guards these are when group members protect the group and the leader from the information that
[00:36:34.960 - 00:36:42.640] is problematic or contradictory to their own views okay so group think happens and this
[00:36:42.640 - 00:36:48.720] some classic engineering and even military case studies where group think has led to disasters
[00:36:50.240 - 00:36:57.520] okay classic one is the Columbia space shuttle disaster 2003 that killed seven people
[00:36:58.160 - 00:37:05.760] yeah you probably won't even born then but what happened was that a large chunks of foam or ice
[00:37:05.760 - 00:37:14.400] that built up on the rocket as was being cooled down before launch as it launched the vibration
[00:37:14.400 - 00:37:21.360] shook those blocks free hit the ceramic tiles which were designed to protect the shuttle and the
[00:37:21.360 - 00:37:32.640] astronauts from basically death on on reentry there was a big report into the Columbia disaster
[00:37:33.440 - 00:37:40.960] by the US military afterwards and yeah what they found was that there were elements of group
[00:37:40.960 - 00:37:48.320] think that led to that disaster okay so the program managers created huge barriers against
[00:37:48.320 - 00:38:00.000] dissenting opinions so my recommendation to you have someone who in a team who can freely
[00:38:00.000 - 00:38:07.120] express the dissenting opinion so remember in a job I was hired years ago I got put on to the
[00:38:07.120 - 00:38:15.840] committee and I said why am I here and they said because you're a critic and I went oh okay
[00:38:18.560 - 00:38:24.400] yeah so and I was there to to challenge because again I wanted to avoid group think I do the same as
[00:38:24.400 - 00:38:31.600] well so in our department we run in an industry advisory board and when I'm looking at bringing
[00:38:31.600 - 00:38:37.600] people onto that board I want to make sure that I've actually got someone who can actually challenge
[00:38:39.840 - 00:38:47.680] provide alternative opinions okay yeah but on the first side cohesion can actually lead to
[00:38:47.680 - 00:38:55.520] really good performance but yeah high group cohesiveness can actually lead to group think
[00:38:55.840 - 00:39:05.840] yeah and yeah when someone does actually put forward a dissenting view sometimes that view can be
[00:39:05.840 - 00:39:13.840] taken up or it can be rejected coming back to the ash experiments what was really interesting about
[00:39:13.840 - 00:39:22.400] the research that happened after that was that the vast majority of people put through those tests
[00:39:22.480 - 00:39:28.720] conformed okay so they went with the group even though the group was wrong but occasionally
[00:39:29.920 - 00:39:36.400] you had someone who held on no matter what they said not one one is not the same as two
[00:39:37.440 - 00:39:42.240] and they kept holding the position but they were in a very small minority I think it was less than
[00:39:42.240 - 00:39:53.660] five percent of people who kept holding the line cool yeah so group leaders part of their role
[00:39:54.220 - 00:40:01.900] is on to facilitate communication but to try and tease out those dissenting voices and creating an
[00:40:01.900 - 00:40:10.220] environment that people can actually share their own opinions as well as expressing different
[00:40:10.220 - 00:40:22.300] views okay so yeah more diverse teams can perform better yeah but there's also evidence that more
[00:40:22.380 - 00:40:30.060] homogenous groups actually perform really well okay so again we have been solved through group
[00:40:30.060 - 00:40:38.220] dynamics thing well what is clear though reinforcing what I was talking about last week is that
[00:40:38.220 - 00:40:46.380] collaboration and the processes that the teams use are the key to excellent performance okay and
[00:40:46.380 - 00:40:55.420] that is enabled by excellent communication including listening I also just want to make a point
[00:40:55.420 - 00:41:04.540] that group decisions are ultimately made by individuals okay so when you hear people say the company
[00:41:04.540 - 00:41:17.630] made a decision it's not the company is actually people who made that decision okay right so how
[00:41:17.710 - 00:41:36.660] might group conformity affect ethical decision making any ideas don't you turn this is certainly
[00:41:36.660 - 00:41:43.540] answer it we'll come back to it in a couple of weeks time okay so how do we address conformity
[00:41:43.540 - 00:41:50.180] in decision making so we can use frameworks for decision making okay so like using ethical codes
[00:41:50.340 - 00:42:00.180] conduct normalizing dissent Boeing used to do this okay so the 737 Max which I talked about last
[00:42:00.180 - 00:42:07.380] week a little bit they used to normalize dissent okay but then that went away and it was one of the
[00:42:07.380 - 00:42:19.780] factors that led to the 737 Max disasters okay you can introduce ways of people expressing
[00:42:20.180 - 00:42:32.420] their views anonymously okay so you know send in your your responses via email to this and de-identify
[00:42:32.420 - 00:42:42.020] it to be wary that sometimes IP addresses are actually identifiable as well yeah so when you're doing
[00:42:42.020 - 00:42:47.300] a survey you might actually want to check that they've actually disabled IP address
[00:42:48.020 - 00:42:53.060] tracking because sometimes they do that if you're working in an office they can trace it back to your
[00:42:53.060 - 00:43:02.820] land port okay and yeah and have groups that cannot offer diverse perspectives including an external
[00:43:02.820 - 00:43:13.540] view okay to avoid group think as an individual when you don't agree with something call it out okay so
[00:43:13.700 - 00:43:22.100] because chances are there's someone else in your team who is going I don't think this is true
[00:43:22.820 - 00:43:34.900] I don't agree with this okay call it out yeah and and look consequences of questioning the majority
[00:43:34.900 - 00:43:41.380] versus keeping quiet okay so yeah this is really quite tricky is that sometimes if you're
[00:43:41.380 - 00:43:46.420] seem to be constantly questioning the majority of people you start to get a bit of a name
[00:43:47.700 - 00:43:53.140] okay it's been that the tricky one who keeps asking difficult questions okay but then you need
[00:43:53.140 - 00:43:58.020] to balance that about you know what if you just keep quiet what's gonna happen okay that's how
[00:43:59.140 - 00:44:06.740] the state's what disasters happen okay so coming back now to codes of conduct
[00:44:07.620 - 00:44:17.220] yeah so these are written by people okay and typically from strong input of members of that
[00:44:17.220 - 00:44:23.700] society as well as experts okay so they might actually have experts in ethics come into help
[00:44:23.700 - 00:44:31.220] write these okay and yeah they set clear and collective standards of how people should behave
[00:44:31.860 - 00:44:40.420] accounting for hopefully lots of diverse perspectives okay but yeah what do you think some of the
[00:44:40.420 - 00:44:46.820] challenges are with coming to consensus about what a code of conduct actually looks like
[00:44:52.190 - 00:45:03.330] yeah yeah perfect yes so yeah so you have to compromise on wording and you're not expressing
[00:45:03.650 - 00:45:18.940] everyone's views in that compromise yeah very good okay not all right yep sure yep so you might not
[00:45:18.940 - 00:45:25.500] be able to include absolutely everything and yeah people's weightings on what is important what is
[00:45:25.500 - 00:45:32.300] not very different okay yeah so as a consequence what you're finding is that you're actually starting
[00:45:32.300 - 00:45:40.700] to to average things out and you're moving towards a framework which is pretty centrist okay
[00:45:41.020 - 00:45:49.660] it's in the middle and it's not going to include some really interesting clauses that are on the
[00:45:50.460 - 00:45:58.860] ends if you like okay and we'll come back to that in a couple of weeks the IEEE code what should
[00:45:58.860 - 00:46:05.660] be improved in that what did people come up with do you remember last week I don't remember much
[00:46:05.660 - 00:46:21.330] last week hopefully you remember more than me yeah yeah yeah yeah so yeah there's nothing in there
[00:46:21.330 - 00:46:27.650] really about it's yeah by culturalism I triple e's a global organization right and it's
[00:46:27.650 - 00:46:36.930] it's going to be hard to capture that yep yeah yeah yeah so yeah nothing really about the environment
[00:46:36.930 - 00:46:43.330] yep sure and you might see in some of the other codes that was pretty similar as well yeah so
[00:46:43.410 - 00:46:49.330] on the environment I mean that's one thing where it's actually very hard to reach consensus on so
[00:46:50.050 - 00:46:56.690] in the truth that I was in last week I was talking to the group about how engineering New Zealand
[00:46:56.690 - 00:47:01.570] developed their code of conduct they actually wanted a stronger clause in the code of conduct
[00:47:01.570 - 00:47:07.250] and that climate change they couldn't actually reach consensus within embers on what that clause
[00:47:07.250 - 00:47:15.410] actually looks like yeah so it can be very hard to yeah to get more interesting codes in there
[00:47:17.090 - 00:47:25.730] cool okay so some takeaway messages see a cognitive biases stereotypes and implicit biases that
[00:47:25.730 - 00:47:33.490] affect your decision making the first perspectives do support better decisions be very wary of
[00:47:33.490 - 00:47:40.450] group dynamics including conformity and group think as well as you know how decisions are actually
[00:47:40.450 - 00:47:49.090] being made and codes of conduct set the ethical standard based on diverse inputs okay so
[00:47:49.970 - 00:47:56.530] a couple of things that I'm going to do over the next week or two is to complete the question
[00:47:56.530 - 00:48:04.850] yeah in the vice diversity and ethics section by August 10 I'll show you what that looks like in
[00:48:04.850 - 00:48:13.730] a second and then I want you to read this critique about hosteeds model okay so should
[00:48:13.730 - 00:48:19.970] hosteeds model be applied to an organization and should it be applied to individuals and why
[00:48:20.930 - 00:48:31.410] okay so the question I want you to ask to answer is a bit of an ethical to a data one so yeah you've
[00:48:31.410 - 00:48:38.450] got sensors are installed pretty much everywhere on devices these days and you've been gifted a
[00:48:38.450 - 00:48:44.450] high-end smartwatch from a company called Zelik case that are private based company based here in
[00:48:44.450 - 00:48:53.570] New Zealand and this includes like a Fitbit right we've got pulse heart rate O2 levels location data
[00:48:53.570 - 00:49:01.410] and so on and it can share some of that data with all sorts of apps okay so Spotify snapchat as well
[00:49:01.410 - 00:49:11.490] as you know fitness apps okay in the end user agreement they say that they will use your data
[00:49:11.490 - 00:49:17.490] to provide you with personalized health recommendations okay so including whether or not you
[00:49:17.490 - 00:49:23.970] might actually be at risk for things like cancer or heart disease okay so maybe it's detected a
[00:49:23.970 - 00:49:30.450] very strange heartbeat and it's gone oh that's a signal okay but they said that they're going to
[00:49:30.450 - 00:49:41.490] protect your data and keep it safe and protect from misuse and with your consent they will transmit
[00:49:41.490 - 00:49:49.490] the data from your watch back to Zelik headquarters for analysis okay as individuals I want you to answer
[00:49:50.370 - 00:49:57.090] whether or not you'd accept this maybe depends more I want to actually see what's in the details
[00:49:57.090 - 00:50:03.970] of the user agreement or not I'm going to reject the watch and put it on trade me for someone else to
[00:50:05.890 - 00:50:11.810] yeah to have probably don't have to declare on your gift register at work but yeah whatever okay
[00:50:11.810 - 00:50:20.370] see I do those couple of things for me next week for those of you in B8 to B14 you've got your
[00:50:20.450 - 00:50:26.370] Pycultural Co-confidence workshops we have two guest lectures on intellectual property
[00:50:27.730 - 00:50:33.250] I'm struggling to get hold of Virginia for Senator a couple of emails I'm going to give her a call
[00:50:34.210 - 00:50:38.610] to make sure that she's locked in for next week she said she was a few months ago but
[00:50:38.610 - 00:50:43.890] she's not answering but I'll lock that in if she's not around then we'll do some lecture
[00:50:43.890 - 00:50:51.650] shuffling we'll bring up some of those those other lectures to a bit earlier cool and just a reminder
[00:50:51.650 - 00:50:59.010] if you're in B8 to B14 these are your rooms okay so they changed in week one so you just check your
[00:50:59.010 - 00:51:04.290] timetable well and then send references and resources you don't have to read them if you want but if
[00:51:04.290 - 00:51:10.690] you want to get stuck in you're more than welcome cool see you next week have an awesome weekend
[00:54:10.050 - 00:54:17.890] thank you for the message oh no that's so good

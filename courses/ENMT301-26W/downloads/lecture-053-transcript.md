# ENMT301-26W Lecture 53 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_53_audio_16k_mono_32k.mp3`
Source audio SHA-256: `0978f1faa11d1ba7428b8bde1ed1d6811d1c1eb9b66eec12e71960393acbcb5f`
Generated: 2026-06-06T07:01:42.350053+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:01 - 00:00:11] Alright, thanks everyone. I think we'll make a start there.
[00:00:11 - 00:00:18] Can hear some really good conversations. I think we'll be out answer a few things today, hopefully.
[00:00:18 - 00:00:39] So as we start, I do have a few notices, but apparently I like to switch things up a tiny
[00:00:39 - 00:00:43] bit just because I saw this, this flow chart that I've made in the past.
[00:00:43 - 00:00:48] Oh, this might be a timely time to remind you guys about this.
[00:00:48 - 00:00:54] They kind of I suppose builds on that whole fact of making sure that you're spinning a little bit of time on everything
[00:00:54 - 00:00:58] and don't get to the end of this assignment having only gone halfway through this flow chart.
[00:00:58 - 00:01:03] So just as a show of hands so that I can kind of get a feel for where everyone is at
[00:01:04 - 00:01:09] in the assignment and then you amount of detail or what I talk about I understand.
[00:01:09 - 00:01:12] I, yeah, they haven't looked at that so they won't want to talk about that.
[00:01:12 - 00:01:18] But hell, who has basically determined this system load and done that first bit of
[00:01:18 - 00:01:21] is my sheer force and linear moment diagram for my front plane and my top plane?
[00:01:22 - 00:01:26] Cool, cool, cool. It looks like most people have at least made a start,
[00:01:26 - 00:01:31] but your hands are going to be made a start on it. Cool, so ideally by the end of this you'll
[00:01:31 - 00:01:35] be feeling relatively comfortable and confident with what you've got moving forward
[00:01:35 - 00:01:39] and that's been sort of my mission for the last kind of couple days or the emails.
[00:01:40 - 00:01:46] Maybe I just get emails from people that they see people doing different stuff and panic,
[00:01:46 - 00:01:51] but in terms of your system loads, I think we made it really clear that you start by working out
[00:01:51 - 00:01:56] what your chain load direction is and then that is going to have a massive influence about what
[00:01:56 - 00:02:03] forces you see or don't see in your front and top plane, right? And so if not only in the horizontal
[00:02:03 - 00:02:07] direction and you're probably only going to see them from the top plane, if the chain is only
[00:02:07 - 00:02:12] acting in the vertical direction then the opposite plane will be the one that you see and if
[00:02:12 - 00:02:17] the chains on some angle then you'll see them in both, right? So there's kind of three ways that
[00:02:17 - 00:02:21] people will go and that's why some people on the frequently asked questions are asking,
[00:02:21 - 00:02:26] well seeing that you know if there are sort of what you do is depends on what you'll see, right?
[00:02:26 - 00:02:30] So all of those ways that are completely fine as long as you state what you assume
[00:02:30 - 00:02:37] your chain direction to be and similarly we then have to look at our secondary moments, right?
[00:02:38 - 00:02:42] So with the loads I think we hopefully we'll clear that we're assuming it for our maximum
[00:02:42 - 00:02:48] motor torque, unless we've specified otherwise in the idea that we'll have some sort of clutch that
[00:02:48 - 00:02:55] slips at that kind of value or a predefined value around that, right? So we're designing our
[00:02:55 - 00:03:00] shaft for a certain torque that is probably going to be well above the actual torque required
[00:03:00 - 00:03:06] for one cart to go up the hill and so that was another check to do is to make sure that the chain
[00:03:06 - 00:03:12] tension that you've developed using this assumption of the maximum motor torque that there is
[00:03:12 - 00:03:20] actually enough power to power your system, right? Any questions on the story so far? Where
[00:03:20 - 00:03:27] everyone's like yeah we've done that we're happy. I need one or the other otherwise I'm
[00:03:27 - 00:03:32] we've got some slide nods, got some thumbs up, everyone's happy if you're watching online hopefully
[00:03:32 - 00:03:38] you're happy as well. Cool and so from that, then we'll see we also need to consider this whole
[00:03:38 - 00:03:45] secondary moment that's occurring from our universal drive shaft, right? So maybe the easiest way for
[00:03:45 - 00:03:53] me to talk about that in a clear way is just to draw a little sketch in just 101 sketching
[00:03:53 - 00:04:07] coming in clutch once again if I can find a pin and so with that I jump over here in the
[00:04:07 - 00:04:14] main thing that I'm trying to show is that in this case we've got this is good we've got our
[00:04:14 - 00:04:19] fixed bearing, our fixed bearing and our bearing that's on a roller we have some universal drive
[00:04:19 - 00:04:24] shaft as we're going through some angle and what this is telling us based on the plots and the
[00:04:24 - 00:04:31] slide is that for a z-configuration there is an additional force that occurs on the perpendicular plane
[00:04:31 - 00:04:37] so if I'm looking in the top view and there's an additional force I can't remember the directions
[00:04:37 - 00:04:47] follow the diagrams directions that occurs twice every revolution, right? And so what we see is that in
[00:04:47 - 00:04:55] this case it will be ending moment diagram or if this is bearing A and this is bearing B it sort
[00:04:55 - 00:05:00] of looks something like this and then this is the end of our end of our shaft, right? Because what's
[00:05:00 - 00:05:06] happening is twice a revolution it's like someone's just like literally bending applying a moment
[00:05:06 - 00:05:11] at the end of our shaft again I don't know if the direction I've just drawn in degrees of that I
[00:05:11 - 00:05:20] don't think it does but I make it clear then yeah and so the idea with that is then if this is our
[00:05:20 - 00:05:27] top view then depending on what way our chain loads are if we're trying to calculate what the next
[00:05:27 - 00:05:32] moment is here then I think our other one the beginning moment diagram is only between A and B
[00:05:33 - 00:05:37] so we know that this would be our next moment value but if we were trying to work out what is the next
[00:05:37 - 00:05:43] moment at this point where our sprocketers or we're going to have to consider both of these values and
[00:05:43 - 00:05:53] combine them if there's multiple values on multiple planes so hopefully we're happy there
[00:05:54 - 00:06:00] but that's where the secondary moments come in but once you've got those you should be away
[00:06:01 - 00:06:06] laughing in terms of doing the next things right so we can use those
[00:06:06 - 00:06:11] beginning moment diagrams to work out what our moment is to put in our shaft diameter calculations
[00:06:11 - 00:06:17] and what our reaction forces about bearings for are then that will let us select a bearing now
[00:06:17 - 00:06:22] some people said that they've had a relatively large sized shaft and it's bigger than the
[00:06:22 - 00:06:28] bore diameter of the sprocket that is okay just make sure that you note that that is something
[00:06:28 - 00:06:34] that will need to be updated subsequently right so I don't think that I don't expect you to do any
[00:06:34 - 00:06:40] iteration in terms of improving some of the stuff that you've been given so for example
[00:06:40 - 00:06:43] people trying to say like do I have to pick a different sprocket and if I pick a different sprocket
[00:06:43 - 00:06:50] to do the whole thing again no no no just say the manager has made a mistake here and that either
[00:06:50 - 00:06:55] the sprocket needs to be bored to a bigger size or a different sprocket with the same pcd
[00:06:56 - 00:07:02] will need to be selected yeah and so if you have a big shaft that means you're going to need a big
[00:07:02 - 00:07:08] bearing big bearings are strong that means that you may have a bearing life that is relatively large
[00:07:09 - 00:07:16] now if that is that's just the nature of having a big shaft and a big bearing right and so
[00:07:17 - 00:07:22] as long as you don't try and pick the biggest possible bearing for the bore diameter
[00:07:23 - 00:07:29] ideally you do the opposite then you may still have a bearing life calculation that might be more
[00:07:29 - 00:07:34] than 20 years but we're possible we want to see that you're sort of slightly minimized that's
[00:07:34 - 00:07:37] so some people I think have used roller bearings and being like you know George these things are going
[00:07:37 - 00:07:43] to last for eternity and I said okay well maybe you need to check and do a check and see if you had
[00:07:45 - 00:07:56] a ball bearing whether it would still be able to hold them in the m
[00:07:56 - 00:08:01] loads and stuff because if you're doing too big then it actually adds complexity to your system to make sure that you're
[00:08:01 - 00:08:08] kind of like a risk be right you're going to get what the risk be kind of gives you and if it's yeah if it's a
[00:08:08 - 00:08:18] big shaft then you have a big bearing which will be strong keep going you can make a comment but um yeah that
[00:08:18 - 00:08:23] was my main points any questions on any of that or hopefully that's put a few people at ease with a like
[00:08:24 - 00:08:36] yeah cool so for this rich here the main focus if I go where am I going I'm going to get out of that one
[00:08:37 - 00:08:45] go on this one we'll see what I had prepared so we can check the freaking last questions and
[00:08:45 - 00:08:50] general comments apparently I was gonna have a paper polish but I think it's published last week
[00:08:50 - 00:08:54] so if I was going to bring any questions you have we'll go over detail drawings and review a few drawings
[00:08:55 - 00:09:01] and then any selection process questions you have kind of relating to that flow diagram that we see
[00:09:01 - 00:09:08] how can highlight these engineering tools of time in terms of my notices we've talked about our
[00:09:09 - 00:09:14] times in on assignment two and being proactive about that I think the teaching review is still on
[00:09:14 - 00:09:20] progress I know it goes away if you do do it I really appreciate some feedback especially positive
[00:09:20 - 00:09:25] feedback if you have appreciated what I've done but obviously if there are things you think I can
[00:09:25 - 00:09:32] prove I'm always trying to improve and for re-test obviously obviously we had a bunch of them happen
[00:09:32 - 00:09:37] on Monday if you're coming next Monday if you're not making any changes you can just rock up thank you
[00:09:37 - 00:09:49] for your patience I know that it is time consuming process sometimes cool so at this point the floor
[00:09:49 - 00:09:53] is yours and I have to make sure that I note down any questions you guys have so that the second
[00:09:53 - 00:10:18] tutorial also has the same sort of questions so what questions currently at top of mind so
[00:10:24 - 00:10:35] so for the springs the question was actually a system here do we need to use the books yeah so
[00:10:35 - 00:10:41] the references like Shigley is kind of the goat but we've kind of packed out the equations that
[00:10:41 - 00:10:47] we want from Shigley so what I would say if you're trying to do the side quest relating to the
[00:10:47 - 00:10:56] springs specification the example calculation is probably a useful example to see right so you'll
[00:10:57 - 00:11:02] write up something that is relatively similar in terms of what amount of force you'll want
[00:11:02 - 00:11:07] to what kind of deflections they'll let you get a spring constant that you're aiming for and
[00:11:07 - 00:11:12] then I expect a table that's sort of similar to this where then you kind of say okay here are the
[00:11:12 - 00:11:18] options this is the one that I would recommend going forward and you'll put the information that's
[00:11:18 - 00:11:26] in this end to I think we saw it just earlier this kind of spring specification form so for this obviously
[00:11:26 - 00:11:31] you don't have to fill out everything but the mandatory stuff is probably kind of important to have
[00:11:31 - 00:11:36] filled out but for example you might not need to fill out B you just have one inside diameter
[00:11:37 - 00:11:44] and you'll have to specify your units whether you're using ISO units or American units but
[00:11:45 - 00:11:53] probably makes sense to use ISO ones right so some of the stuff here you may be able to specify
[00:11:53 - 00:11:59] some of it you may not be able to specify that is okay we have some things blank right but
[00:12:01 - 00:12:08] yep full of material how do we specify that a good question you mean so full of material you'll see
[00:12:09 - 00:12:17] that it's good to notice up here the wise frequently of high strength of 1600 to 2000 megapascals
[00:12:17 - 00:12:24] so what you well what you could do is literally just go and find a common material that is used
[00:12:24 - 00:12:30] for spring and just reference that you know so whether it's what you've heard the material was I
[00:12:30 - 00:12:34] think we'll move on to frequently ask questions though did it on my computer and I managed to find
[00:12:34 - 00:12:40] I either material here has a yield or a tensile strength of this or an expuniceable strength but
[00:12:40 - 00:12:47] it's just of this so they are quite high the other thing I would recommend is we have a spring
[00:12:47 - 00:12:54] that is in compression right so if the thing is loaded in compression what is one possible failure
[00:12:54 - 00:13:00] that we might want to check out buckling and the easiest way to do the buckling thing
[00:13:01 - 00:13:11] would be to annotate a plot it looks like this right so once you have your selected spring you
[00:13:11 - 00:13:18] could go okay my critical value of if over l0 over d is this and my relative deflection is the
[00:13:18 - 00:13:28] therefore it should be fine for that right if it's not fine I would probably well have anyone done
[00:13:28 - 00:13:38] it yeah if it's not fine and it's easy to update ensure updated otherwise say this might want to
[00:13:38 - 00:13:44] be updated before being actually made if that's the night before and you're doing it right but
[00:13:45 - 00:13:54] the bigger effort is not buckling right that's what we want to see yeah yeah the idea would be that
[00:13:54 - 00:14:02] you should have enough information in the assignment brief to sort of fill out a relatively similar
[00:14:05 - 00:14:10] table for your kind of specific situation and I think it specifies the amount of load
[00:14:10 - 00:14:36] that it wants to apply something quite big from you me yeah good question so the question was
[00:14:36 - 00:14:44] how do we know what wider mentions or diameters would be standard right so typically what we want
[00:14:46 - 00:15:07] is we probably want steel and here and then we could say you do this ideally you should be able to
[00:15:07 - 00:15:15] find in reference something that looks sort of similar to this I will try to find one that I
[00:15:15 - 00:15:21] think is from a reputable source that you can kind of see here that nominal dimensions in the
[00:15:21 - 00:15:28] millimeter are appropriate yeah so as long as you're not specifying that you want a 16.63 millimeter
[00:15:28 - 00:15:34] diameter but in general I'd say as long as you're picking a whole number for millimeters that's
[00:15:34 - 00:15:42] relatively fair for the smaller sizes of spring diameter they probably do have each half millimeter
[00:15:42 - 00:15:48] but again so long as you're at your assumptions clear I'm sort of happy right so you can see in here
[00:15:48 - 00:15:54] in this example they've gone fearing from six to eight in each 0.5 millimeter diameter increment
[00:15:56 - 00:16:02] yeah I'll try to find find a resource that might be useful but yeah
[00:16:04 - 00:16:11] cool there's good questions yeah again similar to like I think a lot of people have been kind of
[00:16:11 - 00:16:14] work trying to work out with someone trying to work out how I picked eight kilonewtons
[00:16:15 - 00:16:19] I've picked eight kilonewtons I was like that seems like a lot of force that should
[00:16:19 - 00:16:26] definitely push it so with you you're just you're just going with that number not having to justify
[00:16:26 - 00:16:36] why eight kilonewtons is enough away too much or not enough right sweet all right is good
[00:16:36 - 00:16:51] questions other ones yeah it's up to you so what do you have to specify for the incanditions of
[00:16:51 - 00:16:57] the spring well if we assume that it's going to be on through parallel surfaces then you probably
[00:16:57 - 00:17:06] want it ground but oh just pick one yeah this one seems probably not appropriate but any of the
[00:17:06 - 00:17:13] ground ones probably appropriate because we're not doing it a bit of that design it's kind of
[00:17:13 - 00:17:22] trivial and yeah like if you wanted to you could say any ground end if you really didn't want
[00:17:22 - 00:17:34] to make the call well the question so do we care about the number of active versus inactive coils
[00:17:34 - 00:17:44] these ones here you will use the number of active coils for is it in I don't remember myself right
[00:17:45 - 00:17:52] you didn't know the number of active coils I believe if you've got an active coils on the end
[00:17:52 - 00:17:56] then you would know that retrospectively once you've done it right that they calculate it in the
[00:17:56 - 00:18:09] first instance you're doing active coils yeah so I guess the overarching thing is that this is a
[00:18:09 - 00:18:18] preliminary calculation to guide future design right so those sort of really specific decals are
[00:18:18 - 00:18:27] lists what we're looking at I'll just make sure that what is asked for in the assignment is
[00:18:27 - 00:18:35] completed right so for completeness if I grab that one and I grab that one we can see it should say
[00:18:35 - 00:18:45] here here's our information about this launch spring indicate the material by a diameter number
[00:18:45 - 00:18:50] of coils which I'm assuming is the active coils but if you want to specify both you can spring
[00:18:50 - 00:18:58] constant and fill out the manufacturer's form right so the idea is that this piece of work that
[00:18:58 - 00:19:04] you've done could be used or built upon once you're kind of through the detail design is done it's
[00:19:04 - 00:19:10] not really typical that this kind of thing would be one and done and we can see in here we've got
[00:19:10 - 00:19:18] the spring kind of calculations as part of this part here right so I'd kind of make sure you're
[00:19:18 - 00:19:24] filled up this table and specified the material wide diameter number of active coils and probably
[00:19:24 - 00:19:44] shown that it's not going to buckle right yeah that's right yeah answers yeah so that question
[00:19:44 - 00:19:51] was should we include should we include two approaches but essentially yes they need to be
[00:19:51 - 00:19:59] considered so yes you need to consider of your standard loading plus your loading from your secondary
[00:19:59 - 00:20:05] moments yeah so similar to what I was drawing on the screen you either will have
[00:20:07 - 00:20:15] I think I've drew a sign there so I want to ask me to grab it to that probably some random page
[00:20:20 - 00:20:25] the idea is that the secondary well that the bending moment is she falls moment diagrams so
[00:20:25 - 00:20:32] done combined then you can use them basically like a wrist speed book I suppose but otherwise if you've
[00:20:32 - 00:20:38] got two then you just combine them yeah I don't know if I made it clearly but the question of
[00:20:38 - 00:20:46] I will first try to re summarize the question do we do we need to combine our moment diagrams for both
[00:20:46 - 00:20:58] the secondary moment loading and the loading from the sprocket the short answer is you don't have to
[00:20:58 - 00:21:05] you could but they both need to be considered so because sometimes there are more than different
[00:21:05 - 00:21:10] planes for some people over the recombination of them you know what I mean so it's not really like
[00:21:10 - 00:21:16] so yeah for some people if your secondary moment forces are acting on the same plane as your
[00:21:16 - 00:21:20] load forces probably makes sense to combine those could then make you a job easier for acting
[00:21:20 - 00:21:25] perpendicular or some combination then I'd probably do the math retrospectively and use like
[00:21:25 - 00:21:38] Pythagoras or whatever to work out the maximum moment would be at that point yeah cool
[00:21:40 - 00:21:53] other questions yeah okay there's a good question about fatigue right so I'm sorry my list here
[00:21:54 - 00:22:04] so I've flipped the question away but sorry to put you on the spot but for fatigue
[00:22:06 - 00:22:23] how how we have we covered fatigue at all so far have we covered it anywhere is open to everyone
[00:22:24 - 00:22:30] have we mentioned the word fatigue anywhere someone's nodding I feel like the answer is yes
[00:22:31 - 00:22:37] George but I don't want you to ask me where it is because I don't know and so the question basically what
[00:22:37 - 00:22:45] I'm trying to say is for your loading do I have to consider fatigue no this assignment is not looking at
[00:22:45 - 00:22:50] designing for fatigue explicitly right they're saying that if you're a mechanical engineering
[00:22:50 - 00:22:56] machine enemy 3.1 we'll give a specific assignment for designing for fatigue we'll do that in a lot
[00:22:56 - 00:23:03] more detail however there is this concept in fatigue called infinite life is everyone I'm just
[00:23:03 - 00:23:08] gonna stick on my own voice does anyone want to summarize in layman terms what does infinite
[00:23:08 - 00:23:29] life mean not free grads for summer it never breaks yes so infinite life is when the loading is
[00:23:29 - 00:23:35] such that you can just keep applying that load forever and you'll never break to make some sort of
[00:23:35 - 00:23:40] weird analogy I don't know I just come up with this right now I should probably should stop doing
[00:23:40 - 00:23:45] this but it'll be like if you had like a three year old trying to punch you like how long could you
[00:23:45 - 00:23:51] survive for probably forever right under a certain amount of like punching force like your body will
[00:23:51 - 00:23:56] be like sweet but for like a 10 year old like you could definitely last like quite a lot of punches
[00:23:56 - 00:24:02] but maybe if they are like if they are infinitely able to still apply the same amount of force
[00:24:03 - 00:24:08] then the material probably won't last forever and then you know 15 year old you might be getting lower
[00:24:08 - 00:24:13] cycles so that kind of idea there right but under some threshold is this assumption in material
[00:24:13 - 00:24:20] science which has been hotly debated and it's not really true but it kind of works for meals
[00:24:21 - 00:24:28] in some situations that below a certain loading limit you have infinite life right and so
[00:24:29 - 00:24:36] what you could do if you want to do an additional check for your shaft diameter would be to use what
[00:24:36 - 00:24:45] we have shown as the wasting house equation right so I'll talk about the ASME equation you're
[00:24:45 - 00:24:50] running those that one right and that's just what standard loading it gives you a shaft size
[00:24:51 - 00:25:07] so I get to it so here's the ASME equation and then here's our cyclic thing and here's that
[00:25:07 - 00:25:15] wasting house formula so one thing that you could do and you'd suppose be rewarded for going to this
[00:25:15 - 00:25:23] detail if you wanted to would be to check whether your diameter would be safe for fatigue or not
[00:25:23 - 00:25:29] you could do this equation and say okay using the whisking house you know do I get the same diameter
[00:25:29 - 00:25:37] or as if smaller or as if they go then my standard loading would I update my shaft diameter I
[00:25:37 - 00:25:43] probably not I'll just say this is going to be used this is going to be designed or keen as we
[00:25:43 - 00:25:47] take in before making this design as the wasting house diameter is less than a minimum diameter
[00:25:47 - 00:25:55] from the ASME so more than a minimum diameter therefore future work needs to be done in that area
[00:25:55 - 00:26:03] right yeah so all I'm trying to say here again if we're looking in here shaft diameter
[00:26:03 - 00:26:09] calculations that could be one that you do so I'm trying to say right so you can use the ASME
[00:26:09 - 00:26:14] in a couple places of interest maybe at your bearing that you're designing for maybe at your
[00:26:14 - 00:26:22] sprocket could work out at those two points what is this factor of safety with a load factor
[00:26:22 - 00:26:27] and a stress concentration and if you wanted to check out whether fatigue is going to be an issue
[00:26:27 - 00:26:33] or dip your finger in and you could use this equation it would tell you nominally whether it will
[00:26:33 - 00:26:38] or won't be right but the thing is that you'll have to look up for your material what the endurance
[00:26:38 - 00:26:45] does right which may or may not be easy to find that roughly you can approximate it if you can't
[00:26:45 - 00:26:55] find it as being about half of how you were a UTS kind of quite remember off the top of my head
[00:26:55 - 00:27:03] but we normally we touch on fatigue a little bit later in the term we just have like a real
[00:27:03 - 00:27:09] higher level so yeah let us go question is that answer I feel like I'm just sort of gathered
[00:27:10 - 00:27:14] it's not the main focus for this assignment right but it could be a check that you do
[00:27:14 - 00:27:19] that could be a check that check assumes infinite life that's why I say more of a
[00:27:19 - 00:27:24] information is needed right same thing with the analogy you think might be safe but then you can use
[00:27:24 - 00:27:28] other methods to work out actually how many cycles it would be safe for and then how that compares
[00:27:28 - 00:27:33] to the life of the system that I feel like I'm going way too far in the wrong direction now so I'm
[00:27:34 - 00:27:46] going to tack back to the middle other questions is it good everyone has anyone done any clutch
[00:27:46 - 00:28:01] calculations you know okay so I guess the main thing there was that we're making multiple plots i.e.
[00:28:01 - 00:28:08] more than one plot and we're making a recommendation from that and the recommendation could be
[00:28:09 - 00:28:14] sweet you need this clutch this material and has this saturation force which is acceptable in terms
[00:28:14 - 00:28:20] of the allowable pressure on my plate or it might be the amount of activation force that you need
[00:28:20 - 00:28:26] as ginormous so the number of patch you need is as ginormous this is a terrible idea if you wanted
[00:28:26 - 00:28:34] to do it this is what you would need to have but it doesn't make much sense yeah so the scan is relying
[00:28:34 - 00:28:40] or relating to that thing of sometimes ideas people have don't always work yeah I haven't done
[00:28:40 - 00:28:46] the numbers myself this year so I can't remember I don't know what kind of clutch size you'll get
[00:28:46 - 00:28:57] for what kind of materials all right any subsequent questions well if they pop up if we have time
[00:28:57 - 00:29:04] we'll just answer them otherwise there's always the 10 minutes in between so last time we talked
[00:29:05 - 00:29:11] drawing essentials I can't remember if I've showed it oh here it is does it look like you have tried
[00:29:11 - 00:29:17] so I would title it so you filled out the title block correctly you just kept all letters
[00:29:17 - 00:29:22] as the size slash layout if you're drawing appropriate do your drawing views show all your details
[00:29:22 - 00:29:30] and functionality you know you uncluttered and easy to read then intermediate as are you following
[00:29:30 - 00:29:35] the drawing standards are there specific times and are they appropriate so some specific areas
[00:29:35 - 00:29:42] in your design might have tolerance that is different to the global tolerance of your part
[00:29:42 - 00:29:49] two dimensions follow the drawing standard are they easy to measure or are they
[00:29:51 - 00:29:56] yeah are they easy to measure and from reasonable data again do your drawing views select show all
[00:29:56 - 00:30:03] the key details and functionality and this is more talking about if you had things like detailed
[00:30:03 - 00:30:11] views or section views so the drawing standard is on the website so in general the idea is a clear
[00:30:11 - 00:30:17] drawing is a good drawing and if and doubt clarity wins if the convention that is outlined in the
[00:30:17 - 00:30:26] drawing standard makes you have to do things in a way that you think is overly cluttered so
[00:30:27 - 00:30:33] this is clean dimensions reasonable types and use of notes to improve clarity I think a few people
[00:30:33 - 00:30:38] probably learned about this when we were looking at our aluminium structure assignments that if you
[00:30:38 - 00:30:43] had had some notes then it might have made it easy to kind of make your part to the way that you
[00:30:43 - 00:30:51] intended it rather than the way that your drawings made you intend to make it wrap so notes are
[00:30:51 - 00:30:59] okay and ideally you'd discuss the drawing with the person making it if you were a grad working
[00:30:59 - 00:31:07] in a workshop or similar so obviously you may be not Tony this time but I know Owen and Dave and Dave
[00:31:07 - 00:31:13] were how he were talking about this so a good engineer will know what dimensions are critical
[00:31:13 - 00:31:21] on the design to ensure that the part functions as intended so I kind of call this designers intent
[00:31:21 - 00:31:25] some of those things where if you're just balancing someone else's drawing or didn't mention
[00:31:25 - 00:31:29] something else's drawing it's kind of hard to know this but if you know what the part is and what
[00:31:29 - 00:31:34] it has to interact with then there will be some more critical dimensions than others
[00:31:35 - 00:31:40] so earlier in the term we did talk about this whole idea of there being standard kind of
[00:31:40 - 00:31:47] tolerances or appropriate tolerances for linear dimensions and so this might be of use for
[00:31:47 - 00:31:55] dimensioning different parts in your drawing depending on what the kind of size is wrap and so
[00:31:55 - 00:32:02] sometimes on drawings if there are a number of different length ranges you might even have a
[00:32:02 - 00:32:08] table for your tolerances that shows for things up to 30mm this is the tolerance that I want to use
[00:32:08 - 00:32:14] and for things 30mm to 100mm this is the tolerance for 100 to 200 this is the tolerance you know
[00:32:14 - 00:32:21] the mean that is something that you will see on some drawings but you guys are sort of that's just
[00:32:21 - 00:32:27] the same information there and then we have this kind of thing for our bearing housing which is kind
[00:32:27 - 00:32:33] of the icing on the cake or the shifts kiss when it comes to dimensioning the diameter of your shaft
[00:32:34 - 00:32:40] where the bearing will be seated right so what kind of fit is it likely that we would want
[00:32:41 - 00:32:48] well I think a lot of the time the manufacturer might tell you but if we have an interference
[00:32:48 - 00:32:54] foot then that's going to need some specialist encouragement to get the bearing in place right
[00:32:54 - 00:33:01] because that's when our bore of our bearing would be actually smaller than the size of our shaft right
[00:33:02 - 00:33:08] so we either need lots of force or some heating and cooling magic to make it all go together
[00:33:08 - 00:33:16] do transition foots exist and really no right so transition foot kind of shows like
[00:33:16 - 00:33:22] up depending on the exact measurement that is kind of manufactured you may have an interference
[00:33:22 - 00:33:27] though you might have a clearance or loose foot but then if you want you think to be easily assembled
[00:33:27 - 00:33:33] some sort of loose foot would be appropriate and don't know if I included the links but
[00:33:34 - 00:33:39] their Wikipedia page on engineering foots is actually really good for specifying the types of
[00:33:39 - 00:33:44] running foots if this is something you end up doing or needing for your finer projects or similar
[00:33:44 - 00:33:49] but the idea would be that you specify where your bearing manufacturer would tell you what the
[00:33:49 - 00:33:52] or diameter is going to be and so you therefore should probably specify your
[00:33:55 - 00:34:04] shaft to account or allow for this. So see some examples here from Dr. Angus McGregor
[00:34:04 - 00:34:11] this was a machine there was a linear sculpture that he designed for his PhD but we see some
[00:34:11 - 00:34:17] examples of use of notes reasonable tolerances a nice complete title block and clear dimensions
[00:34:17 - 00:34:23] where we've mentioned a smaller things and then the larger things you can see here that
[00:34:23 - 00:34:28] here's actually not followed the drawing standard and some instances where he's added the
[00:34:28 - 00:34:34] dimensions on the path. I would not recommend this but he's done that in this case because otherwise
[00:34:34 - 00:34:41] it would make it more cluttered or difficult to read if he did pull them all outside.
[00:34:42 - 00:34:51] So sit and views useful for showing detail don't section shafts or fasteners don't section shafts
[00:34:51 - 00:34:56] or fasteners don't section shafts or fasteners don't section shafts or fasteners you're going to be
[00:34:56 - 00:35:02] drawing a shaft and your housing will probably go together with fasteners so apparently if you repeat
[00:35:02 - 00:35:06] things three times to all make it makes it more memorable so when you're checking off your drawing
[00:35:06 - 00:35:13] probably remember that so we can see here another section view in this case we've got some
[00:35:13 - 00:35:20] machine for our roughness which also might be useful if you've got specific requirements on your
[00:35:20 - 00:35:28] shaft for your seals and then we see here sometimes you might have parts that are difficult to
[00:35:28 - 00:35:34] see or manufacture just using the view the large global view to heading a detail view
[00:35:35 - 00:35:44] as an easy way to simplify adding more detail about this area of your part. So in terms of your
[00:35:44 - 00:35:50] assembly drawings this is what you'll be kind of doing to be showing one section view of your shaft
[00:35:51 - 00:35:58] you're now just showing the bill of materials color views are often not appreciated only
[00:35:58 - 00:36:03] explode parts where you need for clarity see some other things there if overall dimensions for the
[00:36:03 - 00:36:10] viewing assignment important details should be included see another example here we see another
[00:36:10 - 00:36:18] example of a cutaway section which would be useful if you want to only show part of your
[00:36:22 - 00:36:28] part of your part essentially so for example if you have a keyway you can't mention hidden detail
[00:36:28 - 00:36:36] hidden details kind of outlawed so you might want to do a cutaway or a partial section to show
[00:36:36 - 00:36:45] the keyway dimensions. Cool so let's look at some examples and see what is good and not so good
[00:36:46 - 00:36:53] and because you guys are first I think all the examples I've got are on learn but would we want to
[00:36:53 - 00:37:03] look at old students' office first when you were student examples first old like I felt sweet so
[00:37:05 - 00:37:15] let's drawing here what are our initial comments thoughts about it what is good what is not so good
[00:37:21 - 00:37:26] so I think I've mentioned this one before or shown it in one of the lectures we've got two
[00:37:26 - 00:37:32] bearings here that's not a good idea because that's going to give us a fairly rigid
[00:37:35 - 00:37:41] situation right we've got two pins which means that it's very difficult to actually work out
[00:37:41 - 00:37:48] what is the load going through each of our bearings right so if your bearing is not big enough
[00:37:49 - 00:37:55] take a bigger bearing don't add two bearings it's kind of what we're saying here right
[00:37:55 - 00:38:01] but in terms of the actual functionality we see some good things right so we've got a nice shaft
[00:38:01 - 00:38:06] shoulder if we were to do what we were doing in the lecture today if we push on this way is that
[00:38:06 - 00:38:11] actually restrained yes right because we can have force going through here and then through here
[00:38:11 - 00:38:15] through this into our plate yeah and if we push on this way is it actually restrained
[00:38:21 - 00:38:28] yes or no as actually restrained if we push on this into the shaft so if we go through the bearing
[00:38:30 - 00:38:37] will that work will it go through the bearing no right there's nothing stopping the in the
[00:38:37 - 00:38:42] seat of the bearing or the inner race of the bearing so it's not actually restrained in that
[00:38:42 - 00:38:47] direction but it is in that direction yeah so this is the kind of thing we'll be looking at for
[00:38:47 - 00:38:52] your assignment to make sure it is actually restrained we have seals they look like they are easy to
[00:38:52 - 00:38:58] kind of relative the easy to assemble and replace our bearing housing goes together we have a
[00:38:58 - 00:39:03] grease nipple that is good a fasteners not sectioned our shafts not section we've got a partial
[00:39:03 - 00:39:22] cutaway cool I think I'm just gonna leave that one of that all right this one here what we think
[00:39:22 - 00:39:35] what's good what's not good so we can start with the bearing detail is the detail of the bearing
[00:39:35 - 00:39:41] good or not good not good we can't see the bearing detail for your assignment we kind of want to be
[00:39:41 - 00:39:50] able to see whether it's a roller or a ball bearing how it goes together because typically we
[00:39:50 - 00:39:56] would have an inner and outer race right now with that why do we think might be an issue with this
[00:39:56 - 00:40:06] design the way that it's shown like that will it operate as intended see some shapes of the head
[00:40:06 - 00:40:12] what do we think is what's gonna happen if it was actually getting used as a machine it's
[00:40:12 - 00:40:19] gonna rub like crazy right so this whole side here is up against it so remember that this is our
[00:40:19 - 00:40:26] rotating element and that should be inner bearing race should be rotating we've got a small gap
[00:40:26 - 00:40:37] which is good right kind of sort of we'll see and then this bit here is stationary but this bit
[00:40:37 - 00:40:46] here is rubbing right this bit stationary this bit moving that's not good same thing on this side
[00:40:46 - 00:40:51] here depending on where our bearing is this bit's rotating that bit stationary so we've got some
[00:40:51 - 00:40:56] issues there in there in there and there if we were to push on up what would happen is actually
[00:40:56 - 00:41:21] restrained it's gonna be more rubbing right madly inducing yeah the previous example or this one
[00:41:21 - 00:41:33] previous example so it's unclear here whether it's rubbing on that side there looks like there's a
[00:41:33 - 00:41:37] gap on the side here it looks like this should be a gap right so we've got a gap that's good
[00:41:38 - 00:41:44] that's gap there yeah but those are good things to kind of check and you do want to show that
[00:41:44 - 00:41:51] detail explicitly in this case here if we push on this direction the whole thing just like
[00:41:52 - 00:41:59] crest isn't that but there right not good we push on this direction where we're already rubbing
[00:41:59 - 00:42:04] on this side here so it's kind of unclear whether it's exhale or lee restrained we see we haven't
[00:42:04 - 00:42:13] used standard drawing convention so we're not really too happy there but we do have a lock now it
[00:42:13 - 00:42:19] looks like it's slightly narrower which is good but those are the kind of things that we want you
[00:42:19 - 00:42:24] to be able to think about with how we actually go together so in this case here our bearing is also
[00:42:25 - 00:42:29] it's not actually restrained on the top half right so if we even if this wasn't here in the
[00:42:29 - 00:42:36] bearing the shaft was kind of appropriate we would still have the bearing just move in what on the way
[00:42:39 - 00:42:46] cool so there's two examples I just am aware of time we can always have a look at more but what
[00:42:46 - 00:42:56] you will probably produce might look something more like this so if you have a quick
[00:42:58 - 00:43:03] one minute if you note down something's got a good sometimes maybe not so good
[00:43:24 - 00:43:29] does anyone got anything that they want to say what is good what could we for we were marking
[00:43:29 - 00:43:46] this student what would we pet them on the back for yeah guess good so that's good good shaft
[00:43:47 - 00:44:03] not seetion excellent right else is good let's say is the cross-section good is that clearly
[00:44:03 - 00:44:14] showing that there are different parts yes I'd say good cross-section what else is good I mean
[00:44:14 - 00:44:31] there are some dimensions probably not perfect especially with the precision but okay so
[00:44:31 - 00:44:37] I guess we were all just waiting to be able to say what is not so good with it so what's not so
[00:44:37 - 00:44:47] good with this drawing actually restrained in one direction okay let's have a look so if we push this
[00:44:47 - 00:44:53] way it's gonna go through into there into there which is good and then if we push this way the shaft
[00:44:53 - 00:45:00] just moves and if it moves too far this thing's gonna have that thing yeah so that's probably room for
[00:45:00 - 00:45:18] improvement improve yeah so that's good what else is there any rubbing is there any rubbing
[00:45:18 - 00:45:27] we need to be yes or no dust sealers okay to be touching so I think we've got no rubbing
[00:45:29 - 00:45:38] yeah dust seal should be done that yeah cool what what could we improve there now bill of materials
[00:45:48 - 00:45:56] I kind of want to go through another drawing so I'm hoping that we can go faster it's what
[00:45:59 - 00:46:04] yes quite big we could make it smaller yes the size would be a big way better for like this big
[00:46:04 - 00:46:10] then we could make this drawing a bit bigger so yeah I think size slash layout could be improved
[00:46:10 - 00:46:16] now this is one thing that always seems to get me but the part number here should be a part number
[00:46:16 - 00:46:22] if it is a part that has a part number right i.e your bearing will have like i it's WB 2001
[00:46:23 - 00:46:29] zen yeah that's where the part number would go if that's just the random thing probably don't have
[00:46:29 - 00:46:35] the part number have it blank in description you could say what it is right so sometimes
[00:46:35 - 00:46:42] it seems it always be people that will have this kind of uh right these kind of rows in there
[00:46:42 - 00:46:46] bill of materials and if you're just repeating yourself just have description and not part number
[00:46:47 - 00:46:52] but if you've got parts that do have part numbers make sure you use that appropriately right
[00:46:52 - 00:47:01] other things that I would improve on do we have capital leaders no is the bill of material
[00:47:01 - 00:47:12] is the table of contents filled out completely no do we have any surface conditions for our seals
[00:47:14 - 00:47:21] no so we could specify our surface conditions for our key way which they don't have
[00:47:22 - 00:47:26] if it was a key way then we'd have a partial section oh yeah here right here we could actually show
[00:47:26 - 00:47:31] the partial we should really show that as a partial section can't just randomly have saying
[00:47:31 - 00:47:38] sectioned and then yeah cool all right we've got two and a half minutes let's hope I pick a good one
[00:47:41 - 00:47:51] or an easy one to improve on i guess this one here what would we improve is the title block filled out
[00:47:52 - 00:48:07] no so that's one thing right what else could be improved dimensions so two add dims go
[00:48:08 - 00:48:24] what else could be improved do I like this thing here I don't like why I don't mind it if it's
[00:48:24 - 00:48:32] filled out properly but either fill or delete there's three right what about our bill of materials
[00:48:38 - 00:48:44] it's what part numbers so yeah for these things here if it's not a part then I would remove that
[00:48:44 - 00:48:53] these ones are parts yeah so I think we could capital leaders will also be another thing cool
[00:48:53 - 00:49:01] in terms of our parts what do we think about it is it good should it be made smaller I mean if they're
[00:49:01 - 00:49:09] making it this small why not just make it micro size right so I would say I mean four five would
[00:49:09 - 00:49:18] probably be size go six would be is there any rubbing is there actually a strain in both directions
[00:49:19 - 00:49:26] so I think rubbing is okay right the rubbing is good but x here restraint is probably
[00:49:26 - 00:49:35] to be improved think if we push on this side here that's only got the bearing there's nothing holding
[00:49:35 - 00:49:44] it in place here have we six in our shaft we have where we should not right that should really be
[00:49:45 - 00:49:55] and but we might want a partial section that there we need to add add key slash important
[00:49:55 - 00:50:19] dimensions we might want to add surface conditions what else can we think of our tolerances
[00:50:19 - 00:50:25] tolerances could be updated probably as well depending on what it is that we want right
[00:50:31 - 00:50:37] the other thing that I would just comment on it's not necessarily tier a bill we've got a
[00:50:37 - 00:50:43] greased never which is good so we can get greased into our system we've got seals are yeah
[00:50:44 - 00:50:48] Ellen there that seal I don't know if you can see that it's hard to see
[00:50:49 - 00:50:56] but you can see how the seal is kind of in the sink that's just like this that's quite hard to get the seal in
[00:50:56 - 00:51:03] there without ruining the seal so similarly I've seen sometimes I've seen
[00:51:03 - 00:51:12] I've seen shafts that look like this before there's our bearing yeah once again
[00:51:13 - 00:51:18] seen shafts that look like this with a shaft is like you just machine out a bit for the bearing
[00:51:19 - 00:51:23] to go to make sure it's a symbol of all right so it's kind of like that's impossible to get together
[00:51:25 - 00:51:31] so yeah make sure that we probably want to have that would need to be going flat across the air
[00:51:31 - 00:51:35] then there might need to be a different step up to some dimensions that sort of would need to
[00:51:35 - 00:51:42] be changed make sure we don't ruin our bearing we do have a locating sprigate which is good makes it
[00:51:42 - 00:51:51] easy to put our thing together so check that and what else was I gonna talk about so we could
[00:51:51 - 00:51:56] have like we could have other locating sprigates on some of these other things and if we've got a
[00:51:56 - 00:52:03] fastener I would purposely choose my section view to kind of show the fastener so that you can actually
[00:52:04 - 00:52:12] see the load path clearly I've gone over time which I hate doing and I know your time is very valuable
[00:52:13 - 00:52:20] so I'm gonna leave it there tools down if I've got further questions let us know and
[00:52:22 - 00:52:28] I think I think I don't have anything like explicit that I have to go through next time so we'll
[00:52:28 - 00:52:33] probably be like it was last term where we open questions and then I'll just float around
[00:52:33 - 00:52:36] seems to be a nice way to finish things off

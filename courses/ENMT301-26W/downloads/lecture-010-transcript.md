# ENMT301-26W Lecture 10 Echo transcript

Source: Echo360 audio downloaded under Marco's authorised UC Learn access.
Transcript type: Hermes local ASR from local audio, not native Echo transcript.
ASR backend/model: faster-whisper tiny.en, CPU int8, beam_size=1.
Source audio: `C:/Users/marco/Documents/Hermes/UC/courses/ENMT301-26W/echo360/downloaded-audio/lecture_10_audio_16k_mono_32k.mp3`
Source audio SHA-256: `6fd66155e40d1532f8e2e8a3a84d11e2262e73481b5095a26314cb7110112437`
Generated: 2026-06-06T05:15:41.091768+12:00
Caveats: Hermes local ASR, not native Echo transcript.; Fast first-pass settings: tiny.en, int8, beam_size=1. Use for exam context; technical terms may need checking against PDFs.

[00:00:00 - 00:00:09] before we go. I just checked, I think there's 96 out of the 121 of you who have
[00:00:09 - 00:00:18] completed the Robocup server. So be really handy if the other 25 people did that. Is
[00:00:18 - 00:00:23] anyone here not done it? Or are you guys just the ones who turn up and they've probably
[00:00:23 - 00:00:31] done what I asked you to do? It's very handy if we can get everyone to do that. So I'll
[00:00:31 - 00:00:36] look at a message on learn either today or tomorrow reminding everyone just to complete
[00:00:36 - 00:00:44] that. Also don't forget to vote for your class reps on the Toronto 3rd year page. I think
[00:00:44 - 00:00:52] maybe 60 people have voted for that. So it's like half of you. So go on, do a vote. I think
[00:00:52 - 00:00:57] forget one of them closes on Sunday, one of them closes on Friday. I can't remember which ones
[00:00:57 - 00:01:06] were. So try and remember the video. So we've got any questions from last week after our lecture talking
[00:01:06 - 00:01:18] about requirements. Is anything important? You might death these silence. Okay, so clearly there we
[00:01:18 - 00:01:24] are. Well, I think you might have, I don't know, the observance of you might have noticed. I have uploaded
[00:01:24 - 00:01:33] a document describing the brief for the robot cup now. It's similar to previous years. Every year
[00:01:33 - 00:01:38] we make a few minor changes just to keep things interesting. Has anyone seen that? How
[00:01:38 - 00:01:45] looking? It's on the Learn page under the Robocup section. There's a document there. I don't know
[00:01:45 - 00:01:50] what it's called. I forget 2026 Robocup description or something to the out of here. So feel free
[00:01:50 - 00:01:59] to have a look. The main differences are going off the top of my head so I might get along.
[00:02:01 - 00:02:05] One this year you'll have to take three weeks on, two weeks on board last year,
[00:02:05 - 00:02:10] they're only about two weeks on board. So that's good. Obviously you've still got them home and you
[00:02:10 - 00:02:15] get a bonus. So you get double the points. If you drop them off back at home. So that's cool.
[00:02:15 - 00:02:22] The other thing is I've banned rubber bands or because you all turn into little lawyers when I
[00:02:22 - 00:02:28] come still looking at the Robocup results, I had a robotic brief and I always get these questions of
[00:02:28 - 00:02:33] people trying to skirt through what I've written and I'm not a lawyer. So that's not like
[00:02:34 - 00:02:40] contract law or anything like that. You've got to read it with the sort of skirt and the intent
[00:02:40 - 00:02:44] of what we're trying to do here. So that comes to me with something that's essentially a rubber band
[00:02:44 - 00:02:51] and you're trying to weasel it through some little loop-off. While reading that document you might
[00:02:51 - 00:02:57] find some attempts to address things like that. We defined on board as being if you pick out the
[00:02:57 - 00:03:03] robot at the end of the competition and the weights come with it. So then some students one year
[00:03:03 - 00:03:08] came and asked if they had the weights sort of on these Bombay doors underneath the robot and when
[00:03:08 - 00:03:15] it detected that it was being picked up they opened and they're like no that's not all right because
[00:03:15 - 00:03:20] obviously you get penalized if you've got more weights on board than you're allowed and so you know
[00:03:20 - 00:03:28] they were trying to work around that. And so read it by thinking about the intent of what we're
[00:03:28 - 00:03:40] trying to do. So rubber bands I think I've defined them as highly an elastomer with high-air
[00:03:40 - 00:03:50] spectraicio by it's long and thin and it's quite elastic rubber bands with rubber strips
[00:03:50 - 00:04:00] things like that. The reason I do that this year is you have to as part of the first report you
[00:04:00 - 00:04:05] have to do some investigation on the videos of what occurred in previous years and what you've
[00:04:05 - 00:04:11] seen is last year a combine harvest the one year before that a combine harvest the one. I think
[00:04:11 - 00:04:16] the year before that wasn't a combine harvest but things start to converge you've got to see
[00:04:16 - 00:04:21] that's winning and that's also relatively easy to manufacture so we'll copy that so I'm trying to
[00:04:22 - 00:04:28] encourage you to do other creative things. The other thing is you'll remember last year there
[00:04:28 - 00:04:36] was a snatch which you've got points for collecting right so this year all going well and I tried to
[00:04:36 - 00:04:41] write this somewhat broadly so in case something cracks out and we can't manage this but the
[00:04:41 - 00:04:46] general idea is there's a snitch and a budget one of them will be red and one of them will be blue
[00:04:46 - 00:04:53] isn't the LEDs inside it they are the same little sparrow robots one will be red I saw one will be green
[00:04:53 - 00:04:57] so they're not the same colors as your bases I don't know red and blue whatever I don't know
[00:04:57 - 00:05:03] season the thing I'll read in yellow that's one of those red in yellow one is plus three kilos
[00:05:03 - 00:05:09] one's minus three kilos so you've got you ideally want to click one and not the other or maybe
[00:05:09 - 00:05:14] just don't click do you hear them and that way you say but there will be not only two in the
[00:05:14 - 00:05:26] arena at the given point in time okay any questions about that no cool so once we have got the
[00:05:26 - 00:05:33] finalized robo cap surveys so this will be early next week we will then go through the process of
[00:05:33 - 00:05:38] assigning groups and then I'll make your way of those groups and you can start thinking about
[00:05:38 - 00:05:47] something to the reason it's not coming to okay cool so obviously with robo cap coming up some
[00:05:47 - 00:05:52] requirements is quite important we talked about that last week but the next important thing is to
[00:05:52 - 00:05:56] sort of start thinking about your system design and architecture of your system design and that's
[00:05:56 - 00:06:04] kind of what we're starting to talk about today I think this quote by see whoa how was a
[00:06:04 - 00:06:11] a British computer scientist do you do cost one one to one what I wanted to the algorithm
[00:06:11 - 00:06:18] scores yeah and so you do quick sort that algorithm right or invent of the quick sort algorithm
[00:06:19 - 00:06:24] so you know about bugs but there's two of those design assistants one is to make it so simple that
[00:06:24 - 00:06:29] they are obviously no bugs and the other is to make it so complex that there are no obvious
[00:06:30 - 00:06:36] and what you'll see in many robo cap years is there are many systems that are quite complex
[00:06:37 - 00:06:44] they have bugs and then obvious until a competition day but you know that's it is a relatively
[00:06:44 - 00:06:53] complicated system regardless with the set and our design V system design and sort of architecture
[00:06:53 - 00:07:01] what do you think what is this system what's the make it on a system since we talked
[00:07:01 - 00:07:10] since this whole course is called make it trying to system design I guess in a more higher level
[00:07:10 - 00:07:25] I guess you yeah it's now it's quite hard to describe as an I struggle as well but yeah I think
[00:07:25 - 00:07:30] you guys you're both getting to it it's a collection of I suppose parts being make it
[00:07:30 - 00:07:37] trying to mechanical or a little computational but they achieve when they're brought together
[00:07:37 - 00:07:42] in a system they achieve more than those parts do individually right and so the system
[00:07:42 - 00:07:46] aspect is that they're integrated and therefore they can achieve something that you can't necessarily
[00:07:46 - 00:07:52] just achieve with the parts by themselves or a collection of parts that aren't integrated right
[00:07:52 - 00:07:57] and so system design is sort of thinking about that collection of the parts and how they
[00:07:59 - 00:08:04] connected right and so that's where we've kind of got analysis and architecture there because our
[00:08:04 - 00:08:12] architecture is starting to think about how these parts are connected and you know and then
[00:08:12 - 00:08:19] the design this is this is iterative and here right once we think about system design you've kind
[00:08:19 - 00:08:24] of you concepts and you come and go and you make changes to the particular parts or you're going
[00:08:24 - 00:08:33] to do things you potentially you know tossing around ideas and so the idea of this lecture
[00:08:34 - 00:08:41] will talk about the broader parts of this so I think this is quite a nice point to make is
[00:08:41 - 00:08:48] every electronic system consists of things that fall into these categories right so the ones
[00:08:48 - 00:08:56] that you mentioned senses communications information processing subsystems CPU's or embedded systems
[00:08:57 - 00:09:03] you figures so everything that you picked the outside environment power subsystems so
[00:09:03 - 00:09:12] everything's like batteries and power regulation systems and housing right but the interesting
[00:09:12 - 00:09:19] thing is that they're not ways arranged in the same way right so everything everything sort of
[00:09:19 - 00:09:25] of megatronics e fits includes well they include all these some of these may not be included
[00:09:25 - 00:09:30] right some of them will be some of them won't be some of them some of the megatrust systems will have
[00:09:30 - 00:09:34] all of these some of them won't have a couple but they're arranged in a different way and so
[00:09:34 - 00:09:42] again that whole idea of architecture is how these are arranged is there anything else that we've
[00:09:42 - 00:09:57] missed there do you think or did that cover and megatronic systems so megatronic system design
[00:09:57 - 00:10:02] less than the context of what we're talking about here kind of covers two things there's architecture
[00:10:03 - 00:10:10] which is the components and how they're connected together both physically and in terms of
[00:10:10 - 00:10:16] wires and communications and power and some and then there's the attributes and the behaviors of
[00:10:16 - 00:10:21] the components both individually and when they're connected so obviously architecture we've got
[00:10:21 - 00:10:25] the idea that what do you think what do we mean by attributes and behaviors of components
[00:10:32 - 00:10:38] what might be an attribute I don't know we've got a Volkswagen golf here and all the bits that make it
[00:10:38 - 00:10:43] up there's a nice illustration of a system right these are all the bits that make up a Volkswagen
[00:10:43 - 00:10:50] golf or an older one but it's a bit useless like that you can't drive it to school
[00:10:52 - 00:10:58] but the parts are all there they're just arranged in a not very helpful way but let's take
[00:10:58 - 00:11:05] the main body of that what might be an attribute of that body wait yeah so weight is an attribute
[00:11:06 - 00:11:16] what's another attribute yeah the material yeah there's an attribute yeah yeah strings
[00:11:18 - 00:11:26] uh yeah shape size these sorts of things right so attribute to basically it things that has
[00:11:26 - 00:11:31] right all the things that we've mentioned other things that we haven't mentioned and then so what
[00:11:31 - 00:11:35] are behaviors of attributes of things that are has what's what's the behavior
[00:11:37 - 00:11:43] sorry yeah things that are does right so attributes things that has the
[00:11:43 - 00:11:49] behaviors of things that it does and then those the parts of our Megatron system will have these
[00:11:50 - 00:11:57] attributes and behaviors individually just the scale out on the floor but also when you've got them
[00:11:57 - 00:12:03] connected together that may change some of that behavior and so in talking or thinking about system
[00:12:03 - 00:12:11] design when we're defining our system we've got to define the architecture so that's the components
[00:12:11 - 00:12:17] that it has and how they're connected and we also need to take into account the attributes and
[00:12:17 - 00:12:23] behaviors because they will lead us to maybe choosing those particular components and so on so
[00:12:23 - 00:12:30] like with RoboCarp it's quite nice because you get a massive kit of stuff you've largely all got
[00:12:30 - 00:12:38] the same stuff but you look at those RoboCarp robots that have either one or persisted on the
[00:12:38 - 00:12:45] window cell and the Tron lab and there are a lot of this commonality between them but there's a
[00:12:45 - 00:12:52] a lot of difference right and particularly things like backup mechanism and stuff and so defining
[00:12:52 - 00:12:59] the system is pretty much starting to define these you know the components and how they connected
[00:12:59 - 00:13:06] and what their attributes and behaviors are and so it's good to note that that system is more than
[00:13:06 - 00:13:17] just the sum of its parts right so is the architecture defines the structure of the system
[00:13:18 - 00:13:22] so would we have this at a you know what sort of level you know if we're going to draw
[00:13:22 - 00:13:28] with sketching out we're thinking about our RoboCarp robot and we want to start thinking about the
[00:13:28 - 00:13:39] architecture of it how might we do that how would you do it if you've got a pen and a paper piece of
[00:13:39 - 00:13:57] paper high level or low level would you start would you start and maybe look at all the low level
[00:13:57 - 00:14:02] things there's a whole there's a whole lot of screws there's some nuts there's some extruded aluminium
[00:14:03 - 00:14:07] if you start at that level we'll just start at the high level controller
[00:14:09 - 00:14:13] pick up mechanism and things like this how much you do it
[00:14:14 - 00:14:18] it's probably high level right I mean you can do bottom up design
[00:14:20 - 00:14:24] there's like starting to design a microchip with right I've got a lot of transistors
[00:14:24 - 00:14:30] I've got to put these in a good order all you can start at that high level and say all right I need
[00:14:30 - 00:14:35] a CPU I need a motorbike you need something like that so for the high level is often a good way of
[00:14:35 - 00:14:41] doing it and so you might start thinking about your architecture from that high level and that's a top
[00:14:41 - 00:14:47] down type approach right you have these big wheel blocks like a pickup mechanism what would you do
[00:14:47 - 00:14:54] then in that process once once you've got a rough idea you've got to pick up mechanism you know
[00:14:54 - 00:14:59] that you're going to not use a combine harness to pick up mechanism perhaps this year
[00:15:00 - 00:15:04] you've got an idea about how you're going to do it what would be like what do you do then you've got
[00:15:04 - 00:15:14] there you've got maybe a locomotion system in mind maybe you've got an investigation strategy in
[00:15:14 - 00:15:22] mind what do you do then with each of those high level block so you go straight to a straight
[00:15:22 - 00:15:29] approach I can just think you've got to figure out the components you need so what I would probably
[00:15:29 - 00:15:33] suggest is you start at that high level and then you drill down a bit right and so you go into that
[00:15:33 - 00:15:43] and you break that part or that that's larger scale block of pickup mechanism into a smaller
[00:15:43 - 00:15:47] scale blocks and smaller scale blocks you're drilling down to the point at which you can do
[00:15:47 - 00:15:54] separate type in the testing as you dive down and so each of these aspects it's kind of a
[00:15:54 - 00:16:01] hierarchical method right you start at the top robot pickup mechanism locomotion navigation
[00:16:01 - 00:16:07] sensors and then you dive down into those and each of those you kind of expand until you get to a
[00:16:07 - 00:16:12] point where you can kind of implement it you don't need to expand that to open you need to expand
[00:16:12 - 00:16:18] to a point where you can you know what transistors and what diodes are in there probably not right
[00:16:18 - 00:16:25] just to the modules that you can use and for this case we give you those modules and so that's
[00:16:25 - 00:16:32] you know we've got a high level structure of the system and we started a high level and that allows
[00:16:32 - 00:16:38] us to abstract away the fine details you don't necessarily need to know what exactly is going on
[00:16:38 - 00:16:43] inside those right and for the range sensors the time of flight sensors anything like that
[00:16:45 - 00:16:51] and it provides a nice broad understanding of how your system is going to work so you can do this
[00:16:51 - 00:16:55] and then you could pass it to your friend in the class and they'll be able to understand what you're
[00:16:55 - 00:17:12] trying to achieve because it's at a fairly high level so the two related types of architecture
[00:17:12 - 00:17:19] I suppose one is we've got physical architecture and that's the physical relationships between
[00:17:19 - 00:17:26] the things that's where they are laid out in space and so and then we contrast that with
[00:17:26 - 00:17:32] functional architecture which are the components of the systems but you know related to the
[00:17:32 - 00:17:38] the functions that they perform and therefore the connections between them in terms of information
[00:17:38 - 00:17:43] to change energy and to change and that sort of thing so there's a picture of an old
[00:17:43 - 00:17:51] rover cut robot it's got numbers pointing to very aspects of it various aspects but they're
[00:17:51 - 00:18:02] either physical or a functional architecture sort of diagram that for physical yeah because we can see
[00:18:02 - 00:18:07] with things are laid out physically you know we can see with a long range and for its
[00:18:07 - 00:18:15] sensors the IRA the micro servos where they are physically but it doesn't necessarily tell us
[00:18:15 - 00:18:23] much about the functional behavior of the the paths that make that up but would you you know if in
[00:18:23 - 00:18:30] thinking about your design would you think about the physical architecture maybe first or would
[00:18:30 - 00:18:38] you think about the functional architecture first what would make sense functional
[00:18:40 - 00:18:51] a advances on that yeah I would say functional like that's how you subdivide the problem
[00:18:51 - 00:18:58] into functional units in the physical architecture then you've got the functional stuff and then
[00:18:58 - 00:19:05] you've got to figure out how they are connected physically or how they are arranged physically
[00:19:05 - 00:19:11] because you could take all these components of your rover cut robot and put them in a whole
[00:19:11 - 00:19:16] different physical layout and it won't be any good for picking up weights or competing in that
[00:19:16 - 00:19:22] competition right physical is important but the functional kind of leads to that physical they're
[00:19:22 - 00:19:28] both important they're both related but it is starting at the functional side is a good place
[00:19:29 - 00:19:38] to start and that's mostly what this picture is about is functional architecture so ultimately in
[00:19:38 - 00:19:44] our and considering systems design from high level what we want is a collection of M strand so you're
[00:19:44 - 00:19:52] not really going into really deep details at this point components maybe subsystems or modules
[00:19:52 - 00:19:58] and so for rover cut that's the kind of things you get right you get drive motors you get
[00:19:58 - 00:20:08] motor drivers you get processing units you get sensor units servos and stuff so you've got modules
[00:20:08 - 00:20:16] and subsystems they're defined in terms of the attributes so what they have their behaviors what
[00:20:16 - 00:20:23] they do in their interfaces so how they kind of talk to the other to whatever needs to control it
[00:20:24 - 00:20:32] and then there's obviously a bunch of connections between those so just this is a functional
[00:20:32 - 00:20:38] architecture in I suppose in a photo that's shown the physical architecture of a robot that was
[00:20:38 - 00:20:44] developed by a picture student one years ago MOS Shreyfi I did have to check what Mario stood for
[00:20:44 - 00:20:50] his mobile autonomous robot for intelligent operations and so it was designed to you know this is
[00:20:50 - 00:20:57] going back to the I don't know before COVID times and the idea of this was that was using
[00:20:57 - 00:21:02] my optical flow and other stuff to be able to navigate accurately in the absence of GPS so
[00:21:02 - 00:21:08] you know maybe under factory cover and orchids or in mines and stuff like that and so
[00:21:09 - 00:21:15] what he was trying to do was process the images from the cameras and no accurately with that
[00:21:15 - 00:21:21] robot was in space without relying on GPS but you can see the functional architecture here he's got
[00:21:21 - 00:21:27] an Intel Knock which was a PC that was driving it he's got four wheel modules but each of those
[00:21:27 - 00:21:35] wheel modules have a DC servo and a DC motor and then a speed controller the information you're
[00:21:35 - 00:21:47] about the connections between these so RS 2 through 2 TCP IP EH demo and so on there was a GPU
[00:21:47 - 00:21:52] that was processing the stereo camera data and other aspects right so that's a pretty basic
[00:21:52 - 00:21:57] functional architecture block diagram out of his thesis and then you can see physically how this
[00:21:57 - 00:22:07] systems were laid out so it was a four-wheel drive for a stereo robot so when you're thinking about
[00:22:07 - 00:22:12] your overcoat robot going back to what we talked about that all megatronic systems have
[00:22:12 - 00:22:19] communications they have seen seen the information processing power housing affecting we can
[00:22:19 - 00:22:26] start we can potentially use this template for starting to think about our architectures of our
[00:22:26 - 00:22:32] robots or anything that you're designing mostly because it's a good reminder and it helps to not
[00:22:32 - 00:22:44] forget our specs and to start to think about things and so this is based on one robot from well you
[00:22:44 - 00:22:53] can see because it's got a Dwino Miga SDKs you guys get teensies that prior to about 2021 2022
[00:22:53 - 00:22:58] you used to get a Miga SDK which are a gap loss compared to what you've got now or a bit processor
[00:22:59 - 00:23:05] running at 16 megahertz you've got a 32 bit processor running up to 600 megahertz that's a bit more
[00:23:05 - 00:23:12] powerful but you can see obviously there's was in a communications on this block
[00:23:16 - 00:23:21] Yeah yeah because that's one of the rules it can't be communicating you can't be secretly
[00:23:21 - 00:23:26] joysticking down down here because that defeats the purposes of autonomous robot
[00:23:28 - 00:23:32] I mean normally you could have it communicating something back you just couldn't have it controlling
[00:23:32 - 00:23:37] it but we don't really want that it's easier for us just to say no communications on the
[00:23:37 - 00:23:42] on the robot but obviously there's sensors there so there's proximity sensors there's limit switches
[00:23:43 - 00:23:52] there's infrared sensors there's processing in terms of the CPU there's power subsystem which is
[00:23:52 - 00:23:57] probably similar to what you I think you'll end up dating them but you've got an lithium-on battery and
[00:23:58 - 00:24:05] a safety module I would just note that safety module is there to prevent accidental
[00:24:05 - 00:24:13] things but we can't necessarily save you from yourself because I do record seeing a student
[00:24:13 - 00:24:17] a number of years ago I was playing with it here plugged in and he dropped a screw and it went down
[00:24:17 - 00:24:24] there and then he stuck a screwdriver down in between those modules to pick it up and shortened it
[00:24:24 - 00:24:31] and Julian's designed those so that they'll cope with like this current limit is on the output
[00:24:32 - 00:24:39] yeah it's not really designed for somebody shorting it within itself there's housings and there's
[00:24:39 - 00:24:47] effectings effecting as you know servos and drive motors and stuff like that and so you can see
[00:24:47 - 00:24:52] we've got these aspects and then we have to connect them into a system so Karen Williams just
[00:24:52 - 00:24:59] was a new robot cut project years ago and it was quite a nice reasonably good architecture
[00:25:00 - 00:25:05] sort of showing some of the details this is at a relatively low level right at the start you've got
[00:25:05 - 00:25:12] process a pickup mechanism like a motion but when you start diving down into the details
[00:25:13 - 00:25:18] which is a little bit easier to do for you because you get given a whole bunch of modules right
[00:25:18 - 00:25:22] and so you kind of know what you've got to choose from whereas if you're out in the wild doing
[00:25:22 - 00:25:30] this for a job I don't know you know you search if you search like in free range sensors on
[00:25:30 - 00:25:37] the GK you probably get 63,000 results and then you've got to choose one of them and so
[00:25:38 - 00:25:43] you may have got a limited ecosystem that you can choose from and you can start to put together
[00:25:43 - 00:26:04] these diagrams reasonably quickly okay so once we start thinking about the function or we've got
[00:26:04 - 00:26:11] these functional aspects of our robot right what do we want to think about when we're starting to
[00:26:11 - 00:26:21] go to the physical side of things what would you take into account yeah that's obviously well
[00:26:21 - 00:26:26] and as in this instance because if you're all in that was a draw we just weigh the robots to see
[00:26:26 - 00:26:35] who's as lightest and next one of the one of the tie breaker mechanisms yeah you might have symbol
[00:26:38 - 00:26:45] yeah there's a I guess at a higher level than that what might we start considering because we've got
[00:26:45 - 00:26:53] functions that we know our system has to implement how do we assign those to chunks of physical
[00:26:53 - 00:27:00] reality if you like modules how do we do that what do we want in these modules
[00:27:00 - 00:27:13] what do we want them to interact with other modules so okay here we're nice if they played well
[00:27:13 - 00:27:20] together so you're probably if I said to you is it good to have a modular design or is that a bad
[00:27:20 - 00:27:32] idea what do we think it's probably good right it makes sense but what does that mean so yeah on the
[00:27:32 - 00:27:38] outside it means I guess I'm still perspective it means that things can be reused like you might
[00:27:38 - 00:27:43] have a module here so you can just give another module and swap out that but I guess what else does
[00:27:43 - 00:27:55] that mean yeah so they start to be interchangeable see if you design your modules well you could say
[00:27:55 - 00:28:00] I've got module A and I don't know okay at Broco can replace it with module A that's easy right
[00:28:00 - 00:28:06] but let's say module B comes along and that's an upgrade and we'd like to swap that out and
[00:28:06 - 00:28:12] instead what would have to be what what else design what would have to be occurring in our
[00:28:12 - 00:28:21] design or how will that does that have to be so we can do that I guess so yeah this needs to be
[00:28:21 - 00:28:26] easy to get out but I guess from integrating it with the rest of our design what would have to
[00:28:26 - 00:28:37] have to make a mouse a regular yeah so on physical physical mounting would have to be so their
[00:28:37 - 00:28:45] interface would have to be consistent but what also let's say it's a laser range finder which you get
[00:28:45 - 00:28:50] for a rowco what would it have to be if you take out one this that's a short range one you
[00:28:50 - 00:28:57] put in a one range one and it's just assume it's got good consistent physical interfaces what else
[00:28:57 - 00:29:09] would have to be the same for this to be useful or easy yeah ideally you wouldn't want to change
[00:29:09 - 00:29:15] anything right and so you would want that the signal interface and hopefully the power interface
[00:29:15 - 00:29:22] to be consistent so that you can plug this one and take this one out like this one in and it just
[00:29:22 - 00:29:27] works with your software but you don't have to we have to make minimal changes you don't want
[00:29:27 - 00:29:36] to have to rewrite all of your code because this one sped out range from an SPI communications
[00:29:36 - 00:29:41] protocol and this one sped out and out on voltage because then you're going to have to change all
[00:29:41 - 00:29:46] your code to work between those and so this catch in this idea which I've got there's narrow
[00:29:46 - 00:29:55] interface so each module exposes only essential high level IOs or hiding the internal implementation
[00:29:56 - 00:30:01] and therefore you can have this modular replacement and so another example of that might be
[00:30:04 - 00:30:12] like a motor and motor controller a wide interface would be something like the motor system
[00:30:12 - 00:30:20] system itself exposes so is these things are visible to whatever is connecting to it you know the
[00:30:20 - 00:30:26] phase currents or the back ear mef and the whole sensor rules signals and things like that and then
[00:30:27 - 00:30:31] your controller has to deal with those it therefore has to know something about motor physics to
[00:30:31 - 00:30:37] drive this motor the way that you want it whereas a narrow interface if you've bought a motor
[00:30:37 - 00:30:48] in motor controller unit a narrow interface might just expose effectively just you know drive motor
[00:30:48 - 00:30:52] the speed like what you get with robocup effectively you control your drive motors using the servo
[00:30:52 - 00:30:58] library and so you've got values you you've got a value a thousand is full speed negative
[00:30:58 - 00:31:04] two thousand is full speed positive fifteen hundred is not moving in the middle and so
[00:31:05 - 00:31:09] you the particular drive motors that you've got you can plug those in and that will work you
[00:31:09 - 00:31:15] could change it out for another motor and it will also work that interfaces is smaller narrow
[00:31:15 - 00:31:22] the CPU doesn't have to know all of the details that's going on inside to control that
[00:31:22 - 00:31:27] and so that's something when you're thinking about modularity you want to make those interfaces
[00:31:27 - 00:31:33] narrow it also means not only like it also relates to you probably don't have a lot of wires right
[00:31:33 - 00:31:38] you probably don't need 25 wires going to that motor to control and bring in a narrow these signals
[00:31:38 - 00:31:47] that you might need to work with because you've got basically a computational element with the
[00:31:47 - 00:31:55] motor driver that deals with those internal implementations and all it exposes externally to you
[00:31:56 - 00:32:04] are the high level stuff that you can control. Does that make sense? So modularity is good
[00:32:05 - 00:32:14] subsystems with good modularity are a plus and so good modularity should encompass conceptually
[00:32:14 - 00:32:21] related concerns so a module should you know do basically one thing one conceptual thing
[00:32:22 - 00:32:27] turn for example if it's a motor you don't want it doing I don't know what you don't want this
[00:32:27 - 00:32:33] module that's got a motor driving out the side here and I don't know if three range since a here
[00:32:34 - 00:32:42] and I don't know a servo like a 180 degree servo there there many things in a separate little
[00:32:42 - 00:32:46] module and they're not necessarily conceptually related so it just makes it complicated it'll be
[00:32:46 - 00:33:04] hard to replace that and so then this narrow interface. Okay so sort of thinking about physical
[00:33:04 - 00:33:11] functional physical architecture this so we started with a high level right now we've got some
[00:33:11 - 00:33:17] imaging spacecraft a good place to start is to think of what are the inputs and the outputs so
[00:33:18 - 00:33:23] imaging spacecraft what does it have what are some inputs obviously visible light because it's
[00:33:23 - 00:33:31] doing some imaging maybe some commands from you know the mission control down on earth
[00:33:32 - 00:33:38] there's an input some external references so it can orient itself in a noisy position
[00:33:39 - 00:33:47] external so outputs are things like applied talk in an image packet right at a high level then
[00:33:49 - 00:33:55] once you know those and you can start to dive down and start to expand that functional architecture
[00:33:57 - 00:34:05] so we might have a module that receives commands, execute commands, census, attitude,
[00:34:05 - 00:34:13] modifies, attitude, so orientation, converts lights to bit stores images, transmit images right so
[00:34:13 - 00:34:19] at a high you know not as high level is just a big box of this imaging spacecraft but this is a higher
[00:34:19 - 00:34:27] level now how might we split this into physical architecture where would you what might we put
[00:34:28 - 00:34:42] like what sort of what things might we can't together and module so what's that a camera unit
[00:34:46 - 00:34:51] so would you have one camera like there's obviously visible light and attitude sensing the
[00:34:51 - 00:34:59] watch may also use a camera would you have those in a single module or would probably not why not
[00:35:01 - 00:35:03] so I don't mean to pick on yes just your answer and questions
[00:35:03 - 00:35:09] yeah because the camera won't come in the visible light cameras cannot even put it
[00:35:09 - 00:35:14] at a risk to the cameras that are used to the stars or whatever
[00:35:14 - 00:35:19] yeah exactly right that comes back to the conceptually related concerns so one that's looking at
[00:35:19 - 00:35:26] the stars to orient itself in space probably one that needs to be black and white and it potentially
[00:35:26 - 00:35:30] could be you know depending on what you're doing it could be lower resolution because it's looking at
[00:35:30 - 00:35:36] bright stars and the one that's imaging that's that's imaging earth needs to be high resolution
[00:35:36 - 00:35:41] maybe quite narrow angle for example so they you may not decide to make those the same camera
[00:35:43 - 00:35:49] because they are while they're both cameras they're doing quite different tasks what else
[00:35:49 - 00:35:53] might you want to give the could you consider lumping together as modules
[00:35:54 - 00:36:04] next to you come on yeah so you could like to receive an execute commands would you have a single
[00:36:04 - 00:36:09] module for that right so yeah because you could have just a receiver I mean one way of looking at
[00:36:09 - 00:36:15] this is you could go I could have a transceiver module one that receives commands and it transmits
[00:36:15 - 00:36:20] stuff back to earth because then you've got a radio transceiver or you could say look I'll receive
[00:36:20 - 00:36:26] and I will decode those commands and start to execute them on a module why might you do that
[00:36:26 - 00:36:37] rather than having a single transceiver sorry yeah so it might be one one aspect of it because
[00:36:37 - 00:36:48] you can do these things simultaneously yeah so yeah so that's true what else might be different
[00:36:48 - 00:36:54] what about bandwidth one sending high resolution photos to earth one's receiving probably quite
[00:36:54 - 00:36:59] low risk low bandwidth even instructions from earth so it might be different bandwidth different
[00:36:59 - 00:37:05] frequencies as well potentially depending again relating to that bandwidth and so these are the
[00:37:05 - 00:37:10] things you want to sort of think about like you know when you robocup at this level of abstraction
[00:37:10 - 00:37:17] you might want to start thinking about what do we assign of our functional architecture what do we
[00:37:17 - 00:37:24] assign to different physical modules right so you know do we put that receive commands and the
[00:37:24 - 00:37:30] transmit commands in a single module or do we separate those do we is a better to have receive
[00:37:30 - 00:37:35] commands and execute commands together in a single sort of receive and decode module do we have
[00:37:35 - 00:37:48] separate cameras for the sensing and the imaging that the system is doing so this I guess the key
[00:37:48 - 00:37:54] to this is there's no right or wrong way despite the fact of a cross and attack here because
[00:37:54 - 00:37:58] they're not saying it's right that's wrong it's just saying one's possibly better and one's
[00:37:58 - 00:38:02] possibly worse but it comes down to a particular situation I didn't give in you much information
[00:38:02 - 00:38:07] about this particular system right we don't know the resolutions and things like that but you might
[00:38:07 - 00:38:14] originally think you know I will put receive commands and transmit commands as a transceiver
[00:38:14 - 00:38:19] execute commands and store images that sounds like something a computer can do maybe that's just a
[00:38:19 - 00:38:27] a single onboard computer then the digital camera can do two aspects the sensing attitude
[00:38:28 - 00:38:35] but as we talked about those you know may have different requirements and so perhaps it's better to
[00:38:37 - 00:38:43] to modularize this or but the physical architecture of the system more like that on the right where
[00:38:43 - 00:38:49] you have a radio receiver with a command decoder you've basically got an earth sensor unit which
[00:38:49 - 00:38:56] looks at the stars and also looks at the magnetic field to orientate itself maybe we've got a
[00:38:56 - 00:39:01] digital camera unit which basically takes photos and stores them and then we've got a separate
[00:39:01 - 00:39:07] radio transmitter which squirts those back to earth right there's no right and wrong but
[00:39:07 - 00:39:14] these are decisions that you want to start to make for robocup but for jobs or roles that you're doing
[00:39:15 - 00:39:22] you know in your and your work experience or in your career do you want any thoughts or comments about
[00:39:22 - 00:39:33] that if you had to think about what you modularize even with say LFR and stuff last year
[00:39:34 - 00:39:46] or you just sort of make it just one big duty modular okay so allocation of hardware
[00:39:47 - 00:39:53] basically allocation too hardware so that physical function or into physical so a single function
[00:39:53 - 00:39:59] to a single physical component so that's you know if you've got a function single function
[00:39:59 - 00:40:03] that goes to a single physical component you don't have a single physical component that's doing
[00:40:03 - 00:40:11] everything you don't necessarily have one processor and then you've got raw sensors which have
[00:40:11 - 00:40:15] to then feed into that and then the processor has to kind of convert that sensor input
[00:40:15 - 00:40:20] into actually something meaningful each little sensor can have its own processor so it has a
[00:40:20 - 00:40:26] narrow interface in it just outputs you know range equals this sort of thing so it avoids one component
[00:40:26 - 00:40:31] doing several things you know obviously that on top of it's trying to drive the motors and whatever
[00:40:31 - 00:40:36] else there's no need to allocate all of a particular type of functionality to a single physical
[00:40:36 - 00:40:42] component so each module effectively can have its own microprocessor and you see this more and more
[00:40:43 - 00:40:51] you know you buy a range sensor module and it's got a processor on it which you know you can then
[00:40:51 - 00:40:56] write to the registers and you can adjust or even actually I am user a good option they'll have a
[00:40:56 - 00:41:03] system on there so you can have onboard sensor fusion and there's filtering and there's
[00:41:04 - 00:41:09] you know what is the range of accelerations that you can sense and all these sorts of things
[00:41:10 - 00:41:15] so it's not like you've just got a raw accelerometer then you've got a separate CPU or
[00:41:15 - 00:41:23] processor which has to deal with that you can have micros on each of these systems which allows
[00:41:23 - 00:41:31] narrow interfaces but it just you know it makes the modularity a bit easier and that last one
[00:41:31 - 00:41:36] is really important particularly when you're early prototyping obviously we give you stuff
[00:41:36 - 00:41:41] for robo-cups so that makes life a bit easier but you know when you're going to finally
[00:41:41 - 00:41:47] your projects next year it's a hell of a lot easier to use existing off the shelf components
[00:41:47 - 00:41:53] particularly at prototyping stage you know by development board and use that rather than trying
[00:41:53 - 00:42:06] to develop your own from scratch why yeah well some people love it and it's an interesting process
[00:42:06 - 00:42:10] actually my my PhD student is designing a board at the moment and you see that's quite therapeutic
[00:42:13 - 00:42:14] but what else?
[00:42:16 - 00:42:18] oh sorry yeah if it breaks
[00:42:20 - 00:42:24] you can replace it with the same thing but you can probably if you've designed it yourself
[00:42:24 - 00:42:29] you can probably you probably order a minimum of five anyway right jowl sees going to move five order
[00:42:29 - 00:42:31] when you order a PhD babe yeah
[00:42:31 - 00:42:50] yeah absolutely like when you develop one of these there are a lot you're going to do this next
[00:42:50 - 00:42:56] year in 461 you will develop an embedded system with a chip on it and all the other stuff again
[00:42:56 - 00:43:03] it's a relatively close ecosystem so it makes it easier for the teaching stuff to help you with it
[00:43:03 - 00:43:09] but it's very easy to make a mistake another PhD student of mine was doing some work using
[00:43:09 - 00:43:16] ESP32's recently designed a board with investing with those and in those four while they're a bit
[00:43:16 - 00:43:24] finicky and there's a couple of pens if you either have those pens driven high or low during the boot
[00:43:24 - 00:43:30] sequence it won't boot and you knew that but it's still inadvertently wired something up so that
[00:43:30 - 00:43:34] it was trying to like it was it was pulling a high salt wouldn't let it boot so it started
[00:43:34 - 00:43:38] working out it just never boot and then took a whole lot of debugging and it was something
[00:43:38 - 00:43:43] you knew to be aware of but it's easy you know when you've got a hell of a lot of connections going
[00:43:43 - 00:43:49] on to accidentally wire something the wrong way and so and ultimately these things can be
[00:43:49 - 00:43:53] fixed but it can slow you down so when you're especially when you're prototyping and you're trying to
[00:43:53 - 00:44:00] develop things as you said like the board will have that most of that will be done for you
[00:44:00 - 00:44:08] it may come with things that you would like later on like a lot of board development boards you
[00:44:08 - 00:44:12] know you might buy from SparkFun or something like that we'll come with a chip and a battery
[00:44:12 - 00:44:18] charger and a couple of LDO's on there which you can then use for all the stuff and so
[00:44:19 - 00:44:23] it's really handy to use off the shelf stuff the other thing is they're often manufactured
[00:44:23 - 00:44:31] on bulk so they'll be cheaper than you buying a single chip from the GK5 PC base in JLC and
[00:44:31 - 00:44:39] you know small things if you look at a tendency for example that's an INXP version of an
[00:44:39 - 00:44:46] Cortex M7 well A INXP won't sell you those chips and sell to OEMs so PJ actually gets those
[00:44:46 - 00:44:51] but it's $50 and you look at what's on that board you probably couldn't buy that stuff for 50
[00:44:51 - 00:44:57] bucks even if you had the time to spend developing that so it's a relatively low cost low risk
[00:44:57 - 00:45:04] quality develop stuff later on if you go into a serial production you might need to do it on
[00:45:04 - 00:45:09] itself or you might have some outside company doing that but it reduces your risk
[00:45:12 - 00:45:17] so that's largely about architecture attributes behaviors and components this is pretty
[00:45:17 - 00:45:22] basic like we've already talked about this you know what it is what it does and you need to start
[00:45:22 - 00:45:28] thinking about these a little bit early in your design as well and you can do some modeling
[00:45:28 - 00:45:34] using these around your design you can start doing preliminary sizing like with your robot cup
[00:45:35 - 00:45:40] robots you can start to think you know you've got some components you can kind of weigh them
[00:45:41 - 00:45:47] how much or and you know what the weights you have to pick up are does their servo from its
[00:45:47 - 00:45:55] attributes does it have the torque to pick up a kilo weight on the end of an arm does it you know
[00:45:55 - 00:46:01] if you're using a electro magnet it pack up what is the current draw of the electro magnet
[00:46:01 - 00:46:09] and how am I going to last or with the battery that you've got since the accuracy is
[00:46:09 - 00:46:16] in dependencies and so you can basically start to use analytical relationships make
[00:46:16 - 00:46:20] tinctive solutions so that's the other thing start designing it start having to go you'll
[00:46:20 - 00:46:24] design it in your circle will use this little servo that servo is not strong enough the f i have to use
[00:46:24 - 00:46:29] the bigger one which means i have to adjust the mount which means that i have to do this and
[00:46:29 - 00:46:36] start that sort of design process and you do that for each of those major elements and then
[00:46:36 - 00:46:42] this is just some examples of some static sort of early concept design calculations and models
[00:46:42 - 00:46:49] that were in the robot cup reports over previous years people starting to look at you know the
[00:46:49 - 00:46:56] accuracy of the range sensors what is the torque of their pick up system what is the current draw
[00:46:56 - 00:47:08] on the the electro magnets and do they pick up the weights if they're on the side also because quite
[00:47:08 - 00:47:14] a common one when you talk to students is they'll say we'll have basically forks and we'll just
[00:47:14 - 00:47:20] drive into the weight fast and then the weight will go and slide up the forks into the storage
[00:47:20 - 00:47:30] mechanism but you can test that like they're still weights and you know if using aluminium forks
[00:47:30 - 00:47:37] there's a bit of friction there and as it turns out you know they this group did testing they just
[00:47:37 - 00:47:42] had a couple of aluminium albins and what angle did they need those to be at before the weight
[00:47:42 - 00:47:48] would begin to slide and it was sort of 17 degrees so there's quite a lot of friction you have to
[00:47:48 - 00:47:55] overcome so that can when you're thinking about your designs doing some basic testing like this can
[00:47:55 - 00:48:02] allow you to come up with ideas that are feasible right so that's looking at the attributes
[00:48:02 - 00:48:08] and the behaviors of the system and you can start to do that fairly early on so system design
[00:48:08 - 00:48:13] is really the definition of the components and how they connect the architecture and it's a
[00:48:13 - 00:48:18] recursive application of subsystem design as a recursive application you know you're you're figuring out
[00:48:18 - 00:48:22] the architecture then you dive down into that and you spread out the architecture and you break
[00:48:22 - 00:48:27] that problem down the functional physical architecture relationships sort of consider modularity
[00:48:27 - 00:48:34] and the interfaces between your modules there's no right and wrong way to do it but there are
[00:48:34 - 00:48:40] probably better and worse ways and then you can start to do sort of preliminary estimates of
[00:48:40 - 00:48:48] subsystem behaviors and stuff like that cool oh that's good time to finish you know if any questions
[00:48:49 - 00:48:54] otherwise if you do want to add something come up on the way out
[00:49:07 - 00:49:13] you look at the
[00:50:07 - 00:50:09] I think that's the problem.
[00:50:09 - 00:50:11] I think that's the problem.
[00:50:11 - 00:50:13] This is all about the minute of a five-year interview.
[00:50:13 - 00:50:14] Yes, yes, yes.
[00:50:14 - 00:50:16] I think it's the problem.
[00:50:16 - 00:50:17] It's the problem.
[00:50:17 - 00:50:19] It's the problem.
[00:50:19 - 00:50:23] But yeah, because we actually like to make this,
[00:50:23 - 00:50:25] I think that's the problem.
[00:50:25 - 00:50:28] I have to find a convention that I have to read.
[00:50:28 - 00:50:29] I have to read.
[00:50:29 - 00:50:30] No, it's the problem.
[00:50:30 - 00:50:31] No, it's the problem.
[00:50:31 - 00:50:33] That, no, it's my problem.
[00:50:33 - 00:50:34] Why?
[00:50:34 - 00:50:35] Why?
[00:50:35 - 00:50:55] Why does it look like a
[00:50:55 - 00:50:56] person?
[00:50:56 - 00:50:57] Why do you see the problem?
[00:50:57 - 00:50:58] Yeah.
[00:50:58 - 00:50:59] Because you basically run a current through the coils and then you switch it off and then it tries to...
[00:50:59 - 00:51:01] It'll make seven hundred volts.
[00:51:01 - 00:51:06] I guess how that's in it and you make the spike plugs in your car, go as you're a coil,
[00:51:06 - 00:51:09] which you break and you make a break and that's exactly what you're doing.
[00:51:09 - 00:51:15] Yeah, because it's funny, we were like, two standard works and then we turned it off and then we turned it on again.
[00:51:15 - 00:51:19] It was like, that's like, I said, you can tell that's probably why it broke.
[00:51:19 - 00:51:25] Yeah. But kind of crazy that, like, even off the shelf stuff, sometimes you would speak that the quality would be good.
[00:51:25 - 00:51:28] But it's a very recent story that we've exactly did.
[00:51:28 - 00:51:37] Another, oh, I hear said PXD students actually were, they were using, it was a little current driver from INXB for driving LEDs.
[00:51:37 - 00:51:44] And so it works on the downstream end of that and you've just, like, it's expecting the current control.
[00:51:44 - 00:51:49] And when you're talking to it through SPI, two other students have used it.
[00:51:49 - 00:51:53] In other words, second on the C3D SPI bus because of drawing computer to work.
[00:51:53 - 00:51:56] So she's definitely a super bus works fine.
[00:51:56 - 00:52:02] But if you're stepping on the same bus with something else, but it turns out the MISO line was just pulling it like,
[00:52:02 - 00:52:07] like, it was constant just driving it like, and when you eventually dig through all the forums and that, get up.
[00:52:07 - 00:52:14] And there's a thing I'm here that says that MISO stays low and you dip away if it's on that line, it won't nothing in community.
[00:52:14 - 00:52:19] And so, I mean, that's something that they're shipping commercially and it's the board stuff.
[00:52:19 - 00:52:20] Yeah.
[00:52:20 - 00:52:25] Yeah, absolutely. They are off the shelf stuff can be useful.
[00:52:25 - 00:52:28] Yes. Sometimes you run to the shoes.
[00:52:28 - 00:52:31] Yeah. And also we suspected as well, they were sending it to us with like,
[00:52:31 - 00:52:33] faulty components because we broke like three of the boards.
[00:52:33 - 00:52:36] One of the buffers just kept like just breaking randomly.
[00:52:36 - 00:52:41] It might have been the flight I've died as well though, but yeah, it was a part boost.
[00:52:41 - 00:52:45] And I don't know. I kind of, yeah, I don't know. I think the board was a little bit.
[00:52:45 - 00:52:51] But that's that the, it comes down to, I suppose, one of, it comes down to, you know, you hit
[00:52:51 - 00:52:55] in what message that you guys speak from the right of country and gets out of express.
[00:52:55 - 00:53:01] Oh, that's a, that's the one that's on the right of the board.

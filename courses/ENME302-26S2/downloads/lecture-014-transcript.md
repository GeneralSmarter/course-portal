# ENME302-26S2 Lecture 14 native Echo transcript

Date: August 5, 2026 11:00am-11:55am
Transcript type: native Echo automated transcript.

[00:00:09:569 - 00:00:09:579] **Speaker 0:** I.
[00:00:16:120 - 00:00:21:520] **Speaker 0:** Because Yeah you.
[00:00:42:360 - 00:00:51:490] **Speaker 0:** Yeah like.
[00:00:58:790 - 00:00:58:799] **Speaker 0:** No.
[00:01:04:480 - 00:01:07:680] **Speaker 0:** I Yeah.
[00:01:30:970 - 00:01:41:639] **Speaker 0:** I I Well, Karakoto, welcome along, everyone.
[00:01:44:459 - 00:01:45:279] **Speaker 0:** Just get underway.
[00:01:48:180 - 00:01:49:529] **Speaker 1:** So there's a few things we want to cover today.
[00:01:51:370 - 00:01:54:389] **Speaker 1:** Um, what we did on Monday was we looked at
[00:01:54:389 - 00:01:55:349] **Speaker 1:** distributed loading.
[00:01:56:160 - 00:02:00:580] **Speaker 1:** And ways of taking the distributed loads and introducing them
[00:02:00:639 - 00:02:01:839] **Speaker 1:** as equivalent nodal loads.
[00:02:02:620 - 00:02:04:949] **Speaker 1:** And that's based upon uh no loads being a way
[00:02:04:949 - 00:02:07:040] **Speaker 1:** in which we have always been able to introduce loads,
[00:02:07:500 - 00:02:10:860] **Speaker 1:** um, that already meets our assumptions, so we're just doing
[00:02:10:860 - 00:02:13:380] **Speaker 1:** that sort of transformation in a way of representing distributed
[00:02:13:380 - 00:02:17:080] **Speaker 1:** loads in terms of those um specific locations.
[00:02:18:270 - 00:02:19:949] **Speaker 1:** So we're gonna continue to work through the example we
[00:02:19:949 - 00:02:22:139] **Speaker 1:** started on Monday, um, we're also gonna work through some
[00:02:22:139 - 00:02:25:039] **Speaker 1:** examples to try and give you confidence that actually the,
[00:02:25:110 - 00:02:27:910] **Speaker 1:** the equations we've derived actually give the answers that you
[00:02:27:910 - 00:02:30:580] **Speaker 1:** would expect, so we're gonna work through, uh, a few
[00:02:30:580 - 00:02:33:990] **Speaker 1:** baseline cases where we have kind of known values that
[00:02:33:990 - 00:02:36:589] **Speaker 1:** we would expect to have and that we can actually
[00:02:36:589 - 00:02:37:770] **Speaker 1:** calculate those values.
[00:02:39:000 - 00:02:41:449] **Speaker 1:** Uh, and then we're gonna look at, um, probably not
[00:02:41:449 - 00:02:43:210] **Speaker 1:** today, but, um, we're just gonna look at the concept
[00:02:43:210 - 00:02:44:869] **Speaker 1:** of lost loads and a few other things.
[00:02:45:050 - 00:02:46:669] **Speaker 1:** So before we get into that, I just want to
[00:02:46:669 - 00:02:47:669] **Speaker 1:** talk a little bit about the test.
[00:02:48:000 - 00:02:52:289] **Speaker 1:** So the test is on, um, it's the Tuesday, the
[00:02:52:289 - 00:02:55:160] **Speaker 1:** week after next, I believe that's the 18th of, uh,
[00:02:55:169 - 00:02:55:610] **Speaker 1:** August.
[00:02:55:770 - 00:02:57:990] **Speaker 1:** It's in an evening from 6:30 to 8:30.
[00:02:59:610 - 00:03:02:110] **Speaker 1:** So, um, I had hoped to have all the details
[00:03:02:110 - 00:03:04:889] **Speaker 1:** for you, um, but there's been a, um, the digital
[00:03:04:889 - 00:03:06:610] **Speaker 1:** team's still sort of building the virtual environment for the
[00:03:06:610 - 00:03:10:669] **Speaker 1:** test to be, um, to be conducted in, so, um,
[00:03:10:679 - 00:03:12:289] **Speaker 1:** there will be still a few details that I need
[00:03:12:289 - 00:03:15:169] **Speaker 1:** to get to you next week, um, but the key
[00:03:15:169 - 00:03:16:490] **Speaker 1:** idea is that you'll actually be sitting this under a
[00:03:16:490 - 00:03:19:289] **Speaker 1:** virtual environment, so there'll be no, uh, you have access
[00:03:19:289 - 00:03:21:899] **Speaker 1:** to the Python IDE, so, uh, there is the intention
[00:03:21:899 - 00:03:24:789] **Speaker 1:** you'd have access to Wing, Um, and the Anaconda suite
[00:03:24:789 - 00:03:27:869] **Speaker 1:** which include Py and Spider and Jupiter notebooks, um, at
[00:03:27:869 - 00:03:30:059] **Speaker 1:** this stage it's not clear whether VS code would, would,
[00:03:30:070 - 00:03:32:070] **Speaker 1:** can be incorporated into that or not.
[00:03:32:270 - 00:03:34:830] **Speaker 1:** Um, I'll have a definitive answer on that for next
[00:03:34:830 - 00:03:37:509] **Speaker 1:** week, um, and I am trying to give you, see
[00:03:37:509 - 00:03:40:029] **Speaker 1:** if we can set up just a, a practise environment
[00:03:40:029 - 00:03:41:630] **Speaker 1:** which you can check in on that.
[00:03:41:820 - 00:03:43:869] **Speaker 1:** Um, the key thing is you'll be able to access
[00:03:43:869 - 00:03:45:669] **Speaker 1:** your OneDrive, so you'll be able to access code.
[00:03:45:830 - 00:03:47:750] **Speaker 1:** Um, I would strongly encourage you to bring in the
[00:03:47:750 - 00:03:50:490] **Speaker 1:** code as a USB as a backup just in case
[00:03:50:490 - 00:03:51:250] **Speaker 1:** anything else goes wrong.
[00:03:51:970 - 00:03:54:070] **Speaker 1:** And um if there's any network issues on the day,
[00:03:54:369 - 00:03:57:210] **Speaker 1:** um, and the key idea is that you bring the
[00:03:57:210 - 00:03:59:320] **Speaker 1:** code that you've developed over those, those, these 4 or
[00:03:59:320 - 00:04:02:570] **Speaker 1:** 5 weeks, um, that you've developed that code, you've got
[00:04:02:570 - 00:04:05:809] **Speaker 1:** familiar with that code, you're confident that across the range
[00:04:05:809 - 00:04:08:529] **Speaker 1:** of examples we've provided for you, that it's producing the
[00:04:08:529 - 00:04:10:770] **Speaker 1:** right answers, and then you just bring that code along
[00:04:10:770 - 00:04:11:550] **Speaker 1:** with you on the night.
[00:04:12:130 - 00:04:14:410] **Speaker 1:** Ah, it's not primarily a coding test, so you shouldn't
[00:04:14:410 - 00:04:17:630] **Speaker 1:** be making any substantive changes to your coding code during
[00:04:17:630 - 00:04:20:209] **Speaker 1:** the test, you should, essentially the idea is that you
[00:04:20:209 - 00:04:21:350] **Speaker 1:** make those ahead of time.
[00:04:21:980 - 00:04:24:570] **Speaker 1:** And you're just changing sort of, you know, input variables,
[00:04:24:799 - 00:04:27:959] **Speaker 1:** um, assembly matrices, um, maybe a little bit of coding
[00:04:27:959 - 00:04:31:209] **Speaker 1:** around specific reaction loads, that type of thing, but the
[00:04:31:209 - 00:04:33:049] **Speaker 1:** actual level of coding you're doing on the night is
[00:04:33:049 - 00:04:33:970] **Speaker 1:** relatively minor.
[00:04:34:290 - 00:04:36:940] **Speaker 1:** Um, what I would say quite clearly is that the,
[00:04:37:089 - 00:04:39:570] **Speaker 1:** I've put up the, the last 4 years of tests,
[00:04:40:049 - 00:04:42:130] **Speaker 1:** um, so I've put up the blank script and the
[00:04:42:130 - 00:04:44:089] **Speaker 1:** model solutions for each of those years and I would
[00:04:44:089 - 00:04:47:329] **Speaker 1:** strongly encourage you to work through, um, the blank script
[00:04:47:329 - 00:04:47:790] **Speaker 1:** first.
[00:04:48:089 - 00:04:51:329] **Speaker 1:** So, Those scripts as they appear on the the the
[00:04:51:329 - 00:04:55:850] **Speaker 1:** ACO learn page, um, as, as they were given to
[00:04:55:850 - 00:04:56:890] **Speaker 1:** students in those years.
[00:04:57:250 - 00:04:59:890] **Speaker 1:** So, um, that's essentially a good chance for you to
[00:04:59:890 - 00:05:01:049] **Speaker 1:** do a dummy run of the test.
[00:05:01:299 - 00:05:03:209] **Speaker 1:** Now, it is very easy to look at someone else's
[00:05:03:209 - 00:05:04:730] **Speaker 1:** working and kind of follow it and think, yeah, that
[00:05:04:730 - 00:05:05:190] **Speaker 1:** makes sense.
[00:05:05:929 - 00:05:07:000] **Speaker 1:** But actually when you've got to come up with the
[00:05:07:000 - 00:05:09:170] **Speaker 1:** answers yourselves, that's a better test, so I would strongly
[00:05:09:170 - 00:05:11:119] **Speaker 1:** encourage you to actually do that kind of blind work
[00:05:11:119 - 00:05:13:670] **Speaker 1:** through, um and only refer to the model answers after
[00:05:14:049 - 00:05:15:309] **Speaker 1:** you've um worked through.
[00:05:16:029 - 00:05:18:190] **Speaker 1:** Now, and working through those, it may be that you
[00:05:18:190 - 00:05:22:890] **Speaker 1:** actually choose a different, um, numbering sequence for your global
[00:05:22:890 - 00:05:23:390] **Speaker 1:** degrees of freedom.
[00:05:23:470 - 00:05:26:769] **Speaker 1:** So your uh lowercase qs and uppercase Q's, you may
[00:05:27:230 - 00:05:28:470] **Speaker 1:** choose a different numbering sequence there.
[00:05:28:630 - 00:05:31:070] **Speaker 1:** Remember within an element we have no flexibility for the
[00:05:31:070 - 00:05:32:970] **Speaker 1:** numbering sequence, but on the structural level we do.
[00:05:33:809 - 00:05:36:850] **Speaker 1:** Um, if you do that, you should see that essentially
[00:05:36:850 - 00:05:39:410] **Speaker 1:** the, the model solutions that are provided is one possible
[00:05:39:410 - 00:05:41:410] **Speaker 1:** model solution, it's not the only possible one.
[00:05:41:769 - 00:05:43:850] **Speaker 1:** There are other, um, ways you could do that which
[00:05:43:850 - 00:05:45:890] **Speaker 1:** would still give the same numbers but in a different
[00:05:45:890 - 00:05:46:299] **Speaker 1:** order.
[00:05:46:649 - 00:05:49:450] **Speaker 1:** Uh, that would still, um, give, you know, it would
[00:05:49:450 - 00:05:50:269] **Speaker 1:** still be a correct answer.
[00:05:50:369 - 00:05:52:600] **Speaker 1:** So don't, if you chose a different numbering sequence but
[00:05:52:600 - 00:05:55:290] **Speaker 1:** you've got all the same answers in a different order
[00:05:55:290 - 00:05:56:489] **Speaker 1:** in your like SQ vector.
[00:05:57:410 - 00:05:59:010] **Speaker 1:** Uh, and then you've got all the same reaction loads,
[00:05:59:049 - 00:05:59:529] **Speaker 1:** etc.
[00:06:00:170 - 00:06:01:290] **Speaker 1:** Um, don't worry about that.
[00:06:01:570 - 00:06:03:769] **Speaker 1:** You wouldn't be, you wouldn't be marked down if you
[00:06:03:769 - 00:06:05:950] **Speaker 1:** did that, um, on the test itself.
[00:06:07:130 - 00:06:11:220] **Speaker 1:** So, um, if you have used any sort of, um,
[00:06:11:690 - 00:06:15:850] **Speaker 1:** generative AI assistance to write the code, um, I'm, I'm
[00:06:15:850 - 00:06:17:730] **Speaker 1:** fine with that in terms of as long as you
[00:06:17:730 - 00:06:20:470] **Speaker 1:** understand the code cause you won't have those tools available
[00:06:20:470 - 00:06:22:089] **Speaker 1:** to you on the night, so you need to know
[00:06:22:089 - 00:06:23:950] **Speaker 1:** and understand the code and be able to manipulate that.
[00:06:24:820 - 00:06:27:140] **Speaker 1:** Um, and the test, as you'll see when you look
[00:06:27:140 - 00:06:30:299] **Speaker 1:** at the previous years, the, the actual test is primarily
[00:06:30:299 - 00:06:36:519] **Speaker 1:** a written submission, um, The, so you'll be um like
[00:06:36:519 - 00:06:38:399] **Speaker 1:** you can see on the learn page, um, so you'll
[00:06:38:399 - 00:06:40:959] **Speaker 1:** be in a vigilated room, um we'll be collecting a
[00:06:40:959 - 00:06:43:350] **Speaker 1:** physical test script at the end and that's because we're
[00:06:43:350 - 00:06:46:390] **Speaker 1:** looking more about your interpretation and your ability to sketch
[00:06:46:390 - 00:06:48:480] **Speaker 1:** affected shapes and work out reaction loads and things.
[00:06:48:959 - 00:06:51:269] **Speaker 1:** But on top of that there'll be an additional, um,
[00:06:51:279 - 00:06:53:989] **Speaker 1:** upload of your code, so you'll be uploading that through
[00:06:53:989 - 00:06:54:799] **Speaker 1:** a portal on learn.
[00:06:55:920 - 00:06:59:429] **Speaker 1:** And That code is really just as a a secondary
[00:06:59:429 - 00:06:59:790] **Speaker 1:** backup.
[00:06:59:869 - 00:07:02:970] **Speaker 1:** Like if you, if your answers are um are correct,
[00:07:03:320 - 00:07:06:350] **Speaker 1:** we probably won't look at your code, um, but if
[00:07:06:350 - 00:07:08:320] **Speaker 1:** there's a lot of issues with your code, um, the
[00:07:08:320 - 00:07:10:630] **Speaker 1:** ability for us to give you partial credit and follow
[00:07:10:630 - 00:07:13:470] **Speaker 1:** on errors through the problem is something that we can
[00:07:13:470 - 00:07:15:029] **Speaker 1:** do, um, when we have your code.
[00:07:15:109 - 00:07:18:089] **Speaker 1:** So it's much easier to to identify an issue and,
[00:07:18:100 - 00:07:20:950] **Speaker 1:** and run that through and see um whether subsequent wrong
[00:07:20:950 - 00:07:23:470] **Speaker 1:** answers are a new issue or a continuation of an
[00:07:23:470 - 00:07:24:369] **Speaker 1:** earlier one, so.
[00:07:25:350 - 00:07:28:950] **Speaker 1:** Um, the tests you might notice, um, if anyone's looked
[00:07:28:950 - 00:07:32:190] **Speaker 1:** at the previous tests, uh, the, the way that they're
[00:07:32:190 - 00:07:36:230] **Speaker 1:** written, um, in previous years is, uh, you'll see on
[00:07:36:230 - 00:07:38:100] **Speaker 1:** the the cover page that there's 90 minutes allowed for
[00:07:38:100 - 00:07:38:380] **Speaker 1:** that.
[00:07:38:670 - 00:07:40:709] **Speaker 1:** Um, if anyone's got sort of eagle eye and we
[00:07:40:709 - 00:07:43:029] **Speaker 1:** look at the course information system, you'll see that the
[00:07:43:029 - 00:07:44:820] **Speaker 1:** test is actually scheduled for 2 hours this year.
[00:07:44:989 - 00:07:46:750] **Speaker 1:** So what we've done in the past is we've had
[00:07:46:750 - 00:07:49:109] **Speaker 1:** 90 minutes of actual test time and then had 5
[00:07:49:109 - 00:07:52:149] **Speaker 1:** to 10 minutes after that for uploading your code to
[00:07:52:149 - 00:07:53:100] **Speaker 1:** learn, um.
[00:07:53:549 - 00:07:56:109] **Speaker 1:** This time we have that 2 hour timetable block, but
[00:07:56:109 - 00:07:57:859] **Speaker 1:** the intention is you actually have 1 hour 50 to
[00:07:57:859 - 00:07:59:950] **Speaker 1:** do the test and then that extra 5 or 10
[00:07:59:950 - 00:08:01:869] **Speaker 1:** minutes after that to upload your code.
[00:08:01:950 - 00:08:04:910] **Speaker 1:** So essentially there's an extra 20 minutes um in the
[00:08:04:910 - 00:08:05:450] **Speaker 1:** test.
[00:08:06:109 - 00:08:09:190] **Speaker 1:** Now the test itself won't be substantially different in format
[00:08:09:190 - 00:08:11:089] **Speaker 1:** to last year's, there'll still be 2 questions.
[00:08:11:670 - 00:08:14:829] **Speaker 1:** Um, so it's not like where the extra time means
[00:08:14:829 - 00:08:16:750] **Speaker 1:** I'm gonna cram a bunch of extra content, it's gonna
[00:08:16:750 - 00:08:18:410] **Speaker 1:** be broadly similar to the previous years.
[00:08:19:160 - 00:08:20:459] **Speaker 1:** Uh, the reason for that is I think if everything
[00:08:20:459 - 00:08:22:089] **Speaker 1:** goes well, you've got plenty of time to finish the
[00:08:22:089 - 00:08:24:450] **Speaker 1:** test, but if your code, if you do start having
[00:08:24:450 - 00:08:26:640] **Speaker 1:** issues with code and things, there had been some negative
[00:08:26:640 - 00:08:28:570] **Speaker 1:** feedback about the time, the test being a little bit
[00:08:28:570 - 00:08:32:250] **Speaker 1:** time pressured, so that's why there's a greater time allocation
[00:08:32:250 - 00:08:32:690] **Speaker 1:** this year.
[00:08:32:929 - 00:08:36:859] **Speaker 1:** So just, if you're worried about that inconsistency, that's the,
[00:08:36:960 - 00:08:38:690] **Speaker 1:** the rationale behind it, so.
[00:08:39:400 - 00:08:43:479] **Speaker 1:** I have said that There'll be 2 problems just like
[00:08:43:479 - 00:08:46:309] **Speaker 1:** in previous years and each problem will have up to
[00:08:46:309 - 00:08:50:440] **Speaker 1:** 4 elements, so a good idea would be to come
[00:08:50:440 - 00:08:53:140] **Speaker 1:** in with code for 23 and 4 elements.
[00:08:54:080 - 00:08:57:239] **Speaker 1:** The, the test will will focus primarily on frame elements,
[00:08:57:280 - 00:08:59:020] **Speaker 1:** so we're not gonna go and give you like a
[00:08:59:200 - 00:09:01:799] **Speaker 1:** a a pin jointed bar element like we did earlier
[00:09:01:799 - 00:09:04:039] **Speaker 1:** in the course, it's gonna be sort of, you know,
[00:09:04:159 - 00:09:07:679] **Speaker 1:** look at frame, using frame elements to solve things, um.
[00:09:08:510 - 00:09:10:869] **Speaker 1:** And essentially what, you know, as I said, would be
[00:09:10:869 - 00:09:12:940] **Speaker 1:** really good is to come in with say skeleton code
[00:09:12:940 - 00:09:15:590] **Speaker 1:** for a 2-ement structure, skeleton code for a 3-element structure,
[00:09:15:700 - 00:09:17:369] **Speaker 1:** skeleton node for a 4-element structure.
[00:09:17:909 - 00:09:19:669] **Speaker 1:** You look at the test problem, right, this is 4
[00:09:19:669 - 00:09:22:090] **Speaker 1:** elements, I'm gonna use that code and then you've you've
[00:09:22:090 - 00:09:24:349] **Speaker 1:** that minimises the amount of change that you have to
[00:09:24:349 - 00:09:25:030] **Speaker 1:** do on the day.
[00:09:25:510 - 00:09:28:390] **Speaker 1:** So, um, one other thing that just we have seen
[00:09:28:390 - 00:09:30:070] **Speaker 1:** a couple of people do, it's pretty rare.
[00:09:30:590 - 00:09:32:590] **Speaker 1:** Um, it might also be good to have another folder
[00:09:32:590 - 00:09:34:190] **Speaker 1:** which is sort of a duplicate of that because in
[00:09:34:190 - 00:09:37:090] **Speaker 1:** very rare cases we do see people where they Accidentally
[00:09:37:090 - 00:09:38:450] **Speaker 1:** delete a bunch of their code and then they run
[00:09:38:450 - 00:09:40:369] **Speaker 1:** the programme and then it overwrites it and they can't
[00:09:40:369 - 00:09:43:070] **Speaker 1:** necessarily back that out, so, um, then they end up
[00:09:43:070 - 00:09:46:780] **Speaker 1:** hastily trying to um, Rewrite the code on the fly,
[00:09:46:869 - 00:09:48:950] **Speaker 1:** so maybe having your sort of primary set of code
[00:09:48:950 - 00:09:51:469] **Speaker 1:** and then just in a different folder, some backup code
[00:09:51:469 - 00:09:53:669] **Speaker 1:** there, um, so if the worst happens like that that
[00:09:53:669 - 00:09:55:710] **Speaker 1:** you do still have a, a rollback state that you
[00:09:55:710 - 00:09:57:109] **Speaker 1:** can go to, so.
[00:09:58:289 - 00:09:59:570] **Speaker 1:** Um, I will send out an email with a lot
[00:09:59:570 - 00:10:02:289] **Speaker 1:** of information as well, um, and I'll probably come back
[00:10:02:289 - 00:10:04:409] **Speaker 1:** when James is lecturing next week and just cover a
[00:10:04:409 - 00:10:07:409] **Speaker 1:** couple of final things, but, um, is there any pressing
[00:10:07:409 - 00:10:08:030] **Speaker 1:** questions on that?
[00:10:08:950 - 00:10:11:309] **Speaker 1:** Question here, uh, is it like closed book like can
[00:10:11:309 - 00:10:11:869] **Speaker 1:** we take this?
[00:10:12:599 - 00:10:14:609] **Speaker 1:** Uh, so you won't be able to take in the,
[00:10:14:669 - 00:10:15:450] **Speaker 1:** the course reader.
[00:10:15:640 - 00:10:18:479] **Speaker 1:** Um, you can comment your code, so you can explain
[00:10:18:479 - 00:10:21:719] **Speaker 1:** what variables are, and I think after 2.5 years now
[00:10:21:719 - 00:10:23:400] **Speaker 1:** of telling you to comment your code, it would be
[00:10:23:400 - 00:10:25:280] **Speaker 1:** quite hypocritical for me to turn around and say you
[00:10:25:280 - 00:10:25:630] **Speaker 1:** can't.
[00:10:26:119 - 00:10:28:679] **Speaker 1:** So putting, you know, if you wanted to, um, you
[00:10:28:679 - 00:10:30:510] **Speaker 1:** know, put comments in to explain what the variables are
[00:10:30:510 - 00:10:32:500] **Speaker 1:** and things, um, that's absolutely fine.
[00:10:32:760 - 00:10:34:669] **Speaker 1:** Um, the exception to that is if you are using
[00:10:34:669 - 00:10:37:159] **Speaker 1:** a Jupiter notebook, there is the potential to like say
[00:10:37:159 - 00:10:40:400] **Speaker 1:** screenshot a PDF and put things into the as images
[00:10:40:400 - 00:10:42:059] **Speaker 1:** into that, um, Jupiter notebook.
[00:10:42:489 - 00:10:44:809] **Speaker 1:** That's not permitted because that is essentially translating into an
[00:10:44:809 - 00:10:45:429] **Speaker 1:** open book.
[00:10:45:890 - 00:10:47:169] **Speaker 1:** Um, so you won't be allowed this, but you would
[00:10:47:169 - 00:10:50:130] **Speaker 1:** be allowed one side of a 4 with any specific
[00:10:50:130 - 00:10:54:130] **Speaker 1:** notes, um, as well as any, you know, text comments
[00:10:54:130 - 00:10:57:729] **Speaker 1:** but not any images that are incorporated into the code
[00:10:57:729 - 00:10:58:349] **Speaker 1:** as well.
[00:10:58:690 - 00:11:02:390] **Speaker 1:** Um, there's no limited to limit to the number of
[00:11:02:729 - 00:11:05:169] **Speaker 1:** um files that you can bring in, but they do
[00:11:05:169 - 00:11:07:890] **Speaker 1:** need to be just Python files, so there's no, um,
[00:11:08:849 - 00:11:11:289] **Speaker 1:** No, you know, vetted scripts or anything like that, so.
[00:11:13:979 - 00:11:15:679] **Speaker 1:** Um, any additional questions?
[00:11:20:210 - 00:11:22:500] **Speaker 1:** Um, we'll have this, uh, I just send out an
[00:11:22:500 - 00:11:24:219] **Speaker 1:** email last night just around the, the focus of the
[00:11:24:219 - 00:11:26:320] **Speaker 1:** lab tomorrow, which is working through equivalent loading.
[00:11:27:739 - 00:11:30:020] **Speaker 1:** In that context, just a reminder that we're not changing
[00:11:30:020 - 00:11:30:599] **Speaker 1:** the structure.
[00:11:31:510 - 00:11:33:299] **Speaker 1:** Equivalent loading all it is is the load side of
[00:11:33:299 - 00:11:36:570] **Speaker 1:** the equation, so everything we've done on the the stiffness
[00:11:36:789 - 00:11:38:840] **Speaker 1:** side of the equation is exactly as it was before
[00:11:39:070 - 00:11:40:950] **Speaker 1:** and we're just adding in additional loading terms.
[00:11:43:299 - 00:11:46:580] **Speaker 1:** So, um, I would just say, I'll follow up with
[00:11:46:580 - 00:11:49:679] **Speaker 1:** an email with a little bit information and I'll also,
[00:11:49:690 - 00:11:51:609] **Speaker 1:** um, Yeah.
[00:11:52:760 - 00:11:55:400] **Speaker 1:** Go through and and probably come back next week after
[00:11:55:400 - 00:11:57:679] **Speaker 1:** James has taken over just with any, any final details,
[00:11:57:760 - 00:12:00:099] **Speaker 1:** but I just wanted to convey that to you today.
[00:12:02:690 - 00:12:06:549] **Speaker 1:** Um, Yeah, I think I've covered everything I wanted to,
[00:12:06:669 - 00:12:06:969] **Speaker 1:** so.
[00:12:08:530 - 00:12:10:890] **Speaker 1:** What we did on Monday was we derived the equivalent
[00:12:10:890 - 00:12:13:609] **Speaker 1:** loading term, so this is taking a, a distributed loading
[00:12:13:609 - 00:12:15:250] **Speaker 1:** term that we have here.
[00:12:16:140 - 00:12:18:979] **Speaker 1:** And we're trying to put what are the, the sheer
[00:12:18:979 - 00:12:21:020] **Speaker 1:** forces and moments applied at the nodal points which would
[00:12:21:020 - 00:12:24:429] **Speaker 1:** induce the same deflected curve within the structure here.
[00:12:24:739 - 00:12:27:260] **Speaker 1:** So, If we very quickly just look at this and
[00:12:27:260 - 00:12:28:570] **Speaker 1:** say the total.
[00:12:34:150 - 00:12:36:090] **Speaker 1:** He accumulated share.
[00:12:38:020 - 00:12:40:479] **Speaker 1:** Will be equal to W bar times L.
[00:12:42:229 - 00:12:44:909] **Speaker 1:** So it doesn't probably come as a surprise given the
[00:12:44:909 - 00:12:48:510] **Speaker 1:** symmetry of this problem that you would expect WR L
[00:12:48:510 - 00:12:50:510] **Speaker 1:** over 2 on each end there.
[00:12:51:669 - 00:12:53:429] **Speaker 1:** And when we solve for that, that's exactly what we
[00:12:53:429 - 00:12:55:109] **Speaker 1:** get a W bar L over 2 and a W
[00:12:55:109 - 00:12:55:909] **Speaker 1:** bar L over 2.
[00:12:56:299 - 00:12:59:570] **Speaker 1:** So, just a reminder, the assumption is that the UDL
[00:12:59:570 - 00:13:01:270] **Speaker 1:** acts upwards in the positive Y direction.
[00:13:03:510 - 00:13:06:429] **Speaker 1:** And what we'd have to do to, if this was
[00:13:06:710 - 00:13:09:330] **Speaker 1:** actually the loading case, we would expect some sort of,
[00:13:09:789 - 00:13:12:070] **Speaker 1:** you know, draw exaggerated as always, um.
[00:13:12:820 - 00:13:14:429] **Speaker 1:** Some sort of curve shaped like this.
[00:13:17:960 - 00:13:22:359] **Speaker 1:** And while the sheer forces are quite obvious, um, There'd
[00:13:22:359 - 00:13:25:580] **Speaker 1:** need to be a positive counterclockwise moment here and a
[00:13:25:580 - 00:13:29:080] **Speaker 1:** negative clockwise moment here to induce this curved shape.
[00:13:29:849 - 00:13:34:609] **Speaker 1:** So thankfully, that's what our mathematical derivation gives us that.
[00:13:35:450 - 00:13:41:570] **Speaker 1:** You can imagine this is going to be a Of
[00:13:41:570 - 00:13:44:590] **Speaker 1:** course, drawn exaggerated in some sort of shape like this.
[00:13:45:549 - 00:13:46:849] **Speaker 1:** Once the loading is applied.
[00:13:54:940 - 00:13:56:830] **Speaker 1:** We also looked at linearly veering loads.
[00:13:58:020 - 00:13:59:510] **Speaker 1:** There were 2 types that we considered.
[00:14:01:020 - 00:14:04:020] **Speaker 1:** One was a linearly varying load which started with a
[00:14:04:020 - 00:14:06:359] **Speaker 1:** zero intensity at X equals L and a maximum of
[00:14:06:849 - 00:14:08:960] **Speaker 1:** X equals 0, a maximum of X equals L.
[00:14:15:869 - 00:14:17:049] **Speaker 1:** So this was the first case.
[00:14:19:190 - 00:14:21:590] **Speaker 1:** And then, so 0 at node 1 and maximum node
[00:14:21:590 - 00:14:22:010] **Speaker 1:** 2.
[00:14:23:000 - 00:14:26:200] **Speaker 1:** This is just the mirror of that, so the maximum
[00:14:26:200 - 00:14:28:159] **Speaker 1:** at node 1 and 0 at node 2.
[00:14:30:090 - 00:14:32:450] **Speaker 1:** Um, the reason I've provided both of those cases is
[00:14:32:450 - 00:14:34:010] **Speaker 1:** this is one of the very few times where the
[00:14:34:010 - 00:14:35:049] **Speaker 1:** element orientation matters.
[00:14:35:250 - 00:14:38:140] **Speaker 1:** So suppose you've got some sort of situation like this,
[00:14:38:409 - 00:14:41:309] **Speaker 1:** um, But if the peak intensity is at the bottom,
[00:14:41:890 - 00:14:46:640] **Speaker 1:** then, The, um, this is the orientation of the element,
[00:14:46:729 - 00:14:49:130] **Speaker 1:** whereas so you could, you could either model it this
[00:14:49:130 - 00:14:51:159] **Speaker 1:** way with the element going upwards or you can model
[00:14:51:159 - 00:14:54:270] **Speaker 1:** it this way with the element going downwards, uh, both
[00:14:54:270 - 00:14:58:840] **Speaker 1:** would be um appropriate, um, but you, whichever way the
[00:14:58:840 - 00:15:01:489] **Speaker 1:** force is acting, there'd be different directions in the two
[00:15:01:489 - 00:15:02:090] **Speaker 1:** cases.
[00:15:03:270 - 00:15:06:390] **Speaker 1:** So That's just the options that are available to you.
[00:15:08:090 - 00:15:10:809] **Speaker 1:** There we looked at a few other cases, um, and
[00:15:10:809 - 00:15:15:299] **Speaker 1:** then we transformed those into the uh frame elements combinations,
[00:15:15:330 - 00:15:19:210] **Speaker 1:** we looked at distributed axial loads, concentrated axial loads partway
[00:15:19:210 - 00:15:19:750] **Speaker 1:** along the element.
[00:15:21:289 - 00:15:25:169] **Speaker 1:** And then we ultimately started this problem here, which is
[00:15:25:169 - 00:15:26:349] **Speaker 1:** page 125.
[00:15:30:380 - 00:15:36:260] **Speaker 1:** So What we had here This was a concentrated load.
[00:15:40:659 - 00:15:47:419] **Speaker 1:** Representing A truck And this here was the bridge deck.
[00:15:48:909 - 00:15:49:590] **Speaker 1:** Self white.
[00:15:56:679 - 00:15:59:159] **Speaker 1:** So we've already solved this problem before with the absence
[00:15:59:159 - 00:16:02:400] **Speaker 1:** of those two loads, so with the 210 kilonewton loads
[00:16:02:400 - 00:16:05:000] **Speaker 1:** there but not the 50 kilonewton load here or the
[00:16:05:000 - 00:16:06:719] **Speaker 1:** distributed load acting along there.
[00:16:10:750 - 00:16:13:280] **Speaker 1:** Um, as I went through yesterday.
[00:16:13:979 - 00:16:14:969] **Speaker 1:** I'll start on, on Monday.
[00:16:15:729 - 00:16:18:130] **Speaker 1:** The next few pages are just a replication of some
[00:16:18:130 - 00:16:20:820] **Speaker 1:** of the information earlier because the structure itself hasn't changed,
[00:16:21:169 - 00:16:24:070] **Speaker 1:** so therefore none of the generation of the stiffness matrices
[00:16:24:070 - 00:16:25:609] **Speaker 1:** or the numbers within them change.
[00:16:25:969 - 00:16:27:830] **Speaker 1:** That's all exactly the same as it was before.
[00:16:29:539 - 00:16:32:450] **Speaker 1:** So we have This is all identical.
[00:16:34:440 - 00:16:37:419] **Speaker 1:** This is all identical, and where we got to here
[00:16:37:880 - 00:16:41:260] **Speaker 1:** was um the way of actually introducing those loads.
[00:16:44:010 - 00:16:46:369] **Speaker 1:** So we have the forcing vector, when we derive those
[00:16:46:369 - 00:16:48:770] **Speaker 1:** it was in local coordinates within an element.
[00:16:49:450 - 00:16:52:340] **Speaker 1:** We then need to transform them into the uppercase F.
[00:16:55:869 - 00:16:56:929] **Speaker 1:** So when we go here.
[00:17:00:669 - 00:17:08:790] **Speaker 1:** In this specific case, Alpha 4 element 2.
[00:17:10:010 - 00:17:11:400] **Speaker 1:** Is equal to 0 degrees.
[00:17:12:790 - 00:17:14:688] **Speaker 1:** So the transformation matrix.
[00:17:16:060 - 00:17:19:349] **Speaker 1:** For element 2 Happens to be a 6 by 6
[00:17:19:349 - 00:17:20:420] **Speaker 1:** identity matrix.
[00:17:21:218 - 00:17:23:859] **Speaker 1:** So when, when you have a zero degree element transformation,
[00:17:23:938 - 00:17:27:537] **Speaker 1:** that means that the element coordinates for the the local
[00:17:27:537 - 00:17:29:659] **Speaker 1:** coordinates of the element are the same as the global
[00:17:29:659 - 00:17:30:328] **Speaker 1:** coordinates.
[00:17:30:899 - 00:17:33:218] **Speaker 1:** So then it turns out that you're actually not scaling
[00:17:33:218 - 00:17:36:979] **Speaker 1:** anything or reassigning anything, your transformation matrix just reverts back
[00:17:36:979 - 00:17:38:338] **Speaker 1:** to being an identity matrix.
[00:17:41:869 - 00:17:52:900] **Speaker 1:** So Therefore, In this case, F equivalent to is also
[00:17:52:900 - 00:17:55:540] **Speaker 1:** equal to F uppercase equivalent to.
[00:17:56:729 - 00:17:58:300] **Speaker 1:** I might just actually add a UDL there.
[00:17:59:890 - 00:18:00:500] **Speaker 1:** UDL there.
[00:18:05:959 - 00:18:12:069] **Speaker 1:** However, This will not always be the case.
[00:18:18:060 - 00:18:20:219] **Speaker 1:** So the key reason I'm just highlighting that is this
[00:18:20:219 - 00:18:22:339] **Speaker 1:** vector and this vector are actually the same one, the
[00:18:22:339 - 00:18:25:900] **Speaker 1:** same numbers in the same locations, but in most cases
[00:18:25:900 - 00:18:27:750] **Speaker 1:** this and this will actually be different vectors.
[00:18:28:109 - 00:18:30:739] **Speaker 1:** So you do need to follow the standard process, even
[00:18:30:739 - 00:18:33:520] **Speaker 1:** though in this particular instance it didn't change anything.
[00:18:34:050 - 00:18:34:060] **Speaker 1:** Yeah.
[00:18:34:709 - 00:18:36:949] **Speaker 1:** You definitely want to stick to that sequence and follow
[00:18:36:949 - 00:18:39:469] **Speaker 1:** through those processes, um, because if you do, then it
[00:18:39:469 - 00:18:41:229] **Speaker 1:** will be general to any element orientation.
[00:18:44:810 - 00:18:58:699] **Speaker 1:** Um, here Likewise In this specific example, A 2.
[00:18:59:630 - 00:19:02:219] **Speaker 1:** Also happens to be a 6 by 6 identity matrix,
[00:19:02:510 - 00:19:04:790] **Speaker 1:** so Q equivalent.
[00:19:06:469 - 00:19:11:530] **Speaker 1:** UDL is equal to F equivalent UDL.
[00:19:14:219 - 00:19:20:020] **Speaker 1:** But again This is not general.
[00:19:26:069 - 00:19:27:479] **Speaker 1:** You could look at this and say well actually all
[00:19:27:479 - 00:19:29:760] **Speaker 1:** three of those uh vectors are the same, I could
[00:19:29:760 - 00:19:30:930] **Speaker 1:** use them interchangeably.
[00:19:31:280 - 00:19:34:239] **Speaker 1:** Well, in this case you could, but not not generally.
[00:19:36:880 - 00:19:39:380] **Speaker 1:** Um, another question is, you know, why is the element
[00:19:39:380 - 00:19:39:869] **Speaker 1:** 2 here?
[00:19:40:040 - 00:19:41:719] **Speaker 1:** Why is it, you know, we're looking at the equivalent
[00:19:41:719 - 00:19:44:560] **Speaker 1:** on 2, we're using this transformation matrix element 2 and
[00:19:44:560 - 00:19:46:880] **Speaker 1:** the assembly matrix element 2, why is it that element?
[00:19:47:400 - 00:19:49:369] **Speaker 1:** Well, very simply, that's the element to which the distributed
[00:19:49:369 - 00:19:51:040] **Speaker 1:** load is applied, so.
[00:19:52:040 - 00:19:54:380] **Speaker 1:** We go back to whatever number of seconds we've applied,
[00:19:54:959 - 00:20:00:829] **Speaker 1:** we look at the um, We look at the numbering
[00:20:00:829 - 00:20:04:130] **Speaker 1:** sequence, the particular element number to which that load is
[00:20:04:130 - 00:20:06:469] **Speaker 1:** applied, and we use the matrices which correspond to that
[00:20:06:469 - 00:20:06:859] **Speaker 1:** element.
[00:20:15:650 - 00:20:17:359] **Speaker 1:** So now we want to look at is the concentrated
[00:20:17:359 - 00:20:19:319] **Speaker 1:** point load, so we've already dealt with the UDL, we've
[00:20:19:319 - 00:20:21:219] **Speaker 1:** got all the way up to our uppercase Q.
[00:20:23:310 - 00:20:26:750] **Speaker 1:** So we have our lowercase f equivalent, so the subscript
[00:20:26:750 - 00:20:28:630] **Speaker 1:** PL refers to point load.
[00:20:30:150 - 00:20:32:520] **Speaker 1:** Uh, in this case, we have the intensity of W
[00:20:32:520 - 00:20:33:400] **Speaker 1:** bar of -50.
[00:20:33:479 - 00:20:35:800] **Speaker 1:** It's negative because it was in the negative Y direction
[00:20:35:800 - 00:20:36:739] **Speaker 1:** for that that element.
[00:20:37:599 - 00:20:41:160] **Speaker 1:** We get this vector again because of this transformation matrix
[00:20:41:160 - 00:20:44:160] **Speaker 1:** for element 2 happens to be identity matrix, the vector
[00:20:44:160 - 00:20:44:780] **Speaker 1:** doesn't change.
[00:20:46:339 - 00:20:49:229] **Speaker 1:** Then we have, uh, again, this transformation to Q.
[00:20:50:150 - 00:20:53:050] **Speaker 1:** And then the total cue that we're gonna use is
[00:20:53:790 - 00:20:54:750] **Speaker 1:** this, this one here.
[00:20:56:619 - 00:20:59:959] **Speaker 1:** So this first vector Is.
[00:21:01:050 - 00:21:01:550] **Speaker 1:** Q Odle?
[00:21:02:810 - 00:21:04:869] **Speaker 1:** So that is the directly applied.
[00:21:09:170 - 00:21:10:030] **Speaker 1:** Nodal lobes.
[00:21:14:199 - 00:21:27:430] **Speaker 0:** Then we have Que equivalent UDL Which is The lumped
[00:21:29:520 - 00:21:30:430] **Speaker 1:** Neal loads.
[00:21:36:079 - 00:21:42:750] **Speaker 1:** That represent The UDL, so that's the bridge deck, so
[00:21:42:750 - 00:21:43:109] **Speaker 1:** white.
[00:21:44:969 - 00:21:46:160] **Speaker 1:** Generally what we have here.
[00:21:47:589 - 00:21:49:130] **Speaker 1:** Is Q equivalent to PL.
[00:21:51:400 - 00:21:52:380] **Speaker 1:** The truck weight.
[00:21:56:310 - 00:21:58:530] **Speaker 1:** And this here is queue total.
[00:22:00:839 - 00:22:02:900] **Speaker 1:** Which is Oh.
[00:22:04:959 - 00:22:06:000] **Speaker 1:** Applied loads.
[00:22:10:069 - 00:22:14:209] **Speaker 1:** So everything we're doing here is on the loading side
[00:22:14:209 - 00:22:15:250] **Speaker 1:** of the equation.
[00:22:16:430 - 00:22:19:180] **Speaker 1:** The stiffness matrices and things haven't changed, they're the same
[00:22:19:180 - 00:22:21:630] **Speaker 1:** as they were when we before we introduced the nodal
[00:22:21:630 - 00:22:22:189] **Speaker 1:** modes.
[00:22:23:209 - 00:22:25:810] **Speaker 1:** And now instead of putting, when we first solved this
[00:22:25:810 - 00:22:27:810] **Speaker 1:** problem, we use this vector, now we're gonna use this
[00:22:27:810 - 00:22:28:150] **Speaker 1:** one.
[00:22:29:109 - 00:22:32:040] **Speaker 1:** And we'll get the corresponding um deflections.
[00:22:48:000 - 00:22:49:660] **Speaker 1:** We solve it the same way, we always have.
[00:22:53:989 - 00:22:57:869] **Speaker 1:** So We have a response which is neither symmetric nor
[00:22:57:869 - 00:22:59:689] **Speaker 1:** anti-symmetric, we'll look at that in more detail.
[00:23:00:869 - 00:23:02:449] **Speaker 1:** Then we have our forcing terms here.
[00:23:04:329 - 00:23:06:400] **Speaker 1:** If we were to go through and solve for deflections,
[00:23:06:819 - 00:23:08:369] **Speaker 1:** so we might say a D1.
[00:23:09:170 - 00:23:15:109] **Speaker 1:** For element one, which would be 0 millimetres, 0 millimetres.
[00:23:16:079 - 00:23:22:520] **Speaker 1:** 0 milliradians, and then we would end up with -1.2655.
[00:23:23:239 - 00:23:44:619] **Speaker 1:** millimetres -18.4615. millimetres And -17.35. 41 Milliadians Now, that looks
[00:23:44:619 - 00:23:46:300] **Speaker 1:** a little bit different, so we've got.
[00:23:47:550 - 00:23:50:189] **Speaker 1:** Uh, the, the order of these has changed and then
[00:23:50:189 - 00:23:53:989] **Speaker 1:** this one, has gone to the 3rd loca was the
[00:23:53:989 - 00:23:55:260] **Speaker 1:** 3rd location has gone to the 6th.
[00:23:56:640 - 00:23:59:199] **Speaker 1:** Well, let's quickly sketch the free body diagram.
[00:24:00:170 - 00:24:02:869] **Speaker 1:** For this element, so we have X for element.
[00:24:03:920 - 00:24:06:180] **Speaker 1:** And Y for the elements, so this is element 1.
[00:24:08:089 - 00:24:09:619] **Speaker 1:** We have D11.
[00:24:11:430 - 00:24:11:439] **Speaker 1:** D.
[00:24:12:449 - 00:24:13:619] **Speaker 1:** 21.
[00:24:14:510 - 00:24:16:150] **Speaker 1:** And D3 1.
[00:24:18:239 - 00:24:26:000] **Speaker 1:** The 41 The 51 And D61, so.
[00:24:26:819 - 00:24:30:060] **Speaker 1:** Yeah, following global X, so local X, Y, Z at
[00:24:30:060 - 00:24:32:979] **Speaker 1:** node 1, local X, local Y, local Z at node
[00:24:32:979 - 00:24:33:300] **Speaker 1:** 2.
[00:24:38:329 - 00:24:41:189] **Speaker 1:** The first thing we have here is that this stuff
[00:24:41:729 - 00:24:42:410] **Speaker 1:** comes down.
[00:24:43:630 - 00:24:44:819] **Speaker 1:** To the fixed support.
[00:24:47:869 - 00:24:49:839] **Speaker 1:** So, we expect those values to be 0.
[00:24:50:729 - 00:24:53:810] **Speaker 1:** It's fully clamped and fixed, so we expect 0 translation
[00:24:53:810 - 00:24:54:689] **Speaker 1:** and 0 rotation.
[00:24:56:020 - 00:24:58:689] **Speaker 1:** And then, uh, these are the amount by which the
[00:24:58:979 - 00:25:01:140] **Speaker 1:** upper end of that element has deflected.
[00:25:04:780 - 00:25:07:699] **Speaker 1:** Um, D2 is actually gonna be equal to the vector
[00:25:07:699 - 00:25:08:239] **Speaker 1:** above.
[00:25:09:189 - 00:25:11:069] **Speaker 1:** Uh, because of the fact that the assembly matrix is
[00:25:11:069 - 00:25:13:290] **Speaker 1:** an identity matrix, so we end up with.
[00:25:14:189 - 00:25:14:579] **Speaker 1:** Yeah.
[00:25:15:579 - 00:25:21:010] **Speaker 1:** Um, 18.4615.
[00:25:22:130 - 00:25:36:239] **Speaker 1:** millimetres, we end up with -1.2655. millimetres -17.3541. Milly radians
[00:25:37:989 - 00:25:39:910] **Speaker 1:** Then 17.
[00:25:40:709 - 00:25:42:550] **Speaker 1:** What is the 7087.
[00:25:43:939 - 00:25:52:560] **Speaker 1:** millimetres, -1.5845 millimetres and, 8.2407.
[00:25:53:699 - 00:25:55:329] **Speaker 1:** Nearly radians, so.
[00:25:56:589 - 00:25:59:239] **Speaker 1:** If we take that, that's being applied relative to the
[00:25:59:239 - 00:26:02:800] **Speaker 1:** free body diagram for that element, so X and Y.
[00:26:03:979 - 00:26:05:689] **Speaker 1:** 1, so this is element 2.
[00:26:06:640 - 00:26:07:880] **Speaker 1:** D1, element 2.
[00:26:09:199 - 00:26:10:560] **Speaker 1:** D2 for element 2.
[00:26:11:780 - 00:26:13:239] **Speaker 1:** And D3 for element 2.
[00:26:15:319 - 00:26:15:329] **Speaker 1:** Before.
[00:26:17:959 - 00:26:18:739] **Speaker 1:** D5.
[00:26:20:530 - 00:26:21:719] **Speaker 1:** And D6.
[00:26:24:290 - 00:26:26:089] **Speaker 1:** So if you look at axial deflections, we have an
[00:26:26:089 - 00:26:29:930] **Speaker 1:** 18.4615 and a 17.7087.
[00:26:30:050 - 00:26:33:089] **Speaker 1:** So what that means is because the the vertical columns
[00:26:33:089 - 00:26:34:589] **Speaker 1:** have actually deflected transverse.
[00:26:35:430 - 00:26:37:339] **Speaker 1:** This element has displaced in space.
[00:26:37:630 - 00:26:39:510] **Speaker 1:** The whole thing's shifted across due to the loads that
[00:26:39:510 - 00:26:40:109] **Speaker 1:** are applied to it.
[00:26:40:880 - 00:26:44:640] **Speaker 1:** But then in addition to that, there's also some strain.
[00:26:44:729 - 00:26:45:939] **Speaker 1:** So if these fellows were equal.
[00:26:47:489 - 00:26:49:930] **Speaker 1:** There would be, um, essentially it would have translated in
[00:26:49:930 - 00:26:51:810] **Speaker 1:** space, but neither stretched nor compressed axialally.
[00:26:52:859 - 00:26:54:719] **Speaker 1:** But in this case, both things have happened here.
[00:26:56:400 - 00:26:57:969] **Speaker 1:** So if we wanted to work out the axial normal
[00:26:57:969 - 00:26:58:510] **Speaker 1:** strain.
[00:27:07:319 - 00:27:08:819] **Speaker 1:** From axial loads only.
[00:27:12:729 - 00:27:15:410] **Speaker 1:** Bearing in mind there would also be additional normal strains
[00:27:15:410 - 00:27:15:989] **Speaker 1:** from bending.
[00:27:17:160 - 00:27:19:319] **Speaker 1:** So this would be um.
[00:27:20:439 - 00:27:24:050] **Speaker 1:** The strain for element two would be D4 for element
[00:27:24:050 - 00:27:28:170] **Speaker 1:** two minus D1 for element two divided by the length
[00:27:28:170 - 00:27:29:329] **Speaker 1:** of element two.
[00:27:31:599 - 00:27:36:109] **Speaker 1:** Um And of course noting that.
[00:27:37:670 - 00:27:39:270] **Speaker 1:** The super scripts.
[00:27:42:010 - 00:27:46:020] **Speaker 1:** Refer to The elements number.
[00:27:49:709 - 00:27:52:380] **Speaker 1:** So that's not L squared, it's the length of element
[00:27:52:380 - 00:27:52:810] **Speaker 1:** 2.
[00:27:59:130 - 00:28:01:069] **Speaker 1:** Now if we go through and solve for deflections.
[00:28:02:930 - 00:28:05:229] **Speaker 1:** What we end up with is.
[00:28:06:439 - 00:28:09:619] **Speaker 1:** Um, so with sulphur reaction loads, we can basically take
[00:28:09:619 - 00:28:11:920] **Speaker 1:** the forcing terms, so we've got these three forcing vectors
[00:28:11:920 - 00:28:13:099] **Speaker 1:** that are represented above.
[00:28:13:640 - 00:28:16:069] **Speaker 1:** We can put those into element freebo diagrams and then
[00:28:16:069 - 00:28:20:239] **Speaker 1:** just sum them up and we get the profile that
[00:28:20:239 - 00:28:22:780] **Speaker 1:** is given on the next page, page 131.
[00:28:23:859 - 00:28:27:219] **Speaker 1:** Which just shows the um the loads that were applied.
[00:28:32:660 - 00:28:36:619] **Speaker 1:** So There was the two directly applied nodal loads, 10
[00:28:36:619 - 00:28:37:489] **Speaker 1:** kilonewtons.
[00:28:38:069 - 00:28:42:790] **Speaker 1:** The 47.5, that represents the the downward shear loads that
[00:28:42:790 - 00:28:46:709] **Speaker 1:** represent both the bridge deck self-weight and the truck, and
[00:28:46:709 - 00:28:49:089] **Speaker 1:** then these are the two moments that are induced, uh,
[00:28:49:109 - 00:28:52:670] **Speaker 1:** that represent the bending loads that are induced from both
[00:28:52:670 - 00:28:54:430] **Speaker 1:** the, the bridge deck self-weight.
[00:28:55:180 - 00:28:59:939] **Speaker 1:** And the um truck, so these 210 kilometres are the
[00:28:59:939 - 00:29:02:339] **Speaker 1:** directly applied nodal loads, these 2 here and these 2
[00:29:02:339 - 00:29:05:140] **Speaker 1:** here, are the equivalent nodal loads, and then these are
[00:29:05:140 - 00:29:06:819] **Speaker 1:** the reactions that result from that.
[00:29:10:189 - 00:29:12:250] **Speaker 1:** Then what we can do is.
[00:29:13:489 - 00:29:15:810] **Speaker 1:** We can plot the response.
[00:29:17:760 - 00:29:19:359] **Speaker 1:** So what we're actually doing here is we're breaking out
[00:29:19:359 - 00:29:21:359] **Speaker 1:** the response, we're looking at how what the response was
[00:29:21:359 - 00:29:22:540] **Speaker 1:** to just the nodal loads.
[00:29:23:390 - 00:29:25:390] **Speaker 1:** Then we're looking at the response to just the equivalent
[00:29:25:390 - 00:29:28:930] **Speaker 1:** nodal loads, and then we're looking at the overall response.
[00:29:32:239 - 00:29:33:719] **Speaker 1:** So if you were sketching this by hand, if you
[00:29:33:719 - 00:29:35:239] **Speaker 1:** haven't got your plotting code, you want to just work
[00:29:35:239 - 00:29:35:859] **Speaker 1:** out this by hand.
[00:29:37:219 - 00:29:39:800] **Speaker 1:** What we can do is focus on the nodal points
[00:29:39:800 - 00:29:40:380] **Speaker 1:** to start with.
[00:29:40:619 - 00:29:43:010] **Speaker 1:** So, first of all, we know that these two nodal
[00:29:43:010 - 00:29:44:099] **Speaker 1:** points are fully fixed.
[00:29:44:339 - 00:29:47:300] **Speaker 1:** So we want zero translation and zero rotation there.
[00:29:47:400 - 00:29:50:880] **Speaker 1:** So it's important they start with zero slope and they're
[00:29:50:880 - 00:29:53:420] **Speaker 1:** aligned with the initial element and then gradually deviate from
[00:29:53:420 - 00:29:53:540] **Speaker 1:** that.
[00:29:53:660 - 00:29:55:869] **Speaker 1:** So if you are sketching this, don't have a lot
[00:29:55:869 - 00:30:00:060] **Speaker 1:** an element coming in like this, uh, because that would
[00:30:00:060 - 00:30:01:540] **Speaker 1:** require a rotation to exist there.
[00:30:01:660 - 00:30:04:339] **Speaker 1:** It's a fixed support that's not representative of the defective
[00:30:04:339 - 00:30:04:599] **Speaker 1:** behaviour.
[00:30:05:819 - 00:30:07:500] **Speaker 1:** Then what you have is the, you know that from
[00:30:07:500 - 00:30:11:420] **Speaker 1:** this information, the 1st 3 correspond to this note here.
[00:30:13:079 - 00:30:16:449] **Speaker 1:** So the first thing here is the difference between their
[00:30:17:160 - 00:30:17:800] **Speaker 1:** And yeah.
[00:30:19:650 - 00:30:20:420] **Speaker 1:** Is Q1.
[00:30:21:130 - 00:30:27:400] **Speaker 1:** Which is equal to 18 01 millimetres.
[00:30:29:380 - 00:30:32:109] **Speaker 1:** Now there's a very small, even drawn exaggerated, there's a
[00:30:32:109 - 00:30:35:069] **Speaker 1:** very small vertical deflection here, even in the exaggerated form,
[00:30:35:109 - 00:30:36:469] **Speaker 1:** it still can't be seen very clearly.
[00:30:37:550 - 00:30:42:849] **Speaker 1:** Then we have a Q2, which is a, Um, 0
[00:30:42:849 - 00:30:43:209] **Speaker 1:** point.
[00:30:45:400 - 00:30:46:680] **Speaker 1:** 160.
[00:30:47:979 - 00:30:51:500] **Speaker 1:** millimetres, um, so that's to the right, and if it's
[00:30:51:500 - 00:30:53:099] **Speaker 1:** not clear in the diagram, it does help to say
[00:30:53:099 - 00:30:53:459] **Speaker 1:** here.
[00:30:55:530 - 00:30:59:229] **Speaker 1:** Upwards, which is indicating that you know, because that's positive
[00:30:59:569 - 00:31:00:770] **Speaker 1:** that it was an upwards deflection.
[00:31:02:890 - 00:31:05:410] **Speaker 1:** Then what we can do is to define this rotation.
[00:31:07:150 - 00:31:09:229] **Speaker 1:** What that is, remember the, the two elements, the default
[00:31:09:229 - 00:31:11:750] **Speaker 1:** assumption we have frames that is that they're rigidly connected
[00:31:11:750 - 00:31:13:729] **Speaker 1:** to each other, so they they welded to one another,
[00:31:14:229 - 00:31:16:810] **Speaker 1:** therefore if they deflect, they translate.
[00:31:17:709 - 00:31:18:910] **Speaker 1:** And rotate together.
[00:31:19:300 - 00:31:22:910] **Speaker 1:** So what was an internal 90 degrees in here should
[00:31:22:910 - 00:31:24:310] **Speaker 1:** remain 90 degrees after bending.
[00:31:25:420 - 00:31:30:670] **Speaker 1:** And what we can have here is The third entry
[00:31:30:670 - 00:31:34:989] **Speaker 1:** there is the angle between the initial deflection and the
[00:31:34:989 - 00:31:35:670] **Speaker 1:** final defection.
[00:31:35:790 - 00:31:37:589] **Speaker 1:** So what we could do is we could draw a
[00:31:37:589 - 00:31:41:410] **Speaker 1:** line that's aligned with the initial orientation of element 2,
[00:31:41:589 - 00:31:44:349] **Speaker 1:** and then we can draw a line that's aligned with
[00:31:44:349 - 00:31:47:380] **Speaker 1:** the final orientation of element 2, which is sort of
[00:31:47:380 - 00:31:48:349] **Speaker 1:** extending out this way.
[00:31:50:680 - 00:31:52:760] **Speaker 1:** And we could say That there.
[00:31:54:530 - 00:31:55:300] **Speaker 1:** There's our Q2.
[00:31:57:290 - 00:32:01:300] **Speaker 1:** Which is 4.56.
[00:32:02:839 - 00:32:03:680] **Speaker 1:** Milly radians.
[00:32:07:229 - 00:32:07:459] **Speaker 1:** Sure.
[00:32:08:170 - 00:32:09:489] **Speaker 1:** Ah, yes, absolutely it is.
[00:32:09:680 - 00:32:09:829] **Speaker 1:** Sorry.
[00:32:10:680 - 00:32:11:280] **Speaker 1:** It's you 3.
[00:32:14:130 - 00:32:17:250] **Speaker 1:** Now, because the two elements rotate together, you could equally
[00:32:17:250 - 00:32:18:510] **Speaker 1:** label it off element one.
[00:32:19:250 - 00:32:21:209] **Speaker 1:** So element one was initially vertically, so we could draw
[00:32:21:209 - 00:32:25:449] **Speaker 1:** a line up here, parallel, get the initial orientation of
[00:32:25:449 - 00:32:27:969] **Speaker 1:** element one, and then we draw a line that essentially
[00:32:27:969 - 00:32:29:869] **Speaker 1:** extends off the deflected shape.
[00:32:31:069 - 00:32:35:449] **Speaker 1:** Of element one, and then, That there will also be
[00:32:35:449 - 00:32:39:010] **Speaker 1:** Q3, which will be 4.56.
[00:32:40:170 - 00:32:41:189] **Speaker 1:** Milli radians.
[00:32:41:810 - 00:32:44:689] **Speaker 1:** Now we're drawing magnitude because we've clearly shown that this
[00:32:44:689 - 00:32:47:729] **Speaker 1:** is actually a clockwise rotation, which is we're already taking
[00:32:47:729 - 00:32:51:410] **Speaker 1:** the negative into account here, so either of those two
[00:32:51:410 - 00:32:54:400] **Speaker 1:** orientations, so if you've got two elements coming into a
[00:32:54:400 - 00:32:58:239] **Speaker 1:** nodal point, you could either draw the, the rotation being
[00:32:58:239 - 00:33:01:619] **Speaker 1:** relative to the initial and final location of one element
[00:33:01:619 - 00:33:03:550] **Speaker 1:** or the initial and final location of the other.
[00:33:04:319 - 00:33:06:640] **Speaker 1:** And they will be, by definition, the same thing.
[00:33:07:510 - 00:33:10:430] **Speaker 1:** Provided we're using the frame element assumption.
[00:33:12:489 - 00:33:13:589] **Speaker 1:** We can do the same thing on the right hand
[00:33:13:589 - 00:33:13:949] **Speaker 1:** side.
[00:33:16:000 - 00:33:22:170] **Speaker 1:** Here Q4 Which is 18.
[00:33:23:439 - 00:33:26:739] **Speaker 1:** 0.1 millimetres, it's gone to the right.
[00:33:27:890 - 00:33:30:180] **Speaker 1:** Then we can sort of have this line relative to
[00:33:30:410 - 00:33:30:859] **Speaker 1:** this one.
[00:33:31:000 - 00:33:31:839] **Speaker 1:** Again, it's very small.
[00:33:33:040 - 00:33:35:260] **Speaker 1:** And this here is Q5.
[00:33:36:880 - 00:33:39:479] **Speaker 1:** Which is 0.1.
[00:33:40:819 - 00:33:42:800] **Speaker 1:** 60 millimetres.
[00:33:47:449 - 00:33:48:189] **Speaker 1:** Downwards.
[00:33:48:810 - 00:33:50:849] **Speaker 1:** So that's, if you are concerned in the test, you
[00:33:50:849 - 00:33:53:290] **Speaker 1:** know, it's not clear from your sketch, whether it's gone
[00:33:53:290 - 00:33:56:209] **Speaker 1:** upwards or downwards, just putting a, a statement there to
[00:33:56:209 - 00:33:57:449] **Speaker 1:** say it's gone to the right, it's gone to the
[00:33:57:449 - 00:34:00:589] **Speaker 1:** left, it's gone upwards, it's gone downwards, um, is a
[00:34:00:650 - 00:34:02:810] **Speaker 1:** nice way of very clearly conveying to us that you
[00:34:02:810 - 00:34:04:189] **Speaker 1:** know what's going on.
[00:34:06:060 - 00:34:08:219] **Speaker 1:** And then finally, you could either do.
[00:34:09:259 - 00:34:11:388] **Speaker 1:** Uh, this vertical line here is parallel to the initial
[00:34:11:388 - 00:34:12:729] **Speaker 1:** orientation of element 3.
[00:34:15:699 - 00:34:16:370] **Speaker 1:** Then you can draw a line which is essentially an
[00:34:16:370 - 00:34:18:790] **Speaker 1:** extension of the defective shape of element 3.
[00:34:20:269 - 00:34:21:489] **Speaker 1:** So therefore, sorry.
[00:34:22:269 - 00:34:24:089] **Speaker 1:** Yeah, the ambulance raises that there's Q6.
[00:34:25:060 - 00:34:27:560] **Speaker 1:** Which is 4.56.
[00:34:29:350 - 00:34:30:628] **Speaker 1:** Milly radians.
[00:34:34:779 - 00:34:37:107] **Speaker 1:** And if you didn't have the plotting code and you
[00:34:37:107 - 00:34:39:178] **Speaker 1:** want to draw this by hand, the key thing is
[00:34:39:178 - 00:34:40:688] **Speaker 1:** focusing around a nodal point.
[00:34:42:019 - 00:34:44:377] **Speaker 1:** And draw what you do know, so you know how
[00:34:44:377 - 00:34:46:418] **Speaker 1:** much the node's affected, you know if it's rotated clockwise
[00:34:46:418 - 00:34:47:739] **Speaker 1:** or counterclockwise.
[00:34:48:377 - 00:34:51:549] **Speaker 1:** So then if you have this information here, You would
[00:34:51:549 - 00:34:55:059] **Speaker 1:** then be able to infer the behaviour that occurs between
[00:34:55:059 - 00:34:55:269] **Speaker 1:** us.
[00:34:55:468 - 00:34:58:148] **Speaker 1:** So try and have a nice consistent curve, don't have
[00:34:58:148 - 00:35:01:089] **Speaker 1:** sudden, you know, kinks in the elements, unless something's failed
[00:35:01:089 - 00:35:02:698] **Speaker 1:** partway along the element, you're not gonna see a sudden
[00:35:02:698 - 00:35:03:519] **Speaker 1:** change in curvature.
[00:35:04:320 - 00:35:08:320] **Speaker 1:** And for this element here, because it's translated, um, this
[00:35:08:320 - 00:35:11:800] **Speaker 1:** node has rotated clockwise and this rotate has node has
[00:35:11:800 - 00:35:16:729] **Speaker 1:** rotated anticlockwise, you've essentially got sort of element ends looking
[00:35:16:729 - 00:35:17:379] **Speaker 1:** like this.
[00:35:18:439 - 00:35:21:879] **Speaker 1:** But there's no significant vertical offset between them, so to
[00:35:21:879 - 00:35:25:360] **Speaker 1:** connect those, that's how you would actually know that there's
[00:35:25:360 - 00:35:27:050] **Speaker 1:** a double curvature shape in here.
[00:35:27:280 - 00:35:29:669] **Speaker 1:** It's because of the fact that despite there only being
[00:35:29:669 - 00:35:33:199] **Speaker 1:** a very minor, um, vertical deflection of the two ends,
[00:35:33:439 - 00:35:36:479] **Speaker 1:** there's no, there's no way that a single curve could
[00:35:36:479 - 00:35:39:979] **Speaker 1:** provide, The linkage between those two elements.
[00:35:43:439 - 00:35:45:040] **Speaker 1:** So we actually have here in this first case is
[00:35:45:040 - 00:35:46:669] **Speaker 1:** this is what we call an anti-symmetric result.
[00:35:53:709 - 00:35:56:510] **Speaker 1:** So it's not symmetric, it's the opposite of symmetric.
[00:35:56:590 - 00:35:59:070] **Speaker 1:** So essentially instead of this being a mirror line, you're
[00:35:59:070 - 00:36:02:030] **Speaker 1:** essentially taking this result and kind of moving that across
[00:36:02:030 - 00:36:02:649] **Speaker 1:** to the right.
[00:36:04:540 - 00:36:06:270] **Speaker 1:** And then what we have here from the equivalent nodal
[00:36:06:270 - 00:36:12:360] **Speaker 1:** loads, As a Symmetric response.
[00:36:16:520 - 00:36:18:090] **Speaker 1:** And of course what we would do is we would
[00:36:18:090 - 00:36:18:840] **Speaker 1:** take these.
[00:36:19:929 - 00:36:20:449] **Speaker 1:** And.
[00:36:22:939 - 00:36:26:500] **Speaker 1:** Sketch or label On the diagram.
[00:36:29:310 - 00:36:30:879] **Speaker 1:** I'm not gonna work through that a second time just
[00:36:30:879 - 00:36:32:860] **Speaker 1:** because it's exactly the same process we did above.
[00:36:34:639 - 00:36:36:810] **Speaker 1:** And of course what we do here as well is.
[00:36:38:459 - 00:36:39:000] **Speaker 1:** Label.
[00:36:41:060 - 00:36:41:909] **Speaker 1:** On the diagram.
[00:36:46:060 - 00:36:47:850] **Speaker 1:** So we have an anti-Semmetric response.
[00:36:48:780 - 00:36:50:040] **Speaker 1:** We have a symmetric response.
[00:36:51:030 - 00:36:53:580] **Speaker 1:** And because we're adding, we're using the principle of linear
[00:36:53:580 - 00:36:56:379] **Speaker 1:** superposition, we're just adding those two things together.
[00:36:57:719 - 00:37:01:520] **Speaker 1:** And what we get here is a response.
[00:37:03:139 - 00:37:04:560] **Speaker 1:** And overall response.
[00:37:08:840 - 00:37:15:239] **Speaker 1:** That is Neither Symmetric.
[00:37:16:909 - 00:37:24:409] **Speaker 1:** Nor Anti-Semitric And the reason I'm just highlighting that is
[00:37:24:409 - 00:37:25:760] **Speaker 1:** it's really easy to look at this problem and go,
[00:37:25:810 - 00:37:28:370] **Speaker 1:** well, I know there's some symmetry in there, and there's
[00:37:28:370 - 00:37:30:570] **Speaker 1:** it kind of looks, maybe at a glance, like symme
[00:37:30:570 - 00:37:31:550] **Speaker 1:** like it's symmetric.
[00:37:32:010 - 00:37:34:629] **Speaker 1:** So why do I end up with this vector that's
[00:37:35:250 - 00:37:37:010] **Speaker 1:** completely non-symmetric?
[00:37:38:169 - 00:37:40:629] **Speaker 1:** That's when you break it out and you can consider
[00:37:40:629 - 00:37:42:530] **Speaker 1:** the contributions to the overall deflection.
[00:37:43:379 - 00:37:45:939] **Speaker 1:** That becomes a little bit clearer there.
[00:37:49:620 - 00:37:52:179] **Speaker 1:** So that's sort of one of the key examples that
[00:37:52:179 - 00:37:54:260] **Speaker 1:** we're gonna work through the, the lab this week is
[00:37:54:260 - 00:37:57:060] **Speaker 1:** not um as extensive and that question here.
[00:37:58:399 - 00:38:02:500] **Speaker 1:** What is anti-swim So, um, symmetric here is that if
[00:38:02:500 - 00:38:03:479] **Speaker 1:** we were to draw a line.
[00:38:04:679 - 00:38:05:530] **Speaker 1:** Basically through here.
[00:38:07:580 - 00:38:10:199] **Speaker 1:** At 2.25, then it's a mirror line.
[00:38:10:580 - 00:38:12:459] **Speaker 1:** Um, but in this case if we were to draw
[00:38:12:459 - 00:38:14:379] **Speaker 1:** a line because it's 4.5 metres across, so we'd draw
[00:38:14:379 - 00:38:16:800] **Speaker 1:** a line at 2.25 up through the structure.
[00:38:18:620 - 00:38:22:030] **Speaker 1:** Then Uh, it's kind of the opposite of symmetric, so
[00:38:22:350 - 00:38:24:689] **Speaker 1:** if this was a symmetric response, this would be inwards.
[00:38:25:909 - 00:38:27:719] **Speaker 1:** But it's actually bending outwards, so it's essentially saying that
[00:38:27:719 - 00:38:31:149] **Speaker 1:** we're taking this um response and we've kind of got
[00:38:31:149 - 00:38:33:520] **Speaker 1:** the opposite of symmetric, so.
[00:38:34:739 - 00:38:37:739] **Speaker 1:** That's, yeah Um, and then when you add the two
[00:38:37:739 - 00:38:40:739] **Speaker 1:** together, you get something that's neither symmetric nor anti-symmetric, and
[00:38:40:739 - 00:38:43:500] **Speaker 1:** you get this kind of, you know, weird curve shape
[00:38:43:500 - 00:38:43:739] **Speaker 1:** there.
[00:38:47:560 - 00:38:48:889] **Speaker 1:** Plotting functions.
[00:38:50:989 - 00:38:52:919] **Speaker 1:** Uh, in the test, I wouldn't expect you to break
[00:38:52:919 - 00:38:55:239] **Speaker 1:** out, um, individual components.
[00:38:55:280 - 00:38:57:080] **Speaker 1:** It would just be, you know, pulling the overall defective
[00:38:57:080 - 00:38:59:040] **Speaker 1:** shape for all those that exist in the structure.
[00:38:59:280 - 00:39:01:320] **Speaker 1:** So, uh, in this case, I'm just breaking it out
[00:39:01:320 - 00:39:04:520] **Speaker 1:** because I think it, it shows some interesting aspects, but
[00:39:04:800 - 00:39:06:379] **Speaker 1:** I wouldn't ask you that in a test.
[00:39:08:860 - 00:39:11:300] **Speaker 1:** Yeah, it would just be that one that you'd, um,
[00:39:11:379 - 00:39:12:979] **Speaker 1:** I mean it wouldn't be different plotting code, you'd just
[00:39:12:979 - 00:39:16:080] **Speaker 1:** be maybe given, given different input, uh, loads and then
[00:39:16:080 - 00:39:18:010] **Speaker 1:** it would your your plotting code would produce each of
[00:39:18:010 - 00:39:18:629] **Speaker 1:** those three.
[00:39:19:219 - 00:39:21:459] **Speaker 1:** So you'd maybe just be, you know, providing this as
[00:39:21:459 - 00:39:23:280] **Speaker 1:** Q, your plotting code should produce this.
[00:39:23:669 - 00:39:25:540] **Speaker 1:** If you provide this as Q, your plotting code should
[00:39:25:540 - 00:39:28:300] **Speaker 1:** produce this, and if you provide the overall total, your
[00:39:28:300 - 00:39:29:860] **Speaker 1:** plotting code should produce this.
[00:39:30:060 - 00:39:32:659] **Speaker 1:** But um, yeah, in the test, it would just be
[00:39:32:659 - 00:39:37:060] **Speaker 1:** the final um total deflected curve for all loads.
[00:39:40:550 - 00:39:42:860] **Speaker 1:** Now, it's important to me here, um, we've gone through
[00:39:42:860 - 00:39:45:989] **Speaker 1:** some mathematical derivations, and it's really important for me to
[00:39:45:989 - 00:39:48:110] **Speaker 1:** not just expect you to believe what I'm saying, it's
[00:39:48:110 - 00:39:52:070] **Speaker 1:** to say, is this, am I just talking garbage here?
[00:39:52:189 - 00:39:53:909] **Speaker 1:** Like, am I just making stuff up, or is, does
[00:39:53:909 - 00:39:56:530] **Speaker 1:** this actually match the values that you would expect?
[00:39:57:110 - 00:40:00:330] **Speaker 1:** So, it's important for me to prove to you that
[00:40:00:909 - 00:40:04:290] **Speaker 1:** the derivations we've done actually do make physical sense.
[00:40:06:389 - 00:40:08:540] **Speaker 1:** So what we're gonna do is work through a few
[00:40:08:540 - 00:40:09:159] **Speaker 1:** cases here.
[00:40:10:449 - 00:40:11:989] **Speaker 1:** It's a quick sanity check.
[00:40:13:530 - 00:40:15:879] **Speaker 1:** So we're going to look at a cantilever with a
[00:40:15:879 - 00:40:17:389] **Speaker 1:** uniformly distributed load on it.
[00:40:17:889 - 00:40:20:159] **Speaker 1:** So this is our equivalent load, this is what we
[00:40:20:159 - 00:40:21:729] **Speaker 1:** derived on Monday.
[00:40:23:209 - 00:40:25:489] **Speaker 1:** We have a shear load at each end and we
[00:40:25:489 - 00:40:26:679] **Speaker 1:** have a counterclockwise moment.
[00:40:26:760 - 00:40:31:090] **Speaker 1:** Of course this is drawn with X upwards and um
[00:40:31:090 - 00:40:34:010] **Speaker 1:** that's based upon a positive value of W bar.
[00:40:35:120 - 00:40:36:550] **Speaker 1:** If we had this loading case, I mean this is
[00:40:36:550 - 00:40:37:860] **Speaker 1:** the loading case that we can derive.
[00:40:38:280 - 00:40:40:219] **Speaker 1:** We, we can know what the results should be.
[00:40:41:709 - 00:40:43:429] **Speaker 1:** So we're gonna say we just have a cantilever beam,
[00:40:43:510 - 00:40:46:110] **Speaker 1:** it's fully fixed at the left-hand end, we've got 3
[00:40:46:110 - 00:40:49:070] **Speaker 1:** nodal deflections at the right-hand end and we have a
[00:40:49:070 - 00:40:50:020] **Speaker 1:** uniformly distributed load.
[00:40:50:070 - 00:40:52:270] **Speaker 1:** So we have no concentrated nodal loads, we just have
[00:40:52:270 - 00:40:54:149] **Speaker 1:** this distributed load, that's the only load that acts on
[00:40:54:149 - 00:40:54:350] **Speaker 1:** it.
[00:40:57:219 - 00:40:59:800] **Speaker 1:** So, uh, the tip deflection for that.
[00:41:00:540 - 00:41:04:500] **Speaker 1:** Is defined as W bar L on 4/80i and the
[00:41:04:500 - 00:41:07:949] **Speaker 1:** tip rotation is W bar L cubed over 60i.
[00:41:08:820 - 00:41:10:639] **Speaker 1:** Now, where did that come from?
[00:41:10:929 - 00:41:15:179] **Speaker 1:** Well, what you probably remember from Paul Docherty in 202
[00:41:15:179 - 00:41:17:040] **Speaker 1:** or any equivalent class that you did.
[00:41:18:290 - 00:41:20:750] **Speaker 1:** As you can start with the bending moment equation and
[00:41:20:750 - 00:41:22:610] **Speaker 1:** you can integrate and you can evaluate constants.
[00:41:24:010 - 00:41:28:260] **Speaker 1:** So if you, you could say, um, You know, do
[00:41:28:260 - 00:41:30:419] **Speaker 1:** a freebo diagram, you could do a cut here and
[00:41:30:419 - 00:41:33:020] **Speaker 1:** you could work some distance X to the cuts, and
[00:41:33:020 - 00:41:36:800] **Speaker 1:** you could, um, determine a moment equation and integrate that
[00:41:36:800 - 00:41:37:199] **Speaker 1:** twice.
[00:41:38:290 - 00:41:44:540] **Speaker 1:** But when it comes to a, Distributed load The much
[00:41:44:540 - 00:41:47:340] **Speaker 1:** easier way to do that is to actually start with
[00:41:47:340 - 00:41:48:340] **Speaker 1:** the 4th derivative.
[00:41:48:419 - 00:41:51:550] **Speaker 1:** So W bar is by definition equal to EI.
[00:41:52:719 - 00:41:55:889] **Speaker 1:** Times the 4th derivative of the with respect to X.
[00:41:57:219 - 00:41:59:939] **Speaker 1:** And that would be equal to W bar.
[00:42:02:129 - 00:42:04:679] **Speaker 1:** Share is equal to the 3rd derivative, so we integrate
[00:42:04:679 - 00:42:05:060] **Speaker 1:** that.
[00:42:07:189 - 00:42:09:300] **Speaker 1:** The item on the 3rd derivative of his share.
[00:42:10:060 - 00:42:14:340] **Speaker 1:** So that would be equal to W X plus A.
[00:42:15:699 - 00:42:17:560] **Speaker 1:** Moment is the 2nd derivative.
[00:42:18:350 - 00:42:19:709] **Speaker 1:** EI times the 2nd derivative.
[00:42:21:389 - 00:42:27:699] **Speaker 1:** Of transverse deflection So that's W bar X2 over 2.
[00:42:29:340 - 00:42:31:429] **Speaker 1:** Plus A X + B.
[00:42:33:110 - 00:42:35:600] **Speaker 1:** The slope, the view by the X.
[00:42:36:959 - 00:42:39:550] **Speaker 1:** Is equal to 1 over EI.
[00:42:40:840 - 00:42:43:439] **Speaker 1:** Time you then have to switch the EI out, and
[00:42:43:439 - 00:42:47:879] **Speaker 1:** you end up with W bar, X cubed over 6
[00:42:48:139 - 00:42:51:719] **Speaker 1:** plus A X 2/2.
[00:42:53:100 - 00:42:54:939] **Speaker 1:** Plus B X plus C.
[00:42:56:050 - 00:42:58:090] **Speaker 1:** And then we have VF X.
[00:42:59:169 - 00:43:00:389] **Speaker 1:** There's one upon the eye.
[00:43:01:989 - 00:43:04:649] **Speaker 1:** W bar x 4/24.
[00:43:06:090 - 00:43:08:189] **Speaker 1:** axe cubed over 6.
[00:43:09:860 - 00:43:11:199] **Speaker 1:** B X 202.
[00:43:13:239 - 00:43:14:699] **Speaker 1:** C X plus D.
[00:43:16:169 - 00:43:17:850] **Speaker 1:** Now, we would then have to go through and evaluate
[00:43:17:850 - 00:43:18:909] **Speaker 1:** all of those constants.
[00:43:20:939 - 00:43:24:070] **Speaker 1:** It is actually relatively easy in this case because we
[00:43:24:070 - 00:43:27:879] **Speaker 1:** know that um, V of X and DV by X,
[00:43:27:989 - 00:43:31:709] **Speaker 1:** the deflection and slope at X equals 0, are 0,
[00:43:31:790 - 00:43:33:189] **Speaker 1:** so that would straight away tell us that C and
[00:43:33:189 - 00:43:36:600] **Speaker 1:** D are equal to 0, But then what we actually
[00:43:36:600 - 00:43:39:250] **Speaker 1:** want to do here is working out that.
[00:43:39:969 - 00:43:42:969] **Speaker 1:** Um, V and M, uh, sheer force at the moment
[00:43:42:969 - 00:43:45:689] **Speaker 1:** are actually zero at the X equals L, but we
[00:43:45:689 - 00:43:47:610] **Speaker 1:** could work through that, evaluate the constants, and we would
[00:43:47:610 - 00:43:48:590] **Speaker 1:** get these equations.
[00:43:50:939 - 00:43:53:020] **Speaker 1:** Now, in case you don't trust me, here's a photograph,
[00:43:53:100 - 00:43:55:340] **Speaker 1:** a photocopy of a textbook.
[00:43:55:439 - 00:43:58:100] **Speaker 1:** So this is actually the Philpot text which was sort
[00:43:58:100 - 00:44:01:399] **Speaker 1:** of uh recommended or required reading for 202 last year.
[00:44:02:489 - 00:44:04:659] **Speaker 1:** And this is what we get here.
[00:44:04:739 - 00:44:09:500] **Speaker 1:** So this is the Tip rotation and tip deflection.
[00:44:10:520 - 00:44:13:530] **Speaker 1:** That you would expect for a tip-loaded cantilever, so.
[00:44:14:250 - 00:44:16:169] **Speaker 1:** Yeah, well we can derive these, giving you a little
[00:44:16:169 - 00:44:17:729] **Speaker 1:** bit of confidence that if you look at the textbook,
[00:44:17:770 - 00:44:20:159] **Speaker 1:** this is what it says those values should be.
[00:44:23:830 - 00:44:27:010] **Speaker 1:** So then if we go through And we, we solve
[00:44:27:010 - 00:44:27:429] **Speaker 1:** this.
[00:44:29:110 - 00:44:34:729] **Speaker 1:** We would set it up We would Um, we've got
[00:44:34:729 - 00:44:36:510] **Speaker 1:** our forcing vector here.
[00:44:37:979 - 00:44:40:899] **Speaker 1:** And we have our queue, so this is how we
[00:44:40:899 - 00:44:42:699] **Speaker 1:** would introduce the the loads.
[00:44:44:000 - 00:44:44:010] **Speaker 1:** Yes.
[00:44:47:870 - 00:44:49:820] **Speaker 1:** Yeah, there's one thing we'll cover in more detail tomorrow,
[00:44:49:939 - 00:44:52:419] **Speaker 1:** but maybe there's the first sign that maybe there's something
[00:44:52:419 - 00:44:54:379] **Speaker 1:** extra to look at here, so it won't affect our
[00:44:54:379 - 00:44:56:050] **Speaker 1:** solution, but something just to be aware of that we'll
[00:44:56:050 - 00:44:57:239] **Speaker 1:** come back and look in more detail.
[00:44:58:310 - 00:44:59:889] **Speaker 1:** Is this in this forcing vector.
[00:45:01:699 - 00:45:05:139] **Speaker 1:** There are 4 Non-zero values.
[00:45:06:449 - 00:45:08:209] **Speaker 1:** And when we use our assembly matrix and we get
[00:45:08:209 - 00:45:11:830] **Speaker 1:** our our overall equivalent forcing vector uppercase Q.
[00:45:13:080 - 00:45:14:620] **Speaker 1:** We only have 2.
[00:45:16:260 - 00:45:18:060] **Speaker 1:** Non-zero values, so.
[00:45:19:500 - 00:45:22:459] **Speaker 1:** That's maybe just a a teaser or a cliffhanger for
[00:45:22:459 - 00:45:23:010] **Speaker 1:** tomorrow's lecture.
[00:45:23:139 - 00:45:24:820] **Speaker 1:** We'll look at that in more detail and there is
[00:45:24:820 - 00:45:26:379] **Speaker 1:** actually an extra step that we need to look at
[00:45:26:379 - 00:45:28:659] **Speaker 1:** in there when we're looking at reaction loads, but we'll
[00:45:28:659 - 00:45:29:760] **Speaker 1:** just ignore that for now.
[00:45:31:199 - 00:45:34:870] **Speaker 1:** We put this in, um, we've got our um stiffness
[00:45:34:870 - 00:45:35:520] **Speaker 1:** matrix.
[00:45:36:510 - 00:45:38:129] **Speaker 1:** And those are the defections that we get.
[00:45:39:699 - 00:45:40:969] **Speaker 1:** And the next page there.
[00:45:42:620 - 00:45:53:679] **Speaker 1:** is if we were to Go through Set up a
[00:45:53:679 - 00:45:55:379] **Speaker 1:** finite element solution for this.
[00:45:56:229 - 00:45:57:909] **Speaker 1:** We work to get to all the vectors and then
[00:45:57:909 - 00:45:59:110] **Speaker 1:** these are the values that we would get.
[00:45:59:229 - 00:46:02:129] **Speaker 1:** So this is the, the values we would solve for
[00:46:02:679 - 00:46:04:459] **Speaker 1:** the horizontal axial deflection of the tip.
[00:46:05:260 - 00:46:09:100] **Speaker 1:** Which is unsurprisingly 0 because while there is the potential
[00:46:09:100 - 00:46:10:479] **Speaker 1:** for there to be non-zero loads there.
[00:46:11:199 - 00:46:14:149] **Speaker 1:** There was no horizontal force applied, so we sold for
[00:46:14:149 - 00:46:14:959] **Speaker 1:** a zero deflection.
[00:46:15:949 - 00:46:18:830] **Speaker 1:** And then we get these values here, applying the equations
[00:46:18:830 - 00:46:22:300] **Speaker 1:** that we derived or put into a textbook, and everything's
[00:46:22:300 - 00:46:23:350] **Speaker 1:** actually matching, so.
[00:46:24:050 - 00:46:29:090] **Speaker 1:** Hopefully that actually gives you some confidence that The mathematical
[00:46:29:090 - 00:46:30:169] **Speaker 1:** derivations we've done.
[00:46:30:870 - 00:46:34:729] **Speaker 1:** Actually do give an answer that is physically reasonable.
[00:46:38:159 - 00:46:41:199] **Speaker 1:** We'll also quickly just work through a distributed load along
[00:46:41:199 - 00:46:42:260] **Speaker 1:** the length of an element.
[00:46:47:800 - 00:46:51:360] **Speaker 1:** So We have an element here We've got a sort
[00:46:51:360 - 00:46:56:439] **Speaker 1:** of concentrated load here of, -10 kilonewtons.
[00:46:57:770 - 00:46:59:889] **Speaker 1:** This is what our assembly matrix would look like, because
[00:46:59:889 - 00:47:01:689] **Speaker 1:** this is the free body diagram for the elements, this
[00:47:01:689 - 00:47:04:530] **Speaker 1:** is the structural, so 45 and 6.
[00:47:05:360 - 00:47:07:879] **Speaker 1:** In the elements correspond to 12, and 3 globally, so
[00:47:07:879 - 00:47:09:689] **Speaker 1:** that's the assembly matrix we would derive.
[00:47:11:320 - 00:47:12:679] **Speaker 1:** Um, the tip deflection.
[00:47:14:689 - 00:47:16:889] **Speaker 1:** This one here is actually from Shigley and Mishki, which
[00:47:16:889 - 00:47:18:229] **Speaker 1:** is the design text.
[00:47:19:909 - 00:47:22:939] **Speaker 1:** So You look at this, this is essentially the loading
[00:47:22:939 - 00:47:25:659] **Speaker 1:** case that we have, and we end up with a
[00:47:25:659 - 00:47:27:280] **Speaker 1:** maximum tip deflection here.
[00:47:27:899 - 00:47:28:860] **Speaker 1:** So this is, you know.
[00:47:29:830 - 00:47:32:550] **Speaker 1:** The textbook tells us that the protection should be, so
[00:47:32:550 - 00:47:36:270] **Speaker 1:** that's what, We get there, um, we can go through,
[00:47:36:310 - 00:47:39:590] **Speaker 1:** we can substitute in the values for A, so it's
[00:47:39:590 - 00:47:44:149] **Speaker 1:** 1.25 metres long, a 3 metre long element, so we
[00:47:44:149 - 00:47:47:310] **Speaker 1:** put those values in, work through these are the forcing
[00:47:47:310 - 00:47:48:169] **Speaker 1:** terms that we get.
[00:47:49:270 - 00:47:51:379] **Speaker 1:** Again, what you'll see here is 4.
[00:47:53:790 - 00:47:58:840] **Speaker 1:** Non-zero values, But once we introduce our assembly matrix down
[00:47:58:840 - 00:48:00:580] **Speaker 1:** here, we actually only have 2.
[00:48:03:340 - 00:48:04:510] **Speaker 1:** Non-zero values.
[00:48:05:820 - 00:48:07:260] **Speaker 1:** And what that means is there's actually a little bit
[00:48:07:260 - 00:48:10:260] **Speaker 1:** of information that's lost from the system that only matters
[00:48:10:260 - 00:48:11:830] **Speaker 1:** when we have to look at reaction loads.
[00:48:12:100 - 00:48:13:780] **Speaker 1:** Uh, we'll cover that in a lot more detail tomorrow
[00:48:13:780 - 00:48:14:739] **Speaker 1:** as to how to deal with that.
[00:48:15:699 - 00:48:18:219] **Speaker 1:** And then what we get here is the same deflections
[00:48:18:219 - 00:48:22:860] **Speaker 1:** and 10.09 millimetres is the answer we get from our
[00:48:22:860 - 00:48:25:500] **Speaker 1:** final element solution, and this is the answer that we
[00:48:25:500 - 00:48:28:179] **Speaker 1:** would have got from the value from the textbooks.
[00:48:29:370 - 00:48:29:850] **Speaker 1:** So.
[00:48:31:760 - 00:48:33:550] **Speaker 1:** The key thing there is.
[00:48:34:350 - 00:48:34:360] **Speaker 1:** Maybe.
[00:48:36:550 - 00:48:41:699] **Speaker 1:** This one And.
[00:48:43:090 - 00:48:44:709] **Speaker 1:** The finite element analysis solution.
[00:48:49:850 - 00:48:50:610] **Speaker 1:** Matches.
[00:48:52:969 - 00:48:53:909] **Speaker 1:** What we would expect.
[00:48:58:560 - 00:49:01:520] **Speaker 1:** Now, you can obviously model much more complex situations that
[00:49:01:520 - 00:49:04:439] **Speaker 1:** may not be that easy to get, uh, an analytical
[00:49:04:439 - 00:49:04:659] **Speaker 1:** solution.
[00:49:05:479 - 00:49:06:939] **Speaker 1:** But all the information's there.
[00:49:07:659 - 00:49:12:489] **Speaker 1:** And you've got Yeah, this is your Yeah, I give
[00:49:12:489 - 00:49:14:479] **Speaker 1:** you a little bit of confidence that the the mathematical
[00:49:14:479 - 00:49:17:120] **Speaker 1:** derivations we did on Monday are actually meaningful.
[00:49:17:439 - 00:49:20:080] **Speaker 1:** They do actually capture the reaction mechanisms that we think
[00:49:20:080 - 00:49:22:719] **Speaker 1:** they do, and give you a little bit of confidence
[00:49:22:719 - 00:49:23:479] **Speaker 1:** in using this.
[00:49:23:919 - 00:49:26:679] **Speaker 1:** So, um, yeah, thank you all for coming along, and
[00:49:26:679 - 00:49:28:120] **Speaker 1:** I'll see you again tomorrow morning.
[00:50:04:280 - 00:50:04:290] **Speaker 0:** Yeah.
[00:50:10:219 - 00:50:10:229] **Speaker 0:** I.
[00:50:13:080 - 00:50:13:090] **Speaker 0:** I.
[00:50:16:489 - 00:50:21:929] **Speaker 0:** I OK Thank.
[00:50:34:159 - 00:50:34:169] **Speaker 0:** Maybe.
[00:50:38:070 - 00:50:38:479] **Speaker 0:** You're doing.
[00:50:39:790 - 00:50:43:629] **Speaker 0:** Yeah, um, it's, it also maybe also yeah.
[00:50:44:669 - 00:50:45:110] **Speaker 0:** There is.
[00:50:52:050 - 00:50:52:060] **Speaker 0:** Um.
[00:51:05:330 - 00:51:07:629] **Speaker 0:** I think it's just You.
[00:51:13:620 - 00:51:18:149] **Speaker 0:** Yeah, and I was like driving off the road, yeah,
[00:51:18:159 - 00:51:20:120] **Speaker 0:** I got a solid like 3 hours.
[00:53:18:790 - 00:53:18:959] **Speaker 0:** I work.
[00:54:13:770 - 00:54:14:189] **Speaker 0:** I

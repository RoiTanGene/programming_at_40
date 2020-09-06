# How I learned to program at age 40

This is the story of how I finally learned to program at the age of 40. Maybe it'll be of some use to you to show that it's never too late, or that sometimes you just need to find the right language for you to make it happen.

My first computer when growing up in the 1980s was an odd beast called an ADAM:

![](Coleco_Adam_(adjusted_version).jpg#thumbnail)

This was a sort of hybrid of personal computer, COLECOVISION gaming system, and a typewriter. The computer itself is as you can see in the image, with two tape drives in place of a disk drive, an actual TV instead of a monitor, and an interesting printer that had a switch on it that let you turn it into a full-blown typewriter. A lot of other ADAM computer users had actual disk drives but we didn't, and I remember my dad doing a lot of tape recording in the basement when we first got it, but wasn't sure why it resulted in getting so many games out of it. (My favourite was called [Gateway to Apshai](https://en.wikipedia.org/wiki/Gateway_to_Apshai) I asked him about it a few months ago, and it turned out that he used Forth to make it happen:

>I used Forth a bit when we had the Coleco Adam computer which had a Zilog Z80 CPU. Not sure if you remember but I ordered a tape from the U.S. (for the tape drive) that came with several hacker programs and a manual called The Hackers Guide to the Adam which allowed us to download ColecoVision cartridge games to blank tapes so we got a ton of games. I didn't write any programs myself but the programs on the tape came with the source code so you could follow the logic. In some cases I needed to tweak the parameters and re-save in order to optimize whatever needed to be hacked. It was interesting and fun to do.

He showed me something called BASIC that at the time I assumed was the only programming language in the world. I took to it and followed along with [books like this one called the Mystery of Silver Mountain](https://archive.org/details/the-mystery-of-silver-mountain/mode/2up) and [Hunt the Wumpus](https://en.wikipedia.org/wiki/Hunt_the_Wumpus), and pretty soon had picked up how to program and began making my own small RPGs based on [Steve Jackson's Sorcery! books](https://en.wikipedia.org/wiki/Steve_Jackson%27s_Sorcery!). They ended up like a larger version of this code below copied from Wikipedia with a lot of `RAND` for the dice rolls and `GOTO` calls. I remember having to add finer and finer line numbers as time went on (adding a line 65 in between 60 and 70, then a line 67, finally renumbering the whole thing when I ran out of room) and somehow managing to play a musical score at the beginning of the game along with a single line drawing.

```basic
10 INPUT "What is your name: "; U$
20 PRINT "Hello "; U$
30 INPUT "How many stars do you want: "; N
40 S$ = ""
50 FOR I = 1 TO N
60 S$ = S$ + "*"
70 NEXT I
80 PRINT S$
90 INPUT "Do you want more stars? "; A$
100 IF LEN(A$) = 0 THEN GOTO 90
110 A$ = LEFT$(A$, 1)
120 IF A$ = "Y" OR A$ = "y" THEN GOTO 30
130 PRINT "Goodbye "; U$
140 END
```

All this I had done all on my own in an era well before being able to search for sample code online, and by all accounts it looked like I was destined to work in IT. Meanwhile, at school we were being taught to use something called [Logo](https://en.wikipedia.org/wiki/Logo_(programming_language)). This was way less fun, and involved pretty much just making a turtle draw shapes on the screen. You would give it functions like `FD 90, RT 90` and then make it do that four times with `REPEAT 4` and it would draw a square. Drawing a circle took forever because you would have to do `REPEAT 360` to make it happen, so sometimes you'd cheat a bit and do `REPEAT 180` and make the turtle move right 2 degrees at a time so the computer would end up drawing pretty much the same thing but only have to make 180 calculations instead of 360.

Now the funny thing about Logo is that I had almost completely forgotten the experience until I saw [this video by Bryan Cantrill](https://youtu.be/LjFM8vw3pbU?t=246) who is about my age and also had an early childhood experience with it. For him it was the same: he remembered feeling complete apathy about the whole thing and trying to make this turtle draw, and fortunately for him he ended up encountering C and getting really drawn into programming. I didn't. Here's how it went with me:

So in computer class in the 1980s we would all sit inside a windowless room in Ranchlands Community School in Calgary at our computers and make the turtles do stuff. Being super easy to use, it actually didn't even feel like a programming language to me and a few others. The teachers noticed this and told us that there was a Logo competition coming up soon and that we should take part. Memory of the competition is a bit vague but I think it was citywide, or maybe a provincial competition. A few of us from our school went, we got into teams, and were supposed to put something together that impressed the judges. It went on for two or three days where we would do some work there, do some more at home, and finally have a product that gets judged and hopefully wins a prize.

This was where the apathy began to really sink in. My teammate was a lot more into the competition than I was, and my lack of interest was starting to show. Eventually we put something together that I think got in 4th or 5th place, which he was unsatisfied with. I felt relief though as by the time the competition ended I knew that this world of programming was something I wanted absolutely *nothing* to do with. Back then just being good at computers = nerd, and my life's goal was to get the girl I had a crush on throughout elementary to like me back. So even up to then I had been keeping a distance from them so that I could maintain the image of "Yeah, I'm good at computers but I'm not a *computer guy* or anything".

So back to the Logo competition: watching the other people at the competition actually struck fear into me. I felt at the time that if I got really into this world of Logo and programming competitions, which I didn't have any interest in in the first place, I would maybe start to look and become like them and then the girl at school would never give me the time of day. We got a t-shirt and a bottle (I think) for participating, and that was the last I ever did anything with it. Meanwhile BASIC continued a bit until we switched the ADAM computer out for a [386](https://en.wikipedia.org/wiki/Intel_80386) one day in the early 90s and I forgot all about it.

The period from the 90s to the 2000s involved no programming whatsoever. Two things did happen during this period however that proved to be very important: I became a huge fan of Star Trek: The Next Generation, and of Ultima 7. As Data was my favourite character, I would sometimes give some thought as to just how Dr. Soong might have put him together, and for Ultima 7 just [read this post](http://www.chrisguincreations.com/the-drawing-board/16dqd44vpx1eae5tqw17p81itqblwi). The post sums up how I felt about it here:

>Ultima VII was perhaps the first game I ever played where it seemed clear that the world did not exist merely to serve me as a game player.  The store owners did NOT keep their stores open 24 hours a day for my benefit.  If they were at dinner or asleep, I was out of luck. If I invaded someone's house, they yelled at me.  If I broke all their jars and looted the (mostly useless) stuff inside of them, the jars did not respawn when I left the house and came back in - they were broken for the rest of the game.  It felt real in a strange way.  Goofy as it may sound, it's like there was a world I was visiting.

I had and still do have the same feel when I play Ultima 7: the world is so packed with detail that I'll play it even now just to go talk to people, visit bars and watch the people  read the numerous books, and just walk around the world and see what happens.

I knew by then that C++ was used to make games, and maybe it could let me make an android like Data and games like Ultima 7 one day, but I had no connection to programming anymore and the internet still wasn't a thing. That gave me a certain (okay, a lot of) veneration for C++ but I had nowhere to go from there. The Logo event in elementary was enough to have me sever any connection to this world and my main interests were elsewhere.

Eventually I moved from Canada to Japan, then Korea, [where I learned that language too](http://www.pagef30.com/2013/02/how-i-learned-korean.html) and continue to live. One day I met a Korean-Canadian guy from Toronto who was working in Korea as a programmer, which piqued my curiosity. As an ethnic Korean he was able to work freelance, and would just sit at Starbucks all day and program in two languages that he said were called PHP and Python. He told me that I should give them a try since I pick up new skills quickly and it would only help my career. He said that he recommended Python out of the two, and that I should start out with that.

The first experience with Python was more or less utter confusion. I remember reading threads about Python 2 vs. 3 and how 2 was so much better and that 3 was being forced down everyone's throat. Whatever that means. I noticed some familiar things like `print` but the familiar `$` was nowhere to be seen, and there weren't any line numbers or `GOTO`! Even worse, by then the internet was useful enough that it was easy to find discussion after discussion of the benefits of one language vs. another. I noticed that there was another language called Ruby that seemed more like my style, so I gave it a try for a bit. Then I saw that there was another one called Lua that felt like maybe it was made for me. Couldn't figure out how to install or use it, but I was kind of convinced for who knows what reason that Lua was what I wanted. I had some vague idea that this was the easiest programming language one could learn and if I just learned that well I could just sort of pick up all the others later on.

A few months later I met the same friend at a Starbucks and he asked me how Python was going. I told him about how I felt like Lua was the language for me, without giving any real reason why. He eventually commented that "Eh, maybe just not in your genes." I insisted that it was, somehow. How could it not be? I learned BASIC by myself when I was in elementary, I knew I had the genes. I just had to get really into Lua and learn it well...or should I learn Javascript? People are saying you should learn that first...no, Python. Though I like Ruby better, shouldn't I just learn that and I'll pretty much know Python by the end anyway? And on and on it went until I lost interest again. I did eventually learn [how to take user input in Python and use it to return results](http://www.pagef30.com/2010/04/creating-necessary-and-useful-content.html), but if I remember correctly I don't think I used a single external function to do it.

I ended up living in Canada again for a few years, and programming was nowhere on the radar. I was at a company called TransCanada Pipelines where becoming a good project controller (or related position to project controls) was key for the employees in our group. The only programming-related event during this period (2011 to 2015) was one time when we were implementing SAP and we heard that there were all these C++ guys in the other building. They were contracters that were there to customize SAP for pipeline and other energy projects, and were making fantastic amounts of cash doing it.

Oil prices crashed in 2015, so did the Calgary economy, and our entire team was let go. With a nice layoff package I decided that this was the time to really learn to code. During this time in Canada (2011 to 2018) all I wanted to do was return to Korea, and I considered either finishing university or learning to code, and decided that the latter was the way to go. It turned out that finishing university was the right choice and that's how I did end up back here, but in the meantime in 2015 I finally got a feel for what Python was. I picked up how to write functions, how to make objects, etc. but the `self` keyword was still confusing and so was using objects. A bit more effort would have sufficed to get over that, but the old wanderlust struck again: 

- "Python's horrible for making games - this won't let you make anything like Ultima 7." 
- "Why not try out C++? No, that's too hard. C#? Let's try that."
- "Wow, this is pretty complicated. Still, looks like C# is the way to go! Wait, what's this? F#? This language is really cool."
- "F# is awesome! Why aren't more people using it though? Maybe I should finish properly learning Python..."
- "So Python it is, nice and easy! Unless it's Javascript. Then I can do anything in just a browser. Maybe start with some browser-based games? Time to give that a try..."

Then the layoff package money started to dry up and it was time to find work again.

I finished university, returned to Korea, and in August last year gave my notice as a copywriter at the company I was working at the time. With a month left until my last day, I started to think about maybe really learning Python this time. I could put in a few hours a day, get pretty good by my last day, and then spend a month or so binging on it before it was time to find work again. So I did that for a few days until the wanderlust struck again. I had read a bit about a language called Rust that apparently was really precise and tough to learn. I was still curious though and decided that I would just give it a try and see what it was all about, but I'd really concentrate on Python. For sure this time - don't give in to the wanderlust!

I started with Rust on [learn x in y minutes](https://learnxinyminutes.com/docs/rust/) and the [Rust playground](https://play.rust-lang.org/). Curly braces to capture variables to print was the same as Python, but a lot of it looked like the C# that I had tried out a bit before. As I started to learn it I checked to see what you could do with this language, and the answer was invariably *pretty much anything*. So I could make something like Ultima 7, or anything I wanted. But what was even more interesting was how the detail and the low-levelness of the language did nothing to turn me off: it only drew me in more. It's probably the time spent growing up in the 80s that has something to do with it as I felt a lot of nostalgia as I got more and more into the language. Everything I wrote was turned straight into a binary and I could see the computer's internals again. Tons of Rust discussions were about how to optimize code, and I found this fascinating. But at the same time this language was high-level and safe enough that I didn't need to worry about shooting my foot off, so to speak.

[Programming Rust](https://www.oreilly.com/library/view/programming-rust/9781491927274/) was too much for me on first reading (too many references to C++ and C for one), so I read [the Rust Book](https://doc.rust-lang.org/book/) and then came back to it, and ended up enjoying it the most. What helped the most though was binging on videos of live coding streams. The first one was the 70 or so videos by [Brooks Builds](https://www.youtube.com/watch?v=SRDqvQqWAuE&list=PLrmY5pVcnuE_dyWibakRuGJcuiwAkhGZB), a Javascript developer who recorded himself going through the Rust Book every step of the way. There's something about watching someone struggle through a language that you are learning too that makes you mentally participate in a way that other types of streams can't do. I had the same experience with the [Lernen to Talk Show](https://www.youtube.com/playlist?list=PLF3lNEjv7avTzYQwXU4DssdwRvG35O7Ei) in German by a guy who recorded himself every week in Germany as he learned the language and got better every video. Watching the person struggle when you know the answer is probably the part that brings you in the most. ["It's mit einer deutschen Familie, not mit einem deutsche Familie!"](https://youtu.be/8BnZAXFAiHg?t=231) or "Just use into_iter() and it'll compile!" are the moments where you feel like you're really learning alongside someone else (and in fact you are) and this can't be replicated by someone who has already learned the language and is already typing or chatting merrily away without a single error.

After that I started watching [Brian Myers](https://www.youtube.com/user/bcmyers05) who also learned Rust basically by binging. [Jon Gjengset](https://www.youtube.com/channel/UC_iD0xppBwwsrM9DegC5cQQ) I was saving for last (this was before he started Crust of Rust to teach simpler things) and in the meantime also watched all of [Hello Rust](https://www.youtube.com/channel/UCZ_EWaQZCZuGGfnuqUoHujw), [Ryan Levick](https://www.youtube.com/channel/UCpeX4D-ArTrsqvhLapAHprQ), [Doug Milford](https://www.youtube.com/watch?v=Az3jBd4xdF4&list=PLLqEtX6ql2EyPAZ1M2_C0GgVd4A-_L4_5), [Tensor Programming](https://www.youtube.com/watch?v=EYqceb2AnkU&list=PLJbE2Yu2zumDF6BX6_RdPisRVHgzV02NW), [this Rust crash course](https://www.youtube.com/watch?v=zF34dRivLOw), [the Rust videos by dcode, etc.](https://www.youtube.com/watch?v=vOMJlQ5B-M0&list=PLVvjrrRCBy2JSHf9tGxGKJ-bYAN_uDCUL) (not all in that order)


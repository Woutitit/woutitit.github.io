# Recording

#############################################
## Equipment
#############################################

### Audio interface
A computer's internal soundcard can (usually) record (AD/DA convert) audio just fine through USB. However, if you can't (or don't want to) record to your computer through USB, you'll need an audio interface. In other words, whenever electric guitars, XLR-cabled mics, etc. are involved you'll need an audio interface to input your cables in. The audio interface, connected via USB (preferably a fast connection such as USB3 or Thunderbird to reduce latency) will then send the audio to your computer.

Now, what does an audio interface do exactly? Well, besides being an input hub for a lot of shit it also has a built-in *DAC*, i.e. a digital-analog converter. What this means is that it can convert analog signal (your voice, guitar string vibrations) to digital so that the computer can understand it and display an interpretation of the analog waveform. However, it can also do the opposite, that is, it can convert digitally encoded audio sound into analog, then send it to our speakers so that we can understand it (for example, a youtube video). In fact, our computer's sound card has/is a DAC too, but usually a DAC of a (high-end) audio interface processes things faster which minimizes latency for whenever your recording things.

Most audio interfaces these days also come with a pre-amp. Recordings of microphones and stuff are usually very low (why?) so with a preamp we want to get it to line-level (why?) so that we get a workable signal in our daw.

One thing to keep in mind with choosing a AI is latency. Like, even if we don't use a computer's DAC and USB recording (which both together can be slow), we can still have latency. This can be annoying since you might be hearing an echo while recording making it hard to accurately record. The above article shows some ways to circumvent it. What also might help is that you do as much plugins/fx as possible BEFORE going into the audio interface so that you don't get the latency of all the virtual processing that might go on in your DAW that need to be processed everytime (I ain't sure about this though):

https://www.bax-shop.be/blog/studio-recording/hoe-voorkom-je-latency-in-daw-software/

### DAC, Preamp, Amp 
So I explained DAC, Preamp already. Sometimes, if you want to have control over everything you'll have your preamp seperate from your DAC Audio interface.

Now, an amp you'll need to really turn up the gain and have a workable signal (why amp and preamp needed, why not just amp? Look up and write here) to the record or play live. The reason we want to seperate an amp and preamp is...


Now, the recorded sound wave we see in the DAW ain't exactly the real audio wave we recorded. You see, just like 3D images there is a certain resolution/quality we can record with it. Like, in a 3D image, a curve is not a curve but basically a series of small lines in an angle (since curves are impossible to draw since computers are pixels)


#############################################
## Recording a guitar
#############################################

### Electric guitar
The two most common ways to record an electric guitar are either through an amp + (multi)mic + audio interface setup or through an audio interace + amp sim(ulator).

#### Amp + (multi)mic + audio interface
For this technique you'll will preferably need to have a treated room to record in since you're working with microphones.

What you do is just connect your electric guitar to your amp as you would usually do and then put a microphone directly to the speaker CONE of your amp. Depending on the microphone and the amp, the distance you need to set your microphone to get the best sound will vary (look it up).

Shure sm57 is a classic guitar amp recording mic.

This technique is the most common technique and still the preferred technique over anything else. Reason is that nothing else can capture the sound of a good electric guitar, a good microphone, an authentic amp and a well-treated room.

If your room is not well-treated, though, you can still do this technique if you do something called "close-micing" in which you place the microphone as close as possible to the amp. The closer you put your mic the more your room gets eliminated since you don't need to turn up your gain as much and stuff to hear your signal thereby eliminating any unwanted noise. The disadvantage is, though, that you don't get the "well-treated room" sound which is a pleasant sound that you usually want in your recordings. Also, some mics and amps function best when there is a distance between them so you're kind of forced to distance your mic more and thus you allow more room to come through too.

Also, if you want to record a stereo guitar, you'll need two microphones and (two audio interface inputs). Of course, the microphones need to be different (so they pick up different stuff) to get actual stereo image and not just doubling of your sound. If you double your microphone you also need to be aware of phase issues. Also, I have seen some people say that it's best to record in mono anyway and just record multiple slightly different tracks (or do processing on two copies of the same track to make them distinct and have stereo). Also, it's common to record the neck and the bridge. (both two mics? Or one mic neck and one bridge?)

#### Audio interface + virtual amp
This one is preferred when you have an untreated room and also not enough guitars and amps to get the sound you want.

What you do is simply feed your guitar to your audio interface directly and then use an amp simulator to dial in your tone. This has the advantage that you don't need several amps for different sounds since there are a lot of amps to choose from in the virtual amp simulator. Your guitar build can of course still matter. 

**INTERMEZZO: The reason we want a virtual amp and not just stock plugins is because these are actually made to simulate an amp, the settings of an amp (even the recording room, just like with drums, in fact you can even change microphones thus to have microphones pick up slightly different things, wouldn't be surprised if you could alter the microphone to amp distance too, and the fx of an amp (like guitar pedals and shit). You could technically come close with stock plugins if you really know what you're doing (a flanger is just a flanger, regardless if it's stock or inside a plugins) but it's just so much more convenient to have an actual amp sim. Additionally, Lenno also likes to run other stuff through guitar effects too other than guitar. So a virtual sim can thus be useful not only for virtual guitar simulation.**

Also, since instead of the signal of a microphone, the signal of your magnetic pickups gets send to a microphone you don't need to worry about your room. Reason is that (magnetic) pick ups ONLY record the strings (mostly) - and then through the guitar internals and the cable send it to the audio interface - and thus don't record anything around it, therefore it won't show in your recording if you're room is shitty. Again, of course, you don't get the acoustics of a well-treated room but still, you get a very decent recording.

**Now I don't know if room treatment matters AT ALL for this method, though. I didn't find any resource on whether you should still treat your room since maybe pick ups or string vibrations itself or whatever can be affected by the sound. I don't think so but I'm not 100% sure. A well-treated room is always best to be safe of course.**

Now disadvantages of this are though that you will have latency in your recording due to your amp simulator/fx. Even with really good audio interfaces, if you play your part with your virtual tone dialed in you will be thrown off by the small latency that it causes. Therefore, you need to click the "direct monitor" button on your audio interface, this will turn off the sound you sent and instead sent you the DIRECT sound you make. This means you can now in real-time hear your playback and it's so much easier to track/record. Keep in mind, though, that in this case you will have just a dull and clean guitar, no fx. (I don't know if there is a way to get effects or at least some distortion on a direct monitor, look it up, that misha guy though somewhere in this video had seemingly fx, how? (https://www.youtube.com/watch?v=er9VhozNHNk&t=613s).

ALSO TRY THE BUFFER SIZE FOR LATENCY? BUT CAN'T BE TOO LITTLE WHY NOT?

Another disadvantage is that of course an amp simulator will never 100% sound like the real thing. But again, it's definitely the best bang for your buck (since you don't need acoustic treatment, or multiple amps irl).

You can even use hardware fx next to your amp simulator if you so desire.

#### Other
Re-amping? For Stereo or what? Amp modelling? Difference between all kind of amps?
Guitar rig is apparently date, I mean it's true there hasn't been an update for real long:
https://www.reddit.com/r/Guitar/comments/8rcol3/question_best_amp_simulator_software/

The shady guy uses both line 6 pod farm 2.5 and bias fx (i guess if not enough amps in one of them that he likes) i guess pod farm really for metal but im looking for clea actually, funky.
Does electric guitar string/wood make sound different ye or no? or only strings?
It's solid I'd suppose (Lenno uses it) but why not check out the newer options now that I'm not yet into the ecosystem of guitar rig.

"crackle" is gekraak is what i heard when i wasn't using correct drivers with my audio interface, also is my interface too slow?

also, if u dont need virtual sim amps u can make channel sends (so not inserts) and then mute ur virtaul amp insert but since u send ur audio also through reverb the reverb + direct monitoring still goes so at least, even if ur guitar signal still dry u got some reverb (albeit with some latency still but only reverb not actual recording) in there:
https://www.bax-shop.be/blog/studio-recording/hoe-voorkom-je-latency-in-daw-software/

### Acoustic guitar
Acoustic guitar, unlike electric guitars, don't have pick ups and instead rely on the body, the strings, etc. to generate a sound. In other words, the actual whole guitar and its build quality, together with string quality is what makes up how good or bad or how a certain guitar sounds. However, this also means that you can't just go straight into an audio interface with your guitar and record it. (well actually you can but you don't want to. I'll explain later.)

#### (Multi)mic + Audio interface
So for acoustic guitar you can have the same setup as electric guitar, just without the amp and the microphones also pointing to bridge (and neck?). Again, room of course matters here.

Investigate this more when I'm actually recording

#### Pick ups
So you can actually also use pick ups on an acoustic guitar to pick up the vibration of the strings. However, as we said, we actually don't want to do that because the string vibrations ain't the whole sound of an acoustic and so we're essentially not listening to a real acoustic tone anymore. Acoustic is all about that well-treated room and the body, string, etc. combination.

So why is that a thing then? Well, again, in untreated rooms, a mic might just sound really bad (like maybe in a church where the reverb is off the charts) so the acoustic will sound really bad. In that case, to capture the clear acoustic sound (only the strings) pick ups are used. In other words, in live setting where often the room ain't ideal, pick ups are used to kind of have a compromise between the real acoustic sound but also the clear sound. And since, in live, real accentuations and antenuations and like detail of sound matter less (it's more about performance and atmosphere) this is an okay compromise if it guarantees a consistent tone.

Some go next level even and record BOTH mic and pick up and then mix the signals together. Reason for that is that you get best of both worlds, clear tone but also the real acoustic tone. Of course it depends on environment and how necessary it is but it can be done (I don't know if this is common, look up).

Also, if you go this route don't go for magnetic pick ups but go for piezo pick ups instead. I don't know the exact science but first of all magnetic pick ups require steel (which I guess ain't ery acousticy as nylon or whatever) but piezo pick ups sound for some reason more acoustic than magnetic pick ups.

### Guitar recording tips
[https://guitar.com/guides/essential-guide/how-to-record-electric-guitars-25-top-tips/](https://guitar.com/guides/essential-guide/how-to-record-electric-guitars-25-top-tips/)
https://www.youtube.com/watch?v=er9VhozNHNk&t=613s
[https://www.sweetwater.com/insync/double-guitar-parts-recording/](https://www.sweetwater.com/insync/double-guitar-parts-recording/)

- Instead of software or a real amp, you can also use amp modelling which is "a real amp" but can model all different kinds of amps. So it's like an amp simulator inside of a hardware amp. High end stuff like the Line 6's Helix Native (https://be.line6.com/helix/helixnative.html) and Fractalaudio's Axe fx II (https://www.fractalaudio.com/p-axe-fx-ii-preamp-fx-processor/) sound real good but are also really expensive. Therefore, usually either a normal amp or a virtual amp simulator is preferred. Other type of amps: https://www.dawsons.co.uk/blog/what-is-the-difference-between-modelling-amps-and-other-types
- Dialing in tones on a virtual amp takes a while (or tweaking presets). Once you're happy with a tone, save it so you can later quickly make use of it when creativity strikes (of course you can still dial in other tones and having that one saved somewhere else)
- When recording through a virtual amp, ff latency issues can't be solved even when doing bax-shop's tips above, then the only solution to record your guitar without latency and with still hearing a wet signal (according to: https://www.gearslutz.com/board/music-computers/1127519-guitar-amp-simulators-latency.html) is to have a split signal. That is, have a cable connected to your amp where you can hear your playing (like distortion and maybe some pedals for fx) and then have the dry signal going to into your interface. Now of course, if you want to record a guitar with loads of fx and a particular amp sound and you don't have a lot of analog fx and that particular amp, your wet sound is going to not be representative of wat the end sound is going to be when then adding fx to the dry recorded signal through the virtual amp which might be annoying.

#### Dual/Quad tracking guitar
The above links have some good tips. For example, double tracking and quad tracking is very common in guitar. Of course it depends on how much of a wall of sound your guitar needs to be, how dense, which will decide whether you need single, double or quad tracking of your guitar. However, at least double tracking your guitar can be helpful for stereo (which is the reason why you want to do it, have a nice full sound + stereo image).

So you can also double track/quad track in many different ways. They will all kind of boil down to a little bit different but same kind of sound. Like, you could record once, and then double them but slightly change up the processing for both of them so they sound different. Or you could play the same line two times and then have the slight incosistencies make up the wideness of the dual track (of course need to pan to have it happen??).

#### Hard left and right panning
https://www.youtube.com/watch?v=ww-cH29IGeM
Ain't sure how much of a tip or how common this is. But hard panning is real wide. Also, like some eq to accentuate some nice shit and some scooping if too much from certain kind of mix to make it sound less boxy.

### Unprocessed notes
will need either audio interface or mic (or even phone if you couldn't care less). With audio interface you need stuff like pod farm 2.5 or guitar rig 5 (basically virtual amps/amp sims/amp simulators) to actually have fx on your guitar. You could do it with fruity fx but these tools make it so much easier to record with fx on and also to get a decent nice tone out of your guitar as they are designed for that.

[https://musicaroo.com/preamplifier-vs-amplifier/](https://musicaroo.com/preamplifier-vs-amplifier/) 

do u need preamp?

[https://musicianshq.com/how-to-record-guitar-without-an-amp-the-complete-guide/](https://musicianshq.com/how-to-record-guitar-without-an-amp-the-complete-guide/)

[https://reverb.com/news/the-easiest-way-to-record-your-electric-guitar](https://reverb.com/news/the-easiest-way-to-record-your-electric-guitar)

3 types of mics with 3 types of function, which is best for close miccing??
ribbon needs power, PHANTOM POWER

we need preamp to make signal to "line level" cuz mics too quiet + and dac (analog to digital, digital to analgo converter) but usually all these are included in an audio interface so they do the job so u dont need seperate gear.

ideal signal to noise (meaning as much signal as u can without degrading the sound) is right where u dont start clipping. so on the edge, on focusrite green, almost going into yellow/orange. Reason u want as much signal is that it's easier to work with i guess, or that in stuff like saturation plugins u need it since otherwise effects wont be audible so if u apply saturation but not enough input to the plugin it won't apply enough to be audible so even if u turn up output u wont hear shit change. Why won't it apply to that. Look at the in the mix audio interface and saturation videos.
if u set signal to lower u dont get the most efficient signal cuz u get more noise relative to output like env noise (?) cuz u need to turn up output to hear ur shit more so u turn possible other artifacts up as well.

why does clipping happen

for dialing in tones u want direct monitor off to hear ur tone (if u work with amp sims i guess only) but then u want direct monitor on ur interface on to record because sadly with direct input and amp sims there is always latency, so to record ur stuff/track stuff u do want direct monitor. Can u get an amp on director monitor or is it only when u mic ur amp or just ur dry guitar sound tone?

double tracking/quad tracking. reason u cant just double ur one recording is because then it just sounds louder, it's the slight imperfections of two records that play the same stuff that makes it wide. However, cant u just do it with two mics then on one take and not two takes? What about quad tracking? Also, can't we make the two guitar tones like different, like detune different and shit to make the stereo sound instead like slight detune? Like we do with synths to make 'em wide. quad tracking u lose transient and some bass, but u get a wall of sound. why not triple track?

reason u want to record ur shit as dry as possible (so like even in a closet with clothes) is that's it's way easier to ADD reverb and other sounds to your recording than to remove from it. If we could as easily remove that shit as add we would not need treated rooms (though it would still be hassle to always remove it since mostly we don't want room reverb/reflections in our sound).

interface fast connection like firewire usb3, also amount of inputs matters, for guitar (i think stereo two tho) u need one, but for choirs and drums u need a lot.

[https://www.youtube.com/watch?v=awzXNl30lKg](https://www.youtube.com/watch?v=awzXNl30lKg)
ribbon condenser and dynamic

should i normalize or not

u can do amp recording and then still do guitar rig for just ur effects (which else u would have in pedals hardware) or do u need to do virtual amp then?

UNPLUG PHANTOM POWER BEFORE UNPLUGGIN CONDENSER MIC CUZ PHANTOM POWER CAN BE A BIT LOOSE/ELUSIVE.

audio is a waveform, and just like in 3d where a wave (or a circle) is basically a series of straight lines (since u cant draw real curves on a computer) a waveform sample rate/bitrate also determine the quality of a wave we "draw". Just like in 3d the more lines we have to make up a curve the more it will look like a curve (if little lines it looks blocky and low samply). Same with sample rate/bitrate. The more we have, the higher quality. However, just like 3d, the more also means more expensive so u want to find a compromise.

so 2 inputs is the minimum to record a stereo signal? else record mono and make it in processing stereo or if virtual amp software can do that?

latency, secret is to have good interface but also keep buffer size low but not so low that the audio starts CRACKLING and bumping?? popping?? (in which u might need to raise buffer size).

standards:
focusrite2i2 audio interface
dynamic mic shure sm57

arming a track
too much gain clipping so like good gains staging

on audio interface the 48V nob is the phantom power, so for ribbon mics that need it.
## Guitar
Modelling amp vs. preamp vs. amp sim vs. amp vs. reamping
## Audio interface vs. Direct Input (DI) Box vs. Preamp
## Random notes
For recording you need to acoustically treat your room. Also if you use audio interface?

[https://www.edmtips.com/14-tips-mixing-bedroom-studio/](https://www.edmtips.com/14-tips-mixing-bedroom-studio/)

Get aywa from walls and corners, like it's all about reflections and standing waves. Close mic technique to record? Is that a good technique
> Written with [StackEdit](https://stackedit.io/).
so u want close mic cuz then u can output less gain and the closer the less gain u need and the less u pickup from room the further the more gain u need to turn up and the more room u pick up so why still room treatment if u can do close mic? Cuz close mic not perfect? Cuz u want the acoustics of a good treated room too???

mixing microphone and pick up recording for live performnces why i guess for natural + stable sound and mainly for acoustic guitar.

what is line level and why do we even need line level?

plectrums also do matter, like u want a soft plectrum for that typical very strummy open chord sounding sound (like also with the plectrum strum sound, i wonder if u would hear that without a mic and only pick ups like do they pick the strumming sound of the plectrum up cuz that is a dinstiged part of the sound), but for like heavy guitar/jazz u need stronger plectrums.

so micing far away better cuz it does capture more like ambient and 3d of a good treated room BUT if u have a bad room it's bad. close mic is more dry but adding slight reverb after COULD be more mechanical than the former. However it's more dry and consistent, thereforeu could even mix the two.

useful links:
[https://ask.audio/articles/6-mistakes-to-avoid-when-recording-electric-guitar](https://ask.audio/articles/6-mistakes-to-avoid-when-recording-electric-guitar)
[https://guitar.com/guides/essential-guide/how-to-record-electric-guitars-25-top-tips/](https://guitar.com/guides/essential-guide/how-to-record-electric-guitars-25-top-tips/)
[https://www.sweetwater.com/insync/double-guitar-parts-recording/](https://www.sweetwater.com/insync/double-guitar-parts-recording/)

## How to Double a Guitar Part

HereÃƒÆ’Ã‚Â¢ÃƒÂ¢Ã¢â‚¬Å¡Ã‚Â¬ÃƒÂ¢Ã¢â‚¬Å¾Ã‚Â¢s a list of four different methods for doubling guitars, and they all give slightly different results.

1.  Copy/paste a performance onto another available track and modify the processing of the  second track.
2.  Along with your original performance through an amp, record a DI track directly from your guitar and re-amp that.
3.  Bus a mono guitar track to a stereo effect.
4.  Create another performance of the same part. Doing this will give you microseconds of inconsistencies in timing, attack, release, and dynamics that create feel, groove, and the intangible human factor.

To hear the differences between a copy/paste or DI track and a second performance of the same part, try this:

1.  Play a single guitar performance
2.  Duplicate (copy/paste) that performance to a second track and mute it
3.  Play a second performance of the same part, as precisely as possible
4.  When youÃƒÆ’Ã‚Â¢ÃƒÂ¢Ã¢â‚¬Å¡Ã‚Â¬ÃƒÂ¢Ã¢â‚¬Å¾Ã‚Â¢re satisfied, mute it
5.  Listen to the original track soloed
6.  Unmute the duplicated (copy/paste) track, and pan the two tracks at 35% Left and 35% Right with the volume levels equal between the two and listen
7.  Do the same with the second performance and mute the copy/paste track

shure57 needs to be close and needs to be directly pointed to the speaker CONE so i guess the round thing inside a speaker.

like double trakc quad tracking just like layering depensd a bit, u want a lot of layrs if u want shit to be huge and absolutely dominate a mix, which basically means no room for other shit. U want no layers if u have a lot of other stuff going on (or u want a little less layers or more subtle layers in this case) and not layers for everything it depends. Like sometimes u want ur guitar to sound huge but sometimes just a funk guitar like one and maybe two subtle layers will do.


the source is huge, sound selection is huge.

put mics in spaced pairs and u need two mics to record stereo cuz they'll pick up diff stuff BUt u want good pairings and good spacing cuz else u will have bad stereo image/phase issues.

mixing env and recording environments need different treatments therefore u often have two spaces one for recording one for mixing, why do they need different environments? Also, usually homestudios make compromises cuz they dont have two rooms let alone the budget for two diff treatments. So good compromise between mix and recording rooom.

boxy is mid range is like dull cuz not too much high or too much mid
ott basically does this too by equalizing the ranges too but kidna extreme

eq sweep spectrum is good to know what to boost and cut => eliminatte but not too much resonant frequencies.
Sample rate can be compared with drawing a circle. Curves don't really exist (https://old.reddit.com/r/explainlikeimfive/comments/g85xxd/eli5_why_can_computers_not_make_curves/) and so a computer can only draw a small circle with angled lines. If he uses 10 angled lines (low sample rate), he might get close to a circle but we kind of still see it as just a figure with a lot of angles. However, if he can use 10 000 lines (high sample rate) for a small circle (slow frequencies), then he can use very small lines and all angle them and to our eye it's going to look like like a perfect circle even though it isn't. Now the bigger the circle (the faster the frequencies) the higher the amount of lines we need for our circle to seemingly appear as a non-angly circle (since there is more length to cover).
[https://www.youtube.com/watch?v=ww-cH29IGeM](https://www.youtube.com/watch?v=ww-cH29IGeM)

what are standard sample/bit rate why? cuz human ear can not distinct above 100 and 44k?



(in other words, too low of a sample rate might cause you to lose some of the faster, higher frequencies)

So (why) would we ever want less than the best. Well, sometimes (for CPU reasons).





sometimes, we on purpose down sample because of fx prurposes  Downsampling?
as effect or any other use? creates saturation warmth or??


Now, the recorded sound wave we see in the DAW ain't exactly the real audio wave we recorded. You see, just like 3D images there is a certain resolution/quality we can record with it. Like, in a 3D image, a curve is not a curve but basically a series of small lines in an angle (since curves are impossible to draw since computers are pixels)

does cpu still matter once recorded so why not always do highest of highest?
So every

since sample rate too slow of course can't catch waves that go faster than the sample rate so these won' recorded and since you need to account for negative values u need to double the sample rate. Bitrate is about loudness?

https://music.stackexchange.com/questions/40529/why-do-people-use-a-microphone-to-record-an-electric-guitar
cigar stomp box what is it
https://old.reddit.com/r/explainlikeimfive/comments/g85xxd/eli5_why_can_computers_not_make_curves/
<!--stackedit_data:
eyJoaXN0b3J5IjpbMzU5MzAxNzMsMjAzNjA3MDQ4MSw2ODIxOD
g1NTEsLTIxMDI0OTQ1MzAsMjIyODU3MjI1LDYyODQyNjk4OCwt
MTUxMDk3MDg4MSw5MDI1MTk0MTgsLTEyOTk4Nzg2MTMsMzM0NT
M2MDExLC0xNzM2MDE0MTQ4LC01NTkwNDY0NTMsLTE1MDg4NzM1
MjMsLTE5NDE5NjQ2MzQsMTI3MzQ5Mjk2Nyw0MTg3OTg1NjMsLT
EyNzAxNTA2OCwtMjEzNTU5NzY0NCwtMTE2NDQ3NDI1NSwtMTg0
NjI4NjgwM119
-->

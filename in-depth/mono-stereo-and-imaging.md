# Mono, stereo & stereo image
## Table of contents
1. Introduction
2. Mono vs. stereo
3. How stereo gives direction
4. How stereo gives width
5. Stereo width techniques
6. When to use stereo vs. mono
7. Common stereo effects
8. Notes

## Introduction
There used to be a time where we didn't have to talk about this topic. Everything used to be mono. However, now that stereo has been here for several years (decades?) we do need to talk about both of them.

Now, at first glance, stereo might just seem like it trumps mono in every aspect. In terms of theoretical possibilities, this is true since stereo can do everything mono does and more. However, practically there are benefits to both and depending on the situation you'll want to favor one over the other.

## Mono vs. Stereo
https://music.stackexchange.com/questions/24631/what-is-the-difference-between-mono-and-stereo
https://www.gearslutz.com/board/low-end-theory/493561-can-someone-explain-phantom-center-me.html
https://en.wikipedia.org/wiki/Phantom_center

The linked answer could not have worded it better. Mono is the use of a single channel (audio signal) that can then be send out to one or more speakers. Stereo is the use of two channels that requires at least two speakers so that 1 channel can be send to one speaker and the other channel to the other speaker.

Now obviously, in the case of stereo, if you're just going to play an exact copy of the first channel in the second channel and cast it to two different speakers, you could have also just casted a single mono channel to two speakers as it is the same. In this case, stereo is pointless. So you may ask, why have 2 channels then? Well, because we can actually have 2 DIFFERENT channels that we can send to two speakers. The result is *the ability to give a sound a certain directionality, perspective, space, etc.* That is the point of stereo.

Now, one note to add here is that when we here mono from a stereo setup (so two speakers with 2 different channels) it simply means the 2 different channels have the exact same output making it APPEAR as a mono signal, i.e. a center. We also call this the *phantom center*. This is an "important" distinction since if you would have 2 different speakers, but they are mono, next to eachother, you would have the same signal too, BUT you'd have it louder (?) since the waves add up.

## How stereo gives direction
https://www.dawsons.co.uk/blog/what-is-panning

Now, how can having 2 channels create direction? Well, you can test it yourself. Get two speakers, setup one left of you and one right of you. Then, sit right in the middle of them. Alright, now just produce a basic sine wave in your DAW. What you'll hear is a mono signal since the signal of the sound wave gets send to both your speakers equally. However, if you were to hard pan this sound to the right, you'll notice something. Yup, indeed, the sound appears as if it comes from the right! 

So how is that possible? Well very simple, the left speaker's channel simply ouputs 0% of the sine wave while the right speaker outputs 100% of it, giving the sense that the sound comes fully from the right. You could do the same with a "hard pan" (i.e. 100% pan) left, noting that the signal comes fully from the left of you. Similarly, if you pan the sine wave 75% right, then there will still be 25% of output left which in essence means 75% of the loudness of the total signal comes from the right speaker and 25% from the left speaker. Because of this more nuanced difference, we'll still hear the sound coming from the right more than the left but is not as pronounced since the volume right isn't maximum and the volume still plays substantially.

Compare stereo with having a space of 180 degrees from left to right in which you can now put sounds in, each in their own little space in that range if you want. This allows us to basically create a more realistic and wide listening experience. For example, in an orchestra the sound of the string all don't come from the same direction either (they all can't sit on the same chair) and it creates this very wide hearing experience. This is what we can emulate in the DAW too thanks to stereo being a thing.

Later we'll go over some common applications of "direction stereo" but read my individual analysis and analyze some music you like to hear how they use "direction stereo". Sometimes they might automate a sound from left to right panning which can be cool or other times one might create some call in left pan and then a response in the right call with percussion. You can get really creative with it.

That said though, you generally don't want to go overboard with panning sound left and right, especially not with your main sounds since it's going to be very weird to have, e.g. your kick drum being audibly louder in the right ear than the left ear. Therefore, generally speaking, if you're going to do "direction stereo" you should mainly do it on ear candy things or on short sounds rather than main elements such as bass, drums, leads and chords that usually really need to be equally heard in both ears to not make the sound weird. Of course, you can still experiment with some short automations here and there of these elements to add some suprising effects but in these cases you want to keep it brief and/or subtle.

## How stereo gives width
https://www.justmastering.com/article-stereo-width.php
https://www.soundonsound.com/techniques/classic-stereo-widening
https://www.kontactrecords.com/easy-ways-to-greatly-improve-your-mixing-fundamentals/

Where the x-axis depicts the frequency range of a sound and the z-axis the volume, the y-axis represents the width/panning of the sound.

Now, another thing that stereo can do is actually create the illusion of thickness and wideness. That is, making it sound as if the sound is coming from all around you (or at least not from the center). The difference with "stereo direction" is that in this case you will actually (usually) not be able to hear as if the sound is panned either left or right, instead you hear a sound coming from all directions. It really is a bit of a trick on our ears but it makes for a sound that sounds "wide" since it seems to becoming from around us rather than the middle.

So, how does this trick work? Well, there are various ways to achieve a "wide" sound but they all have in common that the left and right center should be different (of course). However, in the case of thickening, what you'll want to do is usually have both the left and right channel be REALLY SIMILAR YET DIFFERENT. Our ears are deceptively good at picking up even minute differences between both channels, thus contributing to the wideness. And thus, this is basically the key to create the illusion that the SAME sound is sounding stereo rather than mono. 

## Stereo width techniques
Now, stereo widening is actually very common (probably more common than "stereo direction") and there are actually are various ways to create this similar yet different sound (look up all techniques, HaaS effect, but why not do that?). Things such as double tracking, short delays, detune, reverb, etc (other? Look up common stereo widening techniques! Izotope article?). all are examples that producers use to make a sound sound similar, yet wide. Do note though, that all these effects do have slightly different purposes as the results will all sound slightly different.

So, double tracking (or even quad tracking) a guitar (or a (backing) vocal) works by recording two very similar takes and hard pan both takes left and right. This way, you'll have a different take for each channel and it will thus sound like a wide thick sound. But again, since the difference is really small, it just sounds like one wide sound and not two different sounds being either hard panned left and right. Having these takes being too different (or if for some reason you processed the two channels with different fx) it will again sound more like two different sounds coming both from left and right and thus diminshing or even destroying the illusion of thickness and wideness.

With delay, what you do is basically (hard?) pan two instances of your signal left and right. Then you add a very short delay to either one signal (so it plays later than the other signal). If your delay is big enough (but not too big), you'll now kind of hear your sound alternating between L and R. It creates this really cool stereo effect of having notes being played in L and then shortly after being repeated in R. Additionally, since there is no silence or space between L and R being played, it also doesn't sound weird or "with a direction" (like if you'd just have a sound panned left and another sound right), but rather it sounds like a full unison wide sound. Now of course, maybe this effect might be too strong for you so you might want to have it less obvious that notes alternating between L and R. In that case, just make the delay shorter and you'll notice that you can get to a point where your sound is still sounding wide (because technically we still have the L+R alternation going on) yet not noticeable that we achieved this with a delay. Now of course, oppositely, if you make your delay too big, it just sounds like a "real" delay effect and just like two sounds being played L + R but there is no real unison or connection since the delay is too huge and thus destroying the widening effect. (HaaS effect is related to this but you want to avoid that, why? Do you want to avoid delays as stereo all together since phase cancellation might occur if summed to mono?). AS this guy say at 27:00 though, your delay needs to be less than 30ms for our ears to hear it as one single sound rather than an actual delay.

Another technique is detune (+ unison). This one is often used to make supersaws wide and thick (thick because a bigger detune adds extra harmonics). The way detune works is by also taking a copy of the original sound and then again panning them both (hard) left and right. However, you make one of the sounds slightly out of tune. This also yields us a very nice wide sound since the waveforms are both slightly different. You can keep doing this with more and more voices, with all slightly different tunings (?) and stuff for different and possible bigger/wider results so it really is a bit up to experimentation for this one and experience.

Last main one is reverb. Reverb is in stereo too (how?), so even if you don't use above techniques you can still use reverb to give it some width. It can be nice if you want a sound to be mainly mono but to have a bit of subtle width too (like a lead or a main vocal).

Now, anyway, all these techniques can be used in conjunction with eachother (should they though?) as they all add different things to the table. Obviously it might not make your sound already wider than it is but might just add some nice effect on top of your wideness obviously. Just experiment a bit.

## When to use stereo vs. mono
So we're gonna talk about speakers and music production, speakers clubs and stuff, maybe main stage cuz u dont want phase cancellation or want people to hear like only L or R depending on where they are.

also, if everything is wide nothing is wide so need contrast
not use it on foundation elements (bass, kick, maybe snare, leads (usually)) low elements. Cuz these are foundation, the higher you go the more wide you can go since it's less needed for stability of the track (same with fx, you can go more crazy and more crazy for longer, than in low end where you want to keep it normal or only do crazy fx for (very) short).

Also, you can't even hear the stereo effect lower than 80Hz (and thus slighlty above will be very hard to notice) since the waveforms travel so slow they'll (seemingly?) reach the ears in the same time anway (?).

So yeah, especially in the fundamental of a track (or a sound, so the lower frequencies) you don't want stereo, cuz again, it's hard to explain, but stereo is kind of airy unstable, just like a dubstep bass needs a stable sub bass for a nice fundamnet. So yeah, if you make your bass stereo, there ain't gonna be a fundamnet. So make the main bass stereo, and if you want, and need it (as maybe the bass is important to the track) add a stereo layer (and parallel process wet/dry) them together so you've got some width in your bass.

Same with lead, you'll usually want it mono since you put chords stereo to make room for mono lead (since they both occupy a lot of same frequencies). However, you can add a stereo layer, which is often done, to give some width to the lead. But again, if other elmets, such as percussion and your chords are already wide you probably don't even need that much wideness on your lead and stuff cuz those background elements being wide is really what makes the mix wide and gives the frontal elements depth. Cuz again, if everything is wide nothing is wide.

## Common stereo effects
in general but more purpose one should read the general anaylsis add here tip to download that voexngo and analyze frequency spectrum and check out my analysis shit.

- Beef up mono vocal with subtle width backing vocals
- Slightly beef up lead
- Double/Quad tracking guitar/(backing) vocals
- Ping pong delay

# Notes
## Recording
Recording stereo is since recording is also mono. // Talk here about recording in stereo vs. mono and when to do what.
## How stereo gives width

## Balancing stereo & mono

## Mono compatibility
Talk about what it is, why it is important (clubs, etc.) and how to (generally) achieve it. Also, the problems like phase issues or mud, why the occur and how to solve.
- What is chorus flanger phaser?
- So hyper is just pseudo chorus? why pseudo? And dimension is just pseudo stereo? Like with 4 delays, look in manual: file:///C:/Users/Wout/Documents/Xfer/Serum%20Presets/Serum_Manual.pdf Why 4 delays? Like "dum" "dum" "dum" "dum" what's the benefit of that than just one delay sound?
- The classic âmagic numberâ for unison is 7 Why? I have seen 7 and 5 also? Like with what ratio then?
- Why odd number when doing unison? Cuz it seems then we have a nice voice in the center, which is good for mono? When is even number beneficial? If wanting more detune? (Look up!)
- detune (is detune always harmonic? Can detune be non-harmonic, like not produce 12-TET notes ) used to beef up sound.
- How does reverb give stereo width? Why delay and reverb both for stereo? https://www.musicradar.com/how-to/8-ways-to-use-reverb-and-delay-to-create-super-stereo-mixes
- LCR panning, why so common in rock? Why not just LR panning?
- There is a wahwahwah sound if you left to right pan a sine wave, is that what chorus does too?
- Talk about effects that can cause width.

Also, for each section of production articles whether in depth or not (except general) keep a heading of unprocessed shit where u have a note that is related to an article but u havent had the time to properly write it down. 

So dive into the concept of stereo image and how it is created and how i should care and share some techniques. In the general we can have stereo image tips but just like tips like (do x for a neat stereo fx or do x for interesint panning fx)
!!! STEREO AND MONO !!!
Note that we're talking mono image, stereo IMAGE and WIDENING and not just stereo itself since stereo ITSELF simply means 2 sounds from 2 sources like for example a headphone. If a headphone were mono you would only have a speaker on one ear. Same with mono, it's about centered sound and not "sound just coming from one speaker". You can't have stereo without more than 1 speaker though, that is true.

So, the concept of stereo and mono is pretty simple. Usually in the real world pretty much all the sounds we hear come from a direction and we kind of hear that direction. So these sounds appear in the stereo field somewhere. However, when we play a synth, the sound output is not left or right to right biased. Nope, by default a synth init patch will output a sound that is 100% centered, i.e. mono. This means that the sound will appear as it comes from the center, i.e. one speaker in front of you. However, usually in modern music - to be able to create more lively experiences - we have stereo speakers. In fact, the headphones we wear are 2 speakers. One on our left ear and one on the right ear. Now, why does the synth still sound centered in stereo headphones? Well because the synth outputs the EXACT WAVEFORM (AND VOLUME) (note the stress on EXACT) with the exact same volume in both left and right ears. Our ears and brain will perceive this as mono, centered. Now, this can ONLY happen if the exact same waveform is output in left and right. From the moment that is not the case you will hear some form of stereo width/direction going on. For example, have your synth (or duplicate your exact synth) and pan a quarter to the left and a half to the right. It's the exact same synth but since the right is higher in volume (slightly different waveform due to volume?) you will perceive ur SINGLE synth coming from the right direction more. Now, this ain't really widening like for real, though, it's panning (also widening) and can be really handy. 

Now for real wideness you thus want to create differences in the waveform of your single synth (or layer or whatever). This can for example be done by having a slight delay on ur synth and then panning both to the left and right. Basically your sound will bounce from left to right (so the waveform will be left, then right) earphone but since it's so fast you will not hear the delay but instead it more sounds like a stereo effect as in, sounds comes kind of from around you (which is true since it comes from left and right real fast alternating). This is known as the Haas effect. And though NOT recommended (due to monocompatibility issues - look up precisly what that is) it's still a technique that can be used.

Also, with panning what you could is kind of pan layers (like maybe in orchestra pan a flute and piano or whatever) and kind of pan one right and the other left and let them play the same melody. This, while not the same sound can also give some stereo width.

Now, there are many more techniques but basically you want to have instances of your synth (or a delay of one synth) and have them SLIGHTLY not similar because even the slightest change our ear can pick up. 

Another trick is detuning. Not only does detuning (slightly) give us an interesting phase movement effect, it also detunes a waveform slightly so that when you have the same oscillator and then another detuned osc (for the rest it's exactly the same) or a detune delay emulation on the main synth whatever, you will immediately hear your sound being wider/fatter since now you have two sounds but two slightly but yet the same sound (though note that you NEED to pan the them both so that there is an actual widening since ohterwise you would just have an osc and a detuned osc blasting both 50/50 L/R, need to take advantage of the fact that one osc is very similar but slight detuned to make your sound wider, though some synths might do that out of the box with their detune knob). Now with detuning it's important to not DETUNE TOO HARD (like more than 50 cents) since then the waveforms will be so far apart (like almost a semitone) that instead of wide it's just going to sound like crap. Therefore, keep the detunes under 50 cents.

Example of stereo widening in use could be a clap or snap where you kind of what a center snap but then you can also have different snaps panned more left and right somewhere in this video here: https://www.youtube.com/watch?v=6eCK7wwSGxY nice way to create a thick sounding snap, though you don't want everything wide but with perc like snap,; clap why not.

what should be wide and what not? also in https://www.youtube.com/watch?v=6eCK7wwSGxY this video, though more research needs to be done.

what is M/S EQ and stuff and how it helps in stereo
unison vs. chorus vs. detune vs. flanger vs. phaser

Other techniques to widen your stereo and also WHY you want to widen your stereo and WHY stereo sounds fatter and WHEN to stereo and WHICH instruments and WHICH not:
https://blog.landr.com/stereo-widening/

links:
https://blog.landr.com/stereo-widening/
https://www.reddit.com/r/edmproduction/comments/1i37bh/why_does_detuning_oscillators_widen_a_synths/
https://www.reddit.com/r/edmproduction/comments/9luun3/how_does_the_widening_a_stereo_image_actually/

IMPORTANT PICTURE WHEN PLACING MONITORS FOR CORRECT PERCEIVING OF STEREO IMAGE: http://coremic.com/wp-content/uploads/2017/10/Home-Studio-Monitors-Placement.jpg
of course ain't no problem in headphones unless you're wearing them weird lol.

what is (stereo) flanger?

so i guess the more left or right (or left AND right) a sound ios the more wide???

Chorus is an audio effect. It takes a dry input signal and delays it a tiny bit to create a second voice, and a little bit more to create a third voice, etc. These voices might be panned individually. Then, changing the depth (length of the delays) around over time makes the chorus effect.

Chorus simulates multiple voices given an input signal.

Unison is not an audio effect. Unison refers to the effect of multiple voices playing the same note, frequently with small variations in pitch. You know, like the violin section in an orchestra.

Unison actually is multiple voices.


## Notes
YO PER TRACK DO ALSO LIKE A STEREO AND FREQUENCY ANALYSIS WITH THE VOXENGO TOOLS SO THAT WHEN I HEAR LIKE INTERESTING SOUNDS AND I AINT SURE IF THEY MONO OR STEREO I CAN SEE WITH THE TOOLS WHETHER IT IS ACTUALLY STEREO OR MONO. THIS IS HANDY TO SEE WHAT IS USUALLY STEREO/MONO IN GENRES I WANT TO PRODUCE (OR HOW MUCH).


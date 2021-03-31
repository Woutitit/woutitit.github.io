# Compression, Limiting & Clipping
Note: this article will probably be added to and rewritten the more I learn about compression and have experience with it.

## Table of contents
1. What is a compressor
2. What is a limiter
3. What is a clipper
4. Dangers of compressor
5. Compression vs. volume automation
6. Why use a compressor
7. How does a compressor work
8. How to use a compressor
9. Most common compression techniques
10. Notes


## What is a compressor
So in its purest and simplest form, all a compressor does is reduce the dynamic range of a signal. For example, when we have a certain signal that fluctuates between 2db and 20db loudness, then we can put the signal through a compressor and tell that compressor "Hey, any sounds above x decibels should be turned down in volume". For example, if we tell it to turn down sound above 10 decibels, it will turn down all the sound above that (how much and how fast, etc. depends on other settings we can set). As a result what we get is less dynamic range. If we have hard compression settings this will mean that instead of having 18dB (20 - 2) dynamic range, we only have 8dB-ish (10 - 2) now. Of course, we can go even further and set the threshold at 3dB, in that case obviously we will have pretty much no dynamic range whatsoever anymore.

## What is a limiter
A limiter is the same as a compressor except that its ratio (see later) is infinite. What this means is that your loudness threshold (see later) becomes your ceiling. Rather than attenuating a signal above that threshold according to a certain ratio (i.e. the attenuated signal doesn't have to be reduced below the threshold necessarily), the signal will now be attenuated to always get reduced until it's below the ceiling. The signal in essence gets fully slammed down to where you set the ceiling. This is helpful in for example mastering where you want to greatly thighten up the dynamic range of the whole song in order to increase its fatness and also be able to make it louder. This is unhelpful in being transparent as you often don't want to just slam down all peaks, no matter how high or low, below a threshold which quickly can lead to distortion but also sucking the whole live out of the sound (though for heavy dnb and dub and what not sounds this + mb compression, see later, is what gets used a lot, see OTT) (Also lookup more compressor vs. limiter usage).

Do note that both a limiter and compressor try to retain the original waveform shape as much as possible. That is, it has sort of a look-ahead functionality so that it will actually try to keep the original waveform at the point it should be attenuated but just at a less loud volume/less big amplitude (Of course, at some point even the limiters and compressors can't do but distort the signal in order to carry out the compression). Whilst this is good as that means we can thighten up stuff or make stuff fatter without distortion, it does mean that if we do too heavy settings, the transients essentially get chopped off without any replacement. E.g. in mastering where there is little dynamic range after limiting, the transients of sounds get reduced in loudness close to the the loudness of the body sounds so there is not much distinction anymore between the two. Transients are important though and luckily there are ways to try and emulate or retain them (see Mixing and mastering) but it's something to be aware off when slamming a brickwall limiter like that.

## What is a clipper
A clipper is the same as a limiter but in reality it really means distortion. What a clipper does is also have a ceiling but rather than attenuate a signal, it quite literally chops its peaks of, "squarifying" the signal (= distortion). Of course, this adds (depending on settings) a lot of extra audible harmonic content (because of the chopping of are extra tones vs. smooth curve see Fourier transform article). Because of this reason, a clipper is hardly used to reduce dynamic range in a signal rather it's more used as an fx (such as distorted guitars) but you have to be careful with notes and harmonies (see "Distortion").

**Intermezzo: Clipping comes from the analog days where, if you'd run your signal too hot, the device couldn't handle the input and would start chopping off peaks at the point where it couldn't handle the signal. This clipping was often damaging for the equipment, luckily in digital we don't have to worry about that. That said, clipping still occurs if digitally (see next Intermezzo) your signal is running too hot (which you can't hear) and you then hear it through speakeers which converted that signal, but since it's too hot, the signal will clip. This is what you often hear when mics are too loud or sounds in general like [here] (https://www.youtube.com/watch?v=kU4gIJgmbfk) and [here] (https://www.youtube.com/watch?v=SUDl2lohcv4).**

**Intermezzo: Small note about digital clipping. In the digital world, stuff can't clip (it can but the range is ridiculous thanks to the floating point stuff used, see image line text in sources). Therefore, INSERT tracks will never clip even if louder than 0db. Of course, if that signal does not get gain reduction at any point afterwards and straight up gets send to the master, than the audio will clip since the master is connected to a speaker and through the digital to analog conversion, (see my "audio recording" article) it will clip the audio. In other words, in the digital world, you only really have to worry about whether your MASTER is going into orange (which is close to clipping) or red (which IS clipping and thus distortion and very bad).**

A useful thing about clipping to reduce dynamic range, though, is soft clipping. You see, normal clipping (distortion) is hard clipping and special clipping (saturation) is soft clipping and kind of works differently. Instead of saying "fuck your peaks", it says "fuck your peaks...gently". It still chops off peaks but it kind of does smoothen it a little bit out making the distortion of the wave less harsh and noticeable. This can be quite effective on a master bus because now it will gently distort the highest peaks in your song, which squarify the peaks instead of attenuating it as a limiter would do. A result is that instead of literally chopping of the transient with the limiter, you have reduced the dynamic range by replacing a part of the transients with distortion which sounds like a transient (see intermezzo).

**Intermezzo: It is known that short unprocessed transients in sound kind of sound the same as there distorted counterpart. This is because distortion adds harmonic content (so high-end too which is a big part of a transient) but the sound (or peak) itself is so short we can't really "hear" the distortion.**

In short, a (soft) clipper can be reduced on the highest peaks on your master chain to attenuate the highest transients and replacing them with distortion. Again, you can''t really push it since the distortion will soon be audible especially if it starts clipping more than just transients. However, the peaks thats you CAN inaudibly distorts is essentially a gain in dynamic range whislt still "keeping" your transients (maybe like 0.5-1db). And after that, now you can slam your brickwall limiter on which now has to work less and also can't chop the transients of as much since parts of those are replaced with distortion anyway. Similarly, a soft clipper (or saturator? same thing?) can also be used on individual transient heavy elements (or sounds with high transient peaks, percussion drum buss, plucks) for the same purpose. Again, you can't slam the limiter fully down as it will either distort too much or be too noticeable but for those sounds where transients are important (or integral), this can be a useful technique to try and shave off a 1 or so db without having to compress and or limit. So you'd use this before your peak reduction compressor usually so you have to reduce less peaks (?).

## Dangers of compressor
(Put this at the back?)
Before we dive into how a compressor works I'd want to note that compression itself is a tradeoff. You're always trading of the raw audio quality for e.g. lessened peaks or for the sake of loudness and fatness. In a mix the latter attributes are more desirable but if you'd hear the sound on itself, it does not sound as good as it once did (though it sounds loud). So yeah, it really is finiding that sweet spot where it sounds as fat as you want in your mix (or other things) and where the quality is not lessened too much. 

If you're a bit experienced you'll hear this lack in quality also in a lot of masters vs. unmastered mixes. The mastered mix sounds very loud, louder than the unmastered mix. However, if you'd compare both at a reasonably loud level you'll notice that there are some slight distortions/clipping artifacts going on or that a lot of stuff is being really fat and not really as punchy and pure as in the mix. You'll also often hear that in sample packs where you might hear the audio quality is not decent on a certain sample, it's probably because it's already been compressed to hell which brings out artifacts and stuff. Though, this is not necessarily (though it can be) a porblem as in a mix context, and especially a loud master context, the rest will be brickwalled. So use these samples with caution and if you know they will sound good in the master, else look for some less compressed higher quality stuff.

## Compression vs. volume automation
So you could argue that if you want a signal to be quieter at certain parts in your mix, you could just automate the volume. That's a viable question and in fact, if all you need is to simply have a vocal be less loud in a verse than it is in the chorus, you can do it this way.

However, with compression, we're usually not talking about those kinds of volume fluctuations. We're talking about volume fluctuations that happen in a short, very short and extremely short (1ms) timeframe. For example, take a look at any (uncompressed) vocal sample and just look at all the little peaks at different volume levels here and there. If we were to want to try to make those even in loudness across a whole mix we'd need tens, or maybe hundreds of tailored volume ducking automation levels...just for that single vocal sample already. And while that gives us the most freedom to set it exactly as we want, it's also extremely tedious, time consuming, error-prone and most likely not needed.

A compressor, on the other hand, will automatically detect when a part of the signal is too loud and turn that down automatically. It can do that down to .01ms accuracy even.

## Why use a compressor
So why do we use a compressor? Well, as we said, if you need vocals to be sounding a bit quieter in a verse than a chorus, you can do that with a single volume automation. That's next to compressing. Compressing is more used to even out the dynamic range in a signal. Because, even if you make a sample quieter, the dynamic range, at least relative between the peaks and draughts of the sample, stay the same so you'll need a compressor if you want to squash that dynamic range.

So why would we want to squash (or keep in check) the dynamic range? Well, in a bit we'll see some common uses cases but for example, you could have a vocal sample that might just be sung way too loud in certain parts (maybe certain letters or words or sentences or sections) and thus, if we want the full vocal sample to cut through the mix, we'd want that pretty loud. However, the loud parts in the signal hinder us to put it as louds as we want (usually) since if we'd turn up the volume louder, say to -2dB , the loud parts will probably sound too loud even though now the quiet parts are perfect volume. A compressor will help by making the louder parts quieter so that if we now turn our vocal up to -2dB, the quiet parts will be audible but ALSO the loud parts won't blow our ears out since they get ducked in volume now. Very nice!

Another common usage is to make important sustain elements in your mix fatter and more prominent. For example, if you play a bass or a piano, the initial hit has way more loudness and energy than that same hit 2 seconds into sustaining it. If you put a compressor on it, the initial loud parts will get ducked more to the levels of the quiet part. If you then, through make-up gain (see later) turn up the volume to what it was before, you now have a piano/bass of which the sustain notes seem to ring out longer at the same volume than before making for more aggresive, prominent, fat sound which you usually want for important elements like these that you want to sound thick and not thin.

In technical terms, a compressor raises the RMS of a signal by reducing the peaks first and then bringin up the gain of the full signal to those previous peaks.

## How does a compressor work
https://musicianonamission.com/wp-content/uploads/2018/10/CompressionCheatSheet.pdf

Explain the buttons and stuff gain release attack threshold knee ratio. Attack is not when it kicks in, it's just the time it takes for compressor to reach full potential so with an attack of 10ms, it will already compress before, just only at 10ms it will compress at the settings you told it too.

- Attack: Controls at what speed a signal compresses downwards. You'll usually want this one fast if not instant because you want to catch all the loudness from the get go. Though, one of the reasons to not have super fast attack is when the transients are important and need to be kept (though there are additional/other and better methods to keep those).
- Release: Controls at what speed a signal goes back to normal. You'd want to keep this as slow as possible since a weird signal paired with a fast release and attack might give some weird fast up and down curves (due to rapid volume fluctuations. Though, for instruments that rely on transients you'd still not want the release not too slow to have the signal (almost) back to normal for the next note for the note to have full impact. Too slow release (with a fast attack) might also cause an audible pumping effect if the compression is hard enough (and if instrument strucks chords/notes fast after eachother, then it ducks fast, comes back up slow but in a very rapid manner causing audible pump).
- Threshold: Controls the loudness threshold when the compressor needs to act. It interacts with the ratio a lot. For example a low ratio and high threshold could almost have the same effect as a high ratio high threshold setting. However, rule of thumb with the threshold is that you usually set it high when you mainly want to catch peaks (tame transients). You set it low(er) if you also want to catch the body of the sound (making stuff fatter). You then simply after having decided and set that adjust the ratio to how much it should compress.
- Ratio: Controls how much the signal above the threshold needs to be compressed.
- Knee?
- Sustain?

## How to use a compressor
I'll share some techniques in a moment but if you're using compressors to actually compress stuff you'll usually want to make your compressed signal as "transparant" as [possible](https://en.wikipedia.org/wiki/Transparency_(data_compression)#:~:text=In%20data%20compression%20and%20psychoacoustics,has%20no%20perceptible%20compression%20artifacts.)

In other words, you want your compressed signal to sound like it's not even being compressed at all since then that means your sound is still sounding as it should. Of course you still do want to achieve your compressor goals so a balance needs to be struck between the too.

Generally speaking, setting a slow attack and release will be the most transparant. In fact, set the slowest attack and release and no matter the ratio or threshold, your signal will barely get compressed and even if it gets compressed, there will never be big fluctuations in your sound due to the slow release. Add in a very low ratio, in fact the lowest 1:1 and you have the most transparant compression: no compression at all.

To tame peaks you have two options: a low threshold low ratio setup or a high threshold high ratio setup. The first one will compress more parts of the signal but it will do it gently and transparant (coupled with a slower release time too). This one is great if you have some peaks that aren't too out of line with the rest. So go for this first if you can. Sometimes, however, it happens that your peaks are "so loud" that you'd need to set your threshold so low to be able to preserve the low ratio that will keep your compression transparant whilst also taming the peaks enough. In that case though you might be introducing compression artifacts and your compression might actually sound more unnatural due to these artifacts (quiet sound being audible and stuff) so it kind of doesn't only compress to tame peaks but also to change the sound. In that case it's often easier to set a more drastic compressor with a high ratio but with a high threshold so that it only catches the peaks BUT does immediately chop them off good enough and leaves the rest of the signal unaffected. This is very handy for those "very" loud peaks that would have required too much fidelling. Of course, it's more drastic and less transparant so you'll might have to play a bit with the threshold and the ratio, but it's more effective at taming peaks. So yeah, high threshold and ratio is more effective at taming peaks, however, low threshold and low ratio is more transparant and can be enough to tame peaks. So it depends (?): 
https://ask.audio/articles/how-to-tame-difficult-vocal-recordings
https://www.gearslutz.com/board/newbie-audio-engineering-production-question-zone/1096224-ratio-vs-threshold-compression.html (see one of the first comments that reiterates what I have said)

In terms of attack (knee?) it will also depend. Attack is straight forward, you'll usually want a fast attack (instant to 10ms???) because when your compressing you don't want to miss out on the sudden transients and peaks, the things you want to compress in the first place usually. That said though, you sometimes want to preserve transients and peaks so that's where you put your attack slower so it reaches full potential only later instead of instantely. Usually you dont want to put your attack slower than necessary but also not faster to avoid cutting transients. Of course, the slower the attack, the more transparant the compression.

In terms of release, it's more a debate. A long release is the most transparant but what happens is that, if you set your attack slower too, it will again not fully let out the beginnng transients since the release is still recovering. So while it gives a really steady sound, it does suck all dynamics out of it and life basically. A fast release, however, is very noticeable and can cause a pumping effect due to the signal going from compressed to suddenly not compressed (which might be a sudden volume change) to compressed again which happens often since a sample, like a snare, has lots of little dynamic changes which then get accented by the short release. Of course a long attack will make it so that the release does not have too much to release too, but a slow attack will, again, not compress too much. So, as a general guideline, for example, in case of a snare or kick or anything transient heavy, you'll usually want your release slower than whenever the next time it hits since you want the full transient of it (and let the peaks be handle by a different compressor see later in techniques) but you also don't want it too fast to avoid too unnatural dynamic changes and pumping effects. So yeah, depending on the sample, sound, loop, etc. you have to hear what setting.

## Most common compression techniques
(Note: this section needs to be added to/changed until I learn more about compression)

There are tons of ways of using a compressor, whether that is how you set its settings or how you use/chain it in your fx chain, but here I will try to cover the most basic and common use cases for compressors.

### 1. Taming peaks
The most common and basic use of a compressor is to simply tame loudness peaks. The reason we often want to tame peaks is because, in the case of for example a vocal, we want it to be on a normal volume level. However, due to the loud peaks this is really hard to accomplish because on a normal level these would blow your ears out. If you'd then try to turn down the volume of the vocals we won't have our ears blown off in certain parts but we will now not hear the vocal that was okay in volume at first loud enough. The solution is to tame the peaks which allows us to stay at the same volume, but since the peaks are reduced, we will never get our ears blown off.

The settings for this compression is usually very gentle. You'll want to make sure to only catch the real too loud peaks and leave the rest of the signal alone as to keep the sound as natural as possible. In other words, set your threshold to the higher side of things. Also, since peaks are often in transients and short, we want our compressor to catch all of it so we'll want a fast attack too.

As I've just said, since this compression is really gentle and only used to catch peaks, it's extremely versatile since the gentleness of the compression will never make your sound suddenly sound unnatural, weak, overcompressed, etc. This is why you could basically throw it on anything, whether that is one-shots, loops, vocals, guitar, piano, busses, etc. Everything can use some peak compression, even the tiniest almost unaudible bit. For real though, you can often look at the waveform (or render MIDI) out to see if it really is necessary to tame some peaks here and there.

### 2. Bringing out body/sustain/fatness
Ok. This one is also very common but you need to be careful with it. Basically, this type of compression is used to give more "umpf" to a sound. It differs from the previous compression technique by actually noticeably, not-so-gently, compressing the signal. Again, nothing extreme, but enough to actually bring the dynamics closer, that is bring the transients closer to the body of the sound.

For example, with a kick sample, you can use this type of compression if you want more body in your kick. That is, the transients is now quieter while the body of the kick is at the same loudness, result is that if you now turn up the volume again to at what it was peaking previously, you'll hear the same loudness but with the same body since now the quiet part of the kick is actually too. Same technique can be applied to bass, or piano where you'll usually want to add a bit of this to make the sustain notes ring a bit longer which adds more stability and overall fatness to the sound. With snares, just like the kick, it's to bring the body more out again.

Settings for this are a little less straight forward. Usually you'll want a fast attack to be able to squash all/most of the signal so everything gets reduced in dynamics. The threshold and ratio also depends on how much squashing you want to do and how drastic you want it to sound. Usually the threshold is lower and the ratio is higher than with peak taming.

Also, while this one is fairly safe to use on one-shots or a sample with only one instruments, it's a bit harder to get the results what you want on loops with multiple elements, busses, etc. This is because there are all different elements at play and you'll probably not want the same compressor settings for these elements. Add to that that your compressor settings will definitely be audible and you can end up with something that sounds unnatural, overcompressed or bad. This is not always the case and it depends also on how drastic your compression is, but yeah, this technique is way easier to do on one-shots and single instruments since you can tailor your compression to that one single thing.

A last thing also. Often, this technique will also reduce/squash the transients. To preserve that, you can make your attack a bit slower so the transients still come through whilst the rest gets nicely compressed. And bonus tip, since this might mean that now your transients are too loud since they are not compressed, you can add a peak tamer compressor (commonly done) before this compressor to tame the peaks. This way you get the nice "umpf" without losing transients AND your transient peaks will also never be too loud since they've been shaved off slightly already preemptively.

### 3. Parallel compression
So then there is parallel compression. This one is also used to give more "umpf" to the sound but usually used more on (drum) busses (even the master) and loops and stuff since it kind of remedies the problem we had with the previous example where compressor settings might not be ideal for multiple elements. With this compression technique we can give "umpf" while preserving the natural sound and dynamics of our sound regardless of whether it is a one-shot, a loop or a buss.

What we're gonna do with PC is basically compress our signal very extremely so that ALL dynamics are crushed. What this gives, is depending on the settings, a really aggresive and possible even distorted forward sound with absolutely no dynamics at all. Now, of course, if we leave that compressor at 100% wet our sound will sound like shit but basically, again depending on the settings we mix in basically only 10-30-40% of the wet of the compressor with our dry uncompressed signal. As a result, what we get is the extreme energy, stability and fatness that our overcompressed signal gives mixed in with the totally preserved dynamics which we have not compressed at all of course. So if the sounds sounds too aggressive and unnatural, simply turn down the wet until it gives "umpf" yet sounds natural. And as you can see, no more messing with ideal compressor settings, you just set all to very aggressive (depending on what you want) and then simply mix in to taste.

Again, since we do preserve the natural dynamics, there might be some peaks here and there so yet again we often first do a gentle peak tamer compression to only then feed it to our parallel compressor to give it the energy it deserves.

As I said, this one is often used on (drum) busses or loops since it remedies the compressor setting issue we had to bring energy to stuff but also because the elements together also make it so that our compressed signal contains a lot of energy. With signal instruments, or a one-shot there is only so much PC and overcompression of that one thing can bring out (?). That said though, you can definitely use it on piano and bass too since these are also very dynamic instruments by nature (especially slapp bass) so this could add some extra life to those things too. Same goes for one-shot drums. But yeah, usually if your just after some extra body on a one-shot or more sustain on a single instrument, then you can be fine with previous compression technique I'd suppose.

### 4. OTT compression
This one I kind of have yet to figure out when to use it but basically it's sort of like parallel compression (like parallel is upward compression but in downward way or something) as it is downward and upward compression and with different settings for each frequency band (so MB-compression). However, it's "over the top (OTT)" so it really crushes the dynamic range and thanks to the upward compression it can bring out very low high frequency noises that downward compression only wouldn't bring out. That's why it generally sounds as if it makes a sound more bright and aggressive, due to the higher frequency content being added/louder.

So this one is used to, just like PC, to bring out life out of an instrument, piano, loop, whatever. You can basically use it on anything and it can sound brighter and more lively. Whether that is what you want is another thing. Again, just like PC, you want to dial back the wetness to 10-30% usually only and even less if you use it on busses. EDM producers often use it on their leads, basses, chords, drums, etc. to make them pop out more. Of cours, you'll very much lose your transients with this so you'll want to dial back the wetness as I have just said.

So yeah, when to use OTT? Well, I have to do more research but usually in EDM and on synths it really sounds good and makes the stuff brighter as it adds more highs to the signal mainly while keeping the lows and mids more stable. It can be used sparingly on drum busses to make them more energy and even slightly on the master to brighten everything up a bit. Again, I have to do more research but in an EDM context I would always try it on the main elements and see how it fits. And on the drum busses, or other use cases for PC i'd try both OTT and PC to see what's best. Sometimes they kind of will sound similar obviously. Sometimes PC sounds better other times OTT. I also feel that PC will stay more true to more naturalness than OTT will, so on actual instruments that you want to sound real maybe better PC than OTT? Again depends on genre, maybe in house where you don't care really about dynamics in piano, you can squash it with OTT too as I have seen some do. Again more research here.

### 5. Bus compression
It's not really a technique but mostly it means you'll compress on the master, or you'll compress on instruments routed to a same track such as your drum kit. This one is used mainly on drum busses or on layers of synths and bass in EDM. This one is used to save CPU sometimes. That is, if there are certain compression settings that can work for your whole bussed sound, no point in applying individually. However, this is most commonly used for "glue compression" (using a glue compressor). The reason it glues things together is again because we're going to reduce the dynamic range a bit, tame some peaks and so in general make the loudness of all sounds more uniform and equal. Again, you'll usually want to use really gentle settings (maybe even the glue compressor plugin, what does it do?) to not introduce artifacts due to your attack and release settings. But yeah mainly just glueing your sounds more nicely packaged together so they sound more coherent, coming from one singular source (cuz having some hats be like louder than snares or whatever may make it not sound as though it's coming from the same drum which is not what you desire).

### 6. Serial compression. 
We already touched upon it, it's basiclaly putting compressors in series to do things rather than letting one do all the work. Very common used in the scenario of taming peaks and then adding umpf but can also be used in other cases. Basically, it's best practice to always use compression settings as gentle as possible and give each compressor basically one job and let it do that job good. Same as with EQs.

### 7. Multiband compression
https://www.waves.com/multiband-compression-beginners-guide

With MB compression you are able to target a or multiple BAND(s) of frequencies of a sound rather than all frequencies with regular compression. This can be handy for more surgical compression. A common scenario is for taming a lead, or a lead bus. Often, we want leads to sound bright so we don't want to cut too much highs (maybe a shelf or low pass at a very high Hz treshold but that's it). However, often in all this brightness the lead (or a lead layer) sounds too harsh in the 4-5k area (usually), especially if you have multiple lead layers (and these frequencies make our ear hurt) as there will be some hurtful resonances (as our ear is sensitive to those high Hz we can hear well and are more than just hiss as the really upper range). Our lead is fine for the rest but we just want to tame some resonant or loud frequencies in that area. We could of course notch out those Hz with  narrow EQ cuts (though if the lead changes pitch often these cuts are kinda redundant) and/or we could use something like the soothe plugin and this will work fine but if it doesn't or if you need more (or you are too lazy to do surgical EQ) you can use MB compression specifically around that range. It will then compress all louder/resonant frequencies in that area whilst for the rest keeping our lead the same keeping those harsh and loud frequencies in check. Also, when our lead changes pitch it will keep compressing at all the new areas where build up is happening rather than with EQ cuts where its set to stone (dynamic EQ though? Is that soothe?).

So what is MB used for? Regular compression, OTT compression an dynamic EQ. Basically if static EQ ain't working for you, since maybe sometimes in the song the highs should be more or less pronounced than at the point you put your static EQ, it can be handy to have an MB that can manage the loudness of bands, in this case the highs, and more carefully attenuate the highs or attenuate the lows if necessary. This can help on the master to make your mix less muddy or too harsh (?) since if done correctly it will turn down lows and turn down highs when needed to. OTT compression, we touched on and regular compression is just if you would like to compress your signal but for some reason you'd want different settings for each frequency band. I see this a better fit already for loops and stuff because you can have at least already different settings for different frequencies.

Also, as this article: https://www.waves.com/multiband-compression-beginners-guide states you can of course use it on your master because it allows more control meaning you can compress some frequencies while leaving others alone which might improve a (bad) mix.

So yeah, anyway, these are just the most common cases. You have to watch some tutorials and livestreams to see how these cases get used but also more advanced cases (especially how EDM leads get compressed and when they get compressed). So again try stuff out, use references, try to match them using the technisues, watch livestream, etc. I've got a general idea, but need to know better still. And then also watch EQ tutorials about taking out resonants best practices etc.

## Notes
hard vs. soft limiting?

## Unprocessed notes
## Compression tips
Usually bass is what needs the most heavy compression because it's very dynamic (ever heard a bass play in the lows and just play one octave higher? The loudness increase is massive and thus needs to be more stabilized). Look up more.
https://www.reddit.com/r/edmproduction/comments/a2qsk8/do_people_actually_know_how_to_use_compression/eb0gakg?utm_source=share&utm_medium=web2x&context=3

## FAQ
### EQ or compression first?
It depends what you want. Also sometimes you want to do both. Sometimes none. TODO!

## Common compression techniques
transparant compression? What does it mean for you compression to be natural and transparant. like slower release more transparant?
## Parallel compression
So parallel compression basically works like this. You compress
So add here and say it's mostly for stuff high transient and high energy we want cuz preserve transient AND add the punch and fatness of high compression. So drum buss also rear end compression or whatever is called new york compression on full master.

### Serial compression
### Bus compression


## Common compression uses cases



## Common compression mistakes
Link izotope article, talk about compressing already compressed samples.

## Advanced Compression: Multiband and OTT
so, compression with slow attack after ott to get some transients back if we need it since ott made our stuff bright which is good but in the process squashed the dynamics and thus also the transient.

## Different kind of compressors
so people use different kinds of compressors, especially analog ones cuz they add stuff other than compression cuz they aint perfect. Like saturation but also all compressors analog add different kinds of saturaiton/distortion. Or sometimes u want sterile and u go for digital. Or u have "fast" and "slow" analog compressors too like 1176 and then L2 something analog ones which are handy for serial etc.

## Digital vs. Analog compressor
## Compressor for bigger RMS
So we use a compressor in essence to get more RMS at the same peak, essentially meaning we have a louder fatter sound at the same peak. Since these peaks are brief they don't add much to the loudness but can still be tedious when turned up. So for vocals, bass sustain, etc.


## Why use a compressor
// TODO: This section will need more work.

There are a lot of reasons why one should use compression but one big reason is to tame peaks. For example, we might have a vocalist that tried to sing the chorus as loud as possible but we do notice that some words or very brief sections are too quiet. Well, then we can just tame the peaks with a compressor


## Common simple use cases for a compressor
So, a vocal is a very c


## Unprocessed notes
so compression/limiting when? Only on master? What goal for limiting on master? Master mastering jonas aden for compression chain and all their functions? Soft clipping? but more in mastering notes.

So protip, just as with eq, try to work in stages. Dont just use a single harsh compressor to try and perfectly shape a sound. Nah, first use some gentle compressor that catches peaks. Usually high threshold as it only works on peaks then, fast attackish so it catches peaks, but again not going to crazy. Then in next compressor if u wanna beef up sound u can do some PC if u want or you can if u want do a compressor with slow attack, preserving transients and try a bit lower threshold to squash sound more in order to keep transients in tact BUT get more beef.

why does release depend on speed tempo BPM of song?
eg release shorter than time between snare hit cuz else of course ull not get the transient of the snare hit fully sine signal at that point not recovered to original state at all, so it don't matter that u set slow attack to catch transient, it wont ring out anyway cuz release too slow. Release u also don't want to set to fast cuz...
see this comment to calculate release basically dont want too fast but never slower than a hit of ur shit?:
http://forum.cakewalk.com/Compressor-settings-just-to-catch-peaks-m2004280.aspx#2004328
others say u dont need to set to bpm eactly, it more or less dictates max release setting, anyhting longer might be bad but anyhting shorter might be good but not too short cuz...?

so in general u want to set release as short as possible without introducing pumping, how can that be introduced tho:
https://www.uaudio.com/blog/audio-compression-basics/

Also reason that a very long release and low threshold seems most compressed is cuz u compress initial signal and so that ducks to below threshold but since threshold so low everyting (fast attack) will duck but signal will never briefly go to original volume, even if for microseconds (as the case with fast release). It just stays low around the threshold the whole time and only gradually turns off (goes back up to original signal which is louder than the compressed signal since our threshold is way below the decibels of our original signal of course, as is the case with downward compression) when the sustain is dying more and more out since now you'll have more and more sounds below threshold so compressor gets more and more time to actually get back up to original signal level.
 If you're not sure if there are any harsh spikes then render the track to a waveform so you can examine it visually, check the clipping level on the meters, or use a spectral analyzer. Sometimes spectral analyzers aren't always accurate or fast enough to reveal spikey transients: https://www.reddit.com/r/edmproduction/comments/3fhhh4/compressor_when_should_slow_attack_slow_release/ so like if u aint sure ur shit needs compression or ur transients might be slightly too loud (or could be slightly quieter in order to brin overall lvl up) just render ur midi to audio for a sec (cuz spectral analyzers aint really that great to show peaks and shit sometimes).

why distortion/clipping when short attack AND release?

so in fl limiter if u want ur limiter part of the plugin to not do shit just put the ceiling on most high (or leave at default). Same if u only want limiting and no compression, the threshold can be turned off if in middle and it won't do shit all your settings. Also dont forget to turn of ur sustain either so ur in peak mode cuz else it might not compress at higher threshold and shit. Also check manual fl limiter about cuz one is pre limiter and the other post limiter pre compressor (or??? see manual!).
short attack and short release u can basically see that the compressions is kinda colored in cuz the release is immediate and since probably on micro level there are so many times where ur like, ok this is below threshold so immediately release but oops this is above so immediately compress so it just goes up down real fast, also thanks to the super fast attack.

so yeah as a side note with my plucks and big transients, the reason they help "cutting through the mix" is cuz they are short bursts of sounds and as humans we don't experience these sounds the same loud as we do with sustain sounds. For example, a short pluck at 50dB might be manageable for our ears but a sustain chord of a second of a piano at the same volume will be overwhelming and probably just loud. However, it's common practice to emphasize the 1 beat (or 2 beat) or certain notes/chords/places/whatever. We can do that with just a sustain chords but even better if we layer it with something more plucky like a hard-hitting piano. That short birts of dynamic range difference in the begnning will make us really hear all the starts of the chords very clearly whilst still not hearing like it sounds too loud since the sustain chord is still at the same lvl (while maybe the pluck is at a higher level). This is the same with a kick. You want to layer a transient heavy kick with a heavily compressed kick (or compress so that transient remains in tact) so then u still keep that beginning dynamic range of ur kick which is important to cut through the mix. Similarly as a small boost in the highs helps since again, even if it's not louder in decibels we perceive higher frequencies as louder too. So yeah that's why transients and plucks are important with stuff we want to really cut through the mix. Thos are usually the important front elements such as lead synth, kick, chord pianos (with backings we can be less careful of course). Also, stuff like vocals transients might also be less needed since yeah we can feel that a voice naturally aint really meant to be transient heavy in the first place. On the other hand, piano, especially hard hitting ones are transient heavy and to preserve that (of course we can still tam if too much transient) we'll thus want our attack to not be too fast (or do PC). so yeah transient in beginning of sound cuz thats on the beat and thats where we want a big one, else, less important.
also take in fact that pluck u can put at higher frequencies or are generally higher freq than sus so they dont even need to be really louder than the sust chord (can be even quieieter even if not high freq?) alsoi sust chords have purpose to fill up mix, transients an dplucks to cut through and give energy and live to a sound.
See: https://www.reddit.com/r/edmproduction/comments/4i9ovb/attack_and_release_on_compressors/d2wmh8y/?utm_source=share&utm_medium=web2x&context=3

but also depends what pluck u layer,like layering a hard hitting piano with supersaw can work but of course they both have bodies so u kinda need to mix them well cuz else simply too loud, so mix so u can hear transient of piano well and adding to mix but then make it so that maybe the chords of supersaw and the body of piano aint too loud.


peak compression vs rms compression?

so eq for harsh sounds, instead of compression or MB compression cuz in the high band its loud? but like harsh sounds, cuz we are more sensitive to it we PERCEIVE as louder which is why even tho it aint much louder, it may sound too harsh for us, so compressor wont do shit for that of course

whatt are transients really and how can u emphasize transients with compression?
and why do that for kick/snare?

why do we perceive big transient as louder lick a clap than a hum with low transiet (cuz hum kinda equal energy) or not louder?

Is it just that it's like something high energy, for short periods so that it doesn't take up much space in mix but when it
hits it does cut through cuz we can put it louder than sustain sounds since it's very short. This is i guess why plucks
and adding transients (with plucks) because it takes very little space headroom which gives us the advantage of putting it at
higher volume then sstain sounds (so like our actual chords) since if these sustain sounds would go at at that loudness
all the way through, the mix would just sound too damn loud compared to the drums.

u want the beefyness fatiness that compression brings especially if you have few elements, this is kind of like good practice
anyway to have sparse (or as sparse as possible) mixes so u can have even those few elements be big.

So reverb and delay can kind of simulate room, so why they make sounds seem further apart and/or in a space why does that sound
more natural and better to us. Why sounds with same reverb sound like in same space. Why even imortant to put sounds in (the same)
a space.

"taming"

different kinds of compressors? analog vs digital compressors? 1176?

So in this way, actually strumming all energy full can actually sound as loud as you just strumming it quietly if you set the treshold very low since the all out strumming will then be lowered to the point where the quiet strumming happens. Resulting in both being equally loud. Of course you need to do make-up gain to have it the same loudness but yeah, thats cool. Now, do you want that? Well perhaps you would try to intially not have too much difference in loudness, and also perhaps you dont want the loud part to be that much squished either to still have some dynamic difference between the too. Depends on the track, genre and your use case/taste.

listen from 8:30 onwards, makes good points: 
https://www.youtube.com/watch?v=RfHA4OPfoi8

Cuz a fast attack (but not super fast) makes the compressor reach fully energy a bit slower so what that means is that it allows the initial ms of a signal to not be compressed...so yeah the transients! This can be handy in funk guitar where you do want your intial transients to be heard, and as we just said, since these are plucky short energy things they can actually be substantially louder than your other part of the track. (I guess we even see that in masters where on the kick  big transient we always see a spike? have to see that in one of the project files). Again,

serial compression, very common to first compress to tame peaks with slow attack/high ratio? and then to keep some transiets to compress that signal but basically with a fast attack. What happens in the second compressor is that indeed all of the signal will get compressed (since the first compressor alraedy squashed the dynamic range) BUT by putting a faster attack, and low treshold we can actually sort of "sculpt" our transient back in since the first part wont get lowered to the treshold but the second art will. Darn, where did i read that? Google serial compression!

"gain reduction"? and how much? -6db? and where? Is that on master? or?

https://www.musicradar.com/tuition/tech/how-to-use-serial-compression-628804

The order in which other effects are placed can also make a huge difference to the results. For example, reverb placed before compression can give a source sound that 'compressed room mics' sound, whereas placing the reverb after the compression will give a less 'reactive', studio-style sound, since the reverb itself won't be compressed. How about EQ? Boost the bass before compression for a rhythmic pumping effect that can sound great for kick-driven music such as house or techno, or after for 'clean' bass boost without affecting the compressor's action.
=) so yeah i have to do this in fl studio, like eq vs compression (first) and look why in bass (and then bass) boost and then compress why u get the pumping effect (that u may want) and why boosting bass after doesn't gt you that? So why low freqs cause that? Cuz loud? and what attack release on compressor?

why do parallel compression instead of normal compression, just like parralel processing (which is for fx, like delay and reverb???) you do PC on a copy and u compress it hard, and then u can dial in the wet hard on original uncompressed signal and choose how much little compression signal gets. Why keeps more energy than nrmal compression?

also compression or eq first in general, what do both achieve, like i guess eq first, ike a roll off usually good, no harm and maybe better, like, if we don't need the frequencies anyway, why even have them in our compressor where they might fuck up shit cuz maybe cause ducking, even tho we eq the freqs out that cause ducking so have ducking in parts we dont want???

This has serial compression answers:
https://theproaudiofiles.com/video/pro-mixing-tips-serial-compression/
https://musicianshq.com/audio-compression-explained-beginners-guide-to-compression-in-music/

So with this theory in mind, a general rule of thumb put a fast compressor before slower compressors and higher ratio compressors before lower ratio ones.

compressor vs saturator and why use saturation as form of compression, i guess cuz add harmonics so makes overall sound on freqs more even? or why use saturaiton with/before compression??? or after???

Serial compression reason:
https://www.reddit.com/r/audioengineering/comments/em65nj/why_would_parallel_compression_be_any_different/fdmlp9a?utm_source=share&utm_medium=web2x&context=3

how to know if master (or single track) over compressed. How to know if compression want/is the answer. Like, in jazz we dont want it for lot of stuff, why? https://www.audio-issues.com/music-mixing/jazz-music-mixing-tips-for-beginners/#:~:text=Compression%3A%20Not%20necessary%2C%20most%20snares,the%20dynamics%20might%20be%20lost.

classic example is throwing in a fast compressor such as 1176 into an LA2A

digital vs. analog compressor?

 YouÃƒÆ’Ã†â€™Ãƒâ€šÃ‚Â¢ÃƒÆ’Ã‚Â¢ÃƒÂ¢Ã¢â€šÂ¬Ã…Â¡Ãƒâ€šÃ‚Â¬ÃƒÆ’Ã‚Â¢ÃƒÂ¢Ã¢â€šÂ¬Ã…Â¾Ãƒâ€šÃ‚Â¢ll get a more natural sound by applying light compression with multiple compressors than you will by applying heavy compression with one compressor =) why??? https://www.blackghostaudio.com/blog/the-ultimate-guide-to-compression

Why not compress for jazz mixing?

also important, HOW to setup parallel compression in FL studio!))))) so send a track to a track and then let track return shit?

so we need to route the track we send to the track we send from so if we send from 1 to 2 we need to then route back to 1? Is this how we do it with reverb too so we can have a single reverb effect we can then send multiple tracks too for consistent reverb application and also for less cpu use? or???? Or do we need a special "return/send track" instead of an "insert" track. Also unroute the 2 track from master.

In a parallel setup, the signal is often compressed much heavier than you normally would as an insert on the channel. As an insert, average compression would range from -3dB to around -10dB before smashing all dynamics. In a parallel setup, compression can range from -3dB all the way to -20dB and above

So yeah, in PC you basically overcompress ur copy (overcompress? i mean at least very heavily compress) and then u dial in wet/dry and mix with original signal. So you "mix" two signals together? Or is it literally playing two signals together and then ride volume fader?

so PC very common for drums. Why? Cuz PC is transient preserving and on drums we want to preserver transients. Why not same with  compressor with slow attack on bus? or on individual tracks? gotta try this in fl tomorrow PC vs. regular compression.

So wouldnt we use PC for everything if it adds the energy? Or not necessary for other stuff, like certainly not for sounds that aint that important as the drums (or in the background) or where the transients aint that important or there still can be life with normal compression.

!!!!!! https://vintageking.com/blog/2017/10/what-is-parallel-compression/
so with PC we can squeeze out some more RMS since the signal is very heavily compressed so yeah, we can add energy to our uncompressed shit and normal compressor, the problem is we cant set it too hard cuz else we'll squash dynamics but then we lose energy so yeah. Gotta try out.

but also again be careful with PC cuz maybe in addictive drummer 2 (if stuff aint compressed) it can be handy but most samples are alredy compressed anyway So ur drum bus might not need it want it anymore or its gonna be overkill. Why is compressing already compressed samples bad? Why/How is that overcompression? What even is overcompression? like wont it just turn down the volume of the stuff if compressed already like np with fast attack and release right? Look up!

is the dry/wet know of an fx not PC? Or is that different? dry/wet vs parallel processing?

so parallel processing, not 100% if exact same, u can do by actually putting ur effect on the same track and simply turn on or off the dry/wet knob. So like do overcompression, real hard, and then turn that to whatever lvl it needs to be at but do it on the same channel as you were. So you dont need to mess with routing and stuff. However, doing PP on different track allows more control as in multiple tracks can be send to it but also like u can have 100% wet level of compressor and then dial that in. Miht be more control. SO yeah it depends, also, PP on same channel might cause some phasing issues (i guess with PC) so if you notice, then put on seperate:
https://www.reddit.com/r/edmproduction/comments/1lheem/drywet_compressor_same_as_parallel_compression/
https://sound.stackexchange.com/questions/22043/what-is-difference-between-parallel-compression-and-dry-wet-knob-on-compressor
https://www.gearslutz.com/board/newbie-audio-engineering-production-question-zone/1266024-compression-mix-knob-exactly-same-separate-track-send-parallel-compression.html
https://www.reddit.com/r/edmproduction/comments/3kgq8y/question_about_parallel_compression/

so PP on aux gives more control (in terms of wet levels can be 60 60 and doesnt have to add to 100, see first reddit link above what does it mean) and flexibility and saves CPU and will not give yo phase issues.

also as last reddit link suggests, its not cuz u do PC that u cant compress signal before too. Like regardless of making ur drums lifely and punchy, u might still need to keep the transients in check cuz still too loud in comparison. So u compress first those a bit, when sound is in check, but not too much so it keeps its dynamics and detail, we can then do PC which brings punch and energy.

so really need to like do an addictive drummer pattern and try out PC vs regular compressor with an attack that keeps transient
but compresses the fuck out of the rest. My guess is that PC will be more natural, again, cuz we keep our original signal and all we do is add to that some heavy ass compression so we retain clarity and dynamics (do we retain dynamic range or not?) while gettig punch. I guess with regular compressor less natural but similar?

So why not always use PC? I answered already above or below, but i guess cuz sometimes not needed. Depends on sound source.

so PC is form of upward compression tho sound on sound said both upward compression and downward. Why mostly use downward? upward vs. downward? When to use what? Why does OTT use both to achieve its overcrushed sound?

eq resonan frequencies how to take out and hear 'em.

Hot Tip: EQ the compressed signal. Try putting a High-Pass Filter on it. This lets your dry signal be the main source of low end. from the articleof landr below, so yeah another reason to put PC on diff track cuz u can do that and so make ur original signal main provider of low-end cuzzz???

why do some compressors add saturation? is it before or after compression?

like the guy from yt vid linked here says he compresses clean guitar before overdrive to control clean and only then overdrive that signal. Why not overdrive/saturation before? and do compression then again or?

MB comression? vs dynamic EQ?

So one dude says that PC better to preserve transients cuz with slow attack and then compression kind of hard of the rest i guess you'll have more weaker smaller sound cuz of it. Again, we should test it But im guessing c more natural anyway. And maybe its indeed a bit hard to put the slow attack just right to preserve transients BUT to compress rest, wih PC dont need to worry about it since we preserve dynamics of everything anyway. So again why not always use PC: https://samplesfrommars.com/blogs/tips-tricks/17081303-use-parallel-compression-to-achieve-punch-fatness

nice overview of common compression mistakes:
https://www.izotope.com/en/learn/6-parallel-compression-mistakes-in-mixing.html

so again, compression, just like eq, you need to do with a purpose. Like not everything in ur mix needs to be fattened up or tamed or whatever (like background elements in an aleady busy mix, cuz, dont need to add another busy compressed element to that, or already compressed drums or whatever).

so on dynamic stuff, real stuff or transient heavy stuff (which is dynamics basically) ull want to especially PC cuz yeah u preserve ur dynamics but u can add punch:
https://www.izotope.com/en/learn/6-parallel-compression-mistakes-in-mixing.html
Like on synth sounds it would be more uselss cuz these of course tend to be less dynamic since its programmed cimputer sounds coming from the same synth instead of real/sampled/real players with dynamics and velocity shit where ud want the dynamics preserved.
https://www.reddit.com/r/edmproduction/comments/9ookfg/parallel_compress_everything/
So again, even then, not all dynamic live elements need PC if ur mix is especialy already crowded. Cuz then just gonna sound over the top, hard to hear, and just too loud and again lifeless everything. So be tasteful.

so in PC the compressed signal also has 1ms attacck i suppose to fully squash range right, that's the point to get the full punch. Of course, maybe not full 1ms if that makes sound too weird or whatever.

So how does mixing dry/wet signals work is it adding two of the same waves or?

Like normal compressor used if u just need to tame a signal and dont necessarily want to make it or need to make it fatter. Thats one case. Or when ur signal isnt very dynamic and/or it aint that important to preserve transients (cuz maybe u have a pluck layer anway, or another reason) like soft synths???

best since it can help you produce an invisible form of compression
https://www.tunecore.com/blog/2018/05/parallel-compression-a-powerful-technique-in-music-production.html
so again more natural form of compression cuz it keeps natural sonic info in tact so again why still se regular comp? i mean looook article maybe

in beginning when they did pc they had to have diff track cz no dry wet know now with digital its easy cuz we have its

Nice use cases for compression and which types to use:
https://blog.landr.com/use-compression-solve-5-common-mixing-mistakes/

So this article is about all kinds of parallel processing (from compression to reverb) and why it can be handy and easy and better to do these things in parallel:
https://www.izotope.com/en/learn/5-ways-to-use-parallel-processing-in-music-production.html
so PC handy to add overall RMS, energy and power. And also to have natural compression cuz the natural dynamic stays intact, it's just that we mix it in with a heavily compressed signal which thus adds body and energy:
https://vintageking.com/blog/2017/10/what-is-parallel-compression/

Of course not at 100% cuz then you'll have an overcompressed signal, do it with taste. Look up how to parrallel compress drums.

which elemnts need same reverb? or almost same. Like, i guess background elements, and especially pads and atmospheric stuff (that need to take up a lot of heardroom to fill all the empty space) need a lot of reverb.

so to keep transients u want slow attack but also not too slow cuz u still want to compress the rest so u can do makeup gain and have overall sound louder and if transients too loud then u can modify attack of course to taste.


Common compressiong things:
Peak compression (?) for bass to give it more sustain and thus more/stable/longer low-end.

Also somewhere make a list of general stuff used for what like general plugins

like OTT, used in x case x case and x case, or for this very particular sound, can also chain if u want

OTT

compressor vs static eq vs dynamic eq

Fast attack on drums and plucks but not too fast cuz u do want the transiet like dynamic range of that

other uses cases?

Compressor to get more sustain out of sustained/legato sounds such as piano,

don't compress already compressed stuff (why not)
often, drums from reputable sample packs are already compressed, but you can see that already if overally the transient has no dynamic range and the body seems to also 
be relatively loud too if its completely rectange, it's been compressed to dead, probably sounding huge, but yeah, maybe not a transient anymore though and maybe distored

why clipping with compression?

so compressor can be used on master for overall track loudness, on individual sample for individual loudness of that instrument, on any other level? Like buss too, for glueing i guess?

limiting vs. compression? compressor vs multi band vs ott?

so compressors used to raise overall RMS but keep same peak (after make up gain of course cuz compressors turn down signal but have a know to do make up gain)
Also, the meter, or the wave in FL studio compressor show how much it compresses, it starts right and then if compresses will shock to the left as you can see to a certain negative
value. That's how UAD compressor works at least. Or it can start in the middle and if u use expander, the compressor can go to right which means it expands the signal there (?)

OTT explained, both upward expansion and downward compression? Why? Why make stuff brighter?

expansion vs compression? Compression easier and cleaner. Just like how cutting is better than boosting.

play higher notes with your bass that the gain tends to increase. Like in a sub or with a bass, suddenly if u player higher notes (like with funk you often have that technique, look up funk bass techniques so i know the names) the gain is much louder than it was just playing lower. So a compressor can help there to keep the gain in check (instead of having ur bass player needed to play softer there). On a bass, compressor can also, again, serve to make sustain notes sound longer and more pronounced. Like that one

bus compression? glue compression? How different from normal compression? https://www.blackghostaudio.com/blog/the-ultimate-guide-to-compression

different kind of compressors?

So why EQ the low end/roll off before compressing? Cuz low end can cause rumble in the compressor? So why not eq out after? More clean to do before? Look up

as sound design

serial compression?

parallel compression?
allow us to raise rms??? like overall loudness of a sound
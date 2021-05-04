# Sidechaining
So this article could go into the "Compression" article since sidechaining is often known as sidechain compression. However, since sidechain compression is only one way of achieving sidechaining (though some say it's the true way) and since the subject itself is big enough I made it a seperate article.

## Table of contents
1. What is sidechaining
2. Why sidechaining
3. Sidechaining as FX
4. Sidechaining as a mixing tool
5. Techniques
6. Notes

## What is sidechaining
So sidechaining simply means that you're lowering the volume of a certain sound based on another sound. So if a bass and kick hit on the same beat, if the bass is sidechained to the kick, then the bass will briefly duck in volume to let the kick play out and then at the tail of the kick the bass comes back in full volume.

## Why sidechaining
We sidechain for two reasons:
  - To make kick clearer
  - Gain more headroom

The bass and kick hit very similar frequencies, especially in the low-end where there is very little. Therefore, the bass may end up masking (or worse, cancelling out some of) the kick a bit in the low-end. Often we can lower the bass (especially the sub of the bass) in volume a bit and all will be good, the kick is quite now clear in the low-end. However, often barely audible, there will still be headroom eaten as the kick and bass are still interfering, especially if both still at a decent loudness level. Again, in that case, you may use mixing techniques (again, weakning the bass.sub) but why go through such hassle if you can simply get best of both world with sidechaining.

Oten sidechain is a very subtle difference that you may not be able to hear (so don't worry too much about it in song making). However, even if not audible, it will definitely make stuff cleaner (also make our kick even clearer in the low-end) down there giving you more headroom in the lows going into the master and thus being able to push stuff more with the limiter.

## Use cases
### As a mixing tool
The original intention of sidechaining was always to be a mix tool. Make both your kick and bass stand out and also get more headroom down there. You'll usually have a seperate sub that will get sidechained to the kick. If no sub, you can sidechain the whole bass (though, these days there are tools that allow you to sidechain only the sub range so that you don't lose top-end transient of the bass).

Next to sub bass, sidechain can also be on other elements, usually in those cases it maybe if certain elements are interfering with the transients of the kick and you want a crystal clear kick, in that case you can SC your other sounds to it as well (such as bass lead chords). Usually you'll apply less heavy sidechain as it's not for interfering, just for a bit less masking.

## To cut stuff out from loops
It's very common to use a drum loop in a track. However, it's also very common for that loop to have a kick, hats, percussion and snare (which is why you sidechain in the first place). Often, though, you already have a kick and a snare so you don't want those in the loop (it's mainly the top loop you want). You could high-pass but then you still have the transients of the kick and snare which are often too much when hitting with your own. That's why you can actually sidechain loops to your kick (and snare) so that it kind of cuts out the kick and snare from the loop and leaves all the rest in. Very handy.

## Sidechain as FX
Lastly, sidechain is also used as an FX. In this case the sidechain is (very) obviousy and is usually used on almost all elements. Whether that is risers, chords, lead, whatever. Of course maybe not all with the same settings or as much as others but yeah a lot of instruments are sidechained. Risers, dnwlifters and other fx are also often sidechained to keep that rhythmic pumping going.

*Note: While it can be a stylistic choice, it's often a good idea to automate the sidechain to be off when the groove is gone (mainly the kick) to give listeners a bit of a break and also, it sounds a bit weird.*

## Techniques
### Compression
*Note: This is the old way and shouldn't be used anymore.*

SC compression based on another source. You route your kick to your bass (with 0% mix in from the route though) and then in your bass compressor you can put in sidechain to kick so now it listens to kick and thus when kick hits, depending oh the loudness of the kick waveform it will thus duck a certain amount (and of course come up in loudness when the kick is getting quieter (so in the tail). You have to play a bit with threshold and release (usually attack set at 0ms cuz u want the SC to kick in straight away) to determine the duration of ducking effect and also the volume reduction (will depend on kick and taste, like longer kick with longer sub might require longer duck to not clash but that's ok cuz kick gives sub energy anyway so u keep having the warmth).

One issue with this is that you'll be compressing hard since that's the point of SC but because of that your SC might sound weird due to the sound variance in your kick sample. Like, if your release (and sustain?) is short then during the SC and the kick tail ringing out the sound might go up real quick and then down and then up resulting in a weird and more distorted sound. Putting sustain and release longer can help smooth this out but then your sound might be ducking for too long. Also, different sounds will behave differently to that same kick and same compressor settings (?). This is why often producers that use this method (see Dylan Tallchief compression video) use a ghost kick. A ghost kick is not a real kick but simply a very short sample to which gets sidechained too. The ghost kick gets the same pattern as the real kick and thus everytime the ghost kick "plays", then the compression that's now SCed to the ghost kick gets triggered and will duck. And now, since it's such a short sample, the SC will come back up almost immediately. This is where you have full control with your release and sustain as you can leave it this short or you can put it longer and since there is no sound (and sound variance) that might make your "going up" weird, the going up curve will always be perfectly smooth no matter how long or short the sidechain is (of course, anything shorter than the sample will have same problem but if it's avery short sample, at that point it's hardly sidechaining anyway and it's also hardly audible so it doesn't matter, but that's why it's important it's a short (inaudible? or muted somewhere else?) sample.

### Peak controller (/LFO?)
- https://www.youtube.com/watch?v=F_lbPvxxL6o&t=69s
- You may reverse sidechain the kick too if needed
- What is peak controller? Vs. compressor? Vs. lfo? vs. kick start
- Shaperbox 2? put on gear to want/buy list!

### Volume automation
*Note: this one is recommended.*
- (See Synthion Konpeito livestream to see how he gets that preset/template and what plugins for SC, like it's not fader, right?)

This one is not based on any input source as it quite literally is just volume ducking. You basically use a volume plugin on the track you want to SC and then you automate the volume from 0 to original volume everytime the kick hits (so you put automation clip at every kick hit in the playlist). 

This one has the advantage that since you can draw in the enveloppe of the sidechain yourself, you can draw a smooth SC curve yourself and so you don't have to play with compressor settings and/or use a ghost kick. Also, having the kick in your playlist and then have your automation next to it are nice visual clues to see how big your kick is and how you have to/can draw your sidechain based on the "bigness" of the kick (like long or short tail that might clash with sub).

According to Dylan Tallchief (see his compressor video) it's annoying to have these in the playlist and you have to drag them together but I see a lot of pros doing it this way regardless. Yes, that's a bit annoying of course but I don't see it as a less legitimate way. Also, you need to use a plugin and not just the fader because then yes, you do lose the ability to control the sounds volume since you're using that to SC and it's messy to adjust your sidechain to the new volume always. So yeah, use a plugin for your sidechain (such as fruity balance) if you do it the volume automation way.

Not based on another source, we simply look at the waveshape of the and just write our curve, kick in play list and also, this volume automation does also already do not have the weird release vibes you get with compression without check synthion his clip and check what he automates there as his SC which plugin not fader cuz then cant adjust volume
Fruity balance or peak controller LFO also volume atuomation or?

## Ghost kick
Usually a very short inaudble tone or kick (which mimicks the notes of the actual) you use basically as a trigger point for the compressor (see first technique). It's so short that the compressor doesn't do weird stuff (as no compression is applied) but immediately ducks to 0db (or whatever). You can thus simply draw in the envelope you want (as the duck will have happened and now you can set the release to as slow or fast as you want depending on the sidechaining you want).
 
## Multi-band sidechaining
- [Au5 black and yellow](https://www.youtube.com/watch?v=oLBqmi0ot_g) (mentions it somewhere in here)

Just like how MB compression is more transparant (= less obvious but still effective) compression, MB sidechaining is also more transparant sidechaining. The reason is that you often don't want to sidechaining anything from your sound that isn't sub frequencies competing with the kick as it is not necessary. Also, the frequencies you may want to sidechain depends (like it may be the sub range but maybe the upper-lows too) as well. MBSC helps with that as it allows you to set bands for SC purposes. Therefore, you could choose to have your mids and highs no or very little sidechaining while you could have your lows and sub a lot of sidechaining.

Typical examples are a bass where you may have more than just a sub in the bass patch and you don't want to really sidechain the whole bass to the kick, but just the sub. In that case you don't even have to seperate the sub from the top bass (anymore) but rather you can do MBSC compression. Or, maybe your top bass still needs or has too much lows and it just gets a tad in the way in some notes, again, can configure a band for that.

A great tool for this is Shaperbox 2.

## FL Studio SC workflow shortcuts
(This should go in my software tips)

templates, or preset or like sc on a send and then with multiple release times depending on how short or long u want sidechain, how?

also the sidechain duck on kickstart, etc. does it always need to be like ducking to 0, like ive seen people adjust the kickstart mix so it doesnt duck too hard, i guess that just depends but in volume control tho usually starts at 0 the automation clip if im correct?

## Notes
Look up "sidechain for loudness and rms"
sidechain tips, different kinds of enveloppes and when and why

again mainly for sub so audible you wont maybe even notice the sidechain if ur untrained as its mianly the warmth that gets sidechained but even that, the kcik brings some warmth tand then the sub too right after so u wont realluy notice loss in warmth anyway

https://www.masterclass.com/articles/music-101-what-is-sidechain-compression-uses-tips-and-tricks-for-sidechaining#what-is-a-sidechain-compression-plugin


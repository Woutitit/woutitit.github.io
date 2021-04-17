[Home](index.md)

# Sound design and recipes
## Table of contents
1. [Introduction](#introduction)
2. [Tips](#tips)
3. [Recipes](#recipes)

## Introduction
This article is for specific sound recipes, like a "DnB snare" or an 'EDM riser". It's not meant for generic stuff and it's also just suggestions to throw into there.

## Tips
### Consider adding ADSR, especially decay
Adding an ADSR is important for a sound because without it, it's basically just an on/off state and nothing in between. Also, the sustain is 100% no matter how long you play the sound so the sound basically has a lot of energy and it never drops. So for example in a lead or in chords and they sustain (and they are usually loud), there is no moment that the energy level drops making those patches very high energy (especially if bright too) and most likely too much energy. 

Again, you most likely want to add decay to lose some energy over time to not be too much (and also allowing other elements to come through) and then when it hits again, it can be full energy going down again. Additionally, again, this is more how real instruments and sound waves work too. Also, this depends on the patch. A pad you may not want or need since it's quiet in the mix and meant as sustained sound (but since it's quiet and perhaps low-passed too it's not overpowering). Same for perhaps a sub bass, which again, is not overpowering in nature but you want to have stable. Not (much) decay needed really. So it depends (same with amount of decay).

Either way, ADSR just adds sophistication and interest to a bland sound and it also adds together with the harmonic content to kind of sound more like a bell or more like a piano or more like a plucky staccato violin or whatever.

## Consider adding (low-pass) filtering to your sound
A lot of synth waves are super rich and dense in harmonics so having them as is usually already taking up a lot of space in a mix. Especially adding multiple synths like that together, all at a considerably amount of volume, and you really have a dense mess quickly and not a lot of room for other stuff to cut through. Also, the harmonics don't decay like in real instruments and therefore often in saw and square waves, if high notes are played, the high harmonics will be loud and thus be quite piercing to the ear. On top of that it also doesn't really sound realistic.

Therefore, consider filtering, especially low-pass filtering. It doesn't have to be much if your sound is supposed to be bright but just a tad. For a bass, probably more as you want mainly the low-end and want to make room for other stuff. But yeah filtering makes the sound less rich and thus less dominant in a mix allowing for other elements and it also kind of shapes a wave (especially low-pass filtering) like a real or more realistic instrument/sound wave.

## Recipes
### Hard-hitting DnB snare
TODO: Research more

You'll usually want to find a snare that has a lot of white noise as a body/tail and possible some reverb (?) on it as well so it really cuts through the mix.

For layering you'll want to look into layering a regular snare with some more high-end but not super subby claps, possibly some stadium claps and also possibly some snare that is more white nois-y. You'll of course want to eq them out as you won't need the fundamentals of all, just the timbre or transients that they bring. Again, you'll also want at least one of the layers to be good in transient.

Also, your other stuff, especially your bass you might want to sidechain to this snare too as it will take up a lot of frequency space once it hits so you'll want to make stuff when this one impacts.

### Generic EDM riser
You'll have to decide whether to use a more tonal or a white noise riser/downlifter. Often both get used and layered together. You'll also need to decide if you let it pump with the music or just as is right now.

### Sub - mid bass (- supersaws configuration/top bass)
- https://www.quora.com/How-do-you-make-good-emotional-melodic-dubstep-chords
- https://theproducersforum.com/index.php?topic=4693.0
- https://www.reddit.com/r/edmproduction/comments/7egayj/chord_voicing_in_supersaws/

This duo (or trio) is super common in a lot of EDM genres. The reason for it is that it's an easy way to fill up the mix but also to seperately fine tune the sounds in each frequency band without screwing the other sounds in the other bands. It's just three convenience layers even if they are the same waveform.

First is the sub bass. This bass lives at 60-150Hz. It's either a low-passed saw wave or it's a straight up sine wave with a bit of saturation to be hard better. Full mono and sidechained to kick usually. Now you have nice low-end energy.

Then it's the supersaws on top. Standard ones are 7 voices detuned, I already described here how to make them.


Next is mid bass which lives around 150-350Hz. It will be thicker than the sub bass. Maybe a low-passed saw (less low-passed) or another wave. Perhaps some saturation and/or OTT. It's harmonics will extend nicely to around 500Hz range and perhaps all the way to 2kHz maximum where it completely falls off.

### EDM supersaws
https://theproducersforum.com/index.php?topic=4693.0
https://theproducersforum.com/index.php?topic=811.0
https://theproducersforum.com/index.php?topic=4925.0

Supersaws often sound big and huge. However, the secret to the hugeness is actually in the bass layer and more specifically, the sub layer of the bass. It's the sub that gives that wide stack the foundation of being huge. Add to that a fatty top bass layer/top bass with charachter and that's a huge sounding harmony. Usually, you'll want to keep your supersaws clean, as in, not too distorted as they are there to make it wide and fill spectrum (but since it's a chord they mud up quickly). Then, the bass, which is one note can be made fat since it's a low frequency and because it's one note (so no mud or clashing whilst still filling) it's going to make the layer on top sound huge even if that supersaw layer on itself does not sound huge.

For the rest, common cuts are a slope around 75-200 Hz and lowering until 500Hz. Also, supersaws tend to be harsh in the highs. Often it gets rolled off a bit there but if you then lack highs then a layer of white noise gets added. Due to the nature (being even over the spectrum) of white noise it sounds less harsh than the highs generated by the saw stack and it can also be layered in at a quieter volume.

Often a chord made in the C4s and then the root put down to C3 (and C2) if needed (will be mostly be rolled off probably but maybe it can add stuff). Then extensions on it. Experiment with voicings and exotic chords. Below C4, don't do extension as beating frequencies and stuff will be just muddy and clash. The chord is often a stack of a triad and then another stack of the duplicated triad on top. Leaving notes in and or out depending on the emphasis note (which is top). Often a speerate synth also plays the emphasis note as a lead.

7 voices detuned layer. Perhpas you want some mono in there mixed to taste, perhaps you want a +1 octave layer in there for taste. Perhaps you want to layer with a square for timbre and stuff like that.

### EDM chiptune-y lead
A few examples:
  - https://www.youtube.com/watch?v=GM7JtFZ5yyU
Common modulations, have a pulse kind of way and then emulate sync (which is pwm i think) and vibrato can have them in a single macro if you want.

### Sub bass
Usually around 60-100Hz. Write in Cm or Fm for ideal sub. Can either be a straight up sub with preferably some saturation to be better heard or it can be a low-passed. Both are kind of the same thing.

### EDM basses

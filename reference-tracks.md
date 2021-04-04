[Home](index.md)

# Reference tracks

## Table of contents
1. [Introduction](#introduction)
2. [Tracks](#tracks)
3. [How to use a reference track](#how-to-use-a-reference-track)

## Introduction
Here I post all the reference tracks I find useful. Perhaps post also the genre and whether it's mainly for mixing or compositional reference or both.

## Tracks
//

## How to use a reference track
*TODO: Add stuff and maybe put somewhere else.*

A reference track is handy but you need to know a bit how to use it in order to actual get something out of it. Here are a few ways how to use a reference track.

### Have a master chain on
Reference tracks usually sound louder and bigger and more brighter since they are mastered so keep that in mind. Of course, level match them (easy plugin "Reference" can do that) and you can have a quick master chain and you can then occasionally see whether you're actually far off or not vs. the reference track. But yeah again, use them because regardless of smashing in the mastering, there will always be quieter elements and louder elements. On the louder elements the smashing will most likely happen. Often that's the drums and stuff but sometimes could just be the leads and chords and the drums more in the background. Again, the levels don't matter to make your master loud, you gotta level as to what you want in forefront and what you want in back. Of course, not having too much dynamic range to not have to make the mastering too difficult.

### Direct out
No matter what purpose you use a reference track it's always useful to have it run straight to the speakers instead of through the master (you can do this by having it on a mix track and then the ouput to something like "Out 1 - Out 2". It's useful as it won't be affected by master channel fx and also you can then mute the reference without muting your track and you can mute your track (one-click-mute via master) without muting the reference. Very handy.

### LUFS match
If the track you are referencing sounds about the same as how you want your MIX to be then it is useful to more or less LUFS match yours and the reference as then you can kind of compare loudness and frequency presence and stuff in a more fair way. In FL Studio you can do this by placing two youlean meters, one on the master, one on the reference and then a parametric eq2 before the two meters. Then you can make the tracks louder or quieter by changing the volume on the eq 2's (as volume fader is after fx chain I think and thus doesn't change the meters). Have both at around the same LUFS. 

Now, note though that you have to compare similar sections and that if your mix is busy and theirs is sparse, the LUFS might be a bit off so you need to try to have as similar sections as you can compared to eachother. Now you can start checking out the loudness of elements, the frequency presence in span/tonal balance control and all that good stuff and you can do it in a more fair way (as in, it's less guessing and more like, it's sounds like x in the reference track which is brighter and louder than x in minde and since it's LUFS matched mine needs to be louder by the difference between their x and mine x more or less). Again use your brain a bit too as this is not exact science even with LUFS matched and even with similar tracks, the more similar the more science of course. 

Also, you might want to setup a quick master chain and LUFS match with that, turn off master when working and then turn on master again everytime you reference for more accurate of what in the end it should be.

### Spectrum analysis
If the mix is more or less what you want, checkout the spectrum of the mix. Now, look also at the waveform and see whether (and how much) compression is going on since that will skew a little with the details as the reference track will always seem fuller because of that mastering it already got. However, try to look past the exagarations and see whether they have a lot of low ends, some dips somewhere (so you know you might need sparser stuff their and/or eq cuts), how dense.

Here it also helps to have a quick master chain going on just to have a bit better clue of how close you are as you're comparing a master to a master now. Again, note how much compression there is and if in cases like dubstep and heavy-sounding stuff, realize the limiting is probably quite a lot, probably some distortion/soft clip before it too. So the closer you can get to the master chain they've used the closer you can get to actually analyzing.

Also, again, for loudness you'll again have level/LUFS matched your stuff. In this case it's a bit easier as if you want to know the loudness of the kick you can actually low pass and then get most of the loudness of the kick (since mostly kick playing), of course it will be louder in the end with the high-end so you'll want to low-pass your kick too at the same point and level match that (have to see through the bass a bit) and then the high-end will add loudness but again, if low-end right that's a good start. Also the kick getting right (and bass) is also already a very good start as doing other stuff by ear and just watching spectrum is/becomes easier. Also, if you think "stuff is so loud" but clearly it's just because your mix is quieter, then you need to LUFS match again.

### Check for solos
Check for soloed tracks. For example if kick and/or snare solo (like in superseded) you can see whether they top the audio waveform as that means then that those are (one of the loudest elements) if you then also have one of the melody/harmony lines solo or kind of together and you see they are less you can kind of deduct that they are less loud (by x amount) than the kick. Again, it depends on context as sometimes there is filter automation making the stuff less loud, sometimes it's volume automation so as always use your brain.

### Check waveform, the heat meter.
Similar to checking solos, just check the waveform and see how much (or little) it is compressed. Check to see how loud stuff is or check maybe even for certain compression settings based on sustains or not. Like, if there is a certain cool sound (like a pluck or something) going on, try and check the waveform to kind of gauge what it really is in the spectrum and what it's doing. Same with heat meter as sometimes you can see some nice frequency sweeps in there or whatever and then you can deduct that the cool sound you heard was a sweep in x frequency range.

### Get inspiration
Use it for inspiration on everything of your track. It doesn't have to be the same track you use for mixing (as sometimes you might want to compose similar to an old song but have the mixing style of a modern song).

## Band soloing
https://www.youtube.com/watch?v=QQU2RDzoFQA&t=16s

## Sounds often need to be tinner than you think
A lot of patches are designed to sound full without context of a mix. They have a lot of reverb and delay and probably a lot of frequencies they take in. Often all those things are to much for a sound and will muddy stuff up quickly, especially in layering.

For the fx problem, a common thing is too simply strip a patch from its fx and then add your own fx to taste and too context. It depends as sometimes your mix is sparse and could indeed benefit (in a section) from a shitload of reverb and delay to fill space out. So again it depends but especially in chorus and busy parts you'll want to make sure you tailor fx.

The frequencies, there are a lot of sounds you'll want to have tinner than expected. Stuff that you'll solo and think "holy shit that sounds thin". For example, if a bass patch is quite fat and filling, then you can kind of have your chords at low volume and also eq'd in such a way that they don't add any bottom end, maybe a bit of mids but maybe also not really high end even and have no fx and stuff. It will sound thin but together with the bass it just adds that lilttle bit of extra fat. Same with layers (especially similar sound-same octave layers, often you don't want a fundamental of a layer as that would clash with the fundamental of your main layer, you only really want some timbre but also not too much timbre so it clashes so again you'll EQ that shit so it probably sounds rather thin on itself but filling in context of the mix and the main sound. Last example, the bass that might have mids cut out to make space for body of sound as bass mainly for low-end and some high-end to add bite and better speaker listening. It sounds tinner than bass before but thanks to that it makes room for mid stuff.

On the other side of the coin, there might be elemens or mixes in which the elements do need to be super thick or rather filling or substantially filling. Perhaps your chords need to be filling, perhaps your bass needs to be filling as that's the only element. Again it's a spectrum and you always have to judge in context of mix and layers and sound and functionality and importance;

## Check stereo field
Use a Mid/Side EQ or Voxengo MSED. It would be even better if you had indivual stems but in this way you can solo either mids or sides and you can see if for example the bass has any sides or only mids or both so you know if you want/need to make your bass (more) mono or stereo.

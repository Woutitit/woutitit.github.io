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
Sidechain is there to make the bass (and bass frequencies of other instruments sit nice with kick). Often in these lowerer frequencies, since there is not a lot of frequency space available mud buildable goes very quick. Or, if no mud build up, since waveforms there are more prone to phase cancellation (and more audible too) there is a big chance that phase cancellation will happen if kick and bass play together (see phase cancellation article) which ends up in a weak kick as it's cancelled. What we thus wanna do is have as little as possible instruments playing in that sub frequency range at the same time. Of course, often the sub bass and kick hit at the same time so that's kind of impossible.

Deciding whether your bass or kick will be the dominating frequency in the sub range can help you make mixing decisions. For example, if you have a big kick with a big tail, there is already enough sub energy (if the kick hits enough times) that the sub frequencies of the bass aren't that important. Similarly if you're kick is short and not very sub-heavy (by choice) you might want your bass to be the dominating factor. Either way though, you usually lose in this battle as choosing is losing and eqing that range is also a bit messy.

This is why in conjunction (or even as replacement) we use sidechain as then we don't have to lose. We can have the kick be at full force and then have the bass duck for that sound but then have the bass come in right after the kick is done. Hell, we can even seperate the sub and top of our bass and have only our sub sidechained so the bass remains all times at full force and it's only the problematic sub frequencies of the bass that duck (or we can have the top bass duck too but less or a for a shorter period). Also, we usually want the bass to duck since our kick does bring the main transient which is important to keep beat and keep groove going we want it stable which is already reason to sc. And also, SC helps for loudness as you can keep your bass louder per usual without having build up so you can slam the compressor harder and the bass louder together with equally loud kick.

However, don't think SC will save your mix. No, you're mix will have to sound decent with or without SC (unless it's really used heavily as a FX tool not a mixing tool). If not, you're FX, sound selection, design, composition, arrangement, tonal balance most likely sucks. Yes, without SC, your low-end is allowed to sound muddy and build up and yes your master might sound bad due to the build-up but it shouldn't be to the point where it's incredibly bad, then something more than your SC is up.

Lastly, not only bass can be sidechained, if there are other instruments that might cause build up (even after some filtering) you might want to sidechain those (or simply for kick clarity sake as frequency could be a thing regardless of overlapping or not but just due to loudness(?)) too, though maybe the mix level not at a 100% as a full duck might not be needed.

## Sidechain as FX
Can make risers rhytmic and stuff, or everythig rythmic like on a 4 on the flour for example, very effective to make everything dance, just put like a kcikstart on everything. Often done on risers, chords and/or bass in a dance groove.

## Sidechain as a mixing tool
Also, more subtle sidechain is a vital mixing tool. Sidechain with shorter release (maybe even higher threshold) will have less of the FX but more of the subtle non-muddying up non-clashing vibe to it. You use this is type for mixing purposes. You usually use this type of sidechain always if you don't use the ducking one since it really clears up the mix no matter what genre, just depending on the genre you'll want to try and be as subtle as possible and the more subtle of course the more you might need to have to EQ a bit too for extra cleaniness.

Also, don't be afraid that it will make your mix sound empty as you might duck a lot of sounds at kick play. But again, it builds on the concept of complextro, it might be only one sound playing at that time (the kick, if all is sidechained which usually isn't anyway) but it's only for a very brief moment so you get the punch of the kick and it doesn't even seem that the music was ever gone since it's back in full force so quick anyway.

## Techniques
### Compression
SC compression based on another source. You route your kick to your bass (with 0% mix in from the route though) and then in your bass compressor you can put in sidechain to kick so now it listens to kick and thus when kick hits, depending oh the loudness of the kcik waveform it will thus duck a certain amount (and of course come up in loudness when the kick is getting quieter (so in the tail). You have to play a bit with threshold and release (usually attack set at 0ms cuz u want the SC to kick in straight away) to determine the lduration of ducking effect and also the volume reduction (will depend on kick and taste, like longer kick with longer sub might require longer duck to not clash but that's ok cuz kick gives sub energy anyway so u keep having the warmth).

One issue with this is that you'll be compressing hard since that's the point of SC but because of that your SC might sound weird due to the sound variance in your kick sample. Like, if your release (and sustain?) is short then during the SC and the kick tail ringing out the sound might go up real quick and then down and then up resulting in a weird and more distorted sound. Putting sustain and release longer can help smooth this out but then your sound might be ducking for too long. Also, different sounds will behave differently to that same kick and same compressor settings (?). This is why often producers that use this method (see Dylan Tallchief compression video) use a ghost kick. A ghost kick is not a real kick but simply a very short sample to which gets sidechained too. The ghost kick gets the same pattern as the real kick and thus everytime the ghost kick "plays", then the compression that's now SCed to the ghost kick gets triggered and will duck. And now, since it's such a short sample, the SC will come back up almost immediately. This is where you have full control with your release and sustain as you can leave it this short or you can put it longer and since there is no sound (and sound variance) that might make your "going up" weird, the going up curve will always be perfectly smooth no matter how long or short the sidechain is (of course, anything shorter than the sample will have same problem but if it's avery short sample, at that point it's hardly sidechaining anyway and it's also hardly audible so it doesn't matter, but that's why it's important it's a short (inaudible? or muted somewhere else?) sample.

### Peak controller (/LFO?)
What is peak controller? Vs. compressor? Vs. lfo?

### Volume automation
(See Synthion Konpeito livestream to see how he gets that preset/template and what plugins for SC, like it's not fader, right?)

This one is not based on any input source as it quite literally is just volume ducking. You basically use a volume plugin on the track you want to SC and then you automate the volume from 0 to original volume everytime the kick hits (so you put automation clip at every kick hit in the playlist). 

This one has the advantage that since you can draw in the enveloppe of the sidechain yourself, you can draw a smooth SC curve yourself and so you don't have to play with compressor settings and/or use a ghost kick. Also, having the kick in your playlist and then have your automation next to it are nice visual clues to see how big your kick is and how you have to/can draw your sidechain based on the "bigness" of the kick (like long or short tail that might clash with sub).

According to Dylan Tallchief (see his compressor video) it's annoying to have these in the playlist and you have to drag them together but I see a lot of pros doing it this way regardless. Yes, that's a bit annoying of course but I don't see it as a less legitimate way. Also, you need to use a plugin and not just the fader because then yes, you do lose the ability to control the sounds volume since you're using that to SC and it's messy to adjust your sidechain to the new volume always. So yeah, use a plugin for your sidechain (such as fruity balance) if you do it the volume automation way.

Not based on another source, we simply look at the waveshape of the and just write our curve, kick in play list and also, this volume automation does also already do not have the weird release vibes you get with compression without check synthion his clip and check what he automates there as his SC which plugin not fader cuz then cant adjust volume
Fruity balance or peak controller LFO also volume atuomation or?

## FL Studio SC workflow shortcuts
(This should go in my software tips)

templates, or preset or like sc on a send and then with multiple release times depending on how short or long u want sidechain, how?

also the sidechain duck on kickstart, etc. does it always need to be like ducking to 0, like ive seen people adjust the kickstart mix so it doesnt duck too hard, i guess that just depends but in volume control tho usually starts at 0 the automation clip if im correct?

## Notes
Look up "sidechain for loudness and rms"
sidechain tips, different kinds of enveloppes and when and why

again mainly for sub so audible you wont maybe even notice the sidechain if ur untrained as its mianly the warmth that gets sidechained but even that, the kcik brings some warmth tand then the sub too right after so u wont realluy notice loss in warmth anyway

https://www.masterclass.com/articles/music-101-what-is-sidechain-compression-uses-tips-and-tricks-for-sidechaining#what-is-a-sidechain-compression-plugin


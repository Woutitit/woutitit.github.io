[Home](../index.md)

# Synthesis
## Table of contents
1. [Introduction](#introduction)
2. [Why synthesis](#why-synthesis)
3. [Synthesis techniques](#synthesis-techniques)
4. [What is MIDI](#what-is-midi)
5. [Waveforms](#waveforms)
6. [Synthesizer settings](#synthesizer-settings)
7. [What is an LFO](#what-is-an-LFO-)

## Introduction
//

## Why synthesis
While in theory you could recreate any sound you'd like with synthesis, synthesis (and synthesizers for that matter) are generally NOT meant for that purpose. They are meant for you to be able to create your own sounds. This is (partially) why (subtractive, see later) synths don't offer realistic waveforms but harsh, frequency-rich waveforms because the math is easy and the frequency content is so rich that through a combination of these waveforms, filters, ADSR, LFOs, etc. you can make sounds that sound musical. They might not sound like a real instrument, but they sound musical, especially since real instruments alre also nothing more than filtered out, ADSRed (sometimes LFOd) waveforms. Also, since these waveforms are so rich, it's a very good way to start and sculpt something good out of it rather than have realistic unrich waveforms and try and sculpt something else out of it. With these waveforms you can be flexible and go any direction you'd like.

So, in other words, if you need a real piano in your production, use a real piano (or a sample library). Same with other real instruments. If you don't, use a synth. Of course certain instruments are common in certain genres or serve certain purposes so a lot of times producers will make (or use a preset) a "piano-like" synth sound or a "bell-like" synth sound or a "slap bass-like" synth sound. Again, just by messing with filters, ADSR, LFOs (and of course fx afterwards) trying to get similar ADSR/filter (harmonic content)/LFOs as the real instrument, though it does not need to sound alike, just come close and you have to luxury to adjust to taste in your synth. Also, often producers will just talk about "pads", "plucks", "leads" and stuff like that as usually some similar ADSR/filter waveforms have the same function (and which you use depends on your mix/taste).

Of course, in your synths you'll have presets that say "piano" or "bell" and you can use these instead of actual samples and might get away with it depending on how in the background it is or how unrealistic your produciton can sound or how good your post processing is. But again, these are made by experts and these are not the things that synthesizers are really made for.

## Synthesis techniques
### FM Synthesis
https://noisegate.com.au/the-fundamentals-of-fm-synthesis-explained/

### Subtractive synthesis
Synths that do SS will accept a certain waveform and then offer you ways (such as filters) to do sculpt the wave form by subtracting frequency content from it. This is an easy to understand way of doing synthesis as it's very intuitive in how it works.

Usually, easy mathematical waves get offered by synths which contain a very rich amount of certain (or all) harmonics and the timbre and thickness you want depends on the wave. However, the harmonic content of these waves, compared to real instruments, is so rich that even when you play a bass note, you'll still hear harshish frequencies. This might be what you want but often, if for example you're tyring to make a bass-like sound, you'll want to filter those frequencies out and through SS you can do that. Usually you can also have a knob and selection of how steep you want to filter or whether the filter should be more smooth and from where the filtering should start. This, together with ADSR and LFOs should give you plenty of tools to make a sound that sounds musical rather than rich (and harsh).

It might be weird at first to think about how SS can be useful, but as we just saw, in SS we DELIBERATELY start with a harsh but rich waveform so that we have a lot of content to work with. If we'd start with, let's say, a sine wave, then SS is very useless as the wave can't be made more interesting and musical at all with SS.

So yeah, now that you go out and start making super saws just remember that the chords the amount of voicings and the unison etc. will create a really dense sound and probably really harsh since even just one saw note is already rich in content. And just remember that this is normal but that it is MEANT for you to use filters and stuff to make that stuff probably less harsh and more musical but that depends on you.

### Wavetable synthesis
https://www.youtube.com/watch?v=mMcRRoXadK4&t=107s

In wavetable synthesis, you're basically constructing a table of sound waves in a synth. In Serum for example, you can go into the editor to add some waves (which you could see as frames in a movie), it doesn't matter how many or little. You could also import a sample and then for each small bit of sound in that sample it will figure out the waveform at that point, in the end you have a wavetable of that whole sample and if you flick very quickly through it whilst holding a note on the synth you might be able to hear the resemblance of your sample.

Wavetable synthesis is nice as it basically allows your synth to be any sound in the wavetable at some point. In theory, if you had a saw and square, you'd be able to for the chorus have the saw be played and then for the verse flick through the square for example (though not sure if people do this). Another cool thing is, which dubstep people use, is that it allows for some nice modulation as going through all the different waves gives a nice modulating sound in and of itself.

Mind though that whether it is from a sample or something you construct yourself (or other ways), often a wavetable needs cleaning (if you have made it yourself). Luckily synths such as Serum alow for several kinds of interpolations techniques which basically all can smoothen out the changes from going to one wave to the next and back (e.g. through crossfading for example) but all with a different flavor (?). Other things are removing harsh hissing sounds that often occurs through other techniques, basically a lot of things to clean up stuff.

crossfade interpolation to smoothen

### What is MIDI
> See "Analog recording in a digital world" to learn more. 

- http://digitalsoundandmusic.com/6-1-3-midi-data-compared-to-digital-audio/
- https://en.wikipedia.org/wiki/MIDI

So in my article "Analog recording in a digital world" I talk about how every recorded note is basically stored as a digital digit and that we need to convert it back to analog to play it back. However, a synth does not use digital digits to play sounds, instead a synth uses something called MIDI.

Unlike audio, MIDI are just instructions that a synth can interpret to generate its final sound (stuff like NoteOn() and NoteOff() and aftertouch value information per note etc.). And thus, from the moment a synth has its MIDI information and we hit "play", it will *interpret* it and then, just like a DA converter, will send electric voltages that represent a continuous wave based on the MIDI information and its "patch" settings. 

An important note to thus make and understand here is that sample rate and bit depth are totally irrelevant to a sound generated by a synth (for both analog and digital synths, unless you would be literally recording the output of an analog synth with an audio interface lol). This is because, in the other camp, so in DA conversion with digitally stored audio, you would always need to have quantized sample points to be able to construct electric voltages that resemble a continuous wave and are send to the speakers. How else would you construct an electric wave signal that was the original sound wave? There is literally no information than the samples but since the samples are quantized we can't be 100% accurate in reconstruction. *A synth on the other hand doesn't need quantized sample points at all* to construct electric voltages that are send to the speakers. All it needs is MIDI information - which is just a list of numbers and settings - and "patch" information which is also just a list of number and settings.

If it is still not clear, let me illustrate with an example:

MIDI information:
Note: C5
Velocity: 1 (MAXIMUM)

Patch information:
Wave: Square wave
Filter: Low Pass
Filter setting: steep cut off at 2000 Hz.

And then if we hit play our synth will interpret all of this:

"Ok I see a square wave in the settings, that means I need to generate an electric signal that looks like a waveform with a fundamental frequency at C5 and contains the odd harmonics that thus resembles the classic square wave."
"But oops, since velocity is maximum I need to send out the electric signal so that it also looks like it makes the fundamental and odd harmonics at max value."
"Oh, but I also need to low pass at 2000 Hz, therefore I need to send out the signal so that it also looks like the above but also looks like it removes all the frequencies above 2000Hz." Etc.

Can you now see how a synth has indeed correct and full information with just numbers to fully send out an accurate electric wave. Of course, the synth still needs to be able to convert/interpret these numbers accurately to electrical waves but that's all and since we're not working with samples but only number settings and then straight electricity (which IS continuous in nature) this will always be 100% accurate. Also, you can even hit play of your synth and hear the sound changing (like if you are opening/close a low pass filter), that is literally the synth modifying it's electrical signal in real-time and sending it to the speakers so that we hear it being modified too in real-time.

One last thing. It IS true that from the moment you are bouncing the sound output of your synth to actual audio (which is called *resampling*) through a digital audio recorder like Edison (named after the guy that FIRST ever recorded an audio signal, cool!), sample rate AND bit depth will of course be relevant again. That is, Edison's recording is of course no different or better from audio interfaces' recording and thus also records at a certain audio rate and also saves the audio at a certain bit depth. This is even clearer to see when you realize that you don't have MIDI anymore, you have an audio file. And thus, you can't also just swap your notes and stuff and you literally have only the audio file (and thus its sample points) to work with (even though it gets displayed graphically as an actual wave, it's just sample points, it's kinda like a preview of what the reconstruction algorithm will do).

## Waveforms
### Saw wave
The saw wave is the most useful and versatile wave since it's super harmonically rich. That is, it has all(?) the harmonics and these harmonics are all very and equally loud. In fact, a saw wave's harmonics are so loud that it's hard to clearly hear a fundamental tone, especially considering higher frequencies don't need to be as loud as lows to be perceived loud.

*Intermezzo: A saw wave's overtone dominance is why if you have a bass, especially one that doesn't need to fill the whole frequency spectrum, you'll want to low-pass (or at the very least low-shelf) filter the wave so that the upper harmonics are tamed. If you don't do this, for the bass to not be too loud in the mix you would need to turn down the wave in volume (since the high frequencies make it loud) but then you're turning down the low frequencies too causing you to have too little low-end. With filtering you can keep the wave at your current volume where it gives nice bottom-end without them being ear-piercingly loud due to the harmonics. Also, for sounds where you mainly want high-end, doing the opposite is also true of course.*

Because of this richness, a saw wave is ideal in subtractive synthesis since we basically have "everything" but every instrument or sound has "a few things (read: less harmonics and per harmonic it's less loud)" but just in a different way. So no matter which sound we want to make, we can technically always start from a saw and pair that together with the ADSR (also discuss here) - and some synths being able to precisely add harmonics/remove and amount - we can pretty much shape the sound to whatever we want and even mimick closely a lot of real instruments. 

Again, a common thing is to low pass filter saw waves at least a little bit since the loud harmonics are really harsh especially in the upper ranges. Additionally, this also mimicks a bit the harmonics decay that normal instruments also go through making the wave a bit more musical.

Either way, all this doesn't mean that starting from a saw is always easiest. There are other waves too with different timbres that may already put us closer to what we're after so in that case it would be a bit silly to start from a saw wave.

### Square wave
A square wave is similar to a saw as in that it is very harmonically rich. A square wave is what "perfect" distortion would look like basically. The difference between a square and a saw is that the square only has odd harmonics. This is still rich in sound but less rich and it also has a different timbre than the saw.

### Triangle wave
A triangle wave is less rich in harmonics and decays quickly too. Because of this it is the go-to waveform for chiptune basses. It can also be used for non-chiptune basses but since we have access to filters and stuff, producers often tend to use a low-passed saw filter which gives a similar effect and is a bit more versatile in where you place the cut off.

### Sine wave
A sine wave is a pure tone. It's very harmonically poor as it has no harmonics which means it doesn't really have charachter and may get lost in the mix. This is why a sine wave often gets saturated a bit to at least give it some bite. Also, since the sine wave is so thin it can be plopped into a mix without taking much space, just make sure to not make it too loud since because you don't hear it cut through the mix you tend to boost it. Favor saturation over it and favor not making a sine wave a main element (though in quiet sections or sparse mixes it can definitely work if you have some saturation and a bit of width and octave layering).

Either way, the sine is often used as a (sub) bass. Again, in the lows you don't necessarily need too much harmonic content anyway so having bass and preventing the low-end to mud up is easily done with a pure tone single frequency sine wave. Again, to prevent from sounding a bit too clean and thin in the low-end you usually start either from a saw and low-pass it until it sounds like a saturated sine or you saturate the sine straight away.

## Settings
### Unison and detune
> See stereo imaging article for how exactly unison/detune works

The unison knob is an important but overused one. What it does is basically make a sound wider. What it does **not** do, unlike popular belief, is make the sound denser as making stuff wide does not magically add harmonic content. A sound with unison sounds fat because it has added voices all spread accross the stereo field making for a "big" sound. If these voices weren't spread (and/or the same pitch), the sound would just increase in volume.

That said, heavy detune, i.e. unison where the added voices are "heavily" different in pitch, there will be noticeable harmonic content added since the pitches are so different from the original pitch. This is indeed used to add thicknes to a wide sound but usually this one is mixed in with a less detuned oscillator to make the awful sound of that heavy detuned (but thick) oscillator be noticed less.

Either way, this fx is overused or too much unison is added to a sound, especially by beginners. Since unison makes stuff wide it adheres to the same drawbacks as other stereo imaging techniques and practices. For example, for a pad, a (dense) chord stack on a synth patch with a lot of unison and/or detune is usually okay (and perhaps what you want) as the pad atmosphere nicely spans the stereo field due to the patch and due to the chord stack it also nicely spans the frequency spectrum. And since a pad is usually not a main element, there doesn't need to be focus on it and also it's further back in the mix so the density doesn't overpower the track but thanks to width and thickness it creates this nice air around the whole track.

And that's the main drawback: lack of direction and focus. For example, a supersaw chord stack in future bass often also has a lot of unison and is pretty wide. Again, this is okay because its purpose is to fill up the stereo and frequency field making a wall of sound, there is no need for it to be focused/in your face/intimate. Also, on top of that and below that you'll usually find that the bass and/or leads are less wide and more focused. So the listener has some elements to focus on whilst the supersaws fill up the mix. Also the chord stack doesn't always have to be super wide and/or stereo either. If in your mix the chord stack's purpose is to be more focused and less wide (and more intimate), then reduce the unison by all means.

*Intermezzo: If everything is wide, nothing is wide. And if everything is wide, everything sounds super directionless adn there isn't really a clear thing to focus on for the listener. Seriously, the graph of your music sounding better does not go up with the wider you make every sound. It's about contrast. Make some stuff wide that you want to be wide make other stuff less wide or completely mono that you want to be more focused. This is what will create a multidemnsional mix rather than a mono 1D or a 1D directionless mix.*

*Intermezzo 2: Rhodes and stuff often also have a bit of imaging going on (how?) but usually not as wide and directionless. Again, they are also not meant to be this wide and stereo-filling entity like a future bass supersaw. Meanwhile, there is a preset for strings on a stereo enhancer because often strings are kind of like pads these backing entities of sounds that you kind of want to be mix filling and don't need to be focused.*

So with unison you want to think what the purpose and function of a sound is. Often a lead you'll want to be more focused and in your face and sometimes even mono. That doesn't mean it can't have unison, in fact, often times a (very) width lead layer gets layered under the focused (more) mono layer for extra fatness. Same with bass, you'll want that more focused usually so (almost) mono but that doesn't mean you can't layer a wide bass with/under it. Or, you can straight up make your patches some kind of wide (but that they are still centered which is the point but have some width) but usually your focused patches you'll want less voices and less detune in case you add a bit of width just to keep them more focused.

*Intermezzo: Contrast is important and cool stuff has been created by working around wide ande centered patches. [A common complextro thing is to have a centered bass quickly followed by a wide supersaw stab making for a really cool contrast](https://www.reddit.com/r/edmproduction/comments/1bz53t/how_often_do_you_use_stereo_width_techniques/). Or having basses fast following eachother having different widths or even automated widths for cool stereo imaging fx. Again, goes hand in hand with "if everything is wide nothing is".*

In short, you can use unison on a lot of patches but think about the purpose. A pad usually benefits from this, a chord stack that is meant to be filling usually too, leads, bass and other elements you want to be careful width. Either way, look at some (e.g. Serum) presets and look at their unison settings (for leads and basses). Do keep in mind they may be exagarated as lots of those are designed to sound good and huge on their own.

### LFO
- https://www.reddit.com/r/edmproduction/comments/o1chd/can_someone_explain_how_lfo_works_or_synthesizers/c3dnahi?utm_source=share&utm_medium=web2x&context=3
- https://www.bhphotovideo.com/explora/pro-audio/tips-and-solutions/fm-synthesis-demystifying-frequency-modulation-synthesis
- https://producerhive.com/ask-the-hive/what-is-an-lfo/

An LFO is a low-frequency oscillator. Unlike our audio oscillators it's not wired to the audio output so it won't make sound itself but even then it doesn't matter because it oscillates at 20Hz and less (inaudible to the human ear).

An LFO also vibrates just like any other oscillator, however, you don't ADD it to the wave. No it's about source and destination (also called modulator and carrier) where one wave is the modulator (in this case our LFO) and the other is the carrier on which the modulation is imposed.

Now, because the modulator wave oscillates, usually a sine but in Serum we can make it a lot of weird-looking waves, the carrier will get that imposed on itself but of course we need to impose it on something of the wave. We can impose it on the volume in which case that oscillation will basically control the volume parameter (visually seen as the knob) and it will have cool gating kind of sound. We can also increase or decrease the oscillator speed to have the parameter be modulated less or more quickly. Note that even though 20Hz is very little for audible stuff, it's already quiet fast in terms of modulating a certain parameter.

So why use an LFO and why not above 20Hz? Well above 20Hz we come more in the territory of modulating a carrier with a wave that goes so fast rather than it being something that just pulses actually becomes something else. For example, if we modulate the pitch with an LFO at 100Hz (not an LFO technically anymore) then the pulsating pitch is so fast that rather than hearing it as an LFO and a wobble we actually hear it as one wave but just extra added harmonic content. In fact, this faster modulation of pitch (i.e. frequency) is called FM synthesis (see above).

So yeah once you start hitting fast rates you start modulating an audible audio signal (carrier) with another actual audible audio signal (modulator but with an actual "audible" signal/wave). And this adds it's own shenanigans like some dope movement and harmonics. A classic example is an FM bass. Of course you can get same-ish with subtractive synthesis and distortion and stuff like that but FM is just a cool breath of fresh air and also it's difficult to produce certain FM sounds with subtractive synthesis.

So yeah, that's why we use LFOs and why we usually don't use them above 20Hz (we can do briefly for certain cool automations) as it loses the point of adding an LFO.

#### LFO vs. automation
Now, usually you want to use an LFO for stuff that needs to repeat in a deterministic manor. For example, you can use it for arp-esque qualities of your synth. Or you can use it for a reese bass. However, often, in for example a reese bass you want these to be controlled in the way you want. Like, perhaps you want the bass to stay closed in a section and then gradually open up but in the chorus you want it to do some crazy filter stuff. So, instead of having the reese-open-up on an LFO, we have it on a macro (in synths with a macro or mod wheel) and then we can automate and choose ourselves when the bass opens and when it doesn't. So it depends on what you need. You may also use an LFO for something and then have a macro on the LFO settings (like speed) and stuff so that you can kind of change the sound like that for some reason.

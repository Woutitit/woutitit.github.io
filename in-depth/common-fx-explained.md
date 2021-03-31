Here dive into all fx, what it is, different kinds of them (like reverb convolve and algo or tube dist or something else). Explain what it does to a sound (like add warmth harmonics)
why we want it, how much we want it and even how to chain them properly (like which come first which come second etc.)

If your drum samples arent cutting through or punch enough, especially for hard hitting genres, check your samples check your processing and try to find new ones. Normally, if you pick the correct samples you have to do very little processing at least for the base groove to sound good. The longer you go the more you know what you need. Again hear and watch others song and check the waveforms of their drum (and maybe even render out AFTER processing (and before and or after mastering). Usually the very hard hitting drums are quiet stacked in the transient (like loads of highs, kinda distorted to give transient vible and because so compressed the body really comes out too). Of course highlighting of the freqs can help as basic VACS.
## Vocoder
https://old.reddit.com/r/synthesizers/comments/lwiwme/vale_daft_punk_waldorf_vocoder/gpizulu/
https://old.reddit.com/r/synthesizers/comments/lwiwme/vale_daft_punk_waldorf_vocoder/gpizeyo/
https://www.musicradar.com/how-to/how-to-get-the-most-out-of-vocoders-a-complete-guide

Makes stuff sound metallic roboty, often done on dubstep basses and voices. Note that it's important that for samples you'll not want to sing in pitch as usually, especiazlly for beginners, you'll articulate letters worse at certain frequencies and with the vocoder you can synthsize it to melody either way (like the vocoding process makes the audio less understandable and less quality which is why you want good articulation and good like consistent words and stuff). Of course, you can throw it on samples regardless though, especially ones in the background, shouldn't degrade sound too much.
## Compressor:
Jzz drums don't get compressed for dynamics, all the rest usually compression? Rhythm guitar also compression, lead none why?

So it's good practice, for if you want to keep your transient to not make your attack time too low since otherwise that transient will just be squashed with the body, while the transient is supposed to be high energy (does that mean amplitude for a brief amount of time?). Of course, if you want to compress the transient out or don't care, a short compression attack time can also work:
https://www.youtube.com/watch?time_continue=2&v=HkSnIw40oZk&feature=emb_logo

## Distortion
Is just shaping a wave. So waveshaping vs. saturator maybe even? Or they the same?

### Saturation
Mention all types of saturation and how it differs from the rest and use cases to use this one over the rest.

### Overdrive
Mention all types of overdrive and how it differs from the rest and use cases to use this one over the rest.
### Distortion
Mention all types of distortion and how it differs from the rest and use cases to use this one over the rest.

### Bitcrushing
https://en.wikipedia.org/wiki/Bitcrusher
https://www.musicradar.com/tuition/tech/distortion-saturation-and-bitcrushing-explained-549516

Mention all types of bitcrushing and how it differs from the rest and use cases to use this one over the rest.

Bitcrushing adds distortion by downsampling its input. The heavier the bitcrush the more downsampling it does. Usually bitcrushing reduces both the sample rate and bit depth meaning both aliasing artifacts and quantization error distortion become more noticeable. If done correctly this "digital distortion" can really add some "retro warmth" to a certain instrument since in 8-bit times and stuff this was how sounds sounded. (Can we also bitcrush without lowering sample rate? Wouldn't that be better? Or? Like, what are use cases?)

checkout the dim vs hyper and checkout why for dubstep basses or stuff we often add soemthing but we always put one or the other on 0% in the mix. Why is that? and what's the difference between the effects?


### Distortion notes
- Thus can distortion also be about shaping a wave by REMOVING harmonics (such as downsampling, tho aliasing adds harmonics again)?
- Tho in music usually we say distortion is a heavier form of saturation so is that technically incorrect then?
- So this is all about altering sound by shaping the wave.
- Why did warmth become a thing, why do we want that? Cuz analog gear and tape tubes and what not?
- Tube = warmth why? tube distortion = saturation = warmth why?


## Reverb
So unles u wanna go for that ultra DRY fx u'd want reverb cuz EVERY sound in the real wolrd is heavy on reverb no matter how small it is. Therefore, synth sounds that usually don't have reverb out of the gate often sound unrealistic ungrounded so u want at least a bit of reverb on it usually (unless heavy DRY fx stuff).





































## Notes
To illustrate that, consider first a totally random linear transfer function (a function that describes the relationship between its input and output) where the input maps proportional to the output (so a linear MAP, not function in this case). That can be literally only 1 function format:

f(x) = mx (where m is amplitude in the case of audio)

Any other linear maps such as "f(x) = 5x + 6x + 7x" can - according to some high school math rules s- simplify to "f(x) = 18x" and from the moment you introduce an exponent (higher than 1) your function is non linear.

Anyway, any sound wave is also a function so our input "x" will be a function. In this case:

y = sin(2πft) (phase excluded) (f = frequency, t = time, A = amplitude at given time)

so taylor series handy for calculations like sine, cuz sine hard to calculate, so want to approximate???
or:

f(t) = sin(2πft)

And of course, if this sine wave was a 1k Hz sine wave and we want to know what the amplitude is of this wave 2 seconds into playback, we can solve that:
and each wave can be made up of sine waves let's not forget, is important here, like this function represents all possible waves, if we add these general function but with different f (harmonic f only i guess then)
f(2) = sin(2 * π * 1000 * 2)


For this, we have to look at the non-linearity of the (memoryless) playback system. 

To start, I think we can all agree that the non-linearity inside a playback can be represented by a non-linear function. Whether, that function changes with each playback doesn't matter, it's always a certain non-linear function. Now, non-linear functions can get really complex and are almost always not easy (and with nice properties) polynomial functions (https://www.mathsisfun.com/algebra/polynomials.html) so calculating the harmonics would get hard. However, thanks to a dude named Taylor(?) we can express ANY function as a special form of a power series, that is a Taylor series. In fact, a Taylor series IS always a polynomial (Now, note that this expression is just an approximation unless you would calculate the Taylor series to infinity at which point the Taylor series and function are equal(?)).

f(1000Hz) = 2.5x + 20x²

2500Hz + 

now for inputting more than a sine (so pure tone is different) is there already intermodulation between just the harmonics i guess so but very little, like with the white noise u could see that it was intermodulating itself so negligible i guess timbre or nah?



so tyalor series is good for anything that doesn't have memory (so systems that remember stuff after u playbacked stuff in it, making the non-linear function change based on what they remember, for that the volterra series is handy as it calculates that: https://en.wikipedia.org/wiki/Volterra_series)

strong non-linearity can't be represendted by Taylor/Volterra, only weak non-linearity can but is strong non-linearity even relevant to an amplifier?

transer function is just a function that describes relationship in and out, linear transer functions could be

f(x) = 5x + 70
f(x) = 7x + 90

Of course, transfer function don't need to be linear. Can also be called mapping functions?

THD 100% is square wae as it contains all multiples of fundametal (so also odd, but why not contain even)

f(200 Hz) = 200Hz + 200Hz³



so approximation around desired point can be 100% accurate but apprxomiation around 0 is macla series then?


we'd only be able to waveshape it in a harmonic way, i.e. every added harmonic would be completely harmonic. Not only that, every harmonic would be an integer multiple This is because This is because ANY waveform can be created through the Fourier transform series

any non-linear function can be replaced by its power series (Taylor series), so every non linear system can be described by a Taylor Series (or Voltair series). Why? And thus ud only able to become integer multiples of the sine wave.


This type of distortion adheres to the harmonic series and thus the way this distortion adds harmonics is in the exact same way as harmonics happen on any instrument (causing there timbre).

In a non-linear playback system, harmonic distortion can only occur pure tone or also just one signal but with harmonics, do the harmonics not cause harmonics? are these third order harmonics or what?

non-harmonic means it doesnt fall onto frequencies that aren't in the 12-TET frequencies, like all these notes have 12-TET and thus if the frequency added aint harmonic, then screwed. Therefore, with distored guitar, playing a octave + fifth is good cuz the difference tone it creates is harmonic but with a third the difference tone is non-harmonic!!!!!!!!





Non-harmonic distortion is everything else, any type of distortion that doesn't have a harmonic relationship with the sound waves that you are distorting is non-harmonic. An example of non-harmonic distortion is IMD

### Intermodulation & Intermodulation distortion




But yet again, when we refer to distortion in audio we also never refer to "linear distortion". We pretty much ALWAYS refer to the non-linear distortion part. To thus sum up, the full definition of distortion that we mean in audio is:

Distortion is any non-linear wave shaping done on a wave.


Now, I am not sure whether removing
resonant frequencies what is it and why u gotta not remove them but lower them and how identify them
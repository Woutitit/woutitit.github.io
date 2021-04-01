[Home](../index.md)

# Intermodulation
## Table of contents
1. [TL;DR](#tldr)
2. [Harmonic distortion vs. Non-harmonic distortion](#harmonic-distortion-vs-non-harmonic-distortion)
3. 
## TL;DR
- https://www.youtube.com/watch?v=jvV_ga3X0Cs

Intermodulation is a phenomenon that happens to a signal when two things are true
- Multiple tones played at once, i.e. if a pure tone is playing there is no IMD
- Those tones running through a non-linear system (an analog playback system or distortion)

Basically sum and difference frequencies will be created and heard whenever a complex tone runs through a non-linear system. These sum and difference frequencies are very often inharmonic (such as with 3rds, 9ths, etc.) and thus don't sound very nice. That said a root, a fourth, a fifth and a tritone do happen to have sum and difference tones which are harmonic and in tune. This is why a distorted guitar often plays power chords which is root > fifth > fourth (octave).

As a producer, you need to simply realize that with little distortion and saturation, the intermodulation might add some warmth content as it's not really audible. Therefore, you can still play 3s and 9ths and stuff with the patch and it sounds good. However, when you have a heavily/decently distorted patch, you'll just want to probably watch out for playing notes together and kind of stick to the ones we mentioned. You can play the 3rds and 9ths more as a stylistic chaotic choice I guess. 

Also, the lower you are the more natural beating there is anyway per usual so the higher in frequency the more you can get away with it (the further the notes apart too?). Distorted sound often also are harmonically rich anyway so no need for dense stuff but if you really need/want to play a lot of decently distorted sounds together you can create seperate distorted patches and play single notes together like that. It will actually sound "clean" since there is no IMD happening since all notes are all going single through their own distortion and after that it's just additive of those distorted signals. So yeah, a distorted bass and a seperate distorted guitar can therefore sound nice and not too dissonant and stuff. Either way, for the rest you don't really have to care and it's mainly using your ear to gauge whether it sounds bad or not.

## Harmonic distortion vs. Non-harmonic distortion
> See "Sound basics" for a refreshment on intervals, overtones and harmonics".

https://en.wikipedia.org/wiki/Total_harmonic_distortion
https://electronics.stackexchange.com/questions/494928/why-harmonic-distortion-and-not-at-other-frequencies
https://www.quora.com/Why-is-harmonic-distortion-not-at-other-frequencies

So, there are two types of distortion: harmonic and non-harmonic distortion. The first is alles called "Total harmonic distortion" (THD) (I guess, if nothing non-harmonic is in there, it's totally harmonically distorted?) and refers to distortion that is....as you guessed harmonic. What this means is that the frequencies this type of distortion creates COULD BE located at any possible harmonic there is. In other words, the frequencies created will ONLY be created at the EXACT frequencies of one or more of the 12 different notes that we use in our standard 12-TET system at ANY octave. Any frequency created that does NOT correspond to a frequency of any of these 12 notes at any octave is thus automatically non-harmonic.

Now, important to note is that "non-linearly waveshaping" ANY wave ALWAYS results in ONLY harmonic distortion of that wave. Intuitively, this makes sense because if we look at a sine wave its distorted form (in any non-linear system) we can see that the distortion in the latter has a period equal to one cycle of the original sine wave, i.e. the distortion in every cycle of the sine wave looks the exact same (like the ripples and shit look the same in/per each cycle). Additionally, what this also implies is that the fundamental frequency in the distorted sine wave is also still that same original sine wave (pure tone) since we can see that the longest waveform (so lowest frequency) in the distorted sine also still has the same wavelength as the original sine. Therefore, what we can conlude is two things:

- The distortion did not alter the fundamental frequency
- The distortion added frequencies that ALL nicely repeated themselves per cycle of the fundamental since each cycle clearly has the same distortion.

What we can deduct from that is that *the only frequencies that the distortion added were all integer multiples of the fundamental, which per definition are ONLY harmonics*. We know this because any other frequency would not be able to end and start a new cycle right at the end/beginning of one cycle of the fundamental (which would make the distortion not look the same per each cycle of the fundamental wave). This, intuitively, is why distortion only adds harmonics.

To completely bring it home, here's an example. If we had a 440 Hz sine wave (A note), then only 440 * 2, 440 * 3, 440 * 4, etc. Hz harmonic could come out of distortion since these all exactly match there beginning/ending of one of their cycles with the beginning/end of the fundamental cycle. For example, a 440 * 2.5 Hz frequency does NOT (always) do that (note that it's not an integer) and since we can see on an analyzer that the distortion is always the same, and repeats per period of the fundamental, a 440 * 2.5 Hz harmonic is impossible to get through distortion (at least harmonic distortion) and therefore non-harmonic distortion is impossible to get with a single wave.

Now, of course, this is all just intuitive speech. We didn't explain why exactly distortion - when we playback a single distorted wave - actually is periodic. Now, the actual reason why is a bit harder to explain. But basically it comes down to the fact that, if we'd let any pure tone go through a non-linear function, assuming that this pure tone is continuous (as it should be) the only thing that can ever come from it is the pure tone itself and some of its harmonics.

Now, this sounds like a bold claim because after all we don't know what the non-linear function is for any playback device, however, we can back up this claim with the *Taylor series* (Or, another series called Volterra for systems with memory). Now, what the Taylor series is (see my Math documents), it's basically a function approximation tool around a local point that assumes that the non-linear function can be represented and approached by a polynomial and thus a power series:

output =  a + bx + cxÂ² + dxÂ³ ... (where a is usually 0 since we're talking about a linear map, see non-linearity in audio notes).

Then what we do is decide with how much accuracy (so to what order) we want to approximate the function. In distortion, we usually look to the third order:

f(x) =  a + bx + cxÂ² + dxÂ³

And so, now we basically have our output function that represents the output of a non-linear amplifier.

Now, the reason why this can ever be accurate is because, as you can see, the coefficients of this function are unknown and calculating the coefficients is what is going to give us the accuracy. Now, it's a pretty complicated thing that I can't grasp, but we do that based on the derivatives evaluated at a certain point of our to-be-approximated function (we thus need to know the solutions to our derivatives) and these derivatives will actually give us information in how an audio signal will behave in any non-linear system (at least locally):

https://www.eeweb.com/profile/christopher-marki/articles/the-taylor-expansion-for-rf-mixers-pretty-and-pretty-useless
https://www.okdxf.eu/lankford/Bidirectional%202nd%20And%203rd%20Order%20Intermodulation%20Distortion.pdf
https://electronics.stackexchange.com/questions/102720/why-does-a-nonlinear-system-cause-inter-modulation
https://electronics.stackexchange.com/questions/494928/why-harmonic-distortion-and-not-at-other-frequencies
https://betterexplained.com/articles/taylor-series/

Long story short, the point is that in a non-linear system, a sine wave can only come out as a sine wave and other harmonics added. Nothing else is possible. Therefore, when distortion happens, it only adds harmonics and no non-harmonic content.

However, using Taylor series, we can also see what happens when we have two signals (or one signal with harmonics, so not a pure tone) go through a non-linear output. In that case, actually you'll see that not only harmonic frequencies will be created but also sum and difference frequencies too between frequencies. So, if you have two pure tones, they are going to create sum and difference frequencies and the Taylor series indeed shows that THESE frequencies are INDEED non-harmonic. Now, this effect becomes (exponentially?) worse and worse with the more harmonics you add, like in the video of fabfilter, if you add white noise and a pure tone, so many difference and sum tones are going to be created.

Anyway, this effect is also called **intermodulation**. And basically, what you need to know about intermodulation is that it thus creates sum and difference frequencies (you don't really need to know why, too complicated) and so we can calculate that when two tones play together, that if their sum/difference isn't harmonic, it's possibly not going to sound well on a playback system. Now, remark that for us we only need to care about *IMD* with distortion since it's a non-linear plugin and thus creates extra harmonics. This can cause IMD. Now, obviously, with low distortion we will probably not hear it because the harmonics that modulate between eachother might not be hearable, but when distortion is high enough, and even harmonics modulation can be heard (like a distorted guitar), we can hear the intermodulation. This is why we often play only power chords on a distorted guitar since thirds, sevenths, etc. create a lot of non-harmonic sum/diff frequencies which can be heard on a distorted guitar:

https://www.youtube.com/watch?v=jvV_ga3X0Cs
https://www.reddit.com/r/audioengineering/comments/7psy72/what_is_intermodulation_distortion_how_do_you/

Now, again, IMD only happens if you have a non-linear playback system or if you run your instrument through a non-linear plugin such as a saturator and distortion that can create extra harmonics and depending on how bad, you might want to stay away from thirds, etc. Also, if you do want a third interval, what you can do is have two distorted instruments play the interval since in that case you actually run two distorted tones through two seperate distortion so they won't modulate eachother and so the third interval is going to sound cleaner as mentioned in the video. But yeah, overall, when producing, we just need to use a bit of our ears to see when we're using distortion on a certain bus/instrument whether it is adding too much non-harmonic content that it thus sounds bad. In case of a heavy distorted guitar we thus know we can reduce the badness sounding by having less distortion and/or by playing power chords because they have nice sum/diff frequencies (of course you can use non-harmonic stuff as an effect, if you like the dissonance). Or, if you want to keep distortion and play thirds, you can maybe try having two seperate distorted guitars play it since you know that then IMD will not be present.

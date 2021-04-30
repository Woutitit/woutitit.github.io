## Distortion
## Todos
- Write here about the phenomenon of distortion, what it actually is and different types of distortion (difference with saturation, cross distortion, non/harmonics dist, tube, etc.).
- What is fuzz btw and why so famous and what is difference with overdrive?
- Anyway, not really talk about the effect distortion here and point to "Common FX eplained" to talk about like most common distortion and how they are used.

## Intro
When talking distortion we're usually talking about harmonic distortion since eq and stuff and any non-linear wave bending is equal to distortion which simply means distorting, ie chaning a wave.

Gotta look more into it
https://www.reddit.com/r/edmproduction/comments/3flzcp/whats_the_huge_difference_between_saturation_and/

Distortion is like compression actually, like what is difference then cuz yeah both do like reduce dynamic range? I guess a distortion does it by running too hot and stuff and a bit more drastically?

Basically u got all kinds of harmonic distortion. I guess if u hard clip, usquarify ur wave making odd harmincs more prominent and/or adding more odd harmonics of not present. Sofr clipping kinda the same, again only odd harmonics added and stuff but again the clipping cuz its clipping, it chops off stuff fully without altering other stuff i guess(?). Tube distortion is kind of equal to saturation usually (why?) and they add even harmonics though not as simple as that like they add 2nd, 3rd and 4th order. Either way this is usually the go to saturation since it amplifies/adds the even harmonics which are like the octave and fifth and stuff so they generally go well. Tape distortion i sgener ally avoided(?) as it usually mainly addss odd harmonics and they don't play will with fundametanl and are too harmonically defining, especially if even attempting to play chords even when fx is not used a lot.

So yeah, if dont know what to choose go for tube distortion.

And then u got bit crushing which does distortion by adding digital distortion (aliasing?) u kinda wanna be careful witht that but as an fx its cool.

and then got shit like overdrive too.

So distortion is running signal too hot if doing tube distortion kinda act like saturation. Saturation is not running shit too hot but rather faults in equipment adding harmonics, but again non-linear but tube distortion is even and stuff but tape saturation kinda same but also third order harmonic too and stuff so a bit different but kinda same either way (?).

## Intermodulation (Distortion)

In fact, a higher sample rate might even do more good then bad because of a phenomenon called *intermodulation*. Intermodulation is basically amplitude modulation (AM, which is different from FM) between two or more signals and this interaction causes extra undesired harmonics to appear in the output signal.

*The modulation itself is called intermodulation and the distortion caused by the intermodulation is called intermodulation distortion (IMD).*

Intermodulation happens ONLY in non-linear systems such as for example analog playback devices (or distortion plugins) that, due to their components and makeup, are non-linear. Incidentally, in linear systems such as perfect digital DAW playback devices there never is any strange modulation/distortion happening between two or more waves and thus playbacks whatever it has to playback without any artifacts in its playback. Additionally, there always need to be at least two signals (so at least two pure tones) to have intermodulation happening. Compare it with FM/AM synthesis where you also need at least two waves where one can modulate the other (or both eachother?).

Now, for more explanation on this topic see "Non linearity in audio and Common FX explained" but the basic reason that you DON'T want higher sample rate when you playback in non-linear systems and have intermodulation is because if there are frequencies happening in the inaudible ranges, they can actually create more intermodulation distortion in the audible frequency ranges. Like, you have (slightly) audible intermodulation happening anyway between the frequencies that are audible, so you don't want to unecessarily add upon that intermodulation by introducing more frequencies that can thus cause even more intermodulation in the audible range. Now, of course, we usually bandlimit at 20k anyway so we don't have to worry about this problem but you do have to be aware that IMD and higher sample rates thus can be a potential added problem if our signal is not bandlimited (I guess, this is the problem, right? Research!).
--
However, using Taylor series, we can also see what happens when we have two signals (or one signal with harmonics, so not a pure tone) go through a non-linear output. In that case, actually you'll see that not only harmonic frequencies will be created but also sum and difference frequencies too between frequencies. So, if you have two pure tones, they are going to create sum and difference frequencies and the Taylor series indeed shows that THESE frequencies are INDEED non-harmonic. Now, this effect becomes (exponentially?) worse and worse with the more harmonics you add, like in the video of fabfilter, if you add white noise and a pure tone, so many difference and sum tones are going to be created.

Anyway, this effect is also called **intermodulation**. And basically, what you need to know about intermodulation is that it thus creates sum and difference frequencies (you don't really need to know why, too complicated) and so we can calculate that when two tones play together, that if their sum/difference isn't harmonic, it's possibly not going to sound well on a playback system. Now, remark that for us we only need to care about *IMD* with distortion since it's a non-linear plugin and thus creates extra harmonics. This can cause IMD. Now, obviously, with low distortion we will probably not hear it because the harmonics that modulate between eachother might not be hearable, but when distortion is high enough, and even harmonics modulation can be heard (like a distorted guitar), we can hear the intermodulation. This is why we often play only power chords on a distorted guitar since thirds, sevenths, etc. create a lot of non-harmonic sum/diff frequencies which can be heard on a distorted guitar:

https://www.youtube.com/watch?v=jvV_ga3X0Cs
https://www.reddit.com/r/audioengineering/comments/7psy72/what_is_intermodulation_distortion_how_do_you/

Now, again, IMD only happens if you have a non-linear playback system or if you run your instrument through a non-linear plugin such as a saturator and distortion that can create extra harmonics and depending on how bad, you might want to stay away from thirds, etc. Also, if you do want a third interval, what you can do is have two distorted instruments play the interval since in that case you actually run two distorted tones through two seperate distortion so they won't modulate eachother and so the third interval is going to sound cleaner as mentioned in the video. But yeah, overall, when producing, we just need to use a bit of our ears to see when we're using distortion on a certain bus/instrument whether it is adding too much non-harmonic content that it thus sounds bad. In case of a heavy distorted guitar we thus know we can reduce the badness sounding by having less distortion and/or by playing power chords because they have nice sum/diff frequencies (of course you can use non-harmonic stuff as an effect, if you like the dissonance). Or, if you want to keep distortion and play thirds, you can maybe try having two seperate distorted guitars play it since you know that then IMD will not be present.

## Distortion
https://en.wikipedia.org/wiki/Distortion
https://en.wikipedia.org/wiki/Distortion_(music)
https://www.sweetwater.com/insync/distortion/

In audio, distortion is one of those words that is far more generic in meaning than most people realize when they use it. Technically distortion is ANY deviation in the shape of an audio waveform between two points in a signal path. So for example, if we had a square wave and we filtered it with a high-pass filter, we distored the square wave because we filtered some harmonics out which makes the wave not look and sound like a square wave anymore. 

We also call distortion *wave shaping*.

### Linear vs. Non-linear distortion
> See "Phase shifting" and "Linearity and non-linearity in audio".

(https://www.nti-audio.com/en/support/know-how/lets-clear-up-some-things-about-distortion)

Now, practically, we don't really use the word distortion to describe "waveshaping" of every kind because in that sense just about any audio process (equalization, compression, filtering, etc.) are all forms of distortion. When we talk about *distortion*, we practically always refer to *non-linear distortion*, i.e. distortion that causes (negative) byproducts (called harmonics/frequency in audio). Therefore any type of distortion that does NOT cause added EXTRA harmonics is not the type of distortion we're referring to when we say "distortion". Confusing, I know.

An example of non-linear distortion would be if we would playback a sine wave on a faulty speaker and it playbacks as a square. The speaker has shaped the wave into a square, which added extra frequency content. Of course this is unwanted as we just wanted to have a non-distorted playback of the sine wave without any extra harmonics.

** FUN FACT: Even a change in amplitude and a phase shift is (linear) distortion. They both change the shape in the wave as in that the former makes the wave larger and the latter shapes the curve of the wave (since now the amplitude at t = 0 might not be 0, so the curve starting from t = 0 will be different and thus shaped). If you phase shifted AND made a sine wave louder, it would still be just a sine wave (no matter how you switched the processes around) and thus this type of waveshaping is also linear.**

Important to thus remember is that distortion in audio refers to non-linear distortion and I'm also going to refer to non-linear distortion as just distortion in this article. Other examples of (non-linear) distortion are *harmonic distortion, aliasing, clipping, crossover distortion, etc.* Additionally, we also sometimes DELIBITERALY add distortion to a sound with plugins since the byproduct of distortion can definitely be desirable and tasteful if one knows what it's doing (e.g. a distored guitar). 

## Notes
## Notes
(or **intermodulation (distortion)**)

AM vs. FM synthesis????? AM createsharmonics too then i guess fm doesn't create harmonics only makes stuff wobble cuz two waves slightly detuned and shit make stuff wobble.
is AM and FM the same in frequency??? like AM seems to us like french, is it to go lower so we pick up different radio stations ,at lowera mplituds or what? so fm vs am radio put this all in the synthesis article.
the modulation that can happen between two or more signals that results in extra added harmonic artifacts. There need to be two conditions met for it to happen. First of all, somewhere there needs to be non-linearity in the DSP of the signals. Now what do we mean with non-linearity? Well, we mean that the change in output is not proportional with the change in input. In other words, linear systems are fully predictable while non-linear systems are (fully) unpredictable. In DSP, a linear playback system thus also has a linear function, e.g. "playback = f(input signal)". Now, in playback obviously playback = input, like if we input a sine wave we want to output a sine wave. Therefore, any playback system that is non-linear will not just playback its input (unless lucky?) but - in the case of audio - will add extra harmonics. On top of that, not only will they add harmonics, the way in which they add harmonics is also not linear (?). An example of non-linear playback devices are physical speakers. An example of linear playback devices are DAWs.

Now, next to just needing a non-linearity in the DSP, you also need at least two signals (so at least two pure tones) that can actually intermodulate between eachother.

Under the above conditions, intermodulation can thus happen in physical speakers but also when using non-linear plugins such as saturation.

IMD grows like between two waves not too much but with white noise ssoooo much imd going on

so is intermodulation still can happen in linear saturation then cuz drive not turned up? Cuz obviously adding odd harmonics predictablly seems linear like its predictable, or is it about intermodulation DISTORTION???

Hereâ€™s a narrow, and rather aggressive, peak filter. We can clearly see the 630Hz sine being attenuated, but without any partials appearing. This is also (very likely) a linear system:

because of course non linear is non linear in nature doesn't mean that it always produces different results than linear, it could be that were lucky in one time, or that it just happens to be non linear but procudes linear results in some cases. (or all cases in some instances?)

**A linear system can only reduce the signalâ€™s bandwidth, and cannot extend its bandwidth. It generally fulfills the sampling theorem, bandlimiting and aliasing is no issue. More precisely, a linear system is independent of samplerate. Nonlinear systems on the other hand always increase the input signalâ€™s bandwidth. They can potentially multiply the bandwidth up to infinity in no time, a fact that produces great trouble in the context of digital audio synthesis and processing. These systems have the inherent potential of breaking the Sampling Theorem, because new content ranging beyond the Nyquist frequency is likely to appear. If not handled properly, such content will directly produce alias images (also called MoirÃ© patterns), a particularly nasty and irreversible form of distortion. Nonlinear systems, if not antialiased adequately, directly depend on sample-rate.**
=> MOST CONVERTERS THESE DAYS HAVE ANTI ALIASING BANDLIMIT SO WHEN UR PLAYING DIGITAL AUDIO THE ARTIFACTS THAT IMD WOULD CREATE BEYOND SAMPLE RATE AND THUS CAUSE ALIASING IN LOWER FREQUENCIES THAT ARE AUDIBLE ARE ELIMINATED!

https://www.tokyodawn.net/meaning-of-system-linearity-in-audio-production/

As a rule of thumb, the narrower and simpler the input signal, the more harmonic the spectra returned by most nonlinearities. From a more practical view, IMD is the reason why an electric guitar can be distorted like crazy and still sound great. However, doing the same with a pop-song will likely not sound agreeable.
:> cuz power chord input simple only fundamental and fifth and fundamental?

converters bandlimit at 20k anyway


Now, whether intermodulation in speakers is a big problem will depend on speakers but in the fabfilter video, you can see that the guy simulates non-linearity with a saturation plugin (therefore our output will kind of look like as if it where a speaker).


## Upsampling and its benefits

so upsample vs oversample apparently upsample more benefits but in the end all this shit apparently doesn't matter too much cuz in a busy mix u won't really hear this shit.

# Practical Tips & Key Takeaways
So with distortion, basically you don't need to worry that much about possible aliasing/extra intermodulation but one thing that you should keep in mind is to keep at power chords and stuff that doesn't create non-harmonic sounds. Obviously this depends on how bad the distortion is and if you do like the sound (or can't really hear the IMD), then go for the weird intervals. Else, just keep to stacking octaves and fifths basically (like power chords) or let two distorted instruments play the interval instead so there is no IMD going on between them.

For the rest, just be high level aware the distortion can cause IMD and also cause aliasing but know that usually these ain't too much to talk about. As I said, IMD is just a matter of rearranging your notes into simpler things and aliasing is usually not a problem and you'll hear it if it is a problem (see "Aliasing" for more).

## Notes

is distortion always clipping??? or can it just be add harmonics but does that always mean clipping?
https://en.wikipedia.org/wiki/Distortion nah its altering of wave shape so yeah both sample and reso reduction are distortion.

converter band limits anyway
Now, let's start with the only reason where one 
the only reason why one might sample at a higher rate than necessary - that also involves the consumer - is because of possible happening in your playback device.

transer function what is it? Is it to calculalate volterra series, like what the linear to non-linear output would be in theory cuz obviously in practice can still be different of random variables we can't predict.

always have an onverview at the end of key takeaways and practical tips as in, what should i actually keep remembering from all of this.

master checklist => should dither or nah? roll of high end?
Talk about undersampling and up/down sampling too
is that why we see cut off at 20k Hz???? No, it's mostly cuz mp3 loses shit at 18k completely. Some people do and its at 18k Hz a cut off to get some more headroom to compress even more if necessary but yeah, so ain't really necessary usually I'd guess but yeah, should be looked up. So headroom in higher frequencies, i see it a lot tho, thats why cut off there, but why tho? Look up! is cuz high freq can be loud fast or what or we can hear it real loud even if not high in amplitude so if cut off we can compress shit more without shit getting too loud in high freq, is it that?

mp3 is lossy format lossy compression, everything is compression why not keep in tact why compress to wav and mp3 is wav also compression to make smaller or only mp3 what does bitrate have to do with it:
https://www.reddit.com/r/makinghiphop/comments/90u831/selling_mp3_or_wav_file_whats_the_difference/ WAV IS LOSSLESS SO NOT COMPRESSED THEN?
MAIN ADVANTAGE OF MP3 IS LOWER BITRATE THAN WAV AND COMPRESSED SO U CAN STORE MORE ON DEVICES THAT HAVE LITTLE SPACE SUCH AS PHONE

what are odd harmonics really?

i guess odd harmonic dist creates more interesting dist cuz not just octaves higher than the fundamental than even harmonic which are always double Hz of last multiple, thus always an extra octave. Is the interest part correct? look up odd harmonics vs. even harmonics distortion and when to use either one.

SO INTERDMODULATION IS PHYSICAL?????? AND ALIASING IS DIGITAL ONLY WHAT IS THE DIFFERENCE CUZ I THINK INTERMOduL CAN SLTILL BE DIGITAL NON LINEAR SHIT

LIKE EVEN IF CLIPPING THEN U GET HIGH LINEAR SHIT 

LIKE IF CAUSE HARMONICS SUDDENLY U CAN GET HARMONICS ADDED IN UPPER RANGES AND THUS CAUSING AUDIBLE ALIASING IN LOWER RANGES:

side band with compression if compression harsh enough it causes clipping thus distortion thus harmonics
again all this is irrelevant to synth sound. can synth sound have aliasing with reflect

power chords and blablabla intermodulation its cuz the distortion is non linear plugin and thus causes intermodulation distortion? and the more chords, or odd harmonics the worse, so thats why u play octave and fifth cuz like not too many odd harmonics and shit?????


The main benefit of higher sampling rates is only relevant to music producers.

psampling and downsampling by integers is much easier and has higher fidelity rather than by fractional amounts. The cost/benefit of upsampling by 2 from 48 to 96k is greater than upsampling by 3 from 44.1 to 132.3 if y so easier for algorhitms

 88.2/96Khz is a whole other ballgame. Has twice the resolution of 44.1/48 and is thus easily down converted without the need for fancy math. so thats why doubling to higher sample rate cuz easier math if we go with high sample rate anyway
 
 Sample rate conversion so when u convert high to low sample rate of low to high i guesss that's up and down sampling? okay this is a whole other ball game i need to investigate for a second

both 48k and 96 hz are common why i mean 48 times two is 96 why not have 88.2k hz which is 44.1 k Hz
still about harmonics if not oversampling but just higher rate

difference is that aliasing is digital and intermodul is analog like speaker
s hq is upsammpling

 Briefly mention upsampling and say it has no benefits also mention downsampling and undersampling, difference but point to "Common FX explained". There we can also add section for resynthesis and resampling. Also say here some stuff about *sample rate conversion* and say that perhaps chaining a lot of those might cause some audible distortion but not much (?).
 So what about resampling?


https://en.wikipedia.org/wiki/Sample-rate_conversion

tape hiss what is tape hiss how does it occur and can it do stuff? like make shit sound more analog

## Distortion
https://en.wikipedia.org/wiki/Distortion
https://en.wikipedia.org/wiki/Distortion_(music)
https://www.sweetwater.com/insync/distortion/

In audio, distortion is one of those words that is far more generic in meaning than most people realize when they use it. Technically distortion is ANY deviation in the shape of an audio waveform between two points in a signal path. So for example, if we had a square wave and we filtered it with a high-pass filter, we distored the square wave because we filtered some harmonics out which makes the wave not look and sound like a square wave anymore. 

We also call distortion *wave shaping*.

### Linear vs. Non-linear distortion
> See "Phase shifting" and "Linearity and non-linearity in audio".

(https://www.nti-audio.com/en/support/know-how/lets-clear-up-some-things-about-distortion)

Now, practically, we don't really use the word distortion to describe "waveshaping" of every kind because in that sense just about any audio process (equalization, compression, filtering, etc.) are all forms of distortion. When we talk about *distortion*, we practically always refer to *non-linear distortion*, i.e. distortion that causes (negative) byproducts (called harmonics/frequency in audio). Therefore any type of distortion that does NOT cause added EXTRA harmonics is not the type of distortion we're referring to when we say "distortion". Confusing, I know.

An example of non-linear distortion would be if we would playback a sine wave on a faulty speaker and it playbacks as a square. The speaker has shaped the wave into a square, which added extra frequency content. Of course this is unwanted as we just wanted to have a non-distorted playback of the sine wave without any extra harmonics.

** FUN FACT: Even a change in amplitude and a phase shift is (linear) distortion. They both change the shape in the wave as in that the former makes the wave larger and the latter shapes the curve of the wave (since now the amplitude at t = 0 might not be 0, so the curve starting from t = 0 will be different and thus shaped). If you phase shifted AND made a sine wave louder, it would still be just a sine wave (no matter how you switched the processes around) and thus this type of waveshaping is also linear.**

Important to thus remember is that distortion in audio refers to non-linear distortion and I'm also going to refer to non-linear distortion as just distortion in this article. Other examples of (non-linear) distortion are *harmonic distortion, aliasing, clipping, crossover distortion, etc.* Additionally, we also sometimes DELIBITERALY add distortion to a sound with plugins since the byproduct of distortion can definitely be desirable and tasteful if one knows what it's doing (e.g. a distored guitar). 

### Harmonic distortion vs. Non-harmonic distortion
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

output =  a + bx + cx² + dx³ ... (where a is usually 0 since we're talking about a linear map, see non-linearity in audio notes).

Then what we do is decide with how much accuracy (so to what order) we want to approximate the function. In distortion, we usually look to the third order:

f(x) =  a + bx + cx² + dx³

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





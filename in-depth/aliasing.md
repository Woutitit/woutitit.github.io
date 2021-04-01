[Home](index.md)

# Aliasing
> For beginners, I highly recommend reading "Audio quality & Recording" first.

## Table of contents
1. [TL;DR](#tldr)
1. [Introduction](#introduction)
2. [Situations in which aliasing occurs](#situations-in-which-aliasing-occurs)
3. [Possible solution: High sample rates and oversampling](#possible-solution-high-sample-rates-and-oversampling)
4. [Conclusion](#conclusion)
5. [FAQ](#faq)
6. [Sources](#sources)
7. [Todos](#todos)

## TL;DR
Aliasing is a **digital-only** phenomenon that creates reflections in your signal making it sound less clear and bad. It only happens when a signal passes the nyquist rate so it only happens for high tones and/or very high harmonics.

To explain a bit more, whenever a signal exceeds the nyquist rate, the stuff above that rate will start to alias and reflect down as these tones are not reproducable in an accurate way. Instead, they'll be represented as lower tones/harmonics in your signal and you might hear those artifacts (see the fabfilter video) which are unwanted.

Now, note that at a default sample rate of 44.1k Hz, we usually don't have to worry about aliasing as most of our fundamental tones and harmonic content will fall between 0-20k Hz anyway so the stuff that falls beyond 20k Hz (i.e. beyond the nyquist rate) will be so little usually and the mix will also usually be quite busy (or busy enough) that you don't hear it. It's only if you're working with (very) high tones in a sparse mix that you might hear aliasing being produced. For that case it's nice to at least recognize how aliasing sounds like.

## Introduction
Aliasing is an effect in which certain frequencies aren't represented as they really are, i.e. they have an alias so to speak.


A first unwanted phenomenon we're going to look at is aliasing. The above article explains aliasing well (TODO: Do explain it here so in "above article" we can reference this article even though we might need some terms from "above" article, but we can hint to that here) so here I'm just going to mention that it is a strictly digital phenomenon since it relates to the limitations of sample rates.

## Situations in which aliasing occurs
A first situation where aliasing can occur is in audio (so analog) recording. If you don't set a bandlimit in your audio interface and you record frequencies beyond your sample rate's nyquist frequency, you'll have all those frequencies being aliased. Now of course, in this case it is easily solvable by simply bandlimiting our signal at the nyquist frequency (which practically every audio interface does for us) so that only frequencies below that get recorded, and thus the whole recording is properly sampled.

A second situation in which aliasing can also occur is in DIGITAL synths. Again, remember from "Synthesis" that digital synths also send discrete values to the speaker at a certain sample rate so they are also prone to aliasing. Now, luckily, this one is also easily solvable as a lot of synths have options such as "band limiting" which limits the band at (I assume) 20k so no frequency content is played beyond and thus no aliasing occurs. Synths also offer oversampling options as an alternative to band limiting (as we'll explain in a minute). It's often inaudible though and most synths actually do apply an anti-alias filter once rendered as audio so there isn't a problem there but regardless it might ocassionally be annoying to work with before you render.

Now, a third situation in which aliasing happens, is in non-linear fx (see "non-linearity in audio" article) plugins such as distortion (both in your FX rack or synth FX rack, like, serum as both obviously act the same way and our FX AFTER a wave is generated. The synth anti-aliasing is only relevant to the wave itself (and its harmonics)?). In this case aliasing happens because if you have a (very high) note and you distort it, harmonics (may also) get added beyond the nyquist frequency and thus aliasing occurs. Now, this one is actually impossible to solve with our usual technique of just band limiting at 20K. The reason for that is because distortion adds harmonics on its own, meaning that even if you anti-alias your synth, you can yet again add harmonics on top of the anti-aliased synth and yet again create harmonics in the ranges beyond the nyquist frequency which cause aliasing to happen. And the worst part is that you can't even filter out these unwanted harmonics because the harmonics get added by the distortion and thus the aliased harmonics are already in the signal before the filter happenss. This is how the DSP goes:

original signal > *heavy distortion happens* > distorted signal with aliasing > *filter at 20k happens* > distorted signal with aliasing except above 20k

DSP is an additive process. This is why you also can't chain two saturators at 50% wet levels and expect it to behave like one saturator at 100%. The latter will create harmonics ON TOP OF and BASED UPON the harmonics created by the first saturator. It's a chain, not an evaluation at the end (which would be impossible and perhaps inpractical?). Trying to filter out aliasing from a distorted signal is like recording an already aliased signal at the nyquist rate, it won't do anything except filter out the harmonics beyond nyquist which weren't audible already anyway.

So yeah, in the first two examples aliasing is easily solvable but it's mainly non-linear plugins such as distortion/saturation that will give us a harder time and we'll look at some ways on how to soften it in a minute. That being said, though, aliasing is usually not a huge deal since the (very) high harmonics (that come from distortion) are not that powerful, since they already come from a long path way down in the frequency spectrum. You can thus imagine that not a very huge amount of harmonics, and certainly not powerful, will be going beyond the nyquist frequency and therefore the aliasing, even the aliasing that happens in the audible spectrum, will be so little that we can't hear it. Certainly not in a busy mix. So, in other words, aliasing in distortion really only matters if you're actually playing very high distorted notes since then the fundamental is already high, so there will be a lot of harmonics beyond nyquist that are decently powerful to be heard. But even then the aliasing might not even be that noticeable and this is also not a practical example.

Also note that I previously said that aliasing only occurs digitally. Because, a distorted guitar (which we distort with an actual analog amp) which we record with a microphone can never alias since in analog world, we can distort as high of a sound as we want, there is no sample rate at which aliasing occurs since our generated wave is analog. And thus, recording this wave we only need to worry about setting a bandlimit in our interface to make sure that aliasing does not occur due to sampling that fully non-aliased wave.

Either way, in digital world, we're sometimes better safe than sorry (like as putting a limiter on the master to prevent earrape). We can soften aliasing certainly - if we're not sure if certain signals will actually cause us some (minor problems) - with *sampling techniques*. However, we will after that also look at a phenomenon that might not always benefit (and even worsen) from these techniques.

## Possible solution: High sample rates and oversampling
One obvious solution to the above problem is to just increase the sample rate setting in the "project settings". As the fabfilter guy says (in his video around 11:25), everything that uses the internal project sample rate - such as plugins and digital synths (most likely?) - will then use the higher sample rate. This way, when distortion gets applied, aliasing occurs way less because of the higher sample rate we set. This can be a good solution if we set the sample rate high enough, though, it isn't practical. You see, just setting our whole project's sample rate to double, or quadruple the sample rate size will eat CPU like crazy because EVERYTHING that uses the internal project sample rate will use that sample rate. And, on top of that, we have not even solved the problem completely yet. This is the reason why we favor *oversampling* instead.

Now, oversampling is pretty much the same as setting the sample rate higher, but usually with oversampling we refer to oversampling done within a plugin rather than the whole project. Also, in that same context, usually oversampling kind of refers to setting the sample rate MUCH higher, instead of just double.

Now, the reason why oversampling is beneficial is because of the way it works. You see, a (good) distortion plugin has an internal oversampling option (which is usually a multiply of the project's current sample rate). This way, ONLY the signal passing through the plugin will be affected by this oversampling and no other things, this obviously saves CPU (drastically). Now, that's not the only real benefit. Because, it also works in a really smart way:

receives signal > upsample to plugin oversample setting > apply distortion > filter beyond project sample rate setting > downsample to project sample rate setting

Basically, with oversampling, we're taking a signal and temporarily upsample it. This way, when we apply distortion less aliasing will occur obviously. And after that, to reduce the sample in size so it doesn't eat too much storage, we downsample it again to the original project sample rate. Now obviously, all the frequencies that we have added with the distortion will alias again if the distortion would just downsample, rendering us the same end result as just applying distortion to a "original sample rate" signal. Therefore, before we downsample, we also filter out all the frequencies and harmonics beyond the nyquist frequency of the project. This way, when we then downsample, we have no "low sample rate aliasing" occurring anymore since the frequencies that would cause that are filtered out.

Now, obviously with the oversampling technique, the aliasing is not gone. We're doing pretty much the same as we're doing with just setting the project settings' sample rate higher. HOWEVER, there is a massive difference. You see, it might not have occurred to you yet, but with oversampling (which is HQ in fabfilter Saturn - which is 8x over sampling - and just "Oversampling" in Fruity WaveShaper, HQ has different meaning between the two plugins, I know, it's confusing) we're basically getting the aliasing of a much higher sample rate at a low sample rate. For example, if we have a normal sample rate of 44.1k Hz, and we oversample 8x times, then the nyquist rate will be at 352.8k Hz which means that INCREDIBLY high frequencies will only still alias (so pretty much nothing). However, since we downsample back to 44.1k Hz (with filter of course), we still have that same aliasing of the 352.8k Hz even though our sample rate is 44.1k Hz. So, even though, we sampled at such a high rate, the size of our audio did not increase thanks to the filter and downsample combination.

Now, oversampling obviously does require more CPU then not oversampling but it is still drastically better than setting the whole damn project file at a higher sample rate. And on top of that, because it's so much more CPU efficient than just setting a general higher sample rate, we can actually sample at absurd stuff like 8x, 16x the rate and practically obliterate any aliasing in our audio (TODO: Check exactly how CPU heavy oversampling is compared to general sample rate).

## Conclusion
Now, with all this said, though. Whether you should actually use oversampling or not really depends. Because with oversampling (see compression section fab filter guy) we obviously need to do up and dowsampling, the *sample conversion* (https://en.wikipedia.org/wiki/Sample-rate_conversion) to do this might slighlty create its own distortion if a lot of up and down sampling are chained. Again, in 99% of the cases not a problem, but it is nice to mention here.

Next to that, it also obviously eats CPU, so even if you can doesn't mean you should. Especially if you're not hearing a difference in sound.

Many times aliasing is really not that big of a deal in a mix. And, if you know what aliasing sounds like (especially in vibrato and bends), and know where it is coming from (like synth, plugin, etc.) and or whether it will be solved at render time (like 3xOsc synth aliasing) you don't have to worry about oversampling and aliasing too much while creating a song, you'll most likely hear it (just be aware of very high notes with distortion which might do some nasty stuff but that's pretty much it).

Lastly, setting a higher sample rate (and oversampling in a plugin?) does also contribute to possibly more *intermodulation distortion*, which, with heavily distorted signals, you might need to be careful with (in fact, to reduce IMD, one prefers a lower sample rate, see "Intermodulation" article).

> Watch at the end of fabfilter guy video to see a demonstration of oversampling and the difference it makes in a real mix. It's very hard to hear the difference, right?

## FAQ

### "Many plugins upsample anyway"
https://www.reddit.com/r/audioengineering/comments/52ovdd/interesting_article_on_mixing_and_mastering_at/

So I guess there are a lot of plugins (and maybe audio interfaces) that also do upsample > apply plugin > downsample to get rid of aliasing artificats. I'd suppose that is with non-linear plugins such as distortion (what are other non-linear plugins? Look up!) since with linear plugins aliasing won't happen either way.

### 44.1k Hz vs. 48k Hz vs. Higher
https://www.reddit.com/r/audioengineering/comments/g9y1j1/working_in_48k_vs_441k/
https://www.reddit.com/r/WeAreTheMusicMakers/comments/8ube76/441k_or_48/
https://www.reddit.com/r/AudioPost/comments/bpekcz/48khz_vs_441khz_question/
https://www.reddit.com/r/Filmmakers/comments/1dubis/question_441_vs_48/
https://www.youtube.com/watch?v=-jCwIsT0X8M at 25:00

So, in the end many producers (used to ) choose to record at 48k Hz for two reasons. One is that 48k Hz audio nicely lines up with the sample rate for video and thus when combining the two, we don't need, they will be in sync. This is because 1 second of 44.1k Hz and 48k Hz aren't exactly the same length (why?) and thus 44.1k audio won't sync up perfectly with 48k Hz video. Therefore, *sample rate conversion* should be needed to convert up to 48k Hz from 44.1k Hz. This used to give some distortion to convert upwards to a higher sample rate from a lower resolution (the 44.1k Hz) and also, it wasn't that easy to convert from 44.1k Hz, as it would be from 24k to 48k (which is just doubling). However, in these days, it doesn't really matter whether you use 44.1k Hz and then *sample rate convert* to make it compatible with a movie (or music video?) as it's as good as working at a 48k Hz sample rate (Of course, you do need to be aware to sample rate convert, if you don't set it to 48k Hz and your DAW doesn't convert automatically).

Now, another reason for 48k Hz is that it can relax your anti-aliasing filters more (the ones interal to plugins when they oversample and downsample, or in digital synths at render) than at 44.1k Hz. The reason for that is because at 44.1k Hz you want to completely filter out frequencies at 22.05k Hz to avoid aliasing, but you also DON'T want to start filtering out at 20k Hz since that is technically audible to the human and we would thus lose audible content. Therefore, we only have room of 2.05k Hz to filter (which is basically a very steep brickwall filter). With 48k Hz, you have 48/2 - 20k Hz = 4k Hz room for your filter to work with meaning it doesn't have to be as steep and thus as CPU intensive. Therefore, for this minor sample rate increase you can have all your plugins and vsts and synths that might use anti-aliasing filters relax twice as much as at 44.1k Hz. This might be worth it, but again, it might also not be noticeable.

In the end, as long as you're not doing anything really professional (with film), you don't need to worry about 44.1k Hz or 48k Hz. Anything beyond that is not even worth looking at since that will just eat CPU space without compared to only a minor increase in filter-relaxing benefits.

## Sources
- https://en.wikipedia.org/wiki/Undersampling
- https://en.wikipedia.org/wiki/Downsampling_(signal_processing)
- https://en.wikipedia.org/wiki/Aliasing
- https://www.youtube.com/watch?v=-jCwIsT0X8M

## Todos
- Talk about how it manifests itself, like reflecting and stuff
- Show visually what aliasing does, mention nyquist and stuff.

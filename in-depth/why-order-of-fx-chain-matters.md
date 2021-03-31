# Why order of FX chain matters (Linearity and non-linearity in audio manipulation)
## Sources
https://www.tokyodawn.net/meaning-of-system-linearity-in-audio-production/
https://webcache.googleusercontent.com/search?q=cache:D71j-fgD-6kJ:https://www.tokyodawn.net/meaning-of-system-linearity-in-audio-production/+&cd=5&hl=nl&ct=clnk&gl=be
https://math.stackexchange.com/questions/1835131/all-linear-functions-are-homogeneous-of-degree-one
https://math.stackexchange.com/questions/2483607/superposition-principle-is-not-synonymous-of-linearity
https://math.stackexchange.com/questions/275310/what-is-the-difference-between-linear-and-affine-function
https://math.stackexchange.com/questions/1912970/intutive-difference-between-linear-map-transformation-vs-linear-function
https://old.reddit.com/r/FL_Studio/comments/lijszh/the_order_you_place_effects_matters_a/
https://www.youtube.com/watch?v=tTQMJ-98_x4
https://www.kvraudio.com/forum/viewtopic.php?t=135518
https://www.gearslutz.com/board/high-end/447509-compression-reverb-first.html
https://www.reddit.com/r/Guitar/comments/27i16w/question_about_a_compressor_and_delay/

## Table of contents
1. Introduction
2. Non-linear FX
3. General rule of thumb order
4. Linear FX
5. Notes

## Introduction
The order of your FX chain matters. Not always, but sometimes. When? Well, when you're dealing with non-linear fx. 

## Non-linear FX
Compression, saturation and distortion are the most commonly known and used non-linear FX. So what makes them non-linear? Well, they can actually give us a different output for the same equation. Consider these two chains:

signal > reverb > distortion = output
same signal as above > distortion (same settings) > reverb = different output

So despite having the same signal fed, the same fx fed, the same settings on the saturator, these two will result in different outcomes. Why? Well, it actually makes sense. In the first example, the reverb adds an echo to the signal and the saturator acts on that new harmonic content, now not only saturating the original harmonics but also saturating the reverb harmonic content. In the second example, only the original signal gets saturated and then there will be an echo of that made. In the latter example there will be less mess and less harmonics saturated.

Another example:
signal > high pass filter  at 200 Hz > distortion = output
same signal as above > distortion (same settings) > high pass filter at 200 Hz = different output

In the first case, the saturator will only saturate the content above 200 Hz. In the second, the sub 200 Hz harmonics get saturated too, some of those saturation harmonics reaching over 200 Hz, then that signal gets high passed to 200 Hz but the harmonics caused by saturation of signal below 200 Hz will still be there. So again, in the latter example you have more harmonic content in the end result than in the first where you only saturate the frequencies above 200 Hz (so no potential filt from anything below).

Same with compression (see video) and same when using compression and distortion together.

## General rule of thumb order
https://www.strymon.net/setting-up-your-effect-signal-chain/#:~:text=Dynamics%20(compressors)%2C%20filters%20(,come%20next%20in%20the%20chain.

So as a rule of thumb, and this is purely for mixing/cleanness and NOT creative purpose, there is a general order:
- Compressors (and OTT) first. We want to setup the signal to have a good dynamic range to work with. The FX after will, thanks to that compression also apply their fx, (such as distortion), more evenly.
- Distortions second. They come after the compressor because putting them before might cause some uneveness in the distortion because of untamed peaks and frequencies.
- Modulation FX such as flanger, chorus, etc. second to last as you don't want those getting affected by compression and or distortion, you want them (usually) to ring out as you dialed them in and not have weird tails etc. suddenly that are ugly.
- Time FX such as delays and reverbs last. These last as (even though idk if the modulation are linear so it wouldn't matter), again, you don't want these to be warped in a weird way by other fx (mainly compression and distortion.
- EQ usually after compression and after distortion.  EQ after compressor since EQ changes dynamics and compressor might respond weirdly to that so better to EQ after. Also, if you put EQ before distortion it will color the distortion (since you're boosting and cutting certain frequencies, it may sound nice it may not). EQ after is  more common and is for mixing purposes.
- Filter (High pass/Low pass) may come before compression but usually not. In cases where a compressor may behave weirdly due to weird low-end rumble, cut out first the sub/lows and then start compressing. Same with high pass. Else, put before reverb and delays for cleaner stuff and or before modulation also for cleaner shit (only relevant if these on aux tracks as in putting the filter on the aux track, though most reverbs got their own filterering build in, so not talking about the signal that gets send to the reverb, that one doesn't need EQ before the reverb, its the reverb sound and purely that that needs the EQ.  (?INEVSITGATE THO) (though I though EQ/filters were linear, why chain matters then there?).

Anyway, sometimes there are certain FX or automations that will cause a change in dynamic range (e.g. a filter sweep), this is where EQ is used as a creative process to SHAPE the sound really so that EQ probably belongs first then and then afterwards come the compressors to tame it.

## Linear FX
Linear FX, the order doesn't matter. Linear stuff is reverb, delay, chorus. EQ filtering. If you had a chain with only linear FX, you can place them in whatever order and you'll get ALWAYS the same output. Introduce a non-linear FX and you might have to switch around your linear plugins and place your non-linear FX correctly in the chain.

## Other non-linear FX
https://www.strymon.net/setting-up-your-effect-signal-chain/#:~:text=Dynamics%20(compressors)%2C%20filters%20(,come%20next%20in%20the%20chain.

## Notes
## Introduction
So, first of all, for those who don't know what linearity is, it's basically when I'd be turning a speaker's volume button to set the volume in db and it went like this:
- turn to 0 degrees   => 0db
- turn to +10 degrees => 2db
- turn to +20 degrees => 4db
- turn to +30 degrees => 6db
- turn to +40 degrees => 8db

Notice for every +10 degrees, the db went +2. In other words, the output is linear/proportional and plotted it would look like a straight line.

Now, it's incredibly important to understand that proportionality means linearity but that linearity does NOT always mean proportionality. For example, let's say for some reason our speaker always made sound, even at 0 degrees volume knob and we would have this:
- turn to 0 degrees   => 2db
- turn to +10 degrees => 4db
- turn to +20 degrees => 6db
- turn to +30 degrees => 8db
- turn to +40 degrees => 10db

In this case change is not fully homogeneous/proportional because at 0 we already have 2db. And so, since at +10 degrees we have 4db we would assume that in a proportional system doubling the degrees to +20 degrees would thus result in a doubling too in decibel, so 8db. However,  due to the 2db at 0 degrees, it doesn't, it's only 6db (even though the output is still fully linear) and therefore this linearity is NOT proportional.

Anyway, just to be complete, proportional doesn't mean exponential either because:
- turn to 0 degrees   => 2db
- turn to +10 degrees => 4db
- turn to +20 degrees => 8db
- turn to +30 degrees => 16db
- turn to +40 degrees => 32db

In this example turning from 0 to +10 degrees results in a 2db increase so we would think that, in a proportional system, turning from +10 to +20 degrees would add another +2db but nope it doesn't, it adds 4db. Therefore, this system is also not linear (proportional change is always additive change, never exponential or multiple, etc.).

Now, why is all of this important? Well, because in CALCULUS (https://en.wikipedia.org/wiki/Linear_function) the two linear examples above would be considered a linear function because they are both straight lines on a graph. However, in mathematical analysis (the one we do here) a linear function is ONLY the proportional example and is actually a linear MAP (https://en.wikipedia.org/wiki/Linear_map). The latter example would be considered an affine function (https://en.wikipedia.org/wiki/Affine_transformation). The two can be distinguished easily:

f(x) = mx => linear map
f(x) = mx + q => affine function

The q is a constant and if that constant isn't 0, the function isn't proportional and thus isn't a linear map.

The reason why we need to know this is that if we're talking about linear systems IN AUDIO, we're ALWAYS talking about linear MAPS, i.e. the linear functions that, from 0 to infinity, are proportional. Additionally a linear system is NOT just a linear map either, it needs to adhere to the *Superposition principle* which states that, next to being proportional, it also needs to be ADDITIVE in order to be considered a proven linear system. Anything else is per definition a non-linear system.

Now, what does additive mean here? Well, it means that the ACTUAL response caused by two or more sources is the THEORETICAL sum of the responses that would have been caused by each source individually. This means that the ACTUAL end result of two or more sources always needs to be same to the theoretical sum of the actual combined sources no matter how the sources are reordered, recombined, etc.

One of the first images in this article shows in a very good way all the possibilities in which additive needs to hold up:
https://www.tokyodawn.net/meaning-of-system-linearity-in-audio-production/

So for example, in playback systems, if we were to play a 1k Hz and 5k Hz sine wave individually, we would hear - in a linear system - a 1k Hz and a 5k Hz individually. According to the additive property, if we then THEORETICALLY take the sum of those, that would be a signal that contains both a 1k and 5k Hz sine wave. For the additive property to be thus true, this same theoretical sum needs to also hold if we were to then ACTUALLY play these two waves together. In a linear system we don't suddenly want to see extra harmonics (which would mean intermodulation - see "Sampling" - and thus a non-linear system), nope, we still want to see the nice 1k + 5k Hz output.

Now, of course, if - in any weird universe- adding a 1k Hz sine wave to any signal always results in adding a harmonic at 3k and 4k Hz and adding a 1 khz square wave always results at adding a harmonc at 5k hz for some reason, and that doubling the frequencies of the sine and square wave would also result in the doubling of the frequencies of the added harmonics, then - even though the output is not the same as the input, this would still be considered a linear system since the superposition principle is adhered to.

Now, of course, in our actual universe, a sine wave is just a sine wave and a square wave is just a square wave and their theoretical individual outputs are also just a sine and square wave respectively. Therefore, their THEORETICAL output together should also be a signal that's simply a square plus a sine wave no matter if you add the sine or square wave first (because as we know, adding sound waves mathematically is simply an additive/linear process):

sine wave input = sine wave output
square wave input = square wave output

Which we can put in our theoretical equation:

sine wave input + square wave input = sine wave output + square wave output

The above, to the right of the equation, is the theoretical output of adding the two waves. Therefore, for a system to be additive at least, it should have that output in practice. Therefore, if adding them does result in adding extra harmonics, no matter if these added harmonics are proportional (i.e. adding a 1k Hz sine wave would always, no matter which order etc., result in adding a harmonic at 3k Hz and adding a 1k Hz square wave would always result in adding a harmonic at 5k Hz (and doubling the frequency would be propertional for the outcome as previous paragraph)), it automatically means that the playback system is not adhering to the additive property and thus NOT linear (even though the extra addition is proportional). Therefore, if stuff like intermodulation happens in a system, it is automatically considered non-linear no matter if the added harmonics would be proportional.

In an FX chain the additive property is also important for the FX chain to be considered linear. For example saturation is a non-linear system/source because combined with other plugins the final sum of the plugins depends on the order of the plugins. For example, consider the following fx chain order:

1. Saturation
2. High-Pass filter

Or like this:

1. High-Pass Filter
2. Saturation

Even though the same plugins are used, the sum of the two sources won't actually be the same in both examples since in the latter case, after the high pass filter, saturation will add harmonics again beyond the high pass filter, while if you do saturation first and THEN high-pass, there won't be harmonics beyond the bandlimit of the filter. Therefore this system is non-linear. This is important to be aware of when chaining fx that if you're using non-linear plugins such as saturation, that you should be careful with its order since the order will shape the end result. Of course, there is no right or wrong and it depends a bit on what end result you want, where you want to put your non-linear plugins. Also, if your FX chain has only linear plugins then you don't need to give a crap about the order of the plugins since reordering them won't change the end result (look up what are linear plugins, I guess reverb?, and what are non-linear plugins, saturation compressor??):

https://www.reddit.com/r/edmproduction/comments/afttw6/effects_before_or_after_reverb_pros_cons/
https://iconcollective.edu/mixing-effects-chain-order/

Even crazier, if you had two saturators in your FX chain and each of them were applied with a 50% wet level, so only half power, you would think that that would be the same as one saturator in your FX chain at 100% power. But nothing is less true, these also give different end results (I guess because second saturator ADDS harmonics based on the harmonics the first one created, while the latter with 100% wet only adds one round of saturation but louder????? Also, is this why people change OTTs sometimes but at lower depth levels since it might make stuff even fatter due to harmonics on harmonics or what? Of course don't have to think about it so much, just experiment and see what sounds good, but also look up if true).

Lastly, if you applied a saturator on one sine wave track and then applied another saturator (equal saturator settings of course like the other examples) to another sine wave track and then played them back, you would actually also get a different result then if you were to playback both sine waves but with a single saturator on the master (I mean different because non-linear, but different how and why? I guess again because harmonics created BASED on two individual waves and then played back vs. harmonics created based on two waves and then played back. How does a saturator create harmonics?).

Now, one last thing, a non-linear system may also seem linear sometimes. This is because in some cases non-linear systems might behave like a linear system for a lot of inputs (due to luck) so we might never even notice that the system is non-linear. Therefore, systems that we do consider linear can never actually be said to be actually linear with a 100% certainty.

## Unprocessed notes

talk about voltaire and the non linear equation functions why we come to more than one linear output see the wikipedia for non-linear system

look at non linear and look at equations how it can cause shit


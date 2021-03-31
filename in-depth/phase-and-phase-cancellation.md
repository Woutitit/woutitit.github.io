# Phase And Phase Cancelation
## Table of contents
1. Introduction
2. Phase and phase shifting
3. What phase cancellation is
4. Quick reminder: Adding waveforms
5. How Phase Cancellation Sounds Like In Sine Waves
6. How Phase Cancellation Sounds Like In Complex Waves
7. How Phase Cancelletion Cancels Frequencies: Comb filtering
8. When is Comb filtering an issue (make better)
9. Conclusion and key takeaways

## Introduction
The phase of a periodic waveform is a certain position on said waveform relative to its period since the beginning of a new cyclus. In other words, if we were to choose any point on a periodic waveform such as a sine wave, we could calculate the angle - a.k.a. phase - of that point relative to the starting point of said wave. This angle is visually easy to see with an animation:

https://jackschaedler.github.io/circles-sines-signals/sincos.html

The middle of a circle is the starting point of your wave and the amplitude of the wave is how big the circle is. You can then see that if you always go round and round a circle with constant speed (with each full going round being a cycle) you get certain angles w.r.t to the starting point of the circle. For example, half way round is 180 degress and thus halfway of your sine wav has a phase angle of 180 degrees. Full way around is 360 degrees. Therefore a sine wave can have phase of minimum 0 and maximum 360 degrees. 

**INTERMEZZO: It's really interesting how a sine, cosine and a circle relate and it's also interesting why we ever heard a pure tone and then mapped it to a sine wave representing that tone. See "Sound basics" if you want to learn more.**

## Phase & Phase Shifting
Now practically, the reason we want to know the phase is because in the case where we're dealing with two identical waves where one of them is so called "phase shifted" we need to know if that is a problem. Now, first of all, what is a phase shift, though? Well, a phase shift is simply the angle (or phase) shift between two (identical?) waves. It happens when two waveforms play together but where one is slightly delayed resulting in the waveforms not lining up. A phase shift is basically the same as a phase with the only difference that here we're talking about the angle of the start of the origin of one particular waveform relative to the origin of another (identical) waveform instead of itself.

Now, how is phase and phase shift important to us, music producers? Well with phase shifting comes a (usually) undesirable phenomenon called "phase cancellation". And as we'll see in a second this IS a nasty little beast that we do need to be aware of when mixing and recording music.

## What Phase Cancellation is
Phase cancellation is the phenomenon that happens when a particular sound wave (not necessarily identical) interferes with another wave. If you know something about waves and interference, you know that there can be constructive and destructive (and comb filtering) interference between waves. Basically every wave that interacts with one another will have both constructive and destructive interference going on to form a resulting waveform. We can add up certain waveforms in such a way that the constructive and destructive interference that add up to a result waveform don't sound good to our ear. One such example is when we'd play a "chord" that consists of C, C# and D, the resulting sound/waveform does not sound very good. Oppositely, we can also add up a set of waveforms that do sound good. One such example is a Cmaj chord where the interferences (both constructive/destructive interference) add up to a waveform we like (= like because everything is subjective in the end).

Now, phase cancellation is the destructive interference part. Anytime destructive interference happens, we're talking about phase cancellation. And while phase cancellation is not "sound ruining" bad between waveforms of DIFFERENT wavelengths (as we've seen, the worst it can do is result in a dissonant chord), it does get bad when we're looking at phase cancellation between two (almost) identical waves. Because, instead of simply having a dissonant sound (badly affecting the fundamental tones/sound), phase cancellation in this case manifests itself on a much more fundamental level (badly affecting harmonics/timbre/amplitude). In fact, when talking about phase cancellation we only really use it as a term in the latter case, so keep that in mind for the whole article.

(Also, constructive interference is not fully in the clear here but as we'll see in a minute, it's less bad than destructive interference.)

## Quick reminder: Adding waveforms
Now, before we move on to how phase cancellation looks and sounds and why it (usually) sounds bad/undesired, let us remind ourselves again very quickly how a final waveform from multiple sound sources is created (as it will come in handy). As you might already know, it's really not voodoo magic. It's simple addition and subtraction. For example, let's say that we have two random sound waves playing together. We notice that there is a peak of the first wave at a timepoint of 2 seconds. That peak is at a value of perhaps 1 in amplitude. Now, let's check out for that same timepoint where our second wave is at. Perhaps there we see that our second wave is not peaking but instead only at an amplitude value of 0.8. Now, what's going to be the final result then for the combined waveform at that point? Well, simply:

1 + 0.8 = 1.8 Amplitude

If we do this same process for every point on the first waveform (or the waveform that ends last to get the full resulting waveform) we can easily calculate and draw out the resulting waveform that we get of the combination of the two waves by adding the amplitudes of all the points. This can be extrapolated towards more complex waveforms and more than two sine waveforms of course.

## How Phase Cancellation Sounds Like In Sine Waves
So now let's check out some phase cancellation examples. Let's see what happens when we would add two sine waveforms that are exactly the same AND are exactly in phase with eachother. What we will notice is that we get a resulting waveform that is still a sine but double as loud (amplitude doubled?). This happens because the waves are FULLY IN PHASE, i.e. at every point, the amplitude values of both waves are equal so it's basically a matter of 1 + 1 = 2 (=> doubling) for every point that they overlap. Differently said, for a full cycle, there is ONLY constructive interference going on which means in this case there would be 0 destructive interference and thus 0 phase cancellation.

However, what if we did the opposite? What if we add the two exact same waveforms together but they are 180 degrees out of phase (so totally out of phase)? Well, something else funny happens. Instead of a 1 + 1 = 2 situation we get a 1 + (-1) = 0 situation for every timepoint they play together. And since the amplitudes will always be the opposite of eachother now, we get a full cycle of total destructive interference, a full cycle of total phase cancellation which results in a full cycle of utter silence. Neat isn't it? 

Also, as an extra, notice what happens when we'd gradually pull the second sine wave back in phase. The result gets louder and louder again until we fully resolved the phase issues and are back to our doubling in amplitude. All this is an example of phase cancellation. Not very nice sounding, isn't it?

## How Phase Cancellation Sounds Like In Complex Waves
Now, let's check out phase cancellation in more complex waveforms because all the above resulting waveforms is what phase cancellation sounds/looks like...between sine waves . However, real life sounds and music are not just simple pure tones interacting with eachother.

So, first thing to note is that in real life, phase issues between *exact* waveforms usually don't manifest itself as being exactly 180 degrees out of phase (as that would be a big coincidence) so only rarely will you hear full silence when phase cancellation is happening. 

A second point is that phase issues - in 99% of the cases - don't simply sound like the result is just quieter as in our sine wave example. Reason being that only a sine wave has unique properties that make it so simple and symmetric that in any way you add a copy of a sine to a sine - whether it's phase shifted by 10 or 180 degrees - the result is always actually going to be a sine wave (but with a varying amplitude). Therefore, the resulting waveform of two sines can never result in "interesting" phase cancellation.

That being said, we CAN very much extrapolate the sine wave example to a complex waveform example because - as Fourier once proved - EVERY complex wave can be broken down into sine waves (or sinusodial(spelling?) components) (there exists tools to do a so called Fourier transform if you don't believe me). And that makes very much sense since a sine wave can kind of be seen as a single harmonic or overtone in a certain complex waveform since it's a single frequency just like a single harmonic is a single frequency. So when we'd play a note on a piano - which has a certain timbre - we would basically hear the fundamental sine wave with then all its sinusodial components (harmonics) ringing too. Similarly, if we'd play a chord (or instruments play together), we'd hear multiple fundamental sine waves and their respective sinusoidal components together.

(Note: A sinusoidal component is not exactly the same as a sine wave, usually it's quieter in amplitude just like a harmonic is, but it's a sine nonetheless)

Now, why is this important to understand? Because, while it would be a big coincidence that a complex waveform is FULLY out of phase with a delayed/phase shifted copy of itself, it's very much possible that some of the sinusoidal components of the two phase shifted waveforms are FULLY out of phase (or fully in phase). This can happen because no matter the delay, and regardless of the waveform there are ALWAYS theoretical sinusoidal waves that can possibly be totally IN phase or totally OUT of phase with one another. 

To give an example, let's say we delay a copy of a complex waveform with 1ms relative to its original self. This would mean that the sinusoidal component/harmonic in both waveforms travelling at 1ms will be fully in phase. Why? Because from the moment the second waveform starts playing, the 1ms sine wave (= harmonic at 1000Hz) in the first waveform would have done exactly 1 full cycle, so they'd start at the same phase again for the 1st sine wave's 2nd cycle and 1st cycle for the second waveform 1ms sine. Similarly, sine wave components travelling at 0.5ms, 0.25ms, 0.125ms, etc. would also be totally IN phase since they all have done exactly n full cycles (an integer) after 1ms of time. Oppositely, a sine wave component that travels at 2ms would be totally out of phase, since at 1ms, the sine wave component of the first waveform is only but exactly in half, while the other one already starts. And just like the in phase example, there is also a whole pattern of other sine waves that get fully cancelled too.

Also, the pattern of sine waves that get cancelled depend on the delay because with different delays come different cancelled sine waves (sounds obvious but try it if in doubt, you will see). However, you can take ANY delay and ALWAYS be able to calculate the sine waves that would in theory cancel eachother out or boost themselves, it's just a matter of whether the two complex waveforms have these sinusoidal components, and how much of them/how prominent they are. Because, if the harmonics that in theory cancel out/boost didn't exist in the waveforms anyway, there of course wouldn't be a difference in sound, so no actual phase cancellation is happening.

So if sine waves/sinusoidal components can very much completely cancel out in complex waveforms too, then why don't we hear that (only) as a loss in amplitude or silence but rather as a nasaly, phasy sound? Well, because a complex waveform is not just a sine wave. Therefore, if one or more sinusoidal components (= harmonics) totally cancel out, we basically hear it as a loss in harmonics rather than a loss in the full sound. In other words, rather than (only) a change in amplitude we'll hear it as a change in timbre. And of course, if we want our piano to sound like an actual, real and full piano we would not want that at all. Additionally, because sinusoidal waves get fully cancelled while others get boosted, our sound becomes less rich in certain areas and more harsh in others making for a usually unpleasant sound.

To really hear yourself how a resulting waveform of 2 identical complex waveforms (with one slightly phase shifted) drop in a vocal in a DAW and put a very small (like 1ms) delay on it. You'll notice that when you phase shift two complex waveforms, like a vocal, the result will sound...phasy. It kind of sounds weak and nasaly which is undesired in most cases. I mean, would you want your MAIN vocal to suddenly sound like phased-out crap? I don't think so, you want it to sound like you originall recorded it. Also another thing, if you slightly change the phase shift you'll notice a change in sound and timbre. Effectively, this happens because now phase cancellation is working on cancelling different sinusoidal components of the wave and thus different frequencies will be cancelled out/boosted resulting in a change in timbre (remember, timbre = frequency/harmonic content).

## How Phase Cancelletion Cancels Frequencies: Comb filtering
So, anyway. We've seen now that with phase cancellation, sinusoidal components of two complex waves can fully be in or out of phase and can therefore be fully boosted/fully cancelled. We've also seen that there even is a certain pattern to that boosting/cancelling. What you don't know, however, is that that exact pattern even has a name, it's called comb filtering.

What comb filtering is, is that it's basically the effect that happens when adding two identical waveforms, one of which is slightly delayed. If you then would playback the resulting waveform and spectate the result in a frequency analyzer (linear scale for a more obvious result) you would see that the resulting waveform gets cancelled in specific frequencies, kind of resembling a comb.

Now, as we've discussed, how much it's going to look like a comb depends on the harmonic content of the waveform because if not a lot of prominent sinusoidal components align with a lot of theoretically fully cancelled/boosted harmonics, not THAT much will happen and seeable. In other words, whether a comb filter is problematic depends entirely on whether it cancels out important frequencies and how much it cancels out. If it's only the highs/very highs, it might not necessarily be an issue as rather than audible cancellation, you'll get your same sound but only phasier - which maybe you want (like, in synths or whatever). However, if it's the lows - as we'll see - we will have a bigger issue.

Anyway, we've already kind of looked at an example of comb filtering but let's see a bit of a more expanded example of why phase cancellation between two (identical) waves results in a comb on a frequency analyzer.

Let's say again that in a certain situation a waveform's exact copy plays at a 1ms delay. What this means is that the harmonic in both waveforms that travels at 1ms speed will be COMPLETELY in phase (with the only difference that the harmonic of the first waveform has already done one cycle). In this case, that harmonic is at 1000Hz (1000Hz = 1ms) and so this harmonic will be boosted/doubled in amplitude which shows as a peak on an analyzer.

However, what this 1ms delay also means is that any harmonic travelling at 2ms in both waveforms is COMPLETELY out of phase. This is because now, the 2ms harmonic of waveform A is only half way when the 2ms harmonic of waveform B starts, meaning they are 180 degrees out of phase. Therefore on an analyzer this will be shown as a very deep through at the 500Hz (2ms) range.

(1: Note that all frequencies in between throughs and valleys are only partially phase cancelled based on the waveforms in question of course.)
(2: Note that the phenomonenon above can ONLY happen when the waveforms are identical because even if they are the slightest different, phase cancellation will still happen but exact out of phase/in phase of frequencies that drastrically boost/cancel is impossible and the throughs and peaks will be already way less.)

Now, these are only 1 peak and 1 through respectively, how does the comb happen then? Well, clever readers have already deducted that this pattern will repeat itself going up the frequency range. For example, a harmonic in waveform A travelling at 0.5ms, 2000Hz, will also be totally in phase with a harmonic travelling at 0.5ms in waveform B (only difference that the harmonic in waveform A has now travelled two full exact cycles before waveform B starts). Similarly, because 1000Hz was in phase and 2000Hz is the next totally in phase harmonic that means that the harmonic of waveform A and B right in between, at 1500Hz = 0.66ms, will be totally out of phase again.

(Note: Any speed you can't add to 1 by multiplying with an integer (= indication of # full cycles) in this case is out of phase. How much out of phase depends. However, any harmonic that lies exactly in between two TOTAL IN PHASE harmonics is totally out of phase).

And you can do this on and on and on up the frequency spectrum until you have the infamous comb.

## When is Comb filtering an issue (make better)
Well, basically anytime you don't want that nasally, metallic sound that a comb filter gives. However, it's a problem more often in certain cases then others. 

One very obvious case is when the comb filtering already starts to happen from very low frequencies. This happens when the delay between the two waveforms is in such a way that a very low harmonic is already FULLY phase cancelled instead of only partially. Because in that case, the low will be cut out, the other lows, mids, highs, very highs etc and the comb happens accross the whole spectrum. More specifically, **the bigger the delay, the more comb accross the whole spectrum there will be**. (Because a 2ms delay will "only" start FULLY cancelling a 4ms harmonic = 250Hz going up the frequency spectrum while a 4ms delay will fully cancel an 8ms = 125Hz harmonic going up the frequency spectrum)

(see: https://books.google.be/books?id=5qzJ5kPAbGsC&pg=PA13&lpg=PA13&dq=partial+phase+cancellation&source=bl&ots=VUwKgevVgI&sig=ACfU3U3s7Jwh3FJoDCJPGxmDz6U5eJq2Rw&hl=nl&sa=X&ved=2ahUKEwjpiP6X2-HoAhXEKewKHcDuCgQ4ChDoATADegQICxA2#v=onepage&q=partial%20phase%20cancellation&f=false)

However, do note that once the delay is around 25ms, rather than hearing cancellation in one sound, we hear 2 distinct echoes. So even if cancellation does happen, we hear it as echoes as we can distinct the two notes and the resulting sound will sound less problematic as it's not trying to be one sound but rather a sound and a proper delay.

Similarly, when the delay is very small, the comb will happen more up into the frequency spectrum only and depending on how small the delay is, it's not going to affect the whole spectrum and therefore is "less of an issue". Of course, if the delay is not small enough (like 0.000025s) your sound will still sound weird, and even at a very small delay there is always partial phase cancellation going on which might or might not be a problem.

Now, one thing to note with the above statements too is that now it might seem that having the comb accross the while spectrum is problematic but rather it's actually really the lows and the mids that we care about, especially when we kind of want that phasy sound to have in our sound. This is because lower frequencies travel slower than faster ones. Therefore, totally in and totally out of phase follow eachother less quickly for lower harmonics. Result is NOTICEABLE cancellation/loss in frequency. Also, notice how comb also doesn't restore after a through. Nope, it travels all the way up in a parabola-like manner until it reaches the peak. So not only is there a loss at the fully cancelled frequency but also at a lot of frequencies before and after that one that get lost. And since each and every frequency count way more in the lows than highs, compared to higher frequencies, we'll thus have "much bigger" loss in overall sound in the lows with a comb than in the highs since in the highs the combs follow eachother so fast and the throughs and peaks are also only a very small portion of the sound. So, that's why phase cancelled kicks there body would dissapear since those are usually in the lower ranges.

But anyway, if that's confusing, it's the same as why a chord in the lows is more muddy than that same chord in the highs, the frequencies of the notes are simply way closer together and thus more audible beating occurs (since the waveforms of overtones line up only in a slow way) and we - for some reason - also don't like that (which is why we voice a chord in the bottom more resononant notes, or only the fifth and stuff)

But yeah. In other words, in a real life situation, usually when you hear phase issues and you need to fix them is when the phase cancellation is happening in the lower frequencies since there it's so blatant that sound and frequencies are missing (since each frequency counts in the lows so to speak) when phase cancellation is happening.

## Conclusion and key takeaways
https://old.reddit.com/r/audioengineering/comments/gnxq67/how_to_identify_phasing_and_fix_it/

So, in practice, phase and phase cancellation are important to understand. Now, it's practically only relevant between equal sound waves emitted from equal instruments at almost equal time. A few exceptions might sometimes exist, mainly when you're layering kicks since a lot of kicks and snares might be really close to eachother in waveform. If you hear phase issues, or you aren't sure, you can always try to reverse polarity of one of the waves to see if they interfere less that way. Or you'll want to low pass your low kick and high pass your top kicks so they don't interfere or you might just choose another sample (or all these techniques combined).

That said, phase issues practically always and only occur in the common case I described first and that's important to realize and be aware of it. In that case, you simply need to be
to be able to hear it and kind of identify it as a weak, metallic (and sometimes almost gone) sound and know that that are phase issues. Now, know that phase issues most often occur in two cases: stereo (delay) and misaligned microphones and thus you should know what to do to fix phase issues in these cases (correctly aligning the microphones and stuff). Also, when you have some stereo going on in your mix, which is good of course, always check via ozone your stereo image (or what it is called) and see how much phase/phase cancellation there would be if you summed to mono and if it is too much and you can also clearly hear it when you sum to mono (= click that button at your master that makes everything sound mono). In that case, you need to fix it too. Now, usually here the culprit is the use of stereo image tools which one says to be avoided as they often are more prone to phase cancellation (why? due to their delays?) and thus create a more natural stereo field/big sound with other tools (like most professional artists do).

So yeah, stereo, multi-mic recording (and sometimes layering) can all have phase issues. Know how to hear it, know how to see it on their frequency spectrum (slight comb) and know how to see it on a correlation meter (like 1 is bad I thought or whateer) (like ozone has, see izotope youtube channel?) and know how to fix it in all these cases. There might be a 5-10% of other cases but they are very rare and if you don't hear them anyway, it might not even be that bad.

## FAQ
### Why Is Phase Cancellation Not An Issue With Frequency Shift
Now, a few things to note before I go, though. Because, throughout this article you might have wondered why we're only talking about identical waves that are phase shifted. Why aren't we talking about two originally identical waves where one is phase shifted AND frequency shifted and the other stays the same. Why isn't the constructive and destructive interference going on between those two waves bad?

The short answer is because they are different waves. If we were to take 2 sine waves, one of which is higher in frequency, and try to phase shift them in any imaginable way possible, we'll will notice that we'll never be able to phase shift the waves so that they are fully in phase or fully out of phase for a full cycle. This means, in other words, that total phase cancellation, no matter how small the frequency difference, can't happen between two sine waves of different frequencies. 

Instead, what happens is something called "beating" (or rhythmic phase cancellation). For example, if you take two sine waves in the lower frequencies that are a semitone apart and play them together, you'll notice a wobble kind of sound. This wobble sound comes from audible and rhytmic changes in amplitude when these two waves are interfering. The reason that happens is because two sine waves of different frequencies played at the same time will - instead of being always the same amount in/out of phase - always slightly diverge more and more either out of phase or in phase relative to eachother due to their different vibration speeds/wavelengths. 

```
SIDENOTE
If you'd like to know. The wobble effect is caused by the fact that sine waves always go more and more out of phase up until the point they are fully out of phase from which point they become more and more in phase again until they reached fully in phase and the cycle continues. The reason this happens is because of a few things:
- They are sine waves, therefore ANY point in and out of phase will only sound like either more or less volume
- Sine waves are predictable, symmetric waves. Therefore there is a regularity in the pattern going in and out of phase accross the whole period they are playing.
- Because, again sine waves. Imagine two waveforms of the exact same type of waveform but one is slightly slower. The faster one is slowly but surely going more and more out of phase with the slower one. However, since they are both sines it's going to be smooth since the wave of a sine is smooth too and they are both sines. If they were complex waves
- 
even fast still beat cuz there is always a point that meets valley and peak that meet.
imagine first a wave full inphase and then imagine one that is tiny bit slower, the slopes are a bit less steap and the ducks too so slowly more out of phase and it's more and more since they are the same wave.
```

And because of this reason, we can never have a full cancellation between sine waves of different frequencies. On top of that, if you listen closely to our sine waves, the wobble effect is only even slow enough to hear between frequencies that are close enough in absolute Hertz (look up how close kind of) which thus means that only in the (very) low frequencies AND with small intervals such as a 2nd minor, you will really hear an audible rise and fall in amplitude. Therefore, even if the wobble is undesired, most of the time we play chords higher up the frequency range. Plus, chords most of the time have big intervals between the notes too (and if they don't we usually tend to stack them higher up in the spectrum anyway). Plus, most instruments are complex waveforms which makes the wobbe less audible too (as we'll see).

The only time where this wobble could be an issue is when you're dealing with two sine waves in the VERY, BARELY AUDIBLE low frequency range that have a difference of only a few cents. Because here, the wobble might be so slow that if these two waves were phase shifted in such a way that they'd at the start briefly cancel eachother out when playing, it might take a while to get an audible amplitude. Also, it's going to stay kind of very loud quite some time before it slowly drops down to more quiet. But even in this EXCEPTIONAL case - that we don't do in music anyway - there is still going to not be that much milliseconds where there is too much cancelled sound.

To make this case even more clear. In complex waveforms, there is even less of an issue because there the wobble is even less heard. So why is that? Well, as we've also already seen, a complex waveform is made up of a lot of sinusoidal components. And thus, even if one sinusoidal component would cancel out a brief moment, then the the other sinusoidal components are still there that are most likely not cancelled out (or at least far from all of them) so there is still a lot of sound going on. You can still kind of hear wobbling and beating of course, but this is yet again only audible in the lower frequencies and with small intervals. And this is the reason why this won't sound phasy is because the harmonics will be audible at some point, and most of the hamonics that would be cut by a comb filter that now simply go in and out of phase are high enough in frequency spectrum (since it doesnt take very high to not be audible) that the time between max and min amplitude is so little it's barely hearable that that harmonic was even cancelled out in the first. So instead of a phasy sound, it's what makes it the sound of a chord (or interval or whatever)

### Why is phase cancellation not an issue with same freq notes but different timbre
Okay, well, if frequencies aren't an issue, then what about phase cancellation between two compplex waveforms both with their fundamental at the same frequency but one of the slightly phase shifted. Surely, they must share harmonic content?

Yes, and they do probably share harmonic content but the reason that even there it is not a problem is because the timbre is different. The harmonics these two instruments have at that frequency will overlap but the amount won't. And also - very important - the amplitudes of the harmonics they have will not overlap. And because the amplitudes for most harmonics they have aren't the same, there can't be full phase cancellation for those harmonics (since 1A + (0.5A) =/ 0). So what you might end up hearing is more of one instrument than the other because maybe he has louder harmonics (and a stronger fundamental) but you won't hear phase cancellation. Also, as I've said many times now, this is for low frequencies too. At higher frequencies you get the same and even for more little parts of the sound so it's going to be an effect even less. Therefore, you very much do hear distinct instruments and depending on who's the strongest you might hear one more than the other even if they are the same volume. But that's nowhere near hearing them as phasy.

The only way this could be a problem is if the complex waveforms are similar in timbre. That is, they have the same harmonics AND most of the harmonics have the exact same amplitude. This is very rare - near impossible - with different irl instruments (unless you're playing the same guitar but even then amplitude by strumming may vary too) but this can happen very rarely happen with made up synths. One example is saw/square. They will create phase issues between eachother if same pitch because they share a lot of the same harmonics and same amplitude of those harmonics. However, we're speaking yet again about the lower ranges here because the further up we go, basically in the ranges where we will usually play these frequencies, even if out of phase, they won't sound phasy cuz it's only the upper ranges that get affected, and even if we hear it a bit maybe we like to have it (look at seamlessr video to see why it could be interesting auto modulation, somewhere at the end of his video it was).

so in dubstep a lot of basess and wub wub basses mainly reese do phase cancellation but also in lower areas because...Well they are basses and phase cancellation is interesting motion but since that also makes the low end unstable since sometimes the sub is is less strong than other times, and thus kinda the fundamental ofur song kinda fades and it doesn't sound very fat you'll want to simply layer that bass with a stable sub that has always the same amplitude (also filter out unstable sub from ur bass). a lot of times they advice to thus have a seperate

at which point delay small enough to not be heard and which point big enough (i guess 25 mx mixing google) to be heard as echo and why not cancelling, i mean its cancelling but because echo it sounds as ehco rather than canelling, second voice cancel first but sound lik echo?

Which is why you avoid, layering basses and again only for lower frequencies it's like talking over eachother
well cuz diff harmonic content and diff amplitudes even iof harmonics overlap but maybe can be issue with very similar, but it already has to be very similar which irl happens only with actually same sound source or i guess maybe square and saw have lots of same harmonics? Look it up!


## Unprocessed Notes
what about octaves then? not issue, cuz again different waveforms

Combine all the above reasons and there you have the answer to why



Also, this wobble effect is only even audible frequencies AND between frequencies that are close enough so that the wobbles aren't too fast.
Because they are sines and because they are identical waves.

This gives it that wobbly effect.

And because of that

And as we've seen with sine waves, this results in more and more silence. In fact, at one particular point they'll be so much out of phase that there is complete silence. We call that a **beat (frequency)**. From that point, the quicker waveform has basically half a cycle of a lead and will now get more and more into phase again, completely lapping the slower waveform and completing the wobble we hear.

You can do this exact same experiment in the higher frequencies too. You'll still notice the wobble but quicker. Why is that? Well, because a minor 2nd interval in the lower frequencies and higher frequencies don't have the same difference in frequency. In equal temperament, a G2 to G#2 110.00 - 103.83 = 6,17Hz difference.  However, a G4 to a G#4 is a difference of 415.30 - 392.00 = 23,30Hz. In other words, in the higher registers, the semitone up a note goes way faster relative than a semitone up in the lower registers. In fact, the higher you go up, the higher this relative difference between two (semi)tones climbs (I think it climbs up logarhytmically or exponentially). Therefore, since the second wave is going faster it's going to be quicker in and out of phase with the first wave, therefore when a beat happens, it very quickly goes back to full amplitude (and back down etc.). In fact, one wave can be so fast in and out of phase with another wave that we don't even hear a wobble going on anymore even though it's still there.

To go a step further, you can even try this with two frequencies that not even have a semiton difference, but only one cent difference.

Also, it should be noted that sine waves of different frequencies will always diverge more and more out of phase. It's never, a little bit out of phase and then suddenly in phase, and then maybe fully out of phase, why is that? Or is that the case though with less imilar waves so waves with more frequnecies apart? Always peak that lines up with a valley at one single point - due to their unique properties -. And so we can so kind of sinusoidal components.

different prominent harmonics or the harmonic content components is not same amplitude therefore not full cancellation/boosting so only little more issue, also it only happens in lower egisters, since for example an octave, loads of harmonics in common but only cancelling out from start, could we cancel out fundamental of the higher pitch with a delay that makes
the fundamental pitch out of phase with sinusoid components, but then again not sample amplitude, cuz fundamental pitch is more volume, however, might be less volume but then that's what we hear as a chord i guess, cuz we both hear low and high. why cant hear wobble (as good betwene piano, cuz its on a sine wave level id suppose??? and more complex waves become a much more complex wave with distr and constr but on subconscious lvl we still hear the sines wobble so dissonance)
also calculate beat frequencies how? 


## Why Phase cancellation isnt an issue with same freq notes but different timbre
well cuz diff harmonic content and diff amplitudes even iof harmonics overlap but maybe can be issue with very similar, but it already has to be very similar which irl happens only with actually same sound source or i guess maybe square and saw have lots of same harmonics?, look it up

waves lining up is just stuff we like to hear, doesn't have necessarily to do with wobbles since wobbles happen faster and faster linearly with 1 semitone slow => 1 semitone above faster => 1 semitone upper faster and faster since differnce in HZ becomes bigger.
not only cuz difference bigger but also cuz original wave travels faster? nah not, this, it's jsut more white cuz waves more and more where both 0 amplitude not out of phase but in pahse since its meant to be 0 so no destructive or full cancellation



Now, unlike phase shift, there is also something called frequency shift, i.e. we copy a waveform and we alter its frequency. When played together, constructive and destructive interference will do it's job and depending on the frequency shift (= interval in this case), it's going to sound nice (a perfect fifth) or bad (a minor 2nd).

Now, one can ask. Why does the destructive interference in these cases don't cause problems? Surely, two complex waveforms, no matter if they are the same or not should have some sinusoidal components that are the same, right?

And that is very much true so let's go through some experiments again to see why here there is no/less of a problem.

Let's start at the beginning. Previously we added 2 sine waves together that were identical with the result being still a sine wave but double as loud. Let's now add two sine waves again that play at the EXACT same time BUT let's now frequency shift one with 1 cent so they are slightly different pitches. 

So. Do we still get a doubling in loudness? Nope. Instead what we get is sort of a very slow "rhytmic phase cancellation". More specifically, since the 2 waves are almost identical AND since they are perfectly lined up, the 2 waves will actually be quiet good in sync for some time. In fact, at the t = 0, they will for a VERY brief - one point - moment be completely in phase. However, the longer time goes on the two almost identical waves diverge more and more out of phase. And in sine waves we already know that this manifest itselfs as getting quieter. In fact, after some time, the two waves are so much "out of sync" with eachother that there comes a VERY BRIEF - one point - where both waves cancel eachother out. And, since the waves are still different, after this full cancellation the second wave will go beyond that point and actually slowly but surely get more and more into phase again until the point where "full amplitude" is yet again reached, basically the start and basically the point where the two waves beginnings come together (since the waves started at that amplitude) and voila, they are ready for the next round where the second wave's gonna diverge yet again.

Now try this same thing but instead, detune the other sine wave with 100 cents (= a semitone). In this case, you'll notice the same thing happening, just much faster. Also, you'll actually notice a sort of wobble sound. That was also there in our previous example, but just very slow. It happens, exactly because of this endless ccyle of fully into phase moments to fully out of phase moments between the two waveforms.

The parts where there is no sound have a name, they're called beats. The more beats per second, the faster the wobbly sound is. The less beats per second, the slower the wobble goes. So, the question now is, do beats happen between any two sine waves that are added together? And the answer is yes,

for the first point "in phase". 




And that's seeable on the waveform as there we have the most amplitude. However, slowly but surely the second goes more and more out of phase. And we know what happens then, yup, the amplitude gets quieter and quieter since we're talking about sine waves here. It keeps getting quieter until at a certain point it's so much out of phase that there is a very slight moment that they both cancel eachother out completely.

If you let them play together for long enough (especially if you have them in the lower frequencies) you'll notice something interesting in the shape of the resulting waveform in both cases. That is, that when, in the first case where the waveforms were playing "in phase", the amplitude was doubled for a very short time, but then gradually became less and less to have a very short silence (= out of phase- to where it was going up to a peak yet again and on and on. Same, with the out of phase one, but here the resulting wave started in silence and got an increase in amplitude up until a very short point where they actually were "in phase" to then go down again and on and it goes.

This is what we call a "beating", and audible kind of wub wub sound if you will. This wub wub sound occurs when 2 sine waves of different frequencies add together.

also amplitude matters of the harmonics since only exact amplitude will do a full cancel as we've see when adding one louder sine with a out of phase quieter sine, you still hear a sine
instead of silence.
so what if phase shift one of the frequency shifted once.


it might sound obvious that two sine waves (or sinusoidal components) with different pitches played together will not result in phase cancellation (as in the dramatic meaning we discussed). Because, obviously we can't talk about phase between two waves that aren't identical as a phase shift of one of them can never result in them either being totally in phase or out of phase. However, there still is phase cancellation - now in the less dramatic meaning - happening of course. Like, the partial cancellations and additions that happen between waveforms to make a waveform that sounds like a nice chord, or even a song. Also, next to those partial cancellations, surely there are some complex waves that aren't the same but will still have some sinusoidal components that they share and thus might totally cancel out when phase shifted, right? Why doesn't our resulting waveform sound phasy in these cases?


Well 2 sines that are frequnecy can never be in phase or out of phase since there is no phase to compare. However, surely complex difrrently fundamnetal tone/timbre waves do have sines harmonics that overlap
Now, before we look at some real life examples of when phase cancelling occurs let's kind of wrap up the whole definition section by answering the question why a frequency shift, rather than a phase shift does not result in phase cancellation.

So, first of all, the fact that two waveforms at different frequencies don't partially cancel eachother out is false. AS we've seen in the beginning, this how the waveform of a bad or nice sounding chord is formed. However, why doesn't it result in that distinct phasy, nasaly sound. Surely two of the same complex waveforms (where one is an octave higher than the other, but NOT phase shifted) has a lot of sinusoidal components in common with eachother. Why wouldn't they cancel if out of phase?
Well, if one waveform would be frequency shifted and we'd play the two waveforms together we'd have something called music. For example, shift one note 1200 cents up and we have an octave interval. In a sense, this is also a change in timbre, however rather than harmonics thats change we add actual fundamental tones, so rather than a timbre change we hear it as an actual chord/sound change since fundamentals way louder/prominent than harmonics.

The reason a frequency shift is okay - even when phase shifted - is because two waveforms with different frequencies can never be totally in phase or out of phase with eachother (or at least not the fundamental tone which is the most important) so phase cancellation is less of a problem here. Of course, phase cancellation still happens but since the waves are different, rather than sounding hollow (because frequencies are cut) it sounds like...a chord yup because now kind of accross the whole spectrum there is kind of happening partial cancellation/boosting but never full cancellation so you won't see throughs and peaks as much but rather a waveform that sounds like a full chord.

Now, of course, the more and more the frequency becomes the same (so again, especially in chords in the lower frequencies) the more and more the waveform becomes the same and the more and more risk for phase issues. For example, take a square wave in the C1 range and make a minor chord. You will HEAR the beating which is basically all the waveforms travelling but since it takes sooo long to line up you kind of physically hear the amplitude diminishing and getting greater again. This is also phase cancellation, but rather rythmic phase cancellation since in this case, rather than cancelling out frequencies and cancelling along the whole way, it cancels in periods and also not certain frequencies since far from the same wave. This is basically how FM synthesis and reese basses and detune work. Like, detune, not only can be used for widening but can thus also be used for getting that interesting "motion" effect that we like in a lot of our synths (without even having to automate or modulate). But the more and more the waveforms go together, the slower and slower the rhythm becomes and when we're aproaching 1 cent and lower, the waveforms kind of start to look like eachother and thus, if these would be phase shifted you would get the problematic phase cancelation more and more again.

#### When to look for phase cancellation in producing
Recording multimike
Having stereo synth and not properly delaying them so that when you sum them to mono they kind of phase/dissapear
#### Notes (TODO)
why above 25ms echo and no cancellaion surely still cancel, is the samme armgument as freq shift, too far apart, too different?
diff freq can also very much have some overlap in sin components so could be cancellation but why less harsh?
at which delay the fundamnetal cancel out? Or impssoible unles full canellation in which case evrything cancels out anyway?
why not cancel out with diff frequency sine waves? cuz don't they contain similar harmonics too cancl out? but ig uess not fundamental tone so less issue ad instead cancellation is more for the tone since in this case you'll hear chord and cancellation shapes hat sound
octave phase shift still comb in harmonics and also comb much more than through, also going down down down up up up slowly instead of small peak and through, i guess not really boost but maybe ye in comparison with throughs also the bigger comb will be diff delay on dif frequencies cuz maybe not much harmonic content for that delay on that point throughs and boosts on octave also not as big, and also, you hear 2 distinct notes (def the more up and up u go in freq) but only low octave porblem cuz absolute freq so close to eachother almost same freq so close to same waveform and also octave so lot of in phase stuff harmonic stuff?
so if lowest fundamental tone is 2ms then can never cancel out stuff like 8ms of first waveform?

//do chords with sine wave also kinda adding harmonics, tho very loud, but u can still see kind of square wavy timbre.

## TODO

PHASE CANCELLATION OFTEN USED FOR ACAPELLAS IF U GOT THE SONG AND THEN INSTRUMENTAL JUST REVERSE POLARITY OF INSTRUMENTAL AND THUS THE WHOLE INSTRUMENTAL WILL (HOPEFULLY) CANCEL OUT
EXCEPT THE VOICE. SAME WITH NOISE CANCELLATION? OTHER APPLICATIONS?

ALSO ADD "PHASE CANCELLATION ISSUES IN PRACTICE" so like with double mic recording maybe bass layering like mainly in lows add a header, same with sample and sample rate add a # IN PRACTICE to get a nice overview after the full explanation.
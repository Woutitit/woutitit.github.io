compressor attenuates the whole frequency spectrum at that point when a peak goes up, it's not just the frequency (band) where the peak is happening. This is totally ok as the transient may be hidden all accross the spectrum and thus with a MB compressor you wouldn't be able to fully compress the transients (of course you could have multiple bands but that's a bit of a hassle). It may also be more handy in sidechaining if you want the whole sound to duck and pump. If you only want to sidechain the sub frequencies then of course an MB can be handier so it all depends:
https://old.reddit.com/r/musicproduction/comments/oq8zre/how_to_hear_compression/h6cg4s4/

compressing is all about a delicate act of balancing, too punchy vs keeping punch too much transients vs enough transients to be audible, sustain vs too little

## Introduction
Note that this is a more general compression article. More specific articles may come out too (like how to compress a kick drum).

## Normal compressor: Basic usage
### Step 1: Determine the type of sound
Knowing how and what to compress starts with **knowing your sound**. The reason for this is that the same exact compression settings will do different things and get you different results based on the type of sound you have.

Usually you'll want to distinguish between two broad categories: short (transient) and long sounds (sustain). While usually synonymous with short/long sound, you'll also want to seperately determine whether the sound has more of a transient-y clicky *role* or more of a sustain-y smooth role. Reason for this is because you can have for example a piano which can either be played very stabby or be played with mainly sustained background chords. If the piano is (mainly) used in a stabby way, you'll probably want to lean towards transient-y role and vice versa for the sustain piano.

Of course, it's not a 0 or 1 situation. A sound, like a piano, may be both short and long sounding and may have more of a smooth role but you want to keep some transients in, then that's totally fine. You can achieve the smoothness you want while still retaining that transients (which you sometimes may not want, as transients do call attention to a sound, which may not be desireable for a background smooth sustain sound).

Classic examples of short sounds are usually drums, percussion and plucks.

### Step 2: Determine why to compress
The next step is determining why you want to compress at all because regardless of type of sound, not all sounds necessarily need to be compressed (that much). The following are the usual reasons to compress:
- Taming peaks
- Bringing out body/sustain/fatness
- (Sidechaining)

Try to listen to and look at your waveform to determine this one and mainly look at the dynamic range. Look at the dynamic range of the sudden peaks, usually synonymous with transients, compared to the body. Then also look at the dynamic range of the body compared to the body/tail of the sound.

Also, note that sometimes you do not need (much) compression at all. Sometimes the samples (especially drums) are already compressed (like kicks and stuff), which you can see on the waveforms, and/or they may actually already be fully usuable.

// Say a bit more why

### Step 3: Set ratio and threshold
To start compression, first we'll want to set the threshold and ratio. More, specifically you want to start with the treshold first. This is because the threshold determines what part of the signal gets put under (potential) control of the compressor. Meanwhile the ratio determines how much gain reduction will be done but that does mean that it can simply not reduce the gain of certain parts in a sound if the threshold is not low enough. Similarly, a ratio will also compress parts of a sound that we don't want to if the threshold is too low. Therefore, setting the treshold first is important because it dictates what part of the sound will be compressed. We can then use ratio, attack and release to attenuate the compression.

*Note: In reality, you don't need to be super specific with threshold. Usually you just set first where it seems ok and then later you may tweak it a bit.*

Setting the htreshold is straight forwards when we're reducing tbe absolute highest of peaks (see later). In fact, we usually use a limiter for that. What we want to do is set the threshold low enough so that the transients are reduced enough so they aren't obnoxious anymore (but not too low to not cut off too much of the transients). Setting the threshold high is an easy choise because we're using extreme settings (high ratio, usually limiting) to abruptly cut peaks and thus we don't want any part of the sound but the peaks to be affected by those settings.

For the next more **sound shaping** compressor (also see later) it's more tricky.

That said, usually a lower threshold setting is what we want here as we do want to be able to shape way more parts of the sound which are all at various dynamic ranges (like the transient, body and tail, quieter parts in the performance, etc.). How low depends a bit, though. If you want literally no dynamic range and you want to super smooth stuff, go super deep low and put no attack and ratio all the way up. If you still want smooth but not endless smooth you can put the ratio a bit up or maybe the treshold or maybe both. If you want some transients before the smoothness, you can also set a slower time. Similarly though, if you want super punch you can set your threshold real low too and have a slower attack (slow release too for exageration) and a high ratio again. 

Generally, though, **for a good starting point you can set your threshold at where it would (potentially?) reduce -6db in gain (gain reduction) (loudest peaks?) and then ratio at 4:1 or 3:1**. Then start playing with your attack and release to shape the sound. If you then think there is not enough shaping going on, you may want to first try and lower the threshold and then you may want to up the ratio too.

Also, you don't necessarily want to go too low on the threshold as it may be hard to correctly compress all the sound under control now. It may also be that you're compressing a multi-loop and you may only want to compress the kick and snare (so settings for kick/snare not for the hat) so in that case you probably don't want to catch the quieter hats in your compressor (as the settings are not made for it).

So in short what you want do for sound shaping:
1. Set threshold at -6db gain reduction
2. Set ratio at 4:1 or 3:1
3. Play with attack and release to shape sound
4. If need more strong gain reduction, adjust the ratio (try first before threshold moving)
5. If need more sound to be caught into the compression, adjust threshold

### Step 4: Setting attack and release
So, let's first start with **a short sound, a kick or a snare**. 

A snare usually has a tranient-y and punchy role so you do not want to get rid of transients and punch. That said, if you look at the waveform and listen to the start of the sound, the transients (around the first 10ms) may be too obnoxiously loud.

Therefore, out of all things, what you want do first in that case is add a peak compressor/limiter that simply cuts off all the peaks that are simply too big. These will usually be short transient sounds. Simply cut them off with a fast attack. Of course mind that you're not cutting too much. Transients are really important in this type of sound (because presence in mix) but we just want to cut the peaks that are absolutely obnoxiously loud. It doesn't really change the sound.

In the next compressor is where you're actually going to define and correct the sound. Again, in the context of the mix determine if there is too much/little transients, too/much little punch, too/much little fatness/body/sustain/tail. 

For transients (and punch) you're looking at the attack knob. **A fast attack (< 10ms) will reduce transients and punch, a slow attack (> 10ms) will retain the transient and punch** we already have and depending on the settings and slowness of the attack may even enhance it. For transient-y sounds we're usually looking for a slower attack. That said, too slow of an attack and our drums may be too punchy and transienty and have too much dynamic range which may not be ideal in terms of fatness and master limiting.

Then for the body and tail of the sound, you're looking at release. To beginner ears, the body and tail may sound like the punch and while the beginning of the body may indeed have some punch, body and especially tail don't add any punchiness to the sound. Either way, the release knob controls the body/tail. **A short release (< 10ms?) adds body (and tail) and therefore a more aggressive/longer/fat snare (with a really short release even distorting adding even more aggressiveness). A long release (> 10ms?) either retains the current body/tail or may even remove it at longer release times.** Usually aggressive and big snares will get shorter release times while more tight and subtle snares get longer ones (of course it's a spectrum not a 1 0 situation here too). Too slow release and again your body/tail may dissapear in terms of dynamic range making your snare end up too punchy again.

In short, a short attack and a short release is the ultimate way of reducing dynamic range and making your snare sound fat. However, it also sucks any transient/punch out of the snare and it probably sounds super duper aggressive/distorted.

Also, all the stuff above goes for the same for kick, by the way, and basically any short transient-y sounds (like plucks). That's why it's handy to distinguish like this.

Then, for a more sustainy sound, say a piano, you have to think about the settings a tiny bit differenlty. For example, you may again do the peak limiter for the absolute highest peaks/transients. However, as with a vocal, usually you'll have a more smooth wave and a more smooth and longer dynamic range over time so reducing the dynamic range for consistency/sustain sake you usually don't want to as aggressive as on drums.

So, in case of longer sustain sounds, the attack knob doesn't mainly mean adding/removing punch/transients. It simply means how much or little transients/punch you want in your smooth sound but it's not as important as with shorter sounds. Nonetheless, transients is important for defining timbre so probably in your audible and upfront stuff you still want it (longer attack) and in your background smooth pads you may want get rid of it just to get out of the way of stuff (shorter attack). Ultimate smoothness is 0 attack.

For the release, it's not necessarily about aggressiveness and fatness since it's a long sound. Of course a shorter release may distort so it can help a bit in fatness that way but on longer sounds you'll hear the distortion much quicker and better so you don't want to go too short on the release usually (around 40ms good starting point). That said, you don't want to go too long on the release either (see below note) but basically you'll want your release where it's (almost) not distorting the sound but if you want aggressiveness (as in, audible distortion) you could do shorter release although you may want to use a real distortion plugin for that instead.

*Important: Also note that with release that you don't want it too long. You usually want your compressor to be fully released before any next note hits. Else, you may have one note hitting at a certain db, another note at another db again (as they both aren't fully released in loudness and maybe at different points hit again) but never even at max volume unless there is some time in between hits.*

Don't forget to compensate with makeup gain for the gain reduction of the compressor to hear the difference.

## Todo
- What's with the -6db (for highest peaks) 3:1 4:1? Why a good starting point for compression in terms of threshold/ratio? I guess not too much and not too little compression so can go from there.

## Relevant articles
- Compression, limiting, clipping


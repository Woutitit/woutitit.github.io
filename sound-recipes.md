# Sound recipes
## Pluck
Common way to pluck is to instead of having the ADSR of the volume short, have the ADSR of the cut off filter short and inver it so that it goes from "allow all frequencies" to "allow none" and downwards from high to low. Gives it this extra typical EDM vibey sound and on top of that gives you this common modulation macro where you can open up the filter essentially making your pluck slowly more and more legato (so from staccato to legato really):
- https://www.youtube.com/watch?v=mfyacc6iWTE at 5:09
- https://www.youtube.com/watch?v=fO_JkNN7gh4

## Basses
Like EDM dnb dubstep basses i mean here more.

## Supersaws
- https://www.youtube.com/watch?v=OJn9_Y58jDU

Cut off also depends heavily on the genre. Usually you can cut off at 75Hz but then in the mid range you may find you shelving a bit until 500-600Hz. and perhaps from 2.5-5K Hz you may be boost shelving the highs a bit for extra presence. You may nonetheless cut off like the top 18-20kHz for the harshness but you can roll of more if the genre calls for it. Reference track it.

Unison/Detune/Layer. Two saw stacks is done but then +1 and/or detune one of the saws (which adds thickness, usually mixed in a bit lower). You may also layer with a square. You may want to layer a mono and a stereo layer an depending on genre you want the saws to be less or or more paddy or floaty you want to either mix in the stereo or mono more. Octave layer is also common, if you don't have that, then you might need thicker chords if important.

So 3 possible layers:
- Mono layer (or not if not needed)
- Stereo layer (or 2nd oscillator)
- Octave layer (or 2nd oscillator)

Voicings? Usually extensions on top? Where start? Usually have root and then fifth and then root and then fifth and then maybe extensions. Be aware of repeating a note too many times as it may create too much resonance and stuff. Don't make stuff too dense, but not too sparse. Again all depends on genre how dense or not dense and how low and or high the saws need to reach. Also, sometimes, voicings don't need to be all fully on top. you could have a third in the middle but then the 9th more on top not to clash or sound better.

Vocoder? Resonator saw? If you have a heavy mid bass, you 

### Automation and modulation
On stabs, often you may automate the filter cut off. Having them come in (usually not fully from 0 though) and increase in loudness. Makes them more interesting and less busy.

## Chiptune-y lead
Examples:
- https://www.youtube.com/watch?v=OJn9_Y58jDU
- https://www.youtube.com/watch?v=GM7JtFZ5yyU
- https://www.youtube.com/watch?v=nTArSq_oqz4
- https://www.youtube.com/watch?v=mfyacc6iWTE

This lead is very often not a preset, just a basic waveform shape. In fact, in Serum there is actually a basic wavetable called "Basic Shapes", and if you browse through the wavetable positions you'll find some basic shapes. Often the one(s) looking like a pulse (for that classic PWM vibe) are/is chosen there.

As far as modulations go. You may choose to either assign them to an ADSR envelope, an LFO or a macro/mod wheel (and use automation clips). Usually automation clips are chosen but if the modulations(s) need(s) to always be the same and always trigger at the same time and/or repeat you may choose an envelope or an LFO.

Usually vibrato and warp mode (sync) are the common combo, anything else is flavor and unnecessary. You can choose to either have those in a macro knob together or seperate if you want full control. 

For vibrato, you'll usually want to do it on sustained notes and/or on accent or impact notes (like note leaps maybe). You'll also want the vibrato to end right when the next note plays (no fade out) and the fade in can be a bit more gradual but also kind of sudden (automation looks like a shark fin kind of). In terms of settings it's up to taste, see the sass video for his settings but he had an LFO at 9.6kHz speed to the fine tune knob. Also see "Software" article for how to setup vibrato in synths like Serum.

For warp mode, you may choose sync but other warp mode options like pwm are also used. In case of sync you may choose to do window sync (especially for softer sounds). With sync the automation curve, if not used with vibrato, maybe more gradual up and down (never max or min really, so it's more gradual but you may have some sudden jumps on impact and accent notes, like in leaps).

Often doesn't seem to be any unison, just a single voice (but need more data on that). I guess that's so it has a strong center/mono presence. However, it's not uncommon to layer this with a more plucky timbre (like a bell an octave up) or perhaps with a different timbre (like a piano) or whatever. It depends on song and section.

In terms of FX:
    - (Tube) saturation: Just a tiny bit. Can also just be a bit of waveshaping. Again for slightly more RMS and high-end presence.
    - OTT compression (or MB in serum): You may want a bit from it. Again, will bring out the high-end.
    - EQ: 
        - Sound: Perhaps a slight 2-3db shelf boost starting from 2.5-5kHz again to boost the highs. Can use in place of OTT and/or together as it kind of does the same.
        - Mixing: May want a cut starting at 100Hz, a bit of shelving up till 500-600Hz and perhaps boost slightly around 2.5-5kHz and perhaps from 10kHz cut slightly for harshness.
     - Dimenion for stereo width: Usually size quite down low, mix something like 30-60%.
     - Reverb for width and space: Size down low. Perhaps slightly cut lows. Mix also to the lower side.
     - Chorus. A tiny bit of chorus for stereo. Can be used in place of dimension (or together). Again, don't want much, jsut a tad.
     - Delay. Not always necessary but you might want to put a ping pong delay with a very low mix-in.

So yeah, it's mainly about giving the lead enough presence to cut through and also having a bit of stereo width whilst also still having a strong mono and centered presence. The rest is kind of fluff and up to taste.

Then the last main thing is the mono and/or porta. I don't immediately recall the difference. But basically they allow for gliding notes and basically pitch bending and fading into eachother when you basically write overlapping notes in your MIDI. This is common to do and you have to play with the settinfs (you also may only need mono or porta or sometimes both). I guess you may want to automate these for when you want pitch bends or when you don't?

the +1 or not cuz like extra harmonics but also like eq'ed out??? isnt that just bad?



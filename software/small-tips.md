# Software tips (FL, Synths, VSTs, etc.)
As the title state, this is some nice helpful tips on software. It's home to useful hot-key combos, how to do certain things in software (e.g. make a vibrato in x or why synth, how to use a certain sample library) and those sorts of things. It shouldn't be super in depth but stuff can be explained.

## Diva
### Enable MIDI velocity
In Diva there is a VEL lever. Pull it full up to have Diva get fully affected by the MIDI velocity notes in the FL Studio piano roll. Anything less and Diva will be less affected by it.

## dBlue Glitch (1.3)
It's the earlier but free version of Glitch 2 and similar to Effectrix (though effectrix is more capable probably). It's a handy tool because you can create cool fx with very little effort. Like, you hear often PSYQUI stuff that is super glitch and stuttery on some notes, well you can do that in Glitch 2.

It's very easy. First you lay down a chord pattern (it can be sustained or it can be in the rhythm that you want or a hybrid it depends) and then you add Glitch and you can choose how to glitch the chord pattern.

Beneath you'll see a couple of FX like tapestop and gate which are all FX/automations that you can choose from and then above it you have a step sequencer similar to the one in FL. Now all you need to do is add FX in the step sequencer. If you want gate to be added on beat 4 and for a duration of a full beat then you add a full beat gate in the sequencer on beat 4 of your chord pattern. And same with other stuff. You can pretty much divide the stuff how you want, you can add blanks and even random stuff in which you may find useful cool sounds.

Use this stuff on a lot of sounds, it usually gets used on like piano and as like fills often the gate gets used and crushers and stuff. Like listen to a lot of these Japan artists like PSYQUI where you can clearly heaar it. Some other common uses case? Link here.

Also, a few tips, you can automate the settings of each glitch fx of course so that when the fx triggered you can still have it be a bit different if you want/need to. It may also be cool to add Glitch on a bus or even the master if you want some section to glitch a whole section or even song for a moment.

## Serum
See manual. For me it's here currently: file:///C:/Users/Wout/Documents/Xfer/Serum%20Presets/Serum_Manual.pdf
### Pitch controls
So there are four ways to control pitch of a single oscillator and then on top of that for the whole synth you have a master tune control which affects all the oscillators.

You have the "oct", "sem", "fin" and "crs" and you can do similar things with it as they all have to do with pitch. They are still different. The oct for example counts in octaves which is nice if you want an added octave layer. It's less nice if you want to smoothly modulate pitch over multiple octaves. For that you can use CRS. For more finetuned stuff or to put some slight detune LFO-ish vibe to your synth you may want to go less obvious so you can use "fin" for that which goes up or down to 100 cents only. And then lastly you have the "sem" which is a bit of hybrid between oct and crs. You can't go octaves with it but you can still modulate in a fast way or you can add like fifths harmony layers or something easily with it.

Therefore, in terms of for example vibrato, you can technically use CRS, fine tune or the master tune ("sem" and "oct" to abrupt for vibrato).

#### Vibrato
- https://www.youtube.com/watch?v=HlOkdtr-fng
- https://www.youtube.com/watch?v=OJn9_Y58jDU&t=1s

There are a multiple pitch controls in Serum (see above) so there are multiple ways to vibrato. It depends on what you want or need. The main questions are if you need all your OSCs to vibrate or just one (or if you want to control vibrato of each OSC independently) and also how much vibrato you may need. If you're ok with a bit of vibrato you may use "fin" if you (sometimes) need large vibrato you may want "crs".

But yeah in the case of single OSC vibrato all you need to do is add an LFO to a pitch control and then in the matrix tab set the aux to a macro so that you can control when the vibrato turns on/off. Main thing here to control is how much vibrato you want to let through, how fast the vibrato goes (LFO rate) and how much pitch change the vibrato can (maximally) do.

Then, in case of all OSCs you'll want to modulate the master tuning. You can do that in the matrix. Source is LFO of choice, destination is master tuning and auxiliar is again macro of choice. As last time, modify parameters to taste (see videos).

# Software tips (FL, Synths, VSTs, etc.)
As the title state, this is some nice helpful tips on software. It's home to useful hot-key combos, how to do certain things in software (e.g. make a vibrato in x or why synth, how to use a certain sample library) and those sorts of things. It shouldn't be super in depth but stuff can be explained.

## FL Studio
## Tips
### Automation clips
It seems right now, it's a bit of a drag to organize automation clips since you cannot truly shorten them. Therefore, if you don't need the automation clip running for the whole song, for your own sake, you are best to just hightlight a small portion and then make the clip as big as you need it it to be. Easier reuse and you can actually merge short clips together like that.

### Shortcuts
- [comprehensive_compilation_of_advanced_fl_studio shortcuts](https://old.reddit.com/r/FL_Studio/comments/ep7jlf/comprehensive_compilation_of_advanced_fl_studio/)
- https://www.youtube.com/watch?v=RBw-pdqus3k&t=88s

Ctrl + T in playlist = timestamp
Ctrl + G when selecting multiple patterns = merging (works both vertically and horizontally)
Ctrl + Alt + G Same as above but for automation clips
Alt + Dragging (?) on velocity = normalizing notes on default velocity

### Troubleshoot
#### 3rd-party VSTs lose focus after knob tweak
On top of your VST (on the Fruity Wrapper top bar) you'll see to the right (somewhere next to the 'x' icon) a keyboard thingy. You have to toggle that (see below picture, though, on the picture you can't see it well as it's half out of frame):

![nklz651m1x461](https://user-images.githubusercontent.com/17428965/113638649-a648de00-9677-11eb-8427-04c95c4888af.png)

#### I forgot to record my MIDI keyboard
Go to Tools > dump latest recorded score to recover what you've played in a pattern.

## Synths
### Serum
#### Vibrato
- https://www.youtube.com/watch?v=OJn9_Y58jDU&t=1s

There are a few ways to vibrato. The main way is either to add an LFO to the fine tune and if you need both oscillators to vibrato you have to add an LFO to the master tuning. Not sure about the master setting but for fine tune, simply drag LFO (unchanged) to the fine tune of an oscillator, then I think you can drag your macro to that fine tune (or do it as auxiliary in matrix tab, same thing I think). For the master tuning you have to go into matrix and basically assign lfo 1 to master tune parameter. And then you have to assign that to auxiliary a macro (or mod wheel). 

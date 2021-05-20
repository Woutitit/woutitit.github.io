# Software tips (FL, Synths, VSTs, etc.)
As the title state, this is some nice helpful tips on software. It's home to useful hot-key combos, how to do certain things in software (e.g. make a vibrato in x or why synth, how to use a certain sample library) and those sorts of things. It shouldn't be super in depth but stuff can be explained.

## FL Studio
## Tips
### Setting up a template
Setting up a template is the same as making a project file. Of course in a template project rather than composing a song you may add some preprogrammed automation, synth racks, coloring if you're into that, send tracks and stuff like that. Add anything that'll make your life easier.

The template needs to be saved in a location similar to D:\Program Files\Image-Line\FL Studio 20\Data\Templates (So depends on your drive). Also, once you opened the template I think it actually automatically becomes your default template too. Cool!

One note, saving it in the templates folder will make it be recognized as a template so anything you then do in the template is seen as a project and you can save it as is. If you want to edit the template file, instead of starting a "File > new" project you'll need to directly open the template file itself and then safe stuff to it.

### Volume automation SC
- https://www.youtube.com/watch?v=9LyciXjMD-U

Usually you have one (or more depending on whether you need different slopes for different instruments) or more SC inserts and everything that needs to have sidechaining you disconnect the direct routing to the master and instead feed it to the SC insert to your liking (and then the SC goes to master).

A basic volume automation SC starting point is a beat long and has two points, one half way the beat and one at the end of the beat. The half way one is usually at full volume (0.8 in value) so from there it's horizontally to the end and from the start to the half is a straight linear line. This is a good starting point but the slope will depend on kick and/or effect you want. Also the half way point does not need to be at full volume already, you may want to lower it a bit and have a bit of a slope until the end. Again depends on your kick and/or effect you want. Finally, for the automation, don't use the fader but use "Fruity Balance" for more flexibility.

Protip: Make a sidechain automation preset under "Channel presets" and/or even make a template with a SC route already ready. Something like Synthion who has a SC lane and already 1 bar (4 beat) of 4 SC automations). See: https://www.youtube.com/watch?v=MDkJckTswJQ.

#### Automation clips
- https://itsgratuitous.com/the-ultimate-guide-to-using-automation-clips-in-fl-studio-20/#fl-snapshot-initialized-controls

It seems right now, it's a bit of a drag to organize automation clips since you cannot truly shorten them. Therefore, if you don't need the automation clip running for the whole song, for your own sake, you are best to just hightlight a small portion and then make the clip as big as you need it it to be. Easier reuse and you can actually merge short clips together like that.

### Shortcuts
> If you hover over certain tools it may give you a shortcut option.

- https://www.image-line.com/fl-studio-learning/fl-studio-online-manual/html/basics_shortcuts.htm
- [comprehensive_compilation_of_advanced_fl_studio shortcuts](https://old.reddit.com/r/FL_Studio/comments/ep7jlf/comprehensive_compilation_of_advanced_fl_studio/)
- https://www.youtube.com/watch?v=RBw-pdqus3k&t=88s

#### Mixer
Ctrl + drag = select multiple tracks

#### Playlist
Shift + P = select draw
Shift + B = select brush
Shift + C = select cut
Shift (in playlist) = cutting
Ctrl + T in playlist = timestamp
Ctrl + G when selecting multiple patterns = merging (works both vertically and horizontally)
Ctrl + Alt + G Same as above but for automation clips
Alt + Dragging (?) on velocity = normalizing notes on default velocity
Ctrl + Drag = Keep vertically aligned whilst dragging
Shift + Drag = Keep horizontally aligned whilst dragging
Shift + Cut = Keep straight while cutting

### Troubleshoot
#### 3rd-party VSTs lose focus after knob tweak
On top of your VST (on the Fruity Wrapper top bar) you'll see to the right (somewhere next to the 'x' icon) a keyboard thingy. You have to toggle that (see below picture, though, on the picture you can't see it well as it's half out of frame):

![nklz651m1x461](https://user-images.githubusercontent.com/17428965/113638649-a648de00-9677-11eb-8427-04c95c4888af.png)

#### I forgot to record my MIDI keyboard
Go to Tools > dump latest recorded score to recover what you've played in a pattern.

#### Controls jump up when replayed
- https://itsgratuitous.com/the-ultimate-guide-to-using-automation-clips-in-fl-studio-20/#fl-snapshot-initialized-controls
If you ever initialized a control with an automation clip, the state is now saved in FL so even when the automation clip isn't there, the initial state of what you had will be the state your sound will jump to (like the volume fader or whatever).

## Synths
### Serum
#### Vibrato
- https://www.youtube.com/watch?v=OJn9_Y58jDU&t=1s

There are a few ways to vibrato. The main way is either to add an LFO to the fine tune and if you need both oscillators to vibrato you have to add an LFO to the master tuning. Not sure about the master setting but for fine tune, simply drag LFO (unchanged) to the fine tune of an oscillator, then I think you can drag your macro to that fine tune (or do it as auxiliary in matrix tab, same thing I think). For the master tuning you have to go into matrix and basically assign lfo 1 to master tune parameter. And then you have to assign that to auxiliary a macro (or mod wheel). 

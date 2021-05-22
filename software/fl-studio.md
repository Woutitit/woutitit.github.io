# FL Studio
## Patcher
- https://www.youtube.com/watch?v=N11la5x5MDk&
- https://www.youtube.com/watch?v=AMCm6qtYkh8 (See patcher trick chapter)
- https://www.image-line.com/fl-studio-learning/fl-studio-online-manual/html/plugins/Patcher.htm

Patcher is a very handy tool that is there to improve and visualize your workflow and can be either used as an instrument or an effect. What you can do in Patcher is visually add VSTs, such as Serum, and then on top of that add all kinds of post-processing fx to it. Or, you can use it as an FX and you can route your signal through the patcher instance. 

So it's mostly handy for preset saving and then for the visual and drag-and-droppy stuff for people that prefer to do stuff visually.

### Saving instruments with multiple layers and post-processing
It's very common that you have a certain sound that either comprises of multiple layers or has certain post-processing to make it the sound that it is. For example, check out the Mo Falk video, it's very common in modern house to have your basic bass have at least a sub, a mid crunch and then a side crunch layer. On top of that he also does a ton of fattening and compression in post. 

Now, the sound itself is very good and can actually be used in multiple of his tracks but there is no way to save all of the layers and post-processing...unless with patchers. So, you don't even need to have made the patches initially in Patcher but once you are satisfied you can drag everything in patcher and have all of it saved as a nice patcher preset that you can drag in fully ready.

Of course, sometimes you may want to save presets but without post-processing or layers so regular presets without patcher are ok too. Or maybe you want to save the presets but without certain FX so you can make a seperate patcher again with only the FX (and layers) you want as a preset.

### Parallel processing
It's very common to EQ your delays and your reverbs without the EQ affecting our original sounds. For this you'd need multiple send mixer tracks. In patcher, however, all you need to do is simply have two paths, one with your dry signal and then the other with your reverb (again want to have 100% wet on these fx) and then afterwards an EQ and then at the end you let them both go to the output. Easy!

Now, I don't kow about PP when multiple instruments need the same PP how to reuse the patcher (I guess multipe patcher presets or better way?) but yeah it's cool.

There are also other parallel processing ways. Like maybe you want your sound to be crunchy and distorted but you don't want to run it through the reverb so again you make multiple paths and stuff.

### Visualizing
Doing stuff in patcher may also just help visualize your signal flow better, certainly if you have multiple parallel routing/processing going on. So for the visual learners it's just something cool.

## Setting up a template
Setting up a template is the same as making a project file. Of course in a template project rather than composing a song you may add some preprogrammed automation, synth racks, coloring if you're into that, send tracks and stuff like that. Add anything that'll make your life easier.

The template needs to be saved in a location similar to D:\Program Files\Image-Line\FL Studio 20\Data\Templates (So depends on your drive). Also, in settings you can change the default template to yourq id you want to use it for most projects anyway.

One note, saving it in the templates folder will make it be recognized as a template so anything you then do in the template is seen as a project and you can save it as is. If you want to edit the template file, instead of starting a "File > new" project you'll need to directly open the template file itself and then safe stuff to it.

## Volume automation sidechaining
- https://www.youtube.com/watch?v=9LyciXjMD-U

Usually you have one (or more depending on whether you need different slopes for different instruments) or more SC inserts and everything that needs to have sidechaining you disconnect the direct routing to the master and instead feed it to the SC insert to your liking (and then the SC goes to master).

A basic volume automation SC starting point is a beat long and has two points, one half way the beat and one at the end of the beat. The half way one is usually at full volume (0.8 in value) so from there it's horizontally to the end and from the start to the half is a straight linear line. This is a good starting point but the slope will depend on kick and/or effect you want. Also the half way point does not need to be at full volume already, you may want to lower it a bit and have a bit of a slope until the end. Again depends on your kick and/or effect you want. Finally, for the automation, don't use the fader but use "Fruity Balance" for more flexibility.

Protip: Make a sidechain automation preset under "Channel presets" and/or even make a template with a SC route already ready. Something like Synthion who has a SC lane and already 1 bar (4 beat) of 4 SC automations). See: https://www.youtube.com/watch?v=MDkJckTswJQ.

## Automation clip shortening
- https://itsgratuitous.com/the-ultimate-guide-to-using-automation-clips-in-fl-studio-20/#fl-snapshot-initialized-controls

It seems right now, it's a bit of a drag to organize automation clips since you cannot truly shorten them. Therefore, if you don't need the automation clip running for the whole song, for your own sake, you are best to just hightlight a small portion and then make the clip as big as you need it it to be. Easier reuse and you can actually merge short clips together like that.

## Shortcuts
> If you hover over certain tools it may give you a shortcut option.

- https://www.image-line.com/fl-studio-learning/fl-studio-online-manual/html/basics_shortcuts.htm
- [comprehensive_compilation_of_advanced_fl_studio shortcuts](https://old.reddit.com/r/FL_Studio/comments/ep7jlf/comprehensive_compilation_of_advanced_fl_studio/)
- https://www.youtube.com/watch?v=RBw-pdqus3k&t=88s

### Mixer
- Ctrl + drag = select multiple tracks

### Playlist
- Shift + P = select draw
- Shift + B = select brush
- Shift + C = select cut
- Shift (in playlist) = cutting
- Ctrl + T in playlist = timestamp
- Ctrl + G when selecting multiple patterns = merging (works both vertically and horizontally)
- Ctrl + Alt + G Same as above but for automation clips
- Alt + Dragging (?) on velocity = normalizing notes on default velocity
- Ctrl + Drag = Keep vertically aligned whilst dragging
- Shift + Drag = Keep horizontally aligned whilst dragging
- Shift + Cut = Keep straight while cutting

## Troubleshoot
### 3rd-party VSTs loses focus after knob tweak
On top of your VST (on the Fruity Wrapper top bar) you'll see to the right (somewhere next to the 'x' icon) a keyboard thingy. You have to toggle that (see below picture, though, on the picture you can't see it well as it's half out of frame):

![nklz651m1x461](https://user-images.githubusercontent.com/17428965/113638649-a648de00-9677-11eb-8427-04c95c4888af.png)

### I forgot to record my MIDI keyboard
Go to Tools > dump latest recorded score to recover what you've played in a pattern.

### Controls (like fader) jump to different value when pressing play
- https://itsgratuitous.com/the-ultimate-guide-to-using-automation-clips-in-fl-studio-20/#fl-snapshot-initialized-controls
If you ever initialized a control with an automation clip, the state is now saved in FL so even when the automation clip isn't there, the initial state of what you had will be the state your sound will jump to (like the volume fader or whatever).
